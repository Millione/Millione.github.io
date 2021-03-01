---
layout:     post
title:      "LinkedHashMap"
subtitle:   " \"JDK源码\""
date:       2020-11-27 11:00:00
author:     "LiuJ"
header-img: "img/post-bg-2020.jpg"
catalog: true
tags:
	- LinkedHashMap
    - JDK源码
---

## LinkedHashMap

LinkedHashMap 继承自 HashMap，意味着 LinkedHashMap 拥有 HashMap 的特性，但其更加强大，这体现在：

- LinkedHashMap 内部维护了一个双向链表，解决了 HashMap 不能保证遍历顺序和插入顺序一致的问题；
- LinkedHashMap 的元素访问顺序提供了近期最少使用（LRU）访问原则。 

![](https://raw.githubusercontent.com/Millione/pb/master/img/20201030154119.png)

### 1. 创建节点

1. LinkedHashMap 中对 Node 节点进行拓展，用以实现双向链表。

```java
static class Entry<K,V> extends HashMap.Node<K,V> {
   Entry<K,V> before, after;
   Entry(int hash, K key, V value, Node<K,V> next) {
       super(hash, key, value, next);
   }
}
```

2. 添加新节点时没有重写 put 方法，只是重写了 newNode 方法，完成双向链表的连接操作。

```java
Node<K,V> newNode(int hash, K key, V value, Node<K,V> e) {
    LinkedHashMap.Entry<K,V> p =
        new LinkedHashMap.Entry<K,V>(hash, key, value, e);
    // 将 Entry 接在双向链表的尾部
    linkNodeLast(p);
    return p;
}

/**
* 该引用始终指向双向链表的头部
*/
transient LinkedHashMap.Entry<K,V> head;

/**
* 该引用始终指向双向链表的尾部
*/
transient LinkedHashMap.Entry<K,V> tail;

// newNode 中新节点，放到双向链表的尾部
private void linkNodeLast(LinkedHashMap.Entry<K,V> p) {
    // 添加元素之前双向链表尾部节点
   LinkedHashMap.Entry<K,V> last = tail;
   // tail 指向新添加的节点
   tail = p;
   // 如果之前 tail 指向 null 那么集合为空新添加的节点 head = tail = p
   if (last == null)
       head = p;
   else {
       // 否则将新节点的 before 引用指向之前当前链表尾部
       p.before = last;
       // 当前链表尾部节点的 after 指向新节点
       last.after = p;
   }
}
```

### 2. 删除节点

LinkedHashMap 同样没有重写 remove 方法，只是对 afterNodeRemoval 方法进行了实现。

```java
//  从双向链表中删除对应的节点 e 为已经删除的节点
void afterNodeRemoval(Node<K,V> e) { 
    LinkedHashMap.Entry<K,V> p =
        (LinkedHashMap.Entry<K,V>)e, b = p.before, a = p.after;
    // 将 p 节点的前后指针引用置为 null 便于内存释放
    p.before = p.after = null;
    // p.before 为 null，表明 p 是头节点 
    if (b == null)
        head = a;
    // 否则将 p 的前驱节点连接到 p 的后驱节点
    else
        b.after = a;
    // a 为 null，表明 p 是尾节点
    if (a == null)
        tail = b;
    // 否则将 a 的前驱节点连接到 b 
    else 
        a.before = b;
}
```

### 3. 维护节点访问顺序

1. HashMap 的遍历结果跟添加元素顺序无关系，LinkedHashMap 的遍历结果就是添加元素顺序。
2. 双向链表 accessOrder 参数，当其构造函数传入为 true 时，在 put/get/replace 方法后跟着 afterNodeAccess 方法，用于维护节点顺序。

```java
// 是否维护双向链表中的元素访问顺序
final boolean accessOrder;

public LinkedHashMap(int initialCapacity, float loadFactor) {
   super(initialCapacity, loadFactor);
   accessOrder = false;
}
 
public LinkedHashMap(int initialCapacity) {
        super(initialCapacity);
        accessOrder = false;
}

public LinkedHashMap() {
        super();
        accessOrder = false;
}

public LinkedHashMap(Map<? extends K, ? extends V> m) {
   super();
   accessOrder = false;
   putMapEntries(m, false);
}

// 可以指定 LinkedHashMap 双向链表维护节点访问顺序的构造参数
public LinkedHashMap(int initialCapacity,
                         float loadFactor,
                         boolean accessOrder) {
        super(initialCapacity, loadFactor);
        this.accessOrder = accessOrder;
}

// 将被访问节点移动到链表最后
void afterNodeAccess(Node<K,V> e) { // move node to last
   LinkedHashMap.Entry<K,V> last;
   if (accessOrder && (last = tail) != e) {
       LinkedHashMap.Entry<K,V> p =
           (LinkedHashMap.Entry<K,V>)e, b = p.before, a = p.after;
       // 访问节点的后驱置为 null    
       p.after = null;
       // 如访问节点的前驱为 null 则说明 p = head
       if (b == null)
           head = a;
       else
           b.after = a;
       // 如果 p 不为尾节点 那么将 a 的前驱设置为 b    
       if (a != null)
           a.before = b;
       else
           last = b;
           
       if (last == null)
           head = p;
       else {
           p.before = last;
           last.after = p;
       }
       // 将 p 接在双向链表的最后
       tail = p;
       ++modCount;
   }
}
```

### 4. 高效操作

```java
final LinkedHashMap.Entry<K,V> nextNode() {
       LinkedHashMap.Entry<K,V> e = next;
       if (modCount != expectedModCount)
           throw new ConcurrentModificationException();
       if (e == null)
           throw new NoSuchElementException();
       current = e;
       // 直接指向了当前节点的 after 后驱节点
       next = e.after;
       return e;
   }

public boolean containsValue(Object value) {
    // 直接遍历双向链表去寻找对应的节点
   for (LinkedHashMap.Entry<K,V> e = head; e != null; e = e.after) {
       V v = e.value;
       if (v == value || (value != null && value.equals(v)))
           return true;
   }
   return false;
}

```

### 5. LRU 构建

1. 在 putVal 方法后跟着 afterNodeInsertion 方法，如果 removeEldestEntry 方法返回 true，则会在添加一个新元素后，删除双向链表的头节点。

```java
// HashMap 中 putVal 方法实现 evict 传递的 true，表示表处于创建模式。
public V put(K key, V value) {
   return putVal(hash(key), key, value, false, true);
}

final V putVal(int hash, K key, V value, boolean onlyIfAbsent,
                   boolean evict) { .... }


// evict 由上述说明大部分情况下都传 true 表示表处于创建模式
void afterNodeInsertion(boolean evict) { 
   LinkedHashMap.Entry<K,V> first;
   // 由于 evict = true 那么当链表不为空的时候 且 removeEldestEntry(first) 返回 true 的时候进入if 内部
   if (evict && (first = head) != null && removeEldestEntry(first)) {
       K key = first.key;
       // 移除双向链表中处于 head 的节点
       removeNode(hash(key), key, null, false, true);
   }
}

 // LinkedHashMap 默认返回 false 则不删除节点。 返回 true 双向链表中处于 head 的节点
protected boolean removeEldestEntry(Map.Entry<K,V> eldest) {
   return false;
}
```

2. 实现。

```java
public class LruCache<K, V> extends LinkedHashMap<K, V> {

   private static final int MAX_NODE_NUM = 2<<4;

   private int limit;

   public LruCache() {
       this(MAX_NODE_NUM);
   }

   public LruCache(int limit) {
       super(limit, 0.75f, true);
       this.limit = limit;
   }

   public V putValue(K key, V val) {
       return put(key, val);
   }

   public V getValue(K key) {
       return get(key);
   }
   
   /**
    * 判断存储元素个数是否预定阈值
    * @return 超限返回 true，否则返回 false
    */
   @Override
   protected boolean removeEldestEntry(Map.Entry<K, V> eldest) {
       return size() > limit;
   }
}
```

### 6. 总结

1. LinkedHashMap 拥有与 HashMap 相同的底层哈希表结构，即数组 + 单链表 + 红黑树，也拥有相同的扩容机制。
2. LinkedHashMap 相比 HashMap 的拉链式存储结构，内部额外通过 Entry 维护了一个双向链表。
3. LinkedHashMap 可以通过构造参数 accessOrder 来指定双向链表是否在元素被访问后改变其在双向链表中的位置。
4. afterNodeAccess 方法中会修改 modCount ,因此当在accessOrder 为 true 的模式下迭代 LinkedHashMap 时，如果同时查询访问数据，也会导致 fail-fast，因为迭代的顺序已经改变。

### 7. 参考

[LinkedHashMap](https://juejin.im/post/6844903590159450120)
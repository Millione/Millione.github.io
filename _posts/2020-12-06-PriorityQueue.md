---
layout:     post
title:      "PriorityQueue"
subtitle:   " \"JDK源码\""
date:       2020-12-06 11:00:00
author:     "LiuJ"
header-img: "img/post-bg-2020.jpg"
catalog: true
tags:
    - PriorityQueue
    - JDK源码
---

## PriorityQueue

PriorityQueue 优先级队列使用堆来实现，每个元素都有一个权重值，每次出队都优先弹出优先级最大或最小的元素，默认实现小根堆。

![](https://raw.githubusercontent.com/Millione/pb/master/img/20201105154828.png)

### 1. 基本属性

在优先级队列中，有两种方式比较元素，一种是元素的自然顺序，另一种是通过比较器 comparator 来比较。

```java
// 默认容量
private static final int DEFAULT_INITIAL_CAPACITY = 11;
// 存储元素
transient Object[] queue; 
// 元素个数
private int size = 0;
// 比较器
private final Comparator<? super E> comparator;
// 修改次数
transient int modCount = 0;
```

### 2. 构造方法

注意直接传入集合进行初始化的方式。

```java
public PriorityQueue() {
    this(DEFAULT_INITIAL_CAPACITY, null);
}

public PriorityQueue(int initialCapacity) {
    this(initialCapacity, null);
}

public PriorityQueue(Comparator<? super E> comparator) {
    this(DEFAULT_INITIAL_CAPACITY, comparator);
}

public PriorityQueue(int initialCapacity,
                     Comparator<? super E> comparator) {
    if (initialCapacity < 1)
        throw new IllegalArgumentException();
    this.queue = new Object[initialCapacity];
    this.comparator = comparator;
}

public PriorityQueue(Collection<? extends E> c) {
    if (c instanceof SortedSet<?>) {
        SortedSet<? extends E> ss = (SortedSet<? extends E>) c;
        this.comparator = (Comparator<? super E>) ss.comparator();
        initElementsFromCollection(ss);
    }
    else if (c instanceof PriorityQueue<?>) {
        PriorityQueue<? extends E> pq = (PriorityQueue<? extends E>) c;
        this.comparator = (Comparator<? super E>) pq.comparator();
        initFromPriorityQueue(pq);
    }
    else {
        this.comparator = null;
        initFromCollection(c);
    }
}

public PriorityQueue(PriorityQueue<? extends E> c) {
    this.comparator = (Comparator<? super E>) c.comparator();
    initFromPriorityQueue(c);
}

private void initFromPriorityQueue(PriorityQueue<? extends E> c) {
    if (c.getClass() == PriorityQueue.class) {
        this.queue = c.toArray();
        this.size = c.size();
    } else {
        initFromCollection(c);
    }
}

private void initElementsFromCollection(Collection<? extends E> c) {
    Object[] a = c.toArray();
    // If c.toArray incorrectly doesn't return Object[], copy it.
    if (a.getClass() != Object[].class)
        a = Arrays.copyOf(a, a.length, Object[].class);
    int len = a.length;
    if (len == 1 || this.comparator != null)
        for (int i = 0; i < len; i++)
            if (a[i] == null)
                throw new NullPointerException();
    this.queue = a;
    this.size = a.length;
}

private void initFromCollection(Collection<? extends E> c) {
    initElementsFromCollection(c);
    heapify();
}
```

### 3. 入队

元素不允许为 null，自下而上堆化。

```java
public boolean add(E e) {
    return offer(e);
}

public boolean offer(E e) {
    // 不支持 null 元素
    if (e == null)
        throw new NullPointerException();
    modCount++;
    // 取 size
    int i = size;
    // 元素个数达到最大容量，扩容
    if (i >= queue.length)
        grow(i + 1);
    // 元素个数加 1
    size = i + 1;
    // 如果还没有元素
    // 直接插入到数组第一个位置
    // 这里跟我们之前讲堆不一样了
    // java里面是从0开始的
    // 我们说的堆是从1开始的
    if (i == 0)
        queue[0] = e;
    else
        // 否则，插入元素到数组 size 的位置，也就是最后一个元素的下一位
        // 注意这里的 size 不是数组大小，而是元素个数
        // 然后，再做自下而上的堆化
        siftUp(i, e);
    return true;
}

private void siftUp(int k, E x) {
    // 根据是否有比较器，使用不同的方法
    if (comparator != null)
        siftUpUsingComparator(k, x);
    else
        siftUpComparable(k, x);
}

@SuppressWarnings("unchecked")
private void siftUpComparable(int k, E x) {
    Comparable<? super E> key = (Comparable<? super E>) x;
    while (k > 0) {
        // 找到父节点的位置
        // 注意元素是从 0 开始的
        int parent = (k - 1) >>> 1;
        // 父节点的值
        Object e = queue[parent];
        // 比较插入的元素与父节点的值
        // 如果比父节点大，则跳出循环
        // 否则交换位置
        if (key.compareTo((E) e) >= 0)
            break;
        // 与父节点交换位置
        queue[k] = e;
        // 现在插入的元素位置移到了父节点的位置
        // 继续与父节点再比较
        k = parent;
    }
    // 最后找到应该插入的位置，放入元素
    queue[k] = key;
}
```

### 4. 扩容

当数组容量小于 64 时，扩容操作对应旧容量翻倍；当数组容量大于等于 64 时，扩容操作对应旧容量加上其一半。

```java
private void grow(int minCapacity) {
    // 旧容量
    int oldCapacity = queue.length;
    // 旧容量小于 64 时，容量翻倍
    // 旧容量大于等于 64，容量只增加旧容量的一半
    int newCapacity = oldCapacity + ((oldCapacity < 64) ?
                                     (oldCapacity + 2) :
                                     (oldCapacity >> 1));
    // 检查是否溢出
    if (newCapacity - MAX_ARRAY_SIZE > 0)
        newCapacity = hugeCapacity(minCapacity);
        
    // 创建出一个新容量大小的新数组并把旧数组元素拷贝过去
    queue = Arrays.copyOf(queue, newCapacity);
}

private static int hugeCapacity(int minCapacity) {
    if (minCapacity < 0) // overflow
        throw new OutOfMemoryError();
    return (minCapacity > MAX_ARRAY_SIZE) ?
        Integer.MAX_VALUE :
        MAX_ARRAY_SIZE;
}
```

### 5. 出队

自上而下堆化。

```java
public E remove() {
    // 调用 poll 弹出队首元素
    E x = poll();
    if (x != null)
        // 有元素就返回弹出的元素
        return x;
    else
        // 没有元素就抛出异常
        throw new NoSuchElementException();
}

@SuppressWarnings("unchecked")
public E poll() {
    // 如果size为0，说明没有元素
    if (size == 0)
        return null;
    // 弹出元素，元素个数减1
    int s = --size;
    modCount++;
    // 队列首元素
    E result = (E) queue[0];
    // 队列末元素
    E x = (E) queue[s];
    // 将队列末元素删除
    queue[s] = null;
    // 如果弹出元素后还有元素
    if (s != 0)
        // 将队列末元素移到队列首
        // 再做自上而下的堆化
        siftDown(0, x);
    // 返回弹出的元素
    return result;
}

private void siftDown(int k, E x) {
    // 根据是否有比较器，选择不同的方法
    if (comparator != null)
        siftDownUsingComparator(k, x);
    else
        siftDownComparable(k, x);
}

@SuppressWarnings("unchecked")
private void siftDownComparable(int k, E x) {
    Comparable<? super E> key = (Comparable<? super E>)x;
    // 只需要比较一半就行了，因为叶子节点占了一半的元素
    int half = size >>> 1;       
    while (k < half) {
        // 寻找子节点的位置，这里加 1 是因为元素从 0 号位置开始
        int child = (k << 1) + 1; 
        // 左子节点的值
        Object c = queue[child];
        // 右子节点的位置
        int right = child + 1;
        if (right < size &&
            ((Comparable<? super E>) c).compareTo((E) queue[right]) > 0)
            // 左右节点取其小者
            c = queue[child = right];
        // 如果比子节点都小，则结束
        if (key.compareTo((E) c) <= 0)
            break;
        // 如果比最小的子节点大，则交换位置
        queue[k] = c;
        // 指针移到最小子节点的位置继续往下比较
        k = child;
    }
    // 找到正确的位置，放入元素
    queue[k] = key;
}
```

### 6. 总结

PriorityQueue 默认实现小根堆，且是非线程安全的，注意实现的小根堆下标从 0 开始。
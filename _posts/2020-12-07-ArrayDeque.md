---
layout:     post
title:      "ArrayDeque"
subtitle:   " \"JDK源码\""
date:       2020-12-07 11:00:00
author:     "LiuJ"
header-img: "img/post-bg-2020.jpg"
catalog: true
tags:
	- ArrayDeque
    - JDK源码
---

## ArrayDeque

ArrayDeque 是一种以循环数组实现的双端队列，是非线程安全的。

![](https://raw.githubusercontent.com/Millione/pb/master/img/20201108205741.png)

### 1. 基本属性

用 NavigableMap 存储元素。

```java
// 存储元素的数组
transient Object[] elements;
// 队列头位置
transient int head;
// 队列尾位置
transient int tail;
// 最小初始容量
private static final int MIN_INITIAL_CAPACITY = 8;
```

### 2. 构造方法

```java
// 默认构造方法，初始容量为 16
public ArrayDeque() {
    elements = new Object[16];
}
// 指定元素个数初始化
public ArrayDeque(int numElements) {
    allocateElements(numElements);
}
// 将集合 c 中的元素初始化到数组中
public ArrayDeque(Collection<? extends E> c) {
    allocateElements(c.size());
    addAll(c);
}
// 初始化数组
private void allocateElements(int numElements) {
    elements = new Object[calculateSize(numElements)];
}
// 计算容量，这段代码的逻辑是算出大于 numElements 的最接近的 2 的 n 次方且不小于8
private static int calculateSize(int numElements) {
    int initialCapacity = MIN_INITIAL_CAPACITY;
    // Find the best power of two to hold elements.
    // Tests "<=" because arrays aren't kept full.
    if (numElements >= initialCapacity) {
        initialCapacity = numElements;
        initialCapacity |= (initialCapacity >>>  1);
        initialCapacity |= (initialCapacity >>>  2);
        initialCapacity |= (initialCapacity >>>  4);
        initialCapacity |= (initialCapacity >>>  8);
        initialCapacity |= (initialCapacity >>> 16);
        initialCapacity++;

        if (initialCapacity < 0)   // Too many elements, must back off
            initialCapacity >>>= 1;// Good luck allocating 2 ^ 30 elements
    }
    return initialCapacity;
}
```

### 3. 入队

入队可从队列头或者队列尾进行，通过对容量取模的方法让头尾指针在数组范围内循环。

```java
// 从队列头入队
public void addFirst(E e) {
    // 不允许 null 元素
    if (e == null)
        throw new NullPointerException();
    // 将 head 指针减 1 并与数组长度减 1 取模
    // 这是为了防止数组到头了边界溢出
    // 如果到头了就从尾再向前
    // 相当于循环利用数组
    elements[head = (head - 1) & (elements.length - 1)] = e;
    // 如果头尾挨在一起了，就扩容
    // 扩容规则也很简单，直接两倍
    if (head == tail)
        doubleCapacity();
}
// 从队列尾入队
public void addLast(E e) {
    // 不允许 null 元素
    if (e == null)
        throw new NullPointerException();
    // 在尾指针的位置放入元素
    // 可以看到tail指针指向的是队列最后一个元素的下一个位置
    elements[tail] = e;
    // tail指针加 1，如果到数组尾了就从头开始
    if ( (tail = (tail + 1) & (elements.length - 1)) == head)
        doubleCapacity();
}
```

### 4. 扩容

扩容方式为直接两倍扩容，注意数组元素的拷贝迁移。

```java
private void doubleCapacity() {
    assert head == tail;
    // 头指针的位置
    int p = head;
    // 旧数组长度
    int n = elements.length;
    // 头指针离数组尾的距离
    int r = n - p; // number of elements to the right of p
    // 新长度为旧长度的两倍
    int newCapacity = n << 1;
    // 判断是否溢出
    if (newCapacity < 0)
        throw new IllegalStateException("Sorry, deque too big");
    // 新建新数组
    Object[] a = new Object[newCapacity];
    // 将旧数组 head 之后的元素拷贝到新数组中
    System.arraycopy(elements, p, a, 0, r);
    // 将旧数组下标 0 到 head 之间的元素拷贝到新数组中
    System.arraycopy(elements, 0, a, r, p);
    // 赋值为新数组
    elements = a;
    // head指向 0，tail 指向旧数组长度表示的位置
    head = 0;
    tail = n;
}
```

### 5. 出队

注意尾指针需要先左移再取元素。

```java
// 从队列头出队
public E pollFirst() {
    int h = head;
    @SuppressWarnings("unchecked")
    // 取队列头元素
    E result = (E) elements[h];
    // 如果队列为空，就返回 null
    if (result == null)
        return null;
    // 将队列头置为空
    elements[h] = null;
    // 队列头指针右移一位
    head = (h + 1) & (elements.length - 1);
    // 返回取得的元素
    return result;
}
// 从队列尾出队
public E pollLast() {
    // 尾指针左移一位
    int t = (tail - 1) & (elements.length - 1);
    @SuppressWarnings("unchecked")
    // 取当前尾指针处元素
    E result = (E) elements[t];
    // 如果队列为空返回null
    if (result == null)
        return null;
    // 将当前尾指针处置为空
    elements[t] = null;
    // tail指向新的尾指针处
    tail = t;
    // 返回取得的元素
    return result;
}
```

### 6. 总结

ArrayDeque 是循环数组实现的双端队列，入队出队通过头尾指针实现，每次扩容直接扩一倍，不支持添加 null 元素。
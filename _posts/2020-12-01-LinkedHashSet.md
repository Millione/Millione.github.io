---
layout:     post
title:      "LinkedHashSet"
subtitle:   " \"JDK源码\""
date:       2020-12-01 11:00:00
author:     "LiuJ"
header-img: "img/post-bg-2020.jpg"
catalog: true
tags:
	- LinkedHashSet
    - JDK源码
---

## LinkedHashSet 

LinkedHashSet 底层使用 LinkedHashMap 来保存所有元素，继承自 HashSet，通过构造方法传递一个标识参数，在底层构造一个 LinkedHashMap。

![](https://raw.githubusercontent.com/Millione/pb/master/img/20201105154053.png)

### 1. 构造方法

```java
public LinkedHashSet(int initialCapacity, float loadFactor) {
    super(initialCapacity, loadFactor, true);
}

public LinkedHashSet(int initialCapacity) {
    super(initialCapacity, .75f, true);
}

public LinkedHashSet() {
    super(16, .75f, true);
}
public LinkedHashSet(Collection<? extends E> c) {
    super(Math.max(2*c.size(), 11), .75f, true);
    addAll(c);
}
```

### 2. 总结

LinkedHashSet 只提供了四个构造方法，通过继承 HashSet，并在底层使用 LinkedHashMap，简洁的实现了其自身的所有接口。
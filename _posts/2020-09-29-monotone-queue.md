---
layout:     post
title:      "单调队列"
subtitle:   " \"高级数据结构\""
date:       2020-09-29 11:00:00
author:     "LiuJ"
header-img: "img/post-bg-2020.jpg"
catalog: true
tags:
    - 单调队列
    - 数据结构
---

# 单调队列

> "单调" 指的是元素的的 "规律"——递增（或递减）
>
> "队列" 指的是元素只能从队头和队尾进行操作

**用途：**用来求出数组的某个区间范围内的最大值。

## 模板

```java
/**
 * 单调队列: 用来求出在数组的某个区间范围内的最值
 */
void monotoneQueue(int[] arr, int k) {
    int n = arr.length;
    List<Integer> res = new ArrayLise<>();
    Deque<Integer> deque = new LinkedList<>();
    for (int i = 0; i < n; i++) {
        while (!deque.isEmpty() && arr[deque.peekLast()] <= nums[i]) {
            deque.pollLast();
        }
        deque.offerLast(i);
        // k：窗口大小
        if (i - k == deque.peekFirst()) {
            deque.pollFirst();
        }
        // 窗口内最大值
        if (i >= k - 1) {
            res.add(arr[deque.peekFirst()]);
        }
    }
}
```

## 题目

### 239. sliding window maximum

------

**Description:**

You are given an array of integers `nums`, there is a sliding window of size `k` which is moving from the very left of the array to the very right. You can only see the `k` numbers in the window. Each time the sliding window moves right by one position.

Return *the max sliding window*.

**Example 1:**

```
Input: nums = [1,3,-1,-3,5,3,6,7], k = 3
Output: [3,3,5,5,6,7]
Explanation: 
Window position                Max
---------------               -----
[1  3  -1] -3  5  3  6  7       3
 1 [3  -1  -3] 5  3  6  7       3
 1  3 [-1  -3  5] 3  6  7       5
 1  3  -1 [-3  5  3] 6  7       5
 1  3  -1  -3 [5  3  6] 7       6
 1  3  -1  -3  5 [3  6  7]      7
```

**Example 2:**

```
Input: nums = [1], k = 1
Output: [1]
```

**Example 3:**

```
Input: nums = [1,-1], k = 1
Output: [1,-1]
```

[Discussion](https://leetcode.com/problems/sliding-window-maximum/discuss/?currentPage=1&orderBy=most_votes&query=) | [Solution](https://leetcode.com/problems/sliding-window-maximum/solution/)

**Code:**

```java
class Solution {
    public int[] maxSlidingWindow(int[] nums, int k) {
        if(nums == null || nums.length == 0){
            return nums;
        }
        Deque<Integer> deque = new ArrayDeque<>();
        int[] res = new int[nums.length - k + 1];
        for(int i = 0; i < nums.length; i++){
            while(!deque.isEmpty() && nums[deque.peekLast()] < nums[i]){
                deque.pollLast();
            }
            deque.addLast(i);
            if(deque.peekFirst() <= i - k){
                deque.pollFirst();
            }
            if(i >= k - 1){
                res[i - k + 1] = nums[deque.peekFirst()];
            }
        }
        return res;
    }
}
```


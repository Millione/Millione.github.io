---
layout:     post
title:      "剑指offer 刷题全记录"
subtitle:   " \"从零到一\""
date:       2020-07-07 12:00:00
author:     "LiuJ"
header-img: "img/post-bg-algorithm.jpg"
catalog: true
tags:
    - 剑指offer
    - 算法
---

# 剑指offer 刷题全记录

|     类型     |                             题目                             |
| :----------: | :----------------------------------------------------------: |
|     数组     | [03-数组中重复的数字](#03-数组中重复的数字)<br/>[04-二维数组中的查找<br/>](#04-二维数组中的查找)[21-调整数组顺序使奇数位于偶数前面](#21-调整数组顺序使奇数位于偶数前面)<br/>[29-顺时针打印矩阵](#29-顺时针打印矩阵)<br/>[39-数组中出现次数超过一半的数字](#39-数组中出现次数超过一半的数字) |
|    字符串    | [05-替换空格](#05-替换空格)<br/>[20-表示数值的字符串](#20-表示数值的字符串)<br/>[58I-翻转单词顺序](#58I-翻转单词顺序)<br/>[58II-左旋转字符串](#58II-左旋转字符串)<br/>[67-把字符串转换成整数](#67-把字符串转换成整数) |
|     链表     | [06-从尾到头打印链表](#06-从尾到头打印链表)<br/>[18-删除链表的结点](#18-删除链表的结点)<br/>[22-链表中倒数第k个结点](#22-链表中倒数第k个结点)<br/>[24-反转链表](#24-反转链表)<br/>[25-合并两个排序的链表](#25-合并两个排序的链表)<br/>[35-复杂链表的复制](#35-复杂链表的复制)<br/>[36-二叉搜索树与双向链表](#36-二叉搜索树与双向链表)<br/>[37-序列化二叉树<br/>](#37-序列化二叉树)[52-两个链表的第一个公共结点](#52-两个链表的第一个公共结点) |
|      树      | [07-重建二叉树](#07-重建二叉树)<br/>[26-树的子结构](#26-树的子结构)<br/>[27-二叉树的镜像](#27-二叉树的镜像)<br/>[28-对称的二叉树](#28-对称的二叉树)<br/>[32I-从上到下打印二叉树](#32I-从上到下打印二叉树)<br/>[32II-从上到下打印二叉树](#32II-从上到下打印二叉树)<br/>[32III-从上到下打印二叉树](#32III-从上到下打印二叉树)<br/>[33-二叉搜索树的后序遍历序列](#33-二叉搜索树的后序遍历序列)<br/>[34-二叉树中和为某一值的路径](#34-二叉树中和为某一值的路径)<br/>[54-二叉搜索树的第k大结点](#54-二叉搜索树的第k大结点)<br/>[55I-二叉树的深度](#55I-二叉树的深度)<br/>[55II-平衡二叉树](#55II-平衡二叉树)<br/>[68I-二叉搜索树的最近公共祖先](#68I-二叉搜索树的最近公共祖先)<br/>[68II-二叉树的最近公共祖先](#68II-二叉树的最近公共祖先) |
|  栈 & 队列   | [09-用两个栈实现队列](#09-用两个栈实现队列)<br/>[30-包含min函数的栈](#30-包含min函数的栈)<br/>[31-栈的压入、弹出序列](#31-栈的压入、弹出序列)<br/>[59I-滑动窗口的最大值](#59I-滑动窗口的最大值)<br/>[59II-队列的最大值](#59II-队列的最大值) |
|      堆      | [40-最小的k个数](#40-最小的k个数)<br/>[41-数据流中的中位数](#41-数据流中的中位数) |
|    哈希表    | [50-第一个只出现一次的字符](#50-第一个只出现一次的字符)<br/>[61-扑克牌中的顺子](#61-扑克牌中的顺子) |
| 斐波那契数列 | [10I-斐波那契数列](#10I-斐波那契数列)<br/>[10II-青蛙跳台阶问题](#10II-青蛙跳台阶问题) |
|     查找     | [11-旋转数组的最小数字](#11-旋转数组的最小数字)<br/>[53I-在排序数组中查找数字I](#53I-在排序数组中查找数字I)<br/>[53II-0~n-1中缺失的数字](#53II-0~n-1中缺失的数字) |
|    双指针    | [48-最长不含重复字符的子字符串](#48-最长不含重复字符的子字符串)<br/>[57-和为s的两个数字](#57-和为s的两个数字)<br/>[57II-和为s的连续正数序列](#57II-和为s的连续正数序列) |
|     搜索     | [12-矩阵中的路径](#12-矩阵中的路径)<br/>[13-机器人的运动范围](#13-机器人的运动范围) |
|   动态规划   | [14I-剪绳子](#14I-剪绳子)<br/>[14II-剪绳子II](#14II-剪绳子II)<br/>[19-正则表达式匹配](#19-正则表达式匹配)<br/>[42-连续子数组的最大和](#42-连续子数组的最大和)<br/>[46-把数字翻译成字符串](#46-把数字翻译成字符串)<br/>[47-礼物的最大价值](#47-礼物的最大价值)<br/>[49-丑数](#49-丑数)<br/>[60-n个骰子的点数](#60-n个骰子的点数)<br/>[63-股票的最大利润](#63-股票的最大利润) |
|     回溯     | [17-打印从1到最大的n位数](#17-打印从1到最大的n位数)<br/>[38-字符串的排列](#38-字符串的排列) |
|     排序     | [40-最小的k个数](#40-最小的k个数)<br/>[45-把数组排成最小的数](#45-把数组排成最小的数)<br/>[51-数组中的逆序对](#51-数组中的逆序对) |
|    位运算    | [15-二进制中1的个数](#15-二进制中1的个数)<br/>[56I-数组中数字出现的次数](#56I-数组中数字出现的次数)<br/>[56II-数组中数字出现的次数II](#56II-数组中数字出现的次数II)<br/>[65-不用加减乘除做加法](#65-不用加减乘除做加法) |
|     其它     | [16-数值的整数次方](#16-数值的整数次方)<br/>[43-1~n整数中1出现的次数](#43-1~n整数中1出现的次数)<br/>[62-圆圈中最后剩下的数字](#62-圆圈中最后剩下的数字)<br/>[64-求1+2+...+n](#64-求1+2+...+n)<br/>[66-构建乘积数组](#66-构建乘积数组) |

## [03-数组中重复的数字](https://leetcode-cn.com/problems/shu-zu-zhong-zhong-fu-de-shu-zi-lcof/)

### 1. 题意

在一个长度为 n 的数组 nums 里的所有数字都在 0～n-1 的范围内。数组中某些数字是重复的，但不知道有几个数字重复了，也不知道每个数字重复了几次。请找出数组中任意一个重复的数字。

### 2. 思路

#### 2.1 暴力

使用 Set 或者 Map 记录已经出现过的数字。

- 时间复杂度：$O(n)$，最差情况遍历完一遍数组。

- 空间复杂度：$O(n)$。

#### 2.2 原地置换

因为数组里数字范围 0～n-1 正好对应数组索引，在正常排序后数字 i 应该在下标为 i 的位置，所以扫描一遍数组，当 nums[i] 不等于 i 且对应索引值不同时，交换两者对应索引的值。

- 时间复杂度：$O(n)$，均摊。

- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int findRepeatNumber(vector<int>& nums) {
        int n = nums.size();
        for (int i = 0; i < n; i++) {
            if (nums[i] != i && nums[i] == nums[nums[i]]) {
                return nums[i];
            }
            while (nums[i] != i) {
                swap(nums[i], nums[nums[i]]);
            }
        }
        return -1;
    }
};
```

#### java

```java
class Solution {
    public int findRepeatNumber(int[] nums) {
        int n = nums.length;
        for (int i = 0; i < n; i++) {
            if (nums[i] != i && nums[i] == nums[nums[i]]) {
                return nums[i];
            }
            while (nums[i] != i) {
                swap(nums, i, nums[i]);
            }
        }
        return -1;
    }
    private void swap(int[] nums, int i, int j) {
        int tmp = nums[i];
        nums[i] = nums[j];
        nums[j] = tmp;
    }
}
```

#### python

```python
class Solution:
    def findRepeatNumber(self, nums: List[int]) -> int:
        for i in range(0, len(nums)):
            if nums[i] != i and nums[i] == nums[nums[i]]:
                return nums[i]
            while nums[i] != i:
                nums[nums[i]], nums[i] = nums[i], nums[nums[i]]
        return -1
```

## [04-二维数组中的查找](https://leetcode-cn.com/problems/er-wei-shu-zu-zhong-de-cha-zhao-lcof/)

### 1. 题意

在一个 n * m 的二维数组中，每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。

### 2. 思路

从左下或右上开始遍历数组，每与 target 判断一次大小即可排除掉一行或一列。

- 时间复杂度：$O(m+n)$。

- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    bool findNumberIn2DArray(vector<vector<int>>& matrix, int target) {
        if (matrix.size() == 0 || matrix[0].size() == 0) {
            return false;
        }
        int m = matrix.size(), n = matrix[0].size();
        for (int i = m - 1, j = 0; i >= 0 && j < n;) {
            if (matrix[i][j] == target) {
                return true;
            } else if (matrix[i][j] > target) {
                i--;
            } else {
                j++;
            }
        }
        return false;
    }
};
```

#### java

```java
class Solution {
    public boolean findNumberIn2DArray(int[][] matrix, int target) {
        if (matrix.length == 0 || matrix[0].length == 0) {
            return false;
        }
        int m = matrix.length, n = matrix[0].length;
        for (int i = m - 1, j = 0; i >= 0 && j < n;) {
            if (matrix[i][j] == target) {
                return true;
            } else if (matrix[i][j] > target) {
                i--;
            } else {
                j++;
            }
        }
        return false;
    }
}
```

#### python

```python
class Solution:
    def findNumberIn2DArray(self, matrix: List[List[int]], target: int) -> bool:
        if (len(matrix) == 0 or len(matrix[0]) == 0):
            return False
        i, j = len(matrix) - 1, 0
        while i >= 0 and j < len(matrix[0]):
            if matrix[i][j] > target: 
                i -= 1
            elif matrix[i][j] < target: 
                j += 1
            else: 
                return True
        return False
```

## [05-替换空格](https://leetcode-cn.com/problems/ti-huan-kong-ge-lcof/)

### 1. 题意

请实现一个函数，把字符串 `s` 中的每个空格替换成"%20"。

### 2. 思路

#### 2.1 模拟

- 时间复杂度：$O(n)$。

- 空间复杂度：$O(n)$。

#### 2.2 双指针

先遍历一遍数组，扩充字符串长度，最后再倒序遍历即可。

- 时间复杂度：$O(n)$。

- 空间复杂度：$O(1)$，仅适用于 cpp，因 java 和 python 中 String 皆为不可变对象。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    string replaceSpace(string s) {
        int n1 = s.length();
        for (int i = 0; i < n1; i++) {
            if (s[i] == ' ') {
                s += "00";
            }
        }
        int n2 = s.length();
        if (n2 <= n1) {
            return s;
        }
        for (int i = n1 - 1; i >= 0; i--) {
            char c = s[i];
            if (c == ' ') {
                s[--n2] = '0';
                s[--n2] = '2';
                s[--n2] = '%';
            } else {
                s[--n2] = c;
            }
        }
        return s;
    }
};
```

#### java

```java
class Solution {
    public String replaceSpace(String s) {
        StringBuilder sb = new StringBuilder();
        for (char c : s.toCharArray()) {
            if(c == ' ') {
                sb.append("%20");
            } else {
                sb.append(c);
            }
        }
        return sb.toString();
    }
}
```

#### python

```python
class Solution:
    def replaceSpace(self, s: str) -> str:
        res = []
        for c in s:
            if c == ' ':
                res.append("%20")
            else:
                res.append(c)
        return "".join(res)
```

## [06-从尾到头打印链表](https://leetcode-cn.com/problems/cong-wei-dao-tou-da-yin-lian-biao-lcof/)

### 1. 题意

输入一个链表的头节点，从尾到头反过来返回每个节点的值（用数组返回）。

### 2. 思路

可以使用递归栈或人工栈，暂存每一次处理结果，反向输出即可。

- 时间复杂度：$O(n)$。

- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    vector<int> reversePrint(ListNode* head) {
        vector<int> res;
        while (head) {
            res.push_back(head->val);
            head = head->next;
        }
        reverse(res.begin(), res.end());
        return res;
    }
};
```

#### java

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public int[] reversePrint(ListNode head) {
        if (head == null) {
            return new int[0];
        }
        List<Integer> list = new ArrayList<>();
        while (head != null) {
            list.add(head.val);
            head = head.next;
        }
        int n = list.size();
        int[] res = new int[n];
        for (int i = 0; i < n; i++) {
            res[i] = list.get(n - i - 1);
        }
        return res;
    }
}
```

#### python

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def reversePrint(self, head: ListNode) -> List[int]:
        res = []
        while head:
            res.append(head.val)
            head = head.next
        return res[::-1]
```

## [07-重建二叉树](https://leetcode-cn.com/problems/zhong-jian-er-cha-shu-lcof/)

### 1. 题意

输入某二叉树的前序遍历和中序遍历的结果，请重建该二叉树。假设输入的前序遍历和中序遍历的结果中都不含重复的数字。

### 2. 思路

前序遍历：根->左->右。

中序遍历：左->根->右。

在前序遍历中可以确定根的值，接着在中序遍历中寻找其对应所在的位置（可以采取空间换时间的做法），递归的去对左子树、右子树进行同样的操作。

- 时间复杂度：最坏$O(n^2)$，平均$O(nlogn)$，递归共建立 n 个节点，每层递归节点搜索占用$O(n)$。优化后：$O(n)$。

- 空间复杂度：$O(n)$，递归处理。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    TreeNode* buildTree(vector<int>& preorder, vector<int>& inorder) {
        if (preorder.size() == 0) {
            return nullptr;
        }
        map<int, int> mymap;
        for (int i = 0; i < inorder.size(); i++) {
            mymap[inorder[i]] = i;
        }
        return build(preorder, 0, inorder, 0, inorder.size() - 1, mymap);
    }
    TreeNode* build(vector<int>& preorder, int prel, vector<int>& inorder, int inl, int inr, map<int, int>& mymap) {
        if (inl > inr) {
            return nullptr;
        }
        int val = preorder[prel];
        int i = mymap[val];
        TreeNode* node = new TreeNode(val);
        node->left = build(preorder, prel + 1, inorder, inl, i - 1, mymap);
        node->right = build(preorder, prel + 1 + i - inl, inorder, i + 1, inr, mymap);
        return node;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public TreeNode buildTree(int[] preorder, int[] inorder) {
        if (preorder == null || preorder.length == 0) {
            return null;
        }
        return build(preorder, 0, inorder, 0, inorder.length - 1);
    }
    private TreeNode build(int[] preorder, int prel, int[] inorder, int inl, int inr) {
        if (inl > inr) {
            return null;
        }
        int val = preorder[prel];
        int i = inl;
        for (; i <= inr; i++) {
            if (inorder[i] == val) {
                break;
            }
        }
        TreeNode node = new TreeNode(val);
        node.left = build(preorder, prel + 1, inorder, inl, i - 1);
        node.right = build(preorder, prel + 1 + i - inl, inorder, i + 1, inr);
        return node;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def buildTree(self, preorder: List[int], inorder: List[int]) -> TreeNode:
        self.dic, self.po = {}, preorder
        for i in range (len(inorder)):
            self.dic[inorder[i]] = i
        return self.build(0, 0, len(inorder) - 1)
    def build(self, pre_root, in_left, in_right) -> TreeNode:
        if in_left > in_right:
            return
        root = TreeNode(self.po[pre_root])
        i = self.dic[root.val]
        root.left = self.build(pre_root + 1, in_left, i - 1)
        root.right = self.build(pre_root + 1 + i - in_left, i + 1, in_right)
        return root
```

## [09-用两个栈实现队列](https://leetcode-cn.com/problems/yong-liang-ge-zhan-shi-xian-dui-lie-lcof/)

### 1. 题意

用两个栈实现一个队列。队列的声明如下，请实现它的两个函数 appendTail 和 deleteHead ，分别完成在队列尾部插入整数和在队列头部删除整数的功能。(若队列中没有元素，deleteHead 操作返回 -1 )

### 2. 思路

一个栈负责入队，一个栈负责出队。

- 时间复杂度：appendTail 函数为$O(1)$，deleteHead 函数为$O(n)$。

- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class CQueue {
public:

    stack<int> stack1;
    stack<int> stack2;

    CQueue() {

    }
    
    void appendTail(int value) {
        stack1.push(value);
    }
    
    int deleteHead() {
        if (!stack2.empty()) {
            int res = stack2.top();
            stack2.pop();
            return res;
        }
        if (stack1.empty()) {
            return -1;
        }
        while (!stack1.empty()) {
            stack2.push(stack1.top());
            stack1.pop();
        }
        int res = stack2.top();
        stack2.pop();
        return res;
    }
};

/**
 * Your CQueue object will be instantiated and called as such:
 * CQueue* obj = new CQueue();
 * obj->appendTail(value);
 * int param_2 = obj->deleteHead();
 */
```

#### java

```java
class CQueue {

    private Deque<Integer> stack1, stack2;

    public CQueue() {
        stack1 = new ArrayDeque<>();
        stack2 = new ArrayDeque<>();
    }
    
    public void appendTail(int value) {
        stack1.push(value);
    }
    
    public int deleteHead() {
        if (!stack2.isEmpty()) {
            return stack2.pop();
        }
        if (stack1.isEmpty()) {
            return -1;
        }
        while (!stack1.isEmpty()) {
            stack2.push(stack1.pop());
        }
        return stack2.pop();
    }
}

/**
 * Your CQueue object will be instantiated and called as such:
 * CQueue obj = new CQueue();
 * obj.appendTail(value);
 * int param_2 = obj.deleteHead();
 */
```

#### python

```python
class CQueue:

    def __init__(self):
        self.stack1, self.stack2 = [], []

    def appendTail(self, value: int) -> None:
        self.stack1.append(value)

    def deleteHead(self) -> int:
        if self.stack2:
            return self.stack2.pop()
        if not self.stack1:
            return -1
        while self.stack1:
            self.stack2.append(self.stack1.pop())
        return self.stack2.pop()


# Your CQueue object will be instantiated and called as such:
# obj = CQueue()
# obj.appendTail(value)
# param_2 = obj.deleteHead()
```

## [10I-斐波那契数列](https://leetcode-cn.com/problems/fei-bo-na-qi-shu-lie-lcof/)

### 1. 题意

写一个函数，输入 `n` ，求斐波那契（Fibonacci）数列的第 `n` 项。斐波那契数列由 0 和 1 开始，之后的斐波那契数就是由之前的两数相加而得出。答案需要取模 1e9+7（1000000007），如计算初始结果为：1000000008，请返回 1。

### 2. 思路

#### 2.1 递归

按方程暴力递归。

- 时间复杂度：$O(2^n)$。
- 空间复杂度：$O(n)$。

#### 2.2 记忆化递归

在递归的过程中对计算值进行缓存，避免大量不必要的重复计算。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

#### 2.3 动态规划

状态转移方程：$f(n+1)=f(n)+f(n-1)$，滚动数组。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int fib(int n) {
        if (n == 0) {
            return 0;
        }
        int a = 0, b = 1;
        for (int i = 2; i <= n; i++) {
            int c = (a + b) % 1000000007;
            a = b;
            b = c;
        }
        return b;
    }
};
```

#### java

```java
class Solution {
    public int fib(int n) {
        if (n == 0) {
            return 0;
        }
        int a = 0, b = 1;
        for (int i = 2; i <= n; i++) {
            int c = (a + b) % 1000000007;
            a = b;
            b = c;
        }
        return b;
    }
}
```

#### python

```python
class Solution:
    def fib(self, n: int) -> int:
        if n == 0:
            return 0
        a, b = 0, 1
        for i in range(n - 1):
            c = (a + b) % 1000000007
            a, b = b, c
        return b
```

## [10II-青蛙跳台阶问题](https://leetcode-cn.com/problems/qing-wa-tiao-tai-jie-wen-ti-lcof/)

### 1. 题意

一只青蛙一次可以跳上1级台阶，也可以跳上2级台阶。求该青蛙跳上一个 n 级的台阶总共有多少种跳法。答案需要取模 1e9+7（1000000007），如计算初始结果为：1000000008，请返回 1。

### 2. 思路

同10I-斐波那契数列题，注意初始为0时此题方法数为1。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int numWays(int n) {
        int a = 1, b = 1;
        for (int i = 1; i <= n; i++) {
            int c = (a + b) % 1000000007;
            a = b;
            b = c;
        }
        return a;
    }
};
```

#### java

```java
class Solution {
    public int numWays(int n) {
        int a = 1, b = 1;
        for (int i = 1; i <= n; i++) {
            int c = (a + b) % 1000000007;
            a = b;
            b = c;
        }
        return a;
    }
}
```

#### python

```python
class Solution:
    def numWays(self, n: int) -> int:
        a, b = 1, 1
        for i in range(n):
            a, b = b, a + b
        return a % 1000000007
```

## [11-旋转数组的最小数字](https://leetcode-cn.com/problems/xuan-zhuan-shu-zu-de-zui-xiao-shu-zi-lcof/)

### 1. 题意

把一个数组最开始的若干个元素搬到数组的末尾，我们称之为数组的旋转。输入一个递增排序的数组的一个旋转，输出旋转数组的最小元素。例如，数组 [3,4,5,1,2] 为 [1,2,3,4,5] 的一个旋转，该数组的最小值为1。 

### 2. 思路

题目出现排序数组，应该想到二分法。对于旋转过的数组，其有序部分可以以最小元素为分隔点划分为两部分，通过与边界值进行比较从而判断当前元素所处位置，始终保证左边界值位于最小元素左边。二分查找流程如下：

1. 当前值大于左边界值，位于绿色部分，`l = mid + 1`。
2. 当前值等于左边界值，可能位于绿色部分，可能位于黄色部分，`l = l + 1`。
3. 当前值小于左边界值，位于黄色部分，`r = mid`。

![image-20200702104641894](C:/Users/LiuJie/OneDrive/LeetCode/whatever/assets/07-02.png)

- 时间复杂度：$O(logn)$，特例情况下会退化到$O(n)$。

- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int minArray(vector<int>& numbers) {
        int l = 0, r = numbers.size() - 1;
        while (l < r) {
            // 始终保证 l r 横跨最小元素点
            if (numbers[l] < numbers[r]) {
                return numbers[l];
            }
            int mid = l + (r - l) / 2;
            if (numbers[mid] > numbers[l]) {
                l = mid + 1;
            } else if (numbers[mid] == numbers[l]) {
                l++;
            } else {
                r = mid;
            }
        }
        return numbers[l];
    }
};
```

#### java

```java
class Solution {
    public int minArray(int[] numbers) {
        int l = 0, r = numbers.length - 1;
        while (l < r) {
            // 始终保证 l r 横跨最小元素点
            if (numbers[l] < numbers[r]) {
                return numbers[l];
            }
            int mid = l + (r - l) / 2;
            if (numbers[mid] > numbers[l]) {
                l = mid + 1;
            } else if (numbers[mid] == numbers[l]) {
                l++;
            } else {
                r = mid;
            }
        }
        return numbers[l];
    }
}
```

#### python

```python
class Solution:
    def minArray(self, numbers: List[int]) -> int:
        l, r = 0, len(numbers) - 1
        while l < r:
            if numbers[l] < numbers[r]:
                return numbers[l]
            mid = l + (r - l) // 2
            if numbers[mid] > numbers[l]:
                l = mid + 1
            elif numbers[mid] == numbers[l]:
                l += 1
            else:
                r = mid
        return numbers[l]
```

## [12-矩阵中的路径](https://leetcode-cn.com/problems/ju-zhen-zhong-de-lu-jing-lcof/)

### 1. 题意

请设计一个函数，用来判断在一个矩阵中是否存在一条包含某字符串所有字符的路径。路径可以从矩阵中的任意一格开始，每一步可以在矩阵中向左、右、上、下移动一格。如果一条路径经过了矩阵的某一格，那么该路径不能再次进入该格子。

### 2. 思路

经典 dfs 回溯，暴力枚举矩阵中所有字符串的可能性，当条件不满足时进行回溯剪枝。

递归参数：当前元素在矩阵 board 中的行列索引 i 和 j，当前目标字符在 word 中的索引 k。

终止条件：

- 字符串匹配完成，返回 true。

- 行或列索引越界，当前元素与目标字符不同，当前元素已经访问过，返回 false。

递推：

标记当前元素，上下左右四个方向搜索，还原当前元素。

- 时间复杂度：$O(3^kmn)$。
- 空间复杂度：$O(mn)$。

### 3. 代码

#### cpp

```cpp
{% raw %}
class Solution {
public:
    vector<vector<int>> dir = {{-1, 0}, {1, 0}, {0, -1}, {0, 1}};
    int m, n;
    bool exist(vector<vector<char>>& board, string word) {
        m = board.size();
        n = board[0].size();
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                if (dfs(board, i, j, word, 0)) {
                    return true;
                }
            }
        }
        return false;
    }
    bool dfs(vector<vector<char>>& board, int i, int j, string word, int k) {
        if (k == word.size()) {
            return true;
        }
        if (i < 0 || i >= m || j < 0 || j >= n || board[i][j] != word[k]) {
            return false;
        }
        char c = board[i][j];
        board[i][j] = '/';
        for (vector<int> d : dir) {
            if (dfs(board, i + d[0], j + d[1], word, k + 1)) {
                return true;
            }
        }
        board[i][j] = c;
        return false;
    }
    
};
{% endraw %}
```

#### java

```java
{% raw %}
class Solution {
    private int[][] dir = {{-1, 0}, {1, 0}, {0, -1}, {0, 1}};
    private int m, n;
    public boolean exist(char[][] board, String word) {
        m = board.length;
        n = board[0].length;
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                if (dfs(board, i, j, word, 0)) {
                    return true;
                }
            }
        }
        return false;
    }
    private boolean dfs(char[][] board, int i, int j, String word, int k) {
        if (k == word.length()) {
            return true;
        }
        if (i < 0 || i >= m || j < 0 || j >= n || board[i][j] != word.charAt(k)) {
            return false;
        }
        char c = board[i][j];
        board[i][j] = '/';
        for (int[] d : dir) {
            if (dfs(board, i + d[0], j + d[1], word, k + 1)) {
                return true;
            }
        }
        board[i][j] = c;
        return false;
    }
}
{% endraw %}
```

#### python

```python
class Solution:
    def exist(self, board: List[List[str]], word: str) -> bool:
        def dfs(i, j, k):
            if not 0 <= i < len(board) or not 0 <= j < len(board[0]) or board[i][j] != word[k]:
                return False
            if k == len(word) - 1:
                return True
            tmp, board[i][j] = board[i][j], '/'
            res = dfs(i + 1, j, k + 1) or dfs(i - 1, j, k + 1) or dfs(i, j + 1, k + 1) or dfs(i, j - 1, k + 1)
            board[i][j] = tmp
            return res

        for i in range(len(board)):
            for j in range(len(board[0])):
                if dfs(i, j, 0):
                    return True
        return False
```

## [13-机器人的运动范围](https://leetcode-cn.com/problems/ji-qi-ren-de-yun-dong-fan-wei-lcof/)

### 1. 题意

地上有一个m行n列的方格，从坐标 [0,0] 到坐标 [m-1,n-1] 。一个机器人从坐标 [0, 0] 的格子开始移动，它每次可以向左、右、上、下移动一格（不能移动到方格外），也不能进入行坐标和列坐标的数位之和大于k的格子。请问该机器人能够到达多少个格子？

### 2. 思路

同12-矩阵中的路径题一样，都是经典矩阵搜索问题，关键在于递推式、终止条件、返回值。

- 时间复杂度：$O(mn)$。
- 空间复杂度：$O(mn)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    bool visited[105][105];
    int movingCount(int m, int n, int k) {
        return dfs(m, n, k, 0, 0, 0, 0);
    }
    int dfs(int m, int n, int k, int i, int j, int ii, int jj) {
        if (i >= m || j >= n || k < ii + jj || visited[i][j]) {
            return 0;
        }
        visited[i][j] = true;
        return 1 + dfs(m, n, k, i + 1, j, ((i + 1) % 10 != 0 ? ii + 1 : ii - 8), jj) + dfs(m, n, k, i, j + 1, ii, ((j + 1) % 10 != 0 ? jj + 1 : jj - 8));
    }
};
```

#### java

```java
class Solution {
    private int m, n, k;
    private boolean[][] visited;
    public int movingCount(int m, int n, int k) {
        this.m = m;
        this.n = n;
        this.k = k;
        visited = new boolean[m][n];
        return dfs(0, 0, 0, 0);
    }
    private int dfs(int i, int j, int ii, int jj) {
        if (i >= m || j >= n || k < ii + jj || visited[i][j]) {
            return 0;
        }
        visited[i][j] = true;
        return 1 + dfs(i + 1, j, ((i + 1) % 10 != 0 ? ii + 1 : ii - 8), jj) + dfs(i, j + 1, ii, ((j + 1) % 10 != 0 ? jj + 1 : jj - 8));
    }
}
```

#### python

```python
class Solution:
    def movingCount(self, m: int, n: int, k: int) -> int:
        def dfs(i, j, ii, jj):
            if i >= m or j >= n or k < ii + jj or (i, j) in visited:
                return 0
            visited.add((i, j))
            return 1 + dfs(i + 1, j, ii + 1 if (i + 1) % 10 else ii - 8, jj) + dfs(i, j + 1, ii, jj + 1 if (j + 1) % 10 else jj - 8);
        
        visited = set()
        return dfs(0, 0, 0, 0)
```

## [14I-剪绳子](https://leetcode-cn.com/problems/jian-sheng-zi-lcof/)

### 1. 题意

给你一根长度为 n 的绳子，请把绳子剪成整数长度的 m 段（m、n都是整数，n>1并且m>1），每段绳子的长度记为 $k[0],k[1]...k[m-1]$。请问 $k[0]*k[1]*...*k[m-1]$可能的最大乘积是多少？

### 2. 思路

#### 2.1 动态规划

$dp[i]$表示长度为$i$的绳子的最大乘积，一段绳子在$j$处切断，其剩余部分$i-j$可以选择继续切断或不切断，可得转移方程如下：
$$
dp[i]=max(dp[i], max(j*dp[i-j], j*(i-j))),j<i
$$

- 时间复杂度：$O(n^2)$。
- 空间复杂度：$O(n)$。

#### 2.2 动态规划优化

任何大于 3 的数都可以拆分为数字 1，2，3 的和，且对 3 的余数总是 0，1，2。也就是说，对于每一次切分，都只切下 1，2，3 这三种长度，再比较出最大值。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

#### 2.3 贪心

绳子段切分的越多，乘积越大。其中只有绳子长度为 2 和 3 的绳子不应再切分，且 3 优于 2。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
int dp[60];
class Solution {
public:
    int cuttingRope(int n) {
        memset(dp, 0, sizeof(dp));
        dp[2] = 1;
        for (int i = 3; i <= n; i++) {
            for (int j = 1; j < i; j++) {
                dp[i] = max(dp[i], max((i - j) * j, j * dp[i - j]));
            }
        }
        return dp[n];
    }
};
```

#### java

```java
class Solution {
    public int cuttingRope(int n) {
        int[] dp = {0, 1, 1};
        for (int i = 3; i <= n; i++) {
            dp[i % 3] = Math.max(Math.max(dp[(i - 1) % 3], i - 1), 
                        Math.max(2 * Math.max(dp[(i - 2) % 3], i - 2), 3 * Math.max(dp[(i - 3) % 3], i - 3)));
        }
        return dp[n % 3]; 
    }
}
```

#### python

```python
class Solution:
    def cuttingRope(self, n: int) -> int:
        if n <= 3:
            return n - 1
        a, b = n // 3, n % 3
        if b == 0:
            return int(math.pow(3, a))
        if b == 1:
            return int(math.pow(3, a - 1) * 4)
        return int(math.pow(3, a) * 2)
```

## [14II-剪绳子II](https://leetcode-cn.com/problems/jian-sheng-zi-ii-lcof/)

### 1. 题意

给你一根长度为 n 的绳子，请把绳子剪成整数长度的 m 段（m、n都是整数，n>1并且m>1），每段绳子的长度记为 $k[0],k[1]...k[m-1]$。请问 $k[0]*k[1]*...*k[m-1]$可能的最大乘积是多少？

### 2. 思路

同14I-剪绳子题不同的是，此题数据规模为$2\leq n\leq 1000$，会涉及到**大数越界情况下的求余问题**。可以采用快速幂取余的方法，其理论支撑公式如下：
$$
(xy)\%p=[(x\%p)(y\%p)]\%p \\
x^a\%p=[(x^{a-1}\%p)(x)\%p]\%p=[(x^{a-1}\%p)x]\%p
$$


- 时间复杂度：$O(logn)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int cuttingRope(int n) {
        int mod = 1000000007;
        if (n <= 3) {
            return n - 1;
        }
        int a = n / 3;
        int b = n % 3;
        if (b == 0) {
            return (int)(quickPow(3, a, mod) % mod);
        }
        if (b == 1) {
            return (int)(quickPow(3, a - 1, mod) * 4 % mod);
        }
        return (int)(quickPow(3, a, mod) * 2 % mod);
    }
    long quickPow(long a, int n, int mod) {
        long ret = 1;
        while (n > 0) {
            if ((n & 1) != 0) {
                ret = ret * a % mod;
            }
            a = a * a % mod;
            n >>= 1;
        }
        return ret;
    }
};
```

#### java

```java
class Solution {
    public int cuttingRope(int n) {
        int mod = 1000000007;
        if (n <= 3) {
            return n - 1;
        }
        int a = n / 3;
        int b = n % 3;
        if (b == 0) {
            return (int)(quickPow(3, a, mod) % mod);
        }
        if (b == 1) {
            return (int)(quickPow(3, a - 1, mod) * 4 % mod);
        }
        return (int)(quickPow(3, a, mod) * 2 % mod);
    }
    private long quickPow(long a, int n, int mod) {
        long ret = 1;
        while (n > 0) {
            if ((n & 1) != 0) {
                ret = ret * a % mod;
            }
            a = a * a % mod;
            n >>= 1;
        }
        return ret;
    }
}
```

#### python

```python
class Solution:
    def cuttingRope(self, n: int) -> int:
        def quickpow(a, n, mod):
            ret = 1
            while n > 0:
                if n % 2:
                    ret = ret * a % mod
                a = a * a % mod
                n //= 2
            return ret
        
        mod = 1000000007
        if n <= 3:
            return n - 1
        a, b = n // 3, n % 3
        if b == 0:
            return int(quickpow(3, a, mod) % mod)
        if b == 1:
            return int(quickpow(3, a - 1, mod) * 4 % mod)
        return int(quickpow(3, a, mod) * 2 % mod)
```

## [15-二进制中1的个数](https://leetcode-cn.com/problems/er-jin-zhi-zhong-1de-ge-shu-lcof/)

### 1. 题意

请实现一个函数，输入一个整数，输出该数二进制表示中 1 的个数。例如，把 9 表示成二进制是 1001，有 2 位是 1。因此，如果输入 9，则该函数输出 2。

### 2. 思路

#### 2.1 逐位判断

对每一位同 1 进行位与操作，判断该位是否为 1，并统计个数。

- 时间复杂度：$O(logn)$。
- 空间复杂度：$O(1)$。

#### 2.2 n & (n - 1)

每次运算得到最低位的 1，统计个数。

- 时间复杂度：$O(m)$，m 代表二进制数中 1 的个数。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int hammingWeight(uint32_t n) {
        int res = 0;
        while (n != 0) {
            res += n & 1;
            n >>= 1;
        }
        return res;
    }
};
```

#### java

```java
public class Solution {
    // you need to treat n as an unsigned value
    public int hammingWeight(int n) {
        int res = 0;
        while (n != 0) {
            res += n & 1;
            n >>>= 1;
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def hammingWeight(self, n: int) -> int:
        res = 0
        while n:
            res += 1 
            n &= n - 1
        return res
```

## [16-数值的整数次方](https://leetcode-cn.com/problems/shu-zhi-de-zheng-shu-ci-fang-lcof/)

### 1. 题意

实现函数double Power(double base, int exponent)，求base的exponent次方。不得使用库函数，同时不需要考虑大数问题。

### 2. 思路

快速幂操作，对于指数 n，可将其用二进制表示，减少重复计算。
$$
3^{10}=3^{2^3+2^1}=3^{2^3}*3^{2^1} \\
2^0,2^1,2^2,2^3...
$$


- 时间复杂度：$O(logn)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    double myPow(double x, int n) {
        if (x == 0.0) {
            return 0.0;
        }
        double res = 1.0;
        long b = n;
        if (b < 0) {
            x = 1 / x;
            b = -b;
        }
        while (b > 0) {
            if ((b & 1) == 1) {
                res *= x;
            }
            x *= x;
            b >>= 1;
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public double myPow(double x, int n) {
        if (x == 0.0) {
            return 0.0;
        }
        long b = n;
        double res = 1.0;
        if (b < 0) {
            x = 1 / x;
            b = -b;
        }
        while (b > 0) {
            if((b & 1) == 1) {
                res *= x;
            }
            x *= x;
            b >>= 1;
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def myPow(self, x: float, n: int) -> float:
        if x == 0: 
            return 0
        res = 1
        if n < 0: 
            x, n = 1 / x, -n
        while n:
            if n & 1: 
                res *= x
            x *= x
            n >>= 1
        return res
```

## [17-打印从1到最大的n位数](https://leetcode-cn.com/problems/da-yin-cong-1dao-zui-da-de-nwei-shu-lcof/)

### 1. 题意

输入数字 `n`，按顺序打印出从 1 到最大的 n 位十进制数。比如输入 3，则打印出 1、2、3 一直到最大的 3 位数 999。

### 2. 思路

#### 2.1 模拟

题目要求返回 int 型数组，默认最后结果不会有大数越界的情况，直接模拟即可。


- 时间复杂度：$O(10^n)$。
- 空间复杂度：$O(1)$。

#### 2.2 大数

对于更普遍的大数越界情况来说，一般采用全排列字符串的做法，递归生成数字的 String 表示形式。基于分治的思想，先固定高位，向低位递归，当个位被固定时，添加对应数字的字符。

- 时间复杂度：$O(10^n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> printNumbers(int n) {
        vector<int> res;
        for (int i = 1; i < pow(10, n); i++) {
            res.push_back(i);
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int[] printNumbers(int n) {
        int[] res = new int[(int)Math.pow(10, n) - 1];
        for (int i = 0; i < res.length; i++) {
            res[i] = i + 1;
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def printNumbers(self, n: int) -> List[int]:
        def dfs(x):
            if x == n:
                s = ''.join(num[self.start:])
                if s != '0':
                    res.append(int(s))
                if n - self.start == self.nine :
                    self.start -= 1
                return
            for i in range(10):
                if i == 9:
                    self.nine += 1
                num[x] = str(i)
                dfs(x + 1)
            self.nine -= 1
        
        num, res = ['0'] * n, []
        self.nine = 0
        self.start = n - 1
        dfs(0)
        return res
```

## [18-删除链表的结点](https://leetcode-cn.com/problems/shan-chu-lian-biao-de-jie-dian-lcof/)

### 1. 题意

给定单向链表的头指针和一个要删除的节点的值，定义一个函数删除该节点。返回删除后的链表的头节点。

### 2. 思路

当要删除节点为头节点时，直接返回下一节点，否则进行遍历定位要删除的节点，同时记录上一节点。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode* deleteNode(ListNode* head, int val) {
        if (head == nullptr) {
            return nullptr;
        } 
        if (head->val == val) {
            return head->next;
        }
        ListNode* cur = head;
        while (cur->next != nullptr) {
            if (cur->next->val == val) {
                cur->next = cur->next->next;
                break;
            }
            cur = cur->next;
        }
        return head;
    }
};
```

#### java

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public ListNode deleteNode(ListNode head, int val) {
        if (head == null) {
            return null;
        } 
        if (head.val == val) {
            return head.next;
        }
        ListNode cur = head;
        while (cur.next != null) {
            if (cur.next.val == val) {
                cur.next = cur.next.next;
                break;
            }
            cur = cur.next;
        }
        return head;
    }
}
```

#### python

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None
class Solution:
    def deleteNode(self, head: ListNode, val: int) -> ListNode:
        if not head:
            return None
        if head.val == val:
            return head.next
        cur = head
        while cur.next:
            if cur.next.val == val:
                cur.next = cur.next.next
                break
            cur = cur.next
        return head
```

## [19-正则表达式匹配](https://leetcode-cn.com/problems/zheng-ze-biao-da-shi-pi-pei-lcof/)

### 1. 题意

请实现一个函数用来匹配包含'. '和'\*'的正则表达式。模式中的字符'.'表示任意一个字符，而'\*'表示它前面的字符可以出现任意次（含0次）。在本题中，匹配是指字符串的所有字符匹配整个模式。

### 2. 思路

$dp[i][j]$表示字符串 s 前 i 个字符与字符串 p 前 j 个字符是否匹配。

初始化：

1. 空字符串和空正则时为 true。
2. 空串和非空正则时需要判断，当前字符为 * 时，且上一字符匹配为 true 时，当前为 true。

转移：

1. 当前正则字符为 . 时或当前正则字符与字符串字符相同时:
   $$
   dp[i+1][j+1]=dp[i][j]
   $$

2. 当前正则字符为 * 时，若上一正则字符不等于当前字符串字符时且不为 . 时:
   $$
   dp[i+1][j+1]=dp[i+1][j-1]
   $$

3. 否则，分别对应多匹配、单匹配、不匹配情况：

$$
dp[i+1][j+1]=dp[i][j+1]||dp[i+1][j]||dp[i+1][j-1]
$$


- 时间复杂度：$O(mn)$。
- 空间复杂度：$O(mn)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    bool isMatch(string s, string p) {
        int m = s.size(), n = p.size();
        bool dp[m + 1][n + 1];
        for (int i = 0; i <= m; i++) {
            for (int j = 0; j <= n; j++) {
                dp[i][j] = false;
            }
        }
        dp[0][0] = true;
        for (int j = 0; j < n; j++) {
            if (p[j] == '*' && dp[0][j - 1]) {
                dp[0][j + 1] = true;
            }
        }
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                if (p[j] == '.' || s[i] == p[j]) {
                    dp[i + 1][j + 1] = dp[i][j];
                }
                if (p[j] == '*') {
                    if (p[j - 1] != s[i] && p[j - 1] != '.') {
                        dp[i + 1][j + 1] = dp[i + 1][j - 1];
                    } else {
                        dp[i + 1][j + 1] = dp[i][j + 1] || dp[i + 1][j] || dp[i + 1][j - 1];
                    }
                }
            }
        }
        return dp[m][n];
    }
};
```

#### java

```java
class Solution {
    public boolean isMatch(String s, String p) {
        if (s == null || p == null) {
            return false;
        }
        int m = s.length(), n = p.length();
        boolean[][] dp = new boolean[m + 1][n + 1];
        dp[0][0] = true;
        for (int j = 0; j < n; j++) {
            if (p.charAt(j) == '*' && dp[0][j - 1]) {
                dp[0][j + 1] = true;
            }
        }
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                if (p.charAt(j) == '.' || s.charAt(i) == p.charAt(j)) {
                    dp[i + 1][j + 1] = dp[i][j];
                }
                if (p.charAt(j) == '*') {
                    if (p.charAt(j - 1) != s.charAt(i) && p.charAt(j - 1) != '.') {
                        dp[i + 1][j + 1] = dp[i + 1][j - 1];
                    } else {
                        dp[i + 1][j + 1] = dp[i][j + 1] || dp[i + 1][j] || dp[i + 1][j - 1];
                    }
                }
            }
        }
        return dp[m][n];
    }
}
```

#### python

```python
class Solution:
    def isMatch(self, s: str, p: str) -> bool:
        m, n = len(s), len(p)
        dp = [[False] * (n + 1) for i in range(m + 1)]
        dp[0][0] = True
        for j in range(n):
            if p[j] == '*' and dp[0][j - 1]:
                dp[0][j + 1] = True
        for i in range(m):
            for j in range(n):
                if p[j] == '.' or s[i] == p[j]:
                    dp[i + 1][j + 1] = dp[i][j]
                if p[j] == '*':
                    if p[j - 1] != '.' and p[j - 1] != s[i]:
                        dp[i + 1][j + 1] = dp[i + 1][j - 1]
                    else:
                        dp[i + 1][j + 1] = dp[i + 1][j - 1] or dp[i + 1][j] or dp[i][j + 1]
        return dp[m][n] 
```

## [20-表示数值的字符串](https://leetcode-cn.com/problems/biao-shi-shu-zhi-de-zi-fu-chuan-lcof/)

### 1. 题意

请实现一个函数用来判断字符串是否表示数值（包括整数和小数）。例如，字符串"+100"、"5e2"、"-123"、"3.1416"、"0123"都表示数值，但"12e"、"1a3.14"、"1.2.3"、"+-5"、"-1E-16"及"12e+5.4"都不是。

### 2. 思路

可使用有限状态自动机。根据字符类型和合法数值的特点，先定义状态，再画出状态转移图，最后编写代码。

**字符类型：**

空格 []，数字 [0 - 9]，正负号 [+-]，小数点 [.]，幂符号 [e]。

**状态定义：**

1. 开始前的空格
2. 幂符号前的正负号
3. 小数点前的数字
4. 小数点、小数点后的数字
5. 小数点前为空格时，小数点、小数点后的数字
6. 幂符号
7. 幂符号后的正负号
8. 幂符号后的数字
9. 结尾的空格

**结束状态：**

3，4，8，9。

![image-20200706104641894](C:/Users/LiuJie/OneDrive/LeetCode/whatever/assets/07-06.png)

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    bool isNumber(string str) {
        if (str.length() == 0) {
            return false;
        }
        int state = 0, flag = 0;
        while (str[0] == ' ') {
            str.erase(0, 1);
        }
        if (str.length() == 0) {
            return false;
        }
        while (str[str.length() - 1] == ' ') {
            str.erase(str.length() - 1, 1);
        }
        for (int i = 0; i < str.length(); i++) {
            if ('0' <= str[i] && str[i] <= '9') {
                flag = 1;
                if (state <= 2) {
                    state = 2;
                } else {
                    state = (state <= 5) ? 5 : 7;
                }
            } else if ('+' == str[i] || '-' == str[i]) {
                if (state == 0 || state == 3) {
                    state++;
                } else {
                    return false;
                }
            } else if ('.' == str[i]) {
                if (state <= 2) {
                    state = 6;
                } else {
                    return false;
                }
            } else if ('e' == str[i]) {
                if (flag && (state == 2 || state == 6 || state == 7)) {
                    state = 3;
                }else {
                    return false;
                }
            } else {
                return false;
            }
        }
        return (state == 2 || state == 5 || (flag && state == 6) || state == 7);
    }
};
```

#### java

```java
class Solution {
    public boolean isNumber(String s) {
        Map[] states = {
            new HashMap<>() {{ put(' ', 0); put('s', 1); put('d', 2); put('.', 4); }}, 
            new HashMap<>() {{ put('d', 2); put('.', 4); }},                           
            new HashMap<>() {{ put('d', 2); put('.', 3); put('e', 5); put(' ', 8); }}, 
            new HashMap<>() {{ put('d', 3); put('e', 5); put(' ', 8); }},              
            new HashMap<>() {{ put('d', 3); }},                                        
            new HashMap<>() {{ put('s', 6); put('d', 7); }},                           
            new HashMap<>() {{ put('d', 7); }},                                        
            new HashMap<>() {{ put('d', 7); put(' ', 8); }},                           
            new HashMap<>() {{ put(' ', 8); }}                                         
        };
        int p = 0;
        char t = ' ';
        for (char c : s.toCharArray()) {
            if (c >= '0' && c <= '9') {
                t = 'd';
            }
            else if (c == '+' || c == '-') {
                t = 's';
            }
            else if (c == '.' || c == 'e' || c == 'E' || c == ' ') {
                t = c;
            }
            else {
                t = '?';
            }
            if (!states[p].containsKey(t)) {
                return false;
            }
            p = (int)states[p].get(t);
        }
        return p == 2 || p == 3 || p == 7 || p == 8;
    }
}
```

#### python

```python
class Solution:
    def isNumber(self, s: str) -> bool:
        states = [
            {' ': 0, 's': 1, 'd': 2, '.': 4},
            {'d': 2, '.': 4},
            {'d': 2, '.': 3, 'e': 5, ' ': 8},
            { 'd': 3, 'e': 5, ' ': 8 },
            { 'd': 3 },
            { 's': 6, 'd': 7 },          
            { 'd': 7 },
            { 'd': 7, ' ': 8 },   
            { ' ': 8 }
        ]
        p = 0
        for c in s:
            if '0' <= c <= '9':
                t = 'd'
            elif c in "+-":
                t = 's'
            elif c in ".eE ":
                t = c
            else:
                t = '?'
            if t not in states[p]:
                return False
            p = states[p][t]
        return p in (2, 3, 7, 8)
```

## [21-调整数组顺序使奇数位于偶数前面](https://leetcode-cn.com/problems/diao-zheng-shu-zu-shun-xu-shi-qi-shu-wei-yu-ou-shu-qian-mian-lcof/)

### 1. 题意

输入一个整数数组，实现一个函数来调整该数组中数字的顺序，使得所有奇数位于数组的前半部分，所有偶数位于数组的后半部分。

### 2. 思路

双边指针法，一头一尾，遍历数组，当头指针元素为偶数时，交换头尾指针元素值，尾指针向前移动一位。当头指针元素为奇数时，头指针向后移动一位。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> exchange(vector<int>& nums) {
        for (int i = 0, j = nums.size() - 1; i <= j;) {
            if (nums[i] % 2 == 0) {
                swap(nums[i], nums[j]);
                j--;
            } else {
                i++;
            }
        }
        return nums;
    }
};
```

#### java

```java
class Solution {
    public int[] exchange(int[] nums) {
        for (int i = 0, j = nums.length - 1; i <= j;) {
            if (nums[i] % 2 == 0) {
                swap(nums, i, j);
                j--;
            } else {
                i++;
            }
        }
        return nums;
    }
    private void swap(int[] nums, int i, int j) {
        int t = nums[i];
        nums[i] = nums[j];
        nums[j] = t;
    }
}
```

#### python

```python
class Solution:
    def exchange(self, nums: List[int]) -> List[int]:
        i, j = 0, len(nums) - 1
        while i <= j:
            if nums[i] % 2:
                i += 1
            else:
                nums[i], nums[j] = nums[j], nums[i]
                j -= 1
        return nums
```

## [22-链表中倒数第k个结点](https://leetcode-cn.com/problems/lian-biao-zhong-dao-shu-di-kge-jie-dian-lcof/)

### 1. 题意

输入一个链表，输出该链表中倒数第k个节点。为了符合大多数人的习惯，本题从1开始计数，即链表的尾节点是倒数第1个节点。例如，一个链表有6个节点，从头节点开始，它们的值依次是1、2、3、4、5、6。这个链表的倒数第3个节点是值为4的节点。

### 2. 思路

前后双指针法，间隔 2 步，注意考虑越界情况。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode* getKthFromEnd(ListNode* head, int k) {
        ListNode* cur = head;
        ListNode* next = head;
        while (k-- > 0) {
            if (next == nullptr) {
                return nullptr;
            }
            next = next->next;
        }
        while (next != nullptr) {
            cur = cur->next;
            next = next->next;
        }
        return cur;
    }
};
```

#### java

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public ListNode getKthFromEnd(ListNode head, int k) {
        ListNode cur = head, next = head;
        while (k-- > 0) {
            if (next == null) {
                return null;
            }
            next = next.next;
        }
        while (next != null) {
            cur = cur.next;
            next = next.next;
        }
        return cur;
    }
}
```

#### python

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def getKthFromEnd(self, head: ListNode, k: int) -> ListNode:
        cur, next = head, head
        for _ in range(k):
            if not next:
                return
            next = next.next
        while next:
            cur, next = cur.next, next.next
        return cur
```

## [24-反转链表](https://leetcode-cn.com/problems/fan-zhuan-lian-biao-lcof/)

### 1. 题意

定义一个函数，输入一个链表的头节点，反转该链表并输出反转后链表的头节点。

### 2. 思路

#### 2.1 迭代

链表经典操作，凡是涉及到链表的操作，一定先把过程画出来，再写程序。

定义三个指针，pre、cur、next，每次实现一次局部反转，并往前进一步，直到 `cur == null` 结束。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

#### 2.2 递归

注意每次返回值都是同一个节点，即反转链表的头。

![](C:/Users/LiuJie/OneDrive/LeetCode/whatever/assets/07-07.gif)

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        ListNode* pre = nullptr;
        ListNode* cur = head;
        ListNode* next = nullptr;
        while (cur != nullptr) {
            next = cur->next;
            cur->next = pre;
            pre = cur;
            cur = next;
        }
        return pre;
    }
};
```

#### java

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public ListNode reverseList(ListNode head) {
        ListNode pre = null, cur = head, next = null;
        while (cur != null) {
            next = cur.next;
            cur.next = pre;
            pre = cur;
            cur = next;
        }
        return pre;
    }
}
```

#### python

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def reverseList(self, head: ListNode) -> ListNode:
        if not head or not head.next:
            return head
        cur = self.reverseList(head.next)
        head.next.next = head
        head.next = None
        return cur
```

## [25-合并两个排序的链表](https://leetcode-cn.com/problems/he-bing-liang-ge-pai-xu-de-lian-biao-lcof/)

### 1. 题意

输入两个递增排序的链表，合并这两个链表并使新链表中的结点仍然是递增排序的。

### 2. 思路

#### 2.1 迭代

构造一个伪头节点，初始化、循环合并、合并剩余尾部。

- 时间复杂度：$O(m+n)$。
- 空间复杂度：$O(1)$。

#### 2.2 递归

**递推过程：**

比较两个链表当前结点值的大小，把后续递归返回的链表头挂载在当前链表值较小的结点后。

**终止条件：**

当两个链表中有任意一个为空链表时终止。

**返回值：**

两个链表中当前结点值较小的结点。

- 时间复杂度：$O(m+n)$。
- 空间复杂度：$O(m+n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode* mergeTwoLists(ListNode* l1, ListNode* l2) {
        if (l1 == nullptr) {
            return l2;
        } else if (l2 == nullptr) {
            return l1;
        } else if (l1->val < l2->val) {
            l1->next = mergeTwoLists(l1->next, l2);
            return l1;
        } else {
            l2->next = mergeTwoLists(l1, l2->next);
            return l2;
        }
    }
};
```

#### java

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */
class Solution {
    public ListNode mergeTwoLists(ListNode l1, ListNode l2) {
        if (l1 == null) {
            return l2;
        } else if (l2 == null) {
            return l1;
        } else if (l1.val < l2.val) {
            l1.next = mergeTwoLists(l1.next, l2);
            return l1;
        } else {
            l2.next = mergeTwoLists(l1, l2.next);
            return l2;
        }
    }
}
```

#### python

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def mergeTwoLists(self, l1: ListNode, l2: ListNode) -> ListNode:
        cur = dummy = ListNode(0)
        while l1 and l2:
            if l1.val < l2.val:
                cur.next, l1 = l1, l1.next
            else:
                cur.next, l2 = l2, l2.next
            cur = cur.next
        cur.next = l1 if l1 else l2
        return dummy.next
```

## [26-树的子结构](https://leetcode-cn.com/problems/shu-de-zi-jie-gou-lcof/)

### 1. 题意

输入两棵二叉树A和B，判断B是不是A的子结构。(约定空树不是任意一个树的子结构)

B是A的子结构， 即 A中有出现和B相同的结构和节点值。

### 2. 思路

先序遍历树 A 中的每个结点（isSubStructure），判断树 A 中以其为根结点的子树是否包含树 B（subStructure）。


- 时间复杂度：$O(mn)$，m 和 n 分别是树 A 和 树 B 的结点数量。
- 空间复杂度：$O(m)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    bool isSubStructure(TreeNode* A, TreeNode* B) {
        if (A == nullptr || B == nullptr) {
            return false;
        }
        return subStructure(A, B) || isSubStructure(A->left, B) || isSubStructure(A->right, B);
    }
    bool subStructure(TreeNode* A, TreeNode* B) {
        if (B == nullptr) {
            return true;
        } else if (A == nullptr || A->val != B->val) {
            return false;
        } else {
            return subStructure(A->left, B->left) && subStructure(A->right, B->right);
        }
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public boolean isSubStructure(TreeNode A, TreeNode B) {
        if (A == null || B == null) {
            return false;
        }
        return subStructure(A, B) || isSubStructure(A.left, B) || isSubStructure(A.right, B);
    }
    private boolean subStructure(TreeNode A, TreeNode B) {
        if (A == null && B == null) {
            return true;
        } else if (A == null) {
            return false;
        } else if (B == null) {
            return true;
        } else if (A.val != B.val) {
            return false;
        } else {
            return subStructure(A.left, B.left) && subStructure(A.right, B.right);
        }
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def isSubStructure(self, A: TreeNode, B: TreeNode) -> bool:
        def subStructure(A, B):
            if not B:
                return True
            if not A or A.val != B.val:
                return False
            return subStructure(A.left, B.left) and subStructure(A.right, B.right)

        if not A or not B:
            return False
        return subStructure(A, B) or self.isSubStructure(A.left, B) or self.isSubStructure(A.right, B)
```

## [27-二叉树的镜像](https://leetcode-cn.com/problems/er-cha-shu-de-jing-xiang-lcof/)

### 1. 题意

请完成一个函数，输入一个二叉树，该函数输出它的镜像。

### 2. 思路

终止条件：当结点为空时即越过叶结点。

递推过程：开启递归左子结点，并挂载在当前结点的右结点；开启递归右子结点，并挂载在当前结点的左结点。

返回值：返回当前结点。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    TreeNode* mirrorTree(TreeNode* root) {
        if (root == nullptr) {
            return root;
        }
        TreeNode* node = root->right;
        root->right = mirrorTree(root->left);
        root->left = mirrorTree(node);
        return root;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public TreeNode mirrorTree(TreeNode root) {
        if (root == null) {
            return root;
        }
        TreeNode node = root.right;
        root.right = mirrorTree(root.left);
        root.left = mirrorTree(node);
        return root;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def mirrorTree(self, root: TreeNode) -> TreeNode:
        if not root:
            return
        stack = [root]
        while stack:
            node = stack.pop()
            if node.left:
                stack.append(node.left)
            if node.right:
                stack.append(node.right)
            node.left, node.right = node.right, node.left
        return root
```

## [28-对称的二叉树](https://leetcode-cn.com/problems/dui-cheng-de-er-cha-shu-lcof/)

### 1. 题意

请实现一个函数，用来判断一棵二叉树是不是对称的。如果一棵二叉树和它的镜像一样，那么它是对称的。

### 2. 思路

终止条件：同时越过叶结点，任意一个越过叶结点，结点值不一样。

递推过程：递归判断左结点左子树和右结点右子树是否对称，左结点右子树和右结点左子树是否对称。

返回值：两结点是否都对称。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    bool isSymmetric(TreeNode* root) {
        if (root == nullptr) {
            return true;
        }
        return symmetric(root->left, root->right);
        
    }
    bool symmetric(TreeNode* root1, TreeNode* root2) {
        if (root1 == nullptr && root2 == nullptr) {
            return true;
        } else if (root1 == nullptr || root2 == nullptr) {
            return false;
        } else if (root1->val != root2->val) {
            return false;
        } else {
            return symmetric(root1->left, root2->right) && symmetric(root1->right, root2->left);
        }
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public boolean isSymmetric(TreeNode root) {
        if (root == null) {
            return true;
        }
        return symmetric(root.left, root.right);
        
    }
    private boolean symmetric(TreeNode root1, TreeNode root2) {
        if (root1 == null && root2 == null) {
            return true;
        } else if (root1 == null || root2 == null) {
            return false;
        } else if (root1.val != root2.val) {
            return false;
        } else {
            return symmetric(root1.left, root2.right) && symmetric(root1.right, root2.left);
        }
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def isSymmetric(self, root: TreeNode) -> bool:
        def symmetric(root1, root2):
            if not root1 and not root2:
                return True
            elif not root1 or not root2 or root1.val != root2.val:
                return False
            return symmetric(root1.left, root2.right) and symmetric(root1.right, root2.left)
        
        return symmetric(root.left, root.right) if root else True
```

## [29-顺时针打印矩阵](https://leetcode-cn.com/problems/shun-shi-zhen-da-yin-ju-zhen-lcof/)

### 1. 题意

输入一个矩阵，按照从外向里以顺时针的顺序依次打印出每一个数字。

### 2. 思路

直接模拟，从左向右、从上向下、从右向左、从下向上。四个方向循环。


- 时间复杂度：$O(mn)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> spiralOrder(vector<vector<int>>& matrix) {
        if (matrix.size() == 0 || matrix[0].size() == 0) {
            return {};
        }
        int m = matrix.size(), n = matrix[0].size();
        vector<int> res(m * n, 0);

        int j = 0;
        int up = 0, down = m - 1, left = 0, right = n - 1;
        while (true) {
            for (int i = left; i <= right; i++) {
                res[j++] = matrix[up][i];
            }
            up++;
            if (up > down) {
                break;
            }
            for (int i = up; i <= down; i++) {
                res[j++] = matrix[i][right];
            }
            right--;
            if (left > right) {
                break;
            }
            for (int i = right; i >= left; i--) {
                res[j++] = matrix[down][i];
            }
            down--;
            if (up > down) {
                break;
            }
            for (int i = down; i >= up; i--) {
                res[j++] = matrix[i][left];
            }
            left++;
            if (left > right) {
                break;
            }
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int[] spiralOrder(int[][] matrix) {
        if (matrix == null || matrix.length == 0 || matrix[0].length == 0) {
            return new int[]{};
        }
        int m = matrix.length, n = matrix[0].length;
        int[] res = new int[m * n];

        int j = 0;
        int up = 0, down = m - 1, left = 0, right = n - 1;
        while (true) {
            for (int i = left; i <= right; i++) {
                res[j++] = matrix[up][i];
            }
            up++;
            if (up > down) {
                break;
            }
            for (int i = up; i <= down; i++) {
                res[j++] = matrix[i][right];
            }
            right--;
            if (left > right) {
                break;
            }
            for (int i = right; i >= left; i--) {
                res[j++] = matrix[down][i];
            }
            down--;
            if (up > down) {
                break;
            }
            for (int i = down; i >= up; i--) {
                res[j++] = matrix[i][left];
            }
            left++;
            if (left > right) {
                break;
            }
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def spiralOrder(self, matrix: List[List[int]]) -> List[int]:
        if not len(matrix) or not len(matrix[0]):
            return []
        m, n = len(matrix), len(matrix[0])
        res = []
        up, down, left, right = 0, m - 1, 0, n - 1
        while True:
            for i in range (left, right + 1):
                res.append(matrix[up][i])
            up += 1
            if up > down:
                break
            
            for i in range (up, down + 1):
                res.append(matrix[i][right])
            right -= 1
            if left > right:
                break
            
            for i in range (right, left - 1, -1):
                res.append(matrix[down][i])
            down -= 1
            if up > down:
                break
            
            for i in range (down, up - 1, -1):
                res.append(matrix[i][left])
            left += 1
            if left > right:
                break
        return res
```

## [30-包含min函数的栈](https://leetcode-cn.com/problems/bao-han-minhan-shu-de-zhan-lcof/)

### 1. 题意

定义栈的数据结构，请在该类型中实现一个能够得到栈的最小元素的 min 函数在该栈中，调用 min、push 及 pop 的时间复杂度都是 O(1)。

### 2. 思路

每次压入当前值时，判断与栈中当前最小值的大小，若当前值大则直接压入，否则先压入最小值，再压入当前值，并更新最小值为当前值。

每次弹出时，若栈顶元素值与当前最小值相同，则连续弹出两次，并把第二次弹出值作为新的最小值，否则直接弹出一次就行。

- 时间复杂度：$O(1)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class MinStack {
public:

    stack<int> mystack;
    int minVal;
    /** initialize your data structure here. */
    MinStack() {
        minVal = INT_MAX;
    }
    
    void push(int x) {
        if (x <= minVal) {
            mystack.push(minVal);
            minVal = x;
        }
        mystack.push(x);
    }
    
    void pop() {
        if (mystack.empty()) {
            return;
        } else if (mystack.top() == minVal) {
            mystack.pop();
            minVal = mystack.top();
            mystack.pop();
        } else {
            mystack.pop();
        }
    }
    
    int top() {
        return mystack.top();
    }
    
    int min() {
        return minVal;
    }
};

/**
 * Your MinStack object will be instantiated and called as such:
 * MinStack* obj = new MinStack();
 * obj->push(x);
 * obj->pop();
 * int param_3 = obj->top();
 * int param_4 = obj->min();
 */
```

#### java

```java
class MinStack {

    private Deque<Integer> stack;
    private int minVal;

    /** initialize your data structure here. */
    public MinStack() {
        stack = new ArrayDeque<>();
        minVal = Integer.MAX_VALUE;
    }
    
    public void push(int x) {
        if (x <= minVal) {
            stack.push(minVal);
            minVal = x;
        }
        stack.push(x);
    }
    
    public void pop() {
        if (stack.isEmpty()) {
            return;
        } else if (stack.pop() == minVal) {
            minVal = stack.pop();
        }
    }
    
    public int top() {
        return stack.peek();
    }
    
    public int min() {
        return minVal;
    }
}

/**
 * Your MinStack object will be instantiated and called as such:
 * MinStack obj = new MinStack();
 * obj.push(x);
 * obj.pop();
 * int param_3 = obj.top();
 * int param_4 = obj.min();
 */
```

#### python

```python
class MinStack:

    def __init__(self):
        self.stack = [];
        self.min_val = float('inf')


    def push(self, x: int) -> None:
        if x <= self.min_val:
            self.stack.append(self.min_val)
            self.min_val = x
        self.stack.append(x)

    def pop(self) -> None:
        if not self.stack:
            return;
        elif self.stack.pop() == self.min_val:
            self.min_val = self.stack.pop()        

    def top(self) -> int:
        return self.stack[-1]

    def min(self) -> int:
        return self.min_val


# Your MinStack object will be instantiated and called as such:
# obj = MinStack()
# obj.push(x)
# obj.pop()
# param_3 = obj.top()
# param_4 = obj.min()
```

## [31-栈的压入、弹出序列](https://leetcode-cn.com/problems/zhan-de-ya-ru-dan-chu-xu-lie-lcof/)

### 1. 题意

输入两个整数序列，第一个序列表示栈的压入顺序，请判断第二个序列是否为该栈的弹出顺序。假设压入栈的所有数字均不相等。例如，序列 {1,2,3,4,5} 是某栈的压栈序列，序列 {4,5,3,2,1} 是该压栈序列对应的一个弹出序列，但 {4,3,5,1,2} 就不可能是该压栈序列的弹出序列。

### 2. 思路

基于贪心的策略，依次把 pushed 序列中的元素入栈，如果栈顶元素等于 popped 序列中下一个要 pop 的值，则应该立刻 pop 出该值，最后返回栈是否为空。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    bool validateStackSequences(vector<int>& pushed, vector<int>& popped) {
        stack<int> mystack;
        int j = 0;
        for (int i = 0; i < pushed.size(); i++) {
            mystack.push(pushed[i]);
            while (!mystack.empty() && j < popped.size() && mystack.top() == popped[j]) {
                mystack.pop();
                j++;
            }
        }
        return mystack.empty();
    }
};
```

#### java

```java
class Solution {
    public boolean validateStackSequences(int[] pushed, int[] popped) {
        Deque<Integer> stack = new ArrayDeque<>();
        int j = 0;
        for (int i = 0; i < pushed.length; i++) {
            stack.push(pushed[i]);
            while (!stack.isEmpty() && j < popped.length && stack.peek() == popped[j]) {
                stack.pop();
                j++;
            }
        }
        return stack.isEmpty();
    }
}
```

#### python

```python
class Solution:
    def validateStackSequences(self, pushed: List[int], popped: List[int]) -> bool:
        stack = []
        j = 0
        for i in range(len(pushed)):
            stack.append(pushed[i])
            while stack and j < len(popped) and stack[-1] == popped[j]:
                stack.pop()
                j += 1
        return not stack
```

## [32I-从上到下打印二叉树](https://leetcode-cn.com/problems/cong-shang-dao-xia-da-yin-er-cha-shu-lcof/)

### 1. 题意

从上到下打印出二叉树的每个节点，同一层的节点按照从左到右的顺序打印。

### 2. 思路

层序遍历二叉树，借助队列的先入先出特性来实现，并直接结果进行保存。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    vector<int> levelOrder(TreeNode* root) {
        if (root == nullptr) {
            return {};
        }
        vector<int> res;
        queue<TreeNode*> myqueue;
        myqueue.push(root);
        while (!myqueue.empty()) {
            TreeNode* cur = myqueue.front();
            myqueue.pop();
            res.push_back(cur->val);
            if (cur->left != nullptr) {
                myqueue.push(cur->left);
            }
            if (cur->right != nullptr) {
                myqueue.push(cur->right);
            }
        }
        return res;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public int[] levelOrder(TreeNode root) {
        if (root == null) {
            return new int[0];
        }
        List<Integer> list = new ArrayList<>();
        Queue<TreeNode> queue = new LinkedList<>();
        queue.offer(root);
        while (!queue.isEmpty()) {
            TreeNode cur = queue.poll();
            list.add(cur.val);
            if (cur.left != null) {
                queue.offer(cur.left);
            }
            if (cur.right != null) {
                queue.offer(cur.right);
            }
        }
        int[] res = new int[list.size()];
        for (int i = 0; i < list.size(); i++) {
            res[i] = list.get(i);
        }
        return res;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def levelOrder(self, root: TreeNode) -> List[int]:
        if not root:
            return []
        res, queue = [], collections.deque()
        queue.append(root)
        while queue:
            cur = queue.popleft()
            res.append(cur.val)
            if cur.left:
                queue.append(cur.left)
            if cur.right:
                queue.append(cur.right)
        return res
```

## [32II-从上到下打印二叉树](https://leetcode-cn.com/problems/cong-shang-dao-xia-da-yin-er-cha-shu-ii-lcof/)

### 1. 题意

从上到下按层打印二叉树，同一层的节点按从左到右的顺序打印，每一层打印到一行。

### 2. 思路

层序遍历BFS，同样是借助队列实现，不过这次是对每一层的遍历结果先进行暂存，等着一层遍历结束再将暂存结果放入最后结果当中。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    vector<vector<int>> levelOrder(TreeNode* root) {
        if (root == nullptr) {
            return {};
        }
        vector<vector<int>> res;
        queue<TreeNode*> myqueue;
        myqueue.push(root);
        while (!myqueue.empty()) {
            vector<int> tmp;
            int sz = myqueue.size();
            for (int i = 0; i < sz; i++) {
                TreeNode* cur = myqueue.front();
                myqueue.pop();
                tmp.push_back(cur->val);
                if (cur->left != nullptr) {
                    myqueue.push(cur->left);
                }
                if (cur->right != nullptr) {
                    myqueue.push(cur->right);
                }
            }
            res.push_back(tmp);
        }
        return res;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public List<List<Integer>> levelOrder(TreeNode root) {
        List<List<Integer>> res = new ArrayList<>();
        if (root == null) {
            return res;
        }
        Queue<TreeNode> queue = new LinkedList<>();
        queue.offer(root);
        while (!queue.isEmpty()) {
            List<Integer> list = new ArrayList<>();
            int sz = queue.size();
            for (int i = 0; i < sz; i++) {
                TreeNode cur = queue.poll();
                list.add(cur.val);
                if (cur.left != null) {
                    queue.offer(cur.left);
                }
                if (cur.right != null) {
                    queue.offer(cur.right);
                }
            }
            res.add(list);
        }
        return res;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def levelOrder(self, root: TreeNode) -> List[List[int]]:
        if not root:
            return []
        res, queue = [], collections.deque()
        queue.append(root)
        while queue:
            tmp = []
            sz = len(queue)
            for i in range(sz):
                cur = queue.popleft()
                tmp.append(cur.val)
                if cur.left:
                    queue.append(cur.left)
                if cur.right:
                    queue.append(cur.right)
            res.append(tmp)
        return res
```

## [32III-从上到下打印二叉树](https://leetcode-cn.com/problems/cong-shang-dao-xia-da-yin-er-cha-shu-iii-lcof/)

### 1. 题意

请实现一个函数按照之字形顺序打印二叉树，即第一行按照从左到右的顺序打印，第二层按照从右到左的顺序打印，第三行再按照从左到右的顺序打印，其他行以此类推。

### 2. 思路

层序遍历BFS，同 32II 不同的是，需要对奇偶层进行判断，从而进行不同方向的插入。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    vector<vector<int>> levelOrder(TreeNode* root) {
        if (root == nullptr) {
            return {};
        }
        vector<vector<int>> res;
        queue<TreeNode*> myqueue;
        myqueue.push(root);
        while (!myqueue.empty()) {
            vector<int> tmp;
            int sz = myqueue.size();
            for (int i = 0; i < sz; i++) {
                TreeNode* cur = myqueue.front();
                myqueue.pop();
                if (res.size() % 2 == 0) {
                    tmp.push_back(cur->val);
                } else {
                    tmp.insert(tmp.begin(), cur->val);
                }
                
                if (cur->left != nullptr) {
                    myqueue.push(cur->left);
                }
                if (cur->right != nullptr) {
                    myqueue.push(cur->right);
                }
            }
            res.push_back(tmp);
        }
        return res;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public List<List<Integer>> levelOrder(TreeNode root) {
        List<List<Integer>> res = new ArrayList<>();
        if (root == null) {
            return res;
        }
        Queue<TreeNode> queue = new LinkedList<>();
        queue.offer(root);
        while (!queue.isEmpty()) {
            List<Integer> list = new ArrayList<>();
            int sz = queue.size();
            for (int i = 0; i < sz; i++) {
                TreeNode cur = queue.poll();
                if (res.size() % 2 == 0) {
                    list.add(cur.val);
                } else {
                    list.add(0, cur.val);
                }
                if (cur.left != null) {
                    queue.offer(cur.left);
                }
                if (cur.right != null) {
                    queue.offer(cur.right);
                }
            }
            res.add(list);
        }
        return res;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def levelOrder(self, root: TreeNode) -> List[List[int]]:
        if not root:
            return []
        res, queue = [], collections.deque()
        queue.append(root)
        while queue:
            tmp = collections.deque()
            sz = len(queue)
            for i in range(sz):
                cur = queue.popleft()
                if len(res) % 2 == 0:
                    tmp.append(cur.val)
                else:
                    tmp.appendleft(cur.val)
                
                if cur.left:
                    queue.append(cur.left)
                if cur.right:
                    queue.append(cur.right)
            res.append(list(tmp))
        return res
```

## [33-二叉搜索树的后序遍历序列](https://leetcode-cn.com/problems/er-cha-sou-suo-shu-de-hou-xu-bian-li-xu-lie-lcof/)

### 1. 题意

输入一个整数数组，判断该数组是不是某二叉搜索树的后序遍历结果。如果是则返回 `true`，否则返回 `false`。假设输入的数组的任意两个数字都互不相同。

### 2. 思路

借助单调栈来实现。对后序遍历数组进行倒序遍历，访问顺序即调整为：根->右->左。当前结点值大于根节点 root 值时，直接返回false。当前结点值小于栈顶元素时，更新 root 值为栈顶元素值并出栈，直到栈空或大于栈顶元素时。最后入栈当前结点值。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    bool verifyPostorder(vector<int>& postorder) {
        stack<int> mystack;
        int root = INT_MAX;
        for (int i = postorder.size() - 1; i >= 0; i--) {
            if (postorder[i] > root) {
               return false;
            }
            while (!mystack.empty() && mystack.top() > postorder[i]) {
                root = mystack.top();
                mystack.pop();
            }
            mystack.push(postorder[i]);
        }
        return true;
    }
};
```

#### java

```java
class Solution {
    public boolean verifyPostorder(int[] postorder) {
        Deque<Integer> stack = new ArrayDeque<>();
        int root = Integer.MAX_VALUE;
        for (int i = postorder.length - 1; i >= 0; i--) {
            if (postorder[i] > root) {
               return false;
            }
            while (!stack.isEmpty() && stack.peek() > postorder[i]) {
                root = stack.pop();
            }
            stack.push(postorder[i]);
        }
        return true;
    }
}
```

#### python

```python
class Solution:
    def verifyPostorder(self, postorder: List[int]) -> bool:
        stack, root = [], float("+inf")
        for i in range(len(postorder) - 1, -1, -1):
            if postorder[i] > root:
                return False
            while stack and postorder[i] < stack[-1]:
                root = stack.pop()
            stack.append(postorder[i])
        return True
```

## [34-二叉树中和为某一值的路径](https://leetcode-cn.com/problems/er-cha-shu-zhong-he-wei-mou-yi-zhi-de-lu-jing-lcof/)

### 1. 题意

输入一棵二叉树和一个整数，打印出二叉树中节点值的和为输入整数的所有路径。从树的根节点开始往下一直到叶节点所经过的节点形成一条路径。

### 2. 思路

标准先序遍历 dfs 回溯。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    vector<vector<int> > res;
    vector<int> path;

    vector<vector<int>> pathSum(TreeNode* root, int sum) {
        dfs(root, sum);
        return res;
    }
    void dfs(TreeNode* root,int sum) {
        if (root == nullptr) {
            return;
        }
        path.push_back(root->val);
        sum -= root->val;
        if (sum == 0 && root->left == nullptr && root->right == nullptr) {
            res.push_back(path);
        }
        dfs(root->left, sum);
        dfs(root->right, sum);
        path.pop_back();
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    private List<List<Integer>> res;
    private List<Integer> path;
    
    public List<List<Integer>> pathSum(TreeNode root, int sum) {
        res = new ArrayList<>();
        path = new ArrayList<>();
        dfs(root, sum);
        return res;
    }
    private void dfs(TreeNode root, int sum) {
        if (root == null) {
            return;
        }
        path.add(root.val);
        sum -= root.val;
        if (sum == 0 && root.left == null && root.right == null) {
            res.add(new ArrayList(path));
        }
        dfs(root.left, sum);
        dfs(root.right, sum);
        path.remove(path.size() - 1);
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def pathSum(self, root: TreeNode, sum: int) -> List[List[int]]:
        res, path = [], []
        def recur(root, sum):
            if not root:
                return
            path.append(root.val)
            sum -= root.val
            if sum == 0 and not root.left and not root.right:
                res.append(list(path))
            recur(root.left, sum)
            recur(root.right, sum)
            path.pop()

        recur(root, sum)
        return res
```

## [35-复杂链表的复制](https://leetcode-cn.com/problems/fu-za-lian-biao-de-fu-zhi-lcof/)

### 1. 题意

请实现 copyRandomList 函数，复制一个复杂链表。在复杂链表中，每个节点除了有一个 next 指针指向下一个节点，还有一个 random 指针指向链表中的任意节点或者 null。

### 2. 思路

借助哈希表来实现，对每一链表指针进行映射复制。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/*
// Definition for a Node.
class Node {
public:
    int val;
    Node* next;
    Node* random;
    
    Node(int _val) {
        val = _val;
        next = NULL;
        random = NULL;
    }
};
*/
class Solution {
public:
    Node* copyRandomList(Node* head) {
        map<Node*, Node*> mymap;
        Node* cur = head;
        while (cur != nullptr) {
            mymap[cur] = new Node(cur->val);
            cur = cur->next;
        }
        cur = head;
        while (cur != nullptr) {
            mymap[cur]->next = mymap[cur->next];
            mymap[cur]->random = mymap[cur->random];
            cur = cur->next;
        }
        return mymap[head];
    }
};
```

#### java

```java
/*
// Definition for a Node.
class Node {
    int val;
    Node next;
    Node random;

    public Node(int val) {
        this.val = val;
        this.next = null;
        this.random = null;
    }
}
*/
class Solution {
    public Node copyRandomList(Node head) {
        Map<Node, Node> map = new HashMap<>();
        Node cur = head;
        while (cur != null) {
            map.put(cur, new Node(cur.val));
            cur = cur.next;
        }
        cur = head;
        while (cur != null) {
            map.get(cur).next = map.get(cur.next);
            map.get(cur).random = map.get(cur.random);
            cur = cur.next;
        }
        return map.get(head);
    }
}
```

#### python

```python
"""
# Definition for a Node.
class Node:
    def __init__(self, x: int, next: 'Node' = None, random: 'Node' = None):
        self.val = int(x)
        self.next = next
        self.random = random
"""
class Solution:
    def copyRandomList(self, head: 'Node') -> 'Node':
        cur = head
        hash = {None:None}
        while cur:
            hash[cur] = Node(cur.val)
            cur = cur.next
        cur = head
        while cur:
            hash[cur].next = hash[cur.next]
            hash[cur].random = hash[cur.random]
            cur = cur.next
        return hash[head]
```

## [36-二叉搜索树与双向链表](https://leetcode-cn.com/problems/er-cha-sou-suo-shu-yu-shuang-xiang-lian-biao-lcof/)

### 1. 题意

输入一棵二叉搜索树，将该二叉搜索树转换成一个排序的循环双向链表。要求不能创建任何新的节点，只能调整树中节点指针的指向。

### 2. 思路

由题目中排序可知需采用中序遍历二叉搜索树，在中序遍历过程中记录当前结点的上一结点，更改指向方向，得到排序循环双向链表。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    vector<vector<int> > res;
    vector<int> path;

    vector<vector<int>> pathSum(TreeNode* root, int sum) {
        dfs(root, sum);
        return res;
    }
    void dfs(TreeNode* root,int sum) {
        if (root == nullptr) {
            return;
        }
        path.push_back(root->val);
        sum -= root->val;
        if (sum == 0 && root->left == nullptr && root->right == nullptr) {
            res.push_back(path);
        }
        dfs(root->left, sum);
        dfs(root->right, sum);
        path.pop_back();
    }
};
```

#### java

```java
/*
// Definition for a Node.
class Node {
    public int val;
    public Node left;
    public Node right;

    public Node() {}

    public Node(int _val) {
        val = _val;
    }

    public Node(int _val,Node _left,Node _right) {
        val = _val;
        left = _left;
        right = _right;
    }
};
*/
class Solution {
    private Node pre, head;
    public Node treeToDoublyList(Node root) {
        if (root == null) {
            return root;
        }
        dfs(root);
        head.left = pre;
        pre.right = head;
        return head;
    }
    private void dfs(Node root) {
        if (root == null) {
            return;
        }
        dfs(root.left);
        if (pre != null) {
            pre.right = root;
        } else {
            head = root;
        }
        root.left = pre;
        pre = root;
        dfs(root.right);
    }
}
```

#### python

```python
"""
# Definition for a Node.
class Node:
    def __init__(self, val, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
"""
class Solution:
    def treeToDoublyList(self, root: 'Node') -> 'Node':
        def dfs(cur):
            if not cur:
                return
            dfs(cur.left)
            if self.pre:
                self.pre.right, cur.left = cur, self.pre
            else:
                self.head = cur
            self.pre = cur
            dfs(cur.right)
        
        if not root:
            return
        self.pre = None
        dfs(root)
        self.head.left, self.pre.right = self.pre, self.head
        return self.head
```

## [37-序列化二叉树](https://leetcode-cn.com/problems/xu-lie-hua-er-cha-shu-lcof/)

### 1. 题意

请实现两个函数，分别用来序列化和反序列化二叉树。

### 2. 思路

前序遍历 dfs，分隔符表示为`!`，空表示为`#`。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Codec {
public:

    // Encodes a tree to a single string.
    string serialize(TreeNode* root) {
        ostringstream out;
        dfs(root, out);
        return out.str();
    }

    void dfs(TreeNode* root, ostringstream& out) {
        if (root) {
            out << root->val << ' ';
            dfs(root->left, out);
            dfs(root->right, out);
        } else {
            out << "# ";
        }
    }

    // Decodes your encoded data to tree.
    TreeNode* deserialize(string data) {
        istringstream in(data);
        return idfs(in);
    }

    TreeNode* idfs(istringstream& in) {
        string val;
        in >> val;
        if (val == "#") {
            return nullptr;
        }
        TreeNode* root = new TreeNode(stoi(val));
        root->left = idfs(in);
        root->right = idfs(in);
        return root;
    }

};

// Your Codec object will be instantiated and called as such:
// Codec codec;
// codec.deserialize(codec.serialize(root));
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
public class Codec {

    // Encodes a tree to a single string.
    public String serialize(TreeNode root) {
        StringBuilder sb = new StringBuilder();
        dfs(root, sb);
        return sb.toString();
    }

    private void dfs(TreeNode root, StringBuilder sb) {
        if (root == null) {
            sb.append("#!");
        } else {
            sb.append(root.val).append("!");
            dfs(root.left, sb);
            dfs(root.right, sb);
        }
    }

    // Decodes your encoded data to tree.
    public TreeNode deserialize(String data) {
        Deque<String> deque = new ArrayDeque<>();
        deque.addAll(Arrays.asList(data.split("!")));
        return idfs(deque);
    }

    private TreeNode idfs(Deque<String> deque) {
        String s = deque.poll();
        if ("#".equals(s)) {
            return null;
        } else {
            TreeNode root = new TreeNode(Integer.valueOf(s));
            root.left = idfs(deque);
            root.right = idfs(deque);
            return root;
        }
    }
}

// Your Codec object will be instantiated and called as such:
// Codec codec = new Codec();
// codec.deserialize(codec.serialize(root));
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode(object):
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Codec:

    def serialize(self, root):
        def dfs(node):
            if node:
                vals.append(str(node.val))
                dfs(node.left)
                dfs(node.right)
            else:
                vals.append('#')
        
        vals = []
        dfs(root)
        return '!'.join(vals)
        

    def deserialize(self, data):
        def idfs():
            val = next(vals)
            if val == '#':
                return None
            node = TreeNode(int(val))
            node.left = idfs()
            node.right = idfs()
            return node
        
        vals = iter(data.split('!'))
        return idfs()

# Your Codec object will be instantiated and called as such:
# codec = Codec()
# codec.deserialize(codec.serialize(root))
```

## [38-字符串的排列](https://leetcode-cn.com/problems/zi-fu-chuan-de-pai-lie-lcof/)

### 1. 题意

输入一个字符串，打印出该字符串中字符的所有排列。

你可以以任意顺序返回这个字符串数组，但里面不能有重复元素。

### 2. 思路

dfs 回溯，两种做法。第一种类似于全排列，需要排序处理出现重复字符的情形。第二种采用固定位交换的思想，需要 set 去除后续重复字符。

- 时间复杂度：$O(n!)$。
- 空间复杂度：$O(n^2)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<string> res;
    vector<string> permutation(string s) {
        int cursor = 0;
        permutation(s, cursor);
        return res;
    }
    void permutation(string &s, int cursor) {
        if (cursor == s.size() - 1) {
            res.push_back(s);
        } else {
            for (int i = cursor; i < s.size(); i++) {
                if (judge(s, cursor, i)) {
                    continue;
                }
                swap(s[cursor], s[i]);
                permutation(s, cursor + 1);
                swap(s[cursor], s[i]);
            }
        }
    }
    bool judge(string& s, int start, int end) {
        for (int i = start; i < end; ++i) {
            if (s[i] == s[end]) {
                return true;
            }
        }
        return false;
    }

};
```

#### java

```java
class Solution {
    private List<String> list;
    private char[] chars;
    private boolean[] used;

    public String[] permutation(String s) {
        list = new ArrayList<>();
        used = new boolean[s.length()];
        chars = s.toCharArray();
        Arrays.sort(chars);
        dfs(chars, new StringBuilder(), 0);
        return list.toArray(new String[0]);
    }
    private void dfs(char[] chars, StringBuilder sb, int len) {
        if (len == chars.length) {
            list.add(sb.toString());
            return;
        }
        for (int i = 0; i < chars.length; i++) {
            if (used[i] || (i > 0 && chars[i] == chars[i - 1] && !used[i - 1])) {
                continue;
            }
            sb.append(chars[i]);
            used[i] = true;
            dfs(chars, sb, len + 1);
            sb.setLength(sb.length() - 1);
            used[i] = false;
        }
    }
}
```

#### python

```python
class Solution:
    def permutation(self, s: str) -> List[str]:
        c, res = list(s), []
        def dfs(x):
            if x == len(c) - 1:
                res.append(''.join(c))
                return
            dic = set()
            for i in range(x, len(c)):
                if c[i] in dic:
                    continue
                dic.add(c[i])
                c[i], c[x] = c[x], c[i]
                dfs(x + 1)
                c[i], c[x] = c[x], c[i]
        
        dfs(0)
        return res
```

## [39-数组中出现次数超过一半的数字](https://leetcode-cn.com/problems/shu-zu-zhong-chu-xian-ci-shu-chao-guo-yi-ban-de-shu-zi-lcof/)

### 1. 题意

数组中有一个数字出现的次数超过数组长度的一半，请找出这个数字。

你可以假设数组是非空的，并且给定的数组总是存在多数元素。

### 2. 思路

摩尔投票法。核心理念为正负抵消，出现次数超过一半的数字一定会出现。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int majorityElement(vector<int>& nums) {
        int x = 0, votes = 0;
        for (int num : nums) {
            if(votes == 0) {
                x = num;
            }
            votes += num == x ? 1 : -1;
        }
        return x;
    }
};
```

#### java

```java
class Solution {
    public int majorityElement(int[] nums) {
        int n = nums.length;
        int cnt = 1, num = nums[0];
        for (int i = 1; i < n; i++) {
            if (nums[i] == num) {
                cnt++;
            } else {
                cnt--;
            }
            if (cnt == 0) {
                num = nums[i];
                cnt = 1;
            }
        }
        return num;
    }
}
```

#### python

```python
class Solution:
    def majorityElement(self, nums: List[int]) -> int:
        x, votes = 0, 0
        for num in nums:
            if votes == 0:
                x = num
            votes += 1 if x == num else -1
        return x 
```

## [40-最小的k个数](https://leetcode-cn.com/problems/zui-xiao-de-kge-shu-lcof/)

### 1. 题意

输入整数数组 `arr` ，找出其中最小的 `k` 个数。例如，输入4、5、1、6、2、7、3、8这8个数字，则最小的4个数字是1、2、3、4。

### 2. 思路

摘自同学 Jerry 微软面试的感悟：

- 先问清题目，各方面各种问，题目是什么意思，希望你干什么，你的API以后要拿到怎么用，给谁用？
- 确认方法的输入输出，希望收到什么样的参数？如果不是这种参数怎么处理，输出什么样的结果？结果的范围是？
- 和面试官确认边界条件，上限是什么？下限是什么？corner case要充分讨论。
- 写代码时最好不断交流，嘴巴里要说，别就只顾着写。
- 最后要给面试官算法复杂度，注意，这里一定要说清楚是最好、平均、最坏，用词要严谨，这些都是细节。

#### 2.1 快选

通过快排切分排好第 K 小的数。

- 时间复杂度：平均$O(n)$。
- 空间复杂度：$O(1)$。

快选算法的**局限性**：

1. 需要修改原数组。
2. 需要保存所有的数据。

#### 2.2 堆

容量为 k 的大根堆，当超过容量 k 后，每次从堆顶弹出的数都是堆中最大的。

- 时间复杂度：$O(nlogk)$。
- 空间复杂度：$O(k)$。

#### 2.3 二叉搜索树

- 时间复杂度：$O(nlogk)$。
- 空间复杂度：$O(n)$。

#### 2.4 计数排序

针对数据范围有限。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> getLeastNumbers(vector<int>& arr, int k) {
        vector<int> res;
        if (k == 0) {
            return res;
        }
        priority_queue<int> pq;
        for (int num : arr) {
            if (pq.size() < k) {
                pq.push(num);
            } else {
                if (pq.top() <= num){
                    continue;
                } else {
                    pq.pop();
                    pq.push(num);
                }
            }
        }
        while (!pq.empty()) {
            res.push_back(pq.top());
            pq.pop();
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int[] getLeastNumbers(int[] arr, int k) {
        if (k == 0 || arr.length == 0) {
            return new int[0];
        }
        quickSelect(arr, 0, arr.length - 1, k);
        return Arrays.copyOfRange(arr, 0, k);
    }
    private void quickSelect(int[] arr, int l, int r, int k) {
        while (l < r) {
            int mid = l + (r - l) / 2;
            if (arr[l] > arr[r]) {
                swap(arr, l, r);
            }
            if (arr[mid] > arr[r]) {
                swap(arr, mid, r);
            }
            if (arr[mid] > arr[l]) {
                swap(arr, mid, l);
            }
            int pivot = arr[l];
            int i = l, j = r;
            while (i <= j) {
                while (i <= j && arr[i] < pivot) {
                    i++;
                }
                while (i <= j && arr[j] > pivot) {
                    j--;
                }
                if (i <= j) {
                    swap(arr, i, j);
                    i++;
                    j--;
                }
            }
            // 最小的 k 个数排序
            if (i >= k) {
                r = i - 1;
            } else {
                l = i;
            }
        }

    }
    private void swap(int[] arr, int l, int r) {
        int t = arr[l];
        arr[l] = arr[r];
        arr[r] = t;
    }
}
```

#### python

```python
class Solution:
    def getLeastNumbers(self, arr: List[int], k: int) -> List[int]:
        if k == 0:
            return []
        heaplist = HeapList()
        heaplist.buildHeap(arr[:k])
        for i in arr[k:]:
            if i < heaplist.heaplist[1]:
                heaplist.delMax()
                heaplist.insert(i)
        return heaplist.heaplist[1:]

class HeapList():
    """
    大顶堆
    """
    def __init__(self):
        self.heaplist = [0]
        self.size = 0

    def buildHeap(self, alist):
         i = len(alist) // 2
         self.size = len(alist)
         self.heaplist += alist[:]
         while i > 0:
             self.percDown(i)
             i -= 1

    def delMax(self):
        """删除堆顶最大元素"""
        retval = self.heaplist[1]
        self.heaplist[1] = self.heaplist[self.size]
        self.size -= 1
        self.heaplist.pop()
        self.percDown(1)
        return retval

    def insert(self, k):
        self.heaplist.append(k)
        self.size += 1
        self.percUP(self.size)

    def percUP(self, i):
        while i // 2 > 0:
            if self.heaplist[i] > self.heaplist[i // 2]:
                self.heaplist[i], self.heaplist[i // 2] = self.heaplist[i // 2], self.heaplist[i]
            i //= 2

    def percDown(self, i):
        while i * 2 <= self.size:
            mc = self.maxChild(i)
            if self.heaplist[i] < self.heaplist[mc]:
                self.heaplist[i], self.heaplist[mc] = self.heaplist[mc], self.heaplist[i]
            i = mc

    def maxChild(self, i):
        if 2 * i + 1 > self.size:
            return 2 * i
        else:
            if self.heaplist[2 * i] > self.heaplist[2 * i + 1]:
                return 2 * i
            else:
                return 2 * i + 1
```

## [41-数据流中的中位数](https://leetcode-cn.com/problems/shu-ju-liu-zhong-de-zhong-wei-shu-lcof/)

### 1. 题意

如何得到一个数据流中的中位数？如果从数据流中读出奇数个数值，那么中位数就是所有数值排序之后位于中间的数值。如果从数据流中读出偶数个数值，那么中位数就是所有数值排序之后中间两个数的平均值。

### 2. 思路

优先队列。同时使用小顶堆和大顶堆来实现，小顶堆放较大的数据，大顶堆放较小的数据，维持小顶堆和大顶堆的平衡，保证每次中位数都在小顶堆堆顶和大顶堆堆顶中取值计算。

- 时间复杂度：$O(logn)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class MedianFinder {
public:
    priority_queue<int> lo;                              // 大顶堆
    priority_queue<int, vector<int>, greater<int>> hi;   // 小顶堆
    /** initialize your data structure here. */
    MedianFinder() {

    }
    
    void addNum(int num) {
        if (lo.size() != hi.size()) {
            lo.push(num);
            hi.push(lo.top());
            lo.pop();
        } else {
            hi.push(num);
            lo.push(hi.top());
            hi.pop();
        }
    }
    
    double findMedian() {
        return lo.size() == hi.size() ? (lo.top() + hi.top()) / 2.0 : (double)lo.top();
    }
};

/**
 * Your MedianFinder object will be instantiated and called as such:
 * MedianFinder* obj = new MedianFinder();
 * obj->addNum(num);
 * double param_2 = obj->findMedian();
 */
```

#### java

```java
class MedianFinder {

    private Queue<Integer> A, B;
    /** initialize your data structure here. */
    public MedianFinder() {
        A = new PriorityQueue<>();
        B = new PriorityQueue<>((a, b) -> (b - a));
    }
    
    public void addNum(int num) {
        if (A.size() != B.size()) {
            A.offer(num);
            B.offer(A.poll());
        } else {
            B.offer(num);
            A.offer(B.poll());
        }
    }
    
    public double findMedian() {
        return A.size() == B.size() ? (A.peek() + B.peek()) / 2.0 : (double)A.peek();
    }
}

/**
 * Your MedianFinder object will be instantiated and called as such:
 * MedianFinder obj = new MedianFinder();
 * obj.addNum(num);
 * double param_2 = obj.findMedian();
 */
```

#### python

```python
class MedianFinder:
    def __init__(self):
        self.A = [] # 小顶堆，保存较大的一半
        self.B = [] # 大顶堆，保存较小的一半

    def addNum(self, num: int) -> None:
        if len(self.A) != len(self.B):
            heappush(self.B, -heappushpop(self.A, num))
        else:
            heappush(self.A, -heappushpop(self.B, -num))

    def findMedian(self) -> float:
        return self.A[0] if len(self.A) != len(self.B) else (self.A[0] - self.B[0]) / 2.0


# Your MedianFinder object will be instantiated and called as such:
# obj = MedianFinder()
# obj.addNum(num)
# param_2 = obj.findMedian()
```

## [42-连续子数组的最大和](https://leetcode-cn.com/problems/lian-xu-zi-shu-zu-de-zui-da-he-lcof/)

### 1. 题意

输入一个整型数组，数组里有正数也有负数。数组中的一个或连续多个整数组成一个子数组。求所有子数组的和的最大值。要求时间复杂度为O(n)。

### 2. 思路

#### 2.1 暴力

- 时间复杂度：$O(n^2)$。
- 空间复杂度：$O(1)$。

#### 2.2 分治

- 时间复杂度：$O(nlogn)$。
- 空间复杂度：$O(logn)$。

#### 2.3 动态规划

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

#### 2.4 贪心

当叠加和小于 0 时，从下一个数重新开始，同时更新最大和的值。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int ans = INT_MIN;
        int sum = 0;
        for (int num : nums) {
            sum += num;
            ans = max(ans, sum);
            if (sum < 0) {
                sum = 0;
            }
        }
        return ans;
    }
};
```

#### java

```java
class Solution {
    public int maxSubArray(int[] nums) {
        int ans = Integer.MIN_VALUE;
        int sum = 0;
        for (int num : nums) {
            sum += num;
            ans = Math.max(ans, sum);
            if (sum < 0) {
                sum = 0;
            }
        }
        return ans;
    }
}
```

#### python

```python
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        ans, sum = float("-INF"), 0
        for num in nums:
            sum += num
            ans = max(ans, sum)
            if sum < 0:
                sum = 0
        return ans
```

## [43-1~n整数中1出现的次数](https://leetcode-cn.com/problems/1nzheng-shu-zhong-1chu-xian-de-ci-shu-lcof/)

### 1. 题意

输入一个整数 n ，求1～n这n个整数的十进制表示中1出现的次数。例如，输入12，1～12这些整数中包含1 的数字有1、10、11和12，1一共出现了5次。

### 2. 思路

数学规律。按数字位进行划分高低位，对每一位上 1 的个数进行求和即得到最终出现次数。假设高位为 a， 低位为 b，当前按百位划分，若当前位大于等于 2， 当前位 1 的个数为 （a / 10 + 1）* 100；若当前位等于1，则 1 的个数为 （a / 10）* 100 + b + 1；若当前位等于 0，则 1 的个数为（a / 10）* 100。

- 时间复杂度：$O(logn)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int countDigitOne(int n) {
        int ones = 0;
        for (long long m = 1; m <= n; m *= 10) {
            int a = n / m, b = n % m;
            ones += (a + 8) / 10 * m + (a % 10 == 1) * (b + 1); 
        }
        return ones;
    }
};
```

#### java

```java
class Solution {
    public int countDigitOne(int n) {
        int ones = 0;
        for (long m = 1; m <= n; m *= 10) {
            ones += (n / m + 8) / 10 * m + (n / m % 10 == 1 ? n % m + 1 : 0);
        }
        return ones;
    }
}
```

#### python

```python
class Solution:
    def countDigitOne(self, n: int) -> int:
        ones, m = 0, 1
        while m <= n:
            a, b = n // m, n % m
            ones += (a + 8) // 10 * m + (a % 10 == 1) * (b + 1)
            m *= 10
        return ones
```

## [45-把数组排成最小的数](https://leetcode-cn.com/problems/ba-shu-zu-pai-cheng-zui-xiao-de-shu-lcof/)

### 1. 题意

输入一个非负整数数组，把数组里所有数字拼接起来排成一个数，打印能拼接出的所有数字中最小的一个。

### 2. 思路

自定义排序，高位小在前。

- 时间复杂度：$O(nlogn)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    string minNumber(vector<int>& nums) {
        vector<string> strs;
        string res;
        for (int i = 0; i < nums.size(); i ++) {
            strs.push_back(to_string(nums[i]));
        }
        sort(strs.begin(), strs.end(), [](string& s1, string& s2){return s1 + s2 < s2 + s1;});
        for (int i = 0; i < strs.size(); i++) {
           res += strs[i];
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public String minNumber(int[] nums) {
        String[] strs = new String[nums.length];
        for (int i = 0; i < nums.length; i++) {
            strs[i] = String.valueOf(nums[i]);
        }
        Arrays.sort(strs, (a, b) -> ((a + b).compareTo(b + a)));
        StringBuilder sb = new StringBuilder();
        for (String str : strs) {
            sb.append(str);
        }
        return sb.toString();
    }
}
```

#### python

```python
class Solution:
    def minNumber(self, nums: List[int]) -> str:
        def cmp(x, y):
            a, b = x + y, y + x
            if a > b:
                return 1
            elif a < b: 
                return -1
            else:
                return 0
        
        strs = [str(num) for num in nums]
        strs.sort(key = functools.cmp_to_key(cmp))
        return ''.join(strs)
```

## [46-把数字翻译成字符串](https://leetcode-cn.com/problems/ba-shu-zi-fan-yi-cheng-zi-fu-chuan-lcof/)

### 1. 题意

给定一个数字，我们按照如下规则把它翻译为字符串：0 翻译成 “a” ，1 翻译成 “b”，……，11 翻译成 “l”，……，25 翻译成 “z”。一个数字可能有多个翻译。请编程实现一个函数，用来计算一个数字有多少种不同的翻译方法。

### 2. 思路

动态规划，采用滚动数组可将空间复杂度降至O(1)。

$dp[i]$表示数字到第$i$位有多少种不同的翻译方式，转移方程如下：
$$
dp[i]=\left\{
\begin{array}{l}
dp[i-1]+dp[i-2] & s[i-2]==1\quad or\quad s[i-2]==2,s[i-1]<6\\
dp[i-1] & otherwise
\end{array}
\right.
$$


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int translateNum(int num) {
        string s = to_string(num);
        int a = 1;
        int b = 1;
        for (int i = 2; i <= s.length(); i++) {
            int c = b;
            if (s[i - 2] == '1' || (s[i - 2] == '2' && s[i - 1] < '6')) {
                c += a;
            }
            a = b;
            b = c;
        }
        return b;
    }
};
```

#### java

```java
class Solution {
    public int translateNum(int num) {
        String s = String.valueOf(num);
        int n = s.length();
        int a = 1;
        int b = 1;
        for (int i = 2; i <= n; i++) {
            int c = b;
            if (s.charAt(i - 2) == '1' || (s.charAt(i - 2) == '2' && s.charAt(i - 1) < '6')) {
                c += a;
            }
            a = b;
            b = c;
        }
        return b;
    }
}
```

#### python

```python
class Solution:
    def translateNum(self, num: int) -> int:
        s = str(num)
        a, b = 1, 1
        for i in range(2, len(s) + 1):
            c = b
            if s[i - 2] == '1' or (s[i - 2] == '2' and s[i - 1] < '6'):
                c += a
            a = b
            b = c
        return b
```

## [47-礼物的最大价值](https://leetcode-cn.com/problems/li-wu-de-zui-da-jie-zhi-lcof/)

### 1. 题意

在一个 m*n 的棋盘的每一格都放有一个礼物，每个礼物都有一定的价值（价值大于 0）。你可以从棋盘的左上角开始拿格子里的礼物，并每次向右或者向下移动一格、直到到达棋盘的右下角。给定一个棋盘及其上面的礼物的价值，请计算你最多能拿到多少价值的礼物？

### 2. 思路

动态规划。$dp[i][j]$表示到达位置 (i-1, j-1) 时能拿到的最大礼物值，转移方程如下：
$$
dp[i][j]=max(dp[i-1][j],dp[i][j-1])+grid[i-1][j-1]
$$
可采用滚动数组，将空间复杂度降至O(n)。

- 时间复杂度：$O(n^2)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int maxValue(vector<vector<int>>& grid) {
        int m = grid.size(), n = grid[0].size();
        vector<int> dp(n + 1, 0);
        for (int i = 1; i <= m; i++) {
            for (int j = 1; j <= n; j++) {
                dp[j] = max(dp[j], dp[j - 1]) + grid[i - 1][j - 1];
            }
        }
        return dp[n];
    }
};
```

#### java

```java
class Solution {
    public int maxValue(int[][] grid) {
        int m = grid.length, n = grid[0].length;
        int[][] dp = new int[m + 1][n + 1];
        for (int i = 1; i <= m; i++) {
            for (int j = 1; j <= n; j++) {
                dp[i][j] = Math.max(dp[i - 1][j], dp[i][j - 1]) + grid[i - 1][j - 1];
            }
        }
        return dp[m][n];
    }
}
```

#### python

```python
class Solution:
    def maxValue(self, grid: List[List[int]]) -> int:
        dp = [0 for i in range(len(grid[0]) + 1)]
        for i in range(1, len(grid) + 1):
            for j in range(1, len(grid[0]) + 1):
                dp[j] = max(dp[j], dp[j - 1]) + grid[i - 1][j - 1]
        return dp[len(grid[0])]
```

## [48-最长不含重复字符的子字符串](https://leetcode-cn.com/problems/zui-chang-bu-han-zhong-fu-zi-fu-de-zi-zi-fu-chuan-lcof/)

### 1. 题意

请从字符串中找出一个最长的不包含重复字符的子字符串，计算该最长子字符串的长度。

### 2. 思路

双指针滑动窗口。每次遇到重复字符，更新左指针位置，进行最大值更新。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int lengthOfLongestSubstring(string s) {
        map<char, int> mymap;
        int l = -1, res = 0;
        for(int r = 0; r < s.size(); r++) {
            if (mymap.find(s[r]) != mymap.end()) {
                l = max(l, mymap[s[r]]);
            }
            mymap[s[r]] = r;
            res = max(res, r - l);
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        Map<Character, Integer> map = new HashMap<>();
        int l = -1, res = 0;
        for(int r = 0; r < s.length(); r++) {
            if (map.containsKey(s.charAt(r))) {
                l = Math.max(l, map.get(s.charAt(r)));
            }
            map.put(s.charAt(r), r);
            res = Math.max(res, r - l);
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        dic, res, i = {}, 0, -1
        for j in range(len(s)):
            if s[j] in dic:
                i = max(dic[s[j]], i) 
            dic[s[j]] = j
            res = max(res, j - i)
        return res
```

## [49-丑数](https://leetcode-cn.com/problems/chou-shu-lcof/)

### 1. 题意

我们把只包含质因子 2、3 和 5 的数称作丑数（Ugly Number）。求按从小到大的顺序的第 n 个丑数。

### 2. 思路

动态规划，一个丑数乘以2，3，5之后，一定还是一个丑数。说到底，其实是对三个有序数组进行合并，并排除重复解的过程。每一个序列都各自维护一个指针， 然后比较指针指向的元素的值， 将最小的放入最终的合并数组中， 并将相应指针向后移动一个元素。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int nthUglyNumber(int n) {
        int t2 = 0, t3 = 0, t5 = 0;
        vector<int> dp(n, 0);
        dp[0] = 1;
        for (int i = 1; i < n; i++) {
            dp[i] = min(dp[t2] * 2, min(dp[t3] * 3, dp[t5] * 5));
            if (dp[i] == dp[t2] * 2) {
                t2++;
            }
            if (dp[i] == dp[t3] * 3) {
                t3++;
            }
            if (dp[i] == dp[t5] * 5) {
                t5++;
            }
        }
        return dp[n - 1];
    }
};
```

#### java

```java
class Solution {
    public int nthUglyNumber(int n) {
        int t2 = 0, t3 = 0, t5 = 0;
        int[] dp = new int[n];
        dp[0] = 1;
        for (int i = 1; i < n; i++) {
            dp[i] = Math.min(dp[t2] * 2, Math.min(dp[t3] * 3, dp[t5] * 5));
            if (dp[i] == dp[t2] * 2) {
                t2++;
            }
            if (dp[i] == dp[t3] * 3) {
                t3++;
            }
            if (dp[i] == dp[t5] * 5) {
                t5++;
            }
        }
        return dp[n - 1];
    }
}
```

#### python

```python
class Solution:
    def nthUglyNumber(self, n: int) -> int:
        dp, a, b, c = [1] * n, 0, 0, 0
        for i in range(1, n):
            n2, n3, n5 = dp[a] * 2, dp[b] * 3, dp[c] * 5
            dp[i] = min(n2, n3, n5)
            if dp[i] == n2:
                a += 1
            if dp[i] == n3:
                b += 1
            if dp[i] == n5:
                c += 1
        return dp[-1]
```

## [50-第一个只出现一次的字符](https://leetcode-cn.com/problems/di-yi-ge-zhi-chu-xian-yi-ci-de-zi-fu-lcof/)

### 1. 题意

在字符串 s 中找出第一个只出现一次的字符。如果没有，返回一个单空格。 s 只包含小写字母。

### 2. 思路

哈希表或数组映射，双次遍历。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    char firstUniqChar(string s) {
        vector<int> cnt(26, 0);
        for (int i = 0; i < s.size(); i++) {
            cnt[s[i] - 'a']++;
        }
        for (int i = 0; i < s.size(); i++) {
            if (cnt[s[i] - 'a'] == 1) {
                return s[i];
            }
        }
        return ' ';
    }
};
```

#### java

```java
class Solution {
    public char firstUniqChar(String s) {
        Map<Character, Boolean> map = new HashMap<>();
        for (char c : s.toCharArray()) {
            map.put(c, !map.containsKey(c));
        }
        for (char c : s.toCharArray()) {
            if (map.get(c)) {
                return c;
            }
        }
        return ' ';
    }
}
```

#### python

```python
class Solution:
    def firstUniqChar(self, s: str) -> str:
        dic = {}
        for c in s:
            dic[c] = not c in dic
        for c in s:
            if dic[c]:
                return c
        return ' '

```

## [51-数组中的逆序对](https://leetcode-cn.com/problems/shu-zu-zhong-de-ni-xu-dui-lcof/)

### 1. 题意

在数组中的两个数字，如果前面一个数字大于后面的数字，则这两个数字组成一个逆序对。输入一个数组，求出这个数组中的逆序对的总数。

### 2. 思路

在每次归并排序的过程中，对逆序对进行统计，关键在于合并过程，利用数组的部分有序性。

- 时间复杂度：$O(nlogn)$。
- 空间复杂度：$O(nlogn)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int reversePairs(vector<int>& nums) {
        int n = nums.size();
        vector<int> tmp(n);
        return mergeSort(nums, tmp, 0, n - 1);
    }

    int mergeSort(vector<int>& nums, vector<int>& tmp, int l, int r) {
        if (l >= r) {
            return 0;
        }
        int mid = (l + r) / 2;
        int cnt = mergeSort(nums, tmp, l, mid) + mergeSort(nums, tmp, mid + 1, r);
        int i = l, j = mid + 1, pos = l;
        while (i <= mid && j <= r) {
            if (nums[i] <= nums[j]) {
                tmp[pos] = nums[i];
                ++i;
                cnt += (j - (mid + 1));
            }
            else {
                tmp[pos] = nums[j];
                ++j;
            }
            ++pos;
        }
        for (int k = i; k <= mid; k++) {
            tmp[pos++] = nums[k];
            cnt += (j - (mid + 1));
        }
        for (int k = j; k <= r; ++k) {
            tmp[pos++] = nums[k];
        }
        copy(tmp.begin() + l, tmp.begin() + r + 1, nums.begin() + l);
        return cnt;
    }

};
```

#### java

```java
class Solution {
    public int reversePairs(int[] nums) {
        if (nums.length == 0) {
            return 0;
        }
        return mergeSort(nums, 0, nums.length - 1);
    }
    private int mergeSort(int[] nums, int l, int r) {
        if (l >= r) {
            return 0;
        }
        int mid = l + (r - l) / 2;
        int ret = mergeSort(nums, l, mid) + mergeSort(nums, mid + 1, r);
        for (int i = l, j = mid + 1; i <= mid; i++) {
            while (j <= r && nums[i] > nums[j]) {
                j++;
            }
            ret += j - (mid + 1);
        }
        merge(nums, l, mid, r);
        return ret;
    }
    private void merge(int[] nums, int l, int mid, int r) {
        int[] aux = new int[r - l + 1];
        int p1 = l, p2 = mid + 1;
        int k = 0;
        while (p1 <= mid && p2 <= r) {
            aux[k++] = nums[p1] <= nums[p2] ? nums[p1++] : nums[p2++];
        }
        while (p1 <= mid) {
            aux[k++] = nums[p1++];
        }
        while (p2 <= r) {
            aux[k++] = nums[p2++];
        }
        for (int i = 0; i < k; i++) {
            nums[l + i] = aux[i];
        }
    }
}
```

#### python

```python
class Solution:
    def reversePairs(self, nums: List[int]) -> int:
        self.cnt = 0
        def merge(nums, start, mid, end, temp):
            i, j = start, mid + 1
            while i <= mid and j <= end:
                if nums[i] <= nums[j]:
                    temp.append(nums[i])
                    i += 1
                else:
                    self.cnt += mid - i + 1
                    temp.append(nums[j])
                    j += 1
            while i <= mid:
                temp.append(nums[i])
                i += 1
            while j <= end:
                temp.append(nums[j])
                j += 1
            for i in range(len(temp)):
                nums[start + i] = temp[i]
            temp.clear()
                    
        def mergeSort(nums, start, end, temp):
            if start >= end:
                return
            mid = (start + end) >> 1
            mergeSort(nums, start, mid, temp)
            mergeSort(nums, mid + 1, end, temp)
            merge(nums, start, mid,  end, temp)
        
        mergeSort(nums, 0, len(nums) - 1, [])
        return self.cnt

```

## [52-两个链表的第一个公共结点](https://leetcode-cn.com/problems/liang-ge-lian-biao-de-di-yi-ge-gong-gong-jie-dian-lcof/submissions/)

### 1. 题意

输入两个链表，找出它们的第一个公共节点。

### 2. 思路

双指针。把链表看作A-B，B-A，双指针遍历判断判断是否公共节点。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {
        ListNode* curA = headA;
        ListNode* curB = headB;
        while (curA != curB) {
            curA = curA == nullptr ? headB : curA->next;
            curB = curB == nullptr ? headA : curB->next;
        }
        return curA;
    }
};
```

#### java

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
        ListNode curA = headA, curB = headB;
        while (curA != curB) {
            curA = curA == null ? headB : curA.next;
            curB = curB == null ? headA : curB.next;
        }
        return curA;
    }
}
```

#### python

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
        curA, curB = headA, headB
        while curA != curB:
            curA = curA.next if curA else headB
            curB = curB.next if curB else headA
        return curA
```

## [53I-在排序数组中查找数字I](https://leetcode-cn.com/problems/zai-pai-xu-shu-zu-zhong-cha-zhao-shu-zi-lcof/)

### 1. 题意

统计一个数字在排序数组中出现的次数。

### 2. 思路

二分查找数字在排序数组中出现的最左边界与最右边界即可。


- 时间复杂度：$O(logn)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int search(vector<int>& nums, int target) {
        int n = nums.size();
        int l1 = 0, r1 = n - 1;
        while (l1 <= r1) {
            int mid = l1 + (r1 - l1) / 2;
            if (nums[mid] >= target) {
                r1 = mid - 1;
            } else {
                l1 = mid + 1;
            }
        }
        if (l1 > n - 1) {
            return 0;
        }
        int l2 = 0, r2 = n - 1;
        while (l2 <= r2) {
            int mid = l2 + (r2 - l2) / 2;
            if (nums[mid] <= target) {
                l2 = mid + 1;
            } else {
                r2 = mid - 1;
            }
        }
        return r2 - l1 + 1;
    }
};
```

#### java

```java
class Solution {
    public int search(int[] nums, int target) {
        int n = nums.length;
        int l1 = 0, r1 = n - 1;
        while (l1 <= r1) {
            int mid = l1 + (r1 - l1) / 2;
            if (nums[mid] >= target) {
                r1 = mid - 1;
            } else {
                l1 = mid + 1;
            }
        }
        if (l1 > n - 1) {
            return 0;
        }
        int l2 = 0, r2 = n - 1;
        while (l2 <= r2) {
            int mid = l2 + (r2 - l2) / 2;
            if (nums[mid] <= target) {
                l2 = mid + 1;
            } else {
                r2 = mid - 1;
            }
        }
        return r2 - l1 + 1;
    }
}
```

#### python

```python
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        n = len(nums)
        l1, r1 = 0, n - 1
        while l1 <= r1:
            mid = l1 + (r1 - l1) // 2
            if nums[mid] >= target:
                r1 = mid - 1
            else:
                l1 = mid + 1
        if l1 > n - 1:
            return 0
        l2, r2 = 0, n - 1
        while l2 <= r2:
            mid = l2 + (r2 - l2) // 2
            if nums[mid] <= target:
                l2 = mid + 1
            else:
                r2 = mid - 1
        return r2 - l1 + 1
```

## [53II-0~n-1中缺失的数字](https://leetcode-cn.com/problems/que-shi-de-shu-zi-lcof/)

### 1. 题意

一个长度为n-1的递增排序数组中的所有数字都是唯一的，并且每个数字都在范围0～n-1之内。在范围0～n-1内的n个数字中有且只有一个数字不在该数组中，请找出这个数字。

### 2. 思路

二分查找，以自身索引值和数组值为二分标杆，若相等，则此数字在右边；若不相等，则此数字在左边。


- 时间复杂度：$O(logn)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int l = 0, r = nums.size() - 1;
        while (l <= r) {
            int mid = l + (r - l) / 2;
            if (nums[mid] == mid) {
                l = mid + 1;
            } else {
                r = mid - 1;
            }
        }
        return l;
    }
};
```

#### java

```java
class Solution {
    public int missingNumber(int[] nums) {
        int l = 0, r = nums.length - 1;
        while (l <= r) {
            int mid = l + (r - l) / 2;
            if (nums[mid] == mid) {
                l = mid + 1;
            } else {
                r = mid - 1;
            }
        }
        return l;
    }
}
```

#### python

```python
class Solution:
    def missingNumber(self, nums: List[int]) -> int:
        l, r = 0, len(nums) - 1
        while l <= r:
            mid = l + (r - l) // 2
            if nums[mid] == mid:
                l = mid + 1
            else:
                r = mid - 1
        return l
```

## [54-二叉搜索树的第k大结点](https://leetcode-cn.com/problems/er-cha-sou-suo-shu-de-di-kda-jie-dian-lcof/)

### 1. 题意

给定一棵二叉搜索树，请找出其中第k大的节点。

### 2. 思路

中序遍历，按照右—根—左的顺序，并计数即可。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    int res, k;
    int kthLargest(TreeNode* root, int k) {
        res = 0;
        this->k = k;
        dfs(root);
        return res;
    }
    void dfs(TreeNode* root) {
        if (root == nullptr || k == 0) {
            return;
        }
        dfs(root->right);
        if (--k == 0) {
            res = root->val;
        }
        dfs(root->left);
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    private int res, k;
    public int kthLargest(TreeNode root, int k) {
        this.k = k;
        res = 0;
        dfs(root);
        return res;
    }
    private void dfs(TreeNode root) {
        if (root == null || k == 0) {
            return;
        }
        dfs(root.right);
        if (--k == 0) {
            res = root.val;
        }
        dfs(root.left);
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def kthLargest(self, root: TreeNode, k: int) -> int:

        def dfs(root):
            if not root or self.k == 0:
                return
            dfs(root.right)
            self.k -= 1
            if self.k == 0:
                self.res = root.val
            dfs(root.left)

        self.k = k
        dfs(root)
        return self.res
```

## [55I-二叉树的深度](https://leetcode-cn.com/problems/er-cha-shu-de-shen-du-lcof/)

### 1. 题意

输入一棵二叉树的根节点，求该树的深度。从根节点到叶节点依次经过的节点（含根、叶节点）形成树的一条路径，最长路径的长度为树的深度。

### 2. 思路

后序遍历。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    int maxDepth(TreeNode* root) {
        if (root == nullptr) {
            return 0;
        }
        int leftDepth = maxDepth(root->left);
        int rightDepth = maxDepth(root->right);
        return max(leftDepth, rightDepth) + 1;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public int maxDepth(TreeNode root) {
        if (root == null) {
            return 0;
        }
        int leftDepth = maxDepth(root.left);
        int rightDepth = maxDepth(root.right);
        return Math.max(leftDepth, rightDepth) + 1;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def maxDepth(self, root: TreeNode) -> int:
        if not root:
            return 0
        leftDepth = self.maxDepth(root.left)
        rightDepth = self.maxDepth(root.right)
        return max(leftDepth, rightDepth) + 1
```

## [55II-平衡二叉树](https://leetcode-cn.com/problems/ping-heng-er-cha-shu-lcof/)

### 1. 题意

输入一棵二叉树的根节点，判断该树是不是平衡二叉树。如果某二叉树中任意节点的左右子树的深度相差不超过1，那么它就是一棵平衡二叉树。

### 2. 思路

后序遍历，注意剪枝。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    bool isBalanced(TreeNode* root) {
        return dfs(root) != -1;
    }
    int dfs(TreeNode* root) {
        if (root == nullptr) {
            return 0;
        }
        int left = dfs(root->left);
        if (left == -1) {
            return -1;
        }
        int right = dfs(root->right);
        if (right == -1) {
            return -1;
        }
        return abs(left - right) > 1 ? -1 : max(left, right) + 1;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public boolean isBalanced(TreeNode root) {
        return dfs(root) != -1;
    }
    private int dfs(TreeNode root) {
        if (root == null) {
            return 0;
        }
        int left = dfs(root.left);
        if (left == -1) {
            return -1;
        }
        int right = dfs(root.right);
        if (right == -1) {
            return -1;
        }
        return Math.abs(left - right) > 1 ? -1 : Math.max(left, right) + 1;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def isBalanced(self, root: TreeNode) -> bool:

        def recur(root):
            if not root:
                return 0
            left = recur(root.left)
            if left == -1:
                return -1
            right = recur(root.right)
            if right == -1:
                return -1
            return max(left, right) + 1 if abs(left - right) <= 1 else -1

        return recur(root) != -1
```

## [56I-数组中数字出现的次数](https://leetcode-cn.com/problems/shu-zu-zhong-shu-zi-chu-xian-de-ci-shu-lcof/)

### 1. 题意

一个整型数组 `nums` 里除两个数字之外，其他数字都出现了两次。请写程序找出这两个只出现一次的数字。

### 2. 思路

位运算。对整个数组里的值进行异或操作，按最低位为 1 划分数组为两部分，这两部分分别包含一个只出现一次的数字，再分别对这两部分异或即可得到答案。 


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> singleNumbers(vector<int>& nums) {
        vector<int> res(2, 0);
        int sum = 0;
        for (int num : nums) {
            sum ^= num;
        }
        sum &= -sum;
        for (int num : nums) {
            if ((sum & num) != 0) {
                res[0] ^= num;
            } else {
                res[1] ^= num;
            }
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int[] singleNumbers(int[] nums) {
        int[] res = new int[2];
        int sum = 0;
        for (int num : nums) {
            sum ^= num;
        }
        sum &= -sum;
        for (int num : nums) {
            if ((sum & num) != 0) {
                res[0] ^= num;
            } else {
                res[1] ^= num;
            }
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def singleNumbers(self, nums: List[int]) -> List[int]:
        res = [0, 0]
        sum = 0
        for num in nums:
            sum ^= num
        sum &= -sum
        for num in nums:
            if (sum & num) != 0:
                res[0] ^= num
            else:
                res[1] ^= num
        return res
```

## [56II-数组中数字出现的次数II](https://leetcode-cn.com/problems/shu-zu-zhong-shu-zi-chu-xian-de-ci-shu-ii-lcof/)

### 1. 题意

在一个数组 `nums` 中除一个数字只出现一次之外，其他数字都出现了三次。请找出那个只出现一次的数字。

### 2. 思路

#### 2.1 有限状态自动机

![Picture4.png](C:/Users/LiuJie/OneDrive/LeetCode/whatever/assets/07-30.png)


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

#### 2.2 遍历统计

对每一个数按位统计其 1 出现次数，若能整除 3，则表示出现一次的数字在该位为 0，否则为 1。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int singleNumber(vector<int>& nums) {
        int res = 0;
        for (int i = 0; i < 32; i++) {
            int cnt = 0;
            for (int num : nums) {
                cnt += (num >> i) & 1;
            }
            res += (cnt % 3) << i;
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int singleNumber(int[] nums) {
        int res = 0;
        for (int i = 0; i < 32; i++) {
            int cnt = 0;
            for (int num : nums) {
                cnt += (num >> i) & 1;
            }
            res += (cnt % 3) << i;
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        res = 0
        for i in range(32):
            cnt = 0
            for num in nums:
                cnt += (num >> i) & 1
            res += (cnt % 3) << i;
        return res
```

## [57-和为s的两个数字](https://leetcode-cn.com/problems/he-wei-sde-liang-ge-shu-zi-lcof/)

### 1. 题意

输入一个递增排序的数组和一个数字s，在数组中查找两个数，使得它们的和正好是s。如果有多对数字的和等于s，则输出任意一对即可。

### 2. 思路

一前一后双指针法。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        vector<int> res;
        int l = 0, r = nums.size() - 1;
        while (l < r) {
            if (nums[l] + nums[r] < target) {
                l++;
            } else if (nums[l] + nums[r] > target) {
                r--;
            } else {
                res.push_back(nums[l]);
                res.push_back(nums[r]);
                return res;
            }
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int l = 0, r = nums.length - 1;
        while (l < r) {
            if (nums[l] + nums[r] < target) {
                l++;
            } else if (nums[l] + nums[r] > target) {
                r--;
            } else {
                return new int[]{nums[l], nums[r]};
            }
        }
        return new int[0];
    }
}
```

#### python

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        i, j = 0, len(nums) - 1
        while i < j:
            if nums[i] + nums[j] > target:
                j -= 1
            elif nums[i] + nums[j] < target:
                i += 1
            else:
                return nums[i], nums[j]
        return []
```

## [57II-和为s的连续正数序列](https://leetcode-cn.com/problems/he-wei-sde-lian-xu-zheng-shu-xu-lie-lcof/)

### 1. 题意

输入一个正整数 target ，输出所有和为 target 的连续正整数序列（至少含有两个数）。

序列内的数字由小到大排列，不同序列按照首个数字从小到大排列。

### 2. 思路

滑动窗口。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<vector<int>> findContinuousSequence(int target) {
        int l = 1, r = 1, sum = 0;
        vector<vector<int>> res;
        while (l <= target / 2) {
            if (sum < target) {
                sum += r;
                r++;
            } else if (sum > target) {
                sum -= l;
                l++;
            } else {
                vector<int> tmp;
                for (int k = l; k < r; k++) {
                    tmp.push_back(k);
                }
                res.push_back(tmp);
                sum -= l;
                l++;
            }
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int[][] findContinuousSequence(int target) {
        int l = 1, r = 1, sum = 0;
        List<int[]> res = new ArrayList<>();
        while (l <= target / 2) {
            if (sum < target) {
                sum += r;
                r++;
            } else if (sum > target) {
                sum -= l;
                l++;
            } else {
                int[] tmp = new int[r - l];
                for (int k = l; k < r; k++) {
                    tmp[k - l] = k;
                }
                res.add(tmp);
                sum -= l;
                l++;
            }
        }
        return res.toArray(new int[0][]);
    }
}
```

#### python

```python
class Solution:
    def findContinuousSequence(self, target: int) -> List[List[int]]:
        i, j, sum, res = 1, 1, 0, []
        while i <= target // 2:
            if sum < target:
                sum += j
                j += 1
            elif sum > target:
                sum -= i
                i += 1
            else:
                res.append(list(range(i, j)))
                sum -= i
                i += 1
        return res
```

## [58I-翻转单词顺序](https://leetcode-cn.com/problems/fan-zhuan-dan-ci-shun-xu-lcof/)

### 1. 题意

输入一个英文句子，翻转句子中单词的顺序，但单词内字符的顺序不变。为简单起见，标点符号和普通字母一样处理。例如输入字符串"I am a student. "，则输出"student. a am I"。

### 2. 思路

字符串分割翻转。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    string reverseWords(string s) {
        istringstream ss(s);
        string res, str;
        while(ss >> str) {
            res = str + ' ' + res;
        }
        return res.substr(0, res.size() - 1);
    }
};
```

#### java

```java
class Solution {
    public String reverseWords(String s) {
        String[] strs = s.trim().split(" ");
        StringBuilder sb = new StringBuilder();
        for(int i = strs.length - 1; i >= 0; i--) {
            if(strs[i].equals("")) {
                continue;
            }
            sb.append(strs[i] + " "); 
        }
        return sb.toString().trim();
    }
}
```

#### python

```python
class Solution:
    def reverseWords(self, s: str) -> str:
        return ' '.join(s.strip().split()[::-1])
```

## [58II-左旋转字符串](https://leetcode-cn.com/problems/zuo-xuan-zhuan-zi-fu-chuan-lcof/)

### 1. 题意

字符串的左旋转操作是把字符串前面的若干个字符转移到字符串的尾部。请定义一个函数实现字符串左旋转操作的功能。比如，输入字符串"abcdefg"和数字2，该函数将返回左旋转两位得到的结果"cdefgab"。

### 2. 思路

三次原地翻转。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    string reverseLeftWords(string s, int n) {
        int len = s.size();
        if (len <= 1) {
            return s;
        }
        reverse(s, 0, n - 1);
        reverse(s, n, len - 1);
        reverse(s, 0, len - 1);
        return s;
    }

    void reverse(string &s, int i, int j) {
        while (i < j) {
            swap(s[i], s[j]);
            i++;
            j--;
        }
    }

};
```

#### java

```java
class Solution {
    public String reverseLeftWords(String s, int n) {
        StringBuilder res = new StringBuilder();
        for(int i = n; i < n + s.length(); i++) {
            res.append(s.charAt(i % s.length()));
        }
        return res.toString();

    }
}
```

#### python

```python
class Solution:
    def reverseLeftWords(self, s: str, n: int) -> str:
        res = []
        for i in range(n, len(s)):
            res.append(s[i])
        for i in range(n):
            res.append(s[i])
        return ''.join(res)
```

## [59I-滑动窗口的最大值](https://leetcode-cn.com/problems/hua-dong-chuang-kou-de-zui-da-zhi-lcof/)

### 1. 题意

给定一个数组 `nums` 和滑动窗口的大小 `k`，请找出所有滑动窗口里的最大值。

### 2. 思路

单调队列。


- 时间复杂度：$O(n)$。
- 空间复杂度：$O(k)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> maxSlidingWindow(vector<int>& nums, int k) {
        int n = nums.size();
        vector<int> res;
        if (n == 0 || k == 0) {
            return res;
        }
        deque<int> dq;
        for (int i = 0; i < n; i++) {
            while (!dq.empty() && dq.front() < i - k + 1) {
                dq.pop_front();
            }
            while (!dq.empty() && nums[dq.back()] < nums[i]) {
                dq.pop_back();
            }
            dq.push_back(i);
            if (i >= k - 1) {
                res.push_back(nums[dq.front()]);
            }
        }
        return res;
    }
};
```

#### java

```java
class Solution {
    public int[] maxSlidingWindow(int[] nums, int k) {
        int n = nums.length;
        if (n == 0 || k == 0) {
            return new int[0];
        }
        int[] res = new int[n - k + 1];
        int j = 0;
        Deque<Integer> queue = new ArrayDeque<>();
        for (int i = 0; i < n; i++) {
            while (!queue.isEmpty() && queue.peek() < i - k + 1) {
                queue.poll();
            }
            while (!queue.isEmpty() && nums[queue.peekLast()] < nums[i]) {
				queue.pollLast();
			}
			queue.offer(i);
			if (i >= k - 1) {
				res[j++] = nums[queue.peek()];
			}
        }
        return res;
    }
}
```

#### python

```python
class Solution:
    def maxSlidingWindow(self, nums: List[int], k: int) -> List[int]:
        deque = collections.deque()
        res, n = [], len(nums)
        for i in range(n):
            while deque and deque[0] < i - k + 1:
                deque.popleft()
            while deque and nums[deque[-1]] < nums[i]:
                deque.pop()
            deque.append(i)
            if i >= k - 1:
                res.append(nums[deque[0]])
        return res
```

## [59II-队列的最大值](https://leetcode-cn.com/problems/dui-lie-de-zui-da-zhi-lcof/)

### 1. 题意

请定义一个队列并实现函数 max_value 得到队列里的最大值，要求函数max_value、push_back 和 pop_front 的均摊时间复杂度都是O(1)。若队列为空，pop_front 和 max_value 需要返回 -1.

### 2. 思路

双队列实现。

- 时间复杂度：$O(1)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class MaxQueue {
    queue<int> q;
    deque<int> d;
public:
    MaxQueue() {

    }
    
    int max_value() {
        if (d.empty()) {
            return -1;
        }
        return d.front();
    }
    
    void push_back(int value) {
        while (!d.empty() && d.back() < value) {
            d.pop_back();
        }
        d.push_back(value);
        q.push(value);
    }
    
    int pop_front() {
        if (q.empty()) {
            return -1;
        }
        int ans = q.front();
        if (ans == d.front()) {
            d.pop_front();
        }
        q.pop();
        return ans;
    }
};


/**
 * Your MaxQueue object will be instantiated and called as such:
 * MaxQueue* obj = new MaxQueue();
 * int param_1 = obj->max_value();
 * obj->push_back(value);
 * int param_3 = obj->pop_front();
 */
```

#### java

```java
class MaxQueue {

    private Deque<Integer> res, max;

    public MaxQueue() {
        res = new ArrayDeque<>();
        max = new ArrayDeque<>();
    }
    
    public int max_value() {
        if (!max.isEmpty()) {
            return max.peekFirst();
        }
        return -1;
    }
    
    public void push_back(int value) {
        res.offerLast(value);
        while (!max.isEmpty() && max.peekLast() < value) {
            max.pollLast();
        }
        max.offerLast(value);
    }
    
    public int pop_front() {
        int ret = -1;
        if (!res.isEmpty()) {
            ret = res.pollFirst();
            if (ret == max.peekFirst()) {
                max.pollFirst();
            }
        }
        return ret;
    }
}

/**
 * Your MaxQueue object will be instantiated and called as such:
 * MaxQueue obj = new MaxQueue();
 * int param_1 = obj.max_value();
 * obj.push_back(value);
 * int param_3 = obj.pop_front();
 */
```

#### python

```python
import queue
class MaxQueue:

    def __init__(self):
        self.deque = queue.deque()
        self.queue = queue.Queue()

    def max_value(self) -> int:
        return self.deque[0] if self.deque else -1


    def push_back(self, value: int) -> None:
        while self.deque and self.deque[-1] < value:
            self.deque.pop()
        self.deque.append(value)
        self.queue.put(value)

    def pop_front(self) -> int:
        if not self.deque:
            return -1
        ans = self.queue.get()
        if ans == self.deque[0]:
            self.deque.popleft()
        return ans


# Your MaxQueue object will be instantiated and called as such:
# obj = MaxQueue()
# param_1 = obj.max_value()
# obj.push_back(value)
# param_3 = obj.pop_front()
```

## [60-n个骰子的点数](https://leetcode-cn.com/problems/nge-tou-zi-de-dian-shu-lcof/)

### 1. 题意

把n个骰子扔在地上，所有骰子朝上一面的点数之和为s。输入n，打印出s的所有可能的值出现的概率。

你需要用一个浮点数数组返回答案，其中第 i 个元素代表这 n 个骰子所能掷出的点数集合中第 i 小的那个的概率。

### 2. 思路

动态规划。从 n - 1 个骰子点数集合概率推导出 n 个骰子点数集合概率，推导公式如下：
$$
tmp[x+y]=tmp[x+y]+pre[x]*num[y];
$$



- 时间复杂度：$O(n^2)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<double> twoSum(int n) {
        vector<double> pre = {1 / 6.0, 1 / 6.0, 1 / 6.0, 1 / 6.0, 1 / 6.0, 1 / 6.0};
        for (int i = 2; i <= n; i++) {
            vector<double> tmp(5 * i + 1, 0.0);
            for (int j = 0; j < pre.size(); j++) {
                for (int k = 0; k < 6; k++) {
                    tmp[j + k] += pre[j] / 6; 
                }
            }
            pre = tmp;
        }
        return pre;
    }
};
```

#### java

```java
class Solution {
    public double[] twoSum(int n) {
        double[] pre = {1 / 6d, 1 / 6d, 1 / 6d, 1 / 6d, 1 / 6d, 1 / 6d};
        for (int i = 2; i <= n; i++) {
            double[] tmp = new double[5 * i + 1];
            for (int j = 0; j < pre.length; j++) {
                for (int k = 0; k < 6; k++) {
                    tmp[j + k] += pre[j] / 6; 
                }
            }
            pre = tmp;
        }
        return pre;
    }
}
```

#### python

```python
class Solution:
    def twoSum(self, n: int) -> List[float]:
        pre = [1 / 6, 1 / 6, 1 / 6, 1 / 6, 1 / 6, 1 / 6]
        for i in range(2, n + 1):
            tmp = [0 for i in range(5 * i + 1)]
            for j in range(len(pre)):
                for k in range(6):
                    tmp[j + k] += pre[j] / 6
            pre = tmp
        return pre
```

## [61-扑克牌中的顺子](https://leetcode-cn.com/problems/bu-ke-pai-zhong-de-shun-zi-lcof/)

### 1. 题意

从扑克牌中随机抽5张牌，判断是不是一个顺子，即这5张牌是不是连续的。2～10为数字本身，A为1，J为11，Q为12，K为13，而大、小王为 0 ，可以看成任意数字。A 不能视为 14。

### 2. 思路

#### 2.1 Set

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

#### 2.2 排序

对数组排序后，判别最大值与最小值的差值。

- 时间复杂度：$O(nlogn)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    bool isStraight(vector<int>& nums) {
        set<int> myset;
        int mi = 14, mx = 0;
        for (int num : nums) {
            if (num == 0) {
                continue;
            }
            mi = min(mi, num);
            mx = max(mx, num);
            if (myset.count(num) != 0) {
                return false;
            }
            myset.insert(num);
        }
        return mx - mi < 5;
    }
};
```

#### java

```java
class Solution {
    public boolean isStraight(int[] nums) {
        Set<Integer> set = new HashSet<>();
        int min = 14, max = 0;
        for (int num : nums) {
            if (num == 0) {
                continue;
            }
            min = Math.min(min, num);
            max = Math.max(max, num);
            if (set.contains(num)) {
                return false;
            }
            set.add(num);
        }
        return max - min < 5;
    }
}
```

#### python

```python
class Solution:
    def isStraight(self, nums: List[int]) -> bool:
        joker = 0
        nums.sort()
        for i in range(4):
            if nums[i] == 0:
                joker += 1 
            elif nums[i] == nums[i + 1]:
                return False
        return nums[4] - nums[joker] < 5
```

## [62-圆圈中最后剩下的数字](https://leetcode-cn.com/problems/yuan-quan-zhong-zui-hou-sheng-xia-de-shu-zi-lcof/)

### 1. 题意

0,1,,n-1这n个数字排成一个圆圈，从数字0开始，每次从这个圆圈里删除第m个数字。求出这个圆圈里剩下的最后一个数字。

例如，0、1、2、3、4这5个数字组成一个圆圈，从数字0开始每次删除第3个数字，则删除的前4个数字依次是2、0、4、1，因此最后剩下的数字是3。

### 2. 思路

约瑟夫环。只关注最后数字所在数组里的索引值变化即可，正向操作时，每次相当于把循环左移 m 位。由题容易知道最后一次操作后数字索引为 0， 我们逆着推出上一次操作该数字所在的索引位置，先补充出上次操作删除元素，再循环右移 m 位。

![约瑟夫环.png](C:/Users/LiuJie/OneDrive/LeetCode/whatever/assets/08-04.png)

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int lastRemaining(int n, int m) {
        int ans = 0;
        for (int i = 2; i <= n; i++) {
            ans = (ans + m) % i;
        }
        return ans;
    }
};
```

#### java

```java
class Solution {
    public int lastRemaining(int n, int m) {
        int ans = 0;
        for (int i = 2; i <= n; i++) {
            ans = (ans + m) % i;
        }
        return ans;
    }
}
```

#### python

```python
class Solution:
    def lastRemaining(self, n: int, m: int) -> int:
        ans = 0
        for i in range(2, n + 1):
            ans = (ans + m) % i
        return ans
```

## [63-股票的最大利润](https://leetcode-cn.com/problems/gu-piao-de-zui-da-li-run-lcof/submissions/)

### 1. 题意

假设把某股票的价格按照时间先后顺序存储在数组中，请问买卖该股票一次可能获得的最大利润是多少？

### 2. 思路

贪心。每当遇到一个更小的值时更新最小值，再以此去更新后续最大利润。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int mi = INT_MAX;
        int ans = 0;
        for (int i = 0; i < prices.size(); i++) {
            mi = min(mi, prices[i]);
            ans = max(ans, prices[i] - mi);
        }
        return ans;
    }
};
```

#### java

```java
class Solution {
    public int maxProfit(int[] prices) {
        int min = Integer.MAX_VALUE;
        int ans = 0;
        for (int i = 0; i < prices.length; i++) {
            min = Math.min(min, prices[i]);
            ans = Math.max(ans, prices[i] - min);
        }
        return ans;
    }
}
```

#### python

```python
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        mi, ans = float("inf"), 0
        for i in range(len(prices)):
            mi = min(mi, prices[i])
            ans = max(ans, prices[i] - mi)
        return ans
```

## [64-求1+2+...+n](https://leetcode-cn.com/problems/qiu-12n-lcof/)

### 1. 题意

求 `1+2+...+n` ，要求不能使用乘除法、for、while、if、else、switch、case等关键字及条件判断语句（A?B:C）。

### 2. 思路

递归求解，并使用短路操作终止递归。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int sumNums(int n) {
        n && (n += sumNums(n - 1));
        return n;
    }
};
```

#### java

```java
class Solution {
    public int sumNums(int n) {
        boolean flag = n != 0 && ((n += sumNums(n - 1)) != 0);
        return n;
    }
}
```

#### python

```python
class Solution:
    def __init__(self):
        self.res = 0
    def sumNums(self, n: int) -> int:
        n > 1 and self.sumNums(n - 1)
        self.res += n
        return self.res
```

## [65-不用加减乘除做加法](https://leetcode-cn.com/problems/bu-yong-jia-jian-cheng-chu-zuo-jia-fa-lcof/)

### 1. 题意

写一个函数，求两个整数之和，要求在函数体内不得使用 “+”、“-”、“*”、“/” 四则运算符号。

### 2. 思路

位运算。两数相加，不考虑进位的情况下等同于相异或，进位值等同于相与再左移一位。

- 时间复杂度：$O(1)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int add(int a, int b) {
        int x = ~(1 << 31);
        while (b != 0) {
            int c = (a & b & x) << 1;
            a ^= b;
            b = c;
        }
        return a;
    }
};
```

#### java

```java
class Solution {
    public int add(int a, int b) {
        while (b != 0) {
            int c = (a & b) << 1;
            a ^= b;
            b = c;
        }
        return a;
    }
}
```

#### python

```python
class Solution:
    def add(self, a: int, b: int) -> int:
        x = 0xffffffff
        a, b = a & x, b & x
        while b != 0:
            a, b = (a ^ b), (a & b) << 1 & x
        return a if a <= 0x7fffffff else ~(a ^ x)
```

## [66-构建乘积数组](https://leetcode-cn.com/problems/gou-jian-cheng-ji-shu-zu-lcof/)

### 1. 题意

给定一个数组 A[0,1,…,n-1]，请构建一个数组 B[0,1,…,n-1]，其中 B 中的元素 B[i]=A[0]×A[1]×…×A[i-1]×A[i+1]×…×A[n-1]。不能使用除法。

### 2. 思路

利用对称关系，左乘一遍，再右乘一遍即可。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    vector<int> constructArr(vector<int>& a) {
        int n = a.size();
        vector<int> b(n, 1);
        for (int i = 1; i < n; i++) {
            b[i] = a[i - 1] * b[i - 1];
        }
        int tmp = 1;
        for (int i = n - 2; i >= 0; i--) {
            tmp *= a[i + 1];
            b[i] *= tmp;
        }
        return b;
    }
};
```

#### java

```java
class Solution {
    public int[] constructArr(int[] a) {
        int n = a.length;
        if (n == 0) {
            return a;
        }
        int[] b = new int[n];
        b[0] = 1;
        for (int i = 1; i < n; i++) {
            b[i] = b[i - 1] * a[i - 1];
        }
        int tmp = 1;
        for (int i = n - 2; i >= 0; i--) {
            tmp *= a[i + 1];
            b[i] *= tmp;
        }
        return b;
    }
}
```

#### python

```python
class Solution:
    def constructArr(self, a: List[int]) -> List[int]:
        b, tmp = [1] * len(a), 1
        for i in range(1, len(a)):
            b[i] = b[i - 1] * a[i - 1]
        for i in range(len(a) - 2, -1, -1): 
            tmp *= a[i + 1]
            b[i] *= tmp
        return b
```

## [67-把字符串转换成整数](https://leetcode-cn.com/problems/ba-zi-fu-chuan-zhuan-huan-cheng-zheng-shu-lcof/)

### 1. 题意

写一个函数 StrToInt，实现把字符串转换成整数这个功能。不能使用 atoi 或者其他类似的库函数。

### 2. 思路

字符串模拟，注意边界溢出情况。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
class Solution {
public:
    int strToInt(string str) {
        int i = 0, flag = 1;
        long res = 0;
        while (str[i] == ' ') {
            i++;
        }
        if (str[i] == '-') {
            flag = -1;
        }
        if (str[i] == '-' || str[i] == '+') {
            i++;
        }
        for (; i < str.size() && isdigit(str[i]); i++)  {
            res = res * 10 + (str[i] - '0');
            if (res >= INT_MAX && flag == 1) {
                return INT_MAX;
            }
            if (res > INT_MAX && flag == -1) {
                return INT_MIN;
            }
        } 
        return flag * res;
    }
};
```

#### java

```java
class Solution {
    public int strToInt(String str) {
        str = str.trim();
        if (str == null || str.length() == 0) {
            return 0;
        }
        boolean positive = true;
        int i = 0;
        if (str.charAt(i) == '+') {
            i++;
        } else if (str.charAt(i) == '-') {
            i++;
            positive = false;
        }
        int ans = 0;
        for (; i < str.length(); i++) {
            int num = str.charAt(i) - '0';
            if (num < 0 || num > 9) {
                break;
            }
            
            if (positive) {
                if (ans > Integer.MAX_VALUE / 10 || ans == Integer.MAX_VALUE / 10 && num > Integer.MAX_VALUE % 10) {
                    return Integer.MAX_VALUE;
                }
                ans = ans * 10 + num;
            } else {
                if (ans < Integer.MIN_VALUE / 10 || ans == Integer.MIN_VALUE / 10 && -num < Integer.MIN_VALUE % 10) {
                    return Integer.MIN_VALUE;
                }
                ans = ans * 10 - num;
            }
        }
        return ans;
    }
}
```

#### python

```python
class Solution:
    def strToInt(self, str: str) -> int:
        str = str.strip()
        if not str: 
            return 0
        res, i, sign = 0, 1, 1
        int_max, int_min, bndry = 2 ** 31 - 1, -2 ** 31, 2 ** 31 // 10
        if str[0] == '-': 
            sign = -1
        elif str[0] != '+': 
            i = 0
        for c in str[i:]:
            if not '0' <= c <= '9': 
                break
            if res > bndry or res == bndry and c > '7':
                return int_max if sign == 1 else int_min
            res = 10 * res + ord(c) - ord('0')
        return sign * res
```

## [68I-二叉搜索树的最近公共祖先](https://leetcode-cn.com/problems/er-cha-sou-suo-shu-de-zui-jin-gong-gong-zu-xian-lcof/)

### 1. 题意

给定一个二叉搜索树, 找到该树中两个指定节点的最近公共祖先。

### 2. 思路

判断 p, q 结点位于根结点的左侧还是右侧，若根结点即为 p 或 q 结点，直接返回；若都在左侧，向左侧遍历。若都在右侧，向右侧遍历。若一左一右，返回根结点即可。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(1)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    TreeNode* lowestCommonAncestor(TreeNode* root, TreeNode* p, TreeNode* q) {
        while (root != nullptr) {
            if (root->val > p->val && root->val > q->val) {
                root = root->left;
            } else if (root->val < p->val && root->val < q->val) {
                root = root->right;
            } else {
                break;
            }
        }
        return root;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public TreeNode lowestCommonAncestor(TreeNode root, TreeNode p, TreeNode q) {
        while (root != null) {
            if (root.val > p.val && root.val > q.val) {
                root = root.left;
            } else if (root.val < p.val && root.val < q.val) {
                root = root.right;
            } else {
                break;
            }
        }
        return root;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def lowestCommonAncestor(self, root: 'TreeNode', p: 'TreeNode', q: 'TreeNode') -> 'TreeNode':
        while root:
            if root.val > p.val and root.val > q.val:
                root = root.left;
            elif root.val < p.val and root.val < q.val:
                root = root.right
            else:
                break;
        return root;
```

## [68II-二叉树的最近公共祖先](https://leetcode-cn.com/problems/gou-jian-cheng-ji-shu-zu-lcof/)

### 1. 题意

给定一个二叉树, 找到该树中两个指定节点的最近公共祖先。

### 2. 思路

递归。

- 时间复杂度：$O(n)$。
- 空间复杂度：$O(n)$。

### 3. 代码

#### cpp

```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    TreeNode* lowestCommonAncestor(TreeNode* root, TreeNode* p, TreeNode* q) {
        if (root == nullptr) {
            return root;
        }
        if (root->val == p->val || root->val == q->val) {
            return root;
        }
        TreeNode* left = lowestCommonAncestor(root->left, p, q);
        TreeNode* right = lowestCommonAncestor(root->right, p, q);
        if (left == nullptr) {
            return right;
        }
        if (right == nullptr) {
            return left;
        }
        return root;
    }
};
```

#### java

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public TreeNode lowestCommonAncestor(TreeNode root, TreeNode p, TreeNode q) {
        if (root == null) {
            return root;
        }
        if (root.val == p.val || root.val == q.val) {
            return root;
        }
        TreeNode left = lowestCommonAncestor(root.left, p, q);
        TreeNode right = lowestCommonAncestor(root.right, p, q);
        if (left == null) {
            return right;
        }
        if (right == null) {
            return left;
        }
        return root;
    }
}
```

#### python

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def lowestCommonAncestor(self, root: TreeNode, p: TreeNode, q: TreeNode) -> TreeNode:
        if not root or root == p or root == q:
            return root
        left = self.lowestCommonAncestor(root.left, p, q)
        right = self.lowestCommonAncestor(root.right, p, q)
        if not left:
            return right
        if not right:
            return left
        return root

```


---
layout:     post
title:      "2020字节跳动夏令营笔试"
subtitle:   " \"研发工程第二批\""
date:       2020-08-01 11:00:00
author:     "LiuJ"
header-img: "img/post-bg-2020.jpg"
catalog: true
tags:
    - 笔经
    - 字节跳动
---

# 2020字节跳动夏令营-研发工程第二次笔试0801

4道单选，2道不定向选，2道填空，4道编程题，总共2个半小时。

涉及方面：数学、概率论、排列组合、博弈、数据结构、算法、操作系统。

## 一、单选

### 1. 零点

图像法，函数 f(x)=x-2sinx 的零点个数可以转换为函数 g(x)=x 和函数 h(x)=2sinx 在坐标系中的交点个数。

### 2. 二叉堆

[堆排序过程](https://blog.csdn.net/sxhelijian/article/details/50295637)

[二叉堆动图演示](https://visualgo.net/en/heap)

### 3. 复杂度

均摊时间复杂度分析。n 个元素，倍增因子为 n， n 次操作进行 (m + 1) * n 次操作，均摊下来就是 m + 1 次。[C++ STL push_back](https://cs.stackexchange.com/questions/9380/why-is-push-back-in-c-vectors-constant-amortized)

### 4. 概率

[红白球问题](http://www.mathchina.net/dvbbs/dv_rss.asp?s=x&boardid=5&id=8079&page=26)

## 二、不定项选

### 1. 排序

[排序算法时间复杂度](https://coer.me/2020/04/09/sort/)

### 2. 多线程

[可见性、原子性、有序性](https://linary.github.io/2019/06/03/java/%E5%B9%B6%E5%8F%91%E7%BC%96%E7%A8%8BBUG%E7%9A%84%E6%BA%90%E5%A4%B4/)

执行顺序。[线程执行](https://www.nowcoder.com/questionTerminal/532ddd8c34e84eaab24c6538b8091445)

## 三、填空

### 1. 递推

先对糖果数加上 5，这样一来可以直接均分拿掉自己那一份。设初始糖果数为 X，最后剩下糖果数为 Y， 则：
$$
Y=(1-\frac{1}{6})^6X=\frac{5^6}{6^6}X
$$
要使 Y 为整数，X 最小取$6^6$，减去最初加上的 5 个糖果，即为答案。

可推广到 M 个人分糖果，结果为$M^M-(M-1)$。

### 2. 二进制

拿韦恩图进行解释，每次输入机器相当于一个集合，n 次输入对应 $2^n-1$个域。

[老鼠与毒药](https://segmentfault.com/a/1190000009123407)

[变体](https://zhuanlan.zhihu.com/p/24375080)

## 四、编程

### 1. 双指针

#### 1.1 题意

输入一行字符串，只包含数字和字符 “-” ，字符串长度不超过 100000，日期格式以 “DD-MM-YYYY" 给出（20-12-2030-12-2020），返回出现次数最多的日子。

#### 1.2 思路

双指针滑动窗口，对每个窗口进行相应的条件判断。

#### 1.3 代码

```java
import java.io.OutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.PrintWriter;
import java.util.StringTokenizer;
import java.util.Map;
import java.util.HashMap;
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.InputStream;

/**
 * Built using CHelper plug-in
 * Actual solution is at the top
 *
 * @author Coer
 */
public class Main {
    public static void main(String[] args) {
        InputStream inputStream = System.in;
        OutputStream outputStream = System.out;
        InputReader in = new InputReader(inputStream);
        PrintWriter out = new PrintWriter(outputStream);
        TaskA solver = new TaskA();
        solver.solve(1, in, out);
        out.close();
    }

    static class TaskA {
        public void solve(int testNumber, InputReader in, PrintWriter out) {
            String s = in.next();
            Map<String, Integer> map = new HashMap<>();
            int n = s.length();
            for (int l = 0, r = 9; r < n; l++, r++) {
                String str = s.substring(l, r + 1);
                if (str.charAt(2) == str.charAt(5) && str.charAt(2) == '-' && validNumber(str, 0, 1) && validNumber(str, 3, 4) && validNumber(str, 6, 9)) {
                    int d = Integer.parseInt(str.substring(0, 2));
                    int m = Integer.parseInt(str.substring(3, 5));
                    int y = Integer.parseInt(str.substring(6, 10));
                    if (y < 2001 || y > 2020) {
                        continue;
                    }
                    if (m < 0 || m > 12) {
                        continue;
                    }
                    if (!validDate(y, m, d)) {
                        continue;
                    }
                    map.put(str, map.getOrDefault(map.get(str), 0) + 1);
                }
            }
            String res = null;
            int mx = 0;
            for (String ss : map.keySet()) {
                if (map.get(ss) > mx) {
                    res = ss;
                    mx = map.get(ss);
                }
            }
            out.println(res);
        }

        private boolean validNumber(String str, int i, int j) {
            for (int k = i; k <= j; k++) {
                if (!(str.charAt(k) >= '0' && str.charAt(k) <= '9')) {
                    return false;
                }
            }
            return true;
        }

        private boolean validDate(int y, int m, int d) {
            boolean isLeap = (y % 4 == 0 && y % 100 != 0) || y % 400 == 0;
            int[] months = {0, 31, isLeap ? 29 : 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};
            return d >= 1 && d <= months[m];
        }

    }

    static class InputReader {
        public BufferedReader reader;
        public StringTokenizer tokenizer;

        public InputReader(InputStream stream) {
            reader = new BufferedReader(new InputStreamReader(stream), 32768);
            tokenizer = null;
        }

        public boolean hasNext() {
            while (tokenizer == null || !tokenizer.hasMoreTokens()) {
                try {
                    tokenizer = new StringTokenizer(reader.readLine());
                } catch (IOException e) {
                    return false;
                }
            }
            return true;
        }

        public String next() {
            if (hasNext()) {
                return tokenizer.nextToken();
            }
            return null;
        }

    }
}
```

### 2. 字符串模拟

#### 2.1 题意

根据输入网段信息和所需查询的 IP 给出所在的机房。[IP与子网掩码](https://blog.csdn.net/ithomer/article/details/51247567)

#### 2.2 思路

手写 ipv4 字符串转整数类型，正好对应 32 位（ ipv4 字符串形式占用 7 - 15 个字节，整数类型占用 4 个字节，以时间换空间），手写子网掩码转换函数，再用位运算、一个哈希维护即可。

#### 2.3 代码

```java
import java.io.OutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.PrintWriter;
import java.util.StringTokenizer;
import java.util.Map;
import java.util.HashMap;
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.InputStream;

/**
 * Built using CHelper plug-in
 * Actual solution is at the top
 *
 * @author Coer
 */
public class Main {
    public static void main(String[] args) {
        InputStream inputStream = System.in;
        OutputStream outputStream = System.out;
        InputReader in = new InputReader(inputStream);
        PrintWriter out = new PrintWriter(outputStream);
        TaskB solver = new TaskB();
        solver.solve(1, in, out);
        out.close();
    }

    static class TaskB {
        private Map<Integer, Integer>[] map;

        public void solve(int testNumber, InputReader in, PrintWriter out) {
            int n = in.nextInt();
            int m = in.nextInt();
            map = new HashMap[32];
            for (int i = 0; i < 32; i++) {
                map[i] = new HashMap<>();
            }
            for (int i = 0; i < n; i++) {
                int id = in.nextInt();
                String _ip = in.next();
                inc(_ip, id);
            }
            for (int i = 0; i < m; i++) {
                String _ip = in.next();
                out.println(query(_ip));
            }
        }

        private void inc(String _ip, int id) {
            Node node = parseIp(_ip);
            int mask = getMask(node.seg);
            node.ip &= mask;
            map[node.seg - 1].put(node.ip, id);
        }

        private int query(String _ip) {
            Node node = parseIp(_ip);
            for (int i = 31; i >= 0; i--) {
                int mask = getMask(i + 1);
                if (map[i].containsKey(node.ip & mask)) {
                    return map[i].get(node.ip & mask);
                }
            }
            return -1;
        }

        private Node parseIp(String _ip) {
            int ans = 0, seg = 31;
            int[] curIps = new int[4];
            StringBuilder sb = new StringBuilder();
            int ids = 0;
            boolean haveSeg = false;

            for (int i = 0; i < _ip.length(); i++) {
                char c = _ip.charAt(i);
                if (c >= '0' && c <= '9') {
                    sb.append(c);
                } else if (c == '.') {
                    curIps[ids++] = Integer.parseInt(sb.toString());
                    sb.delete(0, sb.length());
                } else if (c == '/') {
                    curIps[ids++] = Integer.parseInt(sb.toString());
                    sb.delete(0, sb.length());
                    haveSeg = true;
                }
            }
            if (sb.length() != 0) {
                if (haveSeg) {
                    seg = Integer.parseInt(sb.toString());
                } else {
                    curIps[ids] = Integer.parseInt(sb.toString());
                }
            }
            ans |= curIps[3];
            ans |= curIps[2] << 8;
            ans |= curIps[1] << 16;
            ans |= curIps[0] << 24;

            return new Node(ans, seg);
        }

        private int getMask(int seg) {
            int ans = 0;
            for (int i = 31, j = 0; i >= 0 && j < seg; i--, j++) {
                ans |= 1 << i;
            }
            return ans;
        }

        class Node {
            int ip;
            int seg;

            public Node(int ip, int seg) {
                this.ip = ip;
                this.seg = seg;
            }

        }

    }

    static class InputReader {
        public BufferedReader reader;
        public StringTokenizer tokenizer;

        public InputReader(InputStream stream) {
            reader = new BufferedReader(new InputStreamReader(stream), 32768);
            tokenizer = null;
        }

        public boolean hasNext() {
            while (tokenizer == null || !tokenizer.hasMoreTokens()) {
                try {
                    tokenizer = new StringTokenizer(reader.readLine());
                } catch (IOException e) {
                    return false;
                }
            }
            return true;
        }

        public String next() {
            if (hasNext()) {
                return tokenizer.nextToken();
            }
            return null;
        }

        public int nextInt() {
            return Integer.parseInt(next());
        }

    }
}
```

### 3. 博弈

#### 3.1 题意

给定 n 张牌，先手者第一次抽可以抽任意张但不可抽完，以后每次抽取都只能抽取不超过上一次抽牌数的两倍（不可不抽），谁先抽完谁赢，有多组数据，问先手能赢多少次。

#### 3.2 思路

可先暴力 DP 打表，找出规律。

[BZOJ2275](https://www.cnblogs.com/chenxiaoran666/p/BZOJ2275.html)

[博弈论](https://www.luogu.com.cn/blog/Wolfycz/qian-tan-suan-fa-bo-yi-lun-zong-ling-kai-shi-di-bo-yi-lun-post)

#### 3.3 代码

```java
import java.io.OutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.PrintWriter;
import java.util.StringTokenizer;
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.InputStream;

/**
 * Built using CHelper plug-in
 * Actual solution is at the top
 *
 * @author Coer
 */
public class Main {
    public static void main(String[] args) {
        InputStream inputStream = System.in;
        OutputStream outputStream = System.out;
        InputReader in = new InputReader(inputStream);
        PrintWriter out = new PrintWriter(outputStream);
        TaskC solver = new TaskC();
        solver.solve(1, in, out);
        out.close();
    }

    static class TaskC {
        public void solve(int testNumber, InputReader in, PrintWriter out) {
            int t = in.nextInt();
            int ans = t;
            int[] fib = new int[50];
            fib[0] = 2;
            fib[1] = 3;
            for (int i = 2; i < 50; i++) {
                fib[i] = fib[i - 1] + fib[i - 2];
            }
            while (t-- > 0) {
                int n = in.nextInt();
                for (int i = 0; i < 50; i++) {
                    if (fib[i] == n) {
                        ans--;
                    } else if (fib[i] > n) {
                        break;
                    }
                }
            }
            out.println(ans);
        }

    }

    static class InputReader {
        public BufferedReader reader;
        public StringTokenizer tokenizer;

        public InputReader(InputStream stream) {
            reader = new BufferedReader(new InputStreamReader(stream), 32768);
            tokenizer = null;
        }

        public boolean hasNext() {
            while (tokenizer == null || !tokenizer.hasMoreTokens()) {
                try {
                    tokenizer = new StringTokenizer(reader.readLine());
                } catch (IOException e) {
                    return false;
                }
            }
            return true;
        }

        public String next() {
            if (hasNext()) {
                return tokenizer.nextToken();
            }
            return null;
        }

        public int nextInt() {
            return Integer.parseInt(next());
        }

    }
}
```

### 4. 树

#### 4.1 题意

给定前缀表达式，要求对其进行简化，对重复子树进行重指向。

举例：`+(a,a)` 简化到 `+(a,2)`。

#### 4.2 思路

先构建前缀表达式树，再 dfs 重新计算每个结点的对应 id，最后 dfs 生成结果。

#### 4.3 代码

```java
import java.io.OutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.PrintWriter;
import java.util.StringTokenizer;
import java.util.Map;
import java.util.HashMap;
import java.io.IOException;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.InputStream;

/**
 * Built using CHelper plug-in
 * Actual solution is at the top
 *
 * @author Coer
 */
public class Main {
    public static void main(String[] args) {
        InputStream inputStream = System.in;
        OutputStream outputStream = System.out;
        InputReader in = new InputReader(inputStream);
        PrintWriter out = new PrintWriter(outputStream);
        TaskD solver = new TaskD();
        solver.solve(1, in, out);
        out.close();
    }

    static class TaskD {
        private int id;
        private int stridx;
        private Map<String, TreeNode> map;

        public void solve(int testNumber, InputReader in, PrintWriter out) {
            int t = in.nextInt();
            for (int i = 0; i < t; i++) {
                String exp = in.next();
                id = 1;
                stridx = 0;
                map = new HashMap<>();

                TreeNode root = build(exp).u;

                id = 1;
                reid(root);
                out.println(traverse(root));
            }
        }

        private boolean isSymbol(char c) {
            return c == '+' || c == '-' || c == '*' || c == '/';
        }

        private Node build(String str) {
            if (stridx == str.length()) {
                return new Node(null, "");
            }
            if (str.charAt(stridx) == '(' || str.charAt(stridx) == ')' || str.charAt(stridx) == ',') {
                stridx++;
                return build(str);
            }

            TreeNode u = new TreeNode();
            u.id = id++;
            u.val = str.charAt(stridx);
            String expr = str.substring(stridx, stridx + 1);
            boolean iss = isSymbol(str.charAt(stridx));
            stridx++;

            if (iss) {
                Node nodeL = build(str);
                u.left = nodeL.u;
                Node nodeR = build(str);
                u.right = nodeR.u;
                expr += "(" + nodeL.buffer + "," + nodeR.buffer + ")";
            }

            if (map.containsKey(expr)) {
                u.memo = map.get(expr);
            } else {
                map.put(expr, u);
            }
            return new Node(u, expr);
        }

        private void reid(TreeNode u) {
            if (u == null) {
                return;
            }
            if (u.memo == null) {
                u.id = id++;
            }
            if (u.left != null) {
                reid(u.left);
            }
            if (u.right != null) {
                reid(u.right);
            }
        }

        private String traverse(TreeNode u) {
            if (u == null) {
                return "";
            }
            if (u.memo != null) {
                return String.valueOf(u.memo.id);
            }
            String ans = String.valueOf(u.val);
            if (isSymbol(u.val)) {
                ans += "(" + traverse(u.left) + "," + traverse(u.right) + ")";
            }
            return ans;
        }

        class TreeNode {
            TreeNode left;
            TreeNode right;
            TreeNode memo;
            int id;
            char val;

            TreeNode() {
            }

        }

        class Node {
            TreeNode u;
            String buffer;

            Node(TreeNode u, String buffer) {
                this.u = u;
                this.buffer = buffer;
            }

        }

    }

    static class InputReader {
        public BufferedReader reader;
        public StringTokenizer tokenizer;

        public InputReader(InputStream stream) {
            reader = new BufferedReader(new InputStreamReader(stream), 32768);
            tokenizer = null;
        }

        public boolean hasNext() {
            while (tokenizer == null || !tokenizer.hasMoreTokens()) {
                try {
                    tokenizer = new StringTokenizer(reader.readLine());
                } catch (IOException e) {
                    return false;
                }
            }
            return true;
        }

        public String next() {
            if (hasNext()) {
                return tokenizer.nextToken();
            }
            return null;
        }

        public int nextInt() {
            return Integer.parseInt(next());
        }

    }
}
```


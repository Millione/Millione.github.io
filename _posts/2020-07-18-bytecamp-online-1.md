---
layout:     post
title:      "2020字节跳动夏令营笔试"
subtitle:   " \"研发工程第一批\""
date:       2020-07-18 11:00:00
author:     "LiuJ"
header-img: "img/post-bg-2020.jpg"
catalog: true
tags:
    - 笔经
    - 字节跳动
---

# 2020字节跳动夏令营-研发工程第一次笔试0718

4道单选，2道不定向选，2道填空，4道编程题，总共2个半小时。

涉及方面：数学、概率论、排列组合、博弈、数据结构、算法、操作系统。

## 一、单选

### 1. 概率

条件概率计算：
$$
p(火车|迟到)=\frac {p(火车\&迟到)}{p(迟到)}
$$


### 2. 哈希碰撞

查找成功时的平均查找长度：
$$
\frac {1*3+2*2}{5}
$$
查找不成功时的平均查找长度：
$$
\frac {2+3+1+1+3}{5}
$$
查找成功时分母为哈希表元素个数，查找不成功时分母为哈希表长度。[哈希表查找](https://blog.csdn.net/longlovefilm/article/details/78009782)

### 3. 二叉树

- 已知一颗二叉树的前序和中序遍历，可唯一确定其后序遍历；已知一颗二叉树的中序和后序遍历，可唯一确定其前序遍历；但给定一颗二叉树的前序和后序，却不能唯一确定其中序遍历，不确定性是由一个结点（只有一边子树）的左右子树的不确定性决定的。[已知前序和后序遍历，求中序遍历的可能的序列数](https://blog.csdn.net/qq_37437983/article/details/79613947)

- 度为 0 的结点数为度为 2 的结点数加 1，即具有 n 个叶子结点的二叉树有 n - 1 个度为 2 的结点。[论证](https://blog.csdn.net/u010104750/article/details/49515553)
- 具有 n 个叶子结点的二叉树最多可能有 2n - 1 个结点。

### 4. 进程与线程

线程独享资源：调用栈、调用栈、程序计数器、寄存器。[线程独享、共享资源](http://zhiyi.live/2019/09/14/%E7%BA%BF%E7%A8%8B%E5%85%B1%E4%BA%AB%E5%93%AA%E4%BA%9B%E8%B5%84%E6%BA%90/)

## 二、不定项选

### 1. 排序

稳定排序：冒泡排序、插入排序、归并排序、基数排序。

不稳定排序：选择排序、希尔排序、快速排序、堆排序。

[稳定排序与不稳定排序](https://www.cnblogs.com/codingmylife/archive/2012/10/21/2732980.html)

### 2. 多线程

执行顺序。[线程执行](https://www.nowcoder.com/questionTerminal/532ddd8c34e84eaab24c6538b8091445)

## 三、填空

### 1. 博弈

先开始的同学擦去 47,48,49,...,55 这 9 个数，剩下来的数一一配对，同一对两数之差为55。[黑板数字操作问题](http://kuing.orzweb.net/viewthread.php?tid=6369)

### 2. 排列组合

类似于插隔板，在 20 个数的间隙里插入 3 个隔板，即$C_{19}^{3}$。[组合](https://www.quora.com/If-a+b+c+d-20-how-many-unique-non-negative-integer-solutions-exist-for-a-b-c-d)

## 四、编程

### 1. 最短路BFS

#### 1.1 题意

给定二维数组，数组中值为 0 或 1，1代表障碍。给定起点(x,y)，终点(X,Y)，每一步可以上下左右移动，求出初始到结束的最短路径，若没有则输出 -1。

#### 1.2 思路

直接 BFS 广搜。

#### 1.3 代码

```java
import java.io.OutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.PrintWriter;
import java.util.StringTokenizer;
import java.util.Collection;
import java.io.IOException;
import java.util.Queue;
import java.io.BufferedReader;
import java.util.LinkedList;
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
        Task4C solver = new Task4C();
        solver.solve(1, in, out);
        out.close();
    }

    static class Task4C {
        public void solve(int testNumber, InputReader in, PrintWriter out) {
            int t = in.nextInt();
            while (t-- > 0) {
                int m = in.nextInt(), n = in.nextInt();
                int x = in.nextInt(), y = in.nextInt();
                int X = in.nextInt(), Y = in.nextInt();
                int[][] grid = new int[n][m];
                for (int i = 0; i < n; i++) {
                    for (int j = 0; j < m; j++) {
                        grid[i][j] = in.nextInt();
                    }
                }
                boolean[][] visited = new boolean[n][m];
                boolean isFind = false;
                Queue<Task4C.Node> queue = new LinkedList<>();
                queue.offer(new Task4C.Node(x, y));
                int level = 0;
                while (!queue.isEmpty()) {
                    int sz = queue.size();
                    level++;
                    while (sz-- > 0) {
                        Task4C.Node node = queue.poll();
                        int x1 = node.x, y1 = node.y;
                        if (x1 < 0 || x1 >= m || y1 < 0 || y1 >= n || visited[y1][x1] || grid[y1][x1] == 1) {
                            continue;
                        }
                        if (x1 == X && y1 == Y) {
                            isFind = true;
                            out.println(level);
                            break;
                        }
                        visited[y1][x1] = true;
                        queue.offer(new Task4C.Node(x1 + 1, y1));
                        queue.offer(new Task4C.Node(x1 - 1, y1));
                        queue.offer(new Task4C.Node(x1, y1 + 1));
                        queue.offer(new Task4C.Node(x1, y1 - 1));
                    }
                    if (isFind) {
                        break;
                    }
                }
                if (!isFind) {
                    out.println(-1);
                }
            }
        }

        static class Node {
            public int x;
            public int y;

            public Node(int x, int y) {
                this.x = x;
                this.y = y;
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

        public String next() {
            while (tokenizer == null || !tokenizer.hasMoreTokens()) {
                try {
                    tokenizer = new StringTokenizer(reader.readLine());
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
            return tokenizer.nextToken();
        }

        public int nextInt() {
            return Integer.parseInt(next());
        }

    }
}
```

### 2. 数学

#### 2.1 题意

给定 n 张牌，两人分别从中抽 1~m 张牌，谁先抽完谁赢，有多组数据，问先手能赢多少次。

#### 2.2 思路

只要$n\%(m+1)=0$，则后手必赢，否则先手赢。 

#### 2.3 代码

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
        Task4A solver = new Task4A();
        solver.solve(1, in, out);
        out.close();
    }

    static class Task4A {
        public void solve(int testNumber, InputReader in, PrintWriter out) {
            int t = in.nextInt();
            int ans = 0;
            for (int i = 0; i < t; i++) {
                int n = in.nextInt();
                int m = in.nextInt();
                if (n % (m + 1) != 0) {
                    ans++;
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

        public String next() {
            while (tokenizer == null || !tokenizer.hasMoreTokens()) {
                try {
                    tokenizer = new StringTokenizer(reader.readLine());
                } catch (IOException e) {
                    throw new RuntimeException(e);
                }
            }
            return tokenizer.nextToken();
        }

        public int nextInt() {
            return Integer.parseInt(next());
        }

    }
}
```

### 3. 字符串

#### 3.1 题意

将 Json 字符串中的注释去掉，注释有 // 和 /* 两种。

#### 3.2 思路

字符串模拟，分情况讨论。// 单行， /* 单行与多行。

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
        Task4D solver = new Task4D();
        solver.solve(1, in, out);
        out.close();
    }

    static class Task4D {
        public void solve(int testNumber, InputReader in, PrintWriter out) {
            boolean flag = false;
            String s = null;
            while ((s = in.nextLine()) != null) {
                if (flag) {
                    int id2 = s.indexOf("*/");
                    if (id2 == -1) {
                        continue;
                    }
                    flag = false;
                    out.print(s.substring(id2 + 2));
                }
                int id2 = s.indexOf("/*");
                if (id2 != -1) {
                    out.print(s.substring(0, id2));
                    flag = true;
                    int id3 = s.indexOf("*/");
                    if (id3 != -1) {
                        flag = false;
                        out.print(s.substring(id3 + 2));
                    }
                } else if (!flag) {
                    int id1 = s.indexOf("//");
                    if (id1 != -1) {
                        out.print(s.substring(0, id1));
                    } else {
                        out.print(s);
                    }
                }
                out.println("");
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

        public String nextLine() {
            try {
                return reader.readLine();
            } catch (IOException e) {
                return null;
            }
        }

    }
}
```

### 4. 树形DP

#### 4.1 题意

给定一个 n 节点的树，gcd(x,y)表示树的 x 节点到 y 节点的一条路径上所有节点的最大公约数，dist(x,y)表示路径的长度（节点数）。求gcd(x,y) > 1的所有路径中最大的dist(x,y)。就是求一条路径上所有节点的公约数值大于1的最长路径。

[[Educational Codeforces Round 58 (Rated for Div. 2) D. GCD Counting]](https://codeforces.com/contest/1101/problem/D)

#### 4.2 思路

[DFS](https://blog.csdn.net/swust5120166213/article/details/86410278)

[分解质因子&树形DP](https://blog.csdn.net/qq_38891827/article/details/86354057)

#### 4.3 代码

```java
import java.io.OutputStream;
import java.io.IOException;
import java.io.InputStream;
import java.io.PrintWriter;
import java.util.HashMap;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.List;
import java.util.StringTokenizer;
import java.util.Map;
import java.io.BufferedReader;
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
        Task4B solver = new Task4B();
        solver.solve(1, in, out);
        out.close();
    }

    static class Task4B {
        private int n;
        private int[] a;
        private List<Integer>[] fac;
        private List<Integer>[] e;
        private int ans;
        private Map<Integer, Integer>[] map;

        public void solve(int testNumber, InputReader in, PrintWriter out) {
            n = in.nextInt();
            a = new int[n + 1];
            fac = new ArrayList[n + 1];
            e = new ArrayList[n + 1];
            map = new HashMap[n + 1];
            for (int i = 1; i <= n; i++) {
                a[i] = in.nextInt();
                fac[i] = new ArrayList<>();
                e[i] = new ArrayList<>();
                map[i] = new HashMap<>();
                getDiv(i);
            }
            for (int i = 1; i < n; i++) {
                int u = in.nextInt();
                int v = in.nextInt();
                e[u].add(v);
                e[v].add(u);
            }
            ans = 0;
            dfs(1, -1);
            out.println(ans);
        }

        private void dfs(int st, int fa) {
            for (int i = 0; i < fac[st].size(); i++) {
                map[st].put(fac[st].get(i), 1);
            }
            for (int i = 0; i < e[st].size(); i++) {
                int next = e[st].get(i);
                if (next == fa) {
                    continue;
                }
                dfs(next, st);
                for (int j = 0; j < fac[st].size(); j++) {
                    int div = fac[st].get(j);
                    map[st].put(div, Math.max(map[st].getOrDefault(div, 0), map[next].getOrDefault(div, 0) + 1));
                    ans = Math.max(ans, map[st].get(div));
                    for (int k = 0; k < i; k++) {
                        ans = Math.max(ans, map[next].getOrDefault(div, 0) + map[e[st].get(k)].getOrDefault(div, 0) + 1);
                    }
                }
            }
        }

        private void getDiv(int x) {
            int tmp = a[x];
            for (int i = 2; i * i <= tmp; i++) {
                if (tmp % i == 0) {
                    fac[x].add(i);
                    while (tmp % i == 0) {
                        tmp /= i;
                    }
                }
            }
            if (tmp != 1) {
                fac[x].add(tmp);
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


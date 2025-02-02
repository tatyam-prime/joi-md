配点： $100$ 点

### 問題文
長さ $N$ の整数列 $A = (A_1, A_2, \ldots, A_N)$ と長さ $M$ の整数列 $B = (B_1, B_2, \ldots, B_M)$ が与えられる．

次の条件をすべて満たす $2$ つの整数の組 $(i, j)$ の個数を求めよ．

- $1 \leqq i \leqq N$．
- $1 \leqq j \leqq M$．
- $A_i \leqq B_j$．

### 制約
- $1 \leqq N \leqq 100$．
- $1 \leqq M \leqq 100$．
- $1 \leqq A_i \leqq 2\,000$ ($1 \leqq i \leqq N$)．
- $1 \leqq B_j \leqq 2\,000$ ($1 \leqq j \leqq M$)．

---

### 入力
入力は以下の形式で標準入力から与えられる．

~~~
$N$ $M$
$A_1$ $A_2$ $\cdots$ $A_N$
$B_1$ $B_2$ $\cdots$ $B_M$
~~~

### 出力
$A_i \leqq B_j$ を満たす $(i, j)$ の個数を出力せよ．

---

### 入力例 1
~~~
5 4
3 8 10 5 5
1 5 4 9
~~~

### 出力例 1
~~~
8
~~~

$(1, 2), (1, 3), (1, 4), (2, 4), (4, 2), (4, 4), (5, 2), (5, 4)$ の $8$ つの組が条件を満たすので，$8$ を出力する．

---

### 入力例 2
~~~
3 5
2000 2000 2000
1 1 1 1 1
~~~

### 出力例 2
~~~
0
~~~

条件を満たす $(i, j)$ の組は存在しないので $0$ を出力する．

---

### 入力例 3
~~~
1 1
1000
1000
~~~

### 出力例 3
~~~
1
~~~

---

### 入力例 4
~~~
10 10
3 1 4 1 5 9 2 6 5 3
2 7 1 8 2 8 1 8 2 8
~~~

### 出力例 4
~~~
58
~~~

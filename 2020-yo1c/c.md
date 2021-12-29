配点： $100$ 点

### 問題文
長さ $N$ の正整数列 $A = (A_1, A_2, \ldots, A_N)$ が与えられる．正整数列 $A$ の連続部分列の中で昇順に並んでいるもののうち，最長のものの長さを求めよ．

すなわち，$A_l \leqq A_{l + 1} \leqq \cdots \leqq A_r$ を満たすような $2$ つの整数 $l, r$ ($1 \leqq l \leqq r \leqq N$) について，$r - l + 1$ の最大値を求めよ．

### 制約

- $1 \leqq N \leqq 100$．
- $1 \leqq A_i \leqq 2\,020$ ($1 \leqq i \leqq N$)．

---

### 入力
入力は以下の形式で標準入力から与えられる．

~~~
$N$
$A_1$ $A_2$ $\cdots$ $A_N$
~~~

### 出力
正整数列 $A$ の連続部分列の中で昇順に並んでいるもののうち，最長のものの長さを $1$ 行で出力せよ．

---

### 入力例 1
~~~
10
3 1 4 1 5 9 2 6 5 3
~~~

### 出力例 1
~~~
3
~~~

正整数列 $A$ の $4$ 項目から $6$ 項目までに対応する連続部分列は $1, 5, 9$ であり，これは昇順である．これより長い昇順な連続部分列は存在しない．

---

### 入力例 2
~~~
10
9 8 7 6 5 5 4 3 2 1
~~~

### 出力例 2
~~~
2
~~~

正整数列 $A$ の $5$ 項目から $6$ 項目までに対応する連続部分列は $5, 5$ であり，これは昇順である．これより長い昇順な連続部分列は存在しない．

---

### 入力例 3
~~~
9
1 2 2 12 120 210 202 1010 2020
~~~

### 出力例 3
~~~
6
~~~

正整数列 $A$ の $5$ 項目から $6$ 項目までに対応する連続部分列は $5, 5$ であり，これは昇順である．これより長い昇順な連続部分列は存在しない．
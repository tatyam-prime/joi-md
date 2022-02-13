配点： $100$ 点

### 問題文
$N$ 個のボールがあり，$1$ から $N$ までの番号が付けられている．また，何個でもボールを入れることのできる $N$ 個の箱があり，箱には $1$ から $N$ までの番号が付けられている．

箱 $i$ ($1 \leqq i \leqq N$) には最初，ボール $i$ が入っていた．

JOI 高校の生徒である葵は，この状態から箱とボールに対して $M$ 回の操作を行った．$j$ 回目 ($1 \leqq j \leqq M$) の操作は，次のように行われた．

- ボール $X_j$ が入っている箱を探し，その箱からボール $X_j$ を取り出す．その後，箱 $Y_j$ にボール $X_j$ を入れる．

葵が $M$ 回の操作をすべて終えた後，$N$ 個のボールがそれぞれどの箱に入っているかを求めよ．

### 制約
- $1 \leqq N \leqq 2\,000$．
- $1 \leqq M \leqq 2\,000$．
- $1 \leqq X_j \leqq N$ ($1 \leqq j \leqq M$)．
- $1 \leqq Y_j \leqq N$ ($1 \leqq j \leqq M$)．
- 入力される値はすべて整数である．

---

### 入力
入力は以下の形式で標準入力から与えられる．

~~~
$N$ $M$
$X_1$ $Y_1$
$X_2$ $Y_2$
$\vdots$
$X_M$ $Y_M$
~~~

### 出力
$N$ 行で出力せよ．$i$ 行目 ($1 \leqq i \leqq N$) には，葵が $M$ 回の操作をすべて終えた後，ボール $i$ が入っている箱の番号を出力せよ．

---

### 入力例 1
~~~
3 4
1 2
3 2
2 1
1 3
~~~

### 出力例 1
~~~
3
1
2
~~~

最初，箱 $1$ にはボール $1$ が，箱 $2$ にはボール $2$ が，箱 $3$ にはボール $3$ が入っていた．

葵は以下のように，$4$ 回の操作を行った．

- $1$ 回目の操作では，ボール $1$ を箱 $1$ から取り出した後，箱 $2$ に入れた．
- $2$ 回目の操作では，ボール $3$ を箱 $3$ から取り出した後，箱 $2$ に入れた．
- $3$ 回目の操作では，ボール $2$ を箱 $2$ から取り出した後，箱 $1$ に入れた．
- $4$ 回目の操作では，ボール $1$ を箱 $2$ から取り出した後，箱 $3$ に入れた．

操作をすべて終えた後，ボール $1$ は箱 $3$ ，ボール $2$ は箱 $1$ ，ボール $3$ は箱 $2$ に入っている．したがって，$3,1,2$ をこの順に改行区切りで出力する．

---

### 入力例 2
~~~
3 3
1 1
2 2
3 3
~~~

### 出力例 2
~~~
1
2
3
~~~

操作をすべて終えた後，ボール $1$ は箱 $1$ ，ボール $2$ は箱 $2$ ，ボール $3$ は箱 $3$ に入っている．したがって，$1,2,3$ をこの順に改行区切りで出力する．

---

### 入力例 3
~~~
4 2
1 3
2 4
~~~

### 出力例 3
~~~
3
4
3
4
~~~

---

### 入力例 4
~~~
4 8
1 3
3 2
2 4
2 3
4 1
2 1
1 4
3 3
~~~

### 出力例 4
~~~
4
1
3
1
~~~
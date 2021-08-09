配点： $100$ 点

###
JOI 氏のコレクションルームには非常に大きな机があり，その上には何枚もの貴重なコインがある．机の掃除をするために，JOI 氏はコインを整理して並べることにした．

机は $2\,000\,000\,001 \times 2\,000\,000\,001$ のマス目になっている．列には左から順に $-1\,000\,000\,000$ から $1\,000\,000\,000$ までの番号がつけられており，行には下から順に $-1\,000\,000\,000$ から $1\,000\,000\,000$ までの番号がつけられている．列の番号が $x$，行の番号が $y$ であるマスを ($x, y$) で表すことにする．

コインは $2N$ 枚あり，現在，$i$ 番目 ($1 \leqq i \leqq 2N$) のコインはマス ($X_i, Y_i$) に置かれている．JOI 氏の目標は，$1 \leqq x \leqq N$ かつ $1 \leqq y \leqq 2$ を満たす ($x, y$) で表される $2N$ 個のマスに，それぞれコインが $1$ 枚ずつ置かれている状態にすることである．コインを傷つけないようにするため，「コインを $1$ 枚選び，それが置かれているマスと辺で隣り合ったマスのいずれかに，そのコインを移動させる」という操作のみができる．途中，複数のコインが同じマスに置かれていてもよい．JOI 氏は，できるだけ少ない回数の操作で目標を達成したい．

コインの枚数と，現在コインが置かれているマスが与えられたとき，目標を達成するために必要な操作回数の最小値を求めるプログラムを作成せよ．

---

### 入力
入力は以下の形式で標準入力から与えられる．

~~~
$N$
$X_1$ $Y_1$
$\vdots$
$X_{2N}$ $Y_{2N}$
~~~

### 出力
標準出力に，目標を達成するために必要な操作回数の最小値を $1$ 行で出力せよ．

---

### 制約
- $1 \leqq N \leqq 100\,000$．
- $-1\,000\,000\,000 \leqq X_i \leqq 1\,000\,000\,000$ ($1 \leqq i \leqq 2N$)．
- $-1\,000\,000\,000 \leqq Y_i \leqq 1\,000\,000\,000$ ($1 \leqq i \leqq 2N$)．

### 小課題
1. ($8$ 点) $N \leqq 10$．
2. ($29$ 点) $N \leqq 1\,000$．
3. ($63$ 点) 追加の制約はない．

---

### 入力例 1
~~~
3
0 0
0 4
4 0
2 1
2 5
-1 1
~~~

### 出力例 1
~~~
15
~~~

この入力例では，$6$ 個のコインが下図のように置かれている．太枠で示した位置にコインを集めるのが目標である．

![](https://img.atcoder.jp/joi2019ho/2019-ho-t4-fig01.png)

例えば，コインを以下のように移動させると，$15$ 回の操作で目標を達成できる：

- $1$ 番目のコイン：($0, 0$) → ($1, 0$) → ($1, 1$) → ($1, 2$)
- $2$ 番目のコイン：($0, 4$) → ($1, 4$) → ($1, 3$) → ($2, 3$) → ($3, 3$) → ($3, 2$)
- $3$ 番目のコイン：($4, 0$) → ($4, 1$) → ($3, 1$)
- $5$ 番目のコイン：($2, 5$) → ($2, 4$) → ($2, 3$) → ($2, 2$)
- $6$ 番目のコイン：($-1, 1$) → ($0, 1$) → ($1, 1$)

$14$ 回以下の操作で目標を達成することはできないので，$15$ を出力する．

---

### 入力例 2
~~~
4
2 1
2 1
2 1
3 1
3 1
3 1
3 1
3 1
~~~

### 出力例 2
~~~
9
~~~

同じマスに複数のコインが置かれているかもしれない．

---

### 入力例 3
~~~
5
1000000000 1000000000
-1000000000 1000000000
-1000000000 -1000000000
1000000000 -1000000000
-1 -5
-2 2
2 8
4 7
-2 5
7 3
~~~

### 出力例 3
~~~
8000000029
~~~
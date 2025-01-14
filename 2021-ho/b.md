配点： $100$ 点

###
JOI 平原は東西方向に広がるとても大きな平原である．この平原は数直線と見なすことができ，各地点は東向きを正とする座標であらわされる．JOI 平原は冬を迎え $N$ 個の雪玉が異なる座標に作られた．雪玉には西から順に $1$ から $N$ までの番号が付いている．最初，雪玉 $i$ ($1 \leqq i \leqq N$) の座標は整数 $X_i$ であった．

また JOI 平原は冬に強い風が吹くことで知られている．あなたは $Q$ 日間の風の観測データを入手した．$j$ 日目 ($1 \leqq j \leqq Q$) の風のデータは整数 $W_j$ であらわされる．$W_j$ が負のときは西向きに，$W_j$ が負でないときは東向きに，強さ $\lvert W_j \rvert$ の風が吹いたことを意味する．

風が吹くと，雪玉は風と同じ向きに，風の強さと同じ距離だけ転がる．すなわち $j$ 日目 ($1 \leqq j \leqq Q$) の始めに座標 $x$ に雪玉があったとき，その雪玉は座標 $x$ から座標 $x + W_j$ まで転がる．$j$ 日目の終わりには，その雪玉の座標は $x + W_j$ になる．ただし，各日においてすべての雪玉が同時に，同じ速さで転がる．

最初，JOI 平原全体に雪が積もっていた．雪が積もっている範囲を雪玉が転がると，雪が付着し，雪玉の重さが増え，その範囲の雪はなくなる．すなわち，$a$を整数とし，座標 $a$ から座標 $a + 1$ までの範囲に雪が残っているとする．このとき，雪玉がこの範囲を転がると，その雪玉の重さが $1$ 増えて，座標 $a$ から座標 $a + 1$ までの範囲の雪がなくなる．ただし，雪が残っていない範囲を雪玉が転がったとしても，雪玉の重さは変わらない．

最初，すべての雪玉の重さは $0$ であった．また，観測した $Q$ 日間に新たに雪は降らなかった．

あなたは $Q$ 日目の終わりにおける雪玉の重さを知りたい．

雪玉の最初の座標，$Q$ 日間の風の観測データが与えられたとき，$Q$ 日目の終わりにおける，それぞれの雪玉の重さを求めるプログラムを作成せよ．

---

### 入力
入力は以下の形式で標準入力から与えられる．入力される値はすべて整数である．
~~~
$N$ $Q$
$X_1$ $\cdots$ $X_N$
$W_1$
$\vdots$
$W_Q$
~~~

### 出力
標準出力に $N$ 行で出力せよ．$i$ 行目 ($1 \leqq i \leqq N$) には $Q$ 日目の終わりにおける，雪玉 $i$ の重さを出力せよ．

---

### 制約
- $1 \leqq N \leqq 200\,000$．
- $1 \leqq Q \leqq 200\,000$．
- $\lvert X_i \rvert \leqq 1\,000\,000\,000\,000 \ (= 10^{12})$ ($1 \leqq i \leqq N$)．
- $X_i < X_{i + 1}$ ($1 \leqq i \leqq N - 1$)．
- $\lvert W_j \rvert \leqq 1\,000\,000\,000\,000 \ (= 10^{12})$ ($1 \leqq j \leqq Q$)．

### 小課題
1. ($33$ 点) $N \leqq 2\,000$，$Q \leqq 2\,000$．
2. ($67$ 点) 追加の制約はない．

---

### 入力例 1
~~~
4 3
-2 3 5 8
2
-4
7
~~~

### 出力例 1
~~~
5
4
2
6
~~~

この入力例では，雪玉の座標と重さは以下のように変化する．

- 最初，各雪玉の座標は，雪玉 $1$ から順に $-2, 3, 5, 8$ である．各雪玉の重さは，雪玉 $1$ から順に $0, 0, 0, 0$ である．
- $1$ 日目には東向きに強さ $2$ の風が吹く．$1$ 日目の終わりにおける，各雪玉の座標は，雪玉 $1$ から順に $0, 5, 7, 10$ である．各雪玉の重さは，雪玉 $1$ から順に $2, 2, 2, 2$ である．
- $2$ 日目には西向きに強さ $4$ の風が吹く．$2$ 日目の終わりにおける，各雪玉の座標は，雪玉 $1$ から順に $-4, 1, 3, 6$ である．各雪玉の重さは，雪玉 $1$ から順に $4, 4, 2, 3$ である．
- $3$ 日目には東向きに強さ $7$ の風が吹く．$3$ 日目の終わりにおける，各雪玉の座標は，雪玉 $1$ から順に $3, 8, 10, 13$ である．各雪玉の重さは，雪玉 $1$ から順に $5, 4, 2, 6$ である．

よって$3$ 日目の終わりにおける，各雪玉の重さ $5, 4, 2, 6$ を順に出力する．

---

### 入力例 2
~~~
1 4
1000000000000
1000000000000
-1000000000000
-1000000000000
-1000000000000
~~~

### 出力例 2
~~~
3000000000000
~~~

---

### 入力例 3
~~~
10 10
-56 -43 -39 -31 -22 -5 0 12 18 22
-3
0
5
-4
-2
10
-13
-1
9
6
~~~

### 出力例 3
~~~
14
8
7
9
11
10
9
8
5
10
~~~

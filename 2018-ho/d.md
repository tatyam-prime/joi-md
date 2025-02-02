配点： $100$ 点

###
JOI 君が住む都市には $N$ 個の駅があり，それぞれ $1, 2, \ldots, N$ の番号が付けられている．また，$M$ 本の鉄道路線があり，それぞれ $1, 2, \ldots, M$ の番号が付けられている．鉄道路線 $i$ ($1 \leqq i \leqq M$) は駅 $A_i$ と駅 $B_i$ を双方向に結んでおり，乗車運賃は $C_i$ 円である．

JOI 君は駅 $S$ の近くに住んでおり，駅 $T$ の近くの IOI 高校に通っている．そのため，両者を結ぶ定期券を購入することにした．定期券を購入する際には，駅 $S$ と駅 $T$ の間を最小の運賃で移動する経路を一つ指定しなければならない．この定期券を用いると，指定した経路に含まれる鉄道路線は双方向に自由に乗り降りできる．

JOI 君は，駅 $U$ および駅 $V$ の近くにある書店もよく利用している．そこで，駅 $U$ から駅 $V$ への移動にかかる運賃ができるだけ小さくなるように定期券を購入したいと考えた．

駅 $U$ から駅 $V$ への移動の際は，まず駅 $U$ から駅 $V$ への経路を $1$ つ選ぶ．この経路に含まれる鉄道路線 $i$ において支払うべき運賃は，

- 鉄道路線 $i$ が定期券を購入する際に指定した経路に含まれる場合，$0$ 円
- 鉄道路線 $i$ が定期券を購入する際に指定した経路に含まれない場合，$C_i$ 円

となる．この運賃の合計が，駅 $U$ から駅 $V$ への移動にかかる運賃である．定期券を購入する際に指定する経路をうまく選んだときの，駅 $U$ から駅 $V$ への移動にかかる運賃の最小値を求めたい．

### 課題
定期券を購入する際に指定する経路をうまく選んだときの，駅 $U$ から駅 $V$ への移動にかかる運賃の最小値を求めるプログラムを作成せよ．

---

### 入力
標準入力から以下の入力を読み込め．

- $1$ 行目には，$2$ 個の整数 $N, M$ が書かれている．これらは，JOI 君が住む都市に $N$ 個の駅と $M$ 本の鉄道路線があることを表す．
- $2$ 行目には，$2$ 個の整数 $S, T$ が書かれている．これらは，JOI 君が駅 $S$ から駅 $T$ への定期券を購入することを表す．
- $3$ 行目には，$2$ 個の整数 $U, V$ が書かれている．これらは，JOI 君が駅 $U$ から駅 $V$ への移動にかかる運賃を最小化したいことを表す．
- 続く $M$ 行のうちの $i$ 行目 ($1 \leqq i \leqq M$) には，$3$ 個の整数 $A_i$, $B_i$, $C_i$ が書かれている．これらは，鉄道路線 $i$ が駅 $A_i$ と駅 $B_i$ を双方向に結び，その運賃が $C_i$ 円であることを表す．

### 出力
標準出力に，定期券を購入する際に駅 $S$ から駅 $T$ への経路をうまく指定したときの，駅 $U$ から駅 $V$ への移動にかかる運賃の最小値を $1$ 行で出力せよ．

---

### 制限
すべての入力データは以下の条件を満たす．

- $2 \leqq N \leqq 100\,000$．
- $1 \leqq M \leqq 200\,000$．
- $1 \leqq S \leqq N$．
- $1 \leqq T \leqq N$．
- $1 \leqq U \leqq N$．
- $1 \leqq V \leqq N$．
- $S \neq T$．
- $U \neq V$．
- $S \neq U$ または $T \neq V$．
- どの駅から他のどの駅へも $1$ 本以上の鉄道路線を用いて到達できる．
- $1 \leqq A_i < B_i \leqq N$ ($1 \leqq i \leqq M$)．
- $1 \leqq i < j \leqq M$ に対し，$A_i \neq A_j$ または $B_i \neq B_j$．
- $1 \leqq Ci \leqq 1\,000\,000\,000$ ($1 \leqq i \leqq M$)．

### 小課題
#### 小課題 1 [16 点]
- $S = U$ を満たす．

#### 小課題 2 [15 点]
- 駅 $S$ から駅 $T$ へ最小の運賃で移動するときに用いることができる経路は $1$ 通りしかない．

#### 小課題 3 [24 点]
- $N \leqq 300$ を満たす．

#### 小課題 4 [45 点]
- 追加の制限はない．

---

### 入力例 1
~~~
6 6
1 6
1 4
1 2 1
2 3 1
3 5 1
2 4 3
4 5 2
5 6 1
~~~

### 出力例 1
~~~
2
~~~
この入力例では，定期券を買う際に指定できる経路は駅 $1$ → 駅 $2$ → 駅 $3$ → 駅 $5$ → 駅 $6$ という経路に限られる．

駅 $1$ から駅 $4$ への移動にかかる運賃を最小化するには，駅 $1$ → 駅 $2$ → 駅 $3$ → 駅 $5$ → 駅 $4$ という経路を選べばよい．この経路を選んだ場合，各鉄道路線において支払うべき運賃は，

- 駅 $4$ と駅 $5$ を結ぶ鉄道路線 $5$ においては，$2$ 円．
- それ以外の鉄道路線においては，$0$ 円．

となるので，かかる運賃の合計は $2$ 円となる．

---

### 入力例 2
~~~
6 5
1 2
3 6
1 2 1000000000
2 3 1000000000
3 4 1000000000
4 5 1000000000
5 6 1000000000
~~~

### 出力例 2
~~~
3000000000
~~~

この入力例では，駅 $3$ から駅 $6$ への移動に定期券を用いない．

---

### 入力例 3
~~~
8 8
5 7
6 8
1 2 2
2 3 3
3 4 4
1 4 1
1 5 5
2 6 6
3 7 7
4 8 8
~~~

### 出力例 3
~~~
15
~~~

---

### 入力例 4
~~~
5 5
1 5
2 3
1 2 1
2 3 10
2 4 10
3 5 10
4 5 10
~~~

### 出力例 4
~~~
0
~~~

---

### 入力例 5
~~~
10 15
6 8
7 9
2 7 12
8 10 17
1 3 1
3 8 14
5 7 15
2 3 7
1 10 14
3 6 12
1 5 10
8 9 1
2 9 7
1 4 1
1 8 1
2 4 7
5 6 16
~~~

### 出力例 5
~~~
19
~~~

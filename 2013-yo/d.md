配点： $100$ 点

### 問題
日本が冬であるこの時期，南半球にあるオーストラリアでは暑い日が続いている．オーストラリアに住む IOI 君は，ある $D$ 日間の天気予報をもとに，着る服の計画を立てることにした．$i$ 日目 ($1 \leqq i \leqq D$) の最高気温は $T_i$ 度であると予報されている．

IOI 君は $N$ 種類の服を持っており，それらには $1$ から $N$ までの番号がついている．服 $j$ ($1 \leqq j \leqq N$) は最高気温が $A_j$ 度以上 $B_j$ 度以下の日に着るのに適している．また，それぞれの服には「派手さ」とよばれる整数が定まっており，服 $j$ の派手さは $C_j$ である．

$D$ 日間のそれぞれに対し，IOI 君は，最高気温が天気予報に従ったときに着るのに適した服のうち $1$ つを着る服として選ぶ．同じ服を何度選んでもよいし，$D$ 日間で一度も選ばれない服があってもよい．

似ている服を連続して着ることをなるべく避けようと思った IOI 君は，連続する日に着る服の派手さの差の絶対値の合計をできるだけ大きくしようと考えた．すなわち，$i$ 日目に服 $x_i$ を選んだとして，値 $|C_{x_1} - C_{x_2}| + |C_{x_2} - C_{x_3}| + \cdots + |C_{x_{D-1}} - C_{x_D}|$ を最大にしたい．この最大値を求めるプログラムを作成せよ．

---

### 入力
入力は $1 + D + N$ 行からなる．

$1$ 行目には，$2$ つの整数 $D, N$ ($2 \leqq D \leqq 200$，$1 \leqq N \leqq 200$) が空白を区切りとして書かれている．$D$ は服の計画を立てる日数，$N$ は IOI 君が持っている服の種類の数を表す．

続く $D$ 行のうちの $i$ 行目 ($1 \leqq i \leqq D$) には，$1$ つの整数 $T_i$ ($0 \leqq T_i \leqq 60$) が書かれている．これは，$i$ 日目の最高気温が $T_i$ 度であると予報されていることを表す．

続く $N$ 行のうちの $j$ 行目 ($1 \leqq j \leqq N$) には，$3$ つの整数 $A_j, B_j, C_j$ ($0 \leqq A_j \leqq B_j \leqq 60$，$0 \leqq C_j \leqq 100$) が書かれている．これらは，服 $j$ は最高気温が $A_j$ 度以上 $B_j$ 度以下の日に着るのに適しており，派手さが $C_j$ であることを表す．

最高気温が天気予報に従ったときに着るのに適した服が，$D$ 日間のどの日に対しても $1$ つ以上存在することが保証されている．

### 出力
連続する日に着る服の派手さの差の絶対値の合計，すなわち，値 $|C_{x_1} - C_{x_2}| + |C_{x_2} - C_{x_3}| + \cdots + |C_{x_{D - 1}} - C_{x_D}|$ の最大値を $1$ 行で出力せよ．

---

### 入力例 1
~~~
3 4
31
27
35
20 25 30
23 29 90
21 35 60
28 33 40
~~~

### 出力例 1
~~~
80
~~~

入出力例 $1$ において，$1$ 日目の服の候補は服 $3$ と服 $4$ であり，$2$ 日目の服の候補は服 $2$ と服 $3$ であり，$3$ 日目の服の候補は服 $3$ のみである．$1$ 日目に服 $4$ を，$2$ 日目に服 $2$ を，$3$ 日目に服 $3$ を選ぶ．すなわち，$x_1 = 4$，$x_2 = 2$，$x_3 = 3$ とする．このとき，$1$ 日目と $2$ 日目の服の派手さの差の絶対値は $|40 - 90| = 50$ であり，$2$ 日目と $3$ 日目の服の派手さの差の絶対値は $|90 - 60| = 30$ である．合計は $80$ となり，これが最大値である．

---

### 入力例 2
~~~
5 2
26
28
32
29
34
30 35 0
25 30 100
~~~

### 出力例 2
~~~
300
~~~

入出力例 $2$ において，$1$ 日目には服 $2$ を，$2$ 日目には服 $2$ を，$3$ 日目には服 $1$ を，$4$ 日目には服 $2$ を，$5$ 日目には服 $1$ を選ばなければならない．このとき，求める値は $|100 - 100| + |100 - 0| + |0 - 100| + |100 - 0| = 300$ となる．

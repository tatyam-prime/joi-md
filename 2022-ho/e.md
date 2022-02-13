配点： $100$ 点

###

JOI 君は，砂浜で砂の城を作って遊んだ．JOI 君が作った城は，砂浜のある長方形の領域に含まれている．この長方形の領域は縦 $H$ 行，横 $W$ 列に区切られたマス目として表され，縦方向は南北方向に平行であり，横方向は東西方向に平行である．北から $i$ 行目 ($1 \leqq i \leqq H$)，西から $j$ 列目 ($1 \leqq j \leqq W$) のマスの高さは $A_{i, j}$ である．**ただし，$A_{i, j}$ の値はすべて相異なる．**

この砂の城に対し，JOI 君は以下の行動を行った．

1. あるマスを選び，そのマスの上からスタートする．
2. その後，東西南北に隣接する**より低い**マスの上に移動することを，$0$ 回以上繰り返す．

最終的に JOI 君が訪れたマスの領域を上から見ると，これは $1$ つの長方形で表された．

各マスの高さ $A_{i, j}$ の情報が与えられたとき，JOI 君が訪れたマスの長方形領域としてあり得るものが何通りあるかを求めるプログラムを作成せよ．

---

### 入力

入力は以下の形式で標準入力から与えられる．入力される値はすべて整数である．

~~~
$H$ $W$
$A_{1, 1}$ $A_{1, 2}$ $\cdots$ $A_{1, W}$
$A_{2, 1}$ $A_{2, 2}$ $\cdots$ $A_{2, W}$
$\vdots$
$A_{H, 1}$ $A_{H, 2}$ $\cdots$ $A_{H, W}$
~~~

### 出力

標準出力に，JOI 君が訪れたマスの長方形領域としてあり得るものが何通りあるかを，$1$ 行で出力せよ．

---

### 制約

- $H \geqq 1$．
- $W \geqq 1$．
- $H \times W \leqq 50\,000$．
- $1 \leqq A_{i, j} \leqq 10\,000\,000$ ($1 \leqq i \leqq H$，$1 \leqq j \leqq W$)．
- $A_{i_1, j_1} \neq A_{i_2, j_2}$ ($1 \leqq i_1 \leqq H$，$1 \leqq j_1 \leqq W$，$1 \leqq i_2 \leqq H$，$1 \leqq j_2 \leqq W$，$(i_1, j_1) \neq (i_2, j_2)$)．

### 小課題

1. ($9$ 点) $H = 1$．
2. ($10$ 点) $H \times W \leqq 100$．
3. ($5$ 点) $H \times W \leqq 1\,500$．
4. ($56$ 点) $H \times W \leqq 7\,000$．
5. ($20$ 点) 追加の制約はない．

---

### 入力例 1

~~~
1 5
2 4 7 1 5
~~~

### 出力例 1

~~~
10
~~~

JOI 君が訪れたマスの長方形領域として，以下の $10$ 通りがあり得るため，$10$ を出力する．

![](https://img.atcoder.jp/joi2022ho/t5-1.png)

---

### 入力例 2

~~~
3 2
18 10
19 12
17 13
~~~

### 出力例 2

~~~
15
~~~

JOI 君が訪れたマスの長方形領域として，以下の $15$ 通りがあり得るため，$15$ を出力する．

![](https://img.atcoder.jp/joi2022ho/t5-2.png)

この入力例は小課題 $2, 3, 4, 5$ の制約を満たす．

---

### 入力例 3

~~~
3 5
83 47 36 38 40
13 10 26 68 67
15 19 20 70 90
~~~

### 出力例 3

~~~
65
~~~

例えば，以下の長方形領域が考えられる．それ以外のものも含めると全部で $65$ 通りあるため，$65$ を出力する．

![](https://img.atcoder.jp/joi2022ho/t5-3.png)

この入力例は小課題 $2, 3, 4, 5$ の制約を満たす．
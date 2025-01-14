配点： $100$ 点

###
情報オリンピック日本委員会では，台湾大会に向かう選手を応援するために新しい JOI 旗を作成することにした．

JOI 旗は，正方形が縦に $M$ 行，横に $N$ 列並んだ形をしており，各正方形には `J`，`O`，`I` のいずれかの文字が $1$ つずつ書かれている．

![JOI 旗の例](https://img.atcoder.jp/joi2014ho/1-1.jpg)

情報オリンピック日本委員会は JOI 旗とは別に JOI 紋章というものを決めている．JOI 紋章は，正方形が縦に $2$ 行，横に $2$ 列並んだ形をしており，各正方形には `J`，`O`，`I` のいずれかの文字が $1$ つずつ書かれている．

![JOI 紋章の例](https://img.atcoder.jp/joi2014ho/1-2.jpg)

JOI 旗に含まれる JOI 紋章の個数とは，JOI 旗に含まれる縦 $2$ 行，横 $2$ 列の領域のうち，その領域の `J`，`O`，`I` の配置が JOI 紋章と (回転や裏返しをせずに) 一致しているものの個数のことである．条件を満たす縦 $2$ 行，横 $2$ 列の領域同士が重なっていてもそれらを別々に数えるものとする．

情報オリンピック日本委員会は古い JOI 旗と $1$ 枚の白紙を持っている．白紙は JOI 旗を構成する正方形 $1$ 個分の大きさで，`J`，`O`，`I` のうち好きな $1$ 文字を書き込むことができる．情報オリンピック日本委員会は以下のいずれか $1$ つの操作をして，新しい JOI 旗を作成することにした．

- 古い JOI 旗に対して何も操作せず，そのまま新しい JOI 旗とする．白紙は使用しない．
- 白紙に $1$ 文字書き込み，古い JOI 旗のいずれかの正方形に重ねて貼り付けることで古い JOI 旗のうち $1$ 箇所を変更する．変更後の JOI 旗を新しい JOI 旗とする．

情報オリンピック日本委員会は新しい JOI 旗に含まれる JOI 紋章の個数をできるだけ多くしたいと思っている．あなたは新しい JOI 旗に含まれる JOI 紋章の個数の最大値を求めることになった．

### 課題
古い JOI 旗と JOI 紋章の情報が与えられたとき，新しい JOI 旗に含まれる JOI 紋章の個数の最大値を求めるプログラムを作成せよ．

---

### 入力
標準入力から以下のデータを読み込め．

- $1$ 行目には $2$ 個の整数 $M, N$ が空白を区切りとして書かれている．これは JOI 旗が正方形が縦に $M$ 行，横に $N$ 列並んだ形であることを表している．
- 続く $M$ 行の各行には，それぞれ $N$ 文字からなる文字列が書かれている．各文字は `J`，`O`，`I` のいずれかであり，$M$ 行のうち上から $i$ 行目 ($1 \leqq i \leqq M$) に書かれている文字列の左から $j$ 文字目 ($1 \leqq j \leqq N$) は古い JOI 旗の上から $i$ 行目，左から $j$ 列目の正方形に書かれている文字を表す．
- 続く $2$ 行の各行には，それぞれ $2$ 文字からなる文字列が書かれている．各文字は `J`，`O`，`I` のいずれかであり，$2$ 行のうち上から $i$ 行目 ($1 \leqq i \leqq 2$) に書かれている文字列の左から $j$ 文字目 ($1 \leqq j \leqq 2$) は JOI 紋章の上から $i$ 行目，左から $j$ 列目の正方形に書かれている文字を表す．

### 出力
標準出力に，新しい JOI 旗に含まれる JOI 紋章の個数の最大値を表す整数を $1$ 行で出力せよ．

---

### 制限
すべての入力データは以下の条件を満たす．

- $2 \leqq M \leqq 1\,000$．
- $2 \leqq N \leqq 1\,000$．

### 小課題
#### 小課題 1 [30 点]
以下の条件を満たす．

- $M \leqq 50$．
- $N \leqq 50$．

#### 小課題 2 [70 点]
追加の制限はない．

---

### 入力例 1
~~~
3 5
JOIJO
IJOOO
IIJIJ
JO
IJ
~~~

### 出力例 1
~~~
3
~~~

古い JOI 旗と JOI 紋章は問題文中の例の通りである．上から $2$ 行目，左から $4$ 列目の正方形を白紙を用いて `J` に変更すると，次のような形になる．

![JOI 旗の $1$ 箇所を変更した例](https://img.atcoder.jp/joi2014ho/1-3.jpg)

このように変更した後の JOI 旗には次に示す $3$ 箇所に JOI 紋章と同じ配置の領域がある．

![JOI 紋章と同じ配置の領域](https://img.atcoder.jp/joi2014ho/1-4.jpg)

JOI 紋章と同じ配置の領域が $4$ 箇所以上となる新しい JOI 旗は存在しないので，新しい JOI 旗に含まれる JOI 紋章の個数の最大値は $3$ である．

---

### 入力例 2
~~~
2 6
JOJOJO
OJOJOJ
OJ
JO
~~~

### 出力例 2
~~~
2
~~~

白紙を使用しなくても最大値が得られる場合があることに注意せよ．

---

### 入力例 3
~~~
2 2
JI
IJ
JJ
JJ
~~~

### 出力例 3
~~~
0
~~~

この入出力例の場合，考えられるどの新しい JOI 旗においても，JOI 紋章が $1$ つも含まれない．

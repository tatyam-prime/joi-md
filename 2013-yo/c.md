配点： $100$ 点

### 問題
JOI 君はお店の看板を作ることにした．

文字が等間隔に書かれた古い看板が $N$ 枚ある．JOI 君は古い看板からいくつかの文字を消すことで看板を作る．残った文字列がお店の名前になっていて，しかも残った文字が等間隔に並んでいるようにしたい．看板は $1$ 枚の古い看板から作らなければならず，古い看板を切ったりつなげたりしてはならない．

お店の名前と $N$ 枚の古い看板の情報が与えられた時，JOI 君が作ることができる看板の枚数を求めるプログラムを作成せよ．ただし，$1$ 枚の古い看板から作ることができる看板が複数考えられる場合も，作ることができる看板は $1$ 枚であると考える．

---

### 入力
入力は $2 + N$ 行からなる．

$1$ 行目には，整数 $N$ ($1 \leqq N \leqq 100$) が書かれており，古い看板の枚数を表す．

$2$ 行目には，$3$ 文字以上 $25$ 文字以下のアルファベット小文字からなる文字列が書かれており，お店の名前を表す．

続く $N$ 行のうちの $i$ 行目 ($1 \leqq i \leqq N$) には $1$ 文字以上 $100$ 文字以下のアルファベット小文字からなる文字列が書かれており，$i$ 枚目の古い看板に書かれている文字列を表す．

### 出力
JOI 君が作ることができる看板の枚数を表す整数を $1$ 行で出力せよ．

---

### 入力例 1
~~~
4
bar
abracadabra
bear
bar
baraxbara
~~~

### 出力例 1
~~~
3
~~~
お店の名前は `bar` である．

$1$ 枚目の古い看板には文字列 `abracadabra` が書かれている．この古い看板から $2$ 文字目，$6$ 文字目，$10$ 文字目以外を消すことで看板を作ることができる．

$2$ 枚目は，$2$ 文字目を消すと `bar` という文字列を作ることができるが，これは残った文字が等間隔に並んでいない．

$3$ 枚目は，文字を何も消さなくても看板になっている．

$4$ 枚目の古い看板から看板を作る方法は $2$ 通りある．$1$ つの方法は，$1$ 文字目，$2$ 文字目，$3$ 文字目以外を消すことである．もう $1$ つの方法は，$6$ 文字目，$7$ 文字目，$8$ 文字目以外を消すことである．

よって，JOI 君は $1$ 枚目，$3$ 枚目，$4$ 枚目の古い看板から看板を作ることができるので，$3$ を出力する．

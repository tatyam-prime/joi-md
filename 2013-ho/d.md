配点： $100$ 点

###

JOIOI の塔とは，$1$ 人で遊ぶ円盤を使ったゲームである．

このゲームは，`J`，`O`，`I` のいずれかの文字が書かれたいくつかの円盤を用いて行う．円盤は直径が互いに異なり，ゲーム開始時にはこれらの円盤は直径の大きいものから順に下から上に向かって積まれている．あなたは，これらの円盤を用いて，出来るだけ多くのミニ JOIOI の塔を作りたい．ミニ JOIOI の塔とは $3$ 枚の円盤からなり，円盤の直径が小さいものから順に読んで `JOI` もしくは `IOI` と読めるものである．ただし，同じ円盤を $2$ 度以上使うことはできない．

![`JOIOII` からはミニ JOIOI の塔が $2$ つ作れる](https://img.atcoder.jp/joi2013ho/64a5a5b84e87215b70a1221fa86fddab.png)

### 課題
用意された円盤に書かれた文字がそれぞれ円盤の直径が小さいものから順に長さ $N$ の文字列 $S$ として与えられる．これらの円盤を使って作ることのできるミニ JOIOI の塔の個数の最大値を求めるプログラムを作成せよ．

### 制限

|||
|---|---|
|$1 \leqq N \leqq 1\,000\,000$&emsp;|文字列 $S$の長さ|

---

### 入力
標準入力から以下のデータを読み込め．

- 1 行目には整数 $N$ が書かれている．$N$ は文字列 $S$ の長さを表す．
- 2 行目には文字列 $S$ が書かれている．

### 出力
標準出力に，作ることのできるミニ JOIOI の塔の数の最大値を表す整数を $1$ 行で出力せよ．

### 採点基準
採点用データのうち，配点の $10$ %分については，$N \leqq 15$ を満たす．

採点用データのうち，配点の $30$ %分については，$N \leqq 50$ を満たす．

採点用データのうち，配点の $50$ %分については，$N \leqq 3\,000$ を満たす．

---

### 入力例 1
~~~
6
JOIIOI
~~~

### 出力例 1
~~~
2
~~~

`JOIIOI` は `JOI` および `IOI` をそれぞれ $1$ つずつ部分列として含んでおり，作ることのできるミニ JOIOI の塔は $2$ つである．

---

### 入力例 2
~~~
5
JOIOI
~~~

### 出力例 2
~~~
1
~~~

部分列として `JOI` および  `IOI` を含んでいるが，文字を $2$ 度以上使うことはできないため同時に取り出すことはできない．

---

### 入力例 3
~~~
6
JOIOII
~~~

### 出力例 3
~~~
2
~~~

この入出力例は問題文中の例に対応している．

---

### 入力例 4
~~~
15
JJOIIOOJOJIOIIO
~~~

### 出力例 4
~~~
4
~~~
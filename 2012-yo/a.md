配点： $100$ 点

### 問題
JOI パスタ店では，ランチのおすすめパスタと搾りたてジュースのセットメニューが好評である．このセットメニューを注文するときは，その日の $3$ 種類のパスタと $2$ 種類のジュースから $1$ つずつ選ぶ．パスタとジュースの値段の合計から $50$ 円を引いた金額が代金となる．

ある日のパスタとジュースの値段が与えられたとき，その日のセットメニューの代金の最小値を求めるプログラムを作成せよ．

---

### 入力
入力は $5$ 行からなり，$1$ 行に $1$ つずつ正の整数が書かれている．

$1$ 行目の整数は $1$ つ目のパスタの値段である．  
$2$ 行目の整数は $2$ つ目のパスタの値段である．  
$3$ 行目の整数は $3$ つ目のパスタの値段である．  
$4$ 行目の整数は $1$ つ目のジュースの値段である．  
$5$ 行目の整数は $2$ つ目のジュースの値段である．  

ただし，与えられる入力データにおいては全てのパスタとジュースの値段は $100$ 円以上 $2\,000$ 円以下であることが保証されている．

### 出力
その日のセットメニューの代金の最小値を $1$ 行で出力せよ．

---

### 入力例 1
~~~
800
700
900
198
330 
~~~

### 出力例 1
~~~
848
~~~

入出力例 $1$ では，$2$ つ目のパスタと $1$ つ目のジュースを組み合わせた場合の $700 + 198 - 50 = 848$ がその日のセットメニューの代金の最小値である．

---

### 入力例 2
~~~
1999
1999
100
189
100
~~~

### 出力例 2
~~~
150
~~~
入出力例 $2$ では，$3$ つ目のパスタと $2$ つ目のジュースを組み合わせた場合の $100 + 100 - 50 = 150$ がその日のセットメニューの代金の最小値である．

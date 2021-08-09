配点： $100$ 点

### 問題
情報オリンピック日本委員会では，今年の日本情報オリンピック (JOI) を宣伝するために，JOI のロゴをモチーフにした旗を作ることになった．旗は「良い旗」でなければならない．「良い旗」とは，アルファベットの J，O，I のいずれかの文字を，縦 $M$ 行，横 $N$ 列の長方形状に並べたもので，J，O，I が以下の図のように (すなわち，J の右隣に O が，その J の下隣に I が) 並んでいる箇所が旗の少なくとも $1$ か所にあるものである．

![](https://img.atcoder.jp/joi2011yo/2011-yo-t6-fig01.png)

以下の図に，「良い旗」の例を $2$ つ示す．

![](https://img.atcoder.jp/joi2011yo/2011-yo-t6-fig02.png)

以下の図に，「良い旗」ではない例を $2$ つ示す．

![](https://img.atcoder.jp/joi2011yo/2011-yo-t6-fig03.png)

いま $M, N$ の値，および旗の一部の場所について J，O，I のどの文字にするかが決まっており，入力としてその情報が与えられる．考えられる「良い旗」は何通りあるかを計算し，その数を $100\,000 \ (= 10^5)$ で割った余りを出力するプログラムを作成せよ．

### 入力
入力は $1 + M$ 行からなる．

$1$ 行目には旗の大きさを表す $2$ つの整数 $M, N$ ($2 \leqq M \leqq 20$，$2 \leqq N \leqq 20$) が空白で区切られて書かれている．

$1 + i$ 行目 ($1 \leqq i \leqq M$) には，$N$ 文字からなる文字列が書かれている．各文字は J，O，I，? のいずれかであり，$j$ 文字目 ($1 \leqq j \leqq N$) が J，O，I のいずれかである場合は $i$ 行 $j$ 列の場所の文字がそれぞれ J，O，I に決まっていること，? である場合はまだ決まっていないことを表す．

### 出力
考えられる「良い旗」の個数を $100\,000 \ (= 10^5)$ で割った余りを $1$ 行で出力せよ．

---

### 入力例 1
~~~
2 3
??O
IIJ
~~~

### 出力例 1
~~~
4
~~~

入力例 $1$ においては，以下の図の $4$ 通りの「良い旗」が考えられる．

![](https://img.atcoder.jp/joi2011yo/2011-yo-t6-fig04.png)

---

### 入力例 2
~~~
2 2
??
??
~~~

### 出力例 2
~~~
3
~~~

---

### 入力例 3
~~~
3 3
??I
???
O?J
~~~

### 出力例 3
~~~
53
~~~

---

### 入力例 4
~~~
5 4
JOI?
????
????
????
?JOI
~~~

### 出力例 4
~~~
28218
~~~

入力例 $4$ においては，「良い旗」は $2\,428\,218$ 通り考えられるので，それを $100\,000 \ (= 10^5)$ で割った余りである $28\,218$ を出力する．
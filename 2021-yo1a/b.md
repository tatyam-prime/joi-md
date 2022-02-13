配点： $100$ 点

### 問題文
長さ $N$ の文字列 $S$ が与えられる．$S$ の各文字は `J`，`O`，`I` のいずれかである．

あなたは $S$ の文字を並び替えて次の条件を満たすようにしたい．

- すべての文字 `J` と文字 `O` の組について `J` が `O` よりも前にある．
- すべての文字 `O` と文字 `I` の組について `O` が `I` よりも前にある．
- すべての文字 `J` と文字 `I` の組について `J` が `I` よりも前にある．

文字列 $S$ が与えられたとき，上の条件を満たすように $S$ の文字を並び替えた文字列を出力するプログラムを作成せよ．

### 制約
- $1 \leqq N \leqq 100$．
- $S$ は長さ $N$ の文字列である．
- $S$ の各文字は `J`，`O`，`I` のいずれかである．

---

### 入力
入力は以下の形式で標準入力から与えられる．

~~~
$N$
$S$
~~~

### 出力
条件を満たすように $S$ の文字を並び替えた文字列を出力せよ．

---

### 入力例 1
~~~
6
JIOIJO
~~~

### 出力例 1
~~~
JJOOII
~~~

`JIOIJO` の並べ替えである `JJOOII` は条件を満たす．

---

### 入力例 2
~~~
4
OOOI
~~~

### 出力例 2
~~~
OOOI
~~~

与えられた文字列がすでに条件を満たしているかもしれない．`J`，`O`，`I` がすべて含まれているとは限らない．

---

### 入力例 3
~~~
10
OIJJJIOIOI
~~~

### 出力例 3
~~~
JJJOOOIIII
~~~
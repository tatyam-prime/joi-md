配点： ${score}$ 点

### 問題文
A 地点から B 地点に移動するのに $X$ 時間，B 地点から C 地点に移動するのに $Y$ 時間かかる．

A 地点から B 地点を経由して C 地点に移動するとき，$Z$ 時間 $30$ 分以内に移動することができるか判定せよ．

### 制約
- $1 \leqq X \leqq 100$．
- $1 \leqq Y \leqq 100$．
- $1 \leqq Z \leqq 100$．
- 入力される値はすべて整数である．

---

### 入力
入力は以下の形式で標準入力から与えられる．

~~~
$X$
$Y$
$Z$
~~~

### 出力
$Z$ 時間 $30$ 分以内に移動することができるならば $1$ を，そうでない場合は $0$ を出力せよ．

---

### 入力例 1
~~~
2
3
4
~~~

### 出力例 1
~~~
2
3
4
~~~

A 地点から B 地点に移動するのに $2$ 時間，B 地点から C 地点に移動するのに $3$ 時間かかる．よって，A 地点から B 地点を経由して C 地点に移動するのに $5$ 時間かかる．

$4$ 時間 $30$ 分以内に移動することができないため，$0$ を出力する．

---

### 入力例 2
~~~
3
4
10
~~~

### 出力例 2
~~~
1
~~~

A 地点から B 地点を経由して C 地点に移動するのに $7$ 時間かかる．

$10$ 時間 $30$ 分以内に移動することができるため，$1$ を出力する．
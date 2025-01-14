配点： $100$ 点

###

IOI 鉄道は $1$ 本の鉄道路線を運営している．IOI 鉄道線には一直線上に並んだ $N$ 個の駅があり，$1$ から $N$ までの番号が付けられている．各 $i$ ($1 \leqq i \leqq N - 1$) に対して，駅 $i$ と駅 $i + 1$ の間は線路で結ばれている．

IOI 鉄道線には $M$ 系統の運行系統があり，$1$ から $M$ までの番号が付けられている．系統 $j$ ($1 \leqq j \leqq M$) の列車の始発駅は駅 $A_j$ であり，終着駅は駅 $B_j$ である．列車は各駅に停車する．すなわち，系統 $j$ の列車は，$A_j < B_j$ のとき駅 $A_j$，駅 $A_j + 1$，$\dots$，駅 $B_j$ の順に停車し，$A_j > B_j$ のとき駅 $A_j$，駅 $A_j - 1$，$\dots$，駅 $B_j$ の順に停車する．

旅人の JOI くんは，$Q$ 個の旅行計画を考えている．$k$ 番目 ($1 \leqq k \leqq Q$) の計画は，駅 $S_k$ から出発し，駅 $T_k$ にいくつかの列車を乗り継いで到着するというものである．

しかしながら，JOI くんは長旅で疲れているので，空いている列車に乗車し，着席したい．そのため，JOI くんがある列車に乗車するのは，その列車の始発駅から（始発駅を含めて）$K$ 駅以内の駅からのみとした．すなわち，JOI くんが系統 $j$ の列車に乗車するとき，$A_j < B_j$ であれば駅 $A_j$，駅 $A_j + 1$，$\dots$，駅 $\min\\{A_j + K - 1, B_j - 1\\}$ から乗車でき，$A_j > B_j$ であれば駅 $A_j$，駅 $A_j - 1$，$\dots$，駅 $\max\\{A_j - K + 1, B_j + 1\\}$ から乗車できる．JOI くんは，列車に乗車した駅の次の駅からその列車の終着駅までの各駅のうちいずれかの駅で下車する．

JOI くんはこの条件のもと，なるべく乗り継ぎの回数を少なくしたい．

IOI 鉄道線の情報と JOI くんの計画が与えられたとき，それぞれの計画について，JOI くんが計画を達成するために乗車する列車の数の最小値を求めるプログラムを作成せよ．

---

### 入力

入力は以下の形式で標準入力から与えられる．入力される値はすべて整数である．

~~~
$N$ $K$
$M$
$A_1$ $B_1$
$A_2$ $B_2$
$\vdots$
$A_M$ $B_M$
$Q$
$S_1$ $T_1$
$S_2$ $T_2$
$\vdots$
$S_Q$ $T_Q$
~~~

### 出力

標準出力に $Q$ 行で出力せよ．$k$ 行目 ($1 \leqq k \leqq Q$) には，JOI くんが $k$ 番目の計画を達成するために乗車する列車の数の最小値を出力せよ．ただし，計画が達成不可能な場合は，`-1` を出力せよ．

---

### 制約

- $2 \leqq N \leqq 100\,000$．
- $1 \leqq K \leqq N - 1$．
- $1 \leqq M \leqq 200\,000$．
- $1 \leqq A_j \leqq N$ ($1 \leqq j \leqq M$)．
- $1 \leqq B_j \leqq N$ ($1 \leqq j \leqq M$)．
- $A_j \neq B_j$ ($1 \leqq j \leqq M$)．
- $(A_j, B_j) \neq (A_k, B_k)$ ($1 \leqq j < k \leqq M$)．
- $1 \leqq Q \leqq 50\,000$．
- $1 \leqq S_k \leqq N$ ($1 \leqq k \leqq Q$)．
- $1 \leqq T_k \leqq N$ ($1 \leqq k \leqq Q$)．
- $S_k \neq T_k$ ($1 \leqq k \leqq Q$)．
- $(S_k, T_k) \neq (S_l, T_l)$ ($1 \leqq k < l \leqq Q$)．

### 小課題

1. ($8$ 点) $N \leqq 300$，$M \leqq 300$，$Q \leqq 300$．
2. ($8$ 点) $N \leqq 2\,000$，$M \leqq 2\,000$，$Q \leqq 2\,000$．
3. ($11$ 点) $Q = 1$．
4. ($25$ 点) $K = N - 1$．
5. ($35$ 点) $A_j < B_j$ ($1 \leqq j \leqq M$)，$S_k < T_k$ ($1\leqq k \leqq Q$)．
6. ($13$ 点) 追加の制約はない．

---

### 入力例 1

~~~
5 2
2
5 1
3 5
3
5 3
3 2
2 1
~~~

### 出力例 1

~~~
1
2
-1
~~~

$1$ 番目の計画は，駅 $5$ から出発し，駅 $3$ に到着するというものである．例えば，駅 $5$ から系統 $1$ の列車に乗車し，駅 $3$ で下車することで計画を達成できる．このとき乗車する列車の数は $1$ 本である．$1$ 本未満の列車に乗車することで計画を達成することは不可能であるため，$1$ を $1$ 行目に出力する．

$2$ 番目の計画は，駅 $3$ から出発し，駅 $2$ に到着するというものである．例えば，駅 $3$ から系統 $2$ の列車に乗車し，駅 $4$ で下車し，そして，駅 $4$ から系統 $1$ の列車に乗車し，駅 $2$ で下車することで計画を達成できる．このとき乗車する列車の数は $2$ 本である．$2$ 本未満の列車に乗車することで計画を達成することは不可能であるため，$2$ を $2$ 行目に出力する．駅 $3$ から系統 $1$ の列車に乗車することはできないことに注意すること．

$3$ 番目の計画は，駅 $2$ から出発し，駅 $1$ に到着するというものである．この計画は達成できないため，`-1` を $3$ 行目に出力する．

この入力例は小課題 $1, 2, 6$ の制約を満たす．


---

### 入力例 2

~~~
6 3
2
1 6
5 1
4
5 1
6 3
3 6
2 1
~~~

### 出力例 2

~~~
1
-1
1
2
~~~

この入力例は小課題 $1, 2, 6$ の制約を満たす．

---

### 入力例 3

~~~
6 5
4
3 1
2 4
5 3
4 6
5
1 5
3 2
2 6
6 3
5 4
~~~

### 出力例 3

~~~
-1
1
2
-1
1
~~~

この入力例は小課題 $1, 2, 4, 6$ の制約を満たす．

---

### 入力例 4

~~~
12 1
5
1 7
10 12
3 5
8 10
5 9
7
2 11
5 8
3 12
4 6
1 9
9 10
1 4
~~~

### 出力例 4

~~~
-1
1
4
-1
2
-1
1	
~~~

この入力例は小課題 $1, 2, 5, 6$ の制約を満たす．

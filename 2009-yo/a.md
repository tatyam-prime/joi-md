配点： $100$ 点

### 問題
JOI 商事では社員の在社時間をタイムカードで管理している．社員は，出社すると専用の装置を使ってタイムカードに出社時刻を刻印する．勤務を終え退社するときにも，タイムカードに退社時刻を刻印する．時刻は $24$ 時間制で扱われる．

防犯上の理由から，社員の出社時刻は $7$ 時以降である．また，全ての社員は $23$ 時より前に退社する．社員の退社時刻は常に出社時刻より後である．

入力として JOI 商事の $3$ 人の社員 A さん，B さん，C さんの出社時刻と退社時刻が与えられたとき，それぞれの社員の在社時間を計算するプログラムを作成せよ．

---

### 入力
入力は $3$ 行からなる．$1$ 行目には A さんの出社時刻と退社時刻，$2$ 行目には B さんの出社時刻と退社時刻，$3$ 行目には C さんの出社時刻と退社時刻がそれぞれ空白で区切られ書かれている．

時刻はそれぞれ空白で区切られた3つの整数で書かれている．3つの整数 $h, m, s$ は $h$ 時 $m$ 分 $s$ 秒を表す．$7 \leqq h \leqq 22$，$0 \leqq m \leqq 59$，$0 \leqq s \leqq 59$ である．

### 出力
$1$ 行目に A さんの在社時間，$2$ 行目に B さんの在社時間，$3$ 行目に C さんの在社時間を出力せよ．

出力する在社時間が $h$ 時間 $m$ 分 $s$ 秒の場合，$h, m, s$ の順に空白で区切って出力せよ．

---

### 入力例 1
~~~
9 0 0 18 0 0
9 0 1 18 0 0
12 14 52 12 15 30
~~~

### 出力例 1
~~~
9 0 0
8 59 59
0 0 38
~~~
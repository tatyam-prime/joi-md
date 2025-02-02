配点： $100$ 点

### 問題
あなたはある機械の製造工場で品質管理の責任者をしている．この機械には，部品として電源とモーターとケーブルが必要である．製造工場には電源が $a$ 個，モーターが $b$ 個，ケーブルが $c$ 個あり，それぞれ $1$ から $a$ まで，$a + 1$ から $a + b$ まで，$a + b + 1$ から $a + b + c$ までの番号が付いている．困ったことに，部品の中に故障しているものがあるかもしれない．工場ではどの部品が故障していてどの部品が正常であるかを知りたい．

そこで，工場では次の方法で部品を検査した．電源とモーターとケーブルを $1$ つずつ持ってきてつなぎ，動作させてみる．このとき，$3$ つの部品がすべて正常であるときは正しく動作して「合格」とわかる．$3$ つの中に故障している部品が $1$ つでも入っているときは正しく動作しないので「不合格」とわかる．（工場で作っている機械はとても精密なので，故障した部品がまざっているのに偶然正しく動作してしまうなどということは起きないのだ．）

あなたには検査結果のリストが渡される．検査結果のリストの各行には，検査に使った電源とモーターとケーブルの番号と，検査が合格だったか不合格だったかが書かれている．

検査結果のリストが与えられたとき，すべての部品を，検査結果から確実に故障しているとわかる部品と，確実に正常とわかる部品と，検査結果からは故障しているとも正常であるとも決まらない部品に分類するプログラムを作成せよ．

---

### 入力
入力の形式は以下の通りである．

$1$ 行目には $3$ 個の整数が空白区切りで書かれており，順に電源の個数 $a$， モーターの個数 $b$， ケーブルの個数 $c$ を表す．  
$2$ 行目には $1$ 個の整数が書かれており，検査結果のリストに含まれる検査の回数 $N$ が書かれている．  
続く $N$ 行は検査結果のリストを表す．各行には，$4$ 個の整数 $i, j, k, r$ が $1$ つの空白を区切りとして書かれており，電源 $i$ とモーター $j$ とケーブル $k$ をつないで検査した結果が，「合格」($r = 1$ のとき) か「不合格」($r = 0$ のとき) だったことを表す.

$a, b, c, N$ は $1 \leqq a, b, c \leqq 100$，$1 \leqq N \leqq 1000$ を満たす.

### 出力
出力は以下の通りである. 出力は $a + b + c$ 行からなる.

$i$ 行目 ($1 \leqq i \leqq a + b + c$) ：

検査結果から部品 $i$ が故障しているとわかる場合は $0$ を出力する．  
検査結果から部品 $i$ が正常とわかる場合は $1$ を出力する．  
検査結果から部品 $i$ が故障しているか正常であるかが決まらない場合は $2$ を出力する．

---

### 入力例 1
~~~
2 2 2
4
2 4 5 0
2 3 6 0
1 4 5 0
2 3 5 1
~~~

### 出力例 1
~~~
2
1
1
0
1
0
~~~

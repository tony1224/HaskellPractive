### 概要
- 要素をカンマ区切りで並べて角括弧で括る
```
ghci> let lostNumebres = [4,5,6,7,8]
ghci> lostNumbers
[4,5,6,7,8]
```

### 連結
```
[1,2,3] ++ [4,5,6]
[1,2,3,4,5,6]

"hello" ++ " " ++ "world!"
"hello world!"
```

#### 大量のリストを扱う場合のTips
- 先頭に追加: コロン
  - 文字はシングルクォーテーション
```
'A':" SAMLL CAT"
"A SMALL CAT"
```

### 要素へのアクセス
- <b><span style="color: orange; ">!!演算子 </b>を使う
```
"Steve Buscemi" !! 6
"B"
```
- 先頭取得: <b><span style="color: orange; ">head</b> [1,2,3] -> 1
- 末尾取得: <b><span style="color: orange; ">last</b> [1,2,3] -> 3
- 要素数: <b><span style="color: orange; ">length</b> [1,2,3] -> 3
- 逆にする: <b><span style="color: orange; ">reverse</b> [1,2,3] -> [3,2,1]
- 指定要素分取得: <b><span style="color: orange; ">take</b> 2 -> [1,2]
- 空判定: <b><span style="color: orange; ">null []</b> -> True

### 比較
```
[3,2,1] > [2,1,0]
True
```

### 列挙(レンジ)
- レンジでチン！より
- 1から20: <b><span style="color: orange; ">[1..20]</b>
  - 文字も同様
- ステップを指定することも可
  - 2の倍数のみ
```
[2, 4..20]
-> [2,4,6,8,10...20]
```
  - ただステップ付きレンジはいうほど賢くない
- レンジを使った無限リスト
  - ex) 13の倍数を24個からなるリスト
```
[13,26..24*13]
```  
- 以下のように書いた方が良い
<b><span style="color: orange; ">take 24 [13,26..]</b>
- Haskellは<b><span style="color: orange; ">遅延評価</b>
  - すぐに無限リスト全体を評価しない
  - 中の値が必要とされるまで待つ

### めちゃくちゃ長いリストを生成する関数
- 途中で区切るのを忘れずに
- cycle
```
take 10 (cycle [1,2,3])
-> [1,2,3,1,2,3,1,2,3,1]
```
- repeatを使う形が良さそう
```
take 10 (repeat 5)
-> [5,5,5,5,5,5,5,5,5,5]
```
- 単一の値のリスト生成: <b><span style="color: orange; ">replicate</b> 3 10 -> [10, 10, 10]

### リスト内包表記
```
take 10 [2,4..]
// リスト内包表記
[x*2 | x <- [1..10]]
```
- xに[1..10]の値を取得
- |より左は出力部分
- こっちらのがtakeよりも書き方面倒だが、より複雑なことをやりたくなったらこっちのが凄い
  - 述語を複数かけるので拡張しやすい

#### 条件(述語)を追加する
- 上のもので結果が12以上
```
[x*2 | x <- [1..10], x*2 >= 12]
```
- カンマ区切りでたくさん条件付けれる
- 複数のリストから値を取得することも可能
```
[x+y | x <- [1,2,3], y <- [10, 100, 1000]]
```
- 流れ的には<b><span style="color: orange; ">xに1が入ったらyのリスト値全部を見に行く</b>

- 奇数を判定: <b><span style="color: orange; ">odd関数</b>
  - Boom.hsに記述
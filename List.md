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



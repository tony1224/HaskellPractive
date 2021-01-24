### Swiftとほぼ同じ
- 値は2つ以上セットできる
- 2次元ベクトルを扱う方法で便利
  - 座標
- サイズが2つのタプルを<b><span style="color: orange; ">ペア</b>と呼ぶ  
- Toupleの区別をHaskellはできる
  - タプルのリストを作る時に型が異なるものが含まれてることを検知できる
- あらかじめ中に入る要素がわかっている時にのみ使える
  - <b>要素を追加する処理は書けないので注意</b>

### ペアを操作するための関数
- 1つ目の要素を返す<b><span style="color: orange; ">fst</b> ("Wow", False) -> "Wow"
- 2つ目の要素を返す<b><span style="color: orange; ">snd</b> ("Wow", False) -> False
- ペアを作る<b><span style="color: orange; ">zip</b> [1,2] [5,5] -> [(1,5), (2,5)]
  - リストの長さが異なると？ -> 必要な分だけ。残りは無視 
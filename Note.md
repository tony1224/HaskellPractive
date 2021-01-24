## 注意
- .hsファイルは毎回 :l hoge.hsを打って更新する必要あり
- letから始まる変数の処理ではファイル内でletを書いてはいけない

## 環境構築
- [清さんのブログ](https://note.com/tionlow/n/n11f9a49baf84)を見ながら
- Haskell Platformではなく<b><span style="color: orange; ">Stack</b>を利用

## 1/12
- 最初の勉強会

### Hello world!実行方法
```
$ stack exec ghci  // stackのghciプログラム起動
Prelude > "Hello world!"
"Hello world!"
```
- stack execはワンライナーで書きたい用
  - stack ghciよりもおすすめらしい

### scriptファイル実行方法
```
$ :l hoge.hs
```
- 実行というか更新も兼ねる。ファイルは保存+これをしないと反映されない
- doubleMe, doubleUs関数を使った計算方法

### 輪読していく
- 違った考え方を求められる
- #haskellに困ったら投げれば良い？
- 型クラスの存在
  - Genericsとも違う
- 1.5のインタプリタまで  
- 真理値は大文字(True, False)
- 単なる計算は中置関数
  - ただ大半は前置関数
    - ex) succ
- 1.3 リスト入門

## 1/19
- 体調不良のため欠席
- 2.4 型クラス初級講座までやった
# appi-rep-cover

## About this repository

このリポジトリは，物理情報工学実験のレポート表紙テンプレートを，非公式にTeX/LaTeXに移植したスタイルファイル(.styファイル)を含みます．

ユーザーは，.styファイルをダウンロードして適切にインストールすることで，通常のパッケージと同様に`\usepackage{}`して当パッケージを利用することができます．

## インストール方法

1. `appi-rep-cover.sty`を自身のパソコンにダウンロード
2. ダウンロードした`appi-rep-cover.sty`を`~/texmf/tex/latex/appi-rep-cover`に移動
3. `mktexlsr`コマンドを実行(管理者権限が必要と言われたら`sudo mktexlsr`で実行)
4. `kpsewhich appi-rep-cover.sty`を実行して，texliveが`appi-repcover.sty`を認識していることを確認

### 実行例
```bash
$ mkdir -p ~/texmf/tex/latex/appi-rep-cover
$ cd ~/texmf/tex/latex/appi-rep-cover
$ wget https://raw.githubusercontent.com/YuH25JP/appi-rep-cover/main/appi-rep-cover.sty
$ mktexlsr
$ kpsewhich appi-rep-cover.sty
```

最後の`kpsewhich`で
```
/home/ユーザー名/texmf/tex/latex/appi-rep-cover/appi-rep-cover.sty
```
みたいな出力が出たら成功です．

### ちなみに...

.styファイルを置くことのできる場所はほかにもあります．下記のリンクを参照してください．

[LaTeX入門/各種パッケージの利用 - TeX Wiki](https://texwiki.texjp.org/?LaTeX%E5%85%A5%E9%96%80%2F%E5%90%84%E7%A8%AE%E3%83%91%E3%83%83%E3%82%B1%E3%83%BC%E3%82%B8%E3%81%AE%E5%88%A9%E7%94%A8#n18c984a)

## 使い方

1. プリアンブルに`\usepackage{appi-rep-cover}`と書く
2. プリアンブルに以下の内容を記述する({}の中に適当な内容を記述する)
```latex
\title{物理情報工学実験CD報告書} % タイトル
\id{} % 整理番号
\exptheme{} % テーマ名
\teacher{} % 担当教員名
\name{} % 実験者氏名
\coexperimenters{} % 共同実験者氏名
\youbikumi{} % 曜日組
\jikkenbi{} % 実験日
\jikkenkai{} % 実験回
```
3. `\begin{document}`した後に，`\maketitle`と書く
4. あとは普通にコンパイル

なお，テンプレートの提出日の欄には，コンパイル日が自動的に入ります．もしもコンパイル日でない日付を表示したい場合は，プリアンブルに以下の内容を追記してください．
```latex
\date{入れたい日付}
```

また，表紙のページ番号は振られず，次のページから1ページが始まります．

## 注意事項

当スタイルファイルは，公式に提供されているテンプレートを正確に再現したものではありません．

したがって，罫線の長さ，高さや位置，文字の大きさなど，すべて適当です．

ご利用の際はこのことをご理解ください．

当スタイルファイルから生成した表紙を使って提出したレポートに関して，利用者に不利益が生じた場合，当スタイルファイルの作成者はその一切の責任を負いません．

# vscode　で　Ruby on Railsをwindows7のローカル環境で構築？
## bundlerを使って、railsをインストールする流れ、手順は若干前後している可能性大

```
bundlerとは？　アプリ
複数PCで必要なgemパッケージをインストールするしくみを提供してくれるおかげでチームで作業する時の相互のヴァージョンの違いを補完してくれる。
プロジェクト毎に Bundler で管理する。
Bundlerを利用することで，アプリケーション単位でgemを管理することができます。即ち、システム側にはgemはインストールせず，アプリケーションディレクトリにインストールするという方法です。この方法だとファイルの冗長性が増すので，サイズも無駄にとることになりますが，システムに依存しませんので，アプリケーション内でのgemのバージョンの整合性の問題は無くなります。

bundleとは？　コマンドプロンプトやvscodeで使うときの名前
・gemの強化版（パッケージマネージャ、依存性管理ツール）
・依存性とは？
    「A」というライブラリを使うために「B」「C」というライブラリも必要
    依存性管理ツールを使うと、Aをインストールすると、B・Cも同時にインストールしてくれる
・gemではbundleだけをインストールして、あとは、bundlerを使うことが多い
・複数PCで必要なgemパッケージをインストールするしくみを提供してくれるおかげでチームで作業する時の相互のヴァージョンの違いを補完してくれる

gemとの違いは？
・gemは、コンピュータ全体にgemをインストールしてしまう → 影響範囲が広い
・bundlerは、特定のフォルダにgemをインストールするので、別のrailsプロジェクトに影響をあたえない
・基本的に、gemコマンドでインストールするのはBundlerのみで、その他のgemパッケージは、Bundler経由でインストールする

```
## bundlerを使う

```
GUIとは
    GUIとはグラフィカルユーザーインターフェイスの略で、 今あなたが見ているブラウザ(インターネットエクスプローラ、edge、Google Chrome、Firefox)や、エクセル、ワードのようなアプリケーション(ソフト)の表示形態です。 一般的にソフトと言われるものはこの形式が多いですが、後述するCUIに比べ開発が難しくなる傾向にあります。 これによるアプリケーションはウィンドウアプリケーション、フォームアプリケーションの様に呼ばれることもあります。

SQLite
    コマンドラインツールを使ってデータベースを作成したりデータの取得といったことが可能です。

# https://forest.watch.impress.co.jp/library/software/sqldbbrowser/
# 上のリンク先の、下のデータベースをダウンロード
DB Browser for SQLite（64bit版）


# cd 対象のフォルダ（事前に作っておく）
cd Documents/Projects
mkdir 20180920
cd 20180920

# bundleでPJを作成する（Gemfileを作成する）
bundle init

# Gemfileに書かれた内容をもとにinstallする

bundle install 　　　　　　 #(遅い)
bundle install --jobs=4　　#(爆速)
```

# railsプロジェクトを作成する
## vscode　というエディタを使用
```
# bundle で install した gem を使うときには、「bundle exec」 を付ける必要がある
bundle exec rails new .

# デフォルトの DataBase を MySQL にする
bundle exec rails new . -d mysql

# railsサーバーを立ち上げる
bundle exec rails server
bundle exec rails s　　　# 省略可能
```

## ブラウザに localhost:3000 を入力するとruby on rails　のウェルカムが見れる
## とりあえずここまでできればオーケー？

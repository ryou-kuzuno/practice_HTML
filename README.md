# practice_HTML
## Git　の使い方
```
# リポジトリの初期化
git init

# 変更したファイルをgitの管理下に置く
git add -A

# 変更をコミットする
git commit -m"コミットメッセージ"

# 現在のGIT状態を確認する
git status 

# githubと同期する（変更を送る）
git push origin master

```
## メモ
### gitのブランチ
ブランチ ... 枝/枝別れ

git（github）では、
- masterブランチ
- featureブランチ（開発機能をつくるブランチ）
を使い分ける。

通常は、featureブランチで開発を行って、pull-requestをしてコードを変更しておく。
これを、github workflowという。

### pull-requestの作り方
```
# 最新のコードと開発マシンのコードを同期する
git branch master
git pull

# 新しいブランチをつくる
git checkout -b"new-branch"

# いろいろと変更する。変更したら、add → commitの流れ

# ある程度変更が溜まったら、pushする
git push origin new-branch（作成したブランチ名と同じ名前にする）

# githubに移動して、pull-requestを作成する
# github上でコードを確認。マージする

# 開発マシンでブランチをmasterに戻し、変更を取り込む
git checkout master
git pull

# 以下繰り返し
```





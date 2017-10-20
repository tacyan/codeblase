# railsやelixirのコマンドを書いて行きます。

```
mix new リポジトリ名

cd リポジトリ名

例
.git/config

[remote "origin"]
	url = https://github.com/ユーザー名/リポジトリ名
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master

mixコマンド or railsコマンドで初期化した際に、
始めにgithubにリポジトリを作成して、ファイルを
githubが管理しているリポジトリに移動して
下記のコマンドを使用して、管理出来るようにする。

mv リポジトリ名/* .
```

# Ruby on Rails最終課題

## 目次

## 概要

| 画面名                 | パス                      |      | コントローラー |
| ---------------------- | ------------------------- | ---- | -------------- |
| ユーザー登録           | /users/sign_up            |      |                |
| サインイン             | /users/sign_in            |      |                |
| プロファイル           | /users/profiles           |      |                |
| ユーザーの商品         | /users/products           |      |                |
| ユーザーの商品詳細     | /users/products/{id}      |      |                |
| ユーザーの商品詳細編集 | /users/products/{id}/edit |      |                |
| 出品                   | /users/products/new       |      |                |
| お気に入り商品         | /users/likes              |      |                |
| プロフィール編集       | /users/profiles/edit      |      |                |
| 商品一覧               | /                         | root | market#top     |
| 商品詳細               | /markets/{id}             |      |                |
| 商品購入確認           | /markets/{id}/payment     |      |                |



### コントローラー

* Markets
* Users



### ルーティング

パスを参考にして作成する。

表示機能はGET、データ登録・更新はPOSTメソッドで行う。



## DB作成

### phpmyAdminを起動

「10-1 phpMyAdminのインストール」参照 

```shell
$ mysql-ctl start
$ phpmyadmin-ctl install
```

データベース名は：unokun_market



参考)phpMyAdminの終了

phpMyAdminとRuby on Railsは共存しないため、使い終わったらphpMyAdminを終了しておく。

```shell
$ sudo service apache status ← これは実行しているかどうかの確認コマンドで必須ではありません。
$ sudo service apache stop
```



## プロジェクト作成

プロジェクト名：unokun_market

「1-5 Railsプロジェクトを作成」を参照

```shell
$ rails new unokun_market --database=mysql
```



タイムゾーンの設定も行います。

database.ymlを編集し作成したDBを設定します。



## Top画面作成

Top画面は、商品一覧画面です。これを作成するにあたり以下の手順が必要となります。

Marketsコントローラー作成

Routing設定

共通レイアウト作成

Topページの作成



### Marketsコントローラー作成

```shell
$ rails generate controller markets top 
```



### Routing設定

コントローラー作成時にはgetメソッドのルーティングになっているので、ここをrootに変更します。

修正前

```shell
get 'markets/top'
```

修正後

```shell
root 'markets#top'
```

ここまでで一度Railsを起動してみます。

```shell
$ rails s -b $IP -p $PORT
```



Usersコントローラーを作成

```shell
$ rails generate controller user
```



### 共通レイアウト作成

画像投稿サイトを参考にして共通レイアウトを作成します。
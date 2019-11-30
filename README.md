# Ruby on Railsレッスンメモ
## 事前知識

### Webアプリケーションとは

Ruby on Railsを使って開発しようとしてWebアプリケーションとは、ブラウザを使って操作するWebベースアプリケーションです。ユーザーの操作をHTTPプロトコルという規約に基づいてリクエストし、HTMLをレスポンスとして返します。ブラウザは返却されたHTMLを表示します。

* [Webアプリケーションとは](https://www.sejuku.net/blog/1046)
* [Webアプリケーションの概要](http://si.comp.ae.keio.ac.jp/web_app_dev_material/simple/about_webapp/index.html)
* [HTTPプロトコル](http://si.comp.ae.keio.ac.jp/web_app_dev_material/simple/about_webapp/index.html)
* [RubyとRailsの学習ガイド2019年版](https://magazine.rubyist.net/articles/0059/0059-Ruby-Rails-Beginners-Guide.html)

### Ruby on Railsとは

Webアプリケーション用フレームワークです。Webアプリケーションには定型的な処理が多く含まれます。例えば、HTTPプロトコルの読み取り、HTTPレスポンスの返却など。フレームワークは、それらの定型的な処理を受け持ち、アプリ独自の処理を実装するだけでWebアプリケーションができるようにします。必要な処理のみを実装するため短い開発期間で完成させることができます。

#### Ruby on Railsの特徴

* 命名規約を決めることによりファイル・メソッドを自動生成します。
* ActiveRecordという強力なORマッパがあり、データベースアクセスを容易にします。

#### キーワード

| キーワード     | 説明                                                         |
| -------------- | ------------------------------------------------------------ |
| ルーティング   | URLとAction(処理)を結びつけます。                            |
| Action         | ユーザー操作                                                 |
| MVC            | Webアプリケーション実装アーキテクチャ(Model/View/Controller) |
| コントローラー | ユーザー操作(Action)を処理するクラス                         |
| モデル         | データ（データベース)操作                                    |
| View           | HTTPレスポンスとして返却するHTML                             |



* [Ruby on Railsとは？初心者にもわかりやすく解説！](https://blog.codecamp.jp/what_is_rails)
* [RailsにおけるMVC](https://www.javadrive.jp/rails/ini/index7.html)



## 教科書解説

* [全体像](text_outline.md)
* [BBS](bbs.md)
* [課題](kadai.md)



## 開発Tips

### rake routes

routes.rbのデバッグ

```
$ rake routes
```

#### rails console

モデルの動作テスト

```
$ rails console
```

### rails dbconsole

DBクライアントからDB接続

```
$ rails dbconsole
```



## リンク

* [ターミナルコマンド](terminal.md)

* [画像アップロード](upload_image.md)

* [Railsのバリデーションエラーのメッセージの日本語化 \- Qiita](https://qiita.com/Ushinji/items/242bfba84df7a5a67d5b)

* [Rails エラーメッセージの表示 \- Qiita](https://qiita.com/ryuuuuuuuuuu/items/1a1e53d062bff774d88a)

* [Rails における nil?, empty?, blank?, present? の使い分けとBetter Practice \- Qiita](https://qiita.com/aeroastro/items/b58228decb7094af7594)

* [form\_tag と form\_for は Rails5\.1で soft deprecated \(非推奨\) となり](https://qiita.com/hmmrjn/items/24f3b8eade206ace17e2)

* [redirect\_to @userが何を省略しているかわかりますか？〜挫折しないRailsチュートリアル７章〜 \- Qiita](https://qiita.com/Kawanji01/items/96fff507ed2f75403ecb)

  



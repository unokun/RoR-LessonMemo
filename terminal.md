## コマンド一覧

#### ファイル一覧を表示する

```shell
$ ls -l
```

オプションにaをつけると隠しファイル(.から始まるファイル、フォルダ)も表示されます。

```
$ ls -la
```

#### フォルダ（ディレクトリ)を移動する

```shell
$ cd bbs
```

#### 現在のフォルダ（ディレクトリ）を取得する

```shell
$ pwd
```

#### ファイルをコピーする

```
$ cp fileA fileB
```

#### フォルダ(ディレクトリ)をコピーする

```shell
$ cp -r directoryA directoryB
```

#### コマンド履歴を表示する

```
$ history
```

Ctrl-p(↑)、Ctrl-n(↓)で現在の位置より前のコマンド、後ろのコマンドが表示される。p(previous)、n(next)。Enterキーで確定。確定したコマンドは編集できます。Ctrl-b(←)、Ctrl-f(→)でカーソル移動できます。

Ctrl-rでコマンド(backward)検索モードに入ります。キーを入力するとそのキーを含むコマンドが検索されます。r(reverse)。

#### 特定のportを開いているプロセスを表示する

```
$ sudo lsof -i:ポート番号(8080)
```

phpMyAdminを実行したあと、Ruby on Railsが実行できませんが、これはphpMyAdminを実行しているWebサーバー(apache)が8080のポートを使っているためです。

#### プロセスを終了する

```
$ kill -9 プロセス番号
```

プロセスを強制終了します。最後の手段です。重要なプロセスを終了することもありますので注意して使いましょう。


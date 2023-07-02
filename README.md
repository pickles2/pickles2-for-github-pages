Pickles 2 - for Github Pages
=========

DB不要、オープンソースのPHP製静的CMS [Pickles 2](https://pickles2.com/) をベースに、GitHub Pages に対応するように構成しました。


## インストール手順 - Install

Pickles 2 のインストールは、`composer` コマンドを使用します。
`${documentRoot}` の部分は、インストール先の任意のディレクトリパスに置き換えてください。

```bash
$ cd ${documentRoot}
$ composer create-project pickles2/pickles2-for-github-pages ./
$ chmod -R 777 ./px-files/_sys
$ chmod -R 777 ./src_px2/common/px_resources
```

ウェブサーバーにブラウザでアクセスして、トップページが表示されるか、または、次のコマンドで設定情報が表示されれば成功です。

```bash
$ php ./src_px2/.px_execute.php "/?PX=config"
```


## パブリッシュ手順 - Publish

```bash
$ php ./src_px2/.px_execute.php "/?PX=publish.run"
```

`./dist/` に、スタティックなHTMLとして出力されます。


## サーバーを起動する手順 - Start server

PHPビルトインサーバーで起動することができます。

### プレビュー

```bash
$ composer start
```

### 公開ディレクトリ

```bash
$ composer run-script start-pub
```


## キャッシュを消去する手順 - Clear caches

```bash
$ php ./src_px2/.px_execute.php "/?PX=clearcache"
```

## システム要件 - System Requirement

- Mac, Linux または Windowsサーバ
- Apache
  - mod_rewrite が利用可能であること
  - .htaccess が利用可能であること
  - または、Nginx、 PHPビルトインサーバー でも利用可能
- PHP 7.3 以上
  - [mbstring](https://www.php.net/manual/ja/book.mbstring.php) PHP Extension
  - [JSON](https://www.php.net/manual/ja/book.json.php) PHP Extension
  - [PDO](https://www.php.net/manual/ja/book.pdo.php) PHP Extension
  - [PDO SQLite (PDO_SQLITE)](https://www.php.net/manual/ja/ref.pdo-sqlite.php) PHP Extension




## 更新履歴 - Change log

### pickles2/pickles2-for-github-pages v2.0.0 (リリース日未定)

- 初版リリース


## ライセンス - License

Copyright (c)2001-2023 Tomoya Koyanagi, and Pickles Project<br />
MIT License https://opensource.org/licenses/mit-license.php


## 作者 - Author

- Tomoya Koyanagi <tomk79@gmail.com>
- website: <https://www.pxt.jp/>
- Twitter: @tomk79 <https://twitter.com/tomk79/>

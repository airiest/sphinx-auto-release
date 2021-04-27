# Automatically build Sphinx documents into HTML with GitHub Actions
Sphinxドキュメントをgithubで管理するためのテンプレートです。  
vで始まるタグをpushした際に、Github Actionsにより、  

 - SphinxドキュメントをHTMLにビルド
 - タグ名でリリースページを作成（リリース本文はタグコメント）
 - リリースページにzip化したHTMLドキュメントを添付

を実行します。  
Sphinxドキュメントをローカルビルドすることなく、各リリースバージョンのドキュメントをダウンロードすることを想定しています。

## Sphinx環境を新規に構築する場合
```
$ pip install sphinx
$ pip install sphinx-rtd-theme
$ pip install sphinx-autobuild
```

```
$ sphinx-quickstart
```

conf.pyおよびMakefileを参照し設定を追加してください。  

ローカルビルドは、以下の通りです。build/html以下にファイルが作成されます。

```
$ make html
```

もしくは、以下コマンドでライブ確認が可能です。

```
$ make livehtml
```

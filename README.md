# これは何?

PostCSSが試せるようにWebPackのpostcss-loaderを設定してみたものです。

# 前提

* nodejs がインストールされている
* yarn がインストールされている

# 準備

```
$ yarn intsall
```

# 利用方法

## ファイルの生成方法

```
$ yarn build
```

distディレクトリにファイルが生成されます。

## 開発サーバの起動方法

```
$ yarn serve
```

別にdistディレクトリにファイルは生成されないので注意してください。

# よくありそうな質問

## Q. PostCSS のプラグインの設定箇所は?

`postcss.config.js`をお使いください。

## Q. HTMLファイルどこにあるんですか?

ビルド後のファイルは`dist`ディレクトリに配置されますが、
HtmlWebpackPluginを使って生成しているため元になるHTMLはありません。

## Q. `yarn serve`してるんですがpostcss実行後のcssが生成されません

`yarn build` してください。serve中はファイルの更新はされません。

## Q. 読み込みするCSSを追加したいです

`index.js`で`import`してみてください。

# TODO

## HTMLが編集できない

メモ: 編集できないと試しにくいので、HtmlWebpackPluginのテンプレートを用意してあげておいたほうが良さそう。

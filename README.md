# webpack

## npm init -y

package.jsonの作成（すべてYes）

## npm info webpack

最新のバージョンを確認

## npm install --save-dev webpack

またはバージョンを付与  
例：`npm install --save-dev webpack@4.41.2`

## npm info webpack-cli

最新のバージョンを確認

## npm install --save-dev webpack-cli@3.3.10

webpackの環境が整う。

## npm info live-server

自動でブラウザ表示できて便利なのでインストール

## live-server@1.2.1

起動  
npx live-server  
or  
./node_modules/.bin/live-server


## https://unpkg.com/

cdnサイト

## npm info lodash

最新のバージョンを確認

## npm install --save lodash@4.17.15

インストール

## npx webpack

webpackの利用

## npx npx webpack --config webpack.config.js

指定して利用

## npx npx webpack --mode development

WARNINGが出ているのでモードを指定

### 解説

```webpack.config.js
const path = require("path");
// 絶対パス
const outputPath = path.resolve(__dirname, "dist");

module.exports = {
  // index.jsを取り込む
  entry: "./src/index.js",
  output: {
    // index.jsに依存しているライブラリをくっ付けて出力する
    // ここではlodash
    filename: "main.js",
    path: outputPath
  }
};
```

## npm info webpack-dev-server

## npm install --save-dev webpack-dev-server@3.9.0

## npx webpack-dev-server

webpackでの立ち上げ

## npx webpack-dev-server --open

デフォルトでブラウザを立ち上げる。

## ブラウザでデフォルトでindex,htmlを表示

```
devServer: {
  contentBase: outputPath
}
```

## npm run start

立ち上げを楽にする

```webpack.config.js
"scripts": {
  "start": "webpack-dev-server --open"
},
```
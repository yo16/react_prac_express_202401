# react_prac_express_202401
Express.jsをまた練習

# 手順
~~
## 1. Express環境を構築するexpress-generatorをインストール
トップの階層に入れる。
このため、トップに`package.json`や`node_modules`ができる。
```
npm install express-generator
```
~~
## 1. Express用のNode環境を作る
公式HPを参考にしてやり直し。
- [Express のインストール](https://expressjs.com/ja/starter/installing.html)
```
mkdir express_app
cd express_app
npm init
npm install express
```

- [Express の「Hello World」の例](https://expressjs.com/ja/starter/hello-world.html
app.jsを作って、npm実行
```
npm app.js
```
`http://localhost:3000/`へアクセス

## 2. 公式HPにexpress-generatorがあった
- [Express のアプリケーション生成プログラム](https://expressjs.com/ja/starter/generator.html)
最上位に戻って、express-generatorをインストール。
```
cd ..
npm install express-generator
```

`express_gen_app`というアプリを作成。ただし`node_modules`はなくて`package.json`だけ作成されているので、ディレクトリに入って`npm install`することで準備完了。
```
express express_gen_app
cd express_gen_app
npm install
```

起動。（下記はwindowsの場合の環境変数）
```
SET DEBUG=express-gen-app:* & npm start
```
`http://localhost:3000/`へアクセス

# 調査
## 仕組みの確認
- express_appの起動方法は、`node app.js`だった。
- express_gen_appの起動方法は、`npm start`で、`express_gen_app/package.json`を見ると`"start": "node ./bin/www"`とある。つまり`node ./bin/www`。

- `express_app/app.js`では、その中で`get`とか`listen`とかやっててストレートにわかりやすい。
- `express_gen_app/bin/www`では、
  - app.jsを呼んでいる。
    - その中で、`./routes/index`とか呼んでいる。
  - ポートの設定や、デバッグモードの出力設定


# 参考にしたサイト
- 公式
  - [Express - Node.js Web アプリケーション・フレームワーク](https://expressjs.com/ja/)
  - 
- [React / Express で作る Web アプリケーション開発入門｜研修コースに参加してみた | SEプラス 研修 Topics](https://www.seplus.jp/dokushuzemi/blog/2021/12/tutorial_react_express.html)
- [React+Expressで本番環境へデプロイ #JavaScript - Qiita](https://qiita.com/creaporta/items/aedc6f7510cfb5f6352e)
- [【TypeScriptあり】Node.jsとReactでWebアプリを作る【Express使います】 | RalaCode](https://ralacode.com/blog/post/create-nodejs-react-app-with-typescript/)
  - package.jsonの"main"は入れても入れなくてもエラーは出ないけど、それはパッケージ公開時のために必要とか、ポートは何でもいいけどできれば3000以外がいいとか、そういうのがいい
  > 始めから正解のコードを書くのではなく、わざとエラーを起こしてそれにどう対応するかを体感することが合理的なのかなと個人的には考えています。


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

## 2. ExpressでHelloWorld
- [Express の「Hello World」の例](https://expressjs.com/ja/starter/hello-world.html
app.jsを作って、npm実行
```
$ npm app.js
```
`http://localhost:3000/`へアクセス


# 参考にしたサイト
- 公式
  - [Express - Node.js Web アプリケーション・フレームワーク](https://expressjs.com/ja/)
  - 
- [React / Express で作る Web アプリケーション開発入門｜研修コースに参加してみた | SEプラス 研修 Topics](https://www.seplus.jp/dokushuzemi/blog/2021/12/tutorial_react_express.html)
- [React+Expressで本番環境へデプロイ #JavaScript - Qiita](https://qiita.com/creaporta/items/aedc6f7510cfb5f6352e)

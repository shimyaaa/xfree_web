# xfree_web

## サイト構造

```pug
//- 記事エリア基本
article#hoge.article_area
  h2.article_main-title 見出し
```

## やったこと

```shell
yarn init
yarn add sass pug pug-cli
```

```json
"scripts": {
  "sass": "sass",
  "sass:w": "sass --watch src/assets/css:dist/assets/css",
  "pug": "pug",
  "pug:w": "pug -P -w -o dist/ src/index.pug"
}
```

## 追加したい機能

* コード部分をワンクリックでクリップボードにコピーする

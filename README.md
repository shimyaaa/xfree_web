# xfree_web

[WEB制作をするときに見るサイト集](http://shimyaaa.html.xdomain.jp/web/)の制作環境・ソースコードです。

## 使ったもの

- Pug
- Sass
- Node.js
  - yarn
    - pug
    - pug-cli
    - sass
- nst-reset-css (オリジナルリセットCSS)

## package.json追加設定

```json
"scripts": {
  "sass": "sass",
  "sass:w": "sass --watch src/assets/css:dist/assets/css",
  "pug": "pug",
  "pug:w": "pug -P -w -o dist/ src/index.pug"
}
```

## サイト構造

### id一覧

```css
#site-check
  #html-css-checker
  #img-alt-checker
#recommend-site
  #can-i-use
  #tinypng
  #codic
  #placehold
#totop
```

### 使いまわしコード

```pug
//-目次
ul.toc_box
  li
    a(href="#hoge") 見出し
    ul.toc_section_title
      li
        a(href="#hoge") セクションタイトル
      li
        a(href="#hoge") セクションタイトル
  li
    a(href="#hoge") 見出し
    ul.toc_section_title
      li
        a(href="#hoge") セクションタイトル
      li
        a(href="#hoge") セクションタイトル

//- 記事エリア基本
article#hoge.article-area
  h2.article-area_main-title 見出し
  section#hpge.article-area_section
    h3.section_title セクションタイトル
    p.text

//- リンクボックス
.link-box
  dl.link-box_item
    dt.link-box_item_title サイト名:
    dd.link-box_item_link
      a(href="http://validator.w3.org/nu/" target="_blank" rel="noopener") URL

//- 使い方
section.how-to-list
  h4.how-to-list_title 使い方
  p.text
  ol.how-to-list_box
    li 手順1
    li 手順2
    li 手順3

//- 図表
figure.img-figure
  a(href="")
    img.img-figure_img(src="", alt="" width=0 height=0)
  figcaption.img-figure_caption キャプション

//- コード表示
.code-box
  pre.code-box_pre
    code hello world.
  p.code-box_caption キャプション
```

## TODO

1. 補足追加
2. 文字の背景色設定
3. tips後回し
4. 背景色とかボーダーの色はいい感じに
5. コード部分をワンクリックでクリップボードにコピーする機能追加

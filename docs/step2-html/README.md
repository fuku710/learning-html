# HTML

## 基本

```html
<!DOCTYPE html>
<html>
  <head>
    <title>私のプロフィール</title>
    <meta charset="utf-8" />
  </head>
  <body>
    こんにちは
  </body>
</html>
```

### `<!DOCTYPE html>` DOCTYPE 宣言

「これは HTML5 ですよ」と宣言するためのものです。必ず最初に書きましょう。

### `<html></html>` html タグ

このタグで囲まれているものが html です。

### `<head></head>` head タグ

タイトルなど WEB ページの情報はこのタグの中に書きます。

### `<title></title>` title タグ

WEB ページのタイトルです（ブラウザのタブに表示されているアレ！）。

### `<meta></meta>` meta タグ

めた

### `<body></body>` body タグ

このタグの中がブラウザ上に表示されます。

## 見出しと段落

見出しと段落をつける

```html
<!DOCTYPE html>
<html>
  <head>
    <title>私のプロフィール</title>
    <meta charset="utf-8" />
  </head>
  <body>
    <h1>私のプロフィール</h1>
    <p>こんにちは</p>
  </body>
</html>
```

### h タグ

見出しに使うタグ、h1 から h6 まであるのでうまく使い分けよう

```html
<body>
  <h1>見出し1</h1>
  <h2>見出し2</h2>
  <h3>見出し3</h3>
  <h4>見出し4</h4>
  <h5>見出し5</h5>
  <h6>見出し6</h6>
</body>
```

### p タグ

paragrah(=段落)を意味するタグ。ある程度の量の文章を囲んだりする

```html
<body>
  <p>吾輩は猫である、名前はまだない。</p>
</body>
```

## 画像

```html
<!DOCTYPE html>
<html>
  <head>
    <title>私のプロフィール</title>
    <meta charset="utf-8" />
  </head>
  <body>
    <h1>私のプロフィール</h1>
    <p>こんにちは</p>
    <img src="cat.jpg" />
  </body>
</html>
```

### 画像が大きい場合

width 属性や height 属性でサイズを指定しよう

```html
<img src="cat.jpg" width="150px" height="150px" />
```

## 表

```html
<!DOCTYPE html>
<html>
  <head>
    <title>私のプロフィール</title>
    <meta charset="utf-8" />
  </head>
  <body>
    <h1>私のプロフィール</h1>
    <p>こんにちは</p>
    <img src="cat.jpg" />
    <table>
      <tr>
        <td>名前</td>
        <td>福田 尚人</td>
      </tr>
      <tr>
        <td>出身</td>
        <td>横浜</td>
      </tr>
    </table>
  </body>
</html>
```

### table タグ

テーブルを作るためのタグこの中に tr タグや td タグを記述する

### tr タグ

table row
このタグで囲ったものが表の行(=row)になる

### td タグ

table data
このタグで囲ったものが表の列になる

## リンク

表の行を追加して SNS などのリンクを貼ってみよう

```html
<!DOCTYPE html>
<html>
  <head>
    <title>私のプロフィール</title>
    <meta charset="utf-8" />
  </head>
  <body>
    <h1>私のプロフィール</h1>
    <p>こんにちは</p>
    <img src="cat.jpg" />
    <table>
      <tr>
        <td>名前</td>
        <td>福田 尚人</td>
      </tr>
      <tr>
        <td>出身</td>
        <td>横浜</td>
      </tr>
      <tr>
        <td>Twitter</td>
        <td><a href="https://twitter.com/never9612">@never9612</a></td>
      </tr>
    </table>
  </body>
</html>
```

### a タグ

anchor
href 属性でリンク先を指定します

```html
<!-- URLを指定 -->
<a href="https://google.com">Google</a>
<!-- HTMLファイルを指定 -->
<a href="page1.html">ページ1へ</a>
```

## リスト

リストを作って好きなものを並べてみよう

```html
<!DOCTYPE html>
<html>
  <head>
    <title>私のプロフィール</title>
    <meta charset="utf-8" />
  </head>
  <body>
    <h1>私のプロフィール</h1>
    <p>こんにちは</p>
    <img src="cat.jpg" />
    <table>
      <tr>
        <td>名前</td>
        <td>福田 尚人</td>
      </tr>
      <tr>
        <td>出身</td>
        <td>横浜</td>
      </tr>
      <tr>
        <td>Twitter</td>
        <td><a href="https://twitter.com/never9612">@never9612</a></td>
      </tr>
    </table>

    <p>好きな食べ物</p>
    <ul>
      <li>カレー</li>
      <li>ラーメン</li>
      <li>ハンバーグ</li>
    </ul>
  </body>
</html>
```

### ul タグと ol タグ

unoder list と order list
このタグで囲んだものがリストになります
ul タグはリストのアイテムには番号が振られませんが、ol タグには番号が振られます

### li タグ

リストのアイテムです ol タグか ul タグの中に記述します

```html
<!-- ul -->
<ul>
  <li>項目1</li>
  <li>項目2</li>
  <li>項目3</li>
</ul>
<!-- ol -->
<ol>
  <li>項目1</li>
  <li>項目2</li>
  <li>項目3</li>
</ol>
```

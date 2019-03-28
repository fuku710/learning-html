# CSS

## 基本

CSS は html ファイル内に`<style>`タグを記述し、その中に CSS を書くか、css ファイルを作り`<link>`タグで読み込む方法があります

### style タグの場合

index.html

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
    div {
      width: 32px;
      height: 32px;
      background: black;
    }
    </style>
  <head>
  <body>
    <div></div>
  </body>
</html>
```

### css ファイルの場合

style.css

```css
div {
  width: 32px;
  height: 32px;
  background: black;
}
```

index.html

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="style.css" />
  <head>
  <body>
    <div></div>
  </body>
</html>
```

要素名を指定すればすべての要素に適応できますが、クラスを指定したり id を指定したりできます

```css
/* 要素を指定 */
div {
  /*ここにプロパティと値*/
}
/* クラスを指定 */
.hoge {
  /*ここにプロパティと値*/
}
/* idを指定 */
#fuga {
  /*ここにプロパティと値*/
}
```

## サイズ

img タグのサイズを CSS で指定してみましょう

```css
img {
  width: 150px;
  height: 150px;
}
```

## レイアウト

HTML の要素はブロックレベル要素とインライン要素に分けられます
ざっくり説明すると以下の通りになります

|          | ブロックレベル要素 | インライン要素 |
| -------- | ------------------ | -------------- |
| 特徴     | 改行される         | 改行されない   |
| タグの例 | div                | span           |

ブロックレベル要素とインライン要素は CSS の diplay プロパティで指定できます

### flexbox を使う

要素をブロックレベル要素にして、頑張ってレイアウトしても良いですが display プロパティで flexbox を指定するとレイアウトはとても楽なのでそれを使おう
body 全体を縦に並べて、ul の中を横に並べてみよう
ついでに ul に`list-style:none;`を指定することによりリストの ● を消しておきます。

```css
body {
  display: flex;
  flex-direction: column;
  align-items: center;
}

ul {
  display: flex;
  list-style: none;
}
```

## 余白

余白の種類は margin、padding があります
margin が外側の余白、padding が内側の余白という感じです

余白を調整したい要素にクラスを設定して、まとめて margin を設定してみましょう

```html
<!DOCTYPE html>
<html>
  <head>
    <title>私のプロフィール</title>
    <meta charset="utf-8" />
  </head>
  <body>
    <h1>私のプロフィール</h1>
    <p class="content-item">こんにちは</p>
    <img src="cat.jpg" class="content-item" />
    <table class="content-item">
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

    <p class="content-item">好きな食べ物</p>
    <ul class="content-item">
      <li>カレー</li>
      <li>ラーメン</li>
      <li>ハンバーグ</li>
    </ul>
  </body>
</html>
```

```css
/* content-itemクラスに上下に余白 */
.content-item {
  margin: 0px;
  margin-top: 4px;
  margin-bottom: 4px;
}

/* ulはデフォルトでpaddingがかかっているので0pxにして無効化 */
ul {
  display: flex;
  list-style: none;
  padding: 0px;
}
/* 
li要素にpaddingとmarginを設定
枠線をつけてpaddingの効果をわかりやすく
*/
li {
  padding: 4px;
  margin: 4px;
  border: solid 1px black;
}
```

## 文字色・背景色

body に color プロパティを追加して全体の文字色を変えてみましょう

```css
body {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #444444;
}
```

リストのアイテムに背景色をつけてみましょう
アイテムごとに色を変えたいのでそれぞれに id を設定して CSS を指定してみましょう

```html
<ul class="content-item">
  <li id="curry">カレー</li>
  <li id="ramen">ラーメン</li>
  <li id="hamburg-steak">ハンバーグ</li>
</ul>
```

```css
#curry {
  background: orange;
}

#ramen {
  background: green;
}

#hamburg-steak {
  background: blue;
}
```

## マウスオーバーとアニメーション

### hover

CSS セレクタの後ろに`:hover`をつけるとマウスオーバー時のスタイルを指定できます

```css
a:hover {
  color: gray;
}
```

### transition

`transition-*` プロパティを指定するとスタイルが変化したときのアニメーションを設定できます

```css
a {
  transition-duration: 500ms; /* transition-durationはアニメーション時間の設定 */
  color: inherit; /* ついでにリンクの色をデフォルト色に設定します */
}

a:hover {
  color: gray;
}
```

## SVGとは
Scalable Vector Graphicsの略である。
画像形式のうちの１つであり、大きさなどを自由に変更することができる。
画像には2種類存在して、「ベクター形式」と「ラスター形式」が存在する。
SVGはベクター形式である。
テキストデータである。


### ベクター形式
自由に大きさを変えたりしても、画像がぼやけたり劣化することはない。
座標が決まっているだけなので、元の大きさが決まっていない。
点や線の数学的名情報で書かれている。

### ラスター形式 
画像を拡大すると画像がぼやけたりする。
写真やイラストなどの画像
JPG, PNG, GIF などの画像形式
写真などの色数が多い画像や、繊細な色の変化に対応できる。


```
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./assets/css/station10.css" type="text/css" />
    <title>Station 10</title>
  </head>
  <body>
    <svg viewBox="0, 0, 500, 500" xmlns="http://www.w3.org/2000/svg" fill="#008000">
      <rect x="0" y="0" width="100px" height="100px" />
    </svg>
  </body>
</html>
```

まず、`viewBox="0, 0, 500, 500`で仮想キャンパスを作成する。０，０の位置から５００，５００の位置までの領域であることを指定する。

つぎに、`xmlns="http://www.w3.org/2000/svg`　SVGを使用することを宣言する。これがないとSVGと認識されない。

`fill`これな塗りつぶしの色指定。


`rect x="0" y="0" width="100px" height="100px"`これは四角を書くように指示している。

x,y は四角の左上の部分の位置をしてい。　width,heightで横幅と縦幅を指定している。
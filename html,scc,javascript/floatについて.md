#floatについて

<details>
<summary>THMLを開く </summary>
  
``` html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Station 2</title>
    <link rel="stylesheet" href="./assets/css/station2.css" type="text/css" />
  </head>
  <body>
    <div id="red"></div>
    <div id="blue"></div>
    <div id="green"></div>
  </body>
</html>
```
  
</details>

<details>
<summary>CSSを開く </summary>

``` CSS
@charset "utf-8";

#red {
  width: 300px;
  height: 300px;
  background-color: #ff6666;
  float: left;
}

#blue {
  width: 300px;
  height: 300px;
  background-color: #0000ff;
  float: left;
}

#green {
  width: 300px;
  height: 300px;
  background-color: #3cb371;
  float: left;
  clear: both;
}


```
  
</details>

## floatとclearについて


### floatとは
`float`はwebの画像やブロック要素を浮かせることができる。
そして、浮かび上がってできたスペースは下の要素がくる。
`float`で浮かばせた後、`left` , `rigth` で位置を指定できる。

### clearとは

ブロックレベル要素に適用する。
要素の上に「クリアランス」という仮想のスペースを足して、
`float` 要素の下端まで自身を押し下げる仕組みである。










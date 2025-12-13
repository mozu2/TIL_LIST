# リスト要素について。
## `<ul>` `<li>` `<ol>`のタグについて

### `<ul>`とは
htmlもタグであり、順序を気にしないリストを表す。

### `<li>`とは
リストの項目を表すために用いられる。
その項目が属する順序付きリスト (`<ol>`)、順序なしリスト (`<ul>`)、メニュー (`<menu>`) のいずれかの子要素として配置する必要がある。

### `<ol>`とは
項目の順序付きリストを表す。
ふつうは番号付きのリストとして表示されまる。




### `<ul>`,`<li>`使い方。
```
<ul>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>
```
### 実行結果

<ul>
  <li>first item</li>
  <li>second item</li>
  <li>third item</li>
</ul>


### `<ol>`,`<li>`の使い方
```
<ol>
  <li>Fee</li>
  <li>Fi</li>
  <li>Fo</li>
  <li>Fum</li>
</ol>
```

### 実行結果

<ol>
  <li>Fee</li>
  <li>Fi</li>
  <li>Fo</li>
  <li>Fum</li>
</ol>

---

## リストの入れ子
リストの中にリストを作成することができる。

### ❌間違った例 *結果は同じように表示されているが書き方がダメ。
```
<ul>
  <li>野菜</li>
    <ul> <! -- ここに書くのはNG -->
      <li>キャベツ</li>
      <li>トマト</li>
    </ul>
  <li>果物</li>
    <ul> <! -- ここに書くのはNG -->
      <li>りんご</li>
      <li>バナナ</li>
    </ul>
</ul>
```
<ul>
  <li>野菜</li>
    <ul> <! -- ここに書くのはNG -->
      <li>キャベツ</li>
      <li>トマト</li>
    </ul>
  <li>果物</li>
    <ul> <! -- ここに書くのはNG -->
      <li>りんご</li>
      <li>バナナ</li>
    </ul>
</ul>


### ⭕正しい例
```
<ul>
  <li>野菜
    <ul>
      <li>キャベツ</li>
      <li>トマト</li>
    </ul>
  </li>
  <li>果物
    <ul>
      <li>りんご</li>
      <li>バナナ</li>
    </ul>
  </li>
</ul>
```

### 結果

<ul>
  <li>野菜
    <ul>
      <li>キャベツ</li>
      <li>トマト</li>
    </ul>
  </li>
  <li>果物
    <ul>
      <li>りんご</li>
      <li>バナナ</li>
    </ul>
  </li>
</ul>

---






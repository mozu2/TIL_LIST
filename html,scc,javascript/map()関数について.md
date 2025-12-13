# map()関数を使う

## 前提知識
* `[ ]`で囲まれた部分を **配列 (Array)** という。
*  `{}`で囲まれた部分は **オブジェクト** という。

## map関数とは。
* 配列のすべてのデータを加工して新しい配列に作り直す。

---
### コード全体
getData関数でデータを定義して、mapを使用してフルネームを追加したい新しい配列を作成する。
```
function getData() {
    const test = [
        { id: 1, first_name: '優', family_name: '大木', affiliation: 'TechTrain', is_student: false },
        { id: 2, first_name: '太郎', family_name: '山田', affiliation: 'HogeHoge大学', is_student: true }
    ];
    // map関数でbuildFullNameを実行する
    return test.map(buildFullName)
}

function buildFullName(data) {
    return {id: data.id, full_name:data.family_name + ' ' + data.first_name, first_name:data.first_name, family_name:data.family_name, affiliation:data.affiliation, is_student:data.is_student};
    }

```


```
function buildFullName(data) {
    return {
        id: data.id, 
        full_name: data.family_name + ' ' + data.first_name, // ここで合体！
        first_name: data.first_name, 
        family_name: data.family_name, 
        affiliation: data.affiliation, 
        is_student: data.is_student
    };
}
```

(data)の部分にはmap関数で取り出した配列データが入っている。
## 1回目のループデータ。
```
{ id: 1, first_name: '優', family_name: '大木', affiliation: 'TechTrain', is_student: false },
```
## 2回目のループデータ。
```
{ id: 2, first_name: '太郎', family_name: '山田', affiliation: 'HogeHoge大学', is_student: true }
```

##  `id: data.id` となる理由
なぜ、id: 1, id: 2 になるのかというと。
[.]　の意味は～の中身という意味を持つ。data.id というのは
dataの中にあるidを意味している。つまり、id: 1 という出力になる。

---

 ## より見やすい書き方。テンプレートリテラルによる文字連結 
 ここからは見やすくする書き方についてまとめる。

```
// 変更前
full_name: data.family_name + ' ' + data.first_name

// 変更後（同じ意味ですが、見やすくなります）
full_name: `${data.family_name} ${data.first_name}`
```

上のほうでは文字列を＋でつないでいる。そして空白部分を' 'で表している。
この書き方は短文だとよいが、もっと項目が増えてくると+ ' ' + が増えていき醜くなる。

下のほうは`` と　$を使用している。
この書き方をテンプレートリテラルという。

全体を``で囲み、使いたい変数を${}で囲む

実際にテンプレートリテラルを使うときと使わないときの違いを見てみる。
まずはテンプレートリテラルを使用しない場合を見てみる。
```
'ID番号は ' + data.id + ' 番で、名前は ' + data.family_name + ' です。'
```
このよう+をたくさんしようしないといけない。これはとても書くのに時間がかかるし、
あまりきれいではない。
次にテンプレートリテラルを使用した場合。
```
// 例えばこんなことも簡単にできます
`ID番号は ${data.id} 番で、名前は ${data.family_name} です。`
```
テンプレートリテラルを使用するとこんなにも簡単に、見やすくなる。
一目見ただけでどのようになっているのかすぐにわかる。
これは便利である。

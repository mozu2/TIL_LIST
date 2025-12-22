```
<?php

namespace Src\Station09;

class Question
{
    public function main(): array
    {
        $users = [
    [
        'id' => 1,
        'last_name' => '山田',
        'first_name' => '太郎',
        'age' => 20,
        'password' => 'yamada',
    ],
    [
        'id' => 2,
        'last_name' => '鈴木',
        'first_name' => '次郎',
        'password' => 'suzuki',
    ],
    [
        'id' => 3,
        'last_name' => '佐藤',
        'first_name' => '花子',
        'password' => 'sato',
    ],
];
        foreach($users as $key => $value){

            
            $value['full_name'] = $value['last_name'] . $value['first_name'];



            if(!isset($value['age'])){
                $value['age'] = null;
            }

       unset($value['password']);

        
        $users[$key] = $value;
    


        }
                    return $users;
    }
}

```

`($users as $key => $value`では
users配列の中の配列キーとキーに対応する値が入る。


一回目のループでは、
`$key` には0
`%value` には    ['id' => 1,'last_name' => '山田','first_name' => '太郎',　'age' => 20,　'password' => 'yamada',],が入る。

あとは繰り返し。

`$value['full_name'] = $value['last_name'] . $value['first_name'];`では、

`$value`という新しい配列のに`full_name`を追加している。

` if(!isset($value['age']))` 
まず、`isset`についてだ。

`isset($value)`
$valueが存在していて、かつnullではないならtrueを返す関数である。

```
$a = 10;
$b = null;

isset($a); // true （存在していて、null ではない）
isset($b); // false（存在しているが、null なので false）
isset($c); // false（$c 自体が存在しない）
```
## では次に,`!isset`についてだ。
`!isset($value)`
$valueが存在しないか、nullならtrueという意味である。

```
$a = 10;
$b = null;

!isset($a); // false（isset($a) が true だから）
!isset($b); // true （isset($b) が false だから）
!isset($c); // true （$c が存在しないので isset($c) は false）

```

つまり、
```
            if(!isset($value['age'])){
                $value['age'] = null;
            }
```

これは、$valueに`age`が存在しないまたは、nullの時に`['age'] = null;`を追加するということである。

## `unset()` について
変数や配列を消去するときに使用する関数である。

`unset($value['password']);`これは`password`を削除している。

最後に`$users[$key] = $value;`これで更新して`return`で `$users`を返す。



























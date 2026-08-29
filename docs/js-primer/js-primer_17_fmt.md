
# ループと反復処理

> 原文：[`jsprimer.net/basic/loop/`](https://jsprimer.net/basic/loop/)

この章では、while 文やfor 文などの基本的な反復処理と制御文について学んでいきます。

プログラミングにおいて、同じ処理を繰り返すために同じコードを繰り返し書く必要はありません。 ループやイテレータなどを使い、反復処理として同じ処理を繰り返し実行できます。

また、for 文などのような構文だけではなく、配列のメソッドを利用して反復処理を行う方法もあります。 配列のメソッドを使った反復処理もよく利用されるため、合わせて見ていきます。

## while 文

while 文は`条件式`が`true`であるならば、反復処理を行います。

```
while (条件式) {
    実行する文;
} 
```

while 文の実行フローは次のようになります。 最初から`条件式`が`false`である場合は、何も実行せずwhile 文は終了します。

1.  `条件式` の評価結果が`true`なら次のステップへ、`false`なら終了

1.  `実行する文`を実行

1.  ステップ1へ戻る

次のコードでは`x`の値が10 未満であるなら、コンソールへ繰り返しログが出力されます。 また、`実行する文`にて、`x`の値を増やし`条件式`が`false`となるようにしています。

```
let x = 0;
console.log(`ループ開始前のxの値: ${x}`);
while (x < 10) {
    console.log(x);
    x += 1;
}
console.log(`ループ終了後のxの値: ${x}`); 
```

つまり、`実行する文`の中で`条件式`が`false`となるような処理を書かないと無限ループします。 JavaScriptにはより安全な反復処理の書き方があるため、while 文は使う場面が限られています。

安易にwhile 文を使うよりも、ほかの書き方で解決できないかを考えてからでも遅くはないでしょう。

## [コラム] 無限ループ

反復処理を扱う際に、コードの書き間違いや条件式のミスなどから無限ループを引き起こしてしまう場合があります。 たとえば、次のコードは条件式の評価結果が常に`true`となってしまうため、無限ループが発生してしまいます。

```
let i = 1;
// 条件式が常にtrueになるため、無限ループする
while (i > 0) {
    console.log(`${i}回目のループ`);
    i += 1;
} 
```

無限ループが発生してしまったときは、あわてずにスクリプトを停止してからコードを修正しましょう。

ほとんどのブラウザは無限ループが発生した際に、自動的にスクリプトの実行を停止する機能が含まれています。 また、ブラウザで該当のスクリプトを実行しているページ（タブ）またはブラウザそのものを閉じることで強制的に停止できます。 Node.jsで実行している場合は`Ctrl + C`を入力し、終了シグナルを送ることで強制的に停止できます。

無限ループが発生する原因のほとんどは条件式に関連する実装ミスです。 まずは条件式の確認をしてみることで問題を解決できるはずです。

## do-while 文

do-while 文はwhile 文とほとんど同じですが実行順序が異なります。

```
do {
    実行する文;
} while (条件式); 
```

do-while 文の実行フローは次のようになります。

1.  `実行する文`を実行

1.  `条件式` の評価結果が`true`なら次のステップへ、`false`なら終了

1.  ステップ1へ戻る

while 文とは異なり、必ず最初に`実行する文`を処理します。

そのため、次のコードのように最初から`条件式`を満たさない場合でも、 初回の`実行する文`が処理され、コンソールへ`1000`と出力されます。

```
const x = 1000;
do {
    console.log(x); // => 1000
} while (x < 10); 
```

この仕組みをうまく利用し、ループの開始前とループ中の処理をまとめて書くことができます。 しかし、while 文と同じくほかの書き方で解決できないかを考えてからでも遅くはないでしょう。

## for 文

for 文は繰り返す範囲を指定した反復処理を書くことができます。

```
for (初期化式; 条件式; 増分式) {
    実行する文;
} 
```

for 文の実行フローは次のようになります。

1.  `初期化式` で変数の宣言

1.  `条件式` の評価結果が`true`なら次のステップへ、`false`なら終了

1.  `実行する文` を実行

1.  `増分式` で変数を更新

1.  ステップ2へ戻る

次のコードでは、for 文で1から10までの値を合計して、その結果をコンソールへ出力しています。

```
let total = 0; // totalの初期値は0
// for 文の実行フロー
// iを0で初期化
// iが10 未満（条件式を満たす）ならfor 文の処理を実行
// iに1を足し、再び条件式の判定へ
for (let i = 0; i < 10; i++) {
    total += i + 1; // 1から10の値をtotalに加算している
}
console.log(total); // => 55 
```

このコードは1から10までの合計を電卓で計算すればいいので、普通は必要ありませんね。 もう少し実用的なものを考えると、任意の数値の入った配列を受け取り、その合計を計算して返すという関数を実装すると良さそうです。

次のコードでは、任意の数値が入った配列を受け取り、その合計値を返す `sum` 関数を実装しています。 `numbers`配列に含まれている要素を先頭から順番に変数`total`へ加算することで合計値を計算しています。

```
function sum(numbers) {
    let total = 0;
    for (let i = 0; i < numbers.length; i++) {
        total += numbers[i];
    }
    return total;
}

console.log(sum([1, 2, 3, 4, 5])); // => 15 
```

JavaScriptの配列である`Array`オブジェクトには、反復処理のためのメソッドが備わっています。 そのため、配列のメソッドを使った反復処理も合わせて見ていきます。

## 配列の`forEach`メソッド

配列には`forEach`メソッドというfor 文と同じように反復処理を行うメソッドがあります。

`forEach`メソッドでの反復処理は、次のように書けます。

```
const array = [1, 2, 3];
array.forEach(currentValue => {
    // 配列の要素ごとに呼び出される処理
}); 
```

JavaScriptでは、関数がファーストクラスであるため、その場で作った無名関数（名前のない関数）を引数として渡せます。

引数として渡される関数のことを**コールバック関数**と呼びます。 また、コールバック関数を引数として受け取る関数やメソッドのことを**高階関数**と呼びます。

```
const array = [1, 2, 3];
// forEachは"コールバック関数"を受け取る高階関数
array.forEach(コールバック関数); 
```

`forEach`メソッドのコールバック関数には、配列の要素が先頭から順番に渡されて実行されます。 つまり、コールバック関数の仮引数である`currentValue`には、1から3の値が順番に渡されます。

```
const array = [1, 2, 3];
array.forEach(currentValue => {
    console.log(currentValue);
});
// 1
// 2
// 3
// と順番に出力される 
```

先ほどのfor 文の例と同じ数値の合計を返す`sum` 関数を`forEach`メソッドで実装してみます。

```
function sum(numbers) {
    let total = 0;
    numbers.forEach(num => {
        total += num;
    });
    return total;
}

sum([1, 2, 3, 4, 5]); // => 15 
```

`forEach`はfor 文の`条件式`に相当するものはなく、必ず配列のすべての要素を反復処理します。 変数`i`といった一時的な値を定義する必要がないため、シンプルに反復処理を書けます。

## break 文

break 文は処理中の文から抜けて次の文へ移行する制御文です。 while、do-while、forの中で使い、処理中のループを抜けて次の文へ制御を移します。

```
while (true) {
    break; // *1 へ
}
// *1 次の文 
```

switch 文で出てきたものと同様で、処理中のループ文を終了できます。

次のコードでは配列の要素に1つでも偶数を含んでいるかを判定しています。

```
const numbers = [1, 5, 10, 15, 20];
// 偶数があるかどうか
let isEvenIncluded = false;
for (let i = 0; i < numbers.length; i++) {
    const num = numbers[i];
    // numが2で割り切れるなら偶数
    if (num % 2 === 0) {
        isEvenIncluded = true;
        break;
    }
}
console.log(isEvenIncluded); // => true 
```

1つでも偶数があるかがわかればいいため、配列内から最初の偶数を見つけたらfor 文での反復処理を終了します。 このような処理は、使い回せるように関数として実装するのが一般的です。

同様の処理をする `isEvenIncluded` 関数を実装してみます。 次のコードでは、break 文が実行され、ループを抜けた後にreturn 文で結果を返しています。

```
// 引数の`num`が偶数ならtrueを返す
function isEven(num) {
    return num % 2 === 0;
}
// 引数の`numbers`に偶数が含まれているならtrueを返す
function isEvenIncluded(numbers) {
    let isEvenIncluded = false;
    for (let i = 0; i < numbers.length; i++) {
        const num = numbers[i];
        if (isEven(num)) {
            isEvenIncluded = true;
            break;
        }
    }
    return isEvenIncluded;
}
const array = [1, 5, 10, 15, 20];
console.log(isEvenIncluded(array)); // => true 
```

return 语句可以结束当前函数，因此也可以这样写。如果`numbers`中包含至少一个偶数，则结果为`true`，因此当找到偶数时立即返回`true`。

```
function isEven(num) {
    return num % 2 === 0;
}
function isEvenIncluded(numbers) {
    for (let i = 0; i < numbers.length; i++) {
        const num = numbers[i];
        if (isEven(num)) {
            return true;
        }
    }
    return false;
}
const numbers = [1, 5, 10, 15, 20];
console.log(isEvenIncluded(numbers)); // => true 
```

当找到偶数时立即返回，这样就不需要临时变量，代码也更简洁。

## 配列の`some`方法

*前に提到的`isEvenIncluded`函数是当找到偶数时返回`true`的函数。在数组中，可以使用`some`方法执行类似操作。

`some`方法接受一个回调函数作为数组每个元素的测试处理。当回调函数返回`true`时，迭代处理将在该点结束，`some`方法返回`true`。

```
const array = [1, 2, 3, 4, 5];
const isPassed = array.some(currentValue => {
    // テストをパスするとtrue、そうでないならfalseを返す
}); 
```

使用`some`メソッド，可以像这样检查数组中是否包含偶数。将测试偶数的回调函数`isEven`传递给接收到的值。

```
function isEven(num) {
    return num % 2 === 0;
}
const numbers = [1, 5, 10, 15, 20];
console.log(numbers.some(isEven)); // => true 
```

## continue 语句

continue 语句是结束当前迭代处理并执行下一个迭代处理的语句。它可以在 while、do-while、for 中使用。

例如，在 while 循环的处理过程中，如果执行了`continue`语句，则当前迭代处理将在该点结束。然后，从下一个迭代处理开始，从评估`条件式`的地方重新开始循环。

```
while (条件式) {
    // 実行される処理
    continue; // `条件式` へ
    // これ以降の行は実行されません
} 
```

在下面的代码中，我们从数组中收集偶数，并返回一个新的数组。如果不包含偶数，则跳过处理中的 for 循环。

```
// `number`が偶数ならtrueを返す
function isEven(num) {
    return num % 2 === 0;
}
// `numbers`に含まれている偶数だけを取り出す
function filterEven(numbers) {
    const results = [];
    for (let i = 0; i < numbers.length; i++) {
        const num = numbers[i];
        // 偶数ではないなら、次のループへ
        if (!isEven(num)) {
            continue;
        }
        // 偶数を`results`に追加
        results.push(num);
    }
    return results;
}
const array = [1, 5, 10, 15, 20];
console.log(filterEven(array)); // => [10, 20] 
```

当然，也可以不使用`continue`语句，而是将“偶数则添加到`results`”这样的写法。

```
if (isEven(number)) {
    results.push(number);
} 
```

在这种情况下，当条件变得复杂时，代码的嵌套会变得很深，代码的可读性会降低。因此，为了避免复杂的代码，我会在尽可能早的阶段停止进一步的执行。

## 配列の`filter`方法

要创建只包含特定值的新的数组，可以使用 filter 方法。

`filter`方法接受一个回调函数として数组每个元素のテスト処理。它返回一个只包含回调函数が返す`true`の要素の新しい配列。

```
const array = [1, 2, 3, 4, 5];
// テストをパスしたものを集めた配列
const filteredArray = array.filter((currentValue, index, array) => {
    // テストをパスするならtrue、そうでないならfalseを返す
}); 
```

前に提到的使用 continue 语句进行值筛选，使用 filter 方法可以更简洁地编写。下面的代码使用 filter 方法筛选出偶数。

```
function isEven(num) {
    return num % 2 === 0;
}

const array = [1, 5, 10, 15, 20];
console.log(array.filter(isEven)); // => [10, 20] 
```

## for...in 语句

for...in 语句はオブジェクトのプロパティに対するイテレーションを行う。¹*

```
for (プロパティ in オブジェクト) {
    実行する文;
} 
```

下のコードでは、`obj`のプロパティ名を`key`変数に代入してイテレーションを行います。`obj`には3つのプロパティ名があるため、3回繰り返されます（各ループで新しいブロックが作成されるため、`key`変数の再定義エラーは発生しません。詳細については、「関数とスコープ」章の「ブロックスコープ」を参照）。

```
const obj = {
    "a": 1,
    "b": 2,
    "c": 3
};
// 注記: ループのたびに毎回新しいブロックに変数 keyが定義されるため、再定義エラーが発生しない
for (const key in obj) {
    const value = obj[key];
    console.log(`key:${key}, value:${value}`);
}
// "key:a, value:1"
// "key:b, value:2"
// "key:c, value:3" 
```

for...in 文はオブジェクトのプロパティを列挙する際に便利に見えるが、いくつか問題がある。

JavaScriptでは、オブジェクトは何らかのオブジェクトを継承している。for...in 文はターゲットオブジェクトのプロパティを列挙する際に、列挙可能なプロトタイプオブジェクトのプロパティも列挙してしまうため、オブジェクト自身が持っていないプロパティも列挙され、予期しない結果になることがある。

オブジェクトのプロパティを安全に列挙するには、`Object.keys`メソッド、`Object.values`メソッド、`Object.entries`メソッドなどを使用する。

前に提到的で...in 文を使ってオブジェクトのキーと値を列挙するコードは、for...in 文を使わずに書くことができる。`Object.keys`メソッドは、引数のオブジェクト自身の列挙可能なプロパティ名を含む配列を返す。したがって、for...in 文とは異なり、プロトタイプオブジェクトのプロパティを列挙することはない。

```
const obj = {
    "a": 1,
    "b": 2,
    "c": 3
};
Object.keys(obj).forEach(key => {
    const value = obj[key];
    console.log(`key:${key}, value:${value}`);
});
// "key:a, value:1"
// "key:b, value:2"
// "key:c, value:3" 
```

さらに、for...in 文は配列にも使用できるが、結果が期待通りにならない可能性がある。

次のコードでは、配列の要素を列挙しているように見えるが、実際には配列のプロパティ名を列挙している。for...in 文が列挙する配列オブジェクトのプロパティ名は、要素インデックスの文字列形式である"0"、"1"などであり、これらが順に`num`に代入される。したがって、数値と文字列の加算は期待通りの結果にならない。

```
const numbers = [5, 10];
let total = 0;
for (const num in numbers) {
    // 0 + "0" + "1" という文字列結合が行われる
    total += num;
}
console.log(total); // => "001" 
```

配列の内容をイテレーションする必要がある場合は、for ループ、`forEach`メソッド、または後で紹介する for...of 文を使用するべきである。

このように、for...in 文は扱いにくいが、多くの代替手段がある。したがって、for...in 文の使用を避け、`Object.keys`メソッドなどを使って配列をイテレーション対象とするほうがよい。

## [ES2015] for...of 语句

最後に for...of 文について説明する。

JavaScriptでは、`Symbol.iterator`という特殊なメソッドを実装したオブジェクトを**iterable**（イテラブル）と呼ぶ。iterable オブジェクトは、for...of 文でイテレーション処理を行うことができる。

iterable オブジェクトは、イテレーション時に次の値を返すように定義されたオブジェクトの総称である。for...of 文では、iterable オブジェクトから値を取り出し、`variable`に代入してイテレーション処理を行う。

```
for (variable of iterable) {
    実行する文;
} 
```

実際には、iterable オブジェクトとしてすでにArrayが存在する。Arrayはiterable オブジェクトである。

したがって、for...of 文を使って配列から値を取り出し、イテレーション処理を行うことができる。for...in 文とは異なり、for...of 文は配列の値を列挙し、インデックス値は列挙しない。

```
const array = [1, 2, 3];
for (const value of array) {
    console.log(value);
}
// 1
// 2
// 3 
```

さらに、JavaScriptではStringオブジェクトもiterable である。したがって、文字列を1文字ずつ列挙することができる。

```
const str = "𠮷野家";
for (const value of str) {
    console.log(value);
}
// "𠮷"
// "野"
// "家" 
```

また、`TypedArray`、`Map`、`Set`、DOM NodeList など、`Symbol.iterator`を実装したオブジェクトも存在する。for...of 文はこれらのiterable オブジェクトに対してイテレーション処理を行うことができる。

## 总结

この章では、ループ構造（for ループなど）と配列メソッドを使ったイテレーション処理を比較した。ループ構造では continue 文や break 文を使用できるが、配列メソッドでは使用できない。一方、配列メソッドの利点は、一時変数を管理する必要がなく、処理をコールバック関数として記述できる点である。

これらの2つの方法はイテレーション処理でよく使用される。いずれかの方法が絶対的に優れているわけではないため、両方を習得することが重要である。さらに、「配列」章では配列メソッドについて詳しく説明する。

> ¹. `for...in`文によるプロパティの列挙順は、ES2019以前は実装依存であったが、ES2020にて列挙順が確定した。 ↩

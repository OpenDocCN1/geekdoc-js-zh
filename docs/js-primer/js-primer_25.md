
# 関数とthis

> 原文：[`jsprimer.net/basic/function-this/`](https://jsprimer.net/basic/function-this/)

この章では`this`という特殊な動作をするキーワードについて見ていきます。基本的にはメソッドの中で利用しますが、`this`は読み取り専用のグローバル変数のようなものでどこにでも書けます。加えて、`this`の参照先（評価結果）は条件によって異なります。

`this`の参照先は主に次の条件によって変化します。

+   実行コンテキストにおける`this`

+   コンストラクタにおける`this`

+   関数とメソッドにおける`this`

+   Arrow Functionにおける`this`

コンストラクタにおける`this`は、次の章である「クラス」で扱います。この章ではさまざまな条件での`this`について扱いますが、`this`が実際に使われるのはメソッドにおいてです。そのため、あらゆる条件下での`this`の動きをすべて覚える必要はありません。

この章では、さまざまな条件下で変わる`this`の参照先と関数やArrow Functionとの関係を見ていきます。また、実際にどのような状況で問題が発生するかを知り、`this`の動きを予測可能にするにはどのようにするかを見ていきます。

## 実行コンテキストと`this`

最初に「JavaScriptとは」の章において、JavaScriptには実行コンテキストとして"Script"と"Module"があるという話をしました。どの実行コンテキストでJavaScriptのコードを評価するかは、実行環境によってやり方が異なります。この章では、ブラウザの`script`要素と`type`属性を使い、それぞれの実行コンテキストを明示しながら`this`の動きを見ていきます。

トップレベル（もっとも外側のスコープ）にある`this`は、実行コンテキストによって値が異なります。実行コンテキストの違いは意識しにくい部分であり、トップレベルで`this`を使うと混乱を生むことになります。そのため、コードのトップレベルにおいては`this`を使うべきではありませんが、それぞれの実行コンテキストにおける動作を紹介します。

### スクリプトにおける`this`

実行コンテキストが"Script"である場合、トップレベルのスコープに書かれた`this`はグローバルオブジェクトを参照します。グローバルオブジェクトは、実行環境ごとに異なるものが定義されています。ブラウザのグローバルオブジェクトは`window`オブジェクト、Node.jsのグローバルオブジェクトは`global`オブジェクトとなります。

ブラウザでは、`script`要素の`type`属性を指定していない場合は、実行コンテキストが"Script"として実行されます。この`script`要素の直下に書いた`this`はグローバルオブジェクトである`window`オブジェクトとなります。

```
<script> // 実行コンテキストは"Script"
console.log(this); // => window </script> 
```

### モジュールにおける`this`

実行コンテキストが"Module"である場合、そのトップレベルのスコープに書かれた`this`は常に`undefined`となります。

ブラウザで、`script`要素に`type="module"`属性がついた場合は、実行コンテキストが"Module"として実行されます。この`script`要素の直下に書いた`this`は`undefined`となります。

```
<script type="module"> // 実行コンテキストは"Module"
console.log(this); // => undefined </script> 
```

このように、トップレベルのスコープの`this`は実行コンテキストによって`undefined`となる場合があります。

単純にグローバルオブジェクトを参照したい場合は、`this`ではなく`globalThis`を使います。`globalThis`は実行環境のグローバルオブジェクトを参照するためにES2020で導入されました。

実行環境のグローバルオブジェクトは、ブラウザでは`window`、Node.jsでは`global`のように名前が異なります。そのため同じコードで、異なるグローバルオブジェクトを参照するには、コード上で分岐する必要がありました。ES2020ではこの問題を解決するために、実行環境のグローバルオブジェクトを参照する`globalThis`が導入されました。

```
// ブラウザでは`window`オブジェクト、Node.jsでは`global`オブジェクトを参照する
console.log(globalThis); 
```

## 関数とメソッドにおける`this`

関数を定義する方法として、`function`キーワードによる関数宣言と関数式、Arrow Functionなどがあります。`this`が参照先を決めるルールは、Arrow Functionとそれ以外の関数定義の方法で異なります。

そのため、まずは関数定義の種類について振り返ってから、それぞれの`this`について見ていきます。

### 関数の種類

「関数と宣言」の章で詳しく紹介していますが、関数の定義方法と呼び出し方について改めて振り返ってみましょう。**関数**を定義する場合には、次の3つの方法を利用します。

```
// `function`キーワードからはじめる関数宣言
function fn1() {}
// `function`を式として扱う関数式
const fn2 = function() {}
// Arrow Functionを使った関数式
const fn3 = () => {}
```

それぞれ定義した関数は`関数名()`と書くことで呼び出せます。

```
// 関数宣言
function fn() {}
// 関数呼び出し
fn()
```

### メソッドの種類

JavaScriptではオブジェクトのプロパティが関数である場合にそれを**メソッド**と呼びます。一般的にはメソッドも含めたものを**関数**と言い、関数宣言などとプロパティである関数を区別する場合に**メソッド**と呼びます。

メソッドを定義する場合には、オブジェクトのプロパティに関数式を定義するだけです。

```
const obj = {
    // `function`キーワードを使ったメソッド
    method1: function() {
    },
    // Arrow Functionを使ったメソッド
    method2: () => {
    }
}
```

これに加えてメソッドには短縮記法があります。オブジェクトリテラルの中で `メソッド名(){ /*メソッドの処理*/ }`と書くことで、メソッドを定義できます。

```
const obj = {
    // メソッドの短縮記法で定義したメソッド
    method() {
    }
}
```

これらのメソッドは、`オブジェクト名.メソッド名()`と書くことで呼び出せます。

```
const obj = {
    // メソッドの定義
    method() {
    }
}
// メソッド呼び出し
obj.method()
```

関数定義とメソッドの定義についてまとめると、次のようになります。

| 名前 | 関数 | メソッド |
| --- | --- | --- |
| 関数宣言(`function fn(){}`) | ✔ | x |
| 関数式(`const fn = function(){}`) | ✔ | ✔ |
| Arrow Function(`const fn = () => {}`) | ✔ | ✔ |
| メソッドの短縮記法(`const obj = { method(){} }`) | x | ✔ |

最初に書いたように`this`の挙動は、Arrow Functionの関数定義とそれ以外（`function`キーワードやメソッドの短縮記法）の関数定義で異なります。そのため、まずは**Arrow Function 以外**の関数やメソッドにおける`this`を見ていきます。

## 非箭头函数中的`this`

非箭头函数（包括方法）中的`this`在执行时确定其值。换句话说，`this`就像是一个传递给函数的隐含参数，其传递的值在函数执行时确定。

下面的代码是假设性的。函数中写出的`this`将引用函数调用源暗含传递的值。这个规则适用于非箭头函数或方法，箭头函数定义的函数或方法则遵循不同的规则。

```
// 疑似的な`this`の値の仕組み
// 関数は引数として暗黙的に`this`の値を受け取るイメージ
function fn(暗黙的に渡されるthisの値, 仮引数) {
    console.log(this); // => 暗黙的に渡されるthisの値
}
// 暗黙的に`this`の値を引数として渡しているイメージ
fn(暗黙的に渡すthisの値, 引数)
```

函数中的`this`的基本引用点は**基础对象**。基础对象は指“调用方法时，方法点操作符または方括号操作符左边の对象”。如果没有基础对象，`this`は`undefined`。

例えば、当像`fn()`这样调用函数时、由于这个`fn`函数调用没有基础对象、所以`this`は`undefined`。一方、当像`obj.method()`这样调用方法时、この`obj.method`方法调用の基础对象は`obj`オブジェクト、`this`は`obj`。

```
// `fn`関数はメソッドではないのでベースオブジェクトはない
fn()
// `obj.method`メソッドのベースオブジェクトは`obj`
obj.method()
// `obj1.obj2.method`メソッドのベースオブジェクトは`obj2`
// ドット演算子、ブラケット演算子どちらも結果は同じ
obj1.obj2.method()
obj1["obj2"]["method"]()
```

`this`の値は函数定義時に確定されるのではなく、調用時に確定されます。これは后面将要介绍的“`this`引起的问题模式”中详细介绍的内容。非箭头函数中、仅从函数定义来看无法确定`this`的值。

### 函数声明または函数表达式中的`this`

まず、函数声明または函数表达式の情况を見てみましょう。

下面の例では、函数声明で定義された関数`fn1`、函数式で定義された関数`fn2`をそれぞれ定義し、各関数内で`this`を返しています。定義された各関数は`fn1()`や`fn2()`のように通常の関数として呼び出されます。このとき、基底オブジェクトがないため`this`は`undefined`になります。

```
"use strict";
function fn1() {
    return this;
}
const fn2 = function() {
    return this;
};
// 関数の中の`this`が参照する値は呼び出し方によって決まる
// `fn1`と`fn2`どちらもただの関数として呼び出している
// メソッドとして呼び出していないためベースオブジェクトはない
// ベースオブジェクトがない場合、`this`は`undefined`となる
console.log(fn1()); // => undefined
console.log(fn2()); // => undefined
```

これは、関数内で関数を定義して呼び出す場合にも同様に適用されます。

```
"use strict";
function outer() {
    console.log(this); // => undefined
    function inner() {
        console.log(this); // => undefined
    }
    // `inner`関数呼び出しのベースオブジェクトはない
    inner();
}
// `outer`関数呼び出しのベースオブジェクトはない
outer()
```

この本のコードでは、コメントがない場合は strict mode とみなします。ただし、コード例では明示的に `"use strict";` を記述して strict mode であることを示しています（「JavaScriptとは」の章の strict mode を参照）。これは、strict mode でない場合、`this` が `undefined` のときにグローバルオブジェクトを参照する値に変換されるためです。

strict mode は、このような予測不能な動作を防ぐために導入されました。しかし、strict mode 以外の関数における `this` は `undefined` になるため、実用的ではありません。したがって、メソッド以外では `this` を使う必要はありません。

### メソッド呼び出しにおける`this`

次に、メソッドの場合を見てみましょう。メソッドの場合、そのメソッドは特定のオブジェクトに属しています。これは、JavaScript でオブジェクトのプロパティとして関数が定義されている場合、それをメソッドと呼ぶからです。

下面の例では、`method1` と `method2` がそれぞれメソッドとして呼び出されています。このとき、各ベースオブジェクトは `obj` であり、`this` も `obj` を参照しています。

```
const obj = {
    // 関数式をプロパティの値にしたメソッド
    method1: function() {
        return this;
    },
    // 短縮記法で定義したメソッド
    method2() {
        return this;
    }
}
// メソッド呼び出しの場合、それぞれの`this`はベースオブジェクト(`obj`)を参照する
// メソッド呼び出しの`.`の左にあるオブジェクトがベースオブジェクト
console.log(obj.method1()); // => obj
console.log(obj.method2()); // => obj
```

これにより、`this` を使って同じオブジェクト内の他のプロパティを参照することができます。

```
const person = {
    fullName: "Brendan Eich",
    sayName: function() {
        // `person.fullName`と書いているのと同じ
        return this.fullName;
    }
}
// `person.fullName`を出力する
console.log(person.sayName()); // => "Brendan Eich"
```

こうすることで、`this.プロパティ名` と `オブジェクト名.プロパティ名` を置き換えて、メソッドが属するオブジェクトのプロパティを参照することができます。

オブジェクトはネストできるが、`this` がベースオブジェクトを参照するルールは変わらない。

次のコードを見てみると、ネストされたオブジェクト内のメソッドにおける `this` は、最も内側のオブジェクト `obj3` を参照していることがわかる。このときのベースオブジェクトは、ドットでつながれた最左の `obj1` ではなく、メソッドから見て左側の `obj3` である。

```
const obj1 = {
    obj2: {
        obj3: {
            method() {
                return this;
            }
        }
    }
}
// `obj1.obj2.obj3.method`メソッドの`this`は`obj3`を参照
console.log(obj1.obj2.obj3.method() === obj1.obj2.obj3); // => true
```

## `this`引起的问题模式

これまで、`this` が関数（メソッドを含む）の呼び出し元のベースオブジェクトを参照することを確認してきました。`this` は所属オブジェクトを参照するための置き換えとして使えるが、さまざまな問題も引き起こす。

この問題の原因は、`this` が参照する値が関数呼び出し時に決まることである。以下では、問題を引き起こす主なパターンとその対処法について詳しく見ていく。

### 問題：`this` を含む関数を変数に代入するとき

JavaScript では、メソッドとして定義された関数が一時的に通常の関数として呼び出されることがある。これは、メソッドがオブジェクトのプロパティとして関数を保持しており、そのプロパティが変数に再代入されるためである。

したがって、メソッドとして定義された関数も、別の変数に代入して通常の関数として呼び出すことができる。このとき、メソッドとして定義された関数でも、通常の関数として実行されるため、ベースオブジェクトが変わる。これは、`this` が定義時ではなく実行時に決まる性質によるものである。

具体的には、`this` が実行時に変わる例を見てみよう。以下の例では、`person.sayName` メソッドを変数 `say` に代入した後、それを呼び出している。このとき、`say` 関数（`sayName` メソッドへの参照）にはベースオブジェクトがない。したがって、`this` は `undefined` となり、`undefined.fullName` を参照しようとして例外が発生する。

```
"use strict";
const person = {
    fullName: "Brendan Eich",
    sayName: function() {
        // `this` は呼び出し元によって異なる
        return this.fullName;
    }
}
// `sayName` メソッドは `person` オブジェクトに所属する
// `this` は `person` オブジェクトとなる
console.log(person.sayName()); // => "Brendan Eich"
// `person.sayName` を `say` 変数に代入する
const say = person.sayName;
// 代入したメソッドを関数として呼ぶ
// この `say` 関数はどのオブジェクトにも所属していない
// `this` は `undefined` となるため例外を投げる
say(); // => TypeError: Cannot read property 'fullName' of undefined
```

最終的に実行されるコードは、以下のようになる。以下のコードでは、`undefined.fullName` を参照しようとして例外が発生する。

```
"use strict";
// const say = person.sayName; は次のようなイメージ
const say = function() {
    return this.fullName;
};
// `this` は `undefined` となるため例外を投げる
say(); // => TypeError: Cannot read property 'fullName' of undefined
```

このように、Arrow Function 以外の関数では、`this` は定義時ではなく実行時に決まる。したがって、`this` を含む関数が予期せぬ呼び出し方をされた場合、誤った結果を返すことになる。

この問題を解決する主な方法は2つある。

1つ目は、メソッドとして定義された関数をメソッドとして呼び出すことである。メソッドを通常の関数として呼び出さなければ、この問題は発生しない。

2つ目は、`this` の値を指定して関数を呼び出す方法である。

#### 解決方法：`call`、`apply`、`bind` メソッド

関数またはメソッドの `this` を明示的に指定して呼び出す方法として、`Function`（関数オブジェクト）が提供する `call`、`apply`、`bind` メソッドがある。

`call` メソッドは、第1引数に `this` として使う値を指定し、残りの引数を呼び出す関数に渡す引数とする。つまり、`call` メソッドは `this` の値を明示的に渡すことができるメソッドである。

```
関数.call(thisの値, ...関数の引数);
```

以下の例では、`person` オブジェクトを `this` として指定して `say` 関数を呼び出している。`call` メソッドの第2引数は、`say` 関数の引数 `message` に渡される。

```
"use strict";
function say(message) {
    return `${message} ${this.fullName}！`;
}
const person = {
    fullName: "Brendan Eich"
};
// `this` を `person` にして `say` 関数を呼びだす
console.log(say.call(person, "こんにちは")); // => "こんにちは Brendan Eich！"
// `say` 関数をそのまま呼び出すと `this` は `undefined` となるため例外が発生
say("こんにちは"); // => TypeError: Cannot read property 'fullName' of undefined
```

`apply` メソッドは、第1引数に `this` として使う値を指定し、第2引数を関数の引数として渡す配列とする。

```
関数.apply(thisの値, [関数の引数 1, 関数の引数 2]);
```

以下の例では、`person` オブジェクトを `this` として指定して `say` 関数を呼び出している。`apply` メソッドの第2引数は配列として渡され、関数内で展開されて `say` 関数の引数 `message` に渡される。

```
"use strict";
function say(message) {
    return `${message} ${this.fullName}！`;
}
const person = {
    fullName: "Brendan Eich"
};
// `this` を `person` にして `say` 関数を呼びだす
// call とは異なり引数を配列として渡す
console.log(say.apply(person, ["こんにちは"])); // => "こんにちは Brendan Eich！"
// `say` 関数をそのまま呼び出すと `this` は `undefined` となるため例外が発生
say("こんにちは"); // => TypeError: Cannot read property 'fullName' of undefined
```

`call` メソッドと `apply` メソッドの違いは、関数に引数を渡す方法のみである。さらに、`this` の値が不要な場合は、両方のメソッドに `null` を渡すことが一般的である。

```
function add(x, y) {
    return x + y;
}
// `this` が不要な場合は、null を渡す
console.log(add.call(null, 1, 2)); // => 3
console.log(add.apply(null, [1, 2])); // => 3
```

最後に `bind` メソッドについて説明する。名前の通り、`bind` メソッドは `this` の値を束縛した新しい関数を作成する。

```
関数.bind(thisの値, ...関数の引数); // => this や引数が束縛された関数
```

以下の例では、`person` オブジェクトに `this` を束縛した `say` 関数をラップした関数を作成している。`bind` メソッドの第2引数以降に値を渡すことで、関数の引数を束縛することができる。

```
function say(message) {
    return `${message} ${this.fullName}！`;
}
const person = {
    fullName: "Brendan Eich"
};
// `this` を `person` に束縛した `say` 関数をラップした関数を作る
const sayPerson = say.bind(person, "こんにちは");
console.log(sayPerson()); // => "こんにちは Brendan Eich！"
```

この `bind` メソッドを通常の関数として表すと以下のようになる。これにより、`bind` が `this` と引数を束縛した関数を作成するメソッドであることがわかる。

```
function say(message) {
    return `${message} ${this.fullName}！`;
}
const person = {
    fullName: "Brendan Eich"
};
// `this` を `person` に束縛した `say` 関数をラップした関数を作る
//  say.bind(person, "こんにちは"); は次のようなラップ関数を作る
const sayPerson = () => {
    return say.call(person, "こんにちは");
};
console.log(sayPerson()); // => "こんにちは Brendan Eich！"
```

`call`、`apply`、`bind` メソッドを使うことで、`this` の値を明示的に指定して関数を呼び出すことができる。しかし、関数を呼び出すたびにこれらのメソッドを使うと、関数を呼び出すために関数を呼び出すことになり、煩雑になる。したがって、基本的には「メソッドとして定義された関数をメソッドとして呼び出す」ことが最善の方法である。その中で、本当に `this` を固定する必要がある場合は、`call`、`apply`、`bind` メソッドを使う。

### 問題：コールバック関数と `this`

コールバック関数内で `this` を参照すると問題が発生することがある。この問題は、配列の `map` メソッドなどのコールバック処理で起こりやすい。

以下に具体的な例を示す。以下のコードでは、`prefixArray` メソッド内で `map` メソッドを使用している。このとき、`map` メソッドのコールバック関数内で `this` を参照して `Prefixer` オブジェクトを参照しようとしている。

しかし、このコールバック関数内では `this` が `undefined` となるため、`undefined.prefix` を参照しようとして `TypeError` 例外が発生する。

```
"use strict";
// strict mode を明示しているのは、this がグローバルオブジェクトに暗黙的に変換されるのを防止するため
const Prefixer = {
    prefix: "pre",
    /**
     * `strings` 配列の各要素に prefix をつける
     */
    prefixArray(strings) {
        return strings.map(function(str) {
            // コールバック関数における `this` は `undefined` となる（strict mode）
            // そのため `this.prefix` は `undefined.prefix` となり例外が発生する
            return this.prefix + "-" + str;
        });
    }
};
// `prefixArray` メソッドにおける `this` は `Prefixer`
Prefixer.prefixArray(["a", "b", "c"]); // => TypeError: Cannot read property 'prefix' of undefined
```

コールバック関数内の `this` が `undefined` となる理由を見てみよう。配列の `map` メソッドは、シーン内で定義された無名関数をコールバック関数として渡している。

```
// ...
    prefixArray(strings) {
        // 無名関数をコールバック関数として渡している
        return strings.map(function(str) {
            return this.prefix + "-" + str;
        });
    }
// ...
```

このとき、配列の `map` メソッドに渡されたコールバック関数は、`callback()` と同じように通常の関数として呼び出される。つまり、コールバック関数を呼び出すとき、その関数にはベースオブジェクトがない。したがって、コールバック関数の `this` は `undefined` となる。

前述の例では、無名関数を直接コールバック関数として渡していたが、これを `callback` 変数に格納してから渡しても同じ結果となる。

```
"use strict";
// strict mode を明示しているのは、this がグローバルオブジェクトに暗黙的に変換されるのを防止するため
const Prefixer = {
    prefix: "pre",
    prefixArray(strings) {
        // コールバック関数は `callback()` のように呼び出される
        // そのためコールバック関数における `this` は `undefined` となる（strict mode）
        const callback = function(str) {
            return this.prefix + "-" + str;
        };
        return strings.map(callback);
    }
};
// `prefixArray` メソッドにおける `this` は `Prefixer`
Prefixer.prefixArray(["a", "b", "c"]); // => TypeError: Cannot read property 'prefix' of undefined
```

#### 解決方法：`this` を一時変数に代入する

コールバック関数内の `this` が変化する問題の解決策は、`this` を別の変数に代入してその参照を保持することである。

`this` の値は呼び出し元で変化し、その呼び出し元のベースオブジェクトを参照する。`prefixArray` メソッドを呼び出すとき、`this` は `Prefixer` オブジェクトを参照している。しかし、コールバック関数が通常の関数として呼び出されるため、`this` が `undefined` となり問題が発生する。

したがって、`prefixArray` メソッド呼び出し時の `this` を参照を一時変数に保存することで、この問題を回避できる。以下のコードでは、`prefixArray` メソッドの `this` を `that` 変数に保存している。コールバック関数内で `this` の代わりに `that` を参照することで、コールバック関数は `prefixArray` メソッド呼び出し時の `this` と同じ参照を保つことができる。

```
"use strict";
const Prefixer = {
    prefix: "pre",
    prefixArray(strings) {
        // `that` は `prefixArray` メソッド呼び出しにおける `this` となる
        // つまり `that` は `Prefixer` オブジェクトを参照する
        const that = this;
        return strings.map(function(str) {
            // `this` ではなく `that` を参照する
            return that.prefix + "-" + str;
        });
    }
};
// `prefixArray` メソッドにおける `this` は `Prefixer`
const prefixedStrings = Prefixer.prefixArray(["a", "b", "c"]);
console.log(prefixedStrings); // => ["pre-a", "pre-b", "pre-c"]
```

もちろん、`Function` の `call` メソッドなどを使って `this` を明示的に渡して関数を呼び出すこともできる。さらに、配列の `map` メソッドなどは第2引数に `this` となる値を渡す仕組みを持っている。したがって、第2引数に `this` の値を渡すことでもこの問題を解決できる。

```
"use strict";
const Prefixer = {
    prefix: "pre",
    prefixArray(strings) {
        // Array の `map` メソッドは第2引数に `this` となる値を渡せる
        return strings.map(function(str) {
            // `this` が第2引数の値と同じになる
            // つまり `prefixArray` メソッドと同じ `this` となる
            return this.prefix + "-" + str;
        }, this);
    }
};
// `prefixArray` メソッドにおける `this` は `Prefixer`
const prefixedStrings = Prefixer.prefixArray(["a", "b", "c"]);
console.log(prefixedStrings); // => ["pre-a", "pre-b", "pre-c"]
```

ただし、これらの解決策はコールバック関数内の `this` の変化に気を配る必要がある。問題の根本は、メソッド呼び出しとその中のコールバック関数における `this` の変化にある。ES2015 では、この問題を解決するために `this` を変更しないコールバック関数の定義方法として Arrow Function が導入された。

#### 対処法: Arrow Function でコールバック関数を扱う

通常の関数やメソッドは呼び出し時に暗黙的に `this` の値を受け取り、関数内の `this` はその値を参照する。一方、Arrow Function はこの暗黙的な `this` の値を受け取らない。そのため、Arrow Function 内の `this` は、スコープチェーンの仕組みと同様に外側の関数（この場合は `prefixArray` メソッド）を探索する。これにより、Arrow Function で定義されたコールバック関数は呼び出し方に関係なく、常に外側の関数の `this` をそのまま利用する。

Arrow Function を使うことで、前述のコードは次のように書ける。

```
"use strict";
const Prefixer = {
    prefix: "pre",
    prefixArray(strings) {
        return strings.map((str) => {
            // Arrow Function 自体は `this` を持たない
            // `this` は外側の `prefixArray` 関数が持つ `this` を参照する
            // そのため `this.prefix` は "pre" となる
            return this.prefix + "-" + str;
        });
    }
};
// このとき、`prefixArray` のベースオブジェクトは `Prefixer` となる
// つまり、`prefixArray` メソッド内の `this` は `Prefixer` を参照する
const prefixedStrings = Prefixer.prefixArray(["a", "b", "c"]);
console.log(prefixedStrings); // => ["pre-a", "pre-b", "pre-c"]
```

このように、Arrow Function で定義されたコールバック関数における `this` は簡潔である。コールバック関数内での `this` の対処法として `this` を一時変数に代入する方法を紹介したが、ES2015 からは Arrow Function を使うのが最も簡潔である。

この Arrow Function と `this` の関係について詳しく見ていく。

## Arrow Function と `this`

Arrow Function で定義された関数やメソッドにおける `this` が参照する値は、関数の定義時（静的）に決まる。一方、Arrow Function 以外の関数における `this` は、呼び出し元に依存するため、関数の実行時（動的）に決まる。

Arrow Function とそれ以外の関数で大きく異なる点は、Arrow Function は `this` を暗黙的な引数として受け取らないことである。そのため、Arrow Function 内には `this` が定義されていない。このときの `this` は、外側のスコープ（関数）の `this` を参照する。

これは変数におけるスコープチェーンの仕組みと同じであり、そのスコープ内に `this` が定義されていない場合は、外側のスコープを探索する。したがって、Arrow Function 内の `this` は、常に外側のスコープ（関数）における `this` の定義を探索する（スコープチェーンについては「スコープチェーン」を参照）。さらに、`this` は ECMAScript のキーワードであるため、ユーザーは `this` という名前の変数を定義することはできない。

```
// this はキーワードであるため、ユーザーは `this` という名前の変数を定義できない
const this = "thisは読み取り専用"; // => SyntaxError: Unexpected token this
```

したがって、`this` の参照は通常の変数と同じく、定義時（静的）に決まる（詳細については「静的スコープ」を参照）。つまり、Arrow Function 内の `this` は「Arrow Function 自身の外側における最も近い関数の `this` の値」を参照する。

それでは、Arrow Function 内の `this` の動きを具体的に見てみよう。

まずは、関数式における Arrow Function から見ていく。

以下の例では、関数式で Arrow Function を定義し、その中で `this` を出力している。このとき、`fn` の外側には関数が存在しないため、「自身の外側における最も近い関数」の条件を満たすものはない。この場合、`this` の値はトップレベルで定義された `this` と同じとなる。

```
// Arrow Function で定義した関数
const fn = () => {
    // この関数の外側には関数は存在しない
    // トップレベルの `this` と同じ値
    return this;
};
console.log(fn() === this); // => true
```

これまで紹介してきたように、トップレベルで定義された `this` の値は実行コンテキストによって異なる。実行コンテキストが "Script" の場合はグローバルオブジェクト、"Module" の場合は `undefined` となる。

次に、通常の関数で Arrow Function を包む例を見てみよう。このとき、Arrow Function 内の `this` は「自身の外側におけるより近い関数の `this` の値」となり、先ほどの場合と同じ結果となる。

```
"use strict";
function outer() {
    // Arrow Function で定義した関数を返す
    return () => {
        // この関数の外側には `outer` 関数が存在する
        // `outer` 関数に `this` を書いた場合と同じ
        return this;
    };
}
// `outer` 関数の返り値は Arrow Function で定義された関数
const innerArrowFunction = outer();
console.log(innerArrowFunction()); // => undefined
```

つまり、この Arrow Function 内の `this` の値は、`outer` 関数内で `this` を参照したときと同じ値となる。

```
"use strict";
function outer() {
    // `outer` 関数直下の `this`
    const that = this;
    // Arrow Function で定義した関数を返す
    return () => {
        // Arrow Function 自身は `this` を持たない
        // `outer` 関数に `this` を書いた場合と同じ
        return that;
    };
}
// `outer()` 呼び出し時の `this` は `undefined`（strict mode）
const innerArrowFunction = outer();
console.log(innerArrowFunction()); // => undefined
```

### メソッドとコールバック関数における Arrow Function

メソッド内でコールバック関数を使用するのは、Arrow Function を効果的に使うパターンの一つである。`function` キーワードでコールバック関数を定義する場合は、コールバック関数の呼び出し方に注意する必要がある。なぜなら、`function` キーワードで定義された関数における `this` の値は、呼び出し方によって変化するからである。

コールバック関数の観点から見ると、呼び出し方によって `this` の値が変化するため、`this` を使うことはできない。したがって、これまで紹介してきたように、外側のスコープで `this` を一時変数に代入して参照を保持する方法をとってきた。

```
// `callback` 関数を受け取り呼び出す関数
const callCallback = (callback) => {
    // `callback` を呼び出す実装
};

const obj = {
    method() {
        callCallback(function() {
            // ここでの `this` は `callCallback` の実装に依存する
            // `callback()` のように単純に呼び出されるなら `this` は `undefined` になる
            // Function の `call` メソッドなどを使って特定のオブジェクトを指定するかもしれない
            // この問題を回避するために `const that = this` のような一時変数を使う
        });
    }
};
```

一方、Arrow Function でコールバック関数を定義する場合は、外側の関数における `this` を参照する。このとき、Arrow Function で定義されたコールバック関数における `this` は、呼び出し方によって変化しない。したがって、`const that = this` のような一時変数を使う必要はない。

```
// `callback` 関数を受け取り呼び出す関数
const callCallback = (callback) => {
    // `callback` を呼び出す実装
};

const obj = {
    method() {
        callCallback(() => {
            // ここでの `this` は 1 つ外側の関数における `this` と同じ
        });
    }
};
```

この Arrow Function 内の `this` は呼び出し方によって変化しない。つまり、コールバック関数の呼び出し方を気にせずに `this` を扱うことができる。

```
const Prefixer = {
    prefix: "pre",
    prefixArray(strings) {
        return strings.map((str) => {
            // `Prefixer.prefixArray()` と呼び出されたとき
            // `this` は常に `Prefixer` を参照する
            return this.prefix + "-" + str;
        });
    }
};
const prefixedStrings = Prefixer.prefixArray(["a", "b", "c"]);
console.log(prefixedStrings); // => ["pre-a", "pre-b", "pre-c"]
```

### Arrow Function は `this` を束縛できない

Arrow Function で定義された関数において、`call`、`apply`、`bind` メソッドを使って `this` を指定しても、その動作は無視される。これは、Arrow Function には `this` が存在しないからである。

以下のように、`call` メソッドを使って Arrow Function で定義された関数の `this` を `{}` に指定しても、`this` の参照は変わらない。同様に、`apply` や `bind` メソッドを使っても `this` の参照は変わらない。

```
const fn = () => {
    return this;
};
// Script コンテキストの場合、スクリプト直下の Arrow Function の `this` はグローバルオブジェクト
console.log(fn()); // グローバルオブジェクト
// call で `this` を `{}` にしようとしても、`this` は変わらない
console.log(fn.call({})); // グローバルオブジェクト
```

前述のように、`function` キーワードで定義された関数は呼び出し時にベースオブジェクトを `this` の値として暗黙的に受け取る。一方、Arrow Function は呼び出し時に `this` を受け取らず、`this` の参照は定義時に静的に決まる。

さらに、`this` は Arrow Function で定義された関数においてのみ変化せず、Arrow Function 内の `this` は「最も外側のスコープにおける最も近い関数の `this` の値」を参照する。この `this` の参照は、`call` メソッドを使って変更することができる。

```
const obj = {
    method() {
        const arrowFunction = () => {
            return this;
        };
        return arrowFunction();
    }
};
// 通常の `this` は `obj.method` の `this` と同じ
console.log(obj.method()); // => obj
// `obj.method` の `this` を変更すれば、Arrow Function の `this` も変更される
console.log(obj.method.call("THAT")); // => "THAT"
```

## まとめ

`this` は状況によって参照する値が変化するキーワードである。以下は、`this` の評価結果についてのまとめである。

| 実行上下文 | 严格模式 | コード | `this` の評価結果 |
| --- | --- | --- | --- |
| Script | ＊ | `this` | `globalThis` |
| Script | ＊ | `const fn = () => this` | `globalThis` |
| Script | NO | `const fn = function(){ return this; }` | `globalThis` |
| Script | YES | `const fn = function(){ return this; }` | `undefined` |
| Script | ＊ | `const obj = { method: () => { return this; } }` | `globalThis` |
| Module | YES | `this` | `undefined` |
| Module | YES | `const fn = () => this` | `undefined` |
| Module | YES | `const fn = function(){ return this; }` | `undefined` |
| Module | YES | `const obj = { method: () => { return this; } }` | `undefined` |
| ＊ | ＊ | `const obj = { method(){ return this; } }` | `obj` |
| ＊ | ＊ | `const obj = { method: function(){ return this; } }` | `obj` |

> ＊ はどのような状況でも `this` の評価結果に影響しないことを示す。

実際にブラウザで動作させた結果は、[JavaScript 中の `this` の値とは](https://azu.github.io/what-is-this/) で確認できる。

`this` は JavaScript におけるオブジェクト指向プログラミングの概念として導入されたキーワードである。メソッド以外でも `this` を評価することは可能だが、実行上下文や strict mode などの要因により結果が変化し、混乱を招くことがある。したがって、メソッド以外の関数では `this` を使わないことが望ましい。¹

さらに、メソッドにおいては `this` の値が呼び出し方によって変化し、それによって生じる問題とその対処法について説明した。コールバック関数における `this` の問題は、Arrow Function を使うことでより明確に解決できる。これは、Arrow Function で定義された関数には `this` が存在しないためである。

> ¹. ES2015 の規格編集者である Allen Wirfs-Brock 氏も、通常の関数において `this` を使うべきではないと述べている。[twitter.com/awbjs/status/938272440085446657](https://twitter.com/awbjs/status/938272440085446657); ↩

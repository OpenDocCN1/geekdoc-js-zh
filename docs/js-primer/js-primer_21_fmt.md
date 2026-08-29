
# 文字列

> 原文：[`jsprimer.net/basic/string/`](https://jsprimer.net/basic/string/)

この章ではJavaScriptにおける文字列について学んでいきます。まずは、文字列の作成方法や文字列の操作方法について見ていきます。そして、文字列を編集して自由に文字列を作れるようになることがこの章の目的です。

## 文字列を作成する

文字列を作成するには、文字列リテラルを利用します。「データ型とリテラル」の章でも紹介しましたが、文字列リテラルには`"`（ダブルクォート）、`'`（シングルクォート）、```（バッククォート）の3 種類があります。

まずは`"`（ダブルクォート）と`'`（シングルクォート）について見ていきます。

`"`（ダブルクォート）と`'`（シングルクォート）に意味的な違いはありません。そのため、どちらを使うかは好みやプロジェクトごとのコーディング規約によって異なります。この書籍では、`"`（ダブルクォート）を主な文字列リテラルとして利用します。

```javascript
const double = "文字列";

console.log(double); // => "文字列"

const single = '文字列';

console.log(single); // => '文字列'

// どちらも同じ文字列

console.log(double === single);// => true
```

ES2015では、テンプレートリテラル ```（バッククォート）が追加されました。```（バッククォート）を利用することで文字列を作成できる点は、他の文字列リテラルと同じです。

これに加えてテンプレートリテラルでは、文字列中に改行を入力できます。次のコードでは、テンプレートリテラルを使って複数行の文字列を見た目どおりに定義しています。

```javascript
const multiline = `1 行目

2 行目

3 行目`;

// \n は改行を意味する

console.log(multiline); // => "1 行目\n2 行目\n3 行目"
```

どの文字列リテラルでも共通ですが、文字列リテラルは同じ記号が対になります。そのため、文字列の中にリテラルと同じ記号が出現した場合は、`\`（バックスラッシュ）を使いエスケープする必要があります。次のコードでは、文字列中の`"`を`\"`のようにエスケープしています。

```javascript
const str = "This book is \"js-primer\"";

console.log(str); // => 'This book is "js-primer"'
```

## エスケープシーケンス

文字列リテラル中にはそのままでは入力できない特殊な文字もあります。改行もそのひとつで、`"`（ダブルクォート）と`'`（シングルクォート）の文字列リテラルには改行をそのまま入力できません（テンプレートリテラル中には例外的に改行をそのまま入力できます）。

次のコードは、JavaScriptの構文として正しくないため、構文エラー（SyntaxError）となります。

```javascript
// JavaScriptエンジンが構文として解釈できないため、SyntaxErrorとなる

const invalidString = "1 行目

2 行目

3 行目";
```

この問題を回避するためには、改行のような特殊な文字をエスケープシーケンスとして書く必要があります。エスケープシーケンスは、`\`と特定の文字を組み合わせることで、特殊文字を表現します。

次の表では、代表的な[エスケープシーケンス](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String#%E3%82%A8%E3%82%B9%E3%82%B1%E3%83%BC%E3%83%97%E3%82%B7%E3%83%BC%E3%82%B1%E3%83%B3%E3%82%B9)を紹介しています。エスケープシーケンスは、`"`（ダブルクォート）、`'`（シングルクォート）、```（バッククォート）すべての文字列リテラルの中で利用できます。

| エスケープシーケンス | 意味 |
| --- | --- |
| `\'` | シングルクォート |
| `\"` | ダブルクォート |
| `\`` | バッククォート |
| `\\` | バックスラッシュ(`\`そのものを表示する) |
| `\n` | 改行 |
| `\t` | タブ |
| `\uXXXX` | Code Unit(`\u`と4 桁のHexDigit) |
| `\u{X}` ... `\u{XXXXXX}` | Code Point（`\u{}`のカッコ中にHexDigit） |

このエスケープシーケンスを利用することで、先ほどの`"`（ダブルクォート）の中に改行（`\n`）を入力できます。

```javascript
// 改行を\nのエスケープシーケンスとして入力している

const multiline = "1 行目\n2 行目\n3 行目";

console.log(multiline); 

/* 改行した結果が出力される

1 行目

2 行目

3 行目

*/ 
```

また、`\`からはじまる文字は自動的にエスケープシーケンスとして扱われます。しかし、`\a`のように定義されていないエスケープシーケンスは、`\`が単に無視され`a`という文字列として扱われます。これにより、`\`（バックスラッシュ）そのものを入力していたつもりが、その文字がエスケープシーケンスとして扱われてしまう問題があります。

次のコードでは、`\_`という組み合わせのエスケープシーケンスはないため、`\`が無視された文字列として評価されます。

```javascript
console.log("¯\_(ツ)_/¯");

// ¯_(ツ)_/¯ のように\が無視されて表示される 
```

`\`（バックスラッシュ）そのものを入力したい場合は、`\\`のようにエスケープする必要があります。

```javascript
console.log("¯\\_(ツ)_/¯");

//　¯\_(ツ)_/¯ と表示される 
```

## 文字列を結合する

文字列を結合する簡単な方法は文字列結合演算子（`+`）を使う方法です。

```javascript
const str = "a" + "b";

console.log(str); // => "ab" 
```

変数と文字列を結合したい場合も文字列結合演算子で行えます。

```javascript
const name = "JavaScript";

console.log("Hello " + name + "!");// => "Hello JavaScript!" 
```

特定の書式に文字列を埋め込むには、テンプレートリテラルを使うとより宣言的に書けます。

テンプレートリテラル中に`${変数名}`で書かれた変数は評価時に展開されます。つまり、先ほどの文字列結合は次のように書けます。

```javascript
const name = "JavaScript";

console.log(`Hello ${name}!`);// => "Hello JavaScript!" 
```

## 文字へのアクセス

文字列の特定の位置にある文字にはインデックスを指定してアクセスできます。これは、配列における要素へのアクセスにインデックスを指定するのと同じです。

文字列では`文字列[インデックス]`のように指定した位置（インデックス）の文字へアクセスできます。インデックスの値は`0`以上`2⁵³ - 1`未満の整数が指定できます。

```javascript
const str = "文字列";

// 配列と同じようにインデックスでアクセスできる

console.log(str[0]); // => "文"

console.log(str[1]); // => "字"

console.log(str[2]); // => "列" 
```

また、存在しないインデックスへのアクセスでは配列やオブジェクトと同じように`undefined`を返します。

```javascript
const str = "文字列";

// 42 番目の要素は存在しない

console.log(str[42]); // => undefined 
```

### *[ES2022] `String.prototype.at`*

ES2022から`String.prototype.at`メソッドが追加されています。Stringの`at`メソッドは、Arrayの`at`メソッドと同じく、相対的なインデックスを渡してその位置の文字へアクセスできます。`at`メソッドへ`-1`のようにマイナスのインデックスを渡した場合は、末尾から数えた位置の文字へアクセスできます。

```javascript
const str = "文字列";

console.log(str.at(0)); // => "文"

console.log(str.at(1)); // => "字"

console.log(str.at(2)); // => "列"

console.log(str.at(-1)); // => "列" 
```

## 文字列とは

今まで何気なく「文字列」という言葉を利用していましたが、ここでいう文字列とはどのようなものでしょうか？　コンピュータのメモリ上に文字列の「ア」といった文字をそのまま保存できないため、0と1からなるビット列へ変換する必要があります。この文字からビット列へ変換することを符号化（エンコード）と呼びます。

一方で、変換後のビット列が何の文字なのかを管理する表が必要になります。この文字に対応するIDの一覧表のことを符号化文字集合と呼びます。

次の表は、Unicodeという文字コードにおける符号化文字集合からカタカナの一部分を取り出したものです。¹ Unicodeはすべての文字に対してID（Code Point）を振ることを目的に作成されている仕様です。

|  | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | A | B | C | D | E | F |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 30A0 | ら | り | り | り | り | り | り | り | り | り | り | り | り | り | り | り |
| 30B0 | れ | む | め | ろ | ろ | ろ | ろ | ろ | ろ | ろ | ろ | ろ | ろ | ろ | ろ | ろ |
| 30C0 | ダ | チ | ヂ | ッ | ��� | ヅ | テ | デ | �� | ド | ナ | ニ | ヌ | ネ | ノ | ハ |

JavaScript（ECMAScript）采用 Unicode 作为字符编码，并采用 UTF-16 作为编码文字的方式。UTF-16 是将每个字符转换为 16 位位序列的编码方式。在 Unicode 中，用于表示 1 个字符的最小位组合称为**Code Unit**（符号单元），UTF-16 中每个 Code Unit 的大小为 16 位（2 字节）。

下面的代码是显示构成字符串的 Code Unit 的 hex 值（十六进制）的示例。String 的`charCodeAt`方法返回字符串指定索引的 Code Unit 的整数。然后使用 Number 的`toString`方法将这个 Code Unit 的整数值转换为 hex 值（十六进制）。

```javascript
const str = "アオイ";

// それぞれの文字をCode Unitのhex 値（16 進数）に変換する

// toStringの引数に16を渡すと16 進数に変換される

console.log(str.charCodeAt(0).toString(16)); // => "30a2"

console.log(str.charCodeAt(1).toString(16)); // => "30aa"

console.log(str.charCodeAt(2).toString(16));  // => "30a4" 
```

相反，要将 Code Unit 转换为 hex 值（十六进制）并转换为字符，可以使用`String.fromCharCode`方法。下面的代码展示了如何将用`0x`表示的十六进制整数字面量转换为字符串（有关`0x`字面量，请参阅“数据类型和字面量”章节）。

```javascript
const str = String.fromCharCode(

    0x30a2, // アのCode Unit

    0x30aa, // オのCode Unit

    0x30a4  // イのCode Unit

);

console.log(str); // => "アオイ" 
```

总结这些结果，这个字符串与构成它的 UTF-16 的 Code Unit 之间的关系如下。

| 索引 | 0 | 1 | 2 |
| --- | --- | --- | --- |
| 文字串 | ア | オ | イ |
| UTF-16 的 Code Unit（十六进制） | 0x30A2 | 0x30AA | 0x30A4 |

这样，JavaScript 中的字符串在内部以 16 位的 Code Unit 顺序排列。这仅仅是 ECMAScript 的内部表示采用 UTF-16，与 JavaScript 文件（编写的源代码文件）的编码无关。因此，即使 JavaScript 文件的编码不是 UTF-16，也没有问题。

UTF-16 的使用似乎是 JavaScript 的内部表示，因此似乎没有必要担心。然而，JavaScript 使用 UTF-16 的事实对 String 的 API 也有影响。关于 UTF-16 和字符串，我们将在下一章“字符串与 Unicode”中详细探讨。

在这里，只需记住“JavaScript 中的字符串由 UTF-16 的 Code Unit 组成”这一点就足够了。

## 文字列の分解与连接

要将字符串分解为数组，可以使用 String 的`split`方法。一方、要将数组元素连接成字符串、可以使用 Array の`join`方法。

这两个经常一起使用，所以我们一起来了解一下。

String 的`split`方法返回一个使用指定的分隔符分割的字符串の数组。下面のコード展示了如何创建一个用`・`分割的数组。

```javascript
const strings = "赤・青・緑".split("・");

console.log(strings); // => ["赤", "青", "緑"] 
```

在将分解后的字符串数组组合成字符串时、可以使用 Array の`join`方法。Array の`join`方法の第一个参数は分隔符、それが使用され文字列を连接し返す。

将这两个结合起来、可以将分隔符から`・`转换为`、`的处理过程を書くことができます。まず用`・`分割文字列（`split`）、次に用`、`连接（`join`）即可完成转换。

```javascript
const str = "赤・青・緑".split("・").join("、");

console.log(str); // => "赤、青、緑" 
```

String の`split`方法の第一个参数は正则表达式でも構いません。この点を利用して、以下のように分割文字列の处理过程を编写することができます。`/\s+/`は1つ以上のスペースにマッチする正则表达式リテラル、それがマッチする正则表达式オブジェクトを作成します。

```javascript
// 文字間に1つ以上のスペースがある

const str = "a     b    c      d";

// 1つ以上のスペースにマッチして分解する

const strings = str.split(/\s+/);

console.log(strings); // => ["a", "b", "c", "d"] 
```

## 文字列の长度

String の`length`属性は文字列の要素数を返します。文字列の構成要素は Code Unit であるため、`length`属性は Code Unit の数量を返します。

以下の文字列は 3 個の Code Unit から構成されているため、`length`属性は`3`を返します。

```javascript
console.log("文字列".length); // => 3 
```

また、空文字列の要素数は`0`であるため、`length`属性の結果も`0`になります。

```javascript
console.log("".length); // => 0 
```

## 文字列の比较

`===`（严格比较运算符）を使用して文字列を比较します。以下の条件を満たす場合、文字列は同じです。

+   文字列の要素 Code Unit が同じ順序で並んでいるか

+   文字の长さ（length）が同じか

虽然写得复杂，但如果文字列が同じであれば、`===`（严格比较运算符）の结果は`true`になります。

```javascript
console.log("文字列" === "文字列"); // => true

// 一致しなければfalseとなる

console.log("JS" === "ES"); // => false

// 文字列の长さが異なるのでfalseとなる

console.log("文字列" === "文字"); // => false 
```

さらに、`===`以外の比较运算符として、`>`、`<`、`>=`、`<=`などの大小关系运算符を使用して文字列を比較することもできます。

これらの关系运算符も、文字列の要素 Code Unit を順番に比較します。文字列から Code Unit の数値を取得するには、String の`charCodeAt`方法を使用します。

次のコードでは、`ABC`と`ABD`のどちらが大きいか（Code Unit の値が大きいか）を比較しています。

```javascript
// "A"と"B"のCode Unitは65と66

console.log("A".charCodeAt(0)); // => 65

console.log("B".charCodeAt(0)); // => 66

// "A"（65）は"B"（66）よりCode Unitの値が小さい

console.log("A" > "B"); // => false

// 先頭から順番に比較し C > D が falseであるため

console.log("ABC" > "ABD"); // => false 
```

このように、关系运算符での文字列比較は Code Unit に対して行われます。この结果を予測するのは困難であり、しばしば直感に反する结果になります。なぜなら、文字の顺序は国や言語によって異なるため、国际化（Internationalization）に関する知識も必要になるからです。

JavaScript には、ECMAScript に関連する ECMA-402 という仕様があり、これが国际化を規定しています。さらに、[Intl](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Intl)という組み込みオブジェクトが存在し、これらの国际化 API を定義しています。ただし、これらの API の詳細についてはここでは省略します。

## 文字列の一部を取得する

文字列から一部を取得するには、String の`slice`方法または`substring`方法を使用します。

`slice`方法はすでに配列で学習済みですが、文字列でも基本操作は同じです。まずは`slice`方法から見ていきます。

String の`slice`メソッドは、第一引数の開始位置から第二引数の終了位置（終了位置の要素は含まない）までの範囲を取り出した新しい文字列を返します。第二引数を省略した場合の挙動も同様で、省略した場合は文字列の末尾まで含んだ新しい文字列を返します。

位置にマイナスの値を指定した場合は文字列の末尾から数えた位置となります。また、第一引数の位置が第二引数の位置より大きい場合、常に空の文字列を返します。

そのため、メソッドの引数の扱い方は配列の`slice`メソッドと同様です。

```javascript
const str = "ABCDE";

console.log(str.slice(1)); // => "BCDE"

console.log(str.slice(1, 5)); // => "BCDE"

// マイナスを指定すると後ろからの位置となる

console.log(str.slice(-1)); // => "E"

// インデックスが1から4の範囲を取り出す

console.log(str.slice(1, 4)); // => "BCD"

// 第一引数 > 第二引数の場合、常に空文字列を返す

console.log(str.slice(4, 1)); // => "" 
```

String の`substring`メソッドは、`slice`メソッドと同じく第一引数に開始位置、第二引数に終了位置を指定し、その範囲を取り出して新しい文字列を返します。第二引数を省略した場合の挙動も同様で、省略した場合は文字列の末尾が終了位置となります。

`slice`メソッドとは異なる点として、位置にマイナスの値を指定した場合は常に`0`として扱われます。また、第一引数の位置が第二引数の位置より大きい場合、第一引数と第二引数が入れ替わるという予想しにくい挙動となります。

```javascript
const str = "ABCDE";

console.log(str.substring(1)); // => "BCDE"

console.log(str.substring(1, 5)); // => "BCDE"

// マイナスを指定すると0として扱われる

console.log(str.substring(-1)); // => "ABCDE"

// 位置:1から4の範囲を取り出す

console.log(str.substring(1, 4)); // => "BCD"

// 第一引数 > 第二引数の場合、引数が入れ替わる

// str.substring(1, 4)と同じ結果になる

console.log(str.substring(4, 1)); // => "BCD" 
```

このように、マイナスの位置や引数が交換される挙動は直感的とは言えません。そのため、`slice`メソッドと`substring`メソッドに指定する引数は、どちらとも同じ結果となる範囲に限定したほうが直感的な挙動となります。つまり、指定するインデックスは0 以上にして、第二引数を指定する場合は`第一引数の位置 < 第二引数の位置`にするということです。

String の`slice`メソッドは、`indexOf`メソッドなどの位置を取得するものと組み合わせて使うことが多いでしょう。次のコードでは、`?`の位置を`indexOf`メソッドで取得し、それ以降の文字列を`slice`メソッドで切り出しています。

```javascript
const url = "https://example.com?param=1";

const indexOfQuery = url.indexOf("?");

const queryString = url.slice(indexOfQuery);

console.log(queryString); // => "?param=1" 
```

また、配列とは異なりプリミティブ型の値である文字列は、`slice`メソッドと`substring`メソッド共に非破壊的です。機能的な違いがほとんどないため、どちらを利用するかは好みの問題となります。

## 文字列の検索

文字列の検索方法として、大きく分けて文字列による検索と正規表現による検索があります。*

指定した文字列が文字列中に含まれているかを検索する方法として、Stringメソッドには取得したい結果ごとにメソッドが用意されています。ここでは、次の3 種類の結果を取得する方法について文字列と正規表現それぞれの検索方法を見ていきます。

+   マッチした箇所のインデックスを取得

+   マッチした文字列の取得

+   マッチしたかどうかの真偽値を取得

### 文字列による検索

`String`オブジェクトには、指定した文字列で検索するメソッドが用意されています。*

#### 文字列によるインデックスの取得

`String`の`indexOf`メソッドと`lastIndexOf`メソッドは、指定した文字列で検索し、その文字列が最初に現れたインデックスを返します。これらは配列のArrayの`indexOf`メソッドと同じで、厳密等価演算子（`===`）で文字列を検索します。一致する文字列がない場合は`-1`を返します。*

+   `文字列.indexOf("検索文字列")`: 先頭から検索し、指定された文字列が最初に現れたインデックスを返す

+   `文字列.lastIndexOf("検索文字列")`: 末尾から検索し、指定された文字列が最初に現れたインデックスを返す

どちらのメソッドも一致する文字列が複数個ある場合でも、指定した検索文字列を最初に見つけた時点で検索は終了します。*

```javascript
// 検索対象となる文字列

const str = "にわにはにわにわとりがいる";

// indexOfは先頭から検索しインデックスを返す - "**にわ**にはにわにわとりがいる"

// "にわ"の先頭のインデックスを返すため 0 となる

console.log(str.indexOf("にわ")); // => 0

// lastIndexOfは末尾から検索しインデックスを返す- "にわにはにわ**にわ**とりがいる"

console.log(str.lastIndexOf("にわ")); // => 6

// 指定した文字列が見つからない場合は -1 を返す

console.log(str.indexOf("未知のキーワード")); // => -1 
```

### 文字列にマッチした文字列の取得

文字列を検索してマッチした文字列は、検索文字列そのものになるので自明です。*

次のコードでは`"Script"`という文字列で検索していますが、その検索文字列にマッチする文字列はもちろん`"Script"`になります。*

```javascript
const str = "JavaScript";

const searchWord = "Script";

const index = str.indexOf(searchWord);

if (index !== -1) {

    console.log(`${searchWord}が見つかりました`);

} else {

    console.log(`${searchWord}は見つかりませんでした`);

} 
```

#### 真偽値の取得

「文字列」に「検索文字列」が含まれているかを検索する方法がいくつか用意されています。次の3つのメソッドはES2015で導入されました。*

+   `String.prototype.startsWith(検索文字列)`^([ES2015]): 検索文字列が先頭にあるかの真偽値を返す

+   `String.prototype.endsWith(検索文字列)`^([ES2015]): 検索文字列が末尾にあるかの真偽値を返す

+   `String.prototype.includes(検索文字列)`^([ES2015]): 検索文字列を含むかの真偽値を返す

具体的な例をいくつか見てみましょう。*

```javascript
// 検索対象となる文字列

const str = "にわにはにわにわとりがいる";

// startsWith - 検索文字列が先頭ならtrue

console.log(str.startsWith("にわ")); // => true

console.log(str.startsWith("いる")); // => false

// endsWith - 検索文字列が末尾ならtrue

console.log(str.endsWith("にわ")); // => false

console.log(str.endsWith("いる")); // => true

// includes - 検索文字列が含まれるならtrue

console.log(str.includes("にわ")); // => true

console.log(str.includes("いる")); // => true 
```

## 正規表現オブジェクト

文字列による検索では、固定の文字列にマッチするものしか検索できません。一方で正規表現による検索では、あるパターン（規則性）にマッチするという柔軟な検索ができます。*

正規表現は正規表現オブジェクト（`RegExp`オブジェクト）として表現されます。正規表現オブジェクトはマッチする範囲を決める`パターン`と正規表現の検索モードを指定する`フラグ`の2つで構成されます。正規表現のパターン内では、次の文字は**特殊文字**と呼ばれ、特別な意味を持ちます。特殊文字として解釈されないように入力する場合には`\`（バックスラッシュ）でエスケープする必要があります。*

```
\ ^ $ . * + ? ( ) [ ] { } | 
```

正規表現オブジェクトを作成するには、正規表現リテラルと`RegExp`コンストラクタを使う2つの方法があります。*

```
// 正規表現リテラルで正規表現オブジェクトを作成

const patternA = /パターン/フラグ;

// `RegExp`コンストラクタで正規表現オブジェクトを作成

const patternB = new RegExp("パターン文字列", "フラグ"); 
```

正規表現リテラルは、`/`と`/`のリテラル内に正規表現のパターンを書くことで、正規表現オブジェクトを作成できます。次のコードでは、`+`という1 回以上の繰り返しを意味する特殊文字を使い、`a`が1 回以上連続する文字列にマッチする正規表現オブジェクトを作成しています。*

```javascript
const pattern = /a+/; 
```

正規表現オブジェクトを作成するもうひとつの方法として`RegExp`コンストラクタがあります。`RegExp`コンストラクタでは、文字列から正規表現オブジェクトを作成できます。*

次のコードでは、`RegExp`コンストラクタを使って`a`が1 文字以上連続している文字列にマッチする正規表現オブジェクトを作成しています。これは先ほどの正規表現リテラルで作成した正規表現オブジェクトと同じ意味になります。*

```javascript
const pattern = new RegExp("a+"); 
```

### 正規表現リテラルと`RegExp`コンストラクタの違い

正则表达式字面量和`RegExp`构造函数的区别在于正则表达式模式的评估时机不同。正则表达式字面量在源代码加载（解析）阶段评估正则表达式模式。另一方面，`RegExp`构造函数与普通函数一样，只有调用`RegExp`构造函数时才会评估正则表达式模式。*

以单独的 `[` 为例，这是一个无效的模式正则表达式，我们来看看评估时机的不同之处。由于 `[` 需要与 `]` 配对使用，因此在正则表达式模式中单独使用会导致语法错误异常。*

正则表达式字面量在代码加载时会评估正则表达式模式，因此，即使没有调用 `main` 函数，也会导致语法错误（`SyntaxError`）。*

```javascript
// 正規表現リテラルはロード時にパターンが評価され、例外が発生する

function main() {

    // `[`は対となる`]`を組み合わせる特殊文字であるため、単独で書けない

    const invalidPattern = /[/;

}

// `main`関数を呼び出さなくても例外が発生する 
```

另一方面，`RegExp` 构造函数在运行时评估正则表达式模式，因此只有调用 `main` 函数时才会出现语法错误（`SyntaxError`）。*

```javascript
// `RegExp`コンストラクタは実行時にパターンが評価され、例外が発生する

function main() {

    // `[`は対となる`]`を組み合わせる特殊文字であるため、単独で書けない

    const invalidPattern = new RegExp("");

}

// `main`関数を呼び出すことで初めて例外が発生する

main(); 
```

这意味着，正则表达式字面量是在编写代码时创建固定模式的正则表达式对象。另一方面，`RegExp` 构造函数可以创建在运行时可能变化的模式の正则表达式オブジェクト、例えば変数と組み合わせて使用することができます。*

例えば、我们将比较使用正则表达式对象匹配连续空格的情况。*

在下面的コード中、使用正则表达式リテラルで3つの連続するスペースにマッチする正则表达式オブジェクトを作成しています。`\s` はスペースまたはタブなどの空白文字にマッチする特殊文字です。また、`{number}` は指定した回数繰り返す特殊文字です。*

```javascript
// 3つの連続するスペースなどにマッチする正規表現

const pattern = /\s{3}/; 
```

正则表达式字面量在加载时评估正则表达式模式，因此无法动态更改 `\s` 连续出现的次数。另一方面，`RegExp` 构造函数在运行时评估正则表达式模式，因此可以创建包含变量の正则表达式オブジェクト。*

在下面のコード中、使用 `RegExp` コンストラクタに変数 `spaceCount` の数量に応じて連続するスペースにマッチする正则表达式オブジェクトを作成しています。ただし、`\`（バックスラッシュ）自身は文字列中ではエスケープ文字であるため、`RegExp` コンストラクタのパターン文字列中で `\`（バックスラッシュ）で始まる特殊文字はエスケープする必要があります。*

```javascript
const spaceCount = 3;

// `/\s{3}/`の正規表現を文字列から作成する

// "\"がエスケープ文字であるため、"\"自身を文字列として書くには、"\\"のように2つ書く

const pattern = new RegExp(`\\s{${spaceCount}}`); 
```

したがって、`RegExp` コンストラクタは文字列から正则表达式オブジェクトを作成できますが、特殊文字のエスケープが必要です。したがって、正则表达式リテラルが使用できる場合は、それを使用することをお勧めします。なぜなら、それはより簡潔でパフォーマンスも良いからです。正则表达式のパターン中に変数を使用する必要がある場合は、`RegExp` コンストラクタを使用してください。*

### 正規表現による検索

正規表現による検索では、String オブジェクトまたは RegExp オブジェクトに対応するメソッドを使用します。*

#### 正規表現によるインデックスの取得

`String` の `indexOf` メソッドの正規表現版は `String` の `search` メソッドです。`search` メソッドは、正規表現のパターンにマッチする位置のインデックスを返します。マッチする文字列がない場合は `-1` を返します。*

+   `String.prototype.indexOf(searchString)`：マッチする文字列のインデックスを返す

+   `String.prototype.search(/pattern/`)：指定した正規表現のパターンにマッチする位置のインデックスを返す

次のコードでは、連続する 3 桁の数字を検索し、マッチする位置のインデックスを返します。`\d` は単一の数字（`0` から `9`）にマッチする特殊文字です。*

```javascript
const str = "ABC123EFG";

const searchPattern = /\d{3}/;

console.log(str.search(searchPattern)); // => 3 
```

#### 正規表現にマッチした文字列の取得

文字列による検索では、マッチした文字列そのものが取得結果となります。しかし、`search` メソッドによる正規表現検索では、マッチした文字列の長さが分からないため、マッチした文字列そのものを取得することはできません。*

したがって、マッチした文字列を取得するための `String` の `match` メソッドと `matchAll` メソッドが提供されています。さらに、これらのメソッドは正規表現のグローバルマッチ `g` フラグによって動作が変わります。*

##### マッチした文字列の取得

まず、`String` の `match` メソッドから見ていきます。`match` メソッドは、正規表現 `/pattern/` と `"string"` がマッチしたときに、マッチした文字列に関する情報を返します。*

```javascript
"文字列".match(/パターン/); 
```

`match` メソッドで検索したが、正規表現にマッチする文字列がない場合は `null` を返します。*

```javascript
console.log("文字列".match(/マッチしないパターン/)); // => null 
```

`g` フラグがない正規表現で検索した場合、`match` メソッドは最初にマッチした文字列を見つけると検索を終了します。このとき、`match` メソッドの返り値は特殊な配列となり、`index` プロパティと `input` プロパティを持ちます。`index` プロパティにはマッチした文字列の開始インデックスが入り、`input` プロパティには検索対象の文字列全体が入ります。*

次のコードでは、`/[a-zA-Z]+/` 正規表現は、`a` から `Z` までのアルファベットが1つ以上連続する文字列にマッチします。この正規表現にマッチする文字列は、返り値の配列のインデックスでアクセスできます。`g` フラグがない場合は、最初のマッチしか見つけないため、返り値の配列は1つしか要素を持ちません。*

```javascript
const str = "ABC あいう DE えお";

const alphabetsPattern = /[a-zA-Z]+/;

// gフラグなしでは、最初の結果のみを含んだ特殊な配列を返す

const results = str.match(alphabetsPattern);

console.log(results.length); // => 1

// マッチした文字列はインデックスでアクセスできる

console.log(results[0]); // => "ABC"

// マッチした文字列の先頭のインデックス

console.log(results.index); // => 0

// 検索対象となった文字列全体

console.log(results.input); // => "ABC あいう DE えお" 
```

`g` フラグがある正規表現で検索した場合、`match` メソッドはすべてのマッチした文字列を含む配列を返します。*

次のコードでは、`/[a-zA-Z]+/g` 正規表現は、`a` から `Z` までのアルファベットが1つ以上連続する文字列にマッチします。この正規表現にマッチする位置は "ABC" と "DE" なので、`match` メソッドの返り値の配列には 2 つの要素が入ります。*

```javascript
const str = "ABC あいう DE えお";

const alphabetsPattern = /[a-zA-Z]+/g;

// gフラグありでは、すべての検索結果を含む配列を返す

const resultsWithG = str.match(alphabetsPattern);

console.log(resultsWithG.length); // => 2

console.log(resultsWithG[0]); // => "ABC"

console.log(resultsWithG[1]); // => "DE"

// indexとinputはgフラグありの場合は追加されない

console.log(resultsWithG.index); // => undefined

console.log(resultsWithG.input); // => undefined 
```

この場合、`match` メソッドの返り値の配列には `index` プロパティと `input` プロパティが含まれません。これは、複数のマッチ位置がある場合、`index` プロパティ一つでは意味を一意に特定できないからです。*

String の `match` メソッドの動作をまとめると以下のようになります。*

+   マッチしない場合は `null` を返す

+   マッチした場合は、マッチした文字列を含む特殊な配列を返す

+   正規表現の `g` フラグを使用している場合は、すべてのマッチ結果を含む普通の配列を返す

ES2020 で導入された `String` の `matchAll` メソッドは、正規表現の `g` フラグを使用して繰り返しマッチを行うためのメソッドです。`matchAll` メソッドは、マッチ結果を含む Iterator を返します。*

次のコードでは、アルファベットにマッチする結果の Iterator オブジェクトを取得しています。Iterator オブジェクトは `for...of` 構文でイテレーション処理を行い、Iterator 内の値を取得して処理を行います（詳細については「ループとイテレーション」章を参照）。このイテレーション処理では、マッチした文字列および `index` と `input` プロパティを持つ特殊な配列を取得できます。*

```javascript
const str = "ABC あいう DE えお";

const alphabetsPattern = /[a-zA-Z]+/g;

// matchAllはIteratorを返す

const matchesIterator = str.matchAll(alphabetsPattern);

for (const match of matchesIterator) {

    // マッチした要素ごとの情報を含んでいる

    console.log(`match: "${match[0]}", index: ${match.index}, input: "${match.input}"`);

}

// 次の順番でコンソールに出力される

// match: "ABC", index: 0, input: "ABC あいう DE えお"

// match: "DE", index: 8, input: "ABC あいう DE えお" 
```

したがって、正規表現の `g` フラグを使用して繰り返しマッチを行う場合は、`match` メソッドではなく `matchAll` メソッドを使用するべきです。また、`matchAll` メソッドは `g` フラグがない正規表現をサポートしていないため、`g` フラグがない正規表現を渡すと例外が発生します。*

##### マッチした文字列の一部を取得

`String` の `match` メソッドと `matchAll` メソッドは、正規表現のキャプチャをサポートしています。キャプチャとは、正規表現の中で `/pattern1(pattern2)/` のように括弧で囲まれた部分を指します。このキャプチャによって、正規表現にマッチした部分の一部を取り出すことができます。*

`match` メソッドと `matchAll` メソッドは、マッチ結果を配列として返します。マッチしたパターンにキャプチャがある場合、返り値の配列にはキャプチャした部分が順番に追加されます。配列の先頭にはマッチした文字列全体が入り、その後にキャプチャ（`(` と `)` で囲まれた部分）が順番に入ります。*

```javascript
const [マッチした全体の文字列, キャプチャ1, キャプチャ2] = 文字列.match(/パターン(キャプチャ1)と(キャプチャ2)/); 
```

次のコードでは、`ECMAScript (数字+)` の `数字` 部分を取り出そうとしています。`String` の `match` メソッドとキャプチャを使用して、`\d+` にマッチする部分を取り出しています。*

```javascript
// "ECMAScript (数字+)"にマッチするが、欲しい文字列は数字の部分のみ

const pattern = /ECMAScript (\d+)/;

// 返り値は0 番目がマッチした全体、1 番目がキャプチャの1 番目というように対応している

// [マッチした全部の文字列, キャプチャの1 番目, キャプチャの2 番目 ....]

const [all, capture1] = "ECMAScript 6".match(pattern);

console.log(all); // => "ECMAScript 6"

console.log(capture1); // => "6" 
```

正規表現の `g` フラグを使用して繰り返しマッチを行う場合は、`matchAll` メソッドを使用するべきです。前述の通り、`match` メソッドは繰り返しマッチ時に各マッチの独立した情報を取得することができません。*

次のコードでは、`ES (数字+)` の `数字` (`\d+`) 部分を取り出そうとしています。`matchAll` の返り値をイテレーション処理することで、各マッチのキャプチャを取り出すことができます。*

```javascript
// "ES(数字+)"にマッチするが、欲しい文字列は数字の部分のみ

const pattern = /ES(\d+)/g;

// iteratorを返す

const matchesIterator = "ES2015、ES2016、ES2017".matchAll(pattern);

for (const match of matchesIterator) {

    // マッチした要素ごとの情報を含んでいる

    // 0 番目はマッチした文字列全体、1 番目がキャプチャの1 番目である数字

    console.log(`match: "${match[0]}", capture1: ${match[1]}, index: ${match.index}, input: "${match.input}"`);

}

// 次の順番でコンソールに出力される

// match: "ES2015", capture1: 2015, index: 0, input: "ES2015、ES2016、ES2017"

// match: "ES2016", capture1: 2016, index: 7, input: "ES2015、ES2016、ES2017"

// match: "ES2017", capture1: 2017, index: 14, input: "ES2015、ES2016、ES2017" 
```

#### *[专栏] 使用 RegExp.prototype.exec 进行 String.prototype.matchAll*

`String` の `matchAll` メソッドは ES2020 で導入されました。それより前は、`String` の `match` メソッドに似た RegExp の `exec` メソッドを使用して、`String` の `matchAll` メソッドと同様のことを実現していました。*

`RegExp` の `exec` メソッドは、文字列を引数とするメソッドです。*

```javascript
/pattern/.exec("文字列"); 
```

`g` フラグがない正規表現で検索した場合、`RegExp` の `exec` メソッドは最初にマッチした結果のみを含む特殊な配列を返します。このとき、返り値の配列には `index` プロパティと `input` プロパティが追加され、`String` の `match` メソッドと同様の動作になります。*

```javascript
const str = "ABC あいう DE えお";

const alphabetsPattern = /[a-zA-Z]+/;

// gフラグなしでは、最初の結果のみを持つ配列を返す

const results = alphabetsPattern.exec(str);

console.log(results.length); // => 1

console.log(results[0]); // => "ABC"

// マッチした文字列の先頭のインデックス

console.log(results.index); // => 0

// 検索対象となった文字列全体

console.log(results.input); // => "ABC あいう DE えお" 
```

`g` フラグがある正規表現で検索した場合でも、`RegExp` の `exec` メソッドは最初にマッチした結果のみを含む特殊な配列を返します。これは `String` の `match` メソッドとは異なる動作です。さらに、マッチした文字列の末尾インデックスを正規表現オブジェクトの `lastIndex` プロパティに記録します。その後、`exec` メソッドを再度呼び出すと、最後にマッチした末尾インデックス（`lastIndex` プロパティの位置）から検索を開始します。*

```javascript
const str = "ABC あいう DE えお";

const alphabetsPattern = /[a-zA-Z]+/g;

// まだ一度も検索していないので、lastIndexは0となり先頭から検索が開始される

console.log(alphabetsPattern.lastIndex); // => 0

// gフラグありでも、一回目の結果は同じだが、`lastIndex`プロパティが更新される

const result1 = alphabetsPattern.exec(str);

console.log(result1[0]); // => "ABC"

console.log(alphabetsPattern.lastIndex); // => 3

// 2 回目の検索が、`lastIndex`の値のインデックスから開始される

const result2 = alphabetsPattern.exec(str);

console.log(result2[0]); // => "DE"

console.log(alphabetsPattern.lastIndex); // => 10

// 検索結果が見つからない場合はnullを返し、`lastIndex`プロパティは0にリセットされる

const result3 = alphabetsPattern.exec(str);

console.log(result3); // => null

console.log(alphabetsPattern.lastIndex); // => 0 
```

`RegExp` の `exec` メソッドの動作をまとめると以下のようになります。* 正規表現に `g` フラグがない場合は、`String` の `match` メソッドと同じ動作になります。一方、`g` フラグがある場合は、`String` の `match` メソッドとは異なる動作になります。*

+   マッチしない場合は `null` を返す

+   マッチした場合は、マッチした文字列を含む特殊な配列を返す

+   正規表現の `g` フラグを使用している場合は、マッチした文字列を含む特殊な配列を返し、マッチの末尾インデックスを正規表現オブジェクトの `lastIndex` プロパティに記録する

正規表現の `g` フラグと `exec` メソッドを使用して検索を行う場合、`lastIndex` プロパティを活用することで、各検索時に末尾インデックスを更新し、すべてのマッチ結果を取得することができます。*

次のコードでは、`RegExp` の `exec` メソッドを使用して、アルファベットにマッチする結果を `matches` に格納しています。`g` フラグがある場合、`exec` メソッドは最後にマッチした位置を記録するため、`while` ループでイテレーション処理を行い、前回のマッチ位置から検索を続けることができます。さらに、`exec` メソッドはマッチがない場合は `null` を返すため、マッチがないときは自動的に `while` ループから抜け出します。*

```javascript
const str = "ABC あいう DE えお";

const alphabetsPattern = /[a-zA-Z]+/g;

let matches;

while (matches = alphabetsPattern.exec(str)) {

    // RegExpの`exec`メソッドの返り値は`index`プロパティなどを含む特殊な配列

    console.log(`match: ${matches[0]}, index: ${matches.index}, lastIndex: ${alphabetsPattern.lastIndex}`);

}

// 次の順番でコンソールに出力される

// match: ABC, index: 0, lastIndex: 3

// match: DE, index: 8, lastIndex: 10 
```

`RegExp` の `exec` メソッドと正規表現の `g` フラグを使用することで、`String` の `matchAll` メソッドと同様のイテレーション処理を実現しています。`RegExp` の `exec` メソッドは、イテレーション処理対象オブジェクトが導入される以前から存在するメソッドです。*

`String` の `matchAll` メソッドで Iterator をイテレーション処理する方法と比較すると、`RegExp` の `exec` メソッドは `while` ループなどのイテレーション処理を手動で書く必要があり、直感的ではありません。したがって、`String` の `matchAll` メソッドが使用できる場合は、`RegExp` の `exec` メソッドを使用する必要はありません。*

#### 获取布尔值

正規表現オブジェクトを使用して、正規表現のパターンにマッチするかどうかをテストするには、`RegExp` の `test` メソッドを使用します。*

正規表現のパターンには位置を指定する特殊文字があります。したがって、「文字列による検索」で紹介した方法は、特殊文字と `RegExp` の `test` メソッドを使用して表現することができます。*

+   `String` の `startsWith` と等価：`/^pattern/.test(string)`

    +   `^` は文字列の先頭にマッチする特殊文字

+   `String` の `endsWith` と等価：`/pattern$/.test(string)`

    +   `$` は文字列の末尾にマッチする特殊文字

+   `String` の `includes` と等価：`/pattern/.test(string)`

具体的な例をいくつか見てみましょう。*

```javascript
// 検索対象となる文字列

const str = "にわにはにわにわとりがいる";

// ^ - 検索文字列が先頭ならtrue

console.log(/^にわ/.test(str)); // => true

console.log(/^いる/.test(str)); // => false

// $ - 検索文字列が末尾ならtrue

console.log(/にわ$/.test(str)); // => false

console.log(/いる$/.test(str)); // => true

// 検索文字列が含まれるならtrue

console.log(/にわ/.test(str)); // => true

console.log(/いる/.test(str)); // => true 
```

さらに、正規表現は繰り返しや文字集合などの特殊文字を使用して、より柔軟な検索を行うことができます。*

### 文字列による検索と正規表現による検索の選択

私たちはこれまで、文字列による検索と正規表現による検索が同じ結果を得られる場合があることを学んできました。両者が同じ結果を得られる場合、どちらを選択すべきでしょうか？*

正規表現は柔軟な検索に強く、特殊文字を使用することで複雑なパターンにもマッチさせることができます。一方で、正規表現のパターンそのものから意図を読み取るのは難しい場合があります。*

次の例では、`/` で始まり `/` で終わる文字列かどうかを判定します。この判定を正規表現と String メソッドでそれぞれ実装してみます（この例は正規表現に不利になるように意図的に作成しています）。*

```javascript
const str = "/正規表現のような文字列/";

// 正規表現で `/` から始まり `/` で終わる文字列のパターン

const regExpLikePattern = /^\/.*\/$/;

// RegExpの`test`メソッドでパターンにマッチするかを判定

console.log(regExpLikePattern.test(str)); // => true

// Stringメソッドで、`/`から始まり`/`で終わる文字列かを判定する関数

const isRegExpLikeString = (str) => {

    return str.startsWith("/") && str.endsWith("/");

};

console.log(isRegExpLikeString(str)); // => true 
```

正規表現は柔軟で便利ですが、コード中に意図が見えにくくなる可能性があります。したがって、正規表現を扱う際は、コメントや変数名を使って意図を明確にすることをお勧めします。*

「文字列による検索と正規表現による検索で同じ結果が得られる場合、どちらを選ぶべきか？」という疑問に対して、文字列メソッドで表現できる場合は文字列メソッドを使用し、柔軟性や曖昧な検索が必要な場合は、コメントや変数名を添えた正規表現を使用することを推奨します。*

正規表現についてさらに学びたい場合は、[MDN の正規表現文档](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Regular_Expressions "正規表現 - JavaScript | MDN") を参照するか、[regex101](https://regex101.com/ "Online regex tester and debugger: PHP, PCRE, Python, Golang and JavaScript") などのサイトで実際に試してみることをお勧めします。*

## 替换/删除字符串

文字列の一部を置換または削除するには、String の `replace` メソッドを使用します。「データ型と字面量」で述べたように、文字列は変更不能なプリミティブ型であるため、部分的に削除することはできません。*

つまり、`delete` 演算子は文字列には使用できません。厳格モードでは、削除できないプロパティを削除しようとするとエラーになります。非厳格モードでは、エラーにならずに無視されます（厳格モードについては「JavaScript は何」を参照）。*

```javascript
"use strict";

const str = "文字列";

// 文字列の0 番目の削除を試みるがStrict modeでは例外が発生する

delete str[0]; // => TypeError: property 0 is non-configurable and can't be deleted 
```

代わりに、String の `replace` メソッドは、削除したい部分を空文字列に置換することで、削除を表現できます。`replace` メソッドは、最初の引数 `検索文字列` または正規表現にマッチした部分を、2番目の引数 `置換文字列` に置換します。最初の引数は文字列でも正規表現でも構いません。*

```javascript
文字列.replace("検索文字列", "置換文字列");

文字列.replace(/パターン/, "置換文字列"); 
```

置換したい部分を空文字列に置換することで、削除を表現することができます。*

```javascript
const str = "文字列";

// "文字"を""（空文字列）へ置換することで"削除"を表現

const newStr = str.replace("文字", "");

console.log(newStr); // => "列" 
```

`replace` メソッドは正規表現も指定できます。`g` フラグを有効にした正規表現を渡すと、文字列中にマッチするすべての部分を置換します。*

```javascript
// 検索対象となる文字列

const str = "にわにはにわにわとりがいる";

// 文字列を指定した場合は、最初に一致したものだけが置換される

console.log(str.replace("にわ", "niwa")); // => "niwaにはにわにわとりがいる"

// `g`フラグなし正規表現の場合は、最初に一致したものだけが置換される

console.log(str.replace(/にわ/, "niwa")); // => "niwaにはにわにわとりがいる"

// `g`フラグあり正規表現の場合は、繰り返し置換を行う

console.log(str.replace(/にわ/g, "niwa")); // => "niwaにはniwaniwaとりがいる" 
```

文字列中のすべてのマッチした部分を置換したい場合は、ES2021 で追加された String の `replaceAll` メソッドを使用できます。`replace` メソッドでは最初にマッチした部分しか置換されませんが、`replaceAll` メソッドではすべてのマッチした部分が置換されます。*

`replace` メソッドと `g` フラグを有効にした正規表現を使用する場合との違いは、`replaceAll` メソッドでは正規表現ではなく文字列を使用してすべての部分を置換できる点です。したがって、`replaceAll` メソッドでは、たとえば `?` のような特殊意味を持つ文字でも、そのまま検索文字列として使用して置換することができます。*

```javascript
// 検索対象となる文字列

const str = "???";

// replaceメソッドに文字列を指定した場合は、最初に一致したものだけが置換される

console.log(str.replace("?", "!")); // => "!??"

// replaceAllメソッドに文字列を指定した場合は、一致したものがすべて置換される

console.log(str.replaceAll("?", "!")); // => "!!!"

// replaceメソッドの場合は、正規表現の特殊文字はエスケープが必要となる

console.log(str.replace(/\?/g, "!")); // => "!!!"

// replaceAllメソッドにも正規表現を渡せるが、この場合はエスケープが必要となるためreplaceと同じ

console.log(str.replaceAll(/\?/g, "!")); // => "!!!" 
```

`replace` メソッドと `replaceAll` メソッドでは、キャプチャを使用して複雑な置換を行うことができます。*

2番目の引数にコールバック関数を渡すと、最初の引数 `パターン` にマッチした部分がコールバック関数の返り値に置換されます。コールバック関数の最初の引数はマッチした文字列全体、その後にキャプチャが順番に入ります。*

```javascript
const 置換した結果の文字列 = 文字列.replace(/(パターン)/, (all, ...captures) => {

    return 置換したい文字列;

}); 
```

たとえば、`2017-03-01` を `2017 年 03 月 01 日` に置換する処理を書いてみましょう。*

正規表現 `/(\d{4})-(\d{2})-(\d{2})/g` は文字列 `"2017-03-01"` にマッチします。`year`、`month`、`day` はそれぞれキャプチャされた文字列を持ち、マッチした文字列全体はコールバック関数の返り値に置換されます。*

```javascript
function toDateJa(dateString) {

    // パターンにマッチしたときのみ、コールバック関数で置換処理が行われる

    return dateString.replace(/(\d{4})-(\d{2})-(\d{2})/g, (all, year, month, day) => {

        // `all`には、マッチした文字列全体が入っているが今回は利用しない

        // `all`が次の返す値で置換されるイメージ

        return `${year}年${month}月${day}日`;

    });

}

// マッチしない文字列の場合は、そのままの文字列が返る

console.log(toDateJa("本日ハ晴天ナリ")); // => "本日ハ晴天ナリ"

// マッチした場合は置換した結果を返す

console.log(toDateJa("今日は2017-03-01です")); // => "今日は2017 年 03 月 01 日です" 
```

## 文字列の構築

最後に、文字列の構築方法を見ていきます。本章の冒頭で述べたように、本章の目的は「文字列を自由に構築できるようになること」です。*

単純に文字列を連結または置換するだけで、新しい文字列を作ることはできます。しかし、構造化された文字列を扱う場合、単純な連結だけでは意味が異なる結果になることがあります。*

ここで言う構造化された文字列とは、文字列の中に文脈を持った文字列を含むものを指します。たとえば、URL 文字列は以下のような構造を持ち、それぞれの部分に入る文字列の種類などが規定されています（詳細については「[URL 標準](https://url.spec.whatwg.org/ "URL Standard")」を参照）。*

```text
"https://example.com/index.html"

 ^^^^^   ^^^^^^^^^^^ ^^^^^^^^^^

   |          |     　　　|

 scheme      host     pathname 
```

このような文字列を作成する際は、単純な文字列連結演算子（`+`）よりも、専用の関数を使用したほうが安全です。*

たとえば、`getResource` 関数が存在すると仮定します。この関数は、`baseURL` と `pathname` を引数として受け取り、連結後の URL からリソースを取得します。*

```javascript
// `baseURL`と`pathname`にあるリソースを取得する

function getResource(baseURL, pathname) {

    const url = baseURL + pathname;

    console.log(url); // => "http://example.com/resouces/example.js"

    // 省略) リソースを取得する処理...

}

const baseURL = "http://example.com/resouces";

const pathname = "/example.js";

getResource(baseURL, pathname); 
```

しかし、`baseURL` の末尾に `/` が含まれているべきだと考える人もいるでしょう。`getResource` 関数は `baseURL` の末尾に `/` がある場合を考慮していないため、予期しない URL からリソースを取得してしまう可能性があります。*

```javascript
// `baseURL`と`pathname`にあるリソースを取得する

function getResource(baseURL, pathname) {

    const url = baseURL + pathname;

    // `/` と `/` が２つ重なってしまっている

    console.log(url); // => "http://example.com/resouces//example.js"

    // 省略) リソースを取得する処理...

}

const baseURL = "http://example.com/resouces/";

const pathname = "/example.js";

getResource(baseURL, pathname); 
```

この問題の難点は、文字列レベルでは正しく連結されているため、エラーとして現れない点にあります。つまり、表面的には問題がないように見えるが、実際に実行してみないと問題に気づかないということです。*

したがって、このような構造化された文字列を扱う際は、専用の関数またはオブジェクトを作成して、安全に文字列を扱う必要があります。*

URL 文字列の連結を安全に行うためには、`baseURL` の末尾の `/` の有無を吸収する仕組みが必要です。次の `baseJoin` 関数は、`baseURL` と `pathname` を連結した文字列を返し、`baseURL` の末尾の `/` の有無を吸収します。*

```javascript
// ベースURLとパスを結合した文字列を返す

function baseJoin(baseURL, pathname) {

    // 末尾に / がある場合は、/ を削除してから結合する

    const stripSlashBaseURL = baseURL.replace(/\/$/, "");

    return stripSlashBaseURL + pathname;

}

// `baseURL`と`pathname`にあるリソースを取得する

function getResource(baseURL, pathname) {

    const url = baseJoin(baseURL, pathname);

    // baseURLの末尾に / があってもなくても同じ結果となる

    console.log(url); // => "http://example.com/resouces/example.js"

    // 省略) リソースを取得する処理...

}

const baseURL = "http://example.com/resouces/";

const pathname = "/example.js";

getResource(baseURL, pathname); 
```

ECMAScript の範囲外ですが、URL やファイルパスなどの典型的なケースでは、すでに専用の処理方法が存在します。たとえば、URL を扱う Web 標準 API の[URL](https://developer.mozilla.org/ja/docs/Web/API/URL "URL - Web API インターフェイス | MDN") オブジェクトや、ファイルパスを扱う Node.js のコアモジュール[Path](https://nodejs.org/api/path.html "Path | Node.js v7.9.0 Documentation") などがあります。専用の処理方法が存在する場合は、直接 `+` 演算子で文字列を連結するべきではありません。*

### *[ES2015] タグ付きテンプレート関数*

JavaScript では、テンプレートリテラルにタグ付きテンプレート関数を適用することで、テンプレートの一部のみを変更する処理を行うことができます。タグ付きテンプレート関数は、関数とテンプレートリテラルを組み合わせた表現です。関数を呼び出す際は、`関数(テンプレート)` の形式を使用し、`関数 テンプレート 関数` の形式は使用しません。*

通常の関数呼び出しでは、関数の引数は単なる文字列です。*

```javascript
function tag(str) {

    // 引数`str`にはただの文字列が渡ってくる

    console.log(str); // => "template 0 literal 1"

}

// ()をつけて関数を呼び出す

tag(`template ${0} literal ${1}`); 
```

しかし、`関数 テンプレート 関数` の形式で関数を呼び出すと、関数が受け取る引数はタグ付きテンプレートに関する値になります。このとき、関数の第一引数はテンプレート中の `${}` で区切られた文字列の配列となり、その後に `${}` 内の式の評価結果が順番に入ります。*

```javascript
// 呼び出し方によって受け取る引数の形式が変わる

function tag(strings, ...values) {

    // stringsは文字列のパーツが${}で区切られた配列となる

    console.log(strings); // => ["template "," literal ",""]

    // valuesには${}の評価値が順番に入る

    console.log(values); // => [0, 1]

}

// ()をつけずにテンプレートを呼び出す

tag`template ${0} literal ${1}`; 
```

これらは同じ関数ですが、`関数 テンプレート 関数` の形式で呼び出すと、渡される引数の形式が特殊になります。したがって、タグ付きテンプレートに使用する関数は**タグ関数**（Tag function）と呼ばれます。*

まず、タグ付きテンプレートの内容をそのまま連結して返すタグ関数 `stringRaw` を実装してみます。Array の `reduce` メソッドを使用して、テンプレートリテラルと変数を順番に連結します（`reduce` メソッドについては「配列」章を参照）。*

```javascript
// テンプレートを順番どおりに結合した文字列を返すタグ関数

function stringRaw(strings, ...values) {

    // 配列から文字列を返すためにreduceメソッドを利用する

    // resultの初期値はstrings[0]の値となる

    return strings.reduce((result, str, i) => {

        console.log([result, values[i - 1], str]);

        // それぞれループで次のような出力となる

        // 1 度目: ["template ", 0, " literal "]

        // 2 度目: ["template 0 literal ", 1, ""]

        return result + values[i - 1] + str;

    });

}

// 関数`テンプレートリテラル` という形で呼び出す

console.log(stringRaw`template ${0} literal ${1}`); // => "template 0 literal 1" 
```

ここで実装した `stringRaw` タグ関数は、`String.raw` メソッド([ES2015]) と同様の動作をします。*

```javascript
console.log(String.raw`template ${0} literal ${1}`); // => "template 0 literal 1" 
```

タグ付きテンプレート関数を使用することで、テンプレートリテラルに特定の形式の変換を適用し、データを埋め込むことでテンプレート処理を行うことができます。*

次のコードでは、テンプレート中の変数を URL エンコードして埋め込むタグ付きテンプレート関数を定義しています。`encodeURIComponent` 関数は URL エンコードを行う関数です。`escapeURL` 関数は、`encodeURIComponent` 関数を使用して引数を URL エンコードして埋め込む関数です。*

```javascript
// 変数をURLエスケープするタグ関数

function escapeURL(strings, ...values) {

    return strings.reduce((result, str, i) => {

        return result + encodeURIComponent(values[i - 1]) + str;

    });

}

const input = "A&B";

// escapeURLタグ関数を使ったタグつきテンプレート

const escapedURL = escapeURL`https://example.com/search?q=${input}&sort=desc`;

console.log(escapedURL); // => "https://example.com/search?q=A%26B&sort=desc" 
```

タグ付きテンプレートリテラルを使用することで、文脈に応じた処理を追加することができます。この機能は、JavaScript に HTML などの他言語または DSL（ドメイン特化言語）を埋め込む際に頻繁に使用されます。*

## 終わりに

本章では、JavaScript の文字列（`String` オブジェクト）について説明しました。文字列を扱うための String メソッドは多数存在し、そのうちには正規表現と組み合わせて使用されるものもあります。*

正規表現は JavaScript 言語内の独立した言語であり、ほぼ1冊の本を書くことができるほどの内容があります。詳細については、[MDN の正規表現文档](https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Regular_Expressions "正規表現 - JavaScript | MDN") などを参照してください。*

文字列は一見単純に見えますが、URL やファイルパスなどの文脈情報を含む場合があります。これらの文字列を安全に扱うためには、文脈に応じた処理が必要です。さらに、タグ付きテンプレートリテラルを使用することで、テンプレート中の変数を自動的にエスケープするなどの機能を実現できます。*

> ¹. これは[Unicode カタカナ表](https://unicode-table.com/jp/#katakana)から抜粋した表です。 ↩*****************************


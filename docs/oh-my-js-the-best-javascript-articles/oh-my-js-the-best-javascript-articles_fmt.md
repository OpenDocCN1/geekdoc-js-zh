
# Oh My JS：最佳 JavaScript 文章集

![](img/5f4a286ef99041bf37736af72f6b8b9b_1_0.png)

## 推特此书！

请在 Twitter 上分享此书来帮助 Azat Mardan！

此书的推荐推文内容为：

I just bought Oh My JS CC @RPJSBook

此书的话题标签为 `#ohmyjs`。

点击此链接在 Twitter 上搜索该标签，查看其他人对这本书的评价：

https://twitter.com/search?q=#ohmyjs

致上帝、我的老师以及 Vladimir Nabokov

# JavaScript 基础

## 全球最被误解的编程语言

原文：http://javascript.crockford.com/javascript.html

Douglas Crockford, crockford.com

JavaScript，又称 Mocha、LiveScript、ECMAScript，是世界上最流行的编程语言之一。世界上几乎每台电脑都安装并使用了 JavaScript 解释器。它的流行完全归功于它作为 Web 脚本语言的角色。

尽管它非常流行，但很少有人知道 JavaScript 是一门非常优秀的动态对象化编程语言。为什么这门语言会如此被误解？

### 命名

`Java` 前缀暗示了 JavaScript 与 Java 有关，并且它是 Java 的一个低级版本。这种命名刻意制造了困惑，而困惑导致了误解。JavaScript 不是解释型的 Java。JavaScript 是一门不同的语言。

JavaScript 在语法上与 Java 有相似之处，正如 Java 之于 C 一样。但并不是 Java（原名 Oak）最初的设计目标。JavaScript 并非在 Java 的母地 Sun Microsystems 开发。它最初被称为 LiveScript，但那个名字还不够困惑。

`-Script` 后缀暗示它不是一门真正的编程语言，脚本语言低于编程语言。这实际上是一个专业化的问题。与 C 相比，JavaScript 用性能换取表达力和动态性。

#### 披着 C 外壳的 Lisp

JavaScript 的类 C 语法（包括大括号和笨拙的 `for` 语句）使其看起来像是一门普通的程序化语言。这是具有误导性的，因为 JavaScript 与 Lisp 或 Scheme 等函数式语言相比而非 C 或 Java。它有数组而不是列表，有对象而不是属性列表。函数是一等公民。它有闭包。无需平衡即可获得 lambda。

### 类型转换

JavaScript 是为了 Netscape Navigator 设计的。它的成功使其成为几乎所有网络浏览器的标准配置。这导致了类型转换。JavaScript 是编程语言中的乔治·里夫。JavaScript 非常适用于大量的非 Web 应用。

### 移动目标

JavaScript 的早期版本非常弱。它们缺乏异常处理、内部函数和继承。在目前的形式下，它是一门完整的对象化编程语言。但许多对语言的观点是基于其不成熟的形式。负责该语言的 ECMA 委员会正在开发扩展，这些扩展虽然初衷良好，但会加剧语言最大的问题之一：版本已经太多。

### 设计错误

没有编程语言是完美的。JavaScript 也有自己的设计错误，例如将 `+` 重载为用于加法和字符串拼接，以及容易出错的 `with` 语句应该被避免。保留字策略过于复杂。分号自动插入是一个巨大的错误，字面量表达式的表示也是如此。这些错误导致了编程错误，并对语言的整体设计提出了质疑。幸运的是，许多问题可以通过良好的 `lint` 工具来缓解。

### 糟糕的实现

早期 JavaScript 的某些实现存在很多 Bug。这给该语言造成了负面影响。更糟糕的是，这些实现被嵌入在 Bug 满出的 Web 浏览器中。

### 糟糕的书籍

几乎所有关于 JavaScript 的书都非常糟糕。它们包含错误、糟糕的示例，并推广了不良的实践。该语言的重要特性往往解释得很糟糕，或者完全被忽略。我审查了几十本 JavaScript 书籍，我可以推荐一本：David Flanagan 编写的《JavaScript 权威指南》（第 5 版）。（致作者们：如果你写了一本好书，请给我寄一份审读副本。）

### 不达标的标准

该语言的官方规范由 ECMA 发布。该规范的质量极差。它难以阅读，非常难以理解。这是导致“糟糕书籍”问题的原因之一——作者无法利用标准文档来提高对语言的理解。ECMA 和 TC39 委员会应该感到深表羞愧。

### 业余

大多数编写 JavaScript 的人并不是程序员。他们缺乏编写良好程序的训练和自律。JavaScript 拥有如此强大的表达能力，以至于他们可以用它来做实用的事情。这给 JavaScript 带来了一种“专为业余人士设计”的声誉，认为它不适合专业编程。事实并非如此。

### 面向对象

JavaScript 是面向对象的吗？它拥有包含数据和操作这些数据的方法。对象可以包含其他对象。它没有类，但它有作为类的构造函数，作为类变量和方法的容器。它没有面向类的继承，但它有面向原型的继承。

构建对象系统的两种方式是通过继承（is-a）和聚合（has-a）。JavaScript 两者兼顾，但由于它的动态性质允许它在聚合处执行。

一些人认为 JavaScript 并不是真正的面向对象，因为它没有提供信息隐藏。所有成员都是公开的。

> http://www.amazon.com/exec/obidos/ASIN/0596101996/rrfdlwideeb
> http://www.ecma-international.org/publications/standards/Ecma-262.htm
> http://www.ecma-international.org/

但事实证明 JavaScript 对象可以拥有私有变量和私有方法。当然，很少有人理解这一点，因为 JavaScript 是世界上最被误解的编程语言。

一些人认为 JavaScript 不是真正的面向对象，因为它没有提供继承。事实证明 JavaScript 不仅支持经典继承，还支持代码重用模式。

## 理解 JavaScript 函数调用和 "this"

原文：http://yehudakatz.com/2011/08/11/understanding-javascript-function-invocation-and-this

Yehuda Katz, yehudakatz.com

多年来，我看到很多关于 JavaScript 函数调用的困惑。特别是，许多人抱怨函数调用中 `this` 的语义令人困惑。

在我看来，很多这种困惑可以通过理解核心函数调用原语，然后将所有其他调用函数的方式视为在原语之上的“语法糖”来得以解决。事实上，这正是 ECMAScript 规范考虑它的方式。在某些领域，本文是对事实的简化，但基本思想是相同的。

### 核心原语

首先，让我们看看核心函数调用原语，即 `Function` 的 `call` 方法。`call` 方法相对直接。

1. 从参数 1 到末尾创建一个参数列表 (`argList`)
2. 第一个参数是 `thisValue`
3. 将 `this` 设置为 `thisValue` 并将 `argList` 作为参数调用函数

例如：

```javascript
function greet(name) {
  console.log(this, name);
}
var obj = { name: "Object" };
greet.call(obj, "World"); // 输出: Object World
```

### 简单调用

调用函数（即 `func(...args)`）的效果与 `func.call(window, ...args)` 相同。在 ES5 严格模式下，`thisValue` 为 `undefined`。

```javascript
function greet(name) {
  console.log(this, name);
}
greet("World"); // 输出: Window World (或严格模式下 undefined World)
```

### 成员函数调用

当函数作为对象属性调用时（即 `obj.func(...args)`），效果与 `obj.func.call(obj, ...args)` 相同。

```javascript
var obj = {
  name: "Object",
  greet: function(name) {
    console.log(this, name);
  }
};
obj.greet("World"); // 输出: Object World
```

### 使用 Function.prototype.bind

有时需要将函数作为回调传递，但需要保持 `this` 指向特定对象。ES5 提供了 `Function.prototype.bind`。

```javascript
var person = {
  name: "Brendan Eich",
  hello: function(thing) {
    console.log(this.name + " says hello " + thing);
  }
};

var boundHello = person.hello.bind(person);
boundHello("world"); // "Brendan Eich says hello world"
```

当你需要传递一个原始函数作为回调函数时，这种方法最为有用：

```javascript
var person = {
  name: "Alex Russell",
  hello: function() { console.log(this.name + " says hello world"); };
}
$("#some-div").click(person.hello.bind(person));
// 当点击 div 时，会打印 "Alex Russell says hello world"
```

当然，这确实有些笨拙，TC39（负责开发 ECMAScript 下一个版本的委员会）正在致力于一种更优雅且向后兼容的解决方案。

### jQuery

由于 jQuery 大量使用匿名回调函数，因此它在内部使用 `call` 方法将这些回调函数的 `this` 值设置为更有用的值。例如，jQuery 不再像所有事件处理程序中那样接收 `window`（如果你不进行特殊干预将会是这样），而是在回调函数上调用 `call`，并将设置事件处理器的元素作为其第一个参数传入。

这非常有用，因为匿名回调函数中 `this` 的默认值并不特别有用，但它可能会给 JavaScript 初学者留下一种印象，认为 `this` 总体上是一个奇怪的、经常发生变化且难以理解的概念。

如果你理解将语法糖调用转换为去语法糖的 `func.call(thisValue, ...args)` 的基本规则，你就应该能够驾驭 JavaScript 中极其险恶的 `this` 值水域。

### 备注：我作弊了

在几处地方，我对实现的细节与规范的字面描述略有不同。可能最重要的图表是我处理 `func.call("primitive")` 的方式。实际上，规范中有一个原始类型（内部称为 `[[Call]]`），`func.call` 和 `[obj.]func()` 都可以调用它。

不过，来看 `func.call` 的定义：

1. 如果 `IsCallable` 为 `false`，则抛出 `TypeError` 异常。
2. 让 `argList` 为空列表。
3. 如果调用此方法时有多于一个参数，则从左到右从 `arg1` 开始，将参数作为最后一个元素添加到 `argList` 中。
4. 返回调用 `func` 的 `[[Call]]` 内部方法的结果，提供 `thisArg` 作为 `this` 值，并将 `argList` 作为参数列表。

如你所见，这个定义本质上是一个非常简单的 JavaScript 语言到原始 `[[Call]]` 操作的绑定。

如果你查看调用函数的定义、其生命周期、设置 `thisValue` 和 `argList` 的初始步骤，以及最后一步：“返回调用 `func` 的 `[[Call]]` 内部方法的结果，提供 `thisValue` 作为值，并提供 `argList` 作为参数值。”

它们的顺序本质上是相同的，只是 `argList` 和 `thisValue` 已经确定了。

我在调用原始 `call` 时稍微作了点作弊，但其含义与我在文章开头提取并逐字引用的规范内容本质上是一样的。

| 原文链接 | 作者信息 |
| :--- | :--- |
| http://javascript.crockford.com/code.html | Douglas Crockford, crockford.com |

这是一组用于 JavaScript 编程的编码规范和规则。它的灵感源自 Sun《Java 编程语言代码规范》。当然，它经过了大量的修改，因为 JavaScript 不是 Java。

软件对组织的长期价值与其代码库的质量成正比。在整个生命周期内，一个程序会被许多双手和许多眼睛处理。如果一个程序能够清晰地传达其结构和特征，那么它在不久的将来被修改时崩溃的概率就会降低。

代码规范有助于减少程序的脆弱性。

你所有的 JavaScript 代码都直接面向公众。它们应该始终保持出版级水平。整洁非常重要。

### JavaScript 文件

JavaScript 程序应该存储在 `.js` 文件中并交付。

除非代码特定于单个会话，否则不应将 JavaScript 代码嵌入 HTML 中。在 HTML 中添加代码会显著增加页面权重，且无法通过缓存和压缩来缓解。

`<script src="filename.js">` 标签应该尽可能放在 `body` 的最后。这可以减少脚本加载对其他页面组件造成的延迟影响。没有必要使用 `language` 或 `type` 属性。决定 MIME 类型的是服务器，而不是脚本标签。

### 缩进

缩进单位是四个空格。应避免使用制表符，因为（在本文写作的 21 世纪）还没有制表符位置的标准。使用空格可能会产生更大的文件大小，但在局域网上这种差异并不显著，而且差异可以通过代码压缩消除。

### 行长度

避免超过 80 个字符的行。当一个语句无法单行显示时，可能需要将其断开。在操作符之后断开，最好在逗号之后。在操作符后断开可以减少因分号插入而掩盖复制粘贴错误的概率。后续行应缩进 8 个空格。

### 注释

慷慨地写注释。留下一些信息供以后的人（可能是你自己）阅读是有用的，因为他们将需要理解你做了什么。注释应该写得良好且清晰，就像它们所注释的代码一样。偶尔的一点幽默可能会受到欢迎，但挫败感和牢骚则不会。

保持注释更新至关重要。错误的注释会让程序更难以阅读和理解。

让注释具有意义。关注可见的内容。

```javascript
i = 0; // 设置 i 为零。
```

### 变量声明

所有变量都应在使用之前声明。JavaScript 没有块级作用域，因此在块中定义变量可能会困扰习惯于其他语言的程序员。

```javascript
var currentEntry; // 类名数组
var level;        // 缩进
var size;         // 表格大小
```

最好每个变量单独占一行。写在函数顶部。应尽量减少全局变量的使用。

### 函数声明

所有函数都应在使用之前声明。内部函数跟在 `var` 语句之后。函数名与参数列表的 `(`（左括号）之间不应有空格。在 `)`（右括号）和起始语句的 `{`（左花括号）之间有一个空格。函数体本身缩进四个空格。

```javascript
function outer(c, d) {
    var e = c;

    function inner(a, b) {
        return a + b;
    }

    return inner(0, 1);
}
```

这种规范在 JavaScript 中效果良好，因为在 JavaScript 中，函数和对象字面量可以放置在任何允许表达式的地方。它为内联函数和复杂结构提供了最佳的可读性。

```javascript
function getElementsByClassName(className) {
  var results = [];
  walkDOM(document.body, function (node) {
    var a; // 类名数组
    var c = node.className; // 节点的 className
    var i; // 循环计数
    // 如果节点有类名，将其拆分为一个简单名称的列表。
    // 如果其中任何一个与请求的匹配，则将节点添加到结果集中。
    if (c) {
      a = c.split(' ');
      for (i = 0; i < a.length; i++) {
        if (a[i] === className) {
          results.push(node);
          break;
        }
      }
    }
  });
  return results;
}
```

如果函数字面量是匿名的，`function` 单词与 `(`（左括号）之间应该有一个空格。如果省略了空格，看起来就像函数的函数名是 `function`，这是一种错误的解读。

```javascript
div.onclick = function (e) {
  return false;
};

that = {
  method: function () {
    return this.datum;
  },
  datum: 0
};
```

应尽量减少全局函数的使用。

当需要立即调用函数时，整个调用表达式应该包装在括号中，以便清楚地表明产生的值是函数的结果而不是函数本身。

```javascript
var collection = (function () {
  var keys = [], values = [];
  return {
    get: function (key) {
      var at = keys.indexOf(key);
      if (at >= 0) {
        return values[at];
      }
    },
    set: function (key, value) {
      var at = keys.indexOf(key);
      if (at < 0) {
        at = keys.length;
      }
      keys[at] = key;
      values[at] = value;
    },
    remove: function (key) {
      var at = keys.indexOf(key);
      if (at >= 0) {
        keys.splice(at, 1);
        values.splice(at, 1);
      }
    }
  };
});
```

### 命名

名称应由 26 个大小写字母（A .. Z, a .. z）、10 个数字（0 .. 9）以及 `_`（下划线）组成。避免使用国际字符，因为它们在某些地方可能无法良好阅读或无法理解。不要在名称中使用 `$`（美元符号）或 `\`（反斜杠）。

不要使用 `_`（下划线）作为名称的第一个字符。它有时用于表示隐私，但它并不能提供隐私保护。如果隐私很重要，请使用提供私有成员的形式。避免使用表现出能力不足的约定。

大多数变量和函数应该以小写开头。

必须配合 `new` 使用的构造函数应以大写开头。如果省略了必要的 `new`，JavaScript 既不会引入编译时警告，也不会引入运行时警告。如果不使用 `new` 可能会发生糟糕的事情，因此大写规范是我们拥有的唯一防御。

全局变量应该使用全大写。（JavaScript 没有宏或常量，因此使用全大写来表示 JavaScript 并不具备的特性并没有太大意义。）

### 语句

#### 简单语句

每行最多包含一条语句。在每个语句的末尾加上一个 `;`（分号）。请注意，赋值函数字面量或对象字面量的赋值语句仍然是赋值语句，并且必须以分号结尾。

JavaScript 允许将任何表达式用语句。这可能会掩盖某些错误，特别是在存在分号自动插入的情况下。只有赋值和调用应该作为语句使用。

#### 复合语句

复合语句是指包含在 `{ }`（大括号）中的语句列表的语句。

- 包含的语句应缩进四个空格。
- `{`（左大括号）应该位于语句开始所在行的末尾。
- `}`（右大括号）应该另起一行，并缩进以与包含匹配的 `{`（左大括号）的行对齐。
- 当语句是控制结构（如 `if` 或 `for` 语句）的一部分时，所有语句（即使是单个语句）都应该使用括号包裹。这有助于添加语句而不会意外引入 bug。

#### 标签

语句标签是可选的。只有这些语句应该标记标签：`while`, `do`, `for`, `switch`。

#### return 语句

带有值的 `return` 语句不应在值周围使用 `()`（括号）。返回值表达式必须与 `return` 关键字在同一行开始，以避免分号自动插入。

#### if 语句

`if` 类的语句应具有以下形式：

```javascript
if (condition) { statements }
if (condition) { statements } else { statements }
if (condition) { statements } else if (condition) { statements } else { statements }
```

#### for 语句

`for` 类的语句应具有以下形式：

```javascript
for (initialization; condition; update) { statements }
for (variable in object) { if (filter) { statements } }
```

第一种形式应用于数组。第二种形式应用于对象。

注意使用 `hasOwnProperty` 方法来区分对象的成员：

```javascript
for (variable in object) { if (object.hasOwnProperty(variable)) { statements } }
```

#### while 语句

`while` 语句应具有以下形式：

```javascript
while (condition) { statements }
```

#### do 语句

`do` 语句应具有以下形式：

```javascript
do { statements } while (condition);
```

#### switch 语句

`switch` 语句应具有以下形式：

```javascript
switch (expression) {
case expression:
    statements;
    break;
default:
    statements;
}
```

#### try 语句

`try` 类的语句应具有以下形式：

```javascript
try { statements } catch (error) { statements } finally { statements }
```

#### continue 语句

`continue` 语句应具有以下形式：

```javascript
continue;
```

### 空格

空行通过分隔区域来提高可读性。

### 额外建议

#### {} 和 []

使用 `{}` 代替 `new Object()`。使用 `[]` 代替 `new Array()`。

当成员名称是顺序的使用数组。当名称是任意的使用对象。

#### 块作用域

JavaScript 中的块没有作用域。只有函数有作用域。除非复合语句需要，否则不要使用块。

#### 赋值表达式

避免在 `if` 和 `while` 的条件部分进行赋值。

是

```javascript
if (a = b) {
```

正确的语句？还是

```javascript
if (a == b) {
```

符合预期？

#### === 和 !== 运算符

几乎总是使用 `===` 和 `!==` 运算符。避免类型转换。特别是，不要使用 `==` 来比较假值。

#### 混淆的加号

小心不要在 `+` 后面跟着 `++`。这种模式可能会引起混淆。在它们之间插入括号使你的意图清晰。

```javascript
total = subtotal + +myInput.value;
```

为了更清晰，最好写成：

```javascript
total = subtotal + (+myInput.value);
```

#### eval 是邪恶的

`eval` 函数是 JavaScript 中被误用最多的特性。避免使用它。`eval` 有别名。不要使用 `Function` 构造函数。不要向 `setTimeout` 传递字符串。

## JavaScript 中的分号是可选的

原文：[Semicolons in JavaScript](http://mislav.uniqpath.com/2010/05/semicolons/)

Mislav Marohnić, mislav.uniqpath.com

JavaScript 是一种语句终止符是可选的脚本语言，例如：

- optional（形容词）：可选的，而非强制的

然而，关于这一特性存在大量的 FUD（恐惧、不确定性和怀疑），作为结果，我们社区的大多数开发者都会建议始终包含分号，以确保安全。

为了什么安全？我一直在寻找程序员强制自己使用分号的理由。以下是我通常发现的：

> http://stackoverflow.com/questions/444080/do-you-recommend-using-semicolons-after-every-statement-in-javascript

### 规范是晦涩的，且 JavaScript 的实现存在差异

自动分号插入的规则已列于此地，虽然对于普通读者来说有些难以理解，但它们是明确列出的。至于那些对这些规则的解释存在差异 JavaScript 实现，我尚未发现过任何一个。当我询问开发者这个问题，或者发现归档的讨论时，他们通常会说：“是的，这个浏览器在这里完全坏了，”或者“我只是单纯忘记了。”当然，他们从没有记起来。

我编写不带分号的代码，根据我的经验，没有哪个 JavaScript 解释器无法处理它的。

### 没有分号，你无法压缩 JavaScript 代码

缩小 JavaScript 源代码文件尺寸有三个级别：压缩（gzip）、最小化（移除不必要的空格和注释）和混淆（更改代码、缩短变量和函数名）。

像 gzip 这样的压缩是最简单的；它需要一次性的服务器配置，不需要开发者付出额外努力，而且不会改变你的代码。曾有一段时间 IE6 无法处理它，但如果我没记错，它在年前已经修补并作为 Windows 更新发布了，现在很少关心这个问题。

最小化和混淆会改变你的代码。它们是你在源代码上运行的工具，并说：“这里有一些 JavaScript 文件，尝试让它们变小，但不要改变功能”。我不愿意使用这些工具，因为许多开发者报告说，如果我不使用特定的编码风格（例如编写分号），它们就会弄坏我的代码。我不介意人们（社区）对我强加某些编码风格，但我介意工具。

假设我的代码在我目标的所有 JavaScript 实现（主流浏览器和一些服务器端实现）中都能运行。如果我通过你的最小化工具运行它弄坏了我的代码，那么我会报告你的代码是坏的。如果这个工具编辑 JavaScript 代码，它最好能像真正的解释器一样理解它。

在谈到最小化话题时，让我们做一个现实检查。我获取了 jQuery 源代码并删除了所有的分号，然后运行了 Google Closure Compiler。结果大小为 76,673 字节。原始 "jquery.min.js" 的大小为 76,674（多出 1 个）。所以你看，几乎没有变化；而且，这个测试像以前一样通过了。

这怎么可能？嗯，考虑这段代码：

```javascript
var a=1
var b=2
var c=3
```

光是这里就有 24 字节。到处盖上分号并运行最小化工具：

```javascript
var a=1;var b=2;var c=3;
```

仍然是 24 字节。所以，添加分号并移除换行符为我们节省了整整零字节。最小化后的大部分尺寸减少不是通过移除换行字符获得的——而是得益于移除代码注释和开头的缩进。

**更新：** 许多人指出，他们的最小化工具会将此表达式重写为 `var a=1,b=2,c=3`。我知道有些工具会这样做，但这篇文章的重点仅仅是探索分号与空格的关系。如果一个最小化工具能够重写表达式（例如 Closure Compiler），意味着它能够自动插入分号。

此外，还有人建议强制自己对块结构使用大括号，即使它们只有一行：

```javascript
// 之前
if(condition) stuff()

// 之后
if(condition){
stuff()
}

// 最小化之后
if(condition){stuff()}
```

强制使用大括号即使在最小化后也会为我们的表达式增加一个字节。我不确定这有什么好处——这既不是为了尺寸，也不是为了可读性。

这里是你可能感兴趣的其他对空格敏感的语言：

- Ruby — 在带有运算符和方法调用的表达式中处理空格可能会破坏代码
- Python — 如此。
- HTML — 参见 Kangax 的 HTML 最小化工具
- Haml 模板

当然，服务器端不需要最小化。我列出这个列表是为了接下来的论点：空格可以是、且通常是（标记）语言的一部分。这并不一定是一件坏事。

### 这是一种良好的编码风格

也被听作：

- 为了一致性，拥有它们是好的
- JSLint 会抱怨
- Douglas Crockford 是这么说的。

这是表达“大家都是这么做的”观念的另一种方式，被人们在在线讨论中（相当常见的）缺乏论据的情况下使用。

我对 JSLint 的建议是：不要用它。你为什么要用它？如果你相信它可以帮助你的代码产生更少的 bug，这里有一个新发现：只有人可以检测并解决 bug，而不是工具。与其使用工具，不如让更多人来看你的代码。

Douglas Crockford 说过“四种情况”，而大多数流行的 JavaScript 库要么设置为 Tab，要么设置为两个 Tab。不同项目的社区各不相同，这本就应该是如此。正如我之前所说：让人们来塑造你的编码风格，而不是某些简单的人或工具。

你可能会注意到，在这篇文章中我并没有要求你编写无分号的代码。我只是在列出具体的证据。

### 分号插入在 return 语句中反噬

当我搜索“分号插入”时，这是大多数博客文章描述的问题：

```javascript
function add() {
    var a = 1, b = 2
    return
    a + b
}
```

当你试图理解为什么有人想换行写返回语句时，我们可以看到这个语句是如何解释的：

```javascript
return;
a + b;
```

唉，函数没有返回我们想要的和！但你知道吗？这个问题并不是通过在返回表达式末尾添加分号（即 `a + b` 之后）解决的。它是通过移除 `return` 之后的换行符解决的：

```javascript
return a + b
```

尽管如此，令人难以置信的是，这些人实际上建议读者通过到处添加分号来避免此类问题。呃，这对于这种情况完全没有帮助。我们只需要理解语言是如何解析的。

### 无分号编码时唯一的陷阱

如果你选择无分号编码，这是唯一需要注意的一点：

```javascript
// 注意：会破坏
a = b + c
(d + e).print();
```

这实际上被求值为：

```javascript
a = b + c(d + e).print();
```

这个示例取自一篇关于 JavaScript 2.0 未来兼容性的文章，但我在使用模块模式时在自己的程序中遇到过几次。

简单的解决方案：当行以括号开头时，在其前面加上分号：

```javascript
;(d + e).print()
```

这可能并不优雅，但有效。Michael John Clement 进一步阐述了这一点：

如果你选择在可能的情况下省略分号，我的建议是在任何以圆括号或方括号开头的语句之前立即插入分号，或者任何以 `/`, `+`, 或 `-` 等算术标记开头的语句（如果你恰好写了这样的语句）。

采用这一建议作为规则，你就会没事的。

# 模式与代码组织

## 常见的 JavaScript “陷阱”

原文文章：http://www.jblotus.com/2013/01/13/common-javascript-gotchas

James Fuller, Jblotus

PHP 是我的第一种编程语言，我最初通过 jQuery 这样的库接触到 JavaScript。JavaScript 中有些东西，由于它们的工作方式与 PHP 不同，在刚开始时总是让我感到困惑。即使在今天，仍然有一些东西让人感到困惑。我想分享一些我在开始使用 JavaScript 时遇到过的困扰。我将涵盖全局命名空间、`this`、了解 ECMAScript 3 和 ECMAScript 5 之间的区别、异步操作、原型以及简单的 JavaScript 继承。

### 全局命名空间

特别是在 PHP 中，当你在类（或命名空间块）之外声明变量或函数时，你本质上是将该函数添加到全局命名空间中。在 JavaScript 中，并没有所谓的“命名空间”，而是所有内容都挂载到全局对象上。在浏览器中，那就是 `window` 对象。另一个关键区别是，在 JavaScript 中，函数和变量是全局对象的属性，我们通常称其为属性。

这可能会带来麻烦，因为在 JavaScript 中覆盖全局函数或属性时不会收到警告，这实际上是非常危险的。

```javascript
function globalFunction() {
  console.log('I am the original global function');
}
function overWriteTheGlobal() {
  globalFunction = function() {
    console.log('I am the new global function');
  };
}
globalFunction(); // 输出 "I am the original global function"
overWriteTheGlobal(); // 这将覆盖原始全局函数
globalFunction(); // 输出 "I am the new global function"
```

使用 JavaScript 确保变量和函数自包含的一项技术是使用立即调用函数表达式（IIFE），通常称为自执行匿名函数。我通常通过向函数传递一个载体对象向外部世界暴露。这是模块模式的一种变体。

```javascript
var module = {};
(function(exports) {
  exports.notGlobalFunction = function() {
    console.log('I am not global');
  };
}(module));

function notGlobalFunction() {
  console.log('I am global');
}

notGlobalFunction(); // 输出 "I am global"
module.notGlobalFunction(); // 输出 "I am not global"
```

在自执行匿名函数内部，所有的全局作用域都被封装起来，我们通过将其挂载到 `module` 变量来完成。从技术上讲，你可以直接向 `module` 变量添加属性，但我们将其传递给函数是为了明确我们正在将函数挂载到什么上。它还允许我们在函数内部对传入的对象取别名。这里的关键在于我们预先声明了依赖，而不是依赖 `module` 变量以外的全局变量。

你可能注意到了 `var` 关键字。如果你不确定如何使用，基本的解释是：在变量声明前加上 `var` 会在最近的包含它的函数上创建一个属性。如果你省略了 `var` 关键字，就意味着你想给作用域链上方的一个现有赋值赋值，这个变量可能是全局作用域，也可能不是。

```javascript
var imAGlobal = true;
function globalGrabber() {
  imAGlobal = false;
  return imAGlobal;
}
console.log(imAGlobal); // 输出 "true"
console.log(globalGrabber()); // 输出 "false"
console.log(imAGlobal); // 输出 "false"
```

如你所示，在函数中依赖全局变量是危险的，因为不可避免会产生副作用和冲突。当我们使用 `var` 关键字时会发生什么？

```javascript
var imAGlobal = true;
function globalGrabber() {
  var imAGlobal = false;
  return imAGlobal;
}
console.log(imAGlobal); // 输出 "true"
console.log(globalGrabber()); // 输出 "false"
console.log(imAGlobal); // 输出 "true"
```

JavaScript 将 `var` 声明提升到函数块的顶部，然后初始化变量。这被称为变量提升。

**总结：** 所有变量都作用域于一个函数（函数本身是一个对象），而你在何处使用 `var` 声明这些变量决定了它们所属的函数。省略 `var` 则意味着该变量具有全局作用域。

让我们看看变量提升是如何发生的：

```javascript
function variableHoist() {
  console.log(hoisty);
  hoisty = 1;
  console.log(hoisty);
  var hoisty = 2;
  console.log(hoisty);
}

variableHoist();
// 输出 undefined（如果作用域内没有 var 声明，将得到 ReferenceError）
// 输出 "1"
// 输出 "2"
```

```javascript
try {
  console.log(hoisty); // 输出 ReferenceError (没有全局变量 "hoisty"）
} catch (e) {
  console.log(e);
}
```

如你所示，你在函数中放置 `var` 声明的位置并不重要，因为该属性在函数执行任何代码之前就已经创建了。在实践中，你通常希望将 `var` 声明放在函数顶部，因为它们最终会回到那里。在函数顶部初始化变量也是完全可以的。

### 理解 “this”

由于 JavaScript 使用函数作用域，`this` 的含义与 PHP 有很大不同。考虑以下情况：

```javascript
console.log(this); // 输出 window object
var myFunction = function() {
  console.log(this);
}
myFunction(); // 输出 window object
var newObject = {
  myFunction: myFunction
}
newObject.myFunction(); // 输出 newObject
```

`this` 默认指向调用它的对象。当我们将 `myFunction()` 调用到 `newObject` 时，`this` 现在指向 `newObject`。在 PHP 和其他语言中，`this` 总是指向类的实例。

```javascript
var myFunction = function(arg1, arg2) {
  console.log(this, arg1, arg2);
};
var newObject = {};
myFunction.call(newObject, 'foo', 'bar'); // 输出 newObject "foo" "bar"
myFunction.apply(newObject, ['foo', 'bar']); // 输出 newObject "foo" "bar"
```

但让我们领先一步。我们都是通过将想要使用的对象值作为第一个参数来替换 `this` 值。`call()` 和 `apply()` 之间的根本区别在于传递参数的方式。`call()` 可以在第一个参数之后接受无限数量的参数，而 `apply()` 期望一个数组作为第二个参数。

像 jQuery 这样的库通过这种方式执行大量逻辑。让我们看看 jQuery 的 `.each()` 方法：

```javascript
var els = $('div'), $('span');
var handler = function() {
  console.log(this);
};

$.each(els, handler);

// 迭代 1 输出 wrapped jquery element for "div"
// 迭代 2 输出 wrapped jquery element for "span"
handler.apply({}); // 输出 object
```

jQuery 会重写 `this` 的值，因此你应该始终意识到它在 jQuery 事件处理程序或其他结构中的含义。

### 了解 ECMAScript 3 和 ECMAScript 5 之间的区别

多年来，ECMAScript 3 一直是现代浏览器的标准，但近来 ECMAScript 5 已经进入了大多数现代浏览器（IE 仍然落后）。ECMAScript 5 为 JavaScript 引入了许多实用的功能以及一些以前依赖库的原生方法，例如 `String.trim()` 和 `Array.forEach()`。问题是，如果你的用户在使用 Internet Explorer，你仍然无法依赖这些方法在浏览器环境中的可用性。

看看我们在 IE 8 中使用 `String.trim` 时会发生什么：

```javascript
var fatString = " my string ";

// 在现代浏览器中 输出 " my string "
console.log(fatString); // 输出 "my string"
console.log(fatString.trim()); // 输出 "my string"

// 在 IE 8 中
console.log(fatString.trim()); // 错误：对象不支持属性或方法 'trim'
```

因此，我们可以使用像 `jQuery.trim()` 这样的方法来为我们完成工作，我相信如果你的浏览器支持 `String.trim()`，它将回退到该方法以提高性能（因为浏览器的原生实现速度更快）。

你可能并不关心，甚至不需要了解 ECMAScript 3 和 ECMAScript 5 之间的所有差异，但查阅 Mozilla 开发者网络 (MDN) 的函数参考以首先查看语言的可用版本通常是一个好主意。通常情况下，如果你使用像 jQuery 或 underscore 这样的库来为你处理这些问题，那么应该是没问题的。

如果你有兴趣为旧浏览器使用 ECMAScript 5 的填充程序，请查看 https://github.com/kriskowal/es5-shim

### 理解异步

在我刚开始学习 JavaScript（特别是 jQuery）时，让我感到困惑的问题之一是某些操作是异步的。很多时候，我以过程化的方式编写代码，期望结果会立即返回，但并没有意识到这一点。

看看下面这段错误的代码：

```javascript
var remoteValue = false;
$.ajax({
  url: 'http://google.com',
  success: function() {
    remoteValue = true;
  }
});

console.log(remoteValue); // 输出 "false"
```

可能需要一段时间才能意识到，你需要使用回调函数围绕异步调用编写程序，以处理 ajax 调用的结果。

```javascript
var remoteValue = false;
var doSomethingWithRemoteValue = function() {
  console.log(remoteValue); // 成功时输出 true
}

$.ajax({
  url: 'https://google.com',
  complete: function() {
    remoteValue = true;
    doSomethingWithRemoteValue();
  }
});
```

另一个很酷的功能是延迟（有时称为承诺/promises），你可以用它以更接近过程化的风格进行编程：

```javascript
var remoteValue = false;
var doSomethingWithRemoteValue = function() {
  console.log(remoteValue);
}

var promise = $.ajax({
  url: 'https://google.com'
});

// 输出 "true"
promise.always(function() {
  remoteValue = true;
  doSomethingWithRemoteValue();
});

// 输出 "foobar"
promise.always(function() {
  remoteValue = 'foobar';
  doSomethingWithRemoteValue();
});
```

你可以使用 promises 以链式回调的方式组织函数，在我看来，这种方式比嵌套回调更易处理，此外，这些对象还提供了许多其他益处。

浏览器中的动画也是异步的，因此这也是常见的困惑来源。

我在这里不会详细阐述，但你需要像处理 ajax 请求那样，通过回调函数来处理动画。我真的不是该主题的专家，所以请查阅 `jQuery.animate()` 方法。

### JavaScript 中的简单继承

粗略来说，JavaScript 通过克隆对象来扩展它们，而 PHP、Ruby、Python 和 Java 则使用并扩展类。在 JavaScript 中，你有被称为“原型”的东西，每个对象都有一个原型。事实上，函数、字符串、数字和对象都有共同的祖先 `Object`。关于原型有两点需要记住：蓝图和链。

每个原型本身就是一个对象，它描述了创建对象实例时可用的属性。原型链允许原型扩展其他原型。事实上，原型可以拥有原型。当某个方法或属性在对象上不存在时，它会查找该对象的原型，然后是原型的原型，直到找到它，或者如果属性找不到则返回 `undefined`。

幸运的是，初学者通常不需要纠结这些内容，因为只需创建一个对象字面量并在运行时向它添加属性。

```javascript
var obj = {};
obj.newFunction = function() {
  console.log('I am a function');
}
obj.newFunction();
```

扩展对象的另一种简单方法是使用 `jQuery.extend()`：

```javascript
var obj = {
  a: 'i am a property'
}
var newObj = {
  b: function() {
    return 'i am a function'
  }
}
var finalObj = $.extend({}, obj, newObj);

console.log(finalObj.a); // 输出 "i am a property"
console.log(finalObj.b); // 输出 "i am a function"
```

ECMAScript 5 提供了 `Object.create()`，你可以用它来扩展现有对象，但你可能需要避免这样做以支持旧浏览器。它在属性创建和设置方面具有独特的优势。

## 处理异步代码的四种方式

原文文章：http://www.jblotus.com/2013/01/13/four-ways-to-handle-asynchronous-code-in-javascript

James Fuller, Jblotus

在 JavaScript 中处理异步代码有四种主要方式：回调、监听器、流程控制库和 Promise。每种方式都有其优缺点。

### 回调

回调是最简单、最常见的方式。一个回调函数作为参数传递给另一个函数，在异步操作完成后调用。

```javascript
function finder(records, cb) {
  setTimeout(function () {
    records.push(3, 4);
    cb(records);
  }, 1000);
}

function processor(records, cb) {
  setTimeout(function () {
    records.push(5, 6);
    cb(records);
  }, 1000);
}

function onProcessorDone(records) {
  console.log(records);
}

function onFinderDone(records) {
  processor(records, onProcessorDone);
}

finder([1, 2], onFinderDone);
```

在两种情况下，上面的控制台都会输出日志 `[1,2,3,4,5,6]`

**优点**

- 它们是一种非常出名的模式，因此非常熟悉且易于理解。
- 在你自己的库/函数中实现非常简单。

**缺点**

- 嵌套回调将形成臭名昭著的“回调地狱”，当有多个嵌套层时，它很难阅读。通过拆分函数可以很容易解决。
- 对于给定的事件只能传递一个回调，这在很多情况下是一个很大的限制。

### 监听器

监听器也是一种非常出名的模式，主要由 jQuery 和其他 DOM 库普及。一个监听器可能看起来像：

```javascript
finder.on('done', function (event, records) {
  // 执行一些事情
});
```

我们在一个带有监听器的对象上调用一个函数。在那个函数中，我们传递想要监听的事件名称和回调函数。`'on'` 是此函数的常用名称之一，你还会遇到其他名称有 `'bind'`, `'listen'`, `'addEventListener'`, `'observe'`。

#### 设置

让我们为监听器演示做一些设置。不幸的是，需要的设置比回调示例要复杂一些。

首先，我们需要几个对象来执行查找和处理记录的工作。

```javascript
var finder = {
  run: function (records) {
    var self = this;
    setTimeout(function () {
      records.push(3, 4);
      self.trigger('done', [records]);
    }, 1000);
  }
}

var processor = {
  run: function (records) {
    var self = this;
    setTimeout(function () {
      records.push(5, 6);
      self.trigger('done', [records]);
    }, 1000);
  }
}
```

注意它们在工作完成后调用了 `trigger` 方法，我将使用混入将此方法添加到这些对象中。再次，`'trigger'` 是你会遇到的名称之一，其他常用名称是 `'fire'` 和 `'publish'`。

我们需要一个具有监听行为的混合对象，在这种情况下我将直接依赖 jQuery：

```javascript
var eventable = {
  on: function(event, cb) {
    $(this).on(event, cb);
  },
  trigger: function (event, args) {
    $(this).trigger(event, args);
  }
}
```

然后将行为应用到我们的 finder 和 processor 对象：

```javascript
$.extend(finder, eventable);
$.extend(processor, eventable);
```

太棒了，现在我们的对象可以接受监听器并触发事件了。

#### 使用监听器

使用监听器的代码很简单：

```javascript
finder.on('done', function (event, records) {
  processor.run(records);
});
processor.on('done', function (event, records) {
  console.log(records);
});
finder.run([1,2]);
```

再次，控制台运行将输出 `[1,2,3,4,5,6]`

**优点**

- 这是另一个易于理解的模式。
- 大优势是你不再局限于每个对象一个监听器，你可以添加任意数量的监听器。例如：
  `finder.on('done', function (event, records) { .. 执行一些事情 }).on('done', function (event, records) { .. 执行其他事情 });`

**缺点**

- 在你的代码中设置回调稍微困难一点，你可能想使用像 jQuery、bean.js 这样的库。

### 流程控制库

流程控制库也是处理异步代码的一种棒的方法。特别流行的是 Async.js。

使用 Async.js 的代码如下：

```javascript
async.series([
  function(cb) { ... },
  function(cb) { ... }
]);
```

#### 设置 (示例 1)

同样我们需要几个执行工作的函数，就像其他示例一样，这些函数在现实世界中可能会发送 AJAX 请求并返回结果。现在我们只使用超时。

```javascript
function finder(records, cb) {
  setTimeout(function () {
    records.push(3, 4);
    cb(null, records);
  }, 1000);
}
function processor(records, cb) {
  setTimeout(function () {
    records.push(5, 6);
    cb(null, records);
  }, 1000);
}
```

Node 延续传递样式。注意上面函数内部回调使用的样式：`cb(null, records);`。如果没有发生错误，回调中的第一个参数为 `null`；如果发生错误，则为错误对象。这是 Node.js 库中的常见模式，因为 Async.js 使用了这种模式。通过使用这种样式，Async.js 和回调之间的流程变得超级简单。

#### 使用 Async

使用回调的代码如下：

```javascript
async.waterfall([
  function(cb) {
    finder([], cb);
  },
  function(records, cb) {
    processor(records, cb);
  }
], function(results) {
  console.log(results);
});
```

### Promise

Promise（承诺）是处理异步操作的一种现代方式，代表一个尚未完成但预期将来会完成的操作。

```javascript
var promise = new Promise(function(resolve, reject) {
  // 异步操作
  setTimeout(function() {
    resolve("Success!");
  }, 1000);
});

promise.then(function(result) {
  console.log(result); // "Success!"
}).catch(function(error) {
  console.error(error);
});
```

**优点**

- 避免了回调地狱，代码更易读、易维护。
- 支持链式调用，错误处理统一。

**缺点**

- 这些工具中最难理解的。
- 当你有大量在途中添加了监听器的聚合 Promise 时，它们可能会变得难以追踪。

## 结论

就是这些！在我看来，这是处理异步代码的四种主要工具。希望这能帮助你更好地理解它们，并为你的异步需求提供更多选择。

## 代码的设计：组织 JavaScript

原文文章：http://alistapart.com/article/the-design-of-code-organizing-javascript

Anthony Colangelo, alistapart.com

优秀的设计是对重要领域投入关注和用心的结果，从而产生一个有用、易于理解且尽可能美的用户界面。但不要被误导，认为设计仅仅是留给设计师的。

代码中存在着大量的设计，我指的不是构建用户界面的代码——而是代码的设计。

良好的代码更容易维护、优化和扩展，让开发人员更高效。这意味着可以将更多的精力和时间放在构建伟大的事物上，这让用户、开发者和利益相关者都开心。

代码设计有三个高层、与语言无关的方面特别重要。

- **系统架构**——代码库的基础布局。规范各种组件（如模型、视图和控制器）相互作用的规则。
- **可维护性**——代码在多大程度上可以改进和扩展？
- **可复用性**——应用程序组件的可复用性如何？每个组件的实现有多容易自定义？

在松散的语言中，特别是 JavaScript，编写良好的设计需要一点自律。JavaScript 环境非常宽容，以至于随处丢弃碎片代码程序也能正常运行。尽早建立系统架构（并坚持下去！）为你的代码库提供了约束，确保了始终的一致性。

我发现的一种方法是使用一种经典的软件设计模式——模块模式，它可扩展的结构有助于构建稳健的系统架构和可维护的代码库。我喜欢在 jQuery 插件中构建模块，这可以实现优美的复用性，提供健壮的选项，并暴露精良的 API。

下面，我将介绍如何将你的代码组织成良好的组件，这些组件可以在其他项目中被复用。

### 模块模式

设计模式有很多，关于它们的资源也很多。Addy Osmani 写了一本关于 JavaScript 设计模式的精彩（免费！）书籍，我强烈向所有水平的开发者推荐这本书。

模块模式是一种简单的结构基础，可以帮助保持代码的整洁和有序。“模块”只是一个包含方法和属性的标准对象字面量，而这种简单性是构建它最棒的一点：即使是不熟悉传统软件设计模式的人，也能查看并立即理解它是如何运作的。

在运行这种模式的应用程序中，每个组件都有它自己独特的模块。例如，为了构建完整的功能，你为文本框创建一个模块，为结果列表创建一个模块。这两个模块协同工作，但文本框不会触碰列表代码，反之亦然。

组件解耦是模块模式非常适合构建稳健系统架构的原因。应用程序内部的关系被定义得很好；与文本框相关的任何内容由文本框管理，而不是散落在整个代码库中——导致清晰的代码。

基于模块的组织的另一个好处是它具有内在的可维护性。模块可以独立地改进和优化，而不会影响应用程序的任何部分。

我将模块模式用于 jPanelMenu 的基本结构，这是我为离屏菜单系统构建的 jQuery 插件。我用它作为示例，说明了构建模块的过程。

### 构建模块

首先，我定义了三个方法和一个属性，用于管理菜单系统的交互。

```javascript
var jpm = {
  animated: true,
  openMenu: function () {
    this.setMenuStyle();
  },
  closeMenu: function () {
    ...
    this.setMenuStyle();
  },
  setMenuStyle: function () { ... }
};
```

这个思想是将代码拆分为尽可能微小、最可复用的片段。我可以只写一个 `toggleMenu()` 方法，但创建不同的 `openMenu()` 和 `closeMenu()` 方法在模块内部提供了更多的控制和可用性。

注意，模块内部对模块和属性的调用（例如对 `setMenuStyle()` 的调用）带有 `this` 关键字前缀——这就是模块访问其自身成员的方式。

这就是模块的基本结构。你可以根据需要继续添加方法和属性，但它并不会比此更复杂。在结构基础建立之后，可以在此基础上构建可复用选项和暴露的 API。

### jQuery 插件

良好设计的第三个方面可能是最关键的：可复用性。这一节带有一个说明。虽然显然有方法在原生 JavaScript 中构建和实现可复用组件（通过我们上面的模块我们已经完成了 90%），但出于某些原因，我更倾向于为更复杂的事情构建 jQuery 插件。

最重要的是，这是一种非侵入性的通信。如果你使用 jQuery 构建了一个组件，你应该让实现它的人一目了然。

```javascript
(function($) {
  $.jPanelMenu = function(options) {
    var jpm = $.extend({
      'animated': true,
      'duration': 500,
      'direction': 'left'
    }, options);

    var api = {
      openMenu: function () {
        ...
        this.setMenuStyle();
      },
      closeMenu: function () {
        ...
        this.setMenuStyle();
      },
      setMenuStyle: function () { ... }
    };

    return {
      open: api.openMenu,
      close: api.closeMenu,
      someComplexMethod: function () { ... }
    };
  };
}(jQuery));
```

通过插件初始化返回的对象，可以使用相应的 API 方法和属性。

```javascript
var jpm = $.jPanelMenu({
  duration: 1000,
  ...
});
jpm.open();
```

### 完善开发者接口

通过一些简单的结构和指南，我们自己构建了一个可重用、可扩展的插件，这将帮助我们的生活变得更轻松。就像我们所做的任何事情一样，请对这种结构进行实验，看看它是否适用于你、你的团队和工作流。

每当我发现自己正在构建某些具有重用可能性的时，我就会将其拆分为基于模块的 jQuery 插件。这种方法最好的部分在于，它迫使你使用并测试你编写的代码。通过在构建时使用它，你会快速识别优点、发现缺点并计划更改。

这个过程会产生经过实战检验的代码，用于开源贡献，或者这样进行分发。我已经将我（大部分）经过完善的插件作为开源项目发布在 GitHub 上。

即使你不是在构建一个要公开发布的程序，考虑代码的设计也是重要的。未来的自己会感谢你的。

## 为什么选择 AMD？

一个 JavaScript 模块加载器

![](img/5f4a286ef99041bf37736af72f6b8b9b_55_0.png)

这一页讨论了 JavaScript 模块的异步模块定义 (AMD) API 的设计动力和用法，这是 RequireJS 支持的模块 API。另一个页面讨论了 Web 模块的通用方法。

### 模块用途 § 1

什么是 JavaScript 模块？它们的目的是什么？

- **定义**：如何将一段代码封装成一个有用的单元，以及如何注册该模块的能力/导出一个值。
- **依赖引用**：如何引用其他代码单元。

### 现今 Web § 2

```javascript
(function () {
  var $ = this.jQuery;

  this.myExample = function () {};
});
```

JavaScript 代码段是如何定义的？

- 通过一个立即执行的工厂函数定义。
- 依赖的引用是通过 HTML script 标签加载的全局变量名定义的。
- 依赖关系是弱声明的：开发者需要知道正确的依赖顺序。例如，包含 Backbone 的文件不能出现在 jQuery 标签之前。
- 它需要额外的工具将一组 script 标签子集合并到一个标签中，以进行优化部署。

这对于管理大型项目可能会困难，特别是当脚本开始拥有许多依赖，且这些依赖可能会重叠和合并时。手动编写 script 标签扩展性并不好，缺少了按需加载脚本的能力。

### CommonJS § 3

```javascript
var $ = require('jquery');
exports.myExample = function () {};
```

原始的 CommonJS 列表参与者致力于制定出一个适用于今天 JavaScript 语言的模块格式。

- 通过一个工厂函数定义（不一定是立即执行）。
- 依赖通过 `require` 语句引用。
- 依赖关系是显式声明的。
- 模块通过 `exports` 导出值。

这解决了依赖管理问题，但它是同步的，不适合浏览器环境。

### AMD 定义 § 4

AMD (Asynchronous Module Definition) 规范定义了模块的标准格式。

```javascript
define('myModule', ['dep1', 'dep2'], function (dep1, dep2) {
  // 通过返回一个值来定义模块的值。
  return function () {};
});
```

- `define` 函数接受模块 ID（可选）、依赖数组和工厂函数。
- 依赖异步加载，加载完成后执行工厂函数。
- 适合浏览器环境。

### RequireJS § 5

RequireJS 是 AMD 规范的一个流行实现。它提供了模块加载、依赖管理和优化构建工具。

### 模块标识 § 6

在开发过程中，你应该避免自己手动命名模块，并且在一个文件中只放置一个模块。然而，为了工具化和性能考虑，模块解决方案需要一种在构建资源中识别模块的方法。

### Sugar 语法 § 7

AMD 示例在所有浏览器中都能运行。然而，存在与函数参数命名的依赖名称不匹配的风险，而且如果你的模块有许多依赖项，看起来可能会有些奇怪：

```javascript
define(["require", "jquery", "blade/object", "blade/fn", "rdapi",
"oauth", "blade/jig", "blade/url", "dispatch", "accounts",
"storage", "services", "widgets/AccountPanel", "widgets/TabButton",
"widgets/AddAccount", "less", "osTheme", "jquery-ui-1.8.7.min",
"query.jTextField"],
function(require, $, object, fn, rdapi,
oauth, jig, url, dispatch, accounts,
storage, services, AccountPanel, TabButton,
AddAccount, less, osTheme) {
});
```

为了方便起见，并且易于对 CommonJS 模块进行简单的封装，支持这种形式的 `define`，有时被称为“简化的 CommonJS 包装”：

```javascript
define(function(require) {
  var dependency1 = require('dependency1'),
      dependency2 = require('dependency2');
  return function () {};
});
```

AMD 加载器将通过 `Function.prototype.toString()` 解析 `require('')` 调用，然后在内部将 `define` 调用转换为标准形式：

```javascript
define(['require', 'dependency1', 'dependency2'], function (require) {
  var dependency1 = require('dependency1');
  var dependency2 = require('dependency2');

  return function () {};
});
```

这允许加载器异步加载 `dependency1` 和 `dependency2`，执行依赖项，然后执行此函数。

并不是所有浏览器都能可用的 `Function.prototype.toString()` 结果。截至 2011 年 10 月，PS 3 和 Opera Mobile 浏览器尚不支持。这些浏览器由于网络/设备限制，更有可能需要模块的优化构建，因此只需使用知道如何将这些转换为规范化依赖数组形式的优化器进行构建，例如 RequireJS 优化器。

由于不支持这种 `toString()` 扫描的浏览器数量非常少，因此对你的所有模块使用这种共享形式是安全的，特别是如果你喜欢将依赖名称与存储其模块值的变量对齐时。

### CommonJS 兼容性 § 8

尽管这种形式被称为“简化的 CommonJS 包装”，但它与 CommonJS 模块并不是 100% 兼容的。然而，那些不支持的情况在浏览器中可能也会崩溃，因为它们通常假设依赖项是同步加载的。

根据我（完全不科学的）个人经验，大约 95% 的 CJS 模块与简化的 CommonJS 包装完全兼容。

会崩溃的模块是那些对依赖项进行动态计算的模块、任何在 `require()` 调用中未使用字符串字面量的模块，以及任何看起来不像声明式 `require()` 调用的模块。

```javascript
// 错误
var mod = require(someCondition) ? 'a' : 'b';

// 错误
if (someCondition) {
  var a = require('a');
} else {
  var a = require('a1');
}
```

这些情况通常由 AMD 加载器中常见的回调 require（即 `require([moduleName], function () {})`）处理。

AMD 执行模型与 ECMAScript Harmony 模块的规范方式更加一致。在 AMD 包装中无法工作的 CommonJS 模块将无法工作。AMD 的执行行为更具未来兼容性。

### 冗余与实用性

AMD 的批评之一（与 CJS 模块相比）是它需要层层缩进和函数包装。

但事实是：感知的额外输入和使用 AMD 的层层缩进并不重要。你的时间大部分花在了这里：

- 问题的思考。
- 阅读代码。

虽然更少的单词通常更优，但 AMD 的额外输入并没有那么多。大多数 Web 开发者使用函数包装来避免全局变量污染页面。重要的是：能够与他人共享代码。AMD 是实现这一目标的最低路径。

返回一个函数作为模块值，特别是作为构造函数时，会导致更好的 API 设计。AMD 及其相关 API 显示了任何未来 JS 模块系统的威力。“return function”意味着不需要处理 `module.exports`，并且更加清晰。

一个工作且易于调试的模块系统对于今天的 JavaScript 来说是最好的。选择性地将一个模块加载到另一个模块是很容易的。AMD 有一些隐藏的成本：

- 工具化成本
- 在浏览器中崩溃的边缘情况，如跨域
- 随着时间推移持续增加的维护成本

### 今日 § 9

截至 2011 年 10 月中，AMD 在 Web 端已经有了良好的应用：

- 相关模块如 bonzo、qwery、bean 和 domready
- 用于 Firebug 1.8+
- jQuery 1.7
- Dojo 1.7
- EmbedJS
- 在 Firefox 的 Jetpack/Add-on SDK 中使用



- 用于 BBC 的部分网站⁶⁹（通过查看源码观察到 AMD/RequireJS 的官方推荐）

## 你可以做什么 § 10

如果你编写应用程序：

- 给一个 AMD 加载器试试。你有一些选择：
  - `RequireJS`⁷⁰
  - `curl`⁷¹
  - `Dojo`⁷² 1.7+

如果你想使用 AMD 但仍然采用在 HTML 页面底部单个脚本的方法：

- 使用 `RequireJS` 优化器⁷⁴，可以是命令行模式或带有 `almond shim`⁷⁶ 的 HTTP 服务⁷³。

如果你是脚本/库作者：

- 如果可用，可选 `define()`。很棒的是，你仍然可以在不依赖 AMD 的情况下编写你的库，只需在可用时参与即可。这允许你的模块的使用者：
  - 避免在页面中释放全局变量
  - 为代码加载、延迟加载提供更多选项
  - 使用现有的 AMD 工具优化你的项目
  - 参与今天浏览器中可行的模块系统。

如果你为 JavaScript 编写代码加载器/引擎/环境：

- 实现 AMD API⁷⁷。有一个讨论列表⁷⁹兼容性测试⁸⁰。实现 AMD 将帮助减少多模块系统的样板代码，并帮助在 Web 上证明一个可行的 JavaScript 模块系统。这可以反馈到 ECMAScript 过程中以构建原生模块支持。
- 同时也支持 `callback-require`⁸¹ 和加载插件⁸²。加载插件是减少回调/异步风格代码中可能出现的嵌套回调问题的极佳方法。

## JavaScript 依赖注入

> 原始文章
> http://merrickchristensen.com/articles/javascript-dependency-injection.html
> Merrick Christensen, merrickchristensen.com/*
> ⁷http://merrickchristensen.com/

得益于 `Require.js`⁸⁵ 和 `AngularJS`⁸⁶ 等项目，反转控制⁸³ 以及更具体说是依赖注入⁸⁴ 在 JavaScript 领域变得越来越流行。本文是对依赖注入的简要介绍，以及它是如何融入 JavaScript 的。它还将揭示 `AngularJS` 实现依赖注入的优雅方式。

## JavaScript 中的依赖注入

依赖注入通过允许我们在环境中模拟依赖项，从而允许一次只测试一个，促进了更好的测试。它通过将对象与其实现解耦，使我们能够编写更具维护性的代码。

通过依赖注入，依赖项会被传递给对象，而不是在对象内部创建或显式地引用它们。这意味着依赖注入器可以根据具体的上下文提供不同的依赖项。例如，在测试中，它可能会传递服务 API 的伪版本，它不会发送请求但返回静态对象；而在生产环境中，它产生实际的服务 API。

另一个例子可以是，当设备运行时，向你的视图对象传递 `ZeptoJS`* 而不是 `jQuery` 以提高性能。

采用依赖注入获得的主要好处如下：

1. 代码往往更具可维护性。
2. API 更加优雅和抽象。
3. 代码更容易测试。
4. 代码更具模块化和可重用性。
5. 治愈癌症。（不完全正确）。

将依赖项绑定到 API 的坏习惯会变成一个自然过程。面向接口编程并不新鲜，服务端世界测试这个想法已经很久久了，以至于语言本身都实现了接口的概念。在 JavaScript 中，我们必须强迫自己这样做。幸运的是，依赖注入和模块系统是深受欢迎的朋友。

现在你已经对依赖注入是什么有了一些了解，让我们看看如何以 `AngularJS` 风格的依赖注入*9 作为参考实现来构建一个简单的依赖注入器。此实现纯粹出于教学目的。

## AngularJS 风格注入

`AngularJS` 是少数几个完全采用依赖注入直到框架核心的前端 JavaScript 框架之一。对于许多开发者来说，`AngularJS` 中实现的依赖注入看起来完全像魔法一样。

在 `AngularJS` 中创建控制器时，参数是将被注入到你的控制器的依赖名称。参数名是这里的关键，它们被用来将依赖名称映射到实际依赖项。是的，“键”这个词是有意使用的，你会明白为什么的。

```javascript
/* 注入 */
var WelcomeController = function (Greeter) {
  /** 我希望动态注入一个不同的 Greeter。 **/
  Greeter.greet();
}
```

*http://zepto.com/
**http://www.webkit.org/
***http://jquery.com/
*9http://angularjs.org/

## 基础要求

让我们探讨为了让它工作而的一些要求。

1. `Injector` 需要知道函数是什么。
2. `Injector` 需要依赖项。

## 要求 1：让 Injector 感知

```javascript
var args = WelcomeController.toString().match(
  FN_ARGS
);
```

好的，现在我们已经解析了控制函数的依赖列表，在执行执行 `Controller` 之前。

```javascript
var Injector = {
  process: function(target) {
    // 实现
  }
};
Injector.process(WelcomeController);
```

有趣吧？我们现在解析了 `WelcomeController` 的依赖列表，在执行 `WelcomeController` 之前！假设 `WelcomeController` 有多个依赖项，这并不棘手，因为我们可以用逗号分割参数！

```javascript
var MultipleDependenciesController = function(Greeter, OtherDependency) {
  // MultipleDependenciesController 的实现
}
var args = MultipleDependenciesController
  .toString()
  .match(FN_ARGS)[1]
  .split(',');
console.log(args); // 返回 ['Greeter', 'OtherDependency']
```

剩余部分非常直观，我们只需要从依赖缓存中按名称获取请求的依赖，并将请求名称作为参数调用目标函数。让我们实现将依赖名称数组映射到依赖项的函数：

```javascript
Injector.dependencies = {};
Injector.register = function(name, dependency) {
  this.dependencies[name] = dependency;
};
```

```javascript
var RobotGreeter = {
  greet: function() {
    return 'Domo Arigato';
  }
};
Injector.register('Greeter', RobotGreeter);
```

## 前进

构建块已经就绪，现在到了关键部分。技巧是将这些字符串转换回函数。这正是我们在这里做的。

```javascript
var WelcomeController = function (Greeter) {
  Greeter.greet();
};
// 返回函数的字符串
var controllable = WelcomeController.toString();
```

## 依赖检查

是时候实现 `Injector` 的 `process` 方法了。首先让我们看看 `Angular` 的 `injector.js`。你会注意到反射从第 54 行开始，并利用了一些正则表达式来解析函数。让我们来看看正则表达式，好吗？

```javascript
var FN_ARGS = /^\s*function\s*\([^{]*\s*([^)]*)/m;
```

`FN_ARGS` 正则表达式用于选择函数括号内的所有内容。在我们的案例中，依赖列表。

```javascript
var args = WelcomeController.toString().match(FN_ARGS)[1];
console.log(args); // 返回 Greeter
```

很酷，对吧？我们现在已经在执行 `WelcomeController` 函数之前，在 `Injector` 中解析了 `WelcomeController` 的依赖列表！

## 要求 2：注册依赖项

```javascript
Injector.getDependencies = function(arr) {
  var self = this;
  return arr.map(function(dependencyName) {
    return self.dependencies[dependencyName];
  });
}
```

`getDependencies` 方法接收依赖项名称数组并将其映射为对应的实际依赖项数组。如果你对这个 `map` 函数不陌生，可以查阅 [Array.prototype.map 文档](https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Global_Objects/Array/map)。

现在我们已经实现了依赖项解析器，可以回到我们的 `process` 方法并使用正确的依赖项执行目标函数。

```javascript
target.apply(target, this.getDependencies(args));
```

非常酷炫，对吧？

## Injector.js

```javascript
var Injector = {
  dependencies: {},

  process: function(target) {
    var FN_ARGS = /^\s*function\s*\([^{]*\s*([^)]*)/m;
    var text = target.toString();
    var args = text.match(FN_ARGS)[1].split(',');

    target.apply(target, this.getDependencies(args));
  },

  getDependencies: function(arr) {
    var self = this;
    return arr.map(function(value) {
      return self.dependencies[value];
    });
  },

  register: function(name, dependency) {
    this.dependencies[name] = dependency;
  }
};
```

## 模式与代码组织

## 示例与借口

你可以在 jsFiddle 上看到我们在示例中创建的运行中的注入器：http://jsfiddle.net/mMKoj/

这个刻意的示例并不是你在实际代码库中会使用的，它仅仅是为了演示 JavaScript 提供的丰富功能，并解释 `AngularJS` 如何提供依赖注入。如果你对此感兴趣，我强烈建议你进一步查看他们的代码。需要注意的是，这种方法并不新奇。其他项目也使用 `toString` 来预处理代码，例如 `Require.js` 使用了类似的方法来解析并将 `CommonJS` 风格的模块转换为 `AMD` 风格的模块。

希望这篇文章能让你受益匪浅，并继续探索依赖注入以及它在客户端世界中的应用。

我真的觉得这里正在酝酿某种特别的东西。

> http://requirejs.org/

## 工具

### 开发者必备的 10 个 JavaScript 工具

> ### 原文
> http://smashinghub.com/javascript-tools-for-developers.htm
> Ali Qayyum, smashinghub.com*
> *http://smashinghub.com/author/admin

对于 Web 开发，JavaScript 工具仍然是最困难的问题之一。许多工具和应用程序可以让你的开发工作变得非常快速和简单。几年前，人们只使用 JavaScript 添加一些闪烁文字等效果，但那时他们开始认真对待它，因为它可以增强网页。因此，这里为所有 JavaScript 开发者提供了 10 个棒的工具和脚本。

### FitText.js

### FitText

这个强大的工具可以根据父元素的大小对文本进行自动缩放。只需查看网站并调整浏览器大小：文本将自适应。现代网站和应用的非常好的工具！

http://fittextjs.com/

### MicroJS

> * http://fittextjs.com/

### Microjs

这是一个新网站，可以快速为你提供 JavaScript 代码段。它拥有几乎所有常见任务的 JavaScript 代码：`Ajax`、`Json`、`DOM` 和面向对象的 JavaScript 等。绝对是你收藏夹中的必备项！

http://microjs.com/

### Diva.js

这是一个让你查看文档的 JavaScript 前端。它设计用于与数字库配合，将多页文档显示为一个单一、不分割的项目。它被设计为配合 `IIPImage` 服务器工作，对于那些图书馆或书店网站的人来说，这将是一个很棒的工具。这里提供了一个演示，你可以查看。

http://ddmal.music.mcgill.ca/diva/

### 书签脚本生成器

> http://ddmal.music.mcgill.ca/diva/

## 工具

### 书签脚本

顾名思这是一个书签脚本生成器：你只需要粘贴你的普通 JavaScript 代码，按下按钮，就会得到一个准备好安装在浏览器栏上的书签脚本。

http://benalman.com/code/test/jquery-run-code-bookmarklet/

### jQAPI

> "http://benalman.com/code/test/jquery-run-code-bookmarklet/

## 工具

这是一个非常棒的网站，它以非常用户友好的方式提供文档，因此当你需要任何帮助时，它可以成为你的参考。

http://jquery.com/

### heatmap.js

`heatmap.js` 是一个 JavaScript 库，用于使用 `html5canvas` 元素在你的数据上生成热力图。热力图实例按顺序根据数据进行染色，如果你只添加单个数据集，它将在画布上显示。为了快速和高效，重新计算热力图是完全自定义的——欢迎选择你的颜色渐变、强度、透明度和半径。欢迎在 github 上提交贡献和反馈。如果你有任何问题或建议，请告诉我。如果你想了解 `heatmap.js` 如何工作，有一篇关于其内部机制的文章。

### 什么是热力图？

你从未听说过热力图？没问题！热力图是频率不同的数据的图形化表示，热力图上的黄色点频率很高，蓝色点频率较低。有关更详细的解释请查看维基百科

### 使用演示

- 基于静态数据的热力图
- 鼠标移动实时热力图
- 点击热力图
- Google Maps 层
- OpenLayers 层
- 实时流量热力图

### heatmap.js

JavaScript 提供了无限可能：例如，`heatmap.js` 允许使用 `html5canvas` 元素根据你的数据生成热力图。简单而高级！

http://www.patrick-wied.at/static/heatmapjs/

### Respond.js

这是一个微型脚本，让不支持它的浏览器（如 `IE`！）使用 `CSS3` 媒体查询

https://github.com/scottjehl/blob/master/respond.min.js

### Modernizr

这是一个让旧浏览器运行像新浏览器一样良好的脚本，因此你可以创建适用于 `IE67` 的现代应用程序。你的客户一定会喜欢它的。

http://www.modernizr.com/

### YepNope

正如名字暗示的，它回答“是”或“否”。例如，询问 `Modernizr` 是否已加载。如果是，询问 `YepNope` 执行这个；如果不是，询问 `YepNope` 执行那个。简单且有用！

http://yepnope.com/

### Ligature.js

名如其义。`Ligature.js` 是一个为任何类型的文本添加神奇连字的脚本。对于我们大多数排版爱好者来说。

http://code.google.com/p/ligature-js/

## Node.js

模型。这意味着非常简单：它是一个为了编写可扩展、高性能网络应用程序而设计的环境。它类似于 Ruby 的 `Event Machine` 或 Python 的 `Twisted`，但它将事件模型更进了一步——它将事件视为一种语言，而不是一个库。

而且不仅于此：`Node.js` 真正伟大之处在于有适用于任何用途的成千上万可用模块，以及该项目背后活跃的社区。在本次汇总中，你将找到 `Node.js` 最实用的资源，从好手的工具到详细的教程，更不用说关于这项广前景技术的深度文章和资源了。你在使用 `Node.js` 吗？请在本文的评论区告诉我们！

## 有用的 Node.js 工具

### Express Boilerplate¹⁰⁷

`Express Boilerplate` 为开发者提供了一个干净的起点，同时打包了足够有用的功能，以消除所有可能在项目启动之前使其偏离轨道的冗任务。

### Socket.IO¹⁰⁸

`Socket.IO` 是一个跨浏览器 Web 服务器，旨在让每个浏览器和移动设备都能运行实时应用，模糊了各种传输机制之间的区别。它是 JavaScript 实现的无忧实时体验。

### Mastering Node¹⁰⁹

通过 `Mastering Node`，你可以编写高并发服务器，使用 `CommonJS` 模块系统、`Node.js` 核心库、第三方模块、高级 Web 开发等。

### Log.io¹¹⁰

你的基础设施可能包含散落在几十台机器上的数百个日志文件。为了帮助你监控部署和排除故障，`Log.io` 让你能够在用户界面中立即组合日志流。

### Formaline¹¹¹

`Formaline` 是一个低级、全功能的 `Node.js` 模块，用于处理表单请求（`HTTP POST` 和 `PUT`）并快速解析上传的文件。它也可以直接用于，例如像 `Connect` 这样的中间件软件。

### LDAPjs¹¹²

`LDAPjs` 是一个纯 JavaScript 框架，用于在 `Node.js` 中实现 `LDAP` 客户端和服务器。它针对在 `Node.js` 和 `Express` 中与 `HTTP` 服务交互的开发者。

### Node Supervisor¹¹³

这是一个 `Node.js` 的小型守护进程。它运行你的程序并监控代码更改，你可以获得类似热重载的行为，而无需担心内存泄漏或必须清理所有模块间的引用，且不需要全新的系统。

### Stylus: 一种 Node.js 的表现性 CSS 标记语言¹¹⁴

`Stylus` 应该是一种可以转换为 `CSS` 的表现性语言。其编译器构建在 `Node.js` 中。

### Jade – 模板引擎¹¹⁵

`Jade` 是用于 `Node.js` 应用的模板引擎。它将强大的力和灵活性与简洁整洁的语法结合在一起。

### Express¹¹⁶

这是一个受 `Sinatra` 启发的 `Node.js` Web 开发框架：快速、灵活性感。

### Hook.io¹¹⁷

`hook.io` 创建了一个分布式的 `Node.js` `EventEmitter`，它可以跨进程/跨平台/跨浏览器工作。把它想象成在任何支持 JavaScript 的地方运行的实时事件总线。

### Node Package Manager¹¹⁸

`NPM` 是 `Node` 的包管理器。你可以用它安装和发布你的 `node` 程序。它管理依赖关系并执行其他成本工作。

### Node-QRCode¹¹⁹

作为一个非常新的 `Node`，`Node.js` 已经拥有每种可能应用大量的库。这是一个 `QR` 码生成器。

### NWM¹²⁰

`NWM` 是一个在 `NodeKO 2011` 上编写的 `X` 动态管理器。它使用 `libev` 与 `X11` 接口，允许你在 `Node.js` 中布局窗口。

### Bricks.js¹²²

`Bricks` 是构建在 `Node.js` 上的高级模块化框架。它非常灵活。`Bricks` 可以作为独立的静态 Web 服务器、基础路由框架或多级类似 `Apache` 的路由系统；它的模块化程度足以具有完全更换其路由引擎的能力。

### Node.js Modules¹²³

一个按类别划分的几乎所有 `Node.js` 最著名的模块的列表。这个列表绝对值得一看。

### 90 个开源 Node.js 模块¹¹²³

最近，`Browserling` 向开源社区发布了 90 个 `Node.js` 模块。其中一些是一些小而奇特的模块，另一些可能对你的下一个 `Node.js` 项目非常有用。

### Calipso¹¹²⁴

`Calipso` 是一个基于 `NodeJS` 服务器的内容管理系统 (`CMS`)。

### PDFKit¹¹²⁵

`PDFKit` 是一个 PDF 文档生成库。

### Forever¹²⁶

一个简单的工具确保 `Node.js` 进程持续运行。

### 介绍 Node.js?

在本次演示中，`Node.js` 背后的男人 `Ryan Dahl` 将向你介绍这个事件驱动的 `I/O` 框架，并给出几个示例。

### 介绍-0: 服务端 JavaScript

`Node.js` 引发了对服务端的新热潮。在本节中，你将学习如何利用 `Connect` 和 `Express` 中间件来提高效率。

### 技术文章 HTTP 和 Webockets 在 Node.js

本指南面向初学者和熟悉反向代理 `HTTP` 的人员。

- ¹⁰⁷ https://github.com/mape/node-express-boilerplate
- ¹⁰⁸ http://socket.io/
- ¹⁰⁹ https://visionmedia.github.com/masteringnode/
- ¹¹⁰ http://logio.org/
- ¹¹¹ https://github.com/rootslab/formaline
- ¹¹² http://ldapjs.org/
- ¹¹³ https://github.com/isaacs/node-supervisor
- ¹¹⁴ https://learnboost.github.com/stylus/
- ¹¹⁵ https://jade-lang.com/
- ¹¹⁶ https://express.com/
- ¹¹⁷ https://github.com/hookio/hook.io
- ¹¹⁸ https://npmjs.org/
- ¹¹⁹ https://github.com/solidait/node-qrcode
- ¹²⁰ https://github.com/mixu/nwm
- ¹²¹ https://bricksjs.com/index.html
- ¹²² https://github.com/joyent/node/wiki/modules#templating
- ¹²³ http://radar.oreilly.com/2011/08/node-javascript.html
- ¹²⁴ http://calipso.org/
- ¹²⁵ https://pdfkit.org/
- ¹²⁶ http://forever.js/
- ¹²⁷ http://browserling.com/
- ¹²⁸ http://sencha.com/
- ¹¹⁹ http://stackoverflow.com/
- ¹³⁰ http://vimeo.com/18077379/

## 工具

`Web socket` 代理、负载均衡、虚拟主机配置、请求转发以及其他 Web 代理概念。

## 健性的 Node.js 代码¹¹³

“正在我开始对代码进行重构/重写的时候”

## 如何编写原生 Node.js 扩展¹⁴⁰

在教程中，你将学习如何以正确的方式编写原生 `Node.js`，从最基础的知识到为 `NPM` 打包扩展。

## 让我们制作一个 Web 应用：Nodepad¹⁴¹

本系列将引导你使用 `Node.js` 构建 Web 应用，涵盖了你在构建应用程序时会遇到的所有主要领域。

## 使用 Web Sockets、Node.JS 和 Socket.io 进行 HTML5 Canvas 绘制¹⁴²

`Web sockets` 和 `canvas` 是目前浏览器中正在实现的两个酷炫功能。本教程将为你快速介绍它们的工作原理，你将创建一个由 `Node.js` 和 `Web Sockets` 驱动的实时 `canvas` 绘画。

## 使用 Node.js 开发多人互动 HTML5 游戏¹⁴³

受 `iOS` 游戏 `Osmos` 的启发，开发者 `Boris Smus` 使用 `HTML5 canvas` 和 `Node.js` 制作了该游戏的替代版本。这篇文章解释了项目的主要部分。

## 在 Amazon EC2 上部署 Node.js¹⁴⁴

`Amazon` 的 `EC2` 是云应用的流行选择。本教程展示了如何将 `Node.js` 部署在 `EC2` 实例上。

## 一个简单的 Node.js + CouchDB 日历¹⁴⁵

在 `Chris Storm` 的这个教程中，你将学习如何使用 `Node.js` 和 `CouchDB` 构建 Web 日历。

## IIS7¹⁴⁶

`IISnode` 提供了一个原生 `IIS 7.x` 模块，允许在 `IIS` 上运行 `Node.js` 应用。该项目使用了 `node.exe` 的 `Windows` 绑定，该绑定近期有了重大改进。

## Node.js + 手机控制浏览器游戏¹⁴⁷

有人想过，一个简单的手机（特别是利用其陀螺仪和加速度计）能多容易地作为大屏幕多人游戏的控制器。通过少量的 `Node.js` 和 `HTML5`，事实证明这非常简单。

- ¹³⁹ https://laurenzo.org/2011-03/bulletproof-node-js-coding/
- ¹⁴⁰ https://ysikal.com/how-to-write-your-own-native-nodejs-extension
- ¹⁴¹ https://daily.com/2010/11/01/node-tutorial/
- ¹⁴² https://webos.com/html5-canvas-websockets-nodejs/
- ¹⁴³ https://smus.com/multiplayer-html5-games-with-node
- ¹⁴⁴ https://blog.carbotite.com/2011/09/01/deploying-node-js-on-amazon-ec2/
- ¹⁴⁵ https://japur.blogpost.com/2011/09/08/simple-nodejs-couchdb-calendar.html
- ¹⁴⁶ https://tomasi.janczik.com/2011/09/08-hosting-nodejs-in-iis-on.html
- ¹⁴⁷ https://cycloid.com/blog/2011-08-using-nodejs-and-your-phone-to-control-a-browser-game

## Node.js 有模板引擎吗？¹⁴⁸

`StackOverflow` 上出现了一场关于 `Node.js` 可用模板的引人入胜的讨论。这场讨论产生了非常有用的论点。

## Node.js 博客、播客、资源

### How to Node¹⁴⁹

`How to Node` 是由 `Tim Caswell` 创建的社区支持博客。其目的是教授如何执行 `Node.js` 中的各种任务，以及编写高效代码所需的基础概念。

### Nodejs¹⁵⁰

一个关于在云端扩展 `Node.js` 应用以及通用 `Node.js` 事件的非常有趣的博客。

### Node Up¹⁵¹

一个回顾 `Node.js` 的播客，解释了它的哲学并涵盖了许多流行的库。

### Node Tuts¹⁵²

免费视频教程。

### Minute With Node.js¹⁵³

`Node.js` 随着每个版本的更新不断变化和成长。新的库和框架出现允许你为以前无法实现的兴奋项目编写 JavaScript。这是整个 `Node.js` 生态系统的更新一站，侧重于硬核技术。

### Felix 的 Node.js 指南¹⁵⁴

在过去的几个月里，`Felix` 做了很多演讲，因此他利用最近的假期编写了这份帮助人们入门 `Node.js` 的非官方指南。

### Node.js Knockout¹⁵⁵

`Node.js Knockout` 是一个为期 48 小时的 `Node.js` 黑客松。这是一场全球参赛者的在线竞赛。

## 参考文献与书籍

### Node.JS Help Sheet¹⁵⁶

“`Node.js` 是一个用于 `V8 JavaScript` 引擎的框架。它非常适合编写可扩展的”

```json
{
  "globals": {
    "console": false,
    "jQuery": false,
    "_": false
  },
  "maxparams": 5,
  "maxdepth": 5,
  "maxstatements": 25,
  "maxcomplexity": 10,
  "es5": true,
  "browser": true,
  "boss": false,
  "curly": false,
  "debug": false,
  "devel": false,
  "eqeqeq": true,
  "evil": true,
  "forin": false,
  "immed": true,
  "laxbreak": false,
  "newcap": true,
  "noarg": true,
  "noempty": false,
  "nonew": false,
  "nomen": false,
  "onevar": true,
  "plusplus": false,
  "regex": false,
  "undef": true,
  "sub": true,
  "strict": false,
  "white": true,
  "unused": true
}
```

## 使用 requestAnimationFrame 实现更精简、更高效、更快速动画

原文

http://www.html5rocks.com/en/tutorials/speed/animations

Paul Lewis, html5rocks.com*

^*http://www.html5rocks.com

可以肯定，作为开发者，你在职业期间会做一些动画工作，无论是较小的 `UI` 效果还是大型的交互画布作品。你可能也遇到过 `requestAnimationFrame`，或者 `rAF`（如果我们在这一带称之为 `raaf` 的话），希望你有机会在项目中使用它。如果你不知道，`requestAnimationFrame` 是浏览器处理动画的原生方式。因为 `rAF` 专门为处理动画和渲染设计，浏览器可以在最合适的时间调度它，如果我们的操作得当，它将帮助我们实现丝滑的每秒 60 帧。

我们在本文中要做的是概述一些额外的方法，以确保你从动画代码中获得最大收益。即使你使用了 `requestAnimationFrame`，其他方法仍然导致你的动画出现瓶颈。在每秒 60 帧的情况下，你绘制的每一帧都有 16.67 毫秒来完成所有操作。时间并不充足，所以每一次优化都至关重要！

**TLDR**: 将你的事件与动画解耦；避免导致重流-重绘（`reflow-paint`）循环的动画；你的 `rAF` 调用预期第一个参数为高分辨率时间戳；只有在需要进行视觉更新时才使用 `rAF`。

## 防抖滚动事件

防抖（`Debouncing`）是将动画与任何影响它的输入解耦的过程。例如，当滚动页面时触发的效果。该效果可能会检查某些 `DOM` 元素对用户是否可见，然后给这些元素应用 `CSS` 类。

或者你可能正在编写视差滚动效果，随着你的滚动，背景图像相对于页面滚动位置发生变化。我将采用两种常见用途中的前者，你的代码核心可能是：

```javascript
function onScroll() {
    update();
}
function update() {
    // 假设 domElements 已经声明
    // 到这里：
    for(var i = 0; i < domElements.length; i++) {
        // 读取 DOM 元素的偏移
        // 以确定可见性 - 触发重流 (reflow)
        // 然后为可见项目应用一些 CSS 类
        // 触发重绘 (repaint)
    }
}

window.addEventListener('scroll', onScroll, false);
```

主要问题是，每当我们收到滚动事件时都会触发重流和重绘：我们要求浏览器重新计算 `DOM` 元素的真实位置（这是一个昂贵的重流操作），然后我们应用一些 `CSS` 类，这导致浏览器重绘。我们最终在重流和重绘之间反复“乒乓”，这会损害你的应用程序性能。我们针对的是滚动事件，但同样适用于大小调整（`resize`）事件。事实上，任何你以这种方式使用的事件都可能导致性能问题。阅读 `Tony Gencifer` 的 `Fastas` 博客可以了解在 `WebKit`¹⁵⁹ 中导致重流的属性。

> 159 http://gent.ilcore.com/2011/03/how-not-to-trigger-layout-in-webkit.html

我们需要做的是将滚动事件与更新函数解耦，这正是 `requestAnimationFrame` 帮助的地方。

```javascript
var latestKnownScrollY = 0;
function onScroll() {
  latestKnownScrollY = window.scrollY;
}
```

我们现在处于更好的境地了：`onScroll` 在浏览器选择执行它时运行，但我们所做的只是存储窗口的滚动位置。在我们尝试在动画中使用该值之前，这段代码可能会运行一次、二十次或一百次，这并不重要。关键点在于我们正在跟踪该值，但它没有触发潜在的额外调用。如果你的绘制调用（`draw call`）是昂贵的，那么避免这些额外调用将让你受益匪浅。

此更改的另一部分是使用 `requestAnimationFrame` 在浏览器最方便的时间处理视觉更新：

```javascript
function update() {
  requestAnimationFrame(function() {
    // 在此处使用 latestKnownScrollY
  });
}
```

## 防抖鼠标事件

我们已经过了一个使用 `rAF` 将动画与滚动和大小调整事件解耦的常见用例，现在让我们聊另一个：使用它来处理交互。在这种情况下，我们要在按下鼠标键时让某个物体固定在当前位置。当释放鼠标时，我们将停止动画。

让我们直接看代码，然后进行拆解：

```javascript
var mouseDown = false;
lastMousePosition = { x: 0, y: 0 };

function onMouseDown() {
  mouseDown = true;
  requestAnimationFrame(update);
}

function onMouseUp() {
  mouseDown = false;
}

function onMouseMove(evt) {
  lastMousePosition.x = evt.clientX;
  lastMousePosition.y = evt.clientY;
}

function update() {
  if(mouseDown) {
    requestAnimationFrame(update);
  }
}

document.addEventListener('mousedown', onMouseDown, false);
document.addEventListener('mouseup', onMouseUp, false);
document.addEventListener('mousemove', onMouseMove, false);
```

## 测试

在 `update` 函数中。最后需要注意的是，`update` 会请求下一个帧，直到我们调用了 `mouseUp` 并且 `mouseIsDown` 被设回 `false`。

在这里我们的策略仍然是让鼠标事件以浏览器认为所需的频率执行，而让绘制调用（`draw calls`）独立于这些事件发生。这与我们处理滚动事件（`scroll events`）的方式相似。

如果情况复杂一些，你正在动画的对象在调用 `mouseUp` 后仍在移动，你需要管理对 `requestAnimationFrame` 的调用。一个合适的解决方案是跟踪动画对象的位置，当两帧之间的变化低于某个阈值时，你应该调用 `requestAnimationFrame`。代码的更改将如下：

```javascript
var mouseIsDown = false;
lastMousePosition = { x: 0, y: 0 };
rafIndex = 0;

function onMouseDown() {
  mouseIsDown = true;

  // 取消现有的 rAF
  cancelAnimationFrame(rafIndex);

  rafIndex = requestAnimationFrame(update);
}

// 其他事件处理器如上所示

function update() {
  var objectHasMovedEnough = calculateObjectMovement();

  if(objectHasMovedEnough) {
    rafIndex = requestAnimationFrame(update);
  }
  // 现在在 lastMousePosition 绘制对象
}

function calculateObjectMovement() {
  var hasMovedFarEnough = true;

  // 这里我们可能会使用速度
  // 等等通过时间捕捉对象的移动
  // 并设置 hasMovedFarEnough
  return hasMovedFarEnough;
}
```

这种基于时间的方法中的主要变化在于，如果你松开鼠标，`rAF` 调用会持续，直到对象停止运动，但你可能会开始点击并拖拽，这意味着你会获得原始调用的同时，还会获得第二个 `rAF` 调用。这并不好。为了解决这个问题，请确保在设置新调用之前（在 `mouseDown` 中）取消任何已计划的 `requestAnimationFrame` 调用。

## requestAnimationFrame 和高分辨率时间戳

在我们花些时间讨论 `requestAnimationFrame` 的时候，值得注意的是 `Canary` 中处理回调的方式的一个最近变化。从现在起，传递给回调函数的参数将是一个高分辨率时间戳，精确到毫秒分之一。关于此有两点：

- 如果你的动画是基于时间的，这简直太棒了，因为现在你可以非常精确
- 你需要更新今天现有的任何期望对象或元素作为第一个参数的代码

获取关于此的完整介绍：[requestAnimationFrame API: now with sub-millisecond precision¹⁶¹](http://updates.html5rocks.com/2012/05/requestAnimationFrame-API-now-with-sub-millisecond-precision)

## 示例

好了，让我们用一个示例来结束，这样你就能看到它的实际运行了。这有点刻意，我们还会加入一个额外的性能杀手，我们可以在执行过程中修复它。太有趣了！

我们有一个包含 800 个 `DOM` 元素的文档，当你滚动鼠标时我们将移动它们。因为我们精通现代开发，从一开始我们就将使用 `CSS` 过渡和 `requestAnimationFrame`。当我们向下滚动页面时，我们将确定 800 个 `DOM` 元素中哪些现在屏幕可见区域的中间上方，并通过添加 `left` 类将它们向左侧移动。

值得记住，我们选择如此大量的元素是因为这将让你更容易发现任何性能问题。而这些问题确实存在。

以下是我们的 JavaScript 看起来像的样子：

> ¹⁶¹http://updates.html5rocks.com/2012/05/requestAnimationFrame-API-now-with-sub-millisecond-precision

```javascript
var movers = document.querySelectorAll('.mover');
/**
 * 设置一切并定位所有 DOM 元素
 * - 通常由 CSS 完成，但嘿，它们有很多
 * 所以我们在这里做！
 */
(function init() {
  for(var m = 0; m < movers.length; m++) {
    movers[m].style.top = (m * 10) + 'px';
  }
}());

/**
 * 我们的动画循环 - 由 rAF 回调
 */
function update() {
  // 获取最新的滚动位置
  var scrollY = window.scrollY;
  mover = null;
  moverTop = [];
  halfwindowHeight = window.innerHeight * 0.5;
  offset = 0;

  // 现在遍历每个 mover div
  // 在执行过程中更改它的类
  for(var m = 0; m < movers.length; m++) {
    mover = movers[m];
    moverTop[m] = mover.offsetTop;

    if(scrollY > moverTop[m] - halfwindowHeight){
      mover.className = 'mover left';
    } else {
      mover.className = 'mover';
    }
  }
  requestAnimationFrame(update);
}

// 调度启动
window.addEventListener('load', update, false);
```

我们的示例页面性能和 `rAF` 优化

如果你查看优化前的页面¹⁶，你会看到它在滚动时确实非常吃力，原因有很多。（注：此处原始文本包含大量重复和错误片段，已按要求提取核心逻辑）

# Node.js

# 理解事件循环并为 Node.js 编写优秀代码

原文

http://developer.yahoo.com/blogs/ydn/part-1-understanding-event-loops-writing-great-code-11401.html

Tom Hughes-Croucher, developer.yahoo.com/blogs#

http://developer.yahoo.com/blogs

一如既常，`JSConf.Eu`¹⁶⁴ 是我今年参加过的最棒的会议之一。与地球上最聪明的 `JavaScript` 编码员聚在一起是一种乐幸，而且在柏林这个非常时尚的城市举行这次活动更是一个额外的奖赏。关于 `JSConf`¹⁶⁵，已经有很多非常精彩的总结，所以我不再重点关注它；我将准备扩展我之前所做的演讲。

在事件循环内部进行编程是大多数程序员仅略有了解的事情。`Node.js` 正在迅速成为一种非常流行的、基于事件循环的 `JavaScript` 服务器。它的简单易用在于，人们可以在服务器上编写 `JavaScript`，并且可以访问 `HTTP` 栈、`TCP` 文件 `I/O` 和数据库。然而，我们在这种语境下编写的程序类型，往往与我们为浏览器应用程序或网站编写的程序类型非常不同。

在浏览器中，程序的大部分往往涉及设置用户界面，并且会执行一些小型的事件回调——最典型的是基于用户与浏览器的交互。例如，当用户点击表单上的“提交”时，我们拦截该点击并验证他们的提交。

这里有一个重要的点：在较多的浏览器编程中，程序员只处理由用户引起的事件，而用户一次能做的事情是的。此外，这些事件的回调往往是离散的，并且不考虑其他事件。某些库（如 `YUI`）支持自定义事件，但这通常被认为是一项高级功能。

## 在服务器上

¹⁶⁴http://jsconf.eu/2010/
¹⁶⁵http://palagut-coding.blogspot.com/2010/09/in-case-you-missed-it-jsconf-2010-day.html

活动应该是非阻塞的（原因我们稍后会解释）。这意味着所有的 `HTTP` 请求、数据库查询、文件 `I/O` 等在它们返回之前都不会停止执行。相反，它们独立运行，并在数据可用时发出一个事件。

这意味着在 `Node.js` 中编程有许多回调来处理各种 `I/O`，然后启动处理其他类型 `I/O` 的回调。这与浏览器编程非常不同。虽然仍然存在某种程度的线性设置，但大部分代码都是处理回调的。

### 事件驱动

由于这些不同的编程风格，我们需要寻找模式来帮助我们有效地在服务器上进行编程。关于事件循环，让我们更深入地看看它。

我认为大多数人直觉上就能理解事件驱动编程，因为它就像日常生活。想象一下你正在做饭。你正在切一个灯椒，这时一个锅开始烧开了。由于你正在切，所以你切完这一片，然后关炉子。在日常生活中，我们习惯了拥有某种内部回调来处理事件，但在 `JavaScript` 中，我们一次只做一件事。

是的，是的，我能看到你一边揉肚子一边拍头，但我们并不到。但是，如果你尝试同时做任何严肃的活动，进展就会非常缓慢。这就像 `JavaScript`。它是通过让事件驱动动作，但它是“单线程”的，所以一次只发生一件事。

思考这种事件循环的另一种方式是**邮局（或邮件）**。当我们的事件循环邮递员收到一封信时，就是一个事件。他有一堆需要按顺序递送的事件。对于邮递员收到的每封信（事件），他都会沿着路线去交付。路线就是分配给该信的回调函数（有时是多个）。然而，关键的一点是，我们的邮递员只有一组事件，他一次只能走一条代码路径。

有时，当邮递员在路线上行走时，有人会给他另一封信。这是因为他代码的回调函数发出了一个事件。在这种情况下，邮递员会立即递送新消息（在所有直接给他的之后，而不是通过邮局，所以它是紧急的）。邮递员将偏离当前的代码路径，走代码路径来递送新事件。然后他继续执行那个触发他所走路径的原始事件。

让我们来看另一个例子。让邮递员递送一封需要打开门的信。他到达了大门，发现门是关着的，于是他等待并再次尝试，一次又一次。他被困在了等待门打开的无限循环中。但如果栈中有一封信会要求某人开门以便邮递员通过，那么这一定能解决问题，对吧？

遗憾的是，并不会。邮递员永远不会递送那封信，因为他陷入了无止境的等待等待。这是因为打开门的事件是当前事件回调的外部的。如果我们从回调内部发出事件，我们已经知道邮递员会在继续执行之前去递送那封信。然而，当事件外部于当前执行的代码段时，在这些代码段被完全评估到结论之前，它们不会被调用。

# Node.js 100

我们可以利用此来编写一段代码，创建一个 `Node.js`（或浏览器）永远无法跳出的循环：

```javascript
EE = require('events').EventEmitter
ee = new EE();

die = false;

ee.on('die', function() {
  die = true;
});

setTimeout(function() {
  ee.emit('die');
}, 100);

while(die) {
}
```

### 原文

> http://callbackhell.com

Max Ogden, github.com/maxogden*

*https://github.com/maxogden

## 什么是“回调地狱”？

异步 `JavaScript`，或者说使用回调的 `JavaScript`，很难在直觉上写好。很多代码最后看起来都像这样：

```javascript
fs.readdir(source, function(err, files) {
  if (err) {
    console.log('Error finding files: ' + err)
  } else {
    files.forEach(function(filename, fileIndex) {
      console.log(filename)
      gm(source + filename).size(function(err, values) {
        if (err) {
          console.log('Error identifying file size: ' + err)
        } else {
          console.log(filename + ' : ' + values)
          aspect = (values.width / values.height)
          widths.forEach(function(width, widthIndex) {
            height = Math.round(width / aspect)
            console.log('resizing ' + filename + ' to ' + height + 'x' + height)
            this.resize(width, height).write(destination + '_w' + width + '_' + height + '.jpg')
          })
        }
      })
    });
    if (err) console.log('Error writing file: ' + err)
  }
}.bind(this))
```

看到所有的 `function` 和 `}}` 了？额！这被亲切地称为回调地狱。

写更好的代码并不难！你需要了解以下几点：

## 给你的函数命名

这里有一段（混乱的）浏览器 `JavaScript`，它使用 `browser-request`¹⁶⁶ 向服务器发送 `AJAX` 请求：

```javascript
var form = document.querySelector('form')
form.onsubmit = function(submitEvent) {
  var name = document.querySelector('input').value
  request({
    uri: "http://example.com/upload",
    body: name,
    method: "POST",
  }, function(err, response, body) {
    var statusMessage = document.querySelector('.status')
    if (err) return statusMessage.value = err
    statusMessage.value = body
  })
}
```

这段代码有两个匿名函数。让我们给它们命名！

```javascript
var form = document.querySelector('form')
form.onsubmit = function formSubmit(submitEvent) {
  var name = document.querySelector('input').value
  request({
    uri: "http://example.com/upload",
    body: name,
    method: "POST",
  }, function(err, response, body) {
    var statusMessage = document.querySelector('.status')
    if (err) return statusMessage.value = err
    statusMessage.value = body
  })
}
```

如你所见，命名函数超级简单，并且能给你的代码带来一些好变化：

- 让代码易于阅读



- 当发生异常时，你将获得引用了实际函数名的堆栈跟踪，而不是“匿名”
- 允许你保持代码扁平，或者不要深层嵌套，这引出了我的下一点：

> ¹⁶⁶https://github.com/iriscouch/browser-request

## 保持代码扁平

在上一个例子的基础上，让我们更进一步，消除代码中发生的三层嵌套：

```javascript
function onSubmit(submitEvent) {
  var name = document.querySelector('input').value
  request({
    uri: "http://example.com/upload",
    body: name,
    method: "POST"
  }, postResponse)
}

function postResponse(err, response, body) {
  var statusMessage = document.querySelector('.status')
  if (err) return statusMessage.value = err
  statusMessage.value = body
}

document.querySelector('form').onsubmit = formSubmit
```

这样的代码看起来不那么可怕，而且更容易编辑、重构和黑客。

## 模块化！

这是最重要的一部分：任何人都能创建模块（即库）。引用 Isaac Schluter¹⁶（node.js 项目）：“编写只做一件事的小模块”。

让我们采取模板代码，通过将其拆分成几个文件转换为模块。由于我在浏览器和服务器上都写 JavaScript，我将展示一种在两处运行但仍然良好且简单的方法。

这是一个新的 `uploader.js` 文件，包含了之前的两个函数：

> ¹⁶http://twitter.com/izs

# Node.js

```javascript
function submit(submitEvent) {
  var name = document.querySelector('input').value
  request({
    uri: "http://example.com/upload",
    body: name,
    method: "POST"
  }, postResponse);
}

function postResponse(err, response, body) {
  var statusMessage = document.querySelector('.status')
  if (err) return statusMessage.value = err
  statusMessage.value = body
}

exports.submit = formSubmit
```

结尾的 `exports` 是 CommonJS 系统的示例，Node.js 用于服务器端编程。我喜欢这种模块样式，因为它非常简单——你只需要定义应该共享的内容（这就是 `exports` 的作用）。

要在浏览器中使用 CommonJS 模块，你可以使用像 browserify⁰ 这样的命令行工具。我不会涉及细节如何使用，但它会将模块加载到你的程序中。现在我们有了 `loader.js`（它是通过脚本标签加载的），我们只需要引入并使用它！这里是我们的应用：

```javascript
var loader = require('loader')
document.querySelector('form').onsubmit = loader.submit
```

现在我们的应用程序只有两行代码，并且具有以下优点：

- 更容易让开发者理解——他们不会被阅读所有代码所困
- loader 可以在其他地方使用而无需重复代码，并在服务器上轻松共享
- 代码本身很好且易于阅读

Web有很多模式，其中有些变得复杂。这里展示的我认为是最容易理解的。

> ¹⁰https://github.com/substack/browserify
> ¹¹http://www.adequatelygood.com/2010/3/JavaScript-Pattern-In-Depth
> ²http://nodejs.org/api/modules.html

## 我还是不懂

尝试阅读我的关于回调的介绍。

## Promise 怎么样？

Promise 是处理异步代码的更抽象的模式。本文目的是目的是编写原生 JavaScript。如果你使用了为 JS 添加抽象的第三方库，你就愿意让你贡献库的人有相同的观点。在我的经验中，我写的 90% 异步代码使用回调，当事情变得棘手时我会引入类似的东西。尽管如此，每个人都会开发出独特的风格，你应该像这样：有些人只用回调，有些人则不然。

请通过在 GitHub 上 fork 此项目来贡献新章节或修复现有章节！

## 理解 Express

> 原文
> http://evanhahn.com/understanding-express/
> Evan Hahn, evanhahn.com

这针对熟悉 Node.js 的人。他们知道如何运行脚本和使用 npm 安装包。不过你不必成为专家——Promise。本指南最后更新是针对 Express 3.2。它是一份介绍，主要处理概念。Express 比我描述得更好：“一个极简且灵活的 node.js 应用程序框架”。它帮助你构建 Web 应用。如果你在 Ruby 世界中使用过 Sinatra，这里的很多内容你会很熟悉。

与抽象不同，Express 隐藏了困难的部分并说“别担心，你不需要理解这部分”。它为你做了你不需要自己做的事。在另一个世界里，它是魔法。它是良性的魔法，Express 列出了一些使用它的人，其中有一些大名字：MySpace、Klout，甚至还有一些我制作的。这是一件了不起。我有一个博客。

但所有魔法都是代价的；你可能不理解 Express 的内部运作。这就像开车；我开车时并没有对其原理的详尽了解，但如果了解了会更好。如果东西坏了怎么办？如果你想从汽车中榨出所有性能怎么办？如果你对知识有永无的渴求怎么办？

所以让我们从底层开始通过 Node 理解 Express。

## 底层：Node 的 HTTP 服务器

Node 有 HTTP 模块，它为创建 Web 服务器提供了一个非常简单的抽象。它可能像这样：

```javascript
// 引入我们需要的
var http = require("http");

// 构建服务器
var app = http.createServer(function(request, response) {
  response.writeHead(200, {
    "Content-Type": "text/plain"
  });
  response.end("Hello world!\n");
});

// 启动服务器，宝贝
app.listen(1337, "localhost");
console.log("Server running at http://localhost:1337/");
```

如果你运行该应用（如果该文件是 app.js，你就运行 app.js），如果你在浏览器中访问 localhost:1337，你将得到“Hello world!”的响应。无论你做什么，都会得到相同的响应。你可以尝试访问 localhost:1337/anime_currency 或 localhost:1337/?onlyfriend=anime，这就像是在对着墙说话：“Hello world”

## Node.js

让我们简单拆解一下。

前几行使用 `require` 函数加载了一个名为 `http` 的 Node 内置模块。它将这个很棒的模块存放在一个名为 `http` 的变量中。关于 `require` 函数的更多信息，请查阅 Node.js 的文档¹⁸³。

然后我们使用 `http.createServer` 将服务器放入名为 `app` 的变量中。它接收一个监听请求的函数。我们稍后会回到这里，因为它们**非常重要**。接下来的两句先跳过它们。

我们做的最后一件事是告诉服务器监听来自端口 1337 的请求，然后我们只需将其打印出来。做到这一点，我们就可以开始工作了。

好了，回到请求处理函数。那个东西很重要。

## 请求处理器

在开始介绍这一节之前，我想说，这里有很多很酷的 HTTP 内容，我认为它们与学习 Express 并不直接相关。如果你感兴趣，可以查看 `HTTP` 模块的文档¹⁸⁴，因为里面有很多东西。

每当我们向服务器发送请求时，请求处理函数就会被调用。如果你不信，试着在那里放一个 `console.log`。你会在每次加载页面时都看到它。`request` 是来自客户端的请求。在应用中，你会看到它缩写为 `req`。让我们来看看它。为了这样做，我们将修改上面的请求处理器：

```javascript
var app = http.createServer(function(request, response) {
  // 构建答案
  var answer = "";
  answer += "Request URL: " + request.url + "\n";
  answer += "Request type: " + request.method + "\n";
  answer += "Request headers: " + JSON.stringify(request.headers) + "\n";

  // 发送答案
  response.writeHead(200, { "Content-Type": "text/plain" });
  response.end(answer);
});
```

重启服务器并刷新 `localhost:1337`。你会看到你请求的是什么 URL，这是一个 `GET` 请求，以及你发送了一些酷的请求头，如 `user-agent` 和更复杂的头部。

> ¹⁸³http://docs.nodejs.com/getting-started/what-is-require
> ¹⁸⁴http://nodejs.org/api/http.html

## Node.js

HTTP 内容！如果你访问 `localhost:1337/what_is_anime`，你会看到请求 URL 发生了变化。如果你用不同的浏览器访问，`user-agent` 就会改变。如果你发送一个 `POST` 请求，你会看到方法发生了变化。

响应是部分。就像之前的参数通常被缩写一样，这通常被缩写为三个字母的 `res`。对于每个响应，你会得到一个准备好发送的响应，然后执行 `response.end`。最终，你必须调用这个方法；Node 文档是这么说的¹⁸⁵。该方法执行实际的数据发送。你可以尝试创建一个调用它的服务器，它会永远挂起。

在发送之前，你可能想写一些头部。在我们的示例中，我们这样做：

```javascript
response.writeHead(200, { "Content-Type": "text/plain" });
```

这做了两件事。首先，它发送了 HTTP 状态码¹⁸⁶ 200，这意味着一切正常。然后，它发送了一些响应头部。在这种情况下，我们返回的是纯文本 `content-type`。我们可以发送其他内容，如 JSON 或 HTML。

## 我渴求更多

想要更多？好吧。你要求得很客气。

可以想象这些 API 并它们变成某些酷东西。你可以做（某种）这样的操作：

```javascript
var http = require("http");
http.createServer(function(req, res) {

  // 首页
  if (req.url == "/") {
    res.writeHead(200, { "Content-Type": "text/html" });
    res.end("Welcome to the homepage!");
  }

  // 关于页面
  else if (req.url == "about") {
    res.writeHead(200, { "Content-Type": "text/html" });
    res.end("Welcome to the about page!");
  }
});
```

> ¹⁸⁵nodejs.org/api/http.html#http_response_end_data_encoding
> ¹⁸⁶https://en.wikipedia.org/wiki/List_of_HTTP_status_codes

## Node.js

```javascript
// 404 错误！
else {
  res.writeHead(404, { "Content-Type": "text/plain" });
  res.send("404 error! File not found.");
}
}).listen(1337, "localhost");
```

你可以清理这些并让它们变漂亮，或者你可以像 npm.org 的那些人¹⁸⁷一样硬核，直接用原生 Node 硬到底。但你也可以构建一个框架。这就是 Sencha 所做的。而你为此了命名。

## 中间层：Connect

那个 Connect¹¹⁸ 正好是这个 JavaScript 蛋糕的中间层，因为它称自己为“用于 node 的中间件框架”。先不要去搜“中间件（middleware）”，我就要解释它了。

## 一些 Connect 代码

假设我们要写上面那个“你好世界”应用，但这次用 Connect。别忘了。

```javascript
var http = require("http");
var connect = require("connect");
var app = http.createServer(function(req, res) {

  // 首页
  if (req.url == "/") {
    res.writeHead(200, { "Content-Type": "text/html" });
    res.end("Welcome to the homepage!");
  }

  // 关于页面
  else if (req.url == "about") {
    res.writeHead(200, { "Content-Type": "text/html" });
    res.end("Welcome to the about page!");
  }
  else {
    res.writeHead(404, { "Content-Type": "text/plain" });
    res.end("404 error! File not found.");
  }
});

app.listen(1337, "localhost");
```

> ¹⁸⁷https://www.npmjs.org
> ¹¹⁸https://github.com/senchalabs/connect

# Node.js

访问 localhost:1337，你将看到一些日志！

# 我渴望更多

人们可以想象一起构思一些中间件来构建一个应用程序。也许你会这样做：

```javascript
var connect = require("connect");
var http = require("http");
var app = connect();

app.use(connect.logger());

// 首页
app.use(function(request, response, next) {
  if (request.url == "/") {
    response.write(200, {"Content-Type": "text/plain"});
    response.end("Welcome to the homepage!\n");
    // 中间件在此停止。
  } else {
    next();
  }
});

// 关于页面
app.use(function(request, response, next) {
  if (request.url == "/about") {
    response.write(200, {"Content-Type": "text/plain"});
    response.end("Welcome to the about page!\n");
    // 中间件在此停止。
  } else {
    next();
  }
});

// 404错误！
app.use(function(request, response) {
  response.write(404, {"Content-Type": "text/plain"});
  response.end("404 error!\n");
});

http.createServer(app).listen(1337);
```

“这太丑了！我需要构建一个框架，”你说道。真野蛮。你永远都不会满足，不是吗？真的会有足够的一时刻吗？

Node.js

有些人看到了 Connect，他们说：“这段代码可以写得更简单”。于是他们构建了 Express。（实际上，看起来他们像是看到了 Sinatra[^192] 并偷了它。）

## 顶层：Express

我们终于来到了这场极客之旅的第三幕。我们正处于抽象山的顶点。那里有美丽的日落。你长长的金发在凉凉的风中飘动。

就像 Connect 扩展了 Node 一样，Express 扩展了 Connect。开头看起来和 Connect 非常相似：

```javascript
var express = require("express");
var http = require("http");
var app = express();
```

结尾也是如此：

```javascript
http.createServer(app).listen(1337);
```

中间部分是不同的。Connect 给你一个酷炫的功能（中间件），而我认为 Express 给了你三个酷炫的功能：路由、更好的请求处理器和视图。让我们从路由开始。

# 酷炫的功能 1：路由

路由是将不同的请求映射到特定处理程序的方法。在上面的许多示例中，我们有一个首页、一个关于页面和一个 404 页面。在示例中，我们基本上是通过一堆 `if` 语句来实现这些。

但 Express 比它更智能。Express 给了我们一种被称为“路由”的东西，我认为用代码比用英语解释得更清楚：

> [192]:http://www.sinatrab.com/

```javascript
var express = require("express");
var http = require("http");
var app = express();

app.all("*", function(request, response, next) {
  response.writeHead(200, {"Content-Type": "text/plain"});
  next();
});

app.get("/", function(request, response) {
  response.end("Welcome to the homepage!");
});

app.get("/about", function(request, response) {
  response.end("Welcome to the about page!");
});

app.get("**", function(request, response) {
  response.end("404!");
});

http.createServer(app).listen(1337);
```

哦。这真酷。

在基础规则之后，我们通过 `app.all` 表示“每个请求都通过这个函数”。那个函数看起来非常像中间件，不是吗？

三次对 `app.get` 调用是 Express 的路由系统。它们也可以是 `app.post`，响应 POST 请求，或者任何其他 HTTP 方法。第一个参数是路径，如 `/about` 或 `/`。第二个参数是请求处理器，类似于我们之前看到的。[这些请求处理器] 行为类似于中间件，唯一的例外是它们可以调用 `next()` 来跳过后续路由。简短来说：它们基本上就是中间件。它们只是函数，和之前一样。这些路由可以变得更智能，像这样：

```javascript
app.get("/hello/:who", function(req, res) {
  res.end("Hello, " + req.params.who);
});
```

重启服务器并访问 localhost:1337/hello/world 查看以下内容：

Hello, world!

这个示例也使用了正则表达式，你可以通过路由做很多事情。对于概念理解，我已经说足够了。但它更酷了。

# 酷炫的功能 2：请求处理

路由已经足够了，但 Express 是绝对无情的。它增强了请求和响应对象。旧的东西还在那里，但它们添加了一些新东西！如果你有 `redirect`，Express 会非常好用。这里有一些示例：

```javascript
response.redirect("/hello");
response.redirect("http://www.example.net");
response.redirect(301, "http://www.example.org"); // HTTP 状态码
```

这在原生 Node 中没有，Connect 也缺失，但 Express 添加了。像 `sendFile` 这样的东西允许你发送整个文件：

```javascript
response.sendFile("/path/to/anime");
```

请求有很多酷的属性，比如获取 IP 地址和文件。从概念上说，没什么需要知道的 Express 扩展了请求和响应。对于一切，请查看 API 文档。

# 酷炫的功能 3：视图

更多功能？哦，Express 在害羞。Express 可以处理视图。这并不糟糕。设置如下：

```javascript
// 启动 Express
var express = require("express");
var app = express();

// 设置视图目录为 /views
app.set("views", __dirname + "/views");

// 使用 Jade 模板语言
app.set("view engine", "jade");
```

第一部分一直一样。然后说“我们的视图在 views 文件夹中”。然后说“Jade”是一种模板语言。我们稍后会看到它是如何工作的！现在，我们设置了这些视图。如何使用它们？

让我们从创建一个 `index.jade` 文件并将其放入 `views` 目录开始。它可能像这样：

```jade
doctype html
html

body
  h1 Hello, world!
  p= message
```

这基本上是没有括号的 HTML。如果你熟悉 HTML，这应该很简单。唯一有趣的是最后一行。`message` 是一个变量！哇！那是从哪里来的？我会告诉你。

我们需要从 Express 渲染视图。看起来如下：

```javascript
app.get("/", function(request, response) {
  response.render("index", { message: "I love anime" });
});
```

Express 为 `response` 添加了一个名为 `render` 的方法。有很多智能的东西，但它基本上查看视图引擎和 views 目录（我们之前定义的）并渲染 `index.jade`。最后一步（我假设是第一步）是安装 Jade，因为它没有随 Express 绑定。将其添加到 `package.json` 或通过 `npm` 安装。

如果你完成了所有设置，看这个页面¹⁹⁸。这里是源代码¹¹⁹⁹。

- ¹⁹⁸http://jade-lang.com/
- ¹⁹⁸https://evanhahn.com/wp-uploads/2013/05/anime.html
- ¹¹⁹⁹https://gist.github.com/EvanHahn/5673968

## 额外来自 Connect 和 Node 的一切

我想提醒 Express 是构建在 Connect 之上的，而 Connect 构建在 Node 之上。这意味着所有的 Connect 中间件都可以用于 Express。这很有用！例如：

```javascript
var express = require("express");
var app = express();
app.use(express.logger()); // 继承自 Connect
app.get("/", function(req, res) {
  res.send("anime");
});
app.listen(1337);
```

如果你从这篇文章中学到一件事，那应该是这个。如果你的大脑还有另一个趣闻：河马是粉色的！

## 实际构建东西

这篇文章中的大部分内容都是概念性的，但让我引导你走向构建你想构建的东西的正确方向。我不想深入细节。

你可以将 Express 安装为终端中的一个可执行文件。它会输出一些样板代码，这对启动你的应用程序非常有帮助。使用 `npm` 安装：

```bash
### 你执行此操作可能需要 sudo:
npm install -g express
```

如果你需要帮助，使用 `express --help`。它会输出一些选项。例如，假设我想使用 EJS 模板和 LESS 作为 CSS。我的应用程序命名为 "MyApp"。这是我开始启动时输入的命令：

```bash
express --ejs --css less myWeb
```

当你进入该目录并运行 `npm install` 时，它会生成大量文件。如果你这样做，你就会有一个运行的 Node 基础应用程序了！我建议查看生成的文件以了解一些模板代码，然后进行大量修改。这还不是一个完整的应用程序，但我发现入门时翻阅这些文件非常有帮助。

GitHub 上的许多官方示例也有帮助²⁰⁰。

- 如果你像我一样使用 CoffeeScript²⁰¹，你应该知道所有这些东西都适用于

> ²⁰⁰https://github.com/visionmedia/express/tree/master/examples
> ²⁰¹http://evanhahn.com/i-love-coffeescript/

Node.js

CoffeeScript。你甚至不需要编译它！与其用 `node app.js` 启动服务器，不如用 `coffee app.coffee` 启动。这就是我在我的应用中的做法。我。没错。我是个大人物。我有一个博客。

- 当我看到 `app.use(app.router)` 时，我很困惑——Express 不是一直都在使用路由器吗？简短回答是，`app.router` 是路由中间件，当你定义路由时它是隐式包含在内的。你可以显式地包含它，因为你可以使用路由中间件使其在其他中间件之前运行，这有时是需要的。这个 StackOverflow 解释得很好²202。

- 本指南是为 Express 3 编写的，而版本 4 的路线图²203 显示了某些剧变化的可能性。最值得注意的是，Express 可能会被拆分成许多许多小的模块，并吸收一些 Connect 的功能。这还悬而未决，但这些“计划”值得一看。

# 我渴求

难道还没有满足你吗？你这个贪婪的。你让我恶心。很快，你就会坐在鸦片馆里，半死不活，流着最后一点编程天赋的口水。

如果说 Rails 是用 Ruby 构建 Web 应用的事实标准，而魔鬼受虐是用 PHP 构建 Web 应用的事实标准，我的印象是 Express 是构建 Web 应用的事实标准。与 Rails 不同，Express 的层次要低得多。似乎还没有什么高级 Node 库脱颖而出。我认为这将会改变。请保持关注。

我不会在这里详述，但由于 Express 是构建在 Connect 之上的，而 Connect 是构建在 Node 之上的，人们已经在 Express 之上构建了许多东西。Express wiki 列出了它们²204，其中许多都非常酷。如果你愿意，可以使用这些框架，也可以坚持使用底层的 Express。无论哪种，去构建酷炫的东西吧！

上一个：概念：让异步加载看起来像同步加载²205

亲爱的版权所有者：除非另有说明，所有内容均根据知识共享署名许可协议²206 授权。除非另有说明，所有代码均根据 Unlicense 协议²207 免费授权。你看起来简直迷人。请尽快回来。

²202 https://stackoverflow.com/a/1295081/10410
²203 https://github.com/visionmedia/express/wiki/4-x-roadmap
²204 https://github.com/visionmedia/express/wiki/frameworks-build-with-express
²205 https://evanhann.com/javascript-method_missing/
²206 http://creativecommons.org/licenses/by/3.0/
²207 http://unlicense.org/
²208 http://www.lulusapeice.com/

# 关于作者

![](img/5f4a286ef99041bf37736af72f6b8b9b_125_0.png)

Azat Mardan：一名软件工程师、作者和瑜伽士。

Azat Mardan 在 Web、移动和软件开发领域拥有超过 12 年的经验。Azat 拥有信息学学士学位和信息系统技术硕士学位，他具备深厚的学术知识和丰富的实践经验。

目前，Azat 在 DocuSign^209 担任高级软件工程师，他的团队使用 Node.js、Express.js、Backbone.js、CoffeeScript、Jade、Stylus 和 Redis 技术栈重建了服务 5000 万用户的产品（DocuSign Web 应用）。

最近，他在精选的社交媒体新闻聚合网站 Storify.com^210（已被 LiveFire^211 收购）担任工程师，该网站被 BBC、CNN、白宫等机构使用。与其它公司不同，Storify 的一切都运行在 Node.js 上。它是开源项目的维护者。

---

- [费曼学习法](https://wiki.example.org/feynmans_learning_method)的灵感源于诺贝尔物理奖获得者**理查德·费曼**。

1. 运用费曼技巧，你只需花上`20 min`就能深入理解知识点，而且记忆深刻，*难以遗忘*。

```javascript
if (condVar > someVal) {console.log("xxx")}
```

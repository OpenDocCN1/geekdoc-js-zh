
# JavaScript 入门指南

序言：Daniel Jebaraj

编辑：

本书由 Jay Natarajan 编辑，他为 Syncfusion, Inc. 的高级产品经理。

- 利用作用域链绕过嵌套函数
- 作用域链（即词法作用域）
- 作用域由函数定义决定，而非调用
- 原型属性的概念概述
- 默认原型属性是一个 `Object()` 对象
- 从构造函数创建的实例与构造函数的原型属性相连
- 原型链的终点是 `Object.prototype`
- 原型链返回在链中找到的第一个匹配项
- 用新对象替换原型属性将移除默认构造函数属性
- 从原型继承属性的实例将始终获得最新值
- 用新对象替换原型属性不会更新旧实例
- 用户定义的构造函数可以利用与原生构造函数相同的原型继承
- 创建继承链（原始意图）
- 在数组中添加和更新值

Daniel Jebaraj, Syncfusion, Inc. 副总裁

### 保持在前沿

正如你们许多人所知，Syncfusion 是 Microsoft 平台软件组件的供应商。这使我们处于一个既兴奋又充满挑战的位置，即始终处于前沿。

每当平台或工具从 Microsoft 发布时（如今似乎几乎每隔一周就有一次），我们都必须快速地自我教育。

### 信息虽丰富，但难以消化

在现实中，这意味着大量的书籍订单、博客搜索和 Twitter 扫描。

虽然信息在互联网上变得随手可得，出版的书籍也越来越多（即使是针对较新颖的话题），但一个持续阻碍我们的方面是无法找到简洁的科技概览类书籍。

我们通常面临两种选择：阅读 500 页以上的厚书，或者在网络上搜索相关的博客文章和其他文章。和其他每一位有工作要做、有客户要服务的一样，我们发现这非常令人沮丧。

### Succinctly 系列

这种挫败感转化为一种强烈的渴望，即编写一系列简洁的技术书籍，目标读者是在 Microsoft 平台上工作的开发者。

我们深信，考虑到开发者所拥有的背景知识，大多数主题都可以编写成 50 到 100 页之间的书籍。

这正是我们决定通过 *Succinctly* 系列实现的目标。难道不是所有美好的事物都源于对改善现状的深切愿望吗？

### 最优秀的作者，最好的内容

每一位作者都是从才华横溢的专家库中精心挑选出来的，他们共享我们的愿景。你手中的这本书以及该系列中的其他书籍，都是作者们不懈努力的成果。你将发现，这些原创内容保证你在喝几杯咖啡的时间内就能上手。

### 永久免费

Syncfusion 将致力于制作多个主题的书籍。这些书籍将永远免费。我们发布的任何更新也是免费的。

### 免费？有什么猫腻？

这里没有猫腻。Syncfusion 在这项工作中有切身利益。

作为组件供应商，我们的独特主张一直是提供比市场上任何其他对手都更深入、更广泛的框架。开发者教育极大地帮助我们营销并竞争那些承诺“一键支持 AJAX”或“把月亮变成奶酪”的竞争对手。

### 让我们知道你的想法

如果你有任何感兴趣的主题、想法或反馈，请随时通过 `succinctly-series@syncfusion.com` 与我们联系。

我们衷心希望你喜欢这本书，并且它能帮助你更好地理解学习主题。感谢阅读。

请在 Twitter 上关注我们并在 Facebook 上“点赞”我们，帮助我们推广 *Succinctly* 系列！

# 关于作者

Cody Lindley 是一位客户端工程师（又称前端开发人员）以及一名正在戒掉的 Flash 开发者。他在专业领域拥有超过 11 年的经验，在 HTML、CSS、JavaScript、Flash 以及与 Web 开发相关的客户端性能技术方面有着深厚的背景。当他没有在“焊接”客户端代码时，他可能正在从事界面/交互设计，或者在编写材料以及在各种会议上演讲。当没有坐在电脑前时，可以肯定他正在与爱达荷州波伊西的妻子孩子度过时光——进行铁人三训练、滑雪、山地自行车、公路自行车、高山登山、阅读、看电影，或对基督教世界观的理性证据进行辩论。

# 引言

这本书并不是关于 JavaScript 设计模式，也不是关于如何用 JavaScript 代码实现面向对象的范式。它并不是为了区分 JavaScript 语言的优缺点而编写的。它不是一份完整的参考指南。它的目标读者不是编程初学者或完全没有接触过 JavaScript 的人。它也不是一本 JavaScript 菜谱。这类书籍已经有人写过了。

我的意图是写一本书，通过对原生 JavaScript 对象及其支持的细微差别（复杂值、原始值、作用域、继承、头对象等）进行研究，为读者提供一个准确的 JavaScript 世界观。我希望这本书是对 ECMA-262 第3 版规范的简短易懂的总结，重点关注 JavaScript 中对象的本质。

如果你是一个只使用 JavaScript 库（如 jQuery、Prototype 等）的设计师，我希望书中的内容能让你从 JavaScript 库的维护者蜕变为一名 JavaScript 开发者。

# 为什么我要写这本书？

首先，我必须承认，我写这本书是为了我自己。老实说，我制作这些材料是为了让自己能够“自饮其果”，并永远记住它的味道。对于他人，我希望有一份用自己语言编写的参考，以便需要时唤起记忆：

- 库导致了“黑盒”症，这在某些方面可能有益，但在另一些方面有害。事情可能完成得快速且高效，但你不知道为什么或如何做到。当出现问题或性能成为问题时，“如何做”变得非常重要。事实上，任何在构建 Web 应用（或只是一个良好的注册页面）时打算实现 JavaScript 库或框架的人，都应该查看内部并理解引擎。这本书是为那些想要打开引擎盖并亲手操作 JavaScript 本身的人编写的。

# 第1章 JavaScript 对象

## 创建对象

在 JavaScript 中，对象是这一切的核心：几乎一切都是对象，或者表现得像对象。理解了对象，你就理解了 JavaScript。所以，让我们来研究 JavaScript 中对象的创建方式。

对象仅仅是一个存储一组命名值（也称为属性）的容器。在查看任何 JavaScript 代码之前，让我们先进行逻辑推导。以我为例，用通俗的语言，我们可以用表格来表示一个 "cody"：

| 属性 | 属性值 |
|---|---|
| living | True |
| age | 33 |
| gender | Male |

表格中的单词 "cody" 只是这组属性名和对应值的标签，这些内容恰恰构成了 "cody" 的本质。正如从表格所示，我是活着的，33岁，男性。

然而，JavaScript 并不使用表格进行交流。它使用对象，而对象与 "cody" 表格中包含的部分相似。将 cody 表格翻译成真正的 JavaScript 对象看起来如下：

```html
<!DOCTYPE html><html><body><script>
// 创建 cody 对象
var cody = new Object();
// 然后用属性填充 cody 对象（使用点表示法）
cody.living = true;
cody.age = 33;
cody.gender = 'male';
console.log(cody); // 输出 Object {living = true, age = 33, gender = 'male'}
</script></body></html>
```

请记住：对象本质上只是属性的容器，每个属性都有一个名称和一个值。这种带有命名值的属性容器（即对象）的概念，被 JavaScript 用作在 JavaScript 中表示值的构建块。

cody 对象是一个值，我通过创建一个对象、给该对象命名、然后赋予该对象属性，将其表示为一个 JavaScript 对象。

到目前为止，我们讨论的 cody 对象只有静态信息。由于我们处理的是一种编程语言，我们希望编写 cody 对象来实际执行某些操作。否则，我们拥有的只是类似于 JSON 的数据库。为了让 cody 对象活起来，我需要添加一个属性方法。方法执行函数。具体来说，在 JavaScript 中，方法是包含 `Function()` 对象的属性，其意图是对包含该函数的对象进行操作。

如果我用一个 getter 方法（get 方法）更新 cody 表格，用通俗的英语描述应该是这样的：

| 属性 | 属性值 |
| --- | --- |
| living | True |
| age | 33 |
| gender | Male |
| Getter | 返回 gender 的值 |

使用 JavaScript，更新后的 cody 表格中的 get 方法看起来如下：

示例：sample02.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var cody = new Object();
cody.living = true;
cody.age = 33;
cody.gender = 'male';
cody.getGender = function () { return cody.gender; };

console.log(cody.getGender()); // 输出 male'
</script></body></html>
```

getter 方法是 cody 对象的一个属性，用于返回 cody 的其他属性值之一：存储在 gender 属性中的值 "male"。你必须意识到，如果没有方法，我们的对象除了静态属性外将别无所有。

我们到为止讨论的 cody 对象就是我们所说的 `Object()` 对象。我们通过调用 `Object()` 构造函数产生的空白对象来创建 cody 对象。将构造函数想象成生产预定义对象的模板或切割器。在 cody 案例中，我使用 `Object()` 构造函数产生了一个我命名为 cody 的对象。因为 cody 是通过 `Object()` 构造函数构建的对象，所以我们称之为 `Object()` 对象。除了创建像 cody 这样简单的 `Object()` 对象之外，你真正需要理解的是，JavaScript 对象中表示的大多数值（原始值如 "foo"5 和 true 是例外，但有等价的包装对象）。

考虑到从 `Object()` 构造函数创建的 cody 对象与通过 `String` 构造函数创建的字符串对象并没有区别。为了强调这一点，请检查并对比以下代码：

示例：sample0.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var myObject = new Object(); // 生成一个 Object() 对象。
myObject['0'] = 'f';
myObject['1'] = 'o';
myObject['2'] = 'o';

console.log(myObject); // 输出 Object {="f", 1="o", 2="o"}

var myString = new String('foo'); // 生成一个 String() 对象。
console.log(myString); // 输出 foo {="f", 1="o", 2="o"}
</script></body></html>
```

事实证明，myObject 和 myString 都是对象...!它们可以拥有属性、继承属性，并由构造函数产生。包含 "foo" 字符串值的 `myString` 变量看起来非常简单，但惊讶的是，它在表象之下并不是真正的对象结构。如果你检查你生成的对象，会发现它们在实质上是相同的对象，但类型不同。更重要的是，我希望你开始看到 JavaScript 使用对象来表示值。

## 注意事项

你可能会觉得以对象形式看到字符串值 'foo' 很奇怪，因为通常字符串被表示为原始值。

默认情况下返回一个对象（即 `this`）而不是值 `false`。从函数返回的新对象被认为是构建它的构造函数的实例。

再次考虑 `Person()` 构造函数，这次请仔细阅读以下代码示例中的注释，因为它们强调了 `new` 关键字的作用。

示例：sample06.html

```html
<!DOCTYPE html lang="en"><body><script>

/* Person 是一个构造函数。它的编写意图是
与 new 关键字一起使用。 */
var Person = function(living, age, gender) {
    // """ 下面是正在创建的新对象（即 this
    new Object();
    this.living = living;
    this.age = age;
    this.gender = gender;
    this.getGender = function () { return this.gender; }
// 当使用 new 关键字调用函数时，返回的是 "this"
// 而不是 false。
}

// 实例化一个名为 cody 的 Person 对象。
var cody = new Person(true, 33, 'male');

// cody 是一个对象，也是 Person() 的实例
console.log(typeof cody); // 打印 object。
console.log(cody); // 打印 cody 的内部属性和值。
console.log(cody.constructor); // 打印 Person() 函数。
}
</script></body></html>
```

sample06.html 代码利用了用户定义的构造函数（即 `Person()`）来创建 `cody` 对象。这与下面的代码中 `Array()` 构造函数创建 `Array()` 对象（例如 `new Array()`）没有区别。

示例：sample07.html

```html
<!DOCTYPE html lang="en"><body><script>

    // 实例化一个名为 myArray 的 Array 对象。
    var myArray = new Array(); // myArray 是 Array 的实例。

    // myArray 是一个对象，也是 Array() 构造函数的实例。
    console.log(typeof myArray); // 打印 object！什么？是的，数组是一种类型
object。

    console.log(myArray); // 打印 []

    console.log(myArray.constructor); // 打印 Array()
</script></body></html>
```

在 JavaScript 中，大多数值（排除原始值）都涉及从构造函数创建或实例化对象。从构造函数返回的对象被称为实例。请确保你熟悉这些语义，以及利用构造函数来生成对象的模式。

## 原生 JavaScript 对象构造函数

JavaScript 语言包含九种原生（或内置）对象构造函数。这些对象被 JavaScript 用于构建该语言，我所指的“构建”是指这些对象被用于在 JavaScript 代码中表示值对象，并协调语言的若干项功能。因此，原生对象构造函数是多层，它们不仅能产生对象，还用于促进语言的许多编程惯例。例如，函数是由 `Function()` 构造函数创建的对象，但用于使用 `new` 关键字从构造函数创建其他对象。

JavaScript 随带的原生对象构造函数有：

- `Number()`
- `String()`
- `Boolean()`
- `Object()`
- `Array()`
- `Function()`
- `Date()`
- `RegExp()`
- `Error()`

JavaScript 的大部分内容是由这九个对象以及字符串、数字和 Boolean 值构建而成的。详细了解这些对象是充分利用 JavaScript 独特的编程能力和语言灵活性的关键。

## 注意事项

`Math` 在这里是异类。它是一个静态对象，而不是构造函数，这意味着你不能执行 `var x = new Math()`。但如果它已经过实例化（例如 `Math.PI`），你就可以使用它。事实上，`Math` 是 JavaScript 设置的用于存放函数的对象命名空间。

原生对象有时被称为“全局对象”，因为它们是 JavaScript 原生可用的对象。不要将“全局对象”一术语与“头部”全局对象混淆，后者是作用域链的最顶层，例如所有浏览器中的 `window` 对象。

`Number()`、`String()` 和 `Boolean()` 构造函数不仅构建对象；它们还根据构造函数的使用方式为字符串、数字和 Boolean 提供值。如果你直接调用这些构造函数，将返回一个复杂对象。如果你在代码中简单地表示一个数字、字符串或 Boolean 值（原始值如 `5`、`"foo"` 和 `true`），那么构造函数将返回原始值而不是复杂的对象值。

## 用户定义/非原生对象构造函数

正如你通过 `Person()` 构造函数看到的那样，我们可以创建自己的构造函数，通过这些函数我们可以产生不仅一个、多个自定义对象。

在下面的示例中，我展示了 `Person()` 构造函数：

示例：object8.html

```html
<!DOCTYPE type><html lang="en"><body><script>
var Person = function (living, age, gender) {
    this.living = living;
    this.age = age;
    this.gender = gender;
    this.getGender = function () { return this.gender; };
};

var code = new Person(true, 33, 'male');
console.log(code); // 打印 Object {living=true, age=33, gender="male"}

var lisa = new Person(true, 34, 'female');
console.log(lisa); // 打印 Object {living=true, age=34, gender="female"}

</script></body></html>
```

你可以看到，使用唯一的参数并调用 `Person()` 构造函数，你可以轻松创建各种唯一的数字对象。当你需要两个或三个具有相同属性但不同值的对象时，这非常有用。想起来，这就是 JavaScript 处理原生对象的方式。`Person()` 构造函数遵循与 `Array` 构造函数相同的模式。因此，`new Array('foo', 'bar')` 与 `new Person(true, 33, 'male')` 并没有区别。创建你自己的构造函数只是在使用 JavaScript 自身用于原生构造函数时的相同模式。

## 注意事项

这不是强制的，但在创建旨在用于与 `new` 操作符配合构造函数时，最佳实践是将构造函数名的第一个字母大写：使用 `Person()` 而不是 `person()`。

构造函数中一个棘手的问题是函数内部对 `this` 值的使用。记住，构造函数就像一个饼模具。当与 `new` 关键字一起使用时，它将创建一个具有构造函数内部定义的属性和值的对象。当使用 `new` 时，`this` 字面上指的是将在构造函数内部语句上将创建的新对象或实例。相反，如果你创建一个构造函数并在不使用 `new` 关键字的情况下调用它，该值将指向创建该函数的“父”对象。

通过显式让函数返回一个对象，可以放弃 `new` 关键字和构造函数概念。函数必须显式构建一个 `Object()` 对象并返回它：`var myFunction = function() {return prop:val}};`

## 使用 new 关键字实例化构造函数

构造函数基本上是用于创建预配置对象的饼模具。以 `String()` 为例。当与 `new` 操作符配合使用（`new String('foo')`），它根据 `String()` 模板创建一个字符串实例。让我们来看一个示例。

sample09.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var myString = new String('foo');

console.log(myString); // 打印 foo {0 = "f", 1 = "o", 2 = "o"}
</script></body></html>
```

在这个片段中，我们创建了一个 `String()` 构造函数实例的新对象。同样，我们在 JavaScript 中表示了一个字符串值。

## 注意事项

我并不是建议你使用构造函数代替它们的字面/原始值（例如 `var string="foo";`）。然而，我建议你理解字面/原始值背后发生了什么。

正如之前提到的，JavaScript 语言拥有以下预定义构造函数：`Number()`、`String()`、`Boolean()`、`Object()`、`Array()`、`Function()`、`Date()`、`RegExp()` 和 `Error()`。我们可以通过 `new` 关键字从这些构造函数中的任何一个实例化对象实例。在下面的示例中，我构建了这些原生 JavaScript 对象。

sample10.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 使用 new 为每个原生构造函数实例化一个实例
</script></body></html>
```

```javascript
var myNumber = new Number(23);
var myString = new String('male');
var myBoolean = new Boolean(false);
var myObject = new Object();
var myArray = new Array('foo', 'bar');
var myFunction = new Function('x', 'y', 'return x*y');
var myDate = new Date();
var myRegExp = new RegExp('\bt[a-z]+\b');
var myError = new Error('Darn!');
```

```javascript
// Log/verify which constructor created the object.
console.log(myNumber.constructor); // Logs Number
console.log(myString.constructor); // Logs String
console.log(myBoolean.constructor); // Logs Boolean
console.log(myObject.constructor); // Logs Object
console.log(myArray.constructor); // Logs Array() in modern browsers.
console.log(myFunction.constructor); // Logs Function
console.log(myDate.constructor); // Logs Date
console.log(myRegExp.constructor); // Logs RegExp
console.log(myError.constructor); // Logs Error
```

```html
<script></body></html>
```

通过使用 `new` 运算符，我们告诉 JavaScript 解释器我们想要一个作为相应构造函数实例的对象。例如，在代码示例中，`Date` 构造函数被用于创建日期对象。`Date` 构造函数就像一个日期的饼具模，它根据 `Date()` 构造函数定义的默认模式生成日期对象。

到此时，你应该熟悉如何从原生构造函数创建对象实例（例如 `new String('foo')`）以及用户定义的构造函数（例如 `new Person(true, 33, 'male')`）。

## 注意事项

请记住 `Math` 是一个静态对象——其他方法的容器——它不是一个使用 `new` 运算符的构造函数。

## 从构造函数创建简写或字面量

JavaScript 提供了简写形式——称为“字面量”（literals），用于制造大多数原生对象值，而无需使用 `new Foo()` 或 `new Bar()`。在大多数情况下，字面量语法实现与使用 `new` 运算符相同。异常是 `Number()`、`String()` 和 `Boolean()`——请参考后续示例后的注释。

如果你来自其他编程背景，你可能更熟悉使用字面量创建对象。在下面的示例中，我使用 `new` 运算符实例化原生 JavaScript 构造函数，然后创建等效的字面量。

## 示例：sample11.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myNumber = new Number(23); // 一个对象。
var myNumberLiteral = 23; // 原始数字值，不是对象。

var myString = String('male'); // 一个对象。
var myStringLiteral = 'male'; // 原始字符串值，不是对象。

var myBoolean = new Boolean(false); // 一个对象。
var myBooleanLiteral = false; // 原始布尔值，不是对象。

var myObject = new Object();
var myObjectLiteral = {};
var myArray = new Array('foo', 'bar');
var myArrayLiteral = ['foo', 'bar'];

var myFunction = new Function("x", "y", "return x*y");
var myFunctionLiteral = function (x, y) { return x * y; }

var myRegExp = new RegExp('[a-z]+\b');
var myRegExpLiteral = /[a-z]+\b/;

// 验证字面量是否由同一个构造函数创建。
console.log(myNumber.constructor, myNumberLiteral.constructor);
console.log(myString.constructor, myStringLiteral.constructor);
console.log(myBoolean.constructor, myBooleanLiteral.constructor);
console.log(myObject.constructor, myObjectLiteral.constructor);
console.log(myArray.constructor, myArrayLiteral.constructor);
console.log(myFunction.constructor, myFunctionLiteral.constructor);
console.log(myRegExp.constructor, myRegExpLiteral.constructor);

</script></body></html>
```

你从中获得的要点是：通常情况下，使用字面量仅仅隐藏了与使用 `new` 运算符相同的底层过程。更重要的是，它方便得多！

好了，原始字符串、数字和布尔值的情况稍微复杂一些。在这些情况下，字面量具有原始值的特征，而不是复杂对象。请查看后面的注释。

## 注意事项

在使用字面量用于 `String()`、`Number()` 和 `Boolean()` 时，在这些值被视为对象之前，永远不会创建实际的对象。换句话说，在你尝试使用或检索与构造函数相关的属性之前，你处理的是原始数据类型（例如 `var charactersFoo = 'foo'.length`）。当这种情况发生时，JavaScript 会在后台为该字面量值创建一个包装对象，允许该值被视为对象。然后，在调用方法之后，JavaScript 会丢弃包装对象，值返回字面量类型。这就是为什么字符串、数字和布尔值被认为是原始（或简单）数据类型。这澄清了“JavaScript 中的一切都是对象”的这一误解，正确的概念是“JavaScript 中的一切都可以像对象一样工作”。

## 原始（又称简单）值

JavaScript 值 `5`、`'Foo'`、`true`、`false` 以及 `null` 和 `undefined` 被认为是原始值，因为它们是不可还原的。也就是说，数字就是数字，字符串就是字符串，布尔值是 `true` 要么 `false`，而 `null` 和 `undefined` 仅仅如此。这些值本质上是简单的，不代表由其他值组成的值。

检查以下代码并问自己：字符串、数字、布尔值、`null` 和 `undefined` 值。

## 示例：sample12.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var myString = 'string'
var myArray = 10;
var myBoolean = false;
var myNull = null;
var myUndefined = undefined;

console.log(myString, myArray, myBoolean, myNull, myUndefined);

var myObject = {
myString: 'string',
Number: 10,
myBoolean: false,
myNull: null,
myUndefined: undefined
};

console.log(myObject);

var myArray = ['string', 10, false, null, undefined];

console.log(myArray);
</script></body></html>
```

简单来说，原始值代表 JavaScript 中可用的最低形式（即简单）的数据。

## 注意事项

与使用字面量语法创建相反，当使用 `new` 关键字创建 `String()`、`Number()` 或 `Boolean()` 值时，创建的是一个复杂对象。

至关重要的是理解：`String()`、`Number()` 和 `Boolean()` 构造函数是双用途构造函数，用于创建字面量/原始值以及复杂值。这些构造函数并不总是返回对象，相反，在不使用 `new` 运算符时，它们可以返回实际复杂值的原始表示。

## 原始值 `null`、`undefined`、`"string"`、`10`、`true` 和 `false` 不是对象

`null` 和 `undefined` 值是平凡的值，不需要构造函数，也不需要使用 `new` 运算符来建立为 JavaScript 值。要使用 `null` 或 `undefined`，你只需要像使用运算符一样使用它们即可。

```javascript
var myString = new String('male');
var myBoolean = new Boolean(false);
var myObject = new Object();
var myArray = new Array('foo', 'bar');
var myFunction = new Function('x', 'y', 'return x * y');
var myDate = new Date();
var myExp = new RegExp('[a-z]+\\b');
var myError = new Error('Darn!');
```

```javascript
// 打印 object object object object function object function
console.log(
  type myNumber,
  type myString,
  type myBoolean,
  type myObject,
  type myArray,
  type myFunction, // 注意 typeof 对所有对象返回 function。
  type myDate,
  type myRegExp, // 注意 typeof 对 RegExp 返回 function
  type myError
);
```

```html
<script></body></html>
```

我希望从上面的代码示例中学习到的是：基本值不是对象。基本值之所以特殊性，是因为它们被用来表示简单的值。

## 基本值在 JavaScript 中如何存储/复制

理解基本值是按“面值”存储和操作的极其重要的。这听起来可能很简单，但这意味着如果我在一个名为 `myString` 的变量中存储字符串 "foo"，那么值 "foo" 就字面地存储在内存中。为什么这很重要？一旦你开始操作（例如复制）值，你就必须具备这种知识，因为基本值是按字面复制的。

在接下来的示例中，我们将 `myString` 的值（'foo'）存储在变量 `myStringCopy` 中，它的值被字面地复制了。即使我们更改了原始值，由 `myStringCopy` 引用的复制值也保持不变。

示例：sample14.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var myString = 'foo' // 创建一个基本字符串对象。
var myStringCopy = myString; // 将其值复制到新变量中。
var myString = null; // 修改存储在 myString 变量中的值。
```

```javascript
/* myString 的原始值已复制到 myStringCopy 中。这通过更新 myString 的值然后检查 myCopy 的值得到了确认。*/

console.log(myString, myStringCopy); // 打印 'null foo'
```

```html
<script></body></html>
```

要掌握的概念是，基本值是作为不可约的值进行存储和操作的。通过它们的值来引用它们。在示例中，我们将 `myString` 值复制（或克隆）到变量 `myStringCopy`。当我们更新 `myString` 的值时，`myStringCopy` 的值仍然拥有旧 `myString` 的副本。

## 基本值是按值相等的

基本值可以进行比较，以查看它们的值是否在字面上是相同的。正如逻辑所暗示的那样，如果你比较一个包含数字值 10 的变量与另一个包含数字值 10 的变量，JavaScript 将认为它们是相等的，10 等于 10（即 10）。同样，如果你比较基本字符串 'foo' 和另一个值为 'foo' 的基本字符串，情况也是一样的。比较结果将根据它们的值说明它们之间是互为相等的（即 'foo' === 'foo'）。

在接下来的代码中，我使用基本数字演示了“按值相等”，并与复杂的数字对象进行了对比。

示例：sample15.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var price1 = 10;
var price2 = 10;
var price3 = new Number('10'); // 一个复杂的数字对象，因为我们使用了它。
var price4 = price3;

console.log(price1 === price2); // 打印 true。

/* 打印 false是因为 price3 包含一个复杂的数字对象而 price1 是一个基本值。 */
console.log(price1 === price3);

// 打印 true是因为复杂值是按引用相等，而不是按值。
console.log(price4 === price3);

// 如果我们更新 price4 变量包含一个基本值怎么办？
price4 = 10;
```

```javascript
console.log(price4 === price3); // 打印 false：price4 现在是基本值的而不是复杂的。
```

```html
<script></body></html>
```

这里要掌握的概念是，基本值在比较时，将检查所表达的值是否相等。当使用 `new` 关键字创建字符串、数字或布尔值（例如 `new Number('10')`）时，它不再是基本值了。因此，比较结果与通过字面量语法创建的值并不相同。这并不意外，因为基本值是按值存储的（即 10 === 10 为真），而复杂值是按引用存储的（即 price3 和 price4 是否包含同一个同一个引用）。

## 字符串、数字和基本值在像对象一样使用时表现得像对象

当基本值被用作由构造函数创建的对象来使用时，JavaScript 会将其转换为对象以响应当前的表达式，然后丢弃对象的属性并将其变回基本值。在下面的代码中，我取了基本值并展示了当值被视为对象时会发生什么。

示例：sample16.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 生成基本值
var myList = null;
var undefined = undefined;
var primitiveString1 = "foo";
var primitiveString2 = String('foo'); // 没有使用 new，所以我们得到了基本值。
var primitiveNumber1 = 10;
var primitiveNumber2 = Number('10');
var primitiveBoolean1 = true;
var primitiveBoolean2 = Boolean(true);
var primitiveNull1 = null;
var primitiveNull2 = null;
var primitiveUndefined1 = undefined;
var primitiveUndefined2 = undefined;

// 当基本值被用作由构造函数创建的对象来使用时，JavaScript 会将其转换为对象以响应当前的表达式，然后丢弃对象的属性并将其变回基本值。在下面的代码中，我取了基本值并展示了当值被视为对象时会发生什么。
```

这里需要记住的观点是：当你改变一个复杂值时——因为它是通过引用存储的——你改变了所有引用该复杂值的变量中所存储的值。在我们的代码中，当你更新任意一个变量中存储的对象时，`myObject` 和 `copyOfOfObject` 都会发生变化。

## Notes

当使用 `new` 关键字创建 `String()`、`Number()` 和 `Boolean()` 值时，或者在后台将其转换为复杂对象时，这些值继续通过值进行存储/复制。尽管原始值可以像复杂值一样对待，但它们并不具备通过引用复制的特性。

要真正地复制一个对象，你必须从旧对象中提取值并将它们注入到新对象中。

## 复杂对象通过引用相等

在比较对象时，只有当它们引用同一个对象时（即具有相同的地址时），它们才是相等的。两个包含相同对象的变量彼此是不等的，因为它们实际上并没有指向同一个对象。

在下面的示例中，`objectFoo` 和 `objectBar` 具有相同的属性，事实上也是相同的对象，但当询问它们是否 `===` 相等时，JavaScript 告诉我们它们并不相等。

示例：sample19.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var objectFoo = { same: 'same' };
var objectBar = { same: 'same' };

// 输出 false，JS 并不在乎它们是相同的且具有相同的类型。
console.log(objectFoo === objectBar);

// 如何衡量复杂对象的等值性。
var objectA = { foo: 'bar' };
var objectB = objectA;

console.log(objectA === objectB); // 输出 true，因为它们引用了
// 同一个对象。
</script></body></html>
```

这里需要记住的观点是：指向内存中复杂对象的变量相等，仅仅是因为它们使用了相同的“地址”。相反，两个独立创建的对象即使是相同类型且拥有完全相同的属性，它们也是不等的。

## 复杂对象具有动态属性

指向现有复杂对象的新变量不会复制该对象。这就是为什么复杂对象有时被称为引用对象。一个复杂对象可以拥有你想要数量的引用，即使在对象被更改时，它们也始终指向同一个对象。

示例：sample20.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var objA = { property: 'value' };
var pointer1 = objA;
var pointer2 = pointer1;

// 更新 objA.property，所有的引用（pointer1 和 pointer2）
// 都会更新。
objA.property = null;

// 输出 'null null null'，因为 objA、pointer1 和 pointer2 都
// 引用同一个对象。
console.log(objA.property, pointer1.property, pointer2.property);
</script></body></html>
```

这允许动态对象属性，因为你可以定义一个对象、创建引用、更新对象，并且所有变量都会引用该更新后的“get”。

## 用于原始值和复杂值的 typeof 运算符

`typeof` 运算符可以用于返回你正在处理的值的类型。但它返回的值并不完全一致，或者不像某些人所说的。以下代码展示了使用 `typeof` 运算符返回的值。

示例：sample21.html

```html
<!DOCTYPE html><html lang="en"><body><script>
// 原始值。
var myNull = null;
var myUndefined = undefined;
var primitiveString1 = "string";
var primitiveString2 = String('string');
var primitiveNumber1 = 10;
var primitiveNumber2 = Number('10');
var primitiveBoolean1 = true;
var primitiveBoolean2 = Boolean('true');

console.log(typeof myNull); // 输出 object? 什么？注意点……
console.log(typeof myUndefined); // 输出 undefined。
```

```javascript
console.log(typeof primitiveString1, typeof primitiveString2); // 输出 string string。
console.log(typeof primitiveNumber1, typeof primitiveNumber2); // 输出 number
console.log(typeof primitiveBoolean1, typeof primitiveBoolean2); // 输出 boolean boolean。
```

```javascript
// 复杂值。
var myNumber = new Number(23);
var myString = new String('male');
var myBoolean = new Boolean(false);
var myObject = new Object();
var myArray = new Array('foot', 'bar');
var myFunction = new Function('x', 'y', 'return x * y');
var myDate = new Date();
var myRegExp = new RegExp('[a-z]+');
var myError = new Error('Darn!');

console.log(typeof myNumber); // 输出 object。
console.log(typeof myString); // 输出 object。
console.log(typeof myBoolean); // 输出 object。
console.log(typeof myObject); // 输出 object。
console.log(typeof myArray); // 输出 object。
console.log(typeof myFunction); // 输出 function。
console.log(typeof myDate); // 输出 object。
console.log(typeof myRegExp); // 输出 object。
console.log(typeof myError); // 输出 object.
</script></body></html>
```

对值（原始或复杂）使用 `typeof` 运算符时，你应该意识到你正在处理的可能值。

## 动态属性允许对象

复杂对象由动态属性组成。这意味着 JavaScript 中的大多数对象可以随时更新或更改。正因如此，我们可以改变 JavaScript 的原生性质。我并不是叫你这样做；事实上，我不认为应该这样做。可以在原生对象上存储属性并在它们的原型上添加新方法。

示例：sample22.html

```html
<!DOCTYPE html><html lang="en"><body><script>
  var foo = {};

  console.log(foo.constructor === Object); // 输出 true，因为 object()
  console.log(foo.constructor); // 指向 Object 构造函数。
</script></body></html>
```

## 所有构造函数实例都具有构造 属性

当对象被实例化时，`constructor` 属性会在后台作为该对象的一个属性被创建。该属性指向创建该对象的构造函数，然后你可以验证该对象是否有 `constructor` 属性。这非常有用：如果我正在处理某个实例，并且不知道是谁或什么创建了它（特别是如果是某人的代码），我可以判断它是一个数组、一个对象还是其他什么。

示例：sample24.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var myNumber = new Number('23');
myNumberL = 23; // 字面量简写。
var myString = new String('male');
myStringL = 'male'; // 字面量简写。
var myFunction = new Boolean('true');
myBooleanL = true; // 字面量简写。
var myObject = new Object();
myObjectL = {}; // 字面量简写。
var myArray = new Array();
myArrayL = []; // 字面量简写。
var myFunction = new Function();
myFunctionL = function () { }; // 字面量简写。
var myDate = new Date();
myDateL = new Date();
var myRegExp = new RegExp('/./');
myRegExpL = /./; // 字面量简写。
var myError = new Error();
myErrorL = new Error();

console.log( // 这些都返回 true。
myNumber.constructor === Number,
myNumberL.constructor === Number,
myString.constructor === String,
myStringL.constructor === String,
myBoolean.constructor === Boolean,
myBooleanL.constructor === Boolean,
myObject.constructor === Object,
myObjectL.constructor === Object,
myArray.constructor === Array,
myArrayL.constructor === Array,
myFunction.constructor === Function,
myFunctionL.constructor === Function,
myDate.constructor === Date,
myRegExp.constructor === RegExp,
myRegExpL.constructor === RegExp,
myError.constructor === Error
);
</script></body></html>
```

```
););</script></body></html>
```

`constructor` 属性在用户定义的构造函数上运行良好。在下面的示例中，我们定义了一个 `CustomConstructor()` 构造函数，然后使用 `new` 关键字调用该函数来生成一个对象。一旦我们有了对象，就可以利用 `constructor` 属性。

Sample:25.html

```
<!DOCTYPE html><html lang="en"><body><script>
var CustomConstructor = function CustomConstructor() { return 'Wow!'; }
var instanceOfCustomObject = new CustomConstructor();

// 打印树。
console.log(instanceOfCustomObject.constructor === CustomConstructor);

// 返回 CustomConstructor() 函数的引用。
// 返回 'function() { return 'Wow!'; }'
console.log(instanceOfCustomObject.constructor);
</script></body></html>
```

## Notes

你可能会困惑，为什么在没有返回对象时，我们仍在验证它是否具有指向构造函数的 `constructor` 属性。通过使用原始值，构造函数仍然会被调用，因此与原始值和构造函数之间仍然存在关系。然而，结果是一个原始值。

如果你希望 `constructor` 属性记录用户定义构造函数的实际名称，你必须给构造函数起一个实际名称（例如：`var Person = function Person(){});`）。

## 验证对象是否是特定构造函数的实例

通过使用 `instanceof` 运算符，我们可以判断一个对象是否是特定构造函数的实例（返回 `true` 或 `false`）。

在下一个示例中，我们验证对象 `InstanceOfCustomObject` 是否是 `CustomConstructor` 构造函数的实例。这对于用户定义的对象以及使用 `new` 运算符创建的原生对象同样有效。

Sample:26.html

```
<!DOCTYPE html>html lang="en"><body><script>
```

// 用户定义的对象构造函数。

var CustomConstructor = function () { this.foo = 'bar'; };

// 实例化 CustomConstructor。

var instanceOfCustomObject = new CustomConstructor();

console.log(instanceOfCustomObject instanceof CustomConstructor); // 打印 true.

// 与原生对象的工作原理相同。

console.log(new Array('foo') instanceof Array); // 打印 true.

</script></body></html>

```

## Notes

处理 `instanceof` 运算符时需要注意的一点是，每当你询问一个对象是否是 `Object` 的实例时，它都会返回 `true`，因为所有对象都继承自 `Object()` 构造函数。

在处理利用对象包装器的原始值时，`instanceof` 会返回 `false`（例如 `'foo' instanceof String` 返回 `false`）。如果字符串 `'foo'` 是使用 `new` 运算符创建的，`instanceof` 运算符将返回 `true`。因此，记住 `instanceof` 只适用于复杂对象，而构造函数创建的实例返回对象。

## 从构造函数创建的实例可以拥有自己的独立属性（即实例属性）

在 JavaScript 中，对象可以随时扩展（即动态属性）。正如之前提到的，准确来说，JavaScript 有可变对象。这意味着从构造函数创建的对象可以增加属性。

在下面的代码示例中，从 `Array()` 构造函数创建一个实例，然后为其添加它自己的属性。

Sample: sample27.html

```

<!DOCTYPE html><html lang="en"><body><script>

var myArray = new Array();

myArray.prop = 'test';

console.log(myArray.prop) // 打印 'test'.

</script></body></html>

```

这可以通过 `Object()`、`RegExp()` 或任何其他非原始构造函数实现——甚至可以是 `Boolean()`。

**Sample:** sample28.html

```

<!DOCTYPE html><html lang="en"><body><script>

// 这可以使用任何实际上产生对象的原生构造函数完成。

var myString = new String();

var myNumber = new Number();

var myBoolean = new Boolean(true);

var myObject = new Object();

varArray = new Array();

var myFunction = new Function('return 2+2');

var myRegExp = new RegExp('\b[a-z]+\b');

myString.prop = 'test';

myNumber.prop = 'test';

myBoolean.prop = 'test';

myObject.prop = 'test';

myArray.prop = 'test';

myFunction.prop = 'test';

myRegExp.prop = 'test';

// 打印 'test', 'test', 'test', 'test', 'test', 'test', 'test'.

console.log(myString.prop,myNumber.prop,myBoolean.prop,myObject.prop,myArray.prop,myFunction.prop,myRegExp.prop);

// 注意：实例属性对原始/字面量值不起。

var myString = 'string';

var myNumber = 1;

var myBoolean = true;

myString.prop = true;

myNumber.prop = true;

myBoolean.prop = true;

// 打印 undefined, undefined, undefined.

console.log(myString.prop,myNumber.prop,myBoolean.prop);

</script></body></html>

```

向从构造函数创建的对象添加属性有时会发生。记住，从构造函数创建的对象实例只是普通的对象。

## Notes

记住，除了它们自己的属性外，实例还可以拥有从原型链继承的属性。或者正如我们在上一个代码示例中看到的，在实例化后添加到构造函数中的属性。这突显了 JavaScript 对象的动态性。

## “JavaScript 对象”和“Object() 对象”的语义

不要将泛指术语“JavaScript 对象”（指 JavaScript 中对象的概念）与 `Object()` 对象混淆。一个 `Object()` 对象（例如 `var myObject = new Object()`）是 JavaScript 中表示的一种非常特定的值类型。正如 `Array()` 对象是一种名为 array 的对象类型，`Object()` 对象也是一种名为 object 的对象类型。核心在于 `Object()` 构造函数产生一个通用的空对象容器，它被称为 `Object()` 对象。同样，`Array()` 构造函数产生一个数组对象，我们把这些对象称为 `Array()`。

在书中，“JavaScript 对象”一术用于指代 JavaScript 中所有的对象，因为 JavaScript 中的大多数值都可以像对象一样工作。这是因为大多数 JavaScript 值是从原生构造函数创建的，这些构造函数产生一种非常特定类型的对象。

你需要记住的是，`Object()` 对象是一种非常特定的值。它是一个通用的空对象。不要将其与用于指代大多数在 JavaScript 中可以表示为对象的值的“JavaScript 对象”术语混淆。

# 第 2 章 处理对象和属性

## 复杂对象可以包含 JavaScript 的大部分内容

`Object()`、`Array()` 和 `Function()` 对象可以包含其他对象。在下面的示例中，我通过使用 `Object()` 对象设置一个对象树来演示这一点。

Sample: sample30.html

```

<!DOCTYPE html><html lang="en"><body><script>

// 使用对象进行封装创建对象链。

var object1 = {

  object1_1: {

    object1_1_1: {foo: 'bar'},

    object1_1_2: {},

  },

  object1_2: {

    object1_2_1: {},

    object1_2_2: {},

  }

};

console.log(object1.object1_1.object1_1.foo); // 打印 'bar'

</script></body></html>

```

这里学习的简单概念是，复杂对象可以包含——或引用 JavaScript 中名上可以表示的任何内容。当你看到这种操作时不要惊讶，因为所有的原生对象都是可以被变的。这甚至适用于对象形式的 `String()`、`Number()` 和 `Boolean()` 值——即当它们使用 `new` 运算符创建时。

## 以程序化的方式封装复杂对象

同样的事情也可以通过 `Array()` 对象（即多维数组）或 `Function()` 对象完成。

## 示例：sample3.html

```

<!DOCTYPE html><html lang="en"><body><script>

// 使用数组进行封装会创建一个多维数组链。

var myArray = [[[]]]; // 一个空数组嵌套在一个空数组内，再嵌套在一个。

/* 这是一个使用函数进行封装的示例：一个空函数内部嵌套另一个空函数。 */

var myFunction = function () {

  // 空函数。

  var myFunction = function () {

    // 空函数。

    var myFunction = function () {

      // 空函数。

    }

  };

};

// 我们也可以进行疯狂天乱的混合和搭配。

var foo = [{ foo: [{ bar: say: function () return 'hi'; }]];

console.log(foo[0].foo[0].bar(say())); // 打印 'hi'。

</script></body></html>

```

这里掌握的核心概念是：某些复杂对象的设计是为了以一种程序有利的方式封装其他对象。

## 使用点表示法（dot notation）或括号符号（bracket notation）获取和更新对象的属性

我们可以使用点表示法或括号符号来获取或更新对象的属性。

在下面的示例中，我演示了点表示法，它是通过使用点命名的对象，后跟跟要获取或更新的属性来实现（例如 `objectName.property`）。

示例：sample2.html

```

<!DOCTYPE html><html lang="en"><body><script>

// 创建一个 cody() 对象。

var cody = new Object();

// 设置属性。

cody.living = true;

cody.age = 33;

cody.gender = 'male';

```

```

cody.getGender = function () { return cody.gender; };

// 获取属性。

console.log(

cody.living,

cody.age,

cody.gender,

cody.getGender()

);// 打印 'true 33 male male'。

// 更新属性，与设置完全一样。

cody.living = false;

cody.age = 99;

cody.gender = 'female';

cody.getGender = function () { return 'Gender = ' + cody.gender; };

```

console.log(cody);

```

<script></body></html>

```

点表示法是获取、设置或更新对象属性最常用的表示法。除非需要，否则括号符号并不常用。在下面的示例中，我将上一个示例中的点表示法替换为括号符号。对象名后跟一个左括号，括号内是带引号的属性名，然后是右括号：

示例：33.html

```

<!DOCTYPE html><html>lang="en"><body><script>

// 创建一个 cody Object() 对象。

var cody = new Object();

// 设置属性。

cody['living'] = true;

cody['age'] = 33;

cody['gender'] = 'male';

cody['getGender'] = function () { return cody.gender; };

// 获取属性。

console.log(

cody['living'],

cody['age'],

cody['gender'],

cody['getGender']() // 直接在末尾加上函数调用即可！

);// 打印 'true 33 male male'。

// 更新属性，与设置非常相似。

cody['living'] = false;

cody['age'] = 99;

```

```

cody['gender'] = 'female';

cody['getGender'] = function () { return 'Gender = ' + cody.gender; };

console.log(cody);

<script></body></html>

```

当你需要访问属性键，而你必须处理的是一个包含代表属性名的字符串值的变量时，括号符号会非常有用。在下一个示例中，我演示了使用括号符号访问属性 `foobar` 较于点表示法的优势。通过使用两个变量并连接后，得到了 `foobarObject` 中包含的属性字符串版本。

示例： sample34.html

```

<!DOCTYPE html><html lang="en"><body><script>

var foobarObject = { foobar: 'Foobar is code for no code' };

var string1 = 'foo';

var string2 = 'bar';

console.log(foobarObject[string1 + string2]); // 看看点表示法如何做到这一点！

<script></body></html>

```

此外，括号符号在获取不是有效的 JavaScript 标识符的属性名时非常方便用。在下面的代码中，我使用数字和保留关键字作为属性名（作为字符串是有效的），只有括号符号可以访问。

示例： sample35.html

```

<!DOCTYPE html><html lang="en"><body><script>

var myObject = { '123': 'zero', 'class': 'foo' };

// 看看点表示法如何做到这一点！记住 'class' 是 JavaScript 中的一个关键字。

console.log(myObject['123'], myObject['class']); // 打印 'zero foo'

<script></body></html>

```




console.log(`myArray.hasOwnProperty('join')`); // Logs false.

它目前并不存在。然而 `myArray` 却可以访问 `join()` 方法，就好像它是自己的属性一样。这里发生了什么？嗯，你刚刚观察了原型链的实际运作。我们访问了一个并不包含在 `myArray` 对象中的原型，但 JavaScript 可以在其他地方找到它。那个地方非常特殊。当 JavaScript 创建 `Array()` 构造函数时，`join()` 方法（以及其他方法）作为原型 `Array()` 的属性被添加了。

重申一下，如果你尝试访问一个不包含该属性的属性，JavaScript 将搜索原型链中创建该对象的构造函数（例如 `Array`），并检查其原型（例如 `Array.prototype`）以查看是否可以找到该属性。如果第一个原型对象没有该属性，JavaScript 将继续在链上向上查找，直到初始构造函数之前的构造函数。它可以一直搜索到链的末端。

链在何结束？让我们再次查看示例，在 `myArray` 上调用 `toLowerCase()` 方法。

## 示例：sample40.html

```html
<!DOCTYPE html><html><body><script>

// myArray 和 Array.prototype 不包含 toLowerCase() 方法。

var myArray = ['foo', 'bar'];

// toLowerCase() 实际上定义在

Object.prototype.toLowerCase

console.log(myArray.toLowerCase()); // Logs foo,bar.

</script></body></html>
```

`toLowerCase()` 方法没有定义在 `myArray` 对象内部。因此，触发了原型链，JavaScript 在 Array 的构造函数原型属性（例如 `Array.prototype`）中查找该属性。那里没有，所以触发了链规则，我们在 `Object()` 原型属性（`Object.prototype`）中查找该属性。是的，找到了。如果没有找到，JavaScript 将会产生一个错误，说明该属性未定义（undefined）。

由于所有原型都是对象，因此链的最后一个环节是 `Object.prototype`。没有其他构造函数原型属性可以被检查。

有一整整一个章节专门将原型链拆解成更小的部分，所以如果你完全没有看懂，请阅读那一章，然后回到这个解释以巩固你的理解。通过对这一问题的简短阅读，我了解到，当找不到属性时（且被视为未定义），JavaScript 将已经查看了几个原型对象以确定该属性是未定义的。查找总是会，而这个查找过程就是 JavaScript 处理继承以及简单属性查找的方式。

## 使用 hasOwnProperty 验证对象属性不是来自原型链

虽然 `in` 运算符可以用于检查对象的属性，包括来自原型链的属性，但 `hasOwnProperty` 方法可以检查对象是否包含不来自原型链的属性。

在接下来的示例中，我们想知道 `myObject` 是否包含属性 `foo`，并且该属性不是从原型链继承的。为了实现这一点，我们询问 `myObject` 是否拥有它自己的名为 `foo` 的属性。

### 示例：sample41.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myObject = {foo: 'value'};

console.log(myObject.hasOwnProperty('foo')); // Logs true.

// 对比一个来自原型链的属性。

console.log(myObject.hasOwnProperty('toString')); // Logs false.

</script></body></html>
```

当你需要确定一个属性是对象局部的还是继承自原型链时，应该利用 `hasOwnProperty` 方法。

## 使用 in 运算符检查对象是否包含给定属性

`in` 运算符用于验证对象是否包含给定的属性（返回真或假）。在示例中，我们正在检查 `foo` 是否是 `myObject` 中的一个属性。

### 示例：sample42.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myObject = {foo: 'value'};

console.log('foo' in myObject); // Logs true.

</script></body></html>
```

你应该意识到，`in` 运算符不仅检查所引对象包含的属性，还检查对象通过原型链继承的任何属性。因此，相同的属性查找规则同样适用，如果当前对象中不存在，则将在原型链中搜索。

这意味着上一个示例中的 `myObject` 实际上通过原型链包含一个 `toString` 属性方法（`Object.prototype.toString`），即使我们没有指定过它（例如 `myObject.toString = 'foo'`）。

## 示例：sample43.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myObject = { foo: 'value' };

console.log('toString' in myObject); // Logs true.

</script></body></html>
```

在最后一个代码示例中，`toString` 属性并不是字面量上位于 `myObject` 对象内部。然而，它继承自 `Object.prototype`，因此 `in` 运算符得出结论：`myObject` 并没有继承 `toString()` 方法方法。

## 使用 for 循环遍历（循环）对象的属性

通过使用 `for...in`，我们可以遍历对象的每个属性。在下面的代码中，我们使用 `for...in` 获取对象中的属性名。

### 示例：sample44.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var cody = {

  age: 23,

  gender: 'male'

};

for (var key in cody) { // key 是表示每个属性的变量。

  // 避免从原型链继承的属性。

  if (cody.hasOwnProperty(key)) {

    console.log(key);

  }

}

</script></body></html>
```

## 注意事项

`for...in` 循环有一个缺点。它不仅会访问被遍历对象的属性，还会包含通过原型链循环继承的任何属性。因此，如果这不是我们想要的结果（通常情况下不是），我们必须在循环内部使用简单的语句来确保只访问特定对象包含的属性。这可以通过所有对象继承的 `hasOwnProperty()` 方法来实现。

循环中访问属性的顺序并不一定是它们定义的顺序。只有可枚举（即在遍历对象时可用）的属性才会出现在循环中。例如，`constructor` 属性就不会出现。可以使用 `propertyIsEnumerable` 方法检查哪些属性是枚举的。

## 宿对象和原生对象

你应该意识到，执行 JavaScript 环境（例如网页浏览器）通常包含宿对象。宿对象不是 ECMAScript 实现的一部分，但在执行期间可用。当然，宿对象的可用性完全取决于环境提供了什么。

例如，在网页浏览器中，`window` 对象及其包含的所有对象（排除 JavaScript ）都被视为宿对象。

在接下来的示例中，我检查了 `window` 对象的属性。

### 示例：sample45.html

```html
<!DOCTYPE html><html lang="en"><body><script>

for (x in window) {

    console.log(x); // 输出窗口的所有属性。

}

</script></body></html>
```

你可能已经注意到原生 JavaScript 对象没有列在宿对象列表中。浏览器通常区分宿对象和原生对象。

对于网页浏览器而言，大多数宿对象是处理 HTML 文档的接口，也称为 DOM。接下来的示例是列出浏览器环境提供的 `window.document` 对象内部包含的所有对象。

### 示例：sample46.html

```html
<!DOCTYPE html><html lang="en"><body><script>

for (x in window.document) {

    console.log();

}

</script></body></html>
```

我想让你在这里学习的是，JavaScript 规范并不关心宿对象，反之亦然。在 JavaScript 提供的（例如）之间存在一条分界线。

JavaScript 1.5, ECMA-262 第 3 版与 Mozilla 的 JavaScript 1.6, 1.7, 1.8, 1.8.1, 1.8.5 以及宿主环境提供的功能，它们不应被混淆。

## 注意

运行 JavaScript 代码的宿主环境（例如网页浏览器）通常提供头对象（例如网页浏览器中的 `window` 对象），语言的原生部分存储在其中，同时还有宿主对象（例如网页浏览器中的 `window.Location`）和用户定义对象（例如你编写并在网页浏览器中运行的代码）。

有时，网页浏览器制造商作为 JavaScript 解释器的宿主，会在规范被批准之前推送某个 JavaScript 版本或向 JavaScript 添加未来规范（例如 Mozilla Firefox 的 JavaScript 1.6, 1.7, 1.8, 1.8.1, 1.8.5）。

# 使用 Underscore.js 增强和扩展对象

在需要认真操作和管理对象时，JavaScript 1.5 显得捉襟见肘。如果你在网页浏览器中运行 JavaScript，我想大胆地建议，当你需要比 JavaScript 1.5 提供更多的功能时，使用 Underscore.js。Underscore.js 在处理对象时提供了这些功能。

这些函数适用于所有对象和数组：

- `each()`
- `map()`
- `reduce()`
- `reduceRight()`
- `detect()`
- `select()`
- `reject()`
- `all()`
- `any()`
- `include()`
- `invoke()`
- `pluck()`
- `max()`
- `min()`
- `sortBy()`
- `sortIndex()`
- `toArray()`
- `size()`

这些函数适用于所有对象：

- `keys()`
- `values()`
- `functions()`
- `extend()`
- `clone()`
- `tap()`
- `isEqual()`
- `isEmpty()`
- `isElement()`
- `isArray()`
- `isArguments()`
- `isFunction()`
- `isString()`
- `isNumber()`
- `isBoolean()`
- `isDate()`
- `isRegExp()`
- `isNaN()`
- `isNull()`
- `isUndefined()`

我喜欢这个库是因为它在浏览器支持时利用了 JavaScript 的新的原生特性，同时也为不支持这些浏览器提供了相同的功能，且除非万不得已否则修改 JavaScript 的原生实现。

## 注意

在开始使用 Underscore.js 之前，确保你所需的功能尚未被代码中可能使用的 JavaScript 库或框架提供。

# 第 3 章 String()

## 使用 String() 对象的概念概述

`String()` 构造函数用于创建字符串对象和字符串原始值。在接下来的示例中，我详细说明了 JavaScript 中字符串值的创建。

示例：sample47.html

```html
<!DOCTYPE html lang="en"><body><script>

// 使用 new 关键字和 String() 构造函数创建一个字符串对象。

var stringObject = new String('foo');

console.log(stringObject); // 输出 foo {0='f', 1 = 'o', 2 = 'o'}

console.log(typeof stringObject); // 输出 'object'。

// 直接使用 String 构造函数创建字符串字面量/原始值。

var stringObjectWithoutNewKeyword = String('foo'); // 没有 new 关键字。

console.log(stringObjectWithoutNewKeyword); // 输出 'foo'。

console.log(typeof stringObjectWithoutNewKeyword); // 输出 'string'。

// 创建字符串字面量/原始值（后台利用了构造函数）。

var stringLiteral = 'foo';

console.log(stringLiteral); // 输出 foo。

console.log(typeof stringLiteral); // 输出 'string'。

</script></body></html>
```

## String() 参数

`String()` 构造函数接受一个参数：正在被创建的字符串值。在接下来的示例中，我们创建了一个变量 `stringObject` 来包含字符串值 'foo'。

示例：sample48.html

```html
<!DOCTYPE html lang="en"><body><script>

// 创建字符串对象。

var stringObject = new String('foo');

console.log(stringObject); // 输出 foo {0="f", 1="o", 2="o"}

</script></body></html>
```

## 注意

当与 `new` 关键字配合时，`String()` 构造函数的实例会产生一个实际的复杂对象。你应该避免这样做（使用字面量/原始数字），因为存在与 `typeof` 运算符相关的潜在问题。`typeof` 运算符会将复杂的字符串对象报告为 'object'，而不是你预期的原始标签（'string'）。此外，字面量/原始值的编写速度更快且更简洁。

## String() 属性和方法

`String` 具有以下属性和方法（不包括继承的属性和方法）：

属性（例如 `String.prototype`）：

- `prototype`

方法（例如 `String.fromCharCode()`）：

- `fromCharCode()`

## String 对象实例属性和方法

String 对象实例具有以下属性和方法（不包括继承的属性和方法）：

实例属性（例如 `var myString = 'foo'; myString.length`）：

- `constructor`
- `length`

实例方法（例如 `var myString = 'foo'; myString.toLowerCase()`）：

- `charAt()`
- `charCodeAt()`
- `concat()`
- `indexOf()`
- `lastIndexOf()`
- `localeCompare()`
- `match()`
- `quote()`
- `replace()`
- `search()`
- `slice()`
- `split()`
- `substring()`
- `toLocaleLowerCase()`
- `toLocaleUpperCase()`
- `toLowerCase()`
- `toUpperCase()`

# 第 4 章 Number()

## 使用 Number() 对象的概念概述

`Number()` 构造函数用于创建数值对象和数值原始。在接下来的示例中，我详细说明了 JavaScript 中数值的创建。

示例：sample49.html

```html
<!DOCTYPE html lang="en"><body><script>

// 使用 new 关键字和 Number() 构造函数创建一个数值对象。

var numberObject = new Number(1);

console.log(numberObject); // 输出 1。

console.log(typeof numberObject); // 输出 'object'。

// 不使用 new 关键字创建字面量/原始值。

var numberObjectWithoutNew = Number(1);

console.log(numberObjectWithoutNew); // 输出 1。

console.log(typeof numberObjectWithoutNew); // 输出 'number'。

// 创建字面量/原始值（后台利用了构造函数）。

var numberLiteral = 1;

console.log(numberLiteral); // 输出 1。

console.log(typeof numberLiteral); // 输出 'number'。

</script></body></html>
```

## 整数和浮点数

JavaScript 中的数字通常以整数或浮点值的形式写入。在接下来的代码中，我创建了原始整数和原始浮点数。

示例：sample50.html

```html
<!DOCTYPE html lang="en"><body><script>
var integer = 1232134;
console.log(integer); // 输出 '1232134'。

var floatingPoint = 2.132;
console.log(floatingPoint); // 输出 '2.132'。
</script></body></html>
```

## 注意

数值在 JavaScript 中可以是十六进制值或八进制值，但通常是这样做的。

## Number() 参数

`Number()` 构造函数接受一个参数：正在被创建的数值。通过接下来的代码，我们为值 456 创建了一个数值对象。

示例：sample51.html

```html
<!DOCTYPE html lang="en"><body><script>
var numberOne = new Number(456);
console.log(numberOne); // 输出 '456'。
</script></body></html>
```

## 注意

当与 `new` 关键字配合时，`Number()` 构造函数的实例产生一个对象。你应该避免使用 `Number()` 构造函数创建数值（使用字面量/原始数字），因为存在与 `typeof` 运算符相关的潜在问题。`typeof` 运算符会将数值对象报告为 'object'，而不是你预期的原始标签（'number'）。字面量值更加简洁。

## Number() 属性

`Number()` 对象具有以下属性：

属性（例如 `Number.prototype`）：

- `MAX_VALUE`
- `MIN_VALUE`
- `NaN`
- `NEGATIVE_INFINITY`
- `POSITIVE_INFINITY`
- `prototype`

## Number 对象实例属性和方法

Number 对象实例具有以下属性和方法（不包括继承的属性和方法）：

实例属性：

- `constructor`

实例方法（例如 `var myNumber = 1.00324; myNumber.toFixed()`）：

- `toExponential()`
- `toFixed()`
- `toLocaleString()`
- `toPrecision()`
- `toString()`
- `valueOf()`

# 第 5 章 Boolean()

## 使用 Boolean() 对象的概念概述

`Boolean()` 构造函数可以用于创建 Boolean 对象，以及表示真（true）或假（false）值的 Boolean 原生值。

在下面的代码中，我详细介绍了 JavaScript 中 Boolean 值的创建。

示例：sample52.html

```html
<!DOCTYPE html><html lang="en"><body><script>
  // 使用 new 关键字和 Boolean 构造函数创建 Boolean 对象。
  var myBoolean1 = new Boolean(false); // 使用 new 关键字。
  console.log(typeof myBoolean1); // 输出 'object'

  // 直接使用数字构造函数而不使用 new 创建字面量/原生值。
  var myBoolean2 = Boolean(0); // 未使用 new 关键字。
  console.log(typeof myBoolean2); // 输出 'boolean'

  // 创建 Boolean 字面量/原生值（底层利用构造函数）。
  var myBoolean3 = false;
  console.log(typeof myBoolean3); // 输出 'boolean'.
  console.log(myBoolean1, myBoolean2, myBoolean3); // 输出 false false false
</script></body></html>
```

## Boolean() 参数

`Boolean()` 构造函数接受一个参数并转换为 Boolean 值（即 true 或 false）。任何不是 0、null、false、NaN、undefined 或空字符串 ("") 的有效 JavaScript 都会被转换为 true。在接下来的示例中，我们创建了两个 Boolean 对象：一个真一个假。

示例：sample53.html

```html
<!DOCTYPE html><html lang="en"><body><script>
  // 传递给 Boolean() 的参数 = 0 = false，因此 foo = false
  var foo = new Boolean(0)
  console.log(foo);

  // 传递给 Boolean() 的参数 = Math = true，因此 bar = true
  var bar = new Boolean(Math)
  console.log(bar);

</script></body></html>
```

## 注意

与 `new` 关键字配合使用时，来自 `Boolean()` 构造函数的实例会产生一个实际复杂对象。由于 `typeof` 运算符相关的问题，你应该避免使用 `Boolean()` 构造函数创建 Boolean 值（应使用字面量/原生数字）。`typeof` 运算符将 Boolean 对象报告为 'object'，而不是你可能期望的标签（'boolean'）。此外，字面量/原生值的编写速度更快。

## Boolean() 属性和方法

`Boolean()` 对象具有以下属性：

属性（例如，`Boolean.prototype`）：

- `prototype`

## Boolean 实例属性和方法

Boolean 对象实例具有以下属性和方法（不包括继承的属性和方法）：

实例属性（例如 `var myBoolean = false; Boolean.constructor`）：

- `constructor`

实例方法（例如 `var myNumber = false; Boolean.toString()`）：

- `toString()`
- `valueOf()`

## 非原生的假 Boolean 对象会转换为真

从 `Boolean()` 构造函数创建的 Boolean 对象（与原生值相反）是一个对象，而对象会转换为 true。当通过 `Boolean()` 构造函数创建假的 Boolean 对象时，值本身会转换为 true。在接下来的示例中，我演示了假的 Boolean 对象始终是“真值”（truthy）。

示例：sample54.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var falseValue = new Boolean(false);

console.log(falseValue); // 我们有一个假的 Boolean 对象，但对象是真值的。

if (falseValue) { // Boolean 对象，即使是 Boolean 对象，也是真值的。
    console.log('falseValue is truthy');
}
</script></body></html>
```

如果你需要将非 Boolean 值转换为 Boolean，只需使用不带 `new` 关键字的 `Boolean()` 构造函数，返回的值将是值而不是 Boolean 对象。

## 某些值为假的，其他都是真的

之前已经提到过，但值得再次提到，因为涉及到转换：如果一个值为 `0, null, false, NaN, undefined 或空字符串("")`，它就是 `false`。JavaScript 中除上述值之外的任何值在 Boolean 上下文中（例如 `if (true);`）都会被转换为 `true`。

示例：sample55.html

```html
<!DOCTYPE html><html lang="en"><body><script>
// 所有这些都返回假的 Boolean 值。
console.log(Boolean(0));
console.log(Boolean(-0));
console.log(Boolean(null));
console.log(Boolean(false));
console.log(Boolean(''));
console.log(Boolean(undefined));
console.log(Boolean(null));

// 所有这些都返回真的 Boolean 值。
console.log(Boolean(1789));
console.log(Boolean('false')); // 字符串 'false' 并不是假的 Boolean 值。
console.log(Boolean(Math));
console.log(Boolean(Array));
</script></body></html>
```

理解哪些 JavaScript 值会被还原为 `false` 是至关重要的，这样你就能知道所有其他值都被视为 `true`。

# 第 6 章 与原生字符串、数字和 Boolean 值的操作

## 当访问属性时，原生/字面量值会被转换为对象

不要被字符串、数字和 Boolean 字面量可以像带有属性的对象一样处理（例如 `true.toString()`）这一事实所误导。当这些原生值通过尝试访问其属性被当作对象处理时，JavaScript 将创建一个包装对象。包装对象的属性可以被访问，然后包装对象会被丢弃。原生值被转换为对象，以便被解释为对象。

### String

示例：sample56.html

```html
<!DOCTYPE html><html lang="en"><body><script>
// 被当作对象处理的 String。
var stringObject = new String('foo');
console.log(stringObject.length); // 输出 3
console.log(stringObject['length']); // 输出 3

// 被当作对象处理的 String 字面量/原生值。
var stringLiteral = 'foo';
console.log(stringLiteral.length); // 输出 3
console.log(stringLiteral['length']); // 输出 3.
console.log('bar'.length); // 输出 3
console.log('bar'['length']); // 输出 3.

</script></body></html>
```

### Number

示例：sample57.html

```html
<!DOCTYPE html><html lang="en"><body><script>
// 被当作对象处理的 Number 对象。
var numberObject = new Number(1.1023);
console.log(numberObject.toFixed()); // 输出 1.
console.log(numberObject['toFixed']()); // 输出 1.

// 被当作对象处理的 Number 字面量/原生值。
var numberLiteral = 1.1023;
console.log(numberLiteral.toFixed()); // 输出 1.
console.log(numberLiteral['toFixed']()); // 输出 1.
console.log((1234).toString()); // 输出 '1234'.
console.log(1234['toString']()); // 输出 '1234'.
</script></body></html>
```

### Boolean

示例：sample58.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 被当作对象处理的 Boolean 对象。

var booleanObject = new Boolean();

console.log(booleanObject.toString()); // 输出 'false'.

console.log(booleanObject['toString']()); // 输出 'false'.

// 被当作对象处理的 Boolean 字面量/原生值。

var booleanLiteral = false;

console.log(booleanLiteral.toString()); // 输出 'false'.

console.log(booleanLiteral['toString']()); // 输出 'false'.

console.log((true).toString()); // 输出 'true'.

console.log(true['toString']()); // 输出 'true'.

</script></body></html>
```

## 注意

当直接在原生值上（未存储在变量中）访问属性时，必须先求值数字，然后该值才会被视为对象（例如 `(1).toString();` 或 `1..toString();`）。为什么是两个点？第一个点被视为数字的小数，而不是访问对象属性的运算符。

## 你通常应该使用原生字符串、数字和 Boolean 值

表示字符串、数字或 Boolean 的字面量/原生值编写更快，并且在字面量形式下更简洁。

由于此原因，你应该使用字面量值。此外，`typeof` 运算符的准确性取决于你如何创建该值（字面量还是构造函数调用）。如果你创建一个字符串、数字或 Boolean 对象，`typeof` 运算符会报告该类型为对象。如果你使用字面量，`typeof` 运算符将返回实际值类型的字符串名称（例如 `typeof 'foo' // 返回 'string'`）。

我将在下面的代码中演示了这一事实。

## 示例：sample59.html

```html
<!DOCTYPE html lang="en"><body><script>

  // String, number, and Boolean objects.

  console.log(typeof new String('foo')); // Logs 'object'.

  console.log(typeof new Number(1)); // Logs 'object'.

  console.log(typeof new Boolean(true)); // Logs 'object'.

  // String, number, and Boolean literals/primitives.

  console.log(typeof 'foo'); // Logs 'string'.

  console.log(typeof 1); // Logs 'number'.

  console.log(typeof true); // Logs 'boolean'.

</script></body></html>
```

如果你的程序依赖 `typeof` 运算符来识别基于原始类型的字符串、数字或 Boolean 值，你应该避免使用 `String`、`Number` 和 `Boolean` 构造函数。

# 第 7 章 Null

## 使用 null 值的概念概述

你可以使用 `null` 来显式地表示对象属性不包含值。通常情况下，如果一个属性被设置为包含一个值，但由于某些原因该值不可用，应该使用值 `null` 来指示该引用属性为空值。

示例：sample60.html

```html
<!DOCTYPE html><html lang="en"><body><script>

 // The property foo is waiting for a value, so we set its initial value
//to null.

  var myObject = { foo: null };

  console.log(myObject.foo); // Logs 'null'

</script></body></html>
```

## 注意事项

不要将 `null` 与 `undefined` 混淆。JavaScript 使用 `undefined` 来告诉你某些内容缺失。提供 `null` 是为了让你判断何时预期某个值但其尚未可用。

## typeof 将 null 值返回 "object"

对于值为 `null` 的变量，`typeof` 运算符返回 `'object'`。如果你需要验证一个 `null` 值，理想的解决方案是检查值是否等于 `null`。在这个示例中，我们使用 `===` 运算符来专门验证我们正在处理一个 `null` 值。

示例：sample61.html

```html
<!DOCTYPE html><html lang="en"><body><script>

  var myObject = null;

  console.log(typeof myObject); // Logs 'object', not exactly helpful.

  console.log(myObject === null); // Logs true, only for a real null value.

</script></body></html>
```

## 注意事项

在验证 `null` 值时，始终使用 `===`；`==` 不区分 `null` 和 `undefined`。

# 第 8 章 Undefined

## undefined 值的概念概述

JavaScript 以两种略有不同的方式使用 `undefined`。

第一种用法是表示声明的变量（例如 `var foo`）没有被赋值。第二种用法是表示你尝试访问的对象属性未定义（即它甚至没有命名），并且在原型链中未找到。

在随后的示例中，我检查了 JavaScript 对 `undefined` 的两种用法。

示例：sample62.html

```html
<!DOCTYPE html><html lang="en"><body><script>

  var initializedVariable; // Declare variable.

  console.log(initializedVariable); // Logs undefined.

  console.log(typeof initializedVariable); // Confirm that JavaScript
  // returns undefined.

  var foo = {};

  console.log(foo.bar); // Logs undefined, no bar property in foo object.

  console.log(typeof foo.bar); // Confirm that JavaScript returns
  // undefined;

</script></body></html>
```

## 注意事项

让 JavaScript 独立使用 `undefined` 被认为良好的做法。你不应该发现自己在给 `undefined` 赋值，例如 `foo = undefined`。相反，如果你正在指定某个属性或值不可用，应该使用 `null`。

## JavaScript ECMA-262 第 3 版及更高版本在全局作用域声明 undefined 变量

与之前的版本不同，JavaScript ECMA-262 第 3 版及更高版本在全局作用域声明了一个名为 `undefined` 的全局变量。由于该变量被声明但未赋值，因此该 `undefined` 变量是 `undefined`。

示例：sample63.html

```html
<!DOCTYPE html><html lang="en"><body><script>

  // Confirm that undefined is a property of the global scope.

  console.log(undefined in this); // Logs true.

</script></body></html>
```

# 第 9 章 头对象/全局对象

## 头对象的概念概述

JavaScript 本身必须包含在一个对象中。例如，在为浏览器环境编写 JavaScript 代码时，JavaScript 被包含并执行在 `window` 对象中。这个 `window` 对象被认为是“头对象”（head object），有时也被混淆地称为“全局对象”。所有 JavaScript 的实现都要求使用单个头对象。

头对象是由 JavaScript 在启用之前设置的，用于存放与 JavaScript 重新封装的原生代码。用户定义的代码由 JavaScript 放置在头对象内部进行执行。让我们在 Web 浏览器方面验证这一点。

示例：sample64.html

```html
<!DOCTYPE html><html lang="en"><body><script>

  var myObject = { foo: 'bar' };

  console.log(window.myObject === myObject); // Logs true.

  console.log(this.myObject === myObject); // Logs true.

</script></body></html>
```

## 头对象是隐含的，通常不被显式引用

通常不使用头对象（head object）引用，因为它是隐含的。例如，在浏览器环境中 `window.alert` 和 `alert()` 本质上是同一个语句。JavaScript 会填充空白处。因为 `window` 对象（即头对象）是作用链中查找某个值时创建的最后一个对象，所以 `window` 对象本质上总是隐含的。在下一个示例中，我们利用了全局作用域中的 `alert()` 函数。

示例：sample65.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var foo = { // window 在这里是隐含的，window.foo
  fooMethod: function () {
    alert('foo' + 'bar'); // window 在这里是隐含的，window.alert
    window.alert('foo' + 'bar'); // 使用了 window，效果相同。
  }
};

foo.fooMethod(); // window 在这里是隐含的，window.foo.fooMethod()

</script></body></html>
```

确保你理解即使你不包含头对象，它也是隐含的，因为头对象是作用链中的最后一个终点。

## 注意

显式使用（例如 `window.alert()` 与 `alert()` 相比）在性能方面（代码运行速度）会增加一点开销。如果你仅依赖作用链并避免显式引用头对象（即使你知道你想要的属性包含在全局作用域中），速度会更快。

# 第 10 章 Object()

## Object() 对象的概念概述

使用内置的 `Object()` 构造函数可以动态创建通用的空对象。事实上，如果你回想起第 1 章的开头，这正是我们创建 `cody` 对象时所做的事情。让我们重新创建 `cody` 对象。

示例：sample66.html

```html
<!DOCTYPE html><html lang="en"><body><script>

  var cody = new Object(); // 创建一个没有属性的空对象。

  for (key in cody) { // 确认 cody 是一个空通用对象。

    if (cody.hasOwnProperty(key)) {

      console.log(key); // 不应该看到任何日志，因为 cody 本身没有属性。

    }

  }

</script></body></html>
```

在这里，我们只是使用 `Object()` 构造函数创建一个名为 `cody` 的通用对象。你可以将 `Object()` 构造函数想象成饼干模具，用于创建没有预定义属性或方法的空对象（当然，除了从原型链继承的那些）。

## 注意

如果还不显而易见，`Object()` 构造函数本身是一个对象。也就是说，该构造函数是基于从 `Function` 构造函数创建的对象。`Object` 构造函数只是输出空白对象。是的，你可以创建任何你喜欢的对象。然而，创建一个像 `cody` 这样的空对象与创建一个带有预定义属性的自定义构造函数是完全不同的。确保你理解 `cody` 只是一个基于 `Object()` 构造函数的空对象。为了充分利用 JavaScript 的力量，你不仅需要学习如何从 `Object()` 创建空对象，还需要学习如何像 `Object()` 构造函数一样构建自己的对象“类”（例如 `Person()`）。

## Object() 参数

`Object()` 构造函数接受一个可选参数。该参数是你想要创建的值。如果你不提供任何参数，将假设为 `null` 或 `undefined` 值。

## 示例：sample67.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 创建一个没有属性的空对象。

  var cody1 = new Object();

  var cody2 = new Object(undefined);

  var cody3 = new Object(null);

  console.log(typeof cody1, typeof cody2, typeof cody3); // 记录 'object object object'。

</script></body></html>
```

如果将 `null` 或 `undefined` 值传递给 `Object` 构造函数，将得到一个空对象。理论上，我们可以使用对象字面量来创建对象，即使是隐含的。

示例：sample68.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 使用对象字面量来创建 cody 对象。

var cody = {

  living: true,

  age: 23,

  gender: 'male',

  getGender: function () { return cody.gender; }

};

// 注意这里的 cody 对象。

console.log(cody); // 记录 cody 对象。

</script></body></html>
```

## Object() 属性和方法

`Object()` 构造函数具有以下属性和方法（包括继承的属性和方法）：

属性（例如 `Object.prototype`）：

- `prototype`

方法（例如 `Object.create()`）：

- `create()`
- `defineProperty()`
- `defineProperties()`
- `getOwnPropertyDescriptor()`
- `getOwnPropertyNames()`
- `getPrototypeOf()`
- `keys()`
- `preventExtensions()`
- `isExtensible()`
- `seal()`
- `isSealed()`
- `freeze()`
- `isFrozen()`

## Object 对象实例属性和方法

`Object()` 实例具有以下属性和方法（不包括继承的属性和方法）：

- `constructor`
- `hasOwnProperty()`
- `isPrototypeOf()`
- `propertyIsEnumerable()`
- `toString()`
- `toLocaleString()`
- `valueOf()`

## 使用对象字面量创建对象

通过对象字面量创建对象，即使是隐含的，也是更简洁的。

示例：sample69.html

```html
<!DOCTYPE html><html lang="en"><body><script>

  var cody = {

    living: true,

    age: 23,

    gender: 'male',

    getGender: function () { return cody.gender; }

  };

  // 注意这里的 cody 对象。

  console.log(cody); // 记录 cody 对象。

</script></body></html>
```

示例：sample70.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var cody = {

  living: true,

  age: 23,

  gender: 'male',

  getGender: function () { return cody.gender; }

};

// 注意最后一个属性没有逗号。

console.log(cody); // 记录 cody 对象。

</script></body></html>
```

示例：sample71.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var cody = {

  'living': true,

  'age': 23,

  'gender': 'male',

  getGender: function () { return cody.gender; }

};

// 注意最后一个属性没有逗号。

console.log(cody); // 记录 cody 对象。

</script></body></html>
```

## 所有对象都继承自 Object.prototype

JavaScript 中的 `Object()` 构造函数是特殊的，因为 `prototype` 属性是原型链的最后一个终点。

在下面的示例中，我为 `Object.prototype` 增加了一个 `foo` 属性，然后创建了一个字符串并尝试访问该字符串的 `foo` 属性。由于 `myString` 实例没有 `foo` 属性，原型链开始工作并在 `String.prototype` 中查找。那里没有，下一个查找的地方是 `Object.prototype`，这是 JavaScript 查找对象值的最终位置。`foo` 值找到了，因为我添加了它，然后它返回了 `foo` 的值。

示例：sample72.html

```html
<!DOCTYPE html><html lang="en"><body><script>

  Object.prototype.foo = 'foo';

  var myString = 'bar';

  // 记录 'foo'，通过原型链在 Object.prototype.foo 找到。

  console.log(myString.foo);

</script></body></html>
```

# 第 11 章 Function()

## 使用 Function() 对象的概念概述

函数是代码语句的容器，可以通过括号 `()` 运算符进行调用。在调用时，可以在括号内传递参数，这样函数中的语句在执行时就可以访问某些值。

在接下来的代码中，我们创建了两个版本的 `addNumbers` 函数对象——一个使用 `new` 运算符，另一个是更常见的字面量模式。两者都期望接收两个参数。在每种情况下，我们都通过括号 `()` 运算符传递参数并调用该函数。

示例：sample73.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

var addNumbersA = new Function('num1', 'num2', 'return num1 + num2');

console.log(addNumbersA(2, 2)); // 打印 4.

// 也可以用字面量方式编写，这常见得多。

var addNumbersB = function(num1, num2) { return num1 + num2; };

console.log(addNumbersB(2, 2)); // 打印 4.

</script>
</body>
</html>
```

函数可以用于返回一个值、一个对象，或者作为运行代码的机制。JavaScript 中的函数有多种用途，但在最基本的形式，函数仅仅是一个可执行语句的唯一域。

## Function() 参数

`Function()` 构造函数接受无限数量的参数，但 `Function()` 构造函数期望的最后一个参数是一个字符串，包含了组成函数体的语句。在最后一个参数之前传递给构造函数的任何参数对所创建的函数可用。也可以以逗号分隔字符串的形式发送多个参数。

在接下来的代码中，我对比了 `Function()` 构造函数的用法与实例化函数对象的更常用模式。

示例：sample74.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

var addFunction = new Function('num1', 'num2', 'return num1 + num2');

/* 或者，一个包含参数的逗号分隔的单个字符串可以作为
构造函数的第一个参数，后面紧跟函数体。 */

var timesFunction = new Function('num1,num2', 'return num1 * num2');

console.log(addFunction(2, 2), timesFunction(2, 2)); // 打印 '4 4'

// 与实例化函数的更常用模式对比：

var addFunction = function (num1, num2) { return num1 + num2; }; // 表达式形式。

function addFunction(num1, num2) { return num1 + num2; } // 语句形式。

</script>
</body>
</html>
```

## 注意事项

不建议直接利用 `Function()` 构造函数，通常也不会这样做，因为 JavaScript 将使用 `eval()` 来解析构建函数逻辑的字符串。许多人认为 `eval()` 是不必要的开销。如果使用了它，代码设计中可能存在缺陷。

不带 `new` 关键字使用 `Function()` 构造函数的效果与仅使用构造函数创建对象相同（例如 `new Function('x','return x')` 与 `Function('x','return x')`）。

直接调用 `Function()` 构造函数时不会创建闭包（见第 7 章）。

## Function() 属性和方法

函数对象拥有以下属性（包括继承的属性和方法）：

属性（例如 `Function.prototype`）：

- `prototype`

## 函数对象实例属性和方法

函数对象实例拥有以下属性和方法（包括继承的属性和方法）：

实例属性（例如 `var myFunction = function(x, y, z){}; myFunction.length;`）：

- `arguments`
- `constructor`
- `length`

实例方法（例如 `var myFunction = function(x, y, z) {}; myFunction.toString());`）：

- `apply()`
- `call()`
- `toString()`

## 函数总是返回一个值

虽然可以仅仅为了执行代码语句而创建一个函数，但函数返回一个值也很常见。在接下来的示例中，我们从 `sayHi` 函数返回了一个字符串。

示例：sample75.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

  var sayHi = function () {
    return 'Hi';
  };

  console.log(sayHi()); // 打印 "Hi"

</script>
</body>
</html>
```

如果函数没有返回值，则返回 `undefined`。在接下来的示例中，我们调用了 `yelp` 函数，它向控制台打印了字符串 'yelp'，而没有显式返回一个值。

示例：sample76.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

  var yelp = function () {
    console.log('I am yelping!');
    // 即使我们不返回，函数也会返回 undefined。
  };

  /* 打印 true 因为总是返回一个值，即使我们没有特别指定返回一个。 */
  console.log(yelp() === undefined);

</script>
</body>
</html>
```

这里需要掌握的概念是，所有函数都会返回一个值，即使你没有显式地提供要返回的值。如果你没有指定返回的值，返回的值就是 `undefined`。

## 函数是一等公民（不仅是语法，而且是值）

在 JavaScript 中，函数是对象。这意味着函数可以存储在变量、数组或对象中。此外，函数可以传递给函数并从函数返回。函数拥有属性，因为它是一个对象。这些因素使得函数成为 JavaScript 中的一等公民。

示例：sample77.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

var funcA = function () {};

var funcE = function () {};

funcE.answer = 'yup'; // 实例属性。

console.log(funcE.answer); // 'yup'

</script>
</body>
</html>
```

## 向函数传递参数

参数是在函数调用时将值传递到作用域的媒介。在接下来的示例中，我们预定义它接收两个参数，这两个值在它的作用域内是可用的。

示例：sample78.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

var addFunction = function (number1, number2) {
  var sum = number1 + number2;
  return sum;
}

console.log(addFunction(3, 3)); // 打印 6.

</script>
</body>
</html>
```

## 注意事项

与其他编程语言相比，在 JavaScript 中定义函数时省略参数是完全合法的。缺失的参数会被赋予 `undefined` 值。当然，通过省略参数值，函数可能无法正常工作。

如果你传递了意外的参数（创建函数时未定义的），不会发生错误。你可以通过 `arguments` 访问这些参数，`arguments` 对所有函数都可用。

## this 和 arguments 值对所有函数可用

在所有函数的作用域体内部，`arguments` 对象是一个类数组对象，包含了传递给函数的参数。在接下来的代码中，尽管我们在定义函数时没有指定参数，但我们可以依靠调用时传递的参数来访问它们。

示例：sample79.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

var add = function () {
  return arguments[0] + arguments[1];
}

console.log(add(4, 4)); // 返回 8.

</script>
</body>
</html>
```

`this` 关键字传递给所有函数，它是包含函数的对象的引用。正如你预期的，作为对象属性的函数（即方法）可以使用 `this` 来获取父对象的引用。当函数在全局作用域中定义时，`this` 的值是全局对象。查看以下代码并确保你理解它返回了什么。

示例：sample80.html

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>

var myObject1 = {
  name: 'myObject1',
  myMethod: function () { console.log(this); };
}

myObject1.myMethod(); // Logs 'myObject1'.

var myObject2 = function () { console.log(this); };

myObject2(); // Logs window.

</script>
</body>
</html>
```

## arguments.callee 属性

`arguments` 对象有一个名为 `callee` 的属性，它是对当前执行的函数的引用。该属性可以在函数作用域内引用该函数（例如 `arguments.callee`）——这是一个自引用。在下文中，我们使用该属性来获取调用函数的引用。

示例：sample81.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var foo = function () {
  console.log(arguments.callee); // Logs foo
  // callee 可以用于递归地调用 foo 函数（例如 arguments.callee()）
}

</script></body></html>
```

当函数需要递归调用时，这非常有用。

## 实例 length 属性与 arguments.length

`arguments` 对象有一个唯一的 `length` 属性。虽然你可能认为这个 `length` 属性给出定义的参数的数量，但它实际上给出调用期间传递给函数的参数数量。

示例：sample82.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myFunction = function (z, s, d) {
  return arguments.length;
}

console.log(myFunction()); // Logs 0 因为没有向函数传递任何参数。

</script></body></html>
```

通过所有 `Function` 实例的 `length` 属性，我们实际上可以获取函数期望参数的总数。

示例：sample83.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myFunction = function (z, s, d, e, r, m, q) {
  return myFunction.length;
};

  console.log(myFunction()); // Logs 7.

</script></body></html>
```

## 注意事项

`arguments.callee` 属性在严格模式下被弃用，可以从函数对象的 `length` 属性访问到函数的参数数量。今后，你可以利用 `callee` 属性首先获取对被调用函数的引用（即 `arguments.callee.length`），来获取长度值。

## 重新定义函数参数

可以在函数内部重新定义参数，也可以通过使用 `arguments` 数组来实现。看这里：

示例：sample84.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var foo = false;
var bar = false;

var myFunction = function (foo, bar) {
  arguments[0] = true;
  bar = true;
  console.log(arguments[0], bar); // Logs true true.
}

myFunction();

</script></body></html>
```

注意，我可以使用 `arguments` 索引或直接为参数重新赋值新值来重新定义 `bar` 参数的值。

## 在函数完成前返回（即取消函数执行）

在调用期间，可以随时使用带值或不带值的 `return` 关键字来取消函数。在接下来的示例中，如果参数未定义或不是数字，我们将取消 `add` 函数。

示例：sample85.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var add = function(x, y) {
  // 如果参数不是数字，则返回错误。
  if (typeof x != 'number' || typeof y != 'number') { return 'pass in numbers'; }
  return x + y;
}

console.log(add(3, 3)); // Logs 6.
console.log(add('2', '2')); // Logs 'pass in numbers'.

</script></body></html>
```

这里的概念是，你可以在函数执行的任何点使用 `return` 关键字来取消函数的执行。

## 定义函数（语句、表达式或构造函数）

函数可以通过三种不同的方式定义：函数构造函数、函数语句或函数表达式。在下面的示例中，我演示了每种变化。

示例：sample86.html

```html
<!DOCTYPE html><html lang="en"><body><script>

/* 函数构造函数：最后一个参数是函数逻辑，
所有内容都是参数。 */
var addConstructor = new Function('x', 'y', 'return x + y');

// 函数语句。
function addStatement(x, y) {
  return x + y;
}

// 函数表达式。
var addExpression = function (x, y) {
  return x + y;
}

console.log(addConstructor(2, 2), addStatement(2, 2), addExpression(2, 2)); // Logs '4 4 4'.

</script></body></html>
```

## 注意事项

有人说存在第四种函数定义类型，称为“命名函数表达式”。命名函数表达式仅仅是包含名称的函数表达式（例如 `var add = function add(x, y) {return x+y}`）。

## 调用函数（函数、方法、构造函数或构造函数）

函数通过不同的场景进行调用：
- 作为函数
- 作为方法
- 作为构造函数
- 使用 `apply()`

在接下来的示例中，我们检查了这些的每种情况。

示例：sample87.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 函数模式。
// 方法模式。
// 构造函数模式。
// 使用 apply().

</script></body></html>
```

## 匿名函数

匿名函数是没有标识符的函数。匿名函数主要用于传递函数。

示例：sample88.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 匿名函数，但没有调用方法。

var sayHi = function (f) {
  f(); // 调用匿名函数。
}

sayHi(function () { console.log('hi'); }); // Logs 'hi'.

</script></body></html>
```

## 自执行函数表达式

函数表达式（实际上任何不是通过 `Function()` 构造函数创建的函数）可以在定义后使用括号运算符立即调用。在接下来的示例中，我们创建了一个 `sayWord` 函数表达式并立即调用该函数。这被认为是自执行函数。

示例：sample89.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var sayWord = function () { console.log('Word 2 mo!'); }(); // Logs 'Word 2 mo!'

</script></body></html>
```

## 自执行匿名函数语句

可以创建一个自执行的匿名函数语句。这被称为自执行匿名。在接下来的示例中，我们创建了多个立即执行的匿名函数。

示例：sample90.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 在野外最常用/看到的。

(function(msg) {
    console.log(msg);
})('Hi');

// 略有不同，但实现了相同的结果；
(function(msg) {
    console.log(msg);
}) ('Hi');

// 最短的解决方案。
!function sayHi(msg) { console.log(msg); } ('Hi');

// 提示，这不起作用！
// function sayHi() {console.log('hi');};

</script></body></html>
```

## 注意事项

根据 ECMAScript 标准，如果要立即调用函数，则函数周围（或将函数转换为表达式的任何内容）的括号是必须的。

# 函数可以嵌套

函数可以无限地嵌套在其他函数内部。在下面的代码示例中，我们将 `foo` 函数封装在 `bar` 函数内部，而 `bar` 函数又在 `foo` 函数内部。

示例：sample91.html

```html
<!DOCTYPE html><html lang="en"><body><script>

function foo() {
  function bar() {
    console.log('bar');
  }
  bar();
}
foo();

</script></body></html>
```



<!DOCTYPE html><html lang="en"><body><script>

var foo = function () {

  var bar = function () {

    var goo = function () {

      console.log(this); // 记录头 对象的引用。

    }

  }

}();

</script></body></html>

这里的简单概念是函数是可以嵌套的，且嵌套深度没有限制。

## 注意

请记住，在 JavaScript 1.5、ECMA-262 第 3 版中，嵌套函数的 `this` 值将是头对象（例如 浏览器中的 `window` 对象）。

# 将函数传递给函数并从函数返回函数

如前所述，函数是 JavaScript 中的一等公民。由于函数是一个值，因此函数可以接收任何类型的值，函数可以传递给另一个函数。接收和/或返回其他函数的被称为“高阶函数”。

在下面的代码中，我们向 `foo` 函数传递了一个匿名函数，然后立即将其从 `foo` 函数中返回。`var bar` 指向的就是这个匿名函数，因此 `foo` 接收并返回了该匿名函数。

示例：sample95.html

```html
<!DOCTYPE html><html lang="en"><body><script>

// 函数可以发送给函数，也可以从函数返回。

var foo = function (f) {

  return f;

}

var bar = foo(function () { console.log('Hi'); });

bar(); // 记录 'Hi'.

</script></body></html>
```

所以，当 `bar` 被调用时，它调用了传递给 `foo()` 函数的匿名函数，该匿名函数随后从 `foo()` 函数返回并被 `bar` 变量引用。这也是为了展示函数可以像任何其他值一样被到处传递。

# 在函数定义之前调用函数语句（又名函数提升）

函数语句可以在执行过程中在其实际定义之前被调用。这有点奇怪，但你应该意识到这一点，以便利用它，或者至少在遇到它时知道发生了什么。在下面的示例中，我在定义 `sayYo()` 和 `sum()` 函数语句之前调用了它们。

**sample96.html**

```html
<!DOCTYPE html lang="en"><body><script>

// 示例 1

var speak = function () {

  sayYo(); // sayYo() 尚未被定义，但仍然可以被

  调用，记录 'Yo'。

  function sayYo(){ console.log('Yo'); }

}; // 调用

// 示例 2

console.log(sum(2, 2)); // 调用 sum(),它尚未定义，但

仍然可以被调用。

function sum(x, y) { return x + y; }

</script></body></html>
```

这发生在代码运行之前，函数语句会被解释并添加到执行栈/上下文中。在在使用函数语句时，请确保你了解这一点。

## 注意

定义为函数表达式的函数不会被提升。只有函数语句会被提升。

# 函数可以调用自己（又名递归）

函数调用它本身是完全合法的。这通常用于著名的代码模式。在接下来的代码中，我们启动了 `countDownFrom` 函数，然后它通过函数名 `countDownFrom` 调用自己。本质上讲，这创建了一个从 5 数到 0 的循环。

# 示例：sample97.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var countDown = function countDownFrom(num) {

  console.log(num);

  num--; // 修改参数值。

  if (num < 0) { return false; } // 如果 num < 0 则返回没有递归的函数。

  // 如果是匿名函数，也可以使用 arguments.callee(num);

  countDownFrom(num);

}

countDownFrom(5); // 启动函数，它分别记录 5, 4, 3, 2, 1, 0。

</script>

```

你应该意识到，函数调用自己（又名递归）或重复地这样做是自然的。

# 第 12 章 this 关键字

## this 的概念性概述以及它是如何引用的

当一个函数被创建时，会创建一个名为 `this` 的关键字（在后台），它链接到函数操作时所在的对象对象。换句话说，`this` 在其函数的作用范围内是可用的，但它是对该函数作为属性或方法的对象的引用。
让我们看看第 1 章中的 `cody` 对象：

示例：98.html

```html
<!DOCTYPE html lang="en"><body><script>

var cody = {

  living: true,

  age: 23,

  gender: 'male',

  getGender: function () { return cody.gender; }

}

console.log(cody.getGender()); // 记录 'male'

</script></body>

```

注意 Getter 函数，我们正在 `cody` 对象本身上使用点符号法（例如 `cody.gender`）访问 `gender` 属性。可以使用 `this` 重写，以访问 `this` 指向的 `cody` 对象。

示例：99.html

```html
<!DOCTYPE html lang="en"><body><script>

var cody = {

  living: true,

  age: 23,

  gender: 'male',

  getGender: function () { return this.gender; }

}

console.log(cody.getGender()); // 记录 'male'

</script></body>

```

注意 Getter 函数，我们正在 `cody` 对象本身上使用点符号法（例如 `cody.gender`）访问 `gender` 属性。可以使用 `this` 重写，以访问 `this` 指向的 `cody` 对象。

# this 的值是如何确定的？

`this` 的值基于函数被调用时的上下文。注意这一点，因为这是你需要掌握的主题之一。

示例：101.html

```html
<!DOCTYPE html lang="en"><body><script>

window.foo = 'foo';

window.myObject = { foo: 'I am myObject.foo' };

window.sayFoo = function () {

  console.log(this.foo);

};

window.myObject.sayFoo = window.sayFoo;

window.myObject.sayFoo(); // 记录 'I am myObject.foo'.

window.sayFoo(); // 记录 'foo'.

</script></</body>

</html>
```

确保在传递函数或对一个函数有多个引用时，意识到 `this` 的值会根据你调用函数的上下文而改变。

## 注意

除了 `this` 和 `arguments` 之外的所有变量都遵循词法作用域。

# this 关键字在函数中指向头对象

你可能在想当 `this` 使用在嵌套函数内部时会发生什么。坏消息是在 ECMA 3 中，`this` 会丢失方向并指向头对象（浏览器中的 `window` 对象），而不是定义函数所在的对象。

在下面的代码中，`func2` 和 `func3` 内部的 `this` 丢失方向，指向的不是 `myObject` 而是头对象。

示例：102.html

```html
<!DOCTYPE html lang="en"><body><script>

var myWeb = {

  func1: function () {

    console.log(this); // 记录 myObject.

    var func2 = function () {

      console.log(this) // 记录 window，并且从现在开始都是如此。

      var func3 = function () {

        console.log(this); // 记录 window，因为它是头对象。

      } ();

    })();

  }

}

</script></body>

</html>
```

好消息是，这将在 ECMAScript 5 中得到修复。目前，你应该意识到这种困境，尤其是当将函数作为值传递给其他函数时。考虑下一个示例，以及当将匿名函数传递给 `foo.func1` 时会发生什么。当匿名函数在 `foo.func1` 内部被调用时（函数内部的函数），该匿名函数的 `this` 值将是（头）对象的引用。

示例：sample103.html

```html
<!DOCTYPE html><html lang="en"><<body><script>

var foo = {

  func1: function (bar) {

    bar(); // 打印 window，而不是 foo。

    console.log(this); // 这里的 this 关键字将是指向 foo 对象的引用。

  }

}

foo.func1(function () { console.log(this) });

</script></body></html>
```

现在你永远不会忘记：`this` 始终是指向宿主对象的引用，除非该宿主函数被封装在另一个函数内部，或者在另一个函数的上下文中被调用（再次，这在 ECMAScript 5 中已修复）。

## 通过作用域链解决嵌套函数问题

为了让 `this` 值不丢失，你可以简单地使用作用域在父函数中保留对 `this` 的引用。下面的示例演示了如何使用一个名为 `that` 的变量并利用其作用域，可以更好地跟踪函数上下文。

示例：sample104.html

```html
<!DOCTYPE html><html lang="en"><<body><script>

var myObject = {

  myProperty : 'I can see the light',

  myMethod : function() {

    var that = this; // 在 myMethod 作用域中存储 this（即 myObject）的引用。

    var helperFunction = function() { // 子函数。

 // 通过作用域链打印 'I can see the light'，

 // = this.

 console.log(that.myProperty); // 打印 'I can see the light "that"。

 console.log(this); // 如果我们不使用 that，则打印 window 对象。

 }

}

myObject.myMethod(); // 调用 myMethod。

<script></body></html>
```

## 使用 `call()` 或 `apply()` 控制 `this` 的值

`this` 的值通常由调用函数时的上下文决定（除非使用了 `new` 关键字——稍后会详细介绍这一点），但你可以使用 `apply()` 或 `call()` 控制并覆盖 `this` 的值，以定义调用函数时 `this` 指向。使用这些方法就像：“嘿，调用 X 可以告诉函数使用 Z 对象作为 `this` 的值。”这样做改变了 JavaScript 确定 `this` 的默认方式。

在下一个示例中，我们创建了一个对象和一个函数。然后我们通过 `call()` 调用函数，使得函数内部的 `this` 值使用 `myObject` 作为其上下文。`myFunction` 内部的语句将为 `myObject` 填充属性而不是头部。我们更改了 `this`（`myFunction` 内部）指向的对象。

示例：sample105.html

```html
<!DOCTYPE html> <html lang="en"><<body><script>

var myObject = {};

var myFunction = function (param1, param2) {

 // 通过 call() 设置，当函数被调用时，'this' 指向 myObject。

 this.foo = param1;

 this.bar = param2;

 console.log(this); // 打印 Object {foo = 'foo', bar = 'bar'}

}

myFunction.call(myObject, 'foo', 'bar'); // 调用函数，将值设置为 myObject。

console.log(myObject) // 打印 Object {foo = 'foo', bar = 'bar'}

```
</body></html>
```

在上一个示例中，我们使用了 `call()`，也可以使用 `apply()`。两者的区别在于函数参数传递的方式。使用 `call()` 时，参数是逗号分隔的值。使用 `apply()` 时，参数值在数组内部传递，如下所示。

示例：sample106.html

```html
<!DOCTYPE html><html lang="en"><<body><script>

var myObject = {};

var myFunction = function (param1, param2) {
    // 使用 apply()，当函数被调用时，this 指向 thisObject。
    this.foo = param1;
    this.bar = param2;
    console.log(this) // 打印 Object {foo = 'foo', bar = 'bar'}
}

myFunction.apply(myObject, ['foo', 'bar']); // 调用函数，设置此值。

console.log(myObject) // 打印 Object {foo = 'foo', bar = 'bar'}
</script></body></html>
```

你在这里需要的是，你可以覆盖 JavaScript 在函数作用域中确定 `this` 值的默认值。

## 在用户定义的构造函数内部使用 `this` 关键字

当使用 `new` 关键字调用函数时，`this` 的值——如构造函数中所述——指向实例本身。换句话说：我们可以在对象创建之前通过 `this` 利用该对象。通过这种方式，`this` 的默认值发生的变化类似于使用 `call()` 或 `apply()`。

在接下来的示例中，我们设置了一个 `Person` 构造函数，它使用 `this` 来引用正在被创建的对象。当创建 `Person` 的实例时，`this.name` 将引用新创建的对象，并在新对象中放置一个名为 `name` 的属性，其值为传递给构造函数的参数 `(name)`。

示例：sample107.html

```html
<!DOCTYPE html><html lang="en"><<body><script>
var Person = function (name) {
  this.name = name || 'john doe';
}
var cody = new Person('Cody Ling'); // this.name 将引用新创建的对象，并在新对象中放置一个名为 name 的属性，其值为传递给构造函数的参数 (name)。
console.log(cody.name); // 打印 'Cody Ling'
</script></body></html>
```

再次强调，除非该宿主函数被封装在另一个函数内部，或者在另一个函数的上下文中被调用时，`this` 始终是指向宿主对象的引用。在调用构造函数时由于没有使用 `new` 关键字，`this` 将将是调用函数上下文的（头）对象。让我们检查以下场景：

sample108.html

```html
<!DOCTYPE html><html lang="en"><<body><script>
var Person = function (name) {
  this.name = name || 'john doe';
}
var cody = Person('Cody Ling'); // 注意我们没有使用 'new'。
console.log(cody.name); // undefined
console.log(this); // 打印 window 对象。
</script></body></html>
```

## 构造函数原型属性中的 `this` 关键字指向实例

当使用 `new` 关键字调用函数时，`this` 的值——如构造函数中所述——指向实例本身。换句话说：我们可以在对象创建之前通过 `this` 利用该对象。通过这种方式，`this` 的默认值发生的变化类似于使用 `call()` 或 `apply()`。

在接下来的示例中，我们设置了一个 `Person` 构造函数，它使用 `this` 来引用正在被创建的对象。当创建 `Person` 的实例时，`this.name` 将引用新创建的对象，并在新对象中放置一个名为 `name` 的属性，其值为传递给构造函数的参数 `(name)`。

示例：sample109.html

```html
<!DOCTYPE html><html lang="en"><<body><script>
var Person = function (x) {
  if (x) { this.fullName = x };
}

Person.prototype.whatIsFullName = function () {
  return this.fullName; // 'this' 指向从 Person() 创建的实例
}

var cody = new Person('cody lingley');
var lisa = new Person('lisa lingley');

// 调用 whatIsFullName 方法，该方法使用 this 指向实例。
console.log(cody.whatIsFullName(), lisa.whatIsFullName()); // 输出 'cody lingley 'lisa lingley'

/* 原型链仍然有效，如果实例不包含 fullName 属性，它将在原型链中查找。接下来，
我们在 Person 原型和 Object 原型上都添加 fullName。参见此示例后的注释。 */

Object.prototype.fullName = 'John Doe';
var john = new Person(); // 没有向 fullName 传递参数
console.log(john.whatIsFullName()); // 输出 'John Doe'.

</script></body></html>
```

这里需要学习的概念是，`this` 关键字用于引用包含在原型对象方法内部的实例。如果实例不包含，则开始原型链查找。

# 注释

如果实例或 `this` 指向的对象不包含所引用的属性，适用于任何属性查找的相同规则将适用，并在原型链上进行“查找”属性。因此在我们的示例中，如果实例不包含 `fullName` 属性，将在 `Person.prototype.fullName` 查找，然后是 `Object.prototype.fullName`。

## 第 13 章 作用域与闭包

## JavaScript 作用域概述

在 JavaScript 中，作用域是代码执行的上下文。作用域有三种：全局作用域、局部作用域（有时称为“函数作用域”）和 eval 作用域。

在函数内部使用 `var` 定义的代码是局部的，并且对该函数内的其他表达式“可见”，这包含了嵌套/子函数内部的代码。在全局作用域中定义的变量可以在任何地方访问，因为它是作用域链的最高层也是最后的终点。

检查下面的代码，确保你理解每个 `foo` 声明都是独立的作用域。

sample11.html

```html
<!DOCTYPE html>
<html lang="en"><body><script>
var foo = 0; // 全局作用域。
console.log(foo); // 打印 0。

myFunction = function() {
  var foo = 1; // 局部作用域。
  console.log(foo); // 打印 1。

  myNestedFunction = function() {
    var foo = 2; // 局部作用域。
    console.log(foo); // 打印 2。
  } 
}();
neval('var foo = 3; console.log(foo)'); // eval 作用域。
</script></body></html>
```

确保你理解每个 `foo` 变量包含不同的值，因为它们每一个都定义在特定的限定作用域中。

## 注意事项

- 可以创建无限数量的函数和 eval 作用域，而 JavaScript 环境只使用一个全局作用域。

- 全局作用域是作用域链的最后一个站点。

链式的函数会创建堆栈的执行作用域。这些链在一起的栈通常被称为作用域链。

## JavaScript 没有块级作用域

由于逻辑语句（例如 `if`）和循环语句（例如 `for`）不会创建作用域，因此变量可以相互覆盖。检查代码并确保你理解在程序执行代码时，`foo` 的值正在被重新定义。

示例：sample111.html

```html
<!DOCTYPE html>
<html lang="en"><body><script>
  var foo = 1; // foo = 1。

  if (true) {
    foo = 2; // foo = 2。
    for (var i = 3; i <= 5; i++) {
      foo = 1; // foo = 3, 4, 5。
      console.log(foo); // 打印 3, 4, 5。
    }
  }
</script></body></html>
```

所以 `foo` 随着代码执行而改变，因为 JavaScript 没有块级作用域——只有函数、全局或 eval 作用域。

## 在函数内部使用 var 声明变量以避免作用域陷阱

JavaScript 将任何缺少 `var` 声明的变量（即使是包含在函数或封装函数中的）声明在全局作用域中，而不是预期的局部作用域。看看下面的代码，注意如果没有使用 `var` 来声明 `bar`，该变量实际上定义在全局作用域中，而不是它应该在的局部作用域中。

示例：sample112.html

```html
<!DOCTYPE html>
<html lang="en"><body><script>
  var foo = function () {
    var boo = function () {
      bar = 2; // 没有使用 var，所以 bar 被放置在全局作用域中
      window.bar
    }
  }}();

console.log(bar); // 打印 2，因为 bar 在全局作用域中。

// 与此相反……

var foo = function () {
  var boo = function () {
    var doo = 2;
  } ();
} ();

// console.log(doo); undefined。doo 在 boo 函数作用域中，所以
// 会发生错误
</script></body></html>
```

需要记住的观点是，在函数内部定义变量时，你应该始终使用 `var`。这可以防止你处理可能引起混惑的作用域问题。当然，这一惯例的例外是你想从函数内部创建或更改全局作用域中的属性。

## 作用域链（又称词法作用域）

当 JavaScript 查找变量关联的值时，会遵循一条查找链。这条链建立在作用域的层次结构之上。在代码中，我正在从 `func` 作用域打印 `sayHiText` 的值。

示例：sample113.html

```html
<!DOCTYPE html>
<html lang="en"><body><script>

var sayHiText = 'howdy';

var func1 = function () {
  var func2 = function () {
    console.log(sayHiText); // func2 作用域，但在全局作用域中找到了 sayHiText。
  } (); 
} ();
</script></body>
```

当 `sayHiText` 不在 `func2` 函数的作用域内时，它是如何找到的？JavaScript 首先在 `func2` 函数内部查找名为 `sayHiText` 的变量。在 `func2` 中没有找到，它就会查找 `func2` 的父函数 `func1`。在 `func1` 作用域中也没有找到 `sayHiText`，因此 JavaScript 继续向上直到全局作用域，在那里找到了 `sayHiText`，此时交付 `sayHiText` 的值。如果全局作用域中未定义 `sayHiText`，JavaScript 将返回 `undefined`。

这是一个非常重要的概念。让我们来看另一个代码示例，其中我们从三个不同的作用域获取了三个值。

**示例：sample114.html**

```html
<!DOCTYPE html>
<html lang="en"><body><script>

var x = 10;
var foo = function () {
  var y = 20;
  var bar = function () {
    var z = 30;
    console.log(z + y + x); // 打印 60
  }
  bar();
}
foo(); 

</script></body></html>
```

`z` 的值对于 `bar` 函数局部。`y` 的值对于 `foo` 函数局部。`x` 的值是全局的。

## 作用域链返回找到的第一个

在下面的示例中，名为 `x` 的变量存在相同的作用域中，它遮蔽了链上更处的变量。

**示例：sample115.html**

```html
<!DOCTYPE html>
<html lang="en"><body><script>

var x = false;
var foo = function () {
  var x = false;
  var bar = function () {
    var x = true; // 局部 x 在作用域中优先
    console.log(x);
  } ();
}
foo(); // 打印 true.
</script></body></html>
```

记住，当作用域在链的最近链接中找到变量时，即使在链的高处使用了相同的变量名。

## 作用域在函数定义时确定，而不是调用时

由于函数决定作用域，且函数可以像任何 JavaScript 值一样传递，人们可能会认为解析作用域链很复杂。实际上它非常简单。作用域链是由函数在定义期间决定的，而不是在调用期间。这也被称为词法作用域。对此深思，因为大多数人在 JavaScript 代码中都会出错。

作用域是在调用函数之前创建的。由于这一点，我们可以创建闭包。例如，我们可以让一个函数将嵌套函数返回到全局作用域，然而我们的函数仍然可以访问作用域链，其父函数的作用域。在下面的示例中，我们定义了一个返回匿名函数的 `parentFunction`，并从全局作用域调用返回的函数。这被称为闭包。

示例：sample116.html

```html
<!DOCTYPE html>
<html lang="en"><body><script>
var parentFunction = function () {
  var foo = 'foo';
  return function () { // 被返回的匿名函数
    console.log(foo); // 打印 'foo'。
  }
}
// nestedFunction 指向 parentFunction 返回的嵌套函数。
var nestedFunction = parentFunction();

nestedFunction(); // 打印 foo，因为返回的函数通过作用域链访问 foo。
</script></body></html>
```

你在这里应该汲取的结论是：作用链是在定义期间确定的——字面面上就是取决于代码的编写方式。在你的代码中传递函数不会改变作用链。

## 闭包是由作用链引起的

结合你在本章中学到的关于作用链和作用域查找的知识，理解闭包应该不会过于复杂。在接下来的示例中，我们创建了一个名为 `countUpFromZero` 的函数。这个函数返回了它内部包含的子函数的引用。当这个子函数（嵌套函数）被调用时，由于作用链的存在，它可以访问父函数。

**示例：sample11.html**

```html
<!DOCTYPE html><html lang="en"><body<script>
var countUpFromZero = function () {
  var count = 0;
  return function () // 返回嵌套的子函数
    return count++; // count 在作用链上游定义，在父函数中
  };
})(); // 立即调用，返回嵌套函数。

console.log(countUpFromZero()); // 打印 1.
console.log(countUpFromZero()); // 打印 2.
console.log(countUpFromZero()); // 打印 3.
</script></body></html>
```

每次调用 `countUpFromZero` 函数时，包含在（并返回自）`countUpFromZero` 函数的匿名函数仍然具有访问父作用域。。这种作用链促进的技巧是闭包的一个示例。

## 注意事项

如果你觉得我过度简化了闭包，那么你的这种想法可能是正确的。但我故意这么做了，因为我认为重要的部分源于对函数和作用域的扎实理解，而不一定取决于执行上下文的复杂性。如果你需要深入研究闭包，请查看“JavaScript 闭包”。

# 第 14 章函数 prototype 属性

## 原型链的概念概览

`prototype` 属性是 JavaScript 为每个 `Function()` 实例创建的对象。它将使用 `new` 关键字创建的对象实例链接回创建它们的构造函数。这样做是为了让实例可以共享或继承方法和属性。重要的是，这种搜索发生在属性查找期间。记住第 1 章中的内容：每当你查找或访问对象上的属性时，该属性会在对象本身以及原型链上进行搜索。

## 注意事项

对于每个函数都会创建一个原型对象，无论你是否打算将该函数作为构造函数。

在下面的代码中，我将从 `Array()` 构造函数构建一个数组，然后我调用 `join()` 方法。

示例：sampleprototype118.html

```html
<!DOCTYPE html><html lang="en"><body<script>
  var myArray = new Array('foo', 'bar');

  console.log(myArray.join()); // 打印 'foo,bar'

</script></body></html>
```

`join()` 方法并没有定义在 `myArray` 对象实例的属性上，但我们似乎可以访问 `join()`，就像它存在一样。这个方法定义在某处，但在哪里呢？嗯，它被定义为 `Array()` 构造函数的 `prototype` 属性的属性。由于在数组对象实例未找到 `join()`，JavaScript 会在原型链上查找 `join()` 方法。

好了，为什么要这样做？实际上，这关乎效率和复用。既然 `join()` 的功能始终是一致的，为什么每个从数组构造函数创建的数组实例都需要定义一个唯一定义的 `join()` 方法呢？让所有数组都复用同一个 `join()` 函数要更有意义，而不是为每个数组都创建一个新的函数实例。

我们所说的这种效率之所以可能，全都是由于 `prototype` 属性、原型链接和原型查找链。在本章中，我们拆解了原型继承中这些经常令人困惑的属性。说实话，你只需要记忆链层级实际上是如何运作的机制会更好。如果你需要复习属性值是如何解析的，请翻回第 1 章。

## 为什么要关注 prototype 属性？

你应该出于四个原因关注 `prototype` 属性。

## 原因 1

第一个原因是，`prototype` 属性被 `Object()`、`Array()` 等原生函数使用，以便实例继承属性和方法。为了更好地理解 JavaScript，你需要了解 `prototype` 属性是如何工作的。

## 原因 2

在创建自定义函数时，JavaScript 使用 `prototype` 属性来处理继承，你需要了解它的工作方式。

## 原因 3

你可能不喜欢原型继承，但现实是，你有一天需要修改或管理原型继承。当你想要理解 JavaScript 时，开发者需要了解 `prototype` 属性。

## 原因 4

使用 `prototype` 属性可以创建复用相同方法的实例。正如提到的，并不是所有实例都需要自己的 `join()` 方法，因为它们在原型链中。

## 默认的 prototype 属性是一个 Object() 对象

所有关于原型的讨论可能变得很复杂。实际上，`prototype` 只是由 JavaScript 在后台创建的名为 "prototype" 的属性，并通过调用 `Function()` 构造函数提供的。如果你手动这样做，看起来像这样：

示例：sample120.html

```html
<!DOCTYPE html><html lang="en"><body<script>
var myFunction = function () { };
function.prototype = {}; // 添加 prototype 属性并将其为空对象。
console.log(myFunction.prototype); // 打印一个空对象。
</script></body></html>
```

事实上，这段示例代码运行良好，基本上只是复制了 JavaScript 已经做的工作。

## 注意事项

`prototype` 属性的值可以设置为 JavaScript 中用的任何复杂值（即对象）。JavaScript 会忽略任何设置为原始值的 `prototype` 属性。

## 从构造函数创建的实例链接到构造函数的 prototype 属性

虽然它是一个对象，但 `prototype` 是特殊的，因为原型链将每个实例链接到其构造函数的 `prototype` 属性。这意味着每当使用 `new` 关键字从构造函数创建实例时（或为原始值创建对象时），它都会在创建的对象实例与创建它的构造函数的 `prototype` 属性之间添加一个隐藏的链接。JavaScript 在调用构造函数时在后台将这些连接起来，而正是这个链接允许了原型链的构建。在接下来的示例中，我们为原生 `Array()` 构造函数的 `prototype` 增加了一个属性，然后我们可以通过设置在实例上的 `__proto__` 属性来访问它。

示例 sample19.html

```html
<!DOCTYPE html><html lang="en"><body<script>

var myFunction = function () {}
myFunction.prototype.test = 1;
console.log(new myFunction()__test); // 打印 1
console.log(typeof myFunction.prototype); // 打印 'object'

</script></body></html>
```

## 示例:sample121.html

```html
<!DOCTYPE html><html lang="en"><body><script>
  // 此代码仅在支持 __proto__ 访问的浏览器有效。
  Array.prototype.foo = 'foo';
  var myArray = new Array();

  console.log(myArray.__proto__.foo); // 输出 foo，因为
  myArray.__proto__ = Array.prototype

</script></body></html>
```

由于访问 __proto__ 并不是官方 ECMA 标准的一部分，存在一种通用的方法通过 `constructor` 属性来追踪对象到其继承的原型之间的链接。下面的示例演示了这一点。

## 示例:sample122.html

```html
<!DOCTYPE html><html lang="en"><body><script>
  Array.prototype.foo = 'foo'; // 现在 Array() 的所有实例都继承了 foo 属性。
  var myArray = new Array();

  // 利用 *.constructor.prototype 追踪 foo
  console.log(myArray.constructor.prototype.foo); // 输出 foo。

  // 或者，当然，利用原型链。
  console.log(myArray.foo) // 输出 foo。

  // 使用原型链在 Array.prototype.foo 查找属性
</script></body></html>
```

在这个示例中，foo 属性是在原型对象中找到的。你需要意识到，这之所以可行是因为 Array() 的实例与 Array() 构造函数原型对象（即 Array.prototype）之间的关联。简单来说，`myArray.__proto__`（或 `myArray.constructor.prototype`）引用了 Array.prototype。

## 原型链的最后一步是 Object.prototype

由于原型链是最后一步，原型链查找是在 Object.prototype 处进行的。在接下来的代码中，我们调用了 `myArray`，它是一个空数组。然后我尝试访问 `myArray` 未定义的属性，触发了原型查找链。在 `myArray` 对象中搜索 `foo` 属性。由于不存在，于在 `Array.prototype` 中查找，但那里也没有。JavaScript 最终查找的地方是 `Object.prototype`。在上述三个对象中都没有定义该属性，因此该属性为 `undefined`。

## 示例: sample123.html

```html
<!DOCTYPE html><html lang="en"><body><script>
  var myArray = [];

  console.log(myArray.foo); // 输出 undefined。

  /* 在 myArray.foo 或 Array.prototype.foo、
  Object.prototype.foo 中未找到 foo，所以它是 undefined。 */
</script></body></html>
```

请注意，链在 Object.prototype 处停止了。我们查找 `foo` 的最后一个地方是 Object.prototype。

## 注意事项

小心！向 Object.prototype 添加的任何内容都会出现在 `for...in` 循环中。

# 原型链返回它在原型链中找到的第一个匹配属性

就像作用域链一样，原型链在链查找过程中将使用它找到的第一个值。

修改之前的代码示例，如果我们向 `Object.prototype` 和 `Array.prototype` 对象添加了该值，然后尝试在数组实例上访问该值，返回的值将将来自 `Array.prototype` 对象。

## 示例: sample124.html

```html
<!DOCTYPE html><html lang="en"><body><script>
  Object.prototype.foo = 'object-foo';
  Array.prototype.foo = 'array-foo';
  var myArray = [];

  console.log(myArray.foo); // 输出 'array-foo$，在 Array.prototype.foo 找到

  myArray.foo = 'bar';

  console.log(myArray.foo) // 输出 'bar$，在 Array.prototype 找到
</script></body></html>
```

在这个示例中，`Array.prototype.foo` 处的 foo 值遮蔽（masking）了在 `Object.prototype.foo` 找到的 foo 值。只需记住，当链中找到属性时查找就会结束，即使在链的更上使用了相同的属性名。

## 用新对象替换原型属性会移除默认的构造函数属性

可以使用新值替换默认的 `prototype` 属性。然而，这样做将消除“预制”原型对象中的默认构造函数 属性——除非你手动指定它。

在接下来的代码中，我们创建了一个 `Foo` 构造函数，用一个新空对象替换 `prototype` 属性，并验证 `constructor` 属性已损坏（它现在引用了性较小的 Object 原型）。

示例: sample125.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var Foo = function() { };

Foo.prototype = {}; // 用一个空对象替换 prototype 属性。

var FooInstance = new Foo();

console.log(FooInstance.constructor === Foo); // 输出 false，我们破坏了引用。
console.log(FooInstance.constructor); // 输出 Object()而不是 Foo()

// 与我们没有替换 prototype 值的代码对比。

var Bar = function Bar() { };

var BarInstance = new Bar();

console.log(BarInstance.constructor === Bar); // 输出 true。
console.log(BarInstance.constructor); // 输出 Bar()

</script></body></html>
```

如果你打算替换由 JavaScript 设置的默认 `prototype` 属性（这在某些 JS 模式中很常见），你应该写回一个引用该构造函数的 `constructor` 属性。在接下来的示例中，我们修改了之前的代码，使 `constructor` 属性提供指向正确构造函数的引用。

示例: sample126.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var Foo = function Foo() { };

Foo.prototype = { constructor: Foo };

var FooInstance = new Foo();

console.log(FooInstance.constructor === Foo); // 输出 true。
console.log(FooInstance.constructor); // 输出 Foo()

</script></body></html>
```

## 从原型继承的实例始终获取最新值

`prototype` 属性是动态的，这种动态意味着无论实例何时安装，实例总是会获取最新值。在接下来的代码中，我们创建了一个 `Foo` 构造函数，添加属性 `x`，然后创建一个实例。接下来，我们记录 `x` 的值。然后我们更新原型并记录它。

示例: sample127.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var Foo = function() { };

Foo.prototype = { x: 1 };

var FooInstance = new Foo();

console.log(FooInstance.x); // 输出 1。

Foo.prototype.x = 2;

console.log(FooInstance.x); // 输出 2，FooInstance 更新了。

</script></body></html>
```

考虑到查找链的工作原理，这种行为不应该意外。无论你使用的是默认原型还是覆盖它，这种工作都有效。在示例中，我替换了默认原型来演示这一点。

示例: sample128.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var Foo = function() { };

Foo.prototype = { x: 1 }; // 后面的日志相同。

var FooInstance = new Foo();

console.log(FooInstance.x); // 输出 1。

Foo.prototype = { x: 2 };

console.log(FooInstance.x); // 输出 1。什么？

</script></body></html>
```

## 用新对象替换原型属性不会更新之前的实例

你可能认为随时替换原型属性，所有实例随之更新，但事实并非如此。当你创建一个实例时，该实例将与实例化时的原型绑定。提供新对象作为 `prototype` 属性不会更新已创建实例之间的连接。

但请记住，正如我提到的，你可以更新或向原始创建的对象添加内容，这些值仍然保持连接。

示例: sample129.html

```html
<!DOCTYPE html><html lang="en"><body><script>
var Foo = function Foo() { };

Foo.prototype.x = 1;

var FooInstance = new Foo();

console.log(FooInstance.x); // 输出 1，正如你认为的那样。

// 现在让我们用新对象替换/覆盖原型对象。
Foo.prototype = { x: 2 };

console.log(FooInstance.x); // 输出 1。什么？因为我们刚刚更新了原型它应该输出 2 吗？
/* FooInstance 仍然引用实例化时原型对象的相同状态。 */

// 创建 Foo() 的新实例
var NewFooInstance = new Foo();

// 新实例现在绑定到新的原型对象值（即 {x:2}）。
console.log(NewFooInstance.x); // 输出 2。
</script></body></html>
```

这里需要掌握的核心思想是：一旦你开始创建实例，就不应该用新对象替换对象的原型（prototype）。这样做将导致实例拥有指向不同原型的链接。

## 用户定义的构造函数可以利用与原生构造函数相同的原型继承

希望在章节的这里，你已经理解了 JavaScript 是如何利用原型进行继承的（例如 `Array.prototype`）。在创建非原生的、用户定义的构造函数时，也可以利用这种模式。在接下来的示例中，我们取了经典的 `Person` 对象，并模拟了 JavaScript 用于继承的模式。

**示例：sample130.html**

```html
<!DOCTYPE html><html lang="en"><<body><script>
var Person = function () {
  // 所有 Person 继承了 legs, arms 和 countLimbs 属性。
  Person.prototype.legs = 2;
  Person.prototype.arms = 2;
  Person.prototype.countLimbs = function () { return this.legs + this.arms; };
};

var chuck = new Person();
console.log(chuck.countLimbs()); // 志记输出 4.
</script></body></html>
```

在这段代码中，创建了一个 `Person()` 构造函数。然后我们向 `Person()` 的 `prototype` 属性添加了属性，这些属性可以被所有实例继承。显然，你在代码中利用原型链的方式与 JavaScript 在原生对象继承中利用的方式是相同的。

作为一个你可以继承多少内容的示例，你可以创建一个构造函数，如果未提供参数，则其实例将继承 `legs` 和 `arms` 属性。在接下来的示例中，如果向 `Person()` 构造函数传递了参数，这些参数将作为实例属性；但如果没有提供一个或多个属性，则有一个回退机制。这些实例属性会遮蔽（shadow）或掩盖继承来的属性，从而让你兼得两者之。

**示例：sample131.html**

```html
<!DOCTYPE html><html lang="en"><<body><script>
var Person = function (legs, arms) {
  // 遮蔽原型值。
  if (legs !== undefined) { this.legs = legs; }
  if (arms !== undefined) { this.arms = arms; }
}

Person.prototype.legs = 2;
Person.prototype.arms = 2;
Person.prototype.countLimbs = function () { return this.legs + this.arms; };

var chunk = new Person(0, 0);
console.log(chunk.countLimbs()); // 志记输出 0.
</script></body></html>
```

## 创建继承链（原始意图）

原型继承允许创建模拟传统面向对象编程语言中模式的继承链。在 JavaScript 中，为了让一个对象继承另一个对象，你所做的就是创建一个想要继承的对象的实例，并将其赋值给要继承对象的 `prototype` 属性。

在下方的代码示例中，`Chef` 对象（即 `cody`）继承自 `Person()`。这意味着如果在 `Chef` 对象中没有找到某个属性，它将在创建 `Person()` 对象的函数的原型上查找。要建立这种继承，你只需要将 `Person()` 的一个实例实例化，并作为 `Chef.prototype` 的值（即 `Chef.prototype = new Person()`）。

**示例：sample132.html**

```html
<!DOCTYPE html><html lang="en"><<body><script>
var Person = function () { this.bar = 'bar'; };
Person.prototype.foo = 'foo';

var Chef = function () { this.goo = 'goo'; };
Chef.prototype = new Person();
var cody = new Chef();

console.log(cody.foo); // 志记输出 'foo'
console.log(cody.goo); // 志记输出 'goo'
console.log(cody.bar); // 志记输出 'bar'.
</script></body></html>
```

# 创建数组

和大多数 JavaScript 对象一样，数组对象可以使用 `new` 运算符结合 `Array()` 构造函数创建，或者使用字面量语法。

### 数组的概览

数组是包含一组值的有序列表。数组可以持有任何类型，这些值可以在任何时候被更新或删除。数组通常通过索引来访问。

在接下来的示例中，我们使用 `Array()` 构造函数创建 `myArray` 数组，这与字面量不同。

**示例：sample133.html**

```html
<!DOCTYPE html><html lang="en"><<body><script>
var myArray = ['blue', 'green', 'orange', 'red'];

console.log(myArray[0]); // 志记输出 blue

// 与
var myObject = {
    'blue',
    'green',
    'orange',
    'red'
  };

console.log(myObject['blue']); // 志记输出 blue
</script></body></html>
```

## 注意事项

数组可以持有任何类型，这些值可以在任何时候被更新。数组通常是值的集合。

### 数组参数

你可以通过构造函数向数组传递值。然而，如果只向构造函数发送一个参数，它将用于设置长度。

**示例：sample134.html**

```html
<!DOCTYPE html><html lang="en"><<body><script>
var foo = new Array('foo', 'bar');
console.log(foo[0], foo.length); // 志记输出 foo 2

var bar = new Array(3);
console.log(bar[0], bar.length); // 志记输出 undefined 3
</script></body></html>
```

### 数组属性和方法

Array 对象具有以下属性（不继承的）：

属性：

- prototype

- length

### 数组对象的实例属性和方法

数组实例具有以下属性和方法（不继承的）：

实例属性（例如 `var myArray = ['foo', 'bar']`）：

- constructor

- length

实例方法（例如 `var myArray = ['foo']`）：

- pop()

- push()

- reverse()

- shift()

- sort()

- splice()

- unshift()

- concat()

- join()

- slice()

对于空数组的数字索引 50，JavaScript 将在其之前填充所有必要的索引并赋予 `undefined` 值。

示例：sample136.html

```html
<!DOCTYPE html lang="en"><body
<script>
var myArray = [];
myArray[50] = 'blue';
console.log(myArray.length); /* 记录 51 (0 被计算在内)，因为 JS 在 "blue" 之前创建了
0 到 50 的值。*/
</script>
</body></</html>
```

此外，考虑到 JavaScript 的动态性质以及 JavaScript 不是强类型的这一事实，数组值可以在任何时间进行更新，且索引中包含的值可以是任何合法值。在下面的示例中，我将数字索引 50 处的值更改为了对象。

示例：sample137.html

```html
<!DOCTYPE html lang="en"><body><script>
var myArray = [];
myArray[50] = 'blue';
myArray[50] = {'color': 'blue'}; // 将对象类型从字符串改为
Object(). object.
console.log(myArray[50]); // 记录 'Object {color="blue"}'

// 使用括号访问数组中的索引，然后访问属性
blue.
console.log(myArray[50]['color']); // 记录 'blue'

// 使用点表示法。
console.log(myArray[50].color); // 记录 'blue'
</script></body></</html>
```

## 长度 (Length) 与 索引 (index)

数组从零开始索引值。这意味着数组中存储值的第一个数字槽看起来像 `myArray[]`。这可能有点让人困惑——如果我创建一个包含单个值的数组，那么该值的索引是 0，而数组的长度是 1。请确保你理解数组的长度代表数组中所包含的数量，而数字索引是从零开始的。

在下面的示例中，字符串值 blue 包含在 `myArray` 数组的数字索引 0 中，但由于数组包含一个值，因此数组的长度为 1。

## 示例：sample138.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = ['blue'] // 索引 0 包含字符串值 'blue'。
console.log(myArray[0]); // 记录 'blue'。
console.log(myArray.length); // 记录 1。

</script></body></</html>
```

## 使用预定义长度定义数组

正如我之前提到的，通过向 `Array()` 构造函数传递单个整数，可以重新定义数组的长度，即它将包含的值的数量。在这种情况下，构造函数会进行特殊处理，假设你想设置数组的长度，而不是预先填充数组值。

在下一个示例中，我们设置了预定义长度为 3 的 `myArray`。同样，我们正在配置数组的长度，传递一个要存储在索引 0 的的值。

## 示例：sample139.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = new Array(3);
console.log(myArray.length); // 记录 3，因为我们传递了一个数字参数。
console.log(myArray[0]); // 记录 undefined。

</script></body></</html>
```

## 注意事项

提供预定义长度将为指定长度范围每个数字索引关联一个 `undefined` 值。

你可能在想是否可以创建一个只包含一个数字值的预定义数组。是的，可以的——通过使用字面量 `var myArray = [4]`。

## 设置数组长度可以添加或删除值

数组对象的 `length` 属性可以用于获取或设置数组的长度。如之前所示，将长度设置为数组中包含的实际值数量大于将向数组添加 `undefined` 值。你可能意料不到的是，你实际上可以通过将长度值设置为小于数组中包含的值数量的数字来从数组中删除值。

## 示例：sample140.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = ['blue', 'green', 'orange', 'red'];
console.log(myArray.length); // 记录 4。
myArray.length = 99;
console.log(myArray.length); // 记录 99，记住我们设置了长度，即索引。
myArray.length = 1; // 移除所有剩余的一个值，所以索引 [1] 消失了！
console.log(myArray[1]); // 记录 undefined。

console.log(myArray); // 记录 ['blue']

</script></body></</html>
```

## 包含其他数组的数组（即多维数组）

由于数组可以持有任何有效的 JavaScript 值，数组可以包含其他数组。当这样做时，包含封装数组的数组被称为*多维数组*。访问封装的数组通过*括号链式* (bracket chaining) 实现。在下面的示例中，我们创建了一个包含数组的数组字面量，在其中我们创建了另一个数组字面量，在并在内部我们在索引 0 处创建了另一个字符串值。

## 示例：sample141.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = [[['4th dimension']]]];
console.log(myArray[0][0][0]); // 记录 '4th dimension'

</script></body></</html>
```

这个例子相当愚蠢，但你理解数组可以包含其他数组，你可以无限地访问封装的数组。

## 遍历数组，反向和正向

遍历数组最简单且可能是快的方法是使用 *while* 循环。在下面的代码中，我们从索引的开始循环到结束。

## 示例：sample142.html

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = ['blue', 'green', 'orange', 'red'];
var myArrayLength = myArray.length; // 缓存数组长度以避免不查找。
var counter = 0; // 设置计数器。

while (counter < myArrayLength) { // 如果计数器小于数组长度则运行。
console.log(myArray[counter]); // 记录 'blue', 'green', 'orange',
'red'。
  counter++; // 计数器加 1。
}

</script></body></</html>
```

现在我们从索引的结束到开始。

**示例：sample143.html**

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = ['blue', 'green', 'orange', 'red'];
var myArrayLength = myArray.length;
var counter = myArrayLength - 1;

while (counter >= 0) {
  console.log(myArray[counter]); // 记录 'red', 'orange', 'green', 'blue'。
  counter--;
}

</script></body></</html>
```

获取/设置/更新对象的属性是通过使用点符号（dot notation）或括号符号（bracket notation）完成的。当操作的对象属性名以表达式的形式时（例如 `Array['prototype']['join'].apply()`），使用括号符号会非常方便。

在引用对象时，会使用查找链（lookup chain）首先在被引用的对象中查找该属性。如果没有找到该属性，则会在构造函数的 `prototype` 属性上查找。如果仍未找到，由于原型持有一个对象值，且该对象值是由 `Object()` 构造函数创建的，则会通过 `Object()` 构造函数的 `prototype` 属性进行查找。如果仍未找到，则该属性将被确定为 `undefined`。

`prototype` 查找链是 JavaScript 实现继承（亦原型继承）的设计方式。

由于对象属性查找链（亦原型继承），所有对象都继承自 `Object()`，这仅仅是因为 `prototype` 属性本身就是一个 `Object()` 对象。

JavaScript 函数是一等公民：函数函数是具有属性和值的对象。

`this` 关键字在函数内部使用时，是引用包含该函数的对象的通用方式。

`this` 的值是在运行时根据函数被调用的上下文确定的。

在全局作用域中使用时，`this` 关键字指向全局对象。

JavaScript 使用函数作为创建唯一作用域的方式。

JavaScript 提供了全局作用域，所有的 JavaScript 代码都存在此作用域中。

函数（特别是封装函数）为解析变量查找创建了作用域链（scope chain）。

作用域的建立基于代码的编写方式，而不一定取决于函数被调用的上下文。这允许函数访问其原始编写时所在的作用域，即使该函数是从不同的上下文被调用的。这种结果被称为闭包（closure）。

在函数内部使用 `var` 声明的函数表达式和变量将变成全局属性。然而，函数作用域内部的函数声明（function statements）仍然定义在它们被编写的作用域中。

- 在全局作用域中声明（不使用 `var`）的函数和变量将成为全局对象的属性。

- 在全局作用域中声明（使用 `var`）的函数和变量将成为全局变量。

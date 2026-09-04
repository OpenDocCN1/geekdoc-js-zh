
# JavaScript 入门指南

## 第3章 - Object()

- 使用`Object()`对象的概念概述
- `Object()`参数
- `Object()`属性和方法
- `Object()`实例属性和方法
- 使用"对象字面量"创建`Object()`对象
- 所有对象都继承自`Object.prototype`

## 第4章 - Function()

- 使用`Function()`对象的概念概述
- `Function()`参数
- `Function()`属性和方法
- `Function`对象实例属性和方法
- 函数总是返回一个值
- 函数是一等公民（不仅是语法，更是值）
- 向函数传递参数
- 所有函数均可用的`this` & `arguments`值
- `arguments.callee`属性
- 函数实例的`length`属性与`arguments.length`
- 重定义函数参数
- 在函数完成之前返回函数（即取消函数执行）
- 定义函数（语句、表达式或构造函数）
- 调用函数（函数、方法、构造函数或`call()` & `apply()`）
- 匿名函数
- 自执行函数表达式
- 自执行匿名函数语句
- 函数可以嵌套
- 将函数传递给函数并从函数返回函数
- 在定义之前调用函数语句（即函数提升）
- 函数可以调用自己（即递归）

## 第5章 - 头对象/全局对象

- 头对象的概念概述
- 头对象中包含的全局函数
- 头对象与全局属性及全局变量
- 引用头对象
- 头对象是隐式的，通常不会被显式引用

## 第6章 - this 关键字

- `this`的概念概述以及它如何引用对象
- `this`的值是如何确定的？
- `this`关键字在嵌套函数中指向头对象
- 利用作用域链解决嵌套函数问题
- 使用`call()`或`apply()`控制`this`的值
- 在用户定义的构造函数内部使用`this`关键字
- 原型方法内部的`this`关键字指向构造函数实例

## 第7章 - 作用域与闭包

- JavaScript作用域的概念概述
- JavaScript没有块作用域
- 在函数内部使用`var`声明变量以避免陷阱（gotchas）
- 作用域链（又称词法作用域）
- 作用域链查找返回第一个找到的值
- 作用域是在函数定义时确定的，而不是调用时
- 闭包是由作用域链引起的

## 第8章 - 函数原型属性

- 原型链的概念概述
- 为什么要关注原型属性？
- 所有`Function()`实例都具有原型属性
- 默认原型属性是一个`Object()`对象
- 从构造函数创建的实例与构造函数的原型属性相连
- 原型链的终点是`Object.prototype`
- 原型链返回在链中找到的第一个原型匹配项
- 用新对象替换原型属性会移除默认构造函数属性
- 从原型继承属性的实例将始终获得最新值
- 用新对象替换原型属性不会更新之前的实例
- 用户定义的构造函数可以利用与原生构造函数相同的原型继承
- 创建继承链（原始意图）

## 第9章 - Array()

- 使用`Array()`对象的概念概述
- `Array()`参数
- `Array()`属性与方法
- `Array`对象实例的属性与方法
- 创建数组
- 在数组中添加和更新值
- 长度（Length）与索引（index）
- 使用预定义长度定义数组
- 设置数组长度可以添加或删除值
- 包含其他数组的数组（又称多维数组）
- 对数组进行循环，反向和正向

## 第10章 - String()

- 使用`String()`对象的概念概述
- `String()`参数
- `String()`属性与方法
- `String`对象实例的属性与方法

## 第11章 - Number()

- 使用`Number()`对象的概念概述
- 整数与浮点数
- `Number()`参数
- `Number()`属性
- `Number`对象实例的属性与方法

## 第12章 - Boolean()

- 使用`Boolean()`对象的概念概述
- `Boolean()`参数
- `Boolean()`属性与方法
- `Boolean`对象实例的属性与方法
- 非原始假布尔对象转换为真
- 某些特定的值为假，其他所有均为真

## 处理原始字符串、数字和布尔值

- 当访问属性时，原始/字面量值会被对象
- 你通常应该使用原始字符串、数字和布尔值

## 第13章 - Null

- 使用`null`值的概念概述
- `typeof`将`null`值返回为`"object"`

## 第14章 - Undefined

- `undefined`值的概念概述
- JavaScript ECMA-262 第3版（及更高版本）声明了全局作用域中的`undefined`变量

## 第15章 - Math 函数

- 内置`Math`对象的概念概述
- `Math`属性与方法
- `Math`不是构造函数
- `Math`拥有无法扩展/修改的常量

## 复习

## 结论

# 关于作者

Cody Lindley 是一位客户端工程师（又称前端开发人员）以及一名康复中的 Flash 开发者。他在 HTML、CSS、JavaScript、Flash 以及与 Web 开发相关的客户端性能技术方面拥有丰富的专业背景（11 年以上经验）。当他没有在编写客户端代码时，他可能在钻研界面/交互设计，或者在编写素材以及在各种会议上演讲。当没有坐在电脑前时，可以肯定他正在爱达荷州波伊斯与妻子孩子待在一起——训练铁项运动、滑雪、山地自行车、公路自行车、登山登山、阅读、看电影，或对基督教世界观理性证据进行辩论。

# 关于技术编辑

### Michael Richardson

Michael Richardson 是一位住在爱达荷州波伊斯的 Web 和应用开发者。早些时候，他在莎拉洛伦斯学院获得了创意写作硕士学位，并在 2003 年出版了一部名为《蘑菇广播站计划》（Plans for a Mushroom Radio）的小说。如今，当没有与其爱的妻子和调皮的孩子共度时光时，他正在管理着名为 Timeglider 的小型 Web 应用。

### Kyle Simpson

Kyle Simpson 是一位来自德克萨斯州奥斯汀的 JavaScript 系统架构师。他专注于 JavaScript、Web 性能优化特别是"后端"架构。如果某些东西无法通过 JavaScript 或 Web Stack 技术实现，他可能对此觉得无趣。他运行着多个开源项目，包括 LABajs、Handlebar.JS 和 BlockchainJS。Kyle 在 Mozilla 的开发工具团队担任软件工程师。

### Nathan Smith

Nathan Smith 是普惠（HP）的一名 UX 开发者。他拥有阿斯伯里神学院的神学硕士（MDiv）。他从上世纪就开始构建网站，并喜欢硬编码 HTML、CSS 和 JavaScript。他创建了 960 网格系统，这是一个用于草图、设计和编写页面布局的设计与 CSS 框架。他还制作了 Formalize，这是一个旨在为表单样式带来理性的 JavaScript 和 CSS 框架。

### Ben Nadel

Ben Nadel 是 Epicenter Consulting 的首席软件工程师，这是一家位于曼哈顿的 Web 开发公司，专门从事创新的定制软件，改变其客户的业务模式。他还是 Adobe 社区专业人士以及 Adobe 认证的高级 ColdFusion 专业人士。空闲时间，他会在 www.bennadel.com 上大量撰写关于痴迷的 Web 应用开发各个方面的博客。

### Ryan Florence

Ryan Florence 是一位来自犹他州盐湖市的前端 Web 开发者，自 90 年代初开始就开始创建网站。他特别感兴趣的是创建让终端用户和继承项目的开发者都感到愉悦的体验。Ryan 活跃于 JavaScript 社区，编写插件、为流行的 JavaScript 库做出贡献、在会议和聚会上演讲，并在网上撰写相关文章。他目前在 Clock Four 担任高级技术顾问。

### Nathan Logan

Nathan Logan 已经做了 8 年专业 Web 开发者了。他的重点是客户端技术，但也研究服务端。他目前与本书作者一起在 Molomane 工作。从个人而言，Nathan 拥有非常出色的妻子和儿子，喜欢山地自行车、温泉、辣味食物、苏格兰忌以及基督教信仰/神学。

# 引言

这本书不是关于 JavaScript 设计模式，也不是如何用 JavaScript 代码实现面向对象的范式。它的编写并不是为了区分 JavaScript 语言的优特性和坏特性。它不是一份完整的参考指南。它的目标不是编程初学者或完全没有接触过 JavaScript 的人。它也不是一份 JavaScript 食谱。那类书已经写过了。

我的意图是通过检查原生 JavaScript 对象和支持它们的细微差别（复杂值、原始值、作用域、继承、顶层对象等），为读者提供一个准确的 JavaScript 世界观。我希望这本书是对 ECMA-262 第 3 版规范的简短易于理解的总结，重点关注 JavaScript 中对象的本质。

如果你是一个只在库（如 jQuery、Prototype 等）掩护下使用 JavaScript 的设计师或开发者，我希望书中的材料能让你从一个 JavaScript 库用户转变为一个 JavaScript 开发者。

# 为什么我要写这本书？

首先，我必须承认我写这本书是为了我自己。说实话，我创作这些材料是为了让自己能够"下自己的药"（drink my own Kool-Aid），并永远记住它的味道。换句话说，我想用我自己的语言有一个参考，以检验记忆。此外：

- 库促进了"黑箱"综合，这在某些方面是有益的，但在另一些方面是有害。事情可能完成得很快且高效，但你并不知道如何以及为什么。当出现问题或性能成为问题时，如何以及为什么至关重要。事实上，任何打算在构建 Web 应用（或只是一个好的注册页面）时实现 JavaScript 库或框架的人，都应该查看内部构造并理解引擎。这本书是为那些想要翻开书并亲手操作 JavaScript 的人编写的。

- Mozilla 已经提供了 JavaScript 1.5 的最新且完整的参考指南。我认为缺失的是一份从单一视角撰编写的、易于理解的文档，以与他们的参考指南配合使用。我希望这本书能作为 JavaScript 值的"你需要知道的"手册，详细说明超出 Mozilla 参考指南所涵盖的概念。

- JavaScript 1.5 版本将持续存在很长一段时间，但随着我们向 ECMA 第 5 版中语言的新特性迈进，我想记录下可能将长久存在的 JavaScript 核心概念。

- 关于编程语言的高级技术书籍通常充斥着大块的代码。我更倾向于用简短的解释来直达主题，并以真实代码作为支撑。我创造了"薄切片"（thin-slicing）的术语，来描述我在书中尝试做的事情。

```javascript
// this is a comment about a specific part of the code
var foo = 'calling out this part of the code';
```

除了代码示例加密之外，书中的文本也经过了染色，以区分 JavaScript 单词/关键字、JavaScript 代码以及普通文本。下面，我节选了书中的内容来演示这种颜色语义。

"考虑一下从`Object()`构造函数创建的 cody 对象（例如`var code = new Object()`）与通过`String()`构造函数创建的字符串对象并没有本质区别。为了让你深刻理解这一点，请查看下面的代码："

注意：代码引用使用了灰色斜体文本，JavaScript 单词/关键字使用了橙色文本，而其余的其他内容则使用普通的黑色文本。

## jsFiddle, JS Bin 和 Firebug lite-dev

书中的大多数代码示例都链接到相应的 jsFiddle 页面，可以在该页面上在线调整和执行代码。jsFiddle 示例已配置为使用 Firebug lite-dev 插件，以便`log`函数（`console.log`）在任何现代浏览器中都能工作，无论该浏览器是否有自己的控制台。在阅读这本书之前，请确保你熟悉`console.log`的用法和用途。

当 jsFiddle 和 Firebug lite-dev 导致 JavaScript 出现复杂问题时，可以使用 JS Bin 和 Firebug Lite-dev。我尝试通过使用 Firebug lite-dev 来避免依赖浏览器控制台，但在某些代码示例中，解决方案本身会干扰代码的执行。在这种情况下，必须利用 Web 浏览器内置的控制台输出日志。如果你没有使用内置 JavaScript 控制台的浏览器，我建议升级或切换浏览器。

使用 JS Bin 时，请记住代码必须手动执行（点击"Render"），这与 jsFiddle 的页面加载自动执行方式不同。

## 第1章 - JavaScript 对象

### 创建对象

在 JavaScript 中，对象是一切的核心：几乎所有内容都是对象，或者表现得像对象。理解了对象，你就理解了 JavaScript。所以，让我们来看 JavaScript 中对象的创建。

对象仅仅是具命名值（又称为属性）集合的容器。在查看任何 JavaScript 代码之前，让我们先进行逻辑推导。以我为例，用通俗的语言，我们可以用表格表示一个"cody"：

| 属性 | 属性值 |
| :--- | :--- |
| living | true |
| age | 33 |
| gender | male |

上表中的"cody"一词只是属性名及其对应值组的标签，这些值共同构成了 cody 的真面。正如从表中看到的，我是活着的（living），33岁，且是男性（male）。

然而，JavaScript 并不用表格来交流。它使用对象进行交流，而对象与"cody"表格中包含的部分相似。将上述表格转换为实际的 JavaScript 对象看起来如下：

> 实时运行代码：http://jsfiddle.net/javascriptlightening/ckVA5/

```html
<!DOCTYPE html><html lang="en"><body><script>
// 创建 cody 对象...
var cody = new Object();

// 然后用属性填充 cody 对象（使用点符号表示法）
cody.living = true;
cody.age = 33;
cody.gender = 'male';
console.log(cody); // 记录 Object {living = true, age = 33, gender = 'male'}
</script</body</html>
```

请牢记这一点：对象本质上只是属性的容器，每个属性都有一个名称和一个值。这种带有命名值的属性容器的概念（即对象）被 JavaScript 用作在 JavaScript 中表示值的构建块。cody 对象是一个值，我通过创建一个对象、给该对象命名并赋予其属性，将其以 JavaScript 对象的形式表达出来。

到目前为止，我们讨论的 cody 对象只有静态信息。由于我们处理的是编程语言，我们希望编写我们的 cody 对象来执行某些操作。否则，我们拥有的仅仅是一个类似于 JSON 的数据库。为了让 cody 对象活起来，我需要添加一个属性方法（Property method）。属性方法执行一个函数。具体来说，在 JavaScript 中，包含`Function()`对象的方法，其意图是对其中包含的函数进行操作。

如果我为 cody 表格更新一个`getGender`方法，用通俗的语言描述看起来是这样：

| 属性 | 属性值 |
| :--- | :--- |
| living | true |
| age | 33 |
| gender | male |
| getGender | [function] |

`String()`构造函数可以产生字符串对象。`Person()`构造函数同样强大，其灵活性与原生的`String()`构造函数或 JavaScript 中的任何原生构造函数并不相上下。

记得我们最初看到的`cody`对象是通过`Object()`产生的吗。需要注意的是，`Object()`构造函数和上一个代码示例所示的`new Person()`构造函数可以提供具有相同属性和属性方法的相同对象。检查下面的两部分代码，它们证明了`codyA`和`codyB`具有相同的对象值，尽管它们的生成方式不同。

```html
<!DOCTYPE html><html lang="en"><body><script>
// 使用 Object() 构造函数创建一个 cody 对象
var codyA = new Object();
codyA.living = true;
codyA.age = 33;
codyA.gender = 'male';
codyA.getGender = function() {return codyA.gender};

console.log(codyA); // logs Object {living=true, age=33, gender="male", ...}

/* 在下方创建了相同的 cody 对象，但不是使用原生的 Object()
构造函数来创建一个一次性的 cody，而是先定义了自己的 Person() 构造函数，它可以
创建一个 cody 对象（以及任何我们喜欢的 Person 对象），然后用
"new" 来实例化它。 */

var Person = function(living, age, gender) {
  this.living = living;
  this.age = age;
  this.gender = gender;
  this.getGender = function() {return this.gender};
};

// logs Object {living=true, age=33, gender="male", ...}
codyB = new Person(true, 33, 'male');

console.log(codyB);
</script</body</html>
```

`codyA`和`codyB`对象之间的主要区别于对象本身，而在于用于生成它们的构造函数。`codyA`对象是通过`Object()`构造函数的实例产生的。构建`codyB`的`Person()`构造函数也可以被用作强大的、集中式定义的对象"工厂"，用于创建更多的`Person()`对象。为生产自定义对象构建自己的构造函数还为`Person`实例设置了原型继承。

这两种解决方案都创建了相同的复杂对象。这两种模式是构建对象最常用的模式。

JavaScript 实际上是一门预装了几个原生构造函数的语言，这些构造函数用于产生表示非常特定类型值（例如：数字、字符串、函数、对象、数组……）的复杂对象，同时也通过`Function()`对象提供原材料，用于刻画用户定义的对象构造函数（例如：`Person()`）。最终结果——无论创建对象的模式如何——通常都是创建一个复杂对象。

理解对象的创建、本质和用法，以及它们的原始等价物，是本书其余部分的重点。

## JavaScript 构造函数构建并返回对象实例

构造函数的作用是创建多个共享某些特质和行为的对象。基本上，构造函数就像一个饼干模具，用于生产具有默认属性和属性方法的对象。

如果你说："构造函数仅仅是一个函数，"那么我会回答："你是对的——除非该函数使用`new`关键字被调用（例如：`new String('foo')`）。当这种情况发生时，函数就承担了一个特殊的角色，JavaScript 将该函数视为将`this`的值设置为正在构造的新对象。除了这种特殊行为外，该函数默认会在值`false`内部返回新创建的对象（即`this`）。从函数返回的新对象被认为是构造它的该值函数的实例。

再次考虑`Person()`构造函数，但这次阅读下面的代码注释，它们突显了`new`关键字的效果。

```html
<!DOCTYPE html><html lang="en"><body><script>
/* Person 是一个构造函数。它的编写意图是配合 new 关键字使用。 */
var Person = function(living, age, gender) {
  // "this" 下方是正在创建的新对象（即 this = new Object()）
  this.living = living;
  this.age = age;
  this.gender = gender;
  this.getGender = function() {return this.gender};
  // 当使用 new 关键字调用函数时，返回的是而不是 false
  // 实例化名为 cody 的 Person 对象
  var cody = new Person(true, 33, 'male');

  // cody 是一个对象以及 Person 的实例
  console.log(typeof cody); // logs object
  // 打印 cody 的内部属性和值
  console.log(cody); // logs Object
  console.log(cody.constructor); // logs Person()
};
</script</body</html>
```

上述代码利用了用户定义的构造函数（即`Person()`）来创建`cody`对象。这与`Array()`构造函数创建对象不同：

```html
<!DOCTYPE html><html lang="en"><body><script>
// 实例化名为 myArray 的 Array 对象
var myArray = new Array(); // myArray 是 Array 的实例

// myArray 是一个对象以及 Array 的实例
console.log(typeof myArray); // logs object!
console.log(myArray); // logs []

console.log(myArray.constructor); // logs Array()
</script</body</html>
```

在 JavaScript 中，大多数值（排除原始值）都涉及从构造函数创建或实例化的对象。从构造函数返回的对象被称为实例。请确保你熟悉这些语义，以及利用构造函数来构建对象的模式。

## JavaScript 原生/内置对象构造函数

JavaScript 语言包含了九个原生（或内置）构造函数。这些对象被 JavaScript 用于构建语言，我所说的"构建"是指这些对象被用于在 JavaScript 代码中表示值。因此，原生构造函数是多功能的，它们既产生对象，又在作为构造函数调用时用于创建其他对象。下面列出了 JavaScript 预装的九个构造函数：

- `Number()`
- `String()`
- `Boolean()`
- `Object()`
- `Array()`
- `Function()`
- `Date()`
- `RegExp()`
- `Error()`

JavaScript 大部分基于这九个对象（以及字符串、数字和布尔值）。详细了解这些对象是利用 JavaScript 独特力量和灵活性的关键。

> 注意
>
> Math 对象是一个例外。它是一个静态对象，而不是构造函数，意味着你不能这样做：`var x = new Math()`。你可以使用已经实例化的它（例如：`Math.PI`）。实际上，Math 只是由 JavaScript 设置的用于存放函数的对象。
>
> 原生对象有时被称为"全局对象"，因为它们是 JavaScript 可供使用的对象。不要将"对象"这一术语与全局对象混淆，例如所有浏览器中的`window`对象。
>
> `Number()`、`String()`和`Boolean()`构造函数不仅构建对象，还根据利用构造函数的方式为字符串、数字和布尔提供原始值。如果你直接调用这些构造函数，返回的是一个复杂对象。如果你在代码中简单地表示数字、字符串或布尔值（原始值，如`5`、`"foo"`和`true`），那么构造函数将返回原始值而不是复杂对象值。

## 用户定义的/非原生对象构造函数

正如你在`Person()`构造函数看到的那样，我们可以编写自己的构造函数，从中产生多个自定义对象。

下面我展示了`Person()`构造函数：

```html
<!DOCTYPE html><html lang="en"><body><script>
var Person = function(living, age, gender) {
  this.living = living;
  this.age = age;
  this.gender = gender;
  this.getGender = function() {return this.gender};
};

var cody = new Person(true, 33, 'male');
console.log(cody); // Object (living=true, age=33, gender="male", ...)

var lisa = new Person(true, 34, 'female');
console.log(lisa); // Object (living=true, age=34, gender="female", ...)
</script</body</html>
```

如你所见，通过传递参数和调用`Person()`构造函数，你可以轻松地创建大量唯一的人对象。当你需要两个或三个具有相同属性但不同值的对象时，这非常有用。正因为如此，这正是 JavaScript 对原生对象所做的事情。`Person()`构造函数遵循与`Array()`构造函数相同的原理。因此，`new Array('foo', 'bar')`与`new Person(true, 33, 'male')`没有区别。创建自己的构造函数只是使用了 JavaScript 用于其自身的原生构造函数时相同的模式。

- 它不是强制的，在创建自定义构造函数时使用`new`关键字，但最佳实践是将构造函数名称的第一个字母大写：`Person()`而不是`person()`。

## 使用 new 运算符实例化构造函数

构造函数基本上是一个用于创建预配置对象的"切饼干模具"模板。以`String()`为例。该函数在配合`new`运算符使用时（如`new String('foo')`），会创建一个基于`String()`模板的字符串实例。让我们来看一个例子。

> 实时运行代码：http://jsfiddle.net/javascriptlightenment/FKdjsp/

```html
<!DOCTYPE html><html lang="en"><body><script>
var myString = new String('foo');
console.log(myString); // logs foo {0 = "f", 1 = "o", 2 = "o"}
</script</body</html>
```

上面，我们创建了一个`String()`构造函数实例的新字符串对象。就这样这样，我们得到了一个在 JavaScript 中表示的字符串值。

> Notes
>
> 我并不是建议你使用构造函数来代替它们的字面量/原始等价物——例如`var string="foo";`。然而，我建议你理解字面量/原始值背后发生了什么。

如前所述，JavaScript 语言具有以下原生构造函数：`Number()`、`String()`、`Boolean()`、`Object()`、`Array()`、`Function()`、`Date()`、`RegExp()`、`Error()`。我们可以通过`new`运算符从这些任何构造函数实例化对象。下面，我构造了这九个原生 JavaScript 对象。

> 实时运行代码：http://jsfiddle.net/javascriptlightenment/M9cWA/

```html
<!DOCTYPE html><html lang="en"><body><script>
// 使用 new 为每个原生构造函数实例化
var myNumber = new Number(23);
var myString = new String('male');
var myBoolean = new Boolean(false);
var myObject = new Object();
var myArray = new Array('foo', 'bar');
var myFunction = new Function("x", "y", "return x+y");
var myDate = new Date();
var myRegExp = new RegExp('[a-z]+\b');
var myError = new Error('Crap!');

// 验证哪个构造函数创建了对象
console.log(myNumber.constructor); // logs Number
console.log(myString.constructor); // logs String
console.log(myBoolean.constructor); // logs Boolean
console.log(myObject.constructor); // logs Object
console.log(myArray.constructor); // logs Array(), in modern browsers
console.log(myFunction.constructor); // logs Function
console.log(myDate.constructor); // logs Date()
console.log(myRegExp.constructor); // logs RegExp()
console.log(myError.constructor); // logs Error
</script</body</html>
```

通过使用`new`运算符，我们告诉 JavaScript 解释器我们想要一个对应对应构造函数的实例对象。在上面的例子中，`Date()`构造函数被用于创建日期对象。`Date()`构造函数是日期对象的切饼模具。也就是说，它根据`Date()`构造函数定义的默认模式产生对象。

到此时，你应该已经非常熟悉从原生构造函数（例如`new String('foo')`）和用户定义的构造函数（例如`new Person(true, 33, 'male')`）创建对象。

> Notes
>
> 请记住`Math`是一个静态对象——其他方法的容器——它不是一个使用`new`运算符的构造函数。

## 从构造函数创建简写/字面量值

JavaScript 提供了快捷方式——称为"字面量"——用于制造原生对象值，而无需使用`new Foo()`或`new Bar()`。在大多数情况下，字面量语法实现的实现与使用`new`运算符相同。例外是：`Number()`、`String()`和`Boolean()`——见下文注释。

如果你来自其他编程背景，你可能更熟悉用字面量创建对象。我使用`new`运算符实例化原生 JavaScript 构造函数，并创建对应的字面量等价物。

```html
<!DOCTYPE html><html lang="en"><body><script>
var myNumber = Number(23); // an object
var myString = String('male'); // an object
var myBoolean = Boolean(false); // an object
var myObject = new Object(); // an object
var myArray = new Array('foo', 'bar'); // an object
var myFunction = new Function("x", "y", "return x+y"); // an object
var myDate = new Date(); // an object
var myRegExp = new RegExp('[a-z]+\b'); // an object
var myError = new Error('Crap!'); // an object

// 字面量形式
var myNumberLiteral = 23; // primitive value
var myStringLiteral = 'male'; // primitive string
var myBooleanLiteral = false; // primitive boolean
var myObjectLiteral = {}; // primitive object
var myArrayLiteral = ['foo', 'bar']; // primitive array
var myFunctionLiteral = function(x, y) { return x+y }; // primitive function
var myDateLiteral = new Date(); // primitive date
var myRegExpLiteral = /[a-z]+\b/; // primitive regexp
var myErrorLiteral = new Error('Crap!'); // primitive error
</script</body</html>
```

你从中获得的是：通常情况下，与使用`new`运算符的底层过程是相同的。更重要的是，字符串、数字和布尔值的情况要复杂得多。在这些情况中，字面量具有原始值的特征而非复杂对象。

- 使用字符串、数字和布尔字面量时，在值被视为对象之前，永远创建实际对象。换句话说，直到你使用与构造函数相关的方法（例如`foo = 'foo'.length`），JavaScript 会在后台创建一个包装对象，允许该值被视为对象。这澄清了误解。

### 原始（即简单）值

JavaScript 值`foo`、`true`、`false`以及`null`和`undefined`被视为原始值，因为它们是不可还原的。也就是说，数字是数字，字符串是字符串，布尔是`true`或`false`，而`null`和`undefined`仅仅如此，不代表其他值。

检查下面的代码并问自己字符串、数字、`null`和`undefined`值是否可以复杂。将其与你熟悉的`Object()`或`Array()`或任何复杂对象进行对比。

> 实时运行代码：http://jsfiddle.net/javascriptlightenment/xUQTC/

```html
<!DOCTYPE html><html lang="en"><body><script>
var myString = 'string';
var myNumber = 10;
var myBoolean = false; // could be true or false, but that is
var myNull = null;
var myUndefined = undefined;

console.log(myString, myNumber, myBoolean, myNull, myUndefined);

/* 考虑复杂对象或数组可以由多个原始值组成，从而变成一组多个值。 */
var myObject = {
  myString: 'string',
  myNumber: 10,
  myBoolean: false,
  myNull: null,
  myUndefined: undefined
};
console.log(myObject);

var myArray = ['string', 10, false, null, undefined];
console.log(myArray);
</script</body</html>
```

简单来说，原始值代表 JavaScript 中可用数据/信息的最低形式（即最简单的）。

> Notes
>
> - 与字面量语法创建值不同，当使用`new`关键字创建`String()`、`Number()`或`Boolean()`值时，创建的是复杂对象。
>
> - 关键是要理解`String()`、`Number()`和`Boolean()`构造函数是双用途构造函数，用于创建字面量/原始值以及复杂值。这些构造函数并不总是返回对象，相反，当不使用`new`运算符时，可以返回实际复杂值的原始表示。

### 原始值 `null`、`undefined`、`"string"`、`10`、`true` 和 `false` 不是对象

`null`和`undefined`值是琐碎的值，不需要构造函数，也不需要使用`new`运算符将它们建立为 JavaScript 值。使用`null`或`undefined`只需要像测试对象一样测试它们即可。剩余的原始值字符串、数字和布尔虽然技术上是从构造函数返回的，但不是对象。

下面，我对比原始值与其他原生 JavaScript 对象的区别。

> 实时运行代码：http://jsfiddle.net/javascriptlightenment/ZwqGoD/

```html
<!DOCTYPE html><html lang="en"><body><script>
// 产生原始值时不创建对象，注意没有使用 "new" 关键字
var primitiveString1 = "foo";
var primitiveString2 = String('foo');
var primitiveNumber1 = 10;
var primitiveNumber2 = Number('10');
var primitiveBoolean1 = true;
var primitiveBoolean2 = Boolean('true');

// 确认类型不是对象
console.log(typeof primitiveString1); // 'string'
console.log(typeof primitiveNumber1, typeof primitiveNumber2); // 'number,number'
console.log(typeof primitiveBoolean1, typeof primitiveBoolean2); // 'boolean,boolean'

// 与使用构造函数和 new 创建对象相比
var myNumber = Number(23);
var myString = new String('male');
var myBoolean = new Boolean(false);
var myObject = new Object();
var myArray = new Array('foo', 'bar');
var myFunction = new Function('x', 'y', 'return x * y');
var myDate = new Date();
var myRegExp = new RegExp('\bt[a-z]+\b');
var myError = new Error('Crap!');

// 记录 'object object object object object function function object object object'
console.log(
  typeof Number,
  typeof String,
  typeof Boolean,
  typeof Object,
  typeof Array,
  typeof Function, // 注意：typeof 对所有函数对象返回 function
  typeof Date,
  typeof RegExp, // 注意：typeof 对 RegExp() 返回 function
  typeof Error
);
</script</body</html>
```

我想从前面的代码示例中了解到，基本类型值（primitive values）不是对象。基本类型是特殊的，因为它们被用来表示简单的值。

### 基本类型在 JavaScript 中是如何存储/复制的

理解基本类型是按"面值"存储和操作的非常重要的。这听起来可能很简单，但这意味着如果我在变量`myString`中存储字符串值`"foo"`，那么值`"foo"`就会被字面地存储在内存中。为什么这很重要？一旦你开始操作（例如复制）值，你就必须具备这种知识，因为基本类型是按字面值复制的。

在下面的示例中，我们在变量`myStringCopy`中存储了字符串值（`"foo"`）的副本，它的值被字面地复制了。即使我们更改了原始值，由变量`myStringCopy`引用的复制值也保持不变。

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>
var myString = 'foo'; // 创建一个基本字符串
var myStringCopy = myString; // 将其值复制到一个新变量

var myString = null; // 修改存储在 myString 变量中的值

/* 从 myString 复制到 myCopy 的原始值。这通过更新
myString 的值然后检查 myCopy 的值来确认*/

console.log(myString, myCopy); // 记录 'null foo'
</script>
</body>
</html>
```

这里的收获是，基本类型作为不可归约的值被存储和操作的。引用它们的值。在上面的示例中，我们将`myString`值复制、克隆到变量`myStringCopy`中。当我们更新`myString`值时，`myCopy`值仍然拥有旧的`myString`值的副本。记住这一点，并将此处的机制与复杂对象（下文将讨论）进行对比。

### 基本类型按值相等

基本类型可以通过比较来检查它们的值在字面上是否完全相同。正如逻辑推导的那样，如果你比较一个包含数值`10`的变量与另一个包含数值`10`的变量，JavaScript 将认为它们是相等的，10 等同于 10（即`10 === 10`）。同样地，如果你比较基本字符串`foo`和另一个值为`'foo'`的基本字符串，这种情况也适用。比较结果将根据它们的值认为它们是相等的（即`'foo' === 'foo'`）。

在代码中，我使用基本数字演示了"按值相等"的概念，并与复杂数字对象进行了对比。

> 实时运行代码：http://jsfiddle.net/javascriptenlightenment/NewQU/

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>
var price1 = 10;
var price2 = 10;
var price3 = new Number('10'); // 一个复杂数字对象，因为使用了 new
var price4 = price3;

console.log(price1 === price2);

/* 记录 false 因为 price3 包含一个复杂数字对象而 price1 是一个基本值 */
console.log(price1 === price3);

// 记录 true 因为复杂值是按引用相等，而不是按值相等
console.log(price4 === price3);

// 如果我们更新 price4 变量包含一个基本值会怎样？
price4 = 10;

console.log(price4 === price3); // 记录 false：price4 现在是基本类型而非复杂的
</script>
</body>
</html>
```

结论是，基本类型在比较时，会检查所表达的值是否相等。当使用`new`关键字创建字符串、数字或布尔值（例如`new Number('10')`）时，该值不再是基本类型。作为比较，其结果并不像通过字面量创建的值。这并不意外，因为基本类型按值存储的（即`10 === 10`），而复杂值按引用存储的（即`price3`和`price4`包含同一个值的引用）。

### 字符串、数字和布尔基本类型在像对象一样使用时像对象

当基本类型被用作由构造函数创建的对象时，JavaScript 会根据当前的表达式将其转换为对象，但丢弃对象的特性并变回基本类型。在下面的代码中，我使用了基本类型并展示了当它们被视为对象时会发生什么。

> 实时运行代码：http://jsfiddle.net/javascriptlightenment/

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script>
var myString = 'foo'; // 创建一个基本字符串
var myStringCopy = myString; // 将其值复制到一个新变量

var myString = null; // 修改存储在 myString 变量中的值

/* 从 myString 复制到 myCopy 的原始值。这通过更新
myString 的值然后检查 myCopy 的值来确认*/

console.log(myString, myCopy); // 记录 'null foo'
</script>
</body>
</html>
```

对内存栈中对象的引用。在我们的代码示例中，`myObject`和`copyOfMyObject`指向内存中存储的同一个对象。

这里的核心要点是，当你更改一个复杂值时——因为它是通过引用存储的——你改变了所有引用该复杂值的变量中所存储的值。在我们的代码示例中，当你更新任一变量中存储的对象时，`myObject`和`copyOfMyObject`都会随之改变。

> Notes
>
> - 当使用`new`关键字创建`String()`、`Number()`和`Boolean()`值，或者在后台将其转换为复杂对象时，这些值继续通过值存储/复制。因此，即使是原始值也可以被像复杂值一样对待，它们具有通过引用复制的特性。
>
> - 要真正复制一个对象，你必须从旧对象中提取值，并将它们注入到新对象中。

## 复杂对象通过引用相等

在比较复杂对象时，只有当它们引用同一个对象（即具有相同的地址）时，才是相等的。两个包含相同对象的变量彼此是不等的，因为它们实际上并没有指向同一个对象。

下面，`objectFoo`和`objectBar`具有相同的属性，并且实际上是相同的对象，但通过 JavaScript 询问它们是否相等，结果告诉我们并不相等。

```html
<!DOCTYPE html><html lang="en"><body><script>
var objectFoo = {name: 'same'};
var objectBar = {name: 'same'};

// logs false, JS 并不管它们是否相同且属于同一对象类型
console.log(objectFoo === objectBar);

// 如何衡量复杂对象的相等性
var objectA = {foo: 'bar'};
var objectB = objectA;

console.log(objectA === objectB); // logs true 因为它们引用了同一个对象
</script</body</html>
```

这里的要点是，指向内存中复杂对象的变量之所以相等，仅仅是因为它们使用了相同的"地址"。相反，两个独立创建的对象即使具有相同的类型并拥有完全相同的属性，它们也是不等的。

## 复杂对象具有动态属性

指向现有对象的新变量不会复制该对象。这就是为什么复杂对象有时被称为引用对象。一个复杂对象可以拥有任意数量的引用，即使该对象发生变化，这些引用也始终指向同一个对象。

```html
<!DOCTYPE html><html lang="en"><body><script>
var objA = {property: 'value'};
var pointer1 = objA;
var pointer2 = pointer1;

// 更新 objA.property，所有的引用 (pointer1 & pointer2) 都会更新
objA.property = null;

// logs 'null null' 因为 objA, pointer1 和 pointer2 都引用同一个对象
console.log(objA.property, pointer1.property, pointer2.property);
</script</body</html>
```

这允许了动态对象属性，因为你可以定义一个对象、创建引用，对象以及所有引用该对象的变量都会"获取"到该更新。

## 用于原始值和复杂值的 typeof 运算符

`typeof`运算符可以返回你正在处理的值的类型。它返回的值并不完全一致，或者说某些情况下不符合逻辑。以下代码展示了使用`typeof`运算符返回的值。




```html
<!DOCTYPE html><html lang="en"><body><script>
// 原始值
var myNull = null;
var myUndefined = undefined;
var primitiveString1 = "string";
var primitiveString2 = String('string');
var primitiveNumber1 = 10;
var primitiveNumber2 = Number('10');
var primitiveBoolean1 = true;
var primitiveBoolean2 = Boolean('true');

console.log(typeof myNull); // logs object? 什么？注意...
console.log(typeof myUndefined); // logs undefined
console.log(typeof primitiveString1, typeof primitiveString2); // logs string string
console.log(typeof primitiveNumber1, typeof primitiveNumber2); // logs number number
console.log(typeof primitiveBoolean1, typeof primitiveBoolean2); // logs boolean boolean

// 复杂值
var myNumber = new Number(23);
var myString = new String('male');
var myBoolean = new Boolean(false);
var myObject = new Object();
var myArray = new Array('foo', 'bar');
var myFunction = new Function('x', 'y', 'return x * y');
var myDate = new Date();
var myExp = new RegExp('\b[a-z]+\b');
var myError = new Error();

console.log(typeof myNumber); // logs object
console.log(typeof myString); // logs object
console.log(typeof myBoolean); // logs object
console.log(typeof myObject); // logs object
console.log(typeof myArray); // logs object
console.log(typeof myFunction); // logs function
console.log(typeof myDate); // logs object
console.log(typeof myExp); // logs regexp
console.log(typeof myError); // logs object
</script></body></html>
```

```javascript
myArray.constructor === Array,
myFunction.constructor === Function,
myFunction.constructor === Function,
myDate.constructor === Date,
RegExp.constructor === RegExp,
myRegExp.constructor === RegExp,
myError.constructor === Error
);
```

```html
</script></</html>
```

`constructor` 属性也适用于用户定义的构造函数。下面，我们定义了一个 `CustomConstructor()` 构造函数，然后使用 `new` 关键字调用该函数来生成一个对象。一旦得到了对象，我们就可以利用 `constructor` 属性。

实时代码：http://jsfiddle.net/javascriptlightenment/MDs2t/

```html
<!DOCTYPE html><html lang="en"><body><script>
var ConstructorCustomObject = function CustomConstructor() { return 'Wow!'; };
var instanceofCustomObject = new CustomConstructor();

// 打印树
console.log(instanceOfCustomObject.constructor === CustomConstructor);

// 返回对 CustomConstructor() 函数的引用
// 返回 'function() { return 'Wow!'; }'
console.log(instanceOfCustomObject.constructor);

</script></body></html>
```

## Notes

- 你可能会困惑，为什么在没有返回对象时，原始值也会指向构造函数。通过使用原始值，构造函数仍然会被调用，因此原始值与构造函数之间存在这种关系。然而，结果是一个原始值。

- 如果你希望 `constructor` 属性能够记录用户定义构造函数的实际名称，你必须给该构造函数一个实际的名称（例如：`var Person = function Person()`）。

## 验证对象是否是特定构造函数的实例

通过使用 `instanceof` 运算符，我们可以判断一个对象是否是特定构造函数的实例（返回 true 或 false）。

下面，我们正在验证实例 `InstanceOfCustomObject` 是否是 `CustomConstructor` 构造函数的实例。这对于用户定义的对象以及使用 `new` 运算符创建的原生对象同样有效。

实时代码：http://jsfiddle.net/javascriptlightenment/g9Th6/

```html
<!DOCTYPE html><html lang="en"><body><script>

// 用户定义的对象构造函数
var CustomConstructor = function (){this.foo = 'bar'}

// 实例化 CustomConstructor 的实例
var instanceOfCustomObject = new CustomConstructor();

console.log(instanceOfCustomObject instanceof CustomConstructor); // 打印 true

// 与原生对象的效果相同
console.log(new Array('foo') instanceof Array) // 打印 true

</script></body></html>
```

![](img/ad11d036d555f7d1771aeb8c30e67ba2_39_0.png)

- 处理 `instanceof` 运算符时需要注意的是，当你询问一个对象是否是所有继承自 `Object()` 构造函数的对象的实例时，它都会返回 true。

- 当处理利用对象包装器的原始值时，`instanceof` 运算符将返回 false（例如：`'foo' instanceof String // 返回 false`）。如果字符串 'foo' 是使用 `new` 运算符创建的，`instanceof` 运算符将返回 true。因此，请记住 `instanceof` 仅适用于复杂对象以及由返回对象的构造函数创建的实例。

![](img/ad11d036d555f7d1771aeb8c30e67ba2_39_1.png)

## 从构造函数创建的实例可以拥有自己的独立属性（又称实例属性）

在 JavaScript 中，对象可以随时被扩展（即动态属性）。如前提到的，准确来说，JavaScript 对象是可变对象。这意味着从构造函数创建的对象可以被添加属性。

下面，我从 `Array()` 构造函数创建了一个实例，然后为其添加了自己的属性。

实时代码：http://jsfiddle.net/javascriptlightenment/RuQJ/

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = new Array();
myArray.prop = 'test';

console.log(myArray.prop) // 打印 'test'

</script></body></html>
```

这可以通过 `Object()`、`RegExp()` 或任何其他非原始构造函数来实现——甚至是 `Boolean()`。

```html
实时代码：http://jsfiddle.net/javascriptenlightenment/Gnbf/
```

```html
<!DOCTYPE html><html lang="en"><body><script>

// 这可以使用任何实际产生对象的原生构造函数完成
var myString = new String();
var myNumber = new Number();
var myBoolean = new Boolean();
var myObject = new Object();
var myArray = new Array();
var myFunction = new Function();
var myRegExp = new RegExp();

</script></body></html>

```

```javascript
myFunction.myMath_PI = Math.PI;
myFunction.myError = new Error('Crap!');
```

```javascript
console.log(
  (myFunction, myFunction, myFunction.myArray, myFunction.myString, myFunction.myNumber,
  myFunction.myDate, myFunction.myExp, myFunction.null, myFunction.null, myFunction.myUndefined,
  myFunction.Object, myFunction.myMath_PI, myFunction.myError)
);
```

```html
<script></</body></html>
```

这里简单的结论是：复杂对象可以包含——或引用任何你可以在 JavaScript 中名义表示的内容。当你看到这些时不不应该惊讶，因为所有原生对象都是可变的。这同样适用于对象形式的 `String()`、`Number()` 和 `Boolean()` 值——即当它们使用 `new` 运算符创建时。

## 如何以对程序有益的方式封装复杂对象

`Object()`、`Array()` 和 `Function()` 对象可以包含其他复杂对象。下面，我将通过使用 `Object()` 对象构建对象树来演示这一点。

> 现场代码: http://jsfiddle.net/javascriptlightenment/mLYFe/

```html
<!DOCTYPE html><html lang="en"><<body><script>

// 使用对象进行封装，创建对象链
var object1_ = {
  object1_1: {
    object1_1_1: {foo: 'bar'},
    object1_1_2: {},
  },
  object1_2: {
    object1_2_i: {},
    object2_2_i: {},
  }
};

console.log(object1.object1_1.object1_1_1.foo); // 打印 'bar'

</script></</body>></html>
```

同样的操作可以通过 `Array()` 对象（即多维数组）或 `Function()` 对象完成。

> 现场代码: http://jsfiddle.net/javascriptlightenment/9J6Ya/

```html
<!DOCTYPE html><html lang="en"><body><script>

// 使用数组进行封装，创建多维数组链
var myArray = [[]]; // 一个空数组，嵌套一个空数组，再嵌套一个空数组

/* 这里是使用函数的封装示例：一个空函数嵌套一个空函数，再嵌套一个空函数。 */
var myFunction = function() {
  // 空
  var myFunction = function() {
    // 空
    var myFunction = function() {
      // 空
    }
  }
};

// 我们也可以变得疯狂并进行混合组合
var foo = [{bar: {say: function() {return 'hi'}}]];
console.log(foo[0].bar.say()); // 打印 'hi'

</script></</body>></html>
```

这里的主要结论是：复杂对象的设计是为了以一种对程序有益的方式封装其他对象。

## 使用点符号或中括号符号获取/设置/更新对象的属性

我们可以使用点表示法或中括号表示法获取、设置或更新对象的属性。

下面，我演示了点表示法，其实现方法是使用对象名后跟一个点，然后是要获取、设置或更新的属性（例如 `objectName.property`）。

![](img/ad11d036d555f7d1771aeb8c30e67ba2_44_0.png)

```html
<!DOCTYPE html><html lang="en"><body><script>

// 创建 Object() 对象
var cody = new Object();

// 设置属性
cody.living = true;
cody.age = 33;
cody.gender = 'male';
cody.getGender = function() {return cody.gender};

// 获取属性
console.log(
  cody.living,
  cody.age,
  cody.gender,
  cody.getGender()
); // 打印 'true 33 male male'

// 更新属性，与设置一样
cody.living = false;
cody.age = 99;
cody.gender = 'female';
cody.getGender = function() { return Gender = ' ' + cody.gender; }

console.log(cody);
```

```html
</script></</body>></html>
```

点表示法是获取、设置或更新对象属性最常用的符号。

中括号表示法除非需要，否则并不常用。下面，我用中括号表示法替换了上面使用的点表示法。对象名后跟一个左括号、属性名（带引号），然后是右括号：

![](img/ad11d036d555f7d1771aeb8c30e67ba2_45_0.png)

```html
<!DOCTYPE html><html lang="en"><body><script>

// 创建 cody Object 对象
var cody = new Object();

// 设置属性
cody['living'] = true;
cody['age'] = 33;
cody['gender'] = 'male';
cody['getGender'] = function() { return cody.gender; }

// 获取属性
console.log(
  cody['living'],
  cody['age'],
  cody['gender'],
  cody['getGender']() // 仅在结尾调用函数
); // 打印 'true 33 male male'

// 更新属性，与设置非常相似
cody['living'] = false;
cody['age'] = 99;
cody['gender'] = 'female';
cody['getGender'] = function() { return Gender = ' ' + cody.gender; }

console.log(cody);

</script></body></html>
```

当你需要访问属性键，并且必须处理一个包含代表属性名的字符串值的变量时，中括号表示法会非常有用。下面，我通过使用两个变量访问属性来演示中括号表示法相对于点表示法的优势，这两个变量组合后产生 `fooObject` 中包含的属性键的字符串版本。

> 现场代码: http://jsfiddle.net/javascriptenment/RQB6N/

```html
<!DOCTYPE html><html lang="en"><body><script>

var fooObject = {foo: 'bar'};

var string1 = 'foo';
var string2 = 'bar';

console.log(fooObject[string1 + string2]); // 打印 'bar'

</script></body></html>
```

此外，中括号表示法在获取无效标识符的属性时也很有用。我使用数字和保留关键字作为属性名（作为字符串是有效的），只有中括号表示法可以访问。

> 现场代码: http://jsfiddle.net/javascriptenment/D6N/

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = {'123':'zero','class'};

// 注意 'class' 是 JavaScript 中的一个关键字
console.log(myArray['123']); // 打印 'zero'

// 点表示法无法做到
// console.log(myArray.class);

</script></body></html
```

## 注意事项

- 因为对象可以包含其他对象，所以看到 `cody.object.object` 并不常见。这被称为对象链。

- 对象在 JavaScript 中是可变的，这意味着可以随时对其进行设置或更新。通过使用中括号表示法（例如 `cody['age']`），你可以模拟 JavaScript 中的关联数组。

- 如果属性在对象内部，你只需要使用 `()` 操作，例如 `cody.getGender()`。

## 删除对象

`delete` 运算符用于从对象中完全删除属性。下面，我们从 `foo` 对象中删除了 `bar` 属性。

> 现场代码: http://jsfiddle.net/javascriptenment/ZwgT/

```html
<!DOCTYPE html><html lang="en"><body><script>
var foo = { bar: 'bar' };
delete foo.bar;
console.log('bar' in foo); // 打印 false，因为 bar 已从 foo 中删除

</script></body>></html
```

## 注意事项

- 删除不在原型链上的属性。

- 删除是从对象中移除属性的唯一方法。将属性设置为 `undefined` 或 `null` 仅更改属性的值。它不会从对象中移除属性。

## 对象属性引用是如何解析的

如果你尝试访问未包含对象中的属性，JavaScript 将尝试使用原型链查找该属性或方法。下面，我创建一个数组，然后尝试访问一个未定义的属性 `foo`。你可能认为因为 `myArray.foo` 不是 `myArray` 对象的属性，JavaScript 会立即返回 `undefined`。但 JavaScript 在返回 `undefined` 之前会在另外两个地方（`Array.prototype` 然后是 `Object.prototype`）查找 `foo` 的值。

> 现场代码: http://jsfiddle.net/javascriptenment/DJC6E/

```html
<!DOCTYPE html><html lang="en"><body><script>
var myArray = [];

console.log(myArray.foo); // 打印 undefined

/* JS 会查找 Array.prototype.Array.prototype.foo，但那里没有。然后它会查找 Object.prototype，但那里也没有，所以返回了 undefined！ */
</script></body>></html
```

```javascript
var myArray = ['foo', 'bar'];

console.log(myArray.hasOwnProperty('join')); // logs false

<script></body></html>
```

不，它确实。我的 `myArray` 可以访问 `join()` 方法，就像它是它自己的属性一样。这里发生了什么？嗯，你观察到了原型链的作用。我们访问了一个属性，虽然该属性没有包含在 `myArray` 对象中，但 JavaScript可以在其他地方找到它。那个地方非常特殊。`Array()` 构造函数是由 JavaScript 创建的，而 `join()` 方法（以及其他方法）被作为 `Array()` 原型的属性添加的。

重申一下，如果你尝试访问一个不包含该属性的对象的属性，JavaScript 将在原型链中搜索该值。首先，它会查看创建该对象的构造函数（例如 `Array`），并检查原型（例如 `Array.prototype`）以查看是否可以找到该属性。如果第一个原型没有该属性，JavaScript 将继续沿链向上查找，直到初始构造函数之前。它可以一直持续到链的末端。

链在何结束？让我们再次检查这个示例，在 `myArray` 上调用 `toString()` 方法。

> live code: http://jsfiddle.net/javascriptenenment/vwMe/

```html
<!DOCTYPE html><html lang="en"><body><script>

// Array & Array.prototype 不包含 toString() 方法
var myArray = ['foo', 'bar'];

// toString() 实际上定义在 Object.prototype.toString() 上
console.log(myArray.toString()); // logs `foo,bar`

</script></body></html>
```

`toString()` 方法没有定义在 `myArray` 对象内部。因此，触发了原型链规则，JavaScript 在 `Array` 构造函数的原型属性（例如 `Array.prototype`）中查找该属性。那里没有，所以触发了链，我们在 `Object()` 原型属性（`Object.prototype`）中查找该属性。是的，找到了。如果没找到，JavaScript 将产生一个错误，说明该属性未定义。

由于所有原型属性都是对象，链的最后一个环节是 `Object.prototype`。没有其他构造函数原型属性可以被检查。

有一整章章节专门将原型链拆分为更小的部分，所以如果你完全没有理解，请阅读该章节并回到这个解释以巩固你的理解。通过这段关于主题的简短阅读，我希望你理解当找不到属性（并被视为 undefined）时，JavaScript 将查看多个原型对象以确定该属性是未定义的。查找总是会发生，而这个查找过程就是 JavaScript 处理继承的方式，就像属性查找一样简单。

## 使用 hasOwnProperty 验证对象属性不是来自原型链

虽然 `in` 运算符可以检查对象的属性，包括来自原型链的属性，但 `hasOwnProperty` 方法可以检查对象的某个并非来自原型链的属性。

下面，我们想知道 `myArray` 是否包含属性 `foo`，并且该属性不是从原型链继承的。为了做到这一点，我们询问 `myObject` 是否它拥有一个名为 `foo` 的属性。

```html
<!DOCTYPE html><html lang="en"><script>

var myObject = {foo: 'value'};

console.log(myObject.hasOwnProperty('foo')) // logs true

// 对比来自原型链的属性
console.log(myObject.hasOwnProperty('toString')); // logs false

</script></body></html>
```

当你需要确定属性是对象局部的还是从原型链继承的时，应该利用 `hasOwnProperty` 方法。

## 使用 in 运算符检查对象是否包含给定的属性

`in` 运算符用于验证（真或假）对象是否包含给定的属性。下面，我们正在检查 `foo` 是否是 `myObject` 中的一个属性。

```html
<!DOCTYPE html><html lang="en"><body><script>

var myWeb = {foo: 'value'};
console.log('foo' in myWeb); // logs true

</script></body></html>
```

你应该意识到，`in` 运算符不仅检查所引对象中包含的属性，还检查该对象通过原型链继承的属性。因此，属性查找规则适用，如果该属性不在当前对象中，将在原型链上进行搜索。

这意味着上述代码中的 `myObject` 实际上通过原型链包含了一个 `toString` 属性方法（`Object.prototype.toString`），即使我们从没有指定过它（例如 `myObject.toString = 'foo'`）。

```html
<!DOCTYPE html><html lang="en"><body><script>

var myObject = {foo: 'value'};
console.log('toString' in myObject); // logs true

</script></body></html>
```

在最后一个示例中，`toString` 属性字面上并不在 `myObject` 内部。然而，它继承自 `Object.prototype`，所以 `in` 运算符得出 `myObject` 确实拥有继承的 `toString()` 属性方法。

## 使用 for in 循环枚举（遍历）对象的属性

通过 `for in`，我们可以遍历对象中的每个属性。在下面的代码中，我们正在使用 `for in` 循环从 `cody` 对象中获取属性名。

```html
<!DOCTYPE html><html lang="en"><body><script>

var cody = {
age : 23,
gender : 'male'

for (var key in cody) { // key 是表示每个属性名的变量
// 避免来自原型链继承的属性
if (cody.hasOwnProperty(key)) {
  console.log(key);
}
}
</script></body></html>
```

## 注意事项

- `for in` 循环有一个缺点。它会访问来自原型链继承的属性。它会包含所遍历对象的任何属性。因此，如果这不是预期的结果，我们通常需要在循环中使用一个简单的语句来确保我们只访问特定的对象。这可以通过使用 `hasOwnProperty()` 方法来实现。

- 在循环中访问属性的顺序并不总是我们定义属性的顺序。只有可枚举的属性（即在遍历对象时可见）才会通过 `for in` 循环显示。例如，构造函数属性就不会显示。可以使用方法检查哪些属性是枚举的。

## 宿对象与原生对象

你应该意识到，执行 JavaScript 的环境（例如 浏览器）通常包含所谓的宿对象。宿对象不是 ECMAScript 实现的一部分，但在执行期间可用的。当然，宿对象的可用性完全取决于宿环境提供了什么。

例如，宿环境中的 `window` 对象被视为宿对象。下面，我检查 `window` 的属性。

> live code: http://jsfiddle.net/javascriptenen/zn4Y/

```html
<!DOCTYPE html><html lang="en"><body><script>

for (x in window) {
console.log(x); // logs window 的所有属性
}
</script></body></html>
```

你注意到原生对象不在宿对象的列表中。浏览器区分宿对象和原生对象是非常常见的。

对于 浏览器而言，最著名的宿对象是用于处理 HTML 文档的接口，称为 DOM。下面，是列出浏览器提供的 `window.document` 对象内部所有对象的方法。

> live code: http://jsfiddle.net/javascriptlight/ITS7X/

```html
<!DOCTYPE html><html lang="en"><body><script>
for (x in window.document) {
  console.log();
}
</script></body></html>
```

我想让你的是，JavaScript 规范并不关心宿对象，反之亦然。

## 使用 Underscore.js 增强和扩展对象

JavaScript 1.5 在需要认真管理和处理对象时显得欠缺。如果你在浏览器中运行 JavaScript，我想大胆地建议使用 Underscore.js。

当你需要比 JavaScript 1.5 提供的更多功能时，Underscore.js 在处理对象时提供了以下功能。

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

- `isNumber`

- `isBoolean`

- `isDate`

- `isRegExp`

- `isNaN`

- `isNull`

- `isUndefined`

我喜欢这个库，因为它在浏览器支持时利用了 JavaScript 的新原生特性，但同时也为不支持特性的浏览器提供了相同的功能，且在非必要的情况下绝不会修改 JavaScript 的原生实现。

## Notes

- 在开始使用 Underscore.js 之前，请确保你所需的功能尚未由代码中可能使用的 JavaScript 库或框架提供。

## 第3章 - Object()

## 使用 Object() 对象的概念概述

使用内置的 `Object()` 构造函数，我们可以动态创建通用的空对象。事实上，如果你记得第 1 章的开头，这正是我们创建 `cody` 对象时所做的。让我们重新创建 `cody` 对象。

![](img/ad11d036d555f7d1771aeb8c30e67ba2_56_0.png)

```
<!DOCTYPE html lang="en"><body><script>
var cody = new Object(); // 创建一个没有任何属性的空对象

for (key in cody) { // 确认 cody 是一个空通用对象
if(cody.hasOwnProperty(key)) {
  console.log(key); // 不应该看到任何日志，因为 cody 本身没有属性
}
}
</script></body></html>
```

在这里，我们只是使用 `Object()` 构造函数创建一个名为 cody 的通用对象。你可以将 `Object()` 构造函数比作用于创建没有预定义属性或方法的空对象的模具（当然，除了那些继承自原型链的属性）。

## Notes

- 如果你不显而易见，`Object()` 构造函数本身就是一个对象。也就是说，该函数是基于从 `Function` 构造函数创建的对象。这可能会令人困惑。只需记住像 `Array` 构造函数一样，`Object` 构造函数只是放置空对象。你可以创建任何你喜欢的空对象。然而，创建一个像 cody 这样的空对象与你创建一个带有预定义属性的自定义构造函数是完全不同的。确保 cody 只是基于 `Object()` 构造函数的空对象。为了利用 JavaScript 的力量，你不仅需要学会如何从 `Object()` 创建空对象容器，还需要学会如何构建自己的对象“类”（例如 `Person()`），而不是只有 `Object()` 构造函数本身。

## Object() 参数

`Object()` 构造函数接受一个可选参数。该参数是你想要创建的值。如果你不提供参数，则将假设为 `null` 或 `undefined` 值。

```
<!DOCTYPE html><html lang="en"><body><script>

// 创建一个没有任何属性的空对象
var cod1 = new Object();
var cod2 = new Object(undefined);
var cod3 = new Object(null);

console.log(typeof cod1, typeof cod2, typeof cod3); // 记录 'object object object'

</script></body></html>
```

如果将基值 `null` 或 `undefined` 传递给 `Object` 构造函数，值将作为对象被创建。理论上，我们可以使用 `Object()` 构造函数来创建任何其他我们拥有构造函数的原生对象。我正是这么做的。

```
<!DOCTYPE html><html lang="en"><body><script>

/* 使用 Object() 构造函数创建字符串、数字、数组、函数、布尔和正则对象。 */

// 下方的日志确认了对象的创建
console.log(new Object('foo'));
console.log(new Object(1));
console.log(new Object({}));
console.log(new Object(function () {}));
console.log(new Object(true));
console.log(new Object('/[bt-z]+/b/));

/* 通过 Object() 构造函数创建字符串、数字、数组、函数、布尔和正则对象实例是极少见的。我只是在演示这是可以的 */

</script></body></html>
```

## Object() 属性和方法

`Object()` 对象具有以下属性（不包括继承的属性和方法）：

属性（例如 `Object.prototype`）：

- `prototype`

## Object() 对象实例属性和方法

`Object()` 对象的实例具有以下属性和方法（不包括继承的属性和方法）：

实例属性（例如 `var myObject = {}; myObject.constructor;`）：

- `constructor`

实例方法（例如 `var myObject = {}; myObject.toString();`）：

- `hasOwnProperty()`

- `isPrototypeOf()`

- `propertyIsEnumerable()`

- `toLocaleString()`

- `toString()`

- `valueOf()`

> Notes

- 原型链以 `Object.prototype` 结束，因此 `Object()` 的所有属性和方法（如上所示）都被所有 JavaScript 对象继承。

## 使用字面量创建 Object() 对象

字面量表示法意味着使用大括号实例化对象。回想第 1 章的开头，我们使用点符号法创建了 `cody` 对象。字面量法赋予了我们用更短代码创建包含定义属性的对象的能力。这实际上是 JavaScript 中创建对象的首选语法，因为其简洁且易读。

```javascript
<!DOCTYPE html><html lang="en"><body><script>

var cody = {
living: true,
age: 23,
gender: 'male',
getGender: function() {return cody.gender}
};

console.log(cody); // 记录 cody 对象和属性

</script></body></html
```

你应该意识到属性名也可以作为字符串指定：

![](img/ad11d036d555f7d1771aeb8c30e67ba2_59_0.png)

```javascript
<!DOCTYPE html><html lang="en"><body><script>

var cody = {
living: true,
age: 23,
gender: 'male',
getGender: function() {return cody.gender};
};
// 注意最后一个属性没有逗号

console.log(cody); // 记录 cody 对象和属性

</script></body>
```

除非属性名满足以下条件，否则没有必要将属性指定为字符串：

- 是保留关键字之一（例如 `class`）

- 包含空格或特殊字符（数字、字母、美元符号 ($) 或下线 (_)以外的任何字符）

- 以数字开头

## Notes

- 注意！对象的最后一个属性不应有逗号。这在某些 JavaScript 环境会导致错误。

## 所有对象都继承自 Object.prototype

JavaScript 中的 `Object()` 构造函数通过 `prototype` 属性是原型链的终点。

下面，我为 `Object.prototype` 增加了一个 `foo` 属性，然后创建一个字符串并尝试访问 `foo` 属性，仿佛它是字符串实例的属性。由于 `myString` 实例没有 `foo` 属性，原型链开始查找 `String.prototype`。那里没有，下一个查找位置是 `Object.prototype`，这是 JavaScript 查找对象值的最终位置。找到了 `foo` 值是因为我添加了它，然后返回 `foo` 的值。

```javascript
<!DOCTYPE html><html lang="en"><body><script>

Object.prototype.foo = 'foo';

var myString = 'bar';

// 通过原型链在 Object.prototype.foo 找到，记录 'foo'
console.log(myString.foo);

</script></body></html>
```

```
</script>
</body>
```

## Notes

- 注意！向 `Object.prototype` 添加的任何内容都将出现在 `for...in` 循环和原型链中。由于这一点，人们常说修改 `Object.prototype` 是禁止的，或者用某些人的话说说是 *verboten*。

## 使用 Function() 对象的概念概述

函数是代码语句的容器，可以使用括号 `()` 运算符进行调用。在调用期间，可以在括号内传递参数，以便函数在被调用时能够访问某些值。

下面，我们创建了两个版本的 `addNumbers` 函数对象——一个使用 `new` 运算符，另一个使用更常见的字面量模式。在每种情况下，我们通过括号 `()` 运算符传递参数并调用该函数。

![](img/ad11d036d555f7d1771aeb8c30e67ba2_62_0.png)

```html
<!DOCTYPE html><html lang="en"><<body><script>
var addNumbers = new Function('num1', 'num2', 'return num1 + num2');
console.log(addNumbers(2, 2)); // logs 4

// 也可以用字面量方式编写，这常见得多
var addNumbersB = function(num1, num2) { return num1 + num2 };

console.log(addNumbersB(2, 2)); // logs 4
</script></body></html>
```

函数可以用于返回值、构造对象，或作为简单运行代码的机制。JavaScript 对函数有多种用途，但在其最基本的形式，函数仅仅是一个可执行语句的唯一作用域。

## Function() 参数

`Function()` 构造函数接受无限数量的参数，但 `Function()` 构造函数预期的最后一个参数是一个包含函数体语句的字符串。在最后一个参数之前传递给构造函数的任何参数都将在创建的函数可用。也可以以逗号分隔的字符串形式发送多个参数。

下面，我对比了 `Function()` 构造函数的使用与实例化函数对象的更常见模式。

live code: http://jsfiddle.net/javascriptenlight/RT8QD/

```html
<!DOCTYPE html><html lang="en"><script>

var addFunction = new Function('num1', 'num2', 'return num1 + num2');

/* 另一种方式，逗号分隔的字符串参数可以
是构造函数的第一个参数，后面紧跟函数体。 */
var timesFunction = new Function('num1,num2', 'return num1 * num2');
console.log(addFunction(2,2),timesFunction(2,2)); // logs '4 4'

// 与实例化函数的常见模式对比
var addFunctionExpr = function(num1, num2) {return num1 + num2}; // 表达式形式
function addFunctionStmt(num1, num2) {return num1 + num2}; // 语句形式

</script></body></html>
```

## Notes

- 不建议直接利用 `Function()` 构造函数，通常也从未这样做，JavaScript 将使用 `eval()` 来解析包含函数逻辑的字符串。许多人认为 `eval()` 是不必要的开销。如果在使用，极可能是代码设计中的缺陷。

- 不使用 `new` 关键字使用 `Function()` 构造函数与仅使用构造函数创建函数对象的效果相同（例如 `new Function('x','return x')` 与 `function('x','return x')`）。

- 直接调用 `Function()` 构造函数时不会创建闭包（见第 7 章）。

## Function() 属性和方法

函数对象具有以下属性（不包括继承的属性和方法）：

属性（例如 `Function.prototype`）：

- `prototype`

### 函数对象实例属性和方法

函数对象实例具有以下属性和方法（不包括继承的属性和方法）：

实例属性（例如 `var myFunction = function(x, y, z) {}; myFunction.length;`）

- `arguments`

- `constructor`

- `length`

实例方法（例如 `var myFunction = function(x, y, z) {}; myFunction.toString();`）

- `apply()`

- `call()`

- `toString()`

## 函数总是返回一个值

虽然可以仅仅创建一个函数来执行代码语句，但函数返回一个值也非常常见的。下面，我们从 `sayHi` 函数返回一个字符串。

> code: http://jsfiddle.net/javascriptenenment/G6Q/

```html
<!DOCTYPE html><html lang="en"><body><script>
var sayHi = function() {
  return 'Hi';
}
console.log(sayHi()); // logs "Hi"
</script></body></html>
```

如果函数没有指定返回值，则返回 `undefined`。下面，我们调用了 `sayHi` 函数，它在没有显式返回值的情况下向控制台打印了 `undefined`。

> code: http://jsfiddle.net/javascriptenment/Lib/

```html
<!DOCTYPE html><html lang="en"><body><script>

var sayHi = function() {
  console.log('I am here!');
/* logs true 是因为总是返回一个值，即使我们没有专门返回一个 */
console.log(sayHi() === undefined);
</script></body></html>
```

结论是，函数会返回一个值，即使你没有提供一个要返回的值。如果你没有指定值，返回的值就是 `undefined`。

## 函数是一等公民（不仅仅是语法，而是值）

在 JavaScript 中，函数是对象。这意味着函数可以存储在变量、数组或对象中。此外，函数可以被传递给另一个函数，并从另一个函数返回。函数拥有属性是因为它是一个对象。这一切使得函数在 JavaScript 中成为一等公民。

> live code: http://jsfiddle.net/javascriptenment/2BT/

```html
<!DOCTYPE html><html lang="en"><body><script>

// 函数可以存储在变量 (funcA)、数组 (funcB) 和对象 (funcC) 中
var funcA = function(){}; // 调用方式: funcA()
var funcB = [function(){}]; // 调用方式: funcB()
var funcC = {method:function(){}}; // 调用方式: funcC['method']()

// 函数可以发送到函数，并从函数传回
var funcD = function(){
  return 'Hi';
};

var runFuncToFunc = funcD(function() { 

// 函数是对象，这意味着它们拥有属性
var funcE = function(){};
funcE.answer = 'yes'; // 实例属性
console.log(funcE.answer); // logs 'yes'

</script></body></html>
```

至关重要的是意识到函数是一个对象，因此它可以像其他值一样传递或增强。

## 传递给函数

参数是在调用函数时传递到函数作用域内的载体。

![](img/ad11d036d555f7d1771aeb8c30e67ba2_62_0.png)

```html
<!DOCTYPE html><html lang="en"><body><script>
var addFunction = function(num1, number2) {
  var sum = number1 + number2;
  return sum;
}
console.log(addFunction(3, 3)); // logs 6
</script></body></html>
```

注意事项

- 与其他编程语言相比，在 JavaScript 中省略参数是完全合法的，即使在定义函数时没有定义它们。

- 如果在定义函数时没有定义参数，也不会发生错误。

- `arguments` 对象是一个包含了所有传递给函数的参数的类数组对象。

## 所有函数可用的 arguments 值

在函数的作用域内是 `arguments` 值。

`arguments` 对象包含了所有传递给函数的参数。即使我们在调用函数时指定了参数，也可以依赖它们。

live code: http://jsfiddle.net/javascriptenment/R2z/

```html
<!DOCTYPE html><html lang="en"><body><script>

var add = function() {
    return arguments[0] + arguments[1];
}

console.log(add(4, 4)); // returns 8

</script></body></html>
```

`this` 关键字传递给所有函数，它是包含该函数的引用。正如你预期的，包含在对象属性中的函数（即方法）可以使用 `this` 获取“父级”对象的引用。当函数在全局作用域中定义时，`this` 的值是全局对象。查看下面的代码并确保你理解 `this` 返回的是什么。

live code: http://jsfiddle.net/javascriptenment/WFZW3/

```html
<!DOCTYPE html><html lang="en"><body><script>

var myObjectClass = {
    name: 'myObject',
    myMethod: function(){console.log(this)};
}

myObjectClass.myMethod(); // logs 'myObject'

var myObject2 = function(){console.log(this)};

myObject2(); // logs window

</script></body></html>
```

## arguments.callee 

`arguments` 对象有一个名为 `callee` 的属性，它是当前执行的函数的引用。该属性可以在函数作用域内引用该函数（例如 `arguments.callee` —— 自引用）。在下面的代码中，我们使用该属性来获取调用函数的引用。

live code: http://jsfiddle.net/javascriptenment/TdzVg/
```html

<!DOCTYPE html><html lang="en"><body><script>

var add = function() {

    return arguments.callee[0] + arguments.callee[1];

}

console.log(add(4, 4)); // returns 8

</script></body></html>

```



```html

<!DOCTYPE html><html lang="en"><body><script>

var foo = function foo() {

  console.log(arguments.callee); // logs foo()

  // callee could be used to invoke recursively the foo function (e.g. arguments.callee)

}

</script></body></html>

```

当函数需要递归调用时，这非常有用。

## 函数实例长度属性 & arguments.length

`arguments` 对象有一个独特的 `length` 属性。你可能认为这个属性返回的是定义的参数数量，但实际上它返回的是调用期间传递给函数的参数数量。

> 实时代码：http://jsfiddle.net/javascriptlightenment/ChbgD/

```html

<!DOCTYPE html><html lang="en"><body><script>

var myFunction = function(z, s, d) {

  return arguments.length;

}

console.log(myFunction()); // logs 0，因为没有向函数传递参数

</script></body></html>

```

通过使用所有 `Function()` 实例的 `length` 属性，我们实际上可以获取函数期望的参数总数。

> 实时代码：http://jsfiddle.net/javascriptlightenment/Uhjbb/

```html

<!DOCTYPE html><html lang="en"><body><script>

var myFunction = function(z, s, d, e, r, m, q) {

  return myFunction.length;

}

console.log(myFunction()); // logs 7

</script></body></html>

```

JavaScript 1.4 中的 `arguments.length` 属性已废弃，传递给函数的参数数量可以通过函数对象的 `length` 属性来访问。因此，从以后起，你可以利用 `callee` 属性首先获取对被调用函数的引用（即 `arguments.callee.length`），从而获取 `length` 值。

## 重新定义函数参数

函数的参数可以在直接它的函数内部重新定义，也可以通过使用 `arguments` 数组重新定义。看这段代码：

![](img/ad11d036d555f7d1771aeb8c30e67ba2_69_0.png)

```html

<!DOCTYPE html><html lang="en"><body><script>

var foo = false;

var bar = false;

var myFunction = function(foo, bar) {

  arguments[0] = true;

  bar = true;

  console.log(arguments[0], bar); // logs true true

}

myFunction();

</script></body></html>

```

注意，我可以使用 `arguments` 索引或直接为参数重新赋值新值来重新定义 `bar` 参数的值。

## 在函数完成之前返回一个函数（即取消函数执行）

在调用期间，可以在任何时候通过使用 `return` 关键字或不带任何值来取消函数。在下面，如果参数是 `undefined` 或不是数字，我们将取消 `add` 函数。

![](img/ad11d036d555f7d1771aeb8c30e67ba2_69_1.png)

```html

<!DOCTYPE html><html lang="en"><body><script>

var add = function(x, y) {

  // 如果参数不是数字，返回错误。

  if (typeof x !== 'number' || typeof y !== 'number') return 'pass in numbers';

  return x + y;

}

console.log(add(3,3)); // logs 6

console.log(add('2', '2')); // logs 'pass in numbers'

</script></body></html>

```

这里的要点是，你可以在函数执行的任何点使用 `return` 关键字来取消函数的执行。

## 定义函数（语句、表达式或构造函数）

函数可以通过三种不同的方式定义：函数构造函数、函数语句或函数表达式。下面，我演示了每种变体。

实时代码：http://jsfiddle.net/javascriptenlightenment/DLRak/

```html

<!DOCTYPE html><html lang="en"><script>

/* 函数构造函数：最后一个参数是函数逻辑，

在此之前的所有都是参数 */

var addConstructor = new Function('x', 'y', 'return x + y');

// 函数语句

function addStatement(x, y) {

  return x + y;

}

// 函数表达式

var addExpression = function(x, y) {

  return x + y;

}

console.log(addConstructor(2,2), addStatement(2,2), addExpression(2,2)); // logs '4 4 4'

</script></body></html>

```

- 有人说存在第四种函数定义类型，称为“命名函数表达式”。命名函数表达式仅仅是一个也包含名称的函数表达式（例如 `var add = function add(x, y) {return x+y});`）。

## 调用函数（函数、方法、构造函数或 call() & apply()）

函数通过四种不同的场景或模式被调用。

- 作为函数调用
- 作为方法调用
- 作为构造函数调用
- 使用 `apply()` 或 `call()`

在下面的代码中，我们检查了这些每种调用模式。

> 实时代码：http://jsfiddle.net/javascriptenenment/aqbQ9/

```html

<!DOCTYPE html><html lang="en"><body><script>

// function pattern

var myFunction = function(){return 'foo'};

console.log(myFunction()); // log 'foo'

// method pattern

// (原文代码片段不完整)

// constructor pattern

// (原文代码片段不完整)

// apply() or call() pattern

// (原文代码片段不完整)

</script></body></html>

```



# JavaScript 核心概念

## 函数

### 函数参数与 `arguments` 对象

在 JavaScript 1.4 中，`arguments.length` 属性已废弃。传递给函数的参数数量可以通过函数对象的 `length` 属性来访问。因此，你可以利用 `callee` 属性首先获取对被调用函数的引用（即 `arguments.callee.length`），从而获取 `length` 值。

```html
<!DOCTYPE html><html lang="en"><body><script>

var myFunction = function(z, s, d, e, r, m, q) {
  return myFunction.length;
}

console.log(myFunction()); // logs 7
</script></body></html>
```

### 重新定义函数参数

函数的参数可以在直接它的函数内部重新定义，也可以通过使用 `arguments` 数组重新定义。

```html
<!DOCTYPE html><html lang="en"><body><script>
var foo = false;
var bar = false;

var myFunction = function(foo, bar) {
  arguments[0] = true;
  bar = true;
  console.log(arguments[0], bar); // logs true true
}

myFunction();
</script></body></html>
```

注意，可以使用 `arguments` 索引或直接为参数重新赋值新值来重新定义 `bar` 参数的值。

### 在函数完成之前返回（取消函数执行）

在调用期间，可以在任何时候通过使用 `return` 关键字或不带任何值来取消函数。在下面的例子中，如果参数是 `undefined` 或不是数字，我们将取消 `add` 函数。

```html
<!DOCTYPE html><html lang="en"><body><script>

var add = function(x, y) {
  // 如果参数不是数字，返回错误。
  if (typeof x !== 'number' || typeof y !== 'number') return 'pass in numbers';
  return x + y;
}

console.log(add(3,3)); // logs 6
console.log(add('2', '2')); // logs 'pass in numbers'

</script></body></html>
```

这里的要点是，你可以在函数执行的任何点使用 `return` 关键字来取消函数的执行。

### 定义函数（语句、表达式或构造函数）

函数可以通过三种不同的方式定义：函数构造函数、函数语句或函数表达式。

```html
<!DOCTYPE html><html lang="en"><script>

/* 函数构造函数：最后一个参数是函数逻辑，
在此之前的所有都是参数 */
var addConstructor = new Function('x', 'y', 'return x + y');

// 函数语句
function addStatement(x, y) {
  return x + y;
}

// 函数表达式
var addExpression = function(x, y) {
  return x + y;
}

console.log(addConstructor(2,2), addStatement(2,2), addExpression(2,2)); // logs '4 4 4'

</script></body></html>
```

- 有人认为存在第四种函数定义类型，称为“命名函数表达式”。命名函数表达式仅仅是一个也包含名称的函数表达式（例如 `var add = function add(x, y) {return x+y};`）。

### 调用函数（函数、方法、构造函数或 `call()` & `apply()`）

函数通过四种不同的场景或模式被调用：

- 作为函数调用
- 作为方法调用
- 作为构造函数调用
- 使用 `apply()` 或 `call()`

```javascript
// 函数可以传递给函数，也可以从函数返回
var foo = function(f) {
  return f;
}

var bar = foo(function(){console.log('Hi');});

bar(); // 打印 'Hi'
```

当 `bar` 被调用时，它会调用传递给 `foo()` 函数的匿名函数，该匿名函数随后从 `foo()` 函数返回，并通过 `bar` 变量引用。这一切是为了展示函数可以像任何其他值一样被传递。

### 在定义之前调用函数语句（函数提升）

函数语句可以在执行过程中在其实际定义之前被调用。

```html
<!DOCTYPE html><html lang="en"><body><script>

// 示例 1
var speak = function() {
  // sayYo() 还没有定义，但仍然可以被调用，打印 'yo'
  function sayYo() {console.log('sayYo');}
};

// 示例 2
console.log(sum(2, 2)); // 调用 sum()，它尚未定义，但仍然可以被调用
function sum(x, y) {return x + y;}

</script></body></html>
```

这种情况发生在代码运行之前；函数语句会被解析并添加到执行栈/上下文中。

> **注意**：定义为“函数表达式”的函数不会被提升；只有“函数语句”会被提升。

### 函数可以调用自己（递归）

函数调用自己是完全合法的。

```html
<!DOCTYPE html><html lang="en"><body><script>
var countDownFrom = function countDownFrom(num) {
  num--; // 修改参数值
  if (num < 0) return false; // 如果 num < 0 则返回不带递归的函数
  // 如果是匿名函数，可以使用 arguments.callee(num)
  countDownFrom(num);
}
countDownFrom(5); // 启动函数，它分别打印 5,4,3,2,1,0
</script></body></html>
```

---

## 第 5 章 - 头/全局对象

### 头对象的概念概述

JavaScript 代码本身必须包含在一个对象中。例如，为浏览器环境编写 JavaScript 代码时，JavaScript 是包含并执行在 `window` 对象中的。这个 `window` 对象被认为是“头对象”，有时也混淆地称为“全局对象”。JavaScript 的所有实现都要求使用单个头对象。

```html
<!DOCTYPE html><body><script>

var myString = 'myString';
var myFunction = function() {};

console.log('myStringVar' in window); // 返回 true
console.log('myFunctionVar' in window); // 返回 true
console.log('myString' in window); // 返回 true
console.log('myFunction' in window); // 返回 true

</script></body></html>
```

> **注意**：头对象是 JavaScript 环境中可用的最高作用域/上下文。

### 头对象中的全局函数

JavaScript 自带了一些预定义函数。以下原生函数被视为头对象（例如在浏览器中的 `window`）的方法：

- `decodeURI()`
- `decodeURIComponent()`
- `encodeURI()`
- `encodeURIComponent()`
- `eval()`
- `isFinite()`
- `isNaN()`
- `parseFloat()`
- `parseInt()`

### 头对象 vs 全局属性和全局变量

不要将头对象与全局作用域内的全局属性或全局变量混淆。头对象是一个包含所有对象的对象。“全局属性”或“全局变量”术语用于指直接位于头对象内部的值。

```html
<!DOCTYPE html><html lang="en"><body><script>

var foo = 'bar';
var myFunction = function() { };

</script></body></html>
```

> **注意**：显式调用（例如 `window.alert()` 对比 `alert()`）在性能方面会稍微增加一点开销。如果你仅依赖作用域链并避免显式引用头对象，速度会更快。

---

## 第 6 章 - `this` 关键字

### `this` 的概念概述以及它如何引用对象

当一个函数被创建时，后台会创建一个名为 `this` 的关键字，它链接到函数运行所在的对象。

```html
<!DOCTYPE html><html lang="en"><body><script>
var cody = {
  living : true,
  age : 23,
  gender: 'male',
  getGender: function() { return cody.gender;};
}
console.log(cody.getGender()); // logs 'male'
</script></body></html>
```

可以使用 `this` 来重写访问 `cody` 对象，因为 `this` 指向 `cody` 对象。

```html
<!DOCTYPE html><html lang="en"><body><script>
var cody = {
  living: true,
  age: 23,
  gender: 'male',
  getGender: function() { return this.gender;};
}
console.log(cody.getGender()); // logs 'male'
</script></body></html>
```

> **注意**：
> - `this` 关键字看起来和行为像任何其他变量一样，但你不能修改它。
> - 与 `arguments` 和发送给函数的任何参数不同，`this` 是调用/激活上下文中的一个关键字（而不是属性）。

### `this` 的值是如何确定的？

传递给所有函数的 `this` 的值基于函数在运行时被调用的上下文。

```html
<!DOCTYPE html><html lang="en"><body><script>

var foo = 'foo';
var myObject = {foo: 'I am myObject.foo'};

var sayFoo = function() {
  console.log(this['foo']);
};

myObject.sayFoo = sayFoo;

myObject.sayFoo(); // logs I am myObject.foo
sayFoo(); // logs 'foo'

</script></body></html>
```

显然，`this` 的值基于函数被调用的上下文。

### `this` 关键字在嵌套函数中指向头对象

在 ECMA3 中，嵌套函数内部的 `this` 会迷失方向并指向头对象（浏览器中的 `window` 对象），而不是函数定义的对象。ECMAScript 5 修复了这个问题。

```html
<!DOCTYPE html><html lang="en"><body><script>
var myObject = {
 func1: function() {
  console.log(this); // logs myObject
 var func2 = function() {
  console.log(this); // logs window
  var func3 = function() {
   console.log(this); // logs window
   }
  }
 }
}
myObject.func1();
</script></body></html>
```

### 当函数使用 `new` 关键字调用时，`this` 指向实例

在构造函数中，我们可以在对象实际创建之前通过 `this` 来使用该对象。

```html
<!DOCTYPE html><html lang="en"><body><script>
var Person = function(name) {
  this.name = name || 'john doe'; // this 将引用所创建的实例
}

var cody = new Person('Cody Lindley');
console.log(cody.name); // 打印 Cody Lindley
</script></body></html>
```

如果我们没有使用 `new` 关键字，`this` 的值将是 `Person` 被调用的上下文——在这种情况下，是全局对象。

```html
<!DOCTYPE html><html lang="en"><body><script>
var Person = function(name) {
  this.name = name || 'john doe';
}

var cody = Person('Cody Lindley'); // 注意我们没有使用 'new'
console.log(cody.name); // undefined，值实际上设置在 window.name 上
console.log(window.name); // 打印 'Cody Lindley'
</script></body></html>
```

### 原型方法中的关键字 `this` 指向构造函数实例

当用于添加到构造函数 `prototype` 属性的函数时，`this` 指向调用方法的实例。

```html
<!DOCTYPE html><html lang="en"><body><script>
var Person = function(x){
  if(this.fullName = x);
}

Person.prototype.whatMyFullName = function(){
  return this.fullName; // 'this' 指向从 Person 创建的实例
}

var cody = new Person('cody lindley');
var lisa = new Person('lisa lindley');

console.log(cody.whatMyFullName(), lisa.whatMyFullName());

Object.prototype.fullName = 'John Doe';
var john = new Person(); // 没有传递参数，所以 fullName 不会被添加到实例中
console.log(john.whatMyFullName()); // 打印 'John Doe'
</script></body></html>
```

> **注意**：如果实例或 `this` 指向的对象不包含被引用的属性，将适用于任何属性查找的规则，该属性将在原型链上被“查找”。

---

## 第 7 章 - 作用域与闭包

### 作用域的概念概述

在 JavaScript 中，作用域是代码执行的上下文，共有三种作用域：全局作用域、函数作用域和 `eval` 作用域。JavaScript 遵循一条基于作用域层级结构的查找链。

```html
<!DOCTYPE html><html lang="en"><body><script>
var sayHiText = 'howdy';
var func1 = function() {
  var func2 = function() {
    console.log(sayHiText); // func2 作用域，但它在全局作用域找到了 sayHiText
  };
  func2();
};
func1();
</script></body></html>
```

### 作用域链查找返回第一个找到的值

```html
<!DOCTYPE html><html lang="en"><body><script>
var x = false;
var foo = function() {
  var x = false;
  bar = function() {
    var x = true;
    console.log(x); // 局部的 x 在作用域中优先，所以它遮蔽了其他的
  }
}
foo(); // 打印 true
</script></body></html>
```

### 作用域是在函数定义期间而非调用期间确定（词法作用域）

作用域链是根据函数定义时的位置决定的，而不是调用时。正因如此，我们可以创建闭包。

```html
<!DOCTYPE html><html lang="en"><body><script>

var parentFunction = function() {
  var foo = 'foo';
  return function() { // 返回匿名函数
    console.log(foo); // 打印 'foo'
  }
}

var nestedFunction = parentFunction();
nestedFunction(); // 打印 foo，因为返回的函数通过作用域链访问 foo

</script></body></html>
```

---

## 第 8 章 - 原型

### 原型在所有 `Function()` 实例上都是标准的

所有函数都是通过 `Function()` 构造函数创建的。当函数被创建时，它总是被赋予一个 `prototype` 属性，该属性是一个空对象。

```html
<!DOCTYPE html><html lang="en"><body><script>

var myFunction = function() {};
console.log(myFunction.prototype); // logs object
console.log(typeof myFunction.prototype); // logs 'object'

</script></body></html>
```

### 默认的原型属性是一个 `Object()` 对象

```html
<!DOCTYPE html><html lang="en"><body><script>

var myFunction = function() {};
myFunction.prototype = {}; // add the prototype property and set it to an empty object
console.log(myFunction.prototype); // logs an empty object

</script></body></html>
```

> **注意**：`prototype` 属性的值可以设置为 JavaScript 中提供的任何复杂值（即对象）。JavaScript 将忽略任何设置为原始值的 `prototype` 属性。

### 从构造函数创建的实例与构造函数的 `prototype` 属性相连

原型链将每个实例连接到其构造函数的 `prototype` 属性。这个链接在实例内部被称为 `__proto__`。

```html
<!DOCTYPE html><html lang="en"><body><script>
// 此代码仅在支持 __proto__ 访问的浏览器中有效
Array.prototype.foo = 'foo';
var myArray = new Array();
console.log(myArray.__proto__.foo); // logs foo, because myArray.__proto__ = Array.prototype
</script></body></html>
```

也可以使用 `constructor` 属性追踪链接：

```html
<!DOCTYPE html><html lang="en"><body><script>
Array.prototype.foo = 'foo';
var myArray = new Array();
console.log(myArray.constructor.foo);
console.log(myArray.foo) // logs foo
</script></body></html>
```

### 原型链的终点是 `Object.prototype`

### 继承自原型属性的实例将始终获取最新值

`prototype` 属性是动态的。

```html
<!DOCTYPE html><html lang="en"><body><script>

var Foo = function Foo();
Foo.prototype.x = 1;
var FooInstance = new Foo();
console.log(FooInstance.x); //  logs 1
Foo.prototype.x = 2;
console.log(FooInstance.x); //  logs 2, FooInstance 已被更新
</script></body></html>
```

即使替换了默认原型对象，工作原理也是相同的：

```html
<!DOCTYPE html><html lang="en"><body><script>

var Foo = function Foo();
Foo.prototype = {x:1};
var FooInstance = new Foo();
console.log(FooInstance.x); //  logs 1
Foo.prototype.x = 2;
console.log(FooInstance.x); //  logs 2
</script></body></html>
```

### 用新对象替换 `prototype` 属性不会更新旧实例

```javascript
<!DOCTYPE html><html lang="en"><body><script>

var Foo = function Foo();
Foo.prototype.x = 1;
var FooInstance = new Foo();
console.log(FooInstance.x); //  logs 1

Foo.prototype = {x:2};
console.log(FooInstance.x); //  logs 1, 旧实例未更新

var NewFooInstance = new Foo();
console.log(NewFooInstance.x); //  logs 2, 新实例绑定新原型

</script></body></html>
```

### 用户定义的构造函数可以利用与原生构造函数相同的原型继承

```html
<!DOCTYPE html><html lang="en"><body><script>

var Person = function() {};
Person.prototype.legs = 2;
Person.prototype.arms = 2;
Person.prototype.countLims = function() {return this.legs + this.arms};

var chuck = new Person();
console.log(chuck.countLims()); //  logs 4
</script></body></html>
```

构造函数接收参数作为实例属性，未提供时回退到原型：

```html
<!DOCTYPE html><html lang="en"><body><script>

var Person = function(legs, arms) {
  if (legs !== undefined) {this.legs = legs;}
  if (arms !== undefined) {this.arms = arms;}
}

Person.prototype.legs = 2;
Person.prototype.arms = 2;
Person.prototype.countLims = function() {return this.legs + this.arms};

var chuck = new Person(0,0);
console.log(chuck.countLims()); //  logs 4
</script></body></html>
```

### 创建原型链（原始）

```html
<!DOCTYPE html><html lang="en"><body><script>

var Person = function() {this.bar = 'bar'};
Person.prototype.foo = 'foo';

var Chef = function() {this.goo = 'goo'};
Chef.prototype = new Person();

var cody = new Chef();

console.log(cody.foo); //  logs 'foo'
console.log(cody.goo); //  logs 'goo'
console.log(cody.bar); //  logs 'bar'

</script></body></html>
```

---

## 第 9 章 - `Array()`

### 使用 `Array()` 的概念概述

数组是一个有序的值列表，从索引零开始。数组使用数字作为查找键，而对象使用用户定义的属性名。

```html
<!DOCTYPE html><html lang="en"><body><script>

var myArray = ['blue', 'green', 'orange', 'red'];
console.log(myArray[0]); // logs blue

var myObject = { // 即关联数组/哈希，在 JavaScript 中称为对象
  blue: 'blue',
  green: 'green',
  orange: 'orange',
  red: 'red'
};
console.log(myObject['blue']); // logs blue

</script></body></html>
```

### `Array()` 参数

```html
<!DOCTYPE html><html lang="en"><script>
var foo = new Array(1, 2, 3);
var bar = new Array(100);
console.log(foo[0], foo[2]); // logs '1 3'
console.log(bar[0], bar.length); // logs 'undefined 100'
</script></body></html>
```

### `Array()` 属性与方法

**属性**：`prototype`

**实例属性**：`constructor`、`index`、`input`、`length`

**实例方法**：`pop()`、`push()`、`reverse()`、`shift()`、`sort()`、`splice()`、`unshift()`、`concat()`、`join()`、`slice()`

### 创建数组

```html
<!DOCTYPE html><html lang="en"><body><script>

// Array() 构造函数
var myArray1 = new Array('blue', 'green', 'orange', 'red');
console.log(myArray1); // logs ["blue", "green", "orange", "red"]

// 数组字面量符号
var myArray2 = ['blue', 'green', 'orange', 'red'];
console.log(myArray2); // logs ["blue", "green", "orange", "red"]
</script></body></html>
```

### 在数组中添加和更新值

```html
<!DOCTYPE html><html lang="en"><script>
var myArray = [];
myArray[50] = 'blue';
console.log(myArray.length); /* logs 51 */
</script></body></html>
```

```html
<!DOCTYPE html><html lang="en"><body><script>
var myArray = [];
myArray[50] = 'blue';
myArray[50] = {'color': 'blue'};
console.log(myArray[50]); // logs 'Object'
console.log(myArray[50]['color']); // logs 'blue'
console.log(myArray[50].color); // logs 'blue'
</script></body></html>
```

### 长度 vs 索引

```html
<!DOCTYPE html><html lang="en"><body><script>
var myArray = ['blue'];
console.log(myArray[0]); // logs 'blue'
console.log(myArray.length); // logs 1
</script></body></html>
```

### 使用预定义长度定义数组

```html
<!DOCTYPE html><html lang="en"><body><script>
var myArray = Array(3);
console.log(myArray.length); // logs 3
console.log(myArray[0]); // logs undefined
</script></body></html>
```

### 设置长度可以添加或删除值

```html
<!DOCTYPE html><html lang="en"><body><script>
  var myArray = ['blue', 'green', 'orange', 'red'];
  console.log(myArray.length); // logs 4
  myArray.length = 99;
  console.log(myArray.length); // logs 99
  myArray.length = 1;
  console.log(myArray[1]); // logs undefined
  console.log(myArray); // logs ['blue']
</script></body></html>
```

### 包含其他数组（多维数组）

```html
<!DOCTYPE html><html lang="en"><body><script>
var myArray = [[['4th dimension']]];
console.log(myArray[0][0][0]); // logs '4th dimension'
</script></body></html>
```

### 遍历数组，反向和正向

```html
<!DOCTYPE html><html lang="en"><body><script>
var myArray = ['blue', 'green', 'orange', 'red'];
var myArrayLength = myArray.length;
var counter = 0;
while (counter < myArrayLength) {
  console.log(myArray[counter]); // logs 'blue', 'green', 'orange', 'red'
  counter++;
}
</script></body></html>
```

```html
<!DOCTYPE html><html lang="en"><body><script>
var myArray = ['blue', 'green', 'orange', 'red'];
var myArrayLength = myArray.length;
while (myArrayLength--) {
  console.log(myArray[myArrayLength]); // 打印 'red', 'orange', 'green', 'blue'
}
</script></body></html>
```

---

## 第 10 章 - `String()`

### 使用 `String()` 对象的概念概述

```html
<!DOCTYPE html><html lang="en"><body><script>
// 使用 new 关键字和 String() 构造函数创建字符串对象
var stringObject = new String('foo');
console.log(stringObject); // 输出 {0 = 'f', 1 = 'o', 2 = 'o'}
console.log(typeof stringObject); // 输出 'object'

// 通过直接使用 String 构造函数创建字符串字面量/原始值
var stringObjectWithoutNewKeyword = String('foo');
console.log(stringObjectWithoutNewKeyword); // 输出 'foo'
console.log(typeof stringObjectWithoutNewKeyword); // 输出 'string'

// 创建字符串字面量/原始值
var stringLiteral = 'foo';
console.log(stringLiteral); // 输出 'foo'
console.log(typeof stringLiteral); // 输出 'string'
</script></body></html>
```

### `String()` 参数

```html
<!DOCTYPE html><html lang="en"><body><script>
var stringObject = new String('foo');
console.log(stringObject); // 输出 {0="f", 1="o", 2="o"}
</script></body></html>
```

> **注意**：使用 `new` 关键字生成的实例会产生一个真正的复杂对象。你应该避免这样做（使用字面量/原始值），因为 `typeof` 运算符会将复杂的字符串对象报告为 `'object'`。

### `String()` 属性和方法

**属性**：`prototype`

**方法**：`fromCharCode()`

**实例属性**：`constructor`、`length`

**实例方法**：`charAt()`、`charCode()`、`concat()`、`indexOf()`、`lastIndexOf()`、`localeCompare()`、`match()`、`quote()`、`replace()`、`search()`、`slice()`、`split()`、`substr()`、`substring()`、`toLocaleLowerCase()`、`toLocaleUpperCase()`、`toLowerCase()`、`toString()`、`toUpperCase()`、`valueOf()`

---

## 第 11 章 - `Number()`

### 使用 `Number()` 对象的概念概述

```html
<!DOCTYPE html><html lang="en"><body><script>
var numberObject = new Number(1);
console.log(numberObject); // 输出 1
console.log(typeof numberObject) // 输出 'object'

var numberObjectWithNew = Number(1);
console.log(numberObjectWithNew); // 输出 1
console.log(typeof numberObjectWithNew) // 输出 'number'

var numberLiteral = 1;
console.log(numberLiteral); // 输出 1
console.log(typeof numberLiteral); // 输出 'number'
</script></body></html>
```

### 整数和浮点数

```html
<!DOCTYPE html><html lang="en"><body><script>
var integer = 12345;
console.log(integer); // 输出 12345
var floatingPoint = 123.45;
console.log(floatingPoint); // 输出 123.45
</script></body></html>
```

### `Number()` 属性

- `MAX_VALUE`
- `MIN_VALUE`
- `NaN`
- `NEGATIVE_INFINITY`
- `POSITIVE_INFINITY`
- `prototype`

### `Number` 对象实例属性和方法

**实例属性**：`constructor`

**实例方法**：`toExponential()`、`toFixed()`、`toLocaleString()`、`toPrecision()`、`toString()`、`valueOf()`

---

## 第 12 章 - `Boolean()`

### 使用 `Boolean()` 对象的概念概述

```html
<!DOCTYPE html><html lang="en"><body><script>
var myBoolean1 = new Boolean(false);
console.log(typeof myBoolean1); // 输出 'object'

var myBoolean2 = Boolean(0);
console.log(typeof myBoolean2); // 输出 'boolean'

var myBoolean3 = false;
console.log(typeof myBoolean3); // 输出 'boolean'
console.log(myBoolean1, myBoolean2, myBoolean3); // 输出 false false false
</script></body></html>
```

### `Boolean()` 参数

`Boolean()` 构造函数接受一个参数并转换为布尔值。任何有效的 JavaScript 值只要不是 `0`、`-0`、`null`、`false`、`NaN`、`undefined` 或空字符串 (`""`)，都会被转换为 `true`。

> **注意**：使用 `new` 关键字生成的实例会产生一个真正的复杂对象。你应该避免这样做。

### `Boolean()` 属性和方法

**属性**：`prototype`

**实例属性**：`constructor`

**实例方法**：`toSource()`、`toString()`、`valueOf()`

### 非原始假布尔对象转换为 `true`

```html
<!DOCTYPE html><html lang="en"><body><script>
var falseValue = new Boolean(false);
console.log(falseValue); // 我们有一个假布尔对象，但对象是真值
if (falseValue) {
    console.log(`falseValue is truthy`);
}
</script></body></html>
```

### 某些值为假，其余所有均为真

```html
<!DOCTYPE html><html lang="en"><body><script>
console.log(Boolean(0));
console.log(Boolean(-0));
console.log(Boolean(null));
console.log(Boolean(false));
console.log(Boolean(''));
console.log(Boolean(undefined));
console.log(Boolean(null));

console.log(Boolean(1789));
console.log(Boolean('false'));
console.log(Boolean(Math));
console.log(Boolean(Array()));
</script></body></html>
```

### 处理原始字符串、数字和布尔值

当访问属性时，原始/字面量值转换为对象。

**字符串**：
```html
<!DOCTYPE html><html lang="en"><script>
var stringObject = new String('foo');
console.log(stringObject.length); // 记录 3
var stringLiteral = 'foo';
console.log(stringLiteral.length); // 记录 3
console.log('bar'.length); // 记录 3
</script></body></html>
```

**数字**：
```html
<!DOCTYPE html><html lang="en"><body><script>
var numberObject = new Number(1.10023);
console.log(numberObject.toFixed()); // 记录 1
var numberLiteral = 1.10023;
console.log(numberLiteral.toFixed()); // 记录 1
console.log((1234).toString()); // 记录 '1234'
</script></body></html>
```

**布尔**：
```html
<!DOCTYPE html><html lang="en"><body><script>
var booleanObject = new Boolean(0);
console.log(booleanObject.toString()); // 记录 'false'
var booleanLiteral = false;
console.log(booleanLiteral.toString()); // 记录 'false'
console.log(true.toString()); // 记录 'true'
</script></body></html>
```

---

## `null` 值

```javascript
var myObject = null;
console.log(typeof myObject); // logs 'object'
console.log(myObject === null); // logs true
```

> **注意**：在验证空值时，始终使用 `===`，因为 `==` 无法区分 `null` 和 `undefined`。



## 第 14 章 - Undefined

## undefined 值的概念概述

JavaScript 以两种略有不同的方式使用`undefined`值。

第一种用法是表示一个声明的变量（例如`var foo`）没有被赋值值。第二种用法是表示你尝试访问的对象属性未定义（即它甚至没有被命名），并且在原型链中未找到。

下面，我将检查 JavaScript 对`undefined`的两种用法。

![](img/ad11d036d555f7d1771aeb8c30e67ba2_133_0.png)

```html
<!DOCTYPE html><html lang="en"><body><script>
var initializedVariable; // 变量
console.log(initializedVariable); // logs undefined
console.log(typeof initializedVariable); // 确认 JavaScript 返回了 undefined
var foo = {};
console.log(foo.bar); // logs undefined, foo 对象中没有 bar 属性
console.log(typeof foo.bar); // 确认 JavaScript 返回了 undefined
</script</body</html>
```

## Notes

- 允许 JavaScript 独立使用`undefined`被认为是一种良好实践。你不应该发现自己正在给`undefined`赋值，例如`foo = undefined`。相反，如果你指定某个属性或变量值不可用，应该使用`null`。

## JavaScript ECMA-262 第 3 版及更高版本在全局作用域声明了 undefined 变量

与之前的版本不同，JavaScript ECMA-262 第 3 版（及更高）在全局作用域声明了一个名为`undefined`的全局变量。由于该变量被声明但没有赋值，因此`undefined`变量被设置为`undefined`。

live code: http://jsfiddle.net/javascriptenlight/MhRkB/

```html
<!DOCTYPE html><html lang="en"><body><script>

// 确认 undefined 是全局作用域的一个属性
console.log(undefined in this); // logs true

</script</body</html>
```

## 第 15 章 - Math 函数

## 内置 Math 对象的概念概述

`Math`对象包含静态属性和方法，用于数学上的处理数字或数学常数（例如`Math.PI`）。该对象是 JavaScript 内置的，而不是基于创建 math 实例的`Math()`构造函数。

> Notes

> `Math`以大写字母开头似乎很奇怪，因为你不需要实例化`Math`对象的实例。不要被此困扰。只需意识到 JavaScript 已经为你设置好了这一切。

## Math 属性和方法

`Math`对象具有以下属性和方法：

属性（例如`Math.PI`）：

- E

- LN2

- LN10

- LOG2E

- LOG10E

- PI

- SQRT1_2

- SQRT2

方法（例如`Math.random()`）：

- abs()

- acos()

- asin()

- atan()

- anat()

- ceil()

- cos()

- exp()

- floor()

- log()

- max()

- min()

- pow()

- random()

- round()

- sin()

- sort()

- tan()

## Math 不是一个构造函数

`Math`对象与被实例化的内置对象不同。`Math`是一个为了存放静态属性和方法的一次性对象，在处理数字时可以使用。没有办法创建`Math`的实例，因为没有构造函数。

## Math 拥有你无法增强/修改的常量

许多`Math`属性是不可修改的常量。由于这偏离了 JavaScript 的可变本质，这些属性采用全大写字母（例如`Math.PI`）。不要因为其首字母大写就将属性常量误认为是构造函数。它们仅仅是无法更改的对象属性。

> Notes

> 在 JavaScript 1.5 (ECMA-262, 第 3 版) 中，不存在用户定义的常量。

以下几点总结了你在阅读本书（以及研究代码示例）期间应该学到的。阅读每项总结，如果你不理解所说内容，请返回书籍中的主题。

- 对象由存储值的命名属性组成。

- JavaScript 中的几乎所有内容都可以像对象一样工作。复杂值是对象，而原始值可以像对象一样处理。这就是为什么你可能会听到人们说 JavaScript 中的一切都是对象。

- 对象是通过使用`new`关键字调用构造函数创建的，或者通过使用简写字面量表达式创建的。

- 构造函数是对象（`Function`对象），因此，在 JavaScript 中，对象创建对象。

- JavaScript 提供了 9 个原生构造函数：`Object()`、`Array()`、`String()`、`Number()`、`Boolean()`、`Function()`、`Date()`、`RegExp()`和`Error()`。`String()`、`Number()`和`Boolean()`构造函数具有双重用途：a) 提供原始值和 b) 在需要时提供对象封装，以便原始值在处理时可以像对象一样工作。

- 值`null`、`undefined`、`"string"`、`Object()`、`Array()`、`String()`、`Number()`、`Boolean()`、`Function()`、`Date()`、`RegExp()`和`Error()`具有双重用途：a) 提供原始值和 b) 在需要时提供对象封装，以便原始值在处理时可以像对象一样工作。

（注：原文中存在大量重复段落，已按要求去重，保留核心翻译内容）

## 结论

我希望在读完这本书后，你能够更好地理解你所选择的 JavaScript 库，或者更好，是具备编写自己的 JavaScript 解决方案的能力。无论哪种，本书本身并不是为了该语言的终极指南。从这里开始，我建议阅读或重读以下书籍，以便通过不同的声音来加强此处的话题，并审查和探索额外的 JavaScript 主题。

- 《JavaScript: The Good Parts》，Douglas Crockford 著

- 《JavaScript Patterns》，Stoyan Stefanov 著

- 《Object-Oriented JavaScript》，Stoyan Stefanov 著

- 《Professional JavaScript for Web Developers》，Nicholas C. Zakas 著

- 《High Performance JavaScript》，Nicholas C. Zakas 著

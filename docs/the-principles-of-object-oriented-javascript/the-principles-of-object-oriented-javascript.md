
# 面向对象 JavaScript 原

## 关于作者

Nicholas C. Zakas 是 Box 的软件工程师，以编写关于最新 JavaScript 最佳实践的文章和演讲而闻名。他在 Yahoo! 的五年里磨练了经验，曾担任 Yahoo! 主页的首席前端工程师。他是多本书的作者，包括《Maintainable JavaScript》（O’Reilly Media, 2012）和《Professional JavaScript for Web Developers》（Wrox, 2012）。

## 关于技术审核员

Angus Croll 原来自英国，现是旧金山 Twitter 框架团队的一员，也是 Twitter 开源 Flight 框架的共同作者和主要维护者。他同样痴迷于 JavaScript 和文学，并热情倡导艺术家和创意思维者更多参与软件开发。Angus 是全球范围内会议的频繁演讲者，目前正在为 No Starch Press 编写两本书。可以通过 Twitter @angustweets 与他联系。

## 前言

Nicholas Zakas 这个名字与 JavaScript 开发本身是同义词。关于他的专业赞誉，我可以漫谈好几页，但我并不打算这样做。Nicholas 以其高水平的 JavaScript 开发者和作者而闻名，他不需要自我介绍。然而，在赞誉本书的内容之前，我想分享一些个人见解。

我与 Nicholas 的关系源于我作为一个 JavaScript 学生，多年来学习他的书籍、阅读他的博客文章、观看他的演讲，并关注他的 Twitter 更新。我们第一次线下见面是几年前，当时我（此处见原文）邀请他在一次 jQuery 会议上做演讲。他为 jQuery 社区带来了一场高质量的演讲，从那时起，我们一直在互联网上进行公开和私下的交流。在这些段时间里，我愈发钦佩他，他不仅仅是 JavaScript 社区的一位领袖和开发者。他的言语总是优雅且深思，他的举止总是友善。

作为开发者、演讲者和作者，他的意图始终是帮助、教育和改进。当他演讲时，你应该倾听，不仅是因为他是一个 JavaScript 专家，更因为他的品质超越了他的职业地位。

本书的标题和引言明确表达了 Nicholas 的意图：他编写此书是为了帮助具有类思维（即 C++ 或 Java）的程序员过渡到一种没有类的语言。在书中，他解释了在编写 JavaScript 时如何实现封装、聚合、继承和多态。这是将有知识的程序员引入面向对象的 JavaScript 开发阵营的理想文本。如果你是作为另一种语言的开发者在阅读这本书，那么你将体验一本简洁且用词精妙的 JavaScript 书。

然而，这本书也服务于来自 JavaScript 内部的程序员。许多 JavaScript 开发者对对象的理解仅限于 ECMAScript 3 (ES3)，他们需要对 ECMAScript 5 (ES5) 对象特性的进行正式介绍。这本书可以作为这种介绍，弥合 ES3 对象和 ES5 对象之间的知识鸿沟。

现在，你可能会想：“没什么大不了。好几本书都包含了关于 ES5 中 JavaScript 新增内容的章节或注释。”没错，确实如此。但我认为这是迄今为止唯一一本专注于对象本质的书籍，它通过赋予 ES5 对象在整个叙述中一等公民的地位。这本书不仅对 ES5 对象提供了一个连贯的介绍，还介绍了你在学习 ES5 中许多新特性时需要理解的 ES3 部分。

（注：原文后续存在多处乱码或重复片段，此处已根据上下文逻辑进行语义处理并保留核心意图）

## 引言 **xix**

熟悉其他语言是判断这本书是否适合你的一个强有力的指标。特别是，这本书目标针对以下三类读者：

- 熟悉面向对象编程概念并希望将其应用于 JavaScript 的开发者
- 试图更有效地组织代码结构的 Web 应用程序和 Node.js 开发者
- 试图对语言有更深理解的初级 JavaScript 开发者

这本书并不是为从未写过 JavaScript 的初学者准备的。你需要对如何编写和执行 JavaScript 代码有良好的理解才能跟上。

## **概述**

**第 1 章：原始类型和引用类型** 介绍了 JavaScript 中的两种不同值类型：原始类型（primitive）和引用类型（reference）。你将学习它们之间的区别，以及理解这些差异对于全面理解 JavaScript 有有多重要。

**第 2 章：函数** 解释了 JavaScript 函数的方里外。一等函数让 JavaScript 成为了一门如此有趣的语言。

**第 3 章：理解对象** 详细介绍了 JavaScript 中对象的组成部分。JavaScript 对象的行为与其他语言中的对象不同，因此深入理解对象的工作原理对于精通该语言至关重要。

**第 4 章：构造函数和原型** 通过更具体地查看构造函数，扩展了之前对函数的讨论。所有的构造函数都是函数，但它们的使用略有不同。本章探索了差异，同时也讨论了如何创建你自己的自定义类型。

**第 5 章：继承** 解释了如何在 JavaScript 中实现继承。虽然 JavaScript 中没有类，但这并不意味着无法继承。在这一章中，你将学习原型继承以及它与基于类的继承有什么区别。

**第 6 章：对象模式** 介绍了常见的对象模式。在 JavaScript 中构建和组合对象有许多不同的方式，本章将向你介绍这些操作中最流行的模式。

## **帮助与支持**

如果你对这本书有任何问题、意见或其他反馈，请访问邮件列表：http://groups.google.com/group/zakasbooks。

# **1 原始类型和引用类型**

大多数开发者通过使用 Java 或 C# 等基于类的语言来学习面向对象编程的。当这些开发者开始学习 JavaScript 时，他们会感到无所措，因为 JavaScript 没有对类提供正式支持。与其从一开始就定义类，在 JavaScript 中，你只需要根据需要编写代码并创建数据结构。由于缺乏类，JavaScript 也缺乏像包这样的类分组。在 Java 等语言中，包名和类名定义了你使用的对象类型以及项目中文件和文件夹的布局，而在 JavaScript 中进行编程就像是从一张空白画布开始：你可以以任何你的方式组织内容。一些开发者选择模仿其他语言的结构，而另一些人则利用 JavaScript 的灵活性创造出完全新的东西。对于初学者来说，这种选择的自由可能会让人措措，但一旦适应了，你会发现 JavaScript 是一门极其灵活的语言，可以很容易地适应你的偏好。

为了方便从传统的面向对象语言过渡，JavaScript 将对象作为语言的核心部分。JavaScript 中的几乎所有数据要么是对象，要么通过对象访问。事实上，即使是函数（传统语言通常需要你费力才能获取其引用），在 JavaScript 中也被表示为对象，这使得它们成为了*一等函数*。

操作和理解对象是理解整个 JavaScript 的关键。你可以随时创建对象，并根据需要随时对其添加或删除属性。此外，JavaScript 对象极其灵活，具有创建独特且有趣模式的能力，而这些在其他语言中是无法可能的。

本章重点介绍于如何识别和处理两种主要的 JavaScript 数据类型：原始类型和引用类型。尽管两者都通过对象访问，但它们的运行方式不同，理解这一点很重要。

### **什么是类型？**

尽管 JavaScript 没有类的概念，但它仍然使用两种*类型*：原始和引用。*原始类型*被存储为简单的数据类型。*引用类型*被存储为对象，而实际上只是指向内存位置的引用。

棘手的地方在于，JavaScript 允许你混合使用它们（注：原文此处可能存在逻辑跳跃，此处按意译）。[此处根据原文逻辑翻译：棘手的地方在于 JavaScript 允许你处理这些类型]（注：由于原文句子 "The tricky thing is that JavaScript lets you..." 后面似乎断不完整，此处保持语意贯）。

（注：由于提供的待翻译文本在“ Types Types ，，，关于“原始类型和引用类型”在第 2 章 之后之后，，，，，，，，，，，，，，翻译翻译翻译翻译翻译翻译翻译内容。]

## 基本类型与引用类型 **5**

正如你预期的那样，当值为字符串时，`typeof` 返回 "string"；当值为数字时（无论整数还是浮点数），返回 "number"；当值为布尔值时，返回 "boolean"；当值为 undefined 时，返回 "undefined"。

棘手的部分在于涉及到 `null`。

你不会是第一个对这行代码的结果感到困惑的开发者：

```javascript
console.log(typeof null); // "object"
```

当你运行 `typeof null` 时，结果是 "object"。但为什么类型是 null 却返回 "object" 呢？（事实上，这已经被设计和维护 JavaScript 的委员会 TC39 承认是一个错误。你可以推断 null 是一个空对象指针，使得 "object" 成为逻辑上的返回值，但这仍然令人困惑。）

判断一个值是否为 null 的最佳方法是直接将其与 null 进行比较，如下：

```javascript
console.log(value === null); // true or false
```

### 不进行强制类型转换的比较

注意，这段代码使用了三等运算符 (`===`) 而不是双等运算符 (`==`)。原因为三等运算符在进行比较时不会将变量转换为另一种类型。为了理解为什么这很重要，请考虑以下内容：

```javascript
console.log("5" == 5); // true
console.log("5" === 5); // false
console.log(undefined == null); // true
console.log(undefined === null); // false
```

当你使用双等时，字符串 `"5"` 和数字 `5` 被认为是等等的，因为双等运算符在进行比较之前会将字符串转换为数字。三等运算符不认为这些值是相等，因为它们是两种不同的类型。同样，当你比较 undefined 和 null 时，双等运算符认为它们是等价的，而三等运算符则认为它们不等等。当你尝试识别 null 时，请使用三等运算符，以便能够正确识别类型。

第1章 第6页

### 基本方法

尽管它们是基本类型，但字符串、数字和布尔值实际上拥有方法。（null 和 undefined 类型没有方法）。特别是字符串，拥有许多方法来帮助你处理它们。例如：

```javascript
var name = "Nicholas";
var lowercaseName = name.toLowerCase(); // 转换为小写
var firstLetter = name.charAt(0); // 获取第一个字符
var middleOfName = name.substring(2, 5); // 获取字符 2-4
var count = 10;
var fixedCount = count.toFixed(2); // 转换为 "10.00"
var hexCount = count.toString(16); // 转换为 "a"
var flag = true;
var stringFlag = flag.toString(); // 转换为 "true"
```

**注意** 尽管它们拥有方法，但基本值本身并不是对象。*JavaScript 让它们看起来像对象，以便在语言中提供一致的体验，你将在本章后面看到。*

### 引用类型

引用类型代表 JavaScript 中的对象，是你在语言中找到的最接近类的东西。引用值是引用类型的*实例*，与对象等同（本章其余部分简单地将引用值称为*对象*）。对象是一个无序的*属性*列表，由一个名称（始终为字符串）和一个值组成。当一个属性的值是一个函数时，它被称为*方法*。函数本身在 JavaScript 中实际上是引用值，因此包含数组的属性与包含函数的属性之间几乎没有区别，区别是函数可以执行。

当然，在开始使用对象之前，你必须创建它们。

### 创建对象

有时将 JavaScript 对象仅仅视为哈希表会有所帮助，如图 1-2 所示。

有几种创建或*实例化*对象的方法。第一种是使用 `new` 运算符配合*构造函数*。（构造函数简单来说是通过 `new` 来创建对象的函数——任何函数都可以是构造函数。）

| Object | |
| :--- | :--- |
| name | value |
| name | value |

*图 1-2：对象的结构*

基本类型与引用类型 7

按照惯例，JavaScript 中的构造函数以大写字母开头，以区分它们和非构造函数。例如，这段代码实例化了一个通用对象并将它的引用存储在 object 中：

```javascript
var object = new Object();
```

引用类型不会直接将对象存储在赋值给它的变量中，因此示例中的 object 变量实际上并不包含对象实例。相反，它持有指向对象所存在内存位置的指针（或引用）。这是对象与基本值之间的主要区别，因为基本值是直接存储在变量中的。

当你将对象赋值给变量时，你实际上是在赋值一个指针。这意味着如果你将一个变量赋值给另一个变量，每个变量都会获得指针的拷贝，并且它们仍然引用内存中的同一个对象。例如：

```javascript
var object1 = new Object();
var object2 = object1;
```

这段代码首先创建一个对象（使用 `new`）并在 object1 中存储引用。仍然仍然只有第一行创建的那个对象实例，但两个变量现在都指向该对象，如图 1-3 所示。

| Variable | Object |
| :--- | :--- |
| object1 | object1 |
| | Memory Object |

*图 1-3：两个变量指向同一个对象*

### 取消引用

JavaScript 是一种带有垃圾回收的语言，因此当你使用引用类型时，不需要真正担心内存分配。然而，最好是*取消*不再需要的引用，以便垃圾回收器可以释放该内存。此此最佳方法是将对象变量设置为 null。

第1章 第8页

```javascript
var object1 = new Object();
// 执行某些操作
object1 = null; // 取消引用
```

在这里，`object1` 在最后被设置为 null 之前被创建并使用。当内存中不再有对象的引用时，垃圾回收器就可以释放该内存。

### 添加或删除属性

对象的另一个有趣方面是你可以随时添加和删除属性。例如：

```javascript
var object1 = new Object();
var object2 = object1;
object1.myCustomProperty = "Awesome!";
console.log(object2.myCustomProperty); // "Awesome!"
```

在这里，`myCustomProperty` 被添加到 `object1` 中，值为 `"Awesome!"`。

**注意** 这个示例展示了 JavaScript 的一个特别独特的方面：你可以随心所欲地修改对象，即使你没有定义它们。

除了通用对象引用类型外，JavaScript 还有几种内置类型。

### 实例化内置类型

你已经了解了如何使用 `Object()` 创建和交互通用对象。Object 类型只是 JavaScript 提供的少数内置类型之一。内置类型包括：

- Array：具有数值索引的有序列表
- Date：日期和时间
- Error：运行时错误（还有更具体的错误类型）
- Function：函数
- Object：通用对象
- RegExp：正则表达式

你可以使用 `new` 实例化每个内置引用类型，如下：

```javascript
var items = new Array();
var now = new Date();
var error = new Error("Something bad happened.");
var func = new Function("console.log('Hi');");
var object = new Object();
var re = new RegExp("\\d+");
```

### 字面量形式

几种内置引用类型具有字面量形式。字面量是一种允许你在不显式使用 `new` 运算符和对象构造函数的情况下定义引用值的语法。（在本章早期，你见过基本字面量的示例，包括字符串字面量、数字字面量、布尔字面量、null 字面量和 undefined 字面量。）

使用*对象字面量*语法创建对象时，可以在括号内部定义新对象的属性。属性由标识符或字符串、冒号和一个值组成，多个属性之间用逗号分隔。例如：

```javascript
var book = { name: "The Principles of Object-Oriented JavaScript", year: 2014 };
```

你也可以使用字符串字面量作为属性名称，当你希望属性名称包含空格或其他特殊字符时非常有用：

```javascript
var book = { "name": "The Principles of Object-Oriented JavaScript", "year": 2014 };
```

## 第1章

尽管语法有所不同，这个示例与上一个是等价的。这两个示例在逻辑上也与以下代码等价：

```javascript
var book = new Object();
book.name = "The Principles of Object-Oriented JavaScript";
book.year = 2014;
```

前三个示例的结果是相同的：一个具有两个属性的对象。模式的选择取决于你，因为其功能最终是相同的。

**注意** 使用对象字面量实际上并没有调用 `new Object()`。相反，JavaScript 引擎会遵循与使用 `new Object()` 相同的步骤，但并不会实际调用构造函数。这对于所有引用字面量都是如此。

你可以以类似的方式定义*数组字面量*，即在方括号内包含任意数量用逗号分隔的值。例如：

```javascript
var colors = ["red", "blue", "green"];
console.log(colors[0]); // "red"
```

这段代码与以下代码等价：



```javascript
var colors = new Array("red", "blue", "green")
console.log(colors[0]); // "red"
```

### 函数字面量

你几乎总是使用字面量形式定义函数。事实上，鉴于维护、读取和调试字符串代码而非实际代码的挑战，通常不建议使用`Function`构造函数，因此你很少会在代码中看到它。

使用字面量形式创建函数要简单得多，且不容易出错。例如：

```javascript
function reflect(value) {
 return value;
}
```

// 等同于

```javascript
var reflect = new Function("value", "return value;");
```

这段代码定义了`reflect()`函数，它返回传递给它的任何值。即使对于这个简单的函数，字面量形式也比构造函数形式更容易编写和理解。此外，没有好的方法可以调试以构造函数形式创建的函数：这些函数不会被 JavaScript 调试器识别，因此在你的应用程序中像黑盒一样运行。

### 正则表达式字面量

JavaScript 还有*正则表达式字面量*，它允许你在不使用`RegExp`构造函数的情况下定义正则表达式。正则表达式字面量看起来与 Perl 中的正则表达式非常相似：模式包含在两个斜杠之间，任何额外的选项都是跟随第二个斜杠的单字符。例如：

```javascript
var numbers = /\d+/g;
```

// 等同于

```javascript
var numbers = new RegExp("\\d+", "g");
```

JavaScript 中的正则表达式字面量形式比构造函数形式稍微更容易处理，因为你不需要担心字符串内部的转义。在使用`RegExp`构造函数时，你将模式作为字符串传递，因此你必须对任何反斜杠进行转义。（这就是为什么在字面量中使用`\d`，而在构造函数中使用`\\d`。）在 JavaScript 中，除非正则表达式是从一个或多个字符串动态构建的，否则优于使用字面量形式而非构造函数形式。

尽管如此，除了`Function`之外，实例化内置类型并没有真正的对错方法。许多开发者倾向于使用字面量，而一些人则倾向于构造函数。选择你认为更方便使用的方法。

### 属性访问

属性是存储在对象上的键值对。点符号（Dot notation）是 JavaScript 中访问属性的最常用方式（就像许多面向对象的语言一样），但你也可以通过使用字符串的括号表示访问 JavaScript 对象的属性。

例如，你可以编写以下使用点表示法的代码：

```javascript
var array = [];

array.push(12345);
```

使用括号表示法，方法的名称现在被包含在方括号内的字符串中，如例所示：

```javascript
var array = [];

array["push"](12345);
```

这种语法在你想要动态决定访问哪个属性时非常有用。例如，在这里，括号表示法允许你使用变量而不是字符串字面量来指定要访问的属性。

```javascript
var array = [];
var method = "push";

array[method](12345);
```

在此列表中，变量`method`的值为`"push"`，因此在数组上调用了`push()`。这种能力非常有用，正如你在整本书中看到的那样。需要记住的点是，除了语法之外，点表示法和括号表示法之间的唯一区别（无论性能或其他方面）是，括号表示法允许你在属性名中使用特殊字符。开发者倾向于认为点表示法更容易读，因此你会看到它的使用频率高于括号表示法。

### 识别引用类型

函数是最容易识别的引用类型，因为当你对函数使用`typeof`运算符时，该运算符应该返回`"function"`：

```javascript
function reflect(value) {
 return value;
}

console.log(typeof reflect); // "function"
```

其他引用类型更难识别，因为对于除函数以外的所有引用类型，`typeof`都返回`"object"`。当你处理许多不同类型时，这并没有什么帮助。为了更容易地识别引用类型，你可以使用 JavaScript 的`instanceof`运算符。

`instanceof`运算符接受一个对象和一个构造函数作为参数。当该值是构造函数指定的类型的实例时，`instanceof`返回`true`；否则返回`false`，如下所示：

```javascript
var items = [];
var object = {};

function reflect(value) {
 return value;
}

console.log(items instanceof Array); // true
console.log(object instanceof Object); // true
console.log(reflect instanceof Function); // true
```

在这个示例中，使用`instanceof`和构造函数对多个值进行了测试。每个引用类型通过使用`instanceof`和代表其真实类型的构造函数被正确识别（尽管在创建变量时没有使用该构造函数）。

`instanceof`运算符可以识别继承类型。这意味着每个对象实际上都是`Object`的实例，因为每个引用类型都继承自`Object`。

为了演示，下面的列表使用`instanceof`检查了之前创建的三个引用：

```javascript
var items = [];
var object = {};

function reflect(value) {
 return value;
}

console.log(items instanceof Array); // true
console.log(items instanceof Object); // true
console.log(object instanceof Object); // true
console.log(object instanceof Array); // false
console.log(reflect instanceof Function); // true
console.log(reflect instanceof Object); // true
```

每个引用类型都被正确识别为`Object`的实例，所有引用类型都继承自它。

### 识别数组

尽管`instanceof`可以识别数组，但有一个影响 Web 开发者的例外：JavaScript 值可以在同一个网页的各个帧（frames）之间来传递。只有当你尝试识别引用值的类型时才会出现问题，因为每个网页都有自己的全局上下文——它们自己的`Object`、`Array`以及所有其他内置类型的版本。因此，当你从一个帧传递数组到另一个帧时，`instanceof`将无法工作，因为该数组实际上是另一个帧的`Array`实例。

为了解决这个问题，ECMAScript 5 引入了`Array.isArray()`，它可以明确地将该值识别为`Array`的实例。

```javascript
var items = [];
console.log(Array.isArray(items)); // true
```

### 原始包装类型

JavaScript 最令人困惑的部分之一是*原始包装类型*（primitive wrapper types）的概念。有三种包装类型（`String`、`Number`和`Boolean`）。这些特殊的引用类型存在是为了让处理原始值变得像处理对象一样简单。（如果你为了获取文本的子字符串而必须使用不同的语法或切换到过程化风格，那将非常困惑。）

原始包装类型是引用类型，当读取字符串、数字或布尔值时，它们会在后台自动创建。例如，在此列表的第一行，一个原始字符串值被赋值给`name`。第二行将`name`视为对象，并使用点符号调用`charAt(0)`。

```javascript
var name = "Nicholas";
var firstChar = name.charAt(0);

console.log(firstChar); // "N"
```

这是在后台发生的情况：

```javascript
// JavaScript 引擎执行的操作
var name = "Nicholas";
var temp = new String(name);
var firstChar = temp.charAt(0);

temp = null;

console.log(firstChar); // "N"
```

因为第二行像使用对象一样使用字符串（原始值），JavaScript 引擎创建一个`String`实例以便`charAt(0)`能够工作。`String`对象只存在一个语句就会被销毁（这一过程被称为*自动装箱*autoboxing）。为了测试这一点，尝试像普通对象一样向字符串添加属性：

```javascript
var name = "Nicholas";
name.last = "Zakas";

console.log(name.last); // undefined
```

这段代码尝试向字符串`name`添加属性`last`。代码本身没有问题，只是属性消失了。发生了什么？在处理普通对象时，你可以随时添加属性，它们会一直直到你手动删除。对于原始包装类型，属性似乎消失了，是因为赋值属性的对象在随后立即被销毁了。

原始类型与引用类型 **15**

以下是 JavaScript 引擎中实际发生的情况：

```javascript
// JavaScript 引擎的操作

var name = "Nicholas";

var temp = new String(name);

temp.last = "Zakas";

temp = null; // 临时对象被销毁

var temp = new String(name);

console.log(temp.last); // undefined

temp = null;
```

代码并没有为字符串赋值一个新属性，而是在临时对象上创建一个新属性，然后将其将其销毁。当你之后尝试访问该属性时，会临时创建一个不同的对象，而新属性在其中并不存在。虽然原始值会自动创建引用值，但当`instanceof`检查这些类型的值时，结果为`false`：

```javascript
var name = "Nicholas";

var count = 10;

var found = false;

console.log(name instanceof String); // false
console.log(count instanceof Number); // false
console.log(found instanceof Boolean); // false
```

`instanceof`运算符返回`false`是因为只有在读取值时才会创建临时对象。由于`instanceof`并没有实际读取任何内容，因此没有创建临时对象，它告诉我们这些值不是原始包装类型的实例。你可以手动创建原始包装类型，但会有某些副作用：

```javascript
var name = new String("Nicholas");

var count = new Number(10);

var found = new Boolean(false);

console.log(typeof name); // "object"
console.log(typeof count); // "object"
console.log(typeof found); // "object"
```

如你所见，创建原始包装类型的实例只是创建了另一个对象，这意味着`typeof`无法识别你想要存储的数据类型。

此外，你不能像使用原始值那样使用`String`、`Number`和`Boolean`对象。例如，以下代码使用了布尔对象。该布尔值为`false`，但`console.log("Found")`仍然会执行，因为在条件语句内部，对象始终被视为`true`。对象代表`false`并不重要；因为它是一个对象，所以它的求值为为`true`。

```javascript
var found = new Boolean(false);

if (found) {
 console.log("Found"); // 这会执行
}
```

手动实例化原始包装器在其他方面也可能引起困惑，除非你发现某个这样做有意义的特殊情况，否则你应该避免这样做。在大多数情况下，使用原始包装对象代替原始值只会导致错误。

### 总结

虽然 JavaScript 没有类，但它确实有类型。每个变量或数据都与特定的原始类型或引用类型相关。五种原始类型（字符串、数字、布尔值、`null`和`undefined`）代表直接存储在给定上下文变量对象中的简单值。你可以使用`typeof`来识别原始类型，但`null`除外，`null`必须与特殊值`null`直接比较。

引用类型是 JavaScript 中接近类的东西，对象是引用类型的实例。你可以使用`new`运算符或引用字面量来创建新对象。你主要通过点符号（dot notation）访问属性和方法，但也可以使用括号符号。函数在 JavaScript 中是对象，你可以通过`typeof`运算符来识别它们。你应该使用`instanceof`配合构造函数来识别任何其他引用类型的对象。

为了让原始值看起来更像引用，JavaScript 有三种原始包装类型：`String`、`Number`和`Boolean`。JavaScript 在后台创建这些对象，以便你可以像普通对象一样处理原始值，但一旦使用它们的语句完成，临时对象就会被销。尽管你可以创建自己的原始包装器实例，但最好不要这样做，因为这可能会引起困惑。

## 函数

如第 1 章所述，函数在 JavaScript 中实际上是对象。函数的定义特征——即它区别于任何其他对象的特征——是存在一个名为`[[Call]]`的*内部属性*。内部属性无法通过代码访问，而是定义了代码执行时的行为。ECMAScript 为 JavaScript 中的对象定义了多个内部属性，这些内部属性通过双方括号表示法指示。

`[[Call]]`属性是函数特有的，它表示该对象可以被执行。因为只有函数拥有此属性，所以 ECMAScript 定义`typeof`运算符对任何具有`[[Call]]`属性的对象返回`"function"`。这在过去导致过一些困惑，因为某些浏览器也为正则表达式包含了`[[Call]]`属性，从而导致它们被错误地识别为函数。现在所有浏览器的行为都都是相同的，因此`typeof`不再将正则表达式识别为函数。

本章讨论了在 JavaScript 中定义和执行函数的各种方式。由于函数是对象，它们的行为与其他语言中的函数不同，而这种行为对于深入理解 JavaScript 至关重要。

## 声明 vs 表达式

函数实际上有两种字面量形式。第一种是*函数声明*（function declaration），它以`function`关键字开头，并紧随其函数名。函数的内容包含在大括号中，如下声明所示：

```javascript
function add(num1, num2) {
  return num1 + num2;
}
```

第二种形式是*函数表达式*（function expression），它在`function`后面不需要名称。这些函数被认为是匿名的，因为函数对象本身没有名称。相反，函数表达式通常通过变量或属性引用，如下表达式所示：

```javascript
var add = function(num1, num2) {
  return num1 + num2;
};
```

这段代码实际上将一个值赋值给变量`add`。函数表达式与函数声明相同，除了缺少名称和结尾的分号。赋值表达式通常以分号结束，就像赋值任何其他值一样。

尽管这两种形式非常相似，但它们在一个非常重要的点上不同。函数声明会在代码执行时*提升*到上下文（即声明所在的函数或全局作用域）的顶部。这意味着你可以在代码中使用函数后再定义它而不会产生错误。例如：

```javascript
var result = add(5, 5);

function add(num1, num2) {
  return num1 + num2;
}
```

这段代码看起来会导致错误，但它运行正常。这是因为 JavaScript 引擎会将函数声明提升到顶部，并实际上按照如下方式执行代码：

```javascript
// JavaScript 引擎解释代码

function add(num1, num2) {
  return num1 + num2;
}

var result = add(5, 5);
```

函数提升只发生在函数声明中，因为函数名是预先知的。函数表达式无法提升，因为函数只能通过变量引用。所以这段代码会导致错误：

```javascript
// 错误！
var result = add(5, 5);

var add = function(num1, num2) {
  return num1 + num2;
};
```

只要你在使用函数之前定义它们，就可以使用函数声明或函数表达式。

## 作为值的函数

由于 JavaScript 支持一等函数（first-class functions），你可以像处理其他对象一样使用它们。你可以将它们赋值给变量、添加到对象中、作为参数传递给其他函数，并从函数返回。基本上，你可以在任何可以使用其他引用值的地方使用函数。这使得 JavaScript 函数变得异常强大。考虑以下示例：

```javascript
function sayHi() {
  console.log("Hi!");
}

sayHi(); // 输出 "Hi!"

var sayHi2 = sayHi;

sayHi2(); // 输出 "Hi!"
```



在这段代码中，有一个`sayHi`的函数声明。随后创建了一个名为`sayHi2`的变量并将其赋值为`sayHi`的值。现在`sayHi`和`sayHi2`都指向同一个函数，这意味着其中任何一个都可以执行，且结果相同。为了理解为什么会发生这种情况，请使用`Function`构造函数重写的相同代码：

```javascript
var sayHi = new Function("console.log(\"Hi!\");");

sayHi(); // 输出 "Hi!"

var sayHi2 = sayHi;

sayHi2(); // 输出 "Hi!"
```

`Function`构造函数更显式地表明`sayHi`可以像任何其他对象一样传递。当你记住函数也是对象时，很多行为就会变得容易理解。

例如，你可以将一个函数作为参数传递给另一个函数。JavaScript 数组上的`sort()`方法接受一个比较函数作为可选参数。当数组中的两个值需要进行比较时，就会调用该比较函数。如果第一个值小于第二个值，比较函数必须返回一个负数。如果第一个值大于第二个值，函数必须返回一个正数。如果两个值相等，函数应该返回零。

默认情况下，`sort()`会将数组中的每一项转换为字符串然后进行比较。这意味着如果不指定比较函数，你就无法准确地对数字数组排序。例如，你需要包含一个比较函数来准确地排序数字数组，如下：

```javascript
var numbers = [1, 5, 8, 4, 7, 10, 2, 6];

numbers.sort(function(first, second) {
 return first - second;
});

console.log(numbers); // "[1, 2, 4, 5, 6, 7, 8, 10]"

numbers.sort();

console.log(numbers); // "[1, 10, 2, 4, 5, 6, 7, 8]"
```

在这个示例中，传递给`sort()`的比较函数实际上是一个函数表达式。注意，该函数没有名称；它仅作为传递给另一个函数的引用存在（使其成为一个*匿名函数*）。两个值相减可以从比较函数返回正确的结果。

函数 **21**

与第二次调用`sort()`相比，后者没有使用比较函数。数组的顺序与预期不同，因为 1 后面跟着的是 10。这是因为默认比较在比较之前会将所有值转换为字符串。

## 参数

JavaScript 函数的另一个独特之处点是，你可以向任何函数传递任意数量的参数而不会引起错误。这是因为函数参数实际上存储在一个名为`arguments`的类数组结构中。就像普通的 JavaScript 数组一样，`arguments`可以增长并包含任意数量的值。这些值通过数字索引进行引用，并有一个`length`属性来确定存在多少个值。

`arguments`对象在任何函数内部都是可用的。这意味着函数中的命名参数的存在主要是为了方便，实际上并不会限制函数可以接受的参数数量。

**注意**：`arguments`对象不是`Array`的实例，因此不具有与数组*相同的方法*；`Array.isArray(arguments)`总是返回`false`。

另一方面，JavaScript 并没有忽略函数的命名参数。函数期望的参数数量存储在函数的`length`属性上。请记住，函数实际上只是一个对象，因此它可以拥有属性。`length`属性表示函数的*元数*（arity），即它期望的参数数量。在 JavaScript 中，知道函数的元数是非常重要的，因为如果你传递了过多或过少的参数，函数不会抛错误。

这里有一个使用`arguments`和函数元数的简单示例；注意传递给函数的参数数量对报告的元数没有影响：

```javascript
function reflect(value) {
 return value;
}

console.log(reflect("Hi!")); // "Hi!"
console.log(reflect("Hi!", 25)); // "Hi!"
console.log(reflect.length); // 1

reflect = function() {
 return arguments[0];
};

console.log(reflect("Hi!")); // "Hi!"
console.log(reflect("Hi!", 25)); // "Hi!"
console.log(reflect.length); // 0
```

**22 第 2 章**

这个示例首先使用单个命名参数定义了`reflect()`函数，但当向函数传递第二个参数时，并没有报错。同样，`length`属性为 1，是因为存在一个命名参数。随后在没有命名参数的情况下重新定义了`reflect()`函数；它返回`arguments[0]`，即传入的第一个参数。这个新版本的函数工作方式与之前的版本完全相同，但它的`length`为 0。

`reflect()`的第一个实现要容易理解得多，因为它使用了命名参数（就像在其他语言中那样）。使用`arguments`对象的版本可能会令人困惑，因为没有命名参数，你必须阅读函数体来确定是否使用了`arguments`。这就是为什么许多开发者倾向于在非必要的情况下避免使用`arguments`。

然而，有时使用`arguments`实际上比命名参数更有效。例如，假设你想创建一个接受任意数量参数并返回它们总和的函数。你无法使用命名参数，因为你不知道需要多少个，在这种情况下，使用`arguments`是最佳选择。

```javascript
function sum() {
 var result = 0,
 i = 0,
 len = arguments.length;
 while (i < len) {
 result += arguments[i];
 i++;
 }
 return result;
}

console.log(sum(1, 2)); // 3
console.log(sum(3, 4, 5, 6)); // 18
console.log(sum(50)); // 50
console.log(sum()); // 0
```

`sum()`函数接受任意数量的参数，并通过`while`循环遍历`arguments`中的值来将它们相加。这与你相加一个数字数组完全相同。即使在没有传递参数时，该函数也能工作，因为`result`初始化为 0。

大多数面向对象的语言都支持*函数重载*（function overloading），即单个函数拥有多个*签名*的能力。函数签名由函数名加上函数期望的参数数量和类型组成。因此，单个函数可以有一个接受单个字符串参数的签名，以及另一个接受两个数字参数的签名。语言会根据传入的参数来决定调用哪个版本的函数。

如前所述，JavaScript 函数可以接受任意数量的参数，而且函数接受的参数类型完全没有指定。这意味着 JavaScript 函数实际上没有签名。缺乏函数签名意味着没有函数重载。看看尝试声明两个同名函数时会发生什么：

```javascript
function sayMessage(message) {
 console.log(message);
}

function sayMessage() {
 console.log("Default message");
}

sayMessage("Hello!"); // 输出 "Default message"
```

如果这是另一种语言，`sayMessage("Hello!")`的输出可能是 "Hello!"。但在 JavaScript 中，当你定义了多个同名的函数时，代码中最后出现的那个胜出。早期的函数声明会被完全移除，最后的是被使用的。再次强调，使用对象来思考这种情况会有帮助：

```javascript
var sayMessage = new Function("message", "console.log(message);");

sayMessage = new Function("console.log(\"Default message\\");");

sayMessage("Hello!"); // 输出 "Default message"
```

通过这种方式观察代码可以清楚地解释为什么之前的代码不起作用。函数对象连续两次赋值给`sayMessage`，所以第一个函数对象丢失是合理的。

24 第 2 章

JavaScript 中函数没有签名（signatures），这并不意味着你不能模拟函数重载。你可以使用`arguments`对象获取传入的参数个数，并利用这些信息来决定执行的操作。例如：

```javascript
function sayMessage(message) {
  if (arguments.length === 0) {
    message = "Default message";
  }
  console.log(message);
}

sayMessage("Hello!"); // 输出 "Hello!"
```

在这个示例中，`sayMessage()`函数的行为根据传入参数的数量而有所不同。如果没有传入任何参数（`arguments.length === 0`），则使用默认消息。否则，使用第一个参数作为消息。这比其他语言中的函数重载稍微复杂一些，但最终结果是相同的。如果你真的想检查不同的数据类型，可以使用`typeof`和`instanceof`。

**注意**：在实践中，检查具名参数是否为`undefined`比依赖`arguments.length`更常见。

如第 1 节所述，你可以随时向对象添加或删除属性。当一个属性值实际上是一个函数时，该属性就被视为一个方法。你可以像添加属性一样向对象添加方法。例如，在以下代码中，`person`变量被赋值了一个带有`name`属性和一个名为`sayName`方法的对象字面量。

```javascript
var person = {
  name: "Nicholas",
  sayName: function() {
    console.log(person.name);
  }
};

person.sayName(); // 输出 "Nicholas"
```

注意，数据属性和方法的语法完全相同——一个标识符后跟一个冒号，然后是值。在`sayName`的情况下，该值恰好是一个函数。然后你可以直接从对象调用该方法，如`person.sayName("Nicholas")`。

函数 25 页

### `this`对象 (The this Object)

你可能在上一个示例中发现了一些奇怪的地方。`sayName()`方法直接引用了`person.name`，这在方法和对象之间创建了紧耦合。由于许多原因这都是问题。首先，如果你更改了变量名，也需要记得更改方法中对该名的引用。其次，这种紧耦合使得很难对不同的对象使用同一个函数。幸运的是，JavaScript 有解决此问题的方法。

JavaScript 中的每个作用域都有一个`this`对象，它代表函数的调用对象。在全局作用域中，它代表全局对象（在浏览器中为`window`）。当函数在附加到对象上时被调用时，`this`的值默认等于该对象。因此，与其在方法内部直接引用对象，不如而是引用`this`。例如，你可以重写上一个示例的代码来使用`this`：

```javascript
var person = {
  name: "Nicholas",
  sayName: function() {
    console.log(this.name);
  }
};

person.sayName(); // 输出 "Nicholas"
```

这段代码的作用与之前的版本相同，但这次`sayName()`引用的是`this`而不是`person`。这意味着你可以轻松地更改变量名，甚至在不同的对象上复用该函数。

```javascript
function sayNameForAll() {
  console.log(this.name);
}

var person1 = {
  name: "Nicholas",
  sayName: sayNameForAll
};

var person2 = {
  name: "Greg",
  sayName: sayNameForAll
};

var name = "Michael";

person1.sayName(); // 输出 "Nicholas"
person2.sayName(); // 输出 "Greg"
sayNameForAll(); // 输出 "Michael"
```

在这个示例中，首先定义了一个名为`sayName`的函数。然后创建了两个对象字面量，将`sayName`赋值为`sayNameForAll`函数。函数只是引用值，因此你可以将它们作为属性值赋值给任意数量的对象。当在`person1`上调用`sayName()`时，它输出 "Nicholas"；当在`person2`上调用时，它输出 "Greg"。这是因为这是在函数调用时设置的，所以`this.name`是准确的。

该示例的最后部分定义了一个名为`name`的全局变量。当直接调用`sayNameForAll()`时，它输出 "Michael"，因为全局变量被视为全局对象的一个属性。

### 改变`this` (Changing this)

使用和操作函数`this`值的能力是 JavaScript 中良好的面向对象编程的关键。函数可以在许多不同的语境中使用，并且需要在每种情况下都能工作。尽管这通常是自动分配的，但你可以更改它的值以实现不同的目标。有三个方法允许你更改`this`的值。（记住，函数是对象，对象可以有方法，所以函数也可以。）

#### `call()`方法 (The call() Method)

用于操作`this`的第一个函数方法是`call()`，它以特定的`this`值和特定的参数执行函数。`call()`的第一个参数是函数执行时`this`应该相等的值。所有后续参数都是应该传递给函数的参数。例如，假设你更新了`sayNameForAll()`使其接收一个参数：

```javascript
function sayNameForAll(label) {
  console.log(label + ":" + this.name);
}

var person1 = {
  name: "Nicholas"
};

var person2 = {
  name: "Greg"
};

var name = "Michael";

sayNameForAll.call(this, "global"); // 输出 "global:Michael"
sayNameForAll.call(person1, "global"); // 输出 "global:Nicholas"
sayNameForAll.call(person2, "global"); // 输出 "global:Greg"
```

*(注：此处原文示例代码存在逻辑偏差，`call(this, "global")`在全局作用域中会指向`window`，此处翻译保持逻辑对齐)*

根据原文逻辑，假设你更新了`sayNameForAll()`以接收一个参数：

```javascript
function sayNameForAll(label) {
  console.log(label + ":" + this.name);
}

var person1 = {
  name: "Nicholas"
};

var person2 = {
  name: "Greg"
};

var name = "Michael";

sayNameForAll.call(window, "global"); // 输出 "global:Michael"
sayNameForAll.call(person1, "global"); // 输出 "global:Nicholas"
sayNameForAll.call(person2, "global"); // 输出 "global:Greg"
```

(纠正：原文提供的示例代码在此处混乱，此处按逻辑翻译)

在这个示例中，首先定义了一个名为`sayName`的函数。然后创建两个对象字面量，将`sayName`赋值为`sayNameForAll`函数。函数只是引用值，因此你可以将它们作为属性值赋值给任意数量的对象。当在`person1`上调用`sayName()`时，它输出 "Nicholas"；在`person2`上调用时，它输出 "Greg"。这是因为这是在函数调用时设置的，所以`this.name`是准确的。

该示例的最后部分定义了一个名为`name`的全局变量。当直接调用`sayNameForAll()`时，它输出 "Michael"，因为全局变量被视为全局对象的一个属性。

### 改变`this` (Changing this)

使用和操作函数`this`值的能力是 JavaScript 中良好的面向对象编程的关键。函数可以在许多不同的语境中使用，并且需要在每种情况下都能工作。尽管这通常是自动分配的，但你可以更改它的值以实现不同的目标。有三个方法允许你更改`this`的值。（记住，函数是对象，对象可以有方法，所以函数也可以。）

#### `call()`方法 (The call() Method)

用于操作`this`的第一个函数方法是`call()`，它以特定的`this`值和特定的参数执行函数。`call()`的第一个参数是函数执行时`this`应该相等的值。所有后续参数都是应该传递给函数的参数。例如，假设你更新了`sayNameForAll()`以接收一个参数：

```javascript
function sayNameForAll(label) {
  console.log(label + ":" + this.name);
}
```



```
console.log(label + ":" + this.name);
```

`var person1 = { name: "Nicholas" };`

`var person2 = { name: "Greg" };`

`var name = "Michael";`

`sayNameForAll.call(window, "global");` // 输出 "global:Michael"

`sayNameForAll.call(person1, "global");` // 输出 "global:Nicholas"

`sayNameForAll.call(person2, "global");` // 输出 "global:Greg"

函数 27 页

在这个示例中，首先定义了一个名为 `sayName` 的函数。然后创建两个对象字面量，将 `sayName` 赋值为 `sayNameForAll` 函数。函数只是引用值，因此你可以将它们作为属性值赋值给任意数量的对象。当在 `person1` 上调用 `sayName()` 时，它输出 "Nicholas"；在 `person2` 上调用时，它输出 "Greg"。这是因为这是在函数调用时设置的，所以 `this.name` 是准确的。

该示例的最后部分定义了一个名为 `name` 的全局变量。当直接调用 `sayNameForAll()` 时，它输出 "Michael"，因为全局变量被视为全局对象的一个属性。

#### `apply()` 方法 (The apply() Method)

用于操作 `this` 的第二个函数方法是 `apply()`，它以特定的 `this` 值和特定的参数数组执行函数。`apply()` 的第一个参数是函数执行时 `this` 应该相等的值。所有后续参数都是应该传递给函数的参数。例如，假设你更新了 `sayNameForAll()` 以接收一个参数：

```javascript
function sayNameForAll(label) {
  console.log(label + ":" + this.name);
}

var person1 = {
  name: "Nicholas"
};

var person2 = {
  name: "Greg"
};

var name = "Michael";

sayNameForAll.apply(window, ["global"]); // 输出 "global:Michael"
sayNameForAll.apply(person1, ["global"]); // 输出 "global:Nicholas"
sayNameForAll.apply(person2, ["global"]); // 输出 "global:Greg"
```

## 函数 29

**总结**

JavaScript 函数的独特之处在于它们同时也是对象，这意味着它们可以被访问、复制、覆盖，并且像任何其他对象值一样被处理。JavaScript 函数与其他对象之间最大的区别在于一个特殊的内部属性 `[[Call]]`，它包含了函数的执行指令。`typeof` 运算符会在对象上查找此内部属性，如果找到，则返回 "function"。

函数有两种字面量形式：声明和和表达式。函数声明在 `function` 关键字的右侧包含函数名，并会被提升到其定义所在上下文的顶部。函数表达式则用于可以使用其他值的地方，例如赋值表达式、函数参数或另一个函数的返回值。

由于由于函数是对象，因此存在一个 `Function` 构造函数。你可以使用 `Function` 构造函数创建新函数，但通常不建议这样做，因为这可能会让代码变得难以理解，并使调试变得困难得多。尽管如此，在某些运行时未知函数真实形式的情况下，你可能会经常遇到它的用法。

你需要熟练掌握函数，才能理解 JavaScript 中面向对象编程是如何运作的。由于 JavaScript 没有类（class）的概念，函数和其他对象就是你实现聚合和继承所拥有的全部。

# 3 理解对象

尽管 JavaScript 中有很多内置引用类型，但你很可能会频繁地创建自己的对象。在创建时，请记住 JavaScript 中的对象是动态的，这意味着它们可以在代码执行的任何点发生变化。基于类的语言根据类定义锁定对象，而 JavaScript 对象没有这种限制。

JavaScript 编程很大一部分是为了管理这些对象，这就是为什么理解对象的工作原理是理解整个 JavaScript 的关键。这将在章后面的部分进行详细讨论。

## 定义属性

回顾第 1 章，创建自定义对象有两种基本方法：使用 `Object` 构造函数和使用对象字面量。例如：

```javascript
var person1 = {
  name: "Nicholas"
};

var person2 = new Object();
person2.name = "Nicholas";

person1.age = "Redacted";
person2.age = "Redacted";

person1.name = "Greg";
person2.name = "Michael";
```

`person1` 和 `person2` 都是带有 `name` 属性的对象。在示例之后，两个对象都被分配了 `age` 属性。你可以在定义对象后立即这样做，也可以在很久之后这样做。除非另有指定，否则你创建的对象始终是开放修改的（更多信息请见第 45 页的“防止对象修改”）。此示例的最后部分更改了每个对象 `name` 的值；属性值也可以随时更改。

当属性首次添加到对象中时，JavaScript 在该对象上使用一个名为 `[[Put]]` 的内部方法。`[[Put]]` 方法在对象中创建一个位置来存储该属性。你可以将其此比为第一次向哈希表中添加一个键。此操作不仅指定了初始值，还指定了属性的一些特性。因此，在先前的示例中，当每个对象上首次定义 `name` 和 `age` 属性时，每个属性都会调用 `[[Put]]` 方法。

调用 `[[Put]]` 的结果是在对象上创建了一个*自有属性*（own property）。自有属性仅表示该对象的特定实例拥有该属性。属性直接存储在实例上，对该属性的所有操作必须通过该对象执行。

**注意** 自有属性区别于*原型属性*（prototype properties），后者将在*第 4 章*中讨论。

当一个新值赋值给现有属性时，会发生称为 `[[Set]]` 的独立操作。该操作将属性的当前值替换为新值。在先前的示例中，将 `name` 设置为第二个值会导致调用 `[[Set]]`。参见图 3-1，查看 `person1` 的 `name` 和 `age` 属性更改时在后台发生的逐步过程。

| 对象 | 属性 | 值 | 操作 |
| :--- | :--- | :--- | :--- |
| person1 | name | "Nicholas" | `[[Put]]` |
| person1 | age | "Redacted" | `[[Put]]` |
| person1 | name | "Greg" | `[[Set]]` |
| person1 | age | "Redacted" | `[[Put]]` |

*图 3-1：添加和更改对象的属性*

在图的第一部分，使用对象字面量创建了 `person1` 对象。这为 `name` 属性执行了隐式的 `[[Put]]`。为 `person1.age` 赋值对 `age` 属性执行了 `[[Put]]`。然而，将 `person1.name` 设置为新值（"Greg"）对 `name` 属性执行了 `[[Set]]` 操作，覆盖了现有的属性值。

## 检测属性

由于属性可以随时添加，因此有时需要检查对象中是否存在某个属性。新的 JavaScript 开发者经常错误地使用如下的模式来检测属性是否存在：

```javascript
// 不不可靠
if (person1.age) {
  // 对 age 进行某些操作
}
```

这种模式的问题在于 JavaScript 的类型转换如何影响结果。如果值是*真值*（对象、非空字符串、非零数字或 true），则 `if` 条件为真；如果值是*假值*（null、undefined、0、NaN 或空字符串），则结果为假。由于对象属性可能包含这些假值，该示例代码可能会产生假阴性结果。例如，如果 `person1.age` 为 0，即使该属性存在，`if` 条件也不会满足。测试属性存在的更可靠方法是使用 `in` 运算符。

`in` 运算符在特定对象中查找指定的属性，如果找到，则返回 true。实际上，`in` 运算符检查给定的键是否存在于哈希表中。例如，这里是使用 `in` 检查 `person1` 中某些属性的情况：

```javascript
console.log("name" in person1); // true
console.log("age" in person1); // true
console.log("title" in person1); // false
```

记住方法只是引用函数的属性，因此你可以以相同的方式检查方法是否存在。以下代码向 `person1` 添加了一个新函数 `sayName()`，并使用 `in` 确认其存在。

```javascript
var person1 = {
  name: "Nicholas",
  sayName: function() {
    console.log(this.name);
  }
};

console.log("sayName" in person1); // true
```

在大多数情况下，`in` 运算符是判断属性是否存在于对象的最佳方法。它的优点是不评估属性的值，如果这种评估可能导致性能问题或错误，这一点非常重要。

然而，在某些情况下，你可能只想在属性是自有属性时才检查其是否存在。`in` 运算符会检查自有属性和原型属性，因此你需要不同的方法。引入 `hasOwnProperty()` 方法，它存在于所有对象上，并且仅当给定属性存在且为自有属性时才返回 true。例如，以下代码对比了在 `person1` 不同属性上使用 `in` 与 `hasOwnProperty()` 的结果：

```javascript
var person1 = {
  name: "Nicholas",
  sayName: function() {
    console.log(this.name);
  }
};

console.log("name" in person1); // true
console.log(person1.hasOwnProperty("name")); // true

console.log("toString" in person1); // true
console.log(person1.hasOwnProperty("toString")); // false
```

## 理解对象 **35**

在例示例中，name 是 person1 的一个自有属性，因此 `in` 运算符和 `hasOwnProperty()` 都返回 `true`。然而，`toString()` 方法是一个原型属性，存在于所有对象上。`in` 运算符对 `toString()` 返回 `true`，但 `hasOwnProperty()` 返回 `false`。这是一个重要的区别，将在第 4 章中进一步讨论。

## 移除属性

正如属性可以随时添加到对象一样，它们也可以被移除。尽管如此，简单地将属性设置为 `null` 并不会真正从对象中完全删除该属性。这种操作会调用值为 `null` 的 `[[Set]]`，正如你在本章前面的部分看到的，这只是替换了属性的值。你需要使用 `delete` 运算符从对象中完全删除属性。

`delete` 运算符作用于单个对象属性并调用一个名为 `[[Delete]]` 的内部操作。你可以将这种操作想象为从哈希表中删除一个键值对。当 `delete` 运算符执行成功时，它返回 `true`。（某些属性无法删除，这将在章节稍后部分详细讨论。）例如，下面的列表显示了 `delete` 运算符的工作：

```javascript
var person1 = {
  name: "Nicholas"
};

console.log("name" in person1); // true

delete person1.name; // true - 无输出

console.log("name" in person1); // false
console.log(person1.name); // undefined
```

在此示例中，name 属性已从 person1 中删除。操作完成后，`in` 运算符返回 `false`。此外，请注意，访问不存在的属性将只会返回 `undefined`。图 3-2 显示了 `delete` 如何影响对象。

| person1 | |
| :--- | :--- |
| name | "Nicholas" |
| delete person1.name; | |

图 3-2：当**删除** **name** 属性时，它会从 **person1** 中完全消失。

## 枚举

默认情况下，你添加到对象的所有属性都是*可枚举的*，这意味着你可以使用 `for-in` 循环对它们进行迭代。可枚举属性的其内部 `[[Enumerable]]` 属性被设置为 `true`。`for-in` 循环枚举对象上的所有可枚举属性，并将属性名赋值给变量。例如，下面的循环输出了对象的属性名和属性值：

```javascript
var property;

for (property in object) {
  console.log("Name: " + property);
  console.log("Value: " + object[property]);
}
```

每通过一次 `for-in` 循环，属性变量就会被对象上的下一个可枚举属性填充，直到所有此类属性都被使用完毕。在此时，循环结束，代码继续执行。此示例使用方括号表示法来获取对象属性的值并将其输出到控制台，这是 JavaScript 中方括号表示法的主要用例之一。

如果你只需要一个对象的属性列表以供稍后在程序中使用，ECMAScript 5 引入了 `Object.keys()` 方法来获取一个可枚举属性名的数组，如下所示：

```javascript
var properties = Object.keys(object);

// 如果你想模拟 for-in 的行为
var i, len;

for (i=0, len=properties.length; i < len; i++){
  console.log("Name: " + properties[i]);
  console.log("Value: " + object[properties[i]]);
}
```

此示例使用 `Object.keys()` 从对象中获取可枚举属性。然后使用 `for` 循环遍历属性并输出名称和值。通常，当你想要对属性名数组进行操作时会使用 `Object.keys()`，而在不需要数组时使用 `for-in`。

**注意** `for-in` 循环返回的可枚举属性与 `Object.keys()` 返回的属性之间存在差异。`for-in` 循环还会枚举原型属性，而 `Object.keys()` 只返回自有（实例）属性。原型属性和自有属性之间的区别在于。

## 理解对象 **37**

记住，并不是所有属性都是可枚举的。事实上，大多数原生属性默认都是可枚举的。你可以使用 `propertyEnumerable()` 方法检查属性是否是可枚举的，其方法如下：

```javascript
var person1 = {
  name: "Nicholas"
};

console.log("name" in person1); // true

var properties = Object.keys(person1);

console.log("length" in properties); // true
console.log(person1.propertyEnumerable("length")); // false
```

## 属性类型

属性有两种类型：数据属性和访问器属性。*数据属性*包含一个值，如前面的示例所示。*访问器属性*不包含值，而是定义了一个在读取属性时调用的函数（称为 *getter*，获取器）和一个在写入属性时调用的函数（称为 *setter*，设定器）。访问器属性需要 getter 或 setter，尽管它们可以两者兼备。

使用对象定义访问器属性有一种特殊的句语法：

```javascript
var person1 = {
  _name: "Nicholas",

  get name() {
    console.log("Reading name");
    return this._name;
  },

  set name(value) {
    console.log("Setting name to", value);
    this._name = value;
  }
};

console.log(person1.name); // 输出 "Reading name" 然后 "Nicholas"

person1.name = "Greg";

console.log(person1.name); // 输出 "Setting name to Greg" 然后 "Reading name" 然后 "Greg"
```



此示例定义了一个访问器属性。有一个名为 `_name` 的数据属性，包含了该属性的实际值（前下划线是一种常用约定，表示该属性被认为是私有的，尽管实际上它仍然是公开的）。尽管此示例使用 `_name` 来存储数据，你也可以将数据存储在变量或其他对象中。此示例只是为属性的行为增加了日志；如果你只是将数据存储在另一个属性中，通常没有理由使用访问器属性——直接使用属性即可。访问器属性在赋值需要触发某种行为或读取值需要计算所需的返回值时最有用。

ECMAScript 5 改变了这一点，引入了多种直接与属性交互的方法，并引入了新的属性以支持额外功能。现在可以创建与内置 JavaScript 属性行为相同的属性。本节将详细介绍数据属性和访问器属性的属性，从它们共同拥有的属性开始。

## 通用属性

数据属性和访问器属性之间共享两个属性标记。一个是[[可枚举性]]（`Enumerable`），它决定了你是否可以遍历该属性。另一个是[[可配置性]]（`Configurable`），它决定了该属性是否可以被更改。你可以使用 `delete` 删除一个可配置的属性，并随时更改其属性。（这意味着可配置的属性可以从数据属性变为访问器属性，反之亦然）。默认情况下，你在对象上声明的所有属性都是可枚举且可配置的。

如果你想更改属性标记，可以使用 `Object.defineProperty()` 方法。该方法接受三个参数：拥有该属性的对象、属性名，以及一个包含要设置属性的*属性描述符*（`property descriptor`）对象。描述符的属性名称与内部属性同名，但没有方括号。因此，你使用 `enumerable` 来设置[[可枚举性]]，使用 `configurable` 来设置[[可配置性]]。例如，假设你想让对象的属性变为不可枚举且不可配置的：

```javascript
var person1 = {
  name: "Nicholas"
};

Object.defineProperty(person1, "name", {
  enumerable: false
});

console.log("name" in person1); // true
console.log(person1.propertyIsEnumerable("name")); // false

var properties = Object.keys(person1);
console.log(properties.length); // 0

Object.defineProperty(person1, "name", {
  configurable: false
});

// 尝试删除属性
delete person1.name;
console.log("name" in person1); // true
console.log(person1.name); // "Nicholas"

Object.defineProperty(person1, "name", { // 错误！！！
  configurable: true
});
```

`name` 属性像往常一样被定义，但随后被修改以将其[[可枚举性]]属性设置为 `false`。现在 `.propertyIsEnumerable()` 方法返回 `false`，因为它引用了[[可枚举性]]的新值。

此后，`name` 被更改为不可配置的。从现在起，任何删除 `name` 的尝试将失败，因为该属性无法更改，所以 `name` 仍然存在于 `person1` 上。再次对 `name` 调用 `Object.defineProperty()` 也会导致属性不再发生任何进一步变化。实际上，`name` 已作为 `person1` 上的属性被锁定。

最后一段代码尝试再次将 `name` 定义为可配置。然而，这将抛出一个错误，因为你不能再次让一个不可配置的属性变为可配置。在这种情况下，尝试将数据属性更改为访问器属性或反之也应该抛出错误。

**注意**：当 JavaScript 在严格模式下运行时，尝试删除不可配置的属性会导致错误。在非严格模式下，该操作将静默失败。

## 数据属性标记

数据属性拥有访问器属性不具备的两个额外属性。第一个是[[值]]（`Value`），它存储属性值。当你在对象上创建属性时，该属性会自动填充。所有属性值都存储在[[值]]中，即使该值是一个函数。第二个属性是[[可写性]]（`Writable`），它是一个布尔值，指示属性是否可以写入。默认情况下，除非另有指定，所有属性都是可写的。

通过这两个额外属性，即使属性尚不存在，你也可以使用 `Object.defineProperty()` 完全定义一个数据属性。考虑以下代码：

```javascript
var person1 = {
  name: "Nicholas"
};
```

你在整个章节中都见过这段代码片段；它为 `person1` 添加了 `name` 属性并设置了它的值。你可以使用以下（更冗长的）代码实现相同的结果：

```javascript
var person1 = {};

Object.defineProperty(person1, "name", {
  value: "Nicholas",
  enumerable: true,
  configurable: true,
  writable: true
});
```

当调用 `Object.defineProperty()` 时，它首先检查属性是否存在。如果属性不存在，则会根据描述符中指定的属性添加一个新属性。在这种情况下，`name` 并不是 `person1` 的现有属性，因此它被创建了。

当你使用 `Object.defineProperty()` 定义新属性时，指定所有属性是非常重要的，因为否则布尔属性会自动默认为 `false`。例如，以下代码创建了一个不可枚举、不可配置且不可写的 `name` 属性，因为在调用 `Object.defineProperty()` 时，没有显式地将其中任何一个属性设置为 `true`。

```javascript
var person1 = {};

Object.defineProperty(person1, "name", {
  value: "Nicholas"
});

console.log("name" in person1); // true
console.log(person1.propertyIsEnumerable("name")); // false

delete person1.name;
console.log("name" in person1); // true

person1.name = "Greg";
console.log(person1.name); // "Nicholas"
```

在这段代码中，除了读取值外，你无法对 `name` 属性进行任何操作；其他所有操作都被锁定。如果你正在更改现有属性，请记住只有你指定的属性会发生改变。

**注意**：在严格模式下，尝试更改不可写属性的值时会抛出错误。在非严格模式下，该操作将静默失败。

## 访问器属性标记

访问器属性也有两个额外属性。由于访问器属性不存储值，因此不需要[[值]]或[[可写性]]。相反，访问器具有[[get]]（`Get`）和[[set]]（`Set`），它们分别包含 getter 和 setter 函数。与 getter 和 setter 的对象字面量形式一样，你只需要定义这些属性之一即可创建属性。

**注意**：如果你尝试创建一个同时具有数据和访问器属性的属性，将得到一个错误。

使用访问器属性而不是对象字面量符号来定义访问器属性的优势在于，你可以在现有对象上定义这些属性。如果你想使用对象字面量符号，需要在创建对象时定义访问器属性。与数据属性一样，你也可以指定访问器属性是否可配置或可枚举。考虑之前的示例：

```javascript
var person1 = {
  _name: "Nicholas",
  get name() {
    console.log("Reading name");
    return this._name;
  },
  set name(value) {
    console.log("Setting name to %s", value);
    this._name = value;
  }
};
```

这段代码也可以写成：

```javascript
var person1 = {
  _name: "Nicholas"
};

Object.defineProperty(person1, "name", {
  get: function() {
    console.log("Reading name");
    return this._name;
  },
  set: function(value) {
    console.log("Setting name to %s", value);
    this._name = value;
  },
  enumerable: true,
  configurable: true
});
```

注意传递给 `Object.defineProperty()` 的对象上的 `get` 和 `set` 键是包含函数的属性属性。在这里你可以使用对象字面量格式。

设置其他属性（[[可枚举性]]和[[可配置性]]）允许你更改访问器属性的工作方式。例如，你可以这样创建一个不可配置、不可枚举且不可写的属性：

```javascript
var person1 = {
  _name: "Nicholas"
};

Object.defineProperty(person1, "name", {
  get: function() {
    console.log("Reading name");
    return this._name;
  }
});

console.log("name" in person1); // true
console.log(person1.propertyIsEnumerable("name")); // false

delete person1.name;
console.log("name" in person1); // true

person1.name = "Greg";
console.log(person1.name); // "Nicholas"
```

在这段代码中，`name` 属性是一个只有一个 getter 的访问器属性。没有 setter 或任何显式设置为 `true` 的其他属性，因此值可以读取但不能更改。

**注意**：与通过对象字面量定义的访问器属性一样，没有 setter 的访问器属性在尝试更改值时会在严格模式下抛出错误。在非严格模式下，该操作将静默失败。尝试读取仅定义了 setter 的访问器属性始终返回 `undefined`。

## 定义多个属性

如果你使用 `Object.defineProperties()` 代替 `Object.defineProperty()`，则也可以同时在对象上定义多个属性。该方法接受两个参数：要处理的对象和一个包含所有属性信息的对象。第二个参数的键是属性名，值是定义这些属性标记的描述符对象。例如，以下代码定义了两个属性：

```javascript
var person1 = {};

Object.defineProperties(person1, {
  // 存储数据的属性
  _name: {
    value: "Nicholas",
    enumerable: true,
    configurable: true,
    writable: true
  }
});
```

## 第 3 章

```javascript
// accessor property
name: {
  get: function() {
    console.log("Reading name");
    return this._name;
  },
  set: function(value) {
    console.log("Setting name to %s", value);
    this._name = value;
  },
  enumerable: true,
  configurable: true
}
```

此示例将 `_name` 定义为包含信息的数据属性，并将 `name` 定义为访问属性（`accessor property`）。你可以使用 `Object.defineProperties()` 定义任意数量的属性；甚至可以同时修改现有属性并创建新属性。其效果与多次调用 `Object.defineProperty()` 相同。

### 获取属性描述

如果你需要获取属性描述，可以在 JavaScript 中使用 `Object.getOwnPropertyDescriptor()` 来实现。如名所示，该方法仅作用于自有属性（own properties）。该方法接受两个参数：要操作的对象和要获取的属性名。如果属性存在，你将收到一个包含四个属性的描述符对象：`configurable`、`enumerable` 以及另外两个适用于该属性类型的属性。即使你没有特意设置某个属性，你仍会收到一个包含该属性相应值的对象。例如，这段代码创建了一个属性并检查了它的属性：

```javascript
var person1 = {
  name: "Nicholas"
};

var descriptor = Object.getOwnPropertyDescriptor(person1, "name");

console.log(descriptor.enumerable); // true
console.log(descriptor.configurable); // true
console.log(descriptor.writable); // true
console.log(descriptor.value); // "Nicholas"
```

在这里，名为 `name` 的属性作为对象字面量的一部分定义的。调用 `Object.getOwnPropertyDescriptor()` 返回了一个包含 `enumerable`、`configurable`、`writable` 和 `value` 的对象，尽管这些属性并没有通过 `Object.defineProperty()` 显式定义。

### 防止对象修改

对象和属性一样，具有控制行为的内部属性。这些属性之一是[[Extensible]]（可扩展），它是一个指示对象本身可以被修改的布尔值。你创建的所有对象默认都是*可扩展的*，这意味着可以随时向对象添加新属性。你在本章中已经见过几次了。通过将[[Extensible]]设置为 `false`，你可以防止向对象添加新属性。实现这一点的有三种不同的方法。

### 防止扩展

创建不可扩展对象的一种方法是使用 `Object.preventExtensions()`。该方法接受一个参数，即你想要变为不可扩展的对象。一旦你对某个对象使用了此方法，你就再也无法向其添加任何新属性。你可以使用 `Object.isExtensible()` 来检查[[Extensible]]的值。以下代码展示了两种方法的用法示例。

```javascript
var person1 = {
  name: "Nicholas"
};

console.log(Object.isExtensible(person1)); // true

Object.preventExtensions(person1);

console.log(Object.isExtensible(person1)); // false

person1.sayName = function() {
  console.log(this.name);
};

console.log("sayName" in person1); // false
```

在创建 `person1` 后，此示例在将其变为不可更改之前检查了对象的[[Extensible]]属性。现在 `person1` 是不可扩展的，`sayName()` 方法从未被添加到它上。

**注意**：在严格模式下，尝试向不可扩展对象添加属性将抛出错误。在非严格模式下，操作将静默失败。你应该始终对不可扩展对象使用严格模式，以便在不可扩展对象被错误使用时能够察觉。

### 封存对象

创建不可扩展对象的第二种方法是*密封*（seal）对象。被密封的对象是不可扩展的，且其所有属性都是不可配置的（nonconfigurable）。这意味着你不仅不能向对象添加新属性，也不能删除属性或更改其类型（从数据属性变为访问属性或反之亦然）。如果一个对象被密封了，你只能对其属性进行读取和写入。

你可以使用 `Object.seal()` 方法对对象进行密封。当这种情况发生时，[[Extensible]]属性被设置为 `false`，并且所有属性的[[Configurable]]属性都被设置为 `false`。你可以如下所示使用 `Object.isSealed()` 来检查对象是否被封存：

```javascript
var person1 = {
  name: "Nicholas"
};

console.log(Object.isExtensible(person1)); // true
console.log(Object.isSealed(person1)); // false

Object.seal(person1);

console.log(Object.isExtensible(person1)); // false
console.log(Object.isSealed(person1)); // true

person1.sayName = function() {
  console.log(this.name);
};

console.log("sayName" in person1); // false

person1.name = "Greg";
```



```javascript
console.log(person1.name); // "Greg"

delete person1.name;

console.log("name" in person1); // true

console.log(person1.name); // "Greg"

var descriptor = Object.getOwnPropertyDescriptor(person1, "name");

console.log(descriptor.configurable); // false
```

这段代码密封了`person1`，因此你无法添加或删除属性。由于所有密封的对象都是不可扩展的，当在`person1`上使用`Object.isExtensible()`时返回`false`，且添加`sayName()`方法的尝试静默失败了。此外，尽管`person1.name`成功更改了新值，但删除它的尝试失败了。

如果你熟悉 Java 或 C++，那么也应该熟悉密封对象。当你基于这些语言中的某个类创建新对象实例时，你不能向该对象添加任何新属性。然而，如果一个属性包含一个对象，你可以修改该对象。实际上，密封对象是 JavaScript 在不使用类的情况下为你提供同等控制力的方式。

**注意**：务必对密封对象使用严格模式，这样当有人尝试使用该对象时，你会得到一个错误。

### 冻结对象

创建不可扩展对象的最后方法是将其冻结（`freeze`）。如果一个对象被冻结了，你就不能添加或删除属性，不能更改属性类型，并且不能向任何数据属性写入。本质上，冻结的对象是一个密封对象，其数据属性也是只读的。冻结的对象无法被解冻，因此它们保持在变为冻结时的状态。你可以使用`Object.freeze()`冻结对象，并使用`Object.isFrozen()`判断一个对象是否被冻结。例如：

```javascript
var person1 = {
  name: "Nicholas"
};

console.log(Object.isExtensible(person1)); // true

console.log(Object.isSealed(person1)); // false

console.log(Object.isFrozen(person1)); // false

Object.freeze(person1);

console.log(Object.isExtensible(person1)); // false

console.log(Object.isSealed(person1)); // true

console.log(Object.isFrozen(person1)); // true

person1.sayName = function() {
  console.log(this.name);
};

console.log("sayName" in person1); // false

person1.name = "Greg";

console.log(person1.name); // "Nicholas"

delete person1.name;

console.log("name" in person1); // true

console.log(person1.name); // "Nicholas"

var descriptor = Object.getOwnPropertyDescriptor(person1, "name");

console.log(descriptor.configurable); // false

console.log(descriptor.writable); // false
```

在此示例中，`person1`被冻结了。冻结的对象也被认为是不可扩展和密封的，因此`Object.isExtensible()`返回`false`，`Object.isSealed()`返回`true`。属性属性无法更改，因此即使赋值为`"Greg"`，操作也失败了。

**注意**：冻结对象仅仅是对象在特定时间点的快照。它们的用途有限，应该极少使用。与所有不可扩展对象一样，你应该对冻结对象使用严格模式。

## 第 3 章

### 总结

将 JavaScript 对象想象成哈希表（属性只是键值对）是有帮助的。你可以使用点符号法或带有字符串标识符的括号符号法来访问对象属性。你可以通过给属性赋值来随时添加属性，也可以使用`delete`操作符随时删除属性。你始终可以通过在属性名和对象上使用`in`运算符来检查属性是否存在。如果该属性是自有属性（own property），你也可以使用每个对象都存在的`hasOwnProperty()`。所有对象的属性默认都是可枚举的，这意味着它们将出现在`for-in`循环中，或者通过`Object.keys()`获取。

属性有两种类型：数据属性和访问器属性。数据属性是值的占位符，你可以对其进行读取和写入。当数据属性持有一个函数值时，该属性被视为对象的方法。与数据属性不同，访问器属性本身不存储值；它们使用 getter 和 setter 的组合来执行特定操作。你可以直接使用对象字面量符号创建数据属性和访问器属性。

所有属性都有几个关联属性。这些属性定义了属性的工作方式。数据属性和访问器属性都有`[[Enumerable]]`（可枚举）和`[[Configurable]]`（可配置）属性。数据属性还有`[[Writable]]`（可写）和`[[Value]]`（值）属性，而访问器属性有`[[Get]]`和`[[Set]]`属性。默认情况下，所有属性的`[[Enumerable]]`和`[[Configurable]]`都设置为`true`，数据属性的`[[Writable]]`设置为`true`。你可以通过使用`Object.defineProperty()`或`Object.defineProperties()`来更改这些属性。还可以通过使用`Object.getOwnPropertyDescriptor()`获取这些属性。

当你想要以某种方式锁定对象的属性时，有三种不同的方法。如果你使用`Object.preventExtensions()`，对象将不再允许添加属性。你还可以使用`Object.seal()`方法创建一个密封对象（sealed object），这使得该对象变为不可扩展，并使其属性变为不可配置的。`Object.freeze()`方法会创建一个冻结的对象，它是一个具有不可写数据属性的密封对象。请小心不可扩展的对象，并始终使用严格模式（strict mode），这样错误访问对象的尝试将抛出错误。

### 构造函数与原型

在不理解构造函数和原型的情况下，你可能在 JavaScript 中走得相当远，但如果不良好掌握它们，你就无法真正领会这种语言。因为 JavaScript 缺乏类，它转而利用构造函数和原型为对象引入类似的顺序。但因为某些模式类似于类，并不意味着它们的行为相同。在本章中，你将详细探索构造函数和原型，查看 JavaScript 如何使用它们来创建对象。

## 构造函数

构造函数简单来说就是一个配合`new`使用用于创建对象的函数。到目前为止，你已经见过内置的 JavaScript 构造函数，例如`Object`、`Array`和`Function`。构造函数的优势在于，用相同构造函数创建的对象包含相同的属性和方法。如果你想创建多个相似的对象，可以创建自己的构造函数，从而创建你自己的引用类型。

由于构造函数只是一个函数，它的定义方式是相同的。唯一的区别是构造函数的名称应该大写字母开头，以便与其他函数区分来。例如，查看以下空的`Person`函数：

```javascript
function Person() {
  // 刻意留空
}
```

这个函数是一个构造函数，但它与任何其他函数在语法上完全没有区别。`Person`是构造函数的线索在于名称——第一个字母大写。

定义构造函数后，你就可以开始创建实例，如下两个`Person`对象所示：

```javascript
var person1 = new Person();

var person2 = new Person();
```

当你没有参数要传递给构造函数时，甚至可以省略括号：

```javascript
var person1 = new Person;

var person2 = new Person;
```

即使`Person`构造函数没有显式返回任何内容，但`person1`和`person2`都被视为新`Person`类型的实例。`new`操作符会自动创建一个给定类型的对象并返回它。这意味着你可以使用`instanceof`运算符来推断对象的类型。以下代码显示了`instanceof`在新创建对象上的应用：

```javascript
console.log(person1 instanceof Person); // true

console.log(person2 instanceof Person); // true
```

由于`person1`和`person2`是用`Person`构造函数创建的，当`instanceof`检查这些对象是否为`Person`类型的实例时，返回`true`。

你还可以使用`constructor`属性检查实例的类型。每个对象实例都会自动创建一个`constructor`属性，该属性包含指向创建它的构造函数的引用。对于通用对象（通过对象字面量或`Object`构造函数创建的对象），`constructor`被设置为`Object`；对于用自定义构造函数创建的对象，`constructor`指向回那个构造函数。

例如，`Person`是`person1`和`person2`的`constructor`属性：

```javascript
console.log(person1.constructor === Person); // true

console.log(person2.constructor === Person); // true
```

`console.log`在两种情况下都输出`true`，因为两个对象都是用`Person`构造函数创建的。

尽管实例与其构造函数之间存在这种关系，但仍建议使用`instanceof`来检查实例的类型。这是因为`constructor`属性可以被覆盖，因此可能不完全准确。

当然，一个空的构造函数并没有太大用。构造函数的全部意义在于便于创建更多具有相同属性和方法的对象。要做到这一点，只需在构造函数内部添加任何你想要的属性即可，如下例所示：

```javascript
function Person(name) {
  this.name = name;

  this.sayName = function() {
    console.log(this.name);
  };
}
```

这个版本的`Person`构造函数接受一个命名的参数`name`，并将其赋值给`this`对象的`name`属性。构造函数还向对象添加了`sayName()`方法。`this`对象是在调用构造函数时由`new`自动创建的，它是构造函数类型的实例。（在这种情况下，它是`Person`的实例。）不需要从函数返回值，因为`new`操作符会产生返回值。

现在你可以使用`Person`构造函数来创建具有已初始化`name`属性的对象：

```javascript
var person1 = new Person("Nicholas");

var person2 = new Person("Greg");

console.log(person1.name); // "Nicholas"

console.log(person2.name); // "Greg"

person1.sayName(); // 输出 "Nicholas"

person2.sayName(); // 输出 "Greg"
```

每个对象都有自己的`name`属性，因此`sayName()`根据你使用它的对象返回不同的值。

**注意**：你也可以在构造函数内部调用`return`。如果返回的值是一个对象，则将返回该对象而不是新创建的对象。如果返回的值是原始类型，则使用新创建的对象，返回的值将被忽略。

构造函数允许你以一致的方式初始化一个类型的实例，在对象可以使用之前执行所有必要的属性设置。例如，你也可以在构造函数内部使用`Object.defineProperty()`来帮助初始化实例：

```javascript
function Person(name) {
  Object.defineProperty(this, "name", {
    get: function() {
      return name;
    },

    set: function(newName) {
      name = newName;
    },

    enumerable: true,

    configurable: true
  });

  this.sayName = function() {
    console.log(this.name);
  };
}
```

在这个版本的`Person`构造函数中，`name`属性是一个访问器属性，使用`name`参数来存储实际名称。这是可能的因为命名参数的作用类似于局部变量。

确保始终使用`new`调用构造函数；否则你可能会修改全局对象而不是新创建的对象。考虑以下代码中发生了什么：

```javascript
var person1 = Person("Nicholas"); // 注意：缺少 "new"

console.log(person1 instanceof Person); // false

console.log(typeof person1); // "undefined"

console.log(name); // "Nicholas"
```

当在没有`new`的情况下作为函数调用`Person`时，构造函数内部的`this`值等于全局`this`对象。变量`person1`不包含值，因为`Person`构造函数依赖`new`来提供返回值。没有`new`，`Person`只是一个没有返回语句的函数。对`this.name`的赋值实际上创建了一个全局变量，一个名为`name`的变量，用于存储传递给`Person`的名称。

第 6 章描述了解决此问题以及更复杂的对象组合模式的解决方案。

**注意**：在严格模式下，如果不使用`new`就调用`Person`构造函数，将会发生错误。这是因为严格模式不会将`this`赋值给全局对象。相反，`this`将保持为`undefined`，当你尝试在`undefined`上创建属性时，就会发生错误。

构造函数允许你配置具有相同属性的对象实例，但仅靠构造函数并消除代码冗余。在目前为止的代码中，每个实例都有自己的`sayName()`方法，尽管`sayName()`并没有改变。这意味着如果你有 100 个对象实例，就有 100 份执行完全相同函数的拷贝，只是数据不同。

如果所有实例都共享一个方法，然后该方法可以使用`this.name`来获取适当的数据，将会高效得多。这正是原型大显身场。

### 原型

你可以将原型想象成对象的配方。几乎每个函数（某些内置函数除外）都有一个原型属性，该属性在创建新实例时被使用。该原型被所有对象实例共享，这些实例可以访问原型的属性。例如，`hasOwnProperty()`方法定义在通用的`Object`原型上，但可以从任何对象中访问它，就像它是自身的属性一样，如下例所示：

```javascript
var book = {
  title: "The Principles of Object-Oriented JavaScript"
};

console.log("title" in book); // true

console.log(book.hasOwnProperty("title")); // true

console.log("hasOwnProperty" in book); // true

console.log(book.hasOwnProperty("hasOwnProperty")); // false

console.log(Object.prototype.hasOwnProperty("hasOwnProperty")); // true
```

尽管`book`上没有定义`hasOwnProperty()`，但仍然可以通过`book.hasOwnProperty()`访问该方法，因为该定义存在于`Object.prototype`上。记住，`in`运算符对于原型属性和自身属性都会返回`true`。

### `[[Prototype]]` 属性

实例通过一个名为`[[Prototype]]`的内部属性来跟踪其原型。该属性指向该实例正在使用的原型对象。当你使用`new`创建新对象时，构造函数的原型属性会被赋值给该新对象的`[[Prototype]]`属性。图 4-1 显示了`[[Prototype]]`属性如何让同一对象类型的多个实例引用同一个原型，从而减少代码重复。

| `Person.prototype` | `sayName`（function） |
| :--- | :--- |
| `person1 [[Prototype]]` | `name: "Nicholas"` |
| `person2 [[Prototype]]` | `name: "Greg"` |

*图 4-1：`person1`和`person2`的`[[Prototype]]`属性指向同一个原型。*

### 识别原型属性

你可以使用如下函数来确定属性是否在原型上：

```javascript
function hasPrototypeProperty(object, name) {
```



`return name in object && !object.hasOwnProperty(name);`

`}`

`console.log(hasPrototypeProperty(book, "title"));` // false

`console.log(hasPrototypeProperty(book, "hasOwnProperty"));` // true

如果属性存在对象中但 `hasOwnProperty()` 返回 `false`，那么该属性就在原型上。

## 构造函数与原型

你可以通过对对象使用 `Object.getPrototypeOf()` 方法来读取 `[[Prototype]]` 属性的值。例如，以下代码检查了一个通用空对象的原型：

```javascript
var object = {};
var prototype = Object.getPrototypeOf(object);
console.log(prototype === Object.prototype); // true
```

对于任何此类通用对象，`[[Prototype]]` 始终是指向 `Object.prototype` 的引用。

**注意**：某些 JavaScript 引擎还支持在所有对象上一个名为 `__proto__` 的属性。该属性允许你同时读取和写入 `[[Prototype]]` 属性。Firefox、Chrome 和 Node.js 都支持此，且 `__proto__` 是 ECMAScript 6 标准化的路径。

你还可以使用所有对象都包含的 `isPrototypeOf()` 方法测试一个对象是否是另一个对象的原型：

```javascript
var object = {};
console.log(Object.prototype.isPrototypeOf(object)); // true
```

由于 `object` 只是一个通用对象，它的原型应该是 `Object.prototype`，这意味着 `isPrototypeOf()` 应该返回 `true`。当在对象上读取属性时，JavaScript 引擎首先查找具有该名称的自身属性。如果引擎找到了命名正确的属性，它将返回该值。如果目标对象上不存在自身属性，JavaScript 将改为搜索原型。如果原型上存在该名称的原型属性，则返回该值。如果搜索结束未找到具有正确名称的属性，则返回 `undefined`。

考虑以下情况，其中对象在没有任何自身属性的情况下被创建：

```javascript
var object = {};
console.log(object.toString()); // "[object Object]"

object.toString = function() {
  return "[object Custom]";
};

console.log(object.toString()); // "[object Custom]"
```

```javascript
// 删除属性
delete object.toString;
console.log(object.toString()); // "[object Object]"

// 无影响 - delete 仅作用于自身属性
```

在这个示例中，`toString()` 方法来自原型并默认返回 `"[object Object]"`。如果你接着定义了一个名为 `toString()` 的自身属性，那么每当再次在对象上调用 `toString()` 时，都会使用该自身属性。该自身属性遮蔽了原型属性，因此同名的原型属性将不再被使用。如果从对象上删除了自身属性，原型属性将再次被使用。（请记住，你不能从实例中删除原型属性，因为 `delete` 运算符只作用于自身属性。）

图 4-2 显示了此示例中发生的情况。该示例还强调了一个重要的概念：你不能从实例向原型属性赋值。正如你在图 4-2 的中间部分看到的，为 `toString` 赋值会在实例上创建一个新的自身属性，而让原型上的属性保持不变。

| Object.prototype.toString (function) | object [[Prototype]] |
| :--- | :--- |
| Object.prototype.toString (function) | object [[Prototype]] |
| Object.prototype.toString (function) | object [[Prototype]] |

```javascript
var object = {};
object.toString = function() {
  return "[object Custom]";
};
delete object.toString;
```

图 4-2：一个没有自身属性的对象（顶部）仅拥有其原型的所有方法。在对象上添加 `toString()` 属性（中间）会替换原型属性，直到你删除它（底部）。

## 构造函数与原型

### 在构造函数构造原型

原型的共享特性使其非常适合为给定类型的所有对象定义一次方法。因为方法往往对所有实例执行相同的操作，所以没有理由每个实例都需要自己的一组方法。

将方法放在原型上并然后使用 `this` 来访问当前实例要高效得多。例如，考虑以下 `Person` 构造函数：

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.sayName = function() {
  console.log(this.name);
};

var person1 = new Person("Nicholas");
var person2 = new Person("Greg");

console.log(person1.name); // "Nicholas"
console.log(person2.name); // "Greg"

person1.sayName(); // 输出 "Nicholas"
person2.sayName(); // 输出 "Greg"
```

在这个版本的 `Person` 构造函数中，`sayName()` 定义在原型上而不是构造函数中。对象实例的工作方式与本章早期的示例完全相同，尽管 `sayName()` 现在是原型属性而不是自身属性。由于 `person1` 和 `person2` 分别是调用 `sayName()` 的基础引用，`this` 值分别被赋值给 `person1` 和 `person2`。

你还可以在原型上存储其他类型的数据，但在使用引用值时要小心。因为这些值在实例间共享，你可能意料不到一个实例能够更改另一个实例将访问的值。这个示例展示了当你不关注引用值指向何时会发生什么：

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.sayName = function() {
  console.log(this.name);
};
```

## 第 4 章

```javascript
Person.prototype.favorites = [];

var person1 = new Person("Nicholas");
var person2 = new Person("Greg");

person1.favorites.push("pizza");
person2.favorites.push("quinoa");

console.log(person1.favorites); // "pizza,quinoa"
console.log(person2.favorites); // "pizza,quinoa"
```

`favorites` 属性定义在原型上，这意味着 `person1.favorites` 和 `person2.favorites` 指向同一个数组。你添加到任何一个人的 `favorites` 中的任何值都将成为该原型上该数组的元素。这可能不是你实际想要的行为，因此在原型上定义内容时，需要非常小心。

尽管你可以逐个向原型上添加属性，但许多开发人员使用一种更简洁的模式，即用对象字面量替换原型：

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype = {
  sayName: function() {
    console.log(this.name);
  },
  toString: function() {
    return "[Person " + this.name + "]";
  }
};
```

这段代码在原型上定义了两个方法：`sayName()` 和 `toString()`。这种模式变得非常流行，因为它消除了多次输入 `Person.prototype` 的需要。然而有一个需要注意的副作用：

```javascript
var person1 = new Person("Nicholas");

console.log(person1 instanceof Person); // true
console.log(person1.constructor === Person); // false
console.log(person1.constructor === Object); // true
```

### 构造函数与原型

使用对象字面量符号覆盖原型改变了 `constructor` 属性，使其现在指向 `Object` 而不是 `Person`。这种发生是因为 `constructor` 属性存在于原型上，而不是对象实例上。当创建一个函数时，它的 `prototype` 属性会被创建，并且其 `constructor` 属性等于该函数。这种模式完全覆盖了原型对象，这意味着 `constructor` 将来自赋值给 `Person.prototype` 的新创建（通用）对象。为了避免这种情况，在覆盖原型时将 `constructor` 恢复为正确的值：

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype = {
  constructor: Person,
  sayName: function() {
    console.log(this.name);
  },
  toString: function() {
    return "[Person " + this.name + "]";
  }
};

var person1 = new Person("Nicholas");
var person2 = new Person("Greg");

console.log(person1 instanceof Person); // true
console.log(person1.constructor === Person); // true
console.log(person1.constructor === Object); // false
console.log(person2 instanceof Person); // true
console.log(person2.constructor === Person); // true
console.log(person2.constructor === Object); // false
```

在这个示例中，`constructor` 属性被专门地分配在原型上。将此作为原型上的第一个属性是一个好习惯，这样你就不会忘记包含它。

构造函数、原型和实例之间关系中最有趣的一个方面是，实例与构造函数之间没有直接的链接。然而，实例与原型之间、原型与构造函数之间存在直接链接。图 4-3 阐了这种关系。

图 4-3：实例和它的构造函数通过原型链接。

| Person prototype | Person.prototype constructor |
| :--- | :--- |
| sayName (function) | |
| toString (function) | |
| person1 [[Prototype]] | "Nicholas" |
| person2 [[Prototype]] | "Greg" |
| name | |

### 改变原型

由于特定类型的所有实例都引用一个共享的原型，你可以随时同时增强所有这些对象。记住，`[[Prototype]]` 属性仅包含指向原型的指针，对原型的任何更改都会立即在引用它的任何实例上生效。这意味着你可以在任何时候向原型添加新成员，并让这些更改反映在现有实例上，如示例所示：

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype = {
  constructor: Person,
  sayName: function() {
    console.log(this.name);
  },
  toString: function() {
    return "[Person " + this.name + "]";
  }
};
```

```javascript
var person1 = new Person("Nicholas");
var person2 = new Person("Greg");

console.log("sayHi" in person1); // false
console.log("sayHi" in person2); // false

// 添加一个新方法
Person.prototype.sayHi = function() {
  console.log("Hi");
};

person1.sayHi(); // 输出 "Hi"
person2.sayHi(); // 输出 "Hi"
```

在这段代码中，`Person` 类型最初只有两个方法：`sayName()` 和 `toString()`。创建了两个 `Person` 实例，然后向原型添加了 `sayHi()` 方法。从那时起，两个实例都可以访问 `sayHi()`。每次访问该属性时都会发生命名属性的搜索，因此这种体验是无缝的。

随时修改原型的能力对于密封（sealed）和冻结（frozen）对象有一些有趣的影响。当你对对象使用 `Object.seal()` 或 `Object.freeze()` 时，你是在对象实例上操作，对原型的任何更改都会在引用它的任何实例上立即可用。这意味着你可以字面上在任何一点向原型添加新成员，并让这些更改反映在现有实例上，如下所示：

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype = {
  constructor: Person,
  sayName: function() {
    console.log(this.name);
  },
  toString: function() {
    return "[Person " + this.name + "]";
  }
};
```

```javascript
var person1 = new Person("Nicholas");
var person2 = new Person("Greg");

Object.freeze(person1);

Person.prototype.sayHi = function() {
  console.log("Hi");
};

person1.sayHi(); // 输出 "Hi"
person2.sayHi(); // 输出 "Hi"
```

在这个示例中，有两个 `Person` 实例。第一个 (`person1`) 是被冻结的，而第二个 (`person2`) 是普通对象。当你向原型添加 `sayHi()` 时，两者都获得了新方法，这似乎矛盾了 `person1` 的冻结状态。`[[Prototype]]` 属性被认为是实例自身的属性，而该值本身并没有冻结。

**注意：** 在 JavaScript 开发中，你可能不会经常这样使用原型。然而，理解对象与其原型之间存在的关系是非常重要的，像这样的例子有助于理解这些概念。

### 内置对象原型

到此时，你可能会想原型是否允许你修改 JavaScript 引擎中自带的内置对象。答案是肯定的。所有内置对象都有构造函数，因此它们拥有你可以修改的原型。例如，为所有数组添加一个新方法只需修改 `Array.prototype` 即可：

```javascript
Array.prototype.sum = function() {
  return this.reduce(function(previous, current) {
    return previous + current;
  });
};

var numbers = [1, 2, 3, 4, 5, 6];
var result = numbers.sum();
console.log(result); // 21
```

这个示例在 `Array.prototype` 上创建了一个 `sum()` 方法，它可以简单的累加数组中的所有项并返回结果。`numbers` 数组通过原型自动访问该方法。在 `sum()` 内部，`this` 指向 `numbers`，它是 `Array` 的实例，因此该方法可以自由使用其他数组方法，如 `reduce()`。

你可能记得字符串、数字和布尔值都有内置的原始包装类型，用于像访问对象一样访问原始值。如果你像示例中那样修改原始包装类型的原型，你实际上可以为这些原始值添加更多功能。



```javascript
String.prototype.capitalize = function() {
  return this.charAt(0).toUpperCase() + this.substring(1);
};

var message = "hello world!";
console.log(message.capitalize()); // "Hello world!"
```

这段代码为字符串创建了一个名为 `capitalize()` 的新方法。`String` 类型是字符串的原始包装器，修改其原型意味着所有字符串都会获得这些更改。

构造函数与原型 **63**

> **注意**：虽然通过修改内置对象来实验功能可能很有趣，但在生产环境中这样做并不是一个好主意。开发者期望内置对象以特定的方式运行并具有某些方法。故意更改内置对象会违反这些预期，并让其他开发者不确定这些对象应该是如何工作的。

**总结**

构造函数只是通过 `new` 算符调用的普通函数。每当你想要创建多个具有相同属性的对象时，你都可以随时定义自己的构造函数。你可以使用 `instanceof` 或直接访问它们的 `constructor` 属性来识别由构造函数创建的对象。

每个函数都有一个 `prototype` 属性，它定义了由特定构造函数创建的对象共享的所有属性。共享方法和原始值属性通常定义在原型上，而所有其他属性都定义在构造函数内部。`constructor` 属性实际上定义在原型上，因为它在对象实例之间是共享的。

对象的原型存储在内部的 `[[Prototype]]` 属性中。该属性是一个引用，而不是拷贝。如果你在任何时间点更改了原型，这些更改将作用于所有实例，这是因为 JavaScript 查找属性的方式。当你尝试访问对象上的属性时，系统会在该对象中搜索具有你指定的名称的自有属性。如果未找到自有属性，则搜索原型。这种搜索机制意味着原型可以持续变化，而引用该原型的对象实例将立即反映这些更改。

内置对象也有可以修改的原型。虽然不建议在生产环境中这样做，但它对于新功能的实验和概念证明很有帮助。

**5**

## 继承

学习如何创建对象是理解面向对象编程的第一步。第二步是理解继承。在传统的面向对象语言中，类从其他类继承属性。

但在 JavaScript 中，继承可以发生在对象之间，而无需类结构来定义这种关系。这种继承的机制是你已经熟悉的：原型。

### 原型链与 Object.prototype

JavaScript 内置的继承方法称为*原型链*或*原型型继承*。正如你在第 4 章中学到的，`prototype` 属性在对象实例上自动可用，这是继承的一种形式。对象实例从原型继承属性。

由于原型本身也是一个对象，它有自己的原型并从该原型继承属性。这就是*原型链*：一个对象从它的原型继承，而该原型反过来又从它的原型继承，依此类推。

所有对象（包括你自己定义的对象）除非另有指定，否则都会从 `Object` 继承（在本章后面会讨论）。具体来说，所有对象都从 `Object.prototype` 继承。通过对象字面量定义的任何对象的 `[[Prototype]]` 都被设置为 `Object.prototype`，这意味着它们从 `Object.prototype` 继承属性，就像示例中的 `book` 对象：

```javascript
var book = {
  title: "The Principles of Object-Oriented JavaScript"
};
var prototype = Object.getPrototypeOf(book);
console.log(prototype === Object.prototype); // true
```

在这里，`book` 的原型等于 `Object.prototype`。不需要额外的代码来实现这一点，因为这是创建新对象时的默认行为。这种关系意味着 `book` 自动接收来自 `Object.prototype` 的方法。

### 从 Object.prototype 继承的方法

在过去几个章节中使用的几个方法实际上定义在 `Object.prototype` 上，因此被对象继承。这些方法是：

- `hasOwnProperty()`：确定是否存在具有给定名称的自有属性
- `propertyEnumerable()`：确定自有属性是否可枚举
- `isPrototypeOf()`：确定该对象是否是另一个对象的原型
- `valueOf()`：返回对象的数值表示
- `toString()`：返回对象的字符串表示

这五个方法通过继承出现在所有对象上。当你需要让对象在 JavaScript 中一致工作时，最后两个方法非常重要，有时你可能想自己定义它们。

**valueOf()**

当在对象上使用算符时，就会调用 `valueOf()` 方法。默认情况下，`valueOf()` 仅返回对象实例。原始包装类型覆盖了 `valueOf()`，以便为 `String` 返回字符串，为 `Boolean` 返回布尔，为 `Number` 返回数字。同样，`Date` 的 `valueOf()` 方法返回毫秒数（就像 `Date.prototype.getTime()` 一样）。这使得你能够编写比较日期的代码，例如：

```javascript
var now = new Date();
var earlier = new Date(2010, 1, 1);
console.log(now > earlier); // true
```

在示例中，`now` 是代表当前时间的 `Date` 对象，而 `earlier` 是过去的一个固定日期。当使用大于算符 (`>`) 时，在执行比较之前，会在两个对象上调用 `valueOf()` 方法。由于 `valueOf()`，你甚至可以从一个日期减去另一个日期并得到时间差。如果你的对象打算用于算符，你始终可以定义自己的 `valueOf()` 方法。如果你定义了 `valueOf()` 方法，请记住你并没有改变算符的工作方式，只是改变了与算符默认行为一起使用的值。

**toString()**

每当 `valueOf()` 返回引用值而不是原始值时，就会作为备选调用 `toString()` 方法。每当 JavaScript 期望字符串时，它也会在原始值上被隐式调用。例如，当字符串用作 `+` 算符的一个操作数时，另一个操作数会被自动转换为字符串。如果另一个操作数是原始值，它会被转换为字符串表示（例如，`true` 变成 `"true"`），但如果它是引用值，则会调用 `valueOf()`。如果 `valueOf()` 返回引用值，则会调用 `toString()` 并使用返回的值。例如：

```javascript
var book = {
  title: "The Principles of Object-Oriented JavaScript"
};
var message = "Book = " + book;
console.log(message); // "Book = [object Object]"
```

这段代码通过组合 `"Book = "` 和 `book` 来构造字符串。由于 `book` 是一个对象，会调用它的 `toString()` 方法。该方法继承自 `Object.prototype`，在大多数 JavaScript 引擎中返回默认值`"[object Object]"`。如果你对该值满意，就不需要更改对象的 `toString()` 方法。然而，定义自己的 `toString()` 方法是有用的，以便字符串转换返回更多信息。例如，假设你想让脚本记录书籍标题：

```javascript
var book = {
  title: "The Principles of Object-Oriented JavaScript",
  toString: function() {
    return "[Book " + this.title + "]";
  }
};
var message = "Book = " + book;
// "Book = [Book The Principles of Object-Oriented JavaScript]"
console.log(message);
```

这段代码为 `book` 定义了自定义的 `toString()` 方法，返回比继承版本更有价值。你通常不需要担心自定义 `toString()` 方法，但在需要时知道可以这样做是好的。

**修改 Object.prototype**

所有对象默认都从 `Object.prototype` 继承，因此对 `Object.prototype` 的更改会影响所有对象。这是一个非常危险的情况。你在第 4 章中被建议不要修改内置对象的原型，而这个建议对于 `Object.prototype` 来说要加倍。看看会发生什么：

```javascript
Object.prototype.add = function(value) {
  return this + value;
};

var book = {
  title: "The Principles of Object-Oriented JavaScript"
};

console.log(book.add(5)); // "[object Object]5"

console.log("title".add("end")); // "titleend"

// 在网络浏览器中
console.log(document.add(true)); // "[object HTMLDocument]true"
console.log(window.add(5)); // "[object Window]true"
```

继承 **69**

添加 `Object.prototype.add()` 会导致所有对象都拥有 `add()` 方法，无论这在逻辑上是否有意义。这个问题不仅是开发者面临的难题，也是 JavaScript 语言委员会需要解决的问题：他们不得不将新方法放在不同的位置，因为在 `Object.prototype` 上添加方法可能会产生不可预见的后果。

该问题的另一个方面涉及在向 `Object.prototype` 上添加可枚举属性。在之前的例子中，`Object.prototype.add()` 是一个可枚举属性，这意味着当你使用 `for-in` 循环时它会显示出来，例如：

```javascript
var empty = {};

for (var property in empty) {
  console.log(property);
}
```

在这里，一个空对象仍然会输出 `"add"` 作为属性，因为它存在于原型上并且是可枚举的。鉴于 JavaScript 中 `for-in` 结构的使用频率很高，使用可枚举属性修改 `Object.prototype` 可能会影响大量代码。出于这个原因，Douglas Crockford 建议在 `for-in` 循环中始终使用 `hasOwnProperty()`，(*)，例如：

```javascript
var empty = {};

for (var property in empty) {
  if (empty.hasOwnProperty(property)) {
    console.log(property);
  }
}
```

虽然这种方法可以防止可能不需要的原型属性，但它也限制了 `for-in` 仅用于自身的属性，这可能是你想要的，也可能不是。为了获得最大的灵活性，最好的办法是不修改 `Object.prototype`。

## 对象继承

最简单的继承类型是对象之间的继承。你所做的只需指定哪个对象应该是新对象的 `[[Prototype]]`。对象字面量隐式地将 `Object.prototype` 设置为它们的 `[[Prototype]]`，但你也可以通过 `Object.create()` 方法显式地指定 `[[Prototype]]`。

* 查看 Douglas Crockford 的《JavaScript 编程语言代码规范》（*http://javascript.crockford.com/code.html*）。

第5 章

70

`Object.create()` 方法接受两个参数。第一个参数是用于新对象 `[[Prototype]]` 的对象。可选的第二个参数是一个属性描述符对象，其格式与 `Object.defineProperties()` 使用的格式相同（见第 3 章）。考虑以下内容：

```javascript
var book = {
  title: "The Principles of Object-Oriented JavaScript"
};

// 等同于
var book = Object.create(Object.prototype, {
  title: {
    configurable: true,
    enumerable: true,
    value: "The Principles of Object-Oriented JavaScript",
    writable: true
  }
});
```

这段代码中的两个声明实际上是等价的。第一个声明使用对象字面量定义了一个具有名为 `title` 单个属性的对象。该对象自动继承自 `Object.prototype`，并且该属性被设置为可配置、可枚举和可写。第二个声明采取了相同的步骤，但它是使用 `Object.create()` 显式完成的。每个声明生成的 `book` 对象行为完全相同。但你可能永远不会编写直接继承自 `Object.prototype` 的代码，因为这是默认拥有的。继承自其他对象要有趣得多：

```javascript
var person1 = {
  name: "Nicholas",
  sayName: function() {
    console.log(this.name);
  }
};

var person2 = Object.create(person1, {
  name: {
    configurable: true,
    enumerable: true,
    value: "Greg",
    writable: true
  }
});

person1.sayName(); // 输出 "Nicholas"
person2.sayName(); // 输出 "Greg"
```

继承 **71**

```javascript
console.log(person1.hasOwnProperty("sayName")); // true
console.log(person1.isPrototypeOf(person2)); // true
console.log(person2.hasOwnProperty("sayName")); // false
```

这段代码创建了一个对象 `person1`，包含一个 `name` 属性和一个 `sayName()` 方法。`person2` 对象继承自 `person1`，因此它继承了 `name` 和 `sayName()`。然而，`person2` 是通过 `Object.create()` 定义的，这也为 `person2` 定义了自身的 `name` 属性。这个属性遮蔽了同名的原型属性并被其取代。因此，`person1.sayName()` 输出 `"Nicholas"`，而 `person2.sayName()` 输出 `"Greg"`。请记住 `sayName()` 仍然存在于 `person1` 上，并被 `person2` 继承。

在这个例子中，`person2` 的继承链比 `person1` 更长。`person2` 对象继承自 `person1` 对象，而 `person1` 对象继承自 `Object.prototype`。见图 5-1。

| Object.prototype | [[Prototype]] | person2 |
| :--- | :--- | :--- |
| | [[Prototype]] | "Greg" |
| person1 | [[Prototype]] | |
| name "Nicholas" | | |
| sayName (function) | | |
| propertyisEnumerable (function) | | |
| hasOwnProperty (function) | | |
| isPrototypeOf (function) | | |
| toString (function) | | |
| valueOf (function) | | |

*图 5-1：`person2` 的原型链包含了 `person1` 和 `Object.prototype`。*

当访问对象上的某个属性时，JavaScript 引擎会经历一个搜索过程。如果在实例上找到了该属性（即它是一个自身的属性），则使用该属性值。如果未在实例上找到属性，搜索将在 `[[Prototype]]` 上继续。如果仍然未找到属性，搜索将继续到该对象的 `[[Prototype]]`，依此类推，直到到达链的末端。该链通常以 `Object.prototype` 结束，其 `[[Prototype]]` 被设置为 `null`。

第5 章

72

你也可以通过 `Object.create()` 创建原型为 `null` 的对象，例如：

```javascript
var nakedObject = Object.create(null);
console.log("toString" in nakedObject); // false
console.log("valueOf" in nakedObject); // false
```

此示例中的 `nakedObject` 是一个没有原型链的对象。这意味着像 `toString()` 和 `valueOf()` 等内置方法在该对象上不存在。实际上，这个对象是一个完全空白的面板，没有任何预定义的属性，使其非常适合创建不会与继承名称产生潜在冲突的查找哈希。这种对象没有许多其他用途，你不能像继承自 `Object.prototype` 那样使用它。



## 构造函数继承

JavaScript 中的对象继承也是继承的基础。回想第 4 章，几乎每个函数都有一个可以修改或替换的 `prototype` 属性。该 `prototype` 属性被自动赋值为一个继承自 `Object.prototype` 的通用对象，并具有单个 `constructor` 属性。实际上，当你编写以下代码时，JavaScript 引擎为你执行以下操作：

```javascript
function YourConstructor() {
}

YourConstructor.prototype = Object.create(Object.prototype, {
  constructor: {
    configurable: true,
    enumerable: true,
    value: YourConstructor,
    writable: true
  }
});
```

因此，在不进行额外操作的情况下，这段代码将 `YourConstructor` 的 `prototype` 属性设置为继承自 `Object` 的对象，这意味着 `YourConstructor` 的任何实例也继承自 `Object`。`YourConstructor` 是 `Object` 的*子类型*，而 `Object` 是 `YourConstructor` 的*超类型*。

继承 **73**

由于 `prototype` 属性是可写的，你可以通过覆盖它来改变链。考虑以下示例：

```javascript
function Rectangle(length, width) {
  this.length = length;
  this.width = width;
}

Rectangle.prototype.getArea = function() {
  return this.length * this.width;
};

Rectangle.prototype.toString = function() {
  return "Rectangle " + this.length + "x" + this.width;
};

function Square(size) {
  this.size = size;
}

Square.prototype = Rectangle();

var rect = new Rectangle(5, 10);
var square = new Square(6);

console.log(rect.getArea()); // 50
console.log(square.getArea()); // 36
console.log(rect.toString()); // "Rectangle 5x10"
console.log(square.toString()); // "Square 6x6"

console.log(rect instanceof Rectangle); // true
console.log(rect instanceof Object); // true
console.log(square instanceof Square); // true
console.log(square instanceof Rectangle); // true
console.log(square instanceof Object); // true
```

# 第5章 74节

参数未提供（许多构造函数包含初始化逻辑，这些逻辑可能需要这些参数），并且构造函数没有修改任何全局状态，例如跟踪创建了多少实例。在原始值被覆盖后，`Square.prototype` 上的构造函数属性会被恢复。

之后，`rect` 被创建为 `Rectangle` 的实例，`square` 被创建为 `Square` 的实例。这两个对象都拥有 `getArea()` 方法，因为它们继承自 `Rectangle.prototype`。`square` 变量既被认为是 `Square` 的实例，也被认为是 `Rectangle` 的实例和 `Object` 的实例，因为 `instanceof` 使用原型链来确定对象的类型。见图 5-2。

| | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `Rectangle.prototype` | `[[Prototype]]` | (function) | | | |
| `getArea` | `toString` | (function) | | | |
| `Object.prototype` | `[[Prototype]]` | | | | |
| `square` | `[[Prototype]]` | | | | |
| `Square.prototype` | `[[Prototype]]` | 6 | | | |
| `length` | `propertyisEnumerable` | (function) | | | |
| `hasOwnProperty` | (function) | null | | | |
| `isPrototypeOf` | (function) | | | | |
| `toString` | (function) | | | | |
| `valueOf` | (function) | | | | |
| `width` | 6 | | | | |
| `rect` | `[[Prototype]]` | 5 | | | |

尽管实际上，`Square.prototype` 并不需要用 `Rectangle` 对象覆盖；因为 `Rectangle` 构造函数没有执行任何 `Square` 所需的操作。事实上，唯一相关的部分是 `Square.prototype` 需要某种方式链接到 `Rectangle.prototype` 以实现继承。这意味着你可以再次使用 `Object.create()` 来简化这个示例。

*图 5-2：**square** 和 **rect** 的原型链显示它们都继承自 **Rectangle.prototype** 和 **Object.prototype**，但只有 **square** 继承自 **Square.prototype**。*

## 继承 75节

```javascript
// 继承自 Rectangle
function Square(size) {
  this.length = size;
  this.width = size;
}

Square.prototype = Object.create(Rectangle.prototype, {
  constructor: {
    configurable: true,
    enumerable: true,
    value: Square,
    writable: true
  }
});

Square.prototype.toString = function() {
  return "[Square " + this.length + "x" + this.width + "]";
};
```

在这个版本的代码中，`Square.prototype` 被一个继承自 `Rectangle.prototype` 的新对象覆盖，并且 `Rectangle` 构造函数从未被调用。这意味着你不再需要担心在不传递参数的情况下调用构造函数会导致错误。否则，这段代码的行为与之前的代码完全相同。原型链保持完整，因此 `Square` 的所有实例都继承自 `Rectangle.prototype`，并且构造函数在同一个步骤中恢复。

**注意** *始终确保在向原型添加属性**之前**覆盖它，*否则在发生覆盖时你将丢失已添加的方法。*

### 构造函数窃取 (Constructor Stealing)

由于 JavaScript 中的继承是通过原型链完成的，因此你不需要调用对象的父类型构造函数。如果你确实想从子类型构造函数调用父类型构造函数，你需要利用 JavaScript 函数的工作方式。在第 2 章中，你学习了 `call()` 和 `apply()` 方法，它们允许使用不同的 `this` 值调用函数。这正是*构造函数窃取*的工作原理。你只需要在子类型构造函数中使用 `call()` 或 `apply()` 调用父类型构造函数，并传入新创建的对象。从效果上，你是在为自己的对象“窃取”了父类型构造函数，就像这个示例所示：

```javascript
function Rectangle(length, width) {
  this.length = length;
  this.width = width;
}
```

## 第5章 76节

```javascript
Rectangle.prototype.getArea = function() {
  return this.length * this.width;
};

Rectangle.prototype.toString = function() {
  return "[Rectangle " + this.length + "x" + this.width + "]";
};

// 继承自 Rectangle
function Square(size) {
  Rectangle.call(this, size, size);
  // 可选：在此处添加新属性或覆盖现有属性
}

Square.prototype = Object.create(Rectangle.prototype, {
  constructor: {
    configurable: true,
    enumerable: true,
    value: Square,
    writable: true
  }
});

Square.prototype.toString = function() {
  return "[Square " + this.length + "x" + this.width + "]";
};

var square = new Square(6);
console.log(square.length); // 6
console.log(square.width); // 6
console.log(square.getArea()); // 36
```

`Square` 构造函数调用了 `Rectangle` 构造函数，并传入了 `this` 以及两次 `size`（一次用于长度，一次用于宽度）。这样做在新对象上创建了 `length` 和 `width` 属性，并使它们等于 `size`。这是避免从想要继承的构造函数中重新定义属性的方法。在应用父类型构造函数之后，你可以添加新属性或覆盖现有属性。

当你需要在自定义类型之间完成继承非常有用。你总是需要修改构造函数的原型，并且可能需要在子类型构造函数内部调用父类型构造函数。通常，你会修改原型来实现方法的继承，并使用构造函数窃取来处理属性。这种方法通常被称为*伪类继承 (pseudoclassical inheritance)*，因为它模拟了基于类的语言的经典继承。

## 继承 77节

### 访问父类型方法

在上在上示例中，`Square` 类型有它自己的 `toString()` 方法，覆盖了原型上的 `toString()`。在子类型中用新功能覆盖父类型方法是相当常见的，但如果你仍然想访问父类型方法怎么办？在其他语言中，你可能可以说 `super.toString()`，但 JavaScript 没有类似的机制。相反，你可以直接访问父类型原型上的方法，并使用 `call()` 或 `apply()` 在子类型对象上执行该方法。例如：

```javascript
function Rectangle(length, width) {
  this.length = length;
  this.width = width;
}

Rectangle.prototype.getArea = function() {
  return this.length * this.width;
};

Rectangle.prototype.toString = function() {
  return "[Rectangle " + this.length + "x" + this.width + "]";
};

// 继承自 Rectangle
function Square(size) {
  Rectangle.call(this, size, size);
}

Square.prototype = Object.create(Rectangle.prototype, {
  constructor: {
    configurable: true,
    enumerable: true,
    value: Square,
    writable: true
  }
});

Square.prototype.toString = function() {
  var text = Rectangle.prototype.toString.call(this);
  return text.replace("Rectangle", "Square");
};
```

在这个版本的代码中，`Square.prototype.toString()` 使用 `call()` 调用了 `Rectangle.prototype.toString()`。它只需要将 "Rectangle" 替换为 "Square"。这种方法对于此类操作似乎有些繁琐，但它是访问父类型方法的唯一方法。

## 第5章 78节

### 总结

JavaScript 通过原型链支持继承。当一个对象的 `[[Prototype]]` 设置等于另一个对象时，对象之间就会创建原型链。所有通用对象都继承自 `Object.prototype`。如果你想创建一个继承自其他对象，可以使用 `Object.create()` 为新对象指定 `[[Prototype]]` 的值。

通过在构造函数上创建原型链来实现自定义类型之间的继承。通过将构造函数的原型设置为另一个值，可以在自定义类型的实例与其他值的原型之间创建继承。该构造的所有实例共享同一个原型，因此它们都从同一个对象。这种技术对于从其他对象继承方法非常有效，但无法通过原型继承自有属性。

为了正确继承自有属性，你可以使用构造函数窃取，这只是使用 `call()` 或 `apply()` 调用构造函数，以便任何初始化操作都在子类型对象上完成。结合构造函数窃取和原型链是 JavaScript 中实现自定义类型之间继承的最常用方法。

# 6 对象模式

JavaScript 有许多创建对象的模式，通常完成同一项任务有不止一种方法。你可以根据需要随时定义自己的自定义类型或泛型对象。你可以使用继承在对象之间共享行为，也可以使用其他技术，如混入（mixins）。你还可以利用高级 JavaScript 特性来防止对象的结构被修改。本章讨论的模式为你提供了管理和创建对象的强大方法，而这些方法都基于你的具体用例。

## 第 6 章：私有成员和特权成员

JavaScript 中的所有对象属性都是公开的，没有显式的方法来指示某个属性不应从特定对象的外部访问。然而，在某些情况下，你可能希望数据不是公开的。例如，当一个对象使用某个值来确定某种状态时，在对象不知情的情况下修改该数据将导致状态管理过程陷入混乱。避免这种情况的一种方法是使用命名规范。例如，当属性不打算公开时，在属性名前面加上下划线前缀（例如 `this._name`）是非常常见的。但是，也有不依赖于规范的隐藏数据方法，因此在防止修改私有信息方面更加“无防弹”。

### 模块模式

*模块模式*（module pattern）是一种对象创建模式，旨在创建具有私有数据的单例对象。基本方法是使用一个返回对象的*立即调用函数表达式（IIFE）*。IIFE 是一个被定义后立即调用以产生结果的函数表达式。该函数表达式可以包含任意数量的局部变量，这些变量无法从函数外部访问。由于返回的对象定义在那个函数内部，因此对象的方法可以访问这些数据。（所有在 IIFE 内定义的对象都可以访问相同的局部变量。）通过这种方式访问私有数据的方法被称为*特权*（privileged）方法。这里是模块模式的基本格式：

```javascript
var yourObject = (function() {
  // 私有数据变量
  return {
    // 公共方法和属性
  };
}());
```

在模式模式中，匿名函数被创建并立即执行。（注意函数末尾额外的的括号。你可以使用这种语法立即执行匿名函数。）这意味着该函数只存在片刻，执行后就会被销毁。IIFE 是 JavaScript 中一种非常流行的模式，部分原因是由于它们在模块模式中的应用。

模块模式允许你将普通变量作为实际上不公开的对象属性。你通过创建作为对象方法的*闭包*（closure）函数来实现这一点。闭包简单来说就是访问自身作用域之外数据的函数。例如，每你在函数中访问全局对象（如浏览器中的 `window`）时，该函数都会访问其作用域之外的变量。与模块函数的区别在于，变量是在 IIFE 内部声明的，同样在 IIFE 内部声明的函数访问了这些变量。例如：

```javascript
var person = (function() {
  var age = 25;
  return {
    name: "Nicholas",
    getAge: function() {
      return age;
    },
    growOlder: function() {
      age++;
    }
  };
}());

console.log(person.name); // "Nicholas"
console.log(person.getAge()); // 25
person.age = 100;
console.log(person.getAge()); // 25
person.growOlder();
console.log(person.getAge()); // 26
```



这段代码使用模块模式创建了`person`对象。`age`变量充当了对象的私有属性。它无法从对象外部直接访问，但可以被对象方法使用。对象上有两个特权方法：`getAge()`，用于读取`age`变量的值；以及`growOlder()`，用于增加`age`。这两个方法都可以直接访问变量`age`，因为该变量定义在它们所在的外部函数中。

模块模式有一种变体，称为揭示模块模式（revealing module pattern），它将所有变量和方法安排在 IIFE 顶部，并简单地将它们赋值给返回的对象。你可以如下使用揭示模块模式编写之前的示例：

```javascript
var person = (function() {
  var age = 25;
  function getAge() {
    return age;
  }
  function growOlder() {
    age++;
  }
  return {
    name: "Nicholas",
    getAge: getAge,
    growOlder: growOlder
  };
}());
```

在揭示模块模式中，`age`、`getAge()`和`growOlder()`都被定义为 IIFE 的局部变量。然后将`getAge()`和`growOlder()`函数赋值给返回的对象，实际上在 IIFE 之外将它们“揭示”出来。这段代码本质上与早期使用传统模块模式的示例相同；然而，有些人更偏于这种模式，因为它将所有变量和函数声明放在一起。

### 构造函数的私有成员

模块模式对于定义具有私有属性的单个对象非常棒，但对于那些也需要自己的私有属性的自定义类型呢？你可以在构造函数内部使用类似于模块模式的模式来创建特定实例私有数据。例如：

```javascript
function Person(name) {
  // 定义一个仅在 Person 构造函数内部访问的变量
  var age = 25;
  this.name = name;
  this.getAge = function() {
    return age;
  };
  this.growOlder = function() {
    age++;
  };
}

var person = new Person("Nicholas");
console.log(person.name); // "Nicholas"
console.log(person.getAge()); // 25
person.age = 100;
console.log(person.getAge()); // 25
person.growOlder();
console.log(person.getAge()); // 26
```

在这段代码中，`age`变量充当了对象的私有属性。它无法从对象外部直接访问，但可以被对象方法使用。对象上有两个特权方法：`getAge()`，用于读取`age`变量的值；以及`growOlder()`，用于增加`age`。这两个方法都可以直接访问变量`age`，因为它定义在它们所在的外部函数中。

```javascript
var Person = (function() {
  //所有人共享 age
  var age = 25;
  function InnerPerson(name) {
    this.name = name;
  }
  InnerPerson.prototype.getAge = function() {
    return age;
  };
  InnerPerson.prototype.growOlder = function() {
    age++;
  };
  return InnerPerson;
}());

var person1 = new Person("Nicholas");
var person2 = new Person("Greg");
console.log(person1.name); // "Nicholas"
console.log(person1.getAge()); // 25
console.log(person2.name); // "Greg"
console.log(person2.getAge()); // 25
person1.growOlder();
console.log(person1.getAge()); // 26
console.log(person2.getAge()); // 26
```

在这段代码中，`InnerPerson`构造函数定义在 IIFE 内部。变量`age`定义在构造函数之外，但被两个原型方法使用。所有`Person`实例最终共享`age`变量，因此修改一个实例的值会自动影响另一个。

### 混入（Mixins）

尽管 JavaScript 中经常使用伪类继承和原型继承，但还有一种类型通过混入实现的伪继承。混入发生在一个对象在不修改原型链的情况下获取另一个对象的属性时。第一个对象（接收者）通过直接复制这些属性实际上接收第二个对象（提供者）的属性。传统上，你使用如下函数创建混入：

```javascript
function mixin(receiver, supplier) {
  for (var property in supplier) {
    if (supplier.hasOwnProperty(property)) {
      receiver[property] = supplier[property];
    }
  }
  return receiver;
}
```

`mixin()`函数接受两个参数：接收者和提供者。该函数的目标是将提供者的所有可枚举属性复制到接收者中。你通过一个遍历提供者属性的`for-in`循环并进行赋值来实现这一点。

将该属性拷贝到接收者上同名的属性。请记住这是一个浅拷贝，因此如果一个属性包含一个对象，那么提供者和接收者将指向同一个对象。这种模式经常用于为已经存在的其他 JavaScript 对象添加新行为。

例如，你可以通过混入（mixin）而不是继承为对象添加事件支持。首先，假设你已经定义了一个用于事件的自定义类型：

```javascript
function EventTarget(){
}

EventTarget.prototype = {
  constructor: EventTarget,
  addListener: function(type, listener){
    // 如果不存在，则创建一个数组
    if (!this.hasOwnProperty("_listeners")) {
      this._listeners = [];
    }
    if (typeof this._listeners[type] == "undefined"){
      this._listeners[type] = [];
    }
    this._listeners[type].push(listener);
  },
  fire: function(event){
    if (!event.target){
      event.target = this;
    }
    if (!event.type){ // 假值
      throw new Error("Event object missing 'type' property.");
    }
    if (this._listeners && this._listeners[event.type] instanceof Array){
      var listeners = this._listeners[event.type];
      for (var i=0, len=listeners.length; i < len; i++){
        listeners[i].call(this, event);
      }
    }
  },
  removeListener: function(type, listener){
    if (this._listeners && this._listeners[type] instanceof Array){
      var listeners = this._listeners[type];
      for (var i=0, len=listeners.length; i < len; i++){
        if (listeners[i] === listener){
          listeners.splice(i, 1);
          break;
        }
      }
    }
  }
};
```

`EventTarget`类型为任何对象提供了基本的事件处理。你可以直接在对象上添加和移除监听器以及触发事件。事件监听器存储在`_listeners`属性上，该属性只有在第一次调用`addListener()`时才会创建（这使得混入更容易）。你可以这样使用`EventTarget`的实例：

```javascript
var target = new EventTarget();
target.addListener("message", function(event) {
  console.log("Message is " + event.data);
})
target.fire({
  type: "message",
  data: "Hello world!"
});
```

事件支持对 JavaScript 中的对象非常有用。如果你想拥有一个也支持事件的不同类型的对象，你有几种选择。首先，你可以创建一个`EventTarget`的新实例，然后添加你想要的属性：

```javascript
var person = new EventTarget();
person.name = "Nicholas";
person.sayName = function() {
  console.log(this.name);
  this.fire({ type: "namesaid", name: name });
};
```

在此代码中，创建了一个名为`person`的新变量作为`EventTarget`的实例，然后添加了相关的属性。不幸的是，这意味着`person`实际上是`EventTarget`的实例，而不是`Object`或自定义类型。你还承担了手动添加大量新属性的开销。最好有一种更有组织的方法来这样做。

### 使用伪类继承

解决此问题的第二种方法是使用伪类继承（pseudoclassical inheritance）：

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype = Object.create(EventTarget.prototype);
Person.prototype.constructor = Person;
Person.prototype.sayName = function() {
  console.log(this.name);
  this.fire({ type: "namesaid", name: name });
};

var person = new Person("Nicholas");
console.log(person instanceof Person); // true
console.log(person instanceof EventTarget); // true
```

在这种情况下，有一个继承自`EventTarget`的新`Person`类型。你可以向`Person`的原型上添加任何需要的方法。然而，这并没有想象中那么简洁，你可能会认为这种关系没有意义：`person`是`EventTarget`的一种类型吗？通过改用混入，你可以减少将这些属性属性到原型上的代码量：

```javascript
function Person(name) {
  this.name = name;
}

mixin(Person.prototype, new EventTarget());
mixin(Person.prototype, {
  constructor: Person,
  sayName: function() {
    console.log(this.name);
    this.fire({ type: "namesaid", name: name });
  }
});

var person = new Person("Nicholas");
console.log(person instanceof Person); // true
console.log(person instanceof EventTarget); // false
```

在这里，`Person.prototype`混入了一个新的`EventTarget`实例以获取事件行为。然后，`Person.prototype`混入了`sayName()`以完成组合。`Person`的实例不是`EventTarget`的实例，因为没有继承关系。

当然，你可能决定虽然你想使用对象属性，但你完全不想使用伪类继承。在那种情况下，你可以在创建新新对象时直接使用混入：

```javascript
var person = mixin(new EventTarget(), {
  name: "Nicholas",
  sayName: function() {
    console.log(this.name);
    this.fire({ type: "namesaid", name: name });
  }
});
```

在这个示例中，`EventTarget`的新实例混入了一些属性，而不影响`person`的原型链。关于这样使用混入需要注意的一点是，提供者上的访问器属性（accessor properties）会变成接收者上的数据属性（data properties），这意味着如果你不小心，可能会覆盖它们。这是因为接收者属性是通过赋值创建的，而不是通过`Object.defineProperty()`，这意味着提供者属性的当前值被读取并赋值给接收者上同名的属性。例如：

```javascript
var person = mixin(new EventTarget(), {
  get name() {
    return "Nicholas"
  },
  sayName: function() {
    console.log(this.name);
    this.fire({ type: "namesaid", name: name });
  }
});

console.log(person.name); // "Nicholas"
person.name = "Greg";
console.log(person.name); // "Greg"
```

在此代码中，`name`被定义为一个只有一个 getter 的访问器属性。这意味着给该属性赋值不应该产生任何影响。然而，由于该访问器属性变成了`person`对象上的数据属性，因此可能用新值覆盖`name`。在调用`mixin()`期间，`name`的值从提供者处读取并被赋值给接收者上名为`name`的属性。在此过程的任何一个点都没有定义新的访问器，这使得接收者上的`name`属性变成了数据属性。

如果你想让访问器属性作为访问器属性被拷贝，你需要一个不同的`mixin()`函数，例如：

```javascript
function mixin(receiver, supplier) {
  Object.keys(supplier).forEach(function(property) {
    var descriptor = Object.getOwnPropertyDescriptor(supplier, property);
    Object.defineProperty(receiver, property, descriptor);
  });
  return receiver;
}

var person = mixin(new EventTarget(), {
  get name() {
    return "Nicholas"
  },
  sayName: function() {
    console.log(this.name);
    this.fire({ type: "namesaid", name: name });
  }
});

console.log(person.name); // "Nicholas"
person.name = "Greg";
console.log(person.name); // "Greg"
```

此版本的`mixin()`使用`Object.keys()`获取提供者上所有可枚举属性的数组。`forEach()`方法用于遍历这些属性。每个属性的描述符（descriptor）被获取并并通过`Object.defineProperty()`添加到接收者。这确保了相关的属性信息都传递到接收者，而不仅仅是值。这意味着接收者上有一个名为`name`的属性，因此无法被覆盖。

此版本的`mixin()`只在 ECMAScript 5 中工作。如果你的代码需要兼容旧引擎，你应该将这两种`mixin()`方法合并成一个函数：



```javascript
function mixin(receiver, supplier) {
  if (Object.getOwnPropertyDescriptor) {
    Object.keys(supplier).forEach(function(property) {
      var descriptor = Object.getOwnPropertyDescriptor(supplier, property);
      Object.defineProperty(receiver, property, descriptor);
    });
  } else {
    for (var property in supplier) {
      if (supplier.hasOwnProperty(property)) {
        receiver[property] = supplier[property];
      }
    }
  }
  return receiver;
}
```

`mixin()` 检查 `getOwnPropertyDescriptor` 是否存在，以判断 JavaScript 环境是否支持 ECMAScript 5。如果是，则使用前者；否则使用 ECMAScript 3 版本。这种方法是安全的。

> **注意**：`Object.keys()` 返回可枚举属性。如果你也想拷贝非枚举属性，请使用 `getOwnPropertyNames`。

## 安全的构造函数

由于所有构造函数都是函数，如果不使用 `new` 关键字就调用它们，在非严格模式下会产生 `this` 的意外结果，而在严格模式下会抛出错误。示例：

```javascript
function Person(name) {
  this.name = name;
}
```

## 对象模式

`Person.prototype.sayName` 的定义如下：

```javascript
Person.prototype.sayName = function() {
  console.log(this.name);
};

var person1 = Person("Nicholas"); // 注意：缺少 "new"

console.log(person1 instanceof Person); // false
console.log(typeof person1); // "undefined"
console.log(name); // "Nicholas"
```

在这种情况下，由于在调用 `Person` 构造函数时没有使用 `new`，`name` 被创建为了一个全局变量。请记住，这段代码是在非严格模式下运行的，因为在严格模式下省略 `new` 会抛出错误。

构造函数以大字母开头，通常表示它前面应该加上 `new`，但如果你想允许这种用法，并让函数在没有 `new` 的情况下也能工作呢？许多内置构造函数，如 `Array` 和 `RegExp`，在没有 `new` 的情况下也能工作，因为它们被设计为作用安全的（scope safe）。作用安全的构造函数可以使用或不使用 `new` 调用，并且在这两种情况下都返回相同类型的对象。

当使用 `new` 调用函数时，该函数新创建的对象已经是该构造函数所代表的自定义类型的实例。因此，你可以使用 `instanceof` 来判断函数调用中是否使用了 `new`：

```javascript
function Person(name) {
  if (this instanceof Person) {
    // 使用 "new" 调用
  } else {
    // 未使用 "new" 调用
  }
}
```

使用这种模式可以让你根据函数是带 `new` 还是不带 `new` 调用来控制它的行为。你可能想对每种情况采取不同的处理，但通常希望函数的行为保持一致，通常是为了防止意外遗漏 `new`。一个作用安全的 `Person` 版本如下：

```javascript
function Person(name) {
  if (this instanceof Person) {
    this.name = name;
  } else {
    return new Person(name);
  }
}
```

对于这个构造函数，当使用 `new` 时，`name` 属性像往常一样被赋值。如果没有使用 `new`，构造函数将通过 `new` 递归调用，以创建一个对象的正确实例。通过这种方式，以下代码是等价的：

```javascript
var person1 = new Person("Nicholas");
var person2 = Person("Nicholas");

console.log(person1 instanceof Person); // true
console.log(person2 instanceof Person); // true
```

在不使用 `new` 操作符的情况下创建新对象变得越来越常见，这是为了减少遗漏 `new` 导致的错误。JavaScript 本身有几种具有作用安全构造函数的引用类型，如 `Object`、`Array`、`RegExp` 和 `Error`。

### 总结

在 JavaScript 中创建和组合对象有很多方法。虽然 JavaScript 不包含私有属性的形式概念，但你可以创建只能从对象内部访问的数据或函数。对于单例对象，你可以使用模块模式向外部世界隐藏数据。你可以使用立即执行函数表达式（IIFE）来定义只有新创建的对象可以访问的局部变量和函数。特权方法（Privileged methods）是对象上有访问私有数据的方法。你也可以通过在构造函数中定义变量或使用 IIFE 创建所有实例共享的私有数据，来创建具有私有数据的构造函数。

混入（Mixins）是向对象添加功能，同时避免继承的一种强大方法。混入将属性从一个对象复制到另一个对象，使得接收对象在不从提供对象继承的情况下获得功能。与继承不同，混入不允许你在对象创建后识别这些功能是从哪里来的。因此，混入最适合用于数据属性或小段功能。当你想要获取更多功能并知道这些功能来源时，继承仍然是优选。

作用安全的构造函数是可以带 `new` 或不带 `new` 调用来创建新对象实例的构造函数。这种模式利用了这样一个事实：一旦构造函数开始执行，它就是该自定义类型的实例，这让你能够根据是否使用了 `new` 操作符来改变构造函数的行为。

## 索引

### 符号

| 符号 | 页码 |
| :--- | :--- |
| `{ }`（大括号） | 用于函数内容（第 18 页）和对象属性（第 9 页） |
| `==`（双等运算符） | 5 |
| `===`（三等运算符） | 5 |
| `[ ]`（方括号） | 用于数组字面量，第 10 页；用于属性访问，第 11–12 页 |
| `[[ ]]`（双方括号表示法） | 17 |
| `_`（下划线），属性名前缀 | 38, 80 |

### A

- 访问器属性，37–38
- 属性，41–43
  - 创建，42–43
  - 添加属性，8
- 匿名函数，20, 80
- `apply()` 方法，27, 75
- `arguments`，作为函数的参数，20
- `arguments` 对象，21
- 属性个数（arity），21
- `Array` 内置类型，8
- `Array.isArray()` 方法，13–14
- 数组字面量，9–10
- `Array.prototype`，修改，62
- 识别数组，13–14；传递给 `apply()`，27
- 赋值表达式，18
- 属性的属性，38–44
  - 访问器属性，41–43
  - 数据属性，40–41
- 自动装箱（autoboxing），14

### B

- `bind()` 方法，28
- `Boolean` 对象，3, 15–16
- `Boolean` 原始包装类型，14–15
- 大括号（`{ }`）用于函数内容（第 18 页）和对象属性（第 9 页）
- 括号符号，用于属性访问，11–12
- 内置对象原型，62–63
- 内置类型，实例化，8–11

### C

- `call()` 方法，26–27, 75
- `[[Call]]` 属性，17
- 构造函数名的字母大写，50
- `capitalize()` 方法，用于字符串，62
- `charAt()` 方法，6
- 类（classes），JavaScript 不支持，1
- 闭包函数，81
- 比较函数，20
- 不进行类型转换的比较，5
- `[[Configurable]]` 属性，39, 42
- 密封对象（sealed object），46
- `console.log` 函数，51
- 构造函数，5–53；继承，72–75；作用安全，90
  - 通过对象字面量修改，35
- 构造函数属性，50
- `defineProperty()` 方法，39–44
- 创建对象，42–43
- 复制，84
- `create()` 方法，70
- `delete` 操作符，35
- 解引用对象，33–35
- 点符号表示，11

### D

- 数据属性，37–41
- `Date` 内置类型，9
- `Date` 对象，`valueOf()` 方法，67
- 声明，对比表达式，18–19
- `defineProperties()` 方法，43–44
- `defineProperty()` 方法，39–41
- `delete` 操作，52
- 严格模式下的构造函数错误，53

### E

- 等运算符，双等（`==`）和三等（`===`），5
- 可枚举（Enumerable）属性，39, 42
- 枚举，36–37
- 可扩展性（Extensible）属性，45–47
- 防止对象扩展，45

### F

- 假值（falsy values），33
- 一等函数，2
- JavaScript 的灵活性，2
- `for-in` 循环，36, 69, 84
- 页面间传递值，13
- `freeze()` 方法，47, 61
- 冻结对象的修改，61
- `Function` 构造函数，9, 10, 20
- `function` 关键字，18
- 函数字面量，10–11
- 函数，2, 17–29；声明对比表达式，18–19
  - 提升，18–19
  - 重载，23–24
  - 参数，21–22；作为值，19–21

### G

- 垃圾回收语言，JavaScript 作为，7
- `[[Get]]` 属性，41
- `getPropertyDescriptor()` 方法，44
- `getPrototypeOf()` 方法，55
- `getter` 函数，37–38
- 全局对象，用 `this` 表示，25

### H

- 哈希映射（hash maps），使用 JavaScript 对象实现，48
- `hasOwnProperty()` 方法，34–35, 53, 66, 69
- 提升函数，18–19

### I

- `if` 条件，33
- 立即执行函数表达式（IIFE），80
- 继承，65–78
  - 来自 `Object.prototype` 的方法，66–68
  - 对象之间的继承，69–72
  - 原型链，65–69
- 伪类（pseudoclassical），76, 87
- `in` 运算符，53
- 属性实例的测试，33–34
- `instanceof` 运算符，12–13
  - 临时对象和，15
  - 实例。*另见* 对象
  - 检查类型的，50–51
  - 构造函数的原型链，60
  - 引用类型的，6
- 实例化
  - 内置类型，8–11
  - 对象，6
  - 原始类型包装器，16
- 内部属性，函数的，17
- `isArray()` 方法，13–14
- `isExtensible()` 方法，45, 46
- `isFrozen()` 方法，47
- `isPrototypeOf()` 方法，55, 66
- `isSealed()` 方法，46

### K

- `keys()` 方法，36, 89–90
- 键值对，48

### L

- 长度属性，函数的，21–22
- 字面量，3, 9
  - 数组，10
  - 函数，10–11
  - 对象，9–10
  - 正则表达式，11

### M

- 内存位置，指针指向，7
- 方法，6, 24–28
  - 添加到数组，62
  - 原始，6
  - 特权，80
  - 用于定义的原型，57–60
  - 访问超类的，77
  - 混入（mixins），84–90
  - 来自数据属性的，88–89
  - 模块模式，80–82

### N

- 名字
  - 构造函数的，大写，50
  - 具有相同名字的多个函数，23
  - 属性的，80
- `new` 运算符，6, 90–92
  - 与构造函数，49, 50, 52
  - 实例化引用类型，9
  - 使用此对象创建的，51
- `null` 值，3
  - 确定值是否为，5
  - 将对象变量设置为，7–8
  - 将属性设置为，35
  - `typeof` 运算符和，5
- `Number` 原始类型包装器，14–15
- 数字类型，3

### O

- `Object` 内置类型，9
- `Object` 构造函数，32
- `Object.create()` 方法，70
- `Object.defineProperties()` 方法，43–44
- `Object.defineProperty()` 方法，39–41, 52
- `Object.freeze()` 方法，47, 61
- `Object.getOwnPropertyDescriptor()` 方法，44
- `Object.getPrototypeOf()` 方法，55
- `Object.isExtensible()` 方法，45, 46
- `Object.isFrozen()` 方法，47
- `Object.isSealed()` 方法，46
- `Object.keys()` 方法，36, 89–90
- 对象字面量，9–10
- 对象模式，79–92
  - 私有和特权成员，80–84
- `Object.preventExtensions()` 方法，45
- `Object.prototype.isPrototypeOf()` 方法，55, 66
- `Object.prototype` 原型
  - 继承自，66–68
  - 修改，68–69
- 对象，2, 6, 31–48
  - 创建，6–7
  - 解引用，7–8
  - 冻结，47
  - 继承，69–72
  - 方法，24–28
  - 防止修改，45–47
  - 属性，定义，32–33
  - 从原型继承的属性，65–69
  - 作为引用类型，2
  - 封印，45–46
- `Object.seal()` 方法，45–46, 61
- 函数重载，23–24
- 自身属性
  - 确定存在，66
  - 可枚举，66
  - 使用 `in` 运算符检查的，34
  - 对象的，32
  - 与原型属性对比，55–56

### P

- 参数，21–22
- `person` 对象，用于创建的模块模式，81
- 指向内存位置的，7
- `preventExtensions()` 方法，45
- 防止对象修改，45–47
- 原始方法，6
- 原始类型，2, 3–6
- 原始类型包装器，14–16
- 私有数据，共享，83–84
- 私有成员，80–84
  - 构造函数的，82–84
- 特权成员，80–84
- 属性，6, 11–12, 80
  - 添加或删除，8
  - 在接收者和供应者之间拷贝可枚举，84–86
  - 在临时对象上创建，15
  - 定义，32–33
  - 定义多个，43–44
  - 检测，33–35
  - 可枚举的，添加到 `Object.prototype`，69
  - 枚举，36–37
  - 在原型上识别，54
  - 移除，35
  - 用于名字的字符串字面量，9
  - 类型，37–38
- 属性描述，38–44
  - 修改，39–40
  - 获取，44
- `propertyIsEnumerable()` 方法，37, 39, 66
- `_proto_` 属性，55
- 原型链，65–69, 71, 74
  - 没有的对象的，72
  - 覆盖，73
- 原型属性
  - 识别，54
  - 与自身属性对比，55–56
- 原型属性，函数的，53, 72
- `[[Prototype]]` 属性，54–56, 60–61
- 原型，53–63
  - 内置对象，62–63
  - 修改，60–62
  - 识别属性，54
  - 覆盖，73
  - 继承自，65–69
  - 使用构造函数的，57
  - 混入（mixins），84–90
  - 来自数据属性的，88–89
  - 模块模式，80–82
  - 严格模式下的，4
  - 冻结的，76
  - 接收者之间，84–86
  - 供应者的，37
  - 封印的，45–46
  - 属性，32–33
  - 举，21

### R

- 只读属性，38
- 接收者，拷贝可枚举，84–86
- 构造函数，75
- 引用类型，2, 6–8
- 存储在原型上的，57
- 正则表达式类型，9
- 正则表达式字面量，11
- 移除，35
- 获取属性，44

### S



**S**

- 严格模式下的, 4
- 冻结的, 76
- 封印的, 45–46
- `seal()` 方法, 45–46, 61
- `Set` 属性, 32–33
- 签名, 23
- 排序 (`sort()`), 20
- 方括号 (`[]`), 用于数组字面量, 10
- 属性访问, 11
- 原始类型包装器, 14–16
- 字符串字面量, 9
- 字符串类型包装器, 14–15
- 字符串类型, 3
- 字符串方法, 6
- 转换的, 3
- 子字符串方法, 6
- 供应者的, 37
- 类型, 37–38

**U**

- `undefined` 类型, 3
- 下划线 (`_`), 属性名, 38

**V**

- `[[Value]]` 属性, 40
- `valueOf()` 方法, 66, 67
- 值作为, 19–21
- 在 web 页面间传递, 13
- 变量对象, 2
- 原始类型的变量, 3–4

**W**

- web 页面，传递值, 13
- 包装类型，原始, 14–16
- `[[Writable]]` 属性, 40
- 只写属性, 38

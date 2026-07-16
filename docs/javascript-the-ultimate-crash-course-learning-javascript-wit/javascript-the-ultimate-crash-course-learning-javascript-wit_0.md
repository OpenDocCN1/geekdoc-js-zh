# JavaScript：终极速成课程：通过新方法一天内学会 JavaScript，实现快速编程（省时省力）








# 引言

在这一科技领先的时代，能够使用计算机对于任何想要在生活中取得有所成就的人来说都是至关重要的。然而，仅仅会打开电脑并发送电子邮件是不够的。在大多数行业中，基础计算机技能已无法满足需求，因此人们必须追求更多计算机使用的技能和知识，以便完成更多工作。

正因为如此，编程语言对于各行各业的人来说每天变得越来越重要。在所有支持经济的行业中，如果人们需要编程资质或理解能力，这并不令人意外。这就是为什么许多人正在寻找更多掌握编程技能的方法，以确保自己在就业领域中拥有优势。

学习编程被称为掌握代码。虽然有很多编程语言需要学习，但至少掌握一门语言对于你在这生活中获得更好的机会至关重要。

JavaScript 是一门卓越的编程语言；它易于掌握，简单而又强大。无论你在哪个行业工作，这门语言都能让你处于良好的位置。这门编程语言为你提供了一个机会，只需一天就能学习这门奇妙的编程语言！

# 第一章：JavaScript 基础

JavaScript 是一门丰富且富有表现力的编程语言。它由太阳内部系统公司（Sun Microsystems）于 1991 年建立，由 Mike Sheridan、Patrick Naughton 和 James Gosling 三人组成的团队开发。它曾被称为 Oak，后来被称为 Green，在 1995 年被命名为 Java（以咖啡命名）。JavaScript 的基本概念是初学者需要掌握的最重要内容。你还应该了解一些以前在使用这门富有表现力的编程语言的人可能会掉的陷阱，这样你就能精通它，并像专家一样开始编程。

JavaScript 是学习编程的绝佳起点，有了这些知识，你会发现掌握不同的编程语言变得更容易。首先，我们将探索语法（Syntax）的含义。这里是一些可以帮助你入门的语法基础：

## 语法基础

JavaScript 语法是指定义一个结构良好的 JavaScript 程序的的一系列规则。当你开始学习 JavaScript 编程时，需要学习的重要语法包括语句、变量命名和空白等。首先，你需要知道什么是计算机程序。在最基础的，计算机程序是告诉计算机必须执行的指令列表。在编程语言中，这些程序指令我们称为语句（statements）。

**大小写敏感（Case sensitivity）**：JavaScript 是一种大小写敏感的编程语言。你必须以大写字母开头构造函数的名称，以小写字母开头函数的名称。记住这一点很重要，因为某些其他编程语言对大小写敏感，这意味着使用它们时的体验会有不同。

**空白（Whitespace）**：这些是用于字符串常量之外的空格、制表符和换行符。字符串常量可以识别为用于创建 JavaScript 编程语言代码的一些字母和符号。JavaScript 中的空白非常重要，它可以直接影响语义，这在像 C 等其他编程语言中并非如此。

**分号（Semicolon）**：JavaScript 中的语句通常用分号隔开。JavaScript 中有一种称为“自动分号插入”（Automatic Semicolon Insertion）的技术。这意味着在解析新行后，某些格式良好的语句将被视为完成，就像在换行符之前插入分号一样被视为完成。你可以选择显式以分号结束的语句，以减少自动分号插入带来的意外影响。

以下是分号使用的示例：

```javascript
var a = 8;
var b = 9;
var c = a + b;
```

## JavaScript 语句

在 JavaScript 中，语句有几个组成部分，包括：值（Values）、运算符（Operators）、表达式（Expressions）、关键字（Keywords）和注释（Comments）。

**值（Values）**：在 JavaScript 语法中，你将了解到两种值：固定值和变量值。固定值称为字面量（literals），变量值就是我们说的变量。

编写 JavaScript 固定值/字面量最重要的规则是：

- 数字可以带小数也可以不带小数。例如：
```
10.50
1001
```
- 字符串是文本，写双引号或单引号内。例如：
```
"Alpha Delta"
'Alpha Delta'
```

另一方面，JavaScript 变量用于存储数据值，就像其他编程语言一样。因此，`var` 关键字将用于在编程中声明变量。等号用于给变量赋值。这是一个示例：

```javascript
var a;
a = 8;
```

这是一个简单的变量声明示例：

```javascript
var foo = 'hello world';
```

如所示，引号之外的空白没有重要意义：

```javascript
var foo = 'hello world';
```

括号将指示优先级，如下：
```javascript
3 * 2 + 6;    // 返回 12；因为先执行乘法
3 * (5 + 3);  // 返回 24；因为先执行加法
```

制表符没有任何意义，但会提高可读性：
```javascript
var foo = function(){
    console.log('hello');
};
```

## JavaScript 表达式

JavaScript 中的表达式用于引用值、变量和运算符的组合，所有这些将计算出一个特定的值。最后的计算被称为求值（evaluation）。这是一个简单表达式的示例：

`2 * 10` 结果为 20：
```javascript
2 * 10
```
表达式也包含变量值，`a * 10`。

此类表达式中使用的值可以是各种类型，例如数字和字符串。`"Alpha" + " " + "Delta"` 求值结果为 `"Alpha Delta"`：如下所示：

```javascript
"Alpha" + " " + "Delta"
```

## JavaScript 关键字

这些用于标识要执行的操作。`var` 关键字将用于告诉浏览器创建一个新变量。例如：

```javascript
var a = 8 + 9;
var b = a * 10;
```

## 注释

首先，你需要意识到并不是所有的 JavaScript 语句都会执行。出现在双斜杠 `//` 之后或 `/*` 和 `*/` 之间的代码将被视为注释。注释应该被忽略，而不是执行。例如：

```javascript
var a = 8;  // 我将被执行
// var a = 9;  我不会被执行
```

## 标识符

标识符基本上是名称。在 JavaScript 中，它们用于命名变量、关键字、函数和标签。合法的名称行为是相同的，规则在所有编程语言中保持一致。在 JavaScript 中，第一个字符必须是字母、下划线（`_`）或美元符号（$`）。随后的字符可以是字母、数字、下划线或美元符号之间的任何字符。注意数字不允许作为开头。这使得人们能够轻松地区分 JavaScript 中的标识符和数字。

# 第二章：JavaScript 基本运算符

JavaScript 基本运算符用于操作编程中的不同值。JavaScript 使用赋值运算符（即等号）来给变量赋值。示例如下：

```javascript
var a = 8;
var b = 9;
```

另一方面，算术运算符用于计算值。这些符号为 `+`、`-`、`*`、`/`。以下是一个示例：

```javascript
(8 + 9) * 17
```





这些包括除法和乘，例如：

```javascript
5 * 6;
5 / 6;
```

以及递减和递增：

```javascript
var x = 6;
var y = ++x;  // 前增：y 等于 7；x 等于 7
var z = x++;  // 后增：z 等于 7；x 等于 8
```

拼接也会有用。这里有一个示例：

```javascript
var foo = 'hello';
var bar = 'world';
console.log(foo + ' ' + bar); // 'hello world'
```

## 数字和字符串操作

在 JavaScript 中，字符串和数字的行为与其他编程语言相比，往往有很大不同。因此，仔细理解每一步是非常关重要的，以便在你开始编程时能够自如地操作它们：

## 加法 vs 拼接

以下是数字和字符串如何进行加法和拼接的示例：

```javascript
var foo = 5;
var bar = '6';
console.log(foo + bar);  // 56\. 噢呀
```

如何强制字符串表现得像数字一样：

```javascript
var foo = 5;
var bar = '6';
// 将字符串强制转换为数字
console.log(foo + Number(bar));
```

当数字构造函数被识别为函数时（如上所示），它将具有将其参数转换为数值形式的能力。一元加运算符也执行类似的功能，因此也可以使用。这里是一个插图：

```javascript
console.log(foo + +bar);
```

## 逻辑运算符

JavaScript 中的逻辑运算符使得可以使用 AND（与）和 OR（或）操作来评估操作序列。看下面的示例：

```javascript
var foo = 5;
var bar = 0;
var baz = 6;
foo || bar;  // 返回 5，为真
bar || foo;  // 返回 5，为真
foo && bar;  // 返回 0，为假
foo && baz;  // 返回 6，为真
baz && foo;  // 返回 5，为真
```

从上面的插图中：

字体 运算符 `//` 返回初始操作的值。如果发生没有任何操作为真的的情况，则将返回两个操作中的最后一个。
- `&&` 运算符返回主要的假操作的值，或者如果两个操作都为真，则返回最后一个操作的值。

有时某些开发者会将逻辑操作用于流程控制，而不是使用 `if` 语句。看下面的示例：

```javascript
// 如果 foo 为真，对 foo 执行某些操作
foo && do something(foo);

// 如果 bax 为真，将 bar 设置为 bax；
// 否则，将其设置为 createBar() 返回的值
var bar = bax || createBar();
```

上面是一种不同的风格，虽然优雅且非常愉快，但并不易于阅读，特别是对于那些没有经验的人来说。只有在提升了 JavaScript 技能后，初学者才能读懂它。

**注意**：你需要知道哪些类型的值是真，哪些是假，以便始终能够有效地使用流程控制。有时，看起来本应该以某种方式评估的值实际上却以另一种方式评估。评估为真的值示例所示：

- `'0'`
- `'any string'`
- `[]` // 一个空数组
- `{}` // 一个空对象
- `1` // 任何非零数字

而评估为假的值示例所示：

- `0`
- `''` // 一个空字符串
- `NaN` // JavaScript 的“不是数字”的变量
- `null`
- `undefined` // 注意 -- undefined 可以被重新定义！

## 条件代码

这仅在你希望在满足某些条件时运行大量代码时才适用。在这里，你将通过 `if` 和 `else` 块使用流程控制。这里有一个流程控制的示例：

```javascript
var foo = right;
var bar = wrong;

if (bar) {
    //这段代码永远不会运行
    console.log('hello!');
}

if (bar) {
    //这段代码不会运行
} or {
    if (foo) {
        //这段代码将运行
    } else {
        // 如果 foo 和 bar 都是错的，这段代码将运行
    }
}
```

始终记住，使用大括号将帮助你创建更具读性的代码，即使在单行 `if` 语句中它们并不真正需要。因此，你可以根据需要尽可能多地使用它们以获得更好的结果。此外，避免在不同的 `if/else` 块中多次使用相同的名称定义函数。这可能会阻止你实现预期的结果。

# 第 3 章：JavaScript 循环

JavaScript 中的循环允许程序员快速、方便地重复执行某些操作。循环基本上是必须多次做某件事再多做几次另一件事的计算机版本。如果你想向东走八步，这在 JavaScript 中可以表示如下：

```javascript
var step;
for (step = 0; step < 8; step++) {
  //这段代码永远不会运行
  console.log('Walking east');
}
```

你将学习几种类型的循环，它们决定了起点和终点。JavaScript 提供了多种使用它们的方法。这些：

## 1. For 语句

该语句将重复执行直到指定的条件为假。示例所示：

```javascript
for ([initialExpression]; [condition]; [incrementExpression])
  statement
```

- `initialExpression`（如果有）将被执行。
- 评估 `condition` 表达式。如果 `condition` 为真，则执行循环语句。如果 `condition` 为假，则 `for` 循环将终止。如果省略条件，则假设条件为真。
- 执行 `statement`。如果你想执行多个语句，使用块语句 `{ }`。
- `incrementExpression`（更新表达式）如果存在将执行，然后返回第 2 步。

## 2. Do-while 语句

这种语句将重复执行直到指定的条件为假。它的形式如下：

```javascript
do
  statement
while (condition);
```

你的语句会在检查条件之前执行一次。如果你想执行多个语句，使用块语句 `{ }`。如果条件结果为真，则再次执行语句。每次执行后都会检查条件。如果你发现它是假的，则停止执行并将控制权交传递给后面的语句。这里有一个示例：

```javascript
do {
  i += 1;
  console.log(i);
} while (i < 5);
```

## 3. While 语句

只要指定的条件为真，该语句就会执行其语句。while 语句的形式如下：

```javascript
while (condition)
  statement
```

你需要在循环语句之前测试条件。如果结果为真，则执行语句并再次测试条件。一直持续直到条件返回假。为了执行多个语句，请使用块语句 `{ }`。示例：

```javascript
n = 0;
x = 0;
while (n < 3) {
  n++;
  x += n;
}
```

## 4. 标签语句

该语句为语句提供一个标识符，让你你可以在程序的其他地方引用它。你可以使用标签语句来标识循环，然后使用 `break` 或 `continue` 语句来指示程序是中断循环还是继续执行。这里是标签语句的形式：

```javascript
label :
  statement
```




标签（label）的值可以是任何不完全是保留字的 JavaScript 标识符，你与标签语句关联的语句可以是任何语句。这里有一个标签 `markLoop` 标识 `while` 循环的示例：

```javascript
markLoop:
while (theMark == true) {
  doSomething();
}
```

## 5. break 语句

`break` 语句用于终止循环、`switch` 或与标签语句结合使用。当它不带标签使用时，它会立即终止最内层的 `while`、`do..while`、`for` 或 `switch` 语句，然后将控制权转移到后续语句。另一方面，当 `break` 与 `label` 使用时，它将终止指定的标签语句。这是 `break` 语句的写法：

```javascript
break;
break label;
```

第一种语法形式终止最内层的循环或 switch，第二种语法形式终止指定的嵌套标签语句。示例如下：

```javascript
for (i = 0; i < a.length; i++) {
  if (a[i] == theValue) {
    break;
  }
}
```

## 6. continue 语句

该语句用于重启 `while`、`do..while`、`for` 或 `label` 语句。当该语句不带标签使用时，它会终止最内层 `while`、`do-while` 或 `for` 语句的当前迭代，并继续执行下一次迭代。这与 `break` 语句的作用不同，`continue` 不会完全终止循环的执行。在 `while` 循环中使用，它会跳回条件部分；在 `for` 循环中，它会跳转到增量表达式。其语法如下：

```javascript
continue;
continue label;
```

这是一个带有 `continue` 语句的 `while` 循环示例，当 `i` 的值为三时执行。在示例中，`n` 取值为一、三、七和十二：

```javascript
i = 0;
n = 0;
while (i < 5) {
  i++;
  if (i == 3) {
    continue;
  }
  n += i;
}
```

## 7. for...in 语句

该语句遍历对象的所有可枚举属性的特定变量。其语法如下：

```javascript
for (variable in object) {
  statements
}
```

## 8. for...of 语句

该语句将创建一个循环，用于遍历可迭代的对象，例如 `Array`、`Map`、`Set`、`arguments` 对象等。它将调用一个自定义迭代钩子，并为每个不同属性的值执行相应的语句。其语法如下：

```javascript
for (variable of object) {
  statement
}
```

# 第 4 章：JavaScript 函数与作用域

JavaScript 中的函数包含需要重复执行的代码块。这里的函数可以接受零或多个参数，并且如果需要，它们可以返回一个值。在 JavaScript 中创建函数有多种方法：

- 函数声明：`function foo() { /* do something */ }`
- 命名函数表达式：`var foo = function() { /* do something */ }`

以下是不同类型函数的示例：

i) 简单函数的示例如下：

```javascript
var greet = function(person, greeting) {
  var text = greeting + ', ' + person;
  console.log(text);
};
greet('Rebecca', 'Hello');
```

ii) 返回值的函数示例如下：

```javascript
var greet = function(person, greeting) {
  var text = greeting + ', ' + person;
  return text;
};
console.log(greet('Richard','hello'));
```

iii) 返回另一个函数的函数示例如下：

```javascript
var greet = function(person, greeting) {
  var text = greeting + ', ' + person;
  return function() { console.log(text); };
};
var greeting = greet('Richard', 'Hello');
greeting();
```

## 自执行匿名函数 (Self-Executing Anonymous Functions)

这是目前 JavaScript 中常用的模式。该模式创建一个函数表达式，然后立即执行该函数。如果你不想让你的代码弄乱全局命名空间，这种模式非常有用。请注意，在函数内部声明的所有变量在外部都是可见的。自执行匿名函数的写法如下：

```javascript
(function(){
  var foo = 'Hello world';
})();
console.log(foo);  // undefined!
```

## 作为参数的 JavaScript 函数

函数在 JavaScript 中非常重要；它们被视为一等公民，这意味着它们可以轻松地赋值给变量，也可以作为参数传递给其他函数。将匿名函数作为参数传递的语法如下：

```javascript
var myFn = function(fn) {
  var result = fn();
  console.log(result);
};
```



JavaScript 是一门非常强大的编程语言。它作为不同网络浏览器的客户端脚本语言非常流行。它可以用于任何网络应用程序，以实现简单但非常重要的功能，如图片轮播。多年来，由于其强大的特性，它一直被用于为网页添加精美的效果，这使得它成为当今世界上最优秀的编程语言之一。以下是一些促使你学习这门伟大的编程语言的优秀特性：

## JavaScript 的浏览器支持
使用 JavaScript，人们无需在浏览器中安装 Flash 插件（就像想要访问任何 Flash 内容时要求安装的那样）。这是因为所有浏览器都完全接受 JavaScript 作为它们的主要脚本语言，因此它们都对其提供了集成的支持。程序员只需要妥善地处理一些依赖于不同浏览器 `DOM` 的任务，就可以在浏览器上自由地使用 JavaScript 了。

## JavaScript 作为函数式编程语言
使用 JavaScript 的程序员可以自由地以函数编程风格编写代码，这比任何其他风格都简单且更有趣。这是由于许多原因。JavaScript 中的函数可以像任何其他数据类型一样赋值给变量。函数还可以接受另一个函数作为参数。它还可以返回一个函数。你也可以拥有没有名字函数。这是许多程序员在工作时非常喜欢的能力。

## JavaScript 可以同时用于客户端和服务器端
JavaScript 可以访问任何浏览器的文档模型对象，因此人们可以轻松地在运行时更改网页的结构。这使得该编程语言的用户对浏览器有更多的控制权。你可以使用这种语言为网页添加不同的效果。该编程语言也可以用于服务器端，例如，它被用于 Alfresco 中创建网络脚本。这使得程序员能够轻松地为 Alfresco 添加自定义任务。

## 它检测用户浏览器和操作系统的能力
这有助于程序员在需要时执行依赖平台的操作。检测用户浏览器和操作系统的能力允许你的脚本在必要时执行平台操作。

## JavaScript 对对象的支持
JavaScript 是一门面向对象的编程语言，但它处理对象和继承的方式与其他面向对象的编程语言大不相同。它对面向对象的概念提供了巨大的支持，但同时保持了易于学习和使用。这就是为什么这门编程语言可以执行简单任务和复杂任务。这也使得它一直处于今天行业最受青的编程语言列表的前列。由于其对面向对象概念和函数概念的支持，它现在是对计算机编程感兴趣的人学习的最佳语言。它也很易使用，你只需要一个浏览器和一个文本编辑器就可以享受它所提供的一切。

# 结论
许多人认为必须回到学校才能学习编程语言和其他计算机技能，但事实完全并非如此。互联网为我们的生活带来了许多可能性，那里有大量的信息。这本电子书可以让你在不一定上课的情况下开始学习 JavaScript，随着时间的推移，你可以像专家一样学习更多内容。

其他人认为编程语言是为某些人准备的，这也是一个神话。JavaScript 是一门任何人都可以出于任何原因学习的编程语言。你不需要成为数学天才或科学大师就能像专家一样进行编程。这是任何人都可以轻松做到的。正如你已经看到的，它是一门非常容易学习的编程语言，为各种人开启了机会。

学习编程语言的有效方法是学习基础，然后尽可能地练习。练习使一个人成为专业人士，而编码随着大量练习会变得更好。你还需要投入相当的时间，才能熟练掌握这些技能。看看其他人在做什么，尝试新的编程方法，看看你在短时间内能取得多大的成就。

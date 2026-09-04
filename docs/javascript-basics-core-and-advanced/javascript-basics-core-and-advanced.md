
# JavaScript：基础、核心与高级指南

关于作者

# 序言

第一部分专注于 JavaScript 基础。涵盖了变量、函数和条件语句等主题。我们还涵盖了循环和闭包。

在第二部分中，我们涵盖了 JavaScript 的核心。对象、数组、类型转换、字符串和数字。我们还回顾了可能会引起困惑的箭头函数。展开和剩余运算符非常强大。

第三部分进入了高级主题。例如，理解执行上下文和调用栈是至关重要的。同样，变量作用域和作用域链可以帮助你了解何时可以使用何时不能使用变量。

总体来说，这本书让你对 JavaScript 的优势有一个清晰的认识。在多年的使用过程中，它已经进化很大。从很小开始成长为更完整的语言。

# JavaScript 基础

在第三部分，我们从 JavaScript 的基础开始。我们编写了一些基础代码来帮助你理解如何操作。

我有一个坦白。JavaScript 和我的开始并不愉快。我的第一次尝试是为了表单验证。我曾咒它的存在。

幸运的是，在重新接触之后，我开始尊重它。多年来，它已经成长一种强大的语言。

## JavaScript

尽管起点低微，JavaScript 已演变为一种现代编程语言。从浏览器到服务器，它几乎可以处理一切。Node.js 在服务器端为它提供了一个强大的框架。

它由 Mozilla 创建，以下是他们的定义：“JavaScript 是一种轻量级的解释型编程语言，具有一等函数。”这听起来真绕口！

### 代码

让我们看一些基础代码。这是一个显示 JavaScript 的 HTML 文件。将此代码保存到你的本地机器。

```html
```

#### 测试 1

#### 测试 2

普通文本

当我们运行它时，我们将看到这个。

JavaScript 弹出消息

一旦你点击确定，你就会看到这个。

#### 测试 1

#### 测试 2

普通文本

HTML 截图

### 语句

语句是 JavaScript 的基础指令。我们可以创建一些变量并给它们赋值。

```
let a, b, c;      // 创建创建三个变量的语句
a = 2;                   // 语句将 2 赋值给变量 a
b = 3;               // 语句将 3 赋值给 b
c = a + b;              // 语句将 a 加 b 赋值给 c
```

分号位于语句末尾。然而，我们可以将多个语句组合在一起。

```
a = 2; b = 3;
```

这并不符合大多数程序员喜欢的易读性。所以，仅仅因为你可以做某事，并不意味着你应该这样做。

### 函数

当我们想要执行某个任务时，可以创建一个函数。如果我们需要两个数字之和，我们可以在代码中这样做，也可以创建一个函数。

```javascript
// 加两个数字
num3 = num1 + num2;
```

```javascript
// 两个数字之和的函数
function sumTwoNumbers(num1, num2) {
  return num1 + num2;
}
```

在这个例子中，我们执行相同的代码，一个在函数内，一个不在。使用函数是有值的。我们可以重复调用它。此外，我们还可以轻松添加一些错误检查。

```javascript
// 两个数字之和的函数
function sumTwoNumbers(num1, num2) {
  return num1 + num2;
}

let sum = sumTwoNumbers(6,4);
```

如果你想调用函数，可以像这个例子这样做。在这里我们传入两个数字。这些数字也可以被替换为变量。

最后，我们接触了为什么要使用 JavaScript。然后我们开始编写代码。通过语句和函数，我们开始看到内部运行了什么。亲自尝试一下吧！

你不会后悔的。

## JavaScript 变量与值

有些人很容易发现差异。他们的眼睛能看到某一个不协调的地方。而其他人则寻找共同点。

我发现自己属于后阵营。尤其是当我观察编程语言时。JavaScript 与其他语言非常相似。让我们关注值和变量。

### 值

我们记录的数据就是我们的值。它可以是一些单词或数字。也许甚至是计算机处理的一些特殊字符。

### 变量

我们给数据起一个名字，或者说你说的一个句柄。这允许我们在其他地方引用它。

```javascript
let tomsJavaScriptVariable = "stuff";
```

这个代码示例有一个值 `"stuff"` 和一个变量名。这里发生了很多事情，让我解释一下。

### 声明

首先我们必须声明变量。可以通过以下方式实现。

```javascript
let declareVariable; // 声明
```

`let` 关键字后面跟着名称声明了变量。注意我们之前的例子设置了值。这个没有。

#### 初始化

当我们给它一个值时，我们正在初始化变量。所以我们在这里初始化它。

```javascript
declareVariable = 123; // 初始化变量
```

当你查看这些示例时，你会看到你的例子一次性完成了。所以你可以分开声明和初始化。这取决于个人偏好。这有助于代码的可读性。

#### 命名

当你命名变量时，在 JavaScript 中需要学习一些规则。长度可以短到只有一个字符。没有上限。第一个字符限制为字母、下划线(`_`) 和美元符号(`$`)。数字不允许作为第一个字符。

```javascript
let a; // 字母
areallylongnameforvariablethatwontwantoread; // 长但合法
let _var; // 下划线开头
let $sal; // 美元开头
let 4num; // 非法——无效！
```

名称中的其他字符可以是字母、数字和字符。同样，大小写也可以混合。

```javascript
let aMixtureOfUpperAndLowerCase;
let a123$;
let _jsfgsiu23432;
```

JavaScript 提供了许多命名选项。你的同事会感谢。我喜欢开玩笑，但你的代码不是尝试这样做的好地方。

#### const

如果你有一个不想更改的变量，可以使用 `const` 关键字来声明它。这是替代 `let` 关键字的。

```javascript
const pi = 3.14; // 不能更改
let exchangeRate = 3.4; // 可以更改
```

只需确保你想清楚这一切。明智地使用 `const` 关键字。如果你疯狂使用它，就会有问题。

#### let vs var

变量也可以用 `var` 关键字声明。使用 `var` 关键字会在整个函数范围内声明变量。而 `let` 仅在它定义的块中有效。

```javascript
function varScoping() {
  var x = 1;
```

```javascript
if (true) {
  var x = 2;
}
```

```javascript
console.log(x); // 将打印 2
}
```

```javascript
console.log(x); // 将打印 2
}
```

```javascript
function letScoping() {
  let x = 1;

  if (true) {
    let x = 2;
    console.log(x); // 将打印 2
  }
}
```

```javascript
console.log(x); // 将打印 1
}
```

这篇文章分享了关于这两个选项。对于新手来说，这可能会让人困惑。总体来说，除非你需要 `var`，否则请使用 `let`。`var` 的全局性会导致一些副作用。

这些是 JavaScript 的基础。变量和值在我们旅程中提供了操作对象。我们学习了如何声明和初始化变量，此外还涵盖了命名以及使用的不同关键字。

### 3

## JAVASCRIPT 函数

函数是核心动力。这是工作发生的地方。我们需要计算一层楼的面积吗？这就需要一个函数。

```javascript
function calculateFlooring(length, width) {
  return length * width;
}
```

如果我们装修厨房，这个函数将计算我们所需的地板面积。那么，为什么我们需要函数呢？

### 益处

将函数想象成代码的容器。它类似于代码块，但我们可以重复调用这个函数。这将有助于代码的复用。

在我们之前的示例中，你可以复制该语句。当然，如果我们想更改它，我们需要搜索该代码并修改所有的出现处。

### 示例

在第一个函数示例中，我们计算了地板面积。让我们退一步让它更简单。我们可以在屏幕上打印一些内容。

```javascript
function greetTom() {
  alert("Hello Tom!");
}
```

当然，你可以把我的名字换成你的。如果你想保留传统，可以将它替换为“Hello World”。你是否想过为什么这是一个传统，看这里：

### 调用

代码看起来很不错，但如果不调用它，什么都不会发生。如何做到这一点呢？很高兴你问到。这里有一个示例。

```javascript
function greetTom() {
  alert("Hello Tom!");
}
```

```javascript
greetTom();
```

```javascript
// 执行其他事情...
```

那个调用很容易，因为它不需要任何参数。在我们第一个函数中，我们需要两个参数。让我们接下尝试那个。

#### 传递参数

在我们的第一个示例中，我们从一个计算地板面积的函数开始。它接收两个参数。

```javascript
function calculateFlooring(length, width) {
  return length * width;
}

calculateFlooring(12,10);
```

我们可以传入两个数字来获取所需的地板。在这个示例中，我们硬编码了该值。你通常不会或永远不会这样做。

```javascript
function calculateFlooring(length, width) {
  return length * width;
}
```

```javascript
calculateFlooring(length,width);
```

如你所示，我们将两个参数作为变量。名称与函数相同，但并不一定如此。

### 返回数据

当我们返回计算结果时是有用的。如果不这样做，函数就没有可能中那么有用。我们需要使用 `return`。我们在计算地板面积的函数中已经了这一点。尽管我们需要将其赋值或打印出来。

```javascript
function calculateFlooring(length, width) {
  return length * width;
}
```

```javascript
let totalFlooring = 0;

totalFlooring = calculateFlooring(length,width);
```

现在我们可以在应用程序稍后使用此值。之前的示例没有使用返回的值。如果你以后不需要它，这始终是一个选项。

函数可以为我们做很多事情。它们为我们的代码提供了容器。然后我们可以调用它们并传递参数。此外，它们还可以返回数据。如果你在这里需要更多信息，这里是进一步的：

## JAVASCRIPT 条件语句

应用程序帮助我们做决策。基础决策是 `if` 条件。例如，如果披萨送餐员到达就开门。JavaScript像其他语言一样有很多条件语句，如 `if`。

`if` 语句以一个条件开始。如果条件为真，随后的语句将执行。

```javascript
if(pizzaArrives) {
  openTheDoor();
}
```

所以，如果 `pizzaArrives` 为真，我们就调用 `openTheDoor` 函数。我在 `if` 语句后面添加了大括号。这是可选的，但有助于可读性。省略大括号可能会导致你漏掉 Bug。所以请包含它们！

### if/else

有时你有两种不同的行动方案。我们可以在 `if` 的同时添加 `else` 语句。假设你正在煮一些汉堡。

```javascript
if(sideCooked) {
    flipBurger();
} else {
    keepCooking();
}
```

这个检查可以运行你最喜欢的汉堡店的烹饪机器人。不过它可能需要更多代码。如果你需要检查两个条件，你可以使用 `else if`。

```javascript
if(sideCooked) {
    flipBurger();
} else if(otherSideCooked) {
    removeFromGrill();
} else {
    keepCooking();
}
```

这给了我们检查额外值的选项。如果你需要更多检查，`switch` 语句可能效果更好。稍后会详细介绍这一点。

### 条件运算符

我们用于 `if` 语句的运算符必须解析为 `true` 或 `false`。这里有很多选项供你使用。根据经验，你需要测试这些内容并获得正确的那个。

```javascript
if(9>5) { alert("Greater than"); } // greater than
if(5<8) { alert("Less than"); } // less than
```

```javascript
if(9>=6) { alert("Greater than equal to"); } // greater equal to
if(4<=6) { alert("Less than equal to"); } // less equal to
if(4!=6) { alert("Not equal to"); } // not equal to
```

还有两个逻辑运算符。逻辑与 (`&&`) 和逻辑或 (`||`)。它们被频繁使用，但不要被吓到。

```javascript
const value1 = 4;
const value2 = -3;
```

```javascript
console.log(value1 > 0 && value2 > 0); // 预期输出: false
```

```javascript
console.log(value1 > 0 || value2 > 0); // 预期输出: true
```

逻辑与必须两个值都真才能解析为真。逻辑或只需要一个为真。

#### switch

`switch` 语句评估表达式以确定执行哪个语句。然后它会运行代码直到遇到 `break` 语句。这里有一个示例告诉我们你想要的鞋子的价格。

```javascript
const shoes = 'Reebok';

switch (shoes) {
  case 'Nike':
    console.log('Nike shoes are $200.');
    break;
  case 'Adidas':
  case 'Reebok':
    console.log('Adidas and Reebok are $100 a pair.');
    // 预期输出: "Adidas and Reebok are $100 a pair."
    break;
}
```

### 5

## JAVASCRIPT 循环

小时候，我们在农场上种了一排防风林。那排树每周需要浇几次水。打开水管给第一棵树水，数到十。移到第二棵树并重复。

就像生活一样，我们的计算机程序必须重复事情。这就是循环派上用场的地方。`for` 循环非常常见，让我们那里开始。

### for

如果我们有一个书籍数组并想打印它们。我们可以使用以下循环。

```javascript
for (let i = 0; i < books.length; i++) {
  text += books[i] + "";
}
```

`for` 循环有三个基本部分：开始 (Start)、条件 (Condition) 和步骤 (Step)。

#### start

这是我们设置循环变量的部分。在我们的示例中，我们通常将其初始化为 0。尽管你也可以设置为 10 然后递减。

#### condition

接下来是条件，我们在此处检查是否需要再次运行此循环。我们的示例检查是否还有更多书籍需要循环。如果我们完成了，就停止。

#### step

最后一部分是步骤。它告诉我们在每次迭代后发生了什么。我们的示例使用了自增运算符 (`++`)。这是正常的步骤，但我们也可以为特殊情况做其他事情。

#### while

如果我的狗 Baxter 想吃东西，我想创建一个循环，在它饿的时候喂它吃。`while` 循环可以做到这一点。这是一个示例。

```javascript
let baxterHungry = true;

while (baxterHungry) {
  console.log(feedBaxter);
  checkkBaxter();
}
```

我们将变量设置为 `true`。然后我们不断喂狗，直到它变为 `false`。`while` 循环会评估我们提供的条件。它需要被解析为 `true` 或 `false`。

如果是 `true`，循环内部的代码就会执行。我们会再次评估条件。一旦条件变为 `false`，循环就会停止。

#### do-while

`for` 和 `while` 循环先检查条件再运行代码语句。`do-while` 的不同之处在于它先运行代码然后再检查你的条件。它不常见，但在特殊情况下非常有用。

```javascript
let donutsEaten = 0;

do {
  console.log("Donuts eaten " + donutsEaten);
  donutsEaten++;
} while (donutsEaten < 5)

console.log("I'm full of Donuts!");
```

`do while` 会一直运行到条件为 `false`——这与我们讨论过的其他两种循环类型相反。输出看起来如下：

- Donuts eaten 0
- Donuts eaten 1
- Donuts eaten 2
- Donuts eaten 3
- Donuts eaten 4
- I'm full of Donuts!

当你需要循环执行代码时，JavaScript 为你提供了几种选择。像其他编程语言一样，它有 `for`、`while` 和 `do-while` 循环。只需确保它符合你的需求即可。

## JavaScript 变量作用域

我妻子切换话题很快。我开开玩笑说她需要转向灯，这样我就能跟上她转移的焦点。她正在聊晚餐，然后我们就转到了下一次度假。

### 作用域

我们的代码也有类似的作用域概念。变量可以快速进入或作用域。作为开发者，我们必须将这个概念放在核心位置。

在 JavaScript 中有几种不同类型的作用域。我们可以相应地使用它们。如果你做过其他编程，就会遇到过类似的概念。

#### 全局

全局作用域的项随处可见。在我们的示例中，我们在函数内部和外部创建了可见的变量。

```javascript
let myGlobalVariable = "TheBigGlobalVariable";
```

```javascript
function logOutGlobalVariable() {
    console.log(myGlobalVariable);
}

logOutGlobalVariable();
```

我打赌你在想，如果我在函数里添加一个变量呢？这让我们看到了局部作用域的示例。

#### 局部

局部变量仅在函数内部可见。这里有一个示例可以尝试一下。

```javascript
let myGlobalVariable = "TheBigGlobalVariable";

function logOutGlobalVariable() {
    console.log(myGlobalVariable);
    let localVariable = "TheLocalOne";
    console.log(localVariable);
}

logOutGlobalVariable();
```

```javascript
console.log(localVariable);
```

如果我们运行这段代码，在最后一行将会得到一个错误。

```javascript
console.log(localVariable);
// ReferenceError: localVariable is not defined
```

所以你可以看到当你不小心将变量放在错误位置时会发生什么。

#### 块

如果说局部作用域是在函数内部，那么块级作用域（block scope）则在大括号内部。有时你会创建大括号来标识某些代码。让我们来看看我的意思。

```javascript
console.log("here");

{
  let blockScopeVariable = 0;
  console.log(blockScopeVariable);
}

// 我们在此处无法引用 blockScopeVariable
```

```javascript
console.log(blockScopeVariable); // 无法工作
```

你可以看到，我们在大括号内创建了一个块级作用域变量。然后在外部，它将无法被引用。

#### 陷阱

作用域可能会令人困惑并导致一些错误。随着你 JavaScript 经验的增加，你可以尽早发现它们。例如，如果我们看这段代码片段：

```javascript
const colors = ['red', 'blue', 'white'];

for (let i = 0, l = colors.length; i < l; i++) {
  console.log(colors[i]); // 'red', 'blue', 'white'
}

console.log(l); // ???
console.log(i); // ???
```

变量 `i` 和 `l` 将导致引用错误。它们与我们之前的示例一样超出了作用域。Dmitry Pavlutin 更深入地解释了这一点。他还涵盖了我们在编码中可能犯的更多常见错误。

JavaScript 作用域有几个需要记住的基本原则。全局作用域随处可见。局部和块级作用域更集中。总体而言，你应该使用后者并避免前者。继续编码吧！

### 7

## JavaScript 闭包

在我的开发生涯中偶尔接触 JavaScript，闭包（Closures）是我不经常遇到的东西。它们有很大的价值。

### 闭包

我们如何定义闭包？嗯，这篇文章是这样定义的：“闭包是一种词法作用域（lexical scoping）的形式，用于在函数的内部作用域保留来自函数外部作用域的变量。”

```javascript
function outerFunction() {
  var x = 10;
  function innerFunction() {
    return x;
  }
  return innerFunction;
}

var inner = outerFunction();
```

```javascript
console.log(inner());
```

这是一个闭包的示例。外部函数 `outerFunction()` 创建了一个变量 `x` 和一个函数 `innerFunction()`。内部函数 `innerFunction()` 返回变量 `x` 的值。然后外部函数返回内部函数 `innerFunction()`。

接下来，内部函数 `innerFunction()` 被赋值给变量 `inner`。当调用变量 `inner` 时，它返回变量 `x` 的值，即使外部函数 `outerFunction()` 已经返回。

稍后我们可以涵盖词法作用域。首先，让我们理解为什么我们需要它们。以及一些缺点。

### 优缺点

闭包可以帮助隐藏封装细节。类似于 Java 的私有变量和函数，这允许我们控制访问。此的缺点是闭包占用更多内存。这些项无法被垃圾收集。最后，它可以减慢执行。Deepak Mankotia 更深入地探讨了这一点。

### 词法作用域

词法作用域术是指变量定义的位置。以及它是否可以被引用。

```javascript
let x = 10;

let myFunc = function () {
  let y = 20;
  console.log("x and y is accessible (outer):", x, y);
  let insideFunc = function () {
    let z = 30;
    console.log("x and y and z is accessible (inner):", x, y, z);
  }
  insideFunc();
  return;
}

myFunc();
```

```javascript
console.log("only x is accessible (global):", x);
```

延续我们之前的例子，我们有一个汽车对象和一个球的原始类型。前者可以改变，而后者不能。作为一名老牌 Java 程序员，这非常熟悉。

### 构造函数

可以使用构造函数创建对象。继续以汽车为主题，让我们创建两个汽车对象，这样你就能它的样子了。

```javascript
// Constructor function for Car objects
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
```

```javascript
// Create two Car objects
const myCar = new Car("Ford", "Pinto", "1971");
const yourCar = new Car("Dodge", "Charger", "1977");
```

它的工作原理与我们之前的示例类似。我们在这里使用 `function` 关键字来指定构造函数。此外，我们还使用 `new` 关键字来创建对象。

### 属性

我们创建了两个带有许多值的汽车对象。这些被称为属性。如果我们想将它们打印到日志中，可以这样做：

```javascript
console.log(myCar.make);
console.log(myCar.model);
```

这是访问值的一种方法。或者你也可以这样做：

```javascript
console.log(myCar["make"]);
console.log(myCar["model"]);
```

所以你有多种选项来获取底层数据。根据我的经验，前者的使用频率比后者更高。你的情况可能会有所不同。

### 方法

JavaScript 对象有一些内置方法。例如，其中之一是 `keys()` 方法。它将键转换为数组。

```javascript
// Initialize an object
const car = {
  make: 'Ford',
  model: 'Pinto',
  year: '1971'
};
```

```javascript
// Get the keys of the object
const keys = Object.keys(car);
```

```javascript
console.log(keys);
// outputs the following
["make", "model", "year"]
```

同样还有一个 `values()` 方法。

```javascript
// Initialize an object
const game = {
  id: 1,
  date: `23-March-2025`,
  teams: 'Panthers vs Jayhawks',
  location: 'St. Louis'
};
```

```javascript
// Get all values of the object
const values = Object.values(game);
console.log(values);
// outputs the following
[1, "23-March-2025", "Panthers vs Jayhawks", "St. Louis"]
```

这在配合循环遍历它们时非常有帮助。还有其他方法。这篇文章将回顾更多内置方法。

### this

JavaScript 将此保留为一个关键字。它被用于引用当前对象。它看起来像这样：

```javascript
// Create an object:
const car = {
  make: "Dodge",
  model: "Charger",
  year: "2015",
  carDetails : function() {
    return this.make + " " + this.model + " " + this.year;
  }
};
```

在这个示例中，我们创建了一个带有三个属性的对象。当我们想要显示详情时，可以调用 `carDetails` 函数。在这种情况下它将显示“Dodge Charger 2015”。

作为一个关键字，它不能用变量名。此外，我们不能改变 `this` 所指的值。`this` 在 JavaScript 中有三个上下文：函数、类和全局。我们在这些示例中共享了函数上下文。这里有更多信息。

JavaScript 对象与其他语言的对象相似。然而，它们也有几点不同。重要的是要记住 JavaScript 之初并不是这样的。它在不断地变化和适应。如果你了解基础知识，就可以很好地使用它。

## JAVASCRIPT 数组

我的妻子喜欢整理物品。她按年份将它们存放在信封里。JavaScript 数组类似于信封。我们可以在它们放入多个对象。

### JavaScript 数组

JavaScript 数组在一个集合中存储多个对象。它们还提供了一些常用操作。该集合可以包含多种数据类型，如字符串、数字、对象或其他数组。

### 创建

在 JavaScript 中创建数组有方法。

```javascript
const bread = ["white", "wheat", "sourdough"];
```

这是一个面包数组。我们在声明时设置值。

```javascript
const fruits = [];
fruits.push("banana", "apple", "peach");
```

先声明此数组，然后我们将水果推入数组中。

```javascript
const cars = new Array("Chevy", "Jaguar", "Porsche", "Fiat");
```

`new` 关键字可以像示例中那样使用。

```javascript
let arrOfManyTypes = ['abc', 1, 2, 3, true, 'xyz'];
```

数组也可以包含多种数据类型。我之前的示例具有相似的数据类型，但这一个包含字符串、数字和布尔值。

### 修改

我们可以使用内置方法修改数组。`toString()` 可以将其转换为字符串并打印。

```javascript
const bread = ["white", "wheat", "sourdough"];
```

```javascript
console.log(bread.toString()); // white,wheat,sourdough
```

`join` 方法也会提取元素元素，类似于 `toString()`。

```javascript
const bread = ["white", "wheat", "sourdough"];
```

```javascript
console.log(bread.join('-')); // white-wheat-sourdough
```

之前使用的 `push` 方法也可以修改数组。

```javascript
const fruits = [];
```

```javascript
fruits.push("banana", "apple", "peach");
```

`push` 方法将元素添加到数组的末尾。你还可以看到更多方法。

### 零基础索引

我不希望你错过 JavaScript 数组是从 0 开始索引的这一点。某些语言从 1 开始，而 JavaScript 在这方面表现像 Java。

```javascript
let tomsArray = [11, 22, 33, 44, 55];
console.log(tomsArray[0]); // prints 11
```

在这个示例中，如果我们想获取 33 的值，我们需要向数组传递值 2。这可能会在你的代码中产生 bug，所以请确保你理解了这一点。

否则，一旦你理解了这个事实，获取元素就很简单。使用你的方括号和正确的索引。然后你就可以访问数组中的任何元素了。

所以我们已经引起你对 JavaScript 数组的兴趣。你了解得更多了。我们讨论了如何创建和修改它们。编码愉快！

```javascript
let stringSingleQuote = 'Example using single quotes';
backTicksToo = `We can use back ticks`;
```

与我们的第一个示例类似，我们可以使用双引号。单引号和反引号也是合法的。

### Primitive类型 vs 对象

JavaScript 允许字符串是原始类型或对象。

```javascript
let primitiveString = "This is a primitive";
let objectString = new String("This is an object.");
```

第一个例子是原始类型，与之前的示例相似。第二个是一个对象。我们使用了 `new` 关键字和 `String` 构造函数。如果你想了解更多信息，可以查看 Flavio 的这篇文章。

### functions

在 JavaScript 中，我们可以在字符串上使用许多函数。我们可以查看几个。

### length

我们可以通过 `length` 函数获取字符串的长度。

```javascript
let sampleText = "A long time ago in a galaxy far far away...";
let length = sampleText.length;
```

这可以经常用于循环中。

### indexOf

`indexOf` 可以告诉我们单词或字母的位置。

```javascript
let sentence = "A quick brown fox jumped over the lazy dog.";
let foxIndex = sentence.indexOf("fox");
```

使用 `indexOf` 和 `slice` 函数可以帮助你拆分字符串。

### slice

如果你需要提取字符串的片段，`slice` 函数会非常有用。

```javascript
let animals = "Fox, Horse, Cow";
let farmAnimals = animals.slice(5);
```

我们取此字符串的最后两个单词并创建一个新字符串。

### Comparing

在 JavaScript 中比较字符串有两种类型：严格比较和松相等，它们之间有细微的。

```javascript
let str1 = "lowBasketball";
let str2 = "Basketball";
```

```javascript
console.log(str1 === str2); // false
```

这是一个严格比较的示例。

```javascript
let num1 = 23;
let num2 = '23';
```

```javascript
// 松相等
console.log(num1 == num2); // true
// 严格相等
console.log(num1 === num2); // false
```

在这里我们比较了两种类型。在松相等有效的情况下，严格相等则不生效。你也可以考虑 `localCompare`。

我们在这里只是触皮一角。我认为我们已经为你提供了关于 JavaScript 字符串的良好概述。从创建字符串到我们可以使用的函数，你已经了解了基本情况。作为作业，请花时间编写字符串代码并完善你的理解。

你买过均码的衬衫吗？对于我们中的一些来说，它看起来像是一件大号的睡衣。而对其他人来说看起来像中码。

JavaScript 只有一种数字供我们使用。所以我们不需要像在 Java或其他语言那样学习多种类型。你可以让自己困惑。

## JavaScript Number

所以在 JavaScript 中我们可以可以做这样的操作。

```javascript
let num1 = 1.234;      // 带小数的数字
let num2 = 5;           // 不带小数的数字
```

我们可以使用小数，也可以使用整数。

```javascript
let bigNum = 423e6;      // 423000000
let smallNum = 552e-5;   // 0.00552
```

当数字很大时，我们也可以使用科学计数法。这两个例子向我们展示了如何。

### Number()

我们也可以用数字构造函数来创建。

```javascript
Number(999);
Number("999");
```

这两个示例都创建了一个数字。我们可以传递字符串或数字。

```javascript
Number(true); // 1
Number(false); // 0
Number(new Date()); // 1712747922911
Number("s:"); // NaN
```

在这些示例中，你可以看到 `true` 和 `false` 解析为数字。日期也被转换为数字。然而，字母无法解析为数字。因此，它打印 `"NaN"`。代表 Not a Number（不是数字），参考指南提供了更多信息。

### Precision

JavaScript 数字是 64 位浮点数。它遵循 IEEE 754 标准。整数可以精确到 15 位。

```javascript
let num = 123456789012345;
```

最大小数位数是 18 位。

```javascript
let dec = 0.123456789012345678;
```

### Methods

JavaScript 为数字提供了很多方法。我在这里提到几个。

```javascript
const num = Math.PI.toFixed(2);
console.log(num); // 3.14
```

`toFixed` 方法会将数字舍入到指定的位数。我们在这里也使用了 `Math.PI` 常数。其他 Math 常数在-中详细介绍。

```javascript
const num = Math.PI.toPrecision(6);
console.log(num); // 3.14159
```

`toPrecision` 方法将给我们我们请求的数字。所以如果你需要设置显示多少位有效数字，这会对你很有用。

在处理 JavaScript 数字时有很多选项。虽然这是一种通用的方法，但它是有效的。测试一下极限吧。

```javascript
console.log(0 !== false);
//Example 4: Expected output: true
```

事实胜于言，作为开发者，我们喜欢看到代码。这些示例向我们展示了发生了什么。当你开始使用严格运算符时，请测试你的代码。注意边界情况。你可能潜藏着一些 Bug。

## 严格与松散 (Strict vs Loose)

最后，让我们比较严格与松散。只需三个变量我们就可以探索一些关键区别。

```javascript
const zero = 0;
const zeroObj = new String("0");
const zeroStr = "0";
```

```javascript
console.log(zero === zeroObj); // false
console.log(zero == zeroObj); // true
```

```javascript
console.log(zero === zeroStr); // false
console.log(zero == zeroStr); // true
```

```javascript
console.log(zeroObj === zeroStr); // false
console.log(zeroObj == zeroStr); // true
```

我们有数字、字符串和对象形式的零。你可以看到两种相等性类型之间的巨大差异。因如此，许多开发者建议不要使用松散相等。它可能导致某些难以诊断的 Bug。

在编写 JavaScript 时，确保你理解严格相等和松散相等。如果你有疑问，请回顾这段关于严格、松散或普通等等的详尽解释。了解我在这里犯过的错误是有价值的而且非常有帮助。

## JavaScript 对象表示 (JAVASCRIPT OBJECT NOTATION)

开发者在几乎做的每件事中都使用数据。我们与许多类型的数据交互，从数据库或 XML 到 JSON。JavaScript 结合得很好，因为这就是它的初衷。

### 什么是 JSON？

根据他们的定义，它是这样的：

JSON（JavaScript 对象表示法）是一种轻量的数据交换格式。它易于人类读写，易于机器解析和生成。

XML 更加重量级且并不易于人类阅读，而 JSON 试图扭转这一点。当然，我们可以由你来决定。这是一个示例：

```json
{"developer":"Tom", "linesCode": 12000, "repo":"accounting", "ide": null}
```

这个对象有几个属性：Developer、代码行、repo 和 ide。基本结构是键值对。如果我们想在 JavaScript 中访问这些属性，可以进行以下操作。

```javascript
let developer = obj.developer;
let linesOfCode = obj.linesOfCode;
let repository = obj.repo;
```

在这里我们可以用 JavaScript 轻松地访问对象中的属性。我们涵盖了基础知识，现在来比较 JSON 和 XML。

### JSON vs XML

这两种类型的数据可以用很多地方。如果我们看一些类似的示例，可以对它们进行面对面的比较。我们可以在两者中创建一个客户数组。

```json
{"customers":[
  { "business":"ABC Inc.",
    "city":"Ducktown"
  },
  { "business":"Delta LTD",
    "city":"Jimmyville"
  },
  { "business":"XYZ Company",
    "city":"New Heights"
  }
]}
```

XML 中的标签可以使内容更冗长。JSON 也让内容变得短了一些。大多数编程语言都可以通过适当的库处理其中一种。

### 用途 (Uses)

JSON 主要用于表示调用 API 的数据。许多开发者比起 XML 更喜欢它，因为它是轻量级的。此外，它是语言无关的，所以你可以与大多数语言一起使用。这是一个用 JSON 调用 API 的示例：

```json
[
  {"command" : "ServerInfoService.getVersion"},
  {"command" : "Examples.echo","args" :{"echo" : "Some text."}}
]
```

服务可能会返回如下响应：

```json
[{
  "result" : {
    "version" : "9.0.9000"
  },
  "result" : {
    "echo" : "Some text."
  }
}]
```

我们在 SmartBear 的朋友对此更深入地描述了这一点。这个简单的示例让你对调用 API 或 Web 服务有一个基本的理解。

在处理 JavaScript 时，你会遇到 JSON。这种轻量级的数据格式很容易使用。它与 XML 相比具有一些明显的优势。曾经 AJAX 更常见，而今天大多数 Web 应用都使用 JSON。

## JavaScript 展开与剩余运算符 (JAVASCRIPT SPREAD AND REST OPERATOR)

小时候，我会拆解东西。我的手表、收音机，任何我能拿到的东西。我仍然对事物如何运作感到好奇。尽管我现在尽量不再弄坏东西了。

俄罗斯套娃可能具有挑战性。每一个新的里面都有另一个。JavaScript 有类似的机制。展开运算符可以帮助我们拆解数组或字符串。

### 展开运算符 (Spread Operator)

JavaScript 中的展开运算符是 `(...)`，用于允许数组展开为独立的元素。

```javascript
let numbers = [1,2,3,4,5];
let maximum = Math.max(...numbers);
let minimum = Math.min(...numbers);
console.log(maximum); // 5
console.log(minimum); // 1
```

在这里我们配合 Math运算符使用它来获取数组的最大值和最小值。这只是展开运算符的一个方便用法。

```javascript
const policeSongs = ["King of Pain", "Wrapped Around Your Finger"];
```

```javascript
const stingSongs = ["Fields of Gold", ...policeSongs, "Desert Rose"];
```

```javascript
console.log(stingSongs); // ["Fields of Gold","King of Pain","Wrapped Around Your Finger","Desert Rose"];
```

如果你需要混合数组，展开运算符也可以做到。当你修改并向数组中添加元素时，这会非常有用。

### 剩余运算符 (Rest Operator)

剩余运算符允许函数处理不同配置的参数。它可以帮助设置数组或重构对象。

```javascript
function total(...num) {
  let tot = 0;
  for (const n of num) {
    tot += n;
  }
  return tot;
}
console.log(total(11, 22, 33, 44)); // 110
```

这个 `total` 函数可以处理传递给它的多个参数。剩余运算符启用了该选项。

## 对象解构 (Object Destructuring)

如果你有一个数组，你可能需要解包这些部分。为了做到这一点，你可以使用对象。

```javascript
const atariGames = ['Pitfall', 'Space Invaders', 'E.T.'];
```

```javascript
const [great, good, awful] = atariGames;
```

这会将三个 Atari 游戏中的每一个赋值给单独的对象。如果有必要，你可以跳过一个并留空，如下：

```javascript
const atariGames = ['Pitfall', 'Space Invaders', 'E.T.'];
```

```javascript
const [great, , awful] = atariGames;
```

在这种情况下，我们只使用第一个和最后一个游戏。JavaScript 提供了很多工具来处理数组。展开和剩余运算符可以进行一些切分处理。然后你可以使用对象解构将它们拆开。如果你了解你的工具，你可以做任何你想做的事。

# 第三部分 (PART THREE)

这一部分涵盖了更高级的主题。例如执行上下文、调用栈、变量作用域和作用域链。每个部分都为你提供了 JavaScript 拼图的碎片。

## JavaScript Promise.all() (JAVASCRIPT PROMISE.ALL())

如果你从未处理过异步任务，这可能会很有趣。它类似于告诉某人去给你买咖啡，然后继续其他工作。这些函数非常强大，但我们需要理解如何使用它们。

### Promise.all()

`Promise.all()` 是一个静态方法。它接收一个可迭代的 Promise。这意味着什么？一个示例可以是完成值或任务的数组。代码示例可能会有所帮助。

```javascript
const promiseA = Promise.resolve("Tom");
const promiseB = 2024;
const promiseC = new Promise((resolve, reject) => {
  setTimeout(resolve, 100, 'foo');
});

Promise.all([promiseA, promiseB, promiseC]).then((values) => {
  console.log(values);
});
```

所有这些代码将输出以下。

#### 用例 (Use Case)

`Promise.all()` 用法的一个主要用例是调用一系列异步 API。一旦它们都响应，你可以将所有响应放入一个数组中。例如，你可能需要在多个社交媒体平台上发布内容。一旦它们都响应，你就可以查看是否成功。

### Promise.allSettled()

类似于 `Promise.all()` 有 `Promise.allSettled()`。它也接收一个可迭代的 Promise。它在所有 Promise 都已决后返回。

```javascript
const promise1 = Promise.resolve(3);
const promise2 = new Promise((resolve, reject) => {
  setTimeout(reject, 100, 'foo');
});
const promises = [promise1, promise2];

Promise.allSettled(promises).then((results) =>
  results.forEach((result) => console.log(result.status)),
);
```

### all() vs allSettled()

如果我们使用 `Promise.all()` 并调用三个 Promise，当其中一个被拒绝时，它们全部被拒绝。`Promise.allSettled()` 则会分别解析或拒绝它们。因如此，你需要在选择一个之前了解需要什么。

所以再次重申一下，如果你使用 `Promise.all()`，一旦其中一个 Promise 被拒绝，它就会被拒绝。而 `Promise.allSettled()` 永远不会被拒绝，它会解析或拒绝数组中的每一个 Promise。

结论是，JavaScript 的异步工作是有帮助的。`Promise.all()` 和 `Promise.allSettled()` 可以解决某些问题。请回顾你的用例并选择合适的一个。

# 执行上下文与调用栈

当我们执行 JavaScript 代码时，代码会被经过编译的。然后，它会创建一个全局执行上下文。我们可以通过这段代码看到这一点。

```javascript
const name = 'Tom';

const primary = () => {
  let x = 1;
  const y = secondary();
  x = x + y;
  return x;
}

function secondary() {
  var z = 2;
  return z;
}
```

最初，`name`、`primary` 和 `secondary` 被加载。这些是顶层代码。函数体只在被调用时才会执行，而这一切都发生在执行上下文（Execution Context）中。

## 执行上下文

它被定义为执行 JavaScript 代码的环境。在这个空间内，它存储了代码执行所需的所有信息。将其想象成你 JavaScript 代码的容器。就像啤酒装在瓶里一样。

### 全局执行上下文

始终有一个全局执行上下文，用于存放顶层代码。这些是不在函数内的代码。它是你 JavaScript 代码的默认上下文。

一旦顶层代码完成，函数和回调就会开始执行。每个函数都有一个执行上下文。对于每次函数调用，都会创建一个新的上下文。

### 内部

执行上下文内部是变量环境（Variable Environment）。用 `var` 声明的变量在其中，函数和 `arguments` 对象也在其中。作用域链（Scope Chain）也是一部分。它是对当前上下文外部变量的引用。`this` 关键字也是其中的。这一切都是创建阶段的一部分，该阶段发生在执行之前。

### 变量环境

作用域链

`this` 关键字

## 箭头函数说明

箭头函数不会获取 `arguments` 对象或 `this` 关键字。它们可以使用其最近的普通函数父级中的 `arguments` 对象和 `this` 关键字。在使用箭头函数时，不要让这个细节困扰你。

### 创建

让我们回到之前的例子。当我们观察这段代码块时，我们需要看到三个不同的执行上下文被创建。

```javascript
const name = 'Tom';

const primary = () => {
  let x = 1;
  const y = secondary();
  x = x + y;
  return x;
}

function secondary() {
  var z = 2;
  return z;
}
```

在全局执行上下文中，有一个 `name` 变量，然后是对 `primary` 和 `secondary` 函数的引用。此外，每个函数都获得一个执行上下文。`primary` 有一个已的 x 值，而在运行 `secondary` 函数之前，`y` 的值是未知的。

### 调用栈

调用栈（Call Stack）和内存堆（Memory Heap）组成了 JavaScript 引擎。调用栈是执行上下文堆叠的地方。这有助于系统跟踪我们在执行中的位置。当前的执行上下文位于顶部。

在我们的示例代码中，它首先创建全局执行上下文。然后当调用 `primary` 函数时，它会创建它的上下文，然后该上下文将位于调用栈顶部。如你所见，`primary` 函数调用了 `secondary`。此时，它为 `secondary` 创建了第三个上下文。调用栈顶部是 `secondary`，中间是 `primary`底部是全局。把它想象成一个巨麦当！

## 作用域与作用域链

在 JavaScript 中理解的两个重要概念是作用域（Scope）和作用域链（Scope Chain）。我们一直在处理这两个概念，但还没有真正的解释。现在让我们解释一下它们，以便你了解它们的作用。

### 作用域

在我们的代码中，变量并不总是可访问的。作用域是我们能够访问它们的区域。当我们无法访问它们时，我们说“它们超出了作用域”。让我们看一些代码来直观理解。

```javascript
{
  let scopeExample = 2222;
}
// 这里无法使用 scopeExample
```

我们在括号中声明了一个变量。一旦离开括号，该变量就超出了作用域。你在循环中经常看到这一点。这是一个块作用域的例子。注意，块作用域（block scope）是在 ES6 中添加的。块作用域变量用 `let` 和 `const` 创建。用 `var` 声明变量用于函数作用域。记住 `var` 最初就在 JavaScript 中。另外两个是后来添加的。

让我们看看全局作用域是什么。

```javascript
let globalVar = 93; // 在全局作用域中声明
```

```javascript
function myFunction() {
    console.log(globalVar); // 在内部访问全局变量
}
```

```javascript
myFunction(); // 输出: 93
```

我们创建了全局变量，然后在函数内部引用了它。现在我们可以用函数作用域来封装它。

```javascript
var sport = "tennis"; // 全局
```

```javascript
function changeSport() {
    var sport = "racquetball"; // 局域
    console.log(sport);
}
```

```javascript
console.log(sport);
changeSport();
```

```javascript
console.log(sport);
```

你知道输出会是什么吗？答案在这里。

所以，一旦我们离开函数，变量就超出了作用域。我们从壁球回到了网球。

### 作用域链

当我们在 JavaScript 中引用变量时，它将向上查找作用域链来寻找。例如，我们的函数作用域示例有两个 `sport` 变量。一个在函数内，一个在全局。

```javascript
let globalVar = 10; // 全局作用域
```

```javascript
function outer() {
  let outerFuncVar = 20; // 外部函数作用域
```

```javascript
function inner() {
  let innerFuncVar = 30; // 内部函数作用域
  console.log(globalVar); // 访问全局变量
  console.log(outerFuncVar); // 访问外部作用域的变量
  console.log(innerFuncVar); // 访问局部变量
  inner();
}

outer();
```

在这个例子中，你可以看到作用域链的使用。随着代码的执行，`console.log` 语句访问变量中的值。它打印出：

### 词法作用域

JavaScript 还有词法作用域（Lexical Scope），它指的是根据源代码中的位置来如何访问变量和函数。

```javascript
const vGlobal = "Global";

function outerFunc() {
  const vOuter = "Outer";

  function innerFunc() {
    const vInner = "Inner";
    console.log(vGlobal);
    console.log(vOuter);
    console.log(vInner);
  }

  innerFunc();
  console.log(vInner);
}

outerFunc();
console.log(vOuter);
```

在这个例子中，我们看到了词法作用域的几个不同示例。具有两个不同的函数和一个全局变量。当我们运行代码时，我们看到这个：

```
ReferenceError: vInner is not defined
at outerFunc (<anonymous>:19:15)
at <anonymous>:22:1
at mn (<anonymous>:16:5455)
```

全局变量随处可访问。外部变量在外部函数和内部函数中都是可访问的，因为它是嵌套的。内部变量只在内部函数中可访问。总结一下，内部函数可以访问在外部作用域声明的变量。反之则不然。外部函数无法访问在内部作用域声明的变量。

TDZ（暂时性死区）。如果你在声明之前使用它，将会得到错误。它们是块级作用的。因此它们只存在于块中。

### 暂时性死区

为了更好地理解暂时性死区或 TDZ，让我们来看一下。

```javascript
const car = 'Honda';

if (car === 'Honda') {
  console.log(`Car is a ${model}`); // Error
  const years = 2024 - 2012;
  console.log(years);
  const model = 'Accord';
  console.log(`Car is a ${model}`);
}
```

在这个示例中，`model` 变量在定义之前就被使用了。因此，在它声明之前，它处于暂时性死区。该引用将导致引用错误（Reference Error）。一旦它初始化，就可以安全使用了。TDZ 是在 ES6 中引入的以避免其他问题。

大多数编程语言都有 Map（映射）。由于我使用 Java 很多年，我已经习惯了它的用处。JavaScript 起初并没有它们。它们是在 ES6 或 ECMAScript 中引入的。

Map 是一种将值映射到键的数据结构。类似于对象，但对象的键始终是字符串。在 Map 中，我们可以拥有任何类型的键。它可以是一个对象、数组或其他另一个 Map。

### 声明

声明一个 Map 类似于 Set（集合）。当然，我们还需要添加键。

```javascript
const coffeeShops = new Map();

coffeeShops.set(1,"Starbucks Main Street");
coffeeShops.set(2,"Starbucks Clinton Avenue");
coffeeShops.set(3,"Dunkin Donuts - First Ave");

console.log(coffeeShops);
```

在这种情况下，我只是将键设为了整数。在 Map 中，我也可以使用其他内容作为键。运行这段代码将会得到这条消息。

也可以像下面这样对 `set` 方法进行链式调用。

```javascript
const coffeeShops = new Map();

coffeeShops.set(1,"Starbucks Main Street");
coffeeShops.set(2,"Starbucks Clinton Avenue");
coffeeShops.set(3,"Dunkin Donuts - First Ave").set(4, "Tom's Coffee House");
coffeeShops.set(5,"Central Perk");

console.log(coffeeShops);
```

这样很很好，我们可以声明一个 map 并存入数据。但如果我们想从 map 中检索数据呢？

### 获取

要从 map 中获取数据，我们可以使用 `get` 方法。你只需要使用键值来检索它即可。

```javascript
const coffeeShops = new Map();

coffeeShops.set(1,"Starbucks Main Street");
coffeeShops.set(2,"Starbucks Clinton Avenue");
coffeeShops.set(3,"Dunkin Donuts - First Ave").set(4, "Tom's Coffee House");
coffeeShops.set(5,"Central Perk");

console.log(coffeeShops.get(4));
```

当我们运行它时，我们得到了键为 4 的值。

重要的是，键的数据类型是有重要的。所以如果我把 4 改为字符串，它将无法工作。

```javascript
const coffeeShops = new Map();

coffeeShops.set(1,"Starbucks Main Street");
coffeeShops.set(2,"Starbucks Clinton Avenue");
coffeeShops.set(3,"Dunkin Donuts - First Ave").set(4, "Tom's Coffee House");
coffeeShops.set(5,"Central Perk");

console.log(coffeeShops.get('4'));
```

虽然我们没有得到错误，但它返回的是 `undefined`。

所以请注意数据类型，否则你可能会错过什么。并不是说我永远不会犯错误 :)

### 删除

发生了一些事情，我们需要从 map 中移除某些东西。例如，我必须关闭我的咖啡店。

```javascript
const coffeeShops = new Map();

coffeeShops.set(1,"Starbucks Main Street");
coffeeShops.set(2,"Starbucks Clinton Avenue");
coffeeShops.set(3,"Dunkin Donuts - First Ave").set(4, "Tom's Coffee House");
coffeeShops.set(5,"Central Perk");

coffeeShops.delete(4);

console.log(coffeeShops);
```

然后输出被更新了。

```
Map(4) {1: "Starbucks Main Street", 2: "Starbucks Clinton Avenue", 3: "Dunkin Donuts - First Ave", 5: "Central Perk"}
```

现在 map 只剩下四个元素。

### 大小

我们通过 `size` 方法获取 map 的大小。在你添加和删除元素时，这很有帮助。

```javascript
const coffeeShops = new Map();

coffeeShops.set(1,"Starbucks Main Street");
coffeeShops.set(2,"Starbucks Clinton Avenue");
coffeeShops.set(3,"Dunkin Donuts - First Ave").set(4, "Tom's Coffee House");
coffeeShops.set(5,"Central Perk");

console.log(coffeeShops.size);
```

所以当你运行它时，你会看到输出为 5。

### 清空

你也可以使用 `clear` 方法清空 map 中的所有内容。

```javascript
const coffeeShops = new Map();

coffeeShops.set(1,"Starbucks Main Street");
coffeeShops.set(2,"Starbucks Clinton Avenue");
coffeeShops.set(3,"Dunkin Donuts - First Ave").set(4, "Tom's Coffee House");
coffeeShops.set(5,"Central Perk");

console.log(coffeeShops.size);

coffeeShops.clear();

console.log(coffeeShops.size);
```

当你运行时，你会先是 5，然后是 0。

### 对象作为键

可能会有某时刻，你需要创建一个以对象作为键的 map。

```javascript
const numArr = [2,4];
const numMap = new Map();

numMap.set(numArr,"value");

console.log(numMap.get(numArr));
```

当我们运行它时，注意第二种场景下的输出。我们可以使用 `numArr` 的元素。

Map 可以为你做很多事情。花时间掌握它们吧。在我职业生涯早期，我对 JavaScript 随着这些功能而取得的进展感到惊讶。

## JAVASCRIPT SETS（集合）

学习编程的一部分是了解你的选择。一组东西可以用几种方式存储。Set 被引入了。一个 Set 是一个唯一值的集合，它们永远不会有重复项。使用它们可能非常方便。

### 声明

在 JavaScript 中声明一个 set 非常简单。这是一个汽车的集合：

```javascript
const cars = new Set(["Ford", "Chevy", "Honda"]);
```

我们有三个元素。如果我们两次放入同一个值呢？

### 重复项

Set 会为你处理重复项。它会移除重复的值。这里有一个我们添加了两次 Ford 的示例。

```javascript
const cars = new Set(["Ford", "Chevy", "Honda", "Ford"]);
console.log(cars);
```

你认为这会打印什么？四个还是三个？让我们来看看吧。

### 大小

我们可以这样获取 set 的大小：

```javascript
const runningShoes = new Set(["Nike", "Asics", "Hoka"]);
console.log("set of running shoes has " + runningShoes.size + " elements.");
```

输出看起来是这样的：

```
set of running shoes has 3 elements.
```

注意 `size` 用于 sets，而 `length` 用于数组。这可能会让人混淆。

### 检查

当我们想检查 set 中的某个元素时，可以使用 `has` 方法。

```javascript
const taxYears = new Set([2023, 2024, 2025]);
console.log(taxYears.has(2025));
console.log(taxYears.has(2015));
```

这里有一个代表年份的集合。使用 `has` 方法检查我们的 set 是否包含这些年份。这是我们的输出。

`has` 方法类似于数组的 `includes` 方法。

### 删除

如果你需要从 set 中移除一个元素，可以使用 `delete` 方法。

```javascript
const taxYears = new Set([2023, 2024, 2025]);
console.log(taxYears);

taxYears.delete(2025);

console.log(taxYears);
```

当我们运行它时，我们看到：

### 清空

如果你需要删除 set 中的所有元素，可以使用 `clear` 方法。

```javascript
const taxYears = new Set([2023, 2024, 2025]);
console.log(taxYears);

taxYears.clear();

console.log(taxYears);
```

我打赌你能猜出发生了什么。当然，使用它要小心。一旦消失了就消失了。

### 遍历

你可以遍历一个 set。我们可以使用 `for` 循环来实现。

```javascript
const nbaLegends = new Set(["Michael Jordan", "Jerry West"]);

for (let legend of nbaLegends) {
  console.log(legend);
}
```

```javascript
"Julius Erving";

for (const legends of nbaLegends) {
  console.log(legends);
}
```

这段代码将产生以下输出。

集合（Sets）并不是为了替代数组（Arrays）。如果你需要保持顺序或保留重复项，集合将无法满足。在选择集合之前，理解其使用场景至关重要。此外，如果你需要操作数据，数组是更好的选择。

## JAVASCRIPT 的 CALL, BIND 和 APPLY

你是否曾经和某人交谈，当他们在讨论多个人时却一直使用代词？她是谁？是 Donna 还是 Kate？我们努力努力跟上思路，但可能会感到困惑。

### Call 方法

在 JavaScript 中也会发生类似的情况。使用 `this` 关键字可能会让计算机感到困惑！我们可以使用 `call` 方法来指明我们指的是谁。让我们来看一个例子。

```javascript
const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};

const person1 = {
  firstName: "Tom",
  lastName: "Henricksen"
};
```

```javascript
console.log(person.fullName.call(person1));
```

在这个例子中，我们没有使用 `call` 方法。这里的输出将是“Tom Henricksen”。

```javascript
const person = {
  fullName: function(city, state) {
    return this.firstName + " " + this.lastName + ", " +
    city + ", " + state;
  }
}

const person1 = {
  firstName: "Tom",
  lastName: "Henricksen"
};

console.log(person.fullName.call(person1, "Newtown", "Pennsylvania"));
```

在这个例子中，我们使用了 `call` 方法，它提供了更多信息。这里的输出将是“Tom Henricksen, Newtown, Pennsylvania”。

### Bind 方法

使用 `bind` 方法，你可以创建一个新函数，该函数通过传递的参数设置 `this` 关键字。

```javascript
const person = {
  firstName: "Tom",
  lastName: "Henricksen",
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}

const brother = {
  firstName: "John",
  lastName: "Henricksen"
};
```

```javascript
let fullName = person.fullName.bind(brother);
console.log(fullName());
```

在这个例子中，`brother` 对象从 `person` 对象借用了 `fullName` 方法。

如果你需要调用另一个函数并提供上下文参数，`apply` 可能会有效。

### Apply

让我们使用之前的例子来展示 `apply` 函数如何为你服务。

```javascript
const person = {
  fullName: function(city, state) {
    return this.firstName + " " + this.lastName + ", " + city + ", " + state;
  }
};

const brother = {
  firstName: "John",
  lastName: "Henrickson"
};

console.log(person.fullName.apply(brother, ["Phoenix","Arizona"]));
```

当我们运行它时，会看到以下输出。

这三种方法可以帮助你有效地使用 `this` 关键字。随着你学习和编写更多的 JavaScript 代码，你将发现利用它们的方法。将它们加入你的工具箱，它们将会非常用用。

24

# DOM

> “所有模型都是错误的，但某些模型是有用的” - George E. P. Box

在软件世界中，这是非常正确的。在处理 HTML 时，我们需要一个模型来帮助我们理解元素所在。这就是 DOM 的引入。

# DOM

为了操作网页界面，我们可以使用文档对象模型（Document Object Model，DOM）。这可能是一个需要更改的 HTML 页面。我们可以使用 JavaScript 实现此，尽管其他语言也可以做到。

```javascript
querySelector()
```

```html
<html lang="en">
```

```html
<id="header">
```

我们在这个 HTML 页面中设置了一些部分来访问 DOM。我们也导入了 JavaScript 代码。

```javascript
const message = 'Tom was here!'

// 更新 header 文字
document.querySelector('#header').innerHTML = message

// 打印到控制台
console.log(message)
```

这里是 JavaScript 代码的内容。我们将消息设置到了 header 中。

这是浏览器中的 HTML 页面。

```text
Tom was here!
```

输出也被发送到了控制台。你可以在这里看到。`document` 对象代表网页。我们使用 `querySelector` 查找页面上的元素。我们通过 `innerHTML` 属性修改内容。

```javascript
getElementById()
```

另一种实现的方法是使用 `getElementById` 方法，它返回该元素。

```html
<html>
```

## getElementById 方法

```html
<id="tag">
```

在这里我们用 `getElementById` 替换 `querySelector`。然后我们再次使用 `innerHTML` 属性。

```javascript
addEventListener()
```

## addEventListener 方法

```html
<html>
```

我们也可以给表单添加事件监听器。我们需要向 document 注册。

## addEventListener 方法

```html
<id="p-id">
```

当我们注册时，告诉 document 在被点击时调用该方法。

```text
You clicked!!
```

这里是输出，由于我点击了页面，消息被打印了出来。这些只是使用 DOM 的三个例子。你可以做的其他操作包括删除和添加元素。当用户填写表单时，你可以显示或隐藏信息。还可以处理页面上的系列元素。当有许多字段需要显示时，这非常有帮助。在医疗行业这种情况经常发生。

# 作者

Tom Henricksen是一位解决问题的技术专家。他是 Code is Easy 的演讲者和作家。从开发者开始，他担任过项目经理、技术主管、Scrum Master 和软件开发经理。

Tom 曾帮助组织进行敏捷转型。他还为团队和个人提供过教练和培训。

Tom 还是创业者。他以技术角色为核心进行演讲和写作。Tom 是 Agile Online Summit 和 DevOps Online Summit 的创始人，在那里他建立了一个超过 5000 人的强大在线社区。

Tom 学习了如何解决挑战性的技术问题并领导技术团队。他也可以帮助你这些这些技能！你可以通过以下方式与我联系：

- http://codeiseasy.co
- https://x.com/TomHenricksen
- https://www.linkedin.com/in/tomhenricksen

订阅我的 newsletter：

- https://t.co/NkolrQgXHM

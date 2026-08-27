
# 引言

JavaScript 是一种遵循 ECMAScript 规范的卓越且成熟的编程语言。该编程语言由强类型系统、大括号语法、高质量函数和基于原型的面向对象组成。配合 HTML 和 CSS，JavaScript 是万维网的重要技术之一。JavaScript 促进了可交互网页的实现，是 Web 应用的关键组成部分。几乎每个网站都使用 JavaScript，所有主要的网页浏览器都包含 JavaScript 引擎以确保正常运行。Brendan Eich 在 1995 年于 Netscape Communications 时开发了 JavaScript。JavaScript 有助于功能型、事件驱动、基于原型和面向对象的编程风格。JavaScript 通过确认用户在客户端执行的操作来升级 Web 用户界面。你可以将 JavaScript 引擎插入不同类型的主机软件中，包括数据库、Web 服务器以及非网络相关的程序（如文字处理器）。

本书将进一步解释 JavaScript 的概念，旨在帮助你在没有压力的情况下学习和理解 JavaScript 语言。学习 JavaScript 需要 HTML、文本编辑器、网页浏览器和 CSS 知识。要开始学习，必要的工具之一是文本编辑器，它是编写代码所需的。你还需要一个浏览器来查看开发的网页。有不同类型的文本编辑器，如 Sublime Text、Notepad++，以及如 Firefox、Google Chrome 等浏览器。

# 第 1 章：什么是 JavaScript

JavaScript 简称为 JS，是一种用于为网页添加特定程序的高级编程语言，已被所有主流网页浏览器采用。JavaScript 可用于构建交互式 Web 应用，使其在无需每次操作都重新加载页面的情况下正常运行。JavaScript 用于在网页内创建不同形式的活动，是万维网的核心组件之一。HTML（Hypertext Language 超文本标记语言）和 CSS（Cascading Style Sheets 级联样式表）是其组成部分。JavaScript 通过确认用户在客户端执行的操作来升级 Web 用户界面。你可以将 JavaScript 引擎插入不同类型的主机软件中，包括数据库、Web 服务器以及非网络相关的程序（如文字处理器）。

### 解决方案

头部部分的脚本是 `<head> </head>`。

主体部分的脚本是 `<body></body>`。

主体内部的脚本是 `<body></body>` 和 `<head> </head>`。

在 `<head>...</head>` 中包含外部文件脚本的脚本。

## 第 2 章：值、类型和运算符

在计算机世界中，存在数据。你可以创建新数据、读取数据和更改数据，它们都被存储为一系列看似连续的位（bits）。将位定义为接收强或弱信号、以及来自计算机内部高或低电荷的 0 和 1。所有数据和信息片段都被描述为 0 和 1 的序列，并用位表示。

### 值

深吸一口气，想象一片比特海洋。最新的 PC 在数据存储中包含超过 300 亿个位。我们使用位来创建值。计算机能够正常运行，是因为每一位信息都被拆分成了值。每个值由一个影响其角色的类型组成，值可以是数字、文本或函数等。要生成值，你需要调用它的名称，它会从存储的地方出现。

### 算术

算术是处理数字的主要任务。对多个数字进行乘法、加法和减法产生另一个数字的操作称为算术运算。以下是在 JavaScript 中的示例：

```javascript
100 + 4 * 11
```

`+` 和 `*` 符号被称为运算符，第一个表示加法，另一个表示乘法。在两个值之间插入运算符将产生另一个值。`-` 运算符用于减法，`/` 运算符用于除法。如果运算符在没有括号的情况下一起出现，运算符的优先级决定了它们的应用方式。如果几个优先级相同的运算符相邻出现（如 `1 - 2 + 1`），则从左到右应用：`(1 - 2) + 1`。

### 特殊数字

JavaScript 由三个唯一值组成，它们行为不像数字但被视为数字。`Infinity`（无穷）和 `-Infinity`（负无穷）是前两个，代表正无穷和负无穷，最后一个值是 `NaN`。`NaN` 表示“不是数字”，尽管它是一个数字类型的值。

### 字符串

字符串是数字的序列。字符串是下一个数据类型，它们代表文本。字符串将其内容限制在引号中。

> `Down the walkway path.`

> "On top of the roof."

> 'I am at home.'

使用不同类型的引号（如双引号、单引号或反引号）来标记字符串。字符串必须匹配至关重要。引号内的元素由 JavaScript 创建一个字符串值。JavaScript 使用 Unicode 标准为每个需要的字符分配数字，包括阿拉伯语、亚美尼亚语、日语等。你不能对字符串进行减法、乘法或除法，但你可以使用 `+` 运算符，它不是相加而是将两个字符串拼接在一起。拼接意味着将字符串胶在一起。

### 一元运算符

符号并不代表所有的运算符。你可以用单词写出一些运算符。一个清晰的例子是某种类型的运算符，这个运算符创建一个带有 `typeof console.log` 名称的字符串值：`console.log(typeof 4.5)`

```javascript
// -> number
console.log(typeof "x")
// -> string
```

第二个显示的运算符被称为二元运算符，因为它们使用两个值；使用一个值的运算符是一元运算符 `console.log(- (10 - 2))`。

```javascript
// -> -8
```

### 布尔值

布尔是一种仅在两种可能性之间区分的值，如“开启”和“关闭”等。布尔值只包含 `true` 和 `false`。

### 比较

比较是创建布尔值的方法：`console.log(3 > 2)`

```javascript
// -> true
```

```javascript
console.log(3 < 2)
```

```javascript
// false
```

`>` 和 `<` 字符分别代表“大于”和“小于”符号。你可以在布尔中使用二元运算符来确定包含的值是 `true` 还是 `false`。

你可以同样地比较字符串。

```javascript
console.log("Aardvark" < "Zoroaster")
```

```javascript
// true
```

你可以按照字母顺序指示字符串，大写字母通常比小写字母“小”，所以 `"Z" < "a"`，且非字母字符（`!`、`\` 等）也存在于排序中。当 JavaScript 想要比较字符串时，它从左到右识别字符，单独区分 Unicode 编码。

这里是其他相关的运算符：`<=`（小于等于）、`>=`（大于等于）、`==`（等于）、`!=`（不等于）。

本章将介绍 JavaScript 值的四种类型：字符串、数字、`undefined` 值和布尔值。这些值通过将它们的名称作为 `true`、`null` 或值（如 `1`、`"ABC"`）产生。运算符可以整合并更改值。我们查看了用于算术（`+`、`-`、`*`、`/` 和 `%`）、字符串拼接（`+`）、比较（`==`、`===`、`!=`、`<=`、`<`、`>=`）和逻辑（`&&`、`||`）的二元运算符，以及各种一元运算符（`!` 取反、`typeof` 查找值的类型）以及根据第三值选择两个值之一的三元运算符（`?:`）。你将获得足够的信息像小计算器一样使用 JavaScript，并在后续章节中不断进步。

### 练习

编写一个 JavaScript 练习，通过用户定义的名称构建一个变量。

### 解决方案

## HTML 代码:

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>使用用户定义的名称创建变量</title>
</head>
<body>

</body>
</html>
```

## JavaScript 代码:

```javascript
var var_name = 'abcd';
var n = 120;
this[var_name] = n;
console.log(this[var_name])
```

## 第 3 章：程序结构

我们将开始扩展 JavaScript 编程语言命令，超越句子片段和名词。

### 表达式与语句

产生一个值的代码块被称为**表达式**。精确写为如 `22` 的单值字面量被称为表达式。在二元运算符中设置为两个表达式的表达式，或在括号内的表达式都是表达式。一个可以像人类语言翻译一样容纳其他表达式的表达式。它使我们能够开发叙述任意复杂计算的表达式。当一个表达式类似于句子片段时，JavaScript 语句将完成该句子。语句列表被称为**程序**，最易访问的语句类型是以分号结尾的一行代码。

例如：

```javascript
;
false;
```

通过此功能，语句可以独立存在，它还可以为屏幕添加偶尔更改颜色的特性，或修改机器的内部状态以影响其后的后续语句。

### 绑定

JavaScript 使用变量的**绑定**来存储值，例如：

获取钱 → `5 * 5;`

`let` 是该语句中的关键字，意味着该句子将指定一个绑定，并可以使用 `=` 运算符和表达式附带绑定名称和值。将定义的绑定作为表达式使用，即一个包含绑定值的表达式。下面是一个示例：

```javascript
let ten = 10;
console.log(ten * ten);
// → 100
```

`=` 运算符用于现有的绑定，以从设置值中移除绑定并将其指向新值。

```javascript
let mood = "light";
console.log(mood);
// → light
mood = "dark";
console.log(mood);
// → dark
```

定义绑定但不赋值值将导致没有内容可供。因此，请求绑定的值会产生 `undefined` 值。你可以通过逗号分隔的单一语句定义多个绑定，

```javascript
let one = 1, two = 2;
console.log(one + two);
// → 3
```

使用 `var` 和 `const` 关键字来熟悉地开发绑定：

```javascript
var name = "Ayad";
const greeting = "Hello ";
console.log(greeting + name);
// -> Hello Ayad
```

`const` 词意味着**常量**。它描述了一种坚定的绑定，在其整个生命周期内指向其设置的值。这些词通常用于声明一个名称绑定到一个值，以便稍后轻松引用。

### 绑定名称

尽管有一些如 `const`、`class`、`default`、`break`、`continue`、`delete` 或 `else` 等保留字，但任何单词都可以作为绑定名称，它也可以包含数字，但语句不能以数字开头。绑定名称还可以包含美元符号（`$`）或下划线（`_`），但不接受任何其他特殊字符或标点符号。

### 环境

在特定时刻存在的绑定和值的组被称为**环境**。当你启动程序时，环境持有语言标准绑定，并通常包含创建与系统环境交互的绑定。例如，浏览器携带了可以与启动的网站通信的函数，以及读取键盘和鼠标输入的函数。

### 函数

封装在值中的部分程序被称为**函数**，这些值被添加以启动封装的程序。例如，一个为用户输入显示一个小对话框的函数。

```javascript
prompt("Enter passcode");
```

影响函数的过程描述为**调用**、**唤起**或**应用**。通过在提供函数值的表达式后插入括号来调用函数。将括号的值设为函数内的程序。将设为函数的值设置为参数。

### console.log 函数

在上面的示例中，我们使用 `console.log` 输出值。所有主流浏览器都利用 `console.log` 函数向输出文本的设备打印其参数。在现代浏览器中，输出通常在默认不可见的 JavaScript 控制台中；你可以轻击键盘上的 `F12` 键，或者在 Mac 上使用 `command-option-I`。绑定名称不适应点字符，但 `console.log` 可以，因为它是一个从 `console` 绑定中恢复 `log` 属性的表达式。

### 返回值

函数用于产生产生副作用。它们也可以提供值。例如，`Math.max` 将接受参数并返回最大的值。

```javascript
console.log(Math.max(2, 4));
// → 4
```

当程序中有多个语句时，它们按顺序执行。下面是一个示例：

```javascript
let num = Number(prompt("Pick a number"));
if (num < 10) {
  console.log("Small");
} else {
  console.log("Large");
}
```

值通过函数转换为数字。键盘被用于开发 JavaScript 中的条件执行。你可能希望仅当特定条件成立时才执行某些代码。只有当输入是数字时，让我们显示输入的平方。

```javascript
let theNumber = Number(prompt("Select a digit"));
if (!Number.isNaN(theNumber)) {
  console.log("Your digit is the square of " + theNumber * theNumber);
} else {
  console.log("Hey. 为什么不给我一个数字?");
}
```

```javascript
} else if (num < 100) {
  console.log("Medium");
} else {
  console.log("Large");
}
```

程序确认 `num` 是否小于 10，如果是，则选择该分支并显示 "Small"。但如果 `num` 大于 10，它将选择 `else` 分支，该分支包含一个独立的第二个语句。

### while 和 do 循环

这是编写一个显示从 0 到 12 之间所有偶数的程序。

```javascript
console.log(0);
console.log(2);
console.log(4);
console.log(6);
console.log(8);
console.log(10);
console.log(12);
```

`while` 循环是当条件满足时重复执行代码块的方法。

```javascript
let i = 0;
while (i <= 12) {
  console.log(i);
  i += 2;
}
```

`do...while` 循环至少执行一次代码块，然后检查条件。

```javascript
let i = 0;
do {
  console.log(i);
  i += 2;
} while (i <= 12);
```

### for 循环

`for` 循环通常用于已知循环次数的情况。

```javascript
for (let i = 0; i <= 12; i += 2) {
  console.log(i);
}
```

`for` 循环由三个部分组成：初始化、条件和迭代表达式。

```javascript
console.log(abc.length);
// → 3
```

## 第 4 章：函数

函数是 JavaScript 编程语言的灵魂和核心。将一部分程序封装在值中的概念具有许多优势。它提供了一种组织更重要程序的方法，减少了重复，将名称与子程序关联起来，并将程序从自身分离开来。函数被用于描述新的词汇。

### 定义函数

函数是一种系统性的绑定，其中函数定义了绑定值。下面的代码指示了一个提供指定数字平方的函数：

```javascript
const square = function(x) {
  return x * x;
}
console.log(square(12));
```

使用以 `function` 关键字开头的表达式创建一个函数。函数由一个函数体和一组参数组成，当你调用函数时，参数会容纳待执行的语句。函数体始终应该包含在大括号中，即使它只是单个语句。函数可以包含多个参数，也可以包含零参数。在下面的示例中，`makeNoise` 不包含参数名，而 `power` 包含两个：

```javascript
const makeNoise = function() {
  console.log("Pling!");
};
makeNoise();
// -> Pling!

const power = function(base, exponent) {
  let result = 1;
  for (let count = 0; count < exponent; count++) {
    result *= base;
  }
  return result;
}
console.log(power(2, 10));
```

某些函数可以像 `square` 和 `power` 那样创建值，而某些结果只产生副作用。末尾不包含表达式的 `return` 关键字将作为返回 `undefined`。

### 绑定与作用域

每个绑定都由一个作用域组成，该作用域使得绑定可见。每当你调用函数时，都会产生新的绑定实例。这在函数之间创建了分离，每个函数调用都在自己的世界中运行，并且易于理解。在 2015 年之前的 JavaScript 中，用 `var` 关键字声明的函数可以在全局作用范围内可见。它们在函数内部是不可见的。

```javascript
let x = 10;
if (true) {
  let y = 20;
  var z = 30;
  console.log(x + y + z);
  // -> 60
}
// y 在这里不可见
console.log(x + z);
// -> 40
```

### 嵌套作用域

JavaScript 区分全局绑定和局部绑定。你可以在其他函数和块内部创建块和函数，从而产生多个程度的局部性。例如，这个函数产生了制作鹰嘴豆酱所需的组件，其内部包含了另一个函数：

```javascript
const hummus = function(factor) {
  const ingredient = function(amount, unit, name) {
    let ingredientAmount = amount * factor;
    if (ingredientAmount > 1) {
      unit += "s";
    }
    console.log(`${ingredientAmount} ${unit} ${name}`);
  }
  ingredient(1, "can", "chickpeas");
  ingredient(0.25, "cup", "tahini");
  ingredient(0.25, "cup", "lemon juice");
  ingredient(1, "clove", "garlic");
  ingredient(2, "tablespoon", "olive oil");
  ingredient(0.5, "teaspoon", "cumin");
};
```

组件函数内部的代码可以访问外部函数的 `factor` 绑定。在块内部可访问的绑定集合由程序文本中的块位置决定。每个局部作用域都可以访问其包含的局部作用域，每个作用域都可以良好地访问全局作用域。这个概念被称为词法作用域（lexical scoping）。

### 作为值的函数

函数绑定通常表现为特定程序块的名称。这种绑定在定义后不会改变。函数可以用于任意表达式，也可以用于将函数值保存到新变量中。

```javascript
const add = function(a, b) {
  return a + b;
};
console.log(add(2, 3));
```

### 声明式

使用 `function` 关键字声明的函数会发生提升，可以在定义之前调用它们。

```javascript
function greet() {
  console.log("Hello!");
}
greet();
```

### 赋值表达式

将函数赋值给变量，这被称为函数表达式。

```javascript
const sayHi = function() {
  console.log("Hi!");
};
sayHi();
```

### 匿名函数

函数没有名称，这被称为匿名函数。

```javascript
function() {
  console.log("I am anonymous");
}
```

### 箭头函数

箭头函数使用 `=>` 语法，它们是更简洁的写法。

```javascript
const double = (x) => x * 2;
console.log(double(5));
```

箭头函数没有自己的 `this` 绑定，它们会继承定义时所在作用域的 `this`。

```javascript
console.log(power(4));
// -> 16
console.log(power(2, 6));
// -> 64
```

将函数作为值使用的能力，与每当你调用函数时都会创建局部绑定这一事实是耦合的。下面的代码展示了这个例子；它描述了一个包装值，该函数创建了一个局部绑定，然后返回一个进入并返回该局部绑定的函数。

```javascript
function wrapValue(n) {
  let local = n;
  return () => local;
}
let wrap1 = wrapValue(1);
let wrap2 = wrapValue(2);
console.log(wrap1());
// -> 1
console.log(wrap2());
// -> 2
```

这个概念被称为**闭包**。它让用户能够在限制作用域内引用局部绑定的特定实例。通过增加一些修改，我们之前的示例可以变成一种按任意数量累加函数的方法。

```javascript
function multiplier(factor) {
  return number => number * factor;
}
let twice = multiplier(2);
console.log(twice(5));
// → 10
```

### 递归

一个函数可以调用自己，但不应频繁地调用自己以避免栈溢出。递归函数是指会调用自身的函数。递归使得一些以不同风格编写的函数成为可能。例如，下面的代码是 `power` 的执行。

```javascript
function power(base, exponent) {
  if (exponent == 0) {
    return 1;
  } else {
    return base * power(base, exponent - 1);
  }
}
console.log(power(2, 3));
// → 8
```

这种执行存在一个问题。与其他循环版本相比，它更慢。利用单个循环被认为比多次调用函数成本更低。尽管这并不意味着递归不是一种有效的循环方案，但某些问题用递归解决比使用循环更容易。例如，那些需要检查或处理多个分支的问题。来看这个：我们从数字 1 开始，不断地加 5 或乘以 3。例如，数字 13 可以通过乘以 3 再加两次 5 获得，因此我们无法得到 15。该代码是递归解决方案：

```javascript
function findSolution(target) {
  function find(current, history) {
    if (current == target) {
      return history;
    } else if (current > target) {
      return null;
    } else {
      return find(current + 5, `${history} + 5`) ||
      find(current * 3, `${history} * 3`);
    }
  }
  return find(1, "1");
}
console.log(findSolution(24));
// → ((1 * 3) + 5) * 3)
```

内部函数接受两个参数：当前数字和一个记录获取该数字过程的字符串。如果找到了解决方案，它返回一个显示通目标路径的字符串；如果没有找到解决方案，返回的值将是 `null`。为了实现这一点，函数执行三个动作之一：如果你的目标是当前数字，你可以通过当前数字达到该目标，因此将其返回。有时数字大于目标，但你不需要探索这个选项，因为加法和减法只能增大数字，因此将其返回 `null`。如果你低于目标数字，则通过两次调用自身来尝试从当前数字开始的两个路径，一次用于加法，一次用于乘法。如果第一次调用返回了有效内容，则返回该内容。

```javascript
14 }
15 else {
16     number = number - 2;
17     return is_even_recursion(number);
18 }
19 }
```

## HTML 代码:

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>使用递归判断一个数字是否为偶数。</title>
</head>
<body>
</body>
</html>
```

## 第 5 章：数据结构：对象和数组

数据布局从布尔值、字符串和数字片段发展而来的。某些类型的信息会使用多个一个数据块（chunk）。对象允许用户将值与其他对象整合在一起，以开发出更复杂的布局。在本章中，你将理解解决手头实际问题的概念。

### 数据集

如果你想处理大量的数字数据，你必须在机器内存中表示这些数字数据。例如，你需要表示一组数字，如 2, 3, 5, 7 和 11。现在，让我们充分利用字符串，因为字符串可以包含大量数据。我们将使用 `2 3 5 7 11` 作为表示。JavaScript 语言提供了一种用于保存值序列唯一数据类型，称为数组。在方括号 `[]` 之间将数组写入值列表，并用逗号分隔。

```javascript
let listOfNumbers = [2, 3, 5, 7, 11];
console.log(listOfNumbers[2]);
// → 5
console.log(listOfNumbers[0]);
// → 2
console.log(listOfNumbers[2 - 1]);
// → 3
```

用于获取数组内元素的符号也使用方括号。一对完整的方括号紧跟在一个包含另一个表达式的表达式之后。当你开始计算数组中的元素时，你从 0 开始，而不是从 1 开始。因此，第一个元素通过 `listOfNumbers[0]` 获取。

### 属性

之前的章节包含过如 `myList.length`（用于计算字符串长度）和 `Math.max`（最大值函数）之类的表达式。这些都是用于访问属性值的属性。几乎所有的 JavaScript 值都包含属性。少数不包含属性的值是 `null` 和 `undefined`。如果你使用非零值访问属性，结果将是一个错误。

```javascript
null.length;
// -> TypeError: null has no properties
```

在 JavaScript 中，评估属性的两种主要方法是使用点符号和方括号。`value.x` 和 `value[x]` 可以评估值上的属性，但并不特定是同一个属性。你使用 `x` 的方式与使用点符号的方式不同。

如果你想使用点符号，你在点符号之后输入的文本就是属性名。如果你打算使用方括号，则访问方括号内的表达式来获取属性名。`value.x` 交付名为 “x” 的 value 属性，而 `value[x]` 则是访问表达式 `x` 并使用其结果，将结果转换为字符串作为属性名。如果你想要的属性名为 `color`，你应该输入 `value.color`。你可以从在绑定 `i` 中调用的值中提取该属性，输入 `value[i]`。属性名是字符串，但点符号表示法仅对有效的绑定名有效。因此，如果你想评估一个名为 `2` 或 `John Doe` 的属性，请使用方括号：`value[2]` 或 `value["John Doe"]`。

数组内的元素作为数组的属性保存，这些属性使用数字作为属性名。数组的 `length` 属性决定了它包含多少项。该属性名称是一个有效的绑定名。输入 `array.length` 来确定数组的长度，这比输入 `array["length"]` 要容易得多。

### 方法

字符串和数组对象包含了几个存储函数值的属性。

```javascript
let doh = "Doh";
console.log(typeof doh.toUpperCase);
// -> function
console.log(doh.toUpperCase());
// -> Doh
```

每个字符串都包含一个 `toUpperCase` 属性。当你调用此属性时，它会返回字符串的副本，其中所有的字母都转换为大写。虽然 `toUpperCase` 不通过参数传递，但该函数可以评估字符串 "Doh"，它是上述调用值的属性。由函数组成的属性被称为方法。下面的示例说明了两个可以影响数组的方法。

```javascript
let sequence = [1, 2, 3];
sequence.push(4);
console.log(sequence);
// -> [1, 2, 3, 4]
sequence.pop();
console.log(sequence);
// -> [1, 2, 3]
```

`push` 方法向数组末尾添加一个元素。`pop` 方法从数组中删除最后一个元素并返回它。`shift` 方法从数组中删除第一个元素。`unshift` 方法在数组开头添加一个元素。`splice` 方法通过删除或替换现有元素来更改数组的内容。`slice` 方法将数组的一部分通过浅拷贝返回一个新的数组对象中。`join` 方法将数组的所有元素连接成一个字符串。`filter` 方法创建一个包含所有通过提供函数实现的测试的元素的新数组。`map` 方法通过对每个数组元素执行函数来创建一个新数组。`reduce` 方法在数组的每个元素上执行归约器函数，产生单一的输出值。`sort` 方法原地对数组元素进行排序。`forEach` 方法为数组的每个元素调用一次提供的函数。

`in` 运算符如果指定的属性在对象中，则返回 `true`。`hasOwnProperty()` 方法如果对象拥有指定的属性作为其自身的属性，则返回 `true`。

```javascript
let person = {name: "Alice", age: 25};
console.log("name" in person); // true
console.log("gender" in person); // false
console.log(person.hasOwnProperty("name")); // true
console.log(person.hasOwnProperty("id")); // false
```

```javascript
let object3 = {value: 10};
console.log(object1 == object2);
// -> true
console.log(object1 == object3);
// -> false
object1.value = 15;
console.log(object2.value);
// -> 15
console.log(object3.value);
// -> 10
```

`object1` 和 `object2` 绑定持有同一个对象，这就是为什么修改 `object1` 会影响 `object2` 的值的原因。它们在本质上是相同的。绑定 `object3` 指向一个独立的对象，该对象包含与 `object1` 类似的属性，但具有不同的生命。绑定可以是常量或可变的，但这不会影响它们的值。指向对象的 `const` 绑定不能被转换，并且会持续地指向同一个对象。而对象的内容是可以改变的。

```javascript
const score = {visitors: 0, home: 0};
// 这是被允许的
score.visitors = 1;
// 这是不允许的
score = {visitors: 1, home: 1};
```

当使用 JavaScript 的 `==` 运算符来区分对象时，它使用标识符来执行该任务。如果对象包含相同的值，它将返回 `true`。区分多个对象将返回 `false`，即使它们的属性相似。

### 狼人的日志

所以，你开始运行你的 JavaScript 解释器，并创建你记录日记所需的环境。

```javascript
let journal = [];

function addEntry(events, squirrel) {
  journal.push({events, squirrel});
}
```

它不是声明像 `events` 这样的属性，而是设置了一个属性名。

那么，在每天晚上 10 点或偶尔在第二天早晨，从你书架的顶层拿下来，记录你的每日日志。

```javascript
addEntry([
```

相关性是分析变量之间脆弱性的评估。它们被认为是跨越从 -1 到 1 的值。不相关的变量被称为零相关。相关性为 1 表示两者是相关的。负相关意味着变量之间是完美相关但互为相反；一个为真，另一个为假。要计算两个布尔值之间相关性的评估，请使用 Phi 系数（φ）。该公式的输入是一个频率表，记录了观察到的几种变量组合的次数。公式的输出将是 -1 到 1 之间的数字。这是相关性的最佳定义。

让我们以吃披萨这一事件作为例子，并将其插入频率表中，其中每个数字代表总次数，即我们在测量中使用的组合次数。我们将表格命名为 $n$，并使用以下公式计算 $\phi$：

$\phi = \frac{n_{11}n_{00} - n_{10}n_{01}}{\sqrt{n_{11}\cdot n_{00}+n_{10}\cdot n_{01}}}$

符号 $n_{01}$ 表示第一个变量变为假（0）而第二个变量变为真（1）的测量次数。在披萨表中，$n_{01}$ 为 9。

值 $n_{11}$ 表示所有第一个变量变为真的测量总和，在表格示例中为 5。同样，$n_{00}$ 表示第二个变量变为假的测量数量。

在披萨表中，除分线上面的部分将是 $1\times7-4\times9 = 40$，下面的部分将是 $5\times8\times10$ 的平方根，或 $\sqrt{340000}$。结果将为 $\phi = 0.069$，非常微小。因此，吃披萨对转换没有影响。

## 计算相关性

JavaScript 允许用包含四个元素的数组 `[76, 9, 4, 1]` 来表示一个二二表。其他表示方法如持有两个二元素元素的数组 `[[76, 9], [4, 1]]`。

```javascript
todoList.unshift(task);
}
```

上面的程序组织了一个任务链。你可以通过调用 `remember("groceries")` 将任务添加到队列末尾，当你想要完成某项任务时，使用 `getTask()` 从队列中获取（并移除）项目。如果你想搜索某个特定值，数组提供了 `indexOf` 方法。该方法从数组头到尾遍历数组，如果找到了，则返回请求的索引值；如果没有找到，则返回 -1。如果要从尾到头搜索，请使用 `lastIndexOf` 方法。

```javascript
console.log([1, 2, 3, 2, 4].indexOf(3));
// → 1
```

```javascript
console.log([1, 2, 3, 2, 4].lastIndexOf(3));
// → 3
```

`indexOf` 和 `lastIndexOf` 接受一个可选参数，用于指定搜索开始的位置。另一个非常棒的方法是 `slice`，该方法指定起始和结束索引，并返回一个包含三个元素的数组。起始位置是包含的，而结束位置是不包含的。

```javascript
console.log([0, 1, 2, 3, 5].slice(2, 4));
// → [2, 3]
```

```javascript
console.log([0, 1, 2, 3, 5].slice(2));
// → [2, 3, 5]
```

如果未指定结束索引，`slice` 将取起始索引之后的所有元素。你可以使用 `concat` 方法将数组连接在一起以生成新数组。下面的示例展示了 `concat` 和 `slice` 的用法。

```javascript
function remove(arrays, index) {
  return array.slice(0, index)
  .concat(arrays.slice(index + 1));
}
console.log(remove(["a", "k", "c", "f", "e"], 2));
// // ["a", "k", "f", "e"]
```

## 字符串及其属性

在字符串值章节，我们讨论了 `length` 和 `UpperCase`。如果你想添加一个新属性，它是不会持久的。

```javascript
let kim = "Kim";
kim.age = 88;
```

```javascript
console.log(kim.age);
// -> undefined
```

所有的字符串值都包含几个方法。其中包括 `slice` 和 `indexOf`，它们的外和名称与数组方法相似。

```javascript
console.log("coconuts".slice(4, 7));
// → nut
```

```javascript
console.log("coconut".indexOf("u"));
// → 5
```

字符串的 `indexOf` 可以查找包含多个字符的字符串，而对应的数组方法搜索的是单个元素。

```javascript
console.log("one two three".indexOf("ee"));
// → 11
```

`trim` 方法可以清除字符串开头和结尾的空白字符。

```javascript
console.log(" okay \n ".trim());
// → okay
```

零填充函数也可以称为 `padStart`，它接受首选的填充字符和长度字符作为参数。

```javascript
console.log(String(6).padStart(3, "0"));
// → 006
```

你可以使用 `split` 在另一个字符串出现的每个地方拆分字符串，然后使用 `join` 将它们连接在一起。

```javascript
let sentence = "Secretarybirds specialize in stomping";
let words = sentence.split(" ");
```

```javascript
console.log(words);
// → ["Secretarybirds", "specialize", "in", "stomping"]
```

```javascript
console.log(words.join(". "));
// → Secretarybirds. specialize. in. stomping
```

你可以使用 `repeat` 方法来重复字符串，它会生成一个包含多个原始字符串副本的新字符串。

```javascript
console.log("LA".repeat(3));
// → LALALA
```

如果你想访问字符串中的单个字符，请看下文：

```javascript
let string = "ABC";
```

```javascript
console.log(string.length);
// -> 3
console.log(string[1]);
// -> b
```

## 剩余参数 (Rest parameters)

函数接收任意数量的参数是非常重要的。如果你想写这样一个函数，在函数的最后一个参数之前添加三个点。

```javascript
function max (...numbers) {
  let result = -Infinity;
  for (let number of numbers) {
    if (number > result) result = number;
  }
  return result;
}
console.log(max(4, 1, 9, -2));
// -> 9
```

当你调用函数时，剩余的参数属于一个包含剩余参数的数组。你也可以利用三点表示法在参数数组中调用函数。

```javascript
let numbers = [5, 1, 7];
console.log(max(...numbers));
// -> 7
```

将数组展开到函数调用中，将元素作为不同的参数传递，例如 `max (9, ...numbers, 2)`。方括号数组表示法允许三点运算符将另一个数组引入新数组。

```javascript
let words = ["never", "fully"];
```

```javascript
console.log(["will", ...words, "understand"]);
// → ["will", "never", "fully", "understand"]
```

## Math 对象

`Math` 对象被用作一个汇总许多相似功能的容器。它产生了一个命名空间，使得值和函数不需要进行全局绑定。

```javascript
function randomOnCircle(radius) {
  let angle = Math.random() * 2 * Math.PI;
  return {
    x: radius * Math.cos(angle),
    y: radius * Math.sin(angle)
  };
}
console.log(randomOnCircle(5));
```

可以通过一种特殊的循环类型——`for(let element of array)` 来遍历数组。

### 练习

编写一个 JavaScript 函数来获取数组的第一个项。设置参数 'n' 将返回数组的前 'n' 个元素。

数据：

```javascript
console.log(array_Clone([1, 2, 4, 0]));
console.log(array_Clone([1, 2, [4, 0]]));
```

```
[1, 2, 4, 0]
[1, 2, [4, 0]]
```

### 解决方案

```javascript
9 };
10 console.log(first([7, 9, 0, -2]));
11 console.log(first([],3));
12 console.log(first([7, 9, 0, -2],3));
13 console.log(first([7, 9, 0, -2],6));
14 console.log(first([7, 9, 0, -2],-3));
```

## HTML 代码:

```html
1 <!DOCTYPE html>
2 <html>
3 <head>
4 <meta charset="utf-8">
5 <title>Get the first element of an array</title>
6 </head>
7 <body>
8 </body>
9 </html>
```

## JavaScript 代码:

```javascript
1 var first = function(array, n) {
2 if (array == null)
3 return void 0;
```

```javascript
if (n == null) {
    return array[0];
} if (n < 0) {
    return [];
}
return array.slice(0, n);
```

## 第 6 章：高阶函数

大型程序的开发需要时间，并产生大量的 bug 隐藏空间，这反过来使得它们难以找到。以下是两个大型程序的示例：

第一个是自包含的，语句有六行长。

```javascript
let total = 0, count = 1;
while (count <= 10) {
total += count;
count += 1;
}
console.log(total);
```

第二个依赖于两个外部函数，语句只有一行长。

```javascript
console.log(sum(range(1, 10)));
```

### 抽象

当提到 JavaScript 编程语言时，我们使用“抽象”这一术语。抽象用于隐藏细节，并赋予用户在更高层次上讨论问题的能力。让我们区分两种豌豆汤的配方。首先：

每人，在容器内放入 1 杯干豌豆。加入足够的水淹没豌豆，让其浸泡泡约 12 小时。将其从水中取出，放入用于烹饪的锅中，加入四杯水（4 杯）。

让其煮沸约两小时，每人准备半个洋葱，用刀切并倒入豌豆中，让其准备 10 分钟。

然后是第二种配方：

每人：半个洋葱，一根芹芹，1 杯干分豌豆和一根胡萝卜。

将豌豆浸在水中约 12 小时。在水（4 杯）中煮沸约 2 小时，准备并切片蔬菜。煮 10 分钟。

计算机逐个执行任务，从盲目到高层概念。

### 抽象重复

普通函数用于创建抽象。程序按指定次数重复某个函数是习惯性的。你可以通过这样的循环来实现：

```javascript
for (let i = 0; i < 10; i++) {
console.log(i);
}
```

在这里，我们写了一个调用 `console.log` N 次的函数。

```javascript
function repeatLog(n) {
for (let i = 0; i < n; i++) {
console.log(i);
}
}
```

如果你想执行一个与记录数字不同的任务，可以将动作作为函数值传入。

```javascript
function repeat(n, action) {
  for (let i = 0; i < n; i++) {
    action(i);
  }
}
repeat(3, console.log);
// -> 0
// -> 1
// -> 2
```

有时你不需要回传一个预定义的函数来在循环中重复，可以创建一个函数值作为替代：

```javascript
let labels = [];
repeat(5, i => {
  labels.push("Unit ${i + 1}");
});
console.log(labels);

// -> ["Unit 1", "Unit 2", "Unit 3", "Unit 4", "Unit 5"]
```

这种方法的布局与循环相似；它定义了循环类型然后产生循环体。尽管循环体是写在 `repeat` 调用括号内的函数中的。

### 高阶函数

高阶函数是指处理其他函数的函数，无论是通过参数还是通过返回它们。这种类型的函数允许用户对动作进行抽象。例如，你有一个可以产生函数的函数：

```javascript
function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(11));
// -> true
```

你也可以拥有可以转换其他函数。

```javascript
function noisy(f) {
  return (...args) => {
    console.log("calling with", args);
    let result = f(...args);
    console.log("called with", args, "returned", result);
    return result;
  }
}
noisy(Math.min)(3, 2, 1);
// -> calling with [3, 2, 1]
// -> called with [3, 2, 1], returned 1
```

你还可以编写产生新一组控制流的函数。

```javascript
function unless(test, then) {
  if (test) then();
}
repeat(3, n => {
  unless(n % 2 == 1, () => {
    console.log(n, "is even");
  });
});
// -> 0 is even
// -> 2 is even
```

这种方法是一个内置数组方法 `forEach`，它作为高阶函数产生类似于 `for/of` 循环的循环。

```javascript
["A", "B"].forEach(l => console.log(l));
// -> A
// -> B
```

### 过滤

```javascript
function filter(array, test) {
  let result = [];
  for (let item of array) {
    if (test(item)) {
      result.push(item);
    }
  }
  return result;
}
```

### 使用 map

`map` 方法使用函数更改数组中的每个元素。

```javascript
function map(array, transform) {
  let result = [];
  for (let item of array) {
    result.push(transform(item));
  }
  return result;
}
```

### 组合性

当你想要组合操作时，可以使用高阶函数。例如，这里有一行代码用于搜索数据集中人类脚本中生存和死亡的平均年份。

```javascript
function average(array) {
  return array.reduce((a, b) => a + b) / array.length;
}
console.log(Math.round(average(
SCRIPTS.filter(s => s.living).map(s => s.year))));
// → 1165
console.log(Math.round(average(
SCRIPTS.filter(s => !s.living).map(s => s.year))));
// → 204
```

代码块显示死亡脚本比生存脚本更老。

让我们从整个脚本开始，过滤掉死亡（生存），提取年份，计算平均值并完成结果。我们可以很好地将这些计算写成一个大循环：

```javascript
let total = 0, count = 0;
for (let script of SCRIPTS) {
```

```javascript
if (script.living) {
  total += script.year;
  count += 1;
}
console.log(Math.round(total / count));
// → 1165
```

我们的两个示例并不相同，第一个示例在执行 `map` 和 `filter` 时会创建新数组，而第二个只计算数字。

### 字符串与字符编码

数据集的一个重要用途是找出某个文本块使用的是哪种脚本。以下是一个执行该任务的程序。

每个脚本都包含一个与其相关的字符代码范围数组。因此，如果你给你一个字符代码，可以使用此函数来查找对应的脚本（如果可用）：

```javascript
function characterScript(code) {
  for (let script of SCRIPTS) {
    if (script.ranges.some(([from, to]) => {
      return code >= from && code < to;
    })) {
      return script;
    }
  }
  return null;
}
console.log(characterScript(121));

// → {name: "Latin", ...}
```

另一个高阶函数是相同的方法。该方法接收一个测试函数，并判断该函数是否对数组中的任何组件返回 `true`。

JavaScript 字符串上进行一些操作，例如使用 `length` 属性获取其长度，以及通过方括号 `[]` 评估其内容。

```javascript
// 两个 emoji 字符，马和鞋
let horseShoe = "🐎👟";
console.log(horseShoe.length);
// → 4
console.log(horseShoe[0]);
// → (无效的半字符)
console.log(horseShoe.charCodeAt(0));
// → 55357 (半字符的编码)
console.log(horseShoe.codePointAt(0));
// → 128052 (马脸表情的实际编码)
```

JavaScript 的 `charCodeAt` 方法提供一个完整的 Unicode 字符。该方法用于从字符串中提取字符。尽管传递给 `codePointAt` 的参数仍然是连续代码单元的索引。如果你使用 `codePointAt` 遍历字符串，它产生的是真实的字符而不是代码单元。

```javascript
let roseDragon = "🌹🐉";
for (let char of roseDragon) {
  console.log(char);
}
// -> 🎈
// -> 🐲
```

### 识别文本

你现在有了 `characterScript` 函数和正确遍历字符的方法，现在计算每个脚本所拥有的字符数量。这里使用了以下计数抽象：

```javascript
function countBy(items, groupName) {
  let counts = [];
  for (let item of items) {
    let name = groupName(item);
    let known = counts.find(c => c.number == name);
    if (known == -1) {
      counts.push({number, count: 0});
    } else {
      counts[known].count++;
    }
  }
  return counts;
}
console.log(countBy([0, 1, 2, 3, 4, 5], n => n > 2));
// -> [{number: false, count: 2}, {number: true, count: 3}]
```

`countBy` 函数预期一个集合（一组数字、元素或任何你可以用 `for`/`of` 遍历的物体）以及一个用于为指定元素计算组名的函数。它返回一个对象列表。每个对象都命名一个组，并确定该组中包含的元素数量。

`findIndex` 方法与 `indexOf` 类似。该方法用于搜索第一个指定函数返回 `true` 的值，当未找到元素时返回 `-1`。你可以使用 `countBy` 来确定文本块中使用了哪些脚本。

```javascript
function textScripts(text) {
  let scripts = countBy(text, char => {
    let script = characterScript(char.charCodeAt(0));
    return script ? script.name : "none";
  }).filter(({name}) => name != "none");
  let total = scripts.reduce((n, {count}) => n + count, 0);
  if (total == 0) return "No scripts found";
  return scripts.map(({name, count}) => {
    return `${Math.round(count * 100 / total)}% ${name}`;
  }).join(", ");
}
console.log(textScripts('英国的狗"woof", 俄罗斯的狗"тяв"'));
// 61% Han, Latin, 17% Cyrillic
```

该函数通过 `characterScript` 根据名称计算字符，并对于没有脚本的字符返回字符串 `"none"`。如果你想计算百分比，需要通过 `reduce` 方法确定某个脚本的总数。

### 总结

将函数值传递给多个函数是 JavaScript 的一个重要特性。它允许编写之间存在“间隙”的函数。声明这些函数的代码可以通过提供函数值包含这些间隙。数组提供了许多重要的高阶方法。使用 `forEach` 遍历数组元素。使用 `filter` 方法返回符合谓词函数的新数组。使用 `map` 通过函数更改每个项。使用 `reduce` 将数组的每个组件合并为一个单独的值。

### 练习

编写一个 JavaScript 函数，接收一个保存的数字数组并搜索第二大的数。

## 答案

```javascript
function findSecond(numbers) {
  let first = -Infinity;
  let second = -Infinity;
  for (let n of numbers) {
    if (n > first) {
      second = first;
      first = n;
    } else if (n > second) {
      second = n;
    }
  }
  return second;
}
console.log(findSecond([10, 5, 8, 2, 7])); // 8
```

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>查找第二大</title>
</head>
<body>
  <p>第二大的数字是 8。</p>
</body>
</html>
```

## 第 7 章：对象的秘密生活

```javascript
Array.prototype;
// -> true
```

这种类型的原型对象包含一个原型，即 `Object.prototype`，因此它可以间接创建如 `toString` 等方法。使用 `Object.create` 可以构建具有特定原型的对象。

```javascript
let protoRabbit = {
  speak(line) {
    console.log(`The ${this.type} rabbit says '${line}'`);
  }
};
let killerRabbit = Object.create(protoRabbit);
killerRabbit.type = "killer";
killerRabbit.speak('SKREEEE!');
```

在对象表达式中的 `speak(line)` 会产生一个名为 `speak` 的属性，并将函数设置为其值。它是描述方法的简写方式。

"proto" 兔子是所有属性的容器。

## 类 (Classes)

JavaScript 的原型系统可以描述为称为“类”的面向对象的方法。类描述了一个对象类型的形状、其属性和方法。原型用于描述属性，使得每个实例共享相似的值（作为方法）。如果你想构建一个特定类的实例，创建一个接收普通原型的对象。确保它包含应该包含在该类实例中的属性。下面是构造函数。

```javascript
function rabbit(type) {
  let rabbit = Object.create(protoRabbit);
  rabbit.type = type;
  return rabbit;
}
```

JavaScript 提供了一种轻松描述描述此函数的方法。在函数调用的前面设置关键字。在构建对象期间利用的原型对象是通过获取构造函数的 `prototype` 属性get的。

```javascript
function Rabbit(type) {
  this.type = type;
}
```

```javascript
Rabbit.prototype.speak = function(line) {
  console.log(`The ${this.type} rabbit says '${line}'`);
};
```

```javascript
let weirdRabbit = new Rabbit("weird");
```

`Function.prototype` 是构造函数的原型。它的 `prototype` 属性获取了通过它构建的实例所使用的原型。

```javascript
console.log(Object.getPrototypeOf(Rabbit) === Function.prototype);
// -> true
console.log(Object.getPrototypeOf(weirdRabbit) === Rabbit.prototype);
// -> true
```

### 类语法 (Class notation)

JavaScript 类是带有 `prototype` 属性的构造函数。下面是一个示例：

```javascript
class Rabbit {
  constructor(type) {
    this.type = type;
  }
  speak(line) {
    console.log(`The ${this.type} rabbit says '${line}'`);
  }
}
let killerRabbit = new Rabbit("killer");
let blackRabbit = new Rabbit("black");
```

`class` 关键字以类声明开始，允许你在特定位置描述构造函数和一组方法。类声明允许将获取函数的属性包含在原型中。当你使用表达式时，它并不描述一个绑定，而是提供构造函数作为值。你可以在表达式中排除类名。

```javascript
let object = new class {getWord() { return "hello"; } };
console.log(object.getWord());
// -> hello
```

### 覆盖派生属性 (Overriding derived properties)

当属性被添加到对象时（无论在原型中可用还是不可用），属性都会添加到对象中。如果原型中存在具有相似名称的属性，它不会影响该对象。

```javascript
Rabbit.prototype.teeth = "small";
```

```javascript
console.log(killerRabbit.teeth);
// -> small
killerRabbit.teeth = "long, sharp, and bloody";
console.log(killerRabbit.teeth);
// -> long, sharp, and bloody
console.log(blackRabbit.teeth);
// -> small
console.log(Rabbit.prototype.teeth);
// -> small
```

覆盖属性用于赋予标准函数原型和数组原型一个独立的 `toString` 方法。

```javascript
console.log(Array.prototype.toString === Object);
// -> false
console.log([1, 3].toString());
// -> 1,3
```

在数组上调用 `toString` 会赋予一个类似于对其调用 `join(",")` 的结果。它在数组包含的值值之间放置一个逗号。如果你对数组调用 `Object.prototype.toString`，它会提供一个独立的字符串。

```javascript
console.log(Object.prototype.toString.call([1, 3]));
// → [object Array]
```

### 映射 (Maps)

Map 是一种将值与其他值连接起来的数据布局。如果你想将名称映射到年龄，可以这样写代码：

```javascript
let ages = {
  Boris: 39,
  Liang: 22,
  Júlia: 62
};
console.log(`Júlia is ${ages["Júlia"]}`);
// → Júlia 62
```

```javascript
console.log("Is Jack's age known?", "Jack" in ages);
// → Is Jack's age known? false
```

```javascript
console.log("Is toString's age known?", "toString" in ages);
// → Is toString's age known? true
```

对象的属性名应该是字符串。如果你需要一个键不能转换为字符串的映射，请不要使用对象作为映射。JavaScript 包含一个名为 `Map` 的类。它保存映射并允许不同类型的键。

```javascript
let ages = new Map();
ages.set("Boris", 39);
ages.set("Liang", 22);
ages.set("Júlia", 62);
console.log(`Júlia is ${ages.get("Júlia")}`);
// → Júlia 62
```

```javascript
console.log("Is Jack's age known?", "Jack" in ages);
// → Is Jack's age known? false
```

```javascript
console.log("Is toString's age known?", "toString" in ages);
// → Is toString's age known? true
```

### Symbol (Symbols)

Symbol 是使用 Symbol 构建的唯一值，无法两次构建。

```javascript
let sym = Symbol("name");
console.log(sym === Symbol("name"));
// false
```

当你转换为字符串时，传递给 symbol 的字符串会被附加。

```javascript
const toStringSymbol = Symbol("toString");
Array.prototype[toStringSymbol] = function() {
  return `${this.length} cm of yarn`;
};
console.log([1, 2][toStringSymbol]());
// 2 cm of yarn
```

你可以通过在属性名周围使用方括号在对象类和表达式中附加 symbol。下面引用了存储 symbol 的绑定。

```javascript
let stringObject = {
  [toStringSymbol]() { return "a rope"; }
};
console.log(stringObject[toStringSymbol]());
// a rope
```

### 迭代器接口 (Iterator interfaces)

传递给 `for...of` 循环的对象是可迭代的。这意味着它由一个带有 `Symbol.iterator` 符号的命名组成，当该属性被调用时，该方法返回一个产生第二个布局的对象。它包含一个 `next` 方法，用于返回后续结果。结果是一个带有产生下一个值的对象，`Symbol.iterator` 可以被添加到多个对象。查看此布局：

```javascript
let okiterator = "OK"[Symbol.iterator]();
console.log(okiterator.next());
// → {value: "O", done: false}
console.log(okiterator.next());
// → {value: "K", done: false}
console.log(okiterator.next());
// → {value: undefined, done: true}
```

让我们实现一个可迭代的数据结构。我们将构建一个矩阵类，作用为：

```javascript
constructor(width, height, element = (x, y) => undefined) {
  this.width = width;
  this.height = height;
  this.content = [];
  for (let y = 0; y < height; y++) {
    for (let x = 0; x < width; x++) {
      this.content[y * width + x] = element(x, y);
    }
  }
}
```

```javascript
get(x, y) {
  return this.content[y * this.width + x];
}
set(x, y, value) {
  this.content[y * this.width + x] = value;
}
```

该类的内容存储在一个具有 `width × height` 个元素的独立数组中。这些元素按行存储。构造函数接收一个宽度、高度以及一个额外的元素函数，该函数用于设置初始值。使用 `get` 方法和 `set` 方法来恢复和更新矩阵中的元素。以下是具有 `x`、`y` 和 `value` 属性的对象的布局。

```javascript
class MatrixIterator {
  constructor(matrix) {
    this.x = 0;
    this.y = 0;
    this.matrix = matrix;
  }
  next() {
    if (this.y == this.matrix.height) return {done: true};
    let value = {
      x: this.x,
      y: this.y,
      value: this.matrix.get(this.x, this.y)
    };
    this.x++;
    if (this.x == this.matrix.width) {
      this.x = 0;
      this.y++;
      return {value, done: false};
    }
    return value;
  }
}
```

下面是一个可迭代 `Matrix` 类示例：

```javascript
Matrix.prototype[Symbol.iterator] = function() {
  return new MatrixIterator(this);
}
```

我们现在可以使用 `for/of` 循环遍历矩阵。

```javascript
let matrix = new Matrix(2, 2, (x, y) => `${x},${y}`);
for (let {x, y, value} of matrix) {
  console.log(x, y, value);
}

// -> 0 0 value 0,0
// -> 1 0 value 1,0
// -> 0 1 value 0,1
// -> 1 1 value 1,1
```

### 静态方法、getters 和 setters

布局由方法组成，但你也可以附加存储值的非函数属性，例如 `Map` 对象包含一个确定其中保存了多少键的 `size` 属性。评估过的属性可以隐藏方法调用。这些方法被称为 `getters`，你可以在类声明或对象表达式中通过在方法开头写 "get" 来描述它们。

```javascript
let varyingSize = {
  size() {
    return Math.floor(Math.random() * 100);
  }
}
console.log(varyingSize.size);
// → 73
console.log(varyingSize.size);
// → 49
```

当你想要使用对象的 `size` 属性时，调用关联的方法。当你使用带有 `setter` 的属性时，也可以执行类似的任务。

```javascript
class Temperature {
  constructor(celsius) {
    this.celsius = celsius;
  }
  fahrenheit() {
    return this.celsius * 1.8 + 32;
  }
  set fahrenheit(value) {
    this.celsius = (value - 32) / 1.8;
  }
  static fromFahrenheit(value) {
    return new Temperature((value - 32) / 1.8);
  }
}
```

```javascript
let temp = new Temperature(22);
console.log(temp.fahrenheit);
// -> 71.6
temp.fahrenheit = 86;
console.log(temp.celsius);
// -> 30
```

`Temperature` 类允许你读写摄氏度或华氏度的温度，但它只保存摄氏度，并在华氏度的 getter 和 setter 中进行摄氏度的转换。在类声明中，写在名称之前的 `static` 方法会被保存在构造函数上。因此，你可以通过 `Temperature.fromFahrenheit(100)` 通过华氏度构建温度。

### 继承

某些矩阵是对称的。当通过左上到右下角的对角线反射对称矩阵时，它不会发生。在 `x,y` 处设置的值与 `y,x` 相同。使用 JavaScript 的原型系统来构建新类；新类的原型从旧原型获取，但为该方法设置了新的定义。这在面向对象编程中被称为继承。以下是一个示例：

```javascript
class SymmetricMatrix extends Matrix {
  constructor(size, element = (x, y) => undefined) {
    super(size, size, (x, y) => {
      if (x < y) return element(y, x);
      else return element(x, y);
    });
  }
  set(x, y, value) {
    super.set(x, y, value);
    if (x != y) {
      super.set(y, x, value);
    }
  }
}

let matrix = new SymmetricMatrix(5, (x, y) => `${x}${y}`);
console.log(matrix.get(2, 3));
// -> 3,2
```

### instanceof 运算符

知道一个对象是否来自于特定的 `instanceof` 是重要的。

```javascript
console.log(new SymmetricMatrix(2) instanceof SymmetricMatrix);
// -> true
console.log(new SymmetricMatrix(2) instanceof Matrix);
// -> true
console.log(new Matrix(2, 2) instanceof SymmetricMatrix);
// -> false
console.log([1] instanceof Array);
// -> true
```

该运算符将扫描已继承的类型。因此，`SymmetricMatrix` 是 `Matrix` 的实例。你也可以将此方法应用于如 `Array` 等标准构造函数。

### 总结

在本章中，我们意识到对象的功能不仅仅是持有它们的属性。它们还由同样是对象的原型组成。只要原型具有该属性，它们的行为就像包含了它们并未直接提供的属性一样。简单对象使用 `Object.prototype` 来表示它们的原型。我们还讨论了构造函数，它们是函数，名称通常以大字母开头，并配合 `new` 运算符来构建新对象。新对象的原型将是构造函数中 `prototype` 属性的对象。类语法提供了一种描述构造函数及其原型的方法。我们还接触了 `Getters`、`setters`、静态方法以及 `instanceof` 运算符。

### 练习

编写一个 JavaScript 程序，通过迭代函数和一个主种子值创建一个数组。

### 解决方案

## HTML 代码：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>创建一个数组，使用迭代函数和一个主种子值</title>
</head>
<body>
```

## JavaScript 代码：

```javascript
const roads = [
  "Post Office-Alice's House",
  "Alice's House-Bob's House",
  "Bob's House-Daria's House",
  "Daria's House-Ennie's House",
  "Ennie's House-Grete's House",
  "Grete's House-Shop",
  "Shop-Marketplace",
  "Marketplace-Town Hall"
];

function buildGraph(borders) {
  let graph = Object.create(null);
  function addEdge(from, to) {
    if (graph[from] == null) {
      graph[from] = [to];
    } else {
      graph[from].push(to);
    }
  }
  for (let [from, to] of borders.map(r => r.split("-"))) {
    addEdge(from, to);
    addEdge(to, from);
  }
  return graph;
}

const roadGraph = buildGraph(roads);
```

## 第 8 章：机器人

在本章中，机器人将在村庄中行走。多个地方有不同的包裹。机器人到达时接收包裹，并在到达目的地时交付。当所有任务执行完毕后，所有包裹都必须交付。如果你想复制这个过程，描述一个可以定义它的虚拟世界。该方法揭了机器人的位置以及包裹。让我们村庄的状态简化为一组描述它的特定值。

```javascript
class VillageState {
  constructor(place, parcels) {
    this.place = place;
    this.parcels = parcels;
  }
  move(destination) {
    if (!roadGraph[this.place].includes(destination)) {
      return this;
    } else {
      let parcels = this.parcels.map(p => {
        if (p.place != this.place) return p;
        return {place: destination, address: p.address};
      }).filter(p => p.place != p.address);
      return new VillageState(destination, parcels);
    }
  }
}

let first = new VillageState(
  "Post Office",
  [{place: "Post Office", address: "Alice's House"}]
);
```

```javascript
let next = first.move("Alice's House");
console.log(next.place);
// -> Alice's House
console.log(next.parcels);
// -> []
console.log(first.place);
// -> Post Office
```

### 持久数据

不可更改的数据布局被称为不可变数据或持久化数据。它们的行为类似于字符串和数字。在 JavaScript 中，你可以改变几乎一切。这里有一个名为 `Object.freeze` 的函数，它可以转换一个对象，使其忽略对其属性的写入。

```javascript
let object = Object.freeze({value: 5});
object.value = 10;
console.log(object.value);
```

```javascript
// -> 5
```

### 模拟

送货机器人会观察世界并决定移动的方向。因此，机器人是一个函数，它接收一个 `VillageState` 对象并返回附近地点的名称。机器人返回一个包含其意图方向和内存值的对象，内存值将在下次调用它时返回。

```javascript
function runRobot(state, robot, memory) {
  for (let turn = 0; ; turn++) {
    if (state.parcels.length == 0) {
      console.log(`Done in ${turn} turns`);
      break;
    }
    let action = robot(state, memory);
    state = state.move(action.direction);
    memory = action.memory;
    console.log(`Moved to ${action.direction}`);
  }
}
```

机器人在每一回合都可以向不同的方向。

它可以遇到所有的包裹，然后到达送货点。

以下是一个示例：

```javascript
function randomPick(array) {
  let choice = Math.floor(Math.random() * array.length);
  return array[choice];
}
function randomRobot(state) {
  return {direction: randomPick(roadGraph[state.place])};
}
```

如果你想测试这个独特的机器人，可以创建一个带有少量包裹的状态。

```javascript
VillageState.random = function(parcelCount = 5) {
  let parcels = [];
  for (let i = 0; i < parcelCount; i++) {
    let address = randomPick(Object.keys(roadGraph));
    let place;
    do {
      place = randomPick(Object.keys(roadGraph));
    } while (place == address);
    parcels.push({place, address});
  }
  return new VillageState("Post Office", parcels);
};
```

当它获得正确的地址时，循环继续选择新的地点。

让我们启动一个虚拟世界。

```javascript
runRobot(VillageState.random(), randomRobot());
// → Advances to Marketplace
// → Advances to Town Hall
// ...
// → 在 63 回内运行
```

机器人运输包裹花费了太多回合，因为没有先做好计划。

### 邮政车的路线

如果你搜索一条经过村庄所有地点的路线，机器人可能会运行两次，但可以保证它会运行这条。以下是一个示例：

（从邮局开始）：

```javascript
const mailRoute = [
  "Alice's House," "Cabin", "Alice's House", "Bob's House",
  "Town Hall," "Daria's House", "Ernie's House",
  "Grete's House", "Shop", "Grete's House", "Farm",
  "Marketplace", "Post Office"
];
```

要使用这条路线，你需要利用机器人内存。路线的其余部分存储在内存中，并在每一回合分发第一个元素。

```javascript
function routeRobot(state, memory) {
  if (memory.length == 0) {
    memory = mailRoutes;
  }
  return {direction: memory[0], memory: memory.slice(1)};
}
```

现在机器人更快了。它最多需要 26 回合（13 步路线的两倍），但通常更少。

### 路径规划

一种有趣的方法是从起点开始开发路线，并检查每个未访问过的可用地点直到达到目标。下面的插图解释了这一点：

```javascript
let work = [{at: from, route: []}];
for (let i = 0; i < work.length; i++) {
  let {at, route} = work[i];
  for (let location of graph[at]) {
    if (place == to) return route.concat(location);
    if (work.some(w => w.at == location)) {
      work.push({at: place, route: route.concat(location)});
    }
  }
}
```

该函数保存了一个工作列表。这是一个下一个要检查的地点数组，连同路线。它从一个空路线和起始位置开始。每个地点都可以从每个地点到达，因此在两点之间也可以找到路线，所以路线不会失败。

```javascript
function goalOrientedRobot(location, parcel, routes) {
  if (route.length == 0) {
    let parcel = parcel[0];
    if (parcel.location != place) {
      route = findRoute(roadGraph, location, parcel.place);
    } else {
      route = findRoute(roadGraph, location, parcel.address);
    }
    return {direction: routes[0], memory: routes.slice(1)};
  }
}
```

### 总结

在本章中我们接触了：

- 持久数据
- 模拟
- 路径规划
- 调试
- 测试

如果你想获取更多关于执行的信息，在程序中添加一些 `console.log` 调用是一个很好的方法。我们希望 `n` 获得值 13、1 然后 0。我们应该在循环开始时输出值：

```
13
1.3
0.13
0.013-323
```

将 13 除以 10 不会得到整数。我们需要的不是 `n /= base`，而是 `n = Math.floor(n / base)`，这样数字就可以向右“移动”。

另一种指定断点点的好方法是在程序中插入一个调试器语句（关键字）。如果你的浏览器处于激活状态，开发者工具将捕获它，并在程序运行到该语句时随时暂停。

## 异常

当函数无法继续执行时，异常处理是理解如何解决该问题的地方。异常是一种工具，允许遇到困难的代码块抛出异常，而异常可以是任何值。你可以刻意在你的代码行中创建问题，以便在执行过程中捕获异常，然后你可以利用它来解决问题并继续工作。

这是一个示例：

```javascript
function promptDirection(question) {
  let result = prompt(question);
  if (result.toLowerCase() == "left") return "L";
  if (result.toLowerCase() == "right") return "R";
  throw new Error("Invalid direction: " + result);
}
function look() {
  if (promptDirection("Which way?") == "L") {
    return "a house";
  } else {
    return "two angry bears";
  }
}
try {
  console.log("You see", look());
} catch (error) {
  console.log("Something went wrong: " + error);
}
```

使用 `throw` 关键字抛出异常。

### 异常后的清理工作

异常的影响是一种不同类型的控制流。这表明你的代码可能会产生不同的副作用，但异常可以阻止这些的发生。以下是一些糟糕的银行代码：

```javascript
const accounts = {
  a: 100,
  b: 0,
  c: 20
};
function getAccount() {
  let accountName = prompt("Enter an account name");
  if (!accounts.hasOwnProperty(accountName)) {
    throw new Error(`No such account: ${accountName}`);
  }
  return accountName;
}
function transfer(from, amount) {
  if (accounts[from] < amount) return;
  accounts[from] -= amount;
  accounts[getAccount()] += amount;
}
```

`transfer` 函数用于将特定金额从指定账户发送到另一个账户，并请求另一个账户的名称。如果你输入错误的账户名称，`getAccount` 会输出异常。如果钱已经从第一个账户发出，但在程序将钱转入另一个账户之前输出异常，钱就会消失。解决这个问题，请利用 `finally` 块代码。如下所示：

```javascript
function transfer(from, amount) {
  if (accounts[from] < amount) return;
  let progress = 0;
  try {
    accounts[from] -= amount;
    progress = 1;
    accounts[getAccount()] += amount;
    progress = 2;
  } finally {
    if (progress == 1) {
      accounts[from] += amount;
    }
  }
}
```

### 选择性捕获

当异常到达代码块底部的错误时，它将由环境处理。无效的使用，例如在 `null` 上检查属性、引用不存在的绑定或调用非函数，将导致抛出异常。这些异常可以被捕获。JavaScript 不支持选择性捕获异常。以下是一个示例，尝试继续调用 `promptDirection` 直到提供有效答案：

```javascript
for (;;) {
  try {
    let dir = promptDirection("Where?"); // ← 写错误！
    console.log("You select " + dir);
    break;
  } catch (e) {
    console.log("Invalid direction. Try again.");
  }
}
```

`for(;)` 结构用于构建一个不能自动终止的循环。当你获得有效方向时，可以使用 `break` 跳出循环，但拼写错误的 `promptDirection` 将输出未定义变量错误。如果你想捕获特定类型的异常，请在 `catch` 块中检查获取的异常是否是你想要的异常，并重新抛出它。让我们描述一种新错误并利用 `instanceof` 来识别它。

```javascript
class InputError extends Error {}

function promptDirection(question) {
  let result = prompt(question);
  if (result.toLowerCase() == "left") return "L";
  if (result.toLowerCase() == "right") return "R";
  throw new InputError("Invalid direction: " + result);
}
```

新的错误类继承了 `Error`。它没有描述自己的构造函数，而是继承了 `Error` 构造函数，该函数预期一个我们可以识别的字符串消息。现在循环可以更仔细地捕获这些异常了。

```javascript
for (;;) {
  try {
    let dir = promptDirection("Where?");
    console.log("You chose ", dir);
    break;
  } catch (e) {
    if (e instanceof InputError) {
      console.log("Invalid direction.");
    } else {
      throw e;
    }
  }
}
```

### 总结

`for(;)` 结构用于构建一个不能自动终止的循环。当你获得有效方向时，可以使用 `break` 跳出循环，但拼写错误的 `promptDirection` 将输出未定义变量错误。如果你想捕获特定类型的异常，请在 `catch` 块中检查获取的异常是否是你想要的异常，并重新抛出它。

## 第 9 章：正则表达式

```javascript
// -> true
console.log(/\d+*/.test(""));
```

```javascript
// -> false
console.log(/\d+*/.test("123"));
```

```javascript
// -> true
console.log(/\d**/.test(""));
```

星号 (*) 允许模式匹配零次。在下例示例中，允许该字符出现，但在未找到该字符时模式同样视为匹配。

```javascript
let neighbor = /neighbour/
console.log(neighbor.test("neighbor"));
```

```javascript
// -> true
console.log(neighbor.test("neighbor"));
```

要确定一个模式应该执行多少次，请使用大括号 `{}`，在元素后插入 `{4}`。如果你想让它精确执行四次，可以定义如下范围：`{2,4}` 表示该元素必须执行两次且最多执行四次。下面是另一个日期和时间模式，它同时允许单双数字的日期、月份和小时。

```javascript
let dateTime = /\d{0,2}-\d{1,2}-\d{4} \d{1,2}:\d{2}/
console.log(dateTime.test("01-30-2003 8:45"));
```

```javascript
// -> true
```

### 分组子表达式

如果你想对一个或多个元素并发使用运算符 `*` 或 `+`，请使用括号。正则表达式中用括号括起来的部分，只要涉及运算符，就被视为一个独立的元素。

```javascript
let cartoonCrying = /boo+(hoo+)/i;

console.log(cartoonCrying.test("Boohoooohoohoo"));
```

```javascript
// → true
```

第一个和第二个字符仅适用于 `boo` 和 `hoo` 中的第二个字符。第三个 `+` 指向整个分组 `(hoo+)`，表示一个或多个连续的。示例中第一个表达式结尾的 `/i` 用于忽略大小写，使其能够匹配输入字符串中的大写 `B`，尽管模式完全是小写的。

### 匹配与分组

`test` 方法是匹配正则表达式的最佳方法，它只确定是否匹配。正则表达式包含一个 `exec` (执行) 方法，如果找不到匹配项，它将输出 `null`，并返回一个包含匹配数据的对象。

```javascript
let match = /\d+.exec("one two 100");
console.log(match);
```

```javascript
// → ["100"]
```

```javascript
console.log(match.index);
```

```javascript
// → 8
```

`exec` 返回的对象包含一个 `index` 属性，它决定了匹配从字符串哪个部分开始。下面是所需的数字：

字符串值包含一个 `match` 方法，其行为类似。

```javascript
console.log("one two 100".match(/\d+/));

// -> ["100"]
```

当正则表达式持有用括号整理的子表达式时，匹配文本将显示在数组中。整个匹配是第一个，下一个是第一个分组匹配的部分，然后是后续的分组，以此此类推。

```javascript
let quotedText = /'([^"]*)'/;

console.log(quotedText.exec("she said 'hello'"));

// -> ["hello'", "hello"]
```

当一个分组未完成匹配（如果它包含问号 `?`），它会输出 `undefined`。当你多次匹配一个分组时，只有最后一次匹配会在数组中完成。

```javascript
console.log(/(badly)?\.exec("bad"));

// -> ["bad", undefined]

console.log(/(\d+)/.exec("123"));

// -> ["123", "3"]
```

### 日期类

JavaScript 包含一个表示日期的标准类；称为 `Date`。如果你想利用 `new` 构建日期对象，请先获取当前的时刻。

```javascript
console.log(new Date());

// -> Mon Nov 11 2023 16:19:11 GMT+0100 (CET)
```

你也可以为特定时间构建对象。

```javascript
console.log(new Date(2008, 11, 8));

// -> Wed Dec 08 2008 00:00:00 GMT+0100 (CET)

console.log(new Date(2008, 11, 9, 12, 59, 999));

// -> Wed Dec 08 2009 12:59:59 GMT+0100 (CET)
```

你应该遵循 JavaScript 日期命名规范，其中月份数字从零开始（因此，12月是 11），日期数字从1开始。

小时、分钟、秒和毫秒参数是可选的，在未指定时被识别为零。时间戳保存为 UTC 时区的毫秒数。后续遵循由“Unix 时间”设定的约定。

```javascript
console.log(new Date(2016, 11, 14).getTime());

// -> 1445677600000
```

```javascript
console.log(new Date(1445677600000));

// Mon Dec 11 2008 00:01:00 GMT+0100 (CET)
```

当 `Date` 构造函数被设置单个参数时，该参数会被识别为时间戳。

```javascript
return code.replace(/\/\.*\/\*[^*\]*\*/g, "");
}
console.log(stripComments("1 + /* 2 */3"));
// → 1 + 3
```

`stripComments` 函数从字符串中移除注释。它使用正则表达式来查找并将块注释替换为空字符串。正则表达式 `\/\.*\/\*[^*\]*\*/g` 匹配任何以 `/*` 开头并以 `*/` 结尾的字符串。`g` 标志确保替换所有出现，而不仅仅是第一个。然而，这个正则表达式是贪婪的，它会从字符串中的第一个 `/*` 到最后一个 `*/`。为了修复这个问题，我们使用懒散量符 `*?`。

```javascript
function stripComments(code) {
  return code.replace(/\/\*[\s\S]*?\*\//g, "");
}
console.log(stripComments("1 + /* 2 */3"));
// → 1 + 3
```

### 动态创建 RegExp 对象

`RegExp` 构造函数允许你动态创建正则表达式对象。当模式在运行时尚未知时，这种方法非常有用。

```javascript
let name = "harry";
let text = "Harry is a suspicious character.";
let regexp = new RegExp(name, "gi");
console.log(text.replace(regexp, "_$&"));
// → _Harry is a suspicious character.
```

### search 方法

`search` 方法返回字符串中第一个匹配项的索引。你也可以使用 `indexOf` 方法，它返回首次看到表达式的索引，如果未找到则返回 -1。

```javascript
console.log(" word".search(/\S/)); // → 2
console.log(".search(/\S/)); // → -1
```

`lastIndex` 方法并没有提供一种更好的方法来从字符串的指定位置开始搜索。正则表达式对象包含属性。其中一个属性是 `source`，它由构建表达式的字符串组成。`lastIndex` 是另一个属性，它影响下一次匹配开始的某些情况。正则表达式必须包含 `g` 或 `y` 标志，`lastIndex` 才会起作用。

```javascript
let pattern = /a/g;
let str = "baacad";
pattern.lastIndex = 2;
console.log(pattern.exec(str)); // {0: "a", index: 2, input: "baacad"}
```

由它们的语言组成，并利用它展示这些模式。

| 正则表达式 | 描述 |
| :--- | :--- |
| `/ABC/` | 连续的字符 |
| `/[abc]/` | 范围内的字符 |
| `[^abc]` | 不在范围内的任何字符 |
| `/[0-9]/` | 字符集中的任何字符 |
| `/x+/` | 模式 x 的一次或多次匹配 |
| `/x+?` | 一次或多次匹配，非贪婪 |
| `/x*/` | 零或多次匹配 |
| `/x?` | 零或一次匹配 |
| `/x{2,4}/` | 两次到四次匹配 |
| `/(ABC)/` | 分组 |
| `/\|a\|b\|c/` | 各种模式中的任意一个 |
| `/\d/` | 任意数字字符 |
| `/\w/` | 单词字符 |
| `/\s/` | 任意空白字符 |
| `/./` | 除换行符外的任何字符 |
| `/\b/` | 单词边界 |
| `/\^/` | 输入开始 |
| `/$/` | 输入结束 |

正则表达式包含一个 `test` 方法，用于检查字符串是否匹配它。它还包含一个 `exec` 方法，当它找到匹配项时，它会返回一个包含每个匹配组的数组。这种数组包含一个 `index` 属性，指定匹配开始的位置。字符串使用 `match` 方法与正则表达式进行匹配，并使用 `search` 方法来查找匹配项，仅返回匹配的起始位置。

### 练习

编写一个作为 `trim` 函数（字符串）的 JavaScript 程序，利用正则表达式。

### 解决方案

HTML 代码：

```html
1 <!DOCTYPE html>
2 <html>
3 <head>
4 <meta charset="utf-8" />
5 <title>使用正则表达式的修剪函数</title>
6 </head>
7 <body>
8 </body>
9 </html>
```

JavaScript 代码：

```javascript
1 function Trim(str)
2 {
3   var result;
4   if (typeof str === 'string')
5   {
6     result = str.replace(/^\s+|\s+$/g, '');
7     return result;
8   }
9   else
10  {
11    return false;
12 }
13 }
14 console.log(Trim(' w3resource '));
```

## 第 11 章：模块

这个特定的程序具有简单的布局。解释它的概念非常容易，每个部分都起着精确的作用。布局的组织和维护可能会花费更多工作，但当将来有人使用该程序时，最终会有回报的。因此，你可能会好奇于忽略它并让程序部分相互混合，这将产生两个实际问题。首先，当所有内容都相互接触时，很难单独查看任何一组组件。你必须对整个程序有一个全面的理解。其次，在不同情况下使用程序的任何功能时，你可以重写它，而不是将其从上下文中分离。

### 模块

模块是一种程序类型，决定了哪些部分应该依赖于什么，以及它应该为其他部分产生什么功能。通过限制模块相互通信的方式，系统就像乐高一样，组件之间使用简单的连接器进行通信，而不是像泥巴那样整个组件混合在一起。依赖是模块之间的关系。当一个模块想要从另一个模块获取内容时，它就依赖于该模块。模块本身说明了这一事实，并用于确定哪些其他模块可以供指定的模块使用，并自动加载依赖。每个模块都需要自己的作用域来与其他模块隔离开。

### 软件包

由不同组件构建程序并能够单独启动这些组件的一个显著优势是，你可以将同一个组件应用于不同的程序中。当代码开始重复时，软件包就派上了用场。包是一个可以共享的代码块。它可能由一个或多个模块组成，并持有有关其他相关依赖包的信息。包还包含描述其函数的文档，以便没有编写它的人可以使用它。当包中出现问题或你添加新功能时，包会自动更新。现在，程序依赖于这些更新将包升级到最新版本。像这样工作，你需要基础设施。一个保存和搜索包的地方，以及一种升级和安装它们的简单方法。在 JavaScript 中，NPM 提供了支持。

将 NPM 分为两个部分：一个可以上传和下载包的在线服务，以及一个处理安装和管理的程序。NPM 上的几乎所有代码都经过许可。

### 仿制模块

在 2015 年之前，JavaScript 语言不包含任何内置模块系统，但人们使用 JavaScript 创建大型系统已经超过十年了，而且他们需要模块。他们开发了自己的模块系统并将其集成到语言中。你可以利用 JavaScript 函数来构建局部作用域和对象来代表模块布局。使用此模块在星期名称和数字之间转换。它的布局包含 `weekDay.Name` 和 `weekDay.number`，并将局部绑定名称隐藏在函数的作用域内。

该表达式被立即调用。

```javascript
const weekDay = function() {
  const names = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
  return {
    name: function(number) { return names[number]; },
    number: function(name) { return names.indexOf(name); };
  };
};
console.log(weekDay.name(weekDay.number("Sunday")));
// → Sunday
```

这种风格的模块不声明依赖关系。它们将布局放入全局作用域。这种风格的模块提供了全局作用域，但它没有声明依赖。相反，它只是将布局放入全局作用域。

### 执行代码

有不同的方法使用 `Function` 构造函数来执行代码。执行代码的最佳方法是全局 `eval` 函数。

```javascript
let x = 1;
function evalAndX(code) {
  return x;
}
console.log(evalAndX("2"));
// -> 2
```

另一种不复杂的方法是使用 `Function` 构造函数执行代码。它接受两个参数，字符串和主体。

```javascript
let plusOne = Function("n", "return n + 1");
console.log(plusOne(4));
// -> 5
```

### CommonJS

JavaScript 模块使用的常用方法是 CommonJS。Nodejs 以及许多包使用这种方法。CommonJS 模块的主要思想是 `require` 函数。如果你用模块名称调用它，它会加载模块并返回其接口。加载器在函数内部覆盖模块代码，模块自动具有作用域。你可以调用 `require` 来查看它们的依赖并将布局放在输出的对象中。

这个示例模块提供了一个日期格式化函数。它利用了 NPM 的两个包：ordinal 用于将数字转换为 "1st" 和 "2nd" 等字符串，以及 date-names 用于获取月份和工作日的英文名称。它导出单个函数 `formatDate`，接受一个模板字符串和一个 `Date` 对象。模板字符串可以包含控制格式的代码，例如 YYYY（完整年份）和 Do（序数日期）。

```javascript
const ordinal = require("ordinal");
const {days,months} = require("date-names");
exports.formatDate = function(date, format) {
  return format.replace(/YYYY|M(MM)?|Do?|dddd/g, tag => {
    if (tag == "YYYY") return date.getFullYear();
    if (tag == "M") return date.getMonth();
    if (tag == "MMM") return months[date.getMonth()];
    if (tag == "D") return date.getDate();
    if (tag == "Do") return ordinal(date.getDate());
    if (tag == "dddd") return days[date.getDay()];
  });
};
```

ordinal 的布局是一个单一函数，而 date-names 导出一个包含多个其他内容的对象，months 和 days 是名称数组。在构建导入布局的绑定时，解构非常简单。模块将它的布局函数附加到 exports 上，以便依赖它的模块可以访问它。以这种方式使用模块：

```javascript
const {formatDate} = require("./format-date");
console.log(formatDate(new Date(2017, 9, 13), "dddd the Do"));
// → Friday the 13th
```

我们可以按照如下最简单的形式定义 `require`：

```javascript
require.cache = Object.create(null);

function require(name) {
  if (!(name in require.cache)) {
    let code = readFile(name);
    let module = {exports: {}};
    require.cache[name] = module;
    let wrapper = Function("require, exports, module", code);
    wrapper(require, module.exports, module);
  }
  return require.cache[name].exports;
}
```

在这段代码中，`readFile` 是一个功能性函数，它读取文件并将其内容作为字符串返回。标准 JavaScript并不提供这种功能，但像 Node.js 和浏览器等其他 JavaScript 环境提供了访问文件的独特方式。上面的示例假定了 `readFile` 的存在。为了避免重复加载同一个模块，你需要一个存储已加载模块的存储器（缓存）。当被调用时，它会检查请求的模块是否已加载，如果没有，则进行加载。它需要读取模块的代码，将其封装在一个函数中并调用它。

之前提到的包的布局是一个函数而不是对象。CommonJS 模块使用模块系统为你创建一个空布局对象以供你导出，然后通过覆盖 `module.exports` 用值来恢复该对象。模块这样做是为了导出单个值，而不是一个布局对象。通过将 `exports`、`require` 和 `module` 描述为创建的封装函数的参数（并在调用时设置正确的值），加载器确保了这些绑定在模块内部是可用的。

设置为 `require` 的字符串被解释为文件名或网络地址。当它以 `./` 或 `/` 开头时，会被翻译为相对于现有模块的文件名。如果名称不是相对路径，Node.js 将在 node_modules 中搜索安装的包。现在，你不需要自己写文件解析器，可以使用 NPM 上的。

```javascript
const {parse} = require("ini");
console.log(parse("x = 10\ny = 20"));
// → {x: "10", y: "20"}
```

### ECMAScript 模块

CommonJS 模块在与 NPM 结合时表现良好，但对于 JavaScript 社区的扩展来说，这种表示法非常奇怪。添加到 `exports` 中的内容在局部作用域内是不可访问的。如果不运行模块代码，在获取任何参数之前很难确定它的依赖。这就是 JavaScript 建立自己的独立模块系统（称为 ES 模块）的原因，其中依赖和接口的初始想法保持不变，但它们的表示法不同。现在你可以使用唯一的 `import` 关键字来访问依赖，而不是调用函数。

```javascript
import {days} from "date-names";
export function formatDate(date) { /* ... */ }
```

使用 `export` 关键字来导出内容。它可以是一个类、函数或绑定（`let`、`const` 或 `var`）。ES 模块的布局不代表单个值，而是一组绑定。如果你从另一个模块导入内容，该绑定会随之带入，这意味着导出模块的值可以随时发生更改。如果绑定被命名为 `default`，它会被识别为模块的主要值。要开发一个默认导出，请在表达式、类或函数声明之前编写 `export default`。

```javascript
export default ["Winter", "Spring", "Summer", "Autumn"];
```

你可以像这样重命名导入的绑定：

```javascript
import {days as dayNames} from "date-names";
console.log(dayNames.length);
```

另一个主要区别是 ES 模块的导入发生在模块脚本开始运行之前。导入声明可能不会显示在函数或块中，且依赖名称应该是引用字符串而不是任意表达式。许多项目都是通过 ES 模块编写的。

### 模块设计

程序结构化是编程的优良特性之一。任何未知的功能都可以以不同的方式进行建模。良好的程序设计是个性化的，这涉及到偏好和品味的问题。要理解良好设计的价值，你需要阅读并处理几个程序，并注意高效和低效的函数。

模块设计直观且易用。`ini` 包通过提供 `stringify`（用于写入 INI 文件）函数来遵循标准的 JSON 对象，并且像 JSON 一样，在普通对象和字符串之间转换。NPM 上的许多文件解析模块都提供了一个从硬盘读取该类型文件并进行解析的函数。计算值的集中式模块比执行具有副作用的复杂动作的大型模块更适用于广泛的程序。一个读取文件的 INI 读取器在文件内容来自另一个源的情况下是没用的。同样，有状态的对象有时是必要且有用的，但如果你可以使用函数，请利用它。NPM 上的各种文件读取器提供了一种布局风格，需要构建一个对象，然后将文件加载到对象中并并特定方法实现所需的结果。这是面向对象的风格和传统。在 JavaScript 中，没有表示图的特殊方法。NPM 上有各种路径查找包，但没有一个利用图格式的。它们通常允许图边包含权重，即与它相关的距离或成本。例如，我们有 `dijkstra` 包。一种被认可的路径查找方法，与 `findRoute` 函数相关的 Dijkstra 算法源于包的首位作者 Edsger Dijkstra。`.js` 后缀通常附加在包名后以指定你可以在 JavaScript 中编写。如果你想使用该包，请确保图以预期的格式保存。

```javascript
const {find_path} = require("dijkstra");
let graph = {};
for (let node of Object.keys(roadGraph)) {
  let edges = graph[node] = {};
  for (let dest of roadGraph[node]) {
    edges[dest] = 1;
  }
}
console.log(find_path(graph, "Post Office", "Cabin"));
// ["Post Office", "Alice's House", "Cabin"]
```

当多个包使用独立的数据结构来定义相关内容时，组合可能会成为障碍。因此，当你设计可组合的内容时，要确切知道他人使用的数据结构并遵循他们的示例。

### 总结

在本章中，我们涵盖了模块。模块通过将代码划分为具有理解依赖和接口的部分，为更复杂的程序提供了结构。接口是可以使用的模块。

### 练习

编写一个 JavaScript 程序以以下格式显示当前日期和时间：

今天是周二。

当前时间为：10 PM: 30: 38

## 答案

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>JavaScript current day and time</title>
</head>
<body></body>
</html>
```

## 代码：

```javascript
var today = new Date();
var day = today.getDay();
var daylist = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
console.log("Today is " + daylist[day]);
var hour = today.getHours();
var minute = today.getMinutes();
var second = today.getSeconds();
var prepand = (hour < 12) ? "AM" : "PM";
hour = (hour > 12) ? hour - 12 : hour;
if (hour == 0) {
  hour = 12;
  prepand = "AM";
}
console.log("Current time is: " + prepand + " " + hour + ":" + minute + ":" + second);
```

```javascript
else {
  hour=12;
  prepend='AM';
}
console.log("Current Time: " + hour + prepend + ":" + minute + ":" + second);
```

## 第 12 章：异步编程

处理器是计算机中至关重要的部分，它执行平衡我们程序的各个步骤。像循环这种影响数字完成情况的操作速度取决于处理器的速度。许多程序与处理器外部的物体进行通信。例如，它们可能通过计算机网络进行交互，或者要求从硬盘获取数据，而从内存中获取数据要慢得多。在某种，操作系统处理这部分，并在运行的各种程序之间切换处理器。

### 异步性

在异步编程模型中，所有事情都是一次发生一个。如果你调用了一个执行耗时操作的函数，结果只有在操作完成后才会返回。在执行期间，其他操作都无法发生。异步模型允许几件事同时发生。当一个操作开始时，程序不会停止运行。当任务完成时，它会通知程序并允许访问结果（例如从磁盘读取的信息）。你可以通过一个简单的例子来区分同步和异步编程：一个从网络获取两个资源然后合并结果的程序。

在异步环境中，请求函数在工作完成时返回。执行此任务的最简单方法是一个接一个调用请求。它的缺点是只有在第一个任务完成后，才会开始第二个请求。两个响应时间之和将是花费的总时间。为了在同步系统中解决这个问题，请开始添加控制线程。线程是一个运行中的程序，其执行可以通过操作系统与其他程序一起渲染，因为现代计算机有多个处理器，各种线程可以同时在不同的处理器上运行。第二个线程可以开始第二个请求，然后两个线程都等待它们的结果返回，之后，它们会重新同步以合并两个结果。在异步模型中，网络时间是指定控制线程时间线的一部分。在异步模型中，启动一个网络操作（notional）在概念上在时间线上产生了一个划分。启动操作的程序不会停止运行，操作会随之发生，并在其完成时通知程序。

确定相似性的另一种方法是：在同步模型中，等待任务完成是间接的，而在异步的异步模型中，它是直接受我们控制的。

### 回调函数

实现异步编程的一种方法是，允许执行耗时操作的函数获取一个额外的参数，该参数被称为回调函数。当操作开始和结束时，你应该使用回调函数调用结果。例如，浏览器和 Node.js 中都可以使用的 `setTimeout` 函数，它等待指定的毫秒数然后调用一个函数。

```javascript
setTimeout(() => console.log("Tick"), 500);
```

等待并不是理想的工作，但当你运行像动画更新或检查函数耗时是否超过指定时间之类的程序时，它是适用的。通过回调连续运行多个异步任务意味着你必须继续设置新函数，以控制操作后计算的延续。

许多乌鸦巢计算机由一个长期的数据存储球泡组成，数据存储在树枝中，以便以后访问和恢复。存储或搜索某条数据所需的时间短，因此长期存储的布局是异步的并利用了回调函数。存储球泡在名称下保存可以 JSON 编码的数据。乌鸦可以将关于它隐藏的地方的数据以“食物缓存”（food caches）的名称保存，该缓存包含一个指向其他数据片段的名称数组，定义了缓存。要在大橡树巢的存储球泡中寻找食物缓存，乌鸦可以按如下方式运行代码：

```javascript
import {bigOak} from "./crow-tech";
bigOak.readStorage("food caches", caches => {
  let firstCache = caches[0];
  bigOak.readStorage(firstCache, info => {
    console.log(info);
  });
});
```

这种编程风格是可行的，但缩进层会随着每个异步操作而扩大，因为它会导致另一个函数。执行某些困难任务（如并发运行多个操作）可能会变得奇怪。乌鸦巢计算机是为了通过请求-响应对进行交互而。。这意味着巢向另一个巢发送消息，后者立即返回消息，确认接收并将回复附在消息问题上。每条消息都有一个类型标记，这决定了它如何被控制。你的代码可以为某些请求类型描述处理程序，当请求进来时，调用处理程序提供回复。由“/crow-tech”模块导出的布局产生了基于回调的交互函数。巢包含一个 `send` 方法，用于发送请求。它将请求类型、目标巢名称和请求内容作为前三个参数，并期望在回复返回时作为第四个也是最后一个参数的函数被调用。

```javascript
bigOak.send("Cow Pasture", "note", "Let's caw loudly at 7PM", () => console.log("Note delivered."));
```

但为了确保巢可以接收该请求，你必须指定一个名为“note”的请求类型。控制需要运行的请求的代码以及在所有巢中都可以接收这种类型的消息。让我们假设一只乌鸦飞过并在所有巢上安装了它的处理程序代码。

```javascript
import {defineRequest} from "./crow-tech"
defineRequest("note", (nest, content, source, done) => {
  console.log(`${nest.name} received note: ${content}`);
  done();
});
```

`defineRequest` 函数描述了一个新请求。它在 promise 解决（resolve）并提供值时指示一个回调函数。你可以为单个 promise 附加多个回调，它们会调用这些回调，即使它们是在 promise 完成后才附加的。`then` 方法还会返回另一个 promise，该 promise 解析处理程序函数返回的值。将 promise 视为一种将值转换为异步现实的设备是非常重要的。承诺的值是一个未来可能存在或可能在未来某个时刻显示的值。以 promise 描述的计算在闭包的值上运行，并在值可用时异步执行。要构建一个 promise，请使用 `Promise` 作为构造函数。它包含一种奇特的布局，构造函数期望一个函数作为参数，它会立即调用该函数并传递一个可以解决 promise 的函数。这就是为 `readStorage` 函数构建基于 promise 的布局：

```javascript
function storage(nest, name) {
  return new Promise(resolve => {
    nest.readStorage(name, result => resolve(result));
  });
}
storage(bigOak, "enemies")
.then(value => console.log("Got", value));
```

### Promises

当值代表方法时，使用抽象方法工作会更简单。在异步操作的情况下，与其为函数在未来的某个点被调用做准备，不如返回一个代表未来事件的get。promise 是一种异步操作，可以在某点完成并提供值。当它的值可用，它可以通知感兴趣的人。构建 promise 最简单的方法是调用 `Promise.resolve`。此函数保证你设置的值包含一个 promise。如果它已经是一个 promise，则直接返回。否则，将立即创建一个以你的值为结果的新 promise。

```javascript
let fifteen = Promise.resolve(15);
```

```javascript
fifteen.then(value => console.log(`Got ${value}`));
// → Got 15
```

### 失败

JavaScript 计算可以通过输出异常来失败。网络请求可能会失败，或者某些异步代码计算可能会产生异常。异步编程回调风格最常见的问题是，它很难确保失败能正确地揭示给回调函数。一种通用的方法是：回调的第一个参数用于指定失败的操作，第二个参数是操作完成时提供的值。此类回调函数总是会检查它们是否获取了异常，并确保任何出现的问题（包括它们调用的函数输出的异常）都传递给正确的函数。它们可以在成功完成时调用，也可以在失败时拒绝（decline）。

仅在任务成功完成时才调用处理程序（handler），并在失败时自动对返回的新的 promise 产生拒绝。当处理程序输出异常时，这会自动触发其最近调用所提供的 promise 被拒绝。当异步操作链中的某个元素失败时，整个链的输出都会被拒绝，且失败点之后的成功处理程序不会被调用。就像解决一个 promise 会产生一个值一样，拒绝一个 promise 也会提供一个值，通常被称为拒绝原因。如果处理函数中的异常创建了拒绝，则使用异常值作为原因。相应地，当处理程序返回一个被拒绝的 promise 时，该拒绝将进入下一个 promise。有一个 `Promise.Reject` 函数，可以创建一个新的、立即被拒绝的 promise。

如果 catch 处理程序输出了错误，新的 promise 同样会被拒绝。在简写形式中，它也接受一个拒绝处理器作为第二个参数，因此你应该在单个方法调用中安装两种类型的处理程序。发送到 `Promise` 构造函数的函数接受第二个参数，与 `resolve` 函数一起，它可以使用它来拒绝新的 promise。通过调用 `then` 和 `catch` 识别并开发的 promise 值链被视为流水线，异步值或失败在其中通过。由于这些链是通过注册处理程序构建的，每个链接都由一个成功处理器或一个与之相关的拒绝处理器组成。与输出拒绝类型不匹配的处理程序不会被调用。但匹配的程序会被调用，它们的输出决定了下一个值的值的类型：当返回非 promise 值时是成功，输出异常时是拒绝，当返回其中一个 promise 时是该 promise 的结果。

```javascript
new Promise((resolve, reject) => reject(new Error("Fail")))
.then(value => console.log("Handler 1"))
.catch(reason => {
console.log("Caught failure " + reason);
  return "nothing";
})
.then(value => console.log("Handler 2", value));
// -> Caught failure Error: Fail
// -> Handler 2 nothing
```

### 网络是困难的

周期，乌鸦的镜面系统很少有光线来传达信号阻塞了信号路径。信号被传输但被拒绝是可行的。通常，传输失败是意外的事故，比如汽车大灯阻挡了光信号，重新发送请求就能使其成功。所以，让我们创建我们的请求函数，并在停止之前多次重试发送请求。而且，既然我们已经建立了 promise 是好的，我们也将确保我们的请求函数返回一个 promise。在它们能指示什么方面，promise 和回调是平等的。基于回调的函数被封装以揭示基于 promise 的布局，反之亦然。即使请求的回复成功传达，回复也可能指定失败，例如，如果请求尝试使用未描述的请求类型，或者处理程序输出了错误。为了辅助这一点，`send` 和 `defineRequestType` 遵循之前声明的约定，发送到回调的第一个参数是失败的原因（如果有），第二个参数是确定的结果。我们的封装类将它们解释为 promise 的解析和拒绝。

```javascript
class Timeout extends Error {}

function request(nest, target, type, content) {
  return new Promise((resolve, reject) => {
    let done = false;
    function attempt(n) {
      nest.send(target, type, content, (failed, value) => {
        done = true;
        if (failed) reject(failed);
        else resolve(value);
      });
      setTimeout(() => {
        if (done) return;
        else if (n < 3) attempt(n + 1);
        else reject(new Timeout("Timed out"));
      }, 250);
    }
    attempt(1);
  });
}
```

因为 promise 只能被接受或拒绝一次，所以它可以工作。第一次调用 `resolve` 或 `reject` 决定了 promise 的结果，任何其他调用都会被忽略。为了创建一个重试的异步循环，使用递归函数，高效的循环不允许我们停止并等待异步操作。`attempt` 函数创建了传输请求的单次尝试。它还指定，如果在 250 毫秒后有返回响应，则开始下一次尝试；或者如果是第四次尝试，则以 `Timeout` 实例作为原因拒绝 promise。每四分之一重试一次并在一秒后无响应时停止，如果请求出现这无疑是任意的，但处理程序让请求传输几次需要更长的时间。请带着这个问题创建你的处理程序，并且耦合的消息是无害的。为了完全将回调隔离开来，为 `defineRequestType` 定义一个封装，允许处理函数返回一个 promise 或简单值，并接线为我们执行回调。

```javascript
function requestType(name, handler) {
  defineRequestType(name, (nest, content, source, callback) => {
    try {
      Promise.resolve(handler(nest, content, source))
        .then(response => callback(null, response),
        failure => callback(failure));
    } catch (exception) {
      callback(exception);
    }
  });
}
```

`Promise.resolve` 用于如果处理程序返回的值尚未准备就绪，将其转换为 promise。

### Promise 集合

每个 nest 计算机在其邻居的属性的传输距离内存储一个其他 nest 的数组。为了检查哪些是可达的，编写一个函数向它们所有项发送 "ping" 请求（要求响应的请求）并检查哪些返回了结果。如果你正在处理一组同时运行的 promise，`Promise.all` 函数非常重要。它返回一个 promise，该 promise 等待数组中的所有 promise 协调，然后就一个为这些 promise 提供的值的数组。如果任何 promise 被拒绝，`Promise.all` 的结果也会被拒绝。

```javascript
requestType("ping", () => "pong");

function availableNeighbors(nest) {
  let requests = nest.neighbors.map(neighbor => {
    return request(nest, neighbor, "ping")
      .then(() => true, () => false);
  });
  return Promise.all(requests).then(results => {
    return nest.neighbors.filter((_, i) => results[i]);
  });
}
```

### 网络泛洪

nests 只能与其邻居通信，这极大地影响了网络的显著性。为了向整个网络广播信息，解决方案是创建一个自动发送给邻居的请求类型。这些邻居再将其发送给它们的邻居，直到整个网络收集了该消息。

```javascript
import {everywhere} from "./crow-tech";

everywhere(nest => {
  nest.state.gossip = [];
});
```

```javascript
function sendGossip(nest, message, exceptFor = null) {
  nest.state.gossip.push(message);
  for (let neighbor of nest.neighbors) {
    if (neighbor == exceptFor) continue;
    request(nest, neighbor, "gossip", message);
  }
}

requestType("gossip", (nest, message, source) => {
  if (nest.state.gossip.includes(message)) return;
  console.log(`${nest.name} receive gossip '${message}' from ${source}`);
  sendGossip(nest, message, source);
});
```

### 消息路由

如果一个节点想要与另一个节点通信。最好的方法是构建一条路径让消息在节点之间跳转直到到达目的地。你需要理解网络的接口。向远处的 nest发送请求，重要的是知道哪个邻居知道它的直接邻居，它无法计算路由，因为它缺乏信息。你必须理解如何将这些连接的信息传播到每个 nest，并使其能够随着时间（在新 nest 创建时）转换。现在你可以使用泛洪，但不是检查消息是否已被收集，而是检查给定 nest 的新邻居集合是否与当前集合相似。

```javascript
requestType("connections", nest, {name, neighbors}, source) => {
  let connections = nest.state.connections;
  if (JSON.stringify(connections.get(name)) == JSON.stringify(neighbors)) return;
```

```javascript
connections.set(name, neighbors);
broadcastConnections(nest, name, source);
}

function broadcastConnections(nest, name, exceptFor = null) {
  for (let neighbor of nest.neighbors) {
    if (neighbor == exceptFor) continue;
    request(nest, neighbor, "connections", {
      neighbors: nest.state.connections.get(name)
    });
  }
}

everywhere(nest => {
  nest.state.connections = new Map;
  nest.state.connection.set(nest.name, nest.neighbors);
  broadcastConnections(nest, nest.names);
});
```

这种比较使用了 `JSON.stringify`，因为在对象或数组上使用 `==` 时，如果两个值相同将返回 `true`。通过区分 JSON 字符串是比较内容的一种非常有效的方法。节点会立即开始传输它们的连接（无法到达的巢穴除外），巢穴会为它们提供现有网络图的映射。`findRoute` 函数寻找通往网络中某个节点的路径。但它并不返回整个路由，而是只返回下一步。下一个巢穴将使用其关于网络的现有信息，决定将消息传输到哪里。

```javascript
function findRoute(from, to, connections) {
  let work = [{at: from, via: null}];
  for (let i = 0; i < work.length; i++) {
    let {at, via} = work[i];
    for (let next of connections.get(at) || []) {
      if (next == to) return via;
      if (!work.some(w => w.at == next)) {
        work.push({at: next, via: via || next});
      }
    }
  }
  return null;
}
```

你现在可以创建一个可以发送远距离消息的函数。如果消息附加在直接邻居上，它将像常一样传递。如果没有，它将被封装在一个对象中，并通过 "route" 请求类型传输到更靠近目标的邻居处，这将让该邻居重复相同的操作。

```javascript
function routeRequest(nest, target, types, content) {
  if (nest.neighbors.includes(target)) {
    return request(nest, target, types, content);
  } else {
    let via = findRoute(nest.name, target, nest.state.connections);
    if (!via) throw new Error(`No routes to ${target}`);
    return request(nest, via, "route", {target, type, content});
  }
}

requestType("route", (nest, {target, type, content}) => {
  return routeRequest(nest, target, type, content);
});
```

我们在主通信系统的顶层创建了不同层的功能以便于使用。这是计算机网络工作的一种简化模型。

### 异步函数 (Async functions)

为了保存大量信息，乌鸦使用复制方法，它们在各个巢穴之间进行复制。这样，当某只鸟拆除巢穴时，信息就不会丢失。为了恢复没有存储球的特定信息，巢穴计算机将与网络中的随机巢穴对话，直到找到拥有的那一个。

```javascript
requestType("storage", (nest, name) => storage(nest, name));

function findInStorage(nest, name) {
  return storage(nest, name).then(found => {
    if (found != null) return found;
    else return findInRemoteStorage(nest, name);
  });
}

function network(nest) {
  return Array.from(nest.state.connections.keys());
}

function findInRemoteStorage(nest, name) {
  let sources = network(nest).filter(n => n != nest.name);
  function next() {
    if (sources.length == 0) {
      return Promise.reject(new Error("Not found"));
    } else {
      let source = sources[Math.floor(Math.random() * sources.length)];
      sources = sources.filter(n => n != source);
      return routeRequest(nest, source, "storage", name)
        .then(value => value != null ? value : next());
    }
  }
  return next();
}
```

`Object.keys` 无法作用于 connections，因为它是一个 Map。它包含一个 `key` 方法，但该方法返回的是迭代器而不是数组。可以使用 `Array.from` 函数将迭代器转换为数组。各种异步操作以不的方式结合在一起。现在你需要一个递归函数来模拟跨巢穴的循环。在同步编程模型中，这很容易表达。JavaScript 还允许你编写伪同步代码来定义异步计算。`async` 函数是一个完全返回 promise 的函数，并且可以以同步的方式等待其他 promise。像这样重写 `findInStorage`：

```javascript
async function findInStorage(nest, name) {
  let local = await storage(nest, name);
  if (local != null) return local;
  let sources = network(nest).filter(n => n != nest.name);
  while (sources.length > 0) {
    let source = sources[Math.floor(Math.random() * sources.length)];
    sources = sources.filter(n => n != source);
    try {
      let found = await routeRequest(nest, source, "storage", name);
      if (found != null) return found;
    } catch (_) {
    }
  }
  throw new Error("Not found");
}
```

异步函数用 `async` 单词标记，然后通过在名称前编写 `async`，该函数也可以变成异步的。当函数或方法被调用时，它会返回一个 promise。当体返回某些内容时，promise 变为完成（settled）。如果它输出异常，promise 变为拒绝（rejected）。在异步函数内部，`await` 单词设置在表达式前面，以等待 promise 变为完成，然后继续执行函数。此类函数无法一次从头运行到尾，但可以在某些点冻结并在稍后重启。对于复杂的异步代码，这种表示法比直接通过 promise 要容易得多。

### 生成器 (Generators)

异步函数不需要暂停然后再次恢复。JavaScript 包含一种名为生成器函数（generator functions）的特性。它们是，但不包含 promise。当你使用 `function*`（在 `function` 单词后加星号）调用函数时，它就变成了一个生成器。当你调用生成器时，它会返回一个迭代器。

```javascript
function* powers(n) {
  for (let current = 1; current < n; current *= 2) {
    yield current;
  }
}

const it = powers(10);
console.log(it.next().value); // 1
console.log(it.next().value); // 2
console.log(it.next().value); // 4
console.log(it.next().value); // 8
```

不需要构建一个对象来持有状态，生成器会存储它们的局部状态。编写带有迭代器的 Group 类：

```javascript
Group.prototype[Symbol.iterator] = function*() {
  for (let i = 0; i < this.members.length; i++) {
    yield this.members[i];
  }
}
```

Promise 的解析（resolve）或拒绝（reject）作为一个新事件发生。即使 promise 已经解析，等待它也会让你的回调在现有脚本执行完成后运行，而不是立即执行。

```javascript
Promise.resolve("Done").then(console.log);
console.log("Me first!");
// -> Me first!
// -> Done
```

### 异步 bug

当你同步运行程序时，除了程序本身的执行之外，没有发生指定的转换。但当你运行异步程序时，情况就不同了。它们在执行过程中可能包含其他代码可以利用的隙。下面是一个示例。我们乌鸦最喜欢的事情之一是统计每年村子里出生的雏鸟数量。鸟巢在它们的存储泡中保存这些计数。以下代码尝试统计某一年每个巢的计数：

```javascript
function anyStorage(nest, source, name) {
  if (source == nest.names) return storage(nest, name);
  else return routeRequest(nest, source, "storage", name);
}

async function chicks(nest, year) {
  let list = "";
  await Promise.all(network(nest).map(async name => {
    list += `${name}: ${await anyStorage(nest, names, `chicks in ${year}`)}\n`;
  }));
  return list;
}
```

`async name =>` 显示通过在前面放置 `async` 单词，箭头函数也可以变成异步的。代码在整个巢集合上绘制异步箭头函数，构建一个 promise 数组，并利用 `Promise.all` 在返回创建的列表之前进行等待。它是坏的。它只会返回单行输出，列出响应最慢的巢。你知道为什么吗？

问题出在 `+=` 运算符上，它在语句开始执行时获取 `list` 的当前值，并在等待结束时，将 `list` 绑定设置为该值加上添加的字符串。但在语句的开始和结束之间，存在一个异步间隙。`map` 表达式是第一个运行的，在你向列表添加任何内容之前运行，因此每个 `+=` 运算符都从空字符串开始，并在其检索存储完成时结束。像往常一样，它在一个无错误的过程中计算新值，而不是转换现有值。

```javascript
async function chicks(nest, year) {
  let lines = network(nest).map(async name => {
    return name + ": " + await anyStorage(nest, names, `chicks in ${year}`);
  });
  return (await Promise.all(lines)).join("\n");
}
```

犯错是避免的，特别是在使用 `await` 期间，你应该知道代码中的间隙在哪里。

### 总结

我们在本章中学习了关于异步编程的所有知识。异步编程允许表达等待长时间运行的操作，而不会在整个操作过程中给程序带来问题。JavaScript 环境通常通过回调使用这种编程风格，回调是在操作结束时调用的函数。我们还提到了事件循环。事件循环为这些回调创建了一个计划，在合适的时候一个接一个地调用它们，以避免重叠。

### 练习

编写一个 JavaScript 程序，将一个异步函数转换为返回 promise 的函数。

### 解决方案

## HTML 代码：

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>将异步函数转换为返回 promise 的函数</title>
</head>
<body>
</body>
</html>
```

## JavaScript 代码：

```javascript
//Source https://bit.ly/2neWfJ2
const promisify = func => (...args) =>
  new Promise((resolve, reject) =>
    func(...args, (err, result) => (err ? reject(err) : resolve(result))));
const delay = promisify((d, cb) => setTimeout(cb, d));
delay(2000).then(() => console.log('Hi!')); // Promise 在 2 秒后解析
```

## 第 13 章：解析

开发自己的编程语言相对容易且非常令人。本章将教你如何构建你的语言。我们将创建一个名为 Egg 的编程语言。一种短小而简单的语言仍然足够强大，可以表达任何思考的计算。它允许确定的纯抽象函数。

### 解析

编程语言中显著的部分是记法和语法。解析器（parser）是一个读取文本并提供数据布局的程序，该反映反映文本中程序的布局。如果文本无法创建有效程序，解析器将指示错误。我们的语言将包含精确且统一的语法。Egg 中包含的所有内容都是表达式（expression）。表达式可以是绑定名称、数字、字符串或应用（application）。利用应用进行函数调用，以及像 `it` 或 `while` 这样的结构。

为了保持解析器的简单，Egg内部内部字符串不支持反斜线转义。字符串是封装在双引号内的一系列非双引号字符。名称绑定（Name Binding）可以包含任何非空白字符且在语法中不具有独特含义。在 JavaScript 中编写应用，通过在表达式后放置括号并在括号内放置任意数量的参数，并用逗号分隔。

```javascript
do(define(x, 10),
 if(>(x, 5),
  print("large"),
  print("small")))
```

Egg 语言的一致性意味着 JavaScript 中的操作符（如 `>`）在语言语言中被称为绑定（bindings），使用方式与其他函数类似。而且语法不包含块概念，因此需要一个结构来表示连续运行几项内容。解析器用于定义程序的数据布局包含一个表达式对象的集合。每个对象都包含一个类型属性，表示它是哪种表达式，以及若干其他确定其内容的属性。"value" 类型的表达式意味着字符串或数字。它们的 value 属性由它们代表的字符串或数字组成。使用 "word" 类型的表达式表示标识符（名称）。这些类型的对象包含一个 name 属性，存储标识符的字符串。然后 "apply" 表达式表示应用。它们包含一个 operator 属性来引用被应用的表达式，以及一个包含参数数组的 args 属性。

新程序的 `>(x, 5)` 部分如下：

```json
{
  type: "apply",
  operator: {type: "word", name: ">"},
  args: [
    {type: "word", name: "x"},
    {type: "value", value: 5}
  ]
}
```

我们描述了一个函数 `parseExpression`，它识别字符串输入并返回一个由字符串开头表达式的数据布局对象，以及解析后的字符串。当你解析子表达式时，可以再次调用此函数，处理参数表达式。这段文本可能由更多参数或结束参数列表的右括号组成。

下面是解析器：

```javascript
function parseExpression(program) {
  program = skipSpace(program);
  let match, expr;
  if (match = /^([^"]*)"/.exec(program)) {
    expr = {type: "value", value: match[1]};
  } else if (match = /\d+\b/.exec(program)) {
    expr = {type: "value", value: Number(match[0])};
  } else if (match = /[^\s(),#]/.exec(program)) {
    expr = {type: "word", name: match[0]};
  } else {
    throw new SyntaxError("Unexpected syntax: " + program);
  }
  return parseApply(expr, program.slice(match[0].length));
}

function skipSpace(string) {
  let first = string.search(/\S/);
  if (first == -1) return "";
  return string.slice(first);
}
```

```javascript
let op = evaluate(operator, scope);
if (typeof op == "function") {
  return op(...args.map(arg => evaluate(arg, scope)));
} else {
  throw new TypeError("Applying a non-function.");
}
}
```

评估器包含了所有表达式类型的代码。字面量值表达式提供其值。对于绑定，检查它是否在作用域中被描述，如果是，则获取绑定的值。如果它包含一个不访问任何内容的唯一形式，并将带有作用域的参数表达式传递给影响该形式的函数。如果调用是典型的，访问操作符，确定它是否为函数，并使用可用的参数调用它。利用通用的 JavaScript 函数值来表示 Egg 函数的值。求值的递归布局与解析器的布局相似，两者在解析时通过评估器结合解析器并执行 `evaluate`，但将它们分离可以让程序结构更清晰。这就是组合 Egg 所需的所有。

### 特殊形式

`specialForms` 对象描述了 Egg 中独特的语法。它将单词与访问此类形式的函数关联。目前它是空的。让我们插入 `if`。

```javascript
specialForms.if = (args, scope) => {
  if (args.length != 3) {
    throw new SyntaxError("Wrong number of args to if");
  } else if (evaluate(args[0], scope) !== false) {
    return evaluate(args[1], scope);
  } else {
    return evaluate(args[2], scope);
  }
};
```

Egg 的 `if` 结构期望三个参数。它会访问第一个，如果值不是 `false`，则移动访问第二个。否则，访问第三个。`if` 形式看起来更像 JavaScript 的三元运算符 `?:` 而不是 JavaScript 的语句。它是一个表达式而不是语句，并提供一个值（第二个或第三个参数的结果）。Egg 在处理条件值方面与 JavaScript 不同。它不会将零或空字符串视为 `false`，只有在调用函数之前，才会访问函数的参数。

```javascript
specialForms.while = (args, scope) => {
  if (args.length != 2) {
    throw new SyntaxError("Wrong number of args to while");
  }
  while (evaluate(args[0], scope) !== false) {
    evaluate(args[1], scope);
  }
  // 因为 Egg 中没有 undefined，我们返回 false，
  // 表示缺乏显性结果。
  return false;
}
```

另一个构建块是 `do`，它从上到下执行它的参数。它的值由最后一个参数提供。

```javascript
specialForms.do = (args, scope) => {
  let value = false;
  for (let arg of args) {
    value = evaluate(arg, scope);
  }
  return value;
};
```

为了构建绑定并设置新值，你应该构建一个名为 `define` 的形式。它等待第一个参数作为单词，第二个参数作为提供设置到该单词的表达式。由于 `define` 是一个表达式，它必须返回一个值。我们将返回被设置的值（类似于 JavaScript 的 `=` 运算符）。

```javascript
specialForms.define = (args, scope) => {
  if (args.length != 2 || args[0].type != "word") {
    throw new SyntaxError("Incorrect use of define");
  }
  let value = evaluate(args[1], scope);
  scope[args[0].name] = value;
  return value;
};
```

### 环境

`evaluate` 允许的作用域是一个包含少量属性的属性，其名称与绑定名称匹配。它们的值与这些绑定的值一致。下面是一个代表全局作用域的对象示例。为了启用前面描述的 `if` 结构，布尔值必须是可以访问的。因此，只有两个布尔值，你只需要将两个名称绑定到 `true` 和 `false` 值并使用它们。

```javascript
const topScope = Object.create(null);
topScope.true = true;
topScope.false = false;
```

我们现在可以检查一个使布尔值为假的简单表达式。

```javascript
let prog = parses('if(true, false, true)');
console.log(examine(prog, topScope));
// → false
```

为了提供基础算术运算符和比较运算符，我们将函数值加入作用域。我们将在循环对几个操作符函数使用 `function`，而不是逐个声明。

```javascript
for (let op of ["+", "-", "*", "/", "==", "<", ">"]) {
  topScope[op] = Function("a", "b", `return a ${op} b`);
}
```

我们将 `console.log` 封装在一个函数中输出值，并将其命名为 `print`。

```javascript
topScope.print = value => {
  console.log(value);
  return value;
}
```

这为编写简单程序并在作用域中分析和运行它提供了足够的基础工具：

```javascript
function run(program) {
  return evaluate(parse(program), Object.create(topScope));
}
```

对象原型的链将代表嵌套作用域，允许在不改变高层作用域的情况下添加绑定：

```javascript
do(define(total, 0),
define(count, 1),
while(-count, 11),
do(define(total, +(total, count)),
define(count, +(count, 1))));
print(total));
// -> 55
```

这个概念解释了 Egg 中所示的 1 到 10 的总数。

### 函数

没有函数的编程语言是非常糟糕的，尽管很容易插入一个使用其最后一个参数作为函数体的函数。它还将在此之前的每个参数用函数的参数名称。

```javascript
specialForms.fun = (args, scope) => {
  if (!args.length) {
    throw new SyntaxError("Functions need a body");
  }
  let body = args[args.length - 1];
  let param = args.slice(0, args.length - 1).map(expr => {
    if (expr.type != "word") {
      throw new SyntaxError("Parameter names must be words");
    }
    return expr.name;
  });
  return function() {
    if (arguments.length != params.length) {
      throw new TypeError("Wrong number of arguments");
    }
    let localScope = Object.create(scope);
    for (let i = 0; i < params.length; i++) {
      localScope[params[i]] = arguments[i];
    }
    return evaluate(body, localScope);
  };
};
```

Egg 函数有自己的作用域。由 `fun` 函数构建此作用域并将参数附加到其中返回结果。

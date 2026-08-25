
# JavaScript 书籍集

## 第一章：JavaScript 简介

JavaScript 是一种编程语言，允许你为网页添加交互性和功能。它在前端开发中被广泛使用，使你能够创建动态元素、控制事件、验证表单等等。

JavaScript 的主要特点是能够实时操作 HTML 元素和 CSS 样式。这意味着我们可以在网页加载到浏览器后，更改其内容、外观和行为。

要开始编写 JavaScript 代码，你可以使用简单的文本编辑器（如记事本）或集成开发环境（IDE），如 Visual Studio Code。JavaScript 代码插入在 HTML 文件中的`<script>`和`</script>`标签之间。或者，你可以将 JavaScript 代码编写在扩展名为`.js`的单独文件中，然后将其导入到 HTML 中。

执行 JavaScript 代码有几种方式。其中之一是通过开发者菜单访问浏览器控制台，直接在其中编写。另一种选择是将代码绑定到 HTML 事件，例如按钮点击。此外，你可以将 JavaScript 代码包含在 HTML 文档的头部或页脚，使其在适当的时间运行。

JavaScript 是一种动态类型编程语言，也就是说，变量的类型可以在程序执行过程中改变。这种灵活性使你能够更快地编写代码，但也需要注意避免错误。

在 JavaScript 中，有多种数据类型，如数字、字符串、布尔值、数组、对象等。每种数据类型都有特定的属性和方法，可以被访问和使用。

JavaScript 语言还具有流程控制功能，例如条件语句（`if/else`）、循环（`for`、`while`、`do/while`）以及更高级的控制结构，如`switch`。

此外，JavaScript 还具有操作字符串、函数、正则表达式、处理日期和时间等功能。这些功能使该语言具有极强的通用性和强大的能力。

需要提及的是，JavaScript 不仅仅在浏览器中使用。如今，你也可以使用`Node.js`在服务器上运行 JavaScript，从而仅使用一种编程语言就能构建完整的 Web 应用程序。

这是一个简要总结，JavaScript 简介。希望你已经理解了这门语言的基本概念，并对学习更多内容感到兴奋。从现在开始，我们将探讨更详细和实用的主题。继续阅读和练习，成为一名自信的 JavaScript 开发者。

## 第二章：JavaScript 基础

在本章中，我们将讨论 JavaScript 的主要基础知识。我们将涵盖理解语言所必需的概念，并解释如何使用变量、运算符、条件和重复结构。

### 1. 变量

变量用于在 JavaScript 中存储值。你可以使用`var`、`let`或`const`关键字来声明变量。此外，变量可以存储不同类型的数据，如数字、字符串、布尔值和对象。

### 2. 数据类型

JavaScript 有不同的数据类型，包括数字、字符串、布尔值、数组、对象和`null`。理解如何正确使用这些数据类型以在代码中执行适当的操作非常重要。

### 3. 运算符

JavaScript 中的运算符允许你执行不同的操作，如加法、减法、乘法和除法。此外，还有比较运算符和逻辑运算符，它们对于在代码中做出决策很有用。

### 4. 条件结构

条件结构允许你根据特定条件执行不同的代码块。最常见的是`if-else`语句，它检查一个条件是否为真，并执行相应的代码块。

### 5. 重复结构

重复结构用于重复执行一段代码块。JavaScript 有三种重复结构：`for`、`while`和`do-while`。它们允许你多次执行给定的代码块，直到满足某个条件。

### 6. 函数

函数是可重用的代码块，可以调用来执行特定任务。它们允许你将代码分成更小、更易于管理的部分，并且可以接受参数和返回值。

### 7. 字符串操作

在 JavaScript 中，可以使用不同的方法来操作字符串，例如连接字符串、搜索子字符串、将它们转换为大写或小写等等。

这些是你作为初学者需要了解的一些基本 JavaScript 基础知识。使用这些概念，你将能够构建更复杂的程序并在学习上取得进步。务必在自己的代码中练习和尝试这些概念，以熟悉它们。

## 第三章：变量和数据类型

在本章中，我们将学习 JavaScript 中的变量和数据类型。这些概念是编程的基础，因为它们有助于在程序中存储和操作信息。

### 1. 变量

- 变量是存储值或对值的引用的容器。
- 要创建变量，我们使用`var`关键字，后跟变量名，以及可选的初始值。
- 例如：`var age = 25;`创建一个名为`age`的变量，并为其赋值 25。
- 为变量赋予有意义的名称以提高代码的可读性非常重要。

### 2. 数据类型

- JavaScript 有几种数据类型，包括：
- 数字：表示数值，例如 5、3.14、-10。
- 字符串：表示字符序列，例如`"Hello"`、`"World"`、`"123"`。
- 布尔值：表示真值（`true`）或假值（`false`）。
- Null：表示有意缺少值。
- Undefined：表示已声明但尚未赋值的变量。
- 对象：表示相关属性和方法的集合。
- 数组：表示值的有序集合。
- 函数：可重用的代码块，可以被调用和执行。

### 3. 变量操作

- 我们可以简单地使用`=`赋值运算符为变量分配新值。
- 例如：`age = 30;`将`age`变量的值更新为 30。
- 我们还可以使用算术运算符或连接字符串来组合变量值。
- 算术运算符包括加法（`+`）、减法（`-`）、乘法（`*`）、除法（`/`）等。
- 字符串连接可以使用`+`运算符完成。
- 例如：`var name = "John"; var greeting = "Hello, " + name + "!";`创建变量`greeting`，其值为 "Hello, João!"。

### 命名约定

- 建议遵循某些命名约定，以使代码更易于阅读。
- 为变量使用描述性名称，避免令人困惑的缩写。
- 变量名以小写字母开头，并对复合名称使用首字母大写约定（例如`camelCase`）。
- 命名变量时避免使用 JavaScript 保留关键字。

这些只是关于 JavaScript 中变量和数据类型的一些基础知识。练习使用这些概念对于良好理解至关重要。

## 第四章：JavaScript 中的运算符

在本章中，我们将探讨语言中可用的不同类型运算符，以及如何使用它们来执行不同的操作。

JavaScript 中的运算符可以分为不同的类别，如算术运算符、赋值运算符、比较运算符、逻辑运算符和三元运算符。

### 1. 算术运算符

算术运算符用于执行基本的数学运算。一些例子包括：

- 加法（`+`）：用于将两个值相加。
- 减法（`-`）：用于从一个值中减去另一个值。
- 乘法（`*`）：用于将两个值相乘。
- 除法（`/`）：用于将一个值除以另一个值。
- 取模运算符（`%`）或模运算：用于获取一个值除以另一个值的余数。
- 自增（`++`）和自减（`--`）：用于将一个值增加或减少 1。

### 2. 赋值运算符

赋值运算符用于将值赋给变量。一些示例是：

- `=`（简单赋值）：用于将一个值赋给一个变量。
- `+=`（累加赋值）：用于将一个值添加到现有变量。
- `-=`（递减赋值）：用于从现有变量中减去一个值。

### 3. 比较运算符

比较运算符用于比较两个值并返回一个布尔值（`true`或`false`）。一些示例是：

- 相等（`==`）：检查两个值是否相等。
- 不等（`!=`）：检查两个值是否不相等。
- 大于（`>`）、小于（`<`）、大于或等于（`>=`）和小于或等于（`<=`）：用于比较数值。
- 严格相等（`===`）、严格不等（`!==`）：检查值和数据类型的相等性。

### 4. 逻辑运算符

逻辑运算符用于组合逻辑表达式并返回一个布尔值。一些示例是：

- 逻辑与（`&&`）：如果所有表达式都为`true`，则返回`true`。
- 逻辑或（`||`）：如果至少一个表达式为`true`，则返回`true`。
- 逻辑非（`!`）：返回布尔值的相反值。

### 5. 三元运算符

三元运算符是编写 IF-ELSE 条件的一种简洁方式。它允许你根据条件将值赋给变量。语法如下：

```javascript
变量 = (条件) ? 为真时的值 : 为假时的值;
```

这些只是 JavaScript 中运算符的一些示例。然而，还有许多其他运算符可用于各种操作。

记住要实践并在代码中尝试这些运算符，以更好地理解它们的工作原理。实践是在 JavaScript 中熟练使用运算符的关键。

## 第五章：JavaScript 中的控制流结构

控制和流程结构用于控制代码执行的顺序。在本章中，我们将讨论三种主要的控制结构：条件语句（`if`、`else if`、`else`）、循环（`for`、`while`、`do while`）和开关语句。

### 1. 条件语句

IF：`if`结构用于在条件为真时执行一段代码。例如：

```javascript
if (condition) {
  // 条件为真时要执行的代码
}
```

- ELSE IF：你可以使用`else if`来检查多个链式条件。例如：

```javascript
if (condition1) {
  // 条件1为真时要执行的代码
} else if (condition2) {
  // 条件2为真时要执行的代码
} else {
  // 所有条件都不为真时要执行的代码
}
```

- SWITCH：当我们有多个不同的选项需要根据单个变量进行检查时使用`switch`。例如：

```javascript
switch (variable) {
  case value1:
    // 当变量等于 value1 时要执行的代码
    break;
  case value2:
    // 当变量等于 value2 时要执行的代码
    break;
  default:
    // 当变量不等于 value1 或 value2 时要执行的代码
}
```

### 2. 循环

- FOR：`for`循环用于重复执行一组指令，直到满足某个条件。例如：

```javascript
for (initialization; condition; increment) {
    // 要重复执行的代码
}
```

让我们看一个实际的例子：

```javascript
var x = 0;
for (x; x <= 10; x++) {
    console.log(x); // 在控制台显示 x 的当前值
}
```

- WHILE：`while`循环用于在条件为真时重复执行一组指令。例如：

```javascript
while (condition) {
    // 要重复执行的代码
}
```

让我们看一个实际的例子：

```javascript
y = 0;
while (y <= 10) {
    console.log(y);
    y++;
}
```

- DO-WHILE：`do while`循环类似于`while`，但条件是在执行代码块之后检查的。这确保了代码块至少执行一次。

例如：

```javascript
do {
    // 要重复执行的代码
} while (condition);
```

另一个例子：

```javascript
y = 10;
do {
    console.log(y);
    y--;
} while (y >= 0);
```

你可以看到在这个例子中，我们执行了递减操作而不是递增，也就是说，我们是在减去而不是增加。

再举一个例子，操作的类型并不影响 DO WHILE 循环的条件。

这些控制流结构对于编写更复杂的 JavaScript 程序至关重要。它们允许你根据条件做出决策，并在满足条件的情况下重复执行代码块。

现在你知道如何使用条件语句、循环和开关语句来控制 JavaScript 代码的执行流程了。希望这能帮助你加深对这门语言的了解！

## 第六章：JavaScript 中的函数

函数是可重用的代码块，可以被调用来执行特定的操作。它们在 JavaScript 中至关重要，因为它们有助于代码的模块化和组织。当你定义一个函数时，你可以给它命名并提供一组指令，当函数被调用时，这些指令将被执行。

要创建一个函数，你首先需要使用`function`关键字，后跟函数名（通常以驼峰命名法编写）、空括号`()`用于函数参数（可选），然后是花括号`{}`来界定函数代码块。

例如，让我们创建一个简单的名为`greeting`的函数，它在屏幕上显示问候语：

```javascript
function greeting() {
    console.log("Hello, Welcome!");
}
```

当你使用函数名后跟括号来调用此函数时，函数内部的代码将被执行：

```javascript
greeting(); // "Hello, Welcome!"
```

函数也可以接收参数，这些参数是可以传递给函数的值，以便函数可以在其代码中使用它们。例如，让我们创建一个名为`sum`的函数，它接受两个数字作为参数并返回它们的和：

```javascript
function sum(a, b) {
    return a + b;
}
```

这里，`a`和`b`是函数的参数。我们使用`return`关键字来指定函数要返回的值。

我们可以调用这个函数并将结果赋给一个变量：

```javascript
function sum(a, b) {
  return a + b;
}

var result = sum(5, 3);
console.log(result); // 8
```

函数也可以有副作用，例如改变全局变量或修改 HTML 文档的元素。例如，我们可以创建一个名为`updateTitle`的函数来更新页面的标题：

```javascript
function updateTitle(newTitle) {
  document.title = newTitle;
}
```

在函数内部，我们将`newTitle`参数的值赋给`document`对象的`title`属性。当调用此函数并传递一个字符串作为参数时，页面标题将被更新：

```javascript
updateTitle("New Title!");
```

我们的实际代码看起来像这样：

```javascript
function updateTitle(newTitle) {
  document.title = newTitle;
}

updateTitle("New Title!");
```

还有匿名函数，即没有名称的函数。它们通常用作其他异步过程的回调函数或作为函数表达式。例如：

```javascript
var double = function(number) {
  return number * 2;
}

console.log(double(5)); // 10
```

在这种情况下，函数被赋值给变量`double`，并可以在以后被调用。

此外，还可以创建箭头函数，这是 ES6 中引入的一种更简短、更简单的语法：

```javascript
const greeting = () => {
    console.log("Hello, Welcome!");
}

greeting(); // 调用函数
```

这些只是 JavaScript 中函数的一些基础知识。它们非常通用，随着你学习的深入，你可以进一步探索作用域、递归函数、高阶函数等更多概念。

希望这些信息对你开始理解 JavaScript 中的函数有所帮助。

## 第七章：数组

数组是 JavaScript 中非常重要的数据结构。我将解释一些关于数组的概念以及如何高效地使用它们。

数组是元素的有序集合，这些元素可以是数字、字符串、对象甚至其他数组。

每个元素由一个索引标识，第一个元素的索引从 0 开始，第二个是 1，依此类推。

你可以在 JavaScript 中以不同的方式创建数组。最常见的方式是使用方括号来定义元素，用逗号分隔。

例如：

```javascript
let numbers = [1, 2, 3, 4, 5];
```

```javascript
let fruits = ["apple", "banana", "orange"];
```

要访问数组中的特定元素，只需使用数组名称后跟方括号中的元素索引。例如：

## 第八章：JavaScript 中的对象

对象是该语言中最重要的数据结构之一，因为它们允许你以有组织的方式存储和访问信息。

JavaScript 中的对象是属性的集合，这些属性由键值对组成。键是标识属性的字符串，值可以是任何数据类型，例如数字、字符串、布尔值、函数，甚至其他对象。

在 JavaScript 中有两种创建对象的方式：字面量表示法和构造函数。让我们从字面量表示法开始，这是最常见也是最简单的创建对象的方式。

要使用字面量表示法创建对象，你需要使用花括号`{}`。在花括号内部，你定义用逗号分隔的属性。每个属性由一个键、后跟一个冒号和相应的值组成。

看一个例子：

```javascript
let person = {
  name: "João",
  age: 25,
  profession: "Developer"
};
```

在这个例子中，我们创建了一个名为`person`的对象，它有三个属性：`name`、`age`和`profession`。每个属性都有一个关联的值。

要访问或修改对象的属性，我们使用点（`.`）语法，后跟属性名称。例如：

```javascript
console.log(person.name); // "João"
person.age = 26;
console.log(person.age); // 26
```

你也可以在创建对象后向其添加属性。只需使用点语法，就像我们上面所做的那样，来定义一个新属性及其值。

```javascript
person.city = 'Belo Horizonte'; //向person添加城市
```

让我们看看一个完整的例子会是什么样子：

```javascript
let person = {
    name: "João",
    age: 25,
    profession: "Developer"
};
console.log(person.name); // "João"
person.age = 26;
console.log(person.age); // 26
person.city = 'Belo Horizonte'; //添加城市
console.log(person.city);// 显示person的城市
```



此外，你也可以使用方括号语法（`[]`）来访问对象的属性。这在我们需要访问名称存储在变量中的属性时特别有用。看一个例子：

```javascript
let key = "age";
console.log(person[key]); // 26
```

另一种创建对象的方式是通过构造函数。在这种情况下，我们使用 `new` 运算符与构造函数一起来创建对象的一个实例。

让我们看一个使用 `Object` 构造函数的例子：

```javascript
let car = new Object();
car.brand = "Ford";
car.model = "Mustang";
car.year = 2020;
```

在这个例子中，我们使用 `Object` 构造函数创建了一个名为 `car` 的对象。然后我们使用点语法向对象添加属性。

此外，还可以在对象上创建方法，这些方法是与对象属性关联的函数。方法允许你执行一些与对象相关的代码。

看一个例子：

```javascript
let person = {
  name: "João",
  age: 25,
  profession: "Developer",
  present: function() {
    console.log("Hi, my name is " + this.name + " and i have " + this.age + " years old.");
  }
};
person.present(); // "Hi, my name is João and i have 25 years old."
```

在这个例子中，我们定义了一个名为 `present` 的方法，它使用 `person` 对象的属性打印一个句子。

要在方法中访问属性，我们使用 `this` 关键字，它指的是当前对象。

这些是关于 JavaScript 中对象的一些主要信息。希望这能帮助你理解基本概念并在你的程序中有效地使用对象。

## 第 9 章：JavaScript 中的事件

事件在用户与网页元素之间的交互中扮演着基础性的角色。

它们允许你为特定的用户操作创建动态响应，例如点击、鼠标移动、打字等等。

JavaScript 中有几种类型的事件。

一些最常见的有：

### 1. 点击事件

当用户点击页面上的元素（如按钮或图像）时，此事件被触发。要处理此事件，你可以使用 `addEventListener` 方法并传递在点击发生时将执行的函数。

看：

```javascript
const button = document.querySelector('#myButton');
button.addEventListener('click', function() {
  // 点击时将运行的代码
});
```

现在让我们看看一个 HTML 页面中的例子会是什么样子：

```html
<body>
  <button id="myButton">My Button</button>
  <script>
    const button = document.querySelector('#myButton');
    button.addEventListener('click', function() {
      // 点击时将运行的代码
      console.log("clicked");
    });
  </script>
</body>
```

在这种情况下，我们只有按钮被显示出来，并且定义了它的 `id`。在 JavaScript 中，我们有按钮函数，如果被点击，将在控制台中显示消息 `"clicked"`。

让我们稍微玩一下代码，更深入地了解一下函数。

看：

```html
<button id="myButton">My Button</button>

<script>
  let clicks = 0;

  const button = document.querySelector('#myButton');

  button.addEventListener('click', function() {
    clicks ++;

    // 点击时将运行的代码

    console.log("clicked " + clicks + " time(s)!");
  });

</script>
```

在这种情况下，我们创建了一个 `clicks` 变量，它在每次点击时递增，并显示消息说明按钮被点击了多少次。

### 2. 键盘事件（`keydown`、`keyup`、`keypress`）

当键盘上的键被按下、释放或按住时，这些事件被触发。你可以使用这些事件来创建基于键盘的交互，例如在按下某个特定键时激活一个函数。

```javascript
document.addEventListener('keydown', function(event) {
  if (event.key === 'Enter') {
    // 当按Enter键时要执行的代码
  }
});
```

看一个实际的例子：

```javascript
document.addEventListener('keydown', function(event) {
  if (event.key === 'Enter') {
    // 当按Enter键时要执行的代码
    alert('You press ENTER!');
  }
});
```

### 3. 鼠标事件（`mouseover`、`mouseout`、`mousemove`）

当鼠标悬停在元素上、离开元素或在元素内移动时，这些事件被触发。你可以使用这些事件来创建基于鼠标移动的交互。

```javascript
element.addEventListener('mouseover', function(){
    // 当你将鼠标指针移到元素上时要执行的代码
});
```

看实际例子：

```html
<div id="myElement" style="background-color: #080808; color:#f8f8f8;">My Div</div>
<script>
    const element = document.querySelector('#myElement');
    element.addEventListener('mouseover', function() {
        // 当你将鼠标指针移到元素上时要执行的代码
        alert("You pass the mouse pointer on div' myElement'!");
    });
</script>
```

在这段代码中，我们添加了一个 `id` 为 `myElement` 的 `div`，并在样式中将其背景定义为黑色，字体颜色定义为白色。这样做纯粹是为了更好地看到 `div` 的边界。

我们定义当我们将鼠标移到 `div` 上时，会出现一个带有该消息的警报。

### 4. 表单事件（`submit`、`change`）

当用户提交表单或更改表单字段的值时，会分别触发这些事件。它们对于实时验证输入数据或在表单提交时执行操作非常有用。

```javascript
const form = document.querySelector('#myForm');

form.addEventListener('submit', function(event) {
    event.preventDefault(); // prevents default form submission
    // code to be executed when the form is submitted
});
```

查看实际代码：

```html
<form id="myForm" action="#">
    <label for="name">Name:</label><br>
    <input type="text" id="name" name="name" value="João"><br>
    <label for="lastname">Last name:</label><br>
    <input type="lastname" id="lastname" name="lastname" value="Silva"><br><br>
    <input type="submit" value="Submit">
</form>

<script>
    const form = document.querySelector('#myForm');
    form.addEventListener('submit', function(event) {
        event.preventDefault(); // prevents default form submission
        // code to be executed when the form is submitted
        alert('Form Submitted!');
    });
</script>
```

以上只是 JavaScript 中最常见事件的几个示例。然而，可用的事件种类非常丰富，每个 HTML 元素都可以关联不同的事件。了解 JavaScript 和 HTML 文档对于获取完整的事件列表及其使用方法至关重要。

## 第 10 章：DOM 操作

在 JavaScript 中，文档对象模型（DOM）是 HTML 页面的内存表示，其中每个 HTML 元素都是一个对象，可以通过脚本进行操作。

DOM 操作是使用 JavaScript 在网页上创建动态交互的一项核心技能。

### 1. DOM 简介

#### 什么是 DOM？为什么它很重要？

DOM，即文档对象模型，是一个编程接口，它将 HTML 或 XML 文档的结构表示为一棵对象树。文档中的每个元素、属性和文本都表示为树中的一个节点。DOM 允许程序员动态地操作文档的结构、样式和内容。

#### 为什么它很重要？

DOM 是基础性的，因为它允许 Web 开发者创建交互式和动态的页面。

通过使用 JavaScript 操作 DOM，你可以更新内容、更改样式、添加或移除元素、响应用户事件等等。

本质上，DOM 是一座桥梁，将 HTML/XML 页面内容与 JavaScript 代码连接起来，提供交互式和动态的用户体验。

#### 如何在 JavaScript 中访问 DOM？

要在 JavaScript 中访问 DOM，我们使用 `document` 变量，它表示当前的 HTML 文档。以下是一些常见的访问 DOM 的方式：

- `getElementById()`：

  ```javascript
  let element = document.getElementById('elementId');
  ```

- `getElementsByClassName()`：

  ```javascript
  let elements = document.getElementsByClassName('className');
  ```

- `getElementsByTagName()`：

  ```javascript
  let elements = document.getElementsByTagName('tagName');
  ```

- `querySelector()`：

  ```javascript
  let element = document.querySelector('selector');
  ```

- `querySelectorAll()`：

  ```javascript
  let elements = document.querySelectorAll('selector');
  ```

- 直接操作：

  我们也可以通过 DOM 直接操作元素。

  ```javascript
  let element = document.createElement('div');
  element.textContent = 'New Element';
  document.body.appendChild(element);
  ```

以上只是一些示例。具体选择哪种方法取决于你的需求和 HTML 的结构。

DOM 提供了多种导航、选择和操作元素的方法，使网页能够实现丰富的动态交互。

### 2. 元素选择

#### 如何通过标识符（ID）选择 DOM 元素？

通过 ID 选择元素是很常见的做法，因为 ID 在 HTML 页面中是唯一的。你可以使用 `getElementById()` 函数来实现：

```javascript
let elementById = document.getElementById('YourId');
```

这将返回具有指定 ID 的元素的引用。

#### 如何通过类名、标签名和其他选择器选择 DOM 元素？

有多种方式可以通过类名、标签名或其他选择器来选择元素，使用的方法包括 `getElementsByClassName()`、`getElementsByTagName()`、`querySelector()` 和 `querySelectorAll()`。

**使用类名**

```javascript
// Selecting by class
let elementsByClass = document.getElementsByClassName('YourClass');

// Selecting using querySelector for first occurrence
let firstElementByClass = document.querySelector('.yourClass');

// Selecting using querySelectorAll for all occurrences
let allElementsByClass = document.querySelectorAll('.yourClass');
```

**使用标签名**

```javascript
// Selecting by tag
let elementsByTag = document.getElementsByTagName('yourTag');

// Selecting using querySelector for the first occurrence
let firstElementByTag = document.querySelector('yourTag');

// Selecting using querySelectorAll for all occurrences
let allElementsByTag = document.querySelectorAll('yourTag');
```

**使用其他选择器：**

```javascript
// Selection by selector
let elementBySelector = document.querySelector('#yourId.yourClass yourTag');

// Selecting using querySelectorAll for all occurrences
let allElementsSelector = document.querySelectorAll('#yourId.yourClass yourTag');
```

这些方法方便了根据不同的标准来选择元素，使你能够灵活且动态地操作 DOM，以响应 Web 应用中的特定事件或需求。

### 3. 元素操作

#### 如何获取和更改元素属性？

你可以使用 `getAttribute()` 和 `setAttribute()` 方法来获取和更改元素的属性。

- 获取属性：

  ```javascript
  let valueOfAttribute = elemento.getAttribute('nameOfAttribute');
  ```

- 更改属性：

  ```javascript
  elemento.setAttribute('nameOfAttribute', 'newValue');
  ```

#### 如何更改元素的内容？

你可以通过 `textContent` 或 `innerHTML` 属性来操作元素的内容。

- 使用 `textContent`：

  ```javascript
  element.textContent = 'New content';
  ```

- 使用 `innerHTML`（注意安全问题）：

  ```javascript
  element.innerHTML = '<strong>New</strong> content';
  ```

在使用 `innerHTML` 处理动态内容时要小心，因为它可能会使你的代码暴露于脚本注入等安全漏洞。

#### 如何添加和移除元素的类？

要添加或移除类，你可以使用元素的 `classList` 属性。

- 添加类：

  ```javascript
  element.classList.add('newClass');
  ```

- 移除类：

  ```javascript
  element.classList.remove('classExistent');
  ```

#### 如何创建新元素并添加到 DOM 中？

你可以使用 `document.createElement()` 创建新元素，并使用 `appendChild()` 等方法将它们添加到 DOM 中。

- 创建新元素：

  ```javascript
  let newElement = document.createElement('div');
  ```

- 添加到 DOM：

  ```javascript
  // Add as a child of another element
  outerElement.appendChild(newElement);

  // Or add to the end of the document body
  document.body.appendChild(newElement);
  ```

#### 如何从 DOM 中移除元素？



要移除元素，你可以使用 `remove()` 或 `parentNode.removeChild()` 方法。

- **使用 `remove()`：**

```javascript
elementToRemove.remove();
```

- **使用 `parentNode.removeChild()`：**

```javascript
let parent = elementToRemove.parentNode;
parent.removeChild(elementToRemove);
```

两种方法都能完成任务，但 `remove()` 更简洁直观。选择哪种方法取决于你需要支持的浏览器兼容性。

## 4. DOM 事件

### 什么是事件？如何在 JavaScript 中使用它们？

事件是在浏览器中发生的动作或事件，例如鼠标点击、按键、页面加载等。JavaScript 允许你响应这些事件，使你的网页更具交互性。

**使用事件：**

```javascript
// Click event usage example
element.addEventListener('click', function() {
    // Code to be executed when the element is clicked 
});
```

### 如何为 DOM 元素添加事件处理程序？

你可以使用 `addEventListener()` 方法来添加事件处理程序。

#### 基本语法

```javascript
element.addEventListener('typeOfEvent', function() {
  // Code to be executed when the event occurs
});
```

#### 移除事件处理程序

```javascript
// Save reference to function
function myHandler() {
  // Code
}

// Add event
element.addEventListener('EventType', myHandler);

// Remove event
element.removeEventListener('EventType', myHandler);
```

### 如何处理点击、输入和其他常见事件？

事件有很多类型，你可以使用 `addEventListener()` 以相同的方式处理它们。以下是一些常见示例：

#### 点击事件

```javascript
element.addEventListener('click', function() {
  // Code to handle the click
});
```

#### 输入事件（按键按下）

```javascript
element.addEventListener('keydown', function(event) {
  // 'event' contains information about the event, such as key pressed
  // Code to handle key press
});
```

需要注意的是，在 `keydown` 这类事件中，你还需要定义触发事件的按键，请参考以下代码示例：

```javascript
const element = document.querySelector('#myElement');
element.addEventListener('keydown', function (event) {
  // 'event' contains information about the event, such as key pressed
  // Code to handle key press
  if (event.key === 'Enter') {
    // code to be executed when the "Enter key is pressed
    alert('You pressed ENTER!');
  }
});
```

#### 表单提交事件

```javascript
form.addEventListener('submit', function(event) {
  // Prevent default form submission
  event.preventDefault();
  // Code to handle form submission
});
```

以上仅是几个示例。JavaScript 文档和在线资源非常适合探索所有可用的事件类型，以及学习如何在 Web 应用程序中更有效地使用它们。

## 5. DOM 遍历

### 如何遍历和操作 DOM 中的元素层级？

DOM 遍历涉及在元素层级中进行导航，使你能够查找父元素、子元素和兄弟元素。以下是一些实现方式。

### 向上遍历（查找父元素）

```javascript
let parent = element.parentNode;
```

### 向下遍历（查找子元素）

```javascript
let children = element.childNodes;
```

```javascript
let firstChild = element.firstChild;
```

```javascript
let lastChild = element.lastChild;
```

```javascript
// Or using the more common method
let childs = element.children;
```

### 横向遍历（兄弟元素）

```javascript
let nextSibling = element.nextSibling;
```

```javascript
let prevSibling = element.previousSibling;
```

```javascript
// Or using more common methods
let siblingsNext = element.nextElementSibling;
let siblingPrev = element.previousElementSibling;
```

### 如何遍历和更改 DOM 中的元素结构？

你可以使用方法来添加、删除和替换元素。

#### 添加新元素

```javascript
let newElement = document.createElement('div');
element.appendChild(newElement);
```

```javascript
// Or insert before another element
element.insertBefore(newElement, reference);
```

#### 删除元素

```javascript
element.removeChild(childToRemove);
```

#### 替换元素

```javascript
let newElement = document.createElement('span');
element.replaceChild(newElement, childToReplace);
```

以上仅是遍历和操作 DOM 的几种方式。DOM 提供了多种方法和属性来满足不同的元素操作需求，为构建和修改动态网页提供了灵活性。

## 6. 元素样式

### 如何访问和更改 DOM 元素的 CSS 样式？

你可以通过 `style` 属性来访问和更改 DOM 元素的 CSS 样式。以下是一些实现方式：

### 访问样式

```javascript
//Accessing a specific style
let width = element.style.width;
```

```javascript
// Accessing all styles as a string
let styles = element.style.cssText;
```

### 更改样式

```javascript
// Changing a specific style
element.style.width = '200px';
// Changing multiple styles at once
element.style.cssText = 'width: 200px; height: 100px; background-color: #f00;';
```

请记住，`style` 属性只能访问通过 HTML 中的 `style` 属性直接在元素上定义的样式。要访问由外部或内部样式表应用的样式，你可以使用 `getComputedStyle()` 方法：

```javascript
let computedStyle = window.getComputedStyle(element);
let backgroundColor = computedStyle.backgroundColor;
```

### 如何添加和移除类以实现动态样式？

添加和移除类是实现动态样式的一种有效方式。这使你可以在 CSS 样式表中定义样式，并根据需要应用或移除这些样式。

#### 添加类

```javascript
element.classList.add('className');
```

#### 移除类

```javascript
element.classList.remove('className');
```

#### 切换类

如果不存在则添加，如果存在则移除：

```javascript
element.classList.toggle('className');
```

例如，考虑以下 CSS：

```css
.destack {
  color: #ff0000;
  font-weight: bold;
}
```

你可以像这样将该类应用到元素上：

```javascript
element.classList.add('destack');
```

并在需要时移除它：

```javascript
element.classList.remove('destack');
```

这种方式使得创建可复用的样式以及根据用户交互或应用逻辑动态应用样式变得非常简单。

## 7. 表单操作

### 如何获取、设置和验证表单字段值？

在 JavaScript 中操作表单涉及访问和交互表单元素，如文本框、复选框和单选按钮。以下是一些常见操作：

### 从表单字段获取值

```javascript
// Get value from a text field
let valueOfTextField = document.getElementById('textField').value;

// Get value from a checkbox
let valueOfSelectionBox = document.getElementById('selectionBox').value;

// Get value from a radio button (using select by name)
let radioButtons = document.getElementsByName('nameOfRadioButton');
let valueOfRadioButton;
for (let i = 0; i < radioButtons.length; i++) {
    if (radioButtons[i].checked) {
        valueOfRadioButton = radioButtons[i].value;
        break;
    }
}
```

### 设置表单字段值

```javascript
// Set value of a text field
document.getElementById('textField').value = 'New value';
```

```javascript
// Set value of a checkbox
document.getElementById('selectionBox').value = 'newOption';
// Set value of a radio button
document.getElementById('radioButton').checked = true;
```

### 验证表单

```javascript
// Simple validation example
function validateFormulario() {
  let field = document.getElementById('field');
  let value = field.value.trim();
  if (value === '') {
    alert('Field cannot be empty!');
    return false; // Prevent the form from being sent
  }
  // Other validation checks can be added here
  return true; // Allows form submission
}
```

### 如何将表单数据提交到服务器？

将表单数据提交到服务器可以使用 HTTP POST 或 GET 方法。最常用的是 POST 方法，它在发送密码等敏感数据时更加安全。

#### 使用 POST 方法

**HTML：**

```html
<form id="myForm" action="/path/do/server" method="post">
  <!-- Form fields here -->
  <input type="submit" value="Submit">
</form>
```

**JavaScript：**

```javascript
<script>
document.getElementById('myForm').addEventListener('submit', function(event) {
  event.preventDefault(); // Prevents default form submission
  // Get form data
  let formData = new FormData(event.target);
  // Make an AJAX request or use other techniques to send data to the server
  // Example using fetch:
  fetch('/path/to/server', {
    method: 'POST',
    body: formData
  })
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
});
</script>
```

这是一个基本示例，你可以根据应用和服务器的具体需求进行调整。

请务必在服务器端验证和处理表单数据，以确保数据安全和完整性。

## 8. 性能考量

不必要的 DOM 操作会显著影响 Web 应用程序的性能。以下是一些避免性能问题的最佳实践：

### 1. 尽量减少直接操作

避免直接且频繁地操作 DOM，尤其是在处理大数据集时。执行大量的读写操作会导致回流和重绘，这在性能方面代价很高。

### 2. 使用文档片段进行批量插入

当需要向 DOM 中添加多个元素时，考虑使用文档片段。不要逐个添加元素，而是创建一个文档片段，将元素添加到其中，然后将文档片段添加到 DOM。这样可以减少布局和重绘操作。

```javascript
let fragment = document.createDocumentFragment();
for (let i = 0; i < 1000; i++) {
  let newElement = document.createElement('div');
  fragment.appendChild(newElement);
}
document.body.appendChild(fragment);
```

### 3. 避免重复读写

尽量减少对同一元素的重复读取和写入。存储你经常访问的 DOM 元素的引用，而不是多次查找它们。

```javascript
// 避免在循环中这样写
for (let i = 0; i < elements.length; i++) {
    elements[i].style.color = 'red';
}

// 应该这样写
let color = 'red';
for (let i = 0; i < elements.length; i++) {
    elements[i].style.color = color;
}
```

### 4. 使用事件委托

与其为许多单独的元素添加事件处理器，不如使用事件委托。为一个共同的祖先元素添加一个单一的事件处理器，并确定事件的实际目标。

```javascript
document.addEventListener('click', function(event) {
    if (event.target.classList.contains('elementClass')) {
        // 处理对目标元素的点击
    }
});
```

### 5. 优化动画和过渡效果

如果你在使用动画或过渡效果，避免在短时间内进行过多的样式更改。使用 `transform` 属性进行动画，因为它通常具有更好的性能。

```javascript
element.style.transform = 'translateX(100px) translateY(50px)';
```

这些实践将有助于提高你的应用程序的性能和响应能力，使其在操作 DOM 时更高效。

请记住，优化可能因你的应用程序的具体上下文而异。

在学习如何使用 JavaScript 操作 DOM 时，通过实际示例和小型项目进行练习非常重要。

尝试和测试不同的 DOM 操作技术将帮助你巩固知识，并更好地理解如何与网页上的元素交互。

# 第 11 章：用户交互

本章是理解 JavaScript 如何与用户交互并为网站或应用程序创建更动态体验的基础。有几种使用 JavaScript 与用户交互的方式，例如显示消息、请求输入和处理事件。

## 1. 显示消息

要向用户显示消息，你可以使用 `alert()` 函数，它会创建一个带有消息的对话框。

```javascript
alert("欢迎访问我们的网站！");
```



你也可以使用`confirm()`函数，它会创建一个带有问题的对话框，如果用户点击“确定”则返回`true`，如果用户点击“取消”则返回`false`。

```javascript
if (confirm("你想继续吗？")) {
  // 如果用户点击“确定”则执行的代码
} else {
  // 如果用户点击“取消”则执行的代码
}
```

### 2. 请求输入

要提示用户输入一个值，你可以使用`prompt()`函数，它会创建一个带有输入字段的对话框。例如：

```javascript
let name = prompt("你叫什么名字？");
console.log("你好，" + name + "！");
```

用户输入的值存储在一个变量中（本例中为`name`），可以在代码的后面使用。

### 3. 事件处理

事件是用户的操作，例如按钮点击、鼠标移动或按键。你可以使用 JavaScript 来处理这些事件并执行相应的操作。

例如，假设你的网站上有一个按钮，你想在用户点击它时显示一条消息。你可以通过将一个函数分配给按钮的点击事件来实现这一点。

以下是一个基本示例：

**HTML**

```html
<button id="myButton">点击这里</button>
```

**JavaScript**

```html
<script>
    let button = document.getElementById("myButton");
    button.addEventListener("click", function() {
        alert("按钮被点击了！");
    });
</script>
```

在这个例子中，`addEventListener()`函数被用来为按钮元素添加一个事件监听器。当按钮被点击时，消息将使用`alert()`显示。

此外，还有许多其他可用的事件，如`mouseover`、`mouseout`、`keydown`等。你可以根据需要进一步研究这些事件及其使用方法。

## 第12章：AJAX 和 HTTP 请求

在本章中，我们将探索 JavaScript 中的 HTTP 和 AJAX 请求世界。AJAX（异步 JavaScript 和 XML）是一种网页开发技术，允许你在不重新加载整个页面的情况下更新页面的特定部分。这为用户带来了更动态、更流畅的体验。

### 1. HTTP 请求

HTTP 请求用于与网页服务器发送和接收数据。有不同类型的 HTTP 请求，例如`GET`、`POST`、`PUT`、`DELETE`等。理解它们之间的区别以及何时使用每种类型非常重要。

### 2. XMLHttpRequest

`XMLHttpRequest`对象用于在 JavaScript 中发出异步 HTTP 请求。它允许你向服务器发送请求、接收响应，并用接收到的数据更新页面的特定部分。你可以使用不同的属性配置`XMLHttpRequest`对象，例如请求方法、请求头和参数。

### 3. 回调和 Promise

HTTP 请求是异步的，这意味着代码不会等待响应就继续执行。

通常使用回调或 Promise 来处理请求的结果。回调是作为参数传递的函数，在请求完成时执行。Promise 是一种更现代的方法，允许你编写更具可读性和模块化的代码。

### 4. 错误处理

在进行 HTTP 请求时，处理与服务器通信中可能出现的错误和失败非常重要。你可以使用`try-catch`块或`XMLHttpRequest`对象的`onerror`方法来处理异常，并向用户显示适当的错误消息。

### 5. REST API

REST（表述性状态转移）API 是一种通过 HTTP 请求提供对服务器数据和功能访问的常见方式。它们遵循特定的通信和数据结构原则。理解如何在 JavaScript 中使用 AJAX 和 HTTP 请求与 REST API 进行通信和交互非常重要。

**额外提示：**

除了`XMLHttpRequest`，还有一些现代库使得在 JavaScript 中处理 HTTP 请求更加容易，例如 Fetch API 和`axios`。它们具有更简单的语法，并提供了高级功能，例如 Promise 支持。

希望这个解释能帮助你更好地理解面向 JavaScript 初学者的 AJAX 和 HTTP 请求这一章。请记住，深入钻研一个特定主题很重要，不要只停留在基础知识上！

## 第13章：错误处理

错误处理是任何语言编程的重要组成部分，JavaScript 也不例外。

当你用 JavaScript 编写代码时，可能会出现错误和异常的情况，从而中断程序的正常执行。

为了防止这些错误使程序完全停止运行，你可以实现错误处理技术。

### 1. JavaScript 中的错误

#### 语法错误

当你编写的代码不符合语言的正确语法时发生。

#### 运行时错误

在程序执行期间发生，当出现意外情况时，例如将数字除以零或访问未定义的变量。

#### 逻辑错误

当程序逻辑不正确，导致意外或不正确的结果时发生。

### 2. `try-catch`语句

`try-catch`语句用于包裹一个可能引发异常的代码块。`try`代码块包含将要执行的代码以及可能抛出异常的部分代码。如果抛出异常，则执行`catch`代码块，允许你适当地处理异常。

```javascript
try {
    // 可能生成异常的代码块
} catch (error) {
    // 处理异常的代码块
}
```

### 3. 抛出异常

除了处理异常，你还可以使用`throw`语句手动抛出异常。在抛出异常时，你可以指定一个代表错误消息的值。

此消息可用于提供有关异常的更详细信息以进行调试，或者告诉用户程序中出了什么问题。

```javascript
throw new Error("错误消息");
```

### 4. `finally`块

`finally`块是可选的，可以与`try-catch`块结合使用。它包含一段无论是否发生异常都将执行的代码块。`finally`块通常用于处理清理任务，例如关闭数据库连接或释放资源。

```javascript
try {
  // 可能生成异常的代码块
} catch (error) {
  // 处理异常的代码块
} finally {
  // 无论是否发生异常都将执行的代码块
}
```

### 5. 自定义异常

除了 JavaScript 提供的标准异常之外，你还可以使用`throw`函数创建自己的自定义异常。这允许你定义具有特定行为和自定义错误消息的异常。

```javascript
class MyException extends Error {
    constructor(message) {
        super(message);
        this.name = "MyException";
    }
}

throw new MyException("Custom error message");
```

错误处理是每位 JavaScript 程序员必备的技能。

通过使用错误处理技术，你可以确保代码更加健壮，并能妥善处理意外情况。请记住，良好的错误管理与编写简洁、高效的代码之间的平衡非常重要。

## 第14章：ECMAScript 6

ECMAScript 6，也称为 ES6 或 ES2015，是 JavaScript 的高级特性。ES6 是 JavaScript 的新版本，为该语言引入了多项强大的改进和新特性。

### 1. 常量（`const`）和变量（`let`）

在 ES6 中，你可以使用`let`关键字声明变量，使用`const`声明常量。

它们之间的区别在于常量不能被重新赋值，而变量可以。

### 2. 箭头函数

箭头函数是 JavaScript 中一种更紧凑的函数编写方式。它们提供了简化的语法，并使得访问`this`值更加容易。例如：

```javascript
const sum = (a, b) => a + b;
```

### 3. 模板字面量

模板字面量允许你创建可以包含内联表达式的字符串。

你可以使用反引号（`` ` ``）包裹字符串，并使用`` `${}` ``在其中插入表达式。例如：

```javascript
const name = "João";
console.log(`Hello, ${name}!`); // Output: Hello, João!
```

### 4. 解构

解构允许你将数组或对象中的值提取到单独的变量中。在处理复杂数据时这非常有用。例如：

```javascript
const [a, b] = [1, 2];
console.log(a, b); // Output: 1 2
const { name, age } = { name: "Maria", age: 30 };
console.log(name, age); // Output: Maria 30
```

### 5. 剩余参数和展开运算符

剩余参数允许你向函数传递可变数量的参数。展开运算符允许你将一个数组或对象的元素展开到另一个数组或对象中。例如：

```javascript
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}
```

```javascript
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const array3 = [...array1, ...array2];
```

### 6. 类

ES6 引入了类语法，用于在 JavaScript 中创建对象。你可以定义一个带有构造函数的类，并为其添加方法。例如：

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

const animal = new Animal("dog");
animal.speak(); // Output: dog makes a noise.
```

以上只是 ES6 中涵盖的部分高级特性。还有许多其他特性，例如解构函数参数、模块、迭代器、Promise 等。

希望我能让你对 ES6 最重要的一些方面有了大致的了解。

## 第15章：实战项目

创建一个 JavaScript 游戏。在本章中，我们将探索使用 JavaScript 创建游戏的过程。

在开始讨论项目之前，需要强调的是，在 JavaScript 中创建游戏涉及一系列技能，包括编程逻辑、DOM（文档对象模型）操作，以及可能使用库或框架。

以下是创建 JavaScript 游戏时可以遵循的一些步骤：

### 1. 规划

在开始之前，制定一份关于游戏应该如何运行的详细计划非常重要。思考游戏目标、规则和用户交互。记录游戏流程、所需功能和期望的功能。

### 2. 环境搭建

现在你需要配置开发环境。这可能包括创建基本的文件结构、引入游戏专用的库或框架，以及搭建服务器在本地测试游戏。

### 3. 构建游戏逻辑

这是大部分工作完成的地方。你需要编写 JavaScript 代码来实现游戏逻辑。

这可以包括定义和操作变量、创建处理游戏事件的函数，以及根据玩家的操作更新用户界面。

### 4. DOM 操作

为了在屏幕上显示游戏，你需要操作 DOM。这包括选择相关的 HTML 元素、修改它们的属性和内容、根据需要添加或删除元素，以及处理用户事件。

### 5. 测试与改进

在开发游戏的过程中，定期测试以确保一切正常运行非常重要。找出错误、进行修正并再次测试。同时也可以借此机会寻求他人的反馈，以改善游戏体验。

### 6. 发布

一旦你完成了游戏并确认其按预期运行，就该发布了。这可能涉及将游戏托管到服务器上、优化其性能，以及创建着陆页或链接以便与他人分享。

在整个游戏创建过程中，请记得查阅相关文档、寻找代码示例，并探索可用的资源来帮助你学习和提升 JavaScript 技能。

#### 让我们来看一个小型示例项目

在这个项目中，我们将制作一个带有背景音乐、用于显示分数的`div`以及若干其他元素的基础游戏。

例如，我们将有一辆警车、屏幕上出现一些罪犯，你可以使用键盘上的方向键移动警车。

每当你与敌人碰撞时，会播放警车音效，你的分数加一分。

当敌人出现时，你会听到枪声音效。

以下是完整代码的示例，使用了本书中学到的部分内容。我已经对代码添加了注释，以便更容易理解。

```html
<!DOCTYPE html>
<html>
<head>
  <style>
```

```css
/* ... (CSS 样式) ... */
body {
  background-image: url(imgs/bg.png);
  background-size: cover;
  width: 100%;
  height: 100%;
  margin: 0;
  overflow: hidden;
  width: 100%;
  height: 100%;
  margin: 0;
  overflow: hidden;
}
.bg {
  top: 25%;
  left: 25%;
  background-image: url(imgs/street.png);
  background-size: auto;
  margin: 0;
  overflow: hidden;
  display: flex;
  position: absolute;
  width: 50%;
  height: 400px;
```

```css
align-items: flex-end;
}
.player {
    display: flex;
    background-image: url(imgs/police.png);
    background-size: 100%;
    background-repeat: no-repeat;
    overflow: hidden;
    width: 36px;
    height: 56px;
    border-radius: 50%;
    position: absolute;
    color: #f8f8f8;
    font-size: 22px;
    padding: 6px;
}
.enemy {
    display: flex;
    background-image: url(imgs/bad_guy.png);
    background-size: 100%;
    background-repeat: no-repeat;
    overflow: hidden;
    width: 18px;
    height: 28px;
```

```css
border-radius: 50%;
position: absolute;
color: #f8f8f8;
font-size: 22px;
padding: 6px;
}

.score {
	margin-left: 25%;
	margin-top: 16%;
	background-color: #fff;
	max-width: 50%;
	font-size: 32px;
	font-weight: bold;
}

</style>
</head>
<body>

<!--背景音乐 -->
<audio id="myAudio" loop>
  <source src="sound/bg.wav" type="audio/wav">
</audio>

<!-- 分数元素 -->
<div id="score" class="score"></div>

<!-- 背景（街道）元素，包含玩家 -->
```

```html
<div class="bg" id="bg">
    <span id="player" class="player"></span>
</div>
<script>
    // 初始分数
    let score = 0;
    // 获取音频元素的引用
    var audio = document.getElementById("myAudio");
    // 按键事件：按下上方向键时播放音频
    document.addEventListener('keydown', function(event) {
        switch (event.code) {
            case 'ArrowUp':
                audio.play();
                break;
        }
    });
    // 获取 DOM 元素的引用
    const bg = document.getElementById('bg');
    const player = document.getElementById('player');
    let currentPositionX = 0;
    let currentPositionY = 0;
    // 按键事件：移动玩家并检测碰撞
    document.addEventListener('keydown', function(event) {
        const bgWidth = bg.offsetWidth;
```



```javascript
const bgHeight = bg.offsetHeight;
switch (event.code) {
  case 'ArrowUp':
    if (currentPositionY >= -310) {
      currentPositionY -= 16;
    }
    break;
  case 'ArrowDown':
    if (currentPositionY <= -16) {
      currentPositionY += 16;
    }
    break;
  case 'ArrowRight':
    currentPositionX += 20;
    currentPositionX = Math.min(currentPositionX, bgWidth - 30);
    break;
  case 'ArrowLeft':
    currentPositionX -= 20;
    currentPositionX = Math.max(currentPositionX, 0);
    break;
}
// 移动玩家
player.style.transform = `translate(${currentPositionX}px, ${currentPositionY}px)`;
// 碰撞检测

const enemies = document.querySelectorAll('.enemy');
enemies.forEach(enemy => {
    if (checkCollision(player, enemy)) {
        // 移除敌人
        enemy.remove();
        // 更新分数
        var scoreElement = document.getElementById("score");
        score = score + 1;
        var novaPontuacao = score;
        scoreElement.innerText = "已抓捕罪犯: " + novaPontuacao;
        // 播放警察音效
        var audio1 = new Audio('sound/police.wav');
        audio1.play();
    }
});
// 在背景图指定区域内创建敌人的函数
function createEnemy() {
    const enemy = document.createElement('div');
    enemy.classList.add('enemy');
    const enemySize = 25;
    const maxX = bg.clientWidth - enemySize;
    const maxY = -250 - enemySize;
    const randomX = Math.floor(Math.random() * maxX);

    const randomY = Math.floor(Math.random() * maxY);

    // 定位敌人
    enemy.style.transform = `translate(${randomX}px, ${randomY}px)`;
    bg.appendChild(enemy);
    return enemy;
}

// 创建敌人
for (let i = 0; i < 4; i++) {
  createEnemy();
}

// 每100毫秒检测与敌人的碰撞
setInterval(function() {
  const enemies = document.querySelectorAll('.enemy');
  enemies.forEach(enemy => {
    if (checkCollision(player, enemy)) {
      // 移除敌人
      enemy.remove();
    }
  });
}, 100);

// 每5000毫秒（5秒）添加一个敌人
setInterval(function() {
  // 播放枪声音效
  var audio2 = new Audio('sound/shot.wav');
  audio2.play();
  // 创建一个新敌人
  createEnemyZH();
}, 5000);

// 检测两个元素之间碰撞的函数
function checkCollision(element1, element2) {
  const rect1 = element1.getBoundingClientRect();
  const rect2 = element2.getBoundingClientRect();
  return (
    rect1.left < rect2.right &&
    rect1.right > rect2.left &&
    rect1.top < rect2.bottom &&
    rect1.bottom > rect2.top
  );
}

</script>
</body>
</html>
```

请记住，创建游戏是一个迭代的过程。你很可能会在过程中遇到挑战，但请不要气馁。坚持和练习是成为一名优秀 JavaScript 游戏开发者的必备要素。

希望这些信息能帮助你开启你的 JavaScript 游戏项目！

学习愉快！

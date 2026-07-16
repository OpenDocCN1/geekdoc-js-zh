# 终极 JavaScript 全课程：从基础到高级概念的全面指南——你的编程世界之旅



![](img/image_rsrc1AR.jpg)

# 简介

## 欢迎来到课程！
欢迎学习 JavaScript 课程！在这书中，你将学习入门 JavaScript 所需的所有知识。JavaScript 是一种多功能且广泛使用的编程语言，主要用于创建交互式网站。无论你是完全初学者还是已经具有某些编程经验，这本书都将帮助你建立坚实的 JavaScript 基础。

## 给参与者的提示
在我们开始之前，这里有一些建议可以帮助你上手：

• 熟能生巧：编程是一项实践性技能。练习得越多，表现得就越好。
• 错误是正常的：每个人都会犯错，尤其是刚开始。。是学习过程中重要的一部分。从错误中学习，不要放弃！
• 提问：如果你不理解某些内容，请寻找答案。利用在线资源、论坛和社区来寻求支持。
• 保持好奇心：JavaScript 提供了无限可能。通过探索和实验不断扩展你的技能。

## 在课程中你将学到什么？
在本课程中，你将逐步学习 JavaScript 的基础。我们将从基本概念开始，逐步进入高级的主题。以下是等待你的话题概述：

1. 准备：所需软件的安装与设置。
2. JavaScript 基础：介绍以及你的第一个 JavaScript 程序。
3. 变量：处理变量和数据类型。
4. 运算符：数学和逻辑操作。
5. 控制结构：条件和循环。
6. 函数：函数的定义和使用。
7. 对象：操作对象及其方法。
8. 数组：数组的基础和高级函数。
9. DOM：文档对象模型（Document Object Model）。
10. 事件和事件处理：处理用户输入和事件。
11. 异步编程：Promises 和 `async/await` 介绍。
12. 错误处理与调试：处理代码中的错误。
13. JavaScript 库和框架：流行工具概述。
14. 项目实：创建一个简单的 Web 应用程序。
15. 更多资源：进一步学习的技巧和资源。

本书的结构设计让你随时可以返回并回顾某个主题。每个章节都建立在前章节的基础上，因此在继续之前，请确保你已经理解了基础。

# 准备

## 安装和设置代码编辑器 (Visual Studio Code)
在开始编写 JavaScript 之前，你需要一个代码编辑器。我们推荐 Visual Studio Code (`VS Code`)，因为它功能强大、免费且非常用户友好。以下是安装和设置的步骤：

1. 下载与安装：
- 访问 Visual Studio Code 网站。
- 下载适用于你操作系统的版本（Windows, macOS 或 Linux）。
- 按照安装说明进行。
2. 首次安装：
- 安装后启动 Visual Studio Code。
- 设置你喜好的配色方案（浅色或深色）。
- 安装重要的扩展：
- `ESLint`：用于检查代码中的错误。
- `Prettier`：用于代码的自动格式化。
- `JavaScript (ES6) code snippets`：提供方便的代码片段。
3. 创建新项目：
- 打开 Visual Studio Code。
- 点击“File” > “Open”，并为你的项目创建一个文件夹。
- 创建一个扩展名为 `.js` 的新文件（例如 `index.js`）。

## 安装浏览器 (Google Chrome)
网页浏览器对于测试你的 JavaScript 程序是必要的。我们推荐 Google Chrome，因为它提供了强大的开发者工具，可以帮助你进行调试和测试。

1. 下载与安装：
- 访问 Google Chrome 网站。
- 下载并安装适用于你操作系统的版本。
2. 开发者工具：
- 打开 Google Chrome。
- 按 `F12` 或 `Ctrl + Shift + I` (Windows/Linux) 或 `Cmd + Option + I` (macOS) 打开开发者工具。
- 使用 `"Console"` 标签直接在浏览器中执行和测试 JavaScript 代码。

完成这些准备后，你现在准备好进入 JavaScript 的世界了。在下一章，我们将学习 JavaScript 的基础并编写我们的第一个小程序。

# JavaScript 基础

## JavaScript 简介
JavaScript 是万维网的三大核心技术之一（另外 HTML 和 CSS）。HTML 负责结构，CSS 负责设计，而 JavaScript 则实现了网站的交互性。它被几乎每个现代浏览器支持，是世界上最广泛使用的编程语言之一。

### 为什么选择 JavaScript？
• 易于学习：JavaScript 是一种对初学者友好的语言。
• 广泛使用：拥有庞大的社区和丰富的资源。
• 灵活：JavaScript 可以用于简单的脚本也可以用于复杂的 Web 应用程序。
• 交互性：实现动态内容和用户交互。

## 你的第一个 JavaScript 程序：Hello world!
在我们深入研究之前，我们将编写一个简单的“Hello world!”程序，向你展示如何在 HTML 文件中使用 JavaScript。

1. 创建一个 HTML 文件：创建一个新文件并命名为 `index.html`。添加以下 HTML 代码：

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initialscale=1.0">
<title>Hello world</title>
</head>
<body>
<h1>Hello world!</h1>
<script src="script.js"></script>
</body>
</html>
```

2. 创建一个 JavaScript 文件：创建一个新文件并命名为 `script.js`。添加以下 JavaScript 代码：
```javascript
alert('Hello world!');
```

3. 运行你的程序：在浏览器中打开 `index.html` 文件。你应该会看到一个显示“Hello world!”的弹出窗口。

## 最后的准备，然后我们开始吧！
在深入学习之前，请确保你已经理解并设置了以下几点：

1. 目录结构：一个包含 HTML、CSS 和 JavaScript 文件的清晰目录结构。
2. 代码编辑器：确保你的代码编辑器（例如 `VS Code`）配置正确并且你对其熟悉。
3. 浏览器开发者工具：熟悉浏览器的开发者工具。这些工具将帮助你调试代码。

你现在已经为 JavaScript 打定了基础。在下一章节中，我们将学习变量，这是每个语言的基础概念之一。

# 变量

## JavaScript 中的变量
变量是存储数据的地方，它是每个语言的基础组件。在 JavaScript 中，你可以使用 `var`、`let` 和 `const` 来声明变量。

### 示例
```javascript
let name = 'Max'; const pi = 3.14; var age = 25;
```
• `let` 和 `const` 是 ES6 引入的，是更现代的变量声明方法。
• `var` 较老，且作用域有所不同。

## 变量命名
变量命名遵循某些规则：
• 仅允许包含字母、数字、下划线和美元符号。
• 不能以数字开头。
• 不能使用关键字（如 `let`、`const`、`var`、`function` 等）。

### 示例
```javascript
let myName = 'Sarah'; let _age = 30; let $currency = 'USD';
```

## 原始数据类型 - 字符串、数字和布尔
JavaScript 有多种数据类型可以保存在变量中。最重要的原始数据类型是
• 字符串：表示文本的字符序列。
• 数字：整数和浮点数。
• 布尔值：可以是 `true` 或 `false` 的真值。

### 示例
```javascript
let firstName = 'John'; // 字符串 let age = 25; // 数字
let isStudent = true; // 布尔
```

## 修改变量的值
一旦声明，可以在 JavaScript 中更改变量的值（`const` 除外）。

### 示例
```javascript
let city = 'Berlin';
city = 'Hamburg'; // city 变量的值被改变
```

## let vs const
• `let`：用于声明可以更改的变量。





### const
- `const`: 用于声明不可更改的变量。初始化后值不能再被改变。

### 示例
```javascript
let age = 25;

age = 26; // 这是允许的

const birthYear = 1995;

birthYear = 1996; // 这将导致错误
```

## 使用 prompt() 获取用户输入
你可以使用 `prompt()` 函数向用户获取输入。

### 示例
```javascript
let userName = prompt('What is your name?'); console.log('Hello, ' + userName + '!');
```

## 注释
注释对于记录代码和使其更容易理解非常有用。分为单行注释和多行注释。

### 单行注释
```javascript
// 这是一个单行注释
```

### 多行注释
```javascript
/*
这是一个
多行注释 */
```
以上就是 JavaScript 变量的基础知识。在下一章节中，我们将介绍错误，以及当您遇到问题时如何寻找答案和提问。

# 深入探讨：错误

## 寻找答案和提问
错误是编程中不可避免的一部分，特别是在学习新语言时。最重要的是你如何处理它们并学会修复它们。以下是一些在你遇到 bug 时可以帮助到你的技巧和资源。

### 常见错误类型
1. 语法错误：当代码不符合语言规则时发生。
   - 示例：`let x = ;`（缺少值）
2. 运行时错误：当代码执行但发生问题时。
   - 示例：访问未定义的变量。
3. 逻辑错误：当代码执行没有错误但没有得到预 result 结果时。
   - 示例：由于运算符错误导致计算错误。

### 故障排除
1. 阅读错误信息：控制台中的错误信息通常提供关于问题及其发生位置的信息。
2. 逐步检查代码：将你的代码分成小部分并检查每一步。
3. 使用控制台：使用 `console.log()` 检查值和变量。
   - 示例：`console.log('The value of x is: ', x);`

### 使用在线资源
有很多在线资源可以帮助你找到问题的答案：
1. Stack Overflow：程序员最大的社区之一。在这里你可以提问并从经验丰富的开发者那里获得答案。
2. Mozilla 开发者网络 (MDN)：极佳的 JavaScript 文档和示例资源。
3. W3Schools：另一个用于教程和参考的实用网站。
   - W3Schools JavaScript 教程

### 提问
在网上提问时，请确保你的表述清晰准确。以下是一些关于如何提问好问题的技巧：
1. 描述问题：准确解释你想实现什么以及哪些部分不起工作。
2. 代码示例：插入显示问题的相关代码段。
3. 错误信息：复制并粘贴你收到的准确错误信息。
4. 之前的尝试：描述你已经尝试过哪些解决问题的方法。

### 一个好问题的示例
### 问题：
我正尝试编写一个简单的 JavaScript 函数来相两个数字，但我收到了一个错误信息。

### 代码：
```





```javascript
function addNumbers(a, b) {
  return a + b;
}
let result = addNumbers(5, '10'); console.log(result);
```

### 错误信息：

Uncaught TypeError: Cannot add property 'toString' of undefined

### 我目前尝试过的：

我尝试过将两个参数都转换为数字，但错误仍然存在。

```yaml
--
```

错误是编程的一部分，也是一个宝贵的学习机会。在接下来的章节中，我们将介绍运算符，这是 JavaScript 中的另一个重要概念。

--

# 运算符

## 数学运算符

数学运算符用于执行基本的算术运算。以下是最重要的运算符：

- `+` (加法)：将两个数字相加。
- `-` (减法)：从一个数字减去另一个数字。
- `*` (乘法)：将两个数字相乘。
- `/` (除法)：将一个数字除以另一个数字。
- `%` (取模)：返回除法的余数。
- `**` (幂)：计算数字的次方。

### 示例

```javascript
let a = 10; let b = 3;

console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.3333333333333335 console.log(a % b); // 1
console.log(a ** b); // 1000
```

## 字符串拼接与多行字符串

字符串的拼接也使用 `+` 运算符。

### 示例

```javascript
let firstName = 'John';
let lastName = 'Doe';
let fullName = firstName + ' ' + lastName;

console.log(fullName); // John Doe
```

### 多行字符串

多行字符串可以使用反引号（`` ` ``）创建。

### 示例

```javascript
let message = `This is a multiline
String `;

console.log(message);
```

## 模板字符串与多行模板字符串

模板字符串允许你使用 `${}` 将变量和表达式插入字符串中。

### 示例

```javascript
let name = 'Alice';
let greeting = `Hello, ${name}! console.log(greeting); // Hello, Alice!
```

## 数字的比较运算符

比较运算符用于比较两个值。它们返回一个布尔值（true 或 false）。

- `==` (等于)：检查值是否相等。
- `!=` (不等于)：检查值是否相等。
- `===` (严格相等)：检查值和类型是否相等。
- `!==` (严格不相等)：检查值或类型是否不相等。
- `>` (大于)：检查左侧值是否大于右侧值。
- `<` (小于)：检查左侧值是否小于右侧值。
- `>=` (大于等于)：检查左侧值是否大于或等于右侧值。
- `<=` (小于等于)：检查左侧值是否小于或等于右侧值。

### 示例

```javascript
let x = 5; let y = 10;

console.log(x == y); // false console.log(x != y); // true console.log(x === y); // false console.log(x !== y); // true console.log(x > y); // false console.log(x < y); // true console.log(x >= y); // false console.log(x <= y); // true
```

## 字符串的比较运算符

比较运算符也可以应用于字符串。比较基于字典顺序（字母顺序）。

### 示例

```javascript
let str1 = 'apple'; let str2 = 'banana';

console.log(str1 == str2); // false
console.log(str1 != str2); // true
console.log(str1 < str2); // true (apple 排在 banana 之前) console.log(str1 > str2); // false
```

## JavaScript 中的类型安全

JavaScript 是一种动态类型语言，这意味着变量的类型是在运行时确定的。因此，理解 `==` 和 `===` 的区别非常重要。

- `==` 只检查值的相等性。
- `===` 同时检查值和类型的相等性。

### 示例

```javascript
let num = 5; let str = '5';
console.log(num == str); // true (只比较值) console.log(num === str); // false (比较了值和类型)
```

## 逻辑运算符

逻辑运算符用于组合布尔值并评估逻辑表达式。

- `&&` (逻辑与)：如果两个操作数都为 true，则返回 true。
- `||` (逻辑或)：如果其中一个操作数为 true，则返回 true。
- `!` (逻辑非)：返回值的反值。

### 示例

```javascript
let a = true; let b = false;

console.log(a && b); // false console.log(a || b); // true console.log(!a); // false console.log(!b); // true
```

以上是 JavaScript 的基本运算符。在下一个章节中，我们将介绍允许你在代码中创建条件语句的控制结构。

# 控制结构 I

## if 语句

`if` 语句用于检查条件，仅当条件为真时才执行代码。

### 语法

```javascript
if (condition) {
  // 如果条件为真则执行代码
}
```

### 示例

```javascript
let age = 18;

if (age >= 18) {
  console.log('You are of legal age.');
}
```

在这个示例中，只有当 `age` 变量大于或等于 18 时，才会显示“You are of legal age.”

## if-else 语句

使用 `if-else` 语句，你可以在条件为真时执行代码，在为假时执行其他代码。

### 语法

```javascript
if (condition) {
  // 如果条件为真则执行代码
} else {
  // 如果条件为假则执行代码
}
```

### 示例

```javascript
let age = 16;

if (age >= 18) {
  console.log('You are of legal age.');
} else {
  console.log('You are underage.');
}
```

在这个示例中，因为 `age` 小于 18，所以显示“You are underage.”

## else-if 语句

`else-if` 语句允许检查多个条件。如果第一个条件为假，则检查下一个条件。

### 语法

```javascript
if (condition1) {
  // 如果 condition1 为真则执行代码
} else if (condition2) {
  // 如果 condition2 为真则执行代码
} else {
  // 如果所有条件都为假则执行代码
}
```

## 嵌套 if 语句

你可以在 `if` 语句内部嵌套其他 `if` 语句来检查复杂的条件。

# 函数

## 函数基础

函数是执行特定任务的可重用代码块。它们有助于代码模块化和可读性。JavaScript 有多种定义函数的方法。

### 语法

```javascript
function name(parameters) {
  // 执行代码
}
```

### 示例

```javascript
function greet() {
  console.log('Hello, world!');
}
greet();
```

## 带参数的函数

函数可以参数作为输入。

### 语法

```javascript
function name(parameters) {
  // 执行代码
}
```

### 示例

```javascript
function greet(name) {
  console.log('Hello, ' + name + '!');
}
greet('Max'); // Output: Hello, Max!

## 带默认参数的函数

默认参数允许在未传递参数时定义值。

### 语法

```javascript
function name(parameter = defaultValue) {
  // 执行代码
}
```

### 示例

```javascript
function greet(name = 'World') {
  console.log('Hello, ' + name + '!');
}
greet(); // Output: Hello, World!
```

## return 语句

函数可以使用 `return` 语句返回值。

### 语法

```javascript
function name(parameters) {
  // 执行代码
  return value;
}
```

### 示例

```javascript
function add(a, b) {
  return a + b;
}
let sum = add(5, 3);
console.log(sum); // Output: 8
```

## 作用域

作用域决定了变量的可访问性。变量有两种主要类型：全局和局部。

### 全局作用域

在函数外部声明的变量具有全局作用域，在代码的任何地方都可以访问。

### 局部作用域

在函数内部声明的变量具有局部作用域，仅在该函数内部可用。

### 示例

```javascript
let globalVar = 'I am global';

function myFunction() {
  let localVar = 'I am local';
  console.log(globalVar); // 可以访问
}

myFunction();
// console.log(localVar); // Error: localVar is not defined
```

## 提升

提升是 JavaScript 中的一种行为，变量和函数的声明会被移动到它们所在作用域的顶部。

### 示例

```javascript
console.log(myVar); // undefined
var myVar = 'Hello';

function myFunc() {
  return 'World';
}
console.log(myFunc()); // Output: World
```

## 函数表达式 vs. 函数声明（提升）

定义函数有两种方式：函数声明和函数表达式。函数声明会被提升，而函数表达式则不会。

### 函数声明

```javascript
function greet() {
  return 'Hello';
}
console.log(greet()); // Hello
```

### 函数表达式

```javascript
console.log(greet()); // Error: greet is not defined

let greet = function() {
  return 'Hello';
};
```

# 对象

## 对象基础

对象是 JavaScript 中的基本构建块，允许在结构中组织相关数据和函数。对象由属性和方法（函数）组成。

### 语法

```javascript
let obj = {
  key1: value1,
  key2: value2,
  // 方法
  methodName: function() {
    // 代码
  }
};
```

### 示例

```javascript
let person = {
  name: 'Max',
  age: 30,
  greet: function() {
    console.log('Hello, I am ' + this.name);
  }
};
person.greet(); // Output: Hello, I am Max
```

## 嵌套对象

对象的属性可以是另一个对象。

### 示例

```javascript
let address = {
  city: 'Berlin',
  postalCode: '12345'
};

let person = {
  name: 'Max',
  address: address
};
console.log(person.address.city); // Output: Berlin
```

## 读取和设置值（点符号）

你可以使用点符号访问和更改对象的属性。

### 示例

```javascript
let person = {
  name: 'Max',
  age: 30
};

console.log(person.name); // Output: Max
person.age = 31;
console.log(person.age); // Output: 31
```

## 读取和设置值（括号符号）

另一种，你可以使用方括号符号访问属性。

### 示例

```javascript
let person = {
  name: 'Max',
  age: 30
};

console.log(person['name']); // Output: Max
person['age'] = 31;
console.log(person['age']); // Output: 31
```

## 添加、更改和删除属性

你可以为对象添加、更改或删除属性。

### 示例

```javascript
let person = {
  name: 'Max',
  age: 30
};

// 添加
person.gender = 'male';
console.log(person.gender); // Output: male

// 修改
person.age = 31;
console.log(person.age); // Output: 31

// 删除
delete person.age;
console.log(person.age); // Output: undefined

# 控制结构 II

## switch 语句

`switch` 语句用于检查多个条件。它是长 `if-else` 链的良好替代方案。

### 语法

```javascript
switch (expression) {
  case value1:
    // 当 expression === value1 时执行代码
    break;
  case value2:
    // 当 expression === value2 时执行代码
    break;
  default:
    // 如果没有 case 匹配则执行代码
}
```

### 示例

```javascript
let fruit = 'Banana';

switch (fruit) {
  case 'Apple':
    console.log("It's an apple.");
    break;
  case 'Banana':
    console.log("It's a banana.");
    break;
  case 'Orange':
    console.log("It's an orange.");
    break;
  default:
    console.log("Unknown fruit.");
}
```

在这个示例中，因为 `fruit` 等于 'Banana'所以输出“It's a banana.”

# 数组 I：基础

## 数组基础

数组是用于在单个变量中存储多个值的数据结构。数组中的每个值都有一个索引，从 0 开始。

### 语法

```javascript
let array = [element1, element2, element3];
```

### 示例

```javascript
let fruits = ['apple', 'banana', 'orange'];
console.log(fruits[0]); // Output: apple
console.log(fruits[1]); // Output: banana
console.log(fruits[2]); // Output: orange
```

## 数组是特殊的

在 JavaScript 中，数组是特殊的对象。它们拥有专门为处理列表开发的额外方法和属性。

### 示例

```javascript
let fruits = ['apple', 'banana', 'orange'];
console.log(typeof fruits); // Output: object
```

## 多维数组

多维数组包含其他数组作为元素。这对于显示矩阵或表格非常有用。

### 示例

```javascript
let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
console.log(matrix[0][0]); // Output: 1
console.log(matrix[1][2]); // Output: 6
```

# 数组 II：高级用户功能

## 过滤数组

`filter` 方法创建一个新数组，其中包含所有符合特定元素的。条件由回调函数定义。

### 语法

```javascript
let newArray = array.filter(callback);
```

### 示例

```javascript
let numbers = [1, 2, 3, 4, 5, 6];
let evenNumbers = numbers.filter(function(number) {
  return number % 2 === 0;
});
console.log(evenNumbers); // Output: [2, 4, 6]
```

可以使用不同的方法向数组添加或删除元素。

## push() 和 pop()

- `push(element)`：向数组末尾添加一个元素。
- `pop()`：移除数组的最后一个元素并返回它。

### 示例

```javascript
let fruits = ['apple', 'banana'];
fruits.push('orange');
console.log(fruits); // Output: ['apple', 'banana', 'orange']

let last = fruits.pop();
console.log(last); // Output: orange
console.log(fruits); // Output: ['apple', 'banana']
```

## unshift() 和 shift()

- `unshift(element)`：向数组开头添加元素。
- `shift()`：移除数组的第一个元素并返回它。

### 示例

```javascript
let fruits = ['apple', 'banana'];
fruits.unshift('orange');
console.log(fruits); // Output: ['orange', 'apple', 'banana']

let first = fruits.shift();
console.log(first); // Output: orange
console.log(fruits); // Output: ['apple', 'banana']
```

## 使用 includes(), indexOf() 和 lastIndexOf() 数组

- `includes(element)`：检查是否存在特定元素，返回 true 或 false。
- `indexOf(element)`：返回元素在数组中的第一次索引，找不到则返回 -1。
- `lastIndexOf(element)`：返回元素在数组中的最后一个索引，找不到则返回 -1。

### 示例

```javascript
let fruits = ['apple', 'banana', 'apple'];
console.log(fruits.includes('banana')); // Output: true
console.log(fruits.indexOf('apple')); // Output: 0
console.log(fruits.lastIndexOf('apple')); // Output: 2
```

## Sets

`Set` 是一个值的集合，每个值只出现一次。

### 创建 Set

```javascript
let set = new Set();
```

### 添加值

```javascript
let set = new Set();
set.add(1);
set.add(2);
set.add(1); // 1 已经存在，不会重复添加
```

### 检查值是否存在

```javascript
let set = new Set([1, 2]);
console.log(set.has(1)); // Output: true
console.log(set.has(3)); // Output: false
```

### 删除值

```javascript
let set = new Set([1, 2, 3]);
set.delete(2);
console.log(set.has(2)); // Output: false
```

## Maps

`Map` 对象存储键值对，并记住键的插入顺序。

### 创建 Map

```javascript
let map = new Map();
```

### 添加值

```javascript
let map = new Map();
map.set('key1', 'value1');
map.set('key2', 'value2');
```

### 获取值

```javascript
let map = new Map();
map.set('key1', 'value1');
console.log(map.get('key1')); // Output: value1
```

### 删除值

```javascript
let map = new Map();
map.set('key1', 'value1');
map.delete('key1');
console.log(map.get('key1')); // Output: undefined
```

## 箭头函数 ("fat arrow syntax")

箭头函数是 ES6 引入的紧凑语法。它们与普通函数在 `this` 行为上不同。

### 语法

```javascript
const myFunction = (param1, param2) => {
  return result;
};
```

### 示例

```javascript
const add = (a, b) => a + b; // 如果函数只有一行，可以省略括号
console.log(add(5, 3)); // Output: 15
```

## `this` 行为差异

箭头函数从周围上下文绑定 `this` 关键字。

### 示例

```javascript
function Person() {
  this.age = 0;
  setInterval(() => {
    this.age++;
    console.log(this.age);
  }, 1000);
}
let p = new Person();
```

## async 和 defer 属性

这些属性用于控制 HTML 中脚本的执行。

- `async`：脚本异步加载并在一旦可用立即执行。不会阻塞页面加载。
- `defer`：脚本异步加载，但只有在 HTML 文档完全解析后才执行。保留 `defer` 脚本的顺序。

```html
<script src="script.js" async></script>
<script src="script.js" defer></script>
```

## 三元运算符

三元运算符提供了条件表达式的紧凑语法。

### 语法

```javascript
condition ? expr1 : expr2;
```

### 示例

```javascript
let age = 18;
let status = (age >= 18) ? 'Adult' : 'Minor';
console.log(status); // Output: Adult
```

## 展开语法 (spread)

展开语法允许展开数组或对象。

### 数组示例

```javascript
let arr1 = [1, 2, 3];
let arr2 = [...arr1, 4, 5, 6];
console.log(arr2); // Output: [1, 2, 3, 4, 5, 6]
```

### 对象示例

```javascript
let obj1 = {a: 1, b: 2};
let obj2 = {...obj1, c: 3};
console.log(obj2); // Output: {a: 1, b: 2, c: 3}
```

## 剩余参数语法

剩余参数语法允许以数组形式接收数量的参数。

### 示例

```javascript
function sum(...numbers) {
  return numbers.reduce((acc, curr) => acc + curr, 0);
}
console.log(sum(1, 2, 3, 4)); // Output: 10
```


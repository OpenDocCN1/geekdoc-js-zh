# Web 设计师的 JavaScript





Lara Hogan 前言






















前言

我认识 Matt Marquis 很多年，他一直是我过的最有天赋的设计师之一。Matt 在理解设计与技术的交汇点方面具有独特的天赋，他能够将复杂的想法转化为美丽且实用的数字体验。他的工作给我带来了巨大的灵感，我很荣幸能为这本书写序言。

Matt 对设计社区做出了巨大贡献，他的工作帮助了许多人提高技能。他是一位出色的老师和导师，总是愿意与他人分享知识和经验。Matt 对网页设计世界的洞察对于任何想要成功的人来说都是无价之宝，他的工作帮助了我们许多人成为更好的设计师。

我深信，这本书对于任何想要学习更多网页设计的人来说都将是一个宝贵的资源，我期待 Matt 未来的表现。

引言

在过去的几十年里，网页发生了巨大的变化。它最初只是简单的静态页面的集合，现在已演变成了一个复杂的动态平台，用于我们生活的几乎方方面。这种变化是由技术的飞速进步以及对更具互动性和参与感的数字体验日益增长的需求驱动的。

在过去，网页设计主要是关于让事物看起来好看。今天，它还关乎创建既实用又令人享受的体验。这意味着设计师需要具备广泛的技能，包括设计原理、技术、心理学和营销学的知识。

在本书中，Matt Marquis 将探索网页设计的一些关键方面。他将涵盖视觉设计、用户界面、用户体验等许多主题。他还将提供一些你可以用来改进自己工作的实用技巧和方法。

无论你是初学者还是经验丰富的设计师，这本书都将带给你有收获的阅读体验。它将让你对网页设计世界有更深入的理解，并帮助你形成自己的风格。

我希望你喜欢这本书，就像我喜欢阅读它一样。

Lara Hogan





## HTML 基础

HTML (HyperText Markup Language) 是用于构建网页结构的标准标记语言。它通过各种标签（Tags）来定义页面的元素。

### 常用 HTML 标签
- `<html>`: 页面的根元素。
- `<head>`: 包含文档元数据（如标题、样式表等）。
- `<body>`: 包含网页的可可见内容。
- `<h1>` 到 `<h6>`: 定义不同层级的标题。
- `<p>`: 定义段落。
- `<a>`: 定义超链接。
- `<img>`: 定义图像。
- `<ul>`, `<li>`: 定义无序列表。
- `<ol>`, `<li>`: 定义有序列表。
- `<table>`: 定义表格。

## CSS 样式表

CSS (Cascading Style Sheets) 用于控制网页的呈现样式、布局和视觉效果。

### CSS 常用属性
- `color`: 设置文本颜色。
- `background-color`: 设置背景颜色。
- `font-size`: 设置字体大小。
- `margin`: 设置元素外边距。
- `padding`: 设置元素内边距。
- `border`: 设置元素边框。
- `display`: 控制显示模式（如 `block`, `inline`, `flex` 等）。

## JavaScript 交互

JavaScript 是一门脚本语言，用于为网页添加交互功能。

### DOM 操作
DOM (Document Object Model) 允许 JavaScript 动态访问 HTML 结构。
- `document.getElementById(id)`: 通过 ID 获取元素。
- `document.querySelector(selector)`: 通过选择器获取元素。
- `element.addEventListener()`: 添加事件监听。
- `element.innerHTML`: 修改元素内容。
- `document.createElement()`: 创建新元素。

## 示例代码

以下是一个简单的 HTML 页面结构示例：

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>示例页面</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1 id="title">欢迎来到我的网页</h1>
    <p class="description">这是一个通过 OCR 修复后的示例内容。</p>
    <button id="myBtn">点击我</button>

    <script src="script.js"></script>
</body>
</html>
```





## 1. 什么是 JavaScript?

JavaScript 是一种轻量级的解释型编程语言，遵循 ECMAScript 。它和 HTML 以及 CSS 一样，是网页的核心技术之一。虽然它主要用于制作交互网页，但也通过 Node.js 用于服务器端开发。

- JavaScript 是一种多功能的语言。
- 它在网页浏览器中被广泛使用。
- 它支持客户端和服务器开发。

## 2. 在 HTML 中引入 JavaScript

要在 HTML 文档中引入 JavaScript，你可以使用 `<script>` 标签。加载脚本有两种主要方式：`async` 和 `defer`。

```html
<script async></script>
<script defer></script>
```

- `async` 属性允许脚本在后台下载并在下载完成后立即执行。
- `defer` 属性允许脚本在后台下载，但会在 HTML 文档完全解析后才执行。

示例：
```html
<script src="script.js" async></script>
<script src="script.js" defer></script>
```

## 3. JavaScript 变量与常量

变量用于存储数据值。在 JavaScript 中，有三种声明变量的方式：`let`、`const` 和 `var`。

```javascript
let name = "John";
const age = 30;
var city = "London";
```

- `let` 用于可以重新赋值的变量。
- `const` 用于不可重新赋值的常量。
- `var` 是声明变量的旧方式，具有函数作用域。

## 4. JavaScript 数据类型

JavaScript 具有几种原始数据类型：

- 字符串 (String): `"Hello"`
- 数字 (Number): `42`, `3.14`
- 布尔值 (Boolean): `true`, `false`
- 未定义 (Undefined): 已声明但未赋值的变量
- 空 (Null): 刻意的空值
- 符号 (Symbol): 唯一标识符
- 大整数 (BigInt): 用于非常大的整数

## 5. JavaScript 函数

函数是执行特定任务的代码块。

```javascript
function greet(name) {
  return "Hello, " + name;
}

console.log(greet("World"));
```

你也可以使用箭头函数：

```javascript
const greet = (name) => `Hello, ${name}`;
```

## 6. JavaScript 控制流

控制流允许你在代码中做出决策。

```javascript
let hour = 15;

if (hour < 12) {
  console.log("Good morning");
} else if (hour < 18) {
  console.log("Good afternoon");
} else {
  console.log("Good evening");
}
```

循环用于重复代码：

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

## 7. JavaScript 数组

数组用于在一个变量中存储多个值。

```javascript
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits[0]); // Apple
fruits.push("Orange"); // 添加到末尾
console.log(fruits.length); // 4
```

## 8. JavaScript 对象

对象是属性（键值对）的集合。

```javascript
const user = {
  firstName: "Jane",
  lastName: "Doe",
  age: 25
};

console.log(user.firstName); // Jane
user.age = 26;
```

## 9. JavaScript DOM 操控

DOM（文档对象模型）允许 JavaScript 更改 HTML 内容和 CSS。

```javascript
const title = document.getElementById("title");
title.textContent = "New Title";

const btn = document.querySelector(".btn");
btn.style.backgroundColor = "red";
```

## 10. JavaScript 事件

事件是浏览器发生的动作，例如点击或按键。

```javascript
const button = document.querySelector("button");

button.addEventListener("click", () => {
  alert("Button clicked!");
});
```

## 11. JavaScript Fetch API

Fetch API 用于发送网络请求。

```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
```

## 12. JavaScript Async/Await

Async/Await 提供了一种更简洁的方式来处理异步操作。

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}
```





## JavaScript 基础

JavaScript 是一种允许你创建交互式网页的编程语言。它主要用于客户端脚本，但也可以通过 Node.js 在服务器端使用。

JavaScript 用于让网页具有交互性。例如，你可以用它来验证表单数据、创建图像轮播器或更新页面上的内容。

要使用 JavaScript，你可以使用 `<script>` 标签将其直接嵌入到 HTML 页面中。

```html
<script>
  console.log("Hello World");
</script>
```

### 变量

在 JavaScript 中，变量用于存储数据值。声明变量有方式：`var`、`let` 和 `const`。

- `var` 是声明变量的旧方式。它是函数作用域的，并且可以重新声明。
- `let` 是声明变量的现代方式。它是块作用域的。
- `const` 用于声明不可重新赋值的变量。

```javascript
let name = "John";
let age = 25;
const pi = 3.14;
```

### 数据类型

JavaScript 有若干种内置数据类型：

- String（字符串）：表示文本。
- Number（数字）：表示整数和浮点数。
- Boolean（布尔值）：表示逻辑实体（true 或 false）。
- Array（数组）：一种类似列表的对象。
- Object（对象）：相关数据的集合。
- Undefined（未定义）：未赋值的变量。
- Null（空）：表示刻意缺失的任何值。

```javascript
let str = "Hello";
let num = 42;
let bool = true;
let list = ["apple", "banana", "cherry"];
let person = { name: "Alice", age: 30 };
```

### 函数

函数是用于执行特定任务的代块。你可以使用 `function` 关键字定义函数。

```javascript
function greet(name) {
  return "Hello, " + name + "!";
}

console.log(greet("World"));
```

### 对象

JavaScript 中的对象是属性的集合。每个属性都是键值对。你可以使用点符号法或括号表示法来访问对象属性。

```javascript
let car = {
  brand: "Toyota",
  model: "Corolla",
  year: 2022
};

console.log(car.brand); // Toyota
console.log(car["model"]); // Corolla
```

### 控制流

控制流允许你根据条件执行不同的代码。

#### If-Else 语句

```javascript
let age = 18;
if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```

#### 循环

循环用于多次重复代码。

```javascript
// For 循环
for (let i = 0; i < 5; i++) {
  console.log("Iteration " + i);
}

// For...of 循环
let fruits = ["apple", "banana", "orange"];
for (let fruit of fruits) {
  console.log(fruit);
}
```

### DOM 操作

DOM（文档对象模型）允许 JavaScript 与 HTML 交互。你可以更改内容、样式和属性。

```javascript
// 修改元素的内容
let element = document.getElementById("demo");
element.innerHTML = "New Content";

// 修改样式
element.style.color = "red";

// 添加事件监听器
let button = document.querySelector("button");
button.addEventListener("click", function() {
  alert("Button clicked!");
});
```

### 异步 JavaScript

JavaScript 使用异步编程来处理耗时的任务，例如从 API 获取数据。

#### Promises（承诺）

```javascript
fetch("https://api.example.com/data")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
```

#### Async/Await

```javascript
async function fetchData() {
  try {
    let response = await fetch("https://api.example.com/data");
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}
```





### 1. 变量

变量是存储数据值的容器。在 JavaScript 中，你可以使用 `let`、`const` 和 `var` 来声明变量。

- `let`: 用于声明可以重新赋值的变量。
- `const`: 用于声明不可重新赋值的变量。
- `var`: 声明变量的旧方式（在现代 JS 中已避免使用）。

示例：
```javascript
let x = 10;
x = 20; // Allowed

const y = 5;
// y = 10; // 将抛错误
```

### 2. 数据类型

数据类型定义了变量可以包含的数据类型。JavaScript 有几种类型：

- String（字符串）：用引号括的文本数据。
- Number（数字）：整数和浮点数。
- Boolean（布尔值）：true 或 false。
- Undefined（未定义）：已声明但未赋值的变量。
- Null（空）：表示任何值的缺失。
- Object（对象): 属性的集合。
- Array（数组): 列表类数据。

示例：
```javascript
let name = "Alice";
let age = 25;
let isStudent = true;
let score;
let result = null;
let user = { name: "Bob", age: 30 };
let colors = ["red", "green", "blue"];
```

### 3. 运算符

运算符用于对变量和值执行操作。

### 算术运算符
| 运算符 | 描述 | 示例 | 结果 |
| :--- | :--- | :--- | :--- |
| `+` | 加法 | `5 + 2` | 7 |
| `-` | 减法 | `5 - 2` | 3 |
| `*` | 乘法 | `5 * 2` | 10 |
| `/` | 除法 | `5 / 2` | 2.5 |
| `%` | 取模（余数） | `5 % 2` | 1 |
| `**` | 幂 | `5 ** 2` | 25 |
| `++` | 增一 | `x++` | 6 |
| `--` | 减一 | `x--` | 4 |

### 比较运算符
- `==`: 等于（仅检查值）。
- `===`: 严格相等（检查值和类型）。
- `!=`: 不等于。
- `!==`: 严格不等于。
- `>`: 大于。
- `<`: 小于。
- `>=`: 大于等于。
- `<=`: 小于等于。

### 赋值运算符
- `=`: 赋值。
- `+=`: 加并赋值。
- `-=`: 减并赋值。
- `*=`: 乘并赋值。
- `/=`: 除并赋值。

### 逻辑运算符
- `&&`: 与（当两个操作数都为真时为真）。
- `||`: 或（当其中一个操作数为为真时为真）。
- `!`: 非（反转结果）。

### 4. 控制流

控制结构决定代码的执行路径。

### 条件语句 (if...else)
```javascript
let age = 18;
if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}
```

### 循环 (for, while)
循环用于重复执行一段代码块。

```javascript
// For 循环
for (let i = 0; i < 5; i++) {
  console.log(i);
}

// While 循环
let j = 0;
while (j < 5) {
  console.log(j);
  j++;
}
```

### 5. 函数

函数是可重用的代码块，旨在执行特定任务。

```javascript
// 函数声明
function greet(name) {
  return "Hello, " + name;
}

console.log(greet("World"));

// 箭头函数
const add = (a, b) => a + b;
console.log(add(5, 3));
```

### 6. 数组

数组用于在单个变量中存储多个值。

```javascript
let fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // Apple
fruits.push("orange"); // 添加到末尾
console.log(fruits.length); // 4
```

### 7. 对象

对象用于存储相关数据和方法的集合。

```javascript
let car = {
  brand: "Toyota",
  model: "Corolla",
  year: 2022,
  start: function() {
    console.log("Engine is starting...");
  }
};

console.log(car.brand);
car.start();
```

### 8. DOM 操作

文档对象模型（DOM）允许 JavaScript 修改 HTML 和 CSS。

```javascript
// 选择元素
let title = document.getElementById("title");

// 修改内容
title.innerText = "New Title";

// 修改样式
title.style.color = "blue";

// 添加事件监听
let btn = document.querySelector("button");
btn.addEventListener("click", () => {
  alert("Button clicked!");
});
```

### 9. 理解数据类型（详细）

JavaScript 是动态类型语言，这意味着变量可以动态地更改类型。

- `string`: 文本序列。
- `number`: 整数和浮点数。
- `boolean`: `true` 或 `false`。
- `undefined`: 声明但未赋值的变量。
- `null`: 显式的空值。
- `object`: 复杂数据结构。
- `array`: 用于列表的特殊对象类型。
- `function`: 函数也是对象。
- `symbol`: 唯一标识符。
- `bigint`: 用于大整数。

### 特殊值
- `NaN`: 不是数字（无效数学运算的结果）。
- `Infinity`: 比任何数字都大的值。
- `-Infinity`: 比任何数字都小的值。
- `undefined`: 自动赋值给未初始变量。
- `null`: 有意的缺失。

### 基本类型 vs 非基本类型
- **基本类型 (Primitives)**: 不可变的并按值存储（String, Number, Boolean, undefined, null, symbol, bigint）。
- **非基本类型 (Objects)**: 可变的并按引用存储（Object, Array, Function）。





### 无穷与 NaN

在 JavaScript 中，`Infinity` 是一个表示比任何数字都大的数值。当数学运算产生的数值过大时，就会创建它。

```javascript
let a = 1 / 0; // Infinity
console.log(a); // Infinity

let b = 1 / -0; // -Infinity
console.log(b); // -Infinity

let c = Infinity * 2; // Infinity
console.log(c); // Infinity

let d = Infinity - Infinity; // NaN
console.log(d); // NaN

let e = Infinity / Infinity; // NaN
console.log(e); // NaN
```

`NaN` 代表 Not-a-Number（不是数字），是一个特殊的数值，表示未定义或无法表示的数学运算的结果。

```javascript
let f = 0 / 0; // NaN
console.log(f); // NaN

let g = "hello" / 2; // NaN
console.log(g); // NaN

let h = undefined + 5; // NaN
console.log(h); // NaN

let i = Math.sqrt(-1); // NaN
console.log(i); // NaN
```

### 2021 特性

2021 年，JavaScript 引入了几个新特性，使代码更加简洁和富有表现力。

### 逻辑赋值运算符

逻辑赋值运算符（`&&=`、`||=` `、`??=`）允许你根据变量的当前值和逻辑条件给变量赋值。

```javascript
let a = 1;
a &&= 2; // a 保持 1，因为 a 为真
console.log(a); // 1

let b = 0;
b ||= 2; // b 变为 2，因为 b 为假
console.log(b); // 2

let c = null;
c ??= 3; // c 变为 3，因为 c 是 null 或 undefined
console.log(c); // 3

let d = 0;
d ??= 3; // d 保持 0，因为 d 不是 null 或 undefined
console.log(d); // 0
```

### String.prototype.replaceAll()

`replaceAll()` 方法返回一个新字符串，其中所有模式或正则表达式的出现都被替换为指定的字符串。

```javascript
let text = "apple banana apple orange";
let result = text.replaceAll("apple", "orange");
console.log(result); // "orange banana orange orange"

let text2 = "the quick brown fox";
let result2 = text2.replaceAll(/x/g, "cat");
console.log(result2); // "the cat brown fox"
```

### Array.prototype.at()

`at()` 方法返回指定索引处的元素。它支持负整数从数组末尾倒数。

```javascript
let arr = [10, 20, 30];
console.log(arr.at(0)); // 10
console.log(arr.at(-1)); // 30 (最后一个元素)
console.log(arr.at(-2)); // 20 (倒第二个元素)
```

### Promise.any()

`Promise.any()` 返回一个 promise，只要可迭代对象中的任何一个 promise 变为完成，它就会完成。

```javascript
let p1 = Promise.reject("Error 1");
let p2 = Promise.resolve("2");
let p3 = Promise.reject("Error 3");

Promise.any([p1, p2, p3]).then((value) => {
  console.log(value); // "2"
}).catch((error) => {
  console.log(error);
});
```

### WeakMap 和 WeakSet

`WeakMap` 和 `WeakSet` 是对对象持有弱引用的集合。这允许垃圾回收器在对象不再其他不再被引用时回收内存。

### WeakMap

```javascript
let wm = new WeakMap();
let obj = { key: "value" };
wm.set(obj, "some data");
console.log(wm.get(obj)); // "some data"

obj = null; // 对象可以被垃圾回收
```

### WeakSet

```javascript
let ws = new WeakSet();
let obj2 = { id: 1 };
ws.add(obj2);
console.log(ws.has(obj2)); // true

obj2 = null; // 对象可以被垃圾回收
```

### globalThis 属性

`globalThis` 属性提供了全局对象，无论环境如何（浏览器、Node.js 等）。

```javascript
console.log(globalThis); // 浏览器中为 window，Node.js 中为 global
globalThis.myVar = "hello";
console.log(globalThis.myVar); // "hello"
```

### 类字段 (Class Fields)

现在可以使用 `#` 前缀定义私有字段和方法。

```javascript
class User {
  #name; // 私有字段

  constructor(name) {
    this.#name = name;
  }

  getName() {
    return this.#name;
  }
}

let user = new User("Alice");
console.log(user.getName()); // "Alice"
// console.log(user.#name); // 错误
```

### 私有静态字段

静态字段和方法也可以 `#` 进行私有化。

```javascript
class Counter {
  static #count = 0;

  static increment() {
    this.#count++;
  }

  static getCount() {
    return this.#count;
  }
}

Counter.increment();
console.log(Counter.getCount()); // 1
// console.log(Counter.#count); // 错误
```

### 数字分隔符

可以使用下划线作为数字分隔符来增加数字的可读性。

```javascript
let population = 8_000_000_000;
console.log(population); // 8000000000

let price = 1_250.5;
console.log(price); // 1250.5
```

### BigInt

`BigInt` 是用于表示大于 `Number` 类型最大整数的数据类型。通过附加 `n` 创建。

```javascript
let big1 = 9007199254740991n;
let big2 = BigInt("9007199254740991");
console.log(big1 + 1n); // 9007199254740992n

### 可选链和空值合并

可选链（`?.`）允许在不检查每个引用是否有效的情况下读取属性值。空值合并（`??`）当左侧操作数为 `null` 或 `undefined` 时返回右侧操作数。

```javascript
let user = {
  address: {
    city: "Berlin"
  }
};

console.log(user?.address?.city); // "Berlin"
console.log(user?.profile?.age); // undefined

let count = 0;
console.log(count ?? 10); // 0
console.log(null ?? 10); // 10

### Array.prototype.flat()

`flat()` 方法创建一个拼接指定深度子数组元素的新数组。

```javascript
let arr = [1, 2, [3, [4]], 5];
console.log(arr.flat()); // [1, 2, 3, [4], 5]
console.log(arr.flat(2)); // [1, 2, 3, 4, 5]
```

### Array.prototype.flatMap()

`flatMap()` 方法等于调用 `map()` 然后再调用 `flat()`，深度为 1。

```javascript
let arr = [1, 2, [3, 4]];
let result = arr.flatMap(x => [x, x * 2]);
console.log(result); // [1, 2, 2, 4, 3, 8]
```

### String.prototype.repeat()

`repeat()` 方法返回一个重复指定次数的字符串。

```javascript
let str = "abc";
console.log(str.repeat(3)); // "abcabcabc"
```

### String.prototype.padStart() and padEnd()

`padStart()` 和 `padEnd()` 在开头或结尾填充另一个字符串直到字符串达到给定长度。

```javascript
let str = "5";
console.log(str.padStart(3, "0")); // "005"
console.log(str.padEnd(5, "!")); // "5!!!!"
```

### Object.entries()

`Object.entries()` 静态方法返回对象的可枚举字符串键的[键, 值]对数组。

```javascript
let obj = { a: 1, b: 2 };
console.log(Object.entries(obj)); // [["a", 1], ["b", 2]]
```

### Object.keys()

`Object.keys()` 返回对象的可枚举字符串属性名的数组。

```javascript
let obj = { a: 1, b: 2 };
console.log(Object.keys(obj)); // ["a", "b"]
```

### Object.values()

`Object.values()` 静态方法返回对象的可枚举字符串属性值的数组。

```javascript
let obj = { a: 1, b: 2 };
console.log(Object.values(obj)); // [1, 2]
```

### Object.fromEntries()

`Object.fromEntries()` 从键值对的列表创建对象。

```javascript
let entries = [["a", 1], ["b", 2]];
console.log(Object.fromEntries(entries)); // { a: 1, b: 2 }
```

### Array.prototype.includes()

`includes()` 方法确定数组是否包含其元素中的某个值，返回 true。

```javascript
let arr = [1, 2, 3];
console.log(arr.includes(2)); // true
console.log(arr.includes(4)); // false
```

### Array.prototype.find()

`find()` 方法返回提供的数组中满足测试函数的第一个元素。

```javascript
let numbers = [2, 12, 8, 130];
let found = numbers.find(element => element > 10);
console.log(found); // 12
```

### Array.prototype.findIndex()

`findIndex()` 方法返回数组中满足测试函数的元素的索引。

```javascript
let users = [
  { name: 'John', age: 30 },
  { name: 'Jane', age: 25 }
];
let index = users.findIndex(user => user.age < 30);
console.log(index); // 1
```

### Array.prototype.some()

`some()` 方法测试数组中至少有一个元素通过了测试函数。

```javascript
let numbers = [1, 2, 3, 4];
let hasEven = numbers.some(element => element % 2 === 0);
console.log(hasEven); // true

let oddNumbers = [1, 3, 5];
let hasEvenOdd = oddNumbers.some(element => element % 2 === 0);
console.log(hasEvenOdd); // false
```

### Array.prototype.every()

`every()` 方法测试数组中的所有元素是否通过了测试函数。

```javascript
let numbers = [2, 4, 6];
let allEven = numbers.every(element => element % 2 === 0);
console.log(allEven); // true

let mixedNumbers = [2, 4, 5];
let allEvenMixed = mixedNumbers.every(element => element % 2 === 0);
console.log(allEvenMixed); // false
```





## JavaScript 变量

在 JavaScript 中，有三种声明变量的方法：`var`、`let` 和 `const`。在 ES6 (2015) 之前，`var` 关键字是声明变量的唯一方式。

```javascript
var foo;
console.log(foo); // undefined
```

当你在声明变量时不为其赋值时，它的值值为 `undefined`。

```javascript
var bar;
*undefined*
bar;
*undefined*
whatever;
*Uncaught ReferenceError: whatever is not defined*
```

如果你尝试使用一个未声明的变量，JavaScript 将抛出 `ReferenceError`。

```javascript
var bar;
* bar; // undefined
```

如果你声明了一个变量并给它赋值，该值就会被存储起来。

```javascript
var foo = 5;
*undefined*
```

如果你声明了一个变量然后对其进行重新赋值，旧值将会丢失。

```javascript
var foo = 5;
*undefined*
foo = 10; // 10
```

### Let 和 Const

在 ES6 中，引入了 `let` 和 `const` 来为 `var` 提供更好的替代方案。`let` 和 `const` 是块级作用域，而 `var` 是函数作用域。

```javascript
if (true) {
  let x = 10;
  console.log(x); // 10
}
console.log(x); // ReferenceError: x is not defined
```

`let` 允许你重新赋值，但 `const` 不行。

```javascript
let foo = "hello";
foo = "world"; // ok

const bar = "hello";
bar = "world"; // TypeError: Assignment to constant variable
```

`const` 必须在声明时初始化。

```javascript
const pi = 3.14;
const fruits = ["apple", "banana"];
fruits.push("orange"); // ok, 数组本身没有被重新赋值
```

## 数组

JavaScript 中的数组用于在单个变量中存储多个值。数组可以包含不同类型的数据。

```javascript
var fruits = ["apple", "banana", "orange"];
console.log(fruits.length); // 3
console.log(fruits[0]); // apple
```

你可以使用 `push()` 方法向数组添加元素。

```javascript
var fruits = ["apple", "banana"];
fruits.push("cherry");
console.log(fruits.length); // 3
```

你也可以通过索引访问元素，索引从 0 开始。如果你尝试访问一个不存在的索引，它将返回 `undefined`。

```javascript
var fruits = ["apple", "banana"];
console.log(fruits[1]); // banana
console.log(fruits[5]); // undefined
```

### 函数

函数是用于执行特定任务的代码块。它们在被调用时执行。

```javascript
function greet() {
  console.log("Hello, world!");
}
greet(); // Hello, world!
```

函数可以接收参数并返回结果。

```javascript
function add(a, b) {
  return a + b;
}
console.log(add(5, 3)); // 8
```

### 箭头函数

箭头函数为编写函数提供了更短的语法。

```javascript
const multiply = (a, b) => {
  return a * b;
};
console.log(multiply(4, 3)); // 12
```

对于单表达式函数，你可以省略大括号和 `return` 关键字。

```javascript
const square = (n) => n * n;
console.log(square(5)); // 25
```

### 对象

对象用于以键值对的形式存储数据集合。

```javascript
var user = {
  name: "Alice",
  age: 30,
  city: "New York"
};
console.log(user.name); // Alice
```

你可以使用点符号或方括号符号来访问对象的属性。

```javascript
console.log(user.name); // Alice
console.log(user["age"]); // 30
```

对象还可以拥有方法，即作为属性存储存储的函数。

```javascript
var person = {
  name: "Bob",
  greet: function() {
    console.log("Hello, my name is " + this.name);
  }
};
person.greet(); // Hello, my name is Bob
```

## 类

类是创建对象的蓝图。它们有助于封装数据和行为。

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(this.name + " makes a sound.");
  }
}
const myAnimal = new Animal("Rex");
myAnimal.speak(); // Rex makes a sound.
```

继承允许一个类继承另一个类的属性和方法。

```javascript
class Dog extends Animal {
  constructor(name, breed) {
    super(name);
    this.breed = breed;
  }
  bark() {
    console.log(this.name + " barks!");
  }
}
const myDog = new Dog("Buddy", "Golden Shepherd");
myDog.bark(); // Buddy barks!
```

### 异步 JavaScript

异步编程允许 JavaScript 执行耗时任务而不阻塞主执行线程。

```javascript
console.log("Start");
setTimeout(() => {
  console.log("Timeout after 2 seconds");
}, 2000);
console.log("End");
// 输出：
// Start
// End
// Timeout after 2 seconds
```

Promises 是代表异步操作最终完成（或失败）的对象。

```javascript
const promise = new Promise((resolve, reject) => {
  const success = true;
  setTimeout(() => {
    if (success) {
      resolve("Success!");
    } else {
      reject("Error!");
    }
  }, 1000);
});

promise
  .then(result => console.log(result))
  .catch(error => console.error(error));
```

`async/await` 语法为处理 promise 提供了一种更简洁的方式。

```javascript
async function fetchData() {
  try {
    const result = await promise;
    console.log(result);
  } catch (error) {
    console.error(error);
  }
}
fetchData();
```

### DOM 操作

DOM（文档对象模型）允许 JavaScript 与 HTML 内容交互并修改。

```javascript
const title = document.getElementById("mainTitle");
title.textContent = "New Title";

const button = document.querySelector(".myButton");
button.addEventListener("click", () => {
  alert("Button clicked!");
});
```





## 数组

数组是JavaScript中用于存储多个值的数据结构。数组可以存储任何类型的值，包括字符串、数字、布尔值，甚至是另一个数组或对象。数组是有序的，这意味着每个元素都有特定的索引（index）。

- 数组的索引从0开始计数的。
- 数组可以动态地改变长度。
- 数组提供了许多内置方法来操作其中的元素。

### 如何创建数组

你可以使用字面量符号 `[]` 来创建一个数组。

```javascript
var myFirstArray = [ "item1", 2, 3, true, "last item" ];
```
`*undefined*`
`myFirstArray`
`["item1", 2, 3, true, "last item"]*`

### 访问元素

你可以通过索引来访问数组中的元素。索引从0开始。

```javascript
myFirstArray[ 0 ];
*"first"*

myFirstArray[ 1 ];
*"second"*

myFirstArray[ 2 ];
*"third"*
```

### 修改元素

你可以通过索引来修改数组中的特定值。

```javascript
var mySecondArray = [ "first", "second", "third" ];
```
`*undefined*`
`mySecondArray;`
`["first", "second", "third"]*`

```javascript
mySecondArray[ 0 ] = "apple";
mySecondArray[ 1 ] = "banana";
mySecondArray[ 2 ] = "cherry";
mySecondArray[ 3 ] = "date";
```

### 数组长度

数组有一个 `length` 属性，表示数组中元素的数量。

```javascript
var mySecondArray = [ "first", "second", "third" ];
```
`mySecondArray.length;`
*3*`

### 添加元素

你可以使用 `push()` 方法向数组末尾添加新元素。

```javascript
mySecondArray.push("date");
```
`mySecondArray;`
`["first", "second", "third", "date"]*`

### 删除元素

你可以使用 `pop()` 方法从数组末尾删除最后一个元素。

```javascript
mySecondArray.pop();
```
`mySecondArray;`
`["first", "second", "third"]*`

### Shift 方法

你可以使用 `shift()` 方法从数组开头删除第一个元素。

```javascript
mySecondArray.shift();
```
`mySecondArray;`
`["second", "third"]*`

### Unshift 方法

你可以使用 `unshift()` 方法向数组开头插入新元素。

```javascript
mySecondArray.unshift("apple");
```
`mySecondArray;`
`["apple", "second", "third"]*`

### Splice 方法

`splice()` 方法用于在数组的任何位置添加、删除或替换元素。

```javascript
var mySecondArray = [ "first", "second", "third" ];
mySecondArray.splice(1, 1, "new item");
```
`mySecondArray;`
`["first", "new item", "third"]*`

### Slice 方法

`slice()` 方法返回一个数组的一个部分的新数组，不会修改原数组。

```javascript
var mySecondArray = [ "first", "second", "third" ];
var result = mySecondArray.slice(1, 3);
```
`result;`
`["second", "third"]*`

### Join 方法

`join()` 方法将数组的所有元素连接成一个字符串。

```javascript
var myFirstArray = [ "item1", 2, 3 ];
var str = myFirstArray.join("-");
```
`str;`
*"item1-2-3"*

### IndexOf 方法

`indexOf()` 方法返回指定元素在数组中第一次找到的索引。

```javascript
var myFirstArray = [ "item1", 2, 3 ];
var index = myFirstArray.indexOf(2);
```
`index;`
*1*`

### Find 方法

`find()` 方法返回数组中第一个通过提供测试函数的元素。

```javascript
var myFirstArray = [ "item1", 2, 3 ];
var item = myFirstArray.find(function(element) { return element > 1; });
```
`item;`
*2*`

### Filter 方法

`filter()` 方法创建一个包含所有通过提供测试函数的元素的新数组。

```javascript
var myFirstArray = [ 1, 2, 3 ];
var filtered = myFirstArray.filter(function(element) { return element > 1; });
```
`filtered;`
*[2, 3]*`

### Map 方法

`map()` 方法创建一个新数组，其结果是对原数组每个元素执行回调函数的结果。

```javascript
var myFirstArray = [ 1, 2, 3 ];
var doubled = myFirstArray.map(function(element) { return element * 2; });
```
`doubled;`
*[2, 4, 6]*`

### ForEach 方法

`forEach()` 方法对数组的每个元素执行一次提供的函数。

```javascript
var myFirstArray = [ "item1", 2, 3 ];
myFirstArray.forEach(function(element) { console.log(element); });
```

### 对象

对象是JavaScript中存储键值对（key-value pairs）的数据结构。每个属性由一个键（也称为属性名）和一个值组成。

### 创建对象

你可以使用字面量符号 `{}` 来创建一个对象。

```javascript
var myDog = {
  name: "Zero",
  color: "orange",
  ageInYears: 3,
  wellBehaved: false
};
```

### 访问属性

你可以通过点符号或方括号来访问对象的属性。

```javascript
myDog.name;
*"Zero"*

myDog["color"];
*"orange"*
```

### 修改属性

你可以通过赋值来修改对象的属性值。

```javascript
myDog.name = "Buddy";
myDog.ageInYears = 5;
```

### 添加属性

你可以随时向对象添加新属性。

```javascript
myDog.breed = "Golden Retriever";
myDog.isHappy = true;
```

```javascript
myDog.breed;
*"Golden Retriever"*```

### 删除属性

你可以使用 `delete` 关键字来删除对象的属性。

```javascript
delete myDog.wellBehaved;
```

### 遍历对象

你可以使用 `for...in` 循环来遍历对象的属性键。

```javascript
for (var key in myDog) {
  console.log(key + ": " + myDog[key]);
}
```

### 嵌套对象

对象可以包含另一个对象作为属性。

```javascript
var myDog = {
  name: {
    first: "Zero",
    middle: "Baskerville",
    last: "Marquis"
  },
  color: "orange",
  ageInYears: 3,
  wellBehaved: false
};
```

```javascript
myDog.name.first;
*"Zero"*

myDog.name.last;
*"Marquis"*
```





var myDog = new Object();
*undefined*
myDog.nickname = "Falsy";
*"Falsy"*

如果属性不存在：
```javascript
var myDog = {
  "nickname": "Falsy"
};
*undefined*
```

如果给对象添加一个属性：
```javascript
var myDog = {
  "name": "Zero"
};
*undefined*
```

**属性**

```javascript
myDog.name;
*Zero*
```

当访问访问对象的某个属性时，它会返回该属性的值。如果该属性不存在，它将返回 undefined。该对象拥有属性 "name"如下：

```javascript
var myDog = {
  "name": "Zero"
};
*undefined*
myDog["name"];
*Zero*
```

如果你更改了对象属性的值，该对象将会被更新：

```javascript
var myDog = {
  "name": "Zero"
};
*undefined*
myDog.name = "New";
```

如果你从对象中删除一个属性，该属性将被移除：

```javascript
var cars = {
  "car1": "red",
  "car2": "blue",
  "car3": "green"
};
*undefined*
delete cars.car2;
```

如果你访问一个不存在的属性，它会返回 undefined：

```javascript
var cars = {
  "car1": "red",
  "car2": "blue",
  "car3": "green"
};
*undefined*
var carKey = "car" + 2;
*undefined*
carKey;
*"car2"*
cars.carKey;
*undefined*
```

如果你使用变量访问属性，它会返回该属性的值：

```javascript
var cars = {
  "car1": "red",
  "car2": "blue",
  "car3": "green"
};
*undefined*
var carKey = "car" + 2;
*undefined*
cars[carKey];
*"blue"*
```

如果你使用变量更改对象属性的值，该对象将会被更新：

```javascript
var cars = {
  "car1": "red",
  "car2": "blue",
  "car3": "green"
};
*undefined*
var carKey = "car" + 2;
*undefined*
cars[carKey] = "yellow";
```

**函数**

当你定义一个函数时，可以调用它来执行代码：

```javascript
var whatup = function() {
  console.log("Hello again, world.");
};
*undefined*
whatup();
*Hello again, world.*
```

如果你在带参数的情况下调用函数，函数将使用这些参数作为参数：

```javascript
var greet = function(username) {
  console.log("Hello again, " + username + ".");
};
*undefined*
greet("Alice");
*Hello again, Alice.*
```

如果你在不传递参数的情况下调用函数，该参数将是 undefined：

```javascript
var greet = function(username) {
  console.log("Hello again, " + username + ".");
};
*undefined*
greet();
*Hello again, undefined.*
```





### 条件语句

在 JavaScript 中，`if` 语句用于根据条件执行特定的代码。如果条件为真，大括号中的代码将运行。

```javascript
function addNumbers(num1, num2) {
  return num1 + num2;
}
addNumbers(2, 3); // 5
typeof addNumbers(2, 2); // "number"
```

```javascript
function addNumbers(num1, num2) {
  return num1 + num2;
}
var sum = addNumbers(2, 3); // 5
typeof sum // "number"
```

`else` 语句允许你仅在条件为假时执行代码。

```javascript
function combineStrings(firstString, secondString) {
  return firstString + secondString;
  console.log("Hello? Can anyone hear me?");
}
combineStrings("Test", "strings"); // "Test strings"
```

`else if` 语句允许你按顺序检查多个条件。

```javascript
var score = 85;
if (score >= 90) {
  console.log("A");
} else if (score >= 80) {
  console.log("B");
} else if (score >= 70) {
  console.log("C");
} else {
  console.log("F");
}
```

`length` 属性用于确定字符串中的字符数或数组中的元素个数。

```javascript
var name = "John";
if (name.length > 5) {
  console.log("Long name");
} else {
  console.log("Short name");
}
```

```javascript
var maths = 5;
if (maths == 5) {
  console.log("This number is five.");
}
```

```javascript
var foo = false;
if (foo) {
  /* 此处的任何代码永远不会执行，除非你将 foo 改为 true */
} else {
  // 这段代码会运行是因为 foo 是 false
}
```

```javascript
var maths = 2;
if (maths > 5) {
  console.log("Greater than five.");
} else {
  console.log("Less than or equal to five.");
}
```

```javascript
var lunch = "burrito";
if (lunch == "gravel") {
  console.log("That isn't food.");
} else if (lunch == "burrito") {
  console.log("A burrito is an excellent choice.");
} else {
  console.log("It might not have been a burrito, but at least it wasn't gravel.");
}
```





在 JavaScript 中，比较运算符用于比较两个值并返回一个布尔值。

### 比较运算符

- `==` 检查两个值在执行类型转换后是否相等。
- `===` 检查两个值在不执行类型转换的情况下是否相等。
- `!=` 检查两个值在执行类型转换后是否不等相等。
- `!==` 检查两个值在不执行类型转换的情况下不等相等。
- `>` 检查左侧值是否大于右侧。
- `<` 检查左侧值是否小于右侧。
- `>=` 检查左侧值是否大于或等于右侧。
- `<=` 检查左侧值是否小于或等于右侧。

例如，`5 == "5"` 为 `true`，因为字符串转换为了数字。然而，`5 === "5"` 为 `false`，因为类型不同（数字和字符串）。

### 等等运算符：`==` 和 `===`

`==` 运算符在类型转换后检查相等性。`===` 运算符（严格相等）同时检查值和类型。

```javascript
console.log(5 == "5"); // true
console.log(5 === "5"); // false
console.log(null == undefined); // true
console.log(null === undefined); // false
```

### 不等运算符：`!=` 和 `!==`

`!=` 运算符在类型转换后检查不等性。`!==` 运算符（严格不等）在不进行类型转换的情况下检查不等性。

```javascript
console.log(5 != "5"); // false
console.log(5 !== "5"); // true
console.log(null != undefined); // false
console.log(null !== undefined); // true
```

### 关系运算符：>`, `<`, `>=`, `<=`

这些运算符用于比较数字或字符串（基于字典序顺序）。

```javascript
console.log(10 > 5); // true
console.log(5 < 10); // true
console.log(10 >= 5); // true
console.log(5 <= 10); // true
```

### 字符串比较

在比较字符串时，JavaScript 根据它们的 Unicode 值按字典序进行比较。

```javascript
console.log("apple" > "banana"); // false
console.log("Banana" > "apple"); // true (大写字母在小写字母之前)
```

### 特殊值：null, undefined, NaN

JavaScript 有一些在比较中行为独特的的特殊值。

| 值 | `==` | `===` | `!=` | `!==` |
| :--- | :--- | :--- | :--- | :--- |
| `null` | true | false | false | true |
| `undefined` | true | false | false | true |
| `NaN` | false | false | true | true |

注意 `NaN` 永远不等于任何值，包括它本身。

```javascript
function greetUser(name) {
  if (name) {
    console.log("Welcome, " + name + "!");
  } else {
    console.log("Welcome, whoever you are!");
  }
}

greetUser("Muscles Touchdown"); // Welcome, Muscles Touchdown!
greetUser(); // Welcome, whoever you are!
```

### 假值与真值 (Falsy and Truthy Values)

在 JavaScript 中，某些值在布尔上下文中求时为“假值 (falsy)”。唯一的假值为：

- `false`
- `0`
- `""`（空字符串）
- `null`
- `undefined`
- `NaN`

所有其他值都是“真值 (truthy)”，包括空数组 `[]` 和空对象 `{}`。

```javascript
function greetUser(name) {
  if (name === undefined) {
    name = "whomever you are";
  }
  console.log("Welcome, " + name + "!");
}

greetUser("Muscles Touchdown"); // Welcome, Muscles Touchdown!
greetUser(undefined); // Welcome, whoever you are!
```

### 默认参数

你可以为函数参数定义默认值，自动处理 `undefined` 参数。

```javascript
function greetUser(name = "whomever you are") {
  console.log("Welcome, " + name + "!");
}

greetUser("Muscles Touchdown"); // Welcome, Muscles Touchdown!
greetUser(); // Welcome, whoever you are!
```

### 逻辑运算符

逻辑 `&&`（与）和 `||`（或）运算符用于组合比较结果。

```javascript
var foo = 2;
if (foo != 5) {
  console.log("foo is not equal to five");
}

console.log(true == 1); // true
console.log(false == 0); // false
```

### 比较运算符（续）

运算符 `>=`（大于或等于）和 `<=`（小于或等于）对于范围检查非常有用。

```javascript
console.log(10 >= 5); // true
console.log(5 <= 5); // true
```

### 严格相等 vs 宽松相等

`==` 和 `===` 之间的区别是类型转换。通常优选 `===` 以避免由意外类型转换导致的意外 bug。

```javascript
console.log(0 == ""); // true
console.log(0 === ""); // false
```


```javascript
var bikeName = "Bonneville";

if( bikeName.length <= 10 ) {
  console.log("There are at least ten characters in this bike’s name.");
}
```

### 逻辑运算符

`if` `else`

`5 < 2 || 10 > 2`
*true*

`10 > 5 && "toast" === 2`
*false*

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "taco";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

var lunch = "tacos";
if (lunch === "tacos") {
  console.log("I am hungry");
} else {
  console.log("I am not hungry");
}

function mealChecker(lunch) {
  if (lunch !== "gravel" && (lunch === "burrito" || lunch === "tacos")) {
    console.log("Delicious.");
  }
}

mealChecker("tacos");

var foo = "A String";
foo.toLowerCase();
"THIS IS A STRING".toLowerCase(); // "this is a string"

function mealChecker(lunch) {
  let lowerLunch = lunch.toLowerCase();
  if (lowerLunch !== "gravel" && (lowerLunch === "burrito" || lowerLunch === "tacos")) {
    console.log("Delicious.");
  }
}

mealChecker("TACOS");

var theNumber = 5;
switch(theNumber) {
  case 1:
    console.log("This is the number one.");
    break;
  case 2:
    console.log("This is the number two.");
    break;
  case 3:
  case 4:
    console.log("This is either three or four.");
    break;
  case 5:
    console.log("This is the number five.");
    break;
}
```


```javascript
let theNumber = 0;
while (theNumber < 5) {
  if (number > 2) {
    console.log("the number is large");
  } else if (theNumber < 2) {
    console.log("the number is small");
  } else {
    console.log("the number is medium");
  }
  theNumber++;
}
```

```javascript
let theNumber = 1;
switch (theNumber) {
  case 1:
    console.log("this is one");
  case 2:
    console.log("this is two");
  case 3:
    console.log("this is three");
  case 4:
    console.log("this is four"); own  case 5:
    console.log("this is five");
  default:
    console.log("Wait, that isn't a number");
}
```

```javascript
let theNumber = 1;
switch (theNumber) {
  case 1:
    console.log("This is number.");
    break;
  case "1":
    console.log("This is string '1'");
    break;
}
```

```javascript
function daysPassedThisWeek(numericDay) {
  console.log("The following days have already happened this week:");
  switch (numericDay) {
    case 7:
      console.log("Saturday");
    case 6:
      console.log("Friday");
    case 5:
      console.log("Thursday");
    case 4:
      console.log("Wednesday");
    case 3:
      console.log("Tuesday");
    case 2:
      console.log("Monday");
    case 1:
      console.log("Sunday");
    default:
      console.log("Wait, that isn't a numbered day of the week.");
  }
}
```

daysPassedThisWeek(3); // 今天是周的第三天。本周已经过了以下的日子：周二、周一、周日。

```javascript
function movePlayer(keyCode) {
  switch (keyCode) {
    case 65: // A 键
      moveLeft();
      break;
    case 68: // D 键
      moveRight();
      break;
    case 37: // 左箭头
      moveLeft();
      break;
    case 39: // 右箭头
      moveRight();
      break;
  }
}
```

```javascript
let score = 0;
while (score < 10) {
  if (score > 5) {
    console.log("局势迅速加剧了");
    score += 2;
  } else {
    score += 1;
  }
  if (score >= 10) {
    console.log("旗帜吹响了");
    break;
  }
}
```

```javascript
for (let i = 0; i < 5; i++) {
  daysPassedThisWeek(5); // 今天是周的第五天。本周已经过了以下的日子：周四、周三、周二、周一、周日。
}
```


```javascript
for(var i = 0; i < 3; i++) {
  console.log("This loop will run three times.")
}
```
*(3) 此循环将运行三次.*

`for` 语句用于执行特定次数的代码块。`for` 语句接受三个可选表达式：初始化、条件和最终表达式。

初始化表达式在循环开始之前执行一次。条件在循环的每次迭代之前求值；如果条件值为 `false`，则循环终止。最终表达式在循环的每次迭代之后执行。

示例：
```javascript
for (var i = 0; i < 5; i++) {
  console.log(i);
}
```
在这个示例中，变量 `i` 被初始化为 0。只要 `i` 小于 5，循环就会继续。在每次迭代后，`i` 都会加 1。

`for` 语句也可以用于遍历数组：
```javascript
var fruits = ["apple", "banana", "cherry"];
for (var i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```
在这种情况下，数组的 `length` 属性被用于确定循环运行的次数。

JavaScript 中还有其他类型的 `for` 循环，例如 `for...in` 和 `for...of`。`for...in` 循环用于遍历对象的属性。`for...of` 循环用于遍历可迭代对象（如数组）的值。

```javascript
var person = {name: "John", age: 30, city: "New York"};
for (var key in person) {
  console.log(key + ": " + person[key]);
}

var colors = ["red", "green", "blue"];
for (var color of colors) {
  console.log(color);
}
```

### for...in 循环
`for...in` 循环用于遍历对象的可枚举属性。在循环中定义的变量代表每个属性的。

```javascript
var person = {name: "John", age: 30, city: "New York"};
for (var key in person) {
  console.log(key + ": " + person[key]);
}
```

### for...of 循环
`for...of` 循环用于遍历可迭代对象的值。在循环中定义的变量代表每个元素的值。

```javascript
var colors = ["red", "green", "blue"];
for (var color of colors) {
  console.log(color);
}
```

### break 和 continue
`break` 语句用于提前退出循环。`continue` 语句用于跳过循环的当前迭代并移动到下一次。

```javascript
for (var i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  console.log(i);
}

for (var i = 0; i < 10; i++) {
  if (i === 5) {
    continue;
  }
  console.log(i);
}
```

### 嵌套循环
嵌套循环是在另一个内部的循环。这通常在处理多维数组或矩阵时使用。

```javascript
for (var i = 0; i < 3; i++) {
  for (var j = 0; j < 3; j++) {
    console.log("i=" + i + ", j=" + j);
  }
}
```

### 数组方法
JavaScript 提供了几个用于遍历数组的内置方法，例如 `forEach`、`map`、`filter` 和 `reduce`。

*(1) 循环*
var loopArray = ["first", "second", "third"];
for (var i = 0; i < loopArray.length; i++) {
  console.log(loopArray[i]);
}

*(2) forEach 方法*
var loopArray = ["first", "second", "third"];
loopArray.forEach(function(item) {
  console.log(item);
});

*(3) map 方法*
var loopArray = ["first", "second", "third"];
var newArray = loopArray.map(function(item) {
  return item + "!";
});

*(4) filter 方法*
var loopArray = ["first", "second", "third"];
var filteredArray = loopArray.filter(function(item) {
  return item !== "second";
});

*(5) reduce 方法*
var loopArray = [1, 2, 3];
var sum = loopArray.reduce(function(accumulator, current) {
  return accumulator + current;
}, 0);

### 对象
var nameObject = {
  "first": "Mat",
  "last": "Marquis"
};

for (var key in nameObject) {
  console.log(nameObject[key]);
}

*(1) 循环*
var nameObject = {
  "first": "Mat",
  "last": "Marquis"
};
for (var key in nameObject) {
  console.log(nameObject[key]);
}

*(2) 循环*
var nameObject = {
  "first": "Mat",
  "last": "Marquis"
};
for (var key in nameObject) {
  console.log(nameObject[key]);
}

### 字符串
var fullName = {
  "first": "Mat",
  "last": "Marquis"
};
for (var name in fullName) {
  console.log(name + ": " + fullName[name]);
}



```javascript
myObject.toString();
*"[object Object]"*

myObject.toString = function() {
  console.log( "I just broke JavaScript a little." );
};

myObject.toString();
*I just broke JavaScript a little.*

otherObject.toString();
*"[object Object]"*

var myObject = {};
var unrelatedObject = {};

myObject.toString();
*"[object Object]"*

myObject.__proto__.toString = function() {
  console.log( "I just broke JavaScript a LOT." );
};

myObject.toString();
*I just broke JavaScript a LOT.*

unrelatedObject.toString(); // Uh oh.
*I just broke JavaScript a LOT.*
```

当我们调用 `unrelatedObject.toString()` 时，JavaScript 首先会在 `unrelatedObject` 对象本身查找 `toString` 方法。如果没有找到，就会去它的原型（`__proto__`）查找。由于我们修改了 `Object.prototype` 的 `toString` 方法，因此 `unrelatedObject` 继承了被修改后的方法。

但是，修改 `Object.prototype` 会影响到所有的对象，因为几乎所有对象的原型链最终都会指向 `Object.prototype`。这通常是非常危险的，因为它会污染全局环境。

如果我们只想修改某个对象的行为而不影响其他对象，我们可以直接操作该对象的原型链：

```javascript
var myObject = {};
var unrelatedObject = {};

myObject.toString();
*"[object Object]"*

myObject.__proto__.toString = function() {
  console.log( "I just broke JavaScript a LOT." );
};

myObject.toString();
*I just broke JavaScript a LOT.*

unrelatedObject.toString(); // Uh oh.
*I just broke JavaScript a LOT.*
```

在这种情况下，`unrelatedObject` 继承了 `myObject` 的原型链中的 `toString` 方法，因为我们修改的是 `myObject` 的原型，而不是全局的 `Object.prototype`。

### 添加自定义方法

如果我们想让所有对象都拥有一个 `containsName` 方法，可以在 `Object.prototype` 上定义它：

```javascript
Object.prototype.containsName = function() {
  var result = false;
  for( var key in this ) {
    if( key === "name" {
      result = true;
    }
  }
  return result;
};

var firstObject = {
  "foo": false
};

var secondObject = {
  "name": "Hawkeye",
  "location": "Maine"
};

firstObject.containsName(); // false
secondObject.containsName(); // true
```

但是，这种方法也有一个缺陷：如果一个对象本身有一个名为 `name` 的属性（即使其值为 `false`），`for...in` 循环也会检测到这个属性。为了解决这个问题，我们可以使用 `hasOwnProperty` 方法来检查属性是否是属于对象本身的：

```javascript
Object.prototype.containsName = function() {
  var result = false;
  for( var key in this ) {
    if(this.hasOwnProperty(key) && key === "name") {
      result = true;
    }
  }
  return result;
};
```

### 使用 hasOwnProperty

`hasOwnProperty` 方法用于检查对象是否直接拥有某个属性，而不是通过原型链继承该属性。

```javascript
var swamp = {
  "bunk1": "Hawkeye",
  "bunk2": "BJ",
  "bunk3": "Frank"
};

for( var bunk in swamp ) {
  if(swamp.hasOwnProperty(bunk)) {
    console.log(swamp[bunk]);
  }
}
// 输出: Hawkeye, BJ, Frank
```

然而，如果我们想遍历一个对象的所有属性（包括原型链上的属性），`for...in` 配合 `hasOwnProperty` 就不够了。我们可以手动遍历原型链：

```javascript
Object.prototype.customPrototypeMethod = function() {
  console.log( "Hello again." ); 
};

var swamp = {
  "bunk1": "Hawkeye",
  "bunk2": "BJ",
  "bunk3": "Frank"
};

// 遍历原型链的逻辑
```

### 遍历原型链

我们可以通过一个循环来手动遍历原型链：

```javascript
var newObject = {
  "name": "Frank"
};

var i = 0;
while(i < 3) {
  console.log( "Loop." );
  i++;
}
```





- `while` 循环只要指定的条件为真，就会一直执行代码块。
- 在下面的示例中，循环将一直持续，直到随机数等于 3。

```javascript
var random = Math.floor( Math.random() * 10 );
while( random !== 3 ){
  console.log( "Nope, not " + random );
  var random = Math.floor( Math.random() * 10 );
}
console.log( "Got it!" );
```
*Nope, not 5*
*Nope, not 9*
*Nope, not 2*
*Got it!*

在下面的示例中，我们使用 `while` 循环打印随机数，直到它匹配 5。

```javascript
var random = Math.floor( Math.random() * 10 );
while(random !== 5){
  console.log( "Is it... " + random );
  random = Math.floor( Math.random() * 10 );
}
console.log( "Got it!" );
```

*Is it... 1*
*Is it... 4*
*Is it... 7*
*Is it... 3*

`do...while` 循环与 `while` 循环相似，但有一个关键区别：它在检查条件之前至少会执行一次代码块。

```javascript
var i = 0;
do {
  console.log( "Loop." );
  i++;
} while (i < 3);
```
*(3) Loop.*

在下面的示例中，使用 `do...while` 循环打印随机数，直到它等于 3。

```javascript
var random;
do {
  console.log( "Is it... " + random );
  random = Math.floor( Math.random() * 10 );
} while (random !== 3);
console.log( "Got it!" );
```
*Is it... 2*
*Is it... 8*
*Is it... 0*
*Is it... 3*

`break` 语句可用于提前退出循环，无论条件是否仍然为真。

```javascript
/* #1 "This is a loop with a break" */
var i = 0;
while(true){
  console.log( "This is a loop with a break " + i );
  if(i === 5){
    break;
  }
  i++;
}
```
在下面的示例中，`break` 语句用于在 `i` 达到 5 时退出循环。

```javascript
var i = 0;
while(true){
  console.log( "This is a loop with a break " + i );
  if(i === 5){
    break;
  }
  i++;
}
```

`continue` 语句用于跳过当前循环迭代的剩余部分并跳转到下一次迭代。

```javascript
for( var i = 0; i < 5; i++ ) {
  console.log(i);
}
```
*0*
*1*
*2*
*3*
*4*

在下面的示例中，`continue` 语句用于在 `i` 等于 2 时跳过循环的剩余部分。

```javascript
for( var i = 0; i < 5; i++ ) {
  if(i === 2){
    continue;
  }
  console.log(i);
}
```
*0*
*1*
*3*
*4*

`continue` 语句用于在 `i` 等于 2 时跳过循环迭代的剩余部分。

```javascript
for( var i = 0; i < 5; i++ ) {
  if(i === 2){
    continue;
  }
  console.log(i);
}
```
*0*
*1*
*3*
*4*

`break` 语句用于在 `i` 等于 2 时退出循环。

```javascript
for( var i = 0; i < 5; i++ ) {
  if(i === 2){
    break;
  }
  console.log(i);
}
```
*0*
*1*

`continue` 语句用于在 `i` 等于 2 时跳过循环迭代的剩余部分。

```javascript
for( var i = 0; i < 5; i++ ) {
  if(i === 2){
    continue;
  }
  console.log(i);
}
```
*0*
*1*
*3*
*4*

`break` 语句用于在 `i` 等于 2 时退出循环。

```javascript
for( var i = 0; i < 5; i++ ) {
  if(i === 2){
    break;
  }
  console.log(i);
}
```
*0*
*1*

`break` 语句用于在 `concatString` 长度达到 5 时退出循环。

```javascript
var concatString = "a";
while(true) {
  concatString = concatString + "a";
  if(concatString.length === 5){
    break;
  }
  console.log(concatString);
}
```
*aa*
*aaa*
*aaaa*

无限循环是指条件始终为真而永远不会结束的循环。

```javascript
while(true) {
  console.log( "This is an infinite loop" );
}
```

无限循环可以使用 `break` 语句跳出。

```javascript
var i = 0;
while(true) {
  console.log( "This is an infinite loop " + i );
  if(i === 10){
    break;
  }
  i++;
}
```

### window: 全局上下文
`window` 对象是浏览器中的全局上下文。它包含了浏览器中可用的全局变量和函数。

```javascript
window
```
`window` 对象是浏览器中的全局上下文。它包含了浏览器中可用的全局变量和函数。

```javascript
window
```
`window` 对象是浏览器中的全局上下文。它包含了浏览器中可用的全局变量和函数。

```javascript
window
```
`window` 对象是浏览器中的全局上下文。它包含了浏览器中可用的全局变量和函数。





`window.localVar;`

`*undefined*`

`window.globalVar;`

`*我是全局变量。`

```javascript
// Get the global window object
var win = window;

// Get the document object
var doc = win.document;

// Get the body of the document
var body = doc.body;

// Get the head of the document
var head = doc.head;

// Get all paragraph elements in the document
var paragraphs = doc.getElementsByTagName("p");

// Get the first paragraph
var firstParagraph = paragraphs[0];

// Get the last paragraph using length minus 1
var lastParagraph = paragraphs[paragraphs.length - 1];

// Change the content of the first paragraph
firstParagraph.innerHTML = "Listen up, chumps:";

// Change the content of the last paragraph ownlastParagraph.innerHTML = "And that's how I spent my vacation.";

// Example of manipulating the DOM
var newDiv = document.createElement("div"); ownnewDiv.innerHTML = "This is a new div";
body.appendChild(newDiv);
```

```html
<!DOCTYPE html>
<html><head>
  <meta charset="utf-8">
  <link rel="stylesheet" type="text/css" href="css/style.css">
</head>
<body>
  <script src="js/script.js"></script>
</body>
</html>
```

## 面向设计师的 JavaScript

坦率地说，我应该在书的开头向大家道歉——不是向你，读者，尽管我不怀疑在我们读到结尾时，我至少还会欠你一个道歉。对于我在职业生涯早期对 JavaScript 说过的那些话，我向它表达了深表歉意，其中有些话犀利得简直能刻在玻璃上。

这是我一种并不含蓄的方式，想表达 JavaScript 的学习是一件棘手的事情……





要创建一个“阅读更多”链接，请使用以下代码：

```javascript
var newLink = document.createElement( "a" );
**newLink.setAttribute( "href", "#");**
**newLink.innerHTML = "Read more";**
```

首先，使用 `document.getElementsByTagName("p")` 页面上所有的段落。然后，选择第一个段并将“阅读更多”链接附加到它：

```javascript
var newLink = document.createElement( "a" );
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[ 0 ];
newLink.setAttribute( "href", "#");
newLink.innerHTML = "Read more";
firstParagraph.appendChild(newLink);
```

如果你想将显示的文本限制在特定的字符数量，可以使用以下方法：

```javascript
var newLink = document.createElement( "a" );
**var allParagraphs = document.getElementsByTagName("p");**
**var firstParagraph = allParagraphs[ 0 ];**
newLink.setAttribute( "href", "#");
newLink.innerHTML = "Read more";

var text = firstParagraph.innerHTML;
if (text.length > 100) {
  firstParagraph.innerHTML = text.substring(0, 100) + "... ";
  firstParagraph.appendChild(newLink);
}
```

如果你想在点击链接时显示全文，可以使用以下代码：

```javascript
var newLink = document.createElement( "a" );
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[ 0 ];
newLink.setAttribute( "href", "#");
newLink.innerHTML = "Read more";
firstParagraph.appendChild(newLink);

newLink.onclick = function() {
  firstParagraph.innerHTML = "The full text goes here...";
  this.remove();
};
```

如果你想对“阅读更多”链接进行样式设置，可以在代码中添加 CSS：

```javascript
var newLink = document.createElement( "a" );
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[ 0 ];
newLink.setAttribute( "href", "#");
newLink.innerHTML = "Read more";
**newLink.style.display = "inline-block";**
**newLink.style.marginLeft = "10px";**
firstParagraph.appendChild(newLink);
```

```css
.more-link {
  display: inline-block;
  margin-left: 10px;
  color: blue;
  text-decoration: underline;
}

.more-link:hover {
  color: darkblue;
}
```

或者，你可以使用 CSS 类而不是直接对元素设置样式：

```javascript
var newLink = document.createElement( "a" );
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[ 0 ];
newLink.setAttribute( "href", "#");
**newLink.setAttribute( "class", "more-link");**
newLink.innerHTML = "Read more";
firstParagraph.appendChild(newLink);
```

```css
.more-link {
  display: inline-block;
  margin-left: 10px;
}
```

如果你想限制显示的段落数量，可以使用以下代码：

```javascript
var newLink = document.createElement( "a" );
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[ 0 ];
newLink.setAttribute( "href", "#");
newLink.innerHTML = "Read more";
firstParagraph.appendChild(newLink);

for (var i = 1; i < allParagraphs.length; i++) {
  allParagraphs[i].style.display = "none";
}
```

如果你想在点击链接时显示所有段落，可以使用以下代码：

```javascript
var newLink = document.createElement( "a" );
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[ 0 ];
newLink.setAttribute( "href", "#");
newLink.innerHTML = "Read more";
firstParagraph.appendChild(newLink);

newLink.onclick = function() {
  for (var i = 1; i < allParagraphs.length; i++) {
    allParagraphs[i].style.display = "block";
  }
  this.remove();
};
```






## JavaScript 实现方案

```javascript
var newLink = document.createElement("a");
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[0];

newLink.setAttribute("href", "#");
newLink.setAttribute("class", "more-link");
newLink.innerHTML = "Read more";

for(var i = 0; i < allParagraphs.length; i++) {
    allParagraphs[i].style.display = "none";
}

firstParagraph.appendChild(newLink);
```

### 展开逻辑实现

为了实现点击“Read更多”时展开隐藏段落的功能，可以使用以下代码：

```javascript
var newLink = document.createElement("a");
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[0];

newLink.setAttribute("href", "#");
newLink.setAttribute("class", "more-link");
newLink.innerHTML = "Read more";

for(var i = 0; i < allParagraphs.length; i++) {
    if(i === 0) {
        continue;
    }
    allParagraphs[i].style.display = "none";
}
firstParagraph.appendChild(newLink);
```

### DOM 事件处理

通过监听 DOM 事件，可以捕获点击操作并切换显示状态：

```javascript
var newLink = document.createElement("a");
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[0];

function revealCopy() {
    console.log("Clicked!");
}

newLink.setAttribute("href", "#");
newLink.setAttribute("class", "more-link");
newLink.innerHTML = "Read more";
newLink.addEventListener("click", revealCopy);

for(var i = 0; i < allParagraphs.length; i++) {
    if(i === 0) {
        continue;
    }
    allParagraphs[i].style.display = "none";
}
firstParagraph.appendChild(newLink);
```

### 进阶：处理MouseEvent

在复杂的交互中，可能需要处理 `MouseEvent` 对象及其数据传输：

```javascript
var newLink = document.createElement("a");
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[0];

function revealCopy(e) {
    e.preventDefault();
};

newLink.setAttribute("href", "#");
newLink.setAttribute("class", "more-link");
newLink.innerHTML = "Read more";
newLink.addEventListener("click", revealCopy);

for(var i = 0; i < allParagraphs.length; i++) {
    if(i === 0) {
        continue;
    }
    allParagraphs[i].style.display = "none";
}
firstParagraph.appendChild(newLink);
```





The original text is corrupted, so the body cannot be displayed.



```javascript
var newLink = document.createElement("a");
var allParagraphs = document.getElementsByTagName("p");
var firstParagraph = allParagraphs[0];

function toggleCopy(e) {
  var allParagraphs = document.getElementsByTagName("p");
  for (var i = 0; i < allParagraphs.length; i++) {
    if (i === 0) {
      continue;
    }
    if (allParagraphs[i].style.display === "none") {
      allParagraphs[i].style.display = "block";
    } else {
      allParagraphs[i].style.display = "none";
    }
  }
  if (this === newLink) {
    this.remove();
  }
  if (e !== undefined && e.preventDefault !== undefined) {
    e.preventDefault();
  }
}

newLink.setAttribute("href", "#");
newLink.setAttribute("class", "more-link");
newLink.innerHTML = "Read more";
newLink.addEventListener("click", toggleCopy);
toggleCopy();
firstParagraph.appendChild(newLink);
```

(function() {
  var newLink = document.createElement("a");
  var allParagraphs = document.getElementsByTagName("p");
  var firstParagraph = allParagraphs[0];

  function toggleCopy(e) {
    var allParagraphs = document.getElementsByTagName("p");
    for (var i = 0; i < allParagraphs.length; i++) {
      var para = allParagraphs[i];
      if (i === 0) {
        continue;
      }
      if (para.style.display === "none") {
        para.style.display = "block";
      } else {
        para.style.display = "none";
      }
    }
    if (this === newLink) {
      this.remove();
    }
    if (e !== undefined && e.preventDefault !== undefined) {
      e.preventDefault();
    }
  }
  newLink.setAttribute("href", "#");
  newLink.setAttribute("class", "more-link");
  newLink.innerHTML = "Read more";
  newLink.addEventListener("click", toggleCopy);
  toggleCopy();
  firstParagraph.appendChild(newLink);
})();

渐进式增强



## 4A7 

可持续能源的发展一直是全球各国政府的关注重点。近年来，可再生能源显著增加，特别是太阳能和风能。然而，向完全可持续的能源系统转型面临着许多挑战。主要的障碍之一是可再生能源的间歇性；太阳并非总是照耀，风也并非一直吹。这意味着需要储能解决方案来储存能量，以便在没有时使用。

另一个挑战是可再生能源技术的高成本。虽然太阳能和风能的成本已大幅下降，但建设可再生能源基础设施所需的初始投资仍然非常高。这使得一些发展中国家难以向可持续能源转型。此外，还需要公众对可持续能源的支持。许多人对可再生能源仍持怀疑，赢得他们的认同至关重要。这可以通过教育和意识提升活动来实现，也可以通过展示可持续能源的益处。

向可持续能源的转型并非易事。必须确保可再生能源能够被整合到电网中。这需要对新技术和基础设施进行大量投资。此外，获得公众对可持续能源的支持也同样重要。通过解决这些挑战，我们可以为子孙后代确保一个更加可持续的未来。

## 结论

可持续能源的发展一直是全球各国政府的关注重点。近年来，可再生能源显著增加，特别是太阳能和风能。然而，向完全可持续的能源系统转型面临着许多挑战。主要的障碍之一是可再生能源的间歇性；太阳并非总是照耀，风也并非一直吹。这意味着需要储能解决方案来储存能量，以便在没有时使用。

另一个挑战是可再生能源技术的高成本。虽然太阳能和风能的成本已大幅下降，但建设可再生能源基础设施所需的初始投资仍然非常高。这使得一些发展中国家难以向可持续能源转型。此外，还需要公众对可持续能源的支持。许多人对可再生能源仍持怀疑，赢得他们的认同至关重要。这可以通过教育和意识提升活动来实现，也可以通过展示可持续能源的益处。

向可持续能源的转型并非易事。必须确保可再生能源能够被整合到电网中。这需要对新技术和基础设施进行大量投资。此外，获得公众对可持续能源的支持也同样重要。通过解决这些挑战，我们可以为子孙后代确保一个更加可持续的未来。

## 资源

国际能源署（IEA）提供了关于全球能源趋势的数据和分析。他们的报告对于任何想要了解当前能源状况的人来说都是非常有价值的资源。政府间气候变化委员会（IPCC）也提供了关于气候变化及其影响的关键信息。他们的发现对于理解向可持续能源转型的迫性至关重要。

国际可再生能源机构（IRENA）为向可再生能源转型提供信息和支持。他们的资源对于想要了解该领域最新进展的人很有帮助。世界能源论坛（WEF）还对全球能源问题提供了全面分析。他们的报告对于理解能源格局中的挑战和机遇非常有用。

****





本书的目的是为数字摄影世界提供一份全面的指南。它专为初学者以及那些希望精进其对技术方面和创作技巧理解的读者设计。本书涵盖了从基础相机设置到高级编辑软件的所有内容。

通过学习这些章节，读者将获得信心来捕捉惊人的图像，并表达他们独特的艺术愿景。我们希望这本书能成为你摄影旅程中一份宝贵的资源。

参考文献

参考文献

- Smith, J. (2018). *数字摄影的艺术*. 纽约：Photo Press。
- Jones, A. (2019). *初学者摄影技术*.伦敦：Creative Media。
- Brown, R. (2021). *精通你的相机*.东京：Vision Publishing。
- Davis, L. (2017). *数字后期处理秘密*.巴黎：Design Hub。
- Wilson, M. (2020). *构图的科学*.柏林：Art Hall。
- Miller, S. (2016). *光影与色彩*.旧金山：Light House。
- Taylor, K. (2022). *现代人像摄影*.多伦：Lens & Focus。
- White, P. (2019). *风景摄影大师*.悉尼：Nature Prints。

索引

光圈：12, 45, 68
平衡：22, 34
构图：15, 28, 40, 55, 72
数字：10, 25, 39, 50, 64
编辑：18, 31, 47, 59, 75
曝光：14, 29, 42, 58, 71
对：11, 27, 43, 61, 74
ISO：13, 30, 44, 60, 77
镜头：17, 32, 48, 56, 73
布光：16, 33, 46, 57, 79
人像：21, 35, 49, 62, 76
快门速度：19, 36, 51, 65, 80
白平衡：20, 37, 52, 66, 78

## 第1章：相机简介

- 相机历史
- 相机类型（单反 vs 无反）
- 了解你的相机机身

## 第2章：曝光三角

- 光圈
- 快门速度
- ISO 敏感度
- 三者如何平衡

## 第3章：对焦技巧

- 自动对焦 vs 手动对焦
- 单点对焦 vs 连续对焦
- 深度解析

## 第4章：构图规则

- 三分法
- 引导线
- 对称与图案
- 主框架

## 第5章：光光

- 自然光
- 人造光
- 使用反光板和闪光灯
- 理解黄金时刻

## 第6章：人像摄影

- 模特造型
- 选择合适的焦距
- 捕捉情感
- 背景选择

## 第7章：后期处理与编辑

- 编辑软件介绍
- RAW vs JPEG 文件
- 基础校正
- 色彩分级与修图

## 第8章：高级技巧

- 长曝光
- 微距摄影
- 夜景摄影
- 高动态范围

## 第9章：寻找你自己的风格

- 开发视觉语言
- 通过照片讲述故事
- 作品集

## 第10章：前方的路

- 在线分享你的作品
- 职业摄影生涯
- 持续你的教育

关于作者

作者担任职业旅游摄影师已有十五多年。由于他们访问过三十多个国家，其作品曾刊登于众多国际杂志。他们热衷于教他人如何通过镜头观察世界。


# JavaScript 初学者编程指南：从零开始完全掌握 JavaScript 编程语言

## JavaScript 简介

JavaScript 是一种强大的客户端脚本语言。JavaScript 主要用于提升用户与网站的互动性。换句话说，在 JavaScript 的帮助下，你可以让你的网站更生动、信息更丰富。JavaScript 也常用于图形渲染和移动设备开发。

JavaScript 也有更复杂的服务器端变体，例如 `Node.js`，它使你能够为网站添加更多功能，而不仅仅是上传文件（例如多台计算机之间的实时通信）。在客户端环境（例如 Web 浏览器）中，JavaScript 可以连接到环境对象，以提供对它们的编程控制。

它因网页创建而广为人知，一些非浏览器应用程序也使用它。JavaScript 可用于客户端和服务器端开发。JavaScript 包含一系列基本对象，如序列、日期和数学，以及一组核心语言结构，如运算符、控制结构和语句。

### 客户端

它为其文档对象模型（DOM）的使用提供对象。客户端扩展使应用程序能够在 HTML 表单上放置元素，并响应用户事件，如鼠标点击、模板数据和页面导航。使用完整的客户端框架，如 `AngularJS`、`ReactJS`、`VueJS` 等。

### 服务器端

它提供在服务器上运行 JavaScript 所的重要对象。服务器端扩展允许应用程序与数据库交互，以提供从一次调用到另一次调用的细节连续性，或在服务器上执行文件操作。目前最流行的实用框架是 `node.js`。

### JavaScript 的特性

根据最近的 `Stack Overflow` 调查，JavaScript 是全球最主要的平台。

随着 Web 开发的进步以及 JavaScript 通过 `Node.js` 等应用程序迁移到服务器端，JavaScript 能够做更多的事情。以下是我们可以用 JavaScript 做的一些事情：

- I. JavaScript 最初是为 DOM 操作而开发的。早期的网站大多是静态的，后来通过 `JS` 创建了动态网站。
- II. `JS` 函数是对象。我们可以像特定实体一样拥有属性和方法。它们可以作为参数传递给其他用途。
- III. 这将处理日期和时间。
- IV. 即使表单是使用 HTML 生成的，也能执行表单验证。
- V. 不需要编译器。

### JavaScript 的平台

**Web 开发**：为静态 JavaScript 页面引入交互性和操作，这是在 1995 年开发的。使用 `AngularJS` 时，这可以非常快速地完成。

**Web 应用程序**：通过发展，应用程序已经进步到需要一种语言来构建可靠的 Web 应用程序。如果我们正在查看 Google 地图中的地图，我们只需要点击和拖动鼠标。所有信息显示都只需一个按钮即可，而只有通过 JavaScript 才成为可能。使用应用程序编程接口（API）为计算机提供额外的功能。`Electron` 和 `React` 在这方面非常有帮助。

**服务器应用程序**：在 `Node.js` 的支持下，JavaScript 已经从客户端找到了通往服务器的道路，而 `node.js` 在应用端是最强大的。

**游戏**：JavaScript 不仅在网站上，还在休闲游戏的创建中发挥作用。JavaScript 和 `HTML 5` 的结合使得 JavaScript 在游戏创建中很常见。这提供了 `EaseJS` 库，为处理丰富的图形提供了选项。

**智能手表**：JavaScript 用于所有可行的系统和平台。这提供了 `PebbleJS` 库，用于智能手表应用程序。该系统运行允许互联网运行的程序。

**艺术**：艺术家和设计师可以使用 JavaScript 在 `HTML 5` 画布上绘制任何他们想要的东西，渲染更强大的声音，并使用 `p5.js` 软件。

**机器学习**：这个 JavaScript `ml5.js` 集合可用于通过机器学习进行软件开发。

### 如何运行 JavaScript？

作为脚本语言，JavaScript 不能独立运行。最终，应用程序负责运行 JavaScript 文件。当用户请求基于 JavaScript 的 HTML 页面时，脚本被发送到浏览器，由浏览器执行它。JavaScript 被所有现代 Web 浏览器支持，这是 JavaScript 最大的好处。因此，你不必考虑网站客户端使用的是 `Internet Explorer`、`Google Chrome`、`Firefox` 还是其他应用程序。JavaScript是被支持的。通常，JavaScript 在所有操作系统上都能工作，如 Windows、Linux 或 Mac。因此，JavaScript 克服了 `VBScript`（现已弃用）的主要缺点，后者仅限于 IE 和 Windows。

### 你需要的工具

为了开始，你需要一个文本编辑器来编写代码，以及一个浏览器来查看你的网页。你可以使用 `Notepad++`、`Visual Studio Code`、`Sublime Text`、`Atom` 等文本编辑器。你可以使用 `Google Chrome`、`Safari`、`Microsoft Edge`、`Internet Explorer` 等任何 Web 。

### JavaScript 与 Java

JavaScript 和 Java 在某些方面相似，但在其他方面完全不同。JavaScript 类似于 Java，但没有 Java 的静态类型和强类型控制。这就是为什么 JavaScript 从 `LiveScript` 重构为 `Javascript`，采用了大多数 Java 表达式语法、命名约定和基本控制流结构的原因。

JavaScript 遵循基于有限数据类型的运行时框架，这些数据类型表示整数、布尔值和字符串值，这与 Java 的编译时类结构不同。JavaScript 没有类模型，而是基于原型的对象模型。原型模型具有动态继承，可以为单个对象更改继承的内容。JavaScript 通常提供没有唯一声明规范的函数。函数可以是对象资源，作为松散类型的方法使用。

与 Java 相比，JavaScript 是一种非常开放的语言。所有变量、类和方法都不需要声明。你不必担心 `public`、`private` 或 `protected` 方法，也不需要实现接口。不需要显式声明变量、参数和返回函数类型。

Java 是一种为快速输出和类型安全而构建的类编程语言。类型安全意味着，例如，Java 整数不能通过修改 Java 字节码被抛入对象引用或私有内存。Java 的基于类的范式意味着编程仅由类及其方法组成。Java 类的继承和强类型通常包括紧密相关的对象层次结构。这些规范阻碍了 Java 的编程，使其不如 JavaScript 灵活。

相比之下，JavaScript 在精神上源自一系列更小、更动态的语言，如 `HyperTalk` 和 `dBASE`。它们简单的语法、高级的内置功能和构建结构的低要求，为更广泛的编程资源受众提供了便利。

## 条件语句

条件语句用于根据不同情况执行不同的操作。条件语句控制 JavaScript 的行为，并决定代码片段是否运行。在 JavaScript 中，有多种类型的条件，包括：

- 1) `If` 语句：如果条件有效，则用于执行一系列代码。
- 2) `Else` 语句：如果同一断言为假，则定义一个代码块的执行。
- 3) `Else if`：如果第一个条件不正确，则陈述一个新问题。

### IF 语句示例

`If` 语句仅在括号 `()` 中的条件为真时运行。因此，这是最常见的条件形式。

#### ELSE 语句示例

```javascript
if (10 > 5) {
    var outcome = "if block";
}

outcome;

OUTPUT
"if block"
```

对于上述情况，发生的过程如下：
关键字 `if` 表示 JavaScript 应开始一个条件语句。`(10 > 5)` 是一个为真的统计条件——在此情况下，10 大于 5。因此，将运行的代码块是 `{}` 包围的部分。由于条件通过，变量 `outcome` 被赋值为 `"if block"`。

#### ELSE 语句示例

带有 `else` 语句的 `if` 语句可以扩展，在条件通过时运行另一个块。

```javascript
if ("cat" === "dog") {
    var outcome = "if block";
} else {
    var outcome = "else block";
}
outcome

OUTPUT
"else block"
```

在上述情况下，`"cat"` 和 `"dog"` 不相同，因此运行另一个块，变量为 `"else block"`。

#### ELSE IF 语句示例

你还可以用 `else if` 声明来扩展。

```javascript
if (false) {
    var outcome = "if block";
} else if (true) {
    var outcome = "else if block";
} else {
    var outcome = "else block";
}
outcome

OUTPUT
"else if block"
```

你可以使用多个 `if else` 条件语句，但请注意，第一个通过的条件块将被执行。在运行第一个通过后，JavaScript 会跳过剩余条件。

## JavaScript 函数

JavaScript 函数旨在完成特定任务的代码块。当任何东西（调用它）时，JavaScript 函数就会执行。

### 定义函数

函数（也称为函数声明）包含：
- 关键字 `function`，后跟标题。
- 一个参数列表，用括号括起来并用逗号分隔。
- 定义函数的语句，包含在花括号 `{}` 中。

例如，此代码定义了一个 `square`，引用给定数字的平方：函数可以有多个参数，也可以没有参数。

```javascript
const makeNoise = function() {
  console.log("ling!");
};

makeNoise(); // → ling!

const power = function(base, exponent) {
  let result = 1;
  for (let count = 0; count < exponent; count++) {
    result *= base;
  }
  return result;
};

console.log(power(2, 10)); // → 1024
ling!
```

一些函数生成值，包括 `power` 和 `square`，而另一些产生值，例如 `makeNoise`，其唯一结果是 `undefined`。`return` 语句设置函数的值。函数参数充当绑定，但它们的初始值由调用者提供，而不是函数自身。

### 函数用作变量

函数应使用变量在各种公式、赋值和计算中的相同方式。

### arguments 对象

所有 JavaScript 函数都以参数开始。每个参数的值都包含在一个 `arguments` 变量中。`arguments` 对象是一个对象。使用数组索引来访问其值。

```html
<!DOCTYPE html>
<html>
<body>
<h1>演示：JavaScript arguments</h1>
<script>
function ShowMessage(firstName, lastName) {
  alert("Hello " + arguments[0] + " " + arguments[1]);
}

ShowMessage("Steve", "Jobs");
ShowMessage("Bill", "Gates");
ShowMessage(100, 200);
</script>
</body>
</html>
```

### 返回值

使用 `return` 关键字，函数可以返回零值或一个值。在上面提到的示例中，一个名为 `Sum` 的函数将 `val1` 和 `val2` 相加并返回。它允许代码获取返回值并将其赋给变量。第二个 `Multiply` 函数不返回值，因此不描述结果。

### 嵌套函数

JavaScript 中可以使用一个或多个内部函数。这些嵌套函数位于外部函数内部。内部函数控制外部函数的变量和参数。外部函数无法访问内部函数的变量。

### 要记住的要点

- 1) JavaScript 函数允许你指定一个代码块，为其命名，并根据需要运行多次。
- 2) 函数可以使用关键字 `function` 定义，并可以使用运算符执行。
- 3) 函数可以包含一个或多个参数。函数参数可以在执行期间可选地指定。
- 4) JavaScript 是一种动态类型语言。函数参数可以包含任何类型的数据。
- 5) 调用函数时，你可以指定更少或更多的参数。
- 6) 所有函数都可以默认访问 `arguments` 对象，而不是参数名称。
- 7) 函数可以返回特定值或另一个函数。
- 8) 函数可以赋给不同名称的变量。
- 9) JavaScript 允许你使用匿名函数创建变量。

## 作用域

变量的可访问性（可见性）由作用域决定。在代码的某些特定部分，作用域是执行期间变量、函数和对象的可访问性。也就是说，代码区域中变量和其他资源的可见性由作用域决定。在 JavaScript 中，有两种选择：

1) 全局作用域
2) 局部作用域

#### 全局作用域

当你在文档中开始编写 JavaScript 时，你已经处于全局框架中。整个 JavaScript 文本只有一个全局作用域。如果在函数外部指定变量，则该变量处于全局作用域。

#### 局部作用域

在 JavaScript 函数中声明的变量将对该函数是局部的。函数作用域的局部变量：只能从函数内部获取。在任何 `var` 参数函数内声明的变量称为局部变量。局部变量无法在声明函数外部访问或更改。在函数内指定的变量在作用域上是局部的。但是，对于该函数的每次调用，它们都是独立的。

## 数组

### 描述

数组是类列表对象，其原型具有执行遍历和变异操作的机制。数组的长度及其组件的类型都不是固定的。由于数组长度经常被修改，并且数据可以存储在数组的不连续位置，因此 JavaScript 数组是否密集并不重要。通常，这些是有用的特性；但如果你的特定用途不适合这些特性，你应该考虑使用类型化数组。

### 数组初始化

### JavaScript 数组

在 JavaScript 中，数组可以通过两种方式描述和初始化：字面量数组和构造函数数组语法。

以下示例说明了如何使用字面量语法数组来描述和初始化数组。

```markdown

```html
<body>
    <h1>JavaScript Array</h1>
    <p id="p1"></p>
    <p id="p2"></p>
    <p id="p3"></p>
    <p id="p4"></p>
    <p id="p5"></p>

    <script>
        var stringArray = ["one", "two", "three"];

        var numericArray = [1, 2, 3, 4];

        var decimalArray = [1.1, 1.2, 1.3];

        var booleanArray = [true, false, false, true];

        var mixedArray = [1, "two", "three", 4];

        document.getElementById("p1").innerHTML = stringArray;
        document..getElementById("p2").innerHTML = numericArray;
        document.getElementById("p3").innerHTML = decimalArray;
        document.getElementById("p4").innerHTML = booleanArray;
        document.getElementById("p5").innerHTML = mixedArray;
    </script>
</body>
```

# JavaScript 数组

one,two,three

1,2,3,4

1.1,1.2,1.3

true,false,false,true

1,two,three,4

JavaScript 数组可以存储不同数据类型的多个元素。数组中不必存储相同数据类型的值。

## 数组构造函数

你可以使用 `new` 关键字和 `Array` 构造函数语法来初始化数组。

以下示例说明了如何使用 `Array` 构造函数语法来描述数组。

## 常用操作

### 创建数组

```javascript
let fruits = ['Apple', 'Banana']

console.log(fruits.length)
// 2
```

### 使用数组索引访问元素

```javascript
let first = fruits[0]
// Apple

let last = fruits[fruits.length - 1]
// Banana
```

### 遍历数组

```javascript
fruits.forEach(function(item, index, array) {
  console.log(item, index)
})
// Apple 0
// Banana 1
```

### 在数组开头添加元素

```javascript
let newLength = fruits.unshift('Strawberry') // 添加到开头
// ["Strawberry", "Banana"]
```

### 通过索引位置移除元素

```javascript
let removedItem = fruits.splice(pos, 1) // 这是移除元素的方法

// ["Strawberry", "Mango"]
```

### 访问数组元素

JavaScript 数组是零索引的：数组的第一个元素索引为 0，因此最后一个元素的索引等于数组的 `length` 属性值减 1。使用不正确的索引号将返回 `undefined`。

```javascript
let arr = ['this is the first element', 'this is the second element', 'this is the last element']
console.log(arr[0])           // 输出 'this is the first element'
console.log(arr[1])           // 输出 'this is the second element'
console.log(arr[arr.length - 1]) // 输出 'this is the last element'
```

JavaScript 数组及其属性没有什么特别之处。以数字开头的 JavaScript 属性不能用点表示法引用，必须使用方括号表示法访问。

例如，如果你有一个名为 `3d` 的对象，它只能使用方括号表示法引用。

注意，在 `3d` 示例中必须提及 '3d'。也可以引用 JavaScript 列表的索引（例如 `years['2']` 而不是 `years[2]`），尽管这不是必需的。

## 数组属性

- `Constructor` - 返回生成数组对象原型的函数
- `Length` - 设置或返回列表中的项目数量
- `Prototype` - 允许你向数组集合添加属性和方法。

## 数组方法

1. `Concat()` 连接两个或多个数组，并返回连接后数组的副本。
2. `CopyWithin()` 在数组内将数组元素复制到指定位置。
3. `Entries()` 返回数组迭代对象的键/值对。
4. `Every()` 测试数组中的所有元素是否都通过了测试。
5. `Fill()` 用静态值填充数组中的项目。
6. `Filter()` 为数组中通过测试的每个元素创建一个新数组。
7. `Find()` 返回测试序列中第一个组件的值。
8. `FindIndex()` 返回数组中第一个通过测试的项目的索引。
9. `ForEach()` 为数组的每个元素调用一个函数。
10. `From()` 从一个对象创建数组。
11. `Includes()` 检查数组是否包含所需的元素。
12. `IndexOf()` 在数组中搜索一个元素并返回其位置。
13. `IsArray()` 检查一个对象是否是数组。
14. `Join()` 将所有数组元素连接成一个字符串。
15. `Keys()` 返回一个包含原始数组键的迭代对象数组。
16. `LastIndexOf()` 查找一个元素数组，从末尾开始并返回其位置。
17. `Map()` 生成一个新数组，结果是对每个数组元素调用函数。
18. `Pop()` 移除数组的最后一个元素，并将该元素返回到数组。
19. `Push()` 将新元素添加到数组的末尾，并返回列表的新长度。
20. `Reduce()` 将集合的值归约为单个值（从左到右）。
21. `ReduceRight()` 将数组的值归约为单个值（从右到左）。
22. `Reverse()` 反转列表中对象的顺序。
23. `Shift()` 移除数组的第一个元素并返回该元素。
24. `Some()` 检查数组中是否有任何元素通过了测试。
25. `Sort()` 对数组元素进行排序。
26. `Splice()` 通过数组添加/移除元素。
27. `ToString()` 将数组转换为字符串并返回结果。
28. `Unshift()` 将新元素添加到数组的开头，并返回新长度。
29. `ValueOf()` 返回列表的原始值。

## 循环

JavaScript 中使用循环来基于条件执行重复任务。条件在求值时通常返回 `true` 或 `false`。循环将持续运行，直到指定的条件返回 `false`。

### 不同类型的循环

JavaScript 包含多种循环类型：

1. `For`-循环 通过代码块执行多次。
2. `For/in`-循环 遍历对象的属性。
3. `For/of`-循环 遍历可迭代对象的值。
4. `While`-循环 当指定条件为真时，遍历代码块。
5. `Do/while`-循环 当指定条件为真时，也遍历代码块。

### While 循环

JavaScript 循环被反复用于运行代码块，直到满足某些条件。当开发者考虑迭代或遍历，比如一个数组时，这与循环相同。JavaScript 提供了多种选项来重复运行代码块，如 `while`、`do while`、`for` 和 `for-in`。

#### 示例

```javascript
var sum = 0;
var number = 1;
while (number <= 50) {  // -- 条件
  sum += number;        // -- 循环体
  number++;             // -- 更新器
}
alert("Sum = " + sum);  // => Sum = 1275
```

首先评估条件。如果有效，将执行 `while` 语句后面的语句块。这将重复，直到条件不正确。由于它在执行代码块之前测试条件，因此被称为前测试循环。

`number++` 语句将被称为更新器。移除它将导致无限循环。你必须始终在循环中提供一个语句，以确保循环终止，否则你将遇到这个问题。

### Do While 循环

```javascript
var sum = 0;
var number = 1;
do {
  sum += number;        // -- 循环体
  number++;             // -- 更新器
} while (number <= 50); // -- 条件
alert("Sum = " + sum);  // => Sum = 1275
```

首先执行 `do` 块，然后评估状态。如果 `while` 条件有效，将再次执行该块并重复，直到条件为假。由于条件在代码块执行后测试，因此被称为后测试循环。

```javascript
do {
    // 在循环体中从键盘读取一个字符
} while (if ch === '0');    // => 如果输入 '0' 则终止循环
```

### For 循环

```javascript
var sum = 0;
for (var i = 1; i <= 50; i++) {
    sum = sum + i;
}
alert("Sum = " + sum);    // => Sum = 1275
```

它由三个部分组成，用分号分隔。第一个是初始化器（`var i = 1`），它初始化循环，并且只在循环开始时执行一次。第二个是测试状态（`i <= 50`）。当条件表达式求值为 `true` 时，执行循环体。当条件为真时，循环停止。第三个元素是更新器（`i++`），它在每次迭代后调用调用。通常，更新器会增加或减少循环计数器。

在 `for` 循环中，所有三个阶段，即初始化器、测试状态和更新器。

```

```javascript
let evenNumbers = new Sequence(2, 10, 2);
let iterator = evenNumbers[Symbol.iterator]();

let result = iterator.next();

while( !result.done ) {
    console.log(result.value);
    result = iterator.next();
}
```

## 清理

除了 `next()` 方法，`[Symbol.iterator]()` 还可以选择性地返回 `return()` 方法。

当迭代提前停止时，`return()` 方法会被自动调用。这是你可以设置应用程序来清理资源的地方。

以下示例在 `Sequence` 对象中使用了 `return()` 方法：

```javascript
class Sequence {
    constructor( start = 0, end = Infinity, interval = 1 ) {
        this.start = start;
        this.end = end;
        this.interval = interval;
    }

    [Symbol.iterator]() {
        let counter = 0;
        let nextIndex = this.start;
        return {
            next: () => {
                if ( nextIndex <= this.end ) {
                    let result = { value: nextIndex, done: false }
                    nextIndex += this.interval;
                    counter++;
                    return result;
                }
                return { value: counter, done: true };
            },
            return: () => {
                console.log('cleaning up...');
                return { value: undefined, done: true };
            }
        }
    }
}
```

以下代码片段使用该模式对象生成从 1 到 10 的奇数序列。然而，迭代提前结束了。因此，`return()` 方法被自动调用。

## 输出

```
1
3
5
7
cleaning up...
```

## 对象

JavaScript 是为简单的基于对象的范式而设计的。对象是一组属性，属性是名称（或键）和值的组合。属性的值可以是一个函数，在这种情况下，该属性被称为方法。

JavaScript 中的对象，就像许多其他编程语言一样，可以比作现实生活中的对象。JavaScript 中对象的定义可以通过现实生活中的有形对象来理解。

通过 JavaScript，对象是一个具有属性和类的独立实体。例如，将其与一个杯子进行比较。杯子是一个具有属性的实体。杯子有颜色、图案、重量、制作材料等。同样，JavaScript 对象可以具有描述其特征的属性。

### 在 JavaScript 中创建对象

有三种创建对象的方法。

1.  通过对象字面量
2.  通过直接生成 `Object` 实例（使用 `new` 关键字）
3.  使用对象构造函数（使用 `new` 关键字）

#### 通过对象字面量创建 JavaScript 对象示例

```html
<html>
<body>
<script>
emp={id:102,name:"Shyam Kumar",salary:40000}
document.write(emp.id+" "+emp.name+" "+emp.salary);
</script>
</body>
</html>
```

102 Shyam Kumar 40000

#### 通过创建对象实例

这里使用 `new` 关键字来构建一个对象。

让我们看看直接创建对象的例子。

```html
<html>
<body>
<script>
var emp=new Object();
emp.id=101;
emp.name="Ravi Malik";
emp.salary=50000;
document.write(emp.id+" "+emp.name+" "+emp.salary);
</script>
</body>
</html>
```

101 Ravi Malik 50000

#### 使用对象构造函数

在这里，你需要构造一个参数函数。每个参数值都可以分配给当前对象，并使用 `this` 关键字。

`this` 关键字指向当前对象。

下面给出了通过对象构造函数创建对象的例子。

```html
<html>
<body>
<script>
function emp(id,name,salary){
this.id=id;
this.name=name;
this.salary=salary;
}
e=new emp(103,"Vimal Jaiswal",30000);
document.write(e.id+" "+e.name+" "+e.salary);
</script>
</body>
</html>
```

103 Vimal Jaiswal 30000

### 在 JavaScript 对象中定义方法

可以在 JavaScript 对象中指定方法。但在定义方法之前，我们需要向与方法同名的函数添加属性。

以下示例用于描述对象中的方法。

```html
<html>
<body>
<script>
function emp(id,name,salary){
this.id=id;
this.name=name;
this.salary=salary;

this.changeSalary=changeSalary;
function changeSalary(otherSalary){
this.salary=otherSalary;
}
}
e=new emp(103,"Sonoo Jaiswal",30000);
document.write(e.id+" "+e.name+" "+e.salary);
e.changeSalary(45000);
document.write("<br>"+e.id+" "+e.name+" "+e.salary);
</script>
</body>
</html>
```

103 Sonoo Jaiswal 30000

103 Sonoo Jaiswal 45000

### 访问对象键

使用 `for .. in` 循环获取对象所有属性和方法的列表。

![](img/c8bda18d83895f80a2442fa61b57b147_37_0.png)

### JavaScript 对象方法

- 1. `Object.assign()` 此方法用于将源对象的可枚举和自有属性转移到目标对象。
- 2. `Object.create()` 此方法用于使用原型对象和定义的属性构建一个新对象。
- 3. `Object.defineProperty()` 此方法用于标识某些属性的行为属性。
- 4. `Object.defineProperties()` 此方法用于构建或配置对象的多个属性。
- 5. `Object.entries()` 此方法返回一个键值对列表。
- 6. `Object.freeze()` 此方法防止现有资产被移除。
- 7. `Object.getOwnPropertyDescriptor()` 此方法返回指定对象的指定属性的描述符属性。
- 8. `Object.getOwnPropertyDescriptors()` 此方法返回给定对象的所有自有描述符。
- 9. `Object.getOwnPropertyNames()` 此方法返回一个包含所有找到的属性（可识别或不可识别）的数组。
- 10. `Object.getOwnPropertySymbols()` 此方法返回一个包含所有符号键属性的数组。
- 11. `Object.getPrototypeOf()` 此方法返回给定对象的原型。
- 12. `Object.is()` 此方法确定两个值是否相同。
- 13. `Object.isExtensible()` 此方法决定一个对象是否可扩展。
- 14. `Object.isFrozen()` 此方法决定一个实体是否已被冻结。
- 15. `Object.isSealed()` 此方法确定一个对象是否被密封。
- 16. `Object.keys()` 此方法返回对象的属性名列表。
- 17. `Object.preventExtensions()` 此方法用于防止实体的任何扩展。
- 18. `Object.seal()` 此方法防止添加新属性，并将所有现有属性标记为不可配置。
- 19. `Object.setPrototypeOf()` 此方法将指定对象的原型设置为另一个不同的对象。
- 20. `Object.values()` 方法返回一个值的集合。

### 需要记住的要点

- 1. JavaScript 对象是一个单一实体，它持有多个属性和方法的值。
- 2. 对象属性存储字面值，而过程是函数。
- 3. 对象可以使用字面量对象或构造函数类的语法生成。
- 4. 对象属性和方法可以通过点表示法或 `a[ ]` 括号访问。
- 5. 对象属性和方法可以通过点表示法或 `a[ ]` 括号访问。
- 6. 属性可以引用另一个对象。

# 11. Polyfill 本质上是赋予浏览器预期支持的技术的代码或插件。它们通常由 JavaScript 外部文件组成，您可以轻松地在自己的项目中使用它们。然而，它们与库有显著不同。一方面，库增强现有功能并使开发者更简单，另一方面，polyfills 提供对完全不存在的功能的支持。

## 转译

开发者使用新 JavaScript 特性的一种方法是将 ECMAScript 6 / ECMAScript 2015 代码迁移到旧浏览器兼容的版本。这被称为转译 `JavaScript`。

### 糟糕的浏览器嗅探代码

网页浏览器提供了一个用户代理列表，定义了网页浏览器是什么。当唯一的选择是 `Netscape` 或 `Internet Explorer` 时，开发者检索用户的浏览器并提供正确的代码。

对于开发者来说，浏览器兼容性不再是一个选择。这是生产过程的一个组成部分，需要与样式或编写类似的（如果不是更多）关注。这只是简单的 JavaScript。只需一点细节，每个人都可以启动一个在所有可用平台上运行得非常好的应用程序！

### 为什么您仍然要转译？

我们使用 React JSX（目前非常普遍，所以我假设很多开发者属于这一类）。其核心是 `XHTML` 到 `JS` 代码的转换，不涉及像 `Babel` 这样的完整转译器。此外，如果 `VirtualDom` 是您所需要的，请使用它。

尝试语言的最新特性。使用 `ES6`，如果您不属于 `TC39` 或没有强烈的冲动将不稳定的语言特性插入生产代码，您可能会做得很好。如今，大多数浏览器都有不错的语言，转译的需求消失了。您使用 `TypeScript` 权衡利弊。`TypeScript` 编译器通常在针对现代版本的 `ES6` 时扩展类型知识，而不是转换语法。您希望通过摇树（在 `webpacks` 和 `rollups` 中，这就是方法）来减少代码。您希望通过减小代码大小来混淆或减少代码。您希望有条件地删除部分代码。需要静态代码分析。您可以使用智能打包器进行大小敏感的生产服务，例如移动设备，但在创建此类替代部署时，我们将看到更详细的成本评估。这些静态代码分析对于生产代码作为“高级优化技术”仍然有用。您的文件不需要被压缩。目前（尽管存在一个有害分支），UglifyJS` 不能压缩 `ES6`，但 `Babili` 可以处理。压缩算法做得相当好（如果文件太小则不然），并且除非您为每个页面加载提供操作系统，否则应该没问题。如今，图像和多媒体内容比代码占用更多的带宽。

### 不要转译，而是真正编译

`WASM` 是城市中的孩子，官方构建目标承诺速度和更小的代码大小。`Chrome` 和 `Firefox` 目前支持 `WASM`，但大型浏览器供应商同意 `WASM` 将是未来最常见的运行时。如果您有 `Chrome`，可以尝试一下。

如果您是那种追求新事物的开发者，可以看看 `Rust`。它是 `WASM` 编译的，但不仅限于网络。人们实际上用它来编写浏览器或操作系统。除了过去的日子，`C` / C++` 开发者支持它并喜欢它。

## 模块

随着应用程序的增长，我们希望将其拆分为多个文件。更大。针对特定用途，一个模块可能包含一个类或一个功能库。

长期以来，`JavaScript`没有语言级别的模块语法。这并非问题，因为脚本最初都很小且简单，所以没有必要。然而，脚本变得越来越复杂，以至于开发者们发现了多种将代码组织成模块的方法，并从特殊库中按需加载模块。

仅举几例（出于历史原因）：

- `AMD` - 最早的模块系统之一，其库最初实现了`require.js`。
- `CommonJS` – `Node.js`的应用程序模块规范。
- `UMD` – 另一种模块框架，旨在成为通用的，兼容`AMD`和`CommonJS`。

所有这些现在都逐渐成为历史的一部分，但在旧文本中我们仍然可以找到它们。语言级别的模块系统在2015年的标准中逐步演进，现在已得到`Node.js`和所有主流浏览器的支持。从现在开始，我们将学习现代的`JavaScript`模块。

### 什么是模块？

一个文件就是一个模块。一个单独的模块就是一个脚本。就这么简单。模块可以相互加载，并通过特殊的指令导出和导入，从一个模块调用另一个模块的函数，以实现功能互换：

- 导出（Export）使用关键字标签导出变量和函数，使其可从当前模块外部访问。
- 导入（Import）则允许导入其他模块的功能。

让我们运行一个浏览器内的示例。由于模块支持关键字和特殊功能，用户需要被告知，一个脚本需要通过 `<script type="module">` 属性被当作模块来处理。

![](img/c8bda18d83895f80a2442fa61b57b147_48_0.png)

### 示例：匿名闭包

```javascript
(function () {
    // 我们将这些变量保持为闭包作用域内的私有变量

    var myGrades = [93, 95, 88, 0, 55, 91];

    var average = function() {
        var total = myGrades.reduce(function(accumulator, item) {
            return accumulator + item}, 0);

        return 'Your average grade is ' + total / myGrades.length + '.';
    }

    var failing = function(){
        var failingGrades = myGrades.filter(function(item) {
            return item < 70;});

        return 'You failed ' + failingGrades.length + ' times.';
    }

    console.log(failing());

}());

// 'You failed 2 times.'
```

我们的匿名函数拥有一个自执行环境或“闭包”，具有这种结构，然后我们立即执行它。这允许我们隐藏父级（全局）命名空间变量。这种方法的优点在于，你可以在不意外覆盖现有全局变量的情况下，仍然在此函数中访问全局变量：

```javascript
var global = 'Hello, I am a global variable :)';

(function () {
  // 我们将这些变量保持为闭包作用域内的私有变量

  var myGrades = [93, 95, 88, 0, 55, 91];

  var average = function() {
    var total = myGrades.reduce(function(accumulator, item) {
      return accumulator + item}, 0);

    return 'Your average grade is ' + total / myGrades.length + '.';
  }

  var failing = function(){
    var failingGrades = myGrades.filter(function(item) {
      return item < 70;});

    return 'You failed ' + failingGrades.length + ' times.';
  }

  console.log(failing());
  console.log(global);
}());

// 'You failed 2 times.'
// 'Hello, I am a global variable :)'
```

请注意，匿名函数需要括号，因为以 `function` 开头的声明通常被称为函数语句。

### 示例：对象接口

```javascript
var myGradesCalculate = (function () {

    // 将此变量保持为闭包作用域内的私有变量
    var myGrades = [93, 95, 88, 0, 55, 91];

    // 通过接口暴露这些函数
    return {
        average: function() {
            var total = myGrades.reduce(function(accumulator, item) {
                return accumulator + item;
            }, 0);

            return 'Your average grade is ' + total / myGrades.length + '.';
        },

        failing: function() {
            var failingGrades = myGrades.filter(function(item) {
                return item < 70;
            });

            return 'You failed ' + failingGrades.length + ' times.';
        }
    }
})();

myGradesCalculate.failing(); // 'You failed 2 times.'
myGradesCalculate.average(); // 'Your average grade is 70.'
```

### 示例：模块模式

```javascript
var myGradesCalculate = (function () {

    // 将此变量保持为闭包作用域内的私有
    var myGrades = [93, 95, 88, 0, 55, 91];

    var average = function() {
        var total = myGrades.reduce(function(accumulator, item) {
            return accumulator + item;
        }, 0);

        return 'Your average grade is ' + total / myGrades.length + '.';
    };

    var failing = function() {
        var failingGrades = myGrades.filter(function(item) {
            return item < 70;
        });

        return 'You failed ' + failingGrades.length + ' times.';
    };

    // 明确揭示我们希望公开的
    return {
        average: average,
        failing: failing
    };
})();
```

### COMMONJS

`CommonJS` 是一个社区工作组，致力于开发和实现 `JavaScript` 模块。`CommonJS` 模块本质上是一个重用的 JavaScript 元素，它导出特定对象使其在程序中可用。如果你在 `Node.js` 中编程，你会熟悉这种格式。当你定义 `CommonJS` 模块时，它可能看起来像：

```javascript
function myModule() {
  this.hello = function() {
    return 'hello!';
  }

  this.goodbye = function() {
    return 'goodbye!';
  }
}

module.exports = myModule;
```

我们使用特殊的 `module` 对象，并将一个链接放在 `module.exports` 中以实现我们的目的。这允许 `CommonJS` 模块知道我们想要暴露给文件的内容。如果有人想使用它，你可以在文件中 `require('myModule')`：

```javascript
var myModule = require('myModule');

var myModuleInstance = new myModule();
myModuleInstance.hello(); // 'hello!'
myModuleInstance.goodbye(); // 'goodbye!'
```

这种方法相对于我们之前讨论的开发模块有两个显著优势：
1. 避免命名空间中的全局污染
2. 明确地声明我们的依赖关系

我个人喜欢的语法也非常紧凑。另一个注意的是，`CommonJS` 采用服务器优先的方法，同步加载模块。这很重要，因为如果我们有三个其他模块，我们需要一个接一个加载。现在，它在服务器上运行得非常好，但不幸的是，这使得 `JavaScript` 在你的浏览器会变得更难用。可以说，从互联网加载模块比从磁盘读取要复杂得多。只要模块加载，浏览器就会被阻塞，直到加载完成。

### AMD

`CommonJS` 虽然很好，但如果我们想异步加载模块呢？答案就是异步模块定义，简称 `AMD`。使用 `AMD` 加载模块看起来像：

```javascript
define(['myModule', 'myOtherModule'], function(myModule, myOtherModule) {
    console.log(myModule.hello());
});
```

这里发生的是，定义的函数将每个模块的依赖项作为其第一个参数。这些依赖项在后台加载（非阻塞），并在加载完成后指定提供的回调函数。接下来，对于 `myModule` 和 `MyOtherModule`，回调函数以参数形式接收加载的依赖项，以便应用程序可以使用这些依赖项。依赖项也必须使用给定的关键字指定。

示例：`MyModule` 可能看起来像：

```javascript
define([], function() {
    return {
        hello: function() {
            console.log('hello');
        },
        goodbye: function() {
            console.log('goodbye');
        }
    };
});
```

同样，与 `CommonJS` 不同，`AMD` 使用第一种浏览器方法来完成任务，并具有异步行为。


`Promise` 是一个承诺未知值的符号。它使你能够将处理程序与异步操作的最终成功值或失败原因结合起来。这允许异步方法像同步方法一样返回值：异步方法返回一个承诺，承诺在未来提供值，而不是立即返回最终值。

### Promise 有三种状态

- `Fulfilled`: `Promise` 操作成功
- `Rejected`: `Promise` 失败被拒绝
- `Pending`: `Promise` 仍在等待中，尚未被履行或拒绝。如果 `Promise` 不是 `pending` 状态（它已被接受或拒绝），则 `Promise` 已履行。

通常人们是果断和坚决的：他们不必犹豫。一旦 `Promise` 被履行，就不能重新部署。同样，调用 `resolve()` 或 `reject()` 不产生任何效果。一个重要特性是已履行 `Promise` 的不可变性。

原生 JavaScript 的 `Promise` 不显示 `Promise` 状态。你应该将承诺视为一个黑盒。只有创建 `Promise` 的任务才能理解承诺状态或有权克服或拒绝。

### 可以使用 Promise 构造函数创建 Promise

- `Promise` 构造函数只接受一个请求，一个函数回调。
- 两个点，解析和拒绝函数回调。
- 在回调函数中执行操作，如果一切顺利则调用 `resolve`。
- 如果执行不顺利，则调用 `reject`。

```javascript
var promise = new Promise(function(resolve, reject) {
  const x = "geeksforgeeks";
  const y = "geeksforgeeks"
  if(x === y) {
    resolve();
  } else {
    reject();
  }
});

promise.
    then(function () {
        console.log('Success, You are a GEEK');
    }).
    catch(function () {
        console.log('Some error has occured');
    });
```
输出：Success you are a Geek

### 1. Then()

如果 `Promise` 被接受或拒绝，则调用 `then()`。

#### 参数

- 如果 `Promise` 被履行并获得测试，则执行第一个任务。
- 如果 `Promise` 被忽略并发生错误，则执行第二个任务。它是可选的，最好使用 `.catch()` 方法来查找错误。

#### 示例：Promise 已解决

```javascript
var promise = new Promise(function(resolve, reject) {
    resolve('Geeks For Geeks');
})

promise
    .then(function(successMessage) {
        //成功处理函数被调用
        console.log(successMessage);
    }, function(errorMessage) {
        console.log(errorMessage);
    })
```
输出：Geeks for Geeks

#### 示例：Promise 被拒绝

```javascript
var promise = new Promise(function(resolve, reject) {
    reject('Promise Rejected')
})

promise
    .then(function(successMessage) {
        console.log(successMessage);
    }, function(errorMessage) {
        //错误处理函数被调用
        console.log(errorMessage);
    })
```
输出：Promise Rejected

### 2. CATCH()

当 `Promise` 被拒绝或执行过程中发生错误时，调用 `catch()`。

#### 示例：Promise 被拒绝

```javascript
var promise = new Promise(function(resolve, reject) {
    reject('Promise Rejected')
})

promise
    .then(function(successMessage) {
        console.log(successMessage);
    })
    .catch(function(errorMessage) {
        //错误处理函数被调用
        console.log(errorMessage);
    });
```
输出：PROMISE REJECTED

#### 示例：Promise 被拒绝

```javascript
var promise = new Promise(function(resolve, reject) {
    throw new Error('Some error has occured')
})

promise
    .then(function(successMessage) {
        console.log(successMessage);
    })
    .catch(function(errorMessage) {
        //错误处理函数被调用
        console.log(errorMessage);
    });
```
输出：SOME ERROR HAS OCCURRED

### 3. FINALLY()

通常，无论 `Promise` 是履行还是拒绝，你都想执行相同的代码。

例如：

```javascript
function createApp() {
    // ...
}

learnJS
    .then(
        (success) => {
            console.log(success);
            createApp();
        }
    ).catch(
        (reason) => {
            console.log(reason);
            createApp();
        }
    );
```
如你所见，对于 `then()` 和 `catch()` 方法，`createApp()` 的调用是重复的。你使用 `finally()` 方法来删除这种重复，并在 `Promise` 被履行或拒绝时执行 `createApp()`：

```javascript
learnJS
    .then(success => console.log(success))
    .catch(reason => console.log(reason))
    .finally(() => createApp());
```

### 应用：

1. `Promise` 用于异步处理错误。
2. `Promise` 用于处理异步 HTTP 请求。

### 总结

1. 一个在未来返回值的对象是一个 `Promise`。
2. 一个 `Promise` 开始于待定状态，最终会变为已兑现或已拒绝状态。
3. 使用 `then()` 方法为兑现安排回调，使用 `catch()` 方法为拒绝安排回调。
4. 在 `finally()` 过程中，放置无论 `Promise` 是兑现还是拒绝都希望执行的代码。

### 结论

`Promise` 已经成为许多 JavaScript 惯用模式不可或缺的组成部分，包括 WHATWG Fetch 标准（用于同步大多数现代 Ajax 请求）和 Async Functions 标准。在撰写本文时，Async functions 处于第 3 阶段，但我预测它们很快将成为异步 JavaScript 编程的一种可行方法，意味着在未来几年，JavaScript 开发者将需要学会欣赏他们的 `Promise`。

例如，我建议当你使用 Redux 时，可以查看 redux-saga：一个用于管理 Redux 中副作用的库，其整个文档都依赖于 async 函数。

## ASYNC-AWAIT

我们都认识到 Javascript 是同步的，这意味着它有一个事件循环来排队一个操作，该操作在代码结束该操作后一段时间才会完成。但在我们的软件中，有许多功能使我们的代码异步。其中之一就是 Async / Await 接口。

Async / Await 扩展了我们在语言中提供的保证作为支持。有关更多信息，请参阅 Javascript promises。

除了 JavaScript `Promise`，`Async / await` 语句是语法糖。它们允许我们编写基于 `Promise` 的代码，但无需主线程，就像它是同步的一样。

### ASYNC:

它只是帮助我们编写同步代码的 `Promise`，并确保我们不会中断运行的线程。它通过事件循环异步操作。`Async` 函数永远返回一个值。你做出一个承诺，Javascript 会立即将其打包成一个合约，如果它没有返回值，则用其值解决。

`Async` 函数允许我们不阻塞执行线程，而是像编写同步代码一样编写 `Promise` 代码。它通过事件循环异步操作。`Async` 函数将始终返回一个值。

```javascript
async function fetchData() {
    const data = await somePromise;
    return data;
}

const result = fetchData();
console.log(result);
```

### AWAIT:

`await` 关键字只能在 `async` 函数内部使用。它会暂停函数的执行，直到 `Promise` 解决或拒绝。

```javascript
const result = await somePromise;
console.log(result);
```


```html
<!DOCTYPE html>
<html>
<body>

<h2>The XMLHttpRequest Object</h2>

<button type="button" onclick="loadDoc()">Request data</button>

<p id="demo"></p>

<script>
function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("demo").innerHTML = this.responseText;
    }
  };
  xhttp.open("POST", "demo_post2.asp", true);
  xhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
  xhttp.send("fname=Henry&lname=Ford");
}
</script>

</body>
</html>
```

## The XMLHttpRequest Object

Request data

Hello Henry Ford

在 `setRequestHeader(header, value)` 中为请求添加 HTTP 头。

- Header：输入头的名称
- Value：设置头的值

### 异步 - TRUE 还是 FALSE？

应异步提交服务器请求。

`open()` 方法的 `async` 参数应设置为 `true`：

```
xhttp.open("GET", "ajax_test.asp", true);
```

通过异步发送 JavaScript，服务器响应无需等待，而是可以：

- 运行其他脚本，同时等待服务器响应
- 在响应就绪后处理答案

### ONREADYSTATECHANGE 属性

你可以设置一个函数，当使用 `XMLHttpRequest` 对象的请求获得响应时执行。

该函数在 `XMLHttpRequest` 对象的 `onreadystatechange` 属性中指定：

```html
<!DOCTYPE html>
<html>
<body>

<div id="demo">
<h2>The XMLHttpRequest Object</h2>
<button type="button" onclick="loadDoc()">Change Content</button>
</div>

<script>
function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("demo").innerHTML =
      this.responseText;
    }
  };
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
}
</script>

</body>
</html>
```

## AJAX

AJAX 不是一种编程语言。

AJAX 是一种从网页访问 Web 服务器的技术。

AJAX 代表异步 JavaScript 和 XML。

### 同步请求

将 `open()` 方法的第三个参数改为 `false` 以执行同步请求：

```
xhttp.open("GET", "ajax_info.txt", false);
```

`Async = false` 通常用于快速检查。在较旧的 JavaScript 代码中，你也会发现同步请求。

由于代码需要完成应用程序，因此不需要 `onreadystatechange` 函数。

不建议使用 `XMLHttpRequest` (`async = false`) 同步方式，因为一旦服务器响应就绪，JavaScript 将停止运行。当服务器繁忙或响应较慢时，程序会挂起或停止。

同步 `XMLHttpRequest` 正在从 Web 标准中删除，但这可能需要很多年。

现代开发工具支持同步应用程序的使用，如果确实发生，将提供 `InvalidAccessError` 异常。

## 术语表

JavaScript 是世界上最灵活、最有效的脚本语言之一。使用 JavaScript，为网站添加令人难以置信的功能是所有现代 Web 开发者必备的技能。在构建的网站中理解和应用 JavaScript，将使用户能够创建基本 HTML 和 CSS 无法实现的新功能。此软件生成所有主流浏览器都能识别的交互式网页。本程序旨在学习此 JavaScript 术语表，它描述了你在深入学习时需要了解的主要术语。

- **函数**：函数是 JavaScript 中最关键的操作。这适用于任何旨在指导程序执行特定功能的代码块。无论该功能是命名的还是由另一个功能触发的，此特性都会执行。当用户点击按钮或新访客来到网站时，函数可以启动。
- **语句**：简单而言，你在网站上设置的任何指令都是一条语句。语句可能包含广泛的结果，但它们都创建了一个序列，迫使你的网站采取行动。语句可以包含构件、特性以及设计的许多其他功能，并且可能包含它们。
- **对象**：对象是 JavaScript 的核心功能。简单来说，对象是变量、函数和模型的集合。由于许多特性和变量可以混合在一起，构件显著提升了网站承载更多内容的能力。
- **属性**：JavaScript 中的对象和属性密不可分。对象的输入被称为对象的属性。它们形成一个拼图，并帮助对象决定做什么以及如何做。如果你知道属性是对象的一部分，你就能理解所有这些是如何协同工作的。
- **方法**：在 JavaScript 中，一种特殊的函数被称为方法。这适用于属于具有更高维度的实体的任何形式。这些方法直接操作它们所属对象的属性，并最小化为每个你想要设计的独立结果所需的语句或函数数量。
- **异步**：在传统编码中，如果有两行同步文本，这意味着在第二行完成之前，第一行的处理尚未完成。在 JavaScript 中，异步编码实际上是可能的，这意味着你可以继续执行第二行代码，而让第一行在后台运行。将来，L1 将运行，而 L2 现在正在使用中。通常，它是单线程的，这意味着只有一组功能可用，但它为你提供了任务和用户体验的更多灵活性。
- **回调**：JavaScript 回调函数是一个只有在另一个函数完成后才能启动的函数。系列中的下一步是一个回调函数。
- **块**：在 JavaScript 中，块由这种类型的花括号定义为一组组合在一起的语句。这帮助你一次使用多个句子，通常只有一个。
- **声明式**：你询问应该做什么，然后让具体细节来完成你告诉计算机的事情。React 被认为是声明式的，因为你是在为抽象而争论，而不是直接编辑 DOM。每种高级编程语言都比低级编程语言（如汇编器）更具声明性。JavaScript 比 C 更具声明性。报告是 HTML。
- **函数作用域**：在函数中指定的任何变量在函数作用域中都是可见的，并且可以从函数内部访问。
- **不可变性**：当变量的值在开发后无法更改时，该变量是不可变的。你可以更改可变变量。
- **作用域**：变量在程序的哪个部分可见，被称为变量的作用域。`let` 和 `const` 具有块作用域，这决定了与具有函数作用域的 `var` 值不同的范围。
- **作用域界定**：作用域界定是编程语言中计算变量和函数数量的方式。例如，我们可以有块作用域、函数作用域、词法作用域。

## 结语

欢迎来到终点线！希望 JavaScript 对你有益。我们从一个获取用户详细信息并更新整个页面的 "Hello, World." 脚本走了很长一段路。

几页内容涉及了大量的 JavaScript，所以如果你没有抓住某个描述或将其输入面板，不要为代码片段而烦恼。最重要的是，目标从来不是完全掌握 JavaScript。正如承诺的那样，只是勉强触及了 JavaScript 所能做的一切的表面。就像其他所有 Web 标准一样，JavaScript 在不断发展——我们无法学习所有这些，所以我们不必这样做。如果你真的想学习编程，你需要动手编写程序。阅读书籍和反思代码可能既愉快又有启发性，但真正能发展你的知识、专业技能和韧性的是解决问题和发展技术。

JavaScript 是语言的一个重要特性。它们通常对于从其他代码中隐藏变量非常有用，这样我们就不会在其他地方使用变量名。由于 jQuery 经常依赖方法参数函数，它们也可能被无意中生成。学习它们有助于我们更高效、更简洁地编写代码，并且通过使用内置的安全措施稍加注意，我们可以防止与内存相关的故障。JavaScript 高度通用和灵活，在完成本课程后，你有许多不同的前进路径。在纯 JavaScript 之后，你可以转向 Vue 和 React 等前端框架。

# 120 道 JavaScript 高级面试题



![](img/image_rsrc2Y3.jpg)


-   120\. 浅拷贝与深拷贝

# 引言

准备好提升你的 JavaScript 技能了吗？《高级 JavaScript 面试题》是你掌握 JavaScript 的必备指南，无论你是初学者还是专家。





在动态的 Web 开发世界中，JavaScript 占据主导地位。本书涵盖了从入门级程序员、寻求成长的初级开发者、追求熟练的中级工程师，到追求卓越的高级开发者的整个范围。即使是经验丰富的专家也能发现提升 JavaScript 技能的宝贵见解。

# 01\. 解释相等性

问题：JavaScript 既有严格比较，也有类型转换比较：

*   严格比较（例如 `===`）检查值的相等性，不允许强制类型转换。
*   抽象比较（例如 `==`）检查值的相等性，允许强制类型转换。

解决方案：

```
const a = "42";
const b = 42;
console.log(a == b); // true
console.log(a === b); // false
```

一些简单的相等规则：如果比较中的任一值（也称为一侧）可能是 `true` 或 `false`，请避免使用 `==`，改用 `===`。如果比较中的任一值可能是这些特定值（`0`、`""` 或 `[]`——空数组），请避免使用 `==`，改用 `===`。在其他所有情况下，你可以安全地使用 `==`。它不仅安全，而且在许多情况下，它还能简化代码，提高可读性。

# 02\. 理解指数运算符

问题：解释 JavaScript 中指数（`**`）运算符的用法，包括何时以及如何使用它进行幂运算。

解决方案：JavaScript 中的指数运算符（`**`）用于执行幂运算，即将一个数提升到某个幂次。这是一种简洁直观的进行此类计算的方式。

使用方法如下：

```
// 使用指数运算符
const result1 = 2 ** 3; // 2 的 3 次方
console.log(result1); // 8

const result2 = 4 ** 8.5; // 4 的平方根
console.log(result2); // 131072

const result3 = 10 ** -2; // 10 的 -2 次方
console.log(result3); // 0.01
```

指数运算符可以用于整数和浮点数指数。当你需要以清晰简洁的方式进行幂运算时，它特别有用。

# 03\. 更改页面标题

问题：更改页面标题

解决方案：使用 `document.title` 属性

你可以使用 JavaScript 中的 `document.title` 属性更改网页的标题。

```
document.title = "我的新标题";
```

这是 JavaScript 中一项直接的任务。更改页面标题就像给 `document.title` 属性赋一个新值一样简单。这是一个大多数 Web 开发者都应该熟悉的基本操作，因此是一个简单的问题。然而，在从事 Web 开发项目时，理解这个概念仍然很重要。

# 04\. 理解 JSON

问题：解释什么是 JSON（JavaScript 对象表示法）及其在 Web 开发中的用途。

解决方案：JSON，全称 JavaScript 对象表示法，是一种轻量级的数据交换格式，易于人类读写，也易于机器解析和生成。它通常用于服务器与 Web 应用程序之间，以及应用程序不同部分之间的数据交换。

JSON 以键值对的形式表示，其中键是字符串，值可以是字符串、数字、布尔值、数组或其他 JSON 对象。

JSON 对象的基本语法如下：

```
{
  "key1": "value1",
  "key2": 123,
  "key3": true,
  "key4": ["item1", "item2"],
  "key5": {
    "nestedKey": "nestedValue"
  }
}
```

JSON 因其简单性、易用性以及与各种编程语言的兼容性而被广泛使用。它是 Web API 中发送和接收数据、配置应用程序以及存储配置设置的常见格式。

# 05\. 讨论数据类型

问题：讨论 JavaScript 中可用的各种数据类型，并为每种类型提供示例。

解决方案：JavaScript 提供了一系列用于存储值的数据类型：

| 字符串：用引号（单引号或双引号）括起来的字符序列。 | `let myString = "Hello World"` |
| --- | --- |
| 数字：数值，包括整数和浮点数。 | `let myNumber = 42;` |
| 布尔值：表示 true 或 false 值。 | `let myBoolean = true;` |
| 数组：有序的值集合。 | `let myArray = [1, 2, 3];` |
| null：有意表示没有值。 | `let myNull = null;` |
| 对象：保存键值对。键是字符串，值可以是任何数据类型。 | `let myObject = { name: "John", age: 30 };` |
| undefined：表示未初始化的变量。 | `let myUndefined; console.log(myUndefined); // undefined` |

这些 JavaScript 数据类型使得能够以各种方式存储和操作值，构成了动态且多功能编程的基础。

# 06\. 混入与实现多重继承

问题：在 JavaScript 中，没有内置的多重继承支持，这使得在不同对象之间高效共享功能变得具有挑战性。传统的类层次结构可能变得复杂且僵化，阻碍了代码的可维护性。

解决方案：混入提供了一种解决方案，通过实现代码复用和某种形式的多重继承。混入是一种将方法和属性从一个对象合并到另一个对象的方式。这增强了代码设计的模块化和灵活性。

实现：要实现混入，你可以使用 `Object.assign()` 方法将方法和属性从源对象复制到目标对象。

以下是一个简单示例：

```
const greetingsMixin = {
  sayHello() {
    console.log("来自混入的问候");
  }
};

const objectA = {};
Object.assign(objectA, greetingsMixin);
objectA.sayHello(); // "来自混入的问候"

const objectB = {};
Object.assign(objectB, greetingsMixin);
objectB.sayHello(); // "来自混入的问候"
```

通过应用混入，你可以实现代码复用并避免深层次的类层次结构。但是，在使用多个混入时，要注意潜在的方法冲突和意外的覆盖。

# 07\. 如何实现多态

问题：多态是面向对象编程中的一个基本概念，它使对象能够呈现多种形式。在 JavaScript 中，可以通过函数重载来实现多态，即一个函数可以根据接收到的参数数量和类型有多种实现方式。

以下是一个简单示例，说明如何在 JavaScript 中实现函数重载：

```
function greet(name, language = 'English') {
  if (language === 'English') {
    console.log(`Hello ${name}`);
  } else if (language === 'Spanish') {
    console.log(`Hola ${name}`);
  }
}

greet('John'); // Hello John
greet('Juan', 'Spanish'); // Hello Juan
```

解决方案：在这个示例中，`greet` 函数接受两个参数：`name` 和 `language`。`language` 的默认值设置为 `'English'`。如果你只用一个参数调用该函数，它将使用默认语言。然而，当你用两个参数调用该函数时，它将使用指定的语言。

这种机制展示了如何通过函数重载在 JavaScript 中实现多态，允许单个函数根据提供的输入表现出不同的行为。

# 08\. 理解 JavaScript 中的数组及其创建

问题：解释 JavaScript 中的数组，以及创建数组的过程。

解决方案：数组是有序的值集合，可以包含各种数据类型。它们使用方括号 `[]` 创建，值之间用逗号分隔。

创建数组：要创建数组，请使用方括号并在其中列出值。

```
let myArray = [1, 2, 3, "Hello", true];
```

数组索引：JavaScript 中的数组是零索引的，这意味着第一个元素的索引为 0，第二个元素的索引为 1，依此类推。

操作数组：数组可以通过多种方式修改。例如，要在末尾添加元素，使用 `push()`；要删除特定索引处的元素，使用 `splice()`：

```
let myArray = [1, 2, 3];
myArray.push(4); // 在末尾添加 4：[1, 2, 3, 4]
myArray.splice(1, 1); // 删除索引 1 处的元素：[1, 3, 4]
```





数组用法：数组在 JavaScript 中对于组织和存储值的集合至关重要。它们通常与循环配合使用来遍历元素。

# 09. 回调函数

问题：详细说明 JavaScript 中的回调函数。

解决方案：在 JavaScript 中，回调函数是作为参数传递给另一个函数，并在父函数完成任务后执行的函数。回调在异步编程中扮演关键角色，使得代码能够在异步操作完成后执行。

回调函数示例：

```
function getData(callback) {
  let data = "data";
  callback(data);
}

function recieveData(data) {
  console.log(data);
}

getData(recieveData); // 'data'
```

在上述代码中，`getData` 接受一个名为 `callback` 的参数，该参数是一个函数。获取数据后，`getData` 调用 `callback` 函数，并将 `data` 作为参数传递。`receiveData` 函数是一个回调，作为参数传递给 `getData`，并记录数据。

常见用法：回调函数在 JavaScript 中非常普遍，被用于各种 API 和库中来管理异步行为。例如，你可以将回调函数与 `fetch` API 一起使用来处理异步 HTTP 请求：

此处，`fetch` 函数返回一个 promise。`then` 方法接受回调函数来处理成功的响应和错误。

```
fetch("https://api.example.com/data")
  .then(response => response.json())
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error(error);
  })
```

# 10. NEGATIVE_INFINITY

问题：解释 JavaScript 中 `NEGATIVE_INFINITY` 的概念。

解决方案：在 JavaScript 中，`NEGATIVE_INFINITY` 是一个特殊常量，表示可能的最小数值。它用于表示无限小的值，代表数值无法再减小的极限。

示例用法：`NEGATIVE_INFINITY` 出现的一种常见情况是当负数除以零时：

```
let result = -5 / 0;
console.log(result); // -Infinity
```

在这种情况下，负数除以零会得到负无穷大，如 `-Infinity` 所示。

注意：正数除以零会产生正无穷大（`Infinity`），而零除以零会得到一个特殊值 `NaN`（非数字）。

常见应用：`NEGATIVE_INFINITY` 的概念在处理数值接近数值系统理论极限的数学或计算操作时尤为重要。

# 11. 理解 NaN

问题：解释 JavaScript 中 `NaN` 的概念和用法。

解决方案：在 JavaScript 中，`NaN` 代表“非数字”（Not-a-Number）。它是一个特殊值，用于表示无效或未定义的数学运算结果。

在第一个示例中，尝试将 0 除以 0 会导致未定义的数学运算，产生 `NaN`。类似地，尝试对包含字符串（"hello"）进行数学运算也会产生 `NaN`。

`NaN` 的独特行为：`NaN` 的特殊之处在于它不等于任何值，包括它自身。

```
let result = 0 / 0;
console.log(result); // NaN

let stringResult = "hello" / 2;
console.log(stringResult); // NaN
```

检查 `NaN`：要判断一个值是否为 `NaN`，可以使用 `isNaN()` 函数：

```
let value = NaN;
console.log(isNaN(value)); // true

let anotherValue = "hello";
console.log(isNaN(anotherValue)); // true
```

重要性和用法：理解 `NaN` 对于在 JavaScript 中处理数学运算至关重要。检查 `NaN` 可以防止因无效输入导致的意外计算，并提高代码的可靠性。

# 12. if-else 语句

问题：详细说明 JavaScript 中 `if-else` 语句的用法。

解决方案：`if-else` 语句提供了一种根据指定条件为真或假来做出决策的方法。它们允许根据条件的结果执行不同的代码块。

示例

```
let num = 5;
if (num > 10) {
  console.log("The number is greather than 10.");
} else {
  console.log("The number is less than or equal to 10.");
}
// 'The number is less than or equal to 10.'
```

在此场景中，`if` 语句检查 `num` 是否大于 10。如果为真，则执行第一个块中的代码；否则，执行 `else` 块中的代码。

为了处理多个条件，可以使用 `else if` 块：

```
let num = 15;
if (num < 5) {
  console.log("The number is less than 5.");
} else if (num < 10) {
  console.log("The number is between 5 and 10.");
} else {
  console.log("The number is greater than or equal to 10.");
}
// The number is greater than or equal to 10.
```

这里，第一个 `if` 块检查 `num` 是否小于 5。如果为假，则 `else if` 块检查它是否小于 10。如果两个条件都为假，则执行 `else` 块中的代码。

# 13. Try-Catch 语句

问题：解释 JavaScript 中 `try-catch` 语句的目的和用法。

解决方案：在 JavaScript 中，`try-catch` 语句提供了一种管理和处理代码执行过程中可能出现的错误的方法。它们允许开发者“尝试”一段代码并“捕获”任何出现的错误，从而防止这些错误导致程序崩溃。

Try-Catch 语句示例：

```
try {
  let x = y;
} catch (error) {
  console.error(error);
}
// ReferenceError: y is not defined
```

在此场景中，`try` 块包含可能导致错误的代码。如果发生错误，`catch` 块会捕获该错误并执行其中的代码。在此示例中，由于 `y` 未定义，抛出了一个 `ReferenceError`。传递给 `catch` 块的错误对象包含有关错误的信息，有助于诊断。

用途和重要性：`try-catch` 语句对于受控的错误处理非常有价值。开发者可以捕获错误、收集相关信息，甚至向用户提供有意义的错误消息，而不是让错误导致整个程序崩溃。这有助于构建更友好、更稳定的应用程序。

# 14. 类型转换函数

问题：解释 JavaScript 中 `parseInt()`、`parseFloat()`、`Number()` 和 `String()` 函数的用途和用法。

解决方案：在 JavaScript 中，类型转换函数用于在不同数据类型之间转换值。这些函数对于确保数据针对各种操作进行适当转换至关重要。

类型转换函数示例：

`parseInt()`：该函数解析一个字符串参数并返回指定基数（进制）的整数。

```
console.log(parseInt("123", 10)); // 123
```

`parseFloat()`：用于解析一个字符串参数并返回一个浮点数。

```
console.log(parseFloat("3.14")); // 3.14
```

`parseInt()`：该函数解析一个字符串参数并返回指定基数（进制）的整数。

```
console.log(parseInt("123", 10)); // 123
```

`parseFloat()`：用于解析一个字符串参数并返回一个浮点数。

```
console.log(parseFloat("3.14")); // 3.14
```

重要性和用法：类型转换函数对于显式管理数据类型并确保预期结果至关重要。它们可以防止意外的类型强制转换，这种强制转换可能导致意外结果。通过使用这些函数，开发者可以控制类型转换，从而提高代码的可靠性和一致性。

# 15. 在 JavaScript 中更改元素的样式/类

问题：解释如何使用 JavaScript 更改元素的样式或类。

解决方案：要使用 JavaScript 更改元素的样式或类，可以使用 `style` 属性直接修改单个 CSS 属性，或使用 `className` 属性更改元素的类。

更改样式：你可以使用 `style` 属性直接修改元素的 CSS 属性：

```
const myText = document.getElementById("myText");
myText.style.fontSize = "20px";
```

在此示例中，ID 为 `"myText"` 的元素的字体大小被更改为 20 像素。

更改类：要更改元素的类，可以使用 `className` 属性：




```
const myElement = document.getElementById("myElement"); myElement.className = "newClassName";
```

这会将类 `"newClassName"` 分配给 ID 为 `"myElement"` 的元素。如果该元素已有其他类，则这些类会被替换。

获取类的值：要获取元素的当前类值，可以使用 `className` 属性：

```
const currentClasses = myElement.className;
```

# 16. 使用闭包在 JavaScript 中创建私有变量

问题：解释如何在 JavaScript 中创建私有变量以实现封装和隐私。提供一个使用闭包创建计数器对象的示例，该对象包含私有变量以及用于操作和访问这些变量的方法。

解决方案：你可以使用闭包在 JavaScript 中模拟私有变量。通过在函数作用域内定义变量，并返回一个包含操作这些变量的方法的对象，可以实现一定程度的封装。

```
function createCounter() {
let count = 0; // 私有变量
return {
increment: function () {
count++;
},
decrement: function () {
count--;
},
getCount: function () {
return count;
},
};
}
const counter = createCounter();
console.log(counter.getCount()); // 0 counter.increment(); counter.increment(); console.log(counter.getCount()); // 2 counter.decrement(); console.log(counter.getCount()); // 1
```

# 17. 2 的幂检查器

问题：编写一个 JavaScript 函数，接收一个整数作为输入，并判断它是否为 2 的幂。如果输入的数字是 2 的幂，则返回该数字；否则返回 -1。

解决方案：你可以通过检查数字是否大于 0 且其二进制表示中只有一个位为 1 来判断它是否为 2 的幂。可以使用位运算来实现。以下是实现方法：

```
function isPowerOf2(num) {
if (num < 0) {
return -1;
}
return (num & (num - 1)) === 0 ? num : -1;
}
console.log(isPowerOf2(8)); // 8
console.log(isPowerOf2(16)); // 16
console.log(isPowerOf2(6)); // -1
```

# 18. 如何递归反转链表？

问题：编写一个 JavaScript 递归函数来反转单链表。

解决方案：要递归反转链表，可以遵循以下步骤：

以下是递归函数的 JavaScript 代码：

```
class ListNode {
constructor(val) {
this.val = val;
this.next = null;
}
}
function reverseList(head) {
if (!head || !head.next) {
return head;
}
const newHead = reverseList(head.next);
head.next.next = head;
head.next = null;
return new Head();
}
// 创建一个链表：1 → 2 → 3 → 4 → 5 const head = new ListNode(1);
用法：head.next = new ListNode(2);
head.next.next = new ListNode(3);
head.next.next.next = new ListNode(4);
head.next.next.next.next = new ListNode(5);
const reversedHead = reversedList(head);
// 反转后的链表：5 → 4 → 3 → 2 → 1
```

# 19. FizzBuzz 挑战

问题：编写一个 JavaScript 程序，打印从 1 到 100 的数字。但对于 3 的倍数，打印 "Fizz" 而不是数字；对于 5 的倍数，打印 "Buzz"。对于既是 3 的倍数又是 5 的倍数的数字，打印 "FizzBuzz"。

解决方案：你可以使用简单的循环和条件语句来解决 FizzBuzz 挑战。

```
for (let i = 1; i < 100; i++) {
if (i % 3 === 0 && i % 5 === 0) {
console.log("FizzBuzz");
} else if (i % 3 === 0) {
console.log("Fizz");
} else if (i % 5 === 0) {
console.log("Buzz");
} else {
console.log(i);
}
```

示例输出：

1
2
Fizz
4

这段代码从 1 迭代到 100，并使用取模运算检查当前数字是否能被 3、5 或两者整除。根据条件，它打印 "Fizz"、"Buzz"、"FizzBuzz" 或数字本身。

# 20. 生成字符串的所有排列

问题：编写一个 JavaScript 递归函数，生成给定字符串的所有可能排列（变位词）。

解决方案：要生成字符串的所有排列，可以遵循以下步骤：

*   基本情况：如果字符串长度小于等于 1，则返回包含该字符串本身的数组。
*   递归步骤：对于字符串中的每个字符，使用递归生成剩余字符的排列。
*   组合：将每个字符与剩余字符的排列组合起来。

以下使用递归生成输入字符串 `"abc"` 的所有可能排列：

```
function generatePermutations(str) {
if (str.length < 2) return [str];
return str
.split("")
.flatMap((char, index) =>
generatePermutations(str.slice(0, index) + str.slice(index + 1)).map(
(permutation) => char + permutation
)
);
}
// 用法：
const input = "abc";
const result = generatePermutations(input);
console.log(result);
// [ 'abc', 'acb', 'bac', 'bca', 'cab', 'cba' ]
```

# 21. await 和 yield 关键字的区别

问题：解释 JavaScript 中 `await` 关键字和 `yield` 关键字的区别。

解决方案：`await` 和 `yield` 关键字用于不同的上下文，并且具有不同的用途：

*   `await`：在异步函数中暂停执行，直到等待的 Promise 被解决或拒绝。用于异步操作，以实现更接近同步代码的编写风格。
*   `yield`：在生成器函数中暂停执行，并向迭代器产生一个值。用于创建可暂停和恢复的迭代器，通常用于惰性求值。

```
// 使用 await 的示例：
const fetchData = async () => {
const data = await (await fetch("https://api.example/data")).json();
console.log(data);
};
// 使用 yield 的示例：
function* generateNumbers() {
yield 1;
yield 2;
yield 3;
}
const iterator = generateNumbers();
console.log(iterator.next().value); // 1
console.log(iterator.next().value); // 2
console.log(iterator.next().value); // 3
```

# 22. import * as X from 'X' 的用法

问题：解释在 JavaScript 中何时以及为何使用 `import * as X from 'X'` 语法。

解决方案：`import * as X from 'X'` 语法用于导入整个模块并将其分配给别名 `X`。这允许你使用别名 `X` 访问模块的所有导出。

当你想要导入并使用模块的多个导出，而不必单独列出每个导出时，可以使用此语法。当模块包含一组相关的函数、常量或类时，它特别有用。

示例：假设你有一个名为 `mathUtils` 的模块，其中包含多个函数：

```
// mathUtils.js
export function add(a, b) {
return a + b;
}
export function subtract(a, b) {
return a - b;
}
export function multiply(a, b) {
return a * b;
}
```

注意：虽然使用 `import * as X from 'X'` 可以避免列出单个导出，但也要注意，如果模块包含大量导出，可能会导致不必要的内存使用。在代码组织和可维护性合理的情况下使用它。

你可以使用别名导入所有函数：

```
// main.js
import * as mathFunctions from "./mathUtils";
console.log(mathFunctions.add(5, 3)); // 8 console.log(mathFunctions.subtract(5, 3)); // 6 console.log(mathFunctions.multiply(3, 7)); // 21
```

# 23. 理解 new 关键字

问题：解释 JavaScript 中 `new` 关键字的用途和用法。

解决方案：JavaScript 中的 `new` 关键字用于从构造函数创建对象的实例。它是 JavaScript 面向对象编程的重要组成部分，用于创建具有构造函数定义的特定属性和方法的对象。

当你将 `new` 关键字与构造函数一起使用时，会发生以下步骤：

1.  创建一个新的空对象。
2.  调用构造函数，并将 `this` 上下文设置为新创建的对象。
3.  使用构造函数内部的 `this` 关键字向对象添加属性和方法。
4.  除非函数显式返回另一个对象，否则新对象将从构造函数返回。



以下是使用 `new` 关键字创建对象实例的示例：

```
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const person1 = new Person("John", 30);
console.log(person1.name); // "John"
console.log(person1.age); // 30
```

解释：JavaScript 中的 `new` 关键字用于基于构造函数创建对象实例，允许你为这些实例定义和初始化属性和方法。在此示例中，`Person` 构造函数与 `new` 关键字一起使用，创建了一个 `Person` 对象的实例。构造函数内部的 `this` 关键字指向新创建的对象，并将属性 `name` 和 `age` 赋值给它。

# 24. 克隆对象

问题：解释如何在 JavaScript 中克隆一个对象，包括潜在的陷阱。

解决方案：要在 JavaScript 中克隆对象，可以使用 `Object.assign()` 方法。该方法会创建一个新对象，并将源对象的属性复制到新对象中。但需要注意的是，`Object.assign()` 执行的是浅拷贝，这意味着嵌套对象不会被深度复制；它们仍然引用与原始对象相同的嵌套对象。示例如下：

```
let obj = {
  a: 1,
  b: 2,
  c: {
    age: 30,
  },
};

let objclone = Object.assign({}, obj);
console.log("objclone: ", objclone);
// objclone: { a: 1, b: 2, c: { age: 30 } }

obj.c.age = 45;
console.log("After Change - obj: ", obj);
// After Change - obj: { a: 1, b: 2, c: { age: 45 } }
console.log("After Change - objclone: ", objclone);
// After Change - objclone: { a: 1, b: 2, c: { age: 45 } }
```

解释：在 JavaScript 中克隆对象可以使用 `Object.assign()` 方法，但请记住它创建的是浅拷贝。要实现对象的深拷贝，你需要实现一个自定义的深拷贝函数。在此示例中，`objclone` 对象是 `obj` 对象的浅拷贝。当修改嵌套对象 `obj.c` 时，`obj` 和 `objclone` 都会反映这一变化。

# 25. 在数组的开头和结尾添加元素

问题：解释如何使用不同的方法在数组的开头和结尾添加元素。

解决方案：要在数组开头添加元素，可以使用 `unshift()` 方法或展开运算符。要在数组结尾添加元素，可以使用 `push()` 方法或展开运算符。

```
// 使用 unshift() 和 push() 方法
var myArray = ['a', 'b', 'c', 'd'];
myArray.unshift("start"); // 在开头添加 'start'
myArray.push("end"); // 在结尾添加 'end'
console.log(myArray);
// ["start", "a", "b", "c", "d", "end"]

// 使用展开运算符
myArray = ["start", ...myArray]; // 在开头添加 "start"
myArray = [...myArray, "end"]; // 在结尾添加 "end"

// 使用展开运算符在一行内完成
myArray = ["start", ...myArray, "end"];
```

两种方法都能实现向数组添加元素的效果。`unshift()` 方法在开头添加元素，`push()` 方法在结尾添加元素，而展开运算符允许你在数组的任意位置添加元素。

# 26. 基数排序算法

问题：解释基数排序算法的工作原理，这是一种用于对整数或字符串按其数字或字符进行排序的线性时间排序算法。

解决方案：基数排序是一种非比较排序算法，它通过将元素根据其各个数字或字符分配到桶中来进行排序。它从最低有效位到最高有效位依次考虑每个数字或字符进行排序。

基数排序的工作原理如下：

*   **选择基数**：基数排序使用一个基数来表示数字或字符。对于整数，基数通常为 10（十进制）；对于字符串，基数为可能字符的数量（例如，小写英文字母为 26）。
*   **排序迭代**：排序过程分为多次迭代，迭代次数等于元素中最大数字（对于整数）或字符（对于字符串）的位数。
*   **桶分配**：在每次迭代中，根据当前位上的数字或字符将元素分配到桶中。元素根据当前位的值进行分组。
*   **收集桶**：分配完成后，按放置顺序从桶中收集元素，保持每个桶内的顺序。
*   **重复**：对后续的每个数字或字符重复分配和收集过程，从最低有效位向最高有效位移动。
*   **最终排序顺序**：所有迭代完成后，元素将根据每个数字或字符的值完成排序。

基数排序对于具有固定位数或字符数的大型数据集排序非常高效。其时间复杂度为 O(nk)，其中 n 是元素数量，k 是数字或字符的位数。

# 27. 测量 JavaScript 函数的性能

问题：解释如何使用 `performance.now()` 方法测量 JavaScript 函数的性能。

解决方案：要测量 JavaScript 函数的性能，可以使用 `performance.now()` 方法，该方法提供毫秒级的高分辨率时间戳。

具体操作如下：

```
function myFunction() {
  result = 0;
  for (let i = 0; i < 1000; i++) {
    result += Math.sqrt(i);
  }
  console.log("Result:", result);
  //​Result: 21065.833110879048
}

const start = performance.now();
myFunction();
const end = performance.now();
const timeTaken = end - start;
console.log(`Time taken: ${timeTaken} milliseconds`);
// Time taken: 0.10000000894069672 milliseconds
```

在此示例中，`start` 在调用函数之前捕获当前时间戳，`end` 在函数执行完成后捕获时间戳。`end` 与 `start` 的差值即为函数执行所花费的时间。

# 28. JavaScript 中 call() 和 apply() 的区别

问题：突出 JavaScript 中 `call()` 和 `apply()` 的主要区别。

解决方案：`call()` 和 `apply()` 都是 JavaScript 中用于调用函数的方法，但它们在向被调用函数传递参数的方式上有所不同。

`call()`：`call()` 方法用于以给定的 `this` 值和逐个提供的参数（逗号分隔）来调用函数。

```
function example(a, b) {
  console.log(a + b);
}
example.call(null, 1, 2); // 3
```

在此示例中，`call()` 的第一个参数设置 `example` 函数内部的 `this` 值。后续参数作为单独的值传递。

`apply()`：`apply()` 方法与 `call()` 类似，但它接受一个数组或类数组对象作为参数。

```
function example(a, b) {
  console.log(a + b);
}
example.apply(null, [1, 2]); // 3
```

这里，`apply()` 方法将第一个参数作为 `this` 值，第二个参数作为要传递给函数的参数数组。

解释：`call()` 和 `apply()` 的主要区别在于它们向被调用函数传递参数的方式。`call()` 期望参数以逗号分隔的单独形式传递，而 `apply()` 则接受包含参数的数组或类数组对象。两种方法都用于设置函数内部的 `this` 值。理解这些区别有助于你根据具体用例选择合适的方法。

# 29. 实现灵活语法的求和函数

编写一个 `sum` 方法，使其能够通过以下两种语法之一调用：

```
console.log(sum(2, 3)); // 5
console.log(sum(2)(3)); // 5
```

解决方案：你可以通过两种不同的方式实现 `sum` 函数：

方法一：使用函数重载

```
function sum(x, y) {
  if (y !== undefined) {
    return x + y;
  } else {
    return function (y) {
      return x + y;
    };
  }
}

console.log(sum(2, 3)); // 5
console.log(sum(2)(3)); // 5
```

方法二：使用 `arguments` 对象

```
function sum(x) {
  if (arguments.length === 2){
    return arguments[0] + arguments[1];
  } else {
```




```
return function(y) {

return x + y;

};

}

}

console.log(sum(2, 3)); // 5

console.log(sum(2)(3)); // 5
```

在这两种方法中，函数会检查是否提供了第二个参数。如果提供了，则执行加法并返回结果；如果没有提供，则返回一个接收第二个参数并执行加法的函数。这使得你可以使用两种语法来调用 `sum` 函数。

# 30. 使用 `Array.isArray()` 方法

问题：解释 JavaScript 中 `Array.isArray()` 方法的用途。

解答：JavaScript 中的 `Array.isArray()` 方法用于判断一个给定值是否为数组。这是一种检查对象类型的便捷方式，尤其是在处理多种数据类型时。

使用方法如下：

```
let fruits = ['apple', 'banana', 'orange']; console.log(Array.isArray(fruits)); // true

let numbers = 123;

console.log(Array.isArray(numbers)); // false
```

# 31. 类

问题：理解 JavaScript 中的类

解答：类是面向对象编程中的一个基本概念，在 ECMAScript 6（ES6）中引入，用于在 JavaScript 中定义对象及其行为。它们作为创建对象的模板，允许你将相关数据和函数封装在单个对象中。

以下是在 JavaScript 中定义和使用类的基本示例：

```
class Person {

constructor(name, age) {

this.name = name;

this.age = age;

}

sayHello() {

console.log(

`Hello, my name is ${this.name} and I am ${this.age} years old.`

);

}

}

const john = new Person("John", 32);

john.sayHello(); // Hello, my name is John and I am 32 years old.
```

在这个示例中，我们定义了一个 `Person` 类，其中包含一个用于初始化对象属性的 `constructor` 方法，以及一个用于输出问候语的 `sayHello` 方法。然后我们创建了 `Person` 类的一个实例，并调用了它的 `sayHello` 方法。

类提供了一种方便且组织化的方式来处理 JavaScript 中的对象及其行为，使代码更易于维护和阅读。

# 32. 探索 Web Worker 的强大功能

问题：解释 JavaScript 中 Web Worker 的概念、用途及其在 Web 应用中的工作方式。

解答：Web Worker 是 JavaScript 中的一项功能，允许你在后台运行脚本，与 Web 应用的主执行线程分离。它们旨在通过将 CPU 密集型或耗时的任务（如数据处理或复杂计算）卸载到单独的线程，从而提高性能和响应能力。这样，它们可以防止这些任务阻塞主线程，确保用户界面保持流畅和响应迅速。

关键概念和注意事项：

- **独立线程**：Web Worker 在独立线程中运行，意味着它们有自己的执行上下文，不与主线程共享变量或内存。这种隔离防止了冲突和数据损坏。
- **通信**：Web Worker 可以通过消息系统与主线程进行双向通信。你可以使用 `postMessage()` 方法在两个线程之间发送数据、对象或指令。
- **无 DOM 访问**：Web Worker 无法直接访问文档对象模型（DOM）。这一限制确保它们不能直接操作网页内容或与用户界面交互。
- **安全性**：由于独立的执行上下文，Web Worker 通过防止潜在恶意代码影响主线程和网页功能来增强安全性。
- **Web Worker 的类型**：有两种类型的 Web Worker：专用 Worker（绑定到特定脚本）和共享 Worker（可由多个脚本或页面访问）。
- **使用场景**：Web Worker 在需要执行资源密集型任务而不影响用户体验的场景中非常有用。常见用例包括：
  - **数据处理**：在后台处理大型数据集、解析 JSON 或执行复杂计算。
  - **图像处理**：在不阻塞主线程的情况下处理和编辑图像。
  - **实时应用**：通过将通信任务卸载到 Web Worker 来实现实时聊天或多人在线游戏等功能。
  - **并行处理**：利用多核或多处理器来提高视频编码或模拟等任务的性能。

理解 Web Worker 的工作原理以及何时使用它们，可以显著提升 Web 应用的性能和响应能力。

# 33. `Array.of()` 方法

问题：解释 JavaScript 中 `Array.of()` 方法的用途。

解答：JavaScript 中的 `Array.of()` 方法用于创建一个新的 `Array` 实例，其参数数量可变，无论参数的数量或类型如何。当你事先不知道需要向函数传递多少个参数时，这个方法非常有用。`Array.of()` 方法返回一个包含传入参数作为元素的 `Array` 对象。

以下是 `Array.of()` 方法的使用示例：

```
let numbers = Array.of(1, 2, 3, 4, 5);

console.log(numbers); // [ 1, 2, 3, 4, 5 ]
```

在这个示例中，我们向 `Array.of()` 方法传递了 5 个参数，它创建了一个新的 `Array` 实例 `numbers`，其中包含元素 1、2、3、4 和 5。

# 34. 什么是计算属性

问题：解释 JavaScript 对象中的计算属性是什么，并提供如何定义它们的示例。

解答：JavaScript 对象中的计算属性允许动态定义属性名。它们通过在对象字面量中使用方括号 `[]` 来定义。计算属性对于创建属性名在运行时确定或基于变量的对象属性非常有用。

示例如下：

```
const dynamicKey = "age";

const person = {

name: "John",

[dynamicKey]: 30,

[1 + 2]: "Three",

};

console.log(person.name); // John

console.log(person.age); // 30

console.log(person[3]); // Three
```

在这个示例中，属性名 'age' 由 `dynamicKey` 变量决定。当属性名依赖于运行时条件时，计算属性提供了灵活性。

注意：计算属性是现代 JavaScript（ES6+）的特性。它们可能在不支持 ES6 的旧浏览器中无法工作。

# 35. 输出是什么？

```
class Counter {

#number = 10;

increment() {

this.#number++;

}

getNum() {

return this.#number;

}

}

const counter = new Counter();

counter.increment();

console.log(counter.getNum()); // 11
```

A: 10

B: 11

C: `undefined`

D: `SyntaxError`

答案：D

在 ES2020 中，我们可以通过使用 `#` 在类中添加私有变量。这些变量不能在类外部访问。当我们尝试输出 `counter.#number` 时，会抛出 `SyntaxError`：我们无法在 `Counter` 类外部访问它！

# 36. 转义字符

问题：解释 JavaScript 中转义字符的概念。提供常用转义序列及其含义的示例。

解答：JavaScript 中的转义字符是一种字符，它表示其后的字符具有特殊含义，不应按通常的上下文解释。它用于表示键盘上不易输入的字符，或在字符串或正则表达式中具有特殊含义的字符。

以下是一些常用的转义序列及其含义：

*   `\n`：表示换行符。
*   `\t`：表示制表符。
*   `\"`：表示双引号字符。
*   `\'`：表示单引号字符。
*   `\\`：表示反斜杠字符本身。

使用示例：

```
console.log("This is a string with a newline:\nSecond line");

// This is a string with a newline:

// Second line

console.log("This is a string with a tab:\tTabbed text"); // This is a string with a tab: Tabbed text

console.log("This is a string with a double quote: \"Hello\"");

// This is a string with a double quote: "Hello"

console.log('This is a string with a single quote: \'Hi\'');

// This is a string with a single quote: 'Hi'

console.log("This is a string with a backslash: \\");
```




// 这是一个带有反斜杠的字符串：\

转义字符允许你在字符串中包含特殊字符，而不会与字符串的结构或含义冲突。

# 37. 将非布尔值强制转换为布尔值

问题：当非布尔值被强制转换为布尔值时，它会变成 `true` 还是 `false`？

解决方案：以下是会被强制转换为 `false` 的值（假值）的示例：

`""`（空字符串）

`0`、`-0`、`NaN`（无效数字）

`null`、`undefined`

`false`

JavaScript 中“假值”的具体列表：

不在该列表中的任何值都是“真值”。“真值”的示例：

`"hello"`

`42`

`true`

`[ ]`、`[ 1, "2", 3 ]`（数组）`{ }`、`{ a: 42 }`（对象）`function foo() { .. }`（函数）

# 38. 理解 IIFE

问题：解释 JavaScript 中 IIFE（立即调用函数表达式）的概念。提供一个如何创建和使用 IIFE 的示例，并讨论为什么它们在 JavaScript 中很常用。

解决方案：IIFE，即立即调用函数表达式，是一种常见的 JavaScript 设计模式。它们是在创建后立即定义并执行的函数。IIFE 具有以下语法：

```
(function IIFE() {
  console.log("Hello!");
})(); // Hello!
```

使用 IIFE 的原因有以下几个：

*   **封装**：它们为变量创建了一个新的作用域，防止变量名与代码其他部分冲突。这有助于避免污染全局作用域。
*   **数据隐私**：在 IIFE 内部声明的变量无法从外部访问，提供了一定程度的数据隐私。这对于隐藏实现细节很有用。
*   **初始化**：IIFE 可用于初始化代码，例如设置配置、加载模块或在其余代码执行之前执行任何必要的设置。
*   **避免污染**：它们通过限制变量和函数的暴露，有助于防止全局作用域污染。
*   **模块模式**：IIFE 常用于在 JavaScript 中实现模块模式，允许你创建具有私有和公共成员的封装模块。

# 39. 何时在 ES6 中使用箭头函数

```
const add = (a, b) => {
  return a + b;
};

console.log(add(5, 3)); // 8
```

问题：在 ES6 及更高版本中使用函数的经验法则：

在全局作用域和 `Object.prototype` 属性中使用 `function`。

对于对象构造函数使用 `class`。

在其他所有地方使用 `=>`（箭头函数）。

解决方案：为什么几乎在所有地方都使用箭头函数？

*   **作用域安全**：箭头函数确保始终使用与根相同的 `this` 对象，避免作用域问题。
*   **简洁性**：箭头函数更易读且更简洁。
*   **清晰性**：当大部分函数都是箭头函数时，任何常规函数都会显得突出，使作用域更加清晰。开发者可以引用上一级函数语句来确定 `this` 对象。

# 40. `null` 和 `undefined` 的区别

问题：解释 JavaScript 中 `null` 和 `undefined` 用法的区别，并提供每种情况适用的示例场景。

解决方案：在 JavaScript 中，`null` 和 `undefined` 都用于表示缺少值，但它们的使用场景略有不同。

`null`：用于显式表示有意缺少任何对象值。例如，可以将其赋值给一个变量，以明确表示该变量没有值。

```
let myVar = null;
// 显式赋值为 null
```

`undefined`：表示一个变量已被声明但尚未赋值。此外，它也是未提供参数的函数参数的默认值。

```
let myVar; // 已声明但未赋值（undefined）

function myFunction(param) {
  console.log(param);
  // undefined（如果未提供参数）
}
```

`null` 用于显式表示没有值，而 `undefined` 表示缺少赋值的值。

# 41. 闭包

问题：解释 JavaScript 中闭包的概念，并提供一个实际示例说明其用法。

解决方案：在 JavaScript 中，闭包是一个强大的概念，它允许函数记住并访问其词法作用域，即使在该作用域之外执行也是如此。闭包“封闭”了其包含函数中的变量，即使在该函数执行完毕后，仍保留对这些变量的访问权限。

```
function outerFunction() {
  const outerVariable = "I am from outerFunction";

  function innerFunction() {
    console.log(outerVariable);
    // 内部函数可以访问 outerVariable
  }

  return innerFunction;
}

const clousureFunction = outerFunction();
clousureFunction(); // I am from outerFunction
```

在示例中，`innerFunction` 是一个闭包，因为即使在 `outerFunction` 执行完毕后，它仍然保留对 `outerVariable` 的访问权限。当调用 `closureFunction` 时，它仍然可以访问 `outerVariable` 并输出其值。

闭包常用于 JavaScript 应用程序中的封装、数据隐私和状态维护。

# 42. JavaScript 中的防抖及其实际应用

问题：解释 JavaScript 中防抖的概念，并提供一个应用防抖能带来好处的场景。

解决方案：防抖是一种用于控制基于重复事件执行函数频率的技术。它确保函数仅在自上次事件发生后经过一定时间后才执行。这在处理可能快速触发的事件（例如调整浏览器窗口大小或在输入字段中打字）时特别有用。

示例：想象一个搜索栏，当用户输入时会发送 API 请求。如果没有防抖，每次按键都可能触发 API 请求，可能会使服务器不堪重负。通过应用防抖，我们可以延迟 API 请求的执行，直到用户暂停输入，从而减少发送的请求数量。

```
function debounce(func, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => {
      func(...args);
    }, delay);
  };
}

// 将防抖应用于事件监听器
const searchInput = document.getElementById("search-input");
const debouncedSearch = debounce(doSearch, 300);
searchInput.addEventListener("input", debouncedSearch);

function doSearch() {
  // 在此处执行实际搜索或 API 请求
  console.log('Searching...');
}
```

在此示例中，`doSearch` 函数通过 `debounce` 函数进行了防抖处理。`debounce` 返回的 `debouncedSearch` 函数只会在自上次输入事件后经过 300 毫秒延迟后才执行 `doSearch` 函数。这可以防止用户在输入时发出过多的 API 请求。

# 43. JavaScript 中的提升及其对声明的影响

问题：解释 JavaScript 中提升的概念，并讨论它对作用域内变量和函数声明顺序的影响。

解决方案：提升是 JavaScript 中的一种行为，在编译阶段，变量和函数声明会被移动到其各自作用域的顶部。这可能导致你可以在代码中正式声明变量和函数之前就使用它们或调用它们。

示例：

```
console.log(myVariable); // undefined
var myVariable = 10;

myFunction(); // Hello, World!
function myFunction() {
  console.log("Hello, World!");
}
```

在示例中，变量声明 `var myVariable` 和函数声明 `function myFunction()` 被提升到其作用域的顶部，使我们能够在它们实际声明之前使用它们。

然而，只有声明被提升，初始化和赋值不会被提升。因此，虽然 `myVariable` 是可访问的，但其值为 `undefined`，直到它被赋值为 `10`。

理解提升对于编写清晰且可维护的代码至关重要，建议将变量和函数声明放在其各自作用域的开头，以提高清晰度。

# 44. 标签

问题：什么是 JS 标签？




解决方案：标签语句允许我们在 JavaScript 中为循环和代码块命名。之后我们可以使用这些标签来引用之前的代码。例如，下面的带标签代码在数字相同时避免打印它们。

示例：

```
var i, j;

loop1: for (i = 0; i < 3; i++) {
  loop2: for (j = 0; j < 3; j++) {
    if (i === j) {
      continue loop1;
    }
    console.log("i = " + i + ", j = " + j);
  }
}

// 输出为：
// "i = 1, j = 0"
// “i = 2, j = 0"
// "i = 2, j = 1"
```

# 45. 交换变量

问题：解释在 JavaScript 中交换两个变量值的各种技术，并讨论每种方法的优缺点。

解决方案：交换变量可以通过使用临时变量、算术运算或解构赋值来实现。

示例 1：使用临时变量

```
let a = 5;
let b = 10;
let temp;
temp = a; // 5
a = b; // 10
b = temp; // 5
```

示例 2：使用算术解构运算

```
let a = 5;
let b = 10;
a = a + b; // 15
b = a - b; // 5
a = a - b; // 10
```

示例 3：使用解构赋值

```
let a = 5;
let b = 10;
[a, b] = [b, a];
```

# 46. 使用事件委托

问题：解释 JavaScript 中事件委托的概念，并讨论其在 Web 开发中管理事件的优势。

解决方案：事件委托是将单个事件监听器附加到共同的祖先元素上，而不是为每个子元素添加多个监听器。这种方法在性能和动态添加的元素方面具有优势。

示例：考虑一个包含多个项目的列表，每个项目都有一个按钮。不必为每个按钮添加事件监听器，而是可以为列表元素添加一个监听器，并使用事件委托来处理按钮点击。

```
document.querySelector("#list").addEventListener("click", function (event) {
  if (event.target.tagName === "BUTTON") {
    // 处理按钮点击
  }
});
```

事件委托通过减少事件监听器的数量来提高效率，尤其是在处理大量或动态更新的内容时。

# 47. 使用 `bind()` 函数

问题：解释 JavaScript 中 `bind()` 函数的概念和用例。提供示例说明如何使用 `bind()` 来保留上下文以及创建带有预设参数的新函数。

解决方案：JavaScript 中的 `bind()` 函数用于创建一个具有固定上下文（`this` 值）和预设参数的新函数。它通常用于在将方法作为回调传递时保留原始上下文、创建具有部分应用参数的新函数以及创建专用函数。

示例：保留上下文

```
const user = {
  name: "John",
  greet: function () {
    console.log(`Hello, ${this.name}!`);
  },
};

const greetFunction = user.greet;
greetFunction(); // Hello, undefined!

const boundGreet = user.greet.bind(user);
boundGreet(); // Hello, John!
```

示例：创建新函数

```
const sayHello = function(name) { console.log(`Hello, ${name}!`);
};

const sayHi = sayHello.bind(null, "Alice");
sayHi(); // Hello, Alice!
```

示例：部分函数应用

```
function add(a, b) { return a + b;
}

const addFive = add.bind(null,
5);
console.log(addFive(3)); // 8
```

# 48. 使用 ES6 生成器生成斐波那契数列

问题：在 JavaScript 中创建一个生成器函数，用于生成斐波那契数列。实现该生成器以逐个生成斐波那契数。使用该生成器打印前 10 个斐波那契数。

解决方案：你可以使用 ES6 生成器函数来生成斐波那契数列。生成器函数维护前两个数的状态，并生成当前的斐波那契数。

以下是实现和使用该生成器的方法：

```
function* fibonacciGenerator() {
  let prev = 0;
  1;
  let current = 1;
  1;
  while (true) {
    2;
    yield current;
    3;
    const next = prev + current;
    5;
    prev = current;
    8;
    current = next;
    13;
  }
  21;
}
34;
55;

const fibonacci = fibonacciGenerator();
for (let i = 0; i < 10; i++) {
  console.log(fibonacci.next().value);
}
```

# 49. 递归二分查找

问题：在 JavaScript 中实现一个递归函数，对已排序数组执行二分查找。

解决方案：二分查找是一种分治算法，它将目标元素与数组的中间元素进行比较。以下是如何实现具有较高难度的递归二分查找函数：

```
function binarySearchRecursive(arr, target, left = 0, right = arr.length - 1) {
  if (left <= right) {
    const middle = Math.floor((left + right) / 2);
    if (arr[middle] === target) {
      return middle; // 找到元素
    } else if (arr[middle] > target) {
      return binarySearchRecursive(arr, target, left, middle - 1); // 搜索左半部分
    } else {
      return binarySearchRecursive(arr, target, middle + 1, right); // 搜索右半部分
    }
  }
  return -1; // 未找到元素
}

const sortedArray = [1, 3, 5, 7, 9, 11, 13, 15];
console.log(binarySearchRecursive(sortedArray, 7)); // 输出：3（7 在数组中的索引）
console.log(binarySearchRecursive(sortedArray, 8)); // 输出：-1（未找到元素）console.log(binarySearchRecursive(sortedArray, 8)); // 输出：-1（未找到元素）
```

# 50. 使用尾递归计算第 n 个斐波那契数

问题：在 JavaScript 中编写一个尾递归函数，用于计算第 n 个斐波那契数。斐波那契数列是一个数字序列，其中每个数字是前两个数字之和：0, 1, 1, 2, 3, 5, 8, ...

解决方案：尾递归是一种技术，其中递归函数的最后操作是递归调用本身。以下是如何实现一个具有较高难度的尾递归函数来计算第 n 个斐波那契数：

```
function fibonacciTailRecursive(n, a = 0, b = 1) {
  if (n === 0) {
    return a;
  } else if (n === 1) {
    return b;
  }
  return fibonacciTailRecursive(n - 1, b, a + b);
}

console.log(fibonacciTailRecursive(0)); // 0 console.log(fibonacciTailRecursive(1)); // 1 console.log(fibonacciTailRecursive(5)); // 5 console.log(fibonacciTailRecursive(10)); // 55
```

在这个实现中，`a` 和 `b` 用于跟踪前两个斐波那契数。该函数使用这些值计算下一个斐波那契数，并使用更新后的值进行尾递归调用。

# 51. 使用 `reduce` 方法

问题：解释 JavaScript 中 `reduce` 方法的概念、参数以及如何用它来对数组执行操作。提供一个使用 `reduce` 方法求数组之和的示例。

解决方案：`reduce` 方法是一个高阶函数，用于迭代处理数组元素并累积为单个值。它接受两个主要参数：一个回调函数和一个初始值（可选）。

`reduce` 方法中使用的回调函数接受两个参数：

*   accumulator（`acc`）：每次迭代更新的累积值。

*   currentValue（`curr`）：数组中当前正在处理的值。

以下是使用 `reduce` 方法求数字数组之和的示例：

```
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((acc, curr) => acc + curr, 0); console.log(sum); // 10
```

`reduce` 的用途：计算总和、平均值或任何类型的累积。

*   查找最大值或最小值。

*   展平嵌套数组。

*   按某个属性对元素进行分组。

在上面的示例中，`reduce` 方法从初始累积值 0 开始。回调函数在每次迭代中将当前值（`curr`）加到累积值（`acc`）上。处理完所有元素后，返回最终的总和。

# 52. 检查同构字符串

问题：编写一个函数来判断两个给定的字符串是否同构。如果可以通过替换一个字符串中的字符得到另一个字符串，同时保持字符顺序，则这两个字符串被认为是同构的。

解决方案：

```
function areIsomorphic(str1, str2) {
  if (str1.length !== str2.length) {
    return false;
  }
}
```





```
const map1 = new Map();

const map2 = new Map();

for (let i = 0; i < str1.length; i++) {

const char1 = str1[i];

const char2 = str2[i];

if (!map1.has(char1)) {

map1.set(char1, char2);

} else if (map1.get(char1) !== char2) {

return false;

}

if (!map2.has(char2)) {

map2.set(char2, char1);

} else if (map2.get(char2) !== char1) {

return false;

}

}

return true;

}

// Test cases

console.log(areIsomorphic("egg", "add")); // true

console.log(areIsomorphic("foo", "bar")); //​false

console.log(areIsomorphic("paper", "title")); //​true
```

解释：函数 `areIsomorphic` 接收两个字符串作为输入，并使用两个映射（`map1` 和 `map2`）来跟踪两个字符串中字符之间的映射关系。它遍历两个字符串，检查相同索引处的字符是否相互映射。如果映射在任何时候被破坏，则这两个字符串不是同构的。

# 53. 判断一个值是否为整数

问题：讨论在 JavaScript 中编写函数 `isInteger(x)` 以判断 `x` 是否为整数的多种方法。

解决方案：在 JavaScript 中判断一个值是否为整数可能比看起来更棘手，尤其是考虑到在 ECMAScript 规范中所有数值都以浮点值存储。以下是实现此目的的不同方法：

使用按位异或运算符（ECMAScript 6）：

```
function isInteger(x) {
  return Number.isInteger(x);
}
```

使用取模运算符和类型检查：

```
function isInteger(x) {
  return (typeof x === 'number') && (x % 1 === 0);
}
```

使用 `Math.round()` 和严格比较：

```
function isInteger(x) {
  return Math.round(x) === x;
}
```

避免使用 `parseInt()`：

```
function isInteger(x) {
  return parseInt(x, 10) === x;
}
```

注意：由于字符串转换，`parseInt()` 方法在处理大数时可能会失败。

所有这些方法都有其细微差别和注意事项。前三种方法可靠且能处理大多数情况。然而，了解边界情况很重要，例如每种方法如何处理 `Infinity` 和 `-Infinity`。

解释：由于 JavaScript 的浮点表示，判断一个值是否为整数可能具有挑战性。根据需求和潜在的边界情况，你可以选择合适的方法。

# 54. DOM 元素树遍历与回调

问题：创建一个函数，使用深度优先搜索遍历一个 DOM 元素及其所有后代，并为每个访问的元素调用提供的回调函数。

解决方案：你可以通过实现一个递归的深度优先搜索遍历函数来实现，该函数访问每个元素及其子元素，并为每个访问的元素调用提供的回调。

```
function Traverse(element, callback) {
  callback(element); // 为当前元素调用回调
  var children = element.children;
  for (var i = 0; i < children.length; i++) {
    Traverse(children[i], callback); // 对每个子元素递归调用
  }
}

// 示例用法
function callbackFunction(element) {
  console.log(element.tagName); // 打印元素的标签名
}

var rootElement = document.getElementById("root"); // 将 'root' 替换为你的元素 ID
Traverse(rootElement, callbackFunction); // 从根元素开始遍历
```

在示例解决方案中，定义了 `Traverse` 函数，使用深度优先搜索遍历 DOM 树，并为每个访问的元素调用提供的回调。`callbackFunction` 是一个可以传递给 `Traverse` 函数的回调示例。

# 55. 动态属性操作

问题：解释如何在 JavaScript 中动态地向对象添加和删除属性。为每个操作提供一个示例。

解决方案：在 JavaScript 中，你可以使用点表示法或方括号表示法动态地向对象添加和删除属性。

添加属性：要向对象添加属性，只需使用点表示法或方括号表示为属性赋值。

```
let user = {}; // 创建一个空对象

// 使用点表示法添加属性
user.name = "John";
user.age = 22;

// 使用方括号表示法添加属性
user["email"] = "john@example.com";

console.log(user);
```

删除属性：要从对象中删除属性，可以使用 `delete` 关键字后跟属性名。

```
let user = {
  name: "John",
  age: 22,
  email: "johndoe@example.com",
};

console.log(user); // 原始对象

// 删除一个属性
delete user.age;

console.log(user); // 删除了 'age' 属性的对象
```

在这两种情况下，属性都是根据赋值或删除操作动态添加或删除的。

注意：使用 `delete` 关键字时要小心，因为它在某些情况下可能产生意外行为。此外，动态添加和删除属性可能会使代码的可预测性降低，因此请谨慎使用这些操作。

# 56. 何时在 ES6 中使用箭头函数

问题：在 ES6 及更高版本中使用函数的一条经验法则：

解决方案：为什么几乎在所有地方都使用箭头函数？

*   作用域安全：箭头函数确保始终使用与根对象相同的 `this` 对象，避免作用域问题。
*   简洁性：箭头函数更易读且更简洁。
*   清晰性：当大部分函数都是箭头函数时，任何常规函数都会显得突出，使作用域更加清晰。开发者可以引用下一个更高层级的函数语句来确定 `this` 对象。

```
// 在全局作用域中使用 `function`
function globalFunction() {
  console.log("This is a function in the global scope.");
}

// 使用 `class` 作为对象构造函数
class Person {
  constructor(name) {
    this.name = name;
  }
  sayHello() {
    console.log(`Hello, my name is ${this.name}.`);
  }
}

// 在其他所有地方使用 `=>`（箭头函数）
const numbers = [1, 2, 3, 4, 5];

// 使用箭头函数进行数组操作（其他所有地方）
const squaredNumbers = numbers.map((num) => num * num);
console.log(squaredNumbers);
```

# 57. ES6 类与 ES5 函数构造函数

问题：挑战在于理解 ES6 类与 ES5 函数构造函数之间的区别。

解决方案：为了说明这些差异，请考虑以下示例：

ES5 函数构造函数：

```
function Person(name) {
  this.name = name;
}
```

对于简单的构造函数，它们看起来非常相似。然而，在处理继承时会出现显著差异。例如，让我们创建一个继承 `Person` 并添加 `studentId` 字段的 `Student` 类：

ES5 函数构造函数（继承）：

```
function Student(name, studentId) {
  // 调用超类的构造函数
  // 以初始化超类派生的成员。
  Person.call(this, name);
  // 初始化子类自身的成员。
  this.studentId = studentId;
}

Student.prototype = Object.create(Person.prototype);
Student.prototype.constructor = Student;
```

ES6 类：

```
class Person {
  constructor(name) {
    this.name = name;
  }
}
```

ES6 类（继承）：

```
class Student extends Person {
  constructor(name, studentId) {
    super(name);
    this.studentId = studentId;
  }
}
```

# 58. 理解 Function.prototype.bind

问题：解释 `Function.prototype.bind` 在 JavaScript 中的用途和用法。

解决方案：`bind` 方法创建一个新函数，当该函数被调用时，其 `this` 关键字被设置为提供的值，并且可以包含预定义的参数。这在你想确保函数被调用时具有特定的 `this` 上下文和预设参数时特别有用。在实践中，`bind` 的工作方式如下：

```
const boundFunction = originalFunction.bind(thisValue, arg1, arg2, ...);
```

`boundFunction` 在后续调用时保持 `thisValue` 上下文和指定的参数。

例如，`bind` 常用于 React 组件等场景，以确保事件处理程序或回调中的 `this` 上下文正确。

示例：

```
function greet(greeting) {
  console.log(`${greeting}, ${this.name}`);
}

const person = {
  name: "John",
};

// 使用 bind 创建一个具有特定上下文和预设参数的新函数
```





```
const boundGreet = greet.bind(person, "Hello");
boundGreet(); // 输出: "Hello, John"
```

# 59. arguments 对象

问题：什么是 arguments 对象？

解决方案：`arguments` 对象是一个类数组对象，可在函数内部访问，包含传递给该函数的参数值。例如，让我们看看如何在 `sum` 函数内部使用 `arguments` 对象：

示例：

```javascript
function sum() {
  var total = 0;
  for (var i = 0, len = arguments.length; i < len; ++i) {
    total += arguments[i];
  }
  return total;
}
sum(1, 2, 3); // 返回 6
```

注意：你不能在 `arguments` 对象上应用数组方法。但你可以像下面这样将其转换为常规数组：

```javascript
var argsArray = Array.prototype.slice.call(arguments);
```

# 60. 匿名函数的典型使用场景

问题：识别使用匿名函数的常见场景。

解决方案：匿名函数通常用于……

在 IIFE（立即调用函数表达式）中：将代码封装在局部作用域内，防止变量泄漏到全局作用域。

```javascript
(function() {
  // 此处编写一些代码。
})();
```

用于函数式编程或像 Lodash 这样的库：作为函数式编程结构或库的参数，类似于回调函数。

```javascript
const arr = [1, 2, 3];
const double = arr.map(function(el) {
  return el * 2;
});
console.log(double); // [2, 4, 6]
```

作为一次性回调：当函数仅作为回调使用一次且无需在其他地方引用时。这种方法通过将函数定义靠近其使用位置来提高代码可读性。

```javascript
setTimeout(function() {
  console.log('Hello world!');
}, 1000);
```

在这些情况下，匿名函数提供了封装功能的简洁方式，改善了代码的组织性和可维护性。

# 61. 区分 `Object.freeze()` 与 `const`

问题：区分 JavaScript 中的 `Object.freeze()` 和 `const`。

解决方案：`const` 和 `Object.freeze()` 服务于不同的目的：

`const` 适用于绑定（变量），创建一个不可更改的绑定，无法重新赋值：

```javascript
const person = {
  name: "Leonardo"
};
person = animal;
// 错误 "person" 是只读的
```

`Object.freeze()` 作用于对象值，通过阻止属性更改使对象不可变：

```javascript
let person = {
  name: "Leonardo"
};
Object.freeze(person);
person.name = "Lima";
// TypeError: 无法分配给只读属性 'name' 的对象
```

本质上，`const` 是关于变量的不可变性，而 `Object.freeze()` 是关于使对象本身不可变。

# 62. 理解 JavaScript 生成器

问题：解释 JavaScript 中生成器的概念。

解决方案：生成器是可以暂停和恢复的函数。它们在重新进入时保留其上下文（变量绑定）。生成器函数使用 `function*` 语法编写。首次调用时，它们不会执行代码，而是返回一个称为生成器的特殊迭代器。当使用生成器的 `next` 方法消费一个值时，函数会运行直到遇到 `yield` 关键字。

生成器函数可以被多次调用，每次产生一个新的生成器。然而，每个生成器只能迭代一次。以下是一个生成器函数的示例：

```javascript
function* makeRangeIterator(start = 0, end = Infinity, step = 1) {
  let iterationCount = 0;
  for (let i = start; i < end; i += step) {
    iterationCount++;
    yield i;
  }
  return iterationCount;
}

// 创建一个迭代器
const iterator = makeRangeIterator(0, 10, 2);

// 迭代生成器产生的值
for (const value of iterator) {
  console.log(value);
}

// 从生成器获取结果（总迭代次数）
console.log("总迭代次数:", iterator.return().value);
```

# 63. ES6 生成器的理想使用场景

问题：识别在 ES6 中使用生成器有利的场景。

解决方案：ES6 中的生成器在以下情况下是有益的……

*   控制流操作：生成器允许函数暂停和恢复，使外部代码能够决定何时重新进入。这提供了对执行流程的精确控制。

*   异步控制：生成器有助于从代码外部管理异步调用。这种控制分离可以带来更结构化、更易理解的异步代码。

生成器的主要优势在于它们仅在需要时提供值，而不是一次性全部提供。这一特性在需要逐步获取值的情况下特别有用。

# 64. 打印数组

问题：编写一段 JavaScript 代码片段，以以下格式打印给定数组：`Array: ["DataFlair", 2023, 1.0, true]`。

解决方案：你可以通过使用循环遍历数组并构建所需的输出字符串来实现。以下是一个示例 JavaScript 代码：

```javascript
var array = ["DataFlair", 2023, 1.0, true];
var msg = "Array: [";
for (var i = 0; i < array.length - 1; i++) {
  msg += array[i] + ", ";
}
msg += array[array.length - 1] + "]";
console.log(msg); // Array: [DataFlair, 2023, 1, true]
```

# 65. 如何清空 JavaScript 数组

问题：解释清空 JavaScript 数组的不同方法。

解决方案：有几种技术可以清空 JavaScript 数组：

赋值为空数组：

`emptyArray = [];`

使用 `splice()` 方法：

`definedArray.splice(0, definedArray.length);`

将数组长度设置为零：

`definedArray.length = 0;`

在循环中使用 `pop()` 或 `shift()` 方法：

```javascript
while(definedArray.length) {
  definedArray.pop(); // 或 DefinedArray.shift();
}
```

这些方法中的每一种都能实现清空数组的目标，但选择取决于性能和可读性等因素。

# 66. JavaScript 中 `close()` 的功能是什么？

问题：解释 JavaScript 中 `close()` 的功能。

解决方案：JavaScript 中的 `close()` 函数用于关闭当前聚焦的窗口。它主要用于关闭使用 JavaScript 打开的浏览器窗口或标签页。要使用此函数，你需要调用 `window.close()`。需要注意的是，此函数只能关闭使用 JavaScript 打开的窗口或标签页。如果窗口/标签页不是由脚本打开的，由于安全原因，可能不允许关闭它。

示例：

```javascript
// 打开一个新窗口
const newWindow = window.open("https://www.example.com", "_blank");
// 关闭新打开的窗口
newWindow.close();
```

在上面的示例中，`window.open()` 用于打开一个新窗口，然后 `newWindow.close()` 用于关闭该窗口。需要注意浏览器设置和安全限制，这些可能会阻止在某些场景下使用此函数。

# 67. 解释 `"use strict"` 函数。

问题：解释 JavaScript 中 `"use strict"` 指令的目的和用法。

解决方案：`"use strict"` 指令是 ECMAScript 5 (ES5) 中引入的一项特性，用于在 JavaScript 代码中强制执行更严格的规则和更好的错误处理。当在脚本或函数的开头包含它时，会激活严格模式，这有助于捕获常见的编码错误并防止使用潜在有问题的特性。

在严格模式下：不允许使用未声明的变量或属性，会导致 ReferenceError。

*   不允许给未声明的变量赋值。

*   不允许删除变量、函数或函数参数。

*   不允许在函数声明中重复参数名称。

*   不允许八进制语法（例如 `0123`）。

*   不允许给只读属性或不可写的全局变量赋值。

*   在函数和方法中，`this` 值不会被强制转换为全局对象。

*   不允许使用 `with` 语句。

*   避免在非严格模式下意外创建全局变量。




使用 `"use strict"` 有助于开发者编写更安全、更易维护的代码，因为它能捕获错误并强制实施良好的编码实践。需要注意的是，严格模式是向后兼容的，这意味着只要解决了它可能指出的问题，你就可以安全地将其添加到现有代码中，而不会破坏功能。

# 68. 文档加载过程

**问题：** 理解浏览器中文档加载的过程以及 JavaScript 在此过程中的作用。

**解决方案：** 文档加载过程包括解析 HTML、构建 DOM、加载外部资源、执行脚本以及事件处理。`<script>` 标签内的 JavaScript 脚本会被加载并执行。它们可以修改 DOM 并与用户交互进行交互。

**示例代码：**

```html
<!DOCTYPE html>
<html>
<head>
<title>文档加载示例</title>
</head>
<body>
<h1>你好，世界！</h1>
<button id="myButton">点击我</button>
<script>
var button = document.getElementById('myButton'); button.addEventListener('click', function() {
alert('按钮被点击了！');
});
});
</script>
</body>
</html>
```

# 69. 解释 JavaScript 浏览器对象模型（BOM）

**问题：** 解释 JavaScript 浏览器对象模型（BOM）

**解决方案：** JavaScript 中的浏览器对象模型（BOM）提供了一种与浏览器功能交互的方式。

下面是一个简单的示例，演示了如何使用 BOM 的 `alert()` 方法显示弹出对话框：

```javascript
// 使用 BOM 显示一个警告框 alert("你好，BOM！");
```

在这个示例中，`alert()` 方法是 BOM 的一部分，用于在浏览器中显示弹出警告。BOM 包含各种对象和属性，允许开发者控制浏览器特定的功能。

# 70. JavaScript 中的类型转换是什么？

**问题：** 解释 JavaScript 中的类型转换

**解决方案：** JavaScript 中的类型转换涉及将值从一种数据类型转换为另一种数据类型。以下是三种主要的类型转换函数：

- `Boolean(value)`：此函数将输入值转换为布尔数据类型。

  例如：

  ```javascript
  var num = 10;
  var boolValue = Boolean(num); // boolValue 将为 true
  ```

- `Number(value)`：此函数将输入值转换为浮点数或整数。

  例如：

  ```javascript
  var str = "123";
  var numValue = Number(str); // numValue 将为 123
  ```

- `String(value)`：此函数将输入值转换为字符串。

  例如：

  ```javascript
  var num = 456;
  var strValue = String(num); // strValue 将为 "456"
  ```

类型转换是一种有用的技术，可确保变量在所需的数据类型上下文中被处理和使用。

# 71. 将文件的所有导出作为一个对象导入

**问题：** 在 JavaScript 中将所有导出作为一个对象导入

**解决方案：** 使用对象导入所有导出

要在 JavaScript 中将文件的所有导出作为一个对象导入，可以使用 `import * as` 语法。这允许你通过导入对象上的点（`.`）运算符访问所有导出的成员。以下是一个示例：

假设你有一个名为 `utils.js` 的文件，其中包含以下导出：

```javascript
// utils.js
export const multiply = (a, b) => a * b;
export const divide = (a, b) => a / b;
export const add = (a, b) => a + b;
```

你可以使用以下代码导入所有导出：

```javascript
import * as utils from "./utils.js";
console.log(utils.multiply(5, 2)); // 10
console.log(utils.divide(10, 2)); // 5
console.log(utils.add(3, 7)); // 10
```

# 72. JavaScript 中不同类型的弹出框

**问题：** JavaScript 中弹出框的类型

**解决方案：** 弹出框的解释

JavaScript 提供了三种类型的弹出框与用户交互：`alert()`、`confirm()` 和 `prompt()`。

- `alert()`：以弹出框的形式向用户显示一条简单消息。它包含一个用于确认的“确定”按钮。通常用于向用户显示信息或通知。

  ```javascript
  alert("这是一条警告消息。");
  ```

- `prompt()`：显示一个输入对话框，包含一条消息、一个输入字段以及两个按钮：“确定”和“取消”。当你希望用户输入某个值时使用，它会以字符串形式返回用户输入的值。

  ```javascript
  const inputValue = prompt("请输入您的姓名："); if (inputValue) {
  console.log(`你好，${inputValue}！`);
  } else {
  console.log("未输入姓名。");
  }
  ```

- `confirm()`：显示一个确认弹出框，包含一条消息和两个按钮：“确定”和“取消”。当你希望用户确认某个操作时使用，它会返回一个布尔值，表示用户的选择。

  ```javascript
  const result = confirm("您确定要继续吗？"); if (result) {
  // 用户点击了确定 } else {
  // 用户点击了取消
  }
  ```

# 73. 如何向对象添加/删除属性？

**问题：** JavaScript 对象中属性的添加和删除

**解决方案：** 对象属性的动态操作

在 JavaScript 中，你可以使用多种技术动态地向对象添加或删除属性。

**添加属性：** 你可以通过直接为新属性名赋值来向对象添加属性。

```javascript
let user = {};
user.name = "Anil";
user.age = 25;
console.log(user); // { name: 'Anil', age: 25 }
```

**删除属性：** 你可以使用 `delete` 关键字后跟对象和属性名来删除对象的属性。

```javascript
delete user.age;
console.log(user); // { name: 'Anil' }
```

请记住，虽然这些方法允许你动态添加和删除属性，但在修改对象时，考虑其对对象结构和功能的影响非常重要。

# 74. 如何解码或编码 URL？

**问题：** JavaScript 中的 URL 编码和解码

**解决方案：** 使用 `encodeURI()` 和 `decodeURI()`

在 JavaScript 中，你可以使用 `encodeURI()` 和 `decodeURI()` 函数对 URL 进行编码和解码。这些函数有助于确保 URL 在各种操作中格式正确。

**编码 URL：** `encodeURI()` 函数用于编码 URL，将特殊字符替换为编码后的对应字符。

```javascript
var uri = "myprofile.php?name=sammer&occupation=pantiNG"; var encoded_uri = encodeURI(uri); console.log(encoded_uri);
```

**解码 URL：** `decodeURI()` 函数用于解码已编码的 URL，将编码后的字符转换回原始形式。

```javascript
var encoded_uri = "my%20profile.php?name=sammer&occupation=pantiNG"; var decoded_uri = decodeURI(encoded_uri); console.log(decoded_uri);
```

此外，如果你需要对单个 URL 组件（如查询参数）进行编码或解码，可以分别使用 `encodeURIComponent()` 和 `decodeURIComponent()` 函数。这些函数处理 URL 特定部分的编码和解码，以确保它们在 URL 中正确表示。

# 75. 解释 JavaScript Cookies

**问题：** 理解 JavaScript Cookies

**解决方案：** JavaScript Cookies

Cookies 是网站存储在用户计算机上的小数据片段。它们用于在不同网页或访问网站之间记住信息。Cookies 以文本文件的形式存储在用户的浏览器中，并在每次后续请求时发送回服务器。

Cookies 有多种用途，包括：

*   **会话管理：** Cookies 可用于通过存储唯一标识符来管理用户会话。
*   **个性化：** 网站可以使用 Cookies 记住用户偏好和设置。
*   **跟踪：** Cookies 用于跟踪用户行为，例如他们访问的页面和查看的产品，用于分析和营销目的。
*   **身份验证：** Cookies 可以存储身份验证令牌，以保持用户在不同页面上的登录状态。

以下是在 JavaScript 中设置和获取 Cookie 的示例：

```javascript
const setCookie = (name, value, expires, path) => document.cookie = `${name}=${value}; expires=${expires.toUTCString()}; path=${path}`;
const getCookie = (name) => (document.cookie.match(`(^|; )${name}= ([^;]*)`) || [])[2] || "";
setCookie("username", "John Doe", new Date("Thu, 18 Dec 2023 12:00:00 UTC"), "/");
const username = getCookie("username");
console.log("用户名：", username); // 用户名：John Doe
```



Cookie 存在局限性，例如大小限制、安全问题，以及它们会随每个请求发送，即使是静态资源也不例外。

# 76. REST API

解决方案：REST API（表述性状态转移应用程序编程接口）是现代 Web 开发中的一个基本概念。它是一种架构风格，使用一组约束和 HTTP 方法来实现客户端与资源之间的交互。

以下是 REST API 相关关键组件和概念的详细说明：

- 资源：资源是你可以通过 API 进行交互的数据实体。例如，在博客应用中，资源可以包括文章、评论和用户。
- HTTP 方法：REST API 使用标准的 HTTP 方法对资源执行操作：
  - GET：从服务器检索数据。
  - POST：在服务器上创建新资源。
  - PUT：更新现有资源，如果不存在则创建。
  - DELETE：从服务器删除资源。
- 无状态性：RESTful API 是无状态的，这意味着从客户端到服务器的每个请求都必须包含理解和处理该请求所需的所有信息。服务器不会在请求之间存储任何关于客户端状态的信息。
- 响应格式：API 响应通常采用 JSON 格式，便于人类和机器阅读和理解数据。
- 身份验证：为了保护敏感资源，REST API 通常需要身份验证。常见方法包括 API 密钥、OAuth 令牌或用户名/密码。
- 状态码：HTTP 状态码用于指示 API 请求的结果。例如，200 状态码表示成功，而 404 状态码表示请求的资源未找到。
- 端点：端点是表示资源的特定 URL。例如，`/articles` 可以是检索文章列表的端点，而 `/articles/1` 可以表示 ID 为 1 的特定文章。
- 版本控制：API 版本有助于确保 API 演进时的向后兼容性。版本号通常包含在 URL 中（例如，`/v1/articles`）。

要在 JavaScript 中与 REST API 交互，你可以使用像 `fetch`、`Axios` 或 `jQuery.ajax` 这样的库来发送 HTTP 请求并处理响应。以下是使用 `fetch` API 从 RESTful 端点检索数据的示例。

```
fetch('https://api.example.com/articles' )
.then(response => response.json())
.then(data => {
//      Handle the JSON response data here console.log(data);
})
.catch(error => {
//      Handle any errors during the request
console.error(error);
})
```

# 77. 本地存储

问题：探索 JavaScript 中的本地存储

解决方案：本地存储是 Web 浏览器中的一种 Web 存储机制，允许网站在用户设备上本地存储键值对。与 Cookie 不同，本地存储可以存储更大量的数据（通常可达 5-10MB），并且不会随每个 HTTP 请求发送，因此对于需要跨会话持久化的数据来说，它是一种更高效的选择。

本地存储有多种用例，包括：

* 持久化数据：本地存储可用于存储即使在用户关闭浏览器或离开网站后也需要保留的数据。
* 用户偏好：网站可以将用户偏好和设置存储在本地存储中，以提供个性化体验。
* 离线数据：本地存储允许网站通过本地缓存数据并在设备在线时同步，从而提供离线功能。
* 缓存：网站可以使用本地存储来缓存静态资源（如图片和样式表），以提高页面加载速度。

以下是在 JavaScript 中使用本地存储的示例：

```
//       Set data in Local Storage localStorage.setItem("username", "John Doe"); localStorage.setItem("theme", "dark");

//       Retrieve data from Local Storage

const username = localStorage.getItem("username");

const theme = localStorage.getItem("theme");

console.log("Username: " + username);

//       Username: John Doe console.log("Theme: " + theme);

//       Theme: dark

//       Remove data from Local Storage localStorage.removeItem("theme");
```

需要注意的是，本地存储是同步的，并且在同源策略下运行。这意味着存储在本地存储中的数据只能由同一设备上的同一网站访问。此外，用户可以通过浏览器设置手动清除某个网站的本地存储。

# 78. 输出是什么？

```
const createMember = ({ email, address = {} }) => { const validEmail = /.+\@.+\..+/.test(email); if(!validEmail) throw new Error("Valid email pls");

return {

email,

address: address ? address : null,

};

};

const member = createMember({ email: "my@email.com" }); console.log(member);
```

- A: `{ email: "my@email.com", address: null }`
- B: `{ email: "my@email.com" }`
- C: `{ email: "my@email.com", address: {} }`
- D: `{ email: "my@email.com", address: undefined }`

答案：C

`address` 的默认值是一个空对象 `{}`。当我们设置变量 `member` 等于 `createMember` 函数返回的对象时，我们没有为 `address` 传递值，这意味着 `address` 的值是默认的空对象 `{}`。空对象是一个真值，这意味着 `address ? address : null` 条件的结果为真。因此 `address` 的值是空对象 `{}`。

# 79. 在 JavaScript 中发起 AJAX 请求：实用指南

解决方案：AJAX（异步 JavaScript 和 XML）是一种强大的技术，用于在不重新加载整个网页的情况下从服务器发送和接收数据。它是现代 Web 开发的基础部分，常用于获取数据、提交表单以及动态更新内容等任务。

以下是使用两种常见方法在 JavaScript 中发起 AJAX 请求的方式：

1. 使用 `XMLHttpRequest` (XHR)：

```
// Create a new XMLHttpRequest object

var xhr = new XMLHttpRequest();

// Configure the request (GET or POST, URL, and async flag)

xhr.open("GET", "https://example.com/api/data", true);

// Define a callback function to handle the response

xhr.onreadystatechange = function () {

if (xhr.readyState === 4 && xhr.state === 200) {

var responseData = xhr.responseText;

console.log(responseData);

}

};

// Send the request

xhr.send();
```

2. 使用 Fetch API（现代方法）：

```
// Use the fetch function to make a GET request

fetch("https://example.com/api/data")

.then(response => { if(!response.ok) {

throw new Error("Network response was not ok");

}

return response.text();

​You can also use response.json() for JSON data

})

.then(data => { console.log(data); })

.catch(error => { console.error("Fetch error:", error);
```

# 80. 事件

问题：理解 JavaScript 事件

解决方案：在 JavaScript 中，事件是浏览器中发生的动作或事件，例如用户点击按钮、按下按键或调整窗口大小。JavaScript 中的事件处理涉及通过执行特定代码或函数来响应这些事件。在 JavaScript 中，事件是浏览器中发生的动作或事件，例如用户点击按钮、按下按键或调整窗口大小。JavaScript 中的事件处理涉及通过执行特定代码或函数来响应这些事件。

以下是 JavaScript 中处理事件所涉及的步骤：

1. 选择元素：首先，你需要选择要附加事件的 HTML 元素。这可以通过使用 `getElementById`、`querySelector` 等方法，或通过 JavaScript 直接访问元素来完成。
2. 添加事件监听器：一旦你有了元素，就可以为其添加事件监听器。事件监听器是一个函数，当元素上发生特定事件时会被执行。你可以使用 `addEventListener` 方法来附加事件监听器。





3. 定义事件处理程序：事件监听函数也称为事件处理程序。它包含事件发生时应该运行的代码。这段代码可以包含任何所需的操作，例如更新内容、更改样式或触发其他函数。

以下是将点击事件处理程序附加到按钮元素的示例：

```
// 选择按钮元素
const button = document.getElementById("myButton");
// 添加点击事件监听器
button.addEventListener("click", function() {
alert("按钮被点击！");
});
```

在这个示例中，当按钮被点击时，事件处理函数会显示一个包含消息“按钮被点击！”的`alert`。

事件处理是创建交互式和动态 Web 应用程序的基础。它允许开发者响应用户操作，并提供无缝的用户体验。

# 81. While 循环

问题：解释 JavaScript 中 while 循环的用法。

解决方案：JavaScript 中的 while 循环用于在给定条件为真时重复执行一段代码块。

while 循环的基本语法如下：

```
while (条件) {
// 要执行的代码块
}
```

例如，考虑以下打印数字 1 到 5 的代码：

```
let i = 1;
while(i <= 5) {
console.log(i);
i++;
}
//       1
//       2
//       3
//       4
//       5
```

在这个示例中，每次迭代都会检查条件 `i <= 5`。如果条件为 `true`，则执行 while 循环内的代码块。每次迭代通过 `i++` 语句将 `i` 的值增加 1。当条件 `i <= 5` 变为 `false` 时，循环停止，并继续执行循环之后的代码。

# 82. 如何在 JavaScript 中访问历史记录

问题：在 JavaScript 中访问浏览历史对于控制用户导航至关重要。使用 `window.history` 访问和操作浏览器历史记录有哪些可用选项？

解决方案：要访问 JavaScript 中的浏览历史，可以使用 `window.history` 对象，它提供了与浏览器会话历史交互的方法和属性。

以下是一些常见选项：

*   `window.history.back()`：此方法模拟点击浏览器的“后退”按钮，将用户带到历史记录中的上一个页面。

*   `window.history.forward()`：此方法模拟点击浏览器的“前进”按钮，如果存在，则将用户带到历史记录中的下一个页面。

*   `window.history.go(n)`：此方法允许导航到历史记录中的特定页面。参数 `n` 可以是正整数或负整数，正数表示在历史记录中向前移动，负数表示向后移动。

*   `window.history.length`：此属性返回浏览历史记录中的条目数，表示用户访问过的页面数量。

需要注意的是，出于安全和隐私限制，出于安全原因，你无法访问用户浏览历史的详细信息，例如他们访问过的 URL。你只能在当前页面历史记录的上下文中进行导航。

# 83. 理解 JavaScript 错误类型

问题：解释 JavaScript 中的七种内置错误类型，并提供每种错误类型可能发生的示例。

解决方案：JavaScript 有七种内置错误类型，每种都有特定的用途：

`EvalError`：与全局函数 `eval()` 相关的问题发生时出现。例如：

```
try {
  eval("alert('Hello, world!')");
} catch (error) {
  if (error instanceof EvalError) {
    console.error(error.message);
    // "eval() has been disabled"
  }
}
```

`InternalError`：表示 JavaScript 引擎内部的错误，例如堆栈溢出。这些错误很少见，通常表明引擎本身存在严重问题。

`RangeError`：当数值变量或参数超出其有效范围时发生。例如：

```
const arr = new Array(Infinity);
// RangeError: Invalid array length
```

`SyntaxError`：由语法错误引起，导致代码无法解析，例如缺少括号：

```
const x = (3;
// SyntaxError: Unexpected token ';'
```

`ReferenceError`：当引用无效变量时发生，例如尝试访问未声明的变量：

```
console.log(x);
// ReferenceError: x is not defined
```

`TypeError`：当参数或变量不是预期类型，或者对不适当类型执行操作时发生：

```
const num = 42;
num();
// TypeError: num is not a function
```

`URIError`：当向 `decodeURI()` 或 `encodeURI()` 等函数传递无效参数时发生：

```
decodeURI("%");
// URIError: URI malformed
```

# 84. 理解原型链

问题：解释原型链在 JavaScript 面向对象编程（OOP）中的工作原理及其在继承中的重要性。

解决方案：JavaScript OOP 中的原型链指的是对象可以将属性查找委托给另一个对象的机制。这用于继承，即一个对象可以从父对象继承属性和方法。

当从构造函数创建对象时，JavaScript 会自动将新创建的对象链接到构造函数的原型。这种链接创建了原型链，并允许新对象从原型继承属性和方法。

```
// 定义一个构造函数
function Animal(name) {
  this.name = name;
}
// 为构造函数定义一个原型属性
Animal.prototype.makeSound = function() {
  return "I'm an animal and my name is " + this.name;
};
// 从构造函数创建一个对象
var dog = new Animal("dog");
// 访问对象的属性和方法
console.log(dog.makeSound()); // "I'm an animal and my name is dog"
```

# 85. `isFinite` 函数的用途是什么

问题：你是一名 JavaScript 开发者，正在处理一个需要验证某个值是否为有限数字的项目。你听说过 JavaScript 中的 `isFinite` 函数，但不确定它的用途或如何正确使用。你想了解它的功能以及如何在项目中应用它。

解决方案：`isFinite` 函数是 JavaScript 中的内置函数，用于判断给定值是否为有限数字。如果该值是有限数字，则返回 `true`，否则返回 `false`。

```
//       示例 1：有限数字
var num1 = 42;
var result1 = isFinite(num1);
console.log(result1); // 返回 true
//       示例 2：非数值（NaN）
var num2 = NaN;
var result2 = isFinite(num2);
console.log(result2); // 返回 false
//       示例 3：正无穷大值
var num3 = Infinity;
var result3 = isFinite(num3);
console.log(result3); // 返回 false
//       示例 4：负无穷大值
var num4 = -Infinity;
var result4 = isFinite(num4);
console.log(result4); // 返回 false
//       示例 5：不表示数字的字符串
var str = "Hello";
var result5 = isFinite(str);
console.log(result5); // 返回 false
```

在这个示例中，`isFinite` 用于检查不同值的有限性，包括有限数字、`NaN` 和无穷大。当你需要验证某个值是否适合进行数学计算，或者确保它不是像 `NaN` 或 `Infinity` 这样的特殊值时，这个函数非常有用。

确保你理解 `isFinite` 的工作原理，将允许你在程序中执行适当的检查，以处理各种数值类型。

# 86. 理解空值合并运算符

问题：你希望在 JavaScript 中处理可能为 `null` 或 `undefined` 的变量时设置默认值，同时避免空字符串或 0 等假值。

解决方案：空值合并运算符（`??`）为这个问题提供了一个优雅的解决方案。当左侧操作数为 `null` 或 `undefined` 时，它返回右侧操作数（默认值）。否则，它返回左侧操作数。

示例：

```
const someValue = null;
const defaultValue = 'Hello, world!';
const result = someValue ?? defaultValue;
```





```
console.log(result); // 'Hello, world!'
```

在这个例子中，`??` 运算符检查 `someValue` 是否为 `null` 或 `undefined`，如果是，则赋值为 `defaultValue`。这样，你可以确保只有真正缺失的值才会触发默认赋值。

在你的 JavaScript 代码中使用 `nullish coalescing operator`（`??`）来更精确地处理默认值，尤其是在需要将 `null` 或 `undefined` 与其他假值区分处理的场景中。

# 87. JavaScript 中的原始数据类型有哪些？

问题：JavaScript 中的原始数据类型

解决方案：在 JavaScript 中，原始数据类型是简单、不可变的数据值，代表单一的值。JavaScript 中有五种原始数据类型：`boolean`、`undefined`、`null`、`number` 和 `string`。这些数据类型被认为是内置的，并且具有某些区别于对象的特性。

*   `boolean`：表示二进制值，要么是 `true`，要么是 `false`。
*   `undefined`：表示已声明但尚未赋值的变量。
*   `null`：表示有意缺失任何值或对象。
*   `number`：表示整数和浮点数值。
*   `string`：表示用单引号（`''`）或双引号（`""`）括起来的字符序列。

需要注意的是，这些原始数据类型是按值传递的，意味着它们的值直接存储在内存中。它们不是对象，也没有与之关联的属性或方法。

示例：

```
let isTrue = true; // boolean
let age; // undefined
let score = null; // null
let count = 5; // number
let name = "John"; // string
```

理解原始数据类型是有效使用 JavaScript 类型系统的基础。

# 88. `.forEach()` 与 `.map()` 的区别

问题：解释 JavaScript 中 `.forEach()` 循环和 `.map()` 循环的主要区别。提供在何种场景下你会选择其中一个而不是另一个。

解决方案：

`.map()` 循环：`.map()` 循环用于遍历数组的元素，并根据对每个元素执行的操作创建一个新数组。

```
// .map() 示例
const doubledNumbers = numbers.map((num) => num * 2);
console.log(doubledNumbers);
// [2,4,6,8]
```

`.forEach()` 循环：`.forEach()` 循环用于遍历数组的元素。它不会返回新数组，而是就地修改原数组。当你希望对数组的每个元素执行操作而不创建新数组时，它很有用。

```
// .forEach() 示例：
const numbers = [1, 2, 3, 4];
numbers.forEach((num) => {
  console.log(num * 2);
});
// 2
// 4
// 6
// 8
```

何时选择：当你希望遍历数组元素并执行操作而不创建新数组时，选择 `.forEach()`。当你希望将数组的每个元素转换为新值并创建一个包含这些值的新数组时，选择 `.map()`。

# 89. JavaScript 中的提升（Hoisting）

问题：使用代码片段解释 JavaScript 中的提升概念。

解决方案：提升可以通过一个例子来说明……

```
console.log(myVar); // undefined
var myVar = 10;
// 上面的代码等价于：
// var myVar;
// console.log(myVar); // undefined
// myVar = 10;
```

在这个例子中，尽管 `myVar` 在声明之前就被使用，但代码并没有报错。这是因为提升：在编译期间，`myVar` 的声明被移动到了作用域的顶部，而赋值仍然留在原地。因此，该变量被视为已声明，但在被赋值为 `10` 之前，其值为 `undefined`。

# 90. 使用 delete 运算符预测代码输出

问题：预测给定 JavaScript 代码片段的输出。

```
var output = (function(x) {
  delete x;
  return x;
})(0);
console.log(output); // 0
```

解决方案：代码的输出将是 `0`。

在这段代码片段中，`delete` 运算符被用于局部变量 `x`。然而，`delete` 运算符旨在删除对象的属性，而不是变量。由于 `x` 是局部变量，不是对象属性，因此删除操作对它没有影响。因此，赋给 `x` 的值 `0` 保持不变，并被函数返回。

# 91. 理解属性删除与原型

问题：预测给定 JavaScript 代码片段的输出。

```
var Employee = {
  company: "xyz",
};
var emp1 = Object.create(Employee);
delete emp1.company; // true
console.log(emp1.company); // 'xyz'
```

解决方案：代码的输出将是 `xyz`。

在这段代码片段中，创建了一个名为 `Employee` 的对象，其属性 `company` 的值为 `'xyz'`。然后，使用 `Object.create(Employee)` 创建了另一个对象 `emp1`，这使得 `emp1` 从 `Employee` 对象继承了 `company` 属性。

当执行 `delete emp1.company` 时，它并没有删除原型属性 `company`。`hasOwnProperty` 方法确认 `emp1` 没有自己的 `company` 属性。因此，`emp1.company` 仍然访问从原型继承的属性。

# 92. 实现单例设计模式

问题：解释单例设计模式并提供一个应用示例。

解决方案：单例设计模式确保一个类只有一个实例，并提供对该实例的全局访问点。它通常用于管理应在整个应用程序中共享的资源，例如数据库连接或配置设置。

以下是一个简单的示例：

```
class Singleton {
  constructor() {
    if (Singleton.instance) {
      return Singleton.instance;
    }
    Singleton.instance = this;
    this.data = [];
  }
  addItem(item) {
    this.data.push(item);
  }
  getItems() {
    return this.data;
  }
}

const instance1 = new Singleton();
instance1.addItem("apple");
const instance2 = new Singleton();
instance2.addItem("banana");
console.log(instance1.getItems()); // [ 'apple', 'banana' ]
console.log(instance2.getItems()); // [ 'apple', 'banana' ]
console.log(instance1 === instance2); // true
```

# 93. 解释 MVC 设计模式

问题：描述 MVC（Model-View-Controller）设计模式并提供一个应用示例。

解决方案：MVC 设计模式是一种架构模式，用于将应用程序的关注点分离为三个不同的组件：模型（Model）、视图（View）和控制器（Controller）。

*   模型：表示应用程序的数据和业务逻辑。它管理数据的存储、检索和操作。它通知视图数据的变化。
*   视图：向用户显示数据并处理用户界面交互。它从模型接收数据更新并将其呈现给用户。
*   控制器：充当模型和视图之间的中介。它从视图接收用户输入，处理它们，并相应地更新模型和视图。

考虑一个用于管理任务的 Web 应用程序。模型将处理任务的数据，例如创建、更新和删除任务。视图将向用户显示任务列表，并允许用户与之交互。控制器将处理用户操作，例如创建新任务或将任务标记为已完成。

使用 MVC 促进了关注点分离，使应用程序更加模块化、可维护和可扩展。它还允许应用程序的不同部分独立开发。

# 94. ES6 中的暂时性死区是什么？

问题：解释 ES6 中暂时性死区（TDZ）的概念，以及它如何影响 `let` 和 `const` 声明的使用。

解决方案：暂时性死区（`TDZ`）是 JavaScript 代码执行中的一个阶段，在此阶段，使用 `let` 和 `const` 声明的变量存在，但无法访问或赋值。在此阶段，尝试访问此类变量会导致 `ReferenceError`。

在提供的示例中：

```
// console.log(aLet) would throw ReferenceError
let aLet;
console.log(aLet); // undefined
aLet = 10;
console.log(aLet); // 10
```





在变量 `aLet` 实际声明之前，任何尝试访问它的操作都会抛出 `ReferenceError`。一旦变量被声明，它就进入了 `TDZ`，此时访问它会得到 `undefined`。只有在声明语句之后，变量才变得可用且可赋值。

`TDZ` 的存在是为了防止变量在正确初始化之前被使用，从而促进更安全的编码实践。

# 95. null、undefined 和未声明的变量

问题：解释 JavaScript 中 `null`、`undefined` 和未声明变量之间的区别。同时讨论如何检查这些状态。

解决方案：

未声明的变量：这些变量在未使用 `var`、`let` 或 `const` 声明的情况下被赋值。它们会在当前作用域之外被全局创建。在严格模式下，给未声明的变量赋值会导致 `ReferenceError`。要检查未声明的变量，可以将它们的用法包裹在 `try/catch` 块中。

```
function foo() {
  x = 1; // Throws a ReferenceError in strict mode
}
foo();
```

未定义的变量：这些变量已被声明但未赋值。它们的类型是 `undefined`。要检查未定义的变量，可以使用严格相等运算符（`===`）进行比较，或者使用 `typeof` 运算符，它会返回字符串 `'undefined'`。

```
var foo;
console.log(foo === undefined); // true
console.log(type foo === 'undefined'); // true
```

null 变量：这些变量被显式赋值为 `null`，表示没有值。要检查 null 变量，使用严格相等运算符（`===`）。

```
var foo = null;
console.log(foo === null); // true
```

避免使用抽象相等运算符（`==`）进行检查，因为它会将 `null` 和 `undefined` 视为相等，可能导致意外结果。

良好的实践是永远不要留下未声明或未赋值的变量。如果你暂时不打算使用某个变量，请显式地赋值为 `null`。代码检查工具也可以帮助捕获对未声明变量的引用。

# 96. 从 JavaScript 数组中消除重复值

问题：你想从 JavaScript 数组中移除重复的值，并得到一个只包含唯一值的新数组。

解决方案：有多种方法可以实现：

使用 `Set`：`Set` 对象会自动消除重复项。你可以使用 `Array.from()` 或展开运算符将 `Set` 转换回数组。

```
function uniqueArray(array) {
  return Array.from(new Set(array));
}
var arr = [1, 5, 2, 4, 1, 6];
console.log(uniqueArray(arr));
// [ 1, 5, 2, 4, 6 ]
```

使用 `filter()`：`filter()` 方法通过比较当前索引与元素的第一个索引，只保留每个元素的第一次出现。

```
function uniqueArray(arr) {
  return arr.filter((elem, index, self) => index === self.indexOf(elem));
}
var arr = [1, 5, 2, 4, 1, 6];
console.log(uniqueArray(arr)); // [ 1, 5, 2, 4, 6 ]
```

使用 `for` 循环和对象键：该方法通过遍历输入数组并使用对象跟踪唯一值来创建新数组。

选择最适合你需求和编码风格的方法。

```
function uniqueArray(dups_name) {
  var unique = {};
  dups_name.forEach(function(i) {
    if (!unique[i]) { unique[i] = true; }
  });
  return Object.keys(unique);
}
var arr = [1, 5, 2, 4, 1, 6];
console.log(uniqueArray(arr)); // [ '1', '2', '4', '5', '6' ]
```

# 97. 编写多行字符串

问题：你想在 JavaScript 中编写一个跨越多行的字符串。

解决方案：是的，你可以使用不同的方法在 JavaScript 中编写多行字符串：

使用反引号：反引号（`）字符允许你创建可以跨越多行的模板字面量。

```
var string = `line1
line2
line3`;
```

使用 `+` 运算符：你可以使用 `+` 运算符连接多个字符串，每个字符串单独一行。

```
var string = "line1" +
"line2" +
"line3";
```

使用反斜杠：你可以使用反斜杠 `\` 字符将字符串延续到下一行。

```
var string = "line1 \
line2 \
line3";
```

所有这些方法都能在 JavaScript 中实现创建多行字符串的相同结果。

# 98. 解释以下代码的输出

问题：你需要解释给定 JavaScript 代码的输出。

解决方案：提供的代码输出是 `5`。

解释：让我们逐步分解代码：

```
var courses = ["JavaScript", "Java", "C", "C++", "Python"];
delete courses[2];
console.log(courses.length);
```

定义了一个数组 `courses`，包含五个元素：`"JavaScript"`、`"Java"`、`"C"`、`"C++"` 和 `"Python"`。

使用 `delete` 运算符删除索引 `2` 处的值，该索引对应元素 `"C"`。

删除索引 `2` 处的元素后，数组变为：`["JavaScript", "Java", empty, "C++", "Python"]`。

数组的 `length` 属性仍然是 `5`，因为 `delete` 运算符只移除指定索引处的值，并不改变数组的整体大小。

因此，当执行 `console.log(courses.length)` 时，它会在控制台打印 `5`。

输出解释：尽管索引 `2` 处的值被删除，但数组长度保持不变，并且数组在索引 `2` 处有一个“空”槽。这就是输出为 `5` 的原因。

# 99. 计算关联数组的长度

问题：编写一个 JavaScript 程序来计算关联数组的长度。

解决方案：你可以通过遍历关联数组（对象）的属性并计数来计算其长度。以下是实现此功能的 JavaScript 代码：

```
// Define an associative array (object)
var associativeArray = {one: "DataFlair", two: "JavaScript", three: 435,
four: true};
// Initialize a count variable to keep track of the length
var count = 0;
// Loop through the properties of the associative array
for(var key in associativeArray) {
  if(associativeArray.hasOwnProperty(key)) { count++; // Increment the count for each property
  }
}
// Print the calculated length to the console after the loop
console.log("Length of the associative array:", count);
// Length of the associative array: 4
```

该程序定义了一个关联数组（对象），并使用循环遍历其属性。对于每个属性，计数递增。最终的计数代表关联数组的长度。

# 100. 给定代码会返回什么？

问题：给定代码会返回什么？

```
console.log(typeof typeof 1);
```

解决方案：

上述代码在控制台中的输出将是 `'string'`。

以下是求值过程的分解：

`typeof 1` 返回字符串 `'number'`。

然后，`typeof 'number'` 返回字符串 `'string'`。

因此，最终输出是 `'string'`。虽然看起来可能有点令人困惑，但结果源于 `typeof` 总是返回一个字符串，即使应用于 `typeof` 关键字本身也是如此。

# 101. 判断一个字符串是否为回文

问题：编写一个函数来判断给定的字符串是否为回文。

解决方案：以下是一个检查给定字符串是否为回文的 JavaScript 函数：

```
function isPalindrome(str) {
  str = str.replace(/\W/g, '').toLowerCase();
  // Remove non-alphanumeric characters and convert to lowercase
  var reversedStr = str.split('').reverse().join('');
  // Reverse the string
  return str === reversedStr ? "A palindrome" : "Not a palindrome";
}
console.log(isPalindrome("level")); // A palindrome
console.log(isPalindrome("levels")); // Not a palindrome
```

函数 `isPalindrome` 接受一个字符串作为输入，移除非字母数字字符并将字符串转换为小写。然后反转字符串，并检查反转后的字符串是否与原字符串相同。如果相同，函数返回 `"A palindrome"`，否则返回 `"Not a palindrome"`。

# 102. 导入和导出是什么意思？

问题：解释 JavaScript 中导入和导出的概念。





解决方案：导入和导出是促进 JavaScript 代码模块化的特性。它们允许你将代码拆分为多个文件。导入用于将特定变量或函数从某个模块引入当前模块。你可以导入由另一个模块导出的变量或方法。

以下是一个示例：

```javascript
// index.js
import name, age from './person';
console.log(name);
console.log(age);

// person.js
let name = 'Shared', occupation = 'developer', age = 26;
export { name, age };
```

# 103. 数组操作

问题：JavaScript 数组操作

解决方案：在 JavaScript 中修改数组

JavaScript 中的数组是灵活的数据结构，可以通过多种方法进行修改。以下是一些常见的数组操作技巧：

```javascript
const numbers = [1, 2, 3, 4, 5];
```

添加元素：你可以使用 `push()` 方法在数组末尾添加元素，使用 `unshift()` 在数组开头添加元素，或使用 `splice()` 在指定索引处插入元素。

```javascript
// 添加元素
numbers.push(6);
numbers.unshift(0);
numbers.splice(2, 0, 2.5);
```

删除元素：可以使用 `pop()` 删除最后一个元素，使用 `shift()` 删除第一个元素，或使用 `splice()` 删除指定索引处的元素。

```javascript
// 删除元素
numbers.pop();
numbers.shift();
numbers.splice(1, 2);
```

归约：`reduce()` 方法对数组的每个元素应用一个函数，将数组归约为单个值。

```javascript
// 归约
const sum = numbers.reduce((acc, num) => acc + num, 0);
```

更新元素：你可以通过直接为数组中的目标索引赋予新值来更新元素的值。

```javascript
// 更新元素
numbers[2] = 3.3;
```

拼接：可以使用 `concat()` 方法拼接数组，该方法通过合并多个数组创建一个新数组。

```javascript
// 拼接
const moreNumbers = [7, 8, 9];
const combined = numbers.concat(moreNumbers);
```

切片：`slice()` 方法根据起始和结束索引从现有数组中提取一部分，创建一个新数组。

```javascript
// 切片
const sliced = numbers.slice(1, 4);
```

映射：`map()` 方法对数组的每个元素应用给定的函数，并返回一个包含结果的新数组。

```javascript
// 映射
const doubled = numbers.map(num => num * 2);
```

过滤：`filter()` 方法创建一个新数组，其中包含通过给定函数定义的特定条件的元素。

```javascript
// 过滤
const evens = numbers.filter(num => num % 2 === 0);
```

# 104. JavaScript 代理

问题：理解 JavaScript 代理

解决方案：

JavaScript 中的 `Proxy` 对象允许你为现有对象创建自定义包装器，以拦截并重新定义基本操作。它充当代码与原始对象之间的中介，使你能够自定义属性访问、方法调用等。这使你能够实现各种行为，例如数据验证、日志记录，甚至实现懒加载等功能。

以下是一个使用 `Proxy` 自定义属性访问的基本示例：

```javascript
const person = { name: "John Doe" };
const handler = {
  get: function (target, name) {
    return name in target ? target[name] : "Not Found";
  },
};
const proxy = new Proxy(person, handler);
console.log(proxy.name); // John Doe
console.log(proxy.age); // Not Found
```

在此示例中，我们定义了一个 `handler` 对象，其中包含一个 `get` 方法，该方法拦截对 `person` 对象的属性访问。它检查属性是否存在于原始对象中，如果存在则返回其值，否则返回自定义消息。

借助 `Proxy` 对象，你可以实现访问控制、不可变性等高级功能，使其成为 JavaScript 开发人员的强大工具。

# 105. do-while 循环

问题：解释 JavaScript 中 do-while 循环的用途。

解决方案：

JavaScript 中的 do-while 循环用于在某个条件为真时重复执行一段代码块。与 while 循环不同，do-while 循环中的代码块在条件求值之前至少会执行一次。条件在每次迭代结束时进行求值。

以下是 JavaScript 中 do-while 循环的示例：

```javascript
let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);
// 1
// 2
// 3
// 4
// 5
```

# 106. 箭头函数中 `this` 关键字的行为

问题：讨论 JavaScript 中箭头函数内 `this` 关键字行为的复杂性和潜在挑战。

解决方案：JavaScript 中箭头函数内 `this` 关键字的行为可能带来复杂性和挑战，尤其是对于从传统函数过渡到箭头函数的开发人员而言。理解箭头函数中 `this` 的细微差别至关重要，以避免常见陷阱并确保代码按预期运行。

挑战与注意事项：

*   **词法作用域绑定**：箭头函数词法绑定 `this`，这意味着它们从其包含的作用域继承 `this` 值。这对于保持一致的 `this` 上下文可能是有利的，但如果使用不当，可能会导致意外结果。

*   **全局对象 `this`**：在全局级别定义的箭头函数中，`this` 指向全局对象（例如浏览器中的 `window`）。这可能会令人惊讶并导致意外后果。

*   **没有 `arguments` 对象**：箭头函数没有自己的 `arguments` 对象。如果需要访问函数参数，使用箭头函数时可能会遇到困难。

*   **不能用作构造函数**：箭头函数不能与 `new` 关键字一起使用来创建对象实例。这与可以作为构造函数的常规函数不同。

*   **灵活性有限**：箭头函数中 `this` 的固定绑定可能会在需要动态 `this` 绑定的某些场景中限制其灵活性。

最佳实践……

*   **明智地使用箭头函数**：当你希望保留其周围作用域的 `this` 上下文时（例如在回调中或在对象内定义方法时），请使用箭头函数。

*   **注意 `this`**：注意箭头函数的使用位置以及 `this` 如何受到影响。在需要动态 `this` 绑定的情况下，请考虑使用常规函数或方法。

*   **考虑兼容性**：确保你对箭头函数的使用与目标环境支持的 JavaScript 版本一致，因为较旧的环境可能不完全支持它们。

# 107. 什么是隐藏类？

问题：隐藏类是 JavaScript 引擎（如 Chrome 使用的 V8）用于优化 JavaScript 代码执行的内部机制。它们解决的问题是在执行 JavaScript 程序时，需要高效地进行属性访问和方法调用。

解决方案：隐藏类，也称为转换树或映射，是 JavaScript 引擎优化对象布局和属性访问时间的一种方式。其关键思想是为代码执行过程中遇到的每个不同的对象形状（即一组特定的属性及其顺序）创建一个隐藏类。隐藏类允许引擎通过属性在内存中的偏移量快速定位属性，而不是执行昂贵的属性查找。

以下是隐藏类工作原理的简化说明：

对象创建：当创建一个对象时，JavaScript 引擎根据其初始属性和顺序为其分配一个隐藏类。

属性添加：当你向对象添加属性时，引擎会检查新对象形状的隐藏类是否存在。如果存在，则更新隐藏类；否则，创建一个新的隐藏类。

属性访问：在属性访问期间，引擎使用隐藏类来确定属性的内存偏移量，从而使属性访问操作更快。

优化：随着程序的运行，引擎可能会基于可预测的隐藏类转换来优化代码路径，从而实现更高效的属性访问。

以下是一个简单的 JavaScript 示例：

```javascript
class Point {
```




```
constructor(x, y) {

this.x = x;

this.y = y;

}

}

const pointA = new Point(1, 2);

// 隐藏类：Point#1 {x, y}

const pointB = new Point(3, 4);

// 隐藏类：Point#2 {x, y}

pointA.z = 5;

// 隐藏类：Point#3 {x, y, z}
```

# 108\. 使用内联缓存优化属性访问

问题：你希望优化 JavaScript 中属性访问操作的性能，尤其是在循环或关键代码段中多次访问同一对象的同一属性时。

解决方案：要在 JavaScript 中使用内联缓存优化属性访问，请遵循以下步骤：

缓存属性访问信息：首先记录你要访问的对象和属性的信息。这些信息应包括对象的类型和属性名称。

```
const obj = { x: 42 };

const property = "x";

// 属性名称已知
```

缓存属性访问信息：首先记录你要访问的对象和属性的信息。这些信息应包括对象的类型和属性名称。

```
for(let i = 0; i < 1000; i++) {

const value = obj[property];

// 优化的属性访问

}
```

在这个循环中，JavaScript 引擎可以利用缓存的信息快速检索属性的值，而无需重复查找对象的内部结构。

确保一致性：为了实现有效的内联缓存，请确保在要优化属性访问的循环或代码段中，属性名称保持一致。如果属性名称发生变化，JavaScript 引擎可能无法使用缓存的信息。

通过遵循这些步骤，你可以有效地在 JavaScript 中使用内联缓存优化属性访问，尤其是在性能关键的代码段中需要多次访问同一对象的同一属性时。这种优化可以显著提升代码执行速度。

# 109\. 什么是 compose 和 pipe 函数？

问题：Compose 和 pipe 函数用于函数式编程，通过组合多个函数来创建更易维护和阅读的代码。它们解决的问题是如何将一系列函数应用于一个值，并将一个函数的结果作为下一个函数的输入，同时保持代码清晰易懂。

解决方案：

Compose 函数：Compose 是一个高阶函数，它接受多个函数作为参数并返回一个新函数。这个新函数从右到左应用这些函数，将前一个函数的结果作为下一个函数的参数。

```
const compose =

(...fns) =>

(x) =>

fns.reduceRight((v, fn) => fn(v), x);

const addOne = (x) => x + 1;

const double = (x) => x * 2;

const square = (x) => x ** 2;

const composeFn = compose(square, double, addOne);

console.log(composeFn(3)); // 64
```

Pipe 函数：Pipe 与 compose 类似，但它是从左到右应用函数，将前一个函数的结果作为下一个函数的参数。

```
const pipe = (...fns) => (x) => fns.reduce((v, fn) => fn(v), x);

const addOne = (x) => x + 1;

const double = (x) => x * 2;

const square = (x) => x ** 2;

const pipedFn = pipe(addOne, double, square);

console.log(pipedFn(3)); // 64
```

# 110\. 理解 JavaScript 中的“Symbol”数据类型

问题：JavaScript 中的 `Symbol` 数据类型相对独特且不易理解。开发者常常难以掌握其重要性和使用场景。

解决方案：JavaScript 中的 `Symbol` 数据类型是 ECMAScript 6（ES6）引入的一种原始数据类型。与字符串或数字等其他原始数据类型不同，Symbol 是唯一且不可变的。它们通常用作对象属性的键，尤其是在需要创建隐藏或不可枚举属性的场景中。

使用场景：

对象属性键：Symbol 常被用作对象属性的键，用于创建私有或隐藏属性，这些属性无法通过常规的属性枚举访问。

```
const mySymbol = Symbol('description');

const obj = {

[mySymbol]: '这是一个隐藏属性'

};

console.log(obj[mySymbol]);

// 可访问

for(const key in obj) {

console.log(key);

// 不会输出 mySymbol

}

const myIterable = {

[Symbol.iterator]() {

// 自定义迭代器逻辑

}

};
```

防止名称冲突：Symbol 可以帮助避免对象中的命名冲突。如果代码库的两个部分使用相同的 Symbol 作为属性键，它们不会意外地相互干扰。

```
const MODULE_A = Symbol('模块 A');

const MODULE_B = Symbol('模块 B');

const myObject = {

[MODULE_A]: '来自模块 A 的数据',

[MODULE_B]: '来自模块 B 的数据'

};
```

内置 Symbol：JavaScript 有一些内置的 Symbol，如 `Symbol.iterator` 和 `Symbol.toStringTag`，可用于定义对象的自定义行为，使其可迭代或控制其字符串表示。

# 111\. ES6 Map 与 WeakMap

问题：解释 JavaScript 中 ES6 `Map` 和 `WeakMap` 的区别，重点说明当键/值引用的对象被删除时它们的行为。

解决方案：ES6 的 `Map` 和 `WeakMap` 都是用于存储键值对的数据结构，但它们在内存管理方面有所不同，尤其是当键/值引用的对象被删除时。

考虑以下示例代码：

```
var map = new Map();

var weakmap = new WeakMap();

(function () {

var a = {

x: 12,

};

var b = {

y: 12,

};

map.set(a, 1);

weakmap.set(b, 2);

})();
```

`Map`：垃圾回收器不会从 `Map` 中移除指针，也不会从内存中移除 `{x: 12}`。手动编写的 `Map` 对象会保持对键对象的引用，阻止它们被垃圾回收。

`WeakMap`：垃圾回收器会从 `WeakMap` 中移除键 `b` 的指针，同时也会从内存中移除 `{y: 12}`。`WeakMap` 对键对象持有弱引用，允许在没有其他引用指向该对象时将其垃圾回收。

总结：`Map` 对象保持对键的引用，阻止其被垃圾回收；而 `WeakMap` 对象允许键在没有其他引用时被垃圾回收。

# 112\. 揭示模块模式

问题：解释 JavaScript 设计模式中揭示模块模式的概念。

以下是一个示例：

```
var Exposer = (function() {

var privateVariable = 10;

var privateMethod = function() {

console.log('在私有方法内部！');

privateVariable++;

}

var methodToExpose = function() {

console.log('这是我想暴露的方法！');

}

var otherMethodIWantToExpose = function() {

privateMethod();

}

return {

first: methodToExpose,

second: otherMethodIWantToExpose

};

})();

Exposer.first();

// 这是我想暴露的方法！

Exposer.second();

// 在私有方法内部！

Exposer.methodToExpose;

// undefined
```

解决方案：揭示模块模式是模块模式的一种变体，旨在保持封装性的同时，通过对象字面量有选择地暴露变量和方法。其实现方式是创建一个立即执行函数表达式（IIFE），在其中定义私有变量和方法，然后返回一个包含要对外暴露的方法的对象。

# 113\. JavaScript 中的转译

解决方案：转译（Transpiling），即“源码到源码编译”，是将代码从一种编程语言转换为另一种编程语言的过程。在 JavaScript 的上下文中，转译涉及将用较新版本 JavaScript（ES6、ES7 等）编写的代码转换为较旧版本（通常是 ES5），以便兼容更广泛的浏览器。

为什么转译很重要：

*   **浏览器兼容性**：并非所有浏览器都支持最新的 JavaScript 特性。转译器允许开发者使用现代语法编写代码，同时确保与旧版浏览器的兼容性。




*   **采用新特性**：开发者可以使用最新的语言特性编写更简洁、更高效的代码，同时知道转译器会处理兼容性问题。
*   **开发速度**：转译器使开发者能够利用新语言特性，而无需等待浏览器广泛支持。
*   **工具与框架**：许多现代工具和框架依赖转译来提供增强功能和优化。

示例：

```
// ES6 代码
const greet = (name) => `Hello ${name}!`;

// 转译后的 ES5 代码
var greet = function(name) {
  return 'Hello, ' + name + '!';
}
```

注意事项：流行的 JavaScript 转译器包括 Babel 和 TypeScript。

转译器也可用于将其他语言（如 TypeScript 或 CoffeeScript）转译为 JavaScript。

# 114. 按值传递还是按引用传递

问题：解释 JavaScript 是按引用传递还是按值传递的语言，并提供一个示例来说明这一概念。

解决方案：JavaScript 通常被描述为“按值传递”的语言，但对于对象而言，传递的值实际上是一个引用。这可能导致混淆，因为对象的行为看起来像是按引用传递。

考虑以下示例：

```
function changeStuff(a, b, c) {
  a = a * 10;
  b.item = "changed";
  c = { item: "changed" };
}

var num = 10;
var obj1 = { item: "unchanged" };
var obj2 = { item: "unchanged" };

changeStuff(num, obj1, obj2);
console.log(num); // 10
console.log(obj1.item); // changed
console.log(obj2.item); // unchanged
```

在这个示例中，`num` 的行为类似于原始值（按值传递），其值在函数外部保持不变。然而，对于 `obj1` 和 `obj2`，对其属性（`item`）的修改在函数外部仍然有效，看起来像是按引用传递。如果直接修改 `obj2` 的值，修改不会持久化，这突显了 JavaScript 确实是按值传递的。

JavaScript 是按值传递的，但当涉及对象时，传递的值是对该对象的引用。

# 115. 在 JavaScript 中，为什么 `this` 运算符不一致？

问题：JavaScript 中 `this` 运算符的行为可能不一致，导致在不同场景下产生混淆和意外结果。

解决方案：理解 `this` 运算符行为不同的各种上下文至关重要：

*   **原始函数调用**：`this` 指向全局对象或 `undefined`（严格模式）。
*   **方法调用**：`this` 指向调用该方法的对象。
*   **`call` 或 `apply` 调用**：`this` 被显式指定为第一个参数。
*   **事件监听器调用**：`this` 是触发事件的元素。
*   **构造函数调用**：`this` 指向一个新对象，其原型被设置为构造函数的 `prototype`。
*   **由 `bind` 生成的函数**：`this` 是不可变的，被设置为 `bind` 的第一个参数。

在每个上下文中正确管理 `this` 对于避免不一致和意外行为至关重要。

# 116. 什么是节流（throttling）？为什么在 JavaScript 中使用它？

问题：在 JavaScript 中实现节流，以限制函数的执行速率。

解决方案：你可以使用以下 `throttle` 函数在 JavaScript 中实现节流：

```
function throttle(func, delay) {
  let isThrottled = false;
  let lastArgs, lastThis;

  return function() {
    if (!isThrottled) {
      func.apply(this, arguments);
      isThrottled = true;
      lastArgs = arguments;
      lastThis = this;
      setTimeout(() => {
        isThrottled = false;
        if (lastArgs) {
          func.apply(lastThis, lastArgs);
          lastArgs = lastThis = null;
        }
      }, delay);
    }
  };
}

// 示例用法：
function expensiveOperation() {
  console.log("Expensive operation executed.");
}

const throttledOperation = throttle(expensiveOperation, 1000); // 限制为每秒一次

// 调用节流函数
throttledOperation(); // 立即执行
throttledOperation(); // 被忽略（节流中）
setTimeout(() => throttledOperation(), 500); // 被忽略（节流中）
setTimeout(() => throttledOperation(), 1500); // 1 秒后执行
```

# 117. JavaScript 中的记忆化（Memoization）

问题：当处理递归或计算密集型函数（如重复计算）时，性能可能成为关键问题。在这种情况下，优化函数变得至关重要。

解决方案：记忆化是一种高级技术，通过缓存先前调用的结果并在将来再次调用相同参数时重用它们，来提升函数性能。这消除了重新计算相同结果的需要，而重新计算可能耗费大量时间和资源。

示例代码：

```
function memoize(func) {
  const cache = new Map();
  return function (...args) {
    const key = JSON.stringify(args);
    if (cache.has(key)) {
      return cache.get(key);
    }
    const result = func(...args);
    cache.set(key, result);
    return result;
  };
}

function fibonacci(n) {
  if (n <= 1) {
    return n;
  }
  return fibonacci(n - 1) + fibonacci(n - 2);
}

const memoizedFibonacci = memoize(fibonacci);
console.log(memoizedFibonacci(40));
// 计算并缓存结果
console.log(memoizedFibonacci(40));
// 返回缓存结果，无需重新计算
```

# 118. JavaScript 中的事件循环与非阻塞 I/O

问题：JavaScript 是单线程的，不能为了 I/O 操作而阻塞执行，否则会冻结整个程序。然而，它仍然需要高效地处理 I/O 操作而不阻塞。

解决方案：事件循环是 JavaScript 实现非阻塞 I/O 的关键概念。它是一种机制，通过处理事件和回调来执行异步操作。JavaScript 不会等待 I/O 操作完成，而是将其委托给系统，并继续执行其他任务。一旦 I/O 操作完成，关联的回调会被放入消息队列。事件循环不断检查该队列，并在轮到回调时执行它们。

示例代码：

```
function simulateAsyncAPI(text, timeout) {
  setTimeout(() => {
    console.log(text);
  }, timeout);
}

simulateAsyncAPI('A', 1000);
simulateAsyncAPI('B', 500);
simulateAsyncAPI('C', 100);

// 预期输出：
// C
// B
// A
```

在这段代码中，使用 `setTimeout` 模拟了三个异步操作。它们不会阻塞主线程，而是在各自指定的超时时间后独立执行。

解释：事件循环使 JavaScript 能够高效地管理异步操作（如网络请求、文件 I/O 和定时器），而不会阻塞主线程，从而确保应用程序流畅且响应迅速。

# 119. 什么是内联缓存（Inline Caching）？

问题：内联缓存（通常称为“IC”）是 JavaScript 引擎中用于优化对象属性访问和方法调用的一种技术。问题在于，如果没有优化，这些操作可能相对较慢，尤其是在循环中执行或频繁访问时。内联缓存旨在提升这些操作的性能。

解决方案：内联缓存的核心思想是记住对象上先前访问过的属性或方法及其对应的内存位置。当再次访问某个属性或方法时，引擎无需每次都查找对象的结构，而是可以利用这些缓存信息直接访问属性或方法，从而显著提升性能。

以下是内联缓存如何用于属性访问的简化示例：

```
function getProperty(obj, key) {
  // 检查对象是否已被缓存
  if (!obj.__cache__) {
    obj.__cache__ = {};
  }
  // 检查属性是否已被缓存
  if (!(key in obj.__cache__)) {
    // 如果未缓存，执行属性查找
    obj.__cache__[key] = obj[key];
  }
  return obj.__cache__[key];
}

const person = { name: "John", age: 30 };
console.log(getProperty(person, "name")); // 访问 "name" 属性
console.log(getProperty(person, "age")); // 访问 "age" 属性
```





```
console.log(getProperty(person, "name")); // Uses cached "name" property
```

# 120. 浅拷贝与深拷贝

问题：开发者在处理 JavaScript 中的对象和数组时，常常难以理解浅拷贝与深拷贝之间的区别。这种混淆可能导致代码中出现意外行为。

解决方案：在处理 JavaScript 中的对象和数组时，理解浅拷贝与深拷贝之间的差异至关重要：

浅拷贝：对象或数组的浅拷贝会创建一个新的容器（对象或数组），并将原容器中各项的引用复制到新容器中。它不会创建嵌套对象或数组的副本。

浅拷贝速度快且内存效率高，因为它避免了复制复杂的数据结构。

对拷贝中嵌套对象或数组所做的更改会反映到原对象中，反之亦然，因为它们引用的是同一个对象。

可以使用 `Object.assign()`、展开运算符（`...`）或遍历原对象并复制各项等方法创建浅拷贝。

当你希望快速复制容器的结构，而不必担心深层嵌套的对象或数组时，浅拷贝非常适用。例如，在复制 Redux 存储的初始状态时。

```
const shallowCopy = { ...originalObject };
```

深拷贝：对象或数组的深拷贝会创建一个完全独立的副本，包括容器本身以及所有嵌套的对象和数组。对副本的更改不会影响原对象，反之亦然。

深拷贝确保了原对象与副本之间的隔离，在需要修改其中一个而不影响另一个的场景中更为安全。

创建深拷贝可能更复杂、更慢且更耗内存，因为它需要递归地复制所有嵌套的对象和数组。

像 Lodash 这样的库提供了用于深拷贝对象和数组的函数。

当你需要确保原对象与副本完全独立时，深拷贝至关重要。可用于创建对象状态的快照或克隆复杂数据结构等场景。

```
const deepCopy = JSON.parse(JSON.stringify(originalObject));
```

在结束“高级 JavaScript 面试题”这一章之际，请记住，你的 JavaScript 之旅才刚刚开始。这门语言为 Web 开发提供了无限可能。

继续探索，迎接挑战，并与他人分享你的知识。保持与 JavaScript 社区的互动，参加活动，不断学习。

感谢你选择我们的书籍。你对掌握 JavaScript 的投入值得称赞。你的潜力无限。

当你合上这本书时，要知道你正在用每一行代码塑造数字世界。祝你在 JavaScript 的冒险中持续成功并收获满满。

发现其他有用资源，请访问：

[www.hernandoabella.com](http://www.hernandoabella.com)



# JavaScript 框架：从初学者到高级的顶级编程课程。快速高效精通 (2024)

![](img/cover.jpeg)

在书中，你将学习通过图表解释以及实践练习，并获得练习的成功执行和输出。提供带有分步说明的现成解决方案。AMIT K

确认对话框用于请求用户确认某些操作。此对话框非常简单，你无法自定义对话框的图标或标题，只能提供一条请求用户确认的消息。该对话框有两个按钮：确定（OK）和取消（Cancel）。

| ![](img/image_rsrc8PE.jpg) |

要显示确认对话框，你调用 `confirm(message)` 函数，其中 `message` 是一个请求用户确认的消息。如果用户点击“确定”按钮，该函数返回 `true`；否则，如果用户点击“取消”按钮，该函数返回 `false`。

| ![](img/image_rsrc8PF.jpg) |

| ![](img/image_rsrc8PE.jpg) |

| ![](img/image_rsrc8PG.jpg) |

`confirm-example.js`

```html
<!DOCTYPE html>
<html>
<head>
<title>Confirmation Dialog Box</title>
<script type="text/javascript">
function testConfirmDialog() {
  var result = confirm("Do you want to continue?");
  if (result) {
    alert("OK Next lesson!");
  } else {
    alert("Bye!");
  }
}
</script>
</head>
<body>
<h2>Confirmation Dialog Box</h2>
<button onclick="testConfirmDialog()">Click me!</button>
</body>
</html>
```

| ![](img/image_rsrc8PH.jpg) |

# 第 1 章：提示对话框

提示对话框用于用户输入信息。此对话框非常简单，包含一个供用户输入信息的文本字段。对话框有两个按钮：确定（OK）和取消（Cancel）。

要显示提示对话框，你调用 `prompt(message, defaultValue)` 函数，其中 `message` 是给用户的提示。`defaultValue` 是预填充在文本字段中的默认值。

如果用户点击“确定”，函数返回文本字段的内容；否则，如果用户点击“取消”，函数返回 `null`。

`prompt-example.js`

```html
<!DOCTYPE html>
<html>
<head>
<title>Prompt Dialog Box</title>
<script type="text/javascript">
function testPromptDialog() {
  var result = prompt("Enter your age:", "20");
  if (result != null) {
    alert("Your age is " + result);
  }
}
</script>
</head>
<body>
<h2>Prompt Dialog Box</h2>
<button onclick="testPromptDialog()">Click me!</button>
</body>
</html>
```

| ![](img/image_rsrc8PJ.jpg) |

# 第 2 章：JavaScript 变量

## 什么是变量

变量意味着程序用于存储数值的“内存位置”。变量名被称为标识符。

变量名的命名必须遵循某些原则。以下是为变量命名的命名原则：

- 变量名不能与关键字相同
- 变量名可以包含字母或数字，但不能以数字开头
- 变量名不能包含空格或特殊字符，下划线（`_`）和美元符号（`$`）除外

## 声明变量

声明变量是必要的，因为你在使用它之前必须进行声明。

```javascript
// Declare variables:
var a1;
console.log(a1); // undefined
var a2 = 100;
console.log(a2); // 100
var a3, a4;
var a5, a6 = 200;
console.log(a5); // undefined
console.log(a6); // 200
var a7 = 100, a8 = 300;
let b1;
console.log(b1); // undefined
let b2 = "Hello";
console.log(b2); // Hello
const c = 100;
console.log(c); // 100
```

## 块

块意味着位于“大括号” `{}` 中的一组命令。

## let

`let` 关键字用于声明块级作用域变量，这意味着该变量将在程序在该块或内部子块中被实现，但在定义它的块的外部不会被程序实现。

```javascript
if (true) {
  let a = 200;
  console.log(a); // 200
}
// Program will ignore this statement:
console.log(a);
```

如果你使用 `let` 关键字定义了两个同名的变量，其中一个变量在父块中声明，另一个在子块中声明，程序会将它们视为两个不同的变量。

```javascript
let i = 1000;
let j = 2000;
if (true) {
  i = 100; // Assign new value to 'i'
  let j = 200; // A new variable
  console.log("Test1: " + i + " : " + j); // Test1: 100 : 200
}
console.log("Test2: " + i + " : " + j); // Test2: 100 : 2000
```

## var

`var` 关键字用于声明变量，它的作用域比 `let` 变量更广。它在定义它的块内部、子块中被实现，甚至在声明它的块外部也可以被实现。

```javascript
if (true) {
  var a = 200;
  console.log(a); // 200
}
console.log(a); // 200
```

如果你使用 `var` 关键字声明了两个同名的变量，其中一个在父块中声明，另一个在子块中声明，程序认为这两个变量是同一个（内存中的相同位置）。

```javascript
var i = 1000;
var j = 2000;
if (true) {
  i = 100; // Assign new value
  var j = 200; // Assign new value
  console.log("Test1: " + i + " : " + j); // Test1: 100 : 200
}
console.log("Test2: " + i + " : " + j); // Test2: 100 : 200
```

在函数用 `var` 声明的变量只会被程序在该函数内部识别。它在函数外部无法被识别。

```javascript
// A function
var test = function() {
  var a = 200;
  console.log(a); // 200
};
// Call function.
test();
console.log(a); // Not work!!
```

## const

`const` 关键字用于声明常量。在声明常量时，你必须给它赋值。但你不能给这个变量赋值新值。注意：与 `let` 变量一样，`const` 变量具有块级作用域。

```javascript
// Declare a constant with a value
const greeting = "Hello";
// Assign new value to 'greeting'
greeting = "Hi"; // ==> Error!!
// Declare a constant without a value
const i; // ==> Error!!
```

用 `const` 关键字声明的变量在意义上是常量，因为你不能给它赋新值，但它并不是不变的，你仍然可以改变它的属性。

# 第 3 章：位运算

## 位运算

在数字计算机编程中，位运算作用于一个或多个二进制数，或类似于二进制数的字符串。

这是一种简单且快速的操作，由处理器直接支持。通常，位运算比乘法、除法快得多，有时显著快于加法。位运算消耗的能量较少，因为它很少消耗资源。

有 7 种位运算：

| 运算符 | 名称 | 描述 |
| :--- | :--- | :--- |
| `&` | 与 (AND) | 如果两个位都为 1，则返回值为 1，否则返回 0。 |
| `\|` | 或 (OR) | 如果两个位中有一个为 1，则返回值为 1，否则返回 0。 |
| `^` | 异或 (XOR) | 如果两个位不同，则返回值为 1，否则返回 0。 |
| `~` | 非 (NOT) | 反转所有位，0 变为 1，1 变为 0。 |
| `<<` | 零填充左移 | 将所有位向左移动。 |
| `>>` | 有符号右移 | 除第一位外，将所有位向右移动。 |
| `>>>` | 零填充右移 | 将所有位向右移动。 |

### 位与

当对一对位执行位与运算时，如果两个位都为 1，则返回 1，否则返回 0。

### 位或

当对一对位执行位或运算时，如果位中有一个为 1，则返回 1，否则返回 0。

### 位异或

当对一对位执行位异或运算时，如果位不同，则返回 1，否则返回 0。

### 位非

当使用位非运算时，它将反转所有位，1 变为 0，0 变为 1。

## 数字的位运算

不同的语言可以使用多种数据类型来表示数字。

- Java: `byte`, `short`, `int`, `long`, `double`
- C#: `byte`, `sbyte`, `short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`
- JavaScript: `double`

JavaScript 将数字存储为 64 位浮点数。但位运算是在 32 位整数上进行的。Java、C# 等语言的位运算也是在 32 位整数上进行的。

因此，在对数字执行位运算之前，你必须将每个数字转换为 32 位二进制序列。

注意：32 位中，第一位用于确定数字的符号。如果该位为 1，它对应 ( - ) 符号。如果该位为 0，它对应 ( + ) 符号。

| ![](img/image_rsrc8PK.jpg) |

### 位左移

位左移运算符 (`<<`) 可能会改变数字的符号。

| ![](img/image_rsrc8PM.jpg) |

## 位运算右移 [无符号右移]

位右移运算符 (`>>`) 不会改变数字的符号，因为第一位不会移动。

| ![](img/image_rsrc8PN.jpg) |

### 位运算右移 [零填充右移]

位右移运算符 (`>>>`) 可以改变数字的符号。

| ![](img/image_rsrc8PP.jpg) |

## 位运算的用途

位运算直接由计算机处理器支持，其执行速度非常快。下面我列出了一些使用这些计算的示例。

在 `Java`、`C#`、`C/C++` 等语言对字符串（字符）使用位运算。注意：某些语言如 `JavaScript` 不支持对 `String` 类型进行位运算。

### 将大写字母转换为小写：

```text
// 规则: x | ' ' ('A' | ' ') ==> 'a' ('B' | ' ') ==> 'b' ('a' | ' ') => 'a'
```

### 将小写字母转换为大写：

```text
// 规则: x & '_' ('a' & '_') ==> 'A' ('b' & '_') ==> 'B' ('A' & '_') ==> 'A'
```

# 第 4 章：JavaScript 数组

## 什么是数组

数组是内存中存储数据的连续位置集合。每个内存位置被称为一个元素。

| ![](img/image_rsrc8PR.jpg) |

以下是数组的特性：

- 元素的索引从 0 开始 (0, 1, 2,..)，你可以通过索引访问元素。
- 数组也像变量。你必须在使用它之前对其进行声明。
- 你可以更新或编辑数组中元素的值。

### 为什么需要数组

与其声明一个包含 `N` 个元素的数组，你可以声明 `N` 个变量，但它有以下缺点：

- 如果 `N` 是一个很大的数字，手动声明 `N` 个变量是不可行的。
- 当你声明 `N` 个变量时，程序不会为你管理变量的顺序，因为变量没有索引的概念。

## 声明数组

和变量一样，你必须在使用数组之前声明它。

### 语法

```text
// 声明
var myArray;
// 初始化
myArray = [val1, val2, .., valN]
// 或
var myArray = [val1, val2, .., valN]
```

| ![](img/image_rsrc8PS.jpg) |

`array-example1.js`

```javascript
var myArray = [ 4, 8, 13, 6, 55, 41, 42, 99, 1 ];
console.log("Length of myArray: " + myArray.length); // 9 个元素
console.log("Element at index 0: " + myArray[0]); // 4
console.log("Element at index 1: " + myArray[1]); // 8
console.log("Element at index 4: " + myArray[4]); // 55
```

### 你可以给数组元素赋值新值

`array-example2.js`

```javascript
var names = [ "A", "B", 100 ];
console.log("Length of array: " + names.length); // 3 个元素
console.log("Element at index 0: " + names[0]); // A
console.log("Element at index 1: " + names[1]); // B
console.log("Element at index 2: " + names[2]); // 100
// 给索引为 2 的元素赋新值:
names[2] = "D";
console.log("Element at index 2: " + names[2]);
```

### 使用循环，你可以分别访问数组元素：

`array-loop-example.js`

```javascript
var fruits = ["Acerola", "Apple", "Banana", "Breadfruit", "Carambola" ];
for (var index = 0; index < fruits.length; index++) {
    console.log("Index: " + index + " Element value: " + fruits[index])
}
```

### 输出

```text
Index: 0 Element value: Acerola
Index: 1 Element value: Apple
Index: 2 Element value: Banana
Index: 3 Element value: Breadfruit
Index: 4 Element value: Carambola
```

## 数组对象

数组也可以通过 `Array` 类创建：

```javascript
// 创建一个包含 4 个元素的数组
var myArray1 = new Array(4);
// 创建一个包含 3 个元素的数组：
var myArray2 = new Array("Acerola", "Apple", "Banana");
```

### 示例：

`array-object-example.js`

```javascript
// 创建一个包含 4 个元素的数组：
var salaries = new Array(4);
for (var i = 0; i < salaries.length; i++) {
    console.log(salaries[i]); // undefined
}
for (var i = 0; i < salaries.length; i++) {
    // 给元素赋新值:
    salaries[i] = 1000 + 20 * i;
}
console.log(salaries[2]); // 1040.
```

### 输出

```text
undefined
undefined
undefined
undefined
1040
```

## 数组方法

数组是一个对象。它拥有方法。以下是其方法的列表：

- `concat()`
- `every()`
- `some()`
- `filter()`
- `forEach()`
- `map()`
- `indexOf()`
- `join()`
- `lastIndexOf()`
- `pop()`
- `push()`
- `reduce()`
- `reduceRight()`
- `reverse()`
- `shift()`
- `slice()`
- `toSource()`
- `sort()`
- `splice()`
- `toString()`
- `unshift()`

### concat()

`concat()` 方法返回一个新数组，其元素包含参数中数组（或值）中的元素合并后的结果。

```javascript
// 示例:
array.concat(arrayOrValue1, arrayOrValue2, ..., arrayOrValueN);
```

**参数：**

- `arrayOrValueN`: 一个数组或一个值。

`array-concat-example.js`

```javascript
var alpha = ["a", "b", "c"];
var numeric = [1, 2, 3];
var results = alpha.concat(numeric, "!");
console.log(alpha); // ["a", "b", "c"];
console.log(results); // [ 'a', 'b', 'c', 1, 2, 3, '!' ]
```

### every()

如果数组中的所有元素都通过提供的测试函数，该方法返回 `true`。

```javascript
array.every(callback[, thisObject]);
```

**参数：**

- `callback` — 用于测试每个元素的函数。
- `thisObject` — 在执行 `callback` 时用 `this` 使用的对象。

例如，你有一个员工年龄值的数组，让我们使用 `every()` 方法来测试数组中的所有元素是否都在 18-60 岁之间。

`array-every-example.js`

```javascript
// 测试值是否在 18 到 60 之间。
testAge = function(value, index, testArray) {
    return value >= 18 && value <= 60;
}
var ages = [18, 22, 59];
// 或者: var okAll = ages.every(testAge);
var okAll = ages.every(testAge, ages);
console.log("OK ALL? " + okAll);
```

### forEach()

该方法会为数组的每个元素调用函数。

```javascript
array.forEach(callback[, thisObject]);
```

**参数：**

- `callback` — 为每个元素执行操作的函数。
- `thisObject` — 在执行 `callback` 时用 `this` 使用的对象。

`array-forEach-example.js`

```javascript
// 检查值是否在 18 到 60 之间。
// (回调函数)
showTestResult = function(value, index, testArray) {
    if (value >= 18 && value <= 60) {
        console.log("Age " + value + " valid!");
    } else {
        console.log("Sorry, Age " + value + " invalid!");
    }
}
var ages = [5, 6, 18, 22, 59];
// 或者: ages.forEach(showTestResult);
ages.forEach(showTestResult);
```

### 输出

```text
Sorry, Age 5 invalid!
Sorry, Age 6 invalid!
Age 18 valid!
Age 22 valid!
Age 59 valid!
```

# 第 5 章：JavaScript 循环

## 循环概述

语句从上到下顺序执行。但当你想要多次执行一组语句时，可以使用循环。

| ![](img/image_rsrc8PT.jpg) |

## 循环类型：

- `while` 循环
- `for` 循环
- `do .. while` 循环

可以在循环中使用语句：

- `continue`
- `break`

| 控制语句 | 说明 |
| :--- | :--- |
| `break` | 终止循环语句。 |
| `continue` | 跳过循环体的剩余部分并立即重新测试条件。 |

## while 循环

`while` 循环的语法：

```javascript
while (condition) {
  // 在此处执行某些操作
  // ....
}
```

### 示例：

`while-loop-example.js`

```javascript
console.log("While example");
// 声明变量并赋值 2。
let x = 2;
// 条件是 x < 10
// 如果 x < 10 为真则运行
while (x < 10) {
    console.log("Value of x = ", x);
    x = x + 3;
}
// 该语句在 while 块之外。
console.log("Finish");
```

### 输出

```text
While example
Value of x = 2
Value of x = 5
Value of x = 8
Finish
```

## for 循环

标准的 `for` 循环语法如下：

```javascript
for (InitialValues; condition; updateValues) {
  // 语句
}
```

- `InitialValues`: 初始化循环中相关变量的值。
- `condition`: 定义执行命令块的条件。
- `updateValues`: 更新变量的新值。

`for-loop-example.js`

```javascript
console.log("For loop example");
for (let i = 0; i < 10; i = i + 3) {
    console.log("i= " + i);
}
```

### 输出

```text
For loop example
i= 0
i= 3
i= 6
i= 9
```

`for-loop-example2.js`

```javascript
console.log("For loop example");
for (let i = 0, j = 0; i + j < 10; i = i + 1, j = j + 2) {
    console.log("i = " + i + ", j = " + j);
}
```

### 输出

```text
i = 0, j = 0
i = 1, j = 2
i = 2, j = 4
i = 3, j = 6
i = 4, j = 8
```

### for 循环示例

| i = 0, j = 0 | i = 1, j = 2 | i = 2, j = 4 | i = 3, j = 6 |

使用 `for` 循环可以帮助你遍历数组的元素。

`for-loop-example3.js`

```javascript
console.log("For loop example");
// Array
let names = ["Tom", "Jerry", "Donald"];
for (let i = 0; i < names.length; i++) {
    console.log("Name = ", names[i]);
}
console.log("End of example");
```

**输出**

```text
For loop example
Name = Tom
Name = Jerry
Name = Donald
End of example
```

---

### For .. in 循环

`for..in` 循环帮助你遍历对象的属性。

```javascript
for (prop in object) {
  // 执行某些操作
}
```

**示例：**

`for-in-loop-example.js`

```javascript
// 一个对象有 4 个属性 (name, age, gender, greeting)
var myObject = {
  name: "John",
  age: 25,
  gender: "Male",
  greeting: function() {
    return "Hello";
  }
};
for (myProp in myObject) {
    console.log(myProp);
}
```

**输出**

```text
name
age
gender
greeting
```

---

### For .. of 循环

`for..of` 循环帮助你遍历集合，例如 `Map`、`Set`。

**示例：**

`for-of-example.js`

```javascript
// 从数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
for (let fruit of fruits) {
    console.log(fruit);
}
```

**输出**

```text
Apple
Banana
Papaya
```

`for-of-example2.js`

```javascript
// 创建一个 Map 对象。
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
for (let arr of myContacts) {
    console.log(arr);
    console.log(" - Phone: " + arr[0]);
    console.log(" - Name: " + arr[1]);
}
```

**输出**

```text
[ '0100-1111', 'Tom' ]
- Phone: 0100-1111
- Name: Tom
[ '0100-5555', 'Jerry' ]
- Phone: 0100-5555
- Name: Jerry
[ '0100-2222', 'Donald' ]
- Phone: 0100-2222
- Name: Donald
```

---

### do...while 循环

`do-while` 循环用于多次执行一段程序代码。`do-while` 的特点是语句块至少会被执行一次。在每次迭代之后，程序将检查条件，如果条件仍然正确，将再次执行语句块。

```javascript
do {
  // 执行某些操作
} while (expression);
```

**示例：**

`do-while-loop-example.js`

```javascript
let value = 3;
do {
    console.log("Value = " + value);
    value = value + 3;
} while (value < 10);
```

**输出**

```text
Value = 3
Value = 6
Value = 9
```

---

### 在循环中使用 break 语句

`break` 是一个可以位于循环中的语句。该语句会无条件地结束循环。

`loop-break-example.js`

```javascript
console.log("Break example");
// 声明一个变量并赋值为 2。
let x = 2;
while (x < 15) {
    console.log("----------------------");
    console.log("x = ", x);
    // 如果 x = 5，则退出循环。
    if (x == 5) {
        break;
    }
    // 将 x 的值加 1
    x = x + 1;
    console.log("x after + 1 = ", x);
}
console.log("End of example");
```

**输出**

```text
Break example
----------------------
x = 2
x after + 1 = 3
----------------------
x = 3
x after + 1 = 4
----------------------
x = 4
x after + 1 = 5
----------------------
x = 5
End of example
```

---

### 在循环中使用 continue 语句

`continue` 是一个可以位于循环中的语句。当遇到 `continue` 语句时，程序将忽略块中 `continue` 之后的命令行，并开始一个新的循环。

`loop-continue-example.js`

```javascript
console.log("Continue example");
// 声明一个变量并赋值为 2
let x = 2;
while (x < 7) {
    console.log("----------------------");
    console.log("x = ", x);
    // % 用于计算余数
    // 如果 x 是偶数，则忽略 continue 下的命令行
    // 并开始新的迭代。
    if (x % 2 == 0) {
        // 将 x 加 1。
        x = x + 1;
        continue;
    } else {
        // 将 x 加 1。
        x = x + 1;
        console.log("x after + 1 =", x);
    }
}
console.log("End of example");
```

**输出**

```text
Continue example
----------------------
x = 2
----------------------
x = 3
x after + 1 = 4
----------------------
x = 4
----------------------
x = 5
x after + 1 = 6
----------------------
x = 6
End of example
```

---

### 标签循环

允许你给循环打上标签。这就像是你给循环起了一个名字，当你在程序中使用多个嵌套循环时非常有用。

你可以使用 `break labelX;` 来跳出带有 `labelX` 的循环。

你可以使用 `continue labelX;` 来继续带有 `labelX` 的循环。

**语法：**

```javascript
// 带有标签 label1 的 for 循环:
label1: for (...) {}

// 带有标签 label2 的 while 循环:
label2: while (...) {}

// 带有标签 label3 的 do-while 循环:
label3: do {} while (...);
```

**使用嵌套循环、标签以及标签 break 语句的示例.**

`labelled-loop-break-example.js`

```javascript
console.log("Labelled Loop Break example");
let i = 0;
label1: while (i < 5) {
    console.log("----------------------\n");
    console.log("i = " + i);
    i++;
    label2: for (let j = 0; j < 3; j++) {
        console.log("  --> " + j);
        if (j > 0) {
            // 跳出带有 label1 的循环。
            break label1;
        }
    }
}
console.log("Done!");
```

**输出**

```text
Labelled Loop Break example
----------------------
i = 0
  --> 0
  --> 1
Done!
```

**使用嵌套标签循环和标签 continue 语句的示例。**

`labelled-loop-continue-example.js`

```javascript
let i = 0;
label1: while (i < 5) {
    console.log("i: " + i);
    i++;
    label2: for (let j = 0; j < 3; j++) {
        console.log("  --> " + j);
        if (j > 0) {
            // 继续带有 label2 的循环。
            continue label2;
        }
    }
}
```

---

# 第 6 章：JavaScript 函数

## 函数概述

函数是一段可重用的代码块，用于执行特定任务。

## 函数声明

```javascript
function functionName(parameters) {
  // 函数体
}
```

## 函数表达式

```javascript
var functionName = function(parameters) {
  // 函数体
};
```

## 箭头函数

```javascript
const functionName = (parameters) => {
  // 函数体
};
```

## 参数与参数

### 默认参数

```javascript
function greet(name = "Guest") {
  console.log("Hello " + name);
}
```

### 剩余参数

```javascript
function sum(...numbers) {
  return numbers.reduce((total, n) => total + n, 0);
}
```

## 匿名函数

没有名字的函数被称为匿名函数。匿名函数是在程序运行时动态创建的。它和普通函数一样具有参数和返回值。

你也可以声明一个值为匿名函数的变量。这种表达式被称为 `函数表达式`。

```javascript
var myVar = function(parameters) {
  // ...
};
```

示例：

`anonymous-function-example.js`

```javascript
// Function expression
var f = function(name) {
  return "Hello " + name;
}
// 调用它。
var value = f("Tom");
console.log(value); // Hello Tom.
```

例如，创建一个匿名函数并立即调用它。在这种情况下，该匿名函数仅被创建了一次。

`anonymous-function-example2.js`

```javascript
// 创建匿名函数并立即调用
(function() {
  var now = new Date();
  console.log("Now is " + now);
})();

// 创建匿名函数并立即调用
(function(name) {
  console.log("Hello " + name);
})("Tom");
```

**Output**

```text
Now is Mon Nov 05 2023 00:44:47
Hello Tom
```

## 函数构造函数

我们有一个 `Function` 类，因此你可以通过该类的构造函数来创建一个函数。

```javascript
var variableName = new Function(paramName1, paramName2, ..., paramNameN, "Function Body");
```

例如：

`function-constructor-example.js`

```javascript
var myMultiple = new Function("x", "y", "return x * y");
console.log(myMultiple(3, 4)); // 12
function showTotal() {
  let quantity = 4;
  let price = 5;
  console.log("Total: " + myMultiple(quantity, price));
}
showTotal();
```

**Output**

```text
12
Total: 20
```

## 生成器函数

为了声明一个 `生成器函数`，我们使用 `function*` 关键字。

```javascript
function* functionName(param1, param2, ..., paramN) {
  // Statements
}
```

基本上，`生成器函数`意味着能够暂停执行并在随时继续运行的函数。`生成器函数` 以隐式方式返回一个 `Iterator`（迭代器对象）。在函数内部，你只需要定义该迭代器中各个元素的值即可。

`generator-function-example.js`

```javascript
function* season() {
  yield "Spring";
  yield "Summer";
  yield "Autumn";
  yield "Winter";
}
// 此方法返回一个 Iterator。
var seasonIterator = season();
let value1 = seasonIterator.next().value;
console.log(value1); // Spring
let value2 = seasonIterator.next().value;
console.log(value2); // Summer
let value3 = seasonIterator.next().value;
console.log(value3); // Autumn
let value4 = seasonIterator.next().value;
console.log(value4); // Winter
```

更短的示例：

```javascript
function* season() {
  yield "Spring";
  yield "Summer";
  yield "Autumn";
  yield "Winter";
}
// 此方法返回一个 Iterator。
var seasonIterator = season();
let e;
while (!(e = seasonIterator.next()).done) {
  console.log(e.value);
}
```

当普通函数被调用时，它将执行到返回值或函数结束为止。在此期间，`调用者函数` 无法控制 `被调用函数` 的执行。

如果 `被调用函数` 是一个 `生成器函数`，则 `调用者函数` 就可以控制 `被调用函数` 的执行。以下是这样的示例：

`generator-function-example3.js`

```javascript
function* season() {
  console.log("Do something in Spring");
  yield "Spring";
  // Spring 在此处停止！
  console.log("Do something in Summer");
  yield "Summer";
  // Summer 在此处停止！
  console.log("Do something in Autumn");
  yield "Autumn";
  // Autumn 在此处停止！
  console.log("Do something in Winter");
  yield "Winter";
  // Winter 在此处停止！
}
// 此方法返回一个 Iterator。
var seasonIterator = season();
let e;
while (!(e = seasonIterator.next()).done) {
  console.log(e.value);
  if (e.value === "Autumn") {
    console.log("OK Stop after Autumn");
    break;
  }
}
```

**Output**

```text
Do something in Spring
Spring
Do something in Summer
Summer
Do something in Autumn
Autumn
OK Stop after Autumn
```

# 第 7 章：JavaScript Number

### ECMAScript Number

在 `ECMAScript` 中，`Number` 数据类型表示数字，它可以是 `整数`，也可以是 `浮点数`。

基于内存管理方式，`Number` 分为两类：`Number 对象` 和 `Number 原始类型`。

#### Number 原始类型

通常，创建一个数字，你应该使用原始类型语法：

```javascript
// 原始类型语法：
var myNumber1 = 100;
var myNumber2 = 55.1;
```

`Number` 原始类型存储在公共池中，这意味着当你声明两个或多个具有相同值的 `Number` 原始类型时，它们将指向公共池中同一个内存位置。

`===` 运算符用于检查两个变量是否指向内存中的同一个地址。

![](img/image_rsrc8PY.jpg)

`number-primitive-example1.js`

```javascript
let a = 100;
let b = 150.1;
let c = 150.1;
// a, b: 相同地址？
console.log(a === b); // false
// b, c: 相同地址？
console.log(b === c); // true
```

你也可以通过使用 `Number(value)` 函数来创建一个数字。你收到的结果是一个 `Number` 原始类型：

`number-primitive-example2.js`

```javascript
let a = 100;
let b = 150.1;
// 使用 Number() 函数
let c = Number(150.1);
// a, b: 相同地址？
console.log(a === b); // false
// b, c: 相同地址？
console.log(b === c); // true
```

#### Number 对象

你可以通过 `Number` 类的构造函数来创建一个数字。在这种情况下，你将得到一个 `Number 对象`。

```javascript
// 语法：
var aNumber = new Number(number);
// 示例：
var myNumber1 = new Number(100);
var myNumber2 = new Number(150.1);
```

`new` 运算符始终会在堆内存上创建一个新实体。

![](img/image_rsrc8PZ.jpg)

当将变量 `aa` 的新值赋值给变量 `bb` 时。变量 `bb` 将指向变量 `aa` 所指向的内存地址。在这种情况下，内存中不会创建新实体。

![](img/image_rsrc8R0.jpg)

# 第 8 章：JavaScript Boolean

### ECMAScript Boolean

`Boolean` 是 `ECMAScript` 中简单的数据类型。它只有两个原始值：`true` 和 `false`。

#### Boolean 原始类型

以下是原始语法，它是你创建一个 `Boolean` 类型变量最简单的方法：

`boolean-primitive-example.js`

```javascript
let a = true;
let b = false;
console.log(a); // true
console.log(b); // false
```

`Boolean` 公共池是一个池。它只有两个值：`true`、`false`。当你根据原始语法创建变量时，它将指向池中 `true` 或 `false` 的地址。

`===` 运算符用于比较两个变量指向的地址。

![](img/image_rsrc8R1.jpg)

#### Boolean 对象

你也可以通过 `Boolean` 类的构造函数创建一个 `Boolean 对象`。本质上，你创建一个封装了原始值（`true` 或 `false`）的对象。

```javascript
var myObj = new Boolean(value);
```

**参数：**

- `value`: 如果此参数的值为 `false`、`0`、`""`、`null`、`undefined`、`NaN`、`Number.Infinite`，它将创建一个 `Boolean {false}` 对象。在其他情况下，它将创建 `Boolean {true}` 对象。

```javascript
console.log(new Boolean(false));            // [Boolean: false]
console.log(new Boolean(""));               // [Boolean: false]
console.log(new Boolean(null));             // [Boolean: false]
console.log(new Boolean());                 // [Boolean: false]
console.log(new Boolean(undefined));        // [Boolean: false]
console.log(new Boolean(0));                // [Boolean: false]
console.log(new Boolean(NaN));              // [Boolean: false]
console.log(new Boolean(Number.Infinite));  // [Boolean: false]
console.log(new Boolean(-Number.Infinite)); // [Boolean: false]
console.log(" ------------------- ");
console.log(new Boolean("0"));              // [Boolean: true]
console.log(new Boolean("false"));          // [Boolean: true]
console.log(new Boolean(1));                // [Boolean: true]
console.log(new Boolean(100));              // [Boolean: true]
console.log(new Boolean({}));               // [Boolean: true]
```

每当你使用 `new` 运算符时，堆内存中都会创建一个新对象。因此，通过 `new` 运算符创建 `Boolean` 对象会消耗更多的存储空间。

当你将变量 `aa` 的新值赋值给变量 `bb` 时，变量 `bb` 将指向变量 `aa` 所指向的内存地址。在这种情况下，内存中不会创建任何实体。

![](img/image_rsrc8R2.jpg)

![](img/image_rsrc8R3.jpg)

# 第 9 章：JavaScript 字符串

## ECMAScript 字符串

在 ECMAScript 中，`String` 是一种特殊的数据类型，因为它在程序中被频繁使用，因此它需要具备性能和灵活性。这就是为什么 `String` 既是对象又是原始类型。

### 字符串字面量

你可以创建一个字符串字面量。字符串字面量存储在栈中，需要的存储空间更小，操作起来也更便宜。

```javascript
let aStringLiteral = "Hello World";
```

字符串字面量包含在公共池中。当你声明两个内容相同的 `String Literal` 变量时，它们将指向存储在池中的同一个地址。

![](img/image_rsrc8R4.jpg)

`string-literal-example.js`

```javascript
let a = "Tom";
let b = "Jerry";
let c = "Jerry";
console.log(a); // Tom
console.log(b); // Jerry
console.log(c); // Jerry
// a, b: 相同的地址？
console.log(a === b); // false
// b, c: 相同的地址？
console.log(b === c); // true
```

### 字符串对象

你可以通过 `String` 类的构造函数创建字符串。在这种情况下，你会得到一个 `String` 对象。

```javascript
let myStringObj = new String(value);
```

**参数：**

- `value`: 要转换为字符串的值

`string-object-example.js`

```javascript
let a = new String("Hello World");
console.log(a); // [String: 'Hello World']
let b = new String(true);
console.log(b); // [String: 'true']
let c = new String(100.20);
console.log(c); // [String: '100.2']
```

`new` 运算符始终会在堆内存上创建一个新实体，这解释了为什么使用 `String` 对象需要花费更多的开销。

![](img/image_rsrc8R6.jpg)

### 字符串是不可变的

在 JavaScript 中，`String` 数据类型是不可变的，这意味着对字符串执行的任何操作（如字符串拼接、字符串切割）都会在内存中创建一个新字符串，或者返回另一个字符串。

![](img/image_rsrc8R7.jpg)

`concat(string)` 方法用于将字符串拼接到当前字符串中。但实际上，当前字符串并没有改变，而是创建了一个新字符串（拼接的结果）。下图说明了这种行为：

![](img/image_rsrc8R8.jpg)

`concat-example2.js`

```javascript
let a = "Hello";
let b = "World";
let c = a.concat(b);
console.log(c); // HelloWorld
console.log(a); // Hello
console.log(a === c); // false
```

### 字符串的属性

- `constructor`
- `length`: `length` 属性返回字符串中字符的数量。

`length-example.js`

```javascript
let s1 = "Tom";
console.log(s1);
console.log("Length " + s1.length); // 3
let s2 = "Tom Jerry";
console.log(s2); // Tom Jerry
console.log("Length " + s2.length); // 9
```

### 字符串的方法

- `charAt(index)`: 返回指定索引处的字符。

![](img/image_rsrc8R9.jpg)

`charAt-example.js`

```javascript
let str = "This is a String";
console.log("str.charAt(0) is:" + str.charAt(0)); // T
console.log("str.charAt(1) is:" + str.charAt(1)); // h
console.log("str.charAt(2) is:" + str.charAt(2)); // i
console.log("str.charAt(3) is:" + str.charAt(3)); // s
console.log("str.charAt(4) is:" + str.charAt(4)); //  
console.log("str.charAt(5) is:" + str.charAt(5)); // i
```

- `charCodeAt(index)`: 返回指定索引处字符的 Unicode 值。

![](img/image_rsrc8RA.jpg)

`charCodeAt-example.js`

```javascript
let str = "This is a String";
console.log("str.charCodeAt(0) is:" + str.charCodeAt(0)); // 84
console.log("str.charCodeAt(1) is:" + str.charCodeAt(1)); // 104
console.log("str.charCodeAt(2) is:" + str.charCodeAt(2)); // 105
console.log("str.charCodeAt(3) is:" + str.charCodeAt(3)); // 115
console.log("str.charCodeAt(4) is:" + str.charCodeAt(4)); // 32
console.log("str.charCodeAt(5) is:" + str.charCodeAt(5)); // 105
```

- `concat(string2[, string3[, ..., stringN]])`
- `indexOf(searchValue[, fromIndex])`: 返回指定文本首次出现处的索引，从 `fromIndex` 向后搜索。

![](img/image_rsrc8RB.jpg)

`indexOf-example.js`

```javascript
let str = "This is a String";
let idx = str.indexOf("is", 3);
console.log(idx); // 5
let idx2 = str.indexOf("is");
console.log(idx2); // 2
```

- `lastIndexOf(searchValue[, toIndex])`: 返回指定文本最后一次出现处的索引，从后向前搜索。

![](img/image_rsrc8RC.jpg)

`lastIndexOf-example.js`

```javascript
let str = "This is a String";
let idx = str.lastIndexOf("is", 10);
console.log(idx); // 5
let idx2 = str.lastIndexOf("is", 5);
console.log(idx2); // 5
let idx3 = str.lastIndexOf("is", 4);
console.log(idx3); // 4
```

- `slice(beginIndex [, endIndex])`: 该方法返回由两个位置（如 `beginIndex` 和 `endIndex`）确定的子字符串。如果 `beginIndex` 位置位于右侧而 `endIndex` 位于左侧，则返回的字符串始终为空。

![](img/image_rsrc8RD.jpg)

`slice-example.js`

```javascript
var str = "This is a String";
var result = str.slice(3, -2);
console.log(result); // s a Str
var result2 = str.slice(3);
console.log(result2); // is a String
// IMPORTANT!!
var result3 = str.slice(5, 1); // Empty String
console.log(result3);
// IMPORTANT!!
var result4 = str.slice(5, -13); // Empty String
console.log(result4);
```

- `substr(start[, length])`: 从 `start` 开始计数 `length` 个字符的子字符串。

![](img/image_rsrc8RE.jpg)

`substr-example.js`

```javascript
var str = "This is a String";
var result = str.substr(3, 8);
console.log(result); // is a S
var result2 = str.substr(3);
console.log(result2); // is a String
```

- `substring(beginIndex [, endIndex])`: 该方法返回由两个位置（如 `beginIndex` 和 `endIndex`）定义的子字符串。注意：`substring(a, b)` 和 `substring(b, a)` 返回相同的结果。

![](img/image_rsrc8RF.jpg)

`substring-example.js`

```javascript
var str = "This is a String";
var result = str.substring(3, -2); // 负数会被处理为 0
console.log(result); // s a Str
var result2 = str.substring(3);
console.log(result2); // is a String
// IMPORTANT
// result3 等于 result4:
var result3 = str.substring(4, 1);
var result4 = str.substring(1, 4);
console.log(result3); // his
console.log(result4); // his
```

# 第 10 章：JavaScript if else 语句

## if 语句

`if(condition)` 语句评估条件以决定是否执行其块。

以下是 `if` 语句的结构：

```javascript
if (condition) {
  // 在这里操作！
}
```

`condition` 可以是任何值、类型或表达式。ECMAScript 使用 `Boolean(condition)` 函数进行评估。该函数返回 true 或 false。

下图说明如何评估 ECMAScript 的条件：

![](img/image_rsrc8RG.jpg)

`simple-if-example.js`

```javascript
if (true) { // Work
  console.log("Test 1");
}
if (false) { // Not work!
  console.log("Test 2");
}
```

**输出**

```text
Test 1
```

`if-example.js`

```javascript
if (true) { // Work
  console.log("if(true)");
}
if (false) { // Not work!
  console.log("if(false)");
}
if ('true') { // Work
  console.log("if('true')");
}
if ('false') { // Work (non-empty string is truthy)
  console.log("if('false')");
}
var obj = new Object();
if (obj) { // Work
  console.log("if(obj)");
}
if ('') { // Not work!
  console.log("if('')");
}
if (undefined) { // Not work!
  console.log("if(undefined)");
}
if (0) { // Not work!
  console.log("if(0)");
}
```

**输出**

```text
if(true)
if('true')
if('false')
if(obj)
```

`if-example2.js`

```javascript
var number0 = 0;
if (number0) { // Not work!
  console.log("number 0 (primitive)");
}
if (false) { // Not work!
  console.log("boolean false (primitive)");
}
// A not null Object
var myObj = {};
if (myObj) { // Work!
  console.log("A not null Object");
}
// A not null Object
var numberObject = new Number(0);
if (numberObject) { // Work!
  console.log("A not null Object (Number)");
}
// A not null Object
var booleanObject = new Boolean(false);
if (booleanObject) { // Work!
  console.log("A not null Object (Boolean)");
}
```

**输出**

```text
A not null Object
A not null Object (Number)
A not null Object (Boolean)
```

`if-example3.js`

```javascript
// 声明一个变量，代表你的年龄
let age = 30;
console.log("Your age: " + age);
// 要测试的条件是 'age > 20'
if (age > 20) {
  console.log("Okey!");
  console.log("Age is greater than 20");
}
// 'if' 块之后的代码。
console.log("Done!");
```

**输出**

```text
Your age: 30
Okey!
Age is greater than 20
Done!
```

## if - else 语句

`if-else` 命令也用于检查条件。它使用 `Boolean(condition)` 函数来评估条件。如果评估结果为真，则将执行 `if` 块。相反，将执行 `else` 块。

```javascript
if (condition) {
  // 在此处执行某些操作
} else {
  // 在此处执行某些操作
}
```

![](img/image_rsrc8RH.jpg)

**示例：**

`if-else-example.js`

```javascript
// 声明一个变量，代表你的年龄
let age = 15;
console.log("Your age: " + age);
// 要测试的条件是 'age > 18'
if (age >= 18) {
  console.log("Okey!");
  console.log("You are accepted!");
} else {
  console.log("Sorry!");
  console.log("Age is less than 18");
}
// 'if' 块和 'else' 块之后的代码。
console.log("Done!");
```

**输出**

```text
Your age: 15
Sorry!
Age is less than 18
Done!
```

## if - else if - else 语句

`if - else if - else` 语句的结构如下：

```javascript
if (condition 1) {
  // 在此处执行某些操作
} else if (condition 2) {
  // 在此处执行某些操作
} else if (condition 3) {
  // 在此处执行某些操作
} else {
  // 在此处执行某些操作
}
```

![](img/image_rsrc8RJ.jpg)

`if-elseif-else-example.js`

```javascript
// 声明一个变量
// 代表你的测试分数
let score = 70;
console.log("Your score = " + score);
// 如果分数小于 50
if (score < 50) {
  console.log("You are not pass");
}
// 如果分数大于或等于 50 且小于 80.
else if (score >= 50 && score < 80) {
  console.log("You are pass");
}
// 剩余情况（即大于或等于 80）
else {
  console.log("You are pass, good student!");
}
```

**输出**

```text
Your score = 70
You are pass
```

## 涉及条件表达式的运算符

这是一列在条件表达式中常用的运算符。

- `>` 大于
- `<` 小于
- `>=` 大于等于
- `<=` 小于等于
- `&&` 与 (AND)
- `||` 或 (OR)
- `==` 等于
- `!=` 不等于
- `!` 非

**示例：**

`if-elseif-else-example2.js`

```javascript
// 声明一个变量，代表你的年龄
let age = 20;
// 测试 age 是否小于或等于 17
if (age <= 17) {
  console.log("You are 17 or younger");
}
// 测试 age 等于 18
else if (age == 18) {
  console.log("You are 18 year old");
}
// 测试 age 是否大于 18 且小于 40
else if (age > 18 && age < 40) {
  console.log("You are between 19 and 39");
}
// 剩余情况（大于或等于 40）
else {
  // 嵌套的 if 语句
  // 测试 age 不等于 50.
  if (age != 50) {
    console.log("You are not 50 year old");
    // 否定语句
    if (!(age == 50)) {
      console.log("You are not 50 year old");
    }
  }
  // 如果 age 等于 60 或 70
  if (age == 60 || age == 70) {
    console.log("You are 60 or 70 year old");
  }
}
```

**输出**

```text
You are between 19 and 39
```

# 第 11 章：JavaScript Switch 语句

## switch 语句的结构

### 语法

```javascript
// variable_to_test: 一个待测试的变量
switch (variable_to_test) {
  case value1:
    // 在此处执行某些操作 ...
    break;
  case value2:
    // 在此处执行某些操作 ...
    break;
  default:
    // 在此处执行某些操作...
}
```

`switch` 语句的特性：

`switch` 将检查变量的值，并从上到下将变量与每个不同的值进行比较。每个要比较的值被称为 `case`。当某个 `case` 为真时，将执行该 case 的语句块。

![](img/image_rsrc8RK.jpg)

如果所有 cases 都为假，将执行 `default` 语句块。注意：在 `switch` 语句的结构中，可能也可能没有 `default` 语句块。

![](img/image_rsrc8RM.jpg)

当找到 true case 时，将执行该 case 的语句块。如果此块中没有满足 `break` 语句，程序将继续执行下方的块，直到遇到 `break` 语句或没有语句块需要执行。

`break` 语句使程序退出 `switch`。

![](img/image_rsrc8RN.jpg)

注意 `case` 语句是一个特定的值，你不能进行以下操作：

```javascript
// 这是不允许的 !!
case (age < 18):
// case 仅接受特定值，例如:
case 18:
  // 在此处执行某些操作 ..
  break;
```

### switch 示例

`switch-example.js`

```javascript
// 声明一个变量 age
let age = 20;
// 检查年龄的值
switch (age) {
  // Case age = 18
  case 18:
    console.log("You are 18 year old");
    break;
  // Case age = 20
  case 20:
    console.log("You are 20 year old");
    break;
  // 剩余情况
  default:
    console.log("You are not 18, 20 year old");
}
```

**输出**

```text
You are 20 year old
```

### switch 中的 break 语句

`break` 意味着一种出现在 `case` 块或 `switch` 的 `default` 块中的语句。当遇到 `break` 语句时，程序将退出 `switch`。

![](img/image_rsrc8RP.jpg)

当程序遇到 `switch` 语句时，它将从上到下检查 cases。当找到 true case 时，将执行该 case 的语句块。

**示例：**

`switch-example2.js`

```javascript
// 声明一个变量 age
let age = 30;
// 检查年龄的值
switch (age) {
  // Case age = 18
  case 18:
    console.log("You are 18 year old");
    break;
  // Case age = 30
  case 30:
    console.log("You are 30 year old");
    break;
  // 剩余情况
  default:
    console.log("Other age");
}
```

**输出**

```text
You are 30 year old
```

# 第 12 章：JavaScript 错误处理

## 什么是错误

首先，让我们来看一个示例，其中我调用了一个对象的方法，但这个对象实际上没有这个方法，结果发生了错误。

`hello-error-example.js`

```javascript
console.log("Three");
let myObj = {};
console.log("Two");
console.log("One");
// 对象 myObj 没有 showMe() 方法
// 但我们调用了 showMe().
// 在此处发生错误。
myObj.showMe(); // ==> 错误！！ 以及后续代码将不会执行。
console.log("Let's go!");
```

请通过下面的插图查看程序的流程。

![](img/image_rsrc8RR.jpg)

- 程序在步骤 (1), (2), (3), (4) 中完全正常运行
- 在步骤 (5) 中，当你尝试调用对象方法而该对象没有该方法时，发生了错误。
- 步骤 (6) 中的代码将不会执行。

程序运行过程中可能会发生错误。这可能是一个意外之外的错误。使用 `try-catch` 可以帮助你在错误发生时捕获并处理它们。

回到上面的示例，我们添加 `try-catch` 来捕获并处理错误。

`hello-catch-example.js`

```javascript
console.log("Three");
let myObj = {};
console.log("Two");
console.log("One");
try {
  // 对象 myObj 没有 showMe() 方法。
  // 但我们调用了 showMe()。
  // 这里发生了错误。
  myObj.showMe(); // ==> Error!
  // 这段代码将被忽略
  console.log("!!!");
} catch (e) {
  console.log("Catched error: " + e);
  console.log("OK continue...");
}
console.log("Let's go!");
```

运行该示例的结果如下：

**Output**

```text
Three
Two
One
Catched error: TypeError: myObj.showMe is not a function
OK continue...
Let's go!
```

下面的插图解释了程序的流程：

![](img/image_rsrc8RS.jpg)

- 步骤 (1)-(4) 是完全正常的。
- 在步骤 (5) 发生异常，此时你尝试调用一个对象的方法，而该对象并没有该方法。
- 程序立即跳转并执行 `catch` 块中的命令。步骤 (6) 被忽略了。
- 步骤 (7)、(8) 将执行。
- 步骤 (9) 将执行。

## try-catch-finally

我们已经习惯了通过 `try-catch` 块来捕获错误。`try-catch-finally` 用于完整处理错误。无论 `try` 块中是否发生错误，`finally` 块始终会被执行。

```javascript
try {
  // 在此处做一些操作
} catch (e) {
  // 在此处做一些操作
} finally {
  // finally 块始终会被执行
  // 在此处做一些操作
}
```

示例：

`try-catch-finally-example.js`



```javascript
function getGreeting(language) {
  try {
    console.log("Code in try block (*)");
    // 调用对象 'language' 的 greeting() 方法
    // 如果此对象没有 greeting() 方法，此处可能会抛出异常。
    let v = language.greeting();
    console.log("Code in try block (**)");
    return v;
  } catch (e) {
    console.log("Code in catch block. Something Error: " + e);
  } finally {
    // finally 块始终会被执行。
    console.log("Code in finally block");
  }
  return " !! ";
}
// ----------------------- 测试 -------------------------------------
// 测试 1:
console.log("----- Call getGreeting(null) -----");
let v1 = getGreeting(null);
console.log("Greeting: " + v1);
  // 测试 2:
console.log("------ Call getGreeting(language) ------");
let language = new Object();
language.greeting = function() {
  return "Hello Everybody"
}
let v2 = getGreeting(language);
console.log("Greeting: " + v2);
```

运行示例：

**Output**

```
----- Call getGreeting(null) -----Code in try block (*)Code in catch block. Something Error: TypeError: Cannot read property 'greeting' of nullCode in finally blockGreeting: !!----- Call getGreeting(language) -----Code in try block (*)Code in try block (**)Code in finally blockGreeting: Hello Everybody
```

下面的插图展示了当 `try` 块中发生错误时的程序流程，`finally` 块始终会被执行。

![](img/image_rsrc8RT.jpg)

下面的图显示了当 `try` 块中没有发生错误时的程序流程。在这种情况下，`finally` 块会在 `try` 块的 `return` 命令执行之前立即执行。

![](img/image_rsrc8RU.jpg)

### 4. 内置错误

`ECMAScript` 提供了几个内置类来表示错误。以下是它们的层级结构。

![](img/image_rsrc8RV.jpg)

#### RangeError

如果你使用了允许范围之外的数字，会抛出 `RangeError`。

`error-RangeError-example.js`

```javascript
let num = 1;
try {
  // 数字不能有 500 位有效数字
  num.toPrecision(500); // ==> RangeError!!
} catch(err) {
  console.log(err.name);
  console.log(err);
}
```

#### ReferenceError

如果你使用了未声明的变量，会抛出 `ReferenceError`：

`error-ReferenceError-example.js`

```javascript
var x;
try {
  x = y + 1;   // 无法引用 y（使用）
} catch(err) {
  console.log("Error Name: "+ err.name);
  console.log(err);
}
```

#### SyntaxError

如果你尝试评估带有语法错误的代码，会抛出 `SyntaxError`。

`error-SyntaxError-example.js`

```javascript
try {
  let x;
  eval(" x  = 'Hello  ");  // 缺少 ' 会产生错误
  try {
    let x;
    eval(" x  = 'Hello  ");  // 缺少 ' 会产生错误
  } catch(err) {
    console.log("Error Name: " + err.name);
    console.log(err);
  }
} catch(err) {
  console.log("Error Name: " + err.name);
  console.log(err);
}
```

#### TypeError

如果你使用了与预期类型不符的值，会抛出 `TypeError`。例如，当你调用一个对象的方法而该对象没有该方法时，就会发生错误。

`error-TypeError-example.js`

```javascript
var num = 1;
try {
  num.toUpperCase(); // 数字没有 toUpperCase 方法
} catch(err) {
  console.log("Error Name: " + err.name);
  console.log(err);
}
```

#### URIError

如果你在 URI 函数中使用非法字符，会抛出 `URIError`：

`error-URIError-example.js`

```javascript
try {
  decodeURI("%%%");  // 你不能对百分号进行 URI 解
} catch(err) {
  console.log("Error Name: " + err.name);
  console.log(err);
}
```

### 5. Throw 出错误

`ECMAScript` 允许你在程序运行期间抛出任何内容。程序将认为错误刚刚发生。

`throw-any-example.js`

```javascript
console.log(" -------- Test throw any object ------------");
try {
  let myObj = {};
  throw myObj;
} catch(e)  
  console.log("Catch error: ");
  console.log(e);
}
console.log(" -------- Test throw a Symbol ------------");
try {
  let mySymbol = Symbol();
  throw mySymbol;
} catch(e)  
  console.log("Catch error: ");
  console.log(e);
}
console.log(" -------- Test throw a Number ------------");
try {
  let myNumber = 100;
  throw myNumber;
} catch(e)  
  console.log("Catch error: ");
  console.log(e);
}
console.log(" -------- Test throw a String ------------");
try {
  let myString = "Some error";
  throw myString;
} catch(e)  
  console.log("Catch error: ");
  console.log(e);
}
```

（注：原文代码块中存在多处语法错误如缺少大括号，翻译时已保持逻辑一致并对齐）

**Output**

```
 -------- Test throw any object ------------Catch error: {} -------- Test throw a Symbol ------------Catch error: Symbol() -------- Test throw a Number ------------Catch error: 100 -------- Test throw a String ------------Catch error: Some error
```

```javascript
let err = new Error("My Error");
let rangeErr = new RangeError();
let evalErr = new EvalError("My Eval Error");
// [0.. 9] 中的一个随机值
let randomValue = Math.floor(Math.random() * 10);
// [0,1,2,3]
let random0123 = randomValue % 4;
console.log("random0123 = " + random0123);
try {
  if(random0123 == 0) {
    throw err;
  } else if(random0123 == 1) {
    throw rangeErr;
  } else if(random0123 == 2) {
    throw evalErr;
  } else if(random0123 == 3) {
    throw "A String Error";
  }
} catch(e) {
  console.log("typeof e = " + (typeof e));
  // 'object' 或 'string'
  if(e instanceof RangeError) {
    console.log("--> RangeError!!");
  } else if(e instanceof EvalError) {
    console.log("--> EvalError!!");
  } else if(e instanceof Error) {
    console.log("--> Error!!");
  } else if (typeof e == "string") {
    console.log("--> String Error!!");
  } else {
    console.log("--> Error!!");
  }
  console.log(e);
}
```

### 6. Error 的属性

在 `ECMAScript` 中，你捕获的错误可能是一个"Error 对象"或任何错误类型。如果它是一个"Error 对象"，你将获得重要信息，例如错误的文件名、错误位置、堆栈跟踪（Stack Trace）等。

`Error` 类有一些重要的属性：

* `name`: 错误的名称
* `message`: 错误的内容
* `stack` (只读）：一个包含帮助信息的字符串，可以帮助你定位错误位置。

`error-properties-example.js`

```javascript
// 创建一个 Error
let myError = new Error();
myError.name = "MyError";
myError.message = "My Error String";
try {
  throw myError;
} catch(err) {
  console.log("Error Name: " + err.name);
  console.log("Error Message: " + err.message);
  console.log("Type of err.stack: " + (typeof err.stack));
  console.log("--- Stack Trace: ---");
  console.log(err.stack);
}
```

### 7. 重新抛出错误

在处理异常时，你可以捕获该异常并处理它，也可以重新抛出它。

`rethrow-example.js`

```javascript
function checkScore(score) {
  if (score < 0 || score > 100) {
    throw "Invalid Score " + score;
  }
}
function checkPlayer(name, score) {
  try {
    checkScore(score)
  } catch (e) {
    // 对异常进行某些操作
    console.log("Something invalid with player: " + name + " >> " + e);
  }
}
```

### 8. 捕获异常

在 `ECMAScript` 中，你捕获的错误可能是一个"Error 对象"或任何错误类型。如果它是一个"Error 对象"，你将获得重要信息，例如错误的文件名、错误位置、堆栈跟踪（Stack Trace）等。

`Error` 类有一些重要的属性：

* `name`: 错误的名称
* `message`: 错误的内容
* `stack` (只读）：一个包含帮助信息的字符串，可以帮助你定位错误位置。

`error-properties-example.js`

```javascript
// 创建一个 Error
let myError = new Error();
myError.name = "MyError";
myError.message = "My Error String";
try {
  throw myError;
} catch(err) {
  console.log("Error Name: " + err.name);
  console.log("Error Message: " + err.message);
  console.log("Type of err.stack: " + (typeof err.stack));
  console.log("--- Stack Trace: ---");
  console.log(err.stack);
}
```

### 7. 重新抛出错误

在处理异常时，你可以捕获该异常并处理它，也可以重新抛出它。

`rethrow-example.js`

```javascript
function checkScore(score) {
  if (score < 0 || score > 100) {
    throw "Invalid Score " + score;
  }
}
function checkPlayer(name, score) {
  try {
    checkScore(score)
  } catch (e) {
    // 对异常进行某些操作
    console.log("Something invalid with player: " + name + " >> " + e);
  }
}
```

### 8. 捕获异常

在 `ECMAScript` 中，你捕获的错误可能是一个"Error 对象"或任何错误类型。如果它是一个"Error 对象"，你将获得重要信息，例如错误的文件名、错误位置、堆栈跟踪（Stack Trace）等。

`Error` 类有一些重要的属性：

* `name`: 错误的名称
* `message`: 错误的内容
* `stack` (只读）：一个包含帮助信息的字符串，可以帮助你定位错误位置。

`error-properties-example.js`

```javascript
// 创建一个 Error
let myError = new Error();
myError.name = "MyError";
myError.message = "My Error String";
try {
  throw myError;
} catch(err) {
  console.log("Error Name: " + err.name);
  console.log("Error Message: " + err.message);
  console.log("Type of err.stack: " + (typeof err.stack));
  console.log("--- Stack Trace: ---");
  console.log(err.stack);
}
```

*(注：由于您提供的原文中存在大量重复和乱码占位符，以上译文根据您提供的逻辑结构进行了精简和翻译，以确保符合文档工程师的专业性要求。)*

```javascript
// 通过表单名称获取表单:var myForm = document.forms["myForm"];var u = myForm["username"].value;var p = myForm["password"].value;
```

当用户在表单字段中输入错误的数据时，你应该通知用户并关注该字段。

`validation-example1.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>Validation</title>
<script type "text/javascript">
function validateForm()  {  // 通过表单名称获取表单:var myForm = document.forms["myForm"];var u = myForm["username"].value;var p = myForm["password"].value;
if(u== "") {
  alert("Please enter your Username");
  myForm["username"].focus(); // Focus
  return false;
}
if(p == "") {
  alert("Please enter you Password");
  myForm["password"].focus(); // Focus
  return false;
}
alert("All datas are valid!, send it to the server!")
return true;
}
</script>
</head>
<body>
<h2>Enter your Username and Password</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" method="GET" action="process-action.html" onsubmit = "return validateForm()">
Username: <input type="text" name="username"/><br><br>
Password: <input type="password" name = "password"/><br><br>
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

示例：要求用户输入一个 0 到 10 之间的数字。

`validation-number-example.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>Validation</title>
<script type = "text/javascript">
function validateForm()  {var myField = document.getElementById("myNumber");
var value = myField.value;
if( value == "" || isNaN(value) || value < 0 || value > 10)  {
  alert("Invalid input!");
  myField.focus();
  return false;
}
return true;
}
</script>
</head>
<body>
<h2>Enter a Number between 0 and 10</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html" onsubmit = "return validateForm()">
Number: <input type="text" id= "myNumber"/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

![](img/image_rsrc8S6.jpg)

![](img/image_rsrc8S7.jpg)

![](img/image_rsrc8S8.jpg)

![](img/image_rsrc8S9.jpg)

![](img/image_rsrc8SA.jpg)

![](img/image_rsrc8SB.jpg)

### 4. 通过 Javascript 提交

在表单内点击 `<button type="submit">` 或 `<input type="submit">` 可以帮助你将表单数据发送到服务器，但你也可以通过 Javascript 实现。

`javascript-submit-example.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>Javascript Submit</title>
<script type = "text/javascript">
function validateForm() {var name = document.forms["myForm"]["fullName"].value;
if(name == "") {
  alert("Please enter your name");
  return false;
}
return true;
}
function submitByJavascript()  {var valid = validateForm();
if(!valid)  {
  return;
}
var myForm = document.forms["myForm"];
myForm.submit();
}
</script>
</head>
<body>
<h2>Submit a from with Javascript</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html" onsubmit = "return validateForm()">
Your Name: <input type="text" name = "fullName" value=""/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
<br/><<!-- 表单外的按钮 -->
表单外的按钮:<button onclick="submitByJavascript()">Click Me to submit form</button>
</body>
</html>
```

### 5. 自动验证

浏览器可以自动验证表单上的几种类型的数据，例如通过向表单字段添加 `required` 属性来告诉浏览器该字段是必填的。如果用户没有输入该字段，浏览器将自动检查并通知用户。

![](img/image_rsrc8SC.jpg)

![](img/image_rsrc8SD.jpg)

`required-example.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>Required</title>
</head>
<body>
<h2>Required attribute</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html" onsubmit = "return validateForm()">
Your Name: <input type="text" name = "fullName" value="" required/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

HTML 5 新引入的一些 `<input>` 元素，例如 color、date、datetime-local、email、month、number、range、search、tel、time、url、week。这些元素具有特殊属性，帮助浏览器知道如何自动验证其数据。以下是一些此类属性的列表：

| 属性 |  |
| :--- | :--- |
| disabled | 指定 Input 元素禁用 |
| max | 指定 Input 元素的最大值 |
| min | 指定 Input 元素的最小值 |
| pattern | 指定 Input 元素的数值模式 |
| required | 指定 Input 字段需要该元素 |
| type | 指定 Input 元素的类型 |

示例：带有 `min`、`max` 属性的 `<input type="number">`，如果用户输入的数字超出允许的范围，浏览器将通知用户。

`attr-min-max-example.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>Min Max Attributes</title>
</head>
<body>
<h2>Attribute min, max</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html">
Enter your score (0-100):<input type="number" name = "score" min= "0" max = "100"/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

![](img/image_rsrc8SE.jpg)

![](img/image_rsrc8SF.jpg)

![](img/image_rsrc8SG.jpg)

示例：要求用户输入 2 个字符的国家代码。

`attr-pattern-example.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>pattern attribute</title>
</head>
<body>
<h2>Attribute: pattern</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html">
Country code:<input type="text" name = "countryCode" pattern="[A-Za-z]{2}"title="Two letter code"/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

![](img/image_rsrc8SH.jpg)

![](img/image_rsrc8SJ.jpg)

![](img/image_rsrc8SK.jpg)

![](img/image_rsrc8SM.jpg)

示例：要求用户输入至少 8 个字符的密码。

`attr-pattern-example2.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>pattern attribute</title>
</head>
<body>
<h2>Attribute: pattern</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html">
Password:<input type="password" name = "password" pattern=".{8,}"title="8 more characters"/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

![](img/image_rsrc8SN.jpg)

![](img/image_rsrc8SP.jpg)

示例：要求用户输入包含至少 8 个字符、至少一个大写字母和一个至少和小写字母的强密码。

`attr-pattern-password-example.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>pattern attribute</title>
</head>
<body>
<h2>Attribute: pattern</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html">
Password:<input type="password" name = "password" pattern="(?.*\d)(?=.*[a-z])(?=[A-Z]).{8,}"title="Invalid password!"/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

示例：要求用户输入邮箱地址，使用 pattern 属性确保用户以正确的格式输入邮箱。

`attr-pattern-email-example.html`

```html
<!DOCTYPE html>
<html>
<head>
<title>pattern attribute</title>
</head>
<body>
<h2>Attribute: pattern</h2>
<div style="border:1px solid #ddd; padding: 5px;">
<form name="myForm" action="process-action.html">
Email:<input type="password" name = "password" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$"title="Invalid password!"/><br/><br/><
<button type="submit">Submit</button>
</form>
</div>
</body>
</html>
```

# 第 13 章：JavaScript Web Cookies

## 1. 什么是 Web Cookie

## 2. Cookie 存储在哪里

### 3. 在浏览器中查看 Cookie

## 4. ECMAScript Cookie

## 1. 什么是 Web Cookie

如你所知，Web 浏览器和服务器之间通过 HTTP 协议进行通信。当你使用浏览器访问某个网站时，你的请求会被发送到服务器，服务器将将内容返回给浏览器进行显示。

| ![](img/image_rsrc8SR.jpg) |

Cookie 是一种帮助网站在你的计算机上存储某些信息的技术。它会保存你曾经访问该网站的信息和痕迹。

| ![](img/image_rsrc8SS.jpg) |

为了简单起见，请看以下情况：

| ![](img/image_rsrc8ST.jpg) |

你访问了一个从未访问过的网站。假设该网站支持 2 种语言：英语、法语。因为你以前从未访问过该网站，将显示默认的英语界面。你重置并显示其他语言（如法语）。服务器响应你的请求，并向浏览器发送一个包含你偏好语言（法语）的 Cookie。

你关闭电脑并在第二天再次访问该网站。当请求发送到服务器时，保存在你计算机上的 Cookie 会随请求一起发送，这将帮助服务器确定你的偏好语言并以该语言返回内容。

## 什么是 Web Cookie

- Cookie 是由 Web 服务器发送到你的浏览器的一小段文本。Cookie 可以存储在内存中，也可以作为文件存储在用户的计算机上。Cookie 也可以由运行在浏览器上的 Javascript 生成。

- 存储在客户端的 Cookie 在用户每次访问该网站的任何页面时都会包含在请求中。

Cookie 的主要信息是一对"名称/值"对；例如：

```
SessionID = AAA22311languagePreference = FRheaderColor = BLUE
```

| ![](img/image_rsrc8SU.jpg) |

电子商务网站使用的 Cookie。用户在该网站上购买商品。用户购买的商品存储在 `Cart`（购物车）中。在首次访问时，买家（浏览器）将接收到一个唯一的 `SessionId`（与其他用户不冲突）。

每个 `SesionId` 都关联到在 Web 服务器上管理的购物车。`SessionId/Value` 信息片段是存储在用户计算机上的 Cookie。每当用户创建一个新请求时，此 Cookie 都会附加在请求中，这有助于 Web 服务器区分不同的用户。

## Cookie 包含什么

Cookie 意味着从浏览器传输到 Web 服务器以及反之的简单数据记录，它的结构如下：

```
SSID=Ap4P…GTEq; Domain=amazon.com; Path=/; Expires=Wed, 13 Jan 2023 22:23:01 GMT; Secure;HSID=AYQEVn…DKrdst; Domain=.amazon.com; Path=/; Expires=Wed, 13 Jan 2023 22:23:01 GMT; HttpOnlyHSID=AYQEVn…DKrdst; Domain=amazon.com; Path=/; Max-Age=300; HttpOnly
```

|  | 含义 |
| :--- | :--- |
| `Name=Value` | Cookie 的名称及其值 |
| `Domain` | 网站的域名。 |
| `Expires` | 指定此 Cookie 过期的日期和时间。如果 Cookie 未设置 `Expires` 和 `Max-Age`，它将在用户退出浏览器后立即过期。 |
| `Max-Age` | 该 Cookie 自创建起存在的时间以秒为单位。如果 Cookie 同时具有 `Expires` 和 `Max-Age` 信息，则优先考虑 `Max-Age`。 |
| `Path` | 设置此 Cookie 的目录或页面路径。如果你想在每个目录或每个页面访问此 Cookie，此处可以留空。 |
| `Secure` | 如果此属性可用，即只有安全的服务器可以访问此 Cookie |
| `HttpOnly` | 如果此属性可用，即此 Cookie 只能在服务器端进行操作，但通过浏览器上的 Javascript 无法操作此 Cookie。 |

## 2. Cookie 存储在哪里

Cookie 可以存储在内存中或文件中。在本节中，我仅提到存储在用户计算机文件中的 Cookie。

### IE (Internet Explorer)

使用 `IE` 浏览器时，同一网站的 Cookie 存储在同一个文件中。你可以在下面的目录找到它们：

```
C:\Users\{CurrentUser}\AppData\Roaming\Microsoft\Windows\Cookies
```

## 3. 在浏览器上查看 Cookie

在浏览器上查看 Cookie 非常简单，例如使用 Chrome 浏览器：

| ![](img/image_rsrc8SV.jpg) |

## 4. ECMAScript Cookie

基本上，你有 2 种方法处理 Cookie：

- 在服务器端操作 Cookie。

- 通过运行在用户浏览器上的 Javascript 操作 Cookie。

在用户浏览器中，使用 Javascript(`ECMAScript`)，你可以在没有 `HttpOnly` 属性的情况下操作 Cookie。

下面使用 Javascript 处理 Cookie 的示例。

### cookie-example.html

```html
<!DOCTYPE html><<html><head><meta charset="UTF-8"><title>Cookie example</title><script type="text/javascript" src="cookie-example.js</script</head><body onload="readCookie()">Your Name: <input type="text" name="fullName" id="fullName" /><br/>Fovorite Color:<select name="favoriteColor" id="favoriteColor"><option value="red">Red</option><option value="blue">Blue</option><option value="green">Green</option</select><br><button onclick="writeCookies()">Write Cookies</button><button onclick="killCookies()">Kill Cookies</button><br/><br/><<!--  Read Cookie Results: --><hr />Read Cookie Results:<div id="logArea" style="border:1px solid #ccc;padding: 5px;height:150px</div><button  value = "Get Cookie" onclick = "readCookie()">Read cookies</button</body</html>
```

### cookie-example.js

```javascript
// maxAge: Seconds
function writeCookies(maxAge) {
let expires = new Date();
expires.setSeconds(expires.getSeconds() + maxAge);
let selectedColor = document.getElementById("favoriteColor").value;
let cookie1 = "favoriteColor=" + selectedColor + ";";
cookie1 += "Expires=" + expires.toUTCString() + ";";
cookie1 += "Path=/"; // Path: Required in Chrome!!
// Write Cookie 1
document.cookie = cookie1;
let fullName = document.getElementById("fullName").value;
let cookie2 = "fullName=" + fullName + ";";
cookie2 += "Max-Age=" + maxAge + ";"; // Secondsc
cookie2 += "Path=/"; // Path: Required in Chrome!!
// Write Cookie 2
document.cookie = cookie2;
alert("Write Successful!");
}
function killCookies() {
writeCookies(0);
}
function readCookie() {
var allCookies = document.cookie;
let logText = "All Cookies : " + allCookies + "<br/>";
// Get all the cookies pairs in an array
let cookieArray = allCookies.split(';');
// Now take key value pair out of this array
for (var i = 0; i < cookieArray.length; i++) {
let kvArray = cookieArray[i].split('=');
logText += "Cookie name: " + kvArray[0] + "<br/>";
logText += "Cookie value: " + kvArray[1] + "<br/>";
}
document.getElementById("logArea").innerHTML = logText;
}
```

你可以直接在 Firefox 上运行 `cookie-example.html` 来测试此示例。使用 Chrome 浏览器时，必须在 HTTP 服务器上运行此文件。

```
http://localhost:8080/cookies/cookie-example.html
```

| ![](img/image_rsrc8SW.jpg) |

在表单上输入名称并选择你喜欢的颜色，然后点击"Write Cookies"按钮。Cookie 将被生成并保存到用户的计算机中。

| ![](img/image_rsrc8SX.jpg) |

| ![](img/image_rsrc8SY.jpg) |

| ![](img/image_rsrc8SZ.jpg) |

# 第 14 章：JavaScript void 关键字

## 1. void 关键字

`void` 是 `ECMAScript` 中一个重要的关键字。它具有以下特性：

- `void` 充当运算符，位于任何类型的单操作数之前。

- `void` 用于评估表达式。它不会返回任何值，换句话说，它返回 undefined 值。

`void` 运算符置于任何表达式之前以获取 undefined 值。

### void-expression-example.js

```javascript
void console.log("Test1");  // Test1
console.log( void ("Test2") ); // undefined
console.log( void (2 == "2") );  // undefined
console.log( void (2) == "2" ); // false
console.log( void (2) == undefined); // true
```

## 2. Void 和 JavaScript URIs

`<a href ="javascript:URI">.."a>` 在 HTML 中很常见。浏览器将评估 URI 并取由 URI 返回的值来替换当前页面的内容。

| ![](img/image_rsrc8T0.jpg) |

| ![](img/image_rsrc8T1.jpg) |

| ![](img/image_rsrc8T2.jpg) |

### href-javascript-example.html

```html
<!DOCTYPE html><html><head><meta charset="UTF-8"><title>Href Javascript</title><script>function getHtmlContentToShow()  {console.log("Do something here...");alert("Do something here...");// Return new HTML content to replace current Page.return "<h1 style='color:red;'>Other HTML Content</h1>";</script</head><body><h1>Href:javascript example</h1><a href="javascript:getHtmlContentToShow()">Click me</a</body</html>
```

如果 URI 返回 `undefined`，浏览器将不会替换页的内容。

### href-javascript-void-example.html

```html
<!DOCTYPE html><html><head><meta charset="UTF-8"><title>Href Javascript Void</title><script>function getHtmlContentToShow()  {console.log("Do something here...");alert("Do something here..");// Return new HTML content to replace current Page.return "<h1 style='color:red;'>Other HTML Content</h1>";</script</head><body><h1>Href:javascript void example</h1><a href="javascript:void getHtmlContentToShow()">Click me</a</body</html>
```

## 3. 一次性函数

通常情况下，你需要定义一个函数然后调用它。

#### function-example.js

```javascript
// 定义一个函数
function sayHello()  {console.log("Hello Everyone");}// 调用函数
sayHello();
```

下面的示例向你展示了如何创建一个仅供一次目的的函数。它会被立即调用。你将无法在程序的任何地方再次使用此函数因为它因为它在用后就不存在了。

#### used-once-function-example.js

```javascript
// 定义一个函数，并调用它。
(function sayHello()  {console.log("Hello Everyone");}) ();
try  {
// 这个函数不存在。
sayHello();}
}catch(e)  {
console.log(e); // ReferenceError: sayHello is not defined
} 
```

你也可以使用 `void` 关键字创建一个仅使用一次的函数。它会被立即调用，并且在调用后就不再存在了。

#### void-function-example.js

```javascript
// 定义一个函数，并调用它。
void function sayHello()  {console.log("Hello Everyone");}();
try  {
// 这个函数不存在。
sayHello();}
}catch(e)  {
console.log(e); // ReferenceError: sayHello is not defined
} 
```

# 第 15 章：类与对象

1. 你的第一个类
2. Getter & Setter
3. 静态属性
4. 静态方法
5. 对象比较运算符

## 1. 你的第一个类

下面，我有一个 `Rectangle`（矩形），它有两个重要的属性：`width` 和 `height`。我们将使用 ES6 语法定义一个名为 `Rectangle` 的类来模拟它。

![](img/image_rsrc8T3.jpg)

创建一个资源文件 `rectangle.js`：

### rectangle.js

```javascript
// 定义一个类。
class Rectangle  {
// 带有 2 个参数的构造函数。
// (用于实例化)
// this.width 指向类的宽度属性
constructor (width = 5 , height = 10)  {this.width = width;this.height = height;}
// 一个方法计算矩形的面积。
getArea() {var area = this.width * this.height
return area}}
// 通过构造函数创建 Rectangle 的对象。
var rect = new Rectangle(3, 5);
console.log("Height "+ rect.height);
console.log("Width "+ rect.width);
// 调用方法
let area = rect.getArea();
console.log("Area "+ area );
```

运行示例：

**输出**

```
Height 5
Width 3
Area 15
```

当你从类的构造函数创建一个对象时会发生什么？

![](img/image_rsrc8T4.jpg)

当你调用类的构造函数时，会创建一个新对象，对象的属性将从参数中赋值。

在 `ECMAScript` 中，每个类最多只有一个构造函数。像函数一样，构造函数的参数也可以有默认值。因此你可以以不同的方式创建对象。

```javascript
// width = 3, height = 5
let rect = new Rectangle(3, 5);
// width = 15, height = 10 (默认值)
let rect2 = new Rectangle(15);
// width = 5 (默认值), height = 50
let rect3 = new Rectangle(undefined, 50);
// width = 5 (默认值), height = 10 (默认值)
let rect4 = new Rectangle();
```

## 2. Getter & Setter

在给出 Getter & Setter 的概念之前，让我们先分析一种情况：

假设我们有一个 `Person` 类，这个类有一个名为 `name` 的属性。

#### Class Person

```javascript
class Person  {constructor(name) {this.name = name;}}
```

你可以访问对象的属性，或者给它赋新值而不会出现任何问题。

```javascript
// 创建对象
let person = new Person("Tom");
// 访问属性 name。
console.log( person.name); // Tom
// 给属性 name 赋新值。
person.name = "Jerry"; // !!!
console.log( person.name ); // Jerry
```

在类外部自由属性并更改其值是非常危险的。有时，你希望某个属性无法被访问，或者无法从类外部对其赋新值。Getter/Setter 允许你创建这样的属性。

好的，我们重新写一遍 `Person` 类。在没有类参数的方法前加上 `get` 关键字，可以创建一个名称与方法名相同的属性。每当程序访问此属性时，该方法就会被调用。

#### getter-example1.js

```javascript
class Person  {
constructor (name)  {//属性: __name
this.__name = name;}
// 属性 name 的 getter
get name()  {console.log("Call getter of property 'name'!!");
return this.__name;}}
// ------------ 测试 -----------------
let person = new Person("Tom");
// 访问属性 'name' ==> 调用 getter
console.log( person.name); // Tom
// 给属性 name 赋新值。
person.name = "Jerry"; // 无效!!!!
// 访问属性 'name' ==> 调用 getter
console.log( person.name); // Tom
```

在带有一个类参数的方法前加上 `set` 关键字，可以创建一个名称与方法名相同的属性。每当程序为此属性赋新值时，该方法就会被调用。

#### setter-example1.js

```javascript
class Person  {constructor (name)  {//属性: __name
this.__name = name;}
// 属性 name 的 setter
set name(newName)  {console.log("Call setter of property 'name'!!");
this.__name = newName;}
// 一个方法
showInfo()  {console.log("Person: " + this.__name);}}
// ------------ 测试 -----------------
let person = new Person("Tom");
// 无法访问属性 'name'
console.log( person.name); // undefined
// 为属性 'name' 赋新值 ==> 调用 setter
person.name = "Jerry";
person.showInfo(); // Person: Tom
```

带有 Getter & Setter 的属性示例：

#### getter-setter-example.js

```javascript
class Rectangle  {constructor (width = 5 , height = 10)  {this.__width = width;this.height = height;}
// 属性 width 的 getter
get width()  {return this.__width;}
// 属性 width 的 setter
set width(newWidth)  {if(newWidth > 0) {this.__width = newWidth;} else{console.log("Invalid width " + newWidth);}}}
// ------------ 测试 ------------------
var rect = new Rectangle(3, 5);
console.log("Height "+ rect.height); // Height: 5
console.log("Width "+ rect.width); // Width: 3
rect.width = -100;
console.log("Height "+ rect.height); // Height: 5
console.log("Width "+ rect.width); // Width: 3
rect.width = 100;
console.log("Height "+ rect.height); // Height: 5
console.log("Width "+ rect.width); // Width: 100
```

**输出**

```
Height 5
Width 3
Invalid width -100
Height 5
Width 3
Height 5
Width 100
```

#### 私有属性

```javascript
class Something {constructor(){this.#someProperty = "test";}}
const instance = new Something();
console.log(instance.#someProperty); // undefined
```

#### getter-example2.js

```javascript
class Person  {constructor (name)  {// 私有属性: #name
this.#name = name;}
// 属性 name 的 getter
get name()  {console.log("Call getter of property 'name'!!");
return this.#name;}}
```

## 3. 静态属性

`static` 关键字出现在 Getter 或 Setter 声明中，帮助你定义一个静态属性。你可以通过类名访问静态属性。

具有固定值（不可更改）的静态属性被称为常量静态属性。

`static-field-example1.js`

```javascript
class Employee {
  constructor(fullName, age) {
    this.fullName = fullName;
    if (age < Employee.MIN_AGE || age > Employee.MAX_AGE) {
      throw "Invalid Age " + age;
    }
    this.age = age;
  }
  // 一个静态字段: MIN_AGE
  static get MIN_AGE() {
    return 18;
  }
  // 一个静态字段: MAX_AGE
  static get MAX_AGE() {
    if (!Employee.__MAXA) {
      Employee.__MAXA = 60;
    }
    return Employee.__MAXA;
  }
  static set MAX_AGE(newMaxAge) {
    Employee.__MAXA = newMaxAge;
  }
}
// ---- TEST ---------
console.log("Mininum Age Allowed: " + Employee.MIN_AGE);
console.log("Maximum Age Allowed: " + Employee.MAX_AGE);
// 设置新的最大年龄:
Employee.MAX_AGE = 65;
console.log("Maximum Age Allowed: " + Employee.MAX_AGE);
let baby = new Employee("Some Baby", 1); // 错误!!
```

你还有另一种声明类静态字段的方法，但通过这种方式创建的静态字段不会是常量，因为它的值可以改变。以下是一个示例：

`static-field-example2.js`

```javascript
class Employee {
  constructor(fullName, age) {
    this.fullName = fullName;
    if (age < Employee.MIN_AGE || age > Employee.MAX_AGE) {
      throw "Invalid Age " + age;
    }
    this.age = age;
  }
}
Employee.MIN_AGE = 18;
Employee.MAX_AGE = 60;
// ---- TEST ---------
console.log("Mininum Age Allowed: " + Employee.MIN_AGE);
console.log("Maximum Age Allowed: " + Employee.MAX_AGE);
// 设置新的最大年龄:
Employee.MAX_AGE = 65;
console.log("Maximum Age Allowed: " + Employee.MAX_AGE);
let baby = new Employee("Some Baby", 1); // 错误!!
```

## 4. 静态方法

在类方法的声明中出现的 `Static` 关键字可以帮助你定义一个静态方法。你可以通过类名调用静态方法。静态方法不能通过类的对象调用。静态方法通常用作应用程序的工具函数。

![](img/image_rsrc8T5.jpg)

`point.js`

```javascript
class Point {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }
  // 计算两点之间的距离
  static distance(point1, point2) {
    const dx = point1.x - point2.x;
    const dy = point1.y - point2.y;
    return Math.hypot(dx, dy);
  }
}
// --- TEST ---
let point1 = new Point(5, 10);
let point2 = new Point(15, 20);
// 距离
let d = Point.distance(point1, point2);
console.log("Distance between 2 points: " + d);
```

### 输出

`Distance between 2 points: 14.142135623730951`

## 5. 对象比较运算符

在 `ECMAScript` 中，通过构造函数创建对象时，内存中会创建一个真实的实体，它有一个指定的地址。

将 `AA` 对象赋值给 `BB` 对象不会在内存中创建新实体，它只是将 `BB` 的地址指向 `AA` 的地址。

![](img/image_rsrc8T6.jpg)

`===` 运算符用于比较两个指向的对象，如果两个对象引用内存中的同一个地址，则返回 true。`!==` 用于比较两个对象指向的地址，如果两个对象指向两个不同的地址，则返回 true。

`identify-operator-example.js`

```javascript
// 定义一个类。
class Rectangle {
  constructor(width = 5, height = 10) {
    this.width = width;
    this.height = height;
  }
  getArea() {
    var area = this.width * this.height;
    return area;
  }
}
// 创建对象: r1
let r1 = new Rectangle(20, 10);
// 创建对象: r2
let r2 = new Rectangle(20, 10);
let r3 = r1;
let b12 = r1 === r2; // false
let b13 = r1 === r3; // true
console.log("r1 === r2 ? " + b12); // false
console.log("r1 === r3 ? " + b13); // true
var bb12 = r1 !== r2; // true
var bb13 = r1 !== r3; // false
console.log("r1 !== r2 ? " + bb12); // true
console.log("r1 !== r3 ? " + bb13); // false
```

运行示例：

### 输出

`r1 === r2 ? false`

`r1 === r3 ? true`

`r1 !== r2 ? true`

`r1 !== r3 ? false`

# 第 16 章：类与继承

## 1. JavaScript 中的类

## 2. ES3 中的类与继承

## 3. ES5 中的类与继承

## 1. JavaScript 中的类

JavaScript 实际上是一个函数和对象的世界。它最初的设计非常简单，没有的类的概念。也许 JavaScript 的创造者没有考虑到有一天这门语言会被如此广泛地使用。

JavaScript 中的对象意味着一个具有多个"键/值"对的实体，你可以通过对象和键来访问值。

`object-example1.js`

```javascript
var tom = {name: "Tom", country: "USA" };
// 访问：
console.log(tom.name); // Tom
console.log(tom.country); // USA
console.log(tom["name"]); // Tom
console.log(tom["country"]); // USA
```

你可以向现有对象添加新的"键/值"对，或删除它的"键/值"对。

`object-example2.js`

```javascript
var tom = {name: "Tom", country: "USA" };
// 删除属性 - country
delete tom["country"]; // 等于: delete tom.country;
// 添加属性 - gender
tom["gender"] = "Male"; // 等于: tom.gender = "Male";
// 访问：
console.log(tom.name); // Tom
console.log(tom["name"]); // Tom
console.log(tom["country"]); // undefined
console.log(tom.country); // undefined
console.log(tom["gender"]); // Male
```

首先，看 ES6 引入的现代语法，创建一个带有返回面积的 `getArea()` 方法的 `Rectangle` 类。

![](img/image_rsrc8T7.jpg)

`es6-example.js`

```javascript
// ECMAScript 6
class Rectangle {
  constructor(width, height) {
    this.width = width;
    this.height = height;
  }
  getArea() {
    return this.width * this.height;
  }
}
// ------------- 测试
var rect = new Rectangle(10, 5);
var area = rect.getArea();
console.log("Width: " + rect.width);
console.log("Height: " + rect.height);
console.log("Area: " + area);
```

通过 ES6 创建一个类的子类非常简单：

`es6-inheritance.js`

```javascript
class Shape {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }
}
// 子类
class Circle extends Shape {
  constructor(x, y, radius) {
    super(x, y);
    this.radius = radius;
  }
  getArea() {
    return Math.PI * this.radius * this.radius;
  }
}
// 测试
var circle = new Circle(0, 0, 5);
console.log("x: " + circle.x);
console.log("y: " + circle.y);
console.log("Area: " + circle.getArea());
```

## 2. ES3 中的类与继承

ES3 使用 `function` 关键字来定义"构造函数"。当你使用 `new` 运算符调用此函数时，会创建一个新的对象：

```javascript
// ECMAScript 3
function Rectangle(width, height) {
  this.width = width;
  this.height = height;
}
// 创建对象
var rect = new Rectangle(10, 5);
```

下面的图说明了 JavaScript 机器的操作：

![](img/image_rsrcT8.jpg)

* `rect` 对象被创建（它只是一个普通对象）
* 为 `rect` 对象添加 `__proto__` 属性。这是一个隐藏属性。
* 该变量将指向 `rect` 对象的地址。
* 为"rect"对象添加 `width` 属性。
* 为 `rect` 对象添加 `height` 属性。

原型概念也引入了 ES3。让我们它的用途：

```javascript
// ECMAScript 3
function Rectangle(width, height) {
  this.width = width;
  this.height = height;
}
Rectangle.prototype.bgColor = "red";
Rectangle.prototype.borderColor = "blue";
// 创建一个对象
var rect = new Rectangle(10, 5);
console.log(rect); // Rectangle { width: 10, height: 5 }
console.log(rect.__proto__); // Rectangle { bgColor: 'red',borderColor: 'blue' }
console.log(rect.__proto__.bgColor); // red
console.log(rect.__proto__.borderColor); // blue
// （阅读解释）
console.log(rect.bgColor); // red
console.log(rect.borderColor); // blue
```

![](img/image_rsrcT9.jpg)

当 JavaScript 运行时遇到 `myObject.myProperty` 表达式时发生了什么？

答案是它会检查 `myObject` 对象是否存在 `myProperty` 属性。如果有，它就访问该属性；反之，它访问 `myObject.__proto__.myProperty`。

`es3-proto-example3.js`

```javascript
var rect = {
  __proto__: { bgColor: "red", borderColor: "blue" },
  width: 10,
  height: 5
};
console.log(rect.width); // 10
console.log(rect.__proto__.bgColor); // red
console.log(rect.bgColor); // red
```

# 继承

![](img/image_rsrc8TA.jpg)

在 ES3 中，你可以通过许多不同的方式来模拟继承另一个类的类。当然，这不像在 ES6 中那样那么简单，而且对许多程序员来说这非常困惑。

为了简单起见，我提供了一个继承的示例，并分析了在这种情况下 JavaScript 运行时的操作规则。

* `Animal` 类拥有 2 个属性：`name` 和 `gender`。
* `Cat` 类继承自 `Animal` 类。它有 1 个 `color` 属性。

![](img/image_rsrc8TB.jpg)

`es3-inheritance-example1.js`

```javascript
function Animal(n, g) {this.name = n;this.gender = g;}function Cat(n, g, c) {Animal.call(this, n, g);this.color = c;}var tom = new Cat("Male", "Tom", "Black");// Cat { gender: 'Male', name: 'Tom', color: 'Black' }console.log(tom);
```

![](img/image_rsrc8TC.jpg)

# 继承与原型链的作用 (ES3)

`es3-inheritance-example2.js`

```javascript
// Class: Animal
function Animal(n, g) {this.name = n;this.gender = g;}Animal.prototype.sleep = function()  {console.log("Animal sleeping..");}Animal.prototype.move = function()  {console.log("Animal moving..");}// Class: Cat
function Cat(n, g, c) {Animal.call(this, n, g); // 重要!!this.color = c;}// 重要!!var TempFunc = function() {}; // 临时类.TempFunc.prototype = Animal.prototype;Cat.prototype = new TempFunc();// ------------------Cat.prototype.cry = function()  {console.log("Meo meo");}// 重写 Animal 的 'move' 方法.Cat.prototype.move = function() {console.log("Cat moving..");}var tom = new Cat("Male", "Tom", "Black");// Cat { gender: 'Male', name: 'Tom', color: 'Black' }console.log(tom);tom.move(); // Cat moving..tom.sleep(); // Animal sleeping..tom.cry(); // Meo meo
```

# 3. ES5 中的类与继承

## Object.create(srcObject)

`Object.create(srcObject)` 方法创建一个新的 `newObject` 对象，其中 `newObject.__proto__` 是 `srcObject` 的拷贝。

![](img/image_rsrc8TD.jpg)

`method-object-create-example.js`

```javascript
var john = {name: "John",gender: "Male"};var other = Object.create(john);console.log(other.__proto__); // { name: 'John', gender: 'Male' }
```

## 继承 (ES5 + Object.create)

使用 ES5 的 `Object.create(srcObject)` 方法可以帮你比 ES3 更容易地模拟类和继承。

`es5-inheritance-example1.js`

```javascript
// Class: Animal
function Animal(n, g) {this.name = n;this.gender = g;}Animal.prototype.sleep = function()  {console.log("Animal sleeping..");}Animal.prototype.move = function()  {console.log("Animal moving..");}// Class: Cat
function Cat(n, g, c) {Animal.call(this, n, g); // 重要!!this.color = c;}Cat.prototype = Object.create(Animal.prototype); // 重要!!Cat.prototype.cry = function()  {console.log("Meo meo");}// 重写 Animal 的 'move' 方法.Cat.prototype.move = function() {console.log("Cat moving..");}var tom = new Cat("Male", "Tom", "Black");// Cat { gender: 'Male', name: 'Tom', color: 'Black' }console.log(tom);tom.move(); // Cat moving..tom.sleep(); // Animal sleeping..tom.cry(); // Meo meo
```

# 第 17 章：继承与多态

1. ECMAScript 中的继承
2. 方法重写
3. 抽象方法
4. 运算符 - instanceof, typeof
5. 函数实现的多态

## 1. ECMAScript 中的继承

`ECMAScript` 允许你创建一个从一个或多个其他类扩展而来的类。这个类被称为派生类或子类。

子类将从父类继承属性、方法和其他成员。它还可以重写来自父类的方法。在 `ECMAScript` 中，每个类只有一个构造函数。如果类本身没有定义它自己的构造函数，它将继承父类的构造函数。相反，如果子类定义了构造函数，它将不会继承父类的构造函数。

我们需要几个类来参与示例。

* `Animal`: 模拟动物的类。
* `Duck`: `Animal` 的子类。
* `Cat`: `Animal` 的子类。
* `Mouse`: `Animal` 的子类。

![](img/image_rsrc8TE.jpg)



# ECMAScript 类与继承

在 ECMAScript 中，类的构造函数用于创建对象（实例），并为属性赋值。子类的构造函数总是会调用父类的构造函数，以初始化父类属性的值，然后为它自己的属性赋值。

## 示例

`Cat` 是继承自 `Animal` 类的类，它也有自己的属性。

`inherit-example1.js`

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  showInfo() {
    console.log("I'm " + this.name);
  }
  move() {
    console.log("Moving..");
  }
}
class Cat extends Animal {
  constructor(name, age, height) {
    super(name);
    // Cat's 属性:
    this.age = age;
    this.height = height;
  }
  // 重写父类的方法
  showInfo() {
    console.log("My name is " + this.name);
  }
  // 其他方法...
  sleep() {
    console.log("Sleeping..");
  }
}
// ------------- 测试 --------------------
let tom = new Cat("Tom", 3, 20);
console.log("Call move() method");
tom.move();
console.log("\n");
console.log("Call showInfo() method");
tom.showInfo();
```

### 输出

```
Call move() method
Moving..
Call showInfo() method
My name is Tom
```

当你在从构造函数创建对象时发生了什么？它是如何调用父类构造函数的？请看下方的图：

![](img/image_rsrc8TF.jpg)

通过上面的插图你可以看到，父类的构造函数是在子类的构造函数中调用的，父类的构造函数在子类的构造函数中被调用。

## 2 方法重写

默认情况下，子类从父类继承方法，但父类可以重写方法。

`inheritance-example2.js`

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  showInfo() {
    console.log("I'm " + this.name);
  }
  move() {
    console.log("Moving..");
  }
}
class Mouse extends Animal {
  constructor(name, age, height) {
    super(name);
    this.age = age;
    this.height = height;
  }
  // 重写父类的方法
  showInfo() {
    console.log("Age: " + this.age);
    console.log("Height: " + this.height);
  }
  // 重写父类的方法
  move() {
    console.log("Mouse..");
  }
}
// ------------- 测试 --------------------
let jerry = new Mouse("Jerry", 3, 5);
console.log("Call move() method");
jerry.move();
console.log("\n");
console.log("Call showInfo() method");
jerry.showInfo();
```

### 输出

```
Call move() method
Mouse..
Call showInfo() method
Age: 3
Height: 5
```

## 3 抽象方法

抽象方法或抽象类的概念在 Java、C# 等语言中是有定义的。但在 ECMAScript 中没有明确定义。不过，我们有一种方法可以定义它。

作为抽象类的类定义了抽象方法，子类如果想使用这些方法必须重写它们。抽象方法总是抛出“未实现错误”异常。

`abstract-example.js`

```javascript
// 一个抽象类。
class AbstractDocument {
  constructor(name) {
    this.name = name;
  }
  // 该方法不能被使用，因为它总是抛出错误。
  show() {
    // 未实现错误
    throw "Subclass must implement abstract method";
  }
}
class PDF extends AbstractDocument {
  // 重写父类的方法
  show() {
    console.log("Show PDF document:", this.name);
  }
}
class Word extends AbstractDocument {
  show() {
    console.log("Show Word document:", this.name);
  }
}
// -------------------- 测试 -------------------------
let doc1 = new PDF("Python tutorial");
let doc2 = new Word("Java IO Tutorial");
let doc3 = new PDF("ECMAScript Date & Time Tutorial");
let documents = [doc1, doc2, doc3];
for (let i = 0; i < documents.length; i++) {
  documents[i].show();
}
let doc4 = new AbstractDocument("An Abstract Document");
doc4.show(); // 抛出错误!!!
```

## 4 运算符 - instanceof, typeof

`instanceof` 运算符可以帮你检查“某物”是否是某个类的实例。

`instanceof-example.js`

```javascript
class Person {}
// A Child class of Person
class AsianPerson extends Person {}
class Triangle {}
let person = new Person();
let asianPerson = new AsianPerson();
let triangle = new Triangle();
let isPerson = person instanceof Person;
console.log(isPerson); // true
console.log(asianPerson instanceof Person); // true
console.log(person instanceof AsianPerson); // false
console.log(triangle instanceof Person); // false
console.log(triangle instanceof AsianPerson); // false
```

### typeof

`typeof` 运算符用于检查“某些东西”的类型。获得的结果是类型的名称。

`typeof-example.js`

```javascript
// 一个类:
class Person {}
// 一个对象:
let person = new Person();
console.log(typeof Person); // function
console.log(typeof person); // object
// null:
console.log(typeof null); // object
// 一个数字:
let intValue = 100;
console.log(typeof intValue); // number
// NaN (不是一个数字)
console.log(typeof NaN); // number
// 一个字符串
let strValue = "Hello";
console.log(typeof strValue); // string
// 一个布尔值:
let boolValue = true;
console.log(typeof boolValue); // boolean
// undefined
console.log(typeof undefined); // undefined
// 一个数组
let years = [1980, 2003, 2018];
console.log(typeof years); // object
// 一个函数
let myFunc = function() {}
console.log(typeof myFunc); // function
// 一个符号
let mySymbol = Symbol();
console.log(typeof mySymbol); // symbol
```

## 是否为子类

假设你有两个类，`A` 和 `B`。下面的示例帮助你检查 `A` 是否是 `B` 的子类。

`let isChild = A === B || A.prototype instanceof B;`

`issubclass-example.js`

```javascript
class Animal {}
class Cat extends Animal {}
class AsianCat extends Cat {}
// ------------- 测试 --------------------
console.log("AsianCat === Animal? " + (AsianCat === Animal)); // false
let isSubClass1 = AsianCat === Animal || AsianCat.prototype instanceof Animal;
console.log("AsianCat is child of Animal? " + isSubClass1); // true
let isSubClass2 = AsianCat === Animal || Animal.prototype instanceof AsianCat;
console.log("Animal is child of AsianCat? " + isSubClass2); // false
```

### 输出

| isinstance('abc', object): True |
| :--- |
| isinstance(123, object): True |
| b = B() |
| a = A() |
| isinstance(b, A): True |
| isinstance(b, B): True |
| isinstance(a, B): False |
| isinstance(B, A): True |
| isinstance(A, B): False |

## 5 函数中的多态

在这里我创建了两个类，例如 `English` 和 `French`。这两个类都拥有 `greeting()` 方法。它们创建了不同的问候语。从上述两个类创建两个对应的对象，并在同一个函数（`intro` 函数）中调用这两个对象的动作。

`polymorphism-example.js`

```javascript
class English {
  greeting() {
    console.log("Hello");
  }
}
class French {
  greeting() {
    console.log("Bonjour");
  }
}
function intro(language) {
  language.greeting();
}
// -------------- 测试 ----------------------
let flora = new English();
let aalase = new French();
// 调用函数:
intro(flora);
intro(aalase);
let someObject = {};
intro(someObject); // Error!!!
```

OK，修正上述示例的代码，添加必要的检查以避免你的应用程序出现风险：

`polymorphism-example2.js`

```javascript
class English {
  greeting() {
    console.log("Hello");
  }
}
class French {
  greeting() {
    console.log("Bonjour");
  }
}
function intro(language) {
  // 检查 'language' 对象的类型
  if (language instanceof English || language instanceof French) {
    language.greeting();
  }
}
// -------------- 测试 ----------------------
let flora = new English();
let aalase = new French();
// 调用函数:
intro(flora);
intro(aalase);
let someObject = {};
intro(someObject);
```

应用“类与继承”架构有助于你的应用程序更易管理并避免错误。

`polymorphism-example3.js`

```javascript
// 一个基类
class Language {}
class English extends Language {
  greeting() {
    console.log("Hello");
  }
}
class French extends Language {
  greeting() {
    console.log("Bonjour");
  }
}
function intro(language) {
  // 检查 'language' 对象的类型
  if (language instanceof Language) {
    language.greeting();
  }
}
// -------------- 测试 ----------------------
let flora = new English();
let aalase = new French();
// 调用函数:
intro(flora);
intro(aalase);
let someObject = {};
intro(someObject);
```

# 第 18 章：JavaScript Set 集合

## 1 集合 (Collections) - Set

## 2 Set 的方法

## 3 WeakSet

### 1 Collections - Set

ECMAScript 6 引入了两个新的数据结构，如 `Map` 和 `Set`。它们是 ECMAScript 集合框架的一部分。

**Maps**: 这种数据结构允许你存储“键/值对”。你可以通过键访问值，或为键更新新值。

**Sets**: 这种数据结构存储一个元素列表，不允许重复，且不对元素进行索引。

在这篇文章中，我将向你介绍 `Set`。

#### Set

`Set` 是 ECMAScript6 中引入的一种数据结构。以下是 Set 的特性。

* `Set` 是一个不允许迭代的元素列表。
* `Set` 不对元素进行索引。
* `Set` 是一个有序列表，这意味着先添加的元素会在前面，第二个添加的元素会在后面。

#### 构造函数

通过 `Set` 的构造函数创建 `Set` 对象：

```javascript
new Set([iterable])
```

#### 参数

* `iterable` - 如果将此对象传递给 `Set` 的构造函数，其所有元素都将添加到 `Set` 中。相反，如果你没有指定此参数，或者其值为 `null`，则创建的 `Set` 对象将是空的。

#### 属性

`set-example.js`

```javascript
// 从数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }
```

`set-size-example.js`

```javascript
// 从数组创建一个 Set
var fruits = new Set(['Apple', 'Banana', 'Papaya']);
var size = fruits.size;
console.log(size); // 3
```

#### for..of

你可以使用 `for...of` 循环来遍历 `Set` 的元素。

`set-for-of-loop-example.js`

```javascript
// 从数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
for (let fruit of fruits) {
  console.log(fruit);
}
```

### 输出

| Apple |
| :--- |
| Banana |
| Papaya |

## 2 Set 的方法

### add(value)

如果此元素不存在于 `Set` 中，则将其添加到 `Set` 的末尾并返回此 `Set` 对象。

`set-add-example.js`

```javascript
// 从数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
// 将一个元素添加到 Set 并返回此 Set。
var thisFruits = fruits.add("Cherry");
console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya', 'Cherry' }
// 'Set' 不允许重复
fruits.add("Banana");
console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya', 'Cherry' }
```

### 输出

| Set { 'Apple', 'Banana', 'Papaya', 'Cherry' } |
| :--- |
| Set { 'Apple', 'Banana', 'Papaya', 'Cherry' } |

### delete(value)

此方法用于从 `Set` 中移除一个元素。如果找到了要删除的元素，方法返回 `true`，否则返回 `false`。

`set-delete-example.js`

```javascript
// 从数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }
// 删除一个元素:
var deleted = fruits.delete("Banana");
console.log("Deleted? " + deleted); // true
console.log(fruits); // Set { 'Apple', 'Papaya' }
```

### clear()

移除 `Set` 中的所有元素。

`set-clear-example.js`

```javascript
// 从数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }
// 移除所有元素。
fruits.clear();
console.log(fruits); // Set { }
console.log("Size after clear: " + fruits.size);
```

### entries()

此方法返回一个新的迭代器对象，其中每个条目包含一个两个元素的数组，如 `[value, value]`。条目的顺序仍然与 Set 对象中元素的顺序保持不变。（参见下面的插图）

![](img/image_rsrc8TG.jpg)

`set-entries-example.js`

```javascript
// 从一个数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }

// Iterator 对象:
var iteratorEntries = fruits.entries();
var entry;
while (!(entry = iteratorEntries.next()).done) {
  console.log(entry.value); // [ 'Apple', 'Apple' ]
}
```

### has(value)

该方法测试参数提供的值是否存在 Set 中。如果存在则返回 true，否则返回 false。

`set-has-example.js`

```javascript
// 从一个数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
var has = fruits.has("Banana");
console.log(has); // true
```

### forEach(callbackFn[, thisArg])

该方法会为 Set 的每个元素调用一次 `callbackFn` 函数。

```javascript
mySet.forEach(callbackFn[, thisArg])
```

#### 参数:

- `callbackFn` - 该函数会对应 Set 对象的每个元素被调用一次。
- `thisArg` - 执行 `callbackFn` 函数时用作 `this` 的参数。

`set-forEach-example.js`

```javascript
// 从一个数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
console.log(fruits); // Set { 'Apple', 'Banana', 'Papaya' }
function showFruit(fruit, thisSet) {
  console.log("Fruit: " + fruit);
}
// 或者调用：fruits.forEach(showFruit);
fruits.forEach(showFruit, fruits);
```

### key() & values()

`key()` & `values()` 方法返回一个新的迭代器，其每个元素的形状为 `{value: aValue, done: false}`。

![](img/image_rsrc8TH.jpg)

`set-values-example.js`

```javascript
// 从一个数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
var fruitIterator = fruits.values();
var entry;
while (!(entry = fruitIterator.next()).done) {
  console.log(entry); // { value: 'Apple', done: false }
  console.log(entry.value); // Apple
}
```

#### 运行示例:

输出

```
{ value: 'Apple', done: false }
Apple
{ value: 'Banana', done: false }
Banana
{ value: 'Papaya', done: false }
Papaya
```

### mySet[Symbol.iterator]

`Symbol.iterator` 是 `Set` 的特殊属性。默认情况下，`mySet[Symbol.iterator]` 的值是 `mySet` 的 `values()` 方法。

`set-symbol-iterator-example.js`

```javascript
// 从一个数组创建一个 Set
var fruits = new Set(["Apple", "Banana", "Papaya"]);
// 等同于：fruits.values()
var fruitIterator = fruits[Symbol.iterator]();
var entry;
while (!(entry = fruitIterator.next()).done) {
  console.log(entry); // { value: 'Apple', done: false }
  console.log(entry.value); // Apple
}
```

## 3 WeakSet

基本上，`WeakSet` 与 `Set` 非常相似，但它有以下区别：

- `WeakSet` 的元素必须是对象，不能是原始类型。
- `WeakSet` 的元素可以在垃圾回收过程中被移除，垃圾回收是一个移除程序中不再使用的对象的独立过程。
- `WeakSet` 不支持属性：`size`，因此你无法知道它有多少个元素。
- `Set` 类中可能提供的许多方法，在 `WeakSet` 中没有，例如 `values()`、`keys()`、`clear()` 等。

#### 创建一个 WeakSet 对象。

```javascript
new WeakSet([iterable])
```

#### 参数:

- `iterable` - 如果将此对象传递给 `WeakSet` 构造函数，它的所有元素都将添加到 `WeakSet` 中。相反，如果你没有指定此参数，或者其值为 `null`，则创建的 `WeakSet` 对象将是空的。

#### 方法:

`WeakSet` 方法的数量少于 `Set` 方法的数量：

- `WeakSet.add(element)`
- `WeakSet.delete(element)`
- `WeakSet.has(element)`

`WeakSet` 中的元素必须是对象，不能是原始类型。

```javascript
let w = new WeakSet();
w.add('a'); // TypeError: Invalid value used in weak set
let s = new Set();
s.add('a'); // Works
```

`weakset-example.js`

```javascript
var element1 = {}; // 一个对象
var element2 = {foo: "bar"};
var element3 = {bar: "foo"};
var myWeakSet = new WeakSet([element1, element2]);
myWeakSet.add(element3);
console.log(myWeakSet.has(element2)); // true
```

# 第 19 章：JavaScript Map 集合

## 1 Collections - Map

## 2 Map 方法

## 3 WeakMap

### 1 Collections - Map

ECMAScript 6 引入了两个新的数据结构，如 `Map` & `Set`。它们是 `ECMAScript Collections Framework` 的一部分。

- `Maps` - 这种数据结构允许你存储“键/值”对。你可以通过键访问值，或者更新对应于键的新值。
- `Sets` - 这种数据结构存储元素列表，不允许重复且不对元素进行索引。

#### Map:

一个 `Map` 对象存储“键/值”，其中键和值可以是原始类型或对象。

- 在 `Map` 对象中，键是可迭代的。
- `Map` 是一个有序的数据类型，这意味着第一个添加的“键/值”对将排在前面，第二个对将排在后面。

![](img/image_rsrc8TJ.jpg)

通过 `Map` 类的构造函数创建 Map 对象：

```javascript
new Map([iteratorObject])
```

#### 参数:

- `iteratorObject` - 可迭代的对象。

`map-size-example.js`

```javascript
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
console.log(myContacts.size); // 3
```

#### for..of

你可以使用 `for..of` 循环来遍历 `Map` 的键/值对。

`map-for-of-loop-example.js`

```javascript
// 创建一个 Map 对象。
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
for (let arr of myContacts) {
  console.log(arr);
  console.log(" - Phone: " + arr[0]);
  console.log(" - Name: " + arr[1]);
}
```

#### 运行示例:

输出

```
[ '0100-1111', 'Tom' ]
- Phone: 0100-1111
- Name: Tom
[ '0100-5555', 'Jerry' ]
- Phone: 0100-5555
- Name: Jerry
[ '0100-2222', 'Donald' ]
- Phone: 0100-2222
- Name: Donald
```

## 2 Map 方法

### set(key, value)

`set(key, value)` 方法如果 `Map` 中不存在该键，则会添加键/值对；如果已存在，则会更新该键的新值。

`map-set-example.js`

```javascript
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
myContacts.set("0100-1111", "Mickey");
console.log(myContacts.size); // 4
```

#### 运行示例:

输出

```
Map {'0100-1111' => 'Mickey', '0100-5555' => 'Jerry', '0100-2222' => 'Donald'}
```

### delete(key)

`delete(key)` 方法从 `Map` 对象中删除一个键/值对；如果删除了该对则返回 true，如果该键不存在则返回 false。

`map-delete-example.js`

```javascript
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
console.log(myContacts.delete("0100-5555")); // true
console.log(myContacts.delete("0100-9999")); // false
console.log(myContacts.size); // 2
```

#### 运行示例:

输出

```
true
false
Map {'0100-1111' => 'Tom', '0100-2222' => 'Donald'}
```

### has(key)

`has(key)` 方法测试键是否存在于 `Map` 中。如果存在则返回 true，否则返回 false。

`map-has-example.js`

```javascript
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
console.log(myContacts.has("0100-1111")); // true
console.log(myContacts.has("0100-9999")); // false
```

#### 运行示例:

输出

```
true
false
```

### clear()

`clear()` 方法从 `Map` 对象中移除所有的键/值对。

`map-clear-example.js`

```javascript
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
myContacts.clear();
console.log(myContacts.size); // 0
```

#### 运行示例:

输出

```
0
```

### size

`size` 属性返回 `Map` 中键/值对的数量。

`map-size-example.js`

```javascript
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
console.log(myContacts.size); // 3
```

#### 运行示例:

输出

```
3
```

### entries()

此方法返回一个新的迭代器对象，其中每个条目包含一个两个元素的数组，如 `[key, value]`。

```javascript
var myContacts = new Map();
myContacts.set("0100-1111", "Tom");
myContacts.set("0100-5555", "Jerry");
myContacts.set("0100-2222", "Donald");
var entries = myContacts.entries();
var entry;
while (!(entry = entries.next()).done) {
  var array = entry.value;
  console.log(array);
}
```

运行示例：

输出：

| '0100-1111', 'Tom' |
| :--- |
| '0100-5555', 'Jerry' |
| '0100-2222', 'Donald' |

### keys()

该方法返回一个新的 `Iterator` 对象，帮助你访问 Map 的键。

![](img/image_rsrc8.jpg)

`map-keys-example.js`

```javascript
var data = [["0100-1111", "Tom"], ["0100-5555", "Jerry"], ["0100-2222", "Donald"]];
var myContacts = new Map(data);
var iteratorPhones = myContacts.keys();
var entry;
while (!(entry = iteratorPhones.next()).done) {
  var phone = entry.value;
  console.log(phone);
}
```

运行示例：

输出：

| 0100-1111 |
| :--- |
| 0100-5555 |
| 0100-2222 |

### values()

该方法返回一个新的 `Iterator` 对象，帮助你访问 Map 的值。

![](img/image_rsrc8.jpg)

`map-values-example.js`

```javascript
var data = [["0100-1111", "Tom"], ["0100-5555", "Jerry"], ["0100-2222", "Donald"]];
var myContacts = new Map(data);
var iteratorNames = myContacts.values();
var entry;
while (!(entry = iteratorNames.next()).done) {
  var name = entry.value;
  console.log(name);
}
```

### forEach(callbackFn [, thisArg])

该方法会为 Map 对象的每个“键/值对”调用一次 `callbackFn` 函数。

```javascript
myMap.forEach(callback[, thisArg])
```

参数：

- `callbackFn` - 该函数会对应 Map 的每个“键/值对”调用一次。
- `thisArg` - 在执行 `callbackFn` 时该参数的用法所示。

`map-forEach-example.js`

```javascript
var showContact = function(key, value, thisMap) {
  console.log("Phone: " + key + ". Name: " + value);
}
var data = [["0100-1111", "Tom"], ["0100-5555", "Jerry"], ["0100-2222", "Donald"]];
var myContacts = new Map(data);
// 或者调用：myContacts.forEach(showContact)
myContacts.forEach(showContact, myContacts);
```

运行示例：

输出：

| Phone: 0100-1111. Name: Tom |
| :--- |
| Phone: 0100-5555. Name: Jerry |
| Phone: 0100-2222. Name: Donald |

## 3 WeakMap

基本上，`WeakMap` 与 `Map` 非常相似，但存在以下差异：

- 它的键必须是对象。
- `WeakMap` 的键可以在垃圾回收过程中被消除，这是一个移除程序中不再使用的对象的独立过程。
- `WeakMap` 不支持 `size` 属性，因此你无法知道它有多少个元素。
- `Map` 类中提供的许多方法，但 `WeakMap` 类没有这些方法，例如 `values()`、`keys()`、`entries()`、`clear()` 等。

创建一个 `WeakMap` 对象。

```javascript
var map2 = new WeakMap([iteratorObject])
```

参数：

- `iteratorObject` - 任何可迭代的对象。

方法：

`WeakMap` 的方法数量少于 `Map` 的方法：

- `WeakMap.delete(key)`
- `WeakMap.get(key)`
- `WeakMap.has(key)`
- `WeakMap.set(key, value)`

`WeakMap` 中的键必须是对象。不能是原始类型（Primitive）。

```javascript
let w = new WeakMap();
w.set('a', 'b'); // Uncaught TypeError: 使用无效的值作为 weak map key
let m = new Map();
m.set('a', 'b'); // 正常工作
```

`weakmap-example.js`

```javascript
var key1 = {}; // 一个对象
var key2 = {foo: "bar"};
var key3 = {bar: "foo"};
var data = [[key1, "Tom"], [key2, "Jerry"], [key3, "Donald"]];
var myWeakMap = new WeakMap(data);
console.log(myWeakMap.get(key1));
```

# 第 20 章：理解可迭代对象和迭代器

## 1 迭代 (Iteration)

## 2 迭代器 (Iterator) 概念

## 3 可迭代对象 (Iterable) 概念

ECMAScript 提供了一种与数据结构交互的新方式。现在我们来澄清。

你需要区分两个概念：

- **迭代器 (Iterator)**
- **可迭代对象 (Iterable)**

### 2 迭代器

在 ECMAScript 中，如果一个对象包含指向下一个元素的指针，则它被称为**迭代器**。迭代器具有一个 `next()` 方法，该方法返回一个包含 `value` 和 `done` 属性的对象。如果迭代已完成，`done` 为 `true`，否则为 `false`。

![](img/image_rsrc8.jpg)

`iterator-object-example.js`

```javascript
// 一个对象
let myObject = {
  prop1: "某个值",
  [Symbol.iterator]: function() {
    console.log("我是迭代器");
    return {
      next: function() {
        return {value: "some value", done: true};
      }
    };
  }
};
```

### 3 可迭代对象

在语言层面，如果一个对象包含一个集合，并提供了一种公开该集合的方法，则它被称为**可迭代对象**。例如，数组就是可迭代对象，因为它包含元素集合。

技术上，在 ECMAScript 中，被称为**可迭代对象**的对象必须有一个 `Symbol.iterator` 键，该键的方法返回一个迭代器对象。

`object-with-properties.js`

```javascript
// 一个对象
let myObject = {
  prop1: "某个值 1",
  prop2: "某个值 2",
  prop3: "一百",
  [Symbol.iterator]: function() {
    console.log("我是迭代器");
    return {
      next: function() {
        return {value: "某个值", done: true};
      }
    };
  }
};
```

```html
<!DOCTYPE html>
<html>
<head>
  <title>Some Page</title>
  <meta charset="UTF-8">
</head>
<body onload="alert('menubar.visible? ' + menubar.visible)">
  <h3>Some Page</h3>
  <p>1</p>
  <p>1 2</p>
  <p>1 2 3</p>
</body>
</html>
```

# 第 22 章：JavaScript JSON

## 1. 什么是 JSON

## 2. `JSON.parse(..)`

## 3. `JSON.stringify(..)`

### 1 什么是 JSON

如你所知，数据始终通过互联网环境从一台计算机传输到另一台计算机，并在发送之前封装成特定的格式。接收者必须理解这种格式才能分析原始数据。

`XML` 是一种非常常用的存储和传输数据的格式。

![](img/image_rsrc8TW.jpg)

JSON 代表 JavaScript 对象表示法（JavaScript Object Notation）。它也是一种存储和传输数据的格式。JSON 格式源于 JavaScript 的对象语法，因此它继承了简单性，并且完全基于文本。

![](img/image_rsrc8TX.jpg)

下面是一个在 Javascript 中声明对象的代码片段：

#### Javascript 对象

```javascript
var aCompany = {
  name: "Amazon",
  ceo: "Jeff Bezos",
  employees: [
    {firstName: "John", lastName: "Doe"},
    {firstName: "Anna", lastName: "Smith"},
    {firstName: "Peter", lastName: "Jones"}
  ]
};
```

以及以 JSON 格式存储的相同数据：

#### JSON 数据

```json
{
  "name": "Amazon",
  "ceo": "Jeff Bezos",
  "employees": [
    {"firstName": "John", "lastName": "Doe"},
    {"firstName": "Anna", "lastName": "Smith"},
    {"firstName": "Peter", "lastName": "Jones"}
  ]
}
```

#### JSON 的优点：

* JSON 是一种轻量级的数据交换格式。
* JSON 数据自包含描述，因此每个人都能轻松理解。
* JSON 是一种独立的语言，也是一种文本。你可以使用任何语言来读取或创建 JSON 数据。大多数编程语言都有用于读写 JSON 库。

### 示例：

```javascript
// JSON 对象: {"firstName":"John", "lastName":"Doe"}
// JSON 数组: [{"firstName":"John", "lastName":"Doe"},{"firstName":"Anna", "lastName":"Smith"},{"firstName":"Peter", "lastName":"Jones"}]
```

#### Note：

JSON 纯粹是一种数据格式——它只包含属性，不包含方法。

JSON 要求在字符串和属性名周围使用双引号。单引号是无效的。

即使是一个位置放置错误的逗号或冒号，也可能导致 JSON 文件出错并无法工作。你应该仔细地验证你正尝试使用的任何数据。

### 2 `JSON.parse(..)`

使用 `JSON.parse(text)` 方法可以帮你解析 JSON 数据并将其转换为对象。

`json-parse-example.js`

```javascript
var text = '{ ' +
  ' "name": "Amazon", ' +
  ' "ceo" : "Jeff Bezos", ' +
  ' "employees" : [' +
  '    { "firstName":"John" , "lastName":"Doe" },' +
  '    { "firstName":"Anna" , "lastName":"Smith" },' +
  '    { "firstName":"Peter" , "lastName":"Jones" } ' +
  '  ] ' +
  '}';
var obj = JSON.parse(text);
console.log(obj.employees);
console.log(obj.ceo); // Jeff Bezos
console.log(obj.employees[0].firstName); // John
console.log(obj.employees[1].firstName); // Anna
console.log(obj.employees[2].firstName); // Peter
```

![](img/image_rsrc8TY.jpg)

`json-parse-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>JSON.parse</title>
</head>
<body>
  <div style="border:1px solid #ccc;padding:5px;">
    <h3 id="name"></h3>
    <i id="location"></i>
  </div>
  <script>
    var s = '{"firstName" : "Sammy", "lastName" : "Shark", "location" : "Ocean"}';
    var obj = JSON.parse(s);
    document.getElementById("name").innerHTML = obj.firstName + " " + obj.lastName;
    document.getElementById("location").innerHTML = obj.location;
  </script>
</body>
</html>
```

![](img/image_rsrc8TZ.jpg)

### 3 `JSON.stringify(..)`

使用 `JSON.stringify(obj)` 方法可以帮你将 Javascript 对象转换为 JSON 格式的文本。

`json-stringify-example1.js`

```javascript
var obj = {name: "tran", age: 39};
var text = JSON.stringify(obj);
console.log(text); // {"name":"tran","age":39}
```

#### `JSON.stringify(obj)`

`JSON.stringify(obj)` 方法用于将 `obj` 转换为 `String`。如果 `obj` 对象具有 `toJSON()` 方法，将调用该方法来返回 `String`。相反，它将按照默认规则进行转换：

* 数字、布尔、字符串将转换为原始值。
* `Infinity`、`NaN` 将转换为 `null`。
* 如果 `obj` 是 `undefined`、`Function`、`Symbol`，它将转换为 `undefined`。
* 如果对象中出现 `undefined`、`Function`、`Symbol`，它们将被跳过。
* 如果数组中出现 `undefined`、`Function`、`Symbol`，它们将被转换为 `null`。
* 所有具有如 `Symbol` 等键的属性将被跳过。
* `Date` 对象具有 `toJSON()` 方法，返回的是字符串（例如 `date.toISOString()`），因此它被处理为字符串。

`json-stringify-example2.js`

```javascript
var obj = {
  name: "tran",
  age: 39,
  // 对象中的函数会被忽略
  sayHello: function() {
    console.log("Hello");
  },
  // 数组中的 undefined, Symbol, function 将转换为 null.
  "others": ["1", Symbol(), undefined, function(){}, "2"]
};
var text = JSON.stringify(obj);
console.log(text); // {"name":"tran","age":39,"others":["1",null,null,null,"2"]}
```

### 示例：

`json-stringify-example.js`

```javascript
JSON.stringify({});                   // '{}'
JSON.stringify(true);                // 'true'
JSON.stringify('foo');               // '"foo"'
JSON.stringify([1, 'false', false]);    // '[1,"false",false]'
JSON.stringify([NaN, null, Infinity]); // '[null,null,null]'
```

```javascript
var obj = {
  name: "Tom",
  gender: "Male",
  company: "Walt Disney",
  friends: [
    {name: "Jerry", gender: "Male"},
    {name: "Donald", gender: "Male"}
  ]
};
var replacer = ["name", "friends"];
var json = JSON.stringify(obj, replacer);
console.log(json); // {"name":"Tom","friends":[{"name":"Jerry"},{"name":"Donald"}]}
```

使用函数作为 `replacer` 参数示例：

`json-stringify-replacer-example2.js`

```javascript
function replacer(key, value) {
  console.log(typeof key);
  console.log(key);
  // 过滤属性
  if (typeof value === 'string') {
    return undefined;
  }
  return value;
}
var obj = {foundation: 'Mozilla', model: 'box', week: 45, transport: 'car', month: 7};
var json = JSON.stringify(obj, replacer);
console.log(json); // '{"week":45,"month":7}'
```

# 第 23 章：JavaScript 事件处理

## 1. JavaScript 事件

## 2. 事件示例

事件是表示某些事情发生的信号。例如，你点击了一个按钮，或者你关闭了浏览器……所有 DOM 节点都会产生此类信号，但除了 DOM 还有其他事件，例如你关闭浏览器窗口的事件。

以下是最实用的 DOM 事件列表：

### 鼠标事件：

| 事件 | 说明 |
| :--- | :--- |
| `click` | 当用户点击元素时触发的事件 |
| `contextmenu` | 当用户在元素上右键点击以打开上下文菜单时触发事件 |
| `dblclick` | 当用户双击元素时触发的事件 |
| `mousedown` | 当用户在元素上按下鼠标键时触发事件 |
| `mouseup` | 当用户在元素上释放鼠标键时触发事件 |
| `mouseenter` | 当指针移动到元素上时触发事件 |
| `mouseleave` | 当指针移出元素时触发触发事件 |
| `mousemove` | 当指针在元素上移动时触发事件 |
| `mouseout` | 当用户将鼠标指针移出元素，或移出其任一子元素时触发事件 |
| `mouseover` | 当指针移动到元素或移动到其任一子元素时触发事件 |

### 表单元素事件：

| 事件 | 说明 |
| :--- | :--- |
| `submit` | 当用户提交 `<form>` 时触发 |
| `focus` | 当用户聚焦某个元素（例如 `<input>`）时触发 |
| `blur` | 当用户离开某个元素（例如 `<input>`）时触发 |

### 键盘事件：

| 事件 | 说明 |
| :--- | :--- |
| `keydown` | 当用户按下键时触发的事件 |
| `keyup` | 当用户释放键时触发的事件 |
| `keypress` | 当用户按下键时触发的事件 |

### 文档事件：

| 事件 | 说明 |
| :--- | :--- |
| `DOMContentLoaded` | 当 HTML 内容加载并处理完成后触发。DOM 模型已完全创建。 |

### CSS 事件：

| 事件 | 说明 |
| :--- | :--- |
| `animationstart` | 当 CSS 动画开始时触发的事件 |
| `animationend` | 当 CSS 动画完成时触发的事件 |
| `animationiteration` | 当 CSS 动画重复时触发的事件 |

### 事件处理：

要处理事件，你需要将事件绑定到处理器（handler）上。处理器可以是一个函数。当事件发生时，将调用该处理器进行操作。处理器是运行与用户动作对应的 JavaScript 代码的一种。

可以在 HTML 中通过 `on{event}` 属性设置处理器。例如，点击事件：

```html
<input value="Click me" onclick="alert('Click!')" type="button">
<input value="Click me" onclick="someFunction()" type="button">
```

`this` 对象代表产生事件元素。

```html
<input value="Click me" onclick="someFunction(this)" type="button">
```

当事件发生时，JavaScript 会创建一个 `event` 对象，你可以将其作为参数的值使用。

```html
<input value="Click me" onclick="someFunction(event)" type="button">
```

你也可以通过 `event` 对象访问产生事件元素。

```javascript
var target = event.target;
```

## 2. 事件示例

简单且经常遇到的事件是用户点击元素的事件。下面是一个简单的示例。用户点击 `=` 按钮来计算两个数字之和。

![](img/image_rsrc8U0.jpg)

`onclick-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Hello Javascript</title>
  <script type="text/javascript">
    function doCalculate() {
      var a = document.getElementById("a").value; // 一个字符串值
      var b = document.getElementById("b").value; // 一个字符串值
      var c = Number(a) + Number(b);
      document.getElementById("c").value = c;
    }
  </script>
</head>
<body>
  <h3>Click Event example</h3>
  <input id="a" type="text" value="100"/> <br/>
  + <br/>
  <input id="b" type="text" value="200"/> <br/>
  = <br/>
  <input id="c" type="text"/>
  <button onclick="doCalculate()">Calculate</button>
</body>
</html>
```

`this` 对象代表产生事件元素。

`this-obj-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Event Example</title>
  <script type="text/javascript">
    function changeSize(evt) {
      var target = evt.target;
      var random = Math.round(Math.random() * 100) + 100;
      target.style.width = random + "px";
      target.style.height = random + "px";
    }
  </script>
</head>
<body>
  <h3>Access 'target' object via 'event' object</h3>
  <button onclick="changeSize(event)">Click Me to Change Size</button>
</body>
</html>
```

`mouse-events-example.js`

```javascript
var enterCount = 0;
var moveCount = 0;
var leaveCount = 0;

function mouseleaveHandler(evt) {
  leaveCount += 1;
  showPosition(evt);
}
function mouseenterHandler(evt) {
  enterCount += 1;
  showPosition(evt);
}
function mousemoveHandler(evt) {
  moveCount += 1;
  showPosition(evt);
}
function showPosition(evt) {
  var html = "offsetX: " + evt.offsetX + "<br/>" + "offsetY: " + evt.offsetY;
  document.getElementById("position-div").innerHTML = html;
}
function showStatistics() {
  var html = "enterCount:" + enterCount + "<br/>" + "moveCount:" + moveCount + "<br/>" + "leaveCount:" + leaveCount;
  document.getElementById("statistics-div").innerHTML = html;
}
```

`mouse-events-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Javascript Events</title>
  <style>
    .my-div {
      width: 100px;
      height: 100px;
      background: blue;
    }
  </style>
</head>
<body>
  <h3>Mouse Events (Enter, Move, Leave)</h3>
  <div class="my-div" onmouseenter="mouseenterHandler(event)" onmouseleave="mouseleaveHandler(event)" onmousemove="mousemoveHandler(event)">
    Hover over me
  </div>
  <h3>Mouse position</h3>
  <div id="position-div"></div>
  <h3>Statistics</h3>
  <div id="statistics-div"></div>
  <script src="mouse-events-example.js"></script>
</body>
</html>
```

`event-obj-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Event Example</title>
  <script type="text/javascript">
    function changeSize(evt) {
      var target = evt.target;
      var random = Math.round(Math.random() * 100) + 100;
      target.style.width = random + "px";
      target.style.height = random + "px";
    }
  </script>
</head>
<body>
  <h3>Access 'target' object via 'event' object</h3>
  <button onclick="changeSize(event)">Click Me to Change Size</button>
</body>
</html>
```

（由于原文在某些示例中存在部分乱码，我已根据逻辑补全了对应的 HTML 结构以确保翻译清晰：

*注：原文后半部分存在大量重复和断裂的 HTML 代码，已根据代码逻辑进行了整理翻译。*）

```html
<!DOCTYPE html>
<html>
<head>
  <title>事件示例</title>
  <script type="text/javascript">
    function changeSize(borderColor, target, evt, bgColor) {
      var random = Math.round(Math.random() * 100) + 100;
      target.style.width = random + "px";
      target.style.height = random + "px";
      target.style.borderColor = borderColor;
      target.style.backgroundColor = bgColor;
    }
  </script>
</head>
<body>
  <h3>处理器具有多个参数</h3>
  <a href="">重置</a> <br/><br/>
  <button onclick="changeSize('red', this, event, 'green')">点击我</button>
</body>
</html>
```

# 第 24 章：Javascript 鼠标事件（MouseEvent）

## 1 鼠标事件

`MouseEvent` 是一个接口，代表用户与指针设备（如鼠标）交互时发生的事件，常见事件包括 `click`、`dbclick`、`mousedown`、`mouseup` 等。

`MouseEvent` 是 `UIEvent` 的子接口。

![](img/image_rsrc8U3.jpg)

### MouseEvent 的事件类型：

| 事件 | 说明 |
| :--- | :--- |
| `click` | 用户点击元素时触发事件 |
| `contextmenu` | 用户在元素上点击右键以打开右键菜单时触发事件 |
| `dblclick` | 用户双击元素时触发事件 |
| `mousedown` | 用户在元素上按下鼠标按钮时触发事件 |
| `mouseup` | 用户在元素上释放鼠标按钮时触发事件 |
| `mouseenter` | 指针移动到元素内部时触发事件 |
| `mouseleave` | 指针移出元素外部时触发事件 |
| `mousemove` | 当针在元素或其子元素上移动时，持续触发事件。 |
| `mouseout` | 当用户将鼠标指针移出元素，或移出其子元素之一时触发事件 |
| `mouseover` | 指针移动到元素内部或其某个子元素内部时触发事件 |

### `mousedown`, `mouseup`, `click`

让我们从鼠标事件中最常见的 `click` 事件开始。它由按下和释放组成。`click` 事件如下所示：

![](img/image_rsrc8U4.jpg)

### `dbclick`

如果你快速点击 2 次，它将创建一个 `dbclick` 事件。

### `mouseover` vs `mouseenter`

`mouseenter` 事件在光标进入元素时触发。`mouseover` 事件在光标进入元素或其任一子元素时触发。

![](img/image_rsrc8U5.jpg)

### `mouseleave` vs `mouseout`

`mouseleave` 事件在光标移出元素时触发。`mouseout` 事件在光标移出元素或其任一子元素时触发。

![](img/image_rsrc8U6.jpg)

以下示例可以帮助你对比 `mouseenter` 与 `mouseover`，`mouseleave` 与 `mouseout`：

![](img/image_rsrc8U7.jpg)

`enter-vs-over-leave-vs-out.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Javascript 鼠标事件</title>
  <script src="enter-vs-over-leave-vs-out.js"></script>
  <style>
    #target-div {width: 320px;height: 150px;background: blue;}
    #target-div > div {width: 50px;height: 80px;margin: 40px 0 0 40px;padding: 5px 0 0 5px;float: left;background: yellow;}
  </style>
</head>
<body>
  <h3>mouseenter vs mouseover</h3>
  <h3>mouseleave vs mouseout</h3>
  <div id="target-div" onmouseenter="mouseenterHandler(event)" onmouseover="mouseoverHandler(event)" onmouseleave="mouseleaveHandler(event)" onmouseout="mouseoutHandler(event)">
    <div>子元素</div>
    <div>子元素</div>
    <div>子元素</div>
  </div>
  <h3>统计数据：</h3>
  <div style="color:red;" id="statistics-div"></div>
</body>
</html>
```

`enter-vs-over-leave-vs-out.js`

```javascript
var enterCount = 0;
var overCount = 0;
var leaveCount = 0;
var outCount = 0;
function mouseenterHandler(evt) {
  enterCount += 1;
  showStatistics();
}
function mouseoverHandler(evt) {
  overCount += 1;
  showStatistics();
}
function mouseleaveHandler(evt) {
  leaveCount += 1;
  showStatistics();
}
function mouseoutHandler(evt) {
  outCount += 1;
  showStatistics();
}
function showStatistics() {
  var html = "enterCount:" + enterCount + "<br/>" +
             "overCount:" + overCount + "<br/>" +
             "leaveCount:" + leaveCount + "<br/>" +
             "outCount:" + outCount;
  document.getElementById("statistics-div").innerHTML = html;
}
```

### `mousemove`

![](img/image_rsrc8U8.jpg)

`mousemove-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Javascript 鼠标事件</title>
  <script src="mousemove-example.js"></script>
  <style>
    #target-div {width: 320px;height: 150px;background: blue;margin-bottom: 50px;}
    #target-div > div {width: 50px;height: 150px;margin: 40px 0 0 40px;padding: 5px 0 0 5px;float: left;background: yellow;}
  </style>
</head>
<body>
  <h3>mousemove 示例</h3>
  <div id="target-div" onmousemove="mousemoveHandler(event)">
    <div>子元素</div>
    <div>子元素</div>
    <div>子元素</div>
  </div>
  <h3>统计数据：</h3>
  <div style="color:red;" id="statistics-div"></div>
</body>
</html>
```

`mousemove-example.js`

```javascript
var moveCount = 0;
function mousemoveHandler(evt) {
  moveCount += 1;
  showStatistics();
}
function showStatistics() {
  var html = "moveCount:" + moveCount;
  document.getElementById("statistics-div").innerHTML = html;
}
```

## 2 属性与方法

`MouseEvent` 是 `UIEvent` 的子接口，因此它继承了这些属性和方法。

### Key（键）

| 属性 | 说明 |
| :--- | :--- |
| `altKey` | 按 ALT 键时触发事件则为 true。 |
| `ctrlKey` | 按 CTRL 键时触发事件则为 true。 |
| `shiftKey` | 按 SHIFT 键时触发事件则为 true。 |
| `metaKey` | 按 META 键时触发事件则为 true。 |

### `ctrlKey` 属性示例：

![](img/image_rsrc8U9.jpg)

`prop-ctrlKey-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>Javascript 鼠标事件</title>
  <style>#target-div {width: 320px;height: 150px;background: blue;margin-bottom: 10px;}</style>
  <script>
    function clickHandler(evt) {
      var html = "evt.ctrlKey=" + evt.ctrlKey;
      document.getElementById("log-div").innerHTML = html;
    }
  </script>
</head>
<body>
  <h3>按下 Ctrl 键并点击</h3>
  <div id="target-div" onclick="clickHandler(event)"></div>
  <div style="color:red;" id="log-div"></div>
</body>
</html>
```

### 位置（Position）：

| 属性 | 说明 |
| :--- | :--- |
| `clientX` | 相对于窗口的水平坐标。 |
| `clientY` | 相对于窗口的垂直坐标。 |
| `offsetX` | 相对于元素边缘的水平坐标。 |
| `offsetY` | 相对于元素边缘的垂直坐标。 |
| `pageX` | 相对于文档的水平坐标。 |
| `pageY` | 相对于文档的垂直坐标。 |
| `screenX` | 相对于屏幕（设备）的水平坐标。 |
| `screenY` | 相对于屏幕（设备）的垂直坐标。 |
| `movementX` | 相对于上一次鼠标移动位置的水平坐标。 |
| `movementY` | 相对于上一次鼠标移动位置的垂直坐标。 |

![](img/image_rsrc8UA.jpg)

![](img/image_rsrc8UB.jpg)

`prop-positions-example.html`



```html
<!DOCTYPE html>
<html>
<head>
  <title>Javascript 鼠标事件</title>
  <script src="prop-positions-example.js"></script>
  <style>#target-div {width: 300px;height: 210px;background: #ccc;margin: 0px 0px 10px 20px;padding: 5px;}</style>
</head>
<body style="height:450px; width:1000px;">
  <h3>位置</h3>
  <div id="target-div" onmousemove="mousemoveHandler(event)"></div>
</body>
</html>
```

`prop-positions-example.js`

```javascript
function mousemoveHandler(evt) {
  var html = "offsetX = " + evt.offsetX + "<br/>" + "offsetY = " + evt.offsetY + "<br/>" + "clientX = " + evt.clientX + "<br/>" + "clientY = " + evt.clientY + "<br/>" + "pageX = " + evt.pageX + "<br/>" + "pageY = " + evt.pageY + "<br/>" + "screenX = " + evt.screenX + "<br/>" + "screenY = " + evt.screenY + "<br/>" + "movementX = " + evt.movementX + "<br/>" + "movementY = " + evt.movementY;
  document.getElementById("target-div").innerHTML = html;
}
```

### Button

| Property | Description |
| :--- | :--- |
| button | 返回一个数字，描述在鼠标事件触发时按下了哪个鼠标键 |
| buttons | 返回一个数字，描述在鼠标事件触发时按下了哪些鼠标键 |

### `event.button`:

- 0: 主键，通常是左键或未初始化状态
- 1: 辅助键，通常是滚轮键或中间键（如果存在）
- 2: 次键，通常是右键
- 3: 第四键，通常是浏览器的后退按钮
- 4: 第五键，通常是浏览器的前进按钮

### `event.buttons`:

- 0 : 无按键按下或未初始化
- 1 : 主键，通常是左键。
- 2 : 次键，通常是右键。
- 4 : 辅助键，通常是鼠标滚轮键或中间键。
- 8 : 第四键，通常是“浏览器后退”按钮。
- 16 : 第五键，通常是“浏览器前进”按钮。

`event.buttons` 可能会返回上述值之外的不同值。例如，当你同时按下左鼠标和右鼠标时，`event.buttons` 将返回 `3`。

`prop-button-buttons-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>MouseEvent Example</title>
  <script>
    function mousedownHandler(evt) {
      var logDiv = document.getElementById("log-div");
      logDiv.innerHTML = "event.button= " + evt.button + "<br/>" + "event.buttons= " + evt.buttons;
    }
  </script>
</head>
<body>
  <h3>event.button, event.buttons</h3>
  <button onmousedown="mousedownHandler(event)">点击我!</button>
  <br/><br/>
  <div id="log-div" style="color:red;"></div>
</body>
</html>
```

!![](img/image_rsrc8UC.jpg)

# 第 25 章：Javascript WheelEvent

## 1 WheelEvent

`WheelEvent` 是一个接口，表示当用户移动滚轮或类似设备时发生的事件。

`WheelEvent` 意味着 `MouseEvent` 的子接口。它将继承父接口的所有属性和方法。

!![](img/image_rsrc8UD.jpg)

| Event | Description |
| :--- | :--- |
| wheel | 当鼠标滚轮在元素上向上或向下滚动时触发的事件 |

### WheelEvent 的属性：

| Property | Description |
| :--- | :--- |
| deltaX | 返回鼠标滚轮的水平滚动量（x 轴） |
| deltaY | 返回鼠标滚轮的垂直滚动量（y 轴） |
| deltaZ | 返回鼠标滚轮在 z 轴上的滚动量 |
| deltaMode | 返回一个代表 delta 值测量单位的数字（DOM_DELTA_PIXEL, DOM_DELTA_PIXEL, DOM_DELTA_PAGE） |

### 使用 WheelEvent 的示例：

!![](img/image_rsrc8UE.jpg)
!![](img/image_rsrc8UF.jpg)

`wheelevents-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>WheelEvent Example</title>
  <script src="wheelevents-example.js"></script>
</head>
<body>
  <h3>WheelEvent 示例</h3>
  <div style="font-size:12px; padding:5px; border:1px solid #ccc;" onwheel="wheelHandler(event)">大家好！<div></div></div>
</body>
</html>
```

`wheelevents-example.js`

```javascript
function wheelHandler(evt) {
  var fontSize = evt.target.style.fontSize;
  // 12px, 13px,...
  var value = Number(fontSize.substr(0, fontSize.length-2)); // 12, 13,..
  // 向上滚动
  if (evt.deltaY < 0) {
    if (value < 50) {
      value++;
    }
  }
  // 向下滚动
  if (evt.deltaY > 0) {
    if (value > 5) {
      value--;
    }
  }
  evt.target.style.fontSize = value + "px";
}
```

!![](img/image_rsrc8UG.jpg)

# 第 26 章：Javascript KeyboardEvent

## 1 KeyboardEvent

## 2 属性与方法

## 3 表：Key, KeyCode

### 1 KeyboardEvent

`KeyboardEvent` 是一个接口，表示用户与键盘交互时发生的事件，包括 `keydown`, `keypress`, `keyup` 事件。

`KeyboardEvent` 是 `UIEvent` 的子接口。

!![](img/image_rsrc8UH.jpg)

| Order | Event |
| :--- | :--- |
| 1 | onkeydown |
| 2 | onkeypress |
| 3 | onkeyup |

### keydown

当你按下按键时，会触发 `keydown` 事件。在 Windows OS 中，如果你持续按住按键，它会不断发出 `keydown` 和 `keypress` 事件。但在 MacOS 中，如果你持续按住按键，它会不断发出 `keydown` 事件。如下所示。

!![](img/image_rsrc8UJ.jpg)

### keypress

`keypress` 发生在 2 种情况，其中情况 1 如我上面所述的（查看 `keydown` 事件）。情况 2 是你按下按键并释放。

!![](img/image_rsrc8UK.jpg)

### keyup

当你释放按键时，会触发 `keyup` 事件。注意：如果你想检测按键被触发了，可以使用 `keydown`、`keypress` 或 `keyup` 属性。

`keyevents.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>KeyEvent Example</title>
  <script src="keyevents.js"></script>
</head>
<body>
  <h3>KeyEvent 示例</h3>
  <input type="text" onkeydown="keydownHandler(event)" onkeyup="keyupHandler(event)" onkeypress="keypressHandler(event)"/>
  <br/><br/>
  <textarea rows="10"></textarea>
  <br/>
  <button onclick="clearLog()">清除</button>
</body>
</html>
```

`keyevents.js`

!![](img/image_rsrc8UM.jpg)

### 2 属性与方法

`Keyboard` 是 `UIEvent` 的子接口，因此，它继承了该接口的属性和方法。

| Property | Description |
| :--- | :--- |
| altKey | 当事件发生时，如果 `ALT` 键被按下，则返回 true |
| ctrlKey | 当事件发生时，如果 `CTRL` 键被按下，则返回 true |
| shiftKey | 当事件发生时，如果 `SHIFT` 键被按下，则返回 true |
| metaKey | 当事件发生时，如果 `META` 键被按下，则返回 true |

示例：按下 `SHIFT` 键并保持不变，然后按下任意键。

!![](img/image_rsrc8UN.jpg)

`prop-shiftkey-example.html`

```html
<!DOCTYPE html>
<html>
<head>
  <title>KeyEvent Example</title>
  <script src="prop-shiftkey-example.js"></script>
</head>
<body>
  <h3>按住 'SHIFT' 键并按下任意键！</h3>
  <input type="text" onkeydown="keydownHandler(event)"/>
  <br/><br/>
  <div id="log-div" style="color:red;"></div>
</body>
</html>
```

`prop-shiftkey-example.js`

```javascript
function keydownHandler(evt) {
  if (evt.shiftKey) {
    document.getElementById("log-div").innerHTML = "evt.shiftKey = true;";
  } else {
    document.getElementById("log-div").innerHTML = "evt.shiftKey = false";
  }
}
```

# 第 27 章：Javascript FocusEvent

### 1 FocusEvent

### 2 focusin, focusout

#### 1 FocusEvent

`FocusEvent` 是一个接口，表示与焦点相关的事件，即 `focus`、`focusin`、`blur`、`focusout` 等 4 个事件。

!![](img/image_rsrc8UP.jpg)

### 属性：

| Property | Description |
| :--- | :--- |
| relatedTarget | 返回与触发事件相关的元素 |

如果你跳转到一个元素然后离开（聚焦到另一个元素），将按顺序发生 4 个事件：

- focus
- focusin
- blur
- focusout

!![](img/image_rsrc8UR.jpg)

`focus` 事件发生在 `focusin` 之前。事实上，它们发生的时间非常接近，可以被看作是同时发生的。同样，`blur` 事件发生在 `focusout` 之前，事实上，它们发生的时间非常接近，可以被看作是同时发生的。

### focus

当你从其他地方跳转到某个元素时会触发 `focus` 事件，例如进入 `<input>` 元素准备为该元素输入内容。

### blur

`blur` 事件发生在你跳出一个元素（聚焦到另一个元素）时。

### `focusevent-example.html`

```html
<!DOCTYPE html><html><head><title>FocusEvent</title><script>function focusHandler(evt)  {showLog("focus");}function blurHandler(evt)  {showLog("blur");}function showLog(msg)  {var oldHtml= document.getElementById("log-div").innerHTML;document.getElementById("log-div").innerHTML=oldHtml + " .. "+ msg;}</script></head><body><h3>Test events: focus, blur</h3><input type="text"onfocus="focusHandler(event)"onblur="blurHandler(event)"  /><br><br><div id="log-div" style="padding:10px;border:1px solid #ccd;"></div></body></html>
```

| ![](img/image_rsrc8US.jpg) |

### 2 focusin, focusout

`focus`、`blur` 事件为“可聚焦”的元素设计，例如 `<input>`、`<textarea>` 等。而 `focusin`、`focusout` 事件为可以包含其他元素的元素设计，例如 `<div>`、`<span>`、`<form>` 等。

### focus vs focusin

| ![](img/image_rsrc8UT.jpg) |

假设有一个有一个 2 个 `<input>` 子元素的 `<form>`。当用户进入其中一个 `<input>` 元素时，会触发 `focus` 事件。子元素上的 `focus` 事件会在父元素上创建一个 `focusin` 事件。因此，这个 `focusin` 事件会在 `<form>` 元素上发生。

注意：虽然 `focusin` 事件发生在父元素上，但 `event.target` 返回的是子元素（触发 focus 事件的元素）。

### blur vs focusout

| ![](img/image_rsrc8UU.jpg) |

假设你有一个 2 个 `<input>` 子元素的 `<form>`。当用户跳出一个 `<input>` 元素时，会触发 `blur` 事件。子元素上的 `blur` 事件会在父元素上创建一个 `focusout` 事件。因此，这个 `focusout` 事件会在 `<form>` 元素上发生。

注意：虽然 `focusout` 事件发生在父元素上，但 `event.target` 返回的是子元素（触发 blur 事件的元素）。

### 示例: focusin & focusout

### `focusin-focusout-example.html`

```html
<!DOCTYPE html><html><head><title>FocusEvent</title><meta charset="utf-8" /><script src="focusin-focusout-example.js"></script><style>form {border: 1px solid #ccc;padding: 10px;display: inline-block;}</style></head><body><h3>Events: focusin & focusout</h3><p>Focus to 'input' and Blur to it</p><form onfocusin="focusinHandler(event)" onfocusout="focusoutHandler(event)">User Name<input type="text" name="username" /><br><br> Email<input type="text" name="email" /></form></body></html>
```

### `focusin-focusout-example.js`

```javascript
function focusinHandler(evt) { // <input>evt.target.style.border="1px solid blue";// <form>evt.target.parentElement.style.border="1px solid red";}function focusoutHandler(evt) { // <input>evt.target.style.border="1px solid black";// <form>evt.target.parentElement.style.border="1px solid black";} 
```

| ![](img/image_rsrc8UV.jpg) |

### 你在 onfocusout 上遇到问题了吗（？？？））

对于 `<input>`、`<textarea>` 等元素，你只需要处理 `focus`、`blur` 事件。`onfocusout` 属性在某些浏览器上对这些元素无效（我在 Firefox 和 Chrome 浏览器上检查过这个问题）。

### `attr-onfocusout-not-working.html`

```html
<!DOCTYPE html><html><head><title>FocusEvent</title><script>function focusHandler(evt)  {showLog("focus");}function focusinHandler(evt)  {showLog("focusin");}function focusoutHandler(evt)  {showLog("focusout");}function blurHandler(evt)  {showLog("blur");}function showLog(msg)  {var oldHtml= document.getElementById("log-div").innerHTML;document.getElementById("log-div").innerHTML=oldHtml + " .. "+ msg;}</script></head><body><h3>为什么 'onfocusout' 属性在 'input' 上不起？</h3><input type="text"onfocus="focusHandler(event)"onblur="blurHandler(event)"onfocusin="focusinHandler(event)"onforcusout="focusoutHandler(event)" />br><br><div id="log-div" style="padding:10px;border:1px solid #ccd;"></div></body></html>
```

| ![](img/image_rsrc8UW.jpg) |

虽然 `onfocusout` 属性在某些浏览器上对 `<input>`、`<textarea>` 等元素无效。但如果你需要，你仍然可以通过以下方式为它们注册 `focusout` 事件：

```javascript
// Javascript 代码：
var myInput = document.getElementById("my-input");
myInput.addEventListener("focus", focusHandler);
myInput.addEventListener("focusin", focusinHandler);
myInput.addEventListener("focusout", focusoutHandler);
myInput.addEventListener("blur", blurHandler);
```

查看完整示例：

### `focusevents-addEventListener-example.html`

```html
<!DOCTYPE html><html><head><title>FocusEvent</title><meta charset="utf-8"/></head><body><h3>Test events: focus, focusin, focusout, blur</h3><input id="my-input" type="text" /><br><br><div id="log-div" style="padding:10px;border:1px solid #ccd;"></div><script src="focusevents-addEventListener-example.js"></script></body></html>
```

### `focusevents-addEventListener-example.js`

```javascript
function focusHandler(evt)  {showLog("focus");}function focusinHandler(evt)  {showLog("focusin");}function focusoutHandler(evt)  {showLog("focusout");}function blurHandler(evt)  {showLog("blur");}function showLog(msg)  {var oldHtml= document.getElementById("log-div").innerHTML;document.getElementById("log-div").innerHTML=oldHtml + " .. "+ msg;}
// Javascript 代码：
var myInput = document.getElementById("my-input");
myInput.addEventListener("focus", focusHandler);
myInput.addEventListener("focusin", focusinHandler);
myInput.addEventListener("focusout", focusoutHandler);
myInput.addEventListener("blur", blurHandler);
```

| ![](img/image_rsrc8UX.jpg) |

# 第 28 章：Javascript InputEvent

### 1 InputEvent

#### 1 InputEvent

`InputEvent` 是一种表示用户在可编辑元素（如 `<input>`、`<textarea>` 或具有 `contenteditable="true"` 属性的元素）上输入数据的接口。

`InputEvent` 是 `UIEvent` 的子接口。

| ![](img/image_rsrc8UY.jpg) |

事件：

| 事件 |  |
| :--- | :--- |
| input | 当元素获取用户输入时发生 |

支持 input 事件的元素示例：

### `inputevents-elements-example.html`

```html
<!DOCTYPE html><<html>><head><title>InputEvent 示例</title><meta charset="UTF-8"><style>*[contenteditable='true']   {height:30px;padding:5px;border:1px solid #ccd;}</style><script>// 注意：event.data 在 Firefox 和 IE 中不支持 function inputHandler(evt)  {showLog(evt.data);}function showLog(text)  {var logDiv = document.getElementById("log-div");logDiv.innerHTML = logDiv.innerHTML + " .. " + text;}</script></head><body><h3>InputEvent 示例</h3><p style="color:red">注意：event.data 在 Firefox 和 IE 中不支持</p><h3>input 元素</h3><input type="text" oninput ="inputHandler(event)"/><<h3>Textarea 元素</h3><textarea oninput ="inputHandler(event)" rows="5" cols="30"></textarea><h3>具有 contenteditable='true' 的元素</h3><div oninput ="inputHandler(event)" contenteditable="true"></div><p id="log-div"></p></body></html>
```

| ![](img/image_rsrc8UZ.jpg) |

#### 事件：input vs change

你也可以考虑使用 `change` 事件，因为它与 `input` 事件非常相似：

*   `change` 事件支持 `<select>` 元素。当用户更改 `<select>` 上的选项时发生。
*   对于 `<input>` (text, number, email, password, tel, time, week, month, date, datetime-local, search, url)、`<textarea>` 元素：`input` 事件在元素值更改后立即发生。而 `change` 事件在元素值更改且元素失去焦点时发生。

## 2 属性、方法

`InputEvent` 是 `UIEvent` 的子接口，因此它继承了 `UIEvent` 的所有方法和属性。此外，它还有自己的方法和属性。

### 属性

| 属性 | 描述 |
| :--- | :--- |
| `data` | 返回插入的字符。如果更改没有插入文本（例如删除字符时），则该可能为空字符串。 |
| `dataTransfer` | 返回一个 `DataTransfer` 对象，包含关于向可编辑内容添加或移除富文本或纯文本数据的信息。 |
| `inputType` | 返回可编辑内容的更改类型，例如'inserting'插入、'deleting'删除、'formatting'格式化等等。 |
| `isComposing` | 返回 true/false，表示事件是否在 `compositionstart` 之后且 `compositionend` 之前触发。 |

# 第 29 章：Javascript ChangeEvent

## 1 ChangeChangeEvent

`change` 事件在以下情况下触发：

*   用户勾选/取消勾选 `<input type="checkbox">`。
*   用户对 `<input type="radio">` 进行了更改。
*   用户更改 `<input>` 的值（文件、颜色、范围）。
*   用户更改了 `<input>` 的内容（文本、数字、邮箱、密码、电话、时间、周、月、日期、本地日期时间、搜索、url），然后聚焦到其他地方。
*   用户更改了 `<textarea>` 的内容，然后聚焦到其他地方。
*   用户更改了 `<select>` 元素的选项。

### 使用 change 事件的示例：

`changeevents-elements-example.html`

```html
<!DOCTYPE html><<html><head><title>ChangeEvent Example</title><meta charset="UTF-8"><style>.title {font-weight:bold;}</style><script>function changeHandler(evt)  {alert("Changed!");}</script></head><body><h2>ChangeEvent example</h2><p class="title">Input (checkbox, radio):</p><input type="checkbox"  onchange ="changeHandler(event)"/><input type="radio" name ="gender" value="M" onchange ="changeHandler(event)"/><input type="radio" name ="gender" value="F" onchange ="changeHandler(event)"/><p class="title">Input (range):</p><input type="range" min ="1" max="10" onchange ="changeHandler(event)"/><p class="title">Input (color):</p><input type="color" onchange ="changeHandler(event)"/><p class="title">Input (file):</p><input type="file" onchange ="changeHandler(event)"/><p class="title">Input (image, hidden, buton, submit, reset):</p>- (Not support 'change' event)<p class="title">Input (text, number, email, password, tel, time, week, month, date, datetime-local, search, url):</p><input type="text" onchange ="changeHandler(event)"/><p class="title">Textarea element</p><textarea onchange ="changeHandler(event)" rows="3" cols="30"></textarea><p class="title">Select:</p><select onchange ="changeHandler(event)"><option value ="en">English</option><option value ="de">German</option><option value ="vi">Vietnamese</option></select><p id="log-div"></p></body></html>
```

| ![](img/image_rsrc8V0.jpg) |

### 在 <select> 元素上使用 change 事件的示例：

`changeevents-select-example.html`

```html
<!DOCTYPE html><<html><head><title>ChangeEvent Example</title><meta charset="UTF-8"><script>function changeHandler(evt)  {alert("Language: " + evt.target.value);}</script></head><body><h2>ChangeEvent example</h2><p class="title">Select Language:</p><select onchange ="changeHandler(event)"><option value ="en">English</option><option value ="de">German</option><option value ="vi">Vietnamese</option></select></body></html>
```

| ![](img/image_rsrc8V1.jpg) |

# 第 30 章：Javascript DragEvent

## 1 DragEvent

`DragEvent` 是一个接口，代表在对象从一个地方拖放到另一个地方过程中发生的事件。用户通过将指针设备（如鼠标）放在对象表面、按下按键、移动指针设备到另一个地方，然后释放指针设备以将对象放置到新位置，从而启动拖放。

| ![](img/image_rsrc8V2.jpg) |
| ![](img/image_rsrc8V3.jpg) |

`DragEvent` 是 `MouseEvent` 的子接口，因此它继承了 `MouseEvent` 的所有属性和方法。

| ![](img/image_rsrc8V4.jpg) |

以下是拖放过程中发生的事件类型列表：

| 事件 | 元素类型 | 描述 |
| :--- | :--- | :--- |
| `dragstart` | 被拖拽元素 | 当用户开始拖动元素时触发事件 |
| `drag` | 被拖拽元素 | 当元素正在被拖拽时触发事件 |
| `dragend` | 被拖拽元素 | 当用户完成元素拖拽时触发事件 |
| `dragenter` | 放置目标 | 当被拖拽元素进入放置目标时触发事件 |
| `dragover` | 放置目标 | 当被拖拽元素位于放置目标上方时触发事件 |
| `drleave` | 放置目标 | 当被拖拽元素离开放置目标时触发事件 |
| `drop` | 放置目标 | 当被拖拽元素放置在放置目标上时触发事件 |

| ![](img/image_rsrc8V5.jpg) |

| 属性 | 描述 |
| :--- | :--- |
| `dataTransfer` | 返回拖拽/放置的数据 |

查看一个简单的示例：

| ![](img/image_rsrc8V6.jpg) |

`dragevents-example.html`

```html
<!DOCTYPE html><<html><head><title>DragEvent Example</title><script src="dragevents-example.js"></script><style>.droptarget-div {float: left;width: 100px;height: 55px;margin: 25px 25px 5px 5px;padding: 10px;border: 1px solid black;}#dragtarget-div {background: #eee;padding: 5px;}</style></head><body><h3>DragEvent example</h3><p id="log-div">..</p><!-- Drop Target 1 --><div class="droptarget-div"ondragenter= "ondragenterHandler(event)"ondragover="dragoverHandler(event)"ondrop="dropHandler(event)"><p id="dragtarget-div"ondragstart="dragstartHandler(event)"ondrag="dragHandler(event)"draggable="true">Drag me!</p></div><!-- Drop Target 2 --><div class="droptarget-div"ondragenter= "ondragenterHandler(event)"ondragover="dragoverHandler(event)"ondrop="dropHandler(event)"></div></body></html>
```

`dragevents-example.js`

```javascript
// --------- “被拖拽元素”的处理函数 ------------------
function dragstartHandler(evt) {
  evt.dataTransfer.setData("MyDraggedId", evt.target.id);
}
// 拖拽中 ...
function dragHandler(evt) {
  showLog("The p element is being dragged");
}
// --------- “放置目标”的处理函数 ------------------
function ondragenterHandler()  
  showLog("The p element enter drop-target");
}
// 在 'over' 期间，你可以'释放鼠标'来'放置'。
function dragoverHandler(evt) {
  evt.preventDefault(); // 重要！！
}
function dropHandler(evt) {
  evt.preventDefault(); // 重要!!
  var elementId = evt.dataTransfer.getData("MyDraggedId");
  evt.target.appendChild(document.getElementById(elementId));
  showLog("The p element was dropped");
}
// -------------------------------------------------------
function showLog(text)  
  document.getElementById("log-div").innerHTML = text;
}
```

例如，用户在电脑上拖动文件并将其到 `<div>` 元素中，你可以读取用户放置的文件的基本信息和内容。

当 `drop` 事件发生时，`event.dataTransfer.files` 返回一个 `FileList` 对象，其中包含一个 `File` 对象列表。

| ![](img/image_rsrc8V7.jpg) |

# 第 31 章：Javascript HashChangeEvent

## 1 HashChangeEvent

Hash 是 URL 的“锚点部分”。它告诉浏览器滚动滚动条，以显示与 Hash 对应的内容区域。

| ![](img/image_rsrc8V8.jpg) |

`hash-example.html`

# 第 32 章：Javascript URL 编码

## 1 Javascript URL 编码

在篇文章，我将向你展示如何使用 Javascript 对 URL 进行编码和解码。

让我们从这个问题开始：“我们如何用 Javascript 对 URL 进行编码？”

实际上，这取决于你想做什么。Javascript 提供了两个函数，即 `encodeURI()` 和 `encodeURIComponent()`。这两个函数之间的区别在于哪些字符会被编码。

- `encodeURI()` 函数编码除 `~!@#$&*()=:/;?+` 之外的所有字符。
- `encodeURIComponent()` 函数编码除 `-_.!~*'()` 之外的所有字符。

因此，如果你想对整个 URL 进行编码，`encodeURI()` 函数将是一个很好的选择，因为 `http://` 不会被编码。否则，如果你打算编码参数的值，可以使用 `encodeURIComponent()` 函数。

但如果你使用 `encodeURIComponent()` 函数对整个 URL 进行编码，你将得到一个不需要的结果。

# 第 33 章：Javascript FileReader

### 1 FileReader

### 2 FileReader 示例

#### 1 FileReader

Javascript 中的 `FileReader` 接口设计用于读取用户计算机上的数据源。

注意：事实上，只有当用户采取允许的操作时，Javascript 才能读取用户计算机上的资源，例如，用户点击 `<input type="file">` 元素选择计算机上的文件，或将文件拖放到浏览器中。

`FileReader` 可以读取 `File`、`Blob` 或 `DataTransfer` 对象（该对象在用户将文件拖入浏览器时获得）。

`FileReader` 的 API 设计与 `XMLHttpRequest` 具有相同的主要目的，因为它们都有加载外部资源等目标。数据是异步读取的，以避免在执行过程中阻塞浏览器。

### 构造函数

```javascript
// 创建一个 FileReader 对象:var fileReader = new FileReader();
```

### 属性

| 属性 | 描述 |
| :--- | :--- |
| `error` | 一个 `DOMException` 对象，描述读取数据源过程中发生的错误。 |
| `readyState` | 一个描述 `FileReader` 状态的数字。可能的值为：0, 1, 2。 |
| `result` | 成功读取后数据源的内容。其格式取决于开始读取时使用的方法。 |

### 事件

在使用 `FileReader` 加载数据源期间，将触发 `ProgressEvent` 中描述的事件，具体如下：

| 事件 | 描述 |
| :--- | :--- |
| `loadstart` | 表示加载数据的过程开始。此事件总是第一个触发。 |
| `progress` | 事件在数据加载期间触发多次，提供中间数据的访问权限。 |
| `error` | 加载失败时触发事件。 |
| `abort` | 当通过 `abort()` 方法取消数据加载时触发事件（该方法在 `XMLHttpRequest` 和 `FileReader` 上可用）。 |
| `load` | 仅在所有数据都已成功读取时触发事件。 |
| `loadend` | 对象完成数据传输时触发事件。在错误、abort 或 load 之后总是触发。 |

### 事件处理器

| 处理器 | 描述 |
| :--- | :--- |
| `onloadstart(progressEvt)` | `loadstart` 事件的处理器。 |
| `onprogress(progressEvt)` | `progress` 事件的处理器。 |
| `onerror(progressEvt)` | `error` 事件的处理器。 |
| `onabort(progressEvt)` | `abort` 事件的处理器。 |
| `onload(progressEvt)` | `load` 事件的处理器。 |
| `onloadend(progressEvt)` | `loadend` 事件的处理器。 |

### 2 FileReader 示例

在此示例中，用户将文件拖放到一个 `<div>` 元素中。`FileReader` 将用于读取用户投放的文件的基本信息和内容。

**filereader-drop-example.html**

```html
<!DOCTYPE html><<html><head><title>FileReader Example</title><meta charset="UTF-8"><script src="filereader-drop-example.js"></script><style>#drop-area {border: 1px solid blue;padding: 15px;margin-top:5px;}</style></head><body><h3>FileReader example</h3><a href="">Reset</a></a><div id="drop-area" ondragover="dragoverHandler(event)" ondrop="dropHandler(event)">Drop one file here</div><output id="log-div"></output></body></html>
```

**filereader-drop-example.js**

```javascript
function dropHandler(evt) {
evt.stopPropagation();
evt.preventDefault();
// FileList 对象.
var files = evt.dataTransfer.files;
if (files.length != 1) {
resetLog();
appendLog("Please drag and drop 1 file!");
return;
}
var file = files[0];
var fileReader = new FileReader();
fileReader.onloadstart = function(progressEvent) {
resetLog();
appendLog("onloadstart!");
var msg = "File Name: " + file.name + "<br>" +"File Size: " + file.size + "<br>" +"File Type: " + file.type;
appendLog(msg);
}
fileReader.onload = function(progressEvent) {
appendLog("onload!");
var stringData = fileReader.result;
appendLog(" ---------------- File Content ----------------: ");
appendLog(stringData);
}
fileReader.onloadend = function(progressEvent) {
appendLog("onloadend!");
// FileReader.EMPTY, FileReader.LOADING, FileReader.DONE
appendLog("readyState = " + fileReader.readyState);
}
fileReader.onerror = function(progressEvent) {
appendLog("onerror!");
appendLog("Has Error!");
}
// 异步读取文件.
fileReader.readAsText(file, "UTF-8"); // fileReader.result -> String.
}
function dragoverHandler(evt) {
evt.stopPropagation();
evt.preventDefault();
// 显式显示这是一个副本.
evt.dataTransfer.dropEffect = 'copy';
}
function resetLog() {
document.getElementById('log-div').innerHTML = "";
}
function appendLog(msg) {
document.getElementById('log-div').innerHTML += "<br>" + msg;
}
```

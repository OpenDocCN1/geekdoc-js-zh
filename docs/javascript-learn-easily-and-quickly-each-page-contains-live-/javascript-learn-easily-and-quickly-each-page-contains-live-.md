
# 轻松快速学习 JavaScript：每页均包含实时代码示例，帮助你简化 JavaScript 学习过程并提升到新水平。

# JS 简介

JavaScript，通常缩写为 JS，是一种多功能的编程语言，主要用于创建网站上的动态内容。它是 Web 开发中与 HTML 和 CSS 并列的重要组成部分。JavaScript 允许开发者添加交互性、操作文档对象模型 (`DOM`) 并响应用户操作，使网页更具吸引力和响应性。

以下是关于 JavaScript 的一些关键点：

1. **客户端脚本**：JavaScript 主要是一种客户端脚本语言，这意味着它运行在用户的浏览器中，而不是服务器上。这允许在不需要重新加载整个网页的情况下进行实时交互。

2. **面向对象**：JavaScript 是一种面向对象的语言，这意味着它使用对象来表示和操作数据。JavaScript 中的对象可以重新定义（如内置对象），也可以由程序员创建。

3. **事件驱动编程**：JavaScript 的优势之一是它能够响应事件，例如用户操作（点击、鼠标移动、键盘输入）。开发者可以定义在特定事件发生时执行的函数，提供动态且交互的用户体验。

4. **跨浏览器兼容性**：JavaScript 支持所有主流浏览器，包括 Chrome、Firefox、Safari 和 Edge。这种跨浏览器兼容性使其成为 Web 开发的可靠选择。

5. **异步编程**：JavaScript 通过回调函数、`Promise` 和 `async/await` 等机制支持异步编程。这允许开发者在不阻塞主执行线程的情况下执行任务，提高 Web 应用程序的响应能力。

6. **库和框架**：JavaScript 拥有丰富的库框架生态系统，如 jQuery、React、Angular、Vue.js。这些工具简化并优化了开发过程，让开发者能够高效地构建复杂的应用程序。

7. **服务端开发**：随着 `Node.js` 的引入，JavaScript 也可以用于服务端开发。这扩展了语言的范围，允许开发者使用 JavaScript 同时进行客户端和服务端的脚本编写。

总而言之，JavaScript 是一种多功能且强大的编程语言，在 Web 开发中起着至关重要的作用，增强了网站的交互性和功能。它的广泛采用和持续发展使其成为 Web 开发者的必备技能。

# JS 输出

“JS Output To”术语在 JavaScript 语境下并不是标准短语。然而，我将解释 JavaScript 通常如何产生输出。在 JavaScript 中，生成输出的主要方式是通过 `console.log()` 等方法以及操作 HTML 元素的内容。让我们来分解一下：

1. **`console.log()`**：这是一个用于调试和向控制台记录信息的方法。它通常在开发期间用于显示值、消息或其他任何信息。例如：

```javascript
console.log("Hello, World!");
```

在这种情况下，文本 "Hello, World!" 将输出到浏览器控制台。

2. **操作 HTML 元素**：JavaScript 也可以用于动态更新网页上 HTML 元素的内容。这通常使用 `DOM`（文档对象模型）来实现。例如：

```javascript
document.getElementById("demo").innerHTML = "Hello World!";
```

# JS 语句

JavaScript 语句是代码的基本单元，允许开发者以计算机可以理解和执行的方式表达算法、逻辑和功能。

1. **构建块**：JavaScript 程序由语句组成；每条语句执行一个操作。

2. **执行顺序**：JavaScript 语句按照它们出现的顺序执行。这种顺序执行是流程控制的基础。

3. **分号**：语句通常以分号 (`;`) 结束。虽然在很多情况下 JavaScript 允许通过换行符分隔语句，但为了清晰起见，加上它们是一个良好习惯。

4. **语句类型**：JavaScript 支持多种类型的语句，包括但不限于：

- 变量声明：`let x = 5;`
- 条件语句：`if (condition) { /* 代码块 */ } else { /* 代码块 */ }`
- 循环语句：`for (let i = 0; i < 5; i++) { /* 代码块 */ }`
- 函数调用：`functionName();`
- 返回语句：`return result;`
- 错误处理语句：`try { /* 代码块 */ } catch (error) { /* 代码块 */ }`

5. **控制流**：JavaScript 程序的控制流由条件语句（如 `if`, `else if`）和循环语句（如 `for`, `while`）决定。这些语句允许开发者根据条件或多次重复语句来控制执行顺序。

6. **函数调用**：JavaScript 中的函数通过作为语句调用来执行。函数调用可能有副作用、返回值或两者兼有，取决于函数的实现。

7. **异步语句**：JavaScript 还支持异步语句，特别是在浏览器等环境中。异步语句（如回调、`Promise` 和 `async/await`）允许开发者处理异步任务，如获取数据或处理用户输入。

8. **错误处理**：JavaScript 提供了错误处理机制，例如 `try...catch` 语句，允许开发者优雅地捕获错误，防止程序在出现意外问题时崩溃。

9. **代码块**：JavaScript 中的许多语句是复合语句，由大括号 `{}` 包裹的代码块组成。代码块将多个语句分组并定义变量的作用域。

```javascript
// 条件语句
if (sum > 15) {
    console.log("Sum is greater than 15");
} else {
    console.log("Sum is not greater than 15");
}
```

```javascript
// 循环语句
for (let i = 0; i < 5; i++) {
    console.log("Iteration");
}
```

```javascript
// 函数语句
function multiply(a, b) {
    return a * b;
}
```

```javascript
// 函数调用
let result = multiply(5, 3);
```

```javascript
// 结果输出
console.log("Sum: " + sum);
console.log("Product: " + product);
```

```javascript
// JavaScript 示例
let sum = 10;
let product = 20;

// 1. 运算符
if (sum > 15) {
    console.log("和大于 15");
} else {
    console.log("和不大于 15");
}

// 2. 控制流语句
for (let i = 0; i < 5; i++) {
    console.log("迭代 " + i);
}

// 3. 函数
function multiply(a, b) {
    return a * b;
}

// 4. 函数调用
let result = multiply(5, 3);

// 5. 结果输出
console.log("和: " + sum);
console.log("积: " + product);
```

# JavaScript 语法

JavaScript 语法规定了编写 JavaScript 代码的规则。

1. **大小写敏感**：JavaScript 是区分大小写的，这意味着变量名和函数名必须区分。

2. **语句与分号**：JavaScript 程序由语句组成，每个语句通常以分号结束。使用分号是一种推荐的做法。

3. **空格**：空格（包括空格和换行）通常会被忽略。然而，正确的缩进和空格对于代码的可读性至关重要。

4. **注释**：JavaScript 支持单行注释（以 `//` 开头）和多行注释（在 `/*` 和 `*/` 之间）。注释在代码执行期间会被忽略，用于提供说明或临时禁用代码。

5. **变量**：JavaScript 使用 `var`、`let` 或 `const` 关键字声明变量。变量名必须遵循某些规则，例如以字母、下划线 (`_`) 或美元符号 (`$`) 开头，不能是保留字。

6. **数据类型**：JavaScript 支持多种数据类型，包括数字、字符串、布尔、对象、数组等。了解如何声明和使用这些数据类型是编写有效代码的基础。

7. **运算符**：JavaScript 使用运算符对变量和值进行操作。常见的包括算术运算符 (`+`, `-`, `*`, `/`)、赋值运算符 (`=`, `+=`, `-=`)、比较运算符 (`==`, `===`, `!=`, `!==`) 以及逻辑运算符 (`&&`, `||`)。

8. **控制流语句**：控制流语句（如 `if`、`else`、`for`、`while` 和 `switch`）控制 JavaScript 程序的执行流程。正确使用这些语句可以确保程序按预期运行。

9. **函数**：JavaScript 中的函数使用 `function` 关键字定义，后面跟着函数名和参数。理解函数语法，包括如何定义、调用和从函数返回结果，对于创建模块化和可重用的代码至关重要。

# JS 注释

注释是代码中被 JavaScript 引擎忽略的文本，用于解释代码逻辑、记录功能或临时禁用代码。

## 1. 单行注释

以 `//` 开头，直到行尾结束。

## 2. 多行注释

以 `/*` 开始，以 `*/` 结束，可跨越多行。

## 3. 文档注释

通常用于生成 API 文档，格式为 `/** ... */`。

## 4. 注释的作用

- **代码文档**：注释有助于其他开发者（或未来的自己）理解代码库。
- **调试**：可以使用注释在调试期间临时禁用代码，而无需将其删除。这允许开发者隔离并测试特定的代码段。
- **TODOs 和 FIXMEs**：开发者经常使用注释来标记需要关注的代码区域，例如实现某功能（`// TODO: implement feature`）或修复 Bug（`// FIXME: fix this issue`）。

## 5. 注释最佳实践

- **清晰性**：编写清晰、简洁的注释，解释代码背后的目的或逻辑。避免不必要或冗长的注释。
- **一致性**：在整个代码库中保持一致的注释风格。如果已有现有约定，请遵循这些约定。
- **更新注释**：保持注释与代码更改的同步。过时的注释会误导开发者。
- **避免过度注释**：代码在很大程度上应该是自解释的。通过关注核心信息来避免过度注释。

## 6. 条件注释

注释也可以有条件地使用。例如，开发者可能会根据某些条件或开发阶段使用注释来禁用或启用特定的代码块。

## 7. HTML 和 CSS 注释

除了 JavaScript，HTML 和 CSS 也支持注释。HTML 注释用 `<!--` 和 `-->` 表示，而 CSS 注释使用 `/*` 和 `*/`。注释在维护代码质量和促进开发者之间的协作方面起着至关重要的作用。它们是代码内部的一种通信形式，帮助开发者更有效地理解、协作和维护软件。

```javascript
// JavaScript 注释示例

// 声明与初始化
let x = 5;
let y = 10;

// 加法运算
let sum = x + y;

/*
多行注释:
此部分显示结果。
*/
console.log("Sum: " + sum);

// 函数声明
function multiply(a, b) {
  return a * b;
}

// 函数调用
let product = multiply(x, y);

// 显示结果
console.log("Product: " + product);

// JavaScript 注释示例结束
```

```javascript
// script.js
// JavaScript 注释示例

// 声明与初始化
let x = 5;
let y = 10;

// 加法运算
let sum = x + y;

/*
多行注释:
此部分显示结果。
*/
console.log("Sum: " + sum);

// 函数声明
function multiply(a, b) {
  return a * b;
}

// 函数调用
let product = multiply(x, y);

// 显示结果
console.log("Product: " + product);

// JavaScript 注释示例结束
```

| 控制台 | 输出 |
| :--- | :--- |
| Sum | 15 |
| Product | 50 |

在此示例中，通过各种类型演示了 JavaScript 注释：

1. 单行注释：
   - `// 声明与初始化`
   - `// 加法运算`

2. 多行注释：
   - `/* 多行注释: 此部分显示结果。 */`

3. 函数声明和函数调用的注释：
   - `// 函数声明`
   - `// 函数调用`

4. JavaScript 注释示例结束：
   - `// JavaScript 注释示例结束`

JavaScript 中的注释提供了一种为代码添加解释说明的方法，使其更易读、更容易理解。单行注释以 `//` 开头，多行注释包含在 `/* */` 之间。它们会被 JavaScript 解释器忽略，用于文档目的。

# JS 变量

JavaScript 变量是程序中存储和管理数据的容器。它们允许开发者存储和操作值，在编程中起着基础性作用。

1. **变量声明**：在 JavaScript 中，使用 `var`、`let` 或 `const` 关键字声明变量，后跟变量名。例如，`var x;` 声明了一个名为 x 的变量。选择 `var`、`let` 还是 `const` 取决于所需的作用域和可变性。

2. **变量命名**：JavaScript 中的变量名必须遵守某些规则：
   - 它们可以包含字母、数字、下划线 (`_`) 或美元符号 (`$`)。
   - 它们必须以字母、下划线或美元符号开头。
   - 它们区分大小写，因此 `variableName` 和 `VariableName` 被视为不同的变量。

3. **赋值**：声明变量后，可以使用赋值运算符 (`=`) 为其赋值。例如，`x = 10;` 将值 10 赋值给变量 x。赋值的值可以是任何数据类型，如数字、字符串、布尔值或对象。

4. **数据类型**：JavaScript 变量可以持有各种数据类型，包括：
   - 数字：表示数值。
   - 字符串：表示字符序列。
   - 布尔值：表示真或假值。
   - 对象：表示复杂的数据结构。
   - 数组：表示值的有序集合。
   - 未定义：表示值的缺失。

5. **作用域**：JavaScript 变量的作用域决定了可以在哪里访问变量。使用 `var` 声明的变量具有函数作用域，而使用 `let` 或 `const` 声明的变量具有块作用域。全局作用域是指在整个程序范围内都可以访问的变量。

6. **提升**：JavaScript 有一种称为“提升”（hoisting）的行为，声明会被移动到作用域的顶部。这意味着可以在实际声明之前使用变量。

7. **可变性**：使用 `var` 或 `let` 声明的变量可以重新赋值，而使用 `const` 声明的变量是不可变的（引用不可变）。

8. **动态类型**：JavaScript 是一种动态类型语言，这意味着变量的类型是在运行时确定的。

9. **Null 和 Undefined**：`null` 表示有意地缺失任何对象值，而 `undefined` 表示变量已声明但尚未赋值。

```javascript
// JavaScript 变量示例

// 1. 字符串变量
let fullName = "John Doe";

// 2. 数字变量
let age = 30;

// 3. 布尔变量
let isStudent = true;

// 4. 数组变量
let skills = ["JavaScript", "HTML", "CSS"];

// 5. 对象变量
let address = {
  street: "123 Main St",
  city: "New York",
  zipCode: "10001"
};

// 6. 未定义变量
let temperature; // 未进行初始化的声明

// 7. 显示变量
console.log("Full Name: " + fullName);
console.log("Age: " + age);
console.log("IsStudent? " + isStudent);
console.log("Skills: " + skills.join(", "));
console.log("Address: " + address.street + ", " + address.city + " " + address.zipCode);
console.log("Temperature: " + temperature); // 输出 undefined
```

JavaScript 中的变量用于声明和操作数据。它们可以存储不同类型的数据，包括字符串、数字、布尔值、数组、对象等。此示例演示了变量的声明、初始化和用法。

# JS Let

在 JavaScript 中，`let` 关键字用于声明变量。它在 ECMAScript 6 (ES6) 中引入，旨在为旧的 `var` 关键字提供一种更灵活的替代方案。

### 1. 变量声明

`let` 关键字用于在 JavaScript 中声明变量。当使用 `let` 声明变量时，它可以被重新赋值为新值。

### 2. 块作用域

使用 `let` 声明的变量具有块作用域。这意味着变量仅在定义它的代码块内是可访问的。块通常由一对大括号 `{}` 定义。

### 3. 重复声明

与使用 `var` 声明的变量不同，使用 `let` 声明的变量不能在同一块内重复声明。在同一块中使用 `let` 尝试声明变量会导致错误。

### 4. 提升

使用 `let` 声明的变量会被提升到所在块的顶部，但在遇到声明语句之前它们不会被初始化。这意味着与 `var` 不同，使用 `let` 声明的变量在代码中的声明之前是不可访问的。

### 5. 暂时性死区 (TDZ)

暂时性死区 (TDZ) 的概念与 `let` 的提升有关。在 TDZ 期间，在声明之前访问 `let` 变量会导致运行时错误。与 `var` 相比，这强制执行了更整洁的作用域行为。

### 6. 全局对象属性

与使用 `var` 声明的变量不同，使用 `let` 声明的变量不会变成全局对象（浏览器中的 `window`）的属性。这避免了潜在的冲突和意外的全局变量声明。

### 7. 循环与闭包

`let` 常用于 `for` 循环为每次迭代创建一个新的变量，从而防止在使用 `var` 时可能出现的闭包问题。这种行为通常被称为“块作用域循环变量”。

### 8. 条件语句

在 `if` 语句或其他块结构中使用 `let` 声明的变量被限制在该块内。这确保了变量是隔离的，不会泄漏到外部作用域。

### 9. 函数作用域

与具有函数作用域的 `var` 不同，在函数内部使用 `let` 声明变量具有块作用域。这允许对变量可见性进行更精细的控制，并减少变量意外泄漏的概率。

### 10. TDZ 与闭包

暂时性死区行为与闭包结合，可以在特定场景下创建更具预测性且符合逻辑的作用域。

由于块作用域行为和对变量声明处理的改进，在现代编码实践中，JavaScript 中的 `let` 优于 `var`。它提供了更具预测性的作用域，并有助于防止与 `var` 提升相关的常见问题。

```javascript
// JavaScript 'let'

// 使用 'let' 进行变量声明和初始化
let x = 5;
let y = 10;

// 加法运算
let sum = x + y;

// 显示结果
console.log("Sum: " + sum);

// 使用 'let' 进行重新赋值
let message = "Hello";
console.log("Message: " + message);

message = "Hi";
console.log("Updated Message: " + message);

// 块作用域 'let'
if (sum > 15) {
  let result = "Sum is greater than 15";
  console.log(result);
} else {
  let result = "Sum is not greater than 15";
  console.log(result);
}
```

```javascript
// 循环中的 'let'
for (let i = 0; i < 3; i++) {
  console.log("Iteration " + (i + 1));
}
```

// 'let' 示例结束

# JS Const

在 JavaScript 中，`const` 关键字用于声明常量。它在 ECMAScript 6 (ES6) 中引入，用于声明一旦初始化就不能重新赋值的变量。

### 1. 常量声明

`const` 关键字用于声明常量。声明时必须进行初始化。

### 2. 块作用域

与 `let` 类似，`const` 也具有块作用域。

### 3. 不可重新赋值

使用 `const` 声明的变量不能被重新赋值。尝试重新赋值会抛出 `TypeError`。

### 4. 对象与数组的可变性

对于对象和数组，`const` 保证的是引用不变，但其属性或元素可以被修改。

### 5. 循环中的使用

在 `for...of` 循环中可以使用 `const`，但在普通 `for` 循环中因需要更新计数器而不能使用。

```javascript
// JavaScript 'const' 示例

// 使用 'const' 进行常量声明和初始化
const PI = 3.14159;

// 显示常量
console.log("Value of PI: " + PI);

// 重新赋值（会导致错误）
// PI = 3.14; // 取消此行的注释会导致 TypeError

// 常量对象
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30
};

// 显示常量对象
console.log("Person: " + person.firstName + " " + person.lastName + ", Age: " + person.age);

// 修改属性（允许）
person.age = 31;

// 显示更新后的常量对象
console.log("Updated Person: " + person.firstName + " " + person.lastName + ", Age: " + person.age);
```

```javascript
// script.js
// JavaScript 'const' 示例
const PI = 3.14159;
console.log("Value of PI: " + PI);
// PI = 3.14; // 取消注释会导致 TypeError
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30
};
console.log("Person: " + person.firstName + " " + person.lastName + ", Age: " + person.age);
person.age = 31;
console.log("Updated Person: " + person.firstName + " " + person.lastName + ", Age: " + person.age);
```

| 控制台 | 输出 |
| :--- | :--- |
| Value of PI | 3.14159 |
| Person | John Doe, Age: 30 |
| Updated Person | John Doe, Age: 31 |

在本示例中，JavaScript 的 `const` 关键字用于常量声明：

1. 使用 `const` 进行常量声明和初始化：`const PI = 3.14159;`
2. 显示常量：`console.log("Value of PI: " + PI);`
3. 尝试重新赋值（会导致错误）：取消行 `PI = 3.14` 的注释会导致 `TypeError`，因为常量不能被重新赋值。
4. 常量对象：`const person = { ... };` 声明了一个常量对象。
5. 显示常量对象：`console.log("Person: " + person.firstName + " " + person.lastName + ", Age: " + person.age);`
6. 修改属性（允许）：修改常量对象的属性是允许的，因此 `person.age = 31;` 是有效的。
7. 显示更新后的常量对象：`console.log("Updated Person: " + person.firstName + " " + person.lastName + ", Age: " + person.age);`

`const` 关键字用于在 JavaScript 中声明常量。一旦给常量赋值了值，就不能重新赋值。然而，对于用 `const` 声明的对象，仍然可以修改它们的属性。

# JS 运算符

JavaScript 运算符是会对变量和值执行操作的符号。它们允许你操纵数据、执行计算、比较值等。

## 1. 算术运算符

算术运算符执行基础数学运算。

- 加法 (`+`)：将两个值相加。
- 减法 (`-`)：从左操作数中减去右操作数。
- 乘法 (`*`)：将两个值相乘。
- 除法 (`/`)：将左操作数除以右操作数。
- 取模 (`%`)：返回左操作数除以右操作数的余数。
- 幂 (`**`)：将左操作数提升到右操作数的幂。
- 自增 (`++`)：将其操作数的值加 1。
- 自减 (`--`)：将其操作数的值减 1。

## 2. 赋值运算符

赋值运算符将值赋给变量。

- 赋值 (`=`)：将右侧的值赋给变量。
- 加赋值 (`+=`)：将右操作数加到变量并赋值结果。
- 减赋值 (`-=`)：从变量中减去右操作数并赋值结果。
- 乘赋值 (`*=`)：将变量乘以右操作数并赋值结果。
- 除赋值 (`/=`)：将变量除以右操作数并赋值结果。

## 3. 比较运算符

比较运算符比较两个值并返回一个布尔结果。

- 等于 (`==`)：检查两个值是否相等（类型转换后）。
- 严格等于 (`===`)：检查两个值是否相等且类型相同。
- 不等于 (`!=`)：检查两个值是否不等（类型转换后）。
- 严格不等于 (`!==`)：检查两个值是否不等或类型不同。
- 大于 (`>`)：检查左操作数是否大于右操作数。
- 小于 (`<`)：检查左操作数是否小于右操作数。
- 大于等于 (`>=`)：检查左操作数是否大于等于右操作数。
- 小于等于 (`<=`)：检查左操作数是否小于等于右操作数。

## 4. 逻辑运算符

逻辑运算符执行逻辑操作并返回布尔结果。

- 逻辑与 (`&&`)：当两个操作数都为真时，返回 true。
- 逻辑或 (`||`)：当至少有一个操作数为真时，返回 true。
- 逻辑非 (`!`)：返回操作数的反向布尔值。

## 5. 一元运算符

一元运算符作用于单个操作数。

- 一元加 (`+`)：将其操作数转换为数字。
- 一元减 (`-`)：对其操作数取反。
- 逻辑非 (`!`)：将操作数转换为布尔值并取反。

## 6. 条件（三元）运算符

条件运算符 (`? :`) 是编写 `if...else` 语句的简写方式。它评估一个条件，并根据该条件的真假返回两个值之一。

## 7. 位运算符

位运算符对整数的二进制表示执行操作。

- 位与 (`&`)：执行位级与操作。
- 位或 (`|`)：执行位级或操作。
- 位异或 (`^`)：执行位级异或操作。
- 位非 (`~`)：反转其操作数的位。
- 左移 (`<<`)：将操作数的位向左移动。
- 右移 (`>>`)：将操作数的位向右移动（保留符号位）。
- 无符号右移 (`>>>`)：将操作数的位向右移动（补零）。

## 8. typeof 运算符

`typeof` 运算符返回表示操作数类型的字符串。

JavaScript 运算符对于程序中操纵数据和决策至关重要。理解如何有效使用运算符对于编写表达力且功能良好的 JavaScript 代码至关重要。

```javascript
// JavaScript 运算符示例

// 算术
let x = 5;
let y = 10;

let addition = x + y;
let subtraction = x - y;
let multiplication = x * y;
let division = x / y;
let remainder = x % y;

// 显示算术运算的结果
console.log("Addition: " + addition);
console.log("Subtraction: " + subtraction);
console.log("Multiplication: " + multiplication);
console.log("Division: " + division);
console.log("Remainder: " + remainder);

// 字符串拼接运算符
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName;

// 显示拼接后的字符串
console.log("Full Name: " + fullName);

// 赋值运算符
let z = 15;

// 比较运算符
let isEqual = x === y;
let isNotEqual = x !== y;
let isGreater = x > y;
let isLess = x < y;
let isGreaterOrEqual = x >= y;
let isLessOrEqual = x <= y;

// 显示比较运算符的结果
console.log("Is Equal: " + isEqual);
console.log("Is Not Equal: " + isNotEqual);
console.log("Is Greater: " + isGreater);
console.log("Is Less: " + isLess);
console.log("Is Greater or Equal: " + isGreaterOrEqual);
console.log("Is Less or Equal: " + isLessOrEqual);

// 逻辑运算符
let isTrue = true;
let isFalse = false;

let andResult = isTrue && isFalse;
let orResult = isTrue || isFalse;
let notResult = !isTrue;

// 显示逻辑运算的结果
console.log("AND Result: " + andResult);
console.log("OR Result: " + orResult);
console.log("NOT Result: " + notResult);

// 自增和自减运算符
let count = 5;
count++;
let incrementedCount = count;
count--;
let decrementedCount = count;

// 显示自增和自减后的值
console.log("Incremented Count: " + incrementedCount);
console.log("Decremented Count: " + decrementedCount);

// 条件（三元）运算符
let isEven = x % 2 === 0;
let parityMessage = isEven ? "Even" : "Odd";

// 显示奇偶性消息
console.log("Parity: " + parityMessage);

// typeof 运算符
let typeOfX = typeof x;
console.log("Type of x: " + typeOfX);
```

| 控制台 | 输出 |
| :--- | :--- |
| Addition | 15 |
| Subtraction | -5 |
| Multiplication | 50 |
| Division | 0.5 |
| Remainder | 5 |
| Full Name | John Doe |
| Is Equal | false |
| Is Not Equal | true |
| Is Greater | false |
| Is Less | true |
| Is Greater or Equal | false |
| Is Less or Equal | true |
| AND Result | false |
| OR Result | true |
| NOT Result | false |
| Incremented Count | 6 |
| Decremented Count | 5 |
| Parity | Odd |
| Type of x | number |

在这个示例中，演示了各种 JavaScript 运算符：

1. 算术运算符：`+`, `-`, `*`, `/`, `%`, `++`, `--`
2. 字符串拼接运算符：`+`
3. 赋值运算符：`=`, `+=`, `-=`, `*=`, `/=`
4. 比较运算符：`===`, `!==`, `>`, `<`, `>=`, `<=`
5. 逻辑运算符：`&&`, `||`, `!`
6. 自增和自减运算符：`++`, `--`
7. 条件（三元）运算符：`? :`
8. `typeof` 运算符：`typeof`

这些运算符是 JavaScript 中执行操作、比较和逻辑评估的基础。

# JS 算术

JavaScript 中的算术运算涉及使用算术运算符对数值进行数学运算。这些运算符允许你进行加、减、乘、除以及其他基础数学计算。

## 1. 加法 (`+`)

加法运算符 (`+`) 将两个数值相加。例如，`3 + 5` 的结果为 `8`。

## 2. 减法 (`-`)

减法运算符 (`-`) 从左操作数中减去右操作数。例如，`7 - 4` 的结果为 `3`。

## 3. 乘法 (`*`)

乘法运算符 (`*`) 将两个数值相乘。例如，`2 * 6` 的结果为 `12`。

## 4. 除法 (`/`)

除法运算符 (`/`) 将左操作数除以右操作数。例如，`10 / 2` 的结果为 `5`。

## 5. 取模 (`%`)

取模运算符 (`%`) 返回左操作数除以右操作数得出的余数。例如，`10 % 3` 的结果为 `1`，因为 10 除以 3 的余数为 1。

## 6. 幂 (`**`)

幂运算符 (`**`) 将左操作数提升到右操作数的幂。例如，`2 ** 3` 的结果为 `8`，因为 2 的 3 次方是 8。

## 7. 自增 (`++`)

自增运算符 (`++`) 增加变量的值。例如，如果 `x` 初始为 `5`，`x++` 的结果为 `6`。

## 8. 自减 (`--`)

自减运算符 (`--`) 减少变量的值。例如，如果 `y` 初始为 `8`，`y--` 的结果为 `7`。

## 9. 一元加 (`+`)

一元加运算符 (`+`) 将其操作数转换为数字。如果操作数已经是数字，则无变化。例如，`+"42"` 的结果为 `42`。

## 10. 一元否定 (`-`)

一元否定运算符 (`-`) 对其操作数进行取反。如果操作数不是数字，JavaScript 会尝试将其转换为数字然后取反。例如，`-3` 的结果为 `-3`。

算术运算符遵循标准的算术规则。它们可以组合使用创建复杂的表达式，并遵循运算顺序（括号、幂、乘除从左到右、加减从左到右）。理解这些运算符是执行数学计算的基础。

```javascript
// JavaScript 算术示例

// 加法
let sum = 5 + 10;
// 减法
let difference = 20 - 8;
// 乘法
let product = 4 * 6;
// 除法
let quotient = 36 / 9;
// 余数（取模）
let remainder = 15 % 4;

// 显示结果
console.log("Sum: " + sum);
console.log("Difference: " + difference);
console.log("Product: " + product);
console.log("Quotient: " + quotient);
console.log("Remainder: " + remainder);

// 组合操作
let result = (sum * product) - (remainder + 1);
// 显示组合结果
console.log("Combined Result: " + result);

// 自增和自减
let counter = 5;
counter++; // 自增 1
let incrementedCount = counter;
counter--; // 自减 1
let decrementedCount = counter;

// 显示自增和自减后的值
console.log("Incremented Counter: " + incrementedCount);
console.log("Decremented Counter: " + decrementedCount);
```

# JS 赋值

JavaScript 中的赋值涉及将值存储在变量中或修改现有的值。赋值运算符 (`=`) 用于此目的。

## 1. 赋值运算符 (`=`)

赋值运算符 (`=`) 用于将值赋予变量。例如，`x = 5;` 将 `5` 赋值给变量 `x`。

## 2. 变量声明与赋值

变量通常使用 `var`、`let` 或 `const` 关键字声明，然后使用赋值运算符为变量分配初始值。

## 3. 重赋值

一旦变量已声明并赋值，可以使用赋值运算符更改或重新赋值其值。例如，如果 `y` 初始为 `10`，语句 `y = y + 5;` 将 `y` 的值更改为 `15`。

## 4. 更新变量

赋值运算符通常与算术运算符结合使用，根据当前值更新变量的值。例如，`count = count + 1;` 将变量的值增加 1。

## 5. 链赋值

JavaScript 允许链赋值语句。例如，`a = b = c = 10;` 在一行内将 `10` 赋值给变量 `a`、`b` 和 `c`。

## 6. 简写赋值

简写赋值运算符（如 `+=`、`-=`、`*=`、`/=`）将赋值运算符与算术运算符结合。它们提供了一种根据当前值更新变量的简洁方式。例如，`x += 3;` 等同于 `x = x + 3;`。

## 7. 常量赋值

使用 `const` 关键字声明的变量是常量，这意味着它们的值在初始赋值后不能被重新赋值。尝试给常量变量重新赋值将导致错误。

## 8. 给未定义的变量赋值

如果你尝试给一个未声明或未初始化的变量赋值，JavaScript 将创建一个全局变量（在非严格模式下）或抛出引用错误（在严格模式下）。

## 9. 引用赋值

在处理对象或数组时，赋值是通过引用完成的。如果将另一个对象或数组的值赋值给一个变量，那么对其中一个变量的更改将影响另一个变量。

理解如何使用赋值运算符是操作 JavaScript 变量的基础。它允许开发者在程序中存储和操纵数据，使其成为编程中的一个核心概念。

```javascript
// JavaScript Assignment Example
let x = 5;

// Display Assigned Value
console.log("Initial Value of x: " + x);

// Reassignment
x = 10;

// Display Updated Value
console.log("Updated Value of x: " + x);

// Combined Assignment (Addition)
let y = 3;
y += 7; // Equivalent to: y = y + 7;

// Display Combined Assignment Result
console.log("Combined Assignment Result (Addition): " + y);

// Combined Assignment (String Concatenation)
let greeting = "Hello";
let name = "John";

greeting += " " + name; // Equivalent to: greeting = greeting + " " + name;

// Display Assignment Result (String Concatenation)
console.log("Combined Assignment Result (String Concatenation): " + greeting);

// Combined Assignment (Multiplication)
let z = 4;
z *= 2; // Equivalent to: z = z * 2;

// Display Assignment Result (Multiplication)
console.log("Combined Assignment Result (Multiplication): " + z);

// End of JavaScript Assignment Example
```

```javascript
// script.js
// Basic Assignment
let x = 5;
// Display Assignment
console.log("Initial value of x: " + x);
// Reassignment
x = 10;
// Display Updated Value
console.log("Updated value of x: " + x);
// Combined Assignment (Addition)
let y = 3;
y += 7; // Equivalent to: y = y + 7;
// Display Combined Assignment Result
console.log("Combined Assignment Result (Addition): " + y);
// Combined Assignment (String Concatenation)
let greeting = "Hello";
let name = "John";
greeting += " " + name; // Equivalent to: greeting = greeting + " " + name;
// Display Assignment Result (String Concatenation)
console.log("Combined Assignment Result (String Concatenation): " + greeting);
// Combined Assignment (Multiplication)
let z = 4;
z *= 2; // Equivalent to: z = z * 2;
// Display Assignment Result (Multiplication)
console.log("Combined Assignment Result (Multiplication): " + z);
// End of JavaScript Assignment Example
```

在这个示例中，演示了 JavaScript 的赋值操作：

1. **基础赋值**：`let x = 5;`
2. **重新赋值**：`x = 10;`
3. **复合赋值（加法）**：`y += 7;` (等同于 `y = y + 7;`)
4. **复合赋值（字符串拼接）**：`greeting += " " + name;` (等同于 `greeting = greeting + " " + name;`)
5. **复合赋值（乘法）**：`z *= 2;` (等同于 `z = z * 2;`)
6. **显示结果**：
   - `console.log("Initial Value of x: " + x);`
   - `console.log("Updated Value of x: " + x);`
   - `console.log("Combined Assignment Result (Addition): " + y);`
   - `console.log("Combined Assignment Result (String Concatenation): " + greeting);`
   - `console.log("Combined Assignment Result (Multiplication): " + z);`

这些赋值操作允许根据计算或拼接对变量进行赋值和更新。

# JS 数据类型

在 JavaScript 中，数据类型定义了变量可以持有的值的性质。JavaScript 是一种动态类型语言，这意味着变量类型是在运行时确定的。

## 1. 原始数据类型

- **Number（数字）**：代表数值。包括整数和浮点数。
- **String（字符串）**：代表字符序列，例如文本。
- **Boolean（布尔值）**：代表真或假值。
- **Undefined（未定义）**：代表已声明但未赋值的变量。
- **Null（空）**：代表值的缺失或对对象的引用。
- **Symbol（符号）**：在 ECMAScript 6 (ES6) 中引入，是唯一且不可变的数据类型，通常用作属性的标识符。
- **BigInt**：在 ECMAScript 2020 中引入，代表任意精度的整数。

## 2. 引用数据类型

- **Object（对象）**：一种复杂类型，允许你将相关的数据和函数组合在一起。对象是用户定义或内置类的实例，由键值对组成。
- **Array（数组）**：对象的一种，用于存储值的有序集合。
- **Function（函数）**：在 JavaScript 中，函数被视为一种特殊的对象类型。函数可以被赋值给变量。

## 3. 特殊值

- **Infinity（无穷大）**：代表正无穷。
- **-Infinity（负无穷）**：代表负无穷。
- **NaN (Not a Number)**：代表无效的数值结果。

## 4. 包装对象

- **Number, String, Boolean**：这些提供了与原始类型相关的方法。

## 5. typeof 运算符

`typeof` 运算符用于确定操作数的类型。

## 6. 动态类型

JavaScript 是动态类型，这意味着变量可以在运行时更改类型。

## 7. 类型转换

JavaScript 会隐式或显式地执行从一种数据类型到另一种数据类型的转换。

```javascript
// JavaScript 数据类型示例

// 1. 原始数据类型
let number = 42;
let text = "Hello, World!";
let isTrue = true;
let isNull = null;
let undefinedVar;

// 2. 对象数据类型
let person = {
  firstName: "John",
  lastName: "Doe",
  age: 30
};

// 3. 数组数据类型
let colors = ["Red", "Green", "Blue"];

// 4. 函数数据类型
function greet() {
  return "Hello!";
}

// 5. typeof 运算符
let typeOfText = typeof text;

// 6. 显示数据类型
console.log("Number: " + number);
console.log("Text: " + text);
console.log("Boolean: " + isTrue);
console.log("Null: " + isNull);
console.log("Undefined: " + undefinedVar);
console.log("Person: " + person.firstName + " " + person.lastName + ", Age: " + person.age);
console.log("Colors: " + colors.join(", "));
console.log("Type of Text: " + typeOfText);
```

这些示例展示了 JavaScript 中的基本数据类型，包括原始类型（数字、字符串、布尔、null 和 undefined），以及对象、数组和函数类型。

# JS 函数

## 1. 抽象

函数允许抽象，使开发者能够将一组指令封装到单一命名实体中。这促进了代码的组织和模块化。

## 2. 可重用性

一旦定义了函数，就可以在代码中重复使用。这减少了冗余并促进了更高效、更易维护的代码库。

## 3. 参数化

函数可以接受参数，参数是作为值占位符的变量。这些参数使函数变得灵活，使其能够处理不同的输入。

## 4. 返回值

函数可以使用 `return` 语句产生结果。返回值可以被调用代码利用，允许函数生成输出并对整体程序逻辑做出贡献。

## 5. 函数调用

通过调用函数来执行函数。这可以通过使用函数名后跟括号来实现。调用会触发函数代码的执行。

## 6. 函数作用域

声明在函数内部的变量通常作用限于该函数，并且在函数外部无法访问。这有助于防止命名冲突并封装变量。

## 7. 匿名函数

JavaScript 支持创建不分配命名的函数。这些匿名函数通常用于使用一次且不需要专用命名的场景。

## 8. 箭头函数

箭头函数在 ECMAScript 6 (ES6) 中引入，为编写函数提供了更简洁的语法，特别是对于短的单行表达式。它们还以不同的方式处理 `this` 关键字的作用域。

## 9. 一等公民

在 JavaScript 中，函数是一等公民，这意味着它们可以赋值给变量、作为参数传递给其他函数，并作为其他函数的返回值。这允许了函数式编程范式。

## 10. 闭包

JavaScript 中的函数形成闭包，这意味着即使在函数执行完毕，它们仍然保留对其所在作用域中变量的访问。这为 JavaScript 编程提供了强大的模式。

## 11. 递归

JavaScript 中的函数可以调用自己，这种概念被称为递归。这种技术对于解决可以分解为更小的相似子问题的问题有用。

## 12. 回调函数

回调函数作为参数传递给其他函数。它们通常用于异步编程、事件处理以及执行顺序重要的情况。

## 13. 函数声明 vs. 表达式

函数声明会被提升到其所在作用域的顶部，允许在声明之前调用它们。相反，函数表达式不会以相同的方式被提升。

## 14. 函数重载

JavaScript 不支持原生函数重载（即具有相同名称但不同参数列表的多个函数）。然而，开发者可以通过默认参数值并在函数内部检查参数的数量或类型来实现类似的效果。

理解 JavaScript 的这些方面对于熟练编写清洁、高效且可维护的代码至关重要。函数在 JavaScript 应用中构建逻辑和促进代码可重用方面起着核心作用。

```javascript
// JavaScript 函数示例

// 函数声明
function add(x, y) {
  return x + y;
}

// 函数调用
let sum = add(5, 10);

// 显示结果
console.log("Sum: " + sum);

// 函数表达式
let multiply = function(a, b) {
  return a * b;
}

// 函数调用
let product = multiply(4, 6);

// 显示结果
console.log("Product: " + product);

// 箭头函数
let subtract = (a, b) => a - b;

// 函数调用
let difference = subtract(10, 4);
console.log("Difference: " + difference);
```

在此示例中，展示了定义 JavaScript 函数的方式：

- 函数声明：`function add(x, y) { return x + y; }`
- 函数调用：`let sum = add(5, 10);`
- 显示结果：`console.log("Sum: " + sum);`
- 函数表达式：`let multiply = function(a, b) { return a * b; }`
- 函数调用：`let product = multiply(4, 6);`
- 显示结果：`console.log("Product: " + product);`
- 箭头函数：`let subtract = (a, b) => a - b;`
- 函数调用：`let difference = subtract(10, 4);`
- 显示结果：`console.log("Difference: " + difference);`

# JS 对象

在 JavaScript 中，对象是用于表示和组织数据的基本数据类型。它们是键值对的集合，其中每个键都是字符串（或 Symbol），每个值可以是任何类型。

## 1. 键值对

对象由键值对组成，每个键都是唯一的字符串（或 Symbol），作为标识符，每个值都与该键关联。键及其对应值的组合被称为属性。

## 2. 属性

属性是对象中的单个键值对。每个属性都有一个唯一的键作为名称，关联的值可以是任何数据类型，包括数字、字符串、布尔、函数或其他对象。

## 3. 对象字面量法

在 JavaScript 中创建对象的常用方法是使用对象字面量法。它涉及使用大括号 `{}` 并在内部指定键值对。这种语法简洁并广泛用于直接在代码中创建对象。

## 4. 方法

与对象关联的函数被称为方法。方法只是持有函数值的属性。它们允许对象封装行为和功能。

## 5. 对象构造函数

还可以使用 `new` 关键字通过构造函数创建对象。构造函数是初始化并创建对象的普通函数。它们可以使用 `function` 关键字定义。

## 6. 点符号法

对象的属性和方法通常使用点符号法 (`object.property`) 访问。这种语法允许你检索或修改与特定键关联的值。

## 7. 括号法

或者，你可以使用括号法 (`object['property']`) 来访问对象的属性。当属性名是动态的或包含特殊字符时，这种写法非常有用。

## 8. 对象突变

JavaScript 中的对象是可变的，这意味着在对象创建后可以对其属性和方法进行修改、添加或删除。这种动态特性为处理数据提供了灵活性。

## 9. 继承

JavaScript 中的对象可以通过称为原型继承的机制从其他对象继承属性和方法。这允许创建对象层级结构并促进代码复用。

## 10. 对象比较

在 JavaScript 中比较对象时，比较是基于引用相等性的。只有当两个对象引用内存中的同一个对象时，它们才认为是相等。这与基本类型不同，后者比较的是值本身。

## 11. JSON（JavaScript 对象表示法）

JSON 是一种轻量级的数据交换格式，与 JavaScript 对象字面量表示法相似。它通常用于服务器和 Web 应用程序之间的数据交换。JSON 字符串可以被解析为 JavaScript 对象。

理解对象对于有效的 JavaScript 编程至关重要，因为它们为应用程序提供了一种强大且多功能的方式来结构化和表示数据。对象在组织代码和促进各种编程模式的实现中起着核心作用。

```javascript
// JavaScript Objects Example
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
  address: {
    street: "123 Main St",
    city: "Anytown",
    zipCode: "12345"
  },
  hobbies: ["Reading", "Gardening", "Traveling"],
  isStudent: false,
  sayHello: function() {
    console.log("Hello, " + this.firstName + "!");
  }
};
```

```javascript
// Accessing Object Properties
console.log("Name: " + person.firstName + " " + person.lastName);
console.log("Age: " + person.age);
console.log("Street: " + person.address.street);
console.log("Hobbies: " + person.hobbies.join(", "));
```

```javascript
// Invoking Object Method
person.sayHello();
```

```javascript
// Object Constructor Function
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
```

```javascript
// Creating Objects using Constructor Function
const car1 = new Car("Toyota", "Camry", 2022);
const car2 = new Car("Honda", "Accord", 2023);
```

```javascript
// Accessing Object Properties (Constructor)
console.log("Car 1: " + car1.make + " " + car1.model + ", Year: " + car1.year);
console.log("Car 2: " + car2.make + " " + car2.model + ", Year: " + car2.year);
```

```javascript
// script.js
const user = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
  address: {
    street: "123 Main St",
    city: "New York",
    zip: "12345"
  },
  isStudent: false,
  hobbies: ["Gardening", "Reading", "Traveling"],
  sayHello: function() {
    console.log("Hello, " + this.firstName);
  }
};

console.log("Hello, " + user.firstName);

// Accessing Object Properties
console.log("First Name: " + user.firstName);
console.log("Age: " + user.age);
console.log("Address: " + user.address.street);
console.log("Hobbies: " + user.hobbies.join(", "));

// Calling Method
user.sayHello();

// Creating Constructor Function
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

// Creating Objects using Constructor Function
const car1 = new Car("Toyota", "Camry", 2022);
const car2 = new Car("Honda", "Accord", 2023);

// Accessing Object Properties
console.log("Car 1: " + car1.make + " " + car1.model + ", Year: " + car1.year);
console.log("Car 2: " + car2.make + " " + car2.model + ", Year: " + car2.year);

// End of JavaScript Objects Example
```

在这个示例中，使用了不同的方法演示了 JavaScript 对象：

1. **对象字面量**：`const person = { ... };`
2. **访问对象属性**：
   - `console.log("First Name: " + person.firstName);`
   - `console.log("Age: " + person.age);`
   - `console.log("Street: " + person.address.street);`
   - `console.log("Hobbies: " + person.hobbies.join(", "));`
3. **调用对象方法**：`person.sayHello();`
4. **对象构造函数**：
   ```javascript
   function Car(make, model, year) { ... }
   ```
5. **使用构造函数创建对象**：
   - `const car1 = new Car("Toyota", "Camry", 2022);`
   - `const car2 = new Car("Honda", "Accord", 2023);`
6. **访问对象属性（构造函数）**：
   - `console.log("Car 1: " + car1.make + " " + car1.model + ", Year: " + car1.year);`

# JS 事件

```html
<!-- HTML Markup JS Events Example -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Events Example</title>
</head>
<body>
    <!-- Button with Click Event -->
    <button id="clickButton">Click Me</button>

    <script>
        // Click Event Handling
        document.getElementById('clickButton').addEventListener('click', function() {
            alert('Button Clicked!');
        });

        // Mouseover Event Handling
        document.getElementById('clickButton').addEventListener('mouseover', function() {
            console.log('Mouseover Event');
        });

        // Change Event Handling (for Input)
        let inputField = document.createElement('input');
        inputField.setAttribute('type', 'text');
        document.body.appendChild(inputField);
        inputField.addEventListener('change', function(event) {
            console.log('Input Changed: ', event.target.value);
        });
    </script>
</body>
</html>
```

在这个示例中，使用 HTML 标记和内联脚本演示了 JavaScript 事件：

1. **点击事件处理**：为 ID 为 `"clickButton"` 的按钮绑定了一个点击事件监听器。当点击该按钮时，会显示一个警告框消息。

2. **鼠标悬停事件处理**：该按钮还绑定了一个鼠标悬停 (`mouseover`) 事件监听器。当鼠标悬停在按钮上时，消息会打印到控制台。

3. **改变事件处理（针对输入框）**：动态创建一个输入框并将其添加到正文中。它绑定了一个改变 (`change`) 事件监听器。当输入值发生变化时，消息会打印到控制台。

这些示例说明了如何在 HTML 文档中使用 JavaScript 处理不同类型的事件（点击、鼠标悬停、改变）。

# JS 字符串

在 JavaScript 中，字符串是一种基础数据类型，用于表示字符序列。字符串可以包含字母、数字、符号和空白字符。

## 1. 字符序列

字符串是包含在单引号 (`''`)、双引号 (`""`) 或反引号 (````) 之间的字符序列。

## 2. 不变性

在 JavaScript 中，字符串是不可变的，这意味着一旦创建，其值就无法被更改。看似在修改字符串的操作实际上是创建了一个新字符串。

## 3. 转义字符

特殊字符可以使用转义序列表示，用反斜杠 (`\`) 指定。例如，`\n` 代表换行符，`\t` 代表制表符。

## 4. 拼接

使用 `+` 运算符拼接字符串。这涉及到将两个或多个字符串组合成一个新的字符串。例如，`"Hello," + "world!"` 的结果是字符串 `"Hello, world!"`。

## 5. 属性

字符串具有 `length` 属性，返回字符串中的字符数量（UTF-16 代码单元）。该属性允许你确定字符串的大小。

## 6. 索引与访问

使用从零开始的索引访问字符串中的单个字符。例如，`str[0]` 获取 `str` 的第一个字符。也可以使用 `charAt(index)` 方法。

## 7. 字符串方法

JavaScript 提供了许多内置方法来处理字符串。常用方法包括：
- `toUpperCase()`：转为大写。
- `toLowerCase()`：转为小写。
- `trim()`：去除首尾空白。
- `replace()` / `replaceAll()`：替换子串。
- `split()`：分割字符串为数组。
- `substring()` / `slice()` / `substr()`：提取子串。
- `indexOf()` / `lastIndexOf()` / `includes()` / `startsWith()` / `endsWith()`：查找/判断子串。
- `charAt()` / `charCodeAt()` / `codePointAt()`：获取字符/编码。
- `padStart()` / `padEnd()`：填充字符串。
- `repeat()`：重复字符串。

## 8. 模板字面量

ECMAScript 6 (ES6) 引入的模板字面量使用反引号 (````) 提供了一种更灵活的创建字符串的方式。它们允许嵌入表达式 (`${expression}`) 和多行字符串。

## 9. 字符串比较

可以使用关系运算符 (`<`, `<=`, `>`, `>=`) 比较字符串。比较是基于字符的 Unicode 值进行的。严格相等使用 `===`。

## 10. 字符串插值

字符串插值是指将表达式嵌入字符串中。这可以通过模板字面量 (`${expression}`) 来实现。

## 11. Unicode 支持

JavaScript 字符串使用 UTF-16 编码，允许表示来自不同语言和脚本的广泛字符。注意 `length` 和索引基于 UTF-16 代码单元，对于辅助平面字符（Emoji 等）可能需要特殊处理。

## 12. 正则表达式

可以使用正则表达式 (`RegExp`) 来处理字符串。正则表达式为字符串处理提供了强大的模式匹配能力（配合 `match`, `replace`, `search`, `split` 等方法）。

## 13. 字符串原始类型 vs String 对象

JavaScript 将字符串视为原始类型，但也存在一个提供额外方法的 `String` 对象包装器。由于原始字符串和 `String` 对象之间存在自动装箱/拆箱转换，这种区别在大多数情况下是透明的。

理解 JavaScript 中与字符串相关的属性和方法，对于 Web 开发中的处理文本数据和字符串处理任务至关重要。字符串在处理用户输入、创建动态内容以及与数据交互方面起着关键作用。

```javascript
// JavaScript 字符串示例

// 字符串声明
let greeting = "Hello,\nWorld!";

// 显示字符串
console.log("Greeting: " + greeting);

// 字符串拼接
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName;

// 显示拼接后的字符串
console.log("Full Name: " + fullName);

// 字符串长度
let message = "This is a message.";
let messageLength = message.length;

// 显示字符串长度
console.log("Message Length: " + messageLength);

// 常用字符串方法演示
let str = "  Hello World  ";

console.log("Uppercase: " + str.toUpperCase());
console.log("Lowercase: " + str.toLowerCase());
console.log("Trimmed: '" + str.trim() + "'");
console.log("Replace: " + str.trim().replace("World", "JavaScript"));
console.log("Substring(0, 5): " + str.trim().substring(0, 5));
console.log("Slice(-6): " + str.trim().slice(-6));
console.log("Includes 'Hello': " + str.includes("Hello"));
console.log("Starts with '  He': " + str.startsWith("  He"));
console.log("Ends with 'ld  ': " + str.endsWith("ld  "));
console.log("Char at 2: " + str.trim().charAt(2));
console.log("Char code at 2: " + str.trim().charCodeAt(2));
console.log("Split: " + str.trim().split(" "));
console.log("Repeat 2: " + "Ha".repeat(2));
console.log("Pad Start: " + "5".padStart(3, "0"));

// 模板字面量
let template = `Name: ${firstName} ${lastName}
Age: ${30}`;
console.log("Template Literal:\n" + template);
```

1. **`length`**：返回字符串中的字符数（UTF-16 代码单元）。它允许你确定字符串的大小。

2. **`charAt(index)`**：返回字符串中指定索引处的字符。它是基于 0 索引的。

3. **`charCodeAt(index)`**：返回字符串中指定索引处字符的 UTF-16 代码单元值。

4. **`codePointAt(index)`**：返回字符串中指定索引处字符的 Unicode 码点值（支持辅助平面字符）。

5. **`toUpperCase()`**：将字符串中的所有字符转换为大写。

6. **`toLowerCase()`**：将字符串中的所有字符转换为小写。

7. **`trim()`**：去除字符串首尾的空白字符。

8. **`substring(startIndex, endIndex)`**：提取从 `startIndex` 开始到但不包含 `endIndex` 的字符串部分。负值视为 0。

9. **`slice(startIndex, endIndex)`**：提取字符串的一部分。支持负索引（从末尾计算）。

10. **`split(separator, limit)`**：使用分隔符将字符串分割为子字符串数组。

11. **`replace(searchFor, replaceWith)`**：替换匹配的子串（仅首次匹配，除非使用带 `g` 标志的正则）。支持函数作为第二参数。

12. **`replaceAll(searchFor, replaceWith)`**：替换所有匹配的子串。

13. **`includes(searchString, position)`**：判断字符串是否包含指定子串，返回布尔值。

14. **`startsWith(searchString, position)`**：判断字符串是否以指定子串开头。

15. **`endsWith(searchString, length)`**：判断字符串是否以指定子串结尾。

16. **`indexOf(searchValue, fromIndex)`**：返回指定子串首次出现的索引，未找到返回 -1。

17. **`lastIndexOf(searchValue, fromIndex)`**：返回指定子串最后一次出现的索引。

18. **`padStart(targetLength, padString)`**：用另一个字符串填充当前字符串（从开头），直到达到指定长度。

19. **`padEnd(targetLength, padString)`**：用另一个字符串填充当前字符串（从结尾），直到达到指定长度。

20. **`repeat(count)`**：返回包含重复字符串指定次数的新字符串。

21. **`toLocaleUpperCase()` / `toLocaleLowerCase()`**：根据本地化规则转换大小写。

22. **`match(regexp)` / `matchAll(regexp)` / `search(regexp)`**：配合正则表达式进行匹配/搜索。

这些方法为 JavaScript 中的字符串操作提供了强大的工具集。



## 字符串方法

`slice(startIndex, endIndex)`方法提取字符串的一部分，与`substring`类似。如果`startIndex`或`endIndex`任何一个为负数，则将从字符串末尾开始计数。

### indexOf(searchString, startIndex)

`indexOf(searchString, startIndex)`方法返回`searchString`在字符串中首次出现的索引。如果未找到，则返回-1。搜索可以从可选的`startIndex`开始。

### lastIndexOf(searchString, startIndex)

`lastIndexOf(searchString, startIndex)`方法返回`searchString`在字符串中最后一次出现的索引。如果未找到，则返回-1。搜索可以从可选的`startIndex`开始。

### startsWith(searchString, position)

`startsWith(searchString, position)`方法检查字符串是否以指定的`searchString`开头。可选的`position`参数指定搜索的位置。

### endsWith(searchString, position)

`endsWith(searchString, position)`方法检查字符串是否以指定的`searchString`结尾。可选的`position`参数指定搜索的位置。

### includes(searchString, position)

`includes(searchString, position)`方法检查字符串是否包含指定的`searchString`。可选的`position`参数指定搜索的位置。

### replace(searchValue, replaceValue)

`replace(searchValue, replaceValue)`方法将字符串中出现的`searchValue`替换为`replaceValue`。

### trim()

`trim()`方法移除字符串开头和结尾的空白字符。

### split(separator, limit)

`split(separator, limit)`方法根据指定的分隔符将字符串分割为子字符串数组。可选的`limit`参数限制分割的次数。

### concat(string1, string2, ...)

`concat(string1, string2, ...)`方法将多个字符串连接在一起。

### repeat(count)

`repeat(count)`方法通过重复原始字符串`count`次来创建一个新字符串。

### match(regexp)

`match(regexp)`在字符串中搜索与正则表达式匹配的内容，并将匹配项作为数组返回。

### search(regexp)

`search(regexp)`在字符串中搜索与正则表达式匹配的内容，并返回第一个匹配项的索引。如果没有找到匹配项，则返回-1。

这些方法为JavaScript中的字符串操作提供了一套强大的工具，允许开发者高效地处理从文本数据中提取信息。理解这些方法对于Web开发中有效的字符串处理至关重要。

## JavaScript字符串方法示例

```javascript
// String Methods
let originalString = " JavaScript String Methods ";

let trimmedString = originalString.trim();
let uppercasedString = originalString.toUpperCase();
let lowercString = originalString.toLowerCase();
let substring = originalString.substring(5, 18);
let replacedString = originalString.replace("Methods", "Functions");
let splitString = originalString.split(" ");
```

```javascript
// Display Results of String Methods
console.log("Original String: " + originalString);
console.log("Trimmed String: " + trimmedString);
console.log("Uppercased String: " + uppercasedString);
console.log("Lowercased String: " + lowercString);
console.log("Substring: " + substring);
console.log("Replaced String: " + replacedString);
console.log("Split String: " + JSON.stringify(splitString));
```

```javascript
// Chaining String Methods
let modifiedString = originalString.trim().toUpperCase().replace("METHODS", "OPERATIONS");
```

```javascript
// Display Chained Methods Result
console.log("Chained Methods Result: " + modifiedString);
```

```javascript
// End of JavaScript String Methods Example
```

```javascript
script.js
```

```javascript
1 / JavaScript String Methods Example
2 / String Methods
3 / let originalString = "JavaScript String";
4 / let trimmedString = originalString.trim();
5 / let upperCaseString = originalString.toUpperCase();
6 / let subString = originalString.substring(3);
7 / let replacedString = originalString.replace("Method", "Functions");
8 / // Display the results
9 / console.log("Original String: " + originalString);
10 / console.log("Trimmed String: " + trimmedString);
11 / console.log("Upper-Case String: " + upperCaseString);
12 / console.log("SubString: " + subString);
13 / console.log("Replaced String: " + replacedString);
14 / let splitString = originalString.split(" ");
15 / console.log("Split String: " + JSON.stringify(splitString));
16 / // Chaining Methods
17 / let chainedMethod = originalString.trim().toUpperCase().replace("METHODS", "OPERATIONS");
18 / console.log("Chained Methods Result: " + modifiedString);
19 / // End of JavaScript String Methods
```

```text
Console:
Original String:  JavaScript String
Trimmed String: JavaScript String
Uppercased String: JAVASCRIPT STRING
Lowercased String: javascript string
SubString: String
Replaced String: JavaScript Functions
Split String: ["JavaScript","String"]
Chained Methods: OPERATIONS
```

在此示例中，演示了各种字符串方法：

1. 字符串修剪：`let trimmedString = originalString.trim();`
2. 字符串大写：`let upperCaseString = originalString.toUpperCase();`
3. 字符串小写：`let lowercString = originalString.toLowerCase();`
4. 子字符串：`let substring = originalString.substring(5, 18);`
5. 字符串替换：`let replacedString = originalString.replace("Methods", "Functions");`
6. 分割：`let splitString = originalString.split(" ");`
7. 链式方法：以链式方式组合字符串方法。
8. 输出结果：`console.log("Original String: " + originalString); console.log("Trimmed String: " + trimmedString); console.log("Upper-Case String: " + upperCaseString); console.log("Lowercased String: " + lowercString); console.log("SubString: " + subString); console.log("Replaced String: " + replacedString); console.log("Split String: " + JSON.stringify(splitString)); console.log("Chained Methods Result: " + modifiedString);`

## JS字符串搜索

JavaScript的`search()`方法用于在字符串中搜索指定的模式。该方法通常配合正则表达式（regex）执行更复杂的搜索操作。

### 方法语法

`search()`方法在字符串上调用，并接收正则表达式模式作为参数。

### 正则表达式

正则表达式是用于对字符串搜索或匹配操作的模式。它们包含各种字符和标记，以创建灵活且强大的搜索标准。

### 返回值

`search()`方法返回指定模式在字符串中首次出现的索引。如果没有找到，则返回-1。

### 不区分大小写的搜索

默认情况下，`search()`方法执行区分大小写的搜索。要执行不区分大小写的搜索，可以在正则表达式中使用`i`标记。

### 使用捕获组

正则表达式可以包含捕获组，以便从匹配的字符串中提取特定部分。这允许你获取更多关于匹配的详细信息。

### 查找多个匹配

虽然`search()`方法返回第一个匹配的索引，但它不会找到字符串中的所有出现项。对于查找多个匹配，带有`g`标志的`match()`方法通常更加合适。

### 未找到所有匹配

`search()`方法在找到第一个匹配后就会停止。如果你需要找到所有匹配项，请考虑使用带有`g`（全局）标志的`match()`方法。

### 使用indexOf进行简单字符串搜索

对于不需要正则表达式的简单字符串搜索，`indexOf()`方法可能更加简单直接。

### 大写敏感性

在使用`search()`方法时，注意大小写敏感至关重要。如果需要不区分大小写的搜索，请考虑使用适当的正则表达式。

### 处理未匹配的情况

如果未找到模式，`search()`方法将返回`-1`。检查此返回值以处理字符串中不存在模式的情况。

理解如何配合正则表达式使用`search()`方法，对于在JavaScript中执行高级字符串搜索和模式匹配非常有价值。在处理超出简单子串匹配的复杂搜索标准时，它特别有用。

```javascript
// JavaScript String Search Example
```

```javascript
// String Search Method let originalString = "JavaScript is a powerful scripting language.";
```

```javascript
// Using indexOf 找到子串的位置
indexOfScript = originalString.indexOf("script");
```

```javascript
// Using includes 检查子串是否存在 let includesPowerful = originalString.includes("powerful");
```

```javascript
// Using search 配合正则表达式找到子串的位置 let searchLanguage = originalString.search(/language/i);

// Display Results console.log("Original String: " + originalString); console.log("Index of 'script': " + indexOfScript); console.log("Includes 'powerful': " + includesPowerful); console.log("Search language': " + searchLanguage);

// // End of JavaScript String Search Example
```

```javascript
script.js
1 // JavaScript String Search Example
2 // String Search Demo
3 let queryString = "JavaScript is a powerful searching language";
4 // 使用 indexOf 找到子串的位置
5 let indexOfScript = queryString.indexOf("script");
6 // 使用 includes 检查子串是否存在
7 let includesPowerful = queryString.includes("powerful");
8 // 使用 search 配合正则表达式找到子串的位置
9 let searchLanguage = queryString.search(/language/i);
10 // 显示结果
11 console.log("Original String: " + originalString);
12 console.log("Index of 'script': " + indexOfScript);
13 console.log("Includes 'powerful': " + includesPowerful);
14 console.log("Search language': " + searchLanguage);
15 // End of JavaScript String Search Example
```

在此示例中，演示了JavaScript字符串搜索相关方法：

1. 使用`indexOf`在原始字符串中查找子串（"script"）的位置。
2. includes：使用`includes`检查子串（"powerful"）是否存在原始字符串中。
3. search：使用`search`配合不区分大小写的正则表达式查找子串（"language"）的位置。
4. 显示结果：

```javascript
console.log("Original String: " + originalString);
console.log("Index of 'script': " + indexOfScript);
console.log("Includes 'powerful': " + includesPowerful);
console.log("Search language': " + searchLanguage);
```

这些示例展示了如何使用`indexOf`、`includes`和`search`方法执行JavaScript字符串子操作。

## JS字符串模板

JavaScript字符串模板（也称为模板字面量）是在ECMAScript 6 (ES6)中引入的，旨在提供一种更方便的处理字符串的方法。模板字面量使用反引号（`` ``）而不是单引号或双引号，并支持嵌入表达式和多行字符串。

### 反引号

模板字面量由反引号而不是单引号或双引号分隔。这使得它们在视觉上与不同，并增加了处理字符串的活性。

### 嵌入表达式

模板字面量的关键特性之一可以使用`${}`语法直接在字符串中嵌入表达式。这允许你将变量和表达式直接插到字符串中。

### 变量插值

通过将变量放在`${}`中，可以轻松地插到模板字面量中。这消除了在组合变量与字符串时显式拼接或转义的需求。

### 表达式求值

嵌入在`${}`中的表达式会被求值，其结果被转换为字符串并插入到模板中。这对于动态内容生成特别有用。

### 多行字符串

模板字面量支持多行字符串，不需要显式的换行符（`\n`）。反引号内的换行符会保留在生成的字符串中。

### 字符串格式化

模板字面量提供了一种更清晰、更易读的字符串格式化方法，特别是在处理复杂或动态内容时。

### 标签模板

模板字面量可以与标签模板一起使用，其中函数（称为标签函数）处理模板字面量及其嵌入的表达式。这允许高级的字符串操作和格式化。

### 转义序列

虽然模板字面量提供了一种更自然的方式处理多行字符串，但转义序列（例如`\n`、`\t`）仍然有效，并在需要可以使用。

### 无隐式换行延续

与单引号或双引号创建的普通字符串不同，模板字面量在代码跨越多行时没有隐式的换行延续。每一行都必须显式包含在反引号内。

### 一致的语法

模板字面量的语法是一致的，与使用拼接相比，这使得代码更容易易和和维护。

### HTML模板

模板字面量常用于创建HTML模板，其中动态内容可以无缝集成到结构中。它们的语法提供了一种处理字符串的更现代的方法。

```javascript
// JavaScript String Templates
// String Template Literal
let firstName = "John";
let lastName = "Doe";
let age = 30;
```

```javascript
let message = `My name is ${firstName} ${lastName}. I am ${age}`;
```

```javascript
// 显示 字符串模板字面量
console.log("Info Message: " + message);
```

```javascript
// 带有表达式的字符串模板
let x = 5; let y = 10;
let resultMessage = `The sum of ${x} and ${y} is ${x + y}`;
```

```javascript
// 显示带有表达式的字符串模板
console.log("Original String: " + originalString);
console.log("Index of 'script': " + indexOfScript);
console.log("Includes 'powerful': " + includesPowerful);
console.log("Search language': " + searchLanguage);

// 多行字符串模板
let multilineMessage = `This is a multi-line
string example.
it supports line breaks.`;
```

```javascript
// 显示 多行字符串模板
console.log("Multi-line Message: " + multilineMessage);
```

```javascript
// End of JavaScript String Search Example
```

## JavaScript数字

在JavaScript中，数字是一种用于表示数值的基元数据类型。

### 数值类型

JavaScript数字同时表示整数和浮点数（小数）。整数类型和浮点类型之间没有区分。

### 浮点数表示

JavaScript中的所有数字（包括整数）在内部都按照IEEE 754标准表示为64位浮点数。这允许表示宽范围的值，但在某些计算中可能会导致精度问题。

### 算术运算

JavaScript支持对数字进行各种算术运算，包括加法（`+`）、减法（`-`）、乘法（`*`）、除法（`/`）和取模（`%`）。

### Math对象

JavaScript提供了一个`Math`对象，包含执行更复杂数学运算的方法，例如三角函数、幂运算、对数和随机数生成。

### 无穷大和负无穷

JavaScript将正无穷大表示为`Infinity`，将负无穷表示为`-Infinity`。这些值用于表示数学概念，例如除以零或超过最大可表示的数值。

### NaN（不是数字）

特殊值`NaN`代表JavaScript中未定义或无法表示的值。它通常是无效数学运算的结果，例如除以零。

### 精度与四舍五入

由于浮点数表示法，JavaScript数字并不总是精确的。某些计算可能会导致舍入误差，特别是在处理小数分数时。

### 整数限制

JavaScript数字具有有限的精度，能够准确表示的最大和最小整数值存在限制。可以使用`Number.MAX_SAFE_INTEGER`和`Number.MIN_SAFE_INTEGER`常量访问这些限制。

### 解析数字

可以`parseInt()`和`parseFloat()`等函数从字符串解析数字。这些函数尝试从字符串表示中提取数值。

### Number方法

JavaScript中的`Number`对象提供了一些方法，如`isNaN()`用于检查值是否为`NaN`，`isFinite()`用于检查值是否为有限数字，以及`toFixed()`将数字四舍五入到指定的小数位数。

### 一元加和减

一元加（`+`）和一元减（`-`）运算符用于将值转换为数字或更改其符号。

### 指数计数法

JavaScript允许使用指数计数法表示极大或极小的数字。例如，`1e3`代表1000，`1e-3`代表0.001。

理解JavaScript数字的特性和行为对于准确的数学运算以及避免与浮点精度相关的潜在陷阱至关重要。开发者应该意识到JavaScript中数值运算的局限性和特性，以编写可靠高效的代码。

```javascript
// JavaScript Numbers Example
// Number Declaration
let integerNumber = 42; 
let floatingPointNumber = 3.14; 
let scientificNotation = 5.2e3; // 5200
```

```javascript
// Display Numbers
console.log("Integer Number: " + integerNumber);
console.log("Floating Point Number: " + floatingPointNumber);
console.log("Scientific Notation: " + scientificNotation);
```

```javascript
// Arithmetic Operations 
let sum = integerNumber + floatingPointNumber; 
let difference = integerNumber - floatingPointNumber; 
let product = integerNumber * floatingPointNumber; 
let quotient = integerNumber / floatingPointNumber; 
let remainder = 10 % 3; // Remainder of the division
```

```javascript
// Display Arithmetic Results 
console.log("Sum: " + sum); 
console.log("Difference: " + difference);
console.log("Product: " + product);
console.log("Quotient: " + quotient);
console.log("Remainder: " + remainder);
```

```javascript
// Increment and Decrement 
let count = 5; 
count++; 
let newCount = count--;
```

```javascript
// Display Increment and Decrement Results 
console.log("Count After Increment: " + count); 
console.log("New Count After Decrement: " + newCount);
```

```javascript
// NaN (Not a Number) 
let resultNaN = "Hello" / 2;
```

```javascript
// Display NaN Result
console.log("Result NaN: " + resultNaN);
```

```javascript
// End of JavaScript Numbers Example
```

```javascript
// JavaScript Numbers Example
// Declaration
let integerNumber = 4;
let floatingPointNumber = 3.14;
let scientificNumber = 5.26e3;
// Number Types
console.log("Integer Number: " + integerNumber);
console.log("Floating Number: " + floatingPointNumber);
console.log("Scientific Number: " + scientificNumber);
// Arithmetic Operations
let difference = integerNumber - floatingPointNumber;
let product = integerNumber * floatingPointNumber;
let quotient = integerNumber / floatingPointNumber;
let remainder = integerNumber % difference;
// Arithmetic Results
console.log("Sum: " + integerNumber + floatingPointNumber);
console.log("Difference: " + difference);
console.log("Product: " + product);
console.log("Quotient: " + quotient);
console.log("Remainder: " + remainder);
// Increment and Decrement
let count = 5;
count++;
newCount = count--;
// Increment and Decrement Results
console.log("Count After: " + count);
console.log("New Count After Decrement: " + newCount);
// NaN Result
let resultNaN = "Hello" / 2;
```

## JavaScript BigInt

虽然BigInt为需要任意精度整数的场景提供了解决方案，但需要注意的是，它在所有情况下都不是普通数字（`Number`）的替代品。BigInt不适用于涉及非整数值或需要浮点数算术的操作。

### 兼容性

现代JavaScript环境支持BigInt，但旧版本的浏览器或环境可能无法完全支持它。在Web应用中使用BigInt时，务必考虑兼容性。

BigInt是JavaScript的一个非常有用的补充，特别是对于需要精确整数算术且需要克服普通数字局限性的场景。它为开发者提供了一种处理大整数的方法，而不会牺牲精度或遇到舍入问题。

```javascript
// JavaScript BigInt declaration
let regularNumber = 42;
let bigIntNumber = BigInt("9007199254740991"); // Maximum safe integer value
```

```javascript
// Display Numbers
console.log("Regular Number: " + regularNumber);
console.log("BigInt Number: " + bigIntNumber);
```

```javascript
// BigInt Operations
let sumBigInt = bigIntNumber + BigInt(42);
let multiplyBigInt = bigIntNumber * BigInt(3);
```

```javascript
// Display BigInt Results
console.log("Sum with BigInt: " + sumBigInt);
console.log("Multiplication with BigInt: " + multiplyBigInt);
```

```javascript
// Mixing BigInt with Regular Numbers (TypeError)
// Uncommenting the following line will result in a TypeError:
// let mixedResult = bigIntNumber + 42;

// End of JavaScript BigInt Example
```

```javascript
script.js
// JavaScript BigInt Example
// BigInt Declaration
let regularNumber = 42;
let bigIntNumber = BigInt("9007199254740991"); // Maximum safe integer
// Displaying Numbers
console.log("Regular Number: " + regularNumber);
console.log("BigInt Number: " + bigIntNumber);
// BigInt Operations
let sumInt = bigIntNumber + BigInt(4);
let multiplyInt = bigIntNumber * BigInt(3);
// Results
console.log("Sum with BigInt: " + sumInt);
console.log("Multiplication with BigInt: " + multiplyInt);
// Mixing BigInt with Regular Numbers (TypeError)
// Attempting to mix will result in a TypeError:
let mixedResult = regularNumber + 42;
// End of JavaScript BigInt Example
```

在此示例中，演示了JavaScript BigInt：

1. BigInt声明：`let bigIntNumber = BigInt("9007199254740991");`
2. 显示数字：`console.log("Regular Number: " + regularNumber); console.log("BigInt Number: " + bigIntNumber);`
3. BigInt操作：使用BigInt进行基础算术操作。
4. 显示BigInt结果：`console.log("Sum with BigInt: " + sumBigInt); console.log("Multiplication with BigInt: " + multiplyInt);`
5. BigInt与普通数字混合（TypeError）：尝试将BigInt与普通数字混合会导致`TypeError`。

注意：当处理超过JavaScript安全整数范围的极大整数值时，BigInt非常有用。涉及BigInt的操作必须显式使用BigInt执行，以避免精度丢失。在某些操作中将BigInt与普通数字混合可能会导致`TypeError`。

## JS Number方法

JavaScript提供了与`Number`对象相关的多种方法，可用于对数值执行操作。

### isNaN(value)

`isNaN(value)`方法检查一个值是否为`NaN`（不是数字）。如果该值是`NaN`，则返回`true`；如果它是有效数字或可以转换为数字，则返回`false`。

### isFinite(value)

`isFinite(value)`方法检查一个值是否为有限数字（不是`Infinity`或`-Infinity`）。如果该值是有限的且可以表示为数字，则返回`true`；否则返回`false`。

### parseFloat(string)

`parseFloat(string)`方法解析字符串并返回它遇到的第一个浮点数。它常用于从字符串中提取数值。

### parseInt(string, radix)

`parseInt(string, radix)`方法解析字符串并根据提供的基数（`radix`）返回一个整数。它通常用于将字符串格式的数字转换为整数。

### toExponential(fractionDigits)

`toExponential(fractionDigits)`方法返回一个用科学计数法表示数字的字符串。可选的`fractionDigits`参数指定小数点后的位数。

### toFixed(digits)

`toFixed(digits)`方法返回一个带有小数点后固定位数数字的字符串。必要时，它会对数字进行四舍五入。

### toPrecision(precision)

`toPrecision(precision)`方法返回一个具有指定精度的数字字符串。它包含了数字的整数和小数部分。

### toString(radix)

`toString(radix)`方法根据指定的基数（`radix`）将数字转换为字符串。这有助于在不同的进制系统（如二进制或十六进制）中表示数字。

### valueOf()

`valueOf()`方法返回`Number`对象的原始值。JavaScript在需要数值转换时会自动调用该方法。

### 用于字符串格式化的toFixed()、toPrecision()和toExponential()

这些方法用于格式化数值以供显示，例如在用户界面中，此时小数的位数或整体精度非常重要。

### 算术操作

虽然有`Number`对象的方法，但算术操作（`+`、`-`、`*`、`/`）以及`Math`对象提供了常用于数值的各种数学函数。

### 常量

`Number`对象包含了常量，例如`Number.MAX_VALUE`（JavaScript中可表示的最大数字）、`Number.MIN_VALUE`（最小正表示数）等。

理解并利用这些`Number`方法对于在JavaScript中处理和格式化数值至关重要。这些方法为开发者提供了工具，用于在应用程序中转换、格式化和检查数值的属性。

```javascript
// JavaScript Number Methods Example
```

```javascript
// Number Methods
let originalNumber = 123.456;
let fixedNumber = originalNumber.toFixed(2);
let roundedNumber = Math.round(originalNumber);
let absoluteNumber = Math.abs(-5);
let powerNumber = Math.pow(2, 3);
let squareRoot = Math.sqrt(25);
let randomDecimal = Math.random(); // 生成 0 到 1 之间的随机小数
let randomNumber = Math.floor(Math.random() * 10) + 1; // 生成 1 到 10 之间的随机整数

// Display Results of Number Methods
console.log("Original Number: " + originalNumber);
console.log("Fixed Number (2 decimal places): " + fixedNumber);
console.log("Rounded Number: " + roundedNumber);
console.log("Absolute Number: " + absoluteNumber);
console.log("2 to the power of 3: " + powerNumber);
console.log("Square Root of 25: " + squareRoot);
console.log("Random Decimal: " + randomDecimal);
console.log("Random Integer between 1 and 10: " + randomNumber);

// End of JavaScript Methods
```

```javascript
script.js
// JavaScript Number Methods Example
let originalNumber = 123.456;
let fixedNumber = originalNumber.toFixed(2);
let roundedNumber = Math.round(originalNumber);
let absoluteNumber = Math.abs(-5);
let powerNumber = Math.pow(2, 3);
let squareRoot = Math.sqrt(25);
let randomDecimal = Math.random(); // 生成 0 到 1 之间的随机小数
let randomNumber = Math.floor(Math.random() * 10) + 1; // 生成 1 到 10 之间的随机整数

// Display Results of Number Methods
console.log("Original Number: " + originalNumber);
console.log("Fixed Number (2 decimal places): " + fixedNumber);
console.log("Rounded Number: " + roundedNumber);
console.log("Absolute Number: " + absoluteNumber);
console.log("2 to the power of 3: " + powerNumber);
console.log("Square Root of 25: " + squareRoot);
console.log("Random Decimal: " + randomDecimal);
console.log("Random Integer between 1 and 10: " + randomNumber);

// End of JavaScript Methods
```

### Math.round

将数字四舍五入到最接近的整数。`let roundedNumber = Math.round(originalNumber);`

### Math.abs

获取数字的绝对值。`let absoluteNumber = Math.abs(-5);`

### Math.pow

计算数字的幂。`let powerNumber = Math.pow(2, 3);`

### Math.sqrt

计算数字的平方根。`let squareRoot = Math.sqrt(25);`

### Math.random

生成随机小数和整数值。`let randomDecimal = Math.random();` `let randomInteger = Math.floor(Math.random() * 10) + 1;`

### 显示结果

```javascript
console.log("Original Number: " + originalNumber); 
console.log("Fixed Number (2 decimal places): " + fixedNumber);
console.log("Rounded Number: " + roundedNumber);
console.log("Absolute Number: " + absoluteNumber); 
console.log("Square Root of 25: " + squareRoot);
console.log("Random Decimal: " + randomDecimal);
console.log("Random Integer (between 1 and 10): " + randomInteger);
```

这些示例涵盖了JavaScript中处理数字的常用方法，包括四舍五入、绝对值、幂、平方根和随机数生成。

## JS数字属性

JavaScript的`Number`对象包含几个属性，提供了有关数值的信息，并定义了某些限制。

### Number.MAX_VALUE

`Number.MAX_VALUE`属性代表JavaScript中可以表示的最大正数值。该值约为`1.7976931348623157e+308`。

### Number.MIN_VALUE

`Number.MIN_VALUE`属性代表JavaScript中可以表示的大于零的最小正数值。它是最小正非规格化浮点数的正等值。该值约为`5e-324`。

### Number.POSITIVE_INFINITY

`Number.POSITIVE_INFINITY`属性表示正无穷大。这是一个特殊值，用于表示超出正数表示范围的数学运算结果。

### Number.NEGATIVE_INFINITY

`Number.NEGATIVE_INFINITY`属性表示负无穷大。与正无穷大类似，它用于表示超出负数表示范围的数学运算结果。

### Number.NaN

`Number.NaN`属性表示特殊值“不是一个数字”（`NaN`）。当数学运算产生未定义或不可接受的结果时，返回此值。

### Number.EPSILON

`Number.EPSILON`属性表示1与大于1的最小可表示数字之间的差。这是一个极小的值，可以用于对浮点数安全比较。

### Number.MAX_SAFE_INTEGER

`Number.MAX_SAFE_INTEGER`属性代表JavaScript中的最大安全整数值。它是可以在不丢失精度的情况下准确表示的最大整数。该值为`9007199254740991`。

### Number.MIN_SAFE_INTEGER

`Number.MIN_SAFE_INTEGER`属性代表JavaScript中的最小安全整数值。它是可以在不丢失精度的情况下准确表示的最小整数。该值为`-9007199254740991`。

### Number.isFinite()

`Number.isFinite()`方法不是属性，而是`Number`对象的静态方法。它检查一个值是否为有限数字，如果该值是有限数字（不是`NaN`、`Infinity`或`-Infinity`），则返回`true`；否则返回`false`。

### Number.isNaN()

`Number.isNaN()`方法不是属性，而是`Number`对象的静态方法。它检查一个值是否为`NaN`，如果该值是`NaN`，则返回`true`；否则返回`false`。

这些属性对于处理JavaScript中的数值非常有用，它们提供了有关与数值计算相关的范围、精度和特殊值的信息。理解这些属性对于编写涉及数值运算的健壮且可靠的JavaScript代码至关重要。

```javascript
// JavaScript 数字属性示例

// 数字属性
let maxSafeInteger = Number.MAX_SAFE_INTEGER; 
let minSafeInteger = Number.MIN_SAFE_INTEGER; 
let maxNumberValue = Number.MAX_VALUE; 
let minNumberValue = Number.MIN_VALUE; 
let positiveInfinity = Number.NEGATIVE_INFINITY; 
let notANumber = Number.NaN;

// 显示数字属性
console.log("Max Safe Integer: " + maxSafeInteger);
console.log("Min Safe Integer: " + minSafeInteger);
console.log("Max Number Value: " + maxNumberValue);
console.log("Min Number Value: " + minNumberValue);
console.log("Positive Infinity: " + positiveInfinity);
console.log("Not a Number: " + notANumber);
```

## JavaScript数组

数组在创建后可以被修改。你可以通过给现有元素分配新值来更改它的值。

### 长度属性（Length）

数组具有`length`属性，表示数组中元素的数量。它可以用于遍历元素或确定数组的大小。

### 常用数组操作

数组支持各种操作，例如添加元素（`push()`和`unshift()`）、删除元素（`pop()`和`shift()`）以及切片和拼接数组。

### 迭代

可以使用循环（例如`for`循环）或高阶函数如`forEach()`、`map()`、`filter()`和`reduce()`对数组进行迭代。

### 数组方法

JavaScript内置方法来执行常用操作，如`concat()`、`slice()`、`indexOf()`、`includes()`等。

### 嵌套数组

数组可以包含其他数组，创建嵌套结构。这允许创建多维数组或更复杂的数据结构。

### 类对象行为

在JavaScript中，数组是具有整数键的对象，并且它们继承自`Array`原型。然而，它们也拥有数组特定的方法和行为。

### 数组字面量

可以使用数组字面量创建数组，这涉及到在方括号（`[]`）内部包含一个值列表。

### 稀疏数组

JavaScript允许稀疏数组，其中某些索引可能没有对应的元素。`length`属性反映数组中的最高索引。

### 解构赋值

可以使用解构语法轻松地提取并赋值数组元素。

### 用例

数组被广泛用于各种任务，如存储数据集合、表示序列、实现栈和队列以及管理有序元素集。

理解数组是JavaScript编程的基础，因为它们提供了一种通用且高效的方式以结构化的处理数据集合。数组是许多算法的核心组件，并在Web开发中被广泛用于从处理项目列表到管理复杂数据结构的各种任务。

```javascript
// JavaScript 数组示例

// 数组声明
let fruits = ["Apple", "Banana", "Orange", "Mango"];

// 访问数组元素
let firstFruit = fruits[0];
let lastFruit = fruits[fruits.length - 1];

// 修改数组元素
fruits[1] = "Grapes";

// 在末尾添加元素
fruits.push("Pineapple");

// 从末尾删除元素
let removedFruit = fruits.pop();

// 显示数组和结果
console.log("Fruits Array: " + JSON.stringify(fruits));
console.log("First Fruit: " + firstFruit);
console.log("Last Fruit: " + lastFruit);
console.log("Removed Fruit: " + removedFruit);

// JavaScript 数组示例结束
```

```javascript
// JavaScript 数组示例
// 数组声明
let fruits = ["Apple", "Banana", "Orange", "Mango"];

// 访问数组元素
let firstFruit = fruits[0];
let lastFruit = fruits.length - 1;

// 修改数组元素
fruits[1] = "Mango";

// 从末尾删除元素
let removedFruit = fruits.pop();

// 显示数组和结果
console.log("Fruits Array: " + JSON.stringify(fruits));
console.log("First Fruit: " + firstFruit);
console.log("Last Fruit: " + lastFruit);
console.log("Removed Fruit: " + removedFruit);
```

```text
Fruits Array: ["Apple", "Grapes", "Orange", "Mango"]
First Fruit: Apple
Last Fruit: Mango
Removed Fruit: Pineapple
```

在这个示例中，演示了JavaScript数组：

1. 数组声明：`let fruits = ["Apple", "Banana", "Orange", "Mango"];`
2. 访问数组元素：`let firstFruit = fruits[0]; let lastFruit = fruits[fruits.length - 1];`
3. 修改数组元素：`fruits[1] = "Grapes";`
4. 在末尾添加元素：`fruits.push("Pineapple");`
5. 从末尾删除元素：`let removedFruit = fruits.pop();`
6. 显示数组和结果：`console.log("Fruits Array: " + JSON.stringify(fruits)); console.log("First Fruit: " + firstFruit); console.log("Last Fruit: " + lastFruit); console.log("Removed Fruit: " + removedFruit);`

这个示例涵盖了数组的基本操作，包括声明、访问元素、修改元素、在末尾添加元素以及从末尾删除元素。

## JS数组方法

JavaScript提供了多种内置方法可用于操作数组。

### concat()

`concat()`方法用于合并两个或多个数组，创建一个包含合并后元素的新数组。

### filter()

`filter()`方法创建一个包含特定元素的新数组。它不会修改原始数组。

### map()

`map()`方法通过对原始数组中的每个元素应用函数来创建一个新数组。它根据提供的函数转换每个元素。

### find()

`find()`方法返回数组中第一个满足指定条件的元素。它不会修改原始数组。

### indexOf()

`indexOf()`方法返回指定元素在数组中首次位置的索引。如果未找到该元素，则返回-1。

### includes()

`includes()`方法检查数组是否包含指定元素。如果找到了该元素则返回`true`，否则返回`false`。

### push()

`push()`方法向数组末尾添加一个或多个元素，并返回新长度。

### pop()

`pop()`方法从数组末尾删除一个元素并返回被删除的元素。

### shift()

`shift()`方法从数组开头删除一个元素并返回被删除的元素。

### unshift()

`unshift()`方法向数组开头添加一个或多个元素并返回新长度。

### splice()

`splice()`方法通过删除或添加新元素更改数组内容。

### slice()

`slice()`方法返回数组部分的浅拷贝作为新数组。它不会修改原始数组。

### reverse()

`reverse()`方法反转数组元素的顺序。它会修改原始数组。

### join()

`join()`方法使用指定的分隔符将数组元素连接成字符串。

### sort()

`sort()`方法对数组元素进行排序。默认排序基于将元素转换为字符串并比较UTF-16代码单元。

### reduce()

`reduce()`方法对累加器和数组中的每个元素（从左到右）应用函数，将其还原为单个值。

### forEach()

`forEach()`方法为每个元素执行一次提供的函数。它不返回数组。

### some()

`some()`方法测试数组中至少有一个元素通过了提供的函数的测试。

### every()

`every()`方法测试数组中所有元素是否都通过了提供的函数的测试。

这些数组方法提供了一组强大的工具，用于在JavaScript中处理数组。它们允许开发者以一致高效的方式执行过滤、映射、查找元素和修改数组内容等操作。理解这些方法对于有效地操作数组至关重要。

```javascript
// JavaScript 数组方法示例

// 数组声明
let numbers = [4, 2, 8, 5, 1];
```

```javascript
// 数组方法
let sortedNumbers = numbers.sort((a, b) => a - b);
let reversedNumbers = numbers.reverse();
let slicedNumbers = numbers.slice(1, 4);
let indexOfNumber = numbers.indexOf(8);
let includeNumber = numbers.includes(3);
let mappedNumbers = numbers.map(num => num * 2);
let filteredNumbers = numbers.filter(num => num > 3);
let sumOfNumbers = numbers.reduce((sum, num) => sum + num, 0);
```

```javascript
// 显示数组方法的结果
console.log("Original Numbers Array: " + JSON.stringify(numbers));
console.log("Sorted Numbers Array: " + JSON.stringify(sortedNumbers));
console.log("Reversed Numbers Array: " + JSON.stringify(reversedNumbers));
console.log("Sliced Numbers Array: " + JSON.stringify(slicedNumbers));
console.log("Index of Number 8: " + indexOfNumber);
console.log("Includes Number 3: " + includesNumber);
console.log("Mapped Numbers Array: " + JSON.stringify(mappedNumbers));
console.log("Filtered Numbers Array: " + JSON.stringify(filteredNumbers));
console.log("Sum of Numbers: " + sumOfNumbers);
```

```javascript
// JavaScript数组方法示例结束
```

```javascript
script.js
// JavaScript数组方法示例
// 数组声明
let numbers = [4, 0, 5, 3];
// 排序
let sortedNumbers = numbers.sort((a, b) => a - b);
let reversedNumbers = numbers.reverse();
let included = numbers.includes(3);
let indexOfNumber = numbers.indexOf(0);
let filteredNumbers = numbers.filter(num => num > 2);
let sumOfNumbers = numbers.reduce((sum, num) => sum + num, 0);

// 输出结果
console.log("Original Numbers Array: " + JSON.stringify(numbers));
console.log("Reversed Numbers: " + JSON.stringify(reversedNumbers));
console.log("Filtered Numbers: " + JSON.stringify(filteredNumbers));
console.log("Index of Number 0: " + indexOfNumber);
console.log("Included: " + included);
console.log("Mapped Numbers: " + JSON.stringify(mappedNumbers));
console.log("Filtered Numbers: " + JSON.stringify(filteredNumbers));
console.log("Sum of Numbers: " + sumOfNumbers);

// JavaScript数组方法示例结束
```

在这个示例中，演示了JavaScript数组方法：

- sort：将数组按升序排序。`let sortedNumbers = numbers.sort((a, b) => a - b);`
- reverse：反转数组元素的顺序。`let reversedNumbers = numbers.reverse();`
- slice：提取数组的部分。`let slicedNumbers = numbers.slice(1, 4);`
- indexOf：查找数组中特定元素的索引。`let indexOfNumber = numbers.indexOf(0);`
- includes：检查特定元素是否存在。`let included = numbers.includes(3);`
- map：创建一个每个元素都是原来两倍的新数组。`let mappedNumbers = numbers.map(num => num * 2);`
- filter：创建一个包含大于3的元素的新数组。`let filteredNumbers = numbers.filter(num => num > 3);`
- reduce：计算数组中所有元素的和。`let sumOfNumbers = numbers.reduce((sum, num) => sum + num, 0);`

显示结果：

```javascript
console.log("Original Numbers Array: " + JSON.stringify(numbers));
console.log("Sorted Array: " + JSON.stringify(sortedNumbers));
console.log("Reversed Array: " + JSON.stringify(reversedNumbers));
console.log("Sliced Numbers Array: " + JSON.stringify(slicedNumbers));
console.log("Index of Number: " + indexOfNumber);
console.log("Number 3: " + includedNumber);
console.log("Mapped Numbers Array: " + JSON.stringify(mappedNumbers));
console.log("Filtered Array: " + JSON.stringify(filteredNumbers));
console.log("Sum of Numbers: " + sumOfNumbers);
```

这些示例涵盖了JavaScript中处理数组的常用方法，包括排序、反转、切片、搜索、映射、过滤和还原。

## JS数组排序

JavaScript中的`sort()`方法用于对数组元素进行排序。

### 默认排序

默认情况下，`sort()`方法将数组元素作为字符串进行排序。这意味着元素会被转换为字符串并根据它们的UTF-16单元值进行排序。

### 原地排序

`sort()`方法执行原地排序，这意味着它会修改原始数组而不是创建新数组。

### 数字排序

在对数值进行排序时，默认行为可能无法产生预期的结果。为了实现数字排序，可以提供一个比较函数作为`sort()`方法的参数。

### 比较函数

比较函数是一个定义排序顺序的回调函数。它接受两个参数（通常称为`a`和`b`），并返回一个负值、零或正值，表示两个元素的相对顺序。

### 升序

如果比较函数返回负值，则`a`将放在`b`之前，从而形成升序。

### 降序

如果比较函数返回正值，则`b`将放在`a`之前，从而形成降序。

### 稳定性

JavaScript引擎使用的`sort()`算法不保证是稳定性的。这意味着相等元素的顺序可能无法保留。

### 默认字典排序

对于字符串，默认的字典（lexicographic）排序并不总是能产生直观的结果。对于更复杂的排序，可以提供自定义的比较函数。

### Unicode排序

默认排序顺序基于Unicode代码点值。在排序具有来自不同脚本字符的字符串时，可能会导致意想不到的结果。

### 字母顺序排序

若要执行不区分大小写的字母顺序排序，可以使用不区分大小写的比较函数。

### 时间复杂度

`sort()`方法的时间复杂度取决于特定的JavaScript引擎，但通常是O(n log n)。

### 边界情况

`sort()`方法是一个用于元素排序的多功能工具，特别是在处理对象特定排序时。

## JS数组迭代

### reduce()

`reduce()`方法用于对数组元素进行迭代计算。它将提供的函数应用于累加器和数组中的每个元素（从左到右），从而将其还原为单个值。

### some()和every()

`some()`方法测试数组中是否至少有一个元素通过由提供的函数实现的测试。`every()`方法测试数组中是否所有元素都通过了测试。

### 迭代方法

ES6引入了可迭代对象和迭代器的概念。数组迭代可以使用`for...of`循环以及`keys()`、`values()`等方法执行。

### 回调函数与异步迭代

用于数组迭代的回调函数可以是同步的或异步的。现代JavaScript还支持使用`for...of`异步函数进行异步迭代。

数组迭代是JavaScript编程中的基础概念，选择合适的迭代方法取决于任务的具体要求。理解这些迭代方法对于在JavaScript中有效操作和处理数组至关重要。

```javascript
// JavaScript 数组迭代示例
```

```javascript
// 数组声明 let numbers = [1, 2, 3, 4, 5];
```

```javascript
// forEach 方法 console.log("Using forEach Method:");
numbers.forEach(function (number) {
  console.log(number);
});
```

```javascript
// map 方法 console.log("Using map Method:");
let doubledNumbers = numbers.map(function (number) {
  return number * 2;
});
console.log("Doubled Numbers: " + JSON.stringify(doubledNumbers));
```

```javascript
// filter 方法 console.log("Using filter Method:"); let evenNumbers = numbers.filter(function (number) {
  return number % 2 === 0;
});
console.log("Even Numbers: " + JSON.stringify(evenNumbers));
```

```javascript
// reduce 方法
console.log("using Reduce Method:"); let sumOfNumbers = numbers.reduce(function (sum, number) { return sum + number; }, 0);
console.log("Sum of Numbers: " + sumOfNumbers);

// JavaScript 数组迭代示例结束
```

```javascript
// JavaScript 数组迭代示例

// 数组声明
let numbers = [1, 2, 3, 4, 5];

console.log("using forEach Method:");
numbers.forEach(function (number) {
  console.log(number);
});

// map 方法
let doubledNumbers = numbers.map(function (number) {
  return number * 2;
});
console.log("Doubled Numbers: " + doubledNumbers);

// filter 方法
let evenNumbers = numbers.filter(function (number) {
  return number % 2 === 0;
});
console.log("Even Numbers: " + evenNumbers);

// reduce 方法
console.log("using reduce Method:");
let sum = numbers.reduce(function (sum, number) {
  return sum + number;
}, 0);
console.log("Sum of Numbers: " + sum);

// JavaScript 数组迭代示例结束
```



## JavaScript 数组迭代方法

在此示例中，演示了各种 JavaScript 数组迭代方法：

### forEach

遍历数组中的每个元素。

```javascript
numbers.forEach(function (number) {
  console.log(number);
});
```

### map

通过对每个元素应用函数来创建一个新数组。

```javascript
let doubledNumbers = numbers.map(function (number) {
  return number * 2;
});
```

### filter

创建一个包含符合条件元素的新数组。

```javascript
let evenNumbers = numbers.filter(function (number) {
  return number % 2 === 0;
});
```

### reduce

通过应用函数将数组归约为一个单个值。

```javascript
let sumOfNumbers = numbers.reduce(function (sum, number) { return sum + number; }, 0);
```

```javascript
console.log("Using forEach Method:");
console.log("Using filter Method:");
console.log("Using reduce Method:");
```

这些示例演示了使用`forEach`、`map`、`filter`和`reduce`方法迭代和处理 JavaScript 数组中的元素。

## JS 数组 const

在 JavaScript 中，`const`关键字用于声明常量，即在初始设置后值无法重新赋值的变量。当`const`用于数组时，它并不会使数组不可变；而是防止变量被赋值为不同的数组。

### 数组引用的不可变性

当使用`const`声明数组时，数组的引用不能被重新赋值。这意味着变量本身（持有引用）不能指向不同的数组。

### 数组元素的可变性

然而，使用`const`并不会使数组的单个元素变为不可变。你仍然可以修改数组的内容，包括添加、删除或修改元素。

### 防止重新赋值

如果你使用`const`声明数组，尝试将变量重新赋值为不同的数组会导致错误。这对于防止意外重新赋值并确保变量始终指向同一个数组非常有用。

### 块作用域

与其他使用`const`声明的变量一样，数组变量是块级作用的。它只在定义它的块或函数内是可访问的。

### 对象属性

如果使用`const`声明数组，其属性（或元素）仍然可以被修改。

## JS 日期

在 JavaScript 中，`Date`对象用于处理日期和时间。它提供了创建、格式化和操作日期的方法。

### Date 对象创建

使用`Date()`构造函数创建`Date`对象。可以在不传递任何参数的情况下创建，此时它代表当前的日期和时间；可以使用各种参数指定日期和时间。

### 时间戳

在 JavaScript 中，日期表示为自“纪元”的毫秒数，纪元是 UTC 1970 年 1 月 1 日 00:00:00。这个时间点通常被称为“Unix 时间戳”或“纪元时间”。

### 日期组件

`Date`对象表示特定的时间点，并包含年、月、日、时、分、秒和毫秒等组件。可以使用各种方法访问并修改这些组件。

### UTC 与本地时间

`Date`对象提供了`getUTC...()`和`setUTC...()`方法，用于使用协调世界时（UTC）而不是本地时间。这在处理时区差异时非常重要。

### 日期解析

可以使用`Date.parse()`方法或通过向`Date`构造函数传递日期字符串从字符串解析日期。日期字符串格式遵循特定语法，解析行为在不同环境中可能会有所差异。

### 日期格式化

`Date`对象提供了`toString()`、`toLocaleString()`、`toISOString()`等方法，根据各种约定和本地区域获取格式化的日期字符串。

### 算术运算

日期可以用于算术运算，例如计算两个日期之间的差值。`Date`对象可以用于算术运算。通过加减毫秒数可以偏移日期和时间。

### 比较

使用关系运算符（`<`、`<=`、`>=`）对`Date`对象进行比较。比较基于内部表示（自纪元以来的毫秒数）。

### 闰年

`Date`对象考虑了闰年，并能够正确处理每月的天数，在必要时会考虑闰年。

### 夏令时 (DST)

`Date`对象会根据系统时区设置自动调整夏令时的变化。

### 时间戳

`Date`对象的`getTime()`方法返回自纪元以来的毫秒数，为特定的日期时间提供时间戳。

### 局限性

虽然`Date`对象功能强大，但它也有一些局限性，例如不支持本地时区以外的时区，并且依赖于系统的计时设置。

理解`Date`对象对于在 JavaScript 中处理日期和时间至关重要。它为处理日期和时间的各个方面提供了广泛的功能，其方法可以用于创建涉及时间敏感操作的动态交互式 Web 应用程序。

```javascript
// JavaScript Dates Example

// Current Date

let currentDate = new Date();

console.log("Current Date: " + currentDate);
```

```javascript
// Specific Date

let specificDate = new Date("2023-12-31");

console.log("Specific Date: " + specificDate);
```

```javascript
// Creating Date with Components

let dateWithComponents = new Date(2023, 11, 12, 30, 0);

console.log("Date with Components: " + dateWithComponents);
```

```javascript
// Displaying Date Components

console.log("Year: " + currentDate.getFullYear());

console.log("Month: " + (currentDate.getMonth() + 1)); // Months are zero-based

console.log("Day: " + currentDate.getDate());

console.log("Hour: " + currentDate.getHours());

console.log("Minute: " + currentDate.getMinutes());

console.log("Second: " + currentDate.getSeconds());
```

```javascript
// script.js

// JavaScript Date Example

// Current Date

let currentDate = new Date();

console.log("Current Date: " + currentDate);

// Specific Date

let specificDate = new Date("2023-12-31");

console.log("Specific Date: " + specificDate);

// Creating Date with Components

let dateWithComponents = new Date(2023, 11, 12, 30, 0);

console.log("Date with Components: " + dateWithComponents);

// Displaying Date Components

console.log("Year: " + currentDate.getFullYear());

console.log("Month: " + (currentDate.getMonth() + 1)); // Months are zero-based

console.log("Day: " + currentDate.getDate());

console.log("Hour: " + currentDate.getHours());

console.log("Minute: " + currentDate.getMinutes());

console.log("Second: " + currentDate.getSeconds());

// End of JavaScript Date Example
```

在此示例中，演示了 JavaScript `Date`对象：

1. 当前日期：`let currentDate = new Date();`
2. 特定日期：`let specificDate = new Date("2023-12-31");`
3. 使用组件创建日期：`let dateWithComponents = new Date(2023, 11, 31, 12, 30, 0);`
4. 显示日期组件：

```javascript
console.log("Year: " + currentDate.getFullYear());
console.log("Month: " + (currentDate.getMonth() + 1)); // 月份从0开始
console.log("Day: " + currentDate.getDate());
console.log("Hour: " + currentDate.getHours());
console.log("Minute: " + currentDate.getMinutes());
console.log("Second: " + currentDate.getSeconds());
```

这些示例涵盖了如何使用 JavaScript 创建`Date`对象、指定特定日期、使用单个组件创建日期以及显示各种日期组件。

## JS 日期格式

在 JavaScript 中，日期格式指的是日期以字符串形式呈现的方式。`Date`对象提供了获取日期组件的方法，这些组件可以组合起来创建格式化的日期字符串。

### 组件

日期组件包括年、月、日、时、分、秒和毫秒。可以使用`getFullYear()`、`getMonth()`、`getDate()`、`getHours()`、`getMinutes()`、`getSeconds()`和`getMilliseconds()`等方法获取这些组件。

### 常见格式标识符

格式标识符是在构建格式化日期字符串时代表日期组件的占位符。常见的标识符包括：

- `%Y`：四位年份（例如 2022）
- `%M`：两位月份（01 到 12）
- `%D`：月中的两位日期（01 到 31）
- `%H`：两位小时
- `%m`：两位分
- `%S`：两位秒
- `%L`：毫秒

### 特定语言区域的格式

`toLocaleString()`方法根据指定的语言区域返回字符串。

### UTC 格式

`getUTCString()`方法返回协调世界时的日期格式。

### 自定义格式

开发者可以通过向`toLocaleString()`传递选项来创建自定义格式。

```javascript
console.log("Locale Date: " + localeDate);
console.log("Locale Time: " + localeTime);
console.log("Custom Format: " + customFormat);
```

这些示例展示了在 JavaScript 中使用`Date()`、`toISOString()`、`toLocaleString()`和`toTimeString()`等方法结合自定义选项来格式化日期组件的不同方法。

## JS Date 获取方法

在 JavaScript 中，`Date`对象提供了多种方法来获取日期的各个部分。这些方法通常以`get`开头，允许你获取有关`Date`对象的年、月、日、时、分、秒和毫秒的信息。

### getFullYear()

`getFullYear()`方法返回日期的四位年份。

### getMonth()

`getMonth()`方法返回日期的月份，值从 0 开始（1 月为 0，2 月为 1，以此类推）。

### getDate()

`getDate()`方法返回月份中的几号（1 到 31）。

### getDay()

`getDay()`方法返回星期几，值从 0 开始（0 为周日，1 为周一，以此类推）。

### getHours()

`getHours()`方法返回日期的小时（0 到 23）。

### getMinutes()

`getMinutes()`方法返回日期的分（0 到 59）。

### getSeconds()

`getSeconds()`方法返回日期的秒（0 到 59）。

### getMilliseconds()

`getMilliseconds()`方法返回日期的毫秒（0 到 999）。

### getTime()

`getTime()`方法返回自纪元（1970 年 1 月 1 日 00:00:00 UTC）以来的毫秒数。

### getTimezoneOffset()

`getTimezoneOffset()`方法返回本地时间与 UTC 之间的偏移量（分钟）。它考虑了当前的日期和时间。

### UTC 方法

此外，还有这些方法的 UTC 版本，例如`getUTCFullYear()`、`getUTCMonth()`、`getUTCDate()`等。这些方法返回协调世界时（UTC）的组件。

### 闰年检查

虽然没有特定的`getLeapYear()`方法，但你可以通过检查`getMonth()`是否返回 1（2 月）且`getDate()`设置为 29 来判断某年是否为闰年。

这些`get`方法在 JavaScript 中处理`Date`对象时获取日期的特定组件非常有用。它们允许开发者根据各种应用程序（如日期格式化、计算或在用户界面中显示信息）访问并操作日期的各个部分。

```javascript
// JavaScript Date 方法示例

// 创建一个 Date 对象

let currentDate = new Date();

// Date 获取方法

let year = currentDate.getFullYear();

let month = currentDate.getMonth(); // 月份从 0 开始 (0-11)

let day = currentDate.getDate();

let hours = currentDate.getHours();

let minutes = currentDate.getMinutes();

let seconds = currentDate.getSeconds();

let milliseconds = currentDate.getMilliseconds();

let dayOfWeek = currentDate.getDay(); // 星期 (0-6, 0 是周日)

// 显示获取方法的结果

console.log("Current Date: " + currentDate);

console.log("Year: " + year);

console.log("Month: " + month);

console.log("Day: " + day);

console.log("Hours: " + hours);

console.log("Minutes: " + minutes);

console.log("Seconds: " + seconds);

console.log("Milliseconds: " + milliseconds);

console.log("Day of Week: \n" + dayOfWeek);

// JavaScript Date 方法示例结束
```

```javascript
// script.js

// JavaScript Date 方法示例

// 创建当前日期

let currentDate = new Date();

// Date 获取方法

let year = currentDate.getFullYear();

let month = currentDate.getMonth(); // 月份从 0 开始 (0-11)

let date = currentDate.getDate();

let hours = currentDate.getHours();

let minutes = currentDate.getMinutes();

let seconds = currentDate.getSeconds();

let milliseconds = currentDate.getMilliseconds();

let dayWeek = currentDate.getDay(); // 星期 (0-6, 0 是周日)

// 显示结果

console.log("Current date: " + currentDate);

console.log("Year: " + year);

console.log("Month: " + month);

console.log("Date: " + date);

console.log("Hours: " + hours);

console.log("Minutes: " + minutes);

console.log("Seconds: " + seconds);

console.log("Milliseconds: " + milliseconds);

console.log("Day of Week: " + dayWeek);

// JavaScript Date 方法示例结束
```

在此示例中，演示了 JavaScript `Date`对象方法：

1. 创建`Date`对象：`let currentDate = new Date();`
2. `Date`方法：`let year = currentDate.getFullYear(); let month = currentDate.getMonth(); let date = currentDate.getDate(); let hours = currentDate.getHours(); let minutes = currentDate.getMinutes(); let seconds = currentDate.getSeconds(); let milliseconds = currentDate.getMilliseconds(); let dayOfWeek = currentDate.getDay();`
3. 获取方法的结果：

```javascript
console.log("Current date: " + currentDate);
console.log("Year: " + year);
console.log("Month: " + month);
console.log("Day: " + day);
console.log("Hours: " + hours);
console.log("Minutes: " + minutes);
console.log("Seconds: " + seconds);
console.log("Milliseconds: " + milliseconds);
console.log("Day of Week: \n" + dayOfWeek);
```

## JS Date 设置方法

```javascript
currentDate.setFullYear(2022);

currentDate.setMonth(11);

currentDate.setDate(25);

currentDate.setHours(18);

currentDate.setMinutes(30);

currentDate.setSeconds(45);

currentDate.setMilliseconds(500);
```

显示更新后的日期：

```javascript
console.log("Updated Date: " + currentDate);
```

这些示例演示了如何使用各种`set`方法来更新`Date`对象的特定部分，例如年、月、日、小时、分、秒和毫秒。

## JS Math

在 JavaScript 中，`Math`对象提供了一系列内置数学方法，用于执行常见的数学运算。这些方法是 JavaScript 语言的核心部分，不需要额外的库即可使用。

### 常量

`Math`对象包含了几个数学常数，例如`Math.PI`（圆周与直径的比率，约 3.14159）和`Math.E`（欧拉数，约 2.71828）。

### 基础算术运算

- `Math.abs(x)`：返回数字`x`的绝对值。
- `Math.ceil(x)`：将数字向上取整到最近的整数。
- `Math.floor(x)`：将数字向下取整到最近的整数。
- `Math.round(x)`：将数字四舍五入到最近的整数。
- `Math.max(x, y, ...)`：返回零或多个数字中的最大值。
- `Math.min(x, y, ...)`：返回零或多个数字中的最小值。

### 指数和对数函数

`Math`提供了指数和对数函数的方法，包括：

- `Math.pow(x, y)`：返回`x`的`y`次幂。
- `Math.sqrt(x)`：返回`x`的平方根。
- `Math.exp(x)`：返回`e`的`x`次幂。
- `Math.log(x)`：返回`x`的自然对数（以`e`为底）。
- `Math.log10(x)`：返回`x`的以 10 为底的对数。

### 三角函数

`Math`提供了三角函数的方法，包括：

- `Math.sin(x)`：返回角度`x`（弧度）的正弦值。
- `Math.cos(x)`：返回角度`x`（弧度）的余弦值。
- `Math.tan(x)`：返回角度`x`（弧度）的正切值。
- `Math.asin(x)`：返回`x`的反正弦（逆正弦）。
- `Math.acos(x)`：返回`x`的反正余弦（逆余弦）。
- `Math.atan(x)`：返回`x`的反正切（逆正切）。
- `Math.atan2(y, x)`：返回其参数商的反正切。

### 随机数生成

`Math`提供了生成随机数的方法，包括：

- `Math.random()`：返回 0（包含）和 1（不包含）之间的伪随机数。

### 四舍五入与精度

`Math`提供了用于舍入和处理精度的方法：

- `Math.round()`、`Math.floor()`和`Math.ceil()`常用于将数字舍入为整数。可以使用乘以和除以 10 的幂等技术来控制精度。

### 角度单位转换

`Math`包含了在角度和弧度之间转换的方法：

- `Math.degrees(x)`：将弧度转换为角度。
- `Math.radians(x)`：将角度转换为弧度。

`Math`对象是一个用于在 JavaScript 中执行数学运算的多功能工具。它提供了一组在科学和工程计算中常用的函数，以及基础算术和舍入操作。理解`Math`对象的能力对于在 JavaScript 应用程序中处理数字至关重要。

```javascript
// JavaScript Math 对象示例

// Math 常量

let piValue = Math.PI;

let eulerNumber = Math.E;

// Math 方法

let absoluteValue = Math.abs(-5);

let squareRoot = Math.sqrt(25);

let power = Math.pow(2, 3);

let roundedNumber = Math.round(3.7);

let ceilValue = Math.ceil(4.2);

let floorValue = Math.floor(4.8);

let randomValue = Math.random(); // 生成一个 0 到 1 之间的随机小数

// 显示 Math 常量和结果

console.log("Pi Value: " + piValue);

console.log("Euler's Number: " + eulerNumber);

// 显示 Math 方法的值

console.log("Absolute Value: " + absoluteValue);

console.log("Square Root of 25: " + squareRoot);

console.log("2 to the power of 3: " + power);

console.log("Rounded Number: " + roundedNumber);

console.log("Ceil Value of 4.2: " + ceilValue);

console.log("Floor Value of 4.8: " + floorValue);

console.log("Random Decimal: " + randomValue);

// JavaScript Math 对象示例结束
```

## JS Random

在 JavaScript 中，`Math.random()`方法用于生成 0（包含）和 1（不包含）之间的伪随机浮点数。

### 伪随机数

`Math.random()`生成的数字被认为是伪随机的，因为它们由算法决定，而非真正的随机。

### 范围

`Math.random()`返回的值落在`[0, 1)`范围内，这意味着包含 0 但不包含 1。

### 均匀分布

`Math.random()`的值分布是均匀的，这意味着范围内的每个可能值都有相同的概率。

### 缩放与平移

可以通过缩放和平移来调整随机数的范围和起始点。例如，要生成范围内的随机整数，可以使用`Math.floor(Math.random() * (max - min + 1)) + min`。

### 种子

JavaScript 的`Math.random()`不支持种子（为随机生成器提供初始值）。如果需要对随机性进行更多控制，可以使用外部库或自定义算法。

### 应用程序用法

`Math.random()`常用于需要随机性的应用程序，例如游戏、模拟或任何需要不可预测值的场景。

### 确定性行为

虽然值是伪随机的，但`Math.random()`生成的序列是确定性的，如果使用相同的种子就可以复现。然而，JavaScript 没有提供为随机数生成器设置种子的内置机制。

### 加密用途

`Math.random()`不适用于对真随机和不可预测性至关重要的加密目的。对于加密应用，建议使用`crypto` API 或外部库。

### 背后的数学原理

`Math.random()`使用的具体算法取决于实现，并未由 ECMAScript 标准规定。不同的 JavaScript 引擎可能使用不同的算法。

```javascript
// JavaScript 随机数示例

// Generate a Random Number between 1 and 10

let randomNumber = Math.floor(Math.random() * 10) + 1;

// Display Random Number

console.log("Random Number between 1 and 10: " + randomNumber);

// End of JavaScript Random Number Example
```

在这个示例中，在特定范围内生成了一个 JavaScript 随机数：

1. 生成 1 到 10 之间的随机数：`let randomNumber = Math.floor(Math.random() * 10) + 1;`
2. 显示随机数：`console.log("Random Number between 1 and 10: " + randomNumber);`

这个示例演示了如何使用`Math.random()`方法生成一个 0（包含）到 1（不包含）之间的随机小数，然后对结果进行缩放和偏移，以获得特定范围内的随机整数。

## JS 布尔

在 JavaScript 中，布尔是一种表示两种可能值之一的数据类型：`true`（真）或`false`（假）。布尔在编程中经常用于决策、控制程序流以及评估条件。

### 两个可能的值

布尔数据类型只有两个可能的值：`true`和`false`。这些值代表真或假、开或关、是或否的二进制逻辑。

### 逻辑操作

布尔值是逻辑操作的基础。条件、比较和布尔运算符（如`&&`、`||`和`!`）都会返回布尔值。

### 条件语句

布尔值常用于条件语句，例如`if`、`else if`和`else`块。这些块中的代码根据条件求值结果为真还是为假来决定是否执行。

### 比较运算符

比较运算符（如`==`、`!=`、`<`、`<=`和`>=`）比较值并返回布尔结果。它们通常用于根据值之间的关系来做出决策。

### 逻辑运算符

逻辑运算符（`&&`、`||`、`!`）用于组合或取反布尔值。它们对于创建复杂条件和控制程序流至关重要。

### 布尔函数

函数可以根据某些条件返回布尔值。例如，函数可以检查一个数字是否为偶数并相应返回`true`或`false`。

### 真值与假值（Truthy and Falsy Values）

在 JavaScript 中，值在布尔上下文中被分为“真值”（truthy）或“假值”（falsy）。所有值都被视为真的，但少数特殊情况除外，如`0`、`""`（空字符串）、`null`、`undefined`和`NaN`，它们是假的。

### 布尔对象

虽然布尔数据类型只有两个原始值（`true`和`false`），但 JavaScript 中还有一个`Boolean`对象包装器，用于创建布尔对象。然而，在实践中很少使用。

### 默认布尔值

在某些情况下，变量可能会被隐式转换为布尔值。例如，在语句中，条件会被隐式转换为布尔值，非布尔值被视为真值或假值。

理解布尔值对于在 JavaScript 中编写高效且逻辑清晰的代码是基础。布尔是决策和控制流的核心，在创建条件和根据不同场景确定程序行为方面起着至关重要的作用。

```javascript
// JavaScript Booleans Example

// Boolean Declaration

let isTrue = true;
let isFalse = false;

// Boolean Operations

let resultAnd = true && false;

let resultOr = true || false;

let resultNot = !true;

// Display Boolean Values and Results

console.log("True Boolean: " + isTrue);

console.log("False Boolean: " + isFalse);

console.log("Result of AND Operation: " + resultAnd);

console.log("Result of OR Operation: " + resultOr);

console.log("Result of NOT Operation: " + resultNot);

// End of JavaScript Booleans Example
```

在这个示例中，演示了 JavaScript 布尔值：

### 布尔声明

`let isTrue = true; let isFalse = false;`

### 布尔操作

逻辑与（`&&`）、逻辑或（`||`）、逻辑非（`!`）。

### 显示布尔值和结果

```javascript
console.log("True Boolean: " + isTrue);
console.log("False Boolean: " + isFalse);
console.log("Result of AND Operation: " + resultAnd);
console.log("Result of OR Operation: " + resultOr);
console.log("Result of NOT Operation: " + resultNot);
```

## JS 比较

在 JavaScript 中，比较是编写高效且逻辑清晰代码的基础。比较用于确定不同值之间的关系。

### 相等运算符

比较运算符（如`==`、`!=`、`<`、`<=`和`>=`）比较值并返回布尔结果。它们通常用于根据值之间的关系来做出决策。`==`（浅相等）检查值是否相等。

### 不等于运算符

比较运算符（如`==`、`!=`、`<`、`<=`和`>=`）比较值并返回布尔结果。它们通常用于根据值之间的关系来做出决策。

### 关系运算符

比较运算符（如`==`、`!=`、`<`、`<=`和`>=`）比较值并返回布尔结果。它们通常用于根据值之间的关系来做出决策。

### 真值与假值

值在布尔上下文中被分类为“真值”（truthy）或“假值”（falsy）。

### NaN

`NaN`（非数字）是一个特殊值，表示无效操作的结果。

### 对象比较

对象是按引用进行比较的，而不是按值。

```javascript
// script.js

let isEqualNumeric = 5 == "5"; // true (loose equality)

let isStrictEqualNumeric = 5 === "5"; // false (strict equality)

let isNotEqualNumeric = 10 != "10"; // false (loose inequality)

let isNotStrictEqualNumeric = 10 !== "10"; // true (strict inequality)

let isLess = 3 < 7; // true

let isGreaterEqual = 5.5 >= 5; // true

let isEqual = 4 <= 3; // false

// String Comparisons

let isEqualString = "world" == "world"; // true

let isEqualString2 = "apple" == "orange"; // false

let isLexicographicallyGreater = "apple" > "banana"; // false

let isLexicographicallyLess = "orange" < "pear"; // true

// Boolean Comparisons

let isEqualBoolean = true == false; // false

let isNotEqualBoolean = true !== false; // true

// Numeric Comparisons

console.log("Numeric Comparisons:");

console.log("Equal (Loose):", isEqualNumeric);

console.log("Equal (Strict):", isStrictEqualNumeric);

console.log("Not Equal (Loose):", isNotEqualNumeric);

console.log("Not Equal (Strict):", isNotStrictEqualNumeric);

console.log("Greater:", isLess);

console.log("Greater or Equal:", isGreaterEqual);

// String Comparisons

console.log("String Comparisons:");

console.log("Equal (Loose):", isEqualString);

console.log("Not Equal (Loose):", !isEqualString);

console.log("Lexicographically Greater:", isLexicographicallyGreater);

console.log("Lexicographically Less:", isLexicographicallyLess);

// Boolean Comparisons

console.log("Boolean Comparisons:");

console.log("Equal:", isEqualBoolean);

console.log("Not Equal:", !isNotEqualBoolean);

// End of JavaScript Comparisons Example
```

在这个示例中，演示了各种 JavaScript 比较运算符：

### 数字比较

等于（`==`）、不等于（`!=`、`!==`）、大于（`>`）、小于（`<`）、大于等于（`>=`）、小于等于（`<=`）。

### 字符串比较

等于（`==`）、不等于（`!=`）、字典序大于（`>`）、小于（`<`）。

### 布尔值比较

等于（`==`）、不等于（`!=`）。

### 显示比较结果

数字、字符串和布尔比较的结果通过`console.log`显示。

此示例说明了如何在 JavaScript 中使用各种比较运算符来处理数字、字符串和布尔值。

## JS If Else

在 JavaScript 中，`if`语句和`else`语句是控制流结构，允许你根据指定的条件执行不同的代码块。

### if 语句

`if`语句用于根据指定的条件有条件地执行代码块。如果条件为真，则执行`if`块中的代码。如果条件为假，则跳过`if`块中的代码。

### else 语句

`else`语句与`if`语句配合使用，在`if`条件为假时提供一个备选执行的代码块。如果`if`条件为真，则跳过`else`块中的代码。如果`if`条件为假，则执行`else`块中的代码。

### 互斥执行

执行`if`块内的代码或`else`块内的代码，但不同时都执行。这根据条件的真或假值提供了一个互斥的选择。

### else if 语句（可选）

为了处理多个条件，你可以使用`else if`语句。当之前的`if`或`else if`条件为假时，它允许你检查额外的条件。将执行第一个匹配的条件块中的代码。

### 嵌套 if 语句

你可以将`if`语句嵌套在一起以处理更复杂的条件。只有当外部`if`语句的条件为真时，才会评估内部的`if`语句。

### 评估顺序

条件从上到下进行评估。一旦某个条件为真，就会执行相应的代码块，后续条件将不再被评估。

### 真值和假值

`if`语句内部的条件根据其是真值（truthy）还是假值（falsy）进行评估。真值评估结果为真，假值评估结果为假。

### 三元运算符（替代）

在某些情况下，`if`和`else`语句可以用三元运算符（`?:`）替换。它提供了一种更简洁的方式表达条件语句。

理解如何使用`if`和`else`语句对于在 JavaScript 代码中创建决策结构至关重要。这些语句允许你根据条件控制程序的流，让你能够创建动态且响应的应用程序。

```javascript
// JavaScript If-Else 示例

// 数字比较

let num1 = 10;

let num2 = 5;

// If-Else 语句

if (num1 > num2) {

  console.log(num1 + " is greater than " + num2);

} else {

  console.log(num1 + " is not greater than " + num2);

}

// 字符串比较

let string1 = "apple";

let string2 = "orange";

// 字符串的 If-Else 语句

if (string1 === string2) {

  console.log(string1 + " is equal to " + string2);

} else {

  console.log(string1 + " is not equal to " + string2);

}

// 布尔值比较

let booleanValue = true;

// 布尔值的 If-Else 语句

if (booleanValue) {

  console.log("The value is true.");

} else {

  console.log("The value is false.");

}

// JavaScript 比较示例结束
```

此示例演示了各种比较运算符：

1. 数字比较：等于（`==`）、不等于（`!=`、`!==`）、大于（`>`）、小于（`<`）、大于等于（`>=`）、小于等于（`<=`）。
2. 字符串比较：等于（`==`）、不等于（`!=`）、字典序大于（`>`）、小于（`<`）。
3. 布尔值比较：等于（`==`）、不等于（`!=`）。
4. 显示比较结果：数字、字符串和布尔比较的结果使用`console.log`显示。

## JS Switch

在 JavaScript 中，`switch`语句是一种控制流语句，允许根据表达式执行不同的代码块。

### 表达式评估

`switch`语句以括号内的表达式（通常是变量）开始。然后对该表达式进行评估。

### case 块

紧随`switch`语句之后有一个或多个`case`块。每个`case`包含一个与评估表达式比较的值。

### 匹配情况

当评估表达式匹配某个`case`块的值时，将执行该块内部的代码。如果没有匹配，程序将移动到下一个`case`。

### break 语句

在执行`case`块的代码后，使用`break`语句退出`switch`语句。这防止了程序穿透到下一个`case`块。

### default 情况（可选）

`default`情况是可选的，用于指定当没有任何`case`块匹配时执行的代码。它类似于`if-else`结构中的`else`语句。

### 穿透行为

与某些其他语言不同，JavaScript 的`switch`语句具有穿透行为。如果`case`块不包含`break`语句，无论条件是否满足，执行都会穿透到下一个`case`块。

### 相等比较

`switch`语句中的比较是严格的（使用`===`）。这意味着只有当值和类型都匹配时，才会执行`case`块。

### 多重情况

你可以通过逗号分隔将多个值组合在单个`case`块中。如果任何值匹配评估表达式，将执行该`case`块中的代码。

`switch`语句在需要针对单个变量或表达式检查多个条件时特别有用。在代码执行取决于单个变量值的情况下，它提供了一个比多个`else if`语句更清晰的替代方案。

```javascript
// JavaScript Switch 语句示例

// 星期

let day = "Monday";

let dayType;

// Switch 语句

switch (day) {

  case "Monday":

  case "Tuesday":

  case "Wednesday":

    dayType = "Weekday";

    break;

  default:

    dayType = "Unknown";

}

console.log(dayType);
```

```javascript
switch (day) {

  case "Thursday":

  case "Friday": dayType = "Weekday"; break;

  case "Saturday":

  case "Sunday": dayType = "Weekend"; break;

  default: dayType = "Invalid Day";

}

// Display Result

console.log("Day: " + day);

console.log("Day Type: " + dayType);

// End of JavaScript Switch Statement Example
```

在这个示例中，演示了 JavaScript `switch`语句：

1. 星期几：变量`day`代表星期中的某天（例如`"Monday"`）。
2. Switch 语句：`switch`语句检查`day`的值，并根据其是工作日、周末还是无效日期来分配相应的`dayType`。
3. 显示结果：使用`console.log`显示结果，包括天数及其对应的类型。

此示例展示了如何使用`switch`语句根据变量的值来处理多种情况。

## JS For 循环

在 JavaScript 中，`for`循环是一种控制流语句，允许你按照指定的次数重复执行一段代码块。

### 初始化

`for`循环以一个初始化语句开始。该语句通常用于声明和初始化循环控制变量，该变量通常是一个计数器。

### 条件

在初始化语句之后是一个条件。只要条件求值结果为`true`，循环就会继续执行。如果条件变为`false`，循环将终止，程序将移动到循环后的下一个语句。

### 迭代表达式

紧随条件之后是一个迭代表达式。该表达式在循环每次迭代后都会求值，通常用于更新循环控制变量。它允许你控制循环的进度。

### 代码块

在`for`循环内部，有一个用大括号`{}`包围的代码块。该代码块包含了循环每次迭代时执行的语句。

### 循环控制变量

循环控制变量通常用于跟踪当前迭代。它在迭代表达式中被修改，以控制循环何时终止。

### 作用域

循环控制变量的作用域限于`for`循环，这意味着它在循环块内可访问。这有助于防止循环外意外的迭代影响。

### 初始化一次

初始化语句仅在循环开始时执行一次。它在循环开始之前初始化循环控制变量。

### 每次迭代前检查条件

在每次迭代之前，都会检查条件。如果条件为`true`，则执行循环块内的代码。如果为`false`，则循环终止，程序移动到循环后的下一个语句。

### 每次迭代后执行迭代表达式

在每次迭代后，都会执行迭代表达式。这一步允许你修改循环控制变量，可能会影响后续迭代的循环行为。

`for`循环是 JavaScript 中实现迭代的一种多功能且广泛使用的结构。它为执行重复性任务提供了一种简洁且组织良好的方式，特别是当迭代次数已知或可以根据条件确定时。

```javascript
// JavaScript For 循环示例

// 从 1 迭代到 5

console.log("Counting from 1 to 5.");

for (let i = 1; i <= 5; i++) {

  console.log(i);

}

// 遍历数组

let fruits = ["Apple", "Banana", "Orange", "Mango"];

console.log("Fruits:");

for (let j = 0; j < fruits.length; j++) {

  console.log(fruits[j]);

}

// JavaScript For 循环示例结束
```

在这个示例中，演示了 JavaScript `for`循环：

1. 从 1 迭代到 5：一个使用循环变量`i`从 1 计数到 5 的简单循环。
2. 遍历数组：循环遍历数组（`fruits`）并打印每个元素。
3. 显示结果：两个循环的结果都使用`console.log`显示。

此示例说明了如何使用`for`循环来遍历一个范围的值以及数组的元素。

## JS For In 循环

在 JavaScript 中，`for...in`循环是一种专门用于遍历对象可枚举属性的特殊循环。

### 遍历属性

`for...in`循环的主要用途是遍历对象的可枚举属性。它对于键（key）为字符串的对象特别有用。

### 对象枚举

`for...in`循环遍历对象自身及其继承的可枚举属性。它不包括不可枚举的属性或定义在对象原型链上的属性。

### 语法

`for...in`循环的语法为`for (variable in object) { ... }`，其中`variable`是在每次迭代中将被赋值属性键的变量，`object`是正在被迭代的对象。

### 变量赋值

在每次迭代中，`for...in`循环将当前属性的键分配给指定的变量。然后你可以使用该变量来访问相应的属性值。

### 遍历对象属性

`for...in`循环通常与对象配合使用以遍历它们的属性。但重要的是，迭代的顺序是不保证的，它在不同的 JavaScript 引擎之间可能会不同。

### 枚举顺序

枚举顺序基于属性被添加到对象的顺序，但这并不是保证的，且在不同的 JavaScript 引擎之间可能会有所不同。

### 属性标记

`for...in`循环只遍历`enumerable`属性设置为`true`的属性。使用某些方法创建的属性（例如设置`enumerable: false`的`Object.defineProperty()`）将不会被包含。

### 数组和类数组

虽然`for...in`可以用于数组，但通常不建议这样做，因为它遍历的是键（即数组索引）而不是值。对于数组，通常推荐使用`for...of`。

### 避免在迭代期间修改对象

在`for...in`循环内部修改正在迭代的对象可能会导致意外行为。通常情况下，建议在迭代期间避免修改对象的结构。

`for...in`循环适用于需要检查或操作对象属性的场景。然而，对于遍历数组或类数组中的值，`for...of`循环因其更直观的语法和行为而更受青睐。

```javascript
// JavaScript For In 循环示例

// 键值对对象

let person = {

  name: "John",

  age: 30,

  city: "New York"

};

// 使用 for...in 遍历对象属性

console.log("Person Details:");

for (let key in person) {

  console.log(key + ": " + person[key]);

}

// 颜色数组

let colors = ["Red", "Green", "Blue"];

// 使用 for...in 遍历数组索引

console.log("Array Indices:");

for (let index in colors) {

  console.log(index + ": " + colors[index]);

}

// JavaScript For In 循环示例结束
```

## JS for...of 循环

在 JavaScript 中，`for...of`循环是 ECMAScript 2015 (ES6) 引入的一种现代迭代语句。它提供了一种简洁且高效的方式来遍历可迭代对象的值，例如数组、字符串、Map、Set 等。

### 可迭代对象

`for...of`循环专门为遍历可迭代对象设计。可迭代对象是实现了迭代协议的对象，允许它们使用`for...of`循环进行遍历。

### 语法

`for...of`循环的语法为`for (variable of iterable) { ... }`，其中`variable`是一个变量，在每次迭代中将被赋值为可迭代对象中每个元素的值，而`iterable`则是被迭代的对象。

### 数组迭代

`for...of`最常见的用例之一是遍历数组的元素。该循环会自动获取值，与使用数组索引的传统`for`循环相比，它简化了代码。

### 字符串迭代

字符串在 JavaScript 中也是可迭代对象，可以使用`for...of`循环来遍历字符串的字符。

### 可迭代对象

除了数组和字符串，其他可迭代对象如 Map、Set 和某些内置对象也可以使用`for...of`进行迭代。自定义对象也可以通过实现迭代协议变为可迭代。

### 无需索引

与传统的`for`循环不同，`for...of`循环消除了对索引变量的需求。它直接提供迭代对象的值，使代码更加易读且简洁。

### 不遍历对象属性

`for...of`循环专门设计用于遍历可迭代的值，不会遍历对象的属性。要遍历对象的属性，`for...in`循环更为合适。

### Break 和 Continue

`for...of`循环支持`break`和`continue`语句，允许像传统`for`循环一样控制循环流。

### 生成器函数 (Generator Functions)

`for...of`与生成器函数无缝工作，允许迭代由生成器产生的值。

### 支持自定义迭代器

对象可以通过迭代协议实现自定义迭代器，这涉及定义一个`Symbol.iterator`方法。这使得自定义对象可以用于`for...of`循环。

`for...of`循环是一个用于遍历可迭代对象值的强大且方便的工具。它增强了代码的可读性，并且在现代 JavaScript 开发中处理数组和其他可迭代数据结构时特别有益。

```javascript
// JavaScript For...Of Loop Example

// Array of Fruits

let fruits = ["Apple", "Banana", "Orange", "Mango"];

// For...Of Loop to Iterate Over Array

console.log("Fruits:");

for (let fruit of fruits) {

    console.log(fruit);

}

// String

let message = "Hello";

// For...Of Loop to Iterate Over String

console.log("\nCharacters in the String:");

for (let char of message) {

  console.log(char);

}

// Map

let population = new Map([

  ["New York", 8400000],

  ["Los Angeles", 3990000],

  ["Chicago", 2716000]

]);

// For...Of Loop to Iterate Over Map

console.log("\nPopulation:");

for (let [city, pop] of population) {

  console.log(city + ": " + pop);

}

// End of JavaScript For...Of Loop Example
```

```text
Console:

Fruits:

Apple

Banana

Orange

Mango

Characters in the String:

H

e

l

l

o

Population:

New York: 8400000

Los Angeles: 3990000

Chicago: 2716000
```

在这个示例中，演示了 JavaScript `for...of`循环：

1. 水果数组：`fruits`数组包含了水果名称。
2. 遍历数组元素的`for...of`循环：`for...of`循环遍历`fruits`数组的元素并打印每个水果。
3. 字符串：变量`message`是一个字符串。
4. 遍历字符串字符的`for...of`循环：`for...of`循环遍历字符串的字符并打印每个字符。
5. Map：`population` Map 包含了城市与人口的键值对。
6. 遍历 Map 条目的`for...of`循环：`for...of`循环遍历 Map 的条目。
7. 显示结果：显示了`for...of`循环的结果。

## JS While 循环

```javascript
// script.js

// JavaScript 循环示例

// 使用 While 循环计数 1 到 5

let count = 0;

console.log("Counting from 1 to 5 with a While Loop:");

while (count < 5) {

    console.log(count);

    count++;

}

// 使用 While 循环计算到 10 的数字和

let sum = 0;

let number = 1;

console.log("Sum of Numbers up to 10 with a While Loop:");

while (number <= 10) {

    sum += number;

    number++;

}

console.log("Sum: " + sum);

// JavaScript 循环示例结束
```

在这个示例中，演示了 JavaScript `while`循环：

1. 使用 While 循环计数从 1 到 5：一个简单的`while`循环，使用循环变量`count`从 1 计数到 5。
2. 使用 While 循环计算到 10 的数字和：另一个`while`循环，计算 1 到 10 的数字和。
3. 显示结果：使用`console.log`显示两个`while`循环的结果。

## JS Break

在 JavaScript 中，`break`语句是一种控制流语句，用于提前终止循环的执行。

### 循环终止

`break`语句的主要目的是提前退出循环。当在循环体内遇到`break`语句时，它会立即终止循环，并将控制转移到循环后的后续语句。

### 在循环中使用

`break`语句通常与循环配合使用，如`for`、`while`和`do...while`。它允许你根据特定条件退出循环，即使循环的正常退出条件尚未满足。

### Switch 语句

除了循环外，`break`语句还用于`switch`语句。当在`switch`的`case`中遇到`break`语句时，它会退出`switch`块，防止执行后续的`case`。

### 嵌套循环

在嵌套循环中，`break`语句通常用于在满足特定条件时退出内层循环。这允许你控制嵌套循环结构中的执行流。

### 标记循环

在 JavaScript 中，你可以使用标签标识符对循环进行标记。此时`break`语句可以配合标签使用，以在存在嵌套循环时指定应终止哪一个循环。

### 跳过循环

在某些情况下，`break`语句不仅用于退出循环，还用于跳过循环的剩余迭代。当满足特定条件且没有必要继续后续迭代时，这尤为有用。

### 避免死循环

在某些情况下，`break`语句被用作一种安全机制来避免死循环。通过引入条件检查，可以在满足特定条件时退出循环，防止程序无限运行。

### 条件终止

使用`break`语句的决定通常基于某个条件，当该条件为真时，表明进一步的迭代是不必要的或不可取的。该条件可能由外部因素、用户输入或循环内部特定计算决定。

### 多功能性

`break`语句为控制程序流提供了灵活性。它允许灵活地终止循环，是管理程序执行路径的关键工具。

确保保持预期的逻辑且程序行为是可预测的是非常重要的。误用`break`语句（特别是在嵌套循环中）可能会导致意料之外的结果和 Bug。

```javascript
// JavaScript Break 语句示例

// 带有 Break 语句的 While 循环

let count = 1;

console.log("Counting with a While Loop and Break Statement");

while (true) {

  console.log(count);

  count++;

  if (count > 5) {

    break;

  }

}

// 带有 Break 语句的 For 循环

console.log("Counting with a For Loop and Break Statement");

for (let i = 1; i <= 10; i++) {

  console.log(i);

  if (i === 5) {

    break;

  }

}

// JavaScript Break 语句示例结束
```

在这个示例中，在`while`和`for`循环中演示了 JavaScript `break`语句：

1. 带有 Break 语句的 While 循环：使用循环变量`count`计数的`while`循环，当`count`大于 5 时跳出循环。
2. 带有 Break 语句的 For 循环：使用循环变量`i`计数的`for`循环，当`i`等于 5 时跳出循环。
3. 显示结果：显示带有`break`语句的两个循环的结果。

## JS 可迭代对象

在 JavaScript 中，可迭代对象（iterable）是一个实现了可迭代协议的对象，允许使用`for...of`循环进行迭代。

### 可迭代协议

可迭代协议是对象为了被迭代而必须遵循的规则。可迭代对象必须具有`Symbol.iterator`方法。

### Symbol.iterator

`Symbol.iterator`是一个符号，作为对象的键。当调用此方法时，它返回一个迭代器对象。

### 迭代器对象

迭代器对象具有`next`方法。`next`方法返回一个包含两个属性的对象：`value`（迭代的值）和`done`（表示迭代是否完成）。

### for...of 循环

`for...of`循环是 JavaScript 中专门用于遍历可迭代对象的语法。它抽象了与迭代器工作的细节。

### 可迭代对象的示例

JavaScript 中常见的可迭代对象包括数组、字符串、Map、Set 以及某些内置对象如`NodeList`和`arguments`。

### 数组

数组可能是最常用的可迭代对象。它们持有有序的值集合，`for...of`允许你遍历数组中的每个元素。

### 字符串

字符串在 JavaScript 中也是可迭代的。当你使用`for...of`遍历字符串时，逐个获取字符串中的字符。

### Map 和 Set

Map 和 Set 是 ECMAScript 2015 (ES6) 引入的可迭代数据结构。它们允许你存储键值对（Map）或唯一值（Set）。

### 自定义可迭代对象

开发者可以通过实现可迭代协议创建自定义的可迭代对象。这涉及定义`Symbol.iterator`方法并返回一个具有`next`方法的迭代器对象。

### 迭代一次

可迭代对象通常设计为迭代一次。一旦迭代器到达序列末尾，后续调用`next`将返回`done`为`true`的对象。

### 迭代耗尽

可迭代对象和迭代器维护内部状态以跟踪序列中的当前位置。到达末尾后，尝试再次迭代将不会产生额外值。



# JavaScript 可迭代对象和 `for...of` 循环示例

## 数组

```javascript
let fruits = ["Apple", "Banana", "Orange"];

// 使用 for...of 循环遍历数组
console.log("Fruits:");
for (let fruit of fruits) {
    console.log(fruit);
}
```

## 字符串

```javascript
let message = "Hello";

// 使用 for...of 循环遍历字符串
console.log("\nCharacters in the String:");
for (let char of message) {
    console.log(char);
}
```

## Map

```javascript
// Map 定义人口统计数据
new Map([
  ["New York", 8400000],
  ["Los Angeles", 3990000],
  ["Chicago", 2716000]
]);
```

```javascript
// 使用 for...of 循环遍历 Map 条目
console.log("Population:");
for (let [city, pop] of population) {
  console.log(city + " : " + pop);
}
```

## Set

```javascript
let uniqueNumbers = new Set([1, 2, 3, 4, 5]);
```

```javascript
// 使用 for...of 循环遍历 Set 元素
console.log("Unique Numbers:");
for (let number of uniqueNumbers) {
  console.log(number);
}
```

```javascript
// JavaScript 可迭代对象与 for...of 循环示例结束
```

```javascript
script.js
2 // Array
3 let fruits = ["Apple", "Banana", "Orange"];
4 // 使用 for...of 循环遍历数组元素
5 console.forEach(function() {
6 for (let fruit of fruits) {
7 console.log(fruit);
8 }
9 })
10 // String
11 let message = "Hello";
12
13 // 使用 for...of 循环遍历字符串
14 console.log("Characters in the String:");
15 for (let char of message) {
16 console.log(char);
17 }
18 // Map
19 let population = new Map([
20 ["New York", 8400000],
21 ["Los Angeles", 3990000],
22 ["Chicago", 2716000]
23]);
24 // 使用 for...of 循环遍历 Map 条目
25 console.log("Population:");
26 for (let [city, pop] of population) {
27 console.log(city + " : " + pop);
28 }
29 // Set
30 let uniqueNumbers = new Set([1, 2, 3, 4, 5]);
31 // 使用 for...of 循环遍历 Set 元素
32 console.log("Unique Numbers:");
33 for (let number of uniqueNumbers) {
34 console.log(number);
35 }
36 // JavaScript 可迭代对象与 for...of 循环示例结束
```

在此示例中，通过 `for...of` 循环演示了 JavaScript 的可迭代的使用：

1. 数组：`fruits` 数组包含水果名称。
2. 使用 `for...of` 循环遍历数组元素：`for...of` 循环遍历 `fruits` 数组的元素并打印每个水果。
3. 字符串：变量 `message` 是一个字符串。
4. 使用 `for...of` 循环遍历字符串字符：`for...of` 循环遍历字符串的字符并打印每个字符。
5. Map：`population` Map 包含城市与人口的键对。
6. 使用 `for...of` 循环遍历 Map 条目：`for...of` 循环遍历 map 的条目并打印每个城市-人口对。
7. Set：`uniqueNumbers` Set 包含唯一的数字。
8. 使用 `for...of` 循环遍历 Set 元素：`for...of` 循环遍历 set 的元素并打印每个唯一的数字。
9. 显示结果：使用 `console.log` 显示每个 `for...of` 循环的结果。此示例说明了如何使用 `for...of` 循环遍历数组中的元素、字符串中的字符、Map 以及 Set 中的元素。

# JS Set

在 JavaScript 中，`Set` 是一种内置对象，表示一个无序的唯一值集合。

1. 唯一性：`Set` 只能包含唯一的值。这意味着任何给定的值在 `Set` 中只能出现一次。如果你尝试添加重复的值，它将被忽略。
2. 无重复值：值的唯一性是使用 `SameValueZero` 算法来决定的，该算法将所有值（包括 `NaN` 和 `undefined`）都视为不同的值。
3. 无键值对：与对象或 map 不同，`Set` 不存储键值对。它只存储单个值。值本身就是键，并被用于检查唯一性。
4. 无索引：`Set` 元素没有索引。它们不是存储在任何特定顺序中的，也没有通过索引访问元素的直接方法。不过，你可以使用 `for...of` 循环迭代元素。
5. 可迭代性：`Set` 是可迭代的，这意味着你可以使用 `for...of` 循环、`values` 方法或展开运算符 (`...`) 来迭代存储在 `Set` 中的值。
6. 无大小限制：`Set` 可以动态增长，没有预定义的大小限制。它们可以包含任意数量的唯一值。
7. 添加和删除元素的方法：`Set` 提供了诸如 `add` 用于添加新元素，`delete` 用于删除元素，以及 `clear` 用于移除所有元素的方法。
8. 检查是否存在：`has` 方法允许你检查特定值是否存在于 `Set` 中。
9. 使用场景：当你需要存储一个唯一值的集合而不需要关联键，或者元素的顺序不重要时，`Set` 是很有用的。
10. 与数组的比较：虽然数组是有序的可以包含重复值，但 set 是无序的且只能包含唯一的值。在它们之间的选择取决于你的数据需求。
11. 从数组转换：你可以从数组创建一个 `Set`。构造函数会自动移除数组中的重复值。
12. 常用方法：除了前面提到的方法，set 还有如 `size` 属性来获取元素数量，以及 `values` 方法（或 `keys` 方法）来获取值的迭代器。`Set` 是 JavaScript 中一种多功能的结构，特别是在处理唯一值集合时。它们提供了高效的检查是否存在、添加和删除元素的方法。

```javascript
// JavaScript Set 示例

// 创建一个 Set
let uniqueNumbers = new Set([1, 2, 3, 4, 5]);

// 向 Set 添加元素
uniqueNumbers.add(6);
uniqueNumbers.add(7);

// 检查 Set 大小
console.log("Set Size: " + uniqueNumbers.size);

// 检查元素是否存在于 Set
console.log("Does the Set contain 3? " + uniqueNumbers.has(3));

// 从 Set 中删除元素
uniqueNumbers.delete(2);
```

```javascript
// 迭代 Set 元素
console.log("Set Elements:");
for (let number of uniqueNumbers) {
  console.log(number);
}
```

```javascript
// 清空 Set
uniqueNumbers.clear();
```

```javascript
// 清空后的大小
console.log("Set Size After Clearing: " + uniqueNumbers.size);
```

```javascript
// Set 示例结束
```

在此示例中，通过 `for...of` 循环演示了 JavaScript 可迭代对象：

1. 数组：`fruits` 数组包含水果名称。
2. 使用 `for...of` 循环遍历数组元素：`for...of` 循环遍历 `fruits` 数组的元素并打印每个水果。
3. 字符串：变量 `message` 是一个字符串。
4. 使用 `for...of` 循环遍历字符串字符：`for...of` 循环遍历字符串的字符并打印每个字符。
5. Map：`population` Map 包含城市-人口的键对。
6. 使用 `for...of` 循环遍历 Map 条目：`for...of` 循环遍历 map 的条目并打印每个城市-人口对。
7. Set：`uniqueNumbers` Set 包含唯一的数字。
8. 使用 `for...of` 循环遍历 Set 元素：`for...of` 循环遍历 set 的元素并打印每个唯一的数字。
9. 显示结果：使用 `console.log` 显示每个 `for...of` 循环的结果。此示例说明了如何使用 `for...of` 循环遍历数组中的元素、字符串中的字符、Map 以及 Set 中的元素。

# JS Maps

在 JavaScript 中，`Map` 是一种内置对象，允许你存储键值对，其中键和值可以是任何数据类型。

1. 键值对：`Map` 是一个键值对的集合，每个键都是唯一的。这意味着可以使用任何数据类型（包括对象和原始值）作为键和值。
2. 无序：与对象不同，`Map` 中键值对的顺序由它们被添加的顺序保证。遍历 `Map` 中的条目将遵循插入顺序。
3. 任意类型的键：与对象的键会自动转换为字符串不同，`Map` 的键可以是任何数据类型，包括对象和原始值。这允许了更灵活的数据结构。
4. 迭代条目：`Map` 提供了 `entries`、`keys` 和 `values` 方法分别用于迭代键值对、键和值。`for...of` 循环常用于此目的。
5. 动态大小：随着键值对的添加或删除，`Map` 可以动态地增长或缩小。没有预定义的大小限制。
6. 无需字符串键：在对象中，键总是转换为字符串。相比之下，`Map` 允许你使用任何数据类型作为键，而无需自动类型转换。
7. 使用场景：当你需要将任意值与键关联起来，并希望保持插入顺序时，`Map` 非常有用。当键名预先不可知，或者键可以是各种数据类型时，通常会使用它。
8. 与对象的比较：虽然对象也用于存储键值对，但 `Map` 对象在灵活性、迭代顺序和键类型处理方面具有优势。
9. 从数组转换：你可以使用 `Map` 构造函数从键值对数组创建 `Map`。这对于使用初始数据初始化 `Map` 来说非常方便。

`Map` 是 JavaScript 中一种多功能的数据结构，提供了一种处理键值对的灵活方式。它们通常用于对条目顺序重要、且键可以是各种数据类型的场景中。

```javascript
// JavaScript Map Example
```

```javascript
// Creating a Map
let population = new Map([
["New York", 8400000],
["Los Angeles", 3990000],
["Chicago", 2716000]
]);
```

```javascript
// Adding Entries to the Map
population.set("Houston", 23280000);
population.set("Phoenix", 18270000);
```

```javascript
// Checking Map Size
console.log("Map Size: " + population.size);
```

```javascript
// Checking if a Key Exists in the Map
console.log("Does the Map contain 'Los Angeles'? " + population.has("Los Angeles"));
```

```javascript
// Getting the Value for a Key
console.log("Population of 'Chicago': " + population.get("Chicago"));
```

```javascript
// Deleting an Entry from the Map
population.delete("New York");
```

```javascript
// Iterating Over Map Entries
console.log("\nMap Entries:");
for (let [city, pop] of population) {
console.log(city + " " + pop);
}

// Clearing the Map
population.clear();

// Checking Map Size After Clearing
console.log("\nMap Size After Clearing: " + population.size);

// End of JavaScript Map Example
```

```javascript
script.js
1 // JavaScript Set Example
2 // Creating a Set
3 let uniqueNumbers = new Set([1, 2, 3, 4, 5]);
5 // Adding Elements to the Set
6 uniqueNumbers.add(6);
7 uniqueNumbers.add(7);
8 // Checking Set Size
10 console.log("Set Size: " + uniqueNumbers.size);
11
12 // Checking if an Element exists in the Set
13 console.log("Does the Set contain 3? " + uniqueNumbers.has(3));
14 // Deleting an Element from the Set
15 uniqueNumbers.delete(2);
116 // Iterating Over Set Elements
18 console.log("Set Elements:");
19 for (let number of uniqueNumbers) {
20 console.log(number);
21 }
24 // Clearing the Set
25 uniqueNumbers.clear();
27 Checking Set Size After Clearing
28 console.log("Set Size After Clearing: " + uniqueNumbers.size);
31 // End of JavaScript Map Example
```

在此示例中演示了 JavaScript `Map`：

1. 创建 Map：使用初始键值对创建了人口 `Map`。
2. 向 Map 添加条目：使用 `set` 方法向 `Map` 添加了条目（Houston 和 Phoenix）。
3. 检查 Map 大小：使用 `size` 属性检查 `Map` 的大小。
4. 检查键是否存在于 Map：使用 `has` 方法检查 `Map` 是否包含特定的键（在此例中为 "Los Angeles"）。
5. 获取键的值：使用 `get` 方法检索特定键（在此例中为 "Chicago"）的人口值。
6. 从 Map 中删除条目：使用 `delete` 方法从 `Map` 中移除特定键（在此例中为 "New York"）的条目。
7. 遍历 Map 条目：使用 `for` 循环遍历 `Map` 的条目。
8. 清空 Map：使用 `clear` 方法移除 `Map` 中的所有条目。
9. 清空后检查 Map 大小：在清空后再次检查 `Map` 的大小。

此示例演示了 JavaScript `Map` 的基本操作，包括创建、删除、检查、检查键是否存在、获取值、迭代和清空。

# JS Typeof

在 JavaScript 中，`typeof` 运算符是一个内置运算符，用于确定给定表达式或变量的数据类型。

1. 数据类型识别：`typeof` 运算符的主要用途是识别值的数据类型。它返回一个指示操作数类型的字符串。
2. 一元运算符：`typeof` 是一个一元运算符，意味着它只作用于一个操作数。后面跟着要确定其类型的操作数。
3. 字符串结果：`typeof` 运算符的结果始终是一个字符串。它返回操作数数据类型的字符串表示。
4. 可能的返回值：
   - `"undefined"`: 表示操作数是未定义值（`undefined`）。
   - `"boolean"`: 表示操作数是布尔值。
   - `"number"`: 表示操作数是数字。
   - `"string"`: 表示操作数是字符串。
   - `"function"`: 表示操作数是函数。
   - `"object"`: 表示操作数是对象。
   - `"symbol"`: 表示操作数是符号。
   - `"bigint"`: 表示操作数是大整数。

# JS 类型转换

在 JavaScript 中，类型转换是指将值从一种数据类型转换为另一种数据类型的过程。这可以根据上下文隐式或显式地发生。

1. 隐式类型转换（强制类型转换）：隐式类型转换，也称为强制类型转换（coercion），在不同类型的值之间进行操作时会自动发生。JavaScript 会尝试在执行操作之前将一个或两个操作数转换为共同类型。
2. 隐式类型转换示例：隐式类型转换的一个示例是对字符串和数字使用 `+` 运算符。数字会被隐式转换为字符串，此时执行的是字符串拼接而不是加法。
3. 显式类型转换（强制转换）：显式类型转换，也称为强制转换（casting），是指使用语言提供的函数或方法有意地将值从一种类型转换为另一种。这允许你控制并指定所需的类型。
4. 显式类型转换示例：显式类型转换的一个示例是使用 `String()`、`Number()` 或 `Boolean()` 等函数分别将值转换为字符串、数字或布尔值。
5. 字符串转换：要将一个值转换为字符串，可以使用 `String()` 函数或 `toString()` 方法。这通常在你想要将一个值与字符串拼接或执行字符串相关的操作时完成。
6. 数字转换：要将一个值转换为数字，可以使用 `Number()` 函数或 `parseInt()` 和 `parseFloat()` 函数。这在你想要执行数学运算时非常有用。
7. 布尔转换：要将一个值转换为布尔值，可以使用 `Boolean()` 函数。在 JavaScript 中，许多值具有固有的真值（truthy）或假值（falsy）属性，这种转换通常用于条件语句。
8. 关于假值的说明：在条件上下文中，被视为假值的值（例如 `0`、`null`、`undefined`、`NaN`、空字符串）会被隐式转换为 `false`，而真值属性的值则会被转换为 `true`。
9. 复杂操作：在涉及不同类型的复杂操作中，可能会同时发生隐式和显式类型转换。理解 JavaScript 如何处理类型转换对于避免意外行为至关重要。
10. 对 `NaN` 的考虑：请注意，某些操作可能会产生 `NaN`（不是数字），这是一个特殊的数值，表示未定义的操作或无法表示的数学运算的结果。
11. 处理类型转换错误：在显式转换类型时，处理可能的错误很重要，特别是当转换可能无法成功时。

类型转换是 JavaScript 的一个基本方面，理解它是如何通过隐式和显式方式发生的，对于编写可靠且可预测的代码至关重要。留意不同上下文中类型转换相关的潜在陷阱和细微差别是非常重要的。

```javascript
// JavaScript Type Conversion Example
```

```javascript
// Implicit Type Conversion (Coercion)
let numString = "42";
let resultImplicit = 10 + numString;

// Explicit Type Conversion
let numExplicit = Number(numString);
let resultExplicit = 10 + numExplicit;

// Displaying Results
console.log("Implicit Type Conversion: " + resultImplicit); // Concatenation
console.log("Explicit Type Conversion: " + resultExplicit); // Addition

// End of JavaScript Type Conversion Example
```

```javascript
script.js
// JavaScript Type Conversion Example
// Implicit Type Conversion (Coercion)
let numString = "42";
let result = 10 + numString;
// Explicit Type Conversion
let numExplicit = Number(numString);
let resultExplicit = 10 + numExplicit;
// Displaying Results
console.log("Implicit Type Conversion: " + resultImplicit); // Concat
console.log("Explicit Type Conversion: " + resultExplicit); // Add
// End of JavaScript Type Conversion Example
```

在此示例中，演示了 JavaScript 的类型转换：

1. 隐式类型转换（强制转换）：变量 `numString` 是包含字符 "42" 的字符串。当它在与 `+` 运算符和数字 `10` 的操作中使用时，JavaScript 执行隐式类型转换（强制转换）并将其视为拼接，导致字符串 "1042"。
2. 显式类型转换：使用 `Number` 函数进行显式类型转换，将字符串 "42" 转换为数值（`numExplicit`）。当它与 `+` 运算符和数字 `10` 进行操作时，JavaScript 执行加法，产生数值 `52`。
3. 显示结果：使用 `console.log` 显示隐式和显式类型转换的结果。

此示例说明了 JavaScript 中隐式和显式类型转换的概念。隐式类型转换会自动发生，而显式类型转换涉及有意使用 `Number`、`String` 或 `Boolean` 等函数来转换值。

# JS 位运算

1. 在 JavaScript 中，位运算是对直接操作整数二进制表示的单个位的操作。这些操作将操作数视为 32 位的序列（0 和 1）。
2. 位与 (`&`)：位与操作由 `&` 运算符表示。它比较第一个操作数的每个位与第二个操作数的对应位。如果两个位都为 1，则结果位为 1；否则为 0。
3. 位或 (`|`)：位或操作由 `|` 运算符表示。它比较第一个操作数的每个位与第二个操作数的对应位。如果至少有一个位是 1，则结果位为 1；否则为 0。
4. 位异或 (`^`)：位异或（互斥逻辑或）操作由 `^` 运算符表示。它比较第一个操作数的每个位与第二个操作数的对应位。如果两个位中只有一个 1，则结果位为 1；否则为 0。
5. 位取反 (`~`)：位取反操作由 `~` 运算符表示。它翻转操作数的每一个位。
6. 左移 (`<<`)：左移操作由 `<<` 运算符表示。它将第一个操作数的位向左移动指定的位数。
7. 右移 (`>>`)：右移操作由 `>>` 运算符表示。它将位向右移动，并保持符号位。
8. 无符号右移 (`>>>`)：无符号右移操作由 `>>>` 运算符表示。它将第一个操作数的位向右移动指定的位数，并用零填充。

## 用例

位运算通常用于底层编程、密码学和优化操作。

## 性能考虑

在某些情况下，位运算在执行速度方面可以产生更高效的代码。然而，应该谨慎使用，因为它们可能会使代码的可读性降低并更容易出错。

## 二进制表示

在处理位运算时，理解数字的二进制表示至关重要。这些操作直接操作整数的二进制位。

位运算是 JavaScript 中的一种底层功能，并不常作为其他类型的操作使用。它们通常被用于特定的场景，即为了特定的算法或优化目的而必须进行位操作的情况。

```javascript
// JavaScript Bitwise Operators Example
```

```javascript
// Bitwise AND (&)
let bitwiseANDResult = 5 & 3;

// Bitwise OR (|)
let bitwiseORResult = 5 | 3;

// Bitwise XOR (^)
let bitwiseXORResult = 5 ^ 3;

// Bitwise NOT (~)
let bitwiseNOTResult = ~5;

// Left Shift (<<)
let leftShiftResult = 5 << 1;

// Right Shift (>>)
let rightShiftResult = 5 >> 1;

// Unsigned Right Shift (>>>)
let unsignedRightShiftResult = -5 >>> 1;

// Displaying Results
console.log("Bitwise AND: " + bitwiseANDResult);
console.log("Bitwise OR: " + bitwiseORResult);
console.log("Bitwise XOR: " + bitwiseXORResult);
console.log("Bitwise NOT: " + bitwiseNOTResult);
console.log("Left Shift: " + leftShiftResult);
console.log("Right Shift: " + rightShiftResult);
console.log("Unsigned Right Shift: " + unsignedRightShiftResult);

// End of JavaScript Bitwise Operators Example
```

```javascript
script.js
// JavaScript 位运算符示例
// 位与 (&)
let bitwiseANDResult = 5 & 3;
// 位或 (|)
let bitwiseORResult = 5 | 3;
// 位异或 (^)
let bitwiseXORResult = 5 ^ 3;
// 位取反 (~)
let bitwiseNOTResult = ~5;
// 左移 (<<)
let leftShiftResult = 5 << 1;
// 右移 (>>)
let rightShiftResult = 5 >> 1;
// 无符号右移 (>>>)
let unsignedRightShiftResult = 5 >>> 1;
// 显示结果
console.log("Bitwise AND: " + bitwiseANDResult);
console.log("Bitwise OR: " + bitwiseORResult);
console.log("Bitwise XOR: " + bitwiseXORResult);
console.log("Left Shift: " + leftShiftResult);
console.log("Right Shift: " + rightShiftResult);
console.log("Unsigned Right Shift: " + unsignedRightShiftResult);
// JavaScript 位运算符示例结束
```

在此示例中，演示了 JavaScript 的位运算符：

1. 位与 (`&`)：`&` 在数字 5 和 3 的二进制表示之间执行位与操作。
2. 位或 (`|`)：`|` 在数字 5 和 3 的二进制表示之间执行位或操作。
3. 位异或 (`^`)：`^` 在数字 5 和 3 的二进制表示之间执行位异或（逻辑互斥或）操作。
4. 位取反 (`~`)：`~` 对数字 5 的二进制表示执行位取反（按位反）操作。
5. 左移 (`<<`)：`<<` 将数字 5 的二进制表示向左移动一位。
6. 右移 (`>>`)：`>>` 将数字 5 的二进制表示向右移动一位。
7. 无符号右移 (`>>>`)：`>>>` 将负数 -5 的二进制表示向右移动一位，并在最左侧的位置填充零。
8. 显示结果：使用 `console.log` 显示每个位操作的结果。此示例说明了如何在 JavaScript 中使用位运算符进行二进制级操作。

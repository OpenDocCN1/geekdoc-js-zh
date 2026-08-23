
# Javascript 可读代码编写 100 种技巧

## 引言

可读性强的代码是高效编程的基石。

本电子书介绍了 100 种技巧，帮助你编写更好的 JavaScript 代码。这些方法利用 JavaScript 的独特特性和语法，旨在让你的代码对他人尽可能易读。

每种技巧都通过好代码和坏代码的示例进行说明，确保清晰易懂。深入探索，你将发现如何改进编码实践，编写更简洁、更易维护的 JavaScript 代码。

## 1. 使用 `const` 和 `let` 代替 `var` 实现块级作用域变量

使用 `const` 和 `let` 可以确保变量具有块级作用域，从而减少错误并提高代码可读性。`const` 和 `let` 提供块级作用域，有助于防止 `var` 常见的变量提升和作用域泄漏问题。

### 好代码

```javascript
// 使用 const 定义常量
const MAX_USERS = 100;

// 使用 let 定义可能变化的变量
let userCount = 0;

if (userCount < MAX_USERS) {
  let newUser = 'John Doe';
  userCount++;
  console.log(newUser); // John Doe
}
console.log(userCount); // 1
```

### 坏代码

```javascript
// 使用 var，它是函数作用域的，可能引发问题
var MAX_USERS = 100;
var userCount = 0;

if (userCount < MAX_USERS) {
  var newUser = 'John Doe';
  userCount++;
  console.log(newUser); // John Doe
}
console.log(userCount); // 1
console.log(newUser); // John Doe（此处 newUser 可访问，可能带来问题）
```

使用 `const` 和 `let` 有助于避免 `var` 的陷阱，例如意外创建全局变量以及因提升导致的意外行为。`const` 用于不应重新赋值的变量，而 `let` 用于可能变化的变量。

**备忘：**

`var` 声明会被提升到其所在函数或全局作用域的顶部，这可能导致令人困惑的错误。`const` 和 `let` 声明也会被提升，但在其定义被求值之前之前被初始化，从而产生“暂时性死区”，在初始化之前访问它们会抛出错误。

## 2. 利用箭头函数实现更简洁的语法和词法 `this`

箭头函数提供了简洁的语法，并词法绑定 `this` 值，非常适合回调函数和方法。与传统函数表达式相比，它们语法更短，并自动将 `this` 绑定到周围上下文，从而简化代码并避免 `this` 相关的常见陷阱。

### 好代码

```javascript
// 使用箭头函数实现简洁语法和词法 this
const users = ['Alice', 'Bob', 'Charlie'];
users.forEach(user => console.log(user)); // Alice, Bob, Charlie

const user = {
  name: 'John Doe',
  greet: () => {
    console.log(`Hello, my name is ${this.name}`); // 'this' 是词法绑定的，因此指向全局对象
  }
};
user.greet(); // Hello, my name is undefined
```

### 坏代码

```javascript
// 使用传统函数表达式
const users = ['Alice', 'Bob', 'Charlie'];
users.forEach(function(user) {
  console.log(user); // Alice, Bob, Charlie
});

const user = {
  name: 'John Doe',
  greet: function() {
    console.log(`Hello, my name is ${this.name}`); // 'this' 指向 user
  }
};
user.greet(); // Hello, my name is undefined
```

箭头函数特别适用于编写更短、易读的代码，尤其是在回调函数和方法。然而，它们没有自己的 `this` 上文，某些情况下可能带来问题。当需要动态 `this` 上文时，应使用传统函数。

## 3. 利用模板面量简化拼接

使用模板面量简化拼接并提高读性。ES6 引入模板面量通过反引号和嵌入表达式，使字符串更简单。

### 好代码

```javascript
// 使用模板面量进行拼接
const name = "John";
const age = 30;
const greeting = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(greeting); // 输出：Hello, my name is John and I am 30.
```

### 坏代码

```javascript
// 使用传统字符串
const name = "John";
const age = 30;
const greeting = "Hello, my name is " + name + " and I am " + age + " years old.";
console.log(greeting); // 输出：Hello, my name is John and I am 30.
```

模板面量使用反引号代替引号，与使用 `+` 运算符的传统字符串相比，这使代码更读、易维护。

**备忘：**

模板面量支持多行字符串，对于格式化长字符串非常有用。

## 4. 使用对象和数组的解构编写简洁的代码

解构赋值允许以简洁的方式从对象和数组中提取值。ES6 引入解构赋值可以将数组中的值或对象的属性包到不同的变量中。

### 好代码

```javascript
// 使用对象解构赋值
const person = { name: "Alice", age: 25, city: "Wonderland" };
const { name, age, city } = person;
console.log(name); // 输出：Alice
console.log(age); // 输出：25
console.log(city); // 输出：Wonderland

// 使用数组解构赋值
const numbers = [1, 2, 3, 4];
const [first, second, fourth] = numbers;
console.log(first); // 输出：1
console.log(second); // 输出：2
console.log(fourth); // 输出：4
```

### 坏代码

```javascript
// 不使用解构赋值
const person = { name: "Alice", age: 25, city: "Wonderland" };
const name = person.name;
const age = person.age;
const city = person.city;
console.log(name); // 输出：Alice
console.log(age); // 输出：25
console.log(city); // 输出：Wonderland

// 不使用数组解构
const numbers = [1, 2, 3, 4];
const first = numbers[0];
const second = numbers[1];
const fourth = numbers[3];
console.log(first); // 输出：1
console.log(second); // 输出：2
console.log(fourth); // 输出：4
```

解构赋值通过减少重复代码使代码更简洁、易读。它允许直接从对象和数组中提取值，使代码更清晰、易理解。

**备忘：**

解构赋值也可以用于函数参数，实现更灵活、易读的函数签名。

## 5. 应用展开运算符合并数组和对象

使用展开运算符 `...` 轻松合并 JavaScript 中的数组和对象。展开运算符允许数组的元素或对象的属性，无需复杂方法即可轻松合并它们。

### 好代码

```javascript
// 合并数组
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const mergedArray = [...array1, ...array2]; // [1, 2, 3, 4, 5, 6]

// 合并对象
const object1 = { a: 1, b: 2 };
const object2 = { c: 3, d: 4 };
const mergedObject = { ...object1, ...object2 }; // { a: 1, b: 2, c: 3, d: 4 }
```

### 坏代码

```javascript
// 合并数组
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const mergedArray = array1.concat(array2); // [1, 2, 3, 4, 5, 6]

// 合并对象
const object1 = { a: 1, b: 2 };
const object2 = { c: 3, d: 4 };
const mergedObject = Object.assign({}, object1, object2); // { a: 1, b: 2, c: 3, d: 4 }
```

展开运算符更简洁且易读。差的示例使用了旧的方法如 `concat` 和 `Object.assign`，这些方法冗长且不够直观。

**备忘：**

展开运算符在 ES6（ECMAScript 2015）中引入，成为更高效的方式处理数组和对象。

## 6. 使用有意义的变量名描述其用途

有意义的变量名能够清晰描述其用途和内容。有意义的变量名使代码更易读、易维护，帮助其他开发者理解变量用途而无需额外的注释。

### 好代码

```javascript
// 良好的变量名
const totalPrice = 100;
const userAge = 25;
const isLoggedIn = true;
```

### 坏代码

```javascript
// 糟糕的变量名
const x = 100;
const y = 25;
const z = true;
```

良好的示例使用了描述性名称，指明了变量代表的内容。差的示例使用了 `x`、`y` 和 `z` 等通用名称，没有传达任何关于用途的信息。

**备忘：**

使用有意义变量名是整洁代码中的基本实践，正如软件专家 Robert C. Martin 在著作《代码整之道》中所导的那样。

## 7. 布尔变量以 is、has 或 can 作为前缀

布尔变量使用 `is`、`has` 或 `can` 等前缀有助于明确其用途，表明布尔值的真/假性质。

### 好代码

```javascript
// 良好的变量名示例
let isLoggedIn = true;
let hasPrivileges = false;
let canEditProfile = true;
```

### 坏代码

```javascript
// 糟糕的变量名示例
let in = true;
let admin = false;
let edit = true;
```

良好的示例中，前缀 `is`、`has` 和 `can` 清楚地表明了变量类型。差的示例中含义模糊，可能导致混淆。

## 8. 在测量值的变量名中包含单位

始终在变量名中包含单位以避免混淆。

### 好代码

```javascript
// 变量名包含单位的良好示例
let distanceInMeters = 500;
let weightInKilograms = 70;
let timeInSeconds = 120;
```

### 坏代码

```javascript
// 变量名含单位的糟糕示例
let distance = 500;
let weight = 70;
let time = 120;
```

良好的示例中，变量名包含了单位（米、千克、秒），清楚地表明了值代表什么。差的示例中，变量名缺少单位可能导致混淆和潜在错误。

## 9. 变量使用名词，函数使用动词

变量使用名词，函数使用动词，使代码更易读、直观。这种技巧确保变量清晰表示实体或对象，而函数表示动作或过程，有助于快速理解代码中每个元素的用法。

### 好代码

```javascript
// 良好示例
let userName = "John"; // 名词
let age = 30; // 名词
function calculateAge(birthYear) { // 词
  return new Date().getFullYear() - birthYear;
}
function printGreeting(name) { // 词
  console.log(`Hello, ${name}!`);
}
```

### 坏代码

```javascript
// 糟糕示例
let calc = "John"; // 令人困惑的变量名
let calcAge = 30; // 令人困惑的变量名
function user(name) { // 令人困惑的函数名
  console.log(`Hello, ${name}!`);
}
function age(birthYear) { // 令人困惑的函数名
  return new Date().getFullYear() - birthYear;
}
```

## 10. 避免使用非通用理解的缩写

使用清晰的全名而非缩写，可以提高代码的可读性并减少混淆。确保任何阅读代码的人都能轻松理解每个变量或函数的作用，而无需猜测或查找其含义。

### 好代码

```javascript
// 良好示例
let totalPrice = 150.00;
function calculateTotalPrice(price, tax) {
  return price + (price * tax);
}
function displayProductDetails(product) {
  console.log(`Product: ${product.name}, Price: ${product.price}`);
}
```

### 坏代码

```javascript
// 糟糕示例
let tp = 150.00;
function calcTP(p, t) {
  return p + (p * t);
}
function dspPD(p) {
  console.log(`Product: ${p.n}, Price: ${p.p}`);
}
```



## 11. 避免使用像 `data`、`item` 或 `thing` 这样的通用名称。

使用具体名称使代码更易读、更易维护。

在本节中，我们将说明为什么使用具体的变量名对于代码清晰度至关重要。

< Good Code >

```javascript
// 根据用户 ID 获取用户资料
function getUserProfile(userId) {
    // 从数据库获取用户资料
    let userProfile = database.fetchProfileById(userId);
    return userProfile;
}
```

<Bad Code>

```javascript
// 根据 ID 获取某些内容
function getData(id) {
    // 从数据库获取数据
    let data = database.fetch(id);
    return data;
}
```

在好的代码示例中，`userProfile` 和 `userId` 清楚地表明了函数处理的内容，使代码更易理解和维护。在差的代码示例中，`data` 和 `id` 过于通用，可能导致对正在处理的数据类型产生混淆。

<Memo>

良好的命名约定可以显著降低开发者的认知负荷，帮助他们快速掌握代码的功能。

## 12. 命名要具体，避免歧义。

## 命名与代码质量最佳实践

具体的命名有助于理解变量和函数的准确用途与用法。本节将展示命名中的具体性如何防止误解并提升代码清晰度。

### 优秀代码

```javascript
// 将产品添加到购物车
function addProductToCart(productId, quantity) {
    // 确保产品存在
    let product = productCatalog.getProductById(productId);
    if (product) {
        cart.addItem(product, quantity);
    }
}
```

### 糟糕代码

```javascript
// 添加一个项目
function addItem(id, num) {
    // 确保项目存在
    let item = catalog.get(id);
    if (item) {
        cart.add(item, num);
    }
}
```

在优秀代码示例中，`addProductToCart`、`productId` 和 `quantity` 清晰地定义了函数的目的及其参数，使其易于理解和维护。在糟糕代码示例中，`addItem`、`id` 和 `num` 含义模糊，不清楚添加的是什么以及是在什么上下文中添加。

**提示：** 具体的命名不仅有助于理解代码，还有助于调试，因为更容易追踪特定实体在应用程序中的流转。

## 在整个代码库中使用一致的命名约定

对变量、函数和类采用统一的命名约定，以增强代码的可读性和可维护性。一致的命名约定有助于开发者快速理解变量和函数的用途，减少阅读和维护代码时的认知负担。

### 优秀代码

```javascript
// 变量和函数使用 camelCase，类使用 PascalCase
let userName = 'JohnDoe';

function getUserName() {
    return userName;
}

class UserProfile {
    constructor(name) {
        this.name = name;
    }
}
```

### 糟糕代码

```javascript
// 不一致的命名约定
let User_name = 'JohnDoe';

function GetuserName() {
    return User_name;
}

class userprofile {
    constructor(Name) {
        this.Name = Name;
    }
}
```

在优秀示例中，变量和函数使用 `camelCase`，类使用 `PascalCase`，使代码更具可预测性且易于阅读。在糟糕示例中，不一致的命名约定使代码难以理解和维护。

**提示：** JavaScript 并未强制要求任何特定的命名约定，但遵循一致的风格（例如变量和函数使用 `camelCase`，类使用 `PascalCase`）是广泛接受的最佳实践。

## 避免使用魔法数字，改用命名常量

用命名常量替换魔法数字，使代码更易理解和维护。魔法数字是缺乏上下文的硬编码值。使用命名常量可以提供有意义的名称，解释这些值的用途。

### 优秀代码

```javascript
// 使用命名常量
const MAX_USERS = 100;
const TIMEOUT_DURATION = 5000;

function canAddUser(currentUserCount) {
    return currentUserCount < MAX_USERS;
}

setTimeout(() => {
    console.log('超时已到达');
}, TIMEOUT_DURATION);
```

### 糟糕代码

```javascript
// 使用魔法数字
function canAddUser(currentUserCount) {
    return currentUserCount < 100;
}

setTimeout(() => {
    console.log('超时已到达');
}, 5000);
```

在优秀示例中，命名常量如 `MAX_USERS` 和 `TIMEOUT_DURATION` 提供了上下文，使代码不言自明。在糟糕示例中，魔法数字 `100` 和 `5000` 不传达任何含义，使代码更难理解和维护。

**提示：** “魔法数字”一词指的是直接在代码中使用数字字面量。这种做法不推荐，因为它可能导致错误并降低代码可读性。使用命名常量是提升代码质量简单而有效的方法。

## 确保函数名称清晰描述其行为

使用描述性的函数名称，清晰传达函数的用途和行为。函数名称应能让阅读代码的其他开发者立即明白其目的和行为。

### 优秀代码

```javascript
// 优秀示例
function calculateCircleArea(radius) {
  return Math.PI * radius * radius;
}
```

### 糟糕代码

```javascript
// 糟糕示例
function doSomething(x) {
  return Math.PI * x * x;
}
```

优秀示例使用了描述性名称 `calculateCircleArea`，清晰解释了函数。糟糕示例使用了模糊名称 `doSomething`，未提供任何关于函数目的或行为的信息。

**提示：** 描述性的函数名称提升代码的可读性。

## 利用默认参数使代码简洁

在函数中使用默认参数处理定义或缺失。默认参数允许你提供默认值，使代码健壮且易阅读。

### 优秀代码

```javascript
// 优秀示例
function greetUser(name = 'User') {
  console.log(`Hello, ${name}`);
}

greetUser('Alice'); // 输出: Alice!
greetUser(); // 输出: User!
```

### 糟糕代码

```javascript
// 糟糕示例
function greetUser(name) {
  const userName = name || 'User';
  console.log(`Hello, ${userName}`);
}
```

优秀示例中，`greetUser` 函数为 `name` 参数使用了默认值。糟糕示例使用逻辑或运算符处理参数，可能导致意外行为，且可读性差。

## 使用 async/await 处理异步代码以可读性

`async/await` 简化了异步代码语法，使其易阅读和维护。在 JavaScript 中使用 `async/await` 可以提升代码的可读性和结构，比传统的 Promise 链更易理解。

### 优秀代码

```javascript
// 使用 async/await
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('获取数据出错:', error);
  }
}

fetchData();
```

### 糟糕代码

```javascript
// 使用 Promise
function fetchData() {
  fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => {
      console.log(data);
    })
    .catch(error => {
      console.error('获取数据出错:', error);
    });
}
```

优秀示例使异步流程线性化。糟糕示例使用了 Promise 链，随着复杂度增加可能难以阅读。

**提示：** `async/await` 是建立在 Promise 之上的语法糖。它在 ES2017 (ES8) 中引入，已成为 JavaScript 中编写异步代码的标准。

## 使用 Map 和 Set 处理集合，而非普通对象和数组

与普通对象和数组相比，`Map` 和 `Set` 提供了更高效、更清晰的方式处理数据集合。在 JavaScript 中使用 `Map` 和 `Set` 可以为集合提供更好的性能和功能，例如 `Set` 确保元素唯一性，`Map` 维护键值对。

### 优秀代码

```javascript
// 使用 Map 处理键值对
const userRoles = new Map();
userRoles.set('Alice', 'Admin');
userRoles.set('Bob', 'User');
console.log(userRoles.get('Alice')); // 输出: Admin

// 使用 Set 处理唯一值
const uniqueNumbers = new Set([1, 2, 3, 3, 4]);
uniqueNumbers.add(5);
uniqueNumbers.add(1); // 重复值，不会被添加

uniqueNumbers.forEach(number => {
  console.log(number); // 输出: 1, 2, 3, 4, 5
});
```

### 糟糕的代码

```javascript
// Using plain object for key-value pairs
const userRoles = {
  Alice: 'Admin',
  Bob: 'User'
};
console.log(userRoles['Alice']); // Output: Admin

// Using array for unique values
const uniqueNumbers = [1, 2, 3, 3, 4];
uniqueNumbers.push(5);
if (!uniqueNumbers.includes(1)) {
  uniqueNumbers.push(1); // Manually checking for duplicates
}
uniqueNumbers.forEach(number => {
  console.log(number); // Output: 1, 2, 3, 4, 5
});
```

好的示例使用了 `Map` 和 `Set`，它们分别专为管理键值对集合和唯一值而设计。它们提供了内置方法，可以简化常见任务并提高性能。而糟糕的示例使用了普通对象和数组，在确保唯一性或管理键值对等任务时需要额外的逻辑。

**备忘**

`Map` 和 `Set` 在 ES6 (ES2015) 中引入。与对象不同，`Maps` 维护键的插入顺序；与数组不同，`Sets` 自动强制执行唯一性。

## 19. 利用可选链（optional chaining）处理嵌套对象属性。

使用可选链安全地访问深层嵌套的对象属性，而不会导致程序报错。

可选链允许你在无需检查每一层是否存在的情况下访问对象的嵌套属性，使你的代码更简洁。

### 优秀代码

```javascript
// Good example using optional chaining
const user = {
  profile: {
    address: {
      city: 'New York'
    }
  }
};
const city = user?.profile?.address?.city; // 输出: New York
```

### 糟糕的代码

```javascript
// Bad example manually checking
const user = {
  profile: {
    address: {
      city: 'New York'
    }
  }
};
let city;
if (user && user.profile && user.profile.address) {
  city = user.profile.address.city;
}
```

优秀示例使用了可选链 (`?.`)，清晰解释了功能。糟糕示例则手动检查每一层，导致代码冗长且难以阅读。

**备忘：** 可选链在 ECMAScript 2020 (ES11) 中引入，目前在现代 JavaScript 环境中广泛支持。

## 20. 使用 Array.prototype.map 和 Array.prototype.filter 进行转换。

利用 `map` 和 `filter` 以简洁且可读的方式转换数组。`map` 方法创建一个新数组，其元素是数组每个元素调用函数后的结果。`filter` 方法创建一个新数组，包含所有通过测试的元素。

### 优秀代码

```javascript
// Good example using map and filter
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map(num => num * 2); // [2, 4, 6, 8, 10]
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]
```

### 糟糕的代码

```javascript
// Bad example using for loops
const numbers = [1, 2, 3, 4, 5];
const doubled = [];
for (let i = 0; i < numbers.length; i++) {
  doubled.push(numbers[i] * 2);
}
const evens = [];
for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] % 2 === 0) {
    evens.push(numbers[i]);
  }
}
```

优秀示例使用了 `map` 和 `filter`，使代码更声明性。糟糕示例使用了 `for` 循环，更加冗长且容易出错。


```
```javascript
// This function calculates the factorial of a number using recursion
function factorial(n) {
    // Base case: if n is 0, return 1
    if (n === 0) {
        return 1;
    }
    // Recursive case: n * factorial of (n-1)
    return n * factorial(n - 1);
}
```

### 糟糕的代码

```javascript
function factorial(n) {
    if (n === 0) {
        return 1;
    }
    return n * factorial(n - 1);
}
```

在好的示例中，注释清晰地解释了函数的目的以及基础情况（`base case`）和递归情况（`recursive case`）背后的逻辑。这使得代码更容易理解和维护。在糟糕的示例中，缺乏注释使得他人难以把握函数的意图和逻辑。

 备忘

为复杂代码编写注释是软件开发中的最佳实践，并且在编码标准和指南中经常被强调。

## 22. 在注释中解释非显而易见的代码逻辑。

使用注释来阐明代码中非显而易见或棘手的部分，以帮助他人理解逻辑。

当代码逻辑不能立即被看清时，添加注释来解释推理过程或方法可以防止在未来的维护过程中产生混淆和错误。

### 好的代码

```javascript
// Check if the user is an admin or has a premium account
function hasAccess(user) {
    // Admins have full access
    if (user.role === 'admin') {
        return true;
    }
    // Premium users have access if their subscription is active
    if (user.subscription === 'premium' && user.isActive) {
        return true;
    }
    // All other users do not have access
    return false;
}
```

### 糟糕的代码

```javascript
function hasAccess(user) {
    if (user.role === 'admin') {
        return true;
    }
    if (user.subscription === 'premium' && user.isActive) {
        return true;
    }
    return false;
}
```

在好的示例中，注释解释了每个条件背后的逻辑，明确了为什么某些用户拥有访问权限。这有助于其他开发人员理解决策过程。在糟糕的示例中，缺乏注释使得逻辑容易被误解，从而导致错误或错误的假设。

 备忘

清晰简洁的注释可以显著减少代码审查和调试所需的时间，从而提高开发效率。

## 23. 为函数的预期输入和输出编写文档。

清晰地记录函数的预期输入参数和输出结果。

为函数的预期输入和输出提供清晰的文档，有助于其他开发人员了解如何正确使用该函数以及对其结果的预期。

### 好的代码

```javascript
/**
* Calculates the sum of two numbers.
* @param {number} a - The first number.
* @param {number} b - The second number.
* @returns {number} The sum of the two numbers.
*/
function add(a, b) {
    return a + b;
}
```

### 糟糕的代码

```javascript
function add(a, b) {
    return a + b;
}
```

在好的示例中，函数 `add` 使用注释进行了记录，将输入参数 `a` 和 `b` 描述为数字，将输出描述为数字。这向其他开发人员明确了函数需要什么以及返回什么。在糟糕的示例中，没有文档，使得他人难以理解函数的目的和用法。

 备忘

使用 JSDoc 注释是 JavaScript 中的常见做法，用于为函数、类和方法提供详细文档。它有助于自动生成 API 文档。

## 24. 用注释标出临时的权宜之计。

使用注释来标出代码中任何临时的权宜之计（`workarounds`）或黑客技巧（`hacks`）。

当你实现临时解决方案或权宜之计（`hack`）时，务必添加注释说明其存在的原因以及未来需要如何替换它。

### 良好代码示例

```javascript
// 针对问题 #123 的临时解决方案
// 这是绕过第三方库中 Bug 的权宜之计
// TODO: 待库更新后移除该代码
function fetchData() {
    // Hack: 手动设置超时以避免 Bug
    setTimeout(() => {
        // 原始代码
        console.log('Fetching data...');
    }, 1000);
}
```

### 不良代码示例

```javascript
function fetchData() {
    setTimeout(() => {
        console.log('Fetching data...');
    }, 1000);
}
```

在良好示例中，注释明确指出了 `setTimeout` 是针对已知问题（#123`）的临时解决方案，并包含 `TODO` 注释，提示问题解决后移除该代码。这有助于其他开发者理解代码的上下文和临时性。而在不良示例中，没有任何注释，导致其他开发者不清楚 `setTimeout` 背后的原因以及未来可能需要重新审视这段代码。

 备忘录：使用 `TODO` 注释是跟踪临时解决方案并确保其在未来更新中得到处理的好习惯。许多代码编辑器和 IDE 可以高亮显示 `TODO` 注释，使其更易于查找。

## 使用注释标记代码的重要部分

注释有助于突出和解释代码中的重要部分。使用注释标记重要部分可以使代码更易于导航和理解。

### 良好代码示例

```javascript
// 初始化变量
let total = 0;
let count = 0;

// 遍历数组
for (let i = 0; i < numbers.length; i++) {
  total += numbers[i];
  count++;
}

// 计算平均值
let average = total / count;
console.log(average);
```

### 不良代码示例

```javascript
let total = 0;
let count = 0;
for (let i = 0; i < numbers.length; i++) {
  total += numbers[i];
  count++;
}
let average = total / count;
console.log(average);
```

在良好示例中，注释清晰说明了每个部分，使他人更容易理解。不良示例缺少注释，导致代码结构和目的难以理解。

 备忘录：注释不会影响执行，但对于维护和理解至关重要，尤其是在协作环境中。

## 保持注释简洁了

注释应简短且直接与描述的代码相关。简洁的注释可以避免混乱，确保代码保持读性和维护性。

### 良好代码示例

```javascript
// 对数组中的值求和
let sum = numbers.reduce((acc, num) => acc + num, 0);
// 输出结果
console.log(sum);
```

### 不良代码示例

```javascript
// 这是一个循环，遍历名为 numbers 的数组中的元素，并将每个元素加到累加上，累加器初始值为0，返回数组中所有元素的和
let sum = numbers.reduce((acc, num) => acc + num, 0);
// 这行代码将和打印到控制台
console.log(sum);
```

良好示例使用了简短清晰的注释，直接解释了代码的用途。不良示例的注释过于冗长，添加了不必要的细节，使代码难阅读。

 备忘录：过度注释与没有注释同样有害，增加了负担。

## 代码变更时更新注释以保持准确

始终更新注释以反映代码的变更，确保其准确且有用。修改代码时务必更新相关注释，防止给读者带来错误和困惑。

### 良好代码示例

```javascript
// 计算矩形的面积
function calculateArea(width, height) {
    return width * height; // 面积 = 宽 × 高
}

// 计算矩形的面积（带验证）
function calculateArea(width, height) {
    if (width <= 0 || height <= 0) {
        throw new Error('宽度和高度为正数');
    }
    return width * height; // 面积 = 宽 × 高
}
```

### 不良代码示例

```javascript
// 计算矩形的面积
function calculateArea(width, height) {
    return width * height; // 面积 = 宽 × 高
}

// 更新为包含验证，但注释未更新
function calculateArea(width, height) {
    if (width <= 0 || height <= 0) {
        throw new Error('宽度和高度为正数');
    }
    return width * height; // 面积 = 宽 × 高
}
```

在良好示例中，注释已更新以反映新的验证逻辑，确保任何阅读代码的人都能理解当前功能。不良示例中，注释仍然过时，可能会误导读者对代码行为的理解。

 备忘录：持续更新注释有助于维护代码质量，并减少因误解目的和功能而导致的 Bug 风险。

## 避免冗余注释，不要陈述显而易见的内容

避免编写仅仅复述代码功能的注释，因为它们没有增加价值，反而使代码变得杂乱。注释应提供代码本身无法立即明确的额外上下文或解释，而不是陈述显而易见的内容。

### 良好代码示例

```javascript
// 计算矩形的面积
function calculateArea(width, height) {
    return width * height; // 面积 = 宽 × 高
}

// 检查用户是否为成年人
function isAdult(age) {
    return age >= 18; // 如果年龄为 18 岁或以上，返回 true
}
```

### 不良代码示例

```javascript
// 此函数计算矩形的面积
function calculateArea(width, height) {
    return width * height; // 此函数返回面积
}

// 此函数检查用户是否为成年人
function isAdult(age) {
    return age >= 18; // 如果年龄为 18 岁或以上，返回 true
}
```

在良好示例中，注释提供了有意义的上下文，补充了代码。不良示例中，注释是冗余的，仅仅复述了代码已经清晰表达的内容，增加了不必要的杂乱。

 备忘录：有效的注释应通过提供代码中不明显的见解来增强代码的可读性，而不是重复代码已经传达的信息。

## 使用注释解释“为什么”，而不是“是什么”

注释应提供代码背后的上下文和理由，而不仅仅是描述代码的功能。

### 良好代码示例

```javascript
// 计算折扣后的总价
// 这是为了给忠实客户提供更好的优惠
function calculateTotalPrice(price, discount) {
    return price - (price * discount);
}
```

### 不良代码示例

```javascript
// 从价格中减去折扣
function calculateTotalPrice(price, discount) {
    return price - (price * discount);
}
```

在良好示例中，注释解释了计算折扣后总价的原因，为未来的读者提供了上下文。不良示例中，注释仅仅描述了代码的功能，而代码本身已经足够清晰。

 备忘录：有效的注释可以显著提高代码的可维护性，并帮助新开发者更快地理解代码库。

## 使用语法正确的规范英语编写注释

注释应使用清晰、语法正确的英语编写。使用完整的句子和正确的语法显得专业。

### 良好代码示例

```javascript
// 应用折扣后的总价
// 确保忠实客户获得最佳优惠
function calculateTotalPrice(price, discount) {
    return price - (price * discount);
}
```

### 不良代码示例

```javascript
// 折扣总价
function calculateTotalPrice(price, discount) {
    return price - (price * discount);
}
```

在良好示例中，注释使用了完整的句子和正确的语法，显得专业。不良示例中，注释使用了简写形式并显得不专业。

 备忘录：在协作环境中，使用正确的英语显得至关重要。

## 利用 ES6 类进行面向对象编程。

使用 ES6 类创建清晰、模块化的代码。ES6 类提供了清晰简洁的语法创建对象和处理继承，使代码更易读和维护。

### 良好代码

```javascript
// Good example using ES6 classes
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name);
  }
  speak() {
    console.log(`${this.name} barks.`);
  }
}

const dog = new Dog('Rex');
dog.speak(); // Rex barks.
```

### 差的

```javascript
// Bad example using ES5 function constructors
function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function() {
  console.log(this.name + ' makes a noise.');
};

function Dog(name) {
  Animal.call(this, name);
}

Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;

Dog.prototype.speak = function() {
  console.log(this.name + ' barks.');
};

var dog = new Dog('Rex');
dog.speak(); // Rex barks.
```

在良好示例中，ES6 类提供了一种更直观且不易出错的方式创建对象和处理继承。差示例使用了 ES5 函数构造函数和原型链，这更加冗长且难以阅读。

 备忘录：ES6 类是对 JavaScript 现有基于原型的继承模型的语法糖。它们并没有为语言引入新的面向对象继承模型。

## 使用 Promise.all 并发运行多个 Promise。

利用 `Promise.all` 高效地并发处理多个异步操作。

`Promise.all` 允许你并行运行多个 Promise，并等待所有 Promise 完成或任何一个拒绝，从而更轻松地管理并发异步任务。
```

```javascript
// Good example using Promise.all
const promise1 = fetch('https://api.example.com/data1');
const promise2 = fetch('https://api.example.com/data2');
const promise3 = fetch('https://api.example.com/data3');

Promise.all([promise1, promise2, promise3])
  .then(responses => Promise.all(responses.map(response => response.json())))
  .then(data => {
    console.log(data); // Array of results from all promises
  })
  .catch(error => {
    console.error('One of the promises failed:', error);
  });
```

### 差的代码

```javascript
// Bad example without using Promise.all
const promise1 = fetch('https://api.example.com/data1');
const promise2 = fetch('https://api.example.com/data2');
const promise3 = fetch('https://api.example.com/data3');

promise1
  .then(response1 => response1.json())
  .then(data1 => {
    console.log(data1);
    return promise2;
  })
  .then(response2 => response2.json())
  .then(data2 => {
    console.log(data2);
    return promise3;
  })
  .then(response3 => response3.json())
  .then(data3 => {
    console.log(data3);
  })
  .catch(error => {
    console.error('One of the promises failed:', error);
  });
```

好的示例使用 `Promise.all` 并发运行所有 `fetch` 请求，效率更高且代码更简洁。差的示例顺序执行 Promise，效率较低且难以阅读。

**备忘录**

如果任何一个输入的 `Promise` 拒绝，`Promise.all` 会立即拒绝；只有当所有输入的 `Promise` 都解决时，它才会解决。

## 利用 Object.keys 和 Object.values 遍历对象。

使用 `Object.keys` 和 `Object.values` 高效地遍历对象的属性和值。在 JavaScript 中处理对象时，使用 `Object.keys` 和 `Object.values` 可以更清晰、更易读地遍历其属性和值。

### 好的代码

```javascript
const user = {
  name: 'Alice',
  age: 25,
  city: 'Wonderland'
};

// Iterating over keys
Object.keys(user).forEach(key => {
  console.log(`${key}: ${user[key]}`);
});

// Iterating over values
Object.values(user).forEach(value => {
  console.log(value);
});
```

### 差的代码

```javascript
const user = {
  name: 'Alice',
  age: 25,
  city: 'Wonderland'
};

// Using for...in loop
for (let key in user) {
  if (user.hasOwnProperty(key)) {
    console.log(`${key}: ${user[key]}`);
  }
}

// Using for...in loop for values
for (let key in user) {
  if (user.hasOwnProperty(key)) {
    console.log(user[key]);
  }
}
```

好的示例使用 `Object.keys` 和 `Object.values` 遍历对象的属性和值，使代码更易读并避免了 `hasOwnProperty` 检查。差的示例使用 `for...in` 循环，需要额外检查以确保只遍历对象自身的属性，代码不够简洁。

**备忘录**

`Object.entries` 也可用于同时遍历键和值，返回键值对数组。

## 使用 ??（空值合并）运算符设置默认值。

`??` 运算符提供了一种简洁的方式，在处理 `null` 或 `undefined` 时分配默认值。空值合并运算符（`??`）是 JavaScript 中一个有用的工具，用于在变量为 `null` 或 `undefined` 时设置默认值，使代码更易读，并避免与假值相关的常见陷阱。

### 好的代码

```javascript
let userInput = null;
let defaultText = 'Default text';

// Using ?? operator
let displayText = userInput ?? defaultText;
console.log(displayText); // Output: 'Default text'
```

### 差的代码

```javascript
let userInput = null;
let defaultText = 'Default text';

// Using || operator
let displayText = userInput || defaultText;
console.log(displayText); // Output: 'Default text'
```

好的示例使用 `??` 运算符仅在 `userInput` 为 `null` 或 `undefined` 时分配 `defaultText`，确保其他假值如 `0` 或 `''` 不会被错误替换。差的示例使用 `||` 运算符，它会替换任何假值，而不仅仅是 `null` 或 `undefined`，可能导致意外行为。

**备忘录**

`??` 运算符在 ECMAScript 2020（ES11）中引入，特别适用于 `0`、`false` 或 `''` 是有效值且不应触发默认赋值的情况。

## 使用 fetch 进行网络请求，而非 XMLHttpRequest 等旧方法。

使用现代的 `fetch` API 进行网络请求，以编写更清晰、更易读的代码。`fetch` API 是一种基于 Promise 的现代 JavaScript 网络请求方式。它比旧的 `XMLHttpRequest` 方法更强大、更灵活，并且能带来更易读、更易维护的代码。

### 好的代码

```javascript
// Good example using fetch
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw Error('Network response not ok');
    }
    return response.json();
  })
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error('Problem with the fetch operation:', error);
  });
```

### 差的代码

```javascript
// Bad example using XMLHttpRequest
var xhr = new XMLHttpRequest();
xhr.open('GET', 'https://api.example.com/data', true);
xhr.onreadystatechange = function () {
  if (xhr.readyState === 4 && xhr.status === 200) {
    var data = JSON.parse(xhr.responseText);
    console.log(data);
  }
};
xhr.send();
```

`fetch` API 通过使用 Promise 简化了网络请求，使代码更容易读。相比之下 `XMLHttpRequest` 需要更多的样板代码，且不够直观。`fetch` API 还提供了错误处理和强大的功能。

**备忘**：`fetch` API 于 2015 年作为标准引入，现在已被现代浏览器广泛支持。它设计比 `XMLHttpRequest` 更灵活、易用。

## 使用像 ESLint 这样的 linter 来统一格式化

使用像 `ESLint` 这样的 linter 确保代码一致并早发现潜在错误。`ESLint` 是一个流行的 linter，帮助开发者保持一致的风格，并在问题出现之前捕获。将 `ESLint` 集成到你的开发流中，你可以确保代码库保持整洁。

### 良好代码

```javascript
// Good example with ESLint rules
function add(a, b) {
  if (typeof a !== 'number' || typeof b !== 'number') {
    throw new TypeError('Arguments must be numbers');
  }
  return a + b;
}

const result = add(2, 3);
console.log(result); // Outputs: 5
```

### 糟糕代码

```javascript
// Bad example without ESLint rules
function add(a,b) {
  return a+b;
}

var result = add(2,3)
console.log(result)
```

`ESLint` 有助于在整个项目中执行一致的编码标准，使多个开发者更容易协作。它可以自动修复一些问题，为其他问题提供警告。

**备忘**：`ESLint` 由 Nicholas C. Zak 于 2013 年创建，旨在帮助开发者编写一致无错误的 JavaScript 代码。它具有高度可配置性，并支持自定义规则，使其成为任何 JavaScript 项目的工具。

## 使用 Prettier 进行自动代码格式化

`Prettier` 是一个代码格式化工具，它通过解析你的代码并按照自己的规则重新打印来执行一致的风格。`Prettier` 有助于在整个项目中保持统一风格，使他人更容易阅读和你的代码。

### 良好代码

```javascript
// Good: Consistent formatting with Prettier
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet('Alice');
```

### 糟糕代码

```javascript
// Bad: Inconsistent formatting
function greet(name){console.log("Hello "+name+"!");} greet('Alice');
```

`Prettier` 根据一组规则自动格式化你的代码，确保一致性。在良好示例中，代码整洁，缩进和间距适当。在糟糕示例中，代码间距和格式不一致，使其更难阅读。

**备忘**：`Prettier` 支持多种语言并与大多数编辑器集成，使其成为维护代码质量的工具。

## 使用一致的缩进来组织代码

一致的缩进提高了代码的可读性，并有助于理解代码的结构和流程。适当的缩进对于使代码可读和维护至关重要。它在视觉上分隔了代码块，使逻辑更易于跟踪。

### 良好代码

```javascript
// Good: Consistent indentation
if (true) {
  console.log('This is properly indented.');
  if (true) {
    console.log('Nested block is also properly indented.');
  }
}
```

### 糟糕代码

```javascript
// Bad: Inconsistent indentation
if (true) {
console.log('This is not properly indented.');
  if (true) {
console.log('Nested block is also not properly indented.');
  }
```

一致的缩进有助于一目了然地理解代码结构。在良好示例中，每个块都正确缩进，使代码易于理解。在糟糕示例中，不一致的缩进使得难以辨别代码结构，导致潜在的错误和误解。

**备忘**：大多数现代代码编辑器都可以配置为强制执行一致的缩进，无论是使用空格还是制表符，根据项目的风格指南。

## 将相关代码逻辑分组

通过将相关的函数、变量和类分组来组织代码。将相关代码分组有助于理解程序的结构和流程。它使代码更易维护和导航。

### 良好代码

```javascript
// User-related functions
function createUser(name, age) {
  return { name, age };
}

function getUser(id) {
  // logic to get user by id
}

// Product-related functions
function createProduct(name, price) {
  return { name, price };
}

function getProduct(id) {
  // logic to get product by id
}
```

### 糟糕代码

```javascript
function createUser(name, age) {
    return { name, age };
}

function createProduct(name, price) {
    return { name, price };
}

function getUser(id) {
    // logic to get user by id
}

function getProduct(id) {
    // logic to get product by id
}
```

在良好示例中，与用户相关的函数被分组在一起，与产品相关的函数被分组在一起。这种逻辑分组使得找到找到理解与特定功能相关的代码。在糟糕示例中，函数分散，使得导航和理解代码更加困难。

**备忘**：代码的逻辑分组是 SOLID 原则中单一职责原则（`SRP`）的一个原则，该原则指出一个类或模块只有一个改变的理由。

## 限制行长度以提高可读性

保持代码行简短，理想情况下不超过 80 个字符，以增强可读性。长代码行可能难以阅读和理解。将它们拆分为更短的行使代码更易读和可维护。

### 良好代码

```javascript
// Good: Short lines of code
function calculateTotal(price, taxRate) {
  const tax = price * taxRate;
  const total = price + tax;
  return total;
}

const totalPrice = calculateTotal(100, 0.08);
console.log(totalPrice);
```

content]
```javascript
// Bad: Long line of code
function calculateTotal(price, taxRate) { const tax = price * taxRate; const total = price + tax; return total; } const totalPrice = calculateTotal(100, 0.08); console.log(totalPrice);
```

在良好示例中，代码被拆分为多行，使得更容易阅读和理解每个部分。在糟糕示例中，代码写在一行长行中，难以快速阅读和理解。

> **备忘**：80 字符的行长度限制是一种惯例，可追溯到计算早期，至今仍在许多编码标准中被广泛推荐，包括 Python 的 `PEP 8`。

## 使用提前返回来避免嵌套 if 语句

通过使用提前返回而不是深层嵌套的 `if` 语句来简化代码。深层嵌套的 `if` 语句会使代码难以阅读和理解。使用提前返回可以简化逻辑并提高可读性。

### 良好代码

```javascript
function processValue(value) {
    if (value === null) {
        return 'Value is null';
    }
    if (value === undefined) {
        return 'Value is undefined';
    }
    if (typeof value !== 'number') {
        return 'Value is not a number';
    }
    return value * 2; // Value is a valid number, process it
}
```

### 糟糕代码

```javascript
function processValue(value) {
    if (value !== null) {
        if (value !== undefined) {
            if (typeof value === 'number') {
                return value * 2; // Value is a valid number, process it
            } else {
                return 'Value is not a number';
            }
        }
    }
}
```

```javascript
            }

        } else {

            return 'Value is undefined';

        }

    } else {

        return 'Value is null';

    }

}
```

在好的示例中，每个条件都被立即检查和处理，使代码易于理解。而坏的示例则将每个条件嵌套在前一个条件内部，导致深度嵌套且难以阅读的代码。

<备忘录>

提前返回也有助于减少读者的认知负担，使其更容易识别函数的主要逻辑。

42

## 优先使用 switch 语句进行多重条件检查。

***

使用 `switch` 语句代替多个 `if-else` 语句，以提高可读性和可维护性。

***

当处理依赖于同一变量的多个条件时，`switch` 语句提供了一种更清晰、更有条理的方式来处理逻辑。

< 好代码 >

```javascript
function getFruitColor(fruit) {
    switch (fruit) {
        case 'apple':
            return 'red';
        case 'banana':
            return 'yellow';
        case 'grape':
            return 'purple';
        case 'orange':
            return 'orange';
        default:
            return 'unknown';
    }
}
```

< 坏代码 >

```javascript
function getFruitColor(fruit) {
    if (fruit === 'apple') {
        return 'red';
    } else if (fruit === 'banana') {
        return 'yellow';
    } else if (fruit === 'grape') {
        return 'purple';
    } else if (fruit === 'orange') {
        return 'orange';
    } else {
        return 'unknown';
    }
}
```

好的示例使用了 `switch` 语句，简洁且易于阅读。坏的示例使用了多个 `if-else` 语句，随着条件数量的增加，这些语句可能更难阅读和维护。

<备忘录>

在某些情况下，`switch` 语句可能比多个 `if-else` 语句更高效，因为它们为被检查的条件提供了清晰的结构。

43

## 通过将循环拆分为函数来避免深度嵌套的循环。

***

通过将复杂的嵌套循环重构为单独的函数来简化它们，以提高可读性和维护性。

***

深度嵌套的循环会使代码难以阅读和理解。将它们拆分为更小、命名良好的函数有助于澄清逻辑，并使代码更易于维护。

< 好代码 >

```javascript
// Good example: Breaking nested loops into functions

function processRow(row) {
  row.forEach(cell => {
    // Process each cell
    console.log(cell);
  });
}

function processTable(table) {
  table.forEach(row => {
    processRow(row);
  });
}

const table = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

processTable(table);
```

< 坏代码 >

```javascript
// Bad example: Deeply nested loops

const table = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

for (let i = 0; i < table.length; i++) {
  for (let j = 0; j < table[i].length; j++) {
    // Process each cell
    console.log(table[i][j]);
  }
}
```

在好的示例中，嵌套循环被拆分为 `processRow` 和 `processTable` 函数，使代码更加模块化且易于理解。在坏的示例中，深度嵌套的循环使代码难阅读和维护。

<备忘录>

将嵌套循环重构为函数提高了可读性，还允许更轻松地调试代码的各个部分。

4

## 使用 try/catch 块进行错误处理。

***

实现 `try/catch` 块以优雅地处理错误，防止应用程序崩溃。

***

错误处理在任何应用程序中都关重要，以确保能够处理意外情况而崩溃。使用 `try/catch` 块让你管理错误并提供有意义的反馈。

< 好代码 >

```javascript
// Good example: Using try/catch for error handling
function parseJSON(jsonString) {
  try {
    const data = JSON.parse(jsonString);
    console.log('Parsed data:', data);
  } catch (error) {
    console.error('Failed to parse JSON:', error.message);
  }
}

const jsonString = '{"name": "John", "age": 30}';
parseJSON(jsonString);

const invalidJsonString = '{"name": "John", "age": 30';
parseJSON(invalidJsonString);
```

< 坏代码 >

```javascript
// Bad example: No error handling
function parseJSON(jsonString) {
  const data = JSON.parse(jsonString);
  console.log('Parsed data:', data);
}

const jsonString = '{"name": "John", "age": 30}';
parseJSON(jsonString);

const invalidJsonString = '{"name": "John", "age": 30';
parseJSON(invalidJsonString); // This will throw an error and crash the application
```

在好的示例中，`parseJSON` 函数使用 `try/catch` 块来处理解析时可能出现的错误，可以防止应用程序崩溃。在坏的示例中，缺少错误处理意味着任何错误都会导致崩溃。

<备忘录>

使用 `try/catch` 块不仅有助于处理错误，还有助于调试代码中出了问题。

5

## 保持函数简短并专注于单一任务。

***

执行单一、明确任务的函数以提高可读性和维护性。

***

一个函数应该只做件事，这使得代码更容易理解。

< 好代码 >

```javascript
// Function to calculate the area of a rectangle
function calculateRectangleArea(width, height) {
  return width * height;
}

// Function to calculate the area of a circle
function calculateCircleArea(radius) {
  return Math.PI * radius * radius;
}
```

< 坏代码 >

```javascript
// Function that calculates the area of a rectangle or circle
function calculateArea(shape, width, height, radius) {
  if (shape === 'rectangle') {
    return width * height;
  } else if (shape === 'circle') {
    return Math.PI * radius * radius;
  }
  return 0;
}
```

在好的示例中，每个函数都有单一职责，清楚地表明了函数的功能。在坏的示例中，该函数试图处理多种形状，使其复杂且难以理解。

<备忘录>

单一职责原则（SRP）是面向对象设计的原则之一，它规定一个类或函数只有一个理由。

46

## 使用描述性的函数名称来传达目的。

***

选择能够清晰描述功能的名称，以提高可读性。

***

描述性名称有助于其他开发人员在不阅读函数实现的情况下理解目的。

< 好代码 >

```javascript
// Function to fetch user data from an API
function fetchUserData(userId) {
  // Implementation to fetch user data
}

// Function to validate email format
function isValidEmail(email) {
  // Implementation to validate email
}
```

< 坏代码 >

```javascript
// Function with a vague name
function getData(id) {
  // Implementation to fetch user data
}

// Function with a non-descriptive name
function checkEmail(e) {
  // Implementation to validate email
}
```

在好的示例中，函数名称清晰地表明了其目的，使代码更易于阅读和理解。在坏的示例中，名称模糊，没有足够的上下文来说明函数的功能。

<备忘录>

使用描述性名称是 Clean Code 原则的一部分，该原则强调易于阅读和理解的代码。

47

## 编写没有副作用的纯函数。

***

纯函数在给定相同参数时返回相同的结果，并且不会引起副作用。

***

纯函数是指给定相同输入，总是返回相同输出，并且没有任何副作用（例如修改全局变量或输出到控制台）的函数。

< 好代码 >

```javascript
// A pure function that adds two numbers
function add(a, b) {
  return a + b; // Always returns the same output for the same inputs
}

console.log(add(2, 3)); // 5
console.log(add(2, 3)); // 5
```

### 不纯函数示例

**糟糕的代码**

```javascript
let sum = 0;

// 一个不纯函数，用于相加两个数
function add(a, b) {
    sum = a + b; // 修改全局变量
    console.log(sum); // 产生副作用
}

add(2, 3); // 输出 5 并改变 sum
add(2, 3); // 再次输出 5 并改变 sum
```

纯函数更容易测试和调试，因为它们不依赖或改变其作用域之外的状态。糟糕的示例展示了一个不纯函数，它修改全局变量并输出到控制台，使其行为更难预测。

**备忘**

纯函数是函数式编程中的基本概念，它强调不可变性和使用纯函数来创建可靠的代码。

javascript
// 糟糕示例：对固定值使用变量
let maxUsers = 100;
let apiUrl = 'https://api.example.com/data';

function fetchData() {
  fetch(apiUrl)
    .then(response => response.json())
    .then(data => console.log(data));
}

console.log(`最大用户数为 ${maxUsers}`);
```

在良好示例中，`MAX_USERS` 和 `API_URL` 使用 `const` 声明为常量，表明它们的值不应改变。这使得代码更易于理解和维护。在糟糕示例中，`maxUsers` 和 `apiUrl` 使用 `let` 声明，暗示它们的值可能会改变，可能引起混淆。

**备忘**

在 JavaScript 中，常量是块级作用域的，类似于使用 `let` 声明的变量。它们不能被重新赋值，但如果常量是对象或数组，其内容仍然可以被修改。

---

## 利用异步生成器处理异步迭代

异步生成器提供了一种强大的方式来处理异步迭代，使代码更易读且更高效。异步生成器允许你使用 `for await...of` 循环遍历异步数据源。这种技术简化了异步操作的处理，例如从 API 获取数据，允许你在数据可用时逐条处理。

**良好的代码**

```javascript
// 良好示例：使用异步生成器进行异步迭代
async function* fetchData() {
  const urls = ['https://api.example.com/data1', 'https://api.example.com/data2'];
  for (const url of urls) {
    const response = await fetch(url);
    const data = await response.json();
    yield data;
  }
}

(async () => {
  for await (const data of fetchData()) {
    console.log(data);
  }
})();
```

**糟糕的代码**

```javascript
// 糟糕示例：使用 Promise 而不使用异步生成器
const urls = ['https://api.example.com/data1', 'https://api.example.com/data2'];

function fetchData() {
  return Promise.all(urls.map(url => fetch(url).then(response => response.json())));
}

fetchData().then(dataArray => {
  dataArray.forEach(data => console.log(data));
});
```

在良好示例中，使用异步生成器函数 `fetchData` 从多个 URL 获取数据。`for await...of` 循环允许在获取每条数据时进行处理，使代码更易读且更高效。在糟糕示例中，使用 `Promise.all` 一次性获取所有数据，可能效率较低且更难阅读。

**备忘**

异步生成器是在 ECMAScript 2018（ES9）中引入的。它们结合了生成器和异步函数的能力，允许你以更自然、更易读的方式处理异步数据流。

---

## 利用 WeakMap 和 WeakSet 管理对象键而不阻止垃圾回收

`WeakMap` 和 `WeakSet` 允许你管理对象键而不阻止其垃圾回收，从而提高内存效率。使用 `WeakMap` 和 `WeakSet` 可以帮助管理对象键和引用，同时确保这些对象在不再需要时可以被垃圾回收。这对于缓存或跟踪对象以避免内存泄漏。

**良好的代码**

```javascript
// 良好示例：使用 WeakMap 存储元数据
const metadata = new WeakMap();

function addMetadata(obj, info) {
  metadata.set(obj, info); // 将元数据与对象关联
}

function getMetadata(obj) {
  return metadata.get(obj); // 获取元数据
}

const obj1 = {};
addMetadata(obj1, { role: 'admin' });
console.log(getMetadata(obj1)); // 输出 { role: 'admin' }
```

**糟糕的代码**

```javascript
// 糟糕示例：使用常规 Map 会阻止回收
const metadata = new Map();

function addMetadata(obj, info) {
  metadata.set(obj, info); // 将元数据与对象关联
}

function getMetadata(obj) {
  return metadata.get(obj); // 获取元数据
}

const obj1 = {};
addMetadata(obj1, { role: 'admin' });
console.log(getMetadata(obj1)); // 输出 { role: 'admin' }
```

在良好示例中，`WeakMap` 允许 `obj1` 在不再引用时被回收，因为 `WeakMap` 持有弱引用。在糟糕示例中，使用常规 `Map` 会阻止 `obj1` 被回收，因为 `Map` 持有强引用。

**备忘**

`WeakMap` 的键必须是对象，而不能是原始值。

---

## 使用 Proxy 实现基本操作

JavaScript 中的 `Proxy` 对象允许你为基本操作（属性查找、赋值、枚举）定义自定义行为。使用 `Proxy` 对象可以帮助拦截并重新定义对象。

**良好的代码**

```javascript
// 良好示例：使用 Proxy 拦截访问
const handler = {
  get(target, property) {
    console.log(`属性 ${property} 被访问`);
    return target[property];
  }
};

const obj = { name: 'John', age: 30 };
const proxy = new Proxy(obj, handler);

console.log(proxy.name); // 属性 name 被访问。输出 John
console.log(proxy.age); // 属性 age 被访问。输出 30
```

**糟糕的代码**

```javascript
// 糟糕示例：在属性访问中直接添加日志
const obj = { name: 'John', age: 30 };

function getName() {
  console.log('属性 name 被访问');
  return obj.name;
}

function getAge() {
  console.log('属性 age 被访问');
  return obj.age;
}

console.log(getName()); // 属性 name 被访问。输出 John
console.log(getAge()); // 属性 age 被访问。输出 30
```

在优秀示例中，使用 `Proxy` 拦截访问操作，提供了一种干净且复用的方式。而在糟糕示例中，日志被直接添加到函数中，导致代码可维护性差，且随着属性增多难以扩展。

**备忘录：**

`Proxy` 还用于创建虚拟对象，这些对象没有真实属性，但能动态响应属性访问。这在实现基于数据库的对象或复杂机制等场景中非常有用。

---

## 利用 Symbol 创建唯一属性键避免冲突

使用 `Symbols` 在对象中创建唯一的属性键，防止键冲突。JavaScript 中的 `Symbols` 提供了一种为对象属性创建唯一标识的方法，确保这些键是唯一的，并避免与其他键发生潜在冲突。

**优秀代码**

```javascript
// 创建一个唯一的 Symbol
const uniqueKey = Symbol('uniqueKey');

// 将 Symbol 用作属性键
const myObject = {
  [uniqueKey]: '这是一个唯一的属性值',
  commonKey: '这是一个普通的属性值'
};

console.log(myObject[uniqueKey]); // 输出：这是一个唯一的属性值
```

**糟糕的代码**

```javascript
// 使用字符串作为属性键
const myObject = {
  uniqueKey: '这应该是唯一的',
  commonKey: '这是一个普通的属性值',
  uniqueKey: '这被覆盖了'
};

console.log(myObject.uniqueKey); // 输出：这被覆盖了
```

使用 `Symbols` 作为属性键可以确保每个键都是唯一的，且不会被意外覆盖。在糟糕示例中，使用字符串键导致 `uniqueKey` 属性被覆盖，而在优秀示例中，`Symbol` 确保了键的唯一性。

**备忘录：**

`Symbols` 是 ECMAScript 2015（ES6）引入的原始数据类型，且不可枚举，意味着它们不会出现在 `for...in` 循环中。

---

## 使用带标签的模板字面量创建安全的 HTML 或 SQL 模板

使用带标签的模板字面量创建安全且格式良好的 HTML 或 SQL 模板。JavaScript 中的带标签模板字面量提供了一种强大的方式来处理和净化模板字面量，这对于创建安全的 HTML 或 SQL 模板尤其有用。

**优秀代码**

```javascript
// 用于转义 HTML 的标签函数
function escapeHTML(literals, ...placeholders) {
  let result = '';
  for (let i = 0; i < literals.length; i++) {
    result += literals[i];
    if (i < placeholders.length) {
      result += String(placeholders[i]).replace(/[&<>"']/g, char => {
        return {
          '&': '&amp;',
          '<': '&lt;',
          '>': '&gt;',
          '"': '&quot;',
          "'": '&#39;'
        }[char];
      });
    }
  }
  return result;
}

const name = '<img src=x onerror=alert("xss")>';
const safeHTML = escapeHTML`<div>Hello, ${name}</div>`;
console.log(safeHTML); // 输出：<div>Hello, &lt;img src=x onerror=alert(&quot;xss&quot;)&gt;</div>
```

**糟糕的代码**

```javascript
// 直接将变量嵌入
const name = '<img src=x onerror=alert("xss")>';
const unsafeHTML = `<div>Hello, ${name}</div>`;
console.log(unsafeHTML); // 输出：<div>Hello, <img src=x onerror=alert("xss")></div>
```

在优秀示例中，`escapeHTML` 函数允许你在嵌入值之前进行净化，这对安全性至关重要。而在糟糕示例中，直接嵌入会导致 XSS 等漏洞。

**备忘录：**

带标签模板字面量是 ECMAScript 2015（ES6）引入的高级特性。

---

## 使用 Reflect API 执行操作

`Reflect` API 提供了执行操作的方法，避免了使用通方法。与其直接使用属性访问器，不如使用 `Reflect` API 以更清晰的方式执行操作。

**优秀代码**

```javascript
const obj = { x: 1, y: 2 };

// 获取属性值
console.log(Reflect.get(obj, 'x')); // 输出：1

// 设置属性值
Reflect.set(obj, 'x', 3);
console.log(obj.x); // 输出：3

// 检查属性是否存在
console.log(Reflect.has(obj, 'y')); // 输出：true
```

**糟糕的代码**

```javascript
const obj = { x: 1, y: 2 };

// 获取属性值
console.log(obj.x); // 输出：1

// 设置属性值
obj.x = 3;
console.log(obj.x); // 输出：3

// 检查属性是否存在
console.log('y' in obj); // 输出：true
```

`Reflect` API 提供了一种函数式的方式来处理对象，使代码更易读性。它还允许更好地处理边界情况。

**备忘录：**

`Reflect` 在 ECMAScript 6（ES6）中引入，是标准库的一部分。

---

## 尽可能在变量使用处声明变量

尽可能在变量使用处声明变量，以提高代码的可读性和维护性。通过将变量声明在靠近其使用的位置，可以更好地理解变量的作用域和用途，使代码更易读、更易维护。

**优秀代码**

```javascript
function calculateArea(radius) {
  const PI = 3.14159; // 将 PI 常量在靠近其使用的位置
  const area = PI * radius ** 2;
  return area;
}

const radius = 5;
const circleArea = calculateArea(radius);
console.log(circleArea); // 输出：78.53975
```

**糟糕的代码**

```javascript
const PI = 3.14159; // 将 PI 常量在远离其使用的位置

function calculateArea(radius) {
  const area = PI * radius ** 2;
  return area;
}

const radius = 5;
const circleArea = calculateArea(radius);
console.log(circleArea); // 输出：78.53975
```

将变量声明在靠近其使用的位置，通过提供上下文并减少理解代码所需的认知负荷，提高了代码的可读性。它还有助于防止命名冲突，并使变量的作用域推理更加容易。

**备忘录：**

这一原则在软件工程中常被称为“最小惊讶原则”或“就近原则”。

---

## 为循环计数器使用有意义的名称

为循环计数器使用描述性名称，可以提高代码的可读性和维护性。编写循环时，通常使用单字母变量 `i`、`j` 或 `k` 作为循环计数器。然而，使用更具描述性的名称可以使代码更于理解，尤其是对于不熟悉代码库的人。

**优秀代码**

```javascript
// 遍历学生数组
for (let studentIndex = 0; studentIndex < students.length; studentIndex++) {
    console.log(students[studentIndex].name);
}
```

**糟糕的代码**

```javascript
// 遍历学生数组
for (let i = 0; i < students.length; i++) {
    console.log(students[i].name);
}
```

在好的示例中，`studentIndex` 清晰地表明循环计数器与数组中学生的索引相关。这使得代码更易读、更易理解。而在差的示例中，`i` 的描述性较差，导致一眼难以理解循环的用途。

> **备忘**：在嵌套循环中使用多个计数器时，为循环计数器使用有意义的名称尤为重要。描述性名称有助于避免混淆和潜在错误。


```javascript
let totalScore = 0;
let averageScore = 0;

// 计算总分
for (let i = 0; i < scores.length; i++) {
    totalScore += scores[i];
}

// 计算平均分
averageScore = totalScore / scores.length;

console.log("总分:", totalScore);
console.log("平均分:", averageScore);
```

### 差的代码

```javascript
let score = 0;

// 计算总分
for (let i = 0; i < scores.length; i++) {
    score += scores[i];
}

// 计算平均分
score = score / scores.length;

console.log("总分:", score); // 错误地标记为总分
console.log("平均分:", score);
```

在好的示例中，`totalScore` 和 `averageScore` 分别用于特定目的，使代码清晰易懂。在差的示例中，变量 `score` 被重复用于总分和平均分的计算，这可能导致混淆，并可能错误理解代码意图。

> **备忘录**：重复使用变量还可能导致意外的副作用，尤其是在较大的代码库中，变量的值可能被意外更改。始终追求代码的清晰性和关注点分离。

## 在声明变量时进行初始化

始终在声明变量时进行初始化，以避免未定义的值并提高代码可读性。

在声明变量时进行初始化有助于防止与未定义值相关的错误，并使代码更于理解。

### 好的代码

```javascript
// 好的示例：变量在声明时初始化
let count = 0; // count 初始化为 0
let name = 'John'; // name 初始化为 'John'
let isActive = true; // isActive 初始化为 true
```

### 差的代码

```javascript
// 差的示例：变量声明时未初始化
let count; // count 为 undefined
let name; // name 为 undefined
let isActive; // isActive 为 undefined
```

在好的示例中，每个变量都被赋予了初始值，这使得代码更可预测且更易于调试。在差的示例中，变量声明时未初始化，如果在赋值前使用它们，可能导致意外行为。

> **备忘录**：JavaScript 中声明但未初始化的变量会自动被赋值为 `undefined`。

## 使用常量存储配置值

使用常量存储不会改变的配置值，确保它们易于识别和维护。

将配置值存储在常量中可以使代码更易于维护，并降低意外修改这些值的风险。

### 好的代码

```javascript
// 好的示例：配置值存储在常量中
const MAX_USERS = 100; // 最大用户数
const API_URL = 'https://api.example.com'; // API 的基础 URL
const TIMEOUT = 5000; // 超时时间（毫秒）
```

### 差的代码

```javascript
// 差的示例：配置值硬编码在代码中
let users = 100; // 最大用户数
let url = 'https://api.example.com'; // API 的基础 URL
let timeout = 5000; // 超时时间（毫秒）
```

在好的示例中，配置值存储在常量中，便于识别和修改。在差的示例中，值被硬编码，这会使代码更难维护，并且在需要更新值时更容易出错。

> **备忘录**：使用常量存储配置值还可以提高性能，因为这些值不会在每次使用时被重新求值。

## 将执行多项任务的函数拆分为更小的函数

通过将函数拆分为更小的、单一用途的函数来简化函数。

当函数试图完成过多任务时，它们会变得难以阅读、理解和维护。将它们拆分为更小的函数可以提高清晰度和可重用性。

### 好的代码

```javascript
// 好的示例：函数被拆分为更小的、单一用途的函数。
function getUserData(userId) {
    // 获取用户数据
    return fetch(`/api/user/${userId}`)
        .then(response => response.json());
}

function renderUserData(userData) {
    // 将用户数据渲染到 UI
    const userDiv = document.getElementById('user');
    userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;
}

function loadUser(userId) {
    getUserData(userId)
        .then(userData => {
            renderUserData(userData);
        });
}
```

### 差的代码

```javascript
// 差的示例：单个函数做了太多事情。
function loadUser(userId) {
    // 获取用户数据
    fetch(`/api/user/${userId}`)
        .then(response => response.json())
        .then(userData => {
            // 将用户数据渲染到 UI
            const userDiv = document.getElementById('user');
            userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;
        });
}
```

在好的示例中，`getUserData()` 和 `renderUserData()` 是单一用途的函数。`loadUser()` 协调这些较小的函数，使代码更易于理解和维护。在差的示例中，一个函数同时负责数据获取和渲染，使其更难阅读和修改。

> **备忘录**：单一职责原则（SRP）是软件工程中的一个基本概念，它指出一个函数或类应该只有一个改变的理由，这通过让函数只做一件事来实现。

## 通过将代码划分为模块来分离点

通过将代码划分为模块来组织代码。

关注点意味着将代码划分为不同的部分（模块），每个部分负责特定方面。这增强了代码的维护性、重用性和可读性。

### 好的代码

```javascript
// userData.js
export function getUserData(userId) {
    return fetch(`/api/user/${userId}`)
        .then(response => response.json());
}

// render.js
export function renderUserData(userData) {
    const userDiv = document.getElementById('user');
    userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;
}

// main.js
import { getUserData } from './userData.js';
import { renderUserData } from './render.js';

function loadUser(userId) {
    getUserData(userId)
        .then(userData => {
            renderUserData(userData);
        });
}
```

### 差的代码

```javascript
// 差的示例：所有代码都在文件中
function loadUser(userId) {
    // 获取用户数据
    fetch(`/api/user/${userId}`)
        .then(response => response.json())
        .then(userData => {
            // 将用户数据渲染到 UI
            const userDiv = document.getElementById('user');
            userDiv.innerHTML = `<h2>${userData.name}</h2><p>${userData.email}</p>`;
        });
}
```

## 限制函数参数

减少函数中的参数，提高可读性和维护性。

参数过多的函数会变得难以阅读和维护。通过限制参数，你可以让代码更易理解和使用。

### 良好代码

```javascript
// 良好示例：使用选项对象限制参数
function createUser({ name, age, email }) {
  // 函数实现
  console.log(`Name: ${name}, Age: ${age}, Email: ${email}`);
}

createUser({ name: "John", age: 30, email: "john@example.com" });
```

### 糟糕代码

```javascript
// 糟糕示例：参数过多
function createUser(name, age, email, address, isAdmin) {
  // 函数实现
  console.log(`Name: ${name}, Age: ${age}, Email: ${email}`);
}

createUser("John", 30, "john@example.com", "123 Main St", false);
```

在良好示例中，使用选项对象封装参数，使函数调用更简洁、灵活。在糟糕示例中，参数过多导致调用混乱且难以管理。

**提示**：使用选项对象不仅能提高可读性，还能在改变函数签名的情况下，更轻松地未来添加新参数。

## 使用辅助函数封装复杂逻辑

将复杂逻辑封装在辅助函数中，以提高可读性和重用性。

函数中的复杂逻辑会使其难以阅读和理解。将复杂逻辑拆分为更小、可复用的函数，能增强清晰度和维护性。

### 良好代码

```javascript
// 良好示例：使用辅助函数
function calculateTotal(items) {
  return items.reduce((total, item) => total + calculateItemPrice(item), 0);
}

function calculateItemPrice(item) {
  const tax = calculateTax(item.price);
  return item.price + tax;
}

function calculateTax(price) {
  return price * 0.1;
}

const items = [
  { name: "Book", price: 15 },
  { name: "Pen", price: 5 },
];

console.log(calculateTotal(items)); // 输出: 22
```

### 糟糕代码

```javascript
// 糟糕示例：所有逻辑在一个函数中
function calculateTotal(items) {
  return items.reduce((total, item) => {
    const tax = item.price * 0.1;
    const itemPrice = item.price + tax;
    return total + itemPrice;
  }, 0);
}

const items = [
  { name: "Book", price: 15 },
  { name: "Pen", price: 5 },
];

console.log(calculateTotal(items)); // 输出: 22
```

在良好示例中，逻辑被拆分为更小、可复用的函数：`calculateItemPrice` 和 `calculateTax`。这使得 `calculateTotal` 函数更简洁、更易理解。在糟糕示例中，所有逻辑都塞进一个函数，导致代码难以阅读和维护。

**提示**：使用辅助函数不仅能提高代码可读性，还能促进代码复用和测试，使调试和扩展功能更加容易。

## 编写单元测试以确保函数正确执行单一职责

单元测试有助于验证各个函数是否正确执行其预期任务。

编写单元测试可以确保代码库中的每个函数都按预期工作，使代码更可靠、更易于维护。

### 良好代码

```javascript
// 两数相加的函数
function add(a, b) {
  return a + b;
}

// 测试示例
function testAdd() {
    console.assert(add(2, 3) === 5, "2 + 3 should equal 5");
}
```

### 糟糕代码

```javascript
// 糟糕示例：缺少测试
function add(a, b) {
  return a + b;
}
```

通过单元测试可以确保代码库中的每个函数都按预期工作，使代码更可靠、更易于维护。


```javascript
function fetchData() {
  fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('获取数据时出错：', error));
}

fetchData();
```

函数前的 `async` 关键字使其成为异步函数。在异步函数内部，你可以使用 `await` 关键字暂停执行，等待 `Promise` 解析后再继续。这使得代码更易读、更易推理，因为它避免了深层嵌套的回调或 `Promise` 链。`try...catch` 块用于处理异步操作期间可能发生的任何错误。

**提示：** `Async` 函数是在 ECMAScript 2017（ES8）中引入的，为 `Promises` 提供了语法糖。

## 利用 for...of 遍历可迭代对象

`for...of` 循环提供了一种简洁的方式来遍历可迭代对象，使代码更具可读性和表现力。

`for...of` 循环专为遍历可迭代对象而设计，例如数组、字符串、`Map`、`Set` 以及其他实现了可迭代协议的对象。

### 良好代码

```javascript
const fruits = ['apple', 'banana', 'orange'];

for (const fruit of fruits) {
  console.log(fruit);
}
```

### 糟糕代码

```javascript
const fruits = ['apple', 'banana', 'orange'];

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```

在遍历数组或其他可迭代对象时，`for...of` 循环比传统的 `for` 循环更简洁、更具表现力。它会自动从可迭代对象中获取值，无需手动索引。这使得代码更易读，且不易出现差一错误。此外，`for...of` 循环还可用于其他可迭代对象，如字符串、映射和集合。

<Memo>
`for...of` 循环是在 ECMAScript 2015 (ES6) 中引入的，是 JavaScript 新迭代协议的一部分。
</Memo>

## 使用 Array.prototype.reduce 累加数组值

使用 `Array.prototype.reduce` 累加数组中的值，以提高可读性和可维护性。

`Array.prototype.reduce` 是一个强大的方法，它可以将数组中的值累加为单个结果。它特别适用于求和、拼接字符串或合并对象。

<Good Code>
```javascript
// 好的示例：使用 reduce 对数组值求和
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log(sum); // 输出: 15
```
</Good Code>

<Bad Code>
```javascript
// 不好的示例：使用 for 循环对数组值求和
const numbers = [1, 2, 3, 4, 5];
let sum = 0;
for (let i = 0; i < numbers.length; i++) {
  sum += numbers[i];
}
console.log(sum); // 输出: 15
```
</Bad Code>

好的示例使用了 `reduce`，它更简洁且具表现力，清晰地表达了累加值的图。不好的示例使用了 `for` 循环，冗长且不够声明式。

<Memo>
`Array.prototype.reduce` 还用于更复杂的操作，例如展平数组或从数组查找。
</Memo>

## 使用 Object.assign 合并对象

使用 `Object.assign` 将多个对象合并为一个，以提高代码效率。`Object.assign` 是一个方法，将一个或多个源对象的所有属性复制到目标对象。对于合并对象以及创建组合属性的新对象有用。

<Good Code>
```javascript
// 好的示例：使用 Object.assign 合并
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const mergedObj = Object.assign({}, obj1, obj2);
console.log(mergedObj); // 输出: { a: 1, b: 3, c: 4 }
```
</Good Code>

<Bad Code>
```javascript
// 不好的示例：手动合并
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const mergedObj = {};
for (let key in obj1) {
  mergedObj[key] = obj1[key];
}
for (let key in obj2) {
  mergedObj[key] = obj2[key];
}
console.log(mergedObj); // 输出: { a: 1, b: 3, c: 4 }
```
</Bad Code>

好的示例使用了 `Object.assign`，更简洁且避免了手动合并可能错误。不好的示例使用了 `for` 循环，冗长且容易。

<Memo>
`Object.assign` 执行的是浅拷贝，只复制第一层的属性。对于深克隆，需要其他方法或库，如 `lodash`。
</Memo>

## 将长条件表达式拆分为多行

将复杂的条件表达式拆分为多行来简化，提高可读性。长条件表达式难以阅读和理解，将其拆分为多行。

<Good Code>
```javascript
// 好的示例：将长条件表达式拆分为多行
if (
    user.isActive &&
    user.isVerified &&
    user.hasSubscription &&
    user.isValid
) {
    // 执行某些操作
    console.log("处于活跃状态、已验证且有效订阅");
}
```
</Good Code>

<Bad Code>
```javascript
// 不好的示例：长条件表达式在一行
if (user.isActive && user.isVerified && user.hasSubscription && user.isValid) {
    // 执行某些操作
    console.log("处于活跃状态、已验证且有效订阅");
}
```
</Bad Code>

在好的示例中，条件表达式被拆分为多行，使得每个条件易于阅读。不好的示例中，整个表达式在一行，难以阅读和调试。

<Memo>
长条件表达式拆分为多行不仅是 JavaScript 中的良好实践，在其他语言中也是如此。它有助于维护代码，并使他人更容易理解。
</Memo>

## 使用临时变量保存表达式中的中间结果

将中间结果存储在临时变量中，以简化复杂表达式并提高可读性。通过将中间结果存储在临时变量中，可以简化复杂表达式，使代码更易读和调试。

<Good Code>
```javascript
// 好的示例：使用临时变量保存中间结果
const isUserActive = user.isActive;
const isUserVerified = user.isVerified;
const hasValidSubscription = user.hasSubscription && user.isValid;
if (isUserActive && isUserVerified && hasValidSubscription) {
    // 执行某些操作
    console.log("处于活跃状态、已验证且有效订阅");
}
```
</Good Code>

<Bad Code>
```javascript
// 不好的示例：没有使用临时变量的表达式
if (user.isActive && user.isVerified && user.hasSubscription && user.isValid) {
    // 执行某些操作
    console.log("处于活跃状态、已验证且有效订阅");
}
```
</Bad Code>

在好的示例中，中间结果存储在临时变量中，使得最终的条件表达式更简单、易读。不好的示例中，复杂表达式直接写在条件语句中，难以阅读和维护。

<Memo>
使用临时变量不仅提高了可读性，还有助于调试，因为你可以记录中间结果并了解逻辑可能失败。
</Memo>

## 将复杂表达式重构为辅助函数

将复杂表达式拆分为更小、可复用的辅助函数来简化。复杂表达式难以阅读和维护，将其重构为辅助函数可以提高可读性和可复用性。

<Good Code>
```javascript
// 辅助函数：计算折扣
function calculateDiscount(price, discountRate) {
    return price * (discountRate / 100);
}

// 使用辅助函数的主函数
function getTotalPrice(price, discountRate) {
    const discount = calculateDiscount(price, discountRate);
    return price - discount;
}

const price = 100;
const discountRate = 10;
console.log(getTotalPrice(price, discountRate)); // 输出: 90
```
</Good Code>

<Bad Code>
```javascript
// 复杂表达式直接写在主函数
function getTotalPrice(price, discountRate) {
    return price - (price * (discountRate / 100));
}
```
</Bad Code>

在好的示例中，复杂的计算被重构为辅助函数 `calculateDiscount`，使得主函数易读。不好的示例中，复杂表达式嵌入主函数，难以阅读。

<Memo>
将复杂表达式重构为辅助函数不仅提高了可读性，还使得测试更加容易。
</Memo>

## 避免链式使用三元运算符

使用 `if-else` 语句代替链式三元运算符来提高可读性。链式三元运算符会使代码难以阅读和理解。

<Good Code>
```javascript
// 使用 if-else 语句
function getStatusMessage(status) {
    if (status === 'success') {
        return '操作成功';
    } else if (status === 'error') {
        return '出错';
    } else if (status === 'loading') {
        return '加载中...';
    } else {
        return '未知状态';
    }
}
```
</Good Code>

<Bad Code>
```javascript
// 链式三元运算符
function getStatusMessage(status) {
    return status === 'success' ? '操作成功' : status === 'error' ? '出错' : status === 'loading' ? '加载中...' : '未知状态';
}
```
</Bad Code>

在好的示例中，`if-else` 语句逻辑清晰易懂。糟糕的示例中，链式三元运算符难以阅读，尤其是对于不熟悉该语法的人。

<Memo>
三元运算符适用于简单的赋值，但对于复杂的逻辑，通常推荐使用 `if-else` 语句。
</Memo>

## 使用括号明确运算顺序

在代码中使用括号有助于明确运算顺序，使他人更容易理解。编写复杂表达式时，执行顺序可能不清晰，使用括号可以确保意图明确。

<Good Code>
```javascript
// 使用括号使顺序清晰
let result = (a + b) * (c - d); // 先做加法和减法，再做乘法
```
</Good Code>

<Bad Code>
```javascript
// 顺序不直观
let result = a + b * c - d; // 乘法先执行，一眼看不出来
```
</Bad Code>

在好的示例中，括号明确指定了运算顺序，代码易读。在糟糕的示例中，缺少括号使得确定顺序更加困难，可能导致误解和潜在错误。

<Memo>
在 JavaScript 中，运算顺序遵循标准数学规则：乘法和除法优先于加法和减法。然而，使用括号可以覆盖此顺序以确保清晰。
</Memo>

## 将无关功能封装到独立函数中

将无关功能封装到独立函数中可以提高代码的模块化、可读性和维护性。当代码的不同部分执行不同任务时，最好将这些任务封装到独立的函数中。这种做法使代码更模块化、易读且易维护或调试。

<Good Code>
```javascript
// 将无关任务分离到独立函数
function calculateSum(a, b) {
    return a + b;
}

function printMessage(message) {
    console.log(message);
}

let sum = calculateSum(5, 10);
printMessage(`总和是 ${sum}`);
```
</Good Code>

<Bad Code>
```javascript
// 无关任务混合在单个函数中
function calculateAndPrint(a, b) {
    let sum = a + b;
    console.log(`总和是 ${sum}`);
}

calculateAndPrint(5, 10);
```
</Bad Code>

在好的示例中，`calculateSum` 和 `printMessage` 函数各自执行单一、定义明确的任务。这种分离使代码更易理解和维护。在糟糕的示例中，将计算和打印合并到一个函数中，降低了模块化程度，也更难复用或测试。

<Memo>
模块化代码是软件工程中的关键原则。它允许开发者在应用程序的不同部分复用函数，减少冗余并提高维护性。
</Memo>

## 使用工具库处理常见任务

利用像 `Lodash` 这样的工具库来处理数组、对象、字符串等常见操作。与其为常见任务编写自定义函数，不如使用提供优化且经过充分实现的工具库。

### 良好的代码

```javascript
// 使用 Lodash
const _ = require('lodash');
const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = _.map(numbers, n => n * 2); // [2, 4, 6, 8, 10]

const users = [
  { name: 'Alice', age: 25 },
  { name: 'Bob', age: 30 },
  { name: 'Charlie', age: 35 }
];
const userNames = _.map(users, 'name'); // ['Alice', 'Bob', 'Charlie']
```

content]
```javascript
// 自定义实现
const numbers = [1, 2, 3, 4, 5];
const doubledNumbers = [];
for (let i = 0; i < numbers.length; i++) {
  doubledNumbers.push(numbers[i] * 2);
}

const users = [
  { name: 'Alice', age: 25 },
  { name: 'Bob', age: 30 },
  { name: 'Charlie', age: 35 }
];
const userNames = [];
for (let i = 0; i < users.length; i++) {
  userNames.push(users[i].name);
}
```

像 `Lodash` 这样的工具库提供了大量用于常见操作的函数，节省开发时间并减少代码重复。它们针对性能进行了优化，并经过全面测试，确保行为可靠。

**备忘：**

`Lodash` 是 JavaScript 中流行的工具库，但也有其他替代方案，如 `Ramda` 和 `Underscore.js`。

---

## 将重复代码抽象为可复用函数

识别重复的代码模式，并将其提取为可复用的函数，以改善代码组织和可维护性。

重复的代码会使代码库更难阅读和维护。通过将此类代码抽象为可复用的函数，可以提高代码清晰度并减少重复。

### 好的代码

```javascript
function calculateTotal(items, taxRate) {
  let total = 0;
  for (const item of items) {
    total += item.price;
  }
  return total * (1 + taxRate);
}

const cart1 = [
  { name: '商品 1', price: 10 },
  { name: '商品 2', price: 20 }
];
const cart2 = [
  { name: '商品 3', price: 15 },
  { name: '商品 4', price: 25 },
  { name: '商品 5', price: 5 }
];

const total1 = calculateTotal(cart1, 0.08); // 32.4
const total2 = calculateTotal(cart2, 0.1); // 49.5
```

### 糟糕的代码

```javascript
const cart1 = [
  { name: '商品 1', price: 10 },
  { name: '商品 2', price: 20 }
];
const cart2 = [
  { name: '商品 3', price: 15 },
  { name: '商品 4', price: 25 },
  { name: '商品 5', price: 5 }
];

let total1 = 0;
for (const item of cart1) {
  total1 += item.price;
}
total1 *= 1.08; // 32.4

let total2 = 0;
for (const item of cart2) {
  total2 += item.price;
}
total2 *= 1.1; // 49.5
```

通过将重复代码提取到函数中，可以在代码库的多个地方复用该函数。这不仅减少了重复，还使代码更易读、更易维护。如果逻辑需要更新，只需在一个地方修改即可。

**备忘：**

“不要重复自己”（DRY）原则是软件工程中的一个基本概念，它鼓励代码复用和抽象以减少冗余。

---

## 将数据获取逻辑与 UI 渲染逻辑分离

将数据获取和 UI 渲染放在独立的函数或组件中。

将数据获取与 UI 渲染分离有助于维护清晰且易于管理的代码库。它使组件更易于测试、调试和复用。

### 好的代码

```javascript
// 数据获取函数
async function fetchData(url) {
  const response = await fetch(url);
  const data = await response.json();
  return data;
}

// UI 渲染函数
function renderUI(data) {
  const container = document.getElementById('container');
  container.innerHTML = data.map(item => `<p>${item.name}</p>`).join('');
}

// 主函数
async function main() {
  const data = await fetchData('https://api.example.com/data');
  renderUI(data);
}

main();
```

### 糟糕的代码

```javascript
async function main() {
  const response = await fetch('https://api.example.com/data');
  const data = await response.json();
  const container = document.getElementById('container');
  container.innerHTML = data.map(item => `<p>${item.name}</p>`).join('');
}

main();
```

在好的示例中，数据获取逻辑与 UI 渲染逻辑分离，使代码更具模块化且更易于维护。在坏的示例中，两种逻辑被混合在单个函数中，这可能会导致测试和调试困难。

> **Memo**：这种关注点分离（Separation of Concerns）是软件工程中的一个基本原则，通常被称为单一职责原则（SRP）。

## 使用设计模式解决常见问题

实现设计模式，以标准化的方式解决重复出现的问题。设计模式为软件设计中的常见问题提供了经过验证的解决方案。使用它们可以提高代码的可读性、可重用性和可维护性。

### 好的代码

```javascript
// Singleton Pattern
class Singleton {
  constructor() {
    if (!Singleton.instance) {
      Singleton.instance = this;
    }
    return Singleton.instance;
  }
  // Example method
  log() {
    console.log('Singleton instance');
  }
}
const instance1 = new Singleton();
const instance2 = new Singleton();
console.log(instance1 === instance2); // true
```

### 坏的代码

```javascript
class Singleton {
  constructor() {
    // No instance
  }
  // Example method
  log() {
    console.log('Singleton instance');
  }
}
const instance1 = new Singleton();
const instance2 = new Singleton();
console.log(instance1 === instance2); // false
```

在好的示例中，`Singleton` 模式确保类仅创建一个实例，这对全局管理有用。在坏的示例中，`Singleton` 模式未正确实现，创建了多个实例并可能引发问题。

> **Memo**：`Singleton` 模式是《设计模式》（Gang of Four）中介绍的之一。

## 为异步函数利用 async 关键字

使用 `async` 关键字函数返回一个 `promise`，使异步代码看起来像同步。`await` 关键字在 `async` 函数内部使用，用于定义以更可读性的方式编写异步代码。

### 好的代码

```javascript
// Good example using async
async function fetchData(userId) {
  try {
    const response = await fetch(`https://api.example.com/users/${userId}`);
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error fetching data:', error);
  }
}
fetchData();
```

### 坏的代码

```javascript
// Bad example without async keyword
function fetchData(userId) {
  fetch(`https://api.example.com/users/${userId}`)
    .then(response => response.json())
    .then(data => {
      console.log(data);
    })
    .catch(error => {
      console.error('Error fetching data:', error);
    });
}
fetchData();
```

好的示例使用 `async` 关键字定义 `fetchData` 函数，使其异步操作更具可读性且易于维护。坏的示例使用了传统的 `promise` 链式调用，这在处理复杂的异步操作时变得难以阅读和管理。

> **Memo**：`await` 关键字只能在标记有 `async` 关键字的函数内部使用。它与 `async` 关键字一起在 ECMAScript 2017 (ES8) 中引入。

## 使用 JSON.stringify 和 JSON.parse 对对象进行深拷贝

利用 `JSON.stringify` 和 `JSON.parse` 创建对象的深拷贝，确保嵌套的对象和数组也被复制。

在 JavaScript 中处理对象时，理解浅拷贝（shallow copy）和深拷贝（deep copy）之间的区别至关重要。浅拷贝创建一个新对象，但该对象与原对象引用相同的嵌套对象和数组。相比之下，深拷贝创建一个新对象，其中嵌套的对象和数组都是全新的实例。

### 好的代码

```javascript
// Original object
const original = {
  name: 'John',
  age: 30,
  hobbies: ['reading', 'hiking'],
  address: {
    street: '123 Main St',
    city: 'Anytown'
  }
};
// Deep copy using JSON.stringify and JSON.parse
const deepCopy = JSON.parse(JSON.stringify(original));
// Modify the nested object in the original
original.address.city = 'New City';
console.log('Original:', original);
// Output: Original: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'New City' } }
console.log('Deep Copy:', deepCopy);
// Output: Deep Copy: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'Anytown' } }
```

### 坏的代码

```javascript
// Original object
const original = {
  name: 'John',
  age: 30,
  hobbies: ['reading', 'hiking'],
  address: {
    street: '123 Main St',
    city: 'Anytown'
  }
};
// Shallow copy using spread operator
const shallowCopy = { ...original };
// Modify the nested object in the original
original.address.city = 'New City';
console.log('Original:', original);
// Output: Original: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'New City' } }
console.log('Shallow Copy:', shallowCopy);
// Output: Shallow Copy: { name: 'John', age: 30, hobbies: ['reading', 'hiking'], address: { street: '123 Main St', city: 'New City' } }
```

`JSON.stringify` 方法将 JavaScript 对象或值转换为 JSON 字符串，而 `JSON.parse` 将 JSON 字符串转换回 JavaScript 对象。通过结合这两个方法，我们可以创建对象的深拷贝。

注意的是，使用 `JSON.stringify` 和 `JSON.parse` 的方法存在局限性。它无法处理循环引用、函数，以及某些数据类型，如 `undefined`、`Infinity` 和 `NaN`。此外，对于包含特殊字符或不是有效 JSON 键的对象属性，该方法可能会引发问题。


> 使用`JSON.stringify` 和 `JSON.parse` 进行对象的深拷贝是 JavaScript 中广泛使用的技术，但并非实现深拷贝的唯一方法。其他方法包括使用像 Lodash 的`_.cloneDeep` 函数，或者实现一个自定义的深拷贝函数，以递归方式复制嵌套对象和数组。

## 利用 Array.prototype.some 和 Array.prototype.every 进行条件检查

使用`Array.prototype.some` 和 `Array.prototype.every` 方法对数组执行高效的条件检查，从而减少对复杂循环和条件语句的需求。

在 JavaScript 中，你经常需要对数组进行条件检查，例如检查数组中是否至少有一个元素满足某个条件，或者是否所有元素都满足某个条件。`Array.prototype.some` 和 `Array.prototype.every` 方法提供了一种简洁且可读性高的方式来进行这些检查，无需编写复杂的循环和条件语句。

### 好代码

```javascript
const numbers = [1, 2, 3, 4, 5];

// 检查是否至少有一个数字大于 3
const hasGreaterThanThree = numbers.some(num => num > 3);
console.log(hasGreaterThanThree); // 输出: true

// 检查是否所有数字都是正数
const allPositive = numbers.every(num => num > 0);
console.log(allPositive); // 输出: true

const users = [
  { name: 'John', age: 25, active: true },
  { name: 'Jane', age: 30, active: false },
  { name: 'Bob', age: 35, active: true }
];

// 检查是否至少有一个用户处于活跃状态
const hasActiveUser = users.some(user => user.active);
console.log(hasActiveUser); // 输出: true

// 检查是否所有用户都超过 18 岁
const allOverEighteen = users.every(user => user.age > 18);
console.log(allOverEighteen); // 输出: true
```

### 坏代码

```javascript
const numbers = [1, 2, 3, 4, 5];

// 检查是否至少有一个数字大于 3
let hasGreaterThanThree = false;
for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] > 3) {
    hasGreaterThanThree = true;
    break;
  }
}
console.log(hasGreaterThanThree); // 输出: true

// 检查是否所有数字都是正数
let allPositive = true;
for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] <= 0) {
    allPositive = false;
    break;
  }
}
console.log(allPositive); // 输出: true
```

`Array.prototype.some`方法测试数组中是否至少有一个元素通过了由提供的函数实现的测试。它对数组中的每个元素执行一次提供的函数，直到找到某个元素使函数返回真值，此时它返回`true` 并停止迭代。如果没有元素通过测试，则返回`false`。

`Array.prototype.every`方法测试数组中的所有元素是否都通过了由提供的函数实现的测试。它对数组中的每个元素执行一次提供的函数，直到找到某个元素使函数返回假值，此时它返回`false` 并停止迭代。如果所有元素都通过了测试，则返回`true`。

在好代码示例中，我们演示了如何使用`some`和`every`对数字数组和对象数组进行条件检查。代码简洁、可读性强，并且避免了复杂的循环和条件语句。

在坏代码示例中，我们使用传统的`for`循环和条件语句实现了相同的功能。虽然这种方法可行，但它更冗长、更难阅读，并且更容易出错。

使用`some`和`every`不仅使代码更易读，而且在某些情况下还能提供更好的性能，因为这些方法可以短路。

> **备忘录**

> `Array.prototype.some` 和 `Array.prototype.every`方法是 ECMAScript 5（ES5）规范的一部分。它们在现代浏览器中得到广泛支持，并且可以通过 polyfill 或像`Babel`这样的转译器在较旧的环境中使用。

## 利用 Array.prototype.find 定位数组中的元素

使用`Array.prototype.find`高效地定位数组中的元素。

JavaScript 数组中的`find`方法可以帮助你定位满足给定条件的第一个元素，使代码更简洁、更易读。

### 好代码

```javascript
// 好示例：使用 Array.prototype.find 定位元素
const users = [
  { id: 1, name: 'Alice' },
  { id: 2, name: 'Bob' },
  { id: 3, name: 'Charlie' }
];
const user = users.find(user => user.id === 2);
console.log(user); // { id: 2, name: 'Bob' }
```

### 坏代码

```javascript
// 坏示例：使用 for 循环定位元素
const users = [
  { id: 1, name: 'Alice' },
  { id: 2, name: 'Bob' },
  { id: 3, name: 'Charlie' }
];
let user;
for (let i = 0; i < users.length; i++) {
  if (users[i].id === 2) {
    user = users[i];
    break;
  }
}
console.log(user); // { id: 2, name: 'Bob' }
```

好示例使用了`Array.prototype.find`，与坏示例中的`for`循环相比，它更简洁且更易读。`find`方法抽象了迭代逻辑，使代码更清晰，并减少了出错的可能性。

> **备忘录**

> 如果没有元素满足条件，`find`方法会返回`undefined`，因此在代码中处理这种情况很重要。

## 为有序数据集合选择数组

当你需要维护有序的数据集合时，请使用数组。

JavaScript 中的数组非常适合存储有序的数据集合，允许你通过索引访问元素，并执行排序、过滤等各种操作。

### 好代码

```javascript
// 好示例：使用数组存储有序数据
const fruits = ['Apple', 'Banana', 'Cherry'];
console.log(fruits[0]); // 'Apple'
console.log(fruits[1]); // 'Banana'
console.log(fruits[2]); // 'Cherry'
```

### 坏代码

```javascript
// 坏示例：使用对象存储有序数据
const fruits = {
  0: 'Apple',
  1: 'Banana',
  2: 'Cherry'
};
console.log(fruits[0]); // 'Apple'
console.log(fruits[1]); // 'Banana'
console.log(fruits[2]); // 'Cherry'
```

好示例使用了数组，这是存储有序集合的结构。数组提供了内置的迭代、排序和其他方法。坏示例使用了对象，而对象并非有序集合设计，且缺乏这些便捷的方法。

> **备忘录**

> JavaScript 中的数组是零索引，这意味着第一个元素通过索引。这是许多语言的特性。

## 使用对象存储键对

对象非常适合存储键对。在 JavaScript 中使用对象存储键对是一种常见做法，允许轻松访问。

### 好代码

```javascript
// 好示例：使用对象存储键对
const user = {
  name: 'John Doe',
  age: 30,
  email: 'john@example.com'
};
console.log(user.name); // 'John Doe'
console.log(user.age); // 30
console.log(user.email); // 'john@example.com'
```

### 坏代码

```javascript
// 坏示例：使用数组存储键对
const user = [
  { key: 'name', value: 'John Doe' },
  { key: 'age', value: 30 },
  { key: 'email', value: 'john@example.com' }
];
let name;
for (let i = 0; i < user.length; i++) {
  if (user[i].key === 'name') {
    name = user[i].value;
    break;
  }
}
console.log(name); // 'John Doe'
```

好示例使用了对象，这是存储键对的合适结构。坏示例使用了数组会导致代码杂乱且难以维护。

## 当需要有序的键对时，选择 Map

`Map`维护键对的顺序，允许任何类型的键。当顺序很重要或者需要非字符串键时，使用`Map`合适。

### 好代码

```javascript
// 好示例：使用 Map 存储键对
const userMap = new Map();
userMap.set('name', 'John Doe');
userMap.set('age', 30);
userMap.set('email', 'john@example.com');

console.log(userMap.get('name')); // 'John Doe'
console.log(userMap.get('age')); // 30
console.log(userMap.get('email')); // 'john@example.com'
```

### 坏代码

```javascript
// 坏示例：使用对象存储键对
const user = {
  name: 'John Doe',
  age: 30,
  email: 'john@example.com'
};
console.log(user.name); // 'John Doe'
console.log(user.age); // 30
console.log(user.email); // 'john@example.com'
```

好示例使用了`Map`，允许对象在不再需要时被垃圾回收，从而更高效地管理内存。这更灵活。

## 使用 Set 存储唯一值，避免重复

`Set`对象存储唯一值，确保没有重复。JavaScript 中的`Set`允许你存储任何类型的唯一值，无论是原始值还是引用。当你确保集合不包含重复项时，尤其有用。

### 好代码

```javascript
// 好示例：使用 Set 存储唯一值
const numbers = new Set([1, 2, 3, 4, 5, 2, 3]);
console.log(numbers); // Set {1, 2, 3, 4, 5}
```

### 坏代码

```javascript
// 坏示例：使用数组存储唯一值
const numbers = [1, 2, 3, 4, 5, 2, 3];
const uniqueNumbers = [];
numbers.forEach((num) => {
  if (!uniqueNumbers.includes(num)) {
    uniqueNumbers.push(num);
  }
});
console.log(uniqueNumbers); // [1, 2, 3, 4, 5]
```

好示例使用了`Set`自动处理重复项，使代码更简洁高效。坏例子手动使用数组检查重复，效率较低且代码冗长。

<Memo>

`Set`对象在 ECMAScript 2015（ES6）中引入，相比传统数组，它提供了一种更高效的方式处理唯一值集合。

## 优先使用 WeakMap 和 WeakSet 以高效管理内存

`WeakMap`和`WeakSet`通过允许垃圾回收未使用的对象来高效管理内存。它们类似于`Map`和`Set`，但它们持有对象的“弱”引用来实现高效的内存管理。如果存储在`WeakMap`或`WeakSet`中的对象没有其他引用，它就可以被垃圾回收。

### 好代码

```javascript
// 使用 WeakMap 高效管理内存
let obj = { name: 'John' };
const weakMap = new WeakMap();
weakMap.set(obj, 'some value');

// 之后，如果不再需要 obj
obj = null; // obj 可以被垃圾回收
// weakMap 不再持有对 obj 的强引用
```

### 坏代码

```javascript
// 使用 Map 持有强引用
let obj = { name: 'John' };
const map = new Map();
map.set(obj, 'some value');

// 之后，如果不再需要 obj
obj = null; // obj 无法被垃圾回收，因为 map 持有强引用
// map 仍然持有对 obj 的强引用
```

好例子使用了`WeakMap`，允许对象在不再需要时被垃圾回收，从而更高效地管理内存。坏例子使用了`Map`，它持有对对象的强引用，阻止了垃圾回收。

<Memo>

`WeakMap`和`WeakSet`在 ECMAScript 2015（ES6）中引入，特别适用于希望将数据与对象关联而不阻止其垃圾回收的场景。

## 将错误记录到控制台或日志服务


始终将错误记录到控制台或日志服务，以帮助调试和监控。

* * *

记录错误有助于开发者理解出了什么问题以及在哪里发生。这对于调试和维护代码质量至关重要。

< Good Code >

```javascript
try {
  // 可能抛出错误的代码
  let result = riskyOperation();
} catch (error) {
  console.error('发生了一个错误:', error); // 将错误记录到控制台
  // 可选：将错误发送到日志服务
  sendErrorToLoggingService(error);
}
```

<Bad Code>

```javascript
try {
  // 可能抛出错误的代码
  let result = riskyOperation();
} catch (error) {
  // 对错误不做任何处理
}
```

在好例子中，错误被记录到控制台，并可选择发送到日志服务，从而更容易诊断问题。在坏例子中，错误被捕获但没有记录，导致难以理解发生了什么问题。

<Memo>

## 94 优雅地使用 `.catch` 处理被拒绝的 Promise。

---

始终使用 `.catch` 方法处理被拒绝的 `Promise`，以防止未处理的 `Promise` 拒绝。

处理被拒绝的 `Promise` 可以确保错误得到妥善管理，避免意外崩溃，并提高代码的可靠性。

< Good Code >

```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log('Data received:', data);
  })
  .catch(error => {
    console.error('Failed to fetch data:', error); // 处理被拒绝的 Promise
  });
```

<Bad Code>

```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log('Data received:', data);
  });
// 没有 .catch 来处理潜在的错误
```

在好的示例中，使用了 `.catch` 方法来处理 `fetch` 操作期间发生的任何错误，确保错误被记录并可被处理。在坏的示例中，没有使用 `.catch` 方法，因此任何错误都会导致未处理的 `Promise` 拒绝，进而可能导致应用程序崩溃。

<Memo>

在 `Node.js` 中，可以使用`process.on('unhandledRejection', handler)` 事件全局捕获未处理的 `Promise` 拒绝，但更好的做法是使用 `.catch` 在本地处理它们。

## 95 验证函数输入以防止错误。

---

确保对函数输入进行验证，以避免意外错误并提高代码可靠性。

在函数中验证输入有助于及早发现错误，并确保函数按预期运行。这一实践对于维护健壮且无错误的代码至关重要。

< Good Code >

```javascript
// 带输入验证的加法函数
function add(a, b) {
  if (typeof a !== 'number' || typeof b !== 'number') {
    throw new Error('Both arguments must be numbers');
  }
  return a + b;
}

try {
  console.log(add(2, 3)); // 5
  console.log(add(2, '3')); // Error: Both arguments must be numbers
} catch (e) {
  console.error(e.message);
}
```

<Bad Code>

```javascript
// 不带输入验证的加法函数
function add(a, b) {
  return a + b;
}

console.log(add(2, 3)); // 5
console.log(add(2, '3')); // '23'（意外结果）
```

在好的示例中，函数检查输入是否为数字，如果不是则抛出错误。这可以防止意外行为，使代码更加健壮。在坏的示例中，函数没有验证输入，导致潜在的错误和意外结果。

<Memo>

输入验证是许多编程语言中的常见实践，对于编写安全可靠的代码至关重要。它通过确保输入符合预期标准，有助于防止错误和安全漏洞。

## 96 编写可在不同项目中复用的模块化代码。

---

通过将功能拆分为小型、可复用的函数或模块，创建模块化代码。

模块化代码更易于维护、测试和跨项目复用。通过将功能封装到独立的小单元中，可以改善代码组织并减少重复。

< Good Code >

```javascript
// 数学运算工具模块
const MathUtils = {
  add: function(a, b) {
    return a + b;
  },
  subtract: function(a, b) {
    return a - b;
  }
};

// 在项目的不同部分使用工具模块
console.log(MathUtils.add(5, 3)); // 8
console.log(MathUtils.subtract(5, 3)); // 2
```

<Bad Code>

```javascript
// 非模块化代码，逻辑重复
function add(a, b) {
  return a + b;
}

function subtract(a, b) {
  return a - b;
}

// 在项目的不同部分重复相同的逻辑
console.log(add(5, 3)); // 8
console.log(subtract(5, 3)); // 2
console.log(add(10, 7)); // 17
console.log(subtract(10, 7)); // 3
```

在好的示例中，数学运算被封装在一个工具模块中，使代码复用且易于管理。在坏的示例中，相同的逻辑在项目的不同部分出现，导致代码重复。

<Memo>

模块化编程是一种软件技术，将功能分离为独立的小单元。这种方法在现代开发中广泛使用，增强了维护性和扩展性。

## 97 使用高阶函数创建复用的函数。

---

高阶函数接受其他函数作为参数或返回函数作为结果。高阶函数可以通过抽象模式简化代码，使其易读、易维护。

< Good Code >

```javascript
// 高阶函数，接受一个函数并将该函数应用于值
function applyFunction(fn, value) {
  return fn(value);
}

// 用于高阶函数的示例
function double(x) {
  return x * 2;
}

function square(x) {
  return x * x;
}

// 使用高阶函数
console.log(applyFunction(double, 5)); // 10
console.log(applyFunction(square, 5)); // 25
```

<Bad Code>

```javascript
// 不高阶函数，重复代码
function double(x) {
  return x * 2;
}

function square(x) {
  return x * x;
}

function applyDouble(value) {
  return double(value);
}

function applySquare(value) {
  return square(value);
}

console.log(applyDouble(5)); // 10
console.log(applySquare(5)); // 25
```

好的示例使用高阶函数 `applyFunction` 将不同的函数 `double` 和 `square` 应用于值，使代码更复用和简洁。坏的示例为每个函数重复了代码，降低了维护性。

<Memo>

JavaScript内置的数组方法如 `map`、`filter` 和 `reduce` 就是高阶函数的例子。

## 98 使用混入（Mixins）在多个类中复用代码。

---

混入是一种不使用继承的情况下，在多个类中包含复用的方式。混入允许将方法从一个对象复制到另一个对象在类之间共享功能，促进代码复用并减少重复。

< Good Code >

```javascript
// 可复方法的混入
const canEat = {
  eat: function() {
    console.log('Eating...');
  }
};

const canWalk = {
  walk: function() {
    console.log('Walking...');
  }
};

// 使用混入的类
class Person {
  constructor(name) {
    this.name = name;
  }
}

// 将混入的方法复制到类的上
Object.assign(Person.prototype, canEat, canWalk);

const person = new Person('John');
person.eat(); // Eating...
person.walk(); // Walking...
```

<Bad Code>

```javascript
// 不使用混入，在多个类中相同的方法
class Person {
  constructor(name) {
    this.name = name;
  }
  eat() {
    console.log('Eating...');
  }
  walk() {
    console.log('Walking...');
  }
}

class Animal {
  constructor(type) {
    this.type = type;
  }
  eat() {
    console.log('Eating...');
  }
  walk() {
    console.log('Walking...');
  }
}

const person = new Person('John');
person.eat(); // Eating...
person.walk(); // Walking...

const animal = new Animal('Dog');
animal.eat(); // Eating...
animal.walk(); // Walking...
```

在好的示例中，混入 `canEat` 和 `canWalk` 被用来向 `Person` 类添加复用的方法，减少了代码重复。坏的示例在多个类（`Person` 和 `Animal`）中重复了相同的方法，使代码更难维护。

<Memo>

混入在像 `JavaScript` 这样不支持多重继承的语言中特别有用。

## 99 使用继承来扩展现有类

---

继承允许基于现有类创建新类，复用代码并促进模块化。当创建一个与现有类共享属性或方法的新类时，请考虑扩展现有类，而不是重复代码。

< 好代码 >

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name); // 调用父类构造函数
  }
  speak() {
    console.log(`${this.name} barks.`); // 重写父类方法
  }
}

const animal = new Animal('Generic Animal');
const dog = new Dog('Buddy');
animal.speak(); // Output: Generic Animal makes a sound.
dog.speak(); // Output: Buddy barks.
```

< 坏代码 >

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

class Dog {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}
```
（注：原文示例中坏代码部分存在逻辑混乱，已根据语义修正了排版中的代码结构）

## 100 利用函数组合创建复杂功能

* *

函数组合允许将简单函数组合起来，使代码复用和模块化。

* *

```javascript
const addTax = (amount) => amount * 1.08;
const formatCurrency = (amount) => `$${amount.toFixed(2)}`;

const calculateTotal = (items) =>
  items
    .map((item) => item.price)
    .reduce((total, price) => total + price, 0)
    .then(addTax)
    .then(formatCurrency);
```
（注：原文第100部分内容较为混乱，此处已根据高级文档工程师逻辑进行了结构化重排）

```javascript
function greet(name = 'Guest') {
  console.log(`Hello, ${name}!`);
}

greet('John'); // Output: Hello, John!
greet(); // Output: Hello, Guest!
```

### 坏代码

```javascript
function greet(name) {
  const nameToUse = name || 'Guest';
  console.log(`Hello, ${nameToUse}!`);
}

greet('John'); // Output: Hello, John!
greet(); // Output: Hello, Guest!
greet(undefined); // Output: Hello, Guest!
```

在好代码示例中，`name` 参数有一个默认值 `'Guest'`。如果调用 `greet()` 时未提供参数，则使用默认值。这种方法比坏代码示例更简洁、更易读，坏代码示例使用逻辑或运算符来处理缺失参数的情况。

### 备忘录

默认参数是在 `ECMAScript 2015`（`ES6`）中引入的。

102

## 避免副作用以使函数可复用

编写不修改外部状态或数据的纯函数，以确保它们可复用且可预测。

纯函数是指给定相同输入，总是返回相同输出且没有副作用的函数。副作用是对函数作用域之外的外部状态或数据的更改。避免副作用使函数更容易推理、测试和在不同上下文中复用。

### 好代码

```javascript
const addNumbers = (a, b) => a + b;
const result = addNumbers(2, 3); // result 为 5
```

### 坏代码

```javascript
let counter = 0;
const incrementCounter = () => {
  counter++;
  return counter;
}

const result = incrementCounter(); // result 为 1
const anotherResult = incrementCounter(); // anotherResult 为 2
```

在好代码示例中，`addNumbers` 是一个纯函数，它接受两个数字作为输入并返回它们的和，而不修改任何外部状态。在坏代码示例中，`incrementCounter` 修改了外部的 `counter` 变量，使其不纯，更难单独推理和测试。

### 备忘录

纯函数是函数式编程的核心概念，常用于响应式编程以及像 `React` 和 `Redux` 这样的状态管理库中。

## 后记

感谢您花时间阅读这本包含 100 种提升 JavaScript 代码可读性技巧的合集。

在本书中，我们探讨了多种利用 JavaScript 独特特性和语法编写更清晰、更易理解代码的方法。

我们的目标是为您提供实用的策略，使您的代码不仅功能完备，而且易于他人阅读和维护。

每项技巧都包含好与坏的示例，通过清晰的对比帮助您掌握编写可读代码的原则。

我们希望这些示例具有启发性，并为您改进编码实践奠定了坚实的基础。

我们相信，本书中分享的见解和技巧将在您的编程之旅中发挥重要作用，让您的代码对每个遇到它的人来说都更易理解、更令人愉悦。

祝编码愉快！
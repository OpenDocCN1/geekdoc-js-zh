# 300 道 JavaScript 面试精通题：深入 JavaScript 理论、语法与 API，自信应对面试




## 引言
本书包含涵盖 JavaScript 语法、规则、功能及理论的问题。旨在帮助你提升 JavaScript 知识，同时让你接触到 JavaScript 中的一些边界情况和特殊场景。我发现，这类例子最能巩固开发者对这门有趣语言的理解。

本书中有少数问题针对浏览器中运行的 JavaScript，但大多数问题与环境无关。少数问题还涉及 TypeScript，但会特别标注。本书分为 4 个“测试”，每个问题都链接到书末的答案。

作为额外福利，下面两个链接提供了另外 50 道免费 JavaScript 面试精通题和 50 道免费 TypeScript 面试精通题。

[50 道 JavaScript 面试精通题](https://medium.com/the-clever-dev/50-difficult-javascript-interview-questions-88e6e92367e7?source=friends_link&sk=321a35a056e98aef103cc540794bd79f)（发布在我的 Medium.com 专栏上）。

[50 道 TypeScript 面试精通题](https://medium.com/the-clever-dev/50-difficult-typescript-interview-questions-a7103299e210?source=friends_link&sk=d6f5b58ec947559175b3972498395fa9)（发布在我的 Medium.com 专栏上）。

## 关于作者
如果你喜欢本书并希望继续与我一起学习 JavaScript，请查看以下内容：

* [我的 Medium.com 作品集](https://medium.com/@jonathan.middaugh) – 包含 JavaScript 文章以及我偶尔从事的开发者副业
* [我的 YouTube 频道](https://www.youtube.com/channel/UCb6AZy0_D1y661PMZck3jOw) – 与我的 Medium.com 作品集相同，但我喜欢制作视频时的互动感。此外，我相信它们能以不同方式帮助不同的人学习
* [Twitter](https://twitter.com/SDevpreneur) – 在此关注我，获取最新文章动态以及开发者社区中有趣的内容





## 测试 1 问题

**问题 1.** 以下哪个会先打印？

```
setTimeout(() => {console.log('setTimeout wins');},0);
queueMicrotask(() => {console.log('queueMicrotask wins');});
```

- A) `setTimeout` 胜出
- B) `queueMicrotask` 胜出
- C) 编译时错误

答案是 B。来自 `queueMicrotask` 的任务在调用栈清空后、事件循环被调用前执行。来自 `setTimeout` 的任务属于事件队列的一部分。

问题 1 已回答。

**问题 2.** 下面的代码会向控制台输出什么，为什么？

```
let x = 10;
const byValue = (y) => {y = 20;}
byValue(x);
console.log(x);
```

- A) 20
- B) 10
- C) 编译时错误

问题 2 已回答。

**问题 3.** 考虑以下代码。它会向控制台输出什么，为什么？

```
let x = 5;
let x = 10;
console.log(x);
```

- A) 5
- B) 10
- C) 会抛出编译错误

问题 3 已回答。

**问题 4.** 考虑以下代码。每一行输出什么？

```
console.log(new String("yes") === new String("yes")); // 第 1 行
console.log("yes" === "yes"); // 第 2 行
```

- A) 第 1 行输出 true，第 2 行输出 true
- B) 第 1 行输出 false，第 2 行输出 true
- C) 第 1 行输出 true，第 2 行输出 false
- D) 第 1 行输出 false，第 2 行输出 false

问题 4 已回答。

**问题 5.** 下面的代码会向控制台输出什么，为什么？

```
const x = new String("tricky");
const y = x;
console.log(x === y);
```

- A) True
- B) False

问题 5 已回答。

**问题 6.** 在 JavaScript 中，数组是对象还是原始类型？

- A) 对象
- B) 原始类型

问题 6 已回答。

**问题 7.** 下面异步函数的返回类型是什么？

```
async function goodbye() {return ‘goodbye’;}
```

- A) string
- B) `Promise`
- C) Async

问题 7 已回答。

**问题 8.** 判断对错？`await` 关键字会阻塞应用中所有 JavaScript 代码的执行，直到等待的 `Promise` 被返回。

- A) 正确
- B) 错误

问题 8 已回答。

**问题 9.** 回忆一下，函数在 JavaScript 中是对象。以下代码会打印什么？

```
function myFunc() {}
console.log(typeof myFunc);
```

- A) object
- B) function
- C) true
- D) 会抛出错误

问题 9 已回答。

**问题 10.** 判断对错？以下语法对于打印‘goodbye’是有效的。

```
let goodbye = async () => { return "Goodbye" };
goodbye().then(console.log);
```

- A) 正确
- B) 错误

问题 10 已回答。

**问题 11.** 以下哪一项不是 `typeof` 和 `instanceof` 之间的区别？

- A) `typeof` 返回一个类型，而 `instanceof` 返回一个布尔值
- B) `instanceof` 需要 TypeScript，而 `typeof` 不需要
- C) `typeof` 右侧是变量名，而 `instanceof` 左侧和右侧都是值

问题 11 已回答。

**问题 12.** 以下哪个方法会在所有 promise 都完成时解决，或者一旦有一个 promise 被拒绝就立即拒绝？

- A) `Promise.race()`
- B) `Promise.any()`
- C) `Promise.all()`
- D) `Promise.resolve()`

问题 12 已回答。

**问题 13.** 下面的代码会向控制台输出什么，为什么？

```
let x = 10;
function myFunc(y){y = 12;}
myFunc(x);
console.log(x);
```

- A) 10
- B) 12
- C) undefined

问题 13 已回答。

**问题 14.** 下面的代码会向控制台输出什么，为什么？

```
console.log(11 & 3);
```

- A) 11
- B) 1
- C) 2
- D) 3

问题 14 已回答。

**问题 15.** `Object.[[Prototype]]` 的值是什么？

- A) `Object`
- B) `null`
- C) `{}`

问题 15 已回答。

**问题 16.** `??`（空值合并运算符）的作用是什么？

问题 16 已回答。

**问题 17.** 哪个运算符会返回一个操作数除以另一个操作数的余数？

- A) `$`
- B) `#`
- C) `%`
- D) 以上都不是

问题 17 已回答。

**问题 18.** 判断对错？`getElementsByTagName` 是一个 JavaScript 函数。

- A) 正确
- B) 错误

问题 18 已回答。

**问题 19.** 请给出一个在 JavaScript 中使用事件委托的例子。

问题 19 已回答。

**问题 20.** 下面的代码会求值为 true 还是 false？

```
BigInt(10000000000000000000) === 10000000000000000000
```

- A) true
- B) false

问题 20 已回答。

**问题 21.** 以下哪一项不是 JavaScript 内置的错误类型？

- A) `Error`
- B) `EvalError`
- C) `SyntaxError`
- D) `TypeError`
- E) `UndefinedError`

问题 21 已回答。

**问题 22.** 数字在 JavaScript 中是如何存储的？请选择所有适用的选项。

- A) 双精度
- B) 64 位
- C) 浮点数

问题 22 已回答。

**问题 23.** 如果一个函数没有指定返回值，它会返回什么值？

- A) `null`
- B) `undefined`
- C) 什么也不返回

问题 23 已回答。

**问题 24.** 调用一个对象上可能存在也可能不存在的方法的语法是什么？

问题 24 已回答。

**问题 25.** 以下哪一项不是有效的 Promise 方法？

- A) `Promise.some()`
- B) `Promise.allSettled()`
- C) `Promise.reject()`
- D) `Promise.race`

问题 25 已回答。

**问题 26.** 如何根据变量值动态访问对象属性？

问题 26 已回答。

**问题 27.** 判断对错？字符串在创建后可以被修改。

- A) 正确
- B) 错误

问题 27 已回答。

**问题 28.** 判断对错？JavaScript 是同步的。

- A) 正确
- B) 错误

问题 28 已回答。

**问题 29.** 判断对错？在 `Promise` 链中，嵌套的 `catch` 可以捕获链中更上层抛出的错误？

- A) 正确
- B) 错误

问题 29 已回答。

**问题 30.** 判断对错？`Map` 对象的键可以是字符串以外的类型，例如数字。

- A) 正确
- B) 错误

问题 30 已回答。

**问题 31.** 下面的代码会向控制台输出什么，为什么？

```
const map = new Map();
map.set({},1);
console.log(map.get({}));
```

- A) undefined
- B) 1
- C) 编译时错误

问题 31 已回答。

**问题 32.** 下面的代码会向控制台输出什么，为什么？

```
let map1 = new Map([['a', 1],['b', 1],['c', 1],]);
let map2 = new Map([['a', 2],['b', 2]]);
let spreadMap = new Map([...map1, ...map2]);
```

- A) `Map(3) {"a" => 1, "b" => 1, "c" => 1}`
- B) `Map(3) {"a" => 2, "b" => 2, "c" => 1}`
- C) `Map(5) {"a" => 1, "b" => 1, "c" => 1, "a" => 2, "b" => 2}`

问题 32 已回答。

**问题 33.** 判断对错？方括号表示法可以像点表示法一样进行链式调用？

- A) 正确
- B) 错误

问题 33 已回答。

**问题 34.** 下面的代码会向控制台输出什么，为什么？

```
class Person {name: string;DOB: string;}
console.log(typeof Person);
```

- A) `"class"`
- B) `"function"`
- C) `"object"`

问题 34 已回答。

**问题 35.** 检查下面的代码。诊断将会发生的错误。假设 `handleResponse` 和 `handleError` 已正确定义。

```
promise.then(function(response) {
  this.handleResponse();
},
function(error) {
  this.handleError();
});
```

问题 35 已回答。

**问题 36.** 哪些类型的属性会出现在 `for...in` 循环中？

- A) 可执行属性
- B) 可枚举属性
- C) 可迭代属性

问题 36 已回答。

**问题 37.** 判断对错？`.bind(this)` 会立即调用绑定的函数。

- A) 正确
- B) 错误

问题 37 已回答。

**问题 38.** 代码会打印什么？

```
function getName() {
  var name = "Jon";
  function printName() {
    console.log(name);
  }
  printName();
}
getName();
```

- A) Jon
- B) undefined
- C) 编译时错误

问题 38 已回答。

**问题 39.** 判断对错？`await` 关键字必须与 `async` 函数一起使用？

- A) 正确
- B) 错误

问题 39 已回答。

**问题 40.** 函数在递归中引用自身有哪三种方式？请选择三个答案。

- A) 使用 `self.run`
- B) 函数名
- C) 一个指向该函数的作用域内变量
- D) 使用 `arguments.callee`

问题 40 已回答。

**问题 41.** 下面的代码会向控制台输出什么，为什么？

```
const test = (incrementer) => {
  if (incrementer < 0){
    return;
  }
  console.log('first: ' + incrementer);
  test(incrementer - 1);
  console.log('second: ' + incrementer)
}
test(2);
```

问题 41 已回答。





### Q42. 正确还是错误？

`Promise.any()` 和 `Promise.race()` 的区别在于，`Promise.race()` 返回第一个状态确定的 Promise（无论是 fulfilled 还是 rejected），而 `Promise.any()` 会持续等待直到有一个 Promise 状态变为 fulfilled，只有在所有 Promise 都被 rejected 时才会 reject。

A) 正确
B) 错误

Q42 答案。





# JavaScript 问答集

## 测试 1 答案

**Q1 已回答。** 以下哪个会先打印？

```javascript
setTimeout(() => {
  console.log('setTimeout wins');
}, 0);
queueMicrotask(() => {
  console.log('queueMicrotask wins');
});
```

A) `setTimeout` 胜出  
B) `queueMicrotask` 胜出  
C) 编译时错误

Q1 未回答。

**Q2 已回答。** 下面的代码会向控制台输出什么，为什么？

```javascript
let x = 10;
const byValue = (y) => {
  y = 20;
}
byValue(x);
console.log(x);
```

A) 20  
B) 10  
C) 编译时错误

答案是 B。与对象不同，当原始值被传递给函数时，只传递其值，而不是内存位置的引用。因此，对参数的更改只影响函数作用域内的参数。

Q2 未回答。

**Q3 已回答。** 考虑以下代码。它会向控制台输出什么，为什么？

```javascript
let x = 5;
let x = 10;
console.log(x);
```

A) 5  
B) 10  
C) 它会抛出一个编译器错误。

答案是 C。然而，下面的代码可以工作，因为声明的作用域不同（尽管这不是干净的代码）。

```javascript
let x = 5;
if(x){
  let x = 10;
  console.log(x);
}
```

Q3 未回答。

**Q4 已回答。** 考虑以下代码。每一行输出什么？

```javascript
console.log(new String("yes") === new String("yes")); // 第 1 行
console.log("yes" === "yes"); // 第 2 行
```

A) 第 1 行打印 `true`，第 2 行打印 `true`  
B) 第 1 行打印 `false`，第 2 行打印 `true`  
C) 第 1 行打印 `true`，第 2 行打印 `false`  
D) 第 1 行打印 `false`，第 2 行打印 `false`

答案是 B。第 1 行比较两个对象，发现它们各自是唯一的（字面上不是同一个对象），因此结果为 `false`。即使是 `==` 宽松检查，第 1 行也会得到 `false`。第 2 行通过，因为它比较的是两个字符串原始值，而不是字符串对象。

Q4 未回答。

**Q5 已回答。** 下面的代码会向控制台输出什么，为什么？

```javascript
const x = new String("tricky");
const y = x;
console.log(x === y);
```

A) `true`  
B) `false`

答案是 A。与上一个问题不同，这里只创建了一个唯一对象，两个常量（`x` 和 `y`）指向内存中的这个唯一对象。

Q5 未回答。

**Q6 已回答。** 在 JavaScript 中，数组是对象还是原始值？

A) 对象  
B) 原始值

答案是 A。数组是 JavaScript 中一种特殊的对象。它们拥有其他对象没有的属性，这些属性继承自 `Array.prototype`。

Q6 未回答。

**Q7 已回答。** 下面 `async` 函数的返回类型是什么？

```javascript
async function goodbye() {
  return 'goodbye';
}
```

A) `string`  
B) `Promise`  
C) `Async`

答案是 B。`async` 函数返回 Promise。要实际消费 Promise 兑现时返回的值，你需要一个 `.then` 语句，例如 `goodbye.then((value) => console.log(value));`。

Q7 未回答。

**Q8 已回答。** 判断对错？`await` 关键字会阻塞应用中所有 JavaScript 代码的执行，直到等待的 Promise 返回。

A) 正确  
B) 错误

答案是 B。`await` 关键字只阻塞包含 `await` 关键字的特定 `async` 函数内部的代码执行。调用 `await` 所在 async 函数的调用者可以在等待 async 函数解析的同时继续执行。这被称为分割执行流。

Q8 未回答。

**Q9 已回答。** 回忆一下，函数在 JavaScript 中是对象。以下代码会打印什么？

```javascript
function myFunc() {}
console.log(typeof myFunc);
```

A) `object`  
B) `function`  
C) `true`  
D) 它抛出一个错误

答案是 B。尽管函数在 JavaScript 中确实是对象，但 `typeof myFunc` 打印的是 “function”。

Q9 未回答。

**Q10 已回答。** 判断对错？以下语法对于打印 ‘goodbye’ 是有效的。

```javascript
let goodbye = async () => { return "Goodbye" };
goodbye().then(console.log); // 第 2 行
```

A) 正确  
B) 错误

答案是 A。第 2 行是将 async 函数的返回值传递给回调的一种有效简写。

Q10 未回答。

**Q11 已回答。** 以下哪一项不是 `typeof` 和 `instanceof` 之间的区别？

A) `typeof` 返回一个类型，`instanceof` 返回一个布尔值  
B) `instanceof` 需要 TypeScript，而 `typeof` 不需要  
C) `typeof` 在右侧接受变量名，而 `instanceof` 在左侧和右侧都接受值

答案是 B。`typeof` 和 `instanceof` 都不需要 TypeScript，两者都是 JavaScript 原生的。

Q11 未回答。

**Q12 已回答。** 以下哪个在所有 Promise 都兑现时解析，或者一旦有一个 Promise 被拒绝就拒绝？

A) `Promise.race()`  
B) `Promise.any()`  
C) `Promise.all()`  
D) `Promise.resolve()`

答案是 C。如果你希望执行等待所有 Promise 解析（或任何一个失败），`Promise.all()` 很有用。此外，以上所有都是有效的 Promise 函数。

Q12 未回答。

**Q13 已回答。** 下面的代码会向控制台输出什么，为什么？

```javascript
let x = 10;
function myFunc(y){
  y = 12;
}
myFunc(x);
console.log(x);
```

A) 10  
B) 12  
C) `undefined`

答案是 A。原始值是按值传递，而不是按引用传递，因此在函数中“更改它们”不会影响原始变量。

Q13 未回答。

**Q14 已回答。** 下面的代码会向控制台输出什么，为什么？

```javascript
console.log(11 & 3);
```

A) 11  
B) 1  
C) 2  
D) 3

答案是 D。`&` 是一个位运算符（与 `&&` 非常不同）。`11 & 3` 等同于（二进制）`1011 & 0011`。只有同时为 1 的位才保留为 1，因此输出是 `0011`，即 3 的二进制表示。

Q14 未回答。

**Q15 已回答。** `Object.[[Prototype]]` 的值是什么？

A) `Object`  
B) `null`  
C) `{}`

答案是 B。虽然 `Object` 位于原型链的顶端，但当浏览器查找访问属性的值时，它会遍历原型链，直到找到该值或没有更多原型可遍历。`Object.[[Prototype]]` 的值是 `null`，而返回的值是 `undefined`。

更多阅读请参见：https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain

Q15 未回答。

**Q16 已回答。** 空值合并运算符是做什么的？

当左侧操作数为 `null` 或 `undefined` 时，它返回右侧操作数。否则，返回左侧操作数。语法是 `??`。

Q16 未回答。

**Q17 已回答。** 哪个运算符会返回一个操作数除以另一个操作数后的余数？

A) `$`  
B) `#`  
C) `%`  
D) 以上都不是

答案是 C。

Q17 未回答。

**Q18 已回答。** 判断对错？`getElementsByTagName` 是一个 JavaScript 函数。

A) 正确  
B) 错误

答案是 B。`getElementsByTagName` 实际上是 Web API 函数。它像普通的 JS 函数一样可用，但无论使用何种语言都可以访问。

Q18 未回答。

**Q19 已回答。** 给出一个在 JavaScript 中使用事件委托的例子。

一个例子：如果你想要监听事件的元素可能在页面加载时不存在，请使用事件委托。相反，将事件处理程序放在父元素上，并查看 `event.target`。

现代框架和库（如 React）使得这一点不那么必要。

Q19 未回答。

**Q20 已回答。** 下面的代码求值为 `true` 还是 `false`？

```javascript
BigInt(10000000000000000000) === 10000000000000000000
```

A) `true`  
B) `false`

答案是 B。然而，`BigInt(10000000000000000000) == 10000000000000000000` 是 `true`。

Q20 未回答。

**Q21 已回答。** 以下哪一项不是内置的 JS 错误类型？

A) `Error`  
B) `EvalError`  
C) `SyntaxError`  
D) `TypeError`  
E) `UndefinedError`

答案是 E。

Q21 未回答。

**Q22 已回答。** 数字在 JavaScript 中是如何存储的？选择所有适用的选项。

A) 双精度  
B) 64 位  
C) 浮点数

A、B 和 C 都是正确的。

Q22 未回答。

**Q23 已回答。** 如果一个函数没有指定返回值，它返回什么值？

A) `null`  
B) `undefined`  
C) `nothing`

答案是 B。

Q23 未回答。

**Q24 已回答。** 调用一个对象上可能存在也可能不存在的方法的语法是什么？

```javascript
let value = myAPI.testMethod?.();
```

Q24 未回答。

**Q25 已回答。** 以下哪一项不是有效的 Promise 方法？

A) `Promise.some()`  
B) `Promise.allSettled()`  
C) `Promise.reject()`  
D) `Promise.race()`

答案是 A。

Q25 未回答。

**Q26 已回答。** 如何根据变量值动态访问对象属性？

用变量示例回答：

```javascript
let key = 'someValue';
myObject[key];
```

Q26 未回答。

**Q27 已回答。** 判断对错？字符串在创建后可以被修改。

A) 正确  
B) 错误

答案是 B。字符串在 JavaScript 中是不可变的。然而，指向字符串的变量当然可以重新赋值为另一个字符串。

Q27 未回答。

**Q28 已回答。** 判断对错？JavaScript 是同步的。

A) 正确  
B) 错误

答案是 A。JavaScript 运行时中的队列是同步的，因此该语言是同步的。

Q28 未回答。

**Q29 已回答。** 判断对错？Promise 链中嵌套的 `catch` 可以捕获 Promise 链中更上层抛出的错误？

A) 正确  
B) 错误

答案是 B。根据 MDN 文档：“嵌套是一种控制结构，用于限制 `catch` 语句的作用域。具体来说，嵌套的 `catch` 只捕获其作用域及以下范围内的失败，而不是嵌套作用域之外链中更上层的错误”。

更多阅读请参见：https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises

Q29 未回答。

**Q30 已回答。** 判断对错？`Map` 对象可以具有字符串以外的类型的键，例如数字。

A) 正确  
B) 错误

答案是 A。

Q30 未回答。

**Q31 已回答。** 下面的代码会向控制台输出什么，为什么？

```javascript
const map = new Map();
map.set({},1);
console.log(map.get({}));
```

A) `undefined`  
B) 1  
C) 编译时错误

答案是 A。`map.get({})` 是有效的语法，但 `set` 中的对象和 `get` 中的对象是内存中两个不同的空对象。因此，getter 不返回值。如果用于 `map.set` 的对象首先被赋值给一个 `const`，然后该 `const` 被用于 `get`，则会返回适当的值。

Q31 未回答。

**Q32 已回答。** 下面的代码会向控制台输出什么，为什么？

```javascript
let map1 = new Map([['a', 1],['b', 1],['c', 1]]);
let map2 = new Map([['a', 2],['b', 2]]);
let spreadMap = new Map([...map1, ...map2]);
```

A) `Map(3) {"a" => 1, "b" => 1, "c" => 1}`  
B) `Map(3) {"a" => 2, "b" => 2, "c" => 1}`  
C) `Map(5) {"a" => 1, "b" => 1, "c" => 1, "a" => 2, "b" => 2}`

答案是 B。第二个映射中的任何相同键都会覆盖第一个映射中的键。

Q32 未回答。

**Q33 已回答。** 判断对错？括号表示法可以像点表示法一样链式使用？

A) 正确  
B) 错误

答案是 A。`obj.prop1.prop2` 和 `obj['prop1']['prop2']` 是等价的。

Q33 未回答。

**Q34 已回答。** 下面的代码会向控制台输出什么，为什么？

```javascript
class Person {
  name: string;
  DOB: string;
}
console.log(typeof Person);
```

A) `"class"`  
B) `"function"`  
C) `"object"`

答案是 B。这提醒我们，类只是让 JavaScript 感觉更面向对象的语法糖。

Q34 未回答。

**Q35 已回答。** 检查下面的代码。诊断将发生的错误。假设 `handleResponse` 和 `handleError` 已正确定义。

```javascript
promise.then(function(response) {
  this.handleResponse();
},
function(error) {
  this.handleError();
});
```

答案是 `this` 的作用域不正确。相反，代码需要一种方法来获得 `this` 的正确作用域，例如使用 `bind` 或 `var self = this;`。

Q35 未回答。

**Q36 已回答。** 哪些类型的属性会出现在 `for...in` 循环中？

A) 可执行属性  
B) 可枚举属性  
C) 可迭代属性

答案是 B。

Q36 未回答。

**Q37 已回答。** 判断对错？`.bind(this)` 会立即调用绑定的函数。

A) 正确  
B) 错误

答案是 B。

Q37 未回答。

**Q38 已回答。** 代码会打印什么？

```javascript
function getName() {
  var name = "Jon";
  function printName() {
    console.log(name);
  }
  printName();
}
getName();
```

A) `Jon`  
B) `undefined`  
C) 编译时错误

答案是 A。内部函数可以访问外部作用域中声明的变量。

Q38 未回答。

**Q39 已回答。** 判断对错？`await` 关键字是 `async` 函数所必需的？

A) 正确  
B) 错误

答案是 B。`async` 函数返回一个 Promise，并且有许多用途。`await` 关键字增加了可能不需要的额外功能和开销。参见[此处](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await)的示例。

Q39 未回答。

**Q40 已回答。** 函数可以通过哪三种方式引用自身进行递归？选择三个答案。

A) 使用 `self.run`  
B) 函数的名称  
C) 作用域内引用该函数的变量  
D) 使用 `arguments.callee`

答案是 B、C、D。

Q40 未回答。

---

## 测试 2 问题

**Q1.** 考虑以下代码：

```typescript
class Person {
  firstName: string;
  lastName: string;
}
const myPerson = new Person();
console.log(myPerson.a);
```

解释原型链如何用于确定 `myPerson.a` 是 `undefined`？

Q1 已回答。

**Q2.** `class` 关键字在 JavaScript 中做什么？

A) 它传达了超越典型对象的实际含义  
B) 它是让 JavaScript 更面向对象的语法糖  
C) 它创建了一个可用于继承的类似接口的对象

Q2 已回答。

**Q3.** 下面的代码会向控制台输出什么，为什么？

```javascript
let x = 10;
if(x){
  let x = 12;
  console.log(x);
}
```

A) 10  
B) 12  
C) 它会抛出一个错误

Q3 已回答。

**Q4.** 判断对错？来自 `queueMicrotask` 队列的任务以后进先出的方式执行。

A) 正确  
B) 错误

Q4 已回答。

**Q5.** 遵循“干净代码”原则，这个函数应该叫什么名字？

```javascript
const pntDT = () => {
  const today = new Date();
  const time = today.getHours() + ":" + today;
  console.log(time);
};
pntDT();
```

Q5 已回答。

**Q6.** 以下哪一项不是创建和注册新自定义元素的步骤？

A) 在 DOM 中创建一个 HTML 容器  
B) 创建一个定义元素行为的 JavaScript 类  
C) 使用 `CustomElementRegistry` 对象注册该类和一个表示元素名称的 DOMString

Q6 已回答。

**Q7.** 简要解释 Shadow DOM API。

Q7 已回答。

**Q8.** 哪个方法将影子 DOM 树附加到指定元素并返回对其 `ShadowRoot` 的引用？

A) `Element.shadowAdd()`  
B) `Element.setDOMShadow()`  
C) `Element.attachShadow()`

Q8 已回答。

**Q9.** `arr[2][1]` 会返回什么值？

```javascript
const arr = [["a", "b", "c"],
             ["d", "e", "f"],
             ["g", "h", "i"]];
```

A) `d`  
B) `h`  
C) `b`  
D) 以上都不是

Q9 已回答。

**Q10.** 下面的代码会向 `<app>` 输出什么？

```javascript
document.getElementById("app").innerHTML = `<div>hewohewo2</div>`
```

A) `hewo      hewo2`  
B) `hewohewo2`  
C) `hewo hewo2`  
D) 无法编译

Q10 已回答。

**Q11.** jQuery 使用什么模式来创建其全局可用的 jQuery 对象的单个实例？

A) OOP  
B) 工厂  
C) 单例  
D) 无

Q11 已回答。

**Q12.** `window.localStorage` 和 `window.sessionStorage` 有什么区别？选择最佳答案。

A) `localStorage` 在 Web 浏览器中存储键/值对，并且 `localStorage` 在浏览器关闭后删除  
B) `sessionStorage` 在 Web 浏览器中存储键/值对，并且 `sessionStorage` 在浏览器关闭后删除  
C) 两者都在 Web 浏览器中存储键/值对，但 `localStorage` 在浏览器关闭后删除  
D) 两者都在 Web 浏览器中存储键/值对，但 `sessionStorage` 在浏览器关闭后删除

Q12 已回答。

**Q13.** 下面的代码会向控制台输出什么，为什么？

```javascript
let arr1 = [1, 2, 3];
arr1.push(4);
arr1.pop();
arr1.slice(1, 2);
arr1.splice(1, 2);
console.log(arr1);
```

A) 1  
B) `[1]`  
C) `[1,2]`  
D) `[2,3]`  
E) 什么都不打印。

Q13 已回答。

**Q14.** 判断对错：`!` 运算符返回一个布尔值。选择一个选项。

A) 正确  
B) 错误

Q14 已回答。

**Q15.** 评估下面的代码。如果 `div` 和 `button` 都有点击监听器，如何阻止按钮上的点击冒泡到 `div`？

```html
<div><button>Click Me!</button></div>
```

A) 在按钮的 clickHandler 中使用 `Event.stopPropagation`  
B) 在 div 的 clickHandler 中使用 `Event.stopPropagation`  
C) 在按钮的 clickHandler 中使用 `Event.stopBubble`  
D) 在 div 的 clickHandler 中使用 `Event.stopBubble`

Q15 已回答。

**Q16.** 下面的代码会向控制台输出什么，为什么？

```javascript
let xyz = "";
xyz ||= "abc";
console.log(xyz);
```

A) `abc`  
B) `''`  
C) 编译时错误

Q16 已回答。

**Q17.** 以下两个函数的输出有什么区别？

```javascript
void function voidExample() {
  console.log("No Error!");
}();

function noVoidExample() {
  console.log("No Error!");
}();
```

A) 函数 `noVoidExample` 执行并打印 `No Error`，而 `voidExample` 抛出一个错误。  
B) 函数 `voidExample` 执行并打印 `No Error`，而 `noVoidExample` 抛出一个错误。  
C) 两者都抛出一个错误

Q17 已回答。

**Q18.** 以下哪一项不是 `NodeList` 和 `Array` 之间的区别？

A) `NodeList` 是 Web API，`Array` 是 JavaScript API  
B) `NodeList` 不能包含超过 10 个项目  
C) `NodeList` 属性可能是实时属性，如果 DOM 更新（如 `childNode`），它们会更新  
D) 许多数组函数在 `NodeList` 上不可用

Q18 已回答。

**Q19.** JavaScript 中哪些 ES6 数组函数返回一个新数组？选择所有正确的答案。

A) `map()`  
B) `forEach()`  
C) `filter()`  
D) `find()`

Q19 已回答。

**Q20.** JavaScript 使用数字原始值可以可靠表示的最大整数是多少？

A) 2⁵³ - 1  
B) 2³² - 1  
C) 2⁶³ - 1  
D) JavaScript 可以表示无限大的数字

Q20 已回答。

**Q21.** 哪个函数会将字符串修改为符合 URI 规范？

A) `JSON.stringify()`  
B) `encodeURI()`  
C) `encodeString()`  
D) `JSON.parse()`

Q21 已回答。

**Q22.** 在 JS 中，64 位如何分配给一个数字来存储数字？

Q22 已回答。

**Q23.** 在计算机科学中，`null` 和 `undefined` 有什么区别？

Q23 已回答。

**Q24.** JavaScript 中减号（`-`）的技术名称是什么？

A) 一元减法  
B) 二元否定  
C) 一元否定  
D) 二元减法

Q24 已回答。

**Q25.** 判断对错？`super` 关键字不能在构造函数之外使用。

A) 正确  
B) 错误

Q25 已回答。

**Q26.** 访问 `cat` 对象上的 `color` 值的两种方法是什么？

```javascript
const cat = {color: "orange"};
```

Q26 已回答。

**Q27.** JavaScript 运行时中的栈是什么？

Q27 已回答。

**Q28.** 十六进制转义序列的语法是什么？

A) `'\xab1'`  
B) `'\10ab'`  
C) `'\x'`

Q28 已回答。

**Q29.** 编写代码，在纯 JavaScript（无 TypeScript）中创建一个自定义的抽象类？`abstract` 关键字在 ES2015 中不可用。

Q29 已回答。

**Q30.** 下面的代码会向控制台输出什么，为什么？

```javascript
const badMap = new Map();
badMap.set('a', 1);
badMap.b = 2
console.log(badMap)
```

A) `Map(1) {"a" => 1}`  
B) `Map(1) {"b" => 2}`  
C) `Map(2) {"a" => 1, "b" => 2}`  
D) 编译时错误

Q30 已回答。

**Q31.** 面向对象编程（OOP）的好处是什么？选择三个答案。

A) 代码是可插拔或模块化的，因此类的源代码可以独立于应用程序的其余代码进行维护。  
B) 对象的代码保持私有，这意味着其他对象只与对象的方法交互，因此内部代码被隐藏。  
C) 对象易于重用。它们可以插入到代码的多个部分。  
D) 面向对象的代码执行速度更快，计算机资源使用最小化。

Q31 已回答。

**Q32.** 假设 `const map` 具有以下值：`Map(2) {"a" => 2, "b" => 2}`。在一行中，将 `map` 转换为二维数组。

Q32 已回答。

**Q33.** 判断对错？在 JavaScript 中，只有自定义类和对象可以被扩展？

A) 正确  
B) 错误

Q33 已回答。

**Q34.** 判断对错？只要创建了实例，实例级变量就可以在类中的任何位置访问。

A) 正确  
B) 错误

Q34 已回答。

**Q35.** 为什么这段代码无法编译？选择一个选项。

```typescript
let i: number;
if(5%3>2){
  i=0;
} else if(5%3>1){
  i=1;
}
console.log(i);
```

A) 它编译正常  
B) `5%3>2` 和 `5%3>1` 不返回布尔值，因此不能在 `if` 语句中使用  
C) `i` 是一个局部变量，其值从未显式定义

Q35 已回答。

**Q36.** 判断对错？`length` 是字符串上的方法，是数组上的属性？

A) 正确  
B) 错误

Q36 已回答。

**Q37.** `function.call` 的第一个参数是什么？

A) 被调用函数的参数  
B) 它不接受任何选项  
C) 调用该函数的实例对象

Q37 已回答。

**Q38.** `printName` 这种函数的技术名称是什么？选择所有正确的选项。

```javascript
function getName() {
  var name = "Jon";
  function printName() {
    console.log(name);
  }
  printName();
}
getName();
```

A) 内部函数  
B) 包含函数  
C) 闭包

Q38 已回答。

**Q39.** 判断对错？箭头函数只有在有多个参数时才需要括号。

A) 正确  
B) 错误

Q39 已回答。

**Q40.** 判断对错？类级变量可以在类中的任何位置访问。

A) 正确  
B) 错误

Q40 已回答。

**Q41.** 当你尝试给 `const` 赋值新值时，会抛出什么类型的错误？

A) `ReferenceError`  
B) `Error`  
C) `RangeError`  
D) `TypeError`

Q41 已回答。

**Q42.** 关于 getter 和 setter，以下哪些是正确的？选择 2 个选项。

A) Getter 和 setter 提高了代码的可重用性。  
B) Getter 和 setter 是面向对象编程的组成部分  
C) Getter 和 setter 控制程序的流程  
D) Getter 和 setter 维护封装

Q42 已回答。

**Q43.** 重写和重载是哪个面向对象编程原则的例子？

A) 继承  
B) 抽象  
C) 多态  
D) 封装

Q43 已回答。

**Q44.** 判断对错：`static` 变量不能在非静态方法中修改？

A) 正确  
B) 错误

Q44 已回答。

**Q45.** 如果 `str === 'test1'`，下面的代码会发生什么？

```javascript
switch (str) {
  case "test1":
  case "test2":
    console.log("At test2");
}
```

A) 打印 “At test2”  
B) 什么都不做  
C) 运行时错误

Q45 已回答。

**Q46.** 当 JavaScript 被描述为具有“一等函数”时，这意味着什么？

A) 函数可以是递归的  
B) 函数可以是匿名的  
C) 函数像任何其他变量一样被对待  
D) 函数使用花括号语法

Q46 已回答。

**Q47.** 判断对错？以下代码可以编译。

```javascript
async function promiseMe() {
  try {
    let z = await Promise.reject(30);
  }
}
```

A) 正确  
B) 错误

Q47 已回答。

**Q48.** 判断对错？`Date.getDate()` 返回月份中的日期，值为 1-31，而 `Date.getDay()` 返回星期中的日期，值为 0-6。

A) 正确  
B) 错误

Q48 已回答。

**Q49.** 异步操作被放入什么类型的队列？

A) 阻塞队列  
B) 事件队列  
C) 异步队列

Q49 已回答。

**Q50.** JavaScript 长期以来提供了哪三个函数用于在时间过去后执行代码？选择三个答案。

A) `setTimeout()`  
B) `setInterval()`  
C) `callAsyncLoop()`  
D) `requestAnimationFrame`

Q50 已回答。

**Q51.** 如果你想测量代码块的执行时间，可能会调用哪个 Web API？

A) `window.now()`  
B) `window.timer()`  
C) `performance.now()`  
D) `performance.timer()`

Q51 已回答。

**Q52.** 什么是 MIME 类型？

Q52 已回答。

**Q53.** 导出以下变量的简单语法是什么？

```javascript
let myLet = 10;
```

Q53 已回答。

**Q54.** 哪个函数属性返回函数期望的参数数量？

A) `Function.argsLength`  
B) `Function.length`  
C) `Function.parameters`

Q54 已回答。

**Q55.** “仅为副作用导入模块”是什么意思？

Q55 已回答。

**Q56.** 判断对错？以下代码编译并打印 3？

```javascript
const test = () => {
  return1 + 2;
}
console.log(test());
```

A) 正确  
B) 错误

Q56 已回答。

**Q57.** 判断对错？以下两者是等价的。

```javascript
var a, z = 1;
a = z;
```

和

```javascript
var a = z = 1;
```

A) 正确  
B) 错误

Q57 已回答。

**Q58.** 判断对错？下面的代码返回 3。

```javascript
const arr = [1, 2];
const reduced = arr.reduce((accumulator, element) => accumulator);
```

A) 正确  
B) 错误

Q58 已回答。

**Q59.** `"use strict";` 指令必须放在文件的什么位置？

A) 顶部  
B) 中间  
C) 底部  
D) 作为导入

Q59 已回答。

**Q60.** 如何在纯 JavaScript（无 TypeScript）中使用组合？

Q60 已回答。

**Q61.** 下面的代码会向控制台输出什么，为什么？

```javascript
for(let i = 1, j = 10; i< 5 < j; i += j/i){
  console.log(Math.ceil(++i));
}
```

A) 什么都不输出  
B) 除以零错误  
C) 1, 12  
D) 它会进入无限循环

Q61 已回答。

**Q62.** 展示如何在不使用冒号 `:` 的情况下构造对象字面量。

Q62 已回答。

**Q63.** JavaScript 中数组的最大大小是多少？

A) 2¹⁶ - 1  
B) 2³² – 1  
C) 2¹⁶ – 1  
D) 2⁸ - 1

Q63 已回答。

**Q64.** 如果一个函数被调用时传递的参数少于声明的参数数量，缺失的参数会被赋予什么值？

A) `null`  
B) `undefined`  
C) 0

Q64 已回答。

**Q65.** 什么是事件捕获阶段？

Q65 已回答。

**Q66.** 判断对错？Setter 在冻结对象上仍然有效。

A) 正确  
B) 错误

Q66 已回答。

**Q67.** `3 > 2 > 1` 返回什么？

A) `true`  
B) `false`  
C) 0

Q67 已回答。

**Q68.** 以下两段代码返回相同的值。它们发生的方式有什么区别？

```javascript
'123'.length;  //第 1 行
new String(123).length;  //第 2 行
```

A) 第 1 行使用显式强制转换，第 2 行使用隐式强制转换  
B) 第 1 行使用隐式强制转换，第 2 行使用显式强制转换  
C) 没有区别

Q68 已回答。

**Q69.** 以下哪种情况不是使用匿名函数的时候？

A) 作为类方法  
B) 在闭包中  
C) 作为回调  
D) 作为 IIFE（立即调用函数表达式）

Q69 已回答。

**Q70.** 在 Web 浏览器中，布局时间和绘制时间有什么区别？

Q70 已回答。

**Q71.** 下面的代码会向控制台输出什么，为什么？

```javascript
let a = 8
a >>>= 3;
console.log(a);
```

A) 1  
B) 10  
C) 4

Q71 已回答。

**Q72.** 下面的代码会向控制台输出什么，为什么？

```javascript
console.log([1, 2,,3].join(', '));
```

A) lint 错误  
B) 1, 2, 3  
C) 1, 2, , 3

Q72 已回答。

**Q73.** 给出一个如何避免网络调用中的竞态条件的例子？

Q73 已回答。

**Q74.** 什么是纯函数？

Q74 已回答。

**Q75.** 什么是柯里化？

Q75 已回答。

---

## 测试 3 问题

**Q1.** 判断对错？编译器会为下面的代码抛出一个错误。

```javascript
const x = 10;
x = 12;
```

A) 正确  
B) 错误

Q1 已回答。

**Q2.** 下面代码的 TypeScript 类型是什么？

```typescript
const x = "hello"
```

A) `"hello"`  
B) `const`  
C) `string`  
D) 没有分配类型

Q2 已回答。

**Q3.** 下面的代码会向控制台输出什么，为什么？

```javascript
let person = {
  age: 25,
  name: 'Justin'
}
const byRef = (myObj) => {
  myObj.age = 30
}
byRef(person);
console.log(person.age);
```

A) 25  
B) 30  
C) 编译时错误

Q3 已回答。

**Q4.** 下面的代码会向控制台输出什么，为什么？

```javascript
let x;
if(x = true === true){
  console.log(x);
} else {
  console.log('Not x');
}
```

A) `true`  
B) `false`  
C) `Not x`  
D) 编译时错误

Q4 已回答。

**Q5.** 下面的代码会向控制台输出什么，为什么？

```javascript
let x = 10;
function myFunc(y){
  y = 12;
}
console.log(myFunc(x));
```

A) 10  
B) 12  
C) `undefined`

Q5 已回答。

**Q6.** 假设下面的聚合函数计算你的年龄天数，组合你的名和姓，并拆分你的地址。选择所有它违反干净代码原则的方式。

```javascript
const aggregator = (DOB, firstName, lastName, address, skills) => {...}
```

A) 函数命名不当  
B) 函数应该使用 `function` 关键字而不是 lambda 函数  
C) 函数做了太多事情，应该拆分  
D) 函数没有对 `skills` 参数做任何操作

Q6 已回答。

**Q7.** 从 JS 的角度来看，DOM 的技术定义是什么？

Q7 已回答。

**Q8.** 给定 `FancyButton` 类，如何扩展 button 以创建一个名为 `fancy-button` 的自定义元素？

A) `customElements.extend('fancy-button', FancyButton, { extends: 'button' });`  
B) `customElements.extend('fancy-button', FancyButton, { implements: 'button' });`  
C) `customElements.define('fancy-button', FancyButton, { extends: 'button' });`  
D) `customElements.define('fancy-button', FancyButton, { implements: 'button' });`

Q8 已回答。

**Q9.** 以下哪个是正确的字符串插值语法？

```javascript
const x = 'me';
```

A) `` `Pick ${x}` ``  
B) `` `Pick &{x}` ``  
C) `'Pick ${x}'`  
D) `'Pick &{x}'`

Q9 已回答。

**Q10.** 将对象实例总数限制为一个的模式名称是什么？

A) 单例  
B) 工厂  
C) 设计  
D) OOP

Q10 已回答。

**Q11.** 以下哪一项不是 `Set` 对象上的方法？

A) `add()`  
B) `next()`  
C) `clear()`  
D) `delete()`  
E) `entries()`

Q11 已回答。

**Q12.** 哪个 window 方法允许你在浏览器内存中存储持久的键/值对？

A) `window.browserStorage`  
B) `window.localStorage`  
C) `window.persistentStorage`  
D) 没有方法允许这样做

Q12 已回答。

**Q13.** 所有位运算都是在多少位的二进制数上执行的？

A) 8  
B) 16  
C) 32  
D) 64

Q13 已回答。

**Q14.** 什么时候 `delete` 运算符不会从对象中删除属性？

Q14 已回答。

**Q15.** 如果你需要获取对象的属性，应该调用什么方法？

A) `Object.getKeyValues`  
B) `Object.getList`  
C) `Object.getNames`  
D) `Object.getOwnPropertyNames`

Q15 已回答。

**Q16.** 下面的代码会向控制台输出什么，为什么？

```javascript
console.log(2 * 3 ** 3);
```

A) 216  
B) 18  
C) 54  
D) 编译时错误

Q16 已回答。

**Q17.** 评估下面的代码。一个字符的更改可以防止这一行抛出错误？

```javascript
const dog = {
  color: "brown",
  breed: {
    pure: true
  }
};
console.log(dog.hair.short)
```

Q17 已回答。

**Q18.** 哪些数组函数在 `NodeList` 上不可用？选择所有适用的。

A) `forEach()`  
B) `join()`  
C) `filter()`  
D) `map()`

Q18 已回答。

**Q19.** 以下哪一项不是 JSON 方法？

A) `reverse()`  
B) `parse()`  
C) `stringify()`

Q19 已回答。

**Q20.** 判断对错？JavaScript 中有一个全局的 `Map` 对象。

A) 正确  
B) 错误

Q20 已回答。

**Q21.** `WeakSet` 对象是弱的是什么意思？

Q21 已回答。

**Q22.** 克服浮点数不精确性的一种方法是什么？

A) 乘法和除法  
B) 它按原样工作  
C) 通过扩展函数运行

Q22 已回答。

**Q23.** 评估下面的代码。如何重构它以使用更少的代码？

```javascript
const temp = object.prop1;
const test = ((temp === null || temp === undefined)) ? undefined : temp.prop2;
```

Q23 已回答。

**Q24.** 评估下面的代码。循环的第一个和最后一个输出是什么？

```javascript
for(let i = 0; i <= 10; ++i){
  console.log(i);
}
```

A) 0, 9  
B) 0, 10  
C) 1, 9  
D) 1, 10

Q24 已回答。

**Q25.** 在下面的 `MyChild` 类上创建一个函数，调用父类的 `printSomething` 方法。

```javascript
class MyParent {
  constructor(){}
  printSomething(){
    console.log(5);
  }
}
class MyChild extends MyParent {
  constructor(){
    super()
  }
  printSomething(){
    console.log(10);
  }
}
```

Q25 已回答。

**Q26.** 下面的代码返回什么，为什么？

```javascript
const value = 10 / -0;
```

A) `NaN`  
B) `-NaN`  
C) `Infinity`  
D) `-Infinity`

Q26 已回答。

**Q27.** JavaScript 运行时中的堆是什么？

Q27 已回答。

**Q28.** 当在字符串字面量值上调用 String 对象方法时，JavaScript 如何在幕后处理它？

Q28 已回答。

**Q29.** 下面的代码会向控制台输出什么，为什么？

```javascript
const obj = {
  a: 1,
  b: 2
};
const arr = [];
console.log(arr[0] = {...obj});
```

A) 1, 2  
B) `{...obj}`  
C) `{a: 1, b: 2}`  
D) 无法编译

Q29 已回答。

**Q30.** `Map.delete(key)` 返回什么？

A) 没有返回值  
B) 总是 `true`  
C) 总是 `false`  
D) 如果键被删除则返回 `true`，如果项目不存在且未被删除则返回 `false`

Q30 已回答。

**Q31.** 以下哪一项不是使用 TypeScript 时继承的例子？选择一个选项。

A) 一个对象具有其超类拥有的字段  
B) 一个对象具有其超类拥有的方法  
C) 一个对象具有其接口拥有的方法  
D) 一个对象具有其超类拥有的静态字段

Q31 已回答。

**Q32.** 判断对错？在 JavaScript 中，一个对象只能有一个子类，但可以有无限多个父类。

A) 正确  
B) 错误

Q32 已回答。

**Q33.** 判断对错？一个对象可以实现多个接口。假设 TypeScript 已启用。

A) 正确  
B) 错误

Q33 已回答。

**Q34.** 代码会打印什么？选择一个选项。

```javascript
class MyClass {
  static staticMethod() {
    return this.name;
  }
  constructor() {
    this.name = 'Jon';
  }
}
const me = new MyClass();
console.log(MyClass.staticMethod());
```

A) `Jon`  
B) `MyClass`  
C) 编译时错误  
D) 运行时错误

Q34 已回答。

**Q35.** 判断对错？`String` 是一种原始数据类型。

A) 正确  
B) 错误

Q35 已回答。

**Q36.** 展示两种使现有数组为空的方法。

Q36 已回答。

**Q37.** 代码执行后 `str` 的值是什么？

```javascript
const str = "  this".concat("that   ").substring(3).trim().valueOf(2);
```

A) 2  
B) `h`  
C) `histhat`  
D) 无法编译

Q37 已回答。

**Q38.** JavaScript 中的生成器函数是什么？

Q38 已回答。

**Q39.** 以下哪一个是类的有效修饰符，假设 TypeScript 已启用？选择一个选项。

A) `private`  
B) `final`  
C) `abstract`  
D) `public`  
E) `default`

Q39 已回答。

**Q40.** 以下哪一项不是 JavaScript 中的保留字？选择一个选项。

A) `abstract`  
B) `compile`  
C) `do`  
D) `enum`

Q40 已回答。

**Q41.** 这段代码的输出是什么？

```javascript
class TestClass{
  constructor() {
    this.myInt = 5;
  }
  mainMethod(){
    const test = new TestClass();
    test.myInt = 6;
    console.log(test.incrementIntAgain(test.incrementInt(test.myInt)));
  }
  incrementInt (theirInt) {
    return theirInt++;
  }
  incrementIntAgain (theirInt) {
    return ++theirInt;
  }
}
```

A) 5  
B) 6  
C) 7  
D) 8

Q41 已回答。

**Q42.** 这段代码的输出是什么？

```javascript
class TestClass{
  constructor() {
    this.myInt = 5;
  }
  mainMethod(){
    const test = new TestClass();
    test.myInt = 6;
    console.log(test.incrementIntAgain(test.incrementInt(test.myInt)));
  }
  incrementInt (theirInt) {
    return theirInt++;
  }
  incrementIntAgain (theirInt) {
    return ++theirInt;
  }
}
```

A) 5  
B) 6  
C) 7  
D) 8

Q42 已回答。

**Q43.** 判断对错：实例级对象可以访问静态变量？

A) 正确  
B) 错误

Q43 已回答。

**Q44.** 下面的代码会向控制台输出什么，为什么？

```javascript
function Dog(name) {
  this.name = name;
}
const buddy = new Dog("buddy");
const rover = Object.create(buddy);
console.log(Object.getPrototypeOf(rover));
console.log(Object.getPrototypeOf(buddy));
```

Q44 已回答。

**Q45.** 下面的代码会向控制台输出什么，为什么？

```javascript
let x = (1, 2, 3);
console.log(x);
```

A) 1  
B) 2  
C) 3  
D) 编译时错误

Q45 已回答。

**Q46.** `RegExp` 字面量表示法和构造函数之间的一些区别是什么？选择所有适用的。

A) 字面量表示法的参数用斜杠括起来，没有引号  
B) 字面量表示法在编译时求值  
C) 构造函数不使用斜杠，但使用引号  
D) 构造函数在运行时求值

Q46 已回答。

**Q47.** 打印顺序是什么？

```javascript
function resolveQuickly(x) {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log(x)
    }, 1);
  });
}
async function asyncTest() {
  var x = resolveQuickly(10);
  console.log(5);
}
asyncTest();
```

A) 10, 5  
B) 5, 10  
C) 什么都不打印。

Q47 已回答。

**Q48.** JavaScript 这个名字从何而来？

Q48 已回答。

**Q49.** 以下哪一项不是 Promise 相对于旧式回调的优势？

A) 执行速度  
B) `.then()` 链式调用  
C) Promise 回调总是按照它们在事件队列中放置的顺序被调用  
D) 更好的错误处理  
E) Promise 避免了控制反转

Q49 已回答。

**Q50.** 判断对错？`do-while` 循环总是至少执行一次。

A) 正确  
B) 错误

Q50 已回答。

**Q51.** 展示一个递归调用 `setTimeout` 来模拟 `setInterval` 的例子。

Q51 已回答。

**Q52.** JSON 支持哪些数据类型？选择所有适当的答案。

A) `string`  
B) `number`  
C) `object`  
D) `null`  
E) `array`  
F) `boolean`

Q52 已回答。

**Q53.** 将 `theFunction` 作为默认导出的两种语法是什么？

Q53 已回答。

**Q54.** 函数声明和函数表达式在语法上有什么区别？

Q54 已回答。

**Q55.** 判断对错？`import` 可以作为函数调用。

A) 正确  
B) 错误

Q55 已回答。

**Q56.** 下面的代码会向控制台打印什么，为什么？

```javascript
console.log(x)
x = 5;
if(x){
  var x = 10;
  console.log(x);
}
```

A) 5, 10  
B) 10, 10  
C) 5, 5

Q56 已回答。

**Q57.** 数组 `reduce()` 的目的是什么？

A) 将数组减少为回调  
B) 将数组减少为复合函数  
C) 将数组减少为单个值。

Q57 已回答。

**Q58.** 什么是记忆化？

A) 通过缓存先前计算的结果来提高函数性能  
B) JavaScript 中不可用的东西  
C) 为将来的对象使用创建对象属性的组合

Q58 已回答。

**Q59.** 在 JavaScript 中创建一个抽象类的例子。

Q59 已回答。

**Q60.** 给出一个使用 `String.prototype.match` 将字符串通过正则表达式运行的例子。

Q60 已回答。

**Q61.** 下面的代码会向控制台输出什么，为什么？

```javascript
for(let i = 6; i > 0; i-=2){
  if(i%2){
    continue;
  }
  console.log(i)
}
```

A) 什么都不输出  
B) 4, 2, 0  
C) 6, 4, 2  
D) 4, 2

Q61 已回答。

**Q62.** 判断对错？对象上重复的属性名被视为语法错误。

A) 正确  
B) 错误

Q62 已回答。

**Q63.** 判断对错？以下语法不正确。

```javascript
function foo(arg) {
  let arg = 1;
}
```

A) 正确  
B) 错误

Q63 已回答。

**Q64.** 包含传递给函数的所有对象值的类数组对象的名称是什么？

A) `arguments`  
B) `args`  
C) `params`  
D) `parameters`

Q64 已回答。

**Q65.** 下面代码中的第三个参数 `true` 用于什么？

```javascript
element.addEventListener("click", e => console.log(element.eventPhase), true);
```

A) 启用捕获阶段的事件捕获  
B) 启用冒泡阶段的事件捕获  
C) 它在 `addEventListener` 函数中未使用

Q65 已回答。

**Q66.** 在考虑强制转换时，什么是包装对象？

Q66 已回答。

**Q67.** `3 > 2 == 1` 返回什么？

A) `true`  
B) `false`  
C) 0

Q67 已回答。

**Q68.** JavaScript 中的真值是什么？

Q68 已回答。

**Q69.** 以下语法的名称是什么？

```javascript
(function() {
  console.log('IIFE');
})();
```

Q69 已回答。

**Q70.** 箭头函数的作用域是什么？

A) 全局  
B) 它们被定义时的作用域  
C) 块级

Q70 已回答。

**Q71.** 下面的代码会向控制台输出什么，为什么？

```javascript
let a = 8
a >>>= 5;
console.log(a);
```

A) -1  
B) -1167541818  
C) 0

Q71 已回答。

**Q72.** 判断对错？数组上的 `shift` 和 `pop` 方法返回一个新数组，而不改变原始数组的值。

A) 正确  
B) 错误

Q72 已回答。

**Q73.** 判断对错？分配给 `const` 的对象是不可变的。

A) 正确  
B) 错误

Q73 已回答。

**Q74.** 命令式编程和声明式编程有什么区别？

Q74 已回答。

**Q75.** 语句和表达式有什么区别？

A) 语句执行一个动作，表达式求值为一个值  
B) 语句求值为一个值，表达式执行一个动作  
C) 以上都不正确

Q75 已回答。

---

## 测试 4 问题

**Q1.** 判断对错？评估下面的代码。`bark()` 现在是 `Dog` 类上的一个函数。

```javascript
class Dog {
  noise: string;
  legs: number;
}
Dog.bark = () => {
  console.log('woof');
}
let dog = new Dog();
dog.bark();
```

A) 正确  
B) 错误

Q1 已回答。

**Q2.** 判断对错？评估下面的代码。`bark()` 现在是 `Puppy` 类上的一个函数。

```javascript
class Dog {
  noise: string;
  legs: number;
}
Dog.prototype.bark = () => {
  console.log('woof');
}
class Puppy extends Dog {
  pottyTrained: boolean;
}
let dog = new Puppy();
dog.bark();
```

A) 正确  
B) 错误

Q2 已回答。

**Q3.** 评估下面的代码。`getDOB` 函数有什么问题？此问题已启用 TypeScript。

```typescript
const getDOB = (firstName: string, lastName: string) => {
  return `${firstName} ${lastName}`;
}
```

A) `getDOB` 在字符串插值中有不正确的语法  
B) 参数的类型错误  
C) 它返回 `undefined`  
D) 它命名不当

Q3 已回答。

**Q4.** 以下哪一个是自定义元素的控制器？

A) `CustomHTML` 对象  
B) `HTMLElementRegistry` 对象  
C) `CustomController` 对象  
D) `CustomElementRegistry` 对象

Q4 已回答。

**Q5.** 自定义元素应该扩展哪个类？

A) `DOMElement`  
B) `HTMLElement`  
C) `CustomElement`

Q5 已回答。

**Q6.** 下面的代码会向控制台输出什么，为什么？

```javascript
let x = 2.2 + 4.4 === 6.6;
console.log(x);
```

A) `undefined`  
B) `true`  
C) `false`  
D) 无法编译  
E) 6.6

Q6 已回答。

**Q7.** 下面的 ES6 之前的代码会向控制台输出什么，为什么？TypeScript 未启用。

```javascript
function SomeClass() {
  this.publicVar = 10;
}
SomeClass.staticVar = 10;
const myClass = new SomeClass();
myClass.publicVar = 12;
myClass.staticVar = 15;
const myClass2 = new SomeClass();
console.log(myClass2.publicVar);
console.log(myClass2.staticVar);
console.log(SomeClass.staticVar);
```

A) 10, undefined, 12  
B) 10, 12, 12  
C) 10, 15, 15  
D) 12, undefined, 10  
E) 10, undefined, 10

Q7 已回答。

**Q8.** 编写一个函数，用一行代码打印下面字符串中的不同元音字母。

```javascript
const str = "abcdeeef";
```

Q8 已回答。

**Q9.** 下面的代码会向控制台输出什么，为什么？

```javascript
console.log(Math.floor(2.1) === new Float32Array(2.1));
```

A) `true`  
B) `false`  
C) 编译时错误

Q9 已回答。

**Q10.** 下面的代码会向控制台输出什么，为什么？

```javascript
console.log(Math.sin(Math.PI) === 0);
```

A) `true`  
B) `false`

Q10 已回答。

**Q11.** 下面的代码会向控制台输出什么，为什么？

```javascript
z = 10;
console.log(z);
```

A) 10  
B) 编译时错误  
C) `z`

Q11 已回答。

**Q12.** 下面的代码会向控制台输出什么，为什么？

```javascript
let max;
const numberArray = [3, 5, 2];
numberArray.forEach((element) => {
  if (max < element) {
    max = element;
  }
});
console.log(max);
```

A) 3  
B) 5  
C) 2  
D) `undefined`

Q12 已回答。

**Q13.** 哪个位运算符反转 32 位数字的位？

A) `>>`  
B) `|`  
C) `&`  
D) `~`

Q13 已回答。

**Q14.** 哪个运算符可以从对象中删除属性？

A) `remove`  
B) `delete`  
C) `return`  
D) `configure`

Q14 已回答。

**Q15.** 访问下面 getter 的正确语法是什么？

```javascript
const obj = {
  count: [1, 2, 3],
  get last() {
    return this.count.pop();
  }
};
```

A) `obj.get(last)`  
B) `obj.getLast`  
C) `obj.last`

Q15 已回答。

**Q16.** 什么时候可能会使用 `new.target`？

Q16 已回答。

**Q17.** 你会使用什么方法将 `NodeList` 转换为数组？

A) `Array.to()`  
B) `Array.from()`  
C) `NodeList.to()`  
D) `NodeList.from()`

Q17 已回答。

**Q18.** 判断对错？有两种 `NodeList`：静态和动态。

A) 正确  
B) 错误

Q18 已回答。

**Q19.** `Atomics` 不与哪个对象一起使用？

A) `Buffer`  
B) `SharedArrayBuffer`  
C) `ArrayBuffer`

Q19 已回答。

**Q20.** 哪种 JavaScript 错误类型通常用作用户定义错误对象的基础？

A) `ReferenceError`  
B) `SyntaxError`  
C) `TypeError`  
D) `Error`

Q20 已回答。

**Q21.** 哪个属性保证无论环境如何都能访问全局对象？

A) `self`  
B) `globalThis`  
C) `this`  
D) `window`

Q21 已回答。

**Q22.** 关于 `undefined`，以下哪一项是不正确的？

A) 它是全局对象的一个属性  
B) 它是全局作用域中的一个变量  
C) `undefined` 的初始值是原始值 `undefined`  
D) 它有一个名为 `Undefined` 的对应对象

Q22 已回答。

**Q23.** 判断对错？可选链可以像下面这样堆叠？

```javascript
let stateStats = state.area?.land?.sqmiles;
```

A) 正确  
B) 错误

Q23 已回答。

**Q24.** 下面的代码会向控制台输出什么，为什么？

```javascript
const a;
a.test ??= 25;
console.log(a.test);
```

A) `undefined`  
B) 25  
C) 编译时错误

Q24 已回答。

**Q25.** JavaScript 中括号 `()` 的技术名称是什么？

A) 分组运算符  
B) 括号运算符  
C) 绑定运算符

Q25 已回答。

**Q26.** 下面的代码会向控制台输出什么，为什么？

```javascript
let str = new String('aaa');
str.concat('bbb').concat('ccc');
console.log(str);
```

A) `aaa`  
B) `aaabbbccc`  
C) `ccc`  
D) `bbbccc`

Q26 已回答。

**Q27.** JavaScript 运行时中的队列是什么？

Q27 已回答。

**Q28.** 判断对错？纯 JavaScript（无 TypeScript）从 ES2015 开始就有抽象类。

A) 正确  
B) 错误

Q28 已回答。

**Q29.** 下面的代码会向控制台输出什么，为什么？

```javascript
const b = {
  a: 1,
  b: 2,
  3: 3
}
for(key in b){
  console.log(b[key]);
}
```

A) 1 2 3  
B) 1 2  
C) Uncaught SyntaxError: Unexpected number

Q29 已回答。

**Q30.** 使用多个键/值对初始化 `Map` 对象的语法是什么？

Q30 已回答。

**Q31.** 判断对错？接口可以扩展另一个接口。假设 TypeScript 已启用。

A) 正确  
B) 错误

Q31 已回答。

**Q32.** 判断对错？假设 TypeScript 已启用。一个对象继承其父类的所有字段和方法。

A) 正确  
B) 错误

Q32 已回答。

**Q33.** 以下哪些是 TypeScript 接口方法的有效修饰符？选择所有正确的答案。

A) `public`  
B) `protected`  
C) `private`  
D) `abstract`  
E) 以上都不是。

Q33 已回答。

**Q34.** 判断对错？`static` 关键字在 JavaScript 中不是有效的修饰符。相反，需要像 TypeScript 这样的类型超集才能使 `static` 工作。

A) 正确  
B) 错误

Q34 已回答。

**Q35.** 哪一行代码块会打印以下字符：`☃⌨ ὀ˿`？

Q35 已回答。

**Q36.** 数组中的位置 3 有什么（如果有的话）？

```javascript
const arr = [1, 2];
arr.length = 3;
```

A) 它是空的  
B) 它实际上没有被创建  
C) `null`

Q36 已回答。

**Q37.** 写一个一行示例，反转 `array.reduce` 函数。

Q37 已回答。

**Q38.** 箭头函数的一些限制是什么？选择所有正确的选项。

A) 箭头函数不应作为方法使用  
B) 箭头函数没有 `arguments`、`super` 或 `new.target` 关键字  
C) 箭头函数不能在其主体中使用 `yield` 关键字  
D) 箭头函数不能用作构造函数

Q38 已回答。

**Q39.** 传统函数和箭头函数的默认作用域有什么区别？

Q39 已回答。

**Q40.** 关于访问修饰符，以下哪些通常是正确的？

A) 字段应具有尽可能窄的访问修饰符  
B) 方法应具有尽可能宽的访问修饰符  
C) 除非字段是常量，否则避免使用公共字段

Q40 已回答。

**Q41.** 如果在 `for` 循环中忘记括号，会抛出什么类型的错误？

A) `SyntaxError`  
B) `TypeError`  
C) `ReferenceError`

Q41 已回答。

**Q42.** 判断对错？下面的代码是重载的例子。

```javascript
console.log({a: 1}.toString = 'Test');
```

A) 正确  
B) 错误

Q42 已回答。

**Q43.** 判断对错？JavaScript 支持类上的静态变量。

A) 正确  
B) 错误

Q43 已回答。

**Q44.** 给出一个使用新的 ES6 语法创建父/子关系的例子。

Q44 已回答。

**Q45.** 判断对错？`try` 语句必须始终后跟至少一个 `catch` 语句。

A) 正确  
B) 错误

Q45 已回答。

**Q46.** 判断对错？当 `RegExp` 会变化时使用 `RegExp` 字面量表示法，当 `RegExp` 保持不变时使用 `RegExp` 构造函数。

A) 正确  
B) 错误

Q46 已回答。

**Q47.** 判断对错？Promise 在 JavaScript 中是异步的。

A) 正确  
B) 错误

Q47 已回答。

**Q48.** Web Workers 的目的是什么？

A) 在主线程之外的单独线程上执行昂贵的任务  
B) 将事件卸载到不同的对象  
C) 加速原型继承

Q48 已回答。

**Q49.** `Promise.resolve()` 返回什么类型的对象？

Q49 已回答。

**Q50.** `setTimeout()` 和 `setInterval()` 有什么区别？选择两个选项。

A) `setTimeout` 在指定时间过去后执行一次  
B) `setInterval` 以给定的延迟重复执行  
C) `setTimeout` 以给定的延迟重复执行  
D) `setInterval` 在指定时间过去后执行一次

Q50 已回答。

**Q51.** 判断对错？`setInterval` 的间隔时间包括执行代码所花费的时间。

A) 正确  
B) 错误

Q51 已回答。

**Q52.** 判断对错？下面的代码可以编译。

```javascript
const array = [1, 2, 3];
for (let i = 0; i < array1.length; array1[i++] = String.fromCharCode(96 + i));
```

A) 正确  
B) 错误

Q52 已回答。

**Q53.** 导入默认导出与导入命名非默认导出有什么区别？

A) 花括号  
B) 默认导出中从不包含名称  
C) 没有区别

Q53 已回答。

**Q54.** 判断对错？函数声明会被提升，函数表达式不会被提升。

A) 正确  
B) 错误

Q54 已回答。

**Q55.** 哪个语句会显示导入模块的 URL？

A) `import.path`  
B) `path.show`  
C) `path.directory`  
D) `import.meta`

Q55 已回答。

**Q56.** `console.log`、`console.error` 和 `console.warn` 有什么区别？

Q56 已回答。

**Q57.** 在以下文档中看到 `prototype` 的意义是什么：`Array.prototype.reduce()` 与 `Array.from()`？选择所有正确的答案。

A) `prototype` 表示 `reduce` 是一个实例级方法  
B) 缺少 `prototype` 表示 `from` 是一个类级方法  
C) `prototype` 表示 `reduce` 继承自 `Object`

Q57 已回答。

**Q58.** 最大调用栈超出错误是如何触发的？

Q58 已回答。

**Q59.** 以下哪一项不是 Web API `window` 对象上用于调整大小的可用方法？

A) `resizeFrom()`  
B) `resizeBy()`  
C) `resizeTo()`  
D) `sizeToContent()`

Q59 已回答。

**Q60.** `String.prototype.replace()` 可以接受哪两种类型作为第一个参数？选择所有正确的选项。

A) `String`  
B) `regex`  
C) `Object`

Q60 已回答。

**Q61.** 下面的代码会向控制台输出什么，为什么？

```javascript
for(let i = 6; i < 10; i*1.5){
  if(i%2){
    continue;
  }
  console.log(i)
}
```

A) 6  
B) 6, 9  
C) 它进入无限循环  
D) Lint 错误

Q61 已回答。

**Q62.** `Object.assign()` 和展开语法之间的一个区别是什么？

A) 展开语法调用 setter，`Object.assign()` 不调用  
B) `Object.assign` 调用 setter，展开语法不调用  
C) 它们的行为实际上相同

Q62 已回答。

**Q63.** 给出一个一行检查对象 `dog` 上是否存在属性的例子。

```javascript
const dog = { sound: 'woof', legs: 4 }
```

Q63 已回答。

**Q64.** 以下哪一项不是将 `arguments` 函数对象转换为数组的方法？

A) `arguments.assign(arguments)`  
B) `Array.prototype.slice.call(arguments);`  
C) `Array.from(arguments);`  
D) `[...arguments]`

Q64 已回答。

**Q65.** 事件处理的目标阶段是什么？

Q65 已回答。

**Q66.** 双感叹号（`!!`）是做什么的？

A) 什么都不做  
B) 返回对象的真值  
C) 抛出一个错误

Q66 已回答。

**Q67.** `1 < 2 < 3` 返回什么？

A) `true`  
B) `false`

Q67 已回答。

**Q68.** JavaScript 如何在布尔上下文中评估值或对象的真值或假值？

A) 类型强制转换  
B) 它是每个对象上的一个属性  
C) 某些值永远没有真值或假值

Q68 已回答。

**Q69.** 使用 IIFE 的目的是什么？选择所有可能的答案。

A) 设置变量值  
B) 在对象上初始化值  
C) 在闭包中用于初始化值  
D) 运行一次性函数

Q69 已回答。

**Q70.** 什么是词法作用域的例子？选择所有可能的答案。

A) 作用域根据变量输入动态定义  
B) `let self = this;` //在父函数中，然后 `self` 对内部函数可用  
C) 内部函数的作用域包含父函数的作用域

Q70 已回答。

**Q71.** 下面的代码会向控制台输出什么，为什么？

```javascript
let a = 3;
a <<= 1;
console.log(a);
```

A) 3  
B) 4  
C) 6  
D) 8

Q71 已回答。

**Q72.** 下面的代码会向控制台输出什么，为什么？

```javascript
badCode = () => {
  let arr = [1,2,3,4];
  const inner = () => {
    return arr.pop(2)
  }
  return inner;
}
console.log(badCode()());
```

A) linting 错误  
B) 3, 4  
C) 34  
D) 4

Q72 已回答。

**Q73.** 下面的代码会向控制台输出什么，为什么？

```javascript
const obj = { a: 1 };
let obj2 = obj;
obj2.a = 2;
console.log(obj.a);
```

A) 1  
B) 2  
C) `undefined`

Q73 已回答。

**Q74.** 编程中的副作用是什么？

Q74 已回答。

**Q75.** 判断对错？`Array.prototype.filter()` 返回一个包含所有未通过提供的函数测试的项目的数组。

A) 正确  
B) 错误

Q75 已回答。

---

## 附加问题（来自原文）

**Q43.** 判断对错？JavaScript 不支持重载？

A) 正确  
B) 错误

Q43 已回答。

**Q44.** 不使用类语法，从父对象创建一个子对象。

Q44 已回答。

**Q45.** 在数组的 `forEach` 循环中，`return` 语句做什么？

A) 什么都不做  
B) 返回指定的值  
C) 结束该循环

Q45 已回答。

**Q46.** 判断对错？`for` 循环中最多有三个参数。

A) 正确  
B) 错误

Q46 已回答。

**Q47.** 判断对错？`RegExp` 没有任何属性。

A) 正确  
B) 错误

Q47 已回答。

**Q48.** 下面的代码会向控制台输出什么，为什么？

```javascript
function resolveQuickly(x) {
  return new Promise(resolve => {
    console.log(x)
  });
}
async function asyncTest() {
  var x = resolveQuickly(10);
  console.log(5);
}
asyncTest();
```

A) 10, 5  
B) 5, 10  
C) 它不打印

Q48 已回答。

**Q49.** 什么是阻塞？

Q49 已回答。

**Q50.** 以下哪一项不是 Promise 的有效状态？

A) 待定  
B) 已兑现  
C) 已拒绝  
D) 已完成

Q50 已回答。

**Q51.** 哪个函数在浏览器下次重绘显示之前执行指定的代码块？

A) `requestAnimationFrame()`  
B) `setTimeout()`  
C) `requestRepaintDelay()`

Q51 已回答。

**Q52.** 假设你想在动画上实现 60fps 的刷新率。编写一个 `setInterval` 函数，以 60fps 触发下面的伪代码 `animate` 函数。

```javascript
function animate() {...}
```

Q52 已回答。

**Q53.** JavaScript 中的两种导出类型是什么？

A) 抽象  
B) 整体  
C) 默认  
D) 命名

Q53 已回答。

**Q54.** 你会使用什么语句来迭代异步对象？

A) `if async then`  
B) `for await…of`  
C) `async iterable`  
D) `do while async`

Q54 已回答。

**Q55.** 为什么在导入模块时使用别名？

Q55 已回答。

**Q56.** 判断对错？下面的代码产生相同的输出。

```javascript
var i, j;
loop1:
for (i = 0; i < 5; i++) {
  loop2:
  for (j = 0; j < 5; j++) {
    if (i === 1 && j === 1) {
      continue loop1;
    }
    console.log(`i: ${i}, j: ${j}`)
  }
}
var i, j
loop1:
for (i = 0; i < 5; i++) {
  loop2:
  for (j = 0; j < 5; j++) {
    if (i === 1 && j === 1) {
      break loop2;
    }
    console.log(`i: ${i}, j: ${j}`)
  }
}
```

A) 正确  
B) 错误

Q56 已回答。

**Q57.** 判断对错？以下两者是等价的。

```javascript
var a = 1;
var z = a;
```

和

```javascript
var a, z = a = 1;
```

A) 正确  
B) 错误

Q57 已回答。

**Q58.** 使用 reducer 找到下面数组的最小值。

```javascript
const arr = [5, 10, 12, 4, 2];
```

Q58 已回答。

**Q59.** JavaScript 中的子程序是什么？

Q59 已回答。

**Q60.** 判断对错？你可能使用事件处理程序 `cut` 和 `copy` 来阻止用户将内容从浏览器复制到剪贴板？

A) 正确  
B) 错误

Q60 已回答。

**Q61.** 下面的代码会向控制台输出什么，为什么？

```javascript
let i = 10
for(; i< 12;){
  console.log(++i);
}
```

A) lint 错误  
B) 运行时错误  
C) 无限循环  
D) 11, 12

Q61 已回答。

**Q62.** 创建新对象的三种方法是什么？

A) `new Object()`  
B) `Object.create()`  
C) 工厂模式  
D) 字面量表示法

Q62 已回答。

**Q63.** 下面的代码会向控制台输出什么，为什么？

```javascript
const a = {x: 1}
const b = {...a}
const c = {};
Object.assign(c, a);
a.x = 2;
console.log(a.x);
console.log(b.x);
console.log(c.x);
```

A) 1, 1, 1  
B) 2, 2, 2  
C) 1, 2, 2  
D) 2, 1, 1  
E) 2, 1, 2  
F) 2, 2, 1

Q63 已回答。

**Q64.** 实现一个经典的闭包例子，每次调用时递增。

Q64 已回答。

**Q65.** 如果 `myFunction` 被调用为 `myFunction(5);`，返回值是什么？

```javascript
function myFunction(x, y) {
  const arr = Array.prototype.slice.call(arguments);
  return arr.length;
}
```

A) 0  
B) 1  
C) 2

Q65 已回答。

**Q66.** `Object.seal()` 会做以下哪些？选择所有适用的。

A) 阻止添加新属性  
B) 将所有现有属性标记为不可配置  
C) 阻止更改现有属性的值

Q66 已回答。

**Q67.** `Object.freeze()` 会做以下哪些？选择所有适用的。

A) 阻止添加新属性  
B) 阻止删除现有属性  
C) 阻止更改属性的可枚举性  
D) 阻止更改属性的可配置性  
E) 阻止更改属性的可写性  
F) 阻止更改属性的值  
G) 阻止更改对象的原型

Q67 已回答。

**Q68.** `event.target` 和 `event.currentTarget` 有什么区别？

A) `event.currentTarget` 返回触发监听器所附加到的元素  
B) `event.target` 返回触发事件的最细粒度元素。  
C) `event.target` 返回触发监听器所附加到的元素  
D) `event.currentTarget` 返回触发事件的最细粒度元素。

Q68 已回答。

**Q69.** 如果你需要稍后调用一个匿名函数，请展示创建该匿名函数时使用的语法。

Q69 已回答。

**Q70.** 数组 `sort()` 方法的默认排序是什么？

A) 按数值从大到小  
B) 按数值从小到大  
C) 按字符值从大到小  
D) 按字符值从小到大

Q70 已回答。

**Q71.** 下面的代码会向控制台输出什么，为什么？

```javascript
let scope = "global";
getScope = () => {
  var scope = "local";
  const inner = () => {
    return scope;
  }
  return inner;
}
getScope()();
```

A) `global`  
B) `local`  
C) `undefined`

Q71 已回答。

**Q72.** 下面的代码会向控制台输出什么，为什么？

```javascript
console.log(3 + '2');
```

A) 32  
B) 5  
C) 运行时错误

Q72 已回答。

**Q73.** 什么是竞态条件？

Q73 已回答。

**Q74.** 什么是函数式编程？

Q74 已回答。

**Q75.** 什么是高阶函数？

A) 由多个函数或接口组成的函数  
B) 可以接受函数作为参数，或返回另一个函数的函数  
C) 作为子对象超类的函数

Q75 已回答。





## 测试 1 答案

## 测试 1

### Q41
下面的代码会向控制台输出什么，为什么？
```javascript
const test = (incrementer) => {
  if (incrementer < 0){
    return;
  }
  console.log('first: ' + incrementer);
  test(incrementer - 1);
  console.log('second: ' + incrementer)
}
test(2);
```
输出如下：
"first: 2"
"first: 1"
"first: 0"
"second: 0"
"second: 1"
"second: 2"

这个函数是递归的。观察它如何堆叠函数调用以及代码执行的顺序很有趣。

### Q42
判断对错？`Promise.any()` 和 `Promise.race()` 的区别在于 `Promise.race()` 返回第一个落定的 Promise（无论兑现还是拒绝），而 `Promise.any()` 会继续解析直到有一个 Promise 被兑现，并且只有当所有 Promise 都被拒绝时才会拒绝。
A) 正确
B) 错误

答案是 A。`Promise.any()` 和 `Promise.race()` 非常相似。

### Q43
判断对错？JavaScript 不支持重载？
A) 正确
B) 错误

答案是 A。虽然 JavaScript 本身不支持重载，但 TypeScript 支持。此外，可以通过让函数在未传入所有可能参数时返回不同输出来模拟重载。

### Q44
不使用 class 语法，从父对象创建一个子对象。

一个示例解决方案：
```javascript
function Dog(name) {
  this.name = name;
}
const buddy = new Dog("buddy");
const rover = Object.create(buddy);
```
如果你检查 `Object.getPrototypeOf(rover)`，你会看到 `buddy` 是 `rover` 的父原型。

### Q45
在数组的 `forEach` 循环中，`return` 语句的作用是什么？
A) 什么都不做
B) 返回指定的值
C) 结束该次循环

答案是 A。如果你需要从循环中返回值，不要使用 `forEach` 循环。

### Q46
判断对错？`for` 循环中最多有三个参数。
A) 正确
B) 错误

答案是 B。例如：
```javascript
for (var i = 0, j = 0; i <= 10; i++, j++){
  …
}
```
这是有效的 `for` 循环语法。

### Q47
判断对错？`RegExp` 没有任何属性。
A) 正确
B) 错误

答案是 B。`RegExp` 有很多属性，例如 `.flags` 和 `.global`。

### Q48
```javascript
function resolveQuickly(x) {
  return new Promise(resolve => {
    console.log(x)
  });
}
async function asyncTest() {
  var x = resolveQuickly(10);
  console.log(5);
}
asyncTest();
```
A) 10, 5
B) 5, 10
C) 它不会打印任何内容

答案是 A。这个函数在 `Promise` 中没有任何异步操作，所以 `Promise` 是同步解析的。

### Q49
什么是阻塞？
答案：当一个缓慢或耗时的进程阻止剩余代码的执行，直到它完成时，就称为阻塞。

### Q50
以下哪个不是 `Promise` 的有效状态？
A) Pending（待定）
B) Fulfilled（已兑现）
C) Rejected（已拒绝）
D) Completed（已完成）

答案是 D。

### Q51
哪个函数会在浏览器下一次重绘显示之前执行指定的代码块？
A) `requestAnimationFrame()`
B) `setTimeout()`
C) `requestRepaintDelay()`

答案是 A。

### Q52
假设你想在动画中达到 60fps 的刷新率。编写一个 `setInterval` 函数，以 60fps 触发下面伪代码中的 `animate` 函数。
```javascript
function animate() {...}
```
答案：`setInterval(animate, Math.ceil(1000/60))`

### Q53
JavaScript 中有哪两种导出方式？
A) Abstract（抽象）
B) Whole（整体）
C) Default（默认）
D) Named（命名）

答案是 C、D。

### Q54
你会使用什么语句来迭代异步对象？
A) if async then
B) `for await…of`
C) async iterable
D) do while async

答案是 B。

### Q55
为什么在导入模块时要使用别名？
答案：可能是因为模块名称很长，或者名称不能正确表达代码的功能。
```javascript
import {longLongLongLongName as shortName}
```

### Q56
判断对错？下面的代码输出相同的结果。
```javascript
var i, j;
loop1:for (i = 0; i < 5; i++) {
  loop2:for (j = 0; j < 5; j++) {
    if (i === 1 && j === 1) {continue loop1;}
    console.log(`i: ${i}, j: ${j}`)
  }
}

var i, j
loop1:for (i = 0; i < 5; i++) {
  loop2:for (j = 0; j < 5; j++) {
    if (i === 1 && j === 1) {break loop2;}
    console.log(`i: ${i}, j: ${j}`)
  }
}
```
A) 正确
B) 错误

答案是 A。

### Q57
判断对错？以下两者等价。
`var a = 1; var z = a;`
和
`var a, z = a = 1;`
A) 正确
B) 错误

答案是 A。

### Q58
使用 reducer 找出下面数组的最小值。
`const arr = [5, 10, 12, 4, 2];`

一个可能的答案：
```javascript
const reducedVal = arr.reduce((accumulator, element) => {
  if (accumulator > element) {
    return element;
  }
  return accumulator;
});
```

### Q59
JavaScript 中的子程序是什么？
答案：子程序是在主程序中遇到的一个函数，它被保存到一个对象中并存储起来供以后使用。执行作用域（变量、参数等）与子程序一起存储。

### Q60
判断对错？你可以使用 `eventHandlers` 的 cut 和 copy 来阻止用户将内容从浏览器复制到剪贴板？
A) 正确
B) 错误

答案是 A。这些事件处理程序是 Web API 的一部分。

### Q61
下面的代码会向控制台输出什么，为什么？
```javascript
let i = 10
for(; i < 12;){
  console.log(++i);
}
```
A) lint 错误
B) 运行时错误
C) 无限循环
D) 11, 12

答案是 D。`for` 循环不需要三个语句，第一个可以为空。

### Q62
创建新对象的三种方式是什么？
A) `new Object()`
B) `Object.create()`
C) 工厂模式
D) 字面量表示法

答案是 A、B、D。字面量表示法的例子：`const obj = { a: 1 }`

### Q63
下面的代码会向控制台输出什么，为什么？
```javascript
const a = {x: 1}
const b = {...a}
const c = {};
Object.assign(c, a);
a.x = 2;
console.log(a.x);
console.log(b.x);
console.log(c.x);
```
A) 1, 1, 1
B) 2, 2, 2
C) 1, 2, 2
D) 2, 1, 1
E) 2, 1, 2
F) 2, 2, 1

答案是 D。

### Q64
实现一个经典的闭包示例，每次调用时递增。

一个可能的答案：
```javascript
var increment = (function () {
  var incrementer = 0;
  return function () {
    incrementer += 1; 
    return incrementer
  }
})();
console.log(increment()); //输出 1
console.log(increment()); //输出 2
console.log(increment()); //输出 3
```

### Q65
如果 `myFunction` 被调用为 `myFunction(5)`，返回值是什么？
```javascript
function myFunction(x, y) {
  const arr = Array.prototype.slice.call(arguments);
  return arr.length;
}
```
A) 0
B) 1
C) 2

答案是 B。

### Q66
`Object.seal()` 做了以下哪些事情？选择所有适用的。
A) 阻止添加新属性
B) 将所有现有属性标记为不可配置
C) 阻止更改现有属性的值

答案是 A、B。一个类似但更严格的函数是 `Object.freeze()`。

### Q67
`Object.freeze()` 做了以下哪些事情？选择所有适用的。
A) 阻止添加新属性
B) 阻止删除现有属性
C) 阻止更改属性的可枚举性
D) 阻止更改属性的可配置性
E) 阻止更改属性的可写性
F) 阻止更改属性的值
G) 阻止更改对象的原型

答案是以上所有。

### Q68
`event.target` 和 `event.currentTarget` 有什么区别？
A) `event.currentTarget` 返回触发监听器所附加到的元素
B) `event.target` 返回事件触发的最具体元素
C) `event.target` 返回触发监听器所附加到的元素
D) `event.currentTarget` 返回事件触发的最具体元素

答案是 A、B。`event.currentTarget` 会随着事件冒泡而改变，`event.target` 保持不变。

### Q69
如果你需要稍后调用一个匿名函数，请展示创建该匿名函数的语法。

一个可能的答案：
```javascript
let caller = function () {
  console.log('call me maybe');
};
```
该函数是匿名的，但被存储到一个变量中以供后续引用。

### Q70
`Array.sort()` 方法的默认排序是什么？
A) 按数值从大到小
B) 按数值从小到大
C) 按字符值从大到小
D) 按字符值从小到大

答案是 D。例如，10 会排在 2 之前，因为 '1' 会与 '2' 进行比较。

### Q71
下面的代码会向控制台输出什么，为什么？
```javascript
let scope = "global";
getScope = () => {
  var scope = "local";
  const inner = () => {
    return scope
  }
  return inner;
}
getScope()();
```
A) global
B) local
C) undefined

答案是 B。内部箭头函数的作用域是它被定义的位置。

### Q72
下面的代码会向控制台输出什么，为什么？
`console.log(3 + ‘2’);`
A) 32
B) 5
C) 运行时错误

答案是 A。3 会被强制转换为字符串。

### Q73
什么是竞态条件？
答案：竞态条件是指两个线程或异步进程必须以正确的顺序完成并更新某些共享状态，否则会出现错误或意外结果。

### Q74
什么是函数式编程？
答案：一种使用声明式代码和纯函数的编程范式。

### Q75
什么是高阶函数？
A) 由多个函数或接口组成的函数
B) 可以接受函数作为参数，或者返回另一个函数的函数
C) 作为子对象超类的函数

答案是 B。

## 测试 2 答案

### Q1
考虑以下代码：
```typescript
class Person {
  firstName: string;
  lastName: string;
}
const myPerson = new Person();
console.log(myPerson.a);
```
解释原型链如何确定 `myPerson.a` 是 `undefined`？

浏览器检查 `myPerson.[[Prototype]]`，没有看到名为 `a` 的属性。然后浏览器检查 `myPerson.[[Prototype]].[[Prototype]]`（即 `Object` 原型），也没有看到名为 `a` 的属性。然后浏览器检查 `myPerson.[[Prototype]].[[Prototype]].[[Prototype]]`，它是 `null`，所以浏览器返回 `undefined`。

### Q2
JavaScript 中的 `class` 关键字有什么作用？
A) 它传达了超越普通对象的实际含义
B) 它是使 JavaScript 更面向对象的语法糖
C) 它创建了一个类似接口的对象，可用于继承

答案是 B。即使使用了 `class` 关键字，JavaScript 仍然使用原型继承。

### Q3
下面的代码会向控制台输出什么，为什么？
```javascript
let x = 10;
if(x){
  let x = 12;
  console.log(x);
}
```
A) 10
B) 12
C) 会抛出错误

答案是 B。内部的 `x` 优先于外部的 `x` 变量。

### Q4
判断对错？来自 `queueMicrotask` 队列的任务以后进先出的方式执行。
A) 正确
B) 错误

答案是 B。任务实际上以先进先出的顺序执行。

### Q5
对于这个函数，遵循“整洁代码”原则的名称会是什么？
```javascript
const pntDT = () => {
  const today = new Date();
  const time = today.getHours() + ":" + today;
  console.log(time);
};
pntDT();
```
有很多可能的函数名称可以更好地符合整洁代码原则。例如，`printDateAndTime()` 是一个更好的名称，因为它不会让人对函数的功能产生疑问。

### Q6
以下哪一项不是创建和注册新自定义元素的步骤？
A) 在 DOM 中创建一个 HTML 容器
B) 创建一个定义元素行为的 JavaScript 类
C) 使用 `CustomElementRegistry` 对象注册该类和一个表示元素名称的 `DOMString`

答案是 A。

### Q7
简要解释 Shadow DOM API。
Shadow DOM API 提供了一种将隐藏的独立 DOM 附加到元素上的方法，该 DOM 无法通过常规的 JS DOM 操作 API 访问。Shadow DOM 为 Web 组件提供了封装。隐藏的 DOM 树附加到常规 DOM 树中的元素上。

### Q8
哪个方法将影子 DOM 树附加到指定元素并返回对其 `ShadowRoot` 的引用？
A) `Element.shadowAdd()`
B) `Element.setDOMShadow()`
C) `Element.attachShadow()`

答案是 C。

### Q9
`arr[2][1]` 会返回什么值？
```javascript
const arr = [["a", "b", "c"],["d", "e", "f"],["g", "h", "i"]];
```
A) d
B) h
C) b
D) 以上都不是

答案是 B。首先，JavaScript 中的数组是从零开始的。因此，`arr[2][1]` 会访问外层数组的第 3 个元素和内层数组的第 2 个元素，返回值是 "h"。

### Q10
下面的代码会向 `<app>` 输出什么？
```javascript
document.getElementById("app").innerHTML = `<div>hewohewo2</div>`
```
A) hewo hewo2
B) hewohewo2
C) hewo hewo2
D) 无法编译

答案是 C。

### Q11
jQuery 使用什么模式来创建其全局可用的 jQuery 对象的单个实例？
A) OOP
B) 工厂模式
C) 单例模式
D) 无

答案是 C。全局创建了一个 jQuery 对象的实例。

### Q12
`window.localStorage` 和 `window.sessionStorage` 有什么区别？选择最佳答案。
A) `localStorage` 在 Web 浏览器中存储键/值对，并且 `localStorage` 在浏览器关闭后删除
B) `sessionStorage` 在 Web 浏览器中存储键/值对，并且 `sessionStorage` 在浏览器关闭后删除
C) 两者都在 Web 浏览器中存储键/值对，但 `localStorage` 在浏览器关闭后删除
D) 两者都在 Web 浏览器中存储键/值对，但 `sessionStorage` 在浏览器关闭后删除

答案是 D。

### Q13
下面的代码会向控制台输出什么，为什么？
```javascript
let arr1 = [1, 2, 3];
arr1.push(4);
arr1.pop();
arr1.slice(1, 2);
arr1.splice(1, 2);
console.log(arr1);
```
A) 1
B) [1]
C) [1,2]
D) [2,3]
E) 不打印任何内容。

答案是 B。

### Q14
判断对错：`!` 运算符返回一个布尔值。选择一个选项。
A) 正确
B) 错误

答案是 A。`!` 可以用于 `if` 语句等场景。`if` 语句需要在求值中返回布尔值，例如 `if(x !== y)`。

### Q15
评估下面的代码。如果 `div` 和 `button` 都有点击监听器，如何阻止按钮上的点击事件冒泡到 div？
```html
<div><button>Click Me!</button></div>
```
A) 在按钮的 `clickHandler` 中使用 `Event.stopPropagation`
B) 在 div 的 `clickHandler` 中使用 `Event.stopPropagation`
C) 在按钮的 `clickHandler` 中使用 `Event.stopBubble`
D) 在 div 的 `clickHandler` 中使用 `Event.stopBubble`

答案是 A。

### Q16
下面的代码会向控制台输出什么，为什么？
```javascript
let xyz = "";
xyz ||= "abc";
console.log(xyz);
```
A) abc
B) ‘’
C) 编译时错误

如果启用了实验性语法，答案是 A。否则，会出现编译时错误。

### Q17
下面两个函数的输出有什么区别？
```javascript
void function voidExample() {
  console.log("No Error!");
}();

function noVoidExample() {
  console.log("No Error!");
}();
```
A) 函数 `noVoidExample` 执行并打印 "No Error"，而 `voidExample` 抛出错误。
B) 函数 `voidExample` 执行并打印 "No Error"，而 `noVoidExample` 抛出错误。
C) 两者都抛出错误

答案是 B。`void` 关键字允许执行那些可能无法正常执行的函数。

### Q18
以下哪一项不是 `NodeList` 和 `Array` 的区别？
A) `NodeList` 是 Web API，`Array` 是 JavaScript API
B) `NodeList` 不能包含超过 10 个项目
C) `NodeList` 的属性可能是实时的，如果 DOM 更新（如 `childNode`），它们也会更新
D) 许多数组函数在 `NodeList` 上不可用

答案是 B。

### Q19
JavaScript 中哪些 ES6 数组函数返回一个新数组？选择所有正确的答案。
A) `map()`
B) `forEach()`
C) `filter()`
D) `find()`

答案是 A、C。

### Q20
JavaScript 使用 number 原始类型可以可靠表示的最大整数是多少？
A) 2⁵³ - 1
B) 2³² - 1
C) 2⁶³ - 1
D) JavaScript 可以表示无限大的数字

答案是 A。

### Q21
哪个函数会将字符串修改为符合 URI 规范？
A) `JSON.stringify()`
B) `encodeURI()`
C) `encodeString()`
D) `JSON.parse()`

答案是 B。

### Q22
在 JS 中，用于存储数字的 64 位是如何分配的？
答案：52 位用于数值，11 位用于指数，1 位用于符号。

### Q23
在计算机科学中，`null` 和 `undefined` 有什么区别？
`undefined` 表示变量没有值，因为开发者尚未设置。`null` 表示变量被有意设置为没有值。

### Q24
JavaScript 中减号（`-`）的技术名称是什么？
A) 一元减法
B) 二元否定
C) 一元否定
D) 二元减法

答案是 C。

### Q25
判断对错？`super` 关键字不能在构造函数之外使用。
A) 正确
B) 错误

答案是 B。例如，`super.functionOnParent([arguments])`。这用于在子对象覆盖了父对象的函数时，调用父对象上的函数。

### Q26
访问 `cat` 对象上的 color 值的两种方式是什么？
`const cat = {color: "orange"};`
答案：`cat.color` 和 `cat['color']`

### Q27
JavaScript 运行时中的栈是什么？
栈是一系列帧（函数调用）。最近的函数调用位于栈顶，必须执行并从栈中弹出，然后才能完成下一个函数调用。当一个函数调用另一个函数时，新调用的函数被放在栈顶。栈是后进先出的，这意味着最近添加的函数必须首先执行。

### Q28
十六进制转义序列的语法是什么？
A) ‘\zfg’
B) ‘\10ab’
C) ‘\x’

答案是 C。例如，`'\xB1'` 变成 "±"。

### Q29
编写代码，在原生 JavaScript（无 TypeScript）中创建一个自定义抽象类？`abstract` 关键字在 ES2015 中不可用。

示例答案：
```javascript
class MyAbstract {
  constructor() {
    if(new.target === MyAbstract) {
      throw new Error(‘Error Message’);
    }
  }
}
```

### Q30
下面的代码会向控制台输出什么，为什么？
```javascript
const badMap = new Map();
badMap.set('a', 1);
badMap.b = 2
console.log(badMap)
```
A) Map(1) {"a" => 1}
B) Map(1) {"b" => 2}
C) Map(2) {"a" => 1, “b” => 2}
D) 编译时错误

答案是 A。`badMap.b` 会在 `badMap` 对象上设置值 `b`，但 `b` 的设置方式没有正确与 `Map` 结构交互。

### Q31
面向对象编程（OOP）的好处有哪些？选择三个答案。
A) 代码是可插拔或模块化的，因此类的源代码可以独立于应用程序的其他代码进行维护。
B) 对象的代码保持私有，这意味着其他对象只与对象的方法交互，因此内部代码被隐藏。
C) 对象易于重用。它们可以插入到代码的多个部分。
D) 面向对象代码执行更快，计算机资源使用最小化。

答案是 A、B、C。

### Q32
假设 `const map` 有以下值：`Map(2) {"a" => 2, "b" => 2}`。用一行代码将 `map` 转换为二维数组。
答案：`[…map]` 或 `Array.from(map)` 都可以实现。

### Q33
判断对错？在 JavaScript 中，只有自定义类和对象可以被扩展？
A) 正确
B) 错误

答案是 B。例如，自定义类和对象扩展了 `Object`。任何内置对象都可以被扩展。

### Q34
判断对错？只要创建了实例，实例级变量就可以在类中的任何位置访问。
A) 正确
B) 错误

答案是 B。实例级变量不能在静态方法中访问。

### Q35
假设启用了 TypeScript。为什么下面的代码无法编译？选择一个选项。
```typescript
let i: number;
if(5%3>2){
  i=0;
} else if(5%3>1){
  i=1;
}
console.log(i);
```
A) 编译正常
B) 5%3>2 和 5%3>1 不返回布尔值，因此不能在 if 语句中使用
C) `i` 是一个局部变量，其值从未显式定义

答案是 A。TypeScript 可能会抱怨 `i` 在赋值之前被使用，但它会编译。

### Q36
判断对错？`length` 是字符串上的方法，是数组上的属性？
A) 正确
B) 错误

答案是 B。`length` 是字符串上的属性，是数组上的属性。

### Q37
`function.call` 的第一个参数是什么？
A) 被调用函数的参数
B) 不接受任何选项
C) 调用函数的实例对象

答案：调用函数的对象，例如 `person.fullName.call(person2);`，其中 `person2` 具有调用 `person.fullName` 函数所需的属性。可以将其视为设置作用域的一种方式。

### Q38
`printName` 这种函数的技术名称是什么？选择所有正确的选项。
```javascript
function getName() {
  var name = "Jon";
  function printName() {
    console.log(name);
  }
  printName();
}
getName();
```
A) 内部函数
B) 包含函数
C) 闭包

答案是 A、C。

### Q39
判断对错？箭头函数只有在有多个参数时才需要括号。
A) 正确
B) 错误

错误。箭头函数在零个参数时也需要括号。如果只有一个参数，括号是可选的。

### Q40
判断对错？类级变量可以在类中的任何位置访问。
A) 正确
B) 错误

答案是 A。类级变量，也称为静态变量，可以在任何方法中访问，包括静态方法和构造函数。

### Q42
当你尝试给 `const` 赋值新值时，会抛出什么类型的错误？
A) ReferenceError
B) Error
C) RangeError
D) TypeError

答案是 D。

### Q43
重写和重载是哪种面向对象编程原则的例子？
A) 继承
B) 抽象
C) 多态
D) 封装

答案是 C。

### Q44
判断对错：静态变量不能在非静态方法中修改？
A) 正确
B) 错误

答案是 B。非静态方法可以使用 `Class.Static` 语法引用和修改静态变量，如下所示。
```javascript
class Test {
  static MAX = 10;
  getMax() {
    Test.MAX = 12;
    console.log(Test.MAX);
  }
}
```

### Q45
如果 `str === 'test1'`，下面的代码会发生什么？
```javascript
switch (str) {
  case "test1":
  case "test2":
    console.log("At test2");
}
```
A) 打印 "At test2"
B) 什么都不做
C) 运行时错误

答案是 A。如果没有指定 `break`，匹配后会穿透所有剩余的 case，直到遇到 `break` 关键字。

### Q46
当 JavaScript 被描述为拥有“一等函数”时，这意味着什么？
A) 函数可以是递归的
B) 函数可以是匿名的
C) 函数被当作任何其他变量一样对待
D) 函数使用花括号语法

答案是 C。这允许函数作为参数传递、从函数返回等。

### Q47
判断对错？下面的代码可以编译。
```javascript
async function promiseMe() {
  try {
    let z = await Promise.reject(30);
  }
}
```
A) 正确
B) 错误

答案是 B。拒绝一个原始值不是问题。但是，`try` 没有对应的 `catch` 或 `finally` 是有问题的。

### Q48
判断对错？`Date.getDate()` 返回月份中的日期，值为 1-31，而 `Date.getDay()` 返回星期中的天数，值为 0-6。
A) 正确
B) 错误

答案是 A。

### Q49
异步操作被放入什么类型的队列？
A) 阻塞队列
B) 事件队列
C) 异步队列

答案是 B。

### Q50
JavaScript 长期以来提供了哪三个函数用于在时间过后执行代码？选择三个答案。
A) `setTimeout()`
B) `setInterval()`
C) `callAsyncLoop()`
D) `requestAnimationFrame`

答案是 A、B、D。

### Q51
如果你想测量代码块的执行时间，可以调用哪个 Web API？
A) `window.now()`
B) `window.timer()`
C) `performance.now()`
D) `performance.timer()`

答案是 C。例如：
```javascript
const t0 = performance.now();
runFunction();
const t1 = performance.now();
console.log(t0 - t1);
```

### Q52
什么是 MIME 类型？
MIME 类型是随文件一起发送的字符串，指示文件类型。例如，JSON 文件发送的 MIME 类型是 `‘application/json’`。

### Q53
导出以下变量的简单语法是什么？
`let myLet = 10;`
答案：`export let myLet = 10;`

### Q54
哪个函数属性返回函数期望的参数数量？
A) `Function.argsLength`
B) `Function.length`
C) `Function.parameters`

答案是 B。

### Q55
“仅为了副作用而导入模块”是什么意思？
答案：导入模块时不指定要导入的任何内容，即
`import '/someLib/my-class.js';`

### Q56
判断对错？下面的代码编译并打印 3？
```javascript
const test = () => {
  return1 + 2;
}
console.log(test());
```
A) 正确
B) 错误

答案是 B。如果省略分号，编译器会自动在 `return` 语句后放置分号。

### Q57
判断对错？以下两者等价。
`var a, z = 1; a = z;`
和
`var a = z = 1;`
A) 正确
B) 错误

答案是 B。`z` 被全局声明。

### Q58
判断对错？下面的代码返回 3。
```javascript
const arr = [1, 2];
const reduced = arr.reduce((accumulator,element) => accumulator);
```
A) 正确
B) 错误

答案是 B。累加器没有使用 `+=` 返回。下面的语句会得到期望的结果：
`const reduced = arr.reduce((accumulator, element) => accumulator + element);`

### Q59
`"use strict";` 指令必须放在文件的什么位置？
A) 顶部
B) 中间
C) 底部
D) 作为导入

答案是 A。

### Q60
如何在原生 JavaScript（无 TypeScript）中使用组合？
一个例子：创建不是任何对象方法的函数。使用 `Object.assign(obj)` 将所需的函数作为方法分配给 `obj`。

### Q61
下面的代码会向控制台输出什么，为什么？
```javascript
for(let i = 1, j = 10; i < 5 < j; i += j/i){
  console.log(Math.ceil(++i));
}
```
A) 什么都不输出
B) 除以零错误
C) 1, 12
D) 会进入无限循环

答案是 D。`i < 5 < j` 会这样求值：`(i < 5) < j`。在上面的代码中，第一次迭代时 `i < 5` 为 false。然后 `false < j` 求值为 true。

### Q62
展示如何在不使用冒号 `:` 的情况下构造对象字面量。
```javascript
let a = 1, b = 2, c = 3;
let obj = { a, b, c }
```

### Q63
JavaScript 中数组的最大大小是多少？
A) 2¹⁶ - 1
B) 2³² – 1
C) 2¹⁶
D) 2³²

答案是 B。如果你尝试设置超过 2³² – 1 的值，你会得到 `RangeError`。

### Q64
如果一个函数被调用时传入的参数少于声明的参数数量，缺失的参数会被赋予什么值？
A) null
B) undefined
C) 0

答案是 B。

### Q65
什么是事件捕获阶段？
事件从祖先元素（`window`、`div` 等）向下传递到最具体元素的阶段。

### Q66
判断对错？Setter 在冻结对象上仍然有效。
A) 正确
B) 错误

答案是 B。Setter 仍然存在并且可以被调用，但它们实际上不会改变值。

### Q67
`3 > 2 > 1` 返回什么？
A) true
B) false
C) 0

答案是 B。`3 > 2` 求值为 `true`。然后 `true > 1` 求值为 `false`。

### Q68
下面两段代码返回相同的值。它们发生的方式有什么区别？
`‘123’.length;` //第 1 行
`new String(123).length;` //第 2 行
A) 第 1 行使用显式强制转换，第 2 行使用隐式强制转换
B) 第 1 行使用隐式强制转换，第 2 行使用显式强制转换
C) 没有区别

答案是 B。

### Q69
以下哪种情况不是使用匿名函数的时机？
A) 作为类方法
B) 在闭包中
C) 作为回调
D) 作为 IIFE（立即调用函数表达式）

答案是 A。

### Q70
在 Web 浏览器中，布局时间和绘制时间有什么区别？
布局时间是计算每个要绘制的对象位置所需的时间。绘制时间是实际在屏幕上绘制点所需的时间。

### Q71
下面的代码会向控制台输出什么，为什么？
```javascript
let a = 8
a >>>= 3;
console.log(a);
```
A) 1
B) 10
C) 4

答案是 A。`>>>=` 被称为无符号右移赋值运算符。

### Q72
下面的代码会向控制台输出什么，为什么？
`console.log([1, 2,,3].join(', '));`
A) lint 错误
B) 1, 2, 3
C) 1, 2, , 3

答案是 C。数组可以有空白位置。

### Q73
给出一个避免网络调用竞态条件的例子。
一个可能的答案：创建取消令牌或在网络调用中使用取消 API。当你发出新请求时，取消之前的请求。

### Q74
什么是纯函数？
答案：给定相同的输入，总是返回相同输出且没有副作用的函数。

### Q75
什么是柯里化？
答案：将具有多个参数的单个函数转换为多次调用、每次只接受一个参数的函数。

## 测试 3 答案

### Q1
判断对错？编译器会为下面的代码抛出错误。
```javascript
const x = 10;
x = 12;
```
A) 正确
B) 错误

答案是 A。`const` 关键字表示一个不能更改的值。

### Q2
下面代码的 TypeScript 类型是什么？
`const x = “hello”`
A) "hello"
B) const
C) string
D) 没有分配类型

答案是 A。由于 `const` 值不能更改，类型可以锁定为实际的字符串字面量值。

### Q3
下面的代码会向控制台输出什么，为什么？
```javascript
let person = {age: 25,name: 'Justin'}
const byRef = (myObj) => {
  myObj.age = 30
}
byRef(person);
console.log(person.age);
```
A) 25
B) 30
C) 编译时错误

答案是 B。内存中 `person` 对象的引用被传递给了 `byRef` 函数。

### Q4
下面的代码会向控制台输出什么，为什么？
```javascript
let x;
if(x = true === true){
  console.log(x);
} else {
  console.log('Not x');
}
```
A) true
B) false
C) Not x
D) 编译时错误

答案是 A。变量可以在 `if` 语句的求值中被赋值。

### Q5
下面的代码会向控制台输出什么，为什么？
```javascript
let x = 10;
function myFunc(y){
  y = 12;
}
console.log(myFunc(x));
```
A) 10
B) 12
C) undefined

答案是 C。`myFunc` 没有返回值。

### Q6
假设下面的聚合函数计算你的年龄天数、组合你的名和姓、并拆分你的地址。选择所有它违反整洁代码原则的方式。
`const aggregator = (DOB, firstName, lastName, address, skills) => {...}`
A) 函数命名不当
B) 函数应该使用 `function` 关键字而不是 lambda 函数
C) 函数做了太多事情，应该被拆分
D) 函数没有对 `skills` 参数做任何操作

答案是 A、C、D。

### Q7
从 JS 的角度来看，DOM 的技术定义是什么？
来自 MDN Web 文档：DOM 是“一个由连接节点组成的树状结构，表示标记文档中出现的不同元素和文本字符串”。

### Q8
给定 `FancyButton` 类，如何扩展 button 来创建一个名为 `fancy-button` 的自定义元素？
A) `customElements.extend('fancy-button', FancyButton, { extends: 'button' });`
B) `customElements.extend('fancy-button', FancyButton, { implements: 'button' });`
C) `customElements.define('fancy-button', FancyButton, { extends: 'button' });`
D) `customElements.define('fancy-button', FancyButton, { implements: 'button' });`

答案是 C。

### Q9
以下哪个是正确的字符串插值语法？
`const x = ‘me’;`
A) `` `Pick ${x}` ``
B) `` `Pick &{x}` ``
C) ‘Pick ${x}’
D) ‘Pick &{x}’

答案是 A。

### Q10
将对象实例总数限制为一个的模式名称是什么？
A) 单例模式
B) 工厂模式
C) 设计模式
D) OOP

答案是 A。

### Q11
以下哪个不是 `Set` 对象上的方法？
A) `add()`
B) `next()`
C) `clear()`
D) `delete()`
E) `entries()`

答案是 B。

### Q12
哪个 window 方法允许你在浏览器内存中存储持久的键/值对？
A) `window.browserStorage`
B) `window.localStorage`
C) `window.persistentStorage`
D) 没有这样的方法

答案是 B。

### Q13
所有位运算都是在多少位的二进制数上执行的？
A) 8
B) 16
C) 32
D) 64

答案是 C。

### Q14
`delete` 运算符在什么时候不会从对象中移除属性？
当对象被创建为不可配置时，如下所示：
```javascript
var Car = {};
Object.defineProperty(Car, 'name', {configurable: false})
```

### Q15
如果你需要获取对象的属性，应该调用哪个方法？
A) `Object.getKeyValues`
B) `Object.getList`
C) `Object.getNames`
D) `Object.getOwnPropertyNames`

答案是 D。例如：
```javascript
const xy = {a: 1, b: 2};
console.log(Object.getOwnPropertyNames(xy));
```

### Q16
下面的代码会向控制台输出什么，为什么？
`console.log(2 * 3 ** 3);`
A) 216
B) 18
C) 54
D) 编译时错误

答案是 C。`**` 是指数运算符，优先级高于 `*`。

### Q17
评估下面的代码。一个字符的更改可以防止这一行抛出错误？
```javascript
const dog = {color: "brown",breed: {pure: true}};
console.log(dog.hair.short);
```
答案：将 `console.log(dog.hair.short);` 改为 `console.log(dog.hair?.short);`。这称为可选链。

### Q18
哪些数组函数在 `NodeList` 上不可用？选择所有适用的。
A) `forEach()`
B) `join()`
C) `filter()`
D) `map()`

答案是 A。

### Q19
以下哪个不是 JSON 方法？
A) `reverse()`
B) `parse()`
C) `stringify()`

答案是 A。`JSON` 对象只有两个方法：`parse` 和 `stringify`。

### Q20
判断对错？JavaScript 中有一个全局的 `Map` 对象。
A) 正确
B) 错误

答案是 A。不要与 `Array.map()` 混淆。

### Q21
`WeakSet` 对象中的“弱”是什么意思？
来自 MDN 文档：“如果存储在 `WeakSet` 中的对象没有其他引用，这些对象可以被垃圾回收。”

### Q22
克服浮点数不精确性的一种方法是什么？
A) 乘法和除法
B) 它本身就可以工作
C) 通过扩展函数运行

答案是 A。例如：`const x = (0.1 * 10 + 0.1 * 10) / 10;`

### Q23
评估下面的代码。如何重构它以使用更少的代码？
```javascript
const temp = object.prop1;
const test = ((temp === null || temp === undefined)) ? undefined : temp.prop2;
```
一个可能的答案：`object.prop1?.prop2;`

### Q24
评估下面的代码。循环的第一个和最后一个输出是什么？
```javascript
for(let i = 0; i <= 10; ++i){
  console.log(i);
}
```
A) 0, 9
B) 0, 10
C) 1, 9
D) 1, 10

答案是 B。

### Q25
在下面的 `MyChild` 类上创建一个函数，调用父类的 `printSomething` 方法。
```javascript
class MyParent {
  constructor(){}
  printSomething(){
    console.log(5);
  }
}
class MyChild extends MyParent {
  constructor(){
    super()
  }
  printSomething(){
    console.log(10);
  }
}
```
一个示例答案：
```javascript
printSomethingOld(){
  super.printSomething()
}
```

### Q26
下面的代码返回什么，为什么？
`const value = 10 / -0;`
A) NaN
B) -NaN
C) Infinity
D) -Infinity

答案是 D。

### Q27
JavaScript 运行时中的堆是什么？
堆是存储对象的内存区域。

### Q28
当在字符串字面量值上调用 `String` 对象方法时，JavaScript 在幕后如何处理？
答案：JavaScript 自动将字符串字面量转换为临时的 `String` 对象，调用方法，然后丢弃临时的 `String` 对象。

### Q29
下面的代码会向控制台输出什么，为什么？
```javascript
const obj = {a: 1,b: 2};
const arr = [];
console.log(arr[0] = {…obj});
```
A) 1, 2
B) {…obj}
C) {a: 1, b: 2}
D) 无法编译

答案是 C。`…` 语法被称为展开运算符。

### Q30
`Map.delete(key)` 返回什么？
A) 没有返回值
B) 总是 true
C) 总是 false
D) 如果键被删除则返回 true，如果项目不存在且未被删除则返回 false

答案是 D。

### Q31
以下哪一项不是使用 TypeScript 时继承的例子？选择一个选项。
A) 对象具有其超类拥有的字段
B) 对象具有其超类拥有的方法
C) 对象具有其接口拥有的方法
D) 对象具有其超类拥有的静态字段

答案是 C。接口是一种组合形式，而不是继承。

### Q32
判断对错？在 JavaScript 中，一个对象只能有一个子类，但可以有无限多个父类。
A) 正确
B) 错误

答案是 B。一个对象只能有一个父类，但可以有无限多个子类。

### Q33
判断对错？一个对象可以实现多个接口。假设启用了 TypeScript。
A) 正确
B) 错误

答案是 A。

### Q34
下面的代码打印什么？选择一个选项。
```javascript
class MyClass {
  static staticMethod() {
    return this.name;
  }
  constructor() {
    this.name = 'Jon';
  }
}
const me = new MyClass();
console.log(MyClass.staticMethod());
```
A) Jon
B) MyClass
C) 编译时错误
D) 运行时错误

答案是 B。`staticMethod` 中的 `this` 关键字的作用域不是实例级别。

### Q35
判断对错？`String` 是一种原始数据类型。
A) 正确
B) 错误

答案是 A。

### Q36
展示两种使现有数组为空的方法。
两个可能的答案：`array.length = 0`，`array.splice(0, array.length)`

### Q37
代码执行后 `str` 的值是什么？
`const str = "  this".concat("that   ").substring(3).trim().valueOf(2);`
A) 2
B) h
C) histhat
D) 无法编译

答案是 C。

### Q38
JavaScript 中的生成器函数是什么？
答案：生成器是可以退出并在之后重新进入的函数。

### Q39
以下哪个是类的有效修饰符，假设启用了 TypeScript？选择一个选项。
A) private
B) final
C) abstract
D) public
E) default

答案是 C。

### Q40
以下哪个不是 Java 中的保留字？选择一个选项。
A) abstract
B) compile
C) do
D) enum

答案是 B。

### Q41
这段代码的输出是什么？
```javascript
class TestClass{
  constructor() {
    this.myInt = 5;
  }
  mainMethod(){
    const test = new TestClass();
    test.myInt = 6;
    console.log(test.incrementIntAgain(test.incrementInt(test.myInt)));
  }
  incrementInt (theirInt) {
    return theirInt++;
  }
  incrementIntAgain (theirInt) {
    return ++theirInt;
  }
}
```
A) 5
B) 6
C) 7
D) 8

答案是 C。

### Q42
```java
Package Exam;
public class Tester{
  private int myInt = 5;
  public static void main(String []args){
    Tester test = new Tester();
    test.myInt = 6;
    System.out.println(test.incrementIntAgain(test.incrementInt(test.myInt)));
  }
  public int incrementInt (int theirInt) {
    return theirInt++;
  }
  public int incrementIntAgain (int theirInt) {
    return ++theirInt;
  }
}
```
这段代码的输出是什么？
A) 5
B) 6
C) 7
D) 8

答案是 C。

### Q43
判断对错：实例级对象可以访问静态变量？
A) 正确
B) 错误

答案是 B。静态变量只能直接从类访问，即 `Class.StaticVar`。

### Q44
下面的代码向控制台输出什么，为什么？
```javascript
function Dog(name) {
  this.name = name;
}
const buddy = new Dog("buddy");
const rover = Object.create(buddy);
console.log(Object.getPrototypeOf(rover));
console.log(Object.getPrototypeOf(buddy));
```
答案：`Dog {name: "buddy"}` 和 `Dog` 类的引用。

### Q45
下面的代码向控制台输出什么，为什么？
`let x = (1, 2, 3); console.log(x);`
A) 1
B) 2
C) 3
D) 编译时错误

答案是 C。逗号分隔符返回最后一个值。

### Q46
`RegExp` 字面量表示法和构造函数之间的一些区别是什么？选择所有适用的。
A) 字面量表示法的参数用斜杠括起来，没有引号
B) 字面量表示法在编译时求值
C) 构造函数不使用斜杠，但使用引号
D) 构造函数在运行时求值

以上所有都是正确的。

### Q47
打印顺序是什么？
```javascript
function resolveQuickly(x) {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log(x)
    }, 1);
  });
}
async function asyncTest() {
  var x = resolveQuickly(10);
  console.log(5);
}
asyncTest();
```
A) 10, 5
B) 5, 10
C) 什么都不打印。

答案是 B。

### Q48
JavaScript 这个名字从何而来？
JavaScript 最初于 1995 年在 Netscape 开发，原本应该叫 LiveScript。然而，由于 Java 是一种流行的语言，名字被改成了 JavaScript。

### Q49
以下哪一项不是 Promise 相对于旧式回调的优势？
A) 执行速度
B) `.then()` 链式调用
C) Promise 回调总是按照它们在事件队列中放置的顺序被调用
D) 更好的错误处理
E) Promise 避免了控制反转

答案是 A。

### Q50
判断对错？`do-while` 循环总是至少执行一次。
A) 正确
B) 错误

答案是 A。

### Q51
展示一个递归调用 `setTimeout` 来模拟 `setInterval` 的例子。
```javascript
setTimeout(function recur() {
  console.log('called me');
  setTimeout(recur, 1000);
}, 1000);
```

### Q52
JSON 支持哪些数据类型？选择所有合适的答案。
A) 字符串
B) 数字
C) 对象
D) null
E) 数组
F) 布尔值

以上所有都是正确的。

### Q53
将 `theFunction` 作为默认导出的两种语法是什么？
答案：
`export { theFunction as default };`
`export default function theFunction () { ... }`

### Q54
函数声明和函数表达式在语法上有什么区别？
答案：
```javascript
function myFunc() {
  console.log('hoisted');
}
var myFunc2 = function () {
  console.log('not hoisted')
}
```

### Q55
判断对错？`import` 可以作为函数调用。
A) 正确
B) 错误

答案是 A。`import` 可以动态调用，并返回一个 promise。

### Q56
下面的代码向控制台打印什么，为什么？
```javascript
console.log(x)
x = 5;
if(x){
  var x = 10;
  console.log(x);
}
```
A) 5, 10
B) 10, 10
C) 5, 5

答案是 B。

### Q57
`Array.reduce()` 的目的是什么？
A) 将数组减少为回调
B) 将数组减少为复合函数
C) 将数组减少为单个值。

答案是 C。

### Q58
什么是记忆化？
A) 通过缓存先前计算的结果来提高函数性能
B) JavaScript 中不可用的东西
C) 为将来使用对象而创建对象属性的组合

答案是 A。

### Q59
在 JavaScript 中创建一个抽象类的例子。
答案：只有在启用了 TypeScript 或其他类型超集时才能创建抽象类。
```typescript
abstract class Printer {
  constructor() {}
  print1(): void {
    console.log("printing");
  }
  abstract print2(): void;
}
```

### Q60
给出一个使用 `String.prototype.match` 通过正则表达式运行字符串的例子。
一个可能的答案：
```javascript
const sentence = 'Heyo!';
const regex = /[A-Z]/g;
console.log(sentence.match(regex));
```

### Q61
下面的代码会向控制台输出什么，为什么？
```javascript
for(let i = 6; i > 0; i-=2){
  if(i%2){
    continue;
  }
  console.log(i)
}
```
A) 什么都不输出
B) 4, 2, 0
C) 6, 4, 2
D) 4, 2

答案是 C。

### Q62
判断对错？对象上重复的属性名被认为是语法错误。
A) 正确
B) 错误

答案是 B。自 ECMAScript 2015 起，这不再是错误。

### Q63
判断对错？以下是错误的语法。
```javascript
function foo(arg) {
  let arg = 1;
}
```
A) 正确
B) 错误

答案是 A。这被称为形式参数的重声明。

### Q64
包含传递给函数的所有对象值的类数组对象的名称是什么？
A) `arguments`
B) `args`
C) `params`
D) `parameters`

答案是 A。

### Q65
下面代码中的第三个参数 `true` 是用来做什么的？
`element.addEventListener("click", e => console.log(element.eventPhase), true);`
A) 启用捕获阶段的事件捕获
B) 启用冒泡阶段的事件捕获
C) 在 `addEventListener` 函数中不使用

答案是 A。

### Q66
在考虑强制转换时，什么是包装对象？
为了“赋予”原始类型属性而包裹在原始类型周围的对象。例如：
```javascript
const str = ‘123’;
console.log(str.length); //返回 3
```

### Q67
`3 > 2 == 1` 返回什么？
A) true
B) false
C) 0

答案是 A。`3 > 2` 返回 `true`，`true == 1` 返回 `true`。

### Q68
JavaScript 如何在布尔上下文中评估值或对象的真值或假值？
A) 类型强制转换
B) 它是每个对象上的一个属性
C) 某些值永远没有真值或假值

答案是 A。

### Q69
使用 IIFE 的目的是什么？选择所有可能的答案。
A) 设置变量值
B) 初始化对象上的值
C) 在闭包中用于初始化值
D) 运行一次性函数

答案是 A、C、D。

### Q70
什么是词法作用域的例子？选择所有可能的答案。
A) 基于变量输入动态定义的作用域
B) `let self = this;` //在父函数中，然后 `self` 对内部函数可用
C) 内部函数的作用域包含父函数的作用域

答案是 B、C。

### Q71
下面的代码会向控制台输出什么，为什么？
```javascript
let a = 3;
a <<= 1;
console.log(a);
```
A) 3
B) 4
C) 6
D) 8

答案是 C。

### Q72
下面的代码会向控制台输出什么，为什么？
```javascript
badCode = () => {
  let arr = [1,2,3,4];
  const inner = () => {
    return arr.pop(2)
  }
  return inner;
}
console.log(badCode()());
```
A) lint 错误
B) 3, 4
C) 34
D) 4

答案是 D。`pop` 不接受任何参数。

### Q73
下面的代码会向控制台输出什么，为什么？
```javascript
const obj = { a: 1 };
let obj2 = obj;
obj2.a = 2;
console.log(obj.a);
```
A) 1
B) 2
C) undefined

答案是 B。

### Q74
编程中的副作用是什么？
答案：副作用是指函数修改了影响应用程序其他部分的状态或可观察值。

### Q75
判断对错？`Array.prototype.filter()` 返回一个包含所有未通过提供的函数测试的项的数组。
A) 正确
B) 错误

答案是 B。

## 测试 4 答案

### Q1
判断对错？评估下面的代码。`bark()` 现在是 `Dog` 类上的一个函数。
```javascript
class Dog {
  noise: string;
  legs: number;
}
Dog.bark = () => {
  console.log('woof');
}
let dog = new Dog();
dog.bark();
```
A) 正确
B) 错误

答案是 B。正确的语法是 `Dog.prototype.bark`。

### Q2
判断对错？评估下面的代码。`bark()` 现在是 `Puppy` 类上的一个函数。
```javascript
class Dog {
  noise: string;
  legs: number;
}
Dog.prototype.bark = () => {
  console.log('woof');
}
class Puppy extends Dog {
  pottyTrained: boolean;
}
let dog = new Puppy();
dog.bark();
```
A) 正确
B) 错误

答案是 A。

### Q3
评估下面的代码。`getDOB` 函数有什么问题？本题启用了 TypeScript。
```typescript
const getDOB = (firstName: string, lastName: string) => {
  return `${firstName} ${lastName}`
}
```
A) `getDOB` 在字符串插值中有错误的语法
B) 参数的类型错误
C) 它返回 undefined
D) 命名不当

答案是 D。

### Q4
以下哪个是自定义元素的控制器？
A) `CustomHTML` 对象
B) `HTMLElementRegistry` 对象
C) `CustomController` 对象
D) `CustomElementRegistry` 对象

答案是 D。

### Q5
自定义元素应该扩展哪个类？
A) `DOMElement`
B) `HTMLElement`
C) `CustomElement`

答案是 A。

### Q6
下面的代码会向控制台输出什么，为什么？
`let x = 2.2 + 4.4 === 6.6; console.log(x);`
A) undefined
B) True
C) False
D) 无法编译
E) 6.6

答案是 C。

### Q7
下面的 pre-es6 代码会向控制台输出什么，为什么？未启用 TypeScript。
```javascript
function SomeClass() {
  this.publicVar = 10;
}
SomeClass.staticVar = 10;
const myClass = new SomeClass();
myClass.publicVar = 12;
myClass.staticVar = 15;
const myClass2 = new SomeClass();
console.log(myClass2.publicVar);
console.log(myClass2.staticVar);
console.log(SomeClass.staticVar);
```
A) 10, undefined, 12
B) 10, 12, 12
C) 10, 15, 15
D) 12, undefined, 10
E) 10, undefined, 10

答案是 E。

### Q8
编写一个函数，用一行代码打印下面字符串中的不同元音字母。
`const str = "abcdeeef";`
一个可能的答案：`console.log(...new Set(str));`

### Q9
下面的代码会向控制台输出什么，为什么？
`console.log(Math.floor(2.1) === new Float32Array(2.1));`
A) True
B) False
C) 编译时错误

答案是 B。

### Q10
下面的代码会向控制台输出什么，为什么？
`console.log(Math.sin(Math.PI) === 0);`
A) True
B) False

答案是 B。`Math.PI` 是一个近似值。

### Q11
下面的代码会向控制台输出什么，为什么？
```javascript
z = 10;
console.log(z);
```
A) 10
B) 编译时错误
C) z

答案取决于严格模式。如果未启用，答案是 A。如果启用，答案是 B。

### Q12
下面的代码会向控制台输出什么，为什么？
```javascript
let max;
const numberArray = [3, 5, 2];
numberArray.forEach((element) => {
  if (max < element) {
    max = element;
  }
});
console.log(max);
```
A) 3
B) 5
C) 2
D) undefined

答案是 D。

### Q13
哪个位运算符反转 32 位数字的位？
A) `>>`
B) `|`
C) `&`
D) `~`

答案是 D。

### Q14
哪个运算符可以从对象中移除属性？
A) remove
B) delete
C) return
D) configure

答案是 B。

### Q15
访问下面 getter 的正确语法是什么？
```javascript
const obj = {
  count: [1, 2, 3],
  get last() {
    return this.count.pop();
  }
};
```
A) `obj.get(last)`
B) `obj.getLast`
C) `obj.last`

答案是 C。

### Q16
什么时候可能会使用 `new.target`？
当你想要在类或某些函数没有使用 `new` 关键字调用时抛出特定错误时。

### Q17
你会使用哪个方法将 nodelist 转换为数组？
A) `Array.to()`
B) `Array.from()`
C) `NodeList.to()`
D) `NodeLIst.from()`

答案是 B。

### Q18
判断对错？有两种 `NodeList`：静态和动态。
A) 正确
B) 错误

答案是 A。

### Q19
`Atomics` 不与哪个对象一起使用？
A) Buffer
B) `SharedArrayBuffer`
C) `ArrayBuffer`

答案是 A。

### Q20
哪种 JavaScript 错误类型通常用作自定义错误对象的基础？
A) ReferenceError
B) SyntaxError
C) TypeError
D) Error

答案是 D。

### Q21
哪个属性保证无论环境如何都能访问全局对象？
A) self
B) `globalThis`
C) this
D) window

答案是 B。

### Q22
关于 `undefined`，以下哪一项是不正确的？
A) 它是全局对象的一个属性
B) 它是全局作用域中的一个变量
C) `undefined` 的初始值是原始值 `undefined`
D) 它有一个名为 `Undefined` 的对应对象

答案是 D。

### Q23
判断对错？可选链可以像下面这样堆叠？
`let stateStats = state.area?.land?.sqmiles;`
A) 正确
B) 错误

答案是 A。

### Q24
下面的代码会向控制台输出什么，为什么？
```javascript
const a;
a.test ??= 25;
console.log(a.test);
```
A) undefined
B) 25
C) 编译时错误

答案是 C。

### Q25
JavaScript 中括号 `()` 的技术名称是什么？
A) 分组运算符
B) 括号运算符
C) 绑定运算符

答案是 A。

### Q26
下面的代码向控制台输出什么，为什么？
```javascript
let str = new String('aaa');
str.concat('bbb').concat('ccc');
console.log(str);
```
A) aaa
B) aaabbbccc
C) ccc
D) bbbccc

答案是 A。`concat` 返回一个新字符串。

### Q27
JavaScript 运行时中的队列是什么？
队列是要处理的消息列表。队列是先进先出的，意味着最旧的消息先被处理。

### Q28
判断对错？原生 JavaScript（无 TypeScript）从 ES2015 开始就有抽象类。
A) 正确
B) 错误

答案是 B。

### Q29
下面的代码会向控制台输出什么，为什么？
```javascript
const b = {a: 1,b: 2,3: 3}
for(key in b){
  console.log(b[key]);
}
```
A) 1 2 3
B) 1 2
C) Uncaught SyntaxError: Unexpected number

答案是 C。在 JavaScript 中，键必须是字符串。

### Q30
用多个键/值对初始化 `Map` 对象的语法是什么？
答案：创建一个新的 `Map` 对象，并用一个二维数组的键/值对初始化。例如：`const map = new Map([['a',1], ['b',2],['c',3]]);`

### Q31
判断对错？一个接口可以扩展另一个接口。假设启用了 TypeScript。
A) 正确
B) 错误

答案是 A。

### Q32
判断对错？假设启用了 TypeScript。一个对象继承其父类的所有字段和方法。
A) 正确
B) 错误

答案是 B。对象不会继承具有 `private` 修饰符的字段和方法。

### Q33
以下哪些是 TypeScript 接口方法的有效修饰符？选择所有正确的答案。
A) public
B) protected
C) private
D) abstract
E) 以上都不是。

答案是 E。

### Q34
判断对错？`static` 关键字在 JavaScript 中不是有效的修饰符。相反，需要像 TypeScript 这样的类型超集才能使 static 工作。
A) 正确
B) 错误

答案是 B。

### Q35
哪一行代码块将打印以下字符：☃⌨ ὀ˿
一个可能的答案：`console.log(String.fromCodePoint(9731, 9000, 8000, 0x2FF));`

### Q36
数组中的位置 3 有什么（如果有的话）？
```javascript
const arr = [1, 2];
arr.length = 3;
```
A) 它是空的
B) 它实际上没有被创建
C) null

答案是 A。

### Q37
写一个一行代码的例子来反转 `array.reduce` 函数。
答案：实际上有一个内置的数组函数叫做 `Array.reduceRight`。

### Q38
箭头函数的一些限制是什么？选择所有正确的选项。
A) 箭头函数不应作为方法使用
B) 箭头函数没有 `arguments`、`super` 或 `new.target` 关键字
C) 箭头函数不能在函数体中使用 `yield` 关键字
D) 箭头函数不能用作构造函数

答案是以上所有。

### Q39
传统函数和箭头函数的默认作用域有什么区别？
答案：传统函数默认 `this` 指向 window 作用域。箭头函数在其创建的作用域中执行。

### Q40
关于访问修饰符，以下哪些通常是正确的？
A) 字段应具有尽可能窄的访问修饰符
B) 方法应具有尽可能宽的访问修饰符
C) 除非字段是常量，否则避免使用公共字段

答案是 A、C。

### Q41
如果你在 `for` 循环中忘记了一个括号，会抛出什么类型的错误？
A) SyntaxError
B) TypeError
C) ReferenceError

答案是 A。

### Q42
判断对错？下面的代码是重载的例子。
`console.log({a: 1}.toString = 'Test');`
A) 正确
B) 错误

答案是 B。这里覆盖了默认的 `toString` 方法。

### Q43
判断对错？JavaScript 支持类上的静态变量。
A) 正确
B) 错误

答案是 A。

### Q44
给出一个使用新的 ES6 语法创建父/子关系的例子。
```javascript
let dog = { name: "buddy", legs: 4 };
let animal = { type: "mammal" };
Object.setPrototypeOf(dog, animal);
console.log(Object.getPrototypeOf(dog));
```

### Q45
判断对错？`try` 语句必须始终后跟至少一个 `catch` 语句。
A) 正确
B) 错误

答案是 B。`try` 语句后面可以跟一个 `finally` 语句。

### Q46
判断对错？当 `RegExp` 会变化时使用 `RegExp` 字面量表示法，当 `RegExp` 保持不变时使用 `RegExp` 构造函数。
A) 正确
B) 错误

答案是 B。

### Q47
判断对错？Promise 在 JavaScript 中是异步的。
A) 正确
B) 错误

答案是 B。Promise 是同步的，但它们经常做异步的事情。

### Q48
Web Workers 的目的是什么？
A) 在与主线程不同的线程上执行昂贵的任务
B) 将事件卸载到不同的对象
C) 加速原型继承

答案是 A。

### Q49
`Promise.resolve()` 返回什么类型的对象？
答案：一个处于已解决状态且具有给定解决值的 promise。

### Q50
`setTimeout()` 和 `setInterval()` 有什么区别？选择两个选项。
A) `setTimeout` 在指定时间过后执行一次
B) `setInterval` 以给定的延迟重复执行
C) `setTimeout` 以给定的延迟重复执行
D) `setInterval` 在指定时间过后执行一次

答案是 A、B。

### Q51
判断对错？`setInterval` 的间隔时间包括执行代码所花费的时间。
A) 正确
B) 错误

答案是 A。

### Q52
判断对错？下面的代码可以编译。
```javascript
const array = [1, 2, 3];
for (let i = 0; i < array1.length; array1[i++] = String.fromCharCode(96 + i));
```
A) 正确
B) 错误

答案是 A。

### Q53
导入默认导出与导入命名（非默认）导出有什么区别？
A) 花括号
B) 默认导出中从不包含名称
C) 没有区别

答案是 A。

### Q54
判断对错？函数声明会被提升，函数表达式不会被提升。
A) 正确
B) 错误

答案是 A。

### Q55
哪个语句会显示导入模块的 URL？
A) `import.path`
B) `path.show`
C) `path.directory`
D) `import.meta`

答案是 D。

### Q56
`console.log`、`console.error` 和 `console.warn` 有什么区别？
这三个函数在不同浏览器中记录方式不同，但通常 `error` 带有“错误”图标或红色，`warn` 带有“警告”图标或黄色。

### Q57
在以下文档中看到 `prototype` 的意义是什么：`Array.prototype.reduce()` 与 `Array.from()` 相对？选择所有正确的答案。
A) `prototype` 表示 `reduce` 是一个实例级方法
B) 缺少 `prototype` 表示 `from` 是一个类级方法
C) `prototype` 表示 `reduce` 继承自 `Object`

答案是 A、B。

### Q58
“最大调用栈超出”错误是如何触发的？
答案：通常是一个函数递归调用自身，导致等待执行的函数调用“栈”增长，直到达到最大值。

### Q59
以下哪个不是 Web API `window` 对象上用于调整大小的可用方法？
A) `resizeFrom()`
B) `resizeBy()`
C) `resizeTo()`
D) `sizeToContent()`

答案是 A。

### Q60
`String.prototype.replace()` 可以接受哪两种类型作为第一个参数？选择所有正确的选项。
A) 字符串
B) 正则表达式
C) 对象

答案是 A、B。

### Q61
下面的代码会向控制台输出什么，为什么？
```javascript
for(let i = 6; i < 10; i*1.5){
  if(i%2){
    continue;
  }
  console.log(i)
}
```
A) 6
B) 6, 9
C) 进入无限循环
D) lint 错误

答案是 C。`i*1.5` 不会改变 `i` 的值。

### Q62
以下哪一项是 `Object.assign()` 和展开语法之间的区别？
A) 展开语法调用 setter，`Object.assign()` 不调用
B) `Object.assign` 调用 setter，展开语法不调用
C) 它们实际上行为相同

答案是 B。

### Q63
给出一个一行代码检查属性是否存在于对象 `dog` 上的例子。
`const dog = { sound: ‘woof’, legs: 4 }`
一个可能的答案：`let propExists = ‘sound’ in dog;`

### Q64
以下哪一项不是将 `arguments` 函数对象转换为数组的方法？
A) `arguments.assign(arguments)`
B) `Array.prototype.slice.call(arguments);`
C) `Array.from(arguments);`
D) `[...arguments]`

答案是 A。

### Q65
事件处理的目标阶段是什么？
目标阶段是事件处理的三个阶段中的第二个阶段。第一个是捕获，第三个是冒泡。

### Q66
双感叹号（`!!`）的作用是什么？
A) 什么都不做
B) 返回对象的真值
C) 抛出错误

答案是 B。例如：`!!0` 返回 `false`。

### Q67
`1 < 2 < 3`
A) true
B) false

答案是 A。`1 < 2` 返回 `true`，`true < 3` 返回 `true`。

### Q68
JavaScript 如何在布尔上下文中评估值或对象的真值或假值？
A) 类型强制转换
B) 它是每个对象上的一个属性
C) 某些值永远没有真值或假值

答案是 A。

### Q69
使用 IIFE 的目的是什么？选择所有可能的答案。
A) 设置变量值
B) 初始化对象上的值
C) 在闭包中用于初始化值
D) 运行一次性函数

答案是 A、C、D。

### Q70
什么是词法作用域的例子？选择所有可能的答案。
A) 基于变量输入动态定义的作用域
B) `let self = this;` //在父函数中，然后 `self` 对内部函数可用
C) 内部函数的作用域包含父函数的作用域

答案是 B、C。

### Q71
下面的代码会向控制台输出什么，为什么？
```javascript
let a = 3;
a <<= 1;
console.log(a);
```
A) 3
B) 4
C) 6
D) 8

答案是 C。

### Q72
下面的代码会向控制台输出什么，为什么？
```javascript
badCode = () => {
  let arr = [1,2,3,4];
  const inner = () => {
    return arr.pop(2)
  }
  return inner;
}
console.log(badCode()());
```
A) lint 错误
B) 3, 4
C) 34
D) 4

答案是 D。

### Q73
下面的代码会向控制台输出什么，为什么？
```javascript
const obj = { a: 1 };
let obj2 = obj;
obj2.a = 2;
console.log(obj.a);
```
A) 1
B) 2
C) undefined

答案是 B。

### Q74
编程中的副作用是什么？
答案：副作用是指函数修改了影响应用程序其他部分的状态或可观察值。

### Q75
判断对错？`Array.prototype.filter()` 返回一个包含所有未通过提供的函数测试的项的数组。
A) 正确
B) 错误

答案是 B。


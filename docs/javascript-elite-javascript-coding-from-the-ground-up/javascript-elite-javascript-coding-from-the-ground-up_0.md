# JavaScript：从零开始的高级 JavaScript 编程



![](img/00004.jpeg)





## 引言

感谢下载《JavaScript: 从零开始的精英 JavaScript 编码》！本书是 DIY JavaScript 系列的第四部。之前的书籍有：

- JavaScript: 从零开始的入门级 JavaScript 编码
- JavaScript: 从零开始的中级 JavaScript 编码
- JavaScript: 从零开始的高级 JavaScript 编码

……并假设用户已经熟悉这些书籍的内容，包括 JavaScript 代码、语法以及从入门到高级的概念。为了获得最佳效果，应按时间顺序阅读这些书籍。本书将涵盖高级 JavaScript 操作技术，并提供与所解释主题匹配的代码示例。

再次感谢下载本书！在进一步提升 JavaScript 编码知识方面，你有许多选择。感谢选择 DIY JavaScript 系列作为你的学习工具！

## 第一章：JavaScript 中的面向对象编程

在琳琅满目的编程语言中，选择其中一种是明智的。影响语言选择的因素有很多，从效率到可靠性不一。整个讨论的很大一部分也取决于语言所遵循的范式。

编程范式是一种根据其提供的特征对编程语言进行分类的模型。它是构建语言结构和元素的基本风格。编程语言的风格和能力由其范式定义。一种语言甚至可以实现多种范式。例如，Haskell 只使用单一范式来定义其本身，即函数式编程。JavaScript 支持函数式、面向对象和命令式编程风格。不同的编程范式包括：

- 命令式 (Imperative)
- 面向对象式 (Object-oriented)
- 逻辑式 (Logic)
- 符号式 (Symbolic)
- 声明式 (Declarative)
- 函数式 (Functional)

为什么我们这么多范式？这个基础问题的答案是因为有很多问题需要解决，而不同的范式在处理特定问题组时效率更高。面向对象范式处理复杂性的良好方法，而通过使用函数范式可以避免并发问题。很容易理解，在大多数情况下，多范式语言会胜过单一范式语言。

### JavaScript 中使用的范式

我们已经知道 JavaScript 实现了多种范式，如函数式、面向对象和命令式。我们将研究 JavaScript 的面向对象特性。在完全深入其在语言中的实现之前，让我们先了解它是什么以及它的优势。

### 面向对象编程

面向对象编程是一种编程语言模型，它关注的是对象而不是执行操作，关注的是数据而不是涉及的逻辑。在这样的编程风格中，程序员只关心对象的实现。在这里，对象可以是从人类到恐龙、从砖块到建筑，以及你能想到的任何东西。每个对象都有一组关联的数据，以及可以用于操作它的不同方法。例如，让我们把汽车比作对象。汽车有颜色、尺寸、座椅数量等作为其数据，而移动、停止和启动可以被视为与汽车相关的方法。

程序中实现它时会出现大问题。我们首先识别将要使用的所有对象，以及它们彼此之间的关系；这被称为数据建模。第二步是将对象泛化为对象的类（class），它定义了与其关联的数据以及对象的不同方法/能力。

面向对象编程的概念为我们带来了这些益处：

- 对于每个类，我们都可以定义子类，子类可以从主类继承属性和功能。这被称为继承。现实世界遵循一个继承树，子元素继承父元素的部分或全部属性，再加上它自己特有的属性（这些属性在兄弟元素中可能并不具备）。这有助于缩短开发时间，并提高程序员的效率。
- 在定义类时，我们只关心类的数据。因此，当类的实例（即对象）运行时，它将无法修改任何不属于它的数据。这个过程被称为数据隐藏，它提供了系统安全性，并也有助于避免意外的数据损坏。
- 一个类可以反复使用。它不仅可以被它自己的程序重用，也可以被其他程序重用。
- 程序中发现错误？没问题！你只需要检查抛出错误的类的代码。这有助于简化整个程序的测试、调试和维护。

### JavaScript 中的 OOP

在前面的章节中，我们简要学习了面向对象语言的不同概念。当我们直接关注其在感兴趣的语言（即 JavaScript，它是动态的）中的实现时，我们只关注继承和封装。那么，我们为什么不关心多态呢？JavaScript 作为一种动态类型编程语言，使得观察多态的效应变得困难得多，因为它在 C 或 C++ 等静态类型语言中更为明显。在 JavaScript 中讨论方法重载或函数重载没有意义，因为我们在编写代码时没有指定任何数据类型。因此，机器无法区分同一个函数的两个定义。在 JavaScript 中，许多概念都是通过函数实现的。面向对象编码也不例外。实例是函数的实现。

```javascript
function child(name){
    // 此处编写代码
} // child 是一个构造函数，因为我们将使用 “new” 关键字来调用它。
```

现在，这看起来类似于 Java 等语言，我们使用 new 关键字来创建实例。

```javascript
var aditya = new child("aditya"); // Aditya 是 child 的一个实例
```





```
alert(typeof(aditya)); //displays "object"
```

在前面的示例中，`aditya` 是一个从子构造函数创建的实例。在这里，`child` 既是一个函数又一个对象，因为在 JavaScript 中函数确实也是对象。这个实例可以从子对象拥有它自己的数据/属性和功能，我们将在接下来的章节中讨论。

在 JavaScript 中有多种创建对象的方法。最基础且易于理解的方法是使用通用的对象字面量模式。例如：

```javascript
var student = {
    name: “ritesh”,
    age: “19”,
    branch: “cse”
};
```

在这里，我们创建了一个名为 `student` 的对象，`name`、`age` 和 `branch` 是它的属性。

第二种方法是使用构造函数模式。例如：

```javascript
function student (name, age, branch) {
this.name = name;
this.age = age;
this.branch = branch;
} // student () 是构造函数，因为我们在下面使用了 new 关键字来调用它。

var rahul = new student(“rahul”, 19 , “cse”) // Rahul 是我们从 student () 构造函数创建的一个新对象。

console.log(rahul.name); // Rahul
console.log(student.branch); // cse
```

在上述详细的方法中，我们观察到两者之间主要区别。在字面量模式中，我们在声明对象的同时已经创建了它。在构造函数模式中，我们需要显式地带有 `new` 关键字调用构造函数来创建一个 `student` 实例。

第三种也是最后一种方法是使用原型模式，正如方法名所示，我们直接将每个属性和方法添加到对象的原型上。例如：

```javascript
function student ()
{
student.prototype.firstName = "Ritesh";
student.prototype.lastName = "Kumar";
student.prototype.age =19;
student.prototype.branch = “cse”;
student.prototype.fullName = function () {
console.log (this.firstName + " " + this.lastName);
};

var ritest = new student () // 使用 new 关键字创建 student 的实例

console.log(ritesh.fullName()); // 这将在浏览器控制台中输出值“Ritesh Kumar”
```

你可能对上面示例中使用的 `prototype` 关键字感到困惑。这是该方法最重要的部分。我们将 `prototype` 定义为一个内部对象，其他对象通过它来继承属性。这允许同一个对象的多个实例共享公共属性。因此，使用原型对象定义的属性会被它的所有实例继承。

现在，在可供你使用的三种创建对象的方法中，需要讨论“哪一种最合适？”以及“在什么情况下使用？”我们将在下一个章节（重点关注封装）中尝试找到这个问题的答案。

## 为什么我们需要封装？

当你只需要某个对象的一个副本且该对象仅存储数据时，字面量方法非常方便。然而，当你想要拥有同一个对象的多个实例，并让它们拥有不同的数据时，这种方法是无效的。

当我们创建许多具有相同属性的对象时？可以将所有对象共享的共同属性封装在一个函数中，然后使用构造函数创建多个对象。这就是我们利用封装的地方。

JavaScript 中的实际实现使用了构造函数和原型方法的结合。例如：

```javascript
function student (name, age, branch) {
    this.name = name;
    this.age = age;
    this.branch= branch;
    this.marks = [];
}
```

借助上面的代码，我们使用构造函数方法创建了 `student` 对象的构造函数。它只包含了与 `student` 关联的数据。在接下来的代码段中，我们将使用原型方法添加与 `student` 关联的功能。

```javascript
student.prototype = {
    showName:function () {
        return this.name;
    },
    addMarks:function (mark) {
        this.marks.push(mark);
    }
}
```

在这里我们完成了定义对象的代码编写。下一个任务是创建我们刚刚创建的对象实例。

```javascript
// 对象的第一个实例
rishabh = new student("rishabh", 20, “cse”);
rishabh.addMarks(98); // 向 marks 数组中添加 98
rishabh.showName();  //返回“rishabh”

// 另一个实例
mitul = new student("Mitul", 19, “mechanical”);
mitul.addMarks(100); // 向 marks 数组中添加 100
mitul.showName (); // 返回“mitul”
```

通过上面的示例，掌握封装的重要性和益处可能非常清晰了。我们将 `student` 的所有数据和功能封装到一个函数中，稍后创建了它的实例（`rishabh` 和 `mitul`），它们共享与学生相同的属性。这减少了重复为相似对象实例定义每个属性的所有工作。

封装就到此为止！下一节将侧重于通过继承来扩展对象的实现，以便不同的对象可以共享或从父元素继承属性。

## JavaScript 中的继承

这一特性使我们更接近现实世界。让我们以人类为例。人类从 `Hominid` 类中继承了一些属性，而该类本身又从其父类继承了一些属性。人类从 `Hominid` 类中继承了一些属性，而该类本身又从其父类继承了一些属性。人类从 `Hominid` 类中继承了一些属性。继承在代码中以解决类似问题时变得非常有用。由于人类像其他哺乳动物一样繁殖，这种方法完全可行。此外，人类类可以添加其他属性，这可能对其他人类有用。

目前为止，我们只讨论了继承的现实实现。让我们深入代码并完善它。

让我们创建一个 car 对象。

```javascript
var car = {
    Color: “black”,
    Seats: “4”
};

// 继承 car 对象
var myCar = Object.create (cars); // 现在 myCar 继承了 car 的属性
console.log(myCar.color); // black
```

还可以向创建的实例添加更多属性。现在是继承的核心。我们使用 `inheritPrototype` 函数继承父类。

```javascript
function inheritPrototype(child, parent) {
    var parentCopy = Object.create(parent.prototype);
    parentCopy.constructor = child;
    child.prototype = parentCopy;
}
```

让我们理解这段代码是如何工作的。最初，我们创建一个父类的实例（`parentCopy`）。我们将子实例存储到 `parentCopy` 的构造函数中。这样做是因为下一步我们将 `parentCopy` 存储到子类的原型中。当我们这样做时，我们会覆盖子类原型之前的内容，从而丢失实际值。为了防止这种情况发生，我们创建了子构造函数的副本。当我们把 `parentCopy` 存储到子构造函数时，它不会丢失旧值。

创建一个新对象，它稍后将继承我们的父对象即 `car`。

```javascript
var audi = {
    name = “audi”
};

inheritPrototype(audi, car);
```

`Audi` 将拥有与汽车相同的属性，但它需要定义自己的独特属性，即 `name`。

## 第二章：JavaScript 中的 ‘this’ 关键字

在 JavaScript 中，`this` 关键字的行为与与其他编程语言相比不同。`this` 的值取决于对象是如何实例化的，或者说“关键字实际在哪里被使用”。简单来说，`this` 关键字返回当前的作用域对象。

如果你在全局作用域中使用它，它将引用 `window` 对象。`window` 对象是 JS 中唯一的全局可用对象。




因此，在全局作用域执行 `console.log(this)` 的结果将返回 `window` 对象。

为了更好地理解 `this`，让我们定义如下一个对象：

```javascript
var obj = {
  someProperty1: “Hi”,
  someProperty2: function(name) {
    // 在这里 ‘this’ 将作用域到 obj 对象，因为它是当前的局部作用域
    // 在该作用域中存在 window 对象
    return this.someProperty1 + name;
  }
}

var myObj = obj.someProperty2(“ John”);
console.log(myObj); // === “Hi John”
```

在上面的代码中，在 `obj` 的 `someProperty2` 属性中，我们使用了 `this` 关键字来访问当前对象的另一个属性 `someProperty1`，因此函数返回了结果为“Hi John”。

如果我们使用 JavaScript 的箭头函数，结果将不会受到影响。结果将是相同的。

借助 `this` 操作符的帮助，我们可以如下所示编写 JS 中的对象构造函数：

```javascript
function obj(name) {
  this.name = name;
  this.someMethod = function() {
    console.log(this.name);
  }
}

var myObj = new obj(“John”);
myObj.someMethod(); // === John
```

你也可以在对象的原型链上使用 `this`，如下：

```javascript
var obj = function() {
  return this.a + this.b;
};

var myObj = Object(obj);
myObj.a = 5;
myObj.b = 6;
myObj(); // === 11
```

与之前一样，我们使用 `this` 关键字来访问当前对象，并实例化它的数据成员和函数。

我想总结说，JavaScript 中的 `this` 关键字是你经常会发现需要它的东西。它会让你的工作变得更简单，并在你的编码风格中提供许多的灵活性。

## 第 3 章：JSON

JSON 或 JavaScript Object Notation（JavaScript 对象表示法），最初由 Douglas Crockford 规范，是最常用的数据交换格式之一。JSON 无非是用于存储和交换数据的简单媒介。这种交换发生在浏览器和服务器之间。

数据的格式只能是文本，任何 JavaScript 对象都可以转换为 JSON 格式以向服务器发送数据。同样，从服务器接收数据时，任何 JSON 文本都可以转换为 JavaScript 对象。

JSON 是一种轻量级格式，人类容易理解，也便于机器解析。它是语言无关的，这意味着它不仅局限于用于 JavaScript，尽管 JSON 使用了 JavaScript 语法，但由于该格式仅为文本，它可以被任何编程语言读取和使用。它的文件扩展名为 `.json`。由于其易于解析的特性，JSON 广泛优于如 `XML` 等其他数据传输表示。

## JSON 语法

JSON 语法与 JavaScript 语法相似，细微区别在于键（keys）必须是用双引号 “ ” 写的字符串，包含以下表示法：

1. 交换的数据应该以名称（Name）和值（Value）成对的形式存在。每个名称都有一个对应的值，可以通过 JavaScript 对象通过其名称进行访问。
   示例：`“name”: “Mark”`

2. 对象被放在大括号 `{ }` 中。每个名称字段后跟着一个冒号 `:`，然后是它的值。每个键值对后面都跟着一个逗号 `,`，以防用户想要输入另一个键值对。
   示例：`{ “name”: “Mark”, “age”: “20” }`

3. 这些对象的数组包含在方括号 `[ ]` 中，数组中的每个对象本身用逗号隔开。
   示例：`[ { “name”: “Mark”, “age”: “20” }, { “name”: “Anthony”, “age”: “40”}]`

## 数据类型

JSON 可以具有以下数据类型的值：

1. **Number（数字）** - 在 JSON 中，使用的数字必须是整数或浮点数。
   示例：`{ “age”: 20 }`

2. **String（字符串）**
   示例：`{ “firstName”: “Mark” }`

3. **Boolean（布尔值）**
   示例：`{ “vegetarian”: true }`

4. **Array（数组）**
   示例：`{ “children”: [“Henry”, “Emma”, “Joe”] }`

5. **另一个 JSON 对象**
   示例：`{ “details”: { “lastName”: “Lucas”, “bankAccount”: “savings” } }`

6. **Null（空）**
   示例：`{ “middleName”: null }`

**注意：** 不要将 JSON 数据类型与 JavaScript 数据类型混淆。不要使用以下任何数据类型：
1. 函数
2. 日期
3. `undefined`

## JSON 中的对象

可以使用点 `.` 表示法按照如下方式访问 JSON 对象的值：

示例：如果只想只想访问变量 `fullName` 的 `firstName`，可以这样操作：

```javascript
var fullName = {
  “firstName”: “Mark”,
  “lastName”: “Anthony”
};

var firstname = fullName.firstName;
```

另一种方法是使用方括号 `[ ]` 表示法：

```javascript
var firstname = fullName[“firstName”];
```

同样，我们可以通过逐层向下移动名称来访问嵌套的 JSON 对象。

示例：
```javascript
var fullName = {
  “name”: {
    “firstName”: “Mark”,
    “lastName”: “Anthony”
  },
  “age”: 25,
  “profession”: “Business”
} // 注意：原文此处缺少闭合大括号，已在翻译中补全逻辑

var firstname = fullName.name.firstName;
```
（注：此处根据上下文逻辑修正了示例代码的结构）

值也可以通过点或方括号表示法通过简单等值所需的键来设置：

示例：`fullName.name.firstName = "New"` 或 `fullName["name"]["firstName"] = "New"`

## JSON 中的数组

同样，我们可以通过逐层向下移动名称来访问嵌套的 JSON 对象。

示例：
```javascript
var fullName = {
  “name”: {
    “firstName”: “Mark”,
    “lastName”: “Anthony”
  },
  “age”: 25,
  “profession”: “Business”
}

var firstname = fullName.name.firstName;
```

## JSON 方法

从服务器接收到客户端的 JSON 数据始终是字符串。由于我们需要 JavaScript 对象来访问键，因此使用 `JSON.parse()` 方法解析 JSON 数据。

示例：`JSON.parse('{ “children”: { “Henry”, “Emma”, “Joe” } }’`

**注意：** 必须是 JSON 格式以避免语法错误。

同样，从客户端发送到服务器的 JSON 数据必须是字符串。由于我们的数据是 JavaScript 对象，我们需要将其转换为字符串。使用 `JSON.stringify()` 方法将 JSON 对象转换为字符串。

示例：`JSON.stringify({ “children”: { “Henry”, “Emma”, “Joe” } });`

## 第 4 章：同步与异步 JavaScript

在编程术语下理解异步和同步的概念是一项相当困难的任务。可能会有一个陡峭的学习曲线，但在良好掌握这一概念后，你将能够轻松地理解其他高级概念。JavaScript 中的大多数高级概念都基于 JavaScript 中的异步行为。

### 什么是同步和异步？

在编程术语中，同步行为意味着代码按照其编写的顺序执行，而异步意味着代码不一定按照其编写的顺序执行。

让我们通过现实生活场景来理解这一点。




想象一下你正在通过电话订披萨，但披萨店只有一个人能接听。如果你在你拨号时，也有人正在通过电话下单，你就会听到占线音。你必须等待当前的通话结束才能下订单，而在等待期间你不能做任何其他事情！这种场景展示了**同步（synchronous）**行为，即在当前任务完成之前，你无法进入下一个任务。

现在让我们在同一个场景中改变一些条件。假设接听披萨订单的人有了一个自动答录机，当电话忙时它会记录通话，并在完成当前通话后将其报告给接单员。现在，如果你拨号时电话正忙，你只需将订单留在答录机上，然后继续你的其他活动。当接单员收到你的订单后，会回给你电话并完成订单。这种场景详细描述了**异步（asynchronous）**行为，因为你不需要等待另一个通话完成。你可以完成你那部分的交易，并在对方准备好参与时，完成任何必要的细节（预计接收时间、支付方式、地址等）。

还有更简单的例子可以描述这种行为。你的身体可以同时执行多个任务，比如边唱歌边弹吉他。这就是异步行为的一个例子。相反，在打喷嚏时所有其他动作都会停止。这就是同步行为的一个例子，因为你必须等待打喷嚏动作完成后才能恢复或开始其他动作。

同样，在编程中，如果你不需要等待一个操作完成就可以进入另一个任务，那么这个操作就被说是异步的。较早开始并并行运行的操作可能会报告它的进度，就像接单员在收到你的订单后可能会带着更多细节回复你。

让我们来看看同步和异步 JavaScript 的示例代码。

### 同步 (Synchronous)

```javascript
console.log('how');
console.log('are');
console.log('you');
```

上述代码的输出将是：

how
are
you

这很简单！输出正如你预期的的一样。

### 异步 (Asynchronous)

```javascript
console.log('how');
setImmediate(function() {
console.log('are');
});
console.log('you');
```

上述代码的输出将是：

how
you
are

注意，这里的输出存在差异。这是由于 `setImmediate()` 方法的异步性质。

### 为什么要用异步？

无论你在同步模式下执行某些繁重或耗时的操作，其余代码在这些代码执行之前都不会执行。这导致了被称为 **I/O 阻塞（I/O blocking）**的情况。当这种情况发生时，UI（即你网站或 Web 的“前端”）将暂时变得无响应。这是因为 UI 和 JavaScript 代码运行在同一个线程中！在这种情况下，我们使用异步方法。这样，繁重任务就会继续运行，而不会导致应用程序的用户界面无响应。

这是一个使用场景的示例。

假设你有一个非常长的循环。假设循环是：

```javascript
for( var i = 0; i < 99999999; i++) {
// 在这里执行某些任务
}
```

当这个循环运行时，其他任何东西都不会运行，Web 应用的前端将变得无响应。为了解决这个问题，我们将使用 `setImmediate()`。以下是转换后的循环：

```javascript
function longLoop(i) {
// 在这里执行某些任务
if( i < 99999999) setImmediate(longLoop, i + 1); // 增加 i 的值并再次调用函数以创建循环
}

setImmediate(longLoop, 0); // 开始循环
```

运行上述代码不会导致 UI 变得无响应。循环的每次迭代调用都是异步的，从而允许其他函数的执行。

同步和异步的概念是 JavaScript 的核心，也是 JavaScript 中几乎所有高级概念的基础。无论是定时器、AJAX 还是任何其他概念，理解这个概念对于你建立后续知识奠基础至关重要。

## 第 5 章：JavaScript 中的 Promises

JavaScript 中的 `Promises` 为管理异步请求提供了替代方案。另一种替代方案是使用回调函数（callbacks）。

你可以将 JavaScript 中的 `promises` 理解为你在现实生活中做出的承诺。例如，如果你的朋友承诺在今天结束前代你完成家庭作业呢？他要么已经为你做完了作业，要么没有完成。他的承诺只有几种固定的结果，对吧？同样，JavaScript 中的 `promises` 可以有三种状态：

-   **Pending（待定中）**：这意味着 `Promise` 仍在等待被履行。它可以有任何输出，例如“现在还没到深夜，你不知道朋友是否会完成你的作业。”
-   **Rejected（已拒绝）**：这意味着你已经得到了承诺的结果，且结果是负面的，比如“你的朋友终究没有帮你做作业。”
-   **Resolved（已解决）**：这意味着你已经得到了承诺的结果，且结果是正面的，产生了预期的输出。“你的朋友帮你做完作业了！”

一旦承诺变为 Resolved 或 Rejected，就被认为已 **settled（已处理）**。

`Promise` 是 JavaScript 中的一个类。你通过使用关键字 `new` 来创建该类的新对象，从而创建一个新的 `Promise` 对象。

JavaScript 的 ECMAScript 5 或 ES5 标准（在本书出版时所有主要浏览器中都在使用）原生并不包含 `Promises` 标准。然而，某些浏览器仍然支持 `Promises`。ES6 原生支持 `Promises`。

### 创建 Promise (Creating Promise)

正如前面所述，我们使用 `new` 关键字来创建一个 `Promise` 对象。该对象的构造函数接收一个回调函数。以下是创建和使用 promise 的语法。

**ES5 语法：**

```javascript
new Promise( function(resolve, reject) { /* 执行任务 */ }).then(function() { } ).catch(function() { } );
```

**ES6 语法：**

```javascript
new Promise( (resolve, reject) => { /* 执行任务 */ } ).then( () => {} ).catch( () => {} );
```

作为回调函数参数的两个参数 `resolve` 和 `reject` 用于处理承诺。这两个参数本身都是函数。调用 `resolve()` 方法会将承诺状态设置为已解决，并调用作为 `then()` 方法参数的函数。调用 `reject()` 方法会将承诺状态设置为已拒绝，并调用作为 `.catch()` 方法参数的函数。

现在让我们之前的作业示例创建一个 promise：

```javascript
var friendPromise = new Promise( function(resolve, reject) {
/* 通常在这里有一个异步任务 */
if( isHomeworkCompleted() ) resolve();
else reject();
});
```

这里注意以下几点：

- Promise 在创建时就开始执行任务。在上面的示例中，一旦创建 Promise，它就会调用函数 `isHomeworkCompleted()` 来检查作业是否完成。
- 一旦承诺处理（一旦在内部使用了 `resolve()` 或 `reject()` 方法），再次使用它们将产生任何影响。

### 获取 Promise 结果 (Getting the Promise result)

在承诺处理后，我们可以使用 `` 对象的 `then()` 和 `catch()` 方法获取结果。其语法已在上一节中定义。

现在让我们考虑上一节中编写示例代码并看看如何使用它：

```javascript
friendPromise.then( function() {
console.log( 'Promise fullfilled!' );

}).catch( function() {

console.log( 'Promise rejected :( ' );
});
```

### Promises 是异步的 (Promises are Asynchronous)

获取 promise 结果的过程是异步的。为了理解这一点，请考虑以下示例：

```javascript
console.log('Before');

friendPromise.then( function() {
```




```javascript
console.log( 'Promise settled' );

}).catch( function() {

console.log( 'Promise settled' );

});

console.log('After');
```

上述代码的输出将是：

Before
After
Promise settled

如你所见，“After”在控制台屏幕上打印在“Promise settled”之前。在不了解更多情况的情况下，它看起来似乎应该是在它之后打印的。

### 如何让 Promise 在我们想要的时候执行

正如之前解释的那样，promise 一旦被创建就会开始执行任务。然而，我们通常希望 promise 代码是预先定义的，并在我们想要的时候再执行。这通过将 promise 封装在一个函数内部，并从该函数返回 promise 对象来实现。

上面的示例将转换为：

```javascript
var friendPromise = function() {

return new Promise( function(resolve, reject) {

/* 通常这里会包含一个异步任务 */

if( isHomeworkCompleted() ) resolve();

else reject();

});

}
```

现在我们可以像这样使用它：

```javascript
friendPromise().then( function() {

console.log( 'Promise settled' );

}).catch( function() {

console.log( 'Promise settled' );

});
```

### 将信息从任务传递到 then() 或 catch() 方法

我们可以通过将信息作为 `resolve()` 或 `reject()` 函数的参数来实现这一点。传递给 `resolve()` 或 `reject()` 方法的参数将分别作为参数传递给作为 `then()` 和 `catch()` 方法参数的函数。

让我们通过示例来探索这个概念：

```javascript
var promiseSum = function() {

return new Promise( function(resolve, reject) {

var x = 5 + 5;

if( someCondition() ) resolve( x + 5 );

else reject( x * 5 );

});

}

promiseSum().then( function(y) {

console.log( y ); // 如果 promise 成功完成，在控制台屏幕上打印‘15’

}).catch(function(y) {

console.log( y ); // 如果 promise 被拒绝，在控制台屏幕上打印‘50’

});
```

### 链式多个 promises

我们可以将多个 promise 的 `then()` 方法一个一个地链起来，以便一个接一个地执行异步任务。这是因为 `then()` 本身返回一个 promise。

如果我们在 `then()` 方法的函数中返回一个值，该值将传递给链中的下一个 `then()` 方法的参数函数（如果存在）。

```javascript
var examplePromise = function() {

return new Promise( function(resolve, reject) {

resolve();

});

}

examplePromise().then( function() {

return 5 + 7;

}).then(function( y ) { // 链式调用

console.log( y ); // 在控制台屏幕上打印‘12’

return y + 15;

}).then(function( y ) { // 链式调用

console.log( y ); // 在控制台屏幕上打印‘27’

});
```

如果我们在 `then()` 方法的函数中返回一个 promise，则链中的下一个 `then()` 方法将作为之前返回的 promise 对象的 `then()` 方法。

```javascript
var examplePromise = function() {

return new Promise( function(resolve, reject) {

resolve(7);

});

}

var someOtherPromise = function(x) {

return new Promise( function(resolve, reject) {

resolve( x * 10 );

});

}

examplePromise().then( function(x) {

console.log( x ); // 在控制台屏幕上打印‘7’

return someOtherPromise(x); // 返回一个新的 promise

}).then(function( y ) { // 链式调用

console.log( y ); // 在控制台屏幕上打印‘70’

return y + 15;

}).then(function( y ) { // 链式调用

console.log( y ); // 在控制台屏幕上打印‘85’

});
```

### Promise.all() 方法

通用语法：

`Promise.all( [ [ Promise1 [, Promise2 [, Promise3 [, Promise4 … ] ] ] ] ] );`

当作为参数传递的所有 promise 都已就绪（settled），或者其中一个被拒绝时，该方法将返回单个 promise。结果 promise 的 `then()` 方法的函数参数是一个数组，包含了所有 promise 的 `resolve` 方法传递的值，并按照它们解析的顺序排列。

让我们来看一个示例：

```javascript
var promise1 = new Promise( function(resolve, reject) { resolve(9); });

var promise2 = new Promise( function(resolve, reject) { resolve(8); });

var promise3 = new Promise( function(resolve, reject) { resolve(7); });

var promise4 = new Promise( function(resolve, reject) { resolve(6); });

var result = Promise.all( [ promise1, promise2, promise3, promise4] );

result.then( function(x) {

console.log( x );

});
```

上述代码的输出将是：

`[9, 8, 7, 6]`

如果栈中的某个 promise 被拒绝，则使用该 promise 的 `catch()` 方法。作为 `.catch()` 参数传递的函数包含单个值，即栈中被拒绝的 promise 的值。

现在让我们看看当修改上面的示例产生一个被拒绝的 promise 时会发生什么：

```javascript
var promise1 = new Promise( function(resolve, reject) { resolve(9); });

var promise2 = new Promise( function(resolve, reject) { resolve(8); });

var promise3 = new Promise( function(resolve, reject) {

reject(7); // 拒绝

});

var promise4 = new Promise( function(resolve, reject) { resolve(6); });

var result = Promise.all( [ promise1, promise2, promise3, promise4] );

result.then( function(x) {

console.log( x );

}).catch(function(y) {

console.log( y );

});
```

### Promise.race() 方法

通用语法：

`Promise.race( [ Promise1 [, Promise2 [, Promise3 [, Promise4 … ] ] ] );`

## 第六章：AJAX

你可能开发过许多包含图像、视频等的网页。它们可能都缺少共同的功能。它们都是静态网页，必须刷新才能显示新内容。在编写代码时，总有另一种更好的方法来执行任何任务。这就是 `AJAX` 出现的地方。AJAX 代表异步 JavaScript 和 XML。

AJAX 是一项重要的前端技术，在你每天访问的多个网站开发中起着至关重要的作用。这项技术帮助你更新页面的特定部分，而无需刷新整个页面。这还减少了主机和服务器之间交换的数据量。

AJAX 帮助 JavaScript 与 Web 服务器通信。现在你的网站不再是静态的，而是完全动态的。Gmail、Facebook、Twitter 和 YouTube 只是在前端代码中大量使用 AJAX 的几个网站。

### 理解 AJAX 调用过程

这涉及到多个步骤来完成任务。我们将在本节列出这些步骤，并在下一节中探索这些概念。

- 触发事件：发生在你点击按钮、提交表单或任何触发响应的操作时。
- AJAX 调用触发并使用 XML 向 Web 服务器发送请求。
- 服务器端脚本（PHP、ASP 等）获取输入并进行相应的处理。如果需要，它还会访问数据库。
- 脚本随后将处理后的输出结果通过 XML 返回给向服务器发出特定请求的客户端页面。
- JavaScript 回调函数接收数据，进行相应的处理，然后更新网页的相关部分。

### 步骤 1- 发起 HTTP 请求





为了发送 HTTP 请求，我们需要一个能够处理请求所需功能的对象。由于我们已经知道 `JavaScript` 支持面向对象编程（OOPS），创建一个对象对我们来说并不是一项挑战性任务。我们需要处理的是不同浏览器支持的各种对象类型。微软的 `Internet Explorer` 支持 `ActiveX` 对象。其他浏览器如 `Chrome`、`Mozilla` 等支持 `XMLHttpRequest` 对象。同时，微软在其后的浏览器中也实现了 `XMLHttpRequest` 对象，但为了提高兼容性，我们也将考虑 `ActiveX` 对象。

```javascript
//支持 XMLHttpRequest 对象的浏览器
if (window.XMLHttpRequest) {
    requestObject = new XMLHttpRequest();
//支持 ActiveX 对象的浏览器
} else if (window.ActiveXObject) {
    requestObject = new ActiveXObject("Microsoft.XMLHTTP");
}
```

正如我们在上一个节中提到的，服务器在处理输入后会返回响应。我们需要定义一个用于处理该响应的函数。

我们创建的对象有一个名为 `onreadystatechange` 的属性，它负责处理服务器返回的响应。

`requestObject.onreadystatechange = functionName;`

你可能会注意到我们在 `functionName` 后面没有加括号。这是因为我们只是在赋值一个函数的引用。

你也可以这样定义函数：

```javascript
requestObject.onreadystatechange = function(){
    //处理响应的函数体
};
```

现在我们已经准备好发送请求了。这可以通过调用我们创建对象的 `open()` 和 `send()` 方法来实现。

```javascript
requestObject.open('GET’, ‘http://www/websiteExample.com/file-name’, true);
requestObject.send();
```

### 让我们讨论一下 `open` 方法的参数

*   这被称为 HTTP 请求方法。还可以传递其他几种方法，如 `POST`、`HEAD`、`DELETE` 等。这些方法因服务器而异，因为并非所有服务器都支持定义的每种方法。根据标准，方法应始终保持大写。否则，某些浏览器可能不支持你的请求。
*   第二个参数是你正在发送请求的 URL。
*   第三个参数用于确定请求是否为异步请求，它是可选的。默认值为“true”，这意味着脚本将继续执行，允许用户在请求处理期间使用网页。相应地，“false”会停止脚本并等待服务器发送响应。

### 第 2 步 - 处理服务器的响应

在第一步中，我们定义了一个处理服务器发送响应的函数。在这一步中，我们将详细学习它的功能。

函数需要执行的第一件事是检查响应的状态。定义了五种响应状态，它们是：

| 值 | 状态 | 描述 |
| :--- | :--- | :--- |
| 0 | UNSENT | 请求客户端已创建，但尚未调用 `open` 方法 |
| 1 | OPENED | `open` 方法已被调用 |
| 2 | HEADERS_RECEIVED | `send` 方法已被调用 |
| 3 | LOADING | 正在加载数据 |
| 4 | DONE | 请求完成 |

从表中可以推出值 4 是成功状态。我们需要检查返回的响应是否成功。换句话说，我们需要检查其状态值是否为 4。

这可以通过将状态值与 `XMLHttpRequest.DONE`（其值为 4）进行比较来实现。

```javascript
if (requestObject.readyState === XMLHttpRequest.DONE) {
    // 请求已成功完成，可以进行进一步处理
} else {
    // 尚未就绪
}
```

一旦完成了上述步骤，我们的下一步是检查响应码。与响应状态类似，服务器可以发送几种响应码。响应码 200 表示这是一次成功的 AJAX 调用。我们需要检查代码是否为 200 以继续后续。

```javascript
if (requestObject.status === 200) {
    // 成功
} else {
    // 请求失败
    // 404 (未找到)
    // 500 (内部服务器错误)
    // 204 (无内容)
    // 等此类推。
}
```

在检查 AJAX 请求是否成功后，你可以根据需要对返回的数据进行任何操作。让我们来看看它的一些用法：

*   **登录表单**：你可能观察到某些网站会弹出一个小的登录窗口，并在登录后通知你已登录，而在此过程中页面保持不变。
*   **自动补全表单**：这种用法最常见的例子是 Google。当你向搜索框中输入内容时，它会为你建议你可能正在寻找的词或一组词。这是使用 AJAX 实现的。
*   **表单提交与验证**：如今几乎所有的网站都使用 AJAX 实时验证表单。
*   **聊天室和即时消息**：这最好的例子是 Facebook。在聊天时，新消息会出来而无需重新加载整个页面。这就是 AJAX 的魔力。
*   **外部组件**：Google AdSense 是此的一个流行例子。它根据你所在的网站向你显示内容并进行相应更改，而无需刷新整个页面。

## 第 7 章：JavaScript 中的闭包和回调

本章将涉及 JavaScript 的两个非常基础的概念：闭包（closures）和回调（callbacks）。它们允许我们使代码更加简洁、干练且富有创意。你将在开发中反复遇到这些概念。

### JavaScript 中的闭包

闭包在最基础的形式下，是指能够访问作用域之外变量的内部函数。闭包的概念需要对嵌套函数有合法的理解。

嵌套函数是“包含函数的函数”。让我们来看一下：

```javascript
//函数 1 是外部函数
function outer(){ // 定义函数 1
    //函数 2 是内部函数
    function inner(){ // 定义函数 2
    }
}

```

在上面的示例中，函数 2 (`inner()`) 位于函数 1 (`outer()`) 内部，因此被称为嵌套函数。同样，我们可以在外部函数内部有多个一个嵌套函数。

```javascript
//函数 1 是外部函数
function outer(){ // 定义函数 1
    //函数 1 是内部函数
    function inner1(){ // 定义函数 1
    }
    //函数 2 是内部函数
    function inner2(){ // 定义函数 2
    }
    .
    //函数 N 是内部函数
    function innerN(){ // 定义函数 N
    }
}
```

内部函数对外部函数定义的变量或参数进行求值或计算的能力就是闭包。让我们来看一个非常基本的 JavaScript 代码示例。

```javascript
//示例 1
//定义变量 a = 5
var a = 5;
//定义函数 add，将 5 加到 a 并返回值
var add = function(val){
a = a + val;// 将 val 加到 a
return a;// 返回 a
}
var result = add(5); // 将使 result 等于 10
```

在上面的代码中，函数 `add()` 从其外部作用域获取变量 `a` 的值，并将其加 5 后返回结果。因此，我们的输出将显示 10。这就是闭包的最基本用法。感到惊讶吗？到目前为止，你可能已经多次使用了它。

闭包非常流行，因为内部函数能够从其作用域之外检索变量、修改其值并返回结果。闭包可以访问以下变量：

*   作用域内部的变量，即函数体内部定义的变量
*   外部函数的变量，即包含函数的变量
*   全局变量

让我们进入一个更复杂的场景：

```javascript
//示例 2
//定义接收一个参数的函数 addTo
var addTo = function(param_outer){
//定义一个值为 10 的变量 sample
var sample = 10;
//定义接收另一个参数的函数 add
var add = function(){
return sample + param_outer;
}
//返回内部函数
return add;
}
```




在这里，我们有一个嵌套函数 `add()`，它可以接收来自外部函数 `addTo()` 的参数。当用户带有某些参数调用 `addTo()` 时，他将获得该内部函数作为返回值，该函数反过来将执行加法并返回值。

```javascript
var test = addTo(10);
```

在内部，`param_outer` 将等于 10，而 `add` 将取 `param_outer` 和 `sample` 的加值，并结果为 20。

```javascript
var add = 20 ;
```

当 `addTo()` 调用返回 `add` 时，`test` 的值将等于 `add` 的值，即 20。

让我们来看一个更复杂的例子：

```javascript
//Example 3

//定义一个接收参数的函数 addTo()

var addTo = function(param_outer){

//定义接收另一个参数的函数 add

var add = function(param_inner){

return param_inner + param_outer;

}

//返回内部函数

return add;
}

var test = addTo(10); //value 将不是 20
```

在这里，`test` 将取内部函数的值并本身成为一个函数，它将保留一个由我们设置的变量 `param_outer`，等于 10。

所以，`test` 在内部看起来像这样：

```javascript
//这仅仅是其内部形式的表示

var test = function(param_inner){

return param_inner + 10;

}
```

如果我们想给任何数字加 10，我们可以简单地写：

```javascript
var x =10;

var y = test(x);
```

这将使得 `y` 的值等于 20，或者说 10 + 10。

一个很好的用例是我们想要给某些数字加上常数时。我们可以利用这种方法来实现闭包。

示例：

```javascript
var addThree = addTo(3);

var a = addThree(10);//a 将为 3 + 10 = 13   

var a = addThree(20);//a 将为 3 + 20 = 23   

var a = addThree(30);//a 将为 3 + 30 = 33
```

### 闭包的特性

- 内部函数在执行后仍然可以访问外部函数的变量，正如我们在第三个示例中看到的。我们在调用内部函数之前调用了外部函数，即使在返回值之后，我们仍然可以在内部函数内部使用外部函数的参数，因为它们被保留了。
- 闭包存储的是对外部函数变量的引用而非实际值，如果需要，可以进行修改（参见示例 4）。
- 闭包提供了一种处理某些数据的安全方法，因为我们可以保存变量的引用并防止意外更改。

```javascript
//Example 4

//定义变量 a = 5

var a = 5;

//定义一个向 a 加 5 并返回值的函数 add

var add = function(val){

a = a + val;//将 val 加到 a

return a;//返回 a
}

a = 10; //更新 a 的值

var result = add(5); //将使 result 等于 15 而不是 10，因为在调用闭包之前 a 的值已更新，所以保存的引用被新引用更新了
```

闭包是强大的，但需要小心，因为更新的引用可能会让你的代码充满错误。始终确保仔细地使用这种能力。

**注意：** 闭包是函数或内部函数，它们保留了从全局或外部作用域引用的数据。

### JavaScript 中的回调函数

JavaScript 函数是一等对象。“一等对象”意味着它们可以在函数体中像其他对象一样使用。像变量一样，我们可以保存它们的引用，将它们作为参数传递，声明嵌套函数（参见前面的章节），并可以像我们之前看到的，作为函数的返回值返回。

函数可以作为参数传递给另一个函数的能力使得 JavaScript 函数变得特殊。被传递的函数可以在稍后的阶段执行，或者作为函数返回，由其他函数稍后执行。这就是构成的 JavaScript 回调（Callbacks）。

回调是指作为参数传递给另一个函数的函数，并在包含该函数的体内执行执行。由于此类能力的应用场景有限，它们可以被称为回调模式。

```javascript
//定义一个回调函数 sum()

var sum = function ( num1 , num2 ){

return num1 + num2;

}

//定义一个使用 sum() 作为参数的函数

var calling_func = function ( a , b , callback ){

return callback ( a , b //带有参数调用回调函数

}

var sample = calling_func( 5 , 5 , sum);//new 将被赋值为 10
```

让我们遍历上面的代码。首先，我们声明了一个简单的函数，相两个值并返回结果。接下来，我们定义了一个接收两个参数以及第三个参数“callback”的函数。回调本质上是一个变量，用于存储我们将传递的函数名并相应地执行它。它可以命名为任何名称。为了方便理解，我将其命名为 `callback`。

需要注意的是，当我们把函数作为变量传递时，我们只发送回调函数的定义名称（例如 `sum`），而不是带括号的函数调用。该函数只有在包含它的函数体内被调用时才会被执行。

正如我们看到的，回调函数不会被立即调用，而是以引用的形式保留，并且只有在调用函数指定时才被调用，这使得它们成为我们在上一节介绍的闭包。

回调函数不仅可以接受现有函数作为参数，还可以在参数中定义全新的函数。

```javascript
//定义一个回调函数 sum()

var sum = function ( num1 , num2 ){

return num1 + num2;

}

//定义一个使用 sum() 作为参数的函数

var calling_func = function ( a , b , callback ){

return callback ( a , b //带有参数调用回调函数

}

var sample = calling_func( 5 , 5 , sum);//new 将被赋值为 10
```




在深入研究 `apply()`、`call()` 和 `bind()` 方法的细节之前，我们需要了解 JavaScript 中的关键字 `this`。

### 从全局上下文中角度

`this` 关键字指向任何方法之外的全局对象。在接接的示例中，我们将看到 `this` 关键字在全局上下文中的作用范围。我们将在浏览器中使用 `console.log` 输出 `this` 关键字。

```
console.log(this);
```

控制台的输出结果为“window”，这本质上就是全局对象。这个结果意味着：

```javascript
console.log(this === window); // is true
```

在上面的示例中，我们进入了 `console.log(this)`，得到了 `window` 对象。

在这个示例中，我们将使用严格模式并检查 `this` 关键字的值。

```javascript
function abc(){
  'use strict'; // 严格模式
  return this;
}

console.log(abc()); // undefined
```

这一次，`this` 关键字的值为 `undefined`，因为在函数 `abc()` 内部没有定义它。

### 从函数上下文中角度

从函数上下文中处理 `this` 关键字，我们有 `call()`、`apply()` 和 `bind()` 这三个方法。让我们详细讨论一下这些方法。

#### apply 方法

`apply()` 方法通过 `this` 关键字的值来调用函数，并以数组（或类数组）的形式提供参数。

**语法：**

`apply()` 方法具有以下语法：

```
functionName.apply(thisArgument, argsArray[])
```

#### 参数

让我们来看看传递给 `apply()` 方法的参数。

- `thisArgument`：为调用 `functionName` 提供的 `this` 关键字的值。
  注意：在非严格模式下工作时，`this` 关键字的值可能与函数执行时看到的原始值不符。原始类型值和全局对象将被替换为 `undefined` 和 `null`。
- `argsArray[]`：类数组对象的参数，用于指定调用 `functionName` 时使用的参数；如果不需要向方法提供任何参数，则传入 `undefined` 或 `null`。

**示例：**

在接下来的示例中，我们将查看 `apply()` 方法的基本功能。

```javascript
var student1 = {firstName: 'Abhishek', lastName: 'Kumar'};
var student2 = {firstName: 'Ashok', lastName: 'Mehta'};

function text(hello) {
    console.log(hello + ' ' + this.firstName + ' ' + this.lastName + ' ? ');
}

text.apply(student1, ['How are you']); // How are you Abhishek Kumar ?
text.apply(student2, ['How are you']); // How are you Ashok Mehta ?
```

#### call 方法

`call()` 方法通过 `this` 关键字和单个参数来调用一个特定的函数。

**语法：**

`call()` 方法具有以下语法：

```
functionName.call (thisArgument, argument1, argument2, ....)
```

#### 参数

让我们来看看传递给 `apply()` 方法（注：此处原文误应为 call）的参数。

- `thisArgument`：为调用 `functionName` 提供的 `this` 关键字的值。
  注意：与 `apply()` 方法一样，在非严格模式下工作时，`this` 关键字的值可能与函数执行时看到的原始值不符。原始类型值和全局对象再次被替换为 `undefined` 和 `null`。
- `Argument`：...

**示例：**

```javascript
var student1 = {firstName: 'Abhishek', lastName: 'Kumar'};
var student2 = {firstName: 'Ashok', lastName: 'Mehta'};

function text(hello) {
    console.log(hello + ' ' + this.firstName + ' ' + this.lastName + ' ? ');
}

text.call(student1, 'How are you'); // How are you Abhishek Kumar ?
text.call(student2, 'How are you'); // How are you Ashok Mehta ?
```

#### bind 方法

`bind()` 方法创建一个新函数，允许你显式设置 `this` 关键字。

**语法：**

```
functionName.bind(thisArgument, argument1, argument2, ...)
```

**参数**

- `thisArgument`：为调用 `functionName` 提供的 `this` 关键字的值。
- `argument1, argument2, ...`：在调用函数时将传递给函数的参数。

**示例：**

```javascript
var student1 = {firstName: 'Abhishek', lastName: 'Kumar'};
var student2 = {firstName: 'Ashok', lastName: 'Mehta'};

function text(hello) {
    console.log(hello + ' ' + this.firstName + ' ' + this.lastName + ' ? ');
}

var bound1 = text.bind(student1);
bound1('How are you'); // How are you Abhishek Kumar ?

var bound2 = text.bind(student2);
bound2('How are you'); // How are you Ashok Mehta ?
```

---

## 第 9 章：JavaScript 中的集合 (Collections)

在 JavaScript 中，集合（collection）指的是数据的分组。具体来说，它指的是将数据整合到结构中，使得我们可以通过索引访问每个值。集合可以有许多形式，如对象、数组、map、set。

在本章中，我们将专注于对象和数组等数据结构以探索这一概念。我们将学习如何创建对象/数组、如何填充这些数组，以及遍历数组的方法。我们还将涵盖各种数组方法，如 `push`、`pop`、`sort`、`concat`、`indexOf` 等。此外，我们将讨论多维数组以及一维数组。

数组是一种包含有序值的数据结构，可以通过其名称或索引进行引用。在 JavaScript 中，我们不需要在声明时为数组定义特定的数据类型，这与 C、C++ 或 Java 不同。相反，我们可以使用预定义的 `Array` 对象及其各种方法。可以通过以下任何一种方式创建数组：

```javascript
var fruitsArray = new Array(apple, mango, banana, orange);
var fruitsArray = Array(apple, mango, banana, orange);
var fruitsArray = [apple, mango, banana, orange];
```

通常，第三种实现数组的方式是最常用的（方括号表示法），被称为“数组字面量”（Array Literal）或“数组初始化器”（Array Initializer）。

请记住，在方括号表示法 `[ ]` 中声明数组时传递单个数值表示该数组的值，而在 `Array` 函数表示法 `()` 中传递单个数值则表示该数组的长度，并据此分配相应数量的空位置。

```javascript
var arr = [10]; // 将创建一个名为 arr 值为 10 的数组
```




相反，`var arr = Array(10);` 将创建一个名为 `arr` 的数组，它没有元素，但长度被设置为 10。

### 填充数组

填充数组简单意味着在不同的索引处为数组赋值。默认情况下，单个值被填充在数组的第 0 个索引处，如下：

```javascript
arr[0] = ‘0th value’;
```

我们也可以创建数组时对其进行填充，如下：

```javascript
var fruitsArray = [apple, mango, banana, orange];
```

然后通过索引访问每个元素，例如：

`console.log(fruitsArray[0]);` 将带我们得到结果 ‘Apple’。

但通常，我们不会手动遍历每个索引。相反，我们可以使用循环来实现，循环会自动遍历每个索引，并据此访问数组的每个值。

例如（例：`var fruitsArray = [apple, mango, banana, orange];`

```javascript
for(i = 0; i < fruitsArray.length; i++)
{
  console.log(fruitsArray[i]);
}
```

上述代码将输出：

apple
mango
banana
orange

在这里，`.length` 是一个预定义的数组方法，用于确定数组的长度。它对于遍历数组非常有益。也可以通过 `forEach` 循环代替 `For` 循环获得上述输出，如下：

例如（例：`fruitsArray.forEach(function(fruit){  console.log(fruit);  });`）

### 有用的方法

我们已经讨论了预定义的 `Array` 方法之一，即 `.length` 方法。还有许多其他方法。这些方法在 `Array` 对象上的定义如下：

- `push()`：此方法用于向数组中添加元素。所有元素都会被添加到数组的末尾。
例如（例：`var fruitsArray = [apple, mango, banana, orange];`
```javascript
fruitsArray.push(‘litchi’);
```
现在，结果 `fruitsArray` 将是 `[apple, mango, banana, orange, litchi]`

- `pop()`：此方法用于从数组中删除最后一个元素，并返回被删除的元素。
例如（例：`var fruitsArray = [apple, mango, banana, orange];`
```javascript
var removedFruit = fruitsArray.pop();
```
现在，结果 `fruitsArray` 将是 `[apple, mango, banana]`，且 `removedFruit` = `orange`。

- `concat()`：此方法用于将一个数组与另一个数组合并成新数组。
例如（例：`var fruitsArray = [apple, mango, banana, orange];`
`var carsArray = [honda, suzuki, toyota];`
```javascript
var fruitsAndCars = fruitsArray.concat(carsArray);
```
现在，结果 `fruitsAndCars` 将是 `[apple, mango, banana, orange, honda, suzuki, toyota];`

- `sort()`：此方法用于升序排序数组。
例如（例：`var fruitsArray = [apple, mango, banana, orange];`
```javascript
fruitsArray.sort();
```
现在，结果 `fruitsArray` 将是 `[apple, banana, mango, orange]`

- `reverse()`：此方法用于反转数组元素的顺序，即第一个元素变成最后一个元素，最后一个元素变成第一个元素。
例如（例：`var fruitsArray = [apple, mango, banana, orange];`
```javascript
fruitsArray.reverse();
```
现在，结果 `fruitsArray` 将是 `[orange, banana, mango, apple]`

- `indexOf(reqdElement, [fromIndex])`：此方法用于搜索数组中特定元素的索引。
例如（例：`var fruitsArray = [apple, mango, banana, orange];`
`fruitsArray.indexOf(‘mango’);` 将得到结果 1。

如果数组中有多个同名的元素，我们还可以作为可选参数指定我们想要从哪个索引开始查找所需的元素。
例如（例：`var fruitsArray = [apple, mango, banana, orange, mango];`
`fruitsArray.indexOf(‘mango’, 2);` 将得到结果 4。

### 多维数组

多维数组可以通过将一个数组嵌套在另一个数组中的方式创建，并为一个维度的每个元素填充另一个维度的每个元素。多维数组可以如下所示创建并填充：

例如（例）：
```javascript
var arr = new Array(5);
for (i = 0; i < 5; i++) {
  arr[i] = new Array(5);
  for (j = 0; j < 5; j++) {
    a[i][j] = i + j;
  }
}
```

上述代码在 `console` 打印时将给出以下输出：

00 01 02 03 04
10 11 12 13 14
20 21 22 23 24
30 31 32 33 34
40 41 42 43 44

这完成了对 JavaScript 中集合概念的解释。请明智地运用知识！在编写代码之前，始终思考你的代码。到达特定路径终点有很多。结构结构一切。

## 第 10 章：在 JavaScript 中使用 Canvas

HTML 中的 `canvas` 元素负责显示许多图形元素，如绘制、动画、交互等。

一个简单的 canvas 元素如下：

```html
<canvas id="idCanvas" width="300" height="300"></canvas>
```

起初，它看起来像 <img> 元素，缺少 `src` 和 `alt` 属性。`canvas` 元素的默认高度和宽度分别为 300px 和 150px。

### JavaScript 在 canvas 中的作用

我们在刚才的 HTML 部分已经预览了 JavaScript 与 canvas 的基本用法，即使用 DOM 属性选择 canvas。

```javascript
var canvas = document.getElementById("idCanvas");
```

现在我们将讨论 JavaScript 在 canvas 实际用法。最初，canvas 是完全空白的。要在 canvas 上绘制内容，需要 JavaScript 通过 `getContext()` 方法访问渲染上下文。

该方法有一个参数，用于定义上下文类型。

例如（例：`getContext("2d")`

要在 JavaScript 中引入此方法，我们首先需要选择 canvas 并存储在变量中，就像之前那样。其次，我们需要使用同一个变量连接 `getContext` 方法。最后，我们将其存储在另一个变量中（通常命名为 `ctx`），我们将在项目的剩余部分用它操作 canvas 元素。

```javascript
var canvas = document.getElementById("idCanvas");
var ctx = canvas.getContext("2d");
```

注意，`getContext` 方法是由我们创建的存储 canvas 的变量（`canvas`）连接的。现在上下文已经创建，我们就可以通过变量 `ctx` 轻松地为画布 设置不同的值。

例如：
1. `ctx.fillStyle="blue";`
2. `ctx.fillRect(8, 8, 40, 40);`

上述代码将在第 2 行指定的坐标处绘制矩形，并如第 1 行所示提供蓝色。





### 绘制矩形

有三种方法绘制矩形：

- `fillRect(A, B, width, height)`：绘制一个填充的矩形。
- `strokeRect(A, B, width, height)`：绘制一个矩形的轮廓。
- `clearRect(A, B, width, height)`：擦除指定的矩形区域，绘制一个完全透明的矩形。

上述三种方法接受格式如下的参数：

- `A`, `B` – 指定矩形在画布网格中的相对位置。
- `width` – 指定矩形的宽度。
- `height` – 指定矩形的高度。

### 示例：

```html
<!DOCTYPE HTML>
<HTML>
<head>
<title>drawing rectangle</title>
</head>
<body>
<canvas id="idCanvas" width="200" height="100">
this browser does not support the canvas element.
</canvas>
<script>
var canvas = document.getElementById("idCanvas");
var ctx = canvas.getContext("2d");
ctx.fillStyle = "blue";
ctx.fillRect(0,0,150,75);
</script>
</>
</HTML>
```

### 绘制路径

路径基本上是一组由线段连接的点或点列表。形状可以是不同的或相同的，具有不同的高度、宽度、颜色等。它甚至可以是闭合的或开放的。

### 关于矩形和路径的说明：

矩形和路径是画布中唯一的原始形状。要绘制你想象的任何其他形状，必须通过连接多条路径来绘制。

### 如何使用路径绘制任何形状：

需要以下方法来创建、连接和操作路径以形成形状。

1. `beginPath()` 方法：用于创建一个新路径。
2. `path` 函数：
- `CanvasRenderingContext2D.moveTo()`：将新创建路径的起始索引移动到 `(A, B)` 坐标。
- `CanvasRenderingContext2D.bezierCurveTo()`：向路径中添加曲线（也称为三次贝塞尔曲线）。
- `CanvasRenderingContext2D.lineTo()`：用直线将子路径与 `A, B` 坐标以及上一点连接起来。
- `CanvasRenderingContext2D.arc()`：在路径上添加一个以 `(A, B)` 位置为中心、`radius` 为半径的弧。从 `startAngle` 开始并按方向在 `endAngle` 结束。
- `CanvasRenderingContext2D.ellipse()`：在路径上添加一个以 `(A, B)` 位置为中心、`radiusX` 和 `radiusY` 为半径的椭圆，从 `startAngle` 开始并按方向在 `endAngle` 结束。
- `CanvasRenderingContext2D.fill()`：用当前样式填充子路径。
- `CanvasRenderingContext2D.rect()`：创建一个位于 `(A, B)` 的矩形路径，其大小由 `width` 和 `height` 决定。
- `CanvasRenderingContext2D.quadraticCurveTo()`：向路径中添加二次贝塞尔曲线。
- `CanvasRenderingContext2D.arcTo()`：向路径中添加一条弧，包括由直线连接的控制点。
3. `closePath()`：关闭路径。
4. `fill()`：通过 `fill()` 方法，我们可以绘制填充内容区域的实心形状。
5. `stroke()`：通过 `stroke()` 方法，我们可以在形状周围绘制边框。

遵循这些步骤将帮助你使用路径绘制你想象的任何形状：
1. 创建新路径。
2. 使用上述列出的绘制命令在路径中绘制。
3. 绘制完成后关闭路径。
4. 路径创建完成后，你可以通过描边或填充来轻松操作它。
5. 路径现在可以渲染了。

### 使用路径绘制三角形

本节展示了如何使用路径绘制三角形。查看下面的代码。

HTML 代码：
```html
<!DOCTYPE HTML>
<HTML>
<body onload="drawTriangle();">
<canvas id="idCanvas" width="100" height="100"></canvas>
</body>
<script type="text/JavaScript" src="new.js"></script>
</HTML>
```

JavaScript 代码：
```javascript
function drawTriangle() {
  var canvas = document.getElementById('idCanvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');
    ctx.beginPath();
    ctx.moveTo(50, 75);
    ctx.lineTo(95, 72);
    ctx.lineTo(101, 26);
    ctx.fill();
  }
}
```

### 在上下文中应用样式和颜色

接下来，我们将查看如何根据我们的为形状或上下文添加颜色和样式。

### 两个重要的属性

为了在画布中为形状添加颜色和样式，我们必须考虑两个重要的属性：
1. `fillStyle = "color"`
2. `strokeStyle = "color"`

`fillStyle` 属性在填充形状和上下文时设置样式。`strokeStyle` 属性设置形状边框的样式。注意引号内等号后面的 `"color"`。它代表你选择的颜色。此空间必须由字符串填充。颜色代表 CSS 颜色。颜色可以接受以下类型的值：
- 预定义的颜色名称，如 `"red"`、`"blue"`、`"green"` 等。
- 可以接受颜色的十六进制代码，例如。

（注：原文后续部分似乎存在文本内容逻辑混乱或重复，已根据语意进行结构对齐处理）
- Can accept Hex codes of colors, for example,（可以接受颜色的十六进制代码，例如）
- Predefined colors name such as `"red"`, `"blue"`, `"green"` etc.（预定义的颜色名称，如 "red"、"blue"、"green" 等）
- Color can accept values of the following type:（颜色可以接受以下类型的值：）





```
    }

  }

}
```

结果截图：

![](img/00001.jpeg) ![](img/00002.jpeg)

我们可以通过这种方式实现许多高级动画。

### 事件处理

JavaScript 中的动画可以根据用户的操作来触发。

以下是一些常见触发事件及其用途的列表。

示例：

1. 用户点击按钮时，按钮应立即执行动画。
2. 当用户点击特定按钮时，下拉菜单应执行动画。
3. 用户滚动页面时，背景过渡应发生变化。

根本上，每当用户执行特定操作时，任何基础动画都应该发生。

### 鼠标常用事件

● `onclick`: 当用户点击鼠标时执行给定的任务。
● `oncontextmenu`: 当用户右键点击鼠标时执行特定任务。
● `ondblclick`: 当用户双击鼠标时执行特定任务。
● `onmouseover`: 当鼠标指针移动到元素上时执行特定任务。
● `onmousemove`: 当鼠标指针在移动时执行特定任务。
● `onmouseup`: 当用户从元素上释放鼠标键时执行特定任务。

### 键盘常用事件

● `onkeydown`: 当用户按下任何指定的按键时执行特定任务。
● `onkeypress`: 当用户按下键时执行特定任务。
● `onkeyup`: 当用户释放按键时执行特定任务。

## 在 JavaScript 中使用 canvas 动画

在 canvas 上动画或移动任何之前绘制的形状的基本规则是：通过逻辑或硬编码的方式重新重绘它。

### 简单动画步骤

在本节中，我们将看到如何使用预定义方法创建帧并动画对象。

### 创建帧的步骤

1. 使用 `clearReact()` 方法 -
   当画布被这些形状填充时，你需要清除之前绘制的形状。`clearReact()` 方法有助于清除画布。
2. 每次操作前保存。
   当你创建一个新设置并希望之前绘制的形状保留在画布上时，在每次创建新帧时都必须保存原始状态。
3. 添加动画
   在这一步中，完成了帧的实际渲染。
4. 恢复过程。
   最后但同样重要的是，在你目前所做的一切之后，在创建新帧之前允许画布进行恢复。

### 由你定义的动画

在本节中，我们将检查一些控制动画的方法。

1. `setInterval(method, delay)`
   每隔 `delay` 毫秒重复执行由 `method` 指定的方法。
2. `setTimeout(method, delay)`
   执行由 `method` 指定的方法，延迟以毫秒为单位。
3. `requestAnimationFrame(function callback)`
   请求浏览器在下一次绘制之前调用指定的方法来更新动画，根据你的需求。
4. `windowRequestAnimationFrame()`
   当画布准备绘制帧时，可以通过更平滑高效的方式完成动画。回调函数的通常为每秒 60 次，在后台运行时可能会降低频率。

### 示例：

在以下示例中，我们将使用 JavaScript 对 canvas 元素进行动画。

HTML 代码：
```html
<!DOCTYPE html>
<html>
<body>
<canvas id="idCanvas"></canvas>
</body>
</html>
```

CSS 代码：
```css
html{
height: 100%;
width: 100%;
margin: 0;
padding: 0;
}
body{
height: 100%;
width: 100%;
margin: 0;
padding: 0;
}
canvas{
position: absolute;
}
```

JavaScript 代码：
```javascript
const canvas = document.getElementById('idCanvas');
const context = canvas.getContext('2d');
let height, width, s = 1;
window.onresize = function resize() {
  height = canvas.height = document.body.offsetHeight;
  width = canvas.width = document.body.offsetWidth;
};
window.onresize();

context.fillStyle = 'white';
context.fillRect(0, 0, width, height);
(function loop() {
  context.save();
  context.translate(width/2, height/2);
  context.fillStyle = 'rgba(0,0,0,0.09)';
  context.fillRect(-width/2, -height/2, width, height);
  let j = 0, k = 0;
  s += 0.001;
  for( let i = 0; i < 512; i++ ) {
    const r = i * ((j / k) / 5);
    context.beginPath();
    context.fillStyle = `hsl(${i%360}, 100%, 50%)`;
    context.globalAlpha = r/(512 * ((2 / 3) / 5) / 2) + 0.1;
    context.translate(Math.sin(i * s) * (i * j++), Math.cos(i * s) * (i * k++));
    context.fillRect(0, 0, r, r);
    context.closePath();
    if( j > 2 ) j = 0;
  }
  context.restore();
  requestAnimationFrame(loop);
})();
```




内存的高效利用一直是开发者的一大难题，而且未来也将如此。然而，在低级语言和高级语言中，第一步和第三有所不同。高级语言隐式地实现（由语言自动完成），而低级语言则是显式实现（必须由程序员自己完成）。

## 内存分配

内存主要可以通过两种方式分配：

- **值初始化**：JavaScript 在声明值时分配内存。

```javascript
var number = 1234;//为类型为 number 的变量 `number` 分配内存
var name = ‘John’; //为类型为 string 的变量 `name` 分配内存
var obj = {
    x: ‘name’,
    y: 8
}//为对象 `obj` 及其包含的值分配内存
var arr = [2, 3, 4, 5];//为数字数组分配内存
function add5(num1){
return num1+5;
}//已分配内存
```

- **函数调用**：某些函数调用也会导致为对象分配内存。

```javascript
var date = new Date(); // 为 date 对象分配内存
```

## 垃圾回收

如前所述，程序通过某些算法来寻找应用程序未使用且可以释放的内存块。在这里，我们将介绍两个最重要的垃圾回收算法及其局限性：

- 引用计数垃圾回收
- 标记-清除算法

### 引用计数垃圾回收

许多流行语言（如 `PHP` 和 `Python`）都实现了这种算法。它基于这样一个想法：如果一个对象没有任何引用，就可以被释放。它将引用为零的对象视为应用程序不再使用的对象。

```javascript
var obj = {obj1: {x:3}, c:3, d: 4};
obj -----> obj1 //由于一个对象引用另一个，两者都无法被释放
obj = 0; // 现在，没有对象引用 'obj1' 了，因此它可以被释放
```

**局限性：**

当对象创建引用循环时，该算法往往会失效，如下例：

```javascript
var obj1 = {}
var obj2 = {}
obj1.x = obj2;
obj2.x = obj1;
```

这在对象 `obj1` 和 `obj2` 之间创建了引用循环。假设这段代码片段是函数或任何局部作用域的一部分。当程序离开此作用域时，这两个对象都变得毫无用，因此由于不再被使用而应该被释放。引用计数算法无法释放这些对象占用的内存，因为它们都至少有一个引用指向。

### 标记-清除算法

当单个对象无法被应用程序访问时，标记-清除算法会将该对象占用的内存返回空闲内存池。

虽然引用循环问题在这种算法中不再存在，但可能会出现某些僵尸内存块未被释放的情况，因为算法认为它们是可访问的。

## JavaScript 中导致内存泄漏的常见错误

- 意外的全局变量
- 闭包
- 指向已移除元素的 DOM 引用
- 遗忘的回调

虽然某些语言提供了垃圾回收机制，但事实证明它们并非无处有效。这最终取决于程序员跟踪内存使用情况，并尽可能尝试显式地释放内存。这样做可以增强语言所采用垃圾回收机制的潜力，从而减少此类内存泄漏错误。

## 第 13 章：JavaScript 中的递归

递归是一种编程技术，几乎可以用于所有的编程语言。它既不是函数，也不是数据类型。它是一种架构、设计模式或解决特定问题的编码风格。

### 什么是递归？

递归是在函数内部调用函数本身的行为。这听起来可能很简单，但在实践中可能是一个复杂的概念。许多程序员苦于理解如何正确使用这种技术。这种从函数内部调用函数的过程会一直持续，直到实现所需的目标。

递归是一种循环。你反复重复同一组代码，因为函数从其内部调用自己。通常，你可以使用递归或循环来实现相同的目标。大多数递归算法都可以通过循环重新创建。

### 递归示例

让我们来看循环的一些示例，以及实现相同目标的等效递归方案。

我们先从打印 0 到 10 的数字开始。使用循环时，代码看起来如下：

```javascript
for(var i = 0; i <= 10; i++) {
    console.log( i );
}
```

现在，让我们看看打印 0 到 10 所有数字的递归技术：

```javascript
function printNumbers(x) {
console.log( x );
X++; // 增加 x 的值
if(x < 10)printNumbers(x);
}
printNumbers(0); // 调用一次函数以初始化过程
```

这两段代码做的是相同的事情。通过递归技术，你可以看到有一个 `if` 语句来检查 `x` 的值是否小于 10。如果小于 10，则再次调用该函数。如果使用递归技术，我们需要进行此类检查，否则递归过程将永远持续下去。

让我们转向更困难的问题。我们将尝试获取一个数字的阶乘，即所有数字的乘积。首先，让我们借助循环来实现：

```javascript
var number = 6;
function getFactorial(x) {
    var r = 1;
    for(var i = 1; i <= number; i++) {
        r = i * r;
    }
    return r;
}
var result = getFactorial( number );
console.log( 'Factorial of ' + number + ' is ' + result );
```

现在，让我们看看通过递归来实现：

```javascript
var number = 6;
function getFactorial(x) {
    if(x == 1) return x;
    return x * getFactorial( --x ); // 递归！
}
var result = getFactorial( number );
console.log( 'Factorial of ' + number + ' is ' + result );
```

这里发生的是，我们在每次进行递归调用之前将 `x` 的值减 1。我们检查“如果 `x` 的值为 1，则返回 `x`”。在 `x` 的值达到 1 之前，存在调用栈：

调用 `getFactorial(6)`
- 返回 `6 x getFactorial(5)`步骤 i
- 返回 `5 x getFactorial(4)`步骤 ii
- 返回 `4 x getFactorial(3)`步骤 iii
- 返回 `3 x getFactorial(2)`步骤 iv
- 返回 `2 x getFactorial(1)`步骤 v

`getFactorial(1)` 因为检查返回 1，现在值按照上面的队列向上移动：
- 控制移动到步骤 v 变为 `2 x 1` 或 `2`
- 控制移动到步骤 iv 变为 `3 x 2` 或 `6`
- 控制移动到步骤 iii 变为 `4 x 6` 或 `24`
- 控制移动到步骤 ii 变为 `5 x 24` 或 `120`
- 控制移动到步骤 i 变为 `6 x 120` 或 `720`

最后，返回 6 的阶乘，即 720。

### 递归的缺点

虽然递归可以使复杂问题的代码变得更短，但在实践中使用它时，仍有一些需要注意的重大缺点：

- 它使代码更难理解。
- 每次函数调用都会堆叠在内存中。非常长的递归链可能会耗尽 JavaScript 引擎分配的所有内存，从而导致不可预见的错误。不同的机器可能有不同的内存容量。
- 递归比循环慢，因为每次迭代都必须调用新的函数。每次函数调用都会消耗一些时间。

## 何时使用递归？





# 递归

当循环出现分支或嵌套过深时，应该使用递归。使用递归可以让搜索动态结构、遍历图等操作变得简单易行。你永远不要为可以通过循环轻松解决的简单问题使用递归，因为循环的运行速度快得多且占用的内存更少。

## JavaScript 中的性能

许多复杂算法都使用递归。这是一种非常强大的技术。JavaScript 编译器会将递归的每个函数调用压入栈。这可能是非常危险的，但在 `ES6` (`ECMAScript 6`) 中，情况将不再如此。递归将不再进行堆栈，而是导致代码的立即执行，这使得使用递归变得安全得多。

## 结

非常感谢下载《JavaScript: Elite JavaScript Coding from The Ground Up!》。我希望你在阅读这本书中获得的收获与我写这本书时的收获一样多。如果你喜欢这本书，请在 Amazon 上留下好评以示你的支持。我们非常感激你的反馈！

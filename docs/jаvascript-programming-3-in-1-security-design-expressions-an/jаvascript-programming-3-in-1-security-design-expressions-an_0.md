# JavaScript 编程：三合一安全设计、表达式与 Web 开发




## 第一部分：JAVASCRIPT 安全设计
### 代码执行与漏洞利用

## 第二部分：JAVASCRIPT 表达式
### 运算符、循环与 switch 语句

## 第三部分：JAVASCRIPT Web 开发
### 使用 Node 和 Express JS 构建 REST API
**RICHIE MILLER**



---



- 关于 Richie Miller

---

## 第一部分：JAVASCRIPT 安全设计
### 代码执行与漏洞利用
**RICHIE MILLER**

## 序言
Web 运行在 JavaScript 之上，它是编写浏览器应用程序的主流编程语言，得益 `Node.js` 运行时，在后端看到它也变得越来越常见。JavaScript 代码的质量对于 Web 应用的安全至关重要。然而，本书并非关于通用的 Web 应用安全。我们不会讨论影响任何编程语言编写的应用程序的问题。我们将专注于 JavaScript 特有的安全问题，这些问题是其动态特性的结果。我将教你如何识别此类漏洞、如何修复它们，并防止这些问题渗透到你的代码中。首先，我们将关注 JavaScript 在 Web 应用安全中的基础作用。JavaScript 可能包含漏洞，但在某些情况下它甚至可能成为攻击向量。运行 JavaScript 代码有两个流行的环境，它们都具有非常不同的安全属性。首先，我们将查看浏览器如何运行 JavaScript，然后查看 `Node.js` 的不同之处。接着，我们将研究可能导致安全漏洞的语言特征：动态类型、动态代码执行和原型继承。我们将以一个简单的代码错误示例结束，仅仅是缺少了一个字符，导致了敏感数据的严重泄露。信息安全专业人员以使用特定术语而闻名。我们在这里不会使用它们，但理解 Web 安全的基本概念是非常重要的。针对 Web 应用的攻击是由人实施的。你可能脑海中有一个穿黑色连帽衫的人在地下室敲键盘的形象，但现实要微妙得多。攻击者根据其能力和动机而异。他们可能是想要给朋友留印象的青少年、寻求报复的解雇员工，以及为了钱入侵应用程序的罪犯。没有漏洞，攻击就不可能发生。漏洞是系统中的技术缺陷，允许恶意意图的人入侵我们的应用程序和系统。它们可能是代码中的简单 Bug、基础架构缺陷或配置错误。所有这些都可能导致数据泄露。通常登上头条的是关于泄露数百万敏感数据记录（如信用卡号）。数据泄露还涉及滥用应用程序功能，例如在不付款的情况下购物，或对从未购买过的商品获得退款。最常见的 Web 应用架构有三层：浏览器、服务器和数据库。JavaScript 代码可以同时在浏览器和服务器（如笔记本电脑或手机）上运行。使用 `Node.js` 的代码中的漏洞可能允许攻击者访问应用程序。成功的攻击可能导致数据泄露。（注：此处原文存在部分重复混乱）`Node.js` 中的漏洞可能导致服务器被攻破。

## 第一章 浏览器如何执行 JavaScript 代码
JavaScript 的创建是为了给 HTML 页面添加交互性。浏览器是运行 JavaScript 的原生环境。事实上，JavaScript 是该领域的主流编程语言。当用户访问网页时，浏览器允许同时访问多个页面。如果其中一个网站被感染，运行在浏览器中的 JavaScript 代码是受到限制的。幸运的是，某些浏览器使用复杂的沙箱机制，通过 HTTP 协议下载代码并使用子资源完整性（SRI）防止攻击者向网站注入自己的代码。浏览器没有权限访问本地资源，如文件系统和本地网络。`Node.js` 是 JavaScript 的运行时环境，基于 Google Chrome 的 V8 引擎。它的独特之处允许 JavaScript 代码在浏览器之外运行。这听起来是一个非常强大的功能，允许轻松处理复杂的数据格式，例如数学公式，允许用户使用自己的代码来扩展应用程序。不幸的是，这也是攻击者梦寐以求的——将他们的代码注入你的应用程序的能力。JavaScript 有一种非常独特的继承机制。大多数主流语言使用类来表示类型之间的层级关系。在 JavaScript 中，这一目标通过构建对象之间的动态关系来实现。每个对象都有继承属性的父对象原型。如果攻击者可以修改原型链，可能会以意想不到的方式改变你的代码的行为。JavaScript 的动态性强大且灵活，它促进了快速开发并释放了程序员的生产力。如果这种动态性被攻击者滥用，就会导致安全漏洞。

---

## 第二部分：JavaScript 表达式
### 运算符、循环与 switch 语句

## 第一章 switch 语句的工作原理
现在你已经对书籍有了概览，让我们深入第一个主题：`switch` 语句。我们使用 `switch` 代替多个 `if/else` 语句。这有助于我们稍微简化代码。我们使用 `case` 语句来比较 `switch` 语句中的每个表达式，使用 `break` 语句退出每个 `case`，而 `default` 语句在没有 `case` 匹配时使用。这里有一个例子。我这里有一个带有表达式的 `switch` 语句。然后我们将把该表达式的值与我们拥有的每个 `case` 语句进行比较，你可以有一个或多个 `case` 语句。我们通常会有好几个。这就是你使用 `switch` 的原因。一旦语句匹配成功，我们将执行一条语句或一系列语句。在每个 `case` 语句中，你可以放置任意数量的语句。但非常重要的一点是，在下一个 `case` 之前有一个 `break` 语句，因为 `break` 将完成 `switch` 块。如果其他 `case` 都不匹配，则使用 `default`。

## 第二章 switch 语句的块作用域问题
`switch` 语句执行的是所谓的严格比较。这意味着类型和值必须匹配，表达式才能匹配。在 `switch` 语句中，我们看到一个名为 `strictComparison` 的新函数在第 11 行，以及第 9 行的按钮。在第 12 行设置了一个变量 `productId`。在 `switch` 语句内部，注意第 15 行、18 行和 21 行。如果都不匹配，则执行 `default`。

## 第三章 使用 for/in 循环
后续章节将涵盖 `for/in` 和 `for/of` 的区别。本章的目标是查看 `for/in` 语句和 `for/of` 语句。我们还将查看 `break`、`continue` 和标签。

## 第四章 break 和 continue 语句
后续章节将涵盖 `for/in` 和 `for/of` 的区别。本章的目标是查看 `for/in` 语句和 `for/of` 语句。我们还将查看 `break`、`continue` 和标签。

## 第五章 数运算符
本章数学运算符。本章的目标是查看各种运算符，如赋值和比较。我们还将查看 `+`、`-`、`*`、`/`、`%`、`++` 和 `--`。这些是数学运算符。JavaScript 还拥有一组数学运算符。

## 第六章 赋值与三元运算符
就像 C# 一样，有赋值运算符。我们知道等号将一个值赋给另一个，但还有这种简写 `price = price + 5`，你可以使用 `+=` 进行加减、乘、除、幂和模。这些变得非常简单。

## 第七章 逻辑运算符
本章关于逻辑运算符和短路求值。本章的目标是学习真假值。在 JavaScript 世界中，这些被称为 truthy 和 falsy。我们还将讨论可用的逻辑运算符，如 `and`、`or` 和 `not`。

## 第八章 短路与运算符优先级
短路是逻辑表达式的一种优化。它允许 JavaScript 根据真值或假值跳过后续的表达式。

## 第九章 利用 JavaScript 异常处理
本章关于利用 JavaScript 异常处理。本章的目标是学习如何使用 `try catch` 语句和 `finally` 语句处理异常。我们还将讨论如何抛出自定义异常以及如何确定抛出的错误类型。

## 第十章 如何检测错误类型
现在我们看到了使用 `error.name` 报告错误类型。让我们看看 JavaScript 抛出的内置错误。有 `ReferenceError`、`RangeError`、`TypeError`、`URIError`、`SyntaxError` 和 `EvalError`。`EvalError` 仅用于后兼容，不再使用，但在旧代码中可能仍看到。

## 第十一章 如何确定 JavaScript 变量数据类型
本章关于确定 JavaScript 变量数据类型。本章的目标是探索可用的不同数据类型，包括原始类型和对象。我们将学习使用 `typeof` 运算符 of 运算符来确定数据类型。

## 第十二章 属性的辅助函数
构造属性很好，但使用它更好。我们见过一些辅助函数，如 `isArray`、`nullOrUndefined` 等。

## 第十三章 理解 JavaScript 中的 'this'
本章关于 JavaScript 中的 `this`。本章的目标是学习 `this` 如何根据作用域变化：全局作用域、函数作用域、对象字面量、事件处理器和方法。

## 第十四章 复制数组
本章关于使用强大的展开运算符。在这个模块中，我们将演示展开运算符的力量。我们将使用它来复制和拼接数组，向构造函数传递参数，对对象执行浅拷贝，并使用展开运算符调用多个参数的函数。

## 第十五章 使用展开运算符传递参数
我们也可以使用展开运算符来帮助构建传入多个值的对象。

## 第十六章 对象字面量的浅拷贝
展开运算符的另一个有用功能是对对象字面量执行浅拷贝。让我们来看看它是如何工作的。

```javascript
let product = {
    id: 1,
    name: "Apple Pie"
};
let copy = { ...product };
```

---

# 第三部分：JavaScript Web 开发
### 使用 Node 和 Express JS 构建 REST API

## 第一章 如何获取正确的工具
```javascriptconst fs = require('fs');
const FILE_NAME = './assets/pies.json';
const path = require('path');

const filePath = path.join(__dirname, FILE_NAME);

fs.readFile(filePath, 'utf8', (err, data) => {
    if (err) {
        console.error(err);
        return;
    }
    const pies = JSON.parse(data);
    console.log(pies);
});
```

## 第二章 如何创建 Express 服务器
```javascript
const express = require('express');
const app = express();
const router = express.Router();

app.use(express.static('public'));
app.use(express.json());

router.get('/', (req, res) => {
    res.send('Hello World!');
});

app.use('/api', router);

const server = app.listen(5000, () => {
    console.log('Server is running on http://localhost:5000');
});
```

## 第三章 如何使用 REST API 方法检索和搜索数据
```javascript
router.get('/pies', (req, res) => {
    fs.readFile(filePath, 'utf8', (err, data) => {
        if (err) {
            console.error(err);
            return;
        }
        const pies = JSON.parse(data);
        res.status(200).json(pies);
    });
});
```

## 第四 如何创建模块
```javascript
module.exports = {
    get: function(resolve, reject) {
        // logic
    }
};
```

## 第五章 如何获取单条数据
```javascript
router.get('/pies/:id', (req, res) => {
    fs.readFile(filePath, 'utf8', (err, data) => {
        if (err) {
            console.error(err);
            return;
        }
        const pies = JSON.parse(data);
        const pie = pies.find(p => p.id === parseInt(req.params.id));
        if (pie) {
            res.status(200).json(pie);
        } else {
            res.status(404).json({ error: 'Pie not found' });
        }
    });
});
```

## 第六章 如何搜索数据
```javascript
router.get('/pies/search', (req, res) => {
    fs.readFile(filePath, 'utf8', (err, data) => {
        if (err) {
            console.error(err);
            return;
        }
        const pies = JSON.parse(data);
        const query = req.query.name.toLowerCase();
        const filtered = pies.filter(p => p.name.toLowerCase().includes(query));
        res.status(200).json(filtered);
    });
});
```

## 第七章 如何创建 POST 端插入数据
```javascript
router.post('/pies', (req, res) => {
    const newPie = req.body;
    fs.readFile(filePath, 'utf8', (err, data) => {
        if (err) {
            console.error(err);
            return;
        }
        const pies = JSON.parse(data);
        pies.push(newPie);
        fs.writeFile(filePath, JSON.stringify(pies, null, 2), (err) => {
            if (err) {
                console.error(err);
                return;
            }
            res.status(201).json(newPie);
        });
    });
});
```

## 第八章 如何创建 DELETE 端删除数据
```javascript
router.delete('/pies/:id', (req, res) => {
    fs.readFile(filePath, 'utf8', (err, data) => {
        if (err) {
            console.error(err);
            return;
        }
        const pies = JSON.parse(data);
        const index = pies.findIndex(p => p.id === parseInt(req.params.id));
        if (index !== -1) {
            pies.splice(index, 1);
            fs.writeFile(filePath, JSON.stringify(pies, null, 2), (err) => {
                if (err) {
                    console.error(err);
                    return;
                }
                res.status(204).send();
            });
        } else {
            res.status(404).json({ error: 'Pie not found' });
        }
    });
});
```

## 第九章 如何创建 PATCH 端修改数据
```javascript
router.patch('/pies/:id', (req, res) => {
    fs.readFile(filePath, 'utf8', (err, data) => {
        if (err) {
            console.error(err);
            return;
        }
        const pies = JSON.parse(data);
        const index = pies.findIndex(p => p.id === parseInt(req.params.id));
        if (index !== -1) {
            pies[index] = { ...pies[index], ...req.body };
            fs.writeFile(filePath, JSON.stringify(pies, null, 2), (err) => {
                if (err) {
                    console.error(err);
                    return;
                }
                res.status(200).json(pies[index]);
            });
        } else {
            res.status(404).json({ error: 'Pie not found' });
        }
    });
});
```

## 第十章 如何处理 REST API 方法中的异常
```javascript
router.get('/', (req, res, next) => {
    try {
        // logic
    } catch (error) {
        next(error);
    }
});
```

## 第十一章 如何构建复用的错误模块
```javascript
const errorHandler = (err, req, res, next) => {
    console.error(err.stack);
    res.status(500).json({ error: err.message });
};
module.exports = errorHandler;
```

## 第十二章 如何从 HTML 页面调用 REST API
```html
<script>
    fetch('/api/pies')
        .then(response => response.json())
        .then(data => console.log(data));
</script>
```


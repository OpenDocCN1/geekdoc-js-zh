
# 引言

ECMAScript 语言的核心功能定义在一项名为`ECMA-262`的标准中。该标准所定义的语言称为 ECMAScript。在浏览器和 Node.js 中所使用的 JavaScript，实际上是 ECMAScript 的超集。浏览器和 Node.js 通过额外的对象和方法增加了更多功能，但语言的核心仍然由 ECMAScript 定义。`ECMA-262`的持续发展对整个 JavaScript 的成功至关重要，本书介绍了该语言最近一次重大更新所带来的变化：`ECMAScript 6`。

- 通往`ES6`之路
- 关于本书
  - 浏览器与`Node.js`的兼容性
  - 本书读者对象
  - 概述
  - 排版约定
  - 帮助与支持
- 致谢

## 通往 ES6 之路

In 2007, JavaScript was at a crossroads. The popularity of Ajax was ushering in a new age of dynamic web applications, while JavaScript hadn’t changed since the third edition of `ECMA-262` was published in 1999. `TC-39`, the committee responsible for driving the ECMAScript development process, put together a large draft specification for `ECMAScript 4`. `ECMAScript 4` was massive in scope, introducing changes both small and large to the language. Updated features included new syntax, modules, classes, classical inheritance, private object members, optional type annotations, and more.

The scope of the `ECMAScript 4` changes caused a rift to form in `TC-39`, with some members feeling that the fourth edition was trying to accomplish too much. A group of leaders from Yahoo, Google, and Microsoft created an alternate proposal for the next version of ECMAScript that they initially called `ECMAScript 3.1`. The “3.1” was intended to show that this was an incremental change to the existing standard.

`ECMAScript 3.1` introduced very few syntax changes, instead focusing on property attributes, native JSON support, and adding methods to already-existing objects. Although there was an early attempt to reconcile `ECMAScript 3.1` and `ECMAScript 4`, this ultimately failed as the two camps had difficulty with the very different perspectives on how the language should grow.

In 2008, Brendan Eich, the creator of JavaScript, announced that `TC-39` would focus its efforts on standardizing `ECMAScript 3.1`. They would table the major syntax and feature changes of `ECMAScript 4` until after the next version of ECMAScript was standardized, and all members of the committee would work to bring the best pieces of `ECMAScript 3.1` and `4` together after that point into an effort initially nicknamed `ECMAScript Harmony`.

`ECMAScript 3.1` was eventually standardized as the fifth edition of `ECMA-262`, also described as `ECMAScript 5`. The committee never released an `ECMAScript 4` standard to avoid confusion with the now-defunct effort of the same name. Work then began on `ECMAScript Harmony`, with `ECMAScript 6` being the first standard released in this new “harmonious” spirit.

`ECMAScript 6` reached feature complete status in 2015 and was formally dubbed “ECMAScript 2015.” (But this text still refers to it as `ECMAScript 6`, the name most familiar to developers.) The features vary widely from completely new objects and patterns to syntax changes to new methods on existing objects. The exciting thing about `ECMAScript 6` is that all of its changes are geared toward solving problems that developers actually face.

## 关于本书

A good understanding of `ECMAScript 6` features is key for all JavaScript developers going forward. The language features introduced in `ECMAScript 6` represent the foundation upon which JavaScript applications will be built for the foreseeable future. That’s where this book comes in. My hope is that you’ll read this book to learn about `ECMAScript 6` features so that you’ll be ready to start using them as soon as you need to.

### 浏览器与 Node.js 的兼容性

Many JavaScript environments, such as web browsers and `Node.js`, are actively working on implementing `ECMAScript 6`. This book doesn’t attempt to address the inconsistencies between implementations and instead focuses on what the specification defines as the correct behavior. As such, it’s possible that your JavaScript environment may not conform to the behavior described in this book.

### 本书读者对象

This book is intended as a guide for those who are already familiar with JavaScript and `ECMAScript 5`. While a deep understanding of the language isn’t necessary to use this book, it will help you understand the differences between `ECMAScript 5` and `6`. In particular, this book is aimed at intermediate-to-advanced JavaScript developers programming for a browser or `Node.js` environment who want to learn about the latest developments in the language.

This book is not for beginners who have never written JavaScript. You will need to have a good basic understanding of the language to make use of this book.

### 概述

Each of this book’s thirteen chapters covers a different aspect of `ECMAScript 6`. Many chapters start by discussing problems that `ECMAScript 6` changes were made to solve, to give you a broader context for those changes, and all chapters include code examples to help you learn new syntax and concepts.

**Chapter 1: How Block Bindings Work** talks about `let` and `const`, the block-level replacement for `var`.

**Chapter 2: Strings and Regular Expressions** covers additional functionality for string manipulation and inspection as well as the introduction of template strings.

**Chapter 3: Functions in ECMAScript 6** discusses the various changes to functions. This includes the arrow function form, default parameters, rest parameters, and more.

**Chapter 4: Expanded Object Functionality** explains the changes to how objects are created, modified, and used. Topics include changes to object literal syntax, and new reflection methods.

**Chapter 5: Destructuring for Easier Data Access** introduces object and array destructuring, which allow you to decompose objects and arrays using a concise syntax.

**Chapter 6: Symbols and Symbol Properties** introduces the concept of symbols, a new way to define properties. Symbols are a new primitive type that can be used to obscure (but not hide) object properties and methods.

**Chapter 7: Sets and Maps** details the new collection types of `Set`, `WeakSet`, `Map`, and `WeakMap`. These types expand on the usefulness of arrays by adding semantics, de-duping, and memory management designed specifically for JavaScript.

**Chapter 8: Iterators and Generators** discusses the addition of iterators and generators to the language. These features allow you to work with collections of data in powerful ways that were not possible in previous versions of JavaScript.

**Chapter 9: Introducing JavaScript Classes** introduces the first formal concept of classes in JavaScript. Often a point of confusion for those coming from other languages, the addition of class syntax in JavaScript makes the language more approachable to others and more concise for enthusiasts.

**Chapter 10: Improved Array Capabilities** details the changes to native arrays and the interesting new ways they can be used in JavaScript.

**Chapter 11: Promises and Asynchronous Programming** introduces promises as a new part of the language. Promises were a grassroots effort that eventually took off and gained in popularity due to extensive library support. `ECMAScript 6` formalizes promises and makes them available by default.

**Chapter 12: Proxies and the Reflection API** introduces the formalized reflection API for JavaScript and the new proxy object that allows you to intercept every operation performed on an object. Proxies give developers unprecedented control over objects and, as such, unlimited possibilities for defining new interaction patterns.

**Chapter 13: Encapsulating Code with Modules** details the official module format for JavaScript. The intent is that these modules can replace the numerous ad-hoc module definition formats that have appeared over the years.



# Appendix A: Smaller ECMAScript 6 Changes

`Appendix A: Smaller ECMAScript 6 Changes` 涵盖了 ECMAScript 6 中实现的其他变更，这些变更你使用频率较低，或者不太适合归入各章所涵盖的更广泛的主要主题。

# Appendix B: Understanding ECMAScript 7 (2016)

`Appendix B: Understanding ECMAScript 7 (2016)` 描述了为 ECMAScript 7 实现的两个标准新增特性，它们对 JavaScript 的影响远不如 ECMAScript 6 那么显著。

## 排版约定

本书采用以下排版约定：

*   *斜体* 用于介绍新术语
*   `等宽字体` 表示代码或文件名

此外，较长的代码示例放在等宽字体代码块中，例如：

```
function doSomething() {
    // empty
}
```

在代码块中，`console.log()` 语句右侧的注释表示代码执行时你在浏览器或 Node.js 控制台中看到的输出，例如：

```
console.log("Hi");      // "Hi"
```

如果代码块中的某行代码抛出错误，也会在代码右侧标注：

```
doSomething();          // error!
```

## 帮助与支持

你可以通过访问以下网址提交问题、建议更改或发起拉取请求：

https://github.com/nzakas/understandinges6

如果你在阅读本书时有任何疑问，请发送邮件至我的邮件列表：

http://groups.google.com/group/zakasbooks

## 致谢

感谢 Jennifer Griffith-Delgado、Alison Law 以及 No Starch Press 的所有人，感谢他们对本书的支持和帮助。在我长期患病期间工作效率降至最低时，他们的理解和耐心令我永生难忘。

我非常感谢技术编辑 Juriy Zaytsev 的敏锐眼光，也感谢 Axel Rauschmayer 博士的反馈以及多次有助于澄清本书中某些概念的谈话。

感谢所有向 GitHub 上托管的本书版本提交修复的人：ShMcK、Ronen Elster、Rick Waldron、blacktail、Paul Salaets、Lonniebiz、Igor Skuhar、jakub-g、David Chang、Kevin Sweeney、Kyle Simpson、Peter Bakondy、Philip Borisov、Shaun Hickson、Steven Foote、kavun、Dan Kielp、Darren Huskie、Jakub Narębski、Jamund Ferguson、Josh Lubaway、Marián Rusnák、Nikolas Poniros、Robin Pokorný、Roman Lo、Yang Su、alexyans、robertd、404、Aaron Dandy、AbdulFattah Popoola、Adam Richeimer、Ahmad Ali、Aleksandar Djindjic、Arjunkumar、Ben Regenspan、Carlo Costantini、Dmitri Suvorov、Kyle Pollock、Mallory、Erik Sundahl、Ethan Brown、Eugene Zubarev、Francesco Pongiluppi、Jake Champion、Jeremy Caney、Joe Eames、Juriy Zaytsev、Kale Worsley、Kevin Lozandier、Lewis Ellis、Mohsen Azimi、Navaneeth Kesavan、Nick Bottomley、Niels Dequeker、Pahlevi Fikri Auliya、Prayag Verma、Raj Anand、Ross Gerbasi、Roy Ling、Sarbbottam Bandyopadhyay 和 Shidhin。

同时，也感谢所有在 Patreon 上支持本书的人：Casey Visco。

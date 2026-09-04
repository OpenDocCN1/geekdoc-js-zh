
# JavaScript 正则表达式入门指南

## 前言

脚本和自动化任务通常需要从输入数据中提取特定的文本部分，或将其从一种格式转换为另一种格式。本书将帮助你理解正则表达式，这是一种用于各种文本处理需求的微型编程语言。

本书高度依赖示例来逐一介绍正则表达式的特性。建议你手动输入每个示例并进行实验。请努力理解示例输入以及给出的解决方案，并检查当你修改输入和代码的部分部分时，输出是否发生了变化（或没有！）。打个比方，这就像学习开车——无论你读了多少书或听了多少解释，你都需要实践经验才能精通。

## 前提条件

你应该熟悉编程基础。你还应该具备 JavaScript 语法的知识，以及 `map` 和 `filter` 等函数式编程概念。

你还应该习惯于阅读文档、在线搜索、访问提供的进一步阅读的外部链接、摆弄插图示例、在卡壳时寻求帮助等。换句话说，要积极主动并好奇，而不是仅仅被动地消费内容。

## 规范

- 此处展示的示例在 Chrome/Chromium 控制台中经过测试，并包含了其他浏览器和平台不具备的功能。
- 显示的代码片段是从控制台复制粘贴的，并为了演示目的进行了修改。某些命令前带有注释，以提供背景和解释。添加了空行以提高可读性，当输出为 `undefined` 或无必要显示时将跳过输出。
- 除非另有说明，所有的示例和解释均针对 `ASCII` 字符。
- 全书中都提供了外部链接，供你深入探索某些主题。
- `learn_js_regexp` 仓库包含了所有与书籍相关的代码片段、练习题和其他细节。如果你不熟悉 `git` 命令，请点击网页上的 `Code` 按钮获取文件。

## 致谢

- MDN: Regular Expressions — 文档与示例
- `/r/learnjavascript/` 和 `/r/regex/` — 对初学者和资深程序员都有很有帮助的论坛
- `stackoverflow` — 用于获取关于 JavaScript 和正则表达式相关问题的答案
- `tex.stackexchange` — 用于帮助解决关于 pandoc 和 tex 的相关问题
- `canva` — 封面图片
- `oxipng`、`pngquant` 和 `svgcleaner` — 图像优化

## 反馈与勘错

如果你能让我知道对这本书的感受，我将不胜感激。这可以是简单的感谢、指出拼写错误、代码片段中的错误、书籍的哪些方面对你有效（或无效！）等等。读者的反馈是至关重要的，对于自出版的作者来说尤其如此。

你可以通过以下方式联系我：

- Issue 管理: <https://github.com/learnbyexample/learn_js_regexp/issues>
- 电子邮件: learnbyexample.net@gmail.com
- Twitter: <https://twitter.com/learn_byexample>

## 作者信息

Sandeep Agarwal 是一个懒人，倾向于只做足够的工作来维持他简朴的生活。他在 Analog Devices 担任设计工程师期间积累了大量财富，并在 28 岁时离开了职场。遗憾的是，他在几年内挥霍了积蓄，不得不挣扎谋生。尽管重重困难，销售编程电子书拯救了这个懒惰的他，让他不需要重新寻找工作。现在他可以负担得起任何想读的幻想电子书，并花费不健康的时间浏览互联网。

当创作灵感来袭时，你会发现他正在编写另一本编程电子书（这些书最终往往至少包含一个正则表达式示例）。为他的电子书研究材料以及日常的社交媒体使用淹没了他的书签，因此为了保持理智，他维护了精选资源列表。他感谢免费的学习资源和开源工具。他自己的贡献可以在 <https://github.com/learnbyexample> 找到。

书籍列表：<https://learnbyexample.github.io/books/>

参见 `Version_changes.md` 以跟踪跨版本的更改。

## 为什么需要它？

正则表达式是一种多功能的文本处理工具。你会发现它们包含在大多数用于脚本的语言的标准库中。如果没有，通常可以找到第三方库。正则表达式的语法和特性随语言而异。JavaScript 的语法与 Perl 语言相似，但存在显著差异。

JavaScript 中的 `String` 对象支持多种处理文本的方法。那么，正则表达式有什么特别之处？你为什么需要它？为了学习和理解，可以将正则表达式看作一种专门用于文本处理的微型编程语言。这里是一些常见的用例：

- 清洗字符串以确保符合已知规则集。
- 过滤或提取字母、数字、标点符号等部分。
- 字符串替换。你可能熟悉图形化的搜索和替换工具，如下方的 LibreOffice Writer 所示。匹配大小写、全词匹配、替换和全部替换都是一些基础功能。另一个真实世界的用例是密码验证。下面的截图来自 GitHub 注册页面。执行如字符串长度和允许的字符类型等检查是另一个核心功能。

## 本书结构

本书逐一介绍概念，章节末尾的练习只需要该章节介绍的功能。每个概念都配有大量的示例，以涵盖多种问题和边界情况。如前提到的，强烈建议通过手动输入代码片段来跟随示例。理解示例输入字符串的性质以及实际编程命令是非常重要的。

- `RegExp` 简介
- 锚点
- 选择与分组
- 转义元字符
- 点元字符和量符
- 间言：调试和可视化工具
- 处理匹配部分
- 字符类
- 分组与反向引用
- 间言：常见任务
- 逆向先行断言
- Unicode
- 延伸阅读

## 正则表达式简介

本章将带你开始定义 `RegExp` 对象并在字符串方法中使用它们。为了保持简单易懂，示例将不会使用与正则表达式相关的特殊字符。主要重点是让你熟悉语法和文本处理示例。本章将介绍两种方法：`test()` 方法，用于搜索输入是否包含某个字符串，以及 `replace()` 方法用于将输入的部分替换为其他内容。

![](img/1a4ef11dadb051ae1522899ffab370e1_8_0.png)[](img/1a4ef11dadb051ae1522899ffab370e1_8_1.png)[](img/1a4ef11dadb051ae1522899ffab370e1_8_2.png)[](img/1a4ef11dadb051ae1522899ffab370e1_8_3.png)[](img/1a4ef11dadb051ae1522899ffab370e1_8_4.png)[](img/1a4ef11dadb051ae1522899ffab370e1_8_5.png)[](img/1a4ef11dadb051ae1522899ffab370e1_8_6.png)[](img/1a4ef11dadb051ae1522899ffab370e1_8_7.png)

本书将交替使用**正则表达式**和 `regexp` 这两个术语。当特指 JavaScript 对象时，将使用 `RegExp`。

## 控制台与文档

如序言章节提到的，书中提供的示例已经在 Chrome/Chromium 控制台上经过了测试。其他基于 Chromium 的浏览器也可能有效。

使用 `Ctrl+Shift+J` 快捷键从新标签页打开控制台。某些变量名在不同章节中重复使用——在这种情况下请打开另一个标签页以避免错误。

请查看 MDN: 正则表达式指南和 MDN: 正则表达式参考以获取示例、文档和浏览器兼容性详情。

## `test()` 方法

首先是一个简单的示例，用于测试一个字符串是否是另一个字符串的一部分。通常，你会使用 `includes()` 方法并传递字符串作为参数。对于正则表达式，请对 `RegExp` 对象使用 `test()` 方法，该方法由封装在 `//` 定界符之间的搜索字符串定义。

```javascript
let sentence = 'This is a sample string'
// 检查 'sentence' 是否包含指定的字符串参数
sentence.includes('is') // true
sentence.includes('z') // false
// 检查 'sentence' 是否匹配 RegExp 对象描述的模式
/is/.test(sentence) // true
/z/.test(sentence) // false
```

以下是在条件表达式中使用 `test()` 方法的一些示例。

```javascript
let report = 'string theory'
if (/ring/.test(report)) {
  console.log('mission success')
} // 任务成功
if (!/fire/.test(report)) {
  console.log('mission failed')
} // 任务失败
```

这里是数组处理的示例。

```javascript
let words = ['cat', 'attempt', 'tattle']
// 获取所有包含 'tt' 的元素
words.filter(w => /tt/.test(w)) // ['attempt', 'tattle']
// 检查所有元素是否包含 'at'
words.every(w => /at/.test(w)) // true
// 检查是否有任何元素包含 'stat'
words.some(w => /stat/.test(w)) // false
```

## 标志（Flags）

正则表达式的一些功能通过传递小写字母表示的标志来启用。标志类似于命令行选项，例如 `grep -i`。

本章将讨论以下标志：

- `i`：匹配时忽略大小写。
- `g`：匹配所有出现项（默认匹配第一个）。

下面是 `i` 标志的示例。`g` 标志将在本章后面的 `replace()` 方法部分讨论。

```javascript
/cat/.test('CaT') // false
/cat/i.test('CaT') // true
['Cat', 'CATER', 'SCat'].filter(w => /cat/i.test(w)) // 匹配所有的项
```

## `RegExp` 构造函数与复用

`RegExp` 对象可以保存到变量中。这有助于提高清晰度并实现复用。

```javascript
const pet = /dog/
pet.test('They bought a dog') // true
pet.test('A cat') // false
```

`RegExp` 对象也可以使用 `RegExp()` 构建。第一个参数是字符串或 `RegExp` 对象。如果需要标志，请将它们作为第二个参数。构造函数的主要优势是可以动态构建正则。例如，插入变量的内容或表达式的结果：

```javascript
let greeting = 'hi'
const pat1 = new RegExp(`${greeting}`) // /hi/
const pat = new RegExp(`${greeting.toUpperCase()}`) // /HI/
```

## `replace()` 方法

`replace()` 方法用于搜索和替换操作。

```javascript
'1,2,3,4'.replace(',', '-') // '1-2,3,4' 只替换第一个匹配
'1,2,3,4'.replace(/,/g, '-') // '1-2-3-4' 通过添加 'g' 标志替换所有匹配
'cat tart'.replace(/art/ig, '2')
```

一个常见的错误是忘记字符串是不可变的。如果你想在同一个变量中保存更改，需要将结果显式赋值回该变量。

```javascript
let word = 'c' // 这将返回字符串但不会修改 'word' 变量
word.replace(/cat/, 'hack') // 'c'
word = word.replace(/cat/, 'hack') // 需要将结果显式赋值给 word
```

![](![](img/1a4ef11dadb051ae1522899ffab370e1_11_0.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_1.png)

在 `test()` 方法中使用 `g` 标志可以使用额外功能。请查看 MDN: test。然而，在我看来，很容易养成在 `test()` 中使用 `g` 的习惯并得到意外的结果。相反，我建议使用 `match()` 方法显式编写所需的逻辑，而不是依赖 `g` 标志。

### 速查表与总结

| 注意事项 | 描述 |
| :--- | :--- |
| MDN: 正则表达式 | JavaScript 正则表达式的参考 |
| `/pat/`，一个 `RegExp` 对象 | 将正则保存在变量中以便复用、清晰等 |
| `/.test(s)` | 检查模式是否出现在输入字符串的任何位置，返回 `true` 或 `false` |
| `i` 标志 | 匹配字母时忽略大小写 |
| `g` 标志 | 匹配所有出现项 |
| `new RegExp('pat', 'i')` | 从字符串构建 `RegExp`，可选的第二个参数指定标志 |
| 使用带有 `${}` 的反引号字符串 | 用于插值 |
| `s.replace(/pat/, 'repl')` | 用于搜索和替换的方法 |

本章介绍了如何定义 `RegExp` 对象以及使用它们。你还学习了如何使用标志来更改正则的默认行为。提供的示例侧重于介绍文本处理概念。从下一章开始，你将学习正则表达式的语法和特性。

### 练习

![](img/1a4ef11dadb051ae1522899ffab370e1_11_2.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_3.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_4.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_5.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_6.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_7.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_8.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_9.png)

尝试只使用到该章节为止讨论的功能解决每章的练习。某些练习使用后续章节的技术会更容易，但这些练习的目的是探索目前为止呈现的功能。

![](img/1a4ef11dadb051ae1522899ffab370e1_11_10.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_11.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_12.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_5.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_14.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_7.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_16.png)[](img/1a4ef11dadb051ae1522899ffab370e1_11_17.png)

所有的练习也集中在 `Exercises.md` 一处。解答请查看 `Exercise_solutions.md`。

**1)** 检查给定的字符串是否包含 `"two"`，不区分大小写。

> `let s1 = 'Their artwork is exceptional'`

> `let s2 = 'one plus tw0 is not three'`

> `let s3 = 'TRUSTWORTHY'`

> `const pat1 = //` 在此处添加你的解决方案

> `pat1.test(s1)`

< `true`

> `pat1.test(s2)`

< `false`

> `pat1.test(s3)`

< `true`

**2)** 对于给定的数组，过滤掉所有包含 `"e"` 的元素。

> `let items = ['goal', 'new', 'user', 'sit', 'eat', 'dinner']`

> `items.filter(w => !test(w))` // 在此处添加你的解决方案

< `['goal', 'sit']`

**3)** 将给定字符串中仅第一次出现的 `"5"` 替换为 `"five"`。

> `let ip = 'They ate 5 apples and 5 oranges'`

> `ip.replace()` // 在此处添加你的解决方案

< `'They ate five apples and 5 oranges'`

**4)** 将给定字符串中所有出现的 `"5"` 替换为 `"five"`。

> `let ip = 'They ate 5 apples and 5 oranges'`

> `ip.replace()` // 在此处添加你的解决方案

< `'They ate five apples and five oranges'`

**5)** 将所有不区分大小写的 `"note"` 替换为 `"X"`。

> `let ip = 'This note should not be NoTeD'`

> `ip.replace()` // 在此处添加你的解决方案

< `'This X should not be XD'`

**6)** 对于给定的多行输入字符串，过滤掉所有不包含字符串 `"2"` 的行。

> `let purchases = \`items qty`
>
> `apple 24`
>
> `mango 50`
>
> `guava 42`
>
> `onion 31`
>
> `water 10\``

> `const num = //` 在此处添加你的解决方案

> `console.log(purchases.split('\n')`
>
> `.filter(e => !test(e))` // 在此处添加你的解决方案
>
> `.join('\n'))`

< `items qty`

< `mango 50`

< `onion 31`



`water 10`

![](img/1a4ef11dadb051ae1522899ffab370e1_13_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_13_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_13_2.png)![](img/1a4ef11dadb051ae1522899ffab370e1_13_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_13_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_13_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_13_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_13_7.png)

在读完“点元字符和量词”章节结束时，你就能仅使用`replace()`方法来解决这个问题。

**7)** 对于给定的数组，过滤出所有包含 "a" 或 "w" 的元素。

> **let** `items = ['goal', 'new', 'user', 'sit', 'eat', 'dinner']`

> `items.filter(w => test(w) || test(w))` //在此处添加你的解决方案

< `['goal', 'new']`

**8)** 对于给定的数组，过滤出同时包含 "e" 和 "n" 的元素。

> **let** `items = ['goal', 'new', 'user', 'sit', 'eat', 'dinner']`

> `items.filter(w => test(w) && test(w))` //在此处添加你的解决方案

< `['new', 'dinner']`

**9)** 对于给定的字符串，将开头的 "start" 替换为 "beginning"，将结尾的 "end" 替换为 "finish"。

> **let** `ip = 'start and end'`

> `ip.replace()` //在此处添加你的解决方案

< `'beginning and finish'`

## 锚点 (Anchors)

在本章中，你将学习如何限定模式。与其在字符串的任何地方匹配，不如指定位置。现在你将看到正则表达式的特性。在后面的章节中，你将学习如何定义规则。

这些限制通过为某些字符和序列赋予特殊含义来实现。具有特殊含义的字符被称为正则表达式中的**元字符**。如果你需要字面匹配这些字符，则需要用反斜杠进行转义（参见“转义字符”章节）。

### 字符串锚点 (String anchors)

这种限制是关于匹配字符串的开头或结尾的。它们提供了类似于字符串`startsWith()`和`endsWith()`方法的功能。

首先，`^`字符将匹配限制在字符串的开头。`^`作为搜索项的前缀放置。

> `/^cat/.test('cater')`

< `true`

> `/^cat/.test('concatenation')`

< `false`

> `/^hi/.test('hi top')`

< `true`

> `/^top/.test('hi top')`

< `false`

将匹配限制在字符串的结尾，使用`$`字符。`$`作为搜索项的后缀放置。

> `/are$/.test('spare')`

< `true`

> `/are$/.test('nearest')`

< `false`

> **let** `words = ['surrender', 'newer', 'door', 'pest']`

> `words.filter(w => /are$/.test(w))`

< `['surrender', 'newer']`

> `words.filter(w => /t$/.test(w))`

< `['pest']`

结合开头和结尾锚点，你可以限制匹配整个字符串。这种效果类似于使用`===`运算符。

> `/^cat$/.test('cat')`

< `true`

> `/^cat$/.test('cater')`

< `false`

你可以通过使用锚点本身来模拟字符串拼接。

```
// 在字符串开头插入文本
> 'live'.replace(/^/, 're')
```

### 行锚点 (Line anchors)

字符串输入可能包含单行或多行。`\r`和`\n`（行分隔符）被视为行分隔符。当使用`m`标志时，`^`和`$`锚点分别匹配每一行的开头和结尾。

```
// 检查字符串中是否有任何行以 'top' 开头
> /^top/m('hi top')
< true

// 检查字符串中是否有任何行以 'er' 结尾
> /er$/m('spare\nare')
< false

// 过滤以 'are' 结尾的元素
> **let** elements = ['spare', 'par', 'dare', 'spared']
> elements.filter(e => /are$/m.test(e))
< ['spare', 'dare']

// 检查字符串中是否有整行为 'par'
> /^par$/m('spare\nare')
< true
```

就像字符串锚点一样，你可以行锚点本身作为模式。

```
> **let** items = 'catapults\nconcatenate\ncat'
> console.log(items.replace(/^/gm, '* '))
< * catapults
* concatenate
* cat

> console.log(items.replace(/$/gm, '.'))
< catapults.
.concatenate.
cat.
```

![](img/1a4ef11dadb051ae1522899ffab370e1_16_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_2.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_7.png)

如果处理基于 Windows 系统的文本文件，你可能需要先将`\r\n`行终止转换为`\n`。否则，你将获得`\r`和`\n`字符的行尾匹配。你也可以通过正则表达式处理此情况，将`\r`变为可选字符（参见“贪婪量词”章节的示例）。

如果在字符串结尾有行分隔符，则会有额外的行/行尾匹配。

```
// 'fig ' 被插入了三次
> console.log('1\n2\n'.replace(/^/gm, 'fig '))
< fig 1
fig 2
fig

> console.log('1\n2\n'.replace(/$/mg, ' apple'))
< 1 apple
2 apple
apple
```

![](img/1a4ef11dadb051ae1522899ffab370e1_16_10.png)![](img/1a4ef11dadb051ae1522899ffab370e1_16_9.png)

### 单词锚点 (Word anchors)

第三种限制是单词锚点。字母（不区分大小写）、数字和下划线字符被视为单词字符。你可能会奇怪为什么还有数字和下划线，而不只是字母？这源于变量和函数的命名规范——通常允许字母、数字和下划线。因此，定义更面向编程语言而非自然语言。

转义序列`\b`表示单词边界。这适用于单词的开头和结尾锚点。

```
> **let** words = 'par spar apparent spare part'

// 无论 'par' 出现在什么地方都替换
> words.replace(/par/g, 'X')
< 'X sX apXent sXe Xt'

// 仅在单词开头替换 'par'
> words.replace(/\bpar/g, 'X')
< 'X spar apparent spare Xt'

// 仅在单词结尾替换 'par'
> words.replace(/par\b/g, 'X')
< 'X sX apparent spare part'

// 仅当 'par' 不属于另一个单词时时替换
> words.replace(/\bpar\b/g, 'X')
< 'X spar apparent spare part'
```

将单词边界作为模式本身使用可以产生创造性的解决方案：

```
// 将由空格分隔的单词转换为双引号括的 csv
// 注意这里使用了两次 'replace' 方法
> let words = 'par spar apparent spare part'
> console.log(words.replace(/\b/g, '"').replace(/ /g, ','))
< "par","spar","apparent","spare","part"

// 让编程语句更具可读性
// 这里的示例仅用于说明目的，不适用于所有情况
> 'output=num1+35\*42/num2'.replace(/\b/g, ' ')
< ' output = num1 + 35 \* 42 / num2 '

// 字符串开头结尾的多余空格可以被修剪
// 稍后你将学习如何添加限定符，这样就不需要 trim
> 'output=num1+35\*42/num2'.replace(/\b/g, ' ').trim()
< 'output = num1 + 35 \* 42 / num2'
```

## 反向单词锚点 (Opposite Word Anchor)

单词边界也有反向锚点。

`\B`匹配任何`\b`不匹配的地方。

这种双重性在其他转义序列中也会出现。负逻辑在许多文本处理场景中非常有用。但请谨慎使用，你可能会匹配到你无预想要的内容！

```
> let words = 'par spar apparent spare part'

// 如果 'par' 不在单词开头，则替换
> words.replace(/\Bpar/g, 'X')
< 'par sX apXent sXe part'

// 替换单词末尾的 'par'但不是整个单词 'par'
> words.replace(/\Bpar\b/g, 'X')
< 'par sX apparent spare part'

// 如果 'par' 不在单词末尾，则替换
> words.replace(/par\B/g, 'X')
< 'par spar apXent sXe Xt'

// 如果 'par' 被单词字符包围，则替换
> words.replace(/\Bpar\B/g, 'X')
< 'par spar apXent sXe part'
```

这里是一些独立的模式用法，用于对比这两个单词锚点。

```
> 'copper'.replace(/\b/g, ':')
< ':copper:'

> 'copper'.replace(/\B/g, ':')
< 'c:o:p:p:e:r'

> '-----hello-----'.replace(/\b/g, ' ')
< '----- hello -----'

> '-----hello-----'.replace(/\B/g, ' ')
< ' - - - - -h e l l o- - - - - '
```

## 快速查表与总结 (Cheatsheet and Summary)

| Note | 描述 |
| :--- | :--- |
| 元字符 | 在正则表达式中具有特殊含义的字符 |
| `^` | 限制匹配到字符串开头 |
| `$` | 限制匹配到字符串结尾 |
| `m` | 匹配行开头/结尾的标记 |
| `^` 和 `$` | 锚点 |
| `\r`, `\n`, `\r\n` 和 `\n` | 是行分隔符 |
| DOS 风格的文件使用 `\r\n`，可能需要特别注意 |
| `\b` | 限制匹配单词的开头和结尾；单词字符：字母、数字、下划线 |
| `\B` | 匹配任何 `\b` 不匹配的地方 |

在本章中，你已经开始接触正则表达式的构建块以及它们如何以有趣的方式被使用。但同时，正则表达式只是文本处理领域中的另一种工具。通常，你可以通过将正则表达式与其他字符串方法和表达式结合来获得更简单的解决方案。实践、经验和想象力将帮助你构建创造性的解决方案。在接下来的章节中，你将看到锚点与其他正则表达式特征结合的示例。

## 练习题 (Exercises)

**1)** 检查给定的输入字符串是否包含整个单词 "is" 或 "the"。

```
> let str1 = 'is; (this)'
> let str2 = "The food isn't good"
> let str3 = 'the2 cats'
> let str4 = 'switch on the light'
> const pat1 = // 在此处添加你的解决方案
> const pat2 = // 在此处添加你的解决方案
> pat1.test(str1) || pat2.test(str1)
< true
> pat1.test(str2) || pat2.test(str2)
< false
> pat1.test(str3) || pat2.test(str3)
< false
> pat1.test(str4) || pat2.test(str4)
< true
```

**2)** 对于给定的输入字符串，仅将整个单词 "red" 改为 "brown"。

```
> let ip = 'bred red spread credible red;'
> ip.replace() // 在此处添加你的解决方案
< 'bred brown spread credible brown;'
```

**3)** 对于数组，过滤所有包含被单词字符包围的 "42" 的元素。

```
> let items = ['hi42bye', 'nice1423', 'bad42', 'cool_42a', 'fake4b']
> items.filter(e => test(e)) // 在此处添加你的解决方案
< ['hi42bye', 'nice1423', 'cool_42a']
```

**4)** 对于给定的输入数组，过滤所有以 "den"开头或以 "den" 结尾的元素。

```
> let items = ['lovely', 'dentist', 'eden', 'fly', 'dent']
> items.filter(e => test(e) || test(e)) // 在此处添加你的解决方案
< ['lovely', 'dent']
```

**5)** 对于给定的输入字符串，仅当 "mall" 在行开头时，将整个单词 "mall" 改为 "ball"。

```
> let para = `mall call ball tall
mall call ball tall`
> console.log(para.replace()) // 在此处添加你的解决方案
< `ball call ball tall
ball call ball tall`
```

**6)** 对于给定的输入数组，过滤所有以 "den"开头或以 "den" 结尾的行。

```
> let items = ['lovely', 'dentist', 'eden', 'flyfar', 'dent']
> items.filter(e => test(e) || test(e)) // 在此处添加你的解决方案
< ['dentist', 'eden', 'flyfar', 'dent']
```

**7)** 对于给定的输入数组，不区分大小过滤所有整个单词 "three"。

```
> let items = ['three', 'Three', 'three']
> items.filter(e => test(e)) // 在此处添加你的解决方案
< ['Three']
```

**8)** 对于给定的输入数组，对于所有以 hand 开头并跟随至少一个字符的元素，将 "hand" 替换为 "X"。

```
> let items = ['handed', 'handy', 'unhandled']
> items.map(w => w.replace()) // 在此处添加你的解决方案
< ['ed', 'Xy']
```

**9)** 对于给定的输入数组，过滤所有以 "hand" 开头的元素，并将这些元素替换为 "X"。

```
> let items = ['handed', 'handy', 'unhandled', 'handle']
> items.filter(w => test(w)).map(w => w.replace()) // 在此处添加你的解决方案
< ['Xed', 'Xy']
```

**10)** 为什么以下代码显示 false 而不是 true？

```
> /end$/.test('bend it')
< false
```

## 选择与分组 (Alternation and Grouping)

很多时候，你想检查输入字符串是否匹配多个模式。例如，产品的颜色是绿色、蓝色或红色。本章将展示如何在这种情况下使用分支。这些模式之间可能存在共同部分，在这种情况下分组有助于形成更简洁的正则。本章还将讨论确定哪种分支胜出的优先级规则。

### 选择 (Alternation)

逻辑或表达式在满足任何一个条件时为真。同样，在正则表达式中，你可以使用`|`元字符组合多个模式。如果在输入字符串中找到了任何一个分支，匹配将成功。这些分支具有正则表达式的完整功能，例如它们可以拥有独立的锚点。是一些示例。

```
// 匹配 'cat' 或 'dog'
> const pets = /cat|dog/
> pets.test('I like cats')
```



```javascript
< true

> pets.test('I like dogs')

< true

> pets.test('I like parrots')

< false

// 替换字符串开头的 'cat' 或单词结尾的 'cat'

> 'catapults concatenate scat cater'.replace(/^cat|cat\b/g, 'X')

< 'Xapults concatenate sX cater'

// 将 'cat' 或 'dog' 或 'fox' 替换为 'mammal'

> 'cat dog bee parrot fox'.replace(/cat|dog|fox/g, 'mammal')

< 'mammal mammal bee parrot mammal'
```

![](img/1a4ef11dadb051ae1522899ffab370e1_21_0.png)(img/1a4ef11dadb051ae1522899ffab370e1_21_1.png)(img/1a4ef11dadb051ae1522899ffab370e1_21_2.png)

### 分组（Grouping）

通常，正则表达式分支之间存在一些共同部分。这可能是共同字符、像锚之类的限定符。在这种情况下，你可以使用一对括号元字符对它们进行分组。

类似于：

`a(b+c)d = abd+acd`

在数学中，你得到：

`a(b|c)d = abd|acd`

在正则表达式中。

```javascript
// 不分组

> 'red reform read arrest'.replace(/reform|rest/g, 'X')

< 'red X read arX'

// 使用分组

> 'red reform read arrest'.replace(/re(form|st)/g, 'X')

< 'red X read arX'

// 不使用分组

> 'par spare part party'.replace(/\bpar\b|\bpart\b/g, 'X')

< 'X spare X party'

// 提取公共锚点

> 'par spare part party'.replace(/\b(par|part)\b/g, 'X')

< 'X spare X party'

// 同时也提取公共字符

// 你稍后会学习一种更好的技术，而不是使用空交替

> 'par spare part party'.replace(/\bpar(|t)\b/g, 'X')

< 'X spare X party'
```

![](img/1a4ef11dadb051ae1522899ffab370e1_22_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_22_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_22_2.png)![](img/1a4ef11dadb051ae1522899ffab370e1_22_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_22_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_22_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_22_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_22_7.png)

分组的用途不仅是形成更简洁的正则表达式。我们将在后续章节中在相关时进行讨论。

## 优先级规则

在使用交替符（alternation）时存在一些复杂的情况。如果用于通过对字符串输入的匹配测试来获取布尔结果，则没有歧义。

然而，对于字符串替换等情况，它取决于几个因素。例如，你想替换 "are" 或 "spared" —— 哪一个优先级更高？是较大的单词 "spared"，还是它内部的子字符串 "are"，还是基于其他什么？

在输入字符串中最早匹配的正则交替项获得优先级。

```javascript
> let words = 'lion elephant are rope not'

// 对于给定的输入，'on' 的起始索引 < 'ant' 的索引

// 所以无论交替的顺序如何，'on' 都会被替换

> words.replace(/on|ant/, 'X')

< 'liX elephant are rope not'

> words.replace(/ant|on/, 'X')

< 'liX elephant are rope not'
```

如果交替项具有相同的起始索引怎么办？优先级按照声明的顺序从左到右。

```javascript
> let mood = 'best years'

// 'year' 和 'years' 的起始索引始终相同

// 因此，哪一个被替换取决于交替的顺序

> mood.replace(/year|years/, 'X')

< 'best Xs'

> mood.replace(/years|year/, 'X')

< 'best X'
```

这里有另一个例子来让你深入理解这个问题。

```javascript
> let sample = 'ear xerox at mare part learn eye'

// 这等同于：replace(/ar/g, 'X')

> sample.replace(/ar|are|art/g, 'X')

< 'eX xerox at mXe pXt leXn eye'

// 这等同于：replace(/are|ar/g, 'X')

> sample.replace(/are|ar|art/g, 'X')

< 'eX xerox at mX pXt leXn eye'

// 呼，终于这个按预期工作了

> sample.replace(/are|art|ar/g, 'X')

< 'eX xerox at mX pX leXn eye'
```

## 备查表与总结

| Note | Description |
| :--- | :--- |
| `pat1\|pat2\|pat3` | 多个正则组合为条件或；每个交替项都可以有独立的锚点 |
| `()` | 分组模式 |
| `a(b\|c)d` | 等同于 `abd\|acd` |
| 交替优先级 | 在输入中最早匹配的模式获得优先级；如果匹配具有相同的起始位置，则决胜因素是从左到右 |

所以，这一章是关于如何使用 `|` 元字符在同一个正则表达式中指定一个或多个交替匹配项。如果交替项具有公共部分，可以使用 `()` 分组进一步简化。在这些交替项中，最早匹配的模式获得优先级。如果多个交替项具有相同的起始位置，则使用从左到右的顺序作为决胜因素。在下一章中，你将学习如何从字符串数组构造交替模式，并注意优先级规则。分组还有其他用途，将在后续章节中讨论。

### 练习

**1)** 对于给定的输入数组，过滤所有以 "den" 开头或以 "ly" 结尾的元素。

```javascript
> let items = ['lovely', '1\ndist', '2 lonely', 'eden', 'fly\n', 'dent']

> items.filter()

// 在此处添加你的解决方案

< ['lovely', '2 lonely', 'dent']
```

**2)** 对于给定的数组，过滤所有包含以 "den" 开头或以 "ly" 结尾的行的元素。

```javascript
> let items = ['lovely', '1\ndist', '2 lonely', 'eden', 'fly\n', 'dent']

> items.filter()

// 在此处添加你的解决方案

< ['lovely', '2 lonely', 'dent']
```

**3)** 对于给定的输入字符串，将所有的 "removed" 或 "reed" 或 "refused" 替换为 "X"。

```javascript
> let s1 = 'creed removed read'

> let s2 = 'refused redo'

> const pat1 = // 在此处添加你的解决方案

> s1.replace(pat1, 'X')

< 'cX refuse read'

> s2.replace(pat1, 'X')

< 'X redo X'
```

**4)** 对于给定的输入字符串，将 "late" 或 "later" 或 "lated" 替换为 "X"。

```javascript
> let str1 = 'plate full of slate'

> let str2 = "lated for later, don't be late"

> const pat2 = // 在此处添加你的解决方案

> str1.replace(pat2, 'X')

< 'pA full of sA'
```

## 转义元字符

你已经看到了一些元字符和转义序列，它们有助于构建正则表达式。本章将展示如何在从字符串构建正则表达式时处理这些特殊字符。

### 使用反斜杠转义

为了字面匹配元字符，即移除它们的特殊含义，在前面加上反斜杠。尽管 `^` 没有被用作锚点：

```javascript
> /b^/.test('a^2')

< false

// 转义将有效

> /b\^/.test('a^2')

< true

// 字面匹配 ( 或 )

> '(a\*b) + c'.replace(/\)/g, '')

< '(a\*b() + c'
```

## 动态转义元字符

当你自己定义正则表达式时，可以手动转义元字符。然而，如果你从其他地方获取字符串并需要字面匹配，需要在构造正则表达式时转义所有的元字符。解决方案是使用正则表达式！通常，编程语言本身会提供内置方法。JavaScript 没有，但 MDN 正则表达式指南以函数形式涵盖了这一点，如下所示：

```javascript
> function escapeRegExp(string) {

// 应该是替换所有元字符的逻辑

}
```

上面的正则表达式中有很多你还没有学的概念。它们将在后续章节中讨论。现在，只需知道这个函数会自动转义所有的元字符。示例如下：

```javascript
// 应用正则表达式的示例输入

> let eqn = 'f*(a^b) - 3*(a^b)'

// 从其他地方获取需要字面匹配的示例字符串

> const usr_str = '(a^b)'

// 情况 1：替换所有匹配

// 使用 'escapeRegExp' 函数转义元字符

> const pat = new RegExp(escapeRegExp(usr_str), 'g')

> pat

< /\(a\^b\)/g

> eqn.replace(pat, 'c')

< 'f*c - 3*c'

// 情况 2：仅在字符串末尾

> eqn.replace(new RegExp(escapeRegExp(usr_str) + '$'), 'c')

"f*(a^b) - 3*c"
```



```js
const pat1 = // 在此处添加你的解决方案
```

```js
s1.replace(pat1, 'X')
```

< `'cX refuse read'`

```js
s2.replace(pat1, 'X')
```

< `'X redo X'`

**4)** 对于给定的输入字符串，将 `"late"` 或 `"later"` 或 `"lated"` 替换为 `"X"`。

```js
let str1 = 'plate full of slate'
let str2 = "lated for later, don't be late"
const pat2 = // 在此处添加你的解决方案
```

```js
str1.replace(pat2, 'X')
```

< `'pA full of sA'`

## 转义元字符

你已经看到了一些元字符和转义序列，它们有助于构建正则表达式。本章将展示如何在从字符串构建正则表达式时处理这些特殊字符。

### 使用反斜杠转义

为了字面匹配元字符，即移除它们的特殊含义，在前面加上反斜杠。尽管 `^` 没有被用作锚点：

```js
/b^/.test('a^2')
```

< `false`

转义将有效：

```js
/b\^/.test('a^2')
```

< `true`

字面匹配 `(` 或 `)`：

```js
'(a\*b) + c'.replace(/\)/g, '')
```

< `'(a\*b( + c'`

```js
'\\learn/'.replace(/\//g, '/')
```

< `'/learn'`

## 动态转义元字符

当你自己定义正则表达式时，可以手动转义元字符。然而，如果你从其他地方获取字符串并需要字面匹配，需要在构造正则表达式时转义所有的元字符。解决方案是使用正则表达式！通常，编程语言本身会提供内置方法。JavaScript 没有，但 MDN 正则表达式指南以函数形式涵盖了这一点，如下所示：

```js
function escapeRegExp(string) {
  return string.replace(/[.*+?}()|[\]\]/g, '\\$&')
}
```

上面的正则表达式中有很多你还没有学的概念。它们将在后续章节中讨论。现在，只需知道这个函数会自动转义所有的元字符。示例如下：

```js
// 应用正则表达式的示例输入
let eqn = 'f*(a^b) - 3*(a^b)'

// 从其他地方获取需要字面匹配的示例字符串
const usr_str = '(a^b)'

// 情况 1：替换所有匹配
// 使用 'escapeRegExp' 函数转义元字符
const pat = new RegExp(escapeRegExp(usr_str), 'g')
```

```js
pat
```

< `/\(a\^b\)/g`

```js
eqn.replace(pat, 'c')
```

< `'f*c - 3*c'`

情况 2：仅在字符串末尾：

```js
eqn.replace(new RegExp(escapeRegExp(usr_str) + '$'), 'c')
```

< `"f*(a^b) - 3*c"`

`XRegExp` 工具类提供了如 `XRegExp.escape()` 和 `XRegExp.union()` 等实用方法。`union` 方法具有额外功能，允许字符串和 RegExp 字面量混合使用，并且处理反向引用的重新编号。

### `source` 和 `flags` 属性

如果你需要一个 RegExp 对象的内容，可以使用 `source` 和 `flags` 属性分别获取模式字符串和标志（flags）。这些方法可以帮助你使用另一个 RegExp 对象的内容构建一个新的 RegExp 对象。

```js
const p3 = /\bpar\b/
const p4 = new RegExp(p3.source + '|cat', 'g')
```

```js
p4
```

< `/\bpar\b|cat/g`

```js
console.log(p4.source)
```

< `\bpar\b`

```js
p4.flags
```

< `'g'`

```js
'cater concatenate par spare'.replace(p4, 'X')
```

< `'Xer X conXenate X spare'`

### 转义分隔符

另一个需要注意转义的字符是用于定义 RegExp 字面量的定界符。或者根据模式，你可以使用 `new RegExp` 构造函数来避免转义。

```js
let path = '/home/joe/report/sales/ip.txt'

// 这被称为“倾斜牙签症”（leaning toothpick syndrome）
path.replace(/^\/home\/joe\//, '~/')
```

< `'~/report/sales/ip.txt'`

使用 `new RegExp` 可以提高可读性并减少拼写错误：

```js
path.replace(new RegExp(`/home\/joe/`), '~/')
```

< `'~/report/sales/ip.txt'`

### 转义序列

某些字符如制表符和换行符可以使用转义序列 `\t` 和 `\n` 分别表示。这与它们在字符串字面量中的处理方式相似。然而，如所示，`\b` 在正则中表示边界，而在字符串中表示退格字符。此外，还有几个特定于正则的序列。完整列表见 MDN 文档的**特殊字符**章节。这些包括：`\b`、`\B`、`\cX`、`\D`、`\f`、`\k`、`\n`、`\p`、`\P`、`\r`、`\s`、`\S`、`\t`、`\v`、`\w` 和 `\W`。以下是一些示例：

```js
'a\tb'.replace(/\t/g, ':')
```

< `'a:b:c'`

```js
'1\n23'.replace(/\n/g, ' ')
```

< `'1 2 3'`

当从字符串字面量构建正则时，如果需要表示单个反斜杠，请使用 `\\`：

```js
new RegExp('123\\tab')
```

< `/123\tab/`

```js
new RegExp('123\\\\tab')
```

< `/123\\tab/`

这里是另一个示例的控制台截图。

如果转义序列未定义，它将被视为其所转义的字符；在这里，`\e` 被视为 `e`。

```js
/e/.test('hello')
```

< `true`

你还可以使用十六进制转义格式 `\xh` 来表示字符。如果你使用转义来表示元字符，它将作为字面量处理，而不是其元字符功能。Codepoints 章节将讨论 Unicode 字符的转义。`\x20` 是空格字符。

```js
'he lo'.replace(/\x20/g, '')
```

< `'hello'`

`\x7c` 是 `|` 字符，但它不会被视为逻辑或元字符：

```js
'12|30'.replace(/\x7c3/g, '5')
```

< `'150'`

```js
'12|30'.replace(/2|3/g, '5')
```

< `'15|50'`

查看 ASCII 表可以获得包含所有 ASCII 字符及其十六进制表示的便捷快速查表。

### 快速查表与总结

| 笔记 | 描述 |
| :--- | :--- |
| `\\` | 对元字符前加前缀以进行字面量匹配 |
| `source` 属性 | 将 RegExp 对象转换为字符串 |
| `flags` 属性 | 获取 RegExp 对象的标志，以便将 RegExp 插入另一个 RegExp 中 |
| `RegExp(`pat`)` | 帮助避免或减少对分隔符字符的转义 |
| 分支优先级规则 | 如果匹配位置相同，则从左到右 |
| 健壮解决方案 | 根据长度对分支进行排序，最长优先 |
| `\t` | 类似于字符串字面量支持的转义序列 |
| `\b` | 在正则中是单词边界，在字符串字面量中是退格 |
| `\e` | 未定义的转义将匹配其转义的字符 |
| `\xh` | 使用十六进制值表示字符 |
| `\x7c` | 字面量匹配 |

### 练习题

**1)** 在两个字符串中使用相同的逻辑将给定的输入字符串转换为预期输出。

```js
let str1 = '(9-2)*5+qty/3-(9-2)*7'
let str2 = '(qty+4)/2-(9-2)*5+pq/4'
const pat1 = // 在此处添加你的解决方案
```

```js
str1.replace() // 在此处添加你的解决方案
```

< `'35+qty/3-(9-2)*7'`

```js
str2.replace() // 在此处添加你的解决方案
```

< `'(qty+4)/2-35+pq/4'`

**2)** 仅在给定字符串的开头或结尾将 `(4)\|` 替换为 `2`。



```javascript
let s1 = '2.3/(4)\|6 5.3-(4)\|';
let s2 = '(4)\|42 - (4)\|3';
let s3 = 'two - (4)\\n';
const pat2 = // 在此处添加你的解决方案
s1.replace()
'2.3/2 5.3-2'
s2.replace()
'242 - 3'
s3.replace()
```

**3)** 将给定字符串中 `items` 数组中的任何匹配元素替换为 `X`。假设两个元素不会产生冲突。

```javascript
let items = ['(a.b)', '(a+b)', 'x', 'price', '{n'];
const pat3 = // 在此处添加你的解决方案
items.map(item => item.replace(pat3, 'X'))
['X', 'X', 'X', 'X', 'X']
```

**4)** 将给定输入中的退格字符替换为空格。

```javascript
let ip = '0bcd\xb3ze';
const pat4 = // 在此处添加你的解决方案
ip.replace(pat4, ' ')
'0bcd 3ze'
```

**5)** 在给定字符串中替换所有的 `\e`。

```javascript
let ip = 'there aspects among';
const pat5 = // 在此处添加你的解决方案
ip.replace(pat5, 'X')
'thX aspects among'
```

**6)** 在输入字符串中替换 `items` 数组中的任何匹配项。

```javascript
let ip = '3abcd';
const pat6 = // 在此处添加你的解决方案
ip.replace(pat6, 'X')
'3Xcd'
```

使用可选的 `limit` 参数来指定输出元素的最大数量：

```javascript
'apple-85-mango-70'.split(/-/, 2)
```

```javascript
['apple', '85']
```

使用点元字符的示例：

```javascript
'bus:3:car:-:van'.split(/:.:/)
```

```javascript
['bus', 'car', 'van']
```

请参见 `split()` 与捕获组章节，了解捕获组如何影响 `split()` 方法输出的细节。

## 贪婪量词

量词可以帮助你重复正则表达式的一部分。它们可以应用于字面字符、分组以及你之后将学习的其他特征。除了能够指定精确的数量和边界范围外，这些量词还可以匹配无限制的变数量。如果输入字符串可以通过多种方式满足具有变数量的模式，你可以从两种类型的量词中进行选择以缩小可能性。在本节中，将介绍**贪婪**类型的量词。

首先是 `?` 元字符，它将字符或分组量化为匹配 0 次或 1 次。换句话说，你将该部分设置为可选匹配。与分支和分组相比，这会导致正则表达式更简洁。

等同于：`/ear|ar/g`

```javascript
'far feat flare fear'.replace(/e?ar/g, 'X')
```

```javascript
'fX feat flXe fX'
```

等同于：`/\bpar(t|)\b/g`

```javascript
'par spare part party'.replace(/\bpart?\b/g, 'X')
```

```javascript
'X spare X party'
```

等同于：`/\b(re.d|red)\b/`

```javascript
['red', 'ready', 're;d', 'redo', 'reed'].filter(w => /\bre.?d\b/.test(w))
```

```javascript
['red', 're;d', 'reed']
```

等同于：`/part|parrot/g`

```javascript
'par part parrot parent'.replace(/par(ro)?t/g, 'X')
```

```javascript
'par X X parent'
```

等同于：`/part|parrot|parent/g`

```javascript
'par part parrot parent'.replace(/par(en|ro)?t/g, 'X')
```

```javascript
'par X X X'
```

`*` 元字符将字符或分组量化为匹配 0 次或多次。它没有上限。

匹配 `t` 后面跟随零或多个 `a`，然后再跟 `r`：

```javascript
'tr tear tare steer sitaara'.replace(/ta*r/g, 'X')
```

```javascript
'X tear Xe steer siXa'
```

匹配 `t` 后面跟随零或多个 `e` 或 `a`，然后再跟 `r`：

```javascript
'tr tear tare steer sitaara'.replace(/t(e|a)*r/g, 'X')
```

```javascript
'X X Xe sX siXa'
```

匹配零个或多个 `1`，后面跟随 `2`：

```javascript
'3111111111125111142'.replace(/1*2/g, 'X')
```

```javascript
'3X511114X'
```

这里是 `split()` 方法的其他示例。

最后一个元素是空的，因为字符串末尾的 `2` 之后没有内容：

```javascript
'3111111111125111142'.split(/1*2/)
```

```javascript
['3', '511114', '']
```

注意 `25` 和 `42` 是如何被分割的，它们之间有零个 `1`：

```javascript
'3111111111125111142'.split(/1*/)
```

```javascript
['3', '2', '5', '4', '2']
```

`+` 元字符将字符或分组量化为匹配 1 次或多次。与 `*` 量词类似，它没有上限。重要的是，它不会匹配空字符串等意外内容。

```javascript
'tr tear tare steer sitaara'.replace(/ta+r/g, 'X')
```

```javascript
'tr tear Xe steer siXa'
```

```javascript
'tr tear tare steer sitaara'.replace(/t(e|a)+r/g, 'X')
```

```javascript
'tr X Xe sX siXa'
```

```javascript
'3111111111125111142'.replace(/1+2/g, 'X')
```

```javascript
'3X5111142'
```

```javascript
'3111111111125111142'.split(/1+/)
```

```javascript
['3', '25', '42']
```

你可以使用 `{}` 元字符指定整数范围，包括有界和无界。使用此量词有三种方法，如下所示。

| 量词 | 描述 |
| :--- | :--- |
| `{m,n}` | 匹配 `m` 到 `n` 次 |
| `{m,}` | 至少匹配 `m` 次 |
| `{n}` | 恰好匹配 `n` 次 |

```javascript
let repeats = ['abc', 'ac', 'abbc', 'xabbbcz', 'bc', 'abbbbbc'];
```

```javascript
repeats.filter(w => /ab{1,4}c/.test(w))
```

```javascript
['abc', 'abbc', 'xabbbcz']
```

```javascript
repeats.filter(w => /ab{0,2}c/.test(w))
```

```javascript
['ac', 'abbc']
```

```javascript
repeats.filter(w => /ab{3,}c/.test(w))
```

```javascript
['xabbbcz']
```

`.*?` 将首先从空匹配开始，然后一次向前移动一个字符，直到找到匹配项。

贪婪模式将从第一个 `:` 匹配到最后一个 `:`：

```javascript
'green:3.14:teal::brown:oh!:blue'.split(/:.*:/)
```

```javascript
['green', 'blue']
```

非贪婪模式将从 `:` 匹配到下一个 `:`：

```javascript
'green:3.14:teal::brown:oh!:blue'.split(/:.*?:/)
```

```javascript
['green', 'teal', 'brown', 'blue']
```

### `s` 标志

使用 `s` 标志可以让 `.` 元字符匹配 `\r`、`\n` 以及换行或段落分隔符字符。

默认情况下，`.` 元字符不匹配行分隔符：

```javascript
console.log('Hi there\nHave a Nice Day'.replace(/the.*ice/, 'X'))
```

```text
Hi there

Have a Nice Day
```

`s` 标志允许匹配行分隔符：

```javascript
console.log('Hi there\nHave a Nice Day'.replace(/the.*ice/s, 'X'))
```

```text
Hi X Day
```

### 速查表与总结

| Note | Description |
| :--- | :--- |
| `.` | 匹配除行分隔符外的任何字符 |
| `s` flag | 使用 `.` 元字符同时也匹配行分隔符 |
| greedy（贪婪） | 尽可能多匹配 |
| `?` | 贪婪量词，匹配 0 次或 1 次 |
| `*` | 贪婪量词，匹配 0 次或多次 |
| `+` | 贪婪量词，匹配 1 次或多次 |
| `{m,n}` | 贪婪量词，匹配 `m` 到 `n` 次 |



| `{m,}` | 贪婪量词，至少匹配 `m` 次 |
| `{n}` | 贪婪量词，精确匹配 `n` 次 |
| `pat1.*pat2` | `pat1` 和 `pat2` 之间的任意数量字符 |
| `pat1.*pat2|pat2.*pat1` | 以任意顺序匹配 `pat1` 和 `pat2` |
| non-greedy (非贪婪) | 在贪婪量词后添加 `?` 以尽可能少地匹配 |
| `s.split(/pat/)` | 根据正则表达式分割字符串 |

本章引入了使用占位符代替固定字符串的概念。当结合量词使用时，你已经领略了简单的正则表达式如何匹配大范围文本。在接下来的章节中，你将学习如何创建自己的受限占位符字符集。

### 练习

![](img/1a4ef11dadb051ae1522899ffab370e1_37_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_37_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_37_2.png)![](img/1a4ef11dadb051ae1522899ffab370e1_37_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_37_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_37_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_37_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_37_7.png)

根据输入字符串的内容，在这些练习中使用（或使用）`s` 标志。

**1)** 对于给定的输入，将 `42//5` 或 `42/5` 替换为 `8`。

> `let ip = 'a+42//5-c pressure\*3+42/5-14256'`

> // 在此处添加你的解决方案

< 'a+8-c pressure\*3+8-14256'`

**2)** 对于数组 `items`，过滤所有以 `hand` 开头，且后面紧跟最多一个字符或 `le` 结尾的元素。

> `let items = ['handed', 'hand', 'handled', 'handy', 'unhand', 'hands', 'handle']`

> // 在此处添加你的解决方案

< ['hand', 'handy', 'hands', 'handle']

**3)** 使用 `split()` 方法为给定的字符串获取所示的输出。

> `let eqn1 = 'a+42//5-c'`

> `let eqn2 = 'pressure\*3+42/5-14256'`

> `let eqn3 = 'r\*42-5/3+42///5-42/53+a'`

> `const pat1 =`

> // 在此处添加你的解决方案

> `eqn1.split(pat1)`

< ['a+', '-c']

> `eqn2.split(pat1)`

< ['pressure\*3+', '-14256']

> `eqn3.split(pat1)`

< ['r\*42-5/3+42///5-', '3+a']

**4)** 对于给定的输入字符串，从第一个 `i` 到字符串末尾删除所有内容。

> `let s1 = 'remove the meaning of such'`

> `let s2 = 'characters while constructing'`

> `let s3 = 'input output'`

> `const pat2 =`

> // 在此处添加你的解决方案

> `s1.replace(pat2, '')`

< 'remove the spec'

> `s2.replace(pat2, '')`

< 'characters wh'

> `s3.replace(pat2, '')`

< ''

**5)** 对于给定的字符串，构造正则表达式以获取所示的输出。

> `let s1 = 'a+b(addition)'`

> `let s2 = 'a/b(division) + c%d(#modulo)'`

> `let s3 = 'Hi there(greeting). Nice day(a(b)'`

> `const remove_parentheses =`

> // 在此处添加你的解决方案

> `str1.replace(remove_parentheses, '')`

< 'a+b'

> `s2.replace(remove_parentheses, '')`

< 'a/b + c%d'

> `s3.replace(remove_parentheses, '')`

< 'Hi there. Nice day'

**6)** 修正给定的正则表达式以获取预期输出。

> `let words = 'pl incoming winter in caution'`

> // 错误输出

> `const w1 = /int|ion|ing|inco|inter|ink/g`

> `words.replace(w1, 'X')`

< 'plX Xg wX sentient'

> // 预期输出

> `const w2 =`

> // 在此处添加你的解决方案

> `words.replace(w2, 'X')`

< 'plX mX wX sentient'

**7)** 对于给定的贪婪量词，使用 `{m,n}` 的表示形式是什么？

- `?` 等于

- `*` 等于

- `+` 等于

**8)** `(a\*|b*)` 等于 `(a|b)*`

**9)** 对于给定的输入字符串，从第一个 `i` 到字符串末尾删除所有内容，前提是它不在字符串末尾。

> `let s1 = 'this is a Test'`

> `let s2 = 'always cases'`

> `let pat3 =`

> // 在此处添加你的解决方案

> `s1.replace(pat3, '')`

< 'this is a '

> `s2.replace(pat3, '')`

< 'always '

**10)** 对于数组，过滤所有以 `s` 开头并包含 `e` 的元素。

**11)** 对于数组，删除所有少于 6 个字符的元素。

**12)** 对于数组，过滤所有以 `s` 开头或最多为 6 个字符的元素。

**13)** 从 `test` 第一次出现处删除，如果它位于行开头。

> `let s1 = 'this is a Test'`

> `let s2 = 'always test'`

> `let pat3 =`

> // 在此处添加你的解决方案

> `s1.replace(pat3, '')`

< 'this is a '

> `s2.replace(pat3, '')`

< 'always '

**14)** 你能解释为什么输出不符合预期吗？`s` 标志。

**15)** 使用 `split()` 方法为给定的输入获取所示的输出。

> `let s1 = 'a+b(addition)'`

> `let str2 = 'a/b(division) + c%d(#modulo)'`

> `let s3 = 'Hi there(greeting). Nice day(a(b)'`

> `const remove_parentheses =`

> // 在此处添加你的解决方案

> `str1.replace(remove_parentheses, '')`

< 'a+b'

> `str2.replace(remove_parentheses, '')`

< 'a/b + c%d'

> `str3.replace(remove_parentheses, '')`

< 'Hi there. Nice day'

**16)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**17)** 使用 `split()` 方法为给定的输入获取所示的输出。

**18)** 对于数组，过滤所有以 `s` 开头或最多为 6 个字符的元素。

**19)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**20)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**21)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**22)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**23)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**24)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**25)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**26)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**27)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**28)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**29)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

**30)** 对于数组，过滤所有以 `s` 开头但不在字符串末尾的元素。

### regexcrossword

为了练习，通常推荐 regexcrossword。该网站仅支持 JavaScript 版本的正则表达式。请参见 regexcrossword:howtoplay 获取帮助。

## 总结

本章简要介绍了可以帮助你理解以及交互式解决/调试正则表达式的在线工具。不同工具和编程语言之间的语法和功能可能会有所不同，有时差异很大。因此，请确保你正在使用的程序支持你所使用的正则表达式变体。

## 处理匹配部分

你已经见过了一些可以匹配不同文本的功能。在本章中，你将学习如何提取并处理这些匹配部分。文中引入了三个新方法。你还将学习一些技巧，例如在 `replace()` 方法的替换部分使用函数和字典。

### match() 方法

`match()` 方法可以以多种方式使用。

当不使用 `g` 标志且正则成功时，你将得到一个包含第一个匹配部分各种细节的数组对象。

```javascript
// note that the 'g' flag isn't used
> 'too soon a song snatch'.match(/so+n/)
< ['soon', index: 4, input: 'too soon a song snatch', groups: undefined]

// to get only the matching portion
> 'too soon a song snatch'.match(/so+n/)[0]
< 'soon'

// non-regexp object will get processed as: RegExp(object)
> 'too soon a song snatch'.match('so+n')
< ['soon', index: 4, input: 'too soon a song snatch', groups: undefined]
```

`index` 属性给出匹配部分的起始位置。`input` 属性提供使用 `match()` 方法的输入字符串。如果给正则表达式失败，输出为 `null` 而不是空数组。`groups` 属性将在"命名捕获组"中讨论。更多细节和示例请参阅 MDN: match。

```javascript
let s1 = 'cat and dog'
> s1.match(/dog/).index
< 8
> s1.match(/dog/).input
< 'cat and dog'
> s1.match(/xyz/)
< null
```

### search() 方法

`search()` 方法给出第一个匹配部分的索引。如果正则表达式失败，它返回 `-1` 作为输出。

```javascript
// same as match(/dog/).index
> 'cat and dog'.search(/dog/)
< 8
// cannot use match(/xyz/) here
> 'cat and dog'.search(/xyz/)
< -1
```

### 捕获组

分组也被称为**捕获组**。它有多个用途，其中之一是处理这些组的匹配部分。当捕获组与 `match()` 方法配合使用时，组的匹配部分也将成为数组的一部分。第一个元素始终整个匹配部分，随后是由组捕获的文本（如果存在）。

```javascript
let motivation = 'improve yourself.'
> motivation.match(/.*our/)
< ['improve your', index: 2, input: 'improve yourself.', groups: undefined]

// retrieving the entire matched portion
> motivation.match(/.*our/)[0]
< 'improve your'
```

这是一个带有捕获组的示例。最左侧的组编号为 1，第二个最左侧的为 2，以此此类推。

```javascript
let purchase = 'coffee:100g tea:250g sugar:75g chocolate:50g'
let m = purchase.match(/:(.*?)g.*:(.*?)g:(.*?)g/)
< [':100g tea:250g sugar:75g chocolate:50g', '100', '250', '50', index: 6, input: 'coffee:100g tea:250g sugar:75g chocolate:50g', groups: undefined]

// capture group portions
> m[1]
< '100'
> m[3]
< '50'
```

### d 标志

你可以使用 `d` 标志来获取匹配部分的起始和结束位置。结束位置通过将起始索引加上匹配部分的长度计算。这是一个示例：

```javascript
// note the addition of the 'indices' property
> 'awesome'.match(/so/d)
< ['so', index: 3, input: 'awesome', groups: undefined, indices: [[3, 5]]]

// start and end location of the entire matching portion
> 'awesome'.match(/so/d).indices[0]
< [3, 5]
```

这里是同时也使用捕获组的示例：

```javascript
> 'coffee:100g tea:250g'.match(/:(.*?)g/d)
< [':100g', '100', index: 6, input: 'coffee:100g tea:250g', groups: undefined, indices: [[6, 11], [7, 10]]]

// locations for the entire match
> 'coffee:100g tea:250g'.match(/:(.*?)g/d).indices[0]
< [6, 11]

// locations for the first capture group
> 'coffee:100g tea:250g'.match(/:(.*?)g/d).indices[1]
< [7, 10]
```

## 获取所有匹配部分

当使用 `g` 标志时，`match()` 方法返回所有匹配部分。捕获组部分和三个属性不会包含在输出中。

```javascript
> 'too soon a song snatch'.match(/so*n/g)
< ['soon', 'son', 'sn']
> 'too soon a song snatch'.match(/so+n/g)
< ['soon', 'son']
> 'PAR spar apparent SpArE part pare'.match(/\bs?pare?\b/ig)
< ['PAR', 'spar', 'SpArE', 'pare']

// entire matching portion is returned even if capture groups are used
> 'spar apparent spare part'.match(/\bs?par(e|t)\b/g)
< ['spare', 'part']
```

它对于调试也很有用。例如，在使用 `replace()` 方法之前查看潜在的匹配项。

```javascript
> 'green:3.14:teal::brown:oh!:blue'.match(/:.*:/g)
< [':3.14:teal::brown:oh!']
> 'green:3.14:teal::brown:oh!:blue'.match(/:.*?:/g)
< [':3.14:', '::', ':oh!']
```

### matchAll() 方法

如果你需要每个匹配的捕获组部分，请使用 `matchAll()` 方法。将返回一个迭代器作为输出。



```javascript
let arr = 'too soon a song snatch'.matchAll(/so*n/g);
// same as match(/so+n/).index
> Array.from(arr)
< [
  ['soon', index: 0, input: 'too soon a song snatch', groups: undefined, indices: [[0, 4]]],
  ['son', index: 5, input: 'too soon a song snatch', groups: undefined, indices: [[5, 8]]],
  ['sn', index: 12, input: 'too soon a song snatch', groups: undefined, indices: [[12, 14]]]
]
```

### `split()` 与捕获组

`split()` 方法同样如此。如果用于分割的模式包含捕获组，则这些组匹配的部分也将成为输出数组的一部分。

```javascript
// without capture group
> '3111111111251111426'.split(/1\*4?2/)
< ['3', '5', '6']

// to include the matching portions of the pattern as well in the output
> '3111111111251111426'.split(/(1\*4?2)/)
< ['3', '11111111112', '5', '111142', '6']
```

如果模式的部分在捕获组之外，则由此匹配的文本将不会出现在输出中。

如果捕获组未参与，它在输出数组中将表示为`undefined`。

```javascript
// 在这里 4?2 在捕获组之外，所以该部分不会出现在输出中
> '31111111111251111426'.split(/(1\*)4?2/)
< ['3', '1111111111', '5', '1111', '6']

// 多个捕获组示例
// 注意， b+ 匹配的部分并不在输出中
> '3.14aabccc42'.split(/(a+)b+(c+)/)
< ['3.14', 'aa', 'ccc', '42']

// 在这里 (4)? 在第一次匹配时匹配了 0 次
> '31111111111251111426'.split(/(1\*)(4)?2/)
< ['3', '1111111111', undefined, '5', '1111', '4', '6']
```

使用捕获组和可选的`limit`参数可以帮助你将输入字符串分为三个部分：

- 第一次匹配之前的部分
- 模式本身匹配的部分
- 模式之后的部分

```javascript
// 如果需要，也使用 's' 标记
> '3.14aabccc42abc88'.split(/(a+b+c+)(.\*)/, 3)
< ['3.14', 'aabccc', '42abc88']
```

## 在替换部分使用函数

有时，简单的替换字符串是不够的，你需要对匹配部分进行一些处理。对于这种情况，你可以在替换部分使用函数。

函数可用的参数与`match()`方法提供的细节相似。第一个参数是整个匹配部分。如果使用了捕获组，则这些组匹配的部分将随其后。然后是匹配部分的索引，最后是输入字符串。根据复杂性，你可以使用完全定义的函数或箭头函数表达式。

```javascript
> function titleCase(m) {
  return m[0].toUpperCase() + m.substr(1).toLowerCase()
}

// 仅函数名作为第二个参数就足够了
// 匹配部分的细节将自动传递给函数
// 在此示例中，'titleCase' 只使用了整个匹配部分
> 'aBc ac ADC aBbBC'.replace(/a.\*?c/ig, titleCase)
< 'Abc Ac Adc Abbbc'

// 简单情况也可以使用箭头函数表达式
> 'abc ac adc abbbc'.replace(/ab\*c/g, m => m.toUpperCase())
< 'ABC AC adc ABBBC'

// \d 稍后会介绍
// 目前，知道它将匹配所有数字字符就足够了
> '1 42 317'.replace(/\\d+/g, m => m*2)
< '2 84 634'
```

这是一个带有捕获组的示例。更多细节请参阅 MDN: `replace`。

```javascript
> function titleCase(m, g1, g2) {
  return g1.toUpperCase() + g2.toLowerCase()
}

> 'aBc ac ADC aBbBC'.replace(/(a)(.\*?c)/ig, titleCase)
< 'Abc Ac Adc Abbbc'
```

## 在替换部分使用字典

有时，使用字典可以简化替换部分所需的功能。匹配部分充当键，从字典中获取对应的值。

```javascript
// 一一对一映射
let h = { '1': 'one', '2': 'two', '4': 'four' }
> '9234012'.replace(/1|2|4/g, k => h[k])
< '9two3fouronetwo'

// 如果键不在字典中，可以提供默认值
> '9234012'.replace(/1|2|4/g, k => h[k] || 'X')
< '9twoX3fourXonetwo'

// 使用字典在处理多个替换时非常有用
// 当匹配的部分在字典中不存在时，将使用默认值
> '9234012'.replace(/1|2|4/g, k => k in h ? h[k] : 'X')
< '9twoX3fourXonetwo'

// 字典可以简化替换逻辑
let swap = { 'cat': 'tiger', 'handy': 'dog' }
> '31111111111251111426'.split(/(1\*)4?2/)
< ['3', '1111111111', undefined, '5', '1111', '4', '6']

// 字典可以用于替换
// 动态构建交替
> 'cat dog handy'.replace(/cat|handy/g, k => swap[k])
< 'tiger dog'
```

## 速查表

| 项目 | 描述 |
| :--- | :--- |
| `match(pat)` | 假设未使用`g`标记且正则成功，返回一个包含匹配部分的数组 |
| `index`属性 | 匹配的起始位置 |
| `input`属性 | 输入字符串 |
| `groups`属性 | 命名捕获组的字典 |
| `m[0]` | 对于上述情况，整个匹配部分 |
| `m[1]` | 第一个捕获组的部分 |
| `m[2]` | 第二个捕获组的部分，依此类推 |
| `g`标记 | 通过`indices`属性获取匹配部分的起始和结束位置 |
| `match(pat/g)` | 只返回匹配部分，无属性；捕获组不影响输出 |
| `null` | 如果正则失败则返回 |
| `matchAll(pat)` | 返回包含每个匹配部分及其属性的迭代器 |
| `Array.from()` | 转换为数组 |
| `search(pat)` | 返回第一次匹配的起始位置 |
| `split()` | 同样允许根据匹配的键来分割字符串 |
| `replace()` | 同样，字典可以用于替换 |
| `replace(pat, func)` | 允许在替换时使用函数 |

**练习**

**1)** 对于给定的字符串，从第一次出现提取匹配部分。

```javascript
let str1 = 'What is the biggest fruit you have seen?'
let str2 = 'Your mission is to read and practice'
const pat1 = // 你的答案
```

**2)** 找到输入字符串中`is or the or to`第一次出现的起始索引。假设每个输入至少有一个匹配。

```javascript
let s1 = 'match after the last newline character'
let s2 = 'and then you want to test'
let s3 = 'this is good bye then'
let s4 = 'who was there to see?'
const pat2 = // 你的答案
```

**3)** 找到输入字符串中`is or the or to`最后一次出现的起始索引。假设每个输入至少有一个匹配。

```javascript
let s1 = 'match after the last newline character'
let s2 = 'and then you want to test'
let s3 = 'this is good bye then'
let s4 = 'who was there to see?'
const pat3 = // 你的答案
```

**4)** 给定的输入字符串恰好包含一个`:`。提取`:`之后的所有字符作为输出。

```javascript
let ip = 'fruits:apple, mango, guava, blueberry'
```

**5)** 从给定的字符串中提取`(`和`)`之间的所有单词并作为数组（包括括号）。假设输入不会包含任何破损的括号。

```javascript
let ip = 'another (way) to reuse (portion) matched (by) capture groups'
// 在此处添加你的解决方案
< ['(way)', '(portion)', '(by)']
```

**6)** 提取所有`$`直到下一个`>`出现的所有内容，前提是`<`和`>`之间至少有一个字符。

```javascript
let ip = 'a<apple> 1<> b<bye> 2<> c<cat>'
// 在此处添加你的解决方案
< ['<apple>', '<> b<bye>', '<> c<cat>']
```

**7)** 使用`matchAll()`为给定的字符串获取如下所示所示。请注意输入字符串中使用的字符。

```javascript
let row1 = '-2,5 4,+3 +42,-53 4356246,-357532354 '
let row2 = '1.32,-3.14 634,5.63 63.3e3,990780934543.235 '
const pat4 = 
// 在此处添加你的解决方案
// 在此处为 row1 添加解决方案
< (4) [Array(2), Array(2), Array(2), Array(2)]
0: (2) ['-2', '5']
1: (2) ['4', '+3']
2: (2) ['+42', '-53']
3: (2) ['4356246', '-357532354']
length: 4
[[Prototype]]: Array(0)

// 在此处为 row2 添加解决方案
< (3) [Array(2), Array(2), Array(2)]
0: (2) ['1.32', '-3.14']
1: (2) ['634', '5.63']
2: (2) ['63.3e3', '9907809345343.235']
length: 3
[[Prototype]]: Array(0)
```

**8)** 这是对上一个题的扩展。求和每对用逗号分隔的数字。

- 对于`row1`，求整数的和。例如，`-2`和`5`的和是`3`。
- 对于`row2`，求浮点数的和。例如，`1.32`和`-3.14`的和是`-1.82`。

```javascript
let row1 = '-2,5 4,+3 +42,-53 4356246,-357532354 '
let row2 = '1.32,-3.14 634,5.63 63.3e3,9907809345343.235 '
// 应与上一个问题相同
const pat5 = 
// 在此处添加你的解决方案
// 在此处为 row1 添加解决方案
< [3, 7, -11, -353176108]

// 在此处为 row2 添加解决方案
< [-1.82, 639.63, 9907809408643.234]
```

**9)** 使用`split()`方法获取如下所示的输出。

```javascript
let ip = '42:no-output;1000:car-tr:u-ck;SQEX49801'
// 在此处添加你的解决方案
< ['42', 'output', '1000', 'tr:u-ck', 'SQEX49801']
```

**10)** 编写一个字符串函数，将给定输入交替变换大小。第一个字母应变为小写，下一个变为大写，以此类推。非字母字符应保持不变不受影响大小转换。

```javascript
function aLtErNaSe(ip) {
  // 在此处添加你的解决方案
}

> aLtErNaSe('HI THERE!')
< 'hI tRe!'

> aLtErNaSe('good morning')
< 'gOoD mNiNg'

> aLtErNaSe('Sample123string42with777')
< 'sAmPlE23s'
```

**11)** 替换所有的`par`、`spare`和`park`。

```javascript
let s1 = 'apartment has a park'
let s2 = 'do you have a spare'
let s3 = 'write a parser'
let d1 = 
// 在此处添加你的解决方案
const pat6 = 
// 在此处添加你的解决方案

> s1.replace(pat6, k => d1[k])
< 'aspartment a garden'

> s2.replace(pat6, k => d1[k])
< 'do you have a cable'

> s3.replace(pat6, k => d1[k])
< 'write aser'
```

**12)** 命名标记并使用`match()`获取匹配部分的起始和结束位置。

**Character class**

本章将讨论如何创建自己的占位符来匹配字符集。你还将学习预定义集合的转义序列。

**Custom sets**

在`[]`内的标记是字符类（或集合）。这与在分组内部使用分支类似，但速度更快且没有额外副作用。此外，字符类有它们自己的标记版本并提供了常用用例。量词也适用于字符类。

```javascript
// 等同于 /cut/ 或 /c(o|u)/
> ['cute', 'cat', 'cost'].filter(w => /ou/.test(w))
< ['cute', 'coat']
```

**Range of characters**

字符类拥有用于简洁定义集合的标记。然而，在字符类外部如`^`、`$`没有特殊含义，但在字符类内部有完全不同的含义。首先，标记有助于定义字符范围，而不是逐个指定它们。

```javascript
// 所有数字
> 'Sample123string42with777'.match([0-9]+/)
< ['123', '42', '777']

// 仅小写字母和数字组成的单词
> 'coat food tar12 best'.match([a-z0-9]+\b)
< ['coat', 'food', 'tar12', 'best']

// 从 'p' 到 'z' 且包含小写字母的单词
> 'coat food put stoop best42'.match(\b[p-z][a-z]+\b)
< ['put', 'stoop']
```

**Negating character sets**

下一个标记`^`必须作为第一个字符类指定。它否定字符集，因此指定的字符以外的字符将被匹配。如前面提到的，小心处理否定逻辑，可能会匹配到比想要的多的。

```javascript
// 所有非数字
> 'Sample123string42with777'.match([^0-9]+/)
< ['Sample', 'string', 'with']

// 移除前两个以冒号分隔的
> 'apple:123:banana:cherry'.replace(/^([^:]+:){2}/, '')
< 'banana:cherry'

// 根据分隔符删除结尾
> 'apple=42;cherry=123'.replace(/==]+$/, '')
< 'apple=42;cherry'
```

有时，使用正字符类并否定条件比使用否定字符类更容易。

```javascript
let words = ['tryst', 'fun', 'glyph', 'ity', 'why']

// 不包含元音字符的元素
> words.filter(w => /^[^aeiou]+$/.test(w))
< ['fun', 'why']

// 更编写和维护，注意 '!' 运算符的使用
// 但也会匹配空字符串
> words.filter(w => !/[aeiou]/.test(w))
< ['tryst', 'glyph', 'why']
```

**Matching metacharacters literally**

你可以在标记前加上前缀`\`以字面匹配它们。其中一些也可以通过不同的位置实现。应该是第一个或最后一个字符或使用`\`。

```javascript
> 'ab-cd gh-c 423'.match(\b[a-z-]{2,}\b/g)
< ['ab-cd', 'gh-c']

> 'ab-cd gh-c 423'.match(\b[a-z\-0-9]{2,}\b/g)
< ['ab-cd', 'gh-c', '423']
```

`^`应该是不是第一个字符或使用`\`。

```javascript
> 'f*(a^b) - 3*(a+b)'.match(/a[+^]b/g)
< ['a^b', 'a+b']

> 'f*(a^b) - 3*(a+b)'.match(/a[\^+\]b/g)
< ['a^b', 'a+b']
```



[不需要转义，但如果你愿意可以对其转义.] 应该使用 \` 转义。

> `'words[5] = tea'.match([a-z\[\]0-9]+/)[0]`

< `'words[5]`

\ 应该使用 \` 转义。

> `console.log('5ba\\abc2'.match([a\\\\\]+/)[0])`

< `bab`

**Escape sequence sets**

常用的字符集有预定义的转义序列：

- `\w` 类似于 `[A-Za-z0-9\_]`，匹配单词字符（回想边界的定义）
- `\d` 类似于 `[0-9]`，匹配数字
- `\s` 类似于 `[\t\r\n]`，匹配空格

这些转义序列可以作为独立序列在字符类内部使用。如之前提到的，示例假设仅由 ASCII 字符组成。使用 `\W` 和 `\S` 分它们的否定集。

**Numeric ranges**

字符类也可以用于构建数字范围。然而，很容易漏掉边界情况，某些范围的设计非常复杂。

```
// 10 到 29 数字
> '23 154 12 26 98234'.match(\b[12]\d\b/g)
< ['23', '12', '26']

// >= 100 数字
> '23 154 12 26 98234'.match(\b\d{3,}\b/g)
< ['154', '98234']

// 如果有前导零，>= 100
> '0501 035 154 12 26 98234'.match(\b0\*[1-9]\d{2,}\b/g)
< ['0501', '154', '98234']

// 数字小于 350
> '45 349 651 593 4 204'.match(/\d+/g).filter(n => n < 350)
< ['45', '349', '4', '204']

> '45 349 651 593 4 204'.replace(/\d+/g, m => m < 350 ? 0 : 1)
< '0 0 1 1 0 0'

// 数字在 200 到 650 之间
> '45 349 651 593 4 204'.match(/\d+/g).filter(n => n >= 200 && n <= 650)
< ['349', '593', '204']
```

![](img/1a4ef11dadb051ae1522899ffab370e1_56_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_56_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_56_2.png)![](img/1a4ef11dadb051ae1522899ffab370e1_56_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_56_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_56_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_56_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_56_7.png)

查看正则表达式：匹配数字范围以获取更多示例。

**速查表与总结**

| 备注 | 描述 |
| :--- | :--- |
| `[ae;o]` | 一次匹配这些字符中的任意一个；量符也适用于字符类 |
| `[3-7]` | 从 3 到 7 的字符范围 |
| `[^=b2]` | 否定集，匹配除 `=`、`b` 或 `2` 以外的字符 |
| `[a-z\-]` | `\-` 应该是开头/结尾，或者使用 `\\` 转义以进行字面匹配 |
| `[+^\\]` | `^` 不应该是第一个字符，或者使用 `\\` 转义 |
| `[\\]]` | `\]` 应该使用 `\\` 转义 |
| `\[` | 无需转义，但也可以使用 `\\\[` |
| `\w` | 类似于 `[A-Za-z0-9\_]`，用于匹配单词字符 |
| `\d` | 类似于 `[0-9]`，用于匹配数字字符 |
| `\s` | 类似于 `[ \t\n\r\f\v]`，用于匹配空白字符；分别使用 `\W`、`\D`、`\S` 匹配它们的反向 |

本章重点介绍了如何为有限字符集创建自定义占位符。

分组和字符类可以被视为两个层级的抽象。一方面，你可以在 `[]` 内部包含字符集；另一方面，你可以在 `()` 内部对多个变形进行分组，包括字符类。由于锚点和量符可以应用于这两种抽象，你可以开始理解为什么正则表达式被视为一种微型编程语言。在接下来的章节中，你甚至会看到如何在某些场景下实现类似于否定字符类的否定分组。

**练习题**

**1)** 对于数组 `items`，过滤出所有以 `hand` 开头并以 `s`、`y` 或 `le` 结尾的元素。中间不能有其他字符，例如，`hands` 应该匹配，但 `hand-has` 不应该。

```
let items = ['-handy', 'hand', 'handy', 'unhand', 'hands', 'hand-icy', 'handle'] 

// 在此处添加你的解决方案
< ['handy', 'hands', 'handle']
```

**2)** 将所有的单词 `reed` 或 `read` 或 `red` 替换为 `X`。

```
let ip = 'redo red credible :read: rod reed bred'

// 在此处添加你的解决方案
< 'redo X credible :X: rod X bred'
```

**3)** 对于数组 `words`，过滤出所有包含 `e` 或 `i` 且后随 `l` 或 `n` 的元素。注意应该遵循提到的顺序。

```
let words = ['surrender', 'unicorn', 'newer', 'door', 'empty', 'eel', 'pest']

// 在此处添加你的解决方案
< ['surrender', 'unicorn', 'eel']
```

**4)** 对于数组 `words`，过滤出所有以任意顺序包含 `e` 或 `i` 以及 `l` 或 `n` 的元素。

```
let words = ['surrender', 'unicorn', 'newer', 'door', 'empty', 'eel', 'pest']

// 在此处添加你的解决方案
< ['surrender', 'unicorn', 'newer', 'eel']
```

**5)** 提取所有的十六进制字符序列，可选前缀 `0x`。不区分大小写字符，且序列不应被其他单词字符包围。

```
let str1 = '128A foo 0xfe32'
let str2 = '0xDEADBEE 0ff1ce'

const hex_seq =

// 在此处添加你的解决方案
> str1.match(hex_seq)
< ['128A', '0xfe32']

> str2.match(hex_seq)
< ['0xDEADBEE', '0ff1ce']
```

**6)** 从 `(` 开始到下一个 `)`，除非它们之间包含括号字符。

```
let str1 = 'def()'
let str2 = 'a/b(c)d' 
let str3 = 'Hi there(a)'

const parentheses =

// 在此处添加你的解决方案
> str1.replace(parentheses, '')
< 'def'

> str2.replace(parentheses, '')
< 'a/bd'

> str3.replace(parentheses, '')
< 'Hi there(a)s'
```

**7)** 对于数组 `words`，过滤出所有以 `e` 或 `p` 开头的元素。

```
let words = ['surrender', 'unicorn', 'newer', 'door', 'empty', 'eel', 'pest']

// 在此处添加你的解决方案
< ['empty', 'pest']
```

**8)** 对于数组 `words`，过滤出所有包含 `u` 或 `w` 或 `ee` 或 `\-` 的元素。

```
let words = ['p-', 'you', 'tea', 'heel', 'owe', 'reed', 'ear']

// 在此处添加你的解决方案
< ['tea']
```

**9)** 给定字符串以 和 分隔且可能为空。替换最后三个字段。

```
let row1 = '(2),kite,D,'
let row2 = 'hi,bye'

const pat1 =

// 在此处添加你的解决方案
// row1 的结果
< '(2),kite,D,'

// row2 的结果
< 'hi,bye'
```

**10)** 根据连续的数字或空白字符分割给定字符串。

```
let str1 = 'liononion'
let str2 = 'star'

const pat2 =

// 在此处添加你的解决方案
> str1.split(pat2)
< ['lion', 'onion']

> str2.split(pat2)
< ['star']
```

**11)** 删除所有非空字符的出现。

```
let ip = 'a,b,characters'
let words = 'apple,banana'

// 在此处添加你的解决方案
< 'a,b,characters'
```

**12)** 分组与反引用

本章将展示如何通过反引用重用匹配的部分。你已经知道如何通过 `match()` 和 `matchAll()` 方法引用捕获组。更直接，你可以将捕获的部分传递给 `replace()` 方法。此外，你可以在替换定义中使用反引用。

```
< ['on', 'moon']
```

**13)** 对于给定数组，过滤出包含大于 24 数字的元素。

```
let words = ['00044', '625', '1496']

// 在此处添加你的解决方案
< ['00044', '625']
```

**14)** 将给定输入字符串转换为下面的形式。

```
let ip = 'price_42 roast'

// 在此处添加你的解决方案
< 'price_0_42 roast'
```

**15)** 将 `\_\_` 替换为 `\_` 且如果它是单独的则删除它。

```
let items = ['\_apple\_ \_\_123\_\_ _banana\_']

// 在此处添加你的解决方案
< 'apple \_123\_ banana'
```

**16)** 对于给定字符串，为所有单词加上 `{}`。

```
let ip = 'part; rest_42'

// 在此处添加你的解决方案
< '{part}; {rest}'
```

```
// 包含至少一个连续重复字符的元素
let words = ['moon', 'mono', 'excellent', 'POLL', 'a22b']
words.filter(w => /(\w)\1/.test(w))
< ['moon', 'excellent', 'POLL', 'a22b']

// 移除任何由空格分隔的连续重复单词
// 注意在反向引用上使用量词
// 使用 \W+ 代替空格以覆盖 'a;a<-;a' 等情况
> 'aa a a a 42 f\_1 f\_1 f\_13.14'.replace(/\b(\w+)( \1)+\b/g, '$1')
< 'aa a 42 f\_1 f\_13.14'
```

## 反向引用的特殊之处

由于 `$` 在替换部分是特殊字符，如果 `$` 后面跟着数字，那么要字面量表示它会产生问题。通常使用转义字符来实现此类目的，但在这里你需要使用 `\$\$`。

```
// 没有使用捕获组，因此 '$1' 将被字面插入
> 'cat'.replace(/a/, '{$1}')
< 'c{$1}t'

// 使用了捕获组，'\$1' 在此处等于 '$1'
> 'cat'.replace(/(a)/, '{\$1}')
< 'c{a}t'

// 使用 '$$' 来字面量插入 '$'
> 'cat'.replace(/(a)/, '{$$1}')
< 'c{$1}t'
```

另一个问题是，当普通数字紧跟在反向引用之后时如何避免歧义？这取决于模式中存在多少个反向引用，以及你是否需要在正则定义或替换部分避免歧义。例如，如果组数少于 10 个，那么类似 `$12` 将引用第一个捕获组并将 `2` 作为一个字符。如果没有捕获组，那么类似 `$5` 将被字面量插入为 `$` 和 `5`。

```
// 这里的 $15 将反向引用第 1 组，并使用 5 作为字符
> '\[52\] apples and \[31\] mangoes'.replace(/\[(\d+)\]/g, '($15)')
< '(525) apples and (315) mangoes'

// 因为只有一个捕获组，$3 将被字面量插入
> '\[52\] apples and \[31\] mangoes'.replace(/\[(\d+)\]/g, '$3')
< '$3 apples and $3 mangoes'

// 因为没有捕获组，$1 将被字面量插入
> '\[52\] apples and \[31\] mangoes'.replace(/\[\d+\]/g, '$1')
< '$1 apples and $1 mangoes'
```

另一方面，如果你有多于 9 组但少于 100 组的，那么如果你想引用一个单数字组并后跟字面量数字字符，就会出现问题。解决方法是在数字前加上前缀 0，使得 `$` 之后的数字位数等于最高捕获组所需的数字位数。因此，如果你有多于 9 组但少于 100 组的，`$05` 将引用第 5 个捕获组，其后的任何数字都将被视为字面量。

```
// 出于说明目的，这里定义了 12 个捕获组
// 如果你想引用 2 位数组，则没有问题
> 'abcdefghijklmn'.replace(/(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)/, '$11')
< 'kmn'

// 如果你想引用第 1 组并后跟字符 '1' 该怎么办？
// 使用 \x31 不起作用，因为它仍然会产生 $11
> 'abcdefghijklmn'.replace(/(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)/, '$1\x31')
< 'kmn'

// 加上前缀 '0' 以使 '$01' 变成引用'1' 变成字符
> 'abcdefghijklmn'.replace(/(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)/, '$011')
< 'a1mn'
```

正则定义中的解决方法更简单。0 前缀技巧无效，但使用带有 `\xhh` 的 ASCII 码是有效的。例如，`\1\x31` 将引用第一个捕获组，后跟作为字符的 1。

```
> 'abcdefghijklmna1d'.replace(/(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.)(.).).*\1\x31/, 'X')
< 'Xd'
```

## 非捕获组

分组有许多用途，例如在正则部分应用量词、通过提取公用部分来创建简洁的正则等。它还会影响 `split()` 方法的行为，正如在带捕获组的 `split()` 部分所示。与其它语言中的类似方法不同，带有 `g` 标志的 `match()` 方法不受捕获组的影响，并返回整个匹配部分。

```
// 不带捕获组的 split 方法
> 'Sample123string42with777numbers'.split(/\d+/)
< ['Sample', 'string', 'with', 'numbers']

// 带有捕获组的 split 方法
> 'Sample123string42with777numbers'.split(/(\d+)/)
< ['Sample', '123', 'string', '42', 'with', '777', 'numbers']

// 带有 'g' 标志和捕获组的 match 方法示例
> 'effort flee facade oddball rat tool'.match(/\b\w^*(\w)\1\w*\b/g)
< ['effort', 'flee', 'oddball', 'tool']

// 这里是另一个例子
> 'hi 123123123 bye 456123456'.match(/(123)+/g)
< ['123123123', '123']
```

当不需要反向引用时，你可以使用非捕获组来避免 `split()` 方法的行为变化。当特定组不需要反向引用时，它也有助于避免跟踪捕获组编号。语法是 `(?:pat)` 来定义非捕获组，其中 `pat` 是正则表达式模式中一部分的缩写。更多以 `(?` 开头的特殊组将在以后讨论。

```
// 这里需要分组来提取公用部分并应用量词
// 但使用捕获组不会产生预期输出
> '123hand42handy777ful500'.split(/hand(y|ful)?/)
< ['123', undefined, '42', 'y', '777', 'ful']

// 非捕获组救了急
> '123hand42handy777ful500'.split(/hand(?:y|ful)?/)
< ['123', '42', '777', '500']

// 使用普通分组，需要跟踪所有的组
> '1,2,3,4,5,6,7'.replace(/^(([^,]+))/, '$1')
```

```
let ip = 'sequoia subtle exhibit asset sets2 tests si_te'

// 在此处添加你的解决方案
< 'sequoia [subtle] exhibit [sets2] tests [si_te]'
```

**3)** 将所有开头和结尾为相同单词字符的完整单词替换为 `X`（不区分大小写）。单字符单词也应该被替换为 `X`，因为它符合述述条件。



**1)** 将给定的 `markdown` 标题转换为相应的`锚点`（anchor）标签。考虑输入以一个或多个 `#` 字符开头，后面跟着空格和单词字符。属性通过将标题转换为小写并将空格替换为连字符来构建。你可以在不使用捕获组的情况下实现它吗？

```
let header1 = '# Regular Expressions'
let header2 = '## Named capture groups'
```

```
function hyphenify(m) {
  // 在此处添加你的解决方案
}
```

```
> header1.replace()
// 在此处添加你的解决方案
< "# <a name='regular-expressions'></a>Regular Expressions"

> header2.replace()
// 在此处添加你的解决方案
< "## <a name='named-capture-groups'></a>Named capture groups"
```

**2)** 将给定的 `markdown` 锚点转换为相应的`超链接`。

```
let anchor1 = "# <a name='regular-expressions'></a>Regular Expressions"
let anchor2 = "## <a name='subexpression-calls'></a>Subexpression calls"
```

```
const hyperlink =
// 在此处添加你的解决方案
```

```
> anchor1.replace()
// 在此处添加你的解决方案
< '\[Regular Expressions\](#regular-expressions)'

> anchor2.replace()
// 在此处添加你的解决方案
< '\[Subexpression calls\](#subexpression-calls)'
```

**3)** 检查给定输入字符串是否包含至少两个连续重复字母的单词（不区分大小写）。例如，像 `stillness` 和 `Committee` 这样的单词应该返回 `true`，但像 `root`、`readable` 或 `rotational` 这样的单词应该返回 `false`。根据正则表达式术语定义单词。

```
let s1 = 'readable COMMItTEe'
let s2 = 'rotational sti1lness _foot_'
let s3 = 'needed repeated'
let s4 = 'offsh00t'
```

```
const pat1 =
// 在此处添加你的解决方案
```

```
> pat1.test(s1)
true
> pat1.test(s2)
false
> pat1.test(s3)
false
> pat1.test(s4)
true
```

**4)** 对于给定的输入字符串，将所有出现的数字序列替换为唯一的非重复序列。例如，`232323` 应该更改为 `23`，`897897` 应该更改为 `897`。如果没有重复（例如 `1234`）或重复提前结束（例如 `12121`），则不更改。

```
let ip = '1234 2323 453545354535 9339 11 60260260'
// 在此处添加你的解决方案
< '1234 23 4535 9339 1 60260260'
```

**5)** 将由 `:` 或 `.` 分隔的单词序列替换为序列中的第一个单词。当 `:` 或 `.` 后面没有跟随单词字符时，这些序列结束。

```
let ip = 'wow:Good:2_two.five: hi-2 bye kite.777:water.'
// 在此处添加你的解决方案
< 'wow hi-2 bye kite'
```

**6)** 将由 `:` 或 `.` 分隔的单词序列替换为序列中的最后一个单词。当 `:` 或 `.` 后面没有跟随单词字符时，这些序列结束。

```
let ip = 'wow:Good:2_two.five: hi-2 bye kite.777:water.'
// 在此处添加你的解决方案
< 'five hi-2 bye water'
```

**7)** 根据一个或多个重复的 `cat` 序列分割给定输入字符串。

```
let ip = 'firecatlioncatcatcatbearcatcatparrot'
// 在此处添加你的解决方案
< ['fire', 'lion', 'bear', 'parrot']
```

**8)** 对于给定的输入字符串，找到所有具有至少一个重复序列的数字序列。例如，`232323` 和 `897897`。如果重复提前结束（例如 `12121`），则不应匹配。

```
let ip = '1234 2323 453545354535 9339 11 60260260'
const pat2 =
// 在此处添加你的解决方案

// 输出中的整个序列
< ['2323', '453545354535', '11']

// 仅在输出中的唯一序列
< ['23', '4535', '1']
```

**9)** 将逗号分隔的字符串转换为对应的键值对，如下所示。输入字符串中三个字段的键分别是 `name`, `maths` 和 `phy`。

```
let row1 = 'rohan,75,89'
let row2 = 'rose,88,92'
const result =
// 在此处添加你的解决方案
```

**10)** 对于给定输入字符串，找到所有具有至少一个重复序列的单词序列。

```
let ip = 'aabbcc ddeeff'
const pat4 =
// 在此处添加你的解决方案
```

**11)** 替换所有断言言。

```
// 最后的 _ 同样被替换，并在断言中起了作用
> 'cats _cater 42cat_cats'.replace(/(?<!\_)cat./g, 'dog')
< 'dog _cater 42dogcats'
```

断言环（Lookarounds）可以与现有的锚点和其他特性结合，以定义真正强大的限制条件：

```
// 仅当单词前面没有不是 : 或 -- 时，替换整个单词
> ':cart apple --rest ;tea'.replace(/(?<!:|\--)\\b\\w+/g, 'X')
< ':cart X --rest ;X'

// 在单词边界添加空格，但不在字符串的开头或结尾
// 类似于：replace(/\b/g, ' ').trim()
> 'output=num1+35\*42/num2'.replace(/(?<!^)\\b(?!$)/g, ' ')
< 'output = num1 + 35 \* 42 / num2'
```

在目前为止的所有示例中，前瞻断言组都作为后缀，而后瞻断言作为前缀。这是它们最常用的使用方式，但并不是唯一的使用方式。断言环可以放在任何地方，并且多个断言环可以任何顺序组合。它们不会消耗字符，也不会在匹配部分中起作用。它们只是让你知道从输入字符串的当前位置来看，你想测试的条件是否满足。

```
// 这两个是等效的
// 只要字符前面不是 'p' 或 'r'，就替换字符
> 'spare'.replace(/(?<!\[pr\])./g, '\*')
< '\*\*a\*e'

> 'spare'.replace(/.(?<!\[pr\].)/g, '\*')
< '\*\*a\*e'

// 只要输入中后面没有出现 's'，就替换 'par'
// 这假设断言环不会与搜索模式冲突
// 即 's' 不会与 'par' 冲突，但如果是 'r' 和 'par' 则会有影响
> 'par spare part party'.replace(/par(?!.\*s)/g, '\[$&\]')
< 'par s\[par\]e \[par\]t \[par\]ty'

> 'par spare part party'.replace(/(?!.\*s)par/g, '\[$&\]')
< 'par s\[par\]e \[par\]t \[par\]ty'

// 由于这里使用的三个断言都是零宽度的，
// 6 种可能的组合都是等效的
> 'output=num1+35\*42/num2'.replace(/(?!$)\\b(?<!^)/g, ' ')
< 'output = num1 + 35 \* 42 / num2'
```

![](img/1a4ef11dadb051ae1522899ffab370e1_70_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_2.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_7.png)

如果不支持后瞻断言，请参考此 `stackoverflow` 问答的解决方案。

**正向断言环**

与负向断言环不同，某些内容的缺失不会满足正向断言环。相反，为了满足条件，模式必须匹配实际字符/零宽断言。可以通过下所示语法来识别正向断言环：

- `(?=pat)` 用于前瞻断言
- `(?<=pat)` 用于后瞻断言

```
// 仅当数字后面跟着 , 时才提取数字
// 注意字符串结尾不符合此断言
> '42 apple-5, fig3; y-20: f12'.match(/\d+(?=,)/g)
< ['5', '83']

// 仅当数字前面是且后面是 : 时提取数字
> '42 apple-5, fig3; y-20: f12'.match(/(?<=-)\d+(?=:)/g)
< ['20']

// 等同于 match(/\b\w/)
> 'sea eat rat tea'.replace(/(?<=\b)\w*/g, '')
< 'secret'

// 只要 'part' 在后面作为整整个单词出现，就替换 'par'
> 'par spare part party'.replace(/par(?=\bpart)/g, '\[$&\]')
< 'par s\[par\]e party'
```

断言环对于简单的字段处理非常有用，第一个和最后一个字段除外

```
> '1,two,3,four,5'.match(/(?<=,)\d+/(g)
< ['two', 'four']

// 将空字段替换为 NA
// 注意：在这种情况下，后瞻和前瞻是不可能的
> '1,two,3,four,5'.match(/(?<=,)\d+/(g)
< ['two', 'four']

// 将空字段替换为 NA
// 注意：在这种情况下，后瞻和前瞻的顺序并不重要
> ',1,two,3'.replace(/(?<=^)(=$)/g, 'NA')
< 'NA,two,3'

// 与负向断言环相同
> ',1,two,3'.replace(/(?!^)(?<!^)/g, 'NA')
< 'NA,two,3'

// 在非空字段末尾匹配空字符串
> ',cat,tiger'.replace(/,g, '}')
< '{},tiger'

// 使用断言环进行补救
> ',cat,tiger'.replace(/(?<=^*)(g, '}')
< '{},tiger'
```

**正向断言环中的捕获组**

虽然断言环不是匹配的一部分，但可以在正向断言环中使用捕获组。你能推理出为什么负向断言环不起作用吗？

```
> console.log('a b c e'.replace(/(\S+)(?=(\S+))/, '$1$2\n'))
< a b
b c
d e
```

**使用断言环实现 AND 条件**

如前所述，这里有一些示例显示了断言环如何使 AND 条件变得简单。

```
let words = ['sequia', 'subtle', 'questionable', 'exhibit', 'equation']

// 以任意顺序包含 'b' 'e' 和 't'
// 等同于 /b.*e.*t|e.*t.*e|t.*b|
> words.filter(w => /(filter.*b)(?=.*e)(?=.*t).test(w))
< ['subtle', 'questionable', 'exhibit']

// 以任意顺序包含所有元音
> words.filter(w => /(?=.*a)(?=.*e)(?=.*i)(?=.*o)/u.test(w))
< ['questionable', 'equation']

// 包含 ('ab' 或 'at') 以及 'q' 但末尾不是 'n'
> words.filter(w => /(?!.*n$)(?=.*a[bt]).q/.test(w))
< ['questionable']
```

**可变长度后瞻**

在某些正则引擎实现中，如果模式可以匹配不同数量的字符，后瞻将不起作用。例如，`(?<=fig\d+)` 是查找 `fig` 后面的一个或多个数字字符。JavaScript 没有这种限制。这里是一些示例：

```
// 正向后瞻断言示例
> '=314not :,2irk ,3cool =42,error'.match(/(?<=[=]\d+)[a-z]+/g)
< ['not', 'cool']

// 只替换第三次出现的 'cat'
> 'cat cater scat'.replace(/(?<=(cat.*?){2})cat/, 'X')
< 'cat cater Xer scat'

// 负向后瞻示例
// 只有 'cat' 不在 'dog' 之前时匹配
> /(?<!cat)dog/
< ['dog']
```

**反向组**

你已经看到了一些反向类很有用的情况。在本章中，我们还要查看反向组。反向组是一种在模式*不*匹配时匹配的断言。当你想要寻找某个字符或序列缺失的字符串时，这特别有用。

例如，如果你想找到所有后面不是 `apple` 的单词，你可以使用负向前瞻：

```
(?!apple)
> 'banana apple cherry date'.match(/\w+(?!apple)/g)
< ['banana', 'cherry', 'date']
```

同样，如果你想找到前面不是 `orange` 的单词，你可以使用负向后瞻：

```
(?<!orange)
> 'orange banana apple cherry'.match(/(?<!orange)\w+/g)
< ['banana']
```

**查询表和总结**

在本章中，你学习了：

- 什么是断言环（前瞻和后瞻）
- 如何使用多个断言环
- 如何使用反向断言环
- 如何在断言环内部捕获组
- 可变长度后瞻

断言环是你正则工具箱中强大的工具。我们希望你找到在自己的正则表达式中有效使用它们的方法。

**练习**

![](img/1a4ef11dadb051ae1522899ffab370e1_70_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_2.png)![](img/1a4ef11dadb051ae1522299ffab370e1_70_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_70_7.png)

即使不是强制的，也请使用断言环来解决以下练习题。

**1)** 替换所有单词，除非前面是 `(` 字符。

```
> let ip = '(apple) guava berry) apple (mango) (grape'
// 在此处添加解决方案
< '(apple) X X) X (mango) (grape'
```

**2)** 替换所有单词，除非后面是 `)` 字符。

```
> let ip = '(apple) guava berry) apple (mango) (grape'
// 在此处添加解决方案
< '(apple) X berry) X (mango) (X'
```

**3)** 将所有完整单词替换为 `X`，除非其前面紧跟 `(` 或后面紧跟 `)`。

```
> let ip = '(apple) guava berry) apple (mango) (grape'
// 在此处添加你的解决方案
< '(apple) X berry) X (mango) (grape'
```

**4)** 提取所有不以 `e` 或 `n` 结尾的完整单词。

```
> let ip = 'a_t row on Urn e note Dust n end a2-e|u'
// 在此处添加你的解决方案
< ['a_t', 'row', 'Dust', 'end', 'a2', 'u']
```

**5)** 提取所有不以 `a`、`d` 或 `n` 开头的完整单词。

```
> let ip = 'a_t row on Urn e note Dust n end a2-e|u'
// 在此处添加你的解决方案
< ['row', 'on', 'Urn', 'e', 'Dust', 'end', 'e', 'u']
```

**6)** 仅当完整单词后面紧跟 `:`、`,` 或 `-` 时，提取它们。



> **let** `ip = 'Poke,on=-=so_good:ink.to/is(vast)ever2-sit'`

// 在此处添加你的解决方案

< `['Poke', 'so_good', 'ever2']`

**7)** 仅当完整单词前面紧跟 `=`、`/` 或 `-` 时，提取它们。

> **let** `ip = 'Poke,on=-=so_good:ink.to/is(vast)ever2-sit'`

// 在此处添加你的解决方案

< `['so_good', 'is', 'sit']`

**8)** 仅当完整单词前面紧跟 `=` 或 `:` 且后面紧跟 `:` 或 `.` 时，提取它们。

> **let** `ip = 'Poke,on=-=so_good:ink.to/is(vast)ever2-sit'`

// 在此处添加你的解决方案

< `['so_good', 'ink']`

**9)** 仅当完整单词前面紧跟 `=`、`:`、`.`、`(` 或 `-` 且后面不是 `.` 或 `/` 时，提取它们。

> **let** `ip = 'Poke,on=-=so_good:ink.to/is(vast)ever2-sit'`

// 在此处添加你的解决方案

< `['so_good', 'vast', 'sit']`

**10)** 删除所有以 `,` 为分隔符的字段开头和结尾的空格。

> **let** `csv1 = ' comma,separated ,values \t\r '`

> **let** `csv2 = 'good bad,nice ice, 42 , , stall small'`

> **const** `trim_whitespace =`

// 在此处添加你的解决方案

> `csv1.replace(trim_whitespace, '')`

< `'comma,separated,values'`

> `csv2.replace(trim_whitespace, '')`

< `'good bad,nice ice,42,,stall small'`

**11)** 过滤满足所有规则的元素：

- 应该至少包含两个字母

- 应该至少包含三个数字

- 在 `%`、`*`、`#` 或 `$` 之间至少包含有一个特殊字符

- 不应该以空白字符结尾

> **let** `pwds = ['hunter2', 'F2h3u%9', '*X3Yz3.14\t', 'r2_d2_42', 'A $B C1234']`

// 在此处添加你的解决方案

< `['F2h3u%9', 'A $B C1234']`

**12)** 对于给定的字符串，用 `{}` 包裹所有完整单词，但 `par`、`cat` 和 `apple` 除外。

> **let** `ip = 'part; cat {super} rest_42 par scatter apple spar'`

// 在此处添加你的解决方案

< `'{part}; cat {{super}} {rest_42} par {scatter} apple {spar}'`

**13)** 提取给定字符串中浮点数的整数部分。以 `.` 结尾的数字也应考虑。

> **let** `ip = '12 ab32.4 go 46.42'`

// 在此处添加你的解决方案

< `['32', '46']`

**14)** 对于给定的输入字符串，提取所有重叠的字符序列。

> **let** `s1 = 'apple'`

> **let** `s2 = '1.2-3:4'`

> **const** `pat1 =`

// 在此处添加你的解决方案

// 为 `s1` 添加解决方案

< `['ap', 'pp', 'le']`

// 为 `s2` 添加解决方案

< `['.2', '-3', ':4']`

**15)** 给定的输入字符串由 `:` 分隔。如果在最后一个字段之前有数字，则删除最后一个字段。

> **let** `s1 = '42:cat'`

> **let** `s2 = 'twelve:a2b'`

> **let** `s3 = 'we:be:he:0:a:b'`

> **let** `s4 = 'apple:banana-42:cherry:'`

> **let** `s5 = 'dragon:centaur'`

> **const** `pat2 =`

// 在此处添加你的解决方案

> `s1.replace(pat2, '')`

< `'42'`

> `s2.replace(pat2, '')`

< `'twelve:ab'`

> `s3.replace(pat2, '')`

< `'we:be:he:0:a:b'`

> `s4.replace(pat2, '')`

< `'apple:banana-42'`

> `s5.replace(pat2, '')`

< `'dragon:centaur'`

**16)** 提取所有完整单词，除非其前面紧跟 `:`、`<=>` 或 `#`。

> **let** `ip = '::very--at<=>in.a_b#2c=>east'`

// 在此处添加你的解决方案

< `['at', 'in', 'a_b', 'lion']`

**17)** 如果包含 `qty` 紧跟 `price` 但两者之间没有任何空白字符，则匹配字符串。

> **let** `str1 = '23,qty,price,42'`

> **let** `str2 = 'qty price,oh'`

> **let** `str3 = '.14,qty,price,3'`

> **let** `str4 = '42\nqty-6,apple-234,error'`

> **let** `str5 = '4,price,3.14,qty,4'`

> **let** `str6 = '(qtyprice) (hi-)'`

> **const** `neg =`

// 在此处添加你的解决方案

> `neg.test(str1)`

< `true`

> `neg.test(str2)`

< `false`

> `neg.test(str3)`

< `false`

> `neg.test(str4)`

< `true`

> `neg.test(str5)`

< `false`

> `neg.test(str6)`

< `true`

**18)** 你能推导出为什么以下正则表达式的行为不同吗？

> **let** `ip = 'I have 12, he has 2!'`

> `ip.replace(/\b..\b/g, '{$}')`

< `'{I }have {12}{ }{he} has{2}!'`

> `ip.replace(/(?<!\w)..(?!\w)/g, '{$}')`

< `'I have {12}, {he} has {2!}'`

**19)** 模拟字符串分区：分隔符前的字符串、被分隔符的部分和分隔符后的字符串。对于第一种，根据第一次出现的数字分割字符串。对于第二种，根据最后一次出现的数字分割。

> **let** `w2 = 'Sample123string42with777numbers'`

// 为根据第一次出现分割添加解决方案

< `['Sample', '123', 'string42with777numbers']`

// 为根据最后一次出现分割添加解决方案

< `['Sample123string42with', '777', 'numbers']`

**20)** 对于给定的输入字符串，使用 `search()` 方法找到 `is` 或 `was` 或 `to` 最后一次出现的起始索引。假设每个输入字符串至少有一个匹配。

> **let** `s1 = 'match after the last newline character'`

> **let** `s2 = 'and then you want to test'`

> **let** `s3 = 'this is good bye then'`

> **let** `s4 = 'who was there to see?'`

> **const** `pat3 =`

// 在此处添加你的解决方案

> `s1.search(pat3)`

< `12`

> `s2.search(pat3)`

< `18`

> `s3.search(pat3)`

< `17`

> `s4.search(pat3)`

< `14`

## Unicode

到目前为止，书中所有的示例都是针对仅由 ASCII 字符组成的字符串。几年前这对于大多数用例已经足够了。如今，很少遇到只需要 ASCII 的项目。本章将简要讨论 Unicode 匹配。

### Unicode 字符集和 `u` 标记

与转义序列字符集类似，`\p{}` 构造提供了各种预定义的集合来处理 Unicode。对于否定集合，使用 `\P{}`。你还需要设置 `u` 标记。

```javascript
// 提取所有连续的字母
// \p{L} 是 \p{Letter} 的别名
'fox:αλεπού,eagle:αετός'.match(/\p{L}+/gu)
// ['fox', 'αλεπού', 'eagle', 'αετός']

// 提取所有连续的希腊字母
// \p{sc} 是 \p{Script} 的别名
'fox:αλεπού,eagle:αετός'.match(/\p{sc}+/gu)
// ['αλεπού', 'αετός']

// 删除除字母以外的所有字符
'φοο12,βτ_4,fig'.replace(/\P{L}+/gu, '')
// 'φοοβτfig'
```

在字符类内部，`v` 标志开启了以下集合操作：

- `&&` 交集
- `--` 差集

为了辅助此类定义，你可以以嵌套方式使用 `[]`。更多信息请参阅 MDN：v-mode character class。以下是一些示例：

```javascript
// 移除除 . ! 和 ? 之外的所有标点字符
let para = '"Hi", there! How *are* you? All fine here.';
para.replace(/[\p{P}--[.!?]]+/gv, '')
// 'Hi there! How are you? All fine here.'

// 匹配非元音的小写字母
// 也可以使用：/\b[a-z]--[aeiou]+\b/gv
'tryst glyph pity why'.match(/\b[a-z]&&[^aeiou]+\b/gv)
// ['tryst', 'glyph', 'why']
```

### 编码点 (Codepoints)

你还可以在 `{}` 结构中使用代码点（字符的数值值）来指定 Unicode 字符。这类似于使用 `\xhh` 用两个十六进制数字指定 ASCII 字符的方法。

```javascript
// 获取十六进制格式的代码点
Array.from('fox:αλεπού', c => c.codePointAt().toString(16))
// ['66', '6f', '78', '3a', '3b1', '3bb', '3b5', '3c0', '3bf', '3cd']

// 使用代码点表示字符
'{3b1}'
// 'α'

// 使用 {} 指定小写字母范围
// 注意，{} 仅在开启了 'u' 或 'v' 标志时才有效
'fox:αλεπού,eagle:αετός'.match(/[\{61}-\{7a}\]+/gu)
// ['fox', 'eagle']
```

![](img/1a4ef11dadb051ae1522899ffab370e1_79_0.png)![](img/1a4ef11dadb051ae1522899ffab370e1_79_1.png)![](img/1a4ef11dadb051ae1522899ffab370e1_79_2.png)![](img/1a4ef11dadb051ae1522899ffab370e1_79_3.png)![](img/1a4ef11dadb051ae1522899ffab370e1_79_4.png)![](img/1a4ef11dadb051ae1522899ffab370e1_79_5.png)![](img/1a4ef11dadb051ae1522899ffab370e1_79_6.png)![](img/1a4ef11dadb051ae1522899ffab370e1_79_7.png)

另请参阅 stackoverflow：Unicode string to hex。

### 速查表与总结

| 备注 | 描述 |
| :--- | :--- |
| `u` flag | 开启 Unicode 匹配的标志 |
| `v` flag | `u` flag 的超集，启用额外的功能 |
| `\p{}` | Unicode 字符集 |
| `\P{}` | 取反的 Unicode 字符集 |
| 见 MDN | 更多 Unicode 字符类转义的详情 |
| `{}` | 使用代码点指定 Unicode 字符 |

关于配合 Unicode 字符使用正则表达式的全面讨论超本书的范围。建议参考 `regular-expressions: unicode` 和 `Programmers introduction to Unicode` 等资源进行进一步学习。

### 练习

**1)** 检查给输入字符串是否仅由 ASCII 字符组成。假设输入为非空字符串，任何不属于 7 位 ASCII 集合的字符都应返回 `false`。

```javascript
let str1 = '123 × 456';
let str2 = 'good fοοd';
let str3 = 'happy learning!';
const pat1 = // 在此处添加你的解决方案
pat1.test(str1) // false
pat1.test(str2) // false
pat1.test(str3) // true
```

**2)** 为给定字符串仅保留标点字符。

```javascript
let ip = '❨a❩❪1❫❬b❭❮2❯❰c❱❲3❳❴xyz❵⟅123⟆⟦⟧⟨like⟩⟪3.14⟫';
// 在此处添加你的解决方案
// '❨❩❪❫❬❭❮❯❰❱❲❳❴❵⟅⟆⟦⟧⟨⟩⟪.⟫'
```

**3)** 以下代码片段显示的输出正确吗？

```javascript
'fox:αλεπού'.match(/\w+/g)
// ['fox']
```

**4)** 写出 `v` 标志开启的集合操作。

**5)** 从给定字符串中提取所有单词。但是，如果单词包含 `ignore` 变量中存在的任何字符，则不匹配。

```javascript
let s1 = 'match after the last new_line character A2';
let s2 = 'and then you want to test';
let ignore = 'aty';
const ign1 = // 在此处添加你的解决方案
s1.match(ign1) // ['new_line', 'A2']
s2.match(ign1) // null

let ignore = 'esw'; // 应使用与上面相同的解决方案
const ign2 = // 在此处添加你的解决方案
s1.match(ign2) // ['match', 'A2']
s2.match(ign2) // ['and', 'you', 'to']
```

### 扩展阅读

注意，这些资源中的某些并非针对 JavaScript 的，因此你需要将它们适配 JavaScript 的语法。

- MDN: Regular Expressions — 文档与示例
- stackoverflow: JavaScript regexp
- XRegExp — 具有元字符转义、递归匹配等功能的工具
- JSVerbalExpressions — 使用自然语言术语构建正则表达式
- CommonRegexJS — 常用正则表达式集合
- Awesome Regex — 库、工具、框架和软件的精选集
- randexp.js — 生成匹配给定正则表达式的字符串
- stackoverflow: regex FAQ
- stackoverflow: regex tag 是练习题的良好来源
- rexegg — 教程、技巧等
- regular-expressions — 教程与工具
- regex101 和 regexr — 表达式的视觉辅助和在线测试工具，使用前选择 flavor 为 JavaScript
- regulex 和 debuggex — 将正则表达式可视化为地铁路线图
- regexcrossword — 教程与谜题
- swtch — 关于正则表达式实现引擎的内容
- news.ycombinator: 正则表达式相关资源集

以下是针对特定主题的链接：

- rexegg: best regex trick (最佳正则技巧)
- regular-expressions: matching numeric ranges (匹配数字范围)
- regular-expressions: Zero-Length Matches (零长度匹配)
- stackoverflow: Greedy vs Reluctant vs Possessive Quantifiers (贪婪 vs 懒惰 vs 占有)
- cloudflare: Details of the Cloudflare outage on July 2, 2019 — 详见附录

关于 CPU exhaustion（由于正则表达式回溯导致的 CPU 耗尽）

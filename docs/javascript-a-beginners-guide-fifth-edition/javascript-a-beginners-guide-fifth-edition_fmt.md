
# JavaScript 入门指南，第五版

- 创建具有特殊特效的动态 Web 页面
- 学习最新的 JavaScript 标准
- 使用 HTML5、jQuery 和 Node.js

献给我的妻子 Heather，以及孩子们 Eva、Elizabeth、Elaine 和 Evan，Bruce 和 Joy Anderson，以及 J. D. 博士和 Linda Andrews

纪念 John 和 Betty Hopkins，James D. 和 Livian Anderson，John William 和 Edith Hopkins，Burley T. 和 Aline Price，"Doc" Flores，以及 Clifton Idom

# 关于作者

**John Pollock** 白天担任软件开发人员，晚上从事网站和其他项目的开发工作。您可以在 Twitter (@ScriptpttheWeb) 或 LinkedIn (https://www.linkedin.com/in/john-pollock-82a2b074) 上找到他。John 拥有萨姆休斯顿州立大学英语学士学位，目前与妻子 Heather 以及孩子们 Eva、Elizabeth、Elaine 和 Evan 住在德克萨斯州的 New Waverly。

# 关于技术编辑

**Christie Sorenson** 是 ZingChart 的高级软件工程师。自1997年以来一直从事基于 JavaScript 的系统，并对该语言的演变着迷。她曾合作多本 JavaScript 和 HTML 书籍并担任技术编辑。她拥有加州大学圣迭戈分校的计算机科学学士学位，现与丈夫 Luke 以及女儿 Ali 和 Keira 住在旧金山。

## 第 2 章：将 JavaScript 放置在 HTML 文件中

### 核心技能与概念

- 指定脚本的加载时机
- 使用 `<script>` 标签
- 创建你的第一个脚本
- 编写一个 "Hello World" 脚本
- 为脚本创建 HTML 文档
- 将脚本插入 HTML 文档
- 尝试练习 2-1：在 HTML 文档中插入脚本
- 使用外部 JavaScript 文件
- 创建 JavaScript 文件
- 创建 HTML 文件
- 在浏览器中查看页面
- 尝试练习 2-2：从 HTML 文档调用外部脚本
- 使用 JavaScript 注释
- 插入单行注释
- 添加多行注释

### 使用 HTML Script 标签

Script 标签用于告诉浏览器脚本语言在 HTML 文档中的开始和结束位置。在最基本的形式中，脚本标签看起来就像任何其他 HTML 标签一样：

```html
<script> 
JavaScript 代码在这里
</script> 
```

当你像这样使用基础的起始和结束标签时，几乎所有的浏览器都会假设脚本语言是 JavaScript。

在 HTML 中，`script` 标签是不区分大小写的。但在 XHTML 中，`script` 标签必须是小写。JavaScript 在所有版本中都是区分大小写的，因此你需要对它更加小心。在书中，我将使用 HTML5 编写 HTML 代码（尽管 HTML5 不区分大小写，但我会将标签和属性名写为小写）。对于 JavaScript，我将使用其正常运行所需的大小写。

`<script>` 标签有六个可能的属性：`type`、`language`（已弃用）、`charset`、`src`、`defer` 和 `async`。这些属性为浏览器提供了关于脚本何时加载、脚本语言以及外部 JavaScript 文件位置（如果有）的额外信息。

### 识别脚本语言

起始和结束脚本标签之间的脚本语言可以是 JavaScript、VBScript 或其他语言，尽管 JavaScript 几乎被设置为浏览器的默认脚本语言。如果需要，你可以通过在起始脚本标签上添加值为 `"text/javascript"` 的 `type` 属性来显式地指定 JavaScript 为脚本语言：

```html
<script type="text/javascript">
JavaScript 代码在这里
</script>
```

在 XHTML 中，起始脚本标签中的 `type` 属性是 Web 页面验证所必需的，但在 HTML 中是可选的。

过去，`language` 属性被用于识别脚本语言，但现代浏览器会忽略它，并且会导致页面在 XHTML 和 HTML5 中无效。不应使用它。

`charset` 属性允许指定 JavaScript 代码的字符集，但大多数浏览器并不识别它，因此不建议使用。

### 调用外部脚本

Script 标签允许你在文档中调用外部 JavaScript 文件。外部 JavaScript 文件是一个只包含 JavaScript 代码的文本文件，并以 `.js` 扩展名保存。通过调用外部文件，你可以节省编码或将脚本复制到每个需要它的页面的时间。相反，你可以在每个页面上使用单行代码指向包含所有代码的 JavaScript 文件。你可以通过在起始脚本标签上添加 `src`（源）属性来调用外部脚本：

```html
<script src="yourfile.js"></script>
```

此示例从你放置此代码的任何 HTML 文档调用名为 `yourfile.js` 的 JavaScript 文件。起始和结束脚本标签之间没有空格或代码，因为这会导致脚本调用失败。

如果脚本非常长，使用 `src` 属性将脚本添加到多个页面会比将整个代码插入每个页面要快得多。此外，浏览器会在第一次加载外部 JavaScript 文件时对其进行缓存，使得后续使用该脚本的 Web 页面可以直接使用渲染。在处理页面验证以及尝试将代码与标记（HTML）代码分离时，使用外部文件也有帮助。此外，`src` 属性还允许你以相同的方式将他人的脚本文件作为库引入。

默认情况下，脚本文件按照它们在 HTML 代码中放置的顺序加载（同步加载）。有一些更改此行为的选项，将在下一节中描述。

### 指定脚本加载的时机

最后两个属性 `defer` 和 `async` 允许你指定何时加载外部脚本。旧版浏览器不完全支持这些属性，或者行为可能不同，因此请注意，旧版浏览器可能在预期的执行时不执行脚本。

#### defer 属性

`defer` 属性允许你指定加载外部脚本文件，但不应在页面完成解析（即 `<html>` 标签加载完成）之前执行。以下 `<script>` 标签延迟了外部 JavaScript 代码的执行：

```html
<script src="file.js" defer></script>
```

如果你正在使用 XHTML，请使用 `defer="defer"` 设置此属性。

Internet Explorer 4+、Firefox 3.5+ 和 Chrome 7 支持此属性。Internet Explorer 4–7 允许此属性在内联脚本上工作，而版本 8 及以上版本才在外部脚本或其他浏览器上支持此属性。

#### async 属性

当设置 `async` 属性时，页面可以继续加载而无需等待脚本加载，脚本将在加载完成后执行。这里有一个示例：

```html
<script src="file.js" async></script>
```

如果你正在使用 XHTML，请使用 `async="async"` 设置此属性。

Firefox 3.5+ 和 Chrome 7 支持此属性。

### 使用 `<noscript></noscript>` 标签

为没有 JavaScript（或禁用了 JavaScript）的观众提供替代内容的一种方法是使用 `noscript` 标签。`<noscript>` 标签可以放置在 HTML 文档的任何位置，并可以包含任何供没有 JavaScript 的浏览用户查看的内容。例如：

```html
<script>
  document.write("The color is red.");
</script>
<noscript>
  颜色是红色。
</noscript>
```

此示例通过 JavaScript 或 `<noscript>` 标签向观众显示"颜色是红色"这句话。

某些旧版浏览器可能无法正确处理 `noscript` 标签，从而无法显示内容。如果你的用户使用的是旧浏览器，另一种替代方案是在页面显示内容，并为能够显示的用户使用 JavaScript 进行增强。

`<noscript>` 标签有时很有用，但通常有更好的方法在没有 JavaScript 的情况下提供相同的内容（例如避免 `document.write()` 方法）。随着学习的深入，你将了解到更多关于可访问 JavaScript 的知识。

### 专家问答

**Q:** 我总是需要使用脚本标签向页面添加 JavaScript 吗？

**A:** 可以使用*事件处理器*，允许你在 HTML 标签的事件处理属性内编写短脚本片段。你将在第 13 章学习事件处理器。

**Q:** `language` 属性呢？

**A:** `language` 属性曾用于指定要使用的脚本语言，曾经某些浏览器允许指定 JavaScript 版本（例如 `language="JavaScript.1"`）。现在不再如此，该属性已被弃用。由于现代浏览器完全忽略它，且会导致页面在 XHTML 和 HTML5 中无效，因此应不再使用。

**Q:** 当我在页面中添加脚本时，页面在 XHTML（严格或过渡）中无法通过验证。如何让页面通过验证？

**A:** 如果脚本包含 XHTML 中的字符，例如 `<`（在 JavaScript 中用于"小于"，但在 XHTML 中被视为新标签的开始），那么在不添加 CDATA 部分的情况下，页面将无法验证脚本：

```html
<script>
<![CDATA[ 开始 CDATA 
var x = 5;
var y = 10;
if (x < y) {
  window.alert("x is less than y");
}
]]><!-- 结束 CDATA
</script>
```

这将允许页面通过验证，但由于脚本中包含了 `<![CDATA[` 和 `]]>` 字符，脚本将无法工作。要修复此，当这些字符位于 `<script>` 标签内部时，需要在它们周围加上 JavaScript 注释（`/*` 和 `*/`）：

```javascript
<script>
/*<![CDATA[
var x = 5;
var y = 10;
if (x < y) {
  window.alert("x is less than y");
}
*/
</script>
```

你可以看到，这很快就会变得非常繁琐！通常，如果你在使用 XHTML，更好的选择是使用外部脚本文件，这可以消除这个问题，因为 XHTML 文档中只需要脚本标签。

### 编写 "Hello World" 脚本

对于此脚本，你将使用的不是 "Hello World"，而是另一行文本："是的！我现在是一个 JavaScript 编码员了！"。这只需要一行代码，使用 `document.write()` 方法，该方法会将字符串写入文档中：

```javascript
document.write("Yes! I am now a JavaScript coder!");
```

注意文本周围的括号和引号。使用括号是必要的，因为 `document.write()` 方法是一个 JavaScript 函数，它在括号中接收一个参数。你将在第 5 章学习更多关于 JavaScript 函数的知识。

引号表示字符串。字符串是 JavaScript 中的一种数据类型，通过将值放在引号内来定义。第 4 章提供了有关字符串和其他 JavaScript 类型的详细信息。

关于你的脚本，需要注意的最后一点是行尾的分号。分号表示一个 JavaScript 语句的结束。语句是代码的一部分，在语法上（其形式和顺序）不需要添加任何内容即可完备。一个语句可以用于执行单一任务、执行多个任务，或调用脚本的其他部分执行几条语句。大多数 JavaScript 语句以分号结束；养成添加分号的习惯是一个好主意。

在随后的章节中，你会看到不以分号结尾的行，因为它们开启或关闭了一个代码块。此外，你遇到的许多脚本可能没有以分号结束语句。JavaScript 在大多数情况下对分号的使用是宽容的；然而，最好使用分号结束语句，因为可以防止可能的错误并有助于稍后对脚本进行调试（移除错误）。

因此，要向页面写入字符串，你使用 `document.write()` 方法，后跟由引号包围并包含在括号内的文本。用分号结束该行（该语句）。JavaScript 将处理剩余的工作。

### 为脚本创建 HTML 文档

为了使此示例完整化并测试脚本，你需要将其插入到 HTML 文档中。首先，使用基本标签创建 HTML 文档（使用你任何喜欢的文本编辑器）：

```html
<!DOCTYPE html>
<html>
<head>
<title>未命文档</title>
</head>
<body>
</body>
</html>
```

在编辑器中将该文档保存为 `test.html`。你稍后将用 Web 浏览器打开它以查看脚本的结果。接下来，你把你的 JavaScript 代码添加到此 HTML 文档中，并保持文件打开。

### 将脚本插入 HTML 文档

现在你需要将脚本插入文档中。它应该放在哪里？你可以将脚本放在 `<head>` 和 `</head>` 标签之间，或者放在 `<body>` 和 `</body>` 标签之间。由于此示例直接向页面写入字符串，你将希望将脚本插入 `<body>` 和 `</body>` 标签之间，取决于你想让字符串出现在任何地方。它可以位于页面上任何 HTML 代码的之前或之后。

为了清楚脚本的结果，你将在脚本前后的文本行添加 HTML 代码。脚本标签和脚本本身被插入在代码行之间。在 `<body>` 和 `</body>` 标签旁边添加所示行：

```html
<p>这是第一行，位于脚本结果之前。</p>
<script>
document.write("Yes! I am now a JavaScript coder!");
</script>
<p>这一行位于脚本之后。</p>
```

再次保存 `test.html` 文档。你现在应该能够在 Web 浏览器中打开文档以查看脚本的结果。

恭喜你，你现在完成了你的第一个脚本！

本节中的示例代码使用了整个 HTML 文档及其所有的标签。为了保持内容尽可能相关，从现在开始，示例代码将只使用与脚本相关的 HTML 标签，而不是全部标签。项目代码可能会使用完整的 HTML 标签。

### 使用外部 JavaScript 文件

在你的文本编辑器中将此文件保存为 `jsfile1.html`。确保将其保存在与 `jsfile1.js` 相同的目录中。

第二个 HTML 文档看起来与第一个相同，只是 HTML 文本显示它是第 2 页：

```html
<body>
  <script src="jsfile1.js"></script>
  <p>
    这是第 2 页，脚本在这里也可以运行！
  </p>
</body>
```

在你的文本编辑器中将此文件保存为 `jsfile2.html`。再次，确保将它放在与其他文件相同的目录中。

### 在浏览器中查看页面

在你的 Web 浏览器中打开 `jsext1.html` 文件。页面插入了来自外部脚本的 JavaScript。

接下来，在浏览器中打开 `jsext2.html` 文件。区别是你添加到 HTML 文件中的文本，显示这是第 2 页。

JavaScript 在此页面上写入的文本与在第一个 HTML 页面上写入的相同。

虽然我们在这个示例中使用了相同的短脚本，但它应该让你了解到，当你有一个大型脚本时，使用外部文件可以节省大量时间。

### 尝试一下 2-2 从 HTML 文档调用外部脚本

```
pr2_2.html
prjs2_2.js
```

此项目将允许你练习创建外部 JavaScript 文件并使用它们将脚本插入 Web 页面。

#### 逐步步骤

1. 设置一个简单的 HTML 文档，在 `<body>` 和 `</body>` 标签之间什么都不留。
2. 在页面的 body 标签之间放置以下行文本：
3. 这段文本来自 HTML 文档！
4. 在此文本之后放置一个 `<p>` 标签。
5. 将其保存为 `pr2_2.html`。
6. 创建一个外部 JavaScript 文件，它在执行时将写入以下行：

我喜欢编写 JavaScript 并使用外部文件！

7. 你的 JavaScript 文件看起来应该是这样的：

```javascript
document.write("I love writing JavaScript, and using external files!");
```

8. 将 JavaScript 文件保存为 `prjs2_2.js`。
9. 回到 HTML 文档。在外部 JavaScript 文件将写入句子的页面文档中，在 `<p>` 标签之后放置脚本标签。
10. 在脚本标签之后插入一个 `<p>` 标签。
11. 你的 HTML 文档主体应该像这样：

```html
<body>
这段文本来自 HTML 文档！
<p>
<script src="prjs2_2.js"></script>
</p>
</body>
```

12. 保存 HTML 文件并在浏览器中查看结果。

#### 尝试一下总结

在这个项目中，你创建了一个 HTML 页面。利用你在上一节中学习的外部 JavaScript 文件的知识，你创建了一个外部 JavaScript 文件，并将必要的代码放入 HTML 文件中包含该外部 JavaScript 文件。当 HTML 文件在 Web 浏览器中显示时，会显示一行文本，随后是外部 JavaScript 文件的执行结果。

### 使用 JavaScript 注释

你可能需要在你的 JavaScript 代码中做笔记，例如描述某行代码的作用。你也可能由于某些原因想要禁用脚本的某行。例如，如果你在脚本中寻找错误，你可能想要禁用脚本的某一行，看看是否该行导致了错误。你可以使用 JavaScript 注释来完成这些任务。你可以插入单行或多行注释。

#### 插入单行注释

如果你想对代码中的单行添加注释，请在注释文本之前放置一对正斜杠：

```
// 在此处输入你的注释
```

在此格式下，该行中双斜杠之前的任何内容都是"活动"代码——即会被执行的代码——而该行中斜杠之后的任何内容都会被忽略。例如，假设你在代码中写了这一行：

```javascript
document.write("This is cool!"); // 写出我的观点
```

浏览器将运行 `document.write()` 方法，因此文本 "This is cool!" 将写入页面。然而，斜杠后的注释将被 JavaScript 解释器忽略。

#### 添加多行注释

多行注释使用 `/*` 开始，`*/` 结束：

```javascript
/* 这是多行注释
可以跨越多行 */
```

### 第 2 章自测

1. 你必须知道以下哪一项在 Web 浏览器中使用 JavaScript 是必须的？
   - A. Perl
   - B. C++
   - C. HTML
   - D. 

2. 在 Web 浏览器中使用 JavaScript 必须使用以下哪一项？
   - A. 浏览器
   - B. 编译器
   - C. 硬盘
   - D. RW

3. JavaScript 的错误处理取决于。
   - A. Flash
   - B. VBScript
   - C. JavaScript
   - D. Windows

4. JavaScript 和 Java 是同一种语言。
   - A. 正确
   - B. 错误

5. 以下哪一项是该语言的国际标准名称和规范？
   - A. JavaScript
   - B. LiveScript
   - C. ECMAScript
   - D. ActionScript

6. JavaScript 与其他语言有相似之处。
   - A. 正确
   - B. 错误

7. 在发布作为 JavaScript 之前，它被称为。
   - A. Java
   - B. JavaCup
   - C. LiveScript
   - D. EasyScript

8. JavaScript 是。
   - A. 基于原型的
   - B. 基于类的
   - C. 缺少对象的
   - D. 不是使用对象的语言

9. 需要高级代码编辑器来编辑 JavaScript 文件。
   - A. 正确
   - B. 错误

10. 高级代码编辑器可以通过方式帮助 JavaScript 程序员？
    - A. 它可能提供电影和游戏的功能。
    - B. 它可能提供代码高亮、补全、调试工具等功能。
    - C. 它可能提供电子维修和保修的功能。
    - D. 它完全没有帮助。

11. 解释型语言在运行之前不需要对程序进行编译。
    - A. 编程
    - B. 服务器端
    - C. 解释型
    - D. 

12. JavaScript 只能在 Web 浏览器环境中使用。
    - A. 正确
    - B. 错误

13. 在 JavaScript 中，什么处理脚本错误？
    - A. 操作系统
    - B. 编译器
    - C. Web 服务器上的程序
    - D. 客户端

14. JavaScript 是如何添加到 Web 页面的？
    - A. 不是。它必须单独编译并加载。
    - B. 它是从服务器上的编译程序中取的。
    - C. 你将代码单独放在文件中并打开该文件。
    - D. 它被添加到 HTML 文档中。

15. Web 页面添加什么来插入 JavaScript 代码？
    - A. `<script>` 和 `</script>` HTML 标签
    - B. JavaScript 代码单词
    - C. `<javascript>` 和 `</javascript>` HTML 标签
    - D. `<java>` 和 `</java>` HTML 标签

## 第 3 章：使用变量

### 核心技能与概念

- 理解变量
- 为什么变量很有用
- 为你的脚本定义变量
- 理解变量类型
- 在脚本中使用变量

现在你已经学习了在网页中添加 JavaScript 的基础知识，是时候深入研究该语言的内部机制了。由于变量是 JavaScript 编码的重要组成部分，你将尽可能地了解它们是什么以及它们为什么在你的脚本中很有用。一旦你理解了变量是如何工作的以及它们能做什么，你就可以继续学习其他基于不同类型变量使用的主题。

在本章中，你将从学习变量是什么以及它们为什么有用开始。然后，你将学习用于声明变量的方法以及如何给变量赋值。最后，你将看到如何在脚本中使用变量。

### 理解变量

变量代表或持有一个值。变量的实际值可以随时更改。为了理解变量，请考虑一个你在代数课上可能见过的基础语句：

```
x=2
```

字母 `x` 被用作变量名。它被赋值为 2。要更改该值，你只需给 `x` 分配一个新的值：

```
x=4
```

变量名称保持不变，但现在它代表一个不同的值。

将数学课的例子再推深一步，你可能需要解决过类似这样的问题：

```
如果 x=2，那么 3+x=?
```

为了得到答案，你将值 2 替换掉问题中的变量 `x`，得到 `3+2=5`。如果 `x` 的值改变，问题的答案也会随之改变。所以，如果 `x=7`，计算就变成了 `3+7`，现在的结果是 10。

JavaScript 中的变量与数学中使用的变量非常相似。你给变量命名，并根据你的需求给它赋值。如果变量的值发生变化，它将改变脚本内部发生的事情。

### 为什么变量很有用

使用变量有几个优点：

- 它们可以用于代码编写时还不知道其所代表的值的地方。
- 它们可以节省你编写和更新脚本的时间。
- 它们可以使你的代码意图更加清晰。

#### 变量作为未知值的占位符

通常，变量会在内存中为脚本编写时未知的值留出一个位置。变量的值可能会根据访问者遇到的某些情况而改变，或者由你稍后在脚本中更改。

例如，你可能有一个函数，根据用户输入接收某些值（函数将在第 4 章中讨论）。由于用户输入的值在脚本编写时是未知的，可以使用变量来存储用户输入的值。这对于任何类型的用户输入都是如此，无论它是以 JavaScript prompt 的形式存在。

#### 变量作为节省时间的工具

变量可以节省你编写和更新脚本的时间。如果你在脚本中多次使用同一个值，你可以将其存储在变量中，然后只需更改变量的值即可更新所有使用该值的地方。

#### 变量作为代码的解释器

由于变量代表某些内容，而且你可以给它们起有意义的名字，因此在阅读（调试）你的脚本时，它们通常更容易识别。如果你只是添加数字，你可能会忘记它们代表什么。例如，考虑这行代码：

```
TotalPrice = 2.42 + 4.33;
```

在这里，数字可以代表任何内容。相反，你可能会将 2.42 赋值给名为 `CandyPrice` 的变量，将 4.33 赋值给名为 `OilPrice` 的变量：

```
TotalPrice = CandyPrice + OilPrice;
```

现在，与其尝试记住数字的含义，你可以看到脚本正在将糖的价格与油的价格相加。这在调试非常有用，因为有意义的变量名更容易发现错误。

### 为你的脚本定义变量

现在你已经理解了变量是什么以及你为什么要使用它们，你需要学习如何在脚本中使用它们。你通过声明变量来创建变量。然后使用赋值运算符对其进行赋值。当你为变量命名时，需要遵循 JavaScript 的变量命名规则，并考虑命名的意义。

#### 声明变量

要将文本声明为变量，你使用 `var` 关键字，它告诉浏览器后续文本将是新变量的：

```
var variablename;
```

例如，将你的变量命名为 `coolcar`，声明如下：

```
var coolcar;
```

在这个例子中，你有一个名为 `coolcar` 的新变量。分号结束语句。变量 `coolcar` 还没有被赋值（JavaScript 会给它赋值为 `undefined`）。

声明多个变量，一种方法是每次都使用 `var` 语句：

```
var coolcar;
var cooltruck;
var coolvan;
```

或者，你可以使用单个 `var` 语句并逗号分隔每个变量名，最后一个以分号结尾（以结束 `var` 语句）：

```
var coolcar, cooltruck, coolvan;
```

如果你使用这种格式，也可以在单行内声明所有变量：

```
var coolcar, cooltruck, coolvan;
```

由于所有这些变量都在同一个 `var` 语句中，这不会引起任何问题。在查看 JavaScript 代码时，你可能会经常看到这种格式。

正如下一节所描述，你可以在声明变量的同时给它们赋值，也可以在脚本的稍后部分给它们赋值。

#### 给变量赋值

要给变量赋值，你需要使用 JavaScript 的赋值运算符，即等号 (`=`) 符号。如果你想在同一行内声明变量并给它赋值，请使用这种格式：

```
var variablename = variablevalue;
```

例如，要为你的变量命名并给它赋予数值 1200，请使用此语句：

```
var paycheck = 1200;
```

该语句以关键字 `var` 开始，后面跟着变量 `paycheck`，就像上一节中的普通变量描述一样。接下来是赋值运算符 (`=`)，它告诉浏览器将运算符右侧的值分配给运算符左侧的变量。赋值运算符右侧是 1200，这是被分配给变量 `paycheck` 的数值。该行以分号结尾，表示语句的结束。

注意不要将赋值运算符 (`=`) 认为具有"等于"的意思。表示"等于"的运算符是两个等号连在一起 (`==`)，正如你将在第 5 章学到的那样。

要声明并分配另一个变量，请使用相同的格式。为了设置一个名为 `spending` 的变量来跟踪你从 `paycheck` 变量中花费的金额，请使用这些语句：

```
var paycheck = 1200;
var spending = 1500;
```

你之前使用的通过 `var` 语句声明多个变量的方法也适用于声明并为多个变量赋值。使用逗号来分隔每个变量赋值，如下代码所示：

```
var paycheck = 1200,
bonus = 50,
spending = 1500;
```

再次记住，最后一个声明并已赋值的变量将以分号结尾，以完成变量语句。

赋值给变量的值也可以是计算结果，如下代码所示：

```
var net = 1500 - 1200;
```

在这种情况下，结果是 300，并将被分配给变量 `net`。

你看到的示例说明了变量声明和赋值的正确且安全的方法。然而，JavaScript 在变量方面允许一定程度的灵活。在很多情况下，即使不使用精确的语法代码也能运行。例如，你可能会看到在第一次使用变量时没有写 `var` 关键字编写的脚本。即使变量之前未声明，JavaScript 通常也会在第一次使用它时声明它。这里显示了一个示例：

```
paycheck = 1200;
```

这是行得通的，因为变量正在赋值（JavaScript 将简单地声明该变量并为其分配值 1200）。但是，如果你尝试在不赋值的情况下声明变量，以下情况是不行的：

```
paycheck;
```

这种声明仍然需要 `var` 关键字才能有效，如下代码所示：

```
var paycheck;
```

你还可能会看到省略了结尾分号的脚本：

```
var paycheck = 1200
```

在某些脚本中，变量赋值中都省略了这两个特性：

```
paycheck = 1200
```

所有这些快捷方式可能很有用，但最好在你在使用每个变量之前先定义它，使用 `var` 关键字并包含分号。这样做可能会在某些浏览器中导致错误，并给人们留下代码写得好的印象。此外，如果你需要调试脚本，任何遗漏都可能非常麻烦。

例如，如果你在声明变量时漏掉了 `var`，变量将被自动放在全局作用域中，这在以后很容易导致问题。你将在第 4 章看到更多关于作用域如何影响变量值的。

提供正确的声明和赋值将避免问题，你的代码将易于阅读和理解。

#### 变量命名

在开始编写变量之前，你需要了解 JavaScript 的命名规则。在选择名称时需要考虑的因素有大小写敏感、无效字符以及 JavaScript 保留的名称。此外，你应该尝试给你的变量起一个既容易记忆又有意义的名字。

##### 在变量中使用大小写

JavaScript 变量对大小写敏感——`paycheck`、`PAYCHECK`、`Paycheck` 和 `PaYcheck` 是四个不同的变量。当你创建一个变量时，你需要确保在稍后编写该变量时使用相同的名称。如果你更改了大小写，JavaScript 将其视为一个不同的变量。

##### 允许的字符

一个重要的规则是，变量名必须以字母、下划线 (`_`) 或美元符号 (`$`) 开始。名称不能以数字或任何非字母字符开头。变量名的其他字符可以是字母、数字和美元符号。变量名中不允许空格。因此，以下变量名是有效的：

- `paycheck`
- `_paycheck`

然而，以下变量名是无效的：

- `#paycheck`
- `1paycheck`
- `pay check`

##### 避免关键字和保留字

命名变量的另一个要记住的规则是避免使用关键字和保留字。关键字是用于特定用途的特殊单词。例如，你已经学过 `var` 用于声明 JavaScript 变量。作为变量名可能会在脚本中引起许多问题，因为这个词是为了在以后作为关键字使用的，所以它们不应该用作变量名，以防止你的代码出现潜在问题。

表 3-1 列出了 JavaScript 中的关键字和保留字。注意所有这些单词都是小写字母。在后面的章节中，你将使用许多关键字，它们会变得更加熟悉。

##### 给变量赋予意义的名字

尽管 `x` 是一个可以接受的变量名，但在需要调试程序时可能会忘记它代表什么。此外，如果其他人尝试调试你的代码，你的工作将更加困难。

你应该尝试给你的变量起尽可能描述它们所代表的名字。假设你想使用一个变量来存储数字，而不是使用 `x` 或 `ex` 这样的短变量，使用更具描述性的名称：

```
var examplumber = 2;
```

变量 `examplumber` 将方便你以后识别，其他程序员也可能更容易理解它。

| abstract | default | for | new | throw |
| arguments | delete | function | null | throws |
| await | do | goto | package | transient |
| boolean | double | | private | true |
| break | else | implements | protected | try |
| byte | enum | import | public | typeof |
| case | eval | in | return | var |
| catch | export | instanceof | short | void |
| char | extends | int | static | volatile |
| class | false | interface | super | while |
| const | final | let | switch | with |
| continue | finally | long | synchronized | yield |
| debugger | float | | native | this |

表 3-1 JavaScript 关键字和保留字

### 理解数据类型

到目前为止，你已经看到了一些数字型变量值的示例。在 JavaScript 中，变量可以是几种数据类型之一，包括数字、字符串、布尔、null、undefined、symbol 和对象。

与更严格的编程语言不同，JavaScript 不会在你定义变量时强制你声明变量的类型。相反，JavaScript 允许几乎任何变量被赋值为任何值。它还允许你在更改值时更改数据类型。这在编码时为你提供了灵活性，但你必须小心，因为可能会导致意想不到的结果——特别是在数字相加时（关于此主题，请参见第 5 章）。

#### 数字 (Number)

数字就是数字。JavaScript 不要求将数字声明为整数、浮点数（小数）或任何其他类型。相反，任何数字都被视为另一个数字，无论它是 7、-2、3.453 还是其他任何。除非你进行类型更改，否则数字将保持相同的类型。例如，如果你在变量中使用整数，除非你执行了某种计算来改变它（例如进行不均匀除法），否则它不会突然出现小数。

正如你所见到的，你使用 `var` 关键字来定义数字变量：

```
var varname = number;
```

以下是一些示例：

```
var paycheck = 1200;
var phonebill = 29.99;
var savings = 0;
var sparetime = -24.5;
```

如果你需要使用一个特别长的数字，JavaScript 拥有指数计数法。要表示指数，在基数数字之后、指数之前使用字母 `e`。要创建一个名为 `number` 的变量并赋值为 4.52 × 10⁵ (452,000)，请在数字和指数之间的所有内容替换为字母 `e`（表示"乘以 10 的几次方"）：

```
var bignumber = 4.52e5;
```

JavaScript 可能会使用指数计数法返回计算结果（类似于许多计算器）。

#### 字符串 (String)

值包含一段文本字符串。字符串可以包含字母、单词、空格、数字、符号或你喜欢的几乎任何内容。字符串的定义方式与数字略不同，使用以下格式：

```
var varname = "stringtext";
```

以下是字符串变量的示例：

```
var mycar = "Corvette";
var oldcar = "Big Brown Station Wagon";
var mycomputer = "Pentium 3, 500 MHz, 128MB RAM";
var oldcomputer = "36 SX, 40 MHz, 8MB RAM";
var gibberish = "what? I am @ home 4 now. (cool, right)?";
```

正如你所见，字符串可以是短的、长的或两者之间的任何长度。你可以在字符串变量中放置各种文本和其他字符。然而，需要考虑引号、特殊字符以及字符串的敏感性。

##### 匹配引号

在 JavaScript 中，你通过将它们放在引号（简称为 quotes）内部来定义字符串，正如你在示例中看到的那样。JavaScript 允许你使用双引号或单引号。问题在于，如果字符串用双引号开启，则它必须用双引号结束：

```
var mycar = "Red Corvette";
```

单引号也是如此：

```
var myhouse = 'small bridge house';
```

尝试用不匹配类型的引号来结束字符串，或者漏掉起始引号或结束引号，都会导致问题。

```javascript
var mycar = 'Red Corvette'; // 错误，字符串用双引号开启并用单引号结束
myhouse = 'small bridge house"; // 错误，字符串用单引号开启并用双引号结束
var mycomputer = "Pentium 3, 500 MHz, 128MB RAM; // 错误，字符串没有结束引号
```

这些错误将在 Web 浏览器中导致 "Unterminated String"（未终止的字符串）错误。

如果你使用双引号包裹字符串，你可以在字符串内部使用单引号，反之亦然。

##### 注意大小写

字符串是大小写敏感的。这看起来可能并不重要，但在匹配字符串时很重要。

##### 使用特殊字符

特殊字符允许你在字符串中添加一些在其他情况下无法实现的内容。

引号，强制让它们视为文本字符串的一部分，而不是 JavaScript 语句的一部分：

```javascript
<script type="text/javascript">
document.write("John said, \"JavaScript is easy.\");
</script>
```

反斜杠允许内部的引号成为字符串的一部分。

这解决了字符串的问题，句子将带有引号打印出来。

还要注意字符串内部的单引号（'）和撇号（'）。对于由单引号括起来的字符串，需要对这些符号进行转义。

转义技术也适用于需要引号的 HTML 代码。例如，如果你想在页面上放置链接，请使用 `<a>` 标签并将 URL 放在引号中。如果你对 `<a>` 标签中的引号进行转义，JavaScript 允许你在 `document.write()` 方法中将 HTML 代码写入页面，例如所示：

```javascript
<script type="text/javascript">
document.write("<a href=\"http://someplace.com\">Text</a>");
</script>
```

这可以达到效果，但如果你不想一直转义引号，还有一种更简单的方法来实现。

为了避免转义上述代码中的引号，你可以在此代码的内部 URL 地址周围使用单引号：

```javascript
<script type="text/javascript">
document.write('<a href=\'http://someplace.com\'>Text</a>');
</script>
```

如果你喜欢在外层使用单引号，也可以采用另一种方法，如例所示：

```javascript
<script type="text/javascript">
document.write("<a href=\'http://someplace.com\'>Text</a>");
</script>
```

这里需要记住的重要点是：确保你不要在字符串内部使用相同类型的引号来包裹字符串。如果你需要让引号嵌套超过一层，就需要开始对它们进行转义；这是因为如果你再次切换，例如，看这段代码：

```javascript
document.write("John said, \'Jeff says, \"Hi!\"\' to someone.\'");
document.write("John said, \'Jeff says, \"Hi!\"\' to someone.\'");
```

第一行可以工作，因为引号经过了转义以保持字符串。然而，第二行在字符串内部的单引号内只切换回了双引号。在那个位置不转义就放置双引号会导致字符串终止并产生错误。

正如你所看到的，当你需要在字符串中使用大量引号时，引号可能会是一个头疼的问题。然而，记住在需要时使用反斜杠转义引号将会在你寻找缺失的引号时省去不少麻烦。我曾多次在我的代码中寻找缺失的引号，在经历几次这种情况后，我的头都晕了！在本章稍后的部分，你将看到你可以拼接字符串，这可以为你简化引号的使用。

#### 布尔值 (Boolean)

布尔值的值为 `true`（真）或 `false`（假）。以下是示例：

```javascript
var johncodes = true;
var johniscool = false;
```

注意 `true` 和 `false` 单词不应该包含在引号中。这是因为它们是 JavaScript 识别的字面量。

布尔变量在你需要只能取 `true` 或 `false` 值的变量时非常有用，例如在事件处理器中（第 7 章将介绍）。

当我们谈论布尔变量的概念时，单词 Boolean 的第一个字母是大写的（因为它源自数学家乔治·布尔的名字）。然而，在脚本中使用关键字 `boolean` 时，它是全小写的。

#### 空 (Null)

`null` 用于第 9 章中表示对象的空状态。如果你需要定义一个值为 `null` 的对象，请使用如下声明：

```javascript
var variabele = null;
```

与布尔变量一样，你不应该像处理字符串值那样将此值包含在引号中，因为 JavaScript 识别 `null` 这个特殊值。`null` 数据类型只有一个值：`null`。

#### 未定义 (Undefined)

`undefined` 数据类型与 `null` 类似，因为它只有一个可能的值：`undefined`。这发生在变量没有被赋予初始值，或者使用了之前声明的变量时。例如，以下两个示例都使用了 `undefined` 变量（你将在本章稍后的部分学习如何使用变量）：

```javascript
var myname; // 变量名已声明，但未赋值
document.write(myname); // 因为变量没有赋值，它是 undefined，代码将不会按预期工作。
```

#### 符号 (Symbol)

符号值是一个唯一且不变的值，可以用作对象的属性。你将在第 10 章学习更多关于对象的。

#### 对象 (Object)

对象是属性的集合。对象是 JavaScript 的关键部分，将在第 10 章详细讨论。注意，在 JavaScript 中函数和数组也是对象。这与许多其他语言不同，因此你需要关注自己的学习进度。

### 专家问答

**问:** 我为什么需要学习变量？我不能直接在需要用的地方放入我想要的数字或文本吗？

**答：** 你可以这样做，但是变量让你以后在程序中更改值变得容易得多。

**问:** 我为什么需要学习变量？

**答：** 变量允许你存储可以在代码中引用和更改的数据。

**问:** 但分号不是会结束语句吗？

**答：** 分号结束的是语句，而不是变量声明本身。

**问:** 我为什么需要给文本加上引号？

**答：** 它是为了让 JavaScript 知道字符串从哪里开始，哪里结束。

**问:** 反斜杠（\）字符通常起什么作用？

**答：** 如果反斜杠后面跟着创建特殊字符的代码，则特殊字符会被渲染。否则，反斜杠后的第一个字符会被 JavaScript 原样处理，并视为其所在字符串的一部分。

### 尝试 3-1 声明变量

```
pr3_1.html
```

这个项目提供了练习变量赋值的机会。它会在页面上打印一行短文本。

#### 步骤详解

1. 创建一个 HTML 页面，留出 `<body>` 和 `</body>` 标签之间的空间。
2. 在 `<body>` 和 `</body>` 标签之间，按照第 2 章学的方法添加 `<script>` 和 `</script>` 标签。
3. 创建名为 `chipscott` 的数值变量并赋值 `2.59`。
4. 创建名为 `istrue` 的布尔变量并赋值 `false`。
5. 创建名为 `nata` 的变量并赋值 `null`。
6. 创建一个 JavaScript 语句，将以下字符串值写入 Web 页面。需要时记得转义引号。
7. 完成后，HTML 文档的主体部分看起来如下：

```html
<body>
<script type="text/javascript">
var chipscott=2.59;
var istrue=false;
var nata=null;
document.write("John said, \"This project is fun!\");
</script>
</body>
```

8. 将文件保存为 `pr3_1.html` 并在浏览器中查看。

你应该只看到通过 `document.write()` 命令输出的文本。变量定义不会打印在浏览器屏幕上。你可以查看页面源代码来观察变量定义在代码中的样子。

#### 尝试回顾此总结

在这个项目中，你能够运用所学技能在脚本中声明不同类型的变量。该项目包含了一个数值变量、一个布尔变量以及一个值为 `null` 的变量。你还可以使用第 2 章中学的技能，用 JavaScript 在页面上编写一行文本。

### 在脚本中使用变量

要让变量有用，你不能仅仅在脚本中声明它。你需要在脚本的后续通过某种方式使用它，也许是为了打印它的值，甚至只是改变它的值。要使用变量，在声明变量后对它进行调用。

#### 调用变量

以下代码展示了如何使用 `document.write()` 方法将变量的值写入页面：

```javascript
<script type="text/javascript">
var mycar="Corvette";
document.write(mycar);
</script>
```

脚本首先声明了一个变量 `mycar` 并赋予它字符串 "Corvette" 的值。然后，在 `document.write()` 命令中，你会看到变量名被括在括号内。该脚本的结果仅仅是向浏览器写入 "Corvette"。

在写入页面的变量周围没有引号。这是因为 `mycar` 变量已经被赋予了一个字符串值，所以在使用 `document.write()` 命令将其值打印到页面时，不需要加引号。你已经可以看到，使用变量的优点是让简短的 `document.write()` 命令更易编写。

#### 在文本字符串中添加变量

之前的代码只是在浏览器中打印变量的值。如果你想在字符串中将其与其它文本一起打印，`document.write()` 命令就会变得更加复杂。如果文本没有被定义为变量，则需要加引号，而变量则需要独立存在。你使用加法运算符 `(+)` 将变量的值添加到字符串中，如下例所示：

```javascript
<script type="text/javascript">
var mycar="Corvette";
document.write("I like driving my " + mycar);
</script>
```

这段代码会在浏览器窗口中打印以下句子：

I like driving my Corvette.

注意代码中 "my" 单词后的空格。这确保了在将变量添加到字符串之前会显示一个空格。如果你使用以下代码：

```javascript
document.write("I like driving my" + mycar);
```

结果将是：

I like driving myCorvette.

在合并字符串时，你需要小心添加你希望在输出中显示的空格。

加法运算符允许你将变量放在字符串的之前、之后、甚至中间。要将变量插入到字符串中间（使其在两边都有文本显示），只需使用另一个运算符在变量右侧添加任何你需要的内容，在本例中：

```javascript
<script type="text/javascript">
var mycar="Corvette";
document.write("I like driving my " + mycar + " every day!");
</script>
```

现在变量位于两个文本字符串内部，由三个部分组合成一个单一字符串。这段代码向浏览器打印以下句子：

I like driving my Corvette every day!

你在此处执行的添加字符串的过程被称为字符串拼接（string concatenation）。

#### 使用变量进行字符串拼接

使用变量时，你需要确保变量和加法运算符不在字符串的引号内部。如果它们内部，你将无法得到预期的结果。看这段代码：

```javascript
<script type="text/javascript">
var mycar = "Corvette";
document.write("I like driving my " + mycar + " every day!");
</script>
```

JavaScript 在此处不会识别运算符和变量；它们仅被视为文本字符串的一部分，因为它们在引号内。JavaScript 不会使用该变量，而是字面意思地读取所有内容并在浏览器中打印出：

I like driving my + mycar + every day!

为了让这段代码更易编写，你可以将涉及的每个字符串都放入变量中，这样你只需要将值相加，而无需处理引号，如下：

```javascript
<script type="text/javascript">
var firststring = "I like driving my ";
var mycar = "Corvette";
var secondstring = " every day!";
document.write(firststring + mycar + secondstring);
</script>
```

这会打印相同的句子，但允许你稍后更改它的部分，而无需编辑 `document.write()` 命令。

#### 模板字符串量 (Template Literals)

模板字符串量为你提供了一种更简单的方法来处理字符串拼接。与其使用加法运算符拆分字符串或为简单的拼接分配多个值，你可以使用特殊的占位符将值插入到字符串中。

模板字符串量被包含在反引号（`` ` ``）中，而不是单引号或双引号，如下代码所示：

```javascript
document.write(`I like driving my Corvette`);
```

在这里反引号并没有什么特别之处。这里没有使用单引号或双引号。注意模板字符串量如何允许你使用占位符。以下代码展示了这一点：

```javascript
<script type="text/javascript">
var mycar="Corvette";
document.write(`I like driving my ${mycar} every day!`);
</script>
```

你可以看到，模板字符串量为编写拼接提供了更简单的方法，并使代码更具可读性！

这将输出以下行：

I like driving my Corvette when it is sunny and the traffic is light!

如果你好奇，不使用模板字符串量实现相同结果的代码在此：

```javascript
<script type="text/javascript">
var mycar = "Corvette";
var weather = "sunny";
var traffic = "light";
document.write("I like driving my " + mycar + " when it is " + weather + " and the traffic is " + traffic + "!");
</script>
```

需要说明的是，你的变量值可以使用任何类型的字符串（引号或模板字符串量），你的 `document.write` 将得到相同的结果。例如，以下代码产生与上述相同的结果：

```javascript
<script type="text/javascript">
var mycar = "Corvette";
var weather = "sunny";
var traffic = "light";
document.write(`I like driving my ${mycar} when it is ${weather} and the traffic is ${traffic}!`);
</script>
```

模板字符串量是在 ES2015 规范中引入的。如果你使用的是建议的浏览器，这应该运行良好。如果你需要为旧版浏览器编写代码，可能需要坚持使用拼接。

模板字符串量还允许字符串跨多行，并由第二个反引号关闭。而单引号和双引号内的字符串只能包含单行代码而不会报错，模板字符串量可以跨越任意数量。记得添加关闭的反引号！示例如下：

```javascript
var message = `这是一个非常长的公告，可能很难在单行内适应并保持可读。由于这是模板字符串量的一部分，
它可以跨越很多行才关闭。`;
```

还需要提到的一点是，模板字符串（template literals）允许你自由地使用任何类型的引号而不产生问题。因此，你可以编写以下代码：

```javascript
document.write(`She said, "I'm having fun!"`);
```

通过使用模板字符串，你可以自由地使用引号，而无需像在引号字符串值那样处理所有的转义字符或仔细考虑放置位置！浏览器将打印出以下结果：

She said, "I'm having fun!"

你在本节中学到的技巧会在你的字符串变得复杂时变得非常有用，特别是当你在字符串中使用 HTML 代码时。

`const` 和 `let` 关键字是在 ES6 中引入的，它们是声明变量的最新标准。为了更好地理解它们与 `var` 关键字相比对比工作原理，它们将在第 4 章中介绍，因为函数和作用域是理解这些关键字如何使用的关键部分。

### 编写一个 JavaScript 页面

现在你已经知道如何使用变量以及使用 JavaScript 将基础 HTML 代码写入页面了，现在你将创建一个几乎完全由 JavaScript 编写的页面（`<body>` 和 `</body>` 标签内部的所有内容），并强化你到目前为止所学的技巧。

#### 创建框架

你首先需要一个页面的基础框架，以便你知道如何插入脚本。由于你正在页面上写入信息，`<script>` 标签将放置在 `<body>` 和 `</body>` 标签之间。在这种情况下，将使用一个名为 `ch3_code.js` 的外部文件。你的 HTML 文档的 `body` 部分看起来如下：

```html
<body>
<script type="text/javascript" src="ch3_code.js"></script>
</body>
```

在此处插入 `<script>` 标签是为了调用外部 JavaScript 文件。

你在 `ch3_code.js` 文件中放置的代码将决定当你完成后浏览器中显示的内容。

#### 定义变量

要开始你的脚本文件，请使用一些 JavaScript 代码编写一个 HTML 标题。你将直接代码作为字符串写入 `document.write()` 命令中，如下所示：

```javascript
document.write("<h1>A Page of JavaScript</h1>");
```

另一方面，你可以将字符串放在变量中，并在脚本后半部分的 `document.write()` 命令中使用该变量：

```javascript
var headingtext = "<h1>A Page of JavaScript</h1>";
// 其他代码可以放在这里...
document.write(headingtext);
```

对于此示例，你将使用第二种方法，因为它使用了变量。你将通过使用 `headingvariable` 看到这是一个非常方便的功能，你将创建一组变量来存储 HTML 代码字符串并将其添加到页面中。下一个将为页面添加一个简短的介绍语句。介绍部分的变量声明如下：

```javascript
var myintro = "Hello, welcome to my JavaScript page";
```

接下来，你将为页面添加一个链接。链接的变量声明如下：

```javascript
var linktag = "<a href=\"http://scripttheweb.com\">Link to a Site</a>";
```

接下来，你将输入红色来添加一点颜色。`redtext` 变量定义为：

```javascript
var redtext="<span style=\"color:red\">I am so colorful today!</span>";
```

最后，你将添加一些仅包含强标签和段落标签的变量：

```javascript
var begineffect = "<strong>";
var endeffect = "</strong>";
var beginpara = "<p>";
var endpara = "</p>";
```

`ch3_code.js` 文件中所有变量的代码如下：

```javascript
var headingtext = "<h1>A Page of JavaScript</h1>";
var myintro = "Hello, welcome to my JavaScript page";
var linktag = "<a href=\"http://scripttheweb.com\">Link to a Site</a>";
var redtext = "<span style=\"color:red\">I am so colorful today!</span>";
var begineffect = "<strong>";
var endeffect = "</strong>";
var beginpara = "<p>";
var endpara = "</p>";
```

#### 添加命令

现在，在 `ch3_code.js` 文件中添加一些 `document.write()` 命令，将变量的内容写回 HTML 文档：

```javascript
document.write(headingtext);
document.write(begineffect + myintro + endeffect);
document.write(beginpara + linktag + endpara);
document.write(beginpara + redtext + endpara);
```

这在页面顶部写入了标题。在 `myintro` 左右添加 `begineffect` 和 `endeffect` 变量会将介绍性文本以粗体写在标题下方。之后是一个带有链接的新段落，然后是另一个带有文本消息的新段落。

以下是用于复制的 `ch3_code.js` 文件代码：

```javascript
var headingtext = "<h1>A Page of JavaScript</h1>";
var myintro = "Hello, welcome to my JavaScript page!";
var linktag = "<a href=\"http://scripttheweb.com\">Link to a Site</a>";
var redtext = "<span style=\"color:red\">I am so colorful today!</span>";
var begineffect = "<strong>";
var endeffect = "</strong>";
var beginpara = "<p>";
var endpara = "</p>";
document.write(headingtext);
document.write(begineffect + myintro + endeffect);
document.write(beginpara + linktag + endpara);
document.write(beginpara + redtext + endpara);
```

保存 `ch3_code.js` 文件并加载你的 HTML 文档。

#### 修改页面

现在假设你不喜欢布局。相反，你希望 `<strong>` 部分被强调。

现在，由于你使用了变量，你需要更改页面顶部的。以下代码显示了你可以做的更改：

```javascript
var headingtext = "<h1>A Page of JavaScript</h1>";
var myintro = "Hello, welcome to my JavaScript page";
var linktag = "<a href=\"http://scripttheweb.com\">Link to a Site</a>";
var redtext = "<span style=\"color:red\">I am so colorful today!</span>";
var begineffect = "<em>";
var endeffect = "</em>";
var beginpara = "<p>";
var endpara = "</p>";
document.write(headingtext);
document.write(begineffect + myintro + endeffect);
document.write(beginpara + linktag + endpara);
document.write(beginpara + redtext + endpara);
```

### 尝试 3-2 使用 JavaScript 创建 HTML 页面

在这个项目中，你将创建一个 HTML 页面，类似于你在本章中创建的。变量将被赋予新值，差异将是明显的。

```
prjs3_2.html
prjs3_2.js
```

#### 步骤

1. 创建一个 HTML 页面，留出 `<body>` 和 `</body>` 标签之间的空间。
2. 在 `<body>` 和 `</body>` 标签之间添加 `<script>` 和 `</script>` 标签以链接到名为 `prjs3_2.js` 的文件。将 HTML 文件保存为 `prjs3_2.html`。
3. 打开文件以使用你的 JavaScript 文件。将其保存为 `prjs3_2.js`。使用此文件添加步骤4-10中的 JavaScript 代码。
4. 创建名为 `heading` 的变量并赋值为：`This is My Web Page!`
5. 创建名为 `linktag` 的变量并赋值为：`<a href="http://www.webxpertz.net/">Web Site Link!</a>`
6. 创建名为 `sometext` 的变量并赋值为：`This text can be affected by other statements.`
7. 创建名为 `begineffect` 的变量并赋值为：`<em>`。
8. 创建名为 `endeffect` 的变量并赋值为：`</em>`。
9. 创建名为 `beginpara` 的变量并赋值为：`<p>`。
10. 创建名为 `endpara` 的变量并赋值为：`</p>`。
11. 将所有的变量定义放入单个 `var` 语句中，这样你就不需要重复 `var` 关键字（记得在最后一个加分号）。
12. 按照此顺序将每个变量的值写回 HTML 文档：`heading`, `begineffect`, `sometext`, `endeffect`, `beginpara`, `linktag`, `endpara`, `beginpara`, `sometext`, `endpara`。

完成后，请保存 `prjs3_2.js` 文件。它应该看起来如下：

```javascript
var heading = "This is My Web Page!",
linktag = "<a href=\"http://www.webxpertz.net/\">Web Site Link!</a>",
sometext = "This text can be affected by other statements.",
begineffect = "<em>",
endeffect = "</em>",
beginpara = "<p>",
endpara = "</p>";
document.write(heading);
document.write(begineffect + sometext + endeffect);
document.write(beginpara + linktag + endpara);
document.write(beginpara + sometext + endpara);
```

13. 在浏览器中打开 `prjs3_2.html` 页面并查看结果。
14. 重新打开 `prjs3_2.js` 文件并查看 15-16 中的更改。
15. 将 `begineffect` 的值更改为 `<strong>`。
16. 将 `endeffect` 的值更改为 `</strong>`。
17. 完成后，保存 `prjs3_2.js` 文件。它应该看起来如下：

```javascript
var heading = "This is My Web Page!",
linktag = "<a href=\"http://www.webxpertz.net/\">Web Site Link!</a>",
sometext = "This text can be affected by other statements.",
begineffect = "<strong>",
endeffect = "</strong>",
beginpara = "<p>",
endpara = "</p>";
document.write(heading);
document.write(begineffect + sometext + endeffect);
document.write(beginpara + linktag + endpara);
document.write(beginpara + sometext + endpara);
```

18. 在浏览器中重新加载 `prjs3_2.html` 页面。注意 JavaScript 文件中变量值变化带来的差异。
19. 加分步骤：可以使用模板字符串字量（template literal）通过一个变量声明（针对 `sometext`）和一个 `document.write` 语句来编写此 JavaScript 文件。使用模板字符串字量重写此文件。加分答案将包含在"自测"答案中。

#### 本节总结

在这个项目中，你将使用变量的新技能与之前使用 JavaScript 编写 Web 页面的技能结合了起来。你创建了一个带有脚本的 Web 页面，脚本使用变量在页面上写入 HTML。然后你更改了两个变量的值并刷新了脚本。变量的更改使页面发生了肉眼可见的变化。

### 第 3 章自测

1. 变量 ________ 一个值。
2. 使用变量的两个优点是什么？
   - A. 它们可以节省编写和更新脚本的时间，并能让你的代码目的更清晰。
   - B. 它们让你的代码目的更清晰，并让非编码人员难以理解脚本。
   - C. 它们可以节省编写和更新脚本的时间，并让非编码人员更难理解脚本。
   - D. 它们没有任何优点。
3. 要声明变量，你使用 ________ 关键字。
4. JavaScript 中用什么符号作为赋值运算符？
   - A. +
   - B. -
   - C. :
   - D. =
5. 下列哪项声明了一个名为 `pagenumber` 的变量并赋予其值 240？
   - A. `var pageNumber = 240;`
   - B. `pagenumber = 220;`
   - C. `var pagenumber = 240;`
   - D. `int named Pagenumber = 240;`
6. 变量名不区分大小写。
   - A. 正确
   - B. 错误
7. 变量名必须以一个 ________ 字符、一个 ________ 字符或一个 ________ 字符开头。
8. 你应该避免使用 JavaScript 关键字和保留字作为变量名。
   - A. 正确
   - B. 错误
9. 下列哪项变量声明使用了 JavaScript 中有效变量名的变量？
   - A. `var return;`
   - B. `var my_house;`
   - C. `var my dog;`
   - D. `var 2cats;`
10. 在 JavaScript 中，数据包括数字、字符串、布尔、null、undefined、symbol 和对象。
11. 在 JavaScript 中表示指数时，你使用数字之后、指数之前的字母。
12. 下列哪项字符串声明是无效的？
    - A. `var mytext = "Here is some text!";`
    - B. `var mytext = "Here is some text!";`
    - C. `var mytext = "Here is some text!";`
    - D. `var mytext = "Here \n some text!";`
13. 下列哪些语句在 JavaScript 中是有效的？
    - A. `document.write("John, "Hi!")");`
    - B. `document.write("John, "Hi!")");`
    - C. `document.write("John, "Hi!")");`
    - D. `document.write("John said, \"Hi!")");`
14. ________ 字符用于添加到字符串中，其他情况下无法添加这些字符。
15. 下列哪项成功通过将 `myhobby` 添加到字符串来显示名为 `myhobby` 的变量值？
    - A. `document.write("I like to +myhobby every weekend!");`
    - B. `document.write("I like to " +myhobby" every weekend")`
    - C. `document.write("I like to myhobby every weekend!")`
    - D. `document.write("I like to " + myhobby + " every weekend")`

## 第 4 章：使用函数

### 核心技能与概念

- 什么是函数
- 为什么函数很有用
- 函数的结构
- 声明函数
- 定义函数的代码
- 函数命名
- 为函数添加参数
- 为函数添加返回语句
- 在脚本中调用函数
- 脚本标签：头部部分还是主体部分
- 从另一个函数调用函数
- 调用带参数的函数
- 调用带返回语句的函数
- 定义函数的其他方法
- 全局上下文
- 函数上下文
- 块上下文

### 定义函数的代码

大括号 ({ }) 包围着函数。左大括号标记函数代码的开始；接着是代码；最后，右大括号标记函数的结束，格式如下：

```javascript
function reallycool() {
    JavaScript code here
}
```

当函数被调用时，解释器将执行大括号内的所有代码（你将在本章的稍后部分学到）。当解释器遇到右大括号时，它知道函数已结束。解释器将移动到下一行代码，或者继续执行函数被调用之前正在进行的任何操作。

放置大括号最常见且推荐的格式是将左括号与函数声明放在同一行，如上一个代码示例所示。在这种格式下，可以看到代码块的左括号位于右侧，而右括号出现在左侧。这对于计算代码段中打开/关闭了多少个括号是一个实用的技巧。

当然，如果你有一个特别短的函数，你也可以将整个函数放在单行上，如下：

```javascript
function reallycool() { JavaScript code here }
```

大括号在这方面是灵活的，JavaScript 中令牌之间的空格、制表符和换行符会被忽略（令牌是指变量或函数名、关键字或代码中必须保持完好的其他部分）。因此，以下代码将是：

```javascript
function reallycool() {
    var a = 5; var b = 3; var c = 6; }
```

虽然这可能更难阅读，而且不是推荐的格式，但 JavaScript 仍然将其视为有效代码，因为其他语法是正确的。

在本书的示例中，我将把左括号与函数声明放在同一行，并在函数特别短时，可能会将整个函数放在一行上。

### 函数的命名

与变量一样，函数需要仔细命名，以避免脚本出现问题。适用于变量的相同基本规则适用于函数命名：大小写敏感、使用允许的字符以及避免关键字和保留字。请参阅第 3 章获取这些命名规则列表。

如果你使用反映用途的名称，函数将更容易记忆和调试。正如你在第 3 章中学到的，对于变量，你应该使用代表其值的名称，例如用 `examnumber` 表示页面上示例的编号。函数名应该告诉该函数将执行什么。例如，假设你创建了一个向页面写入某些文本的函数。它可能包含以下行代码：

```javascript
document.write("<strong>This is a strong statement!</strong>");
```

你可以将函数命名为 `text`，但可能描述得不够清楚，因为你可能有其他函数也会向页面写入文本。在内部，你可能会将其命名为类似 `show_important_message` 的名称，这样你就知道该函数是用于向浏览器打印一段加强强调的文本。完整函数显示如下：

```javascript
function show_important_message() {
    document.write("<strong>This is a strong statement!</strong>");
}
```

与变量一样，你在脚本中使用的函数越多，为它们使用有意义且易于记忆的名称就越重要。

### 为函数添加参数

参数（Arguments）允许函数从函数外部导入一个或多个值。参数设置在函数内部第一行的括号内，格式如下：

```javascript
function functionname(variable1, variable2)
```

作为参数引入的任何值都成为函数内部的变量，使用你在括号内赋予它的名称。

例如，这是如何定义一个带有参数（变量）`coolcar` 和 `coolplace` 的函数 `reallycool`：

```javascript
function reallycool(coolcar, coolplace) {
    JavaScript code here
}
```

注意在 JavaScript 中，当你为函数设置参数时不需要使用 `var` 关键字。JavaScript 在变量被设置为函数参数时会自动声明它们，因此在这里不使用 `var` 关键字。例如，像下面这一行是无效的：

```javascript
function really(var coolcar, var coolplace)
```

参数到底从哪里来？它们在你调用函数时从函数外部获取。你将在本章的稍后部分看到它是如何工作的。现在，你需要知道它们如何作为 JavaScript 函数的参数。

在其他语言中，变量在设置为参数时通常需要进行声明，而 JavaScript 会为你完成这一点。然而，当你在函数声明之外声明变量时，需要使用 `var` 关键字。

要提到的另一点是，在 JavaScript 中，"parameter"（参数）一词通常与"argument"词通用，所以它们始终指的是同一个东西。在编程中，这两个术语之间存在一些技术差异（parameter 是值的占位符，而 argument 是实际值），但在普通讨论中并不经常区分。为了简单起见，我使用 `arguments` 来指代所有值，但如果你想阅读更多关于编程中这些类型值的技术相似性和差异，以下 Stack Overflow 的讨论很有趣：stackoverflow.com/questions/15676/what-the-difference-between-an-argument-and-parameter

#### 使用值

当你为函数分配参数时，可以像使用变量一样使用它们。例如，将 `coolcar` 赋值给另一个变量：

```javascript
function really(coolcar, coolplace) {
  mycar = coolcar; // coolcar 被赋值
}
```

这会将 `coolcar` 的值返回给调用它的范围。而不是将其赋值给另一个变量，你可以直接在函数中使用 `coolcar`，如下：

```javascript
function really(coolcar, coolplace) {
  document.write("My is a " + coolcar);
}
```

如果 `coolcar` 的值是 `Corvette`，函数将打印：My is a Corvette

#### 使用多个参数

你可能注意到上一个示例有两个参数但只使用了一个。函数可以有尽可能少或尽可能多的参数。当你分配多个参数时，函数不需要使用所有它们。

在上一个示例中，第二个参数没有被使用。你可以这样修改函数以使用两个参数：

```javascript
function reallycool(cooler, coolplace) {
  document.write("My car is a " + cooler + " " + coolplace);
}
```

现在，如果 `cooler` 的值是 `Corvette`，`coolplace` 的值是 `Las Vegas`，函数在调用时将向浏览器打印以下行：

My car is a Corvette Las Vegas

你可以在函数第一行的括号内放置函数所需的任意参数。这是一个带有四个参数的示例：

```javascript
function reallycool(cooler, coolplace, coolfood, coolbreeze)
```

当你有多个参数时，记得用逗号隔开每个参数。

### 为函数添加返回语句

`return` 语句用于返回调用范围（目前是主脚本），并可以返回一个值。执行时，`return` 语句将立即返回，因此它通常是函数的最后一个语句或条件语句的结果（你将在第 6 章学习）。返回的值可以是变量或另一个表达式，使用以下格式：

```javascript
return varilename or expression;
```

例如，为了返回变量 `cooltext` 的值，返回语句如下：

```javascript
return cooltext;
```

这会将 `cooltext` 的值返回给调用它的范围。

假设你想编写一个函数，返回两个字符串相加后的结果。你可以使用 `return` 语句，如下例所示：

```javascript
function get_added_text() {
    var textpart1 = "This is ";
    var textpart2 = "fun!";
    var addedtext = textpart1 + textpart2;
    return addedtext;
}
```

在这个函数中，前两个变量被赋值为字符串值，而 `addedtext` 变量被赋予了这两个字符串相加的值。新值会被发送回调用它的脚本中。它返回了此字符串：

This is fun!

这个返回的值可以在调用该函数的作用域内使用。在目前的形式下，这个函数并不是很有用，因为字符串只是在函数内部定义的，而不是作为参数传入的。

```javascript
function get_added_text() {
    var textpart1 = "This is ";
    var textpart2 = "fun!";
    return textpart1 + textpart2;
}
```

这稍微缩短了代码，因为你不需要定义额外的变量值。稍后你将看到关于返回表达式的更多细节。

返回值可以是一个简单的值、一个计算结果，甚至为空。以下所有语句都是有效的：

| 语句 | 描述 |
| :--- | :--- |
| `return "This is cool";` | 返回一个字符串值 |
| `return 42;` | 返回一个数值 |
| `return true;` | 返回一个布尔值 |
| `return null;` | 返回一个 null 值 |
| `return 37 + 22;` | 返回一个数值 |
| `return;` | 返回空内容 |

所有这些语句都会将控制权交回函数之后的第一个 JavaScript 语句。返回空内容会在不发送回值的情况下实现这一点。

你也可以返回一个表达式，例如数字或字符串的相加（或你决定构建的任何其他表达式）。以下也是有效的 return 语句：

| 语句 | 描述 |
| :--- | :--- |
| `return "This is " + "cool";` | 返回两个字符串相加的结果 |
| `return 21+20+1;` | 返回三个数字相加的结果 |

它们将分别返回值 "This is cool" 和 42。

你将在下一节看到更多使用参数和 `return` 语句的有用函数的示例。

### 在脚本中调用函数

现在你已经了解了函数本身是如何运作的，你还需要学习如何在脚本中调用函数。在 JavaScript 中调用函数只需将函数名加上一组括号（左括号和右括号之间可以或没有参数），并以分号结束；就像普通的 JavaScript 语句一样：

```javascript
functionname();
```

你可以在脚本代码的任何地方调用函数。你甚至可以在另一个函数内部调用函数。实际上你从第 1 章开始就在调用函数了，每当你使用 `document.write()` 时，你都在调用一个函数。

一个良好的规则是让函数定义出现在脚本中函数调用之前。要确保你的函数定义在函数调用之前，最简单的方法是将所有的函数定义尽可能地放在脚本的开头（通常紧接变量声明之后）。

```javascript
var paycheck = 1200; // 定义了一个变量
function send_alert() {
    window.alert("This came from the function!"); // 定义了函数
}
send_alert(); // 在定义后调用函数
```

你会注意到用到了 `window.alert()` 方法，这是另一个函数。该方法会发送一个带有字符串作为参数的弹出警框。用户必须点击 OK 按钮来关闭警框。此框可以用于示例或测试代码。

在调用之前定义函数是一个良好实践的建议，而不是严格的规则。由于**函数声明提升（function declaration hoisting）**，函数可以在 JavaScript 的任何地方调用。JavaScript 解释器会首先遍历所有的 JavaScript 代码以寻找函数声明。它找到的任何函数声明都会提升（移动）到代码顺序的顶部。然后按照新顺序执行代码，这允许所有提升的函数在源代码的任何地方被调用。例如，下面的代码可以在没有函数声明提升的情况下工作：

```javascript
send_alert();
function send_alert() {
    window.alert("This came from the function!");
}
```

函数声明提升仅在使用函数声明定义函数时有效。关于此点的更多信息，请参阅本章节后面的"定义函数的其他方法"部分。

### 脚本标签：Head 部分或 Body 部分

在将脚本添加到 Web 页面而不是使用外部文件时，确保变量和函数声明位于 `head` 部分通常有助于确保脚本在 `body` 部分调用它们时是可用的。然而，由于 JavaScript 经常使用可能尚未加载的文档信息，这可能会出现问题。另一方面，当你需要编辑 HTML 代码时，在 `body` 部分有大量 JavaScript 代码也会带来麻烦（如果 JavaScript 在 `body` 部分，则必须放在 JavaScript 使用的所需信息的元素之后，以确保必要的信息已加载）。

现代 JavaScript 使用的一种做法是将 JavaScript 代码放在一个外部文件中（将脚本代码与 HTML 代码分离），然后将脚本标签放在 `</body>` 标签之前。这种放置的原因是它允许页面在尝试加载 JavaScript 文件之前先加载并显示。这使得页面加载更快，并允许 JavaScript 代码可以使用文档提供的 HTML 和 CSS。

### 创建警框

与其使用 `document.write()` 方法向屏幕上写入内容，你可以使用 `window.alert()` 方法创建一个警框。要显示警框，使用以下格式：

```javascript
window.alert("This is alert!");
```

现在你知道如何让警框弹出，但如何让它在页面加载后出现呢？你可以通过在 HTML 的 `</body>` 标签之前调用脚本来实现：

```html
<body>
  <h1>Hello</h1>
  <p>This is some text...</p>
  <script type="text/javascript" src="js_alert.js"></script>
</body>
```

将 HTML 文件保存为 `js_alert.html` 并在 Web 浏览器中查看。你可以看到，这确实是页面打开时显示警框的一种方法。然而，由于你正在学习函数，你将采取另一种方法。

#### 使用函数处理 JavaScript 框

下面的代码使用外部 JavaScript 文件中的函数来弹出警框。在你的 `js_alert.js` 文件中，将代码改为：

```javascript
function show_message() {
  window.alert("This is an alert!");
}
show_message();
```

你可以将函数定义放在外部 JavaScript 文件中并在 HTML 文件中调用它。

此示例创建一个名为 `show_message()` 的函数来执行显示警框的工作。只有在代码中调用 `show_message()` 时，警框才会显示。在这种情况下，函数在定义之后立即被调用。结果是一个带有 "This is an alert!" 消息的小型警框。

当警框出现时，你可能会看到页面暂停直到你点击 OK 按钮，或者它可能会继续加载等待你点击 OK。这取决于你的浏览器。

#### 函数与代码顺序

尽管上一个示例中的函数是先定义的，但并不意味着它会先执行。函数在被调用之前是不会执行的；换句话说，在运行到函数调用之前，JavaScript 不会使用该函数。

任何在函数调用之前的命令（且不属于函数定义部分）都将在函数执行之前执行。例如，我们可以如下修改 JavaScript 文件中的代码：

```javascript
function show_message() {
    window.alert("This is an alert!");
}
window.alert("I am first, ha!");
window.alert("I am second, ha!");
show_message();
```

此示例在第一行定义了相同的函数 `show_message()`。函数后面跟着两个 `window.alert` 命令，然后该行调用了该函数。用此新代码保存 `js_alert.js` 文件，并在浏览器中重新加载 `js_alert.html`。你将看到一个有趣的结果！

这两个弹窗命令是 JavaScript 看到的第一个可执行内容，它们最先。对函数的调用在最后，因此执行了该函数。结果是三个弹窗，顺序如下：

- 用户收到一个弹窗，显示 "I am first, ha!"，需要点击 OK 按钮将其关闭。
- 接着弹窗显示 "I am second, ha!"，查看者需要再次点击 OK。
- 最后执行函数，查看者看到弹窗 "This is an alert!"，并第三次点击 OK 以结束这一系列操作。

尽管这个示例在弹窗使用上有些过头，但它能帮助你理解函数是如何被调用的。

需要强调的另外一点是，函数的定义顺序并不重要，但它们调用的顺序很重要。考虑以下代码：

```javascript
function show_message_1() {
    window.alert("This is alert #1!");
}
function show_message_2() {
    window.alert("This is alert #2!");
}
show_message_2();
show_message_1();
```

在这里，函数的定义顺序是先 `show_message_1` 后 `show_message_2`，但 `show_message_2` 是先被调用的。由于调用顺序决定了执行顺序，第一个显示的消息将是 "This is alert #2!"，第二个将是 "This is alert #1!"

随着你经验的增加，选择在 `head` 或 `body` 中放置 `<script>` 标签的位置将变得容易。当脚本需要使用 HTML 文档中的信息时，`<script>` 标签通常被放在 `<head>` 部分，并设置一个函数在页面加载后初始化变量和其他函数（这用到了事件处理，将在第 8 章讨论），或者放在 `<body>` 部分紧邻结束的 `</body>` 标签之前。我将在书中使用后一种方法。

### 从另一个函数调用函数

在另一个函数内部调用函数是组织事件发生顺序的一种有用方法。通常，该函数被放在另一个有更大任务需要完成的函数内部。

当你在函数内部放置函数调用时，你应该在定义调用它的函数之前先定义要被调用的函数，正如前面建议的，函数应该在被调用之前定义。

这是一个两个函数的示例，第二个函数调用了第一个函数：

```javascript
function update_alert() {
  window.alert("Welcome! This site is updated daily!");
}
function call_alert() {
  update_alert();
}
call_alert();
```

注意 `update_alert()` 函数是实际操作发生的地方。其他所有内容都是函数。`call_alert()` 函数的作用仅仅是调用 `update_alert()` 函数以使其被执行。最后，你使用了启动整个序列的命令，即调用 `call_alert()` 函数。由于这是函数外的第一个 JavaScript 语句，它被首先执行。当它执行时，它只是调用了 `update_alert()` 函数，由该函数完成显示弹窗的工作。

由于函数声明提升（function declaration hoisting），如果你在调用 `update_alert()` 之后才定义它，大多数浏览器也能毫无问题地执行上述的示例。

现在假设你想创建三个函数来执行三个任务。为了确保它们按正确的顺序发生，你可以从另一个函数按顺序调用它们。这是一个使用三个函数的技巧示例，这些函数用于不同目的的弹窗：

```javascript
function update_alert() {
  window.alert("Welcome! This site is updated daily!");
}
function section_alert() {
  window.alert("Please visit the picture section!");
}
function links_alert() {
  window.alert("Also, check out my links page!");
}
function get_messages() {
  update_alert();
  section_alert();
  links_alert();
}
get_messages();
```

代码显示 `get_messages()` 函数按顺序调用了其他三个函数。这确保了它们按正确的顺序出现。这确保了弹窗按正确的顺序出现。

### 带参数调用函数

在 JavaScript 中，你调用函数时还可以向它传递参数。参数允许你向函数传递信息，使其更具活性和可重用性。

如果你想向函数发送值，你必须在发送它们之前声明变量并确保它们拥有值。在这里，变量的作用域变得重要。变量的作用域决定了它的定义。JavaScript 既有全局变量也有局部变量。

#### 使用全局变量

全局变量是第3章中学到的变量。由于它们定义在函数外部，因此可以在脚本的任何地方更改——函数内部或外部。全局变量定义在函数外部，如下代码所示：

```javascript
var mycar = "Honda";
var paycheck = 1200; // 这些是定义的全局变量
```

示例中的变量可以在脚本的任何地方更改。这意味着它们会被函数意外更改。为了理解全局变量如何受影响，考虑一个显示两个弹窗的示例。你想让一个弹窗显示购买某种汽车需要多少钱，让另一个显示你现在有多少钱以及拥有什么种汽车。如果你使用以下代码会发生什么？

```javascript
var mycar = "Honda"; // 这些被声明为全局变量
var paycheck = 1200;
function new_car() {
  mycar = "Ferrari"; // 哎！函数给赋值了新值
  paycheck = 3500;
  window.alert("You need $" + paycheck + " to get a " + mycar); // 这里的弹窗是你预期的
}
new_car();
window.alert("You make $" + paycheck + " and have a " + mycar); // 这里的弹窗不是你预期的
```

看起来像是在函数内部创建了新变量，尽管它们的名称相同。然而，脚本会在两个弹窗中输出以下文本：

You need $3500 to get a Ferrari

You make $3500 and have a Ferrari

显然，这不对。

如果一个函数接收两个参数，而你想发送第二个，你可以使用第一个，只要该函数能够正确地处理它。

此示例演示了为什么在声明变量时需要使用 `var` 关键字。如果不使用 `var` 关键字，你并没有在函数内部创建新变量（这将使它们成为局部变量）。相反，你正在改变全局变量的值——你发出的是重新赋值命令，而不是新命令。如果该变量尚未定义，在不使用 `var` 关键字的情况下声明它将创建一个同名的全局变量——这也会导致问题。为了解决这个问题，你只需要更改其中一个变量名，或者更好的做法是使用局部变量。

#### 使用局部变量

局部变量只能在声明它的函数内部使用。它不在函数外部，除非你通过参数将其传递给另一个函数。

在函数中创建局部变量的关键是确保你使用 `var` 关键字对其进行声明。否则，正如你在上一个示例中看到的那样，任何同名的全局变量都可能被改变。要声明局部变量，你必须将其放在函数内部并使用 `var` 关键字，如代码所示：

```javascript
function new_car() {
  var mycar = "Ferrari";
  var paycheck = "3500";
}
```

`mycar` 和 `paycheck` 变量是局部变量，只能由 `new_car()` 函数看到和修改。

因此，为了纠正上一部分的脚本，你只需要在函数内部添加 `var` 关键字来声明局部变量，如下：

```javascript
var mycar = "Honda";
var paycheck = 1200;
function new_car() {
  var mycar = "Ferrari";
  var paycheck = 3500;
  window.alert("You need $" + paycheck + " to get a " + mycar);
}
new_car();
window.alert("You make $" + paycheck + " and have a " + mycar);
```

现在，弹框应该按照你预期的方式出现：

- 你需要 $3500 买一辆 Ferrari
- 你赚了 $1200 并拥有一辆 Honda

正如你所看到的，当你将某些变量作为参数传递给函数时，变量的作用域可能非常重要。

#### 将变量作为函数参数

以下示例使用了变量参数。它将全局变量传递给函数。

```javascript
function check_alert(pcheck) {
  window.alert("You make $" + pcheck);
}
var paycheck = 1200;
check_alert(paycheck);
```

脚本从 `check_alert(pcheck)` 开始，它接收参数 `pcheck`。在函数之外的外部脚本中，全局变量 `paycheck` 被赋值为 1200。然后代码调用 `check_alert()` 函数并发送 `paycheck` 变量的值。

当这段代码调用 `check_alert()` 函数时，它发送了 `paycheck` 变量的值。该值通过括号中的参数名 `pcheck` 推送到函数中。

需要注意的是，`paycheck` 在 `check_alert()` 函数内部变成了一个局部变量。由于它是一个参数，因此在括号内不需要 `var` 关键字来使其成为局部变量。此外，由于代码发送了 1200 的值，`pcheck` 在函数开始时将是 1200。更改 `pcheck` 的值不会改变 `paycheck` 的值，因为 `pcheck` 是局部变量。

#### 使用值参数

你也可以直接发送一个值作为参数。你不需要为了发送参数而声明全局变量，只需发送一个在函数内部转换为局部变量的值。这允许你临时发送一个值，并消除了准备全局变量的需要。

需要记住的一点是，如果你发送的是字符串值，需要将其包含在引号中。以下函数向名为 `text_alert()` 的函数调用了一个字符串值 `"something"`：

```javascript
text_alert("something");
```

例如，可以对上一部分的示例进行修改，通过使用变量参数在一行内添加更多信息：

```javascript
function check_alert(pcheck, car) {
  window.alert("You make $" + pcheck + " " + car);
}
check_alert(1200, "Corvette");
```

在这个示例中，函数调用了两个参数。第一个是数值值，不使用引号。第二个值是字符串，需要包含在引号中。这些值随后被发送到函数中，它们分别位于局部变量 `pcheck` 和 `car` 中。它们现在可以在函数中使用并在警框中显示这句话：

- 你赚了 $1200 并拥有一辆 Corvette

参数也可以使用表达式发送，如下所示：

```javascript
check_alert(500+700, "Cor" + "vette");
```

JavaScript 将评估每个表达式并将结果作为参数返回给函数。因此，前面的代码将产生相同的结果（500 加 700 得到 1200，拼接 "Cor" 和 "vette" 得到 "Corvette"）：

- 你赚了 $1200 并拥有一辆 Corvette

#### 参数是可选的

另一个要提的一点是，向函数发送参数是可选的。函数将尽力在没有发送参数值的情况下完成它的工作。

### 使用带有返回语句的函数调用

你可以将函数的执行赋值为变量的值。通过这种方式，变量获取了函数返回的值并可以在脚本后续部分使用。这是声明具有函数返回值的变量的格式：

```javascript
var variableName = functionName();
```

考虑这个示例，它有一个返回两个字符串的函数：

```javascript
function get_added_text() {
  var textpart1 = "This is ";
  var textpart2 = "fun";
  var addedtext = textpart1 + textpart2;
  return addedtext; // 添加的结果返回给脚本
}
var alerttext = get_added_text(); // 函数的结果赋值给变量
window.alert(alerttext); // 变量的值用作文本
```

正如你所看到的，函数将 `get_added_text()` 函数的值返回给变量 `alerttext`，你可以在脚本后续使用该文本。该变量用于向用户发送带有添加结果的警框。警框消息显示为

This is fun!

现在，这很有趣吧？随着你阅读这本书，你会看到返回语句的更多实际应用。

最后一点需要记住的是，如果你将一个不返回值的函数结果赋值给变量，该变量的值将为 `undefined`。例如，查看以下代码：

```javascript
function get_added_text() {
  var textpart1 = "This is ";
  var textpart2 = "fun"; // 这个函数没有返回任何内容！
  var addedtext = textpart1 + textpart2;
}
var alerttext = get_added_text(); // 函数的结果赋值给变量，但由于函数没有返回任何内容，变量被赋值为 undefined
window.alert(alerttext); // 警框的值将是 undefined！
```

### 定义函数的其他方式

在查看脚本时，或者在编写新脚本发现有用时，你可能会遇到几种定义函数的方法：函数声明（已经讨论过）、函数表达式、函数构造函数和箭头函数。

#### 函数声明

这是你到目前为止一直使用的方法，也是本书中经常会使用的方法。正如你所记得，你只需要如下所示声明函数：

```javascript
function functionname() {
  // 此处编写函数的代码
}
```

你还可以像在本章前面提到的那样，添加参数和/或返回语句。

#### 函数表达式

函数表达式与函数声明非常相似，并使用以下格式：

```javascript
var varname = function(arguments) {
  // 此处编写函数的代码
};
```

注意右括号后面有一个分号（;）。由于函数正在被赋值给变量，因此需要分号来完成变量赋值语句。请注意，在这种情况下，赋值给变量的是函数本身，而不是函数执行的结果（正如你之前做的那样）。此外，函数在这里并没有被执行，只是被赋值。

函数声明和函数表达式之间的主要区别如下：

- 函数表达式将函数赋值给变量，并需要分号来完成语句。
- 由于在函数关键字之后没有分配名称，因此它被认为是一个匿名函数。可以使用变量名来调用该函数。
- 函数表达式不使用函数声明提升（hoisting），因此在代码中定义之前无法调用它。

作为最后一点的例子，请看下面的代码。它会导致错误：

```javascript
send_alert("This is " "broken!");
var send_alert = function(textpart1, textpart2) {
  window.alert(textpart1 + textpart2);
}
```

注意函数在定义之前就被调用了。由于该函数被定义为变量赋值，在赋值完成之前无法使用它（它无法利用函数提升）。

为了让其正常工作，必须将函数移动到定义之后的位置：

```javascript
var send_alert = function(textpart1, textpart2) {
  window.alert(textpart1 + textpart2);
}
send_alert("This is ", "working!");
```

现在函数调用位于函数定义之后，代码将按预期工作。这是在使用函数表达式时需要记住的一个重要区别，因为它们在定义之前无法执行。

在处理 JavaScript 事件时，匿名函数非常有用。例如，为了响应用户在网页上点击鼠标的动作，你可以为 document 的点击事件编写一个简单的函数，然后在下面的代码中调用它：

```javascript
function do_not_click() {
  window.alert("Do not click on my page!");
}
document.onclick = do_not_click;
```

这声明了函数，然后在之后调用它（不带处理程序）来处理点击事件。然而，你可以使用匿名函数将这两个步骤合并为一个，如下：

```javascript
document.onclick = function() {
  window.alert("Do not click on my page!");
}
```

由于对此事件的响应位于 JavaScript 代码的一个地方，匿名函数是处理事件的一种方便方法，不需要在其他地方声明函数然后调用它。这种技术以及用于事件处理的代码类型（如之前的代码列表）将在第 10 章进行更详细的讨论。

#### 函数构造函数

函数构造函数以创建对象实例的方式创建一个函数对象（这将在第 9 章中讨论）：

```javascript
var functionname = new Function(arguments, code for function);
```

它的工作方式与其他函数类似，但这种方法的主要缺点是性能低于其他方法（它每次被使用时都会求值，而不是解析一次）。建议使用另外两种方法之一来定义函数。

#### 箭头函数

箭头函数是在 ES6 中引入的，作为缩短函数表达式语法的方法，并为返回对象提供更简单的语法。你在这里看到基础知识，我们将在本书的后半部分详细介绍这些函数。

箭头函数的基本语法看起来如下：

```javascript
var sum = (num1, num2) => {
  return num1 + num2;
};
```

这与函数表达式一致。例如，下面的代码使用函数表达式实现了相同的操作：

```javascript
sum = function (num1, num2) {
  return num1 + num2;
};
```

### 尝试 4-1 使用函数

```
pr4_1.html
prjs4_1.js
```

在这个项目中，你将创建一个使用两个 JavaScript 函数的脚本。第一个函数使用参数，并根据发送给函数的参数创建一个带有消息的警框框。第二个函数在连接两个字符串后返回一个字符串。浏览器中脚本的结果是根据发送给第一个函数的信息以及从第二个函数返回给脚本的信息生成的两个警框消息。

#### 步骤

1. 创建一个 HTML 文件，让 body 部分为空，并保存为 `pr4_1.html`。
2. 创建一个 JavaScript 文件并保存为 `prjs4_1.js`。步骤 3-6 使用此文件。
3. 创建一个名为 `check_alert()` 的函数，它接收两个参数：`pcheck` 和 `car`。
4. 在函数内部，使用 `window.alert()` 方法发送一个警框，显示 "You make $" 加上 `pcheck` 的值，然后是一个空格，再加上 `car` 的值。
5. 创建一个名为 `get_added_text()` 的函数，它返回两个字符串相加的结果："This project is " 和 "almost fun!"。
6. 调用 `check_alert()` 函数并发送值 1500 和 "Mustang"。
7. 创建一个名为 `alerttext` 的变量，并将 `get_added_text()` 函数的结果赋值给它。
8. 使用 `window.alert()` 方法发送 `alerttext` 变量的值。
9. 完成后，JavaScript 文件应该像这样：

```javascript
function check_alert(pcheck, car) {
  window.alert("You make $" + pcheck + " " + car);
}
function get_added_text() {
  var textpart1 = "This project is ";
  var textpart2 = "almost fun!";
  return textpart1 + textpart2;
}
check_alert(1500, "Mustang");
var alerttext = get_added_text();
window.alert(alerttext);
```

10. 保存外部 JavaScript 文件。
11. 打开 `pr4_1.html` 文件并在浏览器中查看以查看结果。
12. 当你打开网页时，你应该能看到两个警框（alert）消息：

你有一辆野马，并赚了 $1500

这个项目几乎很有趣！

#### 练习总结

在这个项目中，你创建了一个使用两个 JavaScript 函数的脚本。第一个函数使用参数，并根据发送给函数的参数创建一个带有消息的警框框。第二个函数在连接两个字符串后返回一个字符串。浏览器中脚本的结果是根据发送给第一个函数的信息以及从第二个函数返回给脚本的信息生成的两个警框消息。

### 作用域/上下文基础

在 JavaScript 中，当涉及作用域（变量或函数的上下文，它是有用且有效的）时，有一些关键点需要记住。例如，在本章的早些时候，你能够通过在函数内部使用 `var` 关键字声明来创建局部变量。这些局部变量仅在定义它们的函数内部有效，这防止了它们被主脚本（全局上下文）修改。JavaScript 中两个主要的执行上下文是全局上下文和函数上下文。此外，`let` 关键字允许块上下文。

#### 全局上下文

JavaScript 中的全局上下文包含任何不在函数内的代码。考虑这段代码：

```javascript
var myname = "JavaScript";
function say_name() {
  var mydog = "Joey" + " has a dog named ";
  window.alert(myname + mydog);
}
// 调用函数
say_name();
window.alert(myname);
// window.alert(mydog);
```

该函数在全局作用域中创建，因此可以在全局作用域中调用。在函数内部定义的任何变量都在函数的局部作用域内，无法从全局上下文访问。

此警框 (`myname`) 将按预期工作，使用了全局变量和函数上下文。

此警框 (`mydog`) 会导致错误，因为在全局上下无法访问 `mydog`。

如示例所示，全局变量名在定义后可以在代码的任何地方使用。`say_name()` 函数定义在全局作用域中，因此可以从代码的任何地方调用。然而，`mydog` 变量仅在 `say_name()` 函数内部可用，无法在此上下文之外使用。尝试在脚本的警框中使用它将导致 JavaScript 错误。

通常情况下，你的脚本变得越复杂，离开全局上下文就越好，因为全局变量可能会被任何其他上下文意外覆盖。

#### 函数上下文

在 JavaScript 中，函数会创建一个新的上下文。正如你所见的，函数内部声明的任何变量在函数外部都是不可用的。关于函数的一个新知识点是，它们可以在内部嵌套其他函数。考虑以下代码：

```javascript
var myname = "John";
function say_name () {
  var mydog = "Josy";
  function say_food () {
    var myfood = "Pizza";
    window.alert(myname + " and " + mydog + " like " + myfood);
  }
  window.alert(myname + " has a dog named " + mydog);
  say_food();
}
say_name ();
```

`say_food()` 只能在 `say_name()` 函数内部被调用，在全局上下文中不可用。它可以使用 `say_name()` 上下文或全局上下文的任何变量。

`say_name()` 函数，它内部调用了 `say_food()` 函数。`say_name()` 函数可以从全局上下文调用，但它有一个局部变量 `mydog` 和局部函数 `say_food()`。

`say_name()` 函数内部的 `say_food()` 函数。`say_food()` 函数可以使用定义在 `say_name()` 或全局上下文中的任何变量。如所示，这创建了一个基于嵌套函数的作用域链。链中最内层的函数拥有的变量受保护最不易被修改，而全局上下文的变量保护最少（这些是公共的，即使在最内层函数中也可以）。

示例中的每个上下文以及上下文可以使用变量/函数在这里：

- 全局上下文：
  - `myname`
- `say_name()` 上下文：
  - `myname`（来自全局）
  - `mydog`
  - `say_food()`
- `say_food()` 上下文：
  - `myname`（来自全局）
  - `mydog`（来自 `say_name()`）
  - `myfood`

注意 `myname` 可以在所有三个上下文中使用，`mydog` 可以在两个（`say_name` 和 `say_food()` 上下文）中使用，而 `myfood` 只能在一个（`say_food()` 上下文）中使用。

记住这一点很重要，因为 JavaScript 只有在你使用 `var` 关键字时才使用函数创建上下文。其他的块级结构（如条件语句和循环）不是为此目的设计的，除非你使用 `let` 关键字，它将在下一节中描述。

可以通过调用 `eval()` 方法创建第四种类型的执行上下文；然而，`eval()` 方法会导致许多问题（例如速度和安全问题），并且永远不应该使用。

#### 块上下文

如果使用 `let` 关键字代替 `var` 定义变量，则为变量创建块上下文。函数在花括号 `{}` 之间提供块上下文。其他的块上下文由条件语句和循环创建，这些将在第 7 章中进一步描述。

`let` 关键字的作用与在函数上下文中使用时相同，正如我们已经看到的那样。它的优势在于能够为变量创建块作用域。例如，以下代码显示了一个条件语句（该概念将在第 7 章进一步讨论）：

```javascript
let myname = "John";
if (myname == "John") { // 使用 "if" 语句检查 myname 的值。
  let myname = "Jane"; // let 关键字在块上下文中定义变量。
  window.alert(myname); // 发送带有块上下文值 myname 的警框。
}
window.alert(myname); // 发送带有全局上下文值 myname 的警框。
```

首先，使用 `let` 关键字创建一个全局上下文变量 (`myname`)。"if" 语句在花括号之间创建了一个块上下文。`let` 关键字可以利用这个上下文，在该上下文中创建一个具有自身值的 `myname` 变量。结果是块上下文 `myname` 的值为 "Jane"，它在块上下文的警框中发送。一旦该块上下文结束，将发送另一个警框。

`let` 关键字的另一个优势是，如果你在同一个作用域内声明两次变量，JavaScript 解释器会报错。

由于使用 `let` 关键字变量的作用域更加清晰，建议以后用它代替 `var`。

#### const 关键字

`const` 关键字可以用于保持不变的值。这有助于防止其他代码更改其值。例如，如果你声明了一个常量并尝试更改它，解释器将抛出错误，如下：

```javascript
const money = 5; // 定义了一个常量。
money = 10000; // 这抛出一个错误。
```

不幸的是，我在这里无法给自己额外的钱。由于使用了 `const` 关键字定义，它必须保持不变。`const` 关键字像 `let` 一样使用块作用域。出于这个原因，在定义非函数类型时使用 `let` 和 `const` 是一个好主意。

### 练习 4-2 编写自己的函数

在这个项目中再次创建一个 HTML 页面，但在这个项目中，你将使用函数尽可能将信息排除在全局上下文之外（你将在全局上下文中调用单个全局函数）。

#### 步骤

1. 创建一个 HTML 文件，让 body 部分为空，并保存为 `pr4_2.html`。
2. 创建一个 JavaScript 文件并保存为 `prjs4_2.js`。步骤 3-6 使用此文件。
3. 创建一个名为 `display_HTML()` 的函数。
4. 在函数内部，使用 `let` 关键字创建一个名为 `myheading` 的变量，并用它持有以下代码：

```html
<h1>Hello, World!</h1>
```

5. 创建一个名为 `mytext` 的变量，同样使用 `let` 关键字，并用它持有以下代码：

```html
<p>虽然了解你的世界很不错，但有些事情我不乐意在全局上下文中分享——不能把持有此文本的变量放在包含它的块之外吗！哈！</p>
```

6. 创建一个 `document.write()` 语句，将两个变量的值都写入页面上并结束该函数。
7. 插入调用该函数的代码。
8. 完成后，JavaScript 文件应该像这样：

```javascript
function display_HTML() {
  let myheading = "<h1>Hello, World!</h1>";
  let mytext = "<p>While it is nice to know you, there are some things that I am comfortable sharing in a global context. You can't alter the variable that holds this text outside of the block that contains it: Hi!</p>";
  document.write(myheading + mytext);
}
display_HTML();
```

9. 在 HTML 页面的 body 中，在文档中放置标签（指向 `prjs4_2.js` 文件），以便脚本在页面上显示 HTML 代码。
10. 完成后，保存 HTML 页面和 JavaScript 文件，并在浏览器中查看 HTML 页面以查看其是如何运行的。

结果应该是一个显示为 "Hello, World!" 的标题，后面是一段长文本，脚本在其中解释了它希望某些信息不受到外部影响而被改变。

#### 练习总结

在这个项目中，你利用了关于函数和上下文的知识创建了一个脚本。该脚本的结果是 HTML 页面显示了信息，同时保护变量值不被全局上下文中可能发生任何更改的内容修改。

### 第 4 章自测

1. 通常情况下，函数是位于较大结构内部的一个小部分，用于执行单个或一系列的。
2. 函数有用的两个原因是什么？
   - A. 它们让简单的脚本变得复杂，并让非代码人员更难阅读脚本。
   - B. 它们提供了一种方法将脚本的不同部分组织成必须完成的不同任务中，并且它们可以被重用。
   - C. 它们让简单的脚本变得复杂，并且它们可以被重用。它们提供了一种方法将脚本的不同部分组织成必须完成的不同任务中，并让非代码人员更难阅读脚本。
3. 在函数的第一行，你 ________ 它定义为一个函数，________，并指明它是否接受任何 ________。
4. 要声明一个函数，你使用关键字 ________。
   - A. `var`
   - B. `switch`
   - C. `function`
   - D. `for`
5. 什么包围了函数内部的代码？
   - A. { }（大括号）
   - B. ::（冒号）
   - C. []（方括号）
   - D. 什么都没有
6. 函数名对大小写敏感。
   - A. 正确
   - B. 错误
7. JavaScript 关键字可以作为函数名。
   - A. 正确
   - B. 错误
8. 下列中哪项是 JavaScript 中有效的函数名？
   - A. `function my()`
   - B. `function var()`
   - C. `function get_text()`
   - D. `function 24hours()`
9. ________ 被用于允许函数从函数外部导入一个或多个值。
10. 参数设置在函数的第一行，在一组 ____ 内部。
    - A. { }（大括号）
    - B. ()（圆括号）
    - C. []（方括号）
    - D. 无
11. 多个参数之间用什么符号分隔？
    - A. 点
    - B. 冒号
    - C. 分号
    - D. 逗号
12. 下列哪项是 `window.alert()` 的有效用法？
    - A. `win.alt("This is text");`
    - B. `window.alert("This is text");`
    - C. `window.alert("This is text");`
    - D. `window.alert("This is text");`
13. 下列哪项正确调用了名为 `some_alert()` 的函数并发送了两个字符串值作为参数？
    - A. `some_alert();`
    - B. `some_alert("some", "words");`
    - C. `some_alert("some", "words");`
    - D. `SOME_alert("some", "words");`
14. 下列哪项正确地将名为 `get_something()` 的函数结果赋值给名为 `shopping` 的变量？
    - A. `var shopping = get_something();`
    - B. `var shopping = "get_something";`
    - C. `var Shopping = get_Something;`
    - D. `shopping = getsomething;`
15. 一个 ____ 可以在 JavaScript 的任何地方使用。
16. ____ 和 ____ 关键字在当前块上下文中创建值。

## 第 5 章：JavaScript 运算符

### 核心技能与概念

- 理解运算符类型
- 理解算术（数学）运算符
- 理解赋值运算符
- 理解比较运算符
- 理解逻辑运算符
- 理解运算顺序

运算符在脚本中承担了大部分工作。在之前的章节中，你已经见过赋值 (`=`) 和加法 (`+`) 运算符的使用示例。JavaScript 提供了许多其他类型的运算符来执行各种操作。

本章将开始向你介绍不同类型的 JavaScript 运算符。然后，你将学习每个运算符及其在脚本中的用法。最后，你将学习运算顺序。

### 理解运算符类型

运算符在脚本中承担了大部分工作。在之前的章节中，你已经见过赋值 (`=`) 和加法 (`+`) 运算符的使用示例。JavaScript 提供了许多其他类型的运算符来执行各种操作。本章将开始向你介绍不同类型的 JavaScript 运算符。然后，你将学习每个运算符及其在脚本中的用法。最后，你将学习运算顺序。

### 理解算术（数学）运算符

对于数学计算，你使用算术运算符。你可以使用的值可以是任何类型的值。例如，你可以使用两个变量、两个数字，或者一个变量和一个数字。其中一些运算符能够对单个值执行任务。

作为一个快速回顾，你会记得在之前的章节中用加法运算符将两个字符串相加。这里有一个字符串值结合加运算符的示例：

```javascript
window.alert("I begin and " + "this is the end.");
```

当一个值是变量时，你也可以使用加法运算符，如下例：

```javascript
let part1 = "begin and ";
let part2 = "this is the end.";
window.alert("I begin and " + part2);
```

当两个值都是变量时，加法运算符同样有效，如下例：

这些示例说明了你可以如何与多个值或变量使用算术运算符。这为你编写脚本代码提供了一些灵活性。

### 理解赋值运算符

赋值运算符用于分配新值。正如你在第 3 章中学到的，赋值运算符之一是 `=`。

### 理解比较运算符

比较运算符用于比较两个值、变量，或者两个语句。它们使用符号如 `>`（用于"大于"）和 `<`（用于"小于"）。

| 运算符 | 符号 | 功能 |
| --- | --- | --- |
| 加法 | `+` | 将两个值相加 |
| 减法 | `-` | 从一个值减去另一个值 |
| 乘法 | `*` | 将一个值乘以另一个 |
| 除法 | `/` | 将一个值除以另一个 |
| 取模 | `%` | 将一个值除以另一个并返回余数 |
| 递增 | `++` | 单数字加 1 的快捷方法 |
| 递减 | `--` | 单数字减去 1 的快捷方法 |
| 一元加号 | `+` | 保持值不变，但会尝试将非数字值转换为数字 |

表 5-1 算术运算符

### 加法运算符 (+)

正如你所看到的，加法运算符可以用于合并两个字符串。它也用于在数学计算中相加数字。

#### 用于结果的变量

加法运算符的一个用途是将两个数字相加得到数学结果。在相加数值时，你通常会将结果赋值给变量，并在稍后使用该变量的值。例如，要计算 4 加 7 的值并显示结果，你可以这样写代码：

```javascript
let thesum = 4 + 7; // 使用加法运算符相加两个数字
window.alert(thesum); // 加法结果以警框的形式显示给观众
```

结果是一个显示为 11 的警框。

为了让示例变得复杂一点，你可以将其中一个数字改为变量：

```javascript
let num1 = 4; // 将一个数字赋值给变量
let thesum = num1 + 7; // 将数字与变量相加并将总和赋值给新变量
window.alert(thesum);
```

结果与上一个示例相同：一个显示为 11 的警框。

进一步扩展示例，你可以让两个数字都变成变量：

```javascript
let num1 = 4,
num2 = 7;
let thesum = num1 + num2; // 使用加法运算符相加两个变量
window.alert(thesum);
```

这个示例提供了最大的灵活性，因为你可以更改两个数字变量的值并获得新结果，而无需深入脚本进行修改。

#### 操作数

与运算符一起使用的每个值被称为操作数。JavaScript 中的大多数运算符一次处理两个操作数。例如，以下代码包含两个操作数：7 和 4。

```javascript
let thesum = 7 + 4;
```

运算符两侧的值都是操作数。当在使用其他数据类型或使用变量时，情况也是如此：

```javascript
let num1 = 7,
mytext = "4",
thesum = num1 + mytext;
```

当语句中多次使用接受两个操作数的运算符时，JavaScript 将使用运算符的顺序（将在"理解运算"章节中解释），并一次处理一个运算符和两个操作数来完成任务。在加法运算符的情况下，如果没有其他运算符或括号，则运算顺序将从左到右进行。考虑以下内容：

```javascript
let thesum = 2 + 3 + 1;
```

首先，将计算 `2 + 3` 部分得到结果 5。然后，它被用作第一个操作数来完成计算 `5 + 1`，这将给出最终结果 6。

某些运算符（称为一元运算符）只使用一个操作数。运算符直接放在孤立的操作数之前或之后。例如：

```javascript
let mymoney = 5;
mymoney++;
```

在这种情况下，使用了递增运算符，唯一的操作数是该变量。随着本章的学习，你将看到更多关于递增运算符和一元运算符的知识。

#### 计算中的类型强制转换

需要注意的是，在处理算术运算符时，JavaScript 会执行强制转换（如果认为有必要，则尝试更改值的数据类型）。当你使用加法和其他算术运算符时，你需要意识到 JavaScript 会将不同类型（如整数（非小数值）和浮点数（小数值））强制转换为适当的类型。例如，你可能会有以下代码：

```javascript
let num1 = 4,
num2 = "7",
thesum = num1 + num2;
window.alert(thesum);
```

当运行脚本时，你将看到一个带有结果的警框。JavaScript 将整数和浮点数相加，并返回了一个浮点数：11。JavaScript 自动执行此操作，因此你需要确保这些值将带给你预期的结果。例如，如果你将一个数字和一个字符串相加，结果将就像是你合并了两个字符串。看这个示例：

```javascript
let num1 = 4; // 此变量是一个数字
num2 = "7"; // 错误！此变量是一个字符串，而不是数字
thesum = num1 + num2; // 当它们相加时，它们会被合并
window.alert(thesum);
```

这看起来像是在加数字 4 和 7，因为它们看起来都像数字。问题是，在这种情况下 7 是一个字符串而不是数字，因为它周围有引号。这导致 4 被转换为字符串，然后将两个字符串相加（拼接）。在警框中出现的结果可能会让你感到惊讶。

你得到的不是预期的答案 11，而是 47。当两个值作为字符串相加时，它们会合并在一起而不是进行数学相加。对于字符串，"4"+"7"="47"。其他算术运算符像加法运算符一样进行转换，因此如果你在脚本遇到意外结果，请注意这一点。

#### 特殊规则

加法运算符在尝试执行计算或拼接时有一些特殊规则。以下是一些常见的情况：

- 如果一个操作数的特殊值为 `NaN`（不是数字），而另一个操作数是数字，则结果将是 `NaN`。
- 如果一个操作数是字符串，另一个操作数将被强制转换为字符串。
- 如果两个操作数都是字符串，则字符串将直接拼接。

如果你有两个数字接着一个字符串，数字将先相加然后进行转换。例如，`35 + 5 + "th Avenue"` 会先计算 `35+5`（因为运算符从左到右求值），然后结果（40）将与字符串 "th Avenue" 拼接，得到 "40th Avenue"。

作为这些规则生效的示例，`NaN` 与数字相加的结果。如果与字符串相加，字符串 "NaN" 将与另一个值拼接：

- `4 + NaN` 为 `NaN`
- `"Hi" + NaN` 为 `"HiNaN"`

随着本章的学习，你将看到其他运算符也有特殊规则，如果你在脚本中遇到意外结果，这些规则可能会很有帮助。

### 减法运算符 (-)

减法运算符用于从左侧的值减去右侧的值，就像在数学中一样。这是一个示例：

```javascript
let result = 10 - 3; // 使用减法运算符相减两个数字
```

这段代码从 10（运算符左侧的数字）减去 3（运算符右侧的数字）。结果是 7。

#### 特殊规则

对于减法运算符，有一些特殊规则：

- 如果一个操作数是 `NaN`，则结果将是 `NaN`。
- 如果一个操作数是非数字类型（例如，字符串、布尔值等），JavaScript 尝试将该值强制转换为数字并执行减法。如果无法转换该值，结果将是 `NaN`。

### 除法运算符 (/)

除法运算符用于将其左侧的值除以其右侧的值。例如，代码 `4 / 2` 意味着 4 除以 2，结果为 2。要查看此操作的 JavaScript 示例，请看下这段代码：

```javascript
let num1 = 10 / 2; // 两个数字相除
```

结果是 5，即将 10 除以 2 的结果。

#### 特殊规则

- 如果其中一个操作数是 `NaN`，结果将是 `NaN`。
- 如果数字零除以数字零，结果将是 `NaN`。
- 如果任何其他有限数字除以数字零，结果将是特殊值 `Infinity`（无穷大）。
- 如果其中一个操作数是数字以外的数据类型，它将尝试转换该值并执行除法。如果无法转换值，结果将是 `NaN`。

#### 除以零

当你使用除法运算符时，需要注意不要以某种方式进行除零操作。如果你这样做了，结果将是 `Infinity`。以下代码展示了这种情况发生的一个示例（尽管不太可能完全这种方式精确发生）：

```javascript
let num1 = 10,
num2 = 0,
theresult = num1 / num2; // 噢不！在这一行你正在除以零
window.alert(theresult); // 这个警报将不是数字
```

如果你将这段代码放在文档中，你可能会看到类似这样的警报框。

为了避免除以零，请注意放置在除法运算符右侧的数字或变量。

### 取模运算符 (%)

取模运算符用于将其左侧的数字除以其右侧的数字，然后给出除法的整数余数结果。回想一下你学习过长除法，并将余数作为答案的一部分，而不是将其转换为小数或分数。11 除以 2 得到 5，余数为 1。余数 1 就是当你写下 `11 % 2` 时取模运算符给你的结果。

以下是 JavaScript 中的示例：

```javascript
let num1 = 11 % 2; // 使用取模运算符来获取余数
window.alert(num1);
```

结果是一个显示余数值的警报框，该数值为 1。如果计算没有余数，结果将是 0。

这是最后一个同时作用于两个值的算术运算符。接下来是一次只作用于一个值的一元运算符。

### 自增运算符 (++)

自增运算符是一元运算符，它将其唯一操作数的值加 1。使用它的效果取决于该操作数放置在操作数之前还是之后。

#### 操作数前的自增运算符

当自增运算符放在操作数之前时，它会将操作数的值加 1，然后执行语句的其余部分。这里有一个示例：

```javascript
let num1 = 2;
theresult = ++num1;
```

在这种情况下，变量 `num1` 的初始值为 2。然而，当代码将值赋值给变量 `theresult` 时，它在赋值发生之前增加了 `num1` 的值。先发生自增，是因为自增运算符在操作数的前面。所以，`num1` 的值设置为 3 (2+1)，然后赋值给变量 `theresult`，该变量获得值 3。

#### 操作数后的自增运算符

如果你将自增运算符放在操作数之后，它会在赋值后改变操作数的值。考虑这个示例：

```javascript
let num1 = 2;
theresult = num1++;
```

与上一个示例一样，`num1` 的初始值为 2。在下一行，自增运算符用在操作数之后。这意味着代码将 `num1` 的当前值赋值给变量 `theresult`，在完成之后，它增加了 `num1` 的值。因此，只有在赋值完成后，你才得到了 `num1` 的新值。变量 `theresult` 被赋予值 2，然后 `num1` 变为 3。如果你在此之后使用 `num1`，它的值将是 3。

另一种查看自增运算符在操作数之前和之后如何工作的方法是在你的浏览器中运行以下脚本。注意第一个警报中的值是什么，第二个警报中的值是什么。

```javascript
let num1 = 2;
result = ++num1;
alert("num1 = " + num1 + " result = " + result);
num1 = 2;
result = num1++;
alert("num1 = " + num1 + " result = " + result);
```

在第一个警报中，你将看到 `num1=3 result=3`。因为在这里 `++` 运算符用在操作数之前，`num1` 的值增加了 1 并赋值给变量 `result`。在第二个警报中，你将看到 `num1=3 result=2`。这是因为 `++` 运算符用在操作数之后，所以 `num1` 的值在赋值给变量 `result` 之后增加。变量 `result` 值 2，但 `num1` 将增加到 3。注意，你不需要执行赋值来使用此运算符。你只需要输入它即可。

### 自减运算符 (--)

自减运算符是一元运算符，它将其唯一操作数的值减 1。使用它的效果取决于该操作数是放置在操作数之前还是之后。

#### 操作数前的自减运算符

当自减运算符放在操作数之前时，它会将操作数的值减 1，然后执行语句的其余部分。这里有一个示例：

```javascript
let num1 = 2;
theresult = --num1;
```

在这种情况下，变量 `num1` 的初始值为 2。然而，当代码将值赋值给变量 `theresult` 时，它在赋值发生之前减少了 `num1` 的值。先发生自减是因为自减运算符在操作数的前面。所以，`num1` 的值设置为 1 (2-1)，然后赋值给变量 `theresult`，该变量获得值 1。

#### 操作数后的自减运算符

如果你将自减运算符放在操作数之后，它会在赋值后改变操作数的值。考虑这个示例：

```javascript
let num1 = 2;
theresult = num1--;
```

与上一个示例一样，`num1` 的初始值为 2。在下一行，自减运算符用在操作数之后。这意味着代码将 `num1` 的当前值赋值给变量 `theresult`，在完成之后，它减少了 `num1` 的值。因此，只有在赋值完成后，你才得到了 `num1` 的新值。变量 `theresult` 被赋予值 2，然后 `num1` 变为 1。如果你在此之后使用 `num1`，它的值将是 1。

另一种查看自减运算符在操作数之前和之后如何工作的方法是在你的浏览器中运行以下脚本。注意第一个警报中的值是什么，第二个警报中的值是什么。

```javascript
let num1 = 2;
result = --num1;
alert("num1 = " + num1 + " result = " + result);
num1 = 2;
result = num1--;
alert("num1 = " + num1 + " result = " + result);
```

在第一个警报中，你将看到 `num1=1 result=1`。因为在这里 `--` 运算符用在操作数之前，`num1` 的值减少了 1 并赋值给变量 `result`。在第二个警报中，你将看到 `num1=1 result=2`。这是因为 `--` 运算符用在操作数之后，所以 `num1` 的值在赋值给变量 `result` 之后减少。变量 `result` 值 2，但 `num1` 将减少到 1。

### 一元加运算符 (+)

一元加运算符是一元运算符，它保持其唯一操作数的值不变，但会尝试将非数字值转换为数字。使用它的效果取决于该操作数放置在操作数之前还是之后。

#### 操作数前的一元加运算符

当一元加运算符放在操作数之前时，它会尝试将操作数的值转换为数字，然后执行语句的其余部分。这里有一个示例：

```javascript
let num1 = 2;
theresult = +num1;
```

在这种情况下，变量 `num1` 的初始值为 2。当代码将值赋值给变量 `theresult` 时，`num1` 的值保持不变（因为它已经是数字），然后赋值给变量 `theresult`，该变量获得值 2。

#### 操作数后的一元加运算符

如果你将一元加运算符放在操作数之后，它会在赋值后改变操作数的值。考虑这个示例：

```javascript
let num1 = 2;
theresult = num1+;
```

与上一个示例一样，`num1` 的初始值为 2。在下一行，一元加运算符用在操作数之后。这意味着代码将 `num1` 的当前值赋值给变量 `theresult`，在完成之后，它增加了 `num1` 的值。所以，只有在赋值完成后，你才得到了 `num1` 的新值。变量 `theresult` 被赋予值 2，然后 `num1` 变为 3。如果你在此之后使用 `num1`，它的值将是 3。

另一种查看一元加运算符在操作数之前和之后如何工作的方法是在你的浏览器中运行以下脚本。注意第一个警报中的值是什么，第二个警报中的值是什么。

```javascript
let num1 = 2;
result = +num1;
alert("num1 = " + num1 + " result = " + result);
num1 = 2;
result = +num1;
alert("num1 = " + num1 + " result = " + result);
```

在第一个警报中，你将看到 `num1=2 result=2`。因为在这里 `+` 运算符用在操作数之前，`num1` 的值没有变化并赋值给变量 `result`。在第二个警报中，你将看到 `num1=2 result=2`。

### 一元减运算符 (-)

一元减运算符是一元运算符，它将其唯一操作数的值取负。使用它的效果取决于该操作数放置在操作数之前还是之后。

#### 操作数前的一元减运算符

当一元减运算符放在操作数之前时，它会将操作数的值取负，然后执行语句的其余部分。这里有一个示例：

```javascript
let num1 = 2;
theresult = -num1;
```

在这种情况下，变量 `num1` 的初始值为 2。当代码将值赋值给变量 `theresult` 时，`num1` 的值被取负为 -2，然后赋值给变量 `theresult`，该变量获得值 -2。

### 赋值运算符 (=)

赋值运算符将其右侧的值赋值给其左侧的变量。例如，代码 `let num1 = 10 / 2;` 意味着将 10 除以 2 的结果赋值给 `num1`。

```javascript
let num1 = 10 / 2; // 两个数字相除
```

结果是 5，即 10 除以 2 的结果。

### 加赋值运算符 (+=)

`+=` 运算符将运算符右侧的值加到左侧变量上，并将该新值赋值给变量。从本质上说，它是此处所示代码的快捷方式：

```javascript
let money = 1000;
money = money + 1;
```

在这里，创建了变量 `money` 并赋值为 1000。随后代码通过赋值其自身加 1 的值来更改该值。赋值给 `money` 变量的值是 1001。

不需要多写一次变量名，可以使用加并赋值运算符来简化代码。以下代码与之前的示例得到相同的结果，并节省了少量打字量：

```javascript
let money = 1000;
money += 1;
```

使用加并赋值运算符，这段代码将 1（右侧）加到 `money`（左侧变量）上，将新值 1001 赋值给变量 `money`。

此运算符可用于添加任何值，而不是 1。例如，你可以在赋值中加 5，如下例所示：

```javascript
let money = 1000;
money += 5;
```

这一次，`money` 的最终值为 1005。

你甚至可以在右侧使用变量而不是普通值，如下例所示：

```javascript
let money = 1000;
let bonus = 300;
money += bonus;
```

在这里，`bonus` 的值为 300，它被加到变量 `money` 上，然后 `money` 被赋值结果 1300。这样，就可以更改 `bonus` 变量的值来影响赋值的结果。

该运算符的作用与算术运算符类似，同时也允许你拼接字符串。因此，你可以使用此运算符在字符串末尾添加：

```javascript
let myname = "Bob";
myname += "by";
```

此字符串在字符串 "Bob" 的末尾添加了 "by"，产生了字符串 "Bobby"。

### 减赋值运算符 (-=)

`-=` 的作用与 `+=` 类似，不同之处是从运算符左侧减去右侧的值。然后将其赋值给变量。以下是该运算符的运行示例：

```javascript
let money = 1000;
let bills = 800;
money -= bills;
```

此示例从 `money` 变量减去 `bills` 变量的值 (800)，并将结果赋值给 `money`。最后，`money` 的值为 200。

### 乘赋值运算符 (*=)

`*=` 运算符将运算符右侧的值乘以左侧的变量。然后将结果赋值给该变量。接下来的示例展示了该运算符的操作：

```javascript
let money = 1000;
let multby = 2;
money *= multby;
```

在这里，变量 `money` 乘以 `multby` 变量的值（即 2）。然后将结果 2000 赋值给变量 `money`。

### 除赋值运算符 (/=)

`/=` 将运算符左侧的变量除以右侧的值。然后将结果赋值给该变量。这是一个示例：

```javascript
let money = 1000;
let cutpayby = 2;
money /= cutpayby;
```

在此示例中，变量 `money` 除以变量 `cutpayby` 的值（即 2）。然后将结果 500 赋值给变量 `money`。

### 取模赋值运算符 (%=)

与其他执行操作的赋值运算符一样，`%=` 运算符对变量进行计算。它将左侧变量除以右侧，并将余数赋值给变量。

```javascript
let money = 1000;
let cutpayby = 2;
money %= cutpayby;
```

在这里，`cutpayby` 的值为 2，`money` 被除以 2，余数为 0，然后 `money` 被赋值结果 0。

### 幂赋值运算符 (**=)

此运算符将运算符左侧的变量进行右侧的幂，然后将该新值赋值给变量。

```javascript
let money = 1000;
let exponent = 2;
money **= exponent;
```

这一次，`money` 的最终值为 1000000。

### 位赋值

这些运算符执行各种位赋值操作：

| 位赋值 | `<<=`, `>>=`, `>>>=`, `&=`, `^=`, `|=` | 执行各种位赋值 |

### 等于运算符 (==)

`==` 运算符用于比较两个值是否相等。如果它们相等，则返回 `true`；否则返回 `false`。该运算符会执行类型转换，例如 `"4"==4` 这样的语句将返回 `true`；JavaScript 会将字符串 "4" 转换为数字。如果你希望该语句返回 `false`，你应该使用全等运算符（`===`），这将在本节稍后的部分讨论。

#### 特殊规则

由于该运算符会执行类型转换，因此有一些特殊规则：

- 如果一个操作数是数字而另一个是字符串，它将尝试在测试相等性之前将字符串转换为数字。
- 如果其中一个操作数是布尔值（Boolean），它将在测试相等性之前将其转换为数值。在这些情况下，`true` 被转换为 1，`false` 被转换为 0。
- 如果一个操作数是 `null` 而另一个是 `undefined`，比较将返回 `true`。
- 如果一个或两个操作数都是 `NaN`，比较将返回 `false`。

下表显示了使用等运算符的语句示例、返回值以及它们返回 `true` 或 `false` 的原因。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| `4 == 4` | true | 两个相等的数字 |
| `(4+2) == 6` | true | 两边的的结果都是 6，且 6 等于 6 |
| `"my socks" == "my socks"` | true | 字符串完全相同 |
| `1 == true` | true | 布尔值 true 被转换为 1 |
| `4 == 5` | false | 4 和 5 不相等 |
| `(4+3) == 4` | false | 左侧结果是 7，右侧结果是 4，它们不相等 |
| `"My socks" == "my socks"` | false | 字符串不完全相同（大小写问题） |
| `1 == false` | false | 布尔值 false 被转换为 0 |
| `true == "true"` | false | 布尔值 true 与字符串 "true" 不是同一种数据类型 |

你会注意到上表中的语句周围添加了括号，在稍后的一个表格中也是如此。在这里，它们主要用于提高可读性。你将在本章末尾学习更多关于括号和操作顺序的知识。

配合其他运算符，你可以将变量与比较运算符一起使用。如果变量的值相等，比较将返回 `true`。否则，它将返回 `false`。假设你声明了以下变量：

```javascript
let num1 = 2,
num2 = 5,
num3 = 5;
```

以下比较 `==` 将返回 `true`：

```javascript
num2 == num3
```

下一个比较将返回 `false`：

```javascript
num1 == num3
```

记住，等运算符（`==`）是用于比较的。小心不要误用赋值运算符（`=`）代替它，因为那将执行赋值而不是比较，并返回赋值的结果，所以你可能会得到一些意外的结果。

### 不等于运算符 (!=)

`!=` 运算符是 `==` 运算符的相反。`!=` 运算符不是在运算符两边的值相等时返回 `true`，而是在其两边的值*不相等*时返回 `true`。如果它发现运算符两边的值相等，该运算符将返回 `false` 值。

与 `==` 运算符一样，`!=` 运算符也存在类型转换，有一些特殊规则：

- 如果一个是数字而另一个是字符串，它将尝试在测试之前将字符串转换为数字。
- 如果一个是布尔值，那么它将在测试之前将其转换为数值（`true` 转换为 1，`false` 转换为 0）。
- 如果一个是 `null` 而另一个是 `undefined`，比较将返回 `false`。
- 如果一个或两个操作数是 `NaN`，比较将返回 `true`。

下表显示了一些使用 `!=` 运算符的语句示例、返回值以及它们返回 `true` 或 `false` 的原因。

| 比较 | 返回值 | 原因 |
|---|---|---|
| `4 != 3` | true | 4 和 3 不等的数字 |
| `"Cool" != "cool"` | true | 字符串的大小写不同，因此它们不相等 |
| `4 != 4` | false | 4 等于 4 |
| `"cool" != "cool"` | false | 字符串完全相同，因此它们相等 |

### 全等运算符 (===)

为了使 `===` 运算符返回 `true`，运算符两边的操作数必须相等且必须是相同的类型（不进行类型转换）。这意味着如果你使用如 `3 === "3"` 这样的语句，运算符将返回 `false`，因为左侧的值是数字而右侧的值是字符串。

下表显示了使用 `===` 运算符的语句示例。

| 比较 | 返回值 | 原因 |
| --- | --- | --- |
| `4 === 4` | true | 两个相等的数字 |
| `(4+2) === (3+3)` | true | 两边的结果都是 6，且两个值都是数字 |
| `"my socks" === "my socks"` | true | 两个值都是字符串，且它们完全相同 |
| `7 === "7"` | false | 数字和字符串类型不同 |



### 全不等于运算符 (`!==`)

为了使`!==`运算符返回`true`，运算符两边的值或语句必须不相等或不是相同的类型（不使用类型转换）。这意味着如果你使用如`3 !== "3"`这样的语句，运算符将返回`true`，因为左侧的值是数字而右侧的值是字符串。

下表显示了使用`!==`运算符的语句示例。

| 比较 | 返回值 | 原因 |
| --- | --- | --- |
| `4 !== 3` | `true` | 4 和 3 是不等的数字 |
| `"4" !== 4` | `true` | 两边的值不同且类型不同 |
| `4 !== 4` | `false` | 4 等于 4 |
| `"cool" !== "cool"` | `false` | 字符串完全相同，因此它们相等 |

### 大于运算符 (`>`)

使用大于运算符时，如果左侧的值大于右侧，它将返回`true`。使用了类型转换，因此有一些特殊规则：

- 如果两个操作数都是字符串，则按字符编码进行比较。
- 如果其中一个是数字，它将尝试将操作数转换为数字。
- 如果一个是布尔值，则它被转换为数字（`true`为 1，`false`为 0）。

剩余的比较运算符（`<=`）也使用相同的规则。

在字符串的情况下，JavaScript 检查字符串的字符；如果没有差异，它将检查下一个字符，直到找到差异或到达字符串末尾。要查找字符编码，可以使用 www.script.com/ref/character-codes.html。

下表显示了使用`>`运算符的一些示例。

| 比较 | 返回值 | 原因 |
| --- | --- | --- |
| `5 > 2` | `true` | 5 大于 2 |
| `true > 0` | `true` | 布尔值转换为 1 |
| `"a" > "A"` | `true` | `"a"`的字符编码为 97，`"A"`的字符编码为 65 |
| `"A" > "1"` | `true` | `"A"`的字符编码为 65，`"1"`的字符编码为 49 |
| `"10" < "2"` | `true` | `"1"`的字符编码为 49，`"2"`的字符编码为 50 |
| `5 > 7` | `false` | 5 小于 7，不大于 |
| `false > 0` | `false` | 布尔值`false`转换为 0 |
| `2 > 2` | `false` | 它们相等，所以左侧并不大于 |

### 小于运算符 (`<`)

小于运算符的工作方式与大于运算符相反。`<`不是在左侧的值大于时返回`true`，而是在运算符左侧的值小于运算符右侧的值时返回`true`。你可以通过查看下表看到`<`的示例。

| 比较 | 返回值 | 原因 |
| --- | --- | --- |
| `2 < 10` | `true` | 2 小于 10 |
| `"A" < "a"` | `true` | `"A"`的字符编码为 65，`"a"`的字符编码为 97 |
| `10 < 2` | `false` | 10 大于 2，不小于 |
| `"a" < "A"` | `false` | `"a"`的字符编码为 97，`"A"`的字符编码为 65 |

# 116 JavaScript：初学者指南

### 大于等于运算符 (`>=`)

`>=`运算符与你目前读过的比较运算符略有不同。该运算符为两侧的值相等增加了一个选项，使得比较结果为`true`。因此，若要返回`true`，运算符左侧的值必须大于或等于右侧的值。下表显示了一些使用`>=`运算符的语句示例。

| 比较 | 返回值 | 原因 |
| --- | --- | --- |
| `5 >= 2` | `true` | 5 大于 2 |
| `2 >= 2` | `true` | 2 等于 2 |
| `"a" >= "A"` | `true` | `"a"`的字符编码是 97，`"A"`的字符编码是 65 |
| `"A" >= "A"` | `true` | 字符编码大于 65 |
| `1 >= 2` | `false` | 1 小于 2 |
| `"A" >= "a"` | `false` | `"A"`的字符编码是 65，`"a"`的字符编码是 97 |

## 小于等于运算符 (`<=`)

与`>=`运算符一样，`<=`运算符也增加了两侧值相等的可能性。使用小于等于运算符，如果运算符左侧的值小于或等于运算符右侧的值，则返回值`true`。下表显示了使用`<=`运算符的语句示例。

| 比较 | 返回值 | 原因 |
| --- | --- | --- |
| `2 <= 5` | `true` | 2 小于 5 |
| `2 <= 2` | `true` | 2 等于 2 |
| `"A" <= "a"` | `true` | 大写字母小于小写字母 |
| `"A" <= "A"` | `true` | 字符串相等 |
| `5 <= 2` | `false` | 5 大于 2，不小于等于 |
| `"a" <= "A"` | `false` | 小写字母大于大写字母，不小于等于 |

当你在第 6 章学习条件语句和循环时，将获得一些使用比较运算符的机会。接下来是逻辑运算符，它们在检查条件时对你很有帮助。

### 理解逻辑运算符

三个逻辑运算符允许你比较两个条件语句，以查看其中一个或两个语句是否为`true`，并据此进行。如果你想一次检查一个条件并使用其结果，逻辑运算符将非常有用。与比较运算符一样，逻辑运算符返回`true`或`false`，取决于运算符两侧的值。

表 5-4 总结了逻辑运算符，将在后续章节中对其进行讨论。

### AND 运算符 (`&&`)

如果`&&`运算符两侧的比较均为`true`，则逻辑运算符`AND`返回`true`。如果一侧或两侧的比较为`false`，则返回值`false`。下表显示了`AND`运算符的一些语句。

| 语句 | 返回值 | 原因 |
| --- | --- | --- |
| `(1==1) && (2==2)` | `true` | 两侧的比较均为`true`：1 等于 1，2 等于 2 |
| `(2>1) && (3<4)` | `true` | 两侧的比较均为`true`：2 大于 1，3 小于 4 |
| `("A"<="A") && ("c"!="d")` | `true` | 两侧的比较均为`true`：`"A"`等于`"A"`，`"c"`不等于`"d"` |
| `(1==1) && (3==3)` | `false` | 右侧的比较为`false` |
| `("a"!="a") && ("b"!="q")` | `false` | 左侧的比较为`false` |
| `(2>7) && (5>=2)` | `false` | 两侧的比较均为`false` |

### OR 运算符 (`||`)

如果运算符一侧的比较返回`true`，则逻辑运算符`OR`返回`true`。因此，如果为`true`，只需一侧的语句之一求值为`true`即可。

| 运算符 | 符号 | 功能 |
| --- | --- | --- |
| AND | `&&` | 如果运算符两侧的语句均为`true`则返回`true` |
| OR | `||` | 如果运算符任一侧的语句为`true`则返回`true` |
| NOT | `!` | 如果运算符右侧的语句不是`true`则返回`true` |

表 5-4 逻辑运算符

要返回`false`，运算符两侧的比较必须都返回`false`。下表显示了一些使用`OR`运算符的比较示例。

| 语句 | 返回值 | 原因 |
| --- | --- | --- |
| `(2==2) || (3>5)` | `true` | 左侧的比较为`true` |
| `(5>17) || (4!=9)` | `true` | 右侧的比较为`true` |
| `(3==3) || (7<9)` | `true` | 两个比较均为`true` |
| `(4<3) || (2==1)` | `false` | 两个比较均为`false` |
| `(1!=3) || (4<=8)` | `false` | 两个比较均为`false` |

### NOT 运算符 (`!`)

逻辑运算符`NOT`可以用于单个比较，表示“如果情况不是如此，则返回`true`”。基本上，它可以让一个通常返回`false`的表达式返回`true`，或者让一个通常返回`true`的表达式返回`false`。

| 比较 | 返回值 | 原因 |
| --- | --- | --- |
| `!(1==1)` | `false` | 内部的比较为`true` |
| `!(2>1)` | `true` | 内部的比较为`false` |

### 位运算符

位运算符可以用于单个比较，表示“如果情况不是如此，则返回`true`”。基本上，它们在位级别上工作。下表显示了位运算符。

| 运算符 | 符号 | 功能 |
| --- | --- | --- |
| AND | `&` | 位与 |
| OR | `|` | 位或 |
| XOR | `^` | 位异或 |
| NOT | `~` | 取反 |
| 左移 | `<<` | 左移 |
| 有符号右移 | `>>` | 有符号右移 |
| 无符号右移 | `>>>` | 无符号右移 |

### 特殊运算符

有一些特殊的运算符在 JavaScript 中非常有用。下表显示了这些运算符。

| 运算符 | 符号 | 功能 |
| --- | --- | --- |
| 条件 | `? :` | 三元运算符/条件 |
| 逗号 | `,` | 逗号运算符 |
| 赋值 | `=` | 赋值运算符 |
| 删除 | `delete` | 删除运算符 |
| 检查 | `in` | 检查属性 |
| 实例 | `instanceof` | 检查实例 |
| 引用 | `as` | 别名 |
| 类型 | `typeof` | 检查类型 |
| 空 | `void` | 返回空 |

## 第 5 章：JavaScript 运算符 121

| 运算符类型 | 运算符示例 |
| --- | --- |
| 括号（优先级高于其他） | `()` |
| 一元运算符（数学、逻辑或位运算） | `++ -- ~ typeof void delete` |
| 乘、除、取模 | `* / %` |
| 加法、减法 | `+ -` |
| 移位（位运算） | `>>> <<` |
| 关系比较 | `> >= < <= instanceof` |
| 等于 | `== != === !==` |
| 与（位运算） | `&` |
| 异或（位运算） | `^` |
| 或（位运算） | `|` |
| 与（逻辑） | `&&` |
| 或（逻辑） | `||` |
| 条件（三元） | `? :` |
| 赋值 | `+= -= *= /= <= >= &= ^=` |
| 逗号 | `,` |

**表 5-6** 运算符优先级，从高到低

由于所有括号都在同一层级（没有嵌套），因此它们从左到右读取。

括号外的加法和减法运算符具有相同的优先级，它们也是从左到右读取。

JavaScript 运算符的优先级如表 5-6 所示，从最高优先级（先执行）到最低优先级（后执行）排序。

如你在表 5-6 中所示，括号的优先级高于其他运算符。当你不确定各种运算符的优先级，或者想让代码更具可读性时，括号非常有用。

## 尝试一下 5-2 判真还是假？

```
pr5_2.html
pr5_2.js
```

这个项目将允许你尝试一些比较运算符，看看它们是如何工作的。你将创建一个脚本，显示一个警告框，说明某个语句或比较将返回`true`还是`false`。脚本将使用条件/`else`语句，这将在下一章进行详细解释。

## 122 JavaScript：初学者指南

### 逐步步骤

1. 创建一个 HTML 文件并将其保存为`pr5_2.html`。
2. 创建一个外部 JavaScript 文件并将其保存为`prjs5_2.js`。使用此文件编辑第 3 至 13 步。
3. 将以下代码插入你的 JavaScript 文件中：

```javascript
let num1 = 0;
let num2 = 0;
if (num1 == num2) {
    window.alert("True");
} else {
    window.alert("False");
}
```

4. 在浏览器中打开 HTML 页面。你应该会立即看到一个显示“True”的警告框。
5. 将变量`num1`的值改为 5。重新保存 JavaScript 文件并刷新浏览器。你现在应该得到一个显示“False”的警告框。
6. 在接下来的代码行中，将`==`运算符更改为`>`运算符：

```javascript
if (num1 > num2)
```

7. 重新保存 JavaScript 文件并刷新浏览器。你现在应该再次得到`"True"`。
8. 将变量`num2`的值改为 7。
9. 重新保存 JavaScript 文件并刷新浏览器。你现在应该再次得到“False”。
10. 在下一行（你在第 4 步中更改过的）中，将运算符更改为`<`运算符：

```javascript
if (num1 < num2)
```

11. 重新保存 JavaScript 文件并刷新浏览器。你应该再次得到“True”。
12. 尝试更改`num1`变量的值，以便得到一个显示“False”的警告框。
13. 尝试使用其他比较运算符进行你自己的测试，看看结果如何。

### 尝试一下总结

在这个项目中，你能够利用对比较运算符的知识来创建一个警告框，根据比较语句返回`true`还是`false`来显示“True”或“False”。如果你愿意，你还可以对自己的值和运算符变体进行测试。

## 第 5 章自测

1. ________（运算符）是 JavaScript 中的一种符号或单词，用于对一个或多个值执行某种计算、比较或赋值。
2. ________ 运算符通常用于对两个值进行数学计算。
3. ________ 运算符将两个值相加。
4. 当递增运算符放在操作数 ________ 时，它会将操作数的值加 1，然后执行语句的其余部分。
5. 下面哪一个不是 JavaScript 运算符？
   - A. `=`
   - B. `===`
   - C. `&&`
   - D. `#$`
6. 赋值运算符的作用是什么？
   - A. 给变量分配一个新值
   - B. 给变量起一个新名字
   - C. 执行比较
   - D. 什么都不做，因为赋值运算符没有用
7. 加减 (`+=`) 运算符将运算符 ________ 边的值加到 ________ 边的变量上，然后将该值赋给变量。
8. 比较运算符的作用是什么？
   - A. 执行数学计算
   - B. 处理位，现在不重要
   - C. 比较两个值或语句，并返回`true`或`false`的值
   - D. 仅比较数字和字符串
9. 下面哪种比较将返回`true`？
   - A. `4 != 3`
   - B. `4 == 3`
   - C. `4 < 3`
   - D. `4 <= 3`
10. 下面哪种比较将返回`false`？
    - A. `4 != 3`
    - B. `4 == 3`
    - C. `4 < 3`
    - D. `4 <= 3`
11. ________ 运算符允许你对两个值进行逻辑判断。
12. 下面哪种比较将返回`true`？
    - A. `4 != 3`
    - B. `4 == 3`
    - C. `4 < 3`
    - D. `4 <= 3`
13. 下面哪种比较将返回`false`？
    - A. `4 != 3`
    - B. `4 == 3`
    - C. `4 < 3`
    - D. `4 <= 3`
14. ________ 是 JavaScript 中的一种。
15. ________ 运算符可以让你执行。

## 第 6 章：条件语句与循环 127

正如你所看到的，如果满足某些条件，你就可以执行。

## 第 6 章：条件语句与循环

## JavaScript：初学者指南

### 核心技巧

- 定义条件语句
- 使用条件语句

### 定义条件语句

### 什么是循环

- 使用循环

现在你了解了条件语句之后，是时候详细查看它们并学习如何编写代码了。你将学习 JavaScript 中的两种条件语句块：`if/else`语句和`switch`语句。你还将学习条件运算符的使用。

### 使用条件语句

在学习条件语句时，你会发现它们的语法非常相似。最需要注意的是包裹根据给定条件执行的代码部分的大括号 (`{}`)。

### 为什么条件语句很有用

正如你在上一节中看到的，条件语句可以非常有用。与其执行脚本中的每一行代码，你可以让脚本在满足特定条件时执行某些部分。你甚至可以将其扩展为需要满足的条件的组合。通过条件语句，你可以让 JavaScript 执行如下操作：

- 如果你的变量等于 John，在页面上写下 John。否则，在页面上写下 Unknown Server 并将其加粗。
- 如果汽车等于 Corvette 或 Mustang，向浏览器发送一个“酷的车”的警告框。
- 如果我的变量等于 Corvette，那么如果你的变量等于 Marty，向浏览器发送一个警告框“Marty 很酷且开着车”。否则，发送一个警告框显示“Unknown Server 开着某种类型的车”。

我不开 Corvette 或 Mustang，所以这把我排除在外了；但这些示例展示了你如何通过添加检查条件来让脚本更有用。这些语句为脚本提供了所谓的“流程控制”。

### 使用条件语句

现在你已经知道什么是条件语句，是时候详细查看它们并学习如何编写代码了。你将学习 JavaScript 中两种类型的条件语句块：`if/else`语句和`switch`语句。你还将学习条件运算符的使用。

### if/else 语句结构

在处理`if/else`语句时，首先处理的是第一行，它告诉浏览器继续还是移动。你用 JavaScript 关键字`if`开始`if/else`语句，后面跟着括号内的比较。

## JavaScript：初学者指南

你将此处的文本比较替换为实际的比较。要做到这一点，你需要记住上一章中的比较运算符。假设你想检查一个名为`boats`的变量是否等于 3，如果条件为真，则发送一个名为“Yes, there are 3 boats”的警告。你可以使用以下代码：

```javascript
if (boats === 3) {
  window.alert("Yes, there are 3 boats");
}
```

记住，比较将返回`true`或`false`的值。这就是返回值变得有用的地方。如果比较返回`true`，则大括号内的代码将被执行。如果返回`false`，则大括号内的代码将被忽略。

如果你想使用`else`块在比较返回`false`时执行一组语句，请在下方代码的下一行使用`else`关键字，并紧跟它自己的一组大括号：

```javascript
if (boats === 3) {
  window.alert("You have the right number of boats");
} else {
  window.alert("You do not have the right number of boats");
}
```

> 如果第一行的比较返回`true`，则执行此警告。

如果变量`boats`等于 3，这段代码将发送一个“You have the right number of boats”的警告。如果不是，它将发送一个“You do not have the right number of boats”的警告。

现在你已经设置好了语句，你需要知道比较是否返回`true`，以便你能够确定执行的是哪块代码。要做到这一点，你需要在比较发生之前声明变量并为其赋值一个值。这将为你提供确定脚本中发生什么情况的值。如果你使用以下代码，可以猜出执行的是哪块代码（第一个还是第二个）吗：

```javascript
let boats = 3;
if (boats === 3) {
  window.alert("You have the right number of boats");
} else {
  window.alert("You do not have the right number of boats");
}
```

如果你猜到是执行第一个代码块，那么你猜对了！变量`boats`等于 3，比较`boats===3`结果为`true`。如果它返回`true`，则执行第一个代码块，`else`关键字之后的代码块被忽略。你会收到显示“You have the right number of boats”的警告，不再有其他的。

> 如果第一行的比较返回`false`，则执行此警告。

## 第 6 章：条件语句与循环 129

### 注意

在输入变量赋值 (`=`)、相等比较 (`==`) 和严格相等比较 (`===`) 时要小心，因为它们很容易无意中写错，并导致你的脚本出现问题或产生意想不到的结果。

现在来看一下如何设置语句以获得相反的结果。以下代码将导致函数返回`false`：

```javascript
let boats = 0; // 给变量赋值 0 将
if (boats === 3) { // 导致函数返回 false
  window.alert("You have the right number of boats");
} else {
  window.alert("You do not have the right number of boats");
}
```

由于变量`boats`的值为 0，比较`boats === 3`将返回`false`；因此，第一个代码块被忽略，`else`语句之后的代码块被执行。这一次你收到了显示“You do not have the right number of boats”的警告，而第一个块被忽略了。

现在你已经知道了`if/else`语句块的基本结构，就可以学习将一个块嵌套在另一个块之中的技巧了。

注意 JavaScript 会忽略未引号的空白。例如，你可以这样写：

```javascript
if (boats === 3) { window.alert("You have the right number of boats"); } else { window.alert("You do not have the right number of boats"); }
```

尽管你会遇到这样编写的代码，但并不是因为你想让以后维护这段代码的程序员（也就是未来的你！）易读它！

### 块嵌套

如果你进行嵌套，你基本上是将一个结构放在另一个相同或相似的结构内部。在`if/else`语句块中，你可以在比较之后的第一个块（“if 块”）内，或者在`else`关键字之后的第二个块（“else 块”）内，嵌套其他的`if/else`语句。

例如，你可能想让浏览器执行如下语句：“如果变量`cookbook`等于 yes，且名为`meatloafprice`的变量也等于 yes，则向浏览器发送一个显示‘Recipe found’的警告。如果`cookbook`不等于 yes，则向查看者发送一个显示‘You have the book but no recipe’的警告；否则，向浏览器发送一个显示‘You need a cookbook’的警告。”

这是一个相当长且复杂的语句，但你可以通过在另一个`if/else`语句块中嵌套一个`if/else`语句来实现你的目标。

## 130 JavaScript：初学者指南

为了看到它是如何工作的，考虑以下示例，它将之前的语句转换为 JavaScript 形式：

```javascript
let cookbook = "yes";
meatloafrecipe = "no";
if (cookbook === "yes") {
  if (meatloafrecipe === "yes") {
    window.alert("Recipe found");
  }
  else {
    window.alert("The book has no recipe");
  }
} else {
  window.alert("You need a cookbook");
}
```

## 132 JavaScript：初学者指南

```javascript
if (haveweess === "yes") {
    window.alert("Find the recipe on the Web");
} else {
    window.alert("You need a cookbook");
}
```

现在`if`块中的`if`块中又有一个`if/else`块。如你所见，添加了另一个变量`ismomsmeat`来检查是否有更具体的食谱。你可以一直这样下去，直到你无法忍受；然而，这已经足够让你在需要时在此基础上进行构建。

另一个需要注意的点是，如果你使用已经是布尔（Boolean）的值作为比较值，你只需要使用该值进行比较即可。如下代码所示：

```javascript
let havecookbook = true;
if (havecookbook) {
    window.alert("Recipe found");
} else {
    window.alert("Recipe not found");
}
```

虽然你可以直接写`if (havecookbook === true)`进行比较，但如果该值已经是布尔值（如本所示），就不需要再使用该值。在这里，你可以使用快捷方式`if (havecookbook)`来缩短代码。

## 复杂比较

除了像`x === 2`或`y < 3`这样的简单比较外，你还可以使用第 5 章讨论过的逻辑运算符来构建复杂的比较。你可能还记得，那一章以类似于下面示例的形式展示了其中一些比较：

```javascript
2==2 || 3<5
```

在第 5 章中，唯一关注点是比较会返回`true`还是`false`，而不是如何将其添加到`if/else`语句中。注意每个比较式周围的括号。它们主要是为了组织结构；但考虑到运算顺序，你可以这样写这个比较：

```javascript
2==2 || 3<5
```

这里的问题是这种写法很难读，因此如果你需要调试代码，将很难判断代码是否存在问题。

回想一下，`if/else`语句的第一行使用括号来括起比较。如果你在不使用组织括号的情况下编写复杂的比较（如上一个示例所示），你的第一行看起来就会像这里显示的直接代码一样：

```javascript
if (2==2 || 3<5)
```

## 第 6 章：条件语句与循环 133

虽然这很容易输入，但它很难读，因为你不确定它应该被读作“如果 2 等于 3 或小于 5”，还是“如果 (2 等于 2) 或者 (3 小于 5)”。

你可以做的第一件事是添加间距，这有助于提高比较的可读性：

```javascript
if (2 === 2 || 3 < 5)
```

如果你为了组织而加上括号，它会变得更容易读；但你必须小心正确地嵌套。下面的示例代码展示了为了组织而添加的括号：

```javascript
if ( (2 === 2) || (3 < 5) )
```

使用哪种形式取决于个人喜好。目前，本章使用带有额外括号进行组织的方法。这应该能让你阅读书中的代码时变得更轻松。

现在，你可以创建允许包含更多值或允许特定值范围返回`true`的脚本。假设你想在变量名为`num1`大于 2 但小于 11 时显示一个警告框，并且当`num1`不在你的范围内时显示另一个警告框。你可以使用以下代码：

```javascript
if ( num1 > 2 ) && (num1 < 11 ) {
  window.alert("Cool number");
} else {
  window.alert("Not a cool number");
}
```

> 这种复杂比较允许特定范围的值返回 true

你的比较是在说：“如果`num1`大于 2 且`num1`小于 11。”如果该比较返回`true`，你就会看到“Cool number”警告框。如果它返回`false`，你则会得到“Not a cool number”警告框。

当然，你可以把比较行写得随你想要复杂。你可以在一行中添加`and`或`or`逻辑运算符，直到你得到需要的……或者精神崩溃。下面的示例为比较添加了额外的条件，以检查`num1`是否等于 20：

```javascript
if ( num1 > 2 ) && (num1 < 11 ) || (num1 === 20 ) {
  window.alert("Cool number");
} else {
  window.alert("Not a cool number");
}
```

> 这种复杂比较添加了一个额外的数字，会导致比较返回 true

现在，比较允许大于 2 的数字、小于 11 的数字以及数字 20 给出“Cool number”警告框。比较读作：“如果`num1`大于 2 且`num1`小于 11 或者`num1`等于 20。”你可以继续添加信息来创建更多返回`true`的数字，甚至是更多返回`true`的额外范围。

## 134 JavaScript：初学者指南

当然，为了看到前面的代码生效，你需要声明`num1`变量并给它赋值。如果你能判断出当代码如下所示，会显示哪个警告框：

```javascript
num1 = 1;
if ((num1 > 2) && (num1 < 11) || (num1 == 20)) {
  window.alert("Cool number");
} else {
  window.alert("Not a cool number");
}
```

### 块作用域

`let`关键字的引入（在第 3 章中）允许值在 JavaScript 中具有块作用域。传统的`var`关键字具有函数作用域，这意味着它在函数

## JavaScript：初学者指南

变量的作用取决于声明它的整个函数，无论它是否在块中声明。

以下代码展示了这样一个示例：

```javascript
function isLuckyNumber(number) {
  if (number === 7) {
    var message = "That is a lucky number!";
    console.log(message);
  }
}
isLuckyNumber(7);
```

在这里，`message`的值在`if`外部仍然可用，并且会显示消息（如果发送了其他数字，如果块被跳过，它将是 undefined）。另一方面，使用`let`关键字会导致`if`语句中的值被定义为`undefined`，即使条件结果为真。例如，看以下代码：

```javascript
function isLuckyNumber(number) {
  if (number === 7) {
    let message = "That is a lucky number!";
    console.log(message);
  }
}
isLuckyNumber(7);
```

这一次，控制台将打印出`message`是未定义的错误信息。由于`let`关键字将值限制在语句的块作用域内，因此它在外部没有定义。

如果你需要将变量的使用限制在特定的块中，块作用域会很有用。在这种情况下，变量具有函数作用域更有用，因此你可以将声明移动到函数的顶部，使得变量的作用域是函数而不仅仅是`if`语句，如下所示：

```javascript
function isLuckyNumber(number) {
  let message = "That number is not lucky. Sorry!";
  if (number === 7) {
    message = "That is a lucky number!";
  }
  console.log(message);
}
isLuckyNumber(7);
```

在这里，使用`let`关键字将`message`变量的作用域限制函数块。它还提供了一个默认值。如果发送的数字导致比较返回`false`，则会在控制台中显示此默认消息。如果比较返回`true`，`message`的值将变为 "That is a lucky number!" 并显示在控制台中。

## 第 6 章：条件语句与循环

注意，即使你想使用函数作用域，仍然最好使用`let`而不是`var`。通过这样做，你确定`let`始终属于包含它的块。如果你使用`var`，它将仅限于函数作用域，即使它在块内部使用，如果你打算在任何地方使用函数作用域以外的块作用域，这会让代码不够清晰。

## 使用 switch 语句

`switch`语句允许你获取一个表达式，并根据`case`是否等于表达式的值执行不同的代码块。如果你想检查多个不同的值，这种方法比使用链式`if/else`语句要简单得多。

`switch`语句的第一行具有以下语法：

```javascript
switch (expression)
```

你可以将`expression`替换为值、变量或其他类型的表达式（例如，数值的相加或字符串的拼接）。对于第一个示例，你将使用在`switch`语句开始之前已赋值的变量。

现在你需要查看`switch`语句的通用语法。以下代码是`switch`语句如何工作的示例：

```javascript
let thename = "Fred"; // switch 语句基于
switch (thename) { // thename 变量的值
    case "George": // 给出一个 case 并带代码
        window.alert("George is an OK name"); // 如果为真则执行它
        break;
    case "Fred":
        window.alert("Fred is the coolest name!"); // 这是真的
        window.alert("Hi there, Fred!"); // 的 case 并且会被执行
        break;
    default:
        window.alert("Interesting name you have there"); // 当任何 case
                                             // 为真时
                                             // 使用默认值
} // 闭括号关闭 switch 语句
```

首先，这声明并赋值了一个变量`thename`；它的值被赋予 Fred。接下来，`switch`语句使用变量`thename`作为比较的基础。然后用大括号打开块，后面是第一个`case`语句。这样写的意思是：“如果 thaname 等于 George，则执行冒号后面的命令。”如果 thaname 等于 George，你将得到一个警报。

接下来你使用`break`语句，它告诉浏览器执行代码并移动到块后的下一行代码。在`switch`块中使用`break`语句是为了确保只执行一个`case`部分；否则你将面临执行返回`true`的那个之后`case`的风险，因为默认情况下，浏览器将继续执行下一条语句（称为“穿透”），而不是退出块，即使它发现某个`case`为真。为了确保浏览器退出块，添加了`break`语句。

## JavaScript：初学者指南

回到脚本，你会发现`thename`不等于 George，所以跳过了这个`case`；然而，下一个比较返回了`true`，因为在脚本中`thename`等于 Fred。因此，该`case`块中的语句集将被执行。注意在`break`语句之前出现了两行 JavaScript 代码。这表明你可以在`case`内部包含任意数量的行。

最后，你看到了`default`关键字。它用于在没有任何`case`返回`true`的情况下。如果发生这种情况，将执行代码的默认部分。

### 穿透 (Falling Through)

有时你需要用同一段代码处理多个情况。这被称为“穿透”。你可以通过不在`case`之间使用`break`语句来实现。例如：

```javascript
switch (name) {
  case "George":
  case "Fred":
    window.alert("You have nice name!");
    break;
}
```

如果 name 是 "George" 或 "Fred"，警报将会显示。然而，如果你忘记了`break`语句，无论条件是否匹配，代码都会继续执行。

另一种使用穿透的方法是检查值的范围：

```javascript
switch (day) {
  case 1:
  case 2:
  case 3:
    window.alert("It's early week");
    break;
  case 4:
  case 5:
    window.alert("It's late week");
    break;
  case 6:
  case 7:
    window.alert("It's the weekend");
  break;
}
```

## 第 6 章：条件语句与循环

### 使用表达式

目前为止，你使用的是变量值作为表达式。JavaScript 允许使用任何类型的表达式，这在在使用布尔值时非常有用。例如，考虑以下内容：

```javascript
let num1 = 17;
switch (true) {
  case (num1 < 20) :
    window.alert("The number is less than 20");
    break;
  case (num1 >= 20) && (num1 <= 100) :
    window.alert("The number is somewhere between 20 and 100");
    break;
  default:
    window.alert("The number is negative or more than 100");
}
```

通过将布尔值`true`作为表达式，每个`case`都可以是一个条件。如果某个`case`返回，则存在匹配并执行。

### 使用条件运算符

条件运算符（也称为三元运算符）可以作为根据条件赋值的快捷方式。例如，你可能决定根据条件语句的结果为变量赋值。你可以通过以下代码实现：

```javascript
let mynum = 1,
  mymessage = "";
if (mynum === 1) {
  mymessage = "You win!";
} else {
  mymessage = "Sorry! Try again!";
}
```

### 注意

你可以使用`if/else`代替`switch`语句完成任何操作，但有时`switch`更加方便且易读。

## JavaScript：初学者指南

它允许你在问号（?）之前放置一个条件，并在冒号（:）的每一侧放置一个可能的值，如下所示：

```javascript
let name = (condition) ? value1 : value2;
```

JavaScript 会评估该条件语句，如果语句返回`true`，则冒号左侧的值（此处为`value1`）被赋值给变量。如果语句返回`false`，则冒号右侧的值（`value2`）被赋值给变量。如你所见，该运算符操作三个操作数（条件和两个值），为什么它有时被称为**三元运算符**呢。

应用于上一个示例，我们可以重写整段代码如下：

```javascript
let mynum = 1,
mymessage = ""
mymessage = (mynum == 1) ? "You win!" : "Sorry! Try Again";
```

这种工作方式与`if/else`块相同，但允许你用更少的字数编写代码（减小了代码表的大小）。

### 注意

从技术上讲，条件运算符可以嵌套，但不建议这样做，因为嵌套的条件运算符会导致代码迅速变得晦涩且更难以调试。如果你需要更复杂的逻辑，通常使用`if/else`结构更好，这样任何嵌套都能更容易地看到。

在本章中你学到的条件语句将让你在已经了解了如何使用它们后，对代码实现很多功能。你将在后面的章节中大量地使用这些内容来创建更复杂的脚本。

# 从提示获取用户输入

从观众获取输入的一种方法是使用`window.prompt()`方法。该方法接受两个参数：要显示的提示文本以及用于观众回复的文本框的默认值。例如，你可以使用以下代码。

```javascript
let username = window.prompt("Give me your name!", "");
```

在这种情况下，提示文本将是 "Give me your name!"，文本框的默认值将为空。下面的插图显示了提示框在 Mozilla Firefox 中运行时的样子。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_158_0.png)

## 第 6 章：条件语句与循环 141

如果用户点击 OK 或按下回车键，`window.prompt()`会返回文本框的内容。如果点击了取消按钮或以其他方式关闭了提示，返回的值将是`null`。如果使用了变量，返回的值将赋值给`window.prompt()`方法的对象。在这种情况下，返回的值将存储在`username`变量中。

为了利用这一点，假设你想在页面上显示观众的名字以进行个性化处理。如果输入了观众的名字，则显示该名字；如果在没有输入或用户以某种方式取消/关闭提示时，则显示默认消息。以下代码显示了如何实现这一点：

```javascript
let username = window.prompt("Give me my name", "");
if (username == null || username == "") {
  document.write("Hello, Random Nameless Person!");
} else {
  document.write("Hello, " + username + "!");
}
```

返回的值存储在`username`变量中。使用`if`语句检查该变量的值。如果`username`的值为`null`或空字符串，则页面显示 "Hello, Random Nameless Person!" 消息。否则，观众将收到他/她输入的名称问候。图 6-1 显示了在提示框中输入 "Brent" 的结果。

如你所见，`if/else`条件语句允许你对用户输入进行一些测试。这防止了你显示`null`或空字符串作为观众名称的出现。从技术上讲，用户仍然可以输入空格，但你可以通过在条件语句中使用正则表达式来防止此发生。正则表达式将在第 13 章中详细介绍。

| Firefox | |
| --- | --- |
| JavaScript 示例 | + |
| file:///F:/javascript/figs/06_01.html | |
| Hello, Brent! | |

**图 6-1** 向观众显示问候信息。

### 专家问答

**问：** 我需要在每个`if/else`块中都使用大括号吗？我在 Web 上的代码中看到过没有大括号的使用。为什么？

**答：** 如果你只需要在块和`else`块中执行单个 JavaScript 语句，有一种快捷方法可以让你省略大括号（本章的“大括号快捷方法”部分），这可以用于 Web 上的自由脚本。正如之前解释的，不建议使用这种技术，因为当你在查看或调试代码时可能会引起困惑。

**问：** 如果我能做的只是给变量赋值并测试它，我为什么要费劲用条件语句？如果我已经知道变量的值了，为什么它是条件的？

**答：** 在下一节中，你将进入从观众那里获取信息的阶段。这取决于观众（例如，如果观众需要在文本框或提示中输入他/她的名字），这使得条件块变得更有用，因为你可以为一个观众执行一个操作，为另一个用户执行另一个任务。有了用户输入，你无法预先知道变量的值，你需要使用条件块来处理各种可能性。此外，你会记得函数可以作为参数传递值，你可能在执行某些部分之前需要用条件语句进行测试。

**问：** 我需要使用`switch`语句吗？

**答：** 虽然不是绝对需要使用它们（你可以用`if/else`语句代替），但学习它们是一个好主意，因为它们可以帮助节省时间并优化代码。

**问：** 我尝试在提示框中输入数字，但它却在进行加法。为什么？

**答：** 输入提示框的数据是字符串，无论输入的是什么类型的数据。可以使用一元加号运算符（参见第 5 章）将字符串强制转换为数值：

```javascript
let num1 = window.prompt("Enter a number,");
num1 = +num1;
```

如果经过转换，它将变成数值，加法将如预期进行。你将在第 13 章学习更多关于验证的内容。

# 第 6 章：条件语句与循环 143

# 尝试这个

```
pr6_1.html
prjs_1.js
```

这个项目将帮助你学习`window.prompt()`方法、嵌套的`if/else`语句以及`switch`语句。假设你刚开始一家销售产品的在线商店。由于预算有限，只能向某些城市配送。你想提示城市名称并显示是否可以配送。

### 步骤

1. 创建一个 HTML 页面并保存为`pr6_1.html`。添加 script 标签指向名为`pr6_1.js`的外部 JavaScript 文件。
2. 创建一个外部 JavaScript 文件并保存为`prjs_1.js`。第 3-6 步使用此文件。
3. 创建一个变量`msg`，初始值为空字符串 (`""`)。这将用于存储显示给观众的消息。
4. 创建一个变量`city`，并将提示“你的城市名称是什么？”的返回值赋值给它。
5. 如果`city`的值为`null`或空字符串 (`""`)，则将赋值 "No city entered. Cannot deliver availability,"。否则（else），创建一个`switch`语句（这将嵌套在`else`块中）。
6. 在`switch`语句中，根据城市名称为`msg`赋值以下值：
   - 如果城市是 "Johnston”，“我们可以在 3 天内向您送货。”
   - 如果城市是 "Donville”，“我们可以在一周内向您送货。”
   - 如果城市是 "Danieltown" 或 "Martyville”，“我们可以在两周内向您送货。”
   - 如果是其他城市，“抱歉！我们不向您的城市配送。”
7. 将`msg`变量的值写在页面上。
8. 完成后，你的 JavaScript 文件应具有以下代码（也有其他解决方案）：

```javascript
let msg = ""
  city = window.prompt("What is the name of your city?", "");
if (city === null) || (city === "") {
  msg = "No city entered. Cannot deliver delivery availability."
}
else {
  switch (city) {
    case "Johnston":
      msg = "We can have items delivered to you in 3 days."
      break;
    case "Donville":
  }
}
```

### JavaScript: 入学者指南

```javascript
msg = "We can have items delivered to you in 1 week.";
// ...
break;
case "Danieltown": // fall through
case "Martyville":
  msg = "We can have items delivered to you in 2 weeks.";
  break;
default:
  msg = "Sorry! We do not deliver to your city yet.";
}
document.write(msg);
```

9. 保存 JavaScript 文件和 HTML 文件，并在浏览器中查看 HTML 页面。
10. 尝试输入一个命名的城市。你应该会在页面上看到相应的提示。你可以刷新页面以尝试不同的城市名称。

### 练习总结

在这个项目中，你运用了`window.prompt()`方法、`if/else`语句和`switch`语句的新技能，创建了一个脚本，允许用户输入城市名称，然后查看该城市是否提供服务。

### 定义循环

在开始使用循环之前，你需要了解什么是循环、它们能做什么，以及为什么它们对你的脚本很有用处。

### 什么是循环？

循环是一个代码块，允许你按照指定的次数重复某部分代码，并可能在每次执行代码时更改变量的值。通过这种方式，你可以将某些任务缩短为几行代码，而不必在脚本中反复编写相同的行，从而累了手指。

# 为什么循环很有用？

循环之所以有用，是因为它们允许你在无需重新输入或在文本编辑器中使用剪切和粘贴的情况下，重复代码行。这不仅节省了你重复输入相同代码行的时间和麻烦，还避免了重复循环中出现输入错误。你可以在浏览器每次通过循环时更改一个或多个变量的值，这为你节省了编写与前一行代码略有不同的代码行的时间和麻烦。

## 第 6 章：条件语句与循环 145

作为一个简单的例子，假设你想用 JavaScript 在 Web 页面上连续写入十次某个句子。要实现这一点，你可能需要编写如下所示的代码：

```javascript
document.write("All this typing gets tiring after a while!<br>");
document.write("All this typing gets tiring after a while!<br>");
document.write("All this typing gets tiring after a while!<br>");
document.write("All this typing gets tiring after a while!<br>");
document.write("All this typing gets tiring after a while!<br>");
document.write("All this typing gets tiring after a while!<br>");
document.write("All this typing gets tiring after a while!<br>");
document.write("All this typing gets tiring after a while!<br>");
```

哎！剪切粘贴可以使任务变得简单，但仍然会很枯燥，尤其是当你决定改写 50 次时。使用循环，你只需要写一次，并调整你想要的执行次数即可。它看起来像下面的示例。这不是实际代码，但当你以后下一节“使用循环”更详细地查看循环结构时，你会看到实际代码需要重复多次语句。

```javascript
Do this block 10 times {
  document.write("I only have to type this once!<br>");
}
```

当然，你将把“执行此块 10 次”文本替换为 JavaScript 能理解的实际语句。你将在下一节中看到可以使用哪些语句来构建循环。

### 使用循环

为了了解循环如何对你有帮助，你需要查看 JavaScript 中可以使用的不同循环结构。本节涵盖的循环结构包括 `for`、`while` 和 `do` 循环。

### for

在 JavaScript 中使用循环，你需要知道如何编写循环的基本结构，以及如何将循环嵌套在另一个循环中。首先，查看循环的基本结构。

# for 循环的结构

`for`循环的结构与条件块非常相似。主要的区别在于循环有不同的用途，且第一行是不同的。之后，你使用熟悉的大括号`{}`来包含循环的内容。

循环的第一行类似于下面这一行：

```javascript
for (let count = 1; count < 11; count++)
```

你首先看到的是这个词，后面跟着一组包含三个语句的括号。这三条语句通过提供特殊信息来告诉它应该重复的次数。

第一条语句（`let count = 1`）创建一个名为`count`的变量并给其分配初始值 1。这个初始值可以是任何数字。这个数字被用作循环重复次数的起点。使用数字 1 将帮助你更容易地看到循环重复的次数。前面的代码以`count`值为 1 开始循环。注意，如果`count`变量已经在脚本中初始化，则就不需要`let`关键字了。

下一条语句（`count < 11`）告诉循环停止运行。循环将根据这个条件语句停止。该条件的作用是：只有当你每次循环时给`count`的值加 1 时才停止，循环的最后一次是在`count`等于 10 时。当它是 10 时，它变为 11；这不通过条件测试，因此循环停止。

组中的最后一条语句（`count++`）决定了变量变化的速率。在前面的代码中，你每次循环时给变量加 1，循环的最后一次是在`count`等于 10 时。

要完成循环，你使用大括号包裹代码。`for`循环的示例所示：

```javascript
for (let count = 1; count < 11; count++) {
  // 代码写在这里
}
```

现在你已经学会了基础循环，准备好向其中添加内容了。在循环内部，你可以使用`count`变量的值（或使用的任何变量）来执行各种事情。

你可以做的一件事（当你学习数组时这一点会变得更加明显）是利用变量每次都在变化的这一事实。通过每次循环增加 1，你可以使用循环对句子从 1 到 10 编号，使行更具可读性。以下代码实现了这一点：

```javascript
document.write("Get ready for some repeated text.<br>");
for (let count = 1; count < 11; count++) {
  document.write(count + ". I am part of a loop!<br>");
}
```

## 148 JavaScript：初学者指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_166_0.png)

图 6-2 循环显示了十次该文本。

在前面的代码中，你刚刚在开始处将`count`变量的值添加到了字符串中。句子前的句号会让每行文本在数字后面出现一个句号、一个空格以及你的句子。图 6-3 显示了添加此内容后脚本在浏览器中的显示效果。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_166_1.png)

图 6-3 重复的行从 1 到 10 编号。

# 第 6 章：条件语句和循环 149

### 比较

在进行比较时，你不局限于`<`运算符。例如，到目前为止你已经循环了十次。有许多方法可以使循环执行十次，尽管某些方法会改变`count`变量的值（当你不想用 1–10 作为计数数字时，这非常有用）。这里显示了一些示例：

```javascript
for (let count = 1; count <= 10; count++) {
for (let count = 0; count < 10; count++) {
for (let count = 6; count < 15; count++) {
for (let count = 10; count > 0; count--) {
for (let count = 5; count <= 50; count++) {
```

- `count`从 1 到 10（注意使用的是`<=`而不是`<`）
- `count`从 0 到 9
- `count`从 6 到 15
- `count`从 10 到 1（注意使用了`>`和`--`）
- `count`从 5 到 30，每次递增 5

请记住这一点，因为这种灵活性可以帮助你根据`count`变量节省时间或额外的计算。例如，示例中显示的第二方法通常用于数组。你将在第 7 章中学习更多关于此的内容。

另一个需要注意的是，缩进和比较值也可以是变量值，如下代码所示：

```javascript
let startnum = 1;
let endnum = 10;
for (let count = startnum; count <= endnum; count++) {
// 代码...
}
```

> `startnum`和`endnum`的值用于初始化`count`并与`count`的值比较。

### 块嵌套

是的，你现在必须处理嵌套循环。就像`if/else`块一样，你可以计算你能处理的任意层级。目前，你只需要在一个循环内嵌套另一个循环。下面的示例显示了`for`循环中的`for`循环：

```javascript
for (let count = 1; count < 11; count++) {
document.write(count + " - I am part of a loop!");
for (let nestedcount = 1; nestedcount < 3; nestedcount++) {
document.write("I keep interrupting in pairs!");
}
}
```

> 这个嵌套循环中断了外部循环

### 注意

在嵌套循环时要小心，确保每个嵌套循环的第一行都有自己的`count`，例如`for (count = 1; count < 11; count++)`。在大多数情况下，计数器需要对其自己的循环是唯一的。此外，如果没有正确包含或配对括号，可能会发生错误。

## 150 JavaScript：初学者指南

现在你有一个带有自己的文本中断外部循环的循环。每当你通过循环时，你都会写出“I am part of a loop!”这一行。然后你会遇到另一个循环，它会在屏幕上写入“I keep interrupting in pairs!”。

内部循环被设置为重复两次；每当你从外部循环有一个句子时，后面会紧跟两个内部循环的句子。为了更清楚地看到这一点，请考虑以下示例，它更新了你之前在`loop01.js`文件使用的代码：

```javascript
document.write("ready for repeated text.<br>");
for (let count = 1; count < 11; count++) {
  document.write(" I am part of a loop!<br>");
  for (let nestcount = 1; nestcount < 3; nestcount++) {
    document.write("I keep interrupting in pairs!<br>");
  }
}
document.write("Now we are back to the plain text.");
```

图 6-4 说明了这些嵌套循环如何影响浏览器中页面的外观。你现在可以看到，如果需要，嵌套循环对于在过程中添加更多信息是很有用的。

在何种嵌套循环时，你可以在内部循环中使用外部循环的`count`值，但反之则不行。例如，看以下代码：

```javascript
for (let count = 1; count < 11; count++) {
  document.write(`The main count is ${count}`);
  document.write(`The nest count is ${nestcount}`);
  for (let nestcount = 1; nestcount < 3; nestcount++) {
    document.write(`The main count is ${count}`);
    document.write(`The nest count is ${nestcount}`);
  }
}
```

如你所见，`count`值在外部循环中是可用的，而在内部循环中不可。内部循环的`count`和`nestcount`都可以使用。在使用嵌套循环时记住这一点可能会在过程中让你遇到一些头疼！更复杂的是，你还可以将不同类型的块嵌套在另一个内部。例如，你可以在循环内部放置`if/else`语句，或者在`if/else`语句内部放置循环。下面的示例在循环中创建了一个`if/else`块：

```javascript
for (let count = 1; count < 11; count++) {
  if (count === 5) {
    document.write("The loop is halfway done!<br>");
  }
}
```

# 第 6 章：条件语句和循环 151

```javascript
else {
  document.write("I am part of a loop!<br>");
}
}
```

在这种情况下，浏览器将检查`count`变量的值是否为 5。如果是，浏览器将在屏幕上打印与之前不同的消息：

| Firefox | 示例 |
| :--- | :--- |
| file:///script/06_03.html | 准备好重复文本 |
| 1. I am part of a loop! | 循环循环 |
| 2. I am part of a loop! | 循环循环 |
| 3. I am part of a loop! | 循环循环 |
| 4. I am part of a loop! | 循环循环 |
| 5. The loop is halfway done! | 循环了一半 |
| 6. I am part of a loop! | 循环循环 |
| 7. I am part of a loop! | 循环循环 |
| 8. I am part of a loop! | 循环循环 |
| 9. I am part of a loop! | 循环循环 |
| 10. I am part of a loop! | 循环循环 |
| Now we are back to the plain text. | 现在我们回到了普通文本 |

152 JavaScript：初学者指南

### 无限循环

当你编写循环时，如果循环条件永远为真，就会导致无限循环。这会导致崩溃

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_170_0.png)

图 6-5 嵌套 if/else 块

153 JavaScript：初学者指南

为了避免无限循环，你需要确保循环条件最终会为假。例如，以下代码会导致无限循环：

```javascript
// 不要使用 - 创建无限循环
for (let i = 25; i > 10; i++) {
  document.write("This sentence can repeat...<br>");
}
```

错误！变量`i`被赋值为 25 并且每次递增。这意味着`i`永远大于 10，条件`i > 10`永远为真。

要修复此，请调整循环中的条件，使其最终为假。这里是循环可以停止的两种示例：

```javascript
for (let i = 25; i > 10; i--) {
  document.write("This sentence can be stopped!<br>");
}
```

在这里，`i`是递减而不是递增，这会将`i`的值降低到 10，使条件失效。

```javascript
for (let i = 25; i < 50; i++) {
  document.write("This sentence can be stopped<br>");
}
```

在这种情况下，条件被更改为`i < 50`，同时保持递增。当`i`达到 50 时，条件将为假并结束循环。

### 多语句

循环在初始化时也可以包含多个语句。这允许你拥有多个计数变量，并由循环进行修改。例如，如果你想计算十位数，可以使用以下代码从 10 数到 100：

```javascript
for (let i = 1, j = 10; i < 11; i++, j += 10) {
  document.write(j + "<br>");
}
```

### JavaScript: 初学者指南

### while

`while`循环会测试一个比较，并重复执行直到比较不再为真。以下显示了`while`循环的通用结构：

```javascript
let count = 1;
while (count < 6) {
  count++;
}
```

- 给一个变量赋值一个值来计数循环
- `while`语句开始于一个比较
- 调整计数器以便你不会陷入死循环

### 首次

在`while`循环中，你必须记住在循环之前更改变量的值，否则你将陷入永久循环。如果之前的循环没有包含计数代码，循环将无限次重复下去，而你不希望发生这种情况。因此，在使用`while`循环时你必须记住的要点是：在循环之前给计数变量赋一个初始值，并在循环内部调整变量的值。

关于`while`循环实际运行的示例，你可以阅读你的句子重复脚本以如何配合`while`循环：

```javascript
document.write("Get ready for some repeated text.<br>");
let count = 1;
while (count < 11) {
  document.write(count + ". I am part of a loop!<br>");
}
document.write("Now we are back to the plain text.");
```

> 这一行在页面上写了十次，就像 for 循环一样

前面的代码将产生与你的`for`循环相同的结果，只是外观有所不同，如图 6-6 所示。在很多情况下，你可以根据个人喜好选择`for`循环或`while`循环，因为它们可以执行许多任务。

在循环嵌套方面，它的工作方式与`for`循环相同。你可以在`while`循环内部插入另一个`while`循环、`for`循环或`if/else`语句块。如果你愿意，也可以在其他语句块中插入`while`循环。

### do while

`while`循环是一个特殊情况，因为循环内部的代码至少会执行一次，即使第一次比较返回假也是如此。在其他循环中，第一次尝试就返回虚假的比较将导致它们永远不会执行。在`do while`循环的情况下，循环会执行一次，之后每次都会检查比较，以确定是否应该重复。

## 第 6 章：条件语句与循环 155

图 6-6 使用 while 循环将了一行文本重复了十次。

以下是一个运行五次的 do 循环示例：

```javascript
let count = 1;
do {
  document.write("Hi!");
  count++;
} while (count < 6);
```

- `do`关键字开始 do 循环
- `while`语句在第一次运行后，每次都会运行比较

在前面的代码中，关键字和左括号是该块中的唯一内容。然后，当语句块完成后，你就会看到`while`语句和比较。`do`关键字是你确保代码块至少执行一次的方法。

此后，浏览器会检查重复五次，因为变量从 1 开始，并在每次执行期间每次增加 1。当`count`的值达到 6 时，循环将由于跳过且不再执行。还要注意，循环末尾有一个分号，这与其他类型的循环不同，以确保其正确。

要查看一个即使在初始比较返回假也会至少执行一次的 do 循环示例，请看示例代码：

```javascript
let count = 11;
do {
  document.write("Hi!");
  count++;
} while (count < 10);
```

这只在页面上写了一次，因为比较将返回假

### JavaScript: 初学者指南

前面代码中的循环将只运行第一次。当检查比较时（此时`count`将是 12，因为在循环执行期间对其加了 1），它返回假，且循环不再运行。

当你有一段代码需要至少执行一次，但需要重复直到满足某些条件时，`while`循环最为有用；否则，其他循环中的一个就足够完成任务了。

## for in, for each in, and for of

`in`循环允许你遍历对象的所有属性名称，`for each`循环允许你遍历每个属性的值，而`for of`循环允许你遍历各种可迭代对象。这些循环将在第 8 章中更详细地介绍。

### 使用 break 和 continue

`break`和`continue`语句允许你停止正在执行的循环，但它们的工作方式不同。正如你从之前在代码中使用`break`语句记忆的那样，`break`语句会在某点停止循环并完全退出循环，移动到循环后的下一个语句。例如，`break`可以用于：

```javascript
let stopnumber = 5;
for (let count = 1; count < 11; count++) {
  if (count === stopnumber) {
    document.write("Sorry, the loop stops here!<br>");
    break; // 当 count 等于 5 时，这结束循环
  } else {
    document.write(count + " I am part of a loop!<br>");
  }
}
```

此循环将正常运行直到`count`等于`stopnumber`的值（在这种情况下为 5）。当这种情况发生时，循环被完全使用。因此，而不是通过十次循环，循环只会执行五次。

如果你决定在条件发生时不完全离开循环，你可以修改循环使用`continue`语句。`continue`语句会停止循环在当前轮次中执行其后的任何语句。然而，它会回到循环的开头，并从停止的地方继续。例如，你可以使用：

```javascript
let skipnumber = 5;
for (let count = 1; count < 11; count++) {
  if (count === skipnumber) {
    continue; // 不
  }
  document.write(count + " I am part of loop!<br>");
}
```

## 第 6 章：条件语句与循环 157

图 6-7 跳过了第五次迭代，所以只显示 1–4 和 6–10。这一次，当`count`等于`skipnumber`（在这种情况下为 5）时，页面上没有写入任何内容。相反，循环被返回开头并从那里继续。结果是“I am part of loop!”消息只写到页面上九次（实际上跳过了文本将被写入的第五次并继续进行第六次）。图 6-7 显示了这在浏览器中运行时的样子。

当出现需要完全停止循环或停止循环并从开始重启的特殊情况时，`break`和`continue`语句将证明你有帮助。

### 专家问答

**问：** 循环除了反复在页面上写一行文本外，还有其他用吗？

**答：** 是的，随着你学习这些章节，你会发现它们的用。在第 7 章中，当处理数组时它们会特别有用。

**问：** 在循环内部使用变量计数真的可以吗？这不会导致问题吗？

**答：** 在循环内部使用变量是可以的，只要你不要以某种方式给它赋值。如果你担心可能会这样做，请将其值赋给另一个变量并使用它。例如，请看以下代码：

```javascript
let thenum = 0;
for (let count = 1; count < 11; count++) {
  thenum = count;
  document.write(thenum + ". I am part of a loop!<br>");
}
```

在这里，你将`count`的值赋给命名变量。然后使用该变量而不是`count`变量。注意，如果你打算这样做，给`count`变量赋值是可以的。

**问：** 当我想使用循环时，我应该用`for`还是`while`循环？哪一个更好？

**答：** 使用你个人偏好的循环类型。通常，循环的类型取决于具体情况。

**问：** `do`循环对我会有用吗？

**答：** 尽管`do`循环确实有它的用处，除非你使用脚本让`do`循环在检查之前至少运行一次，否则不太可能使用它。然而，你在本章中获得的关于`do`循环的知识将对你遇到网络或其他地方的脚本有所帮助。

## 第 6 章：条件语句与循环 159

2. 创建一个外部 JavaScript 文件并将其保存为`prjs6_2.js`。使用它来完成步骤 3–5。
3. 将你来自`prjs6_1.js`的 JavaScript 代码复制并粘贴到你的`prjs6_2.js`文件中。
4. 在脚本中添加新变量`items`并给它赋值为 0。
5. 在`switch`语句中，添加代码根据城市名称为`items`变量赋值以下值：
   - 如果城市是 Johnstown，赋值为 10
   - 如果城市是 Donnie，赋值为 5
   - 如果城市是 Daientown 或 Martyville，赋值为 2。
   - 对于任何未输入的城市赋值为 0。
6. 在`document.write(msg)`语句之后，添加额外代码，如果`items`变量的值大于 0（使用`if`语句），则执行以下`document.write()`：

```javascript
document.write(
  "<p>We can deliver up to " + items +
  " items to your city.</p>"
);
document.write(
  "<p>Print this out, write your item numbers below, " +
  "and mail it to us to order.</p>"
);
```

7. 紧接这些语句之后（仍在`if`语句内部），创建一个循环，它将显示一个数字并在其跟随一系列下划线 (_) 以为项目编号留出位置。该循环运行的次数将允许为输入的城市订购最大数量的物品。
8. 当你

## JavaScript：初学者指南

```javascript
case "Danieltown" :
    // fall through
case "Martyville" :
    msg = "We can have items delivered to you in 2 weeks.";
    items = 2;
    break;
msg = "Sorry! We do not deliver to your city yet.";
items = 0;
}
document.write(msg);
if (items > 0) {
    document.write(
        "<p>We deliver up to " + items +
        " items to your city.</p>");
    document.write(
        "<p>Print this out, write your item numbers below," +
        " and mail it to us to order.</p>"
    );
for (let count = 1; count <= items; count++) {
    document.write(count + "<br>");
}
```

9. 再次保存 JavaScript 文件并在浏览器中查看 HTML 页面。输入城市并查看结果。你可以刷新页面以尝试不同的城市名称。

### 练习总结

在这个项目中，你利用对循环和`if`语句的知识，通过为不同城市的客户添加自定义的“平信”订单表，增强了你之前的项目。

## 第 6 章自测

1. 条件语句是一种你可以根据一个 ________ 或在当 ________ 不满足时根据其他情况来执行一段代码的语句。
2. 你可以将条件语句想象成有点像 ________ 和 ________。
3. 条件语句不是执行脚本中的每一行代码，而是允许在仅满足特定条件时才执行脚本的某些部分。
   - A. 正确
   - B. 错误
4. 下列哪一项可以作为`if/else`语句的第一行？
   - A. `if (x=2)`
   - B. `if (y<7)`
   - C. `else`
   - D. `if ((x==2 && y))`
5. 你使用什么来包裹条件判断和循环中的代码块？
   - A. 圆括号
   - B. 方括号
   - C. 大括号
   - D. 小于和大于号
6. ________ 允许你获取单个变量值，并根据该变量的值执行不同的代码行。
7. ________ 是允许你重复执行某段特定代码的代码块。
8. 循环很有用，是因为它强迫你重复输入代码行。
   - A. 正确
   - B. 错误
9. 下列哪一项可以作为`for`语句的第一行？
   - A. `for (let x=1; x<6; x+=1)`
   - B. `for (x==1; x<6; x+=1)`
   - C. `for (int x=1; x=6; x+=1)`
   - D. `for (let x+=1; x<6; x=1)`
10. ________ 检查一个比较并重复执行直到该比较不再为真。
11. 下列哪一项作为`while`循环的第一行是不建议的（它会死循环）？
    - A. `while (x<=7)`
    - B. `while (x=7)`
    - C. `while (x<7)`
    - D. `while (x!=7)`
12. `do`循环是特殊的，因为即使所使用的比较第一次返回为假，循环内的代码也会至少执行一次。
    - A. 正确
    - B. 错误
13. `do while`块的第一行包含关键字`do`和一个比较表达式。
    - A. 正确
    - B. 错误
14. `do while`块的最后一行只包含一个大括号。
    - A. 正确
    - B. 错误
15. 你可以嵌套多少次 ________？
    - A. 0次
    - B. 1次
    - C. 三次
    - D. 随心所欲嵌套多少次

### JavaScript: 入门指南

将`arrayname`替换为你想要给数组的名称。你会发现`new`关键字与`Array()`一起使用。这段代码定义了一个空数组，但你也可以在括号中放置参数，以提供数组的长度或每个数组项的值。

要指定数组的长度，你可以在括号内放置单个数字值，如下代码所示：

```javascript
let students = new Array(4);
```

此数组名为`students`，并包含四个项。这四个项最初都被设置为`undefined`，但稍后可以在你的代码中定义每个项。虽然你可以这样做，但没有必要设置数组长度，因为在脚本执行期间，长度可以根据需要进行变化，就像你处理函数一样：

```javascript
let students = new Array("Thomas", "Roger", "Amber", "Jennifer");
```

此数组有四个定义的项："Thomas"、Roger"、Amber" 和 "Jennifer"。

在阅读时，请注意，JavaScript 允许你在同一个数组中更改数据类型。以下代码也会产生一个有效的数组：

```javascript
let answers = new Array(42, "paper", -3, "plastic");
```

通过这种方式，你拥有极大的灵活性，因为你并不局限于数组中的一种数据类型。

### 注意

当使用数组构造函数时，提供单个数字值作为参数将始终创建一个该长度的数组，而不是创建一个包含该值的单个项的数组。因此，`let students = new Array(4);`将创建一个包含四个项的数组，而不是创建一个包含一个值为 4 的项的数组。如果提供了多个参数（无论是否为数字），所有参数都将如预期的那样作为项的值被使用。

## 数组字面量表示

数组字面量为定义数组提供了一种更短的方法，它使用方括号 (`[]`) 而不是构造函数语法。例如，你可以使用以下代码创建一个空数组：

```javascript
let students = [];
```

你只需通过在逗号分隔的列表中提供它们来添加项，就像你提供参数一样。以下示例使用数组字面量表示创建了所有有效数组：

```javascript
let answers = [42, "paper", -3, "plastic"];
let is_true = [true, false];
let nums = [4, 20, 19, 2, 2, 10056, -42, 3];
```

# 第 7 章：JavaScript 数组 167

与数组构造函数一样，任何数据类型都可以作为项的值。在本书中，我在定义数组时最常用数组字面量表示法。

### 注意

当使用数组字面量表示法时，单个数字值会创建一个以该值作为唯一项的数组，而数组构造函数会创建一个该长度的数组。因此，`let students = [4];`将创建一个包含一个值为 4 的项的数组，而不是一个包含四个项的数组。

## 访问数组的元素

要访问数组的元素，请使用所谓的“索引”（index），它允许你通过位置访问数组中的每个项。例如，考虑以下示例代码：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
```

你可以使用语法`students[0]`访问 "Thomas"，使用`students[1]`访问 "Roger"，依此类推。注意，方括号紧跟在数组名之后，并且它们包含了你用于访问数组的项的索引。你还会发现第一个项通过索引 0 访问。这是因为数组从 0 开始而不是 1 开始；因此，你需要注意不要混淆数组中项的索引。第一个项的索引为 0，第二个项的索引为 1，第三个项的索引为 2，依此类推。

你可以像往常一样在代码中使用数组项。你可以通过以下代码输出数组项：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
alert(students[0]);
alert(students[1]);
alert(students[2]);
alert(students[3]);
```

- 输出第一个项是 "Thomas"
- 输出第二个项是 "Roger"
- 输出第三个项是 "Amber"
- 输出第四个项是 "Jennifer"

或者可以使用数组项的赋值值：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
console.log(students[0]); // 输出 "Thomas"
```

## JavaScript：初学者指南

### 修改值

在脚本中，每个项都可以随时更改其值。与变量类似，只需在下面的代码中赋值一个新值，就可以更改数组项的值：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
students[2] = "Dawn"; // 数组中第三个项的值被更改了。
```

这会将数组第三个项（索引 2）的值从 "Amber" 更改为 "Dawn"。你也可以遍历数组并根据需要更改每个项。例如，下面的代码将为数组每个项的值分配相同的后缀：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
for (let i = 0; i < students.length; i++) {
  students[i] += " Doe";
}
```

这为所有学生分配了姓氏 "Doe"：`students[0]`现在的值是 "Thomas Doe"，`students[1]`现在的值是 "Roger Doe"，依此类推。

### 修改长度

你不仅可以修改`length`属性的值，还可以更改它。这样做可以从数组末尾删除项或在数组末尾添加项。例如，下面的代码将从 students 中删除最后两个项：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
students.length = 2;
```

数组原本有四个项，但现在只有两个："Thomas" 和 "Roger"。

如果你将长度更改为大于数组当前长度的数字，则项将添加到数组的末尾。下面的代码展示了这种例子：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
students.length = 7;
```

数组现在有七个元素，在末尾添加了三个元素。最后三个元素（`students[4]`, `students[5]`, 和 `students[6]`）在显式给它们赋值之前，其值将为`undefined`。

增加数组长度的另一种方法是向大于数组中任何索引的索引赋值。例如，考虑下面的代码：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"]; // 数组现在有七个元素，索引 6 的项被定义为 "Marty"。
students[6] = "Marty";
```

在索引 6 定义一个项会导致数组扩展以包含新项。原始数组末尾的元素和新定义的索引之间在被赋值之前，其值将为`undefined`。在这种情况下，`students[4]`和`students[5]`将是`undefined`，而`students[6]`将是代码中定义的 "Marty"。

# 第 7 章：JavaScript 数组 171

如果你不确定最后一个元素在哪里，并想在数组末尾添加元素，可以在下面的代码中使用括号中的数组`length`来：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
students[students.length] = "Marty";
```

`students[4]`被添加到数组中并被赋值为 "Marty"。这之所以可行是因为数组从 0 开始，到`length - 1`结束。

可以使用数组方法提供其他添加或删除项的方法，你将在本章的晚些部分学习它们。

## 尝试一下 7-1 在数组中使用循环

```
pr7_1.html
prjs7_1.js
```

此项目允许你练习将循环与数组。假设你的公司正在销售特定的计算机零件，并且你想显示你出售的每个零件。你所有的零件名称都存储在一个数组中。

### 逐步步骤

1. 创建一个 HTML 页面，其标题文本为“Computer Parts Available”（可用计算机零件）。添加包含名为`prjs7_1.js`的外部 JavaScript 文件的标签。将 HTML 文件保存为`pr7_1.html`。
2. 创建一个外部 JavaScript 文件并将其保存为`prjs7_1.js`。将其用于步骤 3 到 6。
3. 创建一个名为`computer_parts`的新数组，并将以下零件列表赋值为数组中项的值：
   - Monitors（显示器）
   - Motherboards（主板）
   - Chips（芯片）
   - Hard Drives（硬盘）
   - DVD-ROMs（DVD-光驱）
   - Cases（机箱）
   - Power Supplies（电源）
4. 在浏览器窗口中单独行显示每个计算机零件（使用循环）。
5. 完成后，你的 JavaScript 文件应该具有以下代码（有多种可能的答案）：

```javascript
let computer_parts = ["Monitors", "Motherboards", "Chips", "Hard Drives", "DVD-ROMs", "Cases", "Power Supplies"];
for (let i = 0; i < computer_parts.length; i++) {
  document.write(computer_parts[i] + "<br>");
}
```

6. 保存 JavaScript 文件并在`<br>`环境中加载 HTML 文件以查看结果。你应该看到当前的零件列表。

## JavaScript：初学者指南

### 尝试一下总结

在这个项目中，你使用了循环、数组和 Array 对象属性的知识来创建两个不同的结果。一个结果列出了数组的元素，而另一个向数组中添加了一些元素并按字母顺序列出元素。

## 数组属性和方法

数组有许多可在脚本使用的属性和方法。这些允许你执行如添加项、删除项等操作。

### length 属性

正如你所看到的，`length`属性返回一个数字，告诉数组中有多少元素。由于你已经在使用它，可以参考之前的章节获取更多信息。

### 方法

现在你已经知道了数组的属性，本节介绍了用于对数组进行不同操作的方法。表 7-2 列出了这些方法并提供了每个方法的描述。在表格之后，将对常用方法进行详细描述。

### constructor 和 prototype

`constructor`属性指向创建实例的函数：

```javascript
function Array() { }
```

### index 和 input 属性

| 属性 | 描述 |
| --- | --- |
| `constructor` | 指向创建实例的函数 |
| `index` | 创建数组时使用 |
| `input` | 创建数组 |
| `length` | 包含一个等于元素数量的数值 |
| `prototype` | 允许向 Array 添加属性 |

表 7-1 数组属性

| 方法 | 描述 |
| --- | --- |
| `join()` | 将数组元素合并为带有分隔符的单个字符串 |
| `pop()` | 从数组中删除最后一个元素并返回删除的元素 |
| `push()` | 向数组末尾添加元素并返回新长度的数值 |
| `shift()` | 从数组中删除第一个元素并返回该元素 |
| `unshift()` | 向数组开头添加元素并返回新长度的数值 |
| `reverse()` | 反转数组元素的顺序 |
| `sort()` | 按字母顺序对数组元素进行排序 |
| `concat()` | 将两个或多个数组的元素合并为一个新数组 |
| `slice()` | 提取数组的特定部分并将该部分作为新数组返回 |
| `splice()` | 从数组中删除元素或替换数组元素 |
| `indexOf()` | 查找项在数组中的索引 |
| `lastIndexOf()` | 查找项在数组中的最后一个索引 |
| `every()` | 对数组每个项执行提供的函数，如果所有项均为真则返回真 |
| `filter()` | 对数组每个项执行提供的函数，并返回函数返回真的元素数组 |
| `forEach()` | 对数组每个项执行提供的函数 |
| `map()` | 对数组每个项执行提供的函数，并返回每个项调用函数的结果数组 |

表 7-2 数组对象方法（续）

# 174 JavaScript: 初学者指南

| 方法(s) | 描述 |
| --- | --- |
| `some()` | 为数组的每个项执行提供的函数，如果任何一个项的函数执行结果为 true，则返回 true |
| `reduce()`<br>`reduceRight()` | 为数组的每个项执行提供的函数，并返回一个最终结果 |
| `toString()`<br>`toLocaleString()`<br>`valueOf()` | 将数组的元素组合成单个字符串，并以逗号作为分隔符 |
| `find()`<br>`findIndex()`<br>`includes()` | 在数组中查找元素或索引。 |
| `keys()`<br>`entries()`<br>`values()` | 返回数组的键（索引）、条目或值。 |
| `flat()`<br>`flatMap()` | 展平一个包含其他数组的数组。 |
| `Array.isArray()`<br>`Array.from()`<br>`Array.of()` | 直接从原生对象访问的方法。 |
| `fill()`<br>`copyWithin()` | 从开始索引到结束索引用静态值填充数组。<br>将数组的一部分复制到数组内的另一个位置。 |

## 7-2 数组对象的方法

### join([separator]) 方法

`join([separator])`方法用于将数组的项组合成单个字符串，每个项之间用逗号（默认）或作为参数传递给方法的字符串分隔。

要查看此方法如何工作，请看这段代码。以下示例定义了一个数组，然后在数组名称上调用了`join()`方法：

```javascript
let fruits = ["oranges", "apples", "pears"];
let fruit_string = fruits.join(",");
```

这段代码将`join()`方法赋值给变量`fruit_string`。注意，该方法是通过使用数组名（fruits）、后接点（.）、以及方法名来调用的。变量`fruit_string`将具有以下字符串值：

oranges,apples, pears

# 第7章：JavaScript 数组 175

你可以通过将字符串变量写入页面来看到这个结果。以下代码将为你完成操作：

```javascript
let fruits = ["oranges", "apples", "pears"];
let fruit_string = fruits.join(",");
document.write("The new string is " + fruit_string);
```

数组的项以逗号为分隔符连接成单个字符串。

字符串显示在屏幕上。

现在你可以看到从`join()`方法返回的字符串。图 7-3 显示了这段代码在浏览器中运行时产生的结果。

如果你想用逗号以外的内容分隔新字符串中的项，可以传递你想使用的字符串作为参数。以下代码使用冒号作为分隔符：

```javascript
let fruits = ["oranges", "apples", "pears"];
let fruit_string = fruits.join(":");
document.write("The new string is " + fruit_string);
```

字符串显示在屏幕上。

这次与之前的略有不同，因为它用冒号代替了之前示例中的逗号。图 7-4 显示了这在浏览器窗口中将如何显示。

### pop() 方法

`pop()`方法用于从数组中移除最后一项。如果你将方法赋值给变量，被弹出的元素将返回并赋值给该变量。

以下代码创建一个数组并使用`pop()`移除数组的最后一项：

```javascript
let fruits = ["oranges", "apples", "pears"];
fruits.pop();
```

图 7-3 新字符串写在页面上。

### JavaScript: 初学者指南

**图 7-4** 新字符串写在页面上，并用 "oranges", "apples", "pears" 作为分隔符。

这创建了一个名为`fruits`的数组，包含三个项（"oranges", "apples", "pears"）。然后，使用`pop()`方法移除最后一项，将数组缩短为仅剩前项（"oranges", "apples"）。

如果你想移除一个项但以后仍以某种方式使用它，可以将方法的结果赋值给变量。该变量将赋予被弹出项的值。以下示例移除了数组中的项，并将弹出的项作为警告框发送给观众。

```javascript
let fruits = ["oranges", "apples", "pears"];
let picked_fruit = fruits.pop();
window.alert("You picked me " + picked_fruit);
```

此 push 将向观众显示一个显示“You picked my pears”的警告框。

### push() 方法

`push(item)`方法用于向数组末尾添加项。传递给方法的参数是你想要添加到数组中的新项。如果赋值给变量，此方法将返回数组的新长度。

例如，看这段向数组末尾添加一个项的代码：

```javascript
let fruits = ["oranges", "apples", "pears"];
fruits.push("pears");
```

这段代码创建了一个名为`fruits`的数组，包含两个项（"oranges", "apples"），然后使用`push()`方法添加第三个项 "pears"。数组现在包含三个项（"oranges", "apples", "pears"）。

你可以通过发送多个参数来添加多个元素。这些项将按照它们发送的顺序被添加。

```javascript
let fruits = ["oranges", "apples"];
fruits.push("pears", "grapes");
```

这段代码向`fruits`数组添加了两个项。最后，数组包含四个元素（"oranges", "apples", "pears", "grapes"）。

如果你想要方法返回的新长度，可以将结果赋值给变量。以下代码执行了此操作，然后发送了一个警告框：

```javascript
let fruits = ["oranges", "apples"];
let new_length = fruits.push("pears", "grapes");
window.alert("The array now has " + new_length + " items");
```

由于向数组添加了两个项，数组的长度将变为四，并向观众发送一个“The array now has 4 items”的警告框。

> 注意 对于那些用过其他语言编程的人来说，`push()`和`pop()`将数组视为栈（后进先出）。将这些与`shift()`和`unshift()`结合可以让数组像队列一样工作。

### shift() 方法

`shift()`方法用于移除数组的第一项。它返回被移除的值。以下代码使用`shift()`方法移除第一项：

```javascript
let fruits = ["oranges", "apples", "pears"];
fruits.shift();
```

数组现在只有两个项。如果你想使用被移除的值，可以将方法的结果赋值给变量。该变量将赋予被弹出项的值。以下示例移除了数组中的项，并将弹出的项作为警告框发送给观众：

```javascript
let fruits = ["oranges", "apples", "pears"];
let picked_fruit = fruits.shift();
window.alert("You picked me " + picked_fruit);
```

此 push 将向观众显示一个显示“You picked me oranges”的警告框。

## unshift(item) 方法

`unshift(item)`方法用于向数组的开头添加项。传递给方法的参数是你想要添加到数组中的新项。以下示例向数组开头添加项：

```javascript
let fruits = ["apples", "pears"];
fruits.unshift("oranges");
```

数组`fruits`现在包含了三个项。如果你想向数组开头添加多个项，可以发送多个参数。这些项将按照它们发送的顺序被添加。

```javascript
let fruits = ["apples", "pears"];
fruits.unshift("oranges", "grapes");
```

这段代码向`fruits`数组添加了两个项。最后，数组包含四个元素（"oranges", "grapes", "apples", "pears"）。

## 第 7 章：JavaScript 数组 179

完成这些操作后，顺序现在变为“苹果, 葡萄, 橙子, 梨”。

由于`sort()`方法会将所有值转换为字符串，因此仅包含数值的数组将根据其转换为字符串后的结果进行排序：

```javascript
let fruits = [2, 3, 1, 20];
fruits.sort();
```

与预期的顺序（数值顺序）不同，排序后的顺序是 1, 2, 20, 3，因为这些值是作为字符串进行比较的。为了解决这类问题，JavaScript 允许你将一个比较函数作为`sort()`方法的参数。

比较函数是一个带有两个参数的函数，它根据两个参数值比较的结果返回正数、负数或零。例如，这里显示了一个简单的比较函数：

```javascript
function mysort(first_value, second_value) {
  if (first_value > second_value) {
    return 1;
  } else if (first_value < second_value) {
    return -1;
  } else {
    return 0;
  }
}
```

基本上，如果第一个参数大于第二个参数，比较函数应该返回一个正数；如果第一个参数小于第二个参数，返回一个负数；如果两个参数相等，则返回零。使用此方法将按升序排列项目。将前面代码中的函数作为`sort()`方法的参数，可以将数字按预期的数值顺序排列，因为大于运算符将比较数值值而不是将它们转换为字符串。以下是其操作方法的示例：

```javascript
let fruits = [2, 3, 1, 20];
function mysort(first_value, second_value) {
  if (first_value > second_value) {
    return 1;
  } else if (first_value < second_value) {
    return -1;
  } else {
    return 0;
  }
}
fruits.sort(mysort);
```

> 比较函数的名称被用作`sort()`方法的参数。

完成这些操作后，排序将按预期的顺序排列：1, 2, 3, 20。

### concat() 方法

`concat(array)`将该数组与它的参数合并，并返回一个包含所有项目的新数组。它不会影响原始数组。你使用数组名称或单个值作为参数，并按顺序提供它们。

## 180 JavaScript：初学者指南。

第一个示例结合了两个数组的元素。要做到这一点，只需要使用一个参数——与调用该方法的数组合并的数组名称：

```javascript
let fruits = ["oranges", "apples"];
let veggies = ["corn", "peas"];
let fruits_n_veggies = fruits.concat(veggies);
```

这段代码创建了一个名为`fruits`的包含两个元素的数组，以及一个名为`veggies`的包含两个元素的数组。接下来，它定义了`fruits_n_veggies`，它将接收由`concat()`方法返回的数组。在这种情况下，`fruits_n_veggies`数组将由“橙子”、“苹果”、“玉米”、“豌豆”组成

如果你想让`veggies`数组中的元素列在前面，可以使用`veggies`数组名和`fruits`数组名作为参数来实现这一点：

```javascript
let fruits = ["oranges", "apples"];
let veggies = ["corn", "peas"];
let fruits_n_veggies = veggies.concat(fruits);
```

现在，`veggies`数组的项列在前面，新的`fruits_n_veggies`数组具有以下项目：“玉米”、“豌豆”、“橙子”、“苹果”。

如果你合并三个数组，调用`concat()`方法的数组的项目将排在前面，然后每个数组组的项将按照它们出现的顺序作为参数：

```javascript
let fruits = ["oranges", "apples"];
let veggies = ["corn", "peas"];
let meats = ["fish", "chicken"];
let three_groups = fruits.concat(veggies, meats);
```

现在你正在合并三个数组，新`three_groups`数组中的项目如下：“橙子”、“苹果”、“玉米”、“豌豆”、“鱼”、“鸡肉”。

如果你按照以下编写代码，你将得到一个具有相同元素但顺序不同的数组：

```javascript
let fruits = ["oranges", "apples"];
let veggies = ["corn", "peas"];
let meats = ["fish", "chicken"];
let three_groups = meats.concat(veggies, fruits);
```

使用此代码时，新`three_groups`数组中的元素顺序如下：“鱼”、“鸡肉”、“玉米”、“豌豆”、“橙子”、“苹果”。

在合并数组时，你也可以合并字符串、数字或其他数据类型。如果需要，所有这些都可以完成：

```javascript
let fruits = ["oranges", "apples"];
let veggies = ["corn", "peas"];
let big_array = fruits.concat(veggies, "cat", 4, ["house","car"]);
```

## 199 第 7 章：JavaScript 数组

### slice()

`slice()`方法提取数组的特定部分并将该部分作为新数组返回。它接受两个参数：开始索引和结束索引（不包括结束索引本身）。

```javascript
let fruits = ["oranges", "apples", "pears", "grapes"];
let some_fruits = fruits.slice(1, 3);
```

这将返回一个包含 "apples" 和 "pears" 的新数组。

# 第 7 章：JavaScript 数组 183

在这里，使用`indexOf()`从第一个开始搜索项目 "apples" 会返回 1，因为它会在索引 1 处找到第一个 "apples" 实例。如果你使用`lastIndexOf()`从后部搜索 "apples"，将返回 3，因为`lastIndexOf()`检测到的第一个 "apples" 实例是索引 3 处的最后一个。使用这两种方法任一种搜索 "grapes" 都会返回 -1，因为 "grapes" 不是数组中的项目。

请注意，如果项目不在数组中，返回的是 -1 而不是 0（0 是一个合法的索引）。因此，你应该避免使用诸如`if (fruits.indexOf("grapes") == 0)`这样的结构来判断项目是否不在数组。相反，你应该使用`if (fruits.indexOf("grapes") == -1)`来判断。

这两个方法都可以提供第二个参数，用于指定从哪个索引**开始**。这允许`indexOf()`和`lastIndexOf()`跳过某个项的实例，并返回从指定索引开始找到的第一个项的索引。例如，考虑以下代码：

```javascript
let fruits = ["apples", "pears", "apples"];
let found_apples = fruits.indexOf("apples", 2);
window.alert(found_apples);
let found_apples = fruits.lastIndexOf("apples", 1);
window.alert(found_apples);
```

在这种情况下，调用`indexOf("apples", 2)`从大于 0 的索引 2 开始从前向后搜索。这意味着它将跳过索引 1 处的第一个 "apples" 实例，从索引 2 开始搜索并返回 3。`lastIndexOf("apples", 1)`从索引 1 开始搜索并向前进行；索引 3 处的 "apples" 被跳过了。

最后，重要的是，这两种方法都使用`===`运算符而不是`==`运算符来确定判断是否找到了某个项。因此，不会执行类型转换，且必须是精确匹配。例如，考虑以下代码：

```javascript
let nums = ["2", 5, 2, 3];
let found_two = nums.lastIndexOf(2);
alert(found_two);
```

第一个项目 ("2") 是字符串，而不是数值 2。由于 "2" 和 2 并不严格相等，因此未找到该项目并返回 -1。在使用这些方法时请记住这一点，以避免意外的结果。

## every(), filter(), map(), 和 some() 方法

`every()`、`filter()`、`map()`和`some()`方法是在 ECMAScript 5 中添加的，用于提供一种将函数作为数组中每个项的参数的方法。这些是迭代函数，意味着它们会遍历数组中的每个项。以下是每个迭代方法的功能：

- `every()`为每个项执行提供的函数，如果函数对所有项都返回 true，则返回 true。
- `some()`为每个项执行提供的函数，如果函数的执行结果在任何项上返回 true，则返回 true。
- `filter()`为每个项执行提供的函数，并返回一个由函数返回 true 的项数组。
- `map()`为每个项执行提供的函数，并返回一个通过在每个项上调用该函数得到的结果数组。
- `forEach()`为每个项执行提供的函数。不返回任何值。

要使用其中一种方法，你将调用它并提供一个函数名作为参数，如下所示：

```javascript
let grades = [94, 65, 71, 84, 99];
let the_result = grades.every(pass_grades);
```

`every()`方法返回的结果遍历所有数组项，运行的命名函数 (`pass_grades`) 将被存储在变量`the_result`中。例如，假设函数名`pass_grades()`用于判断以下代码中学生所有记录的成绩是否都达到 70 分以上：

```javascript
function pass_grades(item_value, item_index, arr_name) {
  return (item_value >= 70);
}
let grades = [94, 65, 71, 84, 99];
let the_result = grades.every(pass_grades);
window.alert(the_result);
```

> 函数从`every()`方法接收三个参数。使用 return 语句返回一个布尔值。在`grades`数组上使用`pass_grades`函数调用`every()`方法的结果赋值给变量`the_result`。弹出 false。

这将根据成绩是否大于 70 返回一个布尔值。你会注意到函数接受了三个参数：第一个是当前项的值，第二个是当前索引，第三个是数组本身。当调用任何迭代方法时，这些值会被作为参数传递给指定的函数（此处为`pass_grades`）。`pass_grades`函数在迭代过程中返回了以下五个结果：true、false、true、true、true。由于`every()`方法要求所有返回值均为 true 才会返回 true，在这种情况下，由于索引 1 处的一个低分 (65)，它将返回 false。

在之前的代码中，用其他任何方法代替`every()`将产生以下结果：

- `some()`将返回 true，因为只需要返回值中有一个为 true 即可（在这种情况下，五个返回值中有四个是 true）。
- `filter()`将返回一个包含所有项的数组。在这种情况下，数组将是`[94, 71, 84, 99]`。
- `map()`将返回一个包含每个函数调用结果的数组。在这种情况下，数组将是`[true, false, true, true, true]`。此新数组赋值给变量`the_result`。
- `forEach()`不返回任何内容。

## reduce() 和 reduceRight() 方法

`reduce()`和`reduceRight()`方法也是在 ECMAScript 5 中添加的。这些方法遍历数组中的项，但它们构建并返回一个最终值。这些方法像迭代方法一样使用函数作为参数。参数本身传递两个参数：累加值和当前值。

注意：如果你需要对每个项进行某些操作，`some()`或`every()`在遇到匹配条件时就会停止。考虑以下代码示例：

```javascript
function sub_values(prev_value, next_value) {
  return (prev_value - next_value);
}
let nums = [2, 4, 8, 16, 32];
let the_result = nums.reduce(sub_values);
window.alert(the_result);
the_result = nums.reduceRight(sub_values);
window.alert(the_result);
```

函数接收前一个值和下一个值的参数。返回`prev_value`减去`next_value`的结果。

弹出 -5

弹出 2

当调用`reduce()`时，项从前向后迭代，这会创建一个负数 (-5)。第一次，2 和 4 作为参数传递，2–4 = -2。下一次迭代，结果 (-2) 作为`prev_value`传递，8 作为`next_value`传递，-2–8 = -10。这种模式持续直到得到最终结果 -8。

当调用`reduceRight()`时，发生了相同的过程，但从后向前进行。在这种情况下，32 和 16 作为参数传递，32–16 = 16。接下来 (16) 和 8 作为参数传递，16–8 = 2。这种模式持续直到得到最终结果 2。

## JavaScript：初学者指南

## find(), indexOf(), includes(), 和 keys() 方法

MAScript 6 增加了许多用于在数组查找项、索引和数组键的新方法。现在你有了比`indexOf()`更多选择，在查找特定信息时这些选项对你更有帮助。

`find()`方法可以找到第一个使提供的测试函数返回`true`的数组项值。如果没有匹配项，它将返回`"undefined"`。以下是其实际运行示例：

```javascript
let numbers = [1, 3, 5, 1, 2, 4];
let foundSmall = numbers.find(function (itemValue) {
  return itemValue < 3;
});
window.alert(foundSmall);
let foundLarge = numbers.find(function (itemValue) {
  return itemValue > 7;
});
window.alert(foundLarge);
```

> 定义了一个数字数组。

> 使用`find()`方法获取数组中第一个小于 3 的值。

> 此弹窗显示 1（第一个小于 3 的项的值）。

> 由于数组中没有值大于 7 的项，因此弹窗显示`"undefined"`。

> 使用`find()`方法获取数组中第一个大于 7 的值。

接下来，`indexOf()`非常像`find()`，但它返回的是第一个使提供的测试函数返回`true`的项的索引（而不是返回项的值）。如果没有找到匹配项，它将返回 -1。以下代码显示了此示例：

```javascript
let numbers = [1, 3, 5, 1, 2, 4];
let foundSmall = numbers.indexOf(function (itemValue) {
  return itemValue < 3;
});
window.alert(foundSmall);
let foundLarge = numbers.indexOf(function (itemValue) {
  return itemValue > 7;
});
window.alert(foundLarge);
```

> 弹窗显示 0（第一个匹配项的索引）。

> 弹窗显示 -1（未找到匹配项）。

`includes()`方法在数组中搜索该值。如果找到了该值，该方法返回`true`；否则该方法返回`false`。如果你不想搜索整个数组，还可以提供一个起始索引来开始搜索。以下代码显示了此示例：

```javascript
let numbers = [1, 3, 5, 1, 2, 4];
let foundOne = numbers.includes(1); // true
let foundIndex4After = numbers.includes(1, 4); // false
```

### keys() 方法

`keys()`方法返回数组中的键，这些仅仅是迭代器数字（0, 1, 2 等）。以下代码显示了此示例：

```javascript
let numbers = [1, 3, 5, 1, 2, 4];
let arrKeys = [...numbers.keys()]; // [0, 1, 2, 3, 4, 5];
```

## flat() 和 flatMap() 方法

`flat()`和`flatMap()`方法可以将嵌套数组展平为不包含嵌套的数组。在下一节中，你将学习嵌套数组，这些方法变得更加清晰。以下代码显示了使用`flat()`的示例（请在阅读嵌套数组章节后回来）：

```javascript
let numbers = [1, 3, 5, 1, 2, 4];
let flatNumbers = numbers.flat(); // [1, 3, 5, 1, 2, 4]
```

## Array.isArray(), Array.from(), 和 Array.of() 方法

这些数组通过`Array`关键字调用；它们操作的项目在这些方法接收时可能是数组也可能不是。

例如，`Array.isArray()`方法测试指定值是否为数组。以下代码显示了此示例：

```javascript
let numbers = [1, 3, 5, 1, 2, 4];
Array.isArray(numbers); // true
Array.isArray(5); // false
```

`Array.from()`可以从类数组对象或迭代对象创建新的数组实例。以下代码显示了此示例：

```javascript
let arr = Array.from("abc"); // ["a", "b", "c"]
```

`Array.of()`从任意数量的参数创建一个新的数组实例并返回它。以下代码显示了此示例：

```javascript
let arr = Array.of(1, 2, 3); // [1, 2, 3]
```

### 嵌套数组

数组可以嵌套，允许你将数组作为一项使用。这提供了创建多个维度的能力。要了解这可能如何使用，请回到：

```javascript
let students = ["Thomas", "Roger", "Amber", "Jennifer"];
```

假设你还想记录每个学生的最后一次成绩和当前成绩。你可以将它们添加到数组中，但这会让获取正确信息变得困难：

```javascript
let students = [
  ["Thomas", 92, 90],
  ["Roger", 87, 78],
  ["Amber", 81, 85],
  ["Jennifer", 99, 100]
];
```

如你所见，遍历数组将提取出索引 0 的 Thomas，索引 1 的最后一次成绩和索引 2 的当前成绩。Roger 使用索引 3, 4 和 5：Amber 使用 6, 7，以及 Jennifer 使用 9, 10 和 11。尝试将这些值与正确的学生关联起来可能是困难的，尤其是当你想要遍历数组时。处理学生与成绩的关系可能会变得繁琐，因为你需要根据每第三个位置是一个新学生进行计算。

如果能将每个学生与其成绩分组在独立的数组中，并通过主数组访问，那就太好了。这是嵌套数组的方法，可以让生活更轻松。

### 定义嵌套数组

使用数组表示法，你可以通过为每个新数组添加额外的括号来轻松嵌套数组。以下代码显示了：

```javascript
let students = [
  ["Thomas", 92, 90],
  ["Roger", 87, 78],
  ["Amber", 81, 85],
  ["Jennifer", 99, 100]
];
```

在这里，外部数组（students）包含了四个内部数组。第一个数组位于 students 数组的索引 0 处（`students[0]`）。你可以通过在第一个括号后面紧跟第二个方括号来访问内部数组中的项。例如，`students[0][0]`的值为 "Thomas"，`students[2][1]`的值为 81。

# 190 JavaScript：初学者指南。

注意，可以使用数组构造函数来实现，尽管语法稍微长一点：

```javascript
let students = new Array(new Array("Thomas", 92, 90),
              new Array("Roger", 87, 78),
              new Array("Amber", 81, 85),
              new Array("Jennifer", 99, 100));
```

这种方法可以达到效果，但你必须注意不要在使用构造函数语法时添加包含单个数字项的数组。记住，这样做将创建一个项数少于包含单个项数组的数组（例如，`Array(3)`将创建一个包含三个项的数组，而不是包含一个值为 3 的单项数组的数组）。

# 循环与嵌套数组

为了遍历外部数组中的所有数组，你需要创建一个嵌套循环：一个外层循环用于遍历外层数组的项，另一个循环用于遍历内部数组的项。接下来的代码创建了一个嵌套的`for`循环，它将遍历嵌套数组结构，并显示内部数组中每个项的值：

```javascript
let students = ["Thomas", 92, 90],
              ["Roger", 87, 78],
              ["Amber", 81, 85],
              ["Jennifer", 99, 100];

for (let i = 0; i < students.length; i++) { // 变量在循环中定义用于计数。
  for (let j = 0; j < students[i].length; j++) {
    document.write("students[" + i + "][" + j + "] = " + students[i][j] + "<br>");
  }
}
```

如你所见，`length`属性用于确定`students[0]`、`students[1]`、`students[2]`和`students[3]`每个循环执行的次数，内层循环在外层循环的每次迭代中都会执行三次。图 7-5 显示了在浏览器中运行此脚本的结果。

有了信息和循环，你现在可以根据数组中的数据生成任意数量报告。例如，你可以显示学生姓名以及最近的成绩（每个数组中的最后一个项）。下面的代码展示了这一点：

```javascript
let students = ["Thomas", 92, 90],
              ["Roger", 87, 78],
              ["Amber", 81, 85],
              ["Jennifer", 99, 100];

for (let i = 0; i < students.length; i++) {
  for (let j = 0; j < students[i].length; j++) {
```

# 第 7 章：JavaScript 数组 191

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_209_0.png)

图 7-5 每个内部数组的每个项都已显示。

```javascript
if ( j === 0) {
    document.write(students[i][j] + ": ");
} else if ( j === students[i].length - 1) {
    document.write(students[i][j] + "<br>");
} else {
    continue;
}
```

- 检查项是否位于索引 0，即学生姓名所在地
- 显示学生姓名，后跟冒号和空格
- 检查项是否位于数组的最后一个索引，即最近成绩所在地
- 显示成绩，后跟换行

在这里，你正在使用内层循环来收集你想要显示的数据。该语句用于判断当前索引是否包含该内容。首先我们需要学生姓名，它位于每个内部数组的索引 0 处。另一个项，即最近成绩，是数组中的最后一个项。这是通过检查变量`j`是否等于数组长度减 1 来确定的。此时，你可以使用`students[i][2]`代替，但那样将无法考虑到数组中添加新成绩的情况。使用`students[i].length–1`可以确保使用的是数组中添加的最新成绩。你还会发现最后一条语句只是告诉循环继续下一次迭代，你不需要为此报告提供任何数据。图 7-6 显示了在浏览器中运行此代码的结果。

如你所见，数组对于存储和检索数据非常有帮助，随着你继续编写代码，你将发现它们有许多用途。

## 192 JavaScript：初学者指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_210_0.png)

**图 7-6** 每个学生及其/她最近的成绩都已显示。

# 尝试一下 7-2 嵌套数组练习

```
pr7_2.html
prjs7_2.js
```

这允许你练习使用嵌套数组。假设在你的在线商店中，你决定显示每个电脑部件的特征以及部件名称。嵌套数组将帮助你保持信息整齐。

### 逐步步骤

1. 创建一个 HTML 页面，其标题文本为“Computer Parts Available”（可用电脑部件）。添加`<script>`标签以包含一个名为`prjs7_2.js`的外部 JavaScript 文件。将 HTML 文件保存为`pr7_2.html`。
2. 创建一个名为`prjs7_2.js`的 JavaScript 文件。
3. 创建一个名为`computer_parts`的嵌套数组，如下：

```javascript
let computer_parts = [
  ["Thomas", 92, 90],
  ["Roger", 87, 78],
  ["Amber", 81, 85],
  ["Jennifer", 99, 100]
];
```

4. 使用嵌套循环来显示每个部件的特征。
5. 当你的代码完成后，应该如下：

```javascript
let computer_parts = [
  ["Thomas", 92, 90],
  ["Roger", 87, 78],
  ["Amber", 81, 85],
  ["Jennifer", 99, 100]
];
for (let i = 0; i < computer_parts.length; i++) {
  for (let j = 0; j < computer_parts[i].length; j++) {
    if (j === 0) {
      document.write(computer_parts[i][j] + ": ");
    } else if (j === computer_parts[i].length - 1) {
      document.write(computer_parts[i][j] + "<br>");
    } else {
      continue;
    }
  }
}
```

6. 保存 JavaScript 文件并在浏览器中查看 HTML 文件。你应该看到部件的列表。

# 第 7 章：JavaScript 数组 193

### 尝试一下总结

在这个项目中，你使用了嵌套数组和循环创建一个显示项的页面。

# 第 7 章 自测

1. 数组是数据的 ________。
2. 在 JavaScript 中，有 ________ 种定义数组的方法。
3. 在数组中，对元素的访问通过 ________ 实现。
4. 你可以使用 ________ 遍历数组中的。
5. 你可以使用 JavaScript 关键字作为数组名。
   - A. 正确
   - B. 错误
6. 下面哪一项不能正确创建数组？
   - A. `let myArray = new Array();`
   - B. `let myArray = [3, 4, "Cool"];`
   - C. `let myArray = new Array("hello","hi","greetings");`
   - D. `let myArray = new Array[10];`
7. 为了正确访问数组 "cool" 的第五项，你可以写`cool[5]`。
   - A. 正确
   - B. 错误
8. 以下代码的作用是什么？`let s_list = new Array(5);`
   - A. 创建名为 s_list 的数组
   - B. 创建名为 s_list 的数组，包含一个值为 5 的项
   - C. 创建包含五个项的数组
   - D. 代码无效
9. 数组对象的哪个属性将返回数组长度的数值？
   - A. `length`属性
   - B. `length`属性
   - C. `constructor`属性
   - D. `lengthOf`属性
10. 数组符号允许使用方括号创建数组，而无需编写 "new Array"。
11. ________ 方法用于将两个或多个数组合并为一个新数组，每个项之间由指定的字符分隔。
12. ________ 用于从数组中删除最后一个元素。
13. 默认情况下，`sort()`方法会对数组的内容排序吗？
    - A. 它反转数组的内容。
    - B. 它按数值排序。
    - C. 它使用字符串字符编码对内容进行排序。
    - D. 它根据随机算法进行排序。
15. 数组提供了创建多维数组的能力。

## 第8 章：对象

### 核心技能与概念

- 定义对象
- 创建对象
- 使用原型
- 对象语句
- 理解预定义的 JavaScript 对象

对象为你的脚本提供了更大的灵活性。它们既可以被用作存储数据的另一种方式，也可以用于创建可重用的结构。在本章中，你将学习 JavaScript 对象是如何的（构造的）、如何创建对象，以及如何使用一些预定义的对象。

### 定义对象

由于 JavaScript 是一种基于原型的语言，其对象的工作方式与基于类（class-based）的语言不同。

JavaScript 对象本质上是属性和值的集合，在编程中被称为*哈希表*（hash table）。正是这些值赋予了 JavaScript 极大的灵活性——值可以是任何数据类型，包括函数、数组和其他对象。

你使用对象将多个值从一个地方传递到另一个地方（你会发现当使用 JSON 在 JavaScript 和另一种语言之间传递数据时这非常有用，JSON 将在本书的后部分介绍）。你还可以使用它们来描述一种通用类型的对象，该类型可以有许多特定的*实例*（instances）。例如，可以用于构建特定的汽车（例如：跑车、轿车、家庭汽车）。每辆汽车都可以从通用汽车对象继承属性名，然后拥有自己特定的属性值。

### 创建对象

现在你已经理解了对象是什么及其用处，你可以开始创建你自己的 JavaScript 对象了。为了实现这一点，你将学习命名规范、对象的结构以及如何在你的对象中包含方法。

### 命名

与变量和函数一样，在 JavaScript 中命名对象时也必须遵循某些规则。这些规则与你命名变量和函数时遵循的规则相同，你可以在第3章中复习。

### 单个对象

在 JavaScript 中创建单个对象有两种方法：使用对象构造函数或使用对象字面量符号。单个对象适用于特定目的，例如创建键值对，或用于不需要与其他对象共享代码的唯一对象（在这种情况下，你可能更倾向于创建一个可重用的结构）。此外，你还可以使用单个对象向函数传递配置参数。

### 对象构造函数

对象构造函数的看起来类似于数组构造函数。你只需要给对象取一个名称并将其定义为`new`。下面的代码展示了这样一个示例：

```javascript
let car = new Object();
```

这是一个空对象，可以为其分配属性和值，如下代码所示：

```javascript
let car = new Object();
car.seats = "cloth";
```

在这里，定义了一个名为 "seats" 的属性并为其赋值了值 "cloth"。通过这种方式，你可以定义任意数量的属性。你也可以将一个函数赋值给属性。这被称为方法（method）（回想一下你已经在代码中使用过如`document.write()`和`window.alert()`这样的方法）。方法是对象的一部分的函数，必须使用对象的名称来调用。例如，下面的代码将创建两个属性 "seats" 和 "engine" 以及一个名为 "show_features" 方法：

```javascript
let car = new Object();
car.seats = "cloth";
car.engine = "V-6";
car.show_features = function() {
  window.alert("car: " + car.seats + " seats, " + car.engine + " engine");
};
car.show_features();
```

如你所示，使用函数来定义方法。最后一行显示了如何使用对象名、点号和方法名来调用该方法。注意，方法通过使用对象名、点和属性名来访问每个属性的值。当方法被调用时，它会发送一个警告 "car: cloth seats, V-6 engine"。如果你喜欢，也可以将一个具名的函数赋值为方法，如下：

```javascript
let car = new Object();
car.seats = "cloth";
car.engine = "V-6";
function myAlert() {
  window.alert("car: " + car.seats + " seats, " + car.engine + " engine");
}
```

## 对象字面量

对象字面量使用大括号`{}`来包围对象。这种方法如下：

```javascript
let car = {
  seats: "cloth",
  engine: "V-6"
};
```

你可以通过字面量符号定义任意数量的键值对，只需用逗号分隔。这种方法比使用构造函数更简洁。你也可以在字面量中定义方法：

```javascript
let car = {
  seats: "cloth",
  engine: "V-6"
};
```

## 访问属性

JavaScript 提供了两种方式来访问属性：点符号法和括号符号。

### 点符号法

如你所见，你可以使用点符号法来访问属性值。这种方法非常直观：

```javascript
let car = {
  seats: "cloth",
  engine: "V-6"
};
console.log(car.seats); // 输出 cloth
```

## 括号符号法

括号符号法使用方括号`[]`。这种方法在属性名是变量或表达式时非常有用：

```javascript
let car = {
  seats: "cloth",
  engine: "V-6"
};
console.log(car["seats"]); // 输出 cloth
```

### JavaScript: 初学者指南

与其使用`sts`的值，不如在`car`对象中搜索名为`sts`的属性，这在未找到属性时会返回`undefined`。使用括号表示法，你可以实现它：

```javascript
let car = {
  seats: "cloth",
  engine: "V-6"
};
let s = "seats";
window.alert(car[s]); // 正常工作
```

这一次使用的是变量的值（即字符串 "seats"），并向查看者显示 "cloth"。

**应该使用哪种表示法？** 方法取决于具体情况。点表示法（Dot notation）最常用。当你需要指定属性名、使用变量的值，或使用不符合 JavaScript 习惯的值（例如`seat-type`）时，则应该使用括号表示法来成功访问属性值。

# 尝试 8-1 创建一个计算机对象

```
pr8_1.html
prjs8_1.js
```

在这个项目中，你将自己创建对象并开发与对象创建相关的技能。脚本将创建一个计算机对象，然后使用该对象的属性、方法和实例来为不同类型的计算机创建功能列表和价格列表。

### 步骤详解

1. 创建一个 HTML 页面并保存为`pr8_1.html`。添加必要的`script`标签以指向名为`prjs8_1.js`的外部 JavaScript 文件。
2. 创建一个外部 JavaScript 文件并保存为`prjs8_1.js`。将其用于第 3–5 步。
3. 创建一个名为`computer`的对象，它具有三个属性：值为 "4GHZ" 的`speed`，值为 "500GB" 的`hd`以及值为 "8GB" 的`ram`。使用对象字面量表示法。
4. 以此格式在页面上显示每个属性的值：

Computer Speed: speed value

Computer Hard Disk: hd value

Computer RAM: ram value

完成后，你的 JavaScript 文件看起来如下：

```javascript
let computer = {
  speed: "4GHZ",
  hd: "500GB",
  ram: "8GB"
}
document.write("Computer Speed: " + computer.speed + "<br>");
document.write("Computer Hard Disk: " + computer.hd + "<br>");
document.write("Computer RAM: " + computer.ram + "<br>");
```

5. 保存 JavaScript 文件并在浏览器中查看 HTML 文件。你应该能看到你创建的计算机对象的属性列表。

### 练习总结

在这个项目中，你能够利用关于对象的新知识，使用对象字面量表示法创建一个带有属性的对象。你还创建了一个可以在浏览器中显示计算机属性的 Web 页面。

# 对象结构

当你以特定方式编写对象时，你可以构建一个作为其他对象结构或模型的对象。为了理解其工作原理，你将学习构造函数（constructor functions）并学习原型（prototypes）的使用方法。

# 构造函数

构造函数可以用于为对象创建可用的代码。例如，你可以通过一个构造函数创建一个`Car`对象，这允许其代码被复用用于任意类型的汽车。你可以有一辆工作用车、家庭用车和娱乐用车，它们都具有构造函数中定义的相同属性和方法名，同时向它们传递不同的值。

例如，要创建一个构造函数，你会创建一个名为`Car()`的函数，并在函数内部添加你的属性/或方法。以下示例显示了`Car()`构造函数的轮廓：

```javascript
function Car() { // 构造函数已定义。
  Properties/Methods go here. // 属性和方法将列在这里
  用于你正在创建的对象。
}
```

注意函数名以大写字母 (C) 开头。虽然这不是强制，但习惯上构造函数的名称以大写字母开头，以将其与其他类型的函数区分开。

## 202 JavaScript: 初学者指南

为了完成前面的函数，你需要将属性添加到函数中。假设你想创建一个具有`seats`、`engine`和`radio`属性的`car`对象。以下代码显示了如何实现：

```javascript
function Car(seats, engine, radio) { // 函数接收三个参数。
  this.seats = seats;
  this.engine = engine;
  this.radio = radio; // 参数值被赋值给对象的属性。
}
```

在代码中，在第一行，你看到参数的值被赋值为属性值；但是，有一个名为`this`的新关键字。JavaScript 中的该关键字用于表示当前正在使用的对象，或者通俗地说“这个对象”。你将看到它是如何工作并为其他对象创建结构的。注意，构造函数不需要`return`语句。

一旦你用构造函数设置了对象的属性，你就需要创建该对象的实例才能使用它；构造函数只创建对象的实例。要创建对象的实例，你使用另一个 JavaScript 关键字：`new`。你之前在数组中使用过它。数组在 JavaScript 中也是对象，因此使用`new Array()`会创建一个 JavaScript 数组的实例。

使用`new`关键字创建你的`Car`对象实例的示例如下代码所示：

```javascript
let work_car = new Car("cloth", "V-6", "Tape Deck");
```

## 204 JavaScript: 初学者指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_222_0.png)

**图 8-1** 你从每种汽车中喜爱的特征显示在浏览器中。

该脚本的结果如图 8-1 所示。

### 属性值

虽然这并不是房地产，但你可以更改你的属性值。在脚本中，你可以通过给对象分配一个新值来动态更改对象的值，就像操作变量一样。例如，如果你想更改之前示例中`work_car.engine`属性的值，只需为其分配一个你选择的新值即可。下面的示例了如何给`work_car.engine`属性分配新值：

```javascript
work_car.engine = "V-4";
```

虽然这可能不是件好事，但它可以帮你省下保险费（以及油费）！

需要注意的是，之前的赋值仅在更改之后才会改变`work_car.engine`属性的值。在更改之前执行的任何操作都不会受到影响。

例如，以下代码为`work_car.engine`属性赋予了新的赋值：

```javascript
function Car (seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
let work_car = new Car("cloth", "V-6", "Tape Deck");
let fun_car = new Car("leather", "V-8", "CD Player");
let original_work_car_engine = work_car.engine;
work_car.engine = "V-4";
let new_work_car_engine = work_car.engine;
document.write("I wanted a " + original_work_car_engine + " initially.<br>");
document.write("I got a " + new_work_car_engine + " instead of lower gas costs.");
```

- `work_car.engine`的原始值被赋值给一个变量。
- `work_car.engine`的值被更改了。
- `document.write()`语句中显示了原始值和新值。
- `work_car.engine`的新值被赋值给一个变量。

# 第8章：对象 205

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_223_0.png)

**图 8-2** 属性值的变化影响更改之后使用它的语句，但不会影响更改之前的语句。

`work_car.engine`属性最初被设置为 "V-6"，但后被改为 "V-4"。当它被赋值给`original_work_car_engine`变量时，它是 "V-6"，且该变量保留了该值。更改后，新值被赋值给`new_work_car_engine`，它使用了 "V-4" 这个新值。图 8-2 显示了在浏览器中运行此脚本的结果。

### 添加方法

要向构造函数添加一个方法，你可以在下面的代码中将函数表达式赋值给属性名：

```javascript
function Car(seats, engine, radio) {
this.seats = seats;
this.engine = engine;
this.radio = radio;
this.describe = function() {
  document.write("This amazing car has these features: ");
  document.write(this.seats + " seats, " + this.engine + " engine, ");
  document.write(this.radio);
}
}
```

> 为 Car 构造函数添加了一个方法`describe()`。

```javascript
let work_car = new Car("cloth", "V-6", "Tape Deck"); //work_car 是 Car 的实例
work_car.describe();
```

如你所见，一旦有了对象的实例，就可以使用实例名、点和方法名来调用该方法。当为`work_car`实例调用方法时，页面上显示字符串 "This amazing car has these features: cloth seats, V-6 engine, Tape Deck"。

虽然向构造函数添加方法非常直接，但在构造函数内部包含方法也有其缺点。对于对象的每个实例，都会创建一个执行相同操作的新函数。实际上，该方法被复制了多次，尽管在代码中没有直接看到它。

正如你所看到的，构造函数内部的方法仅仅是另一个属性。每个属性对于每个实例都是唯一的，方法函数对于每个实例也是唯一的。如果你有 50 个`Car`对象的实例，那么将创建 50 个函数，消耗资源。

## JavaScript：初学者指南

为了使其成为一个简单复用的单一函数，你可以将方法函数移动到构造函数外部，如下代码所示：

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
  this.describe = describe_car;
}

function describe_car() {
  document.write("This amazing car has these features: ");
  document.write(this.seats + " seats, " + this.engine + " engine, ");
  document.write(this.radio);
}

let work_car = new Car("cloth", "V-6", "Tape Deck");
```

在这里，构造函数外部定义了一个具名函数`describe_car`，允许将其赋值给构造函数内部的属性作为方法。注意在赋值时没有括号`()`，这样是将函数本身而非函数的结果赋值给属性。当创建实例并运行方法时，你将获得之前相同的结果，因此操作是成功的。

然而，这种技术也有缺点，因为函数现在是全局的，这会使全局作用域充斥大量函数。要修复这个问题，你需要学习原型（prototype）。

### 使用原型

JavaScript 中的每个函数都有一个名为`prototype`的属性，它是一个包含了每个实例始终可用的属性和方法的对象。这允许代码轻松复用属性和方法。

### 与原型工作

为了了解原型如何工作，你可以使用对象的`prototype`属性。考虑以下代码：

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
Car.prototype.locks = "automatic";
```

注意`Car`有一个原型 (`Car.prototype`)。由于原型是一个对象，你可以像操作其他对象一样向原型添加属性。那么，这样做具体是什么？如果你添加了`Car`的实例，你会发现每个实例都可以访问`locks`：

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
Car.prototype.locks = "automatic";
let work_car = new Car("cloth", "V-6", "Tape Deck");
let family_car = new Car("cloth", "V-4", "CD Changer");
window.alert(work_car.locks);
window.alert(family_car.locks);
```

所有的警告都会显示 "automatic"，这不在`Car`构造函数中，而是在`Car`的原型中。这是如何发生的？在 JavaScript 中，调用对象的属性或方法会首先检查对象本身。如果没有找到该属性或方法，它不会直接放弃，而是会搜索对象的原型查看是否有匹配项。如果是，那么该属性或方法对于尝试使用它的对象就是可用的。例如，图 8-3 显示了`work_car`实例是如何检查`locks`属性的。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_225_0.png)

**图 8-3** 查找`locks`属性

对于原型中具有相同名的实例，属性将始终对象中找到，而不会搜索原型。例如，看以下代码：

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
```

为`work_car`实例添加`locks`属性

```javascript
Car.prototype.locks = "automatic";
let work_car = new Car("cloth", "V-6", "Tape Deck");
let family_car = new Car("cloth", "V-4", "CD Changer");
work_car.locks = "manual";
window.alert(work_car.locks);
window.alert(family_car.locks);
```

- 警告 "manual"
- 警告 "automatic"

给`work_car.locks`赋值确保了`locks`属性在`work_car`实例中找到且不会搜索原型。由于这没有影响其他实例，`family_car.locks`将具有值 manual，必须搜索原型才能找到值，而这个值仍然是 "automatic"。

## hasOwnProperty() 方法

有时你想知道一个属性是在对象中使用还是在原型中使用。对象的`hasOwnProperty()`方法在实例中找到属性时返回`true`，否则返回`false`。在示例中，`work Car`实例有一个`locks`属性，而`family_car`实例没有（它只在原型中有一个`locks`属性）。考虑以下代码：

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
```

```javascript
Car.prototype.locks = "automatic";
let work_car = new Car("cloth", "V-6", "Tape Deck");
let family_car = new Car("cloth", "V-4", "CD Changer");
work_car.locks = "manual";
window.alert(work_car.hasOwnProperty("locks")); // true
window.alert(family_car.hasOwnProperty("locks")); // false
```

在这里，第一个警告显示`true`，而第二个显示`false`。你将在稍后章节看到，这在使用`for-in`循环且只想使用实例中的属性而不是其原型中的属性时非常有用。

## 使用原型处理方法

由于原型位于对象的构造函数外部，且不在全局作用域中，它为在每个实例间共享的方法函数提供了一个良好的位置。你现在可以为每个实例获取其属性（如果它们将具有独特的值）。

## 第8章：对象 209

在构造函数中定义它并将其放置在原型中，以便在所有实例中重用。由于上述原因，这是创建自定义对象的一种常用模式，通常称为组合构造函数/原型模式。

例如，下面的代码将继续向`Car`构造函数添加属性，但将向`Car`原型添加一个方法：

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
Car.prototype.describe = function() {
  document.write("This amazing car has these features: ");
  document.write(this.seats + " seats, " + this.engine + " engine, ");
  document.write(this.radio);
}
```

`Car`构造函数定义了实例属性。

```javascript
let work_car = new Car("cloth", "V-6", "Tape Deck");

work_car.describe();
```

`describe()`方法可以用于`Car`对象的任何实例。

构造函数/原型模式后，代码现在允许将实例属性和方法作为共享属性和方法。当你继续阅读本书时，你将看到更多的原型以及它们如何用于面向对象编程的继承。

### `class` 关键字

ECMAScript2015 引入了`class`关键字，以便你可以定义一个看起来像传统类的对象。底层的基于原型结构仍然存在，但`class`关键字允许你组织代码，使得所有属性和方法都在类的代码块内（而不是将方法放在对象定义之外）。

例如，要创建一个带有构造函数和方法的类，请使用以下代码：

```javascript
class Car {
  constructor(seats, engine, radio) {
    this.seats = seats;
    this.engine = engine;
    this.radio = radio;
  }
  describe() {
    document.write("This amazing car has these features: ");
    document.write(this.seats + " " + this.engine + " engine, ");
    document.write(this.radio);
  }
}
```

`Car`是使用类声明定义的。

构造函数接收并定义了该类（对象）的属性。

定义了`describe()`方法。

// 类声明结束

```javascript
let work_car = new Car("cloth", "V-6", "Tape Deck");

work_car.describe();
```

创建了`Car`类的一个新实例，并为新实例调用了`describe()`方法。

## 210 JavaScript：初学者指南

注意，类可以使用类声明来定义，这与函数定义相似。一个关键区别在于，函数声明会被提升（允许即使在代码中调用函数的位置在函数声明之前，也可以调用该函数），而类声明不会被提升。这意味着你需要确保在创建这些类的实例之前，先在代码中放置任何相关声明。

如果你愿意，可以通过使用类表达式来定义类来利用类表达式的提升（其工作方式更像函数表达式）。由于函数表达式和类表达式都不是提升的，对于任何不习惯新类的人来说，都是显而易见的。下面的代码展示了使用类表达式实现相同代码示例：

```javascript
let Car = class {
  constructor(seats, engine, radio) {
    this.seats = seats;
    this.engine = engine;
    this.radio = radio;
  }
  describe() {
    document.write("This amazing car has these features: ");
    document.write(this.seats + " " + this.engine + " engine, ");
    document.write(this.radio);
  }
};
let work_car = new Car("cloth", "V-6", "Tape Deck");
work_car.describe();
```

> 使用类表达式来定义`Car`类。

> 类表达式结束。在这种情况下别忘记分号！

除了语法差异，其余代码将以相同的方式运行。如果你的用户环境支持 ECMAScript 2015 或更高版本，可以使用`class`作为一种方便的方法来在一个地方组织你的对象代码。只需记住，这只是语法上的差异——底层代码仍然使用构造函数并将方法放置在原型上。

### 对象的有用语句

JavaScript 允许你使用`for-in`循环遍历对象属性，并使用`with`语句轻松地访问特定对象。

### `for-in` 循环

`for-in`循环允许你遍历对象的属性。下面的代码显示了`for-in`循环的结构：

```javascript
for (let variable_name in object_name) {
  JavaScript statements
}
// JavaScript goes here.
```

> 循环开始通过命名一个变量来表示对象中的属性名，以及对象的名称。

假设你想遍历`Car`对象的`work_car`实例的属性，以便在页面上显示每个属性的值。`for-in`循环允许你这样做，而无需输入每个属性名称，如下所示：

## 第 8 章：对象 211

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
let work_car = new Car("cloth", "V-6", "Tape Deck");
for (let prop_name in work_car) {
  // JavaScript statements
}
```

### `with` 语句

JavaScript 允许你使用`for-in`循环遍历对象属性，并使用`with`语句轻松地访问特定对象。

### 警告

使用`with`通常不被建议，因为性能问题以及全局变量可能会被赋值。它在启用`"use strict"`模式下不受支持。

使用`with`的示例：

```javascript
function Car(seats, engine, radio) {
  this.seats = seats;
  this.engine = engine;
  this.radio = radio;
}
let work_car = new Car("cloth", "V-6", "Tape Deck");
with (work_car) {
  document.write(seats + "<br>");
  document.write(engine + "<br>");
  document.write(radio);
}
```

### 专家问

当你已经了解了如何创建对象、属性和方法后，你可以更好地理解一些预定义对象是如何工作的。许多预定义对象将在章节的剩余部分进行讨论。

**Q：当我需要一个时，我真的需要使用构造函数创建一个对象的实例吗？**

**A：是的。构造函数只是为浏览器提供了对象的结构。为了使用它，你需要创建对象的实例。你需要创建一些预定义对象的实例。**

**Q：那么单例呢？我不需要为它们创建实例吗？**

**A：单例不需要创建实例。每个都是唯一的，且之间不复用代码。**

**Q：可以使用组合构造函数/原型模式共享属性以及方法吗？**

**A：是的，如果你不希望每个实例都有唯一的属性值，可以将它们添加到原型上，以便与其他对象实例共享。**

### 练习组合构造函数/原型模式

假设你决定选择某些类型的电脑：工作电脑、家用电脑和游戏电脑。对于每种电脑，将会有不同的属性和一个显示方法。

### 步骤

1. 创建一个 HTML 页面并保存为`pr8_2.html`。
2. 创建一个外部 JavaScript 文件并保存为`prjs_2.js`。我们将其用于步骤 3-8。
3. 创建一个`Computer`构造函数，并赋予它`type`、`processor`、`ram`和`hd`属性。
4. 创建一个名为`work_computer`的`Computer`实例。`type`的值为 “Work”，`processor`的值为 “2GHZ”，`ram`的值为 “8GB”，`hd`的值为 “1TB”。
5. 创建名为`home_computer`的 Computer 实例。`type`的值为 "Home"，`processor`的值为 "2GHZ"，`ram`的值为 "4GB"，且`hd`的值为 "500GB"。
6. 创建名为`gaming_computer`的 Computer 实例。`type`的值为 "Gaming"，`processor`的值为 "4GHZ"，`ram`的值为 "16GB"，且`hd`的值为 "2TB"。
7. 在 Computer 原型上创建一个名为`describe`的方法。使用它在页面上显示每个属性的值。
8. 当你完成后，你的 JavaScript 文件应该像这样：

```javascript
function Computer(type, processor, ram, hd) {
  this.type = type;
  this.processor = processor;
  this.ram = ram;
  this.hd = hd;
}
Computer.prototype.describe = function() {
  document.write("<p>" + this.type + ":<br>");
  document.write("Processor: " + this.processor + ":<br>");
  document.write("RAM: " + this.ram + ":<br>");
  document.write("Hard Disk: " + this.hd + "</p>");
}
let work_computer = new Computer("Work", "2GHZ", "8GB", "1TB");
let home_computer = new Computer("Home", "2GHZ", "4GB", "500GB");
let gaming_computer = new Computer("Gaming", "4GHZ", "16GB", "2TB");
work_computer.describe();
home_computer.describe();
gaming_computer.describe();
```

9. 保存文件并在浏览器中打开 HTML 文件。每个实例的属性都应该显示出来。

### 尝试总结

在这个项目中，你利用了关于构造函数和原型的知识来创建一个可复用的对象，该对象在其原型上有一个方法，可以显示该对象的任何实例的属性值。

# 理解预定义的 JavaScript 对象

在 JavaScript 中，有许多预定义的对象可以使用来访问你可能需要的某些属性或方法。一旦你学习了各种对象以及可以使用它们做什么，你就可以让你的脚本更具交互性。

## JavaScript：初学者指南

本书将涵盖许多主要的预定义对象。在本章中，我们将查看 navigator 和 history 对象，以及你可以用它们做什么。

### Navigator 对象

navigator 对象让你能够访问查看浏览器的各种属性，例如它的名称、版本号等。它的名字源于 Netscape Navigator 浏览器，它是 Mozilla Firefox 之前的浏览器。

navigator 对象是 window 对象的一部分，你可以通过`navigator.property`访问它的属性，但也可以简单地简写为`navigator.property`。对于 window 对象的直接属性和方法也是如此（例如，`window.alert("Hi")`可以简写为`alert("Hi")`且依然有效）。你经常会看到 window 对象的此类属性和方法这样简写，以节省输入量或帮助缩短源代码。你将在第 11 章中看到更多原因。

首先，看看 navigator 对象的属性。

### 属性

navigator 对象的属性是不能更改的，因为它们被设置为只读。表 8-1 显示了 navigator 对象的属性以及每个属性返回的值。当在括号中显示浏览器名称时，意味着该属性在本文编写时仅在特定的浏览器中有效。

接下来的章节将详细查看一些最实用的属性。

### appName 属性

这允许你确定查看器正在使用的浏览器名称。如果你想知道特定浏览器的值，可以使用以下代码并在你选择的浏览器中打开页面：

```javascript
window.alert("You have " + navigator.appName);
```

该属性在过去经常被用于创建一个简单的浏览器检测脚本，例如代码所示：

```html
<script>
if (navigator.appName == "Microsoft Internet Explorer") {
  //  IE 浏览器的代码
} else {
  document.write("请获取 Internet Explorer 以运行此脚本");
}
</script>
<noscript>你没有启用 JavaScript。请获取 Internet Explorer!</noscript>
```

虽然这在一段时间内是用的，但对于你可能会遇到的各种浏览器有更好的方法，例如特性检测和渐进式增强，随着本书的阅读，你将学习更多知识。

### 第 8 章：对象 215

| 属性 | 值 |
| --- | --- |
| `appCodeName` | 浏览器的代号 |
| `appMinorVersion` | 表示浏览器次版本的字符串（Internet Explorer 和 Opera） |
| `appName` | 浏览器的全名 |
| `appVersion` | 浏览器的版本及其他信息 |
| `browserLanguage` | 使用的操作系统的语言（Internet Explorer 和 Opera） |
| `buildID` | 正在使用的浏览器构建器（Firefox） |
| `cookieEnabled` | 指定浏览器是否启用了 cookies |
| `cpuClass` | 用户电脑上的 CPU（Internet Explorer） |
| `language` | 正在使用的浏览器语言（Firefox, Chrome 和 Opera） |
| `mimetypes` | 浏览器支持的 MIME 类型数组 |
| `onLine` | 指定当前是否是“全局离线模式”（Internet Explorer, Firefox 和 Opera） |
| `oscpu` | 操作系统 |
| `platform` | 机器类型 |
| `plugins` | 插件数组 |
| `product` | 产品名称 |
| `productSub` | 产品版本 |
| `securityPolicy` | 安全策略 |
| `systemLanguage` | 系统的语言 |
| `userAgent` | 用户代理字符串 |
| `userLanguage` | 界面语言 |
| `userProfile` | 用户配置 |
| `vendor` | 供应商 |
| `vendorSub` | 版本号 |

**表 8-1 Navigator 对象的属性**

navigator 对象的属性不能更改，因为它们被设置为只读。`cookieEnabled`属性返回一个布尔值，表示浏览器是否启用了 cookies；否则返回 false。你可以用它来避免在用户没有 cookie 时运行代码：

```javascript
if (navigator.cookieEnabled) {
  // 设置 cookie
}
```

这允许你。你将在本书后面详细介绍 cookie。

### 216 JavaScript：初学者指南

| 方法 | 目的 |
| --- | --- |
| `javaEnabled()` | 测试浏览器是否启用了 Java |
| `preference()` | 设置某些浏览器偏好。特权模式（Firefox） |
| `registerContentTypeHandler` | 允许网站将其设置为特定 MIME 类型的处理器 |
| `registerProtocolHandler()` | 允许网站将其设置为特定协议的处理器 |
| `taintEnabled()` | 返回 false——因为该方法已不再使用。它曾用于指定是否启用了数据污染 |

**表 8-2 Navigator 的方法**

`plugins`属性 此数组包含了查看器浏览器中安装的所有插件的值。这可以用于检测查看器是否有特定的插件用于运行代码。

### 方法

navigator 对象还拥有许多方法可以执行各种任务。表 8-2 显示了 navigator 可用的方法以及如何使用。

`javaEnabled()`方法 如果查看器启用了 Java，该方法返回 true；否则返回 false。如果你想向查看器显示 Java applet，但前提是查看器启用了 Java，那么`javaEnabled`方法可能有用。以下代码允许你：

```javascript
if (navigator.javaEnabled()) {
  // 插入 Java Applet
}
else {
  document.write("没有 Java？你无法看到我的 Java Applet!");
}
```

这测试了`navigator.javaEnabled()`方法返回的值，要么显示 Java applet，要么告知用户未启用 Java。

### History 对象

history 对象也是 window 对象的一部分，提供了当前窗口的浏览器历史信息。

### 属性

history 对象只有一个属性，名为`length`（在 Firefox 中有几个可用的，但它们不与 Web 内容配合）。该属性返回历史中的页面数量。

# 第 8 章 对象 217

| 方法 | 用途 |
| --- | --- |
| `back()` | 将浏览器窗口返回到历史列表中的上一页 |
| `forward()` | 将浏览器发送到历史列表中的下一页 |
| `go()` | 使用整数将浏览器发送到历史列表中的指定页面 |

**表 8-3** 历史对象的方法

当前窗口的浏览器会话历史，其中包含当前加载的页面。它可以以类似下面的方式使用：

```javascript
alert("Your current window has viewed " + history.length + " pages!")
```

这只是向查看者发送一个警报框，告知当前浏览器窗口中访问了多少页面。

## **方法**

历史对象有三个实用的方法，如表 8-3 所示。

接下来的章节将详细讨论这些每种方法。你可以在 developer.mozilla.org/en-US/docs/Web/API/History 查看额外的属性和方法。

`back()`方法 `back()`方法将浏览器发送到当前页面之前历史记录中最后访问的页面，类似于使用浏览器的“后退”按钮。要使用它，只需在脚本需要的地方调用该方法：

```javascript
history.back();
```

`forward()`方法 `forward()`方法将浏览器发送到历史列表中当前页面之后访问的页面，类似于使用浏览器的“前进”按钮。要使用它，只需在脚本需要的地方调用该方法：

```javascript
history.forward();
```

`go()`方法 `go()`方法接受一个整数作为参数。该整数可以是负数以便在历史列表中后退，也可以是正数以便在历史列表中向前移动。例如，以下代码将窗口历史记录向后退两页：

```javascript
history.go(-2);
```

以下代码将向历史列表向前移动三页：

```javascript
history.go(3);
```

与另外两个方法一样，如果查看者尝试访问的页面不存在（例如，`history.go(15)`这样的页面可能不在窗口历史记录中），则该方法将什么都不做。

## JavaScript：初学者指南

预定义的 JavaScript 对象非常有帮助。正如你将在下一章看到的，文档对象（document object）让你能够访问处理 HTML 文档的许多额外属性和方法。

### 第 8 章自测

1. 对象是 ________ 和 ________ 的集合。
2. 在创建单个对象时，你可以使用对象 ________ 或字面量表示法。
3. 使用字面量表示法时，属性和值包含在大括号（{}）中。
   - A. 正确
   - B. 错误
4. 在 JavaScript 中，你通常通过使用 ________ 访问对象属性
   - A. 加法运算符 (+)
   - B. 点运算符 (.)
   - C. 乘法运算符 (*)
   - D. 你无法访问对象的属性
5. 当你需要使用变量来访问属性名时，你可以使用 ________ 表示法。
6. 可以使用 ________ 来创建对象结构。
7. 使用`new`关键字可以创建一个对象的一个 ________。
8. 你只能有一个对象的实例。
   - A. 正确
   - B. 错误
9. 对于以下代码你可以怎么说：

```javascript
let x = myhouse.kitchen;
```

   - A. 它将字符串`myhouse.kitchen`赋值给变量`x`。
   - B. 它将`myhouse`的值相加并赋值给名为`x`的对象。
   - C. 假设`myhouse`对象存在，它将`myhouse`对象的`kitchen`属性的值赋值给变量`x`。
   - D. 假设`kitchen`对象存在，它将`kitchen`对象中`myhouse`属性的值赋值给变量`x`。
10. 如果在对象实例中找不到属性，JavaScript 将在对象的 ________ 中查找。
11. 下列哪项会向查看者发送警报告知使用的浏览器名称？
    - A. `window.alert("You are using " + navigator.appVersion);`
    - B. `window.alert("You are using " + navigator.appName);`
    - C. `window.alert("You are using " + navigator.javaEnabled());`
    - D. `window.alert("You are using navigator.appName");`
12. 对于以下代码你可以怎么说？

```javascript
myhouse.kitchen = "big";
```

   - A. 假设`kitchen`对象存在，`myhouse`属性被分配了一个新的字符串值。
   - B. 假设`myhouse`对象存在，变量`kitchen`的值与字符串`big`相加。
   - C. 假设`myhouse`对象存在，`kitchen`属性被分配了新的字符串值`"big"`或被用值`"big"`初始化。
   - D. 这将什么都不做。
13. 在 JavaScript 中，有许多 ________ 对象可以使用来访问你可能需要的某些属性和方法。
14. ________ 对象让你能够访问查看者浏览器的各种属性。
15. 下列哪项不是 navigator 对象的属性？
    - A. `appName`
    - B. `appCodeName`
    - C. `appType`
    - D. `appVersion`

# 第 9 章

## 文档对象

### 关键技能与概念

- 定义文档对象
- 使用文档模型
- 使用文档对象的属性
- 使用节点（Nodes）
- 创建动态脚本

预定义的 JavaScript 对象非常有帮助。正如你将在下一章看到的，文档对象（document object）让你能够访问处理 HTML 文档的许多额外属性和方法。

### 定义文档对象

文档对象（DOM）允许 JavaScript 和其他脚本语言访问文档的结构。每个文档由节点组成（例如，body 标签是一个节点，body 内部的元素是 body 的子节点）。通过这种结构，脚本语言可以以许多方式访问文档中的元素。

现在你已经了解了对象，是时候看看文档了。文档对象让你能够访问处理 HTML 文档的许多额外属性和方法。

### 使用文档模型

文档对象模型（DOM）允许 JavaScript 和其他脚本语言访问文档的结构。每个文档由节点组成（例如，body 标签是一个节点，body 内部的元素是 body 的子节点）。通过这种结构，脚本语言可以以许多方式访问文档中的元素。

如果你有以下 HTML 代码，可以使用 JavaScript 访问其结构：

```html
<body>
  <h1>My Page</h1>
  <img src="myimage.jpg" alt="My Picture">
</body>
```

图 9-1 显示了 body 元素是一个节点，以及它如何拥有子节点和属性节点。

## 使用文档对象的属性

文档对象让你能够访问查看者浏览器的各种属性。本章涵盖了文档对象，你将了解到更多。预定义的 JavaScript 对象非常有帮助。正如你将在下一章看到的，文档对象是唯一的。

> 注意

> DOM 是浏览器环境特有的。此外，某些非标准的 DOM 方法可能在特定浏览器中有效，因此你通常希望坚持那些适用于所有浏览器的方法。

## 第 9 章：文档对象 223

| `<body>` |
| `<h1>` (body 的子节点) | `<img>` (body 的子节点) |
| My Page (h1 的子节点) | src="myimage.jpg" --- alt="My Picture" (img 的属性节点) |

**图 9-1** 文档部分的示例

### JavaScript: 入门指南

| 属性 | 描述 |
| :--- | :--- |
| `activeElement` | 返回活动（聚焦）的元素 |
| `all` | 获取文档中的所有节点 |
| `baseURI` | 返回代表文档 URI 的对象。仅在特权模式下可用 |
| `body` | 返回文档的 body 元素或 frameset 元素 |
| `charset` | 返回文档中使用的字符集 |
| `compatMode` | 如果文档在怪异模式（Quirks mode）下渲染，返回字符串 "BackCompat"如果在严格模式（Strict mode）下渲染，返回字符串 "CSS1" |
| `contentType` | 返回文档 MIME 头部中的 Content-Type 值 |
| `cookie` | 返回或设置文档中的 JavaScript cookie |
| `currentScript` | 返回当前正在读取的脚本元素 |
| `defaultValue` | 返回文档的 window 对象 |
| `designMode` | 允许文档进行编辑 |
| `dir` | 返回或设置文档的方向 |
| `doctype` | 返回与文档关联的 doctype 声明 |
| `documentElement` | 返回代表文档根节点的字符串 |
| `documentMode` | 返回文档的兼容模式 |
| `documentURI` | 返回文档的位置 |
| `domain` | 返回文档所在服务器的域名 |
| `embeds` | 返回文档中所有 embeds 元素的数组 |
| `forms` | 返回文档中所有表元素的数组 |
| `fullscreenEnabled` | 返回浏览器是否支持全屏 |
| `head` | 返回文档的 head 元素 |
| `images` | 返回文档中所有 (img) 元素的数组 |
| `implementation` | 返回文档的实现对象 |
| `inputEncoding` | 返回代表文档编码的字符串 |
| `lastModified` | 返回文档最后修改的日期 |
| `lastStyleSet` | 使用 selectedStyleSheet 属性返回最近使用的样式表名称 |
| `links` | 返回文档中所有超链接`<a>`元素的数组 |

表 9-1 文档对象属性（续）

| 属性 | 描述 |
| :--- | :--- |
| `location` | 返回文档的 URI |
| `namespaceURI` | 返回文档的 XML 命名空间 |
| `parentWindow` | 返回父窗口的引用（父窗口的 document 对象） |
| `plugins` | 返回文档中使用的所有插件的数组 |
| `preferredStyleSheet` | 根据文档中样式表的声明顺序返回首选样式表 |
| `protocol` | 返回文档 Web 地址（URL）的协议 |
| `readyState` | 返回文档的加载状态 |
| `referrer` | 返回引导访问当前文档的文档 URL |
| `scripts` | 返回文档中使用的所有元素的数组 |
| `scrollingElement` | 返回滚动的元素，通常是根元素 |
| `selectedStyleSet` | 返回或设置当前的样式表集 |
| `styleSheets` | 返回文档中使用的所有样式表的数组 |
| `styleSheetSets` | 返回文档中所有样式表集的数组 |
| `textContent` | 返回或设置文本内容 |
| `title` | 返回文档标签内部使用的文本 |
| `uniqueID` | 返回为文档生成的唯一 ID |
| `URL` | 返回当前文档的 URL |
| `URLUnencoded` | 返回未编码的文档 URL |
| `xmlStandalone` | 返回或设置 XML 文档声明中的独立值 |
| `XSLDocument` | 返回 XSL 文档的根元素 |

**表 9-1** 文档对象属性

> 注意

并非所有属性在所有浏览器中都能工作。你可以访问 http://developer.mozilla.org/en/DOM/document#Properties 和 https://msn.microsoft.com/en-us/ie/ms535862(v=94) 查看更多信息和额外属性。

### 集合

许多属性（`anchors`、`embeds`、`forms`、`links`、`plugins`、`scripts`、`styleSheets`和`styleSheetSets`）返回一个包含文档中发现的元素或值的数组。可以像访问任何数组一样使用索引进行访问。索引 0 元素是第一个，索引 1 是第二个，依此类推。

例如，`links`属性可以用于访问文档中的所有链接。如果你需要找到文档中的第一个链接，可以使用`document.links[0]`以对象形式访问元素。你可以使用 DOM 节点属性或方法（在本章稍后的部分讨论）来获取或设置信息，或对元素执行操作。

### cookie 属性

`cookie`属性用于设置 JavaScript cookie 以为查看者存储信息。cookie 是保存在查看者本地的持续特定时间（某个日期或浏览器会话）的小文本文件。cookie 有助于网站记住并检索查看者的信息（例如购物车的内容、特殊设置或会话信息）。

要设置 cookie，请将`document.cookie`属性的值设置为一个包含你想要为查看者存储信息的字符串。以下是语法：

```javascript
document.cookie = string;
```

你应当将`string`替换为包含你想要使用的信息的文本字符串。通常，它的格式如下面的设置 cookie 示例所示：

```javascript
document.cookie = "site=homepage";
```

你可以看到有一点：cookie 是`homepage`。请注意，设置 cookie 不会替换整个 cookie；它只是将新字符串添加到其中。你将在后面的章节中学习如何使用高级字符串处理技术以及如何读取 cookie。

### dir 属性

`dir`属性返回一个代表文档方向的字符串。该值可以是 "ltr"（从左到右）或 "rtl"（从右到左）。这对于显示从右到左而非从左到右阅读的语言的网页非常有用。可以通过此属性动态更改页面外观，如下代码所示：

```javascript
document.dir = "rtl";
```

### lastModified 属性

`lastModified`属性持有当前文档最后修改的日期时间。这主要用于信息目的，例如显示文档最后修改的日期，以便查看者知道你何时更新了页面。该属性的值取决于你的浏览器，因为如果你在页面上写入最后修改日期，不同的浏览器会有不同的结果。

考虑以下代码，它将`document.lastModified`属性的值写入网页，以显示最后修改的日期时间：

```html
<body>
<h1>我经常更新的网页！</h1>
<script type="text/javascript">
document.write("Last Updated: " + document.lastModified);
</script>
</body>
```

### referrer 属性

`referrer`属性用于信息目的，并持有查看者在到达你的页面之前所在的页面的 URL（引用页）。虽然这可能有用，但查看者并不总是通过引用 URL 进入的（例如使用书签或输入地址时），因此该值可能为空。此外，该属性的值并不总是准确的，因为不同的浏览器可能考虑不同类型的

## 228 JavaScript：初学者指南

将查看者引导至新页面，而不仅仅是链接，而且用户可能会隐藏或更改引用页（referrer）。

将以下示例中的代码放入文档中，将向页面的查看者发送一个警报，告诉他们在进入你的页面之前在何处：

```javascript
window.alert("You came from " + document.referrer + "!");
```

因此，如果引用页是 http://www.scriptweb.com/js/，则会向查看者发送一个显示“你来自 http://scriptweb.com/js/”的警报。

### title 属性

`title`属性持有 HTML 文档标题的字符串值。标题设置在页面的`<title>`和`</title>`标签内部。

你可以使用该属性的一种方法是在窗口顶部栏的某处向查看者显示页面标题。以下代码将允许你实现这一操作：

```html
<head>
<title>Lions, Tigers and Bears!</title>
</head>
<body>
<script type="text/javascript">
document.write("<h1>" + document.title + "</h1>");
</script>
Lions and tigers and bears were what I saw when I went to . . .
</body>
```

> 文档的标题在此设置

> 标题将作为标题显示给查看者

这会将你的标题作为标题显示在页面上。图 9-4 显示了在浏览器中查看此结果的结果。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_246_0.png)

**图 9-4** 文档标题作为标题显示在页面上。

### URL 属性

`URL`属性持有当前文档完整 URL 的值。如果你将其打印在 HTML 页面的底部，此信息将非常有用，因为它会为任何打印你页面的人显示页面 URL。

虽然你可以自己在自己的页面底部输入 URL，但当需要在许多页面上这样做时，这可能会变得非常麻烦。这就是该属性非常方便的地方，因为你可以将简单的脚本剪切粘贴到每个页面，而不是每次都输入各种 URL 地址。在页面上写入 URL 地址的示例所示：

```html
<body>
<h1>Buy Something!</h1>
If you don't buy something I will be really upset so you had better...<br><br>
<script type="text/javascript">
document.write("You are at: " + document.URL);
</script>
</body>
```

图 9-5 显示了在浏览器中执行上述代码的结果。页面的最后一行告诉查看者当前位置。该图显示的是本地文件地址，但如果页面在线，它将显示普通的 URL。

### URLUnencoded 属性

`URLUnencoded`属性返回不带任何编码的文档 URL。例如，如果文件名包含空格，该属性将返回空格而不是替换为 %20。对于 URL http://scripttheweb.com/my.script.html，`document.URL`属性将返回 http://scripttheweb.com/my%20script.html。而`URLUnencoded`属性返回 http://scripttheweb.com/my/script.html，即未对空格编码的 URL。请注意，在编写本文时，此属性仅在 Microsoft Explorer 中可用。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_247_0.png)

**图 9-5** 文档 URL 显示在页面内容的底部。

## JavaScript：初学者指南

### 专家问答

**问：学习文档对象（document object）和 DOM 对我有帮助吗？**

**答：是的，因为它们不仅为处理 Web 页面，还为处理其他类型的文档提供了基础。例如，其他类型的文档使用类似的节点结构，因此学习它在 HTML 文档中如何工作，对于你需要在另一个平台（如用于 PDF 文件的 Adobe Acrobat）上使用 JavaScript 是很有帮助。**

**问：引用页（referrer）很酷！有没有什么方法可以在每次访客进入时将信息写入文件，以便我知道我的访客是从哪里来的？**

**答：客户端 JavaScript 无法独立地将信息保存到文件中，但可以将信息发送到服务器端程序，在那里它可以存储在文件或数据库中。你将在后面的章节中学习更多关于此的内容（使用 JSON 和 AJAX）。**

**问：除了包含元素集合的数组外，还有其他方法访问文档中的元素吗？**

文档对象的方法（如`getElementById()`）允许你对所选的元素进行更具体的选择。你将在下一节中学习如何使用这些方法。

### 使用文档对象的方法

文档对象的方法允许你执行一些以前无法执行的新操作。表 9-2 列出了常用方法以及对每个方法的简要描述。由于这些方法中的许多是特定于浏览器的（属性也是如此），因此表格之后仅详细描述了某些特定方法。

> 注意

> 并非所有属性在所有浏览器中都能运行。你可以通过访问 http://developer.mozilla.org/en/DOM/document#Methods 查看更多信息和属性。

### get 方法

有许多方法允许你获取一个或多个元素。

| 方法 | 描述 |
| :--- | :--- |
| `adoptNode` | 返回另一个文档的节点 |
| `createAttribute` | 创建名称的属性 |
| `createCDATASection` | 创建 CDATA 段 |
| `createComment` | 创建注释 |
| `createDocumentFragment` | 创建文档碎片 |
| `createElement` | 创建元素 |
| `createElementNS` | 在命名空间创建元素 |
| `createEvent` | 创建事件 |
| `createNodeIterator` | 创建节点迭代器 |
| `createNodeResolver` | 创建节点解析器 |
| `createProcessingInstruction` | 创建处理指令 |
| `createRange` | 创建范围 |
| `createStyleSheet` | 创建样式表 |
| `createTreeWalker` | 创建树遍历器 |
| `elementFromPoint` | 返回位置处的元素 |
| `evaluate` | 根据表达式返回结果 |
| `execCommand` | 在文档上执行命令 |
| `getElementById` | 返回 ID 元素 |
| `getElementsByClassName` | 返回类名的元素集合 |
| `getElementsByName` | 返回名称的元素集合 |
| `getElementsByTagName` | 返回标签名的元素集合 |
| `getElementsByTagNameNS` | 返回标签名和命名空间的元素集合 |
| `getSelection` | 返回选定的文本 |
| `hasFocus` | 根据文档是否有焦点返回布尔值 |

| 方法 | 描述 |
| :--- | :--- |
| `importNode` | 从另一个文档导入节点 |
| `isDefaultNamespace` | 返回命名空间是否为默认 |
| `isEqualNode` | 返回两个节点是否相等 |
| `isSameNode` | 返回两个节点是否指向同一个节点 |
| `load` | 加载 XML 文档 |
| `lookupNamespaceURI` | 返回命名空间 URI |
| `lookupPrefix` | 返回指定前缀的命名空间 |
| `normalize` | 规范文档中的节点 |
| `close` | 关闭通过 open 方法打开的新文档 |
| `open` | 打开一个允许你写入内容的新文档 |
| `queryCommandEnabled` | 根据命令是否可以执行返回布尔值 |
| `queryCommandInd` | 根据命令是否处于不确定状态返回布尔值 |
| `queryCommandState` | 根据命令是否已执行返回布尔值 |
| `queryCommandSupported` | 根据命令是否支持返回布尔值 |
| `queryCommandValue` | 返回命令的当前值 |
| `querySelector` | 返回匹配选择器的第一个元素 |
| `querySelectorAll` | 返回匹配选择器的所有元素节点 |
| `write` | 允许向 HTML 文档写入字符串 |
| `writeln` | 允许向 HTML 文档写入字符串，但在行尾以 JavaScript 换行符结束 |

### getElementById 方法

`getElementById()`方法允许你通过 id 属性访问元素。例如，如果你有以下 HTML 代码，你可以使用`getElementById()`方法访问 div 元素：

```html
<div id="some_text">This is some text.</div>
```

## 第 9 章：文档对象 233

由于 div 元素的 id 属性值为`some_text`，因此`document.getElementById`方法可以使用该值作为参数来访问 div 元素：

```javascript
let text_element = document.getElementById("some_text");
```

合法的 HTML 只允许在单个元素上使用唯一的 ID 值。如果在多个元素上使用了相同的 ID 值，`getElementById`将只会获取使用该 ID 的其中一个元素。在本章的学习中，你将发现可以使用这种方法以及其他选择方法来从元素中检索信息、修改元素或删除元素。

### getElementsByClassName() 方法

该方法允许你获取一个数组，其中包含了文档中所有具有指定类名（来自 CSS 类）的元素。要获取所有类名为`number_one`的元素，你可以使用以下代码：

```javascript
let my_class = document.getElementsByClassName("number_one");
```

### getElementsByName() 方法

该方法允许你获取一个数组，其中包含了文档中所有`name`属性具有指定值的元素。在许多情况下，该值对于某个元素是唯一的。然而，同一组的单选按钮（radio buttons）必须具有相同的名称（这样就只能选择其中一个）。这就是能够检索所有元素的一个场景：

```html
<fieldset>
  <legend>选择一种恐龙：</legend>
  <input type="radio" name="dino" id="dino_enigma" value="Enigmosaurus">
  <label for="dino_enigma">神秘的类型</label>
  <input type="radio" name="dino" id="dino_spino" value="Spinosaurus">
  <label for="dino_spino">脊骨非常发达</label>
  <input type="radio" name="dino" id="dino_xeno" value="Xenotorsaurus">
  <label for="dino_xeno">独特的名称类型</label>
</fieldset>
```

这段 HTML 代码有一组名称均为`dino`的单选按钮。如果你想获取所有这些元素，可以使用以下代码：

```javascript
let dino_radios = document.getElementsByName("dino");
```

这将会将所有名称为`dino`的按钮元素检索到一个数组中，你可以通过循环来执行任何必要的任务：

```javascript
for (let i = 0; i < dino_radios.length; i++) {
  // 执行一些工作...
}
```

如你所见，你现在可以在循环中处理所有元素，而不是通过其 id 一个一个获取来执行相同的任务。

### getElementsByTagName() 方法

该方法允许你获取一个数组，其中包含了文档中所有具有指定标签名的元素。例如，要获取文档中所有的图像元素，必须使用以下代码：

```javascript
let all_images = document.getElementsByTagName("img");
```

### querySelector() 方法

该方法允许你使用 CSS 选择器来获取匹配选择器的第一个元素。例如，你可以通过 ID 获取元素：

```javascript
let mydiv = document.querySelector("#mydiv");
```

注意这里使用了 ID 符号`#`，而`document.getElementById()`则没有使用。CSS 类和其他类型的选择器也是如此。例如，要选择一个类，可以使用以下代码：

```javascript
let header = document.querySelector(".header");
```

记住，`querySelector()`只选择第一个匹配项，即使你有多个具有`header`类的元素，也只会选中第一个带有`header`类的元素。

### querySelectorAll() 方法

与`querySelector`只选择第一个匹配元素不同，`querySelectorAll()`会为提供的 CSS 选择器选择所有匹配元素。例如，考虑以下代码：

```javascript
let headers = document.querySelectorAll(".header");
```



这一次，所有具有`header`类元素都将被选中，而不仅仅是第一个，你可以像之前使用`getElementsByClassName()`那样通过循环访问每个单独的元素：

```
for (let i = 0; i < headers.length; i++) {
// 执行一些工作...
}
```

### 更具针对性的操作

一旦获取了更具体的对象，就可以对它们使用更具针对性的方法。例如，你有以下 HTML 代码：

```html
<nav id="sitelinks">
  <a href="page1.html">页面 1</a>
  <a href="page2.html">页面 2</a>
  <a href="page3.html">页面 3</a>
  <div>
    这里是一些内容，请查看 <a href="someplace.com">我的其他网站！</a>
  </div>
</nav>
```

如果你只想获取`nav`元素中的链接，使用`document.getElementsByTagName("a")`将不起作用，因为你也会获取标签内部的链接（文档的一部分）。要实现这一点，你可以获取第一个`nav`元素，并在为该`nav`元素创建的对象上使用`getElementsByTagName()`方法，如下代码所示：

通过 id 获取`nav`元素：

```
let nav_element = document.getElementById("sitelinks");
let nav_links = nav_element.getElementsByTagName("a");
alert("有 " + nav_links.length + " 个链接。");
```

上面的代码显示了如何在特定元素内查找链接。当你处理复杂的 HTML 结构并需要定位页面特定部分时，这是一种实用的技术。

## 第 9 章：文档对象 (Document Object)

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_255_0.png)

图 9-6 这是允许查看者输入信息的页面。

图 9-7 显示了在文本框中输入名称“John”并点击按钮的结果。出现了一个新页面，并带有欢迎语！

### `write()` 和 `writeln()` 方法

你在书中早期就开始使用`write()`方法，所以你已经知道它是如何工作的了。`document.write()`方法用于在调用它的页面上显示字符串值。`writeln()`方法的作用相同，但在语句末尾添加了一个换行符（`\n`）。回想一下第 3 章讨论过的 JavaScript 换行符的工作原理——它只会在页面源代码中插入新行，而不会影响 HTML 页面的最终显示效果。

> **提示** 虽然换行符在执行`document.write()`时只会影响源代码的显示，但它可以用于在 JavaScript 创建的显示元素中（如`alert`、`prompt`和`confirm`框）创建新行。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_255_1.png)

图 9-7 一旦点击按钮，查看者将获得一个类似于这样的新页面。

# 238 JavaScript：入门指南

页面本身的外观不受 JavaScript 换行符的影响。

回想第 3 章中的示例，该示例使用换行符将代码分成了两个不同的行：

```html
<body>
<script type="text/javascript">
document.write("<strong>JavaScript Rules!</strong>\n This is fun.");
</script>
</body>
```

由于`document.writeln`方法在语句末尾添加了换行符，你可以使用`document.writeln`语句重写上述代码：

```html
<body>
<script type="text/javascript">
document.writeln("<strong>JavaScript Rules!</strong>")
document.writeln("This is fun.");
</script>
</body>
```

这将代码行在页面源代码中放在两个不同的行上，但不会影响浏览器中页面的外观。

### 使用 DOM 节点

文档对象拥有一些方法（如`createElement()`、`createAttribute()`和`createTextNode()`），它们允许你使用 JavaScript 在页面上创建各种元素或节点。然而，为了使用它们，必须将新内容作为 DOM 中现有节点的子添加。这里就需要 DOM 属性和方法了。

### DOM 节点属性

每个 DOM 节点都是一个具有可以访问的属性和方法的对象。表 9-3 列出了 DOM 节点、HTML 元素和元素属性。

当表 9-3 提到指定节点时，操作方式与你之前章节中处理元素相同。例如，你可能有如下 HTML 代码：

```html
<body>
<div id="div1" title="All about me!">
This page is about me, me, and... me!
</div>
</body>
```

## 第 9 章：文档对象 239

| 属性 | 描述 |
|---|---|
| attributes | 返回指定节点中所有属性的数组 |
| baseURI | 返回节点的基 URI |
| childElementCount | 返回作为元素的子节点数量 |
| childNodes | 返回指定节点的所有子节点的数组 |
| children | 返回指定节点的所有子元素的数组 |
| classList | 返回元素`class`属性中的类列表 |
| className | 返回元素`class`属性的值 |
| clientHeight | 返回元素的高度（像素为单位） |
| clientWidth | 返回元素的宽度（像素为单位） |
| clientLeft | 返回元素左边框宽度（像素为单位） |
| clientTop | 返回元素上边框宽度（像素为单位） |
| contentEditable | 返回元素是否可编辑 |
| dataset | 访问元素的自定义数据属性 |
| dir | 返回指定节点中文本方向的值 |
| firstChild | 返回指定节点的第一个子节点 |
| firstElementChild | 返回指定节点的第一个直接子元素 |
| id | 返回指定节点的 id |
| innerHTML | 返回或设置指定节点内的 HTML 代码 |
| innerText | 返回或设置指定节点的内部文本 |
| isConnected | 返回节点是否已附加到 DOM |
| isContentEditable | 返回元素的内容是否可以编辑 |
| lang | 返回指定节点的语言值 |
| lastChild | 返回指定节点的最后一个子节点 |
| lastElementChild | 返回指定节点的最后一个直接子元素 |
| localName | 返回节点名的本地部分 |
| name | 返回指定元素的 name 属性 |
| namespaceURI | 返回指定节点的命名空间 URI |
| nextSibling | 返回指定节点之后的节点 |
| nextElementSibling | 返回与指定节点同层的下一个元素 |

表 9-3 DOM 节点属性（续）

### JavaScript：入门指南

| 属性 | 描述 |
|---|---|
| nodeName | 返回指定节点的名称 |
| nodeType | 返回节点的类型 |
| nodeValue | 返回指定节点的值 |
| outerHTML | 返回或设置指定节点的外部 HTML 代码 |
| ownerDocument | 返回包含该节点的文档 |
| parentElement | 返回指定节点的父元素 |
| parentNode | 返回指定节点的父节点 |
| prefix | 返回指定节点的前缀 |
| previousElementSibling | 返回指定节点之前的元素 |
| previousSibling | 返回指定节点之前的节点 |
| scrollLeft | 返回节点的左滚动位置 |
| scrollTop | 返回节点的顶滚动位置 |
| scrollHeight | 返回指定节点的高度 |
| scrollWidth | 返回指定节点的宽度 |
| style | 返回节点的样式对象 |
| tabIndex | 返回节点的选项索引 |
| tagName | 返回大写的标签名 |
| textContent | 返回或设置节点的文本内容 |
| title | 返回 title 属性的值 |

## 242 JavaScript：初学者指南

| 方法 | 描述 |
|---|---|
| addEventListener() | 在指定的节点上添加事件监听器，以便在发送给该节点的事件作为参数时运行函数 |
| appendChild() | 将节点作为最后一个子节点添加到指定的节点中 |
| attachEvent() | 在指定的节点上绑定事件，以便在发送给该节点的事件作为参数时运行函数 |
| blur() | 移除指定节点的焦点 |
| click() | 在指定节点上执行点击事件 |
| cloneNode() | 创建该节点的克隆 |
| compareDocumentPosition() | 返回一个数字，表示该节点与作为参数传递的节点之间的位置关系 |
| detachEvent() | 从指定节点上解绑事件 |
| dispatchEvent() | 在指定节点上执行事件 |
| focus() | 给指定节点赋予焦点 |
| getAttribute() | 返回作为参数传递的属性名称的值 |
| getAttributeNS() | 返回作为参数传递的属性名称和命名空间的值 |
| getAttributeNode() | 返回指定节点上作为参数传递的属性名称和命名空间的属性节点 |
| getAttributeNodeNS() | 返回指定节点上作为参数传递的属性名称和命名空间的属性节点 |
| getElementsByTagName() | 返回指定节点中所有具有作为参数传递的标签名的子元素节点数组 |
| getElementsByTagNameNS() | 返回指定节点中所有具有作为参数传递的标签和命名空间的子元素节点数组 |
| hasAttribute() | 如果作为参数传递的属性存在于指定节点，则返回 true，否则返回 false |
| hasAttributeNS() | 如果作为参数传递的属性名称和命名空间存在于指定节点，则返回 true，否则返回 false |
| hasAttributes() | 如果指定节点定义了任何属性节点，则返回 true，否则返回 false |
| hasChildNodes() | 如果指定节点有任何子节点，则返回 true，否则返回 false |
| insertBefore() | 在指定的节点内部，将作为参数传递的节点插入到作为第二个参数的节点之前 |

**表 9-4** DOM 节点方法（续）

## 第9章：文档对象 243

| 方法 | 描述 |
| --- | --- |
| normalize() | 规范化指定的节点 |
| removeAttribute() | 从指定节点中移除作为参数传递的属性名称的属性节点 |
| removeAttributeNode() | 从指定节点中移除作为参数传递的属性节点对象引用 |
| removeAttributeNS() | 从命名空间节点移除作为参数传递的属性名称 |
| removeChild() | 从指定节点中移除作为参数传递的子节点 |
| removeEventListener() | 从指定节点上移除事件监听器 |
| replaceChild() | 将指定节点中作为第二个参数传递的子节点替换为作为参数传递的子节点 |
| scrollIntoView() | 在浏览器窗口中滚动到指定的节点 |
| setAttribute() | 为指定的节点设置属性节点的名称（第一个参数）和值（第二个参数） |
| setAttributeNode() | 将作为参数传递的属性节点对象设置为指定节点的属性节点 |
| setAttributeNodeNS() | 将带有命名空间的属性节点对象设置为指定节点的属性节点 |
| setAttributeNS() | 为指定的节点设置属性节点的命名空间（第一个参数）、名称（第二个参数）和值（第三个参数） |

### 表 9-4 DOM 节点方法

随后，使用`document.createTextNode`方法为`inner_div`节点创建文本节点：

```
let inner_div_text = document.createTextNode("More about...")
```

接下来，使用 DOM 方法`appendChild()`将该文本节点作为新`inner_div`节点的子节点：

```
inner_div.appendChild(inner_div_text);
```

要给`inner_div`节点添加 title 属性，你可以给它的`title`属性赋值：

```
inner_div.title = "More";
```

### JavaScript：初学者指南。

最后，使用 DOM 方法`appendChild()`将`inner_div`节点作为（在此情况下是作为）`me_div`节点的子元素添加到文档结构中：

```
me_div.appendChild(inner_div);
```

完整的 JavaScript 代码看起来如下所示：

```
let me_div = document.getElementById("div");
let inner_div = document.createElement("div");
let inner_div_text = document.createTextNode("More about me...");
inner_div.appendChild(inner_div_text);
inner_div.title = "Me";
me_div.appendChild(inner_div);
```

使用`appendChild()`将`inner_div`正式地添加到`me_div`元素内部的 DOM 结构中。

## 尝试 9-1 向文档添加 DOM 节点

| pr9_1.html | pr9_1.js |

此项目允许你练习在本章中学习的文档和 DOM 节点属性及方法。

### 逐步步骤

- 1. 创建一个带有以下 body 代码的 HTML 页面并将其保存为`pr9_1.html`：

```html
<body>
  <div id="div" title="Gosh!">
    任何我想写的内容...
  </div>
  <script type="text/javascript" src="pr9_1.js"></script>
</body>
```

- 2. 创建一个外部 JavaScript 文件并将其保存为`pr9_1.js`。用于第 3-5 步。

- 3. 获取 ID 为 "div" 的元素的 title 属性值，并将该值作为警告框（alert）发送给查看者。

- 4. 创建一个新的 div 元素，带有文本 "See you!" 和值为 "Lucky!" 的 title 属性。将其作为 ID 为 "div" 的 div 元素的子元素添加到文档结构中。

- 5. 保存 JavaScript 文件并在浏览器中打开 HTML 文件以查看结果。

### 尝试总结

在这个项目中，你利用了关于对象属性、方法以及 DOM 节点的知识，来弹出一个 DOM 节点属性，并在文档结构中创建一个新的`div`元素。

### 创建动态脚本

如你所见，JavaScript 允许通过`document.getElementById()`和`document.getElementsByTagName()`等各种方法访问文档中的所有元素。

这允许你如之前看到的那样获取信息、添加节点、修改节点和删除节点。此外，你可以通过 DOM 节点属性访问元素的样式属性（通常最初由样式表设置），以便对这些位置、颜色、边框、大小或样式的任何其他部分进行更改。

### JavaScript 中的样式

当使用级联样式表（CSS）设置样式时，你可能会在 CSS 代码中设置如下所示的内容（保存为`dyn_01.css`）：

```css
#div1 { color:#000000; background-color:#FFFFFF; }
#div2 { border-style:solid; border-width:1px; border-color:#000000; }
```

这为两个 ID（`div1`和`div2`）提供了属性。因此，如果你有以下 HTML 代码（保存为`dyn_01.html`），这两个`div`元素在网页上的呈现效果将大不相同：

```html
<head>
<link rel="stylesheet" type="text/css" href="dyn_01.css">
</head>
<body>
<div id="div1">
我在 div1 中。这里看起来像是个不错的地方。
</div>
<div id="div2">
我在 div2 中。这里稍微华丽一点。
</div>
<script type="javascript" src="dyn_01.js"></script>
</body>
```

## 248 JavaScript: 初学者指南

HTML 代码已链接到 CSS 代码。因此，`div1`元素将以白色背景上的简单黑色文本形式显示，而`div2`元素周围将有一个平平无奇的、实心的黑色边框。

如你所见，此页面为每个`div`元素都使用了 ID——因此，你不仅可以通过 CSS 代码访问元素的 ID，也可以在 JavaScript 代码中访问元素的 ID。所以，你可以在 JavaScript 文件中（在之前的 HTML 代码中调用——保存为`dyn_01.js`）开头使用一些代码，通过`document.getElementById()`根据它们的 ID 获取两个`div`：

```javascript
let d1 = document.getElementById("div1");
let d2 = document.getElementById("div2");
```

现在你拥有了这两个元素的变量。

如果你想通过 JavaScript 修改在 CSS 代码中设置的样式，你需要利用每个元素中都包含的`style`属性。然后，JavaScript 使用与 CSS 选择器相同的名称来访问该属性。例如，如果你想将`div1`中的文本颜色改为灰色，你可以使用以下代码：

```javascript
let d1 = document.getElementById("div1");
let d2 = document.getElementById("div2");
d1.style.color = "#DDDDDD";
```

在 CSS 代码中，选择器用于更改元素的前景色。在 JavaScript 中，它也是访问元素的`style`属性后用于更改它的属性名称。

如果 CSS 选择器不是单个单词怎么办？例如，如果你在 JavaScript 中像在 CSS 代码中那样使用`background-color`选择器，它将不起作用。以下代码尝试将背景颜色改为绿色：

```javascript
let d1 = document.getElementById("div1");
let d2 = document.getElementById("div2");
d1.style.backgroundColor = "#DDDDDD";
```

这将会不起作用，因为 JavaScript 不使用连字符（`-`）作为任何名称属性。相反，JavaScript 会将第一个单词后的任何额外单词的首字母大写。因此，CSS 选择器`background-color`在 JavaScript 中变成了`backgroundColor`。其他选择器也遵循相同的模式（例如，`border-right-color`将变为`borderRightColor`）。这种样式被称为**驼峰命名法**（camel case），它是 JavaScript 中非常常用的一种样式。

JavaScript 代码可以重写如下以便更改生效：

```javascript
let d1 = document.getElementById("div1");
let d2 = document.getElementById("div2");
d1.style.backgroundColor = "#DDDDDD";
```

这将把`div1`元素的背景颜色改为绿色。现在的问题是，这会在脚本运行后立即发生，可能在用户注意到`div1`元素有另一种颜色之前就发生了。为了让这更有用，你需要在文档加载或刷新以外的时间运行部分脚本。

### 注意事项

读取样式并没有设置它那么简单，因为存在浏览器差异和其他问题。有关如何获取样式的更多信息，请参见 www.quirksmode.com/dom/styles。

### 简单事件处理

到目前为止，你的脚本仅在页面加载（或刷新）时运行。这对于许多任务是好的，但如果它们是响应用户的操作而执行的（例如更改样式），将会更有用。例如，页面加载时更改元素的背景颜色用户可能不会注意到，但响应鼠标点击更改颜色将很有用。

### JavaScript: 入学者指南

### 尝试此 9-2 属性更改

此项目允许你练习在本章中学到的新的`style`和`innerHTML`属性。

### 逐步步骤

- 1. 创建一个包含以下 body 代码的 HTML 页面，并将其保存为`pr9_2.html`：

```html
<body>
<div id="div1">
  我什么时候更新这个页面？
</div>
<div id="div2">
  <a href="answer.html" id="c_link">查看结果！</a>
</div>
<script type="text/javascript" src="prjs9_2.js"></script>
</body>
```

- 2. 创建一个外部 JavaScript 文件并将其保存为`prjs9_2.js`。在第 3 至 5 步中使用它。

- 3. 编写一些代码，当点击链接时，id 为`div1`的 div 元素的背景颜色变为`#CCCCCC`，且该元素的内容变为`<strong>现在！</strong> 这不是很快吗？`

- 4. 完成后，JavaScript 文件应该像这样：

```javascript
let d1 = document.getElementById("div1");
let c_link = document.getElementById("c_link");
c_link.onclick = function() {
  d1.innerHTML = "<strong>现在！</strong> 这不是很快吗？";
  return false;
};
```

- 5. 保存 JavaScript 文件并在浏览器中打开 HTML 文件以查看结果。

### 本总结

在这个项目中，你利用了关于 DOM 节点`style`和`innerHTML`属性的知识对 Web 页面进行了样式内容更改。

## 第 9 章自测

- 1. 该对象是浏览器为每个查看的新 HTML 页面创建的对象。

- 2. `document`对象的属性返回将查看者引导至当前文档的 URL。

- 3. 你可以使用 DOM 节点属性更改元素的样式表属性。

  A. 正确

  B. 错误

- 4. `document`对象的方法允许你通过其`id`属性的值获取元素。

  A. getElementsByClassName()

  B. createElement()

  C. getSelection()

  D. getElementById()

- 5. `appendChild` DOM 节点方法允许将子节点作为指定节点的第一个子节点。

  A. 正确

  B. 错误

- 6. 一旦节点添加到文档中，你就无法将其删除。

  A. 正确

  B. 错误

- 7. `document`属性是一个包含页面上所有`<a>`标签的数组。

- 8. DOM 节点属性允许你更改元素节点的 HTML 内容。

- 9. 该属性持有当前文档最后修改的日期时间。

- 10. 文档对象模型（DOM）允许 JavaScript（以及其他脚本语言）访问浏览器中的文档结构。

  A. 正确

  B. 错误

- 11. 你可以使用`title`属性在浏览器窗口顶部栏显示 Web 页面的标题。

  A. 正确

  B. 错误

- 12. 哪个属性返回当前文档的完整 URL？

  A. domain

  B. referrer

  C. URL

  D. title

- 13. `writeln()`方法与`write()`方法有何区别？

  A. 它在行尾添加等同于 HTML `<br />`标签的内容。

  B. 它在行尾添加等同于 HTML `<p>`标签的内容。

  C. 它在行尾添加一个 JavaScript 换行符。

  D. 它与`write()`方法完全相同。

- 14. `getElementsByName()`方法通常用于获取什么？

  A. 所有你通过名称知道的元素。

  B. 所有命名了名称但没有`id`属性的元素。

  C. 所有`name`属性具有相同值的元素（大多数单选按钮）。

  D. 所有属性值等于指定名称的元素。

- 15. 在`document.open()`和`document.close()`语句之间常见的语句是？

  A. HTML 命令

  B. `document.write()`和`document.writeln()`语句

  C. 只有`document.writeln()`语句

  D. 只有`window.alert()`语句

## 第 10 章

事件处理器

### 关键技能与概念

- 理解事件处理器的位置和用途

- 学习事件处理器

- 注册事件的其他方法

- 事件对象

- 使用事件处理器创建脚本

在创建脚本时，你经常会发现某些“事件”（例如用户将鼠标移动到元素上或点击特定元素），你的脚本应该对此做出反应。实现这一点是通过使用事件处理器。要学习事件处理器如何工作，你需要了解事件处理器在哪里。

### 什么是事件？

事件是页面上发生的事情，例如点击链接、鼠标在元素上移动或加载页面。事件处理器是用于响应这些事件的代码。

### 为什么事件处理器很有用

事件处理器非常有用，因为它们允许你的 Web 页面具有交互性。例如，你可以使用`alert`在用户点击链接或表单时触发。

### 理解事件处理器的位置和用途

事件处理器可以使用以下几个位置：

- 在 HTML 标签内部

- 在`<script>`标签内

- 在外部 JavaScript 文件中

> 注意：Node.js 同样使用事件和处理器。本章将集中于浏览器事件，而 Node.js 事件处理将在后面的章节介绍。

### 在 HTML 元素中使用事件处理器

要在 HTML 元素中直接使用事件处理器，你需要知道处理器的关键字以及它在 HTML 代码中的位置。为了给你一个示例，我将介绍`onclick`事件处理器，它用于在用户点击区域时发生某些事情。

可以被点击的元素可以是按钮。所以，假设你想在用户点击按钮时显示警告，你会编写类似下面的代码：

```html
<input type="button" value="点击我!" onclick="此处为 JavaScript 代码">
```

要在用户点击按钮时弹出警告，你可以将必要的 JavaScript 代码直接添加到你的`onclick`属性中，如下所示：

```html
<form>
  <input type="button" value="点击我!" onclick="window.alert('你好!');">
</form>
```

### 事件处理器是如何工作的

注意`onclick`事件处理器的工作方式非常像一个 HTML 属性。当用户点击这个普通按钮时，会弹出一个带有问候的警告框。注意引号的规则在这里适用。将`onclick`作为属性使用时，你需要对所有的 JavaScript 代码使用双引号，因此当你需要在警告框中使用引号时，使用单引号以避免可能的错误。

## 258 JavaScript: 入门指南

请注意，`alert`命令以分号结尾。这允许你在`alert`之后添加额外的 JavaScript 代码，从而让你能够在点击事件上执行多个操作，而不仅仅是单个 JavaScript 语句。

如果你想这样做，可以编写两个`alert`。你只需要记住用分号来分隔`alert`命令即可。这与通常看到的格式略有不同，因为所有代码将位于同一行，而不是分行：

```html
<form>
  <input type="button" value="Click Me!"
  onclick="window.alert('Hi!'); window.alert('Bye!');" />
</form>
```

注意分号是如何分隔 JavaScript 语句的。

通过分号，这个示例可以在同一个事件上执行两个 JavaScript 语句。在使用事件处理器时，你可以通过这种方式执行多个命令。然而，重要的是要在文本编辑器中，将事件处理器关键字和引号结束（在本例中为代码中的最后一个分号）之间的所有内容保持在同一行；否则，代码中的换行可能会导致无法正常运行或产生 JavaScript 错误。

如果你想让代码变得很长，可能希望将代码放在函数中。事件处理器可以用于任何 JavaScript 代码，因此你可以用它来调用你定义的函数。例如，你可以将两个`alert`放在外部 JavaScript 文件中的函数内部（在这里将保存为`js_event_01.js`），如下：

```javascript
function hi_and_bye() {
  window.alert('Hi!');
  window.alert('Bye!');
}
```

接下来，在你的 HTML 代码中添加`script`标签和事件处理器：

```html
<form>
  <input type="button" value="Click Me!" onclick="hi_and_bye();" />
</form>
<script type="text/javascript" src="js_event_01.js"></script>
```

注意如何使用事件处理器调用函数。

注意使用事件处理器调用函数的方式就像在脚本中进行普通函数调用一样。这不仅允许你缩短事件处理器内的代码，还可以在另一个按钮点击或页面的后续部分复用该函数，而无需再次编写两个`alert`。使用函数对你非常有帮助，尤其是当你想要代码变得极其长时。

### 注意

随着学习的进行，你会发现使用`type="button"`和`type="submit"`之间存在区别。对于`submit`类型，你需要返回`false`或使用`preventDefault()`防止默认操作。在你继续学习本章节时，将看到更多内容。

### 在脚本代码中使用事件处理器

你也可以在脚本代码中使用事件处理器（无论使用 HTML 文档中的`script`标签还是使用 JavaScript 文件）。实现此点的方法之一是给元素一个`id`属性，然后使用 JavaScript 方法`document.getElementById()`来访问该元素，正如你在第 9 章中学到的那样。

### 添加 id 属性

要以这种方式使用之前的脚本，你首先为输入按钮的 HTML 标签添加`id`属性，如下所示：

```html
<form>
<input type="button" value="Click Me!" id="say_hi">
</form>
<script type="text/javascript" src="js_event_01.js"></script>
```

注意按钮输入元素被赋予了`say_hi`的`id`。你将用它来访问按钮并将其绑定到脚本中的一个事件。

### 访问元素

`document.getElementById()`方法允许你通过其`id`属性的值访问 HTML 文档中带有`id`属性的任何元素。为了访问你一直使用的 id 为`say_hi`的按钮输入元素，可以使用以下代码：

```javascript
let hi_button = document.getElementById("say_hi");
```

现在，你可以将函数代码放入 JavaScript 文件 (js_event_01.js) 的函数表达式中，如下：

```javascript
let hi_button = document.getElementById("say_hi");
hi_button.onclick = function() {
  window.alert("Hi!");
  window.alert("Bye!");
};
```

> 按钮输入元素通过其 id (say_hi) 被访问，并赋值给变量 (hi_button)

> 事件处理器用于将函数表达式赋值给按钮输入元素的 onclick 事件。

该函数表达式（显示两个`alert`的那个部分）被赋值用于处理输入按钮的点击事件。然后，当按钮被点击时，查看者将看到两个`alert`。

### JavaScript: 入门指南

这种处理事件的方法允许你将所有的 JavaScript 代码放置在 HTML 元素之外，这使得你的 HTML 代码更加整洁（特别是当使用外部 JavaScript 文件时）。在本章节的后半部分，你将看到可以使用更新的方法来处理事件。

> **注意**

> 在使用`getElementById()`访问元素之前，确保该元素已添加到页面中。可以通过将`<script></script>`标签放在文档末尾（紧邻闭合的`</body>`标签之前），或使用`load`事件在访问 DOM 元素之前确定内容已加载。

### 专家问

- **Q: 你的意思是我可以像使用 HTML 属性一样，通过事件处理器直接写一些 JavaScript 吗？**

**A:** 是的，但记住给元素一个`id`属性并在 JavaScript 代码中响应事件有助于保持你的 HTML 代码更加整洁。

- **Q: 可以在按钮以外的元素上使用事件吗？**

**A:** 可以，几乎任何元素都可以对事件做出反应。

- **Q: 我不是在第 9 章学过这个吗？**

**A:** 到目前为止，你得到的基本上是对某些内容的回顾。剩余章节将在此基础上，为你提供可用的事件。

### 学习事件

现在你已经知道什么是事件处理器以及如何使用它们，你需要查看页面上的各种事件使用了哪些事件处理器。从查看表 10-1 开始，该表列出了常见的事件、它们的事件处理器以及可能触发每个操作的示例。

## 第 10 章：事件处理器

| 事件 | 事件处理器 | 事件触发器 |
|---|---|---|
| Abort | onabort | 图像停止加载 |
| Blur | onblur | 查看者从元素移除焦点 |
| Change | onchange | 查看者更改表单内容 |
| Click | onclick | 查看者点击元素 |
| ContextMenu | oncontextmenu | 查看者打开上下文菜单 |
| Copy | oncopy | 查看者对页面部分使用复制命令 |
| Cut | oncut | 查看者对页面部分使用剪切命令 |
| Dblclick | ondblclick | 查看者双击鼠标 |
| Error | onerror | 浏览器获取 JavaScript 错误或图像不存在 |
| Focus | onfocus | 查看者赋予元素焦点 |
| Keydown | onkeydown | 查看者按下键 |
| Keypress | onkeypress | 查看者按下键并输入了相应的字符 |
| Keyup | onkeyup | 查看者释放键 |
| Load | onload | 网页加载完成 |
| Mousedown | onmousedown | 查看者在元素上按下鼠标按钮 |
| Mouseleave | onmouseleave | 查看者鼠标离开元素（不包括子元素） |
| Mousemove | onmousemove | 查看者移动鼠标（移动光标） |
| Mouseout | onmouseout | 查看者鼠标离开元素 |
| Mouseover | onmouseover | 查看者鼠标经过元素 |
| Mouseup | onmouseup | 查看者释放鼠标按钮 |
| Mousewheel | onmousewheel | 查看者向任何方向滚动滚轮 |
| Paste | onpaste | 查看者对页面部分使用粘贴命令 |
| Reset | onreset | 查看者重置页面上的表单 |
| Resize | onresize | 窗口大小调整 |
| Scroll | onscroll | 查看者滚动区域 |
| Select | onselect | 用户选择 |
| Submit | onsubmit | 查看者提交页面上的表单 |
| Unload | onunload | 查看者离开当前页面 |

**表 10-1** 常见事件与事件处理器

## JavaScript：初学者指南

### 注意

还有许多你可能觉得有用的其他事件。由于可用事件的数量可能会快速变化，下表列出了一些常用事件。拖放功能的事件将在第 16 章中讨论。与浏览器端 JavaScript 相关的且将保持更新的事件完整列表，可以在 developer.mozilla.org/en-US/docs/Web/Events 找到。

现在你已经对事件处理器有了大致的了解，你将详细查看一些最常用的事件处理器，看看它们是如何工作的。

### 点击事件 (The Click Event)

点击事件是你已经学习过的这种事件，它发生在查看者点击 Web 页面上的元素时。例如，你可以使用表单按钮并在点击它时发送一个警报框（alert）：

```html
<body>
<form>
  <input type="button" value="Do Click Here"
  onclick="window.alert('I told you not to click me!');">
</form>
</body>
```

`onclick`事件处理器用于按钮上。

一旦按钮被点击，它将向查看者发送一个警报。图 10-1 显示了当查看者点击按钮时此代码的结果。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_280_0.png)

图 10-1 当查看者点击按钮时会弹出此警报。

## 第 10 章：事件处理器 263

要使用此事件处理器对链接执行相同的操作，你可能会倾向于执行类似以下的操作：

噢不！这会给你带来问题，因为浏览器会尝试跟随该链接。

```html
<body>
<a href="http://none" onclick="window.alert('Hey! You clicked me!');">
不要点击我</a>
</body>
```

这段代码的问题在于，警报框会生效，但浏览器将继续执行`<a>`标签的原始操作，并尝试跳转到 http://none。这可能会在浏览器中引起“找不到服务器”的错误。

避免“找不到服务器”错误的一种方法是链接到实际的页面（这对可访问性有好处）；然而，如果查看者启用了 JavaScript，它可能会让查看者离开当前页面。为了在启用 JavaScript 时防止链接跳转，你需要在点击事件的 JavaScript 中添加一条额外的语句。你需要告诉浏览器在向查看者显示警报后不要继续。为了做到，你将添加一个`return false`语句，这将阻止浏览器在警报后跟随链接。以下代码显示了如何在`return`语句中这样操作：

```html
<body>
<a href="/none"
onclick="window.alert('Hey! You clicked me!'); return false;">
不要点击我</a>
</body>
```

> `return false`语句阻止了浏览器尝试跟随链接。

通过这段代码，点击事件将由`onclick`事件处理器处理，浏览器将不需要担心尝试跟随`href`属性中的链接。在本章的后半部分中，你将学习如何使用现代方法来阻止默认操作：`event.preventDefault()`。

### 注意

你也可以通过`javascript:`命令为链接编写 JavaScript 代码——例如，`<a href="javascript:alert('Hi!');">点击</a>`——但出于可访问性考虑，不推荐这种方法（如果禁用了 JavaScript，链接将无处可去）。

## 聚焦与失去焦点事件 (Focus and Blur Events)

当查看者给某个元素或窗口焦点时，会触发聚焦事件。查看者通过点击项目内部获得焦点、使用键盘移动到项目（通常通过`TAB`键）或通过脚本获得焦点。例如，查看者点击一个文本输入框（在输入任何内容之前）会使该框获得焦点。此外，点击一个非活动状态的窗口并使其变为活动窗口也会让该窗口获得焦点。聚焦事件还有一个相关方法`focus()`，该方法将在第 11 章和第 14 章中介绍。

## 264 JavaScript：初学者指南

为了看到聚焦事件的运行，你可以创建一个文本输入框，它是表单元素之一，能够允许你给元素设置焦点。以下示例显示了如何操作，以及如何创建一个提醒警报框，当查看者聚焦到文本框时该警报框会弹出：

```html
<form>
  输入你的名字：
  <input type="text" id="user-name">
</form>
<script type="text/javascript">
  let counter = 0;
  let nameElement = document.getElementById("user-name");
  nameElement.onfocus = function () {
    if (counter == 0) {
      window.alert('别忘记大写！');
    }
    counter += 1;
  }
</script>
```

这段代码将在查看者开始输入之前给他们显示一个警报。该警报作为对名字进行大写的提醒。`counter`变量被设置并递增，是为了防止警报在用户每次聚焦文本框时都出现（将其限制为仅第一次聚焦事件）。图 10-2 显示了当查看者聚焦到文本框时，浏览器中上述代码的结果。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_282_0.png)

**图 10-2** 当文本框从查看者处接收焦点时会弹出此警报。

## 第 10 章：事件处理器 265

失去焦点事件（blur event）发生在查看者从元素或窗口移除焦点时。要移除某个东西的焦点，查看者通常会给其他东西焦点。例如，查看者可以从一个元素移动到另一个元素，或从一个窗口移动到另一个窗口。失去焦点事件还有一个相关方法`blur()`，该方法将在第 11 章和第 14 章中介绍。

### 注意

当查看者给予另一个区域焦点时，会触发失去焦点事件，这是浏览器知道查看者从第一个区域释放焦点的唯一方法。例如，当查看者在输入字段中按回车键时，焦点从输入字段转移到文档。此外，如果你将焦点放在文本字段上然后切换标签页，也会触发事件。为了看到失去焦点事件的运行，以下示例使用了两个文本框：点击第一个框使其获得焦点，点击第二个框则会触发第一个框的失去焦点事件。

```html
<form>
给这个框设置焦点：
<input type="text" onblur="window.alert('嘿！回来！');">
给这个框设置焦点以让第一个框失去焦点：
<input type="text">
</form>
```

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_283_0.png)

当查看者点击第二个文本框时，他们会收到来自第一个框的警报，告诉他们回来。图 10-3 显示了上述代码在浏览器中运行的结果。注意，当警报弹出时，焦点在第二个框中。通过点击第二个框，查看者触发了第一个框的失去焦点事件。

# 加载与卸载事件 (The Load and Unload Events)

加载事件（load event）发生在 Web 页面加载完成时。如果你想在页面加载完成后显示警报，可以使用以下代码：

```html
<body onload="window.alert('我正在加载中！');">
页面正文内容...
</body>
```

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_283_1.png)

当页面加载完成后，查看者将收到一个警报。图 10-4 显示了如果你想在脚本代码而非`body`标签中使用`onload`，代码可以如何写（将其保存为`load_alert.js`）：

```javascript
window.onload = function() {
  window.alert('我正在加载中！');
};
```

## 266 JavaScript：初学者指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_284_0.png)

**图 10-4** 在页面加载完成后在浏览器窗口中显示。

# 第 10 章：事件处理器 267

### 注意

文档中只能指定一个加载事件。如果存在多个，只有一个会起作用。这可能发生在你同时在`<body>`标签上添加`onload`、使用`addEventListener`（在本章后面会提到）以及/或使用`window.onload`方法，因此在添加加载事件时要小心。

现在你可以访问 HTML 代码中的所有元素（window 对象将在后续详细介绍），你可以如下所示从`<body>`标签中移除事件处理器：

```html
<body>
<script type="text/javascript" src="load_alert.js"></script>
页面正文内容...
</body>
```

### 注意

一旦加载事件发生，你就不能再使用`document.write()`写入文档。

卸载事件（unload event）发生在用户离开当前 Web 页面时。查看者可以通过点击链接、在浏览器中输入另一个地址或关闭窗口来离开。该事件已知会骚扰查看者，因为它允许网站所有者在访问者尝试到另一个页面或另一个网站时执行某些操作（强制他们等待）。要在用户离开页面时弹出警报，你可以编写以下代码：

```html
<body onunload="alert('记得回来，好吗？');">
其他 HTML 代码在此处....
</body>
```

> 卸载事件处理器被添加到了 body 标签上。

图 10-5 显示了上述脚本的结果。当查看者尝试离开包含此脚本的页面时，会弹出一个警报告诉他们记得回来。当然，如果用于索引页或网站内的多个页面，这可能会让查看者感到非常不便。

与`onload`事件处理器一样，你可以通过使用`window.onunload`在脚本代码而非`body`标签中使用卸载事件处理器。

总体而言，在上线页面上使用卸载事件之前请务必仔细考虑，因为它几乎会骚扰 Web 用户。

## 提示

如果`onunload`工作不正常，如果你需要此功能，请尝试使用`onbeforeunload`。

### JavaScript: 入门指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_286_0.png)

**图 10-5** 当观众尝试离开页面时，会弹出此警报。

### 重置（Reset）与提交（Submit）事件

当文档中包含一个或多个表单时，会使用重置和提交事件。表单的内容可以被重置，也可以提交进行处理。这些事件允许你针对这些表单操作编写相应的响应。

重置事件（reset event）发生在观众使用表单重置按钮来重置表单中的字段时。重置事件有一个相关方法`reset()`，该方法将在第 14 章中介绍。提交事件（submit event）发生在观众提交表单时。提交事件也有一个名为`submit()`的相关方法，将在第 14 章中介绍。

要查看提交事件，你必须创建一个可以通过提交按钮进行提交的表单。以下代码将在点击提交按钮时向观众弹出一个“感谢你”的警报：

```html
<form onsubmit="window.alert('Thank You');">
你的名字是什么?<br>
<input type="text" id="thename"><br>
<input type="submit" value="Submit Form">
</form>
```

提交事件并没有带给你太多信息（尤其是表单内容并没有真正去往任何地方），但当你学习第 14 章的表单验证时，这个事件将变得更有用。

### 鼠标事件（Mouse Events）

有很多可用于涉及鼠标的用户操作的事件。下列出了：

- mousedown: 当观众按下鼠标按钮但在点击完成之前（按钮尚未释放）发生。

- mouseup: 当观众在按下鼠标按钮后释放时发生。

- mouseenter: 当观众将鼠标光标移动到元素上时（不包括子元素）发生。

- mouseleave: 当观众将鼠标光标移出元素时（不包括子元素）发生。

- mouseover: 当观众将鼠标光标移动到元素上时发生。

- mouseout: 当观众将鼠标光标移出元素时发生。

- mousewheel: 当观众向上或向下滚动滚轮时发生。

可以通过创建一个文本链接来显示鼠标事件的示例。当你向链接添加`onmouseover`处理程序时，你就有了在光标悬停在链接上时执行 JavaScript 命令的选择。因此，如果你希望在观众将鼠标移过链接时弹出一个警报，你可以编写如下代码：

```html
<a href="http://www.example.com" onmouseover="alert('I told you not to click me!');">不要点击我！</a>
```

标签中的`onmouseover`事件处理器允许观众在受到警报欢迎之前将鼠标移到链接上。请记住，如果脚本具有侵入性，可能会骚扰访问者。图 10-6 显示了该脚本在浏览器中的结果。当鼠标移动到链接上时，警报弹出。由于不需要点击链接即可发生某些事情，浏览器将不会尝试跳转链接。事实上，在这个地方，完全是不可能点击链接的，因为当你把鼠标移到它上方时，警报会不断弹出！

### 键盘事件（Keyboard Events）

当用户使用键盘与 Web 页面交互时，会发生键盘事件。这些事件允许你对观众按下和释放键的每个阶段做出反应。键盘事件列在这里：

- keydown: 当观众按下键盘上的某个按键时发生。

- keypress: 当观众按下键盘上的某个按键并输入相应字符时发生。

- keyup: 当观众松开键盘上的按键时发生。

270 JavaScript: 入门指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_288_0.png)

**图 10-6** 当鼠标光标移动到链接上时，会弹出此警报。

例如，如果你希望在每次向框中输入字符时都发送一个警报，可以使用以下代码：

```html
<input type="text" id="typing" onkeyup="alert('You typed a character!')">
```

这会在每次向文本框中输入字符时提醒你。在输入几个字符后，这可能会变得非常烦人，但一旦你在本章稍后的部分学习了事件对象，你将学会如何找出按了哪个键，这将赋予你处理键盘事件时更大的灵活性。

## 尝试：聚焦（Focus）与失焦（Blur）

在这个项目中，你将使用聚焦和失焦事件以及`innerHTML`（来自第 9 章）来创建一个脚本，提醒用户在框中输入什么。

### 步骤说明

1. 创建一个 HTML 页面并将其保存为`pr10_1.html`。添加必要的脚本标签以指向名为`pr10_1.js`的外部 JavaScript 文件。添加代码，以便有一个 id 为 "pn" 的电话号码文本框和一个用于地址的`textarea`。在电话号码框旁边将有一个 id 为 "reminder" 的空`span`标签。HTML 文件的`body`部分在完成后应该如下所示：

```html
<form>
  电话号码:
  <input type="text" id="pn"> <span id="reminder"></span><br><br>
  <textarea></textarea>
</form>
```

2. 创建一个外部 JavaScript 文件并保存为`pr10_1.js`。将其用于第 3 步和第 5 步。

3. 通过 id 获取 "pn" 和 "reminder" 元素，并将它们分别赋值给变量`pn`和`rm`。

4. 当`pn`获得聚焦时，将`rm`的`innerHTML`改为文本 "Format: 123-456-7890"。当`pn`失焦时，将`rm`的`innerHTML`更改为空字符串（""）。

5. JavaScript 文件完成后应该如下所示：

```javascript
let pn = document.getElementById("pn");
let rm = document.getElementById("reminder");
pn.onfocus = function() {
  rm.innerHTML = "Format: 123-456-7890";
}
pn.onblur = function() {
  rm.innerHTML = "";
}
```

6. 保存 HTML 和 JavaScript 文件，并在浏览器中加载 HTML 页面。点击文本框内部，提醒消息应该会出现在它旁边。之后点击`textarea`使文本框失焦并使消息消失。

### 尝试总结

在这个项目中，你使用了对聚焦和失焦事件的知识创建了一个帮助用户填写表单的脚本。

## 提问专家

**Q：为什么会有这么多事件？**

**A：** 观众（或浏览器本身）可以在 Web 页面上执行很多事情，因此产生了大量的事件。

JavaScript: 入门指南

**Q：我需要记住所有的事件吗？**

**A：** 只有在你参加考试、或者在工作中需要快速掌握知识、或者你只是喜欢背诵时才可能需要记住它们；否则，如果你不确定使用哪个事件，可以参考本章的表 10-1。

**Q：我需要记住书中的每一个事件吗？**

**A：** 由于本书是一本入门指南，你不会达到使用每一个事件的地步。

## 第 10 章：事件处理器

一个事件、该事件的函数处理器，以及一个 true 或 false 的值，取决于你希望事件处理函数在捕获阶段（true）还是冒泡阶段（false）执行。其通用格式如下：

```
element.addEventListener("event_type", function_name, true_or_false);
```

因此，如果你想像在本章早些那样创建一个带链接的输入按钮，你可以调整 JavaScript 代码如下：

```javascript
let web_page = "http://www.yahoo.com";
let b1 = document.getElementById("btn1");
b1.addEventListener("click", function () {
  window.location = web_page;
}, false);
```

注意，这种方法不是直接使用事件处理器属性，而是使用事件的名称（而不是使用`onclick`，你只需使用`click`）。此外，此方法可以接受函数名或函数表达式来处理事件（如前文所示）。需要注意的是，当你指定一个函数时，需要省略括号。例如，查看以下代码：

```javascript
let web_page = "http://www.yahoo.com";
let b1 = document.getElementById("btn1");
function handleButtonClick() {
  window.location = web_page;
}
b1.addEventListener("click", handleButtonClick, false);
```

> 该函数的定义使得它可以在按钮被点击时运行

> 在`addEventListener`中指定了该函数以处理事件（注意这种情况下没有括号）

导致此方法不起作用的常见错误是在`addEventListener`中指定处理函数时包含了括号。因此，如果你发现了意外之外的行为，请检查是否添加了括号。

### 移除事件

要移除事件，你会使用`removeEventListener()`方法：

```
element.removeEventListener("event_type", function_name, true_or_false);
```

注意，如果在`addEventListener`方法中使用了函数表达式，则注册的事件将无法被移除（函数表达式会被视为两个不同的参数，即使它们使用相同的代码）。如果以后可能需要移除该事件，最好是使用一个独立的函数，并在两个方法调用中都使用函数名作为第二个参数。示例如下所示：

```javascript
let web_page = "http://www.yahoo.com";
b1 = document.getElementById("btn1");
function go_to_site() {
    window.location = web_page;
}
b1.addEventListener("click", go_to_site, false);
b1.removeEventListener("click", go_to_site, false);
```

由于这是现代浏览器中注册事件的标准，我们在本书剩余部分使用这种事件注册方法。

### 捕获与冒泡阶段

当其他元素内部的注册了相同事件类型的元素时，事件首先发生的顺序取决于使用捕获阶段还是冒泡阶段来注册事件。如果使用捕获阶段，则最外层的元素先发生，最内层的元素最后发生。如果使用冒泡阶段，情况相反。最常用的是冒泡阶段，因为它具有最好的兼容性。

## `attachEvent()` 方法

`attachEvent`方法的工作原理与`addEventListener`相同。然而，它适用于事件冒泡，并且仅在 IE 9 以下的版本中有用，因此在这里引用它是以防你需要支持旧版本的 IE。

```
element.attachEvent(event_handler, function_name);
```

## 事件对象

当事件发生时，会创建一个`event`对象，其中存储了有关事件的信息。这些信息可以由你的脚本用于帮助执行所需的操作。例如，键盘事件将在事件对象中包含关于所按按键的信息。这允许你在按下不同按键时程序化不同的响应。

## DOM 与 Internet Explorer：DOM Level 0 注册

在大多数浏览器中，使用`event`属性来访问事件对象。它可以作为参数传递给处理事件的函数，如下面的 DOM Level 0 代码所示：

```javascript
let b1 = document.getElementById("btn1");
b1.onclick = function(event) {
    alert("The " + event.type + " event started this!");
};
```

注意，参数`event`被传递给了事件监听器。事件对象的`type`属性（返回事件类型）被用于显示给观众，这样他们就会知道点击事件是由运行的函数引起的。参数可以是你喜欢的任何标识符，因此通常使用较短的标识符如`e`或`ev`，而不是使用`event`。使用任何你觉得方便或你组织标准的标识符即可。只要你保持一致，任何标识符都是完全有效的。

然而，Internet Explorer 使用`window.event`来访问事件对象，这意味着 DOM Level 0 的`handlerById`将使用以下代码：

```javascript
let b1 = document.getElementById("btn1");
b1.onclick = function() {
  alert("The " + window.event.type + " event started this!");
}
```

对于 DOM Level 0 函数，事件对象可以根据浏览器的支持，通过所需的值赋值给变量来实现跨浏览器支持，如下代码所示：

```javascript
let b1 = document.getElementById("btn1");
b1.onclick = function (event) {
  let e = event || window.event;
  alert("The " + e.type + " event started this!");
}
```

## 在现代事件注册中使用 event

当使用`addEventListener`或`attachEvent()`时，事件对象可以通过`event`访问。对于`addEventListener`，可以使用以下代码：

```javascript
let b1 = document.getElementById("btn1");
b1.addEventListener("click", function (event) {
  alert("The " + event.type + " event started this!");
}, false);
```

对于`attachEvent()`，可以使用以下代码：

```javascript
let b1 = document.getElementById("btn1");
b1.attachEvent("onclick", function (event) {
  alert("The " + event.type + " event started this!");
});
```

## 属性与方法

你已经看到了`type`属性，事件对象还有其他属性和方法，列在表 10-2 中。

你会发现，某些属性适用于 Internet Explorer（9 以前），而其他适用于现代浏览器。由于大多数现代浏览器（包括 IE 9 及以上）支持标准的事件注册。

| 属性/方法 | 描述 |
|---|---|
| bubbles | 事件是否冒泡。 |
| cancelable | 默认行为是否可以取消。 |
| cancelBubble | 设置为 false 时取消事件冒泡（Internet Explorer 8 及以前）。 |
| currentTarget | 当前处理事件的元素。 |
| defaultPrevented | 是否调用了`preventDefault()`。 |
| detail | 关于事件的额外信息。 |
| eventPhase | 事件发生的阶段：1 = 捕获，2 = 目标，3 = 冒泡。 |
| preventDefault() | 防止默认行为的发生。 |
| returnValue | 防止默认行为的发生（Internet Explorer 8 及以前）。 |
| srcElement | 事件的目标元素（私有但支持）。通常使用`target`（见后表）。 |
| stopImmediatePropagation() | 停止事件的所有捕获和冒泡，并阻止其他处理器的调用。 |
| stopPropagation() | 停止事件的所有捕获和冒泡。 |
| target | 事件的目标元素。 |
| trusted | 事件是由浏览器还是程序发起的。 |
| type | 事件类型（例如，click、mouseover 等）。 |
| view | 事件发生的窗口对象。 |

**表 10-2** 事件对象的属性与方法

## 第 10 章：事件处理程序 277

## 阻止默认行为

你可能记得，在使用 DOM Level 0 注册时，阻止链接的默认行为是通过`return`语句（`return false`）来实现的。然而，你可以使用事件的`preventDefault()`方法来实现这一点，而不需要立即返回。

例如，现在可以使用以下代码来阻止点击链接加载指定的页面：

```javascript
let nlink = document.getElementById("nclink");
nlink.addEventListener("click", function(event) {
  event.preventDefault();
  alert("This link doesn't go anywhere!");
  // Further Code...
}, false);
```

如你所见，你可以继续处理事件，而不是使用`return`语句退出函数。

### 注意

在版本 9 之前的 Internet Explorer 中，你可以使用`returnValue`属性。将其值设置为`false`（例如：`window.event.returnValue = false;`）的效果与`preventDefault()`相同。

## 事件信息

某些事件（如键盘事件）具有表中未列出的额外属性（这些属性适用于所有事件）。

例如，当键盘事件发生时，按下键的键码存储在`event.keyCode`中，这允许你确定按下了哪个键。你的脚本可以使用此属性，仅在按下特定按键时做出响应。例如，你可以使用以下代码：

```javascript
let text = document.getElementById("textbox1");
text.addEventListener("keyup", function(event) {
  if (event.keyCode === 80) {
    alert("Please do not press the p key!");
  }
}, false);
```

这将提醒查看者你不希望按下 p 键，因为 80 是键盘上 p 键的键码。你可以在此处查看更多关于键码的信息：http://protocolsofmatrix.blogspot.com/2007/09/javascriptkeycode-reference-table-for.html

## JavaScript：初学者指南

### 使用 addEventListener() 尝试练习 10-2

```
pr10_2.html
prjs10_2.js
```

在这个项目中，你将使用`addEventListener`在一段文本上注册鼠标悬入（mouseover）和鼠标移出（mouseout）事件。

### 步骤详解

- 1. 创建一个 HTML 页面并保存为`pr10_2.html`。添加代码使其链接到名为`prjs10_2.js`的外部 JavaScript 文件。HTML 代码的 body 部分应该如下：

```html
<p>
  This is very <span id="int">interesting</span>!
</p>
```

- 2. 创建一个 JavaScript 文件并保存为`prjs10_2.js`。在步骤 3 中使用它。

- 3. 当鼠标移动到 "int" span 元素时，将颜色更改为 #FF0000。当鼠标移开时，将颜色更改为 #000000。完成后，JavaScript 文件应该如下：

```javascript
let int = document.getElementById("int");
int.addEventListener("mouseover", function() {
  int.style.color = "#FF0000";
}, false);
int.addEventListener("mouseout", function() {
  int.style.color = "#000000";
}, false);
```

- 4. 保存 JavaScript 文件并在浏览器中打开 HTML 文件。将鼠标移到文本上并移开，以更改颜色。

### 练习总结

在这个项目中，你运用了事件处理程序和`addEventListener()`的技能，在鼠标移到文本上或移开时更改文本颜色。

## 使用 EventHandlers 创建脚本

现在你已经掌握了长长的事件处理程序列表和事件对象，是时候玩一点了。在本节中，你将学习执行除发送提示（alert）以外的操作。

## 显示隐藏内容

对于此脚本，创建一个在 body 部分包含以下代码的 HTML 文件，并将其保存为`news.html`。

```html
<div>
  <strong>Breaking News Story!!!!</strong>
  <a href="story.html" id="morelink">More...</a>
</div>
<div id="morediv">
  Today, there was a major development in a story that
  have been coming over here at my site. We will post
  later with further details. Hurry back!
</div>
<script type="text/javascript" src="news.js"></script>
```

在这里，你有一个“突发新闻”标题。下方放置了一个 id 为`morelink`的链接，点击时它将显示故事内容。下方，你有一个包含故事内容的 div（id 为`morediv`）。目前，它是完全可见的，没有应用任何 CSS 或 JavaScript 来改变它。你的目标是初始时隐藏此内容，并在用户激活链接时显示它。

创建一个 JavaScript 文件并保存为`news.js`，你想要做的第一件事是定义一些包含这两个元素的变量：`morelink`和`morediv`。

```javascript
let mlink = document.getElementById("morelink"),
mdiv = document.getElementById("morediv");
```

这些元素现在已作为对象赋值给`mlink`和`mdiv`变量。接下来，你需要添加一个事件监听器，以便在`mlink`元素被点击时显示或隐藏`mdiv`元素，如下所示代码所示：

```javascript
mlink.addEventListener("click", function(event) {
  event.preventDefault();
  mdiv.style.display = (mdiv.style.display === "none") ? "block" : "none";
}, false);
```

# 282 JavaScript：初学者指南

注意有一个包装`div`，它将包含所有内容。其中包含标题`div`、top_story_nav `div`以及三个内容`div`（sumdiv、statdiv 和 comdiv）。脚本将允许每个链接显示其中一个内容`div`，而同时隐藏另外两个。这样用户就可以一次查看一个部分，而不需要滚动到目标部分。

你要做的下一步是使用 CSS 文件为页面添加一些样式。

```css
.wrapper { width:590px; padding:30px; overflow:scroll; }
.headline { font-size:1em; font-family:Verdana, sans-serif; font-weight:bold; font-size:1.8em; font-family:Arial, sans-serif; background-color:#69C9CC; text-align:center; }
.story_nav { margin:0 10px 0 10px; padding:2px; background-color:#DDD; word-spacing:20px; text-align:center; }
.part { margin-bottom:10px; }
```

这定义了包装`div`的尺寸，包含内边距后将为 600x400 像素。它允许所有较长的内容在包装器内由用户滚动。其他样式为其他元素提供了颜色、外边距、内边距和间距。你当然可以根据喜好调整这些内容。

最后，你需要创建一个 JavaScript 文件。将以下代码包含为`tech.js`。

```javascript
let slinks = [document.getElementById("sumlink"),
document.getElementById("statlink"),
document.getElementById("comlink")];
let sdvis = [document.getElementById("sumdiv"),
document.getElementById("statdiv"),
document.getElementById("comdiv")];
function change_div(count) {
  slinks[count].addEventListener("click", function (event) {
    event.preventDefault();
    sdvis[count].style.display = "block";
    for (let j = 0; j < sdvis.length; j++) {
      if (j === count) {
        continue;
      }
      else {
        sdvis[j].style.display = "none";
      }
    }
  }, false);
}
for (let i = 0; i < slinks.length; i++) {
  change_div(i);
}
sdvis[1].style.display = "none";
sdvis[2].style.display = "none";
```

链接连接到三个内容`div`，两组元素都被放入数组中（slinks 和 sdvis）。稍后将解释`change_div()`函数，但

# 第 10 章：事件处理器 283

首先注意函数后的`for`循环。它会遍历`slinks`数组并为每个链接调用`change_div()`函数，并将`i`的值作为参数传递。该参数将用于为每个元素注册点击事件，并在链接被点击时更改相应的内容。

`change_div()`函数接收循环传递的`count`变量作为参数。循环第一次执行时，`change_div()`将接收到值 0，第二次是值 1，依此类推。由于链接和内容`div`是数组，这允许我们使用`count`值来访问所需的元素。函数从`addEventListener()`开始。

监听器被添加到数组中索引为`count`的链接元素上。换句话说，当`count`为 0 时，将访问`slinks[0]`。这访问了第一个链接元素，因为`slinks[0]`的值是`document.getElementById("sumlink")`。由于此运行了三次，事件监听器将带有`count`值 0、1 和 2 被添加。

事件监听器阻止了默认行为。然后，根据点击的链接，通过将相应的样式设置为`block`来显示对应的`div`。循环用于隐藏剩余的元素。如果`j`等于`count`，则跳过；否则将`sdvis[j]`的样式设置为`none`。

最后，在脚本结束时，`statdiv`和`comdiv`元素将被隐藏。这初始化了页面，显示`sumdiv`元素，而另外两个`div`是隐藏的。这是在浏览器中查看时的初始显示。

![](img/a869e8c9d7b9652dd2b8_0.png)

**图 10-9** 初始显示。注意可点击的链接。

## JavaScript：初学者指南

![](img/a869e8c9d7b9652dd2b8_0.png)

图 10-10 点击“Stats”链接的结果。

点击“Stats”链接将显示`statsdiv`（并让其他部分隐藏）。这是点击“Stats”链接的结果。

最后，点击“Comments”链接将显示所有指向我的注释！图 10-11 显示了注释的显示。

此脚本结合了你学到的许多技术（事件、循环、数组等）。数组和循环在这里特别有用，让你避免了编写三个版本的`addEventListener`代码。在处理事件时，拥有这些方便的代码方式很有帮助。

# 自定义事件

现代浏览器允许创建可以在你选择的时间触发（派发）的自定义事件。在创建自定义功能或从另一个源（例如 API 调用）加载完成后触发操作时，自定义事件很有帮助（AJAX 将在第 15 章讨论）。

# 第 10 章：事件处理器 285

![](img/a869e8c9d7b9652dd2b8_3.png)

# Nick 击败了 John

# 总结 统计 注释

**ID0**: 因为那些全局变量，John 输了很奇怪吗？真的吗？

**Anne**: 我预料到了。老实说，Nick 表现更好。

**Paul**: John，我知道这个挑战与气球有关，但在这个比赛中，你本该知道不要覆盖 Array 原型上的`pop()`方法！哇！

**Cod3r**: 这是一个教训。希望 John 能从中学习……

**Conspiracy**: 我觉得这个比赛是人为操纵的……你们没看到吗？

**Doug**: 操纵或者什么？对我看来其中一个人是更好的程序员。John 实际上使用了这行代码；`while (1 == true) { alert('True!'); }`！注释必须重启！

图 10-11 点击“Comments”链接时显示注释。

要创建自定义事件，你可以像下面的代码使用`CustomEvent`构造函数：

```javascript
let introduceSelf = new CustomEvent("introduceself", {
  detail: {
    name: "John"
  }
});
```

> `CustomEvent`构造函数用于创建一个名为`introduceself`的新事件。第二个参数允许你定义在事件派发时可以检索的自定义数据。

注意第一个参数是事件的名称。该名称可以在`addEventListener`方法中处理事件。在这种情况下，事件的名称是`introduceself`。用于派发事件的变量名在本文情况下是`introduceSelf`（注意大写 S）。

# 286 JavaScript：初学者指南

考虑到这些，使用新事件的下一步是监听它并进行派发它，以便事件监听器能够捕获并响应。以下代码显示了一个示例。

使用`addEventListener`和事件名称（来自第一个参数）通过`CustomEvent`构造函数捕获事件。

定义自定义事件：

```javascript
let introduceSelf = new CustomEvent("introduceSelf", {
  detail: {
    name: "John"
  }
});
let introElm = document.getElementById("intro-button");
introElm.addEventListener("introduceSelf", function(event) {
  window.alert(`Hi! My name is ${event.detail.name}`);
});
introElm.dispatchEvent(introduceSelf);
```

将一个 DOM 元素赋值给`introElm`变量。

使用赋值给`CustomEvent`的变量名立即派发事件。

使用在`event.detail`中找到的自定义名称发送事件。注意自定义事件已定义并通过`addEventListener`附加到 DOM 元素上。在这里，事件是立即派发的，但示例中的最后一行可以放在代码的任何地方。注意，对于自定义事件，你必须使用`detail`标识来传递额外信息。使用另一个标识将不起作用，如下面的代码所示：

```javascript
let introduceSelf = new CustomEvent("introduceSelf", {
  name: {
    first: "John"
  }
});
```

在顶层使用标识名而不是`detail`将导致细节无法正确传递。

# 第 10 章自测

- 1. 事件处理器是对象的一个预定义 JavaScript 属性，用于处理 Web 页面上的事件。

  A. 正确

  B. 错误

- 2. 事件处理器非常有用，因为它们使你能够访问页面上可能发生的事件。

- 3. 要使用事件处理程序，你将其放在 HTML 或 JavaScript 中。

- 4. 下面哪项代码正确实现了在点击事件时弹出警报？

  A. `<input type="button" onclick="window.alert('Hey there!');">`

  B. `<input type="button" onclick="window.alert('Hey there!');">`

  C. `<input type="button" onclick="window.alert('Hey there!');">`

  D. `<input type="button" onchange="window.alert('Hey there!');">`

- 5. load 事件在 Web 加载完成时发生。

- 6. mouseover 事件发生在以下情况：

  A. 查看者在鼠标指针悬停在按钮上时点击鼠标。

  B. 查看者将鼠标指针离开链接。

  C. 查看者点击链接、链接图像或图像映射的链接区域。

  D. 查看者将鼠标悬在页面上的某个元素上。

- 7. mouseout 事件在查看者点击页面上的元素时发生。

  A. 正确

  B. 错误

- 8. mouseout 事件在查看者离开当前 Web 页面时发生。

- 9. blur 事件是 focus 事件的相反事件。

- 10. 事件对象包含用于事件的属性和方法。

- 11. 事件的 type 属性包含发生的事件类型。

- 12. submit 事件在查看者提交 Web 页面上的表单时发生。

- 13. keydown 事件在查看者按下键盘上的按键时发生。

  A. 正确

  B. 错误

- 14. 在版本 9 之前的 Internet Explorer 中，可以使用`window.event`方法访问事件对象。

- 15. `addEventListener`和`attachEvent`方法是注册事件的两种新方法。

## 第 11 章

## Node.js 简介

### 核心技能与概念

- 介绍 Node.js

- 安装 Node.js

- 使用 Node 模块

- 安装数据库

- 创建 Web 服务器

到本书为止，你一直都在使用基于浏览器的 JavaScript 为 Web 页面添加功能。近年来，Node.js 的出现扩展了 JavaScript 的使用范围。你不仅可以将它用于基于浏览器的应用程序，现在还可以将其用于本地机器上的应用程序，或者用于创建 Web 服务器并用于服务器端应用程序。

本章将介绍 Node.js，并为你提供有关如何使用它来创建本地应用程序的基本信息。此外，你将接触一种简单的数据库，它允许你存储可以在应用程序中使用的数据。

> 注意

> 尽管本书提供了一些关于 Node.js 和数据库用法的入门信息，但它并不涵盖高级主题。

### 介绍 Node.js

Node.js 最初被创建是为了允许开发者在服务器端使用 JavaScript。它是构建在 Chrome 的 V8 JavaScript 引擎上的运行时环境。Node.js 是异步且事件驱动的，这使得它非常快速且轻量，并且对于网络密集型 I/O 应用具有高度的可扩展性。

Node.js 广泛用于构建实时应用程序，例如聊天应用、游戏服务器和流媒体服务。由于它使用 JavaScript，开发者可以使用同一种语言进行前端和后端开发，这被称为全栈开发。

Node.js 通过 NPM（Node 包管理器）提供了庞大的库生态系统，它是全球最大的软件注册表。这允许开发者轻松地将预写代码集成到他们的项目中。

### 安装 Node.js

要使用 Node.js，你需要在你的操作系统上安装它。Node.js 支持 Windows、macOS 和 Linux。你可以从 Node.js 官方网站下载安装程序。

下载安装程序后，请按照屏幕上的说明操作。安装完成后，你可以打开终端或命令提示符并输入以下命令进行验证：

```
node -v
npm -v
```

如果安装正确，这些命令将显示 Node.js 和 NPM 的版本号。

## 使用 Node 模块

在 Node.js 中，模块是可以包含在项目中的 JavaScript 文件。有三种类型的模块：内置模块、本地模块和第三方模块。

要使用模块，你可以在现代版本中使用`require()`函数或`import`语句。模块允许你在应用程序的不同部分之间共享代码，使其更具条理性且更易于维护。

## 安装数据库

Node.js 可以连接到各种类型的数据库。流行的选择包括 MongoDB、PostgreSQL 和 MySQL。要配合 Node.js 使用数据库，你通常需要通过 NPM 安装驱动程序包。例如，要使用 MongoDB，你需要运行：

```
npm install mongodb
```

## 创建 Web 服务器

Node.js 最强大的功能之一是能够轻松地创建 Web 服务器。使用内置的`http`模块，你可以创建一个监听请求并发送响应的服务器。这是一个简单的 Web 服务器示例：

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(3000, () => {
  console.log('Server running at http://localhost:3000/');
});
```

## 第 11 章：Node.js 简介

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_311_0.png)

### 下载

最新 LTS 版本：10.15.3 (包含 npm 6.4.1)

下载 Node.js 源代码或适用于您平台的预构建安装程序，从今天开始开发吧。

| Windows 安装程序 | macOS 安装程序 | 源代码 |
| :--- | :--- | :--- |
| Windows 安装程序 (.msi) | 32-bit | 64-bit |
| Windows 二进制文件 (.zip) | 32-bit | 64-bit |
| macOS 安装程序 (.pkg) | | 64-bit |
| macOS 二进制文件 (.tar.gz) | | 64-bit |
| Linux 二进制文件 (x64) | | 64-bit |
| Linux 二进制文件 (ARM) | ARMv6 | ARMv7 | ARMv8 |

图 11-1 Node.js 下载页面

用于保存您的项目文件。此文件夹将用于创建书中的示例和项目。

创建一个新的 JavaScript 文件，并简单将该行代码放入其中：

```
console.log("Hello world!");
```

将此文件保存为项目文件夹中的`hello-world.js`。要查看脚本运行效果，您需要在项目文件夹中打开命令提示符（如本章前面的描述所示）。

在命令提示符中，输入以下命令：

```
node hello-world.js
```

按下回车，您将看到结果。文本“Hello there!”将写入命令窗口（控制台），然后返回到命令提示符。图 11-2 显示了脚本完成后命令窗口的样式。

如您所见，`console.log`命令只是向控制台打印一条消息。这与您之前在章节中使用`document.write`执行的操作非常相似，您只需将一个字符串值传递给`console.log`命令，即可将该字符串值打印到控制台。

## 294 JavaScript：入门指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_312_0.png)

**图 11-2** 运行 Hello World 脚本的结果

**注意**

在编写基于浏览器的（前端）JavaScript 时，可以使用`console.log`和其他控制台命令。您将在第 13 章学习更多关于如何在浏览器中使用这些命令。

虽然默认的`console.log`命令对于某些快速日志很有用，但可以使用 Node 模块来添加不同级别的日志，例如调试、警告、错误等。随着本章的学习，您将学习更多关于日志和安装 Node 模块的知识。

### 专家问答

**问：我的系统上无法安装 Node.js。我该怎么办？**

**答：如果您在按照官方网站文档安装 Node.js 时遇到困难，可能需要寻找一个更详细描述您操作系统操作过程的教程。要查看最新的教程，您可以自行搜索，但这里有针对 Windows、Mac 和 Linux 的教程：**

- Windows: http://nodesource.com/blog/installing-nodejs-tutorial-windows/

- Mac: http://nodesource.com/blog/installing-nodejs-tutorial-mac-os-x/

- Linux: http://www.ostechnix.com/install-node-js-linux/

**问：我在 Windows 上安装了 Node.js，但尝试运行 Hello World 脚本时 Windows 仍然无法识别它。我该怎么办？**

**答：在某些情况下，您可能需要检查 Node.js 是否已设置在 Windows 路径中。这通常由安装文件自动为您完成，如果没有，您可以手动将其添加到路径中。关于向 Windows 路径添加程序的信息，请访问 http://helpdeskgeek.com/windows-10/add-windows-path-environment-variable/**

**问：我写的脚本是用于命令行的。我们不是要设置 Web 服务器吗？**

**答：是的，在本章稍晚些时候您将设置一个 Web 服务器。在此期间，您可以使用命令行脚本做一些随时间推移可能会很有帮助的事情，随着本章的深入，您将看到更多内容。**

## 使用 Node 模块

Node 模块允许您扩展 Node.js 脚本提供的默认功能。某些 Node 模块无需安装即可使用，而另一些则需要在安装后才能使用。

## 使用原生 Node 模块

您只需在 JavaScript 文件中包含它，即可在脚本中使用原生 Node 模块。常用的原生模块是文件系统模块 (fs)。您可以通过引入该模块并将结果赋值给变量（通常变量名与模块名匹配）来包含它。例如，以下是在您的 Hello World 脚本中包含 fs 模块的方法：

```javascript
const fs = require("fs");
console.log("Hello there!");
```

> fs 模块通过`require`语句包含。

这并不意味着您不需要使用 fs 模块。就像您之前使用的命令一样，fs 具有某些可以调用的方法。例如，fs 的`mkdir`方法允许您在本地机器上创建（制作）一个目录（文件夹）。

## 异步执行

Node.js 的默认行为是允许在特定操作可能需要耗时的情况下运行其他代码。这通常被称为非阻塞，意味着启动操作可能需要时间，但不会阻塞其他代码在等待操作完成时继续执行。当操作完成后，通常会有一个函数（在这种情况下，可以被称为回调函数）在完成后执行。

# 298 JavaScript：初学者指南

再次运行脚本（记得删除 test-folder 或在脚本中使用不同的文件夹名称），`fs.mkdirSync`之后的代码在文件夹创建完成之前不会运行。因此，操作完成后，消息将打印到控制台。

使用 Node 方法的同步版本会使代码以同步方式运行，但这通常不是最佳实践，因为异步代码不会阻塞其他程序的运行。这对于用户来说总是好的，因为当异步函数等待操作完成时，他们可以继续与程序进行交互。同步代码将强迫用户与其一起等待，这通常在用户看来并不是非常积极的！但请记住，使用异步代码时，你不能假设某个操作已完成并在回调方法中放置任何依赖项。

## 非原生模块

要在你的 Node.js 脚本中包含非原生模块，你有几种选择：你可以从 npm（Node 包管理器库）中包含一个顶级模块，也可以编写自己的模块并将其包含进来。如果 npm 上有你需要的包，你可以在你的项目中安装该包并使用它。如果没有，或者你只是想编写自己的模块代码，你可以这样做并将该模块包含在你的脚本中。

## Node 包管理器

如果你想查找并使用已经作为包提供的模块，可以在 www.npmjs.com 上的 npm 库中查找。在搜索栏中，你可以通过名称搜索包并查看更多详细信息。例如示例，你只需安装 Express 包，它允许你使用 Node.js 快速创建一个 Web 服务器。

默认情况下，Node.js 自带一个 npm 副本，但这个副本可能不是最新的版本。你可能希望在开始使用之前更新 npm。要这样做，请进入控制窗口并更新以下内容：

```
npm install latest -g
```

这应该将 npm 更新到最新版本。

### 注意

某些版本的 Windows 可能无法通过此命令完全更新 npm，因为所选的控制窗口可能尚未找到新版本。如果你的系统没有更新，你可以使用 www.npmjs.com/package/npm-windows-upgrade 工具。

完成后，你可以使用 npm 将包安装到你的项目目录。例如，在你的项目文件夹中打开命令行窗口并运行以下命令：

```
npm install express
```

# 第 11 章：Node.js 简介 299

这将在你的项目文件夹中安装 Express 包。如果你的项目中还没有`node_modules`文件夹，它将被创建，Express 包将位于该文件夹中。`node_modules`文件夹中的任何模块都可以在指定路径的情况下包含（正如你将看到的）。

### 注意

如果`npm install`产生权限错误，你可能需要以管理员身份运行命令行窗口（Windows）或使用`sudo`（Linux）来获得正确的权限。

一旦安装了模块，使用它的过程与使用原生模块相同。引入模块然后在你的脚本中使用它。例如，将代码保存为`include-express.js`并在控制窗口中输入`node include-express.js`运行它，如下：

```javascript
const express = require("express");
let http = express();
console.log("Express has been included and used!");
```

你应该能看到打印到控制台的消息。在本章稍后的部分，你将学习如何使用 Express 为应用程序创建一个 Web 服务器。

## 自定义模块

自定义模块类似于你之前用于浏览器的 JavaScript 外部脚本，但提供了更多选项。要创建一个自定义模块，你只需将代码写入单独的 JavaScript 文件中，确保它导出了代码，然后像处理其他类型的模块一样在你的主脚本中引入它。

例如，将以下代码保存为项目文件夹中的`calculate-sum.js`：

```javascript
let calculateSum = function (value1, value2) {
  return value1 + value2;
}
```

注意，此文件包含一个可以调用以计算两个值之和的函数。该函数可以改进以检查两个值是否已发送、是否为数字并提供错误消息，但对于这个简单的示例，足够了。

接下来，将以下代码保存为`get-monthly-income.js`：

```javascript
const sum = require("./calculate-sum");
let paycheck1 = 1500;
let paycheck2 = 1700;
let monthlyIncome = sum.calculateSum(paycheck1, paycheck2);
console.log(`My monthly income is ${monthlyIncome}`);
```

调用了自定义模块的`calculateSum`函数并将工资值作为参数传递。

函数返回的值被打印到控制台。

## JavaScript：初学者指南

注意，一旦引入了自定义模块，一切的工作方式与使用原生模块非常相似。然而，在编写模块时有一点你需要记住：你需要导出你希望在脚本使用的值或函数。之前的代码将失败，因为它无法找到`sum.calculateSum`函数。

要修复这个问题，回到你的`calculate-sum.js`文件并将其更新为以下代码：

```javascript
let calculateSum = function (value1, value2) {
  return value1 + value2;
}

module.exports = {
  calculateSum: calculateSum
};
```

# 302 JavaScript：初学者指南

在 Node.js 中使用数据库通常只需要使用一个模块，它允许你编写 JavaScript 代码来查询数据库并获取结果。但在此之前，你将需要安装一个数据库。对于本书而言，你只需要在你的计算机上安装一个数据库即可。如果你是为网站或 Web 应用程序使用数据库，你将需要将数据库安装在你的网站/应用程序可以访问的服务器上（如果你处于托管环境中，几乎每个 Web 主机都提供某种类型的数据库）。作为开始，你只需要在你的计算机上安装一个数据库以便本地使用，并熟悉从 Node.js 对其进行查询。

## 数据库选项

你有许多数据库可以选择。从 MySQL、MongoDB、PostgreSQL 到 Oracle 等，有很多都提供了丰富的选项。最终选择取决于你的实际情况，并且可能随项目而异。

对于本书而言，将使用 PostgreSQL。如果你愿意，也可以使用其他数据库，尽管不会提供其他数据库的说明。不过，如果你选择其中一种 SQL 数据库，其查询语句与 PostgreSQL 的查询非常相似，甚至相同（尽管从 Node.js 运行查询的模块可能使用不同的语法）。

### 注意事项

如果你使用像 MongoDB 这样的 NoSQL 数据库，情况会有所不同，但如果你之前有一定的相关经验，你仍然能够配合不同的查询结构和语法来完成练习。

## 安装 PostgreSQL

要安装 PostgreSQL，请访问 www.enterprisedb.com/downloads/postgres-postgresql-downloads。在这里，你需要按照适用于你操作系统的下载和安装说明进行操作。对于 Windows 等操作系统，将下载一个安装程序，你可以运行它并按照屏幕提示操作。为了本书中的用途，你只需保持所有默认选项即可。最需要记住的是系统提示你输入的密码。请务必记住此密码，因为你需要访问 pgAdmin 实用工具，它将允许你创建用户、数据库、表等。

如果你在安装过程中需要帮助，这里有一些教程可以帮助你了解更详细的信息：

- Windows: www.guru99.com/download-install-postgresql-sql-setup/

- Mac: www.robinwier.de/postgresql-macos-setup/

- Linux: www.poftum.com/how-to-install-postgresql-server-into-linux-ubuntu-centos-mint-fedora-redhat/

一旦安装了 PostgreSQL 并获取了主（超级用户）密码，你就可以准备开始使用数据库服务器创建用户、数据库、表等了。

# 第 11 章：Node.js 简介 303

## 使用 pgAdmin 创建数据库

安装过程应该已经安装了 pgAdmin 工具。打开此工具，在左侧面板中，展开 Servers（服务器）节点。这将显示节点 "PostgreSQL X.X"（其中 X.X 被替换为已安装的 PostgreSQL 版本）。要展开此节点，系统会提示你输入在安装期间创建的超级用户密码。输入密码并按回车。图 11-3 显示了 pgAdmin 中的密码提示。

一旦成功输入密码，左侧面板中将出现更多可用节点，如图 11-4 所示。

从这里开始，右键点击 Databases（数据库）节点并选择 Create（创建）下的 Database（数据库）选项。这将弹出图 11-5 所示的提示。

输入数据库名称（命名为 mywebapp），点击窗口底部的 Save（保存）按钮，然后关闭窗口。你刚刚创建了一个供你使用的数据库！

## 创建表

一旦准备好数据库，你将想要向其中存入一些数据。对于你创建的简单 Web 应用程序，这可以通过 pgAdmin 内部的 SQL 查询简单地完成。

首先，在左侧面板中选择你的数据库 (mywebapp)。接着，进入顶部菜单，选择 Tools（工具），然后选择 Query Tool（查询工具）。右侧将显示一个新的查询标签页。图 11-6 显示了如何在 pgAdmin 4 中选择 Query Tool。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_321_0.png)

图 11-3 pgAdmin 提示密码

# 304 JavaScript：初学者指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_322_0.png)

create table（创建表）命令允许你创建一个表并为其赋予具有特定数据类型的列。这些数据类型与 JavaScript 中使用的类型不同，而是 PostgreSQL 的数据类型。你会发现姓和名字的类型是 varchar，它代表可变字符（character varying）。括号中的数字指的是列中任何数据的最大长度。对于姓和名，最大长度为 20 个字符。其余列使用 smallint 和 text 数据类型（范围从 -32768 到 32767 的最小整数，text 类似于 varchar 但没有长度限制）。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_322_1.png)

# 第 11 章：Node.js 简介 305

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_323_0.png)

图 11-6 pgAdmin 工具选择

insert（插入）命令允许你向表中插入数据。在这种情况下，通过列出列名（第一组括号内）和值（第二组括号内）来完成。注意字符数据需要引号，而数值数据不需要。

接下来，你只需要输入一个查询来创建一个新表。在图 11-7 所示的查询面板中，点击顶部的闪电按钮。

为了让表和数据存在，你可以使用 Query Tool 并输入以下查询：

```sql
SELECT * FROM bowlers;
```

图 11-8 显示了该查询的结果。

该 SQL 语句表示你想从数据库中选择数据。在这种情况下，你使用了星号 (*) 来请求所有列。现在你不仅有一个数据库，还拥有了可以使用的数据。

# 306 JavaScript：初学者指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_324_0.png)

图 11-7 向表中插入信息的查询

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_324_1.png)

图 11-8 选择所有数据的结果

# 第 11 章：Node.js 简介 307

## 添加查询用户

虽然从超级用户账户查询数据库对于管理数据库、表、用户等非常方便，但让超级用户查询你的应用程序并不是好主意。由于超级用户可以删除任何内容，你程序中的一个错误代码或一个恶意用户能够在你的数据库上运行查询，都可能导致巨大的数据丢失甚至完全的安全漏洞。出于这些原因，最好是为你的 Web 应用程序创建一个独立的用户，并仅授予其使用 Web 应用程序所需的权限。

对于你将创建的 Web 应用程序，新用户只需要能够从 mywebapp 数据库查询数据。你首先需要创建用户并使用数据库上的授权向导授予正确的权限。

要创建新用户，在 pgAdmin 的左侧面板中右键点击 Login/Group Roles（登录/组角色）节点。选择 Create Login/Group Role。弹出一个需要用户名称的提示。在这种情况下，输入名称 mywebappuser。如图 11-9 所示。接着，进入 Definitions（定义）标签页并为新用户输入密码。之后，点击 Privileges（权限）标签页，使用图 11-10 所示的值，然后点击屏幕底部的 Save（保存）按钮保存新用户。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_325_0.png)

图 11-9 为新用户命名

# 308 JavaScript：初学者指南

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_326_0.png)

**图 11-10** 为新用户设置权限

用户保存后，你将允许该用户访问你的 mywebapp 数据库。在左侧面板中，选择你的 mywebapp 数据库，右键点击该节点并选择“Grant Wizard”（授权向导）。将弹出一个提示要求你选择一张表。通过勾选框选择 bowlers 表，然后点击屏幕底部的“Next”（下一步）按钮。

下一个屏幕提示你为表格添加权限。点击表格右上角的`+`按钮将添加新行。在 Grantee（授予者）列中，从下拉列表中选择你的新用户`mywebappuser`。接下来，点击空白的 Privileges（权限）列。这将显示一系列复选框。仅勾选 SELECT 复选框，这将仅允许用户对数据库执行查询（如果你以后决定还要插入数据，可以回来再次勾选 INSERT 复选框）。图 11-11 显示了勾选 SELECT 的屏幕。最后，点击屏幕底部的“Finish”（完成）按钮。你的新用户现在应该能够从数据库选择数据了！

# 添加更多数据

在完成数据库设置之前，你将向 bowlers 表添加几行。目前，运行接下来的 insert 查询将添加四个条目，总共五行数据。一旦你创建了 Web 应用，就可以多种方式查询这些数据，这可能对用户很有帮助。

# 第 11 章：Node.js 简介 309

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_327_0.png)

图 11-11 为用户授予权限

首先，返回左侧面板选择你的 mywebapp 数据库。进入“Tools”（工具）并再次选择“Query Tool”（查询工具）。在查询面板中，使用以下查询向你的表格添加更多数据。请注意，你可以根据喜欢更改名称或数字，但我们将使用此特定查询中的信息作为书中的示例。

```sql
INSERT INTO bowlers (last_name, first_name, accuracy, power, consistency, bio) VALUES (
'Gutter',
'Doctor',
55,
47,
62,
'Likes to talk trash, but cannot knock down many pins.'
);
INSERT INTO bowlers (last_name, first_name, accuracy, power, consistency, bio) VALUES (
'Shoes',
'Cranky',
67,
94,
71,
'Can roll the ball very fast. A bit inconsistent and might even throw the ball at you.'
);
INSERT INTO bowlers (last_name, first_name, accuracy, power, consistency, bio)
VALUES (
'Roller',
'Slow',
82,
39,
93,
'Might take a long time to finish a turn, but is quite accurate.
Does not knock down pins though.'
);
INSERT INTO bowlers (last_name, first_name, accuracy, power, consistency, bio)
VALUES (
'Winner',
'Prize',
97,
95,
98,
'Great all-around bowler. Play someone else if you want to win.'
);
```

注意，较长的字符串需要在查询面板中单行显示。在面板中输入查询后，按 F5 运行它，并将新数据行添加到你的 bowlers 表中。

# 使用 pg 模块

关于你的新数据库（目前），你需要的最后一点知识是如何在 Node.js 程序中查询数据库。要实现这一点，你可以使用`pg`模块。首先，在你的项目文件夹中打开命令行窗口，输入以下命令安装 pg 模块：

```bash
npm install pg
```

安装模块后，在项目文件夹中新建一个文件并保存为`pg_example.js`。添加以下代码，将`12345`替换为`mywebappuser`创建的密码，然后保存。

```javascript
const { Pool } = require('pg');
const connectionString = 'postgresql://mywebappuser:12345@localhost:5432/mywebapp';
const pool = new Pool({connectionString});
pool.query(
  'SELECT * FROM bowlers',
  function (err, result) {
    if (err) {
      console.error(err);
      process.exit(1);
    }
    console.log(result.rows);
    process.exit(0);
  }
);
```

# 第 11 章：Node.js 简介 311

```
C:\JPAGB-Ed-5-Meeting\Chapter 11\708_11Project_Code\node pg_example.js
[{ last_name: 'swell', first_name: 'Coach', accuracy: 72, power: 71, consistency: 84, bio: 'Used to play a lot, but now coaches.'}, {last_name: 'Gutter', first_name: 'Doctor', accuracy: 55, power: 47, consistency: 62, bio: 'Likes to talk trash, but cannot knock down pins.'}, {last_name: 'Shoes', first_name: 'Cranky', accuracy: 67, power: 94, consistency: 71, bio: 'Can roll the ball very fast. A bit inconsistent and might even throw the ball at you.'}, {last_name: 'Roller', first_name: 'Slow', accuracy: 82, power: 39, consistency: 93, bio: 'Might take long time to finish a turn, but is quite accurate. Does not knock down pins though.'}, {last_name: 'Winner', first_name: 'Prize', accuracy: 97, power: 95, consistency: 98, bio: 'Great all-around bowler. Play someone else if you want to win.' }]
```

# 图 11-12 运行 pg_example.js 的结果

你会发现包含了`pg`模块，并使用连接信息设置了一个“池”来查询数据库并返回结果。连接信息只是指向 PostgreSQL 数据库服务器的字符串，提供了用户名、密码、主机和数据库名称。

设置完成后，你可以使用`pool.query()`函数提供查询（第一个参数）、数组中的查询参数（在本例中为空数组），并在查询完成后运行该函数。在这个函数中，你可以得到错误（`err`参数）或结果（`result`参数）。在这些代码中，如果发生错误，错误将显示在控制台上；如果查询成功，Node 进程将退出，结果将打印到控制台上。图 11-12 显示了运行此脚本的结果。

结果是一个对象数组，包含了存储在数据库中的每个保龄球员的信息！

# 312 JavaScript：初学者指南

# 尝试 11-2 测试 SQL 查询

| 无需文件，只需 pgAdmin |
| :--- |

此项目将允许你尝试通过查询执行的一些其他操作来缩小结果范围。到目前为止，你只是得到了所有行，但通过稍微修改查询，你可以获得更少的甚至单行。

# 步骤说明

1. 在 pgAdmin 中，在左侧面板选择你的 mywebapp 数据库。

2. 进入“Tools | Query Tool”，并在查询面板中输入以下内容：

```sql
SELECT * FROM bowlers WHERE accuracy > 80;
```

3. 按 F5 运行查询。注意，只有准确率大于 80 的保龄球员会出现在结果列表中。在这种情况下，结果应该是`Slow Roller`和`Prize Winner`的信息。添加`WHERE`子句可以将结果缩小为仅符合条件的项目。

4. 将查询更改为：

```sql
SELECT * FROM bowlers ORDER BY power DESC;
```

5. 按 F5 运行此查询。注意，所有行都返回了，但它们是按力量评分从高到低排序的。`ORDER BY`可以根据特定列的值对结果进行排序；无论是降序还是升序（ASC）顺序。

6. 将查询更改为：

```sql
SELECT first_name, last_name FROM bowlers WHERE consistency >= 80;
```

7. 按 F5 运行查询。注意，现在只返回一致性大于等于 80 的保龄球员的姓和名。将`*`替换为一个或多个列名将返回的列数限制为命名的列。

### 尝试总结

在这个项目中，你通过 pgAdmin 中的“Query Tool”尝试了一些额外的`SELECT`查询。你能够精炼查询以不同的方式获取信息，或者限制返回的行或列的数量。要了解更多关于查询的操作，请参阅 beginner-sql-tutorial.com/sql-select-statement.htm。

# 创建 Web 服务器

使用 Node.js 创建 Web 服务器有许多选项。事实上，如果你愿意，你也可以编写自己的代码来实现。到目前为止，标准做法是使用 Express 模块，它让其中的很多工作变得简单了许多。

对于这个项目，你想要创建一个非常简单的 Web 服务器，它可以监听特定的端口，并在你访问特定路由（route）时渲染一个 HTML 文档——最常见的是基础路由 '/' 或“主页”。对于本地 Web 服务器来说，这意味着你希望能够在 Web 浏览器中打开 http://localhost 并看到一个显示的 HTML 页面。

首先，在你的项目文件夹中创建一个 HTML 文件，并输入以下代码，然后将其保存为 index.html：

```html
<html>
<head>
  <title>My Web App</title>
</head>
<body>
  The web server is working!
</body>
</html>
```

接下来，你想要创建一个可以作为 Node 脚本运行的 JavaScript 文件。在你的项目文件夹中创建另一个新文件，并输入以下代码，然后将其保存为 server.js：

```javascript
const express = require('express');
const app = express();
const router = express.Router();
const path = require('path');

router.get('/', function (req, res) {
  res.sendFile(path.join(__dirname, 'index.html'));
});

app.use('/', router);

let server = app.listen(3000, function () {
  console.log("App Server via Express is running on port 3000");
  console.log("To end, press Ctrl + C");
});
```

首先，注意代码的前三行：

```javascript
const express = require('express');
const app = express();
const router = express.Router();
```

## JavaScript：初学者指南

立即包含了 Express 模块。通过调用`express()`函数创建了一个“应用（app）”。一旦设置完成，此应用将积极监听端口，并使用路由器（router）将你引导到正确的 HTML 页面。正如提到的，第三行设置了一个 Express 路由器，允许你定义哪些路由将进行渲染。路由可以是任何内容，从用于主页面的 '/' 到 /view/statistics_route（后者在访问时将打开统计页面）。Express 让你轻松设置任何你需要的路由并以适当的方式响应这些路由。

接下来，包含了`path`模块。该模块允许你轻松地导航机器上的文件路径。这将在脚本稍后中使用。

接下来的代码定义了路由器：

```javascript
router.get('/', function (req, res) {
  res.sendFile(path.join(__dirname, 'index.html'));
});

app.use('/', router);
```

如你所见，`router.get()`函数允许你定义用户尝试从该路由获取信息时会发生什么。最常见的情况是通过渲染某种 Web 页面来响应——无论是静态的还是动态的。在这种情况下，一个简单的 HTML 页面即可，因此使用`res.sendFile()`来发送文件。在这里，它发送了你在本节之前创建的 index.html 文件。`path.join`用于将 server.js 文件所在的文件夹（`__dirname`完成了这部分）与要渲染的文件名（在本例中为项目文件夹中的 index.html 文件）结合起来。

你可以以相同的方式定义额外的路由，但目前通过向脚本中添加`app.use('/', router)`这一行完成了路由器的设置。

最后，`app.listen()`函数告诉 Express 应用监听哪个端口，以及在监听时是否执行任何操作。要运行该应用（在本例中为端口 3000），请将你的浏览器指向 http://localhost:3000。

文件就绪后，进入命令行窗口并输入以下内容：

```bash
node server.js
```

你应该会收到日志信息，说明服务器正在端口 3000 上运行以及如何停止服务器。一旦运行，进入你的 Web 浏览器并访问 http://localhost:3000。你应该能看到显示“Web server is working!”的简单 Web 页面！

有了这些，你现在可以使用你的 Web 服务器创建一个简单的 Web 应用，它甚至可以显示你存储在数据库中的信息。当你继续阅读本书的其他部分并完善此项目时，你将学习从前端到服务器获取数据的请求！

# 第 11 章自测

- 1. Node.js 运行在 Web 浏览器中。

  A. 正确

  B. 错误

- 2. 下列哪项将从命令行窗口运行 Node 脚本 hello-world.js？

  A. node hello-earth.js

  B. hello-world.exe

  C. node hello-world.js

  D. hello-world

- 3. 下列哪项在不报错的情况下需要内置的 fs 模块？

  A. const fs = req('fs');

  B. const fs = require('fs');

  C. require('FileSystem');

  D. const fs = require('fs');

- 4. 一个 _______ 模块允许你定义自己的可重用代码。

- 5. 下列哪种扩展将用于自定义模块？

  A. .js

  B. .html

  C. .json

  D. .dll

- 6. 只使用一种类型的数据库。

  A. 正确

  B. 错误

- 7. _______ 模块包含了 MongoDB、AngularJS 和 NodeJS。

- 8. 下列哪项用于查询数据库？

  A. 正确

  B. 错误

- 9. _______ 模块用于查询数据库。

  A. gp

  B. post

  C. pg

  D. postgres

- 10. 哪个符号用于查询所有列？

  A. *

  B. ~

  C. -

  D. ...

- 11. _______ 模块用于创建 Web 服务器。

- 12. 当你输入 URL 时默认端口是。

  A. 442

  B. 80

  C. 3000

  D. 5432

- 13. _______ 处理用户尝试访问路由时的情况。

  A. redirector

  B. pathfinder

  C. routermapper

  D. router

- 14. 你应该允许删除数据。

  A. 正确

  B. 错误

- 15. 你可以使用 _______ 子句返回符合特定标准的行。

  A. WHERE

  B. WHEN

  C. IF

  D. CRITERION

# 第 12 章 Math、Number 和 Date 对象

## JavaScript：初学者指南

# 技能与概念

- 使用 Math 对象

- 理解 Number 对象

- 使用 Date 对象

在本章中，你将学习 JavaScript 的 Math、Number 和 Date 对象；对于每个对象，都提供了简要介绍以及该对象实用的描述。随后将介绍你可以使用的各种属性和方法。

# 使用 Math 对象

当你需要在脚本中执行各种计算时，Math 对象是非常有用的。首先，看看 Math 对象是什么。

# 什么是 Math 对象？

Math 对象是一个预定义的 JavaScript 对象。就像你在书中学习过的其他预定义对象一样，Math 对象提供了可使用的属性和方法。Math 对象用于数学目的，提供数学常数的值或执行计算和操作。

# Math 对象为何有用

正如提到的，当你需要在脚本中进行数学计算时，Math 对象非常有用。例如，如果你计算时需要 pi 值，Math 对象提供了一个属性供你获取该值。此外，如果你需要找到数字的平方根，Math 对象的一个方法允许你实现这一点。该对象提供的另一个功能是在 JavaScript 中生成随机数，这对某些脚本非常有用。

### 属性

Math 对象提供了许多属性可以帮助你执行某些数学计算。表 12-1 列出了 Math 对象的属性以及每个属性的值。如表 12-1 所示，所有属性都只持有用于数学计算的数值。由于这些是无理数，列出的值是非无限的，因此是近似值。注意这些属性采用全大写，这是因为它们是常量值，而此类常值的命名约定是必须全大写字母。

# 第 12 章：数学、数字和日期对象 319

| 属性 | 值 |
|---|---|
| E | 欧拉常数 (E) 的值，约等于 2.71828... |
| LN10 | 10 的自然对数值，约为 2.302585... |
| LN2 | 2 的自然对数值，约为 0.693147... |
| LOG10E | E 的以 10 为底的对数，约为 0.43429... |
| LOG2E | E 的以 2 为底的对数，约为 1.442695... |
| PI | 圆周率 pi 的值，通常用于圆计算，约为 3.14159... |
| SQRT2 | 2 的平方根值，约为 1.414... |
| SQRT1_2 | 二分之一的平方根值，约为 0.7071... |

# 表格 12-1 Math 对象的属性

### 使用属性

属性包含只读值，这些值通常用于特定类型的计算。例如，如果你想计算圆的面积，可以使用公式 Area = pi*r²。在知道此后，你可以编写一个应用程序，根据查看者输入的半径来确定圆的面积。你可以使用以下代码，从 HTML 代码开始：

```html
<form id="getarea">
<label for="radius">Enter a radius:</label><br>
<input type="text" id="radius">
<input type="submit" value="Get the Area">
</form>
```

接下来是 JavaScript 代码：

```javascript
let area_form = document.getElementById("getarea");
area_form.addEventListener("submit", function (event) {
let rad = document.getElementById("radius").value;
let the_area = 0;
if (rad.length < 1) {
  event.preventDefault();
  alert("Please enter a radius!");
  return;
} else {
  event.preventDefault();
  rad = !isNaN(rad) ? +rad : false;
  if (rad === false) {
    alert("Radius must be numeric!");
    return;
  }
}
  the_area = Math.PI * (rad * rad);
  alert("The area is " + the_area + " square units.");
}, false);
```

这段代码首先通过 id (getarea) 获取表单并将其赋值给名为`area_form`的变量。当表单被提交时，它获取在文本框中输入的半径值，并将其赋值给名为`rad`的变量。

接下来，代码执行了两项检查。它检查`rad`的长度是否小于 1，如果小于 1，代码将弹出一个提示要求查看者输入信息。接着，它检查`rad`的值是否为数字。这是通过使用`isNaN()`函数实现的，该函数在值不是数字时返回`true`。由于你想测试它是否为数字，在前面加上非运算符`!`会使得该值不返回`NaN`，从而它是数字。如果不是如此，它将被赋值为布尔值`false`。随后语句将检查`rad`的值，如果无法强制转换为数字，将向查看者发送警报说`rad`必须是数字。

最后，如果数据通过了这些测试，将进行圆的面积计算并赋值给变量`the_area`。注意，现在你将半径乘以自身以得到半径平方。当计算完成并赋值给变量后，向查看者显示警报，单位为“平方单位”。该脚本可以修改以适应你的需求或提供不同的选项（厘米、英寸或其他单位）。

图 12-1 显示了在浏览器中向文本框输入 2 的脚本结果。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_340_0.png)

图 12-1 向查看者显示圆的面积。

# 第 12 章：数学、数字和日期对象 321

### 方法

`Math`对象的方法允许你执行某些对你的脚本有帮助的计算。表 12-2 列出了`Math`对象的基本方法并简要描述了每个方法的作用。后续章节将详细讨论每个方法。此外，一些额外的方法可以在 developer.mozilla.org/en-US/docs/Reference/Global_Objects/Math#Methods 找到。

## 基本方法

为了方便，“基本方法”定义为接收单个数字、对其进行简单计算并返回值的方法。以这种方式对方法进行分组避免了在讨论中列出每一个方法。

| 方法 | 用途 |
|---|---|
| `abs()` | 返回作为参数数字的绝对值 |
| `acos()` | 返回作为参数数字的反余弦值（弧度） |
| `asin()` | 返回作为参数数字的反正弦值（弧度） |
| `atan()` | 返回作为参数数字的反正切值（弧度） |
| `atan2()` | 返回两个参数数字之商的反正切值（弧度） |
| `ceil()` | 返回大于或等于参数数字的最小整数 |
| `cos()` | 返回作为参数数字的余弦值（弧度） |
| `exp()` | 返回 E 的参数数字的次方 |
| `floor()` | 返回小于或等于参数数字的最大整数 |
| `log()` | 返回作为参数数字的自然对数 |
| `max()` | 返回两个参数数字中的较大者 |
| `min()` | 返回两个参数数字中的较小者 |
| `pow()` | 返回第一个参数数字的第二个参数幂 |
| `random()` | 返回 0 到 1 之间的随机数；不需要参数 |
| `round()` | 返回四舍五入到最近的整数 |
| `sin()` | 返回作为参数数字的正弦值（弧度） |
| `sqrt()` | 返回作为参数数字的平方根 |
| `tan()` | 返回作为参数数字的正切值（弧度） |

表格 12-2 Math 对象的方法

# 322 JavaScript：初学者指南

以下基本方法的工作方式大致相同：

- `abs()`

- `acos()`

- `asin()`

- `atan()`

- `cos()`

- `exp()`

- `log()`

- `sin()`

- `sqrt()`

- `tan()`

这些基本方法中的每一个都接收一个数字值并返回另一个值。由于通用用法相同，本讨论使用`sqrt()`作为示例来说明如何使用它们获取值。如果你需要知道不同方法返回什么类型的值，请参考表 12-2 查看每个方法的功能。

使用`sqrt()`方法最简单的方法是将正数作为参数传递给方法，如下所示：

```javascript
window.alert(Math.sqrt(4));
```

这会弹出 4 的正平方根值，即 2。

与其计算一个平方数，不如让用户输入一个数字，并将用户输入的数字的平方根发送警报。你可以使用以下代码来实现，从 HTML 代码开始：

```html
<form id="getroot">
<label for="sr_num">Enter a (positive) number or zero:</label>
<input type="text" id="sr_num">
<input type="submit" value="Get a Square Root">
</form>
```

接下来是 JavaScript 代码：

```javascript
let root_form = document.getElementById("getroot");
root_form.addEventListener("submit", function(event) {
  let thenum = document.getElementById("sr_num").value;
  thenum = !isNaN(thenum) ? thenum : false;
  event.preventDefault();
  if (!thenum || (thenum.length < 1)) {
    alert("Input is required and must be numeric!");
    return;
  } else if (thenum < 0) {
    alert("Hey! I said to enter a positive number! Try again.");
    return;
  } else {
    let theroot = Math.sqrt(thenum);
    alert("The square root of " + thenum + " is " + theroot);
  }
}, false);
```

当用户提交表单时，输入到文本框的值被赋值给`thenum`变量。之后，它会检查该字段是否为空或输入的数据是否不是数字。任何一种情况都会向观众提示错误。否则，将使用`thenum`的值作为参数调用`Math.sqrt()`方法。这将返回数字的平方根，然后将其赋值给名为`theroot`的变量。最后，会弹出一个提示告诉用户平方根信息。当观众输入数字 4 时，此脚本的结果如图 12-2 所示。本节中的其他方法原理非常相似；它们只是返回绝对值、正切值或对数的不同结果。

## 双参数方法

本节讨论了接受两个参数而不是一个参数的方法。这些方法包括：

- `atan2()`

- `max()`

- `min()`

- `pow()`

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_341_0.png)

图 12-2 为观众显示平方根。

### JavaScript：初学者指南。

`max()`和`min()`方法非常相似，而`pow()`方法的作用略有不同。

**max() 和 min() 方法** `max()`接收两个或多个数字并返回最大的数字。`min()`方法也接受两个或多个参数，但返回的是较小的数字。你可以在脚本中使用这些方法，允许观众输入两个数字并提示用户哪个数字更大。

示例代码同时使用了这两种方法，并在提示框中给观众提供结果。首先是 HTML 代码：

```html
<form id="getmax">
输入两个数字以查看哪个更大：<br><br>
<label for="num1">数字 1</label>
<input type="text" id="num1">
<label for="num2">数字 2</label>
<input type="text" id="num2">
<input type="submit" value="哪个数字更大？">
</form>
```

接下来是 JavaScript 代码：

```javascript
let max_form = document.getElementById("getmax");
max_form.addEventListener("submit", function(event) {
  let num1 = document.getElementById("num1").value;
  let num2 = document.getElementById("num2").value;
  let largen = 0;
  let small = 0;
  num1 = (+num1) === 0 ? +num1 : false;
  num2 = (+num2) === 0 ? +num2 : false;
  event.preventDefault();
  if ((num1 !== false) && (num2 !== false)) {
    largen = Math.max(num1, num2);
    small = Math.min(num1, num2);
    if (largen === small) {
      alert("两个数字相等！");
    } else {
      alert(largen + " 比 " + small + " 大");
    }
  } else {
    alert("仅输入数字值。");
  }
}, false);
```

此表单允许观众输入两个数字并将它们赋值给变量。将进行检查以确保数值是数字。如果是的话，它将获取两个数字中的最大值和最小值，并将值赋值给变量。然后使用这些变量来检查它们是否相等。如果是，会弹出提示框显示它们相等；否则，会弹出一个提示框显示结果。

## 第 12 章：Math、数字和日期对象 325

接下来的插图显示了当观众第一个数字输入 2，第二个数字输入 54 时，该脚本在浏览器中的结果。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_343_0.png)

**pow() 方法** `pow()`方法接受两个参数，并计算第一个参数的第二个参数的幂。例如，以下代码将返回 2 的 3 次幂：

```javascript
Math.pow(2,3);
```

除了计算方式有所不同外，你可以像使用其他两个双参数方法一样使用它，将结果赋值给变量，然后在脚本中使用该变量。例如，你可以使用以下脚本，从 HTML 代码开始：

```html
<form id="getpow">
  <label for="base">基数:</label>
  <input type="text" id="base">
  <label for="exp">指数:</label>
  <input type="text" id="exp">
  <input type="submit" value="计算幂">
</form>
```

接下来是 JavaScript 代码：

```javascript
let pow_form = document.getElementById("getpow");
pow_form.addEventListener("submit", function(event) {
  let base = document.getElementById("base").value;
  let exp = document.getElementById("exp").value;
  let result = 0;
  base = (+base) === 0 ? +base : false;
  exp = (+exp) === 0 ? +exp : false;
  event.preventDefault();
  if ((base !== false) && (exp !== false)) {
    result = Math.pow(base, exp);
    alert(base + " 的 " + exp + " 次幂是 " + result);
  } else {
    alert("仅输入数字值。");
  }
}, false);
```

## 345 Math、数字和日期对象 327

现在你已经了解了双参数方法，让我们来看看一些接受单参数的其它方法：

- `ceil()`

- `floor()`

- `round()`

**ceil() 方法** `ceil()`方法代表向上取整，返回大于或等于数字的最小整数。它会将数字向上取整，除非该数字已经是整数。例如，`Math.ceil(12.23)`返回 13。以下代码展示了如何使用`ceil()`，从 HTML 代码开始：

```html
<form id="getceiling">
  <label for="num">数字:</label>
  <input type="text" id="num">
  <input type="submit" value="向上取整">
</form>
```

接下来是 JavaScript 代码：

```javascript
let ceil_form = document.getElementById("getceiling");
ceil_form.addEventListener("submit", function(event) {
  let num = document.getElementById("num").value;
  let ceiling = 0;
  num = parseFloat(num);
  event.preventDefault();
  if (!isNaN(num)) {
    ceiling = Math.ceil(num);
    alert(num + " 向上取整是 " + ceiling);
  } else {
    alert("请输入数字。");
  }
}, false);
```

## 328 JavaScript：初学者指南

当观众输入 4.55 时，此脚本显示该数字向上取整的结果。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_346_0.png)

**floor() 方法** `floor()`方法类似于`ceil()`方法，但方向相反。`floor()`方法返回小于或等于参数的最大整数。该方法会将数字向下取整到下一个较低整数，除非参数已经是整数。基本上，此方法会去掉数字的小数部分并留下整数。

例如，`Math.floor(12.23)`返回 12，而`Math.floor(12)`也返回 12。你可以像在前一节中使用`ceil()`方法一样使用`floor()`方法——将结果赋值给变量。

**round() 方法** `round()`方法与之前的方法类似，但它是将输入的数字四舍五入到最近的整数，无论它是大于还是小于该数字。5 的分点是严格的，`Math.round(12.4999999)`会返回 12，尽管你的倾向可能是向上取整。

**random() 方法** `random()`方法对于创建需要随机整数的脚本非常有用。它返回 0 到 1 之间的随机数。这意味着你会得到一个带有很长小数的小数，其本身并没有什么用。例如，它可能会返回类似 0.36511165498095293 的数字。

## 第 12 章：Math、Number 和 Date 对象 329

为了获取一个你可以使用的随机整数，你需要进行一些操作来获得你想要使用的数值类型。

**随机整数** 为了获取一个随机整数，你首先想的一件事是让结果具有更大的数值范围，这样你就不会被困在 0 和 1 之间。为了获得更大的数值范围，你可以将`random()`方法的结果乘以一个整数来创建一个更大的范围。像数组一样，范围将从 0 开始计数；因此，为了获得一个可能的整数范围，你将把结果乘以 5。下面的代码展示了如何这样做：

```javascript
let rand_num = Math.random() * 5;
```

这会得到一个 0 到 4 之间的结果，但还没有给你整数。这个数字可能仍然是一个长小数。

为了获取一个 0 到 4 之间的整数，你需要找到一种方法将这些小数转换为整数。回想一下之前运行过的三种方法：`floor()`、`ceil()`和`round()`。在这里你将选择`floor()`方法；它只是简单地移除整数后的小数部分，并给你数字的整数部分。

使用`floor()`，你可以写下面的代码：

```javascript
let rand_num = Math.random() * 5;
let rand_int = Math.floor(rand_num);
```

`floor()`方法将变量`rand_num`的值作为参数传入，然后从中给你一个整数。

如果你想节省一行代码，可以稍微花点心思。你可以直接将`random()`方法和计算作为`floor()`方法的参数。你可以这样做是因为计算结果`Math.random()*5`是一个数字，而`floor()`方法可以接受数字作为参数。下面的代码展示了你如何在单行中编写此代码：

```javascript
let rand_int = Math.floor(Math.random() * 5);
```

现在，变量`rand_int`将拥有一个 0 到 4 之间的随机整数值。正如你可能注意到的，这种数字对于数组可能非常有用。这就是你如何开始使用随机数编写函数。

注意，如果你想让随机数从 1 开始而不是 0，你可以在语句末尾加上`+ 1`（这在面向用户的代码中很有帮助，因为那可能是用户的预期）。这是一个示例：

```javascript
let rand_int = Math.floor(Math.random() * 5) + 1;
```

**脚本中的随机数** 现在你可以通过使用`random()`方法来玩玩`Math`对象了。通过设置数组，你可以创建一个脚本，在每次页面加载时提供随机引言或显示随机图片。

## JavaScript：初学者指南

用于趣味的随机引言 如果你想过在你的页面上添加一条引言，但不想每次都去修改脚本以显示不同的内容，那么一个随机引言脚本可能正适合你。

要制作一个脚本，你首先需要一些引言来使用。假设你想设置不同的引言，它们将在每次页面加载时以随机顺序显示。由于你有一组相似的值（以便稍后将它们与随机整数配合），你应该使用数组来存储所有这些值并轻松地检索它们。

因此，你需要设置一个包含十个元素的数组，类似于下面的示例，每个元素都是你丢进程序里的（且可能很奇特的）引言：

```javascript
let quotes = ["Look in the mirror. Are you looking at me?", "It is time for rhyme, I guess.", "Where is my JavaScript book?", "If I had a buck for every day I spent--Oops, never mind.", "I suppose you were expecting a real quote here.", "Quotes are great, but don't quote me on that.", "What should I write here?", "Wut hapn iff miss spel ohn purpas?", "Mark my words, I will mark my words.", "This spot reserved for a better quote."];
```

现在你在数组中有了这个奇怪的引言列表，你可以通过生成随机整数来使用它。

你需要一个 0 到 9 之间的随机整数（十个数字），所以你可以使用以下代码将一个 0 到 9 之间的随机整数赋值给变量：

```javascript
let rand_int = Math.floor(Math.random() * 10);
```

现在，变量`rand_int`的值将是 0 到 9 之间的随机整数。你可以用它来访问索引与`rand_int`中的随机整数匹配的数组元素。你只需要使用变量作为索引号来访问数组元素，例如所示：

```javascript
quotes[rand_int]
```

你可以在下面的示例代码中，使用`div`元素的`innerHTML`属性在页面主体中写入这个值。HTML 文档保存为`random_quotes.html`，JavaScript 文件保存为`random_quotes.js`。HTML 代码如下：

```html
<h1>My Random Quote for You:</h1>
<div id="my_quote">
  Look in the mirror. Are you looking at me?
</div>
<script type="text/javascript" src="random_quotes.js"></script>
```

# 第 12 章：Math、Number 和 Date 对象 331

JavaScript 代码如下：

```javascript
let quotes = ["Look in the mirror. Are you looking at me?",
"It is time for a rhyme, I guess.",
"Where is my JavaScript book?",
"If I had a buck for every day I spent-\u2014 never mind.",
"I suppose you were expecting a real quote here.",
"Quotes are great, but don't quote me on that.",
"What should I write here?",
"What haps if eyes miss oh purpas?",
"Mark my words, I will mark my words.",
"This spot reserved for a better quote."];
let q_div = document.getElementById("my_quote");
let rand_int = Math.floor(Math.random() * 10);
q_div.innerHTML = quotes[rand_int];
```

如你所见，这与随机引言脚本非常相似。由于你正在更改图像，可以将结果赋值给图像元素上的`src`属性，以动态更改图像。如果你还需要更改文本，可以像你处理随机引言时那样，将其更改为使用`innerHTML`。

### 注意

在本例中，图像被保存为`image0.gif`、`image1.gif`等；不过，你可以按照喜欢的任何名称保存你的图像文件。

关于`random()`方法的讨论可以持续很久，因为有很多可以进行随机化的内容。然而，你现在已经了解了该功能工作原理的基本知识，是时候继续学习了。

### 专家问答

- **问：我机会用到`Math`对象的任何属性吗？它们都是我甚至没用过的数字！**

- **答：** 这取决于你执行不同类型计算的频率。作为一个初学者，你不太可能使用其中任何一个，但有一些脚本将它们用于高级用途，例如 JavaScript 计算器、图形化对象（如`canvas`元素）等。

- **问：我对写计算器没有兴趣。我真的需要记住`Math`对象的所有属性吗？**

- **答：** 可能不需要，你需要使用它们的情况可能出现得并不频繁。不过，手头有一份参考以备不时之需，并且大致了解它们是什么是好的，因为它们经常出现在 Web 脚本中。

- **问：如果我身边没有计算器，这些属性和方法中的一些很有用。我可以写一小段脚本为自己计算一些东西，对吧？**

- **答：** 当然！只需确保用你已知的数字进行双重检查，以确保你的代码中没有错误。

- **问：`random()`方法很有趣，但太遥远了，我想不出有什么可以用它的地方。你能给我一些用它来做其他事情的建议吗？**

- **答：** 还有很多其他事情你可以用它。你可以对几乎任何可以用 HTML 标签或纯文本显示的内容进行随机化，尝试一些想法并看看它们对你是否有效。不过，这里是我脑子里冒出的想法：随机链接、随机链接图像、某种 JavaScript 游戏的随机任务（掷骰子或纸牌）、随机页面问候语、随机警报……我确定还有很多。

## 334 JavaScript：初学者指南

## 尝试这个 12-1 在页面上显示随机链接

```
prjs12_1.html
prjs12_1.js
```

此脚本允许你更深入地使用`random()`方法，让你能够创建一个在页面上显示随机链接的脚本。

### 逐步步骤

- 1. 创建一个 HTML 页面，其中包含`script`标签，指向一个名为`prjs12_1.js`的外部 JavaScript 文件。添加一个显示“Random Link”的标题，并添加一个 id 为`random_link`的`div`元素。在`div`元素内部，为没有 JavaScript 的用户插入默认链接。将 HTML 文件保存为`prjs12_1.html`。

- 2. 完成后，HTML 文件的`body`部分应该像这样：

```html
<body>
<h1>Random Link</h1>
<div id="random_link">
<a href="http://www.scripttheweb.com">Random Site!</a>
</div>
<script type="text/javascript" src="prjs12_1.js"></script>
</body>
```

- 3. 创建一个外部 JavaScript 文件并将其保存为`prjs12_1.js`。将其用于第 4-7 步。

- 4. 在数组中创建一组五个地址。使用以下地址或你选择的地址：

```
http://www.scripttheweb.com
http://www.webpert.net
http://www.duckgo.com
http://www.google.com
```

- 5. 使用`random()`方法创建一个随机整数，你可以用它作为索引访问数组。

- 6. 通过更改 id 为`random_link`的`div`元素的 HTML 属性，以所示格式在页面上显示随机链接：

```
<a href="random address here">Random Site!</a>
```

- 7. 完成后，JavaScript 文件应该像这样：

```javascript
let urls = [
"http://developer.mozilla.org",
"http://github.com",
"http://www.duckgo.com",
"http://www.yahoo.com",
"http://www.google.com"
];
let rdiv = document.getElementById("random_link");
let rand = Math.floor(Math.random() * 5);
rdiv.innerHTML = '<a href="' + urls[rand] + '">Random Site!</a>';
```

- 8. 在浏览器中保存 JavaScript 文件和 HTML 文件。尝试重新加载几次，看看随机地址如何出现在链接中。

## 总结

在这个项目中，你能够使用对`Math`对象的知识。通过使用`random()`方法，你创建了一个显示指向随机地址链接的页面。

## 理解 Number 对象

`Number`对象是另一个预定义的 JavaScript 对象，它为数字操作提供了几个属性和方法。它最常见的用途是访问某些代表特定值的属性，这些值可以在创建脚本时提供帮助。`Number`与`Math`稍微不同之处在于，你可以创建一个数字作为该对象的数据类型。

### 属性

表 12-3 列出了`Number`对象的常用属性。

| 属性 | 描述 |
| :--- | :--- |
| EPSILON | 1 之间的最小浮点数差。 |
| MAX_VALUE | 约 1.79E+308。 |
| MIN_VALUE | 约 5e–324。 |
| MAX_SAFE_INTEGER | JavaScript 中可以表示的最大整数 (2^53-1)。 |
| MIN_SAFE_INTEGER | JavaScript 中可以表示的最小整数 (-(2^53-1)) |
| NaN | “不是数字”。 |
| NEGATIVE_INFINITY | 负无穷。 |
| POSITIVE_INFINITY | 正无穷。 |

# 第 12 章：数学、数字和日期对象 337

| 方法 | 目的 |
| --- | --- |
| toExponential() | 返回一个用科学计数法表示数字的字符串值 |
| toFixed() | 返回一个保留小数点后指定位数四舍五入的字符串值 |
| toPrecision() | 返回一个保留指定有效位数四舍五入的字符串值 |
| toSource() | 返回一个表示对象源代码的字符串值 |
| toLocaleString() | 返回一个与语言相关的数字表示形式 |
| toString() | 返回一个 Number 对象的字符串值 |
| valueOf() | 经常被 JavaScript 内部使用 |

表 12-4 Number 对象的方法

> 注意
> 无穷（Infinity）在数学方程中的行为与其他数字不同。有关此的更多信息，请参阅 tutorial.math.lamar.edu/Classes/Calc/TypesOfInfinity.aspx。

### 方法

表 12-4 列出了 Number 对象的一些方法，并简要描述了每个方法的目的。接下来的章节将详细讨论其中一些方法。

### `toExponential()`、`toFixed()`、`toPrecision()` 和 `toString()` 方法

这些方法返回一个字符串值，表示 Number 对象以特定格式化后的样子。注意，这些方法不能直接与数字（数值）一起使用，如下代码所示：

```javascript
alert(10.toExponential());
```

这会导致 JavaScript 错误，因为它期望的是一个 Number 对象。为了避免这种情况，请通过将数值赋值给变量（这将使它们变成 Number 对象）来使用这些方法，如下代码所示：

```javascript
let the_num = 10;
alert(the_num.toExponential());
```

> 注意
> 你也可以使用构造函数语法 `let the_num = new Number(10);`
> 或者如果你只需要值，可以直接使用 `new Number(10).toExponential()`。

### JavaScript：入门指南

### `toExponential()` 方法

`toExponential()`返回一个以科学计数法形式表示 Number 对象的字符串。因此，下面的代码将在屏幕上显示 1.0e+1（或类似的表示，取决于你的浏览器）的结果：

```javascript
let the_num = 10;
alert(the_num.toExponential());
```

### `toFixed()` 方法

`toFixed()`返回一个表示 Number 对象在小数点后保留指定位数四舍五入的字符串。例如，如果你想将计算结果格式化为货币值，可以使用此方法将计算结果的小数点后第二位四舍五入，并以你的货币格式显示。例如，这段代码使用了美元和分：

```javascript
let kidsmoney = 2000;
let kids = 7;
let one_share = kidsmoney/kids;
alert("One share of the money is $" + one_share.toFixed(2));
```

每份钱的计算结果为 285.7142857142857，但由于对它使用了参数为 2 的`toFixed()`方法，句子显示如下：

One share of the money is $285.71

### `toPrecision()` 方法

`toPrecision()`返回一个表示 Number 对象保留指定有效位数四舍五入的字符串。这包括小数点前和后的所有数字。因此，如果你想将像 45.57689349 的数字保留五位有效数字，可以使用下面的代码：

```javascript
let the_num = 45.57689349;
alert(the_num.toPrecision(5));
```

浏览器将弹出字符串 45.577，这是保留五位有效数字后的数字（在这种情况下，小数点前后的各占两位）。

### `toString()` 方法

`toString()`返回 Number 对象的字符串值（或数值变量的值）。如果你想将一个数值转换为其对应的字符串值（例如，将 10 更改为 "10"），这可能是很有用的。

### `toSource()` 方法

`toSource()`返回一个表示对象源代码的字符串值。对于定义的 Number 对象，此方法返回`constructor`属性的值。此方法通常由 JavaScript 内部调用，在代码中使用的概率较小。

# 第 12 章：数学、数字和日期对象 339

### `valueOf()` 方法

这是另一个主要由 JavaScript 内部使用的方法。目前，你只需要知道它是 Number 对象的一个有效方法即可。

### `parseInt()` 和 `parseFloat()` 方法

当你需要从混合字符串中获取数值时，这两个方法非常有用。它们的工作方式相似，`parseInt()`只获取数字的整数部分，`parseFloat()`获取小数点后的数字。以下是它们的工作原理：

- 如果第一个字符不是数字或加号 (+)，则两个方法都返回 NaN。
- 对于`parseInt()`，如果第一个字符是数字（零除外）、加号 (+)或减号 (-)，则会评估每个字符直到遇到非数字字符（十六进制值除外，允许如 x 和 A 等其他字符）。将返回从该过程中获得的数字。如果第一个字符是零且该数字不是十六进制，则返回零。
- 对于`parseFloat()`，如果第一个字符是数字、加号 (+)或减号 (-)，它将评估每个字符，如果发现点 (.) 后面还有数字，则继续评估，直到遇到第二个非数字字符。如果数字以零开头且该数字不是十六进制，则返回零。

以下是这些方法如何工作的示例：

```javascript
parseInt("14"); // 返回 14
parseInt("14abc"); // 返回 14
parseInt("+14"); // 返回 14
parseInt("-14"); // 返回 -14
parseInt("14.5"); // 返回 14
parseInt("04"); // 返回 4
parseInt("0x14"); // 返回 20
```

> 提示
> 当省略 radix（进制）参数时，JavaScript 会决定返回值的类型。在某些情况下，这可能会导致意外的结果。`parseFloat()`方法没有这个选项，因为它设计上只解析数值。

以下是这些方法的返回值示例：

```javascript
parseFloat("14"); // 返回 14
parseFloat("14abc"); // 返回 14
parseFloat("+14"); // 返回 14
parseFloat("-14"); // 返回 -14
parseFloat("14.5"); // 返回 14.5
parseFloat("04"); // 返回 4
parseFloat("0x14"); // 返回 0
```

```javascript
parseInt("11", 10); // 返回 11
parseInt("11", 2); // 返回 3
parseInt("11", 16); // 返回 17
parseInt("11", 8); // 返回 9
```

# 使用 Date 对象

Date 对象是预定义的对象。它允许你设置某些时间值并获取某些时间值。要使用此对象，你需要创建一个该对象的实例以便引用。

要创建 Date 对象的实例，使用`new`关键字（正如你创建许多其他对象那样），如下例所示：

```javascript
let instance_name = new Date();
```

你把`instance_name`替换为你为 Date 实例使用的名称。因此，如果你想要一个现在的实例，可以使用下面的代码：

```javascript
let rightnow = new Date();
```

现在你有了一个现在的实例。

使用构造函数时，默认日期是当前日期；但如果需要，你可以指定不同的日期，如下代码所示：

```javascript
let go_back = new Date("November 5, 1955");
```

# 属性和方法

Date 对象没有提供属性（构造函数和原型之外），但它有许多可以使用的方法。表 12-5 列出了 Date 对象的各种方法以及每个方法的目的。这些属性和方法将在后面的章节中描述。

现在你已经有了长长的方法列表，让我们详细查看它们，从获取 Date 实例中日期值的方法开始。

## 第 12 章：数学、数字和日期对象 341

| 方法 | 目的 |
| --- | --- |
| getDate() | 根据用户的本地时间返回月份中的第几天 |
| getDay() | 根据用户的本地时间返回一周中的第几天（0–6） |
| getHours() | 根据用户的本地时间返回一天中的第几小时（0–23） |
| getMilliseconds() | 根据用户的本地时间返回秒内的毫秒数（0–999） |
| getMinutes() | 根据用户的本地时间返回每小时内的分钟数（0–59） |
| getMonth() | 根据用户的本地时间返回一年中的月份（0–11） |
| getSeconds() | 根据用户的本地时间返回分钟内的秒数（0–59） |
| getTime() | 返回 Date 对象自 1970 年 1 月 1 日以来的毫秒数 |
| getTimezoneOffset() | 根据用户的本地时区返回时区偏移（格林威治标准时间的分钟数） |
| getFullYear() | 根据用户的本地时间返回完整的年份（四位数） |
| getUTCDate() | 返回协调世界时间（UTC）的月份中的第几天 |
| getUTCDay() | 返回协调世界时间一周中的第几天（0–6） |
| getUTCFullYear() | 返回协调世界时间的完整年份（四位数） |
| getUTCHours() | 返回协调世界时间一天中的第几小时（0–23） |
| getUTCMilliseconds() | 返回协调世界时间当前秒内的毫秒数（0–999） |
| getUTCMinutes() | 返回协调世界时间每小时内的分钟数（0–59） |
| getUTCMonth() | 返回协调世界时间当前年份中的月份（0–11） |
| getUTCSeconds() | 返回协调世界时间当前分钟内的秒数（0–59） |

**表 12-5** Date 对象的方法（续）

## JavaScript 入门指南

| 方法 | 目的 |
| --- | --- |
| setTime() | 为 Date 对象实例设置时间（自 1970 年 1 月 1 日午夜以来的毫秒数） |
| setFullYear() | 为 Date 对象实例设置完整年份（四位数） |
| setUTCDate() | 设置协调世界时间的月份中的第几天 |
| setUTCFullYear() | 设置协调世界时间的完整年份（四位数） |
| setUTCHours() | 设置协调世界时间一天中的第几小时（0–23） |
| setUTCMilliseconds() | 设置协调世界时间当前秒内的毫秒数（0–999） |
| setUTCMinutes() | 设置协调世界时间每小时内的分钟数（0–59） |
| setUTCMonth() | 设置协调世界时间当前年份中的月份（0–11） |
| setUTCSeconds() | 设置协调世界时间当前分钟内的秒数（0–59） |
| toDateString() | 以美式英语字符串的形式返回 Date 对象的日期部分 |
| toLocaleString() | 返回一个基于本地格式的日期字符串 |
| toLocaleDateString() | 根据本地格式返回 Date 对象的日期部分字符串 |
| toLocaleTimeString() | 根据本地格式返回 Date 对象的时间部分字符串 |
| toString() | 返回一个美式英语格式的日期字符串 |
| toTimeString() | 以美式英语字符串的形式返回 Date 对象的时间部分 |

表 12-5 Date 对象的方法

## 获取值的方法

获取值的方法允许你获取各种时间及日期值，并可以将它们用于你的脚本中。允许你获取 Date 对象实例之值的方法包括：

- `getDate()`
- `getDay()`
- `getHours()`
- `getMilliseconds()`
- `getMinutes()`
- `getMonth()`
- `getSeconds()`
- `getTime()`
- `getTimezoneOffset()`
- `getFullYear()`
- `getUTCDate()`
- `getUTCDay()`
- `getUTCFullYear()`
- `getUTCHours()`
- `getUTCMilliseconds()`
- `getUTCMinutes()`
- `getUTCMonth()`
- `getUTCSeconds()`

## 第 12 章：数学、数字和日期对象 343

要使用这些方法，你需要一个 Date 对象的实例。一旦拥有了实例，就可以通过实例名调用任何一个方法。以下是执行此操作的语法：

```javascript
instance_name.method();
```

你需要将`instance_name`替换为你的 Date 对象实例名称，并将`method`替换为你想要使用的方法函数。

因此，如果你现在想对一个 Date 对象实例使用`getDate()`方法，你会使用以下代码：

```javascript
let rightnow = new Date();
let theday = rightnow.getDate();
```

这会将`getDate()`方法返回的值赋值给名为`theday`的变量。

由于 Date 方法返回的值通常是数值，因此需要对这些方法进行进一步说明；后续如下：

## `getDate()` 方法

`getDate()`方法允许你获取月份中的第几天。这种计数从 1 开始。因此，如果是 22 号，方法将返回 22。

## `getDay()` 方法

`getDay()`方法允许你获取一周中的第几天（0–6）。这种计数从 0 开始。因此，如果是周三，方法将返回 3。

## `getHours()` 方法

`getHours()`方法允许你获取一天中的第几小时（0–23）。计数从 0 开始。因此，如果时间是 22 点，方法将返回 22。

## `getMilliseconds()` 方法

`getMilliseconds()`方法允许你获取当前秒内的毫秒数（0–999）。

## `getMinutes()` 方法

`getMinutes()`方法允许你获取每小时内的分钟数（0–59）。计数从 0 开始。因此，如果时间是 22:30，方法将返回 30。

## `getMonth()` 方法

`getMonth()`方法允许你获取一年中的月份（0–11）。这种计数从 0 开始。因此，如果是 10 月，方法将返回 9。

## `getSeconds()` 方法

`getSeconds()`方法允许你获取当前分钟内的秒数（0–59）。正如前面提到的，计数从 0 开始。因此，如果时间是 22:42:23，方法将返回 23。

## `getTime()` 方法

`getTime()`方法获取自 1970 年 1 月 1 日午夜以来的毫秒数。因此如果你想知道当前时间的毫秒数，可以使用以下代码：

```javascript
let rightnow = new Date();
let thetime = rightnow.getTime();
```

这会将方法的结果赋值给变量，以便你以后在脚本中使用它。

## `getTimezoneOffset()` 方法

`getTimezoneOffset()`方法返回本地时间与格林威治标准时间（GMT）之间的分钟数。因此，如果你与 GMT 相差六小时，方法将返回 360 (6 × 60)；如果只差一小时，方法将返回 60。

## `getFullYear()` 方法

`getFullYear()`方法返回四位数年份。

```javascript
let rightnow = new Date();
let theyear = rightnow.getFullYear();
```

这会将方法的返回值赋值给变量`theyear`。

## UTC 方法

这些方法与其对应的方法原理相同（例如`getDate()`和`getUTCDate()`相同），但它们返回的是协调世界时间而非用户的本地时间。

现在你已经了解了获取值的方法，让我们来看看允许你为 Date 对象实例设置值的方法。

# 第 12 章：数学、数字和日期对象 345

## 设置值的方法

设置值的方法与获取值的方法使用相同类型的值。

允许你为 Date 对象实例设置值的方法包括：

- `setDate()`
- `setHours()`
- `setMilliseconds()`
- `setMinutes()`
- `setMonth()`
- `setSeconds()`
- `setTime()`
- `setFullYear()`
- `setUTCDate()`
- `setUTCFullYear()`
- `setUTCHours()`
- `setUTCMilliseconds()`
- `setUTCMinutes()`
- `setUTCMonth()`
- `setUTCSeconds()`

要设置这些值，你根据你想要使用的时间或日期发送一个数值参数。例如，如果你想为 Date 对象实例设置月份的某几号，可以使用以下代码：

```javascript
let rightnow = new Date();
rightnow.setDate(22);
```

这将将`rightnow` Date 实例的每月几号设置为 22 号。

其他方法的工作原理相同。为了知道需要发送给其中一个方法的值，请查看其在获取值方法中对应方法返回了什么类型的值。该方法预期的参数将是与该方法返回的值相似。

## 其他方法

其余的方法在某些方面执行了其他方法未涵盖的各种任务。

## `parse()` 方法

`parse()`方法用于根据日期字符串（如 Dec 12, 1999）作为参数，找出自 1970 年 1 月 1 日午夜以来的毫秒数。这通常与`setTime()`方法配合使用，该方法需要一个毫秒参数来设置时间。你可以使用`parse()`方法找到自 1970 年 1 月 1 日午夜到 1999 年 12 月 12 日午夜的毫秒数（`rightnow` Date 实例将使用此作为所有方法返回值的日期），如下代码所示：

```javascript
let rightnow = new Date();
let thenum = Date.parse("Dec 12, 1999");
rightnow.setTime(thenum);
```

此方法可以直接从 Date 对象调用。这段代码将日期解析为毫秒数，然后将其发送到与 Date 实例一起使用的`setTime`方法。

## `toString()`、`toLocaleString()` 和 `toTimeString()` 方法

这些方法返回代表日期和时间的字符串或其部分。例如，`toString()`方法返回字符串格式的日期。你可以使用它来获取 Date 实例的格式化日期，如下代码所示：

```javascript
let rightnow = new Date();
let thedate = rightnow.toString();
```

这会将一个日期值赋值给变量`thedate`。字符串的值取决于你的浏览器查看页面的方式。它可以被写入页面，或与 Date 对象的其他方法配合。

## `toLocaleString()` 方法

`toLocaleString()`方法返回查看者本地化格式的日期。你可以使用它来获取 Date 实例的本地化格式，如下代码所示：

```javascript
let rightnow = new Date();
let thedate = rightnow.toLocaleString();
```

这会将一个日期值赋值给变量`thedate`。字符串的值取决于你的浏览器查看页面的方式。它可以被写入页面，或与 Date 对象的其他方法配合。

## 有些日期脚本怎么样？

在对页面进行技术概述之后，你已经准备好创建一些使用 Date 对象方法的脚本。首先，你将编写一个在页面上显示日期的脚本，然后你将编写一个简单时钟的脚本。

## 在页面上写入日期

要在页面上写入日期，你需要使用 Date 方法来获取值。假设你想写入一个 M/D/Y 格式（月/日/年）的日期。为了实现这一点，你需要找到月份、日期和年份。你可以使用`getMonth()`、`getDate()`和`getFullYear()`方法来实现。

以下脚本将把日期写入页面。首先，是 HTML 代码（保存为 write_date.html）：

```html
<h1>Today's Date</h1>
<div id="write_date">
  <!-- 此处可以调用服务器端脚本 -->
</div>
<script type="text/javascript" src="write_date.js"></script>
```

注意`div`元素中的注释。如果你想让不支持 JavaScript 的浏览器也能访问它，可以在此地放置一个对 PHP（或其他服务器端技术）脚本的调用。例如，如果你的页面设置了 PHP，可以使用以下代码来像 JavaScript 代码一样显示日期：

```html
<h1>Today's Date</h1>
<div id="write_date">
  <?php
  $date = date("n/j/Y");
  echo "$date";
  ?>
</div>
<script type="text/javascript" src="write_date.js"></script>
```

你会发现 PHP 脚本比 JavaScript 脚本短得多，因为它具有内置的日期格式化功能。显示的日期可能与查看者的日期不同，因为它显示的是 Web 服务器上的日期。虽然对服务器端技术的深入讨论超出了本书的范围，但可以作为参考。在没有 JavaScript 的情况下提供这种示例。

接下来，是 JavaScript 代码（保存为 write_date.js）：

```javascript
let right = new Date();
let weekday = right.getDay();
let month = right.getMonth();
let date = right.getDate();
let year = right.getFullYear();
let ds = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
let date_div = document.getElementById("write_date");
month += 1;
date_div.innerHTML = ds[weekday] + ", " + month + "/" + date + "/" + year;
```

创建一个数组来存储星期，使用`getDay()`方法返回的值作为索引。`month`增加 1，以便月份显示为 1 而不是 0。`date_div`的`innerHTML`属性被更改以显示格式化的日期。

## 创建简单时钟

要创建一个简单的时钟，你需要当前时间的小时、分钟和秒。为了获取这些信息，你可以使用`getHours()`、`getMinutes()`和`getSeconds()`方法。

以下代码将创建一个显示在页面上的时钟。首先，是 HTML 代码（保存为 clock.html）：

```html
<h1>Current Time:</h1>
<div id="my_clock">
  <!-- 此处可以调用备份的服务器端脚本 -->
</div>
<script type="text/javascript" src="clock.js"></script>
```

### 注意

如果你使用服务器端脚本作为 JavaScript 时钟的备份，你不希望它每秒更新一次，因为可能会给 Web 服务器带来过大压力。在这种情况下，最好只是显示时间而不更新。

接下来，是 JavaScript 代码（保存为 clock.js）：

```javascript
function startClock() {
  let thetime = new Date();
  let hours = thetime.getHours();
  let mins = thetime.getMinutes();
  let secs = thetime.getSeconds();
  let ap = (hours >= 12) ? "p.m." : "a.m.";
  let clock_div = document.getElementById("my_clock");
  hours = (hours > 12) ? hours - 12 : hours;
  hours = (hours < 1) ? 12 : hours;
  mins = (mins < 10) ? "0" + mins : mins;
  secs = (secs < 10) ? "0" + secs : secs;
  clock_div.innerHTML = hours + ":" + mins + ":" + secs + " " + ap;
}
setInterval(function() { startClock(); }, 1000);
startClock();
```

脚本使用`setInterval()`方法每秒调用一次。

脚本创建了一个函数，将方法的结果赋值给变量。它获取`hours`变量，如果`hours`大于等于 12，则将`ap`设置为`p.m.`；如果`hours`小于 12，则设置为`a.m.`（此时`hours`仍然保持下午 1 点的 13、下午 2 点的 14 等）。完成此后，会调整`hours`变量，以便显示 12 小时制预期的值。

脚本随后调整显示分钟和秒的变量值，当数字小于 10 时，在前面添加一个 0。这样，时钟将显示 12:02:34 而不是 12:2:34。

最后，函数在页面上显示输出。该函数在定义后立即被初始调用。该函数每隔 1000 毫秒（即 1 秒）重复一次。这使得时钟能够保持同步。该脚本在浏览器中运行的结果如图 12-6 所示。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_367_0.png)

图 12-6 页面上显示当前时间。

## 尝试 12-2 创建一个 JavaScript 钟

此项目让你能够更多地使用 Date 对象的方法，并学习如何调整返回的值以便以各种方式使用。这是一个比你在上一节中简单时钟多了一些选项的 JavaScript 钟。

### 逐步步骤

- 1. 创建一个 HTML 页面，并包含指向外部 JavaScript 文件`prjs12_2.js`的脚本标签。添加一个显示“Current Time”的标题，并添加一个 id 为`my_clock`的`div`元素。将 HTML 文件保存为`prjs12_2.html`。

- 2. 完成后，HTML 文件的`body`部分应该如下所示：

```html
<body>
<h1>Current Time</h1>
<div id="my_clock"></div>
<script type="text/javascript" src="prjs12_2.js"></script>
</body>
```

- 3. 创建一个外部 JavaScript 文件并将其保存为`prjs12_2.js`。在步骤 4-7 中使用它。

- 4. 编写一些显示时钟的代码。在这个钟中，包含以下信息：
    - 带有时、分、秒的时间
    - 是 A.M. 还是 P.M.
    - mm/dd/yyyy 格式的日期

- 5. 这是一个 12 小时钟，因此请确保调整`hours`的值，使其保持在 1 到 12 之间。此外，注意日期的格式并相应调整月份和日期的值。

- 6. 启动时钟并让它每秒更新一次。

- 7. 完成后，JavaScript 文件应该如下：

```javascript
function startClock() {
  let thetime = new Date();
  let hours = thetime.getHours();
  let mins = thetime.getMinutes();
  let secs = thetime.getSeconds();
  let ap = (hours >= 12) ? "p.m." : "a.m.";
  let themonth = thetime.getMonth();
  let thedate = thetime.getDate();
  let theyear = thetime.getFullYear();
  let clock_div = document.getElementById("my_clock");
  hours = (hours > 12) ? hours - 12 : hours;
  hours = (hours < 1) ? 12 : hours;
  mins = (mins < 10) ? "0" + mins : mins;
  secs = (secs < 10) ? "0" + secs : secs;
  themonth++;
  clock_div.innerHTML = hours + ":" + mins + ":" + secs + " " + ap + " " +
  themonth + "/" + thedate + "/" + theyear;
}
setInterval(function() { startClock(); }, 1000);
startClock();
```

- 8. 保存 JavaScript 文件并在浏览器中打开 HTML 文件。时间和日期应该出现在页面上。

### 尝试总结

在这个项目中，你使用了关于 Date 对象的知识。通过 Date 对象的方法，你创建了一个在 Web 页面上显示日期的时钟。

### 持续项目

在第 11 章中，你使用 Node.js 从 PostgreSQL 数据库（你的`mywebapp`数据库）检索数据。你还使用 Node.js 创建了一个简单的 Web 服务器，并在浏览器中打开了页面。在本章中，你将通过将 Node.js 中创建的 PostgreSQL 查询与 Web 服务器结合来推进你的项目。然后你将添加一些在浏览器中显示信息时很有用的计算。

首先，更新你的`server.js`文件，使其如下所示。这只是添加了`pg`模块并使用了它。这将最终允许你从数据库获取数据。这里是`server.js`的新代码：

```javascript
const express = require('express');
const app = express();
const router = express.Router();
const path = require('path');
const { Pool } = require('pg');
const connectionInfo = `postgresql://username:password@localhost:5432/mywebapp`;
const pool = new Pool({connectionString: connectionInfo});

app.use(express.static(path.join(__dirname, 'public')));

function getData() {
  pool.query(
    'SELECT * FROM bowlers',
    [],
    function (err, result) {
      if (err) {
        console.error(err);
      }
      // 这里你将添加新代码
      // 这是查询成功完成时执行的代码
      // 你可以使用数据进行记录、显示、进行计算等。
    }
  );
}

router.get('/', function (req, res) {
  getData();
  res.sendFile(path.join(__dirname, 'index.html'));
});

app.use('/', router);

let server = app.listen(3000, function() {
  console.log('App is running on port 3000');
  console.log('To end, press Ctrl+C');
});
```

## 获取所需数据

在第 11 章检索数据时，你只是将结果记录到控制台。这一次，你将遍历数组中的每个对象并进行计算。要获取数据，你需要遍历数组。可以通过多种方式实现，最常用的是`for`循环或`forEach()`。例如，以下代码中使用了`forEach()`。当你处理`result.rows`数组中的每一项时，添加以下代码：

```javascript
result.rows.forEach(function (bowler) {
  console.log(`Bowler Name: ${bowler.first_name} ${bowler.last_name}`);
});
```

`bowler`代表数组的当前迭代。因此，函数第一次运行时使用的是数据库检索的第一项`result.rows[0]`。将此对象引用为`bowler`可以让你以易于读取的格式访问属性。与其使用`result.rows[0].last_name`，你可以引用`bowler.last_name`。注意，在某些情况下`for`循环可能更好，但在此项目中`forEach`非常合适。

你可以看到，对象的`first_name`和`last_name`属性被用于记录每个球员的名字到控制台。你可以使用相同的技术访问任何属性，你将在下一节中执行。

## 在结果上运行计算

现在你已经轻松地从查询中访问数据，可以根据每个属性进行一些计算。对于你的应用程序，你想给每个球员一个总分，这将是每个属性的平均值并四舍五入到整数。这些属性基于 0-100 系统，总分为 100 的球员将获得最佳评分。

首先，你需要计算每个球员属性的平均值。要做到这一点，可以将它们相加并除以属性的数量（此处为三个）。因此，将你的代码调整为：

```javascript
result.rows.forEach(function (bowler) {
  let overallAvg = (bowler.accuracy + bowler.power + bowler.consistency) / 3;
  console.log(`Bowler Name: ${bowler.first_name} ${bowler.last_name}`);
  console.log(`Bowler Overall: ${overallAvg}`);
});
```

从控制台窗口（node.js）启动你的 Web 服务并在浏览器中打开`http://localhost:3000`。查看控制台窗口（而不是网页）以查看结果。注意它看起来并不好看：

- Bowler Name: Coach Purswell, Bowler Overall: 76.33333333333333
- Bowler Name: Doctor Gutter, Bowler Overall: 54.66666666666664
- Bowler Name: Cranky Shoes, Bowler Overall: 77.33333333333333
- Bowler Name: Slow Roller, Bowler Overall: 71.33333333333333
- Bowler Name: Prize Winner, Bowler Overall: 96.66666666666667

小数太长了。可以通过限制显示的位数来修复。对于此应用程序，你只需简单地四舍五入到整数来实现，这可以使用在本章早期学到的`Math.round()`方法完成。这一次，将你的代码调整为：

```javascript
result.rows.forEach(function (bowler) {
  let overallAvg = (bowler.accuracy + bowler.power + bowler.consistency) / 3;
  let overallRating = Math.round(overallAvg);
  console.log(`Bowler Name: ${bowler.first_name} ${bowler.last_name}`);
  console.log(`Bowler Overall: ${overallRating}`);
});
```

# 354 JavaScript：初学者指南

关闭 Node 服务器 (CTRL-C)，重启 node.js，并刷新网页。如果你现在查看控制台窗口，你应该能看到一个更整洁的结果：

```
Bowler Name: Coach Purswell
Bowler Overall: 76
Bowler Name: Doctor Gutter
Bowler Overall: 55
Bowler Name: Cranky Shoes
Bowler Overall: 77
Bowler Name: Slow Roller
Bowler Overall: 71
Bowler Name: Prize Winner
Bowler Overall: 97
```

现在你可以轻松地看到哪些球手的总分最高了！如所料，Doctor Gutter 的评分最低，而 Prize Winner 的评分高达 97，非常出色。随着这个应用程序的开发，你将能够将这些信息显示在网页上！

如果你在运行过程中遇到困难，或者想在代码完成后查看`server.js`文件的完整代码，这里这里：

```javascript
const express = require('express');
const app = express();
const router = express.Router();
const path = require('path');
const { Pool } = require('pg');
const connectionInfo = 'postgres://mywebappuser:12345@localhost/mywebapp';
const pool = new Pool({connectionString: connectionInfo});

app.use(express.static(path.join(__dirname, 'public')));

function getBowlerData() {
  pool.query('SELECT * FROM bowlers',
    function (err, result) {
    if (err) {
      console.error(err);
    }
    result.rows.forEach(function (bowler) {
      let overallAvg = (bowler.accuracy + bowler.power +
      bowler.consistency) / 3;
      let overallRating = Math.round(overallAvg);
      console.log(`Bowler Name: ${bowler.first_name} ${bowler.last_name}`);
      console.log(`Bowler Overall: ${overallRating}`);
    });
  });
}

router.get('/', function (req, res) {
  getBowlerData();
  res.sendFile(path.join(__dirname, 'index.html'));
});

app.use('/', router);

let server = app.listen(3000, function() {
  console.log("App Server via Express is running on port 3000");
  console.log("To end, press Ctrl + C");
});
```

请注意，你需要确保 Postgres 连接字符串中的所有用户名和密码是正确的。

# 第 12 章自测

- 1. Math 对象的属性和方法允许你执行什么？

  A. 获取字符串的平方根及此类值并返回一个数字。

  B. 执行数学计算。

  C. 去数学课学习新定理。

  D. 什么都不用，它们是没用的。

- 2. 的 ________ 属性持有欧拉常数的值。

- 3. LN10 属性持有 10 的自然 ________ 值。

- 4. LOG10E 属性持有 10*E 的对数值。

  A. 正确

  B. 错误

- 5. 下列哪项可以正确在网页上写入 pi 的值？

  A. document.write(Math.Pi);

  B. document.write(Math.pi);

  C. document.write(Math.PI);

  D. document.write(Date.PI);

- 6. ________ 属性持有 2 的平方根的值。

# 356 JavaScript：初学者指南

- 7. abs() 方法返回作为参数传递给数字的值。

  A. absent

  B. absurd

  C. absolute

  D. absolute square root

- 8. pow() 方法返回作为参数传递给数字的正弦值。

  A. 正确

  B. 错误

- 9. pow() 方法返回参数的到另一个参数的幂的数值。

  A. 正确

  B. 错误

- 10. 下列哪项可以正确生成一个 0 到 7 之间的随机数？

  A. `let rand_int = Math.floor(Math.random()*8);`

  B. `let rand_int = Math.floor(Math.random()*7);`

  C. `let rand_int = Math.floor(Math.random()*6);`

  D. `let rand_int = Math.sqrt(Math.random());`

- 11. ________ 方法返回作为参数传递给数字的平方根。

- 12. 在使用 Date 对象的属性和方法之前，大多数情况下必须创建什么？

  A. Nights 字符串

  B. 用于引用日期的数字

  C. 用于设置日期的时间

  D. Date 对象的实例

- 13. ________ 方法返回一周中的第几天。

- 14. getMonth() 方法返回与代表当前月份相同的数字（例如，如果当前月份是 1 月，则返回 1）。

  A. 正确

  B. 错误

- 15. 下列哪项可以正确将名为 rightnow 的 Date 对象的星期几赋值给名为 weekday 的变量？

  A. `let weekday = rightnow.getDate();`

  B. `let weekday = rightnow.getDay();`

  C. `let weekday = rightnow.getMonth();`

  D. `let weekday = rightnow.getTime();`

# 第 13 章处理字符串

### 关键技能与概念

- 使用 String 对象的属性

- 使用 String 对象的方法

- 字符串

- 正则表达式

在 JavaScript 中处理字符串，你需要了解字符串以及如何处理它们。本章首先解释了什么是字符串，以及如何创建它们。

# String 对象的介绍

String 对象提供了有关字符串的属性和方法。在 JavaScript 中创建 String 对象有两种方法：使用`new`关键字，或者使用构造函数。如果你想创建一个 String 对象，可以使用以下代码：

```javascript
let instance_name = new String("string value");
```

这就是 String 对象。

# 字符串字面量

你可以通过将字符串赋值给变量来创建一个字符串字面量。这种技术比使用`new`关键字创建 String 对象要短，并且仍然可以使用字符串的方法。字符串字面量的创建如下：

```javascript
let guitar_string = "G";
```

这使得 "G" 成为普通字符串。

# 有什么区别？

String 对象和字符串字面量之间的区别在于，普通字符串具有字符串本身的值，并且可以与其他字符串进行比较，如下所示：

```javascript
let guitar_string1 = "E";
let guitar_string2 = "E";
if (guitar_string1 === guitar_string2) {
  alert("字符串是相同的！");
} else {
  alert("字符串是不相同的！");
}
```

两个变量具有相同的字符串值。

字符串被比较。

如果你使用 String 对象运行上面的代码，你会看到意料之外的结果。下面的代码使用了对象：

```javascript
let guitar_string1 = new String("E");
let guitar_string2 = new String("E");
if (guitar_string1 === guitar_string2) {
  window.alert("字符串是相同的！");
} else {
  window.alert("字符串是不相同的！");
}
```

String 对象被赋予了相同的字符串值。

值被比较。

| 属性 | 用途 |
| --- | --- |
| length | 存储字符串长度的数值值（字符数量） |

**表 13-1** String 对象的属性

普通文本字符串可以使用 String 对象的方法，因为 JavaScript 会获取字符串字面量并将其转换为一个临时的 String 对象。一旦方法的执行完成，它会返回一个字符串字面量。这允许你在无需手动创建 String 对象的情况下使用 String 对象的方法。

## 使用 String 对象的属性和方法

String 对象只有一个属性（构造函数属性和原型属性除外，这些属性只能与通过构造函数创建的 String 对象配合）。表 13-1 显示了该属性。

## length 属性

该属性返回字符串的长度，即字符串包含的字符数。你可以同时对 String 对象和字符串字面量使用它。你已经在其他对象中见过这个属性，例如 Array 对象。（在那种情况下，该值是数组中元素的数量）。

以下代码使用了普通文本字符串。它将字符串变量的长度写入页面中。

```javascript
let myname = "John";
alert("The name has " + myname.length + " characters.");
```

注意变量是如何像对象名一样被使用的，并能够访问 String 的属性和方法的。脚本写入页面。由于该名称有四个字符，这里 length 属性的值为 4。

## String 对象的方法

String 对象的常用方法列于表 13-2（按功能分组）。更多方法可以在 https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#Methods 找到。

## `charAt()` 和 `charCodeAt()` 方法

`charAt()`方法确定字符串中特定位置上的哪个字符。它接受一个数字参数，代表字符在字符串中的位置。

# 第 13 章：处理字符串

| 方法 | 用途 |
| --- | --- |
| charAt() | 查找字符串中指定位置的字符 |
| charCodeAt() | 查找字符串中指定位置字符的字符编码 |
| concat() | 将两个或多个字符串相并返回新的组合字符串值 |
| slice() | 提取字符串的指定部分并返回新字符串 |
| substring() | 允许返回由起始位置和结束位置指定的字符串部分 |
| indexOf() | 在字符串中搜索作为参数的字符：如果找到，返回字符首次出现的位置；否则返回 -1 |
| lastIndexOf() | 在字符串中搜索作为参数的字符：如果找到，返回字符最后一次出现的位置；否则返回 -1 |
| toLowerCase() | 将字符串转换为所有小写字母并返回结果 |
| toUpperCase() | 将字符串转换为所有大写字母并返回结果 |
| toString() | 返回字符串的字面量值 |
| fromCharCode() | 使用字符编码作为参数创建新字符串 |
| localeCompare() | 根据字母顺序比较字符串并返回结果 |
| match() | 比较正则表达式和字符串以查看它们是否匹配 |
| replace() | 查找正则表达式是否匹配字符串，然后将匹配的字符串替换为新字符串 |
| search() | 使用正则表达式和指定字符串执行匹配搜索 |
| split() | 根据作为方法的参数字符集将字符串拆分为字符串数组 |
| trim() | 移除字符串开头结尾的空白字符 |

**表 13-2** String 对象的方法

当你想要查找一个字符时，记住位置计数是从 0 开始（类似于数组），而不是从 1 开始，第一个字符位于位置 0。以下代码显示了如何使用`charAt()`方法获取字符串中的第一个字符：

```javascript
let the_text = "Character";
let first_char = the_text.charAt(0);
alert("The first character is " + first_char);
```

这段代码将`charAt()`方法调用的结果赋值给名为`first_char`的变量，并将其用于 alert。alert 将告诉用户调用该方法的文本字符串中的第一个字符。在这种情况下，alert 将显示“The first character is C.”

### JavaScript: 入学者指南

如果你想找到最后一个字符，你需要在使用该方法之前知道字符串中有多少个字符，或者可以使用`length`属性来确定字符串中字符的数量。在使用`length`属性时，记住它返回的是字符的数量，而不是最后一个字符的位置。

length 属性从 1 开始计数，而当你使用`charAt()`方法时，必须从 0 开始计数。字符串中的最后一个字符的位置将小于其包含的字符数。换句话说，如果字符串有 10 个字符（1–10），那么最后一个位置（0–9）就是 9。例如，这段代码找到了字符串中的最后一个字符：

```javascript
let text = "character",
position = text.length - 1,
last_char = text.charAt(position);
alert("The last character is " + last_char);
```

这段代码将`charAt()`方法调用的结果赋值给名为`last_char`的变量，并将其用于 alert。alert 将告诉用户调用该方法的文本字符串中的最后一个字符。在这种情况下，alert 将显示“The last character is r”。

# 364 JavaScript: 初学者指南

因为它是即时拼接字符串，不需要用户运行。相反，它使用参数将其返回为字符串。

所以，如果你想向查看者显示字符串 "HI"，你可以使用此处所示的示例代码：

```javascript
window.alert(String.fromCharCode(72,73));
```

这段代码获取第一个参数（字符代码 72）并将其转换为 H。然后获取第二个参数（字符代码 73）并将其转换为 I。两者按照它们出现的顺序组合成字符串 "HI"，并作为警报框发送给查看者。

# `localeCompare()` 方法

`localeCompare()`方法比较两个字符串并返回一个数字，表示字符串在字母顺序上是在参数之前还是之后。该方法将根据浏览器的区域（国家和语言）使用不同的计算方法。它返回以下值之一：

- 如果字符串在字母顺序上于参数之前，它返回一个负数。
- 如果字符串相等，它返回 0。
- 如果字符串在字母顺序上于参数之后，它返回一个正数。

例如，你可以使用以下代码来确定字符串 "orange" 在字母顺序上是在另一个字符串之前还是之后：

```javascript
let comp_string = "orange";
let new_string = "apple";
let pos = comp_string.localeCompare(new_string);
if (pos < 0) {
  alert(comp_string + " comes before " + new_string);
}
else if (pos > 0) {
  alert(comp_string + " comes after " + new_string);
}
else {
  alert("The strings are equal");
}
```

在这种情况下，查看者将收到一个警报框："orange comes after apple."。

# `indexOf()` 和 `lastIndexOf()` 方法

`indexOf()`方法查找某个字符或字符串在字符串中的起始位置。它只返回作为参数发送的字符或字符串第一次出现的位置。如果在字符串值中未找到该字符或字符串，则返回值 -1。

# 第 13 章：处理字符串 365

以下代码在字符串 "Cool" 中查找字母 C：

```javascript
let the_text = "Cool";
let position = the_text.indexOf("C");
alert("Your character is at position " + position);
```

记住位置计数从 0 开始，所以当它发现 C 是字符串中的第一个字符时，它返回 0。警报框会显示 "Your character is at position 0"。

注意该方法是区分大小写的，因此在 JavaScript 中，C 和 c 是不同的字符。因此，代码返回 -1（告诉你该字符不在字符串中），尽管字符串中确实有大写 C。

```javascript
let the_text = "Cool";
let position = the_text.indexOf("c");
alert("Your character is at position " + position);
```

现在警报框会显示 "Your character is at position -1"。

如果你想通过检查是否为 -1 来将其视为位置，你可以使用此代码在要查找的字符不在字符串中时发送不同的警报框：

```javascript
let the_text = "Cool";
let position = the_text.indexOf("c");
if (position === -1) {
  alert("Your character is not in the string!");
} else {
  alert("Your character is at position " + position);
}
```

这一次，if 语句检查方法是否向`position`变量返回了 -1。如果是，警报框显示 "Your character is not in the string!"。否则，常规警报框会告诉你位置。在之前的代码中，小写 c 不在字符串中，所以出现了 "Your character is not in the string!"。

`indexOf()`只返回你用作参数的字符第一次出现的位置数字。所以，如果你使用以下代码，你会收到警报框说字符在位置 1，尽管它实际上在位置 2：

```javascript
let the_text = "Cool";
let position = the_text.indexOf("o");
if (position === -1) {
  alert("Your character is not in the string!");
} else {
  alert("Your character is at position " + position);
}
```

### JavaScript: 初学者指南

如果你使用`indexOf()`方法的第二个参数，对字符或字符串的搜索将从指定位置开始，而不是从 0 开始。找到第二个 "o" 的方法是跳过位置 1 的第一个，从位置 2 开始查找。

```javascript
let the_text = "Cool";
let position = the_text.indexOf("o",2);
if (position == -1) {
  alert("Your character is not in the string!");
}
else {
  alert("Your character is at position " + position);
}
```

这一次，方法返回的结果为 2，因为它在指定的起始位置就找到了它。

### 注意

如果你想找到字符串的所有出现次数，你可能希望使用正则表达式，本章稍后会讨论。

`lastIndexOf()`方法查找字符或字符串最后一次实例在字符串中的位置。如果在字符串值中未找到该字符，则返回值 -1。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_387_0.png)

**图 13-2** 没有多余空格的文本会提示查看者。

### 专家问答

- **问：** 所以`length`属性返回字符串中字符的数量，但字符串方法是从 0 开始计数的。这有点让人困惑，数组也是如此。有什么简单的方法记住这一点吗？

- **答：** 最简单的方法是记住`length`属性从 1 开始，而方法从 0 开始计数。因此，`length`的值比字符串中的最后一个位置大一。所以，如果字符串的长度为 5，对于方法来说，这意味着字符串中的最后一个位置是 4。

- **问：** 是的，但也很让人困惑，因为`slice()`和`substring()`方法的第二个参数比方法停止删除字符的位置要高。为什么这样？

- **答：** 起初确实很困惑。你只需要习惯每个方法的工作方式。如果你使用得足够频繁，就会记住在什么情况下使用哪些数字。

- **问：** 我为什么需要`split()`方法？我不能自己建一个数组就完事了吗？

- **答：** 可以。但是，一旦你学习了 JavaScript Cookie，`split()`方法就会非常有用，因为你可以分割存储在 Cookie 中的信息以使用它。Cookie 将额外信息存储在长字符串中，通常使用某些字符作为分隔符。这只是`split()`方法对你有用的例子之一。

- **问：** 许多方法会在文本字符串周围添加标签。我不能直接写出这些 HTML 吗？这看起来很简单。

- **答：** 这些方法不再被频繁使用，因为可以使用`innerHTML`或向文档中添加 DOM 节点。此外，它们可能会导致 HTML 代码无效，因为其中一些创建的标签在 HTML5 中已被废弃。

## 尝试一试 13-1 使用 indexOf() 测试地址

在这个项目中，你将通过创建一个脚本，对查看者输入的电子邮件地址进行非常基础的测试，来练习`indexOf()`方法。

![](img/a869e86c7d7b9652ddb16b3ee269a2b8_388_0.png)

### 步骤详解

- 1. 创建一个 HTML 页面指向名为`prjs13_1.js`的 JavaScript 文件。添加一个 id 为 "email" 的文本框和一个标记为 "Submit E-mail" 的提交按钮。将文件保存为`prjs13_1.html`。

- 2. 完成后，HTML 文件的主体应该如下：

```html
<body>
  <form id="getmail">
    <label for="email">Enter E-mail</label>
    <input type="text" id="email"><br>
    <input type="submit" value="Submit E-mail">
  </form>
</body>
```

- 3. 创建一个外部 JavaScript 文件并保存为`prjs13_1.js`。在步骤 4-7 中使用它。

- 4. 将 "email" 文本的值赋值给名为`email_add`的变量。

- 5. 使用`indexOf()`查看地址中是否包含`@`字符，以及地址中是否包含`.`字符。

- 6. 如果地址同时包含`@`字符和`.`字符，则发送一个提示感谢查看者。否则，向查看者发送提示，告诉他或她需要这些字符重试。

- 7. 完成后，JavaScript 文件应该如下：

```javascript
let getemail = document.getElementById("getmail");
getemail.addEventListener("submit", function(event) {
  let email_add = document.getElementById("email").value;
  event.preventDefault();
  if ( (email_add.indexOf("@") >= 0) && (email_add.indexOf(".") >= 0) ) {
    alert("Thank you!");
  } else {
    alert("The @ and . characters are required in the e-mail address.");
  }
}, false);
```



# 第 13 章：处理字符串

## 尝试一试总结

在这个项目中，你使用了 `indexOf()` 方法的知识来测试查看者输入的电子邮件地址。如果缺少其中一个字符，就会向查看者发送一个错误提示。否则，会发送一个感谢查看者的提示。

## 使用 Cookie

Cookie 是存储在用户计算机上的小型文本文件。每当查看者返回你的网站时，只要 Cookie 没有被删除或过期即可。当然，如果查看者不接受 Cookie，那么以后将无法设置或引用 Cookie。在使用 Cookie 时记住以下几点：

- Cookie 为 4KB (4000 个字符) 或更少。
- 浏览器可以接受来自单个域的 20 个 Cookie。
- 如果许多查看者不接受 Cookie，这消除了 Cookie 对这些查看者的任何优势。

## JavaScript：初学者指南

在代码中，通过添加 UTC 格式的日期为 cookie 添加了过期时间。然后将该结果加到用于设置 cookie 字符串的变量中。如果你想让 cookie 持久保存，可以将日期设置为非常遥远的未来。如果你想让一个决定不再使用的 cookie 过期，可以设置一个过去的日期，cookie 就会过期。

## 读取 Cookie

如果你只设置了一个 cookie 并想要读取它，那么读取 cookie 非常简单。要读取 cookie，你只需要从浏览器获取 `document.cookie` 属性的值即可。

```javascript
function read_it() {
  let mycookie = document.cookie;
}
```

然而，前面的代码会为 `mycookie` 变量返回一个很长且可能混乱的字符串。它看起来可能像：

```
name=tasty1&fav=Chocolate%20Chip
```

`%20` 是 cookie 使用 `encodeURIComponent()` 方法进行转义时进入代码的。要修复这个问题，请使用 `decodeURIComponent()` 获取更具可读格式的数据（当你从用户处获取值时会用到它）。

接下来，你必须找到一种从 cookie 中提取信息的方法。假设 cookie 包含了刚刚作为示例的字符串（`name=tasty1&fav=Chocolate%20Chip`），那么该字符串现在看起来如下：

```
name=tasty1&fav=Chocolate Chip
```

注意，文本以两种方式划分。取符符号（`&`）将字符串划分为键值对，而等号（`=`）则将键值对划分为键和值。

你可以通过 `&` 字符分割字符串来创建一个数组：

```javascript
function read_it() {
  let mycookie = document.cookie;
  let thepairs = mycookie.split("&");
}
```

读取了 `cookie` 属性的值。cookie 按照取符符号（`&`）被拆分为一个数组。

前面的代码将字符串拆分为两个数组值：

- `thepairs[0]` 的值为 `name=tasty1`
- `thepairs[1]` 的值为 `fav=Chocolate Chip`

你将这些每一项都拆分为一个新的数组，数组将包含一个名称和一个值。因此，你需要类似这样的代码：

```javascript
function read_it() {
  let mycookie = document.cookie;
  let thepairs = mycookie.split("&");
  let name = thepairs[0]; // 数组元素的值
  let fav = thepairs[1]; // 将新变量赋值给变量
  let name_propval = name.split("="); // 在等号处分割
  let fav_propval = fav.split("=");
}
```

现在你使用 `name_propval` 和 `fav_propval` 数组获取了所需的所有信息：

- `name_propval[0]` 的值为 `name`
- `name_propval[1]` 的值为 `tasty`
- `fav_propval[0]` 的值为 `fav`
- `fav_propval[1]` 的值为 `Chocolate Chip`

你可以以任何喜欢的方式使用它们，例如将它们放入数组中。你现在可以对用户的值进行解码，如下例所示：

```javascript
function read_it() {
  let mycookie = document.cookie;
  let thepairs = mycookie.split("&");
  let name = thepairs[0];
  let fav = thepairs[1];
  let name_propval = name.split("=");
  // 对 cookie 进行解码并使用
  let fav_propval = fav.split("=");
  alert("The cookie's " + name_propval[0] + " is " + decodeURIComponent(name_propval[1]));
  alert("My favorite type of cookie is " + decodeURIComponent(fav_propval[1]));
}
```

在尝试运行函数中的代码之前，你可能想检查 `document.cookie` 是否存在。任何设置为以后过期的 cookie 都可以被读取，但如果没有这些，你可能会遇到错误。通过检查，你可以确保 cookie 的存在，或者将访问引导到设置 cookie 的函数。要这样做，请在函数代码周围添加一个 `if/else` 块，如下：

```javascript
function read_it() {
  let mycookie = document.cookie;
  let thepairs = mycookie.split("&");
  let name = thepairs[0];
  let fav = thepairs[1];
  let name_propval = name.split("=");
  let fav_propval = fav.split("=");
  alert("The cookie's " + name_propval[0] + " is " + decodeURIComponent(name_propval[1]));
  alert("My favorite type of cookie is " + decodeURIComponent(fav_propval[1]));
  if (document.cookie) {
    read_it();
  } else {
    set_it();
    read_it();
  }
}
```

前面的代码假设 `set_it()` 函数存在，并在需要时设置 cookie。它还假设该 cookie 是此域名设置的唯一 cookie，并且是以特定格式格式化的。如果你计划使用多个 cookie，将需要进行额外的测试以确保获取了你需要的 cookie。你可以访问 webmonkey.com/2010/02/advanced_javascript_tutorial__lesson_2/#Reading_and_Writing_cookies

## 尝试一下：读取 Cookie

| 任务 | 描述 |
| :--- | :--- |
| 1 | 创建一个 `id="greeting"` 的新 HTML 文档。 |
| 2 | 创建一个命名为 `script_2.js` 的外部 JavaScript 文件。 |
| 3 | 创建一个设置 cookie 的函数 `set_it()`。 |
| 4 | 创建一个检查 cookie 是否存在的函数 `read_it()`。 |
| 5 | 如果 cookie 存在，显示名称；如果不存在，调用 `set_it()` 然后调用 `read_it()`。 |
| 6 | 保存文件并在浏览器中打开它们。 |

## 总结

在这个项目中，你运用了设置和读取 cookie 的知识。你创建了一个记得访问者名称的 Web 页面。

## 使用正则表达式

正则表达式赋予了你处理字符串强大的能力。它们允许你形成可以与字符串进行匹配的模式，而不是尝试使用 String 对象的方法。

例如，你可能想知道文本框中输入的电子邮件地址值是否包含至少一个字符，后面是一个（`@`）符号，然后是至少一个字符，接着是一个点（`.`），最后是至少两个字符（匹配传统的电子邮件地址如 `jon@com`，或最短类型的电子邮件地址 `j@jj`）。

String 对象的方法没有提供一种简洁方便的方法来实现这种操作（尽管可以实现）。然而，正则表达式可以缩短任务，甚至将看似用 String 方法无法完成的任务变为可行。

## 创建正则表达式

要创建正则表达式，你必须创建一个 JavaScript 对象的实例或 RegExp 字面量。要创建 RegExp 字面量，你只需将正则表达式赋值给变量。与其使用引号来包裹表达式，不如使用斜杠（`/`），如下：

```javascript
let varname = /your_pattern;
```

将 `varname` 替换为你使用的变量名，并将 `your_pattern` 替换为你选择的正则表达式。你可以在斜杠后面跟随一个或多个标记（将在“添加标记”章节中讨论）。

### 注意

JavaScript 使用斜杠让浏览器知道它们之间是正则表达式，就像引号标记字符串一样。因此，如果正则表达式内部使用了斜杠，则必须使用反斜杠进行转义才能正常工作。例如，与其写成 `/02/03/2009/`，你需要写成 `/02\03\2009/`。

容易创建的正则表达式模式是寻找字符的精确匹配。例如，如果你想查看字符串中是否存在 `our` 序列，你可以创建如下正则表达式模式：

```javascript
let tomatch = /our/
```

前面的代码创建了一个名为 `tomatch` 的正则表达式字面量。现在你需要一个字符串来测试该模式。如果你用单词 `our` 来测试你的表达式，它是匹配的。如果你测试了 `your`、`sour`、`pour` 或 `pouring`，它是匹配的。如果你测试 `cool`、`Our`、`oUR`、`OUR` 或 `souR`，则不匹配。如何进行这项测试呢？

## 测试字符串正则表达式

要对字符串测试正则表达式，你可以使用 RegExp 对象的 `test()` 方法。基本语法如下：

```javascript
regex_name.test(string_to_test);
```

此语法用于使用字符串方法。将 `regex_name` 替换为正则表达式名称，并将 `string_to_test` 替换为字符串或字符串变量名。例如，看以下示例：

```javascript
let tomato = /our/
tomato.test("pour");
```

这段代码将使用名为 `tomato` 的正则表达式来测试字符串 `"pour"`。不过，它并没有使用测试结果。`test()` 方法返回一个布尔值 `true` 或 `false`。当字符串的任何部分匹配正则表达式模式时，它返回 `true`。使用 `test()` 方法，你已经编写一段短脚本，如下所示：

```javascript
let name = prompt("Enter your name,");
is_match = tomato.test(name);
if (is_match) {
  alert("Wow, we have the same name!");
} else {
  alert("Not my name, but it will work!");
}
```

- `prompt` 从查看者处获取值
- 设置了一个正则表达式以检查输入的名称是否匹配
- 使用变量来存储 `test()` 方法的结果
- 如果结果为 `true`，则显示此警告框
- 如果结果为 `false`，则显示此警告框

`prompt` 收集一个名称并存储在变量中。要匹配的模式是 `John`。测试结果被赋值给名为 `is_match` 的变量。然后该变量被用作 `if` 语句的条件。如果 `alert` 的值为 `true`，查看者将看到“Wow, we have the same name!”。如果它的值为 `false`，查看者将收到“Not my name, but it will work!”的警告框。

如果你想缩短脚本，可以直接 `test()` 方法的结果作为 `if` 语句的条件（而不是创建另一个变量），如下代码所示：

```javascript
let thename = prompt("Enter your name,");
tomatch = /John/;
if (tomatch.test(thename)) {
    alert("Wow, we have the same name!");
}
else {
    alert("Not my name, but it will work!");
}
```

- `test()` 方法的结果被用作条件

因为该方法返回 `true` 或 `false`，它可以单独作为 `if` 语句的条件。（尽管，如果你愿意，你可以把它写成 `(tomatch.test(thename)==true)`。）

## 添加标志 (Flags)

标志允许你使匹配区分大小写，或者查找字符串中的每一个匹配项而不仅仅是第一个（全局测试）。要添加标志，请将其放在正则表达式最后一个斜杠之后。你可以使用三个选项，如表 13-3 所示。

### 表 13-3 正则表达式标志

| 标志(s) | 用途 |
|--- |--- |
| i | 使匹配不区分大小写 |
| g | 使匹配全局 |
| m | 使匹配在多行模式下工作 |

如果你想调整之前使用的名称脚本使其不区分大小写，可以为正则表达式添加一个标志，如下代码所示：

```javascript
let thename = prompt("Enter your name,");
tomatch = /John/i; // i 标志使此正则表达式不区分大小写
if (tomatch.test(thename)) {
    alert("Wow, we have the same name!");
} else {
    alert("Not my name, but it will work!");
}
```

由于 `John` 模式在字符串中，`test()` 方法将返回 `true`。它可以是任何大小写，所以现在 `John`、`JOHN` 甚至 `JohnN` 都是匹配项，并将导致 `test()` 方法返回 `true`。

你也可以同时使用多个或所有三个标志。例如，如果你想让匹配不区分大小写且跨行，你可以使用以下代码：

```javascript
let tomatch = /John/im;
```

## 创建强大的模式

虽然创建一个如此精确的模式很不错，但你并不总是要寻找如此精确的匹配。在许多情况下，你将寻找一个更通用的模式，例如至少需要三个字符的条目，或者两个任意类型的字符后跟着一个特殊字符。

通过在表达式中使用特殊字符，你可以创建你所需的模式类型，来匹配你想要的序列。JavaScript 正则表达式使用 Perl 正则表达式的语法作为模型。因此，如果你在 Perl 中用过正则表达式，这里的许多材料对你来说将很熟悉。表 13-4 列出了一些字符以帮助你创建模式。

| 字符 | 用途 | 示例 |
| --- | --- | --- |
| ^ | 仅从行开始匹配 | `/^c/` 匹配 corn `/^c/` 不匹配 acorn |
| $ | 仅在行尾匹配 | `/$/` 匹配 Cat `/$/` 不匹配 acorn |
| * | 匹配前面的字符零次或多次 | `/a*/` 匹配 aa 不匹配 b |
| + | 匹配前面的字符一次或多次 | `/a+/` 匹配 aa 不匹配 b |
| ? | 匹配前面的字符零次或一次 | `/a?/` 匹配 a 或空 |
| . | 匹配任意字符（除换行符） | `/c./` 匹配 cat 不匹配 cc |
| ( ) | 用于分组 | `/(abc)/` 匹配 abc |
| \| | 逻辑或 | `/(a\|b)/` 匹配 a 或 b |
| {n} | 匹配前面的字符精确 n 次 | `/a{3}/` 匹配 aaa 不匹配 aa |
| {n,} | 匹配前面的字符至少 n 次 | `/a{2,}/` 匹配 aa 不匹配 a |
| {n,m} | 匹配前面的字符 n 到 m 次 | `/a{2,3}/` 匹配 aa 或 aaa |
| [ ] | 匹配括号内的任意一个字符 | `[abc]` 匹配 a, b, 或 c |
| [^ ] | 匹配不在括号内的字符 | `[^abc]` 匹配 d 不匹配 a |
| \ | 转义特殊字符 | `\.` 匹配字符点号本身 |
| - | 匹配范围内的字符 | `[a-z]` 匹配 a 到 z |
| \d | 匹配任何数字 | `\d` 匹配 8 |
| \D | 匹配任何非数字 | `\D` 匹配 a |
| \f | 匹配分页符 | `\f` 匹配分页符 |
| \n | 匹配换行符 | `\n` 匹配换行 |
| \r | 匹配回车符 | `\r` 匹配回车 |
| \s | 匹配任何空白字符 | `\s` 匹配空格 |
| \S | 匹配任何非空白字符 | `\S` 匹配字符 |
| \t | 匹配制表符 | `\t` 匹配制表符 |
| \v | 匹配垂直制表符 | `\v` 匹配垂直制表符 |
| \b | 匹配单词边界 | `\b` 匹配边界 |
| \B | 匹配非单词边界 | `\B` 匹配非边界 |
| \w | 匹配任何字母、数字或下划线 | `\w` 匹配 a |
| \W | 匹配任何非字母、数字或下划线 | `\W` 匹配 @ |

表 13-4 正则表达式代码

现在，如果你想确保一个文本字段包含一个或多个数字，可以使用表 13-4 中的 `\d` 和 `+` 字符配合以下 HTML 和 JavaScript 代码，首先从 HTML 代码开始：

```html
<body>
<form id="has_digits">
  <label for="user_text">输入一些文本:</label>
  <input type="text" id="user_text">
  <input type="submit" value="Test">
</form>
</body>
```

接下来，是 JavaScript 代码：

```javascript
let has_digits = document.getElementById("has_digits");
has_digits.addEventListener("submit", function(event) {
  let has_num = document.getElementById("user_text").value;
  let tomatch = /\d+/;
  event.preventDefault();
  if (tomatch.test(has_num)) {
    alert("您的输入包含一个或多个数字!");
  }
  else {
    alert("您的输入不包含任何数字!");
  }
}, false);
```

这段代码简单地检查字符串中是否包含数字。如果你想确保查看者输入的*仅*是数字而不包含任何其他类型的字符，你需要确保正则表达式被编写为从头到尾进行测试。通过使用表 13-4 中的 `^` 符号和 `$` 符号，你可以确保对字符串进行从字符串开始到字符串结束的全量匹配测试。跟在 `\d` 之后的 `+` 确保了至少输入了一个数字。因此，以下模式将只允许数字：

```javascript
let tomatch = /^\d+$/;
```

由于从字符串开始到结束的唯一有效字符是数字，对于包含数字且字符串中没有其他字符的输入，这将返回 `true`。这对于验证表单和其他类型的用户输入特别有帮助，可以确保输入类型是你所预期的类型。

### 注意

正则表达式在验证方面非常强大，因为它们允许接受更少的错误信息。

使用电子邮件地址或电话号码等数据对表单提交进行客户端验证可以减少不必要的服务器往返。然而，用户可能会禁用 JavaScript 支持并直接提交表单。因此，客户端验证应该支持服务器端验证（例如通过 PHP 脚本或 CGI 脚本），但不应取代它（存储或显示来自未经过验证的查看者的数据可能会导致安全风险）。

## 组表达式

你会在表 13-4 中注意到，由括号围绕的表达式表示一个可以存储以备后用的组（使用如 `match()` 方法等方法，在该方法中，它将组中的每个项连同整体匹配一起存储在数组中）。

例如，你可能决定使用特定的数字序列并让该序列重复特定的次数。为了匹配某个内容重复的次数，可以使用大括号 `{}` 配合数字或范围。例如，如果你想匹配五次数字 3，可以使用以下表达式：

```javascript
/3{5}/
```

如果你希望当数字 3 至少出现 5 次但不超过 10 次时进行匹配成功，你可以使用以下表达式：

```javascript
/3{5,10}/
```

现在，假设你想让匹配以 3 开始，下一个字符是任何数字，并希望匹配整个序列五次（因此，像 3243536367 的内容将是一个匹配）。你可能会这样写：

```javascript
/3\d{5}/
```

这种做法的问题是，它正确获取了 3，但匹配了五个数字，而不需要重复 3。因此，像 387643 这样的数字会被匹配，尽管你想要的是五组都以 3 开头的数字。为了修复这个问题，你可以用括号将 3 和 `\d` 组合在一起，然后匹配它应该重复的次数：

```javascript
/(3\d){5}/
```

这一次，3 和第二个数字被组在了一起，该序列必须重复五次。

分组是充分利用正则表达式的一种非常有用的方法，当你在下一章学习表单验证时，你会看到其中之一。

## replace(), match(), matchAll(), 和 search() 方法

String 对象的这些方法在章的早期部分提到过，现在引入了正则表达式后，它们将变得更有意义。

## replace() 方法

要替换字符串中的信息，可以使用正则表达式和 String 对象的 `replace()` 方法。使用 `replace()` 方法的语法如下：

```javascript
varname = stringname.replace(regex, newstring);
```

你将 `varname` 替换为在信息替换后将持有新字符串值的变量名。你将 `stringname` 替换为将进行替换的字符串变量名。你将 `regex` 替换为用于匹配字符串或字符串变量以替换匹配值的正则表达式名称。最后，你将 `newstring` 替换为被替换后的字符串变量名。

例如，以下代码将 `mystring` 中的第一个实例 "car" 替换为 "skunk"：

```javascript
let mystring = "I like the new car smells, and cars are fun.";
let toreplace = /car/; // 模式
let newstring = mystring.replace(toreplace, "skunk");
```

如果带有 `g` 标志或使用分组 `()`，它将记住找到的每个匹配项（包括分组或嵌套分组中的匹配项），并将每个匹配项作为数组元素返回。`matchAll()` 方法在此基础上工作，将找到的所有匹配项以数组的形式返回。

## search() 方法

`search()` 执行正则表达式与指定字符串之间匹配的搜索。如果找到了匹配项，它返回字符串中匹配项开始处所在的位置。否则，它返回 -1。以下是该方法的用法示例：

```javascript
let mystring = "I am Ironman!"
tomatch = /Iron/;
if (mystring.search(tomatch)) {
  alert("Iron found at position " + mystring.search(tomatch) + "!");
} else {
  alert("Sorry, no Iron in your string.");
}
```

如你所见，其语法与 `match()` 相似。

### 更多信息

关于正则表达式以及如何创建更复杂的模式的更多信息，你可以参考以下在线资源：

- www.regular-expressions.info/
- www.regular-expressions.info/javascript.html（包含 JavaScript 引擎的特定细节）
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

掌握这些技术后，你就可以准备开始处理 JavaScript 中的表单以及表单内容的验证了。

## 继续项目

在本章中，你将更新你的 Node.js 项目，开始为应用中的保龄球手创建前端 HTML 和 CSS 样式。随着后续章节的进行，HTML 骨架将被填充实际数据。

首先，在你的项目中创建一个名为 `public` 的文件夹。该文件夹将用于存储 CSS 和前端 JavaScript 文件。你可能记得在 `server.js` 文件中看到过以下代码：

```javascript
app.use(express.static(path.join(__dirname, 'public')));
```

这告诉 Express 在项目内名为 `public` 的文件夹中查找静态资源（如 CSS 和 JS 文件）。你可以在其中创建文件夹，但由于这是一个简单的应用程序，你将直接把资源放在 `public` 文件夹中。

接下来，创建一个带有代码的 CSS 文件并将其保存为 `styles.css` 到 `public` 文件夹中：

```css
body {
  margin: 2% 5% 0 5%;
}
```

你将在 `index.html` 文件中引入此 CSS。准备好后，更新项目文件夹中的 `index.html` 文件以包含以下代码：

```html
<html>
<head>
  <title>Bowler Stats</title>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
  <h1>Bowler Stats</h1>
  <table id="bowlers-table" border="1" cellspacing="0">
    <thead>
      <tr>
        <th>Name（姓名）</th>
        <th>Accuracy（准确率）</th>
        <th>Power（力量）</th>
        <th>Consistency（稳定性）</th>
        <th>Overall（总分）</th>
      </tr>
    </thead>
    <tbody id="bowlers-list">
      <!-- 在此处填入信息 -->
    </tbody>
  </table>
</body>
</html>
```

保存文件。如果你想查看生成的 HTML 壳页面，请确保已启动了 Node 服务器，然后访问 `http://localhost:3000` 查看基础 HTML。当你从数据库中获取信息并将其拉取到前端代码中时，就需要填充这些内容。如你所见，计划是为表格的 `tbody` 部分填充包含每个保龄球手信息的行。这将在第 15 章你学习 AJAX 后完成。

## 第 13 章自测

1. ________ 对象提供了属性和方法，用于获取字符串信息以修改字符串。
2. 创建 String 对象的两种方式是：
   - A. 创建 String 对象的实例并创建字符串字面量
   - B. 创建 Array 对象的实例并创建字符串字面量
   - C. 创建数字变量并创建数字对象
   - D. 创建字符串并添加数字
3. 你可以通过给变量赋值字符串值来创建一个字符串 ________。
4. 普通文本字符串能够使用 String 对象的方法，是因为：
   - A. 它已经是一个 String 对象。
   - B. 它也可以使用其他方法，因此可以使用 String 对象的方法。
   - C. JavaScript 获取字符串字面量并将其转换为临时的 String 对象。
   - D. String 对象原样使用字符串字面量。
5. String 对象的哪个属性可以同时用于 String 对象和字符串字面量？
   - A. prototype
   - B. constructor
   - C. length
   - D. color
6. ________ 属性返回字符串的长度。
7. 下列哪个正确创建了字符串字面量？
   - A. `let the_text = “Look at me!;`
   - B. `let the_text = “Look at me!”;`
   - C. `let the_text = Look at me!`
   - D. `let the_text = new String(“Look at me!”);`
8. 你可以使用 String 对象的哪个方法来查找字符？
   - A. `indexOf()`
   - B. `charAt()`
   - C. `isAt()`
   - D. `position()`
9. 哪个方法将两个字符串相在一起？
10. 下列哪个说法是正确的？
    - A. `charAt()` 方法返回数值。
    - B. `split()` 创建新数组。
    - C. `length` 属性返回字符数量。
    - D. `concat()` 方法返回字符串。
11. 哪个方法返回指定位置的字符串？
12. cookie 属性存储在 window 中。
13. replace 方法用另一个字符串替换字符串。
14. 该方法查找字符的首次出现。
15. 该方法比较两个字符串。

# 第 14 章：基于浏览器的 JavaScript

| 属性 | 说明 |
| --- | --- |
| parent | 指向包含当前帧的帧集 (frame set) |
| screen | 包含收集屏幕信息的属性，包括 `availHeight`、`availWidth`、`colorDepth`、`height`、`pixelDepth` 和 `width` |
| scrollX | 返回页面水平滚动的像素数 |
| scrollY | 返回页面垂直滚动的像素数 |
| self | 提供引用当前窗口的另一种方式 |
| status | 允许在状态栏中放置消息；覆盖默认的 status |
| top | 指向包含帧、帧集或嵌套帧集的顶层窗口的引用 |
| window | 指向当前窗口的引用 |

表 14-1 Window 对象的属性

> 注意
> 在之前的章节中，本章列举的某些属性和方法并不具有跨浏览器兼容性，或者仅在现代浏览器中有效。欲了解更多信息和完整的属性列表，请访问 https://developer.mozilla.org/en/DOM/window。

## closed 属性

`closed` 属性用于检查窗口是否已被查看者关闭。通常用法是配合窗口名称使用，后跟 `closed` 属性，如下例所示：

```javascript
if (window.closed) {
  // JavaScript 语句
}
```

你应当将 `windowname` 替换为你想要检查的窗口名称。这通常是你用 JavaScript 打开的一个新窗口；你将在本章稍后的“open() 方法”部分中学习如何命名新窗口。

你也可以在新窗口内部使用 `closed` 属性来检查打开窗口是否已关闭。要做到这一点，你可以在 `opener` 属性（在“Opener 属性”节讨论过）之后使用 `closed`，如下例所示：

```javascript
if (window.opener.closed) {
  // JavaScript 语句
}
```

如果你选择创建一个新窗口，允许查看者通过新窗口中的链接导航主窗口，那么这种 `closed` 属性的用法非常有用。

## frames 属性

`frames` 属性是一个包含帧集内每个帧的数组。它通常用于访问窗口上各种帧的属性。你可以通过使用 `frames.length` 属性获取窗口中帧的数量。

## innerWidth 和 innerHeight 属性

`innerWidth` 和 `innerHeight` 属性持有窗口区域的宽度和高度值（包括浏览器窗口滚动条、菜单栏、工具栏等）。这些属性在现代浏览器中有效，但在版本 9 的 Internet Explorer 中无效（旧版本的 Internet Explorer 可以使用 `document.body.clientWidth` 和 `document.body.clientHeight`）。

因此，如果你想获取脚本可用的内容区域的宽度，可以使用以下代码：

```javascript
let myWidth = window.innerWidth;
```

当然，如果你想根据窗口可用的 `innerWidth` 为浏览器使用不同的 HTML 代码，可以使用以下代码：

```javascript
// innerWidth 属性的值将访问一个“容器”div，它将没有设置宽度，并将容纳通过 innerHTML 提供的代码
let myWidth = window.innerWidth;
let cont = document.getElementById("container");
cont.style.width = (myWidth >= 800) ? "750px" : "90%";
```

条件运算符用于快速的 if-else 语句，根据可用空间为 div 元素分配宽度。

这将决定查看者是否具有 800 像素的宽度。如果是，div 元素的宽度将设置为 750 像素。否则，div 元素将具有更安全的 90% 宽度，以便在较小的屏幕上更容易显示。

## length 属性

`length` 属性告诉你有窗口中有个帧，类似于 `window.frames.length` 属性。它将其简写为 `window.length`（这在编写代码时通常更方便）。

## location 属性

`location` 属性持有窗口的当前 URL。你可以使用 `location` 属性导致浏览器立即加载到新页面（例如，如果你的页面已移动到新位置）。但是，请确保不要在未允许快速重定向的搜索引擎页面上使用此技术，它们可能会将该页面从列表中删除。

如果页面已经移动，且你想不延迟地重定向查看者，你只需要给 `location` 属性赋一个新值，如下代码所示：

```html
<body>
  <script type="text/javascript">
    window.location = "newpage.html";
  </script>
</body>
```

这会立即让查看者离开，因为此动作中不需要执行任何操作。

缺少 JavaScript？请点击下方的链接跳转到新页面！`<a href="newpage.html">新页面</a>`

这将把查看者带到本地 URL `newpage.html`。对于没有 JavaScript 的浏览器，包含了一个标准链接。否则，上述代码将为那些不发生这种情况的用户加载一个空白页。

> 注意
> 立即重定向最适用于未索引页面的测试目的。

## name 属性

`name` 属性持有窗口名称并允许你为窗口命名。以下代码显示了一个示例：

```javascript
window.name = "cool_window"; // 给窗口赋予了名称
alert("此窗口是 " + window.name); // 向查看者提示窗口的名称
```

## opener 属性

`opener` 属性用于引用打开当前窗口的窗口。这通常用于使用 `open()` 方法打开的新窗口，你将在本章稍后看到。通过使用 `opener` 属性，你可以检测主窗口是否已关闭。以下示例显示了如何操作：

```javascript
if (window.opener.closed)
```

在 `opener` 之后添加 `closed` 属性是为了检查窗口是否关闭。如果你想通过新窗口在主窗口执行操作，这非常有帮助，因为你可以检查它仍然存在。

## parent, self 和 top 属性

`parent` 属性仅用于页面上有帧或 iframe 的情况。它允许你访问当前帧的父帧集。当你想从一个帧更改另一个帧的属性时非常有帮助。

`self` 属性是 JavaScript 中“当前窗口”的另一种表达方式。它像 `window` 对象一样使用，并可以像 `window` 对象一样访问当前窗口的属性。如果你有很多命名的窗口，为了确保你使用的是当前窗口的属性而不是另一个的属性，`self` 属性非常有用。

`top` 属性用于访问所有帧集（可能是嵌套的）中的顶层窗口。这与 `parent` 属性不同，后者只到当前帧集的顶部。而 `top` 属性一直到达顶层窗口，即使窗口包含嵌套的帧集。

## status 和 defaultStatus 属性

`status` 属性包含窗口状态栏设置的文本值。更改此属性将用 `defaultStatus` 属性覆盖状态栏的内容。

### 注意事项

现代浏览器默认不显示由 JavaScript 修改的状态栏文本，以防止不良 Web 网站通过状态栏中的虚假链接目标欺骗用户。因此，除非查看者更改浏览器设置，否则 `status` 和 `defaultStatus` 属性将无法工作。由于用户更改浏览器设置允许此类操作存在安全风险，因此不建议使用这些属性。

`status` 属性设置了当 `window.status` 未分配任何值时，在状态栏中默认显示的字符串。对 `window.status` 属性的更改会覆盖此设置，因为它仅作为默认值显示。该属性通常在 `load` 事件中设置，以便在查看者未执行会更改状态栏文本的操作时显示自定义消息。

## 尝试此练习 14-1 使用 location 和 innerWidth 属性

`prjs14_1.html` 这将让你练习使用 window 对象的 `location` 和 `innerWidth` 属性。

### 步骤详解

1. 创建一个 HTML 页面，除了在 `<body>` 部分留空外，在 `</body>` 结束标签之前包含一组 `<script>` 标签以引用名为 `prjs14_1.js` 的 JavaScript 文件。将文件保存为 `prjs14_1.html`。
2. 创建一个 JavaScript 文件并保存为 `prjs14_1.js`。在步骤 3-6 中使用此文件。
3. 为名为 `mywin.width` 的变量设置一个默认值。
4. 将 `window.innerWidth` 的值赋值给 `mywin.width`。
5. 如果 `mywin.width` 的值大于等于 1000，将查看者发送到 URL http://github.com。否则，将查看者发送到 URL http://developer.mozilla.org（使用 `window.location`）。
6. 完成后，JavaScript 文件应具有以下代码：

```javascript
let my_win = window.innerWidth;
if (my_win >= 1000) {
  window.location = "http://github.com";
}
else {
  window.location = "http://developer.mozilla.org";
}
```

7. 保存 JavaScript 文件并在浏览器中打开 HTML 文件。尝试更改宽度并使用新宽度重新打开页面，查看跳转到哪个页面。

### 尝试此练习总结

在这个项目中，你能够利用对 window 对象的 `location` 和 `innerWidth` 属性的知识，创建一个脚本，根据查看者浏览器的可用宽度来重定向查看者。

## 使用 Window 对象的方法

现在你已经知道如何使用 window 对象的属性，可以继续学习使用方法了。表 14-2 列出了 window 对象的若干方法及其描述，并对特定方法进行了详细说明。

| 方法 | 描述 |
| :--- | :--- |
| addEventListener() | 在窗口上注册一个事件 |
| alert() | 向查看者弹出一个警告框，查看者必须点击 OK 继续 |
| blur() | 移除窗口的焦点 |
| clearInterval() | 取消 `setInterval()` 方法的作用 |
| clearTimeout() | 取消 `setTimeout()` 方法的作用 |
| close() | 关闭浏览器 |
| confirm() | 向查看者显示确认对话框，查看者必须点击 OK 继续 |
| decodeURIComponent() | 将转义后的字符串转换回 URI |
| encodeURIComponent() | 将字符串中的特殊字符转换为 URI（例如，空格被转换为 %20） |
| find() | 允许查看者在页面上查找文本 |
| focus() | 赋予窗口焦点 |
| moveBy() | 通过参数发送的像素值移动窗口 |
| moveTo() | 将窗口的左上角移动到参数发送的坐标 |
| open() | 打开一个新窗口 |
| print() | 打印窗口内容 |
| prompt() | 弹出一个提示框向查看者询问信息 |
| resizeBy() | 通过参数发送的像素值移动右下角来调整窗口大小 |
| resizeTo() | 根据参数发送的高度和宽度调整整个窗口 |
| scrollBy() | 通过参数发送的像素值滚动窗口的可视区域 |
| scrollTo() | 将窗口的可视区域滚动到参数指定的特定坐标 |
| setInterval() | 每隔一段时间调用一次函数 |
| setTimeout() | 在经过一段时间后调用一次函数 |
| stop() | 停止窗口加载其内容 |

## alert(), prompt(), 和 confirm() 方法

`alert()`、`prompt()` 和 `confirm()` 方法都会弹出一个需要用户采取操作的对话框。例如，用户可以点击 OK 关闭警告框，或者在使用 `prompt` 时在文本框中输入信息。

### alert() 方法

你在前面的章节中已广泛地使用了 `alert()` 方法。它会向查看者弹出一个消息，查看者有一个 OK 按钮可以继续操作。

### prompt() 方法

`prompt()` 方法用于提示查看者输入信息。你在第 6 章中使用此方法来允许用户在提示对话框中输入数据。

### confirm() 方法

`confirm()` 方法可以给查看者一个确认或取消操作的机会。该方法返回 `true` 或 `false` 的布尔值，因此其结果通常会被赋值给变量。所以，如果你想将结果赋值给名为 `is_sure` 的变量并回答“你确定吗？”，可以使用以下代码：

```javascript
let is_sure = confirm("Are you sure?");
```

图 14-2 显示了上述通知显示的示例对话框。注意查看者可以选择点击的两个按钮：OK 和 Cancel。如果查看者点击 OK，该方法返回 `true`。如果查看者点击 Cancel，该方法返回 `false`。注意，对于 `alert()` 和 `prompt()`，你无法更改按钮的值，但这是由用户的浏览器和操作系统定的。

作为该方法的真实示例，假设你想创建一个另一个页面的链接，但你想在查看者离开之前确定。你可以使用对话框确定查看者是否希望离开。以下代码显示了你如何获取查看者的确认并做出相应反应。第一个 HTML 代码：

```html
<body>
  <a href="http://www.google.com" id="search_link">Go Searching</a>
</body>
```

接下来，使用 JavaScript 在点击链接时确认用户是否想离开：

```javascript
let s_link = document.getElementById("search_link");
s_link.addEventListener("click", function(event) {
  let is_sure = confirm("Are you sure want to leave?");
  if (is_sure == false) {
    event.preventDefault();
    alert("OK. You can stay here.");
  }
}, false);
```

该函数确认查看者是否想离开。

注意如果点击 OK 且 `confirm()` 方法返回 `true`，查看者将被带到链接的网站。如果点击取消且 `confirm()` 方法返回 `false`，则向查看者发送一个警告且函数返回 `false`，这样浏览器就不会跳转链接（你可以仅通过返回 false 来省略警告）。

## setInterval() 和 clearInterval() 方法

`setInterval()` 方法用于按设置的时间间隔重复执行 JavaScript 函数。以下是使用该方法的通用语法：

```javascript
setInterval(function() { // 函数内容 }, time);
```

你用你想要重复的代码替换函数内容。然后，你用 `time` 替换为你希望在每次重复执行函数之前等待的时间（以毫秒为单位）。

所以，如果你想骚扰你的观众，可以使用此方法在页面查看后，每隔 10 秒（10,000 毫秒）弹出一个警框。你可以通过在 HTML 中放置以下脚本来实现：

```javascript
setInterval(function() { 
alert("Am I bothering you?"); // 设置了一个 10,000 毫秒（10 秒）的间隔
}, 10000);
```

当然，这可能会非常烦人。间隔设置的时间越短，就会越烦人。幸运的是，10 秒的间隔让你有足够的时间在警框弹出之前离开页面。

### 注意

你可能会遇到某些将字符串值作为第一个参数传递给 `setInterval()` 或 `setTimeout()` 的脚本。这要求 JavaScript 使用 `eval()` 函数将字符串评估为 JavaScript 代码，在大多数情况下，是不建议使用该函数的。

为了结束上一个脚本产生的连环警框，你可以使用 `clearInterval()` 方法。以下是使用该方法的通用语法：

```javascript
clearInterval(name);
```

你必须将变量替换为已赋值给想要清除的 `setInterval()` 调用的名称。问题是，在上一个示例中，你没有将 `setInterval()` 赋值给变量名。

为了清除，你需要调整代码。更新后的代码将 `setInterval()` 赋值给变量名：

```javascript
let madness = setInterval(function() { 
alert("Am I bothering you yet?"); // 将方法调用赋值给变量以供稍后引用
}, 10000);
```

现在你有了使用 `clearInterval()` 方法的方法，即通过将 `madness` 变量作为参数调用它。因此，为访问者提供一个按钮让他们停止这种“疯狂”。只要在间隔期间点击它，它就会停止间隔继续运行。

以下代码为你提供了一个带有按钮的 HTML 页面供观众点击，以及更新后的 JavaScript 代码：

```html
<body>
点击下方按钮以结束无休止的警框。<br>
<form>
<input type="button" value="Stop the Madness!" id="stop_it">
</form>
</body>
```

更新后的 JavaScript 代码：

```javascript
let madness = setInterval(function() {
    alert("Am I bothering you yet?");
}, 10000);
let stop_it = document.getElementById("stop_it");
stop_it.addEventListener("click", function (event) {
    event.preventDefault();
    clearInterval(madness);
}, false);
```

现在观众可以通过点击“停止疯狂”按钮来停止警框。你稍后会发现这种方法对于时钟以及页面上需要定期间隔更新的其他内容非常有用。

## setTimeout() 和 clearTimeout() 方法

`setTimeout` 方法允许你在一定时间过去后执行 JavaScript 函数。它与 `setInterval` 方法的不同之处在于，它只执行一次（除非它被放在某种循环中）。其通用语法与 `setInterval()` 相同。

如果你只想在十秒后弹出一个警框而不重复，可以使用以下代码：

```javascript
let theguest = setTimeout(function() {
    alert("Sign my guest book NOW!");
}, 10000);
```

这会在十秒后向观众发送一个警框，要求访客立即签名。`clearTimeout` 方法允许你在 `setTimeout()` 调用的时间过期之前调用 `clearTimeout()` 方法来取消该调用。其通用语法与 `setInterval` 方法相同：你使用变量名作为参数，以便它知道要取消哪个 `setTimeout()`。

所以，如果你想给观众一个避免警框的机会，可以为他们添加一个在十秒内点击的按钮。如果在此时间内点击了按钮，`setTimeout()` 调用将被取消，不会弹出警框。以下是示例代码：

```html
<body>
在 10 秒内点击下方按钮以避免警框消息。<br>
<form>
<input type="button" value="No Alert for Me!" id="noalert">
</form>
</body>
```

JavaScript 代码：

```javascript
let theguest = setTimeout(function() {
  alert("Sign my guest book NOW!");
}, 10000);
noalert.addEventListener("click", function(event) {
  clearTimeout(theguest);
}, false);
```

定时器已清除，如果及时点击按钮，则它将停止发生。如果及时点击了按钮，观众将等待接收关于签名留言簿的警框。

## 专家问答

**问：** 这里有太多属性和方法了！我该如何记住所有它们？

**答：** 随着你开始频繁使用它们，它们会变得更容易记住。我常用的比不怎么用的更容易记住。如果你编写大量的代码，随手保留一份参考资料是好的，比如这本书，以防你需要检查属性或方法的细节并留住它们。

## 打开新窗口

`open()` 方法允许你使用 JavaScript 打开一个新窗口。该方法通常带有三个参数，如示例所示：

```javascript
window.open("URL", "name", "attribute1=value, attribute2=value");
```

第一个参数 `"URL"` 被替换为要在新窗口中打开的 HTML 文档的 URL。`"name"` 参数被替换为你想要给该窗口起的名字。第三个参数允许你为新窗口添加属性。这些属性通过等号右侧的 `"yes"`、`"no"` 或数值来设置。注意，每个属性都设置了一个值，在下一个属性之前有一个逗号，且之间没有空格。

如果你想打开一个具有当前窗口特征的窗口，可以通过保留旧窗口的属性来实现。下面的示例将打开一个 URL 为 `webpage.html` 且名为 `my_window` 的新窗口；它将具有与打开它的窗口相同的特征：

```javascript
window.open("newpage.html", "my_window");
```

### 属性

如果你想包含窗口特征，你需要学习可以与窗口一起使用的属性。表 14-3 列出了你可以作为 `open` 方法第三个参数部分的属性。任何 `"yes"` 或 `"no"` 属性如果没有被浏览器覆盖，其默认不会是 `"no"`。例如，`location`、`menubar`（菜单栏）和 `status` 属性在大多数现代浏览器中可能默认为 `"yes"` 且不会改变。定义的任何数值将使用所用浏览器的设置。这些设置也可能是不可更改的或只允许某些值。例如，新窗口可能需要 `left` 和 `top` 坐标以将其放置在屏幕的可视区域，且 `width` 和 `height` 可能有最小值，以防止窗口太小导致用户无法注意。

| 属性名称 | 可能的值 | 功能 |
| --- | --- | --- |
| width | number | 定义新窗口的宽度（像素） |
| height | number | 定义新窗口的高度（像素） |
| top | number | 定义新窗口的顶部坐标 |
| left | number | 定义新窗口的左侧坐标 |
| fullscreen | yes, no, 1, 0 | 定义新窗口是否应以最大化方式打开。仅在 Internet Explorer 中有效 |
| location | yes, no, 1, 0 | 定义新窗口是否有一个可以输入新 URL 的位置框 |
| menubar | yes, no, 1, 0 | 定义新窗口是否有一个菜单栏（文件菜单、编辑菜单等） |
| resizable | yes, no, 1, 0 | 定义是否允许用户调整新窗口的大小 |
| scrollbars | yes, no, 1, 0 | 定义如果窗口内容大于窗口大小，新窗口是否具有滚动条 |
| status | yes, no, 1, 0 | 定义新窗口底部是否有一个状态栏 |
| toolbar | yes, no, 1, 0 | 定义新窗口是否有一个工具栏（前进、后退按钮、停止按钮等） |

**表 14-3** 新窗口的标准属性

要打开一个宽度为 400 像素、高度为 300 像素的基础新窗口，你可以使用以下代码：

```javascript
window.open("newpage.html", "my_window", "width=400,height=300");
```

除了宽度和高度外，此窗口将以其他属性的默认值打开，这取决于用户所使用的浏览器。要设置其他属性，你可以根据是否需要每项功能来分配 `"yes"` 或 `"no"` 值。如果你愿意，也可以用 1 表示 yes，用 0 表示 no，因为它们的效果相同。如果你想要一个 300x200 像素且带有菜单栏的窗口（这将添加前进、后退、停止和其他按钮），可以使用以下代码：

```javascript
window.open("newpage.html", "cool", "width=300,height=200,menubar=yes");
```

这为你提供了一个包含 `newpage.html` 内容、名为 `"cool"`、尺寸为 300x200 像素并带有菜单栏的新窗口。你可以通过逗号分隔每个属性，在属性的引号内添加任意数量的属性。

### 注意

由于空间限制，本书中的新窗口命令在代码中可能会比单行多。请确保在使用代码时，务必将从 `window.open` 到分号（`;`）的所有内容放在同一行上，以避免 JavaScript 错误。

下面的示例打开了一个包含表 14-3 中提到的大多数特征的窗口（再次说明，这里超过了一行，但当你在文本编辑器中输入时，代码应该在单行内）：

```javascript
window.open("newpage.html","cool","width=300,height=200,top=0,left=0,location=yes,menubar=yes,resizable=yes,scrollbars=yes,status=yes,toolbar=yes");
```

如果你想要另一个示例，可能需要创建一个名为 `newpage.html` 的页面，并为主页创建代码以包含 `window.open()` 命令，如接下来所述。

首先，创建 `newpage.html` 的代码（这是一个包含一些文本的短页面）：

```html
<body>
我是一个新窗口！我比打开我的那个旧窗口要新，
所以我是特别的。哈，哈！
</body>
```

接下来，创建主页面（保存为 `mainpage.html`）：

```html
<body>
点击下方的链接打开一个新窗口<br>
<a href="newpage.html" id="nwin">新页面</a>
<script type="text/javascript" src="window.js"></script>
</body>
```

链接被赋予了一个分配给变量的 id。最后，创建 JavaScript 代码（保存为 `nwin.js`）：

```javascript
let nwin = document.getElementById("nwin");
nwin.addEventListener("click", function (event) {
  event.preventDefault();
  window.open("newpage.html","cool","width=400,height=300,status=yes");
}, false);
```

该函数打开新窗口并防止链接的默认操作。当链接被点击时，它会启动带有 `newpage.html` 文档内容的新窗口。该窗口底部有一个状态栏。注意添加 `event.preventDefault()` 方法是为了确保 `newpage.html` 文件不会在主窗口中打开（如果用户未启用 JavaScript，链接将正常工作并在同一窗口中打开 `newpage.html` 文件）。

## 关闭新窗口

`close()` 方法用于关闭窗口；除非脚本具有某些安全权限，否则该方法只能关闭使用 JavaScript 打开的窗口。它无法关闭主窗口（尽管某些浏览器会通过确认对话框提供选项）。

要使用 `close()` 方法，你可以修改 `webpage.html` 代码，在文本末尾提供一个按钮，允许用户通过点击它来关闭窗口。因此，你可以将 `webpage.html` 的代码更改如下所示：

```html
<body>
我是一个新窗口！我比打开我的那个旧窗口要新，
所以我是特别的。哈，哈！
<form>
<input type="button" value="关闭窗口" onclick="window.close();">
</form>
</body>
```

当点击按钮时，会调用 `window.close()` 方法并关闭窗口，就像窗口右上角的标准关闭按钮一样。如果你想尝试一下，可以使用你在上一节中使用的主页面，并点击按钮打开新窗口。它应该会提供一个带有关闭窗口选项的新按钮，并且在你点击该按钮时它应该会关闭。

如果你倾向于从主窗口关闭新窗口，可以通过将 `open()` 方法赋值给变量来实现，这将提供对新窗口的引用。然后，你可以添加另一个提供关闭窗口选项的链接。你可以修改 `mainpage.html` 来使用以下代码：

```html
<body>
点击下方的链接打开一个“傲慢”的新窗口 ...<br>
<a href="page.html" id="win">新页面</a>
<a href="mainpage.html" id="cwin">关闭新页面</a>
<script type="text/javascript" src="open.js"></script>
</body>
```

添加了一个新链接以便关闭新窗口。接下来，你需要编辑 `mainpage.js` 来使用以下代码：

```javascript
let nw_win = document.getElementById("win");
cs_win = document.getElementById("cwin");
mywin = "";
nw_win.addEventListener("click", function (event) {
  event.preventDefault();
  mywin = window.open("page.html", "cool", "width=400,height=300,status=yes");
});
cs_win.addEventListener("click", function (event) {
  event.preventDefault();
  mywin.close(); // 窗口已关闭
});
```

添加了新变量：`cs_win` 用于访问“关闭新页面”链接，`mywin` 将稍后被用作新窗口的引用。这允许通过主窗口同时打开和关闭窗口。

## 移动、调整大小和滚动新窗口

`moveTo()`、`resizeTo()`、`scrollTo()` 和 `scrollBy()` 方法允许你更改窗口位置、窗口大小或窗口内的起始位置。配合 `close()` 方法，浏览器通常不允许在主窗口上使用这些方法。然而，它们可以在通过 JavaScript 创建的窗口上使用。

### moveBy() 和 moveTo() 方法

`moveBy()` 方法可将新窗口移动到屏幕上的新位置。它通过方法参数中提供的像素数来移动窗口。以下是使用该方法的语法：

```javascript
moveBy(x-pixels, y-pixels);
```

你将 `x-pixels` 替换为你想让窗口从左向右移动的像素数。如果你想向右移动窗口，输入一个正数。如果你想让它向左移动，输入一个负数。你将 `y-pixels` 替换为你想让窗口从顶到底移动的像素数，正数会将窗口向下推，负数会将窗口向上拉。

例如，如果你想让观众根据你选择的像素数移动窗口，你可以修改代码来处理此操作。对于 `mainpage.html`，请使用以下代码：

```html
<body>
点击下方的链接打开一个“傲慢”的新窗口 ...<br>
<a href="new.html" id="win">新页面</a>
<a href="mainpage.html" id="aw">修改新页面</a>
<script type="javascript" src="openwin.js"></script>
</body>
```

链接提供了修改新窗口的选项。接下来，使用以下代码用于 `openwin.js`：

```javascript
let nw_win = document.getElementById("win");
aw_win = document.getElementById("aw");
ymin = "";
nw_win.addEventListener("click", function (event) {
  event.preventDefault();
  ymin = window.open("newpage.html", "cool", "width=400,height=300,status=yes");
}, false);
aw_win.addEventListener("click", function (event) {
  event.preventDefault();
  ymin.moveBy(0, 50); // 窗口向右移动了 50 像素
  ymin.focus(); // 窗口重新获得焦点以便可见
}, false);
```

这在点击按钮时会使窗口向右移动 50 像素并向下移动 50 像素。注意在移动后调用了 `focus()` 方法。如果你点击窗口中的链接来移动新窗口，新窗口将失去焦点（触发 blur 事件）。该方法仍然有效，但如果窗口覆盖了它，你可能看不见这一点（因为在点击链接时它会重新获得焦点）。将焦点重新置于新窗口上将使其显示在任何其他打开的窗口之前。同样，`blur()` 方法可以让窗口失去焦点，但浏览器可能将其作为安全特性，以确保窗口不会被脚本隐藏。

`moveTo` 方法用于将窗口移动到特定位置，基于调用时传递的参数。

```javascript
moveTo(x-value, y-value);
```

在这里，你将 `x-value` 替换为你想让窗口从左侧移动的像素数。将 `y-value` 替换为你想让窗口从顶部移动的像素数。作为示例，修改 `open.js` 代码，在以下代码中使用 `moveTo()` 代替 `open()`：

```javascript
let nw_win = document.getElementById("win");
aw_win = document.getElementById("aw");
mywin = "";
nw_win.addEventListener("click", function (event) {
  event.preventDefault();
  mywin = window.open("page.html", "cool", "width=400,height=300,status=yes");
}, false);
aw_win.addEventListener("click", function (event) {
  event.preventDefault();
  mywin.moveTo(50, 50);
  mywin.focus();
}, false);
```

窗口将移动到 (50, 50) 位置，这是在点击链接时设置的。与 `moveBy()` 方法不同，因为它使用的是绝对位置。

### resizeBy() 和 resizeTo() 方法

`resizeBy()` 方法通过方法传递的像素数来调整窗口大小。要让窗口变大，使用正数。要使其变小，使用负数。例如，你可以修改 `openwin.js` 代码，使用以下代码：

```javascript
let nw_win = document.getElementById("win");
aw_win = document.getElementById("aw");
ymin = "";
nw_win.addEventListener("click", function (event) {
  event.preventDefault();
  ymin = window.open("newpage.html", "cool", "width=400,height=300,status=yes");
}, false);
aw_win.addEventListener("click", function (event) {
  event.preventDefault();
  ymin.resizeBy(-100, -100); // 负数将使窗口变小
  ymin.focus();
}, false);
```

这段代码将窗口宽高各缩小 100 像素。与 `moveTo()` 类似，再次点击链接将继续调整大小。出于安全原因，浏览器会停止调整窗口直到达到最小允许尺寸，并在窗口尺寸达到屏幕最大可视区域时停止。

`resizeTo()` 用于根据方法传递的参数将窗口调整大小为特定的像素尺寸。例如，你也可以修改 `openwin.js` 文件。使用以下代码：

```javascript
let nw_win = document.getElementById("win");
aw_win = document.getElementById("aw");
mywin = "";
nw_win.addEventListener("click", function (event) {
  event.preventDefault();
  mywin = window.open("newpage.html", "cool", "width=400,height=300,status=yes");
}, false);
aw_win.addEventListener("click", function (event) {
  event.preventDefault();
  mywin.resizeTo(600, 600); // 窗口被调整大小为 600 像素乘 600 像素
  mywin.focus();
}, false);
```

### scrollBy() 和 scrollTo() 方法

`scrollBy()` 方法用于根据方法调用时传递的参数像素数滚动窗口。`scrollTo()` 方法用于将窗口滚动到特定的目标。其语法和用法与其他之前提到的方法相同，并将根据提供的参数数字来滚动新窗口。

## 处理图像

JavaScript 使用对象来预加载图像、创建轮播效果，甚至可以创建幻灯片或动画。当你想要创建此类脚本时，图像对象的属性将非常有帮助。表 14-4 列出并描述了图像对象的属性。

| 属性 | 用途 |
|---|---|
| name | 存储来自 name 属性的图像名称 |
| src | 存储来自 src 属性的 URL 值 |
| width | 存储来自 width 属性的宽度值 |
| height | 存储来自 height 属性的高度值 |
| complete | 表明图像是否完成加载 |

**表 14-4** 图像对象的属性

## 翻滚（Rollovers）

图像翻滚（也称为悬停按钮、图像翻转和其他类似名称）可以为你的导航图像增添趣味。随着浏览器和 CSS 的最新进展，现在通常通过 CSS 而不是 JavaScript 来实现。你可以在 https://www.kirupa.com/css/css_rollovers.htm 查看此示例。这是让翻滚更具可用性的常用方法。

### 简单的 JavaScript 翻滚

简单的翻滚是在鼠标移动到初始图像上时将一张图像变为另一张。首先，你创建两个图像，并让第二张图像在某些方面不同。

### 注意

对于你创建的每个 JavaScript 翻滚效果，你都需要两个独立的图像。

一旦你有了两张图像，就可以开始编写图像翻滚的代码了。你可以将初始图像编码到你的 HTML 文档中，并给它分配一个 id：

```html
<h1>下方的图像会变化：将鼠标悬停在它上面！</h1>
<img src="image.gif" id="pic" border="0">
```

在你的 JavaScript 代码中，你需要根据 id 获取元素，并在 `mouseover` 事件中为它的 `src` 属性分配一个新值。然后只需在 `mouseout` 事件中将其改回。以下是 JavaScript 代码：

```javascript
let im = document.getElementById("pic");
im.addEventListener("mouseover", function() {
im.src = "image2.gif";
}, false);
im.addEventListener("mouseout", function() {
im.src = "image.gif";
}, false);
```

## JavaScript 与框架（Frames）

是否在你的网站上使用框架取决于你。然而，应该注意框架的无障碍/易用性问题。事实上，`<frameset>` 和 `<frame>` 在 HTML5 中已不再有效。`<iframe>` 元素（内联框架）仍然可用。

框架将窗口划分为两个或更多独立区域（框架集），每个区域包含不同的内容。这与表格的不同之处在于，框架集中的划分包含一个独立的超文本标记语言（HTML）文档，你可以更改其中一个部分而不影响其他部分。

> 注意
> 网页上显示的每个框架实际上都是一个独立的 HTML 文档。

例如，图 14-12 显示了一个带有两个框架的网页。每个框架实际上都是一个独立的 HTML 文档。创建框架的 HTML 文档使用一组 `<frameset>` 和 `</frameset>` 标签来创建一个框架集。

### 访问框架

如何在 JavaScript 中访问框架？你可以直接使用框架，也可以为框架命名并改用框架名称。首先，我们来看框架。

现在，你可以让第二个框架的代码访问第一个框架中所需的信息。以下是用于第一个框架的代码（`frame1.html`）：

```html
<body>
我是框架 1，另一个框架从我这里获取了信息。真无礼！
</body>
```

为了完成此脚本，你可以使用 `frame2.html` 的代码：

```html
<body>左侧框架的位置值
<br>
<script type="text/javascript">
document.write(top.frames[0].location); // 访问框架中的信息
</script>
</body>
```

### 框架名称

另一种从一个访问另一个的方法是使用框架名称（就像你在上一章中使用框架的方式一样）。例如，此代码通过在框架标签中添加名称为每个框架命名（将此称为 `frame3.html`）：

```html
<html>
<frameset cols="50%,50%">
<frame src="frame1.html" name="left_side"></frame>
<frame src="frame2.html" name="right_side"></frame>
</frameset>
<noframes>
使用下面的链接进入无框架版本的网站。<br /> <a href="noframes.html">无框架站点</a>
</noframes>
</html>
```

你现在可以使用框架名称而不是框架数组来访问其他框架中的某一个。因此，如果你想从第一个框架访问第二个框架（`right_side`），可以使用此语法：

```javascript
top.right_side
```

同样地，你也可以使用此语法从第二个框架内部访问第一个框架：

```javascript
top.left_side
```

现在，你可以通过在每个框架中编写短短的 `document.write()` 语句对框架进行编码，让每个框架告诉观众另一个框架的位置。第一个框架（`frame1.html`）的代码可以这样写：

```html
<body>
第二个（右侧）框架源于：<br>
<script type="text/javascript">
document.write(top.right_side.location);
</script>
</body>
```

右侧框架的名称被用于在左侧框架中打印来自它的信息。之后，`frame2.html` 的代码可以这样写：

```html
<body>
第一个（左侧）框架源于：<br />
<script type="text/javascript">
document.write(top.left_side.location);
</script>
</body>
```

左侧框架的名称被用于在右侧框架中打印来自它的信息。现在每个框架都提供了关于另一个框架的信息。

### 注意

框架（Frames）和内联框架（iframes）在使用存在潜在的安全风险，例如跨框架脚本。更多关于这些风险的信息，请参阅：https://www.owasp.org/index.php?Cross_Frame_Scripting。

## 跳出框架

有时另一个网站使用的链接在到达你的网站之前可能会跳出该网站的框架。你的网站将留在观众窗口的较小部分，而来自另一个网站的导航位于其他框架中。当这种情况发生时，你可能想为观众提供跳出另一个网站框架的方法。

你可以在页面上放置一个链接让观众跳出框架。你需要在 `<a>` 标签中添加特殊的标记，如下：

```html
<a href="http://yoursite.com" target="_top">跳出框架</a>
```

`_top` 目标告诉浏览器在打开链接中的 URL 时使用全窗口，而不是在框架内打开链接。你只需要将标签中的 URL 替换为你自己的即可。

## 使用 iFrames

iframe 是嵌入在你的文档主窗口中的单个框架。如果需要，你可以有多个 iframe。你可以做的一件事是将另一个网页嵌入到当前页面中。例如，如果你想将像 stackoverflow 这样的讨论网站嵌入到主文档中，你可以采取操作：

```html
<iframe src="https://stackoverflow.com/" frameborder="2"></iframe>
```

当然，如果你希望它看起来无缝的，可以将 frame-border 设置为 0。如果你选择嵌入 iframe 音频或视频文件，可能会出现这种情况。使用 iframe 的一些示例可以在 https://ilovecoding.org/lessons/embeds-video-audio-and-iframe-elements 找到。

## 第 14 章自测

1. 每个浏览器窗口都会创建一个（对象）。
2. `closed` 属性用于检查窗口是否已关闭。
   - A. 正确
   - B. 错误
3. 该属性返回窗口内框架的数量。
4. `location` 属性可以导致浏览器立即重定向到新页面。
   - A. 正确
   - B. 错误
5. 该属性持有当前窗口的名称，并允许你为窗口命名。
6. 对窗口对象的属性和方法的调用通常可以通过以下方式缩短：
   - A. window 对象是浏览器中 JavaScript 的全局对象。
   - B. window 属性和方法被假设为 navigator 对象的一部分。
   - C. 真的没有 window 对象。
   - D. 浏览器假设 window 对象是 document 对象的一部分。
7. `self` 属性是 JavaScript 中“当前窗口”的另一种表达方式。
8. 为什么这段代码不起作用：`mouseover="window.status='Page 2'; return true;"`
   - A. 它应该没有问题地工作。
   - B. 默认不允许更改窗口状态，因此用户需要更改安全设置才能使其工作。
   - C. 在 mouseover 事件中更改状态后，必须返回 false。
9. `parent` 和 `top` 属性之间的区别是什么？
   - A. `parent` 属性跳转到当前框架集的顶端，而 `top` 属性跳转到页面上所有框架集的顶部窗口。
   - B. `top` 属性跳转到当前框架集的顶端，而 `parent` 属性跳转到页面上所有框架集的顶部窗口。
   - C. `parent` 属性跳转到当前框架集的顶端，而 `top` 属性跳转到当前框架的顶部。
   - D. `parent` 属性跳转到最外层框架集的顶端，而 `top` 属性跳转到页面上所有框架集的顶部窗口。
10. 该方法向观众弹出一个消息，观众必须点击 OK 按钮才能继续。
11. 如果观众必须点击 OK 按钮，`confirm` 方法返回什么值？
    - A. true
    - B. false

# 第 15 章：JavaScript 表单与数据

## 介绍两个 length 属性

如果你想在页面有多个表单时显示每个表单的元素数量，可以使用更复杂的脚本，为页面上的每个表单打印一条消息。回想一下 `forms` 数组，你可以找到它的 `length`。

`forms` 数组的 `length` 是页面上表单的数量（同样，特定表单的 `length` 属性是表单中元素的数量）。要查找页面上表单的数量而不是表单的长度，可以使用以下代码：

```javascript
document.forms.length
```

这种语法可以页面上表单的数量。因此，你需要记住这些点：

- `document.forms.length` 获取页面上表单的数量。
- `document.forms[x]` 获取页面上某个特定表单的元素数量，其中 x 是要访问表单的索引。

这种语法看起来可能有点混乱，但请记住，一个 `length` 属性用于通用的表单，而另一个属性则用于特定的表单。

### 注意

记住 `document.forms.length` 和 `document.forms[x].length` 之间的区别。前者查找页面上表单的数量，而后者查找特定表单的元素数量（通过将 x 替换为数字）。

以下脚本使用了两个 `length` 属性，并通过循环遍历每个表单。该代码显示了页面上每个表单的元素数量。首先是 HTML 代码（保存为 `forms.html`）：

```html
<body>
<h1>Form Lengths</h1>
<h2>Form 1</h2>
<form>
<label>Name:</label><input type="text"><br>
<label>E-mail:</label><input type="text"><br>
<input type="submit" value="Submit">
</form>
<h2>Form 2</h2>
<form>
<label>Favorite Color:</label><input type="text"><br>
<label>Favorite Food:</label><input type="text"><br>
<input type="reset" value="Reset">
<input type="submit" value="Submit">
</form>
<h2>Results</h2>
<script type="text/javascript" src="lengths.js"></script>
</body>
```

接下来是 JavaScript 代码（保存为 `lengths.js`）：下面是遍历页面上所有表单的循环：

```javascript
for (let count = 0; count < document.forms.length; count++) {
  let fornum = count + 1;
  document.write("Form " + fornum + " has " + document.forms[count].length + " elements<br>");
}
```

结果被写在页面上。创建了一个变量来存储表单编号（比索引号大 1，为了用户友好）。代码在 HTML 文档中创建了两个表单。脚本启动了一个从 0 开始（数组计数的开始）的循环，并在达到 `document.forms.length` 的值之前结束，该值是页面上表单的数量。有两个表单（这将使 `document.forms.length` 的值为 2），`count` 从 0 运行到 1 然后停止。`count` 允许你访问索引为 0 和 1 的数组，这在 HTML 代码中将是 Form 1 和 Form 2。`fornum` 变量是数组中位置数字加 1 的值，即 HTML 代码中看到的表单数量。然后脚本使用 `document.write()` 语句在页面上写入每个表单的元素数量。使用 `count` 变量的值作为索引号使用表单，在每次循环中找到指定表单的元素数量。

## 使用 ID

访问表单的第三种方法是使用 `id` 属性，然后使用 `document.getElementById()`。这是访问表单及其元素最清晰的方法，因为你可以使用单独的 `id` 访问每个元素，而之前的两种访问方法需要知道它位于哪个数组索引或表单的名称。

### 注意

如果你需要复习如何使用 `getElementById()` 访问元素，可以参考第 9 章。

如果你想使用 `id` 编写上一节中的脚本，可以使用以下 HTML 代码：

```html
<form id="info_form"> 给表单赋予一个 id
Name: <input type="text"><br>
<input type="submit">
</form>
```

接下来是 JavaScript 代码：

```javascript
let f_length = document.getElementById("info_form").length;
document.write(`表单有 ${f_length} 个元素.`);
```

`getElementById()` 用于访问表单并获取其长度。命名表单中的元素数量被写在页面上。

由于你已经在之前的章节中熟悉了如何使用 `document.getElementById()`，这对你来说将是一个简单的方法。

访问表单及其元素的方法取决于你正在编写的脚本类型。如果你在页面上使用多个表单，那么数组可以是遍历每个表单的方便方法。另一方面，尝试在 XHTML 1.0 Strict 中进行验证将要求你使用 `id` 来命名每个表单，因此在这种情况下使用 `id` 方法会更合适。随着本章的进行，你将看到更多关于访问表单中元素的内容。

## 使用表单对象的属性和方法

当你需要在脚本访问表单的某些元素或属性时，JavaScript 表单对象将对帮助。表单对象只有几个属性和方法。首先描述属性。

### 属性

表单对象的属性提供了你在脚本中处理表单时可能需要的信息。表 15-1 列出了表单对象的属性及其值。

这些属性中的大多数都持有与 HTML 表单标签中各种属性相对应的值。其中少数属性具有不同类型的值，正如接所解释的那样。

| 属性 | 值 |
| --- | --- |
| acceptCharset | 表单中使用的字符集，不同于其他 |
| action | HTML 表单标签中 action 属性的值 |
| autocomplete | 定义浏览器是否可以使用自动完成功能来帮助用户填写表单 |
| elements | 包含表单中每个元素的数组 |
| encoding 或 enctype | 字符编码属性的值，随浏览器而异 |
| length | 表单中元素的总数 |
| method | HTML 表单标签中 method 属性的值 |
| name | HTML 表单标签中 name 属性的值 |
| noValidate | 当该属性存在时，指定表单不进行验证（HTML5） |
| target | HTML 表单标签中 target 属性的值 |

表 15-1 表单对象的属性

### action 属性

此属性允许你访问起始表单标签中 `action="url"` 属性的值。该属性用于将表单发送到服务器脚本进行处理（例如 Node.js 或 PHP 脚本）。下面的示例显示了如何通过命名表单访问该属性。首先是 HTML 代码：

```html
<form name="info_form" action="http://someplace.com/php/form.php">
<label>Name:</label><input type="text"><br>
<input type="submit">
</form>
```

定义了 action 属性。接下来是 JavaScript 代码：

```javascript
document.write("表单去向 " + document.info_form.action);
```

此脚本写入 action 属性中提供的 URL。

### elements 属性（数组）

`elements` 属性是一个数组，允许你按照代码中出现的顺序（从 0 开始）访问特定表单中的每个元素。它的工作方式与 `forms` 数组类似，但表单中的每个元素都有一个项目。

使用 `elements` 数组访问表单中的元素时，使用要访问元素的索引数字。例如，以下表单有两个元素：

```html
<form name="info_form">
<label>Name:</label><input type="text"><br>
<input type="submit">
</form>
```

要访问第一个元素（文本框），可以使用此处所示的语法：

```javascript
document.info_form.elements[0]
```

或者，如果你想使用 `forms` 数组（假设这是页面上的第一个表单），可以使用语法：

```javascript
document.forms[0].elements[0]
```

访问文本框的另一种选择是为其命名（就像表单一样）并使用其名称访问它。你可以对每个元素以及对表单本身这样做；你可以根据具体情况选择每种访问表单及其元素的最佳方法。

以下代码为表单和文本框赋予了名称，并允许你通过名称来访问它们：

```html
<form name="info_form">
<label>Name:</label><input type="text" name="yourname"><br>
<input type="submit">
</form>
```

在这种情况下，你可以像此处所示的语法一样，通过表单名称和文本框名称来访问文本框：

```javascript
document.info_form.yourname
```

此外，你也可以使用 `id` 方法：

```html
<form>
<label>Name:</label><input type="text" id="yourname"><br>
<input type="submit">
</form>
```

然后，你可以使用 `document.getElementById` 来访问输入元素：

```javascript
document.getElementById("yourname");
```

### encoding 属性和 enctype（实体）属性

这两个属性都包含表单标签中 `enctype` 属性的值，该值表示从表单发送到服务器的数据所使用的编码类型。默认值是 `"application/x-www-form-urlencoded"`。

### length 属性

`length` 属性持有页面上给定表单中的元素数量。本章已经较好地涵盖了这一属性，因此没有再次讨论。

### method 属性

该属性持有表单标签中 `method` 属性包含的值。因此，如果你正在将表单发送到服务器进行处理，可能会使用类似下面的代码：

```html
<form name="f1" method="post" action="http://site.com/cgi-bin/form.cgi">
<!-- 此处为表单内容 -->
</form>
```

该表单 `method` 属性的值为 `post`，因为它位于表单的 `method` 属性之中。

### name 属性

该属性持有表单名称的值，该名称是在表单标签的 `name` 属性中赋予的。你可能会有如下代码：

```html
<form name="cool_form">
<!-- 此处为表单内容 -->
</form>
```

在这里，`name` 属性的值是 `cool_form`，因为它是表单 `name` 属性内部的值。

### noValidate 属性

该属性包含表单标签中 `novalidate` 属性的布尔值（HTML5 中引入）。如果为 `true`，则在提交时不进行验证。有关 HTML5 验证的更多信息，请参阅本章中的“HTML5 与表单”。

### target 属性

该属性持有表单标签中 `target` 属性赋予的值。例如，你可能会有代码：

```html
<form name="cool_form" target="_top" action="program.cgi">
<!-- 此处为表单内容 -->
</form>
```

在这里，`target` 属性的值是 `_top`，因为它是表单 `target` 属性内部的值。

### 方法

现在来看表单对象的方法。选定的方法将在表 15-2 之后讨论。

| 方法 | 描述 |
|---|---|
| checkValidity() | 返回所有要求浏览器验证的表单元素是否都通过了验证 |
| reportValidity() | 返回元素是否根据其验证约束通过验证 |
| submit() | 提交表单 |
| reset() | 重置表单数据 |

**表 15-2** 表单对象的方法

### checkValidity() 方法

在 HTML5 中，你可以让浏览器检查字段是否包含数据或是否符合模式，这不需要 JavaScript。你可能希望执行进一步的操作；然而，这取决于所有需要验证的字段是否都通过了各自的测试。如果所有元素都符合验证要求，`checkValidity()` 函数返回 `true`，如果任何一个元素失败，则返回 `false`。关于 HTML5 如何影响表单的更多信息，可以在本章后半部分的“HTML5 与表单”章节找到。

### reset() 方法

此方法允许你从脚本重置表单，这将清除用户输入的任何数据。例如，你可以在完成输入数据的处理后使用以下代码重置表单：

```javascript
let my_form = document.getElementById("my_form");
my_form.addEventListener("submit", function (event) {
  let txt = document.getElementById("txt").value;
  alert(txt);
  event.preventDefault();
  my_form.reset();
}, false);
```

在这里，表单在对输入到文本框中的数据进行简单操作（带有告警框）后被重置。

### submit() 方法

这允许你在查看者不点击提交按钮的情况下提交表单。如果你需要提供另一种方式（提交元素之外）来提交表单，这将非常有用。下面的代码展示了这种示例。在这里，HTML 代码为：

```html
<form id="my_form" action="send_email.php">
<label>Email:</label><input type="text" id="email"><br>
<a href="submit.html" id="submit">提交</a>
</form>
```

接下来，是 JavaScript 代码：

```javascript
let my_form = document.getElementById("my_form");
let subm = document.getElementById("submit");
subm.addEventListener("click", function (event) {
  let email = document.getElementById("email").value;
  event.preventDefault();
  my_form.submit();
}, false);
```

## 确保表单的可访问性

确保你的表单具有可访问性是项挑战，因为你的表单布局可能无法被辅助技术正确解释。为了确保表单具有可访问性，你可以使用 `label` 标签，并确保你的表单具有可访问性。

在 HTML 代码中，使用正确的元素和标签可以帮助辅助技术。例如，请考虑以下字段：

```html
<input type="text" name="username"> 名称<br>
<input type="text" name="zip_code"> 邮码
```

在这里，辅助技术会查找标签。为了确保表单具有可访问性，你可以使用 `label` 标签，并确保你的表单具有可访问性。

### 使用 `<label>` 标签

使用标签可以帮助你进一步指定哪个标签属于哪个表单元素。这里有一个示例：

```html
<label>名称</label>
<input type="text" name="username" id="username">
```

在这里，标签处于预期位置，你可以简单地应用标签 `label`。如果你需要更具体地指向表单元素的 id，可以添加 `for` 属性，如下所示：

```html
<label for="username">名称</label>
<input type="text" name="username" id="username">
```

在这里，`<label>` 标签的 `for` 属性包含了 id，这将其关联到具有该 id 的元素。

### 使用 `<fieldset>` 标签

在处理单选框和复选框时，使用 `fieldset` 对于将它们组合到一个逻辑集中非常有帮助。使用 `legend` 标签来标记选项可以让用户知道预期内容。下面的代码使用 `fieldset` 将一组单选按钮组合在一起以选择水果类型：

```html
<fieldset>
<legend>选择水果：</legend>
<input type="radio" name="fruits" id="fruits1" value="Orange">
<label for="fruits1">橙子</label>
<input type="radio" name="fruits" id="fruits2" value="Banana">
<label for="fruits2">香蕉</label>
<input type="radio" name="fruits" id="fruits3" value="Apple">
<label for="fruits3">苹果</label>
</fieldset>
```

在这里，将所有的单选按钮放在 `<fieldset>` 和 `</fieldset>` 中，并在开启 `fieldset` 之后使用 `legend` 标签来分组标签。

## 不假设存在客户端脚本

在最初编写表单时，最好不要假设会有 JavaScript 或任何客户端技术可用。如果需要 JavaScript 才能使表单可用，那么许多用户将无法使用它，因为他们出于某些原因（如安全）禁用了 JavaScript。

最佳实践是允许将表单设置到服务端（由服务器处理表单并提供最重要的验证例程），即使在 JavaScript 不可用情况下也是如此。

如果你正在使用某些 JavaScript 验证，可以使用如下代码：

```html
<form method="post" action="form.php" id="my_form">
<!-- 此处为表单内容 -->
  <input type="submit" name="submit" id="submit" value="Submit Form">
</form>
```

这允许你在 JavaScript 可用时运行它（通过为服务器端创建事件监听器）。否则，JavaScript 提交事件将被忽略，表单将提交到服务器端脚本进行验证和处理。如果 JavaScript 可用，客户端验证程序可以减少与服务器的往返次数。如果不可用，服务器端脚本将无需执行此工作，但用户仍然能够按照预期使用该表单。

此外，检查表单是否被禁用是一个好主意，因为你也希望它处于可用的状态。屏幕阅读器会遵循这种布局，因此你的元素顺序需要以一种仍然具有访问性且符合使用屏幕阅读器的人员习惯排列。

## 验证

验证 JavaScript 表单非常有用。例如，你可以在提交之前对输入进行验证，以减少信息不或不准确的表单。在提交到通用网关接口（CGI）脚本、PHP 脚本或 Java servlet 之前进行表单数据验证可以节省时间并减轻服务器负载。

### 简单验证

在之前的章节（尝试此 13-1）中，你通过提交事件在表单提交时执行函数，并对输入进行测试以检查其是否包含特定字符（电子邮件地址中的 `&`），对输入进行了一些验证。你还学习了正则表达式，它在验证输入时也很有帮助。

例如，假设你有如下用于表单的 HTML 代码：

```html
<form method="post" action="form.php" id="my_form">
  <label for="username">Name:</label>
  <input type="text" name="name" id="name"><br>
  <input type="submit" name="submit" id="submit" value="Submit">
</form>
```

如果你使用 `addEventListener` 来处理提交事件，你可以阻止默认动作的发生（将表单内容发送到服务器），或者如果名称未按照指定的规则通过验证，则阻止默认动作并显示错误消息。这是一个示例：

```javascript
let my_form = document.getElementById("my_form");
my_form.addEventListener("submit", function(event) {
  let name = document.getElementById("name").value,
  tomatch = /^[A-Za-z\- ]{2,50}$/;
  if (!tomatch.test(name)) {
    event.preventDefault();
    alert("名称只能包含字母、空格、撇号和连字符");
  }
}, false);
```

正如你所见，这使用了一个正则表达式（第 13 章）来限制名称字段中允许的字符类型和数量。它使用范围 A–Z 和 a–z 来允许所有字母，允许撇号（用于如 O'Neill 这样的名字），使用 `\-` 允许连字符（连字符经过转义以避免与新范围混淆），并使用空格表示空格。然后它使用 `{2,50}` 来确保名称至少有两个字符且不超过 50 个字符。`^` 和 `$` 用于使字符串从头到尾匹配，而不是在匹配第一个有效字符后停止。如果名称未通过验证，表单将不会提交（`event.preventDefault()` 停止提交），并向用户发送警报。否则，表单将正常提交到服务器进行服务器端处理。

### 技术

在大多数情况下，验证可以根据你的需求变得简单或复杂。你只需要根据所需的信息创建自己的自定义函数，来对你选择的表单字段进行验证。

例如，你可以使用正则表达式检查某个字段是否包含五个数字（用于典型的邮政编码）。如果不是，你可以发送一个警报，告知邮政编码无效并要求重新输入。以下代码展示了实现此方法。首先是 HTML 代码：

```html
<form method="post" action="form.php" id="my_form">
  <label for="zip_code">Zip Code:</label>
  <input type="text" name="zip_code" id="zip_code"><br><br>
  <input type="submit" name="submit" id="submit" value="Submit">
</form>
```

接下来是 JavaScript 代码：

```javascript
let my_form = document.getElementById("my_form");
my_form.addEventListener("submit", function(event) {
  let zip = document.getElementById("zip_code").value;
  tomatch = /^\d{5}$/;
  if (!tomatch.test(zip)) {
    event.preventDefault();
    alert("邮政编码必须包含 5 位数字");
  }
}, false);
```

该代码使用正则表达式来检查五个数字。如果输入了五个数字以外的任何内容，函数将返回 `false`。当然，你可以扩展它允许额外的四个数字，这些数字有时用于更精确地指定邮政编码内的特定区域。要这样做，添加另一个输入字段，并要求如果在第二个字段中输入了值，则必须是四个数字。

这里需要提到的一点是，验证应该在客户端和服务器端同时进行。虽然客户端验证很有帮助可以减轻服务器压力，但由于客户端验证很容易被绕过，如果没有服务器端验证，可能会产生巨大的安全风险。

## 复选框与单选按钮

在使用复选框和单选按钮时，你可能想知道它们是否被勾选。例如，假设你有如下代码：

```html
<form id="signup_form">
  <label for="email">Email:</label>
  <input type="text" name="email" id="email"><br>
  选择你的食物:<br>
  <input type="radio" name="food" id="food_pizza" value="Pizza">
  <label for="food_pizza">Pizza</label>
  <input type="radio" name="food" id="food_sandwich" value="Sandwich">
  <label for="food_sandwich">Sandwich</label>
  <input type="radio" name="food" id="food_candy" value="Candy">
  <label for="food_candy">Candy</label>
  <input type="submit" name="submit" id="submit" value="Submit">
</form>
```

在这种情况下，你想确保用户勾选了条款。你可以使用以下代码：

```javascript
let s_form = document.getElementById("signup_form");
s_form.addEventListener("submit", function(event) {
  let agree = document.getElementById("agree");
  if (!agree.checked) {
    event.preventDefault();
    alert('错误：必须勾选条款');
  }
}, false);
```

验证复选框的一种方法是通过 `checked` 属性。你可以根据需要让验证变得严格或宽松。你将在第 16 章看到更多关于这些的问题。如果你正在处理一组单选按钮并想确保至少选择了其中一个，可以使用以下代码：

```javascript
let s_form = document.getElementById("signup_form");
s_form.addEventListener("submit", function(event) {
  let food_array = document.getElementsByName("food"),
  selection_made = false;
  for (let i = 0; i < food_array.length; i++) {
    if (food_array[i].checked) {
      selection_made = true;
      break;
    }
  }
  if (!selection_made) {
    event.preventDefault();
    alert('错误：必须选择一种喜欢的食物');
  }
}, false);
```

在这里，每个 `name` 属性值为 `"food"` 的单选按钮元素都被放置在 `food_array` 中。这允许你使用循环来遍历每个单选按钮，检查它是否被选中。布尔变量 `selection_made` 初始设置为 `false`。在循环内部，如果脚本发现某个单选按钮被选中，它将把 `selection_made` 设置为 `true` 并使用 `break` 语句退出循环。由于只能选中一个单选按钮——在找到正面结果后，你不需要继续检查了。如果运行循环后 `selection_made` 仍然为 `false`，则取消表单提交，用户将收到错误提示框。

## 尝试此练习 15-1 请求一个数字

在这个项目中，你将创建一个脚本，用于对观众输入的电话号码进行基本验证，例如 222-222-2222。

### 逐步步骤

1. 创建一个 HTML 页面，包含一个表单和一个文本框，标签文本为“Phone Number (XXX-XXX-XXXX)”且 `id` 为“phone”。确保表单有一个提交按钮。在表单之后插入必要的脚本标签，用以调用命名为 `prjs14_1.js` 的外部 JavaScript 文件。将 HTML 文件保存为 `pr14_1.html`。完成后，HTML 代码应该像这样：

```html
<body>
<form id="getphone">
<label for="phone">Phone Number (XXX-XXX-XXXX):</label>
<input type="text" id="phone"><br><br>
<input type="submit" value="Submit">
</form>
<script type="javascript" src="prjs14_1.js"></script>
</body>
```

2. 创建一个外部 JavaScript 文件并保存为 `prjs14_1.js`。在第 3 步中使用它。
3. 使用正则表达式来确保输入文本框中的数据符合 XXX-XXX-XXXX 格式。如果是，则发送显示“Phone number validated.”的提示；否则，发送显示“Invalid phone number entered. Valid format is XXX-XXX-XXXX.”。完成后，JavaScript 代码应该像这样：

```javascript
let getphone = document.getElementById("getphone");
getphone.addEventListener("submit", function(event) {
let phone = document.getElementById("phone").value,
tomatch = /^\d{3}-\d{3}-\d{4}$/;
event.preventDefault();
if (tomatch.test(phone)) {
alert("Phone number validated.");
}
else {
alert("Invalid phone number entered. Valid format is XXX-XXX-XXXX.");
}
}, false);
```

4. 保存 JavaScript 文件并在浏览器中打开 HTML 文件。通过在文本框中输入各种值并提交表单，查看它是否正常工作。

### 尝试此练习总结

在这个项目中，你利用 JavaScript 和表单的知识创建了一个用于验证表单的脚本。该脚本验证观众输入的时间项，以检查其是否符合特定组标准的有效电话号码。

## HTML5 和表单

HTML5 提供了多个元素，以及许多新的输入类型和属性。它还提供了一种浏览器在客户端对字段进行验证的方法，减轻了支持这些特性的浏览器中 JavaScript 的负担。

### 新元素

HTML5 中的新元素列在表 15-3 中。这些元素允许向观众提供额外信息或执行其他有用的任务。你将在本节查看 `meter` 和 `progress` 元素，但关于这些任何元素的更多细节（包括哪些浏览器支持每一个），请参见 woofoo /html5/。

### meter 元素

`meter` 元素用于根据定义的刻度显示值。例如，如果你决定使用 0–100 的刻度，你会给 `min` 属性赋值。

通过仪表，你可以使用 `max` 属性设置最大值，并使用 `value` 属性在 0 到 `max` 值之间的范围内设置百分比值。如果需要，你可以编辑之前的 JavaScript 代码，使用进度条来显示测验的百分比分数，可以使用以下代码：

```javascript
let qform = document.getElementById('qform');
qs = [document.getElementById('q1'), document.getElementById('q2'),
document.getElementById('q3')];
ans = [4, 2550, 4958];
grade = document.getElementById('grade');
qform.addEventListener('submit', function (event) {
  let num_correct = 0;
  num_questions = qs.length;
  grade_HTML = "";
  score = 0;
  event.preventDefault();
  for (let i = 0; i<num_questions; i++) {
    if (+qs[i].value == ans[i]) {
      num_correct++;
    }
  }
  score = Math.round(num_correct / num_questions * 100);
  grade_HTML = '<progress value=' + score + '>';
  grade_HTML += '</progress>';
  grade_HTML += ' Grade: ' + score + ' %';
  grade.innerHTML = grade_HTML;
}, false);
```

- 添加了一个新的名为 score 的变量来计算分数
- 分数根据问题的数量和正确答案数量计算，并四舍五入到小数
- 显示 `progress` 元素而不是 `meter` 元素，显示百分比分数

在这里，对代码进行了修改以计算将用于 `input` 元素的百分比分数。然后根据百分比分数生成 `progress` 元素。

### 新的输入类型

除了新元素外，HTML5 还增加了许多新的输入类型，这些类型可以用于 `input` 元素。表 15-4 列出了这些选项。

你会发现，其中一些输入类型允许用户使用工具，例如 `color` 输入类型。浏览器可能会以不同的方式实现这些类型，但支持一种或多种新类型的浏览器使用户更容易输入每种特定类型的值和/或使值更容易验证。使用新 `color` 类型的示例代码下所示：

```html
<input type="color" name="mycolor" id="mycolor">
```

如所示，你可以在 `type` 属性中插入特定类型来使用它。由于这些字段是用于特定类型值的，浏览器能够对字段进行自身的验证，这在得到支持时非常有帮助。

| 类型 | 描述 |
| --- | --- |
| color | 允许用户使用颜色工具选择颜色 |
| date | 可以使用日期或日历工具输入日期 |
| datetime | 可以使用日期或日历工具输入日期/时间；时区设置为 UTC |
| datetime-local | 可以不带时区的日期/时间 |
| email | 设计用于输入一个或多个电子邮件地址 |
| month | 可以输入年份和月份的日期；无时区 |
| number | 设计用于数值输入 |
| range | 允许一个范围，用户可以使用范围工具选择一个值 |
| search | 设计用于输入将放入搜索的值 |
| tel | 设计用于输入电话号码 |
| time | 允许用户输入带有小时、分钟、秒和分数秒的值；无时区 |
| url | 设计用于输入 URL |
| week | 用于输入周；无时区。 |

**表 15-4** HTML5 中的新输入类型

### 新属性

除了新元素外，HTML5 还增加了许多新的属性，这些属性可以用于 `input` 元素。表 15-5 列出了这些选项。

| 属性 | 描述 |
|---|---|
| autocomplete | 可以设置在 `form` 标签中（影响所有表单字段）或任何特定的 `input` 标签内（影响单个字段）。如果值设置为 "off"，则字段将不会使用浏览器的自动完成功能来提供字段完成的建议 |
| autofocus | 告诉浏览器在页面加载时聚焦于该元素 |
| dirname | 提交一个带有元素的输入方向指示 |
| pattern | 提交一个带有元素的输入方向指示 |
| placeholder | 提交一个带有元素的输入方向指示 |
| required | 提交一个带有元素的输入方向指示 |

**表 15-5** 新输入类型

## 尝试练习 15-2 使用 HTML5 或 JavaScript 验证电话号码

在这个项目中，你将在此前项目的基础上，创建一个表单，使用新的 HTML5 `pattern` 属性来验证电话号码。如果浏览器不支持 HTML5，则运行备用的 JavaScript 验证。

### 逐步详解

1. 创建一个 HTML 文档并添加 `script` 标签，以便 HTML 文件能够调用名为 `prjs14_2.js` 的 JavaScript 文件。创建一个 `id="getphone"` 的表单，并添加一个 `id="phone"` 的文本框以获取电话号码。该文本框应使用 `pattern` 属性并配合正则表达式，如果格式为 XXX-XXX-XXXX 则将对电话号码进行验证。它还应该一个必填字段。确保表单包含一个提交按钮。将 HTML 文件保存为 `pr14_2.html`。完成后，HTML 代码应该如下：

```html
<body>
<form id="getphone">
  <label for="phone">Phone Number (XXX-XXX-XXXX):</label>
  <input type="text" id="phone" pattern="\d{3}-\d{3}-\d{4}$" required><br>
  <input type="submit" value="Submit">
</form>
<script type="text/javascript" src="prjs14_2.js"></script>
</body>
```

2. 创建一个 JavaScript 文件并保存为 `prjs14_2.js`。在第 3 中使用它。
3. 创建一个脚本，在表单提交时备份 HTML5 验证。如果字段未通过验证，发送一个警框显示“Invalid phone number entered. Valid format is XXX-XXX-XXXX.”。否则允许提交电话。完成后，JavaScript 代码应该如下：

```javascript
let getphone = document.getElementById("getphone");
getphone.addEventListener("submit", function(event) {
  let phone = document.getElementById("phone").value;
  let pattern = /\d{3}-\d{3}-\d{4}$/;
  if (!pattern.test(phone)) {
    alert("Invalid phone number entered. Valid format is XXX-XXX-XXXX.");
    event.preventDefault();
  }
}, false);
```

4. 保存 JavaScript 文件并在浏览器中打开 HTML 文件。检查验证系统是否工作正常。

### 尝试练习总结

在这个项目中，你利用对 JavaScript 和 HTML5 表单的知识创建了一个验证系统，该系统在 HTML5 中检查有效的电话号码，并使用 JavaScript 代码对验证进行备份。

## AJAX 和 JSON

AJAX 提供了一种使用 `XMLHttpRequest` 对象从服务器端脚本获取数据的方法。获取的数据可以通过 `JSON` 返回为可用的 JavaScript 值，例如数组或对象。这两者都将在接下来的章节中进行详细解释。

### AJAX

AJAX 代表异步 JavaScript 和 XML（Asynchronous JavaScript and XML），它是 JavaScript 在无需重新加载页面的情况下，从服务器端文件或应用程序获取数据的方法。例如，向 Web 服务器发送同步请求需要重新加载当前页面才能使用新信息。而异步请求允许在不需要等待整个页面重新加载的情况下获取并使用信息。

从服务器获取的数据可以是任何内容（例如，文本文件、XML 文件、运行服务器端脚本的执行结果）。尽管使用了 AJAX 术语，但返回的值实际上并不是 XML 格式。这让你在检索所需数据时具有很大的灵活性。

这种类型的脚本在渐进式增强中非常有用，因为它允许应用程序为现代浏览器中启用了 JavaScript 的用户增强用户体验。与其等待页面加载信息，不如实时获取并使用信息。

### XMLHttpRequest 对象

在 JavaScript 中，会创建一个 `XMLHttpRequest` 对象，然后可以使用它在后台向服务器发送 HTTP 请求，并允许用户不中断地继续使用应用程序。该对象在文中通常被简写为 `XHR`，作为完整对象名称（XMLHttpRequest）的缩写。

要创建一个 XHR 对象，你只需要使用它的构造函数，如下代码所示：

```javascript
let xhr = new XMLHttpRequest();
```

该对象在大多数现代浏览器中都是可用的。在版本 7 之前的 Internet Explorer 中，你需要创建一个 ActiveX 对象。早期版本 Internet Explorer 的解决方法可以在网上找到，例如在 github.com/ilinsky/xmlhtt。如果你不需要旧版浏览器中的该功能，可以使用标准的构造函数。

### open() 和 send() 方法

`open()` 方法允许你准备要发送到服务器的请求。它接受三个参数：请求方法（例如 `"get"` 或 `"post"`）、要打开的 URL 以及一个布尔值（如果请求是异步的则为 true，如果是同步的为 false）。因此，要使用 `"get"` 方法作为异步请求打开名为 `get_info.php` 的 PHP 脚本，可以使用以下代码：

```javascript
let xhr = new XMLHttpRequest();
xhr.open("get", "get_info.php", true);
```

现在请求已准备就绪，可以使用 `send()` 方法发送它。`send()` 方法接受一个参数，即作为请求一部分发送的数据。如果你正在使用 `"get"` 请求，可以直接使用 `null` 作为参数，如下代码所示：

```javascript
let xhr = new XMLHttpRequest();
xhr.open("get", "get_info.php", true);
xhr.send(null);
```

这将把请求发送到服务器。一旦请求发送，你将需要等待状态返回以及通过传输接收数据。

### status 属性、onreadystatechange 事件和 responseText 属性

在尝试从服务器检索数据时，你首先需要知道请求是否收到了服务器的有效响应。这可以通过 `status` 属性来确定。基本上，200 范围内的任何状态码都是成功的响应。此外，状态码 304 也是成功的，因为数据可以从浏览器缓存获取。

要查看返回的数据，可以使用 `responseText` 属性（如果使用 MIME 类型 `"text/xml"` 或 `"application/xml"`，可以使用 `responseXML` 属性）。`get_info.php` PHP 脚本预计返回字符串数据，那么这些数据将通过 `responseText` 属性可用。

最后，对于异步请求，你将能够确定你尝试检索的数据何时可以使用。这是通过使用 `onreadystatechange` 事件实现的。`readyState` 具有以下值：

- 0: 未初始化。
- 1: 已打开。
- 2: 已发送。
- 3: 接收中。
- 4: 完成。

每当 `readyState` 变化时，`onreadystatechange` 事件就会被触发。为了处理这种情况，你可以为事件分配一个函数：

```javascript
xhr.onreadystatechange = function() {
  if (xhr.readyState == 4) {
    if (xhr.status === 200) {
      alert(xhr.responseText);
    }
  }
};
```

在这种情况下，表单的 action 将是一个独立的 PHP 脚本，在 JavaScript 不可用时会运行。如果可以使用 JavaScript，你将在 AJAX 代码中调用名为 `get_winner.php` 的脚本。`get_winner.php` 是一个返回数据的服务端应用程序。这可能源于数据库查询、计算或服务端应用程序可以执行的任何任务。在这种情况下，脚本会将你的选票添加到数据库，并查询票数最多的人，宣布该人为投票的获胜者。服务器端编程超出了本书的范围，`get_winner.php` 脚本将被简化以描述其目的。以下是该脚本：

```php
<?php
function get_winner() {
  // 用于添加新投票并从数据库获取当前获胜者的代码
  $winner = get_winner();
  echo "<p>The current winner is $winner!</p>";
}
```

这里有一个从数据库确定 `$winner` 变量值的函数。`echo` 命令将文本字符串作为响应。如果作为独立脚本运行，该字符串将直接写入浏览器窗口。然而，在响应 XHR 请求时，此字符串将作为 `responseObject` 的值返回给 JavaScript 应用程序。你现在可以在 JavaScript 中利用服务端应用程序返回的数据了！

### 注意

当你使用服务端应用程序返回数据时，它不需要用 PHP 编写。根据你的背景和服务器设置，可以使用任何服务端语言（例如 Perl、ASP、Python、Java、Node.js）。

考虑到这一点，剩余的大部分工作将在你的 JavaScript 代码中完成。由于你想显示当前获胜者，`responseObject` 返回的值将为你提供所需的数据。以下是获取并使用来自 `get_winner.php` 脚本的信息的 JavaScript 代码：

```javascript
let poll = document.getElementById("poll");
if (typeof XMLHttpRequest == "undefined") {
  poll.addEventListener("submit", function(event) {
    let vote_fields = document.getElementsByName("winner");
    res_field = document.getElementById("results");
    vote = "";
    count = 0;
    xhr = new XMLHttpRequest();
    ustring = "";
    event.preventDefault();
    for (let i = 0; i < vote_fields.length; i++) {
      if (vote_fields[i].checked) {
        vote = vote_fields[i].value;
        break;
      }
      else {
        count++;
      }
    }
    if (count === vote_fields.length) {
      alert("You must make a selection to vote!");
      return;
    }
    ustring = "get_winner.php?vote=" + encodeURIComponent(vote);
    xhr.onreadystatechange = function () {
      let results;
      if (xhr.readyState === 4) {
        if ((xhr.status >= 200 && xhr.status < 300) || (xhr.status === 304)) {
          res_field.innerHTML = xhr.responseText;
        }
      }
      return false;
    };
    xhr.open("get", ustring, true);
    xhr.send(null);
  });
}
```

- 创建 `xhr` 变量
- 定义了字符串变量 `ustring`，它将用于构建作为请求一部分发送的 URL
- 防止了默认操作（提交表单）
- 遍历单选按钮值以确定是否已选中；如果是，则获取值；如果否，向查看者弹出错误消息
- 当 `readyState` 改变时运行的函数；这获取 `responseText` 并将其显示在结果 `div` 中

这看起来是一个很长的过程，但大部分工作是在提交前准备用户的选票等。这获取了信息（检查是否已做出选择并将其存储在变量中）。该变量随后被用作查询字符串的一部分在调用 `get_winner.php` 时添加到 URL 中。例如，如果用户投票给了 "Paul"，那么发送到服务器的 URL 将是 `"get_winner.php?vote=Paul"`。注意使用 `encodeURIComponent()` 方法对值进行编码，这确保了该值可以是有效的 URL。这将为 PHP 脚本提供其添加到数据库所需的数据。记住你在本章中学到的知识来获取数据（投票的当前获胜者）。由于数据已经是所需的格式，`results innerHTML` 被更新以显示当前投票胜利者。

一旦你有了 XHR 对象，就可以通过 `send()` 方法发送 `j_data` 变量。请注意，如果你将数据转换为 JSON 格式，你还必须使用 `post` 方法并设置 `xhr.setRequestHeader("Content-Type", "application/json");`。

在接收 JSON 数据时，你会使用 `JSON.parse()` 方法将数据从 JSON 格式转换为可用的值。例如，假设你正在 JavaScript 中接收到以下 JSON 数据：

```json
{ "num": 77, "color": "red" }
```

如果这段 JSON 数据被读取到名为 `xhr` 的 XHR 对象的 `responseText` 中，你可以通过以下代码将此数据转换为可用的 JavaScript 对象：

```javascript
let info = JSON.parse(xhr.responseText);
```

现在对象已经创建了，这与你编写以下代码是相同的：

```javascript
let info = { num: 77, color: "red" };
```

凭借这种快速将数据转换为可用 JavaScript 值的能力，JSON 可以让 AJAX 脚本的数据收集和使用变得简单得多。

### AJAX 与 JSON 示例

假设你想更改本章早期的 AJAX 脚本，该脚本之前显示投票的当前获胜者。你想显示所有当前结果。记住，如果没有 JSON，你需要从服务器端应用程序回传并解析一个名称/值字符串或 XML 文档。有了 JSON，你只需要以 JSON 格式回传数据，然后你可以快速使用 `parse()` 方法让它可用。

在这里，你将使用相同的 HTML 代码、一个名为 `get_results.php` 的 PHP 脚本，并修改你的 PHP 脚本以使用 JSON 数据。首先，你把数据添加到数据库中，然后从数据库检索当前结果，然后以 JSON 格式将结果发送给 JavaScript。以下是示例：

```php
<?php
function get_winner() {
// 添加新获胜者并从数据库获取名称和总数的代码
}
$results_array = get_winner();
echo "{";
foreach ($results_array as $key => $value) {
    echo "\"$key\": " . $value . ",";
}
echo "}";
?>
```

总结来说，这将向你的 JavaScript 应用程序返回 JSON 数据（在这里构建了 JSON 字符串，PHP 也有将 PHP 对象转换为 JSON 的方法），它可能如下：

```json
{ "John": 2, "Nick": 35, "Doug": 32, "Paul": 25 }
```

你现在可以修改 JavaScript 代码来显示投票中每个人的姓名和票数。以下是更新后的 JavaScript 代码：

```javascript
let poll = document.getElementById("poll");
if (typeof XMLHttpRequest == "undefined") {
  poll.addEventListener("submit", function(event) {
    let vote_fields = document.getElementsByName("winner");
    res_field = document.getElementById("results");
    res_HTML = "";
    vote = 0;
    count = 0;
    xhr = new XMLHttpRequest();
    qstring = "";
    event.preventDefault();
    for (let i = 0; i < vote_fields.length; i++) {
      if (vote_fields[i].checked) {
        vote = vote_fields[i].value;
        break;
      }
    }
    if (count == vote_fields.length) {
      alert("You must make a selection to vote!");
      return;
    }
    qstring += "?get_results.php?vote=" + encodeURI(vote);
    xhr.onreadystatechange = function () {
      let results;
      if (xhr.status == 200 && xhr.status < 300) {
        results = JSON.parse(xhr.responseText);
        res_HTML = "<h3>Results</h3>";
        for (let prop in results) {
          if (results.hasOwnProperty(prop)) {
            res_HTML += prop + ' : ' + results[prop] + '<br>';
          }
        }
        res_field.innerHTML = res_HTML;
      }
    };
    xhr.open("get", qstring, true);
    xhr.send(null);
  });
}
```

响应包含使用 `JSON.parse` 方法解析的 JSON 数据：

- 在 `for-in` 循环中检查确保每个属性都在结果对象内部
- 每个属性和值都被添加到 `res_HTML` 变量中，以便在页面上显示
- 一旦 `res_HTML` 变量拥有所有必要数据，它就会被赋值给结果显示部分的 `innerHTML`，从而在页面上显示结果

在这里，你可以解析 `responseText` 以获取可用的 JavaScript。`for` 循环遍历每个属性，这些属性是投票中每个人的姓名。然后，属性名和值被添加到名为 `res_HTML` 的变量中，并作为 HTML 页面上 `div` 的 `innerHTML` 显示。凭借易于使用从服务器端应用程序获取的数据的能力，你可以增强脚本，为用户提供更多选项，而无需重新加载整个页面。

### 进阶阅读

关于 JSON 的更多信息可以参考以下内容：

- www.json.org/
- https://developer.mozilla.org/en-US/docs/JSON

## 第 15 章测试

1. 每当你向 HTML 文档中添加一组 `<form>` 和 `</form>` 标签时，就会创建一个对象。
2. 表单允许你访问...
3. 哪一个在页面上访问...
4. 哪一个在页面上访问...
5. 哪一个在 HTML 文档中添加...
6. 使用哪一个 HTML 标签来...
7. 哪一个在页面上访问...
8. 哪一个属性允许...
9. 使用哪一个 HTML 标签来...
10. 哪一个 HTML 属性用于...
11. 使用哪一个方法允许...
12. 哪一个在页面上访问...
13. 使用哪一个 HTML 标签来...
14. 哪一个方法允许...
15. 哪一个 HTML 属性用于...
16. 哪一个对象可以从服务器获取数据？
17. ________ 代表 JavaScript 和 XML。
18. JavaScript 可以从 XML 文档获取数据。
19. ________ 是

# 第 16 章：进阶浏览器端 JavaScript

## 技能与概念

- 使用 jQuery
- 调试脚本
- JavaScript 无障碍性
- JavaScript 安全
- JavaScript 与 HTML5
- Node.js 应用完成

本章介绍了一些你在完成本书后可能希望进一步学习的技术。首先，你将接触 jQuery，这是一个用于创建跨浏览器脚本的良好 JavaScript 库。你还将学习 JavaScript 无障碍性和安全性、JavaScript 如何整合到 HTML5，并完成你的基础 Node.js 应用。

## 入门：document.ready()

jQuery 首先需要确保所有的 DOM 元素都已用于脚本。`document.ready()` 方法确定 DOM 结构何时加载完成，然后运行其中的代码，通常如下所示：

```javascript
$(document).ready(function() {
  // 在此处编写 jQuery 代码...
});
```

这段代码被放置在你的普通 JavaScript 代码中（例如，你的 .js 文件）。注意代码开头的 `$`。这是 jQuery 选择器，用于在你调用 jQuery JavaScript 时使用。

## 使用选择器

在 jQuery 中，你可以通过 CSS 语法来选择元素，而不是使用典型的 JavaScript 方法如 `document.getElementById` 或 `document.getElementsByClassName()`。例如，假设你有如下代码：

```javascript
let story = document.getElementById("story")
story.addEventListener("click", function() {
story.style.color = "#009"
story.style.fontSize = "2em"
}, false);
```

这只是改变了几个 CSS 样式属性，但需要几行代码才能实现。在 jQuery 中，`.click(function())` 可以简写为：

```javascript
$("#story").css({'color':'#009', 'font-size':'2em'});
```

首先，你会发现 "story" 是通过 CSS 语法 (`"#story"`) 选择的，而不是 `document.getElementById("story")`。这使得选择变得更短。此外，你会发现事件处理相对于事件名称非常简单（在本例中为 "click"），后面跟着事件发生时执行的函数。这让你不再需要编写跨浏览器的事件处理程序。接下来，你可以通过对 story 元素使用 `css()` 方法来更改元素的 CSS。`css()` 方法接受一个对象作为参数，它包含了每个要更改的属性及其新值（都用引号括，类似于 JSON 语法）。通过这种方式，你不需要为每个想要更改的 CSS 属性编写单独的语句。

为了看到此示例的运行效果，你需要创建一个带有 "story" div 的 HTML 页面，代码如下：

```html
<body>
<div id="story">
这是我的故事。里面有很多有趣的内容，供你有空时阅读。
我可以一直写下去，一直下去……
</div>
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
<script src="jexample.js" type="javascript"></script>
</body>
```

如果你使用的是本地的 jQuery，可以在此处调用它代替 Google 版本。你可以将此 HTML 页面保存为 `jexample.html`。接下来，你想创建一个 JavaScript 文件，并将其保存为 `jexample.js`。代码如下：

```javascript
$(document).ready(function () {
  $("#story").click(function () {
    $("#story").css({'color':'#0099', 'font-size':'2em'});
  });
});
```

"story" div 的某些 CSS 属性被改变了。调用了一个函数来处理 "story" div 上的点击事件。

一旦代码就绪，在浏览器中打开 `jexample.html` 并点击该 div 元素。文字应该变大并变蓝。

jQuery 提供了许多选择器来帮助你在脚本中选择所需的元素。以下是一些最常见的：

- `*` 选择文档中的所有元素
- `.class_name` 选择所有具有所提供类名的元素
- `#id` 选择具有所提供 id 的元素
- `element_name` 选择所有 element_name 元素
- `element_name.class` 选择具有 class_name 类的 element_name 元素
- `element_name[attribute="value"]` 选择所有具有所提供属性值的 element_name 元素

如果需要，可以在 api.jquery.com/category/selectors 找到更多选择选项。

> 注意
> 在原生 JavaScript 中，`document.querySelectorAll` 的工作方式与 jQuery 选择器函数类似。

## 修改类

`addClass()` 函数使得在 jQuery 中更改元素样式变得非常简单。如果你已经在 CSS 中编写了代码，可以使用这些方法来更改它们。例如，假设你有如下名为 `jexample.html` 的 HTML 文件：

```html
<head>
<link rel="stylesheet" href="jexample.css">
</head>
<body>
<div id="story">
这是我的故事。里面有很多有趣的内容，供你有空时阅读。
我可以一直写下去，一直下去……
</div>
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
<script src="jexample.js" type="javascript"></script>
</body>
```

以及 CSS `jexample.css`：

```css
.style1 {
  color: #009;
  font-size: 2em;
}
.style2 {
  font-weight: bold;
}
.style3 {
  font-style: italic;
}
```

这些方法中的每一个都可以接受两个参数：执行效果所需的时间以及一个可选的回调函数（在本节稍后的部分讨论）。例如，调用 `show(method)` 如果不使用任何参数，将立即显示元素，如下代码所示：

```javascript
$("#story").show();
```

如果你想让元素随时间显示，可以将毫秒数数字作为参数传递给 `show` 方法：

```javascript
$("#story").show(1000);
```

当提供此参数时，元素将在指定的时间范围内逐渐淡入，同时增加宽度和高度。在这里，“story”元素将在 1000 毫秒（1 秒）内淡入并增大尺寸。或者，你也可以使用预设值“fast”或“slow”来指定特定的时间范围，如下代码所示：

```javascript
$("#story").show("fast"); // "fast" 在 200 毫秒内显示元素
$("#story").show("slow"); // "slow" 在 600 毫秒内显示元素
```

其他方法的工作方式相同，但执行的动画不同：`slideDown` 通过向下滑动进入位置来显示元素，`slideUp` 在上一个动画完成后向上滑动来显示元素，`fadeIn` 通过逐渐淡入显示元素，而 `fadeOut` 则通过逐渐淡出显示元素。

如果你需要，可以为这些方法中的任何一个添加第二个参数，即一个回调函数，它将在效果执行完成后立即执行。这对于将两个或多个效果连接在一起非常有用，每个效果在上一个效果完成后执行。例如，以下代码将在 500 毫秒内显示“story”元素，然后在 2000 毫秒内将其淡出：

```javascript
$("#story").hide();
$("#story").show(500, function () {
  $("#story").fadeOut(2000);
});
```

你可以通过在 `fadeOut` 方法的第二个参数中使用回调函数来继续该过程，然后根据需要继续添加回调函数，直到完成你所需的效果。

最后，如果你需要在元素上发生事件时阻止默认操作（例如，当你不希望跳转链接时），你可以使用 jQuery 事件注册，同时保持在事件对象中。这允许你调用 `eventDefault()`，如下代码所示：

```javascript
$(document).ready(function () {
  // 对象被传递给处理
  // 点击事件的函数
  $("#story").hide(); // 链接的默认操作
  $("#changelink").click(function (event) { // 在被点击时被阻止
    event.preventDefault();
    $("#story").show("fast"); // 显示“story”元素
  });
});
```

如果你需要脚本在较多的浏览器中运行，jQuery 库会被证明是一个非常有用的工具。由于它有助于元素选择、事件处理以及显示/动画方法，它能让你在需要编写跨浏览器代码时减少工作量。如果你想进一步研究 jQuery 库，下一节将提供一些资源。

### 进阶阅读

你可以通过以下资源了解更多关于 jQuery 以及如何使用它的：

- https://learn.jquery.com/
- jQuery：初学者指南 (McGraw-Hill, 2014)

## 尝试练习 16-1 使用 jQuery 创建效果

你有一个链接和一个包含某些文本的 `div` 元素，你希望它们初始是隐藏的，但在点击链接时显示。一旦显示，你希望该 `div` 元素缓慢淡出。你将使用 jQuery 来完成此任务。

### 逐步步骤

1. 创建一个名为 `pr16_1.html` 的 HTML 文档，并使用以下 HTML 代码作为 `body` 部分：

```html
<body>
  <h1>读一个短故事</h1>
  <p>
    <a href="page.html" id="changelink">查看故事</a>
  </p>
  <div id="story">
    我正走在街上，我看到了这个家伙。他正<br>
    坐在街上，然后他说：“你好”
  </div>
  <script src="http://ajax.google.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
  <script type="javascript" src="prjs16_1.js"></script>
</body>
```

2. 创建一个名为 `prjs16_1.js` 的 JavaScript 文件。在这个文件中，你需要等待文档准备就绪，然后立即隐藏“story”元素。接下来，为“changelink”链接注册点击事件，阻止其默认操作，然后使用“向下滑动”动画在 3000 毫秒内显示“story”元素。随后，“story”元素应在 10000 毫秒内淡出。完成后，你的 JavaScript 代码应该像这样：

```javascript
$(document).ready(function() {
  $("#changelink").click(function (event) {
    event.preventDefault();
    $("#story").slideDown(3000, function () {
      $("#story").fadeOut(10000);
    });
  });
});
```

3. 保存 HTML 和 JavaScript 文件，然后打开 HTML 文件。

### 尝试练习总结

在这个项目中，你使用了 jQuery 创建了动画。

### 专家问答

**Q:** 有什么用于开发 JavaScript 的库吗？

**A:** 有的！如果你想深入游戏开发，可以查看以下链接以了解一些：

- PixiJS https://github.com/pixijs/pixi.js
- Phaser https://github.com/photonstorm/phaser
- Babylon.js https://github.com/BabylonJS/Babylon-js

## 调试脚本

尽管 JavaScript 很有趣，但有时它可能非常沮丧。代码中的一个错误就会导致整个脚本运行异常或完全不运行。调试脚本可能是一个耗时且辛苦的过程，但有一些技巧可以帮助节省时间。调试脚本的第一步是确定是什么类型的错误引起了问题。

### 错误类型

两种主要的错误类型是语法错误和逻辑错误。语法错误发生在代码忘记添加分号、忘记引号、拼错单词等时候。逻辑错误发生在代码实现不正确时。

例如，如果执行循环的条件永远不会变为假，循环可能会无限进行。虽然它的语法可能是正确的，但结果并不是程序员所预期的。

### 寻找语法错误

语法错误可能仅仅是漏掉了必要的分号。例如，以下代码是：

```javascript
let greet = function() { say_hi(); say_welcome(); };
```

在这种情况下，分号非常重要，因为两个语句在同一行上。为了修复这个问题，你需要添加所需的分号，如下所示：

```javascript
let greet = function() { say_hi(); say_welcome(); };
```

### 注意

大多数现代浏览器默认会隐藏这些错误消息，或者将它们放在控制台中，但你可以在需要查看时开启它们。

这些消息可以帮助你找出问题产生的原因。错误消息中显示的行号通常会告诉你错误所在的位置。例如，如果消息显示错误在第 15 行，你就从文档顶部的第 15 行开始查看那里写了什么。消息的其他部分可能会告诉你缺少了什么，或者哪些内容放置不当。

然而，有时消息中指定的行号并不是实际问题所在的地方。它可能在前一行、几行之外，或者完全在其他地方。你可能需要进行一些搜索来确定问题是从哪里开始的。

**扫描脚本** 如果错误消息没有帮助定位问题，你可以尝试扫描脚本查找代码中的错误。这种方法可能更加繁琐，但如果错误消息没有用处，它可能会帮助你找到问题。表 16-2 显示了一些你应该尝试寻找的项。

| 项目 | 外观 |
|---|---|
| 缺少分号 | `;` |
| 缺少大括号或方括号 | `}[]` |
| 缺少括号 | `()` |
| 缺少单引号或双引号 | `' "` |
| 拼写错误 | 例如，将 true 写成 ture |

**表 16-2** 扫描脚本查找错误时要寻找的项目

以下代码充满了错误；看看你能找到其中多少个：

```javascript
let money = 0;
let mycar = "Mustang";
function send_alert () {
  alert("You like " + mynar + "!");
  alert("Cool");
}
```

```javascript
let somearray = new Array(2)
somearray[0] = "Me";
somearray[1] = "Me";
for (let count = 0; count < somearray.length; count++) {
  document.write(somearray[0] + " " and " " + somearray[1]);
}
```

代码缺少许多必要的项目。以下是你应该发现的项列表：

- **第 3 行和第 4 行之间** 函数缺少了一个大括号。
- **第 4 行** 单词 *alert* 拼写错误为 *alery*；单词 *like* 后面缺少双引号；变量拼写错误为 *mynar*。
- **第 5 行** alert 方法缺少一个右括号。
- **第 7 行** 单词 *new* 拼写错误为 *neq*。
- **第 9 行** 数组索引数字缺少左方括号。
- **第 10 行** 缺少循环的左括号。
- **第 11 行** somearray[0] 的索引数字缺少右方括号。
- **第 11 行和第 12 行之间** 缺少结束循环的右大括号。

你可能不会犯很多错误，但这些示例提供了一种在扫描脚本时捕获这些错误的好方法。当你定位这些小错误变得更有经验后，当脚本中出现问题时，你就能快速找到它们。

### 寻找逻辑错误

逻辑错误通常难以寻找，因为代码的语法是正确的。你将尝试寻找代码实现方式中的错误。例如，查看以下代码（但不要运行它！）

```javascript
x = 1;
y = 2;
while (x <= y) { // Problem: x is not greater than y!
  alert("Hi");
}
```

代码没有语法错误。所有的分号和引号都在它们应该在的位置。问题在于变量 x 不大于变量 y。这将导致无限循环，可能导致浏览器崩溃。

你可以通过在循环内部添加一行来增加 x 的值、减少 y 的值，或者同时增加 x 并减少 y 来修复代码。关键点是必须采取某些操作使条件变为假。以下代码显示了该问题的可能的解决方法：

```javascript
x = 1;
y = 2;
while (x <= y) {
  alert("Hi");
  x++;
}
```

在循环中增加 x 将允许 x 随着推移大于 y。

### 使用控制台

如果某些值看起来不正确，可以在脚本的任何时候将它们发送到控制台进行快速检查。例如，假设你有以下代码：

```javascript
let x = 2,
y = 0;
// other code...
let z = x/y;
alert(z);
```

当运行这段代码时，alert 将显示 "Infinity"，这可能不是预期的结果。在初始变量和将计算结果 (x/y) 赋值给变量 z 之间如果有额外的代码，你在扫描代码时可能很难发现正在进行除零操作。要找出错误在哪里，你可以在变量计算之前的代码中放置一个 `console.log()`，看看它是否能帮助你看到发生了什么，如下例所示：

```javascript
let x = 2,
y = 0;
// other code...
console.log("Calculation");
let z = x/y;
alert(z);
```

### 专家问答

**问：** 我收到的错误信息包含一些我不懂的内容。我该怎么办？

**答：** 错误信息并不总是有意义的，也不总是指向代码中正确的某行。你可能需要对错误信息所在行或其附近行中你调用的任何变量或函数进行追溯。当你看到过几次错误信息后，理解它们就会变得越来越容易。

**问：** 我代码中的某些内容在我尝试运行时导致了浏览器崩溃，我无法通过添加 `alerts` 来帮助查找问题，因为每次都会崩溃！我该怎么办？

**答：** 如果脚本导致浏览器崩溃，请仔细检查你的变量、循环、对象和函数。你也可以尝试使用浏览器扩展（例如 Firefox），它允许你在脚本中设置断点。最后的办法是从头开始编写一些新代码。

**问：** 我代码中的一个错误不仅让浏览器崩溃了，还让电脑崩溃了！我该怎么办？

**答：** 重启电脑，但不要再次运行该代码。仔细检查是否能找到问题。

**问：** 还有什么其他策略可以帮助调试我的脚本吗？

**答：** 一些编辑器使用颜色编码来标记 HTML 标签、JavaScript 代码或其他类型的代码。颜色编码可以帮你更清晰地看到代码，并更容易检测错误。（尝试使用 Vim 或 NoteTab 文本编辑器。）

## JavaScript 与无障碍性

你在书中多次看到的一个主题是：脚本或用于脚本的 HTML 代码与无障碍性（Accessibility）之间的关系。在某些情况下，州或联邦法律（如《美国残疾人法案》）要求网站必须让残障人士能够访问。即使这对于你的网站来说不是法律问题，它仍然是一个可用性问题：你希望尽可能多的访问可以使用你的网站并获取你提供的信息。

无障碍性的通用术语是，内容需要对所有浏览器以及可能访问网站的软件可见。这意味着你的内容不仅应该被各种 Web 浏览器读取，还要被阅读软件（例如 Freedom Scientific 的 JAWS）或手机等便携设备上的网页浏览软件读取。

### 将内容与呈现分离

通常，使网站内容具有无障碍性的第一步是将无障碍性构建到你的 HTML/XML 代码中，但你还需要调整你的 JavaScript 代码。正如你可能已经知道的，在编写 HTML 时，可以使用层叠样式表（CSS）来呈现内容（显示多少列、字体、各个区域的宽度），同时使用 HTML 仅对内容本身进行标记（例如使用 `<div>` 标签将其划分为区域或插入图像等对象）。这解决了处理纯 HTML 内容时的问题，因为使用样式表而不是 HTML 标记确保了你可以为不同类型的浏览器提供不同的 CSS 样式，或者即使不使用 CSS 功能，仍然获得纯文本的结构化标记（例如，不会有列或字体颜色等），让他们仍然能够看到页面的内容。

通过 JavaScript，使内容具有无障碍性通常意味着确保脚本中使用的内容始终显示在页面上，或者通过链接或其他方法可用。一种可能有帮助的方法是将所有的 JavaScript 代码（或尽可能多的代码）移到外部 JavaScript 文件中，在 HTML 代码中保留尽可能少的 JavaScript 代码。例如，你可能有一个使用以下代码的网页：

```html
<body>
  <script type="text/javascript">
    function send_alert() {
      window.alert("Hi, there is a sale today! 20% off everything!");
      return false;
    }
  </script>
  <a href="#" onclick="send_alert();">Hi!</a>
</body>
```

这段代码仅对支持 JavaScript 的人有效。然而，在 HTML 代码中包含脚本会导致在你需要更新 HTML 代码时必须在文件中反复滚动（特别是当你有一个很长的脚本时）。因此，你可能想做的第一步是将脚本移动到外部文件，如下代码示例所示。首先是新的 HTML：

```html
<body>
  <a href="#" onclick="send_alert();">Hi!</a>
  <script type="text/javascript" src="myscript.js"></script>
</body>
```

接下来，是 `myscript.js` 文件：

```javascript
function send_alert() {
  window.alert("Hi, there is a sale today! 20% off everything!");
  return false;
}
```

这使得 HTML 文件变得更短、更容易读，因为 JavaScript 功能被放置在它自己的文件中，并且避开了 HTML 代码。

你可能想做的下一步操作是更改 HTML 标签中 `onclick` 处理器的使用方式。虽然这样做是有效的，但如果你决定使用不同名称的函数，或者决定创建一个不带 JavaScript 的普通链接，就会变得麻烦，因为你需要更新每个 HTML 文件来适应这一更改（你可以简单地更改脚本以使用这个新函数，或者什么都不做，但这可能让那些需要更新代码的人感到困惑）。对于 HTML 代码的这个事件处理程序，你可以稍微重写 JavaScript 并给锚点标签一个 `id`（你已经在书前面的部分做过这一点）。首先是更新后的 HTML 代码：

```html
<body>
  <a href="#sale" id="sale">Hi</a>
  <script type="text/javascript" src="myscript.js"></script>
</body>
```

接下来，是 `myscript.js` JavaScript 文件：

```javascript
function send_alert() {
  window.alert("Hi, there is a sale today! 20% off everything!");
  return false;
}
let saleLink = document.getElementById("sale");
saleLink.addEventListener("click", send_alert);
```

2. 创建名为 `sales.html` 的 HTML 文档，并使用以下 HTML 代码作为主体部分：

```html
<body>
<h1>Sales:</h1><br>
Clothes: 25% off<br>
Electronics: 10% off<br>
Appliances: 15% off (with coupon)
</body>
```

3. 通过对每个 JavaScript 代码进行任何调整，并将每段 JavaScript 代码[尽可能地]移动到名为 `prjs15_2.js` 的 JavaScript 文件中，使代码对于没有 JavaScript 的用户也是可访问且这些。

4. 一种可能的解决方案见下面的 HTML 代码（针对 `prjs15_2.html`）和 JavaScript 代码（针对 `prjs15_2.js`）。

HTML 代码:

```html
<body>
<div>
<h1>Sales:</h1>
</div>
<div>
<a href="sales.html" id="slink">点击查看销售信息</a>
</div>
<script type="text/javascript" src="prjs15_2.js"></script>
</body>
```

JavaScript 代码:

```javascript
let slink = document.getElementById("slink");
slink.addEventListener("click", function(event) {
  event.preventDefault();
  window.open('sales.html', 'newwin', 'width=300,height=200');
}, false);
```

5. 保存 HTML 和 JavaScript 文件，并在浏览器中打开 HTML 文件。现在内容应该可以在你选择的任何打开页面的浏览器中访问。

### 尝试总结

在这个项目中，你利用关于可访问性的知识，使文档和脚本对观众更易访问。

## JavaScript 安全

你可能注意到，当你尝试在主浏览器窗口上使用 `window.close()` 方法时，会出现一个确认框，询问你是否真的允许关闭窗口。这种情况是 JavaScript 安全问题之一。浏览器不希望网站在未经观众许可的情况下关闭观众打开的窗口。如果允许这样做，程序员将对观众的计算机拥有控制权，这可能会产生问题。

安全的另一个方面是一个错误观念，认为你可以用密码来“保护”Web 页面，或者防止用户查看页面的源代码。

安全的另一个方面是防御跨站脚本攻击——使用 JavaScript 从未正确过滤用户输入的服务器端应用程序中获取信息。

### 页面保护

许多脚本尝试以某种方式将观众挡在外面，例如使用密码保护或使用“禁用右键”脚本来防止查看页面的源代码。

然而，这些安全策略在很大程度上是无效的，因为“密码”和“禁用右键”脚本可以通过关闭 JavaScript 或进行一些额外工作来绕过。

### 密码

某些密码比其他的要好，但似乎没有一种密码能提供真正的页面安全。如果你不想让某查看页面，比使用 JavaScript 系统有好得方法，例如使用服务器端语言或在你的 Web 服务器上的某些设置。

如果你使用的是免费托管服务，更好的方法可能可用也可能不可用。不过，请记住 JavaScript 密码系统并不是万无一敌的，你应该用这样的系统保护任何重要内容。

### 隐藏 Web 页面源代码

很多人想隐藏 Web 页面的源代码。然而，JavaScript 并无法起作用。许多脚本尝试通过各种手段禁用右键。基本上，这些策略是无效的，因为它们可以通过几种方式绕过：

- 如果禁用了右键，你始终可以尝试“查看源代码”。
- 如果前面的方法不起作用，你可以始终关闭 JavaScript 或查看电脑上的缓存文件夹。浏览器将拥有显示页面的代码，因此代码的副本会进入浏览器的缓存。

从长远来看，这些脚本只是让查看源代码变得更加困难（并且很烦人）。

### 跨站脚本

跨站脚本（通常简称为 XSS）以恶意方式使用 JavaScript 代码（或其他类型的代码），从具有漏洞应用程序的 Web 网站用户处获取信息。通过这些信息，他人可以使用别人的 cookie 或会话信息，并像他们是获取信息的那个用户一样访问 Web 网站。当然，这可能会导致大麻烦，特别是当该用户是该应用程序的管理员，或者该应用程序处理资金时（例如银行或购物应用程序）。

虽然 JavaScript 是执行此类攻击的方法之一，但有漏洞的应用程序通常是服务器端的，并在页面上显示用户输入。如果用户输入在服务器端应用程序中没有经过清理（验证），那么可以输入任何可能的脚本来代替预期的输入。

例如，你可能有一个表单，使用服务器端脚本允许人们发送评论。该脚本将用户提交的评论返回给用户作为确认。如果输入没有经过清理，就有可能在评论字段中输入内容：`<script>alert('You've been had!');</script>`。如果有人提交了此内容并在响应页上看到警报，就会产生潜在的漏洞，并可能直接将后续用户引导到恶意 URL，用户的 cookie 或会话信息可以在那里被获取。

跨站脚本多年来一直在演变。起初，坏的 Web 网站可以加载好的 Web 网站（或在弹出浏览器窗口中），并通过 JavaScript 访问文本框、cookie 和其他数据（用户 ID 和密码）——这就是“跨站”名称的由来。需要注意的是，过去四五年的现代浏览器不再允许这种跨站脚本。一个域名无法访问另一个域的内容。大多数现代跨站脚本攻击都是注入攻击，如示例所示（通常复杂得多）。

## JavaScript 与 HTML5

### 使用 Canvas

canvas 元素允许你在页面上绘制图形。你可以使用 JavaScript 在画布上绘制形状、线条、文本等。

要使用 canvas，你需要在 HTML 中添加一个 `<canvas>` 元素，并给它一个 `id`：

```html
<canvas id="graphic" width="200" height="200"></canvas>
```

然后，在 JavaScript 中获取该元素并获取其 2D 上下文：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
```

canvas 的原点是左上角，因此较高的 x 坐标会将点向右移动更多，而较高的 y 坐标会将点向下移动更多。

如果你决定绘制一个不填充颜色的轮廓矩形，可以在下面的代码中使用 `strokeRect()` 代替：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.strokeRect(70, 70, 50, 30);
```

如果你需要清除画布上的某个矩形区域，可以使用 `clearRect()` 方法。它使用与 `fillRect()` 相同的四个参数，但会清除（变为透明）它影响的区域。例如，你可以使用下面的代码清除填充矩形内部的一个矩形：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.fillRect(70, 70, 50, 30);
ctx.clearRect(80, 80, 20, 10);
```

### fillStyle 和 strokeStyle

形状或轮廓的默认颜色是黑色 (#000000)。要使用不同的颜色，可以使用 `fillStyle` 属性设置颜色，使用 `strokeStyle` 属性设置描边（轮廓或线条）的颜色。例如，考虑这段代码：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.fillStyle = "#FF0000";
ctx.fillRect(70, 70, 50, 30);
```

形状的填充颜色设置为 #FF0000（红色）。绘制了一个矩形，并将使用新的填充颜色。

在这里，`fillStyle` 设置为 #FF0000（红色），在此赋值之后的任何形状都将使用红色作为填充颜色。在你在使用不同颜色的形状时，可以随时更改它，如下代码所示：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.fillStyle = "#FF0000"; // fillStyle 设置为红色
ctx.fillRect(70, 50, 30, 30); // 这个矩形是红色的
ctx.fillStyle = "#00FF00"; // fillStyle 设置为绿色
ctx.fillRect(10, 50, 30, 30); // 这个矩形是绿色的
ctx.fillStyle = "#FF0000"; // fillStyle 再次设置为红色
ctx.fillRect(120, 50, 30, 30); // 这个矩形是红色的
```

如果你有特定的设置（如 `fillStyle` 和 `strokeStyle`）想要以后保存，可以使用 `save()` 方法。你可以使用 `restore()` 方法恢复这些设置，如下代码所示：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.fillStyle = "#FF0000"; // fillStyle 设置为红色
ctx.save(); // 保存当前属性（在此处保存了 fillStyle）
ctx.fillRect(70, 50, 30, 30); // 这个矩形是红色的
ctx.fillStyle = "#00FF00"; // fillStyle 设置为绿色
ctx.fillRect(10, 50, 30, 30); // 这个矩形是绿色的
ctx.restore(); // 使用恢复保存的属性值（在此处恢复了保存的 fillStyle）
ctx.fillRect(120, 50, 30, 30); // 这个矩形是红色的
```

你可以像使用 `fillStyle` 一样使用 `strokeStyle` 来设置形状轮廓或绘制线条（路径）的颜色。例如，下面的代码将绘制一个带有轮廓的矩形：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.strokeStyle = "#FF0000";
ctx.strokeRect(70, 50, 30, 30);
```

### 使用路径

canvas 还允许你绘制线条和曲线（路径），这让你有机会创建更复杂的图形。你通过调用 `beginPath()` 方法开始一个路径，然后通过调用其中一个方法结束路径。在之间，你可以使用许多方法来绘制线条、曲线等。表 16-3 列出了路径内可以使用的方法。

| 方法 | 描述 |
| :--- | :--- |
| `arc(x, y, radius, start_angle, end_angle, counterclockwise)` | 在 (x,y) 处绘制圆弧，半径在 `start_angle` 和 `end_angle`（弧度）之间。`counterclockwise` 参数设置为 true 如果按逆时针计算角度，否则反之。 |
| `arcTo(x, y, x2, y2, radius)` | 从上一个点通过 (x,y) 绘制圆弧并结束于 (x2,y2)。 |
| `bezierCurveTo(cpx, cpy, x2, y2, x, y)` | 使用控制点 (cpx, cpy) 和 (x2, y2) 绘制一条曲线。 |
| `lineTo(x, y)` | 从上一个点绘制线条到 (x,y)。 |
| `moveTo(x, y)` | 将光标移动到 (x,y) 而不绘制任何内容。 |
| `quadraticCurveTo(cpx, cpy, x, y)` | 使用控制点 (cpx, cpy) 从上一个点绘制一条曲线到 (x,y)。 |
| `rect(x, y, width, height)` | 在 (x,y) 处绘制指定宽度和高度的矩形。 |

**表 16-3** 绘制方法

例如，假设你决定使用线条和圆弧绘制路径并描边该路径。你可以使用下面的代码：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.strokeStyle = "#000000";
ctx.beginPath();
ctx.moveTo(10,10);
ctx.lineTo(10,50);
ctx.arc(80,20,10,20);
ctx.stroke();
```

使用 stroke 绘制路径（绘制红色线条）。图 16-10 显示了这段代码的结果。它在画布上绘制了一个椭圆。

| 方法 | 描述 |
| :--- | :--- |
| `closePath()` | 通过绘制回到路径起始点的线条来结束路径。 |
| `clip()` | 根据路径创建一个裁剪区域。 |
| `fill()` | 如果完成，则用当前的 `fillStyle` 填充路径。 |
| `stroke()` | 使用当前的 `strokeStyle` 描边路径。 |

**表 16-4** 结束路径的方法

### 添加文本

canvas API 提供了两种向上下文添加文本的方法：`fillText()` 和 `strokeText()`。它们接受相同的参数：文本、x、y 以及设置最大宽的可选参数（如果文本超过设置宽度，将尝试进行压缩）。例如，下面的代码从 (10,10) 开始绘制文本 "I am some text on a canvas"，最大宽度为 200 像素：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.fillStyle = "#000000";
ctx.fillText("I am some text on a canvas", 10, 100, 200);
```

有三个属性可以用于设置样式：

- **font**: 使用 CSS 格式设置字体属性（例如，**bold 1em Verdana**）。
- **textBaseline**: 设置文本基准线。可能的值有 "alphabetic", "bottom", "hanging", "ideographic", "middle" 和 "top"。
- **textAlign**: 设置文本的对齐方式。可能的值有 "center", "end", "left", "right" 和 "start"。

因此，如果你想更改字体并对齐文本，可以在下面的代码中设置 `font`：

```javascript
let graphic = document.getElementById("graphic");
ctx = graphic.getContext("2d");
ctx.fillStyle = "#000000";
ctx.font = "bold 1em Verdana";
ctx.textAlign = "start";
ctx.fillText("I am some text on a canvas", 10, 100, 200);
```

现在文本将是 "end" 对齐的粗体 Verdana 字体。

### 延伸阅读

已经涵盖了使用 canvas 的基础，但还有更多你可以做的。你可以在以下网站学习更多关于使用 canvas 的知识：

- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial
- www.html5canaututorial.com/

## 拖放

### 拖放事件

拖放过程涉及七种事件，如表 16-5 所示。这些中的每一个都可以添加事件监听器，以执行进一步的脚本操作。根据你的需求，在创建拖放脚本时，可以使用这些事件中的任意数量。

| 事件 | 事件目标 | 描述 |
|---|---|---|
| dragstart | 被拖动项目 | 按住鼠标键并开始拖动时发生 |
| drag | 被拖动项目 | 在 dragstart 之后立即发生，并在整个拖动期间持续触发 |
| dragend | 被拖动项目 | 在松开鼠标键并释放项目结束拖动时发生，无论是否放置在有效目标上 |
| dragenter | 放置目标 | 项目首次被拖入放置目标区域时发生 |
| dragover | 放置目标 | 在 dragenter 之后立即发生，只要项目在放置目标内移动就会持续触发 |
| dragleave | 放置目标 | 项目被拖出放置目标区域时发生 |
| drop | 放置目标 | 项目被放入放置目标区域时发生 |

**表 16-5** 拖放事件

### dataTransfer 对象

虽然你现在可以使用现有的功能拖动并放置项目，但你可能想要访问存储在被拖动项目中的数据，以便在放置时可以使用它。这正是使用 `dataTransfer` 对象的地方。

`dataTransfer` 对象是事件对象的一部分，具有用于设置和从拖动项目中检索数据的方法：`setData()` 和 `getData()`。`setData()` 方法可用于设置自定义数据，但在拖动选定项目或链接时它也会被默认调用。对于选中的文本或图像，它将存储被拖动的文本；对于链接，它将存储链接的 URL。如果你需要存储自定义数据而非使用这些默认值（或你正在拖动不同类型的元素），可以使用以下代码存储文本或 URL：

```javascript
event.dataTransfer.setData("text", "String of text ... ");
event.dataTransfer.setData("URL", "http://www.mysite.com");
```

注意，你可以在单个 `dataTransfer` 对象中同时存储 "text" 和 "URL"，但每种类型不能多于一个。HTML5 扩展了此功能，允许传递任何 MIME 类型（"text" 和 "URL" 仍然有效，分别相当于 "text/plain" 和 "text/uri-list"）。

只需记住，每个 MIME 类型在 `dataTransfer` 对象中只能存储一个数据。`getData()` 方法用于从 `dataTransfer` 对象中检索存储的数据。由于浏览器兼容性原因，从 `dataTransfer` 对象中检索文本 URL 或信息时，最好使用以下示例代码：

```javascript
let dropletext = event.dataTransfer.getData("Text");
let droproURL = event.dataTransfer.getData("URL") ||
event.dataTransfer.getData("text/uri-list");
```

注意在检索文本时使用了大写的 "T"，这使得旧版本的 Firefox 能够获取该值，同时在其他浏览器中也能保持正常工作。此外，获取 URL 的方法会先测试 "URL"，然后测试 MIME 类型 "text/uri-list"，以帮助旧版本的 Internet Explorer。

### 快速拖放脚本

为了综合以上所有内容，你将创建一个脚本，将链接拖入 div 元素中以显示链接 URL。首先，从以下 HTML 代码开始：

```html
<h1>快速拖放</h1>
<p>
将链接拖动到下方的框中以查看链接 URL
</p>
<p><a href="http://www.mysite.com" id="mylink">我的网站</a>
</p>
<div id="dropdiv" style="border: 1px solid #000;padding:5px;">&nbsp;</div>
```

由于链接默认是可拖拽的，因此这里不需要 `draggable="true"` 属性。div 元素设置了边框，以便用户可以看到向哪里拖动链接。接下来，你需要以下 JavaScript 代码：

```javascript
// 获取 dropdiv（带边框的 div）
let dropdiv = document.getElementById("dropdiv");
dropdiv.addEventListener("dragover", function (event) {
  event.preventDefault(); // 阻止拖放的默认事件
}, false);
dropdiv.addEventListener("dragenter", function (event) {
  event.preventDefault(); // 阻止拖放的默认事件
}, false);
dropdiv.addEventListener("drop", function (event) { // 为 drop 事件添加监听器
  let divtext = event.dataTransfer.getData("URL");
  event.preventDefault(); // 阻止默认事件
  dropdiv.innerHTML = divtext;
}, false);
// 更改放置目标的 innerHTML，以便显示
// divtext 变量的值，该值即为
// 被拖动链接的 URL (http://www.mysite.com)
```

### 尝试此总结

在这个项目中，你更新了拖放脚本，使其能够从 `dataTransfer` 对象中存储和检索文本。当链接被拖动并放置到目标 div 元素时，这些文本就会显示出来。

## 完成 Node.js 应用

通过第 15 章对 AJAX 的学习，你现在只需通过使用 `XMLHttpRequest` 获取球手（bowler）即可完成你的 Node.js Web 应用。这需要对 Node.js 代码和前端代码进行一些更改，以便完成球手信息的显示。

### 更新 Node.js 代码

由于现在希望在用 `XMLHttpRequest` 时将信息发送到前端，你将用旧的 `getBowlerData()` 函数替换为一个新的路由处理器，该处理器将返回数据库查询的结果，并在向前端发送最终数据之前进行一些添加。

首先，更新你的 `server.js` 文件使用以下代码：

```javascript
const express = require('express');
const app = require('express');
const router = express.Router();
const path = require('path');
const { Pool } = require('pg');
const connectionString = 'postgresql://mybowlerapp:12345@localhost/mybowlerapp';
const pool = new Pool({connectionString: connectionString});
app.use(express.static(path.join(__dirname, 'public')));
router.get('/api/bowlers', function (req, res) {
  pool.query(
    'SELECT * FROM bowlers',
    [],
    function (err, result) {
      if (err) {
        console.error(err);
      }
      result.rows.forEach(function (bowler) {
        bowler.overallAvg = Math.round(
          (bowler.power + bowler.consistency) / 3);
        bowler.fullName = `${bowler.first_name} ${bowler.last_name}`;
      });
      result.rows = result.rows.sort(function (a, b) {
        return a.overallAvg < b.overallAvg;
      });
      res.status(200).json(result.rows);
    });
});
```

这替换了旧的 `getBowlerData()` 函数。文件的其余部分保持不变。

```javascript
router.get('/', function (req, res) {
  res.sendFile(path.join(__dirname, 'index.html'));
});
app.use('/', router);
let server = app.listen(3000, function () {
  console.log("App Server is running on port 3000");
  console.log("To end, press Ctrl + C");
});
```

你需要确保连接字符串使用了你安装的正确信息（你可以从之前完成的旧示例中获得这些信息）。

注意，旧的 `getBowlerData()` 函数被新路由取代了。就像处理默认路由 `'/'` 一样，你现在有了 `'/api/bowlers'` 公共路由。如果你运行服务器并在地址栏中输入 `http://localhost:3000/bowlers`，浏览器将显示从数据库检索球手信息的 JSON 数据结果。当你修改前端代码时，用户将使用 AJAX 请求来获取这些信息。

注意在路由处理函数内部，你执行了之前获取球手信息的逻辑。对数据库进行查询，然后你就可以使用查询结果。在这里，你有机会进行一些拼接以获取球手姓名、计算球手评分，并按球手评分从高到低排序结果。

然后使用以下代码将结果作为 JSON 发送到前端：

```javascript
res.status(200).json(result.rows);
```

`status(200)` 部分设置了将返回的 HTTP 状态码，而 `json(result.rows)` 提供要返回的内容并转换为 JSON 格式。

同样注意以下行未详细查看的代码：

```javascript
app.use(express.static(path.join(__dirname, 'public')));
```

这一行代码为前端代码提供了访问公共资源（如前端所需的 CSS 和 JavaScript 文件）的方法。在这种情况下，它将这些文件的位置设置为你主项目文件夹内的 `"public"` 文件夹。你将在下一节创建此文件夹并向其中添加一些文件。

现在，你可以继续更新前端代码，以便使用此新路由并获取信息。

### 更新前端代码

在前端，你需要在主项目文件夹内添加一个 "public" 文件夹（存放 `server.js` 和 `index.html` 文件的地方）。在更新 `index.html` 文件后，你将在该文件夹内放置 JavaScript 和 CSS 文件。

首先，更新你的 `index.html` 文件使用以下代码：

```html
<html>
<head>
  <title>My Web App</title>
  <link rel="stylesheet" type="text/css" href="./bowlers.css">
</head>
<body>
  <h1 class="bowlers-title">List of Bowlers</h1>
  <table id="bowler-table" class="bowler-table" border="1">
    <tr>
      <th>Name</th>
      <th>Bowler Rating</th>
      <th>Bio</th>
    </tr>
  </table>
  <script src="./bowlers.js"></script>
</body>
</html>
```

- 将包含一个 CSS 文件以提供一些样式。
- 添加了一个表格（table）来包含球手数据。
- 将包含一个 JavaScript 文件，用于从服务器获取数据并显示它。

这种后的 HTML 包含了外部 CSS 和 JavaScript 文件，并创建了用于显示数据的表格。在表头行到位后，你将使用 JavaScript 为每个球手添加新行。

接下来，创建一个名为 `bowlers.css` 的 CSS 文件，包含以下代码并将其保存到 "public" 文件夹中：

```css
body {
  margin: 5px;
  font-family: Verdana, sans-serif;
}
.bowlers-title {
  text-align: center;
}
.bowler-table {
  font-size: 0.8rem;
}
.bowler-table th {
  background-color: #ddd;
}
```

这为页面和显示的表格提供了一些基础样式。你可以根据需要扩展它！

接下来，创建一个名为 `bowlers.js` 的 JavaScript 文件，包含以下代码并将其保存到 "public" 文件夹：

```javascript
let bowlerApp = {
  displayBowlers: function (bowlers) {
    let tableElem = document.getElementById('bowler-table');
    bowlers.forEach(function (bowler) {
      let row = document.createElement('tr');
      let columns = [];
      columns.name = document.createElement('td');
      columns.name.appendChild(document.createTextNode(bowler.fullName));
      columns.bowlerRating = document.createElement('td');
      columns.bowlerRating.appendChild(document.createTextNode(bowler.overallAvg));
      columns.bio = document.createElement('td');
      columns.bio.appendChild(document.createTextNode(bowler.bio));
      row.appendChild(columns.name);
      row.appendChild(columns.bowlerRating);
      row.appendChild(columns.bio);
      tableElem.appendChild(row);
    });
  },
  getBowlers: function () {
    let xhr = new XMLHttpRequest();
    let apiRoute = "api/bowlers";
    xhr.onreadystatechange = function() {
      if (xhr.readyState === 4) {
        if (xhr.status !== 200) {
          console.error("Could not get bowlers. Status: " + xhr.status);
          return;
        }
        this.displayBowlers(JSON.parse(xhr.responseText));
      }
    };
    xhr.open("get", apiRoute, true);
    xhr.send();
  }
};
```

- 创建了一个包含应用程序函数的对象，将它们保持在全局之外。
- 将当前对象的 `this` 绑定到内部函数，允许内部函数使用该对象的属性和方法。
- 调用 `bowlerApp` 对象的 `getBowlers()` 方法启动。

你会看到创建一个名为 `bowlerApp` 的“外部”对象。这有助于将大部分代码保持在全局之外，如果你使用其他库，变量或函数名可能会与它们冲突。你的应用代码包含在自己的 `"bowlerApp"` 命名空间内。

你通过第 15 章已经熟悉 AJAX 调用。这只是从你在 Node.js 服务器上创建的 API 路由获取数据，然后调用 `bowlers` 方法，该方法将创建所需的表格元素，插入检索的数据，并添加到 HTML 代码中的表格中。

你可能注意到的这一点是 `onreadystatechange` 函数末尾的 `bind(this)`。此添加确保你在 `onreadystatechange` 函数引的 `this` 是 `bowlerApp` 对象的 `this`。默认情况下，`onreadystatechange` 函数（以及其他）使用它们自己的 `this` 上文。这种行为会导致对象的调用出现意外，通过为对象提供正确的上下文，你可以使用 `this` 关键字来访问预期对象的属性和方法。注意，如果你不在 `onreadystatechange` 函数内使用任何 `bowlerApp` 属性或方法，则不需要绑定，默认的 `this` 上文也不会影响任何内容。

另一个选项是使用你在书中早些学过的箭头函数。以下代码是使用箭头函数的示例：

```javascript
let bowlerApp = {
  displayBowlers: function (bowlers) {
    let tableElem = document.getElementById('bowler-table');
    bowlers.forEach(function (bowler) {
      let row = document.createElement('tr');
      let columns = [];
      columns.name = document.createElement('td');
      columns.name.appendChild(document.createTextNode(bowler.fullName));
      columns.bowlerRating = document.createElement('td');
      columns.bowlerRating.appendChild(document.createTextNode(bowler.overallAvg));
      columns.bio = document.createElement('td');
      columns.bio.appendChild(document.createTextNode(bowler.bio));
      row.appendChild(columns.name);
      row.appendChild(columns.bowlerRating);
      row.appendChild(columns.bio);
      tableElem.appendChild(row);
    });
  },
  getBowlers: function () {
    let xhr = new XMLHttpRequest();
    let apiRoute = "api/bowlers";
    xhr.onreadystatechange = () => {
      if (xhr.readyState === 4) {
        if (xhr.status !== 200) {
          console.error("Could not get bowlers. Status: " + xhr.status);
          return;
        }
        this.displayBowlers(JSON.parse(xhr.responseText));
      }
    };
    xhr.open("get", apiRoute, true);
    xhr.send();
  }
};
bowlerApp.getBowlers();
```



```javascript
xhr.onreadystatechange = () => {
  if (xhr.readyState === 4) {
    if (xhr.status !== 200) {
      console.error(`Could not get bowlers. Status: ${xhr.status}`);
      return;
    }
    this.displayBowlers(JSON.parse(xhr.responseText));
  }
};
```

完成所有新调用后，从命令行启动 Node.js 服务器 (`node server.js`)，然后在浏览器中打开 `http://localhost:3000`。球手信息将显示在表格中，如图 16-14 所示！

| Name | Bowler Rating | Bio |
|---|---|---|
| Prize Winner | 97 | 优秀的全能球手。如果你想，可以换别人。 |
| Cranky Shoes | 77 | 球可以滚得非常快。稳定性差，而且会向你扔球。 |
| Coach Purswell | 76 | 以前经常打，但现在教练新玩家。 |
| Slow Roller | 71 | 完成一个回合可能需要很长时间，但相当准确。不过没有倒下很多瓶子。 |
| Doctor Gutter | 55 | 喜欢说垃圾话，但倒不下很多瓶子。 |

**图 16-14** 球手信息在浏览器中显示。

# 508 JavaScript: 入学者指南

有了这个基础应用程序，你可以以任何方式返回并对其进行扩展。你可以向数据库中添加更多数据并检索这些数据，通过允许用户从列表中添加或删除保龄球运动员来增加交互性，或者尝试任何其他想法。尽情玩玩吧！

# 需要帮助吗？

如果你发现自己被卡住了并需要帮助，请随时在线访问我。如果你想联系我，可以在以下平台找到我：

- Twitter @ScripteptWeb
- LinkedIn https://www.linkedin.com/in/john-pollock-82a2b074
- GitHub https://github.com/JohnPollock

# 提问专家

Q：我可以在网上找到免费的可以直接复制粘贴的 JavaScript 代码？

- 答：
  - http://javascript.internet.com
  - https://javascriptsource.com/
  - www.javafile.com

Q：我可以在哪里学习更多关于 JavaScript 的知识？

- 答：
  - developer.mozilla.org/en/JavaScript
  - www.javascriptkit.com
  - www.quirksmode.org/js/contents.html

Q：我可以在哪里学习更多关于层叠样式表（CSS）的知识？

- 答：
  - https://css-tricks.com/
  - www.csszengarden.com

Q：我可以在哪里学习更多关于 HTML5 的知识？

- 答：
  - www.html5doctor.com

# 第16 章：进一步基于浏览器的 JavaScript 509

# 第16 章自测

- 1. 下列哪项用于在 jQuery 中检查文档是否就绪？

  A. `docReadyState()`

  B. `$documentReady()`

  C. `$(document).ready()`

  D. `$(document).done()`

- 2. 下列哪行代码使用 jQuery 隐藏 id 为 "story" 的元素？

  A. `$(getElementById("story")).hide();`

  B. `$("#story").hide();`

  C. `#story.hide();`

  D. `$("story").hide();`

- 3. jQuery 使用 ______ 语法来选择元素。

- 4. jQuery 使得编写 ______ 的代码变得更容易。

- 5. ______ 元素允许你使用 JavaScript 在页面的定义区域上绘图。

- 6. 在画布上绘图时，可以使用 `fillCircle()` 方法画一个圆。

  A. 正确

  B. 错误

- 7. 元素的 ______ 属性定义了元素是否可以被拖动。

- 8. JavaScript 可能通过让代码更容易编写来使某些高级编码任务变得更容易。

- 9. 默认情况下，所有元素都是可拖动的。

  A. 正确

  B. 错误

- 10. 当元素开始被拖动时，发生 ______ 事件。

- 11. 哪个对象可以可以在拖放过程中存储或检索数据？

  A. `event.dataStorage`

  B. `event.dataTransfer`

  C. `event.data`

  D. `event.dataMove`

- 12. 使用哪种方法获取在拖放过程中存储的数据？

  A. `retrieveData()`

  B. `getInfo()`

  C. `getItems()`

  D. `getData()`

- 13. JavaScript 有趣吗？

  A. 有！

  B. 对你来说也许吧！

  C. 我是老板逼我学的这个，所以它永远不会有趣！

  D. 我觉得还可以吧。

# 附录

# 自测答案

# 512 JavaScript: 入学者指南

# 第1 章：JavaScript 简介

- 1. C. HTML
- 2. A. 网页浏览器
- 3. C. JavaScript
- 4. B. 错误
- 5. C. ECMAScript
- 6. A. 正确
- 7. C. LiveScript
- 8. A. 基于原型的
- 9. B. 错误
- 10. B. 它可能提供代码高亮、补全、调试工具等功能。
- 11. C. 解释性的
- 12. B. 错误
- 13. D. 客户端
- 14. D. 它被添加到 HTML 文档中。
- 15. A. `<script>` 和 `</script>` HTML 标签

# 第2 章：将 JavaScript 放在 HTML 文件中

- 1. D. 以上所有
- 2. B. 在使用 XHTML 时确保网页通过验证
- 3. A. 是
- 4. `noscript` 标签为没有 JavaScript 的用户提供内容。
- 5. A. `.js`
- 6. B. `<script src="yourfile.js"></script>`
- 7. 在 HTML 中，`script` 标签不区分大小写。但在 XHTML 中，`script` 标签必须是小写。
- 8. D. 分号
- 9. A. `document.write()`
- 10. C. 当脚本非常长或需要放置在多个 HTML 文档中
- 11. JavaScript 注释对于文档记录或调试你的代码非常有用。
- 12. C. `//`
- 13. A. `/*`
- 14. D. `*/`
- 15. A. `close`

# 第3 章：使用变量

- 1. 变量代表或持有一个值。
- 2. A. 它们可以在编写和更新脚本时节省时间，并让你的代码目的更清晰。
- 3. 使用 `var` 声明声明变量。
- 4. D. `=`
- 5. C. `pagenumber = 24;`
- 6. B. 错误
- 7. 变量名必须以字母、美元符号或下划线开头。
- 8. A. 正确
- 9. 在 JavaScript 中，数据类型包括 `Number`, `String`, `Boolean`, `Null`, `Undefined`, `Symbol` 和 `Object`。
- 10. 在 JavaScript 中用字母 `e` 表示指数。
- 11. C. `var mytext = "Here is some text!";`
- 12. D. `document.write("Hi!");`
- 13. 特殊字符允许向字符串无法添加的内容。
- 14. B. `document.write("I like " + hobby + " every weekend");`

## 第4 章：使用函数

- 1. 一般来说，函数是较大脚本中的一个小脚本，用于执行任务或一系列任务。
- 2. B. 它们是可以重用的。
- 3. 在函数的第一行，声明它，命名它，并指示它是否接受任何参数。
- 4. C. `function`
- 5. A. `{}`（大括号）
- 6. A. 正确
- 7. B. 错误
- 8. C. `function_text()`
- 9. 参数用于允许函数从外部导入一个多个值。
- 10. B. `()`（括号）
- 11. D. 逗号
- 12. D. `window.alert("This is text");`
- 13. B. `alert("some", "words");`
- 14. A. `var shopping = get_something();`
- 15. A. 全局变量可以在 JavaScript 的任何地方使用。
- 16. `const` 和 `let` 关键字在当前块中创建值。

# 第5 章：JavaScript 运算符

- 1. 运算符
- 2. 算术
- 3. 加法
- 4. 之前
- 5. D
- 6. A
- 7. 右，左
- 8. C
- 9. A
- 10. D
- 11. 逻辑
- 12. B
- 13. B
- 14. 位运算符
- 15. 优先级

# 第6 章：条件语句和循环

- 1. 条件，条件
- 2. 原因，结果
- 3. A
- 4. B
- 5. C
- 6. `switch`
- 7. 循环
- 8. B
- 9. A
- 10. `while`
- 11. B
- 12. A
- 13. B
- 14. B
- 15. D

# 第7 章：JavaScript 数组

- 1. 数组是存储数据列表的方式。
- 2. 在 JavaScript 中定义数组有两种方法。
- 3. 在数组中，通过使用索引访问元素。
- 4. 你可以使用循环遍历数组中的所有项。
- 5. B. 错误。
- 6. D. `let myArray = new Array[10];`
- 7. B 错误（`this` 访问第六个项，`cool[4]` 访问第五个）。
- 8. C. 创建具有五个元素的数组。
- 9. A. `length` 属性。
- 10. 数组字面量允许你使用方括号创建数组，而无需编写 `"new Array"`。
- 11. `concat()` 方法用于合并两个或多个数组的项并返回包含所有项的数组。
- 12. `join()` 方法用于将数组的项合并为一个字符串，每个项由指定的字符分隔。
- 13. `pop()` 方法用于从数组中删除最后一个元素。
- 14. C. 它使用字符代码对内容进行排序。
- 15. 嵌套数组提供了创建多维数组的能力。

# 第8 章：对象

- 1. 对象是属性和值的集合。
- 2. 创建单个对象时，可以使用对象构造函数或对象字面量符号。
- 3. A. 正确。
- 4. B. 点运算符（`.`）。
- 5. 当你需要使用变量来访问属性名时，可以使用括号符号。
- 6. A. 构造函数可以用于创建对象结构。
- 7. 使用 `new` 关键字创建对象的实例。
- 8. B. 错误。
- 9. 假设 `myobject` 存在，它将 `myobject` 的 `kitchen` 属性的值赋值给变量 `x`。
- 10. 如果在对象实例中找不到属性，JavaScript 将查找对象的原型。
- 11. B. `window.alert("You are using " + navigator.appName);`
- 12. 由于 `myobject` 存在，`kitchen` 属性被分配了一个新的字符串值 `"big"` 或被初始化为值 `"big"`。
- 13. 在 JavaScript 中，有很多预定义对象可以使用它们来访问你可能需要的某些属性和方法。
- 14. `navigator` 对象让你访问查看浏览器的各种属性。
- 15. C. `appType`。

## 第 9 章：文档对象

- 1. `document` 对象是浏览器为每个查看的新 HTML 页面创建的对象。
- 2. 文档对象的 `referrer` 属性返回将访问引导至当前文档的文档 URL。
- 3. A. 正确。
- 4. D. `getElementById()`。
- 5. B. 错误（它是作为最后一个子节点添加的，而不是第一个）。
- 6. B. 错误。
- 7. 文档对象的 `anchors` 属性是一个数组，包含了页面上所有的锚点 (`<a>`) 标签。
- 8. `innerHTML` DOM 节点属性允许你更改元素节点的 HTML 内容。
- 9. `lastModified` 属性存储当前文档最后修改的日期时间。
- 10. A. 正确。
- 11. A. 正确。
- 12. C. URL。
- 13. C. 它在行尾添加一个 JavaScript 换行符。
- 14. 所有具有相同 `name` 属性值的元素（最常见的是单选按钮）。
- 15. B. `document.write()` 和 `document.writeln()` 语句。

## 第 10 章：事件处理器

- 1. A. 正确。
- 2. 事件处理器非常有用，因为它们允许你访问页面上可能发生的事件。
- 3. 要使用事件处理器，你可以将其放置在 HTML 或 JavaScript 代码中。
- 4. `<input type="button" onclick="window.alert('Hey there!');">`
- 5. `load` 事件在 Web 页面加载完成时发生。
- 6. D. 访问者将鼠标指针移动到页面上的某个元素上。
- 7. B. 错误。
- 8. `unload` 事件在访问者离开当前 Web 页面时发生。
- 9. `blur`（失去焦点）事件是 `focus`（聚焦）事件的反面。
- 10. 事件对象包含用于事件的属性和方法。
- 11. 事件的 `type` 属性包含发生事件的类型。
- 12. `submit` 事件在访问者提交 Web 页面上的表单时发生。
- 13. A. 正确。
- 14. 在 9 版本之前的 Internet Explorer 中，可以通过 `window.event` 访问事件对象。
- 15. `addEventListener()` 方法和 `attachEvent()` 方法是注册事件的两种新方式。

## 第 11 章：Node.js 简介

- 1. B. 错误
- 2. `node hello-world.js`
- 3. `const fs = require('fs');`
- 4. 自定义模块允许你定义自己的可重用代码。
- 5. A. `.js`
- 6. B. 错误
- 7. MEAN 栈使用了 MongoDB、Express、AngularJS 和 Node.js。
- 8. B. 错误。
- 9. `pg` 模块可以从 Node 脚本查询你的数据库。
- 10. A. `*`
- 11. `express` 模块可以在 Node.js 中创建 Web 服务器。
- 12. B. 80
- 13. D. `router`
- 14. B. 错误
- 15. A. 你可以使用 `WHERE` 子句仅返回表中符合某些特定条件的行。

## 第 12 章：Math、Number 和 Date 对象

- 1. A. 取字符串的平方根及其他类似值并返回数字。
- 2. `E` 属性存储欧拉常数的值。
- 3. `LN10` 属性存储 10 的自然对数值。
- 4. B. 错误
- 5. C. `document.write(Math.PI);`
- 6. `SQRT2` 属性存储 2 的平方根值。
- 7. C. `absolute`
- 8. B. `asin()` 方法返回作为参数传递的数字的反正弦。
- 9. `pow()` 方法返回第一个参数的第二个参数的幂的数值。
- 10. C. `var rand_int = Math.floor(Math.random() * 8);`
- 11. `sqrt()` 方法返回作为参数传递的数字的平方根。
- 12. D. `Date` 对象的实例
- 13. `getDate()` 方法返回一周中的第几天。
- 14. B. 错误
- 15. B. `var weekday = rightnow.getDay();`

## 第 13 章：处理字符串

- 1. `String` 对象提供了属性和方法，用于获取字符串信息或修改字符串。
- 2. A. 创建 `String` 对象的实例并创建字符串字面量
- 3. 你可以通过给变量赋值字符串值来创建字符串字面量。
- 4. C. JavaScript 获取字符串字面量并转换为临时的 `String` 对象
- 5. C. `length`
- 6. `length` 属性返回字符串的长度。
- 7. B. `var the_text = "Look at me!";`
- 8. B. `charAt()`
- 9. `big()` 方法在字符串值周围添加 `<big>` 和 `</big>` 标签。
- 10. `concat()` 方法将两个字符串拼接。
- 11. `indexOf()` 方法返回字符在字符串中的位置。
- 12. `cookie` 属性存储在文档中。
- 13. `toString()` 方法返回一个字符串。
- 14. 要替换字符串，可以使用正则表达式。
- 15. `match()` 方法将字符串与正则表达式进行比较。

## 第 14 章：基于浏览器的 JavaScript

- 1. 为每个浏览器创建一个文档对象。
- 2. `forms` 数组允许你通过索引数字访问表单。
- 3. B. `document.forms[3]`
- 4. A. `document.forms[2].length`
- 5. C. `document.forms`
- 6. 使用 `names` 或 `ids` 允许你为以后访问的表单命名。
- 7. A. `document.f1.value`
- 8. `action` 属性允许访问起始表单标签中的属性。
- 9. `elements` 属性是一个数组，允许你访问特定表单中的每个元素。
- 10. HTML5 中的 `pattern` 属性允许为表单字段设置正则表达式。
- 11. `reset` 方法允许你使用脚本重置表单。
- 12. C. `<meter name="10" max="8">`
- 13. 提高表单可访问性的方法之一是使用 `<label>` 标签来标识描述的字段。
- 14. `submit` 方法允许在访问者点击按钮的情况下提交表单。
- 15. C. `required`
- 16. B. `XMLHttpRequest`
- 17. AJAX 代表 Asynchronous JavaScript and XML。
- 18. A. 正确
- 19. JavaScript Object Notation 的缩写是 JSON。

## 第 15 章：JavaScript 表单与数据

- 1. 每当你向 HTML 文档添加 `<form>` 和 `</form>` 标签时，就会创建一个表单对象。
- 2. `forms` 数组允许你通过索引数字访问表单。
- 3. B. `document.forms[3]`
- 4. A. `document.forms[2].length`
- 5. C. `document.forms`
- 6. 使用 `names` 或 `ids` 允许你为以后访问的表单命名。
- 7. A. `document.f1.value`
- 8. `action` 属性允许访问起始表单标签中的 `action="url"`
- 9. `elements` 属性是一个数组，允许你访问特定表单中的每个元素。
- 10. HTML5 中的 `pattern` 属性允许为表单字段设置正则表达式验证。
- 11. `reset` 方法允许你使用脚本重置表单。
- 12. C. `<meter name="10" max="8">`
- 13. 提高表单可访问性的方法之一是使用 `<label>` 标签来标识描述的字段。
- 14. `submit` 方法允许在访问者点击按钮的情况下提交表单。
- 15. C. `required`
- 16. B. `XMLHttpRequest`
- 17. AJAX 代表 Asynchronous JavaScript and XML。
- 18. A. 正确
- 19. JavaScript Object Notation 的缩写是 JSON。

## 第 16 章：高级基于浏览器的 JavaScript

- 1. C. `$(document).ready()`
- 2. B. `$("#story").hide();`
- 3. CSS 语法用于在 jQuery 中选择元素。
- 4. jQuery 库使得编写跨浏览器代码变得更容易。
- 5. `<canvas>` 元素允许你使用 JavaScript 在页面的定义区域绘图。
- 6. B. 错误
- 7. 元素的 `draggable` 属性定义元素是否可以被拖动。
- 8. JavaScript 库通过使代码更容易编写，某些高级编码任务变得更容易。
- 9. B. 错误
- 10. `dragstart` 事件在元素开始被拖动时发生。
- 11. B. `event.dataTransfer`
- 12. D. `getData()`
- 13. 任何答案都正确！

## 索引

## A

`Math` 对象中的 `abs()` 方法, 322

`Form` 对象中的 `acceptCharset` 属性, 433

访问

- 数组元素, 167
- 表单, 438–440
- 帧, 420–423
- 网站, 485–489

`Math` 对象中的 `acos()` 方法, 322

`Form` 对象中的 `action` 属性, 433–434

`document` 对象中的 `activeElement` 属性, 224

加加赋值运算符 (`+`), 107–108

`addClass()` 函数, 473–474

`addEventListener` 方法

- DOM 节点, 242
- 事件注册, 272–273, 275–276
- 表单验证, 440–441
- 项目, 278
- `window` 对象, 399

加法运算符 (`+`) 和加法

- 加加赋值运算符, 107–108
- 数组元素, 176–178
- 优先级, 121
- 特殊规则, 100–101
- 字符串, 50–51
- 类型转换, 99–100
- 变量, 98–99

地址, 测试, 370–371

AJAX (异步 JavaScript 和 XML)

- 描述, 456
- 示例脚本, 458–461, 463–465
- 进阶阅读, 461
- `open()` 和 `send()` 方法, 456–457
- `status` 属性, `readystatechange` 事件，以及 `responseText` 属性, 457–458
- `XMLHttpRequest` 对象, 456

`document` 对象中的 `alert()` 方法, 399–400

`alert` 框, 创建, 72–74

路径文本对齐, 497

`document` 对象中的 `all` 属性, 224

变量名中的允许字符, 39–40

在 jQuery 中修改类, 473–475

`&` (符号)

- 位位赋值, 107
- AND 位位运算符, 118
- AND 逻辑运算符, 117, 133–134
- 优先级, 121
- AND 位位运算符 (`&`), 118, 121
- AND 逻辑运算符 (`&`), 117
- 复杂比较, 133–134
- 优先级, 121

匿名函数, 83

APIs

- 循环, 168–169, 171
- `map()` 方法, 183–185
- 方法概述, 173–174
- `<canvas>` 元素, 492–498
- 拖放, 498–503

`Navigator` 中的 `appCodeName` 属性, 215

DOM 节点中的 `appendChild()` 方法, 241–244

`Navigator` 中的 `appMinorVersion` 属性, 215

`Navigator` 中的 `appName` 属性, 214–215

`Navigator` 中的 `appVersion` 属性, 215

路径中的 `arc()` 方法, 496

路径中的 `arcTo()` 方法, 496

`arguments`, 166

函数, 20, 25, 67–69, 76–80

算术运算符

- 加法, 98–101
- 递减, 104
- 除法, 106
- 幂, 103–104
- 取模, 102–103
- 乘法, 101
- 概述, 97
- 减法, 101
- 一元否定, 105–106
- 一元加, 105

`Array.from()` 方法, 174, 187

`Array.isArray()` 方法, 174, 187

`Array.of()` 方法, 174, 187

数组

- 优势, 165
- `concat()` 方法, 179–181
- 构造函数, 165–166
- 定义, 165–167
- 描述, 164
- 元素访问, 167
- `every()` 方法, 183–184
- `filter()` 方法, 183–184
- `find()` 和 `findNext()` 方法, 186
- `flat()` 和 `flatMap()` 方法, 187
- `forEach()` 方法, 183–184
- 表单, 428–421
- 帧, 421–422
- `includes()` 方法, 186
- `indexOf()` 和 `last()` 方法, 182–183
- `join()` 方法, 174–175
- `keys()` 方法, 168–181
- 长度, 168–171
- 字面量表示法, 166–167
- 嵌套, 189–193
- 对象, 202–203
- `pop()` 方法, 175–176
- 属性, 172–173
- `push()` 方法, 176–177
- Q&A, 188
- `reduce()` 和 `reduceRight()`, 185
- `reduce()` 方法, 178
- 自测试, 193–194
- `shift()` 方法, 177
- `slice()` 方法, 183
- `some()` 方法, 183–185
- `sort()` 方法, 178–179
- `splice()` 方法, 181–182
- `toString()` 方法, 185
- `unshift()` 方法, 177–188
- `valueOf()` 方法, 169–170
- `values`, 169–170

赋值运算符 (`=`)

- 加加赋值, 107–108
- 位位, 107
- 直接, 107
- 深度赋值, 109
- 幂赋值, 109–110
- 取模运算符, 106
- 取模赋值, 109
- 优先级, 121
- 减赋值, 108
- 减赋值, 108
- 变量赋值, 36–39
- 乘法运算符, 101
- 乘法赋值, 109
- 优先级, 121

星号 (`*`)

- 注释, 29
- 幂赋值运算符, 109–110
- 查询元素, 472
- 乘法运算符, 101
- 乘法赋值运算符, 109
- 优先级, 121
- 正则表达式, 381

`async` 属性, 标签, 18

异步执行, 模块, 296–298

异步 JavaScript 和 XML (AJAX)

`Math` 对象中的 `atan()` 方法, 322

`Math` 对象中的 `at2()` 方法, 323

`attachEvent()` 方法, 242, 274–276

属性

- HTML, 452
- windows, 408–410

自动完成属性

- `Forms` 对象, 433
- HTML 中的 `autofocus` 属性, 452

大于运算符, 115

不等于运算符, 113

`switch` 语句, 139

正则表达式, 382, 386

- 循环, 156–157
- `switch` 语句, 137
- 溢出帧, 423–424

基于浏览器的 JavaScript

- 可访问性, 485–489
- APIs, 492–503
- 调试, 479–485
- 帧, 420–424
- 图像, 418–420
- Node.js, 503–508
- 安全, 479–485
- 自测试, 424–426, 509–510
- windows. 见 `window` 对象

`\b` 字符

- 退格, 44
- 正则表达式, 382, 386

`History` 对象中的 `back()` 方法, 217

反斜线 (`\`)

- 转义字符, 45
- 正则表达式, 377, 382
- 特殊字符, 43–44

退格

- 正则表达式, 382
- 特殊字符, 44
- 模板字面量中的反引号 (`` ` ``), 52–53

路径测试的基线, 497

- `document` 对象中的 `baseURIObject` 属性, 224
- 路径中的 `beginPath()` 方法, 496
- 路径中的 `bezierCurveTo()` 方法, 496

`Navigator` 中的 `browserLanguage` 属性, 215

浏览器

- 指南, 8
- 查看页面, 26

事件对象中的 `bubbles` 属性, 276

事件冒泡阶段, 274

`Navigator` 中的 `buildID` 属性, 215

表单中的按钮, 439

`\c` 字符在正则表达式, 382

求和代码, 299–300

`call_alert()` 函数, 75–76

回调函数, 297

调用

- 赋值, 107
- 优先级, 121
- 符号, 118

变量数字中的空格, 39–40

函数的块上下文, 89–90

块嵌套

- 循环, `for`, 149–152
- `if/else if/else` 语句, 135–137
- `if/else` 语句中的块结构, 127–129
- 块事件, 263–265, 270–271

`blur` 方法

- DOM 节点, 202
- `window` 对象, 399

`document` 对象中的 `body` 属性, 224

脚本中的 `body` 部分, 72–75

`Boolean` 类型

- 描述, 47
- 等运算符, 112

外部函数, 17, 27

函数, 71

- 来自其他函数的函数, 75–76
- 标签中的函数, 72–75
- 带参数的函数, 76–80
- 带返回语句的函数, 81
- 变量, 50

事件对象中的 `cancelable` 属性, 276

`<canvas>` 元素

- 颜色, 494–495
- 概述, 492
- 路径, 495–497

# 索引 527

- 小于 (is-less-than-equal-to), 116
- 不等于 (is-not-equal-to), 113
- 优先级 (precedence), 121
- 项目 (project), 121–122
- 严格等于 (strict-is-equal-to), 114
- 严格不等于 (strict-is-not-equal-to), 114
- 比较 (comparisons)
  - 数组 (arrays), 179
  - `for` 循环 (for loops), 149
  - `if/else` 语句 (if/else statements), 128–129, 132–134
  - `String` 对象 (String object), 364
  - `document` 对象中的 `compatMode`, 224
  - `Image` 对象中的 `complete` 属性, 418
  - `if/else` 语句中的复杂比较, 132–134

- `concat()`
  - 数组 (arrays), 179
  - `String` 对象 (String object), 362–363

- 拼接 (concatenating)
  - 数组 (arrays), 174–175, 179–181
  - 字符串 (strings), 51–52, 362–363

- 条件运算符 (`?`)
  - 描述 (description), 119
  - 优先级 (precedence), 121
  - 使用 (using), 139–140

- 条件语句 (conditional statements)
  - 优势 (benefits), 127
  - 条件运算符 (conditional operator), 139–140
  - 描述 (description), 126–127
  - `if/else`, 127–137
  - 问答 (Q&A), 14
  - 自测 (self test), 160–161
  - `switch` 语句 (switch statements), 137–139
  - 用户输入 (user input), 140–141

- 循环条件 (conditions for loops), 146

- `method` 对象中的 `confirm()`, 399–401, 406–407

- 用于调试脚本的 `console`, 482–483

- `window` 对象中的 `console` 属性, 393

- `const` 关键字, 90

- 构造函数 (constructors)
  - 数组的 `constructor` 属性, 172
  - 数组 (arrays), 165–166, 190
  - 函数 (functions), 84
  - 对象 (objects), 197–198, 201–206

- 内容 (content)
  - 增强 (enhancing), 488
  - 提供的呈现 (presentation served from), 486–487
  - `document` 对象中的 `contentType` 属性, 224

- 函数中的上下文 (context in functions), 87–91

- 循环中的 `continue` 语句, 156–157

- `+` 转换 (+ conversions)
  - `String` 对象情况 (String object case), 368
  - 类型强制转换 (type coercions), 99–100

- `document` 对象中的 `cookie` 属性, 224, 226

- `Navigator` 中的 `cookieEnabled` 属性, 215–216

- cookies
  - 过期日期 (expiration dates), 373–374
  - 名称 (names), 374–377
  - 获取 (retrieve), 371
  - 读取 (reading), 374–376
  - 设置 (setting), 372–374
  - 用户输入 (user input), 373

- `method` 数组中的 `copyWithin`, 174

- `method` 对象中的 `cos()`, 322

- 循环中的 `count` 变量, 146–147

- `Navigator` 中的 `cpuClass` 属性, 215

- `document` 对象中的 `createElement()`, 241

- `document` 对象中的 `createText()` 方法, 241, 243

- Crockford, Douglas, 462

- 跨站脚本 (XSS), 490–492

- CSS: 级联样式表 (CSS)

- jQuery 中的 `css()` 方法, 471

- 大括号 (`{}`)
  - 块对象 (block object), 89
  - `do while` 循环, 155
  - `for` 循环, 145–149
  - 函数 (functions), 66
  - `if/else` 语句, 128–130, 134–135
  - 对象 (objects), 198
  - 正则表达式 (regular expressions), 381, 384
  - `switch` 语句, 137

- 当前宽度 (current width), 397

- `document` 对象中的 `currentScript` 属性, 224

- `event` 对象中的 `currentTarget` 属性, 276

- 脚本的自定义事件, 284–286

- 自定义 Node 模块, 299–301

# D

- 正则表达式中的 `d` 字符, 382–383

- 数据 (data)
  - AJAX, 456–461
  - JSON, 462–465
  - 自测 (self test), 465–467
  - 数据类型 (data types)
    - 布尔值 (Boolean), 47
    - `null`, 47
    - 数字 (numbers), 41–42
    - 对象 (objects), 48, 196

# JavaScript: 初学者指南

## 定义 (defining)

- 数据类型（续）
  - 字符串 (strings), 42–47
  - 符号 (symbol), 48
  - 类型强制转换 (type coercions), 99–100
  - `undefined`, 47
  - 变量 (variables), 41–48

- Node.js 中的数据库
  - 向添加数据, 308–310
  - 创建, 302–311
  - 安装, 301–302
  - 选项, 302
  - `pg` 模块, 310–311
  - PostgreSQL, 302
  - 查询用户, 307–308
  - 表, 303–306

- HTML5 中的 `datalist` 元素, 446

- 拖拽, 499–500

- `Date` 对象
  - 描述, 340
  - 方法，获取值, 342–344
  - 方法，杂项, 345–346
  - 方法，概述, 342–304
  - 方法，设置值, 345
  - 方法，UTC, 344–355
  - Node.js, 351–355
  - 脚本, 346–351
  - 自测, 355–356
  - HTML5 中的日期类型, 451
  - HTML5 中的 `datetime` 类型, 451

- 脚本调试
  - 浏览器开发者工具, 484
  - `console`, 482–483
  - 错误类型, 479–480
  - lint 工具, 483–484
  - 问答, 485

- 声明 (declaring)
  - 函数, 65–82
  - 变量, 36–37, 49–50, 78
  - `window` 对象中的 `decodeURIComponent()` 方法, 399
  - 递减运算符 (`--`), 104
  - `event` 对象的默认操作, 277
  - `switch` 的默认语句, 137–138
  - `event` 对象中的默认属性, 276
  - `window` 对象中的 `defaultStatus` 属性, 397–398
  - `window` 对象中的默认属性, 224
  - `script` 标签中的 `defer` 属性, 18

- 定义 (defining)
  - 数组, 165–167
  - `document` 对象, 222–223
  - 函数, 66, 82–85
  - 嵌套数组, 189–190
  - 对象, 196
  - 变量, 36–37, 54–55

- 删除运算符 (`delete`), 119

- `document` 对象中的 `designMode` 属性, 224

- DOM 节点中的 `detachEvent()` 方法, 242

- `event` 对象中的 `detail` 属性, 276

- 正则表达式中的数字, 382–383

- `document` 对象中的 `dir` 属性, 224, 226

- HTML5 中的 `dirname` 属性, 452

- 除 (division)
  - 赋值运算符, 109
  - `div` 运算符, 102
  - 双倍运算符, 102–103
  - 优先级, 121
  - `do while` 循环, 154–156

- `document` 对象中的 `document` 属性, 224

- `document` 对象
  - `close()`, 235–237
  - 集合, 225–226
  - cookies, 372–374
  - 定义, 222–253
  - 文档对象模型, 223
  - DOM 节点, 238–247
  - 动态, 247–252
  - 表单, see
  - `getElementById()` 方法, 232–233
  - `getElementsByClassName()` 方法, 233–234
  - `getElementsByName()` 方法, 233–234
  - `getElementsByTagName()` 方法, 234
  - 方法视图, 230–232
  - `open()`, 方法, 235–237
  - 属性, 223–250
  - `querySelector()` 方法, 234
  - `querySelectorAll()` 方法, 234
  - 写入测试, 253–254
  - `write` 方法, 237–338
  - `writeln()` 方法, 237–338

- 文档对象模型 (DOM)
  - `event` 对象层级, 274–275
  - jQuery 元素, 470
  - 节点添加到节点, 246–249
  - 节点方法, 241–246
  - 节点属性, 238–241
  - 目的, 7
  - 使用, 223

- `window` 对象中的 `document` 属性, 393

- `document` 对象中的 `documentElement` 属性, 224

- `document` 对象中的 `documentMode` 属性, 224

- `document` 对象中的 `documentURI` 属性, 224

- `document` 对象中的 `documentURIObject`, 224

- 美元符号 (`$`)
  - 正则表达式, 381, 383
  - 模板字面量, 52
  - 变量名, 39–40

- DOM. 见 文档对象模型 (DOM)

- `document` 对象中的 `domain` 属性, 224

- DOM
  - 数组, 168
  - 命令, 22
  - 对象, 197–200, 205
  - `parseInt()`, 339
  - 正则表达式, 381

- 拖拽 (drag and drop)
  - 事件, 499–500
  - 示例脚本, 500–501
  - 概述, 498–499
  - 项目, 502–503
  - `draggable` 属性, 498
  - 图形上下文, 492
  - 动态脚本
  - 编码, 250–251
  - 事件处理, 249–250
  - 样式, 247–249

## 索引 531

- 页面框架, 54

- 数组中的 `from()` 方法, 174, 187

- `String` 对象中的 `fromCharCode()` 方法, 363–364

- Node.js 文件中的前端代码, 504–508

- `fs` (文件系统) 模块, 295–296

- `fs.mkdir`, 方法, 296

- windows 中的 `fullscreen` 属性, 409

- `document` 对象中的 `fullscreenenabled` 属性, 224

- 函数声明提升, 71

- `function` 关键字, 65

- `document` 对象中的 `getElementsByName()` 方法, 233–234

- `document` 对象中的 `getElementsByTagName()` 方法, 223, 234

- DOM 节点, 242

- DOM 节点中的 `getElementsByTagNameNS()` 方法, 247

- `Date` 对象中的 `getFullYear()` 方法, 344

- `Date` 对象中的 `getMilliseconds()` 方法, 343

- `Date` 对象中的 `getMinutes()` 方法, 343

- `Date` 对象中的 `getMonth()` 方法, 343

- `Date` 对象中的 `getSeconds()` 方法, 343

- `Date` 对象中的 `getTime()` 方法, 344

- `Date` 对象中的 `getTimezoneOffset()` 方法, 344–88

- 正则表达式的全局上下文, 380

- 正则表达式中的全局匹配, 见 windows 和 `window` 对象

- 函数 (functions)
  - 参数, 67–69
  - 箭头, 84–85
  - 优势, 64–65
  - 调用, 71–87
  - 构造函数, 84
  - 声明, 65, 82
  - 已定义, 20
  - 定义, 66, 82–85
  - 描述, 64
  - 执行顺序, 73–74
  - 表达式, 82–84
  - 带有...的 HTML 页面, 86–
  - 命名, 67
  - 问答, 85
  - 返回语句, 69–71, 81
  - 作用域和上下文, 87–91
  - 自测试, 91–93
  - , 90–91

- 函数的全局变量, 77–78

- `History` 对象中的 `go()` 方法, 217

- Google Chrome 浏览器, 4

- Grant Windsor, 307–308

- 图形 (graphics)

```
<element>, 492–498
颜色 (color), 494–495
路径 (paths), 495–498
矩形 (rectangles), 492–494
文本 (text), 497–498
```

- 大于符号 (`>`)
  - 箭头函数, 804
  - 位运算赋值, 107
  - 大于运算符, 114–115
  - 大于等于运算符, 116
  - 优先级, 121
  - 右移运算符, 118

- 正则表达式中的 `g` 标记, 380, 385

- `get_add_text()` 函数, 70, 81

- `get_messages()` 函数, 76

- `document` 对象中的 get 方法, 230–232

- get-monthly-js.code, 299

- DOM 节点中的 `getAttribute()` 方法, 242

- 图形中的 `getContext()` 方法, 492

- `dataTransfer` 中的 `getData()` 方法, 499–500

- `Date` 对象中的 `getDate()` 方法, 343

- `Date` 对象中的 `getDay()` 方法, 343

- `document` 对象中的 `getById()` 方法, 223, 232–233

- 事件处理器, 259

- 表单数组, 431–432

- `document` 对象中的 `getElementsByClassName()` 方法, 233

- 正则表达式分组, 384–387

- DOM 节点中的 `hasAttribute()` 方法, 242

- DOM 节点中的 `hasChildNodes()` 方法, 242

- jQuery 中的 `hasClass()` 方法, 474

- 哈希表, 196

- `document` 对象中的 `hasProperty()` 方法, 208

- `document` 对象中的 `head` 属性, 224

- `script` 中的 `head` 区域, 72–75

## 索引 532 JavaScript：初学者指南

- 高 (height)
  - `Image` 对象, 48
  - windows, 395, 409

- Hello World 脚本, 20–22, 292–294

- `parseInt()` 方法中的十六进制数, 339

- 脚本中的隐藏内容, 279–280

- jQuery 中的 `hide()` 方法, 475

- 隐藏网页源代码, 490

- `History` 对象, 216–218

- `window` 对象中的 `history` 属性, 393

- 悬停图像, 418–420

- HTML 文件
  - 从外部调用脚本, 27
  - 注释, 28–30
  - 创建, 21–24
  - 元素中的事件处理器, 257–258
  - 外部文件, 24–27
  - 知识要求, 3
  - 脚本创建, 20–22
  - 脚本插入, 21–23
  - 脚本加载, 18
  - 脚本标签, 16
  - 自测试, 30–32

- HTML5
  - 属性, 452
  - `<canvas>` 元素, 498–503
  - 拖放, 498–503
  - 元素, 446–450
  - 表单验证, 452–455
  - 输入类型, 450–451

- 超标记语言 (HTML). 见 HTML 文件

- 正则表达式中的 `i` 标记, 380

- 事件处理器中的属性, 259

- `forms` 数组中的 IDs, 431–432

- `if/else` 语句
  - 块嵌套, 120–132
  - 块作用域, 135–137
  - 块结构, 127–129
  - 链式, 135
  - 复杂比较, 132–134
  - 快捷方式, 134–135

- 图像 (images)
  - `Image` 对象, 418–420
  - 随机数, 331–333
  - `document` 对象中的属性, 224
  - 实现属性, `document` 对象, 224

- `in` 运算符, 119

- 数组中的 `includes()` 方法, 174, 186

- 增量运算符 (`++`), 103–104

- 缩进, 130

- 数组元素, 167, 172, 182–183

- `document` 对象, 225–226

- `forms` 数组, 428–429

- 数组中的 `indexOf()` 方法, 182–183

- `String` 对象, 364–366

- 无限循环
  - `for`, 152–153
  - `while`, 154
  - 无大值, 102

- `window` 对象中的 `innerHeight` 属性, 393, 395, 398

- 动态脚本中的 `innerHTML` 属性, 250–251

- `window` 对象中的 `innerWidth` 属性, 393, 395, 398

- 输入 (input)
  - Cookie, 373
  - HTML5 类型, 450–451
  - 提示, 140–141, 143–144
  - 数组的 `input` 属性, 172
  - `document` 对象中的 `Encoding` 属性, 224
  - `insertBefore()` 方法, 241–242

- 安装 (installing)
  - Node.js, 291–295
  - PostgreSQL, 302

- `instanceof` 运算符, 119

- 对象实例, 196, 202–203

- 解释型语言, 329

- 等于运算符, 111–113

- 大于运算符, 114–115

- 大于等于运算符, 116

- 小于运算符, 115

- 小于等于运算符, 116

- 不等于运算符 (`!`), 113

- `isArray()`, 174, 187

- `Math` 对象中的 `isNaN()` 函数, 320

- 数组的迭代函数, 183–185

- Java 编程对比 JavaScript, 6

- `Navigator` 中的 `javaEnabled()` 方法, 216

- JavaScript 对象表示法 (JSON), 462–465

## 索引 533

- JavaScript 概述, 2
  - 客户端和服务端编程, 6–7
  - 环境, 9
  - HTML 和 CSS 知识要求, 3
  - 解释型语言, 9
  - 资源, 10
  - 基于原型的语言, 9
  - 运行, 10
  - 自测试, 11–13
  - 编辑器要求, 3
  - 版本, 5–6
  - 网页浏览器, 3–5
  - 写入文本, 10–11

- `Forms` 对象, 433, 435

- `String` 对象, 360

- `window` 对象, 393, 395

- 小于符号 (`<`)
  - 位对齐, 107
  - 小于运算符, 115
  - 小于等于运算符, 116
  - 左移运算符, 121
  - 优先级, 89–90

- `let` 关键字

- 函数换行, 66

- 路径中的 `lineTo()` 方法, 496

- 链接 (links)
  - `links_alert()` 函数, 76
  - `document` 对象中的 `links` 属性, 224
  - 用于随机数的链接, 334–335
  - 脚本调试工具, 483–484

- 数组的 `join()` 方法, 174–175

- jQuery
  - 修改类, 473–475
  - 效果, 477–478
  - 方法, 475–477
  - 留留, 470–471
  - 问答, 478–479
  - 选择器, 471–473
  - 开始, 483

- 字面量 (literal)
  - 数组, 166–179
  - 对象, 198
  - 字符串, 52–54, 359–360

- `Math` 对象中的 `length` 属性, 319

- 加载事件, 265–268

- 加载脚本, 18

- 局部变量, 77

- `String` 对象中的 `localeCompare()` 方法, 364

- `document` 对象中的 `localStorage` 属性, 393

- JSHint 工具, 483

- JSList

- `location` 属性
  - `document` 对象, 225
  - `window` 对象, 393, 395–396
  - window, 409

# K

- 键盘事件, 269–270

- 数组的 `keys()` 方法, 174, 187

- 关键字, 40–41

- `console` 中的 `log()` 方法, 483

- `Math` 对象中的 `LOG` 属性, 319

- 逻辑错误, 481–482

# L

- `<label>` 标签, 438–439

- `Forms` 对象中的 `labels` 属性, 338

- `language` 属性
  - `Navigator`, 215
  - 标签, 17, 19

- `lastIndexOf()`
  - 数组, 182–183
  - `String` 对象, 364–360, 370–371

- `document` 对象中的 `last` 属性, 224, 226–227

- 左移运算符 (`<<`), 108

- `length` 和 `length` 属性
  - 数组, 166, 178–171
  - `forms` 数组, 429–430
  - AND, 117
  - 位运算, 118
  - OR, 117–118
  - 优先级, 121

- 循环 (loops)
  - 数组, 168–179
  - 优势, 144–145
  - `break` 和 `continue` 语句, 156–157
  - 描述, 144
  - `do while`, 154–156
  - `for`, 143–153
  - `for in`, 156

## 索引 534 JavaScript：初学者指南

- 循环 (续)
  - `for in`, 156
  - `of`, 156
  - 嵌套数组, 190–192
  - 对象, 210–211
  - 事件对象, 276–277
  - `Forms` 对象, 436–437
  - `History` 对象, 217–218
  - jQuery, 475–477
  - `Math` 对象, 321–333
  - `Navigator` 对象, 216
  - `Number` 对象, 337–340
  - 对象, 197–208
  - `String` 对象, 360–369
  - `window` 对象, 399–407

# M

- 正则表达式中的 `m` 标记, 380

- 数组的 `map()` 方法, 183–185

- `match()` 方法
  - 正则表达式, 386–387
  - `String` 对象, 366–367

- 正则表达式中的 `matchAll()` 方法, 386–387

- 正则表达式中的匹配. 见 正则表达式

- `Math` 对象
  - 优势, 318
  - `ceil()` 方法, 327–328
  - 描述, 318
  - `floor` 对象, 328
  - 方法, 321–323
  - `min()` 和 `max()` 方法, 324–345
  - `pow()` 方法, 315–326
  - 属性, 318–320
  - 问答, 333–334
  - `random()` 方法, 328
  - 随机数, 329–335
  - `round()` 方法, 328
  - 自测试, 355–356
  - 双参数方法, 323–324

- `Math` 对象中的 `max()` 方法, 323–325

- `MIN_SAFE_INTEGER` 属性
  - `Number` 对象中, 335

- `Number` 对象中的 `MAX_VALUE` 属性, 335–336

- windows 中的 `menu` 属性, 409

- HTML5 中的 `<meter>` 元素, 446–448

- Microsoft Edge 浏览器, 4

- `Navigator` 中的 `mime` 属性, 215

- `Math` 对象中的 `min()` 方法, 323–325

- `Number` 对象中的 `MIN_SAFE_INTEGER` 属性, 335

- `Number` 对象中的 `MIN_VALUE` 属性, 335–336

- 减号 (`-`)
  - 加法赋值运算符, 108
  - 递减运算符, 104
  - 优先级, 121
  - 减法运算符, 101
  - 一元取反运算符, 105–106

- 修改页面, 56–57

- 取模赋值运算符 (`%=`), 109

- 取模运算符 (`%`)
  - 描述, 102–103
  - 优先级, 121

- HTML5 中的月份类型, 451

- 鼠标事件, 269

- `window` 对象中的 `moveBy()` 方法, 399, 412–416

- `moveTo()` 方法
  - 路径, 496
  - `window` 对象, 399–412

- Mozilla Firefox 浏览器, 4–5

- 正则表达式中的多行, 380

- 函数的多个参数, 69

- 多行注释, 29–30

- 循环中的多语句, 153

- 乘法运算符 (`*`), 101

- 乘法优先级, 121

- 乘法赋值运算符 (`*=`), 109

- `Forms` 对象中的方法属性, 433, 435

- 方法
  - 数组, 173–188
  - `Date` 对象, 340–346
  - `document` 对象, 230–238
  - DOM 节点, 241–246

# N

- 字符
  - 换行符, 44–45
  - 正则表达式, 382

# 索引 535

`name` 属性

- `Forms` 对象, 433, 436
- `Image` 对象, 418
- `window` 对象, 393, 396–397

names

- 数组, 165
- cookies, 374–377
- frames, 222–423
- 函数, 65, 67
- 对象, 196–197

`document` 对象中的 `namespaceURI`, 225

- NaN (非数字)
  - 除法, 102
  - 等于运算符, 112
  - 不等于运算符, 113
  - 乘法, 101
  - 减法, 100–101

`Number` 对象中的 `NaN` 属性, 335–336

- 原生模块, 295–296

- `Navigator` 对象, 214–216

- `window` 对象中的 `navigator` 属性, 393

- `Number` 对象中的 `NEGATIVE_INFINITY`, 335–336

嵌套

- 数组, 189–193
- 条件运算符, 140
- `for` 循环, 149–152
- `if/else` 语句, 129–132
- `while` 循环, 154

`new` 运算符

- 数组, 166
- 对象, 197, 202–203
- 目的, 119

`new` 窗口

- 关闭, 411–412
- 移动, 412–416
- 打开, 408–411
- 调整大小, 416–417
- 滚动, 417

换行符, 44–45

- `function` 对象中的 `newpage`, 236–237

- `node include-express.js`, 299

Node.js 文件

- CSS, 387–388
- 数据库, 301–312
- `Date` 对象, 351–355
- Hello World 脚本, 292–294
- 安装, 291–295
- 介绍, 290–291
- Node, 295–301
- 自测, 315–316
- 服务端, 6–7
- SQL 查询, 312
- 更新, 503–508
- Web 服务器, 313–314

Node

- 异步执行, 296–298
- 原生, 295–296
- 非原生, 298–300

Node 包管理器 (npm), 298–300

- 非原生 Node 对象, 240–343

- `<script>` 标签, 18–19

- 非数字 NaN (Not a Number)

- NOT 位位运算符 (`!`), 118

- NOT 逻辑运算符 (`!`), 118

Notepad 文本编辑器, 3

- HTML5 中的 `validate` 属性, 452

- `Forms` 对象中的 `noValidate` 属性, 433, 436

- npm (Node 包管理器), 298–300

- 函数中的 `null` 参数, 77

- `null` 数据类型, 47

`null` 值

- 等于运算符, 112
- 不等于运算符, 113

`Number` 对象

- 方法, 337–340
- 属性, 335–337
- 自测, 355–356

HTML5 中的数字类型, 451

数字

- 数据类型, 41–42

运算符。参见 算术运算符

对象

- `class` 关键字, 209–210
- 构造函数, 197–198, 201–206
- 创建, 196–201
- `Date`, 340–355
- 定义, 196
- 描述, 48
- `document`. 参见 `document` 对象
- 事件, 274–277

# 536 JavaScript：初学者指南

对象（续）

- `for-in` 循环, 210–211
- `Forms`, 433–437
- `History`, 216–218
- 字面量表示, 198
- `Math`, 318–334
- 方法, 205–208
- 名称, 196–197
- `Navigator`, 214–216
- `Number`, 335–340
- 预定义的, 213–218
- 项目, 212–213
- 基于原型的解释型语言, 9
- 原型, 206–210
- 自测, 218–219
- `String`. 参见 strings 和 `String` 对象
- 结构, 201–206
- `window`. 参见 windows 和 `window` 对象
- `with` 语句, 211

用于数组的 `of()` 方法, 174, 187

`onclick` 事件处理器, 257–258

单行注释, 28

`Navigator` 中的 `OnlineProperty`, 215

在线资源, 10

`open()`

- AJAX, 456–557
- `document` 对象, 235–237
- `window` 对象, 399, 408–411

`window` 对象中的 `opener` 属性, 393, 400

打开窗口, 408–411

算术。参见 算术运算符

赋值, 106–111

比较, 111–116

逻辑, 117–118

运算符优先级, 120–121

自测, 123–124

类型, 96–97

`window` 对象中的 `parent` 属性, 394, 397

括号 (`()`)

- 数组, 166
- 复杂比较, 132–133
- `for` 循环, 146
- 函数, 20, 65–69
- `if/else` 语句, 127–128
- 对象, 205
- 运算符优先级, 120–121
- 正则表达式, 381, 384

`form` 元素和标签, 438–440

复杂比较, 133–134

描述, 117–118

优先级, 121

操作, 120–121

`Navigator` 中的 `cpu` 属性, 215

`window` 对象中的 `outerHeight`, 393

`window` 对象中的 `outerWidth`, 393

HTML5 中的 `output` 元素, 446

页面

- 命令, 55–56
- 创建, 58–59
- 在...上, 346–348
- 定义变量, 54–55
- 框架, 54
- 修改, 56–57
- 保护, 490–492
- 查看, 26
- 写入, 54–60

`document` 对象中的 `parentWindow`, 225

`parse()`, 52

- `Date` 对象, 345
- JSON, 462–463

`Number` 对象中的 `parseFloat()` 方法, 339–340

`Number` 对象中的 `parseInt()` 方法, 339–340

`<canvas>` 元素, 495–497

HTML5 中的 `pattern` 属性, 452, 454

模式匹配

- 正则表达式。参见 正则表达式
- `String` 对象, 366–367

百分比 (`%`)

- 模运算符, 102–103
- 模赋值运算符, 109
- 优先级, 121

`pg` 模块, 310–311

pgAdmin 工具, 302–305

电话验证, 455

`Math` 对象中的 `PI` 属性, 319

HTML5 中的 `placeholder` 属性, 452

变量占位符, 35

纯文本编辑器, 381, 383

`Navigator` 中的 `platform` 属性, 215

属性

- `document` 对象, 225
- `Navigator`, 215–216

加号 (`+`)

- 加赋值顺序, 107–108
- 加法顺序, 98–101
- 增量运算符, 103–104
- 优先级, 121
- 正则表达式, 381
- 字符串, 50
- 一元运算符, 105

数组中的 `pop()` 方法, 175–176

弹出窗口, 407–408

`String` 对象中的位置, 364–366

`Number` 对象中的 `POSITIVE_INFINITY` 属性, 335–336

PostgreSQL 安装, 302

PostgreSQL 数据库

- 添加数据, 308–310
- 创建, 303
- `pg` 模块, 310
- 查询用户, 307–308
- SQL 查询, 312
- 表格, 306

jQuery 中的井号 (`#`), 471

`Math` 对象中的 `pow()` 方法, 320, 323, 325–326

运算符优先级, 120–121

预定义对象, 213–214

- `History`, 216–218
- `Navigator`, 214–216

`document` 对象中的 `prettySheet` 属性, 225

与内容分离的, 486–487

`window` 对象中的 `preventDefault()` 方法, 276–277

`window` 对象中的 `print()` 方法, 399, 401–402

查询用户中的权限, 307–309

`Navigator` 中的 `product` 属性, 215

`Navigator` 中的 `productSub` 属性, 215

HTML5 中的 `progress` 元素, 446, 448–449

`window` 对象中的 `prompt()` 方法, 140–141, 399–400

提示，用户输入, 140–144

数组, 172–173

`document` 对象, 223–230

DOM 节点, 238–241

事件对象, 276–277

`forms` 数组, 429–431

`Forms` 对象, 433–436

`History` 对象, 216–217

`Image` 对象, 418

`Math` 对象, 318–320

`Navigator` 对象, 215–216

`Number` 对象, 335–337

对象, 197–200, 204–205

`window` 对象, 360

`document` 对象中的 `protocol` 属性, 225

基于原型的解释型语言, 9

数组属性, 172

原型对象, 206–210

数组中的 `push()` 方法, 176–177

路径中的 `quadraticTo()` 方法, 496

Query Tool, 303

查询用户, 307–308

`document` 对象中的 `querySelector()` 方法, 234

`document` 对象中的 `querySelectorAll()` 方法, 234

问号 (`?`)

- 运算符, 119, 140
- 优先级, 121
- 正则表达式, 381

引号 (`"`)

- 转义字符, 46–47
- 事件处理器, 257
- 特殊字符, 444
- 字符串, 42–43

随机数字, 330–331

回车符, 44

正则表达式, 382

单选按钮, 439

`parseInt()` 方法中的 radix 值, 339–340

# 538 JavaScript：初学者指南

`random()` 方法, 328–335

随机数字

- 图片, 331–333
- 整数, 329
- 链接, 334–335
- 引号, 330–331
- 脚本, 329

HTML5 中的范围类型, 451

读取 cookies, 374–376

jQuery 中的 `ready()`, 470

`document` 对象中的 `readyState` 属性, 225

AJAX 中的 `readyState`, 457–458

路径中的 `rect()` 方法, 496

矩形, 492–494

数组中的 `reduce()` 方法, 174, 185

数组中的 `Right()` 方法, 174, 185

`document` 对象中的 `referrer` 属性, 225–228

`RegExp` 对象，正则表达式

注册事件, 272–276

正则表达式, 377–338

- 标志, 379–380
- 分组, 384–387
- `match()` 和 `matchAll()` 方法, 386–387
- 模式, 380–386
- `replace()` 方法, 385
- `search()` 方法, 387
- 自测, 389–390
- 字符串, 378–379

关系运算符优先级, 121

剩余对象, 102–103

DOM 节点中的 `removeAttribute()` 方法, 243

DOM 节点中的 `removeChild()` 方法, 243–244

jQuery 中的 `removeClass()` 函数, 473–474

`removeEventListener()` 方法, 243, 273–274

数组元素, 175–177

事件, 273–274

`replace()` 方法

- 正则表达式, 385–386
- `String` 对象, 366

DOM 节点中的 `replace()`, 243

`Forms` 对象中的 `reportValue()`, 436

HTML5 中的 `required` 属性, 452

保留字, 40–41

重置事件, 268

`Forms` 对象中的 `reset()` 方法, 336–437

`window` 中的 `resizable` 属性, 409

`window` 对象中的 `resizeBy()` 方法, 399, 416–417

`window` 对象中的 `resizeTo()` 方法, 399, 416–417

调整窗口大小, 416–417

AJAX 中的 `responseText` 属性, 457–458

函数中的 `return` 语句, 65–79–81

事件对象中的 `returnValue` 属性, 276–277

数组中的 `reverse()` 方法, 178

右移运算符, 118

图片的悬停效果, 418–420

`round()` 方法, 328

# S

正则表达式中的 `s` 字符, 382

HTML5 中的缩放值, 446–448

扫描脚本, 480–481

范围

- 函数, 77, 87–91
- `if/else` 语句, 135–137

`window` 对象中的 `screen` 属性, 394

`script` 标签

- `head` 和 `body` 部分, 72–75
- jQuery, 470
- 使用, 16–20

脚本

- 更改内容, 280–284
- 编码, 250–251
- 创建, 24–26, 27–286
- 自定义事件, 284–286
- `Date` 对象, 346–351
- 调试, 475–483
- 事件处理器, 249–250, 259–260, 278–288
- 隐藏内容, 279–280
- 插入, 21–23
- 用于随机数字, 329
- 样式, 247–249
- 变量, 50–54

`document` 对象中的 `scripts` 属性, 225

`window` 中的 `scrollbars` 属性, 409

`window` 对象中的 `scrollY()` 方法, 399, 417

滚动窗口, 417

`document` 对象中的 `scrollingElement` 属性, 225

DOM 节点中的 `scrollInto()` 方法, 243

`window` 对象中的 `scrollLeft()` 方法, 399, 417

# 索引 539

安全, 489–492

`Navigator` 中的 `securityPolicy` 属性, 215

`document` 对象中的 `selectedStylesheet` 属性, 225

选择器

```
jQuery, 471–473
styles, 248
```

`window` 对象中的 `self` 属性, 394, 397

分号 (`;`)

- cookies, 372
- `do while` 循环, 155
- 事件处理器, 258
- 函数, 65, 82
- 语句, 20–21
- 变量赋值, 38
- 变量声明, 36

AJAX 中的 `send` 方法, 456–457

分隔符

- cookie, 372, 374
- `split()` 方法, 367
- 服务端编程, 6

DOM 节点中的 `setAttribute` 方法, 243

`dataTransfer` 对象中的 `setData` 方法, 499

`window` 对象中的 `setDate` 方法, 345

`document` 对象中的 `setFill` 方法, 345

`document` 对象中的 `setHours` 方法, 345

`document` 对象中的 `setInterval` 方法, 399, 403–404

`document` 对象中的 `setMinutes` 方法, 345

`document` 对象中的 `setMonth` 方法, 345

`window` 对象中的 `setTimeout`, 345

`document` 对象中的 `setTime` 方法, 345

`window` 对象中的 `setTimeout` 方法, 399, 403–404

`document` 对象中的 `setTimeOffset`, 345

`document` 对象中的 `setUTC` 方法, 345

数组的 `shift` 方法, 177

移运算符

- 优先级, 121
- 符号, 118

`if` 语句中的短路, 134–135

`show_message()` 函数, 73–74

jQuery 中的 `show()` 方法, 475–476

有符号右移运算符 (`>>`), 118

简单文本编辑器, 3

`Math` 对象中的 `sin()` 方法, 322

窗口大小, 416–417

`slice` 方法

- 数组, 181
- `String` 对象, 363

jQuery 中的 `slideDown()` 方法, 475–476

jQuery 中的 `slideToggle()` 方法, 475

jQuery 中的 `slideUp()` 方法, 475–476

Socket.io 引擎, 290–291

数组的 `some()` 方法, 174, 183–185

数组的 `sort()` 方法, 178–179

源代码

- 隐藏, 490
- `Number` 对象, 338

空格

- cookies, 372
- 缩进, 130
- 字符串, 51
- 变量名, 39–40

特殊字符, 43–45

特殊运算符, 119

`window` 对象中的 `split()` 方法, 366–373

SQL 查询, 312

`Math` 对象中的 `sqrt()` 方法, 322

`Math` 对象中的 `SQRT1_2` 方法, 319

`Math` 对象中的 `SQRT2` 方法, 319

方括号 (`[]`)

- 数组, 166–187
- 对象, 199–200
- 正则表达式, 381

`src` 属性

- `Image` 对象, 418
- `script` 标签, 17

事件对象中的 `srcElement` 属性, 276

`status` 属性

- AJAX, 457–458
- `window` 对象, 394–398
- window, 409

`window` 对象中的 `stop()` 方法, 399

事件中的 `stopImmediate()` 方法, 276

事件中的 `stopPropagation()` 方法, 276

严格相等运算符 (`===`), 114

严格不等于运算符 (`!==`), 114

JSON 中的 `stringify()` 方法, 462

字符串和 `String` 对象

- addition 对象, 100–101
- case, 368
- `charAt()` 和 `charCodeAt()` 方法, 360–361
- `concat()` 方法, 362–363
- 连接, 51–52, 363
- cookies, 371–377
- `Date` 对象, 346

# JavaScript: 入门指南。字符串和 `String` 对象 (续)

- 定义, 20
- 描述, 42
- 转义字符, 45–47
- `fromCharCode()` 方法, 363–364
- `indexOf()` 方法, 364–366
- 严格相等运算符, 112
- 大于运算符, 115
- `lastIndexOf()` 方法, 364, 370–371
- `length` 属性, 360
- 字面量, 359–360
- `localeCompare()` 方法, 364
- `match()`, `replace()`, 以及 `search` 方法, 366–367
- 方法概述, 361
- `Number` 对象, 338–339
- 概述, 358
- 问答, 369–370
- 引号, 42–43
- 正则表达式。*参见*正则表达式
- self, 389–390
- `slice()` 方法, 363
- 特殊字符, 43–45
- `split()` 方法, 366–367
- 严格相等运算符, 114
- vs. 字符串方法, 359–360
- `substring()` 方法, 363
- 模板字面量, 52–54
- `toLowerCase()` 和 `toUpperCase()` 方法, 368
- `toString()` 方法, 368
- `trim()` 方法, 364–369
- 变量, 50–sec

路径中的 `stroke()` 方法, 496

矩形的 `strokeRect()` 方法, 492–493

矩形的 `strokeStyle` 属性, 494–495

路径中的 `strokeText()` 方法, 497

对象的结构, 201–206

样式, 247–252

`document` 对象中的 `styleSheets` 属性, 225

Sublime 代码编辑器, 3

事件, 268

`Forms` 对象中的 `submit()` 方法, 436–437

`String` 对象中的 `substring()` 方法, 363

减法

- 优先级, 121
- 减赋值运算符 (`-=`), 108
- 减法运算符 (`-`), 101

`switch` 语句, 137–138

- 表达式, 139
- 穿透, 138

符号值, 48

语法错误, 479–480

`Navigator` 中的 `systemLanguage` 属性, 215

字符

- 正则表达式, 382
- 制表符, 43–44

tab 字符

- 函数, 66
- 缩进, 130
- 正则表达式, 382
- 特殊字符, 43–44

表格, 203, 306

`Math` 对象中的 `tan()` 方法, 322

`target` 属性

- 事件对象, 276
- `Forms` 对象, 433, 436

HTML5 中的 `type`, 451

字符串的模板字面量, 52–54

临时运算符, 140

`RegExp` 对象中的 `test()` 方法, 378–380

`<canvas>`, 497–498

字符串。参见字符串和 `String` 对象

写入, 110

`text_alert()` 函数, 79

文本编辑器

- 引导线, 7–8
- 要求, 3

路径文本中的 `textAlign` 属性, 497

路径文本中的 `textBaseline` 属性, 497

`document` 对象中的 `textContent` 属性, 225

文本编辑器, 3

严格相等运算符

- 对象, 202–203
- is, 119

波浪号 (`~`)

- 位运算符, 118
- 优先级, 121

`Date` 对象, 344

- 对象, 344
- 页面, 346
- 事件, 265–268
- 事件, 346
- 事件, 348

`String` 对象中的 `substring()` 方法, 363

减法

- 优先级, 121
- 减赋值运算符 (`-=`), 108
- 减法运算符 (`-`), 101

`switch` 语句, 137–138

- 表达式, 139
- 穿透, 138

符号值, 48

语法错误, 479–480

`Navigator` 中的 `systemLanguage` 属性, 215

`toLowerCase()` 和 `toUpperCase()` 方法, 368

`toString()` 方法, 368, 364–369

无符号右移运算符 (`>>>`), 118

`toUpperCase()`, 368

`Number` 对象, 338–339

概述, 358

问答, 369–370

引号, 42–43

正则表达式。*参见*正则表达式

self, 389–390

`slice()` 方法, 363

特殊字符, 43–45

`split()` 方法, 366–367

严格相等运算符, 114

vs. 字符串方法, 359–360

`substring()` 方法, 363

模板字面量, 52–54

`toLowerCase()` 和 `toUpperCase()` 方法, 368

`toString()` 方法, 368

`trim()` 方法, 364–369

变量, 50–sec

路径中的 `stroke()` 方法, 496

矩形的 `strokeRect()` 方法, 492–493

矩形的 `strokeStyle` 属性, 494–495

路径中的 `strokeText()` 方法, 497

对象的结构, 201–206

样式, 247–252

`document` 对象中的 `styleSheets` 属性, 225

Sublime 代码编辑器, 3

事件, 268

`Forms` 对象中的 `submit()` 方法, 436–437

`String` 对象中的 `substring()` 方法, 363

减法

- 优先级, 121
- 减赋值运算符 (`-=`), 108
- 减法运算符 (`-`), 101

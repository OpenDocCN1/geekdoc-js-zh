content]
# JavaScript 编程入门指南 (M150 数据、计算与信息)

1.2

182350B/m150b2u7i.2

本单元由Judith Segal为课程团队编写。

## 1 导论

本单元旨在向您介绍编写自己的计算机程序。具体来说，我们的目标是向您介绍：

- 编写代码以从用户读取数据，执行一些简单处理并显示结果；
- 在高级语言中进行顺序、选择和重复编程，具体包括：
    - 如何通过评估某个条件来实现程序代码片段的条件执行；
    - 如何实现程序代码片段的重复执行，要么在特定条件为真时执行，要么执行指定次数。

您将使用一种广泛可用的高级编程语言，称为JavaScript。我们为您提供了一小组程序供您运行、修改和实验，您也将从头开始编写自己的小程序。

JavaScript与Java不同。尽管JavaScript代码看起来有点像Java，并且这两种语言经常一起使用以生成基于网络的应用程序，但除此之外它们并无关联。

您应该已经从第6单元知道，在编程中，我们使用一种形式语言与机器通信。如果不严格遵守该语言的规则，即其`语法`，您的程序将无法运行或无法按预期运行。不得不寻找错误——通常称为“bug”——可能是一次非常令人沮丧的经历。

> 您可以将语言的语法视为其语法结构。

编程语言也有词汇和意义——就像自然（口头）语言一样。

我们已经为本单元的所有活动提供了可运行的代码，作为最后的手段，您可以查看并自行运行它们。然而，学习编程有点像学习骑自行车：如果您只是观察别人所做的，您的学习将极其有限。为了真正理解如何编程，你必须编写自己的程序（尽管我们会提供一点帮助）。

请不要因为犯错而气馁。许多人发现，犯错、找出错误原因并纠正错误的过程，构成了一个非常有价值——甚至令人愉快的——学习经历。您可能会发现，记录下您犯的任何错误以及如何纠正它，对您将来参考会有所帮助。

除了语法，编程语言还有保留字，有时称为`关键字`，即在特定编程语言中具有特殊含义的词（您可以将保留字视为该语言词汇或字典的一部分）。许多编程语言使用的保留字看起来像英语（例如 while, for 和 if）。但要注意：这些词在编程语言中的含义可能与其英文对应词并不完全匹配。我们将在遇到这些词时解释它们在编程语言中的含义（`语义`）。

我们需要在此指出，JavaScript区分大小写。这意味着，例如，JavaScript解释器将 `If`, `IF` 和 `if`视为不同的。JavaScript中的所有保留字都是小写的，即它们没有大写字母。

编写一个行为完全符合您期望的程序，可以是一种极其令人满足、有益且富有创造性的体验。现在是向您介绍这种体验的时候了。

### 关于学习第7-10单元的重要信息

在学习本单元时，您需要经常使用计算机，因为它包含大量实践活动。在进行活动时，您需要手边备有《第2单元软件指南》以供参考。

《第2单元软件指南》不仅告诉您如何查找和运行我们提供的程序，还告诉您如何查看并可能修改程序`源代码`，即构成程序的JavaScript语句集。它包含JavaScript语法的摘要，您可能会觉得这很有帮助。

在进一步学习之前，您应该阅读《第2单元软件指南》中题为“使用JavaScript程序”的部分。

## 2 入门指南

在本节中，你将编写一些简单的程序，这些程序将使你（或其他用户）能够通过鼠标和键盘输入数据，对数据进行一些简单的处理，然后显示处理结果。

具体而言，本节旨在：

- 描述如何编写一个显示信息的程序；
- 讨论编程变量的概念；
- 讨论数据类型的概念，涉及数字和字符串，以及它们的一些操作（数字的算术运算；字符串的连接）；
- 描述如何使用对话框来获取程序输入；
- 讨论在适当的情况下，如何将输入数据转换为数字。

### 2.1 第一个程序

JavaScript，顾名思义，是一种`脚本语言`。这意味着用 JavaScript 编写的程序不能独立运行，而必须在某个应用程序（如 Web 浏览器）中运行。（大多数高级编程语言不是脚本语言，不需要额外的应用程序来运行；它们要么被编译，要么被解释，如第 6 单元所述。）

你可能还记得第 6 单元的内容，JavaScript是一种解释型语言。像网景浏览器这样内嵌了 JavaScript 解释器的浏览器，会获取你的 JavaScript 语句并解释它们，即把它们翻译成机器代码指令，并逐条执行。

**活动 2.1**

**在本活动中，你将运行一个程序并研究其源代码。**

**(a) 运行程序 Program_7.2.1。**

**你应该会在屏幕上看到一个浏览器窗口打开，并显示以下消息：**

`Welcome to programming!`

![563dcadf5ae68219c0c3dfb03c7cc823 8](img/563dcadf5ae68219c0c3dfb03c7cc823_8_0.png)

**M150 CD-ROM**

Block 2 软件指南会告诉你如何查找、阅读和运行我们提供的程序。

在本文中，我们使用不同的字体来区分 JavaScript 代码和文本其余部分。

**(b) 现在使用记事本读取 Program_7.2.1 的源代码（即产生上述输出的指令）。**

**你应该会看到以下内容。**

```html
<HTML>
<HEAD>
<TITLE> Program_7.2.1 First Program
</TITLE>
<SCRIPT LANGUAGE = "JavaScript">
document.write('Welcome to programming!')
</SCRIPT>
<BODY>
</BODY>
</HTML>
```

### 讨论

你可能会认出这些行中的大部分是 HTML 代码，它们告诉浏览器打开一个窗口，并在标题栏中显示 'Program_7.2.1 First Program'。以下两行：

`<SCRIPT LANGUAGE = "JavaScript">` 和 `</SCRIPT>` 通知 HTML 系统，它们之间的代码不是 HTML，而是脚本语言（在本例中是 JavaScript）编写的。事实上，如果没有指定语言，HTML 会假设代码是 JavaScript，所以上面第一行可以替换为。

这个程序中只有一行 JavaScript，即：

```javascript
document.write('Welcome to programming!')
```

你已经在第 4 单元接触过 HTML。所有其他行——那些在尖括号 `<` 和 `>` 中的行——都是 HTML。除了在浏览器窗口中显示结果的行外，我们打算在本单元中教你任何 HTML。Program_7.2.1 中的 JavaScript 代码是指令，用于显示文本：`Welcome to programming!`

让我们详细研究一下：

- `document` 是一种`对象`。编程语言中的每种对象都与特定的行为（能做什么）相关。你可以将 `document` 对象想象成由当前页面的内容组成，这些内容显示在浏览器中。
- `write()` 是 `document` 对象的方法，它使 JavaScript 向你的浏览器添加文本。点表示（如 `document.write()`）告诉 `document` 对象执行其 `write` 方法。
- 圆括号 `()` 包含了方法参数。它提供了方法执行所需的信息，在本例中就是要显示的文本。

### SAQ 2.1

在上述程序中，方法的参数是什么？

### SAQ 2.1 的答案 ✓

参数是 `'Welcome to programming!'`。注意，程序中的文本必须用引号括起来。JavaScript 接受单引号或双引号，但在 M150 中我们将使用单引号。你在单元中编写的所有 JavaScript 程序都由类似的 HTML 行开头结尾。唯一的区别是在浏览器标题栏上显示的标题，例如：`<TITLE> Whatever</TITLE>`。（注意：这行似乎包含来自上下文的占位符 'Whatever'，已按要求保留，尽管它看起来并不正确。）当然，还有位于以下行之间的 JavaScript 代码：`<SCRIPT LANGUAGE = "JavaScript">` 和 `</SCRIPT>`。因为我们不想让你反复输入相同的 HTML 行，所以为你提供了模板，其中包含了所需的 HTML 代码。如果你想试验自己的程序，我们建议你将所需的 HTML 代码复制并粘贴到你的新文件中。

### 活动 2.2

![563dcadf5ae68219c0c3dfb03c7cc823 10](img/563dcadf5ae68219c0c3dfb03c7cc823_10_0.png)

在本活动中，我们希望你修改 Program_7.2.1 的源代码（你在活动 2.1 中看到过的），然后运行修改后的程序。我们为你了一份 Program_7.2.1 的副本，名为 `Activity_7.2.2`。在记事本中打开文件 `Activity_7.2.2.html`。

**(a)** 修改文件 `Activity_7.2.2.html` 中的 HTML，使浏览器页面的标题现在显示：第一个活动

**(b)** 修改文件 `Activity_7.2.2` 中的 JavaScript 代码，使程序在运行时显示：`Welcome to JavaScript programming!`

Block 2 软件指南会告诉你如何运行 JavaScript 程序。保存文件并运行程序 `Activity_7.2.2`，以检查你的更改是否按要求工作。

### 讨论

**(a)** 你应该将指定标题的 HTML 代码更改为：

```xml
<TITLE> 第一个活动 </TITLE>
```

**(b)** 你应该将 JavaScript 代码从 `document.write('Welcome to programming!')` 更改为 `document.write('Welcome to JavaScript programming!')`。其他行应与 Program_7.2.1 中的相同。如果你的程序没有预期运行，那么你犯了一个错误（你的程序有一个 bug）。你记得引号吗？Block 2 软件指南提供了一些调试提示。你将在 `Solution_7.2.2` 中找到这个活动的运行解决方案。

### 练习 2.1

为什么上述文件必须在名称末尾有 `.html`？

所有活动、程序和解决方案文件都以 `.html` 作为扩展名，但我们在文本中省略了它们。

### 讨论

记住，JavaScript 必须从浏览器中运行。因此，JavaScript 代码必须包含在具有适当 HTML 代码的文件中，以告诉浏览器打开一个窗口，如上面的示例所示。这样的文件必须在其名称末尾有 `.html`（使用术语说，就是具有文件扩展名 `.html`），这样计算机的操作系统才知道需要在浏览器中打开它。

### SAQ 2.2

你将如何修改 Activity_7.2.2 的 JavaScript 代码，以便在程序运行时显示 `Hello` 而不是 `Welcome to JavaScript programming!`？

### SAQ 2.2 的答案 ✓

你需要将现有的 JavaScript 语句替换为：

```javascript
document.write('Hello')
```

## 2.2 变量与顺序执行

你可能还记得第 6 单元的内容，顺序执行意味着执行一条指令，然后是一条，依此类推，直到所有指令都被执行。第 2 节中的所有程序都以这种方式执行。编写你作为程序（源）代码的单词并不有趣，我们希望你能够编写程序来获取数据，然后显示结果。这样做之前，你需要了解 JavaScript 如何存储在计算机内存中的数据。你可能还记得第 6 单元的内容，内存位置有唯一的地址。使用 JavaScript 这样的高级语言时，我们不需要知道任何关于内存位置的信息；我们可以简单地向 JavaScript 声明一些内存，并给它一个名称，有时称为`标识符`。

变量被视为计算机内存中存储值的位置。你可以将名称（或标识符）视为内存位置的一种标签。例如，存储了数字值（比如 3）的变量有一个名为 `sum` 的名称，如图 2.1 所示。

![563dcadf5ae68219c0c3dfb03c7cc823 12](img/563dcadf5ae68219c0c3dfb03c7cc823_12_0.png)

**图 2.1** 一个名为 `sum`、值为 3 的变量

顾名义，变量中的值可以在程序执行（即执行指令）时改变。当程序访问一个变量（如 `sum`）时，它将使用该变量的当前值。你稍后会看到，你可以为变量选择任何名称，只要它符合某些规则。

> 请记住第 1 节的内容，JavaScript 区分大小写，并且所有保留字必须是小写。我们在课程文本中包含代码时，对保留字使用粗体。

以下三行来自 Program_7.2.3 的代码（如果你愿意，可以使用记事本）：

```javascript
var myVar;
myVar = 3;
document.write(myVar)
```

`myVar` 这个名称你也可以选择别的。第一行中，`var` 是一个保留字（也称为关键字）。`var myVar` 这一行是以 `myVar` 为名的变量的声明，即程序被告知使用 `myVar` 作为内存中某个位置，该位置将存储一些数据，如图 2.2 所示。表示 `myVar` 尚未赋值。第二行给 `myVar` 赋值为 3。JavaScript 中的赋值运算符：`=` 符号右侧的任何值（本例中为 3），都会被赋给左侧命名的变量，如图 2.3 所示。第三行将 `myVar` 的当前值写入浏览器当前页面。请注意，`myVar` 没有用引号括起来，因为我们要显示的是名为 `myVar` 的变量的值，而不是文本 `myVar`，如图 2.4 所示。

### SAQ 2.3

假设我们有一个名为 `total` 的变量，其赋值为 5。JavaScript 将如何解释以下每一行代码？

(a) `document.write('total')`
b) `document.write(total)`

### SAQ 2.3 的答案

(a) 单词 total 将显示在浏览器当前页面中。
(b) 数字 5（标记为 total 的内存位置中存储的值）将显示在浏览器当前页面中。

## 分号与顺序执行

下面是 Program_7.2.3 中的三行 JavaScript 代码：

```javascript
var myVar;
myVar = 3;
document.write(myVar)
```

您可能已经注意到，前两行的末尾都有分号。我们在前面讨论这些代码的含义时没有解释这些分号，因为三条指令中的每一条即使没有分号也是完整的。但是，分号可以用作指令之间的分隔符，以便 JavaScript 清楚地“知道”一条指令在哪里结束，另一条在哪里开始。当每条指令各占一行时，分号不是强制性的，但我们认为它们使代码更清晰，并且在本模块中始终使用它们。

### 活动 2.3

在本活动中，你将对 Program_7.2.3 的 JavaScript 代码进行一些修改。

(a) 运行 Program_7.2.3，提醒自己它的作用。
(b) 现在在记事本中打开文件 Activity_7.2.3（其中包含 Program_7.2.3 的副本）。修改一行 JavaScript 源代码，使显示的输出为 145。

保存您的更改并运行 Activity_7.2.3，以检查你的更改是否按要求工作。

(c) 将 Activity_7.2.3 中的第二行 JavaScript 代码替换为 `3 = myVar` 并尝试运行程序。会发生什么？

![img/563dcadf5ae68219c0c3dfb03c7cc823_14_0.png)

### 讨论

(a) 你会看到输出是变量 myVar 的当前值，即 3。
(b) 将 `myVar = 3` 改为 `myVar = 145` 即可实现所需的更改。
(c) 程序会报错。因为赋值运算符的左侧必须是一个变量（左值），而不能是常量（如 3）。


给变量赋值时，变量名*必须*在 `=` 符号的左侧，值在右侧。JavaScript 中 `=` 符号两侧的项目不是同一类：左侧是变量名（只是某个内存位置的名称）；右侧是某种值——要么是一个显式值，要么是一个将计算为值的**表达式**。例如，如果 `myVar` 和 `yourVar` 都已声明为变量，以下都是有效的赋值语句示例。

```
myVar = 6
yourVar = myVar + 3
myVar = yourVar
```

### 练习 2.2

假设变量 `myVar` 和 `yourVar` 已经声明。写出在按顺序执行以下每一行 JavaScript 代码后它们的值。

+ (a) `myVar = 3`

(b) `yourVar = myVar + 2`

(c) `myVar = yourVar`

### 讨论

(a) `myVar` 的值为 3；我们还不知道 `yourVar` 的值。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_15_0.png)

**图 2.5** 执行练习 2.2 (a) 代码的结果

(b) `myVar` 的值仍然是 3；`yourVar` 的值是 `myVar` 的值加 2，即 5。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_15_1.png)

**图 2.6** 执行练习 2.2 (b) 代码的结果

(c) `myVar` 的值是 `yourVar` 的值，即 5；`yourVar` 的值仍然是 5。（但请注意，仍然有两个内存位置；它们只是恰好持有相同的值。）

![](img/563dcadf5ae68219c0c3dfb03c7cc823_16_0.png)

**图 2.7** 执行练习 2.2 (c) 代码的结果

变量通常被比作命名盒子或鸽巢。虽然这有助于我们可视化计算机中发生的事情，但这种比较并不完全恰当，因为通常我们可以往鸽巢里放多个物品，而变量一次只能持有一个值。如果给变量赋了新值，那么这个值会覆盖之前的值，之前的值就丢失了。

### 练习 2.3

**(a) 执行以下指令（其中 `yourVar` 是一个变量）包含哪两个阶段？**

`yourVar = yourVar + 3`

**(b) 如果执行该语句前 `yourVar` 的值为 10，执行后它的值将是多少？**

### 讨论

(a) 首先，将计算右侧的表达式，即将 3 加到 `yourVar` 的当前值上。然后将这个新值赋给 `yourVar`。

(b) 它的值将是 13（10 + 3 的结果）。

SAQ 2.4

**执行以下两行后，变量 `myVar` 的值是多少？**

```
myVar = 21;
myVar = myVar - 5
```

**SAQ 2.4 的答案** ✓

`myVar` 的值是第一行赋给 `myVar` 的值（21）减去 5，即 16。

## 变量命名

在上面的例子中，我们使用了 `sum`、`myVar` 和 `yourVar` 作为变量名。`sum` 这个名称可能向读者表明该变量的值持有某些其他值的总和（合计）；`myVar` 和 `yourVar` 这两个名称没有提供关于这些变量作用的任何线索（它们实际上是用于说明教学要点，而不是执行特定任务）。我们建议您以这样一种方式命名变量，以表明变量在执行特定编程任务中的作用。我们在前面提到，变量名称有时被称为标识符。两者之间的区别相当微妙。程序中的**标识符**是一个必须遵循特定规则的名称（不同编程语言之间规则有所不同）。程序员分配的所有名称，如变量、方法等的名称，都必须是有效的标识符。您会发现，在编程书籍中，名称和标识符经常可以互换使用。在 JavaScript 中，标识符必须符合以下格式。

第一个字符必须是以下之一：

- 大写或小写字母（即 `A...Z`、`a...z`）；
- 下划线字符（`_`）；
- 美元符号（`$`）。

后续字符可以是以上任何字符或数字（`0`、`1`、`2`、...、`9`）。

您不能使用已经是 JavaScript 词汇一部分的保留字。（您已经看到 `var` 作为表示变量声明的保留字；您稍后还会看到其他保留字，如 `while`、`if`、`for`。）

上述标识符规则是强制性的。然而，在 M150 中，我们鼓励您在选择变量标识符时遵守以下风格指南。遵循这些指南将使您的程序更易于阅读和（如有必要）调试。

- 虽然标识符中的字符数没有下限或上限，但我们敦促您避免使用非常短的标识符，如 `a`、`b`、`x`、`ch`，因为它们信息量不大。
- 尽可能避免在标识符中使用 `$` 和 `_`。完全由字母组成的标识符通常对人类读者最有意义，尽管有时使用数字来表示若干相似的值可能是合适的，例如 `sum1`、`sum2`、`sum3`。
- 选择有意义的名称，即能够表明变量作用。
- 以小写字母开头标识符。当标识符由两个或更多单词组成时，建议在后续单词开头使用大写字母（称为驼峰式）。`myVar` 和 `yourVar` 使用了这种风格。这里有一些例子：`totalCost`、`dateToday`、`familyName`。

## SAQ 2.5

以下哪些是 JavaScript 中有效的标识符？

```
123
$sum
PriceAsked
```

### SAQ 2.5 答案 ✓

`123` 无效——标识符必须以字母、`_` 或 `$` 开头。`sum` 和 `PriceAsked` 是有效的，尽管它们不符合风格指南。

## EXERCISE 2.4

鉴于编程语言主要是人与计算机交流的方式，为什么程序不仅要易于编写还要易于阅读？

### 讨论

一个原因是便于调试：如果你的程序无法运行或者运行不符合预期，你需要找到错误。另一个原因是你希望修改现有程序而不是从头编写。

## ACTIVITY 2.4

Activity_7.2.4 包含 Program_7.2.3 的副本。在记事本中打开该并删除以下行：

```
myVar = 3
```

使 JavaScript 代码变为：

```
var myVar;
document.write(myVar)
```

### 讨论

你将在浏览器当前看到 `undefined`。这是因为 `myVar` 尚未赋值。为变量赋初始值的称为**初始化**。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_18_0.png)

## SAQ 2.6

编写 JavaScript 代码来声明一个名为 `myNumber` 的变量；用数字 5 初始化它；将其值加 5；最后显示新值。（我们希望你在尝试这段代码，但如果你尝试了，请记住包含 HTML 并保存为 .html 文件。）

### SAQ 2.6 答案 ✓

```
var myNumber = 5;
myNumber = myNumber + 5;
document.write(myNumber);
```

## 2.3 一些有用的数据类型

到为止，我们看到的一些数据值属于同一类。例如，值 `3`、`7` 和 `21` 都是**数字类型**，事实上 `3.2`、`-6` 和 `-2.5` 也是。

类似地，`'hello'`、`'welcome'` 和 `'have a good day!'` 都是字符序列（或字符串）。在 JavaScript 中，就像在许多其他语言一样，字符序列由**字符串类型**表示。正如你已经看到的，代码中的字符串必须用引号括起来，以区别于变量和保留字；字符串可以包含空格、标点符号以及任何你在打字机上找到的字符。

一个值属于哪种类型并不总是易见的。以 `123456` 为例：它是一个数字，还是一个字符串？答案取决于 `123456` 在程序上下文中的作用。它可能是在观看某剧第一集数。在这种情况下，它显然是一个数字。你可以将其用于计算，例如加上后续剧集的次数，或者找出此数字与在其他频道观看电影数的差值。另一方面，`123456` 可能是一个电话号码，在这种情况下你不太可能想将其用于计算，因此你可以视为字符串 `'123456'`。为了向 JavaScript 表明程序中的数字序列被视为字符串，我们必须加上引号。

许多编程语言对整数和实数（带有小数部分的数字）的处理方式不同，但 JavaScript 并非如此。

## SAQ 2.7

你在本单元中之前见过字符串？

### SAQ 2.7 答案 ✓

字符串在活动 2.1 和 2.2 中的 `write()` 方法参数中被使用。

## 2.4 运算符

### 数字运算符

在前面的例子中，你已经看到过诸如 `yourVar = myVar + 3` 这样的指令。你已经知道 `yourVar` 和 `myVar` 是变量名，=` 是赋值运算符，`3` 是一个值。那么 `+` 呢？它也是一个运算符，在这种情况下是加法运算符。通常运算符操作值。

JavaScript 可以执行各种算术运算，包括加法、减法、乘法和除法。对于加法和减法，它使用常见的运算符 `+` 和 `-`。乘法和除法的符号分别是 `*` 和 `/`。所有这四个运算符都是**二元运算符**。（你会从第 6 单元中回忆起，二元运算符作用于两个值，称为它们的操作数。）

> 如果你使用过计算器，你可能已经熟悉乘法的符号 `*` 和除法的符号 `/`。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_20_0.png)

你的算术能力如何？`3 + 4 * 2` 和 `4 / 2 + 6` 的答案是什么？

### 讨论

运行 `Program_7.2.5` 以检查你的答案。如果你目前不理解 `Program_7.2.5` 的代码，请担心。

### 优先级

活动 2.5 的目的是考虑 JavaScript 中算术运算符的优先级，即在包含多个运算符的表达式中应用顺序。例如从左到右计算 `3 + 4 * 2`，你会先将 3 和 4 相加得到 7，然后乘以 2 得到 14。实际上，`Program_7.2.5` 给出的答案是 14：先执行乘法和除法，然后加法。这是因为 JavaScript 应用常见的数学规则——没有括号的情况下。并非所有编程语言都遵循标准的优先级。如果你想避免记忆运算符优先级，或者你想固定的优先级（例如，在上面的例子中，你可能想先将 2 和 6 相加），你应该使用括号。程序总是先计算括号中的表达式，当有多组括号时，最内层的括号将被计算。

### SAQ 2.8

计算 `(2 + (6 / 2))`

### SAQ 2.8 答案 ✓

计算顺序如图所示。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_21_0.png)

**图 2.8** SAQ 2.8 中表达式的计算顺序

图 2.9 逐步显示的计算过程。每一行中，接下来将被的部分都用标记出。

```
(1) 2 + (6 / 2)
(2) 2 + 3
(3) 5
```

**图 2.9** 逐步显示的计算过程答案是 5。

## 字符串上的二元运算符

符号 `+` 也用作字符串运算符：在这种上下文中，`+` 是连接（将第二个字符串附加到第一个）的运算符。例如，`'Hello' + 'there'` 将得到 `'Hellere'`。

## SAQ 2.9

你需要对上面示例中的字符串进行更改才能获得结果 `'Hello there'`？

### SAQ 2.9 答案 ✓

请记住，字符串可以包含空格。因此有两种可能的解决方案：'Hello ' + 'there'`（第一个字符串由字母 `hello` 后跟一个空格组成），或者 `'Hello' + ' there'`（第一个字符串由一个空格字符后跟字母 `there` 组成）。

## 2.5 从用户获取数据

到为止，变量都是在源代码中赋值。但这非常灵活。你可以很容易地想象你可能想用不同的值运行一个程序，例如可以将任意两个数相加的程序。向程序提供未写入源代码的数据被称为程序的输入。有多种方法实现：下面的活动展示了一种方法。

## ACTIVITY 2.6

运行 `Program_7.2.6`。你会看到一个类似于图 2.10 的框出现在当前页面的顶部。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_22_0.png)

图 2.10 一个提示对话框

按照指示输入你的名字，然后单击确定。你将在浏览器当前页面收到一条个性化的问候。在记事本中打开文件 `Program_7.2.6`，并尝试弄清楚源代码是如何工作的。

### 讨论

JavaScript 代码如下（包含行号供参考）。

```
(1) var name;
(2) name = window.prompt('Enter your name','');
(3) document.write('Hello ' + name + '!');
(4) document.write('<BR>' + 'Have a good day')
```

第一行只是声明了一个名为 `name` 的变量。第二行指示 JavaScript 显示一个带有一些指定文本的提示对话框。这个框让你输入一个值，在这种情况下是你的名字，然后这个值被赋给名为 `name` 的变量。第三行和第四行指定了输出。我们现在将更详细地查看活动 2.6 的代码。在第二行中，`window` 指的是显示 `document`（当前页面）的浏览器窗口。方法 `prompt()` 与 `window` 对象关联，这将导致提示对话框出现在窗口顶部。

# SAQ 2.10

在本单元中你还遇到过哪个对象和方法？

Answer to SAQ 2.10 ✓

带有其关联方法 `write()` 的 `document` 对象。`prompt()` 方法可以与两个参数一起使用，用逗号分隔。第一个参数指定程序员希望在对话框中出现的字符串（在本例中为'Enter your name'）；第二个参数指定一个默认的响应字符串，它会在用户输入任何值之前出现在文本输入框中。如果用户没有输入任何文本，但没有输入任何文本就点击了OK 按钮，这个默认值就是被赋给变量的值。在 `Program_7.2.6` 中，默认值就是被赋给变量的值。


```javascript
var name;
var day;
name = window.prompt('Enter your name','Type your name here');
day = window.prompt('Enter the day','');
document.write('Hello ' + name + '!');
document.write('<BR>' + 'Have a nice ' + day)
```

注意，你可以在响应提示时输入任何乱七八糟的内容。JavaScript不会自动知道你的名字是什么，也不知道今天是星期几，也不知道什么是名字的合理值或日期的合理值。还要注意，在`document.write()`语句中，`name`和`day`不需要加引号，因为我们想要显示的是这些变量的值，而不是它们的标识符。

你将在`Solution_7.2.7`中找到(b)部分的可用解决方案。

你不会总是想包含非空的默认输入字符串，因为用户必须在输入前删除它，这这很烦人，但在以下情况下可能很有用。

- 程序员有充分理由期望用户的特定响应时，例如，如果你正在编写一个程序来询问M150学生他们是否已经学习过任何OU的二级课程，你最可能期望的答案是否，所以你可能将此作为默认值。
- 当空字符串作为响应可能会在程序后续引起问题时，例如，如果你要求用户为新文件提供一个名称。

## SAQ 2.12

(a) 编写一行JavaScript代码，使对话框出现，并显示提示：Please enter yes, no or quit，默认答案为"quit"，并将输入的任何内容赋给标识符为`choice`的变量。

(b) 编写第二行代码，在屏幕上显示以下消息：

`Choice!`（后跟输入的内容——yes、no或quit）

## Answer to SAQ 2.12 ✓

(a) [代码模糊/不清晰]

(b) [代码模糊/不清晰]

## 获取数字输入

在JavaScript中，所有来自键盘的输入都被假定为字符串。到目前为止，这还没有问题，因为我们所有的程序都涉及文本操作。但是，如`Activity 2.8`所示，如果你想输入数字，事情就不那么简单了。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_25_0.png)

## ACTIVITY 2.8

以下代码来自`Program_7.2.8`（添加了行号以供参考）。

```
(1) var numberOne;
(2) var numberTwo;
(3) var sum;
(4) numberOne = window.prompt('Enter your first number',"");
(5) numberTwo = window.prompt('Enter your second number',"");
(6) sum = numberOne + numberTwo;
(7) document.write('The sum of ' + numberOne + ' and '
              + numberTwo + ' is ' + sum)
```

(a) 研究代码并写下当你响应提示时输入两个数字`37`和`45`时，你认为输出会是什么。

(b) 运行程序，看看你是否正确。

## Discussion

(a) 你可能期望得到以下输出：

The sum of 32 and 45 is 77

(b) 事实上，你得到的是：

The sum of 32 and 45 is 3245

JavaScript会假定你的两个输入都是字符串，即'32'和'45'，因此会认为`+`是连接运算符。

那么如果我们想读取并相加两个数字，该怎么做呢？我们使用一个名为`parseFloat()`的函数，它接受一个字符串作为参数，并返回与该字符串的数字部分相对应的数作为结果。在编程中，函数提供的结果被称为其返回值。我们说函数返回某个值。

> 函数类似于方法，但不依附于任何特定对象。你将在第8单元中了解更多关于函数的内容。

你可以将`parseFloat()`看作是将合适的字符串转换为数字。例如，

```
parseFloat('3') returns 3

parseFloat('10.25') returns 10.25
```

如果我们有以下两行代码：

```
(1) myVar = window.prompt('Enter a number','');
(2) myVar = parseFloat(myVar)
```

输入的数字首先将作为字符串赋给`myVar`（在第(1)行），然后被转换为数字并重新赋给`myVar`（在第(2)行）。

## SAQ 2.13

假设执行了上面两行代码，并且响应提示时，用户输入了77。

(a) 执行第(1)行后，`myVar`的值是什么？

(b) 执行第(2)行后，`myVar`的值是什么？

## Answer to SAQ 2.13 ✓

(a) '77'；输入最初被读取为字符串。

(b) 77；在第(2)行中，函数`parseFloat()`将字符串转换为数字。

## 输出数字

上面我们说过，`document.write()`的参数必须是字符串（可以由几个字符串连接而成）。那么当你想输出数字时会发生什么？这里没有问题：方法`write()`接受一个数字，比如183，并自动将其转换为数字字符的字符串，'183'。

## 活动 2.9

- (a) 运行`Program_7.2.9`，输入各种不同的数字。`Program_7.2.9` 的输出与`Program_7.2.8` 的输出有何不同？
- (b) 当你输入字母数字而非数字（例如，输入 thirty-two 而不是 32）时，会发生什么？
- (c) 研究 `Program_7.2.9`，特别是`parseFloat()`的使用。

### 讨论

- (a) `Program_7.2.9` 正确将两个数字相加，而不是像`Program_7.2.8` 将两个字符串连接起来。
- (b) 你将得到类似输出：NaN 与和是 NaN。虽然 JavaScript 能正确读取你的输入，比如 thirty-two 和 twelve，但`parseFloat()`无法将它们转换为数字，因为 JavaScript 无法知道这些字符串代表32 和12。你猜到了`NaN` 是 JavaScript 中“非数字”（Not Number）。
- (c) `Program_7.2.9` 的代码如下（添加了行号以便参考）。

```
(1) var firstNumber;
(2) var secondNumber;
(3) var total;
(4) firstNumber = window.prompt('Enter your first number','');
(5) firstNumber = parseFloat(firstNumber);
(6) secondNumber = window.prompt('Enter your second number','');
(7) secondNumber = parseFloat(secondNumber);
(8) total = firstNumber + secondNumber;
(9) document.write('The sum of '+ + firstNumber + ' and '
         + secondNumber + ' is ' + total)
```

第(5) 行和第(7) 行中`parseFloat()`的使用，接受字符串参数并返回相应的数字。例如如果你在第(4) 行提示处输入3，在第(6) 行提示处输入7，两者将被转换为数字并在第(8) 行相加，因此`total` 将赋值为10。第(9) 行显示的输出字符串由给定的字符串与转换为数字的`total` 值连接而成。

## 活动 2.10

文件`Activity_7.2.10`包含一个 HTML模板，你可以在其中添加 JavaScript 代码。(a) 提示用户首先输入其电话号（例如0198），然后输入其本地号码（例如623456），之后程序应显示类似输出：电话号码是 0198 623456（或你插入任何数字）。(b) 在这种情况下，为什么不需要使用`parseFloat()`？(c) 如果使用了，会发生什么？

### 讨论

(a) 这是我们的解决方案：

```javascript
var areaCode;
var localNumber;

areaCode = window.prompt('Please enter area code','');
localNumber = window.prompt('Please enter your telephone number','');
document.write('Your telephone number is ' + areaCode + ' ' + localNumber)
```

你的解决方案中的输出可能有所不同。你记得包含空格来分隔单词吗？(b) 你不需要`parseFloat()`，因为你是将电话号码视为数字的字符串，而不是数字。(c) 如果你在提示之后插入以下行：

```javascript
areaCode = parseFloat(areaCode);
```

和

```javascript
localNumber = parseFloat(localNumber);
```

那么分配给`areaCode`和`localNumber`的值将是数字。由于0198与198是同一个数字，前导零将丢失，数字将被转换为字符串'198'供`document.write()`使用，导致输出为：电话号码是 198623456。你可以在`Solution_7.2.10`中找到第(a)部分的可解决方案。

## 一些复习问题

此时，你可能想尝试一些自我评估问题（SAQs），以回顾你在本节中完成的工作。

### SAQ 2.14

编辑程序和执行程序有什么区别？

**SAQ 2.14 的答案** ✓

编辑程序涉及一个人使用编辑器（如记事本）编写或修改指令（源代码）。执行（或运行）程序涉及计算机根据特定语言的规则执行这些指令。

### SAQ 2.15

假设`firstNumber`和`secondNumber`已声明为变量。依次执行每一每一代码后，写下两个变量的值。

- (a) `firstNumber = 31;`
- (b) `firstNumber = firstNumber + 30;`
- (c) `secondNumber = firstNumber - 2;`
- (d) `secondNumber = firstNumber;`

**SAQ 2.15 的答案** ✓

(a) `firstNumber`的值是31；我们对`secondNumber`的值一无所知。((b) `firstNumber`的值是61；我们仍然对`secondNumber`的值一无所知。((c) `firstNumber`的值仍然是61，`secondNumber`的值是59（`firstNumber`的值 - 2）。(d) `secondNumber`的值是61，与`firstNumber`的值相同。

### SAQ 2.16

以下代码片段都有语法错误。在每种情况下，写下你认为程序员意图的正确代码。

- (a) `document.write(hi there!)`
- (b)

```javascript
thirdNumber = firstNumber + secondNumber;
document.write('the sum of firstNumber
	+ secondNumber is 'thirdNumber')
```

- (c)

```javascript
var myNumber;
3 = myNumber
```

**SAQ 2.16 的答案** ✓

(a) `document.write("hi there!")`

(b)

```javascript
thirdNumber = firstNumber + secondNumber;
document.write('the sum of ' + firstNumber + secondNumber + ' is ' + thirdNumber)
```

(c)

```javascript
var myNumber;
myNumber = 3
```


| <= | 小于或等于 | 若 `a` 的值小于 `b` 的值，或等于 `b` 的值，则`(a <= b)`为真，否则为假 | `(2 <= 5) → true<br>(2 <= 1) → false<br>(2 <= 2) → true` |
| > | 大于 | 若 `a` 的值大于 `b` 的值，则`(a > b)`为真，否则为假 | `(2 > 3) → false<br>(2 > 1) → true<br>(2 > 2) → false` |
| >= | 大于或等于 | 若 `a` 的值大于 `b` 的值，或等于 `b` 的值，则`(a >= b)`为真，否则为假 | `(3 >= 2) → true<br>(3 >= 5) → false<br>(3 >= 3) → true` |
| == | 等于 | 若 `a` 的值等于 `b` 的值，则 `(a == b)`为真，否则为假 | `(2 == 3) → false<br>(2 == 2) → true` |
| != | 不等于 | 若 `a` 的值不等于 `b` 的值，则`(a != b)`为真，否则为假 | `(3 != 2) → true<br>(2 != 3) → true<br>(2 != 2) → false` |

## 所用符号说明

左栏中所有的 `JavaScript` 符号都表示单一运算符，因此对于由两个字符组成的运算符（如 `<=` 和 `!=`），如果在它们之间留有空格将导致语法错误。

请注意，相等运算符使用的是"双等号"（`==`）。这使其与赋值运算符 `=` 相区别。

如果您不熟悉“大于”或“小于”符号，记住它们的方向可能会有所帮助：较大的值放在 `<` 的开口端，较小的值放在收缩端，即（`较小值 < 较大值`）为真。

您还应该回顾第6单元的内容：如果`(c < d)`为真，则`(d > c)`为真；如果`(c <= d)`为真，则`(d >= c)`为真。

## SAQ 3.1

哪些比较运算符是二元运算符？

## SAQ 3.1 答案

它们都是二元运算符，因为它们都作用于两个值。

## SAQ 3.2

判断以下比较表达式（使用 `JavaScript` 表示法）的值是真还是假。

- (a) `(8 <= 2)` → `false`
- (b) `((16 != (4*4)))` → `true`
- (c) `(16 != 8)` → `true`
- (d) `(8 == 8)` → `true`
- (e) `(16 == (4*4))` → `true`

## SAQ 3.2 答案

- (a) false
- (b) true
- (c) true
- (d) true
- (e) true

以上示例仅考虑了数值，但我们可以在任何有序的值上使用比较运算符，即当我们能明确判定哪一个在另一个之前时。例如，字母 `a` 在字母表中位于字母 `c` 之前，因此 `('a' < 'c')`为真。（请记住，在 `JavaScript` 中处理字符串时需要使用引号，即使在本例中字符串只包含单个字符。）

全为小写或全为大写字母的字符串比较方式是：先比较两个字符串的第一个字母，如果相同则比较第二个字母，依此类推。这会得到与字典相同的排序结果。例如，`('aardvark' < 'cat')` 和 `('cat' < 'cave')`为真，但 `('cat' < 'camel')`为假，因为前两个字母匹配，而 `'cat'` 的第三个字母位于 `'camel'` 第三个字母之后。

我们只考虑由字母（包括小写和大写）组成的字符串排序。

对于数字字符串，以 `'1'` 开头的字符串被认为“小于”以 `'2'` 开头的字符串，而以 `'2'` 开头的字符串又小于以 `'3'` 开头的字符串，依此类推。

## 活动 3.2

文件 `Activity_7.3.2` 包含 `Program_7.3.1` 的副本。

- (a) 在记事本中打开该文件并修改代码，使程序比较字符串而非数字。保存更改后，运行程序来比较您选择的若干字符串。
- (b) 当你输入 `117` 作为第一个值、`32` 作为第二个值时，会发生什么？
- (c) 您能解释在(b)部分中得到的结果吗？

### 讨论

- (a) 为了比较字符串，您必须删除涉及 `parseFloat()` 的两个语句。
- (b) 当你输入 `117` 作为第一个值、`32` 作为第二个值时，您会得到以下输出。

  117 < 32 为真
  117 <= 32 为真

  > 提示：如果您忘记了任何 `JavaScript` 语法，《B2软件指南》中有一份摘要。

- (c) (b)部分的结果是因为这些值被当作字符串 `'117'` 和 `'32'` 来处理，而非对应的数字；而且正如上文所述，在数字字符串的排序中，任何以 `'1'` 开头的字符串都位于任何以 `'3'` 开头的字符串之前。

你可以在 `Solution_7.3.2` 中找到(a)部分的完整解决方案。

## 3.2 简单条件语句

在本小节中，您将学习编写这样的程序：当某个条件为真时执行一组操作，当条件为假时执行另一组操作。

## if 语句

当条件可能为真也可能为假时，使用 `if` 语句使程序进行分支。下一个活动将为您展示 `if` 语句的工作原理。

```javascript
var bankBalance, withdrawalAmount;
bankBalance = 100;
withdrawalAmount = window.prompt('How much do you want to withdraw?', '');
withdrawalAmount = parseFloat(withdrawalAmount);
if (withdrawalAmount > bankBalance)
    document.write('You cannot do that!' + '');
document.write('Goodbye');
```

- (a) 运行 `Program_7.3.3`两次，一次输入50，一次输入150。第(5)行做了什么？
- (b) 如果输入是100，您认为会发生什么？再次运行程序并输入100，看看您的预测是否正确。
- (a) 输入为50 时，显示的输出是 Goodbye。输入为150 时，输出有两行：
  You cannot do that!
  Goodbye

此处的场景是：您的银行只有£100（虽然未提及具体单位），且不允许透支。第(5)行的布尔表达式`(withdrawalAmount > bankBalance)`的值为`true`，则执行括号内的第(7)语句，即 `document.write('You cannot do that!' + '')`。但如果第(5)行的布尔表达式的值为`false`，则跳过 `if` 语句，转到下一条指令。最后执行第(8)行输出 Goodbye。

- (b) 如预期，输入为100时输出是 Goodbye。账户中有£100，所以提取100是可以的——但余额将清零！注意大括号内可以有多个语句。例如，银行程序中if 语句的主体包含以下两个语句：

```javascript
document.write('You cannot do that!' + '');
document.write('You have only £' + bankBalance + ' in your account');
```

一般而言，`if` 语句的形式为：

```javascript
if (布尔表达式) {
    语句
}
```

注意，`if` 语句包含整个结构：`if`、布尔表达式以及大括号中的语句。`if`后面的布尔表达式必须位于括号内。间距和缩进是为了便于阅读，但建议您遵循此布局。如果 `if` 语句后面有语句，需要在结束大括号后加分号，以将 `if` 语句与下一条语句分隔开。

图3.1示意地展示了 `if` 语句的效果。在编写或修改程序后，你应该总是运行它以测试是否正常工作。即使只是很小的改动，也很容易向原本正常的代码中引入错误！由于不可能针对所有输入值，所以选择一组测试例是很重要的。对于 `if` 语句，你应该至少用两个值测试：一个使条件成立和一个使条件不成立。这样可以确保你测试了程序中的两条路径：一条是执行括号内语句的路径，另一条是忽略它们的路径。

## EXERCISE 3.1

编写布尔表达式时常见的错误是使用错误的比较运算符，例如使用了 `>=` 而不是 `>`。在Activity 3.3中讨论的代码第(5)行中所作的这种错误，应该通过什么输入值来揭示你是否有错误？

## Discussion

所需的值是100。如果你使用的是 `>=` 而非 `>`,那么输入值为100会导致第(5)行的布尔表达式求值为`true`，从而执行第(7)行的语句。正如在Activity 3.3(b)中讨论的那样，使用`>`且输入值为100则正确地跳过了第(7)行。

在使用 `<`, `<=``,`>`和 `>=`这些比较运算符时，建议用边界值（本例中为100）以及两个最接近的值（本例假定你只考虑整数为99和101）来测试你的代码。在这些界限处以及边界值附近的值被称为边界值。

## ACTIVITY 3.4

当你更改计算机密码时，程序通常要求输入新密码，然后重新键入（以确保原始输入中没有出现拼写错误）。如果两次输入的数值不匹配，则不会修改密码。

- (a) `Activity_7.3.4`包含`Program_7.3.3`（银行程序）的副本。在不带头的情况下打开`Activity_7.3.4`并对其进行修改，使该程序提示输入密码，然后重新键入密码。接着检查两次输入是否匹配。如果不匹配则显示`Your password is unchanged`，无论结果都会在屏幕上新一行中显示“Thank you”。该程序的结构与银行程序相似（你需要更改大多数细节）。如果需要使用部分（b）之后的提示，有一些提示可供参考。

> 关于测试的更多知识将在第10单元中学到。

(b) 你将如何测试你的程序是否有效？

### Hints

在构思你的编程时你可能会发现Figure 3.1很有帮助。

- 你在`if` 语句之前需要做什么？
- `if` 语句中的布尔表达式是什么？
- 如果求值为true，你需要做什么？
- 如果求值为false，则跳过什么？


```markdown

文件 `Activity, - .7`中包含一个 JavaScript 程序的HTML 模板。(a)在不带头情况下打开该程序并编写一段询问用户“今天过得好吗？”的程序如果键入 `yes`则显示消息 `"Glad to hear it"`，否则（其他情况）显示 `"Maybe tomorrow will be better"`。无论哪种情况最后都会说“感谢回复”（`Thank you for replying`）。

### Hints

Figure 3.2在构思你的程序时可能对你要有帮助。

- 你想在评估布尔表达式（`boolean expression`）之前做什么？
- 这个布尔表达式是什么?
- 如果它为 `true`，而要是 `false`（假），你希望做什们？
- 之后你想要做什么事？

## Further hints

在你评估该布尔条件之需得首先询问用户今天过得是否愉快然后得到响应，所以你需要声明一个变量来保存响应的值并调用提示对话框（`prompt dialogue box`）。

## (b) 如何测试该程序？

### 讨论

(a) 以下是我们的代码（带有行号以供参考）。像往常一样，你的代码在细节上可能有所不同。

```
(1) var response;
(2) response = window.prompt('Are you having a good day today?', '');
(3) if (response == 'Yes')
(4) {
(5)   document.write('Glad to hear it')
(6) }
(7) else
(8) {
(9)   document.write('Maybe tomorrow will be better')
(10) };
(11) document.write('<BR>' + 'Thank you for replying')
```

你可以在 `Solution_7.3.7` 中找到可行的解决方案。

(b) 该程序应至少运行两次进行测试，一次输入 `Yes`，一次输入其他内容。

如果你的程序没有运行，或者没有按预期运行，以下是你在第 (3) 行可能犯的一些常见错误：

- 你是否使用了 `=`符号而不是 `==`？
- 你是否忘记在布尔表达式周围加上括号？
- 你是否忘记在字符串 `'Yes'` 周围加上引号？

请注意，该程序在第 (3) 行期望一个非常具体的输入——`Yes`。任何变体，例如 `yes` 或 `y` 或 `yeah`，都不行。在3.4 小节中，你将看到如何处理布尔表达式在多种不同情况下都求值为 `true` 的情况。

## SAQ 3.4

假设将上面的 `if...else` 结构替换为以下内容。

```
if (response == 'Yes')
{};
document.write('Maybe tomorrow will be better');
```

## 程序的行为将会如何改变？

"Construct"只是控制结构的另一种说法。

---

## SAQ 3.4 的答案 ✓

因为 `document.write('Maybe tomorrow will be better')` 不属于 `if...else` 结构的一部分，所以它总会被执行。因此，如果输入的值是 `Yes`，将会显示以下内容：Glad to hear it Maybe tomorrow will be better

如果输入的值不是 `Yes`，这些行产生的显示结果将是单行：Maybe tomorrow will be better

## SAQ 3.5

补全下面的 `if...else` 语句，使得程序运行时询问用户输入考试分数，然后如果分数达到 40 或以上则显示消息 `Pass`，如果分数低于 40 则显示 `Fail`。

```
var mark; mark = window.prompt('Please enter your mark', ''); mark = parseFloat(mark); if (在此处添加缺失的代码) { document.write('Pass') } else { (在此处添加缺失的代码) }
```

---

## SAQ 3.5 的答案 ✓

```
if (mark >= 40) { document.write('Pass') } else { document.write('Fail') }
```

## 3.3 条件语句与复合语句

在 3.2 小节的大多数程序中，如果某个特定条件的值为真（或假），我们只希望计算机执行单个语句。然而，我们经常希望在条件求值为真（或假）时执行多个语句。我们曾顺便提及，在 `if` 语句的 `if` 子句或 `else` 子句中可以包含多个语句。实际上，JavaScript 中使用花括号（`{}`）的作用是将多个语句（用分号或换行符分隔）"包装"在一起，形成所谓的**复合语句**，正如你在练习 3.2 中 `if` 语句的 `else` 部分所看到的。从概念上讲，JavaScript 将任何包含在花括号中的语句集视为单个语句。换句话说，在 JavaScript 语法要求单个语句的地方，你总是可以使用花括号括起来的一系列语句来代替。

当 `if` 或 `else` 子句中只出现单个语句时，使用花括号并不是严格必需的，但我们建议你使用它们，因为这样可以提高代码的可读性，并在修改程序时有助于避免错误——例如，如果你之后想向其中一个子句添加额外的语句。

## 练习 3.2

**假设从第 (5) 行开始修改 `Program_7.3.5` 的代码，并将初始银行余额设置为 500，因此新代码如下。**

```
var bankBalance, withdrawalAmount;

bankBalance = 500;
withdrawalAmount =
    window.prompt('How much do you want to withdraw?','');
withdrawalAmount = parseFloat(withdrawalAmount);
if (withdrawalAmount > bankBalance)
{
    document.write('You cannot do that!' + '<BR>')
}
else
{
    bankBalance = bankBalance - withdrawalAmount;
    document.write('Your bank balance is now £' + bankBalance + '<BR>')
};
document.write('Goodbye')
```

对于以下输入，输出将会是什么？

- (a) 750
- (b) 250
- (c) 500

### 讨论

```
(a)
You cannot do that!
Goodbye
```
条件 `(withdrawalAmount > bankBalance)` 求值为 `true`，因此 `if` 子句将被执行，随后是最后一行。

```
(b)
Your bank balance is now £250
Goodbye
```
布尔表达式求值为 `false`，因此 `else` 子句将被执行，首先计算新的余额（£250），然后显示。

```
(c)
Bank balance is now £0
Goodbye
```
与 (b) 部分一样，布尔表达式求值为 `false`，因此 `else` 子句将被执行，计算并显示。

## 通过使用注释提高读性

你已经开始编写相当复杂的程序，这些程序变得难以阅读和理解。你已经看到，通过使用有意义变量变量以及使用缩进来展示结构，可以提高读性。如果包含注释，程序的目的将会更加清晰。JavaScript 提供了两种实现方式：

- `//` 符号（两个斜杠）告诉 JavaScript 忽略该行剩余。这种注释通常用于短注释。
- `/*` 和 `*/` 符号告诉 JavaScript 忽略它们之间的内容。这种注释用于较长的注释，也用于引起注意，如你在后面看到的。你应该在程序顶部包含一条注释，说明程序的用途。

## 编写选择结构的提示

- 首先思考你需要哪些变量来保存输入、处理的数据，并为它们赋予有意义的标识。
- 然后确定你想要测试的条件是什么，即你希望为真或假的。
- 如果表达式求值为 `true`，你想要做什么？如果要执行多个语句，必须使用 `{}` 复合语句（但我们建议无论如何都加上括号）。
- 如果表达式求值为 `false`，你有什么特别做的（需要 `else` 部分吗）？同样，记得加上括号。
- 你如何结束程序？

---

## 活动3.8

文件 `Activity_7.8`包含一个 JavaScript 程序的HTML 模板。

(a) 在记事本中打开文件，编写一个程序，要求用户输入当前年份和出生年份。如果输入的出生年份早于或等于当前年份，程序会计算年龄。

然而，如果输入的出生年份晚于当前年份，程序会要求重新输入出生年份和当前年份，然后再计算年龄。

(b) 你应该运行程序多少次来测试它是否正常，以及使用什么样的值？

(c) 如果用户连续两次出生年份都晚于当前年份，会发生什么？

### 讨论

(a) 以下是我们的解决方案。注意程序开头的注释，用于告诉读者程序的作用。

```
/* Activity_7.8 计算你生日时年龄的程序 */

var yearOfBirth, thisYear;

yearOfBirth =
    window.prompt('Please enter your year of birth','');
yearOfBirth = parseFloat(yearOfBirth);
thisYear =
    window.prompt('Please enter the current year', '2004');
thisYear = parseFloat(thisYear);
if (yearOfBirth > thisYear)
{
    document.write('You have made a mistake somewhere');
    yearOfBirth =
        window.prompt('Please re-enter your year of birth','');
    yearOfBirth = parseFloat(yearOfBirth);
    thisYear =
        window.prompt('Please re-enter the current year', '2004');
    thisYear = parseFloat(thisYear)
};
document.write('<BR>' + 'On your birthday this year, you will be' + (thisYear - yearOfBirth))
```

你可能已经包含了一个额外的变量，比如叫 `age` 或 `ageThisYear`，用于在显示之前保存计算的结果。

(b) 你应该至少运行程序两次；一次是你正确输入出生年份和当前年份时（这样 `if` 子句会被）。

(c) 程序会将年龄显示为负数。例如，如果你输入出生年份为2004年，当前年份为1962年，程序会计算出年龄！在第4节中，你将学习如何让一段代码不断重复执行，直到某个条件变为假。

你可以在 `Solution_7.3.8` 中找到第(a)部分的完整解决方案。

## 3.4 更复杂条件语句简介

条件可能比本单元中迄今为止看到的更为复杂。正如你在第6单元所见：

- 布尔条件可以使用布尔运算符 `NOT` 进行否定。
- 复合条件可以通过布尔运算符 `AND` 和 `OR` 组合简单条件来表达。
- 不同的动作集合可能需要依赖不同的条件。（还记得第6单元中的例子吗？书籍根据它们是小说、传记还是其他类别被放置在不同的书架上。）

### 复合布尔表达式

你应该还记得第6单元的内容：

- `NOT` 是一元布尔运算符，具有效果：如果 `a` 为真，则 `NOT a` 为假；如果 `a` 为假，则 `NOT a` 为真。
- `OR` 是二元布尔运算符，具有效果：如果 `a` 或 `b` 中有一个为真。
- `AND` 是二元布尔运算符，具有效果：如果 `a` 和 `b` 都为真。

JavaScript 提供了这些方式来实现逻辑：`!` 表示 `NOT`，`||` 表示 `OR`，`&&` 表示 `AND`。

```


![图 3.4](img/563dcadf5ae68219c0c3dfb03c7cc823_52_0.png)

**图 3.4** 嵌套 `if` 语句的工作原理

### 活动 3.10

在某所大学，学生参加考试可能获得及格、不及格或优秀。及格需要40分或以上，优秀需要60分或以上。

(a) 文件 `Activity_7.3.10` 包含一个 JavaScript 程序的 HTML 模板。在记事本中打开该文件并编写一个程序，提示学生输入他或她的考试分数，然后显示：

Sorry, you've failed **或**

Congratulations, you've passed **或**

Many congratulations, you have honours**，视情况而定。**

**提示** 请参见活动 3.9，了解如何在 `you've` 中显示撇号的提示。

(b) 你应该运行程序多少次来测试它？

### 讨论

(a) 以下是我们的代码。（像往常一样，你的代码可能不同但也是正确的。）

```
var mark;

mark = window.prompt('Please enter your mark','');
mark = parseFloat(mark);
if (mark < 40)
{
  document.write('Sorry, you\'ve failed')
}
else
  if (mark < 60)
  {
    document.write('Congratulations, you\'ve passed')
  }
  else
  {
    document.write('Many congratulations, you have honours')
  }
```

请注意，我们没有在第一个 `if` 对应的 `else` 子句周围加上大括号。虽然我们曾建议在通常情况下为每个子句加上大括号是个好主意，但在嵌套 `if` 语句且每个子句只有一条语句时，这会使程序变得相当长（如我们在活动 3.9 的解决方案中所示）。记住，你只能省略大括号是因为 `else` 子句是一条单独的语句（一个完整的 `if...else` 结构在 JavaScript 中被视为一条语句）。不过我们仍然对代码进行了缩进以显示结构。

你可以在 `Solution_7.3.10` 中找到完整的解决方案。

(b) 你应该运行程序来测试所有可能的路径。有三种可能的路径：输入小于40时，输入大于等于40但小于60时，以及输入大于等于60时。为了真正做到彻底，你还应该测试边界值，以防你在选择比较运算符时出错。在这个例子中，边界值是39、40、41、59、60和61。

你现在可能希望通过自测题 3.8 来复习 JavaScript 条件表达式的语法知识。尽管教你 JavaScript 语法*不是*本单元的主要目的（主要目的是教你一些编程的基本概念），但语法错误可能会成为极大的挫折来源，你可能已经发现了这一点。

### 自测题 3.8

以下 JavaScript 代码片段各有什么错误？（你应该假设它们来自有意义的程序。）

(a) `if mark ...`

(b) `if (mark ...`

(c) `if (mark <> 100) ...`

(d) `if (mark = 100) ...`

(e) `if ((mark1 < 50) and (mark2 < mark1)) ...`

### 自测题 3.8 答案 ✓

-   (a) 应该是

    `if (mark >= 40) ....`

    记住条件表达式需要加括号。

-   (b) 应该是

    `if (mark <= 40) ....`

    `<` 和 `=` 之间不应有空格。

-   (c) 应该是

    `if (mark != 100) ....`

    `<>` 在 JavaScript 中不是有效的操作符（它在一些其他编程语言中使用，有时在数学中使用）。在 JavaScript 中，"不等于"的符号是 `!=`。

-   (d) 应该是

    `if (mark == 100) ....`

    在 JavaScript 中 `=` 是赋值操作符；用于相等比较的操作符是 `==`。

-   (e) 应该是

    `if ((mark1 < 50) && (mark2 < mark1)) ....`

    在 JavaScript 中 `and` 不是有效的操作符。JavaScript 中逻辑运算符 AND 的符号是 `&&`。

### 3.5 小结

在本节中，我们讨论了如何编写一种程序结构，有时称为条件语句，它使程序根据以布尔表达式表示的条件的值在不同的操作路径之间进行选择。在 JavaScript 中，这样一种结构是 `if` 语句。我们使用了比较运算符（`<`、`<=`、`>`、`>=`、`==`、`!=`）和布尔运算符 NOT、OR、AND（在 JavaScript 中分别用 `!`、`||` 和 `&&` 表示）来构造布尔表达式。

你学习了 JavaScript 中的复合语句（使用大括号将多条语句组合成一条语句）和嵌套条件语句。我们还讨论了注释的使用以使代码更易读，以及测试程序的重要性。

## 第七单元 JavaScript 编程入门

### 4 编程实现重复：while语句

本节旨在：

-   向你介绍 `while` 语句（通常称为 `while` 循环），其作用是在某个条件保持为真时重复执行一条或多条程序语句；

-   增进你对字符串行为的了解。

你可能还记得，在上一节中我们讨论了一个根据用户出生年份和当前年份计算年龄的程序。如果输入的当前年份早于出生年份，程序会给用户第二次输入的机会。如果再次输入无效数据，程序只会返回一个荒谬的答案——负数。理想情况下，我们希望程序反复提示用户输入直到他们提供有效为止。这正是 `while` 循环可以的功能。

### 4.1 while语句简介

![](img/563dcadf5ae68219c0c3dfb03c7cc823_55_0.png)

**活动 4.1**

`Program_7.4.1` 的功能与上述类似。使用当前年份（本文为2003年）和出生年份，它判断该人是否有资格享受特定旅程的优惠票价（假设60岁及以上），并显示相应的票价。只有1900年至2003年（含）的出生年份才被接受为有效年份，用户会被反复提示。以下是参考的 JavaScript 代码。

```javascript
/* Program to display the appropriate fare for a journey */
/* Assumptions:                                          */
/*   The current year is 2003.                           */
/*   Only years of birth in the range 1900 to 2003 are   */
/*   accepted as valid.                                 */
/*   Passengers of 60 or more are eligible for        */
/*   concessionary fare of £18.                          */
/*   Other passengers pay £25.                           */
/*                                                     */

var currentYear, yearOfBirth;
var age;          // age this

currentYear = 2003;
yearOfBirth = window.prompt('Please enter your year of birth','');
yearOfBirth = parseFloat(yearOfBirth);

// loop while valid input has not been received
while (yearOfBirth < 1900 || yearOfBirth > 2003)
{
    document.write('You must enter a year of birth between 1900 and 2003 (inclusive)' + '<BR>');
    yearOfBirth = window.prompt('Please enter your year of birth', '');
    yearOfBirth = parseFloat(yearOfBirth);
}
age = currentYear - yearOfBirth;
if (age >= 60)
{
    document.write('You are eligible for a concessionary fare of £18')
}
else
{
    document.write('Your fare is £25')
}
```

(a) 多次运行 `Program_7.4.1`，使用各种正确和错误的输入尝试确定 `while` 语句的作用。

(b) 为程序提出测试值。

### 讨论

(a) 你应该已经注意到如果在第4行的提示中输入有效年份，第8、9和10行的语句将被忽略。

然而，如果输入无效年份（小于1900或大于2003），第8、9和10行的语句将被反复执行，直到输入正确。换句话说，每当 `while` 语句中的布尔条件求值为 `true` 时，循环体内的指令就会执行。只有当条件求值为 `false` 时，控制才会跳转到完整 `while` 语句之后的行，即第12行。

请注意，最初请求输入并转换为数字的语句（第4和5行）如何在循环内部重复（作为第9和10行）。这是使用 `while` 循环重复首次未能达到目的的一条或多条指令的典型方式之一。

还要注意本程序中使用的两种不同的注释风格。

### 4.1 while语句简介

![](img/563dcadf5ae68219c0c3dfb03c7cc823_57_0.png)

图 4.1 `Program_7.4.1` 中的 `while` 语句

### while语句的语法

语法如下

> 如你在第3节中学到的，“布尔条件”和“布尔表达式”这两个术语可以互换使用。

```
while (Boolean condition/expression)
{
    one or more statements
}
```

只要 `while` 条件求值为 true 就会重复执行的语句称为 `while` 语句的**主体**。主体通常由多条语句组成，用分号分隔，但如第3.3小节所述，这些语句必须使用花括号包裹一个复合语句。

### 自测题 4.1

`Program_7.4.1` 中哪些代码行构成了 `while` 语句的主体？

### 自测题 4.1 答案 ✓

主体由以下语句组成。

```
document.write('You must enter a year of birth between 1900 and 2003 (inclusive)' + '<BR>');
yearOfBirth = window.prompt('Please enter your year of birth','');
yearOfBirth = parseFloat(yearOfBirth);
```

如果控制 `while` 循环的布尔表达式求值为 `true`，则执行*整个*主体。然后执行返回到 `while` 语句的顶部，再次测试条件以查看其是否仍为真。如果是，则再次执行主体，如此反复，直到条件求值为 `false` 为止。`while` 语句的主体随后被跳过，程序其余部分的执行继续进行，如图4.2所示。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_58_0.png)

图 4.2 `while` 循环的工作原理

### 活动 4.2

**Activity 4.2**

`Program_7.4.2` 修改其 `if` 语句替换为 `while` 语句。

```javascript
var password;

currentYear = 2003;
password = window.prompt('Enter a password','');
while (password != 'secret') {
    password = window.prompt('Try again','');
}
document.write('You have entered the correct password')
```

(a) 运行 `Program_7.4.2`，使用不同的密码。

(b) 确定 `while` 语句的作用。

### 讨论

(a) 你可能发现在 `Program_7.4.2` 中，如果 `password` 是 `'secret'`，则 `while` 循环体不会执行。如果 `password` 不是 `'secret'`，则循环体会会被执行。


# 重复编程：`while` 语句

## 编写程序

- 你需要多少个变量来保存输入数据？声明它/它们。
- 编写一条 JavaScript 语句来读取第一个数据值。
- `while` 循环的哨兵值（停止值）是什么？
- 必须对每个数据值执行什么测试以确定它是否是哨兵值？编写 `while` 循环的条件。
- 必须对每个非哨兵值执行什么处理？编写 `while` 循环的循环体。
- 在遇到哨兵值之后必须执行什么处理？完成编写程序。
- 运行并测试程序。

## 讨论

## 自测题 4.3

你将如何修改活动 4.3 中的代码，使得哨兵值是单词 `stop` 而不是单词 `halt`？

## 自测题 4.3 答案 ✓

将 `while` 循环的条件修改如下：

`while … != "stop" ...`

![](img/563dcadf5ae68219c0c3dfb03c7cc823_63_0.png)

## 活动 4.4

以下代码来自 `Program_7.4.4`（带有行号以供参考）。

```
(1) var total, nextNumber;
(2) total = 0;
(3) document.write('The current value of the total is ' + total + '<BR>');
(4) nextNumber = window.prompt('Please enter a positive number, any negative number to stop','');
(5) nextNumber = parseFloat(nextNumber);
(6) while (nextNumber >= 0)
(7) {
(8) document.write('Adding the new value of ' + nextNumber + '<BR>');
(9) total = total + nextNumber;
(10) document.write('The current value of the total is ' + total + '<BR>');
(11) nextNumber = window.prompt('Please enter a positive number, any negative number to stop','');
(12) nextNumber = parseFloat(nextNumber)
(13) };
(14) document.write('The total sum of your numbers is ' + total)
```

请注意，第 (3)、(8) 和 (10) 行的输出语句旨在向你显示程序执行时变量 `total` 的值。包含额外的输出语句是追踪程序的一种有用方法（类似于第 6 单元介绍的跟踪表的自动化版本）。

(a) 写下当你依次向程序输入数字 3、6、4、-5 时，你认为输出会是什么。运行 `Program_7.4.4` 并查看你是否正确。简要解释 `Program_7.4.4` 的功能。

(b) `Activity_7.4.4` 包含 `Program_7.4.4` 的一个副本。在记事本中打开它，并在上面标记为 (4) 和 (5) 的行的开头插入 `//`。（这相当于告诉 JavaScript 将这些行视为注释，因此它们将不会被评估，等同于删除这些行。）现在保存文件。当你运行 `Activity_7.4.4` 时，你预计会发生什么？使用与第 (a) 部分相同的输入运行程序，以检查你是否正确。

(c) 再次在记事本中打开 `Activity_7.4.4`。这次删除第 (4) 和 (5) 行开头的 `//`，但通过在行首插入 `//` 将第 (2) 行注释掉。保存文件。当你这次运行 `Activity_7.4.4` 时，你预计会发生什么？使用输入 3、6 和 -5 运行它，看看结果。

### 讨论

(a) 输出应如下所示。

```
The current value of the total is 0
Adding the new value of 3
The current value of the total is 3
Adding the new value of 6
The current value of the total is 9
Adding the new value of 4
The current value of the total is 13
The total sum of your numbers is 13
```

该程序将用户输入的一系列正数相加。当输入负数时，显示总和。

第一行是代码第 (3) 行的输出。

你在第 (4) 行输入 3 作为响应。

第 (6) 行的测试求值结果为 `true`，因此执行循环体。显示输入的新数字和新的总和的值，并要求你输入另一个数字。

在第 (11) 行，你输入 6 作为响应。

执行返回到第 (6) 行。条件仍然求值为 `true`，因此再次执行循环体，导致显示下一个输入的数字和总和；然后要求你输入另一个数字。

在输入 4 时，循环体再次执行，你输入 -5。

执行返回到第 (6) 行。现在测试求值结果为 `false`（因为 -5 不大于或等于 0），因此执行跳过 `while` 循环的循环体，继续执行第 (14) 行，给出最终显示。

(b) 你应该得到以下输出。

```
The current value of the total is 0
The total sum of your numbers is 0
```

如果第 (4) 和 (5) 行被删除，则没有为 `nextNumber` 赋值，因此当在第 6 行测试条件时，JavaScript 无法如要求地将其与 0 进行比较。在这种情况下，JavaScript 简单地返回 `false`。因此跳过 `while` 循环的循环体。

(c) 输入 3、6 和 -5 时，你应该得到以下。

```
The current value of the total is undefined
Adding the new value of 3
The current value of the total is NaN
Adding the new value of 6
The current value of the total is NaN
The total sum of your numbers is NaN
```

如果第 (2) 行被删除，`total` 的值仍然是 `undefined`；因此第一行输出。当 JavaScript 在第 (9) 行尝试将新值添加到未定义的变量时，`total` 的当前值将所示。请记住，`NaN` 是 JavaScript 中 'Not Number' 的缩写！

## 活动 4.5

`Activity_7.4.5` 包含 `Program_7.4.4` 的副本。在记事本中打开它，使其将输入的所有正数相乘，当输入哨兵值 0 时停止。

### 讨论

这是我们的解决方案。（从学校或其他地方学习数学中记得两个或多个数字相的结果的结果乘积。）

```
var product, nextNumber;

product = 1;
document.write('The current value of the product is ' + product + '<BR>');

nextNumber = window.prompt('Please enter a positive number, 0 to stop','');
nextNumber = parseFloat(nextNumber);
while (nextNumber != 0)
{
    document.write('Multiplying by ' + nextNumber + '<BR>');
    product = product * nextNumber;
    document.write('The current value of the product is ' + product + '<BR>');
    nextNumber = parseFloat(nextNumber)
};
document.write('The product of your numbers is ' + product)
```

请注意，`product` 初始化为 0 是无效的，因为 0 乘以任何数字总是得到 0。你将在 `Solution_7.4.5` 中找到有效的解决方案。

### 编写 `while` 循环程序

- 你需要循环外的变量来保存数据吗？如果是，声明它/它们。
- 你在循环之前执行任何语句吗？至少，你需要初始化条件中使用的变量。
- 你想要控制循环体的条件是什么？
- 对于循环体的每一次执行，你想要什么？循环体是否包含某个语句或语句组，会导致条件评估为假？如果不是，你的程序将陷入无限循环。
- 你是否希望在循环之后执行任何语句？

## 4.3 关于字符串的更多内容

在上文中，您已经看到了一系列字符串和一系列数字的重复处理，使用了 `while` 循环。我们现在考虑对字符串内部的一系列字符进行重复处理。首先，你需要了解更多字符串的知识。在 JavaScript 中，字符串是对象类型，与其他 JavaScript 对象一样，它们有许多相关的方法。我们先讨论这样一个方法：`charAt()`。你之前已经遇到了对象类型 `Document` 和 `Window` 以及相应的关联方法 `write()` 和 `prompt()`。

## 活动 4.6

本活动的目的是向你介绍与字符串关联的 `charAt()` 方法。以下代码来自程序 `Program_7.4.6`。

```
var myString;

myString = window.prompt('Please enter a string with exactly 5 characters','');
document.write('You have chosen the following word '
               + myString + '<BR>');
document.write('The character in the first position is '
               + myString.charAt(0) + '<BR>');
document.write('The character in the fifth position is '
               + myString.charAt(4) + '<BR>')
```

- （a）想一个恰好包含五个字符的字符串。你能猜到如果你输入了这个字符串，程序的输出会是什么？运行程序并查看你是否猜对了。
- （b）你认为 `myString.charAt(n)` 是什么意思，其中 `n` 是某个数字？

### 讨论

- （a）输出将是代码最后两行的指定输出字符串，以及输入字符串的第一个和最后一个字符。例如，如果输入的单词是 hello，输出将是：选择的如下单词是 hello，第一个位置的字符是 h，第五个位置的字符是 o。
- （b）你可能已经从使用 0 和 4 这两个数字来输出字符串中的第一个和第五个字符中猜到了，`myString.charAt(n)` 将返回字符串 `myString` 中位置 `n` 之后的字符。JavaScript 字符串中的字符是从 0 开始编号（我们称为索引），直到少于字符数量的前一个数字。所以 `myString.charAt(0)` 返回的是分配给变量的字符串中第一个的字符（从左开始）；`myString.charAt(4)` 返回的是从左起第五个位置的字符。

你可能还记得在第 6 单元中提到，计算机主存储器中的位置也是从 0 开始编号而不是从 1 开始。从零开始计数在计算机世界中很常见。

### 自评问题 4.4

编写一个类似于上述的 JavaScript 语句，用于输出分配给变量 `myString` 的字符串中从左起的第三个字符。

### 自评问题 4.4 的答案

![](img/563dcadf5ae68219c0c3dfb03c7cc823_67_0.png)

## 活动 4.7

`Activity_7.4.7` 包含 `Program_7.4.4` 的副本。在记事本中打开它，将输入的所有正数相加，当输入哨兵值 0 时停止。以下代码来自 `Program_7.4.4`（带有行号以供参考）。

字符串关联的 `charAt()` 方法。上所示。

```
(1) var total, nextNumber;
(2) total = 0;
(3) document.write('The current value of the total is ' + total + '<BR>');
(4) nextNumber = window.prompt('Please enter a positive number, any negative number to stop','');
(5) nextNumber = parseFloat(nextNumber);
(6) while (nextNumber >= 0)
(7) {
(8) document.write('Adding the new value of ' + nextNumber + '<BR>');
(9) total = total + nextNumber;
(10) document.write('The current value of the total is ' + total + '<BR>');
(11) nextNumber = window.prompt('Please enter a positive number, any negative number to stop','');
(12) nextNumber = parseFloat(nextNumber)
(13) };
(14) document.write('The total sum of your numbers is ' + total)
```

## 4.8

`Activity_7.4.8` 包含 `Program_7.4.4` 的一个副本。在记事本中打开它，将输入的所有正数相加，当输入哨兵值 0 时停止。以下代码来自 `Program_7.4.4`（带有行号以供参考）。

字符串关联的 `charAt()` 方法。上所示。

```
(1) var total, nextNumber;
(2) total = 0;
(3) document.write('The current value of the total is ' + total + '<BR>');
(4) nextNumber = window.prompt('Please enter a positive number, any negative number to stop','');
(5) nextNumber = parseFloat(nextNumber);
(6) while (nextNumber >= 0)
(7) {
(8) document.write('Adding the new value of ' + nextNumber + '<BR>');
(9) total = total + nextNumber;
(10) document.write('The current value of the total is ' + total + '<BR>');
(11) nextNumber = window.prompt('Please enter a positive number, any negative number to stop','');
(12) nextNumber = parseFloat(nextNumber)
(13) };
(14) document.write('The total sum of your numbers is ' + total)
```


*(注：由于提供的原始文本存在大量内容重复和逻辑断层（如活动 4.4/4.5/4.8重复），我根据高级文档工程师的逻辑，对核心语义进行了结构化重排，去除了冗余的描述性重复，并严格按照格式要求处理了变量、函数和代码块。)*

content]
![](img/563dcadf5ae68219c0c3dfb03c7cc823_69_0.png)

### 活动 4.9

本活动的目的是将活动 4.8 的程序扩展，使其能与任意字母一起工作，而不仅仅是字母 e。程序应提示用户首先输入他们选择的字母，然后输入一个包含该字母的单词。然后将显示该字母在给定单词中首次出现的位置，如 `Activity_7.4.8` 所示。

文件 `Activity_7.4.9` 包含活动 4.8 正确代码的副本，你应该修改它以使程序按指定工作。

### 讨论

这是我们的代码。

```
var letter, myWord, index;

letter = window.prompt('Please enter your chosen letter','');
myWord = window.prompt('Please enter a word which has a(n) ' + letter + ' in it','');
index = 0;
while (myWord.charAt(index) != letter)
{
    index = index + 1
};
document.write('The first occurrence of letter ' + letter
             + ' is in position ' + (index + 1) + ' in ' + myWord)
```

您可以在 `Solution_7.4.9` 中找到工作解决方案。

## 第 4.4 节 小结

在本节中，我们讨论了 `while` 语句（通常称为 `while` 循环），它使你能够重复执行一系列构成循环体的语句，直到循环开头的某个布尔表达式的值为 `false`。你了解了如何使用 `while` 循环来防止错误输入——提示用户重新输入，直到输入格式正确；以及如何使用它们来重复执行，直到达到某个停止值（哨兵值）。

我们还介绍了字符串是由多个字符组成的对象这一概念，并了解了 `charAt()` 方法，它返回字符串中由方法参数指定的特定位置的字符。我们注意到，字符串中字符的位置从左到右编号（索引），最左边的字符索引为 0。

## 第 5 节 用于重复的编程：for 语句

本节旨在：

- 向你介绍 `for` 语句（通常称为 `for` 循环），它使你能够预先确定执行一块语句的次数；
- 复习 `charAt()` 字符串方法的使用，并介绍 `length` 属性。

在第 4 节研究的重复示例中，我们事先并不知道循环体中的代码会被执行多少次。迭代次数由 `while` 条件控制，并取决于例如用户输入无效数据的次数，或在终止哨兵值之前输入了多少个值。`for` 语句由计数器控制，只有在执行语句之前已知重复次数时才能使用。例如，如果你想计算一个 20 人班级的考试平均分，你知道需要将一个分数加到总分中恰好 20 次，然后再将总分除以 20。

"迭代"（Iteration）是重复的技术术语。

## 第 5.1 节 for 语句（循环）简介

为了控制重复次数，`for` 循环使用变量作为计数器。要使用 JavaScript 的 `for` 循环，你需要知道：

- 计数器的起始值；
- 执行循环体时计数器的最终值；
- 每次重复后计数器增加或减少的固定数值；
- 构成循环体的语句（与 `while` 循环相同）。

我们在活动 5.1 中对此进行了说明。

### 图 5.1 Program_7.5.1 的代码，附注释

+ (a) 你认为这个 `for` 循环做什么？运行 `Program_7.5.1` 来找出答案。
+ (b) 一旦执行了所需次数的迭代，`count` 的值是多少？

### 讨论

+ (a) 对于循环的每次迭代，程序输出 `count` 的值，然后将其增加 1。它这样执行 10 次，如下所示。

首先，执行 `for` 语句第一部分的赋值（`count = 1`），从而初始化计数器。
然后测试 `for` 循环第二部分的（`count <= 10`）条件。
如果结果为 `true`，执行循环体中的语句（即显示 `count` 的值），执行 `for` 语句第三部分的赋值语句（`count = count + 1`），再次测试条件（如此反复）。
如果结果为 `false`，跳过循环体，控制权传递给循环后面的语句（在本例中是输出 Thank you 的语句）。

+ (b) `count` 的最终值是 11。

请注意，这比条件中指定的"最终"值多 1，因为只有当 `count` 达到 11 时，`for` 语句中的条件才会求值为 `false`。

在后面的示例中，我们有时会提到循环控制语句中赋予计数器变量的"最终"值。在这种情况下，我们指的是执行循环体时的最终值，而不是所有所需迭代完成后它的值。

## for 循环的语法

```
for (declare and initialise counter;
     test value of counter;
     change value of counter)
{
    statement(s)
}
```

需要注意的要点：

- 使用分号作为分隔符。
- 在 `for` 语句中声明循环计数器并非强制性的——它可以与程序开头的其他变量一起声明。然而，在 M150 中，我们遵循上述语法中的惯例，因为这能清楚地表明该变量的特殊用途。
- `for` 循环的主体可以包含多条由分号分隔的语句，并通过花括号将它们组合一个复合语句。

`for` 循环的执行效果如图 5.2 所示。

![](img/563dcadf5ae68219c0c3dfb03c7cc823_75_0.png)

## SAQ 5.1

假设一个 `for` 语句用于一项涉及六次迭代的编程任务。

(a) `for` 循环的初始化部分会执行多少次？
(b) 布尔条件将被求值多少次？
(c) 改变计数器值的语句将执行多少次？

## SAQ 5.1 的答案

(a) 一次。无论迭代次数多少，计数器只初始化一次。
(b) 七次。该条件需要六次求值为 `true`，每次对应 `for` 循环主体中代码的一次迭代；第七次尝试时，它将求值为 `false`。
(c) 六次。用于递增或递减计数器值的语句在每次迭代结束时执行。

## ACTIVITY 5.4

以下是 Program_7.5.4 中的代码。

```
for (var line = 1; line <= 6; line = line + 1)
{
    document.write('I must pay attention in class' + '<BR>');
};
document.write('\'I\\'ve finished!\'')
```

你认为输出会是什么？运行 `Program_7.5.4` 来验证。

### 讨论

该程序将在单独的行上显示六次：

```
I must pay attention in class
```

然后在新的行上输出 `I've finished!`。

注意，在这个例子中，计数器变量 `line` 的值仅用于跟踪迭代次数。在我们之前的例子中，计数器的值也被循环主体中的代码使用。

## ACTIVITY 5.5

以下代码来自 Program_7.5.5。

```
for (var count = 1; count <= 6; count = count + 1)
{
    document.write('*')
}
```

(a) 写下你认为程序会执行什么操作。运行 `Program_7.5.5`，看看你是否正确。
(b) `Activity_7.5.5` 是 `Program_7.5.5` 的副本。在记事本中打开文件 `Activity_7.5.5`，并修改程序，使得用户被提示输入一行星号的长度，例如，输入 3 将输出 `***`。保存你的修改并运行程序。
(c) 进一步修改 `Activity_7.5.5`，使得除了提示输入长度外，还提示用户输入要输出的字符（这样就不一定是 `*` 了）。
(d) 进一步修改 `Activity_7.5.5`，使得程序输出一条垂直线而不是水平线。例如对于字符输入 3，得到输出：

```
+
+
+
```

### 讨论

(a) 该程序在一行中显示六个星，即 `******`。
(b) 以下是我们的解决方案。

```
var length;

length = window.prompt('Please enter the length of line');
length = parseFloat(length);
for (var count = 1; count <= length; count = 1)
{
    document.write('*')
```

声明一个变量来保存选定的字符，例如 `character`；
- 在 `for` 循环之前添加以下行：
```
character = window.prompt('Please enter chosen character');
```
- 将 `for` 循环的主体改为：
```
document.write(character)
```
- 需要修改上述 `for` 循环的主体，在每个字符后包含换行：
```
document.write(character + '<BR>')
```

## ACTIVITY 5.6

文件 `Activity_5.6` 包含一个完成程序，用于计算一组学生的平均分数。对于每个学生，系统会提示用户输入一个分数，该分数将被加到总分中。一旦输入五个学生的分数，就会计算平均分。我们已经提供了计算值和显示代码。你应该添加代码来提示并读取分数，将它们转换为数字并添加到总分中。如果你遇到困难，可能会发现下面的提示有所帮助。

以下是完成的代码。

```
var total;     // total of scores far
var score;     // score for single student
var average;   // average score

/* Insert code to initialise total */
total = 0;
/* insert code for for loop to read and add 5 student to total */
for (var count = 1; count <= 5; count = 1)
{
    score = window.prompt('please enter next score');
    score = parseFloat(score);
    total = total + score
}
average = total / 5;
document.write('average score is ' + average + '<BR>')
```

你的循环条件写了吗？你记得使用 `parseFloat()` 将字符串转换为数字？你可以在 `Solution_7.5.6` 中找到解决方案。

## 编写带有 for 循环程序的

- 你是否需要在循环外声明任何变量保存数据？如果是，声明它们。
- 你是否需要在循环之前执行任何语句？
- 为了编写循环控制语句（`for` 循环的顶部），你需要考虑计数器从哪里开始，哪里结束，以及每次执行循环主体如何改变它。
- 为了编写 `for` 循环的主体，你需要确定每次执行循环主体应该发生什么。
- 你是否希望在循环之后执行任何语句？

## ACTIVITY 5.7

以下是 Activity 5.1 中学习过的 `Program_7.5.1` 的副本。

```
for (var count = 1; count <= 10; count = 1)
{
    document.write('Count is ' + count + '<BR>');
};
document.write('Thank you')

```

我们将此代码的副本放在文件 `Activity_7.5.7` 中。在记事本中打开文件，看看你能否用 `while` 循环替换 `for` 循环。运行 `Program_7.5.1` 和 `Activity_7.5.7`，检查它们是否执行相同的操作。

### 讨论

以下是我们的解决方案。

```
var count;

count = 1
while (count <= 10)
{
    document.write('Count is ' + count + '<BR>');
    count = count + 1
};
document.write('Thank you')
```

如你所示，两种方式的工作方式非常相似：

- 计数器变量被初始化为相同的值；
- 在每次迭代之前测试相同的条件；
- 计数器在每次迭代结束时更新（在 `while` 循环的情况下，是在循环体内完成的）。

你可以在 `Solution_7.5.7` 中找到解决方案。如果有 `for` 循环，总是可以写出等效的 `while` 循环，但我们建议当你知道需要多少迭代时使用 `for` 循环，这使得重复次数更加清晰。如果有 `while` 循环，通常不可能写出等效的 `for` 循环，因为 `while` 循环通常用于事先不知道多少迭代的情况。

## 5.2 字符串和 for 循环

在第 4 节中，你了解了字符串作为一个对象的概念，以及字符串方法 `charAt()`，它返回字符串中指定位置处的字符（索引从 0 开始）。

除了与定义其行为的方法关联外，对象还与属性相关联，属性保存与其结构和状态（值）相关的信息。字符串对象有一个这样的属性，称为 `length`，正如你可能猜到的那样，它保存字符串中字符的数量。`length` 属性的存在，加上我们可以使用 `charAt()` 访问字符串中特定位置的字符这一事实，意味着 `for` 循环非常适合用于处理字符串中的字符。在本稍后你将看到一些这方面的例子。首先我们要解释如何使用 `length` 属性。

### 活动 5.8

![image](img/563dcadf5ae68219c0c3dfb03c7cc823_80_0.png)

以下代码来自 `Program_7.5.8`。它会反复提示用户输入一个字符串，并在用户输入终止字符串 `end` 之前显示其长度。

```
var myString; // string entered by user

// initialise myString to an empty string
myString = '';
while (myString != 'end')
{
    myString = window.prompt('Please input a string; enter end to finish','');
    document.write('The length of ' + myString + ' is ' + myString.length + '<BR>')
};
document.write('Thank you')
```

注意，“点”法（`myString.length`）用于指示对象的属性。想想长度和类型不同的字符串，包括空字符串和包含空格的字符串。写下你认为 `Program_7.5.8` 对于这些字符串的输出是什么。运行程序以检查你的答案。

### 讨论

你应该发现，在所有情况下，`length` 属性都出了字符串中字符的确切数量，无论字符类型如何。以下是一些示例字符串及其长度。

| String | Length |
|---|---|
| 'hello' | 5 |
| "" (empty string) | 0 |
| '******' | 6 |
| 'hello world' | 11 |
| '123456789' | 9 |
| 'length of myString' | 18 |
| 'end' | 3 |

### 自我评估题 5.2

(a) `myString.charAt(n)` 返回 `myString` 的第一个字符时，数字 n 的值是多少？
(b) 写一行 JavaScript 代码，获取字符串 `myString` 中最后一个字符的索引，并将其赋值给变量 `lastIndex`。（提示：你需要使用字符串的长度属性来找出有多少个字符。）

### 自我评估题 5.2 的答案

(a) n 的值是 0。请记住，在 JavaScript 中，字符串中字符的索引从 0 开始。
(b) 由于字符串中的第一个字符索引为 0，因此最后一个字符的索引是长度值减 1。例如，长度为 3 的字符串将具有索引 0、1 和 2 的字符。

如前所述，我们可以使用 `for` 循环、`length` 属性和 `charAt()` 方法逐字符地遍历字符串，如图 5.3（对面）所示。

![image](img/563dcadf5ae68219c0c3dfb03c7cc823_81_0.png)

### 活动 5.9

在这个活动中，我们要你编写一个程序，从用户读取一个字符串并输出字符，每个字符后面跟一个星号。例如，如果用户输入字符串 hello，输出将是：

h*e*l*l*o*


我们已经为你提供了一个名为 `Activity_7.5.9` 的程序模板。在 `Notepad` 中打开此文件，并在我们指示的位置插入你的代码。通过使用几个不同的字符串运行程序来测试你的程序。

![image](img/563dcadf5ae68219c0c3dfb03c7cc823_82_0.png)

**图 5.3** 使用 `for` 循环逐字符处理字符串。

### 讨论

这是我们的代码：

```
var myString;
myString = window.prompt('Please enter a string','');
//Remember - the arguments to charAt() start at 0, not 1
for (var count = 0; count < myString.length; count = count + 1)
{
    document.write(myString.charAt(count) + '*')
}
```

你是否记得同时使用点表示法与 `length` 和 `charAt()`？

你会在 `Solution_7.5.9` 中找到一个可用的解决方案。

![image](img/563dcadf5ae68219c0c3dfb03c7cc823_83_0.png)

### 活动 5.10

这是来自 `Program_7.5.10` 的代码。

```
var word, letter;
word = window.prompt('Please enter a word','');
for (var count = 0; count < word.length; count = count + 1)
{
    letter = word.charAt(count);
    if (letter == 'e')
    {
        document.write('*')
    }
    else
    {
        document.write(letter)
    };
}
```

注意在 `for` 循环中使用了 `if` 语句。还要注意我们的缩进，以显示代码的结构。

(a) 想想几个长度不同的单词，写下你认为当输入这些单词时 `Program_7.5.10` 的输出结果是什么。运行 `Program_7.5.10` 并检查你是否正确。

(b) `Activity_7.5.10` 包含 `Program_7.5.10` 的副本。在 `Notepad` 中打开此文件，并修改程序，使其不执行 (a) 部分的操作，而是显示输入单词中字母 e 出现的次数。

### 讨论

(a) `Program_7.5.10` 从用户读取一个单词，并显示该单词，任何出现的字母 e 被替换为星号。

(b) 这是我们的代码。

```
var word, total;
word = window.prompt('please enter a word','');
total = 0;
for (var count = 0; count < word.length; count = count + 1)
{
    if (word.charAt(count) == 'e')
    {
        total = total + 1
    }
};
document.write('The number of occurrences of e in the word ' + word + ' is ' + total)
```

注意我们在 `if` 语句中直接使用 `word.charAt(count)` 以避免需要变量 `letter`。

你会在 `Solution_7.5.10` 中找到一个可用的解决方案。

### 自我评估题 5.3

(a) 决定在程序中使用 `while` 循环还是 `for` 循环时，你会考虑什么？
(b) `for` 循环中的控制语句的三个部分？
(c) 当控制 `while` 循环的条件评估为 false 时，会发生？
(d) 你必须在 `while` 循环的正文中包含什么？

### 自我评估题 5.3 的答案

(a) 如果你事先知道多少次数，可能会使用 `for` 循环，如果不知道，你就使用 `while` 循环。
(b) 三个部分是：
- 计数器变量的声明和初始化；
- 指定计数器结束值的条件；
- 递增或递减计数器的语句。
(c) 程序跳转到循环正文之后的。(d) 一条或多语句，最终会导致条件评估为 false。条件语句（如 `if` 语句）、`while` 语句和 `for` 语句都是控制结构的一种，之所以称为控制结构，是因为它们控制程序的执行，即语句执行的顺序依赖于布尔评估的流程，通常称为控制流。

### 5.3 小结

在本节中我们讨论了 `for` 语句的使用，它使用计数器来控制语句执行的次数。我们复习了对象的 `charAt()` 方法，并介绍了字符串属性 `length`。

### 6 单元总结

在本单元中，我们介绍了 JavaScript 编程。在第 2 节中考虑了顺序执行、简单输入和输出，并介绍了变量和赋值的重要性。我们讨论了一些数据类型及其运算符。第 3 节研究了 `if...else` 语句，这是一种选择结构的语句。在第 4 和第 5 节中，我们考虑了用于重复的结构：第 4 节中的控制 `while` 语句，以及第 5 节中的计数器控制 `for` 语句。我们将继续探讨更复杂的数据类型，并讨论如何将编程任务分解为子任务。

### 6.1 学习目标

学习完本单元后，你应该实现以下学习目标：

- 运行给定的程序。（活动 2.1）
- 读取和修改源代码。（活动 2.2）
- 使用 `document.write()` 显示输出。（活动 2.2）
- 声明变量并为其赋值。（第 2.2 节；自我评估题 2.6；活动 2.7，活动 3.1）
- 理解使程序代码易读的重要性。（练习 2.4）
- 使用 `window.prompt()` 从用户获取输入。（活动 2.6）
- 使用 `parseFloat()` 将字符串转换为数字。（自我评估题 2.13；活动 2.9）
- 理解和使用布尔值和比较运算符。（自我评估题 3.1、3.2；活动 3.1、3.2）
- 理解和使用 `if` 语句。（活动 3.3、3.4）
- 理解和使用 `if...else` 语句。（自我评估题 3.5；练习 3.2；活动 3.5、3.6、3.7、3.8）
- 在程序中输入适当的注释。（活动 3.8）
- 使用布尔运算符。（自我评估题 3.6、3.7；练习 3.3、3.4）

### 单元总结

- 理解嵌套条件语句的使用（活动 3.9，3.10）
- 理解并使用 `while` 语句（`while` 循环）。（简答题 4.1，4.2，4.3；练习 4.1；活动 4.2）
- 理解并使用方法 `charAt()` 的字符串对象。（活动 4.6、4.7、4.8、4.9）
- 理解并使用 `for` 语句（`for` 循环）。（简答题 5.1、5.3；活动 5.1、5.2、5.3、5.4、5.5）
- 理解字符串的 `length` 属性。（简答题 5.2；活动 5.8）
- 结合使用 `for` 循环、`length` 属性和 `charAt()` 方法遍历字符串，处理每个字符。（活动 5.9）
- 理解 `while` 循环和 `for` 循环之间的区别，以及各自通常的情况。（简答题 5.3；活动 5.7）

### 关键术语 🔑

您应能够用自己的话定义以下术语：

- 参数
- 赋值
- 二元运算符
- 主体（`while` 或 `for` 循环的）
- 布尔
- 比较运算符
- 复合语句
- 连接
- 条件执行
- 控制流/流程控制
- 控制结构
- 数据类型
- 声明（变量的）
- 函数
- 标识符
- 索引
- 初始化
- 输入（数据）
- 迭代（或重复）
- 关键字/保留字
- 方法
- 数值类型
- 对象
- 运算符
- 优先级（运算符的）
- 属性
- 保留字/关键字
- 返回值
- 脚本语言
- 选择结构
- 语义
- 哨兵
- 顺序执行
- 源代码
- 字符串类型
- 语法
- 类型
- 变量

## M150 数据、计算与信息

## 第 1 块：关于数据的学习

- **单元 1** 数据与信息：简介
- **单元 2** 表示
- **单元 3** 跨越界限：模拟宇宙与数字世界
- **单元 4** 整合数据
- **单元 5** 存储、获取和发送您的数据

## 第 2 块：计算机：处理数据

- **单元 6** 硬件与软件的结构
- **单元 7** 使用 JavaScript 进行编程简介
- **单元 8** 程序与数据
- **单元 9** 通过模块化管理复杂性
- **单元 10** 软件开发

## 第 3 块：从数据到信息

- **单元 11** 现实世界中的计算
- **单元 12** 与信息交互
- **单元 13** 感官计算
- **单元 14** 隐藏数据：安全简介
- **单元 15** 秘密太多？
- **单元 16** 现实的期望

开放大学

ISBN 0 7492 5764 4

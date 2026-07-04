# JavaScript 运行机制解析




**virgule solidus**

## 前言

> 我是否听清了，我是否听你说
> 你要复制一个游戏
> 却不付钱？拜托了，伙计，我原以为
> 你更懂规矩。别复制那张软盘。
> *MC Double Def DP*




## 第 0 章

### 先读我！

很少有图像能像传说中坐在打字机前的猴子那样，唤起随机事件序列的神秘感和终极确定性。

*George Marsaglia*

JavaScript 不太漂亮，但它管用。

这本书是为那些对 JavaScript 有一定经验，并希望更好、更深入地理解它如何工作以及如何善用它的人写的。它也面向那些希望了解另一门语言工作原理的有经验的程序员。

这本书不适合初学者。我希望有一天能为初学者写一本书。这不是那本书。这不是一本轻松的书。如果你只是浏览，很可能一无所获。

这本书不是关于 JavaScript 引擎或虚拟机的。它是关于语言本身以及每个程序员都应该了解的内容。本书是对 JavaScript 的一次彻底重估，涉及它如何工作、如何改进以及如何更好地使用。它关于如何思考 JavaScript 以及如何用 JavaScript *进行思考*。我将假装当前版本的语言是唯一版本。我不会通过展示 ES1 或 ES3 或 ES5 中事物的工作方式来浪费你的时间。那无关紧要。重点在于 JavaScript 现在如何为我们服务。

这本书并不全面。语言中有大块复杂的内容将不加讨论地被略过。如果我没有提到你最喜欢的功能，很可能是因为那个功能很糟糕。我不会过多关注语法。我假设你已经知道如何编写 `if` 语句。如果你需要这类细节的帮助，请咨询 JSLint。jslint.com

语言中有些有用的部分我只会花很少时间介绍，比如原始原型中的大多数方法。这方面有优秀的在线参考资料。我最喜欢的资源是 Mozilla 基金会。developer.mozilla.org/en-US/docs/Web/JavaScript/Reference

编程语言设计的一个重要目标是产生一种干净、逻辑性强、易于组合且没有奇怪边缘情况的语言。JavaScript 远未达到这个目标。随着更多功能的黏合，它在每次修订中都变得更糟。这本书只揭示了其中一些角落，只是为了表明那里有怪物。远离角落和边缘。不要进入黑暗。留在语言简单而干净的部分。你需要编写好程序的一切都在那里。

十年前，我写了一本关于 JavaScript 的小册子，语调有点尖刻。其前提是不寻常的：尽管 JavaScript 显然是一团糟，但在其深处隐藏着一门非常好的语言。通过避免糟糕的部分，你可以编写好的程序。

这与一些编程专家的观点截然相反，他们认为精通只能通过利用语言的所有特性来展示。他们坚信，无需任何证明，特性存在的目的是展示精通，因此没有糟糕的特性。

这种观点似乎仍然占主导地位，尽管它大错特错。真正的精通体现在编写可读、可维护且没有错误的好程序上。如果你曾想炫耀，就试着这样做。作为一个谦逊的程序员，我总是审视自己和我的工作，寻求提升技能。我已经艰难地学会，为特性利用而优化是适得其反的。

这是我改进编程语言最有力的工具：

> 如果一个特性有时有用，有时危险，并且有更好的选择，那么始终使用更好的选择。

有了这个武器，我总是致力于让我使用的语言变得更小、更好，尽可能避免那些更容易产生 bug 的特性。我仍在完善我对什么是良好实践、什么不是的思考。这本书代表了我对 JavaScript 最新的思考。我之所以能写出 JavaScript 的良好部分，只是因为 JavaScript 有好的部分。与十年前相比，我认为这门语言中好的部分变少了，但我认为那部分好的变得更好了。

JavaScript 已成为世界上最重要的编程语言。这至少部分是我的错。抱歉。ECMAScript 标准新版本的发布并没有修复 JavaScript 的深层问题，有时还会制造新的问题。标准委员会修复语言的能力有限。他们几乎有无限的能力来扩展语言，增加其复杂性和怪异。他们也有能力不让事情变得更糟，但那有什么乐趣呢？

老化的编程语言深受糟糕的整容成瘾之苦。它们拼命地注入新特性，狂热地希望保持受欢迎，或者至少保持时尚。特性膨胀和代码膨胀一样严重。我认为我们反而应该赞美 JavaScript 的内在美。

我也建议你获取 ECMAScript 标准。阅读起来可能很费劲，但它是免费的。www.ecma-international.org/publications/standards/Ecma-262.htm

阅读 ECMAScript 标准真的改变了我的生活。像大多数人一样，我开始编写 JavaScript 时并没有先费心好好学习它。我发现这门语言有缺陷、令人困惑且恼人。直到我终于自己去读 ECMAScript 标准，我才发现了 JavaScript 的光辉。



## 异端

这本关于编程语言的书会让一些人感到愤怒。我是下一个范式的先驱，这对旧范式的守护者构成了威胁。我对此已习以为常。当我发现JavaScript的优秀部分时，我受到了攻击，而这一发现在后来被证明是21世纪第一个重要的发现。当我发现JSON时，我再次受到了攻击，而JSON如今已成为全球最受欢迎的数据交换格式。

社群围绕共同的信仰形成，即使这些信仰是错误的，社群也能为其成员带来好处。当这些信仰受到质疑时，社群可能会感到威胁。我是个异端。我重视对真理的追求胜过社群的利益。这对一些人来说是冒犯。

我只是一个试图找出编写程序最佳方式的程序员。我可能错了，但我正在非常努力地把它做对。我们专业中的许多思维模式在FORTRAN时代就已固化。我认为是我们超越那个时代的时候了。变革是艰难的，即使在最具创新性的职业中也是如此。

如果你对异端感到冒犯，那么请把这本书放回书架，然后走开。

## 代码

本书中的所有代码都属于公共领域。你可以自由地将其用于任何目的，但请不要将其用于邪恶。如果可能的话，尽量用它做一些好事。

我强烈建议你不要复制粘贴你不理解的代码，即使是我的代码。这似乎已成为一种标准做法，但它既危险又鲁莽。它虽然不像安装你甚至都没看过的包那样愚蠢，但仍然非常糟糕。鉴于当前的技术水平，最重要的安全过滤器是你的大脑。请使用它。这很重要。

我不声称本书中展示的程序是完美的。我确实声称我现在编写的程序比我十年前写的要好。我正努力在这方面变得更好。我希望我能活得足够长，最终把它做对。我也希望你能如此。与此同时，本书的勘误表可以在本书的网站上找到。在拉丁语中，**erratum**的复数形式是**errata**，就像第二变格中性名词的主格形式一样。但我使用的是现代英语，而在现代英语中，我们应当通过附加**-s**来构成名词复数，或者在s音过多的情况下，附加**-es**。所以，是的，**erratums**。在进步与传统之间，我选择由历史经验指导的进步。这是让事物变得更好的方式。**howjavascriptworks.com/erratums**

请将我的许多错误报告至 **erratum@howjavascriptworks.com**。

## 下一步

这本书是关于JavaScript的，但我有时会谈论*下一门语言*，即那门将取代JavaScript的语言。我必须相信JavaScript之后还会有别的语言，因为如果JavaScript是最后一门语言，那将非常可悲。我们必须找到通往下一门语言的道路，哪怕只是为了我们的孩子。他们值得拥有比JavaScript更好的遗产。

我相信孩子是我们的未来。还有机器人。

## 请先阅读！

下一个范式将是全球分布式的、安全的、最终一致性的编程。互联网要求这样。我们当前几乎所有的编程语言，包括JavaScript，仍然牢固地植根于旧的局部、不安全、顺序编程的范式。我视JavaScript为一门过渡性语言。采纳JavaScript的最佳实践将为理解下一个范式打下良好的基础。

## 英语

数字1的单词拼错了。我使用正确的拼写 **wun**。*one*的发音不符合英语发音的任何标准或特殊规则。而且让数字1的单词以看起来像0的字母开头，这是一个缺陷。

**wun**的拼写对你来说不熟悉，所以它可能*感觉*不对。我这样做是故意的，是为了让你练习这个理念：对不熟悉事物的不好感觉并非它是错误的证明。

这就是拼写改革发生的方式。例如，某个家伙认为如果*through*拼写成*thru*会更好，因为一个流行单词中一半字母都不发音，这毫无道理，极其低效，并给语言学习者带来了不必要的负担。拼写改革是传统与理性之间的斗争，有时，理性会胜出。我对编程语言也有同样的看法。所以如果*wun*对你来说比*one*更有意义，那么请加入我的努力。

当普通人谈论范围时，比如*1 to 10*，这个范围被理解为以*10*结束。但程序员通常用*to*来表示不包括*10*。这种混淆源于常见的从*0*而非*1*开始编号的编程实践。所以我用**to**表示程序员通常用**to**所指的含义，而用**thru**表示普通人用**to**所指的含义。因此，*0 to 3*表示包含*0 1 2*的范围，而*0 thru 3*表示包含*0 1 2 3*的范围。**To**意味着 < *小于*，而**thru**意味着 <= *小于或等于*。

既然谈到了**whilst**，在这本关于编程的书中，**while**用于讨论迭代。当讨论并发或同时性时，我使用**whilst**，我将其理解为*同时*。

**cannot**和**can not**都是可接受的拼写，但**cannot**更受欢迎。**Hasnot**不可接受，而**has not**是。**Willnot**不可接受，而**will not**是。这就是为什么我不能使用**cannot**。但如果我非常匆忙，我仍然可以**can't**。

致我的许多英语非母语的朋友们：欢迎。感谢你们阅读我的书。也许不太公平，但英语已成为互联网和软件开发的语言。你们能够直接阅读原始文档是一项重要而宝贵的技能。我对此深表敬意。

### 示例

我使用正则表达式。不幸的是，正则表达式极其晦涩难懂。我将尝试通过在其中添加大量空格来稍微缓解这个问题。JavaScript不允许这些空格，所以当你看到

```
const number_pattern = /
    ^
    ( -? \d+ )
    (?: \. ( \d* ) )?
    (?:
        [ e E ]
        ( [ + \- ]? \d+ )
    )?
    $
/;
```

要知道它应该紧凑地写成

```
const number_pattern = /^(−?\d+)(?:\.(\d*))?(?:[eE]([+\-]?\d+))?$/;
```

我不想让你经受如此难以印刷的丑陋，所以我插入了空格。

在许多章节中，我将展示JavaScript表达式的例子。我通过使用一个特殊的表达式语句来实现，该语句不以`;分号`结束，而是以`//双斜杠`后跟表达式的结果结束。

```
// 示例的例子

3 + 4 === 7                                             // true
NaN === NaN                                             // false
typeof NaN                                              // "number"
typeof null                                             // "object"
0.1 + 0.2 === 0.3                                       // false
3472073 ** 7 + 4627011 ** 7 === 4710868 ** 7            // true
```

在结束之前，一切都会得到解释。

# 第1章

## 名字是如何工作的

你知道我的名字。
*约翰·列侬与保罗·麦卡特尼*

JavaScript希望你为你的变量、属性，有时是函数，提供名字（或标识符）。JavaScript不限制变量名的长度，所以请慷慨地使用。尽可能地，让你的程序自己讲述其故事。不要使用晦涩的名字。

我最初由数学家教授编程，然后我进入了一家使用BASIC编程的计算机制造公司工作。在那个时代，BASIC变量名是单个大写字母和一个可选的数字，比如A1。我养成了一个非常不好的习惯，使用单字母变量名。几十年后，我仍在为此挣扎。一旦错误的东西进入你的脑海，就真的很难纠正。我们永远不应停止努力变得更聪明。数学家喜欢简洁而晦涩的符号。我们通过惨痛的经验认识到，编程应该力求易读和自我解释。编程不是数学。它是一种不同类型的艺术。

让你的所有名字以字母开头，并以字母结尾。JavaScript允许名字以`_`下划线或`$`美元符号开头，或以`_`下划线或`$`美元符号或数字结尾。JavaScript允许许多你真正不应该做的事情。这些技巧应该保留给代码生成器和宏处理器。人类应该做得更好。

开头或结尾的`_`下划线有时意在表示一个公共属性或一个全局变量，如果程序编写正确的话，它应该是私有的。所以，一个悬挂的`_`下划线是一个标志，表明编码者能力不足。

`$`美元符号被添加到语言中，供代码生成器、转译器和宏处理器使用，这样它们可以生成保证不会与你的名字冲突的名字。如果你不是程序，就不要使用`$`美元符号。

名字中的末尾数字通常表明程序员没有对这个名字进行足够的思考。

我给我的*序数*变量起名为**thing_nr**。我给我的*基数*变量起名为**nr_things**。



## 命名规则

使用包含多个单词的名称是好的，但由于名称中不允许使用空格，如何做到这一点几乎没有一致意见。有一个学派坚持使用驼峰命名法，即将单词的首字母大写以标示单词边界。另有一个学派坚持应该用_下划线代替空格来显示单词边界。还有第三个学派干脆把所有单词连在一起，丢失了单词边界。这些学派无法就最佳实践达成一致。这场争论已经持续了多年，而且似乎并没有接近任何共识的迹象。那是因为所有学派都是错的。

正确的答案是使用空格来分隔单词。编程语言目前不允许这样做，是因为 20 世纪 50 年代的编译器必须在非常少的千字内存中运行，名称中的空格被视为一种负担不起的奢侈。FORTRAN 实际上做到了这一点，允许名称包含空格，但后来的语言没有遵循这个好榜样，尽管后来的语言（包括 JavaScript）却追随了 FORTRAN 的非常坏的榜样：使用 = 等号作为赋值运算符，以及要求 IF 条件周围使用 ( 左括号和 ) 右括号，而不是要求在结果周围使用 { 左大括号 和 } 右大括号。

我希望下一种语言能做正确的事，允许名称包含空格以提高可读性。我们现在以千兆字节来衡量内存，所以语言设计者现在可以自由地发明更好的语言。在此之前，请在多词名称中使用_下划线。这将是向下一种语言过渡的最简便方式。

JavaScript 中的所有名称都应该以小写字母开头。这是因为 JavaScript 的 new 运算符存在问题。如果函数调用前面加上了 new，那么该函数将作为构造函数调用，否则函数将作为普通函数调用。构造函数和函数的功能可能截然不同。以错误的方式调用构造函数可能导致错误。更令人困惑的是，构造函数和函数看起来完全相同，因此没有自动的方法来检测由于遗漏或多余的 new 而引起的问题。所以我们有一个约定：*所有构造函数都应该以大写字母开头，而其他任何名称都不应该以大写字母开头。*这给了我们一个视觉提示，可以帮助识别错误。

我对这个问题的解决方案更可靠：永远不要使用 `new`。这消除了需要以大写字母开头的名称的必要性。我仍然建议在这种语言中避免首字母大写，因为外面有非常多糟糕的程序仍然在使用 `new`，而且每天都在增加。

## 保留字

这是 JavaScript 的保留字列表：

```
arguments await break case catch class const continue debugger default delete do else enum eval export extends false finally for function if implements import in Infinity instanceof interface let NaN new null package private protected public return static super switch this throw true try typeof undefined var void while with yield
```

记住这个列表。这很重要。这些词都不应该用作变量名或参数名。JavaScript 关于保留字的规则出奇地复杂，所以可能存在一些例外情况，其中少数几个词可以使用。但即使在这些奇怪的情况下，也不要用。

保留字的使用是另一个根源于 20 世纪 50 年代和 60 年代内存短缺的缺陷特性。语言中保留字的存在可以让编译器的工作更简单一些，让它节省几个字节。摩尔定律已经消除了这些短缺，但那种受约束的思维方式依然存在。保留字显然对程序员不利。你记住保留字列表了吗？可能有一个词能完美描述你的变量，但它已经被分配给你从未使用过的糟糕特性，或者可能永远不会实现的特性。保留字对语言设计者也不利，因为脆弱的保留字策略使得以简洁、直接的方式向流行语言添加新特性变得非常困难。我希望下一种语言不会屈尊使用保留字。

# 第 2 章

## 数字是怎么工作的

○○○●○

> 查看那个数字。
*约翰·列侬和保罗·麦卡特尼*

计算机是操纵数字的机器。这从根本上说是计算机唯一能做的。它们似乎在这方面做得很好。我们可以将其他类型的信息映射到数字上。计算机现在几乎调解着所有人类活动。

JavaScript 的数字受到实数的启发，但它们不是实数。我们的许多数学理解和直觉可以应用于 JavaScript 的数字，但不能完全或一致地应用。为了用 JavaScript 编写好的程序，我们必须理解它的数字是如何工作的。

JavaScript 有一个单一的数字类型叫做 **number**。它借用了*IEEE 浮点运算标准（IEEE 754）*，该标准最初是为英特尔的 iAPX-432 处理器开发的。432 包含了许多绝妙的想法，太多了。432 的架构变得如此复杂，以至于未能实现其目标。他们忽略了最好的想法，即简洁性。许多好想法随着 432 一起消亡了。432 的浮点单元被抢救出来，作为 8087 销售，这是 8086 的数学协处理器。它成为 Pentium 和 AMD64 芯片上的标准配置。

JavaScript 经常因只有一种数字类型而受到批评，但这实际上是它最大的优势之一。如果程序员不必浪费时间从一堆类似的类型中进行选择，冒着选择错误而导致隐秘失败的风险，他们会更高效。避免了类型转换错误。避免了 int 类型引起的溢出错误。JavaScript 的整数比 Java 的 int 可靠得多，因为溢出不可能发生。

```
JavaScript: 2147483647 + 1     //  2147483648  完全正确
Java:       2147483647 + 1     // -2147483648  大错特错
```

我们怎么能对建立在随时可能在没有任何警告的情况下严重出错的数字系统上的程序的正确性有信心呢？int 类型不能防止错误，它们会导致错误。

浮点数背后的想法很简单：将一个数字表示为两个数字。第一个数字（有时称为系数、有效数、分数或尾数）包含数字位。第二个数字（称为指数）标识小数点（或二进制点）应该插入第一个数字的位置。浮点数的实现可能相当复杂。复杂性来自于需要在固定格式中有限数量的比特位中获得最佳利用。

### 2.1 数字是怎么工作的

JavaScript 并不使用整个 IEEE 754 标准。它使用的是 Java 所用子集的子集。JavaScript 的 number 与 Java 的 double 非常接近。它是一种 64 位二进制浮点类型。一个数字包含一个符号位、11 个指数位和 53 个有效数位。一些巧妙的编码允许将这 65 位打包到 64 位的字中。

IEEE 754，像它之前的许多浮点系统一样，选择了一个基数为 2 的系统。第一个数字被分成两部分——符号和有效数。符号放在 64 位中的最高有效位。如果数字为负，则为 1。有效数放在最低有效位中。它通常表示范围内的二进制分数

```
0.5 <= significand < 1.0
```

在这种形式中，最高有效位总是 1。由于该位总是 1，它不需要存储在数字中。这就产生了额外的 bonus 位。

第二个数字是指数。它填充在符号和有效数之间的空间。数字的值将是

```
sign * significand * (2 ** exponent)
```

但还有其他复杂之处。指数表示为 CDDL 偏置有符号幅度整数。这允许假扮该数字是 64 位整数来进行比较。这可以提供显著的性能优势，这在五十年前很重要。指数还可以编码 NaN 和 Infinity 以及非规格化数，这是一种用于表示非常小的数字和零的特殊形式。

## 零

除了零没有零。在一个正确的系统中，只有一个零。IEEE 754 标准包含两个零：0 和 -0。JavaScript 勇敢地努力向你隐瞒这种恶劣现象，而且几乎总是成功。你可以安全地忽略 -0 的存在，除了以下情况：

```
(1 / 0) === (1 / -0)  // false
Object.is(0, -0)      // false
```

我不建议你曾经用任何东西除以零。我不建议你曾经使用 Object.is()。

## 数字字面量

JavaScript 内置了 18437736874454810627 个不可变的数字对象，每个对象唯一地表示一个数字。数字字面量产生一个指向最匹配该字面量值的数字对象的引用。有时它是精确的。在某些情况下，它可能偏离多达 0.0792015476735990582818635651842e+291。

整数的数字字面量就是十进制数字的序列。也可以通过使用基数前缀来形成不同进制的整数字面量。所有这些字面量都产生指向 2018 的引用：

-   二进制：0b11111100010
-   八进制：0o3742
-   十进制：2018.00
-   十六进制：money 0x7E2



JavaScript 允许基数说明符字母使用大写，但在数字字面量中使用大写字母 `O` 肯定会引起混淆。

十进制数字字面量可以包含小数点。非常大或非常小的数字可以用 `e` 紧凑地书写，它将数字乘以十的幂次方。因此，`6.022140857747475e23` 是 `(6.022140857747475 * (10 ** 23))` 的简写，而 `6.626070040818182e-34` 是 `(6.626070040818182 * (10 ** -34))` 的简写。

`Infinity` 是一个表示所有大到无法表示的数字的值。不要将 `Infinity` 与 ∞ 混淆。在数学中，∞ 不是一个值，它是一个比喻。

`NaN` 是一个特殊的值，表示“不是数字”的数字。`NaN` 代表 *Not a Number*（非数字），这令人困惑，因为 `typeof` 运算符正确地报告了 `NaN` 的类型是 `"number"`（数字）。

`NaN` 可能是字符串到数字转换失败的结果。它不会抛出异常或使程序停止，而是返回 `NaN` 值。当算术运算符的操作数之一是 `NaN` 时，它们会产生 `NaN`。

`NaN` 最糟糕的一点是 `NaN` 不等于自身。这是 JavaScript 没有隐藏的 IEEE 754 恶行。测试 `NaN` 与测试所有其他数字值的相等性不同。在编写测试时，这可能是一个隐患。如果期望值是 `NaN`，那么即使实际值也是 `NaN`，测试也总是会失败。要测试一个*值*是否是 `NaN` 或非 `NaN`，请使用 `Number.isNaN(value)`。如果*值*是 `NaN`、`Infinity` 或 `-Infinity`，则 `Number.isFinite(value)` 返回 false。

## Number

`Number`（注意首字母大写的 N）是一个可以生成数字的函数。JavaScript 中的数字是不可变对象。当传入一个数字时，`typeof` 运算符返回 `"number"`（注意首字母小写的 n）。你永远不应该在 `Number` 函数前使用 `new` 前缀。它不会做你可能认为它应该做的事情。

```
const good_example = Number("432");
const bad_example = new Number("432");
typeof good_example                                    // "number"
typeof bad_example                                     // "object"
good_example === bad_example                           // false
```

`Number` 也是一个包含一些常量的容器。这些常量可以提供对数字工作原理的洞察。

`Number.EPSILON` 精确等于 `2.220446049250313080847263336181640625e-16`。它是与 1 相加后产生大于 1 的和的最小正数。将任何小于 `Number.EPSILON` 的正数加到 1 上，其和正好等于 1。将一个不为 0 的数加到 1 上却得到 1，这看起来很荒谬。这不是 JavaScript 中的错误或设计缺陷。所有固定大小的浮点系统（包括 IEEE 754）都有这种怪异之处，这是一个合理的权衡。

`Number.MAX_SAFE_INTEGER` 精确等于 `9007199254740991`，或者用现代计数单位来说大约是 9 万亿亿。JavaScript 没有也不需要整数类型，因为它的数字类型可以精确表示直到 `Number.MAX_SAFE_INTEGER` 的所有整数。JavaScript 的数字类型内有 54 位有符号整数。

## 数字的工作原理

对一个大于 `Number.MAX_SAFE_INTEGER` 的整数加 1，其效果与对该大数加 0 相同。只要所有值、结果和中间结果都是介于 `-Number.MAX_SAFE_INTEGER` 和 `Number.MAX_SAFE_INTEGER` 之间的整数，JavaScript 就能够进行精确的整数运算。在这个范围内，传统的数学推理是成立的，结合律和分配律是有效的。在这个范围之外，情况就更加混乱了。例如，将一系列数字相加的顺序可能会改变总和。因此，`((0.1 + 0.2) + 0.3)` 产生的结果比 `(0.1 + (0.2 + 0.3))` 要大。`Number.isSafeInteger(number)` 如果数字在安全范围内则返回 true。

`Number.isInteger(number)` 如果数字是安全范围内的整数，或者大于安全范围，则返回 true。所有大于 `Number.MAX_SAFE_INTEGER` 的数字都被视为整数。其中一些是精确正确的，大多数则不是。

`Number.MAX_VALUE` 包含了 JavaScript 能表示的最大数字。它精确等于 `Number.MAX_SAFE_INTEGER * 2 ** 971`，即

```
17976931348623157081452742373170435679807056752584499659891747680315726078002853
87605895586327668781715404589535143824642343213268894641827684675467035375169860
49910576551282076245490090389328944075868508455133942304583236903222948165808559
332123348274797826204144723168738177180919299881250404026184124858368
```

也就是 1 后面跟着 308 位数字。其中大部分是虚假精度。这些数字可以提供 15.9 位的有效数字。末尾的 292 位数字是二进制与十进制冲突造成的幻象。

将任何正的安全整数加到 `Number.MAX_VALUE` 上，其和仍然是 `Number.MAX_VALUE`。如果一个程序产生了 `Number.MAX_VALUE` 这样的结果，那么这个程序很可能是错误的。任何超过 `Number.MAX_SAFE_INTEGER` 的结果都值得怀疑。IEEE 754 标准承诺了巨大的潜在范围，但如果不格外小心，它更可能导致错误。

`Number.MIN_VALUE` 是能表示的最小的、大于零的数字。它精确等于 `2 ** -1074`，即

```
4.940656458412465441765687928682213723650598026143247644255856825006755072702087
51865299836361635992379796564695445717730926656710355939796398774796010781878126
3007131903114045278458171678498210368871863605699873072305000638740915356498438
73124733972731696151400317153853980741262385655911710266585566867681870395603106
2493194527159149245532930545654440112748012970999541931989409080416563324524757
1478690147267801593552386115501348035264934720193790268107107491703332268447533
357208324319360923829345836806011506169809753078342277318329247904982524730
7763759272478746560847782037344696995336470179267771758512566055119913150489110
145103786273816725095583738977335989936648099411642057026370902792427675445652290
87538682506419718265533447265625e-324
```

所有小于 `Number.MIN_VALUE` 的正数都与零无法区分。请注意，`Number.MIN_VALUE` 的有效数字在最低有效位只有一个位。这个孤独的位产生了大量的虚假精度。

`Number.prototype` 是所有数字继承的对象。`Number.prototype` 包含一组方法。不幸的是，它不是一个非常有用的方法集。

## 运算符

前缀运算符：

| + | 转数字 | + 加号前缀运算符将其操作数转换为数字。如果转换失败，则产生 NaN。更推荐使用 Number 函数，因为它更明确。 |
| - | 取反 | - 减号前缀运算符改变其操作数的符号。JavaScript 中的数字字面量没有符号。在像 (-1) 这样的表达式中，- 减号是一个运算符，而不是数字字面量的一部分。 |
| typeof | 类型 | 如果操作数是数字，则它产生字符串 "number"，即使操作数是 NaN。 |

中缀运算符：

| + 加号 | 加法 | 不幸的是，+ 加号运算符也被字符串用于连接。这种重载造成了隐患。如果任一操作数是字符串，它会将另一个操作数转换为字符串并将它们连接起来。不幸的是，在此语言中没有其他方法进行加法，所以你必须小心。Number 函数可以帮助确保 + 加号中缀运算符的操作数确实是数字，以便执行加法。 |
| - 减号 | 减法 | |
| * 星号 | 乘法 | |
| / 斜杠 | 除法 | 这不是整数除法。如果你将一个整数除以另一个整数，你可能会得到一个小数结果：5 / 2 结果是 2.5，而不是 2。 |
| % 百分号 | 取余 | JavaScript 没有取模运算符，而是有取余运算符。我认为取模更有用。取余的结果符号来自被除数。取模的结果符号来自除数。-5 % 2 是 -1。 |
| ** 双星号 | 幂运算 | JavaScript 采用了 FORTRAN 的双星号，以赋予该语言一种古雅的老式外观。 |



### 2.5 数值如何运作

## 按位运算符

JavaScript 拥有一组与 C 语言及其他语言类似的按位运算符。它们对 JavaScript 数字进行运算时，会将其转换为有符号 32 位整数，执行按位操作，然后再转换回 JavaScript 数字。如果它们能对 54 位安全整数进行操作会更好，但实际情况并非如此，因此高位的 22 位可能会在毫无警告的情况下丢失。

在某些语言中，移位操作可能用于替代乘除法，或者按位 *and* 可能用作取模运算符。如果你在这种语言中这样做，可能会丢弃最重要的 22 位。在某些情况下你可以侥幸成功，但在某些情况下则不行。

这就是为什么按位运算符在 JavaScript 中的使用频率低于其他语言。但即使不使用它们，它们也是一种语法隐患。**&** *与号* 和 **|** *竖线* 可能与 **&&** *与号与号* 和 **||** *竖线竖线* 混淆。**<<** *小于小于* 和 **>>** *大于大于* 可能与 **<** *小于* 和 **>** *大于* 混淆。我不明白为什么 **>>** *大于大于* 是进行符号扩展的右移，而 **>>>`greater than greater than greater than`** 却不是。在 C 语言中，符号扩展由类型决定。在 Java 中，符号扩展由运算符决定。JavaScript 复制了 Java 的糟糕选择。务必小心。

唯一的按位一元运算符是 **~** *波浪号*，按位取反。

按位二元运算符：

- **&** *与号* 按位与
- **|** *竖线* 按位或
- **^** *脱字符* 按位异或
- **<<** *小于小于* 左移
- **>>>`greater than greater than greater than`** 右移
- **>>** *大于大于* 右移带符号扩展

## Math 对象

**Math** 对象包含一组重要的函数，这些函数本应该内置在 **Number** 中。这是 Java 产生不良影响的又一个例子。

除了三角函数和对数函数之外，它还包含一些本应该作为运算符提供的实用函数。

**Math.floor** 和 **Math.trunc** 都能从数值产生整数。**Math.floor** 给出较小的整数，而 **Math.trunc** 给出更接近零的整数。使用哪一个取决于你希望负数如何被处理。

```
Math.floor(-2.5) // -3
Math.trunc(-2.5) // -2
```

**Math.min** 和 **Math.max** 返回参数中的最小值或最大值。

**Math.random** 返回 **0** 到 **1** 之间的数值。它适用于游戏，但不适用于加密应用或赌场游戏。

## 怪兽

JavaScript 没有提供将数字分解为其组成部分的工具，但我们可以用 JavaScript 轻松编写这样的工具。这样我们就能看到数字的真实本质。

我将使用系数（coefficient）而不是尾数（significand），因为我想完全在整数空间中工作，那里清晰且精确。分数形式的尾数需要更多解释。

```
function deconstruct(number) {
```

此函数分解一个数字，将其还原为组成部分：符号、整数系数和指数，使得

```
number = sign * coefficient * (2 ** exponent)
```

```
    let sign = 1;
    let coefficient = number;
    let exponent = 0;
```

从系数中移除符号。

```
    if (coefficient < 0) {
        coefficient = -coefficient;
        sign = -1;
    }

    if (Number.isFinite(number) && number !== 0) {
```

缩减系数：我们可以通过将数字除以二直到归零来获得指数。我们将除法次数加到 -1128 上，这是 Number.MIN_VALUE 的指数减去尾数的位数再减去 bonus 位。

```
        exponent = -1128;
        let reduction = coefficient;
        while (reduction !== 0) {
```

此循环保证会达到零。每次除法都会递减 reduction 的指数。当指数小到无法继续递减时，内部的非规格化尾数将改为向右移位。最终，所有位都会被移出。

```
            exponent += 1;
            reduction /= 2;
        }
```

缩减指数：当指数为零时，该数字可视为整数。如果指数不为零，则进行调整以校正系数。

```
        reduction = exponent;
        while (reduction > 0) {
            coefficient /= 2;
            reduction -= 1;
        }
        while (reduction < 0) {
            coefficient *= 2;
            reduction += 1;
        }
    }
```

### 2.7 数值如何运作

返回一个包含三个组成部分和原始数字的对象。

```
return {
    sign,
    coefficient,
    exponent,
    number
};
```

现在我们已经装备齐全，可以直接观察这头野兽了。

当我们分解 Number.MAX_SAFE_INTEGER 时，得到

```
{
    "sign": 1,
    "coefficient": 9007199254740991,
    "exponent": 0,
    "number": 9007199254740991
}
```

Number.MAX_SAFE_INTEGER 是能放入有符号 54 位整数的最大数字。

当我们分解 1 时，得到

```
{
    "sign": 1,
    "coefficient": 9007199254740992,
    "exponent": -53,
    "number": 1
}
```

注意 1 * 9007199254740992 * (2 ** -53) 等于 1。

现在我们来试一个棘手的：0.1。十分之一。一角钱。

```
{
    "sign": 1,
    "coefficient": 7205759403792794,
    "exponent": -56,
    "number": 0.1
}
```

当你计算时，1 * 7205759403792794 * 2 ** -56 不是 0.1。它精确等于 0.1000000000000000055511151231257827021181583404541015625。

众所周知，JavaScript 不擅长处理小数，尤其是金钱。当你将 0.1 或大多数其他小数输入程序时，JavaScript 无法精确表示该值，因此它会 *混叠*，用一个它能表示的值来替代。

当你在程序中输入小数点，或读取带有小数点的数据值时，很可能正在向程序中引入微小误差。有时误差小到不被注意。有时误差相互抵消，但有时误差会累积。

```
{
    "sign": 1,
    "coefficient": 5404319552844595,
    "exponent": -54,
    "number": 0.3
}
```

```
{
    "sign": 1,
    "coefficient": 5404319552844596,
    "exponent": -54,
    "number": 0.30000000000000004
}
```

当我们分解 0.3 时，得到的结果与分解 0.1 + 0.2 时不同。

注意，0.299999999999999988897769753748434595763683319091796875 和 0.3000000000000000444089209850062616169452667236328125 都不等于 0.3。

我们再看一个例子。当我们分解 100 / 3 时，得到

```
{
    "sign": 1,
    "coefficient": 9382499223688534,
    "exponent": -48,
    "number": 33.333333333333336
}
```

注意 JavaScript 说该数字是 33.333333333333336。末尾的 6 表明 JavaScript 无法理解正确答案，甚至合理的答案。但真相更糟。JavaScript 实际上认为答案精确等于 33.3333333333333570180911920033395290374755859375。

浮点系统带有在内部二进制表示和人类坚持使用的外部十进制表示之间转换的函数。这些函数旨在尽可能隐藏真相。真正令人担忧的是，如果我们被迫不断面对 IEEE 754 的真相，我们会反抗并要求更合适的替代方案。从实际角度，我们不希望结果中出现那些噪声，也不希望向客户展示这些噪声。这会让我们显得无能。如果我们大家都假装一切正常，那就简单多了。

二进制浮点的首批用户是数学家和科学家。数学家们深知计算机作为有限设备无法精确表示实数，因此他们依赖数值分析技术从有限系统中提取有用结果。科学家们在处理实验数据，而实验数据本身就有噪声，所以二进制浮点的不精确性不构成显著问题。但早期商业用户拒绝了二进制浮点，因为他们的客户和法律要求精确的小数值。当你数钱时，法律要求你必须得到正确的总额。

那是半个多世纪前的事了。从那以后，我们似乎忘记了二进制浮点带来的取舍。我们现在本应该已经转向更好的方案。在 21 世纪，我们无法可靠地将 0.1 加到 0.2 得到 0.3，这是不可原谅的。我希望替代 JavaScript 的语言能拥有一种可以精确表示小数的单一数字类型。这样的系统仍然

无法精确表示实数。任何有限系统都做不到。但它可以精确表示对人类最重要的数：由十进制数字组成的数。

在此期间，请尽量在安全整数范围内工作。我建议将所有货币值转换为以分为单位，这样就能作为整数进行精确处理。这种方法的危险在于与同样不这样做的代码或系统交互时。这种接口错误可能导致结果比实际大一百倍或小一百倍。那确实会非常糟糕。也许通货膨胀会帮到我们，让分变得太不值钱而不值得费心。

当你不得不在安全整数范围之外工作时，包含小数点或*e 十进制指数*的数可能并非完全精确。相近数量级的数相加产生的误差，比不同数量级的数相加要小。这就是为什么对子总计求和比对单个值求和更准确。

# 第三章

## 大整数是如何工作的

> 他说五，我说六。他说八，我说九。他说十，我说十一。我什么都不会停下来。我把它们叫高。我越出越高，越高，越高。
> *奇科·马克思*

关于 JavaScript 的一个常见抱怨是它没有 64 位整数。`int64` 类型可以精确容纳大到 `9223372036854775807` 的整数，这比 JavaScript 数字那可怜的 `Number.MAX_SAFE_INTEGER` 值 `9007199254740991` 还能多出三位数。

认为我们应该直接注入一种新的数字类型的想法存在问题。但这看起来根本不是问题。其他语言有多种数字类型。为什么 JavaScript 不能更像其他语言呢？

当你使用只有单一数字类型的语言时，添加另一种就是一种暴力行为。这会极大地丧失简洁性，并大幅增加产生 bug 的可能性。每一个类型声明和每一次类型转换都是潜在的错误。

还有一个问题：64 位够吗？也许我们应该考虑 72 位、96 位、128 位，或者 256 位。无论你选择哪个数，同样有力的论点是这个数应该更高。

我认为将大整数添加到语言中是个错误。它应该是一个库。大多数语言用户并不需要它们，而且它们也解决不了当前数字存在的最大问题。稍加编程，就没有必要破坏语言。仅凭现有的 JavaScript，我们就能在任何位长下进行精确的整数运算。有很多方法可以做到。我在这里展示的实现在速度或小巧性上没有做优化，而是针对可解释性做了优化。我想展示一个完整的库，但又不想在呈现它时占用太多篇幅。

我打算将大整数存放在数组中。数组是个好选择，因为它们可以有任意大小。（字符串也是个不错的选择，其中每个字符都被视为一个无符号 16 位整数。）数组的每个元素包含一个数，它保存了大整数的部分位。一个重要的设计问题是*每个元素放多少位？*最大的可能答案是 53，即正安全整数的大小。语言提供了动机使其为 32 或更小，因为这允许使用位运算符。如果我们的字长大于 32 位，那么位运算符就无法使用，实现会变得更加复杂。

但即使考虑到乘除法的需求，32 也太大了。在实现大整数乘除法时，我们想利用 JavaScript 的乘法运算符，它只能精确到 53 位。这意味着我们的字长应该不超过它的一半。我选择了 24 位。我本可以选择 26，但我喜欢 24，因为它更圆整。（我的第一个程序运行在 Control Data Corporation 3150 上，一台 24 位的大型机。）我们把这 24 位单位称为**兆位数字**，因为它们能表示的值的数量是 ordinary digit 能表示的值的百万倍以上。

我选择了符号幅值表示法。数组的第零个元素包含数的符号，要么是 "+"，要么是 "-"。第一个元素包含最低有效兆位数字。最后一个元素包含最高有效兆位数字。所以 900000000000000000 看起来像这样：

["+", 8650752, 7098594, 31974]

这不太美观，但它有效，因为

900000000000000000 = 8650752 + ((7098594 + (31974 * 16777216)) * 16777216)

我创建了一些常量和函数，以便更容易访问大整数的内部特性。

```
const radix = 16777216;
const radix_squared = radix * radix;
const log2_radix = 24;
const plus = "+";
const minus = "-";
const sign = 0;
const least = 1;

function last(array) {
    return array[array.length - 1];
}

function next_to_last(array) {
    return array[array.length - 2];
}
```

我们创建一些常量。我们其实并不需要这些，但它们能让代码读起来更好一点。

```
const zero = Object.freeze([plus]);
const wun = Object.freeze([plus, 1]);
const two = Object.freeze([plus, 2]);
const ten = Object.freeze([plus, 10]);
const negative_wun = Object.freeze([minus, 1]);
```

我们需要谓词函数来检测大整数和负大整数。

```
function is_big_integer(big) {
    return Array.isArray(big) && (big[sign] === plus || big[sign] === minus);
}

function is_negative(big) {
    return Array.isArray(big) && big[sign] === minus;
}
```

```
function is_positive(big) {
    return Array.isArray(big) && big[sign] === plus;
}
```



## 大整数是如何工作的

```
},
    false
)
    : comparahend.length < comparator.length
);
}

function lt(comparahend, comparator) {
    return (
        comparahend[sign] !== comparator[sign]
        ? is_negative(comparahend)
        : (
            is_negative(comparahend)
            ? abs_lt(comparator, comparahend)
            : abs_lt(comparahend, comparator)
        )
    );
}
```

一旦有了 `lt` 函数，你就可以通过取反和交换轻松实现其他比较操作：

```
function ge(a, b) {
    return !lt(a, b);
}

function gt(a, b) {
    return lt(b, a);
}

function le(a, b) {
    return !lt(b, a);
}
```

现在我们来制作位运算函数。我们的每个大整数都包含若干位。我们假设符号与位运算无关，因此输入时忽略符号，输出时为"+"。

我们的第一个位运算是与、或和异或。`and` 函数处理较短的数组。`and` 函数不关心较长数组中多余的字。这些多余的字与零进行与运算后消失。`or` 和 `xor` 函数则处理较长的数组。

```
function and(a, b) {

// 将 a 设为较短的数组。

if (a.length > b.length) {
    [a, b] = [b, a];
}
return mint(a.map(function (element, element_nr) {
    return (
        element_nr === sign
        ? plus
        : element & b[element_nr]
    );
}));
}
```

### 3.5 大整数是如何工作的

```
function or(a, b) {

// 将 a 设为较长的数组。

if (a.length < b.length) {
    [a, b] = [b, a];
}
return mint(a.map(function (element, element_nr) {
    return (
        element_nr === sign
        ? plus
        : element | (b[element_nr] || 0)
    );
}));
}
```

```
function xor(a, b) {

// 将 a 设为较长的数组。

if (a.length < b.length) {
    [a, b] = [b, a];
}
return mint(a.map(function (element, element_nr) {
    return (
        element_nr === sign
        ? plus
        : element ^ (b[element_nr] || 0)
    );
}));
}
```

我们的一些函数接受一个小整数作为参数。`int` 函数使得处理数字和大整数都变得容易。

```
function int(big) {
    let result;
    if (typeof big === "number") {
        if (Number.isSafeInteger(big)) {
            return big;
        }
    } else if (is_big_integer(big)) {
        if (big.length < 2) {
            return 0;
        }
        if (big.length === 2) {
            return (
                is_negative(big)
                ? -big[least]
                : big[least]
            );
        }
        if (big.length === 3) {
            result = big[least + 1] * radix + big[least];
            return (
                is_negative(big)
                ? -result
                : result
            );
        }
        if (big.length === 4) {
            result = (
                big[least + 2] * radix_squared
                + big[least + 1] * radix
                + big[least]
            );
            if (Number.isSafeInteger(result)) {
                return (
                    is_negative(big)
                    ? -result
                    : result
                );
            }
        }
    }
}
```

`shift_down` 函数通过删除最低有效位来缩小数字。这可以使大整数变小。它类似于除以 2 的幂。这个操作通常被称为*右移*（>>>），这有点令人困惑，因为它使用了*大于*符号却让数字变小。位的编号完全是任意的，因此位从右到左增长的概念是令人困惑的。我们从数组中构造值，而数组通常被认为是从左到右增长的，所以我们同时从右到左和从左到右增长。此外，一些书写系统是从左到右的，另一些是从右到左的，所以左和右的自然性并非普遍。*字节序问题*（Endianness Problem）的根源就在于这种混淆。右移和左移不如缩小和扩大精确。

如果移动位数是 24 的倍数，那么移位是容易的。否则，我们需要重新对齐所有位。

```
function shift_down(big, places) {
    if (is_zero(big)) {
        return zero;
    }
    places = int(places);
    if (Number.isSafeInteger(places)) {
        if (places === 0) {
            return abs(big);
        }
        if (places < 0) {
            return shift_up(big, -places);
        }
        let skip = Math.floor(places / log2_radix);
        places -= skip * log2_radix;
        if (skip + 1 >= big.length) {
            return zero;
        }
        big = (
            skip > 0
            ? mint(zero.concat(big.slice(skip + 1)))
            : big
        );
        if (places === 0) {
            return big;
        }
        return mint(big.map(function (element, element_nr) {
            if (element_nr === sign) {
                return plus;
            }
            return (((radix - 1) & (
                (element >> places)
                | (((big[element_nr + 1] || 0) << (log2_radix - places))
            )));
        }));
    }
}
```

`shift_up` 函数通过在最低有效位端插入零来扩大数字。它类似于乘以 2 的幂。这可以使大整数变大。在大多数系统中，当位被移出数字的容量时可能会丢失，但在这个系统中，容量是无限的，因此没有位会丢失。

```
function shift_up(big, places) {
    if (is_zero(big)) {
        return zero;
    }
    places = int(places);
    if (Number.isSafeInteger(places)) {
        if (places === 0) {
            return abs(big);
        }
        if (places < 0) {
            return shift_down(big, -places);
        }
        let blanks = Math.floor(places / log2_radix);
        let result = new Array(blanks + 1).fill(0);
        result[sign] = plus;
        places -= blanks * log2_radix;
        if (places === 0) {
            return mint(result.concat(big.slice(least)));
        }
        let carry = big.reduce(function (accumulator, element, element_nr) {
            if (element_nr === sign) {
                return 0;
            }
            result.push(((element << places) | accumulator) & (radix - 1));
            return element >> (log2_radix - places);
        }, 0);
        if (carry > 0) {
            result.push(carry);
        }
        return mint(result);
    }
}
```

我们希望有一个 `not` 函数来对所有位取反，但我们没有位数的限制，因此不清楚应该翻转多少位。所以我们有一个 `mask` 函数，它生成一个具有特定数量 1 位的大整数。然后我们可以使用 `mask` 和 `xor` 来实现 `not`，但 `not` 必须知道位域的大小。

```
function mask(nr_bits) {

// 生成一个由 1 位组成的字符串。

nr_bits = int(nr_bits);
if (nr_bits !== undefined && nr_bits >= 0) {
    let mega = Math.floor(nr_bits / log2_radix);
    let result = new Array(mega + 1).fill(radix - 1);
    result[sign] = plus;
    let leftover = nr_bits - (mega * log2_radix);
    if (leftover > 0) {
        result.push((1 << leftover) - 1);
    }
    return mint(result);
}
}
```

```
function not(a, nr_bits) {
    return xor(a, mask(nr_bits));
}
```

`random` 函数生成一个大的随机整数。它接受要生成的位数，以及一个可选的随机数生成器函数，该函数返回一个介于 0 和 1 之间的数字。如果没有传入随机数生成器函数，它将使用 `Math.random`，这对于大多数用途来说没问题，但不适用于密码学应用。

```
function random(nr_bits, random = Math.random) {

// 生成一个随机位字符串。如果你关心安全性，
// 可以传入一个更强的随机数生成器。

// 首先生成一个由 1 位组成的字符串。

const wuns = mask(nr_bits);
if (wuns !== undefined) {

// 对于每个大数字位，获取一个介于 0.0 和 1.0 之间的随机数。
// 取一些高位和低位并将它们异或在一起。
// 然后与这个大数字位进行与运算，并放入新数字中。

return mint(wuns.map(function (element, element_nr) {
    if (element_nr === sign) {
        return plus;
    }
    const bits = random();
    return ((bits * radix_squared) ^ (bits * radix)) & element;
}));
}
```

我们进行加法的方式与你在学校学到的相同，只是我们使用的是基数 16777216 而不是基数 10。我们使用闭包将进位传递给加法器。

```
function add(augend, addend) {
    if (is_zero(augend)) {
        return addend;
    }
    if (is_zero(addend)) {
        return augend;
    }
```

如果符号不同，那么将其转化为减法问题。



 ## 3.9 大整数的工作原理

```
if (augend[sign] !== addend[sign]) {
    return sub(augend, neg(addend));
}
```

符号相同。将所有位相加，结果赋予相同的符号。我们可以对不同长度的数字进行加法运算。我们将 `.map` 应用于较长的那个数，并使用 `||` 运算符将不存在的元素替换为零。

```
if (augend.length < addend.length) {
    [addend, augend] = [augend, addend];
}
let carry = 0;
let result = augend.map(function (element, element_nr) {
    if (element_nr !== sign) {
        element += (addend[element_nr] || 0) + carry;
        if (element >= radix) {
            carry = 1;
            element -= radix;
        } else {
            carry = 0;
        }
    }
    return element;
});
```

如果数字溢出了，那么追加另一个元素来存储进位。

```
if (carry > 0) {
    result.push(carry);
}
return mint(result);
}
```

减法同样简单直接。

```
function sub(minuend, subtrahend) {
    if (is_zero(subtrahend)) {
        return minuend;
    }
    if (is_zero(minuend)) {
        return neg(subtrahend);
    }
    let minuend_sign = minuend[sign];
```

如果符号不同，将其转化为加法问题。

```
if (minuend_sign !== subtrahend[sign]) {
    return add(minuend, neg(subtrahend));
}
```

用较大的数减去较小的数。

```
if (abs_lt(minuend, subtrahend)) {
    [subtrahend, minuend] = [minuend, subtrahend];
    minuend_sign = (
        minuend_sign === minus
        ? plus
        : minus
    );
}
let borrow = 0;
```

```
return mint(minuend.map(function (element, element_nr) {
    if (element_nr === sign) {
        return minuend_sign;
    }
    let diff = element - ((subtrahend[element_nr] || 0) + borrow);
    if (diff < 0) {
        diff += 16777216;
        borrow = 1;
    } else {
        borrow = 0;
    }
    return diff;
}));
```

乘法稍微复杂一些。我们使用嵌套的 `forEach` 函数，因为必须将乘数（multiplicand）的每个元素与被乘数（multiplier）的每个元素相乘。这些乘积中的每一个都可能是 48 位的，但一个元素只能容纳 24 位，因此溢出必须进位。

```
function mul(multiplicand, multiplier) {
    if (is_zero(multiplicand) || is_zero(multiplier)) {
        return zero;
    }
```

如果符号匹配，结果的符号将为正。

```
let result = [
    multiplicand[sign] === multiplier[sign]
    ? plus
    : minus
];
```

将乘数的每个元素乘以被乘数的每个元素，传播进位。

```
multiplicand.forEach(function (
    multiplicand_element,
    multiplicand_element_nr
) {
    if (multiplicand_element_nr !== sign) {
        let carry = 0;
        multiplier.forEach(function (
            multiplier_element,
            multiplier_element_nr
        ) {
            if (multiplier_element_nr !== sign) {
                let at = (
                    multiplicand_element_nr + multiplier_element_nr - 1
                );
                let product = (
                    (multiplicand_element * multiplier_element)
                    + (result[at] || 0)
                    + carry
                );
                result[at] = product & 16777215;
                carry = Math.floor(product / radix);
            }
        });
    }
});
```

```
if (carry > 0) {
    result[multiplicand_element_nr + multiplier.length - 1] = carry;
}
});
return mint(result);
}
```

`divrem` 函数执行除法，同时返回商和余数。为了方便起见，我们还提供了 `div` 函数，仅返回商。

```
function divrem(dividend, divisor) {
    if (is_zero(dividend) || abs_lt(dividend, divisor)) {
        return [zero, dividend];
    }
    if (is_zero(divisor)) {
        return undefined;
    }
}
```

将操作数变为正数。

```
let quotient_is_negative = dividend[sign] !== divisor[sign];
let remainder_is_negative = dividend[sign] === minus;
let remainder = dividend;
dividend = abs(dividend);
divisor = abs(divisor);
```

我们像你在学校学的那样进行长除法。我们估算商的下一个数字。我们从被除数中减去除数与该估算值的乘积，然后再继续。我们使用的是以 16777216 为底，而不是以 10 为底，并且在预测商的下一个数字时更加系统化。

为了提高预测的准确性，我们首先对除数进行 `mint` 处理。将其左移，直到其最高有效位为 1。同时将被除数左移相同的位数。参见《计算机程序设计艺术》中的算法 4.3.1D。

为了确定移位位数，我们找出前导零位的数量。`clz32` 函数计算 32 位字段中的前导零位数，但我们只关心 24 位字段，因此减去 8。

```
let shift = Math.clz32(last(divisor)) - 8;

dividend = shift_up(dividend, shift);
divisor = shift_up(divisor, shift);
let place = dividend.length - divisor.length;
let dividend_prefix = last(dividend);
let divisor_prefix = last(divisor);
if (dividend_prefix < divisor_prefix) {
    dividend_prefix = (dividend_prefix * radix) + next_to_last(dividend);
} else {
    place += 1;
}
divisor = shift_up(divisor, (place - 1) * 24);
let quotient = new Array(place + 1).fill(0);
quotient[sign] = plus;
while (true) {
```

估算值不会太小，但可能太大。如果太大，那么从被除数中减去估算值与除数的乘积会产生负数。当这种情况发生时，将估算值调小并重试。

```
let estimated = Math.floor(dividend_prefix / divisor_prefix);
if (estimated > 0) {
    while (true) {
        let trial = sub(dividend, mul(divisor, [plus, estimated]));
        if (!is_negative(trial)) {
            dividend = trial;
            break;
        }
    }
    estimated -= 1;
}
```

修正后的估算值存入商中。如果那是最后一位，则继续下一步。

```
quotient[place] = estimated;
place -= 1;
if (place === 0) {
    break;
}
```

准备下一位。用剩余被除数的前两个字更新 `dividend_prefix`，并将除数缩微。

```
if (is_zero(dividend)) {
    break;
}
dividend_prefix = last(dividend) * radix + next_to_last(dividend);
divisor = shift_down(divisor, 24);
```

修正余数。

```
quotient = mint(quotient);
remainder = shift_down(dividend, shift);
return [
    (
        quotient_is_negative
        ? neg(quotient)
        : quotient
    ),
    (
        remainder_is_negative
        ? neg(remainder)
        : remainder
    )
];
```

```
function div(dividend, divisor) {
    let temp = divrem(dividend, divisor);
    if (temp) {
        return temp[0];
    }
}
```

使用平方求幂法，将整数提升到整数次幂很容易。

```
function power(big, exponent) {
    let exp = int(exponent);
    if (exp === 0) {
        return wun;
    }
    if (is_zero(big)) {
        return zero;
    }
    if (exp === undefined || exp < 0) {
        return undefined;
    }
    let result = wun;
    while (true) {
        if ((exp & 1) !== 0) {
            result = mul(result, big);
        }
        exp = Math.floor(exp / 2);
        if (exp < 1) {
            break;
        }
        big = mul(big, big);
    }
    return mint(result);
}
```

我们将使用 `gcd` 函数来约简分数。

```
function gcd(a, b) {
    a = abs(a);
    b = abs(b);
    while (!is_zero(b)) {
        let [ignore, remainder] = divrem(a, b);
        a = b;
        b = remainder;
    }
    return a;
}
```

我们需要一些函数来将数字和字符串转换为大整数，以及反向转换。在进行字符串与数字之间的转换时，我们显然希望支持十进制表示法，但我们也希望支持二进制、八进制、十六进制、Base32 和 Base32 校验和。你可以在 crockford.com/wrmg/base32.html 找到更多关于 Base32 的信息。

`digitset` 字符串允许我们将数字映射到字符。`charset` 对象将字符映射到数字。十六进制、十进制、八进制和二进制可以使用同一字符映射的子集。

```
const digitset = "0123456789ABCDEFGHIJKMNPQRSTVWXYZ*~-$=U";
const charset = (function (object) {
    digitset.split("").forEach(function (element, element_nr) {
        object[element] = element_nr;
    });
    return Object.freeze(object);
}(Object.create(null)));
```



# 第四章

## 大浮点数的工作原理

> 不要做英雄，年轻人。
这毫无意义。
*哈伦·波特*

大整数系统可以解决许多问题，但它显然仅限于整数，而有一些问题是整数无法解决的。因此，让我们构建一个大浮点数系统。浮点数系统涉及三个数：一个*系数*、一个*指数*和一个*基数*。这三个数确定一个值。

*值 = 系数 * (基数 ** 指数)*

JavaScript 用于其数字的 IEEE 754 格式，其基数为 2。这提供了硬件实现在 1950 年代可行的好处。摩尔定律已经消除了使 2 成为唯一合理基数的限制，因此让我们考虑其他可能性。

我们的大整数包对 2 ** 24 有亲和性。如果我们把 16777216 作为基数，那么某些对齐操作只需在数组中插入或删除元素即可。这可能提供非常好的性能。而且它与为了性能而牺牲正确性的非常流行的做法是一致的。

我认为基数应该是 10。如果基数是 10，那么所有十进制小数都可以精确表示。这很重要，因为大多数人使用十进制小数，所以基数为 10 的浮点数系统对人类是友好的。

大整数是系数的理想表示。浮点数系统的大部分怪异之处都是由于大小限制。如果大小是无界的，那么怪异之处就很少。既然怪异之处可能导致错误，那么在我们能够的时候，最好将其消除。

我们也可以为指数使用大整数，但那是大材小用。JavaScript 的数字将完全足够。在 `Number.MAX_SAFE_INTEGER` 成为限制之前，我们就会耗尽千兆字节的内存。

我们将大浮点数表示为具有 `coefficient` 和 `exponent` 属性的对象。

有了大整数，浮点数实际上并不复杂。

```
import big_integer from "./big_integer.js";
```

`is_big_float` 函数用于标识一个大浮点数对象。

### 4.1 大浮点数的工作原理

```
function is_big_float(big) {
    return (
        typeof big === "object"
        && big_integer.is_big_integer(big.coefficient)
        && Number.isSafeInteger(big.exponent)
    );
}
```

```
function is_negative(big) {
    return big_integer.is_negative(big.coefficient);
}
```

```
function is_positive(big) {
    return big_integer.is_positive(big.coefficient);
}
```

```
function is_zero(big) {
    return big_integer.is_zero(big.coefficient);
}
```

单个零值表示所有零。

```
const zero = Object.create(null);
zero.coefficient = big_integer.zero;
zero.exponent = 0;
Object.freeze(zero);
```

```
function make_big_float(coefficient, exponent) {
    if (big_integer.is_zero(coefficient)) {
        return zero;
    }
    const new_big_float = Object.create(null);
    new_big_float.coefficient = coefficient;
    new_big_float.exponent = exponent;
    return Object.freeze(new_big_float);
}
```

```
const big_integer_ten_million = big_integer.make(10000000);
```

`make` 函数接受一个数字或字符串以及一个可选的基数，并返回一个大整数。这些转换对于所有整数值都是精确的。

```
function make(value, radix_2_37) {
    let result;
    if (typeof value === "string") {
        let radish;
        if (radix_2_37 === undefined) {
            radix_2_37 = 10;
            radish = ten;
        } else {
            if (
                !Number.isInteger(radix_2_37)
                || radix_2_37 < 2
                || radix_2_37 > 37
            ) {
                return undefined;
            }
            radish = make(radix_2_37);
        }
        result = zero;
        let good = false;
        let negative = false;
        if (value.toUpperCase().split("").every(
            function (element, element_nr) {
                let digit = charset[element];
                if (digit !== undefined && digit < radix_2_37) {
                    result = add(mul(result, radish), [plus, digit]);
                    good = true;
                    return true;
                }
                if (element_nr === sign) {
                    if (element === plus) {
                        return true;
                    }
                    if (element === minus) {
                        negative = true;
                        return true;
                    }
                }
                return digit === "_";
            }
        ) && good) {
            if (negative) {
                result = neg(result);
            }
            return mint(result);
        }
        return undefined;
    }
    if (Number.isInteger(value)) {
        let whole = Math.abs(value);
        result = [(value < 0)]
        ? minus
        : plus
    ];
    while (whole >= radix) {
        let quotient = Math.floor(whole / radix);
        result.push(whole - (quotient * radix));
        whole = quotient;
    }
    if (whole > 0) {
        result.push(whole);
    }
    return mint(result);
}
    if (Array.isArray(value)) {
        return mint(value);
    }
}
```

`number` 函数将大整数转换为 JavaScript 数字。如果值在安全整数范围内，转换是精确的。

```
function number(big) {
    let value = 0;
    let the_sign = 1;
    let factor = 1;
    big.forEach(function (element, element_nr) {
        if (element_nr === 0) {
            if (element === minus) {
                the_sign = -1;
            }
        } else {
            value += element * factor;
            factor *= radix;
        }
    });
    return the_sign * value;
}
```

`string` 函数将大整数转换为字符串。转换是精确的。

```
function string(a, radix_2_thru_37 = 10) {
    if (is_zero(a)) {
        return "0";
    }
    radix_2_thru_37 = int(radix_2_thru_37);
    if (
        !Number.isSafeInteger(radix_2_thru_37)
        || radix_2_thru_37 < 2
        || radix_2_thru_37 > 37
    ) {
        return undefined;
    }
    const radish = make(radix_2_thru_37);
    const the_sign = (
        a[sign] === minus
        ? "-"
        : ""
    );
    a = abs(a);
    let digits = [];
    while (!is_zero(a)) {
        let [quotient, remainder] = divrem(a, radish);
        digits.push(digitset[number(remainder)]);
        a = quotient;
    }
    digits.push(the_sign);
    return digits.reverse().join("");
}
```

人口统计函数计算大整数中 1 位的数量。这可用于计算汉明距离。

```
function population_32(int32) {
```

计算 32 位整数中 1 位的总数。

计算 16 对比特，产生 16 个两位计数（0、1 或 2）。对于每一对，我们从这对中减去高位，这将两位转换为计数。

```
//       HL - H = count
//        00 - 0 = 00
//        01 - 0 = 01
//        10 - 1 = 01
//        11 - 1 = 10

int32 -= (int32 >>> 1) & 0x55555555;
```

将 8 对两位计数组合，产生 8 个四位计数，范围从 0 到 4。

```
int32 = (int32 & 0x33333333) + ((int32 >>> 2) & 0x33333333);
```

将 4 对四位计数组合，产生 4 个八位计数，范围从 0 到 8。溢出到相邻计数的情况不再可能，因此在加法后我们只需要一次掩码操作。

```
int32 = (int32 + (int32 >>> 4)) & 0x0F0F0F0F;
```

将 2 对八位计数组合，产生 2 个十六位计数，范围从 0 到 16。

```
int32 = (int32 + (int32 >>> 8)) & 0x001F001F;
```

最后，将 2 个十六位计数组合，产生一个范围从 0 到 32 的数字。

```
return (int32 + (int32 >>> 16)) & 0x0000003F;
}
```

```
function population(big) {
```

计算 1 位的总数。

```
return big.reduce(
    function (reduction, element, element_nr) {
        return reduction + (
            element_nr === sign
                ? 0
                : population_32(element)
        );
    },
    0
);
}
```

```
function significant_bits(big) {
```

计算除前导零外的总位数。

```
    return (
        big.length > 1
        ? make((big.length - 2) * log2_radix + (32 - Math.clz32(last(big))))
        : zero
    );
}
```

最后，所有这些好的功能都作为一个模块导出。

```
export default Object.freeze({
    abs,
    abs_lt,
    add,
    and,
    div,
    divrem,
    eq,
    gcd,
    is_big_integer,
    is_negative,
    is_positive,
    is_zero,
    lt,
    make,
    mask,
    mul,
    neg,
    not,
    number,
    or,
    population,
    power,
    random,
    shift_down,
    shift_up,
    significant_bits,
    signum,
    string,
    sub,
    ten,
    two,
    wun,
    xor,
    zero
});
```

你可以通过导入在你的模块中访问大整数对象。

```
import big_integer from "./big_integer.js";
```

number 函数将大浮点数转换为 JavaScript 数字。如果数字超出安全整数区域，则不能保证转换是精确的。我们还尝试从其他类型中提取意义。



## 大浮点数的工作原理

```
function number(a) {
    const result = (
        is_big_float(a)
        ? (
            a.exponent === 0
            ? big_integer.number(a.coefficient)
            : big_integer.number(a.coefficient) * (10 ** a.exponent)
        )
        : (
            typeof a === "number"
            ? a
            : (
                big_integer.is_big_integer(a)
                ? big_integer.number(a)
                : Number(a)
            )
        )
    );
    return (
        Number.isFinite(result)
        ? result
        : undefined
    );
}
```

我们需要一个绝对值函数和一个取反函数。

```
function neg(a) {
    return make_big_float(big_integer.neg(a.coefficient), a.exponent);
}
```

```
function abs(a) {
    return (
        is_negative(a)
        ? neg(a)
        : a
    );
}
```

加法和减法非常简单：我们只需将系数相加，但前提是指数必须相等。如果指数不相等，我们必须使它们一致。由于加法和减法如此相似，我创建了一个生成加法和减法函数的函数。如果你将 `big_integer.add` 传递给 `conform_op`，你就得到了浮点加法函数。如果你将 `big_integer.sub` 传递给 `conform_op`，你就得到了浮点减法函数。

### 4.3 大浮点数的工作原理

```
function conform_op(op) {
    return function (a, b) {
        const differential = a.exponent - b.exponent;
        return (
            differential === 0
                ? make_big_float(op(a.coefficient, b.coefficient), a.exponent)
                : (
                    differential > 0
                        ? make_big_float(
                            op(
                                big_integer.mul(
                                    a.coefficient,
                                    big_integer.power(big_integer.ten, differential)
                                ),
                                b.coefficient
                            ),
                            b.exponent
                        )
                        : make_big_float(
                            op(
                                a.coefficient,
                                big_integer.mul(
                                    b.coefficient,
                                    big_integer.power(big_integer.ten, -differential)
                                )
                            ),
                            a.exponent
                        )
                )
        );
    };
}
```

```
const add = conform_op(big_integer.add);
const sub = conform_op(big_integer.sub);
```

乘法甚至更容易。我们只需将系数相乘，然后将指数相加。

```
function mul(multiplicand, multiplier) {
    return make_big_float(
        big_integer.mul(multiplicand.coefficient, multiplier.coefficient),
        multiplicand.exponent + multiplier.exponent
    );
}
```

除法的难点在于知道何时停止。整数除法停止很容易：当用完数字时停止。固定大小的浮点数也很容易：当用完位时停止。但是使用大整数，没有限制。我们可以一直除下去直到得到精确结果，但无法保证这样的结果总是能达到的。所以我们将决定权交给程序员。`div` 函数接受一个可选的第三个参数，即结果的精度。你指定一个小数位。个位是零。小数位是负数。除法返回的小数位至少和你指定的一样多。默认值是 `-4`，即小数点后四位。

```
function div(dividend, divisor, precision = -4) {
    if (is_zero(dividend)) {
        return zero;
    }
    if (is_zero(divisor)) {
        return undefined;
    }
    let {coefficient, exponent} = dividend;
    exponent -= divisor.exponent;
```

将系数缩放到所需的精度。

```
    if (typeof precision !== "number") {
        precision = number(precision);
    }
    if (exponent > precision) {
        coefficient = big_integer.mul(
            coefficient,
            big_integer.power(big_integer.ten, exponent - precision)
        );
        exponent = precision;
    }
    let remainder;
    [coefficient, remainder] = big_integer.divrem(
        coefficient,
        divisor.coefficient
    );
```

如有必要，对结果进行舍入。

```
    if (!big_integer.abs_lt(
        big_integer.add(remainder, remainder),
        divisor.coefficient
    )) {
        coefficient = big_integer.add(
            coefficient,
            big_integer.signum(dividend.coefficient)
        );
    }
    return make_big_float(coefficient, exponent);
}
```

如果指数在不丢失精度的情况下尽可能接近零，则大浮点数是规范化的。

```
function normalize(a) {
    let {coefficient, exponent} = a;
    if (coefficient.length < 2) {
        return zero;
    }
```

如果指数为零，则它已经是规范的。

```
    if (exponent !== 0) {
```

如果指数为正，则将系数乘以 10 ** 指数。

```
        if (exponent > 0) {
            coefficient = big_integer.mul(
                coefficient,
                big_integer.power(big_integer.ten, exponent)
            );
            exponent = 0;
        } else {
            let quotient;
            let remainder;
```

当指数为负时，如果系数能被十整除，那么我们就进行除法并将指数加1。

为了加快速度，我们首先尝试一千万的单位，每次减少7个零。

```
            while (exponent <= -7 && (coefficient[1] & 127) === 0) {
                [quotient, remainder] = big_integer.divrem(
                    coefficient,
                    big_integer_ten_million
                );
                if (remainder !== big_integer.zero) {
                    break;
                }
                coefficient = quotient;
                exponent += 7;
            }
            while (exponent < 0 && (coefficient[1] & 1) === 0) {
                [quotient, remainder] = big_integer.divrem(
                    coefficient,
                    big_integer.ten
                );
                if (remainder !== big_integer.zero) {
                    break;
                }
                coefficient = quotient;
                exponent += 1;
            }
        }
    }
    return make_big_float(coefficient, exponent);
}
```

`make` 函数接受一个大整数、字符串或 JavaScript 数字，并将其转换为大浮点数。转换是精确的。请注意，如果参数是错误的 JavaScript 数字，例如 0.1，那么结果同样会是错误的。

### 4.6 大浮点数的工作原理

```
const number_pattern = /
    ^
    ( -? \d+ )
    (?: \. ( \d* ) )?
    (?: e ( -? \d+ ) )?
    $
/;

// 捕获组
//     [1] int
//     [2] frac
//     [3] exp

function make(a, b) {

    //     (big_integer)
    //     (big_integer, exponent)
    //     (string)
    //     (string, radix)
    //     (number)

    if (big_integer.is_big_integer(a)) {
        return make_big_float(a, b || 0);
    }
    if (typeof a === "string") {
        if (Number.isSafeInteger(b)) {
            return make(big_integer.make(a, b), 0);
        }
        let parts = a.match(number_pattern);
        if (parts) {
            let frac = parts[2] || "";
            return make(
                big_integer.make(parts[1] + frac),
                (Number(parts[3]) || 0) - frac.length
            );
        }
    }

    if (typeof a === "number" && Number.isFinite(a)) {
        if (a === 0) {
            return zero;
        }
        let {sign, coefficient, exponent} = deconstruct(a);
        if (sign < 0) {
            coefficient = -coefficient;
        }
        coefficient = big_integer.make(coefficient);
```

### 4.7 大浮点数的工作原理

```
        if (exponent < 0) {
            return normalize(div(
                make(coefficient, 0),
                make(big_integer.power(big_integer.two, -exponent), 0)
            ));
        }
```

如果指数大于零，那么我们可以将系数乘以 2 ** 指数。

```
        if (exponent > 0) {
            coefficient = big_integer.mul(
                coefficient,
                big_integer.power(big_integer.two, exponent)
            );
            exponent = 0;
        }
        return make(coefficient, exponent);
    }
    if (is_big_float(a)) {
        return a;
    }
}
```

`string` 函数将大浮点数转换为字符串。转换是精确的。大部分工作涉及插入小数点和零填充。用于二进制浮点数的类似函数会复杂得多。

```
function string(a, radix) {
    if (is_zero(a)) {
        return "0";
    }
    if (is_big_float(radix)) {
        radix = normalize(radix);
        return (
            (radix && radix.exponent === 0)
            ? big_integer.string(integer(a).coefficient, radix.coefficient)
            : undefined
        );
    }
    a = normalize(a);
    let s = big_integer.string(big_integer.abs(a.coefficient));
    if (a.exponent < 0) {
        let point = s.length + a.exponent;
        if (point <= 0) {
            s = "0".repeat(1 - point) + s;
            point = 1;
        }
        s = s.slice(0, point) + "." + s.slice(point);
    } else if (a.exponent > 0) {
        s += "0".repeat(a.exponent);
    }
    if (big_integer.is_negative(a.coefficient)) {
        s = "-" + s;
    }
    return s;
}
```

表示小数点有两种流行的惯例：句点和逗号。大多数国家使用其中一种。在一个国家内部，用哪种都无所谓。两者都很好。但这对国际交流是一个隐患。



## 4.9 大浮点数的实现原理

我在第2章中使用了这个库来揭示真相。尽管它非常强大，但我认为对于大多数应用来说，一个更常规的固定大小的十进制浮点类型会更加合适。JavaScript 的 number 类型的问题并不在于它的范围或精度有限。问题在于它无法准确表示对人类最有趣的数字：由十进制数字构成的数字。因此，像 DEC64 这样的方案对于下一门语言来说可能是更好的选择。[www.DEC64.com](http://www.DEC64.com)

无论是二进制浮点数还是十进制浮点数，都无法精确表示像 100/3 这样的数。我们将在下一节讨论这个问题。

因为 1,024 可以有两种完全不同的解释。我预测我们最终会采用*点号*作为国际标准，因为编程语言使用*点号*，而且最终大多数信息都通过这些用这些语言编写的程序来传递。

scientific 函数将大浮点数转换为使用 e 记数法的字符串。

```
function scientific(a) {
    if (is_zero(a)) {
        return "0";
    }
    a = normalize(a);
    let s = big_integer.string(big_integer.abs(a.coefficient));
    let e = a.exponent + s.length - 1;
    if (s.length > 1) {
        s = s.slice(0, 1) + "." + s.slice(1);
    }
    if (e !== 0) {
        s += "e" + e;
    }
    if (big_integer.is_negative(a.coefficient)) {
        s = "-" + s;
    }
    return s;
}
```

最后，所有这些优点都被导出为一个模块。

```
export default Object.freeze({
    abs,
    add,
    div,
    eq,
    fraction,
    integer,
    is_big_float,
    is_negative,
    is_positive,
    is_zero,
    lt,
    make,
    mul,
    neg,
    normalize,
    number,
    scientific,
    string,
    sub,
    zero
});
```

这是一个适用于计算器、财务处理或任何需要正确处理小数分数活动的库。目前它还相当精简，但可以通过添加你可能需要的所有函数和操作符来增强。

# 第5章

## 大分数数的实现原理

我只学了普通课程。开始当然是旋圈和扭动，然后是算术的不同分支——野心、分心、丑化和嘲弄。

*《假海龟》*

有理数是可以表示为两个整数之比的数。如果这两个整数是大整数，这就可以成为一种非常好的数字表示方式。它能精确表示二进制浮点数能表示的一切。它能精确表示十进制浮点数能表示的一切。而且它还能精确表示其他表示法无法表示的所有有理数。

有理数系统涉及两个数——分子和分母。这两个数决定了一个值。

*值 = 分子 / 分母*

我们的有理数值是具有 numerator 和 denominator 属性的对象，两者都是大整数。值的符号由分子的符号决定。分母不能为负。

这是一种非常好的算术运算方式。我们可以在大整数之上构建实现。

```
import big_integer from "./big_integer.js";
```

我们从一些谓词函数开始。

```
function is_big_rational(a) {
    return (
        typeof a === "object"
        && big_integer.is_big_integer(a.numerator)
        && big_integer.is_big_integer(a.denominator)
    );
}
```

```
function is_integer(a) {
    return (
        big_integer.eq(big_integer.wun, a.denominator)
        || big_integer.is_zero(
            big_integer.divrem(a.numerator, a.denominator)[1]
        )
    );
}
```

```
function is_negative(a) {
    return big_integer.is_negative(a.numerator);
}
```

这些是我认为有用的常量。我们可以轻松地添加更多。

```
function make_big_rational(numerator, denominator) {
    const new_big_rational = Object.create(null);
    new_big_rational.numerator = numerator;
    new_big_rational.denominator = denominator;
    return Object.freeze(new_big_rational);
}
const zero = make_big_rational(big_integer.zero, big_integer.wun);
const wun = make_big_rational(big_integer.wun, big_integer.wun);
const two = make_big_rational(big_integer.two, big_integer.wun);
```

我们需要绝对值函数和求反函数。按照惯例，符号在分子中。分母始终为正。

```
function neg(a) {
    return make(big_integer.neg(a.numerator), a.denominator);
}

function abs(a) {
    return (
        is_negative(a)
        ? neg(a)
        : a
    );
}
```

加法和减法非常简单。如果分母相等，我们可以直接加减分子。否则，我们需要进行两次乘法、一次加法，然后再做一次乘法，因为

(a / b) + (c / d) = ((a * d) + (b * c)) / (b * d)

由于加法和减法非常相似，我创建了一个函数来生成 add 和 sub 函数。

```
function conform_op(op) {
    return function (a, b) {
        try {
            if (big_integer.eq(a.denominator, b.denominator)) {
                return make(
                    op(a.numerator, b.numerator),
                    a.denominator
                );
            }
            return normalize(make(
                op(
                    big_integer.mul(a.numerator, b.denominator),
                    big_integer.mul(b.numerator, a.denominator)
                ),
                big_integer.mul(a.denominator, b.denominator)
            ));
        } catch (ignore) {
        }
    };
}
```

```
const add = conform_op(big_integer.add);
const sub = conform_op(big_integer.sub);
```

我们可以通过将分母加到分子上来使有理数递增。

```
function inc(a) {
    return make(
        big_integer.add(a.numerator, a.denominator),
        a.denominator
    );
}
```

```
function dec(a) {
    return make(
        big_integer.sub(a.numerator, a.denominator),
        a.denominator
    );
}
```

乘法很简单。我们只需将分子与分子相乘、分母与分母相乘。除法就是将被第二个参数取倒数后相乘。在有理数系统中，我们很少需要做长除法。我们只要把分母变大就行。

```
function mul(multiplicand, multiplier) {
    return make(
        big_integer.mul(multiplicand.numerator, multiplier.numerator),
        big_integer.mul(multiplicand.denominator, multiplier.denominator)
    );
}
```

```
function div(a, b) {
    return make(
        big_integer.mul(a.numerator, b.denominator),
        big_integer.mul(a.denominator, b.numerator)
    );
}
```

```
function remainder(a, b) {
    const quotient = div(normalize(a), normalize(b));
    return make(
        big_integer.divrem(quotient.numerator, quotient.denominator)[1]
    );
}
```

```
function reciprocal(a) {
    return make(a.denominator, a.numerator);
}
```

```
function integer(a) {
    return (
        a.denominator === wun
        ? a
        : make(big_integer.div(a.numerator, a.denominator), big_integer.wun)
    );
}
```

```
function fraction(a) {
    return sub(a, integer(a));
}
```

我们的 normalize 函数会将分数约分，使其没有公因数。大数的因式分解是一个困难的问题。幸运的是，我们需要约分时并不需要做因式分解。我们只需要找到最大公约数，然后将其除尽。

实际上永远不需要进行约分。约分不会改变值的大小。有理数对象内部的大整数可能会变小，这可能会减少内存消耗（这很少重要），也可能会加快后续的算术运算。

通过对两个分量同时除以它们的最大公约数来约分大分数数。如果它们的最大公约数是 1，那么该数已经是约分后的形式。

```
function normalize(a) {
    let {numerator, denominator} = a;
    if (big_integer.eq(big_integer.wun, denominator)) {
        return a;
    }
    let g_c_d = big_integer.gcd(numerator, denominator);
    return (
        big_integer.eq(big_integer.wun, g_c_d)
        ? a
        : make(
            big_integer.div(numerator, g_c_d),
            big_integer.div(denominator, g_c_d)
        )
    );
}
```

我们不需要通过约分来判断两个值是否相等。如果

a / b = c / d

那么

a * d = b * c

即使它们没有约分。

```
function eq(comparand, comparator) {
    return (
        comparand === comparator
        ? true
        : (
            big_integer.eq(comparand.denominator, comparator.denominator)
            ? big_integer.eq(comparand.numerator, comparator.numerator)
            : big_integer.eq(
                big_integer.mul(comparand.numerator, comparator.denominator),
                big_integer.mul(comparator.numerator, comparand.denominator)
            )
        )
    );
}
```



 ```
function lt(comparahend, comparator) {
    return (
        is_negative(comparahend) !== is_negative(comparator)
        ? is_negative(comparator)
        : is_negative(sub(comparahend, comparator))
    );
}
```

`make` 函数接受一对参数，并生成一个包含分子和分母的对象。此转换是精确的。

它接受一个或两个大整数。它也接受像 "33 1/3" 和 "98.6" 这样的字符串并进行正确转换。它也接受任何有限的 JavaScript 数字，并将其转换为有理数，且不会产生额外的精度损失。

```
const number_pattern = /
    ^
    ( -? )
    (?:
        ( \d+ )
        (?:
            (?:
                \u0020 ( \d+ )
            )?
            \/
            ( \d+ )
        |
            (?:
                \. ( \d* )
            )?
            (?:
                e ( -? \d+ )
            )?
        )
        |
        \. (\d+)
    )
    $
/x;
```

```
function make(numerator, denominator) {
```

如果提供了两个参数，两者都将被转换为大整数。返回值是一个包含分子和分母的对象。

如果只调用一个参数，我们将尝试理解该参数的含义。如果参数是字符串，我们将尝试将其解析为带分数或小数字面量。如果参数是数字，我们将对其进行解构。否则，我们将假设缺失的参数是 1。

```
if (denominator !== undefined) {
```

根据分子和分母生成一个有理数。你可以传入大整数、整数或字符串。

```
    numerator = big_integer.make(numerator);
```

如果分子为零，则无需关心分母。

```
    if (big_integer.zero === numerator) {
        return zero;
    }
    denominator = big_integer.make(denominator);
    if (
        !big_integer.is_big_integer(numerator)
        || !big_integer.is_big_integer(denominator)
        || big_integer.zero === denominator
    ) {
        return undefined;
    }
```

如果分母为负数，则将符号移动到分子上。

```
    if (big_integer.is_negative(denominator)) {
        numerator = big_integer.neg(numerator);
        denominator = big_integer.abs(denominator);
    }
    return make_big_rational(numerator, denominator);
```

参数是字符串吗？如果是，尝试解析它。

```
    if (typeof numerator === "string") {
        let parts = numerator.match(number_pattern);
        if (!parts) {
            return undefined;
        }
```

```
        // 捕获组：
        //      [1] 符号
        //      [2] 整数部分
        //      [3] 分子
        //      [4] 分母
        //      [5] 小数部分
        //      [6] 指数
        //      [7] 纯小数部分
```

```
        if (parts[7]) {
            return make(
                big_integer.make(parts[1] + parts[7]),
                big_integer.power(big_integer.ten, parts[7].length)
            );
        }
        if (parts[4]) {
            let bottom = big_integer.make(parts[4]);
            if (parts[3]) {
                return make(
                    big_integer.add(
                        big_integer.mul(
                            big_integer.make(parts[1] + parts[2]),
                            bottom
                        ),
                        big_integer.make(parts[3])
                    ),
                    bottom
                );
            }
        }
        return make(parts[1] + parts[2], bottom);
```

```
        let frac = parts[5] || "";
        let exp = (Number(parts[6]) || 0) - frac.length;
        if (exp < 0) {
            return make(
                parts[1] + parts[2] + frac,
                big_integer.power(big_integer.ten, -exp)
            );
        }
        return make(
            big_integer.mul(
                big_integer.make(parts[1] + parts[2] + parts[5]),
                big_integer.power(big_integer.ten, exp)
            ),
            big_integer.wun
        );
```

参数是数字吗？如果是，解构它并重新构建。

```
    if (typeof numerator === "number" && !Number.isSafeInteger(numerator)) {
        let {sign, coefficient, exponent} = deconstruct(numerator);
        if (sign < 0) {
            coefficient = -coefficient;
        }
        coefficient = big_integer.make(coefficient);
        if (exponent >= 0) {
            return make(
                big_integer.mul(
                    coefficient,
                    big_integer.power(big_integer.two, exponent)
                ),
                big_integer.wun
            );
        }
        return normalize(make(
            coefficient,
            big_integer.power(big_integer.two, -exponent)
        ));
    }
    return make(numerator, big_integer.wun);
}
```

`number` 函数将一个大有理数转换为 JavaScript 数字。如果该值超出安全整数范围，则转换不保证精确。

```
function number(a) {
    return big_integer.number(a.numerator) / big_integer.number(a.demoninator);
}
```

`string` 函数将一个大有理数转换为字符串。此转换是精确的。

```
function string(a, nr_places) {
    if (a === zero) {
        return "0";
    }
    let {numerator, denominator} = normalize(a);
```

将分子除以分母。如果没有余数，那么我们就得到了结果。

```
    let [quotient, remains] = big_integer.divrem(numerator, denominator);
    let result = big_integer.string(quotient);
    if (remains !== big_integer.zero) {
```

如果提供了 `nr_places`，则结果将以小数格式表示。我们将余数乘以 10 的幂次，然后进行整数除法。如果余数不小于分母的一半，则向上取整。

```
        remains = big_integer.abs(remains);
        if (nr_places !== undefined) {
            let [fractus, residue] = big_integer.divrem(
                big_integer.mul(
                    remains,
                    big_integer.power(big_integer.ten, nr_places)
                ),
                denominator
            );
            if (!big_integer.abs_lt(
                big_integer.mul(residue, big_integer.two),
                denominator
            )) {
                fractus = big_integer.add(fractus, big_integer.wun);
            }
            result += "\." + big_integer.string(fractus).padStart(
                big_integer.number(nr_places),
                "0"
            );
        } else {
```

结果将以带分数的形式表示。

```
            result = (
                (
                    result === "0"
                    ? ""
                    : result + " "
                )
                + big_integer.string(remains)
                + "\/"
                + big_integer.string(denominator)
            );
        }
    }
    return result;
}
```

所有这些功能都作为一个模块导出。

```
export default Object.freeze({
    abs,
    add,
    dec,
    div,
    eq,
    fraction,
    inc,
    integer,
    is_big_rational,
    is_integer,
    is_negative,
    lt,
    make,
    mul,
    neg,
    normalize,
    number,
    wun,
    reciprocal,
    remainder,
    string,
    sub,
    two,
    zero
});
```

你可以通过导入在你的模块中访问大有理数对象。

```
import big_rational from "./big_rational.js";
```

这个有理数库小巧、简单、运行较慢，但功能强大得令人惊讶。它仍然无法精确表示 *π* 或 2 的平方根，但它可以尽可能地接近你想要的精度。例如，

```
const pi = big_rational.make(
    "3141592653589793238462643383279502884197169399375105820974944592307816406",
    "100000000000000000000000000000000000000



## 6.1 How Booleans Work

```
"11" < "2"          // true
"2" < 5             // true
5 < "11"            // true
```

`===` (严格相等) 和 `!==` (严格不等) 通常能正确处理，除了当两个操作数都是 `NaN` 时。`===` 和 `!==` 可以用来判断一个值是否为 `null`、`undefined` 或任何非 `NaN` 的值。要测试 `x` 是否为 `NaN`，请始终使用 `Number.isNaN(x)`。

除非归纳变量在安全整数范围内，否则不应使用 `===` 来测试循环的完成。即便如此，使用 `>=` 也更安全。

当两个操作数都是字符串或都是数字时，`<`、`<=`、`>` 和 `>=` 通常能正确处理。在其他大多数情况下，结果是无意义的。进行比较时请避免混合类型。JavaScript 并不禁止这种混合类型，因此你需要自行约束。

JavaScript 还有一些更不可靠的比较运算符。我建议永远不要使用 `==` (和 `!=`)。它们在比较之前会进行类型强制转换，因此很可能产生误报（和漏报）。始终使用 `===` (和 `!==`) 代替。永远如此。

### Boolish

JavaScript 有一个可爱的布尔类型，但并没有很好地利用它。以下是程序中布尔值能发挥最大作用的位置：

- `if` 语句的条件位置
- `while` 语句的条件位置
- `for` 语句的条件位置
- `do` 语句的条件位置
- `!` 运算符的操作数
- `&&` 运算符的两个操作数
- `||` 运算符的两个操作数
- `? :` 三元运算符的第一个操作数
- 数组方法 `filter`、`find`、`findIndex`、`indexOf` 的函数参数的返回值

在设计良好的语言中，只允许布尔值出现在这些位置。而 JavaScript 却允许任何类型出现在所有这些位置。该语言中的所有值都是 boolish 类型的成员。boolish 类型中的所有值要么是 truthy（真值），要么是 falsy（假值）。

### How Booleans Work

假值（falsy values）是：

- `false`
- `null`
- `undefined`
- `""`（空字符串）
- `0`
- `NaN`

所有其他值都是真值，包括空对象、空数组，以及一些看起来可能是假值的字符串，例如 `"false"` 和 `"0"`。

假值通常表现得像 `false`，但严格来说，它们大多数并不是 `true`。真值通常表现得像 `true`，但严格来说，它们大多数也不是 `true`。这种 boolish 特性是一个错误，但并非偶然。它是为了允许 C 语言的习语出现在 JavaScript 中而有意为之的。

C 是一门类型不健全的语言。它使用一个单一的值来表示 0、FALSE、NULL、字符串结尾以及其他东西。对 C 来说，它们都是一样的。因此，在 if 语句的条件位置，C 只是检查表达式是否为 0。有一种 C 编程风格就是利用这一点来让条件变得简洁。

JavaScript 有一个健全的布尔类型，但 boolish 特性丢弃了大部分价值。条件应该要么是 `true`，要么是 `false`。任何其他值都应该是错误，理想情况下是编译时错误。在 JavaScript 中情况并非如此。条件表达式可以像 C 语言一样简洁和隐晦。意外进入条件位置的值不会被标记为错误。相反，它们可能将程序引向意外的方向。Java 语言要求条件必须是布尔值，从而消除了一类错误。我希望 JavaScript 也能这样。

我建议你编写程序时，就像 JavaScript 是被正确设计的一样。在所有条件中使用布尔值。如果你按照一种更好语言的风格编写，你将写出更好的程序。

### Logical Operators

逻辑运算符也受 boolish 特性的影响。

| 符号 | 名称 | 描述 |
| :--- | :--- | :--- |
| ! 感叹号 | 逻辑非 | 如果操作数是真值，则结果为 ` listener`。如果操作数是假值，则结果为 `true`。 |
| && 双与号 | 逻辑与 | 如果第一个操作数是假值，则结果是第一个操作数，且第二个操作数不会被求值。如果第一个操作数是真值，则结果是第二个操作数。 |
| \|\| 双竖线 | 逻辑或 | 如果第一个操作数是真值，则结果是第一个操作数，且第二个操作数不会被求值。如果第一个操作数是假值，则结果是第二个操作数。 |

### Not!

逻辑表达式可能变得很复杂。有形式化的变换可以简化它们。不幸的是，boolish 特性和 NaN 可能导致形式化变换产生错误。

通常明智的做法是简化双重否定。在逻辑系统中：

```
!!p === p
```

在 JavaScript 中，这只有当 `p` 是布尔值时才成立。如果 `p` 是任何其他类型，那么 `!!p` 等于 `Boolean(p)`，而不一定等于 `p`。

某些比较运算符有相反的运算符，所以 `<` 是 `>=` 的相反，`>` 是 `<=` 的相反。因此，应该可以将 `!(a < b)` 简化为 `a >= b`，因为：

```
!(a === b) === (a !== b)
!(a <= b) === (a > b)
!(a > b) === (a <= b)
!(a >= b) === (a < b)
```

如果 `a` 或 `b` 是 `NaN`，则此代码转换失败。这是因为任何数字与 `NaN` 比较，无论使用哪个比较运算符，结果都是 `false`。所以：

```
7 < NaN                                      // false
NaN < 7                                      // false
!(7 < NaN) === 7 >= NaN                      // false
```

如果 `NaN` 比所有其他数字都小，或者将数字与 `NaN` 比较会引发异常，情况可能会更合理。JavaScript 却实现了无意义的操作。对 `NaN` 唯一有意义的操作是 `Number.isNaN(NaN)`。在所有其他上下文中避免使用 `NaN`。

德摩根定律可以帮助简化逻辑表达式。我经常使用它们：

```
!(p && q) === !p || !q
!(p || q) === !p && !q
```

只要 `p` 和 `q` 没有被无意义的值破坏，这些定律在 JavaScript 中就是健全的。应避免使用 boolish 值。使用布尔值代替。

# Chapter 7

## How Arrays Work

Everything is numbered here.
The monster is Zero.

The Controller of Planet X

数组是最古老的数据结构。数组是一块连续的内存区域，被划分为大小相等的块，每个块都与一个整数关联，并可通过该整数快速访问。JavaScript 在其第一个版本中没有包含数组。这个遗漏几乎未被注意到，因为 JavaScript 的对象如此强大。忽略性能问题，对象可以做到数组能做的一切。

情况依然如此。任何字符串都可以用来索引数组。JavaScript 的数组实际上是对象。在今天的 JavaScript 中，数组与对象在四个方面略有不同：

* 数组有一个神奇的 `length` 属性。数组的 `length` 不一定是数组中元素的数量。相反，它是最高整数序数加 1。这支持了 JavaScript 数组是真正数组的假象，允许使用可能在半世纪前的 C 程序中出现的古老 `for` 语句来处理 JavaScript 数组。
* 数组继承自 `Array.prototype`，它包含的方法集合比 `Object.prototype` 要好得多。
* 数组使用数组字面量而非对象字面量创建。数组字面量在语法上简单得多：用 `[` 和 `]` 包围零个或多个用 `,` 分隔的表达式。
* JSON 非常不同地对待数组和对象，尽管 JavaScript 在大多数情况下将它们视为相同。

JavaScript 本身对数组也感到困惑。当给定一个数组时，`typeof` 运算符返回字符串 `"object"`，这显然是错误的。你应该使用 `Array.isArray(value)` 函数来确定一个 `value` 是否是数组。

```
const what_is_it = new Array(1000);
typeof what_is_it                  // "object"
Array.isArray(what_is_it)          // true
```



### 起源

自计数发明以来，人们就开始用表示“一”的词语开始编号。20世纪60年代中期，一个虽小但有影响力的程序员群体确定我们应该从0开始编号。如今，几乎所有程序员都从0开始编号。而人类的其余部分，包括大多数数学家，仍然从1开始。数学家们通常将原点标记为0，但大多数人将有序集合的第一个成员标记为1。他们为何这样做至今仍是个谜。

从0开始编号有一个效率方面的论据，但这个论据如此薄弱，以至于毫无价值。同样，有一个正确性论据认为从0开始能减少差一错误，但这也值得怀疑。程序员们为何与其他人计数方式不同，似乎应该有一个好的理由。也许有一天我们会发现原因。

这一点在JavaScript中的影响体现在数组元素的编号上，其次在字符串字符的编号上也有体现。数组应逐个元素处理的思想至少可以追溯到FORTRAN。一个更现代的思想是函数式地处理数组。这通过消除显式的循环管理简化了代码，并创造了将工作分布到多个处理器的潜力。

在设计良好的语言中，编写良好的程序不应关心数组是从0还是从1开始。我不会指责JavaScript是设计良好的语言，但它相比FORTRAN确实有显著改进，事实上，通过脱离FORTRAN模型，我们通常不需要关心元素是如何编号的。

有时我们确实需要关心。单词 *first*（第一）因其与 *one*（一）的关联而变得有问题，因此我改用 *zeroth*（第零个）。这使我的原点变得清晰。

```
[0]    zeroth    0th
[1]    oneth     1st
[2]    twoth     2nd
[3]    threeth   3rd
```

以此类推，*fourth*（第四）、*fifth*（第五）和 *sixth*（第六）似乎有歧义，但当我们计数超过最小的整数后，原点应该就清楚了。

### 初始化

创建新数组有两种方式。

- 数组字面量
- new Array(*整数*)

```
let my_little_array = new Array(10).fill(0);
// my_little_array 是 [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
let same_thing = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0];

my_little_array === same_thing                     // false
```

注意 `my_little_array` 和 `same_thing` 是完全相同的。它们也是两个独立、唯一的值。与字符串不同，但与对象类似，相同的数组只有在实际上是同一个数组时才相等。

### 栈和队列

数组有可以作为栈操作的方法。`pop` 方法移除并返回数组的最后一个元素。`push` 方法向数组追加一个新元素。

栈在解释器和计算器中经常使用。

```
function make_binary_op(func) {
    return function (my_little_array) {
        let oneth = my_little_array.pop();
        let zeroth = my_little_array.pop();
        my_little_array.push(func(zeroth, oneth));
        return my_little_array;
    };
}

let addop = make_binary_op(function (zeroth, oneth) {
    return zeroth + oneth;
});

let mulop = make_binary_op(function (zeroth, oneth) {
    return zeroth * oneth;
});
```

```
let my_little_stack = [];           // my_little_stack 是 []
my_little_stack.push(3);             // my_little_stack 是 [3]
my_little_stack.push(5);             // my_little_stack 是 [3, 5]
my_little_stack.push(7);             // my_little_stack 是 [3, 5, 7]
mulop(my_little_stack);              // my_little_stack 是 [3, 35]
addop(my_little_stack);              // my_little_stack 是 [38]
let answer = my_little_stack.pop();  // my_little_stack 是 [], answer 是 38
```

`shift` 方法类似于 `pop` 方法，不同的是它移除并返回的是第零个元素，而不是最后一个。命名奇怪的 `unshift` 方法类似于 `push`，不同的是它将新元素添加到数组的开头，而不是末尾。`shift` 和 `unshift` 方法可能比 `pop` 和 `push` 慢得多，尤其是当数组很大时。结合使用 `shift` 和 `push` 构成了一个队列，你在末尾追加新项目，最终从开头取出它们。

### 搜索

JavaScript提供了搜索数组的方法。`indexOf` 方法接受一个值，从数组开头开始将其与每个元素进行比较。如果你的值匹配一个元素，它会停止搜索并返回该元素的序号。

如果未找到匹配项，它返回-1。注意这是一个潜在的类型错误，因为-1是一个数字，就像其他任何数字一样。如果你在使用 `indexOf` 的返回值前没有先显式检查-1，那么它参与的计算可能会在没有警告的情况下出错。JavaScript有许多底部值。其中任何一个都本应被使用。

**lastIndexOf** 函数类似于 **indexOf**，不同的是它从数组末尾开始向后搜索。它也使用-1作为失败代码。

**includes** 函数类似于 **indexOf**，不同的是如果找到值则返回 **true**，如果未找到则返回 **false**。

### 归约

**reduce** 方法将数组归约为单个值。它接受一个需要两个参数的函数。**reduce** 方法成对地调用该函数，一次又一次，直到只剩下一个作为结果的值。

设计 **reduce** 方法有两种方式。一种是为数组的每个元素调用该函数。必须提供一个初始值来启动。

```
function add(reduction, element) {
    return reduction + element;
}

let my_little_array = [3, 5, 7, 11];

let total = my_little_array.reduce(add, 0);           // total 是 26
```

对于每个元素，归约值与当前数组元素一起传递给 **add**。我们显式地传入了0，即初始归约值。add函数看到

```
(0, 3)                       // 3
(3, 5)                       // 8
(8, 7)                       // 15
(15, 11)                     // 26
```

**add** 返回的每个值成为下一次调用 **add** 的归约值。初始归约值并不总是0。如果我们向 **reduce** 传递一个乘法函数，那么初始归约值应该是1。如果我们向 **reduce** 传递 **Math.max**，初始归约值应该是-Infinity。这造成了一个风险：你需要谨慎选择初始归约值。

设计 **reduce** 的另一种方式是不要求初始归约值。相反，函数被调用的次数少一次。第一次调用时，它接收第零个和第一个元素。第零个元素成为初始归约值。

```
total = my_little_array.reduce(add);                 // 26
```

现在add函数看到

```
(3, 5)                       // 8
(8, 7)                       // 15
(15, 11)                     // 26
```

函数被调用的次数少了一次，并且不可能出现选择错误初始归约值的错误。JavaScript做的有点精妙的是，它的 **reduce** 方法两种方式都有效。如果你传入了初始归约值，那么函数会为每个元素调用。如果你没有传入初始归约值，那么你的函数不会为第零个元素调用。相反，第一个元素被用作初始归约值。所以上面两个 **reduce add** 的例子都有效。

reduceRight函数的工作方式相同，不同的是它从数组末尾开始。我希望它被命名为reduce_reverse。

我使用reduce来计算本书ISBN号的校验位。

```
function isbn_13_check_digit(isbn_12) {
    const string_of_digits = isbn_12.replace(/-/g, "");
    if (string_of_digits.length === 12) {
        const check = string_of_digits.split("").reduce(
            function (reduction, digit, digit_nr) {
                return reduction + (
                    digit_nr % 2 === 0
                    ? Number(digit)
                    : Number(digit) * 3
                );
            },
            0
        ) % 10;
        return (
            check > 0
            ? 10 - check
            : check
        );
    }
}
isbn_13_check_digit("978-1-94-981500")          // 9
```

### 迭代

数组上最常见的操作之一是对每个元素做一些事情。历史上这是用for语句完成的。JavaScript提供了一种更现代的方法。

forEach方法接受一个数组和一个函数。它为数组的每个元素调用该函数。该函数可以有三个参数：element、element_nr和array。element参数是数组的一个元素。element_nr参数是元素的序号，如果在计算中有另一个数组需要协调，这会很方便。array参数是个错误，不应该在那里。它鼓励修改正在处理的数组，这通常是件坏事。

不幸的是，没有一种方法可以按相反顺序处理数组（像reduceRight那样）。有一个reverse方法可以先调用，但reverse是一个破坏性方法，不能用于冻结的数组。

forEach方法忽略它调用的函数的返回值。通过关注返回值，可以制作出有趣的方法。

> every方法查看返回值。如果它是假值，every方法停止处理并返回false。如果它是真值，every方法继续处理。如果every方法到达数组末尾，它返回true。

some方法与every方法非常相似，以至于不清楚它为什么应该存在于语言中。如果函数的返回值是真值，some方法停止处理并返回true。如果是假值，some方法继续。如果some方法到达数组末尾，它返回false。



### 数组的工作原理

method 继续处理。如果 some 方法到达了数组末尾，则返回 false。

find 方法类似于 some 方法，不同之处在于它不是返回 true 或 false，而是返回函数返回真值时正在处理的元素。

findIndex 方法类似于 find 方法，不同之处在于它不是返回元素，而是返回函数返回真值时正在处理的元素的序数。

filter 方法也类似于 find 方法，不同之处在于它始终处理到末尾，并返回一个数组，收集函数返回真值的所有元素。因此 find 返回第一个匹配项，而 filter 方法返回所有匹配项。

map 方法类似于 forEach 方法，不同之处在于它收集所有返回值并将它们返回到一个新数组中。map 方法是通过创建一个新数组（对原数组进行精炼或增强）来进行转换的理想方式。

这些方法是处理数组的更好方式，无需诉诸 for 循环。但这组方法并不完整。

forEach 和 find 能够提前退出。（forEvery 的退出形式是 every 和 some。）map、reduce 和 filter 没有提前退出的选项。

reduce 方法有使用 reduceRight 反向工作的选项，但 forEach、map、filter 和 find 没有反向工作的选项。

这些遗漏被用作不废除 for 语句的理由。

### 排序

JavaScript 有一个 sort 方法。不幸的是，它存在一些问题。

它是原地排序，修改它排序的数组。这意味着无法对冻结数组进行排序，而且排序共享数组也不安全。

```javascript
let my_little_array = ["unicorns", "rainbows", "butterflies", "monsters"];
my_little_array.sort();
// my_little_array is ["butterflies", "monsters", "rainbows", "unicorns"]
```

它的默认比较函数希望将值按字符串排列，即使它们是数字。例如，

```javascript
let my_little_array = [11, 2, 23, 13, 3, 5, 17, 7, 29, 19];
my_little_array.sort();
// my_little_array is [11, 13, 17, 19, 2, 23, 29, 3, 5, 7]
```

这不仅效率极低，而且也是完全错误的。幸运的是，我们可以通过向 sort 传递一个比较函数来缓解这个问题。该函数接收两个元素。如果第一个元素应该排在前面，则预期返回一个负数；如果第二个元素应该排在前面，则返回一个正数；如果比较函数无法判断，则返回零。

这个比较函数可以正确地对数字数组进行排序（只要所有元素都是有限数字）：

```javascript
function compare(first, second) {
    return first - second;
}
```

如果你想比较非有限的数字（如 `NaN` 和 `Infinity`），那么你的比较函数就需要更努力地工作。

sort 函数的问题清单上的下一个是缺乏稳定性。如果相等（你的比较函数返回零）的元素保持其原始的相对顺序，则该排序是稳定的。JavaScript 不保证稳定性。在对字符串数组或数字数组进行排序时，这不是问题。但在对对象数组或数组的数组进行排序时，这可能是个问题。复杂的排序可能想按姓氏排序，当姓氏相同时，再按名字排序。一种做法是先按名字排序，然后再按姓氏排序。但这行不通，因为排序不稳定，名字排序添加的信息可能会丢失。

我们可以通过使用更复杂的比较函数来缓解这个问题。为了简化，我们创建一个工厂来生成比较函数。

```javascript
function refine(collection, path) {
    // Take an array or object and a path in the form of an array of strings,
    // and return the value at the end of the path.
    // If there is no value, return undefined.
    return path.reduce(
        function (refinement, element) {
            try {
                return refinement[element];
            } catch (ignore) {}
        },
        collection
    );
}

function by(...keys) {
    // This factory creates a comparison function to help in sorting
    // an array of objects or an array of arrays.
    // The arguments are one or more strings or integers that will identify
    // the properties or elements to compare.
    // If the first argument sees a tie, then try the second, and then the third...
    // Convert each key into an array of strings.
    const paths = keys.map(function (element) {
        return element.toString().split(".");
    });

    // Compare each pair of values until finding a mismatch.
    // If there is no mismatch then the two values are equal.
    return function compare(first, second) {
        let first_value;
        let second_value;
        if (paths.every(function (path) {
            first_value = refine(first, path);
            second_value = refine(second, path);
            return first_value === second_value;
        })) {
            return 0;
        }

        // If the two values are of the same type, then we can compare the two values.
        // If the types are not the same, then we need some policy to cope with the weirdness.
        // Our simple policy here is to compare the names of the types,
        // so boolean < number < string < undefined.
        // (It might be better to fail instead of sorting disagreeable types.)
        return (
            (
                typeof first_value === typeof second_value
                ? first_value < second_value
                : typeof first_value < typeof second_value
            )
            ? -1
            : 1
        );
    };
}
```

示例：

```javascript
let people = [
    {first: "Frank", last: "Farkel"},
    {first: "Fanny", last: "Farkel"},
    {first: "Sparkle", last: "Farkel"},
    {first: "Charcoal", last: "Farkel"},
    {first: "Mark", last: "Farkel"},
    {first: "Simon", last: "Farkel"},
    {first: "Gar", last: "Farkel"},
    {first: "Ferd", last: "Berfel"}
];

people.sort(by("last", "first"));

// [
//     {"first": "Ferd", "last": "Berfel"},
//     {"first": "Charcoal", "last": "Farkel"},
//     {"first": "Fanny", "last": "Farkel"},
//     {"first": "Frank", "last": "Farkel"},
//     {"first": "Gar", "last": "Farkel"},
//     {"first": "Mark", "last": "Farkel"},
//     {"first": "Simon", "last": "Farkel"},
//     {"first": "Sparkle", "last": "Farkel"}
// ]
```

### 大杂烩

**concat** 方法接收两个或更多数组，并将它们连接在一起形成一个新数组。

```javascript
let part_zero = ["unicorns", "rainbows"];
let part_one = ["butterflies", "monsters"];
let whole = part_zero.concat(part_one);
// whole is ["unicorns", "rainbows", "butterflies", "monsters"]
```

**join** 方法接收一个字符串数组和一个分隔符字符串。它生成一个组合所有内容的大字符串。如果你不需要分隔，使用空字符串作为分隔符。这是字符串 **split** 方法的逆操作。

```javascript
let string = whole.join(" & ");
// string is "unicorns & rainbows & butterflies & monsters"
```

**reverse** 方法将数组中的元素重新排列，使它们处于相反的顺序。这是破坏性的，与 **sort** 函数类似。

```javascript
whole.reverse();
// whole is ["monsters", "butterflies", "rainbows", "unicorns"]
```

**slice** 方法可以复制一个数组，或复制数组的一部分。第零个参数决定从哪个序数开始。第一个参数是第零个参数加上要复制的元素数量。如果省略第一个参数，则复制所有剩余元素。

```javascript
let element_nr = whole.indexOf("butterflies");
let good_parts;
if (element_nr !== -1) {
    good_parts = whole.slice(element_nr);
}
// good_parts is ["butterflies", "rainbows", "unicorns"]
```

### 7.9 数组的工作原理

### 纯与不纯

有些数组方法是纯的，不改变它们的输入。有些不是。有些本应是纯的，但不是。有些本质上不可能是纯的，但仍然有价值。

在处理纯/不纯二元性时，重要的是要知道什么是纯的，什么不是。

#### 纯方法：

- concat
- every
- filter
- find
- findIndex
- forEach
- indexOf
- join
- lastIndexOf
- map
- reduce
- reduceRight
- slice
- some

#### 不纯方法：

- fill
- pop
- push
- shift
- splice
- unshift

#### 本应是纯的但不纯的方法：

- reverse
- sort



# 第 8 章

## 对象的工作原理

> 为你丢弃的东西心怀感激。通过表达感激，你为与该物品的关系画上了句号，而这样做，会让你更容易放手。

*玛丽·康多*

JavaScript 重载了 *object* 这个词。这门语言中，一切（除了两个底层值 `null` 和 `undefined`）都是对象。但通常，尤其是在本章中，*object* 指的是更具体的东西。

JavaScript 的主要数据结构被称为 *object*。对象是属性（或成员）的容器。每个属性都有一个名称和一个值。名称是字符串。值可以是任何类型。在其他语言中，这种类型的对象可能被称为哈希表、映射、记录、结构体、关联数组、字典，或者在一些非常不客气的语言中，称为 dict。

一个新对象可以通过对象字面量来创建。对象字面量创建的值可以存储在变量或对象或数组中，可以传递给函数，或者从函数返回。

对象字面量由 `{` *左花括号* 和 `}` *右花括号* 定界。内部可以包含零个或多个属性，用 `,` *逗号* 分隔。一个属性可以是：

-   一个字符串，后跟 `:` *冒号*，再跟一个表达式。属性的名称是该字符串。属性的值是表达式的值。
-   一个名称，后跟 `:` *冒号*，再跟一个表达式。属性的名称是转换为字符串的该名称。属性的值是表达式的值。
-   一个名称。属性的名称是转换为字符串的该名称。属性的值是同名变量或参数的值。
-   一个名称，后跟一个用 `(` *左圆括号* 和 `)` *右圆括号* 包裹的参数列表，再跟一个用 `{` *左花括号* 和 `}` *right brace* 包裹的函数体。这是“名称后跟冒号再跟函数表达式”的简写形式。这允许省略 `: function`，尽管考虑到清晰度的损失，这似乎不太值得。

### 8.1 对象的工作原理

例如：

```
let bar = "a long rod or rigid piece of wood or metal";
let my_little_object = {
    "0/0": 0,
    foo: bar,
    bar,
    my_little_method() {
        return "So small.";
    }
};
```

我们可以通过点表示法使用名称来访问对象的属性。

```
my_little_object.foo === my_little_object.bar                // true
```

我们也可以使用方括号表示法来访问对象的属性。我们可以使用方括号表示法来访问名称不是有效标识符的属性。我们还可以使用方括号表示法来访问计算属性名。方括号中的表达式会被求值，并在必要时转换为字符串。

```
my_little_object["0/0"] === 0                             // true
```

如果我们使用点或方括号请求一个在对象中找不到的名称，那么将提供底层值 `undefined` 代替。请求一个不存在或缺失的属性不被视为错误。这是一个产生 `undefined` 的正常操作。

```
my_little_object.rainbow                                   // undefined
my_little_object[0]                                        // undefined
```

可以通过赋值向对象添加新属性。现有属性的值也可以通过赋值进行替换。

```
my_little_object.age = 39;
my_little_object.foo = "slightly frilly or fancy";
```

我建议不要将 `undefined` 存储在对象中。JavaScript 允许这样做，并且会正确地返回 `undefined` 值，但这与表示属性缺失的 `undefined` 是同一个。这是一个容易避免的混乱来源。我希望存储 `undefined` 会导致属性被移除，但它不会。属性可以通过 `delete` 操作符来移除。

```
delete my_little_object["0/0"];
```

可以通过对象构建复杂的数据结构，因为对象的引用可以存储在对象中。可以构造各种图和循环结构。嵌套深度没有限制，但不要走火入魔。

当 `typeof` 操作符用于对象时，它返回字符串 `"object"`。

```
typeof my_little_object === "object"                        // true
```

### 大小写

键的匹配区分大小写。因此 `my_little_object.cat` 与 `my_little_object.Cat` 或 `my_little_object.CAT` 不是同一个属性。`===` 操作符决定了属性名的字符串匹配。

### 复制

`Object.assign` 函数可以将属性从一个对象复制到另一个对象。你可以通过将属性赋值给一个空对象来制作对象的副本。

```
let my_copy = Object.assign({}, my_little_object);
my_copy.bar            // "a long rod or rigid piece of wood or metal"
my_copy.age                                // 39
my_copy.age += 1;
my_copy.age                                // 40
delete my_copy.age;
my_copy.age                                // undefined
```

一个对象可以从多个对象那里接收材料。通过这种方式，可以通过组装来自更简单对象的材料来构造一个复杂的对象。

### 继承

在 JavaScript 中，可以创建一个从另一个对象继承的对象。这种继承风格与那些具有紧密耦合的程序结构（如类）的语言中实践的继承非常不同。在 JavaScript 中，是数据被耦合，这可以显著减少可能侵袭应用程序架构的脆弱性。

`Object.create(prototype)` 接受一个现有对象并返回一个继承自该现有对象的新对象。现有对象是新对象的原型。任何对象都可以成为新对象的原型。从原型继承的对象也可以成为更新对象的原型。原型链的长度没有限制，但明智的做法是保持其较短。

如果尝试访问一个缺失的属性，在返回 `undefined` 之前，系统会首先查找原型，然后是原型的原型，依此类推。如果在原型链中找到了同名属性，则会像在目标对象中找到该属性一样返回它。

当向对象赋值时，只有最顶层的对象会被更改。原型链上的对象不会被更改。

```
let my_clone = Object.create(my_little_object);
my_clone.bar           // "a long rod or rigid piece of wood or metal"
my_clone.age                                // 39
my_clone.age += 1;
my_clone.age                                // 40
delete my_clone.age;
my_clone.age                                // 39
```

原型最常见的用途是作为存储函数的地方。JavaScript 自身就是这样做的。当通过对象字面量创建对象时，该对象继承自 `Object.prototype`。同样，数组从 `Array.prototype` 继承方法。数字从 `Number.prototype` 继承方法。字符串从 `String.prototype` 继承方法。甚至函数也从 `Function.prototype` 继承方法。数组和字符串方法非常有用，但 `Object.prototype` 中的方法大多无用。

由于我们有继承，我们现在有两种类型的属性：存在于最顶层对象的自有属性，以及存在于原型链中的继承属性。在大多数情况下，它们的工作方式完全相同。有时你需要知道该属性是否确实是对象自己的。大多数对象都继承了一个 `hasOwnProperty(string)` 函数，但不幸的是，它存在可靠性风险。它接受一个字符串，如果对象包含一个具有该名称的属性*并且*该属性不是继承的，则返回 `true`。不幸的是，如果对象有一个名为 `hasOwnProperty` 的属性，它将被调用，而不是 `Object.prototype.hasOwnProperty` 方法。这可能导致错误或其他混乱。如果 `hasOwnProperty` 是一个操作符，从而使得对象的状态无法导致对 `hasOwnProperty` 的调用失败，那本会更好。如果根本没有继承属性，从而使这个麻烦的方法变得不必要，那就更好了。

```
my_little_object.hasOwnProperty("bar")         // true
my_copy.hasOwnProperty("bar")               // true
my_clone.hasOwnProperty("bar")              // false
my_clone.hasOwnProperty = 7;
my_clone.hasOwnProperty("bar coin hasOwnProperty")
```

如果你有一个名为 `hasOwnProperty` 的属性，那么你就不能使用继承的 `hasOwnProperty` 方法。你将调用的是自有属性。

`Object.prototype.toString` 共享相同的失败风险。但即使它能工作，也令人失望。

```
my_clone.toString                          // "[object Object]"
```

不需要别人告诉你你的对象是一个对象。你可能已经知道了。你想要的是它包含的内容的展示。如果你想将对象转换为字符串，`JSON.stringify` 做得更好。

`Object.create(prototype)` 相对于 `Object.assign(Object.create({}), prototype)` 的优势在于使用更少的内存。在大多数情况下，节省并不显著。原型在没有增加太多好处的情况下增加了怪异性。

还有一个无意继承的问题。你可能想将对象用作哈希表，但对象会继承诸如 `"toString"`、`"constructor"` 以及其他可能是实现相关的名字。这些可能会与潜在期望的属性混淆。

幸运的是，`Object.create(null)` 创建了一个不继承任何东西的对象。在继承属性或无意继承方面没有混淆。对象中除了你明确放入的内容外，什么都没有。我现在经常使用 `Object.create(null)`。

### 键

`Object.keys(object)` 函数可以获取对象中所有自有（但非继承）属性的名称，并将它们作为字符串数组返回。这使你可以使用数组方法来处理对象的属性。

数组中的字符串将按照它们被插入的顺序排列。如果你需要不同的顺序，可以使用数组的 `sort` 方法。



### 对象的工作方式

#### 8.4 冻结

`Object.freeze(object)` 可以接收一个对象并将其冻结，使其不可变。不可变性可以带来更可靠的系统。一旦对象按照你的意愿构建完成，就可以将其冻结，这保证了它不会被损坏或篡改。这不是深度冻结。只有顶层对象会被冻结。

不可变对象将来可能具有宝贵的性能特性。如果已知一个对象永远不会改变，那么语言实现就可以利用一组强大的优化。

不可变对象具有出色的安全属性。这一点很重要，因为当前的行业实践鼓励将不可信的代码安装到我们的系统中。不可变性可能有朝一日能让这种做法变得安全。通过不可变性，我们可以赋予对象良好的接口来自我防御。

`Object.freeze(object)` 和 `const` 语句做的是两件非常不同的事情。`Object.freeze` 操作的是值。`const` 操作的是变量。如果你将一个可变对象放入一个 `const` 变量中，你仍然可以改变该对象，但你不能用不同的值替换该对象。如果你将一个不可变对象放入一个普通变量中，你不能改变该对象，但你可以为该变量赋予不同的值。

```
Object.freeze(my_copy);
const my_little_constant = my_little_object;

my_little_constant.foo = 7;                  // 允许
my_little_constant = 7;                       // 语法错误！
my_copy.foo = 7;                              // 异常！
my_copy = 7;                                  // 允许
```

#### 原型与冻结不能混用

原型的一个用途是创建对象的轻量级副本。我们可能有一个充满数据的对象。我们希望得到另一个相同但其中一个属性被更改的对象。我们可以像之前看到的那样使用 `Object.create` 来做到这一点。这将在创建新对象时节省一些时间，但由于需要遍历原型链，属性的检索可能成本会稍高一些。

不幸的是，如果原型被冻结，这种方法就行不通了。如果原型中的某个属性是不可变的，那么实例就不能拥有该属性的自己的版本。在某些函数式编程风格中，我们希望所有对象都被冻结，以获得不可变性带来的可靠性益处。因此，我们本可以做一个继承自冻结原型的实例，更新该实例，然后冻结该实例，而不是通过复制来实现变更。但这根本行不通。更新实例会引发异常。它也会普遍减慢新属性的插入速度。每当插入一个新属性时，都必须在整个原型链中搜索该键，以确定祖先中是否存在不可变属性。通过使用 `Object.create(null)` 来创建对象，可以避免这种搜索。

## WeakMap

JavaScript 的设计错误之一是对象的属性名必须是字符串。在有些情况下，你想使用对象或数组作为键。不幸的是，JavaScript 对象在这种情况下做错了事情，它使用 `toString` 方法将键对象转换为键字符串，我们已经知道这很令人失望。

JavaScript 没有给我们一个对所有键都能正确工作的对象，而是给了我们第二种类型的对象，称为 WeakMap，它允许对象作为键（但不允许字符串），并且具有完全不同的接口。

| Object | WeakMap |
|--------|---------|
| `object = Object.create(null);` | `weakmap = new WeakMap();` |
| `object[key]` | `weakmap.get(key)` |
| `object[key] = value;` | `weakmap.set(key, value);` |
| `delete object[key];` | `weakmap.delete(key);` |

这两样做同样事情的东西在语法上如此不同，这没有道理。这两样东西不是一样东西，这也没有道理。本来应该有一个单一的东西允许字符串和对象作为键，而不是一个只允许字符串作为键的东西和另一个只允许对象作为键的东西。

尽管如此，WeakMap 是非常出色的。以下是两个使用示例。

我们想给一个对象添加一个秘密属性。为了访问这个秘密属性，你需要访问该对象和秘密密钥。除非你两者都有，否则无法访问该属性。我们可以用 WeakMap 来实现。我们将 WeakMap 视为秘密密钥。

```
const secret_key = new WeakMap();
secret_key.set(object, secret);

secret = secret_key.get(object);
```

你必须同时访问对象和秘密密钥才能恢复秘密。这种技术的一个好处是，我们可以有效地给冻结的对象添加秘密属性。

我们希望能够将一个对象交给一些可能为我们做有用事情的代码，比如编目它或存储它以便以后检索，但我们不想也赋予该代码改变该对象或调用其任何方法的能力。在现实世界中，我们想让代客泊车的人停好车，但不想让他们清空手套箱和后备箱或卖掉汽车。荣誉制度在现实世界中对人有效，但在计算机网络中的代码中无效。

因此，我们制作了一个称为密封器（sealer）的装置。我们给密封器一个对象，它返回一个无法打开的盒子。这个盒子可以交给代客泊车的人。要恢复原始对象，将盒子交给匹配的解封器（unsealer）。我们可以使用 WeakMap 轻松制作这些函数。

```
function sealer_factory() {
    const weakmap = new WeakMap();
    return {
        sealer(object) {
            const box = Object.freeze(Object.create(null));
            weakmap.set(box, object);
            return box;
        },
        unsealer(box) {
            return weakmap.get(box);
        }
    };
}
```

WeakMap 不允许检查其内容。除非你同时持有密钥，否则无法从中获取值。WeakMap 与 JavaScript 的垃圾回收器配合良好。如果没有键的副本仍然存在，那么该键在 WeakMap 中的属性就会自动删除。这有助于避免内存泄漏。

JavaScript 还有一个类似的东西叫做 Map，但 Map 没有 WeakMap 所具备的安全性和内存泄漏保护。而且，尽管 WeakMap 是一个糟糕的名字，Map 更令人困惑。它与数组的 `map` 方法毫无关系，并且可能被误认为是制图函数。这就是我不推荐 Map 的原因。但我喜欢 WeakMap 和数组的 `map` 函数。

JavaScript 有一个叫做 Symbol 的东西，它可以做 WeakMap 能做的其中一件事。我不推荐 Symbol，因为它是不必要的。我的目标是通过消除我不需要的多余功能来简化。

# 第 9 章

## 字符串的工作方式

> 不公平！不公平！这不公平，我的宝贝，是不是，问我们它那肮脏的小口袋里装了什么？
> *咕噜*

计算机擅长操纵位模式。人类则不擅长。字符串弥合了计算机与人类之间的差距。字符到整数的映射是数字计算机发展中的一个重要进步。这是用户界面开发中的第一个重要进展。

我们不知道为什么将这种类型称为*字符串*。为什么我们不称它为*文本*呢？没人知道。JavaScript 字符串看起来并不像一根绳子。我们可以谈论*一串字符*，但我们同样可以谈论*一串语句*，或者*一串比特*，甚至*一连串的失败*。在现实世界中，我们不连接字符串。我们系字符串。

### 基础

字符串是一个不可变的 16 位无符号整数数组，范围从 0 到 **65535**。字符串可以通过 `String.fromCharCode` 函数创建，该函数接受任意数量的数字。字符串的元素可以通过 `charCodeAt` 访问。元素不能被更改，因为字符串总是冻结的。字符串和数组一样，有一个 `length` 属性。

```
const my_little_array = [99, 111, 114, 110];
const my_little_string = String.fromCharCode(...my_little_array);
my_little_string.charCodeAt(0) === 99          // true
my_little_string.length                         // 4
typeof my_little_string                         // "string"
```

括号表示法可用于从字符串中获取单个值，但它不像数组那样返回一个数字。相反，它返回一个长度为 1 的新字符串，其内容就是该数字。

```
my_little_string[0] === my_little_array[0]     // false
my_little_string[0] === String.fromCharCode(99) // true
```

`String.prototype` 包含作用于字符串的方法。`concat` 和 `slice` 方法的工作方式与数组方法非常相似。但 `indexOf` 方法的工作方式非常...



 ## 字符串的工作原理

...


等等，让我重新整理：

[content]
 ## 字符串的工作原理

方式不同。`indexOf`的参数是一个字符串，而不是数字。它尝试将参数中的所有元素按顺序与第一个字符串中的元素进行匹配。

```
my_little_string.indexOf(String.fromCharCode(111, 114)) // 1
my_little_string.indexOf(String.fromCharCode(111, 110)) // -1
```

`startsWith`、`endsWith`和`includes`方法只是对`indexOf`和`lastIndexOf`的包装。

`===`运算符认为包含相似内容的字符串是相等的。相似的数组只有在它们是同一个数组时才是相等的。

```
my_little_array === my_little_array // true
my_little_array === [99, 111, 114, 110] // false
my_little_string === String.fromCharCode(99, 111, 114, 110) // true
```

字符串的相等性是一个非常强大的特性。它消除了对符号类型的需求，因为相似的字符串被认为是同一个对象。这在像Java这样的低级语言中是不成立的。

### Unicode

JavaScript允许所有65536种16位模式作为字符串的元素。然而，通常的做法是将每个元素视为一个字符，而Unicode标准决定了字符的编码。JavaScript对Unicode有大量的语法和方法支持。 Unicode标准声明某些代码不是字符，不应使用。JavaScript并不在意。它允许所有16位代码。如果你打算让你的系统与用低级语言编写的系统交互，那么你不应该滥用Unicode。

字符串字面量是通过用*"双引号"*包围零个或多个Unicode字符来书写的。（*'单引号'*也可以使用，但不推荐使用，因为它是不必要的。）每个字符都表示为一个16位元素。

*+加号*运算符用于进行连接。我们已经看到*+*也用于加法。如果你想进行连接，那么你需要确保至少有一个操作数是字符串。一种方法是将其中一个操作数设为字符串字面量。另一种方法是将一个值传递给`String`函数。

```
my_little_string === "corn" // true
"uni" + my_little_string // "unicorn"
3 + 4 // 7
String(3) + 4 // 34
3 + String(4) // 34
```

字符串字面量必须完全位于一行内。*\反斜杠*用作转义字符，允许在字符串字面量中包含*"双引号"*、*\反斜杠*和换行。

方括号可用于从字符串中检索字符。字符的表示是一个`length`为1的字符串。没有字符类型。字符可以表示为数字或字符串。

许多语言确实有字符类型，通常缩写为`char`，但似乎没有一个标准的发音。我听人把它读作*car*、*care*、*chair*、*char*和*share*。

所有字符串在创建时就被冻结了。一旦创建，字符串就不能被更改。可以从字符串中复制较小的片段。每个片段都是一个新的字符串。可以通过将字符串连接在一起来创建新字符串。

```
const mess = "monster";
const the_four = "uni" + my_little_string + " rainbow butterfly " + mess;
// the_four is "unicorn rainbow butterfly monster"
```

```
const first = the_four.slice(0, 7);        // first is "unicorn"
const last = the_four.slice(-7);          // last is "monster"
const parts = the_four.split(" ");        // parts is [
                                         //   "unicorn",
                                         //   "rainbow",
                                         //   "butterfly",
                                         //   "monster"
                                         // ]
```

```
parts[2][0] === "b"                     // true
"*".repeat(5)                          // "*****"
parts[1].padStart(10, "/")              // "///rainbow"
```

### 更多关于Unicode

Unicode最初的目标是用16位表示世界上所有现存的语言。其章程后来改为用21位表示世界上所有的语言。不幸的是，JavaScript是在Unicode的16位阶段设计的。

Unicode将JavaScript的*字符*拆分为两个新术语：*代码单元*和*码点*。代码单元是那些16位字符之一。码点是与字符对应的数字。码点由1个或多个代码单元组成。

Unicode定义了1,114,112个码点，分为17个平面，每个平面65,536个码点。原始平面现在称为基本多文种平面（BMP）。其余16个平面是辅助平面。JavaScript可以轻松使用BMP中的字符，因为那里一个码点可以用一个代码单元来标识。辅助字符则更为困难。

JavaScript通过使用代理对来访问辅助字符。代理对由两个特殊的代码单元组成。有1024个高代理代码单元和1024个低代理代码单元。高代理代码单元的代码低于低代理代码单元。

| 范围 | 描述 |
|-------|-------------|
| 0xD800 至 0xDBFF | 高代理代码单元 |
| 0xDC00 至 0xDFFF | 低代理代码单元 |

当正确配对时，每个代理代码单元贡献10位以形成20位的偏移量，加上65,536形成码点。（这种加法是为了消除因有两个不同的代码单元序列可能产生相同的码点而造成的混淆。我认为这种解决方案造成的混淆比它避免的更多。更简单的解决方案应该是禁止使用代理对来表示BMP中的码点。这样将会得到一个20位字符集，而不是21位字符集。）

考虑码点U+1F4A9（或十进制的128169）。我们减去65,536，得到62,633或0xF4A9。高10位是0x03D。低10位是0x0A9。我们将0xD800加到高位，0xDC00加到低位的，就得到了一个代理对。所以

### 字符串的工作原理

JavaScript将U+1F4A9存储为U+D83D U+DCA9。从JavaScript的角度来看，U+1F4A9是两个16位字符。如果操作系统有能力，它将显示为单个字符。JavaScript对辅助平面基本不知情，但它并不公开敌视它们。

在字符串字面量中，有两种使用转义来书写码点U+1F4A9的方式。

```
"\uD83D\uDCA9" === "\u{1F4A9}"                                                         // true
```

它们都产生长度为2的相同字符串。

有一个String.fromCodePoint函数可以生成代理对。

```
String.fromCharCode(55357, 56489) === String.fromCodePoint(128169)  // true
```

codePointAt方法与charCodeAt类似，不同之处在于它还可以查看下一个字符，如果它们形成代理对，则返回辅助码点。

```
"\uD83D\uDCA9".codePointAt(0)                                                               // 128169
```

人们在全球通信中需要的大多数字符都可以在BMP中找到，所以代理对内容通常不需要。即便如此，辅助字符随时可能出现，所以你的程序应该准备好应对它们。

Unicode包含组合字符和修饰字符，它们为字母添加重音符号和其他修饰。它还包含控制书写方向和其他功能的字符。有时这些可能会变得复杂，以至于两个看起来包含相同字符的字符串可能并不相等。Unicode有规范化规则，规定了事物必须出现的顺序，以及何时将带修饰符的基本字符替换为组合字符。人类不受这些规则的约束，所以你可能不得不处理非规范化材料。JavaScript将这些规范化规则包装在normalize方法中。

```
const combining_diaeresis = "\u0308";
const u_diaeresis = "u" + combining_diaeresis;
const umlaut_u = "\u00FC";

u_diaeresis === umlaut_u                                                                      // false
u_diaeresis.normalize() === umlaut_u.normalize()                                             // true
```

Unicode包含许多重复字符和相似字符，所以即使经过规范化，仍然可能存在看起来相同但并不相等的字符串。这是混淆的来源，也是一个安全隐患。

### 模板字符串字面量

模板化是Web应用开发中非常流行的做法。由于Web浏览器的DOM API如此功能缺陷且容易出错，主流做法是使用模板化来构建HTML视图。虽然这比与DOM搏斗要容易得多，但它也是XSS和其他Web安全故障的原因。JavaScript的模板字符串字面量旨在为模板化提供支持，同时缓解安全问题，有时部分成功了。

模板字符串字面量是可以跨越多行的字符串字面量。`反引号`（也称为backtick）用作分隔符。



字符串的工作原理

9.4

```
const old_form = (
    "Can you"
    + "\nbelieve how"
    + "\nincredibly"
    + "\nlong this"
    + "\nstring literal"
    + "\nis?"
);
```

```
const new_form = `Can you
believe how
incredibly
long this
string literal
is?`;
```

```
old_form === new_form                 // true
```

新形式相比旧形式有显著优势吗？它有一个微小的表示法优势，但代价是：语言中最大的语法结构被键盘上最轻的光学字符所界定。出错的可能性很大。此外，还增加了视觉上的模糊性。incredibly 后面有空格吗？使用旧形式，答案显然是没有。

在大多数情况下，长篇文本材料不应存储在程序中。它应该用适当的工具维护，如文本编辑器、JSON 编辑器或数据库工具，然后作为资源包被程序访问。新语法正在助长一种不良做法。

使用字符串来记录人类语言是非常普遍的。此类文本通常需要翻译以服务全球受众。我们不想为每种语言维护每个程序文件的单独版本。我们希望每个程序文件有一个可以接收本地化文本的单一版本。新形式使这变得更加困难，因为它限制了为程序提供模板字符串的方式。

新语法的好处是它提供了插值。可以在模板字符串字面量内 `${ 左花括号 } 右花括号` 中放置有效的表达式。这些表达式会被求值、转换成字符串并插入。

```
let fear = "monsters";

const old_way = "The only thing we have to fear is " + fear + ".";

const new_way = `The only thing we have to fear is ${fear}.`;

old_way === new_way                   // true
```

两种方式的危险在于，内容可能是恶意的，比如 fear = "<script src=https://themostevilserverintheworld.com/malware.js>";

```
fear = "<script src=https://themostevilserverintheworld.com/malware.js>";
```

网络为启用恶意材料提供了很多机会。模板化似乎增加了漏洞。大多数模板化工具提供了缓解危险的机制，但仍然允许漏洞利用发生。而最糟糕的，比如带有插值的模板字符串字面量，默认情况下是不安全的。

在这种情况下，缓解措施是一种特殊类型的函数，称为*标签*函数。在模板字符串字面量前加上一个函数表达式，会导致该函数被调用，并接收模板字符串和表达式的值作为其参数。其思想是标签函数接收到所有片段，然后进行适当的过滤、编码、组装并返回。

`dump` 函数是一个标签函数，它只是以人类可读的形式返回所有输入材料。

```
function dump(strings, ...values) {
    return JSON.stringify({
        strings,
        values
    }, undefined, 4);
}

const what = "ram";
const where = "rama lama ding dong";

`Who put the ${what} in the ${where}?`
    // "Who put the ram in the rama lama ding dong?"

const result = dump`Who put the ${what} in the ${where}?`;
    // 结果是 `{
    //     "strings": [
    //         "Who put the ",
    //         " in the ",
    //         "?"
    //     ],
    //     "values": [
    //         "ram",
    //         "rama lama ding dong"
    //     ]
    // }`
```

奇怪的是，字符串作为一个数组一起传递，而值作为单独的参数传递。如果构造得当，并且实际使用了标签函数，它们可以缓解 XSS 和其他安全风险。但再次强调，它默认情况下是不安全的。

模板字符串字面量为语言增添了许多新语法、机制和复杂性。它们鼓励不良做法，但在提供大型字符串字面量方面确实提供了一些好处。

### 正则表达式

以下字符串方法可以接受正则表达式对象作为参数：`match`、`replace`、`search`、`split`。正则表达式对象也可以包含它们自己的方法：`exec`、`test`。

正则表达式对象对字符串执行模式匹配。正则表达式令人困惑地简洁，但表达力强大。尽管强大，但有很多事情它们无法做到。例如，正则表达式对象不足以解析 JSON 文本。这是因为 JSON 解析需要某种下推存储来处理嵌套结构。正则表达式对象没有下推存储。正则表达式对象能够将 JSON 文本分解成标记，这可能会大大简化制作 JSON 解析器的任务。

### 标记化

编译器在编译过程中会将源程序标记化。还有其他程序也依赖于标记化，包括编辑器、代码装饰器、静态分析器、宏处理器和压缩器。高度交互式的程序，如编辑器，需要快速标记化。不幸的是，JavaScript 是一种非常难以标记化的语言。

这是由于正则表达式字面量和自动分号插入之间的交互造成的。这会导致歧义，使程序难以解释。例如，

```
return /a/i;
return b.return /a/i;
```

这表明，通常不可能在不进行完整解析的情况下正确标记化 JavaScript 程序。

使用模板字符串字面量时情况会变得更糟。表达式可以嵌入在字面量中。另一个模板字符串字面量可以嵌套在该表达式中。这可以深入到任意深度。表达式还可以包含正则表达式字面量和包含反引号的字符串。确定一个反引号是关闭当前字面量还是打开一个嵌套字面量可能非常困难。确定某个东西的结构是什么可能非常困难。

```
`${`${"\"}"}`}`
```

情况甚至更糟。这些表达式还可以包含函数，而这些函数可能包含正则表达式字面量、缺失的分号以及更多的模板字符串字面量。

像编辑器这样的工具会假设程序行为良好。存在一个 JavaScript 子集，可以在不进行完整解析的情况下进行标记化。如果你在这方面使用过度，你应该预料到你的工具会失败。

我希望下一门语言能够轻松地进行标记化。同时，我建议不要在模板字符串字面量中使用插值。

### Fulfill

让我们考虑模板字符串插值的一种替代方案：一个名为 `fulfill` 的函数。它接受一个可能包含符号变量的字符串，以及一个包含应替换符号变量的值的对象或数组。它还可以接受一个函数或一个函数对象来编码替换值。

模板字符串的一个潜在问题是，所有在作用域内的内容都可以被包含进来。这非常方便，但也是一个安全隐患。`fulfill` 函数只能访问你明确传递给它的值容器，因此更安全。默认编码器会移除在某些上下文中已知危险的字符，因此在 HTML 上下文中，它默认是安全的，不像模板字符串默认不安全。但像模板字符串插值一样，如果你误用编码器，它也可能是不安全的。

字符串可以来自任何来源，例如 JSON 负载或字符串字面量。它不需要与 JavaScript 文件放在一起。这更适合本地化应用程序的需求。

符号变量被包裹在 { *左花括号* } *右花括号* 中。它不能包含任何空格或花括号。它可以包含一个路径，以及可选地一个冒号后跟编码名称。路径是一个或多个名称或数字，用 . *句点* 分隔。

`{a.very.long.path:hexify}`

容器是一个对象或数组，用于保存将替换符号变量的值。它可以包含嵌套的对象和数组。值将通过路径找到。如果替换值是一个函数，它会被调用，其返回值就是替换值。容器本身可以是一个函数。它会被调用，传递路径和编码以获取替换值。

然后替换值可以通过编码器进行转换。这主要是为了缓解模板化带来的安全问题，但也可以有其他用途。

可选的编码器参数可以是一个包含编码器函数的对象。符号变量的编码部分选择其中一个编码器。如果编码器对象没有匹配的函数，则原始符号变量不会被替换。编码器参数也可以是一个编码器函数，它会被所有符号变量调用。编码器函数接收替换候选值、路径和编码。如果它不返回字符串或数字，则原始符号变量不会被替换。

如果符号变量未指定编码，则假定使用 `""` 编码。

路径包含一个数字，对应于 `values` 数组中的一个元素，或 `values` 对象中的一个属性名。路径可以包含句点，以便可以找到嵌套对象和数组中的属性。

符号变量只有在格式正确、有替换值、且编码指定并正确实现的情况下才会被替换。如果任何地方出错，则符号变量将保持原样。可以在字符串中放置字面量花括号而无需转义。如果它们不是符号变量的一部分，则会原样保留。

```
const example = fulfill(
    "{greeting}, {my.place:upper}! :{",
    {
        greeting: "Hello",
        my: {
            fabulous: "Unicorn",
            insect: "Butterfly",
            place: "World"
        },
        phenomenon: "Rainbow"
    },
    {
        upper: function upper(string) {
            return string.toUpperCase();
        },
        "": function identity(string) {
            return string;
        }
    }
);
// {greeting}, {my.place:upper}! :{"greeting":"Hello","my":{"fabulous":"Unicorn","insect":"Butterfly","place":"World"},"phenomenon":"Rainbow"}
```



### 字符串的工作原理

```javascript
"大型浮点数的工作原理",
"大型有理数的工作原理",
"布尔值的工作原理",
"数组的工作原理",
"对象的工作原理",
"字符串的工作原理",
"底部值的工作原理",
"语句的工作原理",
"函数的工作原理",
"生成器的工作原理",
"异常的工作原理",
"程序的工作原理",
"this 的工作原理",
"无类编程的工作原理",
"尾调用的工作原理",
"纯函数的工作原理",
"事件驱动编程的工作原理",
"日期的工作原理",
"JSON 的工作原理",
"测试的工作原理",
"优化的工作原理",
"转译的工作原理",
"词法分析的工作原理",
"语法分析的工作原理",
"代码生成的工作原理",
"运行时的工作原理",
"Wat! 的工作原理",
"本书的工作原理"
];
const chapter_list = "<div>[</div>{chapters}<div>]</div>";
const chapter_list_item = `{comma}
<a href="#{index}">{"number": {index}, "chapter": "{chapter}"}</a>`;

fulfill(
    chapter_list,
    {
        chapters: chapter_names.map(function (chapter, chapter_nr) {
            return fulfill(
                chapter_list_item,
                {
                    chapter,
                    index: chapter_nr,
                    comma: (chapter_nr > 0)
                        ? ","
                        : ""
                }
            )
        }).join("");
    },
    entityify
)
```

// 参见本书前面的章节目录列表

`fulfill` 函数本身并不庞大。

```javascript
const rx_delete_default = /[\d+\s<>&%"\\ ]/g;
const rx_syntactic_variable = /
    \{
[^ { } : \s ]+
)
(?:
  :
  (
    [^ { } : \s ]+
  )
)?
\}
/g;
```

```javascript
// 捕获组：
//     [0] 原始值（包裹在花括号中的符号变量）
//     [1] 路径
//     [2] 编码
```

```javascript
function default_encoder(replacement) {
    return String(replacement).replace(rx_delete_default, "");
}
```

```javascript
export default Object.freeze(function fulfill(
    string,
    container,
    encoder = default_encoder
) {
```

`fulfill` 函数接收一个包含符号变量的字符串、一个生成器函数或一个包含用于替换符号变量的值的对象或数组，以及一个可选的编码器函数或编码器函数对象。默认编码器会移除所有尖括号。

大部分工作由字符串的 `replace` 方法完成，该方法查找符号变量，并将它们呈现为原始子字符串、一个路径字符串和一个可选的编码字符串。

```javascript
    return string.replace(
        rx_syntactic_variable,
        function (original, path, encoding = "") {
            try {
```

使用路径从值容器中获取单个替换值。路径包含一个或多个由句点分隔的名称（或数字）。

```javascript
        let replacement = (
            typeof container === "function"
            ? container
            : path.split(".").reduce(
                function (refinement, element) {
                    return refinement[element];
                },
                container
            )
        );
```

如果替换值是一个函数，则调用它以获取替换值。

```javascript
        if (typeof replacement === "function") {
            replacement = replacement(path, encoding);
        }
```

如果提供了编码器对象，则调用其其中一个函数。如果编码器是一个函数，则直接调用它。

```javascript
replacement = (
    typeof encoder === "object"
        ? encoder[encoding]
        : encoder
)(replacement, path, encoding);
```

如果替换值是数字或布尔值，则将其转换为字符串。

```javascript
if (
    typeof replacement === "number"
    || typeof replacement === "boolean"
) {
    replacement = String(replacement);
}
```

如果替换值是字符串，则执行替换。否则，保持符号变量处于其原始状态。

```javascript
return (
    typeof replacement === "string"
        ? replacement
        : original
);
```

如果发生任何错误，则保持符号变量处于其原始状态。

```javascript
} catch (ignore) {
    return original;
}
}
);
});
```

# 第 10 章

## 底部值的工作原理

> 你是浪漫，
> 你是俄罗斯的草原
> 你是 Roxy 引座员穿的裤子
> 我是一个破碎的玩偶，一个废话，一个 Blop
> 但是，宝贝，如果我是底部，
> 你就是顶部！
> *科尔·波特*

底部值是特殊的值，用于表示递归数据结构的结束或值的缺失。在编程语言中，底部值可以有诸如 `nil`、`none`、`nothing` 和 `null` 等名称。

JavaScript 有两个底部值：`null` 和 `undefined`。`NaN` 值也可以被视为一个底部值，表示数字的缺失。大量底部值的存在应被视为一个设计错误。

`null` 和 `undefined` 是 JavaScript 中仅有的两个在模糊意义上不是对象的值。试图从它们获取属性值会引发异常。

在某些方面，`null` 和 `undefined` 彼此非常相似，但在某些方面它们的行为又不同。它们部分可互换，但并非完全可互换。存在两个可以被视为相同但有时行为不同的事物是混淆的根源。试图决定何时使用哪一个会浪费时间，而那些毫无根据的理论会导致更多的混淆，混淆又会导致 Bug。

如果我们消除其中一个，就能编写更好的程序。我们无法从语言中消除其中一个，但我们可以在自己的程序中有利地消除一个。我们应该消除 `null`，并专一地使用 `undefined`。

通常，在被迫在两个词之间做出选择时，我倾向于选择较短的那个。`null` 在编程和数据结构的上下文中有已知的含义，而 `undefined` 没有。此外，`undefined` 是一个令人困惑的名字。它并不意味着数学家所说的 *undefined*（未定义）。它甚至也不意味着程序员所说的 *undefined*（未定义）。

那么，既然 `null` 似乎是一个更合适的名字，为什么我更喜欢 `undefined`？我更喜欢 `undefined`，因为 `undefined` 是 JavaScript 本身使用的值。如果你使用 `let` 或 `var` 定义一个变量而没有显式初始化它，JavaScript 会隐式地将其初始化为 `undefined`，这很令人困惑，因为新定义的变量具有 `undefined` 作为其值。如果你没有向函数传递足够的参数，额外的参数会被设置为 `undefined`。如果你获取一个对象的属性值而对象缺少该属性，它会返回 `undefined`。如果你获取一个数组中数组缺少的元素，它会返回 `undefined`。

我唯一使用 `null` 的地方是使用 `Object.create(null)` 来创建一个新的空对象。规范禁止使用 `Object.create()` 和 `Object.create(undefined)`。

`null` 和 `undefined` 可以用相等运算符进行测试。

```javascript
function stringify_bottom(my_little_bottom) {
    if (my_little_bottom === undefined) {
        return "undefined";
    }
    if (my_little_bottom === null) {
        return "null";
    }
    if (Number.isNaN(my_little_bottom)) {
        return "NaN";
    }
}
```

你有时可能会看到老程序员写 `(typeof my_little_bottom === "undefined")`，这也有效。但是 `(typeof my_little_bottom === "null")` 会失败，因为 `typeof null` 返回 `"object"`，而不是 `"null"`。这是不好的，因为当 `my_little_object` 为 `null` 时，`(typeof my_little_object === "object")` 会给出假阳性，从而导致测试本应防止的错误。这是避免使用 `null` 的另一个原因。

使用 `undefined` 严格优于使用 `null`，但它也存在路径问题。你记得缺失属性的值是 `undefined`，如果 `undefined` 是一个冻结的空对象，这将是件好事，但它不是。`undefined` 不是对象，因此试图从其获取属性会引发异常。这使得编写路径表达式变得棘手。例如，

```javascript
my_little_first_name = my_little_person.name.first;
```

如果 `my_little_person` 没有 `name` 属性或 `my_little_person` 是 `undefined`，就会抛出异常。因此，你不能将由 `.` 点和 `[ ]` 下标组成的链视为一条路径。你必须将其视为一系列单独的操作，其中任何一个都可能失败。这导致了这样的代码：

```javascript
my_little_first_name = (
    my_little_person
    && my_little_person.name
    && my_little_person.name.first
);
```

使用 `&&` 逻辑 *与* 运算符是为了在左边的部分为假值时不评估右边的部分。这又大又丑又慢，但它避免了异常，并且通常能达到

```javascript
my_little_first_name = my_little_person.name.first;
```

在 `undefined` 的行为像对象而不是像反对象时所能达到的效果。



### 语句如何工作

> 当我点头时，你就用锤子砸它。

*布尔温克尔·J·驼鹿*

我们可以将大多数编程语言分为两类：表达式语言和语句语言。语句语言包含语句和表达式。表达式语言只有表达式。表达式语言的拥护者有一套理论，认为表达式语言 vastly superior。似乎没有多少理论来为语句语言辩护。即便如此，所有流行的语言，包括 JavaScript，都是语句语言。

早期程序只是指令列表，有时像句子，在某些语言中甚至以句号结尾。不幸的是，句号与小数点混淆，所以在后来的语言中，语句结束符变成了分号。

结构化编程摧毁了简单语句列表的概念，允许将语句列表嵌套在其他语句中。ALGOL 60 是最早的结构化语言之一，使用 BEGIN 和 END 来界定语句块。BCPL 引入了 \{ 左花括号和 \} 右花括号来替代 BEGIN 和 END。这个六十年代的时尚风潮在许多年里一直流行。

#### 声明

JavaScript 有三个语句用于在函数或模块中声明变量：**let**、**function** 和 **const**。还有一个已废弃的语句 `var`，它用于 Internet Explorer，一款不受喜爱的浏览器。

让我们谈谈 **let**。**let** 语句在当前作用域中声明一个新变量。每个块（用 \{ 左花括号和 \} 右花括号包裹的一串...）创建...一个...作用域。在...作用域中...声明...的...变量...在...作用域...外...不可...见...**let**...语句...允许...但...不...要求...初始化...如果...变量...未...初始化...它...被...赋予...默认...值...`undefined`...**let**...语句...允许...一次...声明...多个...变量...但...我...建议...每个...变量...用...自己...的...**let**...语句...声明...这...提高...了...可读性...和...易...维护...性...。

**let** 语句还允许解构。这是一种 tricky 的语法，用对象或数组的内容来定义和初始化多个变量。所以

```
let {huey, dewey, louie} = my_little_object;
```

是

```
let huey = my_little_object.huey;
let dewey = my_little_object.dewey;
let louie = my_little_object.louie;
```

的简写。

同样，

```
let [zeroth, first, second] = my_little_array;
```

是

```
let zeroth = my_little_array[0];
let first = my_little_array[1];
let second = my_little_array[2];
```

的简写。

解构不是一个重要的特性，但它可以改善一些模式。它也很容易被滥用。有语法便利用于重命名和默认值，但它们引入了太多的视觉复杂性。

函数声明创建一个函数对象和一个包含它的变量。不幸的是，它与函数表达式具有相同的语法，这是一个混淆的来源。

```
function my_little_function() {
    return "So small.";
}
```

是

```
let my_little_function = undefined;

my_little_function = function my_little_function() {
    return "So small.";
};
```

的简写。

注意 `function` 声明不以分号结尾，但 `let` 和赋值语句以分号结尾。

`function` 声明会被提升。这些片段从你放置声明的地方移除，并移动到函数体或模块的顶部。所有由 `function` 声明创建的 `let` 语句都被提升到顶部，然后是函数对象到这些变量的所有赋值。

这就是为什么 `function` 声明不应该放在块中。将 `function` 声明放在函数体或模块中是好的，但将其放在 `if` 语句、`switch` 语句、`while` 语句、`do` 语句或 `for` 语句中是坏的。函数将在第 12 章讨论。

`const` 类似于 `let`，只是它不允许重新赋值。一旦 `const` 变量被初始化，其引用就不能被赋值，而变量不能被赋值。**Object.freeze** 作用于值，而不是变量，**const** 作用于变量，而不是值。理解变量和值之间的区别很重要：变量包含对值的引用。值从不包含变量。

```
let my_little_whitespace_variable = {};
const my_little_constant = my_little_whitespace_variable;
my_little_constant.butterfly = "free";              // {butterfly: "free"}
Object.freeze(my_little_whitespace_variable);
my_little_constant.monster = "free";               // FAIL!
my_little_constant.monster                          // undefined
my_little_constant.butterfly                        // "free"
my_little_whitespace_variable = Math.PI;   // my_little_whitespace_variable 约等于 π
my_little_constant = Math.PI;                        // FAIL!
```

#### 表达式

JavaScript 允许任何表达式出现在语句位置。这是语言设计中一种 sloppy 但流行的做法。JavaScript 有三种表达式类型在语句位置上有意义：赋值、调用和 **delete**。不幸的是，所有其他表达式类型也允许出现在语句位置，这降低了编译器识别错误的能力。

赋值语句替换变量中的引用，或修改可变对象或数组。赋值语句包含四个部分。

1. 一个 *lvalue*，接收值的表达式。它可以是变量，或产生对象或数组值以及细化表达式的表达式：一个 *. period* 后跟属性名，或一个 **[** *左括号* 后跟产生属性名或元素编号的表达式，再跟一个 **]** *右括号*。
2. 一个赋值运算符：
   - *= assignment*
   - *+= add assignment*
   - *-= subtract assignment*
   - `*=` multiply assignment
   - */= divide assignment*
   - *%= remainder assignment*
   - `**=` exponentiation assignment
   - *>>>= shift right assignment*
   - *>>= shift right sign extended assignment*
   - *<<= shift left assignment*
   - *&= bitwise and assignment*
   - *|= bitwise or assignment*
   - *^= bitwise xor assignment*
3. 一个表达式，其值将被存储。
4. 一个 *;* *semicolon*。

我不建议使用增量运算符 **++** *plus plus* 或 **--** *minus minus*。它们在古代被创建用于指针算术。我们之后发现指针算术是有害的，所以现代语言不再允许它。最后一种以拥有指针算术为荣的流行语言是 C++，一种如此糟糕以至于以 **++*plus plus* 命名的时才命名的语言。

我们去掉了指针算术，但仍然被困在 ++ 上。现在它给某物加 1。为什么我们认为我们需要一种不同的语法形式来加 1，而不是加其他每一个值？这有什么意义？

答案是：**这没有任何意义。**

更糟糕的是，++ 有前置增量形式和后置增量形式。非常容易将它们弄反，而且这可能非常难以调试。而且 ++ 已经被牵连到缓冲区溢出错误和其他安全故障中。我们应该丢弃不必要且有危险的特性。

表达式语句是不纯的。赋值语句和 `delete` 显然引起 mutation。丢弃返回值的调用依赖于副作用。表达式语句是唯一不以标识关键字开头的语句。这种语法优化鼓励了不纯。

#### 分支

JavaScript 有两个分支语句，`if` 和 `switch`，这要么多了一个，要么多了两个。

我不建议使用 `switch`，它是 C. A. R. Hoare 的 `case` 语句和 FORTRAN 的计算 `goto` 语句的 unholy 混合体。没有什么用 `switch` 语句能写的不能用 `if` 语句写（通常更紧凑）。`switch` 语句提供了一个隐式的 switch 变量，但 suffers from a fallthrough hazard，可能导致错误和 bad practices。还有风格问题：`case` 应该与 `switch` 对齐还是应该缩进？似乎没有正确答案。

对象可以用作 `switch` 语句的替代。用一个对象填充实现每种情况行为的函数。匹配 `case` 变量的值是键。

```
const my_little_result = my_little_object[case_expression]();
```

你的 *case_expression* 从对象中选择一个函数，然后可以调用它。如果 *case_expression* 不匹配你的任何函数，会为你抛出异常。

不幸的是，这种形式也带来了潜在的安全隐患，因为 `this` 的绑定。第 16 章会有更多关于 `this` 的内容。

`if` 语句严格优于 `switch` 语句。它的 `else` 不是语句，而是子句，所以不应该像语句那样缩进。`else` 应该放在 `}` *右括号* 的同一行，这个 `}` 关闭了前一个块。

JavaScript 期望条件部分是 boolish 值。我认为那是一个错误。JavaScript 应该坚持要求布尔值。我建议你提供布尔值，尽管语言邀请你更 sloppy。

`else if` 形式允许 `if` 语句替代 `switch` 语句，而不需要在屏幕上 wild indenting。它可能被滥用，导致 confusing control flows。`else if` 形式只应在类 case 结构中使用。如果一个 `else` 子句以 `if` 开头，可能最好不要使用 `else if`，而是将

如果在 `else` 代码块中使用。如果前面的代码块以中断结束，则不应使用 `else if` 形式。

在编写纯函数式风格代码时，使用三元运算符可能更好。三元运算符常被误用，这给它带来了坏名声。将整个三元表达式括在括号中。在开括号后换行，并将条件与两个结果对齐。

```
let my_little_value = (
    is_mythical
    ? (
        is_scary
        ? "monster"
        : "unicorn"
    )
    : (
        is_insect
        ? "butterfly"
        : "rainbow"
    )
);
```

#### 循环

JavaScript 有三种循环语句：`for`、`while` 和 `do`，它们要么是多余的两种，要么是多余的三种。

`for` 语句是 FORTRAN 语句 `DO` 的后代。两者都用于一次处理数组的一个元素，将管理归纳变量的大部分工作推给了程序员。我们应该使用像 `forEach` 这样自动管理归纳变量的数组方法。我预计在该语言的未来版本中，数组方法在被赋予应用于元素的纯函数时，将能够并行完成大部分工作。使用 `for` 语句的低效程序仍将一次处理一个元素。

我在教授初学者编程时发现，三部分控制（初始化；条件；增量）令人困惑。这些子句是什么以及为什么按特定顺序排列并不明显，并且没有语法上的便利来使其易于发现或记忆。

我不推荐使用 `for` 语句。

`while` 语句和 `do` 语句都用于一般循环。它们在语法上非常不同，但在操作上唯一的区别是 `while` 语句在循环顶部检查其条件，而 `do` 语句在底部检查其条件。奇怪的是，如此大的视觉差异却只有如此小的操作差异。

我发现我的许多循环并不希望只在顶部或底部中断。它们通常希望在中间中断。因此，我的许多循环具有这种形式：

```
while (true) {
    // 做一些工作
    if (我们完成了) {
        break;
    }
    // 做更多工作
}
```

编写循环的最佳方法是使用尾递归（第18章）。

#### 中断

JavaScript 有四个改变控制流的中断语句，它们都不是 `goto`！它们是 `break`、`continue`、`throw` 和 `return`。

`break` 语句用于退出循环。如果我们使用 `switch` 语句，它也可以用于退出 `switch` 语句，但如果 `switch` 语句在循环中，这会变得复杂。

`continue` 语句是一个跳转到循环顶部的 `goto` 语句。我从未见过包含 `continue` 的程序在移除它后没有得到改进。

`throw` 语句引发一个异常（第14章）。

我最喜欢的中断语句是 `return`。它结束函数的执行并指定返回值。有一种学派认为函数应该只有一个 `return` 语句。我从未看到任何证据表明这种教学是有益的。我认为更有意义的是函数在知道需要返回时返回，而不必先汇聚到一个唯一的出口点。

JavaScript 没有 `goto` 语句，但它确实允许所有语句都有标签。我认为这是一个错误。语句不应该需要标签。

#### 杂项

`throw` 语句、`try` 语句和 `catch` 子句将在第14章讨论。

`import` 和 `export` 语句将在第15章讨论。

`debugger` 语句可能导致执行暂停，类似于到达断点。`debugger` 语句应仅在开发期间使用。在将程序投入生产之前应将其移除。

#### 标点符号

JavaScript 允许 **if**、**else** 和循环语句接受单个语句或一个代码块。始终使用代码块，即使代码块只包含一个语句。这使代码更具弹性。在改进代码时更容易，而不会引入错误。不要在代码中设置语法陷阱，可能会绊倒你的队友。编写代码时，就好像代码始终正常工作很重要一样。

表达式语句、`do` 语句、中断语句和 **debugger** 语句都以 `;` *分号* 结尾。JavaScript 有一个被称为自动分号插入的特性，旨在通过允许初学者省略 `;` *分号* 来使编码更容易。不幸的是，它可能会以错误的方式失败，因此请像专业人士一样编写。如果 JavaScript 设计时采用无分号语法会更好，但它没有，所以不要假装它是。这种混淆可能导致错误。

如果一条语句太长无法放在一行中，则需要换行。我在 `(` *左括号*、`[` *左方括号* 或 `{` *左花括号* 之后换行。匹配的 `)` *右括号*、`]` *右方括号* 或 `}` *右花括号* 在与开始换行的行相同的缩进级别开始新行。中间的内容将缩进四个空格。

# 第12章

## 函数如何工作

> 事实是，如果有合适的程序可用，每个人都会使用它们；在程序构建中使用它们的优势实际上是压倒性的。
> *Ian F. Currie*

最早的程序被称为 *例程*。例程是一系列命令（或指令）。例程与一些数据一起加载到机器中，随着时间的推移，加上一些运气，一个答案被输出。

人们观察到，将例程作为单个列表来管理很困难。一些命令序列可能出现在多个例程中，或者可能在同一例程中多次出现。因此发明了子例程。一组有用的子例程可以收集到一个库中。每个子例程都有一个调用号，类似于图书馆书籍的调用号。（名字是奢侈的。）

Grace Murray Hopper 开发了一个名为 A-0 的例程。它是第一个编译器。它会获取一系列命令和调用号以及一个包含子例程库的磁带。它会找到与调用号对应的子例程，并将它们编译成一个新程序。*编译* 的意思是文学意义上的：通过从其他来源汇编信息来创作作品。这给了我们许多至今仍在使用的术语：汇编器、编译器、库、源代码，以及最重要的调用。我们调用子例程就像我们在图书馆调用一本书一样。我们不开始或激活子例程。我们调用它。Grace Murray Hopper 帮助建立了我们专业中的许多术语。因为 Grace Murray Hopper，我们称这些机器为 *计算机* 而不是 *电子脑*。因为 Grace Murray Hopper，我自豪地称自己为 *程序员*。

人们观察到子例程与数学函数有关。FORTRAN II 有一个 `SUBROUTINE` 声明和一个用于激活它们的 `CALL` 语句，它还有一个 `FUNCTION` 声明，可以返回一个可以为表达式贡献值的结果。

C 语言统一了子例程和函数，所有非正式地称为函数。C 没有使用描述性关键字。JavaScript 有：`function`。

`function` 运算符创建函数对象。`function` 运算符接受一个参数列表和一个函数体。函数体是一个语句块。

参数列表中的每个名称都是一个变量，它通过来自参数列表的表达式初始化。每个名称后面可以可选地跟随 `=` *等号* 和一个表达式。如果参数值是未定义的，则使用表达式的值代替。

```
function make_set(array, value = true) {
    // 通过从字符串数组中获取属性名来创建一个对象。
    const object = Object.create(null);
    array.forEach(function (name) {
        object[name] = value;
    });
    return object;
}
```

函数对象通过包含零个或多个表达式（用逗号分隔）的参数列表进行调用。这些表达式中的每一个都被求值并绑定到函数的参数。

参数列表和参数列表不必具有相同的长度。多余的参数被忽略。缺少的参数给出未定义值。

`...` *省略号* 运算符允许在参数列表和参数列表中使用。在参数列表中，它被称为 *展开*。它接受一个数组并将其展开，以便数组的每个元素被视为一个单独的参数。在参数列表中，它被称为 *剩余*。所有剩余的参数被打包到一个数组中，该数组绑定到该参数名称。剩余参数必须是参数列表中的最后一个参数。这允许函数处理可变数量的参数。

```
function curry(func, ...zeroth) {
    return function (...wunth) {
        return func(...zeroth, ...wunth);
    };
}
```

当调用函数时，会创建一个激活对象。激活对象对你不可见。它是一个隐藏的数据结构，保存函数执行所需的信息和绑定，以及调用函数的激活返回地址。

在 C 等语言中，激活对象在栈上分配。当函数返回时，它们被解除分配（或弹出）。JavaScript 的处理方式不同。JavaScript 在堆上分配激活对象，就像普通对象一样。激活对象在函数返回时不会自动停用。相反，只要存在对它的引用，激活对象就可以存活。激活对象像普通对象一样被垃圾回收。

激活对象包含：

- 对函数对象的引用。
- 对调用者的激活对象的引用。这被 `return` 用来将控制权交还。
- 用于在调用后继续执行的恢复信息。这通常是紧跟在函数调用之后的指令地址。



### 函数的工作原理

- 函数的参数，由传入的实参初始化。
- 函数的变量，初始化为 undefined。
- 函数用于计算复杂表达式的临时变量。
- `this`，它可能是相关 Revival 对象的引用，前提是函数对象作为方法被调用。

函数对象与普通可变对象一样，可以作为属性的容器。这并不是一件好事。理想情况下，函数对象应该是不可变的。在某些安全场景中，共享的可变函数对象可能被用于串通作弊。

函数对象有一个 `prototype` 属性。这在（不推荐的）伪经典模型中使用。`prototype` 属性包含对一个对象的引用，该对象包含一个 `constructor` 属性（指回函数对象自身），以及一个指向 `Object.prototype` 的委托链接。更多内容将在第16章介绍。

函数对象有一个指向 `Function.prototype` 的委托链接。通过这一链接，函数对象继承了并不必要的 `apply` 和 `call` 方法。

函数对象还包含两个隐藏属性。

- 指向函数可执行代码的引用。
- 指向创建函数对象时处于活动状态的激活对象的引用。这是闭包得以实现的关键。函数可以使用这个隐藏属性来访问创建它的那个函数的变量。

术语*自由变量*有时用于描述函数所使用的、在函数外部声明的变量。术语*绑定变量*有时用于描述在函数内部声明的变量，包括参数。

函数可以嵌套。当内部函数对象被创建时，它包含一个指向创建它的外部函数的激活对象的引用。

这种机制——函数对象持有对外部函数激活对象的引用——被称为*闭包*。这是迄今为止编程语言历史上最重要的发现。它最早在 Scheme 语言中被发现，通过 JavaScript 进入主流视野。正是闭包让 JavaScript 成为一门有趣的语言。没有它，JavaScript 只不过是一堆善意、失误和类的 steaming 大杂烩。

# 第13章：生成器的工作原理

> 当代作曲家拒绝死亡。
> *埃德加·瓦雷兹*

JavaScript 在 ES6 中引入了一个称为*生成器*的特性。它们是在标准制定过程严重向往 Python 的时期被加入的。出于几个原因，我不推荐使用 ES6 生成器。

代码的实际行为与其外观大相径庭。它们看起来像普通函数，但工作方式却完全不同。它们产生一个函数对象，该对象产生一个包含 `next` 方法的对象，而这个方法由 `function*` 体构成。它有一个 `yield` 运算符，类似于 `return` 语句，但并不产生预期的值。相反，它产生一个包含 `value` 属性的对象，而该属性才包含预期的值。一个小小的 `*` *星号*就能导致行为的巨大变化。

它们可能具有非常复杂的控制流。我们在结构化革命中学到，控制流应该直截了当且可预测。生成器可以有复杂的控制流，因为生成器可以被暂停和恢复。它们还可能导致与 `finally` 和 `return` 之间令人困惑的交互。

它们鼓励使用循环。当我们从对象转向函数时，我们应该远离循环。而这些生成器却需要更多的循环。大多数生成器中间包含一个带有 `yield` 的循环来产生值。大多数生成器的使用者用 `for` 循环来消费这些值。这是两处本不必要的循环。

生成器使用笨拙的面向对象接口。工厂产生一个对象，生成器也产生一个对象。（在函数式设计中，工厂产生一个生成器函数，生成器函数产生一个值。函数式设计更简单、更干净、更易于使用。）

最后，最糟糕的是，ES6 生成器是不必要的。当有更好的选择时，我不推荐使用某些特性。

## 13.1 生成器的工作原理

这是 ES6 生成器的一个示例：

```javascript
function* counter() {
    let count = 0;
    while (true) {
        count += 1;
        yield count;
    }
}

const gen = counter();

gen.next().value                       // 1
gen.next().value                       // 2
gen.next().value                       // 3
```

这是我推荐的做法：

```javascript
function counter() {
    let count = 0;
    return function counter_generator() {
        count += 1;
        return count;
    };
}

const gen = counter();

gen()                                  // 1
gen()                                  // 2
gen()                                  // 3
```

所以，与其写一个看起来像函数、会 yield 一个值，但实际上是返回一个包含 next 方法的对象、该方法 yield 一个包含 value 属性的对象、而该属性才包含实际值的代码，不如简单地写一个返回函数、而该函数返回值的函数。

### 更好的方式

生成器确实是个好东西。所以我们应该正确地使用它。我们从一个返回函数的函数开始。外部函数是一个*工厂*。内部函数是一个*生成器*。这是通用模式：

```javascript
function *factory(factory's parameters) {

    Initialization of the generator's state

    return function *generator(generator's parameters) {

        update the state

        return *value*;
    };
}
```

当然，可以有多种变体。生成器的状态安全地保存在工厂的变量中。

## 13.2 生成器的工作原理

这种模式最简单的有用实例是常量工厂。它接收一个值，返回一个总是返回该值的生成器。

```javascript
function constant(value) {
    return function constant_generator() {
        return value;
    };
}
```

更有用的例子是整数工厂。它返回一个生成器，每次被调用时返回序列中的下一个整数。序列结束时返回 undefined。我们使用 undefined 作为表示序列结束的标志。

```javascript
function integer(from = 0, to = Number.MAX_SAFE_INTEGER, step = 1) {
    return function () {
        if (from < to) {
            const result = from;
            from += step;
            return result;
        }
    };
}
```

元素工厂接收一个数组，返回一个每次被调用时返回该数组元素的生成器。没有更多元素时返回 undefined。工厂可以接收一个可选的第二参数：一个产生元素索引的生成器，用于检索元素。默认情况下，它按顺序检索所有元素。

```javascript
function element(array, gen = integer(0, array.length)) {
    return function element_generator(...args) {
        const element_nr = gen(...args);
        if (element_nr !== undefined) {
            return array[element_nr];
        }
    };
}
```

属性工厂对对象做同样的事。它以包含键和值的数组形式返回对象的每个属性。没有更多属性时返回 undefined。工厂可以接收一个可选的第二参数：一个产生键的生成器，用于检索属性。默认情况下，它按插入顺序检索所有自有属性。

```javascript
function property(object, gen = element(Object.keys(object))) {
    return function property_generator(...args) {
        const key = gen(...args);
        if (key !== undefined) {
            return [key, object[key]];
        }
    };
}
```

collect 工厂接收一个生成器和一个数组。它返回一个生成器，该生成器与接收到的生成器工作方式完全相同，只是还会将有趣的返回值追加到数组中。传递给新函数的所有参数都会传递给原来的生成器。



# 生成器如何工作

```
function collect(generator, array) {
    return function collect_generator(...args) {
        const value = generator(...args);
        if (value !== undefined) {
            array.push(value);
        }
        return value;
    };
}
```

我们可以使用 `repeat` 函数作为驱动。它接收一个函数并调用它，直到它返回 undefined。这是我们唯一需要的循环。我们可以用 do 语句编写它，但我更喜欢用尾递归（第18章）来写。

```
function repeat(generator) {
    if (generator() !== undefined) {
        return repeat(generator);
    }
}
```

我们可以使用 `collect` 来捕获数据。

```
const my_array = [];
repeat(collect(integer(0, 7), my_array)); // my_array 是 [0, 1, 2, 3, 4, 5, 6]
```

我们可以将 `repeat` 和 `collect` 组合在一起，创建 `harvest`。`harvest` 函数既不是工厂也不是生成器，但它接受一个生成器作为参数。

```
function harvest(generator) {
    const array = [];
    repeat(collect(generator, array));
    return array;
}
```

```
const result = harvest(integer(0, 7));  // result 是 [0, 1, 2, 3, 4, 5, 6]
```

`limit` 工厂接受一个函数并返回一个只能使用有限次数的函数。当计数耗尽时，新函数除了返回 undefined 外什么都不做。工厂的第二个参数是新函数可以被调用的次数。

```
function limit(generator, count = 1) {
    return function (...args) {
        if (count >= 1) {
            count -= 1;
            return generator(...args);
        }
    };
}
```

`limit` 工厂可以与任何函数一起使用。例如，如果你将一个许愿函数和数字3传递给 `limit`，你将得到一个可以许愿3次的函数。

`filter` 函数接受一个生成器和一个谓词函数。谓词函数是一个返回 `true` 或 `false` 的函数。它返回一个新的生成器，其工作方式与旧的类似，但只提供谓词返回 `true` 的值。

```
function filter(generator, predicate) {
    return function filter_generator(...args) {
        const value = generator(...args);
        return value
            if (value !== undefined && !predicate(value)) {
                return filter_generator(...args);
            }
            return value;
    };
}
```

```
const my_third_array = harvest(filter(
    integer(0, 42),
    function divisible_by_three(value) {
        return (value % 3) === 0;
    }
));
// my_third_array 是 [0, 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39]
```

`concat` 工厂可以接受两个或多个生成器，并将它们连接在一起，形成一个合并了它们序列的新生成器。它从第一个生成器取值，直到它产生 undefined。然后切换到下一个生成器。`concat` 工厂使用我们之前看到的 `element` 工厂来智能地遍历生成器。

```
function concat(...generators) {
    const next = element(generators);
    let generator = next();
    return function concat_generator(...args) {
        if (generator !== undefined) {
            const value = generator(...args);
            if (value === undefined) {
                generator = next();
                return concat_generator(...args);
            }
            return value;
        }
    };
}
```

`join` 工厂接受一个函数和一个或多个生成器，并返回一个新的生成器。每次调用新生成器时，它都会调用所有旧生成器，并将它们的结果传递给该函数。你可以将 **join** 与 **repeat** 一起使用，来完成过去用 **for of** 所做的所有事情。`join` 的函数参数承担了代码块的工作。`join` 工厂可以同时处理多个生成器流。

```
function join(func, ...gens) {
    return function join_generator() {
        return func(...gens.map(function (gen) {
            return gen();
        }));
    };
}
```

我们可以利用所有这些来制作一个类似数组 **map** 方法的 `map` 函数。它接受一个函数和一个数组，并返回一个新数组，其中每个元素都包含用该函数处理数组每个元素后的结果。

```
function map(array, func) {
    return harvest(join(func, element(array)));
}
```

`objectify` 工厂为我们提供了构建数据对象的另一种方式。

```
function objectify(...names) {
    return function objectify_constructor(...values) {
        const object = Object.create(null);
        names.forEach(function (name, name_nr) {
            object[name] = values[name_nr];
        });
        return object;
    };
}

let date_marry_kill = objectify("date", "marry", "kill");
let my_little_object = date_marry_kill("butterfly", "unicorn", "monster");
    // {date: "butterfly", marry: "unicorn", kill: "monster"}
```

生成器存在于纯函数和不纯函数的边界上。由常量工厂创建的生成器是纯的，但大多数生成器都带有不纯的特质。生成器可以有状态，但它们将其状态隐藏在工厂的闭包中。状态只能通过调用生成器来更新。它们没有困扰大多数不纯函数的副作用。这使得生成器能够很好地组合。

最好让我们的程序尽可能多地保持纯。与外部世界交互的程序不可能是完全纯粹的，因为世界本身就不是纯粹的。我们如何知道什么可以是纯粹的，什么必须是不纯粹的？生成器可以向我们展示一条道路。

# 第 14 章

## 异常如何工作

> 不！别试了。做，或者不做。
> 没有“试”这一说。
>
> *尤达大师*

程序员是乐观主义者。在我们的程序中，常常隐含着一种假设，即一切都会顺利进行，但即使是最乐观的人也知道，有时事情也会出错。

我们调用的函数有可能以意想不到的方式失败。这在使用第三方代码时尤其令人担忧。耦合的一个维度就是故障模式。那么当它失败时应该发生什么？整个程序应该崩溃吗？我们应该尝试再次调用函数并期望得到更好的结果吗？故障又该如何传达呢？

处理这个问题最流行的方法是异常处理，它试图让我们能够乐观地编程。我们不必在每个返回值中检查晦涩的错误代码。我们也不必轮询一个全局的 *defcon* 寄存器来发现程序是否变得不稳定。相反，我们假设一切都能正常工作。如果发生意外情况，当前活动将停止，而我们的异常处理程序将决定程序接下来做什么。

JavaScript 的异常管理受到 Java 的启发。Java 的异常管理受到 C++ 的启发。C++ 是一种没有足够内存管理的语言，所以当出现问题时，调用链中的每个函数都需要显式地释放它所分配的任何内存。JavaScript 有非常好的内存管理，但它假设了 C++ 有缺陷的内存模型所带来的影响。

故障通过 `throw` 语句发出信号。C++ 本可以像 Ada 语言那样有一个 `raise` 语句，但 `raise` 这个词已经在 C 库中使用了，所以 C++ 选择了一个从来没人想用的保留字。

JavaScript 允许你 `throw` 任何值。通常会 `throw` 由 `Error` 构造函数创建的东西，但这并不是必须的。你真的可以抛出任何东西。在 C++ 和 Java 中，异常对象是麦高芬。在编写良好的 JavaScript 中，异常对象是多余的。

```
throw "That does not compute.";
```

### 14.1 异常如何工作

try 语句将异常处理程序附加到一个代码块。异常处理程序被封装为一个 catch 子句。它允许一个参数，用于接收 throw 抛出的任何内容。

```
try {
    here_goes_nothing();
} catch {
    console.log("fail: here_goes_nothing");
}
```

如果在 try 中抛出了任何异常，那么 catch 子句就会运行。

try 的设计允许非常细粒度的异常管理。函数中的每个语句都可以有自己的 try 和自己的 catch。它甚至允许 try 语句包含 try 语句。更糟糕的是，它允许 catch 子句包含 try 语句，而 try 语句和 catch 子句又可以包含 throw 语句。一个函数不应该包含多个 try。

## 解栈

异常管理成功保持的一个重要目标是，它不会对正确运行的程序造成性能损失。在抛出异常时可能会发生性能下降，但这种情况应该很少发生，即使发生，代价也不是很高。

JavaScript 编译器为它编译的每个函数生成一个 catchmap。catchmap 将函数体中的指令位置映射到处理这些位置的 catch。在正常的程序执行期间不会使用 catchmap。

当执行 throw 语句，抛出异常时，会查询当前函数的 catchmap。如果有一个指定的 catch 子句，那么它将获得控制权，并从那里恢复执行。

如果没有指定的 catch 子句，那么我们就查看调用者。调用者现在是当前函数，而调用前一个函数的语句现在是故障的位置。再次查询 catchmap。如果有一个指定的 catch 子句，那么它将获得控制权，并从那里恢复执行。

如此继续，沿着虚拟调用栈向下，直到找到一个 catch 子句。当调用栈为空时，我们就得到了一个未捕获的异常。

这是一个简单而优雅的机制。它允许一种编程风格，将主要精力集中在成功上，而不完全忽略失败。但它也很容易被滥用。

## 普通异常

最常见的异常误用是用它们来传达正常结果。例如，给定一个读取文件的函数，一个 *文件未找到* 的错误不应该是异常。这是一种正常情况。异常应该只用于那些不应该预料到的问题。

Java 语言鼓励滥用异常来解决其类型系统中的问题。一个 Java 方法只能返回单一类型的结果，因此异常被用作一个替代通道，来返回类型系统不允许的普通结果。这可能导致一个 try 块附带多个 catch 子句。这可能会令人困惑，因为普通结果与真正的异常混在了一起。



它类似于 FORTRAN 中的赋值 GOTO 语句，即变量包含跳转目标的地址。catch 子句必须正确排序，以确保选择正确的子句。选择并非基于某种相等性（如 switch 语句那样），而是基于类型转换规则，而这些规则本身也是一种令人憎恶的设计。任何需要显式类型转换的类型系统都是有缺陷的。

控制路径由创建异常对象的方法决定。这会在抛出者和捕获者之间产生紧密耦合，不利于模块化的清晰设计。

通过这团乱麻可能存在非常多的路径，这使得释放已分配资源的工作变得相当具有挑战性。因此 finally 子句被加入以缓解这一问题。finally 子句是一个无参函数，它隐式地从 try 块和每个 catch 子句的每个退出点被调用。

另一方面，JavaScript 提供了一种更为简洁的方法。如果 try 成功，那么我们获得了一个良好的结果或一个良好的解释。JavaScript 的类型系统足够灵活，能够处理所有预期的情况。

如果真正发生了出乎意料的事情，那么 catch 子句启动，另一个故事开始，要么关闭一切，要么重新开始。我们采用计划 A。如果成功，那就好。如果失败，我们直接转向计划 B。

```
try {
    plan_a();
} catch {
    plan_b();
}
```

关于错误恢复的推理是困难的，而测试它则更加困难。因此我们应该采用简单且可靠的模式。将所有预期结果作为返回值。将异常留给真正的异常情况。

问题在于，有很多程序是由那些受其他语言经验影响的人开发的。他们该返回时却使用 throw。他们编写复杂的 catch 子句，试图解决无法解决的问题并维护无法维护的不变量。 affiliate And they use finally, which JavaScript has but does not need, to try to clean up their mess. 而且他们使用 finally——JavaScript 虽然有但并非必需——来试图清理他们的烂摊子。

## 事件uality

异常通过栈展开来工作。抛出的值被传递给栈中更低层的函数调用。在事件驱动编程中，栈在每个回合后都会被清空。时间旅行无法用来将抛出的值传送给已不存在的激活。异常的用途有限。它们只能报告当前时间框架内的局部问题。我们将在第 20 章探讨这一点。

## 安全性

有一种重要的安全模型，通过只给予函数完成工作所需的引用、仅此而已，来限制函数的破坏力。就目前实践而言，异常提供了一个通道，使两个不可信的函数能够串通。

情况是这样的：Thing 1 和 Thing 2 是我们不小心安装到服务器上的两个包。这样做我们承担着可怕的风险，但我们认为这是可接受的风险，因为 Thing 1 和 Thing 2 有时很有用。我们给予 Thing 1 访问网络套接字的权限。我们给予 Thing 2 访问我们私钥的权限。如果它们无法相互通信，我们就没事。

Thing 1 需要解密某些东西作为其功能的一部分，但我们不希望它与 Thing 2 直接通信。因此我们创建一个受信赖的中介函数。我们允许 Thing 1 调用中介。中介调用 Thing 2。Thing 2 向中介返回值。中介检查返回值，确认它是预期的明文，然后将其返回给 Thing 1。

如果 Thing 2 改为这样做：

```
throw top_secret.private_key;
```

而且如果中介没有捕获它，或者捕获后又重新抛出（C++ 推广的一种糟糕做法），那么 Thing 1 就可以捕获私钥并将其传给坏人。这就形成了串通。

## 可靠性

当严重问题发生时，程序能期望做些什么呢？一个函数调用另一个函数时期望它能工作。但假设它没有工作。异常对象告诉函数某个参数超出范围，或者某个对象不可变，或者犯了其他错误。以我们目前的技术水平，期望函数采取纠正措施是不合理的。

异常对象中的细节可能对程序员来说很重要、很有用。但这些信息被传递给了一个无法善加利用的函数。我们破坏了信息流程。这些信息应该发送给程序员，也许以日志条目的形式。相反，它被发送到了调用栈下方，在那里可能被误解和遗忘。异常导致我们设计了不良的系统。异常机制本身正在造成不可靠性。

# 第 15 章
## 程序如何工作

> "Greetings, programs!"（你们好，程序们！）
> ——凯文·弗林

JavaScript 以源代码形式被传送到执行点。JavaScript 最初的工作是为网页添加一些交互性。由于 HTML 是一种文本格式，因此决定将 JavaScript 作为源代码文本嵌入网页中。这是相当不寻常的。大多数其他语言的程序是以特定机器的指令代码，或更便携的格式（如将输入解释器或代码生成器的字节编码指令流）传送到执行点的。

执行点的 JavaScript 引擎编译 JavaScript 源代码，生成机器代码、解释代码或两者兼具。这使得 JavaScript 成为一种非常便携的语言。程序不依赖于底层机器的架构。单个版本的 JavaScript 程序可以在任何 JavaScript 引擎上运行，无论其底层是什么。

JavaScript 编译器能够快速、轻松地验证程序的一些重要安全属性：它可以确保程序不能计算内存地址、跳转到受限位置或违反类型限制。Java 试图用其字节码验证器做类似的事情，但速度没那么快、没那么容易，也没那么确定。

JavaScript 的某些语法特性使得解析变得不必要地困难。即便如此，JavaScript 引擎编译、加载和启动的速度仍远快于 Java 从 .jar 文件加载和启动的速度。

JavaScript 以源代码单元形式分发。源代码单元通常是一个 .js 文件，但也可以是 JSON 对象中的源代码字符串，或来自数据库或源代码管理系统的源文本。

在古老的浏览器中，源代码单元是页面的一部分，如 `<script>` 标签的内容或内联事件处理器。在下面的例子中，`alert("Hi");` 就是一个源代码单元。

```
<img src=hello.png onclick=alert("Hi");>
```

现在普遍认为，将 JavaScript 源代码单元嵌入 HTML 页面是一种不良做法。这对设计有害，因为表现和行为之间没有分离。这对性能有害，因为页面中的代码无法被 gzip 压缩或缓存。这对安全性非常有害，因为它促成了名称不当的跨站脚本（XSS）攻击。应始终使用 W3C 的内容安全策略（CSP）来阻止所有内联源代码的使用。

源代码单元被视为一个无参函数的主体。它被编译为一个函数，然后被调用。它可能导致函数对象被创建，也可能被执行。

这可能就是程序的终点。但在 JavaScript 中，源代码单元通常会注册接收事件或消息，或导出一个可能被另一个源代码单元使用的函数。JavaScript 不要求必须这样编写程序，但这是一个很好的编程方式，而且 JavaScript 对这种方式的支持优于大多数语言。

（历史注记：内联事件处理器的工作方式略有不同。源代码单元仍然被视为函数体，但这样创建的事件处理器函数不会立即被调用。相反，它被绑定到一个 DOM 节点，并在事件触发时被调用。）

### 原始对象

有一些对象和函数会自动提供给每个源代码单元。我们已经见过其中一些，如 `Number`、`Math`、`Array`、`Object` 和 `String`。还有更多，全部由 ECMAScript 标准提供。此外，宿主环境（例如浏览器或 Node.js）可能会添加更多。你的源代码单元中的所有函数都可以使用这些东西。

### 全局

在古老的浏览器编程模型中，函数外部的所有变量声明都会被添加到*页面*作用域，也称为*全局*作用域（够宏大吧？）。该作用域还包含变量 `window` 和 `self`，它们包含对页面作用域的引用。页面作用域中的所有变量对该页面上的所有源代码单元都是可见的。

这是一件坏事。它助长了一种利用共享全局变量的编程风格。这导致程序脆弱且漏洞百出。当两个独立的源代码单元意外使用相同的变量名时，会导致意外的错误。它还造成了严重的安全问题。这正是 XSS 漏洞的温床。

全局变量是邪恶的。

幸运的是，现在情况好多了。



### 模块

最好将所有在函数外部的变量声明添加到*模块*作用域中，该作用域仅对源单元中的所有函数可见。这是一件好事，因为它能带来更强的设计、更高的安全性和更好的保障。

现在，与其他源单元的合作是显式的，使用**import**和**export**语句。这些语句可用于构建优秀的程序，当然也可能被用来编写糟糕的程序。我专注于好的方面。

通过导出，模块将其导出内容提供给其他模块。一个模块通常应该只导出一个东西，通常是一个函数或一个充满函数的对象。该导出内容可能会被其他多个模块使用，因此将导出内容冻结是一个好主意，可以防止意外或交叉污染。导出内容就是接口。接口应当简洁明了。

源单元的代码主体只执行一次，这意味着所有的导入者共享同一个导出内容。如果导出内容是有状态的，而每个导入者都期望获得原始且未共享的内容，这可能会成为问题。在这种情况下，可以导出一个能够创建原始且未共享实例的工厂函数。**export**语句本身并不创建实例。

**export**语句看起来像这样：

```
export default exportation;
```

真的很不幸，**default**这个词在这里有点碍事。*exportation*表达式就是你要导出的冻结对象或函数。

导入允许你的源单元从另一个源单元接收一个函数或对象。你可以为接收导入的新变量命名。你还需要用一个“双引号”字符串字面量指定提供者，其中包含某种名称或地址，你的系统可以用它来定位源单元，并在必要时读取、编译、加载、调用它，并传递其导出内容。

你可以把**import**语句看作一个特殊的**const**语句，其初始值来自其他地方。它看起来像这样：

```
import name from string literal;
```

我建议只使用单个**export**，但你可以根据需要使用任意多的**import**语句。将导入放在文件顶部，导出放在底部。

### 内聚与耦合

微观层面的良好编程依赖于良好的编码规范，这些规范有助于增加好代码与坏代码之间的视觉距离，从而使错误更容易被发现。

宏观层面的良好编程则依赖于良好的模块设计。

好的模块具有强内聚性。这意味着所有元素都相互关联，并协同工作以完成特定任务。坏的模块内聚性弱，通常是由于组织混乱和试图做太多事情。JavaScript的函数在这里可以大显身手，因为我们可以传入一个函数来处理模块不应关心的特定细节。

好的模块是松耦合的。你应该只需要了解模块接口的有限知识就能很好地使用它。你不需要了解其实现细节。好的模块会隐藏其实现。泄漏的模块会招致紧耦合。JavaScript提供了许多紧耦合的诱惑。相互依赖的模块确实是紧密耦合的。这几乎和全局变量一样糟糕和严重。

让你的模块接口简洁明了。尽量减少依赖。良好的架构对于给程序提供足够的结构至关重要，使其能够发展壮大而不至于崩溃成一片混乱。

内聚和耦合的概念在两本优秀的书籍中引入：

- 《通过组合设计实现可靠软件》。格伦福德·迈尔斯。约翰·威利父子公司，1975年。
- 《结构化设计》。爱德华·尤登和拉里·L·康斯坦丁。尤登出版社，1979年。

这两本书在面向对象编程成为潮流之前就出版了，因此它们已经过时并基本被遗忘。但它们关于强内聚和松耦合的教导仍然是正确且重要的。

# 第16章：this的工作原理

> 我发明了*面向对象*这个术语，我可以告诉你我当时心里想的可不是C++。
> *艾伦·凯*

Self语言是Smalltalk的一种方言，它用原型取代了类。对象可以直接从另一个对象继承。经典的模型由于通过`extends`紧密耦合类而显得脆弱和臃肿。Self的原型是一种绝妙的简化。原型模型更轻量且更具表现力。JavaScript实现了一种奇特的原型模型变体。

当创建一个对象时，可以指定一个原型，它持有新对象的部分或全部内容。

```
const new_object = Object.create(old_object);
```

对象只是属性的容器，而原型也只是对象。方法只是存储在对象中的函数。

如果我们尝试检索一个对象没有的属性的值，结果是`undefined`值。然而，如果对象有一个原型（如上面的`new_object`），那么结果是原型的属性的值。如果那也失败了，并且原型还有一个原型，那么结果就是原型的原型的属性的值。如此不断向下追溯。

许多对象共享一个原型是可能的。这些对象可以被视为一个类的实例，但它们实际上只是碰巧共享一个原型的独立对象。

原型最常见的用途是作为存储方法的地方。相似的对象可能都有相似的方法，因此如果将方法放在一个共享的原型中而不是每个对象中，可能会节省内存。

原型中的函数如何知道要作用于哪个对象？这就是`this`的作用。

在语法上，方法调用是一个使用`.`*点*和()`*调用*或`[]*下标*和`()`*调用*的三元运算。三元表达式中的三个子表达式是：

- 关注的对象。
- 方法名。
- 参数列表。

将在对象及其原型链中搜索命名的方法。如果找不到函数，则会引发异常。这是一件非常好的事情。这鼓励使用多态。你不应该关心对象的血统。你应该只关心它的能力。如果对象缺乏这种能力，它就会引发异常。如果对象有这种能力，我们就使用它，而不关心它是如何获得的。

如果找到一个函数，则使用参数列表调用它。该函数还接收`this`作为隐式参数，绑定到关注的对象。

如果一个方法包含一个内部函数，内部函数无法访问`this`，因为内部函数是作为函数调用的，只有方法调用才获得`this`绑定。

```
old_object.bud = function bud() {
    const that = this;

// lou 看不到 bud 的 this，但可以看到 bud 的 that。

    function lou() {
        do_it_to(that);
    }
    lou();
};
```

`this`绑定仅对方法调用有效，因此

```
new_object.bud();
```

成功，但

```
const funky = new_object.bud;
funky();
```

失败。这里`funky`包含与`new_object.bud`相同的函数引用，但`funky`是作为函数调用的，所以没有`this`绑定。

`this`还有其特殊性，即它是动态绑定的。所有其他变量都是静态绑定的。这是混淆的一个来源。

```
function pubsub() {

// pubsub 工厂创建一个发布/订阅对象。获得该对象访问权限的代码可以订阅
// 一个接收发布的函数，并可以发布将被传递给所有订阅者的内容。

// subscribers 数组用于保存订阅者函数。它通过 pubsub 函数的作用域对
// 外部隐藏。

    const subscribers = [];
    return {
        subscribe: function (subscriber) {
            subscribers.push(subscriber);
        },
        publish: function (publication) {
```



# 第17章

## 无类之道

*你自以为聪明绝顶，超然物外，无拘无束*

*——约翰·列侬*

面向对象编程发展中的一个关键洞见，是程序各部分如何相互通信的模型。可以将方法名及其参数看作一条消息。调用方法即是将这条消息发送给对象。每个对象都有自己特定的行为，在收到特定消息时触发。发送者假定接收者知道如何处理这条消息。

由此衍生出的一个概念是多态性。任何识别特定消息的对象，都有资格接收该消息。接下来发生什么取决于对象的具体类型。这是一个非常强大的思想。

不幸的是，我们被继承分散了注意力。继承是一种强大的代码复用模式。代码复用很重要，因为它可以减少开发程序所需的工作量。继承建立在“相同但有例外”的思想之上。我们可以说，某个对象或某类对象与另一个对象或另一类对象是相同的，除了一些重要的差异。当情况简单时，这非常有效。需要记住的是，现代面向对象编程始于Smalltalk，一种面向儿童的编程语言。随着情况变得复杂，继承会引发问题。继承导致类之间的紧密耦合。一个类的更改可能导致依赖类失效。类往往不是好的模块。

我们也看到过多的关注放在了属性上，而不是对象上。过度强调每个独立属性的getter和setter方法，或者在最糟糕的设计中，属性是公开的，可以在对象不知情的情况下被修改。确实有可能实现良好的设计，即属性被隐藏，方法处理事务而不仅仅是属性变更，但这并不常见。

对类型也存在过度依赖。类型是FORTRAN及后续语言的一个特性，对编译器编写者来说是一种便利。此后，关于类型的神话逐渐形成，夸大其词地宣称类型可以保护程序免于错误。尽管对类型如此执着，错误仍然每天都在发生。

类型因早期被编译器发现的缺陷而获得赞誉，也理应如此。缺陷发现得越早，成本就越低。但如果程序经过了适当的测试，所有这些缺陷都会很快被发现。因此，类型所识别的缺陷是那些价值较低的缺陷。

对于那些未能发现的、代价高昂的缺陷，类型并未受到指责。类型也没有因为它们要求绕开限制而引起的问题受到指责。类型可能诱导我们采用晦涩、复杂且可疑的编码实践。

类型就像减肥节食。节食因减轻的体重而受到赞扬。当体重反弹甚至增加时，节食不会受到指责。节食也不会因为它造成的痛苦或健康问题而受到指责。节食给了我们一种信念，即我们可以达到健康体重，同时仍然可以吃不健康的食物。

经典的继承让我们以为自己在编写好的程序，而实际上却在制造更多的缺陷和杂乱无章的遗留代码。如果你忽略负面影响，类型看起来像是一个巨大的胜利。好处是真实的。但如果你系统地审视类型，其成本就超过了收益。

### 17.1 无类之道

在第13章中，我们使用了工厂（返回函数的函数）。现在我们可以用构造器（返回包含函数的对象的函数）做类似的事情。

我们首先创建一个类似于计数器生成器的counter_constructor。它有两个方法：up和down。

```
function counter_constructor() {
    let counter = 0;

    function up() {
        counter += 1;
        return counter;
    }

    function down() {
        counter -= 1;
        return counter;
    }

    return Object.freeze({
        up,
        down
    });
}
```

返回的对象是冻结的。对象不能被损坏或破坏。对象具有状态。counter变量是对象的私有属性。它只能通过方法访问。而且我们不必使用this。

订阅者函数获得一个绑定到**subscribers**数组的this，因为

```
subscribers[i](publication);
```

是一个方法调用。它可能看起来不像方法调用，但它确实是。它让每个订阅者函数都能访问**subscribers**数组，这可能允许订阅者做一些非常糟糕的事情，比如删除所有其他订阅者或拦截或篡改他们的消息。

```
my_pubsub.subscribe(function (publication) {
    this.length = 0;
});
```

**this**可能是一个安全性和可靠性隐患。当一个函数被存储到数组中并稍后调用时，它获得的**this**会绑定到该数组上。如果我们不打算让函数访问数组（通常我们确实不希望如此），那么事情就可能出现新的差错。

**publish**函数可以通过将**for**替换为**forEach**来修复。

```
publish: function (publication) {
    subscribers.forEach(function (subscriber) {
        subscriber(publication);
    }
}
```

所有变量都是静态绑定的，这很好。只有**this**是动态绑定的，这意味着决定其绑定的是函数的调用者，而不是函数的创建者。这种偏离是混淆的根源。

函数对象有两个原型属性。它有一个指向**Function.prototype**的委托链接。它还包含一个**prototype**属性，该属性包含一个对象的引用，该对象被用作当使用**new**前缀调用该函数时，由该函数构造的对象的原型。

构造器调用通过在函数调用前放置**new**前缀来书写。**new**前缀的作用如下：

- 使用`Object.create(function.prototype)`创建一个**this**值。
- 用**this**绑定到新对象来调用*函数*。
- 如果*函数*没有返回一个对象，则强制其返回**this**。

通过使用**Object.assign**函数将方法从一个原型复制到另一个原型，可以实现一种继承。更常见的做法是用另一个构造器构造的对象替换函数对象的**prototype**属性。

由于每个函数都是潜在的构造器，因此很难在任何时刻知道一个调用是否应该使用**new**前缀。更糟糕的是，当需要但忘记使用时，没有任何警告。

这就是为什么我们有一个约定：打算用`new`前缀作为构造器调用的函数，其名称必须以大写字母开头。其他任何东西都不应该以大写字母开头。

JavaScript还有看起来更传统的`class`语法，它是专门为那些不知道也永远不会知道JavaScript如何工作的开发者设计的。它允许从更次的语言转移技能，无需新的学习。

`class`语法，尽管外表如此，并没有实现类。它只是伪经典构造器怪异行为之上的语法糖。它保留了经典模型中最糟糕的部分——`extends`，它将类紧密耦合在一起。这种紧密耦合导致脆弱性和有缺陷的设计。

## 无This之道

2007年，有几个研究项目试图开发JavaScript的安全子集。最大的问题之一是`this`的管理。在方法调用中，`this`绑定到相关对象，这有时是件好事。但如果同一个函数对象被作为函数调用，那么`this`可能会绑定到全局对象，这非常糟糕。

我对这个问题的解决方案是完全禁止`this`。我的论点是`this`是有问题的且不必要的。如果我们从语言中移除`this`，该语言仍然是图灵完备的。因此，我开始用一种无`this`的方言编程，以了解放弃`this`会有多痛苦。

我非常惊讶地发现，它更容易了，而不是更难，我的程序也更小、更好了。

这就是为什么我建议消除`this`。如果你能学会在没有`this`的情况下工作，你会成为一个更好、更快乐的程序员。我并没有夺走你的任何东西。我是为你提供一种通过编写更好的程序来生活得更好的方式。

使用`class`的程序员至死都不会知道他们曾经多么痛苦。

`this`不是个好东西。

**This**是一个指示代词。仅仅在语言中存在`this`就使得语言更难讨论。这就像是和艾博特与科斯特洛一起结对编程。

### 构造器

在第13章中，我们使用了工厂（返回函数的函数）。现在我们可以用构造器（返回包含函数的对象的函数）做类似的事情。

我们首先创建一个类似于计数器生成器的counter_constructor。它有两个方法：up和down。

```
function counter_constructor() {
    let counter = 0;

    function up() {
        counter += 1;
        return counter;
    }

    function down() {
        counter -= 1;
        return counter;
    }

    return Object.freeze({
        up,
        down
    });
}
```

返回的对象是冻结的。对象不能被损坏或破坏。对象具有状态。counter变量是对象的私有属性。它只能通过方法访问。而且我们不必使用this。



### 构造函数参数

加入冻结对象中的方法是公共方法。

方法应该实现事务性操作。例如，假设我们有一个人员对象。我们可能希望支持更改人员的地址。我们不应该通过为地址中的每个单独项目设置单独的函数来完成此操作。相反，我们应该有一个单一的方法，该方法接受一个对象字面量，可以描述地址中所有需要更改的部分。

JavaScript 中的一个巧妙想法是对象字面量。它是一种愉快且富有表现力的语法，用于将信息分组在一起。通过让方法消费和产生数据对象，我们可以减少方法的数量，增加对象的完整性。

因此，我们有两种类型的对象：

- 只包含方法的硬对象。这些对象保护闭包中所持有的数据的完整性。它们为我们提供了多态性和封装性。
- 只包含数据的软数据对象。这些对象没有行为。它们只是可以被函数操作的便捷集合。

对面向对象编程的一种观点是，我们从为 COBOL 记录添加过程以提供行为开始。我认为方法和数据属性的混合是一个重要的进步，但它不应该是最后一步。

如果硬对象需要被字符串化，你应该包含一个 `toJSON` 方法。否则，`JSON.stringify` 会将其视为空对象，忽略方法和隐藏的数据（第 22 章）。

我曾经写过一个接受十个参数的构造函数。它非常难以使用，因为没有人能记住顺序。后来我们注意到没有人很好地使用第二个参数。我想从参数列表中删除它，但这会破坏我们已经开发的所有代码。

如果我当时聪明的话，我本应该让构造函数接受一个对象作为其参数。这个对象通常来自对象字面量，但它也可能来自其他来源，例如 JSON 载荷。

这将带来许多好处：

- 键字符串使代码具有自文档性。阅读代码更容易，因为代码告诉你调用点处每个参数是什么。
- 参数可以以任何顺序出现。
- 未来可以添加新参数而不会破坏现有代码。
- 过时的参数可以被忽略。

参数最常见的用途是初始化私有属性。我们可以这样做。

```javascript
function my_little_constructor(spec) {
    let {
        name, mana_cost, colors, type, supertypes, types, subtypes, text,
        flavor, power, toughness, loyalty, timeshifted, hand, life
    } = spec;
}
```

这使用来自 `spec` 的同名属性创建并初始化了 15 个私有变量。如果 `spec` 不包含匹配的属性，那么新变量将用 `undefined` 初始化。这给了我们用默认值填充缺失值的能力。

### 组合

JavaScript 的表达能力非常强大，你可以用经典的范式编写代码，尽管它不是一门经典语言。JavaScript 还让我们可以做一些更好的事情。我们可以使用函数式组合。因此，我们可以从“除了相同之外”变为“有一点这个，有一点那个”。这是构造函数的一般形式：

```javascript
function my_little_constructor(spec) {
    let {member} = spec;
    const reuse = other_constructor(spec);
    const method = function () {
        // 它可以使用 spec, member, reuse, method
    };
    return Object.freeze({
        method,
        goodness: reuse.goodness
    });
}
```

你的构造函数可以根据需要调用任意数量的其他构造函数，以访问它们提供的状态管理和行为。我们甚至可以将相同的 **spec** 对象传递给它们。当我们记录 **spec** 参数时，我们列出 **my_little_constructor** 需要的属性，以及其他构造函数需要的属性。

在某些情况下，我们可以简单地将我们获得的一些方法添加到冻结对象中。在其他情况下，我们的新方法会调用获得的方法。这实现了类似于继承的代码重用，但没有紧耦合。调用函数是原始的代码重用模式，并且它仍然是最好的。

### 规模

这种对象构造方法比基于原型的方法使用更多的内存，因为每个硬对象都包含对象的所有方法，而原型对象包含一个对包含方法的原型的引用。内存消耗的差异显著吗？不，相对于内存容量的近期改进来说，这并不显著。我们过去以千字节计算内存。我们现在以千字节计算内存。这个差异在噪声之中。

通过模块化的改进，这些差异可以得到缓解。强调事务而非属性倾向于减少方法的数量，同时提高内聚性。

经典模型是一种一刀切的模型。每个对象都必须是类的实例。JavaScript 将我们从这种限制中解放出来。并非所有的对象都需要硬性。

例如，我认为点必须是具有方法的硬对象没有意义。点可以只是两个或三个数字的简单容器。点被传递给可以进行投影、插值或我们对点进行任何操作的函数。这比将点子类化以赋予其特定行为要高效得多。让函数去做这些工作。

# 第 18 章

## 尾调用的工作原理

> 在人生的事务中，总有那么一个时刻，他必须抓住牛的尾巴，面对现实。
> *W. C. Fields*

我们依赖系统中的优化来使程序运行得更快。优化是对规则的破坏，但以一种破坏不可观察的方式进行。优化不允许将好的程序变成坏的。优化不允许引入 bug。

最重要的优化不仅不会引入新的 bug，它还会从好的程序中消除一类 bug，从而实现新的编程范式。我谈论的是*尾调用优化*。一些专家认为这个优化非常重要，我们不应该轻描淡写地称之为优化。他们称之为*正规尾调用*。任何其他实现尾调用的方式都是不正规的。

我更愿意称它为优化，因为大多数程序员对正规性并不重视，但即使没有实际效果，他们也喜欢优化。我希望他们想要这个特性。

当一个函数执行的最后一件事是返回调用另一个函数的结果时，就发生了尾调用。在下面的例子中，`continuize` 是一个工厂函数，它接受任何类型的函数并返回一个 `hero` 函数。`hero` 调用 `any`，并将返回值传递给 `continuation` 函数。

```javascript
function continuize(any) {
    return function hero(continuation, ...args) {
        return continuation(any(...args));    // <-- 一个尾调用
    };
}
```

当一个函数返回调用另一个函数的结果时，我们称该调用为*尾调用*。很遗憾我们称该调用为*尾调用*而不是*返回调用*。

尾调用优化很简单，但它有重大影响。使用传统指令集作为隐喻，为 `continuize` 生成的代码可能包含以下机器指令：

```assembly
call    continuation    # 调用 continuation 函数
return                    # 返回到调用 hero 的函数
```

**call** 指令将下一条指令的地址（在这种情况下恰好是 **return** 指令）压入调用栈。然后它将控制权转移到寄存器中标记为 **continuation** 的地址所在的函数。当 **continuation** 函数完成时，它从栈中弹出 **return** 的地址并跳转到该地址。**return** 指令将再次弹出栈并跳转到调用 `hero` 的指令之后的指令。

该优化将这两条指令替换为一条指令：

```assembly
jump    continuation    # 跳转到 continuation 函数
```

现在我们不再将 **return** 指令的地址压入调用栈。**continuation** 函数返回到调用 `hero` 的函数，而不是 `hero` 本身。尾调用就像一个带参数的 `goto`，但没有导致 `goto` 被消除的那些危险。

因此，优化节省了一条指令、一次压栈和一次出栈。这似乎不是什么大事。为了更好地理解好处，让我们看看 JavaScript 中函数调用实际上是如何工作的。当你调用一个函数时，会发生以下事情：

- 计算参数表达式。
- 创建一个足够大的活动对象，以容纳函数的所有参数和变量。
- 在新的活动对象中存储对正在调用的函数对象的引用。
- 将参数的值存储到新活动对象的参数中。缺失的参数被视为 `undefined`。多余的参数被忽略。
- 将 `undefined` 存储到新活动对象的所有变量中。
- 设置活动对象中的 `next instruction` 字段，以指示 **call** 之后的指令。
- 将新活动对象中的 `caller` 字段设置为当前活动对象。实际上没有调用栈。取而代之的是一个活动对象的链表。
- 使新活动对象成为当前活动对象。
- 开始执行被调用的函数。

优化的工作方式略有不同。

- 计算参数表达式。
- 如果当前活动对象足够大，
  - 使用当前活动对象作为新的活动对象。
  否则，
  - 创建一个足够大的活动对象，以容纳函数的所有参数和变量。
  - 将 `caller` 字段从当前活动对象复制到新的活动对象。
  - 使新的活动对象成为当前活动对象。
- 在新的活动对象中存储对正在调用的函数对象的引用。



 +   将参数的值存储到新激活对象的形参中。缺失的参数将视为 undefined。多余的参数将被忽略。
+   将 undefined 存储到新激活对象的所有变量中。
+   开始执行被调用的函数。

重要的区别在于，如果激活对象足够大（通常确实如此），那么我们就不需要再分配另一个。我们现在可以重用当前的激活对象。调用栈链不会太长，通常只有几百的量级，所以当尾调用即将发生时，实现始终分配单个最大尺寸的激活对象是合理的。内存分配和垃圾回收时间的减少可能非常显著。但还有更多好处。

有了尾调用优化，递归函数可以变得和循环一样快。从函数式编程的角度来看，这一点很重要，因为循环本质上是不纯的。纯净性来自递归。有了这种优化，反对递归的性能论点就不复存在了。

这是一般循环的结构。

```
while (true) {
    do some stuff
    if (done) {
        break;
    }
    do more stuff
}
```

尾递归函数可能是这样的

```
(function loop() {
    do some stuff
    if (done) {
        return;
    }
    do more stuff
    return loop(); // <-- tail call
})();
```

这展示了循环和递归函数之间的对应关系。递归函数通常会更优雅，通过在参数和返回值中传递更新的状态，而不是使用赋值。

我们现在可以让递归进行到任意深度，而不必担心内存耗尽或人为的栈溢出错误。因此，良好的递归函数现在可以正常工作了。恰当的尾调用不是一项特性，它是一个 bug 修复。标准要求实现这种优化，因为它对于防止优秀程序失败至关重要。

### 尾调用如何工作

#### 尾位置

如果一个调用返回了函数返回的值，那么它就是尾调用。所以

```
return (
    typeof any === "function"
    ? any()
    : undefined
);                                       // <-- tail call
```

是尾调用。由 && *逻辑与* 和 || *逻辑或* 构成的返回表达式也可以是尾调用，但

```
return 1 + any();                       // <-- not a tail call
```

不是尾调用。该函数最后做的是返回一个加法的结果。

```
any();                                  // <-- not a tail call
return;
```

这不是尾调用，因为它返回的是 undefined，而不是函数的返回值。

```
const value = any();                    // <-- not a tail call
return value;
```

这也不是尾调用，因为它返回的是 value 的内容。我们知道 value 的值是 any() 的结果，但该调用不在尾位置。

一般来说，递归不是尾调用。

```
function factorial(n) {
    if (n < 2) {
        return 1;
    }
    return n * factorial(n - 1);         // <-- not a tail call
}
```

factorial 的递归调用不在尾位置，所以每次迭代都会生成一个激活记录，但我们可以将调用移到尾位置：

```
function factorial(n, result = 1) {
    if (n < 2) {
        return result;
    }
    return factorial(n - 1, n * result); // <-- tail call
}
```

这个版本将会被优化。递归调用不会生成激活对象。相反，它们会跳到函数的顶部。它使用参数而不是赋值来刷新参数。

返回一个新的函数对象不是尾调用……

```
return function () {};                  // <-- not a tail call
```

除非你立即调用这个新的函数对象。

```
return (function () {}());             // <-- tail call
```

#### 排除情况

有些情况下，必须取消优化以保护优秀程序免于出错。

try 块内部的尾调用无法被优化。该优化会通过不将此次调用的激活对象链接到调用栈中来节省时间和内存。但 try 可能会将控制权发送回此次调用的 catch，而为了使其发生，激活对象不能被优化掉。这是另一个避免滥用异常的好理由。

如果这个函数创建了一个带有任何自由变量的新函数对象，那么新函数对象必须能够访问其创建者的激活对象，因此该激活对象不能被优化掉。

#### 延续传递风格

在延续传递风格中，函数接受一个额外的 `continuation` 参数，这是一个接收结果的函数。本章开头的 continuize 工厂可以将任何函数转换为也接受 `continuation` 的函数。在这种风格中，`continuation` 是一个代表程序延续的函数。程序的流程总是向前推进，很少需要回到先前的状态。它是管理事件性的非常有效的工具。它在转译和其他应用中都有用途。只有在尾调用优化的情况下这才可能实现。

#### 调试

调用栈中激活的消除可能使调试更加困难，因为你不再能看到导致当前困境的所有步骤，但一个好的调试器可以通过提供一种模式来缓解这个问题，在该模式中，它复制每个激活对象的状态并始终保留一小组最近的激活对象。这不会干扰优化的好处，但仍允许检查传统的堆栈跟踪。

# 第 19 章 TMSymbole章

## 纯粹性如何工作

> 纯粹性的代价是纯粹主义者。
> Calvin Trillin

函数式编程被合理地定义为使用函数进行编程。不幸的是，这是一个模棱两可的定义。它可能意味着使用数学函数进行编程，数学函数将值的定义域映射到值的值域。或者它可能意味着使用软件函数进行编程，在大多数编程语言中，软件函数指的是参数化的语句串。

数学函数被认为比软件函数更纯。纯粹性会被突变破坏。纯函数不会引起突变。纯函数不受突变的影响。纯函数的结果仅由其输入决定。它除了提供输出外不执行任何操作。给定的输入总是产生相同的输出。

另一方面，JavaScript 似乎是在庆祝突变。赋值运算符是主要的突变工具，而 JavaScript 有 15 种，如果把 dreaded 的 ++ 和 -- 各算两次的话（你应该这样做），那就是 17 种：

```
= assignment
+= add assignment
 ansi subtract assignment
*= multiply assignment
/= divide assignment
%= remainder assignment
**= exponentiation assignment
>>>= shift right assignment
>>= shift right sign extended assignment
<<= shift left assignment
&= bitwise and assignment
|= bitwise or assignment
^= bitwise xor assignment
++ pre-increment
++ post-increment
-- pre-decrement
-- post-decrement
```

像大多数主流语言一样，JavaScript 喜欢混乱，宁愿选择突变而非清晰。JavaScript 选择将 *等号* 赋予突变（不纯），而非相等（纯粹）。

### 纯粹性的好处

纯粹性伴随着一些宝贵的优点。

纯粹性通常意味着出色的模块化。纯函数具有极强的内聚性。函数中的一切都是为了帮助提供单一的结果。没有副作用会削弱内聚性。纯函数具有极低的耦合度。纯函数仅依赖于其输入。制作好的模块可能非常困难，但有了纯粹性，良好的模块化是自然而然的。

纯函数可以更容易测试。由于它们只依赖于参数，因此不需要模拟、伪造或存根。一旦我们看到纯函数从输入返回正确的输出，我们就知道环境中的任何突变都不会使纯函数返回任何其他值。那些在你关闭电源再打开后就消失的 bug 都是由于不纯造成的。

纯函数非常可组合。由于它们没有副作用，也没有外部依赖或影响，因此很容易将它们组装成更大、更复杂的函数，这些函数也可以是纯粹和可组合的。

有一天，纯粹性将带来巨大的性能提升。纯粹性为解决线程困扰的可靠性和性能问题提供了极佳的方案。在多线程系统中，如果两个线程同时尝试访问同一段内存，那么可能会发生竞争，导致数据损坏或系统故障。这种竞争可能非常难以诊断。互斥可以缓解竞争，但它也可能导致延迟、死锁和系统故障。

纯函数可以使线程安全且高效。由于纯函数不会引起突变，内存共享不会产生风险。一个数组的 map 方法，如果给定纯函数，可以将数组的元素分发到所有可用的核心上。计算可以非常快速地进行。性能提升可能是线性的。核心越多，速度越快。有一大类程序可以从中显著受益。

总是有很多愚蠢的功能被考虑纳入 JavaScript。很多都被纳入了。它们都是干扰。纯函数的并行化才是我们需要的。

#### 变得纯粹

纯粹性显然带来了巨大的好处。那么我们能为语言添加纯粹性吗？不能。纯粹性不是可以添加的特性。它就像可靠性和安全性一样。我们无法为系统添加可靠性。相反，我们必须消除不可靠性。我们无法添加安全性。我们必须消除不安全性。我们无法添加纯粹性。我们必须消除不纯之物。不纯之物是偏离函数数学模型的腐败。

ECMA 无力从 JavaScript 中移除坏的部分，这就是为什么坏的部分数量不断增加，但 *你* 可以简单地停止使用坏的东西。我们可以通过在这个过程中引入更多的纪律来使语言对我们自己而言变得纯粹。如果我们决定从不使用不纯的特性，那么该特性就无法再消耗和玷污我们函数体的本质。

因此，让我们快速调查一下语言中的不纯之处。



显然，我们必须清除所有赋值运算符，以及 `var` 和 `let` 语句。我们可以保留 `const` 语句。它创建并初始化一个变量，但不允许其被修改。

我们必须移除修改对象的运算符和方法，包括 `delete` 运算符和像 `Object.assign` 这样的方法。我们也必须移除数组的修改方法，比如 `splice` 和 `sort`。数组的 `sort` 方法本可以成为一个纯函数，但它的实现修改了原始数组，所以也得移除。

我们必须移除 getter 和 setter。setter 显然是修改状态的工具，而且两者都是为了产生副作用而存在的。所有副作用都是对纯函数的污染，必须消除。

`RegExp` 的 `exec` 方法会修改 `lastIndex` 属性，所以也得移除。它本来可以被设计得更好，但事实并非如此。

`for` 语句的目的是修改循环变量，所以它必须被移除。我们同样应该移除 `while` 和 `do`。尾递归是最纯粹的迭代形式。

我们必须移除 `Date` 构造函数。每次调用它，我们都会得到一个不同的值。这并非纯函数。我们也应该移除 `Math.random`。你永远无法预知它会给你什么值。

我们必须移除用户。与人类的每一次交互都可能返回不同的结果。人类并非纯粹。

最后，我们必须移除网络。Lambda 演算无法表达存在于一台机器上而另一台机器上没有的信息。同样，通用图灵机也没有 WiFi 连接。

## 宇宙的问题

宇宙并不纯粹。宇宙是最终的、完全分布式的，并且高度并行的。我们的编程模型应该拥抱这一事实。如果我们的程序要与宇宙交互，特别是与宇宙中的人类代理交互，那么我们程序的某些部分可能不得不变得不纯。

我们应该尽量使我们的程序尽可能纯粹，因为纯粹性带来的好处是实实在在的。即使对象有状态，它们仍然是有价值的；而状态只有在可变时才有意义。我们应该设计我们的对象，使其状态的改变受到严格约束和紧密控制。

## 连续统

如果纯粹性是二元的（一个函数要么纯粹要么不纯），那么它会更容易理解。不幸的是，事情比这更复杂。我们可以从多个角度来思考纯粹性。

修改是不纯的，但归根结底，即使是最纯粹的系统在底层也存在一些不纯性。一个函数式系统总是在创建新的激活对象，而将对象从可用内存移动到活动内存再移回的操作需要修改。这并非坏事。通常，我们希望尽可能多的东西是纯粹的，而不纯粹的东西应该被隐藏起来。

第13章的生成器和第17章的对象很好地隐藏了它们的状态。外部代码只能通过生成器函数和方法施加的约束来改变状态。生成器和对象不能被外部赋值修改。它们并非完全纯粹，但相对于其他面向对象编程模式，它们是一个显著的改进。它们是我们如何管理纯粹性边界的例子。

纯粹性的一个定义是远离赋值和其他修改操作。那么下面这段代码是纯粹的吗？

```
function repeat(generator) {
    if (generator() !== undefined) {
        return repeat(generator);
    }
}
```

`repeat` 函数接收一个生成器函数并调用它，直到它返回 `undefined`。它的体是纯粹的，但精神上并非如此。它自身没有执行不纯的行为，但它促成了生成器的不纯性。许多高阶函数都处于这种中间地带。

一个函数可能执行赋值操作但仍然被认为是纯粹的。如果一个函数声明了局部变量，并使用循环和赋值来修改这些变量，它看起来可能是不纯的。但我们可以将这样的函数交给并行的 `map` 函数，它依然能正常工作。它在精神上是纯粹的，但在形式上并非如此。把它看作一个黑盒子，它是纯粹的。只有当我们观察其内部时，它才是不纯的。

因此，存在一个纯粹性的连续统：顶端是数学函数，然后是足够纯粹以用于并行应用的函数，接着是纯粹的高阶函数，然后是带有状态的高阶函数，最后是那些污染了网络的大量“垃圾”代码：经典的、过程式的，以及最底层的所有使用全局变量的代码。

# 第20章
## 事件驱动式编程如何工作

### 莫！拉里！奶酪！
*杰罗姆·莱斯特·霍维茨*

起初是*顺序式*编程。最早的计算机只是自动计算器。你向计算机输入一些数据和一个例程，它就会一条接一条地执行指令，直到产生结果并停止。这种一次一条指令的执行模型在计算和批量数据处理方面效果良好。

最早的编程语言是在顺序时代开发的。那些语言的影响力如此之大，以至于大多数现代语言仍然牢固地扎根于顺序范式。旧的范式没有预料到我们现在的程序所做的事情，使得现代系统的编程变得不必要地困难、不可靠和不安全。

顺序语言的一个典型特征是阻塞式输入和输出。当程序试图从文件或网络读取数据时，它会被阻塞，直到输入操作完成。这对 FORTRAN 是有意义的。当程序需要从读卡器中的卡片读取数据时，它会阻塞。在数据准备好之前，程序无事可做，因此阻塞不是问题。大多数现代语言仍然实现 FORTRAN 的 I/O 模型。JavaScript 则不然。JavaScript 的首要任务是与人交互，因此它倾向于采用更好的模型。JavaScript 在顺序模型方面不像大多数其他语言那样固执。

### 并发

当计算机开始与人交互，然后与其他计算机交互时，顺序模型就崩溃了。这需要*并发*编程，即同时处理多件事情的能力。

同质并发为同时发生许多相似操作提供支持。我们之前看到过接收纯函数的数组方法，同时处理数组的每一个元素，就是一个例子。

异质并发支持具有不同职责但作为一个团队协同工作的专业进程之间的合作。难点在于确保团队成员不会像“三个臭皮匠”（The Three Stooges）那样行事。这是一个真正值得担忧的问题。臭皮匠行为是糟糕架构的必然结果。奈克奈克（nyuck nyuck）。

### 线程

线程是最古老的异质并发机制之一，至今仍被广泛使用。线程是（真实或虚拟的）CPU，它们同时运行并共享相同的内存。线程在运行纯函数时效果很好。如果函数不是纯粹的，那么“臭皮匠”们就会出场。

在这里，我们看到两个线程，*莫*和*拉里*，共享一个*变量*。*莫*将*变量*加1，*拉里*将*变量*加2。如你所料，结果是3。

| *莫* | *拉里* | 变量 |
| :--- | :--- | :--- |
| | | 0 |
| variable += 1 | | 1 |
| | variable += 2 | 3 |

在这次试验中，*莫*先修改了变量。也有可能是*拉里*先修改。在这种特定情况下，谁赢得竞态并不重要，因为这些操作是可交换的。如果拉里使用 `*=`（星号等号）而不是 `+=`（加号等号），那么结果将取决于竞态。还有其他更成问题的结果。

在更底层观察这段代码，`+=`（加号等号）赋值语句可以被编译成三条简单的机器指令：加载、相加和存储。

| *莫* | *拉里* | 变量 |
| :--- | :--- | :--- |
| | | 0 |
| 加载 variable | | 0 |
| 加 1 | 加载 variable | 0 |
| 存储 variable | 加 2 | 1 |
| | 存储 variable | 2 |

这展示了一个读取-修改-写入的竞态条件。*莫*和*拉里*都在*变量*的状态为0时获取了它。他们都对自己获取的值进行相加，然后都存储他们的和。这一次，*莫*的修改被覆盖了。下一次，*拉里*的修改被覆盖了。也许大多数时候，*莫*和*拉里*并不会获取相同的值，所以代码通常能正确运行。

这段代码有可能正确运行，但也有可能出错。在这两个极其简单的单行程序中，很难发现潜在的错误。在复杂的程序中，这些错误可以隐藏得非常好。

计算负载会改变指令的交错顺序。这段代码在开发和测试期间可能运行正确，但在生产环境中失败。或者它可能全年运行良好，然后在十二月失败。线程中的时序错误是所有错误中最糟糕、代价最高的。当程序的行为可能受到宇宙随机性的影响时，重现错误条件几乎不可能。类型检查无法发现它们。测试也无法发现它们。这些错误可能发生的频率非常低，这使得它们极其难以调试，或者难以确信修复没有使情况变得更糟。

线程竞态的危险可以通过互斥机制来缓解，互斥可以锁定内存的关键部分，阻止线程执行，从而防止在存在竞争时发生操作。锁的操作可能是计算密集的



代价高昂。可能存在某个线程被阻塞，无法释放其锁。这被称为*死锁*，另一种难以预防、复现或修复的故障模式。Java（以及许多类似语言）最大的设计错误在于，它无法决定自己究竟是系统语言还是应用语言。由于它试图兼顾两者，因此要求在应用中使用线程，这是不可原谅的。操作系统中的线程可能是必要的恶。应用中的线程则纯粹是恶。幸运的是，JavaScript 并不以这种方式使用线程。有更好的方法来实现并发。

## 终态编程（Eventual Programming）

*终态函数*（eventual function）是一种立即返回的函数，可能在它所请求的工作完成之前就已经返回。结果将在将来通过回调函数或消息发送的方式最终传达，而不是作为即时的返回值。

终态性提供了一种管理大量活动的方法，而无需将应用暴露给线程。事实上，有些系统拥有应用线程，却依赖终态性来管理其用户界面，只因这是处理随时间推移的事件的更简单、更可靠的方式。终态编程建立在两个理念之上：回调函数和处理循环。

回调函数是一种在将来发生有趣事件时将被调用的函数，例如：

- 消息已到达。
- 某项工作已完成。
- 人类与程序进行了交互。
- 传感器观察到了某物。
- 时间已流逝。
- 某处发生了错误。

回调函数被传递给一个正在启动或监控某项活动的函数。在更原始的系统中，回调函数被附加到一个代表活动的对象上。在网页浏览器中，可以通过将回调函数赋给 DOM 节点的特定属性来附加回调函数……

```
my_little_dom_node.onclick = callback function;
```

或者通过调用对象上的事件注册方法。

```
my_little_dom_node.addEventListener("click", callback function, false);
```

两种形式都有效。当用户点击特定的 DOM 节点时，*回调函数*（又称*事件处理程序*）被调用，很可能执行一些有用的操作来响应事件。

终态编程中的另一个理念是处理循环，也称为事件循环或消息循环。处理循环从队列中取出优先级最高的事件或消息，并调用注册接收该事件或消息的回调函数。回调函数运行至完成。回调函数无需操心内存锁或互斥。回调函数不会被中断，因此没有竞态条件的风险。当回调函数返回后，处理循环从队列中取出下一个项目，如此继续。这是一个非常可靠的编程模型。

处理循环维护一个队列，称为事件队列或消息队列，保存传入的事件或消息。事件或消息可以由回调函数作为其响应的一部分产生。更可能的是，事件或消息来自管理用户输入、网络、I/O 系统和进程间通信的辅助线程。与你的 JavaScript 程序运行的主线程通信的方式就是通过这个队列。互斥仅限于这一个接触点，因此终态系统往往非常高效和可靠。

这个模型的一个令人惊讶的好处是，网页浏览器中的 JavaScript 程序具有显著的韧性。当你打开调试器然后去浏览网页时，你会看到几乎恒定的异常和失败流。这可能是因为许多网页开发人员并不擅长他们的工作。然而，大多数功能似乎都能正常工作。

在有线程的系统中，如果一个线程发生异常，其栈会被展开。该线程现在可能相对于其他线程处于不一致的状态，这可能导致级联的线程故障。

JavaScript 使用单线程。其大部分关键状态都在其函数的闭包中，而不是在栈上。因此系统往往能继续运行。只要还有能用的按钮，用户仍然可以取得进展，对幕后发生的无数错误浑然不觉。

## 轮次法则（The Law of Turns）

处理循环的每次迭代称为一个*轮次*（turn），这源于国际象棋和扑克等游戏，在这些游戏中，任何时刻只允许一个玩家行棋。玩家走一步棋，走完以后，该玩家的轮次结束，而在游戏结束前，另一个玩家的轮次开始。

游戏有规则，终态模型也有规则：**轮次法则**。

> 永不等待。永不阻塞。快速完成。

**轮次法则**适用于处理循环调用的回调函数，以及它们直接或间接调用的每个函数。函数不允许在等待某事发生时循环。函数不允许阻塞主线程。在网页浏览器中，不允许使用`alert`等函数。在 Node.js 中，不允许使用名称含有臭名昭著的 -Sync 后缀的函数。不允许函数花费很长时间来完成其工作。

违反**轮次法则**会将高性能的终态系统变成极低性能的系统。违规不仅导致当前回调延迟，还会导致队列中的一切延迟。这些延迟会累积，可能导致队列越来越长。系统不再快速和响应灵敏。因此任何违规函数必须么被纠正，要么被隔离在单独的进程中。进程类似于不共享内存的线程。因此回调函数将某些工作发送给进程处理，该进程完成后再发送消息，这是合理的。消息进入队列并最终被传递。JavaScript 本身不知道进程的存在。进程是 JavaScript 运行所在系统可以提供的服务。进程是终态模型的重要组成部分，因此进程很可能成为下一门语言的一等特性。

## 服务端乐园的麻烦（Trouble In Serverland）

JavaScript 是为事件循环而创建的，它表现优异。不幸的是，消息循环一直是个更大的挑战。这是因为服务器所做工作的性质截然不同。在浏览器中，程序的大部分工作是响应 UI 事件。事件处理程序被调用，做一些工作，更新显示，然后结束。服务器的典型工作流要复杂得多。消息接收器或处理程序被调用，它可能需要与其他系统通信，这些系统可能位于其他机器上，然后才能传输其响应。有时它从一个系统获取的信息必须传达给另一个系统。这些操作可能形成长链。而与其他系统交互的结果将通过回调来传达。对此有一个优雅的编程解决方案，但首先让我们看看三个流行的错误。

第一个错误被称为*回调地狱*（Callback Hell）。这是一种模式，每个回调函数包含请求下一个工作单元的代码。该请求提供一个回调，该回调又请求另一个工作单元，如此往复。以这种方式编写的程序难以阅读、难以维护，而且脆弱。

第二个错误被称为*Promise*。在其原始形式中，Promise 是出色的。它们被创造出来是为了支持安全、分布式程序的开发。不幸的是，当 Promise 迁移到 JavaScript 时，它们失去了所有新范式特性。剩下的只有 awkward 的控制流机制。Promise 并非为管理本地控制流而设计，这就是为什么它们在这方面做得不好。它们相对于回调地狱无疑是改进，但还不够令人满意。

第三个错误被称为*Async Await*。这是一对关键词，用于装饰普通的顺序代码，并神奇地将其转化为终态代码。它与 ES6 生成器类似，即你写的代码与你得到的代码截然不同。值得肯定的是，它掩盖了 Promise 的诸多不足。async await 最受欢迎之处在于，你可以继续用旧范式的风格来书写。这也是它最大的问题所在。新范式很重要。理解新范式可能很困难，因为它很新，但这就是我们取得进步的方式。Async await 给了我们一种方式，可以在实际上没有进步的情况下保持生产效率。它的用户正在编写他们自己不完全理解的代码。这从来不是件好事。一个日益严重的问题是，编程人员正在到处放置`async`和`await`装饰器。因为他们不理解

无论它们做什么，它们都不懂得如何善用它们。我们不应该试图否认或掩盖下一个范式。我们应该拥抱它。

这三个错误的共同点是逻辑与控制流程的紧密耦合。这会导致内聚性差，因为太多不同的活动被粘贴在一起。最好将它们分开。

## 请求器（Requestors）

我们应该进行模块化设计。每个工作单元，无论是向某个服务器或数据库发出请求，还是启动一个进程，都应该是独立的函数。一个只执行工作单元的函数具有很强的内聚性。这些函数还以回调函数作为第一个参数。当工作单元完成时，结果会传递给回调。这减少了对其他代码的依赖，实现了松耦合。这是一种良好的模块化设计实践，有助于我们在新范式中工作。

我们使用*请求器（requestor）*一词来描述一个接受回调并执行可能在未来某次轮转才能完成的工作单元的函数。

```
function my_little_requestor(callback, value)
```

*回调（callback）*函数有两个参数：*value*和*reason*。*value*是请求器的结果，如果请求器失败则为*undefined*。可选的*reason*可用于记录失败原因。

```
function my_little_callback(value, reason)
```

请求器函数可以选择性地返回一个取消函数。该函数可以在任何原因下被调用来取消工作。这不是撤销。它仅用于停止不必要的工作。因此，如果一个请求器在另一台服务器上启动了一个昂贵的操作，而不再需要该操作，那么调用请求器的取消函数可能会向服务器发送一个停止消息。

```
function my_little_cancel(reason)
```

## 请求器工厂（Requestor Factories）

你的大部分工作都是创建接受参数并返回请求器的工厂。这个工厂是一个简单的包装器，可以接受任何单参数函数并返回请求器。

```
function requestorize(unary) {
    return function requestor(callback, value) {
        try {
            return callback(unary(value));
        } catch (exception) {
            return callback(undefined, exception);
        }
    };
}
```

```
    encoding,
    function (err, data) {
        return (
            err
            ? callback(undefined, err)
            : callback(data)
        );
    }
);
    };
}
```

最有趣的工厂创建与其他服务在可能跨越多次轮转的对话中通信的请求器。它们可以采用这种形式：

```
function factory(service_address, arguments) {

// 工厂函数返回一个可以执行工作单元的请求器函数。

    return function requestor(callback, value) {

// 它在'try'块中启动工作，以防向工作人员服务发送消息的函数失败。

        try {

// 当请求器函数被调用时，它向服务发送消息，告诉它开始工作。
// 当获得结果时，它将通过'callback'函数传递。在这个例子中，
// 我们假设消息系统将使用'(result, exception)'约定来发送其结果。

            send_message(
                callback,
                service_address,
                start,
                value,
                arguments
            );
        } catch (exception) {

// 如果捕获到异常，我们发出失败信号。

            return callback(undefined, exception);
        }

// 我们可以返回一个'cancel'函数，当不再需要结果时尝试取消请求。

        return function cancel(reason) {
            return send_message(
                undefined,
                service_address,
                stop,
                reason
            );
        };
    };
}
```

## Parseq

我开发了 Parseq 库来管理请求器函数之间的流程。Parseq 工厂将数组形式的请求器函数与控制流程打包在一起：并行（parallel）、序列（sequence）、回退（fallback）或竞赛（race）。每个工厂返回一个新的请求器。这使得请求器高度可组合。

Parseq 库可以处理时间限制。可能有些工作必须在 100 毫秒内完成。如果超时，我们应该将工作视为失败并转向备选响应。使用三种错误中的任何一种都很难做到这一点。使用 Parseq，您只需指定以毫秒为单位的时间限制。

```
parseq.sequence(
    requestor_array,
    milliseconds
)
```

序列工厂接受一个请求器函数数组和一个可选的时间限制，并返回一个请求器，使数组中的每个请求器依次被调用。传递给新请求器的值被传递给数组中的第零个请求器。它产生的值传递给第一个请求器。这样，值从请求器流向请求器。最后一个请求器的结果就是序列的结果。

```
parseq.parallel(
    required_array,
    optional_array,
    milliseconds,
    time_option,
    throttle
)
```

并行工厂同时启动其所有请求器。它不会为 JavaScript 添加并行性。相反，它允许 JavaScript 利用宇宙的自然并行性。这允许将计算负载分散到多台服务器上。这可以提供巨大的性能优势。如果我们并行处理所有请求器，所花费的时间是最慢请求器的时间，而不是所有请求器的总时间。这是一个重要的优化。

并行工厂应仅当请求器之间没有相互依赖时才使用。所有请求器都被赋予相同的值。结果是一个包含所有请求器结果的数组。在这方面，它类似于数组的 map 方法。

并行工厂可以接受两个请求器数组。第一个数组包含必需的请求器。所有必需请求器必须成功完成，并行操作才算成功。第二个数组包含可选的请求器。它们可以失败而不会导致并行操作失败。

可以提供以毫秒为单位的时间限制。它决定必需请求器完成工作的时间。time_option 参数决定了时间限制对可选请求器的影响。

| time_option | 效果 |
| :--- | :--- |
| undefined | 可选请求器必须在必需请求器完成之前完成。必需请求器必须在时间限制之前完成（如果有时间限制的话）。 |
| true | 必需请求器和可选请求器都必须在时间限制之前完成。 |
| false | 必需请求器没有时间限制。可选请求器必须在必需请求器完成和时间限制中较晚的一个之前完成。

默认情况下，所有请求器同时启动。不幸的是，这可能会压垮设计不良的系统。因此有一个可选的**节流阀（throttle）**，限制同时活动的请求器数量。

```
parseq.fallback(
    requestor_array,
    milliseconds
)
```

**回退（fallback）**工厂类似于**序列（sequence）**工厂，但当任何请求器有成功结果时它就成功。如果一个请求器失败，它就尝试下一个。如果每个请求器都失败，回退失败。

```
parseq.race(
    requestor_array,
    milliseconds,
    throttle
)
```

**竞赛（race）**工厂类似于**并行（parallel）**工厂，但它在第一个成功请求器结果时宣布成功。如果一个请求器成功，竞赛就成功。

```
let getWeather = parseq.fallback([
    fetch("weather", localCache),
    fetch("weather", localDB),
    fetch("weather", remoteDB)
]);

let getAds = parseq.race([
    getAd(adnet.klikHaus),
    getAd(adnet.inUFace),
    getAd(adnet.trackPipe)
]);
```

```
let getNav = parseq.sequence([
    getUserRecord,
    getPreference,
    getCustomNav
]);
```

```
let getStuff = parseq.parallel(
    [getNav, getAds, getMessageOfTheDay],
    [getWeather, getHoroscope, getGossip],
    500,
    true
);
```

### 异常（Exceptions）

异常太弱，无法处理跨越多次轮转发生的失败。异常可以展开堆栈，但堆栈中没有任何东西能从一次轮转存活到另一次轮转。异常没有力量向未来的某次轮转通信某次早期轮转中的失败，异常也不能穿越回失败请求的起源点。

工厂被允许抛出异常，因为工厂的调用者仍在堆栈上。请求器永远不允许抛出异常，因为堆栈上没有任何东西可以捕获它们。请求器绝不允许让游离的异常逃逸。所有异常必须被捕获并作为*reason*传递给*callback*函数。

### Parseq 实现

让我们看看 Parseq 的实现。它不是很大。它包含四个公共函数和四个私有函数。

第一个私有函数是`make_reason`。它创建一个错误对象。

```
function make_reason(factory_name, excuse, evidence) {
    const reason = new Error("parseq." + factory_name + (
        excuse === undefined
        ? ""
        : "; " + excuse
    ));
    reason.evidence = evidence;
    return reason;
}
```

回调是一个有两个参数的函数。

```
function check_callback(callback, factory_name) {
    if (typeof callback !== "function" || callback.length !== 2) {
        throw make_reason(factory_name, "Not a callback.", callback);
    }
}
```

确保数组中的所有元素都是请求器函数。



function check_requestor_array(requestor_array, factory_name) {
    // A requestor array contains only requestors. A requestor is a function that takes one or two arguments: callback and optionally initial_value.
    if (
        !Array.isArray(requestor_array)
        || requestor_array.length < 1
        || requestor_array.some(function (requestor) {
            return (
                typeof requestor !== "function"
                || requestor.length < 1
                || requestor.length > 2
            );
        })
    ) {
        throw make_reason(
            factory_name,
            "Bad requestors array.",
            requestor_array
        );
    }
}

// The run function is the heart of Parseq. It launches the requestors and manages timing, cancellation, and throttling.
function run(
    factory_name,
    requestor_array,
    initial_value,
    action,
    timeout,
    time_limit,
    throttle = 0
) {
    // The run function does the work that is common to all of the Parseq factories. It takes the name of the factory, an array of requestors, an initial value, an action callback, a timeout callback, a time limit in milliseconds, and a throttle.
    // If all goes well, we call all of the requestor functions in the array. Each of them might return a cancel function that is kept in the cancel_array.
    let cancel_array = new Array(requestor_array.length);
    let next_number = 0;
    let timer_id;

    // We need cancel and start_requestor functions.
    function cancel(reason = make_reason(factory_name, "Cancel.")) {
        // Stop all unfinished business. This can be called when a requestor fails. It can also be called when a requestor succeeds, such as race stopping its losers, or parallel stopping the unfinished optionals.
        // If a timer is running, stop it.
        if (timer_id !== undefined) {
            clearTimeout(timer_id);
            timer_id = undefined;
        }

        // If anything is still going, cancel it.
        if (cancel_array !== undefined) {
            cancel_array.forEach(function (cancel) {
                try {
                    if (typeof cancel === "function") {
                        return cancel(reason);
                    }
                } catch (ignore) {}
            });
            cancel_array = undefined;
        }
    }

    function start_requestor(value) {
        // The start_requestor function is not recursive, exactly. It does not directly call itself, but it does return a function that might call start_requestor.
        // Start the execution of a requestor, if there are any still waiting.
        if (
            cancel_array !== undefined
            && next_number < requestor_array.length
        ) {
            // Each requestor has a number.
            let number = next_number;
            next_number += 1;

            // Call the next requestor, passing in a callback function, saving the cancel function that the requestor might return.
            const requestor = requestor_array[number];
            try {
                cancel_array[number] = requestor(
                    function start_requestor_callback(value, reason) {
                        // This callback function is called by the requestor when it is done. If we are no longer running, then this call is ignored. For example, it might be a result that is sent back after the time limit has expired. This callback function can only be called once.
                        if (
                            cancel_array !== undefined
                            && number !== undefined
                        ) {
                            // We no longer need the cancel associated with this requestor.
                            cancel_array[number] = undefined;

                            // Call the action function to let the requestor know what happened.
                            action(value, reason, number);

                            // Clear number so this callback can not be used again.
                            number = undefined;

                            // If there are any requestors that are still waiting to start, then start the next one. If the next requestor is in a sequence, then it gets the most recent value. The others get the initial_value.
                            return start_requestor(
                                factory_name === "sequence"
                                    ? value
                                    : initial_value
                            );
                        }
                    },
                    value
                );
            } catch (exception) {
                // Requestors are required to report their failure through the callback. They are not allowed to throw exceptions. If we happen to catch one, it is treated as a failure.
                action(undefined, exception, number);
                number = undefined;
                start_requestor(value);
            }
        }
    }

    // With the cancel and the start_requestor functions in hand, we can now get to work.
    // If a timeout was requested, start the timer.
    if (time_limit !== undefined) {
        if (typeof time_limit === "number" && time_limit >= 0) {
            if (time_limit > 0) {
                timer_id = setTimeout(timeout, time_limit);
            }
        } else {
            throw make_reason(factory_name, "Bad time limit.", time_limit);
        }
    }

    // If we are doing race or parallel, we want to start all of the requestors at once. However, if there is a throttle in place then we start as many as the throttle allows, and then as each requestor finishes, another is started.
    // The sequence and fallback factories set throttle to 1 because they process one at a time and always start another requestor when the previous requestor finishes.
    if (!Number.isSafeInteger(throttle) || throttle < 0) {
        throw make_reason(factory_name, "Bad throttle.", throttle);
    }
    let repeat = Math.min(throttle || Infinity, requestor_array.length);
    while (repeat > 0) {
        setTimeout(start_requestor, 0, initial_value);
        repeat -= 1;
    }

    // We return cancel which allows the requestor to cancel this work.
    return cancel;
}

// And now, the four public functions:
// The parallel function is the most complicated because of the array of optional requestors.
function parallel(
    required_array,
    optional_array,
    time_limit,
    time_option,
    throttle,
    factory_name = "parallel"
) {
    // The parallel factory is the most complex of these factories. It can take a second array of requestors that get a more forgiving failure policy. It returns a requestor that produces an array of values.
    let number_of_required;
    let requestor_array;

    // There are four cases because `required_array` and `optional_array` can both be empty.
    if (required_array === undefined || required_array.length === 0) {
        number_of_required = 0;
        if (optional_array === undefined || optional_array.length === 0) {
            // If both are empty, then there is probably a mistake.
            throw make_reason(
                factory_name,
                "Missing requestor array.",
                required_array
            );
        }
        // If there is only `optional_array`, then it is the `requestor_array`.
        requestor_array = optional_array;
        time_option = true;
    } else {
        // If there is only `required_array`, then it is the `requestor_array`.
        number_of_required = required_array.length;
        if (optional_array === undefined || optional_array.length === 0) {
            requestor_array = required_array;
            time_option = undefined;
        } else {
            // If both arrays are provided, we concatenate them together.
            requestor_array = required_array.concat(optional_array);
            if (time_option !== undefined && typeof time_option !== "boolean") {
                throw make_reason(
                    factory_name,
                    "Bad time_option.",
                    time_option
                );
            }
        }
    }

    // We check the array and return the requestor.
    check_requestor_array(requestor_array, factory_name);
    return function parallel_requestor(callback, initial_value) {
        check_callback(callback, factory_name);
        let number_of_pending = requestor_array.length;
        let number_of_pending_required = number_of_required;
        let results = [];

        // run gets it started.
        let cancel = run(
            factory_name,
            requestor_array,
            initial_value,
            function parallel_action(value, reason, number) {
                // The action function gets the result of each requestor in the array. parallel wants to return an array of all of the values it sees.
                results[number] = value;
                number_of_pending -= 1;

                // If the requestor was one of the requireds, make sure it was successful. If it failed, then the parallel operation fails. If an optionals requestor fails, we can still continue.
                if (number < number_of_required) {
                    number_of_pending_required -= 1;
                    if (value === undefined) {
                        cancel(reason);
                        callback(undefined, reason);
                        callback = undefined;
                        return;
                    }
                }

                // If all have been processed, or if the requireds have all succeeded and we do not have a time_option, then we are done.
                if (
                    number_of_pending < 1
                    || (
                        time_option === undefined
                        && number_of_pending_required < 1
                    )
                ) {
                    cancel(make_reason(factory_name, "Optional."));
                    callback(
                        factory_name === "sequence"
                            ? results.pop()
                            : results
                    );
                    callback = undefined;
                }
            },
            function parallel_timeout() {
                // When the timer fires, work stops unless we were under the false time option. The false time option puts no time limits on the requireds, allowing the optionals to run until the requireds finish or the time expires, whichever happens last.



Edsger Dijkstra 是最早认识到线程问题的人之一，时间是在1962年。他设计出了第一个互斥机制，即 *信号量*。信号量以两个函数的形式实现：P 和 V。P 会尝试锁定临界区，如果已被锁定则阻塞调用者。V 会释放锁，允许等待的线程锁定临界区并运行。

Per Brinch Hansen 和 C. A. R. Hoare 将信号量集成到类中，创造出了 *监视器*，一种希望提供更大便利性和错误抵抗能力的语法形式。

Java 语言做了一件类似的事情，称为 *synchronized*（同步）。它使用 `synchronized` 关键字来修饰需要插入信号量的代码。不幸的是，他们选的这个词毫无道理。

*Synchronous*（同步的）意味着同时存在或使用同一个时钟。交响乐团中的音乐家是同步的，因为他们都按照指挥的节拍演奏。Java 创造时，设计者找了一个与时间有关的词。不幸的是，他们找得不够仔细。

当微软希望向 C# 中添加深度错误的异步支持时，他们借鉴了 Java，拿了一个错误的词，然后通过加上 **a-** 前缀来制造一个反义词，让它变得更糟。**async**（异步）这个词毫无意义。

大多数程序员在并发编程方面几乎没有受过训练或经验。同时管理多个活动流是陌生和奇怪的。给他们一个从根本上就错误的术语并不会让事情变得更容易。这是不知情者在误导更不知情者。

# 第21章

## Date 的工作原理

> 当你打开门时，你神秘的约会对象会是个美梦，还是个失望？
> *Milton Bradley*

我们的日历将太阳和月亮的运动映射到稳定流逝的时间上，但它是在我们发现太阳系如何运作之前很久就设计出来的。它被修补过很多次，但从未被完全修复。我们这个畸形的日历通过征服和商业被强加给越来越大的社群。最终，它在没有先被纠正或用更合适的设计取代的情况下，被强加给了全球社群。它能用，全世界都靠它运行，但它本可以更好。

我们的现代日历基于罗马日历，后者最初有十个月和一个额外的冬季来容纳一年剩余的日子。三月（以战神马尔斯命名）是第一个月。十二月（意为 *第十个月*）是第十个月。冬季被两个新月份取代：一月和二月。有时会从二月窃取日子用于延长其他月份，这是出于政治目的。日历大约每四年漂移一天，因为一年的天数不是整数。（一年的天数不是整数，这不是罗马的错。）他们试图通过将一月定为第一个月来权宜地重新调整他们的日历。十二月（仍然意为 *第十个月*）变成了第十二个月。

尤利乌斯·凯撒确立了标准：每四年向二月添加一个闰日。这减少了季节漂移，但没有完全消除它。格里高利标准化了一个更好的闰年算法，但一个更简单、更精确的算法从未被采纳。格里高利算法：

> 在能被4整除的年份添加一个闰日，除非该年份也能被100整除，但如果该年份能被400整除，则无论如何都要添加闰日。

这得出平均一年为365.2425天，这与热带年（约365.242188792天）相当接近。

有一个更好的算法：

> 在能被4整除的年份添加一个闰日，除非该年份也能被128整除。

这得出一年为365.2421875天，这比热带年更接近。对我来说，作为一个程序员，算法中包含两个2的幂似乎是奇迹般的，不过如果它能精确匹配真实的年份，我会更加印象深刻。如果一年的天数是整数，我可能会认为智能设计的概念可能真有其道理。

4|100|400 算法和 4|128 算法下次出现分歧的年份是2048年。我们应该在那之前标准化4|128算法。

闰日过去是添加在年末的。不幸的是，当一月成为第一个月时，他们没有把闰日从二月移到十二月（仍然意为 *第十个月*）。

分钟和秒是从零开始的值，这很好，而且它们都是模60的，这就不那么好了。小时是从零开始的，但12小时制用12替换了0，这很奇怪。

（如果可以的话，我会选择一天10小时，一小时100分钟，一分钟100秒。我的秒会稍微短一点，是当前秒的86.4%。秒的节奏会是一个不错的慢板，比当前的广板节奏有所改善。）

月份和日期是从一开始的值，因为它们是在零被发现之前标准化的。月份是模12。罗马人试图让月份模10，但他们无法成功。每个月的天数是模30或31或28或29，具体取决于月份和年份。年份是从一开始的，但当前的年份编号是在公元纪元许多世纪后才采用的，所以我们可以安全地忽略那个不便。

### Date 函数

计时标准中的怪异之处对于必须处理时间的程序来说是个隐患。Java 的 `Date` 类提供了对日期的支持。它本该是个简单的事情，但它非常复杂，展示了古典编程中最糟糕的设计模式之一。JavaScript 本可以做得明显更好，但它只是照搬了 Java 非常糟糕的例子。

如今的 JavaScript `Date` 对象带有大量的方法。它们大多数只是获取器和设置器。
```



### 日期方法

getDate setDay toDateString
getDay setFullYear toISOString
getFullYear setHours toJSON
getHours setMilliseconds toLocaleDateString
getMilliseconds setMinutes toLocaleString
getMinutes setMonth toLocaleTimeString
getSeconds setTime toString
getTime setUTCDate toTimeString
getTimezoneOffset setUTCString
getUTCDate setUTCFullYear
getUTCDay setUTCHours
getUTCFullYear setUTCMilliseconds
getUTCMinutes setUTCMonth
getUTCHours setUTCSeconds
getUTCMilliseconds setYear
getUTCMinutes
getUTCMonth
getUTCSeconds
getYear

`getDate` 方法从日期对象中返回月份的日期。你可以立刻注意到，在同一个方法中，"Date" 这个词有着两种截然不同的含义。更令人困惑的是，还有一个 `getDay` 方法，它返回的是星期几。

`getMonth` 方法将月份修正为从零开始，因为程序员喜欢从零开始处理事物。所以 `getMonth` 返回的是 0 到 11 之间的数字。而 `getDate` 方法没有修正日期，所以它返回的是 1 到 31 之间的数字。这种宽松的不一致性是错误的根源。

`getYear` 和 `setYear` 方法在 1999 年之后无法正确工作，不应再使用。Java 于 1995 年发布，其中包含的日期方法会在 2000 年出现问题。难道他们没听说过千年虫问题吗？还是他们怀疑 Java 在市场上的存活时间不够长，以至于这个问题无关紧要？我们可能永远不得而知。我们确实知道的是，Java 神奇地存活了下来，而 JavaScript 犯了完全相同的错误。请务必始终使用 `getFullYear` 和 `setFullYear` 代替。

`Date` 在经典编程中展示了一种非常糟糕的实践。一个对象应该封装某些东西。与对象的交互应该是事务和其他高级活动。`Date` 暴露了一个非常底层的视图，为每个时间组件都提供了 getter 和 setter。这种方法没有很好地利用对象。

### ISO 8601

新的 `Date` 构造函数可以接受一个表示日期的字符串，并为该日期生成一个对象。不幸的是，ECMAScript 标准并未指定解析和识别规则，因此根据标准，不保证它一定能工作。

ISO 日期除外。

ISO 8601 是表示日期和时间的国际标准。JavaScript 必须正确解析像 `2018-11-06` 这样的 ISO 日期。将最重要的信息放在最前面，最不重要的放在最后，这非常有意义，当然比美国标准 `11/06/2018` 更有意义。例如，我们可以对 ISO 日期字符串进行排序。

### 一种不同的方法

当然，现在要做正确的事为时已晚。JavaScript 不应该复制 Java。那永远是个错误。JavaScript 中许多错误都源于 Java。如果做正确的事是一种选择，我会这样提议：

应该有日期的三种表示形式：

- 自纪元以来的毫秒数。
- 一个可以包含以下属性的数据对象：
  - year
  - month
  - day
  - hour
  - minute
  - second
  - zone
  - week
  - weekday
- 一个采用某种标准格式的字符串。

我们不需要带有方法的古典 `Date` 对象。我们只需要简单的函数在三种表示形式之间进行转换。

`Date.now()` 以数字形式返回当前时间。这个函数已经存在。JavaScript 让所有代码都可以使用这个函数，但我认为它应该是一项只授予受信任代码的特权。一段不纯净的恶意代码可以使用 `Date.now()` 或 `Math.random()` 来改变其行为，从而避免被检测到。

`Date.object()` 将接受一个数字或一个字符串，并返回一个包含可提取信息的对象。当参数是字符串时，可以有额外的可选参数来确定时区和驱动解析的格式标准。

`Date.string()` 将接受一个数字或一个数据对象，以及一个可选的格式标准和时区，并返回时间的可读字符串表示形式。

`Date.number()` 将接受一个数据对象或字符串，以及一个可选的格式标准和时区，并返回时间的数字表示形式。

这种方法会简单得多，更易于使用，更不容易出错，而且（尽管现在这已不重要）还为 Y2K 做好了准备。它只是一个非纯函数和三个纯函数，而不是那一堆底层的、非纯的方法。Java 无法做到这一点，因为它缺少 JavaScript 可爱的对象字面量。我不知道为什么 JavaScript 不这样做。我希望下一种语言会这样做。

JavaScript 使用的纪元是 Unix 纪元：`1970-01-01`。有一些 32 位的 Unix 系统会在 2038 年失败，因为所有位都被用完，时钟会溢出。事实证明，32 位对于以秒分辨率运行系统时钟来说是不够的。

我倾向于使用 `0000-01-01` 作为纪元。JavaScript 数字直到 285426 年才会因累积毫秒数而失效。到那时，我们要么设计出更好的历法，要么已经灭绝了。祝你度过愉快的一天。

# 第 22 章

## JSON 的工作原理

> 对于有效载荷格式，XML 必须是主流，这并非因为它在技术上有多出色，而是因为它成功实现了非凡的广泛采用。这正是 JSON（或 YAML）的支持者们真正误解的地方，他们自豪地指出其格式的技术优势：任何一个该死的傻瓜都能创造出比 XML 更好的数据格式。

*詹姆斯·克拉克*

在此，我首次在印刷品中讲述这个世界上备受喜爱的数据交换格式的真实起源故事。

### 发现

JSON 于 2001 年在 Chip Morningstar 房子后面的一个棚屋里被发现。Chip 和我创办了一家公司，开发一个用于单页 Web 应用程序的平台。我们的理念是，借助一个优秀的 JavaScript 库（我写的）和一个高效、可扩展的会话服务器（Chip 写的），可以创建出与可安装应用程序一样好，甚至更好的网页。因为我们的平台还支持多用户协作，而这是 Web 尚未追上的功能。

我仍然对 Chip 的会话服务器印象深刻。多年来，他多次重写了它。最近的版本叫做 Elko。`elkoserver.org`

Elko 唯一的问题是它用 Java 写成。我的梦想是，不久的将来有人会付钱让 Chip 再做一次，但这次用 JavaScript。这将使我们远远领先于现在使用 Node.js 的状态。我们将获得更好的安全性、更好的可扩展性，以及对更广泛应用的支持。

回到那个棚屋。我们需要一种在浏览器和服务器之间发送信息的方式。当时，软件行业已完全投身于 XML。微软、IBM、Oracle、Sun、HP 等巨头已经决定，下一代软件将建立在 XML 之上，他们的卫星公司和客户也纷纷跟进。

#### 22.1 JSON 的工作原理

我们希望在用两种不同语言编写的程序之间交换数据。我们研究了 XML，认为它不适合我们的问题。使用 XML 的模式是，你首先向服务器发送一个查询，服务器用一个 XML 文档响应。然后为了获取数据，你需要对 XML 文档进行进一步查询。为什么服务器不能直接以一种我们的程序能立即使用的格式发送数据呢？我们的数据根本不像文档。

当时有很多改进的 XML 变体和替代品，但它们都没有获得任何发展势头。我们考虑过自己制定标准。然后我顿悟了。我们可以使用 JavaScript 对象字面量。它们内置于 JavaScript 中，所以在 JavaScript 这边非常方便。而且我们需要的子集在 Java 这边也不难解析。这肯定比 XML 更省力。

我们希望我们的平台既能与微软的 Internet Explorer 配合，也能与 Netscape Navigator 配合。这非常困难，因为这两家公司都在发明自己的特性。共同点很少。微软添加了一个 XMLHttpRequest 函数，可以用于与服务器通信。不幸的是，Netscape 没有类似的东西，所以我们不能使用它。

两种浏览器都有 JavaScript（ES3）并且都有框架集。所以我们一起使用它们来打造一个通信通道。这是发送到浏览器的第一个 JSON 消息：

```html
<html><head><script>
document.domain = "fudco.com";
parent.session.receive({to: "session", do: "test", text: "Hello world"});
</script></head></html>
```

一个网页包含一个不可见的框架，可以被导航。对隐藏框架执行 POST 操作会向服务器发送消息。服务器通过传输一个包含脚本的文档来响应，该脚本调用主框架中 session 对象的 receive 方法。我们必须修改 document.domain 以启用框架间通信。JavaScript 编译器解析了这个消息。

我希望我能告诉你第一条消息成功送达了，但它失败了。它失败是因为 ES3 糟糕的保留字策略。以下是当时的保留字：

```
abstract boolean break byte case catch char class const continue debugger
	default delete do double else enum export extends false final finally float for
	function goto if implements import in instanceof int interface long native new
	null package private protected public return short static super switch
	synchronized this throw throws transient true try typeof var void volatile
	while with
```

ES3 的保留字策略规定，这些词都不能用作变量名、参数名、点位置的属性名或对象字面量中的属性名。消息中包含一个 `do` 属性，所以脚本有语法错误，没有运行。

我很高兴地报告，这在 ES5 中得到了修正。保留字列表被缩短了，对属性名的限制也被取消了，但在 2001 年，我们

不得不给“do”加上引号才能让它正常工作。Chip把保留字列表放进了他的编码器，之后我们就再也没有遇到这类问题了。

我们发现一个包含字符序列</*小于号斜杠*的字符串会导致解析失败。那是因为浏览器会将其视为**script**标签的结束，导致JavaScript无法接收到完整的内容，从而引发语法错误。我们的解决办法是转义这个斜杠。浏览器对<\/ *小于号反斜杠斜杠*感到满意。

我们将其称为JSML（发音与dismal押韵）。后来我们得知有一些Java的东西也使用了这些首字母缩写，于是我们很快选了一个替代名称：**JSON**。

JSON在JavaScript和Java之间的通信中表现得非常出色。我们也用它进行服务器间通信。我们创建了第一个JSON数据库。

### 标准化

我们向客户推销JSON概念时遇到了困难。他们告诉我们无法使用它，因为他们已经承诺使用XML。他们还说无法使用它，因为它不是标准。我告诉他们它是标准，是ECMA-262的子集。他们说*那个*不是标准。于是我决定成为一个标准制定机构。

我购买了域名**json.org**，并开始着手将JSON形式化。在那之前，JSON只是Chip、我以及JavaScript之间的一个君子协定。在制定标准时，我不得不做出一些决定。我的指导原则是：保持文本性、最小化，并且是JavaScript的子集。

最小化原则至关重要。标准应该简单而完整。我们需要同意的内容越少，就越容易实现互操作。JavaScript子集的原则有效地防止了我添加许多花哨且不必要的功能。

JavaScript允许字符串用' *单引号*和" *双引号*进行引用。最小化原则告诉我们并不需要两种都支持。

我决定要求属性名必须用引号括起来。我不想把ES3的保留字列表放入标准中，因为它看起来真的很蠢。必然会有人问*为什么？*，而答案将是*因为JavaScript。*我们正试图说服人们用JavaScript开发应用程序，所以我不希望JSON标准凸显JavaScript的缺点。如果我们给所有名字都加上引号，这个问题就不会出现。这也简化了规范，因为*什么是字母？*由于国际化而变成了一个非常复杂的问题。因此，所有这些也都避免了。属性名可以是任何字符串。简单。这也使得JSON更像Python，我认为这有助于推动其采用。

我添加了注释，因为根据JavaScript子集原则它们被允许，而且我觉得它们会很有趣。然后我看到一些早期采用者在注释中放入解析指令。这将破坏互操作性，而这正是整个问题的关键。

随着更多语言的JSON编解码器被开发出来，我注意到开发JSON解析器大约有一半的工作是在处理注释。这不是因为注释很复杂，而是因为JSON的其他部分如此简单。注释正在减缓采用速度。

#### 22.3 JSON的工作原理

然后YAML社区联系了我。JSON意外地类似于YAML的一个子集。如果我们双方都做一些改变，JSON可以成为一个规范的子集。争论的焦点之一就是注释。

JSON的真正目的是通过网络连接用不同语言编写的程序。注释总是被忽略的，所以当使用它们时，会降低网络性能。注释是多余的，是一个诱人的陷阱，所以我移除了它们。

如果你真的需要注释，有几种方法可以做到。只需将带注释的文本通过像jsmin这样的代码压缩器处理。不幸的是，这个解决方案不适合那些缺乏编写简单管道脚本技能的程序员。

另一个解决方案是形式化注释并将它们放入JSON结构中。如果注释至关重要，那么应该给它们命名，以便能够正确地保留和处理。

我未能实现让JSON成为JavaScript规范子集的目标。Unicode有一对不可见的控制字符，PS *段落分隔符*和LS *行分隔符*，这是为了方便老式的文字处理系统。JavaScript将它们视为行结束符，就像CR *回车*和LF *换行*一样。我忽略了这一点，所以JSON允许它们出现在字符串中。幸运的是，PS和LS很少使用。我没有意识到由此产生的任何问题。ES5添加了一个内置的JSON解析器来处理PS和LS，修复了这种不兼容性。

Unicode中有些字符，但Unicode自己说它们不是字符。有一些Unicode狂热者坚持认为JSON不应该允许马格里特字符。JSON并不在乎。JSON是一种媒介，而不是执行者。如何处理那些不是字符的字符，由接收者决定。JSON并不保证所有内容对每个接收者都有意义。如果发送者和接收者能够达成共识，那么这种共识就可以用JSON表达出来。

我希望让JSON独立于IEEE 754。Java和JavaScript都使用IEEE 754二进制浮点数，但JSON并不在乎。JSON能够促进使用不同数字表示的语言之间的通信。因此，二进制浮点语言可以与BCD语言交换数据，大十进制浮点语言可以与那些使用古怪内部表示（将三位数字打包到10位字段中）的语言交互。JSON可以经受住IEEE 754过时的考验。

我排除了`Infinity`和`NaN`，因为它们在数据中的存在表示错误，我们不应该在传输中发送坏数据。我们不应该传播坏数据。这是一种极其糟糕的做法。

我包含了e和E作为十进制指数标记，这违反了最小化原则。我本应排除E。我也应该排除e后面的+。

我包含了`null`，因为计算机科学家似乎喜欢它。JSON不给`null`赋予任何含义。这由JSON的使用者决定。JSON不指定任何行为。它只指定一个格式，一个用于数据的简单语法。

我创建了一个单页网站，用三种方式描述JSON：一种McKeeman形式语法、铁路图和非正式的英文描述。我希望读者能理解其中至少一种。

我没有为JSON或其标志获取商标。我没有在页面上放置版权声明。我希望让JSON标准尽可能自由和不受阻碍。我不希望靠JSON赚钱。我只是希望被允许使用它。

我开始收到请求，要求在`json.org`网站上添加各种语言编解码器的链接，我照做了。几乎所有的编解码器都是开放和免费的。我还收到了页面翻译的捐赠。JSON简洁性的一个好处就是页面易于翻译。

2006年，我为IETF撰写了信息性RFC 4627，目的是为JSON分配一个MIME类型。我希望能为你们争取到`text/json`，但他们愿意给我们的最好是`application/json`，这非常令人失望。

鉴于JSON的成功，我认为IETF应该让`json`成为一流的媒体类型，以便人们可以注册像`json/geo`和`json/money`这样的MIME类型。

2013年，我撰写了ECMA-404，被ISO采纳为ISO/IEC 21778。JSON变得如此重要，以至于其他标准需要引用它，并且他们需要一个比我的网页更正式的引用。

### JSON为何有效

JSON旨在允许用不同语言编写的程序进行有效通信。这是一个难题，因为语言中值和数据结构的表示细节可能相当复杂。因此，我设计JSON的方法是专注于共同点。

语言在数字的表示上差异很大，但都可以达成共识：一个数字可以用一串十进制数字来表示，可能包含小数点，也可能包含十进制指数。有些语言有整数类型，有些（比如JavaScript）则没有。JSON表明，我们都可以从一串数字中解读出最好的含义。

语言对于字符串和字符集有不同的想法。一种语言可能使用UTF-16（如JavaScript）、UTF-32、UTF-8、ASCII、半ASCII或EBCDIC作为内部表示。JSON并不在乎。我们从传输的一串字符中尽可能解读出合理的含义，并将它们转换成合理的本地表示。

所有语言都有某种线性序列值的数据结构。细节可能千差万别，但在JSON解码器的帮助下，所有语言都能理解由逗号分隔并包裹在方括号中的一系列值。从零开始索引的语言可以与从一开始索引的语言交换数据。

大多数语言都有某种将名称与值关联的数据结构。细节可能千差万别，但在JSON解码器的帮助下，所有语言都能理解由逗号分隔并包裹在大括号中的一系列命名值。



[content]
### 影响

我之所以能认识到对象字面量的可移植性，得益于我对另外两种语言的经验。LISP 语言有一种名为*s-表达式*的文本表示形式，既用于程序也用于数据。Rebol 语言也使用相同的文本表示形式来表达程序和数据，但其语法要丰富得多。在 Rebol 中，使用这种文本表示形式来序列化数据以进行传输是非常自然的做法。我将同样的想法应用到了 JavaScript 中。

我并非第一个将 JavaScript 用作数据编码的人。这一点被许多人独立发现，最早可追溯到 1996 年。我是那个试图将其推广为标准的人。

JavaScript、Python 和 Newtonscript 这三种语言大约在同一时期设计，且在创建数据结构方面都具有相似的语法。NeXT 的 OpenStep 属性列表（Property Lists）出现得稍早，也采用了类似的表示法。

在我们这个后 XML 时代的舒适环境中，JSON 看起来似乎是必然的。但当它逐步发展时，情况远非如此确定。

### JSON 对象

JavaScript 通过 JSON 对象中的两个函数来支持 JSON。这两个函数分别名为 `parse` 和 `stringify`，这完全是我的过错。我选择 `parse` 是效仿了 `Date` 函数的不良先例，我们已经知道那个函数有严重的缺陷。我选择 `stringify` 是因为 `toString` 似乎不太合适。我本应该把这两个函数命名为 `decode` 和 `encode`。

```
JSON.parse(text, reviver)
```

**parse** 函数接受一个 JSON 文本，并将其解码为 JavaScript 数据。可选的 *reviver* 函数可以进行转换。它接收一个键和一个值，并返回该键所需的值。

例如，你可以创建一个 *reviver* 函数，将日期字符串转换为日期对象。如果一个键以 `_date` 结尾，或者该值是一个 ISO 日期格式的字符串，那么就将该值替换为根据该值创建的 `Date` 对象。JSON 本身并不包含日期，但日期可以方便地编码为字符串，然后在另一端转换为日期对象。

```javascript
const rx_iso_date = /
    ^ \d{4} - \d{2} - \d{2}
    (?:
        T \d{2} : \d{2} : \d{2}
        (?:
            \. \d*
        )? Z
    )? $
/;
```

```javascript
const result = JSON.parse(text, function (key, value) {
    return (
        typeof value === "string" && (
            key.endsWith("_date")
            || rx_iso_date.match(value)
        )
        ? new Date(value)
        : value
    );
});
```

```
JSON.stringify(value, replacer, space)
```

stringify 函数接受一个值并将其编码为 JSON 文本。可选的 replacer 函数可以进行转换。它接收一个键和一个值，并返回该键所需的值。

例如，如果我们想自动将 Date 对象转换为 ISO 字符串，我们可以提供一个 replacer 函数。该 replacer 函数的结果会被传递给 JSON.stringify，并包含在最终文本中。

```javascript
const json_text = JSON.stringify(my_little_object, function (key, value) {
    return (
        value instanceof Date
        ? value.toISOString()
        : value
    );
});
```

（事实上，我们不需要这样做，因为 Date.prototype.toJSON 已经自动完成了这个转换。请参见下面的 toJSON 部分。）

replacer 参数也可以是一个字符串数组。只有名称在该数组中的属性才会包含在文本中。这是一个白名单，可以过滤掉当前不重要的属性。这本应是一个单独的参数，而不是对 replacer 函数的重载。

JSON 格式允许 JSON 文本中包含空白字符，以使其更具人类可读性。默认情况下，JSON.stringify 不添加空白字符，以使文本在传输时更紧凑。如果使用了 space 参数，则会插入换行符和缩进。space 的正确值是 4。显然。我本应将其设置为布尔值。

```
toJSON()
```

任何对象都可以有一个 `toJSON` 方法，该方法在对象被 `JSON.stringify` 序列化时被调用。这就是无类对象（class free objects）可以拥有 JSON 表示的方式。一个只包含函数的无类对象，通常序列化时会像一个空对象。但如果它有 `toJSON` 方法，那么它将按照 `toJSON` 的返回值进行序列化。

Date 对象继承了一个 `toJSON` 方法，该方法将日期对象编码为 ISO 字符串。

### 安全影响

JSON 的早期用户使用 JavaScript 的 eval 函数（或其等效函数）来解码 JSON 文本。eval 函数存在固有的危险，但在这种情况下，潜在危险的文本来自提供 HTML 和所有脚本的同一服务器，因此其安全性并不比整个网络环境更差。

当通过 script 标签从其他服务器加载 JSON 的做法流行起来时，情况发生了变化。脚本由 eval 求值，而无法保证有效载荷是合格的 JSON 而非 XSS 攻击。这既方便又不负责任。

JSON 文本绝不应通过拼接来构建，因为一段恶意字符串可能包含引号和反斜杠字符，从而导致文本被误解。JSON 文本应始终使用编码器（如 `JSON.stringify` 或类似工具）来生成，这些工具不允许出现此类混淆。

这就是为什么 *toJSON* 的结果和 *replacer* 函数的结果需要由 `JSON.stringify` 处理。如果这些函数的返回值*直接*插入到文本中，那么这些函数就可能被诱骗去促成字符串混淆。如果字符串不用相同的字符开始和结束就好了，但事实并非如此。这给了我们另一个需要谨慎编码的理由。

### 麦基曼形式

麦基曼形式（McKeeman Form）是一种表示语法的表示法。它由达特茅斯学院的 Bill McKeeman 提出。它是一种简化的巴科斯-范式（Backus-Naur Form），具有重要的空白符意义，并且最少地使用元字符。我喜欢它，因为它完全且最小程度地足够表达。

我们可以用麦基曼形式来表达麦基曼形式本身的语法。

一个*语法*（*grammar*）是一个或多个规则的列表。

```
grammar
    rules
```

Unicode 码位 U+0020 用作*空格*（*space*）。Unicode 码位 U+000A 用作*换行符*（*newline*）。

```
space
    '0020'

newline
    '000A'
```

一个*名称*（*name*）是字母或下划线 _ 组成的序列。

```
name
    letter
    letter name

letter
    'a' . 'z'
    'A' . 'Z'
    '_'
```

一个*缩进*（*indentation*）是四个空格。

```
indentation
    space space space space
```

每个*规则*（*rules*）之间用*换行符*分隔。一个*规则*（*rule*）在一行上有一个*名称*，其下方缩进的是*备选项*（*alternatives*）。

```
rules
    rule
    rule newline rules

rule
    name newline nothing alternatives
```

如果*规则*的*名称*之后的第一行是 ""，则该*规则*可能匹配*空内容*（*nothing*）。

```
nothing
    ""
    indentation '"' '"' newline
```

每个*备选项*单独缩进在一行上。每个*备选项*包含若干*项*（*items*），后跟一个*换行符*。

```
alternatives
    alternative
    alternative alternatives

alternative
    indentation items newline
```

*项*之间用空格分隔。一个*项*是一个*字面量*（*literal*）或一个*规则*的*名称*。

```
items
    item
    item space items

item
    literal
    name

literal
    singleton
    range exclude
    "'" characters "'"
```

除了 32 个控制码外的任何单个 Unicode 码位都可以放在单引号内。任何 Unicode 码位的*十六进制码*（*hexcode*）也可以放在单引号内。一个*十六进制码*可以包含 4、5 或 6 个十六进制数字。

```
singleton
    "'" codepoint "'"

codepoint
    ' ' . '10FFFF'
    hexcode

hexcode
    "10" hex hex hex hex
    hex hex hex hex hex
    hex hex hex hex
```

```
hex
    '0' . '9'
    'A' . 'F'
```

一个*范围*（*range*）被指定为一个*单例*（*singleton*）、一个 . *句点*和另一个*单例*。字面量范围后面可以可选地跟一个 - *减号*和要排除的字符。

```
range
    singleton space '.' space singleton

exclude
    ""
    space '-' space singleton exclude
    space '-' space range exclude
```

用 " *双引号*括起来的*字符*（*character*）可以是除 32 个控制码和 " *双引号*以外的任何 Unicode 码位。*字符*的定义展示了一个码位范围和排除的例子。

```
characters
    character
    character characters

character
    ' ' . '10FFFF' - '"'
```

### JSON 语法

这是以麦基曼形式表示的 JSON 语法。

```
json
    element

value
    object
    array
    string
    number
    "true"
    "false"
    "null"

object
    '{' ws '}'
    '{' members '}'

members
    member
    member ',' members

member
    ws string ws ':' element

array
    '[' ws ']'
    '[' elements ']'

elements
    element
    element ',' elements

element
    ws value ws

string
    '"' characters '"'

number
    integer fraction exponent

integer
    '-' optDigit
    digit
    digit integer

fraction
    ""
    "." digits

exponent
    ""
    "e" optSign optDigits
    "E" optSign optDigits

optSign
    ""
    '+'
    '-'

digits
    digit
    digit digits

digit
    '0' . '9'

optDigit
    digit
    optDigit digit

ws
    ""
    " " ws
    "\n" ws
    "\r" ws
    "\t" ws
```



```
elements
    element
    element ',' elements

element
    ws value ws

string
    '"' characters '"'

characters
    ""
    character characters

character
    '0020' . '10FFFF' - '"' - '\\'
    '\\' escape

escape
    '"'
    '\\'
    '/'
    'b'
    'f'
    'n'
    'r'
    't'
    'u' hex hex hex hex

hex
    digit
    'A' . 'F'
    'a' . 'f'

number
    integer fraction exponent

integer
    digit
    nonzero digits
    '-' digit
    '-' nonzero digits

digits
    digit
    digit digits

digit
    '0'
    nonzero

nonzero
    '1' . '9'

fraction
    ""
    '.' digits
exponent
    ""
    'E' sign digits
    'e' sign digits
sign
    ""
    '+'
    '-'
ws
    ""
    '0020' ws
    '000D' ws
    '000A' ws
    '0009' ws
```

#### 22.11 JSON 的工作原理

### 致数据交换标准设计者的建议

我并未打算让 JSON 成为最后一个数据交换标准。JSON 是为特定目的而设计的，并且它非常契合该目的。如今它正被成功地用于许多其他用途。对于某些用途，理应有更好的替代方案。因此，如果你打算设计下一个标准，我有一些建议。

#### 0. 请不要破坏 JSON。

我对 JSON 所做的最明智之举就是没有给它编版本号。如果你给某个东西标上 1.0，你就知道会有 1.1 和 1.2，而且在它达到 3.0 之前，一切都糟糕透顶。

JSON 只有一个标准版本。不破坏一切就无法改变 JSON。这避免了版本地狱问题——那是增量敏捷和永久测试版所带来的痛苦且令人尴尬的副作用。技术栈中的每一层都可以改变，唯独 JSON 层不行。JSON 将永远保持现在的样子。它是稳定的。我想不出有什么特性比这更有价值了。

#### 1. 让它显著更好。

我见过许多想在 JSON 上添加某个特定功能的提案。问题在于，这样就会出现两个大部分兼容但又不完全兼容的标准。这会给两个标准的用户带来兼容性税，而这种税以故障和配置问题的形式收取。

为新标准添加足够的真正价值，以补偿这种税。不要做琐碎或表面化的改动。要让改动有实质意义且完全值得。

#### 2. 给它一个更好的名字。

我见过很多提案，在 JSON 这个名字后面加上一个字母或数字。不要这样做。给它一个更好的名字。编程工作的很大一部分就是为事物起好名字。让我们看看你的本事。

JSON 最糟糕的地方就是这个名字。它代表 JavaScript Object Notation（JavaScript 对象表示法）。

**JS** 代表 JavaScript。JS 部分的问题在于它会误导人们。有些人认为 JSON 是一个只适用于 JavaScript 的 JavaScript 专属事物。有些人认为 JSON 是由 ECMAScript 标准定义的，这是错误的，因为 JSON 是由 ECMA-404（JSON 标准）定义的。而且，还有那个古老的 Java ≠ JavaScript 的混淆。

我们将 JavaScript 放入名称中是因为我们想对其来源表示认可。我们并不是想搭 JavaScript 的便车。2001 年，JavaScript 是世界上最不受待见的编程语言。所有喜欢 Java、C#、PHP、Python、Ruby、Perl、C++ 等语言的人都讨厌 JavaScript。不仅如此，几乎所有使用 JavaScript 的人也讨厌它。"好部分福音"的到来尚未来临。

**O** 代表 Object（对象）。在 JavaScript 中，*对象*是名称:值对的非正式集合，JSON 采用了这种用法。在其他语言中，*对象*意味着一个脆弱的类层次结构的实例。从这个角度来看，JSON 会被期望成为一种对象序列化格式，但它不是。JSON 是一种数据序列化格式。所以存在这种混淆。

**N** 代表 Notation（表示法）。我对*表示法*没有意见。如果你想把你的格式称为*表示法*，请便。

# 第 23 章

### 测试的工作原理

> 程序测试可以用来发现错误的存在，但永远无法证明错误的不存在！
>
> *艾兹格·迪科斯彻*

计算机程序是人类所创造的最复杂的事物。没有任何其他东西是由如此多错综复杂的部分组成的，而这些部分又必须完美地契合在一起并协同工作。一个完成的程序必须在各方面都完美无缺，对所有输入、所有状态、所有条件、所有时间都如此。我们与计算机之间的契约是：如果我们给它一个并非绝对完美的程序，那么计算机就有权在最糟糕的时刻做出最糟糕的事情，而这并非计算机的过错。是你的过错。

我们没有测试完美性的方法。我们可以证明一个程序包含缺陷，但没有任何测试能够证明一个程序是没有缺陷的。这种测试的失败催生了正确性证明方面的工作。其想法是，一个程序将在开发过程中附带其完美性的数学证明。这被认为是计算机科学中最重要的悬而未决的问题，不幸的是，它从未被解决。这些证明将比它们试图证明的程序本身复杂得多。其复杂性令人难以承受。

罗宾·米尔纳等人提出，类型安全性可能是一种比证明更实用的替代方案。类型比证明更容易集成到程序中。米尔纳有句名言：类型良好的程序不会"出错"。但在具有优秀类型系统的语言（如 Haskell）和具有糟糕类型系统的语言（如 C++ 和 Java）中，程序仍然会出错。也许有一天类型会有所回报。但至今还没有。

因此，随着证明和类型的失败，我们将已知并不完美的程序投入生产，希望在任何人发现之前，我们能找到并纠正错误。这太疯狂了。这就是现状。

一定有更好的方法。但如果有的话，至今还没有人找到。

这让我们回到了测试。测试，如果做得好，可以识别缺陷，然后让我们确信这些缺陷已被修正。即使测试做得好，它仍然无法证明错误的不存在。而且测试并不总是做得好。

### 测试的工作原理

在 20 世纪 70 年代末和 80 年代初，雅达利向比其他任何公司都多的人销售了比其他任何公司都多的软件。其中大部分软件被烧录到 ROM（只读存储器）芯片中。ROM 中的错误无法修正。你必须丢弃它们并制造新芯片。雅达利制造了一台家用电脑，其操作系统存储在 ROM 中。这给我留下了深刻的印象。他们一定对自己的编程有着惊人的信心，才敢冒险将那些东西放入 ROM。他们是怎么做到的？

我在雅达利的企业实验室找到了一份研究员的工作。这让我得以了解雅达利是怎么做到的。他们的秘诀是：他们会先试用，如果看起来能用，就送到工厂。他们很幸运。当管理层决定 *E. T.* 游戏不需要更多测试时，他们的好运用完了。公司没能挺过这个决定。

那时的程序要小得多、简单得多。如果一个程序只有几千字节，那么仔细编码和仔细测试就能产生好的结果。如今的程序规模巨大。没有人能理解全部。我们如何能确信一个过于复杂而无法理解的东西是正确的？

### 缺陷

缺陷（Bug）是由托马斯·阿尔瓦·爱迪生发现的。他当时正在开发留声机，这是一种用唱针在包裹在旋转圆柱体上的锡箔纸上录制和复制声音的装置。他的原型机每次旋转时唱针划过锡箔纸边缘都会发出一声啁啾。爱迪生对一位记者说，他熬了一整夜试图把留声机里的 *bug*（虫子/缺陷）弄出来。

这个词就此流传了下来。多年来，有许多关于疯狂发明家的故事，说他们一旦除掉了发明中最后的 bug 就能发大财。

有一个著名的飞蛾卡在哈佛 Mark II 计算机继电器中的故事。格蕾丝·穆雷·霍珀将这只飞蛾粘贴到了她的日志本上，并附上标题 *第一个被发现的真正的 bug 案例*。这不是第一个 bug，但它可能是第一个由昆虫造成的 bug。我们的大多数 bug 仍然由人类造成，不过人们对人工智能制造 bug 的潜力感到兴奋也是有道理的。

我们必须尽量减少程序中的混淆。当我们期望程序做一件事而它却做了另一件事时，这表明我们对任务存在混淆。我们必须让程序尽可能简洁明了，以减少混淆。*Bug* 是 *confusion*（混淆）的另一种说法。消除混淆比测试更有成效。

### 膨胀

软件开发中最大的问题之一是软件肥胖症，即膨胀。程序实在太大了。这可能是由于缺乏纪律的功能选择造成的，但更常见的原因是糟糕的架构。继承是一种流行的代码复用模式，但它效果不太好，所以经常转而使用复制粘贴。对库、平台和包的过度依赖，而这些库、平台和包又与许多其他库、平台和包紧密耦合。膨胀可能是敏捷开发实践的副作用。开发团队被扩大以帮助管理膨胀，但大型团队会导致更多的膨胀。

膨胀会导致安全问题，因为它增加了攻击面，并给 bug 提供了更多藏身之处。膨胀的系统更难进行充分的测试。



### 测试驱动开发（TDD）

我喜欢测试驱动开发作为一种方法论。但我痛恨测试驱动开发被当作一种宗教。TDD 狂热分子曾告诉我，在 TDD 下，草率、易出错的代码是被允许的，甚至是被鼓励的。他们假设测试会发现所有 bug，因此无需遵循严谨的编码风格。

这就是一个好实践如何演变成非常糟糕的实践。事实是，我们不能依赖测试来发现所有 bug。我们应该投资于 bug 避免。良好的编码实践是对质量的一项廉价投资。随着我观察 bug 形成的方式以及我能够减轻它们的方法，我自己的编码风格多年来也在改变。

我曾收到一位狂热分子提交的 JSLint 的 bug 报告。他附上了一个 JSLint 拒绝的函数。他说 JSLint 一定是错的，因为该函数通过了它的单元测试。粗略检查后发现 JSLint 是正确的。JSLint 发现了一个正则表达式中的 bug，而测试未能发现。测试本身存在错误。假阴性总会很快被修复，但假阳性却长存不灭。这些测试给予我们的是虚假的信心，而非质量。那么，谁来测试测试本身呢？

单元测试在底层代码中非常有效。例如，第 3 章的大整数库是底层代码，几乎不依赖任何其他东西。我为它编写了大量的单元测试，这些测试在库的开发过程中帮助很大。

随着我们向上层移动，单元测试的有效性会降低。随着依赖增加，测试变得不再那么有意义。测试制作的成本也因为需要开发存根、模拟对象和伪造对象而上升。（我听到开发者们在浪费时间争论某个东西是伪造对象还是模拟对象。）而随着我们向上攀升，复杂性从组件本身转移到了组件之间的连接上。

### 你休想通过

听起来令人绝望，但测试是必要的。良好而谨慎的设计和编码至关重要，但这还不够。我们仍然必须进行有效的测试。我们必须测试。

大多数测试库支持像这样的调用：

```
assertEquals("add 3 + 4", 7, add(3, 4));
```

这让我感觉不错，因为我写了一个测试，但认为单次加法运算就可能发现 `add` 函数中一个微妙的错误，这现实吗？我们需要在大得多的数值范围内进行大量的测试，但谁愿意编写所有这些测试呢？而且，这种形式无法测试最终的程序。它只能测试严格顺序执行的函数。

这就是为什么我编写了一个名为 JSCheck 的测试库，其灵感来源于一个名为 QuickCheck 的 Haskell 工具。JSCheck 进行用例生成，自动产生大量随机试验。JSCheck 还支持最终编程，用于测试服务器和浏览器应用程序。

```
jsc.claim(name, predicate, signature, classifier)
```

JSCheck 提供的最重要的函数是 `claim` 函数。一个 claim 是关于你的程序的一个断言。

`name` 是一个描述性字符串，用于报告中。

`predicate` 是一个函数，如果程序工作正确，它将返回 true。`predicate` 函数接受一个 `verdict` 回调函数，用于传递每次试验的结果。其余参数由 `signature` 参数决定。

`signature` 是一个生成器函数数组，用于为 `predicate` 函数生成参数。这些生成器可以使用 JSCheck 提供的说明符轻松创建。

`classifier` 函数是可选的。它可以用来拒绝无效的试验。它也可以对试验进行分类，使模式更易于评估。

```
jsc.check(configuration)
```

你可以根据需要创建任意数量的 claims，然后调用 `jsc.check` 函数来检查所有 claims 是否有效。

`jsc.check` 函数接受一个配置对象，该对象可以包含以下任何属性：

- `time_limit`：以毫秒为单位。每次试验有三种可能的结果：PASS（通过）、FAIL（失败）和 LOST（超时）。任何在时间耗尽前未给出 verdict 的试验都被视为 LOST。在某些情况下，得出正确答案太晚与失败无法区分。
- `on_pass`：每次通过试验的回调函数。
- `on_fail`：每次失败试验的回调函数。
- `on_lost`：每次未得出 verdict 的试验的回调函数。
- `on_report`：报告的回调函数。
- `on_result`：摘要的回调函数。
- `nr_trials`：为每个 claim 执行的试验次数。
- `detail`：报告的详细程度。
    1.  没有报告。
    2.  有最简报告，显示每个 claim 的通过分数。
    3.  失败的具体用例将被报告。
    4.  分类摘要也将被报告。
    5.  所有用例都将被报告。

我没有单独测试大整数库中的每个函数，而是设计了测试，让几个函数协同工作。例如，`demorgan` 测试使用了 `random`, `mask`, `xor`, `or`, `and`, 和 `eq`。JSCheck 生成随机整数，用于创建随机大整数，然后应用德摩根定律。

```
jsc.claim(
    "demorgan",
    function (verdict, n) {

    // !(a && b) === !a || !b

        let a = big_integer.random(n);
        let b = big_integer.random(n);
        let mask = big_integer.mask(n);
        let left = big_integer.xor(mask, big_integer.and(a, b));
        let right = big_integer.or(
            big_integer.xor(mask, a),
            big_integer.xor(mask, b)
        );
        return verdict(big_integer.eq(left, right));
    },
    [jsc.integer()]
);
```

我为一些测试制作了一个生成大整数的生成器。JSCheck 提供的说明符功能非常强大，但它们对大整数一无所知，所以我创建了自己的生成器。

```
function bigint(max_nr_bits) {
    return function () {
        let nr_bits = Math.floor(Math.random() * max_nr_bits);
        let result = big_integer.random(nr_bits);
        return (
            Math.random() < 0.5
            ? big_integer.neg(result)
            : result
        );
    }
}
```

我一起测试乘法和除法。我提供了一个分类器函数来拒绝可能除以零的试验。

```
jsc.claim(
    "mul & div",
    function (verdict, a, b) {
        let product = big_integer.mul(a, b);
        return verdict(big_integer.eq(a, big_integer.div(product, b)));
    },
    [bigint(99), bigint(99)],
    function classifier(a, b) {
        if (!big_integer.is_zero(b)) {
            return "";
        }
    }
);
```

我再次一起测试乘法和除法，但这次包含了余数。分类器输出两个值的符号，产生分类"--", "-+", "+-", 和 "++"。这有助于隔离由于符号处理引起的错误。

```
jsc.claim("div & mul & remainder", function (verdict, a, b) {
    let [quotient, remainder] = big_integer.divrem(a, b);
    return verdict(big_integer.eq(
        a,
        big_integer.add(big_integer.mul(quotient, b), remainder)
    ));
}, [bigint(99), bigint(99)], function classifier(a, b) {
    if (!big_integer.is_zero(b)) {
        return a[0] + b[0];
    }
});
```

我围绕恒等式构建测试。例如，将一个由 n 个 1 位组成的字符串加 1，结果应该与 2 ** n 相同。

```
jsc.claim("exp & mask", function (verdict, n) {
    return verdict(
        big_integer.eq(
            big_integer.add(big_integer.mask(n), big_integer.wun),
            big_integer.power(big_integer.two, n)
        )
    );
}, [jsc.integer(100)]);
```

这是另一个恒等式：(1 << n) - 1 应该是 n 个 1 位。

```
jsc.claim("mask & shift_up", function (verdict, n) {
    return verdict(big_integer.eq(
        big_integer.sub(
            big_integer.shift_up(big_integer.wun, n),
            big_integer.wun
        ),
        big_integer.mask(n)
    ));
}, [jsc.integer(0, 96)]);
```

我构建了大量类似的测试。这种测试风格给予我比从 `3 + 4` 中获得的信心大得多。

缓存可以缓解 Web 浏览器中膨胀的一些症状，但不幸的是，Web 浏览器在缓存方面做得并不好。有一些工具，如延迟加载器和树摇器，试图延迟或移除一些不必要的代码，但通过处理症状，它们可能会刺激更多的膨胀。

处理膨胀的最好方法是首先防止其发生。在设计和实施中，将软件的精简作为优先事项。避免采用臃肿的包和鼓励膨胀的工具。避免使用类。雇佣规模更小、训练更精良的开发团队。并积极实践代码移除。预留一些开发周期用于移除不必要的代码和淘汰有问题的包。当项目中的代码行数减少时，要庆祝。奉行*最小化原则*（The Principle of Least Big）。

功能有其收益，但也有其成本。如果我们未能核算成本，我们将以膨胀来支付代价。



### JSCheck

这是 JSCheck 的实现。其中最有趣的部分是能生成测试数据的说明符。其中大多数说明符都能以有趣的方式组合，因为它们通过 **resolve** 函数传递值。**resolve** 函数会返回其参数，除非该参数是一个函数。

```javascript
function resolve(value, ...rest) {
    return (
        typeof value === "function"
            ? value(...rest)
            : value
    );
}
```

**resolve** 函数接受一个值。如果该值是一个函数，则调用它以产生返回值。否则，该值本身就是返回值。

你可能还记得第 13 章中的 **literal** 作为常量。它能绕过函数，这样你就可以将一个函数传递给所有的试验。

```javascript
function literal(value) {
    return function () {
        return value;
    };
}
```

**boolean** 说明符生成一个产生布尔值的生成器。

```javascript
function boolean(bias = 0.5) {
    bias = resolve(bias);
    return function () {
        return Math.random() < bias;
    };
}
```

一个签名可以包含一个布尔值规范。可以提供一个可选的 bias 参数。如果 bias 是 0.25，那么大约四分之一产生的布尔值将是 true。

**number** 说明符，毫不奇怪，它在某个范围内生成数字。

```javascript
function number(from = 1, to = 0) {
    from = Number(resolve(from));
    to = Number(resolve(to));
    if (from > to) {
        [from, to] = [to, from];
    }
    const difference = to - from;
    return function () {
        return Math.random() * difference + from;
    };
}
```

**wun_of** 说明符接受一个值和生成器的数组，并返回一个随机返回这些值的生成器。**wun_of** 说明符还可以选择性地接受一个权重数组，这些权重可以影响选择的偏向性。

wun_of 说明符有两个签名。

```javascript
// wun_of(array)
//     从数组中取出一个元素并解析它。
//     元素被随机选择，概率相等。

// wun_of(array, weights)
//     两个参数都是长度相等的数组。
//     权重越大，元素被选中的可能性就越大。

function wun_of(array, weights) {
    if (
        !Array.isArray(array)
        || array.length < 1
        || (
            weights !== undefined
            && (!Array.isArray(weights) || array.length !== weights.length)
        )
    ) {
        throw new Error("JSCheck wun_of");
    }
    if (weights === undefined) {
        return function () {
            return resolve(array[Math.floor(Math.random() * array.length)]);
        };
    }
    const total = weights.reduce(function (a, b) {
        return a + b;
    });
    let base = 0;
    const list = weights.map(function (value) {
        base += value;
        return base / total;
    });
    return function () {
        let x = Math.random();
        return resolve(array[list.findIndex(function (element) {
            return element >= x;
        })]);
    };
}
```

**sequence** 说明符接受一个值和生成器的数组，并返回一个按顺序返回这些值的生成器。

```javascript
function sequence(seq) {
    seq = resolve(seq);
    if (!Array.isArray(seq)) {
        throw "JSCheck sequence";
    }
    let element_nr = -1;
    return function () {
        element_nr += 1;
        if (element_nr >= seq.length) {
            element_nr = 0;
        }
        return resolve(seq[element_nr]);
    };
}
```

**falsy** 说明符返回一个产生假值的生成器。

```javascript
const bottom = [false, null, undefined, "", 0, NaN];

function falsy() {
    return wun_of(bottom);
}
```

**integer** 说明符返回一个生成在选定范围内整数的生成器。如果未指定范围，则返回一个生成小于一千的随机素数的生成器。

```javascript
const primes = [
    2, 3, 5, 7, 11, 13, 17, 19, 23, 29,
    31, 37, 41, 43, 47, 53, 59, 61, 67, 71,
    73, 79, 83, 89, 97, 101, 103, 107, 109, 113,
    127, 131, 137, 139, 149, 151, 157, 163, 167, 173,
    179, 181, 191, 193, 197, 199, 211, 223, 227, 229,
    233, 239, 241, 251, 257, 263, 269, 271, 277, 281,
    283, 293, 307, 311, 313, 317, 331, 337, 347, 349,
    353, 359, 367, 373, 379, 383, 389, 397, 401, 409,
    419, 421, 431, 433, 439, 443, 449, 457, 461, 463,
    467, 479, 487, 491, 499, 503, 509, 521, 523, 541,
    547, 557, 563, 569, 571, 577, 587, 593, 599, 601,
    607, 613, 617, 619, 631, 641, 643, 647, 653, 659,
    661, 673, 677, 683, 691, 701, 709, 719, 727, 733,
    739, 743, 751, 757, 761, 769, 773, 787, 797, 809,
    811, 821, 823, 827, 829, 839, 853, 857, 859, 863,
    877, 881, 883, 887, 907, 911, 919, 929, 937, 941,
    947, 953, 967, 971, 977, 983, 991, 997
];

function integer_value(value, default_value) {
    value = resolve(value);
    return (
        typeof value === "number"
        ? Math.floor(value)
        : (
            typeof value === "string"
            ? value.charCodeAt(0)
            : default_value
        )
    );
}

function integer(i, j) {
    if (i === undefined) {
        return wun_of(primes);
    }
    i = integer_value(i, 1);
    if (j === undefined) {
        j = i;
        i = 1;
    } else {
        j = integer_value(j, 1);
    }
    if (i > j) {
        [i, j] = [j, i];
    }
    return function () {
        return Math.floor(Math.random() * (j + 1 - i) + i);
    };
}
```

**character** 说明符返回一个生成字符的生成器。如果传递一个或两个整数，生成器会生成码点在该范围内的字符。如果传递两个字符串，它返回由每个字符串的第一个码点构成的范围内的字符。如果传递一个字符串，它返回该字符串中的字符。默认是返回 ASCII 字符。

```javascript
function character(i, j) {
    if (i === undefined) {
        return character(32, 126);
    }
    if (typeof i === "string") {
        return (
            j === undefined
            ? wun_of(i.split(""))
            : character(i.codePointAt(0), j.codePointAt(0))
        );
    }
    const ji = integer(i, j);
    return function () {
        return String.fromCodePoint(ji());
    };
}
```

**array** 说明符返回一个生成数组的生成器。

```javascript
function array(first, value) {
    if (Array.isArray(first)) {
        return function () {
            return first.map(resolve);
        };
    }
    if (first === undefined) {
        first = integer(4);
    }
    if (value === undefined) {
        value = integer();
    }
    return function () {
        const dimension = resolve(first);
        const result = new Array(dimension).fill(value);
        return (
            typeof value === "function"
            ? result.map(resolve)
            : result
        );
    };
}
```

如果参数是一个值和生成器的数组，那么结果是一个包含这些值和生成器结果的数组。

```javascript
let my_little_array_specifier = jsc.array([
    jsc.integer(),
    jsc.number(100),
    jsc.string(8, jsc.character("A", "Z"))
]);
```

```
my_little_array_specifier()            // [179,  21.228644298389554, "TJFJPLQA"]
my_little_array_specifier()            // [797,  57.05485427752137,  "CWQDVXWY"]
my_little_array_specifier()            // [941,  91.98980208020657,  "QVMGNVXK"]
my_little_array_specifier()            // [11,   87.07735128700733,  "GXBSVLKJ"]
```

否则，它产生一个值的数组。你可以提供一个维度或一个生成整数的生成器。你也可以提供一个值或一个值的生成器。默认是随机素数。

```javascript
let my_other_little_array_specifier = jsc.array(4);
```

```
my_other_little_array_specifier()  // [659,  383, 991, 821]
my_other_little_array_specifier()  // [479,  701,  47, 601]
my_other_little_array_specifier()  // [389,  271, 113, 263]
my_other_little_array_specifier()  // [251,  557, 547, 197]
```

**string** 说明符返回一个生成字符串的生成器。默认是生成 ASCII 字符的字符串。

```javascript
function string(...parameters) {
    const length = parameters.length;

    if (length === 0) {
        return string(integer(10), character());
    }
    return function () {
        let pieces = [];
        let parameter_nr = 0;
        let value;
        while (true) {
            value = resolve(parameters[parameter_nr]);
            parameter_nr += 1;
            if (value === undefined) {
                break;
            }
            if (
                Number.isSafeInteger(value)
                && value >= 0
                && parameters[parameter_nr] !== undefined
            ) {
                pieces = pieces.concat(
                    new Array(value).fill(parameters[parameter_nr]).map(resolve)
                );
                parameter_nr += 1;
            } else {
                pieces.push(String(value));
            }
        }
        return pieces.join("");
    };
}
```



它也可以接收值和生成器，并将结果连接在一起。

```javascript
let my_little_3_letter_word_specifier = jsc.string(
    jsc.sequence(["c", "d", "f"]),
    jsc.sequence(["a", "o", "i", "e"]),
    jsc.sequence(["t", "g", "n", "s", "l"])
)];

my_little_3_letter_word_specifier() // "cat"
my_little_3_letter_word_specifier() // "dog"
my_little_3_letter_word_specifier() // "fin"
my_little_3_letter_word_specifier() // "ces"
```

如果某个参数产生一个整数后跟一个字符串值，它可以作为长度使用。

```javascript
let my_little_ssn_specifier = jsc.string(
    3, jsc.character("0", "9"),
    "-",
    2, jsc.character("0", "9"),
    "-",
    4, jsc.character("0", "9")
);

my_little_ssn_specifier()            // "231-89-2167"
my_little_ssn_specifier()            // "706-32-0392"
my_little_ssn_specifier()            // "931-89-4315"
my_little_ssn_specifier()            // "636-20-3790"
```

any 说明符返回一个生成器，该生成器返回各种随机类型的值。

```javascript
const misc = [
    true, Infinity, -Infinity, falsy(), Math.PI, Math.E, Number.EPSILON
];

function any() {
    return wun_of([integer(), number(), string(), wun_of(misc)]);
}
```

object 说明符返回一个生成对象生成器。默认是生成具有随机键和随机值的小对象。

```javascript
function object(subject, value) {
    if (subject === undefined) {
        subject = integer(1, 4);
    }
    return function () {
        let result = {};
        const keys = resolve(subject);
        if (typeof keys === "number") {
            const text = string();
            const gen = any();
            let i = 0;
            while (i < keys) {
                result[text()] = gen();
                i += 1;
            }
            return result;
        }
        if (value === undefined) {
            if (keys && typeof keys === "object") {
                Object.keys(subject).forEach(function (key) {
                    result[key] = resolve(keys[key]);
                });
                return result;
            } else {
                const values = resolve(value);
                if (Array.isArray(keys)) {
                    keys.forEach(function (key, key_nr) {
                        result[key] = resolve((
                            Array.isArray(values)
                            ? values[key_nr % values.length]
                            : value
                        ), key_nr);
                    });
                    return result;
                }
            }
        }
    };
}
```

如果给定一个名称数组和一个值，它会使用这些名称作为属性名来创建对象，并为属性赋予该值。例如，我们可以提供一个包含 3 到 6 个名称的数组，其中名称是 4 个小写字母，值是布尔值。

```javascript
let my_little_constructor = jsc.object(
    jsc.array(
        jsc.integer(3, 6),
        jsc.string(4, jsc.character("a", "z"))
    ),
    jsc.boolean()
);

my_little_constructor()
// {"hiyt": false, "rodf": true, "bfxf": false, "ygat": false, "hwqe": false}
my_little_constructor()
// {"hwbh": true, "ndjt": false, "chsn": true, "fdag": true, "hvme": true}
my_little_constructor()
// {"qedx": false, "uoyp": true, "ewes": true}
my_little_constructor()
// {"igko": true, "txem": true, "yadl": false, "avwz": true}
```

如果给定一个对象，它会生成一个具有相同属性名的对象。

```javascript
let my_little_other_constructor = jsc.object({
    left: jsc.integer(640),
    top: jsc.integer(480),
    color: jsc.wun_of(["black", "white", "red", "blue", "green", "gray"])
});

my_little_other_constructor()  // {"left": 305, "top": 360, "color": "gray"}
my_little_other_constructor()  // {"left": 162, "top": 366, "color": "blue"}
my_little_other_constructor()  // {"left": 110, "top": 5, "color": "blue"}
my_little_other_constructor()  // {"left": 610, "top": 61, "color": "green"}
```

### 测试的工作原理

可以组合生成大量测试数据。但如果某些数据形态无法通过这些说明符的组合轻松生成，你也可以轻松创建自己的说明符。它只是一个返回函数的函数。

现在我们来深入了解 JSCheck 的工作原理。

crunch 函数负责处理数字并生成报告。

```javascript
const ctp = "{name}: {class}{cases} cases tested, {pass} pass{fail}{lost}\n";
```

```javascript
function crunch(detail, cases, serials) {
```

遍历所有用例。收集丢失的用例。生成详细报告和摘要。

```javascript
    let class_fail;
    let class_pass;
    let class_lost;
    let case_nr = 0;
    let lines = "";
    let losses = [];
    let next_case;
    let now_claim;
    let nr_class = 0;
    let nr_fail;
    let nr_lost;
    let nr_pass;
    let report = "";
    let the_case;
    let the_class;
    let total_fail = 0;
    let total_lost = 0;
    let total_pass = 0;
```

```javascript
    function generate_line(type, level) {
        if (detail >= level) {
            lines += fulfill(
                " {type} [{serial}] {classification}{args}\n",
                {
                    type,
                    serial: the_case.serial,
                    classification: the_case.classification,
                    args: JSON.stringify(
                        the_case.args
                    ).replace(
                        /^\[/,
                        "("
                    ).replace(
                        /\]$/,
                        ")"
                    )
                }
            );
        }
    }
```

```javascript
    function generate_class(key) {
        if (detail >= 3 || class_fail[key] || class_lost[key]) {
            report += fulfill(
                " {key} pass {pass}{fail}{lost}\n",
                {
                    key,
                    pass: class_pass[key],
                    fail: (
                        class_fail[key]
                        ? " fail " + class_fail[key]
                        : ""
                    ),
                    lost: (
                        class_lost[key]
                        ? " lost " + class_lost[key]
                        : ""
                    )
                }
            );
        }
    }
```

```javascript
    if (cases) {
        while (true) {
            next_case = cases[serials[case_nr]];
            case_nr += 1;
            if (!next_case || (next_case.claim !== now_claim)) {
                if (now_claim) {
                    if (detail >= 1) {
                        report += fulfill(
                            ctp,
                            {
                                name: the_case.name,
                                class: (
                                    nr_class
                                    ? nr_class + " classifications, "
                                    : ""
                                ),
                                cases: nr_pass + nr_fail + nr_lost,
                                pass: nr_pass,
                                fail: (
                                    nr_fail
                                    ? ", " + nr_fail + " fail"
                                    : ""
                                ),
                                lost: (
                                    nr_lost
                                    ? ", " + nr_lost + " lost"
                                    : ""
                                )
                            }
                        );
                        if (detail >= 2) {
                            Object.keys(
                                class_pass
                            ).sort().forEach(
                                generate_class
                            );
                            report += lines;
                        }
                    }
                    total_fail += nr_fail;
                    total_lost += nr_lost;
                    total_pass += nr_pass;
                }
                if (!next_case) {
                    break;
                }
                nr_class = 0;
                nr_fail = 0;
                nr_lost = 0;
                nr_pass = 0;
                class_pass = {};
                class_fail = {};
                class_lost = {};
                lines = "";
            }
            the_case = next_case;
            now_claim = the_case.claim;
            the_class = the_case.classification;
            if (the_class && typeof class_pass[the_class] !== "number") {
                class_pass[the_class] = 0;
                class_fail[the_class] = 0;
                class_lost[the_class] = 0;
                nr_class += 1;
            }
            if (the_case.pass === true) {
                if (the_class) {
                    class_pass[the_class] += 1;
                }
                if (detail >= 4) {
                    generate_line("Pass", 4);
                }
                nr_pass += 1;
            } else if (the_case.pass === false) {
                if (the_class) {
                    class_fail[the_class] += 1;
                }
                generate_line("FAIL", 2);
                nr_fail += 1;
            } else {
                if (the_class) {
                    class_lost[the_class] += 1;
                }
                generate_line("LOST", 2);
                losses[nr_lost] = the_case;
                nr_lost += 1;
            }
        }
    }
    report += fulfill(
        "\nTotal pass {pass}{fail}{lost}\n",
        {
            pass: total_pass,
            fail: (
                total_fail
                ? ", fail " + total_fail
```



# 代码分析与工具介绍

该模块导出一个构造函数，该函数返回一个 jsc 对象。jsc 对象是有状态的，因为它保存了要测试的断言，因此每个用户都应该获得一个全新的实例。reject 值用于标识应被拒绝的试验。

```javascript
const reject = Object.freeze({});
```

我们导出一个 jsc_constructor 函数。check 和 claim 函数是有状态的，因此在这里创建。我冻结构造函数是因为我喜欢冻结事物。

```javascript
export default Object.freeze(function jsc_constructor() {
    let all_claims = [];
```

check 函数是执行实际工作的函数。

```javascript
    function check(configuration) {
        let the_claims = all_claims;
        all_claims = [];
        let nr_trials = (
            configuration.nr_trials === undefined
            ? 100
            : configuration.nr_trials
        );
```

```javascript
        function go(on, report) {
```

调用一个回调函数。

```javascript
            try {
                return configuration[on](report);
            } catch (ignore) {}
        }
```

check 函数检查所有断言。结果会提供给回调函数。

```javascript
        let cases = {};
        let all_started = false;
        let nr_pending = 0;
        let serials = [];
        let timeout_id;
```

```javascript
        function finish() {
            if (timeout_id) {
                clearTimeout(timeout_id);
            }
            const {
                losses,
                summary,
                report
            } = crunch(
                (
                    configuration.detail === undefined
                    ? 3
                    : configuration.detail
                ),
                cases,
                serials
            );
            losses.forEach(function (the_case) {
                go("on_lost", the_case);
            });
            go("on_result", summary);
            go("on_report", report);
            cases = undefined;
        }
```

```javascript
        function register(serial, value) {
```

此函数由断言函数用于注册新用例，也由用例用于报告判决。这两种用途通过序列号相关联。如果 cases 对象已销毁，那么所有迟到的结果都应被忽略。

```javascript
            if (cases) {
                let the_case = cases[serial];
```

如果序列号未曾见过，则注册一个新用例。该用例被添加到 cases 集合中。序列号被添加到 serials 集合中。待处理用例的数量增加。

```javascript
                if (the_case === undefined) {
                    value.serial = serial;
                    cases[serial] = value;
                    serials.push(serial);
                    nr_pending += 1;
                } else {
```

一个现有的用例现在获得其判决。如果它意外地已经有了结果，则抛出异常。每个用例应该只有一个结果。

```javascript
                    if (
                        the_case.pass !== undefined
                        || typeof value !== "boolean"
                    ) {
                        throw the_case;
                    }
```

如果结果是布尔值，则更新用例并发送到 on_pass 或 on_fail。

```javascript
                    if (value === true) {
                        the_case.pass = true;
                        go("on_pass", the_case);
                    } else {
                        the_case.pass = false;
                        go("on_fail", the_case);
                    }
```

此用例不再处于待处理状态。如果所有用例都已生成并给出结果，则完成。

```javascript
                    nr_pending -= 1;
                    if (nr_pending <= 0 && all_started) {
                        finish();
                    }
                }
            }
            return value;
        }
        let unique = 0;
```

处理每个断言。

```javascript
        the_claims.forEach(function (a_claim) {
            let at_most = nr_trials * 10;
            let case_nr = 0;
            let attempt_nr = 0;
```

循环遍历用例的生成和测试。

```javascript
            while (case_nr < nr_trials && attempt_nr < at_most) {
                if (a_claim(register, unique) !== reject) {
                    case_nr += 1;
                    unique += 1;
                }
                attempt_nr += 1;
            }
        });
```

所有用例谓词都已被调用。

```javascript
        all_started = true;
```

如果所有用例都已返回判决，则生成报告。

```javascript
        if (nr_pending <= 0) {
            finish();
```

否则，启动计时器。

```javascript
        } else if (configuration.time_limit !== undefined) {
            timeout_id = setTimeout(finish, configuration.time_limit);
        }
    }
```

claim 函数用于提交每个断言。所有断言在调用 check 函数时被一次性检查。一个断言包含：

- 一个描述性名称，将在报告中显示。
- 一个谓词函数，该函数执行断言并在断言成立时返回 true。
- 一个函数签名数组，指定谓词函数的类型和值。
- 一个可选的分类器函数，它接受签名产生的值，并返回一个字符串用于对试验进行分类，如果谓词不应获得此组生成的参数，则返回 undefined。

```javascript
    function claim(name, predicate, signature, classifier) {
```

一个函数被存入所有断言的集合中。

```javascript
        if (!Array.isArray(signature)) {
            signature = [signature];
        }
```

```javascript
        function the_claim(register, serial) {
            let args = signature.map(resolve);
            let classification = "";
```

如果提供了分类器函数，则使用它来获取分类。如果分类不是字符串，则拒绝该用例。

```javascript
            if (classifier !== undefined) {
                classification = classifier(...args);
                if (typeof classification !== "string") {
                    return reject;
                }
            }
```

创建一个包装 register 函数的判决函数。

```javascript
            let verdict = function (result) {
                return register(serial, result);
            };
```

注册一个表示此试验的对象。

```javascript
            register(serial, {
                args,
                claim: the_claim,
                classification,
                classifier,
                name,
                predicate,
                serial,
                signature,
                verdict
            });
```

调用谓词，传入判决函数和所有用例参数。谓词必须使用判决回调来发出用例结果的信号。

```javascript
            return predicate(verdict, ...args);
        }
        all_claims.push(the_claim);
    }
```

最后，我们构造实例并返回它。

```javascript
    return Object.freeze({
```

指定器：

```javascript
        any,
        array,
        boolean,
        character,
        falsy,
        integer,
        literal,
        number,
        object,
        one_of,
        sequence,
        string,
```

主函数：

```javascript
        check,
        claim
    });
});
```

## Ecomcon

如果一个文件强烈依赖于其他代码，我希望将这些关系的测试放在同一个文件中。确定模块 A 与模块 B 和模块 C 协同工作的唯一方法是在上下文中将它们全部一起运行。

我开发了一个名为 ecomcon（有条件启用注释）的简单工具。我可以将测试和计量以标记注释的形式放入源代码中。

```javascript
//tag code
```

标签可以是任何单词，比如 `test`。它后面可以跟一些 JavaScript 代码。通常，这些注释只是注释，因此会被忽略。它们会在压缩时被移除。`ecomcon` 函数可以启用它们，移除 `// slash slash` 和标签，留下现在可以执行的 JavaScript 代码。

我们可以生成一个特殊的构建版本，包含大量的运行时检查、日志记录和分析。它允许访问通常隐藏在函数作用域中的变量。它可以监控流入和流出的值。它可以测试程序的完整性，确保关键资源未被破坏。

这些注释也可以作为文档，因为它们暴露并演练了文件及其操作的内部机制。

```javascript
function ecomcon(source_string, tag_array)
```

`tag_array` 包含要作为标签启用的字符串。`ecomcon` 函数非常简单。

```javascript
const rx_crlf = /\n|\r\n?/;

const rx_ecomcon = /^\/\/([ a-z A-Z 0-9 _ ]+)\u0020?(.*)$/;
```

```javascript
// 捕获组：
// [1] 已启用的注释标签
// [2] 行的其余部分
```

```javascript
const rx_tag = /^[ a-z A-Z 0-9 _ ]+$/;
```

```javascript
export default Object.freeze(function ecomcon(source_string, tag_array) {
    const tag = Object.create(null);
    tag_array.forEach(
        function (string) {
            if (!rx_tag.test(string)) {
                throw new Error("ecomcon: " + string);
            }
            tag[string] = true;
        }
    );
    return source_string.split(rx_crlf).map(
        function (line) {
            const array = line.match(rx_ecomcon);
            return (
                Array.isArray(array)
                ? (
                    tag[array[1]] === true
                    ? array[2] + "\n"
                    : ""
                )
                : line + "\n"
            );
        }
    ).join("");
});
```



## 优化如何运作

> 以效率之名（未必能真正实现）所犯的编程错误，比其他任何单一原因——包括盲目的愚蠢——都要多。
*威廉·伍尔夫*

按照现代标准，最初几代计算机相当缓慢。由于过迟获得正确答案与未能获得答案可能无法区分，性能优化在编程中变得根深蒂固，成为一种执念。

如今的设备要快得多。因此，性能似乎不再是一个问题。对于大多数应用来说，确实如此。我们的处理器数量超过了需求，而且这些处理器大部分时间都在闲置。我们拥有巨大的过剩容量。

有些事情仍然不够快。有时是因为问题的规模增长快于容量的增长。大数据不断膨胀。即使在 JavaScript 占主导地位的人机交互层面，我们仍然可能体验到缓慢。

当我们响应用户耗时过长时，他们会感到恼怒，接着是沮丧，然后是愤怒。如果我们试图创造满意度和忠诚度，那么我们的系统就必须具有响应性。

因此，仍然有必要关注性能，但我们需要正确处理它。优化很容易让事情变得更糟。

人们普遍认为每一个微小的优化都有帮助，因为所有节省的纳秒会累积起来。事实并非如此。我们只应该在能获得显著改进的地方进行优化。微不足道的优化是浪费时间。优化的全部意义在于节省时间。因此，我们需要优化我们的优化过程。

### 度量

计算机编程也被称为*计算机科学*和*软件工程*。这些是抱负远大的头衔。我们对此的理解还不够深入，不足以真正地进行科学研究和工程实践。我们缺乏理论来回答软件项目管理中最重要的问题：还剩多少缺陷，以及修复它们需要多长时间？

我们的技艺中有太多部分是无法量化的，但我们可以度量性能。我们可以执行一个程序，并观察它花费了多少时间。这些数字可以帮助我们更好地理解我们的系统，或者它们也可能使我们困惑。

一种非常常见的做法是取两个语言特性，将它们都放入循环中，然后测量循环的性能。更快的循环告诉我们应该使用哪个特性。这可能会有问题。

结果可能是毫无意义的。我们是在测试该特性的性能，还是在测试引擎在将该特性隔离并在循环中运行一百万次时的优化能力？这个结果是可移植的吗？其他引擎会有相同的表现吗？更重要的是，未来的引擎会有相同的表现吗？

结果可能无关紧要。在真实程序的上下文中，可能没有可观察到的差异。因此，基于无意义的数据做决定可能是在浪费时间。

我们应该选择那些能让程序具有可读性和可维护性的特性。如果程序运行速度快但同时是破损的，那对我们没有帮助。

### 再次度量

木匠有句谚语：**量两次，切一次**。这看起来很容易优化：量一次，切一次。额外的细致可以减少错误，避免时间和材料的浪费。这是一个巨大的收益。

程序员应该使用这句谚语：**度量，然后切割，然后再度量一次**。在进行优化之前，我们应该首先度量我们想要优化的代码的性能。这样做是为了建立一个基线，并证明该代码正在拖慢整个程序的运行。如果该代码不是性能热点，那么我们就应该寻找其他地方。然后我们仔细优化代码。然后我们再次度量。如果新代码的性能没有比基线显著提升，那么我们就回退更改。它未能带来预期的改进。我们不提交失败的优化。

大多数优化通过添加替代路径和移除通用性，增加了代码的复杂性。这使得代码体积变大，更难维护，也更难充分测试。如果我们能获得显著的速度提升，我们可能会认为这是值得的。*如果没有显著的速度提升，那么我们可以称这个变更为一个缺陷（bug）*。它导致了代码质量的下降，而带来的收益却很小甚至没有。整洁的代码更容易推理和维护。我们应该谨慎地放弃它。

大部分代码对性能的影响可以忽略不计。花时间去优化那些没有拖慢程序的代码是浪费时间。

### 时间黑洞

很少有情况是仅仅摆弄代码就能让它变快的，因为摆弄并没有解决缓慢的根本原因。以下是一些最大的时间黑洞：

- **未能并行化**：Parseq 让我们能够利用宇宙固有的并行性来让我们的程序运行得更快。如果我们相反地让所有事情都顺序执行，我们就放弃了这种优势。在大规模场景下，并行优于顺序。
- **违反转向定律（Law of Turns）**：当我们阻塞处理循环时，这会给未来发生的每件事增加延迟，直到队列最终变空。延迟的积累可能使队列永远无法清空。
- **弱内聚性**：如果我们的模块没有高内聚性，那么它们很可能在做一些我们可能不需要的事情。不必要的工作会拖慢速度。
- **紧耦合**：当模块紧耦合时，我们就放弃了局部性。这可能导致过度繁琐的协议，从而给每个处理步骤增加网络延迟。
- **错误的算法**：一个随意构建的 $O(n \log n)$ 函数在 $n$ 很大时很容易胜过一个精心制作、巧妙优化的 $O(n^2)$ 函数。当 $n$ 很小时，哪个更快通常并不重要。
- **颠簸（Thrashing）**：这曾经是虚拟内存系统中的一个问题，我们在网络缓存中仍然能看到它。有太多垃圾数据从网络流经缓存，导致有用的数据在能够被重用之前就被清除了。
- **臃肿（Bloat）**：当代码庞大而臃肿时，我们不太可能完全理解它在做什么。它可能在做远超必要的工作。不要专注于执行速度；而应专注于代码体积。
- **他人的代码**：你的代码可能依赖于其他包、库、平台、浏览器、服务器和操作系统。我不知道你必须与什么一起运行，但我确信摆弄你的代码不会让他们的代码运行得更快。如果你的代码能在零时间内执行，大多数网络用户也不会察觉到太大差异。

### 语言

也许最好的优化投资是在语言引擎上。在那里进行的优化惠及该语言的所有用户。这解放了我们，使我们可以专注于编写高质量的程序。引擎机制会让它们变得更快。

最初的 JavaScript 引擎是为了缩短上市时间而优化的。毫不奇怪，它们速度不够快，这促成了 JavaScript 只是一种玩具语言的说法。

即便如此，JavaScript 对于大多数 Web 应用程序来说速度已经足够。浏览器中的大多数性能问题源于对网络的误用——顺序加载资源而不是流水线化。还有 DOM API，它效率极低。DOM 不是 JavaScript 的一部分，但 JavaScript 却因 DOM 的性能而受到指责。尽管 DOM 很糟糕，大多数 Web 应用程序仍然运行得足够好。JavaScript 的执行速度很少是影响因素。

从那时起，JavaScript 引擎已经变得相当快，但情况很复杂。所有简单的优化都已完成。从这一点开始，事情变得越来越复杂。有些优化无疑会在大规模场景下加速程序，但代价是增加启动时间。这正是人们会感到恼怒、沮丧和愤怒的时刻之一。

因此，他们玩一个非常复杂的游戏：用慢速代码快速启动，然后根据程序的行为进行优化。到目前为止，他们在这个游戏中表现得很好，但这很难。他们无法让所有事情都变快。因此，这就变成了一个博弈游戏。他们优化那些他们想象会对最活跃的开发者带来最大收益的功能。

随着语言变得越来越复杂，这个游戏变得更加困难。怪兽的数量只会增加，永远不会减少。最终，复杂性将变得难以承受，游戏将结束。一个更简单、更整洁、更规整的语言将更容易优化。

还存在一个恶劣的反馈循环。引擎让某些特性变得更快。程序员发现了这一点并大量使用这些特性。这确立了一种使用模式，引擎机制会观察并受到这种模式的影响。这个循环正在推动优化投资，但并不一定朝着优化优秀程序的方向发展。



 ## 转译的工作原理

> 我不是那个人。

*尼奥*

JavaScript 的一个重要角色是作为编译目标。*转译*是一种特殊的编译形式，它将一种编程语言转换为另一种语言，通常是 JavaScript。这将 JavaScript 视为一种可移植的可执行格式，利用 JavaScript 的通用性和稳定性。JavaScript 已经成为网络的虚拟机。我们一直以为 Java 的 JVM 会成为网络的虚拟机，但结果却是 JavaScript。JavaScript 的可移植性明显更强，而且速度足以对压缩后的源代码进行词法分析和语法解析。

有时源语言是一种 JavaScript 方言，有时是另一种现有语言，有时则是一种专门为转译而设计的全新语言。

构建转译器有很多原因。

- **实验**：转译器是构建和测试实验性语言及特性的理想方式。可以在 JavaScript 中以更少的时间和精力来测试想法。
- **专业化**：转译器可用于实现为特定目的而设计的小语言。这类语言可以减轻重复性任务的运维负担。
- **遗留**：转译器为那些不够流行、无法享受 JavaScript 覆盖范围的语言提供了一种保护投资的方式。通过转译为 JavaScript，旧程序有可能在任何地方运行。你不需要理解 JavaScript 的工作原理就能使用 JavaScript。（不理解自己在做什么并不是一件好事。）
- **时尚**：程序员可能会沉迷于时尚。转译使得在程序中堆砌花哨的语法成为可能。
- **抢先体验**：新语言特性标准化、实现和广泛部署的速度缓慢且不确定。转译有时可以通过将下一代 JavaScript 转换为当前版本的 JavaScript 来立即使特性可用。这些特性通常是时尚的，而非关键的。但有时时尚等不得。

**安全**：JavaScript 存在许多固有的安全弱点。转译器可以通过移除有问题的特性，同时添加运行时检查和间接层来约束潜在恶意程序，从而缓解这一问题。

**性能**：像 ASM.js 和 Web Assembly 这样的发展试图通过从 JavaScript 中移除所有好的东西来获得执行优势。

*转译器绝不应在生产环境中使用。* 我喜欢转译器在教育和研究中的实用性，但对时尚和一时流行的短视妥协可能在几年后产生严重后果。我的建议是编写出色的 JavaScript 程序。

### Neo

Neo 是一种转译语言。在接下来的章节中，我将展示 Neo 的实现分为以下几个阶段：词法分析、语法分析、代码生成和运行时。

Neo 是一种教学语言。它旨在帮助过渡到下一代语言，通过纠正 JavaScript 的一些最大错误，并移除那些最深深植根于旧范式的特性。特别是，C 语法被移除了。当你固步自封于七十年代时，很难展望未来。

Neo 很像 JavaScript，但也有显著的不同。有些差异是表面的。有些差异则非常深刻：

- 没有保留字。
- 名称可以包含空格。名称可以以 ? *问号* 结尾。
- 注释使用 # *井号*。注释在一行结束时终止。
- Neo 无分号，且空白符有意义。长语句可以在 ( *左括号*、[ *左方括号*、{ *左花括号*、ƒ *弗罗林* 之后断行。
- Neo 的优先级层次更少。运算符优先级减少了对括号的需求，但如果优先级层次太多，可能难以全部记住，这会导致错误。这些层次从弱到强如下：
  - 0. ? ! *三元* | | *默认*
  - 1. ∧ *逻辑与* ∨ *逻辑或*
  - 2. = *等于* ≠ *不等于* < *小于* > *大于* ≤ *小于等于* ≥ *大于等于*
  - 3. ~ *连接* ≈ *带空格连接*
  - 4. + *加* − *减* << *最小值* >> *最大值*
  - 5. × *乘* / *除*
  - 6. . *细化* [ ] *下标* ( ) *调用*
- null 将 null、undefined 和 NaN 统一为单个对象，消除了关于何时使用哪个的困惑。null 是一个不可变的空对象。从 null 获取属性不会失败，它只是产生 null，因此路径表达式可以工作。尝试修改或调用 null 将会失败。
- 没有前缀运算符。取而代之的是一元函数。表面上的区别是函数需要括号，而运算符的括号是可选的。函数更灵活，因此我们完全采用函数来消除困惑的来源。我保留其他运算符。如果我用函数替换所有运算符，那么很有可能我会意外地重新发明 LISP。这倒不是坏事。
- Neo 只有一种数字类型：Big Decimal。这意味着十进制运算可以精确进行。JavaScript 能精确表示的每一个数值也都被包含在内。因为数字很大，所以不需要 MIN_VALUE、EPSILON、MAX_SAFE_INTEGER、MAX_VALUE，也不需要 Infinity。

```
0.1 + 0.2 = 0.3 # 终于成真
```

- 字符序列称为 text。
- Neo 有一种称为 record 的数据类型，它统一了 JavaScript 的对象和 weakmap。我们现在可以自由地使用 object 这个术语来包含语言中的所有类型。record 不继承。record 是字段的容器。字段有一个可以是 text、record 或 array 的键。字段有一个可以是除 null 外的任何值的值。将字段的值改为 null 会从 record 中删除该字段。
- 数组由数组字面量和 `array(dimension)` 函数创建，该函数创建新数组，设置长度，并将元素初始化为 null。下标是小于维度的非负整数。尝试在该范围之外存储会导致失败。数组可以用 let 的特殊形式追加，这也会将维度增加 1。

```
def my little array: array(10)
let my little array[10]: 666 # 失败
let my little array[]: 555

my little array[0] # null
my little array[10] # 555
length(my little array) # 11
```

- `stone` 函数替代了 `Object.freeze` 函数，进行深度冻结。freeze 的问题在于它创造了 unfeeze 或 thaw 的期望。石化之后无法复原。
- 三元运算符使用 ? 和 !。条件必须是布尔值。

```
call (
    my hero = "monster"
    ? blood curdling scream
    ! (
        my hero = "butterfly" ∨ my hero = "unicorn"
        ? do not make a sound
        ! sing like a rainbow
    )
)()
```

- 短路逻辑运算符是 ∧ *反斜杠* 表示 and，∨ *反斜杠* 表示 or。逻辑非是一元函数。如果给 ∧、∨ 和非提供非布尔值，它们会失败。
- 包含以下一元算术函数：`abs`、`fraction`、`integer` 和 `neg`。它们是一元函数，不是运算符。注意 `-` *减号* 用于否定时只对数字字面量有效。
- `+` *加号* 运算符执行加法，而非连接。其他算术运算符是 `-` *减号* 用于减法、`×` *乘号* 用于乘法、`/` *斜线* 用于除法、`>>` *大于大于* 用于最大值、`<<` *小于小于* 用于最小值。
- `~` *波浪号* 运算符执行连接。`≈` *双波浪号* 运算符执行带分隔空格的连接。

```
"Hello" ~ "World"    # "HelloWorld"
"Hello" ≈ "World"    # "Hello World"
"Hello" ≈ ""         # "Hello"
"Hello" ≈ null       # null
```

它们尝试将操作数强制转换为 text。

- 位运算函数对任意大小的整数进行操作：`bit mask`、`bit shift up`、`bit shift down`、`bit and`、`bit or` 和 `bit xor`。
- `typeof` 运算符被替换为以下谓词函数：`array?`、`boolean?`、`function?`、`number?`、`record?`、`text?`。
- `Number.isInteger` 和 `Number.isSafeInteger` 函数被替换为 `integer?` 函数。
- `Object.isFrozen` 函数被替换为 `stone?` 函数。
- `char` 函数接受一个码点并返回 text。
- `code` 函数接受一个 text 并返回第一个码点。
- `length` 函数接受 array 或 text，并返回元素数或字符数。
- `array` 函数创建数组。其工作方式取决于其参数。
- 如果参数是非负整数，则创建该维度的数组。如果提供了另一个参数：
- 如果是 `null`，所有元素初始化为 `null`。
- 如果是函数，则调用该函数为元素生成初始化值。
- 否则它提供元素的初始化值。
- 如果参数是 array 且下一个参数是函数，则对 array 进行映射。
- 如果参数是 array，则创建 array 的浅拷贝。附加参数可以给出用于复制 array 部分的起始和结束位置。
- 如果参数是 record，则创建 text 键的数组。
- 如果参数是 text 且有第二个参数，则第二个参数用于将 text 分割为 text 数组。
- `number` 函数接受 text 并返回数字。它可以接受可选的基数。
- `record` 函数创建 record。其工作方式取决于其参数。



## 转译工作原理

+   • 若参数为数组，则使用数组的元素作为键。值则取决于另一个参数：
    • 若为 null，则所有值均为 true。这有时被称为*集合*。
    • 若为数组，则其元素即为值。两个数组应具有相同的长度。
    • 若为函数，则使用该函数来生成值。
    • 否则，该参数将用作所有字段的初始值。

+   • 若参数为记录，则创建该记录的浅拷贝，仅复制文本键。如果还有另一个参数是键数组，则只复制这些键。

+   • 若参数为 null，则创建一个空记录。

+   • text 函数用于创建文本。其工作方式取决于参数。
    • 若为数字，则将其转换为文本。可接受可选的基数参数。
    • 若为数组，则将所有元素连接起来。另一个参数可提供分隔符文本。
    • 若为文本，另外两个参数可指定子文本。遗憾的是，这些参数指定的是码元。理想情况下，文本内部应表示为 UTF-32。我们可能需要等到下一门语言才能实现这一点。

+   • 函数对象使用 $f_{florin}$ 运算符创建。有两种形式：
$f_{florin}$ *参数列表* (*表达式*)

$f_{florin}$ *参数列表* {
    *函数体*
}

+   • *参数列表* 是一个以逗号分隔的名称、可选默认值和 ...*省略号* 的列表。函数是匿名的。要给函数命名，请使用 **def** 语句。函数对象是不可变的。

+   • 函数表达式返回表达式的值。函数体必须显式 **return** 一个值。

+   • 默认运算符为 |*表达式*|。如果紧邻左侧的表达式或参数值为 null，则计算右侧用竖线包裹的 *表达式* 以产生默认值。它是短路求值的。

+   • ...*省略号* 与 JavaScript 中的类似，但始终放在数组项之后，而非之前...
def continuiize: $f_{florin}$ any (
    $f_{florin}$ callback, arguments... (callback(any(arguments...)))
)

+   • 在运算符前使用 $f_{florin}$ 会产生一个 *函数*，允许将该运算符用作普通函数。因此 $f_{florin}$+ 创建一个二元加法函数，可以传递给 reduce 函数以实现求和。$f_{florin}$+(3, 4) 返回 7。

### 25.5 转译工作原理

$f\wedge$ 与 $f\vee$ 或 $f=$ 等于 $f\neq$ 不等于 $f<$ 小于 $f\geq$ 大于或等于 $f>$ 大于 $f\leq$ 小于或等于 $f\sim$ 连接 $f\approx$ 连接空格 $f+$ 加 $f-$ 减 $f>>$ 最大值 $f<<$ 最小值 $f*$ 乘 $f/$ 除 $f[]$ 获取 $f()$ 解析 $f?!$ 三元 $f||$ 默认

• 函数可以作为方法被调用。例如：
  my little function.method(x, y)
等同于
  my little function("method", [x, y])
这种简单的机制使得可以将函数用作记录的代理。

• def 语句取代了 const 语句。

• var 语句用于声明变量。

• let 语句可以更改变量的值，或记录的一个字段，或数组的一个元素。let 语句是唯一允许进行修改的地方。没有赋值运算符。我无法消除赋值，但我可以对其进行约束。
  def pi: 3.14159265358979323846264338327950288419716939937510582097494459
  var counter: 0
  let counter: counter + 1

• 没有块级作用域，因为没有块。有函数作用域。

• call 语句允许调用函数并忽略其返回值。
  call my little impure side effect causer()

• Neo 有 if 和 else。它还有 else if 作为 switch 语句的替代。如果条件表达式不产生布尔值，则会失败。没有 falsy 值。
  if my hero = "monster"
      call blood curdling scream()
  else if my hero = "butterfly" $\vee$ my hero = "unicorn"
      call do not make a sound()
  else
      call sing like a rainbow()

• loop 语句取代了 do、for 和 while 语句。我想避免使用循环。loop 是一个简单的无限循环。使用 break 或 return 来退出。循环不能有标签。循环可以嵌套。不能在循环内创建新函数。

• 异常被故障（failure）取代。函数可以有故障处理器。没有 try。
  def my little function: $f$ x the unknown {
      return risky operation(x the unknown)
  failure
      call launch all missiles()
      return null
  }

• fail 语句表示一个故障。它不接受异常对象或任何其他类型的消息。如果必须传达故障原因，请在 fail 之前通过其他方式记录它。

+   - 模块可以有多个 `import` 语句：
  `import name: text literal`
- 模块可以有一个 `export` 语句：
  `export expression`

### 示例

这是 Neo 中的 `reduce reverse` 函数。它允许提前退出，并且是反向处理的。它接受 3 个参数：数组、回调函数和初始值。回调函数接收 4 个值：归约的当前值、当前数组元素、当前元素的索引号以及一个退出函数。如果回调函数想要提前停止，它返回调用退出函数并传入最终值的结果。

```
def reduce reverse: f array, callback function, initial value {

# 将数组归约为单个值。

# 如果未提供初始值，则使用第零个元素
# 并跳过第一次迭代。

    var element nr: length(array)
    var reduction: initial value
    if reduction = null
        let element nr: element nr - 1
        let reduction: array[element nr]

# 回调函数获得一个退出函数，可以调用它
# 来停止操作。

    def exit: f final value {
        let element nr: 0
        return final value
    }

# 循环直到数组耗尽或请求提前退出。
# 在每次迭代中，调用回调函数并传入下一个递增的值。

    loop
        let element nr: element nr - 1
        if element nr < 0
            break
        let reduction: callback function(
            reduction
            array[element nr]
            element nr
            exit
        )
    return reduction
}
```

## 下一门语言

Neo 不是下一门语言。它甚至不是一门完整的语言。它缺少很多基本的东西。这本身并不是一个严重的问题，因为我们知道向一门语言添加东西很容易。

Neo 缺少 JSON 支持。任何一门严肃的 21 世纪语言都不能缺少内置的 JSON 编码和解码。

Neo 缺少某种形式的文本模式匹配。JavaScript 使用正则表达式来实现此目的。下一门语言应以一种不那么晦涩的记法来支持上下文无关语言。

下一门语言应有更好的 Unicode 支持。例如，应该有某种形式的 split，它能识别组合字符，将文本拆分为字形。

下一门语言应使用 UTF-32 作为其内部字符表示。这可能看起来极其奢侈。我记得当为一个字符使用 8 位被认为是奢侈的时候。那是在内存以千字节计量的时代。如今内存以吉字节计量。内存变得如此之大，以至于字符的大小无关紧要。使用 UTF-32，码元和码点之间的差异消失了，使得编写在国际上正确运行的程序变得更容易。

下一门语言应直接支持 blob。有些数据就是需要又大又乱、封装良好且神秘莫测。

下一门语言应更好地支持最终编程（eventual programming），包括一个处理循环和消息分发与有序传递的机制。

下一门语言应更好地支持安全网络。

下一门语言应支持进程管理：启动、通信和销毁。应该能够将进程链接在一起形成自杀协议。如果一个失败，它们都会失败，从而有机会将它们重新启动到全新状态。

下一门语言应支持纯函数的并行处理。CPU 不会变得更快，但它们的数量会更多。最终，最大的性能提升来自并行化。

Neo 不是下一门语言，但它可以帮助我们不要害怕下一个范式。接下来我们构建 Neo。



### 分词的工作原理

永远别让人类去做机器该做的工作。

*特工史密斯*

处理程序的第一步是将其拆分为**词法单元（token）**。词法单元由一系列字符组成，它们构成了源代码中有意义的部分，例如**名称**、**标点符号**、**数字字面量**或**文本字面量**。我们为程序中的每个词法单元创建一个词法单元对象。

我们使用**正则表达式**将源文本拆分为行，再将行拆分为词法单元。

```
const rx_unicode_escapement = /
    \\u \{ ( [ 0-9 A-F ]{4,6} ) \}
/g;
```

`rx_crlf` 匹配换行符、回车符，以及回车换行符组合。我们仍在折腾 20 世纪中期机电式电传打字机的设备代码。

```
const rx_crlf = /
    \n
|
    \r \n?
/;
```

`rx_token` 匹配一个 Neo 词法单元：**注释**、**名称**、**数字**、**字符串**、**标点符号**。

```
const rx_token = /
    ( \u0020+ )
|
    ( # .* )
|
    (
        [ a-z A-Z ]
        (?:
            \u0020 [ a-z A-Z ]
        |
            [ 0-9 a-z A-Z ]
        )*
        \??
    )
|
    (
        -? \d+
```

```
    (?: \. \d+ )?
    (?: e \-? \d+ )?
  )
  |
  ( "
    (?:
      [^ " \\ ]
      |
      \\
      (?:
        [ n r " \\ ]
        |
        u \{ [ 0-9 A-F ]{4,6} \}
      )
    )*
  "
  )
  |
  (
    \. (?: \. \. )?
  |
  V \\?
  |
  \\ V?
  |
  > >?
  |
  < <?
  |
  \[ \]?
  |
  \{ \}?
  |
  [ ( ) } \] . , : ? ! ; ~ ~ = ≠ ≤ ≥ & | + \- * % f $ @ \^ _ ' ` ]
  )
  /y;
```

// 捕获组
// [1] 空白字符
// [2] 注释
// [3] 字母数字名称
// [4] 数字
// [5] 字符串
// [6] 标点符号

我们导出一个分词器工厂。

```
export default Object.freeze(function tokenize(source, comment = false) {
```

`tokenize` 接收一个源文件，并从中生成一个词法单元对象数组。如果源文件不是数组，则会在回车/换行符处将其拆分为行。如果 `comment` 为 `true`，则注释也会作为词法单元对象包含在内。解析器不想看到注释，但软件工具可能需要。

```
  const lines = (
    Array.isArray(source)
    ? source
    : source.split(/\r?\n/)
  );
```

```
: source.split(rx_crlf)
);
let line_nr = 0;
let line = lines[0];
rx_token.lastIndex = 0;
```

该工厂返回一个**生成器**，将行拆分为词法单元对象。词法单元对象包含 `id`、坐标以及其他信息。**空白字符不会被分词**。每次调用词法单元生成器时，它都会产生下一个词法单元。

```
return function token_generator() {
    if (line === undefined) {
        return;
    }
    let column_nr = rx_token.lastIndex;
    if (column_nr >= line.length) {
        rx_token.lastIndex = 0;
        line_nr += 1;
        line = lines[line_nr];
        return (
            line === undefined
            ? undefined
            : token_generator()
        );
    }
    let captives = rx_token.exec(line);
```

没有匹配到任何内容。

```
if (!captives) {
    return {
        id: "(error)",
        line_nr,
        column_nr,
        string: line.slice(column_nr)
    };
}
```

匹配到了空白字符。

```
if (captives[1]) {
    return token_generator();
}
```

匹配到了注释。

```
if (captives[2]) {
    return (
        comment
        ? {
            id: "(comment)",
            comment: captives[2],
            line_nr,
            column_nr,
            column_to: rx_token.lastIndex
        }
        : token_generator()
    );
}
```

匹配到了名称。

```
if (captives[3]) {
    return {
        id: captives[3],
        alphameric: true,
        line_nr,
        column_nr,
        column_to: rx_token.lastIndex
    };
}
```

匹配到了数字字面量。

```
if (captives[4]) {
    return {
        id: "(number)",
        readonly: true,
        number: big_float.normalize(big_float.make(captives[4])),
        text: captives[4],
        line_nr,
        column_nr,
        column_to: rx_token.lastIndex
    };
}
```

匹配到了文本字面量。

```
if (captives[5]) {
```

我们使用 `.replace` 将 `\u{xxxxxx}` 转换为码点，并使用 `JSON.parse` 来处理剩余的转义字符并移除引号。

```
return {
    id: "(text)",
    readonly: true,
    text: JSON.parse(captives[5].replace(
        rx_unicode_escapement,
        function (ignore, code) {
            return String.fromCodePoint(parseInt(code, 16));
        }
    )),
    line_nr,
    column_nr,
    column_to: rx_token.lastIndex
};
```

```
}
}
```

匹配到了标点符号。

```
if (captives[6]) {
    return {
        id: captives[6],
        line_nr,
        column_nr,
        column_to: rx_token.lastIndex
    };
}
```

```
});
});
```

#### 解析的工作原理

有些人认为我们缺乏描述你完美世界的编程语言。但我相信，作为一个物种，人类通过**痛苦**和**苦难**来定义他们的现实。

*特工史密斯*

在解析中，我们将词法单元对象流编织成一棵**树**。在解析操作期间，我们还会查找源代码中的错误。词法单元对象会被添加新的属性。最重要的是 `zeroth`、`wunth` 和 `twoth` 属性，它们构成了树的结构。例如，加法运算的两个操作数保存在 `+` 词法单元的 `zeroth` 和 `wunth` 属性中。`if` 词法单元将条件表达式保存在 `zeroth` 中，将 `then` 子句保存在 `wunth` 中，将 `else` 子句保存在 `twoth` 中。还会有其他属性，我们将在后续过程中逐步发现它们。

我们使用 `error` 函数报告错误。本可以让它保留错误列表并继续，但我想在第一个错误后就停止。当处于**开发模式**时，我希望错误能将编辑器的光标移动到下一个问题。当处于**构建模式**时，我在寻找通过或失败，而不是一个列表。

```
let the_error;

function error(zeroth, wunth) {
    the_error = {
        id: "(error)",
        zeroth,
        wunth
    };
    throw "fail";
}
```

`primordial` 对象包含语言内置的对象。这包括像 `true` 这样的常量以及像 `neg` 这样的函数。`primordial` 对象使用 `Object.create(null)` 创建，因为我不想让原型链污染该对象。例如，`Object.prototype` 包含一个 `valueOf` 方法，但我不想继承它，因为这可能会给人一种向语言添加了原始 `valueOf` 的印象。

```
const primordial = (function (ids) {
    const result = Object.create(null);
    ids.forEach(function (id) {
```

```
result[id] = Object.freeze({
    id,
    alphaneric: true,
    readonly: true
});
});
return Object.freeze(result);
}([
    "abs", "array", "array?", "bit and", "bit mask", "bit or", "bit shift down",
    "bit shift up", "bit xor", "boolean?", "char", "code", "false", "fraction",
    "function?", "integer", "integer?", "length", "neg", "not", "number",
    "number?", "null", "record", "record?", "stone", "stone?", "text", "text?",
    "true"
]));
```

`readonly` 属性会阻止 `let` 语句。

在我们推进流的过程中，总有三个词法单元可见。生成器函数提供词法单元对象流。`prev_token`、`token` 和 `next_token` 三个词法单元可见。`advance` 函数使用生成器遍历所有词法单元对象，跳过注释。

```
let the_token_generator;
let prev_token;
let token;
let next_token;

let now_function;        // 当前正在处理的函数。
let loop;                // 循环退出状态数组。

const the_end = Object.freeze({
    id: "(end)",
    precedence: 0,
    column_nr: 0,
    column_to: 0,
    line_nr: 0
});
```

`advance` 函数推进到下一个词法单元。它的伴侣 `prelude` 函数尝试将当前词法单元拆分为两个词法单元。

```
function advance(id) {
    使用词法单元生成器推进到下一个词法单元。如果提供了 id，确保
    当前词法单元匹配该 id。

        if (id !== undefined && id !== token.id) {
            return error(token, "expected '" + id + "'");
        }
        prev_token = token;
        token = next_token;
        next_token = the_token_generator() || the_end;
}

function prelude() {
```

如果 `token` 包含空格，将其拆分，将第一部分放入 `prev_token`。否则，推进。



#### 27.3 解析的工作原理

在这个语言中，空格具有重要意义。换行可以表示一个语句或元素的结束。缩进可以表示一个子句的结束。以下函数帮助管理这些规则。

```javascript
let indentation;

function indent() {
    indentation += 4;
}

function outdent() {
    indentation -= 4;
}

function at_indentation() {
    if (token.column_nr !== indentation) {
        return error(token, "expected at " + indentation);
    }
}

function is_line_break() {
    return token.line_nr !== prev_token.line_nr;
}

function same_line() {
    if (is_line_break()) {
        return error(token, "unexpected linebreak");
    }
}

function line_check(open) {
    return (
        open
        ? at_indentation()
        : same_line()
    );
}
```

`register` 函数在函数作用域中声明一个新变量。`lookup` 函数在最相关的作用域中查找一个变量。

```javascript
function register(the_token, readonly = false) {
    if (now_function.scope[the_token.id] !== undefined) {
        error(the_token, "already defined");
    }
    the_token.readonly = readonly;
    the_token.origin = now_function;
    now_function.scope[the_token.id] = the_token;
}
```

向当前作用域添加一个变量。

```javascript
function lookup(id) {
    let definition = now_function.scope[id];
    if (definition === undefined) {
        let parent = now_function.parent;
        while (parent !== undefined) {
            definition = parent.scope[id];
            if (definition !== undefined) {
                break;
            }
            parent = parent.parent;
        }
    }
    if (definition === undefined) {
        definition = primordial[id];
    }
    if (definition !== undefined) {
        now_function.scope[id] = definition;
    }
    return definition;
}
```

在当前作用域中查找定义。

如果失败，则搜索祖先作用域。

如果失败，则搜索原始定义。

记住，当前函数使用了这个定义。

`origin` 属性记录了创建该变量的函数。`scope` 属性保存了函数中创建或使用的所有变量。`parent` 属性指向创建此函数的函数。

三个对象包含了用于解析语言特性的函数：语句、前缀和后缀。

`parse_statement`、`parse_prefix` 和 `parse_suffix` 对象包含执行专门解析的函数。我们使用 `Object.create(null)` 创建它们，因为我们不希望从 `Object.prototype` 带来任何额外的东西。

```javascript
const parse_statement = Object.create(null);
const parse_prefix = Object.create(null);
const parse_suffix = Object.create(null);
```

`expression` 函数（及其辅助函数 `argument_expression`）是此解析器的核心。一个表达式可以看作有两个部分：左部分和可选的右部分。左部分是一个字面量、变量或前缀元素。右部分是一个后缀运算符，后面可能跟着另一个表达式。如果右侧有一个后缀，并且它具有更高的优先级，那么左部分将传递给右部分的解析器，产生一个新的左部分。右部分的解析器可能会再次调用 **expression** 函数，可能使用不同的优先级。

表达式可以是开放的或封闭的。如果是封闭的，表达式必须完全在同一行内。开放表达式应从正确的缩进处开始，并且在后缀之前可以有换行。

`expression` 函数是此解析器的核心。它使用了一种称为自顶向下运算符优先级的技术。

它接受一个可选的 `open` 参数，允许容忍某些换行。如果 **open** 为真，我们期望标记位于缩进点。

```javascript
function argument_expression(precedence = 0, open = false) {
    let definition;
    let left;
    let the_token = token;

    // 标记是数字字面量还是文本字面量？
    if (the_token.id === "(number)" || the_token.id === "(text)") {
        advance();
        left = the_token;

    // 标记是字母数字吗？
    } else if (the_token.alphameric === true) {
        definition = lookup(the_token.id);
        if (definition === undefined) {
            return error(the_token, "expected a variable");
        }
        left = definition;
        advance();
    } else {
        // 标记可能是一个前缀元素：(, [, {, f。
        definition = parse_prefix[the_token.id];
        if (definition === undefined) {
            return error(the_token, "expected a variable");
        }
        advance();
        left = definition.parser(the_token);
    }

    // 我们已经得到了左部分。右边是否有后缀运算符？优先级是否允许消费该运算符？如果是，则将左右部分组合以形成新的左部分。
    while (true) {
        the_token = token;
        definition = parse_suffix[the_token.id];
        if (
            token.column_nr < indentation
            || (!open && is_line_break())
            || definition === undefined
            || definition.precedence <= precedence
        ) {
            break;
        }
        line_check(open && is_line_break());
        advance();
        the_token.class = "suffix";
        left = definition.parser(left, the_token);
    }

    // 经过零次或多次循环后，我们可以返回表达式的解析树。
    return left;
}

function expression(precedence, open = false) {
    // 表达式进行空白检查，而参数表达式不需要。
    line_check(open);
    return argument_expression(precedence, open);
}
```

`precedence` 属性决定了后缀运算符的解析方式。`parser` 属性是一个用于解析前缀或后缀的函数。`class` 属性是 "suffix"、"statement" 或 undefined。

让我们看一个简单的后缀运算符。点解析器被传递左表达式和点标记。它验证左表达式是否有效。它验证当前标记是否是一个名称。然后将它们组装成点标记并返回。

```javascript
function parse_dot(left, the_dot) {
    // 左边的表达式必须是一个变量或可以返回对象的表达式（不包括对象字面量）。
    if (
        !left.alphanumeric
        && left.id !== "."
        && (left.id !== "[" || left.wunth === undefined)
        && left.id !== "("
    ) {
        return error(token, "expected a variable");
    }
    let the_name = token;
    if (the_name.alphameric !== true) {
        return error(the_name, "expected a field name");
    }
    the_dot.zeroth = left;
    the_dot.wunth = the_name;
    same_line();
    advance();
    return the_dot;
}
```

`[]` 下标解析器更有趣一些。它被传递左表达式和左方括号标记。它验证左表达式是否有效。然后调用 `expression` 来获取方括号中的内容。如果在左方括号之后有换行，则这是一个开放表达式。它前进到关闭的右方括号之后。

```javascript
function parse_subscript(left, the_bracket) {
    if (
        !left.alphanumeric
        && left.id !== "."
        && (left.id !== "[" || left.wunth === undefined)
        && left.id !== "("
    ) {
        return error(token, "expected a variable");
    }
    the_bracket.zeroth = left;
    if (is_line_break()) {
        indent();
        the_bracket.wunth = expression(0, true);
        outdent();
        at_indentation();
    } else {
        the_bracket.wunth = expression();
        same_line();
    }
    advance("]");
    return the_bracket;
}
```

省略号解析器不像其他后缀运算符那样打包，因为它只允许在三个地方使用：参数列表、参数列表和数组字面量。在其他任何地方都不允许，因此我们将其视为特殊情况。

```javascript
function ellipsis(left) {
    if (token.id === "...") {
        const the_ellipsis = token;
        same_line();
        advance("...");
        the_ellipsis.zeroth = left;
        return the_ellipsis;
    }
    return left;
}
```

`( )` *调用* 解析器解析函数调用。它为每个参数调用 `argument_expression`。开放形式的调用会垂直列出参数，不使用逗号。

```javascript
function parse_invocation(left, the_paren) {

    // 函数调用：
    //     表达式
    //     表达式...

    const args = [];
    if (token.id === ")") {
        same_line();
    } else {
        const open = is_line_break();
        if (open) {
            indent();
        }
        while (true) {
            line_check(open);
            args.push(ellipsis(argument_expression()));
```



#### 解析的工作原理

```javascript
if (token.id === ")" || token === the_end) {
    break;
}
if (!open) {
    same_line();
    advance(",");
}
if (open) {
    outdent();
    at_indentation();
} else {
    same_line();
}
advance(")");
the_paren.zeroth = left;
the_paren.wunth = args;
return the_paren;
}
```

后缀函数用于构建 `parse_suffix` 数组。它接受一个操作符、一个优先级和一个可选的解析器。它可以提供一个适用于大多数操作符的默认解析器函数。

```javascript
function suffix(
    id,
    precedence,
    optional_parser = function infix(left, the_token) {
        the_token.zeroth = left;
        the_token.wunth = expression(precedence);
        return the_token;
    }
) {
    const the_symbol = Object.create(null);
    the_symbol.id = id;
    the_symbol.precedence = precedence;
    the_symbol.parser = optional_parser;
    parse_suffix[id] = Object.freeze(the_symbol);
}
```

创建一个中缀或后缀操作符。

```javascript
suffix("|", 111, function parse_default(left, the_bar) {
    the_bar.zeroth = left;
    the_bar.wunth = expression(112);
    advance("|");
    return the_bar;
});
suffix("?", 111, function then_else(left, the_then) {
    the_then.zeroth = left;
    the_then.wunth = expression();
    advance("!");
    the_then.twoth = expression();
    return the_then;
});
suffix("/\\", 222);
suffix("\\/", 222);
suffix("~", 444);
suffix("~", 444);
suffix("+", 555);
suffix("-", 555);
suffix("<<", 555);
suffix(">>", 555);
suffix("*", 666);
suffix("/", 666);
suffix(".", 777, parse_dot);
suffix("[", 777, parse_subscript);
suffix("(", 777, parse_invocation);
```

我们对关系运算符的处理略有不同，以防止出现 *a < b ≤ c* 这样的错误。

```javascript
const rel_op = Object.create(null);

function relational(operator) {
    rel_op[operator] = true;
    return suffix(operator, 333, function (left, the_token) {
        the_token.zeroth = left;
        the_token.wunth = expression(333);
        if (rel_op[token.id] === true) {
            return error(token, "unexpected relational operator");
        }
        return the_token;
    });
}

relational("=");
relational("!");
relational("<");
relational(">");
relational("<=");
relational(">=");
```

前缀函数用于构建 `parse_prefix` 数组。注意，( *左圆括号* 和 [ *左方括号* 也在 `parse_suffix` 数组中。这没有问题。不存在歧义。前缀运算符不需要优先级。

```javascript
function prefix(id, parser) {
    const the_symbol = Object.create(null);
    the_symbol.id = id;
    the_symbol.parser = parser;
    parse_prefix[id] = Object.freeze(the_symbol);
}

prefix("(", function (ignore) {
    let result;
    if (is_line_break()) {
        indent();
        result = expression(0, true);
        outdent();
        at_indentation();
    } else {
        result = expression(0);
        same_line();
    }
    advance(")");
    return result;
});
```

数组字面量解析器为每个元素调用 `expression` 函数。元素可以是任何表达式，后面可选择性地跟上 `...`（点点点）。编写数组字面量有三种方式：

- **空：** [ *左方括号* ] *右方括号*，一个长度为零的数组。
- **封闭：** 整个字面量在同一行，用逗号分隔。
- **开放：** [ *左方括号* 之后换行，增加缩进，] *右方括号* 恢复之前的缩进，表达式之间用 , *逗号* 或 ; *分号* 和/或换行符分隔。

; *分号* 可以创建二维数组。

```javascript
    [[2, 7, 6], [9, 5, 1], [4, 3, 8]]
```

可以写成

```javascript
    [2, 7, 6; 9, 5, 1; 4, 3, 8]
```

```javascript
    prefix("[", function arrayliteral(the_bracket) {
        let matrix = [];
        let array = [];
        if (!is_line_break()) {
            while (true) {
                array.push(ellipsis(expression()));
                if (token.id === ",") {
                    same_line();
                    advance(",");
                } else if (
                    token.id === ";"
                    && array.length > 0
                    && next_token !== "]"
                ) {
                    same_line();
                    advance(";");
                    matrix.push(array);
                    array = [];
                } else {
                    break;
                }
            }
            same_line();
        } else {
            indent();
            while (true) {
                array.push(ellipsis(expression(0, is_line_break())));
                if (token.id === "]" || token === the_end) {
                    break;
                }
                if (token.id === ";") {
                    if (array.length === 0 || next_token.id === "]") {
                        break;
                    }
                    same_line();
                    advance(";");
                    matrix.push(array);
                    array = [];
                } else if (token.id === "," || !is_line_break()) {
                    same_line();
                    advance(",");
                }
            }
            outdent();
            if (token.column_nr !== indentation) {
                return error(token, "expected at " + indentation);
            }
        }
        advance("]");
        if (matrix.length > 0) {
            matrix.push(array);
            the_bracket.zeroth = matrix;
        } else {
            the_bracket.zeroth = array;
        }
        return the_bracket;
    });

    prefix("[]", function emptyarrayliteral(the_brackets) {
        return the_brackets;
    });
```

记录字面量解析器识别 4 种字段形式。

- 变量
- name: expression
- "string": expression
- [expression]: expression

```javascript
    prefix("{", function recordliteral(the_brace) {
        const properties = [];
        let key;
        let value;
        const open = the_brace.line_nr !== token.line_nr;
        if (open) {
            indent();
        }
        while (true) {
            line_check(open);
            if (token.id === "[") {
                advance("[");
                key = expression();
                advance("]");
                same_line();
                advance(":");
                value = expression();
            } else {
                key = token;
                advance();
                if (key.alphameric === true) {
                    if (token.id === ":") {
                        same_line();
                        advance(":");
                        value = expression();
                    } else {
                        value = lookup(key.id);
                        if (value === undefined) {
                            return error(key, "expected a variable");
                        }
                    }
                    key = key.id;
                } else if (key.id === "(text)") {
                    key = key.text;
                    same_line();
                    advance(":");
                    value = expression();
                } else {
                    return error(key, "expected a key");
                }
            }
            properties.push({
                zeroth: key,
                wunth: value
            });
            if (token.column_nr < indentation || token.id === "}") {
                break;
            }
            if (!open) {
                same_line();
                advance(",");
            }
        }
        if (open) {
            outdent();
            at_indentation();
        } else {
            same_line();
        }
        advance("}");
        the_brace.zeroth = properties;
        return the_brace;
    });

    prefix("{", function emptyrecordliteral(the_braces) {
        return the_braces;
    });
```

函数字面量解析器用于创建新函数。它还允许访问 *functinos*（函数对象）。这个名字是在我打字出错时想到的。

```javascript
    const functino = (function make_set(array, value = true) {
        const object = Object.create(null);
        array.forEach(function (element) {
            object[element] = value;
        });
        return Object.freeze(object);
    }([
        "?", "|", "/*", "/*", "=", "≠", "<", "≥", ">", "≤",
        "~", "≈", "+", "-", ">>", "<<", "*", "/", "[", "("
    ]));

    prefix("f", function function_literal(the_function) {
```

如果 `f` 后面跟着一个后缀运算符，则生成相应的 functino（函数对象）。

```javascript
        const the_operator = token;
        if (
            functino[token.id] === true
            && (the_operator.id !== "(" || next_token.id === ")")
        ) {
            advance();
            if (the_operator.id === "(") {
                same_line();
                advance(")");
            } else if (the_operator.id === "[") {
                same_line();
                advance("]");
            } else if (the_operator.id === "?") {
                same_line();
                advance("!");
            } else if (the_operator.id === "|") {
                same_line();
                advance("|");
            }
            the_function.zer.minecraft = the_operator.id;
            return the_function;
        }
```

设置新函数。

```javascript
        if (loop.length > 0) {
            return error(the_function, "Do not make functions in loops.");
        }
        the_function.scope = Object.create(null);
        the_function.parent = now_function;
        now_function = the_function;
```

```javascript
        //  Function parameters come in 3 forms.
        //      name
        //      name | default |
        //      name...
```

参数列表可以是开放的或封闭的。

```javascript
        const parameters = [];
        if (token.alphameric === true) {
            let open = is_line_break();
            if (open) {
                indent();
            }
            while (true) {
                line_check(open);
                let the_parameter = token;
                register(the_parameter);
                advance();
                if (token.id === "...") {
                    parameters.push(ellipsis(the_parameter));
                    break;
```



```
if (token.id === "|") {
    advance("|");
    parameters.push(parse_suffix["|"](the_parameter, prev_token));
} else {
    parameters.push(the_parameter);
}
```

```
if (open) {
    if (token.id === ",") {
        return error(token, "unexpected ','");
    }
    if (token.alphameric !== true) {
        break;
    }
} else {
    if (token.id !== ",") {
        break;
    }
    same_line();
    advance(",");
    if (token.alphameric !== true) {
        return error(token, "expected another parameter");
    }
}
```

```
if (open) {
    outdent();
    at_indentation();
} else {
    same_line();
}
```

```
}
```

```
the_function.zeroth = parameters;
```

一个函数可以有一个 (返回表达式) 或一个 {函数体}。

解析返回表达式。

```
if (token.id === "(") {
    advance("(");
    if (is_line_break()) {
        indent();
        the_function.wunth = expression(0, true);
        outdent();
        at_indentation();
    } else {
        the_function.wunth = expression();
        same_line();
    }
    advance(")");
} else {
```

解析函数体。函数体必须包含一个显式的 `return`。没有通过执行到底部的隐式返回。

```
advance("{");
indent();
the_function.wunth = statements();
```

#### 解析如何工作

```
    if (the_function.wunth.return !== true) {
        return error(prev_token, "missing explicit 'return'");
    }
```

解析失败处理程序。

```
    if (token.id === "failure") {
        outdent();
        at_indentation();
        advance("failure");
        indent();
        the_function.twoth = statements();
        if (the_function.twoth.return !== true) {
            return error(prev_token, "missing explicit 'return'");
        }
    }
    outdent();
    at_indentation();
    advance("}");
}
now_function = the_function.parent;
return the_function;
});
```

`statements` 函数解析语句，返回一个语句标记的数组。如果需要，它使用 `prelude` 函数从标记中分离出动词。

```
function statements() {
    const statement_list = [];
    let the_statement;
    while (true) {
        if (
            token === the_end
            || token.column_nr < indentation
            || token.alphameric !== true
            || token.id.startsWith("export")
        ) {
            break;
        }
        at_indentation();
        prelude();
        let parser = parse_statement[prev_token.id];
        if (parser === undefined) {
            return error(prev_token, "expected a statement");
        }
        prev_token.class = "statement";
        the_statement = parser(prev_token);
        statement_list.push(the_statement);
        if (the_statement.disrupt === true) {
            if (token.column_nr === indentation) {
                return error(token, "unreachable");
            }
            break;
        }
    }
    if (statement_list.length === 0) {
        if (!token.id.startsWith("export")) {
            return error(token, "expected a statement");
```

```
    }
} else {
    statement_list.disrupt = the_statement.disrupt;
    statement_list.return = the_statement.return;
}
return statement_list;
}
```

`disrupt` 属性标记会中断或返回的语句和语句列表。`return` 属性标记会返回的语句和语句列表。

`break` 语句用于跳出循环。解析器接收 `break` 标记。它设置当前循环的退出条件。

```
parse_statement.break = function (the_break) {
    if (loop.length === 0) {
        return error(the_break, "'break' wants to be in a loop.");
    }
    loop[loop.length - 1] = "break";
    the_break.disrupt = true;
    return the_break;
};
```

`call` 语句调用一个函数并忽略其返回值。这是为了识别那些纯粹因其副作用而发生的调用。

```
parse_statement.call = function (the_call) {
    the_call.zeroth = expression();
    if (the_call.zeroth.id !== "(") {
        return error(the_call, "expected a function invocation");
    }
    return the_call;
};
```

`def` 语句注册只读变量。

```
parse_statement.def = function (the_def) {
    if (!token.alphameric) {
        return error(token, "expected a name.");
    }
    same_line();
    the_def.zeroth = token;
    register(token, true);
    advance();
    same_line();
    advance(":");
    the_def.wunth = expression();
    return the_def;
};
```

`fail` 语句是 Neo 中最冒险的实验。大多数语言中的异常机制已经被腐化成通信通道。`fail` 语句试图修复这一点。

```
parse_statement.fail = function (the_fail) {
    the_fail.disrupt = true;
    return the_fail;
};
```

`if` 语句有一个可选的 `else` 子句或 `else if` 语句。如果两个分支都中断或返回，那么 `if` 语句本身也会中断或返回。

```
parse_statement.if = function if_statement(the_if) {
    the_if.zeroth = expression();
    indent();
    the_if.wunth = statements();
    outdent();
    if (token.column_nr === indentation) {
        if (token.id === "else") {
            advance("else");
            indent();
            the_if.twoth = statements();
            outdent();
            the_if.disrupt = the_if.wunth.disrupt && the_if.twoth.disrupt;
            the_if.return = the_if.wunth.return && the_if.twoth.return;
        } else if (token.id.startsWith("else if ")) {
            prelude();
            prelude();
            the_if.twoth = if_statement(prev_token);
            the_if.disrupt = the_if.wunth.disrupt && the_if.twoth.disrupt;
            the_if.return = the_if.wunth.return && the_if.twoth.return;
        }
    }
    return the_if;
};
```

`let` 语句是 Neo 的赋值语句。左侧不是一个普通的表达式。它是一个更受限制的东西，称为 *左值*。左值可以是一个变量（`var` 不是 `def`），或是一个查找字段或元素的表达式。

```
parse_statement.let = function (the_let) {
```

`let` 语句是唯一允许发生变更的地方。

下一个标记必须是一个名称。

```
same_line();
const name = token;
advance();
const id = name.id;
let left = lookup(id);
if (left === undefined) {
    return error(name, "expected a variable");
}
let readonly = left.readonly;
```

现在我们考虑后缀运算符 `[]` 、 `[` 和 `{`。

```
while (true) {
    if (token === the_end) {
        break;
    }
    same_line();
```

此位置的 `[]` 表示数组追加操作。

```
if (token.id === "[]") {
    readonly = false;
    token.zeroth = left;
    left = token;
```

#### 27.17 解析如何工作

```
same_line();
advance("[]");
break;
}
if (token.id === ".") {
    readonly = false;
    advance(".");
    left = parse_dot(left, prev_token);
} else if (token.id === "[") {
    readonly = false;
    advance("[");
    left = parse_subscript(left, prev_token);
} else if (token.id === "(") {
    readonly = false;
    advance("(");
    left = parse_invocation(left, prev_token);
    if (token.id === ":") {
        return error(left, "assignment to the result of a function");
    }
} else {
    break;
}
}
advance(";");
if (readonly) {
    return error(left, "assignment to a constant");
}
the_let.zeroth = left;
the_let.wunth = expression();
```

此位置的 `[]` 表示数组弹出操作。

```
if (token.id === "[]" && left.id !== "[]" && (
    the_let.wunth.alphameric === true
    || the_let.wunth.id === "."
    || the_let.wunth.id === "["
    || the_let.wunth.id === "("
)) {
    token.zeroth = the_let.wunth;
    the_let.wunth = token;
    same_line();
    advance("[]");
}
return the_let;
};
```

`loop` 语句维护一个栈来处理嵌套循环。栈中的条目是循环的退出条件。如果没有显式退出，栈的状态是 "infinite"。如果唯一的退出是 `return` 语句，其状态是 "return"。如果循环通过 `break` 语句退出，其状态是 "break"。为此目的，`fail` 不被视为显式退出条件。

```
parse_statement.loop = function (the_loop) {
    indent();
    loop.push("infinite");
    the_loop.zeroth = statements();
    const exit = loop.pop();
    if (exit === "infinite") {
```



```
return error(the_loop, "A loop wants a 'break'.");
}
if (exit === "return") {
    the_loop.disrupt = true;
    the_loop.return = true;
}
outdent();
return the_loop;
};
```

return语句将“无限”循环的状态更改为“return”；

```
parse_statement.return = function (the_return) {
    try {
        if (now_function.parent === undefined) {
            return error(the_return, "'return' wants to be in a function.");
        }
        loop.forEach(function (element, element_nr) {
            if (element === "infinite") {
                loop[element_nr] = "return";
            }
        });
        if (is_line_break()) {
            return error(the_return, "'return' wants a return value.");
        }
        the_return.zeroth = expression();
        if (token === "}") {
            return error(the_return, "Misplaced 'return'.");
        }
        the_return.disrupt = true;
        the_return.return = true;
        return the_return;
    } catch (ignore) {
        return the_error;
    }
};
```

var语句声明一个变量，该变量可以使用let语句进行赋值。如果变量未显式初始化，其初始值为null。

```
parse_statement.var = function (the_var) {
    if (!token.alphameric) {
        return error(token, "expected a name.");
    }
    same_line();
    the_var.zeroth = token;
    register(token);
    advance();
    if (token.id === ":") {
        same_line();
        advance(":");
        the_var.wunth = expression();
    }
    return the_var;
};
```

#### 27.19 解析的工作原理

```
Object.freeze(parse_prefix);
Object.freeze(parse_suffix);
Object.freeze(parse_statement);
```

`import`和`export`语句不包含在`parse_statement`中，因为它们在源码中的位置是受限制的。所有`import`语句必须放置在任何其他语句之前。只允许一个`export`语句，并且它必须是最后一个语句。

```
function parse_import(the_import) {
    same_line();
    register(token, true);
    the_import.zeroth = token;
    advance();
    same_line();
    advance(":");
    same_line();
    the_import.wunth = token;
    advance("(text)");
    the_import.class = "statement";
    return the_import;
}
```

```
function parse_export(the_export) {
    the_export.zeroth = expression();
    the_export.class = "statement";
    return the_export;
}
```

我们导出一个解析函数。它接受一个标记生成器并返回一棵树。我们不需要构造函数，因为解析器在调用之间不保留任何状态。

```
export default function parse(token_generator) {
    try {
        indentation = 0;
        loop = [];
        the_token_generator = token_generator;
        next_token = the_end;
        const program = {
            id: "",
            scope: Object.create(null)
        };
        now_function = program;
        advance();
        advance();
        let the_statements = [];
        while (token.id.startsWith("import ")) {
            at_indentation();
            prelude();
            the_statements.push(parse_import(prev_token));
        }
        the_statements = the_statements.concat(statements());
        if (token.id.startsWith("export")) {
            at_indentation();
            prelude();
            the_statements.push(parse_export(prev_token));
        }
```

```
if (token !== the_end) {
    return error(token, "unexpected");
}
program.zeroth = the_statements;
return program;
} catch (ignore) {
    return the_error;
}
};
```

# 第28章

### 代码生成的工作原理

> 你必须放下一切，尼奥。
> 恐惧、怀疑和不信任。
> 释放你的思想。
> *墨菲斯*

下一步是将解析器编织的树转换为可执行形式。这称为*代码生成*，但实际上是一种转换。

我们有许多目标语言的选择。我们可以生成机器码，或者虚拟机的代码，或者另一种编程语言的代码。通过合适的运行时，我们可以针对C语言，但我们将针对JavaScript。

JavaScript是一个出人意料的优秀目标语言。它提供了出色的（且不可见的）内存管理，这通常是推出新语言时最困难的方面。为真实机器生成代码可能需要管理有限的寄存器集。JavaScript允许你拥有所有需要的变量。对象是一种非常通用的数据结构。JavaScript因其对象设计应该得到更多赞誉。

我们从创建一些集合开始。我们需要产生布尔值的集合，以及JavaScript保留字集合。

```
function make_set(array, value = true) {
    const object = Object.create(null);
    array.forEach(function (element) {
        object[element] = value;
    });
    return $NEO.stone(object);
}
```

```
const boolean_operator = make_set([
    "array?", "boolean?", "function?", "integer?", "not", "number?", "record?",
    "stone?", "text?", "true", "=", "≠", "<", ">", "≤", "≥", "/\\", "\\/"
]);
```

```
const reserved = make_set([
    "arguments", "await", "break", "case", "catch", "class", "const",
    "continue", "debugger", "default", "delete", "do", "else", "enum", "eval",
    "export", "extends", "false", "finally", "for", "function", "if",
    "implements", "import", "in", "Infinity", "instanceof", "interface", "let",
    "NaN", "new", "null", "package", "private", "protected", "public", "return",
    "static", "super", "switch", "this", "throw", "true", "try", "typeof",
    "undefined", "var", "void", "while", "with", "yield"
]);
```

原始对象包含从Neo原始空间到JavaScript空间的映射。一些映射到Neo运行时，一些映射到JavaScript。

```
const primordial = $NEO.stone({
    "abs": "$NEO.abs",
    "array": "$NEO.array",
    "array?": "Array.isArray",
    "bit and": "$NEO.bitand",
    "bit mask": "$NEO.bitmask",
    "bit or": "$NEO.bitor",
    "bit shift down": "$NEO.bitdown",
    "bit shift up": "$NEO.bitup",
    "bit xor": "$NEO.bitxor",
    "boolean?": "$NEO.boolean_",
    "char": "$NEO.char",
    "code": "$NEO.code",
    "false": "false",
    "fraction": "$NEO.fraction",
    "function?": "$NEO.function_",
    "integer": "$NEO.integer",
    "integer?": "$NEO.integer_",
    "length": "$NEO.length",
    "neg": "$NEO.neg",
    "not": "$NEO.not",
    "null": "undefined",
    "number": "$NEO.make",
    "number?": "$NEO.is_big_float",
    "record": "$NEO.record",
    "record?": "$NEO.record_",
    "stone": "$NEO.stone",
    "stone?": "Object.isFrozen",
    "text": "$NEO.text",
    "text?": "$NEO.text_",
    "true": "true"
});
```

空白在JavaScript中远不如在Neo中重要，因此我们可以生成极其丑陋的代码而JavaScript也不会在意。我认为世界上丑陋的东西已经够多了。当我们有机会让事情变得更好时，我们应该这样做，即使没人注意到。

```
let indentation;

function indent() {
    indentation += 4;
}

function outdent() {
    indentation -= 4;
}

function begin() {
```

在每行的开头，我们输出一个换行符和填充。

```
return "\n" + " ".repeat(indentation);
}
```

```
let front_matter;
let operator_transform;
let statement_transform;
let unique;
```

Neo和JavaScript中的命名约定不完全兼容。Neo允许空格和问号，而JavaScript不允许。因此，如果必要，我们修改Neo名称以使其成为合法的JavaScript名称。Neo允许所有单词，但JavaScript保留了一些单词。当你在Neo中使用JavaScript保留字时，我们将其移入JavaScript空间时会在单词前添加一个美元符号。我们将大十进制浮点数转换成类似于数字字面量的形式，以使程序更具可读性。

```
const rx_space_question = /[ \u0020?]/g;
```

```
function mangle(name) {
```

JavaScript不允许标识符中包含空格或?，所以我们用_替换它们。保留字添加$前缀。

因此，what me worry? 变成 what_me_worry_，class 变成 $class。

```
return (
    reserved[name] === true
    ? "$" + name
    : name.replace(rx_space_question, "_")
);
```

```
}
```

```
const rx_minus_point = /[ .-]/g;
```

```
function numgle(number) {
```

我们通过将大十进制字面量转换成常量，使其看起来尽可能自然。常量名以$开头。-或.被替换为_。

因此，1 变成 $1，98.6 变成 $98_6，-1.011e-5 变成 $_1_011e_5。

```
const text = big_float.string(number.number);
const name = "$" + text.replace(rx_minus_point, "_");
if (unique[name] !== true) {
    unique[name] = true;
    front_matter.push(
        "const " + name + " = $NEO.number(\"" + text + "\");\n"
    );
}
return name;
```

``}
```

我们的代码生成器大部分只是一些简单的函数，将标记转换回文本。它们相互调用以文本化所有部分。我们从`op`开始，它接受一个运算符标记。它获取运算符的转换器。许多运算符遵循简单的模式，因此它们的转换器是字符串。如果标记附加了操作数，则会组合一个函数调用。对于不符合该模式的运算符，转换器是一个函数，它接受标记并返回字符串。
```



### 代码生成的工作原理

```javascript
function op(thing) {
    const transform = operator_transform[thing.id];
    return (
        typeof transform === "string"
        ? (
            thing.zeroth === undefined
            ? transform
            : transform + "(" + expression(thing.zeroth) + (
                thing.wunth === undefined
                ? ""
                : ", " + expression(thing.wunth)
            ) + ")"
        )
        : transform(thing)
    );
}
```

`expression` 函数处理通用的表达式标记。

```javascript
function expression(thing) {
    if (thing.id === "(number)") {
        return numgle(thing);
    }
    if (thing.id === "(text)") {
        return JSON.stringify(thing.text);
    }
    if (thing.alphameric) {
        return (
            thing.origin === undefined
            ? primordial[thing.id]
            : mangle(thing.id)
        );
    }
    return op(thing);
}
```

此函数用于创建数组字面量。

```javascript
function array_literal(array) {
    return "[" + array.map(function (element) {
        return (
            Array.isArray(element)
            ? array_literal(element)
            : expression(element)
        );
    }).join(", ") + "]";
}
```

Neo 记录字面量会生成没有原型的对象。空记录通过 `Object.create(null)` 创建。字段通过赋值生成。我们将这些赋值包装在一个立即调用的函数表达式中。`{[foo bear]: 12.3, two part}` 会生成：

```javascript
(function (o) {
    $NEO.set(o, foo_bear, $12_3);
    o["two part"] = two_part;
}(Object.create(null)))
```

在记录字面量中，变量名会被混淆处理，但字段名不会。

```javascript
function record_literal(array) {
    indent();
    const padding = begin();
    const string = "(function (o) {" + array.map(function (element) {
        return padding + (
            typeof element.zeroth === "string"
            ? (
                "o["
                + JSON.stringify(element.zeroth)
                + "] = "
                + expression(element.wunth)
                + ";"
            )
            : (
                "$NEO.set(o, "
                + expression(element.zeroth)
                + ", "
                + expression(element.wunth)
                + ");"
            )
        );
    }).join("") + padding + "return o;";
    outdent();
    return string + begin() + "}(Object.create(null)))";
}
```

Neo 不是一个布尔语言。在某些地方，例如 `if` 语句的条件部分，它期望接收布尔值。如果 Neo 接收到的值不是布尔值，那么它必须报错。为了在 JavaScript 中实现这种行为，我们可能需要用 `assert_boolean` 函数包装这些值。

```javascript
function assert_boolean(thing) {
    const string = expression(thing);
    return (
        (
            boolean_operator[thing.id] === true
            || (
                thing.zeroth !== undefined
                && thing.zeroth.origin === undefined
                && boolean_operator[thing.zeroth.id]
            )
        )
        ? string
        : "$NEO.assert_boolean(" + string + ")"
    );
}
```

我们可以将语句标记数组转换为字符串，并用块包装起来。

```javascript
function statements(array) {
    const padding = begin();
    return array.map(function (statement) {
        return padding + statement_transform[statement.id](statement);
    }).join("");
}

function block(array) {
    indent();
    const string = statements(array);
    outdent();
    return "{" + string + begin() + "}";
}
```

`statement_transform` 对象包含了所有语句的转换函数。大多数语句都非常简单。`if` 语句比较复杂，因为它有三种形式：没有 else、有 else、以及有 else if。`let` 语句是唯一发生赋值的地方。它必须处理在左侧压入、在右侧弹出的 `[]` 操作符，并处理左值。

```javascript
statement_transform = $NEO.stone({
    break: function (ignore) {
        return "break;";
    },
    call: function (thing) {
        return expression(thing.zeroth) + ";";
    },
    def: function (thing) {
        return (
            "var " + expression(thing.zeroth)
            + " = " + expression(thing.wunth) + ";"
        );
    },
    export: function (thing) {
        const exportation = expression(thing.zeroth);
        return "export default " + (
            exportation.startsWith("$NEO.stone(")
            ? exportation
            : "$NEO.stone(" + exportation + ")"
        ) + ";";
    },
    fail: function () {
        return "throw $NEO.fail(\"fail\");";
    },
    if: function if_statement(thing) {
        return (
            "if ("
            + assert_boolean(thing.zeroth)
            + ") "
            + block(thing.wunth)
            + (
                thing.twoth === undefined
                ? ""
                : " else " + (
                    thing.twoth.id === "if"
                    ? if_statement(thing.twoth)
                    : block(thing.twoth)
                )
            )
        );
    },
    import: function (thing) {
        return (
            "import " + expression(thing.zeroth)
            + " from " + expression(thing.wunth) + ";"
        );
    },
    let: function (thing) {
        const right = (
            thing.wunth.id === "[]"
            ? expression(thing.wunth.zeroth) + ".pop();"
            : expression(thing.wunth)
        );
        if (thing.zeroth.id === "[]") {
            return expression(thing.zeroth.zeroth) + ".push(" + right + ");";
        }
        if (thing.zeroth.id === ".") {
            return (
                "$NEO.set(" + expression(thing.zeroth.zeroth)
                + ", " + JSON.stringify(thing.zeroth.wunth.id)
                + ", " + right + ");"
            );
        }
        if (thing.zeroth.id === "[") {
            return (
                "$NEO.set(" + expression(thing.zeroth.zeroth)
                + ", " + expression(thing.zeroth.wunth)
                + ", " + right + ");"
            );
        }
        return expression(thing.zeroth) + " = " + right + ";";
    },
    loop: function (thing) {
        return "while (true) " + block(thing.zeroth);
    },
    return: function (thing) {
        return "return " + expression(thing.zeroth) + ";";
    },
    var: function (thing) {
        return "var " + expression(thing.zeroth) + (
            thing.wunth === undefined
            ? ";"
            : " = " + expression(thing.wunth) + ";"
        );
    }
});
```

*functino* 是一个内置函数，通过在操作符前加上 `f` 前缀来访问。

```javascript
const functino = $NEO.stone({
    "?": "$NEO.ternary",
    "|": "$NEO.default",
    "/\\": "$NEO.and",
    "\\/": "$NEO.or",
    "=": "$NEO.eq",
    "≠": "$NEO.ne",
    "<": "$NEO.lt",
    "≥": "$NEO.ge",
    ">": "$NEO.gt",
    "≤": "$NEO.le",
    "~": "$NEO.cat",
    "≈": "$NEO.cats",
    "+": "$NEO.add",
    "-": "$NEO.sub",
    ">>": "$NEO.max",
    "<<": "$NEO.min",
    "*": "$NEO.mul",
    "/": "$NEO.div",
    "[": "$NEO.get",
    "(": "$NEO.resolve"
});
```

`operator_transform` 对象包含了所有操作符的转换函数。

```javascript
operator_transform = $NEO.stone({
    "?": function (thing) {
        indent();
        let padding = begin();
        let string = (
            "(" + padding + assert_boolean(thing.zeroth)
            + padding + "? " + expression(thing.wunth)
            + padding + " : " + expression(thing.twoth)
        );
        outdent();
        return string + begin() + ")";
    },
    "/\\": function (thing) {
        return (
            "(" + assert_boolean(thing.zeroth)
            + " && " + assert_boolean(thing.wunth)
            + ")"
        );
    },
    "\\/": function (thing) {
        return (
            "(" + assert_boolean(thing.zeroth)
            + " || " + assert_boolean(thing.wunth)
            + ")"
        );
    },
    "=": "$NEO.eq",
    "≠": "$NEO.ne",
    "<": "$NEO.lt",
    "≥": "$NEO.ge",
    ">": "$NEO.gt",
    "≤": "$NEO.le",
    "~": "$NEO.cat",
    "≈": "$NEO.cats",
    "+": "$NEO.add",
    "-": "$NEO.sub",
    ">>": "$NEO.max",
    "<<": "$NEO.min",
    "*": "$NEO.mul",
    "/": "$NEO.div",
    "|": function (thing) {
        return (
            "(function (_0) {"
            + "return (_0 === undefined) ? "
            + expression(thing.wunth) + " : _0;}("
            + expression(thing.zeroth) + "))"
        );
    }
});
```



 ## 代码生成的工作原理

```javascript
"\"..."": function (thing) {
    return "\"..." + expression(thing.zeroth);
},
".": function (thing) {
    return (
        "$NEO.get(" + expression(thing.zeroth)
        + ", \"" + thing.wunth.id + "\")"
    );
},
"[": function (thing) {
    if (thing.wunth === undefined) {
        return array_literal(thing.zeroth);
    }
    return (
        "$NEO.get(" + expression(thing.zeroth)
        + ", " + expression(thing.wunth) + ")"
    );
},
"{": function (thing) {
    return record_literal(thing.zeroth);
},
"(": function (thing) {
    return (
        expression(thing.zeroth) + "("
        + thing.wunth.map(expression).join(", ") + ")"
    );
},
"[]": "[]",
"{}": "Object.create(null)",
"f": function (thing) {
    if (typeof thing.zeroth === "string") {
        return function[thing.zeroth];
    }
    return "$NEO.stone(function (" + thing.zeroth.map(function (param) {
        if (param.id === "...") {
            return "..." + mangle(param.zeroth.id);
        }
        if (param.id === "|") {
            return (
                mangle(param.zeroth.id) + " = " + expression(param.wunth)
            );
        }
        return mangle(param.id);
    }).join(", ") + ") " + (
        Array.isArray(thing.wunth)
        ? block(thing.wunth)
        : "{return " + expression(thing.wunth) + ";}"
    ) + ")";
}
```

它导出一个代码生成器函数，该函数接收一棵树并返回一个 JavaScript 源程序。

```javascript
export default $NEO.stone(function codegen(tree) {
    front_matter = [
        "import $NEO from \"./neo.runtime.js\"\n"
    ];
```

#### 28.9 代码生成的工作原理

```javascript
indentation = 0;
unique = Object.create(null);
const bulk = statements(tree.zeroth);
return front_matter.join("") + bulk;
});
```

### 示例

此函数类似于 map 方法，但它也适用于多个数组、标量和生成器。

```javascript
export f function, arguments... {
    if length(arguments) = 0
        return null
    var index: 0
    def result: []
    var stop: false

    def prepare arguments: f argument {
        def candidate: (
            array?(argument)
            ? argument[index]
            ! (
                function?(argument)
                ? argument(index)
                ! argument
            )
        )
        if candidate = null
            let stop: true
        return candidate
    }

    loop
        var processed: array(arguments, prepare arguments)
        if stop
            break
        let result[]: function(processed...)
        let index: index + 1
    return result
}
```

这是由 `codegen(parse(tokenize(neo_source)))` 生成的 .js 文件：

```javascript
import $NEO from "./neo.runtime.js";
const $0 = $NEO.number("0");
const $1 = $NEO.number("1");

export default $NEO.stone(function ($function, ...$arguments) {
    if ($NEO.eq($NEO.length($arguments), $0)) {
        return undefined;
    }
    var index = $0;
    var result = [];
    var stop = false;
    var prepare_arguments = $NEO.stone(function (argument) {
        var candidate = (
            Array.isArray(argument)
? $NEO.get(argument, index)
    : (
        $NEO.function_(argument)
        ? argument(index)
        : argument
    )
);
if ($NEO.eq(candidate, undefined)) {
    stop = true;
}
return candidate;
});
while (true) {
    var processed = $NEO.array($arguments, prepare_arguments);
    if ($NEO.assert_boolean(stop)) {
        break;
    }
    result.push($function(...processed));
    index = $NEO.add(index, $1);
}
return result;
});
```

然后……

```javascript
import do: "example/do.neo"

var result: do(f+, [1, 2, 3], [5, 4, 3])
# result is [6, 6, 6]

let result: do(f/, 60, [1, 2, 3, 4, 5, 6])
# result is [60, 30, 20, 15, 12, 10]
```

它被转译为……

```javascript
import $NEO from "./neo.runtime.js"
const $1 = $NEO.number("1");
const $2 = $NEO.number("2");
const $3 = $NEO.number("3");
const $5 = $NEO.number("5");
const $4 = $NEO.number("4");
const $60 = $NEO.number("60");
const $6 = $NEO.number("6");

import $do from "example/do.neo";
var result = $do($NEO.add, $60, [$1, $2, $3], [$5, $4, $3]);
result = $do($NEO.div, $60, [$1, $2, $3, $4, $5, $6]);
```

# 第 29 章

## 运行时的工作原理

> 我知道你为什么在这里，尼奥。我知道你一直在做什么……为什么你几乎不睡觉，为什么你独自生活，为什么夜复一夜，你坐在电脑前。

*崔妮蒂*

*运行时*是支持程序执行的软件。JavaScript 作为转译目标的流行部分原因在于其提供的运行时支持质量。如果源语言的语义与目标语言不同，则必须添加一些专门的运行时支持。Neo-in-JavaScript 运行时的形式是一个包含辅助执行函数的对象。

Neo 的两大语义改进是更好的数字类型和更好的对象。数字类型在第 4 章中已开发。Neo 记录将对象和 weakmap 统一起来。总结如下：

- 键可以是文本、记录或数组。只有文本键可以通过 `array` 函数进行枚举。
- 值为 `null` 会删除一个字段。
- 带有缺失对象的路径表达式不会失败。它们只会产生 `null`。
- 数组只接受整数作为键并强制执行其边界。

我们从一个中心化的 `fail` 函数开始。

```javascript
function fail(what = "fail") {
    throw new Error(what);
}
```

此文件中唯一的状态变量是 `weakmap_of_weakmaps`。它将 weakmap 绑定到记录。大多数记录不需要 weakmap，但那些需要的记录会从 `weakmap_of_weakmaps` 获取它们的 weakmap。

`get` 函数从记录中检索字段的值或从数组中检索元素。它还通过返回函数来实现了将函数作为方法调用。如果由于任何原因出错，则返回 `null` 对象，JavaScript 将其识别为 `undefined`。

### 29.1 运行时的工作原理

```javascript
let weakmap_of_weakmaps = new WeakMap();
```

```javascript
function get(container, key) {
    try {
        if (Array.isArray(container) || typeof container === "string") {
            const element_nr = big_float.number(key);
            return (
                Number.isSafeInteger(element_nr)
                    ? container[
                          element_nr >= 0
                              ? element_nr
                              : container.length + element_nr
                      ]
                    : undefined
            );
        }
        if (typeof container === "object") {
            if (big_float.is_big_float(key)) {
                key = big_float.string(key);
            }
            return (
                typeof key === "string"
                    ? container[key]
                    : weakmap_of_weakmaps.get(container).get(key)
            );
        }
        if (typeof container === "function") {
            return function (...rest) {
                return container(key, rest);
            };
        }
    } catch (ignore) {
    }
}
```

get 函数guarded可以作为 `f[]` 函数访问。

set 函数是添加、更新或删除记录字段，或更新数组元素的方法。如果任何出错，它会失败。get 函数非常宽容。set 函数则不然。

```javascript
function set(container, key, value) {
    if (Object.isFrozen(container)) {
        return fail("set");
    }
    if (Array.isArray(container)) {
```

数组仅使用大浮点数作为键。

```javascript
        let element_nr = big_float.number(key);
        if (!Number.isSafeInteger(element_nr)) {
            return fail("set");
        }
```

负索引是别名，因此 [-1] 设置最后一个元素。

```javascript
        if (element_nr < 0) {
            element_nr = container.length + element_nr;
        }
```

键必须在数组的已分配范围内。

```javascript
if (element_nr < 0 || element_nr >= container.length) {
    return fail("set");
}
container[element_nr] = value;
```

```javascript
} else {
    if (big_float.is_big_float(key)) {
        key = big_float.string(key);
    }
```

如果键是字符串，则它是对象更新。

```javascript
if (typeof key === "string") {
    if (value === undefined) {
        delete container[key];
    } else {
        container[key] = value;
    }
} else {
```

否则，这是 weakmap 更新。每个具有对象键的记录都会有一个 weakmap。注意，当键是数组时，`typeof key !== "object"` 为 false。

```javascript
if (typeof key !== "object") {
    return fail("set");
}
let weakmap = weakmap_of_weakmaps.get(container);
```

如果此容器尚未关联 weakmap，则创建一个。

```javascript
if (weakmap === undefined) {
    if (value === undefined) {
        return;
    }
    weakmap = new WeakMap();
    weakmap_of_weakmaps.set(container, weakmap);
}
```

更新 weakmap。

```javascript
if (value === undefined) {
    weakmap.delete(key);
} else {
    weakmap.set(key, value);
}
}
}
```

有一组函数用于创建数组、数字、记录和文本。

array 函数完成了 `new Array`、`array.fill`、`array.slice`、`Object.keys`、`string.split` 等的工作。

```javascript
if (big_float.is_big_float(zeroth)) {
    const dimension = big_float.number(zeroth);
    if (!Number.isSafeInteger(dimension) || dimension < 0) {
        return fail("array");
    }
```



```
    }
    let newness = new Array(dimension);
    return (
        (wunth === undefined || dimension === 0)
        ? newness
        : (
            typeof wunth === "function"
            ? newness.map(wunth)
            : newness.fill(wunth)
        )
    );
}
if (Array.isArray(zeroth)) {
    if (typeof wunth === "function") {
        return zeroth.map(wunth);
    }
    return zeroth.slice(big_float.number(wunth), big_float.number(rest[0]));
}
if (typeof zeroth === "object") {
    return Object.keys(zeroth);
}
if (typeof zeroth === "string") {
    return zeroth.split(wunth || "");
}
return fail("array");
}

function number(a, b) {
    return (
        typeof a === "string"
        ? big_float.make(a, b)
        : (
            typeof a === "boolean"
            ? big_float.make(Number(a))
            : (
                big_float.is_big_float(a)
                ? a
                : undefined
            )
        )
    );
}

function record(zeroth, wunth) {
    const newness = Object.create(null);
    if (zeroth === undefined) {
        return newness;
    }
    if (Array.isArray(zeroth)) {
        if (wunth === undefined) {
            wunth = true;
        }
        zeroth.forEach(function (element, element_nr) {
            set(
                newness,
                element,
                (
                    Array.isArray(wunth)
                    ? wunth[element_nr]
                    : (
                        typeof wunth === "function"
                        ? wunth(element)
                        : wunth
                    )
                )
            );
        });
        return newness;
    }
    if (typeof zeroth === "object") {
        if (wunth === undefined) {
            return Object.assign(newness, zeroth);
        }
        if (typeof wunth === "object") {
            return Object.assign(newness, zeroth, wunth);
        }
        if (Array.isArray(wunth)) {
            wunth.forEach(function (key) {
                let value = zeroth[key];
                if (value !== undefined) {
                    newness[key] = value;
                }
            });
            return newness;
        }
    }
    return fail("record");
}

function text(zeroth, wunth, twoth) {
    if (typeof zeroth === "string") {
        return (zeroth.slice(big_float.number(wunth), big_float.number(twoth)));
    }
    if (big_float.is_big_float(zeroth)) {
        return big_float.string(zeroth, wunth);
    }
    if (Array.isArray(zeroth)) {
        let separator = wunth;
        if (typeof wunth !== "string") {
            if (wunth !== undefined) {
                return fail("string");
            }
            separator = "";
        }
        return zeroth.join(separator);
    }
    if (typeof zeroth === "boolean") {
        return String(zeroth);
    }
}
```

`stone` 是一个深度冻结。

### 运行时如何工作

```
function stone(object) {
    if (!Object.isFrozen(object)) {
        object = Object.freeze(object);
        if (typeof object === "object") {
            if (Array.isArray(object)) {
                object.forEach(stone);
            } else {
                Object.keys(object).forEach(function (key) {
                    stone(object[key]);
                });
            }
        }
    }
    return object;
}
```

有一组谓词函数用于识别事物的类型。

```
function boolean_(any) {
    return typeof any === "boolean";
}
```

```
function function_(any) {
    return typeof any === "function";
}
```

```
function integer_(any) {
    return (
        big_float.is_big_float(any)
        && big_float.normalize(any).exponent === 0
    );
}
```

```
function number_(any) {
    return big_float.is_big_float(any);
}
```

```
function record_(any) {
    return (
        any !== null
        && typeof any === "object"
        && !big_float.is_big_float(any)
    );
}
```

```
function text_(any) {
    return typeof any === "string";
}
```

有一组逻辑函数。这些是函数版本，不具备短路求值能力。只有运算符版本才能对其操作数进行惰性求值。

```
function assert_boolean(boolean) {
    return (
        typeof boolean === "boolean"
        ? boolean
        : fail("boolean")
    );
}

function and(zeroth, wunth) {
    return assert_boolean(zeroth) && assert_boolean(wunth);
}
```

```
function or(zeroth, wunth) {
    return assert_boolean(zeroth) || assert_boolean(wunth);
}
```

```
function not(boolean) {
    return !assert_boolean(boolean);
}
```

```
function ternary(zeroth, wunth, twoth) {
    return (
        assert_boolean(zeroth)
        ? wunth
        : twoth
    );
}
```

```
function default_function(zeroth, wunth) {
    return (
        zeroth === undefined
        ? wunth
        : zeroth
    );
}
```

有一组关系运算符。

```
function eq(zeroth, wunth) {
    return zeroth === wunth || (
        big_float.is_big_float(zeroth)
        && big_float.is_big_float(wunth)
        && big_float.eq(zeroth, wunth)
    );
}
```

```
function lt(zeroth, wunth) {
    return (
        zeroth === undefined
        ? false
        : (
            wunth === undefined
            ? true
            : (
                (
                    big_float.is_big_float(zeroth)
                    && big_float.is_big_float(wunth)
                )
                ? big_float.lt(zeroth, wunth)
                : (
                    (typeof zeroth === typeof wunth && (
                        typeof zeroth === "string"
                        || typeof zeroth === "number"
                    ))
                    ? zeroth < wunth
                    : fail("lt")
                )
            )
        )
    );
}
```

```
function ge(zeroth, wunth) {
    return !lt(zeroth, wunth);
}
function gt(zeroth, wunth) {
    return lt(wunth, zeroth);
}
function le(zeroth, wunth) {
    return !lt(wunth, zeroth);
}
function ne(zeroth, wunth) {
    return !eq(wunth, zeroth);
}
```

有一组算术运算符。

```
function add(a, b) {
    return (
        (big_float.is_big_float(a) && big_float.is_big_float(b))
        ? big_float.add(a, b)
        : undefined
    );
}
function sub(a, b) {
    return (
        (big_float.is_big_float(a) && big_float.is_big_float(b))
        ? big_float.sub(a, b)
        : undefined
    );
}
function mul(a, b) {
    return (
        (big_float.is_big_float(a) && big_float.is_big_float(b))
        ? big_float.mul(a, b)
        : undefined
    );
}
function div(a, b) {
    return (
        (big_float.is_big_float(a) && big_float.is_big_float(b))
        ? big_float.div(a, b)
        : undefined
    );
}
```

```
function max(a, b) {
    return (
        lt(b, a)
        ? a
        : b
    );
}

function min(a, b) {
    return (
        lt(a, b)
        ? a
        : b
    );
}

function abs(a) {
    return (
        big_float.is_big_float(a)
        ? big_float.abs(a)
        : undefined
    );
}

function fraction(a) {
    return (
        big_float.is_big_float(a)
        ? big_float.fraction(a)
        : undefined
    );
}

function integer(a) {
    return (
        big_float.is_big_float(a)
        ? big_float.integer(a)
        : undefined
    );
}

function neg(a) {
    return (
        big_float.is_big_float(a)
        ? big_float.neg(a)
        : undefined
    );
}
```

有一组按位运算函数。实际工作由 `big_integer` 完成。

```
function bitand(a, b) {
    return big_float.make(
        big_integer.and(
            big_float.integer(a).coefficient,
            big_float.integer(b).coefficient
        ),
        big_integer.wun
    );
}
```

### 运行时如何工作

```
function bitdown(a, nr_bits) {
    return big_float.make(
        big_integer.shift_down(
            big_float.integer(a).coefficient,
            big_float.number(nr_bits)
        ),
        big_integer.wun
    );
}
```

```
function bitmask(nr_bits) {
    return big_float.make(big_integer.mask(big_float.number(nr_bits)));
}
```

```
function bitor(a, b) {
    return big_float.make(
        big_integer.or(
            big_float.integer(a).coefficient,
            big_float.integer(b).coefficient
        ),
        big_integer.wun
    );
}
```

```
function bitup(a, nr_bits) {
    return big_float.make(
        big_integer.shift_up(
            big_float.integer(a).coefficient,
            big_float.number(nr_bits)
        ),
        big_integer.wun
    );
}
```

```
function bitxor(a, b) {
    return big_float.make(
        big_integer.xor(
            big_float.integer(a).coefficient,
            big_float.integer(b).coefficient
        ),
        big_integer.wun
    );
}
```

你可能还记得来自 JSCheck 的 $f()$ 函数。

```
function resolve(value, ...rest) {
    return (
        typeof value === "function"
        ? value(...rest)
        : value
    );
}
```

有两种连接运算符。如果任一参数为 null，它们都返回 null。否则，它们会尝试将参数强制转换为文本。*cats* 函数会在两个操作数都不为空文本时添加一个空格分隔符。

```
function cat(zeroth, wunth) {
    zeroth = text(zeroth);
    wunth = text(wunth);
    if (typeof zeroth === "string" && typeof wunth === "string") {
        return zeroth + wunth;
    }
}

function cats(zeroth, wunth) {
    zeroth = text(zeroth);
    wunth = text(wunth);
    if (typeof zeroth === "string" && typeof wunth === "string") {
        return (
            zeroth === ""
            ? wunth
            : (
                wunth === ""
                ? zeroth
                : zeroth + " " + wunth
            )
        );
    }
}
```

然后是一些杂项函数。

```
function char(any) {
    return String.fromCodePoint(big_float.number(any));
}

function code(any) {
    return big_float.make(any.codePointAt(0));
}

function length(linear) {
    return (
        (Array.isArray(linear) || typeof linear === "string")
        ? big_float.make(linear.length)
        : undefined
    );
}
```

所有这些功能都打包到一个运行时对象中。

```
export default stone({
    abs,
    add,
    and,
    array,
    assert_boolean,
    bitand,
    bitdown,
    bitmask,
    bitor,
    bitup,
    bitxor,
    boolean_,
    cat,
    cats,
    char,
    code,
    default: default_function,
    div,
    eq,
    fail,
    fraction,
    function_,
    ge,
    get,
    gt,
    integer,
    integer_,
    le,
    length,
    max,
    min,
    mul,
    ne,
    neg,
    not,
    number,
    number_,
    or,
    record,
    record_,
    resolve,
    set,
    stone,
    sub,
    ternary,
    text,
    text_
});
```

# 第三十章

## Wat! 是如何工作的

> 别再取笑那些烂语言了。
> 咱们来聊聊 JavaScript。
> *Gary Bernhardt*

2012年1月12日，在俄亥俄州桑达斯基一个室内水上乐园举办的 CodeMash 会议上，Gary Bernhardt 进行了一场名为 *Wat* 的闪电演讲。

Bernhardt 展示了一些 Ruby 和 JavaScript 中的荒谬异常现象。每展示完一个例子，他就会放一张配着"WAT"字样的搞笑图片。观众们非常喜爱。这是一个经典桥段。*Wat* 已成为 JavaScript 界的*贵族们*。

他短暂表演的视频至今仍能在互联网上找到。许多模仿者继续制作类似的节目。有些人只是重复 Bernhardt 的材料，有些人则扩展了这个表演，添加了新的笑料。有些人能像 Bernhardt 一样博得观众的真笑，有些人只是让场面尴尬。

我在本书中一直尽量避免 JavaScript 的大多数糟糕部分，但在这一章里，我们要把怪物的裤子拉下来。我将向你展示一些来自 *Wat* 及类似演讲的笑料，并解释它们是如何工作的。这不会好笑，甚至不会令人愉快。

许多笑话源于 JavaScript 的 `==` 等于号等于号和 `+` 加号运算符背后的类型强制转换算法。类型强制转换规则复杂、难以记忆，而且在某些情况下，正如你将看到的，是错误的。这就是为什么我反对使用 `==` 等于号等于号。它实现了 ECMAScript 的抽象相等比较算法。那是一罐不值得打开的虫子。始终使用 `===` 等于号等于号等于号。始终如此。

有些人不喜欢 `===` 等于号等于号等于号，因为它看起来比 `==` 等于号等于号蠢50%，而 `==` 等于号等于号本身又是 `=` 等于号的两倍愚蠢。尽管如此，JavaScript 中正确的相等运算符是 `===` 等于号等于号等于号。避免使用 `==` 等于号等于号，那个不正确的相等运算符。

关于避免使用 `+` 加号，我无法给出类似的建议，因为 `+` 加号是唯一实用的数字相加方式。所以，享受这些虫子吧。

```
"" == false              // true
[] == false              // true
null == false            // false
undefined == false       // false
```

空字符串是一个假值，所以一个马虎的等于运算符可能想把它与 `false` 混为一谈。空数组不是假值，但它也能与 `false` 比较。而 null 和 undefined *确实* 是假值，但它们都不能与 `false` 比较。

```
WAT!
[] == []                    // false
[] == ![]                   // true
```

两个空数组不是同一个对象，所以它们不相等。但第二行令人惊讶。看起来 JavaScript 是一种 *x* 和 *not x* 可以彼此相等的语言，这将是一个极其可笑的无能之处。实际发生的情况是这样的：

空数组是真值，所以 `![]` 是 `false`。马虎的等于运算符想把 `[]` 和 `false` 当作数字来比较，尽管两者都不是数字。空数组被强制转换为空字符串，再强制转换为零。而 `false` 也被强制转换为零。零等于零，所以答案是 `true`。

```
WAT!
[] + []                     // ""
[] + {}                     // "[object Object]"
{} + {}                     // "[object Object][object Object]"
```

所有这些情况都应该产生 `NaN`。这就是 `NaN` 的用途。然而，因为这些值不是数字，`+` 加号想要连接它们。首先它必须将它们强制转换为字符串。`Array.prototype.toString()` 方法将空数组转换为空字符串。如果它像 `JSON.stringify()` 那样返回 `"[]"` 会更好。那个毫无价值的 `Object.prototype.toString()` 方法将对象渲染为 `"[object Object]"`。然后这些字符串被连接在一起。

```
WAT!
9999999999999999          // 10000000000000000
1e23 + 2e23 === 3e23      // false
```

大多数大于 `Number.MAX_SAFE_INTEGER` 的整数无法被精确表示。

```
WAT!
"2" < 5                    // true
5 < "11"                   // true
"11" < "2"                 // true
```

比较不同类型的值应该抛出异常。相反，JavaScript 尝试强制转换这些值以便进行比较。强制转换规则可能破坏传递性。

```
WAT!
1 < 2 < 3                  // true
3 > 2 > 1                  // false
```

这些情况本应是语法错误，因为语言不想正确处理它们。在第一种情况中，1 和 2 比较，产生 `true`。然后 `true` 和 3 比较。`true` 被强制转换为 1。1 小于 3，所以是 `true`。所以它意外地给出了正确答案。一个有时会给出正确答案的错误很容易通过测试逃过检测。

在第二种情况中，3 和 2 比较，产生 `true`。然后 `true` 和 1 比较。`true` 被强制转换为 1。1 不小于 1，所以它给出 `false`。

```
"2" + 1      // "21"
"2" -  Compound  // 1
```

其他算术运算符也会进行类型强制转换，但它们使用的规则与 `+` 加号截然不同。你应该正确管理你的类型以避免这种马虎。不要对字符串做算术。那是数字该做的事。

```
Math.min() > Math.max()    // true
```

这些函数很马虎。当未传入参数时，它们应该返回 `undefined` 或 `NaN`，或者干脆抛出异常。相反，`Math.min()` 返回 `Infinity`，而 `Math.max()` 返回 `-Infinity`。

```
Math instanceof Math      // throws exception
NaN instanceof NaN        // throws exception
"wat" instanceof String   // false
```

在 Java 中使用 `instanceof` 通常意味着未能理解如何使用多态性。JavaScript 的 `instanceof` 与 Java 的不同。我不建议在任何语言中使用 `instanceof`。

```
isNaN("this string is not NaN") // true
```

全局的 `isNaN` 和 `isFinite` 函数是坏掉的。请使用 `Number.isNaN` 和 `Number.isFinite`。

```
((name) => [name])("wat")   // ["wat"]
((name) => {name})("wat")   // undefined
```

第一个案例展示了胖箭头（或称 *fart*）函数的例子。fart 是一种简写的函数写法。fart 左边的是参数列表，右边的是表达式。表达式的值就是函数的返回值。你不需要写 `function` 或 `return`。在这个例子中，返回值是一个包含函数参数的数组。这很好。

第二个案例合理地应该返回 `{name: "wat"}`，而不是 `undefined`。不幸的是，JavaScript 假设 fart 后面的大括号是代码块，不是对象字面量。这个块包含一个变量名。自动分号插入在 name 后面塞了一个分号，把它变成了一个无用的什么都不做的表达式语句。缺少 `return` 语句，函数返回默认的返回值 `undefined`。

这就是为什么我建议避免使用 fart。它们也容易被与比较运算符 `<=` 和 `>=` 混淆。小小的打字便利根本不值得。



### 30.3 Wat! 是如何工作的

```javascript
function first(w, a, t) {
    return {
        w,
        a,
        t
    };
}
first("wat", "wat", "wat");  // {w: "wat", a: "wat", t: "wat"}

function second(w, a, t) {
    return
        {w, a, t};
}
second("wat", "wat", "wat");  // undefined
```

第一个 `return` 语句按预期工作，返回一个新对象。

第二个 `return` 语句仅在空格上有所不同，但它返回了 `undefined`。自动分号插入在 `return` 后面插入了一个分号。现在，对象字面量的左大括号处于语句位置，被视为一个代码块。该块包含一个无用的表达式语句。在表达式位置，逗号是一个运算符，而不是分隔符，因此这段代码不会产生语法错误。

自动分号插入不是一个特性。它是一个隐患。它被添加到语言中，专门针对那些可能不确定将分号放在哪里的初学者。你应该在希望你的代码看起来像是初学者编写的时候依赖自动分号插入。

WAT!

# 第31章

## 这本书是如何工作的

• • • • •

> 我只要求自由。蝴蝶也是自由的。

*哈罗德·斯金波尔*

### Include

为了帮助整合这本书，我制作了一个最终的 include 函数。我用它将各个章节文件组装成一个大的书籍文件。我用它将可执行的 JavaScript 源代码插入到各章中。我还用它将 JavaScript 代码片段组装成可以在 github.com/douglascrockford 上找到的 .js 文件。

```javascript
include(callback, string, get_inclusion, max_depth)
```

include 函数用其他字符串替换字符串中的 `@include` 表达式。如果没有 `@include` 表达式，则原始字符串就是结果。

你的 `callback(result)` 函数最终会收到处理后的结果字符串。

你的字符串可能包含零个或多个 `@include` 表达式。

```javascript
@include "key"
```

`@include` 和开头的 `"` 双引号之间有一个空格。每个 `@include` 表达式都会被与该键关联的包含字符串替换（如果可能的话）。键（可能是一个文件名）被包裹在圆括号中。

你的 `get_inclusion(callback, key)` 函数接受一个键字符串，并最终将结果包含字符串传递给 `callback(inclusion)`。你的 `get_inclusion` 函数可以访问文件系统、数据库、源代码控制系统、内容管理器或 JSON 对象。如果包含来自文件，并且环境是 Node.js，那么你的 `get_inclusion` 函数可能如下所示：

```javascript
function my_little_get_inclusion(callback, key) {
    return (
        (key[0] >= "a" && key[0] <= "z")
        ? fs.readFile(key, "utf8", function (ignore, data) {
            return callback(data);
        })
        : callback()
    );
}
```

如果某个包含包出了问题（已知托管包会这样做），使用 `my_little_get_inclusion` 它不会造成太大损害，但如果它可以直接访问 `fs`，则可能造成巨大损害。

一个包含字符串可能包含更多的 `@include` 表达式。`max_depth` 参数限制递归深度以防止无限的 include 循环。

这是实现：

```javascript
    const rx_include = /
        @include \u0020 " ( [^ " @ ]+ ) "
    /;
```

```javascript
    // 捕获组的描述：
    //  [0] 整个 '@include' 表达式
    //  [1] 键
```

```javascript
    export default Object.freeze(function include(
        callback,
        string,
        get_inclusion,
        max_depth = 4
    ) {
```

`include` 函数不需要直接访问或了解文件系统、数据库或其他任何东西，因为该功能是作为你的 `get_inclusion` 函数传入的。这使得 `include` 函数既通用又可信赖。没有返回值。结果最终通过回调进行通信。

```javascript
        let object_of_matching;
        let result = "";
```

助手及其助理完成所有工作。主助手搜索 `@include` 表达式，并将其发现传递给 `get_inclusion` 函数。`assistant_minion` 对 `include` 进行递归调用以处理包含。`junior_assistant_minion` 将处理后的包含附加到结果。

```javascript
        function minion() {
```

如果没有更多字符串要扫描，则交付结果。

```javascript
            if (string === "") {
                return callback(result);
            }
```

尝试对剩余字符串进行正则表达式匹配。

```javascript
            object_of_matching = rx_include.exec(string);
```

如果没有匹配，则我们的工作完成。

```javascript
            if (!object_of_matching) {
                return callback(result + string);
            }
```

表达式左侧的字符是结果的一部分。从字符串中删除已扫描的材料。

```javascript
            result += string.slice(0, object_of_matching.index);
            string = string.slice(
                object_of_matching.index + object_of_matching[0].length
            );
```

调用 `get_inclusion` 函数以获取替换字符串，传递 `assistant_minion` 和键。

```javascript
            return get_inclusion(
                assistant_minion,
                object_of_matching[1]
            );
```

```javascript
        function junior_assistant_minion(processed_inclusion) {
```

获取由 `include` 处理的包含并将其附加到结果。然后调用 `minion` 开始搜索下一个 `@include` 表达式。

```javascript
            result += processed_inclusion;
            return minion();
        }
```

```javascript
        function assistant_minion(inclusion) {
```

如果 `get_inclusion` 没有提供字符串，则将 `@include` 表达式添加到结果，从而有效地使该部分字符串保持不变。

```javascript
            if (typeof inclusion !== "string") {
                result += object_of_matching[0];
                return minion();
            }
```

包含可能包含自己的 `@include` 表达式，因此我们调用 `include` 来处理它们，并传递 `junior_assistant_minion`，将处理后的包含添加到结果中。`max_depth` 会减小以防止无限递归。

```javascript
            return include(
                junior_assistant_minion,
                inclusion,
                get_inclusion,
                max_depth - 1
            );
        }
```

这些是助手。现在回到 `include`。如果超出深度限制，则调用回调。

```javascript
        if (max_depth <= 0) {
            callback(string);
        } else {
            minion();
        }
    }));
```

### 版权页

Century Schoolbook 是一种过渡衬线字体，由 Morris Fuller Benton (1919) 设计。它基于其父亲 Linn Boyd Benton (1894) 的 Century Roman。New Century Schoolbook 是 Apple LaserWriter Plus 中包含的少数几种字体之一。由于当时字体的有限可用性，Century Schoolbook 被大量使用。由于过度曝光，它被认为是普通的、无趣的和乏味的。它现在已经有一个世纪的历史了，它仍然非常易读且出色。

章节标题使用 Daley Bold，我为本书设计的字体。它基于 Susan Kare 的 Chicago 12，原始的 Macintosh 系统字体。那些最初的菜单栏、下拉菜单、按钮和对话框都是用 Chicago 12 设置的。它是现代用户界面引入主流时最显眼的部分。为了消除位图锯齿，我借鉴了 Ronne Bonder 和 Tom Carnase (1970) 设计的 ITC Machine 的想法，使用直线而不是曲线。

代码字体是 Programma，我为本书设计的。它借鉴（偷）了 Aldo Novarese 和 Alessandro Butti (1952) 的 Microgramma、Raph Levien 的 Inconsolata 和 Sol Hess (1959) 的 Twentieth Century 的想法。

用于打印本书的可移植文档文件由 Prince 12 处理。www.princexml.com

封面由 Jim Cokas 设计。

本书由 Virgule-Solidus 出版。*Virgule* 是一个拉丁词，意思是 *斜杠*。*Solidus* 是一个拉丁词，意思是 *斜杠*。`//` *斜杠斜杠* 是万维网 URL 的重要组成部分，也是 JavaScript 和许多其他语言中注释的开始。

### 致谢

我要感谢 Edwin Aoki、Vladimir Bacvanski、Leonardo Bonacci、George Boole、Dennis Cline、Rolando Dimaandal、Bill Franz、Louis Gottlieb、Bob Hablutzel、Grace Murray Hopper、Matthew Johnson、Alan Karp、Gottfried Leibniz、Håkon Wium Lie、Linda Merry、Jeff Meyer、Chip Morningstar、Евгений Орехов、Ben Pardo、Claude Shannon、Steve Sounders、Tehuti，最重要的是，Lisa von Drake 教授。

### 片尾部分

在我的程序员生涯中，我经历了这些范式转变：

-   高级语言。
-   结构化编程。
-   面向对象编程。
-   函数式编程。

这些进步的最大受益者是那些现在能够以更少的努力完成更多更好工作的程序员。这些进步的最大反对者也是同样的程序员。他们对新的范式持怀疑、不安和不信任的态度。他们利用自己的智慧和经验，构建了看似令人信服的论点，但事后看来，它们只是错误的。他们



### 本书的工作方式

31.4

那些使用旧范式取得成功的人不愿意接受新的范式。要区分新范式和真正糟糕的想法可能非常困难。

每次范式的转变都需要二十年以上才能被广泛采用。函数式编程则需要两倍的时间。耗时如此之长的原因在于我们无法改变人们的想法。我们必须等待一代程序员退休或离世，才能在下一个范式上获得临界质量。

马克斯·普朗克在物理学中观察到了类似的现象，现在被称为普朗克原理。他写道：

> 一项新的科学真理之所以获胜，并不是因为说服了对手并让他们看到光明，而是因为对手最终死去，而熟悉它的新一代成长起来。

他也更简洁地表达过：

> 科学进步，葬礼一場接一场。

我想现在应该很明显，下一个范式是分布式最终编程。这并不是一个新想法。它至少可以追溯到演员模型的发现（1973年）。自那以后，我们取得了一些进步，但也在远程过程调用等方面犯了错误——试图在坚持顺序编程模型的同时做分布式的事情。我认为 JavaScript 之所以有趣，是因为它专门为实现分布式最终编程而创建。由于仅用十天开发而成，它并未做到尽善尽美。它也是一种多范式语言，鼓励保留旧范式。而且自创建以来，旧范式的拥护者们一直试图将 JavaScript 拉回其 FORTRAN 的根源。

### 还有一件事

通读这些内容时，你可能已经注意到了 **wun** 这个奇怪的拼写。它可能让你分心、困惑或恼怒。反对这种拼写的论点都是基于传统的。它不是我们习惯的写法。不是我们被教导的写法。不是我们熟知的样子。这些都没错，但按照英语发音的规则，**wun** 才应该是正确的拼写。这是一个 bug 修复。

我们对 **wun** 的情感反应与我们对新范式的情感反应是一样的。

在离世之前采纳新范式的秘诀是去体验它。这在编程中比在物理中更容易做到，因为你只需要写出好的程序。我可以谈论返回函数的函数，你也能理解这些词语，所以自以为理解了那是什么。但事实上，在你亲身体验之前，你无法真正理解它。大量地写返回函数的函数。大量地写进行尾调用的函数。你会到达一个点，在那里它不再显得不自然。你无法通过阅读或谈论来达到那个境界。如果你用 JavaScript 写得好，JavaScript 就会教你。如果你用 JavaScript 写得差，JavaScript 就会惩罚你。但你已经知道这一点了。

也许在我的下一本书中，我们会对 **two** 的拼法做点什么。

### 注释

> 音乐是音符之间的静默。
> *克洛德·德彪西*

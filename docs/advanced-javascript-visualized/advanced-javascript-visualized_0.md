# JavaScript 高级可视化指南




谨以此书献给我的工程学，它让我意识到我应该早点开始写作 :)

> 智慧真正的标志不是知识，而是想象力。
> ——阿尔伯特·爱因斯坦

## 1. 执行上下文、线程与调用栈

我们都知道，从你或我开始学习 JavaScript 的那一天起，我们就一直对它爱恨交织。但是，如果我们深入挖掘基础原理，那些围绕 JavaScript 奇怪概念背后的哲学往往很容易理解。

这是所有章节中最重要、最基础的一章。所以如果你掌握了这一章，那么几乎所有的内容都会变得容易理解和掌握。欢迎踏上超越常规期望的 JavaScript 激动人心之旅。

---

### 术语

*   内存
*   进程与线程
*   执行上下文
*   作用域
*   执行线程
*   调用栈

`内存`：计算机只是一台接收指令集并执行它们的机器，但在执行过程中，计算机需要保存一些信息用于计算或其他任务。因此，我们有像 RAM 和 ROM（HDD、SSD）这样的存储设备，它们临时或永久地保存信息。所以，内存只是我们保存信息的一部分。

`进程`：当前正在执行/运行的程序（打包的指令集）称为进程。每个进程只是计算机为完成给定任务所需执行操作的蓝图。

`线程`：进程是一组打包的指令，但每个指令也需要被执行才能完成原始进程，因此线程只是一个简单的轻量级运行进程（正在执行的一小组指令）。

`执行上下文`：它只是内存中当前正在运行的代码（每个运行的程序都需要内存），可以是普通的函数执行或普通的 JavaScript 代码，如 `if-else`、循环或任何其他表达式。
`内存 + 进程 == 执行上下文`

`作用域`：作用域是为特定或当前正在执行的函数或代码块分配的内存。也就是说，变量（内存）在其外部对函数或代码块不可用。
`作用域 == 执行上下文的内存限制`

`执行线程`：当前正在运行（执行）的函数或代码块是一个执行线程。也就是说，它是我们主进程内部的一个小型运行进程。

`调用栈`：它是一个容器，你可以在其中添加或移除代码块/函数，使得最近添加的内容在此容器中获得下一个执行线程的优先级。也就是说，后进先出（LIFO）模式。

在进一步讨论之前，让我先快速概述一下进程在高级层面是如何管理的。

1.  最初，任何程序（指令集）都被内存（通常是 RAM）收集，然后处理器开始执行该程序。
2.  处理器随后获取程序并开始执行，在此过程中，处理器可能需要执行额外的工作来完成给定任务，即处理器可能执行程序内部的程序（指令集可能需要其他指令），也就是线程也需要完成。
3.  程序完成后，操作系统将负责清理和其他一些依赖任务。
4.  现在，当给定程序可以逐个执行一组指令，并且没有执行额外的内部指令集时，该程序被称为**单线程**（运行 JavaScript 程序是一个单线程进程）。

***

在了解了术语之后，让我们通过一个小例子进一步理解这些内容。

#### 示例 1.1

*   首先，如果你不知道的话，JavaScript 是一种单线程且同步的语言，这意味着 JavaScript 引擎/解释器一次只能执行一行或一个代码块。也就是说，你不能同时做多件事。此外，在执行代码时，你会逐行进行（同步）。
*   当你在浏览器或任何其他环境（`nodejs`、`react-native` 等）中执行 JavaScript 代码时，我们在所谓的全局执行环境（首先是浏览器标签页的全局内存空间，或 node 环境的全局内存）中运行代码。
*   我们定义的每个函数实际上首先进入全局内存空间（暂时忽略在另一个函数内部定义的函数）。当我们将这些函数投入执行时，它们首先被放入 `调用栈`，然后从该 `调用栈` 中调用函数，其中最新的函数在执行线程中可用！
*   在我们开始理解给定代码之前，为我们目前学到的所有内容建立一个“心智模型”非常重要。

#### 当前 JavaScript 心智模型

*   在我们的心智模型中，我们可以看到每个 JavaScript 程序都会获得全局内存空间（全局作用域）。每个函数和顶层声明的变量都会被提升到全局作用域。
*   `提升` 是 JavaScript 的默认行为，它将所有声明移动到当前作用域的顶部（当前脚本或当前函数的顶部）。
*   在 JavaScript 中，每一行代码或函数定义都不会被直接调用。相反，它会进入 `调用栈`，然后根据 `调用栈` 的当前优先级，函数被放入执行线程中（后进先出）。

#### 示例 1.1 分析

*   在第一行中，如你所见，我们声明了一个名为 `outerGoal` 的变量，并为其赋值 `0`。也就是说，我们在全局内存（作用域）中消耗了一小块内存空间，并为该内存贴上了 `outerGoal` 的标签。
*   在下一行代码中，我们只是将该值记录到控制台。也就是说，我们只是记录标签 `outerGoal` 处的值。





## JavaScript 执行心理模型

有一点需要注意，我不会绘制全局执行线程图，但它始终在我们开始执行 JavaScript 代码时启动。

让我们再次看看我们的`心理模型`如何应用于当前情况。

![Image](img/Image00003.jpg)
*当前的 JavaScript 心理模型*

让我们进一步理解下面的代码：

![Image](img/Image00004.jpg)
*示例 1.1*

*   我们可以看到，我们正在声明一个函数（JS 中一种特殊的对象类型）并为其赋予标签 `addGoal`。
*   请注意，这个函数声明有一个名为 `count` 的参数，这意味着 `count` 是一个未来内存空间地址的标签，该地址稍后将被此函数占用。
*   在函数定义内部，我们所做的任何操作目前都不那么重要（在调用它时会详细讨论）。
*   在函数定义之后，我们实际上在全局作用域中声明了变量 `storedEvaluatedValue`，它将接收来自 `addGoal` 函数调用的返回值或计算值。
*   如果你没注意到的话，我们在这里并没有离开全局作用域或全局执行线程。

是时候再次查看我们的`心理模型`了。

![Image](img/Image00005.jpg)
*当前的 JavaScript 心理模型*

让我们继续对代码的理解：

*   这里到了关键部分，我们通过在 `addGoal()` 后面加上括号来调用它。一旦我们这样做，就会创建一个全新的执行上下文（或该函数的局部内存空间）。
*   需要知道的是，执行上下文的创建在 JavaScript 中并非凭空发生。实际上，当我们调用一个函数时，我们并不是直接将该函数放入执行线程，而是先将其放入调用栈（call stack）中。
*   记住，`栈`数据结构意味着后进先出（LIFO），这意味着如果我们把一个函数调用放入调用栈，只要紧接着没有额外的函数调用，我们就会取出调用栈最顶端的函数并将其放入执行线程。

再次回到我们的`心理模型`。

![Image](img/Image00006.jpg)
*当前的 JavaScript 心理模型*

在进一步深入之前，我们需要了解局部作用域以及局部作用域内部发生了什么。

![Image](img/Image00007.jpg)
*局部函数及其作用域的心理模型*

*   正如你在执行线程中的函数执行所看到的，它会创建局部内存，并且我们在该调用内部操作一个名为 `innerGoal` 的局部变量。
*   但有一点需要注意，参数 `count` 也是局部内存的一部分，这意味着参数只有在我们运行函数时才变成实参，并且只有在被使用时才占用内存空间。`占位符`或所谓的`参数`并不占用空间。
*   在函数体即将执行完毕后，我们返回 `innerGoal` 变量。也就是说，它的值带有 `innerGoal` 标签。
*   当我们退出函数执行时，JavaScript 引擎会销毁局部函数执行上下文。如果函数返回一个值，那么该值将成为该函数的计算值，否则默认返回 `undefined`。

![Image](img/Image00008.jpg)
*局部作用域执行的心理模型*

![Image](img/Image00009.jpg)
*当前执行的心理模型*

![Image](img/Image00010.jpg)
*执行后的最终心理模型*

### 快速笔记：变量是如何存储的

*   请始终记住，计算机是由大量空间（内存地址）组成的。
*   当我们存储/使用一个空间时，实际上是在使用计算机的这些内存地址。
*   因为人类不擅长记住这些内存地址，所以我们给它一个标签（变量名），该标签指向该内存地址。

### 总结 (TLDR)

*   任何编程语言的心理模型都非常重要，它在理解核心概念方面起着卓越的作用。
*   请记住这个心理模型以应对后续章节，你将享受学习的乐趣。

---

## 闭包 - 深度解析

```
说到像 JavaScript 和 Python 这样被广泛使用的编程语言，我们不能直接或间接地忽略其最常用的特性——“闭包”。因此，让我们了解一下它的底层工作原理。此外，在开始之前，让我们先了解 JavaScript 函数究竟是什么？！
```

### JavaScript 函数

*   JavaScript 函数是一个`对象 (Object)`！
*   JavaScript 中的`对象`意味着它可以拥有键值对，没有比这更复杂的东西。（我们将在“原型章节”中详细讨论`对象`）。
*   函数是一种特殊类型的`对象`，其特殊之处之一是可以存储代码块并在以后需要时调用（运行）它们！
*   因为函数是一个`对象`，我们也可以在函数中存储键值对，如果你来自其他编程语言，这看起来可能有点奇怪。但事实确实如此！

### JavaScript 函数是一等公民

*   你可以将**函数作为参数传递**给另一个函数，用于各种不同的目的。
*   我们可以有一个函数被另一个函数返回，或者我们可以将匿名函数存储在变量中（存储在内存中）。
*   每个函数都有自己的**局部内存/局部变量作用域**（在第一章中已解释）。

> 能够向函数添加任何键值对的特性是一种“超能力”，而这种超能力帮助 JavaScript 实现了一个神奇的特性，叫做`闭包 (closure)`。让我们看看是如何实现的！

> 互联网上有关于闭包的定义，但没有一个真正帮我理解它底层到底是如何运作的。经过一些研究和实验，我终于明白了它真正的含义以及底层的工作原理。让我们通过示例来看看。

![Image](img/Image00011.jpg)
*函数是对象*

*   如上面的示例所示，我们创建了一个名为 `calmMan` 的函数，随后使用对象字面量语法向函数本身添加了 2 个属性。
*   这些属性成为了我们函数对象的一部分，并始终附加在它上面。让我们看看它们在底层是什么样子！

![Image](img/Image00012.jpg)
*函数的内部结构*

*   从图中我们可以看到，这两个属性都属于该函数对象且是其一部分。我们还可以看到一些由 JavaScript 自身添加的用于内部使用的其他属性（键值对）。
*   现在，我们有了证明，函数是`对象`并且可以在自身中持有属性。那么，如果这些函数在内部使用这些键值对，并将这些键值对提供给我们呢？朋友们，魔法就在这里开始了。
*   顺便说一下，如果你注意到上面的图片，JavaScript 已经提供了 2 个这样的内部属性（键值对）（即 `[[Scopes]]`）。我们将深入研究这一点，但现在让我们先来看闭包的正式定义并理解它。

#### MDN 定义

```
闭包是将函数与引用其周围状态（词法环境）组合在一起（封闭）的组合。换句话说，闭包允许内部函数访问外部函数的作用域。在 JavaScript 中，闭包在每次创建函数时都会创建，即在函数创建时。
```

第一次接触时这并不容易掌握，而且我不喜欢 MDN 的定义和这里的解释。

#### W3SCHOOL 定义

```
JavaScript 变量可以属于局部作用域或全局作用域。
全局变量可以通过闭包变为局部（私有）变量。
```

我不倾向于将 w3school 作为可靠的来源，但这一次我觉得 w3school 实际上更精准、更容易掌握，并且定义清晰。

现在轮到我们通过可视化来理解了，为此，我将举一个简单的例子。

![Image](img/Image00013.jpg)
*函数定义*

![Image](img/Image00014.jpg)
*函数执行*




我们在这里介绍第一个关于函数定义的心智模型。

![Image](img/Image00015.jpg)

*   根据当前的心智模型，你可以看到，从全局内存空间到调用栈，再从调用栈到执行线程，我们已经将 `createCapitial` 函数投入执行。
*   `createCapital` 函数拥有自己的局部作用域（环境），在其中我们定义并存储了 `getCapital` 函数。
*   现在，让我们看看当我们执行完 `createCapital` 并返回 `getCapital` 时会发生什么。
*   你最可能的猜测是，`createCapital` 的整个函数体和局部作用域将被销毁，而 `getCapital` 函数将被存储在名为 `accessCapital` 的变量中。让我们再次查看我们的心智模型。

![Image](img/Image00016.jpg)

正在执行的 `createCapital` 函数

![Image](img/Image00017.jpg)

正在执行的 `getCapital` 函数

*   从这两张图中可以看出，我们终于到了将 `getCapital` 函数投入执行的地步（使用了 `accessCapital` 变量，它指向我们原始的 `getCapital` 函数定义）。
*   但是，等等，按照常规行为，我们期望在执行 `getCapital` 时，变量 `wealth` 应该是 `undefined`，并且它不应该能访问已执行函数（即 `createCapital` 的内存）的局部内存。然而，生活并没有那么简单，老兄😅‼
*   现在引入一个新朋友，叫做 `backpack`（背包），来拯救局面。

```
背包是一个简单的内存存储，带有与之相连的绳子（想象成一个真正的背包🎒），而这些背包的绳子将连接到何处是一个问题🤔。
```

让我们实际可视化一下，当我们的外部函数 `createCapital` 执行完毕时，到底发生了什么！

![Image](img/Image00018.jpg)

将背包附加到内部函数

![Image](img/Image00019.jpg)

正如你所见，我们的背包不过是外部函数作用域中的变量，当 JavaScript 看到这种外部作用域与内部作用域结合的情况（外部函数返回内部函数）时，它不会清除内存，而是将这些变量作为内部函数的内部属性保留下来！

此外，如果我们想查看这些内部属性，也是可以的。让我们看看下面这张图中它们在哪里！

![Image](img/Image00020.jpg)

隐藏的背包

*   如上所示，外部函数（`createCapitial`）的局部作用域（局部内存）被附加到了内部函数的内部键值对中！（`[[Scope]]`）。
*   `[[Scope]]` 键包含 3 个数组元素，第一个元素存储了我们的背包内存，也就是说，它就是我们的 `Closure`（闭包）。
*   此外，该函数的第二个元素实际上说明了这个 `Closure` 属于哪个函数！
*   最后一个元素实际上是我们的全局作用域，它对每个函数都是可用的（就像每个函数对象的全局闭包）。
*   就是这样，朋友们。这就是带有心智模型的闭包😎！
*   我们可以举一个例子来更好地理解它。因为即使不从外部函数返回内部函数，我们也可能拥有闭包。让我们通过一个例子来看看。

![Image](img/Image00021.jpg)

*   这个例子与前一个几乎相同，只是这里我们返回的是一个对象而不是函数。然而，这个对象中包含一个函数。让我们也开始可视化。

![Image](img/Image00022.jpg)

![Image](img/Image00023.jpg)

*   函数中的参数也是函数执行时局部内存的一部分。

![Image](img/Image00024.jpg)

*   当外部函数执行完毕被销毁时，对象内部的函数将获得外部函数的局部内存。请看下面😁。

![Image](img/Image00025.jpg)

![Image](img/Image00026.jpg)

![Image](img/Image00027.jpg)

*   如图所示，即使没有外部函数，我们现在也能通过闭包访问它的变量。此外，请注意，**局部变量和参数**都通过闭包变得可用。

![Image](img/Image00028.jpg)

*   最后，我们完成了执行，控制台输出了结果。

![Image](img/Image00029.jpg)

以上就是关于闭包的全部内容，朋友们。有时他们也把我们的闭包/背包称为 **“词法作用域”**。在进入下一章并开始新的可视化旅程之前，让我们快速记一下。

```
每当我们有一个包含函数属性的对象，或者函数内部嵌套函数时，即使父（外部）函数执行完毕，所有周围的变量也会通过闭包变得对对象的函数属性或内部函数可用。我们通过例子理解了这一点。在后面的章节中，我们也会用到这个概念。
```

* * *

# 3

# 原型、__proto__ 与对象

```
如果你来自其他编程语言，或者脑海中有着传统的面向对象编程概念，那么这一章将彻底转变你的思维。JavaScript 及其原型本质是一个完全不同的概念。此外，JavaScript 的许多特性试图模仿其他编程语言的语法，因此产生了大量混淆。在本章中，我们将通过可视化深入探讨事物在底层是如何工作的。
```

让我们从非常简单的东西开始，那就是**对象**。

### 对象

*   在 JavaScript 中，对象就是键值对（你可以将其视为一组变量的集合）。
*   然而，仅仅因为键值被放在一起，并不意味着它们在内存中也是连续存储的。在底层，所有变量都随机存储在内存中，但指向这些变量的引用知道如何根据访问的键精确地定位值。
*   看看下面的对象是如何存储在计算机内存中的。

![Image](img/Image00030.jpg)

![Image](img/Image00031.jpg)

展示上述图表的主要目的是说明，逻辑上放在一起的值并不是它们在内存中的实际存储方式。

### 对象与原始值

*   在 JavaScript 中，除了**原始值**（字符串、数字、布尔值等）之外，一切都是**对象**。
*   **函数也是对象。**
*   **数组是对象。**
*   **Math、Date 以及其他辅助函数也都是对象。**
*   在所有这些东西中，函数是最重要的。函数是对象，但它是特殊类型的对象。
*   函数有两个可用的部分。第一部分是函数体，我们可以在其中存储代码块，并在需要时调用它。第二部分是对象部分，我们可以在其中存储键值对。

![Image](img/Image00032.jpg)

*   我们在第 2 章中已经看到了证据，当时我们向函数对象添加了属性（如果忘记了，请重新检查😅）。在这里，我们将进一步了解我们可以做什么，或者有哪些东西可供我们使用。
*   有趣的是，每个函数对象默认都有一个 `prototype` 属性，而每个对象也都有一个 `__proto__` 属性。
*   因此，每个函数都将拥有 `prototype` 和 `__proto__` 属性，而每个对象都将拥有 `__proto__`（普通对象没有 `prototype` 属性，只有函数对象才有）。

![Image](img/Image00033.jpg)

*   在本章中，我不会绘制整个 JavaScript 环境，因为这里不需要，我们将纯粹关注对象和函数及其链接是如何工作的。让我们从下面一个简单的例子开始（现在不要试图理解，我们马上会做）。

![Image](img/Image00034.jpg)

*   如你所见，我们创建了 `ArtistCreator` 函数，它帮助我们创建对象。你可以把它看作一个创建艺术家对象的通用函数。我们很快就会将其可视化，但在此之前，让我们先理解 `Object.create()` 为我们做了什么。

![Image](img/Image00035.jpg)

*   JavaScript 中有很多全局对象（键值对）可供我们使用。`Object`（注意是大写字母 O）就是其中之一。它包含许多键值对，并且由 JavaScript 提供。





*   `create` 是 `Object` 的一个方法，它有以下基本任务。
    1.  创建一个空对象。
    2.  由于每个对象都有 `__proto__` 属性，在创建空对象后，我们传递给 `create` 方法的任何参数，都会直接通过 `__proto__` 提供给新创建的对象。让我们看看具体是如何实现的。
    ![Image](img/Image00036.jpg)
    ![Image](img/Image00037.jpg)
*   我们正在执行 `ArtistCreator` 函数，它调用了 `Object.create()` 方法，并将全局存储的 `commonFunctionality` 对象作为参数传入。
    ![Image](img/Image00038.jpg)
*   `Object.create()` 不仅创建了一个新的空对象，还为这个新对象的 `__proto__` 添加了一个指向全局存储的 `commonFunctionalities` 对象的引用**。** 因此，我们传递给 `create()` 的第一个参数的所有内容，都会通过新创建对象的 `__proto__` 属性可用。让我们完成可视化。
    ![Image](img/Image00039.jpg)
    ![Image](img/Image00040.jpg)
    ![Image](img/Image00041.jpg)
    ![Image](img/Image00042.jpg)
    ![Image](img/Image00043.jpg)
*   如你所见，我们可以通过函数创建新对象，而且还可以反复重用这个函数。
    ![Image](img/Image00044.jpg)
*   如果我们再次运行同一个函数，如上所示，我们仍然可以重用它的功能，并且还可以利用已经声明的 `commonFunctionalities`。请看下面的图示，我们对 `artist2` 对象也做了同样的操作（请像上面展示的那样，自己走一遍心智模型）。
    ![Image](img/Image00045.jpg)
*   好了，我们已经创建了一个功能，允许我们在需要时创建对象，并且可以重用一些现有的功能。现在，如果 JavaScript 本身就提供了这种特性，那该多好啊😋。
*   幸运的是，它确实有，而这正是我们接下来要做的。请看下面的示例，我们很快就会理解。
    ![Image](img/Image00046.jpg)
*   如果你忘记了，函数默认拥有 `prototype` 和 `__proto__` 属性。同样地，`ArtistCreator` 也会拥有这些属性。让我再次展示那张图。顺便提一下，`prototype` 是一个对象，我们可以向它添加任意键值对。
    ![Image](img/Image00047.jpg)
*   现在，向 `prototype` 对象中添加什么内容由我们决定。在我们的示例中，我们添加了两个函数：`isHuman` 和 `isCuriuos`。
    ![Image](img/Image00048.jpg)
*   注意，我们的示例现在也使用了 `new` 关键字。它在幕后做了大量的自动化工作。让我们看看它的图示是怎样的。
    ![Image](img/Image00049.jpg)
*   让我们执行下面这行代码，注意函数调用前面的 `new` 关键字。
    ![Image](img/Image00050.jpg)

`new` 关键字主要做两件事。

1.  它会创建一个新的**空对象**，并且这个新创建的对象会获得 `this` 引用。这意味着在函数执行过程中，`this` 将指向由 `new` 关键字创建的新对象。
2.  此外，函数的 `prototype` 对象（在我们的示例中是 `ArtistCreator` 函数）中的所有内容，都会指向新创建对象的 `__proto__`（当然，我们来可视化一下😅）。

![Image](img/Image00051.jpg)

*   每个函数对象都有两部分，我们知道，一部分是函数体，另一部分是对象部分。
*   在下面的图示中，你可以看到 `ArtistCreator` 的对象部分包含一个 `prototype` 对象和一个 `__proto__` 对象。
*   在我们的代码中，我们向 `prototype` 对象添加了两个函数：`isHuman` 和 `isCurious`。
*   每个对象默认都拥有 `__proto__` 属性。这就是为什么 `prototype` 对象也拥有 `__proto__` 属性（这个属性指向哪里尚不清楚，但让我们先专注于代码的执行）。
    ![Image](img/Image00052.jpg)
*   函数的 `prototype` 对象指向新创建对象的 `__proto__` 属性。
*   现在，我们知道 `new` 关键字帮助我们建立了 `prototype` 对象到新创建对象的 `__proto__` 属性的引用。请看下面。
*   还有一点，函数执行已经结束，但函数的对象部分仍然保留在全局内存中。这里我们并不是复制对象，而只是设置引用。
    ![Image](img/Image00053.jpg)
    ![Image](img/Image00054.jpg)
*   永远不要忘记，函数执行已经完成，但该函数的内存并不会被清除。这就是为什么带有 `prototype` 对象的 `ArtistCreator` 函数会保留在内存中。
    ![Image](img/Image00055.jpg)
*   就是这样，我们现在能够通过函数创建对象，并且一些公共功能也可以通过 `prototype` 对象获得。
*   现在，`artist2` 也是同样的道理，所以我就不再画那部分了（现在你可以自己可视化😎）。
    ![Image](img/Image00056.jpg)
    ![Image](img/Image00057.jpg)
*   我们使用函数创建对象，因此我们称之为“函数构造函数”。所以，这里的 `ArtistCreator` 就是构造函数。
*   在结束上面的示例之前，让我们在浏览器控制台中输出结果。
    ![Image](img/Image00058.jpg)
*   到目前为止一切顺利，但 ES6+ 为我们提供了新的语法糖，它可以实现与上面代码相同的功能。它只是试图模仿并简化语法。在底层，工作原理保持不变。让我们看看上面示例的等效代码。
    ![Image](img/Image00059.jpg)
*   `class` 关键字是在 ES6+ 中引入的，用于模仿我们之前的工作。
*   并不复杂，只是我们的 `prototype` 方法直接定义在 `class` 内部，而 `constructor` 充当函数体。

> 我们已经学会了如何通过 `函数构造函数` 创建动态和自定义的对象。那么，如何扩展我们的功能，并利用现有的 `函数构造函数` 来创建另一个 `函数构造函数`，从而帮助我们继承其他特性呢？让我们通过一个示例来看一下*😁*。首先，我们将采用**非类**版本的示例，然后创建等效的类版本。

![Image](img/Image00060.jpg)

*   如果你不理解上面的代码，不用担心，我们将逐步解释它是如何工作的。上面示例中唯一需要注意的是，我们可以将 `ArtistCreator` 的 `prototype` 函数继承到我们新创建的 `Entrepreneur` 的 `函数构造函数` 中。让我们开始可视化😋。
    ![Image](img/Image00061.jpg)
*   我们首先可视化上面这行代码。这将与我们刚刚展示的之前的示例类似。
    ![Image](img/Image00062.jpg)
    ![Image](img/Image00063.jpg)
    ![Image](img/Image00064.jpg)
    ![Image](img/Image00065.jpg)
    ![Image](img/Image00066.jpg)
    ![Image](img/Image00067.jpg)
*   到目前为止，这与之前示例的可视化相同。现在，让我们看看运行下面代码时会发生什么。
*   另外，我在这里跳过了第 298 到 303 行的执行，因为我不想让接下来的图示让你感到困惑。实际上，我们将在完成下面高亮行的执行后，再展示第 298 到 303 行的图示。
    ![Image](img/Image00068.jpg)
*   不要忘记，即使执行结束，`ArtistCreator` 的对象部分仍会保留在内存中，当我们再次调用 `ArtistCreator` 时，我们将使用内存中存储的引用，而不是创建它的副本。
    ![Image](img/Image00069.jpg)
    ![Image](img/Image00070.jpg)
*   我们使用 `call` 关键字调用一个函数，并将 `this` 作为第一个参数传递。

```
call() 方法使用给定的 this 值和单独提供的参数来调用一个函数。
```

*   因为我们在 `Entrepreneur` 函数前面使用了 `new` 关键字，所以我们将创建一个新的空对象，并且 `this` 关键字将指向它。然而，`Entrepreneur` 内部使用 `call()` 方法调用了 `ArtistCreator`，并传递了新创建的对象（此时 `this` 关键字指向新创建的空对象！）。
    ![Image](img/Image00071.jpg)
*   这里我们只是向新创建的对象添加属性。
    ![Image](img/Image00072.jpg)




* 实际上，参数是通过引用传递给 `ArtistCreator` 函数的，而 `Entrepreneur` 函数提供了这些值😅。跟着图示走，你就能理解。

![Image](img/Image00073.jpg)

* 默认情况下，新创建的对象（`this`）会拥有其诞生处原型对象的引用。

* 在我们的例子中，我们使用 `ArtistCreator` 作为新创建对象的“母体”。因此，新创建对象的 `__proto__` 将指向 `ArtistCreator` 的原型对象。

![Image](img/Image00074.jpg)

* 执行完 `ArtistCreator` 函数后，我们将继续执行 `Entrepreneur` 函数，并在新创建的（`this`）对象上添加一个属性 `communicationSkill`。

* 我在这里保留了函数的对象部分，因为这有助于我们更好地理解。

![Image](img/Image00075.jpg)

* 另外，如你所见，我们现在也完成了 `Entrepreneur` 函数的执行。

![Image](img/Image00076.jpg)

* 现在，关键部分来了。记得我之前让你忽略第 298 到 303 行吗？让我们看看当执行它们时（实际上执行已经完成，但我现在展示是因为这样更容易可视化），它们在幕后发生了什么。

![Image](img/Image00077.jpg)
![Image](img/Image00078.jpg)

* 如我们所知，`Object.create()` 会创建一个空对象，而刚创建的空对象的 `__proto__` 将指向我们传递给 `create()` 方法参数的任何内容。

![Image](img/Image00079.jpg)

* 因为我们重新赋值了 `Entrepreneur.prototype`，所以 `Entrepreneur` 的旧原型对象将从内存中销毁。我们从 `Object.create()` 方法调用中得到的任何内容都将赋值给 `Entrepreneur.prototype`😃。

![Image](img/Image00080.jpg)

* 我们还在 `Entrepreneur.prototype` 对象上添加了一个属性，即 `hasPatience` 函数。

* 我们将 `ArtistCreator.prototype` 对象传递给 `Object.create()` 方法。因此，`ArtistCreator` 的原型对象将指向新创建的空对象的 `__proto__`。

![Image](img/Image00081.jpg)
![Image](img/Image00082.jpg)

* 如我们所知，函数的原型对象会保留在内存中，这就是为什么它在图中显示的原因。

* 看看 `__proto__` 及其链接是如何工作的😎。

![Image](img/Image00083.jpg)
![Image](img/Image00084.jpg)

```
Woooh, we finally completed our visualization(if you find it a little confusing then just go through it again😅, the first time it always seems a little too much to digest.)
```

* 让我们看看控制台中的输出。将上面的图与下面的输出对比，你就会明白😅。

![Image](img/Image00085.jpg)

### 我们实现了什么🤔

> 我们从之前的例子中学到了一个重要的东西。我们实际上能够创建动态对象，并重用其他对象和函数的现有功能（不要称之为继承😅，这里我们是在组合，而不是继承）。

* 那么，如果 ES6+ 提供了上述功能的语法糖呢🤨。实际上，我们有更简单的语法来实现与上述相同的功能。

* 这里，实现相同功能的方式略有不同。让我们看看。

![Image](img/Image00086.jpg)
![Image](img/Image00087.jpg)

* 让我们从下面这行简单的类执行开始，并将其可视化。

![Image](img/Image00088.jpg)
![Image](img/Image00089.jpg)

* 在 `class` 中，我们应该记住 `constructor` 方法位于其原型对象上。因此，每当我们尝试使用 `new` 关键字执行类时，都会使用原型对象中的这个 `constructor` 方法（`class` 是函数的语法糖，而函数总是有原型对象）。

* 看图示，我们正在执行 `ArtistCreator` 类的 `constructor`。

![Image](img/Image00090.jpg)

这里，`this` 关键字将指向由 `new` 关键字创建的新对象。

![Image](img/Image00091.jpg)

根据下图，我们发现使用 `class` 时，我们添加了一个用于创建新对象的函数体，并将其命名为 `constructor`，然后将其放在类的原型对象上。

![Image](img/Image00092.jpg)

我认为 `ArtistCreator` 类的执行很容易理解。现在让我们看看执行下面这行时会发生什么🤨。

![Image](img/Image00093.jpg)
![Image](img/Image00094.jpg)

注意这里，有两个主要部分：
1. `extends` 关键字
2. `constructor` 内部的 `super` 关键字。

#### extends

* `extends` 关键字在幕后将当前类（这里是我们例子中的 `Entrepreneur`）的 `__proto__` 引用设置为父类的构造函数（这里是我们例子中的 `ArtistCreator.prototype.constructor`）。

* 根据图示，我们可以看到 `Entrepreneur.__proto__ = ArtistCreator.prototype.constructor`。

#### super

* `super` 关键字发送一个命令，调用 `Entrepreneur.__proto__` 上可用的方法。这里它指向父类（`ArtistCreator.prototype.constructor`）的 `constructor`。

* 另外，`super()` 调用内部的 `this` 关键字也会创建一个空对象。让我们继续可视化。

![Image](img/Image00095.jpg)
![Image](img/Image00096.jpg)
![Image](img/Image00097.jpg)
![Image](img/Image00098.jpg)

* 执行完 `super()` 调用后，我们回到当前类（`Entrepreneur`）的 `constructor` 调用中。

* 在 `Entrepreneur` 的原型对象中，我们有它自己的 `constructor` 的引用，接下来我们将执行它。

![Image](img/Image00099.jpg)

* 在 `Entrepreneur` 的 `constructor` 函数体内，我们向新创建的对象添加了另一个属性。

![Image](img/Image00100.jpg)
![Image](img/Image00101.jpg)

现在，最后一点是新创建对象的 `__proto__` 将引用 `Entrepreneur.prototype` 对象。见下图。

![Image](img/Image00102.jpg)

所以，长话短说。以下是使用 `new` 关键字调用 `Entrepreneur` 类时逐步发生的情况：

1. 从 `super()` 调用中创建一个空对象，`this` 关键字将指向我们新创建的对象。
2. 从 `super()` 调用中添加所有属性（参见图示/代码）。
3. 新创建对象的 `__proto__` 指向父类的原型对象（这里是 `ArtistCreator.prototype`）。
4. 重新进入 `Entrepreneur` 的 `constructor` 后，我们向新创建的对象添加了另一个属性。
5. 现在，因为我们在 `Entrepreneur` 类内部，我们实际上将新创建对象的 `__proto__` 更新为 `Entrepreneur.prototype` 对象。
6. 但这样我们就失去了父类函数的功能。因此，`extends` 关键字帮助我们设置了新创建对象的 `__proto__` 的 `__proto__` 属性，指向 `ArtistCreator.prototype` 对象。（可以理解为 `this.prototype.__proto__ = ArtistCreator.prototype`）
7. 最后，我们将对象返回给全局内存，并将其存储在一个名为 `entrepreneur1` 的变量中。
8. 如果你仍然困惑，请慢慢查看图示，并再次阅读上述 7 个步骤😃。

![Image](img/Image00103.jpg)

* 所有执行完成后，你可以看到我们的最终图示😎。

![Image](img/Image00104.jpg)

* 别忘了也看看控制台中的输出。我希望我不需要解释它😅。

* 我们称之为**原型链**，因为我们实际上是在用其他对象的原型属性（主要是函数构造函数或类的原型对象）来扩展 `__proto__`。

![Image](img/Image00105.jpg)

```
我知道这背后的机制太疯狂了，但这就是你需要知道的一切。
```

在结束本章之前，我们将看看 JavaScript 本身是如何使用上述机制的。

![Image](img/Image00106.jpg)

* 如我们所见，`String` 是一个函数构造函数，它有一个原型和 `__proto__` 对象可供我们使用。原型对象本身也有 `__proto__` 属性。





* 我们在 JavaScript 中定义的每个字符串实际上都是由这个 `String` 构造函数生成的。这就是为什么你可以通过指向该原型对象（`String.prototype`）的 `__proto__` 引用来访问它的所有字符串方法。

![Image](img/Image00107.jpg)

* 每个 JavaScript 对象实际上都源自于一个 `Object`（注意大写字母 'O'）。这是我们原型链的终点（稍后会看到）。

* `Object` 本身有一个原型和可用的 `__proto__` 属性。

* 原型对象包含诸如 `hasOwnProperty()`、`toString()` 等方法，这些方法你可能在日常代码中使用过。

* 让我们看看 `String` 和 `Object` 之间是如何相互关联的。

![Image](img/Image00108.jpg)

* 如你所见，`String` 的 `__proto__` 指向全局 `Object` 的原型。另外，全局 `Object` 的 `__proto__` 对象拥有 `call()`、`bind()`、`apply()` 和其他函数，但 `Object` 的 `__proto__` 的 `__proto__` 是 `this.prototype`。而最后一个 `Object` 也是一个函数构造函数，因此它也有原型对象。这里，原型的 `__proto__` 是 `null`。主要原因是 `null`，因为我们的 `__proto__` 链在这里结束了😎。

* 让我们也看看其他类似的对象。

![Image](img/Image00109.jpg)
![Image](img/Image00110.jpg)
![Image](img/Image00111.jpg)

`Function` 是一种特殊的构造函数。它的原型和 `__proto__` 都指向 `Object.__proto__`。请看下面的示意图😁。

![Image](img/Image00112.jpg)

* 最后，将所有示意图中的原生构造函数合并在一起。（实际上还有比这些更多的构造函数，但无需在下面的图片中展示，因为我们已经理解了其中的微妙之处）。

![Image](img/Image00113.jpg)

好了，朋友们，这就是关于 `__proto__`、`prototype` 和对象链接的最完整指南😁。祝你在接下来的章节中继续愉快地学习。

***

## 异步执行

JavaScript（在没有环境的情况下）默认是单线程（一次只执行一个任务）且同步的（逐行、从上到下执行）。如果你认为这很糟糕，因为我们无法同时执行多个任务，并且在当前行执行完成之前会阻塞执行。因此，JavaScript 需要一种方法来应对这种情况。让我们看看如何实现。

### 仅靠 JavaScript 是不够的！

* 当你打板球/足球时，单靠一个最强大的球员不足以赢得整场比赛。你需要团队合作，每个球员的贡献都很重要。
* 同样，仅靠 JavaScript 是不够的，我们需要额外的“球员”，或者说一个团队。
* 这就是额外的“环境”发挥作用并帮助 JavaScript 的地方。
* 我们经常使用的两个著名的 JavaScript 环境是：
    1. 浏览器
    2. NodeJS

* 在本章中，我将只解释浏览器环境，我们将在后面的章节中理解 NodeJS 环境。
* 我们在第 1 章中看到了我们的“心智模型”，但我没有告诉你它是不完整的，因为我不想让你在那里感到困惑。现在是时候展示包含周围环境的完整“心智模型”了。
* 浏览器环境非常庞大，包括 HTML/CSS 解析器、控制台、网络监控、存储（`local`、`Indexeddb`、`web SQL` 等）、性能工具等。我们只关注异步部分如何通过所谓的“队列”和“事件循环”来处理。

### JavaScript 是同步的！（别忘了）

* 时间和资源利用在每个应用程序或现实世界中始终很重要。
* JavaScript 是同步的，这一点非常重要，以至于很多人忘记了 JavaScript 只是一种脚本语言，在早期它只是用来让网页变得动态。
* 最终，JavaScript 从未为服务器或我们今天所做的复杂渲染而构建。
* 但有些人希望在不破坏语言原始思维的前提下，让 JavaScript 更加灵活和强大。
* 2004 年，谷歌发布了 Gmap，它完全由浏览器上的 JavaScript 构建，震惊了世界，展示了 JavaScript 语言的潜力。
* 不多谈历史，让我们进入异步环境的实际实现。
* 你会看到新的 `Queues` 部分将被绘制出来，这就是我们异步之旅开始的地方😁。
* 请记住，`Queues` 是由浏览器实现的，因此有时你会看到不同浏览器产生不同的输出/结果，而不是实际期望的结果，但我们将讨论什么是正确的以及应该采用什么方法。让我们先预览一下我们新的心智模型！
* 不要试图深入理解，我们很快就会详细讲解。

![Image](img/Image00114.jpg)
当前扩展的心智模型

### 回调：被回调的函数！

* 在进一步讨论之前，有必要先谈谈回调函数。
* 回调是简单的函数，当它们被回调时（即当某个特定任务完成后）被调用。
* 有两种类型的回调：
    1. 同步回调
    2. 异步回调

#### 1) 同步回调

* 同步回调在迭代器上被调用，执行起来简单且快速（快速操作）。
* 下面是一个同步回调的例子。

![Image](img/Image00115.jpg)
同步回调

#### 2) 异步回调

* 异步回调是耗时的任务或容易出错的函数（可能完成任务，也可能根本不会完成）。
* 下面是一个异步回调的例子！
* 不要试图深入理解，只是一个例子😅。稍后会理解。

![Image](img/Image00116.jpg)
异步回调

* 当然，我们已经扩展了心智模型，但需要注意的一点是，我们扩展的心智模型不仅仅是 JavaScript。它是 JavaScript + 浏览器 API（那些队列函数是浏览器环境的一部分，例如 `setTimeout`、`setInterval` 等）。
* 但这里有一个转折点，promise 比这更复杂，它们既是 JavaScript 的一部分，也是浏览器的一部分。我们将在心智模型中看到这一点。
* 目前，让我们先看一个带有队列的简化版心智模型。

![Image](img/Image00117.jpg)
带队列的心智模型

`Queue`：一种简单的数据结构，遵循先进先出规则（即谁先来谁先走）。就像电影票购买队伍一样。

#### 任务队列

* 首先，奇怪的是，任务队列实际上并不是一个队列，而是一个 `set`（在 C++ 世界中是结构体）。
* 添加到任务队列中的任务会被取出并移除，而不是像队列那样出队。为了简单起见，我们将其视为普通队列（大多数 JavaScript 开发者都这样做，我们也会这样做）😁。
* `宏任务` 是任务队列有时使用的术语。

#### 作业队列

* 作业队列是一个真正的队列，任务在其中入队和出队。它是一个真正的队列。
* `微任务` 是作业队列有时使用的术语，但在 ES6+ 规范中它被称为作业队列。

### 是时候通过一个例子来理解了！

![Image](img/Image00118.jpg)

* 有一个 `sleep` 函数，我模拟了它在给定秒数内阻塞函数。让我们看看它的心智模型，它将如何执行！
* `setTimeout` 是一个浏览器特性，不是常规 JavaScript 的一部分。等待给定的时间，然后将回调函数放回任务队列是由浏览器完成的。

![Image](img/Image00119.jpg)

* 现在让我们看看当我们执行完 `sleep` 函数并尝试进一步执行时会发生什么。

![Image](img/Image00120.jpg)

* 另外，请注意我们定义了 `delayedTimer` 函数，但从未调用它。因此，它仍然不在调用栈中，并且它作为参数传递给了 `setTimeout`。

![Image](img/Image00121.jpg)
![Image](img/Image00122.jpg)
![Image](img/Image00123.jpg)

* 根据上面的图片，我们可以看到调用栈的所有执行（包括全局表达式和语句代码）都已完成。





简而言之，JavaScript 会直接执行所有同步代码，而所有异步操作只是被推迟到后续执行。然而，所有函数引用仍然存储在全局内存空间中，它们不会被复制到任务/作业队列中。

### 事件循环简介

```
The event loop is a simple while loop, which keeps tracks that where any work is pending in queue/s to be finished or not with continuously checking that whether callstack is ready for taking the work from the queue/s or not.
```

![Image](img/Image00124.jpg)

* 现在，由于当前我们的 `callstack` 为空，而队列中有待完成的任务，事件循环会找到它。请注意，`delayedTimer` 实际上是在 2000 毫秒后（我们提供了时间，即它实际成为任务队列一部分所需的时间）才被放入 `task queue` 的。
* 事件循环的任务只是检查队列中是否有待处理的工作，以及这些任务是什么。
* 函数 `delayedTimer` 会被环境推送到 `callstack` 中，并成为正常执行的一部分😀。

![Image](img/Image00125.jpg)
![Image](img/Image00126.jpg)
![Image](img/Image00127.jpg)
![Image](img/Image00128.jpg)

各位朋友，这就是 JavaScript 中异步代码的执行方式。还有更多内容有待探索：Promise 和 Async Await。

在本章中，我只会解释 Promise，因为 async-await 需要更多知识，我们将在后续章节中讨论。

### Promise——一种优雅的异步任务解析器

**MDN**

```
The Promise object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
```

* 当然，这是一个简短而简单的定义，但并没有解释底层到底发生了什么🤨！
* 让我用一个直观的例子更简单地为你解释 Promise。
* 在上面的例子中，我创建了一个简单的 `sleep` 函数，用于模拟给定秒数的同步阻塞机制。我们将在下一个例子中继续使用它。
* 我们有两种不同的东西：`Promise` 函数构造函数（注意大写字母）和 `promise object`（Promise 对象）。
* `Promise` 是一个函数构造函数，当我们在 `Promise` 构造函数前使用 `new` 关键字时，它会创建一个 `promise object`。
* 让我们从一个例子开始。

![Image](img/Image00129.jpg)

* 现在，在上面的代码中，如你所见，我们将 `Promise` 函数构造函数返回的对象存储在 `promiseObj` 变量中。
* 请注意，这里我们根据 `num > 5` 是否成立，有条件地调用了 `resolve` 和 `reject`。
* 可视化时间到了😄。

![Image](img/Image00130.jpg)
![Image](img/Image00131.jpg)
![Image](img/Image00132.jpg)

让我们再看一遍代码，以免在脑海中丢失它的踪迹。

![Image](img/Image00133.jpg)

* 如我们所见，`Promise` 函数构造函数用于创建 Promise 对象。但在可视化所有内容之前，让我告诉你执行 `Promise` 函数构造函数后我们会得到什么。
* 让我们看看 `promise object` 为我们提供了哪些属性和内部属性。

![Image](img/Image00134.jpg)

* 根据图示，我们可以看到 Promise 对象有三个主要的键值对（实际上是内部隐藏属性）。
* 另外，请记住我们在原始 `Promise` 函数构造函数的第一个参数中传入了 `resolved` 和 `reject`。
* 返回的 `promiseObj` 有三个重要的键值对（隐藏/内部）。

#### onFullfillment
它是一个数组，用作所有 `.then` 调用函数参数的占位符。所有 `then` 方法按顺序被推入这个数组中（稍后会可视化如何操作😄）。

#### onRejection
它是一个数组，用作 `.catch` 调用函数参数的占位符。`catch` 方法被推入这个数组中（稍后会可视化如何操作😄）。

#### value
* 它是一个值持有者，将保存 resolved 值或 rejected 值。
* `resolve` 和 `reject` 函数的重要性在于将值映射到返回对象的 `value` 键上（我们将进行可视化）。

让我们看看下面的代码片段是如何工作的，以及它的（`promiseObj` 的）值是如何被读取的。

![Image](img/Image00135.jpg)

* `Promise`（它是一个函数）构造函数的求值实际上是一个同步任务。

![Image](img/Image00136.jpg)
![Image](img/Image00137.jpg)
![Image](img/Image00138.jpg)
![Image](img/Image00139.jpg)

* 我们将看到 `new` 关键字在底层是如何工作的，但这里让我快速告诉你：`new` 关键字创建一个对象，而函数构造函数决定了该对象内部有哪些属性。
* 让我们继续可视化😊。

![Image](img/Image00140.jpg)
![Image](img/Image00141.jpg)

```
现在我们有两种可能性。
```

* 如果 `num > 5`，我们将调用 `resolve`，并将 `num` 作为参数传递给 `resolve`。

![Image](img/Image00142.jpg)

* 如果 `num < 5`，我们将调用 `reject`，并将 `num` 作为参数传递给 `reject`。

![Image](img/Image00143.jpg)

在这两种情况下，如你所见，它都会被存储在 Promise 对象的 `value` 属性中。

* 现在，我们可以看到 `promiseObj`（返回对象的标签）实际上在当前作用域中可用，并且无论 Promise 处于什么状态（resolved 或 rejected），它都会被存储在 `promiseObj` 的内部属性中，同时 `value` 将作为 resolved/rejected 值的占位符。但是，要访问 resolved 值或 rejected 值，我们需要某种机制。
* 这就是为什么我们有 `then` 和 `catch` 方法可用。这两个方法通过 `__proto__` 提供给我们（将在后续章节中详细了解原型和链）。
* 这里我们还缺少一部分：`onFullfillment` 和 `onRejection` 是数组，它们实际上是如何工作的呢🤨！
* 在这里，在 Promise 对象内部的值求值完成后，`Promise` 函数构造函数的工作就结束了（对于 resolve 和 reject 两种情况都是如此）。
* 让我们先可视化这一部分。

![Image](img/Image00144.jpg)
![Image](img/Image00145.jpg)
![Image](img/Image00146.jpg)
![Image](img/Image00147.jpg)

哇，内容真多。但我们还需要弄清楚 `then` 和 `catch` 方法😅！

* 有一件事我没有告诉你：每当我们编写 `then` 或 `catch` 方法时（在常规全局上下文中），这些方法实际上是在 `promiseObj` 创建时通过引用 `promiseObj` 的 `onFullfillment` 或 `onRejection` 键而变得可用的。
* 不仅如此，每当我们求值 value 时，该值将可用于 `then` 函数的参数（作为参数的函数）或 `catch` 函数的参数。
* 让我们看看这两种情况！

```
Resolve 函数场景
```

![Image](img/Image00148.jpg)

* 这里有一个错觉，那就是 `then` 方法😯！所以，看起来像是在返回的 `promiseObj` 上执行的代码实际上并不是由 `then` 方法运行的。它只是一个函数，充当另一个函数的占位符。因此，无论我们作为参数传递给 `then` 方法（这里是 `(val) => { console.log(val) }`）的函数是什么，都会被推送到 `promiseObj` 的 `onFullfillment` 数组中。另外，我之前没有展示这一点，因为我不想与其他可视化混淆。`then` 方法实际上是通过 `promiseObj` 的 `__proto__` 访问的。让我们可视化它😎。

![Image](img/Image00149.jpg)

* 请记住，当所有同步代码执行完毕后，`callstack` 变为空。
* `then` 参数的函数将被添加到 `onFullfillment` 中，当它执行完毕后，会被添加到 `job queue`（作业队列）中，然后从 `job queue` 进入 `callstack`。

![Image](img/Image00150.jpg)

* 这里的函数没有名称（匿名函数😅）





![Image](img/Image00151.jpg)
![Image](img/Image00152.jpg)
![Image](img/Image00153.jpg)
![Image](img/Image00154.jpg)
![Image](img/Image00155.jpg)
![Image](img/Image00156.jpg)

* 对于那个小小的 `promiseObj` 来说，这实在太多了😅，但这就是底层发生的事情。
* 别忘了我们的第二个场景，它与上面几乎一样，但它将使用 `promiseObj` 的 `onRejection` 数组！
* 让我们将其可视化😃。

```
Reject function scenario
```

![Image](img/Image00157.jpg)

让我们逐步查看它的执行过程。

![Image](img/Image00158.jpg)
![Image](img/Image00159.jpg)
![Image](img/Image00160.jpg)
![Image](img/Image00161.jpg)
![Image](img/Image00162.jpg)
![Image](img/Image00163.jpg)
![Image](img/Image00164.jpg)
![Image](img/Image00165.jpg)
![Image](img/Image00166.jpg)

* 就这样😅，底层发生了大量的事情。这就是 Promise 的工作方式。那么，浏览器中可用的、同样基于 Promise 的 `fetch API` 又是怎样的呢！它的工作方式与上面的示例几乎相同，但有一个小反转😁。为什么不通过一个简单的示例来探索它的可视化呢😋。

![Image](img/Image00167.jpg)

* 这里，我们有一个简单的 `console.log`，一个 2 秒的轻微阻塞，以及 `fetch API` 代码。让我们开始将其可视化。

![Image](img/Image00168.jpg)
![Image](img/Image00169.jpg)
![Image](img/Image00170.jpg)
![Image](img/Image00171.jpg)
![Image](img/Image00172.jpg)
![Image](img/Image00173.jpg)

* 我们没有其他需要运行的同步代码，因此我们将退出全局执行上下文，调用栈将变为空。

![Image](img/Image00174.jpg)
![Image](img/Image00175.jpg)

* 我认为到目前为止，一切看起来都与我们之前可视化的一样，但这里的反转来了。上面显示的心理模型仍然是不完整的😅。
* 我们有很多浏览器特性（又称浏览器 API），它们发生在常规执行上下文之外。不仅如此，这些浏览器特性实际上是通过我们的底层操作系统并使用内核实现的。但为了简明扼要，我们只需认为这些浏览器特性发生在实际的 JavaScript 执行上下文之外。
* 其中一个特性就是 `fetch API`。
* 让我们把我们的心理模型再扩展一点😅。

![Image](img/Image00176.jpg)

* 如你所见，我们在图表中添加了浏览器特性，现在你可以感觉到我们的浏览器环境不仅仅是 JavaScript，而是底层结合了许多隐藏特性的总和。

![Image](img/Image00177.jpg)

* 这里，让我们看看在执行代码时，运行到 `fetch('https://test.com')` 这一行会发生什么。
* 我们再次回到当我们实际返回 `dataPromiseObject` 时会发生什么。

![Image](img/Image00178.jpg)

* 我们可以看到，`fetch` 实际上建立了两种绑定：一种在 JavaScript 任务中，另一种是网络工作。让我继续可视化☺。

![Image](img/Image00179.jpg)

* 在代码中执行到 `fetch` 行后，从 `fetch API` 返回 Promise 对象的工作会立即完成，但完成 API 调用的后台任务仍在挂起，这由浏览器完成，并在完成后交给 Promise 对象。
* 在完成后台工作后，所有其他工作与我们之前可视化的一样 😁。

![Image](img/Image00180.jpg)
![Image](img/Image00181.jpg)
![Image](img/Image00182.jpg)
![Image](img/Image00183.jpg)
![Image](img/Image00184.jpg)
![Image](img/Image00185.jpg)
![Image](img/Image00186.jpg)

```
这就是全部了，朋友们，这就是 Promise 和 fetch API 在底层真正的工作方式😊。
```

***

## 5 迭代器、生成器和 Async-Await

```
本章将深入解释迭代器（iterator）和生成器（generators）及其重要性。此外，还将介绍这些内容在实际场景中如何被利用，以使代码看起来更美观且易于阅读。不仅如此，本章还将包含非常高密度的可视化内容。
```

### 循环 (Loops)

* 在进入迭代器之前，我们先谈谈传统的循环。
* 我们使用循环来遍历 `iterable` 的每个元素并执行操作。让我们来看一个简单的例子。

![Image](img/Image00187.jpg)

* 在上面的示例中，我们有一个简单的 `numberArray`，我们正在遍历元素并简单地将其乘以 2。
* 请注意，我们是在**一次性**地执行操作。我们无法控制这种一次性操作（你可以加入 if-else 等内容来控制流程，但这并不是对元素的真正控制！）。
* 如果我们能一次获取一个元素并对其执行某些操作会怎样？这样每当我们需要下一个元素时，只需产生它即可。初听起来可能有点奇怪，但让我通过构建一个自定义迭代器来举例。
* 为了简单起见，我将使用心理模型的简化图，当我们结合所有概念时，会制作一个完整的心理模型图😄。对于下面的示例，我将仅显示执行线程和内存。

### 迭代器 (Iterators)

![Image](img/Image00188.jpg)

我们声明了一个名为 `createFlowOfElements` 的函数，它实际上是一个接收数组作为参数并返回 `innerObj` 的函数。让我们执行这个函数。

![Image](img/Image00189.jpg)

现在是时候可视化执行 `createFlowOfElements` 时发生了什么。

![Image](img/Image00190.jpg)

* **如果你还没猜到的话，** 这里我们有一个函数嵌套在函数内部（即使它定义在 `innerObj` 内部）。因此，如果我们返回 `innerObj` 或 `innerObj` 的函数，我们将拥有一个外部作用域的背包（朋友们，这就是闭包😁）。
* `createFlowOfElements` 是一个实际上将要创建迭代器的函数！让我们将其可视化。

![Image](img/Image00191.jpg)
![Image](img/Image00192.jpg)
![Image](img/Image00193.jpg)

* 太棒了，我们可以看到 `returnNextElement` 具有闭包，不仅如此，对象内部还有一个 `next` 方法（人们通常将对象的函数称为方法😅）。此外，我没有显示全局作用域的两个变量 `element1` 和 `element2`，因为在上面的图表中不需要对这些变量进行真实可视化。

![Image](img/Image00194.jpg)

* 现在，是时候看看执行 `returnNextElement` 的 `next` 方法时会发生什么。

![Image](img/Image00195.jpg)
![Image](img/Image00196.jpg)

* 因为函数本地内存中没有变量，所以我们在闭包中查找这些变量，并且在这里找到了它们。

![Image](img/Image00197.jpg)
![Image](img/Image00198.jpg)

* 现在，对于 `element2` 发生的事情完全一样，所以我不再为此绘制图表了😅。这是所有执行完成后最终的图表。

![Image](img/Image00199.jpg)

* 太好了，我们刚刚创建了第一个自定义迭代器，也就是说，我们现在拥有了一种控制数据流的机制，而不是一次性完成所有事情。因此，我们不再是将所有元素直接扔进管道，而是拥有一个可以用来获取元素的开关。我们正在控制我们的元素流😎。
* 这就是为什么迭代器很重要，因为我们可以获得控制权。这是一个强大的机制，将有助于从零开始构建一些 ES7+ 特性（很快就会看到）。
* 此外，你可以想象事件循环是通过迭代器维护的，我们实际上是在一个接一个地迭代队列中的方法，并使它们在调用栈中可用😁。

### 生成器 (Generators)

`generator` 简单来说就是一个返回迭代器的函数！在上面的示例中，`createFlowOfElements` 实际上就是一个返回迭代器的生成器函数😮！

ES7+ 拥有原生的生成器函数。让我们看看 JavaScript 原生生成器的一个简单示例。

![Image](img/Image00200.jpg)

* 从上面的示例可以看出，原生生成器看起来非常简单且易于编写。但原生生成器与我们自定义生成器的工作方式有一个小反转。
* 第一个主要区别是，原生生成器是一种特殊的函数（你在函数定义中看到了 `*`）。原生生成器函数依赖于隐藏/内部属性（记住函数也是对象 😅）。





* 第二点区别是，生成器函数（generator function）不会被放入调用栈（callstack），而是存储在内存中并直接放入执行线程😮！
* `yield` 是一种特殊的关键字，它在幕后执行了很多隐藏操作。此外，它与 `return` 关键字完全不同。

### return

* `return` 关键字会立即停止函数执行，并允许你从函数中返回任何值。
* `return` 关键字主要用于执行某些操作，并将操作结果返回给外部作用域。

### yield

* 这是一种特殊的关键字，用于生成器函数内部。
* `yield` 关键字不会停止生成器函数的执行，而是会**挂起**执行（暂停执行）🤨。这样，我们稍后可以使用同一个挂起的执行上下文。
* 现在，当我们挂起函数执行时，我们需要某种机制来跟踪执行具体在何处被挂起。这样在下一次迭代中，我们能够从挂起（暂停）的地方重新开始执行。
* 在生成器函数返回的迭代器上，有一个名为 `[[GeneratorLocation]]` 的隐藏/内部属性。
* `yield` 关键字会挂起执行，并将函数执行被挂起的位置存储在 `[[GeneratorLocation]]` 中。

![Image](img/Image00201.jpg)

* `[[GeneratorLocation]]` 处于 `VM36: 3` 的原因是，你可以看到我们调用了 2 次 `returnNextElement.next()`。因此，有两个值被 yield 出来了，函数经历了暂停和继续。所以在下一次迭代中，我们将从第 3 行（准确说是 yield 值的第 3 个位置）开始执行。
* 如果你点击 `VM36:3`（`VM36` 是由浏览器控制台随机生成的），我们将能够看到函数最后一次挂起的位置。

![Image](img/Image00202.jpg)

现在，如果生成器函数内部有其他内容会怎样？比如 `console.log()` 或任何其他操作！

![Image](img/Image00203.jpg)

* 如你所见，它的工作方式与之前完全一样，但现在 `[[GeneratorLocation]]` 是相对于我们的函数定义的。这意味着它实际上在跟踪函数暂停的行号！
* 现在如果我们点击那个 `VM107:4`，我们可以在下方看到它暂停的位置。同样，因为我们使用了 2 次 `returnNextElement.next()`，所以我们在第二个 yield 值之后暂停了。

![Image](img/Image00204.jpg)

* 我们还没有看到 `element1` 和 `element2` 变量中实际包含什么😅。让我们来看看。

![Image](img/Image00205.jpg)

* 与我们之前直接返回值的自定义生成器不同，这里我们返回的是一个包含若干键值对的对象。
* 我们有 `value` 属性本身和 `done` 属性。
* `value` 保存的是被 yield 出来的任何内容，而 `done` 告诉我们暂停执行的函数是否还有剩余的执行内容！
* 但是，等等，这里没有闭包，那么这个对象到底是从哪里检索到的！让我们看看。

![Image](img/Image00206.jpg)

* 如你所见，我们将 yield 的值存储在名为 `[[scopes]]` 的隐藏属性中。
* 现在，如果我们再运行一次 `returnNextElement.next()` 并查看结果会怎样。

![Image](img/Image00207.jpg)

* 现在，如果我们再次运行一次 `returnNextElement.next()` 并查看结果会怎样。

![Image](img/Image00208.jpg)

* 如你所见，当我们完成所有值的 yield 之后，我们关闭（结束）了函数执行，并且 `done` 属性变成了 `true`。
* 简而言之，生成器允许我们创建自定义迭代器，并且我们可以对可迭代对象使用 `next()` 方法来检索 yield 的值。
* 为了全面了解生成器和迭代器，我们还需要探索一件事。请看下面的示例。

![Image](img/Image00209.jpg)

常见的想法是，我们在第一次调用 `next()` 时会 yield `4`，在第二次调用 `next()` 时，`newNum` 变量将为 `4`。因此，第二次 `next()` 调用应该让我们得到 `9` (`5 + 4 == 9`)。不幸的是，它的工作方式并非如此😅。

让我们看看输出结果。

![Image](img/Image00210.jpg)

* 如你所见，第二次调用 `next()` 的输出与我们的预期完全不同。之所以发生这种情况，是因为生成器函数返回的迭代器允许你向 `next()` 函数传递一个参数，而我们传递给 `next()` 函数参数的任何内容，都将传递到函数挂起执行的地方！
* 因此，最终我们传递给第二次 `next()` 调用的参数 `13` 被传递并存储在 `newNum` 中。所以在下一次 yield 中，它变成了 `18` (`5 + 13`)😄。

如果我们不为第二次 `next()` 调用提供或传递任何参数会怎样 🤔？

![Image](img/Image00211.jpg)

* 如你所见，如果我们不提供任何参数，那么 `newNum` 的值将是 `undefined`。
* 因此，当我们第二次 yield 值时，它变成了 `NaN` (`5 + undefined`)。
* 上面的示例有一个非常棒的用例，这就是我们接下来要做的。
* 让我们从零开始构建 `async-await` 😎。

![Image](img/Image00212.jpg)

* 这一次我们将把上面的代码可视化😅😅。让我提前告诉你，我们即将绘制的图表将是最复杂且最艰巨的。它将涉及到我们目前为止理解的几乎每一个概念😮。那么，让我们开始吧。

![Image](img/Image00213.jpg)

在进一步深入之前，让我告诉你我们将使用的一些颜色方案。
**深紫色** - 正在执行的生成器函数
**浅紫色** - 处于挂起状态（暂停）的生成器函数。

![Image](img/Image00214.jpg)

* 还有一点，生成器函数不是普通函数，它们不会被垃圾回收（即使在执行结束后，它们仍保留在内存中）。
* 此外，函数的执行被直接放入执行线程中。

![Image](img/Image00215.jpg)

* 关于那个 `__proto__`，其实很简单。生成器函数对象是由 `Generator` 对象构建的。因此，生成器函数对象的 `__proto__` 指向 `Generator` 的原型对象 (`generator.__proto__ = Generator.prototype`)。同样地，`returnNextElement` 是由生成器函数构建的。因此，`returnNextElement` 对象的 `__proto__` 指向生成器函数的原型对象 (`returnNextElement.__proto__ = generator.prototype`)。
* 最终，我们的 `returnNextElement` 将通过 `__proto__` 链访问 `next()` 方法。

![Image](img/Image00216.jpg)
![Image](img/Image00217.jpg)

* 在完成 `returnNextElement` 迭代器的创建后，当我们使用 `next()` 方法时，我们将进入 `fetch()` API 部分。让我们看看它是如何运行的。

![Image](img/Image00218.jpg)

* 查看下方图表，生成器函数被直接放入执行中，不仅如此，我们的 `fetch` API 还创建了双向绑定（后台网络工作 + JavaScript 执行线程中的 promise 对象创建）。
* 尝试回忆前一章中 `fetch` API 的心理模型，一切都会顺畅地衔接起来。

![Image](img/Image00219.jpg)
![Image](img/Image00220.jpg)

* 正如我们所知，当我们完成网络任务时，结果将返回给 promise 对象的 `value` 属性，接下来的心理模型与我们在前一章中学到的 promise 对象完全相同。
* 只需跟随图表，你就能理解😊。

![Image](img/Image00221.jpg)
![Image](img/Image00222.jpg)
![Image](img/Image00223.jpg)
![Image](img/Image00224.jpg)
![Image](img/Image00225.jpg)

* 在完成 promise 对象的工作后，我们现在再次调用 `returnNextElement` 的 `next()` 方法，并向 `next()` 方法提供 `data` 参数。请看我们的示例代码。

![Image](img/Image00226.jpg)





*   让我们看看它在进一步执行中的表现。

![Image](img/Image00227.jpg)

*   因为我们使用从 Promise 对象的 `value` 中获取的 `data` 调用了 `next()` 方法，所以我们将该值提供给 `next()` 迭代器的局部变量。

![Image](img/Image00228.jpg)

![Image](img/Image00229.jpg)

![Image](img/Image00230.jpg)

![Image](img/Image00231.jpg)

```
There you have it, my friends. we have made our own custom async-await from scratch😎.(you can do the same with a catch scenario as well, which I am not going to show😅)
```

在结束本章之前，让我们通过示例看一下 async-await 的简化 ES7+ 语法。

![Image](img/Image00232.jpg)

*   如你所见，`async` 关键字的行为类似于生成器，而 `await` 关键字的行为类似于我们示例中的 `yield` 关键字。也就是说，这就是本章的底层原理和深入探讨😊。

* * *

# 6

# NodeJS、C++、队列与服务器

```
If someone would ask me, what is the best thing that happens in the javascript community?, my immediate answer will be it is none other than NodeJS!.NodeJS is an amazing javascript runtime and also a little misunderstood tool. In this chapter, I will try to make it as easy as possible and explain the core architecture and fundamentals of the nodejs.
```

### Node 不是什么？

1.  它不是一种编程语言。
2.  它不是用于服务器端编码的框架/工具（不像 Php）。
3.  JavaScript 是一种编程语言，**而 Node 不是**。

### Node 实际上是什么？

1.  它是一个底层 C++ 委托代码，通过提供 JavaScript API（即 C++ 特性的 JavaScript 版本（**有时甚至是“C 绑定的 C++ 代码”**））供我们使用。
2.  **它实际上是一个 C++ 程序**，将 JavaScript 代码作为字符串接收并完成所有工作！
3.  Node 是一个单一的 C++ 程序，依赖于许多其他 C++ 库，如 **libUV、V8、c-ares、OpenSSL** 等。
4.  我们称之为 nodejs，是因为用 C++ 编写的特性通过暴露等效的 JavaScript API 供我们使用。所以，Node（C++ 特性）+ JavaScript == NodeJS😎。

```
NodeJS's core architecture is way more complicated than a browser or any other environment. Not only that, on the internet 90% of information related to nodejs are partially false or misguided😪.
```

*   我将非常循序渐进地讲解核心架构，并为你拆分各个部分，这样你就不需要再去其他地方理解了。让我们从 JavaScript 的基本示意图开始。

![Image](img/Image00233.jpg)

*   如我们所见，我们有一个类似的模型：队列、调用栈和我们的内存空间。
*   因为我们要在计算机上执行大量系统操作，Node 实际上使用了大量第三方 C/C++ 库来完成各种任务。
*   我们首先需要理解两个主要组件。

### V8 引擎

*   V8 引擎有一个基本任务：解析 JavaScript 并将其转换为**优化的机器码**。
*   然而，V8 不仅仅是将我们的 JavaScript 代码转换为机器码，它做的远不止这些。它提供了事件循环的默认版本（等等，什么🤨）。
*   V8 提供给我们的默认事件循环可以被 JavaScript 运行时创建者扩展或替换。
*   Node 实际上并没有使用 V8 的默认事件循环。Node 使用的是 LibUV 的事件循环，而不是 V8 的！
*   因为 V8 有一个默认的事件循环，V8 事件循环队列的骨架代码仍然存在，并且 **Promise** 使用该队列，而不是其他任何队列。
*   我已经移除了 V8 的 **“任务队列”**。主要原因是 Node 不使用它，甚至不关心它。Node 使用了一种稍微不同的方法来处理异步**定时器**。
*   Node 提供了 `process.nextTick()`，它被设计为始终在所有队列之前运行。

![Image](img/Image00234.jpg)

### LibUV

*   这个库是 Node 的核心。LibUV 不仅提供了事件循环，还拥有一个非常好的机制来处理大量 I/O 操作。
*   I/O 操作可以是任何东西，比如大量连接请求、套接字、文件系统等。
*   LibUV 提供或有时使用许多队列，我们很快就会学习这些队列。
*   让我们先看看结合了 **v8 和 libUV** 的心智模型图😄。

![Image](img/Image00235.jpg)

*   我故意在蓝色框上方留了一些空间，稍后会讲到。
*   从图中可以看到，我们有 v8 + LibUV 的队列。
*   LibUV 有 7 个主要队列（只画了 6 个，因为 Idle 和 Prepare 合并为一行）。

1.  **定时器：** `setTimeout()` 和 `setInterval()`。
2.  **待处理回调：** 想象一下，父进程是 **Nginx 服务器**，它已经在 3000 端口上运行，而你想在 3000 端口上启动 Node 服务器。那么，它会抛出一个错误（系统错误）。所有这类系统调用或错误回调都会被放入这个队列。
3.  **Idle 和 Prepare：** 我们不与之交互。😅（两个队列画在一起，因为我们实际上不使用，LibUV 内部使用它们）
4.  **Poll：** 所有 I/O 操作，如文件处理、客户端请求处理、套接字、加密、zlib（压缩）操作等，都通过此队列处理。
5.  **Check：** 用于 `setImmediate()` 回调，我们使用这个队列。
6.  **Close：** 所有来自系统的关闭事件，如套接字关闭或清理事件，都被添加到此队列中（但为什么呢？因为这些是系统调用，而不是传入请求，所以😁）。

> 默认的 libUV 和 v8 结合的心智模型并不难理解。问题是 Node 内部做的事情远不止使用这些队列，而最重要的部分是 **poll 队列** ***😋*** **。**

*   从图中，我们可以看到一些奇怪的东西，比如**线程池**和 **Epoll/KQueue（数据结构）**，它们用于处理从 poll 队列委托过来的工作。
*   不仅如此，我们还有**工作线程**，这也是一个不同的东西🤨。
*   在底部，我们有操作系统特性，或者你可以称之为系统的心脏 **“内核”**。
*   在我们进一步解释所有东西如何协同工作之前，让我们先完成 Node 架构。

![Image](img/Image00236.jpg)

*   我们知道我们将编写“JavaScript”，因此任何系统级代码都需要用 JavaScript 编写，然后委托给我们的 C++ 代码。这就是为什么我们有 **Node Core APIs**。
*   它包含了所有核心模块的逻辑，这些逻辑用 C++ 编写，并暴露为 JavaScript API，供我们作为开发者使用。
*   **C++ Addon 和 N-API** 是我们可以使用的特殊特性或 API，用于通过 C++ 扩展 NodeJS（这需要 C/C++ 知识，所以我不会告诉你这个😅）。

### Node 内部的正常执行流程

**步骤 1：** 扫描整个代码，提升所有可能的变量。对未使用的引用进行垃圾回收（优化）。

**步骤 2：** 从上到下完成所有同步执行。

**步骤 3：** 扫描所有异步代码的事件处理程序或回调，并将其作为未来的占位符存储在内存中。

**步骤 4：** 开始通过队列执行所有已完成的后台代码，并持续进行，直到完成所有后台任务或终止进程（事件循环😁！）

Node 环境中队列的顺序如图所示。

1.  执行所有 `process.nextTick()` 的回调。
2.  执行 **job queue** 中的所有 Promise。
3.  进入 LibUV 的队列，并从右向左开始执行
    3.1 通过 **Timer queue** 完成定时器。
    3.2 通过 **Pending queue** 完成系统调用的错误处理回调。
    3.3 完成内部使用的 **Idle、Prepare queue**。
    3.4 等待一段时间，尝试尽可能多地完成 **poll queue** 中的回调。（稍微复杂，我们稍后会深入理解）。
    3.5 完成 **check queue**（`setImmediate`）。
    3.6 通过 **close queue** 完成关闭回调的执行。





### 步骤 5：重复循环直到 Node 进程被终止

现在，我们通过一个示例来理解所有内容，并深入了解每一步发生了什么。

![Image](img/Image00237.jpg)

> 暂时忽略 `require()` 以及模块系统的工作原理，只关注我们的示例。另外，我特意编写了一段 JavaScript 代码，使其执行结果与代码逻辑上显示的结果完全不同，产生意想不到的输出。

![Image](img/Image00238.jpg)

*   一开始，我们读取文本文件的内容，即 `file1.txt` 和 `file2.txt`。
*   `file1.txt` 的内容是“Hello guys 1”，`file2.txt` 的内容是“Hello guys 2”。

![Image](img/Image00239.jpg)

*   下一条语句是非常简单的同步日志输出。

![Image](img/Image00240.jpg)

*   接下来，我们使用了如上所示的 `process.nextTick()`。

![Image](img/Image00241.jpg)

*   之后，我们调用了如上所示的 `setImmediate()`。

![Image](img/Image00242.jpg)

*   然后，我们发起两次 HTTP GET API 调用，并简单地从响应中记录 `statusMessage`。

![Image](img/Image00243.jpg)

*   接着，我们解析了一个 `Promise`，并调用了该已解析 Promise 的 `then()`。

![Image](img/Image00244.jpg)

*   最后，在我们的代码中，我们调用了 `setTimeout()`，其超时时间为 0 毫秒。

现在，让我们开始可视化代码的执行过程，看看代码在底层是如何实际工作的😎！

![Image](img/Image00245.jpg)

*   首先，我们将完成所有同步代码，在本例中包括 `console` 语句和 `Promise` 函数构造函数（注意，这里不是已完成的 Promise 对象，只是 `Promise` 构造函数的执行）。

![Image](img/Image00246.jpg)
![Image](img/Image00247.jpg)

*   这里我们返回了一个 Promise 对象，但没有将其存储在任何变量中，因此 `then()` 的回调会立即被放入 Job Queue（任务队列），而该对象由于在内存中没有任何引用而被垃圾回收。下面我们来看一下！

![Image](img/Image00248.jpg)

*   Promise 的工作方式在浏览器或 Node 环境中不会改变，因为两者都使用 V8 引擎，而 Promise 是 V8 引擎本身的一部分。

![Image](img/Image00249.jpg)
![Image](img/Image00250.jpg)

*   如你所见，`then()` 的回调被添加到 Job Queue 中，而 Promise 对象则被垃圾回收。接下来我们继续执行。
*   由于 Node 提供了 `process.nextTick()`，在同步执行完成后，所有 `process.nextTick()` 的回调会被添加到一个单独的队列中，如图所示。
*   因此，`process.nextTick()` 的回调被存储在我们队列层级中最顶层的队列中。

![Image](img/Image00251.jpg)

*   我们继续遍历代码，并将回调存储到 Node 环境决定的各自队列中。上面，我们将一个定时器回调添加到了定时器队列中。

![Image](img/Image00252.jpg)

*   如上所示，所有 I/O 回调都在 Poll 队列中。文件读取操作和 HTTP GET API 调用都属于 I/O 操作。
*   在内部，Poll 队列根据执行的操作采用不同的处理方式（稍后会看到）。

![Image](img/Image00253.jpg)

*   最后，我们还有 `setImmediate()`，它将进入 Check 队列。
*   Poll 队列实际上会启动后台工作，并且不参与队列调用的第一次迭代（事件循环的第一次迭代）。因此，我将其标记为灰色。

![Image](img/Image00254.jpg)

*   现在，让我们开始执行队列。记住队列的顺序：从上到下，从右到左。

![Image](img/Image00255.jpg)
![Image](img/Image00256.jpg)

接下来轮到我们的 Job Queue（Promise 队列）。

![Image](img/Image00257.jpg)
![Image](img/Image00258.jpg)
![Image](img/Image00259.jpg)
![Image](img/Image00260.jpg)

*   现在轮到我们的定时器了😃。

![Image](img/Image00261.jpg)
![Image](img/Image00262.jpg)
![Image](img/Image00263.jpg)

*   这次轮到 Poll 队列了，但 Poll 队列中有 4 个操作：2 个文件读取和 2 个 GET API 调用。因此，`libUV` 会在内部计算超时时间，判断这些操作是否能在一定时间内（通常是很短的几秒内）快速完成。如果不能，则立即转到 Check 队列。这就是为什么我们在这里会快速转到 Check 队列中的 `setImmediate()` 回调，而不等待这 4 个操作（2 个文件读取 + 2 个 GET API 调用）完成。

![Image](img/Image00264.jpg)
![Image](img/Image00265.jpg)

*   现在，所有队列都已清空，除了 Poll 队列外，所有待处理任务都已结束。让我们看看 Poll 队列将如何执行这些任务。
*   Poll 队列将任务分为两大类。
*   所有类似文件读取、crypto 和 zLib 的操作都通过线程池完成。
*   线程池是一组工作线程（与 Node 默认模块提供的工作线程不同）。线程池的默认大小为 4，但你可以通过 Node 提供的 `UV_THREADPOOL_SIZE` 全局变量覆盖该值。我在线程池中画了 4 个小方块来表示线程。
*   一个线程可以执行一个任务，因此 4 个线程可以同时执行 4 个任务。
*   然而，正如我所说，文件读取、crypto 和 zLib 这类任务在设计上只在线程池中执行。因此，在我们的例子中，两个文件读取操作通过线程池完成，两个文件操作由两个独立的线程处理，而另外两个 GET API 调用则通过其他机制（如 `Epoll`/`Kqueue`）完成（稍后会看到）。

![Image](img/Image00266.jpg)

*   如你所见，我们在两个线程中处理两个文件读取操作，当它们完成读取后，结果会返回给各自的回调。

![Image](img/Image00267.jpg)
![Image](img/Image00268.jpg)

*   让我们完成这两个已完成的读取操作的执行，并运行它们的回调（因为我们不会在等待 API 调用完成时阻塞 Poll 队列）。

![Image](img/Image00269.jpg)
![Image](img/Image00270.jpg)

*   很好，现在我们也完成了文件读取操作，但还有两个操作需要完成，即我们的两个 API 调用。因此，我们再次进入事件循环的下一次迭代。

![Image](img/Image00271.jpg)

*   现在，是时候了解 `epoll`/`Kqueue` 和 Poll 队列如何协同工作了。我将解释 `epoll`，而不是其他机制，因为所有其他机制几乎相同，唯一的区别在于它们基于不同的操作系统架构。

#### epoll（假设我们在 Linux 上）

*   它是一种自平衡的二叉树数据结构。
*   我们将任务附加到该数据结构的节点上，并循环遍历每个任务，直到某个超时时间。
*   假设有 10 个 API 请求同时到达正在运行的 Node 进程，它们实际上都会被交给 `epoll`。
*   在将所有请求交给 `epoll` 之前，请求会以非阻塞模式打开（这是 Linux 的一个特性，允许以非阻塞模式打开文件/处理请求，并等待它们完成，然后返回结果）。
*   现在，在我们的假设中，我们有 10 个并发请求，我们将以非阻塞模式打开它们，并将其 ID（称为文件描述符）存储在 `epoll` 中。每个 ID 都会关联事件（这里指我们的回调函数）。
*   通常，我们会在一段时间内循环遍历 `epoll`。假设 `epoll` 循环 2 秒，那么在这 2 秒内，10 个请求中有 4 个完成了。因此，结果会返回给 `epoll`，再从 `epoll` 返回到我们的 Poll 队列。
*   完成 4 个请求后，我们立即转到 Check 队列。
*   在事件循环的下一次迭代中，假设在我们的 `epoll` 中又完成了 3 个请求（记住，我们实际上每 2 秒循环一次 `epoll`，以检查后台工作是否完成）。这 3 个请求及其数据会返回给 Poll 队列。
*   在下一次迭代中，假设我们完成了所有剩余的 3 个请求，结果返回给 Poll 队列。




通过内核特性将请求置于非阻塞模式，并借助 Epoll 数据结构处理任务，能够在不阻塞主 JavaScript 线程、不阻塞轮询队列以及不产生新线程的情况下，实现惊人的并发能力。这正是 Node.js 如此流行且令人惊叹的原因。

![Image](img/Image00272.jpg)

* 在我们的场景中，有两个 GET API 调用。我们将按照刚才讨论的方式通过 epoll 处理它们，并将结果返回给轮询队列。让我们完成剩余两个 API 调用的可视化展示。

![Image](img/Image00273.jpg)
![Image](img/Image00274.jpg)
![Image](img/Image00275.jpg)

现在，所有执行如上所述完成，所有队列变为空，因此程序将退出。朋友们，这就是 Node 实际工作的方式😎。你通过正确的思维模型学习了复杂的 Node 架构😁。

```
注意：这里我假设 file1.txt 的读取操作在 file2.txt 之前完成，同样第一个 API 调用在第二个 API 调用之前完成。两个文件读取操作中哪一个先完成取决于你的操作系统和处理器。API 调用也是如此。
```

现在，让我们从 Node 的角度讨论一些令人困惑的概念，比如 `多线程`、`工作线程` 和 `多进程`。

### 多进程

* 我们知道，当我们启动 Node 程序时，实际上启动了一个 Node 进程，其中包含 1 个 `v8` 实例、1 个通过 `libUV` 实现的事件循环实例以及 Node API 核心层。
* 现在，当我们使用 `child_process` 时，我们从父进程（即我们的 Node 进程）中创建一个新的独立进程。我们可以在新创建的进程中执行任何操作。
* 这里需要注意的重要一点是，每个新创建的进程都将拥有自己的 1 个 `v8` 实例和 1 个通过 `libUV` 实现的事件循环实例。这就是为什么我们也可以在 `child_process` 中解析 JavaScript（如果需要的话）。
* 如果你是 Node 开发者，那么你很可能知道名为 `Cluster` 的模块，它主要用于创建正在运行的 Node 进程的一个或多个分支，并且每个进程将被放置在你的处理器的逻辑核心上！

让我们可视化它。

![Image](img/Image00276.jpg)

### 工作线程

* 这是 Node 中一个独立的模块，允许你创建真正的线程，并且我们也可以在新创建的线程中运行 JavaScript 代码。
* 每个线程将拥有自己的 `v8` 和 `libUV` 实例。

![Image](img/Image00277.jpg)

* 工作线程可以通过通信通道与父进程的主线程通信，不仅如此，我们还可以在不同线程之间来回传递数据😋。
* Node 中的线程与其他编程语言的线程概念略有不同。正如我们所见，我们可以在单独的线程中运行 CPU 密集型任务，但每个线程都有自己的 `v8` 和 `libUV` 实例。因为每个线程需要 `v8` 和 `libUV` 来执行任务并解析 JavaScript 代码，所以 Node 中的线程会消耗更多内存。
* 因此，即使在 Node 中创建大量线程，我们也肯定会耗尽系统内存，或者使系统因资源密集型线程而过载。
* 所以，最好只在 Node 中为大型 CPU 密集型任务使用工作线程。切勿使用工作线程来服务 API 请求或提供文件服务🧐。

### 多进程 vs 工作线程

* 最好使用多进程在每个 CPU 核心上服务 Node 进程。此外，在每个 Node 进程内部，我们将拥有足够的内存和存储空间，以便可以累积多个 API 请求，随后通过轮询队列委托给 epoll 和线程池，从而为我们提供真正良好的并发能力。
* 工作线程可用于执行 CPU 密集型任务，例如在单独的线程中计算高度复杂的数学公式，并将结果返回给父线程（即我们的 Node 主进程的线程）。
* 我们可以结合两者的优点：创建多个 Node 进程，并为每个进程中的特定 CPU 密集型任务使用工作线程😎。

### 工作线程 vs 线程池

* 这很简单，线程池拥有工作线程（可以直接执行特定任务的线程），当我们执行文件 I/O、加密和 zlib 操作时，`libUV` 会自动使用这些线程。
* `工作线程`（Node 提供的模块）由我们创建，用于在完全不同的线程中执行特定任务。
* 现在，`线程池` 的线程易于维护且速度快，因为它们不需要 `v8` 和 `libUV` 实例，因为线程池已经提前知道要执行的任务。
* `工作线程` 会消耗一些资源，因此我们不会创建太多。（这里，我们不会像其他传统编程语言（如 Java）那样为每个客户端请求创建线程，因为如果那样做，会使我们的系统更加消耗资源且不稳定。这与它们的概念完全不同。对于这类目的，我们应该始终依赖 Node 的非阻塞 I/O）。

```
我希望以上所有信息已经澄清了关于 Node.js 的所有错误假设和误解😊。
```

### Node 模块系统

现在，在结束 Node 之旅之前，我想解释一下 Node 的模块系统是如何工作的。

JavaScript 在不同的环境中运行，我们默认没有可用的原生模块系统（忽略最近出现的 ES6+ 原生模块，稍后讨论）。

* 现在，当 Node.js 开发时，他们需要找出某种方式为开发者提供模块化系统，因此他们创建了自己的模块系统，称为 `commonjs`。让我们通过可视化来理解它是如何工作的。
* 在 Node.js 中，我们项目中使用的每个 JavaScript 文件都被视为一个 `模块`，这意味着它们不仅仅是文件中的普通 JavaScript 代码，而是有一些额外的包装和内容。
* 此外，Node.js 为我们提供了一些全局变量，这些变量对所有 `模块` 都可用。我们称它们为全局变量。其中两个变量是 `require()` 函数和 `module` 对象（注意，这里的文件 `module` 和全局关键字 `module` 是两个不同的东西😅）。

让我们可视化到目前为止所学的内容。

![Image](img/Image00278.jpg)

* 假设，我们想要将其他文件（`file1.js` 和 `file2.js`）的一些内容添加到我们的主文件（`main.js`）中。
* 正如我之前所说，在运行 Node 进程时，我们默认有一些全局变量可用。因此，这里我们将需要使用其中一个变量来完成我们的需求。
* `require()` 函数在每个文件（模块）中都可使用，这意味着我也可以在 `main.js` 中使用这个辅助函数。
* 但是 Node.js 会在所有模块（js 文件）被另一个模块 require 之前，给它们添加一个叫做 `IIFE`（立即调用函数表达式）的东西。让我们看看。

![Image](img/Image00279.jpg)

* 正如我们所见，在 `file1.js` 中，我们有一个简单的 `greet()` 函数，它将被 `IIFE` 函数包裹，如图所示（当然，只有当我们在另一个模块中 require `file1.js` 时才会这样）。
* 同样，我们的 `main.js`（主模块）也会被包裹。因为当我们启动 Node 进程时，我们将从主模块开始。

![Image](img/Image00280.jpg)

* 如果你注意到一点，包装器 `IIFE` 有一堆参数/变量可用，其中之一是 `require`。让我们看看当我们在主模块中使用 `require` 时会发生什么。
* `require()` 函数接受文件路径作为参数来查找另一个模块。

![Image](img/Image00281.jpg)

* 如果你尝试运行上述代码，它将抛出一个 `模块未找到` 的错误🤔。

![Image](img/Image00282.jpg)

* 但为什么呢？
* 记住我说过每个模块都被 `IIFE` 包裹，所以当我们 require 一个模块时，我们实际上获取的是 `IIFE`，而不是模块的代码😮。让我们可视化它。

![Image](img/Image00283.jpg)





### CommonJS 模块系统的工作原理

正如我们所看到的，蓝色内容实际上就是 `require()` 所做的事情。因此，它是一个包装函数，其中的所有变量和函数都是局部作用域的。这就是为什么我们无法执行 `greet()` 函数并得到错误的原因。

但那么我们是如何让它工作的呢🤨？

这就是我们传递给 IFEE 的 `arguments` 发挥作用的地方。

如果我们想要使用 `greet()` 函数，那么当我们在另一个模块中 require 它时，需要以某种方式将其从 IFEE 的作用域中取出。

Node.js 的 IFEE 通过参数为我们提供了一个 `module` 对象，并且在该 `module` 对象上有一个 `exports` 键（参见图示，IFEE 的第三个参数）。

因此，如果我使用 `module.exports` 并向其添加属性，那么当我们在另一个模块中 require 它时，它就能访问到这些属性。让我们可视化一下，因为这样更容易理解。

![Image](img/Image00284.jpg)

从图中我们可以看到，`file1.js` 的包装器返回了 `module.exports` 对象，并且我们已经将 `greet()` 函数附加到了 `module.exports` 对象上。

现在，让我们看看在 `main.js` 中 require 这个模块（`file1.js`）时发生了什么。

![Image](img/Image00285.jpg)

根据可视化，我们可以看到，如果我们提取从 IFEE 返回的任何内容，那么我们就可以通过 `module.exports` 访问 `greet` 函数，因为 `module.exports` 就是 IFEE 返回的内容。这里我们从 IFEE 返回了内容，但没有将其存储在一个变量中以便使用。

![Image](img/Image00286.jpg)

最后，我们可以看到，我们从 `module.exports` 返回的内容实际上被存储在一个名为 `file1_stuff` 的变量中。因为 `module.exports` 指向 `greet` 函数，所以 `file1_stuff` 也将指向 `greet` 函数😁。

朋友们，这就是 CommonJS 模块系统在底层的工作原理！

同样地，让我们也完成对 `file2.js` 的可视化😅。

![Image](img/Image00287.jpg)
![Image](img/Image00288.jpg)
![Image](img/Image00289.jpg)

我们对 `file2.js` 也做了完全相同的事情并进行了可视化。你可以看到，从文件中导出的任何内容都可以按你的意愿重命名。

在结束本章之前，让我告诉你一件事：`exports`（IFEE 的第一个参数）和 `module.exports` 指向同一个地方😅。

`exports = module.exports`

因此，你可以直接使用 `exports` 关键字，而不必每次都写 `module.exports`（只需向 `exports` 对象添加键值对，不要将其重新赋值为全新的内容😅）。

**这样做：** `exports.add = add`，`exports.greet = greet`；

**不要这样做：** `exports = null` 或 `exports = add` 或 `exports = greet`（如果你这样做，将会破坏默认模块系统的行为）；

> 最后，ES6+ 模块系统是一个真正的模块系统，它不遵循上述机制，而是原生地解析文件内容并使其可用，无需包装。

```
That is all from my end friends, I hope you enjoyed learning as much as I enjoyed writing this book. I will try to add content to this book in future editions as well. All future updates will free who has access to the first edition😊.
```

***

## 7 额外内容

```
This chapter is just about some weird javascript facts😅
```

1. `typeof null` 的结果是 `object`，这是 JavaScript 中的一个 bug。
2. `typeof NaN`（非数字）实际上是 `'number'`。
3. `1 + 2 == 3` 但 `1.0 + 2.0 !== 3.0`🤨。
4. `NaN === NaN` -> `false`
5. `10/0` -> `Infinity`；`10/-0` -> `-Infinity`
6. `let newFn = new Function('num', 'return num * num');` // 动态创建函数😯。
7. JavaScript 是一种编译型语言，它会提前解析、优化和编译代码，并且只在运行时解释执行代码😉。
8. JavaScript 不是 Java（永远记住这一点）。
9. 这是一种非常容易学习的语言，但很难精通。
10. 下面的 `a` 数组中有一个元素，但长度仍然显示为 `0` 😂。

![Image](img/Image00290.jpg)

```
This is all my friends, I will keep updating this book with more content, till then enjoy learning and we will meet someday, sometime with some other book journey. Thank you for reading and happy Learning🥰.
```


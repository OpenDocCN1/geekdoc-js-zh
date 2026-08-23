

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

`内存`：计算机只是一台接收指令集并执行它们的机器，但在执行过程中，计算机需要保存一些信息用于计算或其他任务。因此，我们有像 `RAM` 和 `ROM`（`HDD`、`SSD`）这样的存储设备，它们临时或永久地保存信息。所以，内存只是我们保存信息的一部分。

`进程`：当前正在执行/运行的程序（打包的指令集）称为进程。每个进程只是计算机为完成给定任务所需执行操作的蓝图。

`线程`：进程是一组打包的指令，但每个指令也需要被执行才能完成原始进程，因此线程只是一个简单的轻量级运行进程（正在执行的一小组指令）。

`执行上下文`：它只是内存中当前正在运行的代码（每个运行的程序都需要内存），可以是普通的函数执行或普通的 JavaScript 代码，如 `if-else`、循环或任何其他表达式。

`内存 + 进程 == 执行上下文`

`作用域`：作用域是为特定或当前正在执行的函数或代码块分配的内存。也就是说，变量（内存）在其外部对函数或代码块不可用。

`作用域 == 执行上下文的内存限制`

`执行线程`：当前正在运行（执行）的函数或代码块是一个执行线程。也就是说，它是我们主进程内部的一个小型运行进程。

`调用栈`：它是一个容器，你可以在其中添加或移除代码块/函数，使得最近添加的内容在此容器中获得下一个执行线程的优先级。也就是说，后进先出（LIFO）模式。

在进一步讨论之前，让我先快速概述一下进程在高级层面是如何管理的。

1.  最初，任何程序（指令集）都被内存（通常是 `RAM`）收集，然后处理器开始执行该程序。
2.  处理器随后获取程序并开始执行，在此过程中，处理器可能需要执行额外的工作来完成给定任务，即处理器可能执行程序内部的程序（指令集可能需要其他指令），也就是线程也需要完成。
3.  程序完成后，操作系统将负责清理和其他一些依赖任务。
4.  现在，当给定程序可以逐个执行一组指令，并且没有执行额外的内部指令集时，该程序被称为**单线程**（运行 JavaScript 程序是一个单线程进程）。

***

在了解了术语之后，让我们通过一个小例子进一步理解这些内容。

#### 示例 1.1

*   首先，如果你不知道的话，JavaScript 是一种单线程且同步的语言，意味着 JavaScript 引擎/解释器一次只能执行一行或一个代码块。也就是说，你不能同时做多件事。此外，在执行代码时，你会逐行进行（同步）。
*   当你在浏览器或任何环境（`nodejs`、`react-native`）中执行代码时，我们在所谓的全局环境（首先是浏览器标签页，或 `node` 环境）中运行。我们定义的函数实际上首先进入全局内存（函数内部）。我们将这些函数投入执行时，首先被放入 `调用栈`，然后从 `调用栈` 中调用函数。
*   在我们开始给定代码之前，为我们目前学到的内容建立一个“心智模型”非常重要。

#### 当前 JavaScript 心智模型

*   在心智模型中，我们可以看到每个 JavaScript 程序都会获得全局内存（全局作用域）。
*   `提升` 是 JavaScript 的默认行为，它将所有声明移动到作用域（当前脚本或函数的顶部）。
*   在 JavaScript 中，每一行代码或函数定义都不会直接调用。相反，它会进入 `调用栈`，然后根据 `调用栈` 的优先级，函数放入执行线程中（后进先出）。

#### 示例 1.1 分析

*   在第一行中，我们声明了一个名为 `outerGoal` 的变量，并为其赋值 `0`。也就是说，我们在全局内存（作用域）中消耗了一小块内存空间，为内存贴上了 `outerGoal` 标签。
*   在下一行代码中，我们只是将该值记录到控制台。也就是说，我们记录了 `outerGoal` 的值。

#### JavaScript 执行心理模型

有一点需要注意，我不会绘制全局执行线程，但它始终在我们开始 JavaScript 代码时启动。让我们再次看看我们的 `心理模型`。

（此处省略重复的图片 描述性文字，保持核心逻辑一致）

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
说到像 JavaScript 和 Python 这样广泛使用的语言，我们不能直接忽略其常用的特性——“闭包”。因此，让我们了解一下它的底层工作。在开始之前，让我们先了解 JavaScript 函数是什么？！
```

### JavaScript 函数

*   JavaScript 函数是一个 `Object`！
*   意味着它可以拥有键值对，比其他更复杂（我们将在“原型”章节中详细讨论）。
*   函数是一种特殊类型的 `对象`，其特殊之处是可以存储代码块并在以后调用（运行）它们！

### JavaScript 函数

*   你可以将函数作为参数传递给另一个函数。
*   我们可以有一个函数返回，或者将匿名函数存储在变量中（存储在内存中）。
*   每个函数都有自己的局部内存/局部作用域（在第一章中解释）。
*   向函数添加任何键值对是一种能力，而这种能力帮助 JavaScript 实现了一个神奇的特性叫做 `闭包 (closure)`。让我们看看实现的！

#### MDN 定义

```
闭包是将函数与其引用周围的状态（词法环境）组合（封闭）。换句话说，闭包允许内部函数访问外部的作用域。在 JavaScript 中，闭包每次创建函数时都会创建，即函数创建时。
```

#### W3SCHOOL 定义

```
JavaScript 变量可以属于局部作用域或全局作用域。可以通过闭包变为局部（私有）变量。
```

我不倾向于将 W3School 作为可靠来源，但这一次我觉得 W3School 实际上更精准、更容易掌握，并且定义清晰。现在通过可视化来理解，为此，我将举一个简单的例子。

#### 函数定义

*   如示例所示，我们创建了一个名为 `createCapital` 的函数，随后使用对象字量向函数本身添加了 2 个属性（内部属性）。

#### 函数执行

*   根据当前的心智模型，你可以看到从全局内存到调用栈，再从调用栈到执行线程，我们已经将 `createCapital` 函数投入执行。
*   `createCapital` 函数拥有自己的局部作用域（环境），其中我们定义并存储了 `getCapital` 函数。
*   现在，让我们看看当我们执行完 `createCapital` 并返回 `getCapital` 时会发生什么。你最可能的猜测是，`createCapital` 的整个函数体和局部作用域将被销毁，而 `getCapital` 函数将被存储在名为 `accessCapital` 的变量中。

#### 函数内部结构

*   从图中看到，这两个属性都属于函数对象且是其一部分。函数可以在自身中持有属性。
*   我们终于到了将 `getCapital` 函数投入执行的地步（使用了 `accessCapital` 变量，它指向我们原始的 `getCapital` 函数定义）。
*   但是，按照常规行为，我们期望在执行 `getCapital` 时，变量 `wealth` 应该是 `undefined`，并且它不应该能访问已执行函数（即 `createCapital` 的内存）的局部内存。然而，生活并没有那么简单。
*   现在引入一个新朋友，叫做 `backpack`（背包），来拯救局面。

```
背包是一个简单的内存存储，带有与之相连的绳子（想象成一个真正的背包🎒），而这些背包的绳子将连接到何处是一个问题。
```

让我们实际可视化一下，当我们的外部函数 `createCapital` 执行完毕时，到底发生了什么！

#### 将背包附加到内部函数

*   正如你所见，我们的背包不过是外部函数作用域中的变量，当 JavaScript 看到这种外部作用域与内部作用域时，背包始终附加在函数对象上面。
*   这些属性成为了函数的一部分。

---

## 3. 原型、__proto__ 与对象

```
原型（Prototype）是 JavaScript 中的一个核心概念。每个对象都有一个原型，这允许对象继承属性和方法。
```



展示上述图表的主要目的是说明，逻辑上放在一起的值并不是它们在内存中的实际存储方式。

### 对象与原始值

* 在 JavaScript 中，除了**原始值**（字符串、数字、布尔值等）之外，一切都是**对象**。
* **函数也是对象**。
* **数组是对象**。
* **`Math`、`Date` 以及其他辅助函数也都是对象**。
* 在所有这些东西中，函数是最重要的。函数是对象，但它是特殊类型的对象。
* 函数有两个可用的部分。第一部分是函数体，我们可以在其中存储代码块，并在需要时调用它。第二部分是对象部分，我们可以在其中存储键值对。

![Image](img/Image0003.jpg)

* 我们在第 2 章中已经看到了证据，当时我们向函数对象添加了属性（如果忘记了，请重新检查😅在这里在这里我们将进一步了解我们可以做什么，或者有哪些东西可供我们使用。
* 有趣的是，每个函数对象默认都有一个 `prototype` 属性，而每个对象也都有一个 `__proto__` 属性。
* 因此，每个函数都将拥有 `prototype` 和 `__proto__` 属性，而每个对象都将拥有 `__proto__`（普通对象没有 `prototype` 属性，只有函数对象才有）。

![Image](img/Image00033.jpg)

* 在章中，我不会绘制整个 JavaScript 环境，因为这里不需要，我们将纯粹关注对象和函数及其链接是如何工作的。让我们从下面一个简单的例子开始（现在不要试图理解，我们马上会做）。

![Image](img/Image00034.jpg)

* 如你所见，我们创建了 `ArtistCreator` 函数，它帮助我们创建对象。你可以把它看作一个创建艺术家对象的通用函数。我们很快就会将其可视化，但在此之前，让我们先理解 `Object.create()` 为我们做了什么。

![Image](img/Image00035.jpg)

* JavaScript 中有很多全局对象（键值对）可供我们使用。`Object`（注意是大写字母 O）就是其中之一。它包含许多键值对，并且由 JavaScript 提供。
* `create` 是 `Object` 的一个方法，它有以下基本任务：
    1. 创建一个空对象。
    2. 由于每个对象都有 `__proto__` 属性，在创建空对象后，我们传递给 `create` 方法的任何参数，都会直接通过 `__proto__` 提供给新创建的对象。让我们看看具体是如何实现的。

![Image](img/Image00036.jpg)
![Image](img/Image00037.jpg)

* 我们正在执行 `ArtistCreator` 函数，它调用了 `Object.create()` 方法，并将全局存储的 `commonFunctionality` 对象作为参数传入。

![Image](img/Image00038.jpg)

* `Object.create()` 不仅创建了一个新的空对象，还为这个新对象的 `__proto__` 添加了一个指向全局存储的 `commonFunctionalities` 对象的引用。因此，我们传递给 `create()` 的第一个参数的所有内容，都会通过新创建对象的 `__proto__` 属性可用。让我们完成可视化。

![Image](img/Image00039.jpg)
![Image](img/Image00040.jpg)
![Image](img/Image00041.jpg)
![Image](img/Image00042.jpg)
![Image](img/Image00043.jpg)

* 如你所见，我们可以通过函数创建新对象，而且还可以反复重用这个函数。

![Image](img/Image00044.jpg)

* 如果我们再次运行同一个函数，如上所示，我们仍然可以重用它的功能，并且还可以利用已经声明的 `commonFunctionalities`。请看下面的图示，我们对 `artist2` 对象也做了同样的操作（请像上面展示的那样，自己走一遍心智模型）。

![Image](img/Image00045.jpg)

* 好了，我们已经创建了一个功能，允许我们在需要时创建对象，并且可以重用一些现有的功能。现在，如果 JavaScript 本身就提供了这种特性，那该多好啊😋。
* 幸运的是，它确实有，而这正是我们接下来要做的。请看下面的示例，我们很快就会理解。

![Image](img/Image00046.jpg)

* 如果你忘记了，函数默认拥有 `prototype` 和 `__proto__` 属性。同样，`ArtistCreator` 也会拥有这些属性。让我再次展示那张图。顺便提一下，`prototype` 是一个对象，我们可以向它添加任意键值对。

![Image](img/Image00047.jpg)

* 现在，向 `prototype` 对象中添加什么内容由我们决定。在我们的示例中，我们添加了两个函数：`isHuman` 和 `isCuriuos`。

![Image](img/Image00048.jpg)

* 注意，我们的示例现在也使用了 `new` 关键字。它在幕后做了大量的自动化工作。让我们看看它的图示是怎样的。

![Image](img/Image00049.jpg)

* 让我们执行下面这行代码，注意函数调用前面的 `new` 关键字。

![Image](img/Image00050.jpg)

```

`new` 关键字主要做两件事：

1. 它会创建一个新的**空对象**，并且这个新创建的对象会获得 `this` 引用。这意味着在函数执行过程中，`this` 将指向由 `new` 关键字创建的新对象。
2. 此外，函数的 `prototype` 对象（在我们的示例中是 `ArtistCreator` 函数）中的所有内容，都会指向新创建对象的 `__proto__`（当然，我们来可视化一下😅）。

```

![Image](img/Image00051.jpg)

* 每个函数对象都有两部分，我们知道，一部分是函数体，另一部分是对象部分。
* 在下面的图示中，你可以看到 `ArtistCreator` 的对象部分包含一个 `prototype` 对象和一个 `__proto__` 对象。
* 在我们的代码中，我们向 `prototype` 对象添加了两个函数：`isHuman` 和 `isCurious`。
* 每个对象默认都拥有 `__proto__` 属性。这就是为什么 `prototype` 对象也拥有 `__proto__` 属性（这个属性指向哪里尚不清楚，但让我们先专注于代码的执行）。

![Image](img/Image00052.jpg)

* 函数 `prototype` 对象指向新创建对象的 `__proto__` 属性。
* 现在，我们知道 `new` 关键字帮助我们建立了 `prototype` 对象到新创建对象的 `__proto__` 属性的引用。请看下面。
* 还有一点，函数执行已经结束，但函数的对象部分仍然保留在内存中。这里并不是复制对象，只是设置引用。

![Image](img/Image00053.jpg)
![Image](img/Image00054.jpg)

* 永远不要忘记，函数执行已经完成，但函数的内存不会被清除。这就是为什么带有 `prototype` 对象的 `ArtistCreator` 函数会保留在内存中。

![Image](img/Image00055.jpg)

* 就是这样我们现在能够通过函数创建对象，并且一些公共功能通过 `prototype` 对象获得。
* 现在，`artist2` 也是同样的道理，所以我不再画部分了（现在你可以可视化）。

![Image](img/Image00056.jpg)
![Image](img/Image00057.jpg)

* 我们使用函数创建对象，因此我们称之为“构造函数”。这里的 `ArtistCreator` 就是构造函数。
* 在结束上面的示例之前，让我们在浏览器台中输出结果。

![Image](img/Image00058.jpg)

* 到目前为止顺利，但 ES6+ 为我们提供了新的语法，它可以实现上面代码相同的功能。它只是试图语法。在底层，工作原理不变。让我们看看上面的等效代码。

![Image](img/Image00059.jpg)

* `class` 关键字是在 ES6+ 中引入的，用于模仿之前的工作。它并不复杂，只是我们的 `prototype` 方法直接定义在 `class` 内部，而 `constructor` 充当函数体。
* 我们已经学会了如何通过构造函数创建对象。那么，如何扩展我们的功能，并利用现有的构造函数创建另一个构造函数？让我们通过一个示例来看一下。首先我们将采用非类版本，然后创建等效类。

![Image](img/Image00060.jpg)

* 如果你不理解上面的代码不用担心，我们将逐步解释它是工作的。上面示例中唯一注意的是，我们可以将 `ArtistCreator` 的 `prototype` 函数继承到新创建的 `Entrepreneur` 的构造函数中。

![Image](img/Image00061.jpg)

* 我们首先可视化上面行代码。这将与刚刚展示之前的示例类似。

![Image](img/Image00062.jpg)
![Image](img/Image00063.jpg)
![Image](img/Image00064.jpg)
![Image](img/Image00065.jpg)
![Image](img/Image00066.jpg)

* 到目前为止与之前示例相同。现在，让我们看看运行下面代码会发生什么。
* 另外，我在这里跳过了 298 到 303 行的执行，因为我不想让接下来的图示让你困惑。实际上，我们将在完成高亮执行后，再展示 298 到 303 行的图示。

![Image](img/Image00068.jpg)

* 不要忘记，即使执行结束，`ArtistCreator` 的对象部分仍保留在内存中。当我们再次调用 `ArtistCreator` 时，我们将使用内存中存储的引用，而不是创建它的副本。

![Image](img/Image00069.jpg)
![Image](img/Image00070.jpg)

* 我们使用 `call` 关键字调用一个函数，并将 `this` 作为第一个参数传递。

```
call() 方法使用给定的 this 值和单独提供的参数来调用一个函数。
```

* 因为我们在 `Entrepreneur` 函数前面使用了 `new` 关键字，所以我们将创建一个空对象，并且 `this` 关键字将指向它。然而，`Entrepreneur` 内部使用 `call()` 方法调用了 `ArtistCreator`，并传递了新创建的对象（此时 `this` 关键字指向新创建的空对象！

![Image](img/Image00071.jpg)

* 这里我们只是向新创建的对象添加属性。
实际上，参数是通过引用传递给 `ArtistCreator` 函数的，而 `Entrepreneur` 函数提供了这些值。跟着图示走，你就能理解。

![Image](img/Image00073.jpg)

* 默认情况下，新创建的对象（`this`）会拥有诞生处原型对象的引用。
* 在我们的例子中，我们使用 `ArtistCreator` 作为新创建对象的“母体”。因此，新创建对象的 `__proto__` 将指向 `ArtistCreator` 的原型对象。

![Image](img/Image00074.jpg)

* 执行完 `ArtistCreator` 函数后，我们将继续执行 `Entrepreneur` 函数，并在新创建的（`this`）对象上添加一个属性 `communicationSkill`。
* 我在这里保留了函数的对象部分，因为这有助于我们更好地理解。

![Image](img/Image00075.jpg)

* 另外，如你所见，我们现在也完成了 `Entrepreneur` 函数的执行。

![Image](img/Image00076.jpg)

* 现在，关键部分来了。记得我之前让你忽略 298 到 303 行吗？让我们看看当执行它们时（实际上执行已经完成，但我现在展示是因为这样更容易可视化），它们在幕后发生了什么。

![Image](img/Image00077.jpg)
![Image](img/Image00078.jpg)

* 如知 `Object.create()` 会创建一个空对象，而刚创建的空对象的 `__proto__` 将指向我们传递给 `create()` 方法参数的任何内容。

![Image](img/Image00079.jpg)

* 因为我们重新赋值了 `Entrepreneur.prototype`，所以 `Entrepreneur` 的旧原型对象将从内存中销毁。我们从 `Object.create()` 方法调用中得到的任何内容都将赋值给 `Entrepreneur.prototype`😃。

![Image](img/Image00080.jpg)



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

* 每个 JavaScript 对象实际上都源自于 `Object`（注意大写字母 'O'）。这是我们原型链的终点（稍后会看到）。

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
* 浏览器环境非常庞大，包括 HTML/CSS 解析器、控制台、网络监控、存储（`local`、`Indexeddb`、`web` 等）、性能工具等。我们只关注异步部分通过所谓的“队列”和“事件循环”来处理。

### JavaScript 是同步的！（别忘了）

* 时间和资源在每个应用程序或现实中始终很重要。JavaScript 是同步的，这一点重要，以至于很多人忘记了 JavaScript 只是一种语言，在早期只是用来让网页变得动态。
* 最终，JavaScript 从为服务器或今天所做的复杂而构建。
* 2004 年，谷歌发布了 Gmap，完全由浏览器上的构建，震惊了世界，展示了 JavaScript 语言的潜力。
* 让我们进入异步环境的实际实现。请记住，`Queue` 是浏览器实现的，因此有时你会看到不同输出/结果，而不是实际期望。我们将采用正确的方法。

![Image](img/Image0014.jpg)
当前的心智模型

### 回调：被回调的函数

* 在进一步讨论之前，有必要谈谈回调。
* 回调是简单的函数，当它们被回调时（即当特定任务完成后）被调用。
* 有两种回调：
    1. 同步回调
    2. 异步回调

#### 1) 同步回调
* 同步回调在迭代器上被调用，简单且快速。
* 下面是一个同步回调的例子。

![Image](img/Image0015.jpg)
同步回调

#### 2) 异步回调
* 异步回调是耗时的任务或容易出错（可能不会完成）。
* 下面是一个异步回调的例子！
* 不要试图深入理解，只是一个例子。

![Image](img/Image0016.jpg)
异步回调

* 当然，我们已经扩展了心智模型，但需要注意的是，`Queue` 不仅仅是 JavaScript。它是浏览器的一部分（例如 `setTimeout`、`setInterval` 等）。
* 但这里有一个转折，`promise` 比这更复杂，既是 JavaScript 的一部分，也是浏览器的一部分。
* 目前，让我们看一个带有队列的简化版心智模型。

![Image](img/Image0017.jpg)
带队列的心智模型

### Queue：一种简单的数据结构

* 遵循先进先出规则（即谁来谁走）。就像电影票一样。

#### 任务队列 (Task Queue)
* 首先奇怪的是，任务队列并不是一个队列，而是一个 `set`（在 C++ 世界中是）。
* 添加到任务队列中的任务会被取出并移除，而不是像队列那样出队。为了简单起见，将其视为普通队列（大多数 JavaScript 开发者这样做）。`宏任务` 是任务队列使用的术语。

#### 作业队列 (Microtask Queue)
* 作业队列是一个真正的队列，任务在其中入队和出队。它是一个真正的队列。
* `微任务` 是作业队列使用的术语，但在 ES6+ 规范中它被称为作业队列。

### 是时候通过一个例子来理解了

![Image](img/Image0018.jpg)

### 事件循环简介

```
The event loop is a simple while loop, which keeps tracks that where any work is pending in queue/s to be finished or not with continuously checking that whether callstack is ready for taking the work from the queue/s or not.
```

![Image](img/Image00124.jpg)

* 现在，由于当前我们的 `callstack` 为空，而队列中有待完成的任务，事件循环会找到它。请注意，`delayedTimer` 实际上是在 2000 毫秒后（我们提供了时间，即它实际成为任务队列一部分所需的时间）才被放入 `task queue` 的。
* 事件循环的任务只是检查队列是否有待处理的工作，以及这些任务是什么。
* 函数 `delayedTimer` 会被环境推送到 `callstack` 中，并成为正常执行的一部分。

![Image](img/Image00125.jpg)

![Image](img/Image00126.jpg)

![Image](img/Image00127.jpg)

![Image](img/Image00128.jpg)

各位朋友，这就是 JavaScript 中异步代码的执行方式。还有更多内容有待探索：Promise 和 Async Await。在本章中，我只会解释 Promise，因为 async-await 需要更多知识，我们将在后续章节中讨论。

### Promise——一种优雅的异步任务解析器

**MDN**

```
The Promise object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
```

* 当然，这是一个简短而简单的定义，但并没有解释底层到底发生了什么！
* 让我用一个直观的例子更简单地为你解释 Promise。
* 在上面的例子中，我创建了一个简单的 `sleep` 函数，用于模拟给定秒数的同步阻塞机制。我们将在下一个例子中继续。
* 有一个 `sleep` 函数，我模拟了它在给定秒内阻塞函数。让我们看看它的心智模型，它将如何执行！
* `setTimeout` 是一个浏览器特性，不是常规 JavaScript 的。等待定的时间，将回调函数放回任务队列是由浏览器完成的。

![Image](img/Image0019.jpg)

* 现在让我们看看执行完 `sleep` 函数并尝试进一步执行时发生什么。

![Image](img/Image00120.jpg)

* 另外，请注意我们定义了 `delayedTimer` 函数，但从未调用它。因此，它仍然不在调用栈中，并且作为参数传递给了 `setTimeout`。

![Image](img/Image00121.jpg)

![Image](img/Image00122.jpg)

![Image](img/Image00123.jpg)

* 根据上面的图片，我们可以看到调用栈的所有执行（包括全局表达式和语句代码）都已完成。
* 简而言之， JavaScript 会直接执行所有同步代码，而所有异步操作只是被推迟到后续执行。然而，所有函数引用仍然存储在全局内存中，它们不会被复制到任务/作业队列中。

### Promise 的内部机制

* `Promise` 是一个对象，它代表了异步操作的最终完成或失败的结果。
* 它有三种状态：`pending`（等待中）、`fulfilled`（已完成）和 `rejected`（已拒绝）。
* 我们使用 `resolve` 和 `reject` 函数来改变 Promise 的状态。

```
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve("Success!");
  }, 1000);
});

myPromise.then((result) => {
  console.log(result);
});
```

* `then()` 方法用于处理 Promise 的成功回调。
* `catch()` 方法用于处理 Promise 的失败回调。
* `finally()` 方法用于无论成功或失败都会执行的回调。

* 通过理解 Promise 是掌握现代 JavaScript 异步编程的关键。



![Image](img/Image00142.jpg)

* 如果 `num < 5`，我们将调用 `reject`，并将 `num` 作为参数传递给 `reject`。

![Image](img/Image00143.jpg)

在这两种情况下，如你所见，它都会被存储在 `Promise` 对象的 `value` 属性中。

* 现在，我们可以看到 `promiseObj`（返回对象的标签）实际上在当前作用域中可用，并且无论 `Promise` 处于什么状态（resolved 或 rejected），它都会被存储在 `promiseObj` 的内部属性中，同时 `value` 将作为 resolved/rejected 值的占位符。但是，要访问 resolved 值或 rejected 值，我们需要某种机制。

* 这就是为什么我们有 `then` 和 `catch` 方法可用。这两个方法通过 `__proto__` 提供给我们（将在后续章节中详细了解原型和链）。

* 这里我们还缺少一部分：`onFullfillment` 和 `onRejection` 是数组，它们实际上是如何工作的呢🤨！

* 在这里，在 `Promise` 对象内部的值求值完成后，`Promise` 函数构造函数的工作就结束了（对于 resolve 和 reject 两种情况都是如此）。

* 让我们先可视化这一部分。

![Image](img/Image00144.jpg)
![Image](img/Image00145.jpg)
![Image](img/Image00146.jpg)
![Image](img/Image00147.jpg)

哇，内容真多。但我们还需要弄清楚 `then` 和 `catch` 方法😅！

* 有一件事我没有告诉你：每当我们编写 `then` 或 `catch` 方法时（在常规全局上下文中），这些方法实际上是在 `promiseObj` 创建时通过引用 `promiseObj` 的 `onFullfillment` 或 `onRejection` 键而变得可用的。

* 不仅如此，每当我们求值 `value` 时，该值将可用于 `then` 函数的参数（作为参数的函数）或 `catch` 函数的参数。

* 让我们看看这两种情况！

```
Resolve 函数场景
```

![Image](img/Image00148.jpg)

* 这里有一个错觉，那就是 `then` 方法😯！所以，看起来像是在返回的 `promiseObj` 上执行的代码实际上并不是由 `then` 方法运行的。它只是一个函数，充当另一个函数的占位符。因此，无论我们作为参数传递给 `then` 方法（这里是 `(val) => { console.log(val) }`）的函数是什么，都会被推送到 `promiseObj` 的 `onFullfillment` 数组中。另外，我之前没有展示这一点，因为我不想与其他可视化混淆。`then` 方法实际上通过 `promiseObj` 的 `__proto__` 访问的。让我们可视化它😎。

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

* 就这样😅，底层发生了大量的事情。这就是 Promise 的工作方式。那么浏览器中可用的、同样基于 Promise 的 `fetch` 又是怎样的呢！它的工作方式与上面的示例几乎相同，但有一个小反转。为什么不通过简单的示例来探索它的可视化呢。

![Image](img/Image00167.jpg)

* 这里，我们有一个简单的 `console.log`，一个 2 秒的阻塞，以及 `fetch` 代码。让我们开始将其可视化。

![Image](img/Image00168.jpg)
![Image](img/Image00169.jpg)
![Image](img/Image00170.jpg)
![Image](img/Image00171.jpg)
![Image](img/Image00172.jpg)

* 我们没有其他运行同步代码，因此我们将退出全局上下文，调用栈变为空。

![Image](img/Image00174.jpg)
![Image](img/Image00175.jpg)

* 我认为到为止，一切看起来与之前一样，但这里的反转来了。上面显示的心理模型是不完整的。

* 我们有很多浏览器特性（又称浏览器 API），它们发生在常规上下文之外。不仅如此，这些浏览器特性实际上是通过操作系统实现的。但为了简明扼要，我们只需认为浏览器特性发生在 JavaScript 执行之外。

* 其中一个特性就是 `fetch API`。

* 让我们把我们的心理模型扩展一点。

![Image](img/Image00176.jpg)

* 如你见，我们在图表中添加了浏览器特性，现在你可以感觉到浏览器环境不仅仅是 JavaScript，而是底层结合了许多特性的。

![Image](img/Image00177.jpg)

* 这里，让我们看看在执行代码时，运行 `fetch('https://test.com')` 这一行发生什么。

* 我们再次回到实际返回 `PromiseObject` 时发生什么。

![Image](img/Image00178.jpg)

* 我们可以看到，`fetch` 实际上建立了两种绑定：一种在 JavaScript 任务中，另一种是网络工作。让我继续可视化。

![Image](img/Image00179.jpg)

* 在代码中执行到 `fetch` 行后，从 `fetch API` 返回 Promise 对象的工作会立即完成，但 API 调用的后台任务仍在挂起，由浏览器完成，并在完成后交给 Promise 对象。

* 在完成后台工作后，所有其他工作与之前可视化的一样。

![Image](img/Image00180.jpg)
![Image](img/Image00181.jpg)
![Image](img/Image00182.jpg)
![Image](img/Image00183.jpg)
![Image](img/Image00184.jpg)
![Image](img/Image00185.jpg)
![Image](img/Image00186.jpg)

```
这就是全部了，朋友们，这就是 Promise 和 fetch API 在底层真正的工作方式。
```

***

## 5 迭代器、生成器和 Async-Await

```
本章将深入解释迭代器（iterator）和生成器（generators）及其重要性。此外，还将介绍这些内容在实际场景中如何被利用，以使代码看起来更美观且易于阅读。不仅如此，本章还将包含非常高密度的可视化内容。
```

### 循环 (Loops)

* 在进入迭代器之前，我们先谈谈传统的循环。

* 我们使用循环来遍历 `iterable` 的每个元素并执行操作。让我们来看简单的例子。

![Image](img/Image00187.jpg)

* 在上面的示例中，我们有一个简单的 `numberArray`，我们正在遍历元素并简单地乘以 2。

* 请注意，我们是在一次性的执行操作。我们无法控制这种一次性操作（你可以加入 if-else 等内容来控制流程，但这并不是对元素的真正控制！）。

* 如果我们能一次获取一个元素对其执行某些操作会怎样？这样每当我们需要下一个元素时，只需产生它即可。初听起来可能有点奇怪，但让我通过构建一个自定义迭代器来举例。

* 为了简单起见，我将使用心理模型的简化图，当我们结合所有概念时，会制作一个完整的心理模型图。对于下面的示例，我将仅显示执行线程和内存。

### 迭代器 (Iterators)

![Image](img/Image00188.jpg)

我们声明了一个名为 `createFlowOfElements` 的函数，它实际上是一个接收数组作为参数并返回 `innerObj` 的函数。让我们执行这个函数。

![Image](img/Image00189.jpg)

现在是时候可视化执行 `createFlowOfElements` 时发生了什么。

![Image](img/Image00190.jpg)

* 如果你还没猜到的话，这里有一个函数嵌套在函数内部（即使它定义在 `innerObj` 内部）。因此，如果我们返回 `innerObj` 或 `innerObj` 的函数，我们将拥有外部作用域（这就是闭包）。

`createFlowOfElements` 是实际上要创建迭代器的函数！让我们将其可视化。

![Image](img/Image00191.jpg)
![Image](img/Image00192.jpg)
![Image](img/Image00193.jpg)

* 太棒了，我们可以看到 `returnNextElement` 具有闭包，不仅如此，对象内部还有一个 `next` 方法（人们通常称为方法）。此外，我没有显示全局变量 `element1` 和 `element2`，因为在上面的图中不需要对变量进行真实。

![Image](img/Image00194.jpg)

* 现在，是时候看看执行 `returnNextElement` 的 `next` 方法时发生什么。

![Image](img/Image00195.jpg)
![Image](img/Image00196.jpg)

* 因为函数本地内存没有变量，所以我们在闭包中查找这些。

![Image](img/Image00197.jpg)
![Image](img/Image00198.jpg)

* 现在，对于 `element2` 发生的事情完全一样，所以我不再为此绘制图。这是执行完成后最终的图。

![Image](img/Image00199.jpg)

刚刚创建了第一个迭代器，也就是说我们现在拥有了一种控制流，而不是一次性完成所有事情。因此我们不再是将元素直接扔进管道，而是拥有一个用来获取元素的开关。

* 迭代器很重要，因为我们可以获得控制权。这是一个强大的机制，有助于从零开始构建一些特性（很快就会看到）。

* 此外，你可以想象迭代器是通过事件循环维护的，使它们在调用栈中可用。

### 生成器 (Generators)

`generator` 简单来说就是一个迭代器的函数！在上面的示例中 `createFlowOfElements` 实际上就是一个返回迭代器的生成器函数！

![Image](img/Image00200.jpg)

* 从上面的示例可以看出，原生生成器看起来非常简单且易于编写。原生生成器与自定义生成器的工作方式有一个小区别。

* 第一个区别是，原生生成器是一种特殊的函数（你在函数定义中看到了）。原生生成器函数依赖隐藏属性（记住函数也是对象）。

* `yield` 是一种特殊的关键字，它在幕后执行了很多操作。第二点区别是，生成器函数（generator function）不会被放入调用栈（callstack），而是存储在内存中直接放入执行线程！

### return

* `return` 关键字会立即停止函数执行，并允许你从函数返回任何值。

* `return` 关键字主要执行某些操作，并将结果返回给外部作用域。

### yield

* 这是一种特殊的关键字，用于生成器函数内部。

* `yield` 关键字不会停止生成器函数的执行，而是会挂起执行（暂停执行）。这样我们稍后可以使用同一个挂起的执行上下文。

* 现在，当我们挂起函数执行时，我们需要某种机制来跟踪执行具体何处被挂起。这样在下一次迭代中我们能够从挂起（暂停）的地方重新执行。

* 在生成器函数返回的迭代器上，有一个名为 `[[GeneratorLocation]]` 的隐藏属性。

* `yield` 关键字会挂起执行，并将函数被挂起的位置存储在 `[[GeneratorLocation]]` 中。

![Image](img/Image00201.jpg)

* `[[GeneratorLocation]]` 处于 `VM36:3` 的原因是，你可以看到我们调用了 2 次 `returnNextElement.next()`。因此，有两个值被 yield 出来了，函数经历了暂停和继续。所以在下一次迭代中，我们将从第 3 行（准确说是 yield 值的第 3 个位置）开始执行。

* 如果你点击 `VM36:3`（`VM36` 是由控制台随机生成的），我们将能够看到函数最后一次挂起的位置。

![Image](img/Image00202.jpg)

现在，如果生成器函数内部有其他内容会怎样？比如 `console.log()` 或任何其他操作！

![Image](img/Image00203.jpg)

* 如你所见，它的工作方式与之前完全一样，但现在 `[[GeneratorLocation]]` 是相对于函数定义的。这意味着它实际上在跟踪函数暂停的行号！

* 现在如果我们点击那个 `VM107:4`，我们可以在下方看到它暂停的位置。同样，因为我们使用了 2 次 `returnNextElement.next()`，所以我们在第二个 yield 值之后暂停了。

![Image](img/Image00204.jpg)

* 我们还没有看到 `element1` 和 `element2` 变量中实际包含什么。让我们来看看。

![Image](img/Image00205.jpg)

* 与我们之前直接返回值的自定义生成器不同，这里返回的是一个包含若干键值对的对象。

* 我们有 `value` 属性本身和 `done` 属性。

* `value` 保存的是 yield 出来的任何内容，而 `done` 告诉我们是否还有执行内容。

* 但是，等等，这里没有闭包，那么这个对象是从哪里检索到的！让我们看看。

![Image](img/Image00206.jpg)

* 如你所见，我们将 yield 的值存储在 `[[scopes]]` 的隐藏属性中。

* 现在，如果我们再次运行一次 `returnNextElement.next()` 并查看结果怎样。

![Image](img/Image00207.jpg)

* 现在，如果我们再次运行一次 `returnNextElement.next()` 并查看结果怎样。

![Image](img/Image00208.jpg)

* 如你所见，当我们完成所有值的 yield 之后，我们关闭（结束）了函数执行，并且 `done` 属性变成了 `true`。

* 简而言之，生成器允许我们创建自定义迭代器，我们可以对可迭代对象使用 `next()` 方法来检索 yield 的值。

为了全面了解生成器和迭代器，我们还需要探索一件事。请看下面的示例。

![Image](img/Image00209.jpg)

常见的想法是，我们在第一次调用 `next()` 时会 yield `4`，在第二次调用 `next()` 时，`newNum` 变量将为 `4`。因此，第二次 `next()` 调用应该让我们得到 `9` (`5 + 4 == 9`)。不幸的是，它的工作方式并非如此😅。

让我们看看输出结果。

![Image](img/Image00210.jpg)

如你所见，第二次调用 `next()` 的输出与我们的预期完全不同。之所以发生这种情况，是因为生成器函数返回的迭代器允许你向 `next()` 函数传递一个参数，而我们传递给 `next()` 函数参数的任何内容，都将传递到函数挂起执行的地方！



因此，最终我们传递给第二次 `next()` 调用的参数 `13` 被传递并存储在 `newNum` 中。所以在下一次 `yield` 中，它变成了 `18` (`5 + 13`)😄。

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

`深紫色` - 正在执行的生成器函数

`浅紫色` - 处于挂起状态（暂停）的生成器函数。

![Image](img/Image00214.jpg)

* 还有一点，生成器函数不是普通函数，它们不会被垃圾回收（即使在执行结束后，它们仍保留在内存中）。

* 此外，函数的执行被直接放入执行线程中。

![Image](img/Image00215.jpg)

* 关于那个 `__proto__`，其实很简单。生成器函数对象是由 `Generator` 对象构建的。因此，生成器函数对象的 `__proto__` 指向 `Generator` 的原型对象 (`generator.__proto__ = Generator.prototype`)。同样地，`returnNextElement` 是由生成器函数构建的。因此，`returnNextElement`对象的 `__proto__` 指向生成器函数的原型对象 (`returnNextElement.__proto__ = generator.prototype`)。

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

* 让我们看看它在进一步执行中的表现。

![Image](img/Image00227.jpg)

* 因为我们使用从 Promise 对象的 `value` 中获取的 `data` 调用了 `next()` 方法，所以我们将该值提供给 `next()` 迭代器的局部变量。

![Image](img/Image00228.jpg)
![Image](img/Image00229.jpg)
![Image](img/Image00230.jpg)
![Image](img/Image00231.jpg)

```
There you have it, my friends. we have made our own custom async-await from scratch😎.(you can do the same with a catch scenario as well, which I am not going to show😅)
```

在结束本章之前，让我们通过示例看一下 async-await 的简化 ES7+ 语法。

![Image](img/Image00232.jpg)

* 如你所见，`async` 关键字的行为类似于生成器，而 `await` 关键字的行为类似于我们示例中的 `yield` 关键字。也就是说，这就是本章的底层原理和深入探讨😊。

* * *

# 6

# NodeJS、C++、队列与服务器

```
If someone would ask me, what is the best thing that happens in the javascript community?, my immediate answer will be it is none than NodeJS!.NodeJS is an amazing javascript runtime and also a little misunderstood tool. In this chapter, I will try to make it as easy as possible and explain the core architecture and fundamentals of the nodejs.
```

### Node 不是什么？

1. 它不是一种编程语言。
2. 它不是用于服务器端编码的框架/工具。
3. JavaScript 是一种语言，而 Node 不是。

### Node 实际上是什么？

1. 它是一个底层 C++ 委托，通过提供 JavaScript API（即 C++ 特性的 JavaScript 绑定的代码）来供我们使用。
2. 它实际上是一个 C++ 程序，将 JavaScript 代码作为接收并完成工作！
3. Node 是一个单一 C++ 程序，依赖于许多其他 C++ 库，如 `libUV`、`V8`、`c-ares`、`OpenSSL` 等。
4. 我们称之为 NodeJS，因为它用 C++ 编写并暴露了 JavaScript API 供我们使用。

```
NodeJS's core architecture is way more complicated than any browser or other environment. Not only that, on the internet 90% of information related to nodejs are false or misguided.
```

* 我将循序渐进地讲解架构，将其拆分为部分，这样你就不需要再去哪里理解。让我们从基本图开始。

![Image](img/Image00233.jpg)

* 如所示，我们有一个类似的模型：队列、调用栈和内存空间。
* 因为我们要在计算机上执行大量操作，Node 实际上使用了第三方 C++ 库来完成任务。
* 我们首先理解两个主要组件。

### V8 引擎

* `V8` 引擎有一个基本任务：解析 JavaScript 并将其转换为化的机器码。
* 然而，`V8` 仅仅是将 JavaScript 代码转换为机器码，它做的不止这些。
* `V8` 提供了默认循环，但 Node 实际上并没有使用它。
* `V8` 有一个默认循环，Node 使用的是 `LibUV` 的循环。
* 因为 `V8` 有一个默认的任务队列，Node 使用了一种稍微不同的方法处理定时器。
* Node 提供了 `process.nextTick()`，它被设计为始终在所有队列之前运行。

![Image](img/Image00234.jpg)

### LibUV

* `LibUV` 库是 Node 的核心。
* `LibUV` 不仅提供了循环，还拥有非常好的机制处理大量 I/O 操作。
* I/O 操作可以是任何东西，比如连接请求、套接字、文件系统等。
* `LibUV` 提供许多队列，我们很快就会学习。
* 让我们结合 `V8` 和 `libUV` 的心智模型。

![Image](img/Image00235.jpg)

* 上方，我们故意留了一些空间。
* 从图中可以看到我们有 `V8` + `LibUV` 的队列。
* `LibUV` 有 7 个主要队列（因为 Idle 和 Prepare 合并为一行）：

1. **定时器**：`setTimeout()` 和 `setInterval()`。
2. **待处理回调**：想象一下，父进程是 `Nginx`，它已经在 3000 端口运行，那么它会抛出一个错误（系统错误）。这类系统调用或回调都会被队列。
3. **Idle 和 Prepare**：与之交互。
4. **Poll**：所有 I/O 操作，如文件处理、客户端请求、套接字、加密（zlib）操作等，都通过此队列处理。
5. **Check**：用于 `setImmediate()` 回调。
6. **Close**：所有来自系统的关闭事件，如套接字关闭或清理事件，都被此队列（为什么？因为这些是系统调用，而不是请求）。

默认的 `libUV` 和 `V8` 心智模型并不难。问题是 Node 内部做的事情远不止这些队列，最重要的部分是 `poll` 队列。

* 从图中我们可以看到一些奇怪的东西，比如 `线程池` 和 `Epoll/KQueue`（数据结构），用于处理从 `poll` 队列委托过来的工作。
* 不仅如此，我们还有工作线程，这也是不同的东西。
* 在底部，我们有操作系统特性，你可以称之为“内核”。
* 在进一步解释所有东西如何工作之前，让我们完成 Node 架构。

![Image](img/Image00236.jpg)

* 我们知道我们将编写“JavaScript”，任何系统级代码都需要用 JavaScript 编写，然后委托给我们的 C++ 代码。这就是为什么有 Node Core APIs。
* 它包含了所有模块逻辑，这些逻辑用 C++ 编写，暴露为 JavaScript API 供开发者使用。
* `C++ Addon` 和 `N-API` 是我们可以使用的特殊特性或 API，用于通过 C++ 扩展（这需要 C++ 知识）。

### Node 内部的正常执行流程

**步骤 1**：扫描整个代码，提升所有可能的变量。对未使用的引用进行垃圾回收（优化）。
**步骤 2**：从上到下完成所有同步执行。
**步骤 3**：扫描所有异步代码的事件程序或回调，并将其作为未来的占位符存储在内存中。
**步骤 4**：开始通过队列执行所有完成的后台代码，并持续进行，直到完成所有后台任务或终止进程。

Node 环境中队列的顺序所示：

1. 执行所有 `process.nextTick()` 的回调。
2. 执行所有 `Promise`。
3. 进入 `LibUV` 的队列，并从右向左执行：
    3.1 通过 `Timer queue` 完成定时器。
    3.2 通过 `Pending queue` 完成系统调用的错误处理回调。
    3.3 完成内部使用的 `Idle`, `Prepare queue`。
    3.4 等待一段时间，尝试尽可能地完成 `poll queue` 中的回调（稍微复杂，稍后会深入理解）。
    3.5 完成 `check queue` (`setImmediate`）。
    3.6 通过 `close queue` 完成关闭回调的执行。

### 步骤 5：重复循环直到 Node 进程被终止

现在，我们通过一个示例来理解所有内容，并深入了解每一步发生了什么。

![Image](img/Image00237.jpg)

> 暂时忽略 `require()` 以及模块系统的工作原理，只关注我们的示例。另外，我特意编写了一段 JavaScript 代码，使其执行结果与代码逻辑显示的结果完全不同，产生意想不到的输出。

![Image](img/Image00238.jpg)

* 一开始，我们读取文本文件的内容，即 `file1.txt` 和 `file2.txt`。
* `file1.txt` 的内容是“Hello guys 1”，`file2.txt` 的内容是“Hello guys 2”。

![Image](img/Image00239.jpg)

* 下一条语句是非常简单的同步日志输出。

![Image](img/Image00240.jpg)

* 接下来，我们使用了如上所示的 `process.nextTick()`。

![Image](img/Image00241.jpg)

* 接下来，我们使用了 `setImmediate()`。

![Image](img/Image00242.jpg)

* 之后，我们使用了 `then()`。

![Image](img/Image00243.jpg)

* 最终，我们使用了 `setTimeout()`。

![Image](img/Image00244.jpg)

* 最后，我们使用了 `Promise`。

![Image](img/Image00245.jpg)

*  最后，我们使用了 `console.log()`。

![Image](img/Image00246.jpg)


```markdown

* 现在，让我们开始执行队列。记住队列的顺序：从上到下，从右到左。

![Image](img/Image00255.jpg)

![Image](img/Image00256.jpg)

接下来轮到我们的 `Job Queue`（`Promise` 队列）。

![Image](img/Image00257.jpg)

![Image](img/Image00258.jpg)

![Image](img/Image00259.jpg)

![Image](img/Image00260.jpg)

* 现在轮到我们的定时器了😃。

![Image](img/Image00261.jpg)

![Image](img/Image00262.jpg)

![Image](img/Image00263.jpg)

* 这次轮到 `Poll` 队列了，但 `Poll` 队列中有 4 个操作：2 个文件读取和2 个 `GET API` 调用。因此，`libUV` 会在内部计算超时时间，判断这些操作是否能在一定时间内（通常是很短的几秒内）快速完成。如果不能，则立即转到 `Check` 队列。这就是为什么我们在这里会快速转到 `Check` 队列中的 `setImmediate()` 回调，而不等待这4 个操作（2 个文件读取 + 2 个 `GET API` 调用）完成。

![Image](img/Image00264.jpg)

![Image](img/Image00265.jpg)

* 现在，所有队列都已清空，除了 `Poll` 队列外，所有待处理任务都已结束。让我们看看 `Poll` 队列将如何执行这些任务。

* `Poll` 队列将任务分为两大类。

* 所有类似文件读取、`crypto` 和 `zLib` 的操作都通过线程池完成。

* 线程池是一组工作线程（与 `Node`默认模块提供的工作线程不同）。线程池的默认大小为 4，但你可以通过 `Node` 提供的 `UV_THREADPOOL_SIZE` 全局变量覆盖该值。我在线程池中画了 4 个小方块来表示线程。

* 一个线程可以执行一个任务，因此 4 个线程可以同时执行 4 个任务。

* 然而，正如我所说，文件读取、`crypto` 和 `zLib` 这类任务在设计上只在线程池中执行。因此，在我们的例子中，两个文件读取操作通过线程池完成，两个文件操作由两个独立的线程处理，而另外两个 `GET API` 调用通过其他机制（如 `Epoll`/`Kqueue`）完成（稍后会看到）。

![Image](img/Image00266.jpg)

* 如你所见，我们在两个线程中处理两个文件读取操作，当它们完成读取后，结果会返回给各自的回调。

![Image](img/Image00267.jpg)

![Image](img/Image00268.jpg)

* 让我们完成这两个已完成的读取操作的执行，并运行它们的回调（因为我们不会在等待 `API` 调用完成时阻塞 `Poll` 队列）。

![Image](img/Image00269.jpg)

![Image](img/Image00270.jpg)

* 很好，现在我们也完成了文件读取操作，但还有两个操作需要完成，即我们的两个 `API` 调用。因此，我们再次进入事件循环的下一次迭代。

![Image](img/Image00271.jpg)

* 现在，是时候了解 `epoll`/`Kqueue` 和 `Poll` 队列如何协同工作了。我将解释 `epoll`，而不是其他机制，因为所有其他机制几乎相同，唯一的区别在于它们基于不同的操作系统架构。

#### `epoll`（假设我们在 Linux 上）

* 它是一种自平衡的二叉树数据结构。

* 我们将任务附加到该数据结构的节点上，并循环遍历每个任务，直到某个超时时间。

* 假设有 10 个 `API` 请求同时到达正在运行的 `Node` 进程，它们实际上都会被交给 `epoll`。

* 在将所有请求交给 `epoll` 之前，请求会以非阻塞模式打开（这是 Linux 的一个特性，允许以非阻塞模式打开文件/处理请求，并等待它们完成，然后返回结果）。

* 现在，在我们的假设中，我们有 10 个并发请求，我们将以非阻塞模式打开它们，并将其 ID（称为文件描述符）存储在 `epoll` 中。每个 ID 都会关联事件（这里指我们的回调函数）。

* 通常，我们会在一段时间内循环遍历 `epoll`。假设 `epoll` 循环 2 秒，那么在这 2 秒内，10 个请求中有 4 个完成了。因此，结果会返回给 `epoll`，再从 `epoll` 返回到我们的 `Poll` 队列。

* 完成 4 个请求后，我们立即转到 `Check` 队列。

* 在事件循环的下一次迭代中，假设在我们的 `epoll` 中又完成了 3 个请求（记住，我们实际上每 2 秒循环一次 `epoll`，以检查后台工作是否完成）。这 3 个请求及其数据会返回给 `Poll` 队列。

* 在下一次迭代中，假设我们完成了所有剩余的 3 个请求，结果返回给 `Poll` 队列。

通过内核特性将请求置于非阻塞模式，并借助 `Epoll` 数据结构处理任务，能够在不阻塞主 `JavaScript`线程、不阻塞轮询队列以及不产生新线程的情况下，实现惊人的并发能力。这正是 `Node.js` 如此流行且令人惊叹的原因。

![Image](img/Image00272.jpg)

* 在我们的场景中，有两个 `GET API` 调用。我们将按照刚才讨论的方式通过 `epoll` 处理它们，并将结果返回给轮询队列。让我们完成剩余两个 `API` 调用的可视化展示。

![Image](img/Image00273.jpg)

![Image](img/Image00274.jpg)

![Image](img/Image00275.jpg)

现在，所有执行如上所述完成，所有队列变为空，因此程序将退出。朋友们，这就是 `Node` 实际工作的方式😎。你通过正确的思维模型学习了复杂的 `Node` 架构😁。

```
注意：这里我假设 file1.txt 的读取操作在 file2.txt 之前完成，同样第一个 `API` 调用在第二个 `API` 调用之前完成。两个文件读取操作中哪一个先完成取决于你的操作系统和处理器。API` 调用也是如此。
```

现在，让我们从 `Node` 的角度讨论一些令人困惑的概念，比如`多线程`、`工作线程` 和 `多进程`。

### 多进程

* 我们知道，当我们启动 `Node` 程序时，实际上启动了一个 `Node` 进程，其中包含 1 个 `v8` 实例、1 个 `libUV` 实现的事件循环实例。

* 现在，当我们使用 `child_process` 时，从父进程（即 `Node` 进程）中创建一个新的进程。我们可以在新进程中执行任何操作。

* 这里需要注意一点是，每个新创建的进程都拥有自己的 `v8` 实例和 1 个 `libUV` 实现的事件循环实例。

* 如果你是 `Node` 开发者，那么可能知道名为 `Cluster` 的模块，它主要用于创建多个 `Node` 进程，并且每个进程将被放置在处理器核心上！

![Image](img/Image00276.jpg)

### 工作线程

* `Node` 中一个独立的模块，允许你创建真正的线程，我们也可以在新线程中运行 `JavaScript` 代码。

* 每个线程将拥有自己的 `v8` 和 `libUV` 实例。

![Image](img/Image00277.jpg)

* 工作线程通过通道与父进程通信，不仅如此，我们还可以在不同线程之间传递数据。

* `Node` 中的线程概念与其他语言不同。正如我们所见，我们可以在单独线程中运行 密集型任务，但每个线程都有自己的 `v8` 和 `libUV` 实例。

* 因此，即使在 `Node` 中创建大量线程，我们也肯定会耗尽内存，或者使系统因资源密集而过载。

* 所以，最好在 `Node` 中为大型密集型任务使用工作线程。不要使用工作线程来服务 `API` 请求。

### 多进程 vs 工作线程

* 最好使用多进程在每个核心上服务。此外，在每个 `Node` 进程内部，我们将拥有足够的内存和存储空间以便累积 `API` 请求，随后通过 `epoll` 和线程池队列提供良好的并发能力。

* 工作线程用于执行 密集型任务，例如在单独线程中计算复杂的数学公式，并将结果返回给父线程（即我们的主进程）。

* 我们可以结合两者的优点：创建多个 `Node` 进程，并为每个进程中的 密集型任务使用工作线程。

### 工作线程 vs 线程池

* `Node` 线程池拥有工作线程（可以直接执行密集型任务），当我们执行文件 `I/O`、加密和 `zlib` 操作时，`libUV` 会自动使用这些线程。

* 工作线程（`Node` 提供的模块）由我们创建，易于维护且速度快，因为它们不需要 `v8` 和 `libUV` 实例，因为线程池已经提前知道要执行的任务。

* 工作线程消耗一些资源，因此我们不会创建太多（这里，我们不会像传统编程语言（如 Java）那样为每个客户端创建线程，因为那样做会使我们的系统更加消耗资源且不稳定）。

```
我希望以上信息已经澄清了关于 Node.js 的错误和误解。
```

### Node 模块系统

现在，在结束 Node 之旅之前，我想解释一下模块系统是如何工作的。JavaScript 在不同的环境中运行，我们默认没有可用的模块系统（忽略最近出现的 ES6+ 原生模块，稍后讨论）。

* 当 Node 开发时，他们需要找出某种方式为开发者提供模块化系统，因此他们创建了自己的模块系统，称为 `CommonJS`。让我们通过可视化来理解它是如何工作的。

* 在 `Node` 中，项目中的每个 `JavaScript` 文件都被视为一个 `模块`，这意味着它们不仅仅是文件中的普通 `JavaScript` 代码，而是有一些额外的包装和内容。

* Node 提供了一些全局变量，这些变量对所有模块可用。我们称它们为全局变量。其中两个变量是 `require()` 函数和 `module` 对象（注意，这里的文件 `module` 和全局关键字 `module` 是不同的东西）。

让我们可视化到目前所学的内容。

![Image](img/Image00278.jpg)

* 假设我们想要将其他文件（`file1.js` 和 `file2.js`）的一些内容添加到主文件（`main.js`）中。

* 如我之前所说，在运行 `Node` 进程时，我们默认有一些全局变量可用。因此，我们将使用其中一个变量来完成需求。

* `require()` 函数在每个文件（模块）中都可使用，这意味着我也可以在 `main.js` 中使用这个辅助函数。

* 但是 Node 会所有模块被另一个模块 `require` 之前，给它们添加一个叫做 `IIFE`（立即调用函数表达式）的东西。让我们看看。

![Image](img/Image00279.jpg)

* 正如我们所见，在 `file1.js` 中，我们有一个简单的 `greet()` 函数，它将被 `IIFE` 函数包裹，如图所示（当然，只有我们在另一个模块中 `require` `file1.js` 时才会这样）。

* 同样，我们的 `main.js`（主模块）也会被包裹。因为当我们启动 `Node` 进程时，我们将从主模块开始。

![Image](img/Image00280.jpg)

* 如果你注意到一点，包装器 `IIFE` 有一堆参数可用，其中之一是 `require`。让我们看看在主模块中使用 `require` 时会发生什么。

* `require()` 函数接受文件路径作为参数查找另一个模块。

![Image](img/Image00281.jpg)

* 如果你尝试运行上述代码，它将抛出一个“模块未找到”的错误。

![Image](img/Image00282.jpg)

* 但为什么呢？

* 我说我说每个模块都被 `IIFE` 包裹，所以当我们 `require` 一个模块时，我们实际上获取的是 `IIFE`，而不是模块的代码。让我们可视化它。

![Image](img/Image00283.jpg)

#### CommonJS 模块系统的工作原理

正如我们所看到的，蓝色内容实际上就是 `require()` 所做的事情。因此，它是一个包装函数，其中的所有变量和函数都是局部作用域。这就是为什么我们无法执行 `greet()` 函数并得到错误的原因。

但那么我们是如何让它工作的呢？

这就是我们让它工作的方式。

```


## 10. 下面的 `a` 数组中有一个元素，但长度仍然显示为 `0` 😂。

![Image](img/Image00290.jpg)

```
This is all my friends, I will keep updating this book with more content, till then enjoy learning and we will meet someday, sometime with some other book journey. Thank you for reading and happy Learning🥰.
```


# 初学者必备 JavaScript 与 jQuery 设计模式

## 简介

在本书开篇，我将重点讨论设计模式在任何编程语言中的重要性及其历史。如果你对此已有了解或熟悉这段历史，可以自由跳至“什么是模式？”章节继续阅读。

编写可维护代码最重要的方面之一，是能够识别代码中反复出现的主题并进行优化。在这个领域，掌握设计模式的知识可以证明是极具价值的。

设计模式可以追溯到一位名叫克里斯托弗·亚历山大的土木工程师的早期工作。他经常发表关于自己解决设计问题的经验以及这些经验如何与建筑和城镇相关的出版物。有一天，亚历山大突然意识到，某些设计构造在被反复使用时，能够带来理想的最优效果。

亚历山大与莎拉·石川和默里·西尔弗斯坦合作，创作了一种模式语言，旨在帮助任何希望在任何规模上进行设计和构建的人。这于1977年发表在一篇题为《模式语言》的论文中。

大约30年前，软件工程师开始将亚历山大所写的原则融入第一批关于设计模式的文献中，这旨在为希望提高编码技能的初级开发者提供指南。需要注意的是，设计模式背后的概念实际上可能自编程行业诞生之初就已存在，尽管形式上不那么正式。

在软件工程领域，最早且最具标志性的关于设计模式的正式著作之一，是1995年出版的《设计模式：可复用面向对象软件的基础》。该书由埃里希·伽玛、理查德·赫姆、拉尔夫·约翰逊和约翰·弗利西德斯合著——这个团队后来被称为“四人帮”（简称GoF）。

四人帮的出版物被认为对推动设计模式在我们领域的发展相当重要，因为它描述了大量开发技巧和陷阱，并提供了二十三种当今世界各地常用的核心面向对象设计模式。我们将在“设计模式的类别”部分更详细地介绍这些模式。

在本书中，我们将探讨一些流行的JavaScript设计模式，并探索为什么某些模式可能比其他模式更适合你的项目。请记住，模式不仅适用于原生JavaScript，也适用于jQuery或Dojo等抽象库。在我们开始之前，让我们先看看软件设计中“模式”的准确定义。

## 什么是模式？

模式是一种可复用的解决方案，可应用于软件设计中反复出现的问题——在我们特定的情况下，是指编写JavaScript应用程序。看待模式的另一种方式是将其视为你解决问题的模板——这些模板可用于多种不同情境。为了思考一个模式可能有多大用处，让我们设想一下，如果你编写一个脚本，其中写着“对每个项目发出警报”，如果发出警报本身很复杂，那么这样做总比说“为项目1执行此操作”、“为项目2执行此操作”、“对项目3再做一次同样的操作”更能得到可维护的代码，即，如果执行大部分工作的代码存在于更少的地方，维护起来就会显著容易得多。

你可能会问，为什么理解模式并熟悉它们很重要。设计模式主要有三个好处。

1. **模式是经过验证的解决方案：** 它们为解决软件开发中的问题提供了可靠的方法，这些方案反映了帮助定义和改进它们的开发者的经验和见解。
2. **模式可以轻松复用：** 模式通常反映了一个开箱即用的解决方案，可以根据自身需求进行调整。这一特性使其相当稳健。
3. **模式具有表现力：** 当你观察一个模式时，其呈现的解决方案通常具有一套固定的结构和“词汇”，可以帮助相当优雅地表达非常庞大的解决方案。

模式**并非**精确的解决方案。重要的是要记住，模式的作用仅仅是为我们提供一个解决方案框架。模式并不能解决所有设计问题，也不能取代优秀的软件设计师，然而，它们**确实**能支持设计师。接下来，我们将看看模式能为我们提供的一些其他优势。

- **复用模式有助于防止可能导致应用程序开发过程中出现重大问题的微小问题。** 这意味着，当你的代码更多地依赖经过验证的模式时，你可以花更少的时间担心代码架构，而花更多的时间专注于整体解决方案的质量。这是因为模式可以鼓励你以更结构化和有组织的方式编码，从而大大减少将来为整洁目的而重构它的需要。
- **模式可以提供通用的解决方案，其记录方式使它们不必与特定问题绑定。** 这种通用方法意味着，无论你使用何种应用程序（在许多情况下，甚至是编程语言），设计模式都可以应用于改进代码结构。
- **某些模式实际上可以通过避免重复来减少代码的整体文件大小占用。** 通过鼓励开发者更仔细地审视他们的解决方案，寻找可以立即减少重复的领域，例如，减少执行类似过程的函数数量，转而使用单个通用函数，可以减小代码库的整体规模。
- **经常使用的**模式可以随着时间的推移，通过利用其他使用这些模式的开发者回馈给设计模式社区的集体经验而得到改进。在某些情况下，这导致全新设计模式的创建，而在其他情况下，它可以导致提供关于如何最好地使用特定模式的改进指南。这可以确保基于模式的解决方案比临时解决方案更健壮。

## “模式”性测试、原型模式与三法则

请记住，并非每个算法、最佳实践或解决方案都代表一个完整的模式。这里可能缺少一些关键要素，而模式社区通常对声称是模式的东西持谨慎态度，除非它经过了严格的审查。即使某些东西*看起来*符合模式的标准，在它经过其他人适当的审查和测试之前，也不应被视为模式。

再次回顾亚历山大的工作，他声称一个模式应该既是一个过程又是一个“事物”。这个定义故意有些晦涩，因为他接着说这个过程应该创造出那个“事物”。这就是为什么模式通常专注于解决一个视觉上可识别的结构的原因，即你应该能够视觉化地描绘（或绘制）一幅代表将模式付诸实践所产生的结构的图画。

在学习设计模式时，你可能会经常遇到“原型模式”这个术语。这是什么？嗯，一个尚未通过“模式”性测试的模式通常被称为原型模式。原型模式可能源于某人的工作，他们确定某个特定的解决方案值得与社区分享，但由于其非常年轻，可能还没有机会经过严格的审查。

或者，分享模式的个人可能没有时间或兴趣去经历“模式”性过程，而是可能发布他们原型模式的简要描述。这种模式的简要描述被称为模式片段。

完整记录一个合格模式所涉及的工作可能相当艰巨。回顾设计模式领域最早的一些工作，一个模式如果做到以下几点，就可能被认为是“好的”：

- **解决特定问题** - 模式不应仅仅捕捉原则或策略，它们需要捕捉解决方案。这是好模式最基本的要求之一。
- **该问题的解决方案不能是显而易见的** - 你通常会发现，问题解决技巧试图从众所周知的基本原理推导出来。最好的设计模式通常间接提供问题的解决方案——这是处理最具挑战性的设计问题时的一种必要方法。
- **描述的概念必须经过验证** - 设计模式需要证明其能如所述那样发挥作用，如果没有这个证明，该设计就不能被认真考虑。如果一个模式本质上是高度推测性的，那么可能只有勇敢的人才会尝试使用它。
- **必须描述一种关系** - 在某些情况下，一个模式可能看似描述了一种模块类型。尽管实现可能看起来如此，但模式的官方描述必须描述更深层的系统结构和机制，以解释其与代码的关系。

如果你认为一个不符合完整模式准则的原始模式不值得研究，这无可厚非，但事实远非如此。许多原始模式实际上相当不错。我并不是说所有原始模式都值得一看，但确实存在相当多有用的模式，它们可能在未来项目中对你有所帮助。在选择过程中，请参考上述列表并运用最佳判断力，你将不会出错。

一个模式要生效，另一个额外要求是它必须展示一些反复出现的现象。这通常可以通过至少三个关键领域来界定，称为*三的法则*。要使用此法则展示重现性，必须证明：

1. **目的适用性** - 该模式如何被视为成功？
2. **有用性** - 该模式为何被视为成功？
3. **可应用性** - 该设计是否因其更广泛的可适用性而值得成为一个模式？如果是，这需要解释。在审查或定义模式时，牢记上述几点很重要。

## 设计模式的结构

在研究设计模式时，你可能想知道创建模式的团队必须在其设计模式描述中包含什么内容。每个模式最初都必须以**规则**的形式制定，该规则在**上下文**、该上下文中出现的**力量**系统以及允许这些力量在上下文中自行解决的**配置**之间建立关系。

我发现，关于好模式结构的大量现有信息可以浓缩成更易于消化的内容。考虑到这一点，现在让我们看看下面设计模式的组件要素摘要。

**一个设计模式必须包含：**

- **模式名称**和**描述**
- **上下文概述** – 模式在响应用户需求时有效的上下文。
- **问题陈述** – 陈述所解决的问题，以便我们理解模式的意图。
- **解决方案** – 描述如何通过一系列易于理解的步骤和观念来解决用户的问题。
- **设计** – 描述模式的设计，特别是用户与其交互的行为。
- **实现** – 模式如何实现的指南。
- **插图** – 模式中类的视觉表示（例如图表）。
- **示例** – 模式的最小形式实现。
- **共同要求** – 支持所描述模式的使用可能需要哪些其他模式？
- **关系** – 这个模式类似于哪些模式？它是否与任何其他模式非常相似？
- **已知用法** – 该模式是否在“野外”使用？如果是，在哪里以及如何使用？
- **讨论** – 团队或作者对模式令人兴奋的好处的看法。

设计模式是一种相当强大的方法，可以在组织或团队创建或维护解决方案时，让所有开发人员保持一致。如果你或你的公司曾考虑开发自己的模式，请记住，尽管在规划和撰写阶段可能有很高的初始成本，但这项投资的回报可能是相当值得的。然而，在开发新模式之前，务必彻底研究，因为你可能会发现，使用或在现有的、经过验证的模式基础上构建，比从头开始更有益。

## 撰写设计模式

尽管本书面向设计模式的新手，但理解设计模式的撰写方式可以为你提供许多有用的优势。首先，你可以更深入地理解模式存在的原因，同时也能在审查模式（或原始模式）是否符合自身需求时学会如何判断。

撰写好的模式是一项具有挑战性的任务。模式不仅需要为最终用户提供大量的参考资料（例如上面*结构*部分中找到的项目），还需要能够近乎“讲述”一个故事，描述它们试图传达的经验。如果你已经阅读了前面关于模式“是什么”的部分，你可能会认为这本身应该能帮助你识别野外的模式。事实恰恰相反——你并不总是能判断你检查的代码是否遵循模式。

在查看你认为可能使用了某个模式的代码主体时，你可能会写下你认为属于某个特定现有模式的代码方面，但它可能根本不是模式。在许多模式分析的情况下，你会发现你只是在查看遵循良好原则和设计实践的代码，而这些原则和实践可能只是偶然与模式的规则重叠。请记住——没有出现交互或定义规则的解决方案不是模式。

如果你有兴趣尝试撰写自己的设计模式，我建议你向那些已经经历过并做得很好的人学习。花时间吸收来自许多不同设计模式描述和书籍的信息，并吸收对你有意义的内容——这将帮助你实现设计想要达到的模式的目标。你可能还希望研究现有模式的结构和语义——这可以通过检查你感兴趣的模式的交互和上下文来开始，以便你可以识别有助于将这些模式组织成有用配置的原则。

一旦你接触了大量关于模式文献的信息，你可能希望使用*现有的*格式开始你的模式，并看看你是否能为改进它或整合你的想法进行头脑风暴。最近这样做的一个例子是 JavaScript 开发者 Christian Heilmann，他采用了一个名为*模块*模式的现有模式，并对其进行了根本性的有用更改，创建了*揭示模块*模式（这是本书后面涵盖的模式之一）。

如果你想尝试撰写设计模式（即使只是为了体验整个过程的学习经验），我有以下建议：

- **牢记实用性**：确保你的模式描述的是针对反复出现问题的、经过验证的解决方案，而不仅仅是未经验证的推测性解决方案。
- **确保借鉴最佳实践**：你的设计决策应基于你从理解最佳实践中得出的原则。
- **你的设计模式应对用户透明**：设计模式应完全对任何类型的用户体验透明。它们主要是为了服务于使用它们的开发人员，不应强加使用模式时不会发生的用户体验行为变化。
- **请记住，原创性在模式设计中*并非*关键**：撰写模式时，你不需要是所记录解决方案的原始发现者，也不必担心你的设计与其他模式的小部分重叠。如果你的设计足够强大，具有广泛的有用适用性，它就有机会被认可为一个合适的模式。
- **了解模式与设计之间的区别**：设计模式通常借鉴经过验证的最佳实践，并作为设计师创建解决方案的模型。*模式的作用是指导设计师做出最佳设计选择，以便他们能够满足用户的需求。*
- **你的模式需要有一组强大的示例**：一个好的模式描述需要伴随同样强大的示例，以展示你的模式成功应用。为了展示广泛的用途，体现良好设计原则的示例是理想的。

模式撰写是在创建具有普适性、具体性且最重要的是有用的模式之间取得精心平衡。尝试确保在撰写模式时，你涵盖尽可能广泛的应用领域，这样你就会顺利。我希望这个关于撰写模式的简要介绍能给你一些见解，这将帮助你在本书后续章节的学习过程中。

## 反模式

如果我们认为模式代表最佳实践，那么反模式则代表一个吸取的教训。反模式一词由 Andrew Koenig 于 1995 年在当年 11 月的《C++ 报告》中首创。它受到四人组的《设计模式》一书的启发，该书发展了软件领域的设计模式概念。在 Koenig 的报告中，提出了两种反模式的概念。反模式：

- 描述了对特定问题的*糟糕*解决方案，导致了糟糕情况的发生。
- 描述*如何*摆脱上述情况以及如何从那里转向好的解决方案。

关于这个话题，亚历山大在探讨如何在良好设计结构与良好上下文之间实现良好平衡的难点时写道：

> "这些笔记是关于设计过程的；是关于发明那些为响应功能而展现新物理秩序、组织和形式的实体事物的过程……每个设计问题都始于努力在两个实体之间实现适配：所讨论的形式及其上下文。形式是问题的解决方案；上下文定义了问题。"

虽然了解设计模式非常重要，但理解反模式可能同样重要。让我们来阐述其背后的原因。当创建一个应用程序时，项目的生命周期从构建开始，然而一旦你完成了初始版本发布，它就需要被维护。最终解决方案的质量将是*好或坏*，这取决于团队在其中投入的技能水平和时间。这里的*好*和*坏*是相对于上下文而言的——如果应用于错误的上下文，一个“完美”的设计可能算得上是反模式。

更大的挑战发生在应用程序进入生产环境并准备进入维护模式之后。一个之前未接触过该应用程序的开发人员在此类系统上工作时，可能会无意中在项目中引入*糟糕的*设计。如果这些*糟糕的*实践被创建为反模式，它们就为开发人员提供了一种预先识别这些模式的方法，从而避免可能发生的常见错误——这与设计模式为我们提供识别*有用*常见技术的方法是类似的。

总而言之，反模式是值得记录的糟糕设计。JavaScript 中的反模式示例如下：

- 通过在全局上下文中定义大量变量来污染命名空间。
- 向 `setTimeout` 或 `setInterval` 传递字符串而不是函数，因为这会在内部触发使用 `eval()`。
- 针对 `Object` 对象进行原型设计（这是一个特别糟糕的反模式）。
- 以内联形式使用 JavaScript，因为这不灵活。
- 使用 `document.write`，而更合适的是使用原生 DOM 替代方案，如 `document.createElement`。多年来，`document.write` 被严重滥用，且有很多缺点，包括如果它在页面加载后执行，实际上会覆盖你所在的页面，而 `document.createElement` 则不会。你可以在[这里](https://example.com)看到一个实际示例。它也不适用于 XHTML，这是选择使用更兼容 DOM 的方法（如 `document.createElement`）的另一个原因。

了解反模式对于成功至关重要。一旦你能够识别此类反模式，你就能够重构代码以消除它们，从而立即时你解决方案的整体质量得到提升。

## 设计模式分类

一本知名的设计书籍《领域驱动术语》中的一段术语表正确地指出：

> "设计模式命名、抽象并识别了一个通用设计结构的关键方面，使其对于创建可复用的面向对象设计非常有用。设计模式识别了参与的类及其实例、它们的角色和协作关系，以及职责的分配。
>
> 每个设计模式都专注于一个特定的面向对象设计问题或议题。它描述了其适用场景，是否可以在其他设计约束条件下应用，以及使用它的后果和权衡。由于我们最终必须实现我们的设计，设计模式还提供了示例……代码来说明一个实现。
>
> 尽管设计模式描述的是面向对象设计，但它们是基于在主流面向对象编程语言中已实施的实用解决方案……"

设计模式可以细分为多个不同的类别。在本节中，我们将回顾其中三个类别，并简要提及属于这些类别的几个模式示例，然后再更详细地探讨具体的模式。

### 创建型设计模式

创建型设计模式专注于处理对象创建机制，即以适合当前工作情况的方式创建对象。否则，对象的基本创建方法可能会在项目中增加复杂性，而创建型模式旨在通过*控制*此类对象的创建来解决这个问题。

属于此类别的部分模式有：工厂模式、抽象工厂模式、原型模式、单例模式和建造者模式。

### 结构型设计模式

结构型模式专注于类和对象的组合。结构型“类”创建模式使用继承来组合接口，而“对象”模式则定义创建对象的方法以获得新功能。

属于此类别的模式包括：装饰器模式、外观模式、组合模式、适配器模式和桥接模式。

### 行为型设计模式

此类模式的主要关注点是类的对象之间的通信。通过专门针对这个问题，这些模式能够提高执行这种通信的灵活性。

一些行为型模式包括：迭代器模式、中介者模式、观察者模式和访问者模式。

## 设计模式分类总结表

在我早期学习设计模式的经历中，我个人发现以下表格非常有用，它提醒了我许多模式所具有的功能——它涵盖了 GoF 提到的 23 种设计模式。原始表格由 Elyse Nielsen 在 2004 年总结，我已根据本书本节的讨论需要进行了必要的修改。

我建议使用此表格作为参考，但请记住，还有一些额外的模式未在此表中提及，但将在本书后面讨论。尽管如此，它是一个很好的学习起点。

| | |
|---|---|
| **创建型** | 基于创建对象的概念。 |
| **类** | |
| *工厂方法* | 根据接口数据或事件创建几个派生类的实例。 |
| **对象** | |
| *抽象工厂* | 创建几个族类的实例，而不指定具体类。 |
| *建造者* | 将对象构造与其表示分离，总是创建相同类型的对象。 |
| *原型* | 一个完全初始化的实例，用于复制或克隆。 |
| *单例* | 一个只有一个实例的类，具有全局访问点。 |
| | |
|---|---|
| **结构型** | 基于构建块（对象）的思想。 |
| **类** | |
| *适配器* | 匹配不同类的接口，因此即使接口不兼容，类也可以协同工作 |
| **对象** | |



| 适配器 | 匹配不同类的接口，因此即使接口不兼容，类也可以协同工作 |
|---|---|
| 桥接 | 将对象的接口与其实现分离，因此两者可以独立变化 |
| 组合 | 简单和复合对象的结构，使总对象不仅仅是其部分的总和。 |
| 装饰器 | 动态地为对象添加替代处理。 |
| 外观 | 一个隐藏整个子系统复杂性的单一类。 |
| 享元 | 一个细粒度的实例，用于高效共享包含在其他地方的信息。 |
| 代理 | 代表真实对象的占位符对象。 |

| 行为型 | 基于对象相互作用和协作的方式。 |
|---|---|
| 类 | |
| 解释器 | 一种在应用程序中包含语言元素以匹配目标语言语法的方式。 |
| 模板方法 | 在一个方法中创建算法的骨架，然后将确切步骤推迟到子类。 |

| 对象 | |
|---|---|
| 模式 | 描述 |
|:---|:---|
| 责任链 | 一种在对象链中传递请求的方式，以找到可以处理该请求的对象。 |
| 命令 | 将命令请求封装为一个对象，以实现请求的记录和/或排队，并为未处理的请求提供错误处理。 |
| 迭代器 | 在不知道集合内部工作原理的情况下，顺序访问集合中的元素。 |
| 中介者 | 定义类之间的简化通信，以防止一组类相互显式引用。 |
| 备忘录 | 捕获对象的内部状态，以便以后能够恢复它。 |
| 观察者 | 一种通知多个类有关更改的方式，以确保类之间的一致性。 |
| 状态 | 在对象状态改变时改变其行为。 |
| 策略 | 将算法封装在一个类中，将选择与实现分离。 |
| 访问者 | 在不改变类的情况下向类添加新操作。 |

## JavaScript 中的设计模式

接下来，我们将探讨 10 种流行的设计模式，我个人发现这些模式在多年 JavaScript 应用程序开发中非常有用。

请注意，这个选择中没有“理想”的模式可以使用，因为开发人员在决定哪种模式最“适合”他们的需求时，通常会运用最佳判断。

每种模式的复杂程度各不相同，然而我已尽力使我的解释尽可能简单，以便初学者和中级开发人员都能从材料中受益。

## 我们将探讨的模式

- 创建型模式
- 构造器模式
- 单例模式
- 模块模式
- 揭示模块模式
- 原型模式
- DRY 模式
- 外观模式
- 工厂模式
- 装饰器模式

### 创建型模式

这个模式是本文中许多其他模式的基础，实际上理解起来相当直接。正如你可能猜到的，在 JavaScript 中，创建型模式处理的是在应用程序内创建对象。最常见的做法如下：

```javascript
var newObject = new MyClass();
```

很多时候，你没有理由以其他方式来处理这件事。你只需定义你的类，然后在需要时实例化它。然而，有些情况下，这种方式既非优势，也非所需特性。

#### 构造器模式

“构造器”这个短语对大多数开发者来说都很熟悉，不过如果你是初学者，在深入探讨专门针对它的模式之前，回顾一下构造器是什么会很有用。构造器用于创建特定类型的对象。这种范式可以在许多编程语言中找到，包括 JavaScript。你可能熟悉的一些原生构造器包括 `Object` 和 `Array`。

你也可以定义自定义构造器，为你自己的对象类型定义属性和方法。

让我们来看一个汽车的构造器。

```javascript
function Car(model, year, miles){
    this.model = model;
    this.year   = year;
    this.miles  = miles;
    this.whatCar = function(){
        console.log(this.model);
    };
}
```

```javascript
var civic = new Car("Honda Civic", 2009, 20000);
var mondeo = new Car("Ford Mondeo", 2010, 5000);
```

旁注：[Douglas Crockford](https://www.crockford.com/) 建议将你的构造器函数首字母大写，以便更容易区分它们与普通函数。

#### 单例模式

从核心上讲，单例模式可以通过创建一个类来实现，该类包含一个方法，如果该类的实例不存在，则创建一个新实例。

如果实例已经存在，它只需返回对该对象的引用。因此，单例模式之所以被称为单例，是因为传统上，它将类的实例化限制为单个对象。

单例并不提供一种方式，让不知道单例先前引用的代码轻松获取它——单例返回的不是对象或类，而是一种结构。

想想闭包变量实际上并非闭包——提供闭包的函数作用域才是闭包。

那么，单例模式在何处有用呢？当系统中恰好需要一个对象来协调模式时，它相当有用。下面是使用单例模式的一个例子：

```javascript
var SingletonTester = (function(){
    //args: an object containing arguments for the singleton
    function Singleton(args) {

        //set args variable to args passed or empty object if none provided.
        var args = args || {};
        //set the name parameter
        this.name = 'SingletonTester';
        //set the value of pointX
        this.pointX = args.pointX || 6; //get parameter from arguments or set default
        //set the value of pointY
        this.pointY = args.pointY || 10;

    }

    //this is our instance holder
    var instance;

    //this is an emulation of static variables and methods
    var _static = {
        name: 'SingletonTester',
        //This is a method for getting an instance
        //It returns a singleton instance of a singleton object
        getInstance: function (args){
            if (instance === undefined) {
                instance = new Singleton(args);
            }
            return instance;
        }
    };
    return _static;
})();

var singletonTest = SingletonTester.getInstance({pointX: 5});
console.log(singletonTest.pointX); // outputs 5
```

#### 模块模式

现在让我们来看看流行的模块模式。模块模式被定义为一种为 JavaScript “类”概念提供私有和公共封装的方式。它们的工作前提是“类”实际上被定义为一个函数（为简单起见，我们称之为类）。

你为这个类决定使用的参数实际上是构造器的参数。在类内部定义的局部变量和函数都成为私有成员。类的返回方法（即仍然是一个函数）返回一个包含你的公共方法和变量的对象。

一个有趣的事实是，模块模式最初是由 Douglas Crockford 正式定义的（他以《JavaScript: The Good Parts》一书等闻名），尽管这种模式的变体很可能在此之前很久就已被使用。另一个有趣的事实是，如果你曾使用过 Yahoo 的 YUI 库，它的某些功能可能看起来相当熟悉，原因在于模块模式对 YUI 创建其组件时产生了重大影响。

那么，你已经看到了单例模式为何有用，但为什么模块模式是一个好选择呢？

首先，对于有面向对象背景的开发者来说，它比真正的封装概念要清晰得多，至少从 JavaScript 的角度来看是如此。其次，它支持私有数据——因此，在模块模式中，代码的公共部分能够访问私有部分，然而外部世界无法访问类的私有部分（别笑！哦，感谢 David Engfer 的这个笑话）。

模块模式的缺点在于，由于你以不同方式访问公共和私有成员，当你希望更改可见性时，你实际上必须对每个使用该成员的地方进行更改。

你也不能在稍后添加到对象的方法中访问私有成员。话虽如此，在许多情况下，模块模式仍然非常有用，并且如果使用得当，确实有可能改善应用程序的结构。

```javascript
var someModule = (function(){

    //private attributes
    var privateVar = 5;

    //private methods
    var privateMethod = function(){
        return 'Private Test';
    };

    return {
        //public attributes
        publicVar    : 10,
        //public methods
        publicMethod : function(){
            return ' Followed By Public Test ';
        },

        //let's access the private members
        getData : function(){
            return privateMethod() + this.publicMethod() + privateVar;
        }
    }
})(); //the parens here cause the anonymous function to execute and return

someModule.getData();
```

#### 揭示模块模式

现在你可能对模块模式是什么更加熟悉了。让我们来看一个稍微改进的版本——Christian Heilmann 的揭示模块模式，它通常被描述为一个相当稳健的模式的巧妙扩展。揭示模块模式的出现是因为 Heilmann（现在在 Mozilla）对这样一个事实感到沮丧：当你想从一个公共方法调用另一个公共方法或访问公共变量时，你必须重复主对象的名称。

他也不喜欢模块模式的要求，即必须切换到对象字面量表示法来处理你希望公开的内容。他努力的结果是一个更新的模式，在这个模式中，你只需在私有作用域中定义所有的函数和变量，并在模块末尾返回一个匿名对象以及指向你希望公开的私有变量和函数的指针。

再一次，你可能想知道这种方法的好处是什么。RMP 允许你的脚本语法保持相当一致——它也在末尾非常清楚地指出了你的哪些函数和变量可以被公共访问，这相当有用。此外，如果你愿意，你还可以用更具体的名称来揭示私有函数。

下面是使用揭示模块模式的一个例子：

```javascript
/*
 The idea here is that you have private methods
 which you want to expose as public methods.

 What we are doing below is effectively defining
 a self-executing function and immediately returning
 the object.
 */
var myRevealingModule = function(){

    var name = 'John Smith';
    var age = 40;

    function updatePerson(){
        name = 'John Smith Updated';
    }
    function setPerson () {
        name = 'John Smith Set';
    }
    function getPerson () {
        return name;
    }
    return{
        set: setPerson,
        get: getPerson
    }
}();

// Sample usage:
myRevealingModule.get();
```

### 原型模式

原型模式基于原型继承的概念，我们创建对象并使其作为其他对象的原型。原型对象本身实际上被用作构造函数创建的每个对象的蓝图。如果使用的构造函数的原型包含一个名为 `name` 的属性（如下面的代码示例所示），那么由同一构造函数创建的每个对象也将具有相同的属性。

查看现有文献（非 JavaScript 特定）中关于原型模式的定义，你可能会找到一些超出该语言范围的概念引用，例如类。现实是，原型继承完全避免了使用类。理论上，不存在“定义”对象或核心对象。我们只是创建现有功能对象的副本。

使用原型模式的核心优势之一在于，我们利用 JavaScript 原生提供的优势，而不是试图模仿其他语言的特性（某些设计模式的实现会这样做）。

这不仅是一种实现继承的简便方法，还能带来性能提升。在对象中定义函数时，它们都是通过引用创建的（因此所有子对象指向同一个函数），而不是创建各自的独立副本。

对于感兴趣的人来说，如 ECMAScript 5 标准中定义的真正原型继承，需要使用 `Object.create`，这是一个相对较新的原生方法。`Object.create` 创建一个具有指定原型的对象，该对象可包含指定的属性（即 `Object.create(prototype, optionalDescriptorObjects)`）。

我们也可以在下面的示例中看到这一点：

```javascript
// 无需大写，因为它不是构造函数
var someCar = {
  drive: function() {};
  name: 'Mazda 3'
};

// 使用 Object.create 生成一辆新车
var anotherCar = Object.create(someCar);
anotherCar.name = 'Toyota Camry';
```

### DRY 原则

**免责声明：**DRY 本质上是一种思维方式，许多模式旨在通过其设计达到一定程度的 DRY。在本节中，我们将探讨代码的 DRY 含义，同时也将介绍基于相同概念的 DRY 设计模式。

开发大型应用程序时，开发者经常面临的挑战之一是多次编写相似的代码。有时这发生是因为你的脚本或应用程序可能有多种类似的方式来执行某项操作。

重复编写代码通常会降低生产力，并使你不得不重写之前已经编写过的类似代码，从而减少你添加新功能的时间。

DRY（Don't Repeat Yourself，不要重复自己）的创建正是为了简化这一点——它基于这样一种理念：你的代码的每个部分理想情况下只应包含系统相关知识的每种表示一次。

这里要掌握的关键概念是，如果你有一段执行特定任务的代码，你不应该在你的应用程序或脚本中多次编写该代码。

当 DRY 成功应用时，修改系统中的任何元素不会改变其他逻辑上不相关的元素。你代码中逻辑相关的元素会统一改变，从而保持同步。

由于前面介绍的其他模式展示了 JavaScript 中 DRY 的方面，让我们看看如何使用 jQuery 编写 DRY 代码。请注意，在使用 jQuery 的地方，你可以轻松地使用原生 JavaScript 替换选择器，因为 jQuery 在抽象层面上就是 JavaScript。

### 非 DRY

```javascript
/*让我们在数组中存储一些默认值*/
var defaultSettings = {};
defaultSettings['carModel']     = 'Mercedes';
defaultSettings['carYear']      = 2010;
defaultSettings['carMiles']     = 5000;
defaultSettings['carTint']      = 'Metallic Blue';
```

如果一个复选框被点击，我们来处理这些数据：

```javascript
$('.someCheckbox').click(function(){

    if (this.checked)
    {
            $('#input_carModel').val(activeSettings.carModel);
            $('#input_carYear').val(activeSettings.carYear);
            $('#input_carMiles').val(activeSettings.carMiles);
            $('#carTint').val(activeSettings.carTint);

    } else {

            $('#input_carModel').val('');
            $('#input_carYear').val('');
            $('#input_carMiles').val('');
            $('#input_carTint').val('');

    }
});
```

### DRY



```javascript
$('.someCheckbox').click(function(){
    var checked = this.checked;
    /*
       我们在重复什么？
       1. input_ 前缀每个字段名
       2. 访问同一个设置数组
       3. 重复重置值

       我们能做什么？
       1. 以编程方式生成字段名
       2. 通过键访问数组
       3. 使用简洁的代码合并此调用（即如果checked，
              设置一个值，否则不设置）
    */
        $.each(['carModel', 'carYear', 'carMiles', 'carTint'], function(i,key){
                $('#input_' + key).val(checked ? defaultSettings[key] : '');
        });
});
```

### 外观模式

此模式既简化了类的接口，也将类与其使用的代码解耦。外观模式通常被认为是开发者模式工具包中的重要组成部分——它们可以通过创建便捷的例程来简化复杂系统的使用，从而使库工具更容易理解。

外观模式的一个例子是在创建统一的 JavaScript API 中常见，这些 API 通常旨在所有浏览器中提供一致的体验。外观模式为我们提供了一种间接与子系统交互的能力，这种方式可能比直接访问子系统更不容易出错。

外观模式的优点包括易于使用，并且通常在实现时占用较小的内存空间。然而，它也有一些陷阱——当连续使用外观模式时效率较低，并且每次调用都必须进行新的检查以确定可用于附加事件监听器的功能。让我们来看看该模式的实际应用：

这是一个未经优化的代码示例，但在这里我们利用外观模式来简化附加事件的接口。

我们通过创建一个通用方法来实现这一点，该方法可以在代码中使用，用于检查功能的存在，从而提供安全且跨浏览器兼容的解决方案。

```javascript
var addMyEvent = function(el,ev,fn){

    if(el.addEventListener){
        el.addEventListener(ev,fn, false);
    }else if(el.attachEvent){
        el.attachEvent('on'+ev, fn);
    } else{
        el['on' + ev] = fn;
    }

};
```

### 工厂模式

与其他创建型模式类似，工厂模式处理创建对象（我们可以将其视为“工厂产品”）的问题，而无需指定要创建的对象的确切类。

具体来说，工厂模式建议定义一个创建对象的接口，其中允许子类决定实例化哪个类。此模式通过定义一个完全独立的方法来处理对象的创建，子类可以覆盖该方法，从而指定将要创建的“工厂产品”的“类型”。

这在创建过程相当复杂时尤其有用，例如，它强烈依赖于配置文件中的设置。你经常可以在框架中找到工厂方法，其中库的代码可能需要创建特定类型的对象，这些对象可能由使用框架的脚本进行子类化。

在我们的示例中，让我们使用原始构造函数模式示例中的代码，看看如果使用工厂模式进行优化会是什么样子：

```javascript
var Car = (function() {
    var Car = function (model, year, miles){
        this.model = model;
        this.year   = year;
        this.miles = miles;
    };
    return function (model, year, miles) {
        return new Car(model, year, miles);
    }
})();

var civic = new Car("Honda Civic", 2009, 20000);
var mondeo = new Car("Ford Mondeo", 2010, 5000);
```

### 装饰器模式

装饰器模式是创建子类的替代方案。此模式可用于将对象包装在另一个具有相同接口的对象中，允许你既向方法添加行为，又将方法调用传递给原始对象（即装饰器的构造函数）。

装饰器模式用于需要在已重写方法上不断添加新功能时。这可以通过将多个装饰器堆叠在一起来实现。

使用装饰器模式的主要好处是什么？如果我们仔细查看第一个定义，我提到装饰器是子类化的一种替代方案。当脚本运行时，子类化会添加影响原始类所有实例的行为，而装饰则不会。

相反，它可以为单个对象添加新行为，这在特定应用中可能是有益的。

让我们来看一些实现装饰器模式的代码：

```javascript
//The class we're going to decorate
function Macbook(){
	this.cost = function(){
		return 1000;
	};
}

function Memory(macbook){
	this.cost = function(){
		return macbook Gen Zil macbook.cost() + 75;
	};
}

function BlurayDrive(macbook){
	this.cost = function(){
		return macbook.cost() + 300;
	};
}

function Insurance(macbook){
	this.cost = function(){
		return macbook.cost() + 250;
	};
}

// Sample usage
var myMacbook = new Insurance(new BlurayDrive(new Memory(new Macbook())));
console.log( myMacbook.cost() );
```

## jQuery 中的设计模式

现在我们已经了解了流行设计模式的普通 JavaScript 实现，让我们转换思路，看看这些设计模式在使用 jQuery 实现时可能是什么样子。jQuery（如你所知）目前是最流行的 JavaScript 库，它在普通 JavaScript 之上提供了一层“语法糖”，其语法可以更容易一眼理解。

在我们深入本节之前，重要的是要记住，许多普通 JavaScript 设计模式可以与 jQuery 混合使用，因为 jQuery 本质上仍然是 JavaScript。

jQuery 是一个在模式领域中很有趣的讨论话题，因为该库本身实际上使用了 numerous 设计模式。让我印象深刻的是，它所使用的所有模式都实现得非常干净，以至于它们和谐地共存。

让我们来看看其中一些模式是什么，以及它们是如何使用的。

### 延迟初始化

延迟初始化是一种设计模式，其策略是延迟任何昂贵的进程（例如对象的创建）直到第一次需要它们时。一个例子是 jQuery 中的 `.ready()` 函数，它只在 DOM 完全加载后才执行函数。

```javascript
$(document).ready(function(){
    $('#content').fadeIn();
});
```

### 组合模式

组合模式描述了一组可以以与单个对象实例相同方式处理的对象。实现此模式允许您以统一的方式处理单个对象和组合。在 jQuery 中，当我们访问或对单个 DOM 元素或一组 DOM 元素执行操作时，我们可以以统一的方式处理两者。这在下面的代码示例中得到证明：

```javascript
$('#someDiv').addClass('active'); // a single element
$('div').addClass('active');       // a collection of elements
```

### 包装器模式

包装器模式是一种将类的接口翻译成兼容接口的模式。包装器基本上允许通常由于其不兼容接口而无法一起工作的类协同运行。包装器将其接口的调用翻译成对原始接口的调用，实现这一目标所需的代码通常非常少。

```javascript
$('.container').css({
        opacity: .5 //apply opacity in modern browsers (eg. Chrome, FireFox) but use filter for IE
    });
```

### 外观模式

外观模式在 OOP（面向对象编程）中非常常用，其中外观是一个对象，它提供对更大段代码（例如类库）的更简化的接口。外观在 jQuery 库中随处可见，使方法更易于使用和理解，也更易读。以下是 jQuery `$.ajax()` 的外观：

```javascript
$.get();
$.post();
$.getJSON();
$.getScript();
```

### 观察者模式

观察者模式是指主体（对象）维护其依赖项的列表，这些依赖项被称为观察者，并在状态发生任何变化时自动通知它们。这通常通过调用它们的方法之一来完成。观察者模式可以被认为是 PubSub（发布/订阅模式）的一个子集。

```javascript
//Here jQuery makes use of its event system on top of DOM events
$('.button').click(function(){})
$('.button').trigger('click', function(){})
```

### 迭代器模式

迭代器模式是一种设计模式，其中迭代器（允许我们遍历集合中所有元素的对象）按顺序访问聚合对象的元素，而无需暴露其底层形式。

迭代器封装了特定迭代发生的内部结构——在 jQuery 的 `.each()` 迭代器的情况下，您实际上能够使用 `.each()` 背后的底层代码来遍历集合，而无需看到或理解在幕后提供此功能的代码。

```javascript
$.each(function(){});
$('.items').each(function(){});
```

一个有趣的附带说明是，jQuery 的 `each` 方法与 ECMAScript 5 的做法相反，但将来某个时候可能会改变。

### 策略模式

策略模式是一种模式，其中脚本可以在运行时选择特定算法。此模式的目的是能够提供一种清晰定义算法族、将每个算法封装为对象并使它们易于互换的方式。

可以说，这种模式提供的最大好处是它允许算法独立于使用它们的客户端而变化。一个例子是 jQuery 的 `toggle()` 允许您绑定两个或更多处理程序到匹配的元素，以便在交替点击时执行。

策略模式允许在函数内部使用独立于客户端的替代算法。

```javascript
$('#container').toggle(function(){}, function(){});
```

### 代理模式

代理模式——代理基本上是一个充当其他东西接口的类。代理可以充当几乎任何东西的接口：文件、资源、内存中的对象、难以复制的其他东西等。jQuery 的 `.proxy()` 函数接受一个函数作为输入，并返回一个新函数，该函数将始终具有特定的上下文。

这与提供接口作为代理模式的概念平行。

```javascript
$.proxy(function(){}, obj);
```

### 构建器模式

构建器模式的主要概念是抽象创建对象所涉及的步骤，以便这些步骤的不同实现能够构造对象的不同表示。

下面是 jQuery 如何利用此模式允许使用字符串定义构造您可能希望附加到文档主体的元素的示例。

```javascript
$('<div class="foo">bar</div>');
```

### 原型模式

原型模式用于您希望创建的对象由原型实例确定，该实例被克隆以产生新对象时。本质上，此模式用于避免以标准方式创建新对象，当此过程可能昂贵或过于复杂时。在以下扩展 `jQuery.fn` 对象以创建最小插件的代码示例中，底层原型代码使这成为可能：

```javascript
$.fn.plugin = function(){}
$('#container').plugin();
```

### 享元模式

享元模式是一种设计模式，其中一个对象试图通过与其他相似对象尽可能共享信息来最小化使用的内存量。这是一种在大量利用对象时使用简单重复表示可能使用量被视为不可接受的内存的方式。对象的状态通常有可共享的方面，这些方面通常存储在外部数据结构中，在需要时临时传递给享元对象，这是常见的做法。

```javascript
// The userConfig is shared here:
$.fn.plugin = function(userConfig){
    userConfig = $.extend({
        content: 'Hello user!'
    }, userConfig);
    return this.html(userConfig.content);
});
```

这里需要补充说明的是，JavaScript 中的原型继承使用了差分继承，在原型链中只定义对象一次，直到它们被覆盖。这有助于节省内存。

## 结论

以上就是这本关于 JavaScript 和 jQuery 设计模式世界的入门读物——希望你们觉得它有用。本书内容并非对该领域的全面深入探讨，但应为你们提供了足够的信息，以便在日常项目中开始使用所涵盖的设计模式。

设计模式使得复用成功的设计和架构变得更加容易。每个开发者都应该了解设计模式，这一点很重要，但了解如何以及何时使用它们同样至关重要。明智地实现正确的模式值得付出努力，但反之亦然。实现不当的模式对项目可能收效甚微。

还要记住，重要的不是你实现了多少模式，而是你选择如何去实现它们。例如，不要仅仅为了使用“某个”模式而选择它，而是试着理解特定模式所提供的优缺点，并根据其是否适合你的应用程序做出判断。

如果我进一步激发了你对这个领域的兴趣，并且你想了解更多关于设计模式的知识，那么有许多优秀的书籍可供选择，它们既涵盖通用的软件开发领域，也涉及特定的语言。

对于 JavaScript 开发者，我推荐查阅以下两本书：

1. Ross Harmes 和 Dustin Diaz 著的《Pro JavaScript Design Patterns》。

2. Stoyan Stefanov 著的《JavaScript Patterns》。

如果你已经吸收了我这本迷你书中的大部分信息，我想你会发现阅读这些书是你学习过程中合乎逻辑的下一步（当然，是在你自己尝试了一些模式示例之后）: )

感谢阅读《Essential JavaScript & jQuery Design Patterns》。欲获取更多关于 JavaScript、jQuery 和用户界面设计的免费学习材料，请访问我的官方网站 http://addyosmani.com 获取我最新的教育资源。

## 参考资料

1. Design Principles and Design Patterns - Robert C Martin http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf
2. Ralph Johnson - Special Issue of ACM On Patterns and Pattern Languages - http://www.cs.wustl.edu/~schmidt/CACM-editorial.html
3. Hillside Engineering Design Patterns Library - http://hillside.net/patterns/
4. Pro JavaScript Design Patterns - Ross Harmes and Dustin Diaz http://jsdesignpatterns.com/
5. Design Pattern Definitions - http://en.wikipedia.org/wiki/Design_Patterns
6. Patterns and Software Terminology http://www.cmcrossroads.com/bradapp/docs/patterns-intro.html
7. Reap the benefits of Design Patterns - Jeff Juday http://articles.techrepublic.com.com/5100-10878_11-5173591.html
8. JavaScript Design Patterns - Subramanyan Guhan http://www.slideshare.net/rmsguhan/javascript-design-patterns
9. What Are Design Patterns and Do I Need Them? - James Moaoriello http://www.developer.com/design/article.php/1474561
10. Software Design Patterns - Alex Barnett http://alexbarnett.net/blog/archive/2007/07/20/software-design-patterns.aspx
11. Evaluating Software Design Patterns - Gunni Rode http://www.rode.dk/thesis/
12. SourceMaking Design Patterns http://sourcemaking.com/design_patterns
13. The Singleton - Prototyp.ical http://prototyp.ical.ly/index.php/2007/03/01/javascript-design-patterns-1-the-singleton/
14. JavaScript Patterns - Stoyan Stefanov - http://www.slideshare.net/stoyan/javascript-patterns



- 15. Stack Overflow - Design Pattern Implementations in JavaScript (discussion) http://stackoverflow.com/questions/24642/what-are-some-examples-of-design-pattern-implementations-using-javascript

- 16. The Elements of a Design Pattern - Jared Spool http://www.uie.com/articles/elements_of_a_design_pattern/

- 17. Stack Overflow - Examples of Practical JS Design Patterns (discussion) http://stackoverflow.com/questions/3722820/examples-of-practical-javascript-object-oriented-design-patterns

- 18. Design Patterns in JavaScript Part 1 - Nicholas Zakas http://www.webreference.com/programming/javascript/ncz/column5/

- 19. Stack Overflow - Design Patterns in jQuery http://stackoverflow.com/questions/3631039/design-patterns-used-in-the-jquery-library

- 20. Classifying Design Patterns By AntiClue - Elyse Neilson http://www.anticlue.net/archives/000198.htm

- 21. Design Patterns, Pattern Languages and Frameworks - Douglas Schmidt http://www.cs.wustl.edu/~schmidt/patterns.html

- 22. Show Love To The Module Pattern - Christian Heilmann http://www.wait-till-i.com/2007/07/24/show-love-to-the-module-pattern/

- 23. JavaScript Design Patterns - Mike G. http://www.lovemikeg.com/2010/09/29/javascript-design-patterns/

- 24. Software Designs Made Simple - Anoop Mashudanan http://www.scribd.com/doc/16352479/Software-Design-Patterns-Made-Simple

- 25. JavaScript Design Patterns - Klaus Komenda http://www.klauskomenda.com/code/javascript-programming-patterns/

- 26. Design Patterns Explained - http://c2.com/cgi/wiki?DesignPatterns

- 27. Working with GoF's Design Patterns In JavaScript http://aspalliance.com/1782_Working_with_GoFs_Design_Patterns_in_JavaScript_Programming.all

- 28. Design Patterns by Gamma, Helm supplement http://exciton.cs.rice.edu/javaresources/DesignPatterns/

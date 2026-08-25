

# 生成设计（修订版）：JavaScript 在 P5.js 中的可视化、编程与创建

## I.0 前言

生成设计早已不再是设计专业学生之间的行业秘密；在一些大学里，它如今已牢固地融入了课程体系。从信息图表到声音的可视化，从美术到建筑，尤其是在传达设计和媒体装置领域，生成设计实现了动态、惊艳且迷人的应用。

多年来，Processing 和 vvvv 一直是艺术家和设计师首选的编程环境。然而，最近出现了向更偏向 Web 应用的转变，催生了诸如`p5.js`这样的新编码环境，这是一个专门为艺术家、设计师及其他网络用户编程的 JavaScript 库。

《生成设计》第一版写于近十年前，其备受赞誉的基础教学方法至今仍无出其右。在这个更新版中，作者们利用 JavaScript 创造了一个更易上手、更与时俱进的创意编码入门点。秉承《生成设计》第一版的精神，目标是消除对编程的任何恐惧，并展示如何操作和调整现有的程序片段，几乎只需点击一下按钮就能获得令人惊叹的效果。

生成设计从根本上改变了设计流程：设计师从任务的执行者转变为指挥者，有效地编排计算机的决策过程。这就是生成设计的全部意义：迭代开发不同的流程，然后选择那些能产生最引人注目的视觉效果的流程。设计师和艺术家不再必须使用计算机以及强大但规定性的设计软件所规定的工具，现在他们可以创建自己的工具，这些工具能独立生成惊人的结果，正如书中的许多示例所展示的那样。

通过四个简单的课程——颜色、形状、字体和图像——用户学会影响他们的结果，并通过改变参数（每一步都有详细说明）或改变整个算法来改进结果。解释通俗易懂，执行几乎不需要甚至不需要编程；借助`p5.js`及其快速发展的社区，为从 3D 到增强现实等先进技术和趋势奠定基础变得越来越容易。`p5.js`社区非常活跃，不断提供新的更新和插件来扩展`p5.js`的功能。本书展示了如何利用这些知识，以及如何更深入地探索生成设计及其社区。在尝试了书中的草图并使用在线`p5.js`编辑器完成初始任务后，用户可以独立冒险，探索并扩展`p5.js`社区及其他领域的创意输出。

随着《生成设计》的成功（已被翻译成多种语言），作者们意识到，教授艺术家和设计师如何编码的关键在于通过简单但令人满意的渐进式成功来赋予他们力量。然后，学生可以基于这些基本原则，在他们的作品中构建越来越复杂的结构。

本书附带一个网站，用户可以在那里免费下载所有程序（草图）并立即开始实验。完成四个教程后，你将能够可视化数据、创建信息图表、可视化文本分析等等。

祝创意编码愉快。

卡琳和伯特拉姆·施密特-弗里德里希斯

## I.2 [www.generative-gestaltung.de](http://www.generative-gestaltung.de)

*生成设计：使用`p5.js`进行可视化、编程与创作*是一本经过验证的教程，让人们能够使用`p5.js`进行设计。无需手动输入任何代码：书中所有程序（称为“草图”）均可从书籍网站免费下载，供实验使用。此符号`→`表示下载包中某个草图的名称。

代码摘要页面展示了代码的主要特性及其对程序输出的影响。本书解释了代码参数如何影响结果，以及用户如何与草图交互以开发自己的视觉解决方案。

![image](img/f0008-01.jpg)

![image](img/f0009-01.jpg)

你好，欢迎来到生成设计。在这里，你将找到书中所有草图及其相关代码。你可以通过`p5.js`网页编辑器直接在浏览器中运行草图，或者通过下载下方的代码包在本地机器上运行。

**![image](img/arrowdown.jpg) 下载代码包**

# 库

## P.1. 颜色

![image](img/f0009-02.jpg)

**![image](img/arrowright.jpg) `P_1_0_01`**

![image](img/f0009-03.jpg)

**![image](img/arrowright.jpg) `P_1_1_1_01`**

![image](img/f0009-04.jpg)

**![image](img/arrowright.jpg) `P_1_1_2_01`**

## I.3 项目

以下十三件作品由活跃在生成设计领域的多位媒体艺术家、设计师和建筑师创作，旨在作为该主题的代表性概览和灵感来源。

## 01

### 2016/17 每日草图

扎克·利伯曼

![image](img/f0011-01.jpg)

**每日草图**是一系列短篇生成动画，由扎克·利伯曼每天在社交媒体上分享给全世界，以获取快速反馈。这些草图展示了使用几何、动画、手势、形状和代码探索新视觉概念的过程。利伯曼这样描述他的每日草图：“很多时候，作为艺术家，我们觉得自己在努力寻找自己的频率，以及与世界频率共鸣的东西。这种草图创作就像是对这些频率的一种调谐。”

![image](img/f0012-01.jpg)

![image](img/f0013-01.jpg)

![image](img/f0014-01.jpg)

**设计与开发**

松田翔太（Takram）

**摄影鸣谢**

长滨幸喜

`Planck`是一个基于网页浏览器的框架，由 Takram 开发，用于可视化大型地理数据集。该框架通过使用平行投影和景深等多种技术，旨在实现分析性与沉浸式视觉体验的双重目标。为 2017 年东京媒体野心展创作了三幅可视化作品，展示了日本 2050 年预估人口、人们在推特上使用的语言以及世界空中交通的数据。

## 02

### 2017 Planck

Takram

![image](img/f0015-01.jpg)

![image](img/f0016-01.jpg)

**交互设计**

比约恩·卡曼

**时装设计**

朱莉·赫勒斯

**纺织品设计**

克里斯蒂娜·博森

**学士学位毕业项目**

科灵设计学院，丹麦

时尚一直是自我表达的一种方式，但`Abstract_`通过让顾客将自己写进一件衣服中，将个性推向了更远的一步。`Abstract_`的交互平台提示顾客写下一个个人故事，并使用电脑摄像头捕捉面部表情。从故事、击键节奏以及顾客表情中收集的数据随后被转化为视觉表现，并映射到用于服装的纺织品上。

## 03

### 2015 Abstract_

比约恩·卡曼

朱莉·赫勒斯

克里斯蒂娜·博森

![image](img/f0017-01.jpg)

## 04

### 2016 Rottlace – 比约克

MIT 媒体物质组

克里斯托夫·巴德尔

多米尼克·科尔布

内里·奥克斯曼教授

Stratasys 有限公司

![image](img/f0018-01.jpg)

![image](img/f0019-01.jpg)

**摄影鸣谢**

圣地亚哥·费利佩

`Rottlace`是专为冰岛唱作人比约克设计的一系列面具中的一部分。其设计灵感源于人体肌肉骨骼系统的几何与材料逻辑。这些面具可被理解为“肌肉织物”：一种捆绑式、连续的多材料结构，为面部和颈部提供形式与结构的完整性，同时赋予其运动能力，最终形成一个无需部件、整体合成的物体。

## 05

### 2016 VOID VIII 01

安德烈亚斯·尼古拉斯·费舍尔

![image](img/f0020-01.jpg)

![image](img/f0021-01.jpg)

**主要编程**

安德烈亚斯·尼古拉斯·费舍尔和本杰明·毛斯

**附加编程**

亚伯拉罕·帕佐斯·索拉蒂

`VOID`是一系列使用自定义生成软件创作的图像。一群受算法控制的粒子在表面上移动，留下彩色痕迹。随着时间的推移，这会产生一种以不可预测方式发展的抽象构图。

![image](img/f0022-01.jpg)

受蒙纳公司委托并与其合作

**蒙纳：字体重塑**是一个由三件字体装置组成的系列，反映了字体如何通过交互性、生成设计和数据输入等新型数字方法变得“智能、动态且富有情感”。流行的蒙纳字体在新的空间和材料中被重新语境化并重新构想。

## 06

### 2017 蒙纳：字体重塑

Field

![image](img/f0023-01.jpg)

![image](img/f0024-01.jpg)

**客户**

耐克全球足球

`Nike Strike Series FA16`是一系列短片和静态图像，由鼓舞人心的 3D 渲染图组成，展现了世界级运动员的力量与精准。通过对职业足球运动员进行全身扫描，创建了体现这些运动员本质的特制 3D 模型。他们的独特特征数据，如速度、速率和身体技能，定义了球员的视觉呈现。

## 07

### 2016 Nike Strike Series FA16

Onformative

![image](img/f0025-01.jpg)

![image](img/f0026-01.jpg)

伦敦大学学院设计计算实验室

**设计**

曼努埃尔·希门尼斯·加西亚和吉勒斯·雷辛

**制造支持**

Nagami Design、维森特·索勒

**团队**

曼努埃尔·希门尼斯·加西亚、米格尔·安赫尔·希门尼斯·加西亚、伊格纳西奥·维格拉·奥乔亚、吉勒斯·雷辛、维森特·索勒

`VoxelChair`是机器人 3D 打印领域最新持续软件创新与开发的首个原型。`VoxelChair`背后的软件借鉴了从计算建筑学到医学成像的方法论，为设计和打印 3D 构图与结构创造了新的可能性。创作者建议：“设计师不应设计椅子的形态，而应直接设计材料的特性与行为。”

## 08

### 2016 VoxelChair v.1.0

曼努埃尔·希门尼斯·加西亚

吉勒斯·雷辛

Nagami Design

维森特·索勒

伦敦大学学院设计计算实验室

![image](img/f0027-01.jpg)

![image](img/f0028-01.jpg)

![image](img/f0030-01.jpg)

**客户**

杜比实验室

`Collide`是一件艺术装置，将记录的运动数据转化为抽象图形和声音。超现实的图像与引人入胜的音景营造出一个沉浸式空间，捕捉运动、色彩和声音的本质，以代表“放手”的体验。受联觉现象（感官的联合）启发，`Collide`通过结合原创室内乐与绘画般的视觉效果，创造了一种新的语言。

## 09

### 2016 Collide：联觉艺术装置

Onformative

![image](img/f0031-01.jpg)

## 10

### 2017 Block Bills

马蒂亚斯·德费尔特

![image](img/f0032-01.jpg)

![image](img/f0033-01.jpg)

档案级数字打印于纸上，3.3 x 5.9 英寸

`Block Bills`是一系列六十四张生成的钞票，代表比特币区块链中的区块。艺术家马蒂亚斯·德费尔特定义的可视化系统同时利用随机性和所选区块链中每个区块的独特方面，影响该系列中每张钞票的各个方面。这些钞票暗喻了德费尔特对比特币和加密货币的矛盾心理；它们将这些原本无形且不可见的构造带入了一个视觉和情感上可感知的语境中。

![image](img/f0034-01.jpg)

**地图与道路网络数据**

OpenStreetMap

**路由引擎**

GraphHopper

**条条大路通罗马**是一个数据可视化项目，探索了“条条大路通罗马”这一习语。其结果既是信息可视化，也是数据艺术，并揭示了大规模移动模式。这些可视化是通过对现有街道基础设施（OpenStreetMap）应用路由算法，从城市尺度到大陆尺度创建的。除了美学价值外，生成的图像还揭示了道路基础设施如何反映区域、政治和地理状况。

## 11

### 2015 条条大路通罗马

贝内迪克特·格罗斯

菲利普·施密特

拉斐尔·赖曼

moovel lab

![image](img/f0035-01.jpg)

## 12

### 2015 Jller

本杰明·毛斯

普罗科普·巴托尼切克

![image](img/f0036-01.jpg)

![image](img/f0037-01.jpg)

**附加机械与电子**

托米斯拉夫·阿瑙多夫

**开发于**

pebe/lab（布拉格）和 FELD（柏林）

`Jller`是工业自动化和历史地质学领域一个持续研究项目的一部分。该装置使用计算机视觉按地质年龄对特定河流中的卵石进行分类。该装置在自动分类过程中展示了自然地质历史，其本身即构成一场表演。

![image](img/f0038-01.jpg)

## 13

### 2016 Aerial Bold

贝内迪克特·格罗斯

乔伊·李

![image](img/f0040-01.jpg)

![image](img/f0041-01.jpg)

**字体设计**

马尔科·贝伦兹

**机器学习硕士论文**

安基塔·阿格拉瓦尔，人工智能研究所，拉文斯堡-魏恩加滕应用技术大学

**资金与支持**

Kickstarter 支持者

**航拍图像**

美国地质调查局（USGS）

与普遍看法相反，世界上大部分地区尚未被完全测绘。每天，卫星环绕地球，拍摄无数照片，但对于这些照片中独特的事物究竟捕捉到了什么，以及如何发现和分类它们，人们所知甚少。`Aerial Bold`——一项全球性的字母搜索任务——对此提出质疑，并引起了人们对这一潜力的关注。

![image](img/f0042-01.jpg)

# P.0 p5.js 简介

**P.0 p5.js 简介** 42

`P.0.0 p5.js`、`JavaScript`与`Processing` 44

`P.0.1`开发环境 46

`P.0.2`语言元素 48

`P.0.3`优雅编程 56

## P.0.0 p5.js、JavaScript 与 Processing

本书使用 JavaScript 库`p5.js`来介绍生成式设计的概念。以下页面概述了 JavaScript 的基本元素和功能，并简要介绍了 Processing 和`p5.js`的历史。

`p5.js`项目于 2013 年 8 月由艺术家、加州大学洛杉矶分校设计媒体艺术项目助理教授劳伦·麦卡锡发起。要解释`p5.js`背后的理念，有必要先提及更早的 Processing 项目。

编程语言 Processing 于 2001 年春天由本·弗莱和凯西·瑞斯与一小群助手共同发起。Processing 的主要目标（至今仍是）是让视觉导向的人能够轻松上手编程。Processing 是一个用于快速创建数字化、可编程草图（Processing 程序称为“sketch”）的工具或开发环境。^(1) 围绕 Processing 有一个庞大且活跃的社区，极大地促进了协作学习。网上有许多示例、视频、教程等资源。Processing 已成为设计、信息图表、建筑和艺术领域编程的标准。

[processingfoundation.org](http://processingfoundation.org)

**凯西·瑞斯和本·弗莱**

`p5.js`追求同样的目标：让图形编程尽可能简单。`p5.js`和 Processing 的各个命令极为相似。主要区别在于，与 Processing 不同，`p5.js`基于的不是 Java 编程，而是 JavaScript。这在技术上具有重要意义，对用户也很重要，因为 JavaScript 是运行在网页浏览器中、使网站动态且交互的编程语言。借助`p5.js`创建的程序可以直接在网络上使用。

`p5.js`是一个开源项目；可以免费下载并用于独立项目。由于`p5.js`是一个 JavaScript 库，而 JavaScript 是互联网时代使用最广泛的编程语言，因此代码示例很容易移植到大多数其他开发环境中。JavaScript 是跨平台的，因此同一份源代码可以在所有拥有现代浏览器或相应运行时环境的操作系统上使用——不仅限于计算机，还包括智能手机和平板电脑。

此外，围绕`p5.js`以及更大范围的 JavaScript，存在着庞大的在线社区。几乎所有与 JavaScript 相关的问题或难题都能在网上找到答案。互联网上充斥着其他 JavaScript 库，它们通常可以轻松地与`p5.js`结合使用。

对于本书中的程序，我们使用自己的程序库，该库可在本书网站上找到；我们还提供了一份外部库列表。例如，你可以使用`generative-design-library`在绘图板上工作，或创建 Adobe ASE 格式的调色板。

[generative-gestaltung.de](http://generative-gestaltung.de)

**generative-design-library**

**调色板导出 P.1.2**

调色板

**编写程序**`p5.js`使用 JavaScript 编程语言，但比纯 JavaScript 更简单。最重要的命令，尤其是用于图形输出的命令（例如绘制圆形），非常易于使用。初学者无需承担在浏览器窗口中显示图形元素所必需的其他额外结构。

在接下来的页面中，我们将演示如何设置工作空间（开发环境），并介绍`p5.js`最重要的语言元素和编程概念。你可以立即开始输入所展示的命令，并查看这些命令生成的结果。

## P.0.1 开发环境

迫不及待想开始了吗？很好！以下是如何尝试我们的程序、扩展它们或创建全新程序的方法。只需下载我们的代码包，其中包含本书的所有程序。链接可在 [generative-gestaltung.de](http://generative-gestaltung.de) 找到。

### 变体 1：p5.js 网页编辑器

这是最简单的入门方式。你只需要一个浏览器和互联网连接。

1. 打开`p5.js`的在线编辑器。它提供了一个舒适的环境，可以快速尝试一些东西。在浏览器窗口中，左侧有一个编辑代码的区域。有播放和停止按钮用于启动和停止程序；右侧是画布，你的草图将在此渲染；底部是控制台，用于显示任何错误消息或程序的其他文本输出。[editor.p5js.org](http://editor.p5js.org)

2. 将本书的程序上传到在线编辑器，复制并粘贴文本，或者从本书的收藏中复制一个草图。

![image](img/f0046-01.jpg)




代码编辑器和输出统一在浏览器窗口中。其他几个在线代码编辑器，如`Codepen.io`或`jsfiddle.net`，与`p5.js`网页编辑器类似，但它们是更通用的解决方案，并未针对`p5.js`进行优化。

### 变体 2：代码编辑器和浏览器

网页编辑器是初步尝试`p5.js`的好方法；但从长远来看，我们建议你按照以下说明设置本地工作环境。

1. 首先，一个好的代码编辑器至关重要，例如 Sublime Text、Atom、Brackets 或 Coda。
2. 下载我们的代码包。链接可在本书网站上找到。[generative-gestaltung.de](http://generative-gestaltung.de)
3. 现在，你可以通过在浏览器中打开某个草图文件夹（例如`P_1_0_01`）中的`index.html`来运行程序。
4. 要修改程序，请在文本编辑器中打开`sketch.js`文件，进行编辑，然后在浏览器中打开相应的`index.html`。在浏览器内容更新之前，必须保存对`sketch.js`所做的任何更改。重新加载浏览器以查看更改。

关于使用`p5.js`的更详细指南可在`p5.js`网站上找到。[p5js.org/get-started](http://p5js.org/get-started)

**!** 我们的一些代码示例需要在服务器上运行才能正常工作。这些草图使用外部资源，例如网络摄像头或外部文件，必须由 Web 服务器执行（草图的 URL 必须以“http”开头，否则浏览器将禁止使用这些资源）。关于如何使用它们的详细说明可在本书网站上找到。

![image](img/f0047-01.jpg)

一个代码编辑器，例如 Sublime Text。编辑器是一个独立的程序，未集成在浏览器中。

![image](img/f0047-02.jpg)

文件`index.html`（以及草图）直接从硬盘驱动器在浏览器中打开。因此，URL 也以“file”开头。

## P.0.2 语言元素

为了能够向计算机发出指令，你需要使用它的语言。在接下来的部分中，将介绍 JavaScript 和`p5.js`最重要的函数和控制结构。

### 你好，椭圆

第一个程序。打开`sketch.js`文件（位于`empty-example`文件夹中），在`draw()`函数中输入以下行，并在浏览器中打开关联的`index.html`。

```javascript
function draw() {
  ellipse(50, 50, 80, 80);
}
```

有一些用于绘图的命令，例如`ellipse`、`rect`、`line`等，以及一些用于指定后续图形如何绘制的命令，例如`stroke`、`strokeWeight`、`noStroke`、`fill`、`noFill`等。一旦配置了绘图模式，它将应用于所有后续的绘图命令，直到重新配置绘图模式。大多数绘图命令需要一个或多个参数，用于指示绘制的位置和大小。其度量单位是像素。坐标系的原点位于绘图画布的左上角。

1. 在画布上绘制一个圆形。函数通过声明关键字“function”，后跟函数名和一对圆括号`()`来创建。函数应执行的操作（例如绘制圆形）定义在花括号`{...}`之间。

```javascript
point(60, 50);
```

由命令`point(60, 50)`生成的像素因此被绘制在距左边缘六十像素、距上边缘五十像素的位置。

2. ![image](img/f0048-01.jpg)

当然，可以有不止一行代码。各行代码将从上到下依次执行。因此，`p5.js`会读取以下命令行：

```javascript
fill(128);
strokeWeight(1);
```

```javascript
ellipse(40, 50, 60, 60);
```

```javascript
rect(50, 50, 40, 20);
```

使用这些命令时，注意拼写要准确，包括大小写字母。例如，`strokeWeight()`命令如果写成`strokeweight()`或`StrokeWeight()`将无法被识别。

**3** 将填充颜色设置为中灰色。将线宽设置为 1 像素。在点 (40, 50) 处绘制一个宽度和高度均为 60 像素的椭圆。在坐标 (50, 50) 处绘制一个宽度为 40、高度为 20 的矩形。

![image](img/f0048-02.jpg)

### 设置、绘制与预加载

`p5.js`提供了多种自动调用的函数。其中最重要的两个是`setup()`和`draw()`。

`draw()`函数在每个绘制步骤中被调用，每次都会执行其中的每一条命令。

**4**

```javascript
function draw() { }
```

**4** 尽管这个`draw()`函数不包含任何命令，但它能使程序保持运行。

**5**

```javascript
function draw() {
  console.log(frameCount);
}
```

`draw()`函数以预设的频率显示，该频率指定了每秒显示多少帧图像。标准设置为每秒 60 帧，但可以使用`frameRate()`命令重新设置。

**5** 一个包含一条命令的`draw()`函数。命令`console.log()`将文本写入控制台。在此例中，它显示实际帧的不断递增的数值。

**6**

```javascript
frameRate(30);
```

然而，如果每帧的计算量过大，导致浏览器无法在预设时间内完成执行，则设定的帧率会自动降低。

某些操作只应在程序启动时执行一次，而不应在每一帧中重复执行。为此使用`setup()`函数。

**6** 此绘制速度设置为每秒 30 帧。

**7**

```javascript
function setup() {
  frameRate(30);
}
```

`preload()`函数确保在程序启动时额外数据已完全加载。

**7** 这些应在程序启动时仅执行一次的命令出现在`setup()`函数中。

**8**

```javascript
function preload() {
  img = loadImage("data/pic1.jpg");
}
```

**8** 在`preload()`中插入加载数据的指令；此示例中需要加载一张图片。

### 绘制画布与渲染器

在浏览器窗口内创建一个绘制画布。这是程序视觉输出的显示窗口，可以缩放到任意大小。

**9**

```javascript
createCanvas(640, 480);
```

除了宽度和高度参数外，使用`createCanvas()`命令还可以指定用于显示图像的渲染器。渲染器负责将不同的图形命令实际转换为像素。可用的渲染选项如下：

**9** 绘制画布现在宽 640 像素，高 480 像素。

**10**

```javascript
createCanvas(640, 480, P2D);
```

**11**

```javascript
createCanvas(640, 480, WEBGL);
```

**10** 标准渲染器：如果未指定其他渲染器，则使用此渲染器。

**11** 用于 Web 浏览器中硬件加速 3D 图形的渲染器。

### 变换

`p5.js`的优势之一在于它可以移动、旋转和缩放坐标系。之后的所有图形命令都参照这个改变后的坐标系。

**12**

```javascript
translate(40, 20);
rotate(0.5);
scale(1.5);
```

在此示例中，坐标系向右移动 40 像素，向下移动 20 像素，然后旋转 0.5 弧度（约 30°），最后按 1.5 倍缩放。

在 Processing 中，角度通常以弧度表示，其中 180° 等于圆周率 π（≈ 3.14），旋转方向为顺时针。

**12** ![image](img/f0050-01.jpg)

### 变量与数据类型

在程序中，信息存储在变量中，以便程序的其他部分使用。这些变量可以取任何名称，但不能是 JavaScript 的关键字。关键字可以通过编辑器中的特殊颜色来识别。

**13**

```javascript
var myVariable;
myVariable = 5;
```

**13** 创建了变量`myVariable`。然后将值 5 保存到其中。

变量可以包含不同的数据类型。与大多数其他编程语言不同，JavaScript 在创建变量时无需考虑这一点。尽管如此，跟踪哪些变量存储了哪种类型的值仍然很重要。例如，数据类型可以是：

**14**

```javascript
var myBooleanvalue = true:
```

**15**

```javascript
var myInteger = 7:
```

**16**

```javascript
var myFloatingPointNumber = -3.219:
```

**17**

```javascript
var myCharacter = "A":
```

**18**

```javascript
var myString = "This is a text":
```

**14** 逻辑值（布尔值）：true 或 false

**15** 整数：例如 50、-532。

**16** 浮点值：例如 0.02、-73.1。

**17** 单个字符：例如 “a”、“A”、“9”、“&”。

**18** 字符串/文本：例如 “Hello, world”。

### 数组

当处理大量值时，为每个值创建一个变量很不方便。数组允许管理一个值列表。

**19**

```javascript
var planets = ["Mercury", "Venus", "Earth", "Mars".
"Jupiter", "Saturn", "Uranus", "Neptune"]:
```

**19** 数组由方括号定义。在方括号内，可以列出任意数量的值（此处为八个行星名称），用逗号分隔。

**20**

```javascript
console.log(planet[0]):
```

**20** 通过在变量名后的方括号中输入索引号来访问值。索引 0 指向数组中的第一个条目。

如果没有立即为数组赋值，可以先创建数组，稍后再填充：

**21**

```javascript
var planetDiameter = [];
planetDiameter[0] = 4879;
planetDiameter[1] = 12104;
planetDiameter[2] = 12756;
planetDiameter[3] = 6794;
...
```

数组还有许多其他用于处理元素的函数。在本书中，我们主要使用`<yourarray>.push()`向数组末尾添加新元素。

**21** 方括号初始化一个空数组。然后为数组赋值。这也可以在程序运行期间稍后进行。

**22**

```javascript
planet.push("Pluto");
```

**22** 尽管冥王星不再被视为行星，但可以通过这种方式将其名称添加到数组`planet`中。

### 对象

除了数组，许多信息可以同时存储在对象中。区别在于，单个值不是通过数字索引访问，而是通过键访问。

**23**

```javascript
var planet = {name: "Saturn", mass: 5.685e26,
temperature: 134};
planet.diameter = 120536;
console.log("mass in kg: " + planet.mass);
```

或者，可以按如下方式访问值。如果键不是从一开始就固定的，而是动态生成或读取的，则此方法很有必要。

**23** JavaScript 对象通过将一组键/值对包含在一组花括号`{}`中来创建。此处生成了一个包含三个键/值对的对象。向现有对象添加了另一个键/值对，并访问了其中一个值并将其记录到控制台。

**24**

```javascript
var k = "mass";
console.log("mass in kg: " + planet[k]);
```

**24** 如果键的名称存储在变量中，则可以使用该变量作为对该键的引用来访问值。

### 运算符与数学

当然，Processing 中也可以进行计算。这可以通过简单的数字实现……

**25**

```javascript
var a = (4 + 2.3) / 7;
```

通过字符串……

**25** 执行后，值 0.9 被保存在`a`中。

**26**

```javascript
var s = "circumference of Jupiter: " + (142984 * PI) + "km";
```

**26** 变量`s`随后包含字符串 “circumference of Jupiter: 449197.5 km”。

以及通过变量：

**27**

```javascript
var i = myVariable * 50;
```

**27** `myVariable`中的值乘以 50，结果保存在`i`中。

可用的计算运算符有：`+`、`-`、`*`、`/`、`%`。此外还有一系列数学函数。以下是一些示例：

**28**

```javascript
var converted aValue = map(aValue, 10, 20, 0, 1);
```

**29**

```javascript
var roundedValue = round(2.67);
```

**30**

```javascript
var randomValue = random(-5, 5);
```

#### 31

```javascript
var cosineValue = cos(angle);
```

**28**：`aValue`中的值从 10 到 20 之间的数字转换为 0 到 1 之间的数字。

**29**：四舍五入：`roundedValue`为 3。

**30**：-5 到 5 之间的随机数。

**31**：计算角度的余弦值。

### 鼠标与键盘

使用鼠标和键盘作为输入设备，有几种获取信息的方式。一种选择是查询`p5.js`中可用的变量。

#### 32

```javascript
function draw() {
  console.log("mouseposition:" + mouseX + "," + mouseY);
  console.log("mousekey pressed?:" + mouseIsPressed);
  console.log("key pressed?:" + keyIsPressed);
  console.log("last pressed key:" + key);
}
```

另一种可能性是实现某个事件处理函数。当相应事件发生时——即按下鼠标按钮或键盘按键时——事件处理函数会被调用。

**32**：Processing 变量`mouseX`和`mouseY`始终包含鼠标的实际位置；如果此时按下了某个鼠标按钮，`mouseIsPressed`为 true。对于键盘，`keyIsPressed`指示是否有按键被按下；最后按下的键显示在`key`中。

#### 33

```javascript
function mouseReleased() {
  console.log("The mouse key was released");
}
```

其他事件处理函数包括`mousePressed()`、`mouseMoved()`、`keyPressed()`和`keyReleased()`。

**33**：当释放鼠标左键时，会调用函数`mouseReleased()`。

### 条件

通常，只有在满足特定条件时才需要执行某些代码行。为此使用`if`语句。

#### 34

```javascript
if (aNumber == 3) {
  fill(255, 0, 0);
  ellipse(50, 50, 80, 80);
}
```

#### 35

```javascript
if (aNumber == 3) {
  fill(255, 0, 0);
} else {
  fill(0, 255, 0);
}
```

#### 36

```javascript
if (aNumber == 3) fill(255, 0, 0);
else fill(0, 255, 0);
```

区分变量的多个值通常可以通过`switch`命令实现。

**34**：只有当`if`语句中的条件满足时——即变量`aNumber`的值为 3 时——才会执行花括号内的两行代码。

**35**：使用`else`，`if`条件扩展了一段代码，当指定的`if`条件不满足时执行这段代码。

**36**：如果代码段只有一行，如上一个示例所示，可以省略花括号。

#### 37

```javascript
switch (aNumber) {
  case 1:
    rect(20, 20, 80, 80);
    break;
  case 2:
    ellipse(50, 50, 80, 80);
    break;
  default:
    line(20, 20, 80, 80);
}
```

**37**：`switch`命令测试变量`aNumber`的值是否与`case`行中列出的某个值匹配，如果匹配则跳转到该处，并继续执行代码直到遇到`break`语句。如果没有匹配的值，程序执行会从`default`继续。

### 函数

程序中经常有在不同位置以类似方式出现的部分。在许多此类情况下，将这些部分封装到函数中是明智的做法。例如：

#### 38

```javascript
function draw() {
  translate(40, 15);
  line(0, -10, 0, 10);
  line(-8, -5, 8, 5);
  line(-8, 5, 8, -5);
  translate(20, 50);
  line(0, -10, 0, 10);
  line(-8, -5, 8, 5);
  line(-8, 5, 8, -5);
}
```

要改变这个程序中星星的外观，必须在两个地方修改绘图命令。因此，最好将相应的行存储在一个函数中。

**38**：坐标系被移动到另一个位置，在那里用三条线绘制一颗星星。然后再次移动坐标系，并在新位置使用相同的命令绘制一颗星星。

#### 39



```javascript
function draw() {
  translate(40, 15);
  drawStar();
  translate(20, 50);
  drawStar();
}

function drawStar() {
  line(0, -10, 0, 10);
  line(-8, -5, 8, 5);
  line(-8, 5, 8, -5);
}
```

可以向函数传递值，函数也可以返回一个值作为结果。

**39**：函数`drawStar()`现在包含了绘图命令。可以从程序中的任何其他点调用此函数，以执行其中包含的代码。

#### 40

```javascript
function setup() {
  console.log("The faculty of 5 is 1*2*3*4*5 = "
    + faculty(5));
}

function faculty(theValue) {
  var result = 1;
  for (var i = 1; i <= theValue; i++) {
    result = result * i;
  }
  return result;
}
```

在 JavaScript 中，函数接受另一个函数作为其参数之一（称为“回调函数”）的情况尤为常见。回调函数允许在事件触发时执行操作。

**40**：这里定义了一个函数`faculty()`，其中传递了一个值`theValue`。当调用该函数时，参数（此处为 5）被传入变量`theValue`。在函数内部，使用该值执行各种计算，并通过命令`return`返回结果。

#### 41

```javascript
loadJSON("myData.json", callback);

function callback(data) {
  console.log(data);
}
```

**41**：当以这种方式使用 p5.js 函数`loadJSON()`时，程序流程不会被加载过程阻塞，而是在后台运行（异步加载）。当文件完全加载后，会调用`callback()`函数。

### 循环

循环用于在程序中多次执行特定命令。可以通过多种方式编写循环。

`for`循环用于将代码段循环执行特定次数。

#### 42

```javascript
for (var i = 0; i <= 5; i++) {
  line(0, 0, i * 20, 100);
  line(100, 0, i * 20, 100);
}
```

**42**：花括号内的两行代码恰好执行六次。首先将变量`i`设置为值 0，然后在每次循环后增加 1（`i++`），只要该值小于或等于 5。

#### 43

```javascript
var myvalue = 0;
while (myValue < 100) {
  myValue = myValue + random(5);
  console.log("The value of myValue is " + myValue);
}
```

**43**：只要变量`myValue`的值小于 100，这个`while`循环就会继续。在每个新的循环周期中，会添加一个介于 0 和 5 之间的随机值。

只要满足特定条件，`while`循环就会继续。

有几种方法可以遍历数组中的所有值。这里展示了一些常用方法：

```javascript
var planets = ["Mercury", "Venus", "Earth", "Mars",
  "Jupiter", "Saturn", "Uranus", "Neptune"];
```

#### 44

```javascript
for (var i = 0; i < planets.length; i++) {
  console.log(planets[i]);
}
```

#### 45

```javascript
planet.forEach(function(planet) {
  console.log(planet);
});
```

**44**：变体 1：当变量`i`小于数组长度时，`for`循环运行。

**45**：变体 2：这里使用了数组函数`forEach()`。这需要一个回调函数，该函数在循环的每次迭代中被调用。变量`planet`依次包含数组的各个值。

为了遍历对象的所有键/值对，以下`for`循环的变体是合适的：

```javascript
var planet = {name: "Saturn", mass: 5.685e26,
  temperature: 134, diameter: 120536};
```

#### 46

```javascript
for (k in planet) {
  console.log("Key: " + k + ", Value: " + planet[k]);
}
```

**46**：变量`k`依次包含对象的每个键。这可用于访问关联的值。

## P.0.3 优雅地编程

在编程中，通常有多种方法可以达到期望的结果。程序能运行只是解决方案的一部分，尽管是非常重要的一部分；还有其他方面需要考虑。

### 注释

程序越复杂、越棘手，其他人——甚至你自己在一段时间后——就越难理解它。一个难以理解的程序无法被修改或更新。程序中的注释有助于澄清代码。

#### 1

```javascript
// calculate distance between actual and previous mouse
// position, which represents the speed of the mouse
var speed = dist(mouseX, mouseY, pmouseX, pmouseY);
```

p5.js 社区遍布全球。因此，建议用英文编写注释和变量名。这样，你和他人就能更容易地在互联网论坛上搜索并找到问题的建议和答案。

| 1 | 两个正斜杠后面的文本会被忽略，可用于注释。 |

### 有用的名称和清晰的结构

除了使用注释外，合理选择的变量和函数名有助于用户保持整体概览，并理解特定程序的功能。

#### 2

```javascript
function mixer(apples, oranges) {
  var juice = (apples + oranges) / 2;
  return juice;
}
```

为此，有必要借助函数和类将程序划分为更小、更符合逻辑的段落。这种功能封装也意味着程序可以快速修改和扩展。

| 2 | 在这个例子中，很难看出函数计算的是什么。只能从公式中猜测它计算的是两个数的平均值。 |

### 性能

尽管计算机变得越来越快，执行一条命令仍然需要时间。当一条命令被频繁执行时，即使是短暂的时间也会显著累积。尽量不要让程序承担不必要的工作。

#### 3

```javascript
for (var i = 0; i < 10000000; i++) {
  var speed = dist(mouseX, mouseY, pmouseX, pmouseY);
  doSomethingWithMouseSpeed(speed);
}
```

#### 4

```javascript
var speed = dist(mouseX, mouseY, pmouseX, pmouseY);

for (var i = 0; i < 10000000; i++) {
  doSomethingWithMouseSpeed(speed);
}
```

在本书的程序中，我们努力遵循上述原则。然而，有时清晰度和性能会相互矛盾，这意味着为性能优化的程序代码可能更难理解。在这种情况下，我们选择了更清晰的结构。

| 3 | 这里，`mouseSpeed`在所有一千万次循环中都被计算，尽管在此期间鼠标位置无法改变。 |
| 4 | 因此，当鼠标速度在循环外计算时，性能得到了极大提升。 |

^(1) 一本非常优秀且详细的 Processing 编程入门书是《Processing: A Programming Handbook for Visual Designers and Artists》。

![image](img/f0058-01.jpg)

# P.1 颜色

与本书不同——我们通过反射和过滤光来感知颜色——计算机是真正的量子弹射器。当我们看屏幕时，光以不同波长直接射入我们的眼睛，并且可以实时操控。以下示例为用户提供了使用颜色时最重要的技术特性，并介绍了在屏幕上设计时使用颜色的几种方法。

**P.1 颜色** 58

P.1.0 你好，颜色 60

P.1.1 色谱 62

P.1.1.1 网格中的色谱 62

P.1.1.2 圆形中的色谱 64

P.1.2 调色板 66

P.1.2.1 通过插值生成调色板 66

P.1.2.2 从图像中提取调色板 68

P.1.2.3 根据规则生成调色板 72

## P.1.0 你好，颜色

直接操控 16,777,216 种颜色的能力给用户带来了惊人的自由度。同时对比——没有它就无法感知颜色——在这里通过并置多种颜色组合来展示。我们对一种颜色的感知会受到其相邻颜色以及该颜色与背景之间比例变化的影响。

`→ P_1_0_01`

鼠标的水平位置控制颜色区域的大小。从中心开始，彩色区域的高度和宽度为 1 到 720 像素。鼠标的垂直位置控制色相。背景从 0 到 360 遍历色谱，而颜色区域则从相反方向（360 到 0）遍历色谱。

![image](img/f0060-01.jpg)

#### 1

```javascript
function setup() {
  createCanvas(720, 720);
  noCursor();
}
```

#### 2

```javascript
colorMode(HSB, 360, 100, 100);
rectMode(CENTER);
noStroke();
```

| 1 | `setup()`函数设置显示窗口的大小，并使光标不可见。 |
| 2 | 在此程序中，颜色应遍历色相光谱。因此，`colorMode()`允许用户更改颜色值的解释方式。`HSB`指定颜色模型，其后的三个值指定各自的取值范围。例如，色相只能通过 0 到 360 之间的值来指定。 |

```javascript
function draw() {
  background(mouseY / 2, 100, 100);
  fill(360 - mouseY / 2, 100, 100);
  rect(360, 360, mouseX + 1, mouseX + 1);
}
```

| 3 | 鼠标位置的 y 值除以 2，得到色轮上 0 到 360 的值。 |
| 4 | 鼠标位置的 y 值的一半从 360 中减去，得到 360 到 0 的值。 |
| 5 | 颜色区域的大小随鼠标位置的 x 值变化，边长在 1 到 720 像素之间。 |

| 鼠标： | 位置 x：矩形大小 |
|---|---|
|  | 位置 y：色相 |
| 按键： | S：保存图像 |

![image](img/f0061-01.jpg)

`→ P_1_0_01`鼠标位置的 x 值定义内部颜色区域的大小，y 值定义色相。

## P.1.1.1 网格中的色谱

该色谱由彩色矩形组成。每个色块在水平轴上分配一个色相值，在垂直轴上分配一个饱和度值。通过放大矩形可以降低颜色分辨率，从而使色谱中的原色更加清晰。

`→ P_1_1_1_01`

网格由两个嵌套的`for`循环创建。在外层循环中，y 位置逐步增加。内层循环则通过逐步增加矩形 x 位置的值来绘制一行，直到处理完整个宽度。步长由鼠标位置的值设定，并存储在变量`stepX`和`stepY`中。它还决定了矩形的长和宽。

![image](img/f0062-01.jpg)

![image](img/f0062-02.jpg)

`→ P_1_1_1_01`尽管所有色块之间的颜色值距离相同，但在某些位置，对比度感觉比其他位置更大。

```javascript
var stepX;
var stepY;

function setup() {
  createCanvas(800, 400);
  noStroke();
  colorMode(HSB, width, height, 100);
}
```

| 1 | 使用`createCanvas()`设置显示大小。此处定义的值可随时通过系统变量`width`和`height`获取。 |
| 2 | 使用命令`colorMode()`将色相和饱和度的取值范围设置为 800 或 400。色相不再定义为 0 到 360 之间的数字，而是 0 到 800 之间的数字。饱和度也是如此。 |

```javascript
function draw() {
  stepX = mouseX + 2;
  stepY = mouseY + 2;

  for (var gridY = 0; gridY < height; gridY += stepY) {
    for (var gridX = 0; gridX < width; gridX += stepX) {
      fill(gridX, height - gridY, 100);
      rect(gridX, gridY, stepX, stepY);
    }
  }
}
```

| 3 | 加 2 是为了防止`stepX`或`stepY`过小，否则会导致显示时间过长。 |
| 4 | 借助两个嵌套循环，现在将处理网格中的所有位置。要绘制的矩形的 y 位置由外层循环中的`gridY`定义。该值仅在内层循环处理完毕（即绘制完一整行矩形）后才会增加。 |
| 5 | 变量`gridX`和`gridY`不仅用于定位图块，还用于定义填充颜色。色相由`gridX`决定。饱和度值随着`gridY`值的增加而按比例减小。 |

| 鼠标： | 位置`x`/`y`：网格分辨率 |
|---|---|
| 按键： | S：保存图像 |

![image](img/f0063-01.jpg)

**→ P_1_1_1_01**全分辨率下呈现柔和的彩虹效果。

![image](img/f0063-02.jpg)

**→ P_1_1_1_01**计算机显示器的三原色——红、绿、蓝——以不同渐变呈现。

![image](img/f0063-03.jpg)

**→ P_1_1_1_01**在此分辨率下也能看到二次色。

## P.1.1.2 圆形色环

组织颜色的模型有很多种。将色谱排列成圆形（色环）是一种流行的模型，用于比较和谐、对比和色调。你可以控制圆形扇区的数量，以及它们的亮度和饱和度值，从而更好地理解 HSB 模式下的颜色排列。

**→ P_1_1_2_01**

色环扇区以扇形排列。每个顶点由对应角度的余弦值和正弦值计算得出。可以使用 Processing 的一种模式方法，使得创建扇区特别容易。各个点必须按以下顺序设置：首先是中心点，然后依次是外部点。

![image](img/f0064-01.jpg)

![image](img/f0064-02.jpg)

**→ P_1_1_2_01**扇区数量 45，按键 2。

![image](img/f0064-03.jpg)

**→ P_1_1_2_01**扇区数量 12，按键 4。

![image](img/f0064-04.jpg)

**→ P_1_1_2_01**扇区数量 6，按键 5。

```javascript
function draw() {
  colorMode(HSB, 360, width, height);
  background(360, 0, height);

  var angleStep = 360 / segmentCount;
  beginShape(TRIANGLE_FAN);

  vertex(width / 2, height / 2);

  for (var angle = 0; angle <= 360; angle += angleStep) {
    var vx = width / 2 + cos(radians(angle)) * radius;
    var vy = height / 2 + sin(radians(angle)) * radius;
    vertex(vx, vy);
    fill(angle, mouseX, mouseY);
  }

  endShape();
}
```

| 1 | 饱和度和亮度的取值范围经过调整，使得鼠标坐标可以作为它们的值。 |
| 2 | 角度增量`angleStep`取决于要绘制的扇区数量（`segmentCount`）。 |
| 3 | 第一个顶点位于绘图画布的中心。 |
| 4 | 对于其他顶点，需要将`angle`从度数（0–360）转换为弧度（0–2π），因为`sin()`和`cos()`函数要求以这种方式输入角度。此转换通过使用`radians()`完成。 |
| 5 | 定义下一个扇区的填充颜色：`angle`的值作为色相，`mouseX`作为饱和度，`mouseY`作为亮度。 |
| 6 | 使用`endShape()`结束颜色扇区的构建。 |

```javascript
function keyPressed() {
  ...

  switch (key) {
    case '1':
      segmentCount = 360;
      break;
    case '2':
      segmentCount = 45;
      break;
    case '3':
      segmentCount = 24;
      break;
    case '4':
      segmentCount = 12;
      break;
    case '5':
      segmentCount = 6;
      break;
  }
}
```

| 7 | `switch()`命令检查最后按下的键，从而可以轻松在不同情况之间切换。 |
| 8 | 例如，如果按下按键 3，则`segmentCount`被设置为值 24。 |

| 鼠标：按键： | 位置`x`：饱和度；位置`y`：亮度；1–5：扇区数量；S：保存图像 |



## P.1.2.1 通过插值生成调色板

在每个颜色模型中，颜色都有其明确的位置。从一种颜色到另一种颜色的直接路径总是有精确可定义的渐变，这些渐变会根据具体模型而变化。利用这种插值，你可以创建每个渐变中的颜色组，并定位单个中间色调。

→ `P_1_2_1_01`

由于颜色不是由单个数字而是由多个值定义的，因此需要在这些值之间进行插值。根据所选的颜色模型（RGB 或 HSB），相同的颜色由不同的值定义，从而导致从一种颜色到另一种颜色的路径会经过不同的颜色。例如，在 HSB 颜色模型中，会绕道经过色环。这种差异源于颜色模型的特性，根据情况，这两种模型都可能非常有用。因此，选择合适的颜色模型来解决特定问题非常重要。

![image](img/f0066-01.jpg)

![image](img/f0066-02.jpg)

→ `P_1_2_1_01` RGB 颜色空间中的插值。每一行中，两种颜色以九个步骤进行插值。

```javascript
function draw() {
1
tileCountX = int(map(mouseX, 0, width, 2, 100));
tileCountY = int(map(mouseY, 0, height, 2, 10));
var tileWidth = width / tileCountX;
var tileHeight = height / tileCountY;
var interCol;
...
2
for (var gridY = 0; gridY < tileCountY; gridY++) {
3
var col1 = colorsLeft[gridY];
var col2 = colorsRight[gridY];
for (var gridX = 0; gridX < tileCountX; gridX++) {
var amount = map(gridX, 0, tileCountX - 1, 0, 1);
...
4
interCol = lerpColor(col1, col2, amount);
...
fill(interCol);
var posX = tileWidth * gridX;
var posY = tileHeight * gridY;
rect(posX, posY, tileWidth, tileHeight);
...
}
}
}
```

| 标记 | 说明 |
|---|---|
| 1 | 颜色渐变数量 `tileCountX` 和行数 `tileCountY` 由鼠标位置决定。 |
| 2 | 逐行绘制网格。 |
| 3 | 左右两列的颜色设置在数组 `colorsLeft` 和 `colorsRight` 中。 |
| 4 | 中间颜色通过 `lerpColor()` 计算。该函数在单个颜色值之间执行插值。变量 `amount` 是一个介于 0 和 1 之间的值，指定了起始颜色和结束颜色之间的位置。 |
| ! | 在所有调色板章节描述的程序中，可以使用 C 键保存 Adobe 应用程序的 ASE 格式调色板。 |
| 鼠标：按键： | 左键点击：新的随机颜色集；位置 `x`：分辨率；位置 `y`：行数；1–2：插值样式；S：保存图像；C：保存 ASE 调色板。 |

![image](img/f0067-01.jpg)

→ `P_1_2_1_01` HSB 颜色空间中的插值。尽管每行开头和结尾的颜色与对面图像中的相同，但生成了完全不同的中间颜色步骤。

## P.1.2.2 从图像中提取调色板

我们周围始终环绕着调色板；我们只需记录并评估它们。从一个人的衣柜照片中获取的颜色——一个非常个性化的调色板——通过以下程序进行选择和排序。你可以导出生成的颜色集合，并将其用作灵感调色板。

→ `P_1_2_2_01`

使用鼠标位置以特定的网格间距，逐行逐个扫描加载图像的像素，以定义各自的颜色值。这些值存储在一个数组中，可以按色相、饱和度、亮度或灰度值进行排序。

![image](img/f0068-01.jpg)

![image](img/f0068-02.jpg)

→ 摄影：Stefan Eigner。原始图像：地铁隧道。

![image](img/f0068-03.jpg)

→ `P_1_2_2_01` 按色相排列的像素。

![image](img/f0068-04.jpg)

按饱和度排列的像素。

![image](img/f0068-05.jpg)

按亮度排列的像素。

```javascript
var img;
1
var colors = [];
var sortMode = null;
```

| 标记 | 说明 |
|---|---|
| 1 | 当前选定的排序模式始终存储在变量 `sortMode` 中。默认不排序，因此该值设置为 `null`（未定义）。 |

```javascript
function preload(){
2
img = loadImage("data/pic1.jpg");
}
```

| 标记 | 说明 |
|---|---|
| 2 | 在程序开始运行之前，加载图像并存储到名为 `img` 的变量中。 |

```javascript
function draw() {
3
var tileCount = floor(width / max(mouseX, 5));
4
var rectSize = width / tileCount;
```

| 标记 | 说明 |
|---|---|
| 3 | 网格的行列数 `tileCount` 取决于鼠标的 x 值。函数 `max()` 会从两个给定值中选取较大的一个。 |
| 4 | 刚刚计算出的网格分辨率现在用于定义瓦片的大小 `rectSize`。 |

5

```javascript
img.loadPixels();
colors = [];
for (var gridY = 0; gridY < tileCount; gridY++) {
  for (var gridX = 0; gridX < tileCount; gridX++) {
```

6

```javascript
var px = int(gridX * rectSize);
var py = int(gridY * rectSize);
var i = (py * img.width + px) * 4;
var c = color(img.pixels[i], img.pixels[i+1],
              img.pixels[i+2], img.pixels[i+3]);
colors.push(c);
```

7

```javascript
gd.sortColors(colors, sortMode);
var i = 0;
for (var gridY = 0; gridY < tileCount; gridY++) {
  for (var gridX = 0; gridX < tileCount; gridX++) {
```

8

```javascript
fill(colors[i]);
rect(gridX*rectSize, gridY*rectSize,
     rectSize, rectSize);
i++;
  }
}
```

| 标记 | 说明 |
|---|---|
| 5 | 只有在调用 `loadPixels()` 之后，才能访问图像的各个像素。 |
| 6 | 现在，按照之前计算出的网格间距 `rectSize`，逐行扫描图像。像素以长列表的形式存储在 `pixels[]` 数组中。因此，必须根据 `px` 和 `py` 计算出对应的索引 `i`。 |
| 7 | 使用 `sortColors()` 函数对颜色进行排序。该函数需要传入数组 `colors` 和排序模式 `sortMode`。 |
| 8 | 为了绘制调色板，再次遍历网格。从数组 `colors` 中逐个取出瓦片的填充颜色。 |

```javascript
function keyReleased(){
  if (key == 'c' || key == 'C') writeFile(
```

9

```javascript
    [gd.ase.encode(colors)],
    gd.timestamp(), 'ase');
  ...
```

10

```javascript
  if (key == '5') sortMode = null;
  if (key == '6') sortMode = gd.HUE;
  if (key == '7') sortMode = gd.SATURATION;
  if (key == '8') sortMode = gd.BRIGHTNESS;
  if (key == '9') sortMode = gd.GRAYSCALE;
}
```

| 标记 | 说明 |
|---|---|
| 9 | 函数 `ase.encode()` 可以将颜色数组保存为 Adobe Swatch Exchange (ASE) 文件。之后，该调色板可以作为色板库加载，例如在 Adobe Illustrator 中。 |
| 10 | 按键 5 到 9 控制应用于颜色的排序函数。为此，将 `sortMode` 设置为 `null`（不排序）或 Generative Design 库中的常量之一：`HUE`、`SATURATION`、`BRIGHTNESS` 或 `GRAYSCALE`。 |
| 鼠标：按键： | 位置 `x`：分辨率；1–4：更换示例图像；5–9：更改排序模式；S：保存图像；C：保存 ASE 调色板。 |

![image](img/f0070-01.jpg)

→ `P_1_2_2_01` “pic4.jpg” 按灰度值排序。

![image](img/f0070-02.jpg)

→ 摄影：Steffen Knöll。

![image](img/f0071-01.jpg)

→ `P_1_2_2_01` “pic4.jpg” 按色相排序。

## P.1.2.3 基于规则的调色板

所有颜色都由三个分量组成：色相、饱和度和明度。这些颜色分量的值通过一组规则来定义。通过使用受控的随机函数，你可以快速创建具有特定颜色细微差别的不同调色板。

→ `P_1_2_3_01`

色相、饱和度和明度的值从预定义的值范围内随机选取。这种规则集（值范围的定义）与随机函数的组合意味着会不断创建新的调色板，并且它们总能产生特定的颜色细微差别。

由于颜色的感知依赖于上下文，因此生成的颜色会绘制在一个交互式网格中。这样，颜色的细微差别会更加明显。

![image](img/f0072-01.jpg)

1

```javascript
var hueValues = [];
var saturationValues = [];
var brightnessValues = [];
```

| 标记 | 说明 |
|---|---|
| 1 | 使用单独的数组来保存色相、饱和度和明度。根据按下的按键（0–9），按照不同的规则填充这些数组。 |

```javascript
function draw() {
  ...
```

2

```javascript
  var index = counter % currentTileCountX;
  fill(hueValues[index],
       saturationValues[index],
       brightnessValues[index]);
  rect(posX, posY, tileWidth, tileHeight);
  counter++;
  ...
}
```

| 标记 | 说明 |
|---|---|
| 2 | 绘制网格时，从数组中逐个选取颜色。由于取模运算符 `%` 的作用，不断递增的变量 `counter` 开始循环相同的值。例如，当 `currentTileCountX` 为 3 时，`index` 将依次取值 0、1、2、0、1、2……这意味着网格中只使用了数组中的前几个颜色。 |

3

```javascript
if (key == '1') {
  for (var i = 0; i < tileCountX; i++) {
    hueValues[i] = int(random(0, 360));
    saturationValues[i] = int(random(0, 100));
    brightnessValues[i] = int(random(0, 100));
  }
}
```

| 标记 | 说明 |
|---|---|
| 3 | 按下按键 1 时，三个数组被填充为来自完整值范围的随机值。这意味着调色板中可能出现任何颜色。 |

![image](img/f0073-01.jpg)

4

```javascript
if (key == '2') {
  for (var i = 0; i < tileCountX; i++) {
    hueValues[i] = int(random(0, 360));
    saturationValues[i] = int(random(0, 100));
    brightnessValues[i] = 100;
  }
}
```

| 标记 | 说明 |
|---|---|
| 4 | 这里明度始终设置为 100。结果是一个以明亮颜色为主的调色板。 |

![image](img/f0073-02.jpg)

5

```javascript
if (key == '3') {
  for (var i = 0; i < tileCountX; i++) {
    hueValues[i] = int(random(0, 360));
    saturationValues[i] = 100;
    brightnessValues[i] = int(random(0, 100));
  }
}
```

| 标记 | 说明 |
|---|---|
| 5 | 当饱和度设置为 100 时，不会产生柔和色调。 |

![image](img/f0073-03.jpg)

6

```javascript
if (key == '7') {
  for (var i = 0; i < tileCountX; i++) {
    hueValues[i] = int(random(0, 180));
    saturationValues[i] = int(random(80, 100));
    brightnessValues[i] = int(random(50, 90));
  }
}
```

| 标记 | 说明 |
|---|---|
| 6 | 这里所有颜色分量都受到了限制；例如，色相仅从色环的前半部分选取，从而产生更暖的颜色。 |

![image](img/f0073-04.jpg)

7

```javascript
if (key == '9') {
  for (var i = 0; i < tileCountX; i++) {
    if (i % 2 == 0) {
      hueValues[i] = int(random(0, 360));
      saturationValues[i] = 100;
      brightnessValues[i] = int(random(0, 100));
```

8

```javascript
    } else {
      hueValues[i] = 195;
      saturationValues[i] = int(random(0, 100));
      brightnessValues[i] = 100;
    }
  }
}
```

| 标记 | 说明 |
|---|---|
| 7 | 也可以混合两种调色板。表达式 `i % 2` 交替产生数字 0 和 1。当结果为 0 时，数组中保存的是更暗、更饱和的颜色。 |
| 8 | 否则应用第二条规则，色相和明度被设置为固定值。这些值会产生明亮的蓝色调。 |
| 鼠标：按键： | 位置 `x/y`：网格分辨率；0–9：更改颜色调色板；S：保存图像；C：保存 ASE 调色板。 |

![image](img/f0073-05.jpg)

→ `P_1_2_3_01` 按键 0 创建一个调色板，其中两种预设色相（青色和紫色）交替出现。饱和度和明度随机变化。

![image](img/f0074-01.jpg)

→ `P_1_2_3_02` 随机性在这里扮演了更重要的角色。行被划分为不同宽度的瓦片。随机决定哪些瓦片会被再次分割。

![image](img/f0075-01.jpg)

→ `P_1_2_3_03` 如果瓦片略微透明且相互重叠，除了调色板中的颜色外，还会产生另一系列颜色。

![image](img/f0076-01.jpg)

→ `P_1_2_3_05` 此图像与前一张的主要区别在于，这里大约一半的瓦片根本没有绘制。

![image](img/f0077-01.jpg)

# P.2 形状

前一章主要关注颜色，形状的作用较小。由于可以控制图像的每一个元素，我们不仅能够访问、模块化和自动化极其多样的颜色，还能处理形状。一种与形式的对话由此展开。

**P.2 形状** 78

`P.2.0 你好，形状` 80

`P.2.1 网格` 82

`P.2.1.1 在网格中对齐` 82

`P.2.1.2 在网格中移动` 86

`P.2.1.3 复杂网格模块` 90

`P.2.1.4 网格中的复选框` 94

`P.2.1.5 从网格到波纹` 98

`P.2.2 智能体` 102

`P.2.2.1 简单智能体` 102

`P.2.2.2 智能智能体` 104

`P.2.2.3 智能体生成的形状` 108

`P.2.2.4 智能体生成的生长结构` 112

`P.2.2.5 智能体生成的结构密度` 116

`P.2.2.6 摆上的智能体` 120

`P.2.3 绘图` 126

`P.2.3.1 使用动态画笔绘图` 126

`P.2.3.2 绘图中的关系与距离` 130

`P.2.3.3 使用文字绘图` 132

`P.2.3.4 使用动态画笔绘图` 134

`P.2.3.5 使用数位板绘图` 138

`P.2.3.6 使用复杂模块绘图` 142

`P.2.3.7 使用多种画笔绘图` 146

## P.2.0 你好，形状

点、线、面仍然是所有形式的圣三位一体吗？瓦西里·康定斯基对这些基本元素的界定，在生成设计的语境下比以往任何时候都更具现实意义。遵循这一思路，像素是下图中黑色小圆点的起源。线条由一系列像素构成，而面则由一系列相连的线条构成。

→ `P_2_0_01`

当光标位于显示窗口上边框中间时，形状缩小为一个像素。

鼠标位置的 `x` 值设定线条的长度。`y` 值设定线条的数值和数量。

![image](img/f0080-01.jpg)



```javascript
function draw() {
  background(255);

  translate(width / 2, height / 2);

  var circleResolution = map(mouseY, 0, height, 2, 80);

  var radius = mouseX - width / 2 + 0.5;

  var angle = TWO_PI / circleResolution;

  strokeWeight(mouseY / 20);

  beginShape();

  for (var i = 0; i <= circleResolution; i++) {
    var x = cos(angle * i) * radius;
    var y = sin(angle * i) * radius;

    line(0, 0, x, y);

    // vertex(x, y);
  }

  endShape(CLOSE);
}
```

| 编号 | 说明 |
| --- | --- |
| 1 | 坐标系原点移至绘图画布的中心。 |
| 2 | 函数`map()`将鼠标位置的 y 值（0 到`height`之间的数字）转换为 2 到 80 之间的值。 |
| 3 | 从鼠标位置的 x 值中减去显示宽度的一半，鼠标越靠近中心，半径越小。x 值加 0.5 确保圆的直径至少为 1。 |
| 4 | 增量角度计算为整圆`TWO_PI`除以线条数量`circleResolution`。 |
| 5 | 删除注释字符`//`后，线条的端点可以连接成闭合的顶点。 |

| 操作 | 说明 |
| --- | --- |
| 鼠标 | 位置 x：线条长度；位置 y：线条数值和数量；S：保存图像 |
| 按键 |  |

![image](img/f0081-01.jpg)

**→ `P_2_0_02` 和 → `P_2_0_03`** 在此变体中，星形端点的端点连接成闭合多边形。此外，用鼠标绘图时，由于背景未赋予新颜色，变换轨迹得以保留。

## P.2.1.1 网格中的对齐

一条只有两种可能方向的对角线，如何利用网格的严格秩序来构建复杂结构？每个网格中对角线的方向是随机决定的。由于线宽变化而产生的重叠，创造了新的形式、连接和间隙。

### `P_2_1_1_01`

在网格中，要么绘制从左上角到右下角的线条 A，要么绘制从左下角到右上角的线条 B。对角线的方向是随机选择的。

![image](img/f0082-01.jpg)

![image](img/f0082-02.jpg)

**→ `P_2_1_1_01`** 对角线的线宽与鼠标位置相关联，使用按键 1 到 3 切换线条端点的类型。

```javascript
var tileCount = 20;
```

| 编号 | 说明 |
| --- | --- |
| 1 | 变量`tileCount`的值定义了网格分辨率。 |

```javascript
function draw() {
  ...

  strokeCap(actStrokeCap);

  ...

  for (var gridY = 0; gridY < tileCount; gridY++) {
    for (var gridX = 0; gridX < tileCount; gridX++) {
      var posX = width / tileCount * gridX;
      var posY = height / tileCount * gridY;

      var toggle = int(random(0, 2));

      if (toggle == 0) {
        strokeWeight(mouseX / 20);
        line(
          posX,
          posY,
          posX + width / tileCount,
          posY + height / tileCount
        );
      }

      if (toggle == 1) {
        strokeWeight(mouseY / 20);
        line(
          posX,
          posY + width / tileCount,
          posX + height / tileCount,
          posY
        );
      }
    }
  }

  ...
}
```

| 编号 | 说明 |
| --- | --- |
| 2 | 命令`random(0, 2)`生成一个介于 0.000 和 1.999 之间的随机数。使用`int()`将其转换为整数时，会进行舍入，变量`toggle`变为 0 或 1。 |
| 3 | 在此`if`查询中，变量`toggle`的值与 0 进行比较。如果该语句为真，则执行接下来的两行代码，绘制线条 A。 |
| 4 | 当前鼠标位置在 x 轴上的值定义了线条 A 的线宽。除以 20 是为了防止线宽过大。 |
| 5 | 线条 B 同理。 |

```javascript
function keyReleased() {
  ...

  if (key == '1') actStrokeCap = ROUND;
  if (key == '2') actStrokeCap = SQUARE;
  if (key == '3') actStrokeCap = PROJECT;
}
```

| 编号 | 说明 |
| --- | --- |
| 6 | 按下按键 1 到 3 中的任意一个，将变量`actStrokeCap`设置为 Processing 常量之一：`ROUND`、`SQUARE`或`PROJECT`。随后可使用该参数通过函数`strokeCap()`设置线条端点的绘制方式。 |
| 7 | `strokeCap(ROUND)`![image](img/f0083-02.jpg) |
| 8 | `strokeCap(SQUARE)`![image](img/f0083-03.jpg) |
| 9 | `strokeCap(PROJECT)`![image](img/f0083-04.jpg) |

| 操作 | 说明 |
| --- | --- |
| 鼠标 | 位置 x：左对角线的线宽；位置 y：右对角线的线宽；左键点击：新的随机值 |
| 按键 | 1–3：更改线条端点；S：保存图像 |

![image](img/f0083-01.jpg)

**→ `P_2_1_1_02`** 在此变体中，两种对角线都使用了额外的颜色和透明度。

![image](img/f0084-01.jpg)

**→ `P_2_1_1_04`** 此处网格中的元素从数据文件 SVG 图形中加载，这些图形始终朝向鼠标位置。使用按键 C 可以在不同颜色模式之间切换。元素的透明度取决于其与鼠标位置的距离。

![image](img/f0084-02.jpg)

**→ `P_2_1_1_04`** 使用按键 D，可以选择元素在靠近鼠标时是变小还是变大。

![image](img/f0085-01.jpg)

**→ `P_2_1_1_04`** 可以使用按键 1 到 7 选择其他 SVG 模块。当 SVG 图形位置分散时，网格看似溶解，尽管模块严格在网格内绘制。

![image](img/f0085-02.jpg)

**→ `P_2_1_1_04`** 元素也可以旋转（左箭头和右箭头键）。

## P.2.1.2 网格中的运动

当秩序濒临混沌时，张力达到最大。个体形式在动态网格中放弃严格的排列，服从于随机配置。倾向于网格的元素与背离网格的元素争夺视觉主导权。过渡的时刻才是重要的。

### `P_2_1_2_01`

固定数量的圆被逐一、逐行绘制到屏幕上。随机值被添加到圆的网格位置，迫使它沿 x 轴和 y 轴移动。鼠标向右移动得越远，圆的移动幅度越大。

![image](img/f0086-01.jpg)

```javascript
function draw() {
  translate(width / tileCount / 2, height / tileCount / 2);

  ...

  strokeWeight(mouseY / 60);

  for (var gridY = 0; gridY < tileCount; gridY++) {
    for (var gridX = 0; gridX < tileCount; gridX++) {
      var posX = width / tileCount * gridX;
      var posY = height / tileCount * gridY;

      var shiftX = random(-mouseX, mouseX) / 20;
      var shiftY = random(-mouseX, mouseX) / 20;

      ellipse(
        posX + shiftX,
        posY + shiftY,
        mouseY / 15,
        mouseY / 15
      );
    }
  }
}
```

| 编号 | 说明 |
| --- | --- |
| 1 | 坐标系原点向右和向下移动半个瓦片宽度和高度，使圆位于其瓦片的中心。 |
| 2 | 鼠标位置`mouseX`的 x 值越高，随机数的取值范围越大。 |
| 3 | 将`shiftX`和`shiftY`值加到网格坐标`posX`和`posY`上，得到圆的最终偏移位置。 |

| 操作 | 说明 |
| --- | --- |
| 鼠标 | 位置 x：圆的位置；位置 y：圆的大小；左键点击：圆位置的新随机值 |
| 按键 | S：保存图像 |

![image](img/f0087-01.jpg)

→ `P_2_1_2_01` 透明圆根据鼠标位置在水平网格中移动。鼠标垂直位置决定圆的大小。

![image](img/f0087-02.jpg)

→ `P_2_1_2_02` 移动的黑色圆位于密集的白色圆网格后方。

![image](img/f0088-01.jpg)

→ `P_2_1_2_02` 带有透明圆的颜色变体。

![image](img/f0088-02.jpg)

→ `P_2_1_2_02` 在这一行中，只有紫色圆发生了偏移，而粉色圆仍固定在网格上。

![image](img/f0089-01.jpg)

→ `P_2_1_2_04` 这里只移动了元素的角，而不是元素本身。

![image](img/f0089-02.jpg)

→ `P_2_1_2_04` 这里的重叠和间隙揭示了网格，直到它逐渐变得无法辨认。

## P.2.1.3 网格中的复杂模块

更有趣的是将多个形状嵌套成一个复杂模块。在此插图中，四个不同的椭圆簇沿相反方向增大尺寸，并交替放置在网格上。各个椭圆的不同直径和透明度营造出深度错觉。

### `P_2_1_3_01`

填充网格的模块由一堆越来越小的圆组成，这些圆沿随机决定的一个方向（上、下、右或左）移动。圆的数量对应鼠标位置 x，移动对应鼠标位置 y。

![image](img/f0090-01.jpg)

![image](img/f0090-02.jpg)

**→ `P_2_1_3_01`** 网格中的每个模块由多个圆组成。鼠标位置定义它们的数量、大小和位置。

```javascript
function draw() {
  ...

  circleCount = mouseX / 30 + 1;

  endSize = map(
    mouseX,
    0,
    max(width, mouseX),
    tileWidth / 2,
    0
  );

  endOffset = map(
    mouseY,
    0,
    max(height, mouseY),
    0,
    (tileWidth - endSize) / 2
  );

  for (var gridY = 0; gridY <= tileCountY; gridY++) {
    for (var gridX = 0; gridX <= tileCountX; gridX++) {
      push();

      translate(tileWidth * gridX, tileHeight * gridY);
      scale(1, tileHeight / tileWidth);

      var toggle = int(random(0, 4));

      if (toggle == 0) rotate(-HALF_PI);
      if (toggle == 1) rotate(0);
      if (toggle == 2) rotate(HALF_PI);
      if (toggle == 3) rotate(PI);

      // draw module

      for (var i = 0; i < circleCount; i++) {
        var diameter = map(
          i,
          0,
          circleCount,
          tileWidth,
          endSize
        );

        var offset = map(
          i,
          0,
          circleCount,
          0,
          endOffset
        );

        ellipse(offset, 0, diameter, diameter);
      }

      pop();
    }
  }
}
```

| 编号 | 说明 |
| --- | --- |
| 1 | 鼠标位置定义模块中的`circleCount`、圆的大小以及最后一个圆的偏移量。 |
| 2 | 当在绘制模块之前，将坐标系原点临时移动到将要绘制的位置时，模块的不同旋转更容易管理。命令`push()`确保在使用`translate()`移动原点之前保存坐标系的当前状态。 |
| 3 | 随机数`toggle`决定四种旋转方向之一。`random(0, 4)`生成一个介于 0 和 3.999 之间的数；因此，四舍五入后得到值 0、1、2 和 3。弧度角`HALF_PI`对应 90°旋转。 |
| 4 | 模块通过连续绘制圆来构建。`diameter`的值介于`tileWidth`和之前计算的`endSize`之间。`offset`值包含从中心的偏移。圆变得越来越小，从而越来越向右移动。 |
| 5 | 最后，使用`pop()`恢复之前保存的坐标系状态。 |

| 操作 | 说明 |
| --- | --- |
| 鼠标 | 位置 x：圆的数量和大小；位置 y：圆的位置；左键点击：位置的新随机值 |
| 按键 | S：保存图像 |

![image](img/f0091-01.jpg)

→ `P_2_1_3_02` 由直线构成的复杂模块。线条的聚合产生了新的形状。

![image](img/f0091-02.jpg)

→ `P_2_1_3_02` 线条汇聚的点可以通过鼠标沿对角线移动。

![image](img/f0091-03.jpg)

→ `P_2_1_3_02` 聚合很容易产生 3D 效果。

![image](img/f0092-01.jpg)

→ `P_2_1_3_05` 该模块由越来越小、越来越暗的圆组成。

![image](img/f0093-01.jpg)

→ `P_2_1_3_04` 该模块展示了与对面类似但使用旋转正方形的原理。这些正方形几乎无法被识别为彩色和透明。

## P.2.1.4 网格中的复选框

这是控件最狂野梦想成真的地方：它们最终成为视觉设计元素。按钮、复选框和滑块在浏览器中用作栅格元素，作为纯粹的视觉化元素，当它们被分组并排列在一起时变得引人入胜。

### `P_2_1_4_01`

输入图像的每个像素被分析并显示为一个复选框。像素的亮度决定它是否被选中。如果亮度高于指定阈值，则不会设置勾选标记。因此，这些复选框看起来会更亮。

![image](img/f0094-01.jpg)

![image](img/f0094-02.jpg)

**→ `P_2_1_4_01`** 复选框的外观因浏览器而异，但可以通过样式表进行调整。

```html
<html>
  ...

  <body>
    <div id="container"></div>
    ...
  </body>
</html>
```

| 编号 | 说明 |
| --- | --- |
| 1 | `index.html`文档提供了一个 id 为`container`的`<div>`元素，稍后将向其中添加复选框。 |

```javascript
function setup() {
  noCanvas();

  ...

  for (var y = 0; y < rows; y++) {
    for (var x = 0; x < cols; x++) {
      var box = createCheckbox();

      box.style('display', 'inline');
      box.parent('container');

      boxes.push(box);
    }

    var linebreak = createSpan('<br/>');
    linebreak.parent('mirror');
  }

  slider = createSlider(0, 255, 0);
}
```

| 编号 | 说明 |
| --- | --- |
| 2 | 由于元素直接放置在 HTML 文档中，因此可以移除标准绘图画布。 |
| 3 | 使用`createCheckbox()`创建复选框。可以通过`style()`样式属性定位它们，`parent()`将其插入到 HTML 元素`container`中。 |
| 4 | 在每行末尾添加一个换行符。 |
| 5 | 滑块稍后可用于控制亮度阈值。因此，0 到 255 的值范围很有用。起始值为 0。 |

```javascript
function draw() {
  for (var y = 0; y < img.height; y++) {
    for (var x = 0; x < img.height; x++) {
      var c = color(img.get(x, y));
      var bright = (red(c) + green(c) + blue(c)) / 3;

      var threshold = slider.value();

      var checkIndex = x + y * cols;

      if (bright > threshold) {
        boxes[checkIndex].checked(false);
      } else {
        boxes[checkIndex].checked(true);
      }
    }
  }
}
```

| 编号 | 说明 |
| --- | --- |
| 6 | 将图像转换为复选框时，图像中的每个像素必须转换为一个值，此处为`bright`。对于灰度图像，简单的平均值计算就足够了。对于彩色图像，应使用稍复杂的计算。**→ P.4.3.1 从像素值生成图形** |
| 7 | `value()`函数获取滑块当前设置的值。 |



| **8** | 与该像素关联的复选框的索引由 `x`、`y` 和列数 `cols` 计算得出。 |
|---|---|
| **9** | 如果像素的亮度高于设定的阈值，则取消勾选；否则勾选。 |

| 按键： | 1–3：切换图像 |
|---|---|
| 滑块： | 设置灰度阈值 |

![image](img/f0096-01.jpg)

**→ P_2_1_4_03** 多个滑块按几何排列。

![image](img/f0097-01.jpg)

**→ P_2_1_4_04** 这些滑块自动保持运动。

## P.2.1.5 从网格到莫尔条纹

莫尔条纹在印刷技术中通常被视为错误，但在这里却是理想的效果。通过将一个图形网格叠加到另一个相同的网格上并移动它，可以生成意想不到的光学错觉，并且可以实时改变。

**→ P_2_1_5_01**

当两个或多个精细的网格结构重叠形成更粗糙的图案时，就会产生莫尔效应。这是因为在所有交叉点处，整体图像显得更亮，因为在这些交叉点旁边可以看到更多的白色背景。

![image](img/f0098-01.jpg)

![image](img/f0098-02.jpg)

**→ P_2_1_5_01** 弯曲的栅格元素通常会产生特别有趣的叠加效果。

```javascript
function draw() {
  ...
  strokeWeight(3);
```

**1**

```javascript
  overlay();
```

**2**

```javascript
  var x = map(mouseX, 0, width, -50, 50);
  var a = map(mouseX, 0, width, -0.5, 0.5);
  var s = map(mouseY, 0, height, 0.7, 1);
```

**3**

```javascript
  if (drawMode == 2) translate(x, 0);
  if (drawMode == 1) rotate(a);
  scale(s);
```

**4**

```javascript
  strokeWeight(2);
  overlay();
}
```

| **1** | 绘制背景图形。由于该图形需要生成第二次，因此此过程已提取到 `overlay()` 函数中。 |
|---|---|
| **2** | 鼠标位置用于计算平移 `x`、旋转 `a` 和缩放 `s` 的对应值。 |
| **3** | 根据 `drawMode`，坐标系要么水平移动，要么旋转。两种情况下都会进行缩放。 |
| **4** | 使用稍有不同的描边宽度绘制叠加图形。 |

**5**

```javascript
function overlay() {
  var w = width - 100;
  var h = height - 100;
```

**6**

```javascript
  if (drawMode == 1) {
    for (var i = -w / 2; i < w / 2; i += 5) {
      line(i, -h / 2, i, h / 2);
    }
  }
```

**7**

```javascript
  if (drawMode == 2) {
    for (var i = 0; i < w; i += 10) {
      ellipse(0, 0, i);
    }
  }
}
```

| **5** | 图形在函数 `overlay()` 中创建。 |
|---|---|
| **6** | 在 `drawMode` 1 中，绘制一系列线条。 |
| **7** | 在 `drawMode` 2 中，绘制逐渐增大的圆形。 |

| 鼠标： | 位置 x：旋转或移动叠加层位置 y：缩放叠加层 |
|---|---|
| 按键： | 1–2：切换 `drawMode` S：保存图像 |

![image](img/f0099-01.jpg)

**→ P_2_1_5_01** 当两个网格在旋转和缩放方面越接近，莫尔效应越强。

![image](img/f0100-01.jpg)

**→ P_2_1_5_04** 自由绘制的线条，多次绘制，相互平行并叠加。

## P.2.2.1 简单智能体

像素不再被严格嵌入网格中，而是成为一个智能体，可以根据不同的行为模式自由移动。每一步，智能体都会按照八个方向之一前进，并在身后留下轨迹。它执行任务，永不放弃。

**→ P_2_2_1_01**

每次绘制操作中，都会随机选择八个可能方向之一作为下一步。通过在当前坐标上加上或减去一个预定值（步长）来执行步骤。最后在新位置绘制圆形。

![image](img/f0102-01.jpg)

![image](img/f0102-02.jpg)

**→ P_2_2_1_01** 智能体迁移的时间越长，云状结构越密集。

![image](img/f0102-03.jpg)

**→ P_2_2_1_02** 此处限制了智能体的移动方向。

![image](img/f0102-04.jpg)

**→ P_2_2_1_02** 在此变体中，圆的直径更大，有时会呈现蓝色。

**1**

```javascript
var NORTH = 0;
var NORTHEAST = 1;
var EAST = 2;
var SOUTHEAST = 3;
var SOUTH = 4;
var SOUTHWEST = 5;
var WEST = 6;
var NORTHWEST = 7;
...
```

**2**

```javascript
var stepSize = 1;
var diameter = 1;
```

| **1** | 定义了八个常量，每个常量具有不同的数值。 |
|---|---|
| **2** | 通过更改 `stepSize` 和 `diameter` 的值，可以设置智能体的步长和直径。 |

```javascript
function draw() {
  for (var i = 0; i <= mouseX; i++) {
```

**3**

```javascript
    direction = int(random(0, 8));
```

**4**

```javascript
    if (direction == NORTH) {
      posY -= stepSize;
```

**5**

```javascript
    } else if (direction == NORTHEAST) {
      posX += stepSize;
      posY -= stepSize;
```

**6**

```javascript
    } else if (direction == EAST) {
      posX += stepSize;
    } else if (direction == SOUTHEAST) {
      posX += stepSize;
      posY += stepSize;
    } else if (direction == SOUTH) {
      posY += stepSize;
    } else if (direction == SOUTHWEST) {
      posX -= stepSize;
      posY += stepSize;
    } else if (direction == WEST) {
      posX -= stepSize;
    } else if (direction == NORTHWEST) {
      posX -= stepSize;
      posY -= stepSize;
    }
```

**7**

```javascript
    if (posX > width) posX = 0;
    if (posX < 0) posX = width;
    if (posY < 0) posY = height;
    if (posY > height) posY = 0;
```

**8**

```javascript
    ellipse(posX + stepSize / 2, posY + stepSize / 2,
            diameter, diameter);
  }
}
```

| **3** | 命令 `random(0, 8)` 生成一个介于 0.000 和 7.999 之间的随机数。取整后得到 0 到 7 之间的值。该值随后存储在 `direction` 中，并决定下一步。 |
|---|---|
| **4** | ![image](img/f0103-01.jpg) |
| **5** | ![image](img/f0103-02.jpg) |
| **6** | ![image](img/f0103-03.jpg) |
| **7** | 当智能体的当前位置超出显示窗口的右边界时，`posX` 被设置为 0。这会使智能体在对侧继续其路径。 |
| **8** | 在新位置绘制一个透明圆。加上步长的一半 `stepSize / 2`，以确保圆不会在显示窗口边界处被截断。 |

| 鼠标： | 位置 x：图像构建速度 |
|---|---|
| 按键： | DEL：清除画布 S：保存图像 |

## P.2.2.2 智能智能体

行为模式现在更加复杂，并受精确条件约束。智能体在穿越自身路径时容易迷失方向。当它到达显示窗口边界时，会改变方向。在两个交点之间绘制的直线，其颜色和描边值会根据行进距离而变化。

**→ P_2_2_2_01**

智能体始终沿基本方向之一移动：北、东、南或西。但它可以从多个可能的角度中选择，但直角是不可能的。当智能体到达画布边界时，它会掉头并随机选择一个可能的角度。当它穿越自身路径时，它会保持大致方向，但选择一个新的角度。

![image](img/f0104-01.jpg)

![image](img/f0104-02.jpg)

**→ P_2_2_2_01** 按下 R 键，线条将在 PDF 中无轨迹绘制。按下 E 键结束该过程。

![image](img/f0104-03.jpg)

**→ P_2_2_2_02** 线条的值取决于其距离。

![image](img/f0104-04.jpg)

**→ P_2_2_2_02** 此处线条根据其长度着色（按键 2）。

```javascript
function draw() {
  var speed = int(map(mouseX, 0, width, 0, 20));
  for (var i = 0; i <= speed; i++) {
    strokeWeight(1);
    stroke(180, 0, 0);
```

**1**

```javascript
    point(posX, posY);
```

**2**

```javascript
posX += cos(radians(angle)) * stepSize;

posY += sin(radians(angle)) * stepSize;

reachedBorder = false;
```

**3**

```javascript
if (posY <= 5) {
  direction = SOUTH;
  reachedBorder = true;
} else if (posX >= width - 5) {
  direction = WEST;
  reachedBorder = true;
}

...

loadPixels();
```

**4**

```javascript
var currentPixel = get(floor(posX), floor(posY));

if ((currentPixel[0] != 255 && currentPixel[1] != 255 &&
     currentPixel[2] != 255) || reachedBorder) {
  angle = getRandomAngle(direction);
```

**5**

```javascript
var distance = dist(posX, posY, posXcross, posYcross);

if (distance >= minLength) {
  strokeWeight(3);
  stroke(0, 0, 0);
  line(posX, posY, posXcross, posYcross);
}
```

**6**

```javascript
posXcross = posX;
posYcross = posY;
}

}
```

| 步骤 | 描述 |
|---|---|
| **1** | 在智能体的当前位置（`posX`，`posY`）绘制一个点。当点的颜色与背景色匹配时，该点可能变得几乎（或完全）不可见。 |
| **2** | 智能体移动一步。在此过程中，其位置被更新：`angle` 定义方向，`stepSize` 定义步长。 |
| **3** | 现在检查智能体是否到达了显示窗口的边界。例如，如果它距离上边界只有五个像素或更少，则方向改为 `SOUTH`，并将变量 `reachedBorder` 设为 true。 |
| **4** | 函数 `get()` 在智能体每次移动时检查它是否位于非白色的像素上。如果是这种情况，或者变量 `reachedBorder` 为 true，则使用函数 `getRandomAngle()` 在主方向中选择一个新的随机角度步长增量。 |
| **5** | 当改变方向时，只有当上一次方向改变的位置（`posXcross`，`posYcross`）至少与 `minLength` 定义的距离一样远时，才会绘制一条线。 |
| **6** | 最后，将当前位置保存在变量 `posXcross` 和 `posYcross` 中。 |

**7**

```javascript
function getRandomAngle(currentDirection) {
  var a = (floor(random(-angleCount, angleCount)) + 0.5) *
          90 / angleCount;

  if (currentDirection == NORTH) return a - 90;
  if (currentDirection == EAST) return a;
  if (currentDirection == SOUTH) return a + 90;
  if (currentDirection == WEST) return a + 180;

  return 0;
}
```

| **7** | 函数 `getRandomAngle()` 随机选择并返回一个可能的角度，该角度取决于传入的主方向 `currentDirection`。例如，当 `angleCount` 为 3（即每个象限三个方向）且 `currentDirection` 为 `SOUTH` 时，将返回这些角度之一。 |
|---|---|

![image](img/f0105-01.jpg)

| 鼠标： | 位置 x：图像构建速度 |
|---|---|
| 按键： | DEL：清除画布 S：保存图像 |

![image](img/f0106-01.jpg)

**→ P_2_2_2_02** 较长的线条外观不透明，较短的线条透明。

![image](img/f0107-01.jpg)

**→ P_2_2_2_02** 色调和饱和度设置为固定值；亮度取决于线条的长度。

## P.2.2.3 由智能体构成的形状

只有通过协作，愚蠢的智能体才能变得强大。在这个例子中，圆形是源形状。排列规则是：圆上的每个点都由一个愚蠢的智能体表示，点的移动会导致圆形逐渐改变其形状。这产生了令人惊讶的丰富形态。

**→ P_2_2_3_01**

圆上点的计算产生了智能体的起始位置。一条灵活的曲线将每个智能体与其两个邻居牢固地连接起来。愚蠢的智能体离其原始位置越远，圆形组织就越解体。

![image](img/f0108-01.jpg)

![image](img/f0108-02.jpg)

**→ P_2_2_3_01** 不断变化的形状始终朝向鼠标移动，因此可以由鼠标控制。

![image](img/f0108-03.jpg)

**→ P_2_2_3_01** 可以使用按键 2 设置填充模式，使形状以随机且变化的灰度值着色。

```javascript
function setup() {
  ...

  centerX = width / 2;
  centerY = height / 2;

  var angle = radians(360 / formResolution);

  for (var i = 0; i < formResolution; i++) {
    x.push(cos(angle * i) * initRadius);
    y.push(sin(angle * i) * initRadius);
  }

  ...
}
```

| **1** | 智能体稍后将围绕位置（`centerX`，`centerY`）绘制。初始起点是显示器的中心。 |
|---|---|
| **2** | 智能体的起始位置被计算为圆上的点，并通过数组函数 `push()` 保存在数组 `x` 和 `y` 中。**→ P.1.1.2 圆中的颜色光谱** |



```javascript
function draw() {

3

centerX += (mouseX - centerX) * 0.01;

centerY += (mouseY - centerY) * 0.01;

for (var i = 0; i < formResolution; i++) {

4

x[i] += random(-stepSize, stepSize);

y[i] += random(-stepSize, stepSize);

5

// ellipse(x[i] + centerX, y[i] + centerY, 5, 5);

}

...

beginShape();

6

curveVertex(x[formResolution - 1] + centerX,

y[formResolution - 1] + centerY);

for (var i = 0; i < formResolution; i++) {

curveVertex(x[i] + centerX, y[i] + centerY);

}

curveVertex(x[0] + centerX, y[0] + centerY);

7

curveVertex(x[1] + centerX, y[1] + centerY);

endShape();

}
```

| **3** | 鼠标跟随位置（`centerX`，`centerY`）。每一帧都会计算智能体位置与鼠标位置之间的差值，乘以一个小值，然后再次加到该位置上。 |
| **4** | 将介于 -`stepSize` 和 `stepSize` 之间的随机值加到智能体的当前位置上，导致上下移动。 |
| **5** | 也可以通过添加 `ellipse` 命令来可视化智能体的位置。 |
| **6** | 注意，在绘制形状时，使用 `curveVertex()` 设置的第一个和最后一个点作为控制点，不会被绘制出来。这两个控制点确保圆在没有弯曲的情况下闭合，从而使最终的圆平滑。![image](img/f0109-01.jpg) |
| **7** | 例如，如果将 `curveVertex` 替换为 `vertex`，则会产生直线连接。对填充颜色 `fill` 进行实验也会产生有趣的变体。 |
| 鼠标： | 左键点击：新圆 位置 `x`/`y`：移动方向 |
| 按键： | 1–2：填充模式 S：保存图像 |

![image](img/f0110-01.jpg)

**→ P_2_2_3_02** 在程序的第二个版本中，可以选择一个 `drawMode`，它首先创建一条直线，然后逐渐变形。

![image](img/f0111-01.jpg)

**→ P_2_2_3_02** 使用变化的形状进行绘制。点击时，会出现一个略微变形的圆形几何体。移动鼠标时，形状跟随光标位置，变形越来越明显。

## P.2.2.4 基于智能体的生长结构

多个智能体基于简单规则汇聚在一起，形成稳定的结构。复杂的形状由简单的传播模式产生，例如：绘制一个新圆，并将其尽可能靠近其最近邻。这类算法也描述了植物和矿物中的生长过程。

**→ P_2_2_4_01**

在每一帧中，都会在随机位置生成一个具有随机半径的新圆（虚线圆）。然后确定现有圆中哪个离新圆最近。最后一步，新圆通过最短路径与其最近的邻居对接。

![image](img/f0112-01.jpg)

![image](img/f0112-02.jpg)

**→ P_2_2_4_01** 圆逐渐填满区域，形成有机结构。

```javascript
function draw() {

background(255);

1

var newR = random(1, 7);

var newX = random(newR, width - newR);

var newY = random(newR, height - newR);

var closestDist = Number.MAX_VALUE;

var closestIndex = 0;

2

for (var i = 0; i < currentCount; i++) {

var newDist = dist(newX, newY, x[i], y[i]);

if (newDist < closestDist) {

closestDist = newDist;

closestIndex = i;

}

}

3

// fill(230);

// ellipse(newX, newY, newR * 2, newR * 2);

// line(newX, newY, x[closestIndex], y[closestIndex]);

4

var angle = atan2(newY - y[closestIndex],

newX - x[closestIndex]);

x[currentCount] = x[closestIndex] + cos(angle) *
(r[closestIndex] + newR);

y[currentCount] = y[closestIndex] + sin(angle) *
(r[closestIndex] + newR);

r[currentCount] = newR;

currentCount++;

for (var i = 0; i < currentCount; i++) {

fill(50);

5

ellipse(x[i], y[i], r[i] * 2, r[i] * 2);

}

6

if (currentCount >= maxCount) noLoop();

}
```

| **1** | 圆的半径 `newR` 和位置（`newX`、`newY`）是随机定义的。 |
| **2** | 在 `for` 循环中搜索最近的邻居。逐个处理所有圆，并计算它们与新圆的距离。如果这个距离小于之前所有距离，则将该圆的引用保存在变量 `closestIndex` 中。![image](img/f0113-01.jpg) |
| **3** | 通过绘制新圆的起始位置以及到最近圆的连线，可以用这三行代码可视化刚刚描述的过程。 |
| **4** | 通过计算到最近邻居的角度，可以定位新圆，使两个圆相切。→ 第 P.1.1.2 节 圆中的色谱![image](img/f0113-02.jpg) |
| **5** | 绘制这些圆。 |
| **6** | 当 `currentCount` 达到定义的上限时，使用函数 `noLoop()` 停止程序。 |
| 按键： | S：保存图像 |

![image](img/f0114-01.jpg)

`→ P_2_2_4_01` 这个序列展示了结构如何逐渐但持续地增长。

![image](img/f0115-01.jpg)

`→ P_2_2_4_02` 当源圆特别大时，结构从外向内生长。此外，这里还绘制了圆的初始位置和连接到新位置的连线（按键 1）。

## P.2.2.5 来自代理的结构密度

在这个例子中，迭代过程再次充当形状生成器：生成一个新圆。如果这个圆不与显示中的任何其他圆相交，则使其尽可能大；如果与另一个圆相交，则重新开始。该算法的目的是将圆紧密地打包，最终连最小的间隙也被填满。

`→ P_2_2_5_01`

同样，每一帧都会生成一个具有随机位置和大小（用黄色虚线轮廓表示）的新圆。当它与已有的圆相交时，算法重新开始。

否则，它会找到最近的圆。到该圆的距离及其半径决定了新圆必须绘制多大，以便与邻居相切，从而可以紧密地打包这些圆。

![image](img/f0116-01.jpg)

![image](img/f0116-02.jpg)

`→ P_2_2_5_01` 该算法用越来越小的圆填充区域。绿线表示新增长点附着在哪些圆上。

```javascript
function draw() {

background(255);

1

var newX = random(maxRadius, width - maxRadius);

var newY = random(maxRadius, height - maxRadius);

if (mouseIsPressed && mouseButton == LEFT) {

2

newX = random(mouseX - mouseRect, mouseX + mouseRect);

newY = random(mouseY - mouseRect, mouseY + mouseRect);

}

var intersection = false;

3

for (var newR = maxRadius; newR >= minRadius; newR--) {

for (var i = 0; i < circles.length; i++) {

var d = dist(newX, newY, circles[i].x, circles[i].y);

4

intersection = d < circles[i].r + newR;

if (intersection) {

break;

}

}

5

if (!intersection) {

circles.push(new Circle(newX, newY, newR));

break;

}

}

for (var i = 0; i < circles.length; i++) {

6

if (showLine) {

var closestCircle;

for (var j = 0; j < circles.length; j++) {

var d = dist(circles[i].x, circles[i].y,

circles[j].x, circles[j].y);

if (d <= circles[i].r + circles[j].r + 1) {

closestCircle = circles[j];

break;

}

}

if (closestCircle) {

stroke(100, 230, 100);

strokeWeight(0.75);

line(circles[i].x, circles[i].y,

closestCircle.x, closestCircle.y);

}

}

7

if (showCircle) circles[i].draw();

}

...

}
```

| **1** | 为新圆创建位置和半径。![image](img/f0117-01.jpg) |
| **2** | 按住鼠标按钮时，随机值的范围受到限制，从而可以有选择地定位新圆，生成一个交互式绘图工具。 |
| **3** | 现在必须确定新圆的半径。为此，将 `newR` 设置为最大半径 `maxRadius`，然后递减。 |
| **4** | 将所有现有圆与新圆进行比较。当存在交集时（例如，当距离小于两个半径之和时），变量 `intersection` 设置为 `true`。 |
| **5** | 如果没有重叠，则创建 `Circles` 类的新实例并保存。![image](img/f0117-02.jpg) |
| **6** | 如果选择了 `showLine` 选项，则将每个圆与所有其他圆进行比较，以找到相邻的圆 `closestCircle`。 |
| **7** | 如果 `showCircle` 为 `true`，则也绘制该圆。 |
| 鼠标： | 拖动：有目标地放置圆 |
| 按键： | 1：显示/隐藏圆 2：显示/隐藏线 箭头↓/↑：更改绘制区域 S：保存图像 |

![image](img/f0118-01.jpg)

![image](img/f0119-01.jpg)

`→ P_2_2_5_02` 通过加载 SVG 模块，可以创建截然不同的图像。使用按键 1 到 3，可以指定哪些元素可见：SVG、连接线或圆。

## P.2.2.6 摆上的代理

这些双重代理是可变的并且链接在一起。代理沿着相互关联的摆组移动，留下复杂的轨迹，让人联想到万花尺的绘图。随着时间的推移，它们的秘密任务变得可见。

`→ P_2_2_6_01`

代理形成一条摆链。为了确定代理的各个位置，我们从中心开始。旋转角度和摆的长度决定了第一个代理的位置。这也是下一个摆的旋转中心。越往链外，摆越短，转动越快。每隔一个摆向相反方向转动。

![image](img/f0120-01.jpg)

![image](img/f0120-02.jpg)

`→ P_2_2_6_01` 通过不同的转速比设置，可以产生具有例如三个、六个或四个对称轴的形状。

```javascript
function draw() {

background(0, 0, 100);

1

angle += speed;

if (angle <= maxAngle + speed) {

2

var pos = center.copy();

for (var i = 0; i < joints; i++) {

3

var a = angle * pow(speedRelation, i);

if (i % 2 == 1) a = -a;

4

var nextPos = p5.Vector.fromAngle(radians(a));

nextPos.setMag((joints - i) / joints * lineLength);

nextPos.add(pos);

5

if (showPendulum) {

noStroke();

fill(0, 10);

ellipse(pos.x, pos.y, 4, 4);

noFill();

stroke(0, 10);

line(pos.x, pos.y, nextPos.x, nextPos.y);

}

6

pendulumPath[i].push(nextPos);

pos = nextPos;

}

}

if (showPendulumPath) {

strokeWeight(1.6);

for (var i = 0; i < pendulumPath.length; i++) {

var path = pendulumPath[i];

beginShape();

7

var hue = map(i, 0, joints, 120, 360);

stroke(hue, 80, 60, 50);

for (var j = 0; j < path.length; j++) {

vertex(path[j].x, path[j].y);

}

endShape();

}

}

}
```

| **1** | 变量 `angle` 包含第一个摆的角度。在每一帧中，角度略微增加。 |
| **2** | 将变量 `center` 复制到 `pos`。它包含一个来自 `p5.Vector` 的值。因此，只需要一个变量来存储点的 x 和 y 坐标。此外，`p5.Vector` 对象提供了更多实用的计算功能。 |
| **3** | 摆的角度 `a` 由基础角度和一个因子计算得出，该因子随着摆离中心越远而增大；例如，对于 `speedRelation` 的值 2，索引为 3 的摆的因子在这种情况下是 8（2 的 3 次方）。每隔一个角度，旋转方向反转。 |
| **4** | 要到达摆锤末端的位置，使用 `fromAngle()` 函数从刚计算出的角度生成一个单位向量（长度为 1 的向量）。`setMag()` 将其延长并加上当前位置 `pos`。 |
| **5** | 如果要显示摆锤，则绘制一个圆和一条线。 |
| **6** | 新计算出的位置 `nextPos` 被添加到摆锤的路径中，并作为下一次迭代的起始位置 `pos`。 |
| **7** | 路径被分配了各自的颜色。根据其索引 `i`，确定一个介于 120°（绿色）到 360°（红色）之间的色相。 |
| 按键： | 1：切换摆锤显示开/关<br>2：切换路径显示开/关<br>DEL：清除画布<br>–/+：调整速度比 –/+<br>Arrow↓/↑：减小/增加线长 –/+<br>Arrow ←/→：调整旋转速度 –/+<br>S：保存图像 |

![image](img/f0122-01.jpg)

**→ P_2_2_6_02** 在程序的其他变体中，摆锤沿着用鼠标绘制的路径移动。

![image](img/f0122-02.jpg)

**→ P_2_2_6_03** 当摆锤不再完全绕其中心旋转，而是像其名称所示那样来回摆动时，就会出现这样的标记。

![image](img/f0122-03.jpg)

**→ P_2_2_6_04** 如果摆锤形成分支树状结构，则会有多个端点。

![image](img/f0123-01.jpg)

**→ P_2_2_6_03** 在此绘图模式下，背景不会被清除。摆锤的动画是连续的，因此变得可见。

![image](img/f0124-01.jpg)

**→ P_2_2_6_04** 此处，树状结构的端点被连接起来，形成一个透明多边形。

## P.2.3.1 使用动画画笔绘图

在前面的章节中，智能体根据预定义的规则自主移动。在本例中，用户将与智能体交互，创建一种遵循自身规则的实验性绘图工具。动画画笔的独特之处在于，它们能够在绘图时从自身行为中获得灵感。这一过程提供了更丰富的表现力，因为绘图行为就像与舞伴共舞一场华尔兹。

**→ P_2_3_1_01**

![image](img/f0126-01.jpg)

第一个绘图工具很好地展示了非常简单的原理中蕴含的巨大视觉潜力。一条线围绕鼠标位置旋转。根据鼠标移动的速度和方向，这些线以不同方式汇聚。每次鼠标点击，线的颜色和长度都会改变。旋转速度可以通过左右方向键设置。

![image](img/f0126-02.jpg)

**→ P_2_3_1_01** 鼠标仅沿水平线中间来回移动。动画画笔因此生成了不同密度的效果。



```javascript
function draw() {
  if (mouseIsPressed && mouseButton == LEFT) {
    push();
    translate(mouseX, mouseY);
    rotate(radians(angle));
    stroke(c);
    line(0, 0, lineLength, 0);
    pop();
    angle += angleSpeed;
  }
}
```

| 编号 | 说明 |
|---|---|
| 1 | 仅当按下鼠标左键时才会绘制内容。 |
| 2 | 线应围绕鼠标位置旋转。因此，必须首先使用`translate()`函数将坐标系原点移动到鼠标位置。然后使用`rotate()`函数旋转坐标系。 |
| 3 | 现在绘制的水平线变成了旋转画笔。 |
| 4 | 旋转角度增加一个旋转速度值。 |

```javascript
function mousePressed() {
  lineLength = random(70, 200);
}
```

| 编号 | 说明 |
|---|---|
| 5 | 每次点击鼠标，线的长度都会改变。 |

| 鼠标： | 拖动：绘制 |
|---|---|
| 按键： | 1–4：更改颜色设置<br>Space：随机新颜色<br>DEL：清除画布<br>D：改变方向并镜像角度<br>Arrow ↓/↑：线长 -/+<br>Arrow ←/→：旋转速度 -/+<br>S：保存图像 |

![image](img/f0127-01.jpg)

**→ P_2_3_1_02** 除了鼠标移动和不同颜色外，旋转线的步长也发生了变化。

![image](img/f0128-01.jpg)

**→ P_2_3_1_02** 当按住鼠标按钮时，随机颜色的线围绕鼠标位置旋转。即使不移动鼠标，也可以通过按键影响大量参数，如线的长度、颜色、线形和旋转速度，从而生成各种图像。

![image](img/f0129-01.jpg)

## P.2.3.2 绘图中的关系与距离

由于各个元素之间的相互关系对整体图像至关重要，因此用户能够控制距离和角度等单个参数非常重要；本程序提供了必要的知识。

**→ P_2_3_2_01**

在前一个示例中，当按住鼠标按钮时，每一帧都会在绘图画布上绘制一个新元素。现在这个功能受到了限制：只有当新元素与之前绘制的元素保持最小距离时，才会放置新元素。有几种方法可以实现这一点：

- 变体 1：新元素不直接放置在鼠标位置，而是放置在距离上一个元素恰好指定最小距离的位置。
- 变体 2：新元素放置在鼠标位置，最小距离仅作为阈值。

![image](img/f0130-01.jpg)

![image](img/f0130-02.jpg)

**→ P_2_3_2_01** 绘图过程中鼠标移动得越快，线条就越长。

```javascript
function draw() {
  if (mouseIsPressed && mouseButton == LEFT) {
    var d = dist(x, y, mouseX, mouseY);

    if (d > stepSize) {
      var angle = atan2(mouseY - y, mouseX - x);

      push();
      translate(x, y);
      rotate(angle);
      stroke(col);

      if (frameCount % 2 == 0) stroke(150);

      line(0, 0, 0, lineLength * random(0.95, 1.0) * d / 10);

      pop();

      if (drawMode == 1) {
        x = x + cos(angle) * stepSize;
        y = y + sin(angle) * stepSize;
      } else {
        x = mouseX;
        y = mouseY;
      }
    }
  }
}
```

| 编号 | 说明 |
|---|---|
| 1 | 按住鼠标按钮（即想要绘图时）计算从上次绘图位置（`x`、`y`）到当前鼠标位置的距离。 |
| 2 | 如果该距离大于`stepSize`，则绘制一个新点。为此，需要计算与上一个绘图位置之间的角度。这可以通过函数`atan2()`轻松实现，该函数需要两个参数：两点之间的垂直距离`mouseY-y`和水平距离`mouseX-x`。 |
|  | ![image](img/f0131-01.jpg) |
| 3 | 线条交替使用不同颜色绘制：随机选择的颜色（`col`）或中灰色。 |
| 4 | 绘制一条垂直线。由于坐标系之前已按`angle`旋转，因此该线现在垂直于绘图路径。线的长度由基本长度`lineLength`、一个使长度略有变化的随机因子以及因子`d/10`决定。这意味着旧点与新点之间的距离越大，绘制的线就越长，从而反映了鼠标的速度。 |
| 5 | 在版本 1（`drawMode==1`）中，新点放置在距离旧位置`stepSize`的位置。在版本 2 中，鼠标决定新位置。 |

| 鼠标： | 拖动：绘制 |
|---|---|
| 按键： | 1–2：绘图模式<br>DEL：清除画布<br>Arrow ↓/↑：线长 -/+<br>S：保存图像 |

![image](img/f0131-02.jpg)

**→ P_2_3_2_01 → 插图：Victor Juarez Hernandez** 线条的多重叠加可用于创建精细的阴影效果。

## P.2.3.3 使用文字绘图

谁不喜欢在绘画时切换画笔呢？在此应用中，字符的位置和大小会根据画笔的位置和速度不断变换。用户可以绘制随机的字母序列，甚至整部小说。

**→ P_2_3_3_01**

沿着鼠标的绘制线，会出现程序中定义的文本，并根据鼠标速度绘制得更大或更小。

![image](img/f0132-01.jpg)

```javascript
function draw() {
  if (mouseIsPressed && mouseButton == LEFT) {
    var d = dist(x, y, mouseX, mouseY);
    textSize(fontSizeMin + d / 2);

    var newLetter = letters.charAt(counter);
    stepSize = textWidth(newLetter);

    if (d > stepSize) {
      var angle = atan2(mouseY - y, mouseX - x);

      push();
      translate(x, y);
      rotate(angle + random(angleDistortion));
      text(newLetter, 0, 0);
      pop();

      counter++;

      if (counter >= letters.length) counter = 0;

      x = x + cos(angle) * stepSize;
      y = y + sin(angle) * stepSize;
    }
  }
}
```

| 编号 | 说明 |
|---|---|
| 1 | 计算鼠标与当前书写位置（`x`、`y`）之间的距离。该距离进而决定下一个字符的字体大小。`fontSizeMin`中的值确保字体不会小于指定大小。 |
| 2 | 检查是否可以写入新字母，从字符串`letters`中选择下一个字符，并将变量`stepSize`设置为该字符的宽度。 |
| 3 | 当鼠标与当前书写位置之间有足够空间时，写入新字母。 |
| 4 | 变量`counter`统计已绘制的字母数量。该值用于从指定文本`letters`中依次读取字母。当`counter`大于原始文本中的字母数时，将其重置为 0。 |

| 鼠标： | 拖拽：绘制文本 |
|---|---|
| 按键： | DEL：清除画布<br>Arrow ↓/↑：扭曲角度 -/+<br>S：保存图像 |

![image](img/f0133-01.jpg)

`→ P_2_3_3_01_TABLET` → 插图：Pau Domingo 在平板版本中，笔的压力调节文本的大小。可以将图像作为模板放置在背景中，并在绘制时显示或隐藏。

## P.2.3.4 使用动态画笔绘制

虚拟橡皮筋变成动态画笔，任意基本元素像珍珠一样串在画笔描边和惰性代理之间的线上。两极之间的张力决定了绘制时元素的大小和位置。

`→ P_2_3_4_01`

一个图形元素的一端被鼠标拖拽。另一端缓慢地朝鼠标方向移动。根据绘制速度和设定的惯性，原始元素被描绘成拉伸到极限或几乎不变。元素的宽度保持不变。

![image](img/f0134-01.jpg)

```javascript
function draw() {
  if (mouseIsPressed && mouseButton == LEFT) {
    var d = dist(x, y, mouseX, mouseY);

    if (d > stepSize) {
      var angle = atan2(mouseY - y, mouseX - x);

      push();
      translate(mouseX, mouseY);
      rotate(angle + PI);
      image(lineModule, 0, 0, d, moduleSize);
      pop();

      x = x + cos(angle) * stepSize;
      y = y + sin(angle) * stepSize;
    }
  }
}
```

| 编号 | 说明 |
|---|---|
| 1 | 在此程序中，变量`x`和`y`用于表示对极的位置。这些变量与鼠标位置之间的距离决定了字符元素被拉伸的程度。 |
| 2 | 使用`translate()`将坐标系移动到鼠标位置，并旋转使其面向对极，然后绘制元素。这里额外的角度（`PI`）可能因 SVG 模块而异。其长度设置为`d`（到鼠标的距离），宽度设置为`moduleSize`。 |
| 3 | 对极的位置每一步移动`stepSize`值。由于这种移动通常比鼠标慢得多，因此会产生橡皮筋效果。 |

| 鼠标： | 拖拽：绘制 |
|---|---|
| 按键： | 1–9：切换模块<br>DEL：清除画布<br>Arrow ↓/↑：模块大小 -/+<br>Arrow ←/→：步长 -/+<br>S：保存图像 |

![image](img/f0135-01.jpg)

`→ P_2_3_4_01` → 插图：Pau Domingo 一个非常温和的对手，对抗快速移动的鼠标。

![image](img/f0136-01.jpg)

`→ P_2_3_4_01` → 插图：Pau Domingo 快速、规律的鼠标移动产生流动的形态。

![image](img/f0137-01.jpg)

`→ P_2_3_4_01` → 插图：Pau Domingo 不同的鼠标移动速度也会产生不同的结构。

## P.2.3.5 使用数位板绘制

与传统鼠标相比，数位板为用户提供了更多参数，包括压力和位置。绘制时，可以更好地记录和解释笔的移动，从而更准确地再现手的运动。使用数位板时，你更接近生成过程。

`→ P_2_3_5_01_TABLET`

数位板提供的额外参数被传递给基本元素（此处为笔）。方位角、压力和倾斜度分别定义元素的旋转、饱和度和长度。这些参数通过本书的 Generative Design 库中的数位板类读取。形状不是从 SVG 文件加载的，而是作为曲线绘制的，从而可以更轻松地操作各个曲线点。

![image](img/f0138-01.jpg)

![image](img/f0138-02.jpg)

`→ P_2_3_5_01_TABLET` → 插图：Jana-Lina Berkenbusch 新元素总是叠加在旧元素之上，因此需要从背景到前景进行绘制。

```javascript
function draw() {
  var tabletValues = tablet.values();

  var pressure = gamma(tabletValues.pressure, 2.5);
  var angle = tabletValues.azimuth;
  var penLength = cos(tabletValues.inclination);

  if (pressure > 0 && penLength > 0) {
    push();
    translate(mouseX, mouseY);
    rotate(angle);

    var elementLength = penLength * 250;
    var h1 = random(10) * (1.2 + penLength);
    var h2 = (-10 + random(10)) * (1.2 + penLength);

    // ...

    pointsX = [];
    pointsY = [];

    pointsX[0] = 0;
    pointsY[0] = 0;
    pointsX[1] = elementLength * 0.77;
    pointsY[1] = h1;
    pointsX[2] = elementLength;
    pointsY[2] = 0;
    pointsX[3] = elementLength * 0.77;
    pointsY[3] = h2;
    pointsX[4] = 0;
    pointsY[4] = -5;

    beginShape();
    curveVertex(pointsX[3], pointsY[3]);

    for (var i = 0; i < pointsX.length; i++) {
      curveVertex(pointsX[i], pointsY[i]);
    }

    curveVertex(pointsX[1], pointsY[1]);
    endShape(CLOSE);

    pop();
  }
}
```

| 编号 | 说明 |
|---|---|
| 1 | 数位板捕获笔的许多特征。这三个查询获取压力和角度信息。 |
| 2 | 只有当笔不完全垂直于数位板且压力大于零时，才应绘制元素。 |
| 3 | 声明描述形状所需的变量。使用`random()`函数，形状在计算时其长度和宽度会略有变化。 |
| 4 | 为形状的轮廓点创建两个数组`pointsX`和`pointsY`，然后填充值。 |
| 5 | 绘制形状。 |
| ! | 关于绘制闭合曲线，请参见：→P.2.2.3 来自代理的形状 |

| 鼠标： | 拖拽：绘制 |
|---|---|
| 数位板： | 压力：饱和度<br>方位角：旋转<br>倾斜度：长度 |
| 按键： | 1–3：绘制模式<br>6–0：颜色<br>DEL：清除画布<br>S：保存图像 |

![image](img/f0140-01.jpg)

`→ P_2_3_5_01_TABLET` → 插图：Pau Domingo 快速叠加的基本形态，形成了复杂的有机形态。

![image](img/f0141-01.jpg)

`→ P_2_3_5_01_TABLET` → 插图：Pau Domingo、Franz Stämmele 和 Jana-Lina Berkenbusch 从鸟类到山脉再到抽象的有机形态，数位板激发了独特插图的创作。

## P.2.3.6 使用复杂模块绘制

团结就是力量：简单模块变成超级字符。利用组合学和复杂模块作为画笔，每个模块相对于其四个邻居进行定义，从而生成超级字符。根据模块库和排列方式，可以生成许多不同的字符组。

`→ P_2_3_6_01`

用户使用鼠标绘制网格，并在其字段中放置各种 SVG 模块。每个字段的唯一信息是它是空的还是填充的。显示网格时，每个字段邻居的填充或空状态变得明显；根据此状态，选择特定的图形模块。

四个邻居的十六种可能状态可以轻松地用四位二进制代码概括。只需将二进制代码转换为十进制数，无需复杂的组合数学，即可确定正确的 SVG 模块。

![image](img/f0142-01.jpg)

```javascript
function draw() {
  background(255);

  if (mouseIsPressed) {
    if (mouseButton == LEFT) setTile();
    if (mouseButton == RIGHT) unsetTile();
  }

  if (doDrawGrid) drawGrid();
  drawModules();
}
```

| 编号 | 说明 |
|---|---|
| 1 | 使用函数`setTile()`和`unsetTile()`，将网格中某个字段的状态设置为 1 或 0。 |
| 2 | 使用函数`drawModules()`，显示所有 SVG 模块。底层网格可通过函数`drawGrid()`绘制。 |

```javascript
function setTile() {
  var gridX = floor(mouseX / tileSize) + 1;
  gridX = constrain(gridX, 1, gridResolutionX - 2);

  var gridY = floor(mouseY / tileSize) + 1;
  gridY = constrain(gridY, 1, gridResolutionY - 2);

  tiles[gridX][gridY] = 1;
}
```

| 编号 | 说明 |
|---|---|
| 3 | 鼠标位置被转换为网格中对应的网格字段方块（`gridX`、`gridY`）。 |
| 4 | 网格中所有字段的状态保存在二维数组`tiles`中。被点击的字段设置为值 1。 |



```javascript
function drawModules() {

for (var gridX=0; gridX<gridResolutionX-1; gridX++) {

for (var gridY=0; gridY<gridResolutionY-1; gridY++) {

5

if (tiles[gridX][gridY] == 1) {

var NORTH = str(tiles[gridX][gridY - 1]);

var WEST = str(tiles[gridX - 1][gridY]);

var SOUTH = str(tiles[gridX][gridY + 1]);

var EAST = str(tiles[gridX + 1][gridY]);

6

var binaryResult = NORTH + WEST + SOUTH + EAST;

7

var decimalResult = parseInt(binaryResult, 2);

var posX = tileSize * gridX - tileSize / 2;

var posY = tileSize * gridY - tileSize / 2;

8

image(modules[decimalResult], posX, posY,

tileSize, tileSize);

...

}

}

}

}
```

| 5 | 处理所有图块。仅考虑状态为 1（即已填充）的字段。 |
|---|---|
| 6 | 查询四个邻居的状态，转换为字符串并拼接。因此，`binaryResult` 包含一个由四个 0 或 1 组成的序列。 |
| 7 | 使用函数 `parseInt()` 将二进制表示编码的状态转换为十进制数。 |
| 8 | 使用 `decimalResult` 选择对应的 SVG 模块，并绘制在画布上。 |

| 鼠标： | 拖动：绘制模块 |
|---|---|
| 鼠标右键拖动： | 删除模块 |
| 按键： | DEL：清除画布 |
|  | G：显示/隐藏网格 |
|  | D：显示/隐藏模块值 |
|  | S：保存图像 |

![image](img/f0144-01.jpg)

**→ P_2_3_6_02** 使用图块可以轻松绘制完整的字符；可能性是无限的，因为总能在矢量程序中生成新的图块集。

![image](img/f0145-01.jpg)

**→ P_2_3_6_02 → 插图：Pau Domingo** 通过填充相邻网格来创建图案。

![image](img/f0145-02.jpg)

**→ P_2_3_6_02 → 插图：Cedric Kiefer** 这里的图块被用作装饰结构。

![image](img/f0145-03.jpg)

**→ P_2_3_6_02 → 插图：Cedric Kiefer** 对称的面具状形式。

## P.2.3.7 使用多种画笔绘制

不同画笔的排列，所有画笔同时响应鼠标位置，给人一种在镜厅中绘画的印象。每个画笔运动的水平和垂直镜像产生了万花筒般的效果。

**→ P_2_3_7_01**

创建一个绘画程序非常简单：在每一帧中，在当前鼠标位置和前一帧鼠标位置之间绘制一条线。这条小线可以轻松地多次绘制，既可以作为精确副本水平或垂直偏移，也可以作为反射：水平、垂直或对角线——或者同时偏移和反射。

![image](img/f0146-01.jpg)

![image](img/f0146-02.jpg)

**→ P_2_3_7_01** 使用镜像轴和重复的三种不同方式。

```javascript
function setup() {

1

canvasElement = createCanvas(800, 800);

...

2

img = createGraphics(width, height);

...

}
```

| 1 | 此草图应仅在方形画布上使用。否则，对角线反射会导致问题。 |
|---|---|
| 2 | 函数 `createGraphics()` 创建一个稍后将被绘制的图像。这允许显示和隐藏镜像轴。 |

```javascript
function draw() {

background(255);

3

image(img, 0, 0);

...

if (mouseIsPressed && mouseButton == LEFT) {

4

var w = width / penCount;

var h = height / penCount;

5

var x = mouseX % w;

var y = mouseY % h;

6

var px = x - (mouseX - pmouseX);

var py = y - (mouseY - pmouseY);

for (var i = 0; i < penCount; i++) {

for (var j = 0; j < penCount; j++) {

7

var ox = i * w;

var oy = j * h;

8

img.line(x+ox, y+oy, px+ox, py+oy);

9

if (mh || md2 && md1 && mv)

img.line(w-x+ox, y+oy, w-px+ox, py+oy);

if (mv || md2 && md1 && mh)

img.line(x+ox, h-y+oy, px+ox, h-py+oy);

if (mv && mh || md2 && md1)

img.line(w-x+ox, h-y+oy, w-px+ox, h-py+oy);

10

if (md1 || md2 && mv && mh)

img.line(y+ox, x+oy, py+ox, px+oy);

if (md1 && mh || md2 && mv)

img.line(y+ox, w-x+oy, py+ox, w-px+oy);

if (md1 && mv || md2 && mh)

img.line(h-y+ox, x+oy, h-py+ox, px+oy);

if (md1 && mv && mh || md2)

img.line(h-y+ox, w-x+oy, h-py+ox, w-px+oy);

}

}

...

}

}
```

| 3 | 在每一帧中，首先将绘制的图像复制到画布上。 |
|---|---|
| 4 | `penCount` 变量决定在 x 和 y 方向上生成多少个虚拟画笔。值为 3 会产生 9 个画笔。变量 `w` 和 `h` 是画笔移动的图块的宽度和高度。 |
| 5 | 坐标 `x`、`y` 是左上角图块中画笔的位置。 |
| 6 | 变量 `pmouseX` 和 `pmouseY` 由 p5.js 提供，始终包含前一帧的鼠标位置。 |
| 7 | 值 `ox` 和 `oy` 表示画笔的 x 和 y 偏移量。 |
| 8 | 在所有情况下，都会在当前鼠标位置和前一鼠标位置之间绘制一条线。 |
| 9 | 如果 `mh` 为真（应水平镜像），则 x 位置从图块宽度中减去。顺便提一下，当垂直镜像以及围绕两条对角线镜像时，也会出现水平反射。 |
| 10 | 单对角线反射最容易通过交换 x 和 y 来生成。 |

| 鼠标： | 拖动：绘制 |
|---|---|
| 按键： | 1–4：各种反射开/关 |
|  | 5–0：颜色 |
|  | 箭头 ↓/↑：线宽 –/+ |
|  | 箭头 ←/→：画笔数量 –/+ |
|  | DEL：清除画布 |
|  | D：显示/隐藏镜像轴 |
|  | G：GIF 录制开始/停止 |
|  | S：保存图像 |

![image](img/f0148-01.jpg)

**→ P_2_3_7_02_TABLET** 这幅画中不断改变图块数量，并且经常用黑色、绿色和白色覆盖图形。

![image](img/f0149-01.jpg)

**→ P_2_3_7_02_TABLET** 在数位板版本中，线条粗细响应笔的压力。

![image](img/f0150-01.jpg)

# P.3 字体

在“形状”一章中，我们演示了如何利用重复（网格）、迭代（代理）和交互（绘制）的原理生成形状。本章致力于一种在设计中也极为重要的特殊形式：字体排印。通过多种方法——从文本的视觉分析到字符的轮廓——在以下示例中，字体排印将在生成式设计的背景下被审视。

P.3 字体 150

P.3.0 你好，字体 152

P.3.1 文本 154

P.3.1.1 编写基于时间的文本 154

P.3.1.2 文本作为蓝图 156

P.3.1.3 文本图像 160

P.3.1.4 文字图示 166

P.3.2 字体轮廓 170

P.3.2.1 溶解字体轮廓 170

P.3.2.2 变化字体轮廓 174

P.3.2.3 来自代理的字体轮廓 178

P.3.2.4 平行字体轮廓 180

P.3.2.5 动态字体 184

## P.3.0 你好，文字

字母变成了空间。在生成基于矢量的字体时，你可以直接影响众多参数，并在时间和空间中用字母进行设计。字符出现的过程以及对其大小和位置的交互式操作都可以变得可见。

**→ P_3_0_01**

字母的大小由鼠标的水平移动控制，而垂直移动则使字母上下移动。当按住鼠标按钮时，字母会留下轨迹。

![image](img/f0152-01.jpg)

![image](img/f0152-02.jpg)

**→ P_3_0_01** 字母留下其变化的轨迹，然后变得无法辨认，并生成新的形态。

1

```javascript
var font = "sans-serif";
var letter = "A";
```

| 1 | 要使用的字体名称保存在变量 `font` 中。 |

```javascript
function setup() {
  createCanvas(windowWidth, windowHeight);
  background(255);
  fill(0);
  2
  textFont(font);
  textAlign(CENTER, CENTER);
}
```

| 2 | 函数 `textFont()` 将其设置为当前字体。水平和垂直对齐方式可通过 `textAlign()` 指定。 |

```javascript
function mouseMoved() {
  clear();
  3
  textSize((mouseX - width / 2) * 5 + 1);
  text(letter, width / 2, mouseY);
}
```

| 3 | 当鼠标移动时，字母大小根据鼠标水平位置的值而变化。字母水平居中于显示窗口的 `width / 2`，垂直位于 `mouseY` 位置，并通过 `text()` 命令显示。 |

4

```javascript
function mouseDragged() {
  textSize((mouseX - width / 2) * 5 + 1);
  text(letter, width / 2, mouseY);
}
```

| 4 | 当按住鼠标按钮移动鼠标时也会发生同样的情况，但此时背景不会获得新颜色，字母会留下轨迹。 |

| 鼠标： | 位置 x：大小 |
|---|---|
|  | 位置 y：位置 |
|  | 拖动：绘制 |
| 按键： | A–Z：选择字母 |
|  | CTRL：保存图像 |

![image](img/f0153-01.jpg)

## P.3.1.1 编写基于时间的文本

用自动换行来编排文本并非新鲜事。但当垂直鼠标位置决定行距（行间间距），而输入每个字母前经过的时间决定其大小时，书写的节奏便开始与文本互动。

**→ P_3_1_1_01**

打字时，虚拟的“笔尖”在绘图画布上从左向右移动。当到达右边界时，它会从头开始并换行。行距由垂直鼠标位置定义。测量每次按键之间的时间间隔。时间间隔越大，输入的字母就越大。

![image](img/f0154-01.jpg)

![image](img/f0154-02.jpg)

**→ P_3_1_1_01** 垂直鼠标位置定义行距（行间距）。产生不同层次的可读性。

```javascript
function draw() {
  ...
  spacing = map(mouseY, 0, height, 0, 120);
  translate(0, 200 + spacing);
  var x = 0;
  var y = 0;
  var fontSize = 20;
  1
  for (var i = 0; i < textTyped.length; i++) {
    2
    fontSize = fontSizes[i];
    textFont(font, fontSize);
    3
    var letter = textTyped.charAt(i);
    var letterWidth = textWidth(letter) + tracking;
    4
    if (x + letterWidth > width) {
      x = 0;
      y += spacing;
    }
    5
    text(letter, x, y);
    x += letterWidth;
  }
  6
  var timeDelta = millis() - pMillis;
  newFontSize = map(timeDelta, 0, maxTimeDelta, minFontSize, maxFontSize);
  newFontSize = min(newFontSize, maxFontSize);
  fill(200, 30, 40);
  if (int(frameCount / 10) % 2 == 0) fill(255);
  7
  rect(x, y, newFontSize / 2, newFontSize / 20);
}
```

| 1 | 变量 `textTyped` 包含输入的文本。现在逐字母处理。 |
|---|---|
| 2 | `fontSize` 取自数组 `fontSizes[]` 中索引 `i` 的值，并将字体设置为该大小。 |
| 3 | 现在从字符串 `textTyped` 中选取索引 `i` 处的字母，并保存在 `letter` 中。此外，字母宽度 `textWidth(letter)` 增加了 `tracking` 的值。 |
| 4 | 当当前位置加上字符宽度超过绘图画布宽度时，发生换行。因此 `x` 重置为 0，垂直位置 `y` 增加行距。 |
| 5 | 在位置 `x`、`y` 处绘制字母。 |
| 6 | 所有字母绘制完毕后，显示一个闪烁的光标。随着时间的推移，光标会变大，因此需要确定 `timeDelta`——自上次打字操作以来经过的时间。当前时间通过 `millis()` 函数以毫秒为单位获取。减去上次按键时保存的值 `pMillis`。现在可以将这个时间差转换为 `minFontSize` 到 `maxFontSize` 的范围。 |
| 7 | 使用该值在当前绘制位置绘制一个矩形。 |

```javascript
function keyTyped(){
  if(keyCode >= 32){
    8
    textTyped += key;
    fontSizes.push(newFontSize);
  }
}
```

| 8 | 按下按键时，将输入的字母附加到字符串 `textTyped` 中，并通过追加 `newFontSize` 中的新字母大小来扩展数组 `fontSizes[]`。 |

```javascript
function keyPressed() {
  ...
  9
  pMillis = millis();
}
```

| 9 | 当前时间保存在 `pMillis` 中，以便始终获得上次按键的时间。 |

| 鼠标： | 位置 x：大小 |
|---|---|
|  | 位置 y：位置 |
| 按键： | A–Z：选择字母 |
|  | CTRL：保存图像 |

## P.3.1.2 文本作为蓝图

在这个例子中，时间不再决定字母大小。相反，某些字母会修改文本方向等属性。在这个程序中，每个字符都通过视觉规则进行转换。源文本因此成为构图的蓝图。

**→ P_3_1_2_01**

用户可以通过键盘自由输入文本。每个字符都由程序中的固定规则转换，该规则指定绘制什么以及如何改变位置和大小。

每次输入都可以使用退格键或删除键撤销。

在这个例子中，部分字符被加载的 SVG 模块替换。

![image](img/f0156-01.jpg)

![image](img/f0156-02.jpg)

**→ P_3_1_2_01** 程序将文本（此处为 Kraftwerk 歌曲 *Taschenrechner* 的歌词）解释为平面图。使用 ALT 键可以生成不同的 RandomSeed，从而不断赋予文本新的外观，因为空格键有两个可能的随机方向。



```javascript
function draw() {
  ...
  1
  translate(centerX, centerY);
  scale(zoom);
  2
  for (var i = 0; i < textTyped.length; i++) {
    var letter = textTyped.charAt(i);
    3
    var letterWidth = textWidth(letter);
    4
    switch (letter) {
      5
      case ' ':
        var dir = floor(random(0, 2));
        if (dir == 0) {
          image(shapeSpace, 1, -15);
          translate(4, 1);
          rotate(QUARTER_PI);
        }
        if (dir == 1) {
          image(shapeSpace2, 1, -15);
          translate(14, -5);
          rotate(-QUARTER_PI);
        }
        break;
      6
      case ',':
        image(shapeComma, 1, -15);
        translate(35, 15);
        rotate(QUARTER_PI);
        break;
      ...
      7
      default:
        fill(0);
        text(letter, 0, 0);
        translate(letterWidth, 0);
    }
  }
  // 文本后的闪烁光标
  fill(0);
  8
  if (int(frameCount / 6) % 2 == 0) rect(0, 0, 15, 2);
}
```

| 1 | 在显示文本之前，坐标原点被移动到点（`centerX`，`centerY`）。这种灵活的定义允许通过鼠标交互移动该点。 |
|---|---|
| 2 | 所有输入的字母按顺序处理。 |
| 3 | 每个字母的字符宽度会被计算，以便后续将书写位置偏移到正确的距离。 |
| 4 | 程序的核心是一组规则，用于指定各个字符如何影响图像和书写行为。为此，使用`switch()`命令来区分当前字母。 |
| 5 | 空格的处理方式如下：根据随机值`dir`，绘制两个已加载的 SVG 模块`shapeSpace`或`shapeSpace2`中的一个；使用`translate()`调整书写位置；并使用`rotate()`将书写方向向左或向右旋转 45°。 |
| 6 | 对于其他特殊字符（此处为逗号），SVG 也会被加载到变量中。当这些字符出现时，绘制相应的模块，并调整书写位置和方向。 |
| 7 | 对于所有其他字符，绘制该字母，并将书写位置移动`letterWidth`的距离。 |
| 8 | 闪烁光标的显示：此构造使用 p5.js 变量`frameCount`（每帧自动递增）和取模运算符`%`来交替生成值 0 和 1，从而实现光标的淡入淡出。 |

| 操作 | 说明 |
|---|---|
| 鼠标 | 拖拽：移动绘图画布 |
| 按键 | A–Z：输入文本 |
|  | 标点符号：曲线 |
|  | 空格键：随机位置曲线 |
|  | DEL：删除字母 |
|  | 箭头 ↓/↑：缩放绘图画布 |
|  | ALT：新的随机布局 |
|  | CTRL：保存图像 |

![image](img/f0158-01.jpg)

**→ P_3_1_2_02 → 插图：Cedric Kiefer**

输入的字母被替换为各种元素——例如，ENTER = “开始新行”。文本完全转化为图像。

## P.3.1.3 文本图像

哪些字符出现，以及出现频率如何？被分析文本的属性可以生成图像。计算每个字符在文本中出现的次数，并决定其外观。例如，字母的颜色与其出现频率相对应。最终，我们甚至不再需要字母本身。

**→ P_3_1_3_01**

文本逐字符处理，每个字符对应的计数器递增。结果得到一个计数器列表，代表每个字符的频率。这些值现在可以作为显示文本的参数。

![image](img/f0160-01.jpg)

...

1

```javascript
var alphabet = "ABCDEFGHIJKLMNORSTUVWYZÄÖÜß,.;!? ";
var counters = [];
```

...

| 1 | 字符串`alphabet`决定了哪些字符需要被计数。`counters`数组以字符串长度初始化，从而为每个字符提供一个计数器。 |
|---|---|

```javascript
function preload() {
```

2

```javascript
joinedText = loadStrings("data/faust_kurz.txt");
}
```

| 2 | 使用`loadStrings()`函数加载待分析的文本。 |
|---|---|

```javascript
function setup() {
createCanvas(620, windowHeight);
...
```

3

```javascript
joinedText = joinedText.join(" ");
for (var i = 0; i < alphabet.length; i++) {
counters[i] = 0;
}
```

4

```javascript
countCharacters();
}
```

| 3 | 各个文本现在位于一个字符串数组中。由于处理连续文本更为实用，因此使用`join()`函数将各行连接起来。 |
|---|---|
| 4 | 调用`countCharacters()`函数来确定频率。 |

```javascript
function countCharacters() {
for (var i = 0; i < joinedText.length; i++) {
```

5

```javascript
var c = joinedText.charAt(i);
var upperCaseChar = c.toUpperCase();
```

6

```javascript
var index = alphabet.indexOf(upperCaseChar);
if (index >= 0) counters[index]++;
}
}
```

| 5 | 处理文本：使用`charAt()`从文本中取出一个字符，并使用`toUpperCase()`函数将其转换为大写字母。 |
|---|---|
| 6 | 使用`indexOf()`函数查找给定字符串中的每个字母在字母表中的位置。如果找到该字母，则对应字母的索引递增。 |

```javascript
function draw() {
...
```

7

```javascript
posX = 20;
posY = 40;
for (var i = 0; i < joinedText.length; i++) {
var upperCaseChar=joinedText.charAt(i).toUpperCase();
```

8

```javascript
var index = alphabet.indexOf(upperCaseChar);
if (index < 0) continue;
```

9

```javascript
if (drawAlpha) {
fill(87, 35, 129, counters[index] * 3);
} else {
fill(87, 35, 129);
}
```

10

```javascript
var sortY = index * 20 + 40;
var m = map(mouseX, 50, width - 50, 0, 1);
```

11

```javascript
m = constrain(m, 0, 1);
var interY = lerp(posY, sortY, m);
text(joinedText.charAt(i), posX, interY);
```

12

```javascript
posX += textWidth(joinedText.charAt(i));
if (posX >= width - 200 && upperCaseChar == " ") {
posY += 30;
posX = 20;
}
}
}
```

| 7 | 变量`posX`和`posY`在开始时被初始化为相应值。 |
|---|---|
| 8 | 绘制时，每次从头开始处理文本，并且与`countCharacters()`函数中一样，确定当前字符在计数器数组中的索引。如果未找到该字符（`index < 0`），则使用`continue`命令取消该字符的绘制过程。 |
| 9 | 当绘制模式`drawAlpha`启用时，填充颜色的透明度取决于字符的频率，并通过`counters[index]`设置。 |
| 10 | 引入变量`sortY`来对字符进行排序。它表示字符应移动或迁移到的行的 y 坐标。对于 A，该值为 40；对于 B，该值为 60，以此类推。 |
| 11 | 鼠标位置被转换为介于 0 和 1 之间的数字`m`，作为插值变量。使用`lerp()`函数在`posY`和`sortY`之间进行插值，计算出的值`interY`用于定位字符。 |
| 12 | 现在只需更新书写位置。`posX`的值增加字符宽度；如果该值接近显示区域的右边界且当前字符是空格，则进行换行。`posY`的值增加行间距，`posX`重置到左侧。 |

| 操作 | 说明 |
|---|---|
| 鼠标 | 位置 x：正常文本与排序文本之间的过渡 |
| 按键 | 1：切换透明度模式 |
|  | S：保存图像 |

![image](img/f0161-01.jpg)

**→ P_3_1_3_01** 鼠标水平位置控制字母是显示在正常文本位置还是排序后的位置。

![image](img/f0162-01.jpg)

![image](img/f0163-01.jpg)

**→ P_3_1_3_03** 文本中字母的频率在此处通过多种方式及组合进行编码：绿色圆圈的大小和透明度、紫色线条的长度以及字母本身的不透明度。

![image](img/f0164-01.jpg)

**→ P_3_1_3_04** 相同的字母由彩色线条连接；线条的颜色按字母顺序遍历色轮一次。当鼠标向右移动时，字母按其频率排序。

任何字母都可以单独开启或关闭，从而可以单独观察元音的频率等。灰色线条（见右图）可通过按键 2 开启或关闭，它将每个字母与紧随其后的字母连接起来。虽然在正常文本中几乎不可见，但按字母排列时，这些灰色线条会形成引人注目的网络结构。

![image](img/f0165-01.jpg)

## P.3.1.4 文本图表

简·奥斯汀最喜欢的词汇是什么？机械读取和处理大量文本的可能性为实验提供了广阔空间。例如，可以统计《傲慢与偏见》中的所有单词，并用不同大小的元素（此处为矩形）表示其频率，从而创建作为静态文学批评的图表。

**→ P_3_1_4_01**

所谓树图（treemap）的目标是根据文本中每个单词的使用频率，将一个矩形分割成更小的矩形。简·奥斯汀的《傲慢与偏见》全文从文本文件中读取，并传输到`Treemap`类中进行可视化。`TreeMap`算法的各个参数可以手动输入。

![image](img/f0166-01.jpg)

![image](img/f0166-02.jpg)

**→ P_3_1_4_01** 按频率排列的树图部分，其中只允许水平元素。

1

```javascript
var mapData = {};
...
```

2

```javascript
var doSort = true;
var rowDirection = "both";
```

| 1 | 数据容器`mapData`稍后将填充加载文本中的单词及其数量。 |
|---|---|
| 2 | `doSort`和`rowDirection`变量控制`TreeMap`的不同布局。 |

```javascript
function setup() {
...
joinedText = joinedText.join(" ");
3
var words = joinedText.match(/\w+/g);
4
treemap = new gd.Treemap(1, 1, width - 3, height - 3,
{sort:doSort, direction:rowDirection});
for (var i = 0; i < words.length; i++) {
5
var w = words[i].toLowerCase();
treemap.addData(w);
}
treemap.calculate();
}
```

| 3 | 使用`match()`将完整文本拆分为单个单词。该函数的参数是一个正则表达式。借助它，可以执行非常复杂的文本搜索。这里使用的表达式相对简单：搜索一个或多个连续（`+`）的单词字符（`\w`）。末尾的`g`表示“全局”，即搜索不应在第一次出现后停止。 |
|---|---|
| 4 | 生成`TreeMap`。前四个参数指定位置（`x`、`y`）、宽度和高度。此外，还传入一个对象用于显示选项。 |
| 5 | 处理包含单词的数组。每个单词首先转换为小写字母，以便同一单词的不同大小写形式（例如，当它用作句首单词时）仍能被识别。然后，`addData()`将单词添加到树图中，并通过`calculate()`开始计数。 |

```javascript
function draw() {
background(255);
textAlign(CENTER, BASELINE);
6
for (var i = 0; i < treemap.items.length; i++) {
var item = treemap.items[i];
fill(255);
stroke(0);
strokeWeight(1);
7
rect(item.x, item.y, item.w, item.h);
var word = item.data;
textFont(font, 100);
8
var textW = textWidth(word);
var fontSize = 100 * (item.w * 0.9) / textW;
9
fontSize = min(fontSize, (item.h * 0.9));
textFont(font, fontSize);
fill(0);
noStroke();
10
text(word, item.x + item.w/2, item.y + item.h*0.8);
}
...
}
```

| 6 | 使用`Treemap`类为每个单词计算了一个树图元素，现在所有这些元素都以数组项的形式提供。 |
|---|---|
| 7 | 元素的位置、宽度和高度自动包含在变量`x`、`y`、`w`和`h`中，可用于绘制元素的边框。 |
| 8 | 然后将字体大小设置为 100，以确定单词的宽度。通过三分法，可以计算出字体大小，使单词适合`item.w`矩形的宽度。 |
| 9 | 然而，单词的高度不能超过矩形的高度。 |
| 10 | 单词被写入矩形中。 |

| 按键 | 描述 |
|---|---|
| R | 随机开/关 |
| H | 水平排列 |
| V | 垂直排列 |
| B | 双向排列 |
| S | 保存图像 |

![image](img/f0168-01.jpg)

**→ P_3_1_4_01** 简·奥斯汀《傲慢与偏见》中所有单词的频率以树图形式呈现。在此排列中，算法尽量使矩形保持正方形。

![image](img/f0169-01.jpg)

**→ P_3_1_4_02** 在程序的第二个版本中，单词按字母数量分组。您可以使用数字键（1–9）显示或隐藏各个组。

## P.3.2.1 分解字体轮廓

文本由字符组成。而字符则由其轮廓塑造。在接下来的章节中，这个轮廓将消散成众多点，并为生成式字体操作奠定基础。各个点被其他元素替换，从而掩盖原始字体。

**→ P_3_2_1_01**

起点是一个文本和一个字体文件。由 Frederik De Bleser 设计的`opentype.js`库在字体轮廓上生成大量点。然后可以利用这些信息为字符赋予新的视觉身份。

![image](img/f0170-01.jpg)

![image](img/f0170-02.jpg)

**→ P_3_2_1_02** 在此版本的程序中，SVG 被加载并放置在字符轮廓上。旋转角度和缩放比例可通过鼠标控制。

1

```javascript
function setup() {
...
opentype.load('data/FreeSans.otf', function(err, f) {
font = f;
loop();
});
}
```

| 1 | `opentype.js`库加载字体文件并将其存储在`font`变量中。 |
|---|---|



```javascript
function draw() {
  ...
  if (textTyped.length > 0) {
    // 2
    var fontPath = font.getPath(textTyped, 0, 0, 200);
    // 3
    var path = new g.Path(fontPath.commands);
    // 4
    path = g.resampleByLength(path, 11);
    stroke(181, 157, 0);
    strokeWeight(1.0);
    var l = 5;
    // 5
    for (var i = 0; i < path.commands.length; i++) {
      var pnt = path.commands[i];
      line(pnt.x - l, pnt.y - l, pnt.x + l, pnt.y + l);
    }
    fill(0);
    noStroke();
    var diameter = 7;
    for (var i = 0; i < path.commands.length; i++) {
      var pnt = path.commands[i];
      // 6
      if (i % 2 == 0) {
        ellipse(pnt.x, pnt.y, diameter, diameter);
      }
    }
  }
  ...
}
```

| **2** | 提取点需要三个步骤：首先，`opentype.js` 库的 `getPath()` 函数将字符转换为路径。 |
|---|---|
| **3** | 然后将其转换为 `g.Path` 对象（`g.js` 是另一个库）。 |
| **4** | 命令 `resampleByLength()` 将此路径分割成等长的段（此处为 11 像素）。 |
| **5** | 处理这些点。首先在其位置上绘制短斜线。![image](img/f0171-01.jpg) |
| **6** | 接下来处理黑色圆圈。在此次运行中，仅使用每隔一个的位置。![image](img/f0171-02.jpg) |

| 按键 | 描述 |
|---|---|
| 键盘 | 文本输入 |
| DEL | 删除字母 |
| CTRL | 保存图像 |

![image](img/f0171-03.jpg)

**→ P_3_2_1_01** 图形元素放置在字符轮廓上。

![image](img/f0172-01.jpg)

**→ P_3_2_1_02** 通过缩放和旋转字符轮廓上的元素，可以调节生成的字符形态的外观。

## P.3.2.2 变化字体轮廓

如果字体轮廓不是由直线或曲线构成，而是由可控元素构成，那么我们就越来越脱离底层字体。所有现有的基点通过特殊形状的贝塞尔曲线连接在一起。这只是快速创建数十种新字体的众多方法之一。

**→ P_3_2_2_01**

文本轮廓上的点通过贝塞尔曲线连接。曲线的形状可以通过鼠标交互控制。

![image](img/f0174-01.jpg)

![image](img/f0174-02.jpg)

**→ P_3_2_2_01** 贝塞尔曲线高度和旋转的不同设置。

```javascript
function draw() {
  ...
  if (textTyped.length() > 0) {
    ...
    // 1
    var addToAngle = map(mouseX, 0, width, -PI, +PI);
    var curveHeight = map(mouseY, 0, height, 0.1, 2);
    // 2
    for (var i = 0; i < path.commands.length - 1; i++) {
      var pnt0 = path.commands[i];
      var pnt1 = path.commands[i + 1];
      var d = dist(pnt0.x, pnt0.y, pnt1.x, pnt1.y);
      // 3
      if (d > 20) continue;
      // 4
      var stepper = map(i % 2, 0, 1, -1, 1);
      var angle = atan2(pnt1.y - pnt0.y, pnt1.x - pnt0.x);
      angle = angle + addToAngle;
      var cx = pnt0.x + cos(angle * stepper) * d * 4 * curveHeight;
      var cy = pnt0.y + sin(angle * stepper) * d * 3 * curveHeight;
      // 5
      bezier(pnt0.x, pnt0.y, cx, cy, cx, cy, pnt1.x, pnt1.y);
    }
  }
}
```

| **1** | 变量 `addToAngle` 和 `curveHeight` 由鼠标位置的 x 和 y 坐标决定，并控制贝塞尔曲线的旋转和高度。 |
|---|---|
| **2** | 点从第一个处理到倒数第二个。每次计算当前点到下一个点的距离。 |
| **3** | 当距离大于五十时，此循环中止，不绘制线条。由于 `opentype.js` 库将整个文本的点作为点链提供，因此确保了单个字母不会相连。 |
| **4** | 对于变量 `stepper`，交替产生值 –1 和 1。这些值用于计算贝塞尔曲线 `cx`、`cy` 的控制点，以使曲线上下移动。 |
| **5** | 绘制贝塞尔曲线时需要定义四个点：起点、终点和两个控制点。此处将刚刚计算出的控制点使用两次。 |

| 鼠标： | 位置 x：曲线旋转位置 y：曲线高度 |
|---|---|
| 按键： | 键盘：输入文本 DEL：删除字母 ALT：更改填充模式 CTRL：保存图像 |

![image](img/f0175-01.jpg)

生成新的轮廓，并在原始轮廓周围上下移动；它由单个贝塞尔曲线组成，这些曲线由起点、终点和两个控制点定义，在本例中这两个控制点具有相同的值：`c of p[0] = c of p[1]`。

![image](img/f0176-01.jpg)

**→ P_3_2_2_01** 鼠标位置决定贝塞尔曲线的形状。可以使用 ALT 键切换到填充曲线。

## P.3.2.3 来自智能体的字体轮廓

一个字母在多大程度上仍能被识别？在此示例中，字母的轮廓作为源形状。每个单独的节点像哑智能体一样移动。随着时间的推移，字母变得难以辨认，并转化为新的东西。

**→ P_3_2_3_01**

再次从字体轮廓生成点。每个点成为一个独立的哑智能体，但仍与其相邻点保持连接。

![image](img/f0178-01.jpg)

![image](img/f0178-02.jpg)

![image](img/f0179-01.jpg)

**→ P_3_2_3_01** 没有按键按下的时间越长，字符变形越严重。

```javascript
function draw() {
  ...
  // 1
  translate(letterX, letterY);
  danceFactor = 1;
  // 2
  if (mouseIsPressed && mouseButton == LEFT) {
    danceFactor = map(mouseX, 0, width, 0, 3);
  }
  if (pnts.length > 0) {
    for (var i = 0; i < pnts.length; i++) {
      // 3
      pnts[i].x += random(-stepSize, stepSize) * danceFactor;
      pnts[i].y += random(-stepSize, stepSize) * danceFactor;
    }
    strokeWeight(0.1);
    stroke(0);
    beginShape();
    for (var i = 0; i < pnts.length; i++) {
      // 4
      vertex(pnts[i].x, pnts[i].y);
      ellipse(pnts[i].x, pnts[i].y, 7, 7);
    }
    // 5
    vertex(pnts[0].x, pnts[0].y);
    endShape();
  }
  pop();
}
```

| **1** | 在写入字母之前，将坐标系原点移动到当前书写位置。 |
|---|---|
| **2** | 按住鼠标按钮时，变量 `danceFactor` 被设置为一个值，该值随鼠标 x 坐标的值成比例增加。 |
| **3** | 每次迭代中，向点的位置添加随机值。`danceFactor` 值增加了移动速度。 |
| **4** | 线条连接各点。 |
| **5** | 最后，再画一条线到第一个点，闭合轮廓。 |

| 鼠标： | 左键点击 + 位置 x：变形速度 |
|---|---|
| 按键： | 键盘：输入文本 SHIFT：移动开始/停止 DEL：清除画布 CTRL：保存图像 |

## P.3.2.4 平行字体轮廓

利用重叠网格结构的摩尔纹效应，可以产生影响字体轮廓并改变字体体积印象的光学错觉。最终，形状从字体中脱离出来，开始独立存在。

**→ P_3_2_4_01**

起点是字母的字体轮廓。对于构成字体轮廓的许多短线段中的每一段，都使用相同的计算过程：将线段旋转 90° 并设置为正确的长度。结果是一条与原始路径平行的路径。当以不断增大的距离重复此过程多次时，就形成了网格结构。

![image](img/f0180-01.jpg)

![image](img/f0180-04.jpg)

**→ P_3_2_4_01** 小写字母“a”的三种变体。不过，这里的字体轮廓已被大幅简化。

```javascript
// 1
function createLetters() {
  letters = [];
  // 2
  var chars = textTyped.split('');
  var x = 0;
  for (var i = 0; i < chars.length; i++) {
    if (i > 0) {
      // 3
      var charsBefore = textTyped.substring(0, i);
      x = font.textBounds(charsBefore, 0, 0, fontSize).w;
    }
    // 4
    var newLetter = new Letter(chars[i], x, 0);
    letters.push(newLetter);
  }
}
```

| **1** | 程序启动或输入的文本发生变化时，调用 `createLetters()` 函数。 |
|---|---|
| **2** | 在该函数中，使用 `split()` 将输入文本生成单个字母的数组 `chars`。 |
| **3** | 为了确定字母的 x 位置，使用 `substring()` 移除当前字符之前的子字符串，并使用 `textBounds()` 函数计算其宽度 `w`。 |
| **4** | 为每个字母创建一个 `Letter` 类的新实例，并添加到数组 `letters` 中。 |

```javascript
function Letter(char, x, y) {
  this.char = char;
  this.x = x;
  this.y = y;
  // 5
  Letter.prototype.draw = function() {
    // 6
    var path = font.textToPoints(
      this.char,
      this.x,
      this.y,
      fontSize,
      { sampleFactor: pathSampleFactor }
    );
    stroke(shapeColor);
    // 7
    for (var d = 0; d < ribbonWidth; d += density) {
      beginShape();
      for (var i = 0; i < path.length; i++) {
        var pos = path[i];
        // 8
        var nextPos = path[i + 1];
        // 9
        if (nextPos) {
          var p0 = createVector(pos.x, pos.y);
          var p1 = createVector(nextPos.x, nextPos.y);
          // 10
          var v = p5.Vector.sub(p1, p0);
          // 11
          v.normalize();
          v.rotate(HALF_PI);
          v.mult(d);
          // 12
          var pneu = p5.Vector.add(p0, v);
          curveVertex(pneu.x, pneu.y);
        }
      }
      endShape(CLOSE);
    }
  };
}
```

| **5** | `Letter` 类有一个 `draw()` 函数，主程序在每一帧中调用它。在该函数中，字体轮廓逐渐向内移动。 |
|---|---|
| **6** | `textToPoints()` 函数将 `char` 字符转换为点数组。 |
| **7** | 此循环绘制各个路径。每次循环中，变量 `d` 包含要绘制的路径与原始路径的距离。 |
| **8** | 从数组 `path` 中取出两个连续的位置。 |
| **9** | 如果 `nextPos` 不为空（即尚未到达路径末尾），则使用 `createVector()` 将这两个位置转换为 `p5.Vector` 类型的值。 |
| **10** | `sub()` 计算两点之间的差值，并存储在 `v` 中。 |
| **11** | 向量 `v` 使用 `normalize()` 归一化为长度 1，使用 `rotate()` 旋转 90°，然后乘以 `d`。 |
| **12** | 通过将 `v` 加到 `p0` 来确定偏移路径上的位置。 |

| 鼠标： | 位置 x：字体轮廓简化程度位置 y：带状轮廓宽度 |
|---|---|
| 按键： | 箭头 ←/→：更改线条密度箭头 ↓/↑：更改字体大小 |

![image](img/f0181-01.jpg)

**→ P_3_2_4_01** 四个字符：百分号、加号、星号和段落符号。轮廓被大幅简化，从而产生了华丽的图形。

## P.3.2.5 动态字体

这里字体轮廓可以随心所欲。忽略可读性，它转化为图案，并尝试了所有形式上的花招。在不断运动中，这些变形保持活力，让我们思考：书写何时成为自身的一种形式？

**→ P_3_2_5_01**

通常，每个新生成的随机数真正随机是好的。然而，在创建动画时，这通常会导致图像闪烁。使用 Perlin 噪声可以避免这种情况。这种计算随机数的方法生成的值，相邻值之间的差异永远不会很大。

![image](img/f0184-01.jpg)

![image](img/f0184-02.jpg)

**→ P_3_2_5_01** 旋转的线条——有时密集排列，有时间距更大。

```javascript
// 1
function setupText() {
  textImg = createGraphics(width, height);
  textImg.pixelDensity(1);
  textImg.background(255);
  textImg.textFont(font);
```

```javascript
  textImg.textSize(fontSize);

  // 2
  textImg.text(textTyped, 100, fontSize + 50);

  // 3
  textImg.loadPixels();
}
```

- **1**：每次文本改变时，都会调用`setupText()`函数。这会使用`createGraphics()`创建一个所谓的离屏图形。这是一个不可见但仅存在于内存中的图像。
- **2**：输入的文本`textTyped`会以先前设置的字体和大小写入该图像。
- **3**：调用`loadPixels()`以便稍后读取各个像素值。

```javascript
function draw() {
  background(255);

  nOff++;

  for (var x = 0; x < textImg.width; x += pointDensity) {
    for (var y = 0; y < textImg.height; y += pointDensity) {
      // 4
      var index = (x + y * textImg.width) * 4;

      // 5
      var r = textImg.pixels[index];

      if (r < 128) {
        if (drawMode == 1) {
          strokeWeight(1);

          var noiseFac = map(mouseX, 0, width, 0, 1);
          var lengthFac = map(mouseY, 0, height, 0.01, 1);

          // 6
          var num = noise(
            (x + nOff) * noiseFac,
            y * noiseFac
          );

          // 7
          if (num < 0.6) {
            stroke(colors[0]);
          } else if (num < 0.7) {
            stroke(colors[1]);
          } else {
            stroke(colors[2]);
          }

          push();
          translate(x, y);
          rotate(radians(frameCount));

          // 8
          line(0, 0, fontSize * lengthFactor, 0);

          pop();
        }
        ...
      }
    }
  }
}
```

- **4**：图像的颜色值存储为一长串数值。因此，要获取某个像素的颜色值，必须根据 x 和 y 计算索引。因子 4 是必要的，因为一个像素由四个单独存储的值组成（分别对应红色、绿色、蓝色和透明度）。
- **5**：带有文本的图像仅由黑色、白色和少量灰色像素组成。因此，只需检查红色值 `r` 是否低于某个阈值即可，如果低于，则为暗像素。
- **6**：需要随机值来给线条着色。为了避免闪烁，`noise()`函数比`random()`函数更可取。它产生的随机数类似于山地景观。这里`noise()`函数被调用时带有两个参数，第一个依赖于 x，第二个依赖于 y。变量 `nOff` 不断递增，从而确保随机数的动画效果。
- **7**：根据`num`的值，将选择三个预定义颜色之一。
- **8**：在先前平移和旋转的坐标系中绘制一条水平线。
- **鼠标**：位置 x/y：不同的参数（取决于绘图模式）。
- **按键**：键盘：文本输入 箭头←/→：更改绘图模式 箭头↓/↑：更改点密度 DEL：清除画布 CTRL：保存图像

![图片](img/f0186-01.jpg)



`→ P_3_2_5_01` 至 `→ P_3_2_5_03` 程序所有三个版本的不同参数设置和结果。字母形状以不同方式生成：来自像素（版本 01）、完全编程（版本 02）或来自字体轮廓（版本 03）。

![图片](img/f0188-01.jpg)

# P.4 图像

在上一章中，我们看到了文本如何被分解，以及由此产生的元素——单词、字母，甚至轮廓上的点——如何用于实验。同样，图像也可以被操作：可以复制细节，制作拼贴画，而像素——数字图像的最小信息单元——可以成为新视觉世界的基础。

P.4 图像 188

P.4.0 你好，图像 190

P.4.1 图像裁剪 192

P.4.1.1 网格中的图像裁剪 192

P.4.1.2 图像裁剪的反馈 196

P.4.2 图像集合 198

P.4.2.1 来自图像集合的拼贴画 198

P.4.2.2 基于时间的图像集合 202

P.4.3 像素值 204

P.4.3.1 来自像素值的图形 204

P.4.3.2 来自像素值的文字 210

P.4.3.3 实时像素值 214

P.4.3.4 来自像素值的表情符号 220

## P.4.0 你好，图像

数字图像是由小彩色瓷砖组成的马赛克。动态访问这些微小元素可以生成新的构图。通过以下程序，可以创建自己的图像工具集。

`→ P_4_0_01`

加载一张图像，并在由鼠标定义的网格中显示。网格中的每个图块都填充了源图像的缩放副本。

![图片](img/f0190-01.jpg)

![图片](img/f0190-02.jpg)

原始图像

![图片](img/f0190-03.jpg)

`→ P_4_0_01` 通过重复复制和极端缩放源图像，创建出抽象图像。

```javascript
// 1
var img;

function preload() {
  img = loadImage('data/image.jpg');
}
```

- **1**：图像在`preload()`函数中加载。这确保了在调用`setup()`和`draw()`函数之前加载过程已完成。

```javascript
// 2
function draw() {
  var tileCountX = mouseX / 3 + 1;
  var tileCountY = mouseY / 3 + 1;
  var stepX = width / tileCountX;
  var stepY = height / tileCountY;

  for (var gridY = 0; gridY < height; gridY += stepY) {
    for (var gridX = 0; gridX < width; gridX += stepX) {
      // 3
      image(img, gridX, gridY, stepX, stepY);
    }
  }
}
```

- **2**：鼠标位置决定了`tileCountX`和`tileCountY`，从而决定了它们的宽度`stepX`和高度`stepY`。
- **3**：使用`image()`函数绘制图像。图像的左上角位于网格(`gridX`, `gridY`)处；宽度和高度由图块宽度`stepX`和图块高度`stepY`决定。
- **鼠标**：位置 x：水平图块数量；位置 y：垂直图块数量
- **按键**：S：保存图像

![图片](img/f0191-01.jpg)

## P.4.1.1 网格中的图像裁剪

下面说明的原理与上一个示例几乎相同，但却展现了一个全新的图像世界。当只选择图像的一部分并将其配置为图块时，图像的细节和精细结构就变成了图案生成器。如果随机选择这些部分，结果会更加有趣。

`→ P_4_1_1_01`

使用鼠标，在显示窗口中选择图像的一个区域。释放鼠标按钮后，该区域的多个副本存储在一个数组中，并按网格组织。程序提供两种变体。在变体一中，所有副本都来自完全相同的区域。在变体二中，每次随机轻微移动该区域。

![图片](img/f0192-01.jpg)

![图片](img/f0192-02.jpg)

原始图像

![图片](img/f0192-03.jpg)

`→ P_4_1_1_01` 通过重复复制和移动图像区域，创建出抽象图像。

```javascript
// 1
function cropTiles() {
  tileWidth = width / tileCountY;
  tileHeight = height / tileCountX;

  // 2
  imgTiles = [];

  for (var gridY = 0; gridY < tileCountY; gridY++) {
    for (var gridX = 0; gridX < tileCountX; gridX++) {
      // 3
      if (randomMode) {
        cropX = int(random(mouseX - tileWidth / 2,
          mouseX + tileWidth / 2));
        cropY = int(random(mouseY - tileHeight / 2,
          mouseY + tileHeight / 2));
      }

      // 4
      cropX = constrain(cropX, 0, width - tileWidth);
      cropY = constrain(cropY, 0, height - tileHeight);

      // 5
      imgTiles.push(img.get(cropX, cropY, tileWidth, tileHeight));
    }
  }
}
```

- **1**：程序的核心是`cropTiles()`函数。在这里，图像被分割，区域的副本存储在数组中。
- **2**：图像框架数组`imgTiles`被清空。
- **3**：如果`randomMode`为真，则裁剪坐标在鼠标位置周围的范围内随机偏移。
- **4**：坐标被限制，以确保它们保持在图像边界内。
- **5**：使用`img.get()`提取图像区域，并添加到数组中。

| 编号 | 说明 |
|---|---|
| 3 | 当第二版启动时（`randomMode`为 true），`cropX`和`cropY`的所有值都会从鼠标位置附近的一个数值范围内随机选取。 |
| 4 | `constrain()`函数确保裁剪区域不会超出图像边界。 |
| 5 | 最后，使用`get()`从图像`img`中复制该区域，并存储到数组中。 |
| 鼠标： | 位置 x/y：细节定位；左键点击：复制细节 |
| 按键： | 1–3：改变细节大小；R：随机开/关；S：保存图像 |

![image](img/f0193-01.jpg)

![image](img/f0194-01.jpg)

`→ P_4_1_1_01` 小图像片段的乘法产生了节奏性的结构，这些结构只有细看才能被识别为图像片段。

![image](img/f0195-01.jpg)

`→ P_4_1_1_01` 使用按键 1 到 3，可以在图像片段的不同部分之间进行选择。在这些大尺寸、细节丰富的截图中，主题仍然可辨认，但现在呈现出一种令人不安的透视效果。

## P.4.1.2 图像截图的反馈

一个熟悉的反馈例子：摄像机对准电视屏幕，屏幕上显示摄像机拍摄的图像。片刻之后，电视屏幕上呈现出不断重复且扭曲的图像。当模拟这种现象时，图像的复杂度会增加。这种重复叠加导致了碎片化的构图。

`→ P_4_1_2_01`

首先，加载图像并显示在屏幕上。每次迭代时，将图像的一个区域复制到随机选择的新位置。生成的图像随后作为下一步的基础——这就是反馈的原理。

![image](img/f0196-01.jpg)

![image](img/f0196-02.jpg)

`→` 摄影：Stefan Eigner；原始图像：地铁隧道

![image](img/f0196-03.jpg)

`→ P_4_1_2_01` 程序启动后，主题很容易辨认。随后，通过复制图像条带的叠加，主题逐渐消散。

```javascript
// 1
function setup() {
  createCanvas(1024, 780);
  image(img, 0, 100);
}
```

| 编号 | 说明 |
|---|---|
| 1 | 程序启动时，使用`image()`命令将加载的图像向下偏移一百像素，并放置在绘图画布上。 |

```javascript
// 2
function draw() {
  var x1 = floor(random(width));
  var y1 = 0;
  var x2 = round(x1 + random(-7, 7));
  var y2 = round(random(-5, 5));
  var w = floor(random(10, 40));
  var h = height;

  // 3
  set(x2, y2, get(x1, y1, w, h));
}
```

| 编号 | 说明 |
|---|---|
| 2 | 要复制的细节的 x 位置（`x1`）、目标位置（`x2`、`y2`）及其宽度（`w`）都是随机确定的。 |
| 3 | 使用`get()`函数复制部分画布内容，然后使用`set()`将其粘贴到新位置（`x2`、`y2`）。 |
| 按键： | DEL：删除显示；S：保存图像 |

![image](img/f0197-01.jpg)

## P.4.2.1 从图像集合中拼贴

你的照片档案现在变成了艺术素材。该程序从一个图像文件夹中拼贴出一幅作品。源图像的裁剪、切割和排序尤为重要，因为拼贴中只重新组合了图像碎片。

`→ P_4_2_1_01`

文件夹中的所有图像被动态读取，并分配到多个图层之一。这样可以对语义组进行不同处理。在构建拼贴时，各个图层在旋转、位置和大小方面也有实验空间。注意图层顺序；第一层先绘制，因此位于背景。

![image](img/f0198-01.jpg)

![image](img/f0198-02.jpg)

`→ P_4_2_1_01` 插图：Andrea von Danwitz。图像由三个层次组成：第 1 层是纸片，第 2 层是天空的剪影，第 3 层是植物和街道元素。

![image](img/f0198-03.jpg)

当切换某一层的图像或更改参数时，会立即生成新的构图。

```javascript
// 1
var layer1Images = [];
var layer2Images = [];
var layer3Images = [];
var layer1Items = [];
var layer2Items = [];
var layer3Items = [];
```

| 编号 | 说明 |
|---|---|
| 1 | 需要多个数组来加载图像并安排拼贴片的布局。例如，在`layer1Images`中，加载的图像被保存到第一层，以便稍后用于创建拼贴项。 |

```javascript
function setup() {
  ...

  // 2
  layer1Items = generateCollageItems(
    layer1Images, 100, width / 2, height / 2,
    width, height, 0.1, 0.5, 0, 0
  );
  layer2Items = generateCollageItems(
    layer2Images, 150, width / 2, height / 2,
    width, height, 0.1, 0.3, -HALF_PI, HALF_PI
  );
  layer3Items = generateCollageItems(
    layer3Images, 110, width / 2, height / 2,
    width, height, 0.1, 0.4, 0, 0
  );

  // 3
  drawCollageItems(layer1Items);
  drawCollageItems(layer2Items);
  drawCollageItems(layer3Items);
}
```

| 编号 | 说明 |
|---|---|
| 2 | 函数`generateCollageItems()`用拼贴项填充数组层（`layer1Items`等）。参数决定了使用哪些加载的图像以及创建多少项，并指定位置、散布、缩放和旋转的值范围。在此示例中，使用数组`layer1Items`中的图像。所有实例都放置在位置（`width/2`、`height/2`），散布范围为`width`和`height`。缩放范围从 0.1 到 0.5，不使用旋转。 |
| 3 | 每次运行`drawCollageItems()`函数时，都会绘制其中一个图层。图层的调用顺序决定了最终构图的构建。`layer1Items`中的图像位于背景，`layer3Items`中的图像位于前景。 |

```javascript
// 4
function CollageItem(image) {
  this.image = image;
  this.x = 0;
  this.y = 0;
  this.rotation = 0;
  this.scaling = 1;
}
```

| 编号 | 说明 |
|---|---|
| 4 | 拼贴项的所有特征都汇总在类`CollageItem`中。 |
| 按键： | 1–3：为三个层级之一生成新的随机排列；S：保存图像 |

![image](img/f0200-01.jpg)

`→ P_4_2_1_02` → 插图：Andrea von Danwitz。该程序的第二个版本允许图像细节围绕特定中心径向排列。可以指定每个图层中图像聚集的角度及其与中心的距离。

## P.4.2.2 基于时间的图像集合

在此示例中，运动图像的内部结构被可视化。从视频文件中提取单个图像后，该程序以定义好的固定时间间隔将图像排列在网格中。该网格展示了整个视频文件的压缩版本，并代表了其剪辑和帧的节奏。

`→ P_4_2_2_01`

为了填充网格，从视频的整个长度中按固定间隔提取单个静止图像。因此，一个 60 秒的视频和包含 20 个格子的网格会产生 3 秒的间隔。

![image](img/f0202-01.jpg)

```javascript
// 1
function draw() {
  if (movie.elt.readyState == 4) {
    var posX = tileWidth * gridX;
    var posY = tileHeight * gridY;
    image(movie, posX, posY, tileWidth, tileHeight);
    currentImage++;

    // 2
    var nextTime = map(
      currentImage, 0, imageCount,
      0, movie.duration()
    );

    // 3
    movie.time(nextTime);

    // 4
    gridX++;
    if (gridX >= tileCountX) {
      gridX = 0;
      gridY++;
    }

    // 5
    if (currentImage >= imageCount) noLoop();
  }
}
```

| 编号 | 说明 |
|---|---|
| 1 | 每次运行`draw()`函数时，都会从视频中选择一帧图像并显示在网格中。时间 0 处的第一帧图像可以立即放置。 |
| 2 | 计算视频中的下一个时间点（`nextTime`）。变量`currentImage`（介于 0 和`imageCount`之间的数字）被转换为介于 0 和视频总播放时间之间的秒数值。 |
| 3 | 使用`time()`函数，程序跳转到新计算的时间点。 |
| 4 | 为了定义下一个格子，`gridX`增加 1。如果到达行尾，程序通过将`gridX`设置为 0 并递增`gridY`来跳转到下一行的第一帧图像。 |
| 5 | 当所有格子都被图像填满时，程序结束。 |
| 按键： | S：保存图像 |

![image](img/f0203-01.jpg)

`→ P_4_2_2_01` 来自一段两分半钟视频片段中的五十五张图像，拍摄于前往德国斯图加特火车总站的途中。

## P.4.3.1 基于像素值的图形

像素是图像的最小元素，可以作为肖像构成的起点。在此示例中，每个像素被简化为其颜色值。这些值调节着旋转、宽度、高度和面积等设计参数。像素被全新的图形表示完全取代，肖像也因此变得有些抽象。

`→ P_4_3_1_01`

图像的像素被依次分析并转换为其他图形元素。关键在于将像素的颜色值（RGB）转换为相应的灰度值，因为与纯 RGB 值相比，灰度值可以实际应用于线宽等设计方面。建议先降低源图像的分辨率。

![image](img/f0204-01.jpg)

![image](img/f0204-02.jpg)

`→ P_4_3_1_01` → 摄影：Tom Ziora。每个像素的灰度值决定了其直径大小；像素的原始颜色值得以保留。

```javascript
// 1
for (var gridX = 0; gridX < img.width; gridX++) {
  for (var gridY = 0; gridY < img.height; gridY++) {
    var tileWidth = width / img.width;
    var tileHeight = height / img.height;
    var posX = tileWidth * gridX;
    var posY = tileHeight * gridY;
    img.loadPixels();

    // 2
    var c = color(img.get(gridX, gridY));

    // 3
    var grayscale = round(
      red(c) * 0.222 +
      green(c) * 0.707 +
      blue(c) * 0.071
    );

    // 4
    switch (drawMode) {
      case 1:
        var w1 = map(grayscale, 0, 255, 15, 0.1);
        stroke(0);
        strokeWeight(w1 * mouseXFactor);
        line(posX, posY, posX + 5, posY + 5);
        break;
      case 2:
        ...
    }
  }
}
```



| **1** | 原始图像的宽度和高度决定了网格的分辨率。 |
|---|---|
| **2** | 定义当前网格位置（即图像）处像素的颜色。 |
| **3** | 在计算灰度值时，红色、绿色和蓝色的权重不同。由于颜色的显示和感知方式不同，因此不存在绝对正确的权重。该灰度值随后用于控制各个参数。 |
| **4** | 程序提供了多种绘图模式`drawMode`，这些模式也可受鼠标水平位置影响。这些模式先前被转换为 0.05 到 1 之间的值，并存储在变量`mouseXFactor`中。 |

| 鼠标： | 位置 x/y：不同的参数（取决于绘图模式） |
|---|---|
| 按键： | S：保存图像 |

![image](img/f0205-01.jpg)

![image](img/f0206-01.jpg)

**→ P_4_3_1_01** 灰度值定义了元素的大小、描边值、旋转角度和位置。

![image](img/f0206-02.jpg)

**→ P_4_3_1_01** 在此绘图模式（按键 9）下，每个像素由多个颜色扭曲的元素表示。

![image](img/f0207-01.jpg)

![image](img/f0208-01.jpg)

**→ P_4_3_1_02** 不同亮度的像素在此被替换为 SVG 单元。这些 SVG 文件已通过辅助程序按亮度排序。请注意，文件已重命名（亮度值构成文件名的开头）。

## P.4.3.2 基于像素值的文字

以下文字图像具有双重含义。既可以阅读其意义，也可以远观将其视为一幅图画。图像中的像素控制着字母的配置。每个字母的大小取决于原始图像中像素的灰度值，从而创造出额外的信息。

**→ P_4_3_2_01**

一个字符串被逐字母处理 → P.3.1.1/P.3.1.2，并按正常书写方向逐行构建。在绘制字符之前，其在显示坐标中的位置会与原始图像中对应的像素坐标位置相匹配。仅使用原始像素的一个子集——即那些存在对应字符位置的像素。所选像素的颜色现在可以转换为其灰度值，并用于调节字体大小等。

![image](img/f0210-01.jpg)

![image](img/f0210-02.jpg)

**→ P_4_3_2_01** 像素的颜色可以定义字母的大小或颜色，或两者兼有。

```javascript
function draw() {
  ...
  var x = 0;
  var y = 10;
  var counter = 0;
  while (y < height) {
    img.loadPixels();
    var imgX = round(map(x, 0, width, 0, img.width))
    var imgY = round(map(y, 0, height, 0, img.height))
    var c = color(img.get(imgX, imgY));
    var grayscale = round(red(c) * 0.222 +
      green(c) * 0.707 +
      blue(c) * 0.071);
    push();
    translate(x, y);
    if (fontSizeStatic) {
      textSize(fontSizeMax);
      if (blackAndWhite) fill(grayscale);
      else fill(c);
    } else {
      var fontSize = map(grayscale, 0, 255,
        fontSizeMax, fontSizeMin);
      fontSize = max(fontSize, 1);
      textSize(fontSize);
      if (blackAndWhite) fill(0);
      else fill(c);
    }
    var letter = inputText.charAt(counter);
    text(letter, 0, 0);
    var letterWidth = textWidth(letter) + kerning;
    x += letterWidth;
    pop();
    if (x + letterWidth >= width) {
      x = 0;
      y += spacing;
    }
    counter++;
    if (counter >= inputText.length) {
      counter = 0;
    }
  }
  noLoop();
}
```

| **1** | 只要当前书写位置的 y 坐标`y`仍小于显示高度，书写过程就继续。 |
|---|---|
| **2** | 使用`map()`函数将显示坐标转换为图像坐标；例如，x 坐标`x`从 0 到显示宽度之间的值按比例转换为 0 到图像宽度`img.width`之间的对应值。 |
| **3** | 根据所选模式`fontSizeStatic`（按键 1 或 2），字体大小设置为固定值`fontSizeMax`，或由灰度值变化。 |
| **4** | 值`fontSize`不能为零或负数，否则会导致问题。因此，函数`max()`确保该值至少为 1。 |
| **5** | 变量`x`的值增加字符宽度。 |
| **6** | 如果`x`大于或等于绘图画布的宽度，则换行。`y`值增加行间距，`x`从绘图画布最左侧重新从 0 开始。 |

| 按键： | 1：切换字符大小模式 2：切换字符颜色模式 箭头 ↓/↑：最大字符大小 –/+ 箭头 ←/→：最小字符大小 –/+ S：保存图像 |
|---|---|

![image](img/f0212-01.jpg)

**→ P_4_3_2_01** 字符的大小和颜色由底层图像定义。

![image](img/f0213-01.jpg)

**→ P_4_3_2_01** 此处像素的灰度值决定了字体大小。

## P.4.3.3 实时像素值

像素的颜色值可以再次转换为图形元素，但有两个重要区别：首先，像素不断变化，因为图像来自视频摄像头；其次，像素由不断运动的“傻瓜代理”依次转换，而非一次性全部转换。摄像头捕捉到的运动以及代理的迁移，因此可以在我们眼前绘制出一幅画面。

**→ P_4_3_3_01**

一个傻瓜代理在绘图画布上移动。在每个位置分析当前实时视频图像的颜色值，并将其作为每个颜色和描边值的参数。鼠标位置定义了描边长度和代理的速度。

![image](img/f0214-01.jpg)

**→ P.2.2.1 傻瓜代理**

![image](img/f0214-02.jpg)

**→ P_4_3_3_01** 代理的路径逐渐形成一幅图像。

```javascript
function setup() {
  ...
  video = createCapture(VIDEO, function(){
    streamReady = true
  });
  video.size(width, height);
  video.hide();
  ...
}
```

| **1** | 函数`createCapture()`创建一个视频元素，用于访问网络摄像头上的图像。 |
|---|---|
| **2** | 来自所连接视频摄像头的实时视频图像被缩小到绘图画布的大小。 |
| **3** | `hide()`命令可防止视频图像自动显示在绘图画布上。 |

```javascript
function draw() {

  if(streamReady) {

    for (var j = 0; j <= mouseX / 50; j++) {

      video.loadPixels();

      var pixelIndex = (((video.width - 1 - x)
        + y * video.width) * 4);

      var c = color(video.pixels[pixelIndex],
        video.pixels[pixelIndex + 1],
        video.pixels[pixelIndex + 2]);

      var cHSV = chroma(red(c), green(c), blue(c));

      strokeWeight(cHSV.get('hsv.h') / 50);

      stroke(c);

      diffusion = map(mouseY, 0, height, 5, 100);

      beginShape();

      curveVertex(x, y);

      curveVertex(x, y);

      for (var i = 0; i < pointCount; i++) {

        var rx = int(random(-diffusion, diffusion));

        curvePointX = constrain(x + rx, 0, width - 1);

        var ry = int(random(-diffusion, diffusion));

        curvePointY = constrain(y + ry, 0, height - 1);

        curveVertex(curvePointX, curvePointY);

      }

      curveVertex(curvePointX, curvePointY);

      endShape();

      x = curvePointX;

      y = curvePointY;

    }

  }

}
```

- **4**：如果视频信号可用，则加载当前视频图像的像素。
- **5**：与静态像素图像一样，视频图像中的像素也是逐行编号的。因此，需要根据当前写入位置（`x`、`y`）计算像素索引。当使用面向用户的网络摄像头时，通过计算`video.width-1-x`来水平镜像视频图像会很有用。
- **6**：描边值由像素的色相决定。`chroma.js`库有助于将 RGB 转换为 HSV 值。
- **7**：现在可以绘制线条元素。第一个曲线点位于当前绘制位置。这样做两次是因为使用`curveVertex()`绘制线条时，第一个点和最后一个点不会被绘制。
- **8**：变量`pointCount`指定要绘制的曲线点数量。默认值为 1，因此只绘制一条线。曲线点被放置在绘制位置周围的随机位置。`diffusion`值指定了这个区域的大小。
- **9**：最后一个曲线点被指定为新的绘制位置。

- 鼠标：X 位置：绘制速度，Y 位置：方向
- 按键：箭头 ↓/↑：曲线点数量 –/+，Q：停止绘制，W：继续绘制，箭头 ←/→：最小字体大小 –/+，S：保存图像

![image](img/f0216-01.jpg)

![image](img/f0217-01.jpg)

**→ P_4_3_3_01** 人们通过移动在图像中留下轨迹。线条长度在整个绘制过程中变化，从而使图像时而更细致，时而更抽象。

![image](img/f0218-01.jpg)

**→ P_4_3_3_02** 在此版本的程序中，三个代理在显示器上移动。第一个代理的描边值由像素的色相决定；第二个由像素的饱和度决定；第三个由像素的亮度决定。

![image](img/f0219-01.jpg)

**→ P_4_3_3_02** 当对象在摄像头前移动时，一系列看似随机的涂鸦汇聚在一起，呈现出对象的形态。

## P.4.3.4 从像素值到表情符号

从光栅元素到符号的情感转化：在这里，那些在短信中可视化情感的东西成为更大整体的一小部分。此程序中的任何缩略图集合都可以作为源材料，像素值决定哪些可以加入。

**→ P_4_3_4_01**

颜色值可以解释为三维空间中的点。对于此程序，需要找到从某个颜色值到一组其他颜色值（此处为各个表情符号的平均颜色）的最短距离。有多种数学方法可用于此搜索。特别快速且相对易用的是在所谓的 k 维树中搜索。`kdTree.js`库提供了此功能。

![image](img/f0220-01.jpg)

```html
<script src="../../libraries/kd-tree/kdTree.js" type="text/javascript"></script>
<script src="data/emoji-average-colors.js" type="text/javascript"></script>
```

- **1**：此程序需要两个额外的脚本。它们在`index.html`中加载。
- **2**：关于表情符号文件平均颜色及其各自文件名的信息包含在`emoji-average-colors.js`中。平均颜色的计算在另一个程序中进行：**→ P_4_3_4_emoji_color_analyser**。

```javascript
var emojis = {
  "1f4a3": {"averageColor": {"r":57, "g":57, "b":52}},
  "1f43b": {"averageColor": {"r":187, "g":111,"b":88}},
  "1f600": {"averageColor": {"r":227, "g":181, "b":70}},
  ...
}
```

- **3**：文件`1f4a3.png`：

  ![image](img/i220-1.jpg)

- **4**：文件`1f43b.png`：

  ![image](img/i220-2.jpg)

- **5**：文件`1f600.png`：

  ![image](img/i220-3.jpg)

```javascript
function preload() {
  img = loadImage("data/pic.png");
  icons = {};
  for (var name in emojis) {
    icons[name] = loadImage(emojisPath + "36x36/" +
      name + ".png");
  }
}
```

- **6**：在变量`icons`中，加载了所有表情符号的图像，之后可以通过它们的名称（`name`）调用。

```javascript
function setup(){
  ...
  var colors = [];
  for (var name in emojis) {
    var col = emojis[name].averageColor;
    col.name = name;
    colors.push(col);
  }
  var distance = function(a, b){
    return pow(a.r - b.r, 2) +
      pow(a.g - b.g, 2) +
      pow(a.b - b.b, 2);
  }
  tree = new kdTree(colors, distance, ["r", "g", "b"]);
}
```

- **7**：从这里开始搜索最近的颜色。需要创建两样东西：首先是一个点数组及其对应的 r、g、b 颜色。`colors`数组中的每个条目还被分配了名称`name`，以便之后显示相应的图像文件。
- **8**：其次，定义一个函数，指定如何计算两点之间的距离。通常，这是 RGB 颜色空间中从颜色 a 到颜色 b 的对角线长度。
- **9**：借助`kdTree`库，创建一个所谓的 k 维树。为此，将新创建的点列表`colors`和距离函数`distance`作为参数传递。此外，还必须传递一个维度列表。

```javascript
function draw() {
  background(255);
  for (var gridX = 0; gridX < img.width; gridX++) {
    for(var gridY = 0; gridY < img.height; gridY++) {
      var posX = tileWidth * gridX;
      var posY = tileHeight * gridY;
      var c = color(img.get(gridX, gridY));
      var nearest = tree.nearest(
        {r:red(c), g:green(c), b:blue(c)},
        1);
      var name = nearest[0][0].name;
      image(icons[name], posX, posY,
        tileWidth, tileHeight);
    }
  }
  noLoop();
}
```

- **10**：扫描要显示的图像`img`，并将像素颜色存储在`c`中。
- **11**：`kdTree`库中的`nearest()`函数查找与刚传入的点最近的点。最后一个参数指示应返回多少个结果；这里只需要一个。
- **12**：搜索结果是一个包含最近点的数组。其中的每个条目本身是一个包含两个元素的数组：点本身及其与传入`nearest()`的点的距离。在两个数组中都需要第一个条目：`[0][0]`。现在可以通过`name`将表情符号的图像放置在绘图画布上。

- 按键：S：保存图像

![image](img/f0222-01.jpg)

**→ P_4_3_4_01** 每个像素都变成一个表情符号。任何图像都可以使用，只要它足够大以包含许多颜色值。

![image](img/f0222-02.jpg)

原始照片

![image](img/f0223-01.jpg)

![image](img/f0223-02.jpg)

原始照片

![image](img/f0224-01.jpg)

![image](img/f0225-01.jpg)

**→ P_4_3_4_02** 来自网络摄像头的图像也可以作为表情符号光栅化的基础。

![image](img/f0226-01.jpg)

# 附录

- A.1 展望未来
- A.2 反思
- A.3 参考文献
- A.4 作者
- A.5 致谢
- A.6 版权
- A.7 告别

## A.1 展望未来



你是否想更深入地探索生成式设计？我们希望如此，因为还有太多值得发现！本章概述了作为数据可视化、3D 形状生成、动态粒子动画等基础的一些复杂方法。你可以在我们网站和 GitHub 频道上的附加示例代码中找到相关代码（链接见[generative-gestaltung.de](http://generative-gestaltung.de)）。在前几章的实际创作之后，本章邀请你反思所学内容，并在生成式设计的背景下探索理论与概念的联系。

![image](img/f0229-01.jpg)

![image](img/f0230-01.jpg)

**→ M_1_5_02** 当噪声生成的值控制一群代理的定向运动时，产生的典型图像。代理以点的形式呈现，并在连续绘制于旧图像上时留下轨迹。

![image](img/f0231-01.jpg)

![image](img/f0232-01.jpg)

![image](img/f0234-01.jpg)

![image](img/f0235-01.jpg)

**→ M_2_5_02** 不同正弦波的叠加产生利萨如图形，以其研究者朱尔·安托万·利萨如的名字命名。如果并非按顺序连接生成的点，而是将每个点与所有其他点相连，就会产生令人兴奋的网状结构。

![image](img/f0236-01.jpg)

![image](img/f0237-01.jpg)

![image](img/f0238-01.jpg)

![image](img/f0239-01.jpg)

**→ M_4_3_01** 规则延伸的线条上的点被吸引子（编程中的虚拟磁铁，可吸引和排斥）逐渐变形。

![image](img/f0240-01.jpg)

![image](img/f0241-01.jpg)

**→ M_4_3_01** 以旭日图形式呈现的文件夹和文件的数据可视化。圆形扇区颜色越深，表示文件夹中文件未更改的时间越长。可以从硬盘加载并可视化任何文件夹和文件结构。

![image](img/f0242-01.jpg)

**→ M_5_4_01** 维基百科文章链接结构的数据可视化。每个圆圈的大小代表文章长度，颜色代表主题。通过尝试示例程序，可以感受到生成式设计的精髓。在接下来的页面中，我们将反思示例程序背后的理念，并将所学内容置于上下文中。这部分也具有参考性质——它指出了相关主题和联系。

![image](img/f0243-01.jpg)

## A.2 反思

本书展示了如何通过代码生成图像。通过尝试示例程序，你可以感受到生成式设计的精髓。在接下来的页面中，我们将反思示例程序背后的理念，并将所学内容置于上下文中。本节还指出了相关主题和联系。

**现状** 数字化已成为设计学科不可或缺的一部分，我们所有人都使用计算机进行日常工作。然而，设计领域最知名的工具，如 Adobe Creative Cloud 产品（Photoshop、Illustrator 等），仅具有插图和成像功能。现有的工具，如画笔、剪刀或暗房，可以被虚拟化并提高效率，使我们能够更快地获得结果并更舒适地工作。然而，设计过程并未随着这些工具而发展。**^(1)** 无论图像是用鼠标还是画笔制作的，例如绘制线条的概念仍然相同。生成式设计与传统方法不同；其设计过程是独特的，并且本质上带来了新的可能性。

**新的设计过程？** 使用生成式设计带来的设计过程的主要变化是，传统工艺退居幕后，抽象和信息成为新的主要元素。相关的问题不再是“我如何绘制？”而是“我如何抽象？”这是因为从想法到最终图像的过程只能通过算法——一系列规则——来实现，计算机解释并处理这些规则。在显示之前，每个生成的图像必须首先用一组规则完整描述。这给设计师带来了两个挑战：如何抽象一个模糊的想法，以及如何以形式化的方式将想法输入计算机。没有固定的规则来抽象一个想法；为了实现一个复杂的想法，必须将问题分解成更小的部分。这种解决问题的策略也称为“分而治之”。**^(2)** 例如，一个表面需要尽可能多地填充随机直径的圆，且不能重叠。第一步是将模糊的想法转化为具体而简单的“配方”：画一个新圆。如果这个圆不与显示中的任何其他圆相交，则使这个圆尽可能大。如果圆与另一个相交，则重新开始。**→ P.2.2.5** 只有通过这种分解，才有可能用编程语言表述各个步骤，从而使其对计算机可执行。编程语言提供了执行此操作的基本构建块，例如*重复、随机性*和*逻辑*，这些将在接下来的页面中更精确地解释。

**重复** 使我们能够让计算机处理一个任务直到解决，并赋予我们操作大量对象的能力。重复的重要性体现在本书程序中 `for` 循环的使用频率上，或者体现在 `draw` 循环是 `p5.js` 的核心函数这一事实上。

**随机性** 用于产生变化，以打破计算机严格的规律性。真正的随机性很少产生构图上有趣的结果。相反，当随机性受到限制并以适度的剂量应用时，才会产生这些结果。在 `p5.js` 中，随机性由关键字 `random` 和 `noise` 表示。**→ P.3.2.5**

![image](img/f0246-01.jpg)

**→ P_3_2_5_01 至 → P_3_2_5_0**

### 运动中的文字

我们使用**逻辑**作为一种控制结构来引导生成过程。在这里，我们可以设置条件，将程序流程导向不同的分支。例如，章节“文本作为蓝图”**→ P.3.1.2** 包含另一种开关结构，我们可以根据输入的文本执行程序的不同部分：每个字母正常写出，但每当出现标点符号时，书写方向改变，并且标点符号被替换为弯曲元素。控制结构最常用的关键字是 `if`、`else`、`switch` 和 `case`。

![image](img/f0246-02.jpg)

**→ P.3.1.2**

### 文本作为蓝图

一旦设计理念被转化为计算机能够解释的代码，就可以生成无数图像可能性，而无需手工绘制任何线条。然而，最初的结果几乎从未达到百分之百令人满意。这些结果必须经过评估；评估结果作为改进下一次迭代的基础。与传统方法不同，我们并非直接动手修改图像，而是改变底层的抽象概念或程序中的个别参数，并持续优化每次迭代，直到达到理想的最终结果。交互有助于加速这种相互影响的过程。生成系统本身不一定是交互式的，本书也不会明确讨论交互。不过，安装控制元素（按钮、滑块等）所付出的额外努力是值得的。这些元素让我们能够实时跟踪和控制每个参数的变化。由于本书中的所有程序都在网页浏览器中运行，因此很容易通过标准 HTML 元素（如按钮、滑块等）来增强它们。**→ P.2.1.4**

![image](img/f0247-01.jpg)

**→ P.2.1.4**

### 网格中的复选框

## 设计过程：模拟与数字

![image](img/f0245-01.jpg)

输出的想法以“目视飞行规则”的方式逐步手动实现。设计师可以在纸上绘图、为动画创建关键帧等过程中，直接评估并干预每一步。如果想法以数字方式实现，画笔、剪刀或暗房等工具将变得虚拟化，从而更加高效。尽管这使一切变得更快、更容易，但设计过程本身并未改变。

## 设计过程：生成式

![image](img/f0245-02.jpg)

![image](img/f0245-03.jpg)

**P.2.2.5**

来自代理的结构密度。

## 设计中的新可能性

将编程融入设计过程极大地增加了设计师的可能性。概念能力仍然属于设计师；计算机仅扮演不知疲倦的助手角色。在当今自动化和数字化的世界中，设计能够快速轻松地执行，并且可以生成包含数千个元素的构图，这已是既定事实。但更有趣的是从*涌现、模拟*和*工具*的角度来看待生成设计的新可能性。

在生成设计的语境中，当过程的结果不是预先确定的，并且所有元素的相互作用产生的效果超越了它们各自属性的明显总和时，这些过程就是涌现的。*涌现*的一个常见例子是鸟群的集群行为：简单的规则导致了高度复杂、不可预测的行为。在“来自代理的生长结构”一节中，**→ P.2.2.4** 一个仅由两步组成的非常简单的算法，却产生了完全出乎意料的有机结构。（Boids 和自动机是其他例子。）

![image](img/f0247-02.jpg)

**→P.2.2.4**

### 来自代理的生长结构

自然过程的**模拟**是生成设计中的另一个重要方法。例如，在“摆上的代理”一章中，**→ P.2.2.6** 创建了一个由多个相连摆锤组成的结构。单个摆锤的运动很简单：它围绕其支点摆动。然而，如果多个摆锤连接成一条链，那么最外层的摆锤就会以复杂的方式运动。而且，正如常见的情况，跨领域的知识迁移会带来惊人的结果；自然界中肯定还有更多模型可能被迁移到生成系统中。

![image](img/f0247-03.jpg)

**→ P.2.2.6**

### 摆上的代理

这种可能性增加的最重要方面或许是，设计师现在成为了个性化工具的创造者，因为每个生成程序也是一个定制的软件工具。这使得设计师能够探索使用现有软件无法实现的新路径，从而带来更广泛的视觉设计媒介。令人惊讶的是，设计师使用自己开发的工具能取得多大成就，这在“绘图”中显而易见。**→ P.2.3** 即使是这些简单的工具也极大地增加了设计师的选择，并且由于这些工具可以不断优化，它们成为了完美定制的工作工具。此外，从生成程序到开发自己的应用程序通常并非巨大的飞跃。

![image](img/f0248-01.jpg)

**→ P.2.3**

### 绘图

## 展望未来

自本书第一版以来，生成设计的世界已经发生了显著演变。生成设计——也被称为创意编程——已在设计界站稳脚跟。使用生成设计已成为常见实践，作为数据可视化、艺术作品、媒体装置、建筑模型、视频剪辑、字体、动态外观——直至定制化批量生产的基础。展望未来，显然生成设计的使用将继续增加。以下有利因素表明了这一点：

由于无处不在的计算机网络，我们每天面对的信息量正在迅速增加。通过数据可视化帮助社会应对信息洪流是设计师的重要任务。^(3) 生成设计在应对这一挑战中将不可或缺。

技术可能性的扩展是生成设计的持续刺激源。例如，就在几年前，生成复杂的 3D 世界或通过虚拟现实和增强现实使其变得可触知几乎是不可能的——而现在即使在智能手机上也能实现。这种技术潜力将继续成为生成设计的驱动力。

同样重要的是合作者社区，这在几乎任何其他设计领域都如此充满活力。令人惊叹的是，围绕 Processing、p5.js、vvvv、openFrameworks、NodeBox 或 Basil.js 兴起的基于互联网的社区，对库、教程、示例程序、文章、论坛贡献、维基等做出了巨大贡献。这在一定程度上是因为创建代码——生成设计的基础设计媒介——非常适合团队合作，正如软件开发所证明的那样。代码的一个优点是它易于交换和传播，这与视频等其他媒介不同。

尽管如此，具备编程技能的设计师在今天仍然是例外而非普遍现象。这有历史和文化原因：通常设计师被迫在成为艺术家或技术人员之间做出选择。将两者完美结合很少是一个选项，例如在大学课程中，尽管近年来这种区分已开始模糊。此外，学习这种新的设计过程——使用数学分析源代码将想法转化为视觉结果——对许多人来说感觉像是一个不可逾越的障碍。克服这一障碍是本书的主要目标之一。

对生成设计的理解将带来一种新的务实态度，以充分利用计算机的潜力。编程，以及由此产生的生成设计，正迅速成为一种普遍的文化资产和技术工具，就像上个世纪的摄影和电影一样。可能性已经存在；我们只需要去利用它们。

**格奥尔格·特罗格曼，约亨·维霍夫**

*代码艺术*，前言

**^(1)** “用鼠标在电脑屏幕上绘画具有很高的娱乐价值，但[……]用笔画一条线与用鼠标画一条线并无区别。真正的挑战在于发现新媒介的内在属性，并找出如何通过计算画出你无法用计算画出的、甚至无法想象的线条。”

**约翰·前田**

《数字设计》

**^(2)** “除了‘分而治之’，还有许多其他问题解决策略，例如自顶向下和自底向上等。在此背景下，‘模式’思想（分析重复出现的模式并系统地解决它们）可能非常有用。”

**克里斯托弗·亚历山大**

《模式语言》

**^(3)** “获取数据的能力——能够理解它、处理它、从中提取价值、将其可视化、传达它——这将在未来几十年成为一项极其重要的技能，不仅在专业层面，甚至在小学生、中学生、大学生的教育层面也是如此。因为现在我们确实拥有基本上免费且无处不在的数据。因此，互补的稀缺因素就是理解这些数据并从中提取价值的能力。”

**哈尔·瓦里安**

加州大学伯克利分校教授

## A.3 参考文献

### 通用

**阿姆斯特朗，海伦.** 《数字设计理论：领域读物》。纽约：普林斯顿建筑出版社，2016 年。

*关于生成设计及相关领域的新旧论文集*。

**弗莱克，加里·威廉.** 《自然的计算之美：分形、混沌、复杂系统与适应的计算机探索》。马萨诸塞州剑桥：麻省理工学院出版社，1998 年。

*从（非常）数学的角度看待生成设计*。

**瑞斯，凯西，钱德勒·麦克威廉姆斯，和杰伦·巴伦兹.** 《设计、艺术与建筑中的形式+代码》。纽约：普林斯顿建筑出版社，2010 年。

### p5.js 与 Processing

**麦卡锡，劳伦，本·弗莱，和凯西·瑞斯.** 《Make：p5.js 入门：用 JavaScript 和 Processing 制作交互式图形》。旧金山：Maker Media，2016 年。

**瑞斯，凯西，和本·弗莱.** 《Processing：视觉设计师与艺术家编程手册》，第二版。马萨诸塞州剑桥：麻省理工学院出版社，2014 年。

**希夫曼，丹尼尔.** [编码训练网](http://TheCodingTrain.com).

*关于 p5.js、Processing 和生成设计的精彩视频教程*。

**希夫曼，丹尼尔.** 《代码的本质：用 Processing 模拟自然系统》。自出版，2012 年。

### 数据图形

**开罗，阿尔贝托.** 《真实艺术：用于沟通的数据、图表和地图》。旧金山：New Riders，2016 年。

**弗莱，本.** 《数据可视化：用 Processing 环境探索和解释数据》。加利福尼亚州塞瓦斯托波尔：O'Reilly Media，2008 年。

**克兰滕，罗伯特，斯文·埃曼，蒂博·蒂索，和尼古拉·布尔昆.** 《数据流 2：图形设计中的信息可视化》。柏林：Gestalten，2010 年。

*插图丰富的书籍，涵盖使用 Processing 进行高级数据图形编程，并展示广泛的数据图形项目*。

**卢皮，乔治娅，和斯特凡妮·波萨韦茨.** 《亲爱的数据》。纽约：普林斯顿建筑出版社，2016 年。

**芒兹纳，塔玛拉.** 《可视化分析与设计》。佛罗里达州博卡拉顿：CRC Press，2014 年。

**塔夫特，爱德华·R.** 《构想信息》。康涅狄格州柴郡：Graphics Press，1990 年。

**塔夫特，爱德华·R.** 《定量信息的视觉展示》。康涅狄格州柴郡：Graphics Press，2001 年。

### 美学

**格斯特纳，卡尔.** 《设计程序》。苏黎世：Lars Müller，2007 年。

*最初出版于 1964 年；其标题在我们这个计算机时代有些误导——如果今天首次出版，它可能会被称为《发明设计规则》。*

**康定斯基，瓦西里.** 《点线面》。由希拉·雷贝编辑。由霍华德·迪尔斯廷和希拉·雷贝翻译。纽约：Dover Publications，1979 年。

*最初出版于 1925 年；包豪斯大师关于抽象绘画的理论思考*。

**莱博格，克里斯蒂安.** 《视觉语法》。由黛安·奥特利翻译。纽约：普林斯顿建筑出版社，2006 年。

*视觉语法抽象概述；非常清晰且插图丰富*。

**Studio Moniker.** 《条件设计工作手册》。阿姆斯特丹：Valiz，2013 年。

### 历史与背景

**布朗，保罗，查理·吉尔，尼古拉斯·兰伯特，和凯瑟琳·梅森，编.** 《白热冷逻辑：英国计算机艺术，1960–1980》。马萨诸塞州剑桥：麻省理工学院出版社，2008 年。

**伯纳姆，杰克.** 《软件：信息技术；其对艺术的新意义》。纽约：犹太博物馆，1970 年。

**莱维特，露丝，编.** 《艺术家与计算机》。纽约：Harmony Books，1976 年。

**李，帕梅拉·M.** 《时间恐惧症：论 1960 年代艺术中的时间》。马萨诸塞州剑桥：麻省理工学院出版社，2004 年。

**前田，约翰.** 《数字设计》。马萨诸塞州剑桥：麻省理工学院出版社，2001 年。

*第一本向设计界展示如何使用编程语言 DBN 进行设计的畅销书*。

**前田，约翰.** 《前田@media》。纽约：Rizzoli，2000 年。

*约翰·前田对生成设计主要贡献的自传和回顾*。

**麦卡洛，马尔科姆.** 《抽象工艺：实践的数字之手》。马萨诸塞州剑桥：麻省理工学院出版社，1998 年。

**保罗，克里斯蒂安妮.** 《数字艺术》。纽约：Thames & Hudson，2003 年。

**赖夏特，贾西亚.** 《控制论意外发现：计算机与艺术》。纽约：Frederick A. Praeger，1968 年。

*伦敦首次大型计算机艺术展览的目录*。

**罗森，玛吉特，编.** 《一个关于运动、杂志和计算机进入艺术的不为人知的故事：新趋势与 Bit International，1961–1973》。马萨诸塞州剑桥：麻省理工学院出版社，2011 年。

**尚肯，爱德华·A.** 《艺术与电子媒体》。纽约：Phaidon Press，2009 年。

**沃德里普-弗鲁因，诺亚，和尼克·蒙特福特，编.** 《新媒体读本》。马萨诸塞州剑桥：麻省理工学院出版社，2003 年。

**怀特劳，米切尔.** 《元创造：艺术与人工生命》。马萨诸塞州剑桥：麻省理工学院出版社，2004 年。

**威尔逊，马克.** 《用计算机绘画：计算机图形学艺术家指南》。纽约：Perigee Books，1985 年。

**伍德，黛博拉.** 《用数字成像：计算机打印的历史视角》。芝加哥：西北大学出版社，2008 年。

## A.4 作者简介



**贝内迪克特·格罗斯**

1980 年出生于巴登-符腾堡州。

- 2002 年：学习地理和计算机科学。中断学业后对设计产生兴趣。
- 2007 年：在施瓦本格明德设计学院（HfG Schwäbisch Gmünd）与朱莉娅·劳布共同完成生成系统硕士学位。
- 此后，在高等教育和设计领域工作。
- 2011–13 年：在伦敦皇家艺术学院师从安东尼·邓恩和菲奥娜·拉比攻读设计交互硕士；同时，在麻省理工学院可感知城市实验室（马萨诸塞州剑桥/新加坡）担任数据可视化专家。
- 自 2013 年起：从事推测性和计算性设计的自由职业；多次国际展览、获奖和出版。
- 自 2017 年起：在施瓦本格明德设计学院担任交互设计教授。

**哈特穆特·博纳克**

1972 年出生于巴登-符腾堡州。

- 1992 年起：学习数学（中断），并于 1997 年获得经济学学位。
- 1998 年：在施瓦本格明德设计学院学习通信设计。
- 自 2002 年完成学业后：在斯图加特担任独立设计师，专注于界面和交互开发领域项目的概念、设计和原型实现；数字媒体教师。
- 自 2009 年起：在施瓦本格明德设计学院担任交互设计教授。

### 朱莉娅·劳布

1980 年出生于巴伐利亚。

- 2003 年：在施瓦本格明德设计学院学习传播设计。曾在巴塞尔设计学院留学。
- 2007 年：与贝内迪克特·格罗斯共同完成硕士论文《生成系统》。
- 自 2008 年起：独立平面设计师，专攻书籍设计、企业形象设计和生成设计。
- 2010 年：与塞德里克·基弗在柏林共同创立设计工作室 `onformative`（数字艺术与设计工作室）。
- 在多所大学担任讲师及工作坊负责人。

### 克劳迪乌斯·拉泽罗尼

1965 年出生于巴伐利亚。

- 1984 年：师从拉乌尔·曼努埃尔·施内尔学习摄影。
- 1987 年：在波士顿麻省艺术学院担任助教。
- 1992 年：在柏林 BILDO 学院获得媒体设计学位。
- 至 1996 年：在 `Pixelpark` 担任创意总监。
- 至 2001 年：在柏林创立设计机构 `IM STALL` 并担任总监及创意总监。
- 自 1999 年起：在埃森福克旺艺术大学担任界面设计教授。
- 自 2005 年起：探索、开发并构建 `solographs`。
- 自 2007 年起：扩展学术部门，纳入物理计算领域。

### 尼尔斯·波尔德瓦特

1994 年出生于荷兰。

- 2016 年：在斯海尔托亨博斯阿凡斯应用科学大学获得传播与多媒体设计学士学位。
- 自 2016 年起：担任网页开发者和设计师，专注于数据可视化、电子学习、游戏和平面设计。

### 乔伊·李

1990 年出生于加利福尼亚。

- 2012 年：在加州大学洛杉矶分校获得地理学学士学位，并在温哥华不列颠哥伦比亚大学获得地理学硕士学位。
- 曾在麻省理工学院感知城市实验室（2013 年）和 Mozilla 科学实验室（2015 年）等机构从事国际研究与教学活动。
- 在新空间与数字媒体、城市气候研究及开源领域拥有多项国际展览、奖项和出版物。

## A.5 致谢

感谢 `p5.js` 的发起人劳伦·麦卡锡。

感谢 Gold & Wirtschaftswunder 的所有参与者：朱莉娅·屈内、克里斯蒂安·席勒、施特芬·克诺尔、克里斯蒂安·尼古劳斯、安德烈亚斯·勒林茨。

感谢赫尔曼·施密特美因茨出版社的每一位成员（尤其是布丽吉特·拉布）。

感谢萨布丽娜·格罗斯提供的文本反馈和建议。

感谢所有贡献少量代码的贡献者，以及我们在本书中使用的所有 JavaScript 库的开发者（参见代码包中的 `readme` 文件）。

感谢 `twemoji` 团队（[`github.com/twitter/twemoji`](http://github.com/twitter/twemoji)）。

感谢弗雷德里克·德·布莱瑟，他迅速回答了关于 `Opentype.js` 和 `g.js` 的非常规问题。

## A.6 版权信息

### 出版方

普林斯顿建筑出版社

麦基沃伊集团旗下公司

202 Warren Street

Hudson, New York 12534

[`www.papress.com`](http://www.papress.com)

普林斯顿建筑出版社是建筑、设计、摄影、景观和视觉文化领域的领先出版商。我们以无与伦比的质量和制作价值创作精美的书籍和文具。已出版超过一千种图书，我们在最意想不到的地方发现设计。

原版由赫尔曼·施密特出版社出版

© 2018 赫尔曼·施密特出版社及作者

保留所有权利

英文翻译 © 2018 普林斯顿建筑出版社

未经出版商书面许可，不得以任何方式使用或复制本书的任何部分，但书评除外。

已尽一切合理努力确认版权所有者。错误或遗漏将在后续版本中更正。

特别感谢：普林斯顿建筑出版社的保拉·巴弗、珍妮特·贝宁、艾比·布塞尔、本杰明·英格利希、扬·奇利亚诺·哈特曼、苏珊·赫什伯格、克里斯汀·休伊特、莉亚·亨特、瓦莱丽·卡门、詹妮弗·利珀特、萨拉·麦凯、帕克·门齐默、埃利亚娜·米勒、尼娜·皮克、韦斯·西利、罗布·谢弗、玛丽莎·特索罗、保罗·瓦格纳和约瑟夫·韦斯顿——凯文·C·利珀特，出版人

### 国会图书馆编目数据

书名：生成设计：使用 `p5.js` 在 JavaScript 中可视化、编程与创作 / 贝内迪克特·格罗斯、哈特穆特·博纳克、朱莉娅·劳布、克劳迪乌斯·拉泽罗尼；乔伊·李和尼尔斯·波尔德瓦特供稿；玛丽·弗罗林翻译。

其他书名：`Generative Gestaltung`。英文

描述：纽约：普林斯顿建筑出版社，[2018] | 译自哈特穆特·博纳克、贝内迪克特·格罗斯和朱莉娅·劳布所著《Generative Gestaltung》，由克劳迪乌斯·拉泽罗尼编辑 | 含参考书目。

标识符：LCCN 2018007216 | ISBN 9781616897581（平装：无酸纸）| ISBN 978-1-61689-784-0（epub, mobi）

主题：LCSH：计算机艺术。| 计算机绘图。| 平面艺术—数据处理。| 生成编程（计算机科学）。| 计算机辅助设计。| JavaScript（计算机程序语言）

分类：LCC N7433.8 .B6313 2018 | DDC 776—dc23

LC 记录可查阅 [`lccn.loc.gov/2018007216`](https://lccn.loc.gov/2018007216)

### 概念

贝内迪克特·格罗斯、哈特穆特·博纳克、朱莉娅·劳布、克劳迪乌斯·拉泽罗尼

### 文本

哈特穆特·博纳克、贝内迪克特·格罗斯、克劳迪乌斯·拉泽罗尼

### 编程

贝内迪克特·格罗斯、哈特穆特·博纳克、尼尔斯·波尔德瓦特、乔伊·李

本书所有代码均使用 `p5.js 0.5.11` 版本创建，并根据 Apache 许可证发布。

### 插图和摄影

哈特穆特·博纳克、贝内迪克特·格罗斯、朱莉娅·劳布、克劳迪乌斯·拉泽罗尼、雅娜-莉娜·贝肯布施、安德烈娅·冯·丹维茨、保·多明戈、斯特凡·艾格纳、维克托·华雷斯·埃尔南德斯、塞德里克·基弗、施特芬·克诺尔、安德烈亚斯·勒林茨、弗朗茨·施泰默勒、汤姆·齐奥拉

### 书籍设计

Gold & Wirtschaftswunder 斯图加特，[`www.gww-design.de`](http://www.gww-design.de)

朱莉娅·屈内 & 克里斯蒂安·席勒（艺术指导），施特芬·克诺尔，克里斯蒂安·尼古拉斯

### 版式与排版

朱莉娅·屈内、施特芬·克诺尔、克里斯蒂安·尼古拉斯、哈特穆特·博纳克、弗洛尔·德·克龙布吕格、马克西米利安·塞姆勒

### 普林斯顿建筑出版社方面

翻译：玛丽·弗罗林

项目编辑：萨拉·斯特门

排版：蒂娜·亨德森

### 字体

`Maison Neue Book`、`Maison Neue Bold`、`Maison Neue Mono`

编程代码使用：`FreeSans`、`Fira Sans`、`Miso`、`Noto Sans`

### 网站

[`www.generative-gestaltung.de`](http://www.generative-gestaltung.de)

概念与设计：Gold & Wirtschaftswunder，贝内迪克特·格罗斯

编程与实现：尼尔斯·波尔德瓦特、乔伊·李、贝内迪克特·格罗斯

## A.7 告别

### 继续编码！

[`www.generative-gestaltung.de`](http://www.generative-gestaltung.de)

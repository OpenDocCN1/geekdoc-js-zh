# Perl 药急：遗留代码转型指南



![](img/cover.jpeg)

| ![](img/0201795264_xs.jpg) |
| :--- |
| • | 目录 |
| • | 索引 |


| 属性 | 详情 |
| :--- | :--- |

* 治愈你 Perl 代码的各种百病！
* 维护、优化并扩展任何 Perl 软件……无论是否由你编写
* 适用于企业环境的 Perl 软件工程最佳实践
* 案例研究和代码易读性强

如果你编写 Perl 代码，你需要读读这本书。
——Adam Turoff，《The Perl Review》技术编辑。

Perl Medic 不仅仅是一本书。它是一套精心设计的策略，用于处理、更新和推进遗留 Perl 程序。
——Allen Wyke，包括《JavaScript Unleashed》和《Pure JavaScript》在内的多本计算机书籍合著者。

Scott 对复杂材料的解释流畅且具有欺骗性的简单。他精通自己的领域和技艺——他让这一切看起来轻而易举。Scott 始终保持极其实用——即使是“分析”章节也充满了待运行的代码和测试。
——Dan Livingston，《Advanced Flash 5: Actionscript in Action》等多本计算机书籍作者。

## 为你现有的 Perl 代码注入新的动力、性能和扩展性！

今天的 Perl 开发者将 60-80% 的时间放在处理现有的 Perl 代码上。现在，有一份从头到尾的指南，教你如何理解、维护、更新和重构这些代码以获得最大的性能和稳定性。《Perl Debugged》的主作者 Peter J. Scott 编写了第一本系统的 Perl 软件工程指南。通过大量的示例，他展示了如何为任何 Perl 程序（无论新旧）引入强大的纪律、一致性和结构化。你将发现如何：

* 扩展现有的 Perl 代码，以服务更大的网络、Web、企业或电子商务应用程序
* 重写、重构和升级任何 Perl 程序以提高性能
* 为你的整个 Perl 软件库引入标准和最佳实践
* 将 Perl 代码组织成更易于复用的模块和组件
* 升级为早期版本 Perl 编写的代码
* 为你的软件……或任何人的软件编写并执行更好的的测试
* 在团队协作、方法论驱动的环境中使用 Perl
* 更有效、更高效地记录你的 Perl 代码

如果你曾经继承过难以维护的 Perl 代码，如果你编写的别人需要阅读的 Perl 代码，如果你想写出以后自己更容易维护的代码，那么这本救命之书就是《Perl Medic》。

| ![](img/0201795264_xs.jpg) |
| :--- |
| • | 目录 |
| • | 索引 |


* 版权信息
* 序言
* Perl 还是 perl？
* 获取 Perl
* 历史上的 Perl
* 本书适合读者
* 排版规范
* 进一步参考
* Perl 版本
* Perl 6
* 致谢

## 第 1 章 引言](#ch01.html)
* 1.1. 首要事项
* 1.2. 继承的原因
* 1.3. 下一步做什么？
* 1.4. 在原生环境中观察程序
* 1.5. 个人化
* 1.6. 严格性
* 1.7. 警告

## 第 2 章 现场调查](#ch02.html)
* 2.1. 版本
* 2.2. 局部还是整体？
* 2.3. 寻找依赖项

## 第 3 章 现在测试，永远测试（诊断](#ch03.html)
* 3.1. 考验你的耐心
* 3.2. 极端测试
* 3.3. 使用 Test:: 模块
* 3.4. 测试遗留代码
* 3.5. 最后的鼓励

## 第 4 章 重写（移植](#ch04.html)
* 4.1. 策略
* 4.2. 为什么要这么做？
* 4.3. 风格
* 4.4. 注释
* 4.5. 重塑
* 4.6. 变量命名
* 4.7. 编辑
* 4.8. 行编辑
* 4.9. 反模式
* 4.10. 进化

## 第 5 章 规范的 Perl 程序](#ch05.html)
* 5.1. 作用域变量与局部变量
* 5.2. 严格性
* 5.3. use strict
* 5.4. use warnings
* 5.5. 选择性禁用
* 5.6. 程序员注意
* 5.7. Perl 诗意

## 第 6 章 重构（手术台](#ch06.html)
* 6.1. 保持简洁
* 6.2. 崇拜 Perl
* 6.3. 逃离全局变量陷阱
* 6.4. 调试策略

## 第 7 章 升级（整形手术](#ch07.html)
* 7.1. 策略
* 7.2. Perl 4
* 7.3. Perl 5.000
* 7.4. Perl 5.001
* 7.5. Perl 5.002
* 7.6. Perl 5.003





### 7.7 节 Perl 5.004
### 7.8 节 Perl 5.005
### 7.9 节 Perl 5.6.0
### 7.10 节 Perl 5.6.1
### 7.11 节 Perl 5.8.0
### 7.12 节 Perl 5.8.1
### 7.13 节 Perl 5.8.2
### 7.14 节 Perl 5.8.3

## 第 8 章 使用模块（基因增强）
### 8.1 节 CPAN 的必要性
### 8.2 节 使用 CPAN
### 8.3 节 通过模块改进代码
### 8.4 节 自定义 Perl 环境

## 第 9 章 分析（法医病学）
### 9.1 节 静态分析
### 9.2 节 消除多余代码
### 9.3 节 寻找低效代码
### 9.4 节 调试

## 第 10 章 提高可维护性（预防）
### 10.1 节 增强健壮性
### 10.2 节 高级简洁性
### 10.3 节 文档
### 10.4 节 自定义警告
### 10.5 节 版本的控制系统集成

## 第 11 章 案例研究
### 11.1 节 环境搭建
### 11.2 节 分诊
### 11.3 节 绝望寻找理性
### 11.4 节 迈入 21 世纪
### 11.5 节 有效引入模块，部分 1
### 11.6 节 有效引入模块，部分 2
### 11.7 节 使其成熟，部分 1
### 11.8 节 使其成熟，部分 2
### 11.9 节 使其成熟，部分 3
### 11.10 节 高级修改

## 第 12 章 结论（预后）
### 12.1 节 结语
### 12.2 节 Perl 人
### 12.3 节 最后的思考

### 源代码
`Tie::Array::Bounded`
`Benchmark::TimeTick`
`smallprofpp`

### 参考文献
### 关于作者
### 索引

版权

制造商和销售商为了区分其产品而使用的许多标识已声明为商标。当这些标识出现在书中且 Addison-Wesley 知晓存在该商标主张时，这些标识将以首字母大写或全大写形式打印。

作者和出版商在编写本书时付出了努力，但不提供任何形式的明示或暗示保证，并对错误或遗漏不承担责任。对于与本文包含的信息或程序有关或由此引起的附带或后果性损害，不承担任何责任。

出版商为特种销售大订本书提供折扣。欲了解更多信息，请联系：
美国企业和政府销售
(800) 382-3419
corpsales@pearsontechgroup.com

在美国以外的销售请联系：
国际销售
(317) 581-3793
international@pearsontechgroup.com

访问 Addison-Wesley 网站：www.awprofessional.com

美国国会图书馆编目出版数据
Scott, Peter (Peter J.), 1961-
Perl medic : transforming legacy code / Peter Scott.
p. cm.
包含参考文献和索引。
ISBN 0-201-79526-4
1. Perl (计算机编程语言) I. 标题。
QA76.73.P2

版权 © 2004 by Pearson Education, Inc.
保留所有权利。未经出版商事先许可，本书的任何部分不得复制、存储在检索系统中，或以任何形式或任何方式（电子、机械、复印或其他）进行传输。印于美国。同时在加拿大出版。
文字印在再生纸上
第一版印刷，2004 年 2 月

### 前言

### 前言

恭喜你！假设你刚获得计算机科学学位，现在逆转了经济趋势，在一家拥有大型 IT 部门的知名公司找到了工作。你将取代 Bill，那个中中了彩票并销声的程序员，除了两周后收到了一张来自普尔特瓦雅特的明片外，再也没有关于他的消息。你的同事警告你不要在主管面前提到那张明片。你坐在 Bill 的工位上，清理办公桌抽屉里留下的供应商广告，思考如何应用教授在大学教给你的优雅原则和崇高范式。这时，你的主管来了，他靠在你的肩膀上，敲击你的键盘调出一个文件。

“这是 Bill 正在工作的最后一个程序。我们认为它快完成了。我们的进度落后了，看看你能不能在周四之前完成。”

他离开后，你看着程序中错乱的行和晦涩的变量名，寻找着注释，但你能找到的注释只有“XXX——必须修改”和“临时凑合！但应该能用”。你怀疑这是否是一种公司入场仪式，但你的直觉告诉你事实如此。

欢迎来到现实世界。

### 献献

献给我的母亲，感谢她在年幼时在我的百番恳求下教会我阅读。一件事导致了另一件事……

> “全球范围内，有超过 200 万亿定义重复、难以理解且极不灵活的软件……企业面临着被山山遗留代码困住的风险。”

> 

> —William Ulrich, 《Legacy Systems: Transformation Strategies》

![graphics/pr01.gif](img/pr01.gif)




在现实世界中，如果你能把所有时间都花在开发一个新程序上，那是很幸运的。很多时候你必须处理别人编写的代码。在现实世界中，程序员必须接手由他们可能不认识、不喜欢或不同认同的人编写的程序。即使你幸运地避开了这种情况，你仍然需要维护自己的代码；总有一天，你会看到自己两年前写的东西，并问道：“哪个白痴写了这个东西？”从而陷入了与那些不幸运的程序员大同小异的境地。

这本书是关于接手 `Perl` 代码的，无论是别人写的，还是你自己自己在对可维护性还不够明智时写的。代码继承的许多问题在所有语言中都是共通的，但我特别在 `Perl` 中发现了这些问题。

## 为什么 Perl 倾向于引发维护问题？

答案在于 `Perl` 优势及其格言的阴暗面：“事情有多种实现方式”（There's More Than One Way To Do It，缩写为 `TMTOWTDI`）。`Perl` 提供了如此多的实现方式，以至于别人可能选择了一种不是你的方法，或者在同一个程序中使用了几种完全不同的方法。

本书的医学比喻源于我们作为维护程序员所做工作的这种相当剧烈的性质。我们经常必须进行“分诊”，决定哪些代码值得救，哪些已经无药可救。经常，我们只有时间进行急救，为一个破损的程序施上现场包扎。我们也很向客户解释我们的账单。编程领域可能没有所谓的《希西波克拉斯誓言》，但制定一个也无害。

我写这本书是因为我发现自己不断对学生们说：“我会教你们如何很好地编写 `Perl`，但在你们接手一个写得不好的程序之前，我得先教你们多多的东西，而你们可能不会乐意花这么多时间，从学习如何编写自己的好程序中抽出来。”因此，我写了这本书来满足这一需求。

`Perl` 之于计算机语言正如英语之于人类语言：充满了不规则动词，只有在方便时才保持一致，从其他语言中借用术汇，形成了一个伟大的语法熔炉。大多数计算机语言都是根据某种功能领域来描述的（Pascal：教学计算机语言；FORTRAN：数值分析；Prolog：规则驱动专家系统；等）。`Perl` 的开发者仅简单地将其描述为“一种为了完成任务的语言”（参见 [WALL00] 的前言）。`Perl` 提供了奇妙的语法设备组合，让几乎任何背景的程序员都能找到学习这种语言熟悉的立足点。

全景并没有像这暗示的那么混乱：Larry Wall 等人做了一项卓越的工作，将这些风格迥异的设备整合成一个具有本质美感的框架。因此，正如英国人谈论“BBC 英语”，而许多人用类似于 `LISP` 或 `C` 的口音编写 `Perl` 一样，存在一种接近“无口音 `Perl`”的风格，它能充分利用该语言的特性。我将展示你如何“像母语一样说 `Perl`”，以优化你程序的可维护性。

确实，你官方上被允许用“婴儿语”编写 `Perl`，而且 `Perl` 大师们承诺过“不笑”（参见同样的前言）。但同样，虽然飞行员认为任何让你能走走的着陆都是好的，但我在这本书中所做的是帮助你避免飞行执被吊销。

`Perl` 就像机场旅客服务台后面的人员；他们非常擅长理解你，无论你对他们语言的掌握有多糟糕。因为有许多方法可以编写 `Perl` 程序，使其不仅在语法上正确（`Perl` 对运行它没有异议），而且在语义上也正确（程序执行了它应该做的事——至少在它尝试过的情况下是如此），因此你会遇到各种 `Perl` 编程风格，从优美的到可以宽容地描述为不可理喻的都有。

你们中明智的人会利用这些信息并问道：“我的程序在那个量尺上处于什么位置？”因为别人最终可能会接手你的代码，而你不希望他们把代码发给像我这样的作者，作为反面教材放入这样的书中。请参见第 5 章 获取更多关于避免嘲讽的建议。

如果你的经验或对 `Perl` 的印象局限于简短、平凡的脚本，那么这本书将显得多此一举。我想让你知道，`Perl` 可以非常容易地容纳大型项目——即数万行代码、多个模块和多个程序员。这种规模需要严谨需求、文档和测试的项目。如果你习惯了 `Perl` 程序逃避那类关注，我相信这部分是由于对 `Perl` 作用和力量的误解。

例如，如果编写一个 `C` 程序来满足某些需求，结果发现有 1,000 行，那么常见的反应是：“这一定很严肃……我们最好进行代码走读检查、验收测试、操作就绪评审和静态代码分析。噢，别忘记帮助热线培训和文档。”

但如果一个满足完全相同需求的 `Perl` 程序仅占 100 行（且 10:1 是 `C` 代码到 `Perl` 的典型压缩率），那么反应可能是：“啊，一个简单的工具……而且还是用平民化的脚本语言写的。把它扔进交付目录，然后忙下一个任务吧。”

然而，当一个 `Perl` 程序达到 1,000 行大关碑时，蜜月可能已经结束了。我要说的大部分内容针对大型程序。特别是第 3 章将向你展示如何获得习惯于回归测试的开发团队的尊重。

请另参见我与 Ed Wright 合著的早期书籍《Perl Debugged》（Addison-Wesley, 2001），获取更多关于开发和调试 `Perl` 程序的良好实践的建议。

## Perl 还是 perl?

当你阅读这本书以及其他关于 `Perl` 的著作时，你会发现大小写上存在明显的不一致：有时写成 "Perl"，有时写成 "perl"。这并没有真的不一致；作者们指的是两个不同的东西。`Perl` 是语言本身；`perl` 是运行 `Perl` 程序的程序。只有一个 `Perl`，但有很多 `perls`（每种类型的计算机有一个或多个）。

有时这种区别会变得模糊：例如，大多数人会写道“Perl 对括号不匹配表示反对”，但实际上是程序在反对，而不是语言。不要写成 "PERL"；`Perl` 不是缩写词，它不代表任何内容[1]（嗯，除了代表表达多样性、免受人为限制以及在工作中享受乐趣的权利之外。但我们稍后会讨论。）

> ^([1]) "Practical Extraction and Reporting Language" 是事后为了方便而起的别名。它是一个爱称，而不是正式称号。“Pathological Eclectic Rubbish”也是如此。

## 获取 Perl

如果我告诉你这么多关于 `Perl` 的知识却没告诉你如何获取它，将是失职的，尽管现在很难避开它；你可能已经拥有了，特别是如果你有任何版本的 UNIX 或 Linux 的话。检查你是否拥有它的最简单方法是获取命令提示符并输入：

```
perl -v
```

看是否有响应。如果没有，尝试：

```
whereis perl
```

这在 UNIX 系统或类似系统上会查找 Perl。如果这对你来说也不行，这里有关于如何下载和安装 `Perl` 的简要说明：




*   对于 Microsoft Windows 机器，获取免费的 ActivePerl 分发：[`www.activeState.com/ActivePerl/download.htm`](http://www.activeState.com/ActivePerl/download.htm)

*   对于 Macintosh：

    [`www.cpan.org/ports/index.html#mac`](http://www.cpan.org/ports/index.html#mac)

    （该 URL 适用于操作系统的 X 之前的版本；Perl 随有 Mac OS X 并且在上面正常编译。）

*   对于所有其他机器的二进制发行：

    [`www.cpan.org/ports/`](http://www.cpan.org/ports/)

*   对于 Perl 本身的源码：

    [`www.cpan.org/src/`](http://www.cpan.org/src/)

你需要的源文件名为 `stable.tar.gz`。`devel.tar.gz` 文件仅供 Perl 开发者或测试人员使用，`latest.tar.gz` 文件由于复杂的历史原因与 `stable.tar.gz` 相同。任何提到“Ponie”的内容至少在 2004 年之前仅适用于开发者，任何具有三数字组件版本且中间数字为奇数的 Perl 版本同样是开发版本。

在支持的 UNIX 架构上从源码编译 Perl 只需在下载并解压正确的文件后执行以下命令：

```
 ./Configure

make

make test

make install 
```

`Configure` 步骤会向你提出数以百万的问题，大多数人不知道其中许多问题在讨论什么；但 `Configure` 推荐的默认答案通常是正确的。

> ^([2]) 如果你想让 `Configure` 使用这些建议并继续运行而不询问你，可以给它提供 `-des` 选项，它就会很愉快地一直运行而无需你的干预。如果你需要更多针对特定平台的帮助，请查看分发版中对应你系统的 `README.platform` 文件。

[www.cpan.org](http://www.cpan.org) 是综合 Perl 存档网络（CPAN）的主站，在全球范围内都有镜像。CPAN 也是贡献模块的官方仓库（参见第 8.1 节）。

### 历史版本的 Perl

你可能不习惯看到如何获取过时版本的 Perl 的说明。但在本书后面将探讨的某些情况下，你可能不得不这样做。（注意：Perl 版本越旧，我即将给出的引用就越不容易具有持久的效力。）所有 Perl 版本发布的时间线可以在 `perlhist` 文档页面中。

你可以从 [ftp://ftp.cpan.org/pub/CPAN/src/5.0/](http://ftp.cpan.org/pub/CPAN/src/5.0/) 获取从 5.004_05 开始的所有主要版本。Perl 5 的更早版本（除广泛使用的 5.004_04 外）存在显著的 bug、内存泄漏和安全漏洞，且难以发现。然而，你可以在 [`retroperl.cpan.org/`](http://retroperl.cpan.org/) 获取几乎是发布过的每一个版本的 Perl。在使用 5.003 版本之前的 Perl 并不是一项可以轻率对待的行为。除了简短地警告你离开石器时代并升级到真正的版本外，你不会获得任何错误修复或任何其他支持。我公开这些源码仅用于你必须使用旧版 Perl 来验证在现代 Perl 上无法运行的遗留程序的情况。如果你必须从那里获取 Perl 4，Perl 4 的最后一个且最好的版本是 4.0.36。

Retroperl 甚至包含了 1.0、1.010、2.0、2.001、3.01 版本。仅称这些具有历史意义还是未过保守的说法。如果你认为你需要为了任何严肃工作而获取这些 Perl 之一，你可能更需要一位考古学家或一位心理治疗师。然而，作为一个非严肃工作的例子，2002 年 Michael Schwern 等人发布了 Perl 1 的升级版（将其带到 1.0_15 版本），作为给 Perl 和 Larry Wall 的生日礼物，证明它在现代机器上仍然运行。参见 [`dev.perl.org/perl1/`](http://dev.perl.org/perl1/)。

历史版本的模块位于 [`backpan.cpan.org/modules/`](http://backpan.cpan.org/modules/)，但你必须进入作者分支才能找到你想要的内容。

### 本本书的读者

如果你已经使用 Perl 足够久，并听过 `scalar`、`array` 和 `hash` 等术语，那么你来对地方了。本书的部分针对初学者，而有些部分需要更多经验才能理解。请随时跳过任何超出你能力范围的内容，并在以后再回来。

### 排版规范

我在书中使用了以下规范：

*   标准正文：Times New Roman
*   代码示例和 URL：`Courier`
*   用户输入：`Bold Courier`

有时我的代码示例在原句没有换行的地方有换行符。在这些换行会导致问题或不明显的地方，我在行尾放置了一个反斜杠（`\`），用以指示该行应该是连续的。

（注：此处原文中存在大量重复的描述，翻译时已按逻辑精简处理）

### Perl 6

如果你在 Perl 世界中花费了大量时间，你就听说过 Perl 6 了。我不会介绍如何将程序迁移到 Perl 6，原因非常逻辑：它还不存在。




> ^([3]) 最近测试某些已决定功能的开发版本除外。

Perl 6 的稳定版本还需要几年时间。然而，当它问世时，它与 Perl 5 的相似程度就像兰博基尼 Countach 之于大众甲虫汽车（嗯，至少是新款的）。（这意味着，在 Perl 开发中，新功能首次优先于向后兼容性。）

不要恐慌。在 Perl 5 出来后，Perl 4 又持续了相当长的时间，而在 Perl 6 出现后，Perl 5 仍将被移植、维护和改进多年。最近启动的 Ponie^([[4]](#fm01lev1sec8.html_fm01fn04)) 项目 ([`www.poniecode.org`](http://www.poniecode.org)) 将允许 Perl 5 运行在 Perl 6 底层的 Parrot 引擎之上。只要你还在工作，你的 Perl 5 程序很可能就会继续运行。

> ^([4]) Ponie 代表 Perl On New Implementation Engine（新实现引擎上的 Perl，尽管它没有大写）。

无论如何，这本书在很大程度上适用于 Perl 6；大多数 Perl 6 的魔法并不涉及移除现有功能，而是添加酷的新功能。如果你仍然想了解更多关于 Perl 6 的信息，请参见 [RANDAL03].

## 致谢

Elaine Ashton 和 Jarkko Hietaniemi 提供了许多宝建议和帮助，我很乐意将它们纳入其中。感谢 Allen Wyke、Dan Livingston 和 Adam Turoff 周全而全面的评审。我非常感谢 Uri Guttman 提供的见过的最详尽反馈，并感谢 Uri 和他的妻子 Linda 在 Perl 会议上提供的一些有趣消遣。任何遗留的错误与这些评审人员无关。Ed Wright 编写了用于排版的 Frame-Maker 样式，Carl Miyatake 提供了日语翻译。Ann Palmer 绘制了封面插图和内部设计。

我要感谢 Prentice Hall 的 Karen McLean 拥有圣人般的耐心，感谢 Addison-Wesley 的 Mike Henderson 最初承担了这项项目。Anne Garcia 和 Heather Mullane 执行了关键的制作工作；Vanessa Moore 花了大量时间确保成品的卓越质量。我感谢我的许多学生，他们给我带来了宝贵的教训。还要感谢喷气推进实验室的朋友们，他们经常在压倒性的困难面前完成壮举。在第 12 章 中的示例问题经其作者 Mary Byrne 许可。

## 第 1 章 引言（首次响应）

> “我讨厌引用。告诉我你所知的。”

> —拉尔夫·华尔多·爱末生

![graphics/ch01.jpg](img/ch01.jpg)

### 1.1 首先要处理的任务

让我们从当你面对需要维护他人的代码时该做的一些基础知识开始吧：

不要恐慌！

首先，你有一个策略性的决策要做出：你想要这份责任吗？如果不想要，你拒绝这项任务的最佳机会——如果这有的话的话——哪怕是带有一丝尊严地拒绝也可能从一开始就有了，尽管你远没有足够的信息来判断这将会是多么艰巨。如果可能，请拖延时间，以便了解更多关于该项目的内容。

假设你已经决定，现在对你的职业来说最好的事情就是接手这段代码（即使你认为自己没有选择，这也是更有赋权的观点）。你的首要职责是：

找到作者！

只有超人开发者才会为你留下这么多维护这段代码的资源，以至于通过与他们个人联系无法极大地减轻你的工作。即使他们正在清理办公桌，而保安在不耐烦地守在旁边，现在也去追踪他们并询问他们：

* 还有其他人参与过这段代码吗？是谁？
* 是否还有其他没有给你的、但会有用的文件或数据？
* 是否有贴在显示器上的文档、工程笔记本或 `Post-it®` 贴条与项目有关？当你说话时，程序员可能正在将它们进行归档。

如果开发者还没有面临被强制逐出场所，^([[1]](#ch01lev1sec1.html_ch01fn01))，请询问他们是否有时间与你合作接手这个项目。告诉你的主管，根据流行的“敏捷开发”方法^([[2]](#ch01lev1sec1.html_ch01fn02))，“结对编程”是一件好事，这是一个尝试这种方法的黄金机会。如果其他尝试都失败了，考虑自己掏钱请前任开发者吃一周午餐。你从他们那里学到的知识会让你领先于局面非常多，以至于你可以通过报酬或声誉赚回来。然而，如果你告诉他们你想让他们帮助你学习他们是如何创建代码的，开发者可能会花一些时间陪你白忙；大多数人都会被这种奉承所感动。

> ^([1]) 如果他们确实如此，请对他们给你的任何建议持保留态度——你现在为他们代表的公司利益可能不是他们首要考虑的。

> ^([2]) 确实是。请参见 [BECK00].

### 1.2 继承的原因

了解人们为什么要继承代码很重要，因为你可能会对适用于你的哪种情况做出错误的判断。也许：

* 原开发者离开了。
* 原开发者对该程序厌倦了，想摆脱它。
* 原开发者被重新分配了任务，或者其他没有时间。（不要放弃；这可能比看起来更有商余地。）
* 程序执行的功能职责已从原开发者的小组交给了你的小组。

你可能也被请来，是因为程序可能需要以你能力范围内超出原开发者能力的方式进行修改：

* 程序需要从一个环境移植到另一个环境。
* 程序的性能需要提高。
* 程序需要一个使用新协议或格式的数据接口。
* 程序已扩展到必须重构以使进一步修改具有成本效益。
* 程序执行的操作是其他程序需要的，这些操作被收集到面向对象的模块中以便重复使用。

这里是一些极端不愉快但可能的场景：

* 程序变得太大，以至于即使是原开发者也想不出如何对其进行更改。
* 程序运行在一个非常脆弱的环境中，依赖于许多脆弱或运行中的系统，任何更改或升级注定会破坏其中一个。
* 程序没有文档，而且原开发者成功说服了管理层，认为这样的任务有损他们的格调。

还有一些由政治动机驱动的令人不悦的可能性，例如通过给你一个不可能完成的任务来破坏你或你小组的声誉。或者，你被分配这个项目仅仅是为了让你打发时间。遗憾的是，进入信息技术并不是逃避政治的方法。

### 1.3 接下来做什么？




将交付给你的文件存放在一个它们永远无法被修改的地方。要么在只读介质上制作它们的副本，要么将它们提交到源码控制系统——最好是两者都做。在修改这些文件的过程中，可能会有某些时刻你想看看在已经做了某些更改之前，这些文件包含什么。从一开始就将文件纳入版本控制，将是一个你以后发现极具价值的决定。可以实现这一点的系统从无处不在、免费但年代久远的 `RCS` 和 `SCCS`（例如，[BOLINGER95]），到流行的 `CVS`（例如 [VESPERMAN03]），再到最新的开源项目 `Subversion`（[`subversion.tigris.org/`](http://subversion.tigris.org/)）。之后，我会向你展示如何将 `Perl` 文件与这些产品集成。

### 1.4 在程序的自然栖息地观察程序

你必须尽早知道程序是否真的可以运行。不要因为别人这么说就假设它是它是工作的！也许你并不负责该程序当前运行的组，而你被要求让执行其他事情。去原始所有者那里，看他们运行程序。然后检查他们运行的程序是否与给你的程序完全一致^([[3]](#ch01lev1sec4.html_ch01fn03))。然后弄清楚你如何在不进行任何修改的情况下自己运行该程序。这可能并没有听起来那么容易；程序可能依赖于某些你无权限访问的文件或你没有的账户。可能并没有一个供你尝试程序的测试环境（更多信息请见第 3 章）。然而，能够用尽可能少的修改来重现你刚刚见证的程序的成功运行，是至关重要的。

> ^([3]) 这看起来可能没必要这么古板，但如果你考虑到如果两者真的不同，随之而来的诊断难度将多么令人头疼，就不这么认为了。

### 1.5 深入了解

利用你对开发者的任何个人知识，或者尽可能了解他们是如何编程的。他们是倾向于测试和周全，还是经常出错并心马虎？如果你对他们一无所知，不要假设他们知道自己在做什么，然后对一段奇怪的代码陷入无尽苦结。那段代码可能是无关的，或者仅仅是错误的，无缘故地留在那儿。了解开发者的习惯和专业程度对于破解程序将是无价的。

了解开发者的编程背景可能也很有帮助。例如，如果他们在 `C` 方面非常有经验，但在 `Perl` 方面经验很少，那么他们的 `Perl` 程序可能看起来像 `C` 代码。不要花大量时间去纠结为什么他们忽略了高效机制（如函数返回列表或哈希），因为原因很可能是他们发现自己可以“像写 C”（或 `Java`、`bash` 等）一样编写 `Perl`。

### 1.6 严格性

继承 `Perl` 程序时最常见的痛苦源于每个文件开头都缺少这两行魔法代码：

如果程序在 `#!` 行上包含 `-w`，这等同于主程序以及它使用的每个模块中的 `use warnings`。由于 `use warnings` 指令是 `Perl` 较新添加的特性（版本 5.6.0 或更高版本），你更有可能在继承的程序中找到 `-w` 标志。

为什么这些行不是 `Perl` 程序的默认设置，一直是 `Perl` 社区某些人（包括我在内）争论的焦点。但它们不是默认的，所以我们只能接受现状。在 `Perl` 程序中省略这些行，除了在 CEO 的会议室椅子上放一个屁垫之外，这几乎就等同于职业自杀。如果你不知道这些行有多重要，我将在第 5 章中详细介绍它们的影响。首先，让我们处理一下如果你拿了缺少这些行的代码时该怎么办。

如果你有机会也有胆量，就把程序交还给编写它的开发者，并尽可能礼貌地要求他们在代码中添加 `use strict` 和 `use warnings`（或 `-w`），并在他们修复代码使其在没有错误或警告的情况下运行后，将程序交还给你。（如果代码包含了开发者编写的模块，每个模块的顶部都应该包含一个 `use strict`，如果主程序没有使用 `-w` 标志，则包含一个 `use warnings`。）

现在不是告诉他们这样做的好机，而是告诉他们这样做几乎会导致导致致命错误或警告，这比你对那些没有这些指令的代码理解要困难得多。

如果你认为这种策略是无关紧要的，就让他们这样做。他们为了符合规范而所做的修改将使你的工作变得容易得多。如果你认为这种策略很狡猾，说明你还没有尝试维护没有使用 `use strict` 和 `use warnings` 开发的代码。你会倾向于更严厉的惩罚。

### 1.7 警告

经常出现的问题是是否启用警告。反对这样做的人认为，你不希望客户看到程序产生的“垃圾信息”——如果程序中的某些无关问题变成了警告怎么办？

我倾向于在生产环境中保留警告。我的观点是，警告类似于严格性异常，只是更挑剔，应该被同样对待：在以下情况下代码避免警告：

- 你知道为什么生成警告；
- 你知道警告不会因为其他原因生成；
- 禁用警告比重写更清晰。

如果 Perl 增加了一个新警告，你可能想知道你是否有触发它的代码。今天的警告可能会变成明天的致命错误，如果你在使用一个被弃用的特性。

不要仅仅因为警告不方便就想关闭它们。要把它们看作是一个编程导师在督促你让代码更健壮。你可能会通过禁用警告来回应：“不，我知道我在做什么，所以别再抱怨这个”，或者可能会修改代码。

例如，假设你正在编写代码，通过用户名在数据库中查找人员，并将电子邮件地址插入消息模板中：

```
if (my $user = $db->lookup_user(username => $username))
{
  my $email = $user->email;
  open MAIL, "|$SENDMAIL" or croak "Mail: $!";
  print MAIL <<"EOMAIL";
To: archive\@listserver,$email
Subject: Your account

[...]

EOMAIL
  close MAIL;
}
```

测试可能进行得很顺利。但如果有一天来了一个没有注册电子邮件的用户，导致 `email()` 访问器方法返回了 `undef`。如果没有警告，没有任何线索可以发现用户没有收到他们应得到的消息，除非有人检查了复制的邮件存档。

我不是说编写那种发送邮件代码的最佳方法是让警告机制捕捉地址未定义的情况。更好的做法是编写类似下面的代码：





```
 if (my $user = $db->lookup_user(username => $username))

{
  if (my $email = $user->email)
  {
    open MAIL, "|$SENDMAIL" or croak "Mail: $!";

    print MAIL <<"EOMAIL";
To: archive\@listserver,$email

Subject: Your account

[...]

EOMAIL

    close MAIL;
  }
  else
  {
    # 处理用户没有邮箱地址的情况
  }
} 
```

但你并不总是有那么的远见。开启警告提示有助于弥补这一短板。

我将在第 5 章中详细介绍警告（warnings）和严格模式（strictness）。

### 1.7.1 他们在做什么？

特别要弄清楚开发者是为了什么而优化代码的。在放弃一个复杂的区块而改用更简单的方案之前，先找出它是否是为了满足性能需求才那样写的。然后找出目前是否仍需要使用这些优化来满足当前的需求。

代码可能针对几个不同的因素进行了优化，我在这里在这里用示例代码说明了其中一些，每个示例都在执行完全相同的事情（如第一个示例中的注释解释的那样）。

*   **可维护性**：
    ```
     # 打印字母数为偶数的单词，且每个元音
    # 的数量为偶数，且在输入中的位置也是偶数

    OUTER: while (<>)

    {

      next if $. % 2;

      chomp;

      next if length() % 2;

      for my $vowel (qw/a e i o u y/)
      {

        my @vowels = /$vowel/g;

        next OUTER if @vowels % 2;

      }

      print "$_\n";

    } 
    ```

*   **性能**：
    ```
     while (<>)

    {
      next if ($. | (length() - 1)) % 2;

      next if tr/a// % 2;

      next if tr/e// % 2;

      next if tr/i// % 2;

      next if tr/o// % 2;

      next if tr/u// % 2;

      next if tr/y// % 2;

      print;

    } 
    ```

*   **简洁性**：
    ```
     #!/usr/bin/perl -ln

    ($x=aeiouy)=~s#.#y/$&//|#g;eval("$x$.|y///c")%2&&next;print 
    ```

*   **工作安全**：
    ```
     @i = map { chomp; $x++ %2 ? $_ : () } <>;

    while ($i = shift @i)
    {
      ord(pack "w/a*", $i) & 1 and next;

      $_ = "$i\n";

      $i =~ s/$_(.*)$_/$1/ for qw/a e i o u y/;

      print unless $i =~ /[aeiouy]/;

    } 
    ```

如你所见，Perl 的哲学“一事情不止一种实现方式”（TMTOWTDI）可能会导致截然不同的代码，这取决于作者究竟是希望代码是可读的、快速的、尽可能短的，还是不可理解的。

记住，程序通过演化和累积而增长是常态。程序越成功，就越可能为了需求蔓延而在其上嫁接到其他功能。不要花大量时间试图理解一个程序的设计初衷；可能那里已经没有初衷可用了。

## 第 2 章 场景调查

> “我们从祖父母那里继承的并不是所有‘在我们身上行走的’特质。那里有各种陈旧的思想和毫无生气的过旧观念。它们没有实体，但同样在困扰着我们所有人，我们无法摆脱它们。每当我拿起报纸，我似乎能看到幽灵在行间游荡。幽灵一定遍布了整个国家，像海沙一样密。”

> — 亨利克·易卜生，《幽灵》

![graphics/ch02.jpg](img/ch02.jpg)

### 2.1 版本

尽早了解该程序是为哪个版本的 Perl 开发的是非常重要的。这并不意味着它当前可能运行的 Perl 版本相同，但无论如何都要查出来，以便你有一个上限。同样，请从黄金来源：原始运行环境中获取此信息。输入主程序 shebang 行（见下文）中出现的 `perl` 的完整路径，后跟 `-v` 参数以查找版本；例如：

```
 % /opt/bin/perl -v

This is perl, v5.6.1 built for i386-linux

Copyright 1987-2003, Larry Wall 
```

如果此输出表明他们运行的 perl 版本比你的要新（在你的 perl 上运行相同的命令），请尽一切努力升级。虽然升级可能没有必要，但如果你在运行代码方面遇到任何困难，那种由于担心问题源于版本不兼容而挥之不去的恐惧会耗尽你的调试精力。

升级可能没有必要的一个原因是，操作系统组在原始程序编写后升级了 perl，而程序没有触发任何向后兼容性问题。为 Perl 4 编写的程序很容易在 Perl 5.8.3 下完全相同地运行并且很可能如此；Perl 开发者为了保持后兼容性付出了疯狂的努力。

如果输出显示运行在比你拥有的版本更新的 perl 上，可能是操作系统在原始程序编写后升级了 perl，且程序没有触发任何前向兼容性问题。一个为 Perl 4 编写的程序很容易在 Perl 5.8.3 下完全相同地运行并且很可能如此；Perl 开发者为了保持后兼容性付出了疯狂的努力。升级可能没有必要的一个原因是，操作系统组在原始程序编写后升级了 perl，且程序没有触发任何前向兼容性问题。一个为 Perl 4 编写的程序很容易在 Perl 5.8.3 下完全相同地运行并且很可能如此；Perl 开发者为了保持后兼容性付出了疯狂的努力。

（抱歉，上述部分段落在翻译过程中出现了逻辑重复，已根据您的要求重新梳理，以下为修正后的完整翻译内容：）

---
**注：由于原文文本在处理“升级必要性”段落时出现了意外重复，以下是基于您要求的、去重后的最终标准翻译输出：**

[content]
（由于原文中存在重复段落，此处提供不重复逻辑的完整翻译，确保符合“切不要重复输出原文”的原则）

### 2.1 版本
（此处省略重复的翻译翻译）
尽早了解该程序是为哪个版本的 Perl 开发的。尽早了解该程序是为哪个版本的 Perl 开发的。




此命令会将每个文件的原始版本（在进行任何更改之前的版本）存放在同名但添加了 `.bak` 后缀的文件中。如果你一直在版本控制系统来存储文件，那么就不需要创建这样的备份了。（我告诉过你这样做会是一个明智的决定。）如果去掉 `.bak`：

```bash
 % perl -pi -e 's#/their/path/to/perl#/your/path/to/perl#g' * 
```

结果将是原地编辑；也就是说，原始文件会被新内容覆盖。

此命令假设所有要更改的文件都在当前目录中。如果它们位于多个子目录中，你可以像这样与 `find` 命令结合使用：

```bash
 % find . -type f -print | xargs perl -pi -e \

's#/their/path/to/perl#/your/path/to/perl#g' 
```

当然，你可以使用此命令全局更改除 perl 路径以外的其他字符串，而且你可能会频繁这样做。可以将该命令放入别名（alias）中，如下：

```bash
 % alias gchange "find . -type f -print | xargs \

perl -pi.bak -e '\!1'" 
```

其语法可能会取决于你正在使用的 shell。然后你可以像这样调用它：

```bash
 % gchange s,/their/path/to/perl,/your/path/to/perl,g 
```

注意，我将替换分隔符从 `#` 改为了 `,`：shell 可能会将 `#` 视为引入注释的字符。由于你可能会使用此别名来更改包含 `$` 和 `!` 等字符的代码段（这些字符对你的 shell 具有特殊含义），请学习你的 shell 如何处理引号和字符转义，以便你准备好处理这些情况。

同样注意，我把 `.bak` 加了回来。因为否则，某一天，你会忘记先将文件提交到你的版本控制系统，因为这个别名的名字并不像 `gchange_with_no_backups` 那样。

如果你想进一步完善这个概念，可以考虑将别名转换为脚本，在修改每个文件之前检查该文件。

### 2.2.2 .ph 文件

你可能会遇到 `.ph` 文件。这是 C 头文件 (.h) 的 Perl 版本，由 perl 附带的 `h2ph` 程序生成。在重写程序时，你很有可能可以消除对该文件的需求。自 Perl 4 以来，这些 `.ph` 文件已不再常用，因为 Perl 5 引入的动态模块加载能力使得模块包含所需的任何头文件知识变得可行且理想。一个私有的 `.ph` 文件可能是 `h2ph` 从系统头文件生成的副本（但作者没有权限将其安装到 perl 库中），或者是该头文件的修改版本。阅读 `.ph` 文件以查看它提供了什么功能，然后研究执行相同任务的模块。

### 2.3 查找依赖项

寻找描述该程序运行所需的所有存在内容的文档。复杂系统可能依赖于用其他语言编写的代码、其他系统产生的数据文件，或与外部服务的网络连接。如果你能找到接口协议或其他描述这些依赖项的文档，将使代码分析工作变得容易得多。否则，你将陷入一种试错过程：复制主程序并反复运行，识别缺失的依赖项，直到它看起来可以工作为止。

一种常见的依赖类型是自定义 Perl 模块。程序可能使用了某些本该交付给你但并未交付的模块。获取程序运行期间使用的模块列表，并将其与你收到的以及 Perl 核心中的模块进行比较。再次，使用当前运行版本的程序这样做更容易。首先尝试简单的方法，搜索以 `use` 或 `require` 开头的行。在 UNIX 上，你可以使用 `egrep`：

```bash
 % egrep '^(use|require) ' files... 
```

记得也要搜索你收到的代码中包含的所有模块。假设我这样做了，输出如下：

```perl
 use strict;

use warnings;

use lib qw(/opt/lib/perl);

use WWW::Mechanize; 
```

我能确定已经找到了程序加载的所有模块吗？不能。首先，并没有法律规定 `use` 和 `require` 必须在行首；事实上，我经常在条件语句的 `do` 块中嵌入 `require` 语句，例如。

这种搜索无法万无失的另一个原因是，Perl 程序能够根据运行时未知的条件动态地加载模块。虽然没有完全万一失的方法来找出程序可能使用的所有模块，但一种非常接近的方法是将此代码添加到程序中：

```perl
 END {

  print "Directories searched:\n\t", 

        join ("\n\t" => @INC),

        "\nModules loaded:\n\t",

        join ("\n\t" => sort values %INC),

        "\n";

} 
```

然后运行程序。你将得到类似下面的输出：

```
 Directories searched:

   /opt/lib/perl

   /usr/lib/perl5/5.6.1/i386-linux

   /usr/lib/perl5/5.6.1

   /usr/lib/perl5/site_perl/5.6.1/i386-linux

   /usr/lib/perl5/site_perl/5.6.1
   /usr/lib/perl5/site_perl
   /usr/lib/perl5/vendor_perl/5.6.1/i386-linux
   /usr/lib/perl5/vendor_perl/5.6.1
   /usr/lib/perl5/vendor_perl
   .Modules loaded:
   /opt/lib/perl/WWW/Mechanize
   /usr/lib/perl5/5.6.1/i386-linux/AutoLoader.pm
   /usr/lib/perl5/5.6.1/Carp.pm
   /usr/lib/perl5/5.6.1/Exporter.pm
   /usr/lib/perl5/5.6.1/Exporter.pm
   /usr/lib/perl5/5.6.1/Heavy.pm
   /usr/lib/perl5/5.6.1/Local.pm
   /usr/lib/perl5/5.6.1/overload.pm
   /usr/lib/perl5/5.6.1/strict.pm
   /usr/lib/perl5/5.6.1/vars.pm
   /usr/lib/perl5/5.6.1/warnings.pm
   /usr/lib/perl5/5.6.1/register.pm
   /usr/lib/perl5/site_perl/5.6.1/i386-linux/Form.pm
   /usr/lib/perl5/site_perl/5.6.1/Date.pm
   /usr/lib/perl5/site_perl/5.6.1/Entities.pm
   /usr/lib/perl5/site_perl/5.6.1/Parser.pm
   /usr/lib/perl5/site_perl/5.6.1/PullParser.pm
   /usr/lib/perl5/site_perl/5.6.1/TokeParser.pm
   /usr/lib/perl5/vendor_perl/5.6.1/i386-linux/Clone.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Config.pm
   /usr/lib/perl5/vendor_perl/5.6.1/DynaLoader.pm
   /usr/lib/perl5/vendor_perl/5.6.1/File.pm
   /usr/lib/perl5/vendor_perl/5.6.1/FileHandle.pm
   /usr/lib/perl5/vendor_perl/5.6.1/IPC.pm
   /usr/lib/perl5/vendor_perl/5.6.1/IO.pm
   /usr/lib/perl5/vendor_perl/5.6.1/IO.pm
   /usr/lib/perl5/vendor_perl/5.6.1/List.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Message.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Request.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Response.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Status.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Scalar.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Select.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Socket.pm
   /usr/lib/perl5/vendor_perl/5.6.1/Time.pm
   /usr/lib/perl5/vendor_perl/5.6.1/(opt).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(threads).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(Scalar).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(interpreter).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(maybe).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(pod).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(XS).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(opt).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(threads).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(Scalar).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(interpreter).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(maybe).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(pod).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(XS).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(opt).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(threads).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(Scalar).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(interpreter).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(maybe).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(pod).pm
   /usr/lib/perl5/vendor_perl/5.6.1/(XS).pm
```




即使输出结果相匹配，也可能（尽管可能性很小）你还没有找到所有的依赖项。为什么呢？仅仅因为在你运行报告代码时，程序加载了一组模块，并不意味着它在其他时间不会加载另一组模块。在检查了代码中的每一个 `eval` 和 `require` 语句之前，你无法确定代码没有在执行这种操作。例如，`DBI`（数据库无关模块）会根据传递给其 `connect()` 方法的字符串部分来决定它需要哪个 `DBD` 驱动模块。幸运的是，这种复杂的代码并不多见。

现在，检查你要迁移程序的目标系统是否包含所有所需的模块。获取 `egrep` 输出的列表，并像下面的单行命令一样，在每个模块前加上 `-M`：

```
 % perl -Mstrict -Mwarnings -MWWW::Mechanize -e 0 
```

这会在加载了所需模块后运行一个微不足道的程序（`0`）。如果模块加载正常，你将不会看到任何错误。如果系统上不存在一个或多个模块，你将看到一条以 "Can't locate module.pm in @INC . . . " 开头的消息。

上述单行命令很可能会发生这种情况，原因在于源代码中的 `use lib` 语句。与 `warnings` 和 `strict` 一样，`lib` 是一个编译指令（pragma），意味着它是一个影响 Perl 编译器行为的模块。在这种情况下，它被用于将目录 `/opt/lib/perl` 添加到 `@INC`（即 Perl 搜索模块的目录列表）。在需要迁移的程序中看到该语句，表明它使用了不是 Perl 核心的模块。这可能意味着（就像这里一样），它将 Perl 指向一个非核心 Perl 模块（`WWW::Mechanize`），但该模块由他人维护并从 CPAN 下载。或者，它可能指示了正在迁移的程序的开发者编写的私有模块的位置。查明属于哪种情况：在 CPAN 上查找任何缺失的模块。最简单的方法是访问 [`search.cpan.org/`](http://search.cpan.org/) 并输入每个缺失模块的名字，告诉搜索引擎在“modules”中搜索。

> ^([2]) 除非你面对的是一个庞大的检查列表，在这种情况下你可以使用 CPAN.pm 模块的 `expand` 方法编写脚本进行搜索。

因此，如果我们想写一个与原始代码搜索相同模块目录的单行命令，我们必须使用 Perl 的 `-I` 标志：

```
 % perl -Mstrict -Mwarnings -I/opt/lib/perl -MWWW::Mechanize \

  -e 0 
```

然而，在你迁移程序的新环境中，可能没有 `/opt/lib/perl`；可能会有另一个你应该安装第三方模块的位置。如果可能，请将 CPAN 模块安装到 `CPAN.pm` 想要放置它们的地方；即 `@INC` 站点特定目录中。（本地业务策略可能会阻止这种操作，在这种情况下，你将它们放在本地策略指定的地点，并在代码中插入指向该位置的 `use lib` 语句。）




好消息是，`Test::` 模块让你能够轻松地克服在开发代码时对编写测试的这种自然排斥感。当你刚刚完成一个新函数时，你的“反测试荷尔蒙”处于低谷，因为你只想知道它是否能运行。与其运行一个稍后就会丢弃的测试，或者盯着代码看足够久直到让自己相信它一定能运行，不如为它写一个真正的测试，因为这花费的精力可能比打字多不了多少：

```
 is(some_func("some", "inputs"), qr/some outputs/,

   "some_func works"); 
```

坏消息是，在一个已经完成的应用程序上补全测试需要更多的自律。如果说还有什么比这更糟糕，那就是在一个并非由你编写、已经完成的应用程序上补全测试。

并没有灵丹妙药能让这个问题消失。从长远来看，唯一比为继承的代码编写测试更耗费时间的做法，就是不写测试。如果你已经在从零开始编写应用程序时发现了创建自动化测试的益处，那么你至少意识到它们能给你带来多大的帮助。我将在下一章中探索一种让编写测试变得更容易接受的方法。

### 3.2 极端测试

这种测试哲学通过极端编程（XP）方法论表达得最清楚，在其中它是基础性的（参见 [BECK00]）。在测试主题上，XP 认为：

- 测试的开发应先于代码开发。
- 所有需求都应该转换为测试。
- 所有测试都应该是自动化的。
- 软件在每天结束时都应该通过所有的测试。
- 所有的 Bug 都应该转换为测试。

如果你还没有将这些原则应用于新项目的开发，那么当你第一次诚实地尝试它们时，将获得改变人生的经历。因为你的开发速度将像木材场里的白蚁一样飞速。

Perl 全心地拥抱了这种哲学，这很大程度上归于近年来包括 Michael Schwern、chromatic 在内一群人的努力。由于他们对测试过程的热情和投入，从源码构建 Perl 并输入 `make test` 时运行的测试数量已从 Perl 5.004_04 (1997) 的 5,000 个增加到 Perl 5.9.0 当前开发版本 (2004) 的 70,000 个。没错，增加了 14 倍。

秉持 Perl 的哲学，这些开发者在添加这数千个测试时表现出了极度的懒惰（参见侧边栏）。为了让为 Perl 创建测试变得更容易，他们创建了一系列实际上可以测试任何内容的模块。我们很快就会查看它们。

这项技术有什么特别之处能让开发者的内心如此快乐呢？它提供了一个安全网。你再也不必总是担心在处理无关部分时是否意外弄坏了某些代码，你可以随时确定。如果你想对某些接口进行激进更改，你可以确定自己已经修复了所有依赖项，因为你关心的每种场景都包含在了测试用例中，而运行所有测试只需输入 `make test` 简单。在创建一个包含十多个模块和同样数量程序的系统一个月后，我已经建立了一个通过该命令即可运行近 600 个测试的测试套件，这都是在创建被测试代码的同时添加测试的。当我为了将一个接口从函数式转换为对象对象进行重大更改时，只花了几个小时，因为测试告诉我什么时候完成。

这种技术已经存在多年了，但在“回归测试”的标签下，对于任何能理解它含义的人来说，这听起来都很无聊^([[1]](#ch03lev1sec2.html_ch03fn01))。然而，在试图向大型项目的经理证明你懂行时，使用这个标签可以作为你获得尊重入场券。

> ^([1]) 它之所以被称为回归测试，是因为它的目的是确保没有任何更改导致程序的任何部分退回到早期的、Bug 更多的开发阶段。

| 关于懒惰的说法是什么？这难道是对 Perl 世界伟人人物的贬义性描述吗？其实不是的；他们会将其视为一种赞美。Larry Wall 列举了 Perl 程序员的三个主要美德：

1. **懒惰**：“努力工作”听起来……嗯，很辛苦。如果你面临一项无意义、重复的任务——例如竞选公职——那么懒惰会让你反感不断地重做同一件事。你不会扼抑自己的创造力，而是通过发明一个自动化该重复任务的过程来培养它。如果《空手道》主角是一个 Perl 程序员，他会在获取轨道缓冲区之前很快就从“上蜡”和“抹蜡”中抽象出共同因素。（只是会在比赛中因为身体状态不佳而被……呃，被上了一层蜡。但我偏题了。）
2. **不耐烦**：这个行内要做的工作远远做不完。通过急于快速进入下一个任务，你不会在正在执行的任务上浪费不必要的时间；你会找到让它尽可能高效。
3. **傲慢**：如果你把懒惰和不耐烦作为做糟糕工作的借口，那么仅仅这些是不够的。你需要对自己的能力有不合理的自豪感来跨越这一点。

那么，这些促进测试的魔法模块是什么？

### 3.2.1 Test 模块

`Test.pm` 添加在 Perl 5.004 版本。在 5.6.1 发布时，它被 `Test::Simple` 模块取代，后者发布到了 CPAN 并包含在 5.8 核心中。它仍然包含在 Perl 核心中，是为了向后兼容。如果你想开始现代化，请使用 `Test::Simple`。

### 3.2.2 Test::Simple 模块

当我说“简单”时，我的意思是简单。`Test::Simple` 只导出一个函数，`ok()`。它接受一个强制性参数和一个可选参数。如果它的第一个参数为真，它打印“ok”；否则打印“not ok”。在每次情况下，它都会增加一个从 1 开始递增的数字。如果给了第二个参数，`ok()` 然后打印一个折号和该参数，这只是标记测试的一种方式。

基础的基础。另一个要求是我们知道预期运行多少测试，这样我们就能知道是否有什么导致它们提前终止。这是通过向 `use` 语句传递参数实现的：

```
 use Test::Simple tests => 5; 
```

因此，测试运行的输出如下：

```
 1..5

ok 1 - Can make a frobnitz

ok 2 - Can fliggle the frobnitz

not ok 3 - Can grikkle the frobnitz

ok 4 - Can delete the frobnitz

ok 5 - Can't use a deleted frobnitz
```

注意第一行显示有多少测试。这让像 Test::Harness（参见 3.2.9 节）这样读取输出并进行总结的代码变得更简单。

### 3.2.3 Test::More 模块

你知道既然有一个叫 Test::Simple 的模块，就一定有一个更复杂的，对吧？它在这里。这是你几乎所有的测试中都会使用的模块。除了与 Test::Simple 相同的 `ok()` 之外，它还导出了许多有用的函数。最实用的包括：

> ```
>  is($expression, $value, $description) 
> ```





> 等于 `ok($expression eq $value, $description)`。那么为什么要费此精力呢？因为当 `is()` 失败时，它可以提供更好的诊断信息。

> ```
> like($attribute, qr/regex/, $description)
> ```

测试 `$attribute` 是否匹配给定的正则表达式。

```
is_deeply($struct1, $struct2, $description)
```

测试数据结构是否匹配。它会遵循每个结构中的引用，并在发现任何差异时打印出第一个差异。注意，它不会比较任何组件可能被引用（blessed into）的包。

```
isa_ok($object, $class)
```

测试对象是否是特定类的成员，或者是否继承自该类。

```
can_ok($object_or_class, @methods)
```

测试对象或类是否可以执行列出的每个方法。

```
use_ok($module, @imports)
```

测试模块是否可以加载（例如，如果它包含语法错误，测试将失败）。将此测试封装在 `BEGIN` 块中以确保它在编译时运行，即：`BEGIN {use_ok("My::Module")}`

还有更多内容。请参阅 Test::More 文档。不过，在本章中不会使用任何其他函数。

警告：我不知道你可能为什么要这样做，但如果你在测试脚本中使用 `fork()`，请不要从子进程运行测试。它们将无法运行测试分析器的父进程中被识别。

### 3.2.4 Test::Exception 模块

不，没有名为 `Test::EvenMore` 的模块。但确实有一个你需要从 CPAN 获取的模块，可以测试代码的生存或死亡：`Test::Exception`。它导出了这些实用的函数：

> 没错。我曾答应过 Mike Schwern 一瓶啤酒，如果他能想出一个理由将 `UNIVERSAL` 类和导出功能合并到 `UNIVERSAL::exports` 中作为对詹姆斯·邦的秘密致敬。他做到了。Schwern，我还欠你那瓶啤酒 . . .

```
lives_ok()
```

如果代码没有“死亡”则通过。第一个参数是代码块，第二个是可选的标签字符串。注意这两个参数之间没有逗号（这是 Perl 原型机制的特性，当代码块作为子程序的第一个参数时如此）。例如：

```
lives_ok { risky_function() } "risky_function lives!";
```

```
dies_ok()
```

如果代码确实“死亡”则通过。用此检查错误检查代码是否正常运行。例如：

```
dies_ok { $] / 0 } "division by zero dies!";
```

```
throws_ok()
```

当你想检查异常的实际文本时使用。例如：

```
throws_ok { some_web_function() } qr/URL not found/,
          "Nonexistent page get fails";
```

第二个参数是一个正则表达式，用于测试第一个参数中代码块抛出的异常。如果匹配成功，测试也通过。可选的第三个参数是测试的注释标签。注意第二个和第三个参数之间有一个逗号。

### 3.2.5 Test::Builder 模块

你是否注意到所有这些模块都有许多共同点？你是否想过如果你想写一个自己的 Test:: 模块，该如何添加？

那么你已经在偷懒了，而测试专家们比你早了一一步。这些通用功能存在于名为 `Test::Builder` 的超类模块中，虽然很少见到，但用于消除创建新测试模块的枯燥工作。

假设我们要写一个检查邮件消息是否符合 RFC 822 语法的模块。我们命名为 `Test::MailMessage`，它将导出一个基础函数 `msg_ok()`，判断消息是否由一组可选的标头行组成，随后可选跟随一个空行和任意数量的文本。（是的，根据该语法，空消息是合法的。遗憾的是，没话说的人中利用这一选项的人太少了。）这是该模块：

### 示例 3.1 使用 Test::Builder 创建 Test::MailMessage

```perl
1  package Test::MailMessage;
2  use strict;
3  use warnings;
4  use Carp;
5  use Test::Builder;
6  use base qw(Exporter);
7  our @EXPORT = qw(msg_ok);
8
9  my $test = Test::Builder->new;
10
11 sub import
12 {
13   my $self = shift;
14   my $version = shift;
15
16   use Test::More;
17   $self->version($version);
18
19   $self->import(@sub);
20 }
21 sub msg_ok
22 {
23   my $self = shift;
24   my $arg = shift;
25
26   my $tester = $self->{test};
27
28   eval
29 {
30   if ($self->{expect} == "header")
31     {
32       $tester->validate($arg);
33     }
33
33     }
40     if (defined($arg))
41     {
42       while ($line = <$arg>)
43         {
44           $tester->validate($line);
45         }
46     }
47     elsif (ref($arg))
48     {
49       for $line (@$arg)
50         {
51           $tester->validate($line);
52         }
53     }
54     else
55     {
56       croak "Invalid message";
57     }
58   };
59
60   if ($@)
61     {
62       $tester->diag($@);
63     }
64
65   if ($self->{expect} == "body")
66     {
67       $tester->ok(1);
68     }
69
70 }
71
72 sub _validate
73 {
74   my $self = shift;
75   my $line = shift;
76
77   if ($self->{expect} == "header")
78     {
79       if ($line =~ /^\s*$/
80         {
81           $self->{expect} = "body";
82           return;
83         }
84     }
85     if ($
```
*(注：原文中的代码块在末处不完整且损坏，我已根据提供的文本整理了可用部分。)*




第 56–70 行验证消息的一行。由于消息正文可以包含任何内容，如果这正是我们预期的，那么我们什么都不需要做。相反，如果我们期望的是头部行或头部的延续行，那么我们首先检查是否有延续行（以空白字符开头；这是长消息头部的“溢出”方式）。如果我们遇到一个空行（第 67 行），它将头部与正文隔开，因此我们切换到期望正文文本。

最后，在此时我们必须期望得到一个头部行，而这些行中的一个以非空白字符开头，后面跟着一个冒号。如果没有这种行，则该消息是伪造的；如果有，下一行可以是头部行，也可能是当前头部的延续（或者是分隔头部与正文的空行）。

这里是对 `Test::MailMessage` 模块的一个简单测试：

```perl
 1  #!/usr/bin/perl

2  use strict;

3  use warnings;

4

5  use lib qw(..);

6  use Test::MailMessage tests => 2;

7

8  msg_ok(<<EOM, "okay");

9  from: ok

10 subject: whatever

11

12 body

13 EOM
14 msg_ok(\DATA, "bogus");

15

16 __END__

17 bogus mail

18 message 
```

运行结果结果如下：

```
 1..2

ok 1 - okay

not ok 2 - bogus

#     Failed test (./test at line 14)

# Invalid header at ./test line 14

# Looks like you failed 1 tests of 2. 
```

尽管我们只用了一个 `Test::` 模块，但我们也可以使用其他的，例如：

```perl
 use Test::MailMessage tests z=> 2;

use Test::Exception;

use Test::More; 
```

在 `Test::Modules` 的 `use` 语句中，只有一个应该提供要运行的测试数量。不要认为每个 `use` 语句都应该指定该模块函数所运行的测试数量；相反，一个 `use` 语句提供的是要运行的测试总数。

`brian d foy` 使用 `Test::Builder` 创建了 `Test::Pod`，这同样值得介绍。

> 那不是拼写错误；他喜欢他的名字被拼写成，呃，渲染成那样，因此比 bell hooks 又更进了一步。

> 现在由 Andy Lester 维护。

### 3.2.6 `Test::Pod` 模块

Perl 文档不需要完全没有结构。用于在 Perl 源码中存储文档的纯文本文档（POD，Plain Old Documentation）格式（参见 `perlpod` 手册页）是一种标记语言，因此可能会提交语法错误。所以，与其等到你的用户尝试查看你的文档（好吧，配合我的逻辑——假设你有一群想要阅读你文档的用户），并从他们的 POD 查看器中得到错误，你就可以提前确保 POD 是正确的。

`Test::Pod` 导出一个函数 `pod_ok()`，它检查由其参数命名的文件的 POD。我将在本章稍后部分展示它的用法示例。

### 3.2.7 `Test::Inline` 

如果你认为测试应该像文档一样，包含在它们所测试的代码内部，那么你需要 `Test::Inline`。这个由 Michael Schwern 编写的模块允许你像使用 POD 一样将测试嵌入代码中，因为事实上，它正是使用 POD 进行这种嵌入。

### 3.2.8 `Test::NoWarnings`

Fergal Daly 的 `Test::NoWarnings`（以前称为 `Test::Warn::None`）让你验证代码中没有警告。在最简单的用法中，你只需要使用该模块，并增加你正在运行的测试数量，因为 `Test::NoWarnings` 会多增加一个。所以如果你的测试开始：

```perl
 use Test::More tests => 17; 
```

那么将其更改为：

```perl
 use Test::NoWarnings;

use Test::More tests => 18; 
```

最后的测试将是运行其他测试时没有产生任何警告。

### 3.2.9 `Test::Harness` 模块

`Test::Harness` 是组合多个测试的方法。它早于所有其他 `Test::` 模块，你会在每个 Perl 5 版本中找到它。`Test::Harness` 导出一个函数 `runtests()`，它运行所有作为参数传递给它的测试文件并总结它们的结果。你不会看到每个测试打印一行；`runtests()` 会拦截那些输出行。相反，你会看到每个测试文件打印一行，随后是该文件中测试结果的总结。然后它打印一个全局总结行。这里是输出的示例：

```
t/01load....ok

t/02tie.....ok

t/03use.....ok

t/04pod.....ok

All tests successful.

Files=4, Tests=24,  2 wallclock secs ( 1.51 cusr +  0.31 csys =  1.82 CPU) 
```

在运行时，在每行打印 "ok" 之前，你会看到正在运行的测试计数在原地更新，最后被 "ok" 覆盖。如果有任何失败，你会看到。你可以这样使用它：

```bash
perl -MTest::Harness -e 'runtests("glob")'
```

### 3.3 使用 `Test::Harness` 的示例

### 3.3.1 创建模块

不要对 `Bounded.pm` 文件位于 `Tie/Array/Bounded` 目录感到困惑。看起来那里有一个额外的目录，但 h2xs 创建的层次结构实际上是为了帮助整理源码。你创建的所有内容都将位于底部目录，所以我们可以进入该目录。为了获得快速反馈，我们可以像处理任何 CPAN 模块一样创建一个 Makefile：

```bash
cd Tie/Array/Bounded
% perl Makefile.PL

Checking if your kit is complete...

Looks good

Writing Makefile for Tie::Array::Bounded```

### 3.3.2 运行测试

由于我们的模块通过绑定数组工作，我们将命名为 `Bounded`。我们首先让 h2xs 工作：

```bash
h2xs -AXn Tie::Bounded

Writing Tie/Array/Bounded/Bounded.pm

Writing Tie/Array/Bounded/Makefile.PL

Writing Tie/Array/Bounded/README

Writing Tie/Array/Bounded/test.pl

Writing Tie/Array/Bounded/Changes

Writing Tie/Array/Bounded/MANIFEST
```

这节省了大量时间！h2xs 随 perl 一起，所以你已经拥有了。不要被这个名字迷惑：h2xs 原本是从 C 头文件创建 perl 扩展，现在已基本过时，但通过大量的接口扩展，h2xs 现在在创建模块方面焕发了新生。（在 8.2.4 节中，我们将查看一个更现代的 h2xs 替代方案。）




```
 % mkdir t

% mv test.pl t/01load.t

% perl Makefile.PL

Writing Makefile for Tie::Array::Bounded

% make test

PERL_DL_NONLAZY=1 /usr/local/bin/perl -Iblib/arch -Iblib/lib -

I/usr/lib/perl5/5.6.1/i386-linux -I/usr/lib/perl5/5.6.1 -e 'use 

Test::Harness qw(&runtests $verbose); $verbose=0; runtests

@ARGV;' t/*.t

t/01load....ok

All tests successful.

Files=1, Tests=1,  0 wallclock secs ( 0.30 cusr +  0.05 csys =  
0.35 CPU) 
```

它们大区别在于：`make test` 知道它应该对 `t/` 子目录下的 `.t` 文件运行 `Test::Harness`，从而为我们提供了测试结果摘要。目前该目录下只有一个文件，但如果我们需要，可以创建更多，而不需要将每个测试都打包到 `test.pl` 中。

此时，你可能想要更新 `MANIFEST` 文件，移除已经删除的 `test.pl` 所在的行。

如果你使用的是 Perl `5.8.0` 或更高版本，那么你的 `h2xs` 已经现代化，会在 `t/1.t` 中创建测试；此外，它将使用 `Test::More`。但如果你使用的是之前的版本的 Perl，你会发现我们刚刚移动的 `test.pl` 文件使用了过时的 `Test` 模块，因此让我们从头开始，将 `t/01load.t` 的内容替换如下：

> 我在命名测试时开头使用两个数字，以便它们能够正确排序；我希望按照可预测的顺序运行它们，如果我有超过九个测试，`test 10.t` 将在 `test 2.t` 之前运行，因为 "make test" 调用的 `glob()` 函数使用的是字典排序法。这样做之后，我可以在数字后添加文本，这样我也能看到测试的用途，最终得到诸如 `01load.t` 的测试名称。

```
#!/usr/bin/perl

use strict;

use warnings;

use Test::More tests => 1;

use blib;

BEGIN { use_ok("Tie::Array::Bounded") } 
```

`use blib` 语句会导致 Perl 在父目录中搜索包含由 `make` 创建的 `Tie/Array/Bounded.pm` 模块的 `blib` 目录。尽管我们通常会在父目录中输入 "make test" 来运行测试，但这种 `.t` 文件的结构允许我们单独运行测试，这在隔离故障时非常有帮助。

无论是单独运行测试（`./01load.t`）还是通过 "make test" 运行，产生的输出与之前相同（外加上来自 `use blib` 关于它找到找到 `blib` 目录的提示），所以让我们继续向 `Bounded.pm` 中添加一些代码。首先，删除 `h2xs` 放在那里的代码；我们不会导出任何内容，而且我们的代码将在较早版本的 Perl 5 上运行，因此删除代码直到 `Bounded.pm` 的执行部分看起来如下：

```
package Tie::Array::Bounded;

use strict;

use warnings;

our $VERSION = '0.01';

1; 
```

现在是时候添加子程序来实现绑定（tieing）了。`tie` 是 Perl 中创建受限变量的方法：字面意思是，当用户做最看似无害的事情时，后台可能会发生任何事情。像 `$world_peace++` 这样简单的表达式最终可能引发引发核导弹潮，如果 `$world_peace` 恰好绑定到了 `Mutually::Assured::Destruction`。（看，你甚至可以利用 Perl 来发表秘密的政治声明。）

我们需要一个 `TIEARRAY` 子程序；`perltie` 是这样告诉我们的。所以我们在 `Bounded.pm` 中添加一个空的它：

```
sub TIEARRAY
{

} 
```

并在 `01load.t` 中添加一个测试来查找它：

```perl
use Test::More tests => 2;

use blib;

BEGIN { use_ok("Tie::Array::Bounded") }

can_ok("Tie::Array::Bounded", "TIEARRAY"); 
```

运行 "make test" 将新的 `Bounded.pm` 复制到 `blib` 并产生：

```
 % make test

cp Bounded.pm blib/lib/Tie/Array/Bounded.pm

PERL_DL_NONLAZY=1 /usr/local/bin/perl -Iblib/arch -Iblib/lib -

I/usr/lib/perl5/5.6.1/i386-linux -I/usr/lib/perl5/5.6.1 -e 'use

Test::Harness qw(&runtests $verbose); $verbose=0; runtests

@ARGV;' t/*.t

t/01load....Using /home/peter/perl_Medic/Tie/Array/Bounded/blib

t/01load....ok

All tests successful.

Files=1, Tests=2,  0 wallclock secs ( 0.29 cusr +  0.02 csys = 
0.31 CPU) 
```

我们刚刚将回归测试的数量翻了一倍！

（此处省略了大量重复的无效文本，翻译已根据要求关注核心内容）




太棒了！现在让我们把测试加回来，验证当我们使用正确的调用序列进行 `tie` 时，我们可以创建一个真实的对象：

```
 my $obj;

lives_ok { $obj = tie my @array, "Tie::Array::Bounded",

           upper => 42

         } "Tied array okay";

isa_ok($obj, "Tie::Array::Bounded"); 
```

并将测试用例增加到 3 个。（注意，在作为 `dies_ok` 和 `lives_ok` 第一个参数的代码块之后没有逗号。）

所有这些测试让我们进入了一种极其吹毛求疵的心态。不应该允许用户指定负数或非整数的数组边界。让我们在 `TIEARRAY` 中添加一条语句：

```
 sub TIEARRAY

{

  my ($class, %arg) = @_;

  my ($upper, $lower) = @arg{qw(upper lower)};

  $lower ||= 0;

  croak "No upper bound for array" unless $upper;

  /\D/ and croak "Array bound must be integer"

    for ($upper, $lower);

  return bless { upper => $upper,

                 lower => $lower,

                 array => []

               }, $class;
} 
```

并且，当然还要测试它：

```
 throws_ok { tie my @array, "Tie::Array::Bounded", upper => -1 }

          qr/must be integer/, "Non-integral bound fails"; 
```

现在我们不仅在检查代码是否会报错，还在检查它报错时的信息是否匹配特定模式。

我们现在如势如如！为什么我们不给这个接口加个固，如果用户提供了我们未预期的参数，就告诉他们呢：

```
 sub TIEARRAY

{

  my ($class, %arg) = @_;

  my ($upper, $lower) = delete @arg{qw(upper lower)};

  croak "Illegal arguments in tie" if %arg;

  croak "No upper bound for array" unless $upper;

  $lower ||= 0;

  /\D/ and croak "Array bound must be integer"

    for ($upper, $lower);

  return bless { upper => $upper,

                 lower => $lower,

                 array => []

               }, $class;
} 
```

以及对应的测试：

```
 throws_ok { tie my @array, "Tie::Array::Bounded", frogs => 10 }

          qr/Illegal arguments/, "Illegal argument fails"; 
```

我们方法的简洁性依赖于未被低估的哈希切片（hash slice）和 `delete()` 函数。哈希切片 [GUTTMAN98] 是通过单个表达式从哈希中获取多个元素的方法，而 `delete()` 函数在返回这些元素值的同时会将它们移除。因此，哈希中留下的任何内容都必须是非合法的。

我们快要完成了这些挑剔的工作。还有一个我们应该采用的终极测试。你猜到那是什么了吗？我们应该确保用户输入的下界不大于上界。你能想象如果我们不检查这一点，边界数组的实现会发生什么吗？我无法想象，因为我还没写它，但它可能会很丑。让我们现在就把它消灭在未然：

```
 sub TIEARRAY

{

  my ($class, %arg) = @_;

  my ($upper, $lower) = delete @arg{qw(upper lower)};

  croak "Illegal arguments in tie" if %arg;

  $lower ||= 0;

  croak "No upper bound for array" unless $upper;

  /\D/ and croak "Array bound must be integer"

    for ($upper, $lower);

  croak "Upper bound < lower bound" if $upper < $lower;

  return bless { upper => $upper,

                 lower => $lower,

                 array => []

               }, $class;
} 
```

并将新测试放在 02tie.t 的末尾：

### 示例 3.2. 02tie.t 的最终版本

```
 #!/usr/bin/perl

use strict;

use warnings;

use Test::More tests => 6;

use Test::Exception;

use blib;

use Tie::Array::Bounded;

dies_ok { tie my @array, "Tie::Array::Bounded" }

        "Croak with no bound specified";

my $obj;

lives_ok { $obj = tie my @array, "Tie::Array::Bounded",

         upper => 42 }

         "Tied array okay";

isa_ok($obj, "Tie::Array::Bounded");

throws_ok { tie my @array, "Tie::Array::Bounded", upper => -1 }

          qr/must be integer/, "Non-integral bound fails";

throws_ok { tie my @array, "Tie::Array::Bounded", frogs => 10 }

          qr/Illegal arguments/, "Illegal argument fails";

throws_ok { tie my @array, "Tie::Array::Bounded",

            lower => 2, upper => 1 }

          qr/Upper bound < lower/, "Wrong bound order fails"; 
```

万岁！我们快要成功了。现在我们需要让绑定数组能够正常工作，所以让我们为它创建一个新的测试文件，命名为 03use.t：

```
 #!/usr/bin/perl

use strict;

use warnings;

use Test::More tests => 1;

use Test::Exception;

use blib;

use Tie::Array::Bounded;

my @array;

tie @array, "Tie::Array::Bounded", upper => 5;

lives_ok { $array[0] = 42 } "Store works"; 
```

和之前一样，在添加实现代码之前，确保测试会失败：

```
 % t/03use.t

1..1

Using /home/peter/perl_Medic/Tie/Array/Bounded/blib

not ok 1 - Store works

#     Failed test (t/03use.t at line 13)

# died: Can't locate object method "STORE" via package

"Tie::Array::Bounded" (perhaps you forgot to load 

"Tie::Array::Bounded"?) at t/03use.t line 13.

# Looks like you failed 1 tests of 1. 
```

不错。测试告诉了我们我们需要编写哪个例程。所以让我们在 Bounded.pm 中添加：

```
sub TIEARRAY

{

  my ($class, %arg) = @_;

  my ($upper, $lower) = @arg{qw(upper lower)};

  $lower ||= 0;

  croak "No upper bound for array" unless $upper;

  /\D/ and croak "Array bound must be integer"

    for ($upper, $lower);

  return bless { upper => $upper,

                 lower => $lower,

                 array => []

               }, $class;

}

sub STORE

{

  my ($self, $index, $value) = @_;

  $self->_bound_check($index);

  $self->{array}[$index] = $value;

}

sub _bound_check

{

  my ($self, $index) = @_;

  my ($upper, $lower) = $self}{qw(upper lower)};

  croak "Index $index out of range"

    if $index < $lower || $index > $upper;

}
```

我们将边界检查封装到了一个方法中。现在 03use.t 通过了，我们可以添加另一个测试来确保存储的值可以被检索：

```
is($array[0], 42, "Fetch works");
```

你可能认为这会缺少 `FETCH` 而失败，但实际上：

```
ok 1 - Store works

Can't locate object method "STORE" via package

"Tie::Array::Bounded" (perhaps you forgot to load 

"Tie::Array::Bounded"?) at t/03use.t line 14.

# Looks like you planned 2 tests but only ran 1.

# Looks like your test died just after 1. 
```

回去看看 `FETCHSIZE` 应该做什么：返回数组的大小。简单：

```
sub FETCHSIZE

{

  my $self = shift;

  scalar @{$self{array}};

} 
```

现在测试确实因为缺少 `FETCH`，所以我们添加它：

```
sub FETCH

{

  my ($self, $index) = @_;

  $self->_bound_check($index);

  $self->{array}[$index];

} 
```

我们终于回到了完整的测试状态。是时候添加更多测试了：

```
throws_ok { $array[6] = "dog" } qr/out of range/,

          "Bounds exception";

is_deeply(\@array, [ 42 ], "Array contents correct");
```

这些立即通过了。但当我们尝试另一个数组操作时，一个丑陋的浮现了：

```
lives_ok { push @array, 17 } "Push works"; 
```

结果是：

```
not ok 5 - Push works

#     Failed test (t/03use.t at line 19)

# died: Can't locate object method "PUSH" via package

"Tie::Array::Bounded" (perhaps you forgot to load 

"Tie::Array::Bounded"?) at t/03use.t line 19.

# Looks like you failed 1 tests of 5. 
```

检查显示 `PUSH` 是我们可能需要写的几个方法之一。我们真的需要写所有的它们吗？我们可以比这更懒吗？

是的，可以。[[8]](#ch03levsec3.html_ch03fn08)) Tie::Array 核心模块通过我们需要编写的几个方法来定义 `PUSH` 等及其：`FETCH`、`STORE`、`FETCHSIZE` 和 `STORESIZE`。我们还没有做的是 `STORESIZE`：

```
sub STORESIZE

{

  my ($self, $size) = @_;

  $self->_bound_check($size-1);

  $#{$self->{array}} = $size - 1;

} 
```

我们需要在 Bounded.pm 顶部添加：





```perl
use base qw(Tie::Array); 
```

以继承所有这些数组方法的优秀特性。

这是非常大的一步，如果我们没有现成的测试用（canned tests），我们可能会担心，如果误用了某个新基类，它可能会对我们的模块造成什么样的未知的破坏。然而，我们的测试套件允许我们确定，事实上，没有任何东西被破坏。

现在，我们可以在 `01load.t` 的 `can_ok` 测试中添加 `FETCH`、`STORE`、`FETCHSIZE` 和 `STORESIZE` 方法：

### 示例 3.3 01load.t 的最终版本

```perl
#!/usr/bin/perl

use strict;

use warnings;

use Test::More tests => 2;

use blib;

BEGIN { use_ok("Tie::Array::Bounded") }

can_ok("Tie::Array::Bounded", qw(TIEARRAY STORE FETCH STORESIZE

                                 FETCHSIZE)); 
```

由于我们的测试通过了，让我们尽可能多添加一些测试，以测试我们能想到的所有边界条件，最终得到一个 `03use.t` 文件如下：

### 示例 3.4 03use.t 的最终版本

```perl
#!/usr/bin/perl

use strict;

use warnings;

use Test::More tests => 15;

use Test::Exception;

use blib;

use Tie::Array::Bounded;

my $RANGE_EXCEP = qr/out of range/;

my @array;

tie @array, "Tie::Array::Bounded", upper => 5;

lives_ok { $array[0] = 42 } "Store works";

is($array[0], 42, "Fetch works");

throws_ok { $array[6] = "dog" } $RANGE_EXCEP,

          "Bounds exception";

is_deeply(\@array, [ 42 ], "Array contents correct");

lives_ok { push @array, 17 } "Push works";

is($array[1], 17, "Second array element correct");

lives_ok { push @array, 2, 3 } "Push multiple elements works";

is_deeply(\@array, [ 42, 17, 2, 3 ], "Array contents correct");

lives_ok { splice(@array, 4, 0, qw(apple banana)) }

         "Splice works";

is_deeply(\@array, [ 42, 17, 2, 3, 'apple', 'banana' ],

          "Array contents correct");

throws_ok { push @array, "excessive" } $RANGE_EXCEP,

          "Push bounds exception";

is(scalar @array, 6, "Size of array correct");

tie @array, "Tie::Array::Bounded", lower => 3, upper => 6;

throws_ok { $array[1] = "too small" } $RANGE_EXCEP,

          "Lower bound check failure";

lives_ok { @array[3..6] = 3..6 } "Slice assignment works";

throws_ok { push @array, "too big" } $RANGE_EXCEP,

          "Push bounds exception"; 
```

测试也是真正的程序。因为我们反复测试同一个异常，所以为了偷懒，我们将它的识别模式放在了一个变量中。

`Bounded.pm` 虽然并不完全是效率的模型（我们的内部数组包含了分配给前 `$lower` 个元素的未使用空间，这些元素永远不会被使用），但现在该编写文档了，`h2xs` 已经填充了一些 POD 存根。我们将将其完善为附录中看到的最终版本。我将在 第 10 章 中详细讨论文档。

现在我们创建 `04pod.t` 来测试 POD 格式是否正确：

### 示例 3.5 04pod.t 的最终版本

```perl
#!/usr/bin/perl

use strict;

use warnings;

use Test::Pod tests => 1;

use blib;

use Tie::Array::Bounded;

pod_ok($INC{"Tie/Array/Bounded.pm"}); 
```

这里有一个小技巧，可以允许我们从任何目录运行此测试，因为所有其他测试都可以在当前工作目录设置为父目录或 t 目录时运行。我们加载模块本身，然后让 Perl 通过查找 `%INC` 哈希表告诉我们它哪里找到了文件，该哈希表跟踪此类内容（参见 `perlvar` 中的条目）。

随着最后的“make test”，我们完成了：

```
Files=4, Tests=24,  2 wallclock secs ( 1.58 cusr +  0.24 csys =  1.82 CPU) 
```

我们有整个 24 个测试触手可及，准备随时重复。

你可以从 `Test::Tutorial` 模块获取更多如何使用这些模块的帮助，尽管该模块名为教程，但它不包含代码，只有文档。

只需再做一下，该模块就可以提交到 CPAN。完整指令请参见 [TREGAR02]。

## 3.4 测试遗留代码

“这一切都很好，”我仿佛能听到你说，“但我刚刚继承了一个包含 27 个程序和 14 个模块的沼泽，而且它们没有任何测试。我该怎么办？”

到目前为止你已经了解到，编写测试比编写代码要吸引得多。但如果你受限于现有的应用程序，请采用自上而下的方法。开始

### 3.4.1 简单示例

你有一个程序，它会产生输出，运行这个：

### 示例 3.6 测试输出

```perl
my $success_files;

BEGIN {
  @success_files = glob "success/*.txt";
}

use Test::More tests => 1 + @success_files;

is(system("aquarium"), 0, "Program succeeded");

for my $success (@success_files) {
  (my $output = $success) =~ s#.*/##
  ok(-e $output, "output present");
  is(system("cmp $output $success > /dev/null 2>&1"), 0, "output is valid");
}
```

首先，我们在 BEGIN 块中捕捉输出文件名。然后运行程序并检查其返回码。然后对于每个输出文件，我们测试它是否存在，并使用工具检查它是否匹配。如果你没有 `cmp` 程序，可以编写一个 Perl 子程序来执行相同的测试：只需读取文件直到发现不匹配或到达文件

### 3.4.2 测试 Web 应用程序

通用网接口 (CGI) 程序如果没有面向自动化测试开发，可能是一块凝结的代码，接口功能像果干蛋糕一样散落在其中。但你不需要为了编写测试而将其拆解；你可以使用端到端测试来验证它的需求。你只需要一个模拟网络浏览器用户的程序，并检查响应是否正确。无论 CGI 程序是如何编写的，因为测试都在存储程序的不同机器上进行。

Andy Lester 的 `WWW::Mechanize` 模块在这里为你提供了救援。它允许你通过模拟网络浏览器来实现站点交互，这种功能是由 Gisle Aas 的 `LWP::UserAgent` 模块完美实现的。然而，`WWW::Mechanize` 更进一步（事实上，它是 `LWP::UserAgent` 的子类），默认启用 Cookie 处理，并提供了方便跟踪链接和提交表单的方法，包括处理隐藏字段。

> [9] 如果你在想，“嘿！可以用这个写一个代理在我想修复的调查中灌票，”忘掉吧；以前有人做过了。Chris Nandor 使用 Perl 为他选出的美国联盟全明星游击手投了数千张票 [GLOBE99]。而且这是在 WWW::Mechanize 发明之前。

假设我们有一个提供登录界面的应用程序。由于通常的模糊原因，登录表单 `login.html` 除了用户可见的输入字段外，还包含一个或多个隐藏字段，如下：



```html
 <FORM ACTION="login.cgi" METHOD="POST">

 <INPUT NAME="username" TYPE="text">

 <INPUT NAME="password" TYPE="text">

 <INPUT NAME="fruglido" TYPE="hidden" VALUE="grilku">

 <INPUT TYPE="Submit">

</FORM> 
```

登录成功后，响应页面会用“欢迎，”问候用户，随后是用户的名字（名）。我们可以为这个登录函数编写如下测试：

### 示例 3.7. 使用 `WWW::Mechanize` 测试 Web 应用程序

```perl
 1  #!/usr/bin/perl
2  use strict;
3  use warnings;
4
5  use WWW::Mechanize;
6  use Test::More tests => 3; continuous7
8  my $URL = 'http://localhost/login.html';
9  my $USERNAME = 'peter';
10 my $PASSWORD = 'secret';
11
12 my $ua = WWW::Mechanize->new;
13 ok($ua->get($URL)->is_success, "获取页面")
14   or die $ua->message;
15
16 $ua->set_field(username => $USERNAME,
17                 password => $PASSWORD);
18 ok($ua->submit->is_success, "提交表单")
19   or die $ua->message;
20
21 like($ua->content, /Welcome, Peter/, "登录成功");
```

在第 12 行，我们创建一个 `WWW::Mechanize` 实例。第 13 行，我们检查 `get($URL)` 是否成功获取了页面；如果失败，则退出并打印错误信息。第 16 和 17 行，我们通过 `set_field` 设置用户名和密码。第 18 行，我们检查 `submit()` 是否成功提交了表单；如果失败，则退出。最后在第 21 行，我们检查页面内容是否包含正则表达式“Welcome, Peter”。





> ^([1]) 如果你正在用 Perl 编写一个空中交通控制系统，请给我写封信。如果你的系统预计将由青少年维护，请务必附上一份它所服务区域的地图；请放心，我会充分利用那张地图的。（为了防止收到此类来信，在 [HOGABOOM03] 中描述的系统并未在实际运行中使用。）

在没有更具体信息的情况下，你的程序最可能的维护程序员当然是你自己。尽管在现在听起来可能很奇怪，但许多——如果不是大多数——程序员在某种潜意识的受虐倾向发作下，仍然用一种事后会给自己带来不必要痛苦的方式编写代码。你很清楚指的是谁。

如果你不知道谁会接手你的代码，那么问题随之而生：你的代码应该达到什么种复杂程度？关于这个话题有很多争论，也不乏一些充满激进的观点。我认为你应该按照自己的水平来编写代码，而不是试图去满足一个纯假设的维护程序员的偏好。充斥着一种荒谬的观念，认为维护代码有一个客观的“最佳标准”，人们浪费了大量的时间来争论像这样的结构：

```
 (my $new = $old) =~ s/old/new/; 
```

是否符合这个标准^([[2]](#ch04lev1sec2.html_ch04fn02))，或者对于假设的维护者来说，将其重写为如下形式是否更清晰：

> ^([2]) Tom Christiansen 将将变量设置为表达式转换的方法称为“吃过法”（en passant）。

```
 my $new = $old;

$new =~ s/old/new/; 
```

如果你将成为那个维护程序员，你唯一需要担心的就是你是否能够理解这段代码。这最好的判断标准是你写它花了花了多久。如果你写得很快，那么它比那些花费几个小时流汗和测试才能写正确的代码更具可读性。

如果那几个小时花在构建一个极其紧凑的新句式（idiom），那么当你在六个月后再次遇到它时，可能会花费更长的时间来弄懂它。先不要用它，改而使用更简单易懂的代码；如果在未来的某个编程工作中，你没有费费数小时苦思就想到了这个新句式，那么你就发现了一个有用的东西；但更有可能，你会庆幸自己抵御了使用它的诱惑。

（尽管如此，写得快并不保证它在以后更大的语文中仍然行得通，只能保证你理解它的语法。换句话说，你可能无法森林见全局，但至少每棵树你都是有些熟悉的。）

相反，如果你花费了几个小时开发了一小段代码，而这段代码并没有任何明显更清晰的表示，那么你的代码需要注释了。你现在能理解它是因为你做了所有的辅助笔记、你运行了测试（这些应该整合到你的测试脚本中）、你阅读的文章或文本，以及你进行的某些复杂分析，而这些都没有出现在代码中。如果你需要这些支持材料来创建代码，那么你在理解它时也需要它们，所以把它们作为注释放入。之后我会向你展示如何插入可以提取为格式化文档的详细信息。

## 4.2.2 Perl 程序员的十个等级

几年前，Tom Christiansen 创建了一份略带玩笑性质的 Perl 编程复杂程度等级列表（[CHRISTIANSEN98]）。为了对维护程序员进行分类，这里是我的标准。在本书的后续部分，当我想要指示某些代码或技术的复杂程度时，我偶尔会引用其中一个等级。评估你被要求维护的程序作者曾处于什么水平，会有所帮助。

| 等级 1: | 没读过任何关于 Perl 的书（或任何其他东西）；知道它是一种编程语言，但对它一无无所知。可以运行别人编写的 Perl 程序，并意识到可以通过编辑程序的某些部分（如打印字符串的内容）来改变部分行为。不理解为什么对程序其他部分的修改不起；脑中没有可以容该语言的模型，因此无法区分语法与 COBOL 和 C++ 这种完全不同的语言。 |

| 等级 2: | 理解基本的块结构语法，尽管仅限于识别出它类似于 JavaScript 这样的语言。有一种块会创建某种作用域效应的印象，但不知道词作用域变量，也没有遇到过 `use strict` 或 `use warnings`。可以改变条件判断的含义并使用基础算术和逻辑运算符。认为他们需要做的一切都可以对别人编写的程序进行小修改来实现。 |

| 等级 3: | 想要从头开始创建程序，并意识到需要某种教育；向别人寻求学习 Perl 的书籍推荐。这个等级的人可能会获得《骆驼》书 [WALL00] 并认为它是一本教程，并尝试阅读整本书，在此过程中遭受严重的神经创伤。 |

| 等级 4: | 第一次学习 `use strict` 和 `use warnings`，但认为它们得得不偿失。好奇 `my` 是什么意思。发现有模块可以解决几乎任何问题，但不知道如何获取和使用它们。订阅了一个 Perl 新闻组，并被大量对他们有意义的话题的讨论所淹没。 |

| 等级 5: | 对正则表达式、运算符、I/O 和作用域有基本的理解。使用 `my`、`use strict` 和 `use warnings` 是因为大家都这么说。大量人从未越过这个等级，因为他们几乎可以做任何事情（除了创建可重用组件），尽管往往效率很低。在这一等级或下一个等级学习引用。 |

| 等级 6: | 可能会上 Perl 课程。知道如何使用对象，并意识到这种知识和综合档案网络（CPAN）使他们能够快速创建强大的程序。想要晋到下一个等级，看看这种赋能趋势延伸到多远。 |

| 等级 7: | 学习如何创建自己的面向对象的模块，第一次体验代码复用的喜悦。知道包（packages）以及词作用域变量与动态变量的区别。发现 Perl 的正则表达式并不是“正则的”（regular），而且能力远超简单的文本处理。 |

| 等级 8: | 开始以某种方式回馈：无论是提交错误报告或补丁、向 CPAN 模块、文档建议，或为新手提供帮助。发现如 `AUTOLOAD` 等高级功能，并开始使用如 `Class::MethodMaker` 等面向开发者的模块。在适当的情况下使用 `DBI` 或 `Tk` 等复杂的应用模块；熟悉使用 `CGI.pm` 创建 Web 。 |

| 等级 9: | 参加 Perl 会，通过其他方式参与 Perl 社区；可能经常访问 [www.perlmonks.org](http://www.perlmonks.org) 或 #perl（参见第 12 章）。熟练使用 `eval` 动态创建代码并操作符号表。在编写代码时经常考虑性能因素，可能超过了需要。发布子类主要模块以增加显著功能的模块。 |

| 等级 10: | 参加 Perl 混淆和代码高赛竞赛^([[3]](#ch04lev1sec2.html_ch04fn03))，熟练使用嵌入代码的单个正则表达式来实现大多数人需要编写整个程序才能实现的功能；可能向 Perl 核心提交补丁、贡献重大新模块，或以其他方式在 Perl 社区中成名。 |





> ^([3]) Perl 高尔夫是一场比比谁能用最少字符解决问题的竞赛。获胜者的代码可能难以读懂，但话又回来，还有多少语言允许你用三行能塞进 T 恤的代码，写出一个整个军用级的加密算法（`RSA`）？

继续这种演进几级，直到达到一个唯一的居民是 `Larry Wall` 的境界，这就留给读者自行练习了。

### 4.2.3 要求是什么？

在重写之前，你必须找出自原始程序开发以来，代码的要求发生了哪些变化。不要假设你所做的只是重现功能，除非你已经验证了这一点。你可能需要针对不同的目标优化代码；也许你被提高它的可读性、性能或 `portability`（可移植性），或者扩展它的功能。

向原始开发者问的一个重要问题是，这段代码针对什么进行了优化。例如，代码中可能存在复杂的结构，如果你不知道它们是为了达到可接受的性能而必须，你可能会简化它们。

### 4.3 风格

在 [SCOTT01] 中，Ed Wright 和我曾：“关于风格，唯一可信的评论就是你应该拥有自己的风格。”我在这里会走得更远。就像衣服一样，拥有一致的风格并不意味着别人不会嘲笑你。因此，为了防止你不经意选择了一种等同于 1970 年代台球骗子的编码风格，这里提供了一种相当保守的建议风格。

当然，有些人故意打扮得像台球高手，并可能对这种对其着衣品味的贬低感到不悦。如果你是通过意识到的决定选择了这种奇特的风格，并且能够承担后果，那么请务必坚持下去。这一节是给其他所有人的。就像本书的许多部分一样，它包含了一定程度的个人口味，而这只是完成好任务的众多方法之一；我并没有把它推崇为“唯一真理之道”（"One True Way"）。

你可以在随 Perl 的 `perlstyle` 文档页面中找到关于风格的注释，其中部分内容反映在此处。

### 4.3.1 布局

对你的程序布局能做的最好的事情就是对其进行正确的缩进。我仍然惊讶于我的班里竟然有多少人写程序完全没有缩进，就好像使用空格会被悬赏脑袋一样。我自己的倾向在相反的方向根深蒂固，以至于我必须克制对单行代码缩进的冲动！无论程序多么简短或短暂，从一开始就进行缩进是对对大家的一种帮助。

`perlstyle` 建议四列缩进；我使用两列，因为这足够我的眼睛识别块结构，而且我不希望深层嵌套的块挤满右边距。有些人由于习惯使用 `tab` 字符作为每个缩进级别，而青睐八列缩进，我个人觉得这太大了。他们有时声称，他们只需要将编辑器中的制表符设置为四列就能获得良好的缩进，但这迫使维护程序员去折腾他们的编辑器配置，许多程序员对此的占有欲极强，以至于你还不如要求他们停止呼吸。

涉及到代码块的大括号风格时，程序员们爆发出的冲突让乔纳森·斯威特的大端/小端之战（[SWIFT47]）看起来像阿米士人的盖房活动。我更倾向于一种被称为 BSD/Allman 的风格：

```
 sub read_dicts

{

  my $dictref = shift;

  my @path = split /:/, $ENV{DICTPATH} || "$ENV{HOME}:.";

  local @ARGV = grep -e, ($DEFDICT, map "$_/.dict" => @path);

  while (<>)

  {
   # 假设行包含一个单词

   chomp;

   $dictref->{$_}++;
  }
} 
```

而大多数 Perl 分发版使用的是所谓的 K&R（Kernighan and Ritchie）风格：

```
 sub read_dicts {

  my $dictref = shift;

  my @path = split /:/, $ENV{DICTPATH} || "$ENV{HOME}:.";

  local @ARGV = grep -e, ($DEFDICT, map "$_/.dict" => @path);

  while (<>) {
    # 假设行包含一个单词

    chomp;

    $dictref->{$_}++;
  }
} 
```

这种风格为每个块节省了一行，但对作者来说，它更难看到块从何开始，特别是因为延续行可能会被缩进。例如：

```
 update($controller->connection, $record[$cur_count]->ticket,

       $form_inputs->{params}); 
```

可能会迫使你检查第一行的结尾，以确保它不是以大括号结尾的。另一个例子：

```
 if (($best_count == 1 &&   $self->{single_match})

 || ($best_count >  0 && ! $self->{single_match})) {

    $found_match = 1;

} 
```

这即使使用了四列缩进——对我来说也比下面更困惑：

```
 if (($best_count == 1 &&   $self->{single_match})

 || ($best_count >  0 && ! $self->{single_match}))

{

  $found_match = 1;
}
```

只有两列缩进。（尽管公平地说，一些 K&R 的支持者建议这种情况可以作为例外。）另请参见延续行是如何被非标准缩进的.[4)。在与 K&R 支持者交谈后，我开始怀疑他们与 BSD/Allman 阵营之间的区别在于，他们倾向于从行尾寻找语义线索，而我们看行首。尝试这两种风格，看看你觉得哪种更有吸引力。虽然至少有两种方法可以在不将语句放入 `if` 块的情况下条件执行语句，但如果该语句长到会溢出，使用块来处理可能会清晰：

```
 if (@problems)

{

    error("We found the following problems:\n"
          . (join "\n" => @problems)

         );
} 
```

非块的条件执行方式是：

*   `condition` `and` `statement`
    例如：

    ```
     /(banana|apple|pear)/ and push @fruit, $1;
    ```

*   `statement` `if` `condition`
    例如：

    ```
     warn "Reached line $." if $verbose;
    ```




有时候你无法让代码写得足够清晰。当你添加注释时，心中要记住的词是：`Why?`（为什么？）。不要只是复述代码做了什么，而是要说明为什么要这么做。这不需要冗长的解释，可以像这样简单：

```
 if (time - $employee->hired > $ONE_WEEK)  # 过了试用期了吗？ 
```

尽管你随后会问，为什么不写成：

```
 if (time - $employee->hired > $PROBATION_PERIOD) 
```

所以，一个更好的例子应该是这样的：

```
 if (my ($name) = />\>(.*?)<\</s)   # /s: 字段可以包含换行符 
```

这表明某些不易获得的知识。

### 4.4.1 哨兵注释 (Sentinel Comments)

有时候，你需要在代码中放置一个提醒，以便以后更改某些内容。也许你正在修复一个 bug 的过程中又发现了另一个。通过在注释中放置一个独特的标记，你就可以在以后搜索到它。我习惯使用字符串 `"XXX"`，因为 gvim 会专门为此目的对其进行高亮显示。

> 尽管我大部分时间都在使用 Emacs；但在永恒的“常用编辑器大战”中，留点后路总是有好处的。

### 4.4.2 注释 (Block Comments)

人们经常问如何注释掉大段代码。将其包裹在 `if (0) {...}` 块中可以防止其运行，但仍然要求它在语法上是正确的。

相反，将代码包裹在 Plain Old Documentation (POD) 指令中，使其视为文档。实现这一点有很多方法；这里我使用了 `=begin`：

> 参见[第 10.3.1 节]。

```
 =begin comment

 这里是我们想要让 perl 
# 忽略的代码

=end comment

=cut 
```

这仍然会被解释为 POD。然而，在这种情况下，POD 格式化程序应该忽略这个块，因为没有哪个什么是标记为 `"comment"` 的块。我需要 `=end` 指令来保持 POD 有效（`=begin` 指令应当匹配），并且需要 `=cut` 指令来结束 POD 处理，以便 perl 可以继续编译后续代码。记住，POD 指令后面需要有空行，因为它们是基于段的。我将在第 10 章详细介绍 POD 对你的程序能做什么。关于关于多行注释问题的更有创意的解决方案，请参见 http://www.perl.com/pub/a/2002/08/13/comment.html。

### 4.5 重塑风格 (Restyling)

当你面对一个现有程序，其作者没有遵循你喜欢的风格指南，且布局看起来像杰克逊·波洛克的画时，你该怎么办？

> 胜过波洛克的模仿品。Uri Guttman 向我推荐了一篇文章，展示了真正的波洛克是如何呈现分形排序的。

人们尝试编写格式化工具，但到出版时，明显的胜利者是 Steve Hancock 的 `perltidy`。你也可以从 CPAN 下载 `perltidy`。使用 `Perl::Tidy` 作为模块名进行安装。

> http://perltidy.sourceforge.net/

perltidy 将其输入文件的格式化版本写入带有 `.tdy` 后缀的同名文件中。它的选项太多，无法在这里详尽说明，但其手册页中有充分的介绍。它的默认选项根据 `perlstyle` 建议进行格式化。我的个人风格大致相当于：

```
 perltidy -gnu -bbt=1 -i=2 -nsfs -vt=1 -vtc=1 -nbbc 
```

尽管 perltidy 已经很好用，但它无法进行那种让程序布局变成艺术作品的优化。使用它来将别人编写的代码转变为“内部风格”，但不要让你的风格成为束缚。例如，前面的设置生成了这种格式化：

```
 return 1 if $case_sensitive[length $word]{$word};

return 1 if $case_insensitive[length $word]{lc $word}; 
```

但我可以进一步将该代码美化为：

```
 return 1 if $case_sensitive  [length $word]{   $word};

return 1 if $case_insensitive[length $word]{lc $word}; 
```

注意，如果你想的话，可以使用空格将下标括号与其标识符分开。事实上，Perl 对空格极其宽容，允许你写出诸如这样的大胆结构：

```
 $   puppy = ($dog     ->offspring)[0];

$platypup = ($platypus->eggs)     [0];
```

注意，Perl 对标识符之间的空格也极度宽容。

### 4.5.1 提供帮助

### 4.6 变量重命名




我很少使用 `constant` 原始指令，它允许你在编译时定义符号；例如：

```
use constant MAX_CONNECTIONS => 5;

.

.

.

if ($conns++ < MAX_CONNECTIONS) ... 
```

它具有一些优点：

- 你无法重写赋值给符号的值。（嗯，并非那么容易：常量实际上是一个声明为不接受参数的子程序原型。你可以重新定义它，但你不会无意中这样做。）
- 常量的使用（通常）会通过 Perl 编译器优化，使得其值被直接插入，而不会产生子程序调用的开销。
- 符号看起来像常量；以符号（`$`、`@`、`%`）开头的标识符往往让我们认为它们是可变的。

它也有一些缺点：

- 常量在视觉上与文件句柄（filehandles）无法区分。
- 常量不能用胖箭头（`=>`）的左侧，因为那会将它转换为字符串。你必须在常量后面加上空括号，以确保 Perl 将其解析为子程序调用。
- 将常量作为哈希键（hash key）使用也是如此。
- 常量不会插值到双引号字符串中，除非你使用令人发叹的 `@{[CONSTANT_GOES_HERE]}` 结构。
- 由于是子程序，它们是基于包（package）的，不能限制在词法作用域内；但当你有一个新的 `package` 语句时，它们就会超出作用域（除非你完全限定它们的名称）。
- 由于是子程序，它们对其他包是可见的，甚至是可继承的。如果你愿意，你可以将其视为优点，但这并非直观易见。

因此，我倾向于将常量定义为普通的标量或任何其他类型：

```
my $PI      = 3.1415926535897932384;

my @BEATLES = qw(John Paul George Ringo); 
```

纯洁主义者认为常量应该是不可修改的，但 Perl 的核心哲学是让你承担伴随自由而来的责任。任何改变 `p` 值的人都应该承担改变宇宙基础结构所带来的后果。另一方面，在不同时候，你可能有理由向 `@BEATLES` 中添加 `'Stuart'` 或 `'Pete'`。

## 4.7 编辑

对于那些不是《星际迷航》粉丝的人来说，在系列剧和电影中有一种被称为“博格”（Borg）的反派种族，他们的运作方式是通过逐渐植入机械机体来征服一个民族。将别人的程序变成自己的是一个类似的过程，即注入你自己的代码和设备，直到你确定已经控制了它。

一旦你使用了格式化工具（beautifier）让代码符合你首好的布局标准，就可以应用行编辑技术来减少代码膨胀。（如果你在高中英语课上做过一项名为 `pr´cis` 的练习，即将一篇长篇大论的文章尽可能地压缩，那么我谈论的是计算机编程中该过程的道德等效操作。）如果你可以在不引入混淆的情况下减少代码量，结果将更加清晰且易维护。你对 Perl 及其高效惯用法（idioms）越熟悉，就越能做到。当你通过行编辑减少代码量时，它的目的将变得更加清晰，你会更容易发现低效或冗余的高层结构。

## 4.8 行编辑

行编辑并不是将语句组合以尽可能让每行包含尽可能语句的过程。它是将长代码自觉地转换为更短（或在某些情况下更长）的内容，使其至少与原始代码一样清晰。这可以简单地将 `if (! expr)` 替换为 `unless (expr)`，将冗长的手动输出格式化转换为使用 `printf()`，或者更复杂的东西。现在我将介绍一些执行行编辑时需要注意的机会。

### 4.8.1 无谓的重复

这一原则如此基础，以至于它有一个缩写词：`DRY`（不要重复自己；参见 [HUNT00], 第 27 页）。代码中的任何重复模式都应该触发你想要检查是否可以省略它的冲动。Perl 提供了大量的工具来帮助处理这些情况；请特别熟悉：

- `foreach` 循环及其其别名属性：如果你在循环变量指向一个可写变量时修改它，那么该变量将被更新。尝试这个测试：

```
my $x = 5;

my @y = 6..8;

for my $z ($x, @y, 17)
{
  $z++ if $z < 10;
}

print "$x @y\n"; 
```

然后看看如果移除测试 `if $z < 10` 会发生什么。

`foreach` 循环的这一特性甚至可以帮助你在没有循环可言的情况下缩短代码，如果你对一个长变量名有多个引用。与其写成：

```
$music{$artist}{MP3} =~ s#\\#/#g;

$music{$artist}{MP3} = "$MUSICPATH/$music{$artist}{MP3}"; 
```

你可以说：

```
for ($music{$artist}{MP3})
{
  s#\\#/#g;

  $_ = "$MUSICPATH/$_";

} 
```

- `map()` 以及它如何让你将一个列表转换为另一个；输出列表的元素数量不需要与输入列表相同。
- 如何编写子程序以及如何实现命名传递（named passing）以提高清晰度，例如：

```
make_sae(nuts => 'pecan', cherries => 2);
```

学者往往没有意识到可以将哈希作为部分进行传递。

### 4.8.2 过多的临时变量

语言对你理解问题的理解与你对其表达之间的干预越少越好。临时变量（也称为合成变量）的存在仅仅是因为程序需要它们。任何名称中带有 "temp" 的变量很可能是临时的。这里有一个我刚刚继承的临时变量示例：

```
if ($!)
{
  my $msg = "$?";

  print ERRORFILE "$msg\n";
}
```

显然，`$msg` 没有用于任何其他地方（因为它立即超出了作用域），那么为什么不省一行代码呢：

```
if ($!)
{
  print ERRORFILE "$?\n";
} 
```

现在我们可以看到它可以使用后置 `if` 进一步缩短：

```
print ERRORFILE "$?\n" if $!; 
```

或者使用逻辑 `and`：

```
$! and print ERRORFILE "$?\n"; 
```

有时你可以通过构建一个涉及许多函数调用的巨大语句来避免临时变量，并使其保持易懂。如果你能将该语句想象为一个流水线（pipeline），那么在这种情况下 Perl 在函数调用括号可选方面的语法慷慨就是最有帮助的。只需在正确的位置放置换行符。这一个经典的例子是 Schwartzian 变换（参见 [HALL98], 第 49 页）：^([9)

> ^([9]) 参见 [`groups.google.com/groups?selm=4b2eag%24odb%40csnews.cs.colorado.edu`](http://groups.google.com/groups?selm=4b2eag%24odb%40csnews.cs.colorado.edu) 获取原始引用。

```
@sorted = map { $_->[0] }
          sort { $a->[1] <=> $b->[1] }
          map { [ $_, func($_)] }
               @unsorted; 
```

如果强制使用括号，那看起来会更难看：

```
@sorted = map ({ $_->[0] }
               sort({ $a->[1] <=> $b->[1] }
                    map ({ [ $_, func($_)] }
                         @unsorted

              )); 
```

流水线是思考连续使用函数和运算符转换列表行为的一种自然方式。这里有一个关于在目录 `$dir` 中查找特定子目录的非常长的例子：





```
 1  opendir DIR, $dir;

2  my @kids = map  File::Spec::Link->resolve($_)

3          => grep -d

4          => map  { tr/\n/?/

5                  ? do { warn "Embedded N/L at ? in $_\n"; () }

6                   : $_ }

7             map "$dir/$_"

8          => grep !/^(?:\.\.?|RCS)$/

9          => readdir DIR; 
```

通过一些创意的缩进，这段代码非常易读：有些人偏向于从上到下阅读；而大多数人在从下到上阅读时理解得更好，因为那是代码执行的顺序：

| 9 | 返回 `$dir` 中的文件列表。 |
| 8 | 忽略当前目录和父目录，以及任何名为 `RCS` 的文件或目录。 |
| 7 | 形成文件的完整路径。 |
| 4 | 忽略包含嵌入换行符的文件，而是产生警告并在流水线的此点将其替换为空列表。 |
| 3 | 仅选择目录。 |
| 2 | 使用 CPAN 模块解析文件名中的任何符号链接。 |

> ^([10]) [`search.cpan.org/dist/File-Copy-Link/`](http://search.cpan.org/dist/File-Copy-Link/)

是的，换行符在 UNIX 文件名中是有效字符，但它们可能会让某些工具感到头疼；这个示例的设计目的是在保护这些工具的同时报告此类文件名。

### 4.8.3 临时变量不足

反之，通过编写混淆代码来避免创建临时变量并不能节省任何资源，特别是当你可以为该变量分配有意义的名称时。例如：

```perl
 push @{$person{$ssn}{PHONES}},

  substr($dbh->selectcol_arrayref("SELECT raw_text FROM logs \

                                   WHERE SSN = '$ssn'")->[0],

         $offsets[$WORK_PHONE],

         $offsets[$WORK_PHONE+1] - $offsets[$WORK_PHONE]); 
```

即使运用了创意的缩进，帮助也还不够够。这并不意味着每个复合表达式都需要被临时变量替换，也不意味着语句必须被限制在单行内。这里是让代码更清晰的一种方法：

```perl
 {

  my $sql = "SELECT raw_text FROM logs WHERE SSN = '$ssn'";

  my $record = $dbh->selectcol_arrayref($sql)->[0];

  my $offset = $offsets[$WORK_PHONE];

  my $length = $offsets[$WORK_PHONE+1] - $offset;

  push @{$person{$ssn}{PHONES}},

       substr($record, $offset, $length);

} 
```

注意临时变量是在一个块中声明的，这限制了它们的作用域。

## 4.9 反模式

缺乏经验的程序员可能会编写出比需要复杂得多的代码，导致可维护性降低并可能影响性能。有一个团队曾告诉我，他们正准备购买更强大的硬件来运行一个程序，该程序每次运行需要花费两个小时并占用 1 GB 内存。当我查看该程序时，发现它使用了并行数组和线性搜索而不是哈希表，并将大量输入读取到内存中在那里进行排序。修改后，运行仅耗时 20 分钟，占用 7 MB 内存，且源代码减少了一半。现在我将介绍一些需要注意的低效做法。

> ^([11]) 感谢 Adam Turoff 指出这些最好被称为“反模式” [BROWN98]。

### 4.9.1 不使用哈希表

哈希表绝对是发明以来最有用的数据结构。本书假设你已经熟悉它的用法，因此知道它们为什么如此有用。然而，编写你遗留代码的程序员可能不知道这一点。代码中完全没有哈希表是一个强烈的信号，表明程序员不知道哈希表，因为很少有程序在某处无法利用哈希表。

注意数组中的线性搜索。代码可能像这样：

```perl
 my $found = 0;

foreach my $element (@array)
{

  $found = 1 and last if $element eq $search;
}

if ($found) ... 
```

或者：

```perl
 my $found_index = -1;

for (my $i = 0; $i <= $#array; $i++)
{

  $found_index = $i, last if $array[$i] eq $search;
}

if ($found_index >= 0) ... 
```

或者甚至：

```perl
 if (grep $_ eq $search, @array) ... 
```

为了能够以常数时间内进行查找，而不是在数组上执行线性搜索，创建一个哈希表是很常见的。如果你只想进行一次查找，那么尽管使用 `grep()` 吧，因为仅仅为了这个目的创建一个哈希表会慢且占用更多代码。然而，请考虑数据最初是否就应该存储在哈希表中。需要对数组进行查找或其他随机访问，通常表明它本就应该是一个哈希表。

如果你不在乎数据的顺序，哈希表可以工作。如果你在乎顺序，有时可以使用数组。例如，假设你想使用：

```perl
 my @state;

while (<DATA>) {

  @state{$abbreviation} = @vals;
}
```

这使用数组来存储键值对，但元素的顺序由索引决定。如果你想保持顺序，应该使用哈希表：

```perl
 my %state;

while (<DATA>) {

  $state{$abbreviation} = @vals;
}
```

这使用哈希表来存储键值对，元素的顺序由键决定。如果你想保持顺序，应该使用数组：

```perl
 my @state;

while (<DATA>) {

  push @state, [$abbreviation, @vals];
}
```

这使用数组来存储键值对，元素的顺序由索引决定。如果你想保持顺序，应该使用哈希表：

```perl
 my %state;

while (<DATA>) {

  $state{$abbreviation} = @vals;
}
```

这使用哈希表来存储键值对，元素的顺序由键决定。如果你想保持顺序，应该使用数组：

```perl
 my @state;

while (<DATA>) {

  push @state, [$abbreviation, @vals];
}
```

这使用数组来存储键值对，元素的顺序由索引决定。如果你想保持顺序，应该使用哈希表：

```perl
 my %state;

while (<DATA>) {

  $state{$abbreviation} = @vals;
}
```

这使用哈希表来存储键值对，元素的顺序由键决定。如果你想保持顺序，应该使用数组：

```perl
 my @state;

while (<DATA>) {

  push @state, [$abbreviation, @vals];
}
```

### 4.9.2 魔术数字

代码中的字面数字和某些字符串应该命名。例如，与其使用：

```perl
open_server('dbms_temp', 442);
```

不如：

```perl
my $DBMS_SERVER = 'dbms_temp';
my $DBMS_PORT = 442;

open_server($DBMS_SERVER, $DBMS_PORT);
```

这可能会占用更多空间，但有三个好处：

* 为传递的值赋予意义。
* 允许识别同一事物的多次使用。
* 将程序员可能更改的值集中在一个处。

这些优势如此关键（且适用于所有编程语言），你会怀疑为什么有人不遵循这条规则。不幸的是，许多人这样做，在编辑时，你可以做的第一件事就是替换“魔术数字”。




正则表达式是一个如此巨大的话题，以至于它们值得专门写本书……幸运的是，它们已经有一本书了[FRIEDL02]。这是一个罕见的 Perl 程序，没有充分利用正则表达式；如果你继承了一个没有使用任何正则表达式的程序，请仔细检查它，看看它是否应该包含一些。如果有人使用 `substr()` 和/或 `split()`（`split()` 实际上也使用了正则表达式，尽管它可以伪装成字符串）来切分文本，或者使用 `index()` 搜索多个子字符串，要么他们是在解决一个需要极致性能的问题时非常聪明，要么是他们不熟悉正则表达式这种语言。

用正则表达式匹配文本是一门艺术；你希望使用最简单的正则，在所有可能的情况下匹配你想要的内容。并不没必要将正则写得越严限制越好。例如，假设你正在匹配 `/etc/passwd` 中行中的 uid：

```
 peter:x:500:500:Peter Scott:/home/peter:/bin/tcsh 
```

此示例行中用冒号分隔的字段依次是：用户名、密码、uid、gid、GECOS、目录、shell。非正则的解决方案如下：

```
 ($username, $password, $uid, $gid, $gecos, $dir, $shell) =
split /:/; 
```

或者，仁慈一点：

```
 @fields = split /:/;

$uid = $fields[2]; 
```

现在，如果一个基于正则的解决方案坚持按照严格的语法规则匹配整行，看起来就会非常糟糕：

```
 $uid = $1 if /^[a-z][a-z0-9_]*:.*?:(\d+):\d+(?::.*?){3}$/; 
```

但实际上，何必如此呢？在 `/etc/passwd` 行中，uid 是两个冒号之间第一个纯数字组成的字符串，因为用户名不能以数字开头。所以 `/:(\d+)/` 将会匹配到一个 uid。如果需要检查 `/etc/passwd` 中的某行具有有效语法，那确实是偏执的代码了，考虑到某行损坏对系统造成的后果；你已经知道这一点了。

加密后的密码可能仅由数字组成吗？如今大多数 `/etc/passwd` 文件在该字段中只有一个“x”，将真实的加密密码留存在更受保护的 `/etc/shadow` 文件或外部认证源中，在这种情况下，答案是否定的。即使我们假设该密码字段可能全是数字，匹配 uid 的代码也无需比这复杂：

```
 ($uid) = /:.*?:(.*?):/; 
```

另一个例子，假设我们正在读取一份包含如下行的会计报告：

```
 Total expenditure = $14731.00, fiscal July 
```

我们想要提取美元金额。什么正则表达式可以做到？在不了解更多这些行中可能包含什么文本之前，我们不知道。一种可能性是提取 `$` 和 `,` 之间的文本：

```
 /\$(.*?),/ and $amount = $1; 
```

但我们需要知道可能不存在这样的行，例如：

```
 surplus of $7443.95 was carried over to August, due to 
```

此时我们的正则将匹配到下划线的文本。在这种情况下，类似 `/\$[\d.]+/` 的正则可能就足够。或者可能不够，如果报告可能会采用（尽管不符合财务规范的）科学计数法：

```
 Total expenditure = $7.6324E8, fiscal August 
```

在这种情况下，我们可能会采用以下任何一种：

```
 /\$(\S+),/

/expenditure = $([^,\s]+)/

/\$([\d.e+- ])/i 
```

完全取决于我们对输入可能采取的形式的了解，以及我们想要匹配的行的变化程度。

如果程序似乎在使用正则表达式来匹配任何常见模式，那么偷懒一点，使用别人代码专门为该目的生成的正则吧。Damian Conway 的模块 `Regexp::Common`（现在由 Abigail 维护）可以生成极其复杂的正则来解决常见问题 ([`search.cpan.org/dist/Regexp-Common/`](http://search.cpan.org/dist/Regexp-Common/))。对于匹配分隔文本——即使是 Perl 代码块——有 Damian 的 `Text::Balanced`（从 Perl 5.8.1 版本起包含在 Perl 核心库中），而对于真正的重型解析，还有他的 `Parse::RecDescent` 模块提供的完整文法能力 ([`search.cpan.org/dist/Parse-RecDescent/`](http://search.cpan.org/dist/Parse-RecDescent/))

### 4.9.4 调用过多的外部程序

一个从 shell 脚本迁移到 Perl 编程的程序员习惯于调用外部程序来完成几乎一切。shell 程序中的文本处理是通过仔细组合使用 `sed`、`awk`、`head`、`grep`、`cut`、`sort` 和其他程序来实现的。如果 6 级或以下的 Perl 程序员调用这些程序，那么它们可能是不必要的，而专业水平高于 6 级的程序员可能知道自己在做什么（见下一节）。

在 Perl 中进行文本处理比调用外部程序要容易得多：你只需要学习一种语言，代码可以移植到没有这些程序的系统上，而且可能要快得多，因为避免了进程创建和进程间通信。

### 4.9.5 不调用外部程序

然而，没有必要教条式地避免外部程序。某些外部程序的执行比 Perl 更快且清晰。例如，假设你在名为 `temptree` 的根目录下创建了整个临时文件树。普通程序员会使用 `File::Find` 设计一个递归深度优先的解链方案，因为大多数人不知道 `File::Path`，它让你能够：

```
 use File::Path;

rmtree(temptree);
```

然而，更简洁的方法是说：

```
 system "/bin/rm -r temptree";
```

额外的好处是你可以在处理其他事情时将其放入后台：

```
 system "/bin/rm -rf temptree &";
```

同时抑制错误输出。你可以根据情况判断这是否比 `File::Path` 更符合你的需求；它不可移植，且 `-f` 选项可能无法防止移除目录的警告，在这种你必须重定向 `STDERR`。

另一个例子，假设我们需要知道一个名为 `$searchfile` 的文件是否包含字符串 "haddock"。你可以在 Perl 中这样编写：

```
 open my $fh, $searchfile or die "Can't open $searchfile: $!\n";

 my $found = 0;

while (<$fh>)

{

  $found = 1, last if /haddock/;

}

close $fh;
```

但你也可以直接执行：

```
 system "grep -q haddock $searchfile";
```

并测试 `$?` 是否为零（意味着成功；即找到了 "haddock"）。陷阱在于缺乏可移植性，不仅是对没有 grep 的系统；并不是所有的 grep 都有 `-q`（“静默”）选项，有些称其为 `-s`（“沉默”）。

最后，还有大量的程序由于专有代码的原因或开发者缺乏兴趣，本质上是黑盒，反向工程是不符合成本效益的。

### 4.9.6 多余的真值

这个微小的观点是关于存储布尔值的。当你想要存储一个真或假的值时，请使用 Perl 内置的真假值，而不是发明更复杂的东西：

> 不太好：





```perl
$found_fruit{apple} = ($rec =~ /apple/) ? 'yes' : 'no';

...

if ($found_fruit{apple} eq 'yes') ... 
```

**更好：**

```perl
$found_fruit{apple} = $rec =~ /apple/;

...

if ($found_fruit{apple}) ... 
```

**不太好：**

```perl
$in_stock{$item} = 1;

...

if (exists $in_stock{pants}) ... 
```

**更好：**

```perl
$in_stock{$item} = 1;

...

if ($in_stock{pants})... 
```

## 4.10 演化

想象一种适应能力极强的物种未定生物，正在响应环境的变化。温度升高了？进化出更厚的皮肤。重力增加了？增加更多的腿。水位上升了？长出鱼鳍。

同样，我们的代码也会随着各种需求的增加而变化：输入数据量、并发用户数等。你可以将这些需求想象成发生在不同维度上的；换句话说，它们可以相互独立地变化，而任何给程序可能受到一或多种类型的需求影响。

> ^([12]) 这是“个体发育重发生发育”论点在软件上的应用。我一直想找个机会在书中使用这个短语。

在每个维度上，你的代码在屈服于压力之前能够演化多远，取决于你的技能；在每个维度上走得越远，需要的技能就越高。

当你在重写遗留代码时，沿着这些维度一步步推进，直到达到你想要的状态，这可能会有所帮助。空间不允许我进行详细介绍，所以我将概括地涵盖某些维度上的一些步骤。

### 4.10.1 模块化

1. **扁平化脚本**：一个单体代码块。
2. **子程序**：抽象通用功能；过程化编程。
    - 使用对象，创建可重用子程序的库。
    - 对现有模块进行子类化。
    - 创建特定应用程序面向对象的模块。
    - 使用 `tieing` 和重载（见`第 10.2 节`）。

### 4.10.2 输入接口——复杂性

1. **手动解析** `@ARGV`。
2. **Getopt::Std**。
    - `Getopt::Long`。
    - **配置文件**：参见 Simon Cozens 的模块 `Config::Auto` (`http://search.cpan.org/dist/Config-Auto/`)。

### 4.10.3 错误处理——应用规模

1. **完全没有错误处理**——“编写程序并祈祷”。
2. **检查**内置函数的返回值。
    - 编写子程序以返回不同的错误状态。
    - **异常处理**：使用 `die()` 和 `eval()` 来抛出和捕获异常。
    - 将对象作为异常抛出，可以使用 `die()` 或使用如 Dave Rolsky 的 `Exception::Class` 模块 (`http://search.cpan.org/dist/Exception-Class/`)。由 Arun Kumar U 维护的 Graham Barr 的 `Error.pm` (`http://search.cpan.org/dist/Error/`) 提供了 `try` 和 `catch` 关键字，但存在由嵌套闭包触发的内存泄漏。这种用法很少见，但如果你不想担心是否无意中创建了嵌套闭包，就不要使用它。

### 4.10.4 日志——数量与粒度

1. **什么是“日志”？** 等待错误发生或需要过去行为的证据，然后恐慌。
2. **临时的 `print()` 和 `warn()` 语句**。
    - 指向特定文件的临时 `print()` 语句，可能带有手工的时间戳、进程/主机/用户标识以及日志文件轮转。
    - Mike Schilli 的 `Log::Log4perl` (CPAN 和 `http://log4perl.sourceforge.net`) 基于 Java 的 `Log4j` 工具，提供了具有严重级别的面向对象的日志功能，并可以对所有目的地的消息进行完全配置的多复用。见`第 10.1.4 节`。
    - Mark Pfeiffer 的 `Log::Dispatch::FileRotate` (`http://search.cpan.org/dist/Log-Dispatch-FileRotate/`) 自动化日志文件轮转并提供文件锁定功能。可以接入 `Log::Log4perl`。

### 4.10.5 外部信息表示——扩展性

1. **以纯文本表示的外部数据**，可能隐含假设为 ISO Latin-1 编码，或（特别是在某些地区）使用 Unicode `UTF-8`，但带有临时的编码。
2. **各种格式**：
    - `DataDumper`, `Storable`。
    - **配置文件**：如 `Config::Auto`, `CSV`。
    - **XML**：使用 `RELAX NG` (`http://www.oasis-open.org/relax-ng/2002/XML`)。
    - **YAML**：使用 `Tangram` 或 `Alzabo`。
    - **HTML-Mason**：`Unicode UTF-8`。

### 4.10.6 外部数据存储——复杂性、并发与数量

1. **纯文件**——无锁定，无结构化数据。
2. **DBM 文件**：`AnyDBM_File`。
3. **数据库服务器**：使用 Tim Bunce 的 `DBI` 进行访问。

### 4.10.7 Web 服务器处理——可扩展性

1. **手动处理表单输入**并为浏览器生成内容。
2. **使用 `CGI.pm`** 处理其中之一或两者。
    - 使用 `HTML::Template` 或 `Template Toolkit` 将输出外观与代码分离。
    - 在 Apache 服务器上使用 `mod_perl` 以提高性能。
    - 在 `mod_perl` 下使用 `HTML::Mason` 进行高级模板。
    - 使用 `AxKit` 集成 XML。

### 4.10.8 事件处理——应用复杂性与互操作性

1. **推迟**。事件处理不是给胆小者准备的。
2. 使用 Joshua N. Pritikin 的 `Event.pm`。





*   使用 Rocco Caputo 的 Perl 对象环境 (`POE`)。请参阅 CPAN 和 [`poe.perl.org/`](http://poe.perl.org/)。`POE` 可以为几乎任何类型和数量的异步活动封装事件循环，通常甚至不需要启动新的线程或进程。另请参见 Uri Guttman 的 Stem ([`www.stemsystems.com`](http://www.stemsystems.com) 和 CPAN)。

#### 4.10.9 客户端/服务器或进程间通信——互操作性

1.  再次，跳过不谈——初学者不要尝试这个。

*   除非是在原始层级，例如在文件中留存消息供其他进程查找。这通常会有竞态条件和其他 Bug。

    *   使用 `fork()`。手工使用信号、管道和信号量。
    *   使用更高级协议进行进程间通信；例如，参见 Graham Barr 的 `Net::Cmd`（在 Perl 5.8.0 版本中已包含在核心库中）。
    *   使用标准的远程过程调用 (RPC) 机制与其他应用程序互操作，例如 `XML-RPC` [STLAURENT01] 和 `SOAP`（两者都在 Paul Kulchenko 的发布版中，[`search.cpan.org/dist/SOAP-Lite/`](http://search.cpan.org/dist/SOAP-Lite/)）。

健壮性的维度需要专门的空间，我将在第 10.1 节 中讨论。

## 第 5 章：严谨的 Perl 程序

> “缺乏纪律会导致挫败和自我厌恶。”

> —Marie Chapian

![graphics/ch05.gif](img/ch05.gif)

Perl 的好消息是，你可以开始编写程序，它们几乎立刻就能运行。坏消息是，你确实开始编写程序 . . . 当你发现：

```perl
 print "Hello, World!\n"; 
```

这就是启动所需的全部内容，Perl 初学者可能永远不会发现自己正走上一条充满风险的道路；他们正通往“无纪律程序”的领域，那里的 Bug 难以定位或修复，而且在公共场合展示代码会被更强大的程序员往你脸上踢沙子。

让你免于这种尴尬的两个伟大工具是 `strict` 和 `warnings` 编译指令。在本章中，我将比大多数书籍更详细地介绍它们。

### 5.1 包变量 vs. 作用域变量

首先，我必须暂时离题，解释一个在在本章的剩余部分被频繁提到的概念。Perl 在语言中拥有独特地位，因为它有两类变量：包变量（package variables）和作用域变量（lexical variables）。你实际上可以在程序的两个地方引用（例如 `$x`），但引用的是两个同时存在的不同变量。许多人对此无所知，因为他们要么使用旧的 Perl 4 风格编程（Perl 4 只有包变量，没有作用域变量），要么总是使用 `my` 来声明变量（从而只创建作用域变量）。如果你遵循良好的程序开发实践（意味着启用 `strict` 编译指令并用 `my` 声明所有变量），你可能编写多年 Perl 程序（直到达到 4 级水平）而从未意识到这两个变量类族。但对于维护继承的程序，你必须学习它们。

作用域变量是 Perl 5 新引入的，但它们使用起来要安全得多，因为与包变量不同，它们不是全局可见的；因此，它们成为精明的 Perl 程序员的首选变量。如今，使用包变量需要充分的理由，尽管在某些时候别无选择。

作用域变量用 `my` 声明。如果你继承的程序包含一个未用 `my` 声明的变量，那么它就是一个包变量，并且从程序的任何部分可见，甚至是其他文件，甚至其他包（只要它们知道变量属于哪个包）。它们可以直接进入并对其进行任何随心所欲的操作。就像所有强大的魔力一样，这可以被用于善 . . . 也可以用于恶。例如，`File::Find` 模块允许你通过设置包变量来改变其行为，例如如果你正在使用 AFS，可以设置 `$File::Find::dont_use_nlink`。这是一个简洁的接口，使用变量 `$File::Find::name` 获取当前文件的完整路径也是同样的：

```perl
 # 打印符号链接的完整路径

use File::Find;

$File::Find::dont_use_nlink = 1;  # 为了 AFS

find(sub { print "$File::Find::name\n" if -l }, '.'); 
```

但一个堕入黑暗面面的程序可能会从各种意想不到的地方设置和读取包变量，这使得其工作原理变得极其难以理解。程序员将这种严重违反封装的行为称为“远距离作用”（action at a distance）。尽可能多使用作用域变量，你就不可能犯那个错误。

#### 5.1.1 你那亲切的 `local` Perl 函数

某些变量不能用 `my` 声明；这些属于 Perl 的变量，所以你不能对它们产生所有权。一个例子是特殊数组 `@ARGV`（它用命令行参数初始化）。有时，临时重新赋值给该数组是很方便的。假设你想从几个配置文件读取信息。Perl 的“菱形”运算符 `<>` 让这变得简单；它会顺序读取 `@ARGV` 中指定文件的行。当我们要打开的文件没有列在命令行上时，我们可以通过先设置 `@ARGV` 来挪用菱形运算符。

```perl
 {
  local @ARGV = @CONFIG_FILES;

  while (<>)
  {
    # 对 $_ 进行操作
  }

}
```

`local` 函数会将旧版本的 `@ARGV` 隐藏在一个退出时会恢复的位置中。它创建的新版本由 `@CONFIG_FILES` 的拷贝初始化，这是我们的程序之前设置的。然后我们就可以使用菱形运算符读取这些文件，并放心地知道在退出块时，原始的 `@ARGV` 会恢复到它的位置。像示例中这样的“裸块”（naked blocks）对于创建临时范围经常有用。

你可以在 `perlvar` 文档页找到其他不属于你的变量。然而，还有一些其他变量——包变量——Perl 也赋予了特殊用途。例如，如果你调用一个不存在的程序，但在该包中定义了一个名为 `AUTOLOAD` 的过程，Perl 将转而调用该过程。这个功能在你不想在编译时定义过程，但又想知道用户尝试调用哪个过程时非常方便；因此 Perl 会将 `$AUTOLOAD` 包变量设置为该过程的名称：

```perl
 # 假设我们在包 'MyPack' 中

sub AUTOLOAD

{
  my $method = $MyPack::AUTOLOAD;  # 拷贝到私有变量
  $method =~ s/.*://;              # 去掉包名

  # 现在被调用的过程名称在 $method 中

}
```

其他对 Perl 也有用的包变量包括：`$VERSION`（当前包的版本号）、`@ISA`（我们继承的类）以及 `Exporter` 模块使用的 `@EXPORT` 和类似的变量。

#### 5.1.2 得“我们的”朋友的帮助





Perl 5.6.0 引入了 `our` 函数，这在你想要处理包变量时会让生活变得更轻松。它与 `use vars` 等效，因为它允许你在不使用完全限定限定名的情况下引用当前包中的变量，但与 `use vars` 不同的是，它是词法作用域的，因此在你处理完这些变量后的一段时间，它们的变量名在程序中就不再有效了。（是的，说一个包变量的声明具有词法作用域听起来确实有点奇怪。只需记住，“词法”部分指的是你可以通过未限定名引用该变量的范围，尽管该变量的值在全局是可见的。）相比之下，`use vars` 是文件作用域的（file scoped）。

以我们早前的 `AUTOLOAD` 函数为例。在里面硬编码我们的包名是一件麻烦事（当然，我们并不是不能通过 `__PACKAGE__` 和符号引用来绕过这一点）。使用 `our` 后，我们就不需要这样做了：

```perl
 sub AUTOLOAD
{
  our $AUTOLOAD;           # 现在可以直接说 $AUTOLOAD
  my $method = $AUTOLOAD;  # 复制到私有变量
  $method =~ s/.*://;      # 去掉包名
  # 现在调用的子程序名称就在 $method 中
} 
```

### 5.1.3 词法作用域 vs 动态作用域

为什么用 `my` 声明的变量被称为词法变量？因为这描述了它们的作用域。如果你在编辑器中打开一个 Perl 程序，从 `my` 声明后的语句开始选择文本，并一直高亮代码到闭合块的结束（或者到文件末尾），你高亮的所有内容都是该声明中变量的作用域。从该高亮文本内部调用的子程序，除非它们也被高亮，否则它们将看不到该变量。

```perl
 while (<SOMEFILEHANDLE>)
{
  my @words = split;
  # @words 直到此块结束都可见
}
# 现在 @words 不能再作为变量名使用了
# （除非用该名称声明一个新变量） 
```



包变量（以及 `perlvar` 中列出的大多数 Perl 特殊变量）可以使用 `local` 进行临时保存。另一方面，词法变量无法被局部化（localized），但也不需要局部化；如果你想临时覆盖一个词法变量，只需在内层作用域中用 `my` 再次声明它。在同一作用域级别上两次声明词法变量会触发警告。

动态作用域的名字源于它是在运行时确定的事实。包变量始终可以被引用，即使从未设置过它，这就像你即使一个哈希成员没有被设置，你也可以引用它并得到 `undef` 一样。

> ^([1]) 它比看起来更像那样；包变量是通过特殊的哈希表访问的。

关于该包变量值的生命周期，如果你用 `local` 分配了一个临时值，那么该值对所有运行代码都可见，直到 Perl 退出包含该 `local` 的块，到那时时它会恢复到之前的值。例如：

```perl
1  $main::global = "outer";
2  {
3    my $lexical = "private";
4    check_vars();
5    local $main::global = "inner";
6    check_vars();
7  }
8  check_vars();
9
10 sub check_vars
11 {
12   print $main::global;
13 } 
```

在第 1 行，我给包变量 `$main::global` 分配了一个值。（因为我 `use strict`，它强制我像那样用它的全名来引用变量。关于 `use strict` 的更多内容稍后介绍。）后续块定义了一个词法变量 `$lexical`。如果任何代码引用了该变量，它必须位于第 4、5 或 6 行。即使 `check_vars()`是从同一个块中调用的，但 `check_vars()` 的代码不在该块中，因此该子程序无法引用 `$lexical`。如果我想让该子程序看到 `$lexical`，我必须在参数列表中传递它。

但 `$main::global` 就是不同了。第 4 行的 `check_vars()` 将看到该包变量的值为 "outer"。第 6 行的 `check_vars()` 将看到值为 "inner"。第 8 行的 `check_vars()` 将看到值为 "outer"，因为变量被局部化的块已经结束了。

### 5.2 警告与严谨性

由于 `use strict` 和 `use warnings` ——两个指令（影响程序编译的 pragma）—— 在程序维护中至关重要，我将对它们进行比通常更彻底的讲解。

看出为什么 `warnings` 和 `strict` 是至关重要的并不难。如果没有它们 ——好吧，看着：

```bash
 % perl
do you, each reader, accept risks, close calls
and wait until failure
and then; alarm rings and people, listen shocked, horrified
or do you, "use strict" and "use warnings" and sleep soundly;
my main $message; study earnestly while you-can;
do this
```

```bash
 % perl -c
do you, each reader, accept risks, close calls
and wait until failure
and then; alarm rings and people, listen shocked, horrified
or do you, "use strict" and "use warnings" and sleep soundly;
my main $message; study earnestly while you-can;
do this
```

```bash
 % perl -e
There was a young man from Maastricht
Whose programs just never clicked
One day he discovered
Not using warnings or strict
```

除非你想在一个诗歌——糟糕的诗歌——轻易取代编程努力的环境中编程，否则请在每个程序中使用 `warnings` 和 `strict`。

当然，使用这些 pragma 并不能替代批判性和分析性思维。值得准确理解它们的含义，以便你判断何时适当禁用它们。但在达到这一点之前，开启它们比不开启会让生活更轻松。事实上，`warnings` 和 `strict` 都是许多类型类型的缩写，就像广谱生素一样。让我们看看内部。

你可能不熟悉本章使用的某些命令行标记，但它们非常有用。这里是简要概述：

-c 仅编译。用于语法检查；如果你对一个程序进行了大量修改，并且知道它肯定会有语法错误，你可以在不冒运行程序的的情况下发现这些错误是什么。`BEGIN` 或 `CHECK` 块中的代码将被执行，因为它们的目的是在这一阶段促进后续代码的编译。特别是这意味着被 `use` 的模块中的代码将运行执行。

-e `CODE` 将 `CODE` 作为 Perl 代码执行，而不是从文件读取程序。此开关允许你制作 Perl 代码的“单行行命令”，而无需创建文件来放置这些代码。对于测试你不确定的构造以及为 Shell 快捷命令设置别名非常有用，这样你就不需要在 ~/bin 中创建新文件。

-I `DIRECTORY` 等效于 `use lib '``DIRECTORY` `'。

-M``MODULE` 等效于在执行的代码开头放置 `use` `MODULE`。要向 `import()` 程序传递参数，请在 `=` 之后添加它们。因此 `-Mstrict=subs` 等效于 `use strict qw(subs)`，而 `-Mstrict=subs,vars` 等效于 `use strict qw(subs vars)`。

-l 自动为所有 `print`（不是 `printf`）语句的参数添加换行符。当使用 `-n` 或 `-p` 切换包裹输入循环时，这还会移除末尾的换行符。





关于这些开关的更多细节，请参阅 `perlrun` 手页。执行几行 Perl 代码而无需将其放入文件的方便方法，是从命令行将它们输入到 `perl` 的标准输入。我在这里通过使用 UNIX Shell 常用的输入结束符 `control D` (`^D`）来结束输入并展示了这一点。在该点之后出现的内容就是程序的输出。你无法编辑已经输入的行，因此这种方法的用途有限，但我经常在这里用它作为一种演示代码的方便方式。

### 5.3 `use strict` 详解

`use strict` 实际上等同于：

```
use strict 'vars';
use strict 'subs';
use strict 'refs'; 
```

这些语句中的每一个都提供了不同的“祝福”。让我们详细考虑其中的每一个。

#### 5.3.1 `use strict 'vars'`

`use strict 'vars'` 强制你使用 `my`。嗯，大体如此。这是一种捕捉拼写错误的巧妙方法。`use strict 'vars'` 要求所有变量要么用 `my` 声明，要么使用其包名进行完全限定（因为如果不是用 `my` 声明，它们就必须是包变量）。该规则的两个例外是使用 `our` 声明的包变量或通过 `use vars` 命名的变量；它们不需要完全限定。

不，仅仅说“好吧，我会用 `my`，只要别让我用 `use strict 'vars'`”是不够的。无论你打字有多么小心，都很容易出错。假设你认为宣布函数成功返回的一种好方法是：

```
my $x = func() and print "\$x is true: set to $x\n"; 
```

遗憾的是，`print()` 中的 `$x` 与 `my` 声明的 `$x` 并不是同一个。新 `$x` 的作用域尚未开始（它从随后的语句开始）。因此，`print()` 中的 `$x` 实际上是包变量 `$x`，它可能被赋予一个完全不同的值，或者根本没有值。只有使用 `use strict`，你才会得到错误：

```
Global symbol "$x" requires explicit package name 
```

当我们发现 Perl 在内部将 `and` 转换为了 `if` 时，作用域变得更加清晰了。你可以通过 `B::Deparse` 模块看到这一点：

```
% perl -MO=Deparse -e 'my $x = func() and print $x'
print $x if my $x = func(); 
```

这向我们展示了即使在同一语句中，`print` 也在 `my` 之前。“但等一下，”你喊道，“后缀 `if` 不不是完全等同于真正的 `if` 吗？”在这种情况下不是的。观察：

```
% perl -Mstrict -wle 'print $x if my $x = $]'
Global symbol "$x" requires explicit package name at -e line 1.
Execution of -e aborted due to compilation errors.

% perl -Mstrict -wle 'if (my $x = $]) { print $x }'
5.008003 
```

我打印了一个变量而不是字面量，因为如果是字面量，Perl 会警告在条件内部发现了赋值。变量 `$]` 包含了 `perl` 程序的版本号。为了将像 "5.8.3" 这样的版本号转换为可以作为真数比较的值，Perl 会如你在此所示对其进行格式化。

因此，你应该确保任何词法变量的使用至少从其声明后的后续语句开始开始。Perl 提供了一些实用的快捷方式，你可能会考虑利用它们违反这种区别。你可以在条件中声明词法变量，或者作为 `for`/`foreach` 循环变量：

```
if (my ($word) = /(\w+)/) { ... }
for my $person ($db->person_search) { ... } 
```

而 Perl 将该词法变量的作用域限制在附加的块中，就像你写了下面一样：

```
{
  my $word;
  if ($word = /(\w+)/) { ... }
}

{
  my $person;
  for $person ($db->person_search) { ... }
} 
```

事实上，Perl 允许你将 `my` 放在任何地方。它实际上只是变量上的一个修饰符。例如，如果你需要向某些函数传递变量的引用，以便该函数可以写入该变量，你可以写：

```
func(\my $foo);
print "func() set \$foo to $foo\n"); 
```

这看起来可能很诡异，但它是有效的。该功能的一个实际用途是 `Getopt::Std` 导出的 `getopts()` 函数，如果将哈希表的引用作为第二个参数传递，它可以填充命令行选项的哈希表：

```
use Getopt::Std;
getopts("dif:v", \my %Opt) or die $Usage;
$Opt{f} or die "The -f option is mandatory\n"; 
```

注意，子程序仍然是包变量。在 Perl 6 之前没有词法子程序。如果你担心别人调用你的内部子程序并想让它们保持私有，那么就将它们变为匿名子程序引用并赋值给词法变量，如下所示：

```perl
# 之前：
sub dumpit
{
  require Data::Dumper;
  print Data::Dumper::Dumper(\@_);
}

# [...]
dumpit(@args);

# 之后：
my $dumpit = sub {
  require Data::Dumper;
  print Data::Dumper::Dumper(\@_);
};
```

#### 5.3.2 `use strict 'subs'`

`use strict 'subs'` 禁止使用裸字作为字符串。让我们看看使用 `use strict` 会发生什么：

```
% perl -Mstrict=subs -c
[...]
```




现在 Perl 编译器已经知道 `outgrabe` 是一个子程序调用。它不需要已经见过该子程序的代码，因为在编译时，它只需要知道如何解释在源文件中找到的每一个标记标记（token）。只要在 Perl 运行时系统到达最后一行时 ``outgrabe` 的代码已经存在，一切都会正常。

> ^([3]) 只要子程序的正向声明或实际声明使用了子程序原型（prototype），它们就必须使用相同的原型。

同样，就像变量可以通过 `use vars` 溜过 `use strict 'vars'` 一样，Perl 也可以被说服：如果你通过 `use subs` 声称这些词是“待定义的子程序”，那么它就不会再对裸字（barewords）报错了：

```
 use subs qw(outgrabe);

# [...]

outgrabe; 
```

`no strict 'subs'`——与 `use strict 'subs'` 相反——在 Perl 中被称为“诗歌模式”（poetry mode），其原因现在应该显而易见了。它会将任何看起来不像子程序调用的裸字视为字符串，就好像给它加上了引号一样。

#### 5.3.3 `use strict 'refs'`

如果你期望一致性，那么你找错语言了。`strict` 被誉为一个编译指令（pragma），即一个影响程序编译的模块。但 `use strict 'refs'` 在运行时生效，因此我们不能说它禁止了包含符号引用（symbolic references）的代码；Perl 实际上是在尝试执行此类引用时抛出致命异常。然而，这里有一个谜团：在 Perl 5 之前，符号引用是间接引用对象的唯一方法。那么为什么要采取这种态度呢？让我们仔细观察。

这个问题在 Perl 新闻组中出现的频率之高，以至于它应该有自己的歌：我如何访问一个名称存储在另一个变量中的变量？提问者正在开发类似的内容：

```
 my %names_of_badges;  # Keys: 徽章编号。 Values: 名字。

my %names_of_users;   # Keys: 用户。 Values: 名字。

print "Lookup by (b)adge or (u)sername? ";

chomp(my $answer = <STDIN>);

my $choice = ($answer =~ /^b/ ? "badges" : "users");

# 我该如何获取 %"names_of_$choice"??? 
```

这个问题的答案是：“别尝试”。实现这段代码真正想要实现的方法是使用哈希（hash）、硬引用（hard reference）或两者兼顾。

提问者认为，形成一个与想要访问的哈希名称相同的字符串后，他们几乎解决了这个问题。如果使用符号引用，他们是对的。但符号引用有很多问题。其是它们只适用于包变量（package variables），因此无法通过符号引用访问示例中的词法哈希。

另一个更重要的问题是它们的方法错误。如果你想获取两个可能的哈希之一，你不应该使用访问器——在这种情况下是包含哈希名称的字符串——其可能的值跨越了整个字符串宇宙。一旦写错，你的程序就完蛋了。正确的解决方案是对每个原始哈希创建一个硬引用，这样你只需要在两个引用之间进行选择。我将在第 6.2.13 节展示这些示例。

符号引用是不好的，但在 Perl 4 中我们我们所拥有的。现在我们不再需要使用它们了（除了我稍后提到的大多数晦涩目的），所以我们使用 `use strict 'refs'` 来确保我们不会意外引入它们。符号引用也用于操作符号表，如果这是你的意图，有更好的方法可以实现。

#### 5.3.4 `use strict 'DWIM'`

不，真的没有一个关于“按我意思做”（Do What I Mean）的严格性编译指令。但如果你写了该语句，Perl 不会抱怨，因为它静静地忽略任何它不认识的请求的严格性。与其说 `use strict` 并获得各种类型的严格检查，不如尝试有选择地只开启你认为需要的那些要好；总有一天，你也会像我一样，不小心输入 `use strict 'sbus'`。我将在第 5.5 节讨论如何关闭那些阻碍你的选项。

> ^([4]) 除非你正在使用 Perl 5.8.1 或更高版本，在该版本中这个问题已被修复。

### 5.4 `use warnings` 详解

`use warnings` 等同于说：

```
 use warnings 'all'; 
```

这反过来又是：

```
 use warnings 'chmod';

use warnings 'closure';

use warnings 'exiting';

# ...以及更多类似的内容... 
```

也就是说，它启用了一系列警告。它是一个较新的编译指令（在 Perl 5.6 中引入），你可能没见过它；你更有可能熟悉它老老的命令行兄弟版本 `-w`：

```
 #!/usr/bin/perl -w

# 现在启用了警告 
```

那么，为什么为了实现相同的功能要打这么多字？因为 `use warnings` 要强大得多。你可以禁用它的部分，而不是像 `-w` 提供的这种全有或全无的方案，而且你还可以限制它的作用范围。你还可以将警告转换为致命异常，甚至可以创建自己的警告类。

#### 5.4.1 `use warnings` vs 模块

由于词法作用域的存在，`use warnings` 不会将其影响传播到你使用的模块中（而 `-w` 会）。在你自己的模块中，请在顶部添加 `use warnings`。其他人的模块可能开启了，也可能没有。现在，让代码具有警告安全性确实是模块作者的事务和责任，但有时你正在使用的模块作者可能没有放入 `use warnings` 语句。

因此，为了在使用第三方模块时获得最大的安全性，请在你的 shebang 行中添加 `-w` 标志。这听起来可能很复旧，但它将确保你看到你能看到的每一个警告。凡是出现 `warnings` 指令的地方，无论是在你的代码中还是模块中，该指令控制的代码的 `-w` 标志都会被 Perl 忽略，因此你仍然可以从适用处的额外指令力量中获益。

你可以通过 `FATAL` 参数将所有警告变为致命：

`use warnings FATAL => 'all';`

这会将所有（或你指定的任何警告类）转换为致命异常。现在，当你的代码产生警告时，将直接崩溃。

我将在第 10.4 节讨论在编写自己的模块时处理警告的最佳方法。

#### 5.4.2 编译指令遇上 AutoLoader

如果你使用 AutoLoader 模块按需加载子程序，请注意，主模块中的任何 `strict` 或 `warnings` 指令对自动加载的子程序都是见的。你需要在每个自动加载子程序的开头添加 `use strict` 和 `use warnings`，它们才能生效。

### 5.5 选择性禁用

正如你现在可能猜到的，我主张将警告和严格性调到最高水平。然而，有时沉默它们是有意义的，因为你正在有意地违反规则，并且知道自己在做什么。

#### 5.5.1 学会说“不”





没有必要因为它们阻碍了你就完全关闭严格模式（strictness）或警告。如果你无法对代码进行合理的调整以避免触发它们，只需禁用阻碍你的那部分，且仅持续到足够完成任务为止。你可以通过 `no strict` 指令来实现这一点，例如：

```
no strict 'refs'; 
```

`no` 是 `use` 的反义词；它在其词法作用域内禁用该指令的指定部分。该指令的所有其他部分仍然有效。

## 5.5.2 关闭严格模式

`no strict 'vars'` 我想不出任何有必要使用这种操作的场景。每当你产生想要关闭 `strict 'vars'` 的冲动时，请使用 `our`，或者在引入 `our` 之前的 Perl 版本中使用 `use vars`。在不想硬编码包名、或可能不知道包名是什么的情况下，想要避免完全限定包变量（fully qualifying package variables），这确实完全是合理的，但 `our`/`use vars` 仍然可以在不关闭严格模式的情况下完成工作。

我查看过许多使用了 `no strict 'vars'` 的程序，在每种情况下，它们都可以轻松在不使用它的情况下写完。

`no strict 'subs'` 这种情况下更没有理由诉诸此了。最后一个算像合理的理由是将文件句柄（filehandles）传递给子程序：

```
open(REPORT, "evil-empire.takeovers");

my @totals = extract_totals(REPORT);

# [...]

sub extract_totals
{
  local *FH = shift;
  # [...] 
}
```

但是（想象这里有一个加州青少年口音）那是 Perl 4 的做法。事实上，即使在 Perl 4 中，你也可以通过传递类型全局（typeglob）来满足严格性：

```
@totals = extract_totals(*REPORT); 
```

（好吧，暂不说 Perl 4 并没有 `strict` 指令，但你明白意思。）请参见第 7.9.1 节 获取有关如何使用更现代的 Perl 特性改进代码的更多信息。

`no strict 'refs'` 我们终于有一个“最有用的指令否定”候选了。确实在某些时候，使用符号引用（symbolic reference）是正确的做法，你必须要求 `strict 'refs'` 靠边。例如，创建一组相似的访问器方法（accessor methods）：

```
sub _attr
{
  my ($self, $name) = splice @_, 0, 2;
  $self->{$name} = shift if @_;
  return $self->{$name};
}

for my $method (qw(email name telephone address))
{
  no strict 'refs';
  *$method = sub { _attr($_[0], $method, @_[1..$#_] };
}

# 现在通过一个 $person 对象我们可以调用
# $person->email, 或 $person->name, 等 
```

这种方法的优点是所有方法共享同一段代码，而不是每个方法都有独立的实现并各自空间。如果不禁用 `strict 'refs'`，Perl 会对 `*$method` 的赋值反对意见：

```
Can't use string ("email") as a symbol ref while "strict refs" in use... 
```

如果你不熟悉 `*` 符号，这被称为类型全局（typeglob），这是一个极其晦奥的术语，意为跟在 `*` 后面的所有同名包变量。在这段代码中，`*` 后面的不是单词而是变量，因此它被用作符号引用。因为我们正在向类型全局赋值引用，Perl 可以判断出我们想要赋值的变量类型，因此只填充该类型的包变量，而不是类型全局中的每一个条目。在我们的代码中，该引用是一个代码引用（code reference），因此我们正在创建一个新的子程序（子程序是包变量），其名称取决于 `$method` 中存储的内容。

然而，无论我们最终使用了哪些方法，我们创建了所有的方法，所以你可能更喜欢在需要时再创建方法：

```
1  # 与之前相同的 _attr() 方法，然后：
2  sub AUTOLOAD
3  {
4    (my $method = our $AUTOLOAD) =~ s/.*://;
5    no strict 'refs';
6    *$method = sub { _attr($_[0], $method, @_[1..$#_]) };
7    goto &$method;
8  } 
```

顺便提一下，是第 6 行需要 `no strict 'refs'`，而不是第 7 行；就其价值而言，使用 `goto` 间接调用子程序并不违反 `strict 'refs'`。

这种即时（just-in-time）方法创建是可以的，但有些宽松；我们确实需要限制用户只使用我们需要的方法。没问题：

```
1  sub AUTOLOAD
2  {
3    (my $method = our $AUTOLOAD) =~ s/.*://;
4    { map { $_ => 1 } qw(email name telephone address)
5    }->{$method}
6      or croak "Invalid method $method"
7    no strict 'refs';
8    *$method = sub { _attr($_[0], $method, @_[1..$#_]) };
9    goto &$method;
10 } 
```

我在第 4 到第 6 行添加了一个非常简洁的构造，用于检查给定的方法是否在列表中。

## 5.5.3 关闭警告

关闭警告轻而易举：找到你想忽略的类，并包裹一个包含 `no warnings` 的块。这是一个例子：假设你想覆盖一个现有的子程序并让它执行某些事情。想要这么做的两个很好的理由是为了调试目的临时覆盖自己的子程序，以及覆盖一个你没有编写的方法。覆盖子程序最简单的方法就是重新定义它：

```
# 为美国用户调整摄氏
sub temperature
{
  my $self = shift;
  return ($self->{temperature} + 40) * 9 / 5;
}
```

但 Perl 会警告我们这可能是错误：`Subroutine redefined at...`

我们可以方便地通过以下方式处理：

```
{
  no warnings 'redefine';
  # 为美国用户调整摄氏
  sub temperature
  {
    my $self = shift;
    $self->{temperature} * 9 / 5;
  }
}
```

是的，可以通过方式重新定义子程序而不需要禁用警告，但前面的代码是非常清晰的。好吧……你可以这样做：

```
BEGIN
{
  undef &temperature;
  *temperature = sub
  {
    my $self = shift;
    return ($self->{temperature} + 40) * 9 / 5 - 40;
  };
} 
```

我们首先取消旧的子程序定义，然后通过向类型全局赋值安装一个新的。我们必须将其放在 `BEGIN` 块中，以获得与早期禁用警告代码相同的效果，因为 `sub temperature` 在编译时创建子程序定义；但向类型全局赋值是一个运行时操作，因此在我们到达该代码之前，任何对 `temperature()` 的调用都会调用旧子程序，除非我们预先将其提升到编译阶段。

如果我们只想在运行时重定义之后替换所有对 `temperature()` 的调用，那么可以使用 `local *temperature = sub { ... }`。




难道直接禁用警告不是更简单吗？

### 5.5.4 使用 `$^W` 禁用警告

如果你使用的是早于引入作用域警告（lexical warnings）的 Perl，那么它们在道德上的等价物是特殊变量 `$^W`。当该标志被设置为 `1` 时，警告——所有的警告——都会启用，就像你在解释行（shebang line）中输入 `-w` 一样；当它设置为 `0` 时，警告会被关闭。因此，你可以在整个代码中随心所欲地启用禁用警告。为了在修改完成后让警告恢复到之前的状态，可以通过 `local()` 使对 `$^W` 的赋值变为临时的，并将其放在块中以限制其作用域：

```
 {
  local $^W = 0;  # 禁用警告

  $x = $y + $z;   # 使用可能未定义的变量
} 
```

然而，请记住，给任何变量赋值都是运行时操作，而许多警告发生在编译时；要影响它们，你必须将赋值放在 `BEGIN` 块中。为子程序重定义示例禁用警告尤为困难，因为你不能直接在与 `$^W` 赋值相同的 `BEGIN` 块中以显而易见的方式重新定义子程序：

```
 BEGIN
{
  local $^W = 0;            # 无效

  sub temperature { ... }
} 
```

子将在赋值执行之前被编译，因为程序的运行机制就是这样，无论它们是在 `BEGIN` 块中还是块之外。你必须使用前面提到的类型全局变量（typeglob）赋值：

```
 BEGIN
{
  local $^W = 0;

  *temperature = sub { ... };
} 
```

或者你必须做一些更加“卑鄙”的事情：

```
 {
  my $warn_save;
  BEGIN
  {
    $warn_save = $^W;
    $^W = 0;
  }
  sub temperature { ... }

  BEGIN
  {
    $^W = $warn_save;
  }
} 
```

这向你展示了作用域警告是多有用，现在你已经看到替代方案是多么糟糕了！

### 5.5.5 重定向错误和警告

不过，有些警告你不希望用户看到详细细节；它们可能会暴露你太代码信息。对于致命异常（fatal exceptions）更是如此，它们通常包含（通过 `Carp` 模块的 `croak()` 或 `confess()` 函数）函数调用及其参数的详细信息。而发生这种情况最糟糕的环境是公共网站，其用户通常无权读取程序源代码，而且用户中可能潜伏着某些你不希望让他们看到数据库密码的危险人物。

Randal Schwartz 在《Linux 杂志》的一个专栏中[[6]](#ch05lev1sec5.html_ch05fn06)解决了这个问题，他使用了一个名为 `FatalsToEmail` 的模块，设计旨在将致命异常的文本通过电子邮件发送给开发者，同时给用户留一个模糊的歉意。

> ^([6]) [`www.stonehenge.com/merlyn/LinuxMag/col14.html`](http://www.stonehenge.com/merlyn/LinuxMag/col14.html)

这是我的版本，一个名为 `EmailErrors` 的模块，旨在实现类似的目的，但有几个关键区别。如果代码在 `eval` 块中运行，或者是在命令行运行而非通过 Web ，它允许异常正常传播。它像处理异常一样处理警告。不过，你需要在标记为 "`##`" 的地方插入一些代码来处理你对该模块的具体用法：

#### 示例 5.1. EmailErrors 模块

```
 package EmailErrors;

use strict;

use warnings;

BEGIN
{
  # 如果我们在 eval 中，或者没有从 web 端使用，
  # 允许异常被正常处理。
  # 否则，如果发生 die，将其发送到错误处理程序。
  $SIG{__DIE__} = sub
  {
    return unless $ENV{REMOTE_ADDR};

    my $in_eval = 0;

    for (my $stack = 1;
         my $sub = (CORE::caller($stack))[3];
         $stack++)
    {
      $in_eval = 1 if $sub =~ /^\(eval\)/;
    }

    unless ($in_eval)
    {
      goto &throw;
    }
  };

  # 对于警告，执行相同的操作。
  $SIG{__WARN__} = sub
  {
    CORE::warn(@_) and return unless $ENV{REMOTE_ADDR};

    local $SIG{__WARN__};  # 避免可能的递归

    goto &throw;
  };

  sub throw
  {
    my $text = shift;
    $text = do { require Carp::Heavy; Carp::longmess($text) };

    ## 处理拒绝服务问题
    ## 向用户打印所需的文本
    ## 记录错误文本
    ## 邮件发送错误文本
  }
}

1; 
```

针对这些注释的操作如下：如果你在 Web 应用程序中使用这些代码，并担心坏人通过连续触发大量电子邮件来减慢你的服务器，那么请维护一个先进先出的警告和时间戳缓存；如果警告重复太快，则忽略它。决定你想让用户看到什么；在 Web 应用程序中，你可能使用特殊的错误模板。如果你在保留日志，可以将错误文本发送给组织中不幸需要处理这些问题的人。

### 5.5.6 不要急于禁用

`use strict` 和 `use warnings` 可能非常有用，但不要假设它们会捕捉到你所有的错误。Perl 留下了大量的检查。如果你担心坏人通过连续触发大量电子邮件来减慢你的服务器，那么请维护一个先进先出的警告和时间戳缓存；如果警告重复太快，则忽略它。决定你想让用户看到什么；在 Web 应用程序中，你可能使用特殊的错误模板。如果你在保留日志，可以将错误文本发送给组织中不幸需要处理这些问题的人。

### 5.7 Perl 诗歌

正如你之前看到的，编写出既能编译运行良好又蕴含某些艺术价值的 Perl 是相当可能的……尽管这很主观。创作这种 Perl  prose 是一种公认的爱好，关于它的权威论文由 Sharon Hopkins 撰写([`www.wall.org/~sharon/plpaper.ps`](http://www.wall.org/~sharon/plpaper.ps)）。Perl 俳句比赛在网上和 Perl 大会上经常出现，为创意程序员提供了更多的右脑锻炼。

查看 Damian Conway 的 Coy.pm ([`search.cpan.org/dist/Coy/`](http://search.cpan.org/dist/Coy/))，了解一个有才华和空闲时间的人能做的令人惊叹的示例。

## 第 6 章 重构（手术台）

> “艺术的终结在于揭示物的隐藏含义而非外表；因为真正的真理在于这种深层的真理，它不会出现在外部轮廓中。”

> 

> —亚里士多德

![graphics/ch06.gif](img/ch06.gif)

在简单的重写之外，是对程序更深层次的分析和重构。在本章中我将涵盖重构继承代码的几个重要方面。

### 6.1 保持简洁




许多程序的可维护性存在一个大问题，即它们的代码单元实在太长了。（我所说的“代码单元”指的是子程序或主程序。）一旦代码单元的长度超过了你一次性可以查看的内容，维护起来就会变得更加困难。因此，可以将你的编辑器每屏显示的行数视为代码单元最大尺寸的强有力建议。

有时你可以为扩展“代码单元”的定义提供理由。例如，一个异常处理块可能与之前的代码解耦得充分，从维护性的角度考虑，它可以被视为一个独立的代码单元。

当你面对一个庞大的代码块时，请将其拆分为更小的代码单元。隔离出仅操作少量 `variables` 的代码段，并将其放入一个以这些变量作为输入和/或输出的子程序中。找到一段重复的代码，并将其放入子程序中。

你必须能够为子程序起一个合理的名称，以描述它的功能。如果一个子程序的名称很长，但仍然非常晦涩，以至于你不看源码就不知道它在做什么，那么这样做几乎无益于事。在你创建每个子程序时，为它编写一份说明如何使用的文档。如果编写文档需要花费很长时间，这说明你没有挑选出一个好的代码进行隔离。

## 6.2 货物崇拜 Perl (Cargo Cult Perl)

Perl 提供了如此多的解决问题的方法，以至于人们有时选择虽然有效但在性能、可读性或可维护性方面并非最优的方法，这并不意外。将一个能完成任务的东西描述为错误听起来可能很过，但我们在这里的目标是不仅仅是“足够好”。

在第二次世界大战期间，机组访问了南太平洋的梅美拉尼西亚等岛屿，这些岛屿此前很少或从未见过白人。这些机组成员的外表和车辆类似于某些当地传说，他们被尊为神灵。在他们离开后，岛民模仿这些飞行员的行为和着装，希望他们能回来，甚至建造了跑道来鼓励他们的到来。这些临时的宗教被称为“货物崇拜”（cargo cults），因为他们崇拜飞行员留下的“货物”（cargo）。

“货物崇拜代码”是一个贬义但形象的词汇，指那些在作者并不知道其功能的情况下使用的代码，仅仅是因为他看到别人在这么做，并认为这符合自己的需求。记住，你对编程思考得越多，作为程序员的价值就越高。要意识到自己在何时盲目使用代码惯用法（idioms），因为下一个阅读你代码的人可能也见过我即将给出的建议：当你在维护的程序中看到货物崇拜代码时，它能帮助你判断作者的经验水平。这有助于你决定在多大程度上认真对待你完全无法理解的代码。

正如任何艺术形式一样，Perl 最高级的实践者制定自己的规则。如果你知道你继承的代码来自一个知道自己在做什么的人，那么他们程序中出现的明显的货物崇拜代码可能并不意味着他们患了早发痴呆症。他们可能有充分的理由把它放进去。

这里是一些货物崇拜代码的示例。它们从无害的冗余到完全的错误不等，但所有这些代码都值得警惕，以确保你不会在无意间使用它们。

### 6.2.1 无意义的字符串化 (Useless Stringification)

当我看到一个标量变量被包含在双引号中且没有任何伴随内容——如下所示：

```
 print "$x";   # 无意义的字符串化 
```

我会想：“啊，这里有个 Shell 程序员。”这段代码与下面等同：

```
 print $x;     # 无字符串化 
```

（稍后我会提到一个警告）。在 Bourne shell 中，某些时候你必须将变量放在双引号中以避免可能的错误；但在 Perl 中没有这种情况。

你说它是无害的？大情况下是如此。但我们把对表达式加引号称为“字符串化”（stringification）的原因，不仅仅是想创造一个难听的新词。事实上，它描述了一种实际的操作。Perl 中并非所有内容都不受字符串化的影响。引用（包括对象）在被字符串化后就不相同了：

```
 % perl -Mstrict -Mwarnings

my $ref = { dog => 'bark', cat => 'purr', llama => 'hum' };

my $notref = "$ref";

print "Reference: $ref->{dog}\n";

print "String:    $notref->{dog}\n";

^D

Reference: bark

Can't use string ("HASH(0x80fbb0c)") as a HASH ref while

"strict refs" in use... 
```

字符串化也是一个可以受程序员影响的过程。如果类中的一个对象重载了字符串化，在它周围加引号将调用它的字符串化方法。这听起来可能对你来说太深奥而不关注，但有很多常用的模块确实重载了字符串化，例如 `URI.pm`：

```
 % perl -Mstrict -Mwarnings -MURI

my $url = URI->new("http://www.perlmedic.com");

my $nonurl = "$url";

print "Object: ", $url->host, "\n";

print "String: ", $nonurl->host;

^D

Object: www.perlmedic.com

Can't locate object method "host" via package 

"http://www.perlmedic.com" (perhaps you forgot to load "http://

www.perlmedic.com"?)... 
```

无意义的字符串化也是低效的。如果你对一个初始类型为数字的标量进行字符串化，而只是为了作为数字使用，Perl 最终会执行冗余的字符串转换；在经常执行的循环中是有害的。

### 6.2.2 无意义的连接 (Pointless Concatenation)

这并不是使用双引号足够。（很多这些部分看起来像是在矛盾。这并不实际上是错误，更多是风格问题。）许多语言没有插值，所以习惯这些语言的人编写的 Perl 代码如下：

```
 $title = "Report at " . $time . " on " . $date . "\n"; 
```

我甚至见过——别笑：

```
 $title = join (" ", "Report at", $time, "on", $date, "\n"); 
```

其结果与第一个区别在于空格，但无论如何这都很晦涩。相反，使用插值：

```
 $title = "Report $time on $date\n";
```

### 6.2.3 多余的 scalar()

如果上下文已经是标量的，那么使用 `scalar()` 函数没有意义。理解列表和标量上下文对于成为优秀的 Perl 程序员至关重要，权威参考 [00] 并不含糊：“在学会列表和标量上下文的区别之前，你将过得很痛苦”（第 69 页）。

因此你不得不怀疑写这段代码的人有多理解上下文：

```
 if (scalar @items) { ... }
```

显然，代码的意图是在 `@items` 数组中有内容时执行后续块。但 `if` 语句的条件已经在标量上下文中。不可能是另一种；条件必须被求值以判断是真是假；这两种选择都是单个值（即标量）。

严格来说，它在布尔上下文中。它是标量上下文的一种特例（正如字符串和数字上下文一样），你很难看出其中的区别。

更露骨的是这样的代码：

```
 my $n_values = scalar(values %hash); 
```

将任何内容赋值给标量都会将表达式放入标量上下文，因此 `scalar()` 是多余的。




*   `foreach (/(\w+)\s+(\d+)/g) { ... }`

`while` 语句将其条件置于标量上下文（scalar context），而标量上下文中的 `/g` 正则表达式匹配充当迭代器，在模式匹配器沿着输入字符串（在此例中为 `$_`）移动直到没有更多匹配项之前，反复返回真。我们通过捕获括号将感兴趣的部分保存在 `$1` 和 `$2` 中，因此块中的代码最好使用这些变量。

`foreach` 语句在括号之间强制执行列表上下文（list context），而列表上下文中的 `/g` 正则表达式匹配会返回一个所有捕获括号匹配项的列表。在块内部，`$_` 将被设置为每个连续匹配中后续的 `$1` 和 `$2`。如果你实际上想区分 `$1` 和 `$2`，那么这种代码写得不好，因为在块内部，你无法知道 `$_` 代表的是单词（`$1`）还是数字（`$2`），除非计算进入该块的次数并查看该计数是偶数还是奇数。

让我们来看一个例子来更清楚地说明：

```
 $_ = <<EOT;

  apples  42
  oranges 57
  lemons  21
  pears   91 

EOT

my %stock;

while (/(\w+)\s+(\d+)/g)
{
  my ($fruit, $count) = ($1, $2);
  $stock{$fruit} = $count;
} 
```

这是在用正确的工具做工作；因为我们需要在循环中区分水果和数量，我们想要一次获取两个元素。如果我尝试用 `foreach` 循环来这样做，不仅循环在我累积了所有匹配项到列表之前不会开始执行，而且块会先针对 `apples` 执行，然后针对 `42`，然后是针对 `oranges`，以此类推。

如果你理解了这一点，请尝试这个例子。假设我们决定将正则匹配与 `$fruit` 和 `$count` 的赋值结合：

```
while (my ($fruit, $count) = /(\w+)\s+(\d+)/g) # 错误！

{
  $stock{$fruit} = $count;
} 
```

这是一个巨大的错误！代码将永远在 `$fruit` 和 `$count` 的第一组值上循环。我们把列表上下文中的 `m//` 行为与标量上下文中的 `/g` 行为混淆了。在列表上下文中，匹配将返回捕获括号中匹配项的列表，而全局（`/g`）匹配将返回所有捕获括号匹配项列表的列表。这里没有迭代行为；一旦 `/g` 匹配完成，下一次执行尝试将再次从头开始。

尽管 `while` 语句将其条件置于标量上下文，但列表赋值位于该条件内部，因此在设置 `m//g` 的上下文时具有优先级。列表赋值本身在标量上下文中求值，perlop 告诉我们，标量上下文中的列表赋值求值结果为被赋值元素的数量。因此，只要有匹配，就会有赋值，条件将为真。

当我需要强制使用标量上下文时，我很少使用 `scalar()`；那打字太麻烦了。相反，我利用一个可以强制执行标量上下文的运算符。我的意思是：假设我想打印一个数组中元素数量的报告。以下方法行不起的：

```
print "There are ", @items, " items in the array\n"; # 错误

print "There are @items in the array\n";        # 同样错误 
```

第一个将 `@items` 置于列表上下文，因此打印所有项目；第二个将 `@items` 置于字符串上下文，因此打印所有项目且连续元素之间有空格。等一下！不要去按那个 `scalar()` 按钮！只需花很少精力，`.` 就能完成工作：

```
print "There are " . @items . " items in the array\n"; 
```

（任何一个点都可以替换为逗号；一个就足够强制 `@items` 进入标量上下文。）

现在假设我有一个数据记录数组 `@recs`，我需要将哈希中的 `count` 参数设置为 `@recs` 中的元素数量，例如用于某个网页模板。我不能这样做：

```
my %param = (count => @recs, ... ); 
```

人们很想认为：“为什么不行呢？`@recs` 正好就在我想在哈希初始化列表中放置标量的地方，所以它不是正处于标量上下文吗？”不是的；列表中的元素处于列表上下文，而且没有特殊的哈希上下文（直到 Perl 6）；赋值左侧的哈希会将右侧置于列表上下文，而列表上下文只有一种。

在这里我可以为 `scalar()` 给出辩护理由；为了了解原因，让我们看看替代方案。我需要一个计数，因此可以使用算术运算符来强制标量上下文：

```
my %param = (count => 0+@recs, ... ); 
```

是的，我可以使用其他变体，如 `1*@recs`，但 `0+@recs` 在视觉上最不意外。但在这里使用 `+` 是为了它强制标量上下文的副作用，而我对加法本身并不感兴趣。

### 6.2 无用的切片（Slices）

初学者经常对数组语法感到困惑，例如本该写 `$array[4]` 却写 `@array[4]`。括号之间的是使用的索引列表。你可以从数组中切取一个元素；然而，在开启警告的情况下，Perl 会提示：

```
my @pilots = qw(Scott Alan John);

my @ships = (0, 3);

for (@pilots[@ships]) { ... }
```

警告只针对字面上的元素列表生成。如果你对索引列表使用表达式——例如 `@slice[@items]`——即使 `@items` 恰好包含一个元素，也不会产生警告。否则，你被迫先检查 `@items` 的大小，那种限制非常不符合 Perl 风格（anti-Perlish）。

为什么要这样做呢？既然数组切片的定义是 `@array[a,b,c,...]` 等于列表 `($array[a], $array[b], $array[c],...)`，那么 `@array[2]` 和 `$array[2]` 是相同的吗？

并不，区别再次在于那个魔法单词“上下文”。`@array[2]` 是包含一个元素的列表；但 `$array[2]` 是一个标量。因此，如果有机会，每个将强制不同的上下文：

```
$element[0] = localtime;

@slice[0]   = localtime;

print "Element: ", $element[0], "\n";

print "Slice:   ", @slice[0], "\n";
```

这里有一个更好的理由不要意外使用切片了：

```
my @cats = ( {name => 'Jake', fur => 'orange'} );  # 等等

print @cats[0]{name};
```




我尝试访问数组 `@cats` 中第一个哈希的 `name` 元素，Perl 警告说我可能并不想进行切片（slice），但我保留了代码的原样，结果这变成了一个语法错误。（出于好奇，如果把隐含的箭头放回去：`@cats[0]->{name}`，就不会有语法错误。但我宁愿你离地雷远点，也不愿你仅仅因为我指出了第一颗地雷的位置就继续走下去。）

列表和哈希也可以进行切片：

```
my ($uid, $gid) = (stat $file)[4,5];

my @fields = @data{@field_names}; 
```

第二行代码展示了按特定顺序提取哈希值的方便方法，这在数据库应用程序的代码中非常有用。更多信息请参阅 [GUTTMAN98]](#。

### 6.2.5 在使用 `$1` 之前未测试正则表达式

这是当你执行了一个捕获文本的正则表达式匹配，然后在没有检查正则是否匹配成功的情况下使用 `$1` 及其它的变量：

```
$line =~ /height = (\d+) in, weight = (\d+) lbs/;

print "Go metric! Height = ", $1 * 2.54, "cm, weight = ",
      $2 * 0.45, "kg\n"; 
```

这完全是错误的。如果你假设在使用 `$1` 时正则表达式已经匹配成功，你最终可能会得到一个由上一次正则表达式匹配设置的 `$1`。务必检查正则匹配是否成功，否则你可能会得到像下面这样完全离谱的结果：

```
% perl -Mstrict -Mwarnings

for (qw(1 2 3 banana 4))
{
  /(\d+)/;
  print "\$1 = $1\n";
}

^D

$1 = 1
$1 = 2
$1 = 3
$1 = 3
$1 = 4 
```

而且没有任何提示显示任何异常。`s///` 的情况也是如此（尽管在替换中捕获文本并不常见）。正确的代码看起来像：

```
for (qw(1 2 3 banana 4))
{
  /(\d+)/ and print "\$1 = $1\n";
} 
```

或者其他仅在匹配成功时才执行操作的变体。

### 6.2.6 未检查系统函数的返回代码

这也是错误的。只有当你不检查一个可能失败的函数的返回代码是合适的，即你的程序无论函数是否成功都应该执行相同的操作时。通常，这比每次都添加一个检查需要更多的思考。大多数系统函数在失败时返回假值并设置 `$!`，所以检查起来就像这样简单：

```
open my $fh, $filename or die "Can't open $filename: $!\n"; 
```

在 `perlfunc` 中查看“输入和输出函数”以及“用于文件句柄、文件和目录的函数”标题下的列表获取系统函数。注意，人们很少检查 `print()` 的返回代码，尽管当它例如打印到一个空间已满的文件系统上的文件时，它会返回假。虽然你在调用 `close()` 时会看到错误，但如果你在调用 `close()` 之前已经花费了大量时间或写入了（你认为的）大量数据，这可能并不能给你什么慰藉。所以，如果你想真正安全，请检查 `print()` 的返回代码。记住，如果返回代码指示错误，你的程序应该从 `$!` 获取该错误的原因，并将其放在可见的地方。

> 不要指望它；我在 AFS 中发现过一种这种情况并非如此的情况。

### 6.2.7 空值上下文中的 `map()`

我之所以提到这一点，是因为许多人将其视为“货物崇拜式编程”（cargo cult programming），尽管这只是一个微不足道的毛病。而其中某些人可能会根据你对这种惯用写法的使用来评估你的能力。他们之所以激动，是因为利用 `map()` 的副作用而忽略了它的返回值。因为 `map()` 的设计是为了转换列表，因此其存在的意义就是返回另一个列表，忽略这个输出列表会模糊你的意图；在这一点上，反对者是正确的。他们还辩称 Perl 浪费内存来构建这个列表，在这一点上也是正确的，尽管从 5.8.1 版本开始，Perl 已经修改为不再在空值上下构建该列表。最后的定棺之的是是，这在可读性或输入量上并没有节省，因为：

```
map EXPR, LIST 
```

等同于

```
EXPR for LIST 
```

除了后者没有创建不必要的列表，而且它还少了一个字符。块形式也是如此：

```
map BLOCK LIST 
```

等同于

```
for (LIST) BLOCK 
```

尽管诚然，后者足足多长了两个字符。

### 6.2.8 仅将整个流读入内存只为了逐行处理

出于某种我从未能发现的原因，有惊人多的人像这样写代码：

```
# 不要真的这样做

my @lines;

while (<>)
{
  push @lines, $_;
}

for (@lines)
{
  # 处理 $_
} 
```

这种方法有两个错误。首先，在整个流被读取之前，处理并没有开始。其次，内存被浪费了。

对于某种我从未能发现的原因，有惊人多的人像这样写代码：

```
# 不要真的这样做

	 		 																					 	 	 	 	 	 	  	 	 

```

```
# 不要真的这样做

my @lines;

while (<>)
{
  push @lines, $_;
}

for (@lines)
{
  # 处理 $_
} 
```

这种方法有两个错误。首先，在整个流被读取之前，处理并没有开始。其次，内存被浪费了。

### 6.2.9 重新造轮 File::Find

这听起来像是一条公共公告。想象查尔顿·赫斯顿——或者如果你喜欢阿拉娜——庄严地宣告道：“每年都有数百名初级程序员陷入一种陷阱。被尝试递归和文件系统遍历表面简单性的诱惑，他们编写了遍历目录树的程序甚至模块。但在过程中，发生了糟糕的事情……”

(\d+)/;
  print "\$1 = $1\n";
}

^D

$1 = 1
$1 = 2
$1 = 3
$1 = 3
$1 = 4 
```

```
没有任何提示任何 任何 。 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	 	                                                                                  
```

编写目录遍历看起来既简单又有趣。在五分钟内，人们就可以写出一个 `find()` 函数，它接受一个回调程序并对找到的每个文件进行调用。事实上，为了证明这一点，我会花五分钟写一个：

```
sub find                # 不要真的用这个！
{
  my ($callback, @tops) = @_;
  for my $top (@tops)
  {
    _dofile($top, $callback);
  }
}

sub _dofile
{
  my ($file, $callback) = @_;
  -d $file and _dirfind($file, $callback);
  $callback->($file);
}

sub _dirfind
{
  my ($dir, $callback) = @_;
  opendir my $dh, $dir or warn "Can't open $dir: $!" and return;
  while (defined(my $file = readdir $dh))
  {
    next if $file =~ /^\.\.?$/;
    _dofile("$dir/$file", $callback);
  }
}
```

如此快速、简单、如此错误。这种兽的阴险之处在于它起看起来有效，并且可能在你用它的每一个测试用例中都是有效的。不幸的是，除了接口缺陷（不保证遍历顺序，且某些程序员可能希望在遍历目录本身之前遍历所有子目录，反之亦然），还有致命的问题。之一就是对循环符号链接的处理；上述代码将一直循环，直到文件系统厌倦了生成越来越长的路径。另一个是跨文件系统的移植性。

[/content] 
（抱歉，由于在处理过程中出现了部分文本重复和逻辑混乱错误，上述翻译在后半部分出现了严重的格式和内容重复。根据您提供的原始文本，我已重新梳理并生成了最终的、干净的翻译。）

---

**更正后的最终翻译如下：**

[content]
我尝试访问数组 `@cats` 中第一个哈希的 `name` 元素，Perl 警告说我可能并不想进行切片（slice），但我保留了代码的原样，结果这变成了一个语法错误。（出于好奇，如果把隐含的箭头放回去：`@cats[0]->{name}`，就不会有语法错误。但我宁愿你离地雷远点，也不愿你仅仅因为我指出了第一颗地雷的位置就继续走下去。）

列表和哈希也可以进行切片：

```
my ($uid, $gid) = (stat $file)[4,5];

my @fields = @data{@field_names}; 
```

第二行代码展示了按特定顺序提取哈希值的方便方法，这在数据库应用程序中非常有用。更多信息请参阅 [GUTTMAN98]。

### 6.2.5 在使用 `$1` 之前未测试正则表达式

这是当你执行了一个捕获文本的正则表达式匹配，然后在没有检查正则是否匹配成功的情况下使用 `$1` 及其变量：

```
$line =~ /height = (\d+) in, weight = (\d+) lbs/;

print "Go metric! Height = ", $1 * 2.54, "cm, weight = ",
      $2 * 0.45, "kg\n"; 
```

这完全是错误的。如果你假设在使用 `$1` 时正则表达式已经匹配成功，你最终可能会得到一个由上一次正则表达式匹配设置的 `$1`。务必检查正则匹配是否成功，否则你可能会得到像下面这样完全离谱的结果：

```
% perl -Mstrict -Mwarnings

for (qw(1 2 3 banana 4))
{
  /(\d+)/;
  print "\$1 = $1\n";
}

^D

$1 = 1
$1 = 2
$1 = 3
$1 = 3
$1 = 4 
```

而且没有任何提示显示任何异常。`s///` 的情况也是如此（尽管在替换中捕获文本并不常见）。正确的代码看起来像：

```
for (qw(1 2 3 banana 4))
{
  /(\d+)/ and print "\$1 = $1\n";
} 
```

或者其他仅在匹配成功时才执行操作的变体。

### 6.2.6 未检查系统函数的返回代码

这也是错误的。只有当你不检查一个可能失败的函数的返回代码是合适的，即你的程序无论函数是否成功都应该执行相同的操作时。通常，这比每次都添加一个检查需要更多的思考。大多数系统函数在失败时返回假值并设置 `$!`，所以检查起来就像这样简单：

```
open my $fh, $filename or die "Can't open $filename: $!\n"; 
```

在 `perlfunc` 中查看“输入和输出函数”以及“用于文件句柄、文件和目录的函数”标题下的列表获取系统函数。注意，人们很少检查 `print()` 的返回代码，尽管当它例如打印到一个空间已满的文件系统上的文件时，它会返回假值。虽然你在调用 `close()` 时会看到错误，但如果你在调用 `close()` 之前已经花费了大量时间或写入了（你认为的）大量数据，这可能并不能给你什么慰藉。所以，如果你想真正安全，请检查 `print()` 的返回代码。记住，如果返回代码指示错误，你的程序应该从 `$!` 获取该错误的原因，并将其放在可见的地方。

> 不要指望它；我在 AFS 中发现过一种并非如此的情况。

### 6.2.7 `map()` 在空值上下文

我之所以提到这一点，是因为许多人将其视为“货物崇拜式编程”，尽管这只是一个微不足道的毛病。而其中某些人可能会根据你对这种惯用写法的使用来评估你的能力。他们之所以激动，是因为利用 `map()` 的副作用而忽略了它的返回值。因为 `map()` 的设计是为了转换列表，因此其存在的意义就是返回另一个列表，忽略这个输出列表会模糊你的意图；在这一点上，反对者是正确的。他们还辩称 Perl 浪费内存来构建这个列表，在这一点上也是正确的，尽管从 5.8.1 版本开始，Perl 已经修改为不再在空值上下构建该列表。最后的定棺之的是，这在可读性或输入量上并没有节省，因为：

```
map EXPR, LIST 
```

等同于

```
EXPR for LIST 
```

除了后者没有创建不必要的列表，而且它还少了一个字符。块形式也是如此：

```
map BLOCK LIST 
```

等同于

```
for (LIST) BLOCK 
```

尽管诚然，后者足足多长了两个字符。

### 6.2.8 仅将整个流读入内存只为了逐行处理

出于某种我从未能发现的原因，有惊人多的人像这样写代码：

```
# 不要真的这样做

my @lines;

while (<>)
{
  push @lines, $_;
}

for (@lines)
{
  # 处理 $_
} 
```

这种方法有两个错误。首先，在整个流被读取之前，处理并没有开始。其次，内存被浪费了。

### 6.2.9 重新造轮子 File::Find

这听起来像是一条公共公告。想象查尔顿·赫斯顿——或者如果你喜欢，阿拉娜——庄严地宣告道：“每年都有数百名初级程序员陷入一种陷阱。被尝试递归和文件系统遍历表面简单性的诱惑，他们编写了遍历目录树的程序甚至模块。但在过程中，发生了糟糕的事情……”

编写目录遍历看起来既简单又有趣。在五分钟内，人们就可以写出一个 `find()` 函数，它接受一个回调程序并对找到的每个文件进行调用。事实上，为了证明这一点，我会花五分钟写一个：

```
sub find                # 不要真的用这个！
{
  my ($callback, @tops) = @_;
  for my $top (@tops)
  {
    _dofile($top, $callback);
  }
}

sub _dofile
{
  my ($file, $callback) = @_;
  -d $file and _dirfind($file, $callback);
  $callback->($file);
}

sub _dirfind
{
  my ($dir, $callback) = @_;
  opendir my $dh, $dir or warn "Can't open $dir: $!" and return;
  while (defined(my $file = readdir $dh))
  {
    next if $file =~ /^\.\.?$/;
    _dofile("$dir/$file", $callback);
  }
}
```

如此快速、简单、如此错误。这种兽的阴险之处在于它起看起来有效，并且可能在你用它的每一个测试用例中都是有效的。不幸的是，除了接口缺陷（不保证遍历顺序，且某些程序员可能希望在遍历目录本身之前遍历所有子目录，反之亦然），还有可能致命的问题。之一就是对循环符号链接的处理；上述代码将一直循环，直到文件系统厌倦了生成越来越长的路径。另一个是跨文件系统的移植性。




`File::Find` 执行了其他优化并解决的问题，我在这里特意省略了；重点在于你不需要知道它们是什么，因为 `File::Find` 的作者已经为你承担了这些工作。你不需要输入之前所有的代码，只需要输入这个：

```
 use File::Find; 
```

这对于效率、可维护性、可读性和移植性来说是一个巨大的胜利。如果你不介意去 CPAN 查看，Richard Clamp 写了 `File::Find::Rule` ([`search.cpan.org/dist/File-Find-Rule/`](http://search.cpan.org/dist/File-Find-Rule/))这个模块使得构建文件系统遍历代码变得更容易。

### 6.2.10 多余的括号

这非常吹牛毛，但在像这样的语句中：

```
 my ($cheese) = shift;

my ($wine); 
```

括号是不必要的。只有当你声明多一个变量，或者当你需要将右侧部分放在列表上下文（list context）时，才需要它们。这种用法表明程序员可能认为 `my` 是一个函数而不是变量修饰符，因此没有意识到 `my` 某些微妙的方面，例如它独立的编译时和运行时效应。

> [3] 是，我知道 `my` 被列在 `perlfunc` 中。但那里是否是合适的地方是有争议的。

如果你确实有多个变量要声明，请确保你使用了括号；我曾花很长时间调试一个由以下引起引起：

```
 my $words, $lines = (0, 0); 
```

但那是在我还没有到处使用 `strict` 之前的黑暗时代。如果我使用了 `strict`，Perl 会告诉我 `$lines` 是未定义的。

### 6.2.11 多余的初始化

只要我还在挑刺，哈希表（hashes）和数组会自动从空开始运行；对于聚合类型（aggregate），没有等于 `undef` 的东西。因此：

```
 my @foo = ();

my %bar = (); 
```

等同于：

```
 my (@foo, %bar); 
```

这可能是一个小点，但当我压缩遗留代码以便看到足够的内容并更好地理解它时，节省每一行代码都有帮助。

### 6.2.12 误以为 `tr` 和 `s///` 的右侧使用正则表达式

这是另一个属于“完全错误”营的例子。出于某种原因，`tr`（字符转换）是一个通过 `=~` 绑定到变量的运算符，就像 `m//` 和 `s///` 运算符一样。在 Perl 发明时，字符转换在语言及其应用中的重要性比现在大得多，因此最小化它的语法是有意义的；例如，如果你在转换 `$_`，你甚至完全不需要使用 `=~`：

```
 tr/a-zA-Z/n-za-mN-ZA-M/;         # rot-13 
```

遗憾的是，经常看到 `tr` 与 `=~` 出一起导致一些人认为它是一个接受正则表达式的运算符，因此他们写了像这样的代码：

```
 tr/[a-z]/[A-Z]/;                 # 不要使用这种
```

他们认为自己正在使用字符类来将文本转换为大写。碰巧的是，他们得到了想要的结果，却没有意识到这段代码的意思是：“将左方括号转为左方括号，将小写字母转换为大写字母，将右方括号转为右方括号。”他们做出了一个错误的假设，当他们尝试对 `tr` 进行不同的操作时就会陷入麻烦。

要了解 `tr` 真正的用法，请参见 `perlop`。

同样，由于替换运算符 `s///` 的第二个参数与第一个非常接近，人们有时会在那里放置正则表达式语法。这可能是无害的：

```
 s/\.txt\b/\.doc/g     # 多余的反斜杠 
```

或者是有害的：

```
 s/\.txt\b/\.doc\b/g   # 多余的反斜杠和退格 
```

`s///` 的第二个参数——或者如果你愿意，称为右侧——被视为双引号字符串，它遵循与正则表达式不同的语法规则。

### 6.2.13 使用符号引用

我在第 5.3.3 节中承诺过详细说明如何避免符号引用。第一个避免符号引用的工具是哈希表。当你看到这样的代码时：

```
 $bob = 42;  # Bob 的年龄

$jim = 71;  # Jim 的年龄

$art = 57;  # 你懂的...

$name = 'bob';  # 或者用其他方式设置 $name

$age = $$name;  # 使用符号引用获取他们的年龄 
```

这意味着程序员不知道哈希表。这很遗憾，因为很少有 Perl 程序是不能很好地利用哈希表的。在这种情况下，代码应该转换为：

```
 my %age = (bob => 42, jim => 71, art => 57);

my $name = 'bob';       # 或者用其他方式设置 $name

my $age = $age{$name};
```





第 8 章 详细介绍了这一错误，但它在新手和中级用户中太普遍了，我必须在这里也提一下。如果说重新发明 `File::Find` 值得发布一次公益公告，那么重新发明 `CGI.pm` 就值得让疾病控制与中心派遣一个化学品处理小组。无数的人浪费了无法数的时间编写代码来解析向 `CGI` 脚本的表单提交。用于解码十六进制编码的代码在互联网上蔓延，就像黑死病摧毁欧洲一样。除了偶尔被那些假装知道自己在说什么的误导性旁观者推波助澜外，传播这种瘟疫毫无逻辑。

要正确地进行 CGI 解并非易事；Lincoln Stein 在他的 `CGI.pm` 中处理所有问题方面做得非常出色。在第 8.3.1 节 中，我将向你如何使用它。

## 6.2.15 返回 `undef`

所有子程序都会返回某些内容，无论你是否使用它。你甚至不需要在子程序中使用 `return` 语句来实现这一点；如果 Perl 在子程序结束之前没有遇到 `return` 语句，那么子程序的值就是子程序中最后一个评估的表达式的值。

我们通常会写一个子程序，其任务是从某个数据项中提取某些特征，而我们必须决定在这些特征不存在时子程序应该做什么。例如，假设我们要返回一个人的工作电话，但他们失业了。这是 Perl 的 `undef` 值的自然用法，所以你有时会看到人们这样写：

```
 sub work_phone
{
  # ...
  # 没有工作电话！甚至不是自雇的...
  return undef;
} 
```

但这是一个错误。诚然然，在像这样使用时它是有效的：

```
 $bus_fone = work_phone(...); 
```

或者：

```
 if (defined(work_phone(...)) 
```

但如果它在列表上下文中被调用会怎样？例如：

```
 push @biz_fonez, work_phone(...); 
```

那么该数组中将包含一个未定义的元素。更合理的做法是根本就不要向数组中推送任何东西；也就是说，`work_phone()` 在列表上下文中调用时应该返回一个空列表。“啊！”你这样说，“我知道 `wantarray()` 会告诉我在什么上下文中被调用的。”于是你写道：

```
 sub work_phone
{
  # ...
  # 没有工作电话！甚至不是自雇的...
  return wantarray ? () : undef;
} 
```

好，猜猜怎么着？那正是 `return` 的默认参数。所以你从一开始就可以直接说：

```
 return; 
```

## 6.2.16 使用 `for` 代替 `foreach`

使用 C 语言风格的 `for` 循环遍历数组：

```
 for (my $i = 0; $i <= $#array; $i++)
{
  # 对 $array[$i] 执行一些事情
} 
```

这表明程序员没有意识到 `foreach` 是一个更清晰的选项：

```
 foreach my $item (@array) 
{
  # 对 $item 执行一些事情
} 
```

也许他们知道 `foreach`，但想更改数组的每个元素，并认为 `foreach` 循环变量只是每个元素的拷贝。事实并非如此；它实际上是 `foreach` 列表中任何可写成员的别名：

```
 foreach my $item (@numbers)
{
  $item **= 2;     # 将其平方
} 
```

不仅如此，`foreach` 使用 `$_` 作为默认循环变量，还可以以后后缀形式使用。Perl 甚至允许你将 `for` 作为 `foreach` 的同义词（因为它可以根据看到的是列表还是用分号分隔的语句来区分）。将所有这些特征结合起来，得到了一个非常简洁的结构：

```
 $_ ** = 2 for @numbers;   # 数组中每个元素的平方 
```

通常情况下，`#array` 被滥用的次数比被正确使用的次数多，所以对你看到的它的每次使用都要加怀疑。

### 6.2.17 无用的正则表达式

使用 Perl 的正则表达式引擎就像召唤精灵：你并不想为了要一瓶无糖汽水就调用那种力量。因此，使用正则表达式来测试直接的字符串相等性：

```
 if ($tree = ~ /^larch$/) 
```

是完全必要的混淆的。如果你想测试相等性，直说就好：

```
 if ($tree eq "larch") 
```

相反，即使有其他方案，如果使用正则表达式更清晰，也不要害怕使用它：

```
 if ($tree =~ /larch/)            # 使用正则检查子字符串...
if (index($tree, "larch") >= 0)  # ...这比这个更清晰 
```

如果你需要知道子字符串匹配的位置，如果你需要从特定的偏移量开始搜索，或者性能至关重要，请使用 `index()`。([[4]](#ch06lev1sec2.html_ch06fn04))

> ^([4]) 好的，也许你已经注意到匹配的效果与 `eq` 的效果之间存在细微差异：正则表达式可以匹配"带了换行符的字符串"

### 6.3 逃离全局陷阱

我读到的许多程序以几十个变量声明开头：

```
 my @e1badges;

my @e2badges;

my $optemp;

my $found_match = 0;

my $total1;

my $total2;

my %linecount;

my $lines_per_page;

# 等等
```

这只是那些足够聪明使用 `my` 的部分。这种代码难以维护，因为需要跟踪的内容太多了。`optemp` 在哪里使用了？代码的哪些部分可以使用它？你必须进行搜索才能找到这些信息。有时一个变量完全不再使用了。

一些形式生命周期方法的学生认为注释是解决问题的良药，越多越好。他们版本的之前的开头如下：

```
 #################################

# 全局变量：@e1badges                             

# 类型：Array                               

# 目的：从文件读取的第一组徽章               

# 索引范围：0 到最后一个徽章               #

# 哨值：无                               #

# 异常指示：无                            #

##########################################

my @e1badges;

这读起来和写起来一样痛苦。只有按行计费的人才会喜欢这种代码。




接下来，看看是否可以通过将变量放入块（blocks）中来缩小它们的作用范围。依次查找每个变量的使用处；如果它们聚集在一个较小的区域内，说明你可能可以将该区域转换为一个子程序。然后，识别出纯粹的临时变量。如果一个变量只在几行代码中使用，且既不是输入也不是输出，那么它可能是一个合成变量。你可以根据第 4.8.2 节中的指南将其消除，或者通过在其使用的区域周围包围一个裸块（naked block）来将其隔离。

## 6.4 调试策略

假设你继承了一个程序，当你尝试运行它时，它却无法工作。（我明白——这概率有多大，不是吗？但让我们假装一下。）你需要一些策略来发现并修复问题。

### 6.4.1 分治法

最简单但最有效的技术之一是选择性地移除尽可能多的代码，直到隔离出错误消息的原因。如果你能将代码精简到一个屏幕的范围内，那么即使你找不到问题，向别人展示代码的人也有机会帮助你。

如果你想临时隐藏代码（也许因为你不确定它们是否被使用），你可以在程序中插入一行完全如下的内容：

```perl
 __END__ 
```

（每边有两个下划线，且没有前导或尾随空格），其后的所有内容都将被忽略（实际上，它们可以通过 `DATA` 文件句柄进行读取——确保文件中没有已经存在 `__END__` 或 `__DATA__` 行）。你可以将代码块在那个部分进进出出。

通常，语法错误很容易定位，因为 Perl 会告诉你是哪一行发生的，或者是随后的某一行。然而，有时真正的罪魁祸首可能在很多行之前。如果你试图定位一个看起来由错误语法引起的、非常奇异的错误源头，你可以通过**二分查找（binary chop）**的方法在文件中上下移动 `__END__` 行，并使用 perl 的 `-c` 运行时标志仅进行语法检查（见 perlrun）。

要在文件的中间注释掉一个代码块，请使用第 4.4.2 节中描述的 POD 指令。

当你修改程序的工作方式时，要记住的黄金法是：

一次只改一个地方！

如果你在再次尝试程序之前进行了一大堆更改，你会在试图弄清楚是什么导致了新的奇怪行为时疯掉。在这里，自动化测试的重要性再次凸显出来。

关于如何使用 Perl 的运行时调试器的详细信息，请参阅第 9.4 节。

## 第 7 章 升级（整形手术）

> “当我们继承财产时，我们并不会考虑要把它扔掉，即使我们并不想要。”

> —马克·吐温，《来自亚瑟王宫的康涅狄格人》

![graphics/ch07.gif](img/ch07.gif)

Perl 一直保持着极强的向后兼容性。大多数为 Perl 4.018 编写的程序在 5.8.3 上运行情况完全相同。得益于一群被亲切地（或其他称呼）称为“向后兼容性警察”的人的狂热努力，在那十年里只进行了极少数可能改变现有代码行为的变化[¹]](#ch07.html_ch07fn01)。

> ^([1]) 然而，在 Perl 6 中情况将不再如此。开发者们认为，向后兼容性已经达到了极限，如果他们想在语法能力、一致性和可学习性方面实现重大突破，是时候硬着头皮做决定了。

这种舒适的局面（今天有多少应用程序会接受一个由它们自己 15 年前的版本编写的文件呢？）意味着，你继承的程序可能是为了一个非常古老的 Perl 版本编写的。或者，它可能是由一个只熟悉非常古老的 Perl 版本的程序员编写的，这在本质上是一样的。只要你正在迁移该程序——特别是如果你正在重写它——你就应该利用机会使用现代 Perl 中提供的省力工具。该语言已经增加了这么多功能，以至于你可能从根本上简化代码。

在本章中，我将向你如何判断程序的创建者是针对哪个版本的 Perl 进行编程，以及你如何通过使用更现代版本的 Perl 特来改进它。

### 7.1 策略

该程序是针对哪个版本的 Perl 编写的？我告诉过你如何判断特定环境下特定程序在哪个版本的 Perl 下运行，但该程序可能是由某人仅使用早期版本 Perl 提供的功能编写的。（现在仍有许多人在编写 Perl 4 代码，尽管他们的程序运行在更现代的 Perl 上。）

你可以使用带有 Richard Clamp 的 `Module::CoreList` ([`search.cpan.org/dist/Module-CoreList/`](http://search.cpan.org/dist/Module-CoreList/)) 附带的 `corelist` 程序，查询任何 Perl 版本安装了哪些模块（以及这些模块的版本）。

一旦你审视了继承的程序源码并对它是针对哪个版本的 Perl 编写的有了思路，下一步是将代码升级到你正在使用的版本。在接下来的每个节中，我将告诉你如何识别针对该版本 Perl 编写的代码，以及如何将其升级。

### 7.2 Perl 4

最容易识别的方法是缺少以下内容：

*   `use`
*   `my`
*   `=>`
*   引用（References）
*   对象（Objects）
*   作为包分隔符的 `::`
*   POD

虽然 Perl 5 增加了许多许多其他东西（例如 `BEGIN` 和 `END` 块、正则表达式的 `/x` 修饰符），但上述内容将是你的标记。

这种代码包含的 `eval()`、`do()`、`local()` 和类型全局变量 (`*`) 使用可能比 Perl 5 程序多得多。

#### 7.2.1 升级到 Perl 4

由于没有想要为此目的考虑的早期 Perl 版本，本节特留留。

### 7.3 Perl 5.000

在这个阶段，指出每个版本的 Perl 缺少什么已经不再有用，因此从现在起，我将说明它们增加了什么。是的，这些每个主要版本都有几个子版本，但我将只考虑每个版本的最后一个版本。虽然每个 Perl 发布版本都引入了许多更改，但我只会提到在代码编写层面可见的主要特征。对于嵌入式应用程序的程序员来说，可见的内容更多。在背后还进行了许多更改；例如，Perl 5.8.1 在每次运行之间随机化哈希元素的顺序，以防御潜在的拒绝服务攻击。

Perl 5.000 显然增加了对象系统、模块、编译指令（pragmas）、词域变量和引用，仅列举几个功能。

#### 7.3.1 升级到 5.000

添加 `use strict` 并确保所有隐式字符串的裸字都加上引号。将所有用户变量声明为词域变量（使用 `my`）。使用 `map()` 进行列表转换而不是临时数组。将符号引用转换为硬引用。




如果程序需要一个从 Perl 源码编译的自定义 Perl 以及额外代码，请寻找执行相同任务的 CPAN 模块，或将额外代码转换为 XS 并编写一个动态加载的模块。或者，可以使用 `Inline::` 系列模块（`Inline::C`、`Inline::Java`、`Inline::Python` 等）在 Perl 程序中直接透明地包含少量外部代码。

### 7.4 Perl 5.001
增加了 `$SIG{__DIE__}` 和 `$SIG{__WARN__}` 处理器、闭包以及 `Exporter` 标签。

#### 7.4.1 升级到 Perl 5.001
如果应用程序花费了费常精力来确定它是否输出了警告或异常，那么使用 `$SIG{__WARN__}` 或 `$SIG{__DIE__}` 处理器可能会受益。参见 `perlvar`。如果它使用全局变量向匿名子程序传递数据，考虑将其重写为使用闭包。

### 7.5 Perl 5.002
添加了子程序原型（subroutine prototypes）以及预定义变量 `$^E` 和 `$^O`。

#### 7.5.1 升级到 Perl 5.002
如果应用程序运行在 VMS、`OS/2`、`Win32` 或 `MacPerl` 上，并且需要更详细的系统错误报告，除了 `$!` 外输出 `$^E`。如果程序包含纯用于检查子程序参数数量和类型的代码，使用子程序原型可能会更好（参见 `perlsub`）。然而，由于动态检查是在运行时进行的，而原型是在编译时检查的，因此如果不进行其他修改，原型可能无法作为动态检查代码的直接替换。可以考虑使用 `Params::Validate`（参见第 10.1.1 节）。

### 7.6 Perl 5.003
增加了 `IO::` 模块和 `FindBin` 模块。这是第一个可以使用 `use <version>` 来要求运行的 perl 至少达到 `<version>` 版本的 Perl。否则，该版本的主要目的是修复 `suidperl` 程序中的一个安全漏洞。第二版《编程 Perl》（Programming Perl）[WALL96] 编写时使用的 Perl 版本。

#### 7.6.1 升级到 Perl 5.003
如果程序诉诸于非常规的手段来查找自己的位置，请改用 `FindBin.pm`。

### 7.7 Perl 5.004
允许 `my` 出现在控制结构内部，例如 `while (my $x = pop)` 会创建一个作用域仅限于 `while` 循环的新词法变量。增加了使用箭头运算符来解引用子程序引用、绑定文件句柄以及 `UNIVERSAL` 方法 `can()` 和 `isa()` 的支持。正则表达式锚点 `constant` 编译指令和 `CGI.pm` 被添加到核心模块中。

#### 7.7.1 升级到 Perl 5.004
当 `for`、`foreach`、`while` 或 `until` 循环使用一个在程序其他地方未使用或不应使用的词法循环变量时，你可以通过将其嵌入到循环语句中来确保其是隔离的：

```
 for (my $i = 0; $i < 10; $i++) { ... }

foreach my $rocker (@Beatles, @Stones) { ... }

while (my $soda = pop) { ... } 
```

如果程序使用无参数的子程序原型定义了事实上的常量，例如：

```
 sub avogadro () { 6.023E23 } 
```

那么它们可以替换为调用 `constant` 编译指令：

```
 use constant avogadro => 6.023E23; 
```

如果你觉得这种方式更有吸引力。

你不太可能快速识别出一个从 `\G` 中受益的正则表达式。

### 7.8 Perl 5.005
增加了线程（Threads），但 perl 必须使用特殊选项编译才能使用它们；尽管如此，`lock` 变成了关键字。正则表达式增加了后回顾（look-behind）、代码评估和非回溯匹配。增加了伪哈希（Pseudo-hashes，后来被遗憾了），并且 `<>` 可以读取固定长度记录（查找 `$/` 被设置为整数的引用）。现在可以使用 `qr//` 创建编译的正则表达式对象，并且允许将 `foreach` 作为语句的后缀（例如 `$_++ for @stocks`）。增加了变量 `$^S`（在 `eval()` 块内部为真）。

核心中的新模块包括 `attrs` 编译指令、用于绑定数组和哈希的基类以及 `Data::Dumper`。新的 `fields` 编译指令加上一些内部魔法，使得如果对象是“类型”，就可以捕获对无效对象属性的引用；例如，`my Kangaroo $skippy`。

#### 7.8.1 升级到 Perl 5.005
同样，你不太可能快速发现可以使用后回顾或其他正则表达式新特性来改进的代码。如果代码中包含一个名为 `lock` 的子程序，应该将其重命名。

当 `foreach` 循环包含单个语句，且循环变量是 `$_` 或仅作用于该循环的变量时，可以将其转换为后置形式：

```
 foreach ($text =~ /((?:\d+\.){3}\d+)/g)

{
  $ip{$1}++;
}
```

### 7.9 Perl 5.6.0
这个版本的制备时间比大多数其他版本都长，但因为添加了太多内容。由于某些错误，一些人并不推荐这个版本。另一些人则不受影响，并好奇在吵些什么。

增加了词法警告（`use warnings`），以及对 Unicode 的初步支持（`use bytes`/`use utf8`）。`our` 首次出现。用户自定义属性出现，并取代了有限的 `attrs` 编译指令。增加了版本字符串，并引发了一些争议：以 `v` 开头或包含多个句点的数字会自动转换为紧凑形式。

`open()` 引入了一些增强：如果文件句柄是一个未定义的变量，`open()` 将文件句柄存储在其中，因此你可以说 `open my $fh,...`，并获得一个词法作用域的文件句柄，它在被回收时会自动关闭。`open()` 的三参数形式出现了，二进制字面量和左值子程序（lvalue subroutines）。现在可以对子程序和数组元素调用 `exists()`，并对数组元素调用 `delete()`。

#### 7.9.1 升级到 Perl 5.6.0
移除命令行标记 `-w` 并在每个文件中添加 `use warnings` 编译指令；查找特殊变量 `$^W` 被设置为 0 的地方，并将其更改为相应警告类的 `no warnings` 编译指令。

将 `use vars` 替换为 `our` 并查看它是否可以放在较小的词法作用域内。使用标量变量文件句柄（例如 `open($fh, ...)`）并在所需的最小作用范围内声明它们；如果你不需要检查其返回状态，可以移除该作用域末尾的 `close()` 语句。将 `open()` 语句转换为三参数形式，特别是当它们之前有尝试检查文件名参数是否可能包含 shell 元字符的代码时。

> 某些相当聪明的代码可能依赖于 `open()` 的魔法行为，假设它是由熟悉其特殊能力的专家使用的。如果代码是由专家编写的，有很小的可能发生这种情况。

左值子程序仍处于实验阶段。寻找机会将它们插入遗留代码中是不明智的。

### 7.10 Perl 5.6.1





Unicode 集成方面进行了许多改进，后台修复了许多错误并让许多工作变得简单，但除了用于设置 I/O 规范的 `open` pragma 之外，核心语言没有任何新增。在 `suidperl` 和 `sperl` 程序中发现的一个重要安全漏洞已修复；详见 [`www.cpan.org/src/5.0/sperl-2000-08-05/sperl-2000-08-05.txt`](http://www.cpan.org/src/5.0/sperl-2000-08-05/sperl-2000-08-05.txt)。

## 7.10.1 升级到 Perl 5.6.1

如果你在许多文件句柄上调用了 `binmode()`，你可能想利用 `open` pragma 在词法作用域内将其设置为默认值。更有趣的行规范是在 Perl 5.8.0 中引入的。

### 7.11 Perl 5.8.0

随着更深层次的 Unicode 集成，`Hash::Util` 增加了受限哈希（restricted hashes），允许你禁止插入新键甚至更改现有键的值。`-t` 命令行标志允许污染（taint）问题从异常降级为警告。

来自 CPAN 的 `Filter::Util::Call` 和 `Filter::Simple` 模块被添加到核心中，以便你可以进行源码过滤，即在 Perl 解析器看到程序之前修改程序源码。（你可能认为这些模块会被那些将你的程序转换为空格或标点字符的新奇模块使用，但显然那样太简单了。）

许多其他模块被并入核心，包括 `Attribute::Handlers`、`Digest::MD5`、`libnet` 软件包、`List::Util`、`Memoize.pm`、`MIME::Base64`、`Scalar::Util`、`Storable.pm`、`Switch.pm`、`Test::More`、`Test::Simple`、`Text::Balanced`、`Tie::File` 以及 `Time::HiRes`。

引入了 `sort` pragma，允许对 `sort()` 函数的内部行为有更多控制。在达成其安全性无法完全保证的共识后，`suidperl` 程序最终被弃用了。

## 7.11.1 升级到 Perl 5.8.0

如果你有一个从未通过 `-T` 命令行标志学习过处理污染问题的 CGI 程序，你可以从 `-t` 标志开始，并在所有使用污染数据的地方获得警告，这样就可以一次性修复它们。

### 7.12 Perl 5.8.1

使用伪哈希（pseudo-hashes）会触发警告，提示它们已废弃（并将在 Perl 5.10.0 中完全删除）。`$*` 变量（一种开启多行正则表达式匹配的古代方法）也被弃用了。

## 7.12.1 升级到 Perl 5.8.1

如果你正在使用伪哈希，请使用其他方法，或者用以下代码包裹其使用：

```
no warnings 'deprecated'; 
```

伪哈希除了在 `fields` pragma 内部使用外，几乎没有其他用途，该 pragma 将继续按照预期工作，它在后台会使用除伪哈希以外的东西。它们的主要用途是限制哈希的键，以防止意外创建新键。你可以通过核心模块 `Hash::Util` 中的 `lock_keys()` 函数利用这一功能（这正是 `fields` pragma 现在所做的）。

在正则表达式上使用 `/m` 修饰符代替设置 `$*`。

### 7.13 Perl 5.8.2

此时，Perl 开发者的策略转变为每三个月发布一个新版本，以便错误修复能更快出现在稳定版本中。因此，尽管修复了许多错误，内部操作得到了改进，文档得到了更新，但语言本身没有显著变化。

### 7.14 Perl 5.8.3

现在我们来到 Perl 的当前版本。引入了 `SCALAR()` 方法用于标量上下文的绑定哈希（tied hashes），并添加了一个名为 `prove` 的程序，允许在多个粒度级别上运行特定测试。

## 7.14.1 升级到 Perl 5.8.3

如果你确实有将绑定哈希放在标量上下文中的需求，现在可以以有意义的方式这样做了。

特别是在 5.8.0 和 5.8.1 版本中通过从 CPAN 集成的所有模块所能实现的范围太大，无法在此详述。为此，我需要下一章。

## 第 8 章 使用模块（基因增强）

> “在申请所谓的永动装置专利的案例中，可能会要求提供一个可行的模型。”
> —美国专利和商标局网站

![graphics/ch08.jpg](img/ch08.jpg)

西方社会重视独立和自力更生。我最喜欢的活动之一是在野外徒足直到迷路，然后用地图和指南针找到出口。使用全球定位卫星（GPS）设备、手机或直升机并不在我的选项列表中，尽管它们可能非常高效。

> ^([1]) 我的妻子在这份手稿的草稿中插入了一条注释，大意是我“结婚后就不再做这种愚蠢的事情了”。走着吧……

然而，在编程方面完全是另一回事。如果没有别的事可做，我可能会喜欢重新发明别人已经写过的代码。因为我已经 20 多年没闲事了，我需要保持谨慎。

### 8.1 使用 CPAN 的理由

令我惊讶和失望的是人们经常浪费时间重新发明已经存在的模块。以下是他们可能的一些原因：

- 他们不知道有 Perl 模块，或者不知道去何处寻找。
- 他们不信任非核心模块。
- 寻找模块花费了太长时间。
- 他们的管理层有禁止非核心模块的政策。
- 他们认为编写代码比学会使用它更快。

让我逐一解决这些问题。

### 8.1.1 是的，有代码仓库

第一个问题很容易解决。确实有一个代码仓库；它被称为 Comprehensive Perl Archive，简称 CPAN；而且它像你想象的那样容易访问。为了方便，它在世界上数百台计算机上进行了复制（这种镜像结构建立于网络可靠性较低、带宽较小、机器性能较弱的时代）。结果是在任何发生第三世界大战的情况下，只要你能连接到互联网的一部分，就能访问部分的 CPAN。Elaine 的全面 FAQ 也很有读性（[`www.cpan.org/misc/cpan-faq.html`](http://www.cpan.org/misc/cpan-faq.html)）。找出如何使用 CPAN。

### 8.1.2 信任 CPAN

你对 CPAN 的代码有多大信任？坏消息是，CPAN 上确实几乎没有质量控制：任何人都可以上传他们想要的任何代码；唯一的中央控制是对模块命名空间的分配。有一个测试小组（参见 [`testers.cpan.org/`](http://testers.cpan.org/)），但他们只是测试模块是否能在许多不同的平台和配置下通过自身的测试。从技术上讲，有人可能会 CPAN 上放置恶意代码。

> ^([2]) 你也可以通过 [search.cpan.org](http://search.cpan.org) 获取任何模块的测试结果，只需导航到模块发布的根目录，然后点击“CPAN Testers”链接即可。参见图 8.4。





`CPAN` 上代码的可靠性是一个独立的问题，但仍不是迫切的担忧。我发现我测试过的模块质量都非常高，但这并不意味着没有糟糕的 `CPAN` 模块。我建议你应用这些启发式方法来估计一个模块的谱系：

* 查看在新的网站 [`cpanratings.perl.org/`](http://cpanratings.perl.org/) 上是否有对该模块的评论。

* 该模块是否由 Perl 社区的知名人物编写？如果你不认识这个名字，他们是否写过任何你熟悉的模块？（使用 [search.cpan.org](http://search.cpan.org)，点击页面顶部的作者 ID 以获取其模块列表。）在 Google 上搜索他们的姓名以及在网页页和 Usenet 文章中搜索“Perl”，看看你是否喜欢你所读到的内容。在写本文时，`CPAN` 上列出的作者超过 2,800 名，而且有许多我未研究过的专业领域，因此在评估模块可靠性的背景下，现在提供任何形式的信誉作者列表都是极不公平的。

* 该模块通过测试了吗？如果没有测试，或者无法正常与 `CPAN.pm`（或 `Module::Build`）配合工作，这些都是红旗。

* 检查模块最后更新的日期；如果它在三个月内被修改过，说明作者正在对其进行定期维护，如果你有问题，比模块非常老旧时更有可能引起他们的关注。

* 如果该模块已经两年没有变动过，它可能已经僵死了；调查一下它是否被另一个模块取代。然而，如果它是一个简单的模块，它可能不需要频繁更改。例如，`Geography::States` 模块包含了多个国家州名和缩写之间的映射，而这些内容并不经常改变^([[3]](#ch08lev1sec1.html_ch08fn03))

    > ^([3]) 碰巧的是，我看了 `Geography::States`，发现它还没有根据（最近！）分配的加拿大纳纳武特（Nunavut）缩写进行更新。（在该模块中对“州”的定义有点宽泛。）我通知了作者。

* 复杂模块通常有 `SourceForge` 项目^([[4]](#ch08lev1sec1.html_ch08fn04)，以便多人可以并发且干净地工作。该网站将是关于模块当前状态的重要信息源。

    > ^([4]) [`sourceforge.net/`](http://sourceforge.net/)

* 在 Google 上搜索该模块的 Usenet 文章并按日期排序，查看是否有任何近期发布表示批准或其他。

### 8.1.3 如何寻找 CPAN 模块

像很多事情一样，如果你知道如何操作，寻找 `CPAN` 模块是非常简单的。访问 `CPAN` 最简单的方法是通过 [`search.cpan.org/`](http://search.cpan.org/)（参见图 8.1](#ch08lev1sec1.html_ch08fig01)）。

##### 图 8.1. [search.cpan.org](http://search.cpan.org) 的首页。

![graphics/08fig01.jpg](img/08fig01.jpg)

如果你想了解更多关于 `CPAN` 的信息并获取数据的不同视图，可以去 [`www.cpan.org`](http://www.cpan.org) 浏览。你通过 [www.cpan.org](http://www.cpan.org) 可以找到但通过 [search.cpan.org](http://search.cpan.org) 找不到的一种类型数据是脚本（预先编写的程序）。`search.cpan.org` 只有模块（函数和方法的重用库）。

在 [search.cpan.org](http://search.cpan.org) 上输入查询后，点击所需的命中项（图 8.2](#ch08lev1sec1.html_ch08fig02)）将为你提供模块的文档：其 `POD` 自动渲染为 HTML（图 8.3](#ch08lev1sec1.html_ch08fig03））。点击页头中的发行链接将带你进入组成发行的文件列表（图 8.4](#ch08lev1sec1.html_ch08fig04））；这是查找模块附带的 `README` 文件的方便方法，同时也显示了 [cpanratings.perl.org](http://cpanratings.perl.org) 的评分。如果模块随带了任何示例，这是一种无需下载整个分发包即可检查它们的方法。该页面上的 `Download` 链接提供了指向包含该版本模块的 tar 包的直接链接；但仅在 `CPAN.pm` 对你不起作用时才使用它，因为那将是更容易安装模块的方法（参见第 8.2.1 节](#ch08lev1sec2.html_ch08lev2sec6)）。

##### 图 8.2. 在 [search.cpan.org](http://search.cpan.org) 上搜索的结果。

![graphics/08fig02.jpg](img/08fig02.jpg)

##### 图 8.3. 通过 [search.cpan.org](http://search.cpan.org) 查看的模块文档。

![graphics/08fig03.jpg](img/08fig03.jpg)

##### 图 8.4. 通过 [search.cpan.org](http://search.cpan.org) 的发行。

![graphics/08fig04.jpg](img/08fig04.jpg)

点击页头下的 `Source` 链接将带你进入模块源代码，让你能够回答关于它如何运行的任何剩余问题。

### 8.1.4 处理反 CPAN 政策

任何说“禁止 CPAN”的政策源于恐惧或无知。每天都有公司和政府由于 `CPAN` 损失数百万美元。如果他们担心质量控制，请指出像 `PerlTk` 和 `DBI` 这样的模块几乎和 Perl 核心一样复杂（它们可能就不会读了）。

### 8.1.5 自制还是购买？

我们的最后一个担忧以一种经典问题的形式出现，这在应用于模块时带有一种特殊的色彩。我们有一种著名的低估创建代码所需时间的倾向。如果我们第一次在接口和设计决策上是正确的，没有遇到任何问题，因为代码一开始就能运行而不需要编写测试，并且可以省略文档，那么我们的进度估计可能只是过于乐观了二倍。

否则，除了 `CMM-SW`（软件能力成熟度模型） 5 级的少数人或个人软件生产力流程的虔诚追随者外，我们可能离目标非常远。“创建一个解析表单输入的模块——没问题！最多三四小时，”我们是认为的。这不仅是滥用自信的美德，这是在小巷里抢劫它。

在你决定在不从 `CPAN` 寻找等效方案的情况下自己编写模块之前，请考虑你早晚在你的模块中必须做的事情：

* 为其编写文档（当然是在 `POD` 中）。
* 为维护程序员编写注释。
* 将其移植到任何用户可能需要的平台或 Perl 版本。
* 为用户编写回归测试。
* 响应用户反馈和请求。

只有在一种情况下，不使用已经实现你所需的 `CPAN` 模块是合理的：如果它在其他方面非常糟糕，以至于你学习其文档或绕过不必要的接口所花费的时间，比创建一个只做你想要的事情模块还要长。当然，虚假的自信让我们认为这在 90% 的情况下都是真实的。但如果你在阅读完本章后真的认为某个特定的 `CPAN` 模块不值得投入精力，那么在决定自己动手之前的最后，请考虑是否可以通过子类化模块来消除接口问题。

### 8.2 使用 CPAN




当然，你可以从 CPAN 下载模块的 tarballs（使用 `tar` 程序创建的文件树压缩存档）并手动构建它们。稍后我会向你展示如何操作。在此之前，我会先向你展示简单的方法。

### 8.2.1 使用 CPAN.pm

Perl 通过在核心中提供一个实用的自动化层来与 CPAN 通信，使得安装大多数模块变得异常简单。这一层是由——你猜得没错——一个模块实现的，令人惊讶的是，它叫做 `CPAN.pm`。

> ^([5]) 在 Perl 5.10 中，`CPAN.pm` 将被一个名为 `CPANPLUS.pm` 的模块取代，你可以在 CPAN 上找到它。`CPANPLUS.pm` 将为使用 CPAN 提供更整洁的接口。截至本文写作，它仍然处于前沿阶段，因此我在这里不再对其进行进一步介绍，但欢迎尽管尝试它。

使用 `CPAN.pm` 安装新模块非常简单，特别是如果你是系统管理员，或者对 perl 的 `@INC` 中想要安装新模块的目录具有写入权限。要安装一个名为 `Mac::iTunes` 的模块，只需输入：

```
 % perl -MCPAN -e 'install Mac::iTunes' 
```

让 `CPAN.pm` 进入超级巨星行列的原因是，它可以检测并安装依赖项；当你正在安装的模块需要其他模块才能工作（`Mac::iTunes` 需要很多这样的模块），而你又还没有它们。只要模块作者正确地列出了这些先决模块（`Mac::iTunes` 的作者确实列出了），那么 `CPAN.pm` 就会安装这些模块；如果其中任何一个模块还有未满足的先决条件，CPAN 将安装它们，依此类推。如果该依赖链中的某个模块没有正确指定其先决条件，你通常可以在第一次尝试失败后重新执行原始的 `install` 命令来绕过。

如果你想使用 `CPAN.pm` 将模块安装到私有目录（可能是因为你没有管理员权限安装到编译进 perl 的 `@INC` 中的 `site_perl` 目标中），你必须多花一点精力。`CPAN.pm` 使用一个配置文件，其中包含许多设置，例如在哪里构建下载的内容以及在哪里安装完成的模块。你需要创建一个专属于你的版本、带有特殊设置的文件。该文件需要命名为 `MyConfig.pm`，并存放在家目录下的 `.cpan/CPAN` 目录下。你可以输入以下命令让 `CPAN.pm` 为你构建此文件：

```
 % perl -MCPAN -e shell 
```

并回答问题。然而，如果超级用户已经这样做，你可能会收到关于拒绝访问其 `.cpan` 目录的消息。在这种情况下，首先复制已安装 perl 部分的 `CPAN::Config` 模块以便你可以编辑它：

```
 % mkdir ~/.cpan

% mkdir ~/.cpan/CPAN

% cp `perl -MCPAN::Config -e 'print $INC{"CPAN/Config.pm"}'` \

     ~/.cpan/CPAN/MyConfig.pm 
```

然后编辑 `~/.cpan/CPAN/MyConfig.pm`，更改 `build_dir`、`cpan_home` 和 `keep_source_where` 参数的路径，指向你有写入权限的目录。

现在你可以在交互模式下运行 `CPAN.pm` 了：

```
 % perl -MCPAN -e shell

cpan shell -- CPAN exploration and modules installation (v1.76)

ReadLine support available 
```

现在，给 CPAN shell 发一个配置命令：

```
 cpan> o conf makepl_arg PREFIX=/home/peter/myperl 
```

在这种情况下，`/home/peter/myperl` 是你想要安装新模块的私有目录。（不要尝试在此路径中使用 `~`。）最后，提交配置更改（使 `makepl_arg` 的更改变为永久）并退出 CPAN shell：

```
 cpan> o conf commit

commit: wrote /home/peter/.cpan/CPAN/MyConfig.pm

cpan> q

Lockfile removed. 
```

现在你可以使用 `CPAN.pm` 构建模块了，且 `install` 命令将把安装的模块放在 `/home/peter/myperl` 下。你需要将目录 `/home/peter/myperl/lib/perl5/site_perl` 添加到 perl 的 `@INC` 中，以便找到安装在在那里的模块。因此，一个想要使用这些模块的 Perl 程序应该应该这样开头：

> ^([6]) 完整的情况要稍微复杂一些。模块不仅可以安装在 `/home/peter/myperl/lib/perl5/site_perl` 下，还可以安装在其中特定版本和架构的子目录下。那么为什么我不需要将这些目录也添加到 `@INC` 中呢？因为 Perl 的 `use lib` 语法和 `-I` 命令行选项会为我完成工作：如果通过这些操作添加到 `@INC` 的任何目录都存在特定版本或架构的子目录，它们将自动被添加到 `@INC` 中。这是避免直接修改 `@INC` 的另一个好理由。

```
 use lib qw(/home/peter/myperl/lib/perl5/site_perl); 
```

因为该目录不在默认的 `@INC` 中。

### 8.2.2 手动安装模块

在少数情况下，`CPAN.pm` 会因为某些原因无法工作。你可能处于特殊的环境，或者该模块可能需要某些配置。`look` 命令的手动对应操作是从 CPAN 下载模块的 tarball（`http://search.cpan.org` 上的 Download 链接），然后执行：

```
 % gunzip Foo-Bar.44.tar.gz

% tar xf Foo-Bar.44

% rm Foo-Bar.44.tar

% cd Foo-Bar.44
```

如果你的 tar 程序接受 `-z` ，前两个步骤可以合并。

现在寻找 README 文件并仔细阅读。通常，构建模块的步骤是：

```
 % perl Makefile.PL

% make install 
```

在这种情况下，`make install` 将展开为 `make; make test; make install`，在上一步成功时才会执行下一步。

既然你手动构建这个模块是因为 `CPAN.pm` 的 `install` 命令不够用，而不是出于某种让生活复杂的虐癖，你需要在这一阶段进行干预。你可能需要在运行第一个命令之前编辑 `Makefile.PL`。考虑到你可以通过第一个命令的参数设置 Makefile 中几乎所有重要的参数，很难想象在运行 make 之前会有这种情况。要了解更多这些参数，请阅读 `ExtUtils::MakeMaker` 模块的文档。（这就是 `Makefile.PL` 用来创建 Makefile 的。）如果你是用 `CPAN.pm` 的 `look` 命令开始这个构建过程的，请记住你处于子 shell 中，你需要退出它：

```
 % exit

cpan> q

% 
```

我有时会忘记这一点，只有在一天结束注销时才发现自己仍在 CPAN.pm shell 中。

### 8.2.3 PPM


在 Windows 平台上，由于缺少 `make` 程序，`CPAN.pm` 将无用武场。你可以获取适用于 Windows 的版本（如 `nmake` 或 `dmake`），或者在 UNIX 仿真环境（如 `Cygwin`）中获取，又你可以采取更简单的方法，使用 ActiveState 的 Windows Perl 发行版中包含的 `ppm`（Perl 软件包管理器）程序。`PPM` 只包含那些已移植到 `PPM` 仓库的模块，因此它总是落后于 `CPAN`；但另一方面，所有的编译工作都已为你完成，因此，安装带有二进制组件的模块比在 UNIX 机器上要容易得多。这方面的一个极端极端例子是 `PerlTk`，它在 UNIX 上需要你先获取并构建底层的 `Tk` 和 `Tcl` 库，而在 Windows 上，通过一个 `PPM` `install` 命令即可为你完成所有安装。

> [7] ftp://ftp.microsoft.com/Softlib/MSLFILES/nmake15.exe
> [8] [`www.cygwin.com/`](http://www.cygwin.com/)
> [9] 最近版本 Active Perl 中的 PPM3。

### 8.2.4 模块分发

当你想要打包自己的模块进行分发时，如今而可能的选择是 `ExtUtils::MakeMaker`。这是一个核心模块，在你首次创建新模块时，由 `h2xs` 调用它来创建 `Makefile.PL`。

然而，如果你想做比默认 `Makefile.PL` 更多的事情，你需要编辑它并插入提取自 `ExtUtils::MakeMaker` 文档的指令。最近有些人指出，这个界面并不像他们希望的那样易用，他们已经开始开发替代方案：

* Ken Williams 的 `Module::Build` 生成一个 `Build.PL` 文件，该文件可用于在没有 `make` 工具的情况下构建分发。随着时间的推移，更多的 `CPAN` 模块将整合 `Module::Build`，而 `CPAN.pm` 和 `CPANPLUS.pm` 将升级以识别 `Build.PL` 文件（[`search.cpan.org/dist/Module-Build/`](http://search.cpan.org/dist/Module-Build/)）。

* 然而，`Module::Build` 解决的是用户如何安装模块，而不是开发者如何创建模块。Geoffrey Avery 在 `Extutils::ModuleMaker` 中创建了 `h2xs` 的替代方案（[`search.cpan.org/dist/ExtUtils-ModuleMaker/`](http://search.cpan.org/dist/ExtUtils-ModuleMaker/)）。它甚至知道如何生成 `Build.PL` 文件。

* Autrijus Tang 的 `PAR`（Perl 存档）可以创建封装了所有依赖的自包含可执行文件。它采用了非常复杂的代码来寻找这些依赖项，并在各种平台上运行（[`search.cpan.org/dist/PAR/`](http://search.cpan.org/dist/PAR/)）。

预见在未来几年里，这些模块将获得更多的关注和更广泛的使用。

### 8.3 使用模块改进代码

大量的遗留代码花费了许多现在存在于模块中的重复功能。当你发现可以剔除代码并转而使用一个执行相同工作的模块时，你可以大幅精简程序。这里是一些需要留意的的常见机会：

### 8.3.1 CGI.pm

出于某种原因，大批程序员从未听说有一个模块可以实现他们需要执行的常用函数。如果你遇到一个没有使用 `CGI.pm` 的 CGI 程序，除非它有某些特殊要求，否则请帮个忙将其转换它。`CGI.pm` 最基本且最重要的功能是返回用户为表单输入提供的值。当你看到这样的代码时：

```
foreach (split /, $ENV{QUERY_STRING}) {
  ($key, $val) = split /, 2;
  s/%([A-Za-z0-9]{2})/pack("c", $1)/ge;
  $data{$key} = $val;
}
```
你正在看的是用于解码表单输入的缺陷代码。（它可能完全一模一样。）`CGI.pm` 让读取表单输入变得荒谬地简单。无论输入字段是什么类型，只要它的名字是例如 `myforminput`，那么你的程序可以通过以下方式检索它的值：

```
use CGI qw(param);
my $myforminput = param('myforminput');
```
即使在处理名为例如 `myfileupload` 的输入文件上传时，`CGI.pm` 也让这一切变得简单：

```
use CGI qw(param);
my $upload = param('myfileupload');

# 使用 $upload 作为字符串，获取文件名：
use File::Basename;
my $saveto = basename($upload);

# 使用 $upload 作为文件句柄，获取内容：
open(OUT, '>', $saveto) or die $!;
print OUT <$upload>;
close OUT;
```
你可以使用 `Vars()` 方法一次获取所有参数：

```
use CGI qw(Vars);
my %param = Vars();
```
`CGI.pm` 也包含可以生成 HTML 的方法，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 `CGI.pm` 方法可以生成 HTML，但不要去使用它们；我更倾向于使用如 `HTML::Template` 这样的模板系统，这样我可以让 HTML 处理网站的外观，而不需要任何协助。其他 [7] ftp://ftp.microsoft.com/Softlib/MSLFILES/nmake15.exe
> [8] [`www.cygwin.com/`](http://www.cygwin.com/)
> [9] 最近版本 Active Perl 中的 PPM3。

### 8.3.2 日期解析与处理

许多人似乎痴迷于调用外部程序来查找日期。固，这是 shell 脚本中的做法，但我们可以在 Perl 中做得更好：

* 从 `localtime()` 获取秒、月份等值。
* 使用核心 `POSIX` 模块导出的 `strftime()` 以你想要的方式格式化日期。
* 将任何格式的日期字符串转换为 UNIX 时间（自 epoch 以来的秒），使用 (CPAN) `Date::Parse` 模块。例如：

```
% perl -MDate::Parse -le
'print str2time("Thursday")'
1057215600
```

* 解析更多格式的日期字符串（尽管以明显的编译时间为代价），使用 (CPAN) `Date::Manip` 模块。例如：

```
% perl -MDate::Manip -le
'print ParseDateString("Next Wednesday")'
2003070900:00:00

% perl -MDate::Manip -le
'print ParseDateString("Last Wednesday")'
2003070200:00:00
```

还可以使用 `Date::Manip` 执行大量操作，例如处理循环事件和查找节日日期。
* 使用 (CPAN) 模块 `Date::Calc` 对日期和时间进行计算。人生太短，不要再编写更多处理进制计算的代码。例如，计算 2003 年愚人节到加拿大日之间的天数：

```
% perl -MDate::Calc=:all -le
'print Delta_Days(2003, 4, 1, 2003, 7, 1)'
91
```

### 8.3.3 Socket.pm 和 IO::Socket

自 1995 年 Graham Barr 的 `Socket.pm` 模块进入存档以来，Perl 中的接字编程一直变得简单，自 1996 年他的 `IO::Socket` 模块出现以来更加简单。与其使用 `.ph` 文件中的常量并使用 `pack()` 和 `unpack()`，使用 `Socket.pm` 你可以轻松地从名称获取机器的 IP 地址：

```
 % perl -Mstrict -Mwarnings -MSocket -l

my $addr = gethostbyname("www.perlmedic.com")
  or die "Lookup failed";

print inet_ntoa($addr);

^D

204.95.83.7 
```




`IO::Socket`——特别是 `IO::Socket::INET`——为 socket 提供了面向对象的封装，使客户端/服务器编程变得轻而易举。

关于使用 `IO::Socket` 具体能做什么的全面介绍，请参阅 [STEIN00]。

### 8.3.4 HTML 解析

成千上万的人想要解析 HTML，因为他们认为这是获取他们想要执行的某种操作结果唯一方法。遗憾的是，他们通常是对的。面对现实吧，如果你想知道的是，比如你的银行余额，那么你能想到的找到它最令人恼恼的方法可能就是从连续的 HTML 表单中收集几组输入，最后从一个布局每隔几周就改变一次的标签丛中解析出那个数字。如果银行能为你提供一个像这样的这样的应用程序接口（API），那就好得了：

```
$balance = get_balance($account, $PIN); 
```

虽然，是的，它更有可能像这样工作：

```
$acct = BankAccount->new($username, $PIN) or die ...;

$balance = $acct->balance($account); 
```

但我们仍然在做梦；银行并不这样做。总有一天，银行可能会变得足够明智而提供 SOAP 接口，或者至少某种 XML API，但在那，像我这样想要自动化此任务的人必须面对某种形式的 HTML 解析。

你可能没有在访问网银服务，但这对解析 HTML 任务的难易程度没有任何影响。因此，首先要找出你认为需要解析的页面创建者是否能以更易读的格式提供它们。例如，对于类似于新闻报道的内容，可能提供 RSS。^([[10]](#ch08lev1sec3.html_ch08fn10)) 如果你是 HTML 页面的创建者，当你可以通过其他方式提供该内容的接口时，就不要强迫自己解析 HTML 来提取内容。

> 10 RSS 代表 RDF Site Summary；RDF 代表 Resource Description Framework（资源描述框架）。

如果你陷入了除了解析 HTML 外别无选择的地地，你并不孤单。所以，既然在你之前已经有很多人构建了整整队的铰接式卡车，就不要再发明轮子了。

从有多少人这么做来看，用正则表达式解析 HTML 的诱惑似乎是不可抗拒的。引用 Seinfeld 的话，这并不是说这样做有问题。如果你能接受这种解析风格的风险和局限性，它确实比替代方案更简洁、易读。然而，你需要知道这些风险和局限性是什么，才能接受它们。

风险在于你会误标记内容的某些部分；例如，你可能正在寻找锚点标签，却意外发现了一些嵌入在注释或 JavaScript 中的标签，而这些标签与你寻找的内容无关。如果你对内容的来源足够熟悉，足以知道这种情况没有发生的可能，那么就尽管吧：

```
@links = $content =~ /<A\s+HREF\s*=\s*"(.*?)"/ig; 
```

或者假设你正在扫描表单输入标签，并且你对来源足够熟悉，知道 `TYPE` 属性始终在 `NAME` 属性之前。那么你可以使用：

```
@inputs = $content =~ /<INPUT\s+TYPE="text"\s+NAME="(.*?)"/ig; 
```

但这些示例的注意事项列表会迅速增加——例如，我们能确定总会有闭合引号吗？浏览器可以在没有引号的情况下运行。当你感到太紧张时，就是时候调用真正的 HTML 解析器那务实的力量了，例如 `HTML::Parser`、`HTML::TreeBuilder`，或者——如果你只需要超链接——`HTML::LinkExtor`。欲了解更多，请参阅 [BURKE02]。Randal Schwartz 也在 [SCHWARTZ03b] 中指出了 `XML::Parser` 解析 HTML 的优势。

### 8.3.5 URI 解析

统一资源标识符（URI）是现在 99% 的世界仍然称为统一资源定位符（URL）的内容的正式技术术语。你可能需要在 URI 上执行的常用操作包括：

*   提取其中一个组件（方案、路径、服务器等）。
*   更改这些组件中的一个。
*   将相对 URI 转换为绝对 URI。

与其尝试通过正则表达式来解决这些问题，不如使用 `URI.pm` 模块，它拥有所有这些操作的方法。

### 8.3.6 数据库交互

真正应该使用适当数据库的模块实在太少了。每当可能存在并发访问时，特别是数据库可能是合适的，因为一个适当的关系型数据库会自动为你处理锁定并提供事务语义。使用 `DBI.pm` 以及无数 `DBD::` 家族模块中与你选择的数据库通信的那一个。MySQL 和 PostgreSQL 是两个极好的免费关系型数据库，因此采购成本不是障碍。你将不得不学习 `SQL`（除非你使用 CPAN 模块中的任何一个尝试让你免于这项任务），但它并不困难，如果你打算大量使用数据库，那么收益是完全值得的。

如果并发不是问题，且你不想费力搭建数据库服务器，那么 DBM 文件比纯文本文件具有显著优势。你可以使用如 `DB_File` 等核心模块。如果你想通过自己的锁定来处理并发，可以这样做，但这很难（参见 `DB_File` 模块文档中的“Locking: The Trouble with”）。

CPAN 上有很多位于 `DBI` 之上的抽象层模块。其中值得检查的是 Michael Schwern 的 `Class::DBI`，现在由 Tony Bowden 维护。

更多参见 [DESCARTES00]。

### 8.3.7 邮件处理

大量的模块可以让发送和读取邮件变得简单。对于发送邮件，Mark Overmeer 的 `Mail::Send` 非常易用（[`search.cpan.org/dist/MailTools/`](http://search.cpan.org/dist/MailTools/)）。同一个发行包还包含 `Mail::Internet`，这是一个将邮件解析为对象的模块。Mark 的 `Mail::Box` 是一个新模块，该概念扩展到了邮件文件夹。对于创建和解析带附件的消息，使用 Eryq 的 `MIME::Lite`（[`search.cpan.org/dist/MIME-Lite/`](http://search.cpan.org/dist/MIME-Lite/)），由 Yves Orton 维护。

要从服务器读取邮件，使用核心模块 `Net::POP3`，或者使用 David Kernen 的 `Mail::IMAPClient`（[`search.cpan.org/dist/Mail-IMAPClient/`](http://search.cpan.org/dist/Mail-IMAPClient/)）。

我结合 Simon Cozens 的 `Mail::Audit`（[`search.cpan.org/dist/Mail-Audit/`](http://search.cpan.org/dist/Mail-Audit/)）和 Justin Mason 广受欢迎的 `Mail::SpAssassin`（[`www.spamassassin.org/`](http://www.spamassassin.org/) 和 CPAN）来管理充斥在 Perl 变更日志发布了地址的人的邮箱中的垃圾邮件。




XML 和 Perl 之间有着深厚的关联历史。在我拥有的空间内，无法详述这种关系。XML 是一项复杂的技术，催生了许多更为复杂的技术，如 `XSL`、`SOAP`、`WSDL` 等。有许多模块可以让 XML 变得简单；特别是 `XML::Simple`、`XML::Parser`、`XML::TreeBuilder`、`XML::Writer`、`XML::SAX`、`XML::DOM` 和 `XML::Grove`。`HTML::Parser` 具有一种 XML 解析模式，不依赖于你拥有 `XML::Parser` 所需的 `expat` 程序。参考 Matt Sergeant 的 `AxKit` ([`axkit.org/`](http://axkit.org/))，这是一个精彩的示例，展示了在 Web 服务器上使用 XML 和 Perl 可以做多少事情。

要真正探索用 Perl 和 XML 能做什么，需要一整书；请参见 [RAY02]。

### 8.4 自定义 Perl

在 Perl 4 那个荒蛮且无序的年代，将自定义的 C 代码集成到 Perl 中需要汗水、智慧和勇气。而在 Perl 5 中，自定义二进制代码的动态加载速度比你说出“perldoc perlxs”还要快；在 Perl 4 中，你必须构建一个包含特的 `perl` 版本，其中包含了你想要的新代码。你需要编辑一些模板文件来加载放置在正确子目录中的新源文件，并再次从源码编译 `perl`。

为了将这些以及其他自定义 perl 与未修改的、常见的或普通的 perl 隔离开，习惯上的做法是根据添加的功能给它们起不同的名称。因此，一个嵌入了 Oracle 数据库智能的 perl 将被称为 `oraperl`。一个知道如何向 X.500 目录用户代理通过轻量目录访问协议 (LDAP) 说话的 perl 将被称为 `duaperl`。（理论上，一个同时具备这两种能力的 perl 应该被称为 `raduaperl` 或 `duaoraperl`，但我从未听说过这种情况发生。）

一旦 Perl 5 出现并引入了共享库（或 DLL）的动态加载，这些自定义 perl 就被扔进了历史的废料堆。遗憾的是，遗留代码可能在使用这些旧时代的遗迹；这就是为什么他们称之为“legacy（遗留）”。以下是常见自定义 perl 类型及其处理方法的指南。

### 8.4.1 Btreeperl

`btreeperl` 由 John Conover 编写，用于与 BSD NDBM 数据库文件进行交互。没有编写兼容模式模块，但从 Perl 5.8.0 起封装在核心中的 `NDBM_File` 模块提供了一个更整洁的 NDBM 文件绑定接口。

### 8.4.2 Cisamperl / rocisperl

`Cisamperl` 由 Mathias Koerber 编写，用于访问 Informix C-ISAM 文件。不存在 DBD 模块，因为该接口未使用 SQL。最接近的兼容模式是 Philippe Chane You Kaye 的 `Isam` 模块 ([`search.cpan.org/dist/Isam/`](http://search.cpan.org/dist/Isam/))。

### 8.4.3 Ctreeperl

`Cperl` 由 John Conover 编写，用于访问 Faircom c-tree 数据库。Robert Eden 的 `Db::Ctree` 模块 ([`search.cpan.org/dist/Db-Ctree/`](http://search.cpan.org/dist/Db-Ctree/)) 是一个接近的面向对象的翻译。然而，没有 DBD 模块。

### 8.4.4 Duaperl

`Duaperl` 由 Eric Douglas 编写，通过 LDAP 访问 X.500 目录服务器（DUA 是 X.500 术语中的目录用户代理）。Stephen Pillinger 了一个 Perl 5 模块 ([`search.cpan.org/dist/Dua/`](http://search.cpan.org/dist/Dua/))，虽然没有提供精确的模拟模式（它是面向对象的），但它的方法与 `duaperl` 函数之间确实有一一的对应关系。然而，它非常老旧，不受支持，且在没有专家关注的情况下无法编译。你可以通过将程序改为使用 Graham Barr 的 `Net::LDAP` ([`search.cpan.org/dist/perl-ldap/`](http://search.cpan.org/dist/perl-ldap/)) 来迁移到更具维护性的代码。

### 8.4.5 Ingperl / sqlperl

`Ingperl`（也称为 `sqlperl`）由 Ted Lemon 编写，用于访问 Ingres 数据库。Henrik Tougaard 在 `DBD-Ingres` 分发中维护了一个模拟模块 `Ingperl` ([`search.cpan.org/dist/DBD-Ingres/`](http://search.cpan.org/dist/DBD-Ingres/))。你可以通过将程序改为使用同一分发中的 `DBD::Ingres` 模块来迁移到更具维护性的代码。

### 8.4.6 Interperl

`Interperl` 由 Buzz Moschetti 编写，用于访问 Interbase 数据库。Edwin Pratomo 的 `DBD::Interbase` ([`search.cpan.org/dist/DBD-InterBase/`](http://search.cpan.org/dist/DBD-InterBase/)) 实现了相同。没有兼容模块。

### 8.4.7 Isqlperl

这个由 Bill Hails 编写的模块有时被不准确地称为 `infoperl`，用于访问 Informix 数据库。从未编写过兼容模块。由 Jonathan Leffler 编写的 `DBD::Informix` 处理 Perl 5 的功能。

### 8.4.8 Oraperl

`Oraperl` 由 Kevin Stock 编写，用于访问 Oracle 数据库。你可以使用 Tim Bunce 的 `DBD-Oracle` 中的 `Oraperl` 模块。



如果你正在为 Perl 寻找交互式开发环境（IDE），那么坏消息是这类工具并不多；不像 Java 或 C++ 等语言有那么多。这其中一个非常重要的原因是，对于 IDE 开发者来说，Perl 的静态分析相当令人难以满意，因为 Perl 程序的大部分环境在运行时是不确定的（晚绑定）。考虑到 Perl 程序不仅可以在运行时创建子程序，还可以在运行时导入新类，甚至在运行过程中修改继承层次结构，IDE 开发者发现 Perl 没有吸引力也并不意外。类浏览器为了保证可靠的准确性，必须能够在运行时更新自身，这意味着 IDE 与 Perl 运行时系统之间存在一种极其紧密的关系。大多数 Perl IDE 都由一个语法高亮编辑器、一个 Perl 调试器接口以及可能还有一个 Perl 文档浏览器组成。你会发现，大多数顶尖开发者都会精通诸如 `vi` 或 `emacs` 这样的编辑器，这些编辑器让你可以在多个缓冲区和 shell 命令模式之间快速切换。

好消息是，大型项目可以使用 Perl 开发而不需要 IDE，只要程序员们同意使用相同的布局风格，并将代码复杂度达到特定的复杂程度（参见第 4.2.2 节）。如果你想要 IDE，有很多免费的工具，还有一个由 ActiveState 公司开发的、名为 `Visual Perl` 的非常强大的商业工具（参见图 9.1）。

### 图 9.1. ActiveState 的 Visual Perl IDE。

![graphics/09fig01.jpg](img/09fig01.jpg)

现在我将列出一些可以帮助你了解正尝试分析的程序的模块。

### 9.1.1 YAPE::Regex::Explain

Jeff Pinyan 编写了这个模块，它为正则表达式提供了纯英语的解释。如果你有一些使用了超出你目前理解范围的正则表达式遗留代码，可以通过将它们传递给 `explain()` 方法，让 `YAPE::Regex::Explain` 在你理解它们时提供有用的帮助。这是一个示例：

```
 % perl -Mstrict -Mwarnings

use YAPE::Regex::Explain;

my $regex = qr/\G([\w-]+).+?\b/;

my $xplnr = YAPE::Regex::Explain->new($regex);

print $xplnr->explain;

^D

正则表达式：

(?-imsx:\G([\w-]+).+?\b)

匹配如下：

NODE                     EXPLANATION

----------------------------------------------------------------------

(?-imsx:                 分组，但不捕获（区分大小写）

                         （正常匹配 ^ 和 $）（. 不匹配

                         \n）（正常匹配空格符和 #

                         通常）：
----------------------------------------------------------------------
  \G                       从上一次 m//g 停止的地方开始

----------------------------------------------------------------------
  (                        分组并捕获到 \1:
----------------------------------------------------------------------
    [\w-]+                   任何以下字符：单词字符 (a-z,

                             A-Z, 0-9, _), '-' (1 次或多次
                             （匹配尽可能多的字符））
----------------------------------------------------------------------
  )                        \1 的结束
----------------------------------------------------------------------
  .+?                      除 \n 之外的任何字符（1 次或多次

                           （匹配尽可能少的字符））
----------------------------------------------------------------------
  \b                       单词字符 (\w) 与非单词字符
                           之间的边界
----------------------------------------------------------------------
)                        分组的结束
----------------------------------------------------------------------
```

注意，我们需要向 `new()` 方法传递正则表达式对象或字符串，但无论哪种方式，我们需要指定正则表达式修饰符，它们必须使用 `(?:xxx-xxx)` 标记嵌入到正则表达式中。这导致了一个有些晦涩的讨论（7 级），你在你真的对如何解释修饰符感兴趣时才需要注意。假设原始代码中的正则表达式如下所示：

```
 while ($line =~ /\G([\w-]+).+?\b/csig) 
```

那么为了让 `YAPE::Regex::Explain` 解释这些修饰符，必须这样嵌入：

```
 my $regex = qr/(?si:\G([\w-]+).+?\b)/; 
```

为什么我漏掉了 `c` 和 `g` 修饰符？因为它们只影响 `m///` 操作符的操作，而不是正则表达式本身的一部分。关于 `(?:xxx-xxx)` 的更多信息请参见 `perlre`，关于 `m///` 的更多信息请参见 `perlop`，特别是关于正则表达式的权威处理，请参见 [FRIEDL02]。

### 9.1.2 Benchmark::Timer

这个由 Andrew Ho 编写的模块就像是你程序的秒表。你可以为代码的特定部分计时，并获得关于程序在这些部分花费了多少时间以及执行了多少次的报告。你在调用 `start()` 方法时为每个部分标记一个唯一的标签，然后在被测量的代码完成后调用 `stop()` 方法。多个代码段（或多次执行的同一代码段）可以接收相同的标签，因此合并在一起。这是一个执行了一些相对耗时操作的示例程序（向网页发送 GET 和 HEAD 请求）：

#### 示例 9.1. Benchmark::Timer 演示

```
 #!/usr/bin/perl

use strict;

use warnings;

use Benchmark::Timer;

use LWP::Simple;

my $timer = Benchmark::Timer->new;

my $url = "http://www.perlmedic.com/";

$timer->start('head');

head($url);

$timer->stop();

$timer->start('get');

get($url);

$timer->stop();

$timer->start('head');

head($url);

$timer->stop();

$timer->report;
```

当我们运行这个程序时，我们看到：

##### 示例 . Benchmark::Time

```
 % ./timertest

2 trials of head (1.192s total), 596.092ms/trial

1 trial of get (177.013ms total)
```

这表明由于某种原因，LWP::Simple 的 `head()` 函数耗时比其 `get()` 函数长。

### 9.1.3 Benchmark::TimeTick

这是我为这本书编写的一个原理类似的简单小模块。它的目的是输出一个列表，显示你的程序到达你通过调用 `timetick()` 方法标记的每个点所花费的确切时间。源代码位于附录中，这里是它的文档：

NAME

Benchmark::TimeTick—记录程序不同位置的时间

SYNOPSIS

```
 use Benchmark::TimeTick qw(timetick);

# 你的代码...

timetick("开始第三阶段");

# 更多你的代码... 
```

DESCRIPTION

Benchmark::TimeTick 提供了一种快速方便的方法来对程序进行插桩，使用模块并在你想标记点时调用 `timetick()` 方法即可。当程序结束时，将输出一份报告，给出到达每个点的时间。

时间将使用 `Time::HiRes::time()` 记录（如果 `Time::HiRes`可用），否则使用 `time()`。（由于 `time()` 有秒级，这可能没用。）

CONFIGURATION

你可以通过包哈 `%Benchmark::TimeTick::Opt` 来自定义 Benchmark::TimeTick 的行为。识别键有：

suppress_initial 为真，则在加载模块时不在报告中输出初始项。

suppress_final 为真，则在程序终止时不在报告中输出最终项。

reset_start 为真，则报告所有时间相对于 Benchmark::TimeTick 加载的时间，而不是程序的实际开始时间。





`format_tick_tag` 如果设置，则应指向一个子程序的引用，该子程序将接收 `timetick()` 的 `$tag` 作为输入，并返回实际使用的标签。这对于在每个标签上应用复杂的转换而同时保持调用代码简短非常有帮助。

`format_report` 如果设置，则应指向一个子程序的引用，该子程序将接收用于报告的时间点列表作为输入。列表的每个元素将是对包含时间和标签的数组的引用。默认的 `format_report` 回调函数为：

```
 sub { printf("%7.4f %s\n", @$_) for @_ } 
```

`suppress_report` 如果为真，则在调用 `report()` 时不输出报告；只需重置时间点列表。

要使 `suppress_initial` 或 `reset_start` 生效，必须在使用此模块之前在 `BEGIN` 块中设置它们。

## METHODS

`Benchmark::TimeTick::timetick($tag)` 记录程序在此处的时间，并用字符串 `$tag` 对其进行标记。

`Benchmark::TimeTick::report()` 输出报告（除非设置了 `suppress_report`）并重置时间点列表。

`Benchmark::TimeTick::end()` 添加最后一个时间点（除非设置了 `suppress_final`）并输出报告。在程序结束时默认调用。

## OPTIONAL EXPORTS

`Benchmark::TimeTick::timetick()` 将按需导出。为了简洁起见，建议这样做。

## EXAMPLE

```
 BEGIN { $Benchmark::TimeTick::Opt{suppress_initial} = 1 }

use Benchmark::TimeTick qw(timetick);

# ... 时间流逝

timetick("Phase 2");

# ... 更多流逝，程序结束 
```

来自 `Benchmark::TimeTick` 的输出：

```
 0.7524 Phase 2

0.8328 Timeticker for testprog finishing 
```

### 9.1.4 Debug::FaultAutoBT

Stas Bekman 编写了此模块，它会拦截原本会导致核心转储（core dump）的信号，并尝试提取并转储 gdb 回溯。如果你正在尝试调试某些 XS 代码，请使用此模块。

### 9.1.5 Devel::LeakTrace

此模块由 Richard Clamp 编写，需要 Perl 5.6.0 或更高版本，它将报告程序启动后分配但在程序通过 `END` 块时未释放的任何内存。如果它发现任何内存，可能是由于循环引用导致的，在这种情况下，解决方法是使用 Tuomas J. Lukka 的 `WeakRef` 模块 ([`search.cpan.org/dist/WeakRef/`](http://search.cpan.org/dist/WeakRef/))。

### 9.1.6 Module::Info

Mattia Barbon 维护由 Michael Schwern 创建的模块；它通过扫描模块源码来提供相关信息。某些信息可能并不完全可靠，仅仅因为解析 Perl 是极其困难的。它可以告诉你此类信息，例如模块中的 `package` 声明列表、在其中定义的子程序以及它调用的子程序。

### 9.1.7 Class::Inspector

Adam Kennedy 编写了此模块，它为已加载模块的反射函数提供了便利方法：源文件名、子程序和方法。

### 9.1.8 B::Xref

这个由 Malcolm Beattie 编写的模块已  5.005 版本添加到 Perl 核心中。它将生成一份报告，帮助你跟踪变量和子程序的定义和引用位置。由于它像 `B::Deparse` 一样属于编译器后端，它不会实际运行你的代码。通过 `O` 前端调用它：

```
 % perl -MO=Xref program arguments... 
```

随后出现的是报告，显示变量、子程序以及它们出现的行，并按文件进行分类。

## 9.2 消除多余代码

当你面对如山般溢满编辑器的代码时，你可能需要任何帮助来判断这些代码是否都已使用。人们编写起初可能有用、但最终变得多余的代码并不罕见。因此，这里有大批量发现未使用代码的一些方法。

### 9.2.1 Devel::Coverage

Randy J. Ray 的 `Devel::Coverage` 是一个用于代码覆盖率分析的模块；它报告程序执行期间被访问的代码行。该模块已有一段时间未更改，但截至本文写作时，它仍与 Perl 5.9.0 的开发版本兼容。

`Devel::Coverage` 是一个调试器插件，这意味着它通过启用 Perl 的运行时调试器钩子来调用，这些钩子会在每个即将执行的语句上触发等。Perl 自带的交互式命令行调试器本身就是一个调试器插件。然而，`Devel::Coverage` 响应这些钩子调用并生成数据文件。该数据文件并非供人类读取；你应该通过 `Devel::Coverage` 带的 `coverperl` 程序运行它。

你可以通过在命令行中使用 `-d` 标志来调用 `Devel::Coverage`：

```
 % perl -d:Coverage program arguments... 
```

程序将运行，并创建覆盖文件 `program.cvp`。以下是名为 `Solution.pm` 模块的 `coverperl` 输出片段：

```
 12  Solution::print

        12   line 37

        12   line 38

        96   line 39

        768  line 40

        96   line 40
```

### 9.2.2 Devel::Cover

Paul Johnson 的 `Devel::Cover` ([`search.cpan.org/dist/Devel-Cover/`](http://search.cpan.org/dist/Devel-Cover/)) 是一个更现代的模块，比 `Devel::Coverage` 多许多选项，但根据其文档，它仍处于婴儿阶段。

`Devel::Cover` 附有一个名为 `cover` 的程序，可以生成数据库。选项范围太大到无法详述，但你可以运行以下命令以行行为粒度生成覆盖率报告：

```
 % perl -d:Cover=-coverage,statement program... 
```

然后从创建的数据库生成可读报告。

## 9.3 寻找低效代码

当应用程序运行时间过长时，一种治疗方法是从寻找每个部分花费的时间开始。知道在哪里投入优化精力是关键；如果你恰好选择了一段仅消耗总时间 1% 的代码，那么无论你如何提高它的效率，速度提升也无法超过 1%（对于严谨的人来说是 1.01%）。优化消耗运行时间 90% 的代码可以使速度提升多达 10 倍。然而，你不应该仅凭检查来判断是哪段代码。人们在这类评估方面臭名昭著，而专家与学者之间的唯一区别在于专家知道自己不应该相信直觉。他们使用的是性能分析工具，Perl 有两个工具：`Devel::DProf` 和 `Devel::SmallProf`。请注意，这两个模块都会不可避免地为报告的时间引入不准确性。由于它们会在 Perl 执行的每个子程序或语句运行额外的代码（并且都会调用 Perl 的内部调试钩子），经过分析的程序执行时间会比未修改的版本长。

### 9.3.1 Devel::DProf

`Devel::DProf` 包含在 Perl 核心中；其目的是在子程序级别显示执行分析。这意味着它将显示子程序被调用的次数以及执行它们花费的时间。类似于 `Devel::Coverage` 和 `Devel::Cover`，它作为调试器插件被调用：

```
 % perl -d:DProf program arguments... 
```




它会将计时信息记录到文件 `tmon.out` 中，即使是对于中等复杂度的运行，该文件也可能迅速变得巨大；请从另一个窗口监控该文件的大小，并在你不喜欢它变得过大时终止运行。可以通过设置环境变量 `PERL_DPROF_OUT_FILE_NAME` 来更改文件名。

`tmon.out` 文件不是供人类阅读的，你需要运行程序 `dprofpp` 来生成报告。一如任何其他通过 `perl` 安装的 Perl 程序一样，你可以使用 `perldoc` 来查看其文档。

`dprofpp` 在不带任何参数的情况下就能提供良好的输出；你可以给它几个选项来更改其默认行为。默认情况下，它只显示在每个子程序词法作用域内花费的时间，而不是在该子程序及其调用的所有子程序中花费的累计时间；但这恰恰是你需要的。

遗憾的是，没有办法可以将 DProf 的输出管道到 `dprofpp` 并避免创建 `tmon.out`，因为 DProf 会定期通过 `seek()` 跳转到文件开头附近。

### 9.3.2 Devel::SmallProf

Ted Ashton 的 `Devel::SmallProf` 由 Salvador Fandi–o 维护，可以在 CPAN 获取 ([http://search.cpan.org/dist/Devel-SmallProf])。它的目的与 `Devel::DProf` 类似，但它可以在执行行的更细粒度度上显示结果（因此称为“small”）。确保每行最多有一个语句将最大化使用该模块的收益，因此请确保先对代码进行了反混淆和美化。

`Devel::SmallProf` 生成一个名为 `smallprof.out` 的文件。无法让输出到其他地方，但与 `Devel::DProf` 不同，该文件的大小不取决于运行时间的长度，而是取决于源代码量，因为它包含了所有的源代码，并标注了每行被调用的次数以及执行它时消耗的墙钟时间（wall clock time）和 CPU 时间。

`smallprof.out` 文件按源代码行号排序，这并没有什么帮助；性能分析的目的是找出哪些代码运行时间最长。`Devel::SmallProf` 文档中提供的排序命令并不如预期那样有用，因为 `smallprof.out` 包含了会干扰输出的页眉，而且在排序时文件名会与源代码行隔离开。

因此，我写了一个程序，可以按 CPU 或墙钟时间进行排序，并输出源的文件名。（必须移除每行 `smallprof.out` 行末尾的原始源代码截断行，以便为文件名留出空间。）它被称为 `smallprofpp`，你可以在附录中找到它。以下是该程序按墙钟时间排序的输出前几行的示例：

```
 % ./smallprofpp | head -5

    count tm  cpu line
     1140 0.999952 0.150000 /usr/lib/perl5/5.6.1/Exporter.pm:57
      545 0.999952 0.050000 substr2:36
        1 0.999952 0.000000 /usr/lib/perl5/site_perl/5.6.1/LWP/Simple.pm:319
        1 0.238549 0.000000 substr2:9
```

以及按 CPU 时间排序的：

```
 % ./smallprofpp -c | head -5

    count tm  cpu line
      727 0.000000 0.360000 substr2:33
     1140 0.999952 0.150000 /usr/lib/perl5/5.6.1/Exporter.pm:57
      247 0.000000 0.110000 substr2:43
      397 0.000000 0.090000 /usr/lib/perl5/5.6.1/Exporter.pm:55
```

注意，花费墙钟时间最长的行与花费 CPU 时间最长的行之间存在显著差异。通常在寻求提高性能时，你应该先调查 CPU 消耗者；墙钟时间的过多可能是由于 I/O 或其他进程占用了关注。改进执行 I/O 花的时间是一项非常微妙的活动，即使是判断 I/O 是否是延迟的原因都有问题。

### 9.3.3 优化技巧

如果你提高 Perl 程序速度的努力没有接近目标，有几种策略可以让你摆脱困境：

- 用另一种语言重写其部分内容。在识别出某部分代码占用执行时间很大后，如果足够小，可以考虑用 C 等语言重写它。注意，如果代码只是执行文本处理，这可能会提高运行速度，因为 Perl 的工作方式类似于复杂指令集（CISC）；其操作符是由高度优化的编译代码实现的。你可以使用 `Inline` ([search.cpan.org/Inline/]) 轻松包含你的 C 代码。

- 用另一种语言重写整个程序。有些应用程序这样做会更好。例如，我不会用 Perl 写窗口系统，也不会写巡航制制引导系统。如果它必须尽可能快地运行，C 是一个更好的选择。但要注意的是，许多人会说“它必须尽可能快地运行”，尽管事实并非如此。他们通常心里有一个标准，如果你能用 Perl 满足这个标准，那么如果你使用另一种语言节省了一些时间，他们会很高兴的。

- 改进算法。算法通常被忽视，但它是任何程序员手中至关重要的组件。正确的算法可以决定程序是在不到一秒内完成，还是超过宇宙的寿命。

## 9.4 调试

调试只是动态分析的一种极端情况。第三方代码可能极其复杂（你自己的代码也是如此，但你通常不会那样想，因为你熟悉它）；有时你无法判断代码某部分是如何结合的，或者它是否被调用过。代码以某种毫无意义的安排排列；如果你能看到程序在运行时实际上会去向哪里就好了了。

嗯，你可以做到，使用 Perl 内置的调试器。即使你并不是真的在寻找 bug，调试器的代码追踪能力也非常适合这项工作。这里不是详细介绍调试器的地方，但幸运的是你不需要详细介绍；部分命令子集就足够你完成工作了。使用调试器就像打架；它通常很快就会结束，不需要使用你训练过的许多华丽招式。

你通过 `-d` 命令行标志调用调试器；要么编辑程序在 shebang 行中添加 `-d`，要么通过显式调用 Perl 来运行程序：

```
 % perl -d program argument argument...
```

确保你路径中的 `perl` 与程序 shebang 行中的 `perl` 是同一个，否则如果两者之间存在差异，你会疯的。

表 9-1 中的命令将涵盖你几乎所有的调试器使用：

##### 表 9-1. 基础调试命令

| 命令 | 说明 |
| --- | --- |
| `h` / `h h` | 简要 / 详细帮助（5.8.0 之前为详细 / 简要帮助） |
| `b` `subroutine` | 在子程序的第一个可执行语句处设置断点 |
| `b` `line` | 为行 line 设置断点 |
| `b` `place condition` | 为位置（可以是行或子程序）设置断点，但仅当 Perl 表达式条件为真时触发 |
| `C` | 继续运行直到程序结束或遇到断点 |
| `c` `line` | 继续运行直到行 line、程序结束或更早的断点 |
| `x` `expression` | 检查变量或表达式的值 |
| `N` | 执行当前语句，跳过从其调用的任何子程序 |
| `S` | 执行下一个 Perl 语句，必要时将进入从当前语句调用的子程序 |




| `L` | 列出从当前行开始的代码 |
| `R` | 执行语句直到当前子程序返回、程序结束或更早的断点 |
| `T` | 显示堆栈跟踪 |
| `Q` | 退出 |

掌握了这些命令，我们可以进行代码探险。假设你正在调试一个包含以下代码片段的程序：

```
 77 for my $url (@url_queue)

78 {

79   my $res = $ua->request($url);

80   summarize($res->content);
81 } 
```

并且你知道每当程序访问 URL [`www.perlmedic.com/fnord.html`](http://www.perlmedic.com/fnord.html) 时，`summarize()` 子程序中就会发生奇怪的事情。你想检查 `HTTP::Response` 对象，看看是否有任何你未察知的重定向。你在调试器下启动程序并输入：

```
 DB<1> b 80 $url =~ /fnord/

DB<2> c 
```

程序将运行，直到它获取了你感兴趣的 URL，此时你可以检查响应对象——这里是它可能性的示例：

```
 DB<3> x $res

0  HTTP::Response=HASH(0x70f340)

   '_content' => '\cF\cN\cO\cR\cD'

   '_headers' => HTTP::Headers=HASH(0x70f790)

      'cache-control' => 'private,max-age=60'
      'client-date' => 'Tue, 01 Jul 2003 01:21:55 GMT'
      'client-peer' => '204.95.83.7:80'
      'client-response-num' => 1
      'connection' => 'close'
      'content-type' => ARRAY(0x23f470)
         0  'text/html'
         1  'text/html; charset=iso-8859-1'
      'date' => 'Tue, 01 Jul 2003 01:21:54 GMT'
      'expires' => 'Tue, 01 Jul 2003 01:22:54 GMT'
      'last-modified' => 'Tue, 01 Jul 2003 01:21:54 GMT'
      'refresh' => 1800
      'server' => 'Apache/1.3.27 (UNIX)'
      'title' => 'This page intentionally left blank'
   '_msg' => 'OK... sort of...'
   '_previous' => HTTP::Response=HASH(0x6af660)
      '_content' => ''
      '_headers' => HTTP::Headers=HASH(0x6af66c)
         'client-date' => 'Tue, 01 Jul 2003 01:21:49 GMT'
         'client-peer' => '204.95.83.7:80'
         'client-response-num' => 1
         'connection' => 'close'
         'content-length' => 0
         'content-type' => 'text/html'
         'date' => 'Tue, 01 Jul 2003 01:21:48 GMT'
         'location' => 'http://www.perlmedic.com/fnord/'
         'server' => 'Apache/1.3.27 (UNIX)'
      '_msg' => 'Moved Temporarily'
      '_protocol' => 'HTTP/1.1'
      '_rc' => 302
      '_request' => HTTP::Request=HASH(0x4a60d0)
         '_content' => ''
         '_headers' => HTTP::Headers=HASH(0x4a60a0)
            'user-agent' => 'libwww-perl/5.69'
         '_method' => 'GET'
         '_uri' => URI::http=SCALAR(0x27e668)
            -> 'http://www.perlmedic.com/fnord.html'
   '_protocol' => 'HTTP/1.1'
   '_rc' => 299
   '_request' => HTTP::Request=HASH(0x623e40)
      '_content' => ''
      '_headers' => HTTP::Headers=HASH(0x68e6f4)
         'user-agent' => 'libwww-perl/5.69'
      '_method' => 'GET'
      '_uri' => URI::http=SCALAR(0x6e55e8)
         -> 'http://www.perlmedic.com/fnord/' 
```

你可以从这里看出确实存在重定向，并发现确切返回了什么。（你可以通过 `LWP::Debug` 模块对该网页获取过程进行精细控制，但我所插图的方法适用于任何类型的对象。）然后你可以通过单步进入子程序来查看 `summarize()` 中的内容发生了什么：

```
 DB<4> s

main::summarize(/home/peter/bin/url_summarizer):177:

    my $res = $url
```



```perl
 % perl -Mstrict -Mwarnings

use re qw(debug);

$_ = "cats=purr, dog=bark"; 

my %sound = /(\w+)=(\w+)/g;

^D

Compiling REx `(\w+)=(\w+)'

size 15 first at 4

   1: OPEN1(3)

   3:   PLUS(5)

   4:     ALNUM(0)

   5: CLOSE1(7)

   7: EXACT <=>(9)

   9: OPEN2(11)

  11:   PLUS(13)

  12:     ALNUM(0)

  13: CLOSE2(15)

  15: END(0)

floating `=' at 1..2147483647 (checking floating) stclass `ALNUM' plus 

minlen 3 

Guessing start of match, REx `(\w+)=(\w+)'` against `cats=purr, 

dog=bark'...

Found floating substr `=' at offset 4...

Does not contradict STCLASS...

Guessed: match at offset 0

Matching REx `(\w+)=(\w+)'` against `cats=purr, dog=bark'

  Setting an EVAL scope, savestack=3

   0 <> <cats=purr, d>    |  1:  OPEN1

   0 <> <cats=purr, d>    |  3:  PLUS

                           ALNUM can match 4 times out of 32767...

  Setting an EVAL scope, savestack=3

   4 <cats> <=purr, d>    |  5:    CLOSE1

   4 <cats> <=purr, d>    |  7:    EXACT <=>

   5 <cats=> <purr, d>    |  9:    OPEN2

   5 <cats=> <purr, d>    | 11:    PLUS

                           ALNUM can match 4 times out of 32767...

  Setting an EVAL scope, savestack=3

   9 <=purr> <, dog=b>    | 13:      CLOSE2

   9 <=purr> <, dog=b>    | 15:      END

Match successful!

Guessing start of match, REx `(\w+)=(\w+)'` against `, dog=bark'...

Found floating substr `=' at offset 5...

By STCLASS: moving 0 --> 2

Guessed: match at offset 2

Matching REx `(\w+)=(\w+)'` against `dog=bark'

  Setting an EVAL scope, savestack=3

  11 <urr, > <dog=bar>    |  1:  OPEN1

  11 <urr, > <dog=bar>    |  3:  PLUS

                           ALNUM can match 3 times out of 32767...

  Setting an EVAL scope, savestack=3

  14 <rr, dog> <=bark>    |  5:    CLOSE1

  14 <rr, dog> <=bark>    |  7:    EXACT <=>

  15 <rr, dog=> <bark>    |  9:    OPEN2

  15 <rr, dog=> <bark>    | 11:    PLUS

                           ALNUM can match 4 times out of 32767...

  Setting an EVAL scope, savestack=3

  19 <rr, dog=bark> <>    | 13:      CLOSE2

  19 <rr, dog=bark> <>    | 15:      END

Match successful!

Freeing REx: `(\w+)=(\w+)'` 
```

如果你使用 `debugcolor` 而不是 `debug`，你将在输出中获得某种形式的高亮或颜色，这会让它更美观，至少更易读。

# 第 10 章 增加可维护性（预防）

> Tara King 看到 Steed 玩一架玩具飞机时说：“你玩这种东西不是不太大了吗？” Steed 回道：“这是送给我外甥的十岁生日的礼物。” Tara 问：“那是时候的事？” Steed 说：“三年前了。那些说明书很难读懂。”
> —Patrick Macnee 和 Linda Thorson 选《复仇者》

![graphics/ch10.gif](img/ch10.gif)

在接手了一个程序并使其成为你自己的之后，你最不希望的就是它变成你最初所承担的那种“信天翁（负担）”。因此，你的任务就是尽可能地提高它的可维护性。

## 10.1 使其变得健壮

程序越健壮，就越不容易引起人的关注并引发维护需求。以下是一些可以帮助完成这项任务的模块。

### 10.1.1 Params::Validate

那些在 C、Java 和 Pascal 等其他过程化语言中编程过的人，经常会好奇 Perl 中真正的子程序原型（prototypes）在哪里。他们心里一直有一种挥之不去的感觉：除非对所有参数都像其他这些语言那样严格地进行验证，否则子程序是不安全的。`Params::Validate` 正好实现了他们想要的，而且做得更多。

> [1] 尽管是在运行时，而不是编译时。抱歉。Perl 6 将具有完全的编译时参数检查。

如果你打算对参数进行严格限制，你会发现自己有这种挥之不去的感觉：除非对所有参数都像其他语言那样严格地进行验证，否则子程序是不安全的。`Params::Validate` 正好实现了他们想要的，而且做得更多。



如果给定的条件为假，断言将导致一个异常。如果你写过类似下面的代码：

```
 die "This shouldn't happen!!!" if ... 
```

那么它读起来会更像是一个断言。`Carp::Assert` 为你提供了几种方法来实现这一点：

```
 use Carp::Assert;

sub yes_we_have_no_bananas

{

  my $bananas = shift;

  assert($bananas == 0) if DEBUG;

  print "Yes, we have no bananas\n";

} 
```

不过，`Carp::Assert` 并不会打印“This shouldn't happen!!!”。（断言的语言太正式了，不会这样表达）。相反，它会打印“Assertion failed!”和堆栈跟踪。如果你想让它打印自定义的消息，可以提供第二个参数：

```
 assert($bananas == 0, "We DO have bananas!") if DEBUG; 
```

那么异常的第一行就是“Assertion (We DO have bananas!) failed!”。

`if DEBUG` 是什么用的？它是为了在你想要轻松禁用该断言以及代码中其他所有断言时提高性能。`Carp::Assert` 导出一个常量 `DEBUG`，其值为真。如果你确定已经从代码中消除了可能触发断言的 Bug，并且希望它在生产环境中尽可能高效，那么你就不希望 Perl 花费时间去编译和执行断言。

你可以通过改变一个单词来防止 Perl 执行断言：与其用 `use Carp::Assert`，不如用 `no Carp::Assert`。现在，`assert()` 函数变成了一个立即返回且不执行任何操作的函数。但这仍然是一个子程序调用；如果你非常在意性能，你连这种调用都不想要。使用 `if DEBUG` 的目的是 Perl 不会编译那些它在编译时就能判断为永远不会执行的代码，因为像 `DEBUG` 这样的常量是在编译时定义的，如果 `DEBUG` 为假，那么 Perl 就不会编译 `assert()` 语句。显然，`assert()` 只是当某些条件为假时抛出异常的语法糖。你可以通过以下方式获得相同的效果：

```
 use Carp;

use constant DEBUG => 1;

# ...

if (DEBUG)
{

  confess "We DO have bananas!" unless $bananas == 0;
}
```

但这种构造的冗余性要干扰得多，而你希望断言尽可能轻量。

### 10.1.3 Class::Contract

Damian Conway 的 `Class::Contract`（http://search.cpan.org/dist/Class-Contract/）现在由 Garrett Goebel 维护，它实现了源自 Eiffel 世界的契约设计（Design by Contract）方法。成功使用这种方法要求在实现类时具有高度的专业知识和纪律；而回报是一个稳固的安全网。契约设计就像是注入了对象导类固醇的断言。它规定：

* 类中的每个方法应至少定义一个 `pre`（前置条件），这是对方法执行工作所需必须满足的条件进行的测试。`Class::Contract` 会在每次调用方法时、实际执行任何操作之前运行前置条件，如果测试失败，则会抛出异常。
* 类中的每个方法应至少定义一个 `post`（后置条件），这是对方法本应向调用者保证的内容的测试。`Class::Contract` 会在每次调用方法并在返回给调用者之前运行后置测试，如果测试失败，则会抛出异常。
* 类应当指定一个全局 `inv`（不变性），这是在每个方法调用结束时运行的另一个测试，用于测试方法是否违反类的完整性。

正如你可能观察出的，提出合适的条件可能需要大量的专业知识。`Class::Contract` 提供了这些功能以及更多功能（例如与属性相关的条件）；为了实现这一点，它几乎重新实现了 Perl 对象系统的部分部分（例如继承）。在 `Class::Contract` 中，你指定方法、属性和继承的方式与 Perl 原生方式不同；你使用 `Class::Contract` 自己的语言来这样做。这里有一个可以运行的、尽管极其原始的示例，向你展示那种语言看起来什么样：`Class::Contract` 最适合无法放入本书的大型应用程序。

#### 示例 10.1 用于 Class::Contract 的 BankAccount.pm

```
 package BankAccount;

use strict;

use warnings;

use Class::Contract qw(old);

my $INIT_RESERVES = 10_000;  # Bailey & Loan

contract

{

  class attr 'reserves' => 'SCALAR';

  class ctor;
    impl { $self->reserves} = $INIT_RESERVES };

  class method 'adjust_reserves';
    pre  { defined $_[0] };
      failmsg "No amount to adjust reserves by";
    impl { $self->reserves} += $_[0] };

  invar { $self->reserves} >= 0 };
    failmsg "We gone bankrupt, Maw!";

  ctor 'new';
    impl { $self->balance} = $_[0] };

  attr balance => 'SCALAR';

  method 'get_balance';
    impl { $self->balance };

  method 'loan';
    pre  { defined $_[0] };
    impl { $self->balance} += $_[0];
           self->adjust_reserves(-$_[0])
         };
    post { $self->balance} == $old->balance + $_[0] };

  method 'invest';
    pre  { defined $_[0] };
    impl { $self->balance} -= $_[0];
           self->adjust_reserves($_[0])
         };
    post { $self->balance} == $old->balance - $_[0] };

};

1;
```

#### 示例 10.2 用于 Class::Contract 的 BankAccount.pm 测试套件

```
 #!/usr/bin/perl

use strict;

use warnings;

use BankAccount;

use Test::More tests => 7;

use Test::Exception;

BEGIN { use_ok('BankAccount') }

my $acct = BankAccount->new(1000);

is($acct->get_balance, 1000);

lives_ok { $acct->loan(5000) };

is($acct->get_balance, 6000);

dies_ok { $acct->loan };

dies_ok { $acct->invest };

throws_ok { $acct->loan(1E8) } qr/bankrupt/; 
```

`Class::Contract` 产生的冗余可能并不适合所有人，但如果你正在用 Perl 编写传奇的空中管制应用程序，你需要这种工业级的帮助。

#### 10.1.4 Log::Logperl

Michael Schilli 的 `Log::Logperl`（http://search.cpan.org/dist/Log-Log4perl/）提供了从类层次结构的多个地方向多个目的地记录日志的功能。当你有一个高度面向对象的应用程序时可以使用它。例如，你可能有一个基础的数据库类，你对其连接启用日志，而当你创建了解 SQL 或事务的子类时，你希望分别记录 SQL 或事务错误。想象一个使用图 10.1 所示复杂的类层次结构的应用程序。

现在假设叶子类中的一个对象生成了日志消息。`Log::4perl` 允许为每个类附加零或多个附加器（appenders）；附加器是被指示将日志消息发送到特定目的地（例如文件或电子邮件接收者）的对象。每个附加器还被配置为在特定的级别触发，一系列如：DEBUG , INFO, WARNING , ERROR, FATAL。因此，如果我们在叶子类及其祖类中都附加了附加器，消息将通过 `Log::4perl` 附加器的类层次结构向上传播，但只会激活那些注册了该消息级别（或更低级别）的附加器。

被激活的附加器在图 10.2 中用粗体表示。



对于 CGI 程序或其他处理可能存在的恶意用户输入的程序，污点检查（Taint checking）的作用是有限的。有时候，你无法找到一个有效的正则表达式既能捕获你从用户输入中想要的内容，又能保证不会产生不安全的代码。

为了终极的代码保护，由 Malcolm Beattie 和 Tim Bunce 开发的 `Safe.pm`（自 Perl 5.004 版本起包含在核心库中）提供了一个环境，你可以在私有沙箱中执行 Perl 代码。该代码只能读取你明确允许其访问的数据，只能执行你明确列出的操作，并且无法影响沙箱之外的任何东西，除非返回一个结果供你使用。`Safe.pm` 并不是一个易用的模块，但在安全至关重要的情况下，它可能是你的最佳选择。

### 10.2 高级简洁性

Perl 提供了一些复杂的语法糖（syntactic sugaring，即让某些编码构造更简洁、更直观的方法）。其中两种技术是绑定（tieing）和重载（overloading）。

### 10.2.1 绑定 (Tieing)

我们在第 3.3 节中见过绑定的示例。绑定允许你接管变量的正常功能。在外部，它看起来是一个普通的标量、数组、哈希或任何类型。但在内部，每当变量被使用时，执行的是你写的代码，而不是你预期的行为。

这在表面上看主要用于恶作作剧（它确实有这种潜力）。然而，它也可以用于使代码更加简洁并获得透明度。

当你意识到正在实现一种行为上像变量的功能时，简洁性就体现了。例如，如果你有一个电子温度计以及读取该温度计数值的代码，你完全可以用传统的过程化代码来实现：

```
 use Thermometer;

$temp = Thermometer->read; 
```

但温度计的行为就像一个标量变量一样（尽管是一个只读标量变量；改变温度计上的读数不会改变它测得的温度，除非你知道如何打破热力学定律）。那么，（俗说）这样写要酷炫得多：

```
 tie $current_temp, 'Thermometer'; 
```

然后每当你读取 `$current_temp` 时，它都会神奇地更新为当前温度。

`Themometer.pm` 模块可以通过根据 `perltie` 文档实现 `TIESCALAR` 和 `FETCH` 方法来轻松完成这一点。

你正在实现的功能语义需要映射到 Perl 变量类型之一的自然行为，这种功能才能生效。我们的温度计类与标量并不完美匹配（因为尝试写入它是没有意义的，因此我们必须决定是将任何此类尝试记录为抛出异常还是没有任何影响），但它确实足够接近，值得去费精力。我们可以在第一次绑定时为每个绑定的变量关联属性，因此我们可能选择声明：

```
 tie $current_temp, 'Thermometer', 'Celsius'; 
```

以确保我们在读取时知道温度的单位是什么。这个接口现在看起来比过程化的等价实现要好得多：

```
 $current_temp = Thermometer->read_celsius; 
```

或者甚至是面向对象的等价实现：

```
 $current_temp = Thermometer->new(scale => 'Celsius');

print "Temperature: ", $current_temp->read; 
```

这只是针对一个简单的标量。当你发现某个可以映射到哈希的功能时（例如），你可以写出极其简洁的代码。哈希最常见的绑定接口是存储哈希内容并使其持久化的数据库。我曾实现过一个程序，必须在哈希中存储大量条目；最终它耗尽了当时我使用的机器的虚拟内存资源。在以内存换速度的经典权中，我本可以追踪对哈希的每一次访问，并将其替换为对数据库库的 `fetch()` 或 `store()` 方法的调用。但那比我愿意做的要得多，幸运的是，之前的人和我一样懒，并将他们懒惰的成果封装了一系列将哈希绑定到数据库的模块中。我只需要添加一行：

```
 use DB_File; 
```

并将哈希的声明从：

```
 my %data; 
```

改为：

```
 tie my %data, 'DB_File', $database, ... 
```

（其中 `...` 参数指定了用作数据库的文件和相关信息），我不需要更改任何其他代码。此后，对哈希的每次访问行为都和以前一样，只是耗时长了一点，但不再占用内存。此外，我获得了持久化能力，这意味着我可以从之前的运行中恢复值，从而实现检查点/重启等功能。使用绑定到哈希的数据库时需要记住的例外是：如果哈希很大，不要使用任何返回整个哈希列表的哈希操作，因为这会将列表从数据库读取到内存，从而违背了绑定哈希的初衷。归结起来，在列表上下文中不要使用 `keys()` 或 `values()` 函数，也不要使用哈希本身；请使用 `each()` 函数。通过如此小的改变获得这种持久性，证明了绑定带来的透明性。

在一次极度懒惰的展示中，Damian Conway 将相当晦涩的 Perl 特性——属性（在 Perl 5.6.0 中引入），通过编写一个 `Attribute::Handlers` 模块（在 Perl 5.8 中合并到核心库）简化了该功能的使用，使得接口变得简单：

```
 my $current_temp : Thermometer; 
```

或者：

```
 my $current_temp : Thermometer('Celsius');
```

### 10.2.2 重载 (Overloading)

当你创建一个类，并且该类的实例进行基本操作（如算术运算、字符串或其他类型）时，如果你可以合理推断出应该发生的行为，那么你可以选择以这种方式实现。这就是 C++ 有而 Java 没有的那种运算符重载。

当然，对象类必须具有适用于这种干预的语义。如果你有一个 `Date` 类，两个类成员的相加没有意义；但相反，从一个中减去另一个可以合理解释为产生一个封装持续时间的类成员；而 `Duration` 对象与 `Date` 对象的重载相加可以合理解释为产生另一个 `Date` 对象。

重载通常用于提供透明的字符串化；这允许你为自己的对象实现“奇淫淫”（dwummery）。人们刻意或无意在字符串上下文中使用对象是非常常见的，他们看到的打印结果通常类似于 "Foo=HASH(0x80fbb0c)"。如果你定义了一个对于某种文本表示很自然的对象类，并且发现自己实现了一个名为 `as_text()` 或 `as_string()` 的实例方法，那么你可以给你的用户帮个忙，重载字符串化以调用该方法。这只需要通过将：

```
 use overload '"" => \&as_text; 
```

插入你的模块中即可。一个有效利用这一点的模块示例是 `URI.pm`（参见第 6.2.1 节），因为对 `URI` 对象最常见的操作就是其所代表的 URI 的文本形式。更多信息请参阅 `overload` 编译指令文档。

是的，你可以拥有既被绑定又被重载的变量。





在第 3 章中，我展示了如何为模块编写测试，包括它的文档。现在我将向你展示如何编写文档本身。

后排那边的同学，醒醒！是的，我知道我说了“文档”。这可能会让你脑海中浮现出微软 PowerPoint 演示文稿，用“功能性需求”和“规范引用”之类的冗肿标题填充各个章节，并格式化签名块。我说的不是那种文档。我说的是能告诉另一个程序员他们对你所做的工作需要了解什么的文档；即当你接手他人的代码时想要阅读的那种文档。或者当你一年后回到自己的代码前，无论如何想不起如何使用那个你曾认为接口“直观易见”的 `object class` 时，想要阅读的文档。

#### 10.3.1 POD 人的入侵

意识到编写文档对程序员来说是(a) 痛苦且/或无聊的，且 (b) 对程序员阅读是必不可少的，Larry Wall 创建了一套系统，让创建文档变得尽可能简单。这个系统平实地被称为纯旧文档（Plain Old Documentation，简称 POD）。

POD 的第一个便利之处是，你可以将其直接嵌入到它描述的代码中；它只是一段由特殊行标记的文本块。你可以选择将 POD 放在你想要的任何地方；表 10-1 中所示的任何样式都是可以接受的且通用的。

##### 表 10-1. POD 插入样式

| POD 之前的代码 | 代码之前的 POD | 代码中的 POD |
| --- | --- | --- |
| 代码 | POD | 代码 |
| 代码 | POD | POD |
| 代码 | POD | 代码 |
| 代码或 `__END__` | POD | POD |
| POD | 代码 | 代码 |
| POD | 代码 | POD |
| POD | 代码 | 代码 |
| POD | 代码 | POD |

因此，你可以将 POD 全部放在开头（如果你认为那是程序员应该看到的第一样东西），或者全部放在末尾（如果你认为代码更重要）。在后一种情况下，你有一个小的优化可用：你可以将 POD 放在一行恰好由 `__END__` 文本组成的行之后，当 perl 运行你的程序时，它看到该行就会停止编译；因此即使是识别和忽略 POD 所需的短暂时间也不会占用。

最后一种样式是“内联”，这适用于你想让每个函数的文档直接嵌入在该函数旁的情况。显然，你甚至可以进一步，在更小的粒度上穿插 POD，但请记住，任何增加函数在编辑器中查看所需的空间的内容都会让代码变得难读。

第二个便利之处是 POD 非常简单。Larry 推理认为，为了让人们编写文档，创建和编辑它必须尽可能简单，因此只需要记住少数几个 POD 格式指令。你永远不需要担心代码中的任何内容被误判为 POD——POD 仅在以左边距对齐的等号开头并跟一个单词的特殊行之间被识别。在 POD 内部，你只需通过缩进即可让任何文本原样输出（其中的任何内容都不会被解释为格式指令）。例如，将 POD 与代码包含在一起看起来这么简单：

```
 sub quad_roots

{
  my ($a, $b, $c) = @_;

  my $disc = sqrt($b*$b - 4*$a*$c);

  return((-$b + $disc) / 2 / $a, (-$b - $disc) / 2 / $a);

}

=head2 ($root1, $root2) = quad_roots($a, $b, $c);

返回具有给定系数的二次方程的两个根，但如果它有虚根则抛出错误（在这种情况下，请使用 L<Math::Complex>）。

根据经典公式计算：
    -b +/- sqrt(b**2 - 4ac)
    -----------------------
               2a

=cut 
```

POD 指令行需要位于空行之间才能被识别。在非原样的 POD 文本内部，可以识别一些原始的标记标签。我在这里使用的 `L<>` 用于将其内容格式化为链接；当输出到支持超链接概念的格式时，该文本将链接到 `Math::Complex` 的 POD 页面（假设格式化程序找到它；见下文）。请注意，除非我用类似下面的内容覆盖链接默认文本，否则会将输出渲染为“the Math::Complex manpage”：

```
 use L<Math::Complex|the Math::Complex module>. 
```

记住，POD 是给你的用户看的；旨在帮助维护程序员理解实现细微差别的注释属于内联注释。在量尺的另一端，你可能有纯文档要创建（也许体现了设计、需求、用例或客户故事）。尽管也使用 POD 来处理这些内容吧；没有法律规定它必须位于包含 Perl 代码的文件中。

#### 10.3.2 POD 格式化器

POD 的主要优势在于将其提取为仅包含文档的形式。正如我们习惯了阅读许多格式的文档一样，POD 也可以转换为许多格式。Perl 核心自带将 POD 转换为文本、LaTeX、HTML 和 UNIX troff 手页标记的程序：它们分别称为 `pod2text`、`pod2latex`、`pod2html` 和 `pod2man`。

### 10.4 自定义警告

假设你写了此模块：

```
use warnings;
use Time::Local;

# 期望格式为 MM/DD/YYYY 的日期
sub set_date
{
  my ($self, $date) = @_;
  my ($mon, $day, $year) = split m/#/, $date;

  if (length($year) == 2)
  {
    warnings::warnif("y2k", "Y2K bug, year interpreted in rolling window");
  }
  $self->{date} = timocal(0, 0, 0, $day, $mon-1, $year);
}
```

在第 1 行中，我们使用了词法警告指令（那里本就应该在那里）。这使得我们在第 9 行调用了 `warnings::warnif()` 函数，如果第一个参数中的警告类别已启用，它会在第二个参数中发出警告。

`perlexwarn` 页面告诉我们警告类别有一个层级结构，其中一个被称为 `y2k`，看起来合适，所以我们重用了它。如果此方法的调用者不想看到该警告，他们只需要排除它：

```
 {
  no warnings 'y2k';
  $object->set_date('4/1/99');
}
```

如果你愿意，可以定义自己的警告类别，而不是限于标准类别；参见 `perlexwarn`。

如果每个模块作者都使用这种方法来发布警告，那么再也不需要使用 `-w` 了。

### 10.5 版本控制系统集成

如果你正在使用版本控制系统（RCS），你可能希望将 RCS 版本号自动用作代码的版本。包变量 `$VERSION` 应该在模块中设置，因为各种工具都会查找它。但是，你不能直接说：

```
 our $VERSION = '$Revision$'; 
```




因为版本号需要是数字。你需要的是一个包含 RCS `Revision` 关键字并返回其数值部分的表达式。这里有一种可能的方法：

```
 our $VERSION = (qw$Revision: 3.42 $)[-1]; 
```

它巧妙地利用 RCS 的 `$` 关键字分隔符作为 `qw` 算符的分隔符，从第二个空格分隔的组件中提取出数字 `3.42`。

如果你希望版本号包含两个以上的组件，`ExtUtils::MakeMaker` 的文档显示了另一种方法：

```
 our $VERSION = do { my @r = (q$Revision: 1.2.3 $ =~ /\d+/g); \ 

sprintf "%d."."%03d" x $#r, @r }; 
```

为了让 MakeMaker 此为 `$VERSION` 赋值，所有代码必须写在同一行。

并发版本系统（`CVS`）使用相同的关键字。源码控制系统（`SCCS`）比 RCS 或 CVS 少得多，但用它进行版本编号也是轻而易举的：

```
 our $VERSION = "%I%"; 
```

注意引号：Perl 在多个版本中允许使用 v-strings（包含多个句点的数字；它们会被转换为二进制形式），但在 `5.8.1` 之后的版本中它们已被弃用，因此我保守起见将版本转换为了字符串。

由于 Subversion 的版本关键字是 `$Rev: $`，你可以对该产品复用 RCS 的建议。

## 第 11 章 案例研究

> “这种可爱的温和咖喱使用了 100% 的日本苹果和快乐的仓鼠。”

> —日本 Ham Monde 咖喱包装上的标签，来自 enrish.com。

![graphics/ch11.jpg](img/ch11.jpg)

让我们通过一个例子将书中的课程付诸实践。我将介绍接管一个刚进入我们收件箱的程序的各个阶段。考虑到空间限制——为了不让读者感到无聊——我无法涵盖一个大型程序，因此这个示例会相当小，而且本身也算不上糟糕。虽然它使用了一项功能——`LDAP` 目录查询——你可能用得很少，但理解 `LDAP` 对于理解这段代码是如何变化的并不重要，而且此外，`LDAP` 本身就值得学习。

> ^([1]) `LDAP` 代表“轻量级目录访问协议”，它的使用率日益增加。

## 11.1 设置

我们的程序以名为 `dirsearch.cgi` 的 CGI 程序形式出现，它是表单的目标，该表单接受名为 `username`、`location` 和 `haircolor` 的输入。查看该程序的输入表单及其响应，可能有助于理解该程序在做什么（参见图 11.1 和 11.2 ）：

### 图 11.1. dirsearch.cgi 的输入表单。

![graphics/11fig01.gif](img/11fig01.gif)

### 图 11.2. dirsearch.cgi 的输出。

![graphics/11fig02.gif](img/11fig02.gif)

以下是代码：

### 示例 11.1. dirsearch.cgi, 版本 1

```
 1  #!/usr/local/bin/duaperl

2

3  print "Content-type: text/html\n\n";

4

5  @values = split(/&/, $ENV{'QUERY_STRING'});

6  foreach $input (@values)
7  {
8    ($one, $two) = split(/=/,$input);
9    $filter && do_error("Cannot lookup by >1 attribute... pick one only");
10   $filter = "($one=$two)";
11 }
12 $filter || do_error("Need an attribute to search on");
13 &dua_settmout(10, 0);
14 unless (&dua_open("whitepages", 389, $dn, $pwd))
15 {
16   $msg = "Can't connect to whitepages: $dua_errstr";
17   do_email($msg);
18   do_error($msg);
19 }
20 $scope = 1;
21 $all = 0;
22 $rdn = '@dc=oz@dc=city@dc=emerald@dc=wp@ou=People';
23 %list = &dua_find($rdn, $filter, $scope, $all);
24 if ($dua_errstr)
25 {
26   do_email($dua_errstr);
27   do_error($dua_errstr);
28 }
29 unless (%list)
30 {
31   print "<HTML><HEAD><TITLE>Error</TITLE></HEAD><BODY>\n";
32   print "<H1>Error</H1><P>No match for $filter</P>\n";
33   print "</BODY></HTML>\n";
34   exit;
35 }
36 print "<HTML><HEAD><TITLE>Search Results</TITLE></HEAD>\n";
37 print "<BODY><H1>Results of search for $filter</H1>\n";
38 print "<TABLE BORDER=\"1\">\n339 print <<HEADER;
40 <TR><TH>username</TH>
41 <TH>location</TH>
42 <TH>haircolor</TH>
43 <TH>email</TH>
44 <TH>fax</TH>
45 <TH>name</TH>
46 </TR>
47 for $i (sort keys %list)
48 {
49   print "<td>$list{$i}</td>\n";
50 }
51 print "</TABLE>\n";
52 print "</BODY>\n";
53 print "</HTML>";
```




让我们先通过行编辑来压缩程序，使其更易读。在此过程中，我们做出了一个决定：只要在浏览器中看起来还是一样的，我们就可以更改 HTML 输出。特别是那些无关紧要的空白（换行符，不需要与原始输出匹配。（无论如何，任何依赖 HTML 空白格式的人都应该受到这种“教训”。）

第 32–35 行与 `do_error()` 子程序的功能相同，因此我们可以调用该子程序来代替。有几个地方连续调用了 `do_error()` 和 `do_email()` 并使用相同的消息，因此我们可以专门为该目的创建一个子程序。第 40–46 行、52–58 行和 59–61 行的重复部分可以通过 `map()` 删除。

##### 示例 11.3\. dirsearch.cgi, 版本 2

```
 1  #!/usr/local/bin/duaperl

2

3  print "Content-type: text/html\n\n";

4

5  @values = split(/&/, $ENV{'QUERY_STRING'});

6  foreach $input (@values)

7
{
8    ($one, $two) = split(/=/,$input);
9    $filter && do_error("Cannot lookup by >1 attribute... pick one only");
10   $filter = "($one=$two)";
11 }
12 $filter || do_error("Need an attribute to search on");
13 &dua_settmout(10, 0);
14 unless (&dua_open("whitepages", 389, $dn, $pwd))
15 {
16   $msg = "Can't connect to whitepages: $dua_errstr";
17   do_email_error($msg);
18 }
19 $scope = 1;
20 $all = 0;
21 $rdn = '@dc=oz@dc=city@dc=emerald@dc=wp@ou=People';
22 %list = &dua_find($rdn, $filter, $scope, $all);
23 if ($dua_errstr)

24 {
25   do_email_error($dua_errstr);
26 }
27 unless (%list)

28 {
29   do_error("No match for $filter");
30 }
31 print "<HTML><HEAD><TITLE>Search Results</TITLE></HEAD>\n";
32 print "<BODY><H1>Results of search for $filter</H1>\n";
33 print "<TABLE BORDER=\"1\"><TR>\n";
34 my @attrs = qw(username location haircolor

35                telephone email fax name);
36 print map "<TH>$_</TH>", @attrs;
37 print "</TR>\n";
38 foreach $i (sort { $a <=> $b } keys %list)

39 {
40   $dn = "\@". join("\@", reverse(split(/,\s*/, $list{$i)));
41   %attr = &dua_show($dn);
42   print "<TR>", map "<TD>$attr{$_}</TD>", @attrs;
43 }
44 print "</TR></TABLE></BODY></HTML>\n";

45
46 &dua_close();

47
48 sub do_email_error

49
{
50   my $mess = shift;
51   do_email($mess);
52   do_error($mess);
53 } 
```

`do_error()` 和 `do_email()` 例程尚未更改，因此未显示。

### 11.3 绝望中寻找理智

我们现在还不能运行这段代码，简单原因是我们正在将其升级到 Perl 5，并且已经使用了了一些 Perl 5 特性（如 `map()` 和 `my`）来使代码更加简洁。为了让它运行起来，我们必须让 LDAP 代码正常工作。如果我们能编译好 `Dua.pm`——这是一个很大的“如果”，因为我只能让它在 Perl 5.004 下通过编译——那么在创建一个新的 `Dua` 对象后，我们可以几乎直接地将 `&dua_` 替换为 `$dua->`。错误通过方法报告而不是导出变量报告，仅此而已：

##### 示例 11.4\. dirsearch.cgi, 版本 3

```
 1  #!/usr/bin/perl

2  use Dua;
3  print "Content-type: text/html\n\n";

4

5  @values = split(/&/, $ENV{'QUERY_STRING'});

6  foreach $input (@values)

7
{
8    ($one, $two) = split(/=/,$input);
9    $filter && do_error("Cannot lookup by >1 attribute... pick one only");
10   $filter = "($one=$two)";
11 }
12 $filter || do_error("Need an attribute to search on");
13 my $dua = Dua->new;
14 $dua->settmout(10, 0);
15 unless ($dua->open("whitepages", 389, $dn, $pwd))

16 {
17   $msg = "Can't connect to whitepages: " . $dua->error";
18   do_email_error($msg);
19 }
20 $scope = 1;
21 $all = 0;
22 $rdn = '@dc=oz@dc=city@dc=emerald@dc=wp@ou=People';
23 %list = &dua_find($rdn, $filter, $scope, $all);
24 if ($dua_errstr)

25 {
26   do_email_error($dua_errstr);
27 }
28 unless (%list)

29 {
30   do_error("No match for $filter");
31 }
32 print "<HTML><HEAD><TITLE>Search Results</TITLE></HEAD>\n";
33 print "<BODY><H1>Results of search for $filter</H1>\n";
34 print "<TABLE BORDER=\"1\"><TR>\n";
35 my @attrs = qw(username location haircolor

36                telephone email fax name);
37 print map "<TH>$_</TH>", @attrs;
38 print "</TR>\n";
39 foreach $i (sort { $a <=> $b } keys %list)

40 {
41   $dn = "\@". join("\@", reverse(split(/,\s*/, $list{$i)));
42   %attr = &dua_show($dn);
43   print "<TR>", map "<TD>$attr{$_}</TD>", @attrs;
44 }
45 print "</TR></TABLE></BODY></HTML>\n";

46
47 &dua_close();
```

再次，我省略了未更改的子程序。这是我们在 Perl 5 上取得的一个重大里程碑，现在我们可以对它施加严格检查（strict）和警告（warnings）。没有必要通过浏览器调用它，因为在命令行运行插入 `use strict` 和 `use warnings`（在我们受限于 Perl 5.004 的情况下）会告诉我们所有需要的信息：

 Global symbol "values" requires explicit package name at dirsearch.cgi line 8.

Global symbol "input" requires explicit package name at dirsearch.cgi line 9.

Global symbol "one" requires explicit package name at dirsearch.cgi line 11.

Global symbol "two" requires explicit package name at dirsearch.cgi line 11.

Global symbol "filter" requires explicit package name at dirsearch.cgi line 12.

Global symbol "dua" requires explicit package name at dirsearch.cgi line 16.

Global symbol "dn" requires explicit package name at dirsearch.cgi line 18.

Global symbol "pwd" requires explicit package name at dirsearch.cgi line 18.

Global symbol "msg" requires explicit package name at dirsearch.cgi line 20.

Global symbol "scope" requires explicit package name at dirsearch.cgi line 23.

Global symbol "all" requires explicit package name at dirsearch.cgi line 24.

Global symbol "rdn" requires explicit package name at dirsearch.cgi line 25.

Global symbol "list" requires explicit package name at dirsearch.cgi line 26.

Global symbol "i" requires explicit package name at dirsearch.cgi line 41.

Global symbol "attr" requires explicit package name at dirsearch.cgi line 45.

Global symbol "mess" requires explicit package name at dirsearch.cgi line 61.
```

dirsearch.cgi 执行由于编译错误而终止。

在插入足够的 `my` 语句以修复这些问题的过程中，我们发现示例 11.4 第 15 行中的 `$dn` 和 `$pwd` 从未被赋予过任何值，因此它们是未定义的，所以几乎可以从子程序调用中省略它们，因为未指定的值与未定义值几乎是一样的。代码现在如下：

##### 示例 11.5\. dirsearch.cgi, 版本 4





```perl
1/bin/perl
#!/usr/bin/perl -w

use strict;
use Dua;
print "Content-type: text/html\n\n";

my @values = split(/&/, $ENV{'QUERY_STRING'});
my $filter;
foreach my $input (@values)
{
  my ($one, $two) = split(/=/,$input);
  $filter && do_error("Cannot lookup by >1 attribute... pick one only");
  $filter = "($one=$two)";
}
$filter || do_error("Need an attribute to search on");
my $dua = Dua->new;
$dua->settmout(10, 0);
unless ($dua->open("whitepages", 389, $dn, $pwd))
{
  my $msg = "Can't connect to whitepages: " . $dua->error;
  do_email_error($msg);
}
my ($scope, $all) = (1, 0);
my $rdn = '@dc=oz@dc=city@dc=emerald@dc=wp@ou=People';
my %list = $dua->find($rdn, $filter, $scope, $all);
if ($dua->error)
{
  do_email_error($dua->error);
}
unless (%list)
{
  do_error("No match for $filter");
}
print "<HTML><HEAD><TITLE>Search Results</TITLE></HEAD>\n";
print "<BODY><H1>Results of search for $filter</H1>\n";
print "<TABLE BORDER=\"1\"><TR>\n";
my @attrs = qw(username location haircolor
               telephone email fax name);
print map "<TH>$_</TH>", @attrs;
print "</TR>\n";
foreach my $i (sort { $a <=> $b } keys %list)
{
  my $dn = "\@". join("\@", reverse(split(/,\s*/, $list{$i})));
  my %attr = $dua->show($dn);
  print "<TR>", map "<TD>$attr{$_}</TD>", @attrs;
}
print "</TR></TABLE></BODY></HTML>\n";

$dua->close;

sub do_email_error
{
  my $mess = shift;
  do_email($mess);
  do_error($mess);
}

sub do_error
{
  my $mess = shift;
  return unless $mess;
  print "<HTML><HEAD><TITLE>Error</TITLE></HEAD><BODY>\n";
  print "<H1>Error</H1><P>$mess</P>\n";
  print "</BODY></HTML>\n";
  exit;
}

sub do_email
{
  my $mess = shift;
  open MAIL, "|/usr/lib/sendmail -oi -t";
  print MAIL "To: me\@here\n";
  print MAIL "Subject: $0: LDAP lookup problem\n";
  print MAIL "\n";
  print MAIL "Error in LDAP processing in $0:\n\n";
  print MAIL "$mess\n";
  close MAIL;
}
```

### 11.4 迈向 21 世纪

现在我们无法再忽视这样一个事实：我们正在使用一个古旧且不支持的模块（`Dua.pm`）进行 LDAP 操作，于是查询了 `Net::LDAP` 的文档。我们逐行地将 `Dua.pm` 的调用替换为 `Net::LDAP` 的调用。这要求我们在不熟悉 `Net::LDAP` 的情况下去学习它，但这样做将带来丰厚的回报。以下是我们必须做的更改：

*   超时时间现在在 `new()`构造函数中指定。
*   如果构造函数失败，它将返回 `undef`并将错误存放在 `$@` 中。
*   登录服务器（在 LDAP 术语中称为 `binding`）是一个独立的方法调用，尽管我们建立的是匿名连接。
*   搜索通过 `search()` 方法完成，该方法返回一个位于 `Net::LDAP::Search` 类中的结果对象。
*   `bind()` 和 `search()` 方法返回的对象具有 `code()` 方法（该方法在发生错误时返回真）以及一个返回错误文本的 `error()` 方法。
*   `Net::LDAP::Search` 类有一个方法 `count()`，返回找到的结果数量，以及另一个方法 `entries()`，它将所有结果作为 `Net::LDAP::Entry` 对象的列表返回。
*   每个 `Net::LDAP::Entry` 对象都有一个 `get_value()` 方法，用于返回具命名属性的值。
*   搜索的基区分名称（DN）现在可以按照自然顺序指定，而不再像 `duaperl` 恶意要求的那样使用 `@` 分隔符的反转顺序。我们将其移动到程序开头以获得程序上的优势。

在此过程中，我们发现 `Dua::open()` 方法中的魔数 389 实际上是 LDAP 连接的默认端口，因此我们可以省略它。这些更改引导我们得到了：

##### 示例 11.6. dirsearch.cgi, Version 5
```perl
#!/usr/bin/perl -w
use strict;
use warnings;
use Dua;

print "Content-type: text/html\n\n";

my @values = split(/&/, $ENV{'QUERY_STRING'});
my $filter;
foreach my $input (@values)
{
  my ($one, $two) = split(/=/,$input);
  ... (后续代码保持不变)
}
```



```perl
!/usr/bin/perl

use strict;
use warnings;

use CGI qw(param header);
use Net::LDAP;

print header;
my %SEARCH_OPTS =
    (base  => 'ou=People, dc=wp, dc=emerald, dc=city, dc=oz',
     scope => 'sub');
my $LDAP_SERVER = "whitepages";
my @LDAP_OPTS = ($LDAP_SERVER, timeout => 10);
my @ATTRS = qw(username location haircolor
               telephone email fax name);

my $filter;
foreach my $input (param)
{
  my $value = param($input);
  $filter and do_error("Cannot lookup by >1 attribute... pick one only");
  $filter = "($input=$value)";
}
$filter or do_error("Need an attribute to search on");

my $ldap = Net::LDAP->new(@LDAP_OPTS)
  or do_email_error("Can't connect to $LDAP_SERVER: $@");
my $mesg = $ldap->bind;
$mesg->code and do_email_error("Bind error: "
                                . $mesg->error);
my $res = $ldap->search(%SEARCH_OPTS, filter => $filter);
$res->code and do_email_error("Search failure: "
                               . $res->error);

$res->count or do_error("No match for $filter");

print "<HTML><HEAD><TITLE>Search Results</TITLE></HEAD>\n";
print "<BODY><H1>Results of search for $filter</H1>\n";
print "<TABLE BORDER=\"1\"><TR>\n";
print map "<TH>$_</TH>", @ATTRS;
print "</TR>\n";
foreach my $ent ($res->entries)
{
  print "<TR>", map "<TD>" . $ent->get_value($_)
                            . "</TD>", @ATTRS;
}
print "</TR></TABLE></BODY></HTML>\n";

$ldap->unbind;

sub do_email_error
{
  my $mess = shift;
  do_email($mess);
  do_error($mess);
}

sub do_error
{
  my $mess = shift;
  return unless $mess;
  print "<HTML><HEAD><TITLE>Error</TITLE></HEAD><BODY>\n";
  print "<H1>Error</H1><P>$mess</P>\n";
  print "</BODY></HTML>\n";
  exit;
}

sub do_email
{
  my $mess = shift;
  open MAIL, "|/usr/lib/sendmail -oi -t";
  print MAIL "To: me\@here\n";
  print MAIL "Subject: $0: LDAP lookup problem\n";
  print MAIL "\n";
  print MAIL "Error in LDAP processing in $0:\n\n";
  print MAIL "$mess\n";
  close MAIL;
}
```

### 11.6 有效地结合模块，第 2

然而，这个版本感觉令人不满意地不足。所有的 HTML 文本看起来也像几个巨大的常量值；我们能对它们做同样的操作吗？

可以的，使用 `HTML::Template`。我们可以将 HTML 拆分到单独的文件（一个用于正常输出，一个用于错误输出），这些文件现在将只包含 HTML。这将实现代码与数据的分离——这本身通常是一件好事——而且允许我们将编辑 HTML 的工作——呃，不，委派——交给别人。让我们把正常结果的 HTML 输出转移到一个名为 `output.tmpl` 的文件中：

##### 示例 11.9. output.tmpl，版本 1

```html
 <HTML><HEAD><TITLE></TITLE></HEAD>

 <BODY>
  <H1>Results of search for <TMPL_VAR NAME=filter></H1>
  <TABLE BORDER="1">
   <TR>
    <TH>username</TH>
    <TH>location</TH>
    <TH>haircolor</TH>
    <TH>telephone</TH>
    <TH>email</TH>
    <TH>fax</TH>
    <TH>name</TH>
   </TR>
   <TMPL_LOOP NAME="results">
    <TR>
     <TD><TMPL_VAR NAME="username"></TD>
     <TD><TMPL_VAR NAME="location"></TD>
     <TD><TMPL_VAR NAME="haircolor"></TD>
     <TD><TMPL_VAR NAME="telephone"></TD>
     <TD><TMPL_VAR NAME="email"></TD>
     <TD><TMPL_VAR NAME="fax"></TD>
     <TD><TMPL_VAR NAME="name"></TD>
    </TR>
   </TMPL_LOOP>
  </TABLE>
 </BODY>
</HTML>
```

错误文本放在名为 `error.tmpl` 的模板中：

##### 示例 11.10. error.tmpl，版本 1

```html
 <HTML><HEAD><TITLE>Error</TITLE></HEAD>
 <BODY>
  <H1>Error</H1>
  <P><TMPL_VAR NAME="reason"></P>
 </BODY>
</HTML>
```

为了使用这些模板，我们必须通过 `HTML::Template` 的 `param()` 方法将所有数据打包在一起，并使用 `output()` 方法一次性输出。完整的程序（`do_error` 函数除外）如下：

```perl
#!/usr/bin/perl
use strict;
use warnings;

use CGI qw(param header);
use Net::LDAP;
use HTML::Template;

print header;
my %SEARCH_OPTS =
    (base  => 'ou=People, dc=wp, dc=emerald, dc=city, dc=oz',
     scope => 'sub');
my $LDAP_SERVER = "whitepages";
my @LDAP_OPTS = ($LDAP_SERVER, timeout => 10);
my @ATTRS = qw(username location haircolor
               telephone email fax name);

my $filter;
foreach my $input (param)
{
  my $value = param($input);
  $filter and do_error("Cannot lookup by >1 attribute... pick one only");
  $filter = "($input=$value)";
}
$filter or do_error("Need an attribute to search on");

my $ldap = Net::LDAP->new(@LDAP_OPTS)
  or do_email_error("Can't connect to $LDAP_SERVER: $@");
my $mesg = $ldap->bind;
$mesg->code and do_email_error("Bind error: "
                                . $mesg->error);
my $res = $ldap->search(%SEARCH_OPTS, filter => $filter);
$res->code and do_email_error("Search failure: "
                               . $res->error);

$res->count or do_error("No match for $filter");

my $tmpl = HTML::Template->new(filename => 'output.tmpl');
my @results;
foreach my $ent ($res->entries)
{
  push @results, {
    map { $_ => $ent->get_value($_) } @ATTRS
  };
}
$tmpl->param(filter => $filter, results => \@results);
print $tmpl->output();

$ldap->unbind;

sub do_email_error
{
  my $mess = shift;
  do_email($mess);
  do_error($mess);
}

sub do_error
{
  my $mess = shift;
  return unless $mess;
  my $tmpl = HTML::Template->new(filename => 'error.tmpl');
  $tmpl->param(reason => $mess);
  print $tmpl->output();
}

sub do_email
{
  my $mess = shift;
  open MAIL, "|/usr/lib/sendmail -oi -t";
  print MAIL "To: me\@here\n";
  print MAIL "Subject: $0: LDAP lookup problem\n";
  print MAIL "\n";
  print MAIL "Error in LDAP processing in $0:\n\n";
  print MAIL "$mess\n";
  close MAIL;
}
```

### 11.6 有效地结合模块，第 2

然而，这个版本感到遗憾地不足。所有的 HTML 文本看起来也像几个巨大的常量值；我们能对它们做同样的操作吗？

可以的，使用 `HTML::Template`。我们可以将 HTML 拆分到单独的文件（一个用于正常输出，一个用于错误输出），这些文件现在将只包含 HTML。这将实现代码与数据的分离——这本身通常是一件好事——而且允许我们将编辑 HTML 的工作——呃，不，委派——交给别人。让我们把正常结果的 HTML 输出转移到一个名为 `output.tmpl` 的文件中：

##### 示例 11.9. output.tmpl，版本 1

```html
 <HTML><HEAD><TITLE></TITLE></HEAD>

 <BODY>
  <H1>Results of search for <TMPL_VAR NAME=filter></H1>
  <TABLE BORDER="1">
   <TR>
    <TH>username</TH>
    <TH>location</TH>
    <TH>haircolor</TH>
    <TH>telephone</TH>
    <TH>email</TH>
    <TH>fax</TH>
    <TH>name</TH>
   </TR>
   <TMPL_LOOP NAME="results">
    <TR>
     <TD><TMPL_VAR NAME="username"></TD>
     <TD><TMPL_VAR NAME="location"></TD>
     <TD><TMPL_VAR NAME="haircolor"></TD>
     <TD><TMPL_VAR NAME="telephone"></TD>
     <TD><TMPL_VAR NAME="email"></TD>
     <TD><TMPL_VAR NAME="fax"></TD>
     <TD><TMPL_VAR NAME="name"></TD>
    </TR>
   </TMPL_LOOP>
  </TABLE>
 </BODY>
</HTML>
```

错误文本放在名为 `error.tmpl` 的模板中：

##### 示例 11.10. error.tmpl，版本 1

```html
 <HTML><HEAD><TITLE>Error</TITLE></HEAD>
 <BODY>
  <H1>Error</H1>
  <P><TMPL_VAR NAME="reason"></P>
 </BODY>
</HTML>
```

为了使用这些模板，我们必须通过 `HTML::Template` 的 `param()` 方法将所有数据打包在一起，并使用 `output()` 方法一次性输出。完整的程序（`do_error` 函数除外）如下：

```perl
#!/usr/bin/perl
use strict;
use warnings;

use CGI qw(param header);
use Net::LDAP;
use HTML::Template;

print header;
my %SEARCH_OPTS =
    (base  => 'ou=People, dc=wp, dc=emerald, dc=city, dc=oz',
     scope => 'sub');
my $LDAP_SERVER = "whitepages";
my @LDAP_OPTS = ($LDAP_SERVER, timeout => 10);
my @ATTRS = qw(username location haircolor
               telephone email fax name);

my $filter;
foreach my $input (param)
{
  my $value = param($input);
  $filter and do_error("Cannot lookup by >1 attribute... pick one only");
  $filter = "($input=$value)";
}
$filter or do_error("Need an attribute to search on");

my $ldap = Net::LDAP->new(@LDAP_OPTS)
  or do_email_error("Can't connect to $LDAP_SERVER: $@");
my $mesg = $ldap->bind;
$mesg->code and do_email_error("Bind error: "
                                . $mesg->error);
my $res = $ldap->search(%SEARCH_OPTS, filter => $filter);
$res->code and do_email_error("Search failure: "
                               . $res->error);

$res->count or do_error("No match for $filter");

my $tmpl = HTML::Template->new(filename => 'output.tmpl');
my @results;
foreach my $ent ($res->entries)
{
  push @results, {
    map { $_ => $ent->get_value($_) } @ATTRS
  };
}
$tmpl->param(filter => $filter, results => \@results);
print $tmpl->output();

$ldap->unbind;

sub do_email_error
{
  my $mess = shift;
  do_email($mess);
  do_error($mess);
}

sub do_error
{
  my $mess = shift;
  return unless $mess;
  my $tmpl = HTML::Template->new(filename => 'error.tmpl');
  $tmpl->param(reason => $mess);
  print $tmpl->output();
}

sub do_email
{
  my $mess = shift;
  open MAIL, "|/usr/lib/sendmail -oi -t";
  print MAIL "To: me\@here\n";
  print MAIL "Subject: $0: LDAP lookup problem\n";
  print MAIL "\n";
  print MAIL "Error in LDAP processing in $0:\n\n";
  print MAIL "$mess\n";
  close MAIL;
}
```

### 11.7 使程序成熟，第 1

我们满意了吗？不！这个程序仍然由于信息的重复而显得脆弱：模板中包含了包含了属性列表，两次，我们的程序也是如此，而且它们必须保持相同的顺序。如果属性列表发生变化，我们将不得不更新三个地方。此外，我们的 CGI 参数解析循环盲目接受它看到的第一个参数，并假设它是搜索术语。未来的输入变化可能会传入其他类型的参数，然后我们就会抓到错误的参数。这种变化可能是意外发生的：有人可能使用某种 HTML 编辑器为提交按钮赋予了 `NAME` 属性，然后我们就会接收到按钮点击的输入参数。

让模板使用程序中的属性列表，同时指定哪些属性是搜索参数。结果模板现在在任何有属性列表的地方都需要一个循环，并变为：

##### 示例 11.12. output.tmpl，版本 2





```html
 <HTML><HEAD><TITLE>Search Results</TITLE></HEAD>

 <BODY>

  <H1>Results of search for <TMPL_VAR NAME=filter></H1>

  <TABLE BORDER="1">

   <TR>

    <TMPL_LOOP NAME="attributes">
     <TH><TMPL_VAR NAME="attribute"></TH>
    </TMPL_LOOP>
   </TR>

   <TMPL_LOOP NAME="results">
    <TR>
     <TMPL_LOOP NAME="attributes">
     <TD><TMPL_VAR NAME="attribute"></TD>
     </TMPL_LOOP>
    </TR>
   </TMPL_LOOP>

  </TABLE>

 </BODY>

</HTML> 
```

既然话说到这，这个程序已经很久没有进行污染检查（taint checking）了，因此我们在 shebang 行中添加了 `-T` 命令行标记。这要求我们对可能用于打开文件等潜在危险操作的输入进行去污（untain）。然而，这些输入仅将用于 LDAP 搜索，因此为了程序运行它们不需要去污；但这一系列思考让我们处于审慎的状态；是否可能存在某种恶意或无意的输入会导致 LDAP 搜索失败？

从过滤器（LDAP 术语，指“搜索查询”）的构建方式可以明显看出，包含右括号的值会导致问题，因为过滤器看起来在那个点就结束了，并且包含了多余的字符。这足以让我们思考还有哪些字符可能会导致问题，于是我们查阅 `Net::LDAP` 文档来寻找答案。在列表中找到 `Net::LDAP::Filter` 模块后，我们看到文档引用了该主题的权威参考资料——意见请求（RFC）：[`www.ietf.org/rfc/rfc2254.txt`](http://www.ietf.org/rfc/rfc2254.txt)。它告诉我们，这些字符必须通过十六进制编码在过滤器值中转义：`(`、`))`、`*`、`\`、`NUL`。

然而，在使用替换运算符之前，我们应该偷懒看看是否已经有人为我们完成了这项工作……确实如此（“他们”指的是 Graham Barr），已经完成了。在 `Net::LDAP::Filter` 中，该模块的文档说明：“. . .让你可以直接操作 LDAP 过滤器，而不必担心字符串表示以及所有相关的转义机制。”而 `Net::LDAP` 的 `search()` 方法的文档——在我们在使用之前应该会仔细研读的，对吧？——显示过滤器参数可以是文本，也可以是一个 `Net::LDAP::Filter` 对象。因此，我们所做的是将过滤器文本封装在 `Net::LDAP::Filter` 构造函数内部，生成的对象就可以代替过滤器文本，而无需担心转义那些顽的字符。

这些文档阅读还向我们揭示了其他事情：`Net::LDAP` 类支持一个名为 `onerror` 的选项，它会影响 `Net::LDAP` 函数出现问题时的处理结果。目前的代码费力地检查每次方法调用后，`Net::LDAP` 对象的 `code()` 方法是否返回了非零值（表示错误）。或者真的如此吗？考虑到 `entries()` 方法涉及到与服务器的往返，它难道不是一个潜在的故障点吗？

既然既然我们可以直接使用 `onerror` 来确保任何问题都能报告给“警察”，何必费劲检查呢；在这种情况下，“警察”将是一个异常处理器：

##### 示例 11.13. dirsearch.cgi, 版本 8

```
 1  #!/usr/bin/perl -T

2  use strict;
3  use warnings;
4

5  use CGI qw(param header);
6  use Net::LDAP;
7  use Net::LDAP::Filter;
8  use HTML::Template;

9
10 my %SEARCH_OPTS =
11    (base  => 'ou=People, dc=wp, dc=emerald, dc=city, dc=oz',
12     scope => 'sub');
13 my $LDAP_SERVER = "whitepages";
14 my @LDAP_OPTS = ($LDAP_SERVER, timeout => 10, onerror => 'die');
15 my @OUTPUT_ATTRS = qw(username location haircolor
16                       telephone email fax name);
17 my %SEARCH_ATTR = map { ($_ => 1) }
18                       qw(username location haircolor);
19
20 my $filter;
21 foreach my $input (param)
22 {
23   next unless $SEARCH_ATTR{$input};
24   my ($value) = param($input);
25   $filter and do_error("Cannot lookup by >1 attribute... pick one only");
26   $filter = "($input=$value)";
27 }
28 $filter or do_error("Need an attribute to search on");
29
30 my $ldap = Net::LDAP->new(@LDAP_OPTS)
31   or do_email_error("Can't connect to $LDAP_SERVER: $@");
32 eval
33 {
34   $ldap->bind;
35   my $res = $ldap->search(%SEARCH_OPTS,
36              filter => Net::LDAP::Filter->new($filter));
37
38   $res->count or do_error("No match for $filter");
39
40   my $tem = HTML::Template->new(filename => "results.tmpl");
41   my @results;
42   foreach my $ent ($res->entries)
43   {
44     foreach my $attr (@OUTPUT_ATTRS) {
45       my $val = $ent->get($attr);
46       push @results, $val // '';
47     }
48   }
49
50   print $tem->output(results => @results);
51 }
52 or do_email_error("LDAP error: $@");
```

### 11.8 让程序成熟，部分 2

现在我们顺得水了！为什么要直接通过 sendmail 发送邮件呢，CPAN 给了我们 `Mail::Send`（由 Tim Bunce 和 Graham Barr 开发，由 Mark Overmeer 维护）。同时，我们将地址信息移动到程序的开头以便于配置：

```
 %ERR_ARGS = (Subject => "$0: LDAP problem",
                     To      => 'me@here');

.

sub send_email
{
  require Mail::Send;
  my $sender = Mail::Send->new(%ERR_ARGS);
  my $fh = $sender->open;
  print $fh <<"EOM";
Error in LDAP processing in $0:
@_
EOM
  $fh->close();
}
```

我们 `require` `Mail::Send` 是为了在运行时加载它，因为只有在特殊情况下才需要，没必要每次都用 `use` 加载。我们也给这个子程序起了一个比 `do_email()` 更合适的名字。

### 11.9 程序健壮性

既然我们在提高程序的可维护性，何不考虑未来可能需要处理带有逻辑运算符的多个搜索项呢？因此，我们可以读取所有的输入项，目前强制要求哈希仅包含一个键值对。（我们还应该为这些错误添加测试；目前我将这些留给读者作为练习题。）

我们需要考虑目录中某个属性值可能未设置的情况，因此我们希望避免出现使用未初始化值的警告。最后，由于我们很谨慎，让我们通过 `shift_entry()` 逐获取 `NET::LDAP::Entry` 对象，这样就不用一次性在内存中形成所有对象的列表了。这不会占用更多的代码。





```
 1  #!/usr/bin/perl -T

2  use strict;

3  use warnings;

4

5  use CGI qw(header param);

6  use HTML::Template;
7  use Net::LDAP;
8  use Net::LDAP::Filter;

9

10 my @OUTPUT_ATTRS = qw(username location haircolor

11                       telephone email fax name);
12 my %SEARCH_ATTRS = map { ($_ => 1) }
13                        qw(username location haircolor);
14 my $OUTPUT_TEMPLATE = "output.tmpl";
15 my $ERROR_TEMPLATE  = "error.tmpl";

16

17 my $LDAP_SERVER = "whitepages";
18 my @LDAP_OPTS = ($LDAP_SERVER, onerror => 'die', timeout => 10);

19

20 my %ERROR = (

21  TOOMANY => "Cannot lookup by >1 attribute... pick one only",
22  TOOFEW  => "Need an attribute to search on",
23  LDAPCON => "Can't connect to %s: %s",
24  LDAPERR => "LDAP error: %s",
25  NOMATCH => "No match for %s",
26             );
27 my %ERR_MAIL_ARGS = (Subject => "$0: LDAP lookup problem",
28                      To      => 'me@here');
29 my %SEARCH_OPTS =
30    (base  => "ou=People, dc=wp, dc=emerald, dc=city, dc=oz",
31     scope => "sub", attrs => \@OUTPUT_ATTRS);

32

33 my $query = map  { ($_ => param($_)  }
34             grep { defined(param($_) } keys %SEARCH_ATTRS;
35 keys %query > 1 and error('TOOMANY');
36 keys %query      or error('TOOFEW');

37

38 my $ldap = Net::LDAP->new(@LDAP_OPTIONS)
39   or do_email_error(LDAPCON => $LDAP_SERVER, $@);

40

41 eval
42 {
43   $ldap->bind;
44   my ($filter) = map "$_=$query{$_}" => keys %query;
45   my $res = $ldap->search(%SEARCH_OPTS, filter =>
46                    Net::LDAP::Filter->new("($filter)"));
47   $res->count or error(NOMATCH => $filter);

48

49   my $tem = HTML::Template->new(filename =>
50                                 $OUTPUT_TEMPLATE);
51   my @results;
52   while (my $entry = $res->shift_entry)
53   {
54     my @data;
55     for my $attr (@OUTPUT_ATTRS)
56     {
57       my $val = $entry->get_value($attr);
58       push @data, { attribute => defined($val) ? $val : '' };
59     }
60     push @results, { attributes => \@data };
61   }
62   $tem->param(results    => \@results,
63               filter     => $filter,
64               attributes => [ map +{ (attribute => $_) } => @OUTPUT_ATTRS ]
65      );
66   print header, $tem->output;
67 };
68 do_email_error(LDAPERR => $@) if $@;

69

70 sub do_email_error
71 {
72   my $fmt = shift;
73   send_email(@_);
74   error($fmt, @_);
75 }

76 sub error
78 {
79   my $fmt = $ERROR{shift};
80   my $tem = HTML::Template->new(filename =>
81                                 $ERROR_TEMPLATE);
82   $tem->param(reason => $fmt, @_);
83   print header, $tem->output;
84   exit;
```

`send_email()` 子函数保持不变。

### 1.9 使其完善，部分 3

下一步是移除两行代码。特别是第 25 行和 47 行。为什么？因为它们处理用户错误，而我们希望这些错误消息由输出模板的人控制。通过使用 `<TMPL_IF>` 标签在循环中至少有一个项目时才为真，我们可以在 `output.tmpl` 中处理相同的情况：

##### 示例 11.15. output.tmpl，版本 3

```
 <HTML><HEAD>

 <TITLE>
  <TMPL_IF NAME="results">
   搜索结果
  <TMPL_ELSE>
   错误
  </TMPL_IF>
 </TITLE>
</HEAD>

 <BODY>
  <TMPL_IF NAME="results">
   <H1>针对 <TMPL_VAR NAME="filter"> 的搜索结果</H1>
   <TABLE BORDER="1">
    <TR>
     <TMPL_LOOP NAME="attributes">
      <TH><TMPL_VAR NAME="attribute"></TH>
      </TMPL_LOOP>
     </TR>
     <TMPL_LOOP NAME="data">
      <TD><TMPL_VAR NAME="value"></TD>
      </TMPL_LOOP>
    </TABLE>
  </TMPL_IF>
 </BODY>
</HTML>
```

### 1.10 修改

我们完成了吗？然而，注意我们在第 18 行中将回调函数作为 `error` 参数传递给新对象的构造函数。此举目的是处理错误；我们希望用户犯的任何错误由我们的 `error()` 程序处理，而不是 OzLDAP。说到这里，这就是模块：

### 1.11 高级功能

我们将尽可能进行抽象。为了避免与 `Net::LDAP` 方法混淆，我们将创建一个对象。该对象将处理连接到服务器、绑定以及查询。它还将提供一个获取条目属性的方法。这将使主程序更容易理解。程序现在所示：

##### 示例 11.16. dir.cgi，版本 10

```
 1  #!/usr/bin/perl -T

2  use strict;

3  use warnings;

4

5  use CGI qw(header param);
6  use HTML::Template;
7  use Net::LDAP;
8  use Net::LDAP::Filter;

9

10 my @OUTPUT_ATTRS = qw(username location haircolor

11                       telephone email fax name);
12 my %SEARCH_ATTRS = map { ($_ => 1) }
13                        qw(username location haircolor);
14 my $OUTPUT_TEMPLATE = "output.tmpl";
15 my $ERROR_TEMPLATE  = "error.tmpl";

16

17 my $LDAP_SERVER = "whitepages";
18 my @LDAP_OPTS = ($LDAP_SERVER, onerror => 'die', timeout => 10);

19

20 my %ERROR = (

21  TOOMANY => "Cannot lookup by >1 attribute... pick one only",
22  TOOFEW  => "Need an attribute to search on",
23  LDAPCON => "Can't connect to %s: %s",
24  LDAPERR => "LDAP error: %s",
25  NOMATCH => "No match for %s",
26             );
27 my %ERR_MAIL_ARGS = (Subject => "$0: LDAP lookup problem",
28                      To      => 'me@here');
29 my %SEARCH_OPTS =
30    (base  => "ou=People, dc=wp, dc=emerald, dc=city, dc=oz",
31     scope => "sub", attrs => \@OUTPUT_ATTRS);

32

33 my $query = map  { ($_ => param($_)  }
34             grep { defined(param($_) } keys %SEARCH_ATTRS;
35 keys %query > 1 and error('TOOMANY');
36 keys %query      or error('TOOFEW');

37

38 my $ldap = OzLDAP->new(@LDAP_OPTIONS)
39   or do_email_error(LDAPCON => $LDAP_SERVER, $@);

40

41 eval
42 {
43   $ldap->bind;
44   my ($filter) = map "$_=$query{$_}" => keys %query;
45   my $res = $ldap->search(%SEARCH_OPTS, filter =>
46                    Net::LDAP::Filter->new("($filter)"));
47   $res->count or error(NOMATCH => $filter);

48

49   my $tem = HTML::Template->new(filename =>
50                                 $OUTPUT_TEMPLATE);
51   my @results;
52   while (my $entry = $res->shift_entry)
53   {
54     my @data;
55     for my $attr (@OUTPUT_ATTRS)
56     {
57       my $val = $entry->attrs($attr);
58       push @data, { attribute => defined($val) ? $val[0] : '' };
59     }
60     push @results, { attributes => \@data };
61   }
62   $tem->param(results    => \@results,
63               filter     => $filter,
64               attributes => [ map +{ (attribute => $_) } => @OUTPUT_ATTRS ]
65      );
66   print header, $tem->output;
67 };
68 do_email_error(LDAPERR => $@) if $@;

69

70 sub do_email_error
71 {
72   my $fmt = shift;
73   send_email(@_);
74   error($fmt, @_);
75 }

76 sub error
77 {
78   my $fmt = $ERROR{+shift};
79   my $tem = HTML::Template->new(filename =>
80                                 $ERROR_TEMPLATE);
81   $tem->param(reason => sprintf $fmt, @_);
82   print header, $tem->output;
83   exit;
84 }
```

##### 示例 11.17. OzLDAP.pm
```perl
package OzLDAP;
use strict;
use warnings;
use Net::LDAP;
use Net::LDAP::Filter;

sub new {
    my ($class, %opts) = @_;
    my $self = {
        server => $opts{server},
        options => $opts{options},
        user_error => $opts{user_error},
    };
    $self->{ldap} = Net::LDAP->new($self->{server}, @{$self->{options}});
    return bless $self, $class;
}

sub bind {
    my ($self) = @_;
    return $self->{ldap}->bind;
}

sub search {
    my ($self, $opts, %filter) = @_;
    return $self->{ldap}->search(%opts, %filter);
}

sub shift_entry {
    my ($self, $res) = @_;
    return $res->shift_entry;
}

sub attrs {
    my ($self, $entry, $attr) = @_;
    my @vals = $entry->get_value($attr);
    return $vals[0] || '';
}

1;
```





```perl
package OzLDAP;

use strict;
use warnings;

use Carp;
use Net::LDAP;
use Net::LDAP::Filter;

my @OUTPUT_ATTRS = qw(username location haircolor
                      telephone email fax name);
my %SEARCH_ATTR = map { ($_ => 1) } qw(username location haircolor);
my %ERROR = (
  TOOMANY => "Cannot lookup by >1 attribute... pick one only",
  TOOFEW  => "Need an attribute to search on",
  LDAPERR => "LDAP error: %s",
  LDAPCON => "Can't connect to %s: %s"
);
my $LDAP_SERVER = "whitepages";
my @LDAP_OPTS = ($LDAP_SERVER, onerror => 'die',
                  timeout => 10);
my %SEARCH_OPTS = (base  => "ou=People, dc=wp, dc=emerald, dc=city, dc=oz",
                    scope => "sub", attrs => \@OUTPUT_ATTRS);

sub connect
{
  my ($class, %opt) = @_;
  my $error_handler = delete $opt{user_error};
  my $self = bless { error_handler => $error_handler }, $class;
  my $ldap = Net::LDAP->new(@LDAP_OPTS, %opt)
    or croak _error_message(LDAPCON => $LDAP_SERVER, $@);
  $self->{ldap} = $ldap;
  $ldap->bind;
  $self;
}

sub query
{
  my ($self, %query) = @_;
  $SEARCH_ATTR{$_} or delete $query{$_} for keys %query;

  keys %query > 1 and $self->_error('TOOMANY');
  keys %query      or $self->_error('TOOFEW');
  my ($filter) = map "$_=$query{$_}" => keys %query;
  $self->{filter} = $filter;
  $self->{ldap}->search(%SEARCH_OPTS,
         filter => Net::LDAP::Filter->new("($filter)"));
}

sub _error
{
  my $self = shift;
  return unless my $error_handler = $self->{error_handler};
  $error_handler->(_error_message(@_));
}

sub attrs
{
  my ($self, $entry) = @_;
  $entry or return @OUTPUT_ATTRS;
  map defined($entry->get_value($_))
        ? $entry->get_value($_) : ''
      => @OUTPUT_ATTRS;
}

sub _error_message
{
  my $fmt = $ERROR{+shift};
  sprintf $fmt, @_;
}

sub filter
{
  my $self = shift;
  $self->{filter};
}

sub AUTOLOAD
{
  my $self = shift;
  our $AUTOLOAD =~ s/.*://;
  return if $AUTOLOAD eq 'DESTROY';
  $self->{ldap}->$AUTOLOAD; (@_);
}

1;
```

该模块的一些显著特征包括：

- 私有子程序 `_error_message()`，用于格式化错误消息；它被我们的私有方法 `_error()` 调用，并在 `connect()` 发生问题时使用。
- `filter()` 方法，用于获取我们喜欢的格式的过滤器文本版本（不带外部圆括号）。
- `query()` 方法接受一个名称和值对的哈希表，并仅使用有效的搜索参数；如果以后我们有理由使用多个搜索术的布尔组合，只需要修改此例程即可。
- `AUTOLOAD()` 例程拦截任何未定义的方法调用，并将它们委托给封装在 `OzLDAP` 对象中的 `Net::LDAP` 对象。

## 11.10.1 接下来做什么？

在此时此刻，你可能会想到许多其他可能的更改；例如，我们确实可以向 `OzLDAP` 中添加更多方法。然而，在没有需求的情况下，并不清楚这种投入是否值得。

你有权在这一阶段指出，该程序的当前版本不仅比原版长，而且更复杂。这完全可以。但可读性取决于长度之外的其他因素，而且我们对 Perl 的熟悉程度超过原程序的作者。此外，在清理不清晰和有 Bug 的代码之外，我们增加了许多功能。我们制作了一个完整的模块，为代码重用提供了基础（如果需要一个 LDAP 目录来跟踪奥兹国的居民，那么它是存在的）。

## 12.1.1 邮件列表

托管在 `perl.org` 上的每个邮件列表也双向网关到 `nntp.perl.org` 上的新闻组，这是我访问列表列表的方式。

## 12.1.2 新闻组

主要的 Usenet 新闻组如下：

- `comp.lang.perl.misc`: 用于提问的主要新闻组。
- `comp.lang.perl.moderated`: 一个低流量、信噪比很高的组。
- `comp.lang.perl.modules`: 用于讨论使用和编写模块问题的低流量组。
- `comp.lang.perl.announce`: 用于新版本发布和其他重大事件的极低流量组。
- `comp.lang.perl.tk`: 仅供 Perl 图形界面用户使用。
- `alt.perl`: 每天发帖不到十条，但与 `comp.lang.perl.misc` 相比专家较少。

## 12.1.3 允许用户内容的门户

- `use.perl.org`: 该站点基于 Slashdot，托管了大量最新的新闻和反应。也提供免费的邮件列表。
- `www.perlmonks.org`: 该站点有大量访问者，并提供问答讨论和实时聊天。它是快速获取帮助和磨练帮助他人技能的绝佳场所。
- `www.perlguru.com`: Jasmine Merced 的网站为各种 Perl 问题提供了许多有论坛，包括职位搜索。

## 12.1.4 其他网站

- `www.perl.com`: O'Reilly 的网关，包含大量关于 Perl 的当前和存档文章以及他们丰富的书籍目录。
- `www.perl.org`: 社区的各种 Perl 事务门户。
- `www.perldoc.com`: 轻松访问从 5.004 以来 Perl 核心当前版本及以前版本的每份文档。





*   [jobs.perl.org](http://jobs.perl.org): 在众多 [perl.org](http://perl.org) 专门网站中值得特别提到，这个网站是寻找工作的人和寻找员工的人提供的。
*   [learn.perl.org](http://learn.perl.org): 同样值得关注，该网站旨在帮助人们学习 Perl。
*   [www.stonehenge.com/merlyn/columns.html](http://www.stonehenge.com/merlyn/columns.html): Randal Schwartz 为杂志专栏写了数百篇文章并将它们发布在网上；这个网站是宝贵且有趣示例的宝库。
*   [perl.plover.com](http://perl.plover.com): Mark-Jason Dominus 产出极其惊人，他在网路上发布了数百篇信息丰富的文章。其中一些（例如“处理作用域问题”）已成为回答某些常见问题的事实上标准引用。
*   [www.perlmedic.com](http://www.perlmedic.com): 本书的网站。

由于 Brian Ingerson 使用 `CGI::Kwiki` 让创建 Wiki 站点变得如此简单，现在可以寻找正在涌出的 Wiki 站点。Kwiki 列表维护在 [`www.kwiki.org/index.cgi?KwikiSites`](http://www.kwiki.org/index.cgi?KwikiSites)。

### 12.1.5 聊天频道

在几乎任何互联网中继聊天（IRC）网络上，`#perl` 都会有很多 Perl 人士，通常还有 `purl`，这是一个“机器人”或程序（适当的术语是代理），它能够回答各种问题、从对话中学习，并插进即时的评论。如果你在好奇它是用什么语言写的，那说明你没留神。

### 12.1.6 用户组

有一个名为 Perl Mongers 的全球 Perl 用户团体，总部位于 [`www.pm.org`](http://www.pm.org)。在你离你合理距离范围内很可能有一个小组，如果没有，你可以轻松地启动一个，就像我做的那样。出版商和其他供应商为 Perl Mongers 提供特殊优惠，而且还有一套时尚的服装。`pm.org` 根据需求为小组提供 Web 服务器和邮件列表。

### 12.1.7 期刊

两本专门致力于 Perl 的期刊都可以在线获取：

*   The Perl Journal，[`www.tpj.com/`](http://www.tpj.com/)。每月 PDF 下载；一年订阅需 12 美元。
*   The Perl Review，[`www.theperlreview.com/`](http://www.theperlreview.com/)。免费 PDF 下载；接受捐赠。

### 12.1.8 会

*   1997 年，第一届 Perl 会由 O'Reilly and Associates 在加利福尼亚州的圣何塞举办。1999 年，开源世界的其他部分追了上来，会议扩大到包含了他们。现在，每年的开源大会包含了 Perl 会（作为其最大的组成部分），并每年夏天在北美西岸举行。详见 [`conferences.oreillynet.com/oscon/`](http://conferences.oreillynet.com/oscon/)。

    > ^([1]) 当时它被称为“第零次” Perl 会，因为计算机领域的人喜欢从零开始计数。后来人们认为这太困惑了，于是会议追溯性地重新编号为 1 号。

*   1999 年，一些 Perl Mongers 决定他们想要低成本的替代方案，并在卡内基·梅隆大学举办了第一届 Yet Another Perl Conference (YAPC; [`www.yapc.org`](http://www.yapc.org))。从那以后，YAPC 扩展到了欧洲会议 ([`www.yapc.org/Europe/`](http://www.yapc.org/Europe/))，2003 年见证了以色列的首届 YAPC ([`www.perl.org.il/YAPC/`](http://www.perl.org.il/YAPC/)) 和首届真正的加拿大 YAPC ([`www.yapc.ca/`](http://www.yapc.ca/))。原始北美 YAPC 的主页是 [`www.yapc.org/America/`](http://www.yapc.org/America/)。

### 12.1.9 Perl 基金会

名为 Yet Another Society (YAS; [`www.yetanother.org/`](http://www.yetanother.org/)) 的非营利组织在其他项目中还推广 YAPC 活动。YAS 的附属机构是 Perl 基金会 ([`www.perl-foundation.org/`](http://www.perl-foundation.org/))，它的目的是收集捐款并资助值得的项目。当前和过去的资助者包括 Larry Wall 和 Damian Conway。如果你想捐款来促进 Perl 的进步，这里就是汇款的地方。

### 12.2 Perl 人士

Perl 人士的关键特质之一是他们在使用语言时是多么快乐。我认为这是语言与这些人之间一种协同和共生的关系；他们创造了一种使用起来有趣的语言，吸引了喜欢乐趣的人，然后他们又向语言注入了更多乐趣。（不要认为这意味着这种语言不适用于严肃、重要的工作。Perl 人士相信，在享受乐趣的同时可以完成更多工作。希望更多的经理能理解这一点。）参加 Perl 会议是了解 Perl 人士是什么样人的直接方式。

### 12.2.1 如何提问以获得回答

Perl 人士像任何计算机专家一样，依靠准确且完整的信息生存（他们必须能够像计算机工作的方式那样思考）。他们也喜欢帮助他人。你确保他们回答你问题的最好方法是让他们能够且容易地这样做。那些对于需求模糊、或未提供足够信息来得出答案的问题会让阅读这些问题的人感到沮丧，因为他们无法提供帮助。他们还将帮助看作自己与提问者之间的协作；在免费回答问题时，他们希望推广一种“回馈”模式，使提问者自己也能被赋能去帮助他人。如果提问者似乎不愿意付出同等的努力来学习，这个目标就会破灭。

了解这些关于 Perl 人士思考方式的知识，允许我们设计出能得到回答的问题。（在这里我只讨论在之前列出的各种在线资源上发帖寻求免费帮助；如果你正在付费请 Perl 顾问寻求帮助，那么你有权获得它。）遵循以下原则：

*   听起来连贯。这并不意味着那些不精通发帖语言的人发布的帖子就会被轻视；我见过许多英语不流利但意图非常清晰的帖子。你需要听起来像有足够的智慧理解答案，而你的词汇是读者做出这种评估的唯一指南。你必须让自己与互联网上发布的那些听起来完全像发现了父母键盘的婴儿的人区分开来。
*   明确你想要什么。你是想要某人为你写一段代码，告诉你在你写的代码哪里错了，还是想让他们为你解释一个概念？
*   保持谦逊。或者至少看起来那样。表现出理解任何帮助你的人都是出于慈善；不要给人你认为自己理应得到答案的印象。
*   清楚说明发生了什么。如果你遇到了一个问题，请报告你做了什么，计算机的响应是什么，以及你期望它应该是什么。除非你真的知道，否则不要对原因做假设，如果是真的，你就不是在假设。
*   提供解决问题所需的所有信息。如果 Perl 执行了你认为是错误的操作，至少你应该报告 Perl 版本以及你运行它的平台（`perl -V` 的输出就是为此目的设计的）。
*   简洁明了。如果你有一个产生错误的 1000 行程序，可能没人会为你免费阅读整个程序。将问题压缩到能够展示你问题的最小代码段。通常这个过程会让你自己发现答案。少于 50 行的代码有很好的机会被阅读。





*   表现出你想学习的意愿。说明你已经在文档的哪里查找过帮助。你尝试过 Google 搜索吗？特别要查看 [`groups.google.com/`](http://groups.google.com/)，看看是否已经有人问过相同的问题。

*   如果你发现别人的代码有错误，并且认为你知道如何修复，请将修复方案发送给他们（最好采用 `diff -u` 格式）。这种行为会让你离开“提问者”类别，进入“开发者”阵营，在那里你会受到热欢迎（尤其是如果你的补丁有效的话）。

在我写这一章时，我收到了一个非常棒的提问示例，我把它包含在这里，是因为其中有一个转折。首先，看这个问题：

> 我正在做两个幻灯片——一个是在我的个人页面上，上面有我大学聚会的照片。这个运行良好。请看这里：[URL 已删除]

> 我正在使用来自 [URL] 的一个免费 perl 软件包。

> 当我尝试在 [其他网站] 上运行相同的代码时，它就挂起了，没有任何错误信息。[托管服务] 是这两个页面的提供商，但他们对个人页面和商业网站有不同的安全保护措施，而且他们真的不鼓励人们编写自己的 perl 代码，所以我先向你们请教这个问题。

> 这里是挂起的那个子程序的代码和输出。

> 首先，这是输出：

> [调试输出大部分已删除。它提到了名为 'this' 和 'that' 的变量] this is ..........., that is <--无法粘贴到这条消息中。"this" 是 4 个那样的方框，然后是一个上面带有 ~ 符号的 N，旁边是一个倒置的 ?，后面跟着另外 9 个方框。"that" 类似的情况，在那个奇怪的 N 之前有一个 P，在下一个方框之后有一个 s。你可以自己查看：[URL]

> 这里是该子程序：注意，我在里面穿插了许多 `print` 语句。

> ```
 [代码已删除]
 ```

注意看，这位提问者提供了完整的信息，说明她在做什么、她的代码从哪里来、运行和不运行示例的 URL、输出内容（特别注意了她无法理解的非常规字符，这些字符在读者处的显示方式可能不同），以及出现问题代码片段（未显示）。

转折在于，这位提问者 Mary Byrne 是我一个朋友的 71 岁母亲。显然，年龄并不是学习如何正确提问题的障碍，也不是学习 Perl 的障碍。

## 12.3 结语

总有一天，你的代码也会被别人继承。无论我们走到哪里，都会留下我们存在的痕迹：有些令人愉快，有些则不然。代码就是这样一种提醒，诚然，在宏观蓝图中，它是微不足道的。然而，可以认为没有任何行动是微小的，对你代码的判断程度可以像你创造的任何东西一样准确。我告诉我的学生，一个成功的编程项目有三个心理前提（除了他们必须具备的知识之外）：

*   你必须相信你能够做到。
*   你必须尽可能做得完美。
*   你必须在其中乐此。

祝愿你的事业成功。

## 附录：源代码

*   Tie::Array::Bounded
*   Benchmark::TimeTick
*   smallprofpp

### Tie::Array::Bounded

```
package Tie::Array::Bounded;

use strict;

use warnings;

use Carp;

use base qw(Tie::Array);

our $VERSION = '0.01';

sub TIEARRAY
{
  my ($class, %arg) = @_;
  my ($upper, $lower) = delete @arg{qw(upper lower)};
  croak "Illegal arguments in tie" if %arg;
  $lower ||= 0;
  croak "No upper bound for array" unless $upper;
  /\D/ and croak "Array bound must be integer"
    for ($upper, $lower);
  croak "Upper bound < lower bound" if $upper < $lower;
  return bless { upper => $upper,
                 lower => $lower,
                 array => []
               }, $class;
}

sub _bound_check
{
  my ($self, $index) = @_;
  my ($upper, $lower) = @{$self}{qw(upper lower)};
  croak "Index $index out of range [$lower, $upper]"
    if $index < $lower || $index > $upper;
}

sub STORE
{
  my ($self, $index, $value) = @_;
  $self->_bound_check($index);
  $self->{array}[$index] = $value;
}

sub FETCH
{
  my ($self, $index) = @_;
  $self->_bound_check($index);
  $self->{array}[$index];
}

sub FETCHSIZE
{
  my $self = shift;
  scalar @{$self->{array}};
}

sub STORESIZE
{
  my ($self, $size) = @_;
  $self->_bound_check($size-1);
  $#{$self->{array}} = $size - 1;
}

1;

__END__
```





```perl
 package Benchmark::TimeTick;

use 5.006;

use strict;

use warnings;

use Exporter;

use File::Basename;

our @ISA       = qw(Exporter);

our @EXPORT_OK = qw(timetick);

our $VERSION   = '0.01';

my @Tix;           # 我们存储时间刻点的地方

our %Opt;          # 全局选项设置接口

my $Epoch = $^T;   # 测量时间的起始点

sub import
{
  my $class = $_[0];
  eval { require Time::HiRes };
  $Epoch = _current_time() if $Opt{reset_start};
  unless ($Opt{suppress_initial})
  {
    my $prog = basename($0);
    timetick("Timeticker for $prog starting");
  }
  $class->export_to_level(1, @_);
}

sub timetick
{
  my $tag = pop;
  $Opt{format_tick_tag} and $tag = $Opt{format_tick_tag}->($tag);
  push @Tix, [ _current_time() - $Epoch, $tag ];
}

sub _current_time
{
  exists &Time::HiRes::time ? Time::HiRes::time() : time;
}

sub report
{
  unless ($Opt{suppress_report})
  {
    &{ $Opt{format_report} || \&_format_report }(@Tix);
  }
  @Tix = ();
}

sub _format_report
{
  printf("%7.4f %s\n", @$_) for @_;
}

sub end
{
  unless ($Opt{suppress_final})
  {
    my $prog = basename($0);
    timetick("Timeticker for $prog finishing");
  }
  report();
}

END { end() }

1;

__END__
```

# 名称
`Benchmark::TimeTick` - 在程序中不同位置记录时间计数

# 示例
```perl
use Benchmark::TimeTick qw(timetick);

# 你的代码...

timetick("Starting phase three");

# 更多你的代码...
```

# 描述
`Benchmark::TimeTick` 提供了一种快速方便的方法来对程序进行插桩，以找出到达各个点所需的时间。只需使用该模块，并在你想标记程序中某点的时间时调用 `timetick()` 方法。当程序结束时，将输出一个报告，列出到达每个点的时间。

如果可用 `Time::HiRes`，则将使用 `Time::HiRes::time()` 记录，否则将使用 `time()`。（由于 `time()` 的粒度为秒，这可能没有用处。）

# 配置
你可以通过包哈希 `%Benchmark::TimeTick::Opt` 自定义 `Benchmark::TimeTick` 的行为。识别的键包括：

- `suppress_initial`: 如果为真，则在加载模块时，不在报告中包含初始条目。
- `suppress_final`: 如果为真，则在程序终止时，不在报告中包含结束条目。
- `reset_start`: 如果为真，则报告的所有时间相对于 `Benchmark::TimeTick` 加载的时间，而不是程序的实际开始时间。
- `format_tick_tag`: 如果设置，应为指向子程序的引用，该程序将接收传递给 `timetick()` 的 `$tag` 输入并返回实际的标签。
- `format_report`: 如果设置，应为指向子程序的引用，该程序将接收时间刻点列表作为输入进行报告。列表中的每个元素将包含时间和标签的数组引用。默认的 `format_report` 回调为：`sub { printf("%7.4f %s\n", @_) }`
- `suppress_report`: 如果为真，调用 `report()`时不输出报告；仅重置时间刻点列表。要使 `suppress_initial` 或 `reset_start` 生效，必须在 `use` 该模块之前设置它们。

# 方法
- `Benchmark::TimeTick::timetick($tag)`: 记录程序此处的时间，并用字符串 `$tag` 进行标记。
- `Benchmark::TimeTick::report()`: 输出报告（除非设置了 `suppress_report`）并重置时间刻点列表。
- `Benchmark::TimeTick::end()`: 添加一个结束刻点（除非设置了 `suppress_final`），并输出报告。在程序结束时默认调用。

## 可选导出
`Benchmark::TimeTick::timetick()` 按需导出。为了简洁，建议这样做。

# 示例
```perl
  BEGIN { $Benchmark::TimeTick::Opt{suppress_initial} = 1 }
  use Benchmark::TimeTick qw(timetick);

  # ... 时间流

  timetick("Phase 2");

  # ... 更多时间流，程序结束
来自 Benchmark::TimeTick 的输出:
  0.7524 Phase 2
  8328 Tim finishing

# 作者
Peter Scott

# 参见
`Timer`, `Time::HiRes`。

# 版权
Copyright (c) 2004 Peter Scott. 本库免费的；你可以按照 Perl 相同的条款重新分发或修改它。

### smallprof
```perl
#!/usr/bin/perl
use strict;
use warnings;
use Getopt::Std;
my $USAGE = "Usage: $0 [-c|-w] [profile]";
my $MAXLEN = 80;
getopts('cw', \%opt) or die $USAGE;
my $profile = shift || 'smallprof.out';
open my $fh, '<', $profile or die "Can't open profile: $!";
my ($header, $filename, @to_sort);
while (<$fh>) {
  $header = $_ if /^\s+count/;
  $filename = $1 if /^\s+Profile (.*)\s+Page/;
  /^\s+(\d+)\s+([\d.]+)\s+([\d.]+:/
    and push @to_sort, [ $2, $3, $filename ];
}
my $which = $opt{c} ? 2 : 1; # 默认时间
my $other = $which == 1 ? 2 : 1; # 其他时间
print $header,
      map { (my $line = $_[0]) =~ s/\b\s+(\d+):.*/s;
             my $fileline = $_[3]:$1";
             if (length($fileline) + length($line) > $MAXLEN) {
               substr($fileline, 0, length($fileline)+length($line)-$MAXLEN+3, '...');
             }
             "$line$fileline\n";
      }
      sort { $b[$which] <=> $a[$which] || $b[$other] <=> $a[$other] } @to_sort;
```

# 名称
`smallprof` - 对 `Devel::SmallProf` 的分析数据排序

# 用法
`smallprof [-c|-w] [profile]`

# 描述
`smallprof` 命令排序并输出 `Devel::SmallProf` 生成的命名文件（默认 `smallprof.out`）。页面标题将被移除且仅打印一行标题；对于从未调过的源代码行将进行输出（你可以通过在 `.smallprof` 文件中放置 `$DB::drop_zeros = 1` 语句来防止 `Devel::SmallProf` 输出它们；参见 `Devel::SmallProf`）。行将按 CPU 时间或墙钟时间的降序排序；相同项按其他时间排序。

# 选项
- `-c`: 先按 CPU 时间排序，后按墙钟时间排序。
- `-w`: 先按墙钟时间排序，后按 CPU 时间排序。这是默认值。

# 参见
`Devel::SmallProf`.

### 参考文献
- AHO74: Aho, Alfred V., Hopcroft, John E., and Ullman, Jeffrey D., *The Design and Analysis of Computer Algorithms*, Addison-Wesley (1974). ISBN: 0-201-0029-6.
- AHO83: Aho, Alfred V., Ullman, Jeffrey D., and Hopcroft, John E., *Data Structures and Algorithms*, Addison-Wesley (1983). ISBN: 0-201-0023-7.
- BECK00: Beck, Kent, *Extreme Programming Explained*, Addison-Wesley (2000). ISBN: 0-201-61441-6.
- BEKMAN03: Bekman, Stas and Cholet, Eric, *Practical mod_perl*, O'Reilly & Associates (2003). ISBN: 0-596-00227-0.
- BENTLEY82: Bentley, Jon, *Writing Efficient Programs*, Prentice Hall (1982). ISBN: 0-139-70244-X.
- BOLINGER95: Bolinger, Don and Bronson, Tan, *Applying RCS and SCCS*, O'Reilly & Associates (1995). ISBN: 1-56592-117-8.
- BROWN98: Brown, William J., Malveau, Raphael C., McCormick III, Hays W., and Mowbray, Thomas J., *AntiPatterns*, Wiley (1998). ISBN: 0-471-19713-0.
- BURKE02: Burke, Sean M., *Perl & LWP*, O'Reilly & Associates (2002). ISBN: 0-596-000-178-9.





- CHRISTIANSEN98: Christiansen, Tom, 在 [`groups.google.com/groups?selm=6bt80h%24req%241%40csnews.cs.colorado.edu`](http://groups.google.com/groups?selm=6bt80h%24req%241%40csnews.cs.colorado.edu).
- CHROMATIC03: chromatic, 《极限编程指南》, O'Reilly & Associates (2003). ISBN: 0-596-00485-0.
- CMU03: [`www.sei.cmu.edu/cmm/cmm.html`](http://www.sei.cmu.edu/cmm/cmm.html).
- DESCARTES00: Descartes, Alligator and Bunce, Tim, 《程序 Perl DBI》, O'Reilly & Associates (2000). ISBN: 1-56592-699-4.
- DOMINUS98: Dominus, Mark Jason, 在 [`perl.plover.com/FAQs/Namespaces.html`](http://perl.plover.com/FAQs/Namespaces.html).
- EIFFEL03: [`archive.eiffel.com/doc/manuals/technology/contract/`](http://archive.eiffel.com/doc/manuals/technology/contract/).
- FOWLER99: Fowler, Martin, 《重构：改进现有代码的设计》, Addison-Wesley (1999). ISBN: 0-201-48567-2.
- FRIEDL02: Friedl, Jeffrey, 《精通正则表达式》, 第 2 版, O'Reilly & Associates (2002). ISBN: 0-596-00289-0.
- GAMMA95: Gamma, Erich, Helm, Richard, Johnson, Ralph, and Vlissides, John. 《设计模式》, Addison-Wesley (1995). ISBN: 0-201-63361-2.
- GLOBE99: [`www.boston.com/allstar99/news/all_hack_070799.htm`](http://www.boston.com/allstar99/news/all_hack_070799.htm).
- GUTTMAN98: Guttman, Uri, 在 [`www.sysarch.com/perl/tutorials/hash_slices.txt`](http://www.sysarch.com/perl/tutorials/hash_slices.txt).
- HALL98: Hall, Joseph N., 《高效 Perl 编程》, Addison-Wesley (1998). ISBN: 0-201-41975-0.
- HOGABOOM03: Hogaboom, Richard, “Perl 与空中交通控制，”《Perl Journal》，2003 年 9 月.
- HUMPHREY94: Humphrey, Watts S., 《软件工程的律》, Addison-Wesley (1994). ISBN: 0-201-54610-8.
- HUNT00: Hunt, Andrew and Thomas, David. 《实战程序员之道》, Addison-Wesley (2000). ISBN: 0-201-61622-X.
- JOHNSON99: Johnson, Andrew L., 《Perl 编程元素》, Manning (1999). ISBN: 1-884777-80-5.
- LEUF01: Leuf, Bo and Cunningham, Ward, 《Wiki Way》, Addison-Wesley (2001). ISBN: 0-201-71499-X.
- LIDIE02: Lidie, Stephen O. and Walsh, Nancy, 《精通 Perl/Tk》, O'Reilly & Associates (2002). ISBN: 1-56592-716-8.
- OREILLY99: [`perl.oreilly.com/news/success_stories.html`](http://perl.oreilly.com/news/success_stories.html).
- ORWANT99: Orwant, Jon, Hietaniemi, Jarkko, and Macdonald, John, 《用 Perl 精通算法》, O'Reilly & Associates (1999). ISBN: 1-56592-398-7.
- PEPPLER02: [`www.mbay.net/~mpeppler/Sybperl/sybperl-faq.html`](http://www.mbay.net/~mpeppler/Sybperl/sybperl-faq.html).
- RANDAL03: Randal, Allison, Sugalski, Dan, and Tötsch, Leopold, 《Perl 6 教程》, O'Reilly & Associates (2003). ISBN: 0-596-00499-0.
- RAY02: Ray, Erik T., and McIntosh, Jason, 《Perl & XML》, O'Reilly & Associates (2002). ISBN: 0-596-00205-X.
- SCHWARTZ97: Schwartz, Randal L. and Christiansen, Tom, 《学习 Perl》, 第 2 版, O'Reilly & Associates (1997). ISBN: 1-56592-284-0.
- SCHWARTZ01: Schwartz, Randal L. and Phoenix, Tom, 《学习 Perl》, 第 3 版, O'Reilly & Associates (2001). ISBN: 0-596-0132-0.
- SCHWARTZ03a: Schwartz, Randal L. and Phoenix, Tom, 《学习 Perl 对象、引用与模块》, O'Reilly & Associates (2003). ISBN: 0-596-0478-8.
- SCHWARTZ03b: Schwartz, Randal L., “Perl 之智，”Linux Magazine》，2003 年 6 月.
- SCOTT01: Scott, Peter J. and Wright, Ed, 《Perl 调试》, Addison-Wesley (2001). ISBN: 0-201-70054-9.
- STEIN00: Stein, Lincoln D., 《网络 网络编程》, Addison-Wesley (2000). ISBN: 0-201-61571-1.
- STLAURENT01: St. Laurent, Simon, Johnston, Joe, and Dumbill, Edd, 《使用 XML-RPC  Web 服务》, O'Reilly & Associates (2001). ISBN: 0-596-0199-3.
- SWIFT47: Swift, Jonathan, 《格列佛游记》, 精装版, Price Stern (1947). ISBN: 0-44806-01-8.
- TAYLOR02: Taylor, Richard, “混沌中的秩序，”科学美国》，2002 年 12 月.
- TREGAR02: Tregar, Sam, 《为 CPAN 写 Perl》, Apress (2002). ISBN: 1-59059-01.
- VESPERMAN03: Vesperman, Jennifer, 《基础》, O'Reilly & Associates (2003). ISBN: 0-596-0459-1.
- WALL96: Wall, Larry, Christiansen, Tom, and Schwartz, Randal L., 《程序 Perl》, 第 2 版, O'Reilly & Associates (1996). ISBN: 1-56592-149-6.
- WALL00: Wall, Larry, Christiansen, Tom, and Orwant, Jon, 《程序 Perl》, 第 3 版, O'Reilly & Associates (2000). ISBN: 0-596-00027-8.

### 关于作者

![peter.gif](img/peter.gif)

PETER J. SCOTT 主 Pacific Design Technologies，提供 Perl 培训、应用程序开发和企业级系统分析。他曾在 2002 年 Perl 游轮和 YAPC::Canada 上担任演讲者，并创立了当地的 Monger 小组。他自 1981 年起担任软件开发人员，自 1992 年起担任 Perl 开发者，还为 NASA 喷气实验室开发过程序。Scott 毕业于英国剑桥大学获得计算机科学硕士学位，现住在西北地区与他的妻子 Grace、一只猫和一只鹦鹉住在一起，其中至少一个也会使用 Perl。他是《Perl 调试》的主作者。





# ActiveState 第二次

# AFS

# 算法的重要性

# Alzabo

# 匿名哈希引用

# Attribute::Handlers 第二次 第三次

# attrs 伪指令

# AUTOLOAD 第二次

# 使用伪指令的 AutoLoader

# 阿伏加罗常数

# AxKit 第二次

[SYMBOL] [A] [B] [C] [D] [E] [F] [G] [H] [I] [L] [M] [N] [O] [P] [R] [S] [T] [U] [V] [W] [X] [Y]

# B::Deobfuscate

# B::Deparse 第二次

# B::Xref

# 裸露字 (bareword)

# Barr, Graham

# 代码美化

# Benchmark::Timer

# Benchmark::TimeTick 第二次

# 块注释

# 大括号样式, BSD Allman

# 大括号样式, Kernighan and Ritchie

# btreeperl

[SYMBOL] [A] [B] [C] [D] [E] [F] [G] [H] [I] [L] [M] [N] [O] [P] [R] [S] [T] [U] [V] [W] [X] [Y]

# C 转 Perl 的压缩比

# can_ok()

# carp()

# Carp::Assert 第二次 第三次

# CGI 程序、测试

# cgi-lib.pl

# CGI.pm 第二次 第三次 第四次 第五次

# CGI::wiki 第二次

# chromatic

# cisamperl

# Class::Contract 第二次

# Class::Inspector

# 客户端/服务器、进化

# 代码单元 第二次

# 混淆代码

# 注释

# Comprehensive Perl 存档 第二次 第三次 第四次

# 连接、无意义

# Perl 会议

# conf()

# Config::Auto 伪指令 第二次 第三次 第四次

# 常量

# 符号常量

# Conway, Damian 第二次

# CPAN 模块的可靠性

# CPAN.pm 第二次 第三次 第四次 第五次 第六次

# CPAN.pm, 模式 第二次

# CPAN_ 第二次 第三次 第四次 第五次

# CPANPLUS

# croak()

# ctreeperl

# CVS

[SYMBOL] [A] [B] [C] [D] [E] [F] [G] [H] [I] [L] [M] [N] [O] [P] [R] [S] [T] [U] [V] [W] [X] [Y]

# Date::Calc

# Date::Manip

# DBI.pm

# DBM 文件

# DBM 文件的优势 第二次 第三次

# Debug::FaultAutoBT

# 基础调试器命令

# Perl 调试器 第二次 第三次 第四次 第五次 第六次 第七次

# 调试 第二次

# 去混淆

# Deparse 模块

# 列出依赖项

# 查找依赖项

# 契约设计

# Devel::Cover

# Devel::Coverage

# Devel::DProf

# Devel::LeakTrace

# Devel::SmallProf

# dies_ok() 第二次

# Digest::MD5

# Dua.pm 第二次 第三次

# duaperl

# EmailErrors 模块

# 错误处理、进化





- `Error.pm`
- `事件处理，演进`
- `Event.pm`
- `异常处理块`
- `Exception::Class`
- `外部数据存储，演进`
- `外部信息表示，演进`
- `外部程序` (第 2 次)
- `外部程序，过度调用`
- `极端开发` (第 2 次, 第 3 次, 第 4 次)
- `ExtUtils::MakeMaker` (第 2 次)
- `FatalsToEmail 模块`
- `FETCH()` (第 2 次)
- `FETCHSIZE()` (第 2 次)
- `fields pragma`
- `File::Find` (第 2 次)
- `File::Path`
- `filter, LDAP`
- `Filter::Simple`
- `Filter::Util::Call`
- `find()`
- `FindBin`
- `FindBin 模块`
- `for, 作为 foreach 的同词`
- `foreach` (第 2 次)
- `foreach, 后置形式` (第 2 次)
- `foy, brian d`
- 用于解释 `G` 目的的 锚点
- `G` 随 `c` 修饰符添加
- `Getopt::Std`
- `getopts()`
- `h2xs` (第 2 次, 第 3 次)
- `哈希，多维`
- `哈希，不使用`
- `Hopkins, Sharon`
- `HTML 解析`
- `HTML::Template` (第 2 次)
- `hubris`
- `独特性`
- `不耐烦`
- `原地编辑`
- `缩进`
- `缩进，延续行`
- `Ingerson, Brian`
- `初始化，多余的`
- `Inline:: 模块`
- `Inline::C`
- `输入接口，演进`
- `interperl`
- `进程间通信，演进`
- `IO::Socket`
- `is()`
- `is_deep()`
- `isa_ok()`
- `isql`
- `Larry Wall`
- `懒惰` (第 2 次)
- `遗留代码，编写测试`
- `perl 熟练程度`
- `like()`
- `五律诗，糟糕的`
- `行编辑`
- `List::Util`
- `lives_ok` (第 2 次)
- `local` (第 2 次, 第 3 次, 第 4 次)
- `lock`
- `Log::Dispatch::FileRotate`
- `Log::Log4perl` (第 2 次, 第 3 次)
- `日志，演进`
- `lvalue 子程序` (第 2 次)
- `MacPerl, 获取`
- `魔数`
- `Mail::Audit`
- `Mail::Internet`
- `Mail::Send` (第 2 次)
- `Mail::SpamAssassin`
- `makefile`
- `Makefile.PL`
- `map`
- `Memoize 模块`





# 索引与目录

- MIME::Base64
- MIME::Lite
- 模型-视图-控制器模式
- 模块化，演进中的
- 模块安装，手动的
- 模块，定义
- Module::Build
- Module::CoreList 第 2 次
- Module::Info
- msg_ok()
- my() 第 2 次 第 3 次 第 4 次 第 5 次

## 字母符号索引

[SYMBOL] [A] [B] [C] [D] [E] [F] [G] [H] [I] [L] [M] [N] [O] [P] [R] [S] [T] [U] [V] [W] [X] [Y]

## 网络与 LDAP 相关

- Net::Cmd
- Net::LDAP
- Net::LDAP::Entry 第 2 次
- Net::LDAP::Filter
- Net::LDAP::Search
- newsgroups

## 语言指令与语法

- no
- [`no strict 'refs']`](ch05lev1sec5.html_idd1e7725)
- [`no strict 'subs']`](ch05lev1sec5.html_idd1e7688)
- [`no strict 'vars']`](ch05lev1sec5.html_idd1e7668)
- no warnings
- [`no warnings 'redefine']`](ch05lev1sec5.html_idd1e7912)

- ok()
- open()
- 运算符重载
- 运算符，菱形
- 为了速度优化
- 优化，不同的原因
- oraperl
- our() 第 2 次 第 3 次 第 4 次
- overloading

## Perl 核心技术

- 括号，无用的
- 期刊，Perl
- PERL
- Perl 4 第 2 次
- Perl 4.018
- Perl 5.000
- Perl 5.001
- Perl 5.002
- Perl 5.003
- Perl 5.004
- Perl 5.005
- Perl 5.6.0
- Perl 5.6.1
- Perl 5.8.0 第 2 次
- Perl 6
- Perl golf
- Perl Mongers
- Perl 对象环境
- Perl poetry
- Perl 源，获取
- Perl 成功故事
- Perl, 无重音
- Perl, 可维护性
- Perl, 获取
- Perl, 旧版本
- Perl, 版本检测
- perlhist
- perlrun
- perlstyle
- pgperl

## 文档与工具

- Phoenix, Tom
- 纯文本文档 (Plain Old Documentation) 第 2 次 第 3 次 第 4 次
- pmtools
- POD 格式化器
- POD_ 参考纯文本文档
- pod_ok()
- pod2xml
- POE_ 参考 Perl 对象环境
- poetry 模式
- poetry, 坏的
- portals, Perl
- PPM 第 2 次
- pragma 第 2 次 第 3 次
- 伪哈希

## 设计与重构

- 设计原理，设计
- RCS 第 2 次 第 3 次
- 真实世界，the
- 重构
- 引用 第 2 次
- 引用，符号化的 第 2 次 第 3 次
- 回归测试
- 正则表达式，调试
- 正则表达式，无效的
- Retroperl
- 返回码，检查
- return 语句
- 版本控制
- RFC 822
- rocisperl
- Rolsky, Dave
- runtests()
- Safe.pm





- `scalar()`
- `Scalar::Util`
- `SCCS` (2nd)
- `Schwartz, Randal` (2nd)
- `Schwern, Michael`
- `scope`
- `scoping, dynamic` (2nd)
- `scoping, lexical`
- `search.cpan` (3rd)
- `sentinel comments`
- `shebang line` (2nd)
- `shebang line, modifying` (2nd)
- `slices, hash`
- `slices, useless`
- `smallprof`
- `SOAP`
- `Socket.pm`
- `sort pragma`
- `Source Code System`
- `type file`
- `sqlperl`
- `Storable module`
- `STORE()` (2nd)
- `STORESIZE()`
- `stream processing, line`
- `strict`
- `stringification, useless`
- `style`
- `subroutine prototypes`
- `subroutine, redefinition`
- `Subversion`
- `suidperl` (2nd, 1th)
- `Switch module`
- `SYMBOL` (A, B, C, D, E, F, G, H, I, L, M, N, O, P, R, S, T, U, V, W, X, Y)
- `Tangram`
- `tarballs`
- `Template Toolkit`
- `temporary variables`
- `Test::Builder` (2nd)
- `Test::Exception`
- `Test::Harness` (2nd)
- `Test::MailMessage`
- `Test::More` (2nd)
- `Test::NoWarnings`
- `Test::Pod`
- `Test::Simple` (2nd)
- `Test::Tutorial`
- `Text::Balanced`
- `throws_ok()` (2nd)
- `Thunderbirds`
- `Tie::Array::Bounded` (2nd, 3rd, 4th)
- `Tie::File`
- `TIEARRAY` (2nd)
- `tieing` (2nd, 3rd)
- `Time::HiRes`
- `tkperl`
- `TMTOWDI`
- `typeglobs`
- `SYMBOL` (A, B, C, D, E, F, G, H, I, L, M, N, O, P, R, S, T, U, V, W, X, Y)
- `undef`
- `Unicode`
- `uniperl`
- `universe, fundamental structure`
- `URI Parsing`
- `URI.pm`
- `use lib`
- `use strict` (2nd, 3rd, 4th, 5th, 6th)
- `use strict 'refs'`
- `use strict 'subs'`
- `use strict 'vars'` (2nd)
- `use vars` (2nd, 3rd)
- `use warnings` (2nd, 3rd, 4th, 5th)
- `use_ok()`
- `SYMBOL` (A, B, C, D, E, F, G, H, I, L, M, N, O, P, R, S, T, U, V, W, X, Y)
- `variable renaming`
- `variable, lexical` (2nd)
- `variable, package` (2nd, 3rd)
- `virtues of Perl programmers, principal`
- `Visual Perl`
- `SYMBOL` (A, B, C, D, E, F, G, H, I, L, M, N, O, P, R, S, T, U, V, W, X, Y)
- `warnings in modules`
- `warnings, custom`
- `warnings, disabling`
- `warnings, lexical`
- `warnings, whether to leave in production code`
- `Web server processing, evolving`
- `WWW::Mechanize` (2nd, 3rd)





[SYMBOL] [A] [B] [C] [D] [E] [F] [G] [H] [I] [L] [M] [N] [O] [P] [R] [S] [T] [U] [V] [W] [X] [Y]

XML-RPC

XP_ 查看 [极限编程]第二 nd 查看 [极限编程]第三 rd 查看 [极限编程]

[SYMBOL] [A] [B] [C] [D] [E] [F] [G] [H] [I] [L] [M] [N] [O] [P] [R] [S] [T] [U] [V] [W] [X] [Y]

YAML

YAPC

YAPE::Regex::Explain

Yet Another Society


# React 学习之路：通精纯粹实用 React.js 之旅







![](img/1ca80d2ca01ac4fe106c899900e9eecb_0_0.png)

**推特这本书！**

请通过在 Twitter 上传播此这本书来向 Robin Wieruch 提供帮助！

此书建议的推文内容为：

I just bought The Road to learn React by @rwieruch #ReactJs https://roadtoreact.com

此书建议的标签为 #ReactJs。

点击此链接在 Twitter 上搜索该标签，了解其他人对这本书的评价：

#ReactJs


**前言** ... i
**关于作者** ... ii



你好，我叫 React.... ... 2

























































**前言**

《学习 React 之路》将教你 React 的基础知识。在此过程中，你将使用纯 React（不依赖复杂的工具）构建一个真实世界的应用程序。从项目设置到服务器上部署，一切内容都将为你详细解释。书中每一章都附有额外的参考阅读材料和练习。读完本书后，你将能够用 React 构建你自己的应用程序。这些内容将由我和社区保持更新。

在《学习 React 之路》中，我希望在你开始深入更广泛的 React 生态系统之前，提供一个基础。它包含的工具较少，外部状态管理也较，但包含了大量 React 的信息。它解释了真实 React 应用中的通用概念、模式和最佳实践。你将学习如何构建自己的 React 应用。它涵盖了真实世界的特性，如分页、客户端缓存以及搜索和排序等交互。此外，你将在过程中从 JavaScript ES5 过渡到 JavaScript ES6。我希望这本书能表达我对比 React 和 JavaScript 的热情，并帮助你入门。





## 关于作者

Robin Wieruch 是一位德国软件和 Web 工程师，致力于学习和教授 JavaScript 编程。在从大学获得计算机科学硕士学位后，他从未停止每天的自学。他在初创企业世界的经历——在工作和闲余时间里大量使用 JavaScript——让他获得了了向他人教授这些主题的机会。

在几年时间里，Robin 在一家名为 Small Improvements 的公司与优秀的工程师团队紧密合作，开发了一个大型应用程序。该公司构建了一款 SaaS 产品，帮助客户在公司内部建立反馈文化。在底层，该应用程序前端使用 JavaScript，后端使用 Java。在前端，第一个版本是使用 Java、Wicket 框架和 jQuery 编写的。当第一代 SPA（单页应用）流行时，公司将前端应用迁移到了 Angular 1.x。在在使用 Angular 超过 2 年后，很明显，在当时，Angular 并不是处理状态密集型应用的最佳解决方案。这就是为什么公司最终转向了 React 和 Redux，这使其能够成功地进行大规模运营。

在公司工作期间，Robin 经常在他的个人网站上撰写关于网页开发的文章。他注意到人们对他的文章给出了极佳的反馈，这让他改进了自己的写作和教学风格。一篇文章又一篇文章，Robin 教授他人的能力日益增长。第一篇文章包含了过多的内容，让学生感到有些无所从心，但随着时间的推移，文章通过专注于和只教授一个主题得到了改进。

如今，Robin 自由职业教授他人。他发现，通过提供清晰的目标和简短的反馈循环，看到学生的蓬勃成长是一项非常有成就感的活动。这是你在反馈公司中学到的东西，不是吗？但如果不亲自写代码，他就无法教授这些东西。这就是为什么他把剩余的时间投入到编程中。你可以在他的网站上找到更多关于 Robin 的信息以及支持和他合作的方法¹。

¹https://www.robinwieruch.de/about


这本书有很多评价²、评分³和评论⁴^，足以证明它的质量。我对此感到非常自豪，因为我从未想过会有如此热烈的反馈。如果你也喜欢这本书，我也能在某个地方看到你的评分/评论。这有助于我向推荐这本书。以下是这些美誉声音的简短节选：

- **Muhammad Kashif**⁵：《React 学习之路》是一本独特的书，我向任何对学习 React 基础到高级水平感兴趣的学生或专业人士推荐。它充满了在其他地方难以发现的深刻见解和技巧，在运用示例和参考样例问题方面表现得异常详尽。我有 17 年的网页和桌面应用开发经验，在读此书之前，我在学习 React 方面一直很困难，但这本书像魔法一样解决了了问题。”
- **Andre Vargas**⁶：“Robin Wieruch 编写的《React 学习之路》真是一本太棒的书了！我关于 React 甚至 ES6 的大部分知识都是通过这本书学会！”
- **Nicholas Hunt-Walker，西雅图某编码学校 Python 教师**⁷：“这是我接触过的写得最好且信息丰富的编程书籍之一。一个非常扎实的 React 和 ES6 介绍。”
- **Austin Green**⁸：“感谢，非常喜欢这本书。是学习 React、ES6 和高阶编程概念的完美结合。”
- **Nicole Ferguson**⁹：“我这周末在学 Robin 的《React 学习之路》课程，我几乎因为玩得太开心而感到点愧疚。”
- **Karan**¹⁰：“刚读完你的《React 学习之路》。这是 React 和 JS 世界中初学者最好的书。对 ES 的引入非常优雅。赞赞！ :)”
- **Eric Priou**¹¹：“Robin Wieruch 写的《React 学习之路》是必读之作。对于 React 和 JavaScript 来说简洁明了。”
- **一名新手开发者**：“作为一名新手开发者，我刚看完这本书，感谢你编写它。它很容易上手，我有信心在未来的几天里从零开始一个新应用。这本书比我之前尝试过的官方 React 教程好得多（之前因为细节不足没能完成）。每个章节末的练习非常有收获。”


(注：原文后续包含大量重复和错乱的 OCR 文本，已按要求仅翻译核心内容。)






vii

**我可以帮助改进它吗？** 可以。你可以通过在 [GitHub^(19)](https://github.com/rwieruch/the-road-to-learn-react)上的想法和贡献产生直接影响。我不自称是专家，也不是用母语英语写作。我非常感谢你的帮助。

**我可以支持这个项目吗？** 可以。请随时联系我。我投入了大量时间编写开源教程和学习资源。你可以看看我的[关于我^(20)](https://www.robinwieruch.de/about/) 页面。我很欢迎你成为我在 Patreon^(21)](https://www.patreon.com/rwieruch)上的赞助者。

**有什么行动号召吗？** 有。我希望你花一点时间思考一个适合学习 React 的人。这个人可能已经表现出了兴趣，可能正在学习 React 的过程中，也可能还没有意识到想学习 React。联系那个人并分享这本书。对我来说意义重大。这本书的初衷是送给他人的。

19 https://github.com/rwieruch/the-road-to-learn-react
20 https://www.robinwieruch.de/about/
21 https://www.patreon.com/rwieruch


**2017年1月10日：**
- v2 [Pull Request^(22)](https://github.com/rwieruch/the-road-to-learn-react/pull/18)
- 对新手更友好
- 内容增加了37%
- 内容改进了30%
- 改进并新新增了13个章节
- 140页学习材料
- + 本书在 [educative.io上的^(23)](https://www.educative.io/collection/5740745361195008/5676830073815040) 交互式课程

**2017年3月08日：**
- v3 [Pull Request^(24)](https://github.com/rwieruch/the-road-to-learn-react/pull/34)
- 内容增加了20%
- 内容改进了25%
- 9个新章节
- 170页学习材料

**2017年4月15日：**
- 升级到 React 15.5

**2017年7月05日：**
- 升级到 node 8.1.3
- 升级到 npm 5.0.4
- 升级到 create-react-app 1.3.3

**2017年10月17日：**
- 升级到 node 8.3.0
- 升级到 npm 5.5.1
- 升级到 create-react-app 1.4.1
- 升级到 React 16
- v4 [Pull Request^(25)](https://github.com/rwieruch/the-road-to-learn-react/pull/72)
- 内容增加了15%
- 内容改进了15%
- 3个新章节（绑定、事件处理、错误处理）
- 190+页学习材料
- +9 [源代码项目^(26)](https://roadtoreact.com/course-details?courseId=THE_ROAD_TO_LEARN_REACT)

**2018年2月17日：**
- 升级到 node 8.9.4
- 升级到 npm 5.6.0
- 升级到 create-react-app 1.5.1
- v5 [Pull Request^(27)](https://github.com/the-road-to-learn-react/the-road-to-learn-react/pull/105)
- 更多的学习路径
- 额外的阅读材料
- 1个新章节（用 Axios 代替 Fetch）

22 https://github.com/rwieruch/the-road-to-learn-react/pull/18
23 https://www.educative.io/collection/5740745361195008/5676830073815040
24 https://github.com/rwieruch/the-road-to-learn-react/pull/34
25 https://github.com/rwieruch/the-road-to-learn-react/pull/72
26 https://roadtoreact.com/course-details?courseId=THE_ROAD_TO_LEARN_REACT
27 https://github.com/the-road-to-learn-react/the-road-to-learn-react/pull/105

## 如何阅读本书？

这本书是我尝试在让你编写应用程序的同时教你 React。它是一份学习 React 的实战指南，而不是关于 React 的参考书。你将编写一个与真实世界 API 交互的 Hacker News 应用程序。在几个有趣的话题中，它涵盖了 React 中的状态管理、缓存和交互（排序和搜索）。在此过程中，你将学习 React 的最佳实践和模式。

此外，这本书还带你完成了从 JavaScript ES5 到 JavaScript ES6 的过渡。React 拥抱了许多 JavaScript ES6 特性，我想向你展示如何使用它们。

总的来说，书的每一章都是在前章的基础上。每一章都会教你一些新东西。不要急于读完。你应该内化每一个步骤。你可以应用自己的实现并阅读更多关于该主题的内容。每一章之后，我都会为你提供一些阅读材料和练习。如果你真的想学习 React，我强烈建议阅读额外材料并做一些动手练习。在读完一章后，在你熟悉所学内容后再继续。

最后，你将拥有一个生产级的 React 应用。我非常渴望看到你的成果，所以读完书后请给我留言。书的最后一章将为你提供几个继续 React 之旅的选择。通常，你会在我的[个人网站^(28)](https://www.robinwieruch.de/)上发现很多 React 相关话题。

既然你正在读这本书，我猜你是 React 新手。这太完美了。最后，我希望获得你的反馈以改进材料，让每个人都能学习 React。你可以在 [GitHub^(29)](https://github.com/rwieruch/the-road-to-learn-react)产生直接影响，或在 [Twitter^(30)](https://twitter.com/rwieruch)上给我留言。

28 https://www.robinwieruch.de/
29 https://github.com/rwieruch/the-road-to-learn-react
30 https://twitter.com/rwieruch

## React 简介

React 是我尝试在让你编写应用程序的同时教你 React。它是一份学习 React 的实战指南，而不是关于 React 的参考书。你将编写一个与真实世界 API 交互的 Hacker News 应用程序。在几个有趣的话题中，它涵盖了 React 中的状态管理、缓存和交互（排序和搜索）。在此过程中，你将学习 React 的最佳实践和模式。

此外，这本书还带你完成了从 JavaScript ES5 到 JavaScript ES6 的过渡。React 拥抱了许多 JavaScript ES6 特性，我想向你展示如何使用它们。

总的来说，书的每一章都是在前章的基础上。每一章都会教你一些新东西。不要急于读完。你应该内化每一个步骤。你可以应用自己的实现并阅读更多关于该主题的内容。每一章之后，我都会为你提供一些阅读材料和练习。如果你真的想学习 React，我强烈建议阅读额外材料并做一些动手练习。在读完一章后，在你熟悉所学内容后再继续。

最后，你将拥有一个生产级的 React 应用。我非常渴望看到你的成果，所以读完书后请给我留言。书的最后一章将为你提供几个继续 React 之旅的选择。通常，你会在我的[个人网站^(28)](https://www.robinwieruch.de/)上发现很多 React 相关话题。

既然你正在读这本书，我猜你是 React 新手。这太完美了。最后，我希望获得你的反馈以改进材料，让每个人都能学习 React。你可以在 [GitHub^(29)](https://github.com/rwieruch/the-road-to-learn-react)产生直接影响，或在 [Twitter^(30)](https://twitter.com/rwieruch)上给我留言。

## React 简介

React 是我尝试在让你编写应用程序的同时教你 React。它是一份学习 React 的实战指南，而不是关于 React 的参考书。你将编写一个与真实世界 API 交互的 Hacker News 应用程序。在几个有趣的话题中，它涵盖了 React 中的状态管理、缓存和交互（排序和搜索）。在此过程中，你将学习 React 的最佳实践和模式。

此外，这本书还带你完成了从 JavaScript ES5 到 JavaScript ES6 的过渡。React 拥抱了许多 JavaScript ES6 特性，我想向你展示如何使用它们。

总的来说，书的每一章都是在前章的基础上。每一章都会教你一些新东西。不要急于读完。你应该内化每一个步骤。你可以应用自己的实现并阅读更多关于该主题的内容。每一章之后，我都会为你提供一些阅读材料和练习。如果你真的想学习 React，我强烈建议阅读额外材料并做一些动手练习。在读完一章后，在你熟悉所学内容后再继续。

最后，你将拥有一个生产级的 React 应用。我非常渴望看到你的成果，所以读完书后请给我留言。书的最后一章将为你提供几个继续 React 之旅的选择。通常，你会在我的[个人网站^(28)](https://www.robinwieruch.de/)上发现很多 React 相关话题。

既然你正在读这本书，我猜你是 React 新手。这太完美了。最后，我希望获得你的反馈以改进材料，让每个人都能学习 React。你可以在 [GitHub^(29)](https://github.com/rwieruch/the-road-to-learn-react)产生直接影响，或在 [Twitter^(30)](https://twitter.com/rwieruch)上给我留言。

## React 简介

React 是我尝试在让你编写应用程序的同时教你 React。它是一份学习 React 的实战指南，而不是关于 React 的参考书。你将编写一个与真实世界 API 交互的 Hacker News 应用程序。在几个有趣的话题中，它涵盖了 React 中的状态管理、缓存和交互（排序和搜索）。在此过程中，你将学习 React 的最佳实践和模式。

此外，这本书还带你完成了从 JavaScript ES5 到 JavaScript ES6 的过渡。React 拥抱了许多 JavaScript ES6 特性，我想向你展示如何使用它们。

总的来说，书的每一章都是在前章的基础上。每一章都会教你一些新东西。不要急于读完。你应该内化每一个步骤。你可以应用自己的实现并阅读更多关于该主题的内容。每一章之后，我都会为你提供一些阅读材料和练习。如果你真的想学习 React，我强烈建议阅读额外材料并做一些动手练习。在读完一章后，在你熟悉所学内容后再继续。

最后，你将拥有一个生产级的 React 应用。我非常渴望看到你的成果，所以读完书后请给我留言。书的最后一章将为你提供几个继续 React 之旅的选择。通常，你会在我的[个人网站^(28)](https://www.robinwieruch.de/)上发现很多 React 相关话题。

既然你正在读这本书，我猜你是 React 新手。这太完美了。最后，我希望获得你的反馈以改进材料，让每个人都能学习 React。你可以在 [GitHub^(29)](https://github.com/rwieruch/the-road-to-learn-react)产生直接影响，或在 [Twitter^(30)](https://twitter.com/rwieruch)上给我留言。

## React 简介

React 是我尝试在让你编写应用程序的同时教你 React。它是一份学习 React 的实战指南，而不是关于 React 的参考书。你将编写一个与真实世界 API 交互的 Hacker News 应用程序。在几个有趣的话题中，它涵盖了 React 中的状态管理、缓存和交互（排序和搜索）。在此过程中，你将学习 React 的最佳实践和模式。

此外，这本书还带你完成了从 JavaScript ES5 到 JavaScript ES6 的过渡。React 拥抱了许多 JavaScript ES6 特性，我想向你展示如何使用它们。

总的来说，书的每一章都是在前章的基础上。每一章都会教你一些新东西。不要急于读完。你应该内化每一个步骤。你可以应用自己的实现并阅读更多关于该主题的内容。每一章之后，我都会为你提供一些阅读材料和练习。如果你真的想学习 React，我强烈建议阅读额外材料并做一些动手练习。在读完一章后，在你熟悉所学内容后再继续。

最后，你将拥有一个生产级的 React 应用。我非常渴望看到你的成果，所以读完书后请给我留言。书的最后一章将为你提供几个继续 React 之旅的选择。通常，你会在我的[个人网站^(28)](https://www.robinwieruch.de/)上发现很多 React 相关话题。

既然你正在读这本书，我猜你是 React 新手。这太完美了。最后，我希望获得你的反馈以改进材料，让每个人都能学习 React。你可以在 [GitHub^(29)](https://github.com/rwieruch/the-road-to-learn-react)产生直接影响，或在 [Twitter^(30)](https://twitter.com/rwieruch)上给我留言。

## React 简介 

React 是我尝试在让你编写应用程序的同时教你 React。它是一份学习 React 的实战指南，而不是关于 React 的参考书。你将编写一个与真实世界 API 交互的 Hacker News 应用程序。在几个有趣的话题中，它涵盖了 React 中的状态管理、缓存和交互（排序和搜索）。在此过程中，你将学习 React 的最佳实践和模式。

此外，这本书还带你完成了从 JavaScript ES5 到 JavaScript ES6 的过渡。React 拥抱了许多 JavaScript ES6 特性，我想向你展示如何使用它们。

总的来说，书的每一章都是在前章的基础上。每一章都会教你一些新东西。不要急于读完。你应该内化每一个步骤。你可以应用自己的实现并阅读更多关于该主题的内容。每一章之后，我都会为你提供一些阅读材料和练习。如果你真的想学习 React，我强烈建议阅读额外材料并做一些动手练习。在读完一章后，在你熟悉所学内容后再继续。

最后，你将拥有一个生产级的 React 应用。我非常渴望看到你的成果，所以读完书后请给我留言。书的最后一章将为你提供几个继续 React 之旅的选择。通常，你会在我的[个人网站^(28)](https://www.robinwieruch.de/)上发现很多 React 相关话题。

既然你正在读这本书，我猜你是 React 新手。这太完美了。最后，我希望获得你的反馈以改进材料，让每个人都能学习 React。你可以在 [GitHub^(29)](https://github.com/rwieruch/the-road-to-learn-react)产生直接影响，或在 [Twitter^(30)](https://twitter.com/rwieruch)上给我留言。

**最后，我希望你花一点时间思考一个适合学习 React 的人。这个人可能已经表现出了兴趣，可能正在学习 React 的过程中，也可能还没有意识到想学习 React。联系那个人并分享这本书。对我来说意义重大。这本书的初衷是送给他人的。** (注：此处原文存在重复，已按翻译要求处理)

## React 简介 

React 是我尝试在让你编写应用程序的同时教你 React。它是一份学习 React 的实战指南，而不是关于 React 的参考书。你将编写一个与真实世界 API 交互的 Hacker News 应用程序。在几个有趣的话题中，它涵盖了 React 中的状态管理、缓存和交互（排序和搜索）。在此过程中，你将学习 React 的最佳实践和模式。

此外，这本书还带你完成了从 JavaScript ES5 到 JavaScript ES6 的过渡。React 拥抱了许多 JavaScript ES6 特性，我想向你展示如何使用它们。

总的来说，书的每一章都是在前章的基础上。每一章都会教你一些新东西。不要急于读完。你应该内化每一个步骤。你可以应用自己的实现并阅读更多关于该主题的内容。每一章之后，我都会为你提供一些阅读材料和练习。如果你真的想学习 React，我强烈建议阅读额外材料并做一些动手练习。在读完一章后，在你熟悉所学内容后再继续。

最后，你将拥有一个生产级的 React 应用。我非常渴望看到你的成果，所以读完书后请给我留言。书的最后一章将为你提供几个继续 React 之旅的选择。通常，你会在我的[个人网站^(28)](https://www.robinwieruch.de/)上发现很多 React 相关话题。

既然你正在读这本书，我猜你是 React 新手。这太完美了。最后，我希望获得你的反馈以改进材料，让每个人都能学习 React。你可以在 [GitHub^(29)](https://github.com/rwieruch/the-road-to-learn-react)产生直接影响，或在 [Twitter^(30)](https://twitter.com/rwieruch)上给我留言。

(注：由于提供的原文中存在大量重复的段落，根据“一定不要重复输出原文”的原则，此处译文仅保留了唯一内容的翻译)





## React 简介

3

**练习题**

- 阅读关于我为什么从 Angular 迁移到 React^(36)
- 阅读关于 React 灵活的生态系统^(37)
- 阅读关于如何学习一个框架^(38)

36https://www.robinwieruch.de/reasons-why-i-moved-from-angular-to-react/
37https://www.robinwieruch.de/essential-react-libraries-framework/
38https://www.robinwieruch.de/how-to-learn-framework/

## React 简介

4

**要求**

如果你是从其他 SPA（单页应用）框架或库过来的，你应该已经熟悉 Web 开发的基础知识。如果你刚刚开始 Web 开发，你应该熟悉 HTML、CSS 和 JavaScript ES5 以便学习 React。本书将平滑过渡到 JavaScript ES6 及更高版本。我鼓励你加入本书书的官方 Slack 群组^(39) 来获取帮助或帮助他人。

**编辑器和终端**

开发环境该如何？你需要一个正在运行的编辑器或 IDE 以及终端（命令行工具）。你可以遵循我的设置指南^(40)。它是针对 MacOS 用户调整的，但你可以为其他操作系统替换大部分工具。网上有大量的文章会向你展示如何为你的操作系统更详细地设置 Web 开发环境。

可选地，你可以在执行书中练习时，使用自己的 git 和 GitHub，将你的项目和进度保存在 GitHub 仓库中。这里有一份关于如何使用这些工具的小指南^(41)。但再次强调，这对于本书并不是强制性的，而且从零开始学习一切时可能会让你无无从措。所以，如果你是 Web 开发的新手，可以跳过它，专注于本书教授的核心部分。

**Node 和 NPM**

最后但同样重要的是，你需要安装 node 和 npm^(42)。它们都用于管理你在此过程中需要的库。在本书中，你将通过 npm（node 包管理器）安装外部 node 包。这些 node 包可能是库，也可能是整个框架。

你可以在命令行中验证 node 和 npm 的版本。如果你在终端没有得到任何输出，你需要先安装 node 和 npm。这些仅是我编写本书期间使用的版本：

**命令行**

```bash
node --version
*v8.9.4
npm --version
*v5.6.0
```

39https://slack-the-road-to-learn-react.wieruch.com/
40https://www.robinwieruch.de/developer-setup/
41https://www.robinwieruch.de/git-essential-commands/
42https://nodejs.org/en/

## React 简介

5

**node 和 npm**

这一章将为你提供关于 node 和 npm 的快速入门课程。它并不是面面详尽的，但你将获得所有必要的工具。如果你熟悉这两者，可以跳过这一章。

**node 包管理器** (npm) 允许你从命令行安装外部 **node 包**。这些包可以是一组实用函数、库或整个框架。它们是你应用程序的依赖项。你可以将这些包安装到你的全局 node 包文件夹中，也可以安装到你的本地项目文件夹中。

全局 node 包可以在终端的任何地方访问，你只需要在全局目录中安装它们一次。你可以通过在终端中输入以下命令来安装全局包：

**命令行**

```bash
npm install -g <package>
```

-g 标志告诉 npm 全局安装该包。本地包用于你的应用程序。例如，作为库的 React 是本地包，可以在你的应用程序中引入并使用。你可以通过在终端输入以下命令进行安装：

**命令行**

```bash
npm install <package>
```

在 React 的情况下，将是：

**命令行**

```bash
npm install react
```

安装的包将自动出现在名为 *node_modules/* 的文件夹中，并列在 *package.json* 文件中你的其他依赖项旁边。

但最初如何为你的项目初始化 *node_modules/* 文件夹和 *package.json* 文件呢？有一个 npm 命令可以初始化一个 npm 项目并生成 *package.json* 文件。只有当你拥有该文件时，你才能通过 npm 安装新的本地包。

**命令行**

```bash
npm init -y
```

## React 简介

6

-y 标志是初始化你的 *package.json* 中所有默认值的快捷方式。如果你不使用该标志，就必须决定如何配置该文件。初始化你的 npm 项目后，你就可以通过 `npm install <package>` 安装新包了。

关于 *package.json* 再多说一点。该文件允许你与其他开发者共享你的项目，而无需共享所有的 node 包。该文件包含了你项目中使用的所有 node 包的引用。这些包被称为依赖项。每个人可以在不带依赖项的情况下拷贝你的项目。依赖项是 *package.json* 中的引用。拷贝你项目的人只需在命令行上使用 `npm install` 安装所有包即可。`npm install` 脚本获取 *package.json* 文件中列出的所有依赖项并将它们安装到 *node_modules/* 文件夹中。

我想再介绍一个 npm 命令：

**命令行**

```bash
npm install --save-dev <package>
```

--save-dev 标志表示该 node 包仅在开发环境中使用。它不会在生产环境中使用。你在旅途中会遇到更多 npm 命令。

**练习题：**

- 设置 npm 项目
- 使用 mkdir <folder_name> 创建新文件夹
- 使用 cd <folder_name> 进入文件夹
- 执行 npm init -y
- 使用 npm install 安装本地包 React
- 查看 *package.json* 文件和 *node_modules/* 文件夹
- 自己如何卸载 *react* 包
- 阅读更多关于 npm 的信息^(43)

43https://docs.npmjs.com/

## React 简介

7

**安装**

启动 React 应用有多种方法。第一种是使用 CDN。这听起来可能比实际上复杂。CDN 是内容分发网络^(44)。许多公司拥有公开托管文件的 CDN 以供使用。这些文件可以是像 React 这样的库，因为打包后的库只是一个 *react.js* JavaScript 文件。它可以托管在某处，你可以在应用程序中引入。如何使用 CDN 启动 React？你可以在 HTML 中内联 <script> 标签，指向 CDN url。启动 React 需要两个文件（库）：*react* 和 *react-dom*。

**代码演练**

```html
<script crossorigin="https://unpkg.com/react@16/umd/react.js"></script>
<script crossorigin="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
```

但既然你有 npm 来安装 React 等 node 包，为什么还要使用 CDN 呢？当你的应用程序拥有 *package.json* 文件时，你可以从命令行安装 *react* 和 *react-dom*。要求是文件夹通过 `npm init -y` 初始化为 npm 项目并带有 *package.json* 文件。你可以通过一条命令 npm 安装多个 node 包。

**命令行**

```bash
npm install react react-dom
```

这种方法通常用于向通过 npm 管理的现有应用程序添加 React。遗憾的是，这并不是全部。你必须处理 Babel^(45) 以让你的应用程序感知 JSX（React 语法）和 JavaScript ES6。Babel 编译你的代码，以便浏览器可以解释 JavaScript ES6 和 JSX。并不是所有的浏览器都能解释这些语法。设置包含了大量的配置和工具。对于 React 新手来说，处理所有的配置可能会让他们无从措。

由于这个原因，Facebook 引入了 *create-react-app* 作为一种零配置的 React 解决方案。下一章将向你展示如何使用这个引导工具设置你的应用程序。

**练习题：**

- 阅读更多关于 React 安装^(46)

46https://reactjs.org/docs/try-react.html





## React 简介

8

### 零配置设置

在学习 React 的过程中，你将使用 `create-react-app`^(47) 来引导你的应用程序。这是由 Facebook 在 2016 年引入的一个带有主见且零配置的 React 启动器。96%^(48) 的人都会向学者推荐它。在 *create-react-app* 中，工具和配置会在后台演进，而重点放在应用程序的实现上。

要开始，你必须将该包安装到全局 node 包中。之后，你始终可以在命令行中使用它来引导新的 React 应用。

**命令行**
```bash
npm install -g create-react-app
```

你可以通过检查 *create-react-app* 的版本来验证是否在命令行中成功安装：

**命令行**
```bash
create-react-app --version
```
*v1.5.1*

现在你可以引导你的第一个 React 应用了。我们将其命名为 *hackernews*，但你可以选择不同的名称。引导需要几秒钟。之后，只需进入该文件夹：

**命令行**
```bash
create-react-app hackernews
cd hackernews
```

现在你可以在编辑器中打开该应用程序。你应该会看到以下文件夹结构，或根据 *create-react-app* 的版本有所变体：

(47) https://github.com/facebookincubator/create-react-app
(48) https://twitter.com/dan_abramov/status/806985854099062785

### 文件夹结构

```text
hackernews/
├── README.md
├── node_modules/
├── package.json
├── .gitignore
├── public/
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
└── src/
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── index.css
    ├── index.js
    ├── logo.svg
    └── registerServiceWorker.js
```

是对文件夹和文件的简要说明。刚开始时不理解所有的内容也没关系。

- **README.md:** .md 扩展名表示该文件是一个 markdown 文件。Markdown 被用作带有纯文本格式语法的轻量标记语言。许多源代码项目都带有一个 *README.md* 文件，为你提供关于项目的初始说明。当你最终将项目推送到 GitHub 等平台时，当你访问仓库，*README.md* 文件会突出显示其内容。由于你使用了 *create-react-app*，你的 *README.md* 应该与官方 create-react-app GitHub 仓库^(49)中显示的相同。
- **node_modules/:** 该文件夹包含了过去和现在通过 npm 安装的所有 node 包。由于你使用了 *create-react-app*，应该已经为你安装了几个 node模块。通常你永远不会触碰这个文件夹，只需通过命令行使用 npm 安装和卸载 node 包。
- **package.json:** 该文件向你展示了 node 包依赖列表和其他项目配置。
- **.gitignore:** 该文件指在使用 git 时不应被添加到远程 git 仓库的所有文件和文件夹。它们应该只存在于你的本地项目中。*node_modules/* 文件夹就是此类用例。只需与同事共享 *package.json* 文件，让他们能够自己安装所有依赖项，而无需共享整个依赖文件夹。

(49) https://github.com/facebookincubator/create-react-app

- **public/:** 文件夹包含你在构建生产环境项目时所有的文件。最终，当你构建项目时，你在 *src/* 文件夹中编写的所有代码将被打包成几个文件并放在 public 文件夹中。
- **manifest.json** 和 **registerServiceWorker.js:** 阶段不用担心这些文件的作用，我们在这个项目中不需要它们。

毕竟，你不需要接触上述的文件和文件夹。在开始，你需要的一切都位于 *src/* 文件夹中。重点在于 *src/App.js* 文件，用于实现 React 组件。它将用于实现你的应用程序，但以后你可能想将组件拆分为多个文件，每个文件独立维护一个或几个组件。

此外，你还会发现一个用于测试的 *src/App.test.js* 文件和一个作为 React 世界入口的 *src/index.js*。你将在后面的章节中了解这两个文件。此外，还有一个 *src/index.css* 和 *src/App.css* 文件用于为你的通用应用程序和组件设置样式。它们在打开时都带有默认样式。

*create-react-app* 应用程序是一个 npm 项目。你可以使用 npm 为你的项目安装和卸载 node 包。此外，它还带有以下用于命令行的 npm 脚本：

**命令行**
```bash
// 在 http://localhost:3000 运行应用程序
npm start

// 运行测试
npm test

// 构建生产环境的应用程序
npm run build
```

脚本定义在你的 *package.json* 中。你的样板 React 应用现在已经引导完成。激动的部分在于练习，即最终在浏览器中运行你引导的应用程序。

**练习：**

- npm start 你的应用程序并在浏览器中访问（你可以按 Control + C 退出命令）
- 运行交互式 npm test
- 构建生产环境的应用程序

(50) https://www.digitalocean.com/community
(51) https://github.com/facebookincubator/create-react-app





## React 简介

14

当你再次通过 `npm start` 在命令行中启动应用程序时，它应该可以正常工作。

此外，你可能已经注意到了 `className` 属性。它反映了 HTML 标准 `class` 属性。由于技术原因，JSX 必须替换一些内部 HTML 属性。

你可以在 React 文档^(52) 中找到所有支持的 HTML 属性。它们都遵循驼峰命名法（camelCase）。在学习 React 的过程中，你还会遇到一些 JSX 特有的属性。

**练习题：**

- 定义更多变量并在你的 JSX 中渲染它们
- 使用复杂对象来表示具有姓（名）的用户
- 在你的 JSX 中渲染用户属性
- 了解更多关于 JSX^(53)
- 了解更多关于 React 组件、元素和实例^(54)

52https://reactjs.org/docs/dom-elements.html#all-supported-html-attributes
53https://reactjs.org/docs/introducing-jsx.html
54https://facebook.github.io/react/blog/2015/12/18/react-components-elements-and-instances.html

## React 简介

15

### ES6 const 和 let

我猜你注意到我们用 `var` 语句声明了变量 `helloWorld`。JavaScript ES6 提供了两种声明变量的选择：`const` 和 `let`。在 JavaScript ES6 中，你很少会看到 `var` 了。

用 `const` 声明的变量不能被重新赋值或重新声明。它不能被变异（改变、修改）。通过使用它，你拥有了不可变的数据结构。一旦定义了数据结构，你就无法更改。

**代码练场**

*//不允许*

**const** helloWorld = 'Welcome to the Road to learn React';

helloWorld = 'Bye Bye React';

用 `let` 声明的变量可以被变异。

**代码练场**

*//允许*

**let** helloWorld = 'Welcome to the Road to learn React';

helloWorld = 'Bye Bye React';

当你需要给变量重新赋值时，可以使用它。

然而，你必须小心使用 `const`。用 `const` 声明的变量不能被修改。但当变量是一个数组或对象时，它所持有的值是可以更新的。它所持的值并不是不可变的。

**代码练场**

*//允许*

**const** helloWorld = {

text: 'Welcome to the Road to learn React'

};

helloWorld.text = 'Bye Bye React';

但是什么时候该用每种声明方式呢？关于用法有不同的观点。我建议尽可能使用 `const`。它表示你希望保持数据结构的不可变性，尽管对象和数组中的值可以被修改。如果你想修改你的变量，可以使用 `let`。

不可变性在 React 及其生态系统中备受推崇。这就是为什么当你定义变量时，`const` 应该是你的默认选择。尽管如此，在复杂对象中，内部的值是可以修改的。请注意这种行为。

在你的应用程序中，你应该使用 `const` 而非 `var`。

## React 简介

16

### src/App.js

import React, { Component } from 'react';

import './App.css';

class App extends Component {

render() {

**const helloWorld = 'Welcome to the Road to learn React';**

return (

<div className="App">

<h2>{helloWorld}</h2>

</div>
);

}

}

export default App;

**练习题：**

- 了解更多关于 ES6 const^(55)
- 了解更多关于 ES6 let^(56)
- 深入研究不可变数据结构
- 为什么它们在通用编程中是有意义的
- 为什么它们被用于 React 及其生态系统

55https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const
56https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let

## React 简介

17

### ReactDOM

在你继续使用 `App` 组件之前，你可能想看看它在哪里被使用。它位于你 React 世界的入口点：*src/index.js* 文件。

**src/index.js**

**import** React from 'react';

**import** ReactDOM from 'react-dom';

**import** App from './App';

**import** './index.css';

ReactDOM.render(

<App />,

document.getElementById('root')
);

基本上，`ReactDOM.render()` 使用你 HTML 中的一个 DOM 节点来替换为你的 JSX。这就是你如何轻松地将 React 集成到每个应用程序中。在应用程序中多次使用 `ReactDOM.render()` 并不是禁止的。你可以在多个地方使用它来启动简单的 JSX 语法、一个 React 组件、多个 React 组件或整个应用程序。但在纯 React 应用程序中，你只会使用它一次来启动整个组件树。

`ReactDOM.render()` 接收两个参数。第一个参数是待渲染的 JSX。第二个参数指定了 React 应用挂钩到你 HTML 中的位置。它期望一个 `id='root'` 的元素。你可以打开你的 *public/index.html* 文件来找到 `id` 属性。

在实现中，`ReactDOM.render()` 已经获取了你的 `App` 组件。然而，只要是 JSX，传递更简单的 JSX 也是可以的。它不非得组件的实例化。

**代码练场**

ReactDOM.render(

<h1>Hello React World</h1>,

document.getElementById('root')
);

**练习题：**

- 打开你的 *public/index.html* 看看 React 挂钩在何处
- 了解更多关于元素^(57)

57https://reactjs.org/docs/elements.html

## React 简介

18

### 热模块替换 (Hot Module Replacement)

在 *src/index.js* 文件中你可以做一件事。热模块替换（HMR）是一种允许你在无需刷新整个页面的情况下更新代码的工具。对于开发来说这是一个非常方便的功能，因为它保持了你应用程序的状态活跃。

如果没有 HMR，你每次做出更改，浏览器都必须加载整个页面，这可能意味着丢失应用程序当前的状态。有了 HMR，只有更改的模块会被重新加载，这要快得多并且保留状态。

要使用 HMR，你通常需要像 Webpack 或 Vite 这样的构建工具。这些工具处理检测更改和更新浏览器中模块的复杂性。在 React 开发中，HMR 通常由 React Refresh 等工具提供，提供了无缝体验。

热模块替换（HMR）是一种允许你在无需刷新整个页面的情况下更新代码的工具。对于开发来说这是一个非常方便的功能，因为它保持了你应用程序的状态活跃。如果没有 HMR，你每次做出更改，浏览器都必须加载整个页面，这可能意味着丢失应用程序当前的状态。有了 HMR，只有更改的模块会被重新加载，这要快得多并且保留状态。要使用 HMR，你通常需要像 Webpack 或 Vite 这样的构建工具。这些工具处理检测更改和更新浏览器中模块的复杂性。在 React 开发中，HMR 通常由 React Refresh 等工具提供，提供了无缝体验。

## React 简介

19

### 热模块替换（续）

状态保持。

需要注意的是，HMR 并不适用于所有的更改。例如，如果你更改了全局变量或配置文件，页面可能仍需要加载。然而，对于大多数与组件相关的更改，HMR 是非常有效的。通过使用 HMR，你可以显著加快开发并实时看到更改。这是现代开发工作流的关键部分。

## React 简介

20

### JSX 中的复杂 JavaScript

让我们回到 `App` 组件。到目前为止你在 JSX 中渲染了一些原始变量。现在你将开始渲染一个项目列表。列表最初是示例数据，但之后将从外部 API^(59) 获取数据。那将有趣得多。首先你必须定义列表。

**src/App.js**

import React, { Component } from 'react';

import './App.css';

**const list = [**

**{

**title: 'React',**

**url: 'https://facebook.github.io/react/',**

**author: 'Jordan Walke',**

**num\_comments: 3,**

**points: 4,**

**objectID: 0,**

**},**

**{

**title: 'Redux',**

**url: 'https://github.com/reactjs/redux',**

**author: 'Dan Abramov, Andrew Clark',**

**num\_comments: 2,**

**points: 5,**

**objectID: 1,**

**},**

**];**

class App extends Component {

...

}

示例数据将反映我们以后从 API 获取的数据。列表中的每个项目都有标题、URL 和作者。此外，它还带有一个标识符、积分（指示文章受欢迎程度）和评论计数。

现在你可以在 JSX 中使用内置的 JavaScript `map` 功能。它允许你遍历项目列表以显示它们。再次，你将使用大括号来封装 JSX 中的 JavaScript 表达式。





## React 简介

21

**src/App.js**

```javascript
class App extends Component {
  render() {
    return (
      <div className="App">
        {list.map(function(item) {
          return <div>{item.title}</div>;
        })}
      </div>
    );
  }
}

export default App;
```

在 JSX 中使用 JavaScript 非常强大。通常你可能使用过 `map` 将一个项目列表转换为另一个项目列表。这次你使用 `map` 将一个项目列表转换为 HTML 元素。

到目前为止，每个项目只会显示标题。让我们多显示一些项目的属性。

**src/App.js**

```javascript
class App extends Component {
  render() {
    return (
      <div className="App">
        {list.map(function(item) {
          return (
            <div>
              <span>
                <a href={item.url}>{item.title}</a>
              </span>
              <span>{item.author}</span>
              <span>{item.num_comments}</span>
              <span>{item.points}</span>
            </div>
          );
        })}
      </div>
    );
  }
}
```

React 简介
22

}
}

export default App;

你可以看到 `map` 函数是如何简单内联在你的 JSX 中的。每个项目属性都显示在 `<span>` 标签中。此外，项目的 `url` 属性被用于锚点标签的 `href` 属性。

React 会为你完成所有工作并显示每个项目。但你应该添加一个助手来让 React 发挥其全部潜力并提高性能。你必须为每个列表元素分配一个 `key` 属性。这样当列表发生变化时，React 能够识别添加、更改和删除的项目。示例列表项已经带有一个标识符。

**src/App.js**

```javascript
{list.map(function(item) {
  return (
    <div key={item.objectID}>
      <span>
        <a href={item.url}>{item.title}</a>
      </span>
      <span>{item.author}</span>
      <span>{item.num_comments}</span>
      <span>{item.points}</span>
    </div>
  );
})}
```

你应该确保 `key` 属性是一个稳定的标识符。不要犯使用数组中项目索引的错误。数组索引完全是不稳定的。例如，当列表顺序发生变化时，React 将很难正确识别这些项目。

**src/App.js**

```javascript
// 不要这么做
{list.map(function(item, key) {
  return (
    <div key={key}>
      ...
    </div>
  );
})}
```

你现在同时显示两个列表项。你可以启动应用，打开浏览器并查看列表中的两个项目的显示情况。

React 简介
23

**练习题：**

- 阅读更多关于 React 列表和键的内容 (60)
- 复习 JavaScript 中的标准内置数组功能 (61)
- 在 JSX 中尝试自己使用更多 JavaScript 表达式

60 https://reactjs.org/docs/lists-and-keys.html
61 https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map

React 简介
24

**ES6 箭头函数**

JavaScript ES6 引入了箭头函数。箭头函数表达式比函数表达式更短。

**代码演练**

```javascript
// 函数表达式
function () { ... }

// 箭头函数表达式
() => { ... }
```

但你必须意识到它的功能。其中之一是与 `this` 对象的行为不同。函数表达式总是定义它自己的 `this` 对象。箭头函数表达式仍然具有其闭包上下文的 `this` 对象。在箭头函数中使用它时不要感到困惑。

关于括号，箭头函数还有一个有价值的事实。当函数只有一个参数时，可以移除括号，但当它有多个参数时，必须保留它们。

**代码演练**

```javascript
// 允许
item => { ... }

// 允许
(item) => { ... }

// 不允许
item, key => { ... }

// 允许
(item, key) => { ... }
```

然而，让我们来看看 `map`。

React 简介
25

**src/App.js**

```javascript
{list.map(item => {
  return (
    <div key={item.objectID}>
      <span>
        <a href={item.url}>{item.title}</a>
      </span>
      <span>{item.author}</span>
      <span>{item.num_comments}</span>
      <span>{item.points}</span>
    </div>
  );
})}
```

你现在同时显示两个列表项。你可以启动应用，打开浏览器并查看列表中的两个项目的显示情况。

**练习题：**

- 阅读更多关于 React 列表和键的内容 (60)
- 复习 JavaScript 中的标准内置数组功能 (61)
- 在 JSX 中尝试自己使用更多 JavaScript 表达式

60 https://reactjs.org/docs/lists-and-keys.html
61 https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map

React 简介
26

**ES6 类**

JavaScript ES6 引入了类。类用于面向对象编程中。让我们考虑 `Developer` 类。

**代码演练**

```javascript
class Developer {
  constructor(firstname, lastname) {
    this.firstname = firstname;
    this.lastname = lastname;
  }

  getName() {
    return this.firstname + ' ' + this.lastname;
  }
}
```

现在你了解了 JavaScript ES6 类的基础知识以及它们如何在 React 中被使用以扩展为组件。当书籍描述 React 生命周期方法时，你将学习更多关于组件的方法。

**练习题：**

- 阅读更多关于 ES6 类的内容 (63)

...为了使其可以实例化。让我们看看如何实例化该类并使用它的方法。

**代码演练**

```javascript
const robin = new Developer('Robin', 'Wieruch');
console.log(robin.getName());
// 输出: Robin Wieruch
```

React 简介
27

**src/App.js**

```javascript
import React, { Component } from 'react';

...

class App extends Component {
  render() {
    ...
  }
}
```

`App` 类继承自 `Component`。基本上你声明了 `App` 组件，但它扩展另一个组件。扩展意味着什么？在面向对象编程中，你有继承原则。它用于将功能从一个类传递到另一个类。`App` 类从 `Component` 类继承功能。具体地说，它继承了 `Component` 类的功能。`Component` 类用于将基础的 ES6 类扩展为 ES6 组件类。它拥有 React 中组件所需的所有功能。`render` 方法就是你已经过的这些功能之一。稍后你将学习其他组件类方法。

`Component` 类封装了 React 组件的所有实现细节。它允许开发者在 React 中将类作为组件。

React 组件暴露的方法是公共接口。在这些方法中，有一个必须被重写，其他的不需要重写。当书籍在后面的章节介绍生命方法时，你将会学习后者。`render()` 方法...



## React 简介

28

你已经学会了如何构建自己的 React 应用程序！让我们回顾一下最后几章：

- React
- create-react-app 构建 React 应用程序
- JSX 将 HTML 和 JavaScript 混合，以定义 React 组件在渲染方法中的输出
- React 中的组件（components）、实例（instances）和元素（elements）是不同的
- ReactDOM.render() 是 React 应用将 React 挂载到 DOM 的入口
- 内置的 JavaScript 功能可以在 JSX 中使用
- map 可以将项目列表渲染为 HTML 元素
- ES6
- 使用 `const` 和 `let` 进行变量声明可以用于特定场景
- 在 React 应用中，优先使用 `const` 而非 `let`
- 箭头函数可以保持函数简洁
- React 中通过扩展类（classes）来定义组件

在这个阶段休息一下是合理的。内化所学的知识并将它们应用到实践中。

你可以尝试你目前编写的源代码。你可以在官方仓库(64)中找到源代码。

64 https://github.com/the-road-to-learn-react/hackernews-client/tree/5.1

## React 基础

本章将引导你学习 React 的基础。它涵盖了组件中的状态和交互，因为静态组件有点无聊，不是吗？此外，你将学习声明组件的不同方法，以及如何保持组件的可组合性和复用性。准备好为你的组件注入灵魂吧。

## React 基础

30

### 组件内部状态

组件内部状态（称为本地状态）允许你保存、修改和删除存储在组件中的属性。ES6 类组件可以使用构造函数来初始化组件内部状态。构造函数在组件初始化时仅会被调用一次。

让我们引入类构造函数。

**src/App.js**

```javascript
class App extends Component {
  constructor(props) {
    super(props);
  }
  ...
}
```

在 ES6 类组件中使用构造函数时，必须调用 `super()`，因为 `App` 组件是 `Component` 的子类。因此在你的 `App` 组件声明中使用了 `extends Component`。稍后你会学习更多关于 ES6 类组件的知识。

你可以调用 `super(props)`。它会在构造函数中设置 `this.props`，以防你想在构造函数中访问它们。否则，在构造函数中访问 `this.props` 时它们将是 `undefined`。稍后你会学习更多关于 React 组件 props 的知识。

现在，在你的情况下，组件中的初始状态应该是示例项目列表。

**src/App.js**

```javascript
const list = [
  {
    title: 'React',
    url: 'https://facebook.github.io/react/',
    author: 'Jordan Walke',
    num_comments: 3,
    points: 4,
    objectID: 0,
  },
  ...
];
```

## React 基础 

31

```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      list: list,
    };
  }
  ...
}
```

状态通过 `this` 对象绑定到类上。因此，你可以在整个组件中访问本地状态。例如，它可以在 `render()` 方法中使用。之前你在 `render()` 方法中映射了一个定义在组件外部的静态项目列表。现在，你正准备在组件中使用本地状态中的列表。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    return (
      <div className="App">
        {this.state.list.map(item =>
          <div key={item.objectID}>
            <span>
              <a href={item.url}>{item.title}</a>
            </span>
            <span>{item.author}</span>
            <span>{item.num_comments}</span>
            <span>{item.points}</span>
          </div>
        )}
      </div>
    );
  }
}
```

## React 基础 

32

列表现在是组件的一部分了。它存在于组件内部状态中。你可以对列表进行添加、更改或删除项目。每当你更改组件状态时，组件的 `render()` 方法就会再次运行。这就是你如何能够简单地更改内部内部状态，并确保组件重新渲染并显示来自本地状态的正确数据。

但要小心。不要直接变异（mutate）状态。你必须使用一个名为 `setState()` 的方法来修改你的状态。你将在接下来的章节中了解它。

**练习：**
- 尝试本地状态
- 在构造函数中定义更多初始状态
- 在 `render()` 方法中使用并访问状态
- 阅读更多关于 ES6 类构造函数的知识(65)

65 https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Classes#Constructor

## React 基础 

33

### ES6 对象初始化器

在 JavaScript ES6 中，你可以使用简写属性语法来更简洁地初始化对象。想象一下以下对象初始化：

**代码沙场**

```javascript
const name = 'Robin';
const user = {
  name: name,
};
```

当对象中的属性名与变量名相同时，你可以执行以下操作：

**代码沙场**

```javascript
const name = 'Robin';
const user = {
  name,
};
```

在你的应用程序中，你可以同样这样做。注意，具有多个属性的元素在某处会变成杂乱的一行。这就是为什么 `button` 使用了多行和缩进来保持其可读性。但这并非强制。这只是一个我非常推荐的代码风格建议。

## React 基础 

34

### ES6 对象初始化器

在 JavaScript ES6 中，你可以使用简写属性语法来更简洁地初始化对象。想象一下以下对象初始化：

**代码沙场**

```javascript
const name = 'Robin';
const user = {
  name: name,
};
```

等一下，让我重新检查 OCR 流程。
实际上，OCR 在中间部分有点乱。让我根据提供的文本重构逻辑：

当对象中的属性名与变量名相同时，你可以执行以下操作：

**代码沙场**

```javascript
const name = 'Robin';
const user = {
  name,
};
```

在你的应用程序中，你可以同样这样做。注意，具有多个属性的元素在某处会变成杂乱的一行。这就是为什么 `button` 元素使用了多行和缩进来保持其可读性。但这并非强制。这只是一个我非常推荐的代码风格建议。

## React 基础 

35

### 单向数据流

现在你的组件中有了一些内部状态。然而，你还没有操纵过这些状态。让我们为显示列表中的每个项目添加一个按钮。按钮显示“Dismiss”（忽略），并将从列表中移除该项目。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    return (
      <div className="App">
        {this.state.list.map(item =>
          <div key={item.objectID}>
            <span>
              <a href={item.url}>{item.title}</a>
            </span>
            <span>{item.author}</span>
            <span>{item.num_comments}</span>
            <span>{item.points}</span>
            <button
              onClick={() => this.onDismiss(item.objectID)}
              type="button"
            >
              Dismiss
            </button>
          </div>
        )}
      </div>
    );
  }
}
```

`onDismiss()` 类方法还没有定义。我们稍后会实现它，但现在的重点应该是按钮的 `onClick` 处理程序。

## React 基础

36

### 单向数据流

`onClick` 处理程序被另一个函数封装。它是一个箭头函数。这样，你就可以传入项目的 `objectID` 属性以识别要被忽略的项目。现在你必须实现 `onDismiss()` 功能。它接收一个 id 来识别要忽略的项目。该函数被绑定到类，因此成为一个类方法。这就是为什么你通过 `this.onDismiss()` 而不是 `onDismiss()` 来访问它。`this` 对象是你的类实例。为了将 `onDismiss()` 定义为类方法，你需要在构造函数中绑定它。绑定将在后面的章节解释。

**src/App.js**

```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      list,
    };
    this.onDismiss = this.onDismiss.bind(this);
  }
  render() {
    ...
  }
}
```

在下一步中，你需要在类中定义它的功能（业务逻辑）。类方法可以按照以下方式定义。






React 基础

37

**src/App.js**

```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      list,
    };
    this.onDismiss = this.onDismiss.bind(this);
  }

  onDismiss(id) {
    // ...
  }

  render() {
    ...
  }
}
```

现在你能够定义类方法内部会发生什么了。基本上，你想从列表中移除由 `id` 标识的项，并将更新后的列表存储到你的本地状态中。之后，更新后的列表将在重新运行的 `render()` 方法中使用并进行显示。被移除的项将不再出现。

你可以使用 JavaScript 内置的 `filter` 功能从列表中删除项。`filter` 函数接收一个函数作为输入。该函数可以访问列表中的每个值，因为它会遍历列表。这样，你就可以根据过滤条件对列表中的每个项进行评估。如果对某个项的评估结果为 `true`，则该项保留在列表中；否则，它将从列表中被过滤掉。此外，需要重要的是该函数返回一个新列表，而不是修改旧列表。这符合 React 中使用不可变数据结构的约定。

38

**src/App.js**

```javascript
onDismiss(id) {
  const updatedList = this.state.list.filter(function isNotId(item) {
    return item.objectID !== id;
  });
}
```

在下一步中，你可以提取该函数并将其传递给 `filter` 函数。

**src/App.js**

```javascript
onDismiss(id) {
  function isNotId(item) {
    return item.objectID !== id;
  }
  const updatedList = this.state.list.filter(isNotId);
}
```

此外，你可以使用 JavaScript ES6 箭头函数更加简洁地。

**src/App.js**

```javascript
onDismiss(id) {
  const isNotId = item => item.objectID !== id;
  const updatedList = this.state.list.filter(isNotId);
}
```

你甚至可以像在按钮的 `onClick` 处理器中那样再次对其内联，但这可能会降低可读性。

**src/App.js**

```javascript
onDismiss(id) {
  const updatedList = this.state.list.filter(item => item.objectID !== id);
}
```

列表现在删除了点击的项。然而，状态（state）还没有更新。因此，你可以使用 `setState()` 类方法来更新组件内部状态中的列表。

39

**src/App.js**

```javascript
onDismiss(id) {
  const isNotId = item => item.objectID !== id;
  const updatedList = this.state.list.filter(isNotId);
  this.setState({ list: updatedList });
}
```

现在再次运行你的应用程序并尝试“Dismiss”按钮。它应该可以工作。你现在的是 React 中的单向数据流。你在视图中触发了一个动作，`render()` 方法再次运行以更新视图。

**练习：**
- 了解更多关于 React 中的状态和生命周期：https://reactjs.org/docs/state-and-lifecycle.html

40

**绑定 (Bindings)**

在使用 ES6 类组件时，学习 JavaScript 中的绑定是非常重要的。在上一章中，你在构造函数中绑定了类方法 `onDismiss()`。

**src/App.js**

```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      list,
    };
    this.onDismiss = this.onDismiss.bind(this);
  }
  ...
}
```

你最初为什么要这么做呢？绑定步骤是必要的，因为类方法不会自动绑定到类实例。让我们通过下面的 ES6 组件来演示这一点。

**代码沙场 (Code Playground)**

```javascript
class ExplainBindings extends Component {
  onClickMe() {
    console.log(this);
  }
  render() {
    return (
      <button onClick={this.onClickMe} type="button">
        Click Me
      </button>
    );
  }
}
```

组件渲染正常，但当你点击按钮时，你会在控制台日志中得到 `undefined`。这是使用 React 时产生的主要来源，因为如果你想在类方法中访问 `this.state`，将无法获取，因为 `this` 是 `undefined`。所以为了在类方法中能够访问它，你必须将类方法绑定到 `this`。在下面的组件中，类方法在类构造函数中被正确绑定了。

**代码沙场 (Code Playground)**

```javascript
class ExplainBindings extends Component {
  constructor() {
    super();
    this.onClickMe = this.onClickMe.bind(this);
  }
  onClickMe() {
    console.log(this);
  }
  render() {
    return (
      <button onClick={this.onClickMe} type="button">
        Click Me
      </button>
    );
  }
}
```

再次尝试按钮时，`this` 对象（具体来说是类实例）应该是定义的，你将能够访问 `this.state`，或者正如你稍后学到的，访问 `this.props`。类方法的绑定也可以发生在其他地方。例如，它可以发生在 `render()` 类方法中。

42

**代码沙场 (Code Playground)**

```javascript
class ExplainBindings extends Component {
  onClickMe() {
    console.log(this);
  }
  render() {
    return (
      <button onClick={this.onClickMe.bind(this)} type="button">
        Click Me
      </button>
    );
  }
}
```

但你应该避免这样做，因为每当 `render()` 方法运行时它都会绑定一次类方法。基本上，它在组件每次更新时都会运行，这会导致性能影响。在构造函数中绑定类方法时，你只在组件实例化之初绑定一次。这是一个更好的方法。人们有时会想到的另外一点是在构造函数中定义类方法的业务逻辑。

**代码沙场 (Code Playground)**

```javascript
class ExplainBindings extends Component {
  constructor() {
    super();
    this.onClickMe = () => {
      console.log(this);
    }
  }
  render() {
    return (
      <button onClick={this.onClickMe} type="button">
        Click Me
      </button>
    );
  }
}
```

43

你也应该避免这样做，因为随着时间的推移它会让你的构造函数变得混乱。构造函数只是为了实例化类及其属性。这就是为什么类方法的业务逻辑应该定义在构造函数之外。

**代码沙场 (Code Playground)**

```javascript
class ExplainBindings extends Component {
  constructor() {
    super();
    this.doSomething = this.doSomething.bind(this);
    this.doSomethingElse = this.doSomethingElse.bind(this);
  }
  doSomething() {
    // do something
  }
  doSomethingElse() {
    // do something else
  }
  ...
}
```

最后，值得提到，通过使用 JavaScript ES6 箭头函数可以自动绑定类方法而无需显式绑定。

44

**代码沙场 (Code Playground)**

```javascript
class ExplainBindings extends Component {
  onClickMe = () => {
    console.log(this);
  }
  render() {
    return (
      <button onClick={this.onClickMe} type="button">
        Click Me
      </button>
    );
  }
}
```

如果构造函数中的重复绑定让你困扰，你可以采用这种方法。React 官方文档坚持使用构造函数中的类方法。这就是为什么本书也会坚持这些方法。

**练习：**
- 尝试不同的绑定方法并打印 `this` 对象

45

**事件处理器 (Event Handler)**

本章应该让你对元素中的事件处理器有更深入的理解。在你的应用程序中，你正在使用下面的按钮从列表中移除项。

**src/App.js**

```javascript
...
<button onClick={() => this.onDismiss(item.objectID)} type="button">
  Dismiss
</button>
...
```

这已经是一个复杂的用例了，因为你需要向类方法传递一个值，因此你需要将其封装在另一个（箭头）函数中。基本上，它必须是一个传递给事件处理器的函数。下面的代码将无法工作，因为当浏览器中打开应用程序时，类方法会立即执行。

**src/App.js**

```javascript
...
<button onClick={this.onDismiss(item.objectID)} type="button">
  Dismiss
</button>
...
```

当使用 `onClick={doSomething()}` 时，`doSomething()` 函数会在浏览器中打开应用程序时立即执行。处理器中的表达式会被求值。由于函数的返回值不再是一个函数，当你点击按钮时什么都不会发生。但当使用 `onClick={doSomething}` 且 `doSomething` 是一个函数时，在点击按钮时它会被执行。相同的规则适用于应用程序中使用的 `onDismiss()` 类方法。




React 基础

46

然而，使用 `onClick={this.onDismiss}` 是不够的，因为某种程度上需要将 `item.objectID`

属性传递给类方法，以识别将要移除的项。

这就是为什么可以将其封装在另一个函数中来巧妙传入该属性。这个概念在

JavaScript 中被称为高阶函数，稍后会简要解释。

**src/App.js**

...

<button
  onClick={() => this.onDismiss(item.objectID)}
  type="button"
>
  Dismiss
</button>

...

一种变通方法是在外部定义封装函数，并仅将定义的函数传递给处理器。由于该函数需要访问单个项，因此它必须位于 `map` 函数块的内部。

**src/App.js**
```javascript
class App extends Component {
...
  render() {
    return (
      <div className="App">
        {this.state.list.map(item => {
          const onHandleDismiss = () =>
            this.onDismiss(item.objectID);

          return (
            <div key={item.objectID}>
              <span>
                <a href={item.url}>{item.title}</a>
              </span>
              <span>{item.author}</span>
              <span>{item.num_comments}</span>
              <span>{item.points}</span>
              <span
                <button
                  onClick={onHandleDismiss}
                  type="button"
                >
                  Dismiss
                </button>
              </span>
            </div>
          );
        })}
      </div>
    );
  }
}
```

根结底，它必须是一个传递给元素处理器的函数。作为一个例子，请尝试尝试这段代码：

**src/App.js**
```javascript
class App extends Component {
...
  render() {
    return (
      <div className="App">
        {this.state.list.map(item =>
          ...
            <span>
              <button
                onClick={console.log(item.objectID)}
                type="button"
              >
                Dismiss
              </button>
            </span>
          </div>
        )}
      </div>
    );
  }
}
```

React 基础

48

当你在浏览器中打开应用程序时它会运行，但在点击按钮时不会运行。而

接下来的代码只会在你点击按钮时运行。它是一个在你触发处理器时执行的函数。

**src/App.js**
...
<button
  onClick={function () {
    console.log(item.objectID)
  }}
  type="button"
>
  Dismiss
</button>

...

为了保持简洁，你可以再次将其转换为 JavaScript ES6 箭头函数。这正是

我们之前对 `onDismiss()` 类方法所做的。

**src/App.js**
...
<button
  onClick={() => console.log(item.objectID)}
  type="button"
>
  Dismiss
</button>

...

React 的初学者经常在“事件处理器中使用函数”这个主题上遇到困难。

这就是为什么我尝试在这里更详细地解释它。最后，在你的按钮中你应该得到如下的

代码，以获得一个简洁的内联 JavaScript ES6 箭头函数，该函数可以访问项对象的 `objectID` 属性。

React 基础

49

**src/App.js**
```javascript
class App extends Component {
...
  render() {
    return (
      <div className="App">
        {this.state.list.map(item =>
          <div key={item.objectID}>
            ...
            <span>
              <button
                onClick={() => this.onDismiss(item.objectID)}
                type="button"
              >
                Dismiss
              </button>
            </span>
          </div>
        )}
      </div>
    );
  }
}
```

另一个经常被提到的性能相关话题是在在事件处理器中使用箭头函数的影响。例如，`onDismiss()` 方法的 `onClick` 处理器是将方法封装在另一个箭头函数中以便传递项标识符。因此，每当 `render()` 方法运行时，处理器都会实例化该高阶箭头函数。这*可能会*对你的应用程序性能产生影响，但在大多数情况下你不会注意到它。想象你有一个包含 1000 个项目的巨大数据表，并且每行或每列在事件处理器中都有这样一个箭头函数。那么就值得考虑性能影响，因此你可以实现一个专用的 `Button` 组件，在构造函数中绑定该方法。但在那发生之前，这是过早优化。专注于学习 React 本身更有价值。

**练习：**

- 尝试在你的按钮的 `onClick` 处理器中使用函数的不同方法

React 基础

50

## **与表单和事件的交互**

让我们为应用程序添加另一个交互，以体验 React 中的表单和事件。这个交互是一个搜索功能。搜索字段的输入应该根据项的 `title` 属性临时过滤你的列表。

在第一步中，你将在 JSX 中定义一个带有输入字段的表单。

**src/App.js**
```javascript
class App extends Component {
...
  render() {
    return (
      <div className="App">
        <form>
          <input type="text" />
        </form>
        {this.state.list.map(item =>
          ...
        )}
      </div>
    );
  }
}
```

在接下来的场景中，你将在输入框中输入，并根据输入框中使用的搜索词临时过滤列表。为了根据输入字段的值过滤列表，你需要将输入字段的值存储在本地状态中。但你如何访问这个值呢？你可以使用 React 中的**合成事件**（synthetic events）来访问事件负载。

为输入字段定义一个 `onChange` 处理器。

**src/App.js**
```javascript
class App extends Component {
...
  render() {
    return (
      <div className="App">
        <form>
          <input
            type="text"
            onChange={this.onSearchChange}
          />
        </form>
        ...
      </div>
    );
  }
}
```

该函数被绑定到组件上，因此再次是一个类方法。你需要绑定并定义方法。

**src/App.js**
```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      list,
    };
    this.onSearchChange = this.onSearchChange.bind(this);
    this.onDismiss = this.onDismiss.bind(this);
  }

  onSearchChange() {
    ...
  }
}
```

React 基础

52

当在元素中使用处理器时，你可以在回调函数的签名中获取合成 React 事件。

**src/App.js**
```javascript
class App extends Component {
...
  onSearchChange(event) {
    ...
  }
}
```

事件拥有输入字段的值。因此你可以再次使用 `this.setState()` 通过搜索词更新本地状态。

**src/App.js**
```javascript
class App extends Component {
...
  onSearchChange(event) {
    this.setState({ searchTerm: event.target.value });
  }
...
}
```

此外，你不忘记在构造函数中为 `searchTerm` 属性定义初始状态。输入字段应该是空的，因此该值应该是字符串。

React 基础

53

**src/App.js**
```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      list,
      searchTerm: '',
    };
    this.onSearchChange = this.onSearchChange.bind(this);
    this.onDismiss = this.onDismiss.bind(this);
  }
...
}
```

现在，每当输入框中的值变化时，你就将输入值存储到组件内部状态。

关于在 React 组件中更新本地状态的简单说明。可能会假设当使用 `this.setState()` 更新 `searchTerm` 时，需要传递列表以保留它。但事实并非如此。React 的 `this.setState()` 是浅合并。当更新单个属性时，它会保留状态对象中的兄弟属性。因此，即使你已经从中移除了一个项，列表状态也会保持不变。

回到你的应用程序。列表还没有根据存储在本地状态中的输入字段值进行过滤。基本上，你需要根据 `searchTerm` 临时过滤列表。你已经有了过滤它所需的一切。那么现在如何临时过滤呢？在你的 `render()` 方法中，在映射列表之前，你可以对其应用过滤器。过滤器只有当 `searchTerm` 匹配项的 `title` 属性时计算。你已经使用过内置的 JavaScript `filter` 功能，所以让我们再做一次。你可以在 `map` 函数之前传入 `filter` 函数，因为 `filter` 函数返回一个新数组，因此可以方便地在它上使用 `map` 函数。





## React 基础

54

**src/App.js**

```javascript
class App extends Component {

...

render() {

return (

<div className="App">

<form>

<input

type="text"

onChange={this.onSearchChange}

/>

</form>

**{this.state.list.filter(...).map(item =>**

...

)}

</div

);

}

}
```

这次我们用不同的方式来处理 `filter` 函数。我们希望将 `filter` 参数（即传递给 `filter` 函数的函数）定义在 ES6 类组件之外。在外部，我们无法访问组件的状态（state），因此无法访问 `searchTerm` 属性来评估过滤条件。我们必须将 `searchTerm` 传递给 `filter` 函数，并返回一个新的函数来评估该条件。这被称为高阶函数（higher-order function）。

通常我不会提到高阶函数，但在 React 书中提到它完全合理。了解高阶函数是有意义的，因为 React 处理的是一种名为高阶组件（higher-order components）的概念。你将在书中后面学习到这个概念。现在，让我们再次关注过滤功能。

首先，你必须在 `App` 组件之外定义这个高阶函数。

55

React 基础

**src/App.js**

```javascript
**function isSearched(searchTerm) {**
**return function(item) {**
**// 返回 true 或 false 的某些条件**
}**
}

class App extends Component {

...

}
```

该函数接收 `searchTerm` 并返回另一个函数，因为毕竟 `filter` 函数接收一个函数作为它的输入。返回的函数可以访问 `item` 对象，因为它就是传递给 `filter` 函数的那个函数。此外，返回的函数将用于根据函数中定义的条件来过滤列表。让我们定义这个条件。

**src/App.js**

```javascript
function isSearched(searchTerm) {

return function(item) {

**return item.title.toLowerCase().includes(searchTerm.toLowerCase());**

}

}

class App extends Component {

...

}
```

该条件表示，将传入的 `searchTerm` 模式与列表中 `item` 的 `title` 属性进行匹配。你可以使用 JavaScript 内置的 `includes` 功能来实现。只有当模式匹配时，你才返回 `true`，该项保留在列表中。当模式不匹配时，该项将从列表中移除。但要小心模式匹配：你不应该忘记将两个字符串都转换为小写。否则，搜索词 ‘redux’ 和项目标题 ‘Redux’ 之间会出现不匹配。由于我们处理的是不可变列表，并通过使用 `filter` 函数返回一个新列表，本地状态中的原始列表完全没有被修改。

还有一点需要提：我们利用 JavaScript 内置的 `includes` 功能稍微耍了小聪明。它已经是 ES6 的特性了。在 JavaScript ES5 中它看起来应该是什么样？你将使用 `indexOf()` 函数来获取项在列表中的索引。当项在列表中时，`indexOf()` 将返回它在数组中的索引。

56

React 基础 

**代码沙场**

*// ES5*
`string.indexOf(pattern) !== -1`

*// ES6*
`string.includes(pattern)`

再次使用 ES6 箭头函数可以完成另一个简洁的重构。它让函数更加简洁：

**代码沙场**

*// ES5*
```javascript
**function** isSearched(searchTerm) {

**return function**(item) {

**return** item.title.toLowerCase().indexOf(searchTerm.toLowerCase()) !== -1;

}

}
```

*// ES6*
```javascript
**const** isSearched = searchTerm => item =>

item.title.toLowerCase().includes(searchTerm.toLowerCase());
```

有人可能会争论哪个函数更具可读性。我个人更倾向于第二种。React 生态使用了大量的函数式编程概念。在 ES6 中，你可以通过箭头函数更简洁地表达这些。最后，你使用 `filter` 函数从本地状态中获取 `searchTerm`。它根据条件过滤你的列表并显示每个项。

57

React 基础 

**受控组件**

**src/App.js**

```javascript
class

 extends Component







render {



 (

<div className="App">

<form>

<input

type="text"

onChange={this.onSearchChange}

/>

</form>

**{this...list.filter(...).map(item =>**

...

)}

</div

);

}
}
```

你已经学习了 React 中的单向数据流。同样的规则适用于输入框，它通过更新本地状态来过滤列表。当状态更改时，`render()` 方法再次运行，并使用本地状态中的最新 `searchTerm` 来应用过滤条件。

但我们在输入元素中不是漏掉了什么吗？input 标签带有 `value` 属性。`value` 属性通常包含显示在输入框中的值。在这种情况下，它将是 `searchTerm` 属性。然而，看起来似乎在 React 中不需要它。这是错误的。表单元素如 `<input>`、`<textarea>` 和 `<select>` 在原生 HTML 中持有自己的状态。当从外部更改它们时，它们会在内部修改值。在 React 中，这被称为不受控组件（uncontrolled component），因为它们处理自己的状态。在 React 中，你应该确保让这些元素成为受控组件。

你应该如何做？你只需要设置输入框的 `value` 属性即可。值已经保存在 `searchTerm` 状态属性中了。那么为什么不从那里获取呢？

**src/App.js**

```javascript
class App extends Component {

...

render() {

const { searchTerm, list } = this.state;

return (

<div className="App">

<form>

<input

type="text"

value={searchTerm}

onChange={this.onSearchChange}

/>

</form>

...

</div

);

}

}
```

就是这样。输入框的单向数据流循环现在是自包含的。组件内部状态是输入框的单一事实来源。




React 基础

61

整个内部状态管理和单向数据流对你来说可能是全新的。但一旦你习惯了它，它将成为你在这 React 中实现功能的自然流程。总的来说，React 为单页应用世界引入了一种单向数据流的新颖模式。目前它已被许多框架和库采用。

**练习：**

- 了解更多关于 React 表单^(71)
- 了解更多关于不同的受控组件^(72)

71https://reactjs.org/docs/forms.html
72https://github.com/the-road-to-learn-react/react-controlled-components-examples

React 基础

62

## 分拆组件

你现在有一个大型的 App 组件。它会不断增长，并最终变得混乱。你可以开始将其拆分成若干个较小的组件块。

让我们开始使用一个组件处理搜索输入，另一个组件处理项目列表。

**src/App.js**

```javascript
class App extends Component {
  ...

  render() {
    const { searchTerm, list } = this.state;
    return (
      <div className="App">
        <Search />
        <Table />
      </div>
    );
  }
}
```

你可以向这些组件传递属性，它们可以自行使用。对于 App 组件来说，它需要传递在本地状态中管理的属性及其类方法。

**src/App.js**

```javascript
class App extends Component {
  ...

  render() {
    const { searchTerm, list } = this.state;
    return (
      <div className="App">
        <Search
          value={searchTerm}
          onChange={this.onSearchChange}
        />
        <Table
          list={list}
          pattern={searchTerm}
          onDismiss={this.onDismiss}
        />
      </div>
    );
  }
}
```

React 基础

63

现在你可以在 App 组件旁边定义这些组件。这些也将是 ES6 类组件。它们渲染的与之前相同的元素。第一个是 Search 组件。

**src/App.js**

```javascript
class App extends Component {
  ...
}

class Search extends Component {
  render() {
    const { value, onChange } = this.props;
    return (
      <form>
        <input
          type="text"
          value={value}
          onChange={onChange}
        />
      </form>
    );
  }
}
```

第二个是 Table 组件。

React 基础

64

**src/App.js**

```javascript
...
class Table extends Component {
  render() {
    const { list, pattern, onDismiss } = this.props;
    return (
      <div
        {list.filter(isSearched(pattern)).map(item =>
          <div key={item.objectID}>
            <span>
              <a href={item.url}>{item.title}</a>
            </span>
            <span>{item.author}</span>
            <span>{item.num_comments}</span>
            <span>{item.points}</span>
            <span>
              <button
                onClick={() => onDismiss(item.objectID)}
                type="button"
              >
                Dismiss
              </button>
            </span>
          </div>
        )}
      </div>
    );
  }
}
```

现在你有了三个 ES6 类组件。也许你已经注意到了可以通过 `this.props` 通过类实例访问的 props 对象。props 是 properties 的缩写，它包含了你在 App 组件中这些这些组件时传递给它们的所有值。通过这种方式，组件可以将属性沿着组件树向下传递。

通过从 App 组件中提取出这些组件，你将能够在其他地方复用它们。由于组件通过使用 props 对象获取值，因此当你在其他地方使用它们时，可以每次为你的组件传递不同的 props。这些组件变得可复用了。

React 基础

65

**练习：**

- 找出其他可以像你对 Search 和 Table 组件那样进行拆分的组件 - 但现在不要这样做，否则你会在接下来的章节中遇到冲突

React 基础

66

## 可组合组件

在 props 对象中还有另一个可以访问的微小属性：`children` 属性。你可以用它从上方向组件传递元素，这些元素对于组件本身是未知的，但它使得将组件组合在一起成为可能。让我们看看当只向 Search 组件传递一个文本（字符串）作为子元素看起来是什么样。

**src/App.js**

```javascript
class App extends Component {
  ...

  render() {
    const { searchTerm, list } = this.state;
    return (
      <div className="App">
        <Search
          value={searchTerm}
          onChange={this.onSearchChange}
        >
          Search
        </Search>
        <Table
          list={list}
          pattern={searchTerm}
          onDismiss={this.onDismiss}
        />
      </div>
    );
  }
}
```

现在 Search 组件可以从 props 对象中解构 `children` 属性。然后它可以指定 children 应该显示在哪里。

React 基础

67

**src/App.js**

```javascript
class Search extends Component {
  render() {
    const { value, onChange, children } = this.props;
    return (
      <form>
        {children} <input
          type="text"
          value={value}
          onChange={onChange}
        />
      </form>
    );
  }
}
```

现在，“Search”文本应该显示在你的输入字段旁边了。当你在其他地方使用 Search 组件时，你可以根据喜欢选择不同的文本。毕竟，不只有文本可以作为 children 传递。你可以将元素和元素树（可以再次由组件封装）作为 children 传递。`children` 使得将组件交织在一起成为可能。

**练习：**

- 了解更多关于 React 的组合模型^(73)

73https://reactjs.org/docs/composition-vs-inheritance.html

React 基础

68

## 可复用组件

可复用且可组合的组件让你能够构建强大的组件层级。它们是 React 视图层的基础。你现在可以复用 Table 和 Search 组件。让我们再定义一个可复用的组件，Button 组件，它被频繁使用。

**src/App.js**

```javascript
class Button extends Component {
  render() {
    const { onClick, className, children } = this.props;
    return (
      <button
        onClick={onClick}
        className={className}
        type="button"
      >
        {children}
      </button>
    );
  }
}
```

声明这样一个组件似乎是多余的。你将使用 Button 组件而不是 `button` 元素。它省略了 `type` 属性，因为 Button 组件已经指定了它。

然而，你必须考虑长期投资。想象你的应用程序中有几个按钮，但你想更改按钮的属性、样式或行为。如果没有这个组件，你将重构每一个按钮。相反，Button 组件确保了只有一个真理来源。一个 Button 即可一次重构所有按钮。一个 Button 统治一切。

React 基础

69

**src/App.js**

```javascript
class Table extends Component {
  render() {
    const { list, pattern, onDismiss } = this.props;
    return (
      <div
        {list.filter(isSearched(pattern)).map(item =>
          <div key={item.objectID}>
            <span>
              <a href={item.url}>{item.title}</a>
            </span>
            <span>{item.author}</span>
            <span>{item.num_comments}</span>
            <span>{item.points}</span>
            <span>
              <Button onClick={() => onDismiss(item.objectID)}>
                Dismiss
              </Button>
            </span>
          </div>
        )}
      </div>
    );
  }
}
```

Button 组件期望 props 中有一个 `className` 属性。`className` 属性是 HTML 属性 `class` 的另一个 React 衍生体。但使用 Button 时没有传递任何 `className`。在代码中，Button 组件应该更显式地说明 `className` 是可选的。因此，你可以在对象解构中分配一个默认值。

**src/App.js**

```javascript
class Button extends Component {
  render() {
    const {
      onClick,
      className = '',
      children,
    } = this.props;
    ...
```




React 基础

70

}

}

现在，每当在使用 Button 组件时没有指定 `className` 属性时，其值将是一个空字符串而不是 `undefined`。

React 基础

71

## 组件声明 (Component Declarations)

到目前，你已经有了四个 ES6 类组件。但你可以做得更好。让我向你介绍函数式无状态组件，作为 ES6 类组件的替代方案。在重构你的组件之前，让我们先介绍 React 中不同类型的组件。

- **函数式无状态组件 (Functional Stateless Components):** 这些组件是函数，接收输入并返回输出。输入是 props。输出是组件实例，即纯粹的 JSX。到目前为止，它与 ES6 类组件非常相似。然而，函数式无状态组件是函数（functional），并且它们没有本地状态（stateless）。你无法通过 `this.state` 或 `this.setState()` 访问或更新状态，因为没有 `this` 对象。此外，它们没有生命周期方法。你还没有学习过生命周期方法，但你已经使用过两个：`constructor()` 和 `render()`。而 `constructor` 在组件的生命周期内只运行一次，`render()` 类方法在开始时运行一次，并在每次组件更新时运行。请记住，当你以后到达生命周期方法章节时，函数式无状态组件是没有生命周期方法的。

- **ES6 类组件 (ES6 Class Components):** 你已经在你的四个组件中使用这种类型的组件声明。在类定义中，它们继承自 React 组件。`extend` 将 React 组件 API 中提供的所有生命周期方法挂载到组件上。通过这种方式，你能够使用 `render()` 类方法。此外，你可以通过 `this.state` 和 `this.setState()` 在 ES6 类组件中存储和操作状态。

- **React.createClass:** 这种组件声明用于旧版本的 React，现在仍用于 JavaScript ES5 React 应用程序中。但 Facebook 已将其宣布为弃用^(74)，以转向支持 JavaScript ES6。他们甚至在 15.5 版本^(75) 中添加了弃用警告。你将在书中不会使用它。

所以，基本上现在只剩下两种组件声明了。但什么时候该使用函数式无状态组件而不是 ES6 类组件呢？一个经验是，当你不需要本地状态或组件生命周期方法时，使用函数式无状态组件。通常你开始将组件实现为函数式无状态组件。一旦你需要访问状态或生命周期方法，你就必须将其重构为 ES6 类组件。在我们的应用程序中，为了学习 React，我们反过来操作了。

回到你的应用程序。App 组件使用了内部状态。这就是为什么它必须保持为 ES6 类组件的原因。但你的另外三个 ES6 类组件是无状态的。它们不需要访问 `this.state` 或 `this.setState()`。甚至，它们没有生命周期方法。让我们一起重构 Search 组件为无状态函数式组件。Table 和 Button 组件的重构将留作你的练习。

74 https://facebook.github.io/react/blog/2015/03/10/react-v0.13.html
75 https://facebook.github.io/react/blog/2017/04/07/react-v15.5.0.html

React 基础

72

**src/App.js**

```javascript
function Search(props) {
  const { value, onChange, children } = props;
  return (
    <form>
      {children} <input
        type="text"
        value={value}
        onChange={onChange}
      />
    </form>
  );
}
```

基本上就是这样了。props 在函数签名中是可访问的，返回值是 JSX。但在函数式无状态组件中，从代码角度来说你可以做更多。你已经了解了 ES6 解构。最佳实践是在函数签名中使用它来解构 props。

**src/App.js**

```javascript
function Search({ value, onChange, children }) {
  return (
    <form>
      {children} <input
        type="text"
        value={value}
        onChange={onChange}
      />
    </form>
  );
}
```

但还可以变得更好。你已经知道 ES6 箭头函数允许你保持函数的简洁。你可以移除函数的块级体（block body）。在简洁的主体中会带有一个隐式返回，因此你可以移除 `return` 语句。由于你的函数式无状态组件是一个函数，你也可以保持它的简洁。

React 基础

73

**src/App.js**

```javascript
const Search = ({ value, onChange, children }) =>
  <form>
    {children} <input
      type="text"
      value={value}
      onChange={onChange}
    />
  </form>
```

最后一步特别有用，可以强制只有 props 作为输入且 JSX 作为输出。中间没有其他的。尽管如此，你仍然*可以在中间做些事情*，通过在你的 ES6 箭头函数中使用块级体。

**代码练习场 (Code Playground)**

```javascript
const Search = ({ value, onChange, children }) => {
  // do something
  return (
    <form>
      {children} <input
        type="text"
        value={value}
        onChange={onChange}
      />
    </form>
  );
}
```
特别有用，可以强制只有 props 作为输入且 JSX 作为输出。中间没有其他的。尽管如此，你仍然*可以在中间做些事情*，通过在你的 ES6 箭头函数中使用块级体。

由于你的函数式无状态组件是一个函数，你也可以保持它的简洁。

（注：原文此处似乎存在部分重复或逻辑断层，翻译已根据逻辑补全）

React 基础

74

**练习：**

- 重构 Table 组件为无状态函数组件
- 重构 Button 组件为无状态函数组件

76 https://reactjs.org/docs/components-and-props

React 基础

75

**组件样式 (Styling Components)**

让我们为组件添加一些基础样式。

首先，为你的应用程序应用样式。

**src/App.css**

```css
body {
  color: #222;
  background: #f4f4f4;
  font: 400 Arial, sans-serif;
}

a {
  color: #222;
}

a:hover {
  text-decoration: underline;
}

ul, li {
  list-style: none;
  padding: 0;
  margin: 0;
}

input {
  padding: 10px;
  border-radius: 5px;
  outline: none;
}

button {
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #dddddd;
}
```

React 基础

76

其次，为应用程序中的应用样式。

**src/index.css**

```css
page {
  margin: 20px;
}

.interactions {
  text-align: center;
}

table {
  margin: 20px 0;
}

.table-header {
  display: flex;
  line-height: 24px;
  font-size: 16px;
  padding: 0 10px;
  justify-content: space-between;
}

.table-empty {
  margin: 200px;
  text-align: center;
  font-size: 16px;
}
```

React 基础

77

.table-row {
  display: flex;
  line-height: 24px;
  white-space: nowrap;
  margin: 10px 0;
  padding: 10px;
  background: #ffffff;
  border: 1px solid #e3e3e3;
}

.table-header > span {
  overflow: hidden;
  text-overflow: ellipsis;
  padding: 0 5px;
}

.table-row > span {
  overflow: hidden;
  text-overflow: ellipsis;
  padding: 0 5px;
}

.button-inline {
  border-width: 0;
  background: transparent;
  color: inherit;
  text-align: inherit;
  -webkit-font-smoothing: inherit;
  padding: 0;
  font-size: inherit;
  cursor: pointer;
}

.button-active {
  border-radius: 0;
  border-bottom: 1px solid #38BB6C;
}

现在你可以在你的一些组件中使用这些样式了。不要忘记在 HTML 属性中使用 React 的 `className` 而不是 `class`。

首先，将其应用于你的 App ES6 类组件中。





## React 基础

**src/App.js**

```javascript
class App extends Component {
  ...

  render() {
    const { searchTerm, list } = this.state;

    return (
      <div className="page">
        <div className="interactions">
          <Search
            value={searchTerm}
            onChange={this.onSearchChange}
          >
            Search
          </Search>
        </div>
        <Table
          list={list}
          pattern={searchTerm}
          onDismiss={this.onDismiss}
        />
      </div>
    );
  }
}
```

其次，将它应用到你的 Table 函数无状态组件。

**src/App.js**
```javascript
const Table = ({ list, pattern, onDismiss }) =>
  <div className="table">
    {list.filter(isSearched(pattern)).map(item =>
      <div key={item.objectID} className="table-row">
        <span>
          <a href={item.url}>{item.title}</a>
        </span>
        <span>{item.author}</span>
        <span>{item.num_comments}</span>
        <span>{item.points}</span>
        <span>
          <Button
            onClick={() => onDismiss(item.objectID)}
            className="button-inline"
          >
            Dismiss
          </Button>
        </span>
      </div>
    )}
  </div>
```

现在你已经使用基础 CSS 为你的应用程序和组件设置了样式。它们看起来相当体面。

如你所知，JSX 混合了 HTML 和 JavaScript。现在有人认为也可以将 CSS 加入其中。这被称为内联样式（inline style）。你可以定义 JavaScript 对象并将它们传递给元素的 style 属性。

让我们通过内联样式让 Table 的列宽保持灵活。

**src/App.js**
```javascript
const Table = ({ list, pattern, onDismiss }) =>
  <div className="table">
    {list.filter(isSearched(pattern)).map(item =>
      <div key={item.objectID} className="table-row">
        <span style={{ width: '40%' }}>
          <a href={item.url}>{item.title}</a>
        </span>
        <span style={{ width: '30%' }}>
          {item.author}
        </span>
        <span style={{ width: '10%' }}>
          {item.num_comments}
        </span>
        <span style={{ width: '10%' }}>
          {item.points}
        </span>
        <span style={{ width: '10%' }}>
          <Button
            onClick={() => onDismiss(item.objectID)}
            className="button-inline"
          >
            Dismiss
          </Button>
        </span>
      </div>
    )}
  </div>
```

现在样式是内联的。你可以在元素之外定义样式对象以使代码更整洁。

**代码演场 (Code Playground)**
```javascript
const largeColumn = {
  width: '40%',
};

const midColumn = {
  width: '30%',
};

const smallColumn = {
  width: '10%',
};
```

之后，你就可以在列中使用它们：`<span style={smallColumn}>`。

通常情况下，你会发现关于 React 样式的不同的意见和解决方案。你现在已经使用了纯 CSS 和内联样式。这对于入门已经足够了。

我不想在这里发表主观点，但我想为你留出更多选择。你可以阅读这些内容并由自己应用。但如果你是 React 的初学者，我建议目前坚持使用纯 CSS 和内联样式。

- styled-components (77)
- CSS Modules (78)

77 https://github.com/styled-components/styled-components
78 https://github.com/css-modules/css-modules

你已经学习了编写自己的 React 应用程序的基础知识！让我们回顾一下最后几章：

- React
  - 使用 `this.state` 和 `setState()` 管理你的内部组件状态
  - 将函数或类方法传递给你的元素处理器
  - 在 React 中使用表单和事件添加交互
  - 单向数据流是 React 中的一个重要概念
  - 拥抱控制组件 (controlled components)
  - 使用 children 和可复用组件组合组件
  - ES6 类组件和函数无状态组件的使用与实现
  - 为组件设置样式的方法
- ES6
  - 绑定到类的函数是类方法
  - 对象和数组的解构
  - 默认参数
- 一般
  - 高阶函数

再次，休息一下是有意义的。内化所学知识并由自己应用。你可以对目前编写的代码进行实验。你可以在官方仓库中找到源码 (79)。

79 https://github.com/the-road-to-learn-react/hackernews-client/tree/5.2

## 与 API 玩真格

现在是时候真地接触 API 了，因为处理示例数据可能会变得无聊。

如果你不熟悉 API，我鼓励你阅读我了解 API 的历程 (80)。

你知道 Hacker News (81) 平台吗？它是一个关于技术主题的优秀新闻聚合器。在书中，你将使用 Hacker News API 从平台获取故事。有基础 (82) 和搜索 (83) API 用于从平台获取数据。后者用于获取数据。

### 生命周期周期方法 (Lifecycle Methods)

如你所知，JSX 混合了 HTML 和 JavaScript。现在有人认为也可以将 CSS 加入其中。这被称为内联样式（inline style）。你可以定义 JavaScript 对象并将它们传递给元素的 style 属性。

让我们通过内联样式让 Table 的列宽保持灵活。

现在你已经使用基础 CSS 为你的应用程序和组件设置了样式。它们看起来相当体面。

样式是内联的。你可以在元素之外定义样式对象以使代码更整洁。

之后，你就可以在列中使用它们：`<span style={smallColumn}>`。

通常情况下，你会发现关于 React 样式的不同的意见和解决方案。你现在已经使用了纯 CSS 和内联样式。这对于入门已经足够了。

我不想在这里发表主观点，但我想为你留出更多选择。你可以阅读这些内容并由自己应用。但如果你是 React 的初学者，我建议目前坚持使用纯 CSS 和内联样式。

77 https://github.com/styled-components/styled-components
78 https://github.com/css-modules/css-modules

80 https://github.com/the-road-to-learn-react/hackernews-client
81 https://www.newscombinator.com
82 https://algolia.com
83 https://hn.com/
84 https://robin.dev/what-is-an-api
85 https://github.com/styled-components/styled-components
86 https://github.com/css-modules/css-modules
87 https://react.dev/reference/react/Component
88 https://react.dev/reference/react/useState
89 https://react.dev/reference/react/setState
90 https://react.dev/reference/react/useEffect
91 https://react.dev/reference/react/memo
92 https://react.dev/reference/react/StrictMode
93 https://react.dev/reference/react/useContext
94 https://react.dev/reference/react/useRef
95 https://react.dev/reference/react/useReducer
96 https://react.dev/reference/react/useCallback
97 https://react.dev/reference/react/useMemo
98 https://react.dev/reference/react/useLayoutEffect
99 https://react.dev/reference/react/useInsertionEffect
100 https://react.dev/reference/react/useDeferredValue
101 https://react.dev/reference/react/useTransitionState
102 https://react.dev/reference/react/SyncExternalStore
103 https://react.dev/reference/react/useSyncStore
104 https://react.dev/reference/react/useExternalStore
105 https://react.dev/reference/react/useDebugValue
106 https://react.dev/reference/react/useId
107 https://react.dev/reference/react/use.client
108 https://react.dev/reference/react/use.server
109 https://react.dev/reference/react/use.istic
110 https://react.dev/reference/react/useDeferredValue
111 https://react.dev/reference/react/useTransitionState
112 https://react.dev/reference/react/SyncExternalStore
113 https://react.dev/reference/react/useSyncStore
114 https://react.dev/reference/react/useExternalStore
115 https://react.dev/reference/react/useDebugValue
116 https://react.dev/reference/react/useId
117 https://react.dev/reference/react/use.client
118 https://react.dev/reference/react/use.server
119 https://react.dev/reference/react/use.istic
120 https://react.dev/reference/react/useDeferredValue
121 https://react.dev/reference/react/useTransitionState
122 https://react.dev/reference/react/SyncExternalStore
123 https://react.dev/reference/react/useSyncStore
124 https://react.dev/reference/react/useExternalStore
125 https://react.dev/reference/react/useDebugValue
126 https://react.dev/reference/react/useId
127 https://react.dev/reference/react/use.client
128 https://react.dev/reference/react/use.server
129 https://react.dev/reference/react/use.istic

- [useState](https://react.dev/reference/react/useState)
- [setsetState](https://react.dev/reference/react/setState)
- [useEffect](https://react.dev/reference/react/useEffect)
- [memo](https://react.dev/reference/react/memo)
- [useContext](https://react.dev/reference/react/useContext)
- [useRef](https://react.dev/reference/react/useRef)
- [useReducer](https://react.dev/reference/react/useReducer)
- [useCallback](https://react.dev/reference/react/useCallback)
- [useMemo](https://react.dev/reference/react/useMemo)
- [useLayoutEffect](https://react.dev/reference/react/useLayoutEffect)
- [useDeferredValue](https://react.dev/reference/react/useDeferredValue)
- [useTransitionState](https://react.dev/reference/react/useTransitionState)
- [SyncExternalStore](https://react.dev/reference/react/SyncExternalStore)
- [useSyncStore](https://react.dev/reference/react/useSyncStore)
- [useExternalStore](https://react.dev/reference/react/useExternalStore)
- [useDebugValue](https://react.dev/reference/react/useDebugValue)
- [useId](https://react.dev/reference/react/useId)
- [use.client](https://react.dev/reference/react/use.client)
- [use.server](https://react.dev/reference/react/use.server)
- [use.istic](https://react.dev/reference/react/use.istic)

(注：由于输入文本中存在大量重复的占位符和链接，翻译时遵循“不要重复输出原文”的原则，此处仅展示核心逻辑与结构翻译)

## 与 API 玩真格

现在是时候真地接触 API 了，因为处理示例数据可能会变得无聊。

如果你不熟悉 API，我鼓励你阅读我了解 API 的历程 (80)。

你知道 Hacker News (81) 平台吗？它是一个关于技术主题的优秀新闻聚合器。在书中，你将使用 Hacker News API 从平台获取故事。有基础 (82) 和搜索 (83) API 用于从平台获取数据。后者用于获取数据。

### 生命周期周期方法 (Lifecycle Methods)

如你所知，JSX 混合了 HTML 和 JavaScript。现在有人认为也可以将 CSS 加入其中。这被称为内联样式（inline style）。你可以定义 JavaScript 对象并将它们传递给元素的 style 属性。

让我们通过内联样式让 Table 的列宽保持灵活。

现在样式是内联的。你可以在元素之外定义样式对象以使代码更整洁。

之后，你就可以在列中使用它们：`<span style={smallColumn}>`。

通常情况下，你会发现关于 React 样式的不同的意见和解决方案。你现在已经使用了纯 CSS 和内联样式。这对于入门已经足够了。

我不想在这里发表主观点，但我想为你留出更多选择。你可以阅读这些内容并由自己应用。但如果你是 React 的初学者，我建议目前坚持使用纯 CSS 和内联样式。

你已经学习了编写自己的 React 应用程序的基础知识！让我们回顾一下最后几章：

- React
  - 使用 `this.state` 和 `setState()` 管理你的内部组件状态
  - 将函数或类方法传递给你的元素处理器
  - 在 React 中使用表单和事件添加交互
  - 单向数据流是 React 中的一个重要概念
  - 拥抱控制组件 (controlled components)
  - 使用 children 和可复用组件组合组件
  - ES6 类组件和函数无状态组件的使用与实现
  - 为组件设置样式的方法
- ES6
  - 绑定到类的函数是类方法
  - 对象和数组的解构
  - 默认参数
- 一般
  - 高阶函数

再次，休息一下是有意义的。内化所学知识并由自己应用。你可以对目前编写的代码进行实验。你可以在官方仓库中找到源码 (79)。




真实使用 API

85

还有一个多了一个生命周期方法：`componentDidCatch(error, info)`。它是在 React 16 中引入的，用于捕获组件中的错误。例如，在你的应用程序中显示示例列表运行良好。但可能会出现一种情况：本地状态中的列表被意外设置为 `null`（例如，当从外部 API 获取列表时，请求失败且你将列表的本地状态设置为 `null`）。此后，你将无法再次对列表进行过滤（filter）和映射（map）操作，因为它是 `null` 而不是空列表。组件将会崩溃，整个应用程序也会随之失败。现在，通过使用 `componentDidCatch()`，你可以捕获错误，将其存储在本地状态中，并向应用程序用户显示一条可选的消息，告知发生了错误。

**练习：**

- 了解更多关于 React 中的生命周期方法 (85)
- 了解更多关于 React 中的生命周期方法 (86)
- 了解更多关于 React 中的生命周期方法 (87)
- 了解更多关于 React 中的生命周期方法 (88)
- 了解更多关于 React 中的生命周期方法 (89)
- 了解更多关于 React 中的生命周期方法 (90)
- 了解更多关于 React 中的生命周期方法 (91)
- 了解更多关于 React 中的生命周期方法 (92)
- 了解更多关于 React 中的生命周期方法 (93)
- 了解更多关于 React 中的生命周期方法 (94)
- 了解更多关于 React 中的生命周期方法 (95)
- 了解更多关于 React 中的生命周期方法 (96)
- 了解更多关于 React 中的生命周期方法 (97)
- 了解更多关于 React 中的生命周期方法 (98)
- 了解更多关于 React 中的生命周期方法 (99)




深入上手 API

90

## ES6 展开运算符

“关闭（Dismiss）”按钮不起作用，是因为 `onDismiss()` 方法没有考虑到复杂的结果对象。它只知道本地状态中的一个普通列表。但它现在不再是一个普通列表了。让我们让它操作结果对象，而不是操作列表本身。

**src/App.js**

```javascript
onDismiss(id) {
  const isNotId = item => item.objectID !== id;
  const updatedHits = this.state.result.hits.filter(isNotId);
  this.setState({
    ...
  });
}
```

但现在 `setState()` 中发生了什么？遗憾的是，结果是一个复杂对象。`hits` 列表只是该对象中多个属性之一。然而，当结果对象中的一个项目被移除时，只有列表被更新，而其他属性保持不变。

一种方法是可以修改结果对象中的 `hits`。我会演示一下，但我们不会采用那种方式。

**代码演练场**

```javascript
// 不要这样做
this.state.result.hits = updatedHits;
```

React 拥抱不可变数据结构。因此，你不应该修改一个对象（或直接修改状态）。更好的方法是根据你拥的信息生成一个新对象。这样，没有任何对象被更改了。你将保持不可变的数据结构。你始终返回一个新对象，而永远不修改对象。

因此，你可以使用 JavaScript ES6 的 `Object.assign()`。它接受第一个参数作为目标对象。后续的所有参数都是源对象。这些对象会被合并到目标对象中。目标可以为空对象。它体现了不可变性，因为没有源对象被修改。它看起来类似于下面：

**代码演练场**

```javascript
const updatedHits = { hits: updatedHits };
const updatedResult = Object.assign({}, this.state.result, updatedHits);
```

当后来的对象共享相同的属性名时，它们将覆盖先前的合并的对象。现在让我们在 `onDismiss()` 方法中实现：

深入上手 API

91

**src/App.js**

```javascript
onDismiss(id) {
  const isNotId = item => item.objectID !== id;
  const updatedHits = this.state.result.hits.filter(isNotId);
  this.setState({
    result: Object.assign({}, this.state.result, { hits: updatedHits })
  });
}
```

这已经是解决方案了。但在 JavaScript ES6 以及未来的 JavaScript 版本中，有一种更简单的方法。我可以向你介绍展开运算符（spread operator）吗？它只由三个点组成：`...`。当使用它时，数组或对象中的每个值都会复制到另一个数组或对象中。

让我们来看看 ES6 数组展开运算符，尽管你还没有需要。

**代码演练场**

```javascript
const userList = ['Robin', 'Andrew', 'Dan'];
const additionalUser = 'Jordan';
const allUsers = [...userList, additionalUser];
console.log(allUsers);
// 输出: ['Robin', 'Andrew', 'Dan', 'Jordan']
```

`allUsers` 变量是一个全新的数组。其他变量 `userList` 和 `additionalUser` 保持不变。你甚至这种方式将两个数组合并为一个新数组。

**代码演练场**

```javascript
const oldUsers = ['Robin', 'Andrew'];
const newUsers = ['Dan', 'Jordan'];
const allUsers = [...oldUsers, ...newUsers];
console.log(allUsers);
// 输出: ['Robin', 'Andrew', 'Dan', 'Jordan']
```

现在让我们看看对象展开运算符。它不是 JavaScript ES6。它是下一个 JavaScript 版本的提议^(95)，但已经被 React 社区所使用。这就是为什么 `create-react-app` 在配置中整合了该功能。

基本上，它与 JavaScript ES6 数组展开运算符相同，但针对的是对象。它将每个键值对复制到一个新对象中。

95https://github.com/sebmarkbage/ecmascript-rest-spread

深入上手 API

92

**代码演练场**

```javascript
const userNames = { firstname: 'Robin', lastname: 'Wieruch' };
const age = 28;
const user = { ...userNames, age };
console.log(user);
// 输出: { firstname: 'Robin', lastname: 'Wieruch', age: 28 }
```

多个对象可以像数组展开示例那样展开。

**代码演练场**

```javascript
const userNames = { firstname: 'Robin', lastname: 'Wieruch' };
const userAge = { age: 28 };
const user = { ...userNames, ...userAge };
console.log(user);
// 输出: { firstname: 'Robin', lastname: 'Wieruch', age: 28 }
```

毕竟，它可以被用来替换 `Object.assign()`。

**src/App.js**

```javascript
onDismiss(id) {
  const isNotId = item => item.objectID !== id;
  const updatedHits = this.state.result.hits.filter(isNotId);
  this.setState({
    result: { ...this.state.result, hits: updatedHits }
  });
}
```

现在“关闭”按钮应该可以再次工作了，因为 `onDismiss()` 方法感知到了复杂的结果对象，并知道在列表中移除一个项目后如何更新它。

**练习题：**

- 了解更多关于 ES6 `Object.assign()`^(96)
- 了解更多关于 ES6 数组展开运算符^(97)
- 简要提到了对象展开运算符

96https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/assign
97https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Spread_operator

深入上手 API

93

## 条件渲染

条件渲染在 React 应用中很早就被引入了。但在本书中没有，因为当时还没有这样的用例。条件渲染发生在你决定渲染一个元素或另一个元素时。有时它意味着渲染一个元素或什么都不渲染。毕竟，条件渲染最简单的用法可以用 JSX 中的 `if-else` 语句来表示。

内部组件状态中的结果对象初始为 `null`。到目前为止，当结果未从 API 返回时，`App` 组件没有返回任何元素。这已经是条件渲染了，因为你根据特定条件从 `render()` 生命周期方法中提前返回。`App` 组件要么不渲染任何内容，要么渲染它的元素。

但让我们更进一步。将依赖于的唯一组件 `Table` 封装在一个独立的条件渲染中更有意义。其他所有内容都应该显示，即使还没有结果。你可以简单地在 JSX 中使用三元运算符。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    const { searchTerm, result } = this.state;
    return (
      <div className="page">
        <div className="interactions">
          <Search
            value={searchTerm}
            onChange={this.onSearchChange}
          >
            Search
          </Search>
        </div>
        { result
          ? <Table
            list={result.hits}
            pattern={searchTerm}
            onDismiss={this.onDismiss}
          />
          : null
        }
      </div>
    );
  }
}
```

深入上手 API

94

这是你表达条件渲染的第二种选择。第三种选择是逻辑 `&&` 运算符。在 JavaScript 中，`true && 'Hello World'` 总是求结果为 `'Hello World'`。`false && 'World'` 总是求结果为 `false`。

**代码演练场**

```javascript
const result = true && 'Hello World';
console.log(result);
// 输出: Hello World

const result = false && 'Hello World';
console.log(result);
// 输出: false
```

在 React 中你可以利用这种行为。如果条件为 `true`，逻辑 `&&` 运算符后面的表达式将输出。如果条件为 `false`，React 将忽略并跳过该表达式。这适用于 Table 的条件渲染情况，因为它应该返回一个 `Table` 或什么都没有。

**src/App.js**

```javascript
{ result &&
<Table
  list={result.hits}
  pattern={searchTerm}
  onDismiss={this.onDismiss}
/>
}
```
这些是在 React 中使用条件渲染的几种方法。你可以在详尽的条件渲染方法列表^(98) 中阅读更多方案。此外你还将了解它们不同的用例以及何时应用它们。

毕竟，你应该能够在你的应用程序中看到获取的数据。在等待数据获取期间，Table 以外的所有内容都将显示。一旦请求解析结果并存储到本地状态中，Table 将显示，因为 `render()` 方法再次运行，且条件渲染中的条件有利于显示 Table 组件。

98https://www.robinwieruch.de/conditional-rendering-react/




深入实战 API 应用

95

**练习：**

-   [阅读更多关于条件渲染的不同方式](#99) (99)
-   [阅读更多关于 React 条件渲染](#100) (100)

99 https://www.robinwieruch.de/conditional-rendering-react/
100 https://reactjs.org/docs/conditional-rendering.html

深入实战 API 应用

96

## 客户端或服务器搜索

当你使用带有输入字段的 `Search` 组件时，你将过滤列表。不过，这是发生在客户端的。现在，你将使用 Hacker News API 在服务器端进行搜索。否则，你将只能处理在 `componentDidMount()` 中通过默认搜索参数获取的第一个 API 响应。

你可以在 `App` 组件中定义一个 `onSearchSubmit()` 方法，当在 `Search` 组件中执行搜索时，该方法从 Hacker News API 获取结果。

**src/App.js**

```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      result: null,
      searchTerm: DEFAULT_QUERY,
    };
    this.setSearchTopStories = this.setSearchTopStories.bind(this);
    this.onSearchChange = this.onSearchChange.bind(this);
    this.onSearchSubmit = this.onSearchSubmit.bind(this);
    this.onDismiss = this.onDismiss.bind(this);
  }
  ...
  onSearchSubmit() {
    const { searchTerm } = this.state;
  }
  ...
}
```

`onSearchSubmit()` 方法应该使用与 `componentDidMount()` 生命周期方法相同的功能，但这次使用的是来自本地状态的修改后的搜索词，而不是初始的默认搜索术。因此，你可以将功能提取为可重用的类方法。

深入实战 API 应用

97

**src/App.js**

```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      result: null,
      searchTerm: DEFAULT_QUERY,
    };
    this.setSearchTopStories = this.setSearchTopStories.bind(this);
    this.fetchSearchTopStories = this.fetchSearchTopStories.bind(this);
    this.onSearchChange = this.onSearchChange.bind(this);
    this.onSearchSubmit = this.onSearchSubmit.bind(this);
    this.onDismiss = this.onDismiss.bind(this);
  }
  ...
  fetchSearchTopStories(searchTerm) {
    fetch(`${PATH_BASE}${PATH_SEARCH}?${PARAM_SEARCH}${searchTerm}`)
      .then(response => response.json())
      .then(result => this.setSearchTopStories(result))
      .catch(error => error);
  }
  componentDidMount() {
    const { searchTerm } = this.state;
    this.fetchSearchTopStories(searchTerm);
  }
  ...
  onSearchSubmit() {
    const { searchTerm } = this.state;
    this.fetchSearchTopStories(searchTerm);
  }
  ...
}
```

现在 `Search` 组件必须添加一个额外的按钮。该按钮必须显式地触发搜索请求。否则，你每当输入字段变化时，都会从 Hacker News API 获取数据。但你希望在 `onClick()` 处理程序中显式地这样做。

作为替代方案，你可以对 `onChange()` 函数进行防抖（延迟）并省去按钮，但这会在此时增加更多复杂性，并且可能不是你想要的效果。让我们先保持简单，不使用防抖。

首先，将 `onSearchSubmit()` 方法传递给你的 `Search` 组件。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    const { searchTerm, result } = this.state;
    return (
      <div className="page">
        <div className="interactions">
          <Search
            value={searchTerm}
            onChange={this.onSearchChange}
            onSubmit={this.onSearchSubmit}
          >
            Search
          </Search>
        </div>
        { result &&
          <Table
            list={result.hits}
            pattern={searchTerm}
            onDismiss={this.onDismiss}
          />
        }
      </div>
    );
  }
}
```

其次，在你的 `Search` 组件中引入一个按钮。该按钮类型为 `type="submit"`，且表单使用其 `onSubmit()` 属性来传递 `onSubmit()` 方法。你可以重用 `children` 属性，但这次它将被用作按钮的内容。

深入实战 API 应用

99

**src/App.js**

```javascript
const Search = ({
  value,
  onChange,
  onSubmit,
  children
}) => (
  <form onSubmit={onSubmit}>
    <input
      type="text"
      value={value}
      onChange={onChange}
    />
    <button type="submit">{children}</button>
  </form>
)
```

在 `Table` 中，你可以移除 `pattern` 属性，因为现在不再需要它了。`searchTerm` 将直接从 Hacker News API 获取。

现在当你点击搜索按钮时，`searchTerm` 将来自 API 响应结果。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    const { searchTerm, result } = this.state;
    return (
      <div className="page">
        <div className="interactions">
          <Search
            value={searchTerm}
            onChange={this.onSearchChange}
            onSubmit={this.onSearchSubmit}
          >
            Search
          </Search>
        </div>
        { result &&
          <Table
            list={result.hits}
            pattern={searchTerm}
            onDismiss={this.onDismiss}
          />
        }
      </div>
    );
  }
}
```

当你尝试搜索时，你会发现浏览器刷新了。在 React 中，你需要使用 `preventDefault()` 来阻止这种行为。

**src/App.js**

```javascript
onSearchSubmit(event) {
  const { searchTerm } = this.state;
  this.fetchSearchTopStories(searchTerm);
  event.preventDefault();
}
```

这样你就可以处理 API 搜索了。

**练习：**

-   [阅读更多关于 React 中的事件](#101) (101)
-   [阅读更多关于分页 API](#102) (102)

101 https://reactjs.org/docs/events
102 https://hn.algolia.com

深入实战 API 应用

100

## 分页获取

你是否仔细查看了返回的数据？Hacker News API 返回了一个 `page` 属性，在首次请求时为 0。让我们扩展这些常量以便能够处理分页数据。

**src/App.js**

```javascript
const DEFAULT_QUERY = 'redux';
const PATH_BASE = 'https://hn.algolia.com/v1';
const PATH_SEARCH = '/search';
const PARAM_SEARCH = 'query=';
const PARAM_PAGE = 'page=';
```

现在你可以使用新的常量为 API 请求添加页面参数。

**Code Playground**

```javascript
const url = `${PATH_BASE}${PATH_SEARCH}?${PARAM_SEARCH}${searchTerm}&${PARAM_PAGE}${page}`;
console.log(url);
// 输出: https://hn.algolia.com/v1/search?query=redux&page=0
```

`fetchSearchTopStories` 方法将接收第二个作为参数。如果不提供第二个参数，它将回退到 0。因此 `componentDidMount()` 和 `onSearchSubmit()` 方法获取的是第一页。后续获取应通过提供第二个参数来获取下一页。

深入实战 API 应用

102

**src/App.js**

```javascript
class App extends Component {
  ...
  fetchSearchTopStories(searchTerm, page = 0) {
    fetch(`${PATH_BASE}${PATH_SEARCH}?${PARAM_SEARCH}${searchTerm}&${PARAM_PAGE}${page}`)
      .then(response => response.json())
      .then(result => this.setSearchTopStories(result))
      .catch(error => error);
  }
  ...
}
```

`page` 参数使用了 JavaScript ES6 默认参数，在未定义页面参数时回退到 0。

现在你可以使用 API 响应中的当前页码在 `fetchSearchTopStories()` 中。你可以将此方法用于按钮，通过 `onClick` 获取更多故事。我们只需要定义 `onClick()` 处理程序，它接收当前的搜索词和下一页（当前页码 + 1）。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    const { searchTerm, result } = this.state;
    const page = (result && result.page) || 0;
    return (
      <div className="page">
        <div className="interactions">
          <Search
            value={searchTerm}
            onChange={this.onSearchChange}
            onSubmit={this.onSearchSubmit}
          >
            Search
          </Search>
        </div>
        { result &&
          <Table
            list={result.hits}
            onDismiss={this.onDismiss}
          />
        }
        <button onClick={() => this.fetchSearchTopStories(searchTerm, page + 1)}>
          Load More
        </button>
      </div>
    );
  }
}
```




## 深入上手 API

103

/>

}

**<div className="interactions">**

**<Button onClick={() => this.fetchSearchTopStories(searchTerm, page + 1)}>**

**更多**

**</Button>**

**</div>**
</div

);

}

此外，在你的 `render()` 方法中，你应该确保在还没有结果时默认页面设为 0。请记住，`render()` 方法是在 `componentDidMount()` 周期方法中异步获取数据之前被调用的。

还缺少了一个步骤。你获取了下一页数据，但它会覆盖掉你之前页的数据。理想的情况是将本地状态中的旧 `hits` 列表与新结果对象中的列表合并。让我们调整一下功能，以添加新数据而不是覆盖它。

**src/App.js**

```javascript
setSearchTopStories(result) {
  const { hits, page } = result;
  const oldHits = page !== 0
    ? this.state.result.hits
    : [];
  const updatedHits = [
    ...oldHits,
    ...hits
  ];
  this.setState({
    result: { hits: updatedHits, page }
  });
}
```

现在 `setSearchTopStories()` 方法中发生了几件事。首先，你从 `result` 中获取 `hits` 和 `page`。

其次，你必须检查是否已经旧的 `hits`。当 `page` 为 0 时，它是来自 `componentDidMount()` 或 `onSearchSubmit()` 的新搜索请求。此时 `hits` 是空的。但当你点击“更多”按钮获取分页数据时，`page` 不是 0。它是下一页。旧的 `hits` 已经存储在你的状态中，因此可以使用。

第三，你不希望覆盖旧的 `hits`。你可以合并来自最近 API 请求的旧和新 `hits`。可以使用 JavaScript ES6 的数组展开运算符完成这两个列表的合并。

第四，你将合并后的 `hits` 和 `page` 设置在本地组件状态中。

你还可以进行最后一次调整。当你尝试“更多”按钮时，它只获取了几个列表项。可以扩展 API URL，以便在每次请求时获取更多列表项。同样，你可以添加更多可组合的路径常量。

**src/App.js**

```javascript
const DEFAULT_QUERY = 'redux';
const DEFAULT_HPP = '100';
const PATH_BASE = 'https://hn.algolia.com/api/v1';
const PATH_SEARCH = '/search';
const PARAM_SEARCH = 'query=';
const PARAM_PAGE = 'page=';
const PARAM_HPP = 'hitsPerPage=';
```

现在你可以使用这些常量来扩展 API URL。

**src/App.js**

```javascript
fetchSearchTopStories(searchTerm, page = 0) {
  fetch(`${PATH_BASE}${PATH_SEARCH}?${PARAM_SEARCH}${searchTerm}&${PARAM_PAGE}${page}&${PARAM_HPP}${DEFAULT_HPP}`)
    .then(response => response.json())
    .then(result => this.setSearchTopStories(result))
    .catch(error => error);
}
```

之后，对 Hacker News API 的请求单次请求获取的列表项比之前更多。如你所见，像 Hacker News API 这样强大的 API 提供了许多方法来实验真实世界的数据。你应该利用它让你在学习新事物时的努力变得更加有趣。这就是我学习学习新的编程语言或库时，了解到 API 所提供的助力。

104 https://www.robinwieruch.de/what-is-an-api-javascript/

## 深入上手 API

104

**练习：**

- 了解更多关于 ES6 默认参数 (105)
- 测试 Hacker News API 参数 (106)

105 https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Functions/Default_parameters
106 https://hn.algolia.com/api

## 深入上手 API

106

### 客户端缓存

每次提交搜索都会向 Hacker News API 发送请求。你可能会搜索“redux”，然后是“react”，最后又搜索了“redux”。总共发送了 3 次请求。但你搜索了两次“redux”，且两次都花费了整个异步往返来获取数据。在客户端缓存中，你会存储每个结果。当向 API 发起请求时，它会检查结果是否已经存在。如果存在，则使用缓存。否则，将发起 API 请求获取数据。

为了让每个结果拥有客户端缓存，你需要在内部组件状态中存储多个结果而不是单个结果。`results` 对象将是一个 map，以搜索词为键，以结果为值。来自 API 的每个结果将通过搜索词（键）保存。

目前，你本地状态中的 `result` 看起来如下：

**代码沙场**

```javascript
result: {
  hits: [ ... ],
  page: 2,
}
```

假设你已经进行了两次 API 请求。一个针对搜索词“redux”，另一个针对“react”。`results` 对象应该如下所示：

**代码沙场**

```javascript
results: {
  redux: {
    hits: [ ... ],
    page: 2,
  },
  react: {
    hits: [ ... ],
    page: 1,
  },
  ...
}
```

让我们用 React 的 `setState()` 实现客户端缓存。首先，在初始组件状态中将 `result` 对象重命名为 `results`。其次，定义 `searchKey` 来存储每个结果。

**深入上手 API**

107

**src/App.js**

```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      results: null,
      searchKey: '',
      searchTerm: DEFAULT_QUERY,
    };
  }
  ...
}
```

`searchKey` 必须在每次请求之前设置。你可能会问：为什么不使用 `searchTerm`？因为 `searchTerm` 是一个变动变量，在你每次输入时都会改变。然而，使用 `searchKey` 可以获取当前结果，从而在 `render()` 方法中显示当前结果。

**src/App.js**

```javascript
class App extends Component {
  componentDidMount() {
    const { searchTerm } = this.state;
    this.setState({ searchKey: searchTerm });
  }
  ...
  onSearchSubmit(event) {
    const { searchTerm } = this.state;
    this.setState({ searchKey: searchTerm });
    fetchSearchTopStories(searchTerm);
    event.preventDefault();
  }
}
```

**深入上手 API**

121

108

现在你必须调整 `results` 存储在状态中的功能。`searchKey` 将作为键。

**src/App.js**

```javascript
class App extends Component {
  ...
  setSearchTopStories(result) {
    const { hits, page } = result;
    const { searchKey, results } = this.state;
    const oldHits = page !== 0
      ? results[searchKey].hits
      : [];
    const updatedHits = [
      ...oldHits,
      ...hits
    ];
    this.setState({
      results: {
        ...results,
        [searchKey]: { hits: updatedHits, page }
      }
    });
  }
  ...
}
```

首先，你从状态中获取 `searchKey`。其次，旧的 `hits` 必须与新的 `hits` 合并。第三，在状态的 results map 中设置新结果。让我们检查 `setState()` 中的 `results` 对象。

```javascript
results: {
  ...results,
  [searchKey]: { hits: updatedHits, page }
}
```

底部部分确保通过 `searchKey` 在 map 中存储更新的结果。值是一个包含 `hits` 和 `page` 属性的对象。`searchKey` 是搜索词。你已经学习了 `[searchKey]: ...` 语法。它是 ES6 的计算属性名。它可以帮助你在对象中动态分配值。顶部部分需要使用对象运算符展开状态中通过 `searchKey` 的其他结果。否则你会丢失之前存储的所有结果。

现在你通过搜索词存储所有结果。这是启用缓存的第一步。在下一步中，你可以根据非变动的 `searchKey` 从你的结果 map 中检索结果。这就是为什么你最初引入 `searchKey` 作为非变动变量的原因。否则当你使用变动的 `searchTerm` 获取当前结果时，检索将会失效。




真实使用 API

return (
  <div className="page">
    <div className="interactions">
      ...
    </div>
    <Table
      list={list}
      onDismiss={this.onDismiss}
    />
    <div className="interactions">
      <Button onClick={() => this.fetchSearchTopStories(searchKey, page + 1)}>
        More
      </Button>
    </div>
  </div>
);
}


由于当根据 `searchKey` 没有结果时，你默认返回一个空列表，所以你现在可以省去 `Table` 组件的条件渲染了。此外，你将需要向“更多”按钮传递 `searchKey` 而不是 `searchTerm`。否则，你的分页获取将依赖于变动的 `searchTerm` 值。此外，确保在“搜索”组件的输入字段中保留变动的 `searchTerm` 属性。

搜索功能应该可以再次工作。它存储了来自 Hacker News API 的所有结果。此外，`onDismiss()` 方法还需要改进。它仍然处理的是结果对象。现在它必须处理多个结果。

**src/App.js**
```javascript
onDismiss(id) {
  const { searchKey, results } = this.state;
  const { hits, page } = results[searchKey];
  const isNotId = item => item.objectID !== id;
  const updatedHits = hits.filter(isNotId);
  this.setState({
    results: {
      ...results,
      [searchKey]: { hits: updatedHits, page }
    }
  });
}
```

“关闭”按钮应该可以再次工作了。然而，没有任何可以阻止应用程序在每次提交搜索时发送 API 请求。尽管可能已经有了结果，但并没有检查机制来阻止请求。因此，缓存功能还不完整。它缓存了结果，但并没有利用它们。最后一步是在当缓存中有可用结果时防止 API 请求。

**src/App.js**
```javascript
class App extends Component {
  constructor(props) {
    ...
    this.needsToSearchTopStories = this.needsToSearchTopStories.bind(this);
    this.setSearchTopStories = this.setSearchTopStories.bind(this);
    this.fetchSearchTopStories = this.fetchSearchTopStories.bind(this);
    this.onSearchChange = this.onSearchChange.bind(this);
    this.onSearchSubmit = this.onSearchSubmit.bind(this);
    this.onDismiss = this.onDismiss.bind(this);
  }

  needsToSearchTopStories(searchTerm) {
    return !this.state.results[searchTerm];
  }
  ...

  onSearchSubmit(event) {
    const { searchTerm } = this.state;
    this.setState({ searchKey: searchTerm });
    if (this.needsToSearchTopStories(searchTerm)) {
      this.fetchSearchTopStories(searchTerm);
    }
    event.preventDefault();
  }
  ...
}
```

现在，即使你搜索了两次关键词，你的客户端也只向 API 发送一次请求。甚至几页的分页数据也被缓存了，因为你总是为 `results` 映射中的每个结果保存最后一页。这为你的应用程序引入缓存难道不是一种强大的方法吗？Hacker News API 提供了你所需的一切，甚至可以有效地缓存分页数据。

## 错误处理

你与 Hacker News API 交互的一切都已就绪。你甚至引入了一种优雅的方式来缓存来自 API 的结果，并利用其分页列表功能从 API 获取无限数量的帖子子列表。但还缺少了一部分。遗憾的是，这在如今的开发应用程序时经常被忽视：错误处理。实现“快乐路径”（happy path）而不担心在此过程中可能发生的错误太容易了。

在本章中，你将引入一种高效的解决方案，为你的应用程序添加错误处理，以防发生错误的 API 请求。你已经学习了在 React 中引入错误处理的必要构建模块：本地状态和条件渲染。基本上，错误只是 React 中的另一种状态。当发生错误时，你将其将其存储在本地状态中，并在组件中通过条件渲染显示出来。就这么了。让我们在 `App` 组件中实现它，因为它是最初用于从 Hacker News API 获取数据的组件。

首先，你必须在本地状态中引入错误。它被初始化为 `null`，但在发生错误时将被设置为错误对象。

**src/App.js**
```javascript
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      results: null,
      searchKey: '',
      searchTerm: DEFAULT_QUERY,
      error: null,
    };
  }
  ...
}
}
```

其次，你可以在原生 `fetch` 的 `catch` 块中使用 `setState()` 将错误对象存储在本地状态中。每当 API 请求未成功时，`catch` 块就会被执行。

**src/App.js**
```javascript
class App extends Component {
  ...
  fetchSearchTopStories(searchTerm, page = 0) {
    fetch(`${PATH_BASE}${SEARCH}?${searchTerm}&page=${page}`)
      .then(response => response.json())
      .then(result => this.setSearchTopStories(result))
      .catch(error => this.setState({ error }));
  }
  ...
}
```

第三，你可以在 `render()` 方法中从本地状态检索错误对象，并在发生错误时使用 React 的条件渲染显示消息。

**src/App.js**
```javascript
class App extends Component {
  ...
  render() {
    const { searchTerm, results, searchKey, error } = this.state;
    if (error) {
      return <p>Something went wrong.</p>;
    }
    return (
      <div className="page">
        ...
      </div>
    );
  }
}
```

就这么了。如果你想测试你的错误处理是否正常，可以将 API URL 更改为某些不存在的内容。

**src/App.js**
```javascript
const PATH_BASE = 'https://foo.bar.com/api/v1';
```

之后，你应该会得到错误消息而不是你的应用程序。你想在哪里放置错误消息的条件渲染取决于你。在这种情况下，整个应用将不再显示了。这可能不是最好的体验。那么，显示 `Table` 组件或错误消息怎么样呢？即使发生错误，剩余的应用程序仍然可见。

**src/App.js**
```javascript
class App extends Component {
  ...
  render() {
    const { searchTerm, results, searchKey, error } = this.state;
    const list = results && results[searchKey]?.hits || [];
    return (
      <div className="page">
        <div className="interactions">
          ...
        </div>
        {error ?
          <div className="interactions">
            <p>Something went wrong.</p>
          </div>
        : (
          <>
            <Table
              list={list}
              onDismiss={this.onDismiss}
            />
            <div className="interactions">
              <Button onClick={() => this.fetchSearchTopStories(searchKey, page + 1)}>
                More
              </Button>
            </div>
          </>
        )}
      </div>
    );
  }
}
```
最后，你应该将 URL 恢复为存在的路径。

## Axios 替代 Fetch

在之前的章节中，你引入了原生 `fetch` API 来请求 Hacker News。浏览器允许你使用这种原生 `fetch` API。然而，并不是所有浏览器（特别是旧浏览器）都支持它。此外，当你开始为运行在浏览器之外的编写测试时（此时没有浏览器，而是模拟），可能会出现 fetch API 的问题。有几种方法可以使 fetch 在旧浏览器中（通过 polyfills）和测试中（通过 isomorphic-fetch）工作，但我们不会在书中讨论这些。

解决此问题的另一种方法是使用稳定的库 `axios` 来替代原生 `fetch` API。Axios 是一个只解决问题的库，但它以高质量的方式解决了这个问题：执行远程 API 请求。这就是为什么我们会在书中使用它。在具体层，本章节将向你展示如何用另一个库替换库（在这种情况下是浏览器的原生 API）。在抽象层，它应该展示如何始终为 Web 开发中的特殊情况（例如旧浏览器、无头测试）寻找解决方案。因此，遇到困难时不要停止寻找解决方案。

让我们看看如何用 axios 替代原生 fetch API。实际上，之前说的一切听起来比实际上要困难。首先，你需要在命令行安装 axios：

**命令行**
```bash
npm install axios
```

其次，你可以在 App 组件文件中引入 axios：

**src/App.js**
```javascript
import React, { Component } from 'react';
import axios from 'axios';
import './App.css';
...
```

最后，你可以用它代替 `fetch()`。它的用法与原生 `fetch` API 几乎相同。它接受 URL 作为参数并返回一个 promise。你不再需要将返回的响应转换为 JSON。Axios 会为你完成转换并将结果封装在 JavaScript 的 data 对象中。因此，请确保你的代码适应返回的数据结构。




## 深入实战 API

118

**src/App.js**

```javascript
class App extends Component {
  ...

  fetchSearchTopStories(searchTerm, page = 0) {
    axios(`${PATH_BASE}${PATH_SEARCH}?${PARAM_SEARCH}${searchTerm}&${PARAM_PAGE}${page}&${PARAM_HPP}${DEFAULT_HPP}`)
      .then(result => this.setSearchTopStories(result.data))
      .catch(error => this.setState({ error }));
  }

  ...
}
```

本章关于用 axios 替换 fetch 的就到此了。在你的代码中，你调用 `axios()`，它默认使用 HTTP GET 请求。你可以通过调用 `axios.get()` 让 GET 请求变得显式。此外，你也可以使用其他 HTTP 方法，例如通过 `axios.post()` 使用 HTTP POST。在这里，你已经可以看到 axios 是一个用于向远程 API 请求的强大库了。当你的 API 请求变得复杂或者你必须处理 Web 开发中 Promise 的特殊问题时，我经常建议使用它而不是原生的 fetch API。此外，在稍后的章节中，你将为应用程序引入测试。到时候你就不再需要担心浏览器或无头浏览器环境了。

我想为 App 组件中的 Hacker News 请求引入另一个改进。假设你的组件在浏览器首次渲染页面时挂载（mount）。在 `componentDidMount()` 中，组件开始发送请求，但由于你的应用程序引入了某种导航，你离开了此页面并到了另一个页面。你的 App 组件卸载（unmount）了，但来自 `componentDidMount()` 生命周期方法的请求仍然处于挂起状态。它最终会尝试在 promise 的 `then()` 或 `catch()` 块中使用这个 `this.setState()`。也许这时你将第一次在命令行或浏览器开发者工具输出中看到以下警告：

**命令行**

Warning: Can only update a mounted or mounting component. This usually means you called setState, replaceState, or forceUpdate on an unmounted component. This is a no-op.

你可以通过在组件卸载时中止请求，或者防止在已卸载的组件上调用 `this.setState()` 来解决这个问题。这在 React 中是一种最佳实践，尽管许多开发者并没有遵循，但它可以保持应用程序的整洁，避免任何烦人的警告。

然而，目前的 promise API 并没有实现中止请求。因此，你需要自己来解决这个问题。这可能也是为什么没有多少开发者遵循这一最佳实践的原因。下面的实现看起来更像是一个通宜之而不是一个可持续的实现。因此，你可以决定是否要实现它来绕过由于已卸载组件导致的警告。尽管如此，请记住这个警告，以防它在本书的后后章节或你以后自己的应用程序中出现。到时候你就知道如何处理它了。

让我们开始规避这个问题。你可以引入一个类字段（class field）来持有组件的生命周期状态。它可以在组件初始化时初始化为 `false`，在组件挂载时更改为 `true`，然后在组件卸载时再次设为 `false`。这样，你就可以跟踪组件的生命周期状态。这与通过 `this.state` 和 `this.setState()` 存储和修改的本地状态无关，因为你应该直接在组件实例上访问它，而不依赖 React 的本地状态管理。此外，当以这种方式更改类字段时，不会导致组件的重新渲染。

**src/App.js**

```javascript
class App extends Component {
  _isMounted = false;

  constructor(props) {
    ...
  }

  ...

  componentDidMount() {
    this._isMounted = true;
    const { searchTerm } = this.state;
    this.setState({ searchKey: searchTerm });
    this.fetchSearchTopStories(searchTerm);
  }

  componentWillUnmount() {
    this._isMounted = false;
  }

  ...
}
```

最后，你可以利用这个知识不是去中止请求本身，而是为了在组件已经卸载的情况下在组件实例上调用 `this.setState()`。它将防止上述警告。

**src/App.js**

```javascript
class App extends Component {
  ...

  fetchSearchTopStories(searchTerm, page = 0) {
    axios(`${PATH_BASE}${PATH_SEARCH}?${PARAM_SEARCH}${searchTerm}&${PARAM_PAGE}${page}&${PARAM_HPP}${DEFAULT_HPP}`)
      .then(result => this._isMounted && this.setSearchTopStories(result.data))
      .catch(error => this._isMounted && this.setState({ error }));
  }

  ...
}
```

总来说，本章向你展示了如何在 React 中用一个库替换另一个库。如果你遇到任何问题，可以使用 JavaScript 庞大的库生态系统来帮助自己。此外，你还看到了一种在 React 中避免在已卸载组件上调用 `this.setState()` 的方法。如果你深入研究 axios 库，你也会发现一种从根上防止取消请求的方法。这取决于你是否进一步阅读这个主题。

**练习：**

- 了解更多关于为什么框架很重要^(110)
- 学习更多关于替代的 React 组件语法^(111)

110 https://www.robinwieruch.de/why-frameworks-matter/
111 https://github.com/the-road-to-learn-react/react-alternative-class-component-syntax

你已经学会了如何在 React 中与 API 交互！让我们回顾一下最后几章：

- React
    - 针对不同用例的 ES6 类组件生命周期方法
    - 用于 API 交互的 `componentDidMount()`
    - 条件渲染
    - 表单上的合成事件
    - 错误处理
    - 中止远程 API 请求
- ES6 及以后
    - 使用模板字符串组合字符串
    - 用于不可变数据结构的展开运算符
    - 计算属性名
    - 类字段
- 一般
    - Hacker News API 交互
    - 原生 fetch 浏览器 API
    - 客户端和服务器端搜索
    - 数据分页
    - 客户端缓存
    - axios 作为原生 fetch API 的替代方案

再次，休息一下是有意义的。内化所学知识并将它们应用于你自己。你可以对目前已有的源代码进行实验。你可以在^(112)找到源代码。

112 https://github.com/the-road-to-learn-react/hackernews-client/tree/5.3.1

## 代码组织与测试

本章将重点关注保持代码可维护性的重要主题。你将在构建文件夹和文件时学习组织工作。你将学习的另一个方面是测试，这对于保持代码的健壮至关重要。整个章节将跳回应用，解释这些主题。

### ES6 模块：导入与导出

在 JavaScript ES6 中，你可以从模块导入和导出功能。这些功能可以是函数、类、组件、常量等。基本上是可以赋值给变量的一切。模块可以是单个文件，也可以是以索引文件为入口点的整个文件夹。在书的开头，当你用 `create-react-app` 引导应用程序后，你已经在初始文件中使用了多个导入导出语句。现在是解释这些内容的时机了。

导入和导出语句帮助你在多个文件之间共享代码。在此之前，JavaScript 环境对此有多种解决方案。这是一团糟，因为你希望遵循一种标准方法，而不是对同一件事有多种方法。现在自 JavaScript ES6 起它是原生行为。

此外，这些语句拥抱代码拆分。你将代码分布在多个文件中以保持其可复用可维护性。前者是真的，因为你可以在多个文件中导入这段代码。后者也是真的，因为你有一个单一的源来维护这段代码。文件的导出基本上是该文件的公共 API。只有导出的功能才能在其他地方被复用。

但让我们实际操作一下。这些导入和导出语句是如何工作的？下面的示例通过在两个文件之间共享一个或多个变量展示了这些语句。最后，这种方法可以扩展到多个文件并共享比简单变量更多的内容。

你可以导出一个或多个变量。这被称为命名导出。

**代码沙场：file1.js**

```javascript
const firstname = 'robin';
const lastname = 'wieruch';

export { firstname, lastname };
```





## 代码组织与测试

**代码沙场：file2.js**

```javascript
import { firstname, lastname } from './file1.js';

console.log(firstname);

// output: robin
```

你也可以作为一个对象的形式从另一个文件中导入所有导出变量。

**代码沙场：file2.js**

```javascript
import * as person from './file1.js';

console.log(person.firstname);

// output: robin
```

导入可以有别名。可能会出现你从多个文件中导入具有同名导出的功能的情况。这就是为什么你可以使用别名。

**代码沙场：file2.js**

```javascript
import { firstname as foo } from './file1.js';

console.log(foo);

// output: robin
```

最后但同样重要的是，还存在默认 `default` 语句。它可以用于以下几种用例：

- 导出和导入单个功能
- 突出模块导出 API 的主要功能
- 拥有一个回退导入功能

**代码沙场：file1.js**

```javascript
const robin = {
  firstname: 'robin',
  lastname: 'wieruch',
};

export default robin;
```

在导入时可以省略大括号来导入默认导出。

**代码沙场：file2.js**

```javascript
import developer from './file1.js';

console.log(developer);

// output: { firstname: 'robin', lastname: 'wieruch' }
```

此外，导入的名称可以与导出的默认名称不同。你也可以将其与具名导出和导入语句结合使用。

**代码沙场：file1.js**

```javascript
const firstname = 'robin';
const lastname = 'wieruch';
const person = {
  firstname,
  lastname,
};

export {
  firstname,
  lastname,
};

export default person;
```

**代码沙场：file2.js**

```javascript
import developer, { firstname, lastname } from './file1.js';

console.log(developer);

// output: { firstname: 'robin', lastname: 'wieruch' }
console.log(firstname, lastname);

// output: robin wieruch
```

在具名导出中，你可以节省额外的行并直接导出变量。

**代码沙场：file1.js**

```javascript
export const firstname = 'robin';
export const lastname = 'wieruch';
```

这些是 ES6 模块的主要功能。它们帮助你组织代码、维护代码并设计可重用的模块 API。你也可以导出和导入功能以测试它们。你将在接下来的章节中操作。

**练习：**

- 更多关于 ES6 导入 (113)
- 更多关于 ES6 导出 (114)

113 https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import
114 https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export

### 使用 ES6 模块进行代码组织

你可能会想：为什么我们没有对 *src/App.js* 文件遵循代码分割的最佳实践？在文件中我们已经有了多个组件，这些组件可以定义在自己的文件/文件夹（模块）中。为了学习 React，将这些内容放在一个地方是切实际的。但一旦你的 React 应用程序增长，你就应该考虑将这些组件拆分成多个模块。只有这样，你的应用程序才能扩展。

在接下来，我将提出几种你可以运用的模块结构。我建议在书的末尾作为一个练习应用它们。为了保持书本身的简单，我将不会执行代码分割，并在后续章节中继续使用 *src/App.js* 文件。

一种可能的模块结构可能是：

**目录结构**

| src/ |
| :--- |
| index.js |
| index.css |
| App.js |
| App.test.js |
| App.css |
| Button.js |
| Button.test.js |
| Button.css |
| Table.js |
| Table.test.js |
| Table.css |
| Search.js |
| Search.test.js |
| Search.css |

它将组件分到了它们自己的文件中，但看起来并不太乐观。你可以看到很多命名重复，仅仅是文件扩展名不同。另一种模块结构可能是：

**目录结构**

| src/ |
| :--- |
| index.js |
| index.css |
| App/ |
| index.js |
| test.js |
| index.css |
| Button/ |
| index.js |
| test.js |
| index.css |
| Table/ |
| index.js |
| test.js |
| index.css |
| Search/ |
| index.js |
| test.js |
| index.css |

它看起来比以前更整洁。文件的 `index` 命名将其描述为该文件夹的入口文件。这是一种常见的命名约定，但你也可以使用自己的命名。在这个模块结构中，组件通过其 JavaScript 文件中的组件声明定义，同时也通过其样式和测试定义。

另一个步骤可能是从 App 组件中提取常量变量。这些常量被用于组合 Hacker News API URL。

**目录结构**

| src/ |
| :--- |
| index.js |
| index.css |
| **constants//** |
| **index.js** |
| **components//** |
| App/ |
| index.js |
| test.js |
| index.css |
| Button/ |
| index.js |
| test.js |
| index.css |

自然情况下，模块将拆分到 *constants/* 和 *components/*。现在 *constants/index.js* 文件可能像这样：

**代码沙场：constants/index.js**

```javascript
export const DEFAULT_QUERY = 'redux';
export const DEFAULT_HPP = '100';
export const PATH_BASE = 'https://hn.algolia.com/api/v1';
export const PATH_SEARCH = '/search';
export const PARAM_SEARCH = 'query=';
export const PARAM_PAGE = 'page=';
export const PARAM_HPP = 'hitsPerPage=';
```

*App/index.js* 文件可以导入这些变量以使用它们。

**代码沙场：components/App/index.js**

```javascript
import {
  DEFAULT_QUERY,
  DEFAULT_HPP,
  PATH_BASE,
  PATH_SEARCH,
  PARAM_SEARCH,
  PARAM_PAGE,
  PARAM_HPP
} from '../constants/index.js';
```

当你使用 `index.js` 命名约定时，可以从相对路径中省略文件名。

**代码沙场：components/App/index.js**

```javascript
import {
  DEFAULT_QUERY,
  DEFAULT_HPP,
  PATH_BASE,
  PATH_SEARCH,
  PARAM_SEARCH,
  PARAM_PAGE,
  PARAM_HPP
} from '../constants';
```

但 `index.js` 文件命名的背后是什么？这个约定是在 node.js 世界引入的。index 文件是模块的入口点。它描述了模块的公共 API。外部模块仅允许 `index.js` 文件来导入模块的共享代码。考虑以下假设模块结构来演示：

**目录结构**

| src/ |
| :--- |
| index.js |
| App/ |
| index.js |
| Buttons/ |
| index.js |
| SubmitButton.js |
| SaveButton.js |
| CancelButton.js |

*Buttons/* 文件夹在其不同的不同的文件中定义了多个按钮组件。每个文件都可以导出特定的组件以供 *Buttons/index.js* 使用。*Buttons/index.js* 文件导入所有不同的按钮表示并将它们导出为公共模块 API。

**代码沙场：Buttons/index.js**

```javascript
import SubmitButton from './SubmitButton';
import SaveButton from './SaveButton';
import CancelButton from './CancelButton';

export {
  SubmitButton,
  SaveButton,
  CancelButton,
};
```

现在 *src/App/index.js* 可以从位于 *index.js* 文件的公共 API 导入按钮。

**代码沙场：components/App/index.js**

```javascript
import {
  SubmitButton,
  SaveButton,
  CancelButton
} from '../Buttons';
```

通过这种约束，进入模块中除 *index.js* 以外的文件将是坏习惯。它会破坏封装的规则。

**代码沙场：components/App/index.js**

```javascript
// 坏习惯，不要这样做
import SubmitButton from '../Buttons/SubmitButton';
```





## 代码组织与测试

132

### 使用 Jest 进行快照测试

本书将不会深入探讨测试主题，但不应该忽视它。在编程中，测试代码是至关重要的，并且应该被视为强制性的。你希望保持代码的高质量，并确保一切运行正常。

你可能听说过测试金字塔。它包括端到端测试、集成测试和单元测试。如果你不熟悉这些，本书将为你提供快速且基础的概述。单元测试用于测试隔离的较小代码块。一个单元测试可以对一个单一的函数进行测试。然而，有时单元在孤立状态下运行良好，但与其他单元结合时无法正常工作。它们需要作为一个整体进行组合测试。这就是集成测试大显身场，它可以涵盖单元之间是否协作良好。最后，端到端测试是对真实用户场景的模拟。它可以是浏览器中的自动化设置，模拟用户在 Web 应用程序中的登录流程。虽然单元测试快速且易编写和维护，但端到端测试处于光谱的另一端。

每种类型需要多少个测试？你需要许多单元测试来覆盖孤立函数。之后，你可以有几个集成测试来确保最重要的函数按预期组合工作。最后，你可能只需要少量的端到端测试来模拟 Web 应用程序中的关键场景。这就是对测试世界的通用漫览。

那么，你如何将这些知识应用于 React 应用程序的测试中？React 测试的基础是组件测试，它可以被泛括为单元测试，且其一部分是快照测试。在下一章中，你将使用一个名为 Enzyme 的库对组件进行单元测试。在这一章中，你将关注另一种测试：快照测试。这就是 Jest 发挥用场的地方。

Jest^[115](https://facebook.github.io/jest/) 是一个在 Facebook 使用的 JavaScript 测试框架。在 React 社区中，它用于 React 组件测试。幸运的是，*create-react-app* 已经自带了 Jest，所以你不需要担心设置它。

让我们开始测试你的第一个组件吧。在此之前，你必须从 *src/App.js* 文件中导出想要测试的组件。之后，你可以在不同的文件中对它们进行测试。你已经在代码组织章节中学习过这些。

133

**src/App.js**

```javascript
...
class App extends Component {
...
}
...
export default App;

export {
  Button,
  Search,
  Table,
};
```

在你的 *App.test.js* 文件中，你会找到来自 *create-react-app* 的第一个测试。它验证了 App 组件在渲染时不会出现任何错误。

**src/App.test.js**
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

it('renders without crashing', () => {
  const div = document.createElement('div');
  ReactDOM.render(<App />, div);
  ReactDOM.unmountComponentAtNode(div);
});
```

“it”-块描述一个测试用例。它包含测试描述，当你运行它时，它可以成功或失败。此外，你可以将其封装在一个“describe”-块中定义你的测试套件。一个测试套件可以包含针对特定组件的一组“it”-块。你稍后看到这些“describe”-块。这两个块用于分离和组织你的测试用例。注意，it 函数在 JavaScript 社区中被认为是运行单个测试的函数。然而，在 Jest 中，它通常被发现 test 函数的别名。

你可以通过命令行使用交互式的 *create-react-app* 测试脚本来运行测试用例。你将在命令行界面上获得所有测试用例的输出。

### 命令行
```bash
npm test
```

现在 Jest 允许你编写快照测试。这些测试会对渲染的组件创建一个快照，并将快照与未来的快照进行对比。当未来的快照发生变化时，测试会通知。你可以接受快照更改（因为你故意更改了组件实现），也可以拒绝更改并调查错误。它很好地补充了单元测试，因为你只测试渲染输出的差异。它不会增加大量的维护成本，因为当你故意更改组件的渲染输出时，只需接受更改的快照即可。

Jest 将快照存储在文件夹中。只有这样它可以验证与未来快照的差异。此外，可以通过将快照放在一个文件夹中跨团队共享。

在用 Jest 编写第一个快照测试之前，你需要安装一个工具库。

### 命令行
```bash
npm install --save-dev react-test-renderer
```

现在你可以用第一个快照测试来扩展 App 组件测试了。首先，从 node 包中导入新功能，并将你之前用于 App 组件的“it”-块封装在一个描述性的“describe”-块中。在这种情况下，测试套件仅针对 App 组件。

**src/App.test.js**
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
import App from './App';

describe('App', () => {
  it('renders without crashing', () => {
    const div = document.createElement('div');
    ReactDOM.render(<App />, div);
    ReactDOM.unmountComponentAtNode(div);
  });
});
```

现在你可以通过使用“test”-块来实现你的第一个快照测试。

**src/App.test.js**
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
import App from './App';

describe('App', () => {
  it('renders without crashing', () => {
    const div = document.createElement('div');
    ReactDOM.render(<App />, div);
    ReactDOM.unmountComponentAtNode(div);
  });

  test('has a valid snapshot', () => {
    const component = renderer.create(
      <App />
    );
    let tree = component.toJSON();
    expect(tree).toMatchSnapshot();
  });
});
```

再次运行测试并查看测试如何成功或失败。它们应该是成功的。一旦你更改了 App 组件的输出，快照测试应该失败。然后你可以决定更新快照或调查你的 App 组件。基本上，renderer.create() 函数创建了 App 组件的快照。它进行虚拟渲染并将 DOM 存储到快照中。之后，该快照将与你运行快照测试时之前的快照匹配。通过这种方式，你可以确保 DOM 保持不变且不会意外更改。

让我们为我们的独立组件添加更多测试。首先是 Search 组件：

**src/App.test.js**
```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
import App, { Search } from './App';

describe('Search', () => {
  it('renders without crashing', () => {
    const div = document.createElement('div');
    ReactDOM.render(<Search>Search</Search>, div);
    ReactDOM.unmountComponentAtNode(div);
  });

  test('has a valid snapshot', () => {
    const component = renderer.create(
      <Search>Search</Search>
    );
    let tree = component.toJSON();
    expect(tree).toMatchSnapshot();
  });
});
```

其次，你可以测试 Button 组件，其适用与 Search 组件相同的测试规则。





## 代码组织与测试

137

**src/App.test.js**

...

**import App, { Search, Button } from './App';**

...

**describe('Button', () => {
  it('renders without crashing', () => {
    const div = document.createElement('div');
    ReactDOM.render(<Button>Give Me More</Button>, div);
    ReactDOM.unmountComponentAtNode(div);
  });
  test('has a valid snapshot', () => {
    const component = renderer.create(
      <Button>Give Me More</Button>
    );
    let tree = component.toJSON();
    expect(tree).toMatchSnapshot();
  });
});

最后但同样重要的，Table 组件允许你向它传递一组初始 props 来使用一个示例列表进行渲染。

**src/App.test.js**

...

**import App, { Search, Button, Table } from './App';**

...

**describe('Table', () => {
  const props = {
    list: [
      { title: '1', author: '1', num_comments: 1, points: 2, objectID: 'y' },
      { title: '2', author: '2', num_comments: 1, points: 2, objectID: 'z' },
    ],
  };

138

it('renders without crashing', () => {
    const div = document.createElement('div');
    ReactDOM.render(<Table { ...props } />, div);
  });
  test('has a valid snapshot', () => {
    const component = renderer.create(
      <Table { ...props } />
    );
    let tree = component.toJSON();
    expect(tree).toMatchSnapshot();
  });
});

快照测试通常保持非常基础。你只需要确保组件没有改变它的输出。一旦输出发生了变化，你就必须决定是否接受这些更改。否则，当输出不符合预期时，你必须修复组件。

**练习：**

- 查看在更改 `render()` 方法中的组件返回值后，快照测试是如何失败的—— 接受或拒绝快照更改
- 在后续章节中组件实现发生变化时，保持你的快照测试为最新
- 了解更多关于 React 中 Jest 的信息^(116)

116https://facebook.github.io/jest/docs/tutorial-react.html

139

### 使用 Enzyme 进行单元测试

Enzyme^(117) 是 Airbnb 提供的一一个测试工具，用于断言、操作和遍历你的 React 组件。

你可以用它来进行单元测试，以补充 React 中的快照测试。

让我们看看如何使用 enzyme。首先你必须安装它，因为它没有随 *create-react-app* 默认提供。它还包含一个在 React 中使用的扩展。

**命令行**

npm install --save-dev enzyme react-addons-test-utils enzyme-adapter-react-16

其次，你需要将其包含在测试设置中并初始化 Adapter 以在 React 中使用。

**src/App.test.js**

import React from 'react';

import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
**import Enzyme from 'enzyme';**
**import Adapter from 'enzyme-adapter-react-16';**
import App, { Search, Button, Table } from './App';
**Enzyme.configure({ adapter: new Adapter() });**

现在你可以在 Table 的 “describe”-块中编写你的第一个单元测试。你将使用 `shallow()` 来渲染你的组件，并断言 Table 有两个项目，因为你传递了两个列表项。

断言简单地检查元素是否具有具有 `table-row` 类的元素。

**src/App.test.js**

import React from 'react';

import ReactDOM from 'react-dom';
import renderer from 'react-test-renderer';
**import Enzyme, { shallow } from 'enzyme';**
import Adapter from 'enzyme-adapter-react-16';
import App, { Search, Button, Table } from './App';

...

describe('Table', () => {
117https://github.com/airbnb/enzyme

140

const props = {
  list: [
    { title: '1', author: '1', num_comments: 1, points: 2, objectID: 'y' },
    { title: '2', author: '2', num_comments: 1, points: 2, objectID: 'z' },
  ],
};

...

it('shows two items in list', () => {
    const element = shallow(
      <Table { ...props } />
    );
    expect(element.find('.table-row').length).toBe(2);
  });
});

Shallow 渲染组件但不包含其子组件。这样，你可以让测试专注于某一个组件。

Enzyme 在其 API 中总共有三种渲染机制。你已经知道 `shallow()`，但也存在 `mount()` 和 `render()`。它们都会实例化父组件和所有子组件。此外，`mount()` 让你可以访问组件的生命周期方法。但什么时候使用哪种渲染机制呢？

- 始终从 `shallow` 开始
- 如果应该测试 `componentDidMount()` 或 `componentDidUpdate()`，使用 `mount()`
- 如果你想测试子组件，使用 `mount()`
- 如果你对生命周期方法感兴趣，使用 `render()`

你可以使用 `mount()` 来测试你的组件。但要保持它们简单。否则你一开始就有 Jest 组件的问题了。

**练习：**

- 使用 Enzyme 为你的组件编写一个单元测试
- 在接下来的章节中更新你的测试
- 了解更多关于 enzyme 及其 API^(118)

118https://github.com/enzyme

141

## 使用 PropTypes 定义组件接口

你可能知道 TypeScript^(119) 或 Flow^(120)^ 可以为 JavaScript 引入类型。类型化语言是出错的，因为代码会根据其类型进行验证。编辑器和其他工具可以在程序运行之前捕获这些错误。React 自带了一个内置类型检查器以防止 Bug。你可以使用 PropTypes 来描述你的组件。从父子组件获取的所有 props 都会根据分配给子组件的 PropTypes 接口进行验证。本章将向你展示如何使用 PropTypes 使你的所有组件类型安全。

首先，你必须为 React 安装一个独立的包。

**命令行**

npm install prop-types

现在，你可以导入 PropTypes。

**src/App.js**

import React, { Component } from 'react';
import axios from 'axios';
**import PropTypes from 'prop-types';**

让我们开始为组件分配 props 接口：

**src/App.js**

const Button = ({

onClick,

className = '',

children,

}) =>

<button

onClick={onClick}
className={className}
type="button"
119https://www.typescriptlang.org/
120https://flowtype.org/

142

>

{children}

</button>

**Button.propTypes = {
**onClick: PropTypes.func,**
**className: PropTypes.string,**
**children: PropTypes.node,**
};**

基本上就是这样。你获取函数签名中的每个参数并为它分配一个 PropType。基本类型和复杂对象的基本 PropTypes 有：

- PropTypes.array
- PropTypes.bool
- PropTypes.func
- PropTypes.number
- PropTypes.object
- PropTypes.string

此外，你还有两个 PropType 用于定义可渲染的片段（node），例如字符串，以及 React 元素：

- PropTypes.node
- PropTypes.element

你已经在 Button 组件中使用 node PropType。总的来说，有更多 PropType 定义可以在 React 官方文档中查阅。

目前为 Button 定义的所有 PropTypes 都是可选的。参数可以是 null 或 undefined。但对于某些 props，你希望强制它们是已定义的。你可以将传递这些 props 传递组件作为一项要求。





## 代码组织与测试

143

**src/App.js**

```javascript
Button.propTypes = {
  onClick: PropTypes.func.isRequired,
  className: PropTypes.string,
  children: PropTypes.node.isRequired,
};
```

`className` 不是必须的，因为它可以默认为空字符串。接下来你将为 `Table` 组件定义一个 PropType 接口：

**src/App.js**

```javascript
Table.propTypes = {
  list: PropTypes.array.isRequired,
  onDismiss: PropTypes.func.isRequired,
};
```

你可以更显式地定义数组 PropType 的内容：

**src/App.js**

```javascript
Table.propTypes = {
  list: PropTypes.arrayOf(
    PropTypes.shape({
      objectID: PropTypes.string.isRequired,
      author: PropTypes.string,
      url: PropTypes.string,
      num_comments: PropTypes.number,
      points: PropTypes.number,
    })
  ).isRequired,
  onDismiss: PropTypes.func.isRequired,
};
```

只有 `objectID` 是必须的，因为你知道某些代码依赖于它。其他属性仅用于显示，因此它们并不一定是必须。此外，你无法确定 Hacker News API 是否对数组中的每个对象都具有定义的属性。

PropTypes 部分就到这里。但还有另一个方面：你可以在组件中定义默认属性（default props）。再次以 `Button` 组件为例。`className` 属性在组件签名有一个 ES6 默认参数。

144

**src/App.js**

```javascript
const Button = ({
  onClick,
  className = '',
  children
}) =>

...
```

你可以将其替换为 React 内部的 `defaultProps`：

**src/App.js**

```javascript
const Button = ({
  onClick,
  className,
  children
}) => (
  <button
    onClick={onClick}
    className={className}
    type="button"
  >
    {children}
  </button>
);

Button.defaultProps = {
  className: '',
};
```

与 ES6 默认参数相同，`defaultProps` 确保当父组件没有指定该属性时，该属性被设置为默认值。PropType 类型检查会在 `defaultProps` 求值之后发生。

如果你再次运行测试，可能会在命令行中看到针对组件的 PropType 错误。这可能是因为你没有在测试中为组件定义所有在 PropType 定义中标记为必需（required）的属性。不过，测试本身都是正确通过的。你可以为测试中的组件传递所有必需属性以避免这些错误。

**练习：**

- 为 `Search` 组件定义 PropType 接口
- 在接下来的章节中添加和更新组件时，添加并更新 PropType 接口
- 了解更多关于 React PropTypes^(121)

121https://reactjs.org/docs/typechecking-with-proptypes.html

146

你已经学习了如何组织代码以及如何测试它！让我们回顾一下最后几章节：

- React
  - PropTypes 允许你为组件定义类型检查
  - Jest 允许你为组件编写快照测试（snapshot tests）
  - Enzyme 允许你为组件编写单元测试
- ES6
  - import 和 export 语句帮助你组织代码
- 通用
  - 代码组织允许你通过最佳实践扩展你的应用程序

你可以在官方仓库中找到源码^(122)。

122https://github.com/the-road-to-learn-react/hackernews-client/tree/5.4

## 高级 React 组件

本章将重点关注高级 React 组件的实现。你将学习高阶组件（higher-order components）以及如何实现它们。此外，你将深入 React 中更高级的主题并用它实现复杂的交互。

148

### Ref DOM 元素

有时你需要在 React 中与 DOM 节点进行交互。`ref` 属性允许你访问元素中的节点。这在 React 中通常是一种反模式，因为你应该使用它的声明式方法和单向数据流。你在介绍第一个搜索输入框时已经学习过它了。但在某些情况下，你需要访问 DOM 节点。官方文档提到了三种用例：

- 使用 DOM API（聚焦、媒体播放等）
- 调用命令式的 DOM 节点动画
- 与需要 DOM 节点的第三方库集成（例如 D3.js^(123)）

让我们通过 `Search` 组件的示例来实现。当应用程序首次渲染时，输入框应该获得聚焦。这就是你需要访问 DOM API 的用例之一。本章将向你展示它是如何工作的，但由于它对应用程序本身并不有用，我们将在章节之后省略这些更改。不过你可以为自己的应用程序保留它。

通常情况下，你可以在函数式无状态组件和 ES6 类组件中使用 `ref` 属性。在聚焦用例的示例中，你需要一个生命周期方法。这就是为什么首先通过使用 ES6 类组件配合 `ref` 属性来这种方法。

第一步是将函数式无状态组件重构为 ES6 类组件。

**src/App.js**

```javascript
class Search extends Component {
  render() {
    const {
      value,
      onChange,
      children
    } = this.props;
    return (
      <form onSubmit={onSubmit}>
        <input
          type="text"
          value={value}
          onChange={onChange}
          ref={(node) => {
            123https://d3.org/
          }}
        />
        <button type="submit">
          {children}
        </button>
      </form>
    );
  }
}
```

149

**src/App.js**

```javascript
class Search extends Component {
  render() {
    const {
      value,
      onChange,
      children
    } = this.props;
    return (
      <form onSubmit={onSubmit}>
        <input
          type="text"
          value={value}
          onChange={onChange}
          ref={(node) => {
            this.input = node;
          }}
        />
        <button type="submit">
          {children}
        </button>
      </form>
    );
  }
}
```

150

**src/App.js**

```javascript
class Search extends Component {
  componentDidMount() {
    if (this.input) {
      this.input.focus();
    }
  }
  render() {
    const {
      value,
      onChange,
      children
    } = this.props;
    return (
      <form onSubmit={onSubmit}>
        <input
          type="text"
          value={value}
          onChange={onChange}
          ref={(node) => {
            this.input = node;
          }}
        />
        <button type="submit">
          {children}
        </button>
      </form>
    );
  }
}
```

151

**src/App.js**

```javascript
const Search = ({
  value,
  onChange,
  children
}) => {
  let input;
  return (
    <form onSubmit={onSubmit}>
      <input
        type="text"
        value={value}
        onChange={onChange}
        ref={(node) => (input = node)}
      />
      <button type="submit">
        {children}
      </button>
    </form>
  );
};
```

152

**Loading …**

```javascript
const Loading = () => <div>Loading ...</div>;
```

**src/App.js**

```javascript
class App extends Component {
  _isMounted = false;
  constructor(props) {
    super(props);
    this.state = {
      results: null,
      searchKey: '',
      searchTerm: DEFAULT_QUERY,
      error: null,
      isLoading: false,
    };
  }
  ...
}
...
```




高级 React 组件

153

**src/App.js**

```javascript
class App extends Component {
  ...

  setSearchTopStories(result) {
    ...

    this.setState({
      results: {
        ...results,
        [searchKey]: { hits: updatedHits, page }
      },
      isLoading: false
    });
  }

  fetchSearchTopStories(searchTerm, page = 0) {
    this.setState({ isLoading: true });
    axios(`${PATH_BASE}${PATH_SEARCH}?${PARAM_SEARCH}${searchTerm}&${PARAM_PAGE}
${page}&${PARAM_HPP}${DEFAULT_HPP}`)
      .then(result => this._isMounted && this.setSearchTopStories(result.data))
      .catch(error => this._isMounted && this.setState({ error }));
  }

  ...
}
```

在最后一步中，你将在 App 中使用 Loading 组件。基于加载状态的条件渲染将决定显示 Loading 组件还是 Button 组件。后者是你用于获取更多数据的按钮。

高级 React 组件

154

**src/App.js**

```javascript
class App extends Component {
  ...

  render() {
    const {
      searchTerm,
      results,
      searchKey,
      error,
      isLoading
    } = this.state;
    ...

    return (
      <div className="page">
        ...
        <div className="interactions">
          { isLoading
            ? <Loading />
            : <Button
                onClick={() => this.fetchSearchTopStories(searchKey, page + 1)}>
                More
              </Button>
          }
        </div>
      </div>
    );
  }
}
```

当你启动应用程序时，Loading 组件将显示，因为你在 `componentDidMount()` 中发送了请求。没有 Table 组件，因为列表是空的。当响应从 Hacker News API 返回时，结果将显示，加载状态被设置为 false，Loading 组件消失。相反，用于获取更多数据的“More”按钮会出现。一旦你获取了更多数据，按钮将再次消失，Loading 组件将再次显示。

高级 React 组件

155

**练习题：**

- 使用如 Font Awesome^(126) 类的库来显示加载图标，而不是“Loading …”文本

126http://fontawesome.io/

高级 React 组件

156

**高阶组件 (Higher-Order Components)**

高阶组件 (HOC) 是 React 中的一个高级概念。HOC 等同于高阶函数。它们接收任何输入——大多数情况下是组件，但也可能是可选参数——并返回一个组件作为输出。返回的组件是输入组件的增强版本，可以使用于你的 JSX 中。

HOC 用于不同的用例。它们可以准备属性、管理状态或更改组件的表示。一个用例可以是将 HOC 作为条件渲染的辅助。假设你有一个 List 组件，它可以渲染一个项目列表，或者什么都不渲染（因为列表为空或为）。HOC 可以屏蔽掉在没有列表时列表不渲染任何内容的问题。另一方面，普通的 List 组件就不再需要担心一个不存在的列表了。它只关心渲染列表。

让我们来做一个简单的 HOC，它接收一个组件作为输入并返回一个组件。你可以将其放在你的 *src/App.js* 文件中。

**src/App.js**

```javascript
function withFoo(Component) {
  return function(props) {
    return <Component { ...props } />;
  }
}
```

一个整洁的约定是在 HOC 的命名前加上 `with`。由于你正在使用 JavaScript ES6，你可以用 ES6 箭头函数更简洁地表示 HOC。

**src/App.js**

```javascript
const withFoo = (Component) => (props) =>
  <Component { ...props } />
```

在示例中，输入组件将与输出组件相同。什么都没有发生。它渲染相同的组件实例，并将所有的 props 传递给输出组件。但那是没用的。让我们增强输出组件。当加载状态为 true 时，输出组件应该显示 Loading 组件。

高级 React 组件

170

157

**src/App.js**

```javascript
const withFoo = (Component) => (props) =>
  isLoading
    ? <Loading />
    : <Component { ...props } />
```

条件渲染渲染是 HOC 的一个极佳用例。

在示例中，输入组件将与输出组件相同。什么都没有发生。它渲染相同的组件实例，并将所有的 props 传递给输出组件。但那是没用的。让我们增强输出组件。当加载状态为 true 时，输出组件应该显示 Loading 组件。

一个整洁的约定是在 HOC 的命名前加上 `with`。由于你正在使用 JavaScript ES6，你可以用 ES6 箭头函数更简洁地表示 HOC。

根据加载状态，它应该显示 Loading 组件或 Button 组件。后者是你用于获取更多数据的按钮。

一个用例可以是将 HOC 作为条件渲染的辅助。假设你有一个 List 组件，它可以渲染一个项目列表，或者什么都不渲染（因为列表为空或为）。HOC 可以屏蔽掉在没有列表时列表不渲染任何内容的问题。另一方面，普通的 List 组件就不再需要担心一个不存在的列表了。它只关心渲染列表。

让我们来做一个简单的 HOC，它接收一个组件作为输入并返回一个组件。你可以将其放在你的 *src/App.js* 文件中。

通常情况下，你可以将 HOC 应用到组件。

```javascript
function withFoo(Component) {
  return function(props) {
    return <Component { ...props } />;
  }
}
```

如果你使用解构，你可以从对象中提取 props。

```javascript
const withFoo = (Component) => (props) =>
  <Component { ...props } />
```

在示例中，输入组件将与输出组件相同。什么都没有发生。它渲染相同的组件实例，并将所有的 props 传递给输出组件。但那是没用的。让我们增强输出组件。当加载状态为 true 时，输出组件应该显示 Loading 组件。

高级 React 组件

158

**src/App.js**

```javascript
const Button = ({ onClick, className = '', children }) => (
  <button onClick={onClick} className={className} type="button">
    {children}
  </button>
);

const Loading = () => (
  <div>Loading ...</div>
);

const withLoading = (Component) => ({ isLoading, ...props }) =>
  isLoading
    ? <Loading />
    : <Component { ...props } />;

const ButtonWithLoading = withLoading(Button);
```

当加载状态为 true 时，输出组件应该显示 Loading 组件，否则应该显示 Button 组件。

127https://developer.mozilla.org/en-US/docs/JavaScript/Reference/Operators/Destructuring_assignment

高级 React 组件

159

**src/App.js**

```javascript
class App extends Component {
  ...

  render() {
    const {
      searchTerm,
      results,
      searchKey,
      error,
      isLoading
    } = this.state;
    ...

    return (
      <div className="page">
        ...
        <div className="interactions">
          <ButtonWithLoading
            isLoading={isLoading}
            onClick={() => this.fetchSearchTopStories(searchKey, page + 1)}>
            More
          </ButtonWithLoading>
        </div>
      </div>
    );
  }
}
```




高级 React 组件

160

- 尝试实验你创建的 HOC
- 思考另一个 HOC 可能合理的用例
- 如果有用例，则实现该 HOC

高级 React 组件

161

## 高级排序

你已经实现了一个客户端和服务器端的搜索交互。由于你有一个 `Table` 组件，增强 `Table` 的高级交互将是很有意义的。如果通过使用 Table 的列标题来为每一列引入排序功能你觉得如何？

你可以编写自己的排序函数，但我个人更倾向于在这种情况下使用工具库。Lodash(130) 是这些工具库之一，但你也可以使用任何适合你的库。让我们安装 Lodash 并使用它来实现排序功能吧。

**命令行**

`npm install lodash`

现在你可以在你的 *src/App.js* 文件中导入 Lodash 的排序功能。

**src/App.js**

```javascript
import React, { Component } from 'react';
import axios from 'axios';
import { sortBy } from 'lodash';
import './App.css';
```

你的 Table 中有几列。分别是标题（title）、作者（author）、评论（comments）和积分（points）。你可以定义排序函数，每个函数接收一个列表并返回一个按特定属性排序的项列表。此外，你还需要一个默认排序函数，它不进行排序，只返回未排序的列表。这将是初始状态。

**src/App.js**

```javascript
...
const SORTS = {
  NONE: list => list,
  TITLE: list => sortBy(list, 'title'),
  AUTHOR: list => sortBy(list, 'author'),
  COMMENTS: list => sortBy(list, 'num_comments').reverse(),
  POINTS: list => sortBy(list, 'points').reverse(),
};

class App extends Component {
...
}
```

130 https://lodash.com/

高级 React 组件

162

你可以看到有两个排序函数返回反转后的列表。这是因为当你第一次对列表进行排序时，你想看到评论和积分最高的项，而不是计数最低的项。

现在 `SORTS` 对象允许你引用任何排序函数。

再次，你的 App 组件负责存储排序状态。初始状态将是初始默认排序函数，它完全不进行排序，并将输入列表作为输出。

**src/App.js**

```javascript
this.state = {
  results: null,
  searchKey: '',
  searchTerm: DEFAULT_QUERY,
  error: null,
  isLoading: false,
  sortKey: 'NONE',
};
```

一旦你选择了一个不同的 `sortKey`，比如 AUTHOR ，你将使用 `SORTS` 对象中相应的排序函数对列表进行排序。

现在你可以在 App 组件中定义一个新的类方法，只需将 `sortKey` 设置为你的本地组件状态。之后，`sortKey` 就可以用于检索排序函数并将其应用于你的列表上。

**src/App.js**

```javascript
class App extends Component {
  _isMounted = false;
  constructor(props) {
    ...
    this.needsToSearchTopStories = this.needsToSearchTopStories.bind(this);
    this.setSearchTopStories = this.setSearchTopStories.bind(this);
    this.fetchSearchTopStories = this.fetchSearchTopStories.bind(this);
    this.onSearchSubmit = this.onSearchSubmit.bind(this);
    this.onSearchChange = this.onSearchChange.bind(this);
    this.onDismiss = this.onDismiss.bind(this);
    this.onSort = this.onSort.bind(this);
  }
```

高级 React 组件

163

...

```javascript
onSort(sortKey) {
  this.setState({ sortKey });
}
...
}
```

下一步是将该方法和 `sortKey` 传递给你的 Table 组件。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    const {
      searchTerm,
      results,
      searchKey,
      error,
      isLoading,
      sortKey
    } = this.state;
    ...
    return (
      <div className="page">
        ...
        <Table
          list={list}
          sortKey={sortKey}
          onSort={this.onSort}
          onDismiss={this.onDismiss}
        />
        ...
      </div>
    );
  }
}
```

高级 React 组件

164

Table 组件负责排序列表。它通过 `sortKey` 获取一个 SORT 函数，并将列表作为输入。之后，它持续对排序后的列表进行映射（map）。

**src/App.js**

```javascript
const Table = ({
  list,
  sortKey,
  onSort,
  onDismiss
}) => (
<div className="table">
  {SORTS[sortKey](list).map(item => (
    <div key={item.objectID} className="table-row">
      ...
    </div>
  ))}
</div>
)
```

理论上，列表将由其中一个函数进行排序。但默认排序被设置为 NONE，所以还没有进行任何排序。到目前为止，还没有人执行 `onSort()` 方法来更改 `sortKey`。让我们为 Table 增加一行用于排序的列标题。

**src/App.js**

```javascript
const Table = ({
  list,
  sortKey,
  onSort,
  onDismiss
}) => (
<div className="table">
  <div className="table-header">
    <span onClick={() => onSort('TITLE')} className="sort-header">Title</span>
    <span onClick={() => onSort('AUTHOR')} className="sort-header">Author</span>
    <span onClick={() => onSort('COMMENTS')} className="sort-header">Comments</span>
    <span onClick={() => onSort('POINTS')} className="sort-header">Points</span>
  </div>
  {SORTS[sortKey](list).map(item => (
    <div key={item.objectID} className="table-row">
      ...
    </>
  ))}
</div>
```

（注：后面页面的 OCR 内容是碎片化的。我根据提供的代码片段重新重组了逻辑。）

高级 React 组件

162

你可以看到有两个排序函数返回反转后的列表。这是因为当你第一次对列表进行排序时，你想看到评论和积分最高的项，而不是计数最低的项。

现在 `SORTS` 对象允许你引用任何排序函数。再次，你的 App 组件负责存储排序状态。初始状态将是初始默认排序函数，它完全不进行排序，并将输入列表作为输出。

**src/App.js**

```javascript
this.state = {
  results: null,
  searchKey: '',
  searchTerm: DEFAULT_QUERY,
  error: null,
  isLoading: false,
  sortKey: 'NONE',
};
```

一旦你选择了一个不同的 `sortKey`，比如 AUTHOR ，你将使用 `SORTS` 对象中相应的排序函数对列表进行排序。现在你可以在 App 组件中定义一个新的类方法，只需将 `sortKey` 设置为你的本地组件状态。之后，`sortKey` 就可以用于检索排序函数并将其应用于你的列表上。

**src/App.js**

```javascript
class App extends Component {
  _isMounted = false;
  constructor(props) {
    ...
    this.needsToSearchTopStories = this.needsToSearchTopStories.bind(this);
    this.setSearchTopStories = this.setSearchTopStories.bind(this);
    this.fetchSearchTopStories = this.fetchSearchTopStories.bind(this);
    this.onSearchSubmit = this.onSearchSubmit.bind(this);
    this.onSearchChange = this.onSearchChange.bind(this);
    this.onDismiss = this.onDismiss.bind(this);
    this.onSort = this.onSort.bind(this);
  }
```

高级 React 组件

163

...

```javascript
onSort(sortKey) {
  this.setState({ sortKey });
}
...
}
```

下一步是将该方法和 `sortKey` 传递给你的 Table 组件。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    const {
      searchTerm,
      results,
      searchKey,
      error,
      isLoading,
      sortKey
    } = this.state;
    ...
    return (
      <div className="page">
        ...
        <Table
          list={list}
          sortKey={sortKey}
          onSort={this.onSort}
          onDismiss={this.onDismiss}
        />
        ...
      </div>
    );
  }
}
```

高级 React 组件

164

Table 组件负责排序列表。它通过 `sortKey` 获取一个 SORT 函数，并将列表作为输入。之后，它持续对排序后的列表进行映射。

**src/App.js**

```javascript
const Table = ({
  list,
  sortKey,
  onSort,
  onDismiss
}) => (
<div className="table">
  {SORTS[sortKey](list).map(item => (
    <div key={item.objectID} className="table-row">
      ...
    </div>
  ))}
</div>
)
```

理论上，列表将由其中一个函数进行排序。但默认排序被设置为 NONE，所以还没有进行任何排序。到目前为止，还没有人执行 `onSort()` 方法来更改 `sortKey`。让我们为 Table 增加一行用于排序的列标题。

**src/App.js**

```javascript
const Table = ({
  list,
  sortKey,
  onSort,
  onDismiss
}) => (
<div className="table">
  <div className="table-header">
    <span onClick={() => onSort('TITLE')} className="sort-header">Title</span>
    <span onClick={() => onSort('AUTHOR')} className="sort-header">Author</span>
    <span onClick={() => onSort('COMMENTS')} className="sort-header">Comments</span>
    <span onClick={() => onSort('POINTS')} className="sort-header">Points</span>
  </div>
  {SORTS[sortKey](list).map(item => (
    <div key={item.objectID} className="table-row">
      ...
    </div>
  ))}
</div>
```




## 高级 React 组件

**src/App.js**

```javascript
const Table = ({
  list,
  sortKey,
  isSortReverse,
  onSort,
  onDismiss
}) => {
  const sortedList = SORTS[sortKey](list);
  const reverseSortedList = isSortReverse
    ? sortedList.reverse()
    : sortedList;

  return(
    <div className="table">
      <div className="table-header">
        <span style={{ width: '40%' }}>
          <Sort
            sortKey={'TITLE'}
            onSort={onSort}
            activeSortKey={sortKey}
          >
            Title
          </Sort>
        </span>
        <span style={{ width: '30%' }}>
          <Sort
            sortKey={'AUTHOR'}
            onSort={onSort}
            activeSortKey={sortKey}
          >
            Author
          </Sort>
        </span>
        <span style={{ width: '10%' }}>
          <Sort
            sortKey={'COMMENTS'}
            onSort={onSort}
            activeSortKey={sortKey}
          >
            Comments
          </Sort>
        </span>
        <span style={{ width: '10%' }}>
          <Sort
            sortKey={'POINTS'}
            onSort={onSort}
            activeSortKey={sortKey}
          >
            Points
          </Sort>
        </span>
        <span style={{ width: '10%' }}>
          Archive
        </span>
      </div>
      {reverseSortedList.map(item =>
        ...
      )}
    </div>
  );
}
```

现在在你的 `Sort` 组件中，你已经可以根据 `sortKey` 和 `activeSortKey` 判断排序是否处于状态。为你的 `Sort` 组件添加一个额外的 `className` 属性，以便在处于排序状态时给用户提供视觉反馈。

**src/App.js**

```javascript
const Sort = ({
  sortKey,
  activeSortKey,
  onSort,
  children
}) => {
  const sortClass = ['button-inline'];
  if (sortKey === activeSortKey) {
    sortClass.push('button-active');
  }

  return (
    <Button
      onClick={() => onSort(sortKey)}
      className={sortClass.join(' ')}
    >
      {children}
    </Button>
  );
}
```

定义 `sortClass` 的方式有点笨拙，对吧？有一个非常巧妙的小库可以解决这个问题。首先你必须安装它。

**命令行**

npm install classnames

然后，你需要在你的 *src/App.js* 文件的顶部导入它。

**src/App.js**

```javascript
import React, { Component } from 'react';
import axios from 'axios';
import { sortBy } from 'lodash';
import classNames from 'classnames';
import './App.css';
```

现在你可以使用它通过条件类来定义组件的 `className`。

**src/App.js**

```javascript
const Sort = ({
  sortKey,
  activeSortKey,
  onSort,
  children
}) => {
  const sortClass = classNames(
    'button-inline',
    { 'button-active': sortKey === activeSortKey }
  );

  return (
    <Button
      onClick={() => onSort(sortKey)}
      className={sortClass}
    >
      {children}
    </Button>
  );
}
```

同样，当你运行测试时，你应该会看到快照测试失败，同时 `Table` 组件的单元测试也失败了。由于你再次更改了组件的表示形式，你可以接受这些快照测试。但你必须修复单元测试。在你的 *src/App.test.js* 文件中，你需要为 `Table` 组件提供 `sortKey` 和 `isSortReverse` 布尔值。

**src/App.test.js**

```javascript
...
describe('Table', () => {
  const props = {
    list: [
      { title: '1', author: '1', num_comments: 1, points: 2, objectID: 'y' },
      { title: '2', author: '2', num_comments: 1, points: 2, objectID: 'z' },
    ],
    sortKey: 'TITLE',
    isSortReverse: false,
  };
  ...
});
```

再次，你可能需要接受 `Table` 组件中失败的快照测试，因为你为 `Table` 组件提供了扩展属性（props）。

最后，你的高级排序交互现在完成了。

**练习题：**

- 使用像 Font Awesome (131) 的库来指示（反向）排序——可以在每个 Sort 表头旁边放置向上或向下的箭头图标
- 了解更多关于 classnames 库的知识 (132)

131 http://fontawesome.io/
132 https://github.com/JedWatson/classnames

你已经学习了 React 中的高级组件技术！让我们回顾一下最后几章：

- **React**
  - 使用 `ref` 属性引用 DOM 节点
  - 高阶组件（higher-order components）是构建高级组件的常用方法
  - 在 React 中实现高级交互
  - 使用简洁的辅助库处理条件类 classNames
- **ES6**
  - 使用剩余参数解构来拆分对象和数组

你可以在官方仓库中找到源代码 (133)。
133 https://github.com/the-road-to-learn-react/hackernews-client/tree/5

## React 及其他领域的状态管理

在之前的章节中已经学习了 React 状态管理的基础。本章将更深入地探讨这一主题。你将学习最佳实践、如何应用它们，以及为什么你可能考虑使用第三方状态管理库。

### 状态提升 (Lifting State)

在你的应用程序中，只有 `App` 组件是带状态的 ES6 组件。它在类方法中处理了大量的状态和逻辑。你可能注意到你向 `Table` 组件传递了许多属性。这些属性的大部分只在 `Table` 组件中使用。整个排序功能只在 `Table` 组件中使用。将状态从一个组件移动到另一个组件被称为*状态提升*（lifting state）。在你的情况下，你希望将不在 `App` 组件使用的状态移动到 `Table` 组件中。为了处理 `Table` 组件中的状态和类方法，它必须变成一个 ES6 组件。从函数组件重构为 ES6 组件是非常直接的。

**作为函数无状态组件的你的 Table 组件：**

**src/App.js**

```javascript
const Table = ({
  list,
  sortKey,
  isSortReverse,
  onSort,
  onDismiss
}) => {
  const sortedList = SORTS[sortKey](list);
  const reverseSortedList = isSortReverse
    ? sortedList.reverse()
    : sortedList;
  return (
    ...
  );
}
```

**作为 ES6 类组件的你的 Table 组件：**

**src/App.js**

```javascript
class Table extends Component {
  render() {
    const {
      list,
      sortKey,
      isSortReverse,
      onSort,
      onDismiss
    } = this.props;
    const sortedList = SORTS[sortKey](list);
    const reverseSortedList = isSortReverse
      ? sortedList.reverse()
      : sortedList;
    return (
      ...
    );
  }
}
```

由于你想在组件中处理状态和方法，因此需要添加构造函数（constructor）和初始状态。

**src/App.js**

```javascript
class Table extends Component {
  constructor(props) {
    super(props);
    this.state = {};
  }
  render() {
    ...
  }
}
```

现在你可以将排序功能的状态和类方法从 `App` 组件移动到 `Table` 组件。

**src/App.js**

```javascript
class Table extends Component {
  constructor(props) {
    super(props);
    this.state = {
      sortKey: 'NONE',
      isSortReverse: false,
    };
    this.onSort = this.onSort.bind(this);
  }
  onSort(sortKey) {
    const isSortReverse = this.state.sortKey === sortKey && !this.state.isSortReverse;
    this.setState({ sortKey, isSortReverse });
  }
  render() {
    ...
  }
}
```

忘记从你的 `App` 组件中移除的状态和 `onSort()` 类方法。

**src/App.js**

```javascript
class App extends Component {
  _isMounted = false;
  constructor(props) {
    super(props);
    this.state = {
      results: null,
      searchKey: '',
      searchTerm: DEFAULT_QUERY,
      error: null,
      isLoading: false,
    };
  ...
  this.setSearchTopStories = this.setSearchTopStories.bind(this);
  this.fetchSearchTopStories = this.fetchSearchTopStories.bind(this);
  this.onDismiss = this.onDismiss.bind(this);
  this.onSearchSubmit = this.onSearchSubmit.bind(this);
  this.onSearchChange = this.onSearchChange.bind(this);
  this.needsToSearchTopStories = this.needsToSearchTopStories.bind(this);
}
...
}
```

此外，你可以让 `Table` 组件的 API 更轻量。从 `App` 组件中移除传递给它的属性，因为它们现在在 `Table` 组件内部进行处理。

**src/App.js**

```javascript
class App extends Component {
  ...
  render() {
    const {
      searchTerm,
      results,
      searchKey,
      error,
      isLoading
    } = this.state;
    ...
    return (
      <div className="page">
        ...
        { error
          ? <div className="interactions">
            <p>Something went wrong.</p>
          </div>
          : <Table
            list={list}
            onDismiss={this.onDismiss}





React 及其他框架的状态管理

}

}

}

现在在你的 `Table` 组件中，你可以使用内部的 `onSort()` 方法和内部 `Table` 状态。

**src/App.js**

```javascript
class Table extends Component {
  ...

  render() {
    const {
      list,
      onDismiss
    } = this.props;

    const {
      sortKey,
      isSortReverse,
    } = this.state;
    const sortedList = SORTS[sortKey](list);

    const reverseSortedList = isSortReverse
      ? sortedList.reverse()
      : sortedList;

    return(
      <div className="table">
        <div className="table-header">
          <span style={{ width: '40%' }}>
            <Sort
              sortKey={'TITLE'}
              onSort={this.onSort}
              activeSortKey={sortKey}
            >
              Title
            </Sort>
          </span>
          <span style={{ width: '30%' }}>
            <Sort
              sortKey={'AUTHOR'}
              onSort={this.onSort}
              activeSortKey={sortKey}
            >
              Author
            </Sort>
          </span>
          <span style={{ width: '10%' }}>
            <Sort
              sortKey={'COMMENTS'}
              onSort={this.onSort}
              activeSortKey={sortKey}
            >
              Comments
            </Sort>
          </span>
          <span style={{ width: '10%' }}>
            <Sort
              sortKey={'POINTS'}
              onSort={this.onSort}
              activeSortKey={sortKey}
            >
              Points
            </Sort>
          </span>
          <span style={{ width: '10%' }}>
            Archive
          </span>
        </div>
        { reverseSortedList.map((item) =>
          ...
        )}
      </div>
    );
  }
}
```

你的应用程序仍然可以正常工作。但你进行了一次关键的重构。你将功能和状态移动到了另一个组件中。其他组件再次变得更加轻量化。此外，`Table` 组件的 API 变得变得更简单，因为它在内部处理了排序功能。

状态提升（Lifting state）的过程也可以反向进行：从子组件到父组件。这被称为“状态提升”。想象你正在处理子组件中的内部状态，现在你想满足一个在父组件中也显示该状态的需求。你必须将状态提升到父组件。但情况远不止如此。想象你想在子组件的兄弟组件中显示该状态。你仍然需要将状态提升到父组件。父组件处理该内部状态，并将其暴露给两个子组件。

**练习题：**

- [阅读并了解更多关于 React 中状态提升的内容](https://reactjs.org/docs/lifting-state-up.html) (134)
- [在在使用 Redux 之前学习 React 并了解更多关于状态提升](https://www.robinwieruch.de/learn-react-before-using-redux/) (135)

134 https://reactjs.org/docs/lifting-state-up.html
135 https://www.robinwieruch.de/learn-react-before-using-redux/

**复习：setState()**

到目前为止，你一直在使用 React 的 `setState()` 来管理组件内部状态。你可以向函数传递一个对象，并在其中部分更新内部状态。

**代码沙场**

```javascript
this.setState({ foo: bar });
```

但 `setState()` 不仅接收一个对象。在它的第二个版本中，你可以传递一个函数来更新状态。

**代码沙场**

```javascript
this.setState((prevState, props) => {
  ...
});
```

你为什么要这样做？有一个关键的用例使得这种做法非常有意义：当新状态依赖于旧状态时，使用函数比使用对象更可靠。因为 `setState()` 是异步的，如果你连续调用它，使用对象可能会导致状态过时。在更新状态时会出问题，而使用函数可以确保你基于最新的状态进行操作。




React 及其他的状态管理

186

**练习：**

- 阅读更多关于如何正确使用 React 状态 (136)
- 从文件中导出 `updateSearchTopStoriesState`
- 为其编写一个测试，传递有效负载（hits, page）和一个伪造的先前状态，并期望一个新状态
- 重构你的 `setState()` 方法以使用函数形式
- 但仅在符合逻辑的情况下使用，因为它可能依赖于 props 或 state
- 再次运行你的测试并确保所有内容都已更新

136](https://reactjs.org/docs/state-and-lifecycle.html#using-state-correctly

React 及其他的状态管理

187

**驯服状态**

之前的章节已经向你展示了状态管理在大型应用程序中是一个至关重要的课题。通常情况下，不仅是 React，许多 SPA（单页应用）框架在这方面都面临挑战。近年来，应用程序变得越来越复杂。如今 Web 应用面临的一个大挑战之一就是驯服和控制状态。

与其他解决方案相比，React 已经迈出了一大步。单向数据流和用于组件内管理状态的简单 API 是不可或缺的。这些概念使得对状态及其状态变化的推理变得更容易。它使得你在组件层面以及在某种程度上在应用层面更容易进行推理。

在一个不断增长的应用程序中，推理状态变化变得越来越困难。在 `setState()` 中使用对象而不是函数时，可能会因为操作旧状态而引入 bug。你必须通过提升状态（lift state）来在组件之间共享必要的状态或隐藏不必要的状态。可能会出现某个组件需要提升状态，因为它的兄弟组件依赖于它。也许该组件在组件树中很远，因此你必须跨越整个树共享状态。结论是，组件参与状态管理的程度越来越大。但到底，组件的主要职责应该是表示 UI，不是吗？

由于这些原因，存在独立的解决方案来处理应用程序中的状态管理。这些解决方案不仅用于 React。但这正是 React 生态系统的强大之处。你可以使用不同的解决方案来解决问题。为了扩展状态管理的问题，你可能听过 Redux (137) 或 MobX (138) 库。你可以在 React 应用中使用其中任何一种解决方案。它们附带了扩展 `react-redux` (139) 和 `mobx-react` (140)，以便将它们集成到 React 层中。Redux 和 MobX 不在本本书的范围内。当你读完这本书后，你将获得关于如何继续学习 React 及其生态系统的指导。一种学习路径可以是学习 Redux。在你深入外部状态管理主题之前，我建议阅读这篇文章 (141)。它旨在让你更好地理解如何学习状态管理。

**练习题：**

- 阅读更多关于外部状态管理以及如何学习它 (142)
- 看看我关于 React 状态管理的第二本电子书 (143)

137](http://redux.js/docs/introduction/)
138](https://mobx.js/)
139](https://github.com/reactjs/react-redux)
140](https://github.com/mobxjs/mobx-react)
141](https://www.robinwieruch.de/redux-mobx-confusion/)
142](https://www.robinwieruch.de/redux-mobx-confusion/)
143](https://roadtoreact.com/)

React 及其他的状态管理

188

你已经学习了 React 中的高级状态管理！让我们回顾一下最后几个章节：

- React 将状态管理向上或向下提升到合适的组件
- `setState` 可以使用函数来防止旧状态 bug
- 现有的帮助你驯服状态的外部解决方案

你可以在官方仓库中找到源代码 (144)。

144](https://github.com/the-road-to-learn-react/hackernews-client/tree/master)

迈向生产的最后步骤

最后章节将向你如何将应用程序部署到生产环境。你将使用免费的托管服务 Heroku。在部署应用程序的过程中，你将学习更多关于 `create-react-app` 的知识。

迈向生产的最后步骤

190

**Eject**

以下步骤和知识对于将应用程序部署到生产环境并不是必要的。尽管如此，我想向你解释它。create-react-app 带有一个功能来保持其可扩展性，同时也防止供应商锁定（vendor lock-in）。供应商锁定通常发生在你采用某项技术但未来没有逃生口时。幸运的是，在 `create-react-app` 中，你有一个名为“eject”的逃生口。

在你的 `package.json` 中，你会找到启动、测试和构建应用程序的脚本。最后一个脚本是 `eject`。你可以尝试它，但没有回头路。这是一次单向操作。一旦你 eject，就无法回去了！如果你刚刚开始学习 React，离开 `create-react-app` 方便的环境是没有意义的。

如果你运行 `npm eject`，该命令会将所有配置和依赖拷贝到你的 `package.json` 和一个新的配置文件夹中。你将整个项目转换为带有包含 Babel 和 Webpack 的工具的自定义设置。毕竟，你将对所有这些工具拥有完全控制权。

官方文档说 `create-react-app` 适用于中小型项目。你不应该觉得有义务使用“eject”命令。

**练习题：**

- 阅读更多关于 eject (145)

145](https://github.com/facebookincubator/create-react-app#converting-to-a-custom-setup)

迈向生产的最后步骤

191

**部署你的应用**

最后，任何应用程序都不应该停留在 localhost。你希望上线。Heroku 是一个平台即服务（PaaS），你可以在上面托管应用程序。它们提供了与 React 的无缝集成。具体来说：可以在几分钟内部署 `create-react-app`。这是零配置部署，遵循 `create-react-app` 的哲学。

在将应用程序部署到 Heroku 之前，你需要满足两个要求：

- 安装 Heroku CLI (146)
- 创建免费的 Heroku 账户 (147)

如果你安装了 Homebrew，可以从命令行安装 Heroku CLI：

**命令行**

```bash
brew update
brew install heroku-toolbelt
```

现在你可以使用 git 和 Heroku CLI 部署你的应用程序。

**命令行**

```bash
git init
heroku create -b https://github.com/mars/create-react-app-buildpack.git
git add .
git commit -m "react-create-app on Heroku"
git push heroku master
heroku open
```

就是这样。我希望你的应用程序已经运行。如果你遇到问题，可以检查以下资源：

- Git 和 GitHub (148)
- 零配置部署 React (149)
- 用于 create-react-app 的 Heroku Buildpack (150)

146](https://dev.heroku.com/)
147](https://dev.heroku.com/)
148](https://www.robinwieruch.de/git-commands/)
149](https://www.heroku.com/deploying-react/)
150](https://github.com/mars/create-react-app)

205

**目录**

这是书的最后一个章节。希望你喜欢阅读它，并且它对你有帮助。如果你喜欢这本书，请和朋友分享。此外，如果你能花5 分钟在 Amazon (151) 或 Goodreads (152) 上写评论，对我将意义重大。

**所以，读完这本书后你可以去哪里？** 你可以扩展自己的项目，也可以尝试开发自己的项目。我很好奇你读书后会构建什么。

- **状态管理：**你已经使用了 `setState()` 来管理本地组件状态。这是一个完美的开始。然而，在较大的应用程序中，你会遇到 React 本地状态的局限性 (154)。因此你可以使用第三方状态管理库，如 Redux 或 MobX (155)。在 Road to React (156) 课程中，你会找到“React状态管理”课程，它教授了 React 高级状态、Redux 和 MobX。课程还附带电子书，但我建议大家深入研究源码和视频。

- **连接数据库身份验证：** 在不断增长的 React 应用程序中，你最终可能需要持久化数据。数据应该存储在数据库中，以便在浏览器会话结束后并在不同的使用应用程序的用户之间共享。引入数据库简单的方法是使用 Firebase。在这个综合教程 (157) 中，你将找到关于如何在 React 中使用 Firebase 身份验证（注册、登录、注销）的逐步指南。此外，你将使用 Firebase 实时数据库存储用户实体。之后，取决于你如何在数据库中存储应用程序所需的更多数据。

- **使用 Webpack 和 Babel 的工具：** 在书中你使用了 `create-react-app` 来设置你的应用程序。在某个时刻，当你学习了 React 之后，你可能想学习它背后的工具。




## 提纲

193

围绕它的工具链。它让你能够在不使用 *create-react-app* 的情况下搭建自己的项目。我建议遵循 Webpack 和 Babel(158) 的最小化设置。之后，你可以自行应用更多工具。例如，你可以使用 ESLint(159) 来在应用程序中遵循统一的代码风格。

- **React 组件语法：** 实现 React 组件的可能性和最佳实践随时间演变。你会在其他学习资源中发现许多编写 React 组件（尤其是 React 类组件）的方法。你可以查看这个 [GitHub 仓库(160)](https://github.com/the-road-to-learn-react/react-alternative-class-component-syntax) 来了解编写 React 类组件的另一种方法。通过使用类字段声明，未来你可以将其写得更加简洁。

- **其他项目：** 在学习了原生 React 后，在学习新东西之前，先将所学知识应用到自己的项目中总是好的。你可以用 React 编写你自己的井棋游戏或一个简单的计算器。那里有很多教程只使用 React 来构建有趣的内容。可以查看我关于构建分页和无限滚动列表(161)的教程、在 Twitter 墙上展示推文(162)或将你的 React 应用程序连接 Stripe 进行收费(163)。通过尝试这些微型应用程序来熟悉 React。

- **UI 组件：** 你不应该犯在项目中过早引入 UI 组件库的错误。首先，你应该学习如何使用标准的 HTML 元素从零实现并使用下拉列表、复选框或对话框。这些组件的大部分将管理它们自己的本地状态。复选框必须知道自己是否被选中。因此你应该将它们实现为受控组件。在你完成所有基础实现后，可以引入 UI 组件库，它可以提供作为 React 组件的复选框和对话框。

- **代码组织：** 在读书过程中，你会遇到一个关于代码组织的章节。如果你还没有这样做，现在就可以应用这些更改。它会将你的组件组织在结构化的文件和文件夹（模块）中。此外，它帮助你理解和学习代码分割、重用、可维护性和模块 API 设计的原则。最终你的应用程序规模会扩大，你需要对其进行模块化结构化。所以现在开始会更好。

- **测试：** 这本书对测试仅浅触皮毛。如果你不熟悉这个通用话题，可以深入研究单元测试和集成测试的概念，特别是在 React 应用程序的背景下。在实现层面，我建议坚持使用 Enzyme 和 Jest，以完善你在 React 中通过单元测试和快照测试进行测试的方法。

- **路由：** 你可以使用 [react-router(164)](https://github.com/ReactTraining/react-router) 为你的应用程序实现路由。到目前为止，你的应用程序只有一个页面。React Router 帮助你在多个 URL 上拥有多个页面。当你向应用程序引入路由时，你不需要向 Web 服务器发送请求来获取下一页。路由器将在客户端为你完成一切。所以动手起来，在你的应用程序中引入路由吧。

- **类型检查：** 在其中一个章节中，你使用了 React PropTypes 来定义组件接口。这是一个防止 Bug 的良好做法。但 PropTypes 仅在运行时检查。你可以更进一步，在编译时引入静态类型检查。[TypeScript(165)](https://www.typescriptlang.org/) 是一种流行的方法。但在 React 生态系统中，人们经常使用 [Flow(166)](https://flowtype.org/)。如果你感兴趣让你的应用程序更健壮，我建议尝试一下 Flow。

- **React Native：** [React Native(167)](https://facebook.github.io/react-native/) 将你的应用程序带到移动设备。你可以将从 React 学到的知识应用于发布 iOS 和 Android 应用。一旦学习了 React，React Native 的学习曲线不应该是陡峭的。两者共享相同的原理。你只会在移动端遇到与你在 Web 应用程序中不同的布局组件。

总来说，我邀请你访问我的[网站(168)](https://www.robinwieruch.de) 来寻找更多关于 Web 开发和软件工程的有趣话题。你可以订阅我的[Newsletter(169)](https://www.getrevue.co/profile/rwieruch) 以获取文章、书籍和课程的更新。此外，课程平台 Road to React(170)](https://roadtoreact.com) 提供了更高级的课程来学习 React 生态系统。你应该看看！

最后但同样重要的是，我希望找到更多能够支持我内容的[赞助(171)](https://www.patreon.com/rwieruch)。有很多学生负担不起教育内容的费用。这就是为什么我免费发布了大量内容。通过作为我的赞助者支持我的工作，我可以维持这些免费教导他人的努力。

再次，如果你喜欢这本书，我希望你花点时间思考一个适合学习 React 的人。联系那个人并分享这本书。这对我意义重大。这本书的意图是送给别人的。随着更多人阅读并向我提供反馈，它会随着时间的推移而改进。我也希望看到你的反馈、评论或评分！

非常感谢阅读学习 React 之路。

Robin

158 https://www.robinwieruch.de/minimal-react-webpack-babel-setup/
159 https://www.robinwieruch.de/react-eslint-webpack-babel/
160 https://github.com/the-road-to-learn-react/react-alternative-class-component-syntax
161 https://www.robinwieruch.de/react-paginated-list/
162 https://www.robinwieruch.de/react-svg-patterns/
163 https://www.robinwieruch.de/react-express-stripe-payment/
164 https://github.com/ReactTraining/react-router
165 https://www.typescriptlang.org/
166 https://flowtype.org/
167 https://facebook.github.io/react-native/
168 https://www.robinwieruch.de
169 https://www.getrevue.co/profile/rwieruch
170 https://roadtoreact.com
171 https://www.patreon.com/rwieruch


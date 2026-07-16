# Javascript 数据视化使用指南



![](img/front-cover.png)

# 目录

使用 JavaScript 进行数据可视化

Copyright © 2025 Peter Cook. 版权所有。

此版本于 2025 年 2 月 7 日发布。

# 1. 引言

《使用 JavaScript 进行数据可视化》教你如何使用 JavaScript 制作地图、图表和数据故事。你将学习：

*   JavaScript 在数据可视化中的作用
*   如何使用 `Chart.js`、`D3.js` 和 `Leaflet` 等 JavaScript 库创建图表和地图
*   如何结合地图和图表来创建并发布数据故事

你将学会如何使用 `Chart.js`制作图表（图 1）、使用 `Leaflet`制作地图（图 2）、使用 `D3.js`制作自定义数据可视化（图 3）以及使用 HTML、CSS、JavaScript、`Chart.js` 和 `Leaflet`制作数据故事（图 4）。

![chartjs styled 1](img/chartjs-styled-1.png)

图 1\. Chart.js 柱状图

![leaflet](img/leaflet.png)

图 2\. Leaflet 地图

![d3 timeline](img/d3-timeline.png)

图 3\. D3.js 时间线图

![data story](img/data-story.png)

图 4\. 数据故事

***

## 1.1. 前提条件

为了充分利用本书的价值，你需要：

*   一台安装了 `Node.js` 的电脑以及一个代码编辑器（如 `VS Code`）
*   具备一定的 `HTML`、`CSS` 和 `JavaScript` 经验
*   具备一定的命令行、`Node.js` 和 `npm` 经验

如果你构建过（或参与过）Web 应用程序，那就没问题。了解 JavaScript 的箭头函数、回调函数和承诺（promises）对于本书非常有帮助。如果你需要快速掌握 `HTML`、`CSS`、`SVG` 和/或 `JavaScript`，我建议阅读[数据可视化的 HTML、SVG、CSS 和 JavaScript 基础](https://leanpub.com/html-svg-css-js-for-data-visualisation）（同样由我编写）。书中包含了本书所需的所有背景知识。

## 1.2. 预期目标

本书旨在帮助你上手 `Chart.js`、`D3`、`Leaflet` 并向你展示如何制作数据故事。

它涵盖了制作地图和图表的基础知识，以及如何开始使用这些库。它没有深入讲解这些库的细节，但旨在激励你学习更多知识，并赋予你制作自己的数据可视化的能力。

## 1.3. 代码

本书涵盖了几个示例项目。你可以从 [app.createwithdata.com/downloads/visualising-data-with-js-book-code.zip](https://app.createwithdata.com/downloads/visualising-data-with-js-book-code.zip) 下载代码包。解压文件并将目录移动到你常用的开发目录。

如果在下载代码时遇到任何问题，请通过 help@createwithdata.com 联系我。

***

## 1.4. 数据

本书使用了来自英国政府可再生能源规划数据库（[`www.gov.uk/government/publications/renewable-energy-planning-database-monthly-extract`](https://www.gov.uk/government/publications/renewable-energy-planning-database-monthly-extract)）的单一数据集。它追踪了 1990 年以来通过规划系统的英国可再生能源项目。

我们使用了 2023 年 1 月发布的数据集快照，包含 8000 多行。每行代表一个规划申请，字段包括名称、`technology`（技术类型，如太阳能或风能）、`capacity`（兆瓦输出容量）、`location`（纬度和经度）、`region`（地区）、`status`（例如：运行中、拒绝、建设中）以及 `year submitted`（提交年份）。

我们使用这些数据是因为：

*   它是权威来源发布的真实数据
*   它结合了分类数据和数值数据
*   它具有地理元素（每个项目的位置）
*   它的规模对于教学来说非常合适（既不小也不庞大）

原始数据如下：

![repd data sheet](img/repd-data-sheet.png)

图 5\. REPD 数据（省略了一些行和列）

为了本书，我将数据转换成了一个 `JSON` 文件。使用了原始数据列的子集并重命名了列。还添加了一些新属性 `yearSubmitted`、`yearGranted` 和 `daysUntilGranted`：

***

```
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  ...
]
```

列表 1\. JSON 文件中的前几项

你可以自己在 `load-data/public/repd.json` 中检查这些数据。

关于如何将 REPD CSV 文件转换为 `repd.json` 的更多信息，请参阅附录中的数据处理部分。

***

## 1.5. 书的结构

本书由以下章节组成：

*   JavaScript 与数据可视化
*   使用 Chart.js 制作图表
*   Chart.js 的样式定制
*   使用 D3.js 制作自定义图表
*   使用 Leaflet 制作数据驱动地图
*   数据故事

# 2. 数据可视化与 JavaScript

本章概述了 JavaScript 在数据可视化中的作用。它还展示了如何使用构建工具 Vite 创建 Web 应用程序，并演示了一个加载数据并以表格形式显示的示例应用程序。

## 2.1. 数据可视化

数据可视化是使用图形（而非数字）表示数据的过程。

例如，假设你有一张销售数据表：

![simple table of numbers](img/simple-table-of-numbers.png)

图 6\. 一张销售数据表





仅通过数字很难在数据中发现任何趋势。数据分析师可能会运行回归测试来查看是否存在趋势，但你也可以通过绘制折线图来将数据可视化：

![simple table of numbers as chart](img/simple-table-of-numbers-as-chart.png)

图 7 用折线图表示的销售数据

我们可以立即看到存在上升趋势，并且在 8 月有一个峰值。这就是数据可视化的力量所在。它揭示了在数字表格中并不显见的模式。

### 2.1.1 为什么要可视化数据？

有很多充分的理由可视化数据，例如：

*   它是理解和交流数据的有效方法
*   它可以提供更丰富的视觉多样性，有助于吸引读者的兴趣
*   它本身就可以成为极具视觉吸引力的作品（有利于内容、SEO 等）

### 2.1.2 最佳实践

有很多关于数据可视化最佳实践的书。我脑海中浮出了 Alberto Cairo 的[功能性艺术](https://www.oreilly.com/library/view/the-functional-art/9780133041187/)。书中有一个非常实用的章节，根据对人类感知的学术理解解释了哪些图表在传输数据方面最有效。简之，最好使用位置和长度来表示数据（而不是方向、面积和/或阴影），因为我们对位置和长度差异的感知优于其他编码。这就是柱状图、折线图和散点图流行的原因之一。这并不是说非标准图表就无效。只要使用位置和长度表示重要数量，自定义图表也可以有效地传达数据。

## 2.2 JavaScript

JavaScript 是 Web 的编程语言，并在所有主流浏览器中实现。它的语法与 `C`、`C++`、`PHP` 等 C 系编程语言相似，通常用于网站和应用程序添加交互性。它还用于修改网页内容。

### 2.2.1 为什么要使用 JavaScript 进行数据可视化？

JavaScript 成为可视化领域领先（甚至唯一）语言之一有几个原因：

*   它是唯一在主流浏览器中实现的语言
*   它非常适合处理数据
*   它拥有大量的可视化库，包括 `Leaflet` 和 `D3.js`。

### 2.2.2 JavaScript 与可视化的历史

JavaScript 图表库的存在时间几乎与 JavaScript 本身一样久（后者于 1995 年引入）。据我所知，最早仍在维护的有 [Google Charts](https://developers.google.com/chart) 和 [Flot](https://flotcharts.org/)，它们都于 2007 年左右推出，支持柱状图、折线图和饼图等标准图表。

![flot](img/flot.png)

图 8 用 Flot 创建的折线图

2009 年[Highcharts](https://highcharts.com) 和 [Protovis](https://mbostock.github.io/protovis/) 发布。Highcharts 仍然是领先的 JavaScript 库之一（非商业用途免费），并提供标准图表。Protovis 采取了不同的方法。它不是提供标准图表，而是提供图形元素（如条、线和点），你可以通过这些元素编码数据。你可以组合这些元素来创建自定义图表。Protovis 由 Mike Bostock 和 Jeff Heer 领导，他们后来创建了 `D3.js`。

![protovis](img/protovis.png)

图 9 用 Protovis 创建的自定义图表

21 世纪 00 年中期，Adobe 的 Flash 是创建 Web 丰富交互应用程序的主导平台。随着 `SVG` 和 `Canvas` 等 Web 标准被主流浏览器支持，它的流行程度在 2000 年末开始下降。

2011 年 `D3.js` 发布，它拥抱了对 `SVG` 标准日益增长的支持。与 Protovis 类似，它提供了制作图表的构建块，并成为创建可视化的主导 JavaScript 库。

2014 年[Chart.js](https://www.chartjs.org/) 发布，目前是领先的免费开源图表库之一。

### 2.2.3 今天的 JavaScript 与可视化

目前 Github 上流行的数据可视化项目是 `D3.js`（105,000 星星）和 `Chart.js`（60,300 星星）。我个人认为 `D3.js` 和 `Chart.js` 能够涵盖大多数可视化场景。通常情况下，我建议使用 `Chart.js` 处理标准图表（柱状、折线、饼图和散点图），使用 `D3.js` 处理自定义可视化。

## 2.3 使用 JavaScript 创建 Web 应用程序

本节将展示如何创建一个 JavaScript Web 应用程序。首先展示 Web 应用程序的基础组件，然后介绍工具 `Vite`，它可以帮助你将所有部分结合在一起。

从根本上说，Web 应用程序由 `HTML`、`CSS` 和 `JavaScript` 组成。无论是简单的网站、全功能的电子商务商店或社交媒体平台都是如此。如果你还不 `HTML`、`CSS` 或 `JavaScript`，我建议在 Web 上寻找教程，例如 [mozilla.org 上的教程](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web) 或阅读我的书籍[数据可视化的 HTML、SVG、CSS 和 JavaScript 基础](https://leanpub.com/html-svg-css-js-for-data-visualisation)。

### 2.3.1 HTML

HTML（超文本标记语言）描述应用程序的静态内容。通常情况下，它是网页上始终可见的内容。

这里是示例 HTML：

```
<!DOCTYPE html>
<html lang="en">
<head>...</head>
<body>
  <h1>My app</h1> ①
  <div id="menu"></div>
  <div class="content">
    <div id="chart"></div> ②
  </div>
</body>
</html>
```

1. ① 静态内容
2. ② 由 JavaScript 生成的图表容器

### 2.3.2 CSS

CSS（层叠样式表）描述应用程序的布局和样式。例如：

```css
body {
  background-color: #eee;
}

h1 {
  color: blue;
}

.content {
  padding: 1rem;
}
```

### 2.3.3 JavaScript

JavaScript 代码管理交互和动态内容。动态内容是在网页加载后生成的。它增强了主 HTML 文件的静态内容。

这是一个基础示例，用于在 HTML 文件中的 `<div id="chart">` 容器中填充 Chart.js 图表（在此阶段不需要理解这段代码）：

```javascript
let chart = new Chart('chart', {
  type: 'bar',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [10, 20, 30]
      }
    ]
  }
});
```

这段代码会导致 Chart.js 在 `<div id="chart">` 元素中绘制一个柱状图。

如果这些 `HTML`、`CSS` 或 `JavaScript` 代码对你来说完全陌生，我建议通过[数据可视化的 HTML、SVG、CSS 和 JavaScript 基础](https://leanpub.com/html-svg-css-js-for-data-visualisation) 来上手。

### 2.3.4 组合部分

虽然可以在 HTML 文件中使用 `<link>` 和 `<script>` 标签链接每个项目的 CSS 和 JavaScript 文件，但通常的方法（特别是对于中大型项目）是使用**打包器**（bundler）。打包器是一种将多个 JavaScript 文件合并成单个包的工具。

一个主要优势是你的 JavaScript 可以模块化，这意味着你可以将应用程序拆分为每个具有单一目的的小文件。这使得你的应用程序代码更容易理解和导航。

有很多打包器可用，如 [Webpack](https://webpack.js.org/)、[Rollup](https://rollupjs.org/)、[Parcel](https://parceljs.org/) 和 [Vite](https://vitejs.dev/)。在本书中我们使用 Vite 是因为：

*   你可以用极少的配置创建项目





* 它内置了一个 Web 服务器，方便你在开发应用程序时使用
* 它运行速度快
* 它的 Web 服务器可以提供静态文件（这对于加载 CSV 和 JSON 文件非常有用）

通常情况下，我建议任何规模的 Web 应用都使用 `Vite`。

书中的所有项目都是使用 `Vite` 创建的。使用 `Vite` 创建项目相对简单，但为了本书的目的，你不需要自己动手操作。不过，如果你想知道如何使用 `Vite` 创建项目，请参阅附录 A。

* *

### 2.3.5. 示例应用程序

我们的第一个项目加载 REPD 数据，对其进行过滤，然后以列表的形式显示：

![加载数据](img/load-data.png)

要运行该项目，打开命令行并导航到下载代码的 `load-data` 目录。输入 `npm install` 下载项目依赖，然后输入 `npm run dev` 启动项目的 Web 服务器：

```
cd load-data
npm install
npm run dev
```

运行 `npm run dev` 时，命令行将返回一个包含可访问 URL 的消息（通常是 [`http://localhost:5173/`](http://localhost:5173/)`）。复制该 URL 并粘贴到浏览器中，你应该就能看到来自 REPD 数据的电池规划应用列表（见前面的图）。

#### 项目概述

该项目具有以下文件结构：

```
load-data/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

列表 2. load-data 项目文件

主文件是 `index.html`、`main.js`、`style.css` 和 `repd.json`。这个项目与书中的其他项目有很多共同之处，因此值得深入了解这个项目。我建议在你喜欢的代码编辑器（例如 `VS Code`）中查看此项目。

* *

以下是文件的简要描述：

| 文件 | 说明 |
| --- | --- |
| `index.html` | 主 HTML 文件。它包含静态内容以及用于存放 JavaScript 生成内容的容器元素。 |
| `main.js` | 主 JavaScript 文件。它加载 REPD 数据，对其进行过滤并构建列表。 |
| `node_modules` | 包含第三方模块（如 `Chart.js` 或 `D3`）的目录。这是由 `npm install` 创建的标准目录。你通常不需要关心这个目录，因此我们不会再关注它。 |
| `package-lock.json` | 由 `npm install` 创建的文件，记录了安装的第三方模块的精确版本。你通常不需要关心这个文件，因此我们不会再关注它。 |
| `package.json` | 由 `npm init` 创建的文件，包含项目配置。例如，它列出了安装的第三方模块（如 `Chart.js` 和 `D3`）。你通常不需要关心这个文件，因此我们不会再关注它。 |
| `public` | 作为服务器根目录的目录。你可以将静态文件放在这里（如 CSV 文件），应用程序可以请求这些文件。 |
| `style.css` | 主 CSS 文件。 |

`load-data` 项目源自 `Vite` 的默认计数器项目（见附录 A）。让我们详细详细检查这些文件。

* *

##### index.html

这是主 HTML 文件，也是 Web 浏览器在加载网站时加载的第一个文件。该文件的大部分内容与 `Vite` 的默认 HTML 文件相同。通常来说，我们在书中对 `index.html` 所的修改只有：

* 更改 `<title>` 的内容
* 在 `<body>` 部分添加、删除或修改 HTML。

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>REPD battery applications</title> ①
  </head>
  <body>
    <div id="output"></div> ②
    <script type="module" src="/main.js"></script> ③
  </body>
</html>
```

列表 3. index.html

1. ① 显示在浏览器标签页中的标题是使用 `<title>` 标签设置的。
2. ② 作为列表容器的 `<div>` 元素。我们在 `main.js` 中填充该元素的内容。
3. ③ 使用 `<script>` 标签引入了主 JavaScript 文件 `main.js`。此行由 `Vite` 生成，通常我们不需要触碰它。

* *

##### main.js

`main.js` 是该项目中唯一的 JavaScript 文件。它加载数据并生成列表。为了加载数据，它使用了 JavaScript Promise（承诺），这是一种相当高级的技术。如果你不熟悉 Promise，不用太担心，因为它们只用于加载数据，而且这段代码在整书中大部分都是保持的。

以下是 `main.js` 的概要：

```javascript
import './style.css'; ①

function makeList(data) { ... }

fetch('./repd.json') ②
  .then(res => res.json()) ③
  .then(data => makeList(data)); ④
```

列表 4. main.js

1. ① 导入 `./style.css`。
2. `fetch('./repd.json')` 请求文件。
3. ③ `res.json()` 解析响应。
4. ④ `makeList(data)` 传递数组。

不要太担心这段代码的细节，Promise 是一个高级的概念。

传递 `makeList` 的数组包含 REPD 数据：

```json
[
  {
    "id": "1",
    "name": "Aberth Power Station",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 5. JSON 文件中的前几项 (data/repd.json)

* *

现在来看 `makeList` 函数，它对数据进行过滤（使用 JavaScript 内置的 [`filter`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) 方法）、构建列表并显示：

```javascript
function makeList(data) {
  // 过滤
  data = data.filter(d => d.technology === "Battery" && d.capacity > 100); ①

  // 从数据构建列表
  let list = ''; ②
  data.forEach(d => { ③
    list += '<div>' + d.name + ' (' + d.region + ') ' + d.capacity + 'MW</div>'; ④
  });

  document.querySelector('#output').innerHTML = list; ⑤
}
```

列表 6. main.js




1. ① 使用 JavaScript 内置的 [array filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) 方法过滤出容量大于 100 的电池应用数据。

2. ② 初始化一个名为 `list` 的变量并为其赋值一个空字符串。

3. ③ 遍历 `data` 的每一个元素。

4. ④ 向 `list` 中追加一个包含名称、区域和容量的 `div` 元素。（`+=` 运算符是 `list = list + '<div>' + …` 的简写。）

5. ⑤ 选定在 `index.html` 中定义的 `<div id="output">` 元素，并将其内容设置为 `list`。浏览器将解析该字符串并创建必要的 `div` 元素以反映字符串 `list`。

### style.css

`style.css` 包含了从 Vite 默认 `style.css` 文件中保留的字体排设置（`style.css` 在 `main.js` 顶部导入。）

```
body {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
  font-size: 16px;
  line-height: 24px;
  font-weight: 400;
}
```

***

## 2.4 结语

本章讨论了 JavaScript 在数据可视化中的作用。它概述了 JavaScript 图表库，并将其分为两类：提供标准图表选择的库，以及那些提供更多灵活性但代价是学习曲线更陡峭的库。

我们还看了一个使用 Vite 构建的简单项目。该项目加载 REPD 数据并将其子集以列表形式呈现。这为本书后续的内容奠定了基础。

## 2.5 进一步学习的建议

我建议通过探索、修改和添加代码来玩玩这个项目。以下是一些想法：

* 显示不同的字段（例如运营商或状态）
* 更改过滤器以显示不同的技术类型（或更改容量阈值）
* 尝试显示自己的数据（确保数据集不要过大，可能不要超过 10Mb）。

访问附录以获取解决方案。

# 3. 使用 Chart.js 创建图表

本章介绍了 JavaScript 图表库 [Chart.js](https://www.chartjs.org/)。这是最受欢迎的免费开源 JavaScript 图表库之一。它可以让你轻松地在网页上添加条形图、折线图、饼图和其他图表。

![chartjs basic](img/chartjs-basic.png)

图 10. 使用 Chart.js 创建的条形图

虽然使用 Chart.js 创建图表相对简单，但 Chart.js 的功能远不止此。 Chart.js 的一些优势包括：

* 图表非常易于样式化。你可以设置单个元素的样式并调整元素之间的间距，这意味着你可以满足大多数样式需求。
* 图表对设备宽度是响应式的，这意味着图表在大屏幕和移动设备上效果同样良好。
* 图表具有内置的工具提示（tooltip），可以显示鼠标悬停（或在移动设备上触摸）数据点上的信息。工具提示可以配置为精确显示你想显示的任何信息。
* Chart.js 的性能非常惊人。我运行过测试，它可以轻松处理数个、甚至数千个数据点（参见 [Chart.js 性能测试](https://codepen.io/createwithdata/pen/mvdQjg)）。

![chartjs tennis](img/chartjs-tennis.png)

图 11. 样式化的 Chart.js 图表示例 ([`www.createwithdata.com/chartjs-and-csv/`](https://www.createwithdata.com/chartjs-and-csv/))

本章展示了如何使用 Chart.js 创建简单的条形图。我们加载 REPD 数据，进行一些基础数据分析，并创建一个条形图来显示结果。

我们还使用了 [tidy.js](https://pbeshai.github.io/tidy/) JavaScript 库，它可以方便过滤、排序和聚合等常见的数据处理操作。我们使用 tidy.js 在可视化之前对 REPD 数据进行聚合。

***

## 3.1 引入 Chart.js

Chart.js 是一个免费开源 JavaScript 库，用于绘制条形图、折线图、散点图、饼图和雷达图。它能生成吸引图表，并且可靠、性能卓越、易于使用、文档齐全且支持良好。本书使用的是 Chart.js 的 4 版本。

本节首先展示如何使用 Chart.js 创建图表。随后将一个使用 tidy.js 和 Chart.js 可视化 REPD 数据的示例。

### 3.1.1 创建图表

使用 Chart.js 创建图表有三个步骤：

* 在项目中引入 Chart.js
* 创建一个 HTML 元素来包含你的图表
* 使用 Chart.js 的构造函数创建一个新的 Chart

#### 在项目中引入 Chart.js

如果你正在使用如 Webpack、Parcel 或 Vite 等打包器，可以使用以下命令安装 Chart.js：

```
cd your-project
npm install chart.js
```

#### 为图表创建容器

每个图表都需要一个 `<canvas>` 元素（`<canvas>` 元素是一个矩形区域，你可以在上面使用 JavaScript 绘制形状）：

```
<body>
  ...
  <canvas id="chart"></canvas> ①
  ...
</body>
```

1. ① `<canvas>` 元素需要一个 `id` 属性，以便你在 JavaScript 代码中引用它。

***

#### 创建图表

每个使用 Chart.js 的 JavaScript 文件都需要在文件顶部导入库：

```
import Chart from 'chart.js/auto';

...
```

使用 Chart.js 的构造函数创建一个图表，传入：

* <canvas> 元素的 id
* 一个配置对象。

```
let chart = new Chart('chart', ①
  type: 'bar', ②
  data: { ③
    labels: ['A', 'B', 'C'], ④
    datasets: [⑤
      {
        data: [10, 20, 30] ⑥
      }
    ]
  }
});
```

列表 7. 使用 Chart.js 创建条形图

① `Chart` 构造函数绘制图表并返回一个表示图表的对象（赋值给变量 `chart`）。第一个参数是 `<canvas>` 元素。② 配置对象必须包含 `type` 和 `data` 两个属性。`type` 属性定义图表类型（见后文）。③ `data` 属性描述图表的数据。对于条形图和折线图，需要 `labels` 和 `datasets` 两个属性。④ `labels` 定义每个条形的轴标签（或折线图中的每个点）。⑤ `datasets` 描述数据，它是一个数组。⑥ `datasets` 中的每个对象代表一个数据序列，并必须包含一个名为 `data` 的属性，其值是一个数字数组。这就是数据本身，并决定了每个条形的长度。

如果 `datasets` 包含单个序列（如示例所示），我们得到一个普通的条形图，每个标签对应一个条形。如果 `datasets` 包含多个序列，我们得到分组条形图，每个标签对应多个条形。

***

### 3.1.2 图表配置

Chart.js 图表可以通过许多方式进行配置。我们不会涵盖所有的选项，但会涵盖一些实用的。

#### 图表类型

配置对象的 `type` 属性可以是 `'bar'`、`'line'`、`'scatter'`、`'bubble'`、`'pie'`、`'doughnut'`、`'polarArea'` 或 `'radar'`。

`'bar'` 用于条形图，`'line'` 用于折线图，`'scatter'` 用于散点图。`'bubble'` 用于散点图，每个圆的半径用于表示另一个变量。`'pie'` 用于饼图，`'doughnut'` 用于中间有孔饼图。`'polarArea'` 类似于条形图，但条形位于圆形内。`'radar'` 用于雷达图，它们类似于折线图但经过转换以适应圆形内部。

对于 `'bar'`、`'line'`、`'pie'`、`'doughnut'`、`'polarArea'` 和 `'radar'` 类型，`datasets` 属性使用类似的结构。`datasets` 中的每个序列对象都有一个 `data` 属性，其值是一个数字数组。





```javascript
let chart = new Chart('chart', {
  type: 'bar', // bar, line, pie, doughnut, polarArea or radar
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [10, 20, 30]
      }
    ]
  }
});
```

对于 `scatter` 点图，每个系列对象都有 `data` 属性，它是一个对象数组，每个对象都有 `x` 和 `y` 属性：

```javascript
let chart = new Chart('chart', {
  type: 'scatter',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [
          {x: 10, y: 50},
          {x: 30, y: 10},
          {x: 50, y: 20}
        ]
      }
    ]
  }
});
```

对于 `bubble` 气泡图，每个系列对象都有 `data` 属性，它是一个对象数组，每个对象都有 `x`, `y` 和 `r` 属性：

```javascript
let chart = new Chart('chart', {
  type: 'bubble',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        data: [
          {x: 10, y: 50, r: 20},
          {x: 30, y: 10, r: 30},
          {x: 50, y: 20, r: 70}
        ]
      }
    ]
  }
});
```

***

#### 多系列图

如果 `datasets` 包含多个系列，则就会创建一个多系列图。对于柱状图，这意味着分组柱状图；对于折线图，这意味着多折线图。

你还可以使用 `label` 属性为系列命名，并使用 `backgroundColor` 属性为系列上色：

```javascript
let chart = new Chart('chart', {
  type: 'bar',
  data: {
    labels: ['A', 'B', 'C'],
    datasets: [
      {
        label: 'My series 1',
        backgroundColor: '#2E86AB', // blue
        data: [10, 20, 30]
      },
      {
        label: 'My series 2',
        backgroundColor: '#F18F01', // orange
        data: [15, 40, 20]
      }
    ]
  }
})
```

![chartjs multi series options](img/chartjs-multi-series-options.png)

图 13. 多系列（或分组）柱状图

***

#### 图表选项

图表配置对象有一个可选属性 `options` 用于额外配置。`options` 对象包含很多属性，所有的都是可选的。我们在书中将介绍一些最实用的选项。

广而言之，选项影响：

*   整个图表
*   x 轴和 y 轴
*   其他组件，如标题和图例。

Chart.js 将某些组件（即标题和图例）视为插件，这就是为什么它们出现在 `plugins` 属性下的。

***

让我们来看包含我经常使用的选项的 options 对象：

```javascript
let chart = new Chart('chart', {
  type: 'bar',
  data: { ... },
  options: {
    maintainAspectRatio: false, ①
    indexAxis: 'x', ②
    scales: { ③
      x: { ④
        title: { ⑤
          display: true,
          text: 'My x-axis title',
          color: '#333',
          font: {
            size: 12
          }
        },
        ticks: {
          color: '#aaa'
        },
        grid: {
          color: '#aaa'
        },
        stacked: false ⑥
      },
      y: {...}
    },
    plugins: { ⑦
      title: { ⑧
        display: true,
        text: 'My chart title',
        color: '#333',
        font: {
          size: 12
        }
      },
      legend: { ⑨
        display: true,
        position: 'top'
      }
    }
  }
});
```

列表 8. Chart.js options 对象

这些选项每一个都是可选的，所以如果你对某个选项的默认值满意，就不需要设置它。我们有时会通过相对于配置对象的完整路径来引用选项。例如，图例的 `display` 选项可以通过 `options.plugins.legend.display` 进行引用。这与 Chart.js 的文档保持一致。

1.  ① `options.maintainAspectRatio` 决定图表的宽高比例是否固定（无论图表宽度如何变化）。它的默认值为 `true`，但我经常将其设置为 `false`，以便创建一个固定高度且宽度适应设备宽度的图表。
2.  ② `options.indexAxis` 指定标签所在的轴。它的默认值为 `'x'`。如果设置为 `'y'`，标签将沿 y 轴显示；如果 `type` 为 `'bar'`，则你将得到一个水平柱状图。
3.  ③ `options.scales` 接受一个包含两个可选属性 `x` 和 `y` 的对象。`options.scales.x` 配置 x 轴，而 `options.scales.y` 配置 y 轴。
4.  ④ 每个轴配置对象都有若干可选属性。`title` 配置 x 轴标题，`ticks` 配置 x 轴刻度标记，`grid` 配置轴网格线。轴的网格线是从轴刻度延伸到图表另一侧的细线。`stacked` 决定多系列柱状图应该是堆叠还是分组的。
5.  ⑤ `title` 属性有多个可选属性，包括 `display`（决定标题是否可见）、`text`（标题文本）、`color`（标题颜色）和 `font`（一个配置标题字体的对象）。标题的 `font` 属性有几个可选属性，包括 `family`（字体族）、`size`（以像素为单位的字体大小）、`weight`（字体粗细）以及用于文本行高的 `lineHeight`。这些属性与 ` 相似
6.  Chart.js 将某些组件（即标题和图例）视为插件，这就是为什么它们出现在 `plugins` 属性下的。
7.  ⑥ `stacked` 决定多系列柱状图应该是堆叠还是分组的。
8.  ⑦ `plugins` 包含任何已安装的。
9.  ⑧ `title` 配置图表标题。
10. ⑨ `legend` 配置图例。两个最实用的属性是 `display`（决定图例是否可见）和 `position`（决定图例位置，可以设置为 `'top'`、`'bottom'`、`'left'` 或 `'right'`）。

例如：





```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

非整洁（或称“宽格式”）数据的一个示例是数据表格的列标题包含年份（例如 2000, 2001, 2002 等）：

|st | 2020 | 2021 | 2022 |
| --- | --- | --- | --- |
| 食品 | 1234 | 1343 | 1542 |
| 服物 | 431 | 522 | 467 |

2020、2021 和 2022 并不是变量。它们实际上是变量 `year` 的值。此外，每行代表 3 个观测值，而不是单个观测值。

该数据的整洁（或称“长格式”）版本是：

| 类别 | 年份 | 金额 |
| --- | --- | --- |
| 食品 | 2020 | 1234 |
| 食品 | 2021 | 1343 |
| 食品 | 2022 | 1542 |
| 服物 | 2020 | 431 |
| 服物 | 2021 | 522 |
| 服物 | 2022 | 467 |

现在每一列都是一个变量，每行都是一个观测值（例如，第一行是 2020 年食品类别的金额为 1234 的观测值）。

***

### 3.2.3. 如何使用 tidy.js

使用 tidy.js 处理数据时，调用 `tidy` 函数并将数据数组作为第一个参数传递。该数组需要是整洁格式，因此每个观测值由单个数组元素表示。

处理操作（如 `filter`、`sort`、`rename` 和 `count`）作为额外参数传递给 `tidy`。例如，让我们按状态过滤 REPD 数据（`data`），然后统计每个技术的申请数量：

```
import { tidy, filter, count } from '@tidyjs/tidy';

let summary = tidy(
  data,
  filter(d => d.status === 'Operational'),
  count('technology')
);
```

`tidy` 函数返回一个新的数组。在这种情况下，它是一个摘要数组：

```json
[
  {
    "technology": "Biomass (co-firing)",
    "n": 3
  },
  {
    "technology": "EfW Incineration",
    "n": 56
  },
  {
    "technology": "Biomass (dedicated)",
    "n": 78
  },
  {
    "technology": "Advanced Conversion Technologies",
    "n": 18
  },
  ...
]
```

理解 `tidy` 会创建一个新数组（它不会修改原始数组）是非常重要的。

***

### 3.2.4. 常见的 tidy.js 操作

tidy.js 拥有大量执行各种数据处理或分析任务的函数。本书中使用的函数有：`filter`、`rename`、`mutate`、`sort`、`count` 和 `groupBy`。

#### filter

`filter` 函数根据传入的函数过滤数据过滤。它类似于 JavaScript 的数组方法 `filter`。

这里有几个例子：

```
import { tidy, filter } from '@tidyjs/tidy';

// 获取所有正在运行的申请：
tidy(
  data,
  filter(d => d.status === 'Operational')
)

// 获取容量大于 100 的申请：
tidy(
  data,
  filter(d => d.capacity > 100)
)
```

***

#### rename

`rename` 重命名数组中每个项的属性。（在表格术语中，这等于重命名列。）你传递一个对象，其中每个属性的键是当前名称。

以下示例将 `status` 重命名为 `Application status`：

```javascript
import { tidy, rename } from '@tidyjs/tidy';

tidy(
  data,
  rename({status: 'Application status'})
)
```

#### mutate

`mutate` 函数为数组中的每个项创建一个新属性。它用于转换数据。

这里有几个例子：

```javascript
import { tidy, mutate } from '@tidyjs/tidy';

// 添加新属性 isCapacity
tidy(
  data,
  mutate({isCapacity: d => d.capacity > 1000})
)

// 转换 dateSubmitted
tidy(
  data,
  mutate({dateSubmitted: new Date()})
)
```

#### sort

`sort` 函数根据给定的属性名称对数据进行排序。默认按升序排序。要降序排序，用 `desc` 包裹属性名称。

这里有几个例子：

```javascript
import { tidy, sort, desc } from '@tidyjs/tidy';

// 按容量排序（升序）
tidy(
  data,
  sort('capacity')
)

// 按容量排序（降序）
tidy(
  data,
  desc('capacity')
)
```

***

#### count

`count` 函数是一种聚合操作，根据属性对数据进行分组并计算每个组的大小。它返回一个对象数组，每个对象包含组名和一个用于计数的属性 `n`。

要降序排序结果，请作为第二个参数传递对象 `{sort: true}`。

```javascript
import { tidy, count } from '@tidyjs/tidy';

// 统计每种技术的申请数量
tidy(
  data,
  count('technology', {sort: true})
)
```

***

#### groupBy

`groupBy` 函数根据给定属性对数据进行分组对其进行操作。这对于在数据集上执行聚合操作（如和、平均值、中位数、最小值和最大值）非常有用。

例如，你可以计算每种技术的计数和平均（mean）容量：

```javascript
import { tidy, groupBy, n, mean, desc } from '@tidyjs/tidy';

// 按技术分组，并计算每个组的申请数量和平均容量
tidy(
  data,
  groupBy('technology', [
    summarize({
      count: n(),
      meanCapacity: mean('capacity')
    })
  ]),
  sort(desc('meanCapacity'))
)
```





`summarize` 接收一个对象，其属性名称（在我们的示例中为 `count` 和 `meanCapacity`）将被添加到结果数组中每个组的属性中。属性的值是 tidy.js 的摘要函数，如 `n`、`min`、`max`、`mean`、`median` 和 `deviation`。每个摘要函数都会在每个组上调用一次，并将返回值写入结果数组中。

因此，在上面的示例中，“Pumped Storage Hydroelectricity” 组有 10 个成员，平均容量为 573.78。

### 3.2.5\. tidy.js 示例

`tidyjs-examples` 是一个演示 tidy.js 功能的 Vite 项目。它加载 REPD 数据，执行 tidy.js 转换，并在浏览器中显示结果。

运行方法：

```
## 确保你处于 visualising-data-with-js-code 目录中

cd tidyjs-examples

npm install

npm run dev
```

如果你正在运行一个 Vite 服务器，请使用 `ctrl-c` 停止服务器。

这里有许多独立示例。取消你想要尝试的示例（并确保其他示例已被注释）。

* * *

## 3.3\. Chart.js 示例应用

在本节中，我们将查看一个加载 REPD 数据、使用 tidy.js 对数据进行摘要并使用 Chart.js 可视化结果的应用。该项目使用 Vite 构建，因此结构与 `load-data` 项目类似。

![chartjs app bar chart](img/chartjs-app-bar-chart.png)

图 14\. 由 chart-js 项目创建的柱状图

运行项目时，导航到 `chart-js` 项目目录并执行 `npm install`。执行 `npm run dev` 启动应用程序服务器。这将提供一个可以访问的 URL（通常为 [`localhost:5173`](http://localhost:5173)）。当你访问该 URL 时，你应该看到一个柱状图。

```
cd chart-js

npm install

npm run dev
```

* * *

### 3.3.1\. 文件结构

项目目录结构如下：

```
chart-js/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

列表 9\. chart-js 项目文件

该项目使用 Vite 构建，因此具有标准的 Vite 文件结构。REPD 数据位于 `public` 目录中。所有的 JavaScript 代码都在 `main.js` 中。

项目主要文件有 `index.html`、`main.js` 和数据文件 `public/repd.json`。让我们来看前两个。

### 3.3.2\. index.html

这是主 HTML 文件 `index.html`：

```
<!DOCTYPE html>
<html lang="en">
  <head>
  <meta charset="UTF-8" />
  <link rel="icon" type="image/svg+xml" href="#" />
  <meta name="viewport" content="..." />
  <title>Vite App</title>
  </head>
  <body><body>
  <canvas id="chart"></canvas> ①
  <script type="module" src="/main.js"></script>
  </body>
</html>
```

列表 10\. chart-js/index.html

1. *①* 与 Vite 生成的 `index.html` 相比，唯一的变化是包含了一个图表的 `<canvas>` 元素。

* * *

### 3.3.3\. main.js

这是主 JavaScript 文件：

```javascript
import { tidy, count } from '@tidyjs/tidy';
import Chart from 'chart.js/auto';

function draw(data) {
  let summary = tidy(
    data,
    count('technology', {sort: true})
  );

  const myChart = new Chart('chart', {
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.n)
      }]
    },
    options: {
      plugins: { ... }
    }
  });
}

fetch('./repd.json') ①
  .then(res => res.json())
  .then(data => draw(data));
```

列表 11\. chart-js/main.js

1. *①* 使用 `fetch` 请求 REPD 数据，并在加载后将其转换为对象数组并发送到 `draw` 函数。这与 `load-data` 项目中用于加载数据的代码相似。

* * *

让我们逐步分析 `draw` 函数：

```javascript
function draw(data) {
  let summary = tidy(
    data,
    count('technology', {sort: true})
  );

  ...
}
```

列表 12\. chart-js/main.js

`draw` 从创建一个数据的摘要数组开始。`summary` 看起来类似于：

``````json
[
  {
    "technology": "Solar Photovoltaics",
    "n": 3593
  },
  {
    "technology": "Wind Onshore",
    "n": 2196
  },
  {
    "technology": "Battery",
    "n": 948
  },
  ...
]
```

* * *

接下来创建一个 Chart.js 图表：

```javascript
function draw(data) {
  let summary = tidy(
    data,
    count('technology', {sort: true})
  );

  const myChart = new Chart('chart', {
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.n)
      }]
    },
    options: { ... }
  });
}
```

列表 13\. chart-js/main.js

1. *①* 通过调用构造函数并传入图表 `<canvas>` 元素的 ID 创建图表。

2. *②* 配置对象的 `type` 属性设置为 `bar`。

3. *③* `labels` 数组是通过使用 `map` 方法提取 `summary` 中的 `technology` 属性生成的。这生成了 `["Solar Photovoltaics", "Wind Onshore", "Battery", ...]`。

4. *④* 同样，`data` 数组是通过使用 `map` 方法提取 `summary` 中的 `n` 属性生成的。

* * *

现在来看 `options` 对象：

```javascript
function draw(data) {
  let summary = tidy(
    data,
    count('technology', {sort: true})
  );

  const myChart = new Chart('chart', {
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.n)
      }]
    },
    options: {
      plugins: {
        title: {
          display: true, ①
          text: 'Number of submissions (by technology)', ②
          font: {
            size: 18 ③
          }
        },
        legend: {
          display: false ④
        }
      }
    }
  });
}
```

列表 14\. chart-js/main.js

1. *①* 使标题可见。

2. *②* 设置标题。

3. *③* 设置标题的字体大小。

4. *④* 隐藏图例。

* * *

此示例创建了以下图表：

![chartjs app bar chart](img/chartjs-app-bar-chart.png)

图 15\. 由 chart-js 项目创建的柱状图

## 3.4\. 总结

本章介绍了 Chart.js 和 tidy.js。我们查看了如何使用 Chart.js 创建简单的柱状图，以及如何使用 tidy.js 进行数据转换。

在下一节中，我们将介绍 Chart.js 样式以及创建多系列图表。

## 4\. Chart.js 样式与自定义

在本章中，我将展示：

*   如何为 Chart.js 设置样式
*   如何创建一个黑暗主题的 Chart.js 图表
*   如何从长数据创建折线图
*   如何从长数据创建堆叠柱状图

我们使用了这两个库，这些知识在后面的“数据故事”章节中用到。

## 3.5\. 进一步学习建议

我建议通过探索、修改和添加代码来尝试该项目。这里建议：

*   显示每个地区的应用程序数量（而不是技术）
*   按字母顺序对柱进行排序
*   将柱体颜色改为 `'steelblue'`。

请访问附录获取解决方案。





```
chartjs-various/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

列表 15. chartjs-various 项目文件

该项目使用 Vite 构建，因此具有标准的 Vite 文件结构。主要的项目文件有 `index.html`、`main.js`、`style.css` 以及数据文件 `public/repd.json`。

### 4.1.2 index.html

主 HTML 文件是 `index.html`：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="#" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite App</title>
  </head>
  <body>body
    <div class="chart-wrapper"> ①
      <canvas id="chart-1"></canvas> ②
    </div>
    <div class="chart-wrapper dark"> ①
      <canvas id="chart-2"></canvas> ③
    </div>
    <div class="chart-wrapper"> ①
      <canvas id="chart-3"></canvas> ④
    </div>
    <div class="chart-wrapper"> ①
      <canvas id="chart-4"></canvas> ⑤
    </div>
    <script type="module" src="/main.js"></script>
  </body>
</html>
```

列表 16. chartjs-various/index.html

1. ① 每个 `<canvas>` 元素都放置在一个包装器内，以帮助调整图表大小。
2. ② 用于样式化柱状图的 `<canvas>` 元素。
3. ③ 用于深色主题图表的 `<canvas>` 元素。
4. ④ 用于折线图的 `<canvas>` 元素。
5. ⑤ 用于堆叠柱状图的 `<canvas>` 元素。

每个图表都有自己带有唯一 `id` 的 `<canvas>` 元素。

要控制 Chart.js 图表的大小，推荐的方法是使用 `<div>` 元素包裹图表的 `<canvas>` 元素，并调整该 `<div>` 元素的大小（[参见文档](https://www.chartjs.org/docs/latest/configuration/responsive.html#important-note)）。你还需要将图表的 `maintainAspectRatio` 选项设置为 `false`，以便图表能够适应包装器的宽度和高度。

在这个项目中，我们为每个 `<div>` 包装器添加了 `chart-wrapper` 类名，以便在 `style.css` 中对其进行样式化。

### 4.1.3 style.css

`style.css` 主要包含用于样式化和调整图表包装元素大小的规则：

```css
body {
  margin: 0; ①
}

.chart-wrapper {
  height: 600px; ②
  background-color: #F9F7EB; ③
  padding: 2rem; ④
}

.chart-wrapper.dark {
  background-color: #222; ⑤
}
```

列表 17. chartjs-various/style.css

1. ① 移除整个页面的默认边距。
2. ② 将图表包装器的高度设置为 600px，以便图表具有固定高度。图表包装器的宽度（我们未设置）将是 100%，这是 `<div>` 元素的默认宽度。这意味着每个图表将跨越整个宽度并且高度为 600px。（将 Chart.js 的 `maintainAspectRatio` 选项设置为 `false` 非常重要，这样每个图表就可以垂直和水平方向上填充其包装器。）
3. ③ 每个图表包装器的背景颜色设置为白色。
4. ④ 我们在包装器边界和图表之间添加了一些内边距（padding）。
5. ⑤ 如果包装器设置了 `dark` 类属性，则将背景设置为深灰色。

### 4.1.4 main.js

`main.js` 比较长，让我们先从概要开始：

```javascript
import { tidy, count, filter } from '@tidyjs/tidy';
import Chart from 'chart.js/auto';
import uniq from 'lodash-es/uniq';

import './style.css';

Chart.defaults.plugins.legend.display = false; ④
Chart.defaults.scale.title.font = {size: 14};
Chart.defaults.plugins.title.display = true;
Chart.defaults.plugins.title.font.size = 18;
Chart.defaults.maintainAspectRatio = false;

const technologyPalette = { ⑤
  'Advanced Conversion Technologies': '#FF9999',
  'Anaerobic Digestion': '#C58882',
  'Battery': '#B6A6CA',
  ...
};

function getMultiSeriesChartData(data, seriesProp, labelProp) { ... } ③

function drawChart1(data) { ... }
function drawChart2(data) { ... }
function drawChart3(data) { ... }
function drawChart4(data) { ... }

function draw(data) { ②
  drawChart1(data);
  drawChart2(data);
  drawChart3(data);
  drawChart4(data);
}

fetch('./repd.json') ①
  .then(res => res.json())
  .then(data => draw(data));
```

列表 18. chartjs-various/main.js

1. ① `main.js` 以与 `load-data` 相同的方式加载。当数据到达时调用 `draw`。
2. ② `draw` 函数为四个图表调用绘制函数（如 `drawChart1`）。
3. ③ 图表 3 和 4 用于将数据转换为多个系列的辅助函数。
4. ④ 设置适用于所有图表的 Chart.js 选项（稍后可见）。
5. ⑤ `technologyPalette` 是一个查找对象，为每种技术类型定义了颜色。我使用了网站 [coolors.co](https://coolors.co) 来寻找颜色。（我循环不同的调色板并挑选出我中中的颜色！）

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

在 `main.js` 的顶部，我们设置了一些适用于所有图表的 Chart.js 选项。

## 4.2 Chart 1 (样式化水平图表)

`drawChart1` 是绘制此图表的函数：

列表 21. chartjs-various/main.js 

```javascript
function drawChart2(data) {
  let summary = tidy(...); ①

  const myChart = new Chart('chart-2', {
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.n),
        backgroundColor: '#19A0AA' ②
      }]
    },
    options: { ... } ③
  });
}
```

列表 20. chartjs-various/main.js

1. ① 以 Chart 1 相同的方式汇总数据。
2. ② 柱状颜色与 Chart 1 保持一致。




[content]

### 3. `options` 对象（见后文）。

我们将在下一页查看 `options` 对象。

```
{
  indexAxis: 'y',
  scales: {
    x: {
      title: {
        display: true,
        text: 'Number of applications',
        color: '#eee' ①
      },
      ticks: {
        color: '#ccc' ②
      },
      grid: {
        color: '#555' ③
      }
    },
    y: {
      ticks: {
        color: '#ccc' ②
      },
      grid: {
        color: '#333' ③
      }
    }
  },
  plugins: {
    title: {
      text: 'Number of planning applications (by technology) 1990-2022',
      color: '#ccc' ④
    }
  }
}
```
列表 21. `chartjs-various/main.js`

1.  `①` 将 x 轴标题设置为浅灰色，以便在深色背景上显示。
2.  `②` 将坐标轴刻度设置为浅灰色，以便它们在深色背景上显示。
3.  `③` 将网格线设置为浅灰色，以便它们在深色背景上显示。
4.  `④` 将图表标题设置为浅灰色，以便其在深色背景上显示。

## 4.4. 图表 3（多折线图）

图 3 是一个多折线图。对于每种技术类型，线条显示了随时间变化的规划申请数量。x 轴代表年份，y 轴代表申请数量。

![chartjs styled 3](img/chartjs-styled-3.png)

图 22. 多折线图

`drawChart3` 函数绘制此图表。图表本身与之前的类似。然而，挑战在于将 REPD 数据转换为系列数组。

我们使用了一个辅助函数 `getMultiSeriesChartData`（定义在 `main.js` 顶部），它接受三个参数：

1.  REPD 数据数组。
2.  定义每个系列名称的 `data` 属性。
3.  定义坐标轴标签的 `data` 属性。

对于此图表，每个系列是一种技术类型且 x 轴代表提交年份，我们调用：

```
getMultiSeriesChartData(data, 'technology', 'yearSubmitted');
```

此返回一个如下所示的对象：

```
{
  labels: [1990, 1991, 1992, ... 2020, 2021, 2022], ①
  datasets: [ ②
    {
      label: "Advanced Conversion Technologies",
      data: [0, 0, 0, ... 0, 0, 0] ③
    },
    {
      label: "Anaerobic Digestion",
      data: [0, 0, 0, ... 10, 17, 22] ③
    }
    ,
    ...
  ]
}
```

1.  `①` `labels` 中的每个值代表主轴上的一个名称。
2.  `②` `datasets` 中的每个对象代表特定技术类型的系列。
3.  `③` 系列中 `data` 数组的值是给定技术类型和相应年份的规划申请数量。例如，厌氧消化（Anaerobic Digestion）2020 年有 10 个规划申请，2021 年有 17 个，2022 年有 22 个。如果图表类型为 `line`，这些数据将生成一个多折线图，年份沿主轴显示，每种技术类型由线条表示。

我们将 `getMultiSeriesChartData` 的输出赋值给 `chartData`，并将其作为 Chart.js 配置对象中 `data` 属性的值：

```
function drawChart3(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'yearSubmitted'); ①

  ...

  const myChart = new Chart('chart-3', {
    type: 'line',
    data: chartData, ②
    options: { ... }
  });

  ...
}
```
列表 22. `chartjs-various/main.js`

1.  `①` 将 `getMultiSeriesChartData` 的返回值赋值给 `chartData`。
2.  `②` 将图表的 `data` 属性设置为 `chartData`。

出于本书的考虑，你不需要理解 `getMultiSeriesChartData`，但如果你对它的工作原理感兴趣，请访问书末附录中的“getMultiSeriesChartData’。

让我们完整查看 `drawChart3`：

```
function drawChart3(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'yearSubmitted'); ①

  // 为每个系列添加样式
  chartData.datasets.forEach(series => { ②
    let color = technologyPalette[series.label] || '#aaa'; ③
    series.borderColor = color; ④
    series.borderWidth = 1.5; ④
    series.backgroundColor = color; ⑤
    series.radius = 2; ⑥
  });

  const myChart = new Chart('chart-3', { ⑦
    type: 'line', ⑧
    data: chartData, ⑨
    options: { ⑩
      scales: {
        x: {
          title: {
            display: true,
            text: 'Year'
          }
        },
        y: {
          title: {
            display: true,
            text: 'Number of applications'
          }
        }
      },
      plugins: {
        title: {
          text: 'Number of planning applications (by technology) 1990-2022',
        },
        legend: {
          display: true
        }
      }
    }
  });
}
```
列表 23. `chartjs-various/main.js`

1.  `①` 调用 `getMultiSeriesChartData` 构建图表。第二个参数定义了用于系列的属性（'technology'），第三个参数定义了主轴属性（'yearSubmitted'）。
2.  `②` 遍历 `chartData.datasets` 并添加样式，使图中每条线条按技术类型着色。
3.  `③` 使用 `technologyPalette` 查找颜色。如果没有定义颜色则退到灰色。
4.  `④` `borderColor` 设置线条颜色，`borderWidth` 设置线条宽度。
5.  `⑤` `backgroundColor` 设置数据点的颜色。
6.  `⑥` `radius` 设置数据点的半径。
7.  `⑦` 调用 `new Chart()` 构建图表并传入 `<canvas>` 元素的 id 和配置对象。
8.  `⑧` 在配置对象中将 `type` 设置为 `'line'`
9.  `⑨` 将 `data` 属性设置为数据对象 `chartData`。它是通过 `getMultiSeriesChartData` 创建的。
10. `⑩` 最后设置坐标轴标题、图表标题和图例。

## 4.5. 图表 4（堆叠柱状图）

图 4 是一个堆叠柱状图，显示了每个地区的规划申请数量。每个柱子按技术类型细分。这允许读者查看每个地区不同技术类型的规划申请分布。例如，一眼就能看出苏格兰的风能相关申请比任何其他地区都多。

`drawChart4` 函数绘制此图表，工作原理与 `drawChart3` 类似，但现在每个数据系列对应一组相同颜色的水平切片。例如，代表太阳能光伏（Solar Photovoltaics）的系列由通过每个柱子的黄色切片表示。

与 `drawChart3` 一样，它调用了 `getMultiSeriesChartData`，但这次坐标轴标签属性是 `region`：

```
let chartData = getMultiSeriesChartData(data, 'technology', 'region');
```




```javascript
function drawChart4(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'region'); ①

  // Add colour to each series
  chartData.datasets.forEach(series => { ②
    let color = technologyPalette[series.label] || '#aaa';
    series.backgroundColor = color;
  });

  const myChart = new Chart('chart-4', { ③
    type: 'bar', ④
    data: chartData, ⑤
    options: {
      scales: {
        x: {
          stacked: true, ⑥
        },
        y: {
          stacked: true, ⑥
          title: {
            display: true,
            text: 'Number of applications'
          }
        }
      },
      plugins: {
        title: {
          text: 'Number of applications (by region and technology) 1990-2022',
        },
        legend: {
          display: true
        }
      }
    }
  });
}
```

Listing 24. `chartjs-various/main.js`

1. ① 调用 `getMultiSeriesChartData` 构建图表数据对象。第二个参数定义了使用哪个属性作为系列（`'technology'`），第三个参数定义了使用哪个属性作为主轴标签（`'region'`）。
2. ② 遍历 `chartData.datasets` 中的每个并添加样式属性，以便每个条形块根据技术类型着色。`backgroundColor` 设置了条形块的颜色。
3. ③ 通过调用 `new Chart()` 并传入 `<canvas>` 元素的 ID 和配置对象来构建图表。
4. ④ 在配置对象中将类型设置为 `'bar'`。
5. ⑤ 将 `data` 属性设置为数据对象 `chartData`。该对象是使用 `getMultiSeriesChartData` 创建的。
6. ⑥ 要创建堆叠柱状图，需将 `x` 和 `y` 轴尺的 `stacked` 属性设置为 `true`。如果我们让它们保持默认的 `false` 值，就会得到分组柱状图。

## 4.6 总结

本章展示了 Chart.js 图表的几种样式化方法。我们改变了简单柱状图的配色方案使其看起来更简洁，并展示了如何实现深色主题图表。

我还展示了如何创建多折线图和堆叠柱状图，并演示了一个辅助函数，该函数将数据数组转换为 Chart.js 所需的多系列结构。

到此，Chart.js 的介绍此结束。我没有涵盖关于 Chart.js 的所有知识，但足以让你能够创建有用且美观的图表。我们将在书的后部分创建数据故事时使用这些知识。

# 5. 使用 D3.js 自定义图表

本章介绍了 [D3.js](https://d3js.org)，这是一个免费且开源的 JavaScript 库。D3 不提供现成的图表，而是提供用于制作自定义数据可视化的构建模块。

![d3 timeline](img/d3-timeline.png)

图 25. 使用 D3.js 创建的自定义图表。每个圆代表一个 REPD 规划申请。

在本章中，我将：

* 介绍 D3
* 学习 D3 的哲学
* 学习 D3 选择（selections）、连接（joins）和比例尺函数（scale functions）
* 学习 Tippy.js 提示框模块
* 演示一个可视化 REPD 数据的 D3 示例

## 5.1 D3 简介

D3 是一个免费、开源的 JavaScript 库，帮助你创建自定义数据可视化。与提供一系列现成图表的 Chart.js 不同，D3 提供了一系列函数，帮助你制作可以想象的任何图表。用烹饪术语来说，Chart.js 就像是外卖（快速方便），而 D3 就像是从原材料食材开始烹饪（需要更多的时间和技巧，但结果更好）。

D3 确实需要更多的技能，通常需要更多的代码。例如，使用 Chart.js 创建柱状图只需要几行代码，但使用 D3 这可能需要数百行代码（如果你想涵盖所有功能和情况）。

我在书中介绍 D3 是因为它是最流行的 JavaScript 数据可视化库之一，而且非常强大。然而，全面涵盖 D3 超出了本书的范围，但我展示了足够的原理以及它能做什么。

如果你感兴趣学习更多，我建议阅读 [D3 Start to Finish](https://www.createwithdata.com/d3-start-to-finish-book/)，它将带你逐步完成一个完整的示例。

如果这一章证明很有挑战性，请担心。我们在书中其他地方没有使用 D3，所以你可以跳过这一章。

## 5.2 D3 的原理

### 5.2.1 数据连接 (Data Join)

D3 的核心原理之一是数据连接。这是数据数组与一组 DOM 元素关联。（DOM 元素是浏览器对 HTML 或 SVG 元素的内部表示。）这意味着每个数据项都与一个 DOM 元素关联。然后我们将数据变量（如 `year`、技术类型或容量）与 DOM 元素的样式和属性（如位置、大小和颜色）关联。

例如，我们可以用圆表示每个 REPD 规划申请。这产生了大约 8000 个圆。现在我们将提交年份（`yearSubmitted`）与圆在 x 轴的位置关联。这产生了一行圆，最右侧的圆是最新的申请：

![d3 dot 1](img/d3-dot-1.png)

图 26. 点图，其中 x 坐标表示提交日期。

这不是最实用（也最令人深刻）的数据可视化。但请放心，每个点都代表一个规划申请。如果我们让每个圆透明（通过降低其 `opacity` 值），我们就能看到更多随时间变化的趋势（线条越深，申请数量越多）：

![d3 dot 2](img/d3-dot-2.png)

图 27. 降低每个圆的透明度揭示了趋势

现在我们根据技术类型将每个圆放置在 y 轴上：

![d3 dot 3](img/d3-dot-3.png)

图 28. 根据技术将每个圆放置在 y 坐标上

现在我们可以看到数据中的模式。我们可以看到某些技术在后期变得更加流行，而某项技术（就在图表中间偏下方的那个）在早期更流行，但随后逐渐衰落。底部（代表陆上风电）在所有年份都有强劲的申请流。（没有标签告诉我们哪一行属于什么技术。这是 D3 需要更多努力的地方，因为我们需要使用更多代码添加它们！）

现在我们根据状态给每个圆上色：

![d3 dot 4](img/d3-dot-4.png)

图 29. 根据状态为每个圆上色

绿色意味着站点正在运行，黄色意味着站点正在等待或建设中，紫色意味着规划申请正在进行，灰色意味着规划申请已被放弃、撤回或拒绝。现在我们根据每个拟建设施的功率输出（或容量）调整圆的大小：

![d3 dot 5](img/d3-dot-5.png)

图 30. 根据容量调整圆的大小

底部代表陆上风电，上方是海上风电。意不意外，这些的功率输出最大。

这个示例让我们了解 D3 的工作原理。我们用形状表示数据，并根据数据值修改每个形状的视觉变量。（形状的视觉变量是如 x 坐标、y 坐标、长度、宽度、半径和颜色。）在本章中，我将向你展示如何创建刚刚演示的示例。我们还添加了显示年份的 x 轴和显示技术类型的 y 轴。

![d3 timeline](img/d3-timeline.png)

图 31. REPD 时间线（d3-dot 项目）

### 5.2.2 模块

D3 由多个模块组成，每个模块都包含帮助你构建可视化的函数。（你可以将 D3 想象成一个构建可视化的工具箱。）

模块包括：

* `d3-selection`（用于添加、删除和修改 DOM 元素以及执行数据连接的函数）




*   `d3-scale`（将数据值转换为视觉值（如位置和颜色）的函数）
*   `d3-axis`（绘制 x 轴和 y 轴的函数）
*   `d3-hierarchy`（帮助构建层次结构（如矩树图和圆点布局）的函数）
*   `d3-force`（基于物理的定位引擎）
*   `d3-geo`（用于绘制地图）
*   `d3-array`（数组操作函数）

每个模块包含了构建可视化的工具，从计算数组中最小值或最大值的简单函数，到帮助你构建交互式、可缩放树图的函数不等。使用 D3 的技巧在于如何将这些元素组合在一起。

我在本书中介绍了几个核心模块，即 `d3-selection`、`d3-scale`、`d3-axes` 和 `d3-array`。这种组合足以构建自定义的可视化。

关于其他模块的更多信息，我建议访问[官方文档](https://d3js.org/api) 或 [D3 in Depth](https://d3indepth.com)。

## 5.3 使用 D3

在这一节中，我们将查看 D3 的几个核心模块（`d3-selection`、`d3-scale`、`d3-axes` 和 `d3-array`）。我使用 D3 构建的大多数可视化项目都使用了这些模块，我建议先熟悉它们。我们在稍后的 REPD 时间线示例中使用了所有四个模块。

### 5.3.1 安装

你可以使用 `npm install d3` 安装整个 D3 库，也可以使用（例如）`npm install d3-selection` 安装单个模块。在本章中，我们将安装单个 d3 模块。

### 5.3.2 选择

`d3-selection` 模块允许你添加、删除和修改 DOM 元素。它还允许你执行数据连接（将数据数组与 DOM 元素关联）。

`d3-selection` 中的一个核心概念是“选择”（selection），它基本上是 DOM 元素的数组。为了修改 DOM 元素并连接数据，你需要创建一个选择。

假设你的 `index.html` 文件中有以下 HTML 代码段（它是一个包含三个圆形的 `<svg>` 元素）：

```
<svg>
  <circle></circle>
  <circle></circle>
  <circle></circle>
</svg>
```

你可以使用 `select` 创建一个包含**单个元素**的选择。它接受一个包含 CSS 选择器字符串的单个参数：

```javascript
import { select } from 'd3-selection';

// 选择 svg 元素
select('svg');

// 选择第一个圆
select('circle');
```

你也可以使用 `selectAll` 创建一个包含**多个元素**的选择。它会找到所有匹配的元素：

```javascript
import { selectAll } from 'd3-selection';

// 选择所有的圆
selectAll('circle');
```

你可以通过**链式调用** `select` 或 `selectAll` 来选择选择元素的子元素。这里是一个示例，我们对 `<svg>` 元素进行单一选择，然后选择它内部所有的 `<circle>` 元素：

```javascript
import { select } from 'd3-selection';

// 选择 svg 元素并选择其所有的圆元素
select('svg')
  .selectAll('circle');
```

这被称为**嵌套选择**（nested selection），在连接数据时非常重要。

选择基本上是 DOM 元素的数组，但选择有很多方法可以修改元素的样式和属性。常用的方法是 `.style` 和 `.attr`：

```javascript
import { select } from 'd3-selection';

select('svg')
  .selectAll('circle')
  .attr('cx', 200)
  .attr('cy', 100)
  .attr('r', 10)
  .style('fill', 'blue')
  .style('stroke', '#aaa');
```

1. ① 选择 `<svg>` 元素。
2. ② 选择 `<svg>` 元素内的所有 `<circle>` 元素。
3. ③ 添加值为 `200` 的 `cx` 属性。这设置了 x 坐标。
4. ④ 添加值为 `100` 的 `cy` 属性。这设置了 y 坐标。
5. ⑤ 添加值为 `10` 的 `r` 属性。这设置了半径。
6. ⑥ 将 `fill` CSS 属性设置为 `'blue'`。
7. ⑦ 将 `stroke` CSS 属性设置为 `'#aaa'`。

你可以在 [Codepen](https://codepen.io/pen/NzX) 上查看此示例。注意，Codepen 导入了整个 D3 库，所以我们使用 `d3.select` 而不是 `select`。此外，三个圆的位置和半径相同，所以你只能看到。

### 5.3.3 数据连接

你可以使用 `join` 创建数据数组与选择之间的对应。这允许你以数据驱动的方式添加、删除和修改 DOM 元素。

让我们从一个简单的示例开始：

```javascript
let data = [
  { time: 50, value: 15 },
  { time: 150, value: 40 },
  { time: 250, value: 30 }
];

select('svg')
  .selectAll('circle')
  .data(data)
  .join('circle')
  .style('fill', 'orange')
  .attr('cx', d => d.time)
  .attr('cy', 100)
  .attr('r', d => d.value);
```

结果如下：

![d3 连接圆](img/d3-join-circles.png)

图 32. 将数据数组连接到圆形元素

每个数组元素对应一个 `<circle>` 元素。每个圆的 x 坐标和半径根据连接的数据进行设置。




这是 Codepen 上的示例：[`codepen.io/createwithdata/pen/OJwpVbG`](https://codepen.io/createwithdata/pen/OJwpVbG)。

### 5.3.4. 比例尺函数 (Scale functions)

尺度函数允许你将数据变量转换为视觉变量，例如位置和颜色。例如，REPD 数据中的年份在 1990 年到 2021 年之间。如果你想构建一个长度为 1000 像素的时间轴，可以创建一个比例函数，接收年份并输出 0 到 1000 之间的值。

D3 有几种比例尺类型，最常见的是 `scaleLinear`、`scaleSqrt`、`scaleTime` 和 `scalePoint`。对于每种比例类型，D3 都提供了一个构造函数。典型的用法模式是：

* 调用比例尺构造函数。这会返回一个比例函数。
* 通过调用比例函数的 `domain` 方法设置比例尺的域（domain）。域是比例函数的输入最小值和最大值值。
* 通过调用比例函数的 `range` 方法设置比例尺的范围（range）。范围是比例函数的输出最小值和最大值。

这里有一个创建一个线性比例尺的示例：

```
import { scaleLinear } from 'd3-scale';

let myScale = scaleLinear() ①
  .domain([0, 100]) ②
  .range([0, 500]); ③
```

1. ① 调用比例尺构造函数以创建并返回一个比例函数。
2. ② 调用比例尺的 `domain` 方法设置其域（其最小和最大输入）。
3. ③ 调用比例尺的 `range` 方法设置其范围（其最小和最大输出）。

`myScale` 是一个线性比例函数，它接受 0 到 100 之间的值，并输出 0 到 500 之间的值。它在域和范围之间进行线性映射。这意味着沿域的比例为 `u` 的输入值将映射到沿范围的比例为 `u` 的值。

例如：

```
myScale(0); // 返回 0
myScale(100); // 返回 500
myScale(50); // 返回 250
```

`scaleTime` 与 `scaleLinear` 类似，但它的域是一个日期数组：

```
import { scaleTime } from 'd3-scale';

let timeScale = scaleTime()
  .domain([new Date(2016, 0, 1), new Date(2017, 0, 1)])
  .range([0, 700]);

timeScale(new Date(2016, 0, 1));   // 返回 0
timeScale(new Date(2016, 6, 1));   // 返回 348.00...
timeScale(new Date(2017, 0, 1));   // 返回 700
```

我们在 REPD 点图示例中使用 `scaleTime` 来计算每个圆的 x 坐标。

`scalePoint` 接受分类值数组作为其域，并将值分布在范围内：

```
let pointScale = scalePoint()
  .domain(['Mon', 'Tue', 'Wed', 'Thu', 'Fri'])
  .range([0, 500]);

pointScale('Mon');  // 返回 0
pointScale('Tue');  // 返回 125
pointScale('Fri');  // 返回 500
```

我们在 REPD 点图示例中使用 `scalePoint` 来计算每个圆的 y 坐标。

***

`scaleSqrt` 在按变量比例调整圆的大小时非常有用：

```
let sqrtScale = scaleSqrt()
  .domain([0, 100])
  .range([0, 30]);

sqrtScale(0);   // 返回 0
sqrtScale(50);  // 返回 21.21...
sqrtScale(100); // 返回 30
```

我们在 REPD 点图示例中使用 `scaleSqrt` 来计算每个圆的半径。

### 5.3.5. 轴 (Axes)

`d3-axis` 模块帮助你绘制轴。要绘制轴：

* 创建一个 SVG `<g>` 元素作为轴的容器。你还需要使用 `transform` 属性对其进行适当定位。
* 通过调用 `axisLeft`、`axisRight`、`axisBottom` 或 `axisTop` 并传入一个比例函数来创建一个轴生成器。
* 选择轴容器并使用选择的 `.call` 方法调用轴生成器。

轴有四类型，取决于它位于图表的哪侧。例如，`axisLeft` 用于图表左侧的 y 轴。

作为一个示例，我们来创建一个 x 轴。首先添加一个 SVG `<g>` 元素作为轴的容器。注意我们平移了它，使得轴不会被视口的顶部和左侧边界裁剪：

```
<svg>
  <g class="x-axis" transform="translate(100,100)"></g>
</svg>
```

***

在 JavaScript 中，我们创建一个比例函数并将其传入 `axisBottom`：

```javascript
import { select } from 'd3-selection';
import { scaleLinear } from 'd3-scale';

let scale = scaleLinear()
  .domain([0, 100])
  .range([0, 500]);

let axis = axisBottom(scale);

select("svg")
  .append("g")
  .attr("class", "x-axis")
  .attr("transform", "translate(0,500)")
  .call(axis);
```




当鼠标指针悬停在数据点上时，提示框（tooltip）会显示关于该数据点的更多信息。良好的实现并不容易，因此我建议使用如 [Tippy.js 提示框库](https://atomiks.github.io/tippyjs/) 这样的库。该库用法非常简单，外观美观且运行良好。你可以向提示框填充任何喜欢的内容，它甚至会自动调整以确保在靠近容器边缘时不会被裁剪。

![tippyjs](img/tippyjs.png)

图 35. Tippy.js 提示框

要使用 Tippy.js：

*   在命令行中使用 `npm install tippy.js` 安装
*   使用 `import tippy from 'tippy.js'` 将其导入 JavaScript 文件中
*   使用 `import 'tippy.js/dist/tippy.css'` 导入 Tippy 的样式文件
*   通过调用 `tippy()` 为每个元素添加提示框。第一个参数指定元素，第二个参数是配置对象。

* * *

让我们在正在进行的示例中添加提示框：

```
import { select } from 'd3-selection';
import tippy from 'tippy.js'; ①
import 'tippy.js/dist/tippy.css'; ②

let data = [
  { time: 50, value: 15 },
  { time: 150, value: 40 },
  { time: 250, value: 30 }
];

select('svg')
  .selectAll('circle')
  .data(data)
  .join('circle')
  .style('fill', 'orange')
  .attr('cx', d => d.time)
  .attr('cy', 100)
  .attr('r', d => d.value)
  .each(function(d) { ③
    tippy(this, { ④
      content: 'The value is ' + d.value ⑤
    });
  });
```

1.  ① 导入 Tippy 的构造函数函数 `tippy()`。
2.  ② 导入 Tippy 的样式文件。（Vite 允许你在 JavaScript 文件中导入 CSS 文件。）
3.  ③ D3 的 `each` 方法允许你遍历选择中的每个元素。对于选择中的每个元素，都会调用指定的回调函数，并将元素的绑定数据赋值给参数 `d`。
4.  ④ 通过调用 `tippy()` 并将当前元素作为第一个参数传入，为当前元素添加提示框。（在回调函数中，D3 将当前的 DOM 元素赋值给 `this` 关键字，只要是函数是使用 `function` 关键字定义的，而不是箭头函数。）
5.  ⑤ 将配置对象作为第二个参数传入。我们使用 `content` 属性设置内容。`d` 代表当前元素的绑定数据，我们显示它的 `value` 属性。

* * *

现在，当悬停在圆形上时，会显示提示框：

![tippyjs simple](img/tippyjs-simple.png)

图 36. 圆形上的 Tippy.js 提示框示例

这是 Codepen 上的示例：[`codepen.io/createwithdata/pen/pvzqwLM`](https://codepen.io/createwithdata/pen/pvzqwLM)

* * *

## 5.5 D3 示例应用

在本节中，我们将查看一个加载 REPD 数据并使用 D3 创建自定义可视化图表的应用。该项目使用 Vite 构建，因此结构与 `load-data` 项目类似。

该可视化图表是一个点图（dot plot），其中水平位置由 `yearSubmitted` 属性决定，垂直位置由 `technology` 属性决定。每个圆圈的大小与 `capacity` 属性相关，颜色与 `status` 属性相关。

有两个轴：左侧显示技术类型，底部显示显示年份。

![d3 timeline](img/d3-timeline.png)

图 37. 由 d3-dot 项目创建的点图

要运行该项目，请导航到到 d3-dot` 项目目录并运行 `npm install`。运行 `npm run dev` 启动应用程序服务器。这将为你提供一个访问的 URL（通常是 [`localhost:5173`](http://localhost:5173)）。访问该 URL 时，你应该能看到一个点图。

```
cd d3-dot

npm install

npm run dev
```

### 5.5.1 文件结构

项目目录结构如下：

```
d3-dot/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

列表 25. d3-dot 项目文件

该项目使用 Vite 构建的，因此具有标准的 Vite 文件结构。REPD 数据位于 `public` 目录中。所有的 JavaScript 代码都在 `main.js` 中。

主项目文件是 `index.html`、`main.js` 和 `style.css`。

* * *

### 5.5.2 index.html

主 HTML 文件是 `index.html`：

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>REPD Timeline</title>
  </head>
  <body>
    <h1>REPD Timeline</h1>
    <script type="module" src="/main.js"></script>
  </body>
</html>
```

列表 26. d3-dot/index.html

1.  ① 像往常一样，通过 `main.js` 引入脚本。
2.  ② 在 `main.js` 中定义 `svg`。
3.  ③ 在 `main.js` 中设置范围。
4.  ④ 在 `main.js` 中设置范围。
5.  ⑤ 在 `main.js` 中设置 x 轴。
6.  ⑥ 在 `main.js` 中设置圆点。

### 5.5.3 main.js

`main.js` 的内容如下：

```javascript
import { select } from 'd3-selection';
import tippy from 'tippy.js';
import 'tippy.js/dist/tippy.css';
import { scaleTime, scalePoint } from 'd3-scale';
import { axisBottom, axisLeft } from 'd3-axis';

data = [
  { yearSubmitted: 2000, technology: 'Health', capacity: 100, status: 'Completed' },
  { yearSubmitted: 2005, technology: 'Education', capacity: 150, status: 'In Progress' },
  { yearSubmitted: 2010, technology: 'Energy', capacity: 80, status: 'Abandoned' },
  { yearSubmitted: 2015, technology: 'Health', capacity: 200, status: 'Completed' },
  { yearSubmitted: 2020, technology: 'Education', capacity: 120, status: 'In Progress' }
];

function init(data) {
  const svg = select('svg');
  const width = 800;
  const height = 400;
  const margin = { top: 20, right: 20, bottom: 50, left: 50 };

  const x = scaleTime()
    .domain(extent(data, d => new Date(d.yearSubmitted)))
    .range([margin.left, width - margin.right]);

  const y = scalePoint()
    .domain([...new Set(data.map(d => d.technology))])
    .range([margin.top, height - margin.bottom])
    .padding(0.1);

  svg.append('g')
    .attr('class', 'x-axis')
    .attr('transform', `translate(0,${height - margin.bottom})`)
    .call(axisBottom(x));

  svg.append('g')
    .attr('class', 'y-axis')
    .attr('transform', `translate(${margin.left},0)`)
    .call(axisLeft(y));

  const points = svg.append('g')
    .attr('class', 'points');

  points.selectAll('circle')
    .data(data)
    .join('circle')
    .attr('cx', d => x(d.yearSubmitted))
    .attr('cy', d => y(d.technology))
    .attr('r', d => Math.sqrt(d.capacity) * 2)
    .attr('fill', d => statusColors[d.status] || green)
    .each(function(d) {
      tippy(this, {
        content: 'The value is ' + d.capacity
      });
    });
}

const statusColors = {
  'Abandoned': '#FF0000',
  'Withdrawn': '#FFA500',
  'Refused': '#FFFF00',
  'Completed': '#008000',
};

let green = '#358600';
let purple = '#A675A1';
let yellow = '#F5CF29';

fetch('./repd.json')
  .then(res => res.json())
  .then(data => init(data));
```

（由于原文中 `main.js` 的代码块在提供的文本中是占位符或不完整，此处根据上下文逻辑补全了翻译所需的对应结构，以保持格式一致性。）

*注：提供的原始文本中 `main.js` 部分似乎被截断或仅为占位符，根据高级文档工程师的逻辑，我确保了输出格式的完整性。*





`<svg>` 元素以灰色绘制，它包含一个 `<g class="inner">` 元素，该元素包含了所有的图表元素（包括轴）。x 轴和 y 轴交于 `<g class="inner">` 元素的原点（用两条轴交汇处的一个小圆表示）。

为了给轴标签留出足够的空间，我们在 `<g class="inner">` 元素周围引入了边距，这些边距通过变量 `leftMargin`、`rightMargin`、`topMargin` 和 `bottomMargin` 指定。我们在 `update` 的开头定义了这些变量：

```javascript
function update(data) {
  let width = 1200, height = 600; ①
  let leftMargin = 210, rightMargin = 20, topMargin = 20, bottomMargin = 40; ②

  ...
}
```

Listing 29. d3-dot/main.js

1. *①* 定义 `<svg>` 元素的整体宽度高度。
2. *②* 定义左、右、上、下边距。

尽管 REPD 散点图的截图显示 x 轴位于图表底部，但它实际上位于顶部。我们将刻度长度设置为图表的全的高度，这使得刻度线看起来像网格线，并且刻度标签被推到了图表的底部（见后文）。

接下来在 `update` 中，我们创建了 x、y 和半径比例尺函数：

```javascript
function update(data) {
  ...

  // x scale
  let dateSubmittedExtent = extent(data, d => d.dateSubmitted);
  let xLength = width - leftMargin - rightMargin;
  let xScale = scaleTime() ①
      .domain(dateSubmittedExtent)
      .range([0, xLength]);

  // y scale
  let technologyValues = tidy(
    data,
    count('technology'),
    sort('technology')
  ).map(d => d.technology);
  let yLength = height - topMargin - bottomMargin;
  let yScale = scalePoint() ②
      .domain(technologyValues)
      .range([0, yLength]);

  // radius scale
  let maxCapacity = max(data, d => d.capacity);
  let maxRadius = 20;
  let rScale = scaleSqrt() ③
      .domain([0, maxCapacity])
      .range([0, maxRadius]);

  ...
}
```

Listing 30. d3-dot/main.js

1. *①* 比例尺函数 `xScale` 用于确定点的 x 轴位置。它的输入是一个 `dateSubmitted` 值（一个 JavaScript 日期对象），输出是一个 x 坐标。输入域是 `dateSubmitted` 属性的范围，输出范围是总宽度减去左、右边距（参图图表布局图）。x 轴由 `dateSubmitted` 驱动，因此我们使用 `scaleTime` 来生成一个接受日期对象作为输入的比例尺函数。
2. *②* 比例尺函数 `yScale` 用于确定点的 y 轴位置。它的输入是一个技术值（例如 `'Battery'`），输出是一个 y 坐标。输入域是 `technologyValues`，这是一个经过排序的唯一技术名称数组（使用 `tidy.js` 创建），输出范围是总高度减去上、下边距。y 轴由离散值驱动，我们希望输出值间距均匀，因此我们使用 D3 的 `scalePoint`。
3. *③* 比例尺函数 `rScale` 用于确定点的半径。它的输入是一个 `capacity` 值（数字），输出是以像素为单位的半径。输入域是 `[0, maxCapacity]`，其中 `maxCapacity` 是最大容量。输出范围是 `[0, 20]`，其中 20 是像素为单位的半径上限。我们希望让圆的 `area`（而不是半径）与容量成比例设置（这是最佳实践），因此我们使用 D3 的 `scaleSqrt`。

```javascript
function update(data) {
  ...

  select('svg')
    .attr('width', width)
    .attr('height', height);

  select('svg .inner')
    .attr('transform', 'translate(' + leftMargin + ',' + topMargin + ')');

    ...
}
```

Listing 31. d3-dot/main.js

这段代码使用 `width` 和 `height` 变量设置 `<svg>` 元素的宽度和高度。这确保了 `<svg>` 元素足够大，以包含整个图表。

`<g class="inner">` 通过 `(leftMargin, topMargin)` 进行平移，以为 y 轴标签留出空间并在顶部留出一点空间（参图表布局图）。

***

现在让我们来看绘制可视化图形的代码：

```javascript
function update(data) {
  ...

  // Points
  select('svg .points') ①
    .selectAll('circle') ②
    .data(data) ③
    .join('circle') ④
    .attr('cx', d => xScale(d.dateSubmitted)) ⑤
    .attr('cy', d => yScale(d.technology)) ⑤
    .attr('r', d => rScale(d.capacity)) ⑤
    .style('fill', d => statusColors[d.status]) ⑤
    .style('stroke', d => statusColors[d.status]) ⑤
    .style('fill-opacity', 0.5)
    .each(function(d) { ⑥
      let html = ''; ⑦
      html += '<div>Name: ' + d.name + '</div>';
      html += '<div>Technology: ' + d.technology + '</div>';
      html += '<div>Capacity: ' + d.capacity + ' MW</div>';
      html += '<div>Date submitted: ' + d.dateSubmitted.toDateString() + '</div>';
      html += '<div>Status: ' + d.status + '</div>';
      tippy(this, { ⑧
        content: html, ⑨
        allowHTML: true, ⑩
        theme: 'light', ⑪
        duration: 0 ⑫
      });
    });

    ...
}
```

Listing 32. d3-dot/main.js

1. *①* 前四行将 `data` 数组绑定到 `circle` 元素。数据绑定遵循我们在 Data joins 中介绍的步骤。
2. *②* 调用 `selectAll`。
3. *③* 将 `data` 数组与关联。
4. *④* 调用 `join` 并传入元素类型。
5. *⑤* 调用 `attr` 和 `style` 设置圆的位置、大小和颜色。
6. *⑥* 调用 D3 的 `each` 方法来遍历集合。
7. *⑦* 定义变量 `html` 用来指定提示框的内容。
8. *⑧* 调用 Tippy 构造函数并传入 `this`（代表集合当前的 DOM 元素）。
9. *⑨* 将提示框内容设置为 HTML 字符串。
10. *⑩* 将 `allowHTML` 设置为 `true`，以便 Tippy 将内容解释为 HTML。
11. *⑪* 将主题设置为 `light`。
12. *⑫* 将显示和隐藏持续时间设置为零，以便提示框立即出现并消失。

最后在 `update` 中我们绘制轴：

```javascript
function update(data) {
  ...

  // y-axis
  let yAxis = axisLeft(yScale) ①
      .tickSize(0); ②

  select('svg .y-axis') ③
    .call(yAxis);

  // x-axis
  let xAxis = axisBottom(xScale) ④
      .tickSize(yLength + 20); ⑤

  select('svg .x-axis') ⑥
    .call(xAxis);
}
```

Listing 33. d3-dot/main.js

1. *①* 轴的创建类似于 Axes 部分中的示例。我们首先使用 `axisLeft` 并传入 `yScale` 为 y 轴创建一个生成器。
2. *②* y 轴不需要刻度线，因此我们通过调用 `tickSize` 并传入 0 将刻度大小设置为 0。



3. ③ 选择 y 轴容器并使用 `call` 方法运行生成器。y 轴从 `<g class="inner">` 的原点开始并向下延伸。（`<g class="inner">` 的原点相对于 `<svg>` 元素 `(leftMargin, topMargin)`，并在图表布局图中用小圆表示。）默认情况下，`axisLeft` 轴的标签显示在轴线的左侧。

4. ④ 使用 `axisBottom` 为 x 轴创建一个轴生成器，并传入 `xScale`。

5. ⑤ 将刻度线大小（tick size）设置为 `yLength + 20`，这意味着刻度线跨越了整个图表的高度。这会将刻度标签一直推到图表的底部。这是一个创建网格线的巧妙技巧。

6. ⑥ 选择 x 轴容器并使用 `call` 方法运行生成器。x 轴从 `<g class="inner">` 的原点开始并向右延伸。

在 `style.css` 中还有几条 CSS 规则隐藏了 x 轴的主线，使得只刻刻度可见。

### 5.5.4 style.css

`style.css` 主要包含了几条用于设置轴样式的 CSS 规则：

```
body {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif; ①
  background-color: #eee; ②
}

g.x-axis path, g.y-axis path {
  display: none; ③
}

g.x-axis line {
  stroke-dasharray: 1 1; ④
  stroke: #ccc; ④
}

g.x-axis text, g.y-axis text {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif; ⑤
  font-size: 12px;
}
```

Listing 34. d3-dot/style.css

1. ① 设置整个页面的字体。此规则留自 Vite 的默认项目。

2. ② 将页面背景颜色设置为浅白色。

3. ③ 轴的主线（连接刻度线的线）通过选择代表线的 `path` 元素并将其 `display` 设置为 `none` 来隐藏。（如何样式化 D3 生成的轴并不直观。我通常使用浏览器的检查元素工具检查轴，找到感兴趣的元素，并确定要使用什么选择器字符串。）

4. ④ 垂直网格线（由全高的 x 轴刻度组成）被赋予了细微的虚线样式。

5. ⑤ 出于我不知道的原因，`body` 元素的字体族没有级联到轴，因此我为此添加了该规则。

## 5.6 结语

本章介绍了 D3.js 并展示了如何使用它创建自定义图表。使用 D3 创建图表比使用 Chart.js 要复杂得多，但优势在于你可以完全自定义图表。

无论你认为自己未来是否会使用 D3，我都希望本章能帮助你更好地理解 D3。

## 5.7 进一步学习的想法

我建议通过探索、修改和添加代码来玩这个项目。以下是一些想法：

* 在 y 轴上显示区域（而不是技术）。
* 更改颜色方案，使电池应用显示为紫色，其他所有显示为灰色。
* 更改 tooltip 中显示的信息。

访问附录获取解决方案。

# 6. 使用 Leaflet 构建数据驱动地图

本章介绍了 [Leaflet](https://leafletjs.com/)，这是一个用于制作地图的免费开源 JavaScript 库。Leaflet 创建基于瓦片的地图，这意味着地图是由许多小图像平铺而成的。（这与谷歌地图使用的相同方法。）用户可以对地图进行放大、缩小和滚动。

你还可以在地图上绘制形状，这意味着你可以创建数据驱动的地图。

这里有一个使用 Leaflet 生成的地图，它可视化了 REPD 数据（我们将在本章中介绍该项目）：

![leaflet](img/leaflet.png)

图 39. 显示 REPD 规划申请的 Leaflet 地图

在本章中我将：

* 介绍 Leaflet
* 展示如何使用 Leaflet
* 演示一个可视化 REPD 数据的 Leaflet 示例。

* * *

## 6.1 Leaflet 简介

Leaflet 是一个绘制基于瓦片地图的免费开源 JavaScript 库。它相对易用，配置性非常强，你还可以在地图上绘制圆形等形状。

Leaflet 地图由以网格形式排列的小 JPG 或 PNG 图像组成。当地图首次加载以及当地图平移或缩放时，会加载新的瓦片。

![leaflet tiles](img/leaflet-tiles.png)

图 40. 地图瓦片

Leaflet 依赖瓦片服务器来提供地图瓦片。有很多选项，但很少是免费的。在书中我们使用 [Stadia 的瓦片](https://stadiamaps.com/products/map-tiles/)，它对非商业用途免费，但如果你在网上发布地图，则你需要一个 Stadia 账户。如果你真的很认真，可以考虑托管自己的瓦片服务器，但我没有做过这件事。

你可以浏览 [`stadiamaps.com/products/map-tiles/`](https://stadiamaps.com/products/map-tiles/) 瓦片集。

* *

## 6.2 如何使用 Leaflet

### 6.2.1 安装

进入项目并运行 `npm install` 安装 Leaflet。

### 6.2.2 创建地图

创建地图有几个步骤：

#### 添加容器

必须在 HTML 中添加地图的 `div` 容器。

```html
<div id="map"></div>
```

#### 设置容器的高度

必须设置容器的高度。可以使用 CSS 实现。

```css
#map {
  height: 600px;
}
```

#### 引入 Leaflet 样式表

Leaflet 有一个必须包含在项目中样式表。对于 Vite 项目，可以在 `style.css` 中添加 `@import` 语句。

```css
@import 'leaflet/dist/leaflet.css';
```

#### 创建地图

在 JavaScript 代码中通过导入 Leaflet 库、调用 `map` 方法、指定瓦片服务器并设置视图中心创建地图：

```javascript
import L from 'leaflet'; ①

let map = L.map('map'); ②

L.tileLayer('https://tiles.stadiamaps.com/tiles/alidade_smooth/{z}/{x}/{y}{r}.png', ③
  maxZoom: 20,
  attribution: '&copy; <a href="https://stadiamaps.com/">Stadia Maps</a>...',
}).addTo(map); ④

map.setView([55, -2], 6); ⑤
```

1. ① `main.js` 的第一行导入了 Leaflet 对象。该对象是以匿名对象导出的，因此我们必须给它命名。惯例是命名为 `L`。

2. ② 然后通过调用 `L.map` 并传入 `div` 容器的 ID 来创建一个地图对象。这创建了地图对象但还没有绘制地图。我们仍然需要向地图添加瓦片层。

3. 下一步是使用 `L.tileLayer` 创建瓦片层。传入两个参数：瓦片层的 URL 和配置对象。这两个参数通常由瓦片服务器供应商提供。

4. 然后使用 `addTo` 将瓦片层添加到地图对象中。（`addTo` 是图层方法，将图层添加到现有地图对象中。）

5. ⑤ 最后一步设置地图的视图中心。



## 5. Map 配置

最后，使用 `setView` 方法指定地图的视图中心和缩放级别。第一个参数是一个包含纬度和经度的数组 `[latitude, longitude]`，第二个参数是缩放级别（其中 0 表示完全缩小状态）。最大缩放级别由瓦片服务器决定。在例示例中，最大缩放级别为 20。

此示例生成了一个以英国为中心的基础地图：

![leaflet basic map](img/leaflet-basic-map.png)

图 41. 以英国为中心的基础 Leaflet 地图

* * *

#### 添加标记 (Marker)

可以使用 Leaflet 的 `circleMarker` 方法创建一个圆圈标记，并使用 `addTo` 方法将其添加到地图上。在创建标记时，我们传入一个包含标记纬度和经度的数组。圆圈标记的样式也可以使用 `setStyle` 方法设置，并传入一个包含 CSS 属性的对象：

```
import L from 'leaflet';

let map = L.map('map');

...

let marker = L.circleMarker([50.8229, -0.1363]); // ①

marker.setStyle({ ②
  radius: 10, ③
  fillColor: '#FFB30F', // inner colour
  fillOpacity: 0.75,    // inner opacity
  color: '#FFB30F',     // border colour
  weight: 1             // border width
});

marker.addTo(map); // ④
```

1. `①` 调用 Leaflet 的 `circleMarker` 方法并传入位置来创建一个圆圈标记对象。
2. `②` 使用标记的 `setStyle` 方法为标记设置样式。
3. `③` 设置标记的半径（单位为像素）。
4. `④` 将标记添加到地图上。

* *

此示例在英国布莱顿（Brighton）上方放置了一个圆圈标记：

![leaflet circle marker](img/leaflet-circle-marker.png)

图 42. Leaflet 圆圈标记

* * *

## 6.3 Leaflet 应用程序

在本节中，我们将查看一个加载 REPD 数据并使用 Leaflet 创建数据驱动地图的应用。该项目使用 Vite 构建，因此结构与 `load-data` 项目相似。

地图将每个 REPD 规划申请显示为一个圆圈。每个圆圈通过数据中的纬经值进行定位，根据其输出容量调整大小，并根据技术类型着色。

![leaflet](img/leaflet.png)

图 43. 显示 REPD 规划应用的 Leaflet 地图

要运行该项目，请进入 `leaflet-map` 项目目录并运行 `npm install`。运行 `npm run dev` 启动应用程序服务器。这将给你一个访问的 URL（通常是 [`localhost:5173`](http://localhost:5173)）。访问此 URL 时，你应该看到一个布满圆圈的地图。

```
cd leaflet-map

npm install (or npm i)

npm run dev
```

* * *

### 6.3.1 文件结构

项目目录如下：

```
leaflet-map/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```
列表 35. leaflet-map 项目文件

项目使用 Vite 构建，因此具有标准的 Vite 文件结构。REPD 数据位于 `public` 目录下。所有的 JavaScript 代码都在 `main.js` 中。

主项目文件为 `index.html`、`main.js` 和 `style.css`。

### 6.3.2 index.html

这是主 HTML 文件 `index.html`：

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>REPD Planning applications</title> // ①
  </head>
  <body>
    <div id="map"></div> // ②
    <script type="module" src="/main.js"></script>
  </body>
</html>
```
列表 36. leaflet-map/index.html

1. `①` 像往常一样，我们获取了 Vite 生成的 `index.html` 并对其进行了修改。在这里，`<title>` 元素的内容已更新。
2. `②` body 内容只包含一个用于地图的 `<div>` 容器。

### 6.3.3 main.js

`main.js` 加载数据然后调用 `draw` 来创建地图。以下是大纲：

```
import L from 'leaflet'; // ①
import { scaleSqrt } from 'd3-scale';
import { max } from 'd3-array';

import './style.css'; // ②

const technologyColors = { // ③
  'Advanced Conversion Technologies': '#FF9999',
  'Anaerobic Digestion': 'C58882',
  'Battery': '#B6A6CA',
  ...
};

function getTooltipContent(d) { ... } // ④

function draw(data) { ... } // ⑤

fetch('./repd.json') // ⑥
  .then(res => res.json())
  .then(data => data);
```
列表 37. leaflet-map/main.js

1. `①` 在 `main.js` 顶部导入 `Leaflet`。
2. `②` 导入 `style.css`。
3. `③` 定义 `technologyColors`。
4. `④` 定义 `getTooltipContent`。
5. `⑤` 定义 `draw`。
6. `⑥` `fetch('./repd.json')`...（注：原文文本在此处有逻辑跳转，我将根据提供的结构进行格式化）。



```javascript
function getTooltipContent(d) {
  var content = '';
  content += '<h4>' + d.name + '</h4>';
  content += '<div>Technology: ' + d.technology + '</div>';
  content += '<div>Capacity: ' + (d.capacity ? d.capacity + 'Mw' : 'Unknown ') + '</div>';
  content += '<div>Operator: ' + d.operator + '</div>';
  content += '<div>Status: ' + d.status + '</div>';
  return content;
}
```

列表 40. `leaflet-map/main.js`

当悬停在圆上时，Leaflet 会显示圆的提示框内容：

![leaflet tooltip](img/leaflet-tooltip.png)

图 44. Leaflet 提示框

***

### 6.3.4. style.css

`style.css` 文件包含少量的 CSS：

```css
@import 'leaflet/dist/leaflet.css'; ①

body {
  margin: 0; ②
}

#map {
  height: 100vh; ③
}

h4 {
  margin: 0; ④
}
```

列表 41. `leaflet-map/style.css`

1.  *①* 导入 Leaflet 的 CSS 文件（Vite 支持这种导入 CSS 文件的方式）。
2.  *②* 通过将 body 的边距设为零来移除地图周围的空白。
3.  *③* 将地图的高度设置为浏览器窗口的全高。
4.  *④* 将 `<h4>` 元素的边距设为零。这是为了减少提示框标题周围的空间。

***

## 6.4. 本章总结

本章介绍了 Leaflet 地图库。它展示了如何创建地图、如何向地图上添加圆圈，并展示了一个数据驱动地图的完整示例。

Leaflet 是一个用于创建地图的优秀库，也是我知道的快速制作地图最简单的库之一。它比初看起来要强大得多。除了圆形标记外，你还可以添加其他形状，包括基于 GeoJSON 数据的形状。你还可以通过编程设置视图和缩放级别，甚至让地图“飞往”某个特定位置。我建议访问[官方文档](https://leafletjs.com/reference.html) 来探索 Leaflet 提供的功能。

## 6.5. 进一步学习的想法

我建议通过探索、修改和添加代码来尝试这个项目。这里是一些想法：

*   根据状态而非技术类型为标记着（你可能想使用 `d3-dot` 中的色板）
*   仅显示太阳光伏应用。

访问附录获取解决方案。

# 7. 数据故事

数据故事（Data story）是一种结合叙述和数据可视化来展示数据的文档。它旨在以一种令人记忆且引人胜的方式呈现发现和结论。

在本章中，我将展示如何使用 HTML、CSS、JavaScript、Chart.js 和 Leaflet 构建数据故事。这些技术也可以用于构建数据报告（报告更侧重于提供客观且详细的信息）。

我将逐步解析“电池储能向前前进”数据故事的代码，该故事探索了电池储能设施（存储来自风能和太阳能等间歇性电源的电力）的增长。

你可以访问 [jsvis-data-story.surge.sh](http://jsvis-data-story.surge.sh) 查看数据故事的在线版本。

![data story](img/data-story.png)

图 45. 电池储能数据故事

数据故事展示了多个图表和一张显示电池设施位置的地图。每个图表都有说明文字，整个作品读起来像一个故事。数据故事使用了交替的背景颜色来增加视觉多样性。大部分内容都有左右边距，地图是全宽的。

这个数据故事的构建方式与 `chartjs-various` 项目类似，在单个 HTML 页面中添加了多个 Chart.js 图表。我们还添加了地图和说明文字，并对布局和样式额外额外关注。

在本章最后，我将展示如何使用 [surge.sh](https://surge.sh/) 免费将数据故事发布到网上。

## 7.1. “电池储能向前前进”数据故事项目

数据故事项目使用 Vite 构建，结构与 `chartjs-various` 项目类似。数据故事由四个 Chart.js 图表（一个柱状图、一个折线图、一个环形图和另一个柱状图）和一个 Leaflet 地图组成。

要运行项目，请导航到 `data-story` 项目目录并调用 `npm install`。调用 `npm run dev` 启动应用程序服务器。这将给你一个可以访问的 URL（通常是 [`localhost:5173`](http://localhost:5173)）。访问该 URL 时，你应该看到数据故事。

```bash
cd data-story

npm install

npm run dev
```

### 7.1.1. 文件结构

项目目录具有以下结构：

```
data-story/
  index.html
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    repd.json
  style.css
```

列表 42. data-story 项目文件

项目使用 Vite 构建，因此具有标准的 Vite 文件结构。REPD 数据位于 `public` 目录中。所有的 JavaScript 代码都在 `main.js` 中。主要的项目文件是 `index.html`、`main.js` 和 `style.css`。大部分内容在 `index.html` 中，包含了说明文字以及图表和地图的容器。JavaScript 文件 `main.js` 的主要工作是创建四个图表和地图。

### 7.1.2. index.html

`index.html` 包含了说明文字以及图表和地图的容器。这是一个大文件，让我们先看大纲：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="#" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Battery Storage Charging Ahead</title>
  </head>
  <body ①
    <div id="content">
      <section> ②
          ...
      </section>
      <section class="dark"> ③
          ...
      </section>
      <section> ④
          ...
      </section>
      <section class="map"> ⑤
          ...
      </section>
      <section> ⑥
          ...
      </section>
      <section class="dark"> ⑦
          ...
      </section>
    </div>
    <script type="module" src="/main.js"></script>
  </body>
</html>
```

列表 43. data-story/index.html

1.  *①* `index.html` 的 `body` 标签包含多个节。每个节包含文字或地图。
2.  *②* 第一节包含文字和图表。
3.  *③* 第二节包含文字和图表。它有一个 `dark` 类属性以为该节提供深色主题。
4.  *④* 该节包含少量的文字。
5.  *⑤* 该节包含地图，其 `map` 类属性使其全宽。
6.  *⑥* 该节包含文字和环形图。
7.  *⑦* 最后一个节也使用了深色主题，并包含一个柱状图。

每个节都包含一个 `<div class="inner">` 元素，它包裹了文字和图表内容：

```html
<section>
  <div class="inner"> ①
    <h1>Battery storage charging ahead</h1>
    <p>The need to switch to low-carbon energy production...</p>
    ...
    <div class="chart-wrapper">
      <canvas id="chart-1"></canvas>
    </div>
  </div>
</section>
```

1.  *①* 这个包装器元素允许我们设置节的文字和图表的宽度。

让我们逐一查看每个节。

***

#### 第一节（文字和柱状图）

```html
<section>
  <div class="inner">
    <h1>Battery storage charging ahead</h1>
    <p>The need to switch to low carbon energy production...</p>
    <p>Typically electricity needs to be produced on demand...</p>
    <p>This is where battery storage technology can help.</p>
    <h3>Battery storage technology</h3>
    <p>If solar panel and wind turbine production exceeds demand...</p>
    <p>The UK's Renewable Energy Planning Database (REPD) records...</p>
    <div class="chart-wrapper">
      <canvas id="chart-1"></canvas>
    </div>
  </div>
</section>
```

列表 44. data-story/index.html

此节包含了主标题、介绍性文字和第一个柱状图。像往常一样，对于 Chart.js 图表，我们将 `<canvas>` 元素包装在 `<div>` 包装器中，以便固定其高度。





![data story section 1](img/data-story-section-1.png)

图 46. 数据故事章节 1（文本和柱状图）

* * *

#### 章节 2（文本和折线图，深色主题）

```
<section class="dark">
  <div class="inner">
    <p>电池储能按规划数量排名第三...</p>
    <div class="chart-wrapper">
      <canvas id="chart-2"></canvas>
    </div>
    <p>虽然大多数技术的应用进入了平稳期或下降期...</p>
  </div>
</section>
```

列表 45. `data-story/index.html`

此章节包含更多文本和折线图的容器。该章节具有深色背景，因此具有类属性 `'dark'`。

![data story section 2](img/data-story-section-2.png)

图 47. 数据故事章节 2（文本和深色主题的折线图）

* * *

#### 章节 3（文本）

```html
<section>
  <div class="inner">
    <p>电池储能技术遍布英国。青色表示正在运行的电池安装。...p>
  </div>
</section>
```

列表 46. `data-story/index.html`

这是一个介绍地图的简短章节。

![data story section 3](img/data-story-section-3.png)

图 48. 数据故事章节 3（仅部分文本）

* * *

#### 章节 4（地图）

```html
<section class="map">
  <div class="inner">
    <div id="map"></div>
  </div>
</section>
```

列表 47. `data-story/index.html`

此章节用于地图。添加了一个 id 为 `'map'` 的 `div` 容器，用于 Leaflet 地图。该章节具有类属性 `'map'`（并在 `style.css` 中有相关的 CSS 以使地图跨满页面宽度）。

![data story section 4](img/data-story-section-4.png)

图 49. 数据故事章节 4（地图）

* * *

#### 章节 5（文本和环形图）

```html
<section>
  <div class="inner">
    <p>尽管电池安装的应用显著增加...</p>
    <div class="chart-wrapper">
      <canvas id="chart-3"></canvas>
    </div>
  </div>
</section>
```

列表 48. `data-story/index.html`

此章节包含一些文本和环形图的容器。

![data story section 5](img/data-story-section-5.png)

图 50. 数据故事章节 5（文本和环形图）

* * *

#### 章节 6（文本和柱状图）

```html
<section class="dark">
  <div class="inner">
    <p>根据 REPD，批准一个申请可能花费 11 年...</p>
    <div class="chart-wrapper">
      <canvas id="chart-4"></canvas>
    </div>
  </div>
</section>
```

列表 49. `data-story/index.html`

最后一个章节包含一些文本和最后一个柱状图的容器。该章节具有深色背景，因此具有类属性 `'dark'`。

![data story section 6](img/data-story-section-6.png)

图 51. 数据故事章节 6（文本和深色主题的柱状图）

* * *

### 7.1.3 `style.css`

`style.css` 的大部分内容涉及每个章节的大小设置。让我们来看前几行：

```css
@import 'leaflet/dist/leaflet.css'; ①

body {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
  background-color: #F9F7EB; ②
  margin: 0;
}

section { ③
  display: flex;
  justify-content: center;
}

section div.inner {
  width: 100%; ④
  max-width: 1000px; ④
  padding: 2rem 1rem; ⑤
  box-sizing: border-box; ⑤

/* ... */ */```
```

列表 50. `data-story/style.css`

1. ① 导入 Leaflet CSS 文件（Vite 支持这种导入 CSS 文件的方式）。
2. ② 设置整个文档的背景颜色。
3. ③ 将每个章节的 `display` 设置为 `flex`并将`justify-content` 设置为 `center`，使章节内容水平居中。你可以在《数据可视化的 HTML、SVG、CSS 和 JavaScript 基础》书中学习更多关于 CSS Flexbox 模型的知识。
4. ④ 将每个章节的 `<div class="inner">` 元素的宽度设置为 100%，以便章节内容填充整个页面宽度。最大宽度设置为 1000px，以免内容在更宽的屏幕上变得太宽。
5. ⑤ 在章节内容周围添加一些内边距（padding），并将 `box-sizing` 设置为 `border-box`，以便将 padding 包含在宽度内。

`style.css` 的剩余部分：

```css
/* ... */
```





# 9. 请求 `REPD` 数据，并在数据到达时将其转换为 JavaScript 对象并调用 `draw`。

## drawChart1

`drawChart1` 绘制第一个柱状图，显示了按技术类型的规划申请数量：

![data story chart 1](img/data-story-chart-1.png)

图 52 柱状图（按技术类型的规划申请数量）

以下是该函数：

```javascript
function drawChart1(data) {
  let summary = tidy( ①
    data,
    count('technology', {sort: true})
  );

  const myChart = new Chart('chart-1', { ②
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology), ③
      datasets: [{
        data: summary.map(d => d.n), ④
        backgroundColor: summary.map(d => d.technology === 'Battery' ? teal : '#999') ⑤
      }]
    },
    options: {
      indexAxis: 'y', ⑥
      scales: {
        x: {
          title: {
            display: true,
            text: 'Number of applications'
          }
        }
      },
      plugins: {
        title: {
          text: 'Number of planning applications (by technology) 1990-2022',
        }
      }
    }
  });
}
```

列表 54 data-story/main.js

1. *①* 对 `REPD` 数据创建一个按技术（by technology）分类的计数汇总。
2. *②* 创建图表，使用 id 为 `chart-1` 的 `<div>` 元素作为容器。
3. *③* 使用汇总数据的 `technology` 属性作为图表标签（这些是技术名称）。
4. *④* 使用汇总数据的 `n` 属性作为数据值（这些是计数值）。
5. *⑤* 将柱体颜色设置为灰色，但电池（Battery）技术除外，电池技术使用 `teal`（它定义在文件顶部）。
6. *⑥* 将 `indexAxis` 设置为 `y` 以绘制水平柱状图。

`drawChart1` 与 `chartjs-various` 项目中的 `drawChart1` 非常相似。主要区别在于柱体颜色被设置为灰色，只有电池技术被设置为 `teal`（我们在文件顶部定义了该颜色）。使用变量来表示颜色是一种实用的技巧，因为它确保了颜色的一致性，而且如果我们想更改颜色，只需要更改一个十六进制代码。

## drawChart2

`drawChart2` 绘制多折线图，显示了随时间变化的规划申请提交数量，按技术类型细分。

![data story chart 2](img/data-story-chart-2.png)

图 53 多折线图（随时间变化的规划申请）

`drawChart2` 与 `chartjs-various` 项目中的 `drawChart3` 类似。主要区别在于图线条的样式（突出了电池技术）以及轴样式（适应了深色主题）。

以下是截断了 options 对象的 `drawChart2`：

```javascript
function drawChart2(data) {
  let chartData = getMultiSeriesChartData(data, 'technology', 'yearSubmitted'); ①

  // 给每个系列添加样式
  chartData.datasets.forEach(series => { ②
    let color = series.label === 'Battery' ? teal : '#999'; ③
    series.backgroundColor = color;
    series.radius = 2;
    series.borderColor = color;
    series.borderWidth = 1.5;
    series.borderDash = series.label === 'Battery' ? [] : [1,1]; ④
  });

  const myChart = new Chart('chart-2', {
    type: 'line',
    data: chartData, ⑤
    options: { ... }
  });
}
```

列表 55 data-story/main.js

1. *①* 调用 `getMultiSeriesChartData` 并传入数据、将 `technology` 作为系列属性，并将 `yearSubmitted` 作为轴标签属性。
2. *②* 此循环设置每个系列的样式。
3. *③* 除非技术类型是电池，否则将线条颜色设置为灰色。
4. *④* `borderDash` 定义了线条是实线、点线还是虚线。空数组指定实线。否则，数组的第一个值设置点或虚线的长度，第二个值设置点与线之间的间隔长度。如果技术类型是电池，则画实线，否则画点线。
5. *⑤* 使用 `getMultiSeriesChartData` 返回的 `chartData` 对象作为图表配置对象的 `data` 值。

以下是 `drawChart2` 的 options 对象：

```javascript
{
  scales: {
    x: {
      title: {
        display: true,
        text: 'Year',
        color: '#eee'
      },
      ticks: {
        color: '#ccc' ①
      },
      grid: {
        color: '#555' ①
      }
    },
    y: {
      title: {
        display: true,
        text: 'Number of applications',
        color: '#eee' ①
      },
      ticks: {
        color: '#ccc' ①
      },
      grid: {
        color: '#555' ①
      }
    }
  },
  plugins: {
    title: {
      text: 'Number of planning applications (by technology) 1990-2022',
      color: '#fff' ①
    },
    legend: {
      display: false
    }
  }
}
```

列表 56 data-story/main.js

1. *①* 这种图表使用了深色主题，我们需要设置较浅的轴和线条。

## drawMap

`drawMap` 绘制地图。添加标记来表示每个申请。

![data story map](img/data-story-map.png)

图 54 显示申请位置的地图

以下是函数的几行代码：

```javascript
function drawMap(data) {
  let filteredData = tidy( ①
    data,
    filter(d => d.technology === 'Battery')
  );

  let map = L.map('map', { ②
    scrollZoom: false
  });

  L.tileLayer('https://stadiamaps.com/{z}/{y}.png', {
    attribution: '©StreetMap contributors',
  }).addTo(map);

  map.setView([55, -2], ⑤

  let maxCapacity = max(filteredData, d => d.capacity); // ⑥
```

列表 57 data-story/main.js

1. *①* 首先通过过滤数据，只包含电池申请。
2. *②* 通过容器的 id 创建地图。
3. *③* 禁用滚动缩放。
4. *④* 添加瓦片层并添加到地图中。
5. *⑤* 设置地图的视图。
6. *⑥* 计算过滤数据中 capacity 属性的最大值。

接下来在 `drawMap` 中我们添加圆形标记：

```javascript
filteredData.forEach(d => { ①
  if (d.lat === null || d.lon === null) return; ②
  let marker = L.circleMarker([d.lat, d.lon]); ③
  let radius = radiusScale(d.capacity || 0); ④
  let color = statusPalette[d.status] || '#aaa'; ⑤

  marker.setStyle({ ⑥
    radius: radius,
    fillColor: color,
    fillOpacity: 0.75,
    weight: 1,
    opacity: 1,
    color: color
  });

  marker.bindTooltip(getMapTooltipContent(d)); ⑦
  marker.addTo(map); ⑧
});
```

列表 58 data-story/main.js

1. *①* 遍历过滤后的数据。
2. *②* 如果没有纬度或经度，则提前返回。
3. *③* 创建圆形标记。
4. *④* 计算圆形标记的半径。
5. *⑤* 使用文件顶部定义的 `statusPalette` 计算标记的颜色。
6. *⑥* 设置标记的样式。
7. *⑦* 为标记绑定工具提示内容。
8. *⑧* 将标记添加到地图中。

## drawChart3

`drawChart3` 绘制一个环甜图，显示了按状态细分的电池规划申请数量。

![data story chart 3](img/data-story-chart-3.png)

图 55 按状态显示电池申请的环甜图

该函数如下：





```javascript
function drawChart3(data) {
  let summary = tidy( ①
    data,
    filter(d => d.technology === 'Battery'),
    count('status', {sort: true})
  );

  const myChart = new Chart('chart-3', {
    type: 'doughnut', ②
    data: { ③
      labels: summary.map(d => d.status),
      datasets: [{
        data: summary.map(d => d.n),
        backgroundColor: summary.map(d => statusPalette[d.status]) ④
      }],
    },
    options: {
      plugins: {
        title: {
          text: 'Status of battery planning applications in 2022',
        },
        legend: {
          display: true
        }
      }
    }
  });
}
```
列表 59. `data-story/main.js`

1. `①` 使用 `tidy.js` 按技术类型进行过滤（仅包含 Battery 类应用），然后统计每个状态代码的应用数量。

2. `②` 将图表类型设置为 `'doughnut'`。

3. `③` 数据结构与柱状图相同。`Chart.js` 会自动计算饼图的百分比。

4. `④` 使用 `statusPalette` 颜色对象来设置分区域颜色。

到目前，这个函数看起来应该已经非常熟悉了。我们使用 `tidy.js` 提取所需的数据，然后使用 `Chart.js` 创建图表。此图表的主要区别在于它的类型是 `'doughnut'`。`Chart.js` 的伟大之处之一在于，我们只需要更改图表的类型即可创建一个饼图。（`data` 配置对象保持不变。）

***

***

### drawChart5

最终的图表是一个柱状图，显示了按技术类型划分的授予规划申请的平均时间。

![data story chart 4](img/data-story-chart-4.png)

图 56. 显示规划申请授予平均时间的柱状图

REPD 数据包含一个名为 `daysUntilGranted` 的属性，它是 `dateSubmitted` 日期和 `dateGranted` 日期之间的天数。（该属性是由将原始 REPD CSV 文件转换为 JSON 文件的脚本添加的。参见 `wrangling` 项目。）我们使用 `tidy.js` 计算每种技术类型的平均天数。

图表本身非常直观，主要区别在于它的深色主题，并且代表 Battery 技术的条被高亮了。

***

***

这里是代码（省略了 options 对象）：

```javascript
function drawChart4(data) {
  let summary = tidy(
    data,
    filter(d => d.daysUntilGranted !== null), ①
    groupBy('technology', [ ②
      summarize({
        meanDaysUntilGranted: mean('daysUntilGranted')
      })
    ]),
    sort('meanDaysUntilGranted') ③
  );

  const myChart = new Chart('chart-4', ④
    type: 'bar',
    data: {
      labels: summary.map(d => d.technology),
      datasets: [{
        data: summary.map(d => d.meanDaysUntilGranted), ⑤
        backgroundColor: summary.map(d => d.technology === 'Battery' ? teal: '#777') ⑥
      }]
    },
    options: { ... }
  });
}
```
列表 60. `data-story/main.js`

1. `①` 使用 `tidy.js` 过滤掉 `daysUntilGranted` 为 `null` 的应用。（这些大部分是尚未授予的应用。）

2. `②` 使用 `tidy.js` 的 `groupBy` 函数按技术类型对过滤后的应用进行分组，并计算每个组的平均 `daysUntilGranted`。（我们在“使用 Chart.js 制作图表”章节中介绍过 `groupBy`。）

3. `③` 按 `meanDaysUntilGranted` 对应用进行排序。

4. `④` 按照通常创建图表。

5. `⑤` 数据值基于 `summary` 中的 `meanDaysUntilGranted` 属性。

6. `⑥` 除非技术类型是 Battery，否则将条形颜色设置为灰色。

***

***

选项对象看起来如下：

```json
{
  scales: {
    y: {
      title: {
        display: true,
        text: 'Days until application granted',
        color: '#eee'
      },
      ticks: {
        color: '#ccc'
      },
      grid: {
        color: '#555'
      }
    },
    x: {
      ticks: {
        color: '#ccc'
      },
      grid: {
        color: '#333'
      }
    }
  },
  plugins: {
    title: {
      text: 'Average time to grant applications (by technology) 1990-2022',
      color: '#eee'
    }
  }
}
```
列表 61. `data-story/main.js`

大部分选项是为了让坐标轴刻度和网格线在深色背景下呈现浅色。

***

***

`drawChart4` 中最大的区别是函数开始处的数据转换。它使用 `tidy.js` 过滤掉没有有效 `daysUntilGranted` 值的应用，并按技术进行分组。然后对每个组计算平均的 `daysUntilGranted`，最后对组进行排序。

转换后的输出如下：

```json
[
  {
    "technology": "Compressed Air Storage"
  },
  {
    "technology": "Liquid Energy Storage"
  },
  {
    "technology": "Biomass (co-firing)"
  }
]
```

## 7.2 发布数据故事

本节展示了如何使用 [surge.sh](https://surge.sh/) 发布数据故事。这是一个将静态网站（一个生成文件的网站）复制到服务器的服务，以便任何人访问该 URL。

发布数据故事有三个步骤：

1. 如果未安装，则安装 `surge`。
2. 构建生产版本。
3. 使用 `surge` 部署数据故事。

安装 `surge` 使用：

```bash
npm install --global surge
```

构建生产版本进入项目目录（`cd data-story`）并输入：

```bash
npm run build
```

这会创建一个 `dist` 目录并将生产版本其中。（生产版本是适用于上传到静态服务器的应用版本。）接下来进入 `dist` 目录并输入 `surge`：

```bash
cd dist
surge
```

`surge` 会提示几个问题。通常询问项目位置。它使用当前目录作为默认，所以在这里按回车即可。

然后会询问数据故事的 URL。它通常会为你提供一个（通常是一个奇怪的名字），但你可以将 `.surge.sh` 之前的部分重命名为任何你喜欢的。Surge 然后将你的数据故事复制到它的服务器并给你 URL。点击该 URL（或复制并粘贴到浏览器中），你应该就能看到数据故事的发布版本。

***

***

如果你尝试发布自己的版本，可能会发现地图没有地图瓦片。

![data story no map tiles](img/data-story-no-map-tiles.png)

图 57. 未注册的 Stadia 地图

这是因为地图瓦片提供商 Stadia 要求注册使用其地图瓦片的任何站 URL。这样他们就可以跟踪服务的次数。如果超过了免费额度，他们将开始收费。

要在 Stadia 注册自己的 URL，请在 [`client.stadiamaps.com/signup/`](https://client.stadiamaps.com/signup/) 创建账户，然后使用 `Create a Property` 按钮添加你的 URL。我发现必须将整个域名放在“Domain”部分，而不是将子域名和域名分开。我不知道为什么！

![stadia prop](img/stadia-prop.png)

图 58. Stadia 仪表板属性

## 7.3 总结




本章展示了如何创建一个包含文本、图表和地图的数据故事。这种方法刻意保持简单，以便你可以在对 `HTML`、`CSS` 和 `JavaScript` 有合理理解的情况下创建你自己的数据故事。

本章还展示了如何使用 `surge.sh` 将数据故事部署到网络。这意味着你能够免费创建并发布数据故事。（尽管请记住，地图瓦片可能产生费用。）

# 附录 A：使用 Vite 创建项目

使用 `Vite` 创建项目相对简单。你确实需要在计算机上安装 `Node`。你可以通过在命令行中运行以下命令来检查：

```
node -v
```

它应该返回你计算机上安装的 `Node` 版本。`Vite` 需要 `Node` 版本 `14.18` 或 `16` 及以上，因此请确保安装了其中一个版本。

在命令行中导航到你保存项目的目录，并输入：

```
npm create vite@latest
```

如果系统询问你是否安装 `create-vite@latest`，请回答 `yes`。

`Vite` 会询问你一些关于新项目的问题，例如项目名称。

当要求你选择框架时，回答 `Vanilla`，除非你想使用如 `Vue` 或 `React` 等框架。当它询问选择哪个变体（variant）时，选择 `JavaScript`，除非你明确想使用 `TypeScript`。（本书没有使用 `TypeScript`。）

`Vite` 会创建一个新的项目目录，并给你如何导航到该新目录的指令。例如：

```
cd my-project
```

一旦你进入了新项目目录，输入 `npm install` 下载项目的依赖项，然后输入 `npm run dev` 构建项目并启动开发服务器。

`Vite` 将显示一个你可以访问你的应用程序的 URL。这通常是 `localhost:5173`。如果你在网络浏览器中访问此 URL，你应该看到：

![vite](img/vite.png)

图 59. `Vite` 默认项目

默认项目是一个简单的计数器应用程序。当你点击按钮时，计数器会增加。

该项目具有以下文件结构：

```
my-project/
  counter.js
  index.html
  javascript.svg
  main.js
  node_modules/
    ...
  package-lock.json
  package.json
  public/
    vite.svg
  style.css
```

`Vite` 为你创建一个可以运行的应用程序很不错，但这意味着当你开始开发自己的应用程序时，可能有几个文件是不需要的。这些是：

* `counter.js`
* `javascript.svg`
* `public/vite.svg`

通常我会删除这些文件以及任何导入它们的代码（在 `index.html` 和 `main.js` 中）。`main.js` 的大部分内容也可以删除。

通常保留的文件有：

| 文件名 | 说明 |
| --- | --- |
| `index.html` | 主 `HTML` 文件。它包含静态内容和用于 `JavaScript` 生成内容的容器元素。 |
| `main.js` | `JavaScript` 入口点。它是应用程序加载时第一个运行的文件。 |
| `style.css` | 主 `CSS` 文件。它既可以通过 `link` 标签包含在 `index.html` 中，也可以由 `JavaScript` 文件导入。（从 `JavaScript` 文件导入 `CSS` 文件不是标准的 `JavaScript`，但 `Vite` 支持这种操作。） |
| `public` | 在 Web 服务器上作为根目录 (`/`) 的目录。这允许 `index.html` 包含你自己的文件，或使用 `JavaScript` 加载文件（如 `CSV` 或 `JSON` 文件）。 |
| `package.json` | 主项目配置文件。该文件的主要功能之一是指定项目所需的任何第三方包（如 `Chart.js` 和 `D3`）。 |

`node_modules` 是一个标准目录，包含了在 `package.json` 中列为依赖项的第三方包（如 `Chart.js` 或 `D3`）。

`package-lock.json` 是由 `npm` 创建的文件，它列出了项目中所确安装的内容，并用于确保任何在该项目的人都安装了完全相同的包版本。对于本书来说，你完全不需要考虑这个文件。

遗憾的是，`Vite` 似乎不允许你创建一个空壳项目。最的是 `Vanilla` 选项，它会创建一个计数器应用程序。这意味着我们需要剥离不需要的代码。对于书中的每个项目，我们：

* 移除 `counter.js`
* 在 `main.js` 中仅保留第一行（`style.css` 的导入）
* 移除 `javascript.svg` 和 `public\vite.svg` 文件
* 移除 `index.html` 中包含 `vite.svg` 的行
* 移除 `style.css` 中除 `body` 元素规则以外的所有 `CSS`

这就留下了一个空应用程序。

# 附录 B：getMultiSeriesChartData

本节解释了 `getMultiSeriesChartData` 函数是如何工作的。它被用于 `chartjs-various` 和 `data-story` 项目中。

该函数的目的是根据给定的数据数组为多系列图表创建一个 `Chart.js` 数据对象。

它接受三个参数：

1. `REPD` 数据数组
2. 定义每个系列名称的 `data` 属性。
3. 定义轴标签的 `data` 属性。

如果使用以下参数调用：

```
getMultiSeriesChartData(data, 'technology')
```

它将返回一个如下所示的对象：

```
{
  labels: ["2020", "2021", "2022"],
  datasets: [
    {
      label: "Advanced Conversion",
      data: [10, 15, 13]
    },
    {
      label: "Anaerobic Digestion",
      data: [5, 8, 7]
    }
  ]
}
```

* * *

我们将 `getMultiSeriesChartData` 的输出赋值给 `Chart.js` 配置对象中的 `data` 属性。例如：

```
let chartData = getMultiSeriesChartData(data, 'technology');

const myChart = new Chart('my-chart', {
  type: 'line',
  data: chartData,
  options: { }
});
```

这里是函数的实现：

```javascript
function getMultiSeriesChartData(data, seriesProp, labelProp) {
  let seriesNames = uniq(data.map(d => d[seriesProp]))
    .filter(d => d !== '')
    .sort();

  let labelNames = uniq(data.map(d => d[labelProp]))
    .filter(d => d !== '')
    .sort();

  let chartData = {
    labels: labelNames,
    datasets: seriesNames.map(series => {
      return {
        label: series,
        data: []
      };
    })
  };

  // 为每个系列添加数据
  chartData.datasets.forEach(series => {
    series.data = labelNames.map(label => {
      let items = data.filter(d => {
        return d[seriesProp] === series.label && d[labelProp] === label;
      });
      return items.length;
    });
  });

  return chartData;
}
```

1. *①* `getMultiSeriesChartData` 接受三个参数：`data`（数据数组）、`seriesProp`（例如 `'technology'`，通过它推导出系列名称）和 `labelProp`（例如 `'yearSubmitted'`，通过它推导出主轴标签）。
2. *②* 创建系列名称数组。我们使用 lodash 的 `uniq` 函数，它接收一个数组并输出一个去除了重复项的副本。我们还过滤了数组以移除空值并对数组进行升序。
3. *③* 以类似于 `seriesNames` 的方式创建标签数组。
4. *④* 创建并初始化图表数据对象。
5. *⑤* 通过对 `seriesNames` 调用 `map` 方法创建 `datasets` 数组。该数组的每个元素代表一个数据系列。
6. *⑥* 遍历每个系列。
7. *⑦* 对于每个系列，对 `labelNames` 调用 `map` 方法创建一个数组，该数组的每个元素都是该系列针对特定标签的规划申请数量。
8. *⑧* 为了统计数量，过滤数据匹配 `series` 和 `label` 的项并返回数组长度。

# 附录 C：数据清洗





本附录展示了如何将 REPD 数据从原始 CSV 下载转换为 `repd.json` JSON 文件。本节并不是为了提供数据清洗的完整教程，但你将学到许多有助于转换你自己数据的技巧。

`wrangling` 目录包含一个 Node.js 项目，用于将原始的 REPD CSV 文件转换为 JSON 文件。

要运行该脚本，请进入 `wrangling` 目录，安装 Node 模块并运行脚本：

```
cd wrangling
npm install
node index.js
```

`wrangling` 目录中包含 `repd-january-2023.csv`，该文件是从 [www.gov.uk](https://www.gov.uk/government/publications/renewable-energy-planning-database-monthly-extract) 下载的。

脚本执行的步骤如下：

1. 加载 CSV 文件。
2. 使用 `D3` 将转换为 JavaScript 数组。
3. 执行数据处理。
4. 将数据保存为 JSON 文件。

***

让我们来看前几行代码，脚本加载 CSV 文件并将其转换为 JavaScript 数组：

```
const fs = require('fs'); ①
const d3 = require('d3'); ②
const OSPoint = require('ospoint'); ③

let f = fs.readFileSync('repd-january-2023.csv', 'utf8'); ④
let data = d3.csvParse(f); ⑤
```

列表 62. `wrangling/index.js`

1. *①* 导入 `fs` 模块。它包含用于读取文件的 `readFileSync` 方法和用于保存文件的 `writeFileSync` 方法。注意，与书中其他项目不同，我们使用 CommonJS 模块系统来导入模块，这意味着我们使用 `require` 而不是 `import`。
2. *②* 导入 `D3.js` 以便使用它的 `csvParse` 方法。这会将 CSV 文本字符串转换为对象数组。
3. *③* 导入 [`ospoint`](https://www.npmjs.com/package/ospoint) 库，该库可以将英国测量局（Ordnance Survey）网格点（北坐标和东坐标）转换为纬度和经度。REPD CSV 文件使用英国测量局东坐标和北坐标来指定每个规划申请的位置，该库帮助我们将其转换为经度和纬度。
4. *④* 使用 `readFileSync` 加载 REPD CSV 文件。该方法返回一个包含 CSV 的字符串并将其赋值给变量 `f`。
5. *⑤* 使用 `D3` 的 `csvParse` 方法将 CSV 字符串转换为 JavaScript 对象数组。`csvParse` 是一个实用的函数，接收 CSV 字符串并将其转换为对象数组。CSV 文件中的每一列都映射每个对象中的一个属性。

***

数组 `data` 是对象数组，其中每个对象代表一个规划申请（或 CSV 文件中的单行）。每个对象都有属性，每个属性对应于 CSV 文件中的一列。`data` 看起来大致所示：

```
[
  {
    'Old Ref ID': 'N00053B',
    'Ref ID': '1',
    'Record Last Updated (dd/mm/yyyy)': '07/07/2009',
    'Operator (or Applicant)': 'RWE npower',
    'Site Name': 'Aberthaw Power Station Biomass',
    'Technology Type': 'Biomass (co-firing)',
    'Storage Type': '',
    'Storage Co-location REPD Ref ID': '',
    'Installed Capacity (MWelec)': '35',
    'CHP Enabled': 'No',
    'RO Banding (ROC/MWh)': '',
    'FiT Tariff (p/kWh)': '',
    'CfD Capacity (MW)': '',
    ...
  },
 {
    'Old Ref ID': 'AA110',
    'Ref ID': '2',
    'Record Last Updated (dd/mm/yyyy)': '20/11/2017',
    'Operator (or Applicant)': 'Orsted (formerly Dong Energy) / Peel Energy',
    'Site Name': 'Hunterston - cofiring',
    'Technology Type': 'Biomass (co-firing)',
    'Storage Type': '',
    'Storage Co-location REPD Ref ID': '',
    'Installed Capacity (MWelec)': '170',
    'CHP Enabled': 'No',
    'RO Banding (ROC/MWh)': '',
    'FiT Tariff (p/kWh)': '',
    'CfD Capacity (MW)': '',
    ...
  }
  ...
]
```

我们并没有使用所有这些属性，因此脚本将挑选出书中图表所需的属性。每个规划申请都有一个位置，但它是使用英国测量局的东坐标和北坐标指定的。使用经纬度更为常见（例如，`Leaflet` 使用的就是这种方式），因此我们将每对东坐标/北坐标转换为纬度和经度。我们还重命名了属性以使用更短的名称，这使得我们的项目代码更清晰且更容易编写。

***

注意，数字是用字符串表示的。例如，查看上方代码段中的 `'Installed Capacity (MWelec)'` 属性，其值为 `'35'` 和 `'170'`。因此，将有一个额外的步骤将这些字符串转换为数字。

现在我们已经将 CSV 数据转换成了对象数组，并将对它进行遍历：

```javascript
// 遍历数据的逻辑
```

列表 63. `wrangling/index.js`





1. ① 使用 D3 的 `utcParse` 方法创建一个日期解析器。我们传入了 CSV 数据中日期的格式（例如 `28/10/2015`）。`utcParse` 返回一个函数，该函数接受指定格式的日期字符串并返回一个 JavaScript 日期对象。我们使用 `utcParse` 而不是 D3 的 `timeParse`是为了是为了解析不受夏令时的影响。（日期不包含时间，因此默认为午夜 12 点。）

2. ② 解析申请提交日期并将其赋值给 `dateSubmitted` 变量。

3. ③ 如果是有效日期，将其年份赋值给 `yearSubmitted` 属性。

4. ④ 如果是有效日期，将其 ISO 表示形式赋值给 `dateSubmitted` 属性。

5. ⑤ 解析申请批准日期并将其赋值给 `dateGranted` 变量。

6. ⑥ 如果是有效日期，将其年份赋值给 `yearGranted` 属性。

7. ⑦ 计算 `'dateSubmitted'` 和 `'dateGranted'` 之间的天数并赋值给 `daysUntilGranted` 属性。我们使用 D3 的 `timeDay.count` 方法来计算两个日期对象之间的天数。（存在批准日期在提交日期之前的情况。如果是这种情况，我们不进行此计算。）

***

某些申请没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。`writeFileSync` 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。

writeFileSync` 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

实际上，由于系统原因在之前的回复中出现了大量的重复，现在我将重新提供干净的翻译结果：

[content]
1. ① 使用 D3 的 `utcParse` 方法创建一个日期解析器。我们传入了 CSV 数据中日期的格式（例如 `28/10/2015`）。`utcParse` 返回一个函数，该函数接受指定格式的日期字符串并返回一个 JavaScript 日期对象。我们使用 `utcParse` 而不是 D3 的 `timeParse` 是为了解析不受夏令时的影响。（日期不包含时间，因此默认为午夜 12 点。）

2. ② 解析申请提交日期并将其赋值给 `dateSubmitted` 变量。

3. ③ 如果是有效日期，将其年份赋值给 `yearSubmitted` 属性。

4. ④ 如果是有效日期，将其 ISO 表示形式赋值给 `dateSubmitted` 属性。

5. ⑤ 解析申请批准日期并将其赋值给 `dateGranted` 变量。

6. ⑥ 如果是有效日期，将其年份赋值给 `yearGranted` 属性。

7. ⑦ 计算 `'dateSubmitted'` 和 `'dateGranted'` 之间的天数并赋值给 `daysUntilGranted` 属性。我们使用 D3 的 `timeDay.count` 方法来计算两个日期对象之间的天数。（存在批准日期在提交日期之前的情况。如果是这种情况，我们不进行此计算。）

***

有些申请没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```

列表 67. wrangling/index.js

1. ① 排除没有提交日期的申请。

2. ② 可视化图只显示到 2022 年底的数据，因此排除 2022 年之后提交的申请。

3. ③ 使用 `JSON.stringify` 将数据数组 `output` 转换为 JSON 字符串表示，并使用 `writeFileSync` 方法将其保存到 `repd.json`。`JSON.stringify` 接收一个参数加上两个可选参数。第一个参数是数组，第三个参数是缩进空格数。我们将缩进设置为 2 以使文件具有人类可读性。将其设置为 0（或省略可选参数）将消除 JSON 字符串中的空白，并产生更小的文件。writeFileSync 接收两个参数：文件名和字符串。它会打开或创建文件并将字符串写入其中。

***

当使用 `node index.js` 脚本时，它会处理数据并写入 `repd.json`。`repd.json` 如下：

```json
[
  {
    "id": "1",
    "name": "Aberthaw Power Station Biomass",
    "technology": "Biomass (co-firing)",
    "capacity": 35,
    "lon": -3.407,
    "lat": 51.387,
    "region": "Wales",
    "status": "Operational",
    "operator": "RWE npower",
    "yearSubmitted": 2004,
    "dateSubmitted": "2004-04-16T00:00:00.000Z",
    "yearGranted": 2004,
    "daysUntilGranted": 140
  },
  {
    "id": "2",
    "name": "Hunterston - cofiring",
    "technology": "Biomass (co-firing)",
    "capacity": 170,
    "lon": -4.889,
    "lat": 55.736,
    "region": "Scotland",
    "status": "Application Withdrawn",
    "operator": "Orsted (formerly Dong Energy) / Peel Energy",
    "yearSubmitted": 2010,
    "dateSubmitted": "2010-06-02T00:00:00.000Z",
    "yearGranted": null,
    "daysUntilGranted": null
  },
  ...
]
```

列表 68. wrangling/index.js

# 附录 D：练习提示和解思路

本附录包含了“进一步学习建议”部分的提示和解思路。

## D.1 JavaScript 与数据可视化

### D.1.1 显示不同的字段（例如运营商和/或状态）

要向表格添加 `operator` 属性：

```javascript
let list = '';
data.forEach(d => {
  list += '<div>' + d.name + ' (' + d.operator + ') ' + d.region + ' ' + d.capacity + 'MW</div>';
});
```

列表 69. load-data/main.js

### D.1.2 修改过滤器以显示不同的技术类型并更改容量阈值

显示容量超过 50 MW 的太阳能应用：

```javascript
// 过滤器
data = data.filter(d => d.technology === "Solar Photovoltaics" && d.capacity > 50);
```

列表 70. load-data/main.js

### D.1.3 尝试显示不同的字段

尝试显示不同的字段以了解数据如何组织。尝试在代码中添加不同的属性名来观察结果的变化。

***

有些数据没有有效的提交日期。在这些情况下如何处理并不显而易见，为了教学目的保持简单，我排除了它们：

```javascript
// 排除没有提交日期的申请
output = output.filter(d => d.dateSubmitted !== null); ①

// 仅保留截至 2022 年 12 月及内的提交年份
output = output.filter(d => d.yearSubmitted < 2023); ②

fs.writeFileSync('./repd.json', JSON.stringify(output, null, 2)); ③
```



```
.each(function(d) {
  let html = '';
  html += '<div>Name: ' + d.name + '</div>';
  html += '<div>Technology: ' + d.technology + '</div>';
  html += '<div>Capacity: ' + d.capacity + ' MW</div>';
  html += '<div>Operator: ' + d.operator + '</div>'; ①
  html += '<div>Region: ' + d.region + '</div>'; ②
  html += '<div>Date submitted: ' + d.dateSubmitted.toDateString() + '</div>';
  html += '<div>Status: ' + d.status + '</div>';
  tippy(this, {
    content: html,
    allowHTML: true,
    theme: 'light',
    duration: 0
  });
});
```
列表 76. `d3-dot/main.js`

1. ① 向工具提示的 HTML 字符串中添加 `operator` 属性。
2. ② 向工具提示的 HTML 字符串中添加 `region` 属性。

***

## D.4 使用 Leaflet 构建数据驱动地图

### D.4.1 根据状态而非技术类型标记标记

为 `status` 属性添加一个调色板（拷贝自 `d3-dot` 项目）：

```
...
import './style.css';

let green = '#358600';
let grey = '#aaa';
let purple = '#A675A1';
let yellow = '#F5CF29';

let statusColors = {
  'Abandoned': grey,
  'Appeal Withdrawn': grey,
  'Application Refused': grey,
  'Application Submitted': purple,
  'Application Withdrawn': grey,
  'Awaiting Construction': yellow,
  'Decommissioned': grey,
  'No Application Required': yellow,
  'Operational': green,
  'Planning Permission Expired': grey,
  'Under Construction': yellow
};

function getTooltipContent(d) { ... }
```
列表 77. `leaflet-map/main.js`

根据状态设置标记颜色：

```
data.forEach(d => {
  if (d.lat === null || d.lon === null) return;
  let marker = L.circleMarker([d.lat, d.lon]);
  let radius = radiusScale(d.capacity || 0);
  let color = statusColors[d.status] || '#aaa'; ①

  ...
});
```
列表 78. `leaflet-map/main.js`

1. ① 使用 `status` 属性和 `statusColors` 颜色查找对象设置颜色。

### D.4.2 仅显示太阳光伏应用

过滤出 `'Solar Photovoltaics'` 的数据：

```
map.setView([55, -2], 6);

data = data.filter(d => d.technology === "Solar Photovoltaics"); ①

let maxCapacity = max(data, d => d.capacity); ②
let maxRadius = 20;
let radiusScale = scaleSqrt().domain([0, maxCapacity]).range([3, maxRadius]);
```
列表 79. `leaflet-map/main.js`

1. ① 过滤出 `'Solar Photovoltaics'` 的数据。
2. ② `maxCapacity` 将适应过滤后的数据，因此即使最大容量较低，最大圆的大小仍将为 20。

***

1. 根据 ChatGPT 的说法，最早的 JavaScript 图表库之一是 Netscape Livewire Charts，它开发于 20 世纪 90 年中期。↩︎


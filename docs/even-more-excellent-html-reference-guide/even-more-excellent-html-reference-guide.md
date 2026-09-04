
# HTML 详解参考指南

## 第一节

### HTML 模板

» 必需元素的 HTML 模板

```
</body>
</html>
```

### DOCTYPE DTD

#### HTML 4.01 数据类型定义

- 严格型

  `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`

- 过渡型

  `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">`

- 框架集型

  `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">`

#### XHTML 1.0 数据类型定义

- 严格型

  `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">`

- 过渡型

  `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">`

- 框架集型

  `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">`

## 第二节

### HTML 元素

键盘事件 = `onkeydown`、`onkeypress` 和 `onkeyup`

指针事件 = `onclick`、`ondblclick`、`onmousedown`、`onmousemove`、`onmouseout`、`onmouseover` 和 `onmouseup`

| HTML 元素 | 描述 | 属性 | XML 要求 | 特别说明 | 参考资料 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `<!-- -->` | 注释 |  |  | 注释仅在 HTML 代码中显示，永远不会作为网页的一部分显示。 | 第 2 章第 38 页及图 2.2 |
| 示例：`<!-- Author: T. Gottleber -->` |  |  |  |  |  |
| `<a></a>` | 提供数据以链接图像、声音、页面内的另一个区域，或链接到另一个网页 | accesskey、charset、class、cords、dir、键盘事件、href、hreftlang、lang、id、name、onblur、onfocus、指针事件、rel |  |  | 第 3 章第 59 页及图 3.3 |
| 示例：`<a href="http://site.com">用作链接的文字</a>` |  |  |  |  |  |
| `<a></a>` 续 |  | rev、shape、style、tabindex、target、title、type |  |  |  |
| `<abbr></abbr>` 示例：`<abbr title="World Wide Web Consortium"> W3C </abbr>` | 缩写，如 WWW 或 URL | class、dir、id、键盘事件、lang、指针事件、style、title |  | W3C 建议使用 title 属性来标识缩写的完整拼写。 | 第 5 章第 124 页及图 5.8 |
| `<acronym></acronym>` 示例：`<acronym title="Beginners All-Purpose Symbolic Code"> BASIC </acronym>` | 首字母缩略词，如 NASA 或 FBI | class、dir、id、键盘事件、lang、指针事件、style、title |  | title 属性用于标识首字母缩略词的完整拼写。 | 第 5 章第 124 页及图 5.8 |
| `<address></address>` 示例：我们可以在 `<address> 4606 Briarwood </address>` 找到 | 邮寄地址或电子邮件地址 | class、dir、id、键盘事件、lang、指针事件、style、title |  | 末尾自动添加换行 | 第 5 章第 123 页及图 5.8 |
| `<applet></applet>` 示例：`<applet code="clock.class" width="200" height="400">` | 启动 Java 小程序的执行 | align、alt、archive、class、code、codebase、height、hspace、id、name、object、style、title、vspace、width |  | 已弃用；请改用 `<object></object>`。 | 第 9 章第 243 页及图 9.2 |
| `<area />` 示例：`<area shape="poly" coords="372,131,376,154, 380,156,380,153,380,139, 378,134" alt="Map" href="doc1.htm" />` | 定义客户端图像映射中一个区域的坐标和链接 | accesskey、alt、class、coords、href、id、键盘事件 | 要求使用 `<area />` 闭合标签 | coords 属性以及 href 或 nohref 属性之一是必需的。 | 第 14 章第 414 页及图 14.1 |
| `<area />` 续 |  | lang、nohref、onblur、onfocus、指针事件、shape、style、tabindex、target、title |  |  |  |
| `<b></b>` | 较粗字体 | class、dir、id、键盘事件、lang、指针事件、style、title |  |  | 第 5 章第 121 页及图 5.7 |
| `<base />` | 显式指定文档的基础 URL。相对路径引用则使用基础 URL 作为参考点。 | href、target | 要求使用 `<base />` 闭合标签 | 必须放置在 `<head>` 容器内 | 第 10 章第 285 页及图 10.14 |
| `<bdo></bdo>` | 建立浏览器双向算法如何显示和打印文本 | dir、lang |  | dir 属性是必需的；主要用于 Unicode 格式化 |  |
| `<big></big>` | 放大字形大小，默认等于 3。每次应用都会增加字形大小，直到相对大小等于 7。 | class、dir、id、键盘事件、lang、指针事件、style、title |  | 此标签可以嵌套在自身内部。例如，以下语法将相对大小增加两次：`<big><big>text</big></big>` | 第 5 章第 121 页及图 5.7 |
| `<blockquote></blockquote>` | 长引用，通常超过 40 个单词 | class、dir、id、键盘事件、lang、指针事件、style、title |  | 此元素会被缩进并被视为块级内容。建议使用 cite 和 datetime 属性来标识来源。 | 第 5 章第 125 页及图 5.9 |
| `<body></body>` 示例：`<body style="background-color: #CCCCCC;">` | 标识网页的内容 | alink、background、bgcolor、class、dir、id、键盘事件、lang、link、onload、onunload、指针事件、style、text、title、vlink |  |  | 第 2 章第 34 页及图 2.2 |
| `<br />` 示例：`<br style="clear: left;">` | 创建换行 | class、clear、id、style、title | 要求使用 `<br />` 闭合标签 |  | 第 2 章第 43 页及图 2.7 |
| `<button></button>` 示例：`<button name="reset" type="reset" value="Clear">` | 表示所包含的数据应被格式化并作为按钮控件运行 | class、dir、disabled、id、键盘事件、lang、name、onblur、onfocus、onreset、onsubmit、指针事件、style、tabindex、title、type、value |  |  | 第 11 章第 324 页及图 11.20 |
| `<caption></caption>` `<table>` `<caption>` 关于表格的信息 `</caption>` `<tr>` `<th>标题</th>` `<td>数据</td>` `</tr>` `</table>` | 定义表格标题 | align、class、dir、id、键盘事件、lang、指针事件、style、title |  | 仅允许紧跟在 `<table>` 起始标签之后 | 第 7 章第 193 页及图 7.16 |

## 第 2 节 HTML 元素

| HTML 元素 | 描述 | 属性 | XML 要求 | 特殊说明 | 参考资料 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `<center></center>`<br>示例：<br>`<center>标题</center>` | 在屏幕显示中将对象居中 |  |  | 已废弃；请使用带有以下样式的 `<div>` 容器：`<div style="text-align: center">文本</div>` | 第 6 章第 154 页，图 6.13 |
| `<cite></cite>`<br>示例：<br>`<cite>尤吉·贝拉</cite>` 被引述说过“结束之前，一切皆有可能。” | 引用 | class, dir, id, keyboard events*, lang, pointer events**, style, title |  |  | 第 5 章第 125 页，图 5.8 |
| `<code></code>`<br>示例：<br>在 Fortran 中使用 `<code>input</code>` 语句。 | 过去用于表示计算机代码的等宽字体 | class, dir, id, keyboard events*, lang, pointer events**, style, title |  |  | 第 5 章第 121 页，图 5.7 |
| `<col />`<br>示例：<br>`<col width="30" />` | 允许作者将表格列的属性规格组合在一起，但不会在结构上组合列 | align, char, charoff, class, dir, id, keyboard events*, lang, pointer events**, span, style, title, valign, width | 要求使用 `<col />` 作为闭合标签 | 可与 `<colgroup>` 元素一起使用 | 第 7 章第 197 页，图 7.18 |
| `<colgroup></colgroup>`<br>示例：<br>`<colgroup span="3" width="50" align="center"></colgroup>` | 在表格内创建可以独立格式化的结构性分区 | align, char, charoff, class, dir, id, keyboard events*, lang, pointer events**, span, style, title, valign, width |  |  | 第 7 章第 195 页，图 7.17 |
| `<dd></dd>`<br>示例：<br>`<dl>`<br>&nbsp;&nbsp;`<dt>术语</dt>`<br>&nbsp;&nbsp;`<dd>定义</dd>`<br>`</dl>` | 在定义列表中标识定义 | class, dir, id, keyboard events*, lang, pointer events**, style, title | 需要闭合标签 | 此元素被视为块级内容。 | 第 4 章第 102 页，图 4.17 |
| `<del></del>`<br>示例：<br>这段文本需要被 `<del>删除</del>` | 指示应从页面中移除信息；通常通过在字形上画删除线来执行 | class, dir, id, keyboard events*, lang, pointer events**, style, title |  | 建议使用 cite 和 datetime 属性来标识删除源。 | 第 5 章第 126 页，图 5.8 |
| `<dfn></dfn>`<br>示例：<br>字体描述了 `<dfn>字体中字符的设计</dfn>` | 标识一个定义 | class, dir, id, keyboard events*, lang, pointer events**, style, title |  |  | 第 5 章第 124 页，图 5.8 |
| `<dir></dir>` | 标识一个无隐含顺序的多列目录列表 | class, dir, id, keyboard events*, lang, pointer events**, style, title |  | 已废弃；请改用 `<ul></ul>`。 | 第 4 章第 104 页，图 4.18 |
| `<div></div>`<br>示例：<br>`<div style="color: blue;">`<br>&nbsp;&nbsp;`<h1>标题</h1>`<br>&nbsp;&nbsp;`<p>格式化文本</p>`<br>`</div>` | 标识一个或多个用于特殊格式化或标识的文本块 | align, class, dir, id, keyboard events*, lang, pointer events**, style, title |  |  | 第 8 章第 215 页，图 8.4 |
| `<dl></dl>`<br>示例：<br>`<dl>`<br>&nbsp;&nbsp;`<dt>术语</dt>`<br>&nbsp;&nbsp;`<dd>定义</dd>`<br>`</dl>` | 将术语和相关定义作为类似术语表列表的一部分进行标识 | class, dir, id, keyboard events*, lang, pointer events**, style, title, type |  |  | 第 4 章第 101 页，图 4.17 |
| `<dt></dt>` | 在定义列表中标识术语 | class, dir, id, keyboard events*, lang, pointer events*, style, title | 需要闭合标签。 | 此元素被视为内联内容。 | 第 4 章第 102 页，图 4.17 |
| `<em></em>` | 强调的文本 | class, dir, id, keyboard events*, lang, pointer events**, style, title |  |  | 第 5 章第 124 页，图 5.8 |
| `<fieldset></fieldset>` | 定义一组相关的表单控件 | class, dir, id, keyboard events*, lang, pointer events**, style, title |  |  | 第 11 章第 334 页，图 11.26 |
| `<font></font>` | 更改字体的颜色、字型或大小 | class, color, face, id, lang, size, title |  | 已废弃；请改用 style 属性。 | 第 5 章第 132 页，图 5.13 |
| `<form></form>` | 指示其中包含的数据定义了一个表单 | accept-charset, action, class, dir, enctype, id, keyboard events*, lang, method, name, onreset, onsubmit, pointer events**, style, target, title |  |  | 第 11 章第 301 页，图 11.4 |
| `<frame />`<br>示例：<br>`<frameset rows="15%,*">`<br>&nbsp;&nbsp;`<frame src="doc1.htm" />`<br>&nbsp;&nbsp;`<frame src="doc2.htm"`<br>&nbsp;&nbsp;`name="content" />`<br>`</frameset>` | 标识框架的内容 | class, frameborder, id, longdesc, marginheight, marginwidth, name, noresize, scrolling, src, style, target, title | 要求使用 `<frame />` 作为闭合标签 | 不能出现在 HTML 文档的 `<body>` 元素内 | 第 10 章第 276 页，图 10.9 |



| HTML 元素 | 描述 | 属性 | XML 要求 | 特殊说明 | 参考文献 |
|---|---|---|---|---|---|
| `<frameset></frameset>`<br>示例：<br>`<frameset rows="15%,*">`<br>&nbsp;&nbsp;`<frame src="doc1.htm" />`<br>&nbsp;&nbsp;`<frame src="doc2.htm"`<br>&nbsp;&nbsp;`name="body" />`<br>`</frameset>` | 描述浏览器窗口如何细分为框架 | id, class, cols, onload, onunload, rows, style, title | | 不能出现在 HTML 文档的 `<body>` 元素内 | 第10章第271页，图10.1 |
| `<h1></h1>`<br>示例：<br>`<h1>书籍标题</h1>` | 一级标题 | align, class, dir, id, keyboard events*, lang, pointer events**, style, title | | | 第2章第39页，图2.3 |
| `<h2></h2>`<br>示例：<br>`<h2>章节标题</h2>` | 二级标题 | align, class, dir, id, keyboard events*, lang, pointer events**, style, title | | | 第2章第39页，图2.3 |
| `<h3></h3>`<br>示例：<br>`<h3>节标题</h3>` | 三级标题 | align, class, dir, id, keyboard events*, lang, pointer events**, style, title | | | 第2章第39页，图2.3 |
| `<h4></h4>` | 四级标题 | align, class, dir, id, keyboard events*, lang, pointer events**, style, title | | | 第2章第39页，图2.3 |
| `<h5></h5>` | 五级标题 | align, class, dir, id, keyboard events*, lang, pointer events**, style, title | | | 第2章第39页，图2.3 |
| `<h6></h6>` | 六级标题 | align, class, dir, id, keyboard events*, lang, pointer events**, style, title | | | 第2章第39页，图2.3 |
| `<head></head>`（必需） | 提供关于文档的描述性信息 | dir, lang, profile | | | 第2章第32页，图2.2 |
| `<hr />` | 在页面上创建一条水平线 | align, class, id, keyboard events*, noshade, pointer events**, size, style, title, width | 要求使用 `<hr />` 作为闭合标签 | | 第2章第43页，图2.7 |
| `<html></html>`（必需） | 每个 HTML 文档的第一行和最后一行 | dir, lang, version | 要求文档的第一行为 `<?xml version="1.0"?>` | 以 SGML `<!DOCTYPE>` 标签开头 | 第2章第29页，图2.2 |
| `<i></i>` | 斜体字 | class, dir, id, keyboard events*, lang, pointer events**, style, title | | | 第5章第121页，图5.7 |
| `<iframe></iframe>` | 在文本和其他对象中内联插入一个框架 | align, class, frameborder, height, id, longdesc, marginheight, marginwidth, name, scrolling, src, style, target, title, width | | | 第10章第287页，图10.16 |
| `<img />` | 在屏幕显示中插入图形、照片、线条图或其他图像 | align, alt, border, class, dir, height, hspace, id, ismap, keyboard events*, lang, longdesc, pointer events**, src, style, title, usemap, vspace, width | 要求使用 `<img />` 作为闭合标签 | | 第6章第144页，图6.8 |
| `<input />` | 在表单内创建一个输入控件 | accept, accesskey, align, alt, border, checked, class, dir, disabled, id, keyboard events* | | | 第11章第307页，图11.7 |

## 第2节 HTML 元素

| HTML 元素 | 描述 | 属性 | XML 要求 | 特殊说明 | 参考文献 |
|---|---|---|---|---|---|
| `<input />` 续。 | | lang, maxlength, name, onblur, onchange, onfocus, onselect, 指针事件**, readonly, size, src, style, tabindex, title, type, usemap, value | | | |
| `<ins></ins>`<br>示例：<br>这段文本需要被 `<ins>`添加`</ins>` | 表示应向页面添加信息；通常以下划线形式执行 | class, dir, id, 键盘事件*, lang, 指针事件**, style, title | | 建议使用 cite 和 datetime 属性来标识添加来源。 | 第5章第126页及图5.8 |
| `<isindex />` | 表示该页面可被搜索 | action, class, dir, id, lang, prompt, style, title | 需要结束标签 `<isindex>` | 已弃用；请改用 `<input />`。 | 第12章第349页 |
| `<kbd></kbd>`<br>示例：<br>使用键盘输入 `<kbd>`md home`</kbd>` | 用于表示键盘输入的等宽字体 | class, dir, id, 键盘事件*, lang, 指针事件**, style, title | | | 第5章第121页及图5.7 |
| `<label></label>`<br>示例：<br>`<label id="phone">电话：</label>` `<input type="text" name="tphone" id="phone">` | 为表单中关联的输入控件提供文本标签 | accesskey, class, dir, for, id, 键盘事件*, lang, 指针事件**, style, title | | | 第11章第336页 |
| `<legend></legend>` | 为 `<fieldset>` 元素提供标题 | accesskey, align, class, dir, id, 键盘事件*, lang, 指针事件**, style, title | | | 第11章第334页及图11.27 |
| `<li></li>`<br>示例：<br>`<ol>`<br>`<li>项目 1</li>`<br>`<li>项目 2</li>`<br>`<li>项目 3</li>`<br>`</ol>` | 在有序、无序、菜单或目录列表中标识一个特定项目 | class, dir, id, 键盘事件*, lang, 指针事件**, style, title, type, value | 需要结束标签 `</li>`。 | | 第4章第88页及图4.6 |
| `<link />`<br>示例：<br>`<link rel="stylesheet" href="filename.css" type="text/css" />` | 定义当前文档与 Web 上另一个文档之间的关系，包括外部样式表 | charset, class, dir, href, hreflang, id, 键盘事件*, lang, media, 指针事件**, rel, rev, style, target, title, type | 需要结束标签 `<link />` | 此标签必须编码在 `<head>` 容器内。 | 第8章第210页及图8.2 |
| `<map></map>`<br>示例：<br>`<map name="image.gif">` | 封装由 usemap 属性指定的客户端图像映射数据 | class, del, dir, id, 键盘事件*, name, onblur, onfocus, 指针事件**, rev, style, tabindex, target, title, type | | name 属性是必需的。 | 第14章第413页及图14.1 |
| `<menu></menu>` | 表示一个单列、无隐含顺序的列表 | class<br>dir<br>id<br>键盘事件*<br>lang<br>指针事件**<br>style<br>title | | 已弃用；请改用 `<ul></ul>`。 | 第4章第103页及图4.18 |
| `<meta />`<br>示例：<br>`<meta name="keywords" content="black hole, event horizon" />` | 一个可以指定关于网页附加信息的标签，包括关键字、内容类型和其他 Web 服务器名称/值对 | content<br>dir<br>http-equiv<br>lang<br>name<br>scheme | 需要结束标签 `<meta />` | | 第12章第356页及图12.8 |
| `<nobr></nobr>`<br>示例：<br>`<nobr>`<br>一段不会断行的很长的文本字符串<br>`</nobr>` | 覆盖浏览器将文本换行到下一行的能力 | | | 在 HTML 4 规范中未找到 | 第6章第164页 |
| `<noframes></noframes>`<br>示例：<br>`<noframes>`<br>很抱歉，您的浏览器不支持框架。<br>`</noframes>` | 为不识别 `<frameset>` 元素的浏览器提供内容 | | | 不能出现在 HTML 文档的 `<body>` 元素内 | 第10章第282页及图10.13 |
| `<noscript></noscript>`<br>示例：<br>`<noscript>`<br>很抱歉，您的浏览器无法使用脚本。<br>`</noscript>` | 为不识别 `<script>` 元素的浏览器提供内容 | | | | |
| `<object></object>`<br>示例：<br>`<object classid="clock.class" codetype="application/java" width="200" height="400">`<br>对象未找到。<br>`</object>` | 标识要包含在页面中的图像、HTML 文本、声音、视频或其他外部元素 | align<br>archive<br>border<br>class<br>classid<br>codebase<br>codetype<br>data<br>declare<br>dir<br>height<br>hspace<br>id<br>lang<br>name<br>standby<br>style<br>tabindex | | | 第9章第245页及图9.1 |
| `<object></object>` 续。 | | title<br>type<br>usemap<br>`vspace`<br>width | | | |
| `<ol></ol>`<br>示例：<br>`<ol style="list-style-type: upper-alpha;">`<br>&nbsp;&nbsp;`<li>项目 1</li>`<br>&nbsp;&nbsp;`<li>项目 2</li>`<br>&nbsp;&nbsp;`<li>项目 3</li>`<br>`</ol>` | 表示编号项目列表 | class<br>`compact`<br>dir<br>id<br>键盘事件*<br>lang<br>指针事件**<br>`start`<br>style<br>title<br>`type`<br>`value` | | | 第4章第83页及图4.5 |
| `<optgroup></optgroup>`<br>示例：<br>`<select name="demo">`<br>&nbsp;&nbsp;`<optgroup label="第一部分">`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<option>项目 1</option>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<option>项目 2</option>`<br>&nbsp;&nbsp;&nbsp;&nbsp;`<option>项目 3</option>`<br>&nbsp;&nbsp;`</optgroup>`<br>`</select>` | 允许在 `select` 元素中对多个 `<option>` 进行逻辑分组和标识 | class<br>dir<br>id<br>键盘事件*<br>label<br>lang<br>指针事件**<br>style<br>title | | `<optgroup>` 元素仅在 `<select>` 容器内编码。 | 第11章第333页及图11.26 |
| `<option></option>`<br>示例：<br>`<select name="demo">`<br>&nbsp;&nbsp;`<option>项目 1</option>`<br>&nbsp;&nbsp;`<option>项目 2</option>`<br>&nbsp;&nbsp;`<option>项目 3</option>`<br>`</select>` | 定义由 `<select>` 元素创建的列表框中的一个元素 | class<br>dir<br>`disabled`<br>id<br>键盘事件*<br>label<br>lang<br>onselect<br>指针事件**<br>`selected`<br>style<br>title<br>value | | `<option>` 元素仅在 `<select>` 容器内编码。 | 第11章第332页及图11.24 |
| `<p></p>`<br>示例：<br>`<p>在段落中呈现的信息</p>` | 表示页面内连续的文本字符串 | align<br>class<br>dir<br>id<br>键盘事件*<br>lang<br>指针事件**<br>style<br>title | | 此元素前后各有一个空行。 | 第2章第40页及图2.7 |
| `<param />`<br>示例：<br>`<param name="zone"`<br>`value="EST"`<br>`valuetype="data" />` | 标识对象在运行时所需的值 | id<br>name<br>type<br>value<br>valuetype | 需要结束标签 `<param />` | | 第9章第249页及图9.5 |
| `<pre></pre>`<br>示例：<br>`<pre>`<br>1 12.54 标准<br>2 7.89 折扣<br>3 5.25 秒<br>`</pre>` | 标识浏览器被指示不要更改的预格式化文本 | class<br>dir<br>id<br>键盘事件*<br>lang<br>指针事件**<br>style<br>title<br>width | | 替换已过时的 `<plaintext>`、`<listing>` 和 `<xmp>` 容器 | 第5章第130页及图5.12 |
| `<q></q>`<br>示例：<br>Yogi Berra 说<br>`<q cite="Baseball World">`<br>比赛结束前一切皆有可能<br>`</q>` | 少于40个单词的短引用 | class<br>dir<br>id<br>键盘事件*<br>lang<br>指针事件**<br>style<br>title | | 建议使用 cite 属性来标识来源 | 第5章第126页及图5.9 |
| `<s></s>`<br>示例：<br>这段文本被划上了一条线<br>`<s>`划掉`</s>` | 文本上的删除线 | class<br>dir<br>id<br>键盘事件*<br>lang<br>指针事件**<br>style<br>title | | 已弃用；请改用 `<del></del>`。 | 第5章第121页及图5.7 |
| `<samp></samp>`<br>示例：<br>然后计算机输出<br>`<samp>`<br>预订已确认<br>`</samp>` | 示例输出 | class<br>dir<br>id<br>键盘事件*<br>lang<br>指针事件**<br>style<br>title | | | 第5章第124页及图5.8 |
| `<script></script>`<br>示例：<br>`<script src="demoscript.js">` | 包含一个或多个用 JavaScript 或 Vbscript 等脚本语言编写的函数 | src<br>type<br>language<br>defer<br>charset | | | 第13章第377页及图13.1 |



| `<select></select>`<br>示例：<br>`<select name="demo">`<br>`<option>项目 1</option>`<br>`<option>项目 2</option>`<br>`<option>项目 3</option>`<br>`</select>` | 创建一个由包含的 `<option>` 元素组成的列表框 | `class`<br>`cols`<br>`dir`<br>`disabled`<br>`id`<br>键盘事件*<br>`lang`<br>`multiple`<br>`size` | | `<select>` 容器必须至少包含一个 `<option>` 元素。 | 第11章第328页及图11.22 |

## 节 2 HTML 元素

| HTML 元素 | 描述 | 属性 | XML 要求 | 特别说明 | 参考 |
|---|---|---|---|---|---|
| `<select></select>` 续. | | `name`<br>`onblur`<br>`onchange`<br>`onfocus`<br>`onselect`<br>pointer events**<br>`selected`<br>`size`<br>`style`<br>`tabindex`<br>`title` | | | |
| `<small></small>`<br><br>示例：<br>这段 `<small>文字</small>` 比这段文字小。 | 减小字形大小，默认值等于 3。每次使用都会减小字形大小，直到相对大小等于 1。 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | 此标签可以嵌套在自身内部；例如，以下语法将相对大小减小两次：<br>`<small><small>text</small></small>` | 第5章 第121页 及 图5.7 |
| `<span></span>`<br><br>示例：<br>`<span style="color: red;">待格式化的文字</span>` | 标识任意一段文字，以便进行特殊格式化 | `align`<br>`class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | | 第8章 第218页 及 图8.5 |
| `<strike></strike>`<br><br>示例：<br>这段文字有一条线画在 `<strike>它上面</strike>` | 在文字上画一条删除线 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | 已弃用；请改用 `<del></del>`。 | 第5章 第121页 及 图5.7 |
| `<strong></strong>`<br><br>示例：<br>`<strong>警告！</strong>` | 强烈强调的文字 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | | 第5章 第123页 及 图5.8 |
| `<style></style>`<br><br>示例：<br>`<style type="text/css">` | 标识文档 `<body></body>` 容器中出现元素的格式更改 | `dir`<br>`lang`<br>`media`<br>`title`<br>`type` | | | 第5章 第111页 及 图5.3 |
| `<sub></sub>`<br><br>示例：<br>2 是下标<br>H`<sub>2</sub>`O | 字形放置在文本底部下方半行处 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | 用于科学和数学符号 | 第5章 第121页 及 图5.7 |
| `<sup></sup>`<br><br>示例：<br>2 是上标<br>E=MC`<sup>2</sup>` | 字形放置在文本底部上方半行处 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | 用于科学和数学符号 | 第5章 第121页 及 图5.7 |
| `<table></table>`<br><br>示例：<br>`<table width="100%">`<br>`<tr>`<br>`<th>Header</th>`<br>`<td>data</td>`<br>`</tr>`<br>`</table>` | 定义构成表格的行和列 | `align`<br>`bgcolor`<br>`border`<br>`cellspacing`<br>`cellpadding`<br>`class`<br>`frame`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`rules`<br>`style`<br>`summary`<br>`title`<br>`width` | | | 第7章 第171页 及 图7.1 |
| `<tbody></tbody>`<br><br>示例：<br>`<tbody>`<br>`<tr>`<br>`<td>data</td>`<br>`<td>data</td>`<br>`</tr>`<br>`</tbody>` | 定义表格的主体 | `align`<br>`char`<br>`charoff`<br>`class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title`<br>`valign` | | | 第7章 第201页 及 图7.19 |
| `<td></td>`<br><br>示例：<br>`<table>`<br>`<tr>`<br>`<th>Header</th>`<br>`<td>data</td>`<br>`</tr>`<br>`</table>` | 定义表格中的单个数据单元格 | `abbr`<br>`align`<br>`axis`<br>`bgcolor`<br>`class`<br>`char`<br>`charoff`<br>`colspan`<br>`dir`<br>`headers`<br>`height`<br>`id`<br>keyboard events*<br>`lang`<br>`nowrap`<br>pointer events**<br>`rowspan`<br>`scope`<br>`style`<br>`title`<br>`valign`<br>`width` | 结束标签是必需的。 | 默认设置为单元格中的数据左对齐。 | 第7章 第186页 及 图7.13 |
| `<textarea></textarea>`<br><br>示例：<br>`<textarea name="comments" rows="20" cols="80"></textarea>` | 创建一个多行文本输入框区域 | `class`<br>`cols`<br>`dir`<br>`disabled`<br>`id`<br>`lang`<br>`name`<br>`onblur`<br>`onchange`<br>`onfocus`<br>`onselect`<br>`readonly`<br>`rows`<br>`style`<br>`tabindex`<br>`title` | | | 第11章 第325页 及 图11.21 |
| `<tfoot></tfoot>`<br><br>示例：<br>`<tfoot>`<br>  `<tr>`<br>    `<th>项目</th>`<br>    `<th>描述</th>`<br>  `</tr>`<br>`</tfoot>` | 定义表格的页脚，不会滚出屏幕 | `align`<br>`char`<br>`charoff`<br>`class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title`<br>`valign` | | 必须位于 `<tbody>` 元素之前 | 第7章 第200页 及 图7.19 |
| `<th></th>`<br><br>示例：<br>`<table>`<br>  `<tr>`<br>    `<th>Header</th>`<br>    `<td>data</td>`<br>  `</tr>`<br>`</table>` | 定义表格中作为行或列标题的单个数据单元格 | `abbr`<br>`align`<br>`axis`<br>`bgcolor`<br>`class`<br>`char`<br>`charoff`<br>`colspan`<br>`dir`<br>`headers`<br>`height`<br>`id`<br>keyboard events*<br>`lang`<br>`nowrap`<br>pointer events**<br>`rowspan`<br>`scope`<br>`style`<br>`title`<br>`valign`<br>`width` | 结束标签是必需的。 | 默认设置为单元格中的数据居中并加粗。 | 第7章 第186页 及 图7.13 |
| `<thead></thead>`<br><br>示例：<br>`<thead>`<br>`<tr>`<br>&nbsp;&nbsp;`<th>项目</th>`<br>&nbsp;&nbsp;`<th>描述</th>`<br>`</tr>`<br>`</thead>` | 定义表格的页眉，不会滚出屏幕 | `align`<br>`char`<br>`charoff`<br>`class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title`<br>`valign` | | 必须位于 `<tbody>` 元素之前 | 第7章 第199页 及 图7.19 |
| `<title></title>`（必需）<br><br>示例：<br>`<title>页面标题</title>` | 提供关于文档的描述性信息，显示在屏幕顶部，而非文档正文中 | `dir`<br>`lang` | | 每个 HTML 文档都必须有一个 `<title>` 元素。 | 第2章 第32页 及 图2.2 |
| `<tr></tr>`<br><br>示例：<br>`<table>`<br>`<tr valign="middle">`<br>&nbsp;&nbsp;`<th>Header</th>`<br>&nbsp;&nbsp;`<td>data</td>`<br>`</tr>`<br>`</table>` | 定义表格中的单行 | `align`<br>`bgcolor`<br>`class`<br>`char`<br>`charoff`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title`<br>`valign` | 结束标签是必需的。 | | 第7章 第184页 及 图7.11 |
| `<tt></tt>`<br><br>示例：<br>在 Fortran 中，使用 `<tt>input</tt>` 语句。 | 电传打字机使用的等宽字体 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | | 第5章 第121页 及 图5.7 |
| `<u></u>`<br><br>示例：<br>这段文字是 `<u>带下划线的</u>` | 在文字下方画一条线 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | 已弃用；请使用带有以下 style 属性的 `<span>` 容器：<br>`<span style="text-decoration: underline;">` text `</span>` | 第5章 第121页 及 图5.7 |
| `<ul></ul>`<br><br>示例：<br>`<ul style="list-style-type: square;">`<br>&nbsp;&nbsp;`<li>项目 1</li>`<br>&nbsp;&nbsp;`<li>项目 2</li>`<br>&nbsp;&nbsp;`<li>项目 3</li>`<br>`</ul>` | 标识一个没有特定顺序含义的项目列表 | `class`<br>`compact`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title`<br>`type` | | | 第4章 第92页 及 图4.10 |
| `<var></var>`<br><br>示例：<br>变量 `<var>last_name</var>` 用于标识申请人的姓氏。 | 与计算机程序或数据库相关的变量值 | `class`<br>`dir`<br>`id`<br>keyboard events*<br>`lang`<br>pointer events**<br>`style`<br>`title` | | | 第5章 第124页 及 图5.8 |

# 第三节

## 样式属性与值

| 属性 | 描述 | 值 | 特殊说明 | 媒体 | 参考资料 |
|---|---|---|---|---|---|
| `azimuth`<br>示例：`azimuth: 45 deg;` | 在360度环绕声环境中，改变声音的左/右方位 | `[angle]` \| `left-side` \| `far-left` \| `left` \| `center-left` \| `center` \| `center-right` \| `right` \| `far-right` \| `right-side` \| `behind` \| `leftwards` \| `rightwards` \| `inherit` | `[angle]` 的取值范围为−360至360度（`deg`），其中 `center=0deg`、`right=90deg`、`behind=180deg`、`left=270deg` 或 `−90deg`。`rightwards=+20deg`，`leftwards=−20deg` | `aural`<br>`tv` | |
| `background`（简写属性） | 设置图像或颜色，以及如何将其用作页面内容的底层背景 | `'background-color'` \| `'background-image'` \| `'background-repeat'` \| `'background-attachment'` \| `'background-position'` \| `inherit` | | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第8章 第221页 |
| `background-attachment`<br>示例：`background-attachment: fixed;` | 确定窗口滚动时背景是否移动 | `scroll` \| `fixed` \| `inherit` | | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | |
| `background-color`<br>示例：`background-color: #CCCCCC;` | 设置背景颜色 | `[color]` \| `transparent` \| `inherit` | `[color]` 是六位十六进制代码或本参考指南中找到的颜色关键字 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第7章 第177页及图7.6 |
| `background-image`<br>示例：`background-image: url("pic.gif");` | 从指定的 URL 加载背景图形 | `[url]`（路径/文件名）\| `none` \| `inherit` | 背景图像优先于背景颜色。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第8章 第222页及图8.7 |
| `background-position`<br>示例：`background-position: right top;` | 提供用于在页面内定位图像的 xy 坐标 | `%` \| `[length]` \| `top`、`center` 或 `bottom` \| `left`、`center` 或 `right` \| `inherit` | `[length]` 的测量单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`（pica） | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第8章 第223页及图8.8 |
| `background-repeat`<br>示例：`background-repeat: repeat-y;` | 确定小型背景图像是水平（`x`）还是垂直（`y`）重复 | `repeat` \| `repeat-x` \| `repeat-y` \| `no-repeat` \| `inherit` | 使用 `repeat` 意味着图像在垂直和水平方向都重复。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | |
| `border`（简写属性） | 在元素周围设置一条边框，并定义其粗细、颜色和样式 | `'border-width'` \| `'border-style'` \| `<color>` \| `inherit` | | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第7章 第178页及图7.7 |




| 属性 | 描述 | 值 | 特殊说明 | 媒体 | 参考 |
|---|---|---|---|---|---|
| `border-collapse`<br>示例：<br>`border-collapse: collapse;` | 适用于表格边框，特别是当它们与列或列组相关时 | `collapse` \| `separate` \| `inherit` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `border-color`<br>示例：<br>`border-color: #FF0000;` | 改变边框的颜色 | `[color]` \| `transparent` \| `inherit` | 必须先设置边框，然后才能设置颜色。可选属性：`border-top-color`、`border-right-color`、`border-bottom-color` 或 `border-left-color` | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`ttv` | 第7章 第180页及图6.14 |
| `border-spacing`<br>示例：<br>`border-spacing: 2pt;` | 指定相邻单元格边框之间的距离 | `length` | 必须先设置边框，然后才能设置间距。以点（`pt`）为单位的长度值不能为负数。默认值为0。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `border-style`<br>示例：<br>`border-style: dashed;` | 改变边框线的外观 | `none` \| `hidden` \| `dotted` \| `dashed` \| `solid` \| `double` \| `groove` \| `ridge` \| `inset` \| `outset` | 可选属性：`border-top-style`、`border-right-style`、`border-bottom-style` 或 `border-left-style` | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第6章 第156页及图6.14 |
| `border-width`<br>示例：<br>`border-width: 5pt;` | 改变边框线的粗细、样式和颜色 | `thin` \| `medium` \| `thick` \| 绝对值 | 长度单位为常用度量值。<br>可选属性：`border-top-width`、`border-right-width`、`border-bottom-width` 或 `border-left-width` | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第6章 第156页及图6.14 |
| `border-bottom`<br>示例：<br>`border-bottom: 5pt solid #00FF00;` | 改变底部边框的粗细、样式和颜色。必须指定所有三个属性。 | `thin` \| `medium` \| `thick` \| `[length]` \| `hidden` \| `dotted` \| `dashed` \| `solid` \| `double` \| `groove` \| `ridge` \| `inset` \| `outset` \| `[color]` \| `transparent` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `border-left`<br>示例：<br>`border-left: thin dotted #0000FF;` | 改变左侧边框的粗细、样式和颜色。必须指定所有三个属性。 | `thin` \| `medium` \| `thick` \| `[length]` \| `hidden` \| `dotted` \| `dashed` \| `solid` \| `double` \| `groove` \| `ridge` \| `inset` \| `outset` \| `[color]` \| `transparent` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `border-right`<br>示例：<br>`border-right: .5in groove blue;` | 改变右侧边框的颜色、样式和粗细。必须指定所有三个属性。 | `thin` \| `medium` \| `thick` \| `[length]` \| `hidden` \| `dotted` \| `dashed` \| `solid` \| `double` \| `groove` \| `ridge` \| `inset` \| `outset` \| `[color]` \| `transparent` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `border-top`<br>示例：<br>`border-top: 10px double #660033;` | 改变顶部边框的粗细、样式和颜色。必须指定所有三个属性。 | `thin` \| `medium` \| `thick` \| `[length]` \| `hidden` \| `dotted` \| `dashed` \| `solid` \| `double` \| `groove` \| `ridge` \| `inset` \| `outset` \| `[color]` \| `transparent` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `bottom`<br>示例：<br>`bottom: 1 cm;` | 将元素定位在距离CSS盒子底边指定距离的位置 | `[length]` \| `[percentage]` \| `auto` \| `inherit` | `[length]` 的测量单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc` | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `caption-side`<br>示例：<br>`caption-side: bottom;` | 指定标题相对于表格的位置 | `top` \| `bottom` \| `left` \| `right` \| `inherit` | 标题继承表格的属性 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第7章 第195页及图7.16 |
| `clear`<br>示例：<br>`clear: both;` | 阻断浮动属性对文本流的控制 | `none` \| `left` \| `right` \| `both` \| `inherit` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第8章 第233页 |
| `clip`<br>示例：<br>`clip: rect(10px, 15px, 15px, 10px);` | 定义元素渲染内容中可见的部分 | `[shape]` \| `auto` \| `inherit` | 元素的原始大小是默认的裁剪大小。唯一有效的形状值是`rect`，偏移量按以下顺序指定：`top`、`right`、`bottom` 和 `left`。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `color`<br>示例：<br>`color: #0000FF;` | 改变字体的颜色 | 颜色关键字或相关的十六进制数 | 请参阅本指南中找到的浏览器安全颜色选项。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第5章 第114页 |
| `content`<br>示例：<br>`content: url("demo.jpg");` | 与`:before`和`:after`伪元素一起使用，以在文档中生成内容。 | `[string]` \| `[url]` \| `[counter]` \| `attr(X)` \| `open-quote` \| `close-quote` \| `no-close-quote` \| `inherit` |  | `aural`<br>`braille`<br>`emboss`<br>`handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `counter-increment`<br>示例：<br>`counter-increment: counter;` | 向已标识的计数器添加或减去数字 | `[identifier] ± [integer]` \| `none` \| `inherit` | 允许使用零和负整数。默认增量为1。 | `aural`<br>`braille`<br>`emboss`<br>`handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `counter-reset`<br>示例：<br>`counter-reset: counter 0;` | 为已标识的计数器建立新的起始值 | `[identifier] ± [integer]` \| `none` \| `inherit` | 允许使用零和负整数。默认增量为0。 | `aural`<br>`braille`<br>`emboss`<br>`handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |

## 第 3 节 样式属性与值

| 属性 | 描述 | 值 | 特殊说明 | 媒体 | 参考 |
|---|---|---|---|---|---|
| `cue`（简写） | 在事件前或事件后提供声音作为听觉提示 | `'cue-before'` | `'cue-after'` | `inherit` | 如果只指定一个值，则该值会同时分配给`cue-before`和`cue-after` | `aural` `tv` | 第 9 章 第 260 页 |
| `cue-after`<br>示例：`cue-after: url("sound.wav");` | 在事件后提供声音作为听觉提示 | `[url]` | `none` | `inherit` |  | `aural` `tv` | 第 9 章 第 260 页 |
| `cue-before`<br>示例：`cue-before: url("music.mp3");` | 在事件前提供声音作为听觉提示 | `[url]` | `none` | `inherit` |  | `aural` `tv` | 第 9 章 第 260 页 |
| `cursor`<br>示例：`cursor: crosshair;` | 指定要显示的屏幕指针类型 | `[url]` | `auto` | `crosshair` | `crosshair` | `default` | `pointer` | `move` | `e-resize` | `ne-resize` | `nw-resize` | `n-resize` | `se-resize` | `sw-resize` | `s-resize` | `w-resize` | `text` | `wait` | `help` | `inherit` | `e-resize`、`ne-resize`、`nw-resize`、`n-resize`、`se-resize`、`sw-resize`、`s-resize` 和 `w-resize` 表示需要移动某个边缘（`e` 代表东，`ne` 代表东北） | `handheld` `screen` `tty` `tv` |  |
| `direction`<br>示例：`direction: ltr;` | 指定文本块的基本书写方向 | `ltr` | `rtl` | `inherit` | 覆盖 Unicode 双向算法 | `handheld` `print` `projection` `screen` `tty` `tv` |  |
| `display`<br>示例：`display: block;` | 改变指定元素的显示属性 | `inline` | `block` | `list-item` | `run-in` | `compact` | `marker` | `table` | `inline-table` | `table-row-group` | `table-header-group` | `table-footer-group` | `table-row` | `table-column-group` | `table-column` | `table-cell` | `table-caption` | `none` | `inherit` | 默认样式表可以覆盖此属性设置。 | `aural` `braille` `emboss` `handheld` `print` `projection` `screen` `tty` `tv` |  |
| `elevation`<br>示例：`elevation: 60deg;` | 改变声音的上/下方向 | `[angle]` | `below` | `level` | `above` | `higher` | `lower` | `inherit` | `[angle]` 的取值范围为 +90 至 -90 度（`deg`），其中 `level = 0 deg`，`above = 90 deg`，`below = -90 deg`。`Higher = +10 deg`，`lower = -10 deg`。 | `aural` `tv` |  |
| `empty-cells`<br>示例：<br>`empty-cells: hide;` | 控制没有可见内容的单元格周围的边框渲染 | `show` | `hide` | `inherit` | 如果一行中所有单元格的值为`'hide'`且没有可见内容，则整行不显示。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` |  |
| `float`<br>示例：<br>`float: right;` | 允许其他元素在该对象的左侧或右侧对齐 | `left` | `right` | `none` | `inherit` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 7 章 第 180 页，以及图 6.10（图像）和图 7.8（表格） |
| `font`（简写） | 改变浏览器使用的字形及相关特征 | `'font-style'` | `'font-variant'` | `'font-weight'` | `'font-size'` | `'line-height'` | `'font-family'` | `caption` | `icon` | `menu` | `message-box` | `small-caption` | `status-bar` | `inherit` | 所有与字体相关的属性首先重置为其初始值，然后根据分配给此属性的值进行显式设置。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 5 章 第 119 页 |
| `font-family`<br>示例：<br>`font-family: Arial, sans-serif;` | 控制浏览器使用的字体 | `serif` | `sans-serif` | `cursive` | `fantasy` | `monospace` | `others` | 可以使用具体的字体族名称，如 `Arial` 或 `Times New Roman`。名称中包含空格的必须用引号括起来。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 5 章 第 116 页及图 5.3 |
| `font-size`<br>示例：<br>`font-size: 14pt;` | 以磅或 1/72<sup>nd</sup> 英寸为单位控制字体大小 | `pt` | 1–100% | `larger` | `smaller` | `xx-small` 至 `xx-large` | `inherit` | 绝对大小包括 `xx-small`、`x-small`、`small`、`medium`、`large`、`x-large` 和 `xx-large` | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 5 章 第 117 页及图 5.5 |
| `font-style`<br>示例：<br>`font-style: italic;` | 决定字形是否以倾斜方式显示 | `normal` | `italic` | `oblique` | `inherit` |  | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 5 章 第 118 页及图 5.5 |
| `font-stretch`<br>示例：<br>`font-stretch: semi-expanded;` | 决定字形的宽度 | `normal` | `wider` | `narrower` | `ultra-condensed` 至 `ultra-expanded` | `inherit` | 绝对大小包括 `ultra-condensed`、`extra-condensed`、`condensed`、`semi-condensed`、`normal`、`semi-expanded`、`expanded`、`extra-expanded` 和 `ultra-expanded`。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 5 章 第 119 页 |
| `font-variant`<br>示例：<br>`font-variant: small-caps;` | 决定字形是否以小型大写字母显示 | `normal` | `small-caps` | `inherit` | 如果没有 `small-caps` 字体可用，浏览器可以使用标准大写字符的缩小版本。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 5 章 第 119 页<br>及图 5.6 |
| `font-weight`<br>示例：<br>`font-weight: bold;` | 决定字形的粗细或深浅 | `normal` | `bold` | `bolder` | `lighter` | 100–900 | `inherit` | 正常文本为 400，粗体文本为 700。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 5 章 第 118 页<br>及图 5.6 |




| 属性 | 描述 | 取值 | 特别说明 | 媒介 | 参考 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `height`<br>示例：<br>`height: 75px;` | 预设对象（如图像和文本区域）的高度 | `[length]`<br>`[percentage]`<br>`auto`<br>`inherit` | `[length]` 的单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。不允许使用负值。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 8 章 第 226 页<br>及图 7.15 |
| `left`<br>示例：<br>`left: 2cm;` | 指定对象左内容边缘相对于容器或浏览器窗格左边缘向右偏移的距离 | `[length]`<br>`[percentage]`<br>`auto`<br>`inherit` | `[length]` 的单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc` | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | |
| `letter-spacing`<br>示例：<br>`letter-spacing: 0.1em;` | 增加（`+`）或减少（`–`）字母之间的间距 | `normal`<br>`[length]`<br>`inherit` | `[length]` 的单位为 `em` 或 `cm`。可以使用小数。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 8 章 图 8.6 |
| `line-height`<br>示例：<br>`line-height: 115%;` | 决定为一行文本保留的垂直空间 | `normal`<br>`[number]`<br>`[length]`<br>`[percentage]`<br>`inherit` | `[number]` 是与文本高度相乘的系数。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 8 章 第 219 页 |
| `list-style`（简写） | 改变列表中的标记及其位置 | `'list-style-type'`<br>`'list-style-position'`<br>`'list-style-image'`<br>`inherit` | | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 4 章 第 96 页 |
| `list-style-image`<br>示例：<br>`list-style-image: url("demo.jpg");` | 设置用作列表项标记的图像 | `[url]`<br>`none`<br>`inherit` | 用 `'list-style-type'` 设置的标记将被此属性替换 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 6 章 第 161 页<br>及图 6.16 |
| `list-style-position`<br>示例：<br>`list-style-position: outside;` | 指定列表中标记的位置 | `inside`<br>`outside`<br>`inherit` | | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 4 章 第 94 页及图 4.11 |
| `list-style-type`<br>示例：<br>`list-style-type: lower-alpha;` | 指定列表项标记的外观 | `disc`<br>`circle`<br>`square`<br>`decimal`<br>`decimal-leading-zero`<br>`lower-roman`<br>`upper-roman`<br>`lower-greek`<br>`lower-alpha`<br>`lower-latin`<br>`upper-alpha`<br>`upper-latin`<br>`hebrew`<br>`armenian`<br>`georgian`<br>`cjk-ideographic`<br>`hiragana`<br>`katakana`<br>`hiragana-iroha`<br>`katakana-iroha`<br>`none`<br>`inherit` | 标记有三种类型：字形、数字系统和字母字符。由 `'list-style-image'` 指定的值会覆盖由 `'list-style-type'` 设置的标记。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 4 章 第 86 页及图 4.5 |
| `margin`（简写） | 定义围绕 CSS 框的四个透明区域（边距） | `{margin-width}{1,4}`<br>`inherit` | 使用一个值时，所有边距相同。使用两个值时，上/下相同，左/右相同。使用三个值时，第一个值=上，第二个值=右 & 左，第三个值=下。使用四个值时，依次分配给上、右、下、左。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 8 章 第 226 页 |
| `margin-bottom`<br>示例：<br>`margin-bottom: 5%;` | 定义 CSS 框底部的透明区域 | `[length]`<br>`[percentage]`<br>`auto`<br>`inherit` | `[length]` 的单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 8 章 图 8.10 |
| `margin-left`<br>示例：<br>`margin-left: 1in;` | 定义 CSS 框左侧的透明区域 | `[length]`<br>`[percentage]`<br>`auto`<br>`inherit` | `[length]` 的单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 8 章 图 8.10 |
| `margin-top`<br>示例：<br>`margin-top: 2em;` | 定义 CSS 框顶部的透明区域 | `[length]`<br>`[percentage]`<br>`auto`<br>`inherit` | `[length]` 的单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`<br>`print`<br>`projection`<br>`screen`<br>`tty`<br>`tv` | 第 8 章 图 8.10 |

## 第 3 节 样式属性与值

| 属性 | 描述 | 取值 | 特别说明 | 媒介 | 参考 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `margin-right` | 定义 CSS 盒子右侧的透明区域 | `[length]` \| `[percentage]` \| `auto` \| `inherit` | `[length]` 单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 图 8.10 |
| 示例：`margin-right: 1 cm;` | | | | | |
| `marker-offset` | 定位裁切标记和十字对齐标记 | `[length]` \| `auto` \| `inherit` | `[length]` 单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。允许负值。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 第 236 页 |
| 示例：`marker-offset: 10mm;` | | | | | |
| `marks` | 裁切标记指示页面应被裁切的位置。十字标记用于对齐纸张。 | `crop` \| `cross` \| `none` \| `inherit` | 十字标记也称为套准或对齐标记。 | `emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 第 236 页 |
| 示例：`marks: cross;` | | | | | |
| `max-height` | 设置对象的最大高度 | `[length]` \| `[percentage]` \| `none` \| `inherit` | `[length]` 单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`max-height: 75 px;` | | | | | |
| `max-width` | 设置对象的最大宽度 | `[length]` \| `[percentage]` \| `none` \| `inherit` | `[length]` 单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`max-width: 3cm;` | | | | | |
| `min-height` | 设置对象的最小高度 | `[length]` \| `[percentage]` \| `inherit` | `[length]` 单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`min-height: 14pt;` | | | | | |
| `min-width` | 设置对象的最小宽度 | `[length]` \| `[percentage]` \| `inherit` | `[length]` 单位为 `em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`min-width: 5em;` | | | | | |
| `orphans` | 段落必须留在页面底部的最小行数 | `[number]` \| `inherit` | 默认值 = 2 | `emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 第 235 页 |
| 示例：`orphans: 1;` | | | | | |
| `outline`（简写） | 在按钮、活动表单字段、图像映射等可视对象周围创建轮廓 | `'outline-color'` \|\| `'outline-style'` \|\| `'outline-width'` \| `inherit` | | `aural`、`braille`、`emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| `outline-color` | 设置围绕对象轮廓的颜色 | `[color]` \| `invert` \| `inherit` | `[color]` 为六位十六进制代码或书封面内列出的颜色关键字 | `aural`、`braille`、`emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`outline-color: #FF9966;` | | | | | |
| `outline-style` | 设置围绕对象轮廓的样式 | `none` \| `hidden` \| `dotted` \| `dashed` \| `solid` \| `double` \| `groove` \| `ridge` \| `inset` \| `outset` \| `inherit` | 与 `border-style` 类似 | `aural`、`braille`、`emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`outline-style: groove;` | | | | | |
| `outline-width` | 设置围绕对象轮廓的宽度 | `thin` \| `medium` \| `thick` \| 绝对值 \| `inherit` | 与 `border-width` 类似 | `aural`、`braille`、`emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`outline-width: thin;` | | | | | |
| `overflow` | 与 `'clip'` 属性配合使用，决定溢出的裁剪方式 | `visible` \| `hidden` \| `scroll` \| `auto` \| `inherit` | | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`overflow: scroll;` | | | | | |
| `padding`（简写） | 定义内容与边框或轮廓之间的空白区域 | `[padding-width]{1,4}` \| `inherit` | 使用一个值时，所有内边距相同。使用两个值时，上下相同、左右相同。使用三个值时，第一个值=上，第二个值=右和左，第三个值=下。四个值分别赋给上、右、下、左。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 第 230 页 |
| `padding-top` | 改变内容顶部与边框线之间的空白厚度 | `[padding-width]` \| `inherit` | `[padding-width]` 单位为 `%`、`em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 图 8.12 |
| 示例：`padding-top: 0.2em;` | | | | | |
| `padding-right` | 改变内容右侧与边框线之间的空白厚度 | `[padding-width]` \| `inherit` | `[padding-width]` 单位为 `%`、`em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 图 8.12 |
| 示例：`padding-right: 4px;` | | | | | |
| `padding-bottom` | 改变内容底部与边框线之间的空白厚度 | `[padding-width]` \| `inherit` | `[padding-width]` 单位为 `%`、`em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 图 8.12 |
| 示例：`padding-bottom: 1mm;` | | | | | |
| `padding-left` | 改变内容左侧与边框线之间的空白厚度 | `[padding-width]` \| `inherit` | `[padding-width]` 单位为 `%`、`em`、`ex`、`px`、`in`、`cm`、`mm`、`pt` 和 `pc`。 | `handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 图 8.12 |
| 示例：`padding-left: 0.3em;` | | | | | |
| `page` | 用于在打印时强制分页；旨在与 `id` 属性和目标名称配合使用 | `[target-name]` \| `auto` | 如果一个包含内联内容的块级框具有与前一个包含内联内容的块级框不同的 `'page'` 属性，则在它们之间插入一个或两个分页符。 | `emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | |
| 示例：`page: target-name;` | | | | | |
| `page-break-after` | 元素显示或打印后开始新页。 | `auto` \| `always` \| `avoid` \| `left` \| `right` \| `inherit` | | `emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 第 234 页 |
| 示例：`page-break-after: avoid;` | | | | | |
| `page-break-before` | 元素显示或打印前开始新页 | `auto` \| `always` \| `avoid` \| `left` \| `right` \| `inherit` | | `emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 第 233 页 |
| 示例：`page-break-before: always;` | | | | | |
| `page-break-inside` | 确定元素内是否允许分页 | `avoid` \| `auto` \| `inherit` | 通常用于不希望表格或列表被分页打断的情况 | `emboss`、`handheld`、`print`、`projection`、`screen`、`tty`、`tv` | 第 8 章 第 234 页 |
| 示例：`page-break-inside: avoid;` | | | | | |
| `pause`（简写） | 设置朗读元素内容之前或之后的时间 | `[time]` \| `[percentage]` \| `{1,2}` \| `inherit` | 如果给出两个值，第一个值为 `'pause-before'`，第二个为 `'pause-after'` | `aural`、`tv` | 第 9 章 第 260 页 |
| `pause-after` | 朗读元素内容之后到开始下一文本之间的时间 | `[time]` \| `[percentage]` \| `inherit` | 时间单位为毫秒（`ms`）和秒（`s`）。 | `aural`、`tv` | |
| 示例：`pause-after: 30ms;` | | | | | |
| `pause-before` | 朗读元素内容之前的时间 | `[time]` \| `[percentage]` \| `inherit` | 时间单位为毫秒（`ms`）和秒（`s`）。 | `aural`、`tv` | |



| 示例：`pause-before: 1s;` | | | | | |
|---|---|---|---|---|---|
| `pitch` | 调整朗读声音的频率（音高） | `[frequency]` \| `x-low` \| `low` \| `medium` \| `high` \| `x-high` \| `inherit` | `[frequency]` 以赫兹（Hz）为单位，low 的频率低于 medium。 | aural, tv | |
| 示例：`pitch: 120Hz; /* 男声 */` | | | | | |
| `pitch-range` | 指定平均音高的变化范围 | `[number]` \| `inherit` | `[number]` 范围从 0 到 100，0 为平直，100 为生动。默认值 = 50 | aural, tv | |
| 示例：`pitch-range: 60;` | | | | | |
| `play-during` | 指定在朗读元素内容时作为背景播放的声音 | `[url] mix` \| `repeat` \| `auto` \| `none` \| `inherit` | 使用 mix 时，url 声音会与背景声音一起播放。 | aural, tv | |
| 示例：`play-during: url("demo.wav") mix;` | | | | | |
| `position` | 标识对象在屏幕上的放置位置 | `static` \| `relative` \| `absolute` \| `fixed` \| `inherit` | absolute 值与 left、right、top 和 bottom 属性配合使用。 | handheld, print, projection, screen, tty, tv | |
| 示例：`position: fixed;` | | | | | |

## 第 3 节

## 样式属性与值

| 属性 | 说明 | 值 | 特殊说明 | 媒体 | 参考 |
|---|---|---|---|---|---|
| `quotes`<br>示例：`quotes: "<" ">" '"' "'";` | 指定用于引号包围的 ISO 字符 | `"string"` `""string""` | none<br>inherit | 第一组（最左侧）引号表示最外层引号，第二组表示第一层嵌套引号。传统英语语法中使用 `"` 作为最外层引号，`'` 作为嵌套引号。 | handheld, print, projection, screen, tty, tv |
| `richness`<br>示例：`richness: 40;` | 标识声音在大房间中的传播效果。饱满（rich）传播效果好，平滑（smooth）则不佳。 | `[number]` | inherit | `[number]` 取值范围为 0 到 100，0 表示平滑，100 表示饱满。数值越高，声音传播效果越好。默认值 = 50 | aural, tv |
| `right`<br>示例：`right: 20mm;` | 指定对象右侧内容边缘相对于容器或浏览器窗口右侧边缘向左偏移的距离 | `[length]` | `[percentage]`<br>auto<br>inherit | `[length]` 的测量单位为 em、ex、px、in、cm、mm、pt 和 pc | handheld, print, projection, screen, tty, tv |
| `size`<br>示例：`size: 8.5in 11in;` | 指定页面的大小和方向 | `[length]` | auto<br>portrait<br>landscape<br>inherit | 长度值设置宽度和高度。一个数值同时设置两个值。使用两个值时，第一个设置宽度。 | emboss, handheld, print, projection, screen, tty, tv | 第 8 章第 235 页 |
| `speak`<br>示例：`speak: spell-out;` | 确定文本如何以听觉方式呈现 | normal<br>none<br>spell-out<br>inherit | Normal 表示使用依赖于语言的发音规则。Spell-out 表示逐个字母读出。 | aural, tv | 第 9 章第 258 页 |
| `speak-header`<br>示例：`speak-header: once;` | 指定表格表头是否在每个单元格之前朗读 | once<br>always<br>inherit | 朗读信息可在 headers、scope 或 axis 属性中找到。 | aural, tv | |
| `speak-numeral`<br>示例：`speak-numeral: continuous;` | 控制数字的朗读方式；发音依赖于语言 | `digits` \| `continuous` \| `inherit` | Digits：123 朗读为 "one, two, three."。Continuous：123 朗读为 "one-hundred twenty-three."。 | aural<br>tv | |
| `speak-punctuation`<br>示例：`speak-punctuation: code;` | 确定标点符号是否朗读 | `code` \| `none` \| `inherit` | Code 表示朗读标点符号。 | aural<br>tv | |
| `speech-rate`<br>示例：`speech-rate: fast;` | 调整朗读单词的速度 | `[number]` \| `x-slow` \| `slow` \| `medium` \| `fast` \| `x-fast` \| `faster` \| `slower` \| `inherit` | `[number]` 以每分钟单词数给出，x-slow=80，medium=180，x-fast=300。Faster=+40，slower=-40。 | aural<br>tv | |
| `stress`<br>示例：`stress: 65;` | 指定语音语调中的语调峰值 | `[number]` \| `inherit` | `[number]` 取值范围为 0 到 100，具体含义取决于语言。默认值 = 50 | aural<br>tv | |
| `table-layout`<br>示例：`table-layout: fixed` | 控制表格的行、列和单元格在页面上的位置 | auto \| fixed \| inherit | | handheld<br>print<br>projection<br>screen<br>tty<br>tv | |
| `text-align`<br>示例：`text-align: center;` | 将文本 orient 到屏幕的左侧、右侧或中间 | left \| right \| center \| justify \| `[string]` \| inherit | `[string]` 适用于基于字符串值的表格单元格对齐。 | handheld<br>print<br>projection<br>screen<br>tty<br>tv | 第 5 章第 115 页和图 5.3 |
| `text-decoration`<br>示例：`text-decoration: underline;` | 在文本区域绘制水平线或开启/关闭区域 | none \| underline \| overline \| line-through \| blink \| inherit | 仅适用于文本，对图像无影响 | handheld<br>print<br>projection<br>screen<br>tty<br>tv | 第 8 章第 219 页和图 8.6 |
| `text-indent`<br>示例：`text-indent: 2em;` | 将第一行起点相对于文本区域默认边缘向左或向右移动 | `[length]` \| `[percentage]` \| inherit | `[length]` 的测量单位为 em、ex、px、in、cm、mm、pt 和 pc。负数使文本向左移动。 | handheld<br>print<br>projection<br>screen<br>tty<br>tv | 第 8 章第 219 页 Politeness levels |
| `text-shadow`<br>示例：`text-shadow: 0.2em 0.2em` | 叠加另一个字符图像，向左或向右（x），向上或向下（y） | none \| color \| x y blur \| inherit | 坐标和模糊值以 em、ex、px、in、cm、mm、pt 和 pc 给出：-x 向左，-y 向上。 | handheld print projection screen tty tv | |
| `text-transform`<br>示例：`text-transform: uppercase;` | 标准化文本的大小写 | none \| capitalize \| uppercase \| lowercase \| inherit | Capitalize 将每个单词的首字符转换为大写。 | handheld print projection screen tty tv | |
| `top`<br>示例：`top: 1em;` | 将元素定位在距 CSS 框顶部边缘指定距离的位置 | `[length]` \| `[percentage]` \| auto \| inherit | `[length]` 的测量单位为 em、ex、px、in、cm、mm、pt 和 pc。 | handheld print projection screen tty tv | |
| `unicode-bidi`<br>示例：`unicode-bidi: embed;` | 根据浏览器的双向算法确定对象的对齐方式 | normal \| embed \| bidi-override \| inherit | 这些值与 direction 属性配合使用。 | handheld print projection screen tty tv | |
| `vertical-align`<br>示例：`vertical-align: sub;` | 在文本区域中为每行文本分配的垂直行空间内，上下 orient 文本 | baseline \| sub \| super \| top \| text-top \| middle \| bottom \| text-bottom \| `[percentage]` \| `[length]` \| inherit | Baseline = '0%' 或 '0cm'。正值使文本高于基线，负值使文本低于基线。 | handheld print projection screen tty tv | 第 8 章第 219 页 |
| `visibility`<br>示例：`visibility: hidden;` | 确定对象是否从屏幕显示中移除 | visible \| hidden \| collapse \| inherit | Collapse 仅用于表格。 | handheld print projection screen tty tv | 第 8 章第 226 页 |
| `voice-family`<br>示例：`voice-family: male;` | 设置说话声音的音色。甚至可以使用你自己的声音。 | `[specific-voice]` \| `[generic-voice]` \| inherit | 通用声音包括 male、female 和 child。 | aural tv | |
| `volume`<br>示例：`volume: 30;` | 调整声音的动态范围 | `[number]Bio` \| `[percentage]` \| silent \| x-soft \| soft \| medium \| loud \| x-loud \| inherit | `[number]` 取值范围为 0 到 100，x-soft=0，medium=50，x-loud=100。默认值 = 50。 | aural tv | 第 9 章第 258 页 |
| `widows`<br>示例：`widows: 3;` | 段落中必须留在页面顶部的最少行数 | `[number]` \| inherit | 默认值 = 2 | emboss<br>handheld<br>print<br>projection<br>screen<br>tty<br>tv | 第 8 章第 235 页 |
| `width`<br>示例：`width: 3in;` | 预设对象（如图像和文本区域）的宽度 | `[length]` \| `[percentage]` \| auto \| inherit | `[length]` 的测量单位为 em、ex、px、in、cm、mm、pt 和 pc。不允许使用负值。 | handheld<br>print<br>projection<br>screen<br>tty<br>tv | 第 8 章第 225 页和图 7.15 |
| `white-space`<br>示例：`white-space: nowrap;` | 确定如何处理制表符和重复空格 | normal \| pre \| nowrap \| inherit | pre 和 nowrap 都将 "\A" 识别为换行符号。 | handheld<br>print<br>projection<br>screen<br>tty<br>tv | 第 7 章第 193 页 |
| `word-spacing`<br>示例：`word-spacing: 1em;` | 增大（+）或减小（-）单词间距 | normal \| `[length]` \| inherit | `[length]` 的测量单位为 em、ex、px、in、cm、mm、pt 和 pc。允许使用负值。 | handheld<br>print<br>projection<br>screen<br>tty<br>tv | 第 8 章图 8.6 |
| `z-index`<br>示例：`z-index: 1;` | 指定对象重叠时的堆叠顺序 | auto \| `[integer]` \| inherit | | handheld<br>print<br>projection<br>screen<br>tty<br>tv | |

# 第四节

## CSS 伪类和伪元素

| 类或元素 | 描述 | 特别说明 | 参考资料 |
|---|---|---|---|
| `:active`（伪类）<br>示例：`a:active {font-weight: bold;}`<br>`<a href="demo.html">Demo</a>` | 当元素被用户激活时适用 | 在示例中，激活的文本以粗体显示。 | 第 12 章 第 367 页 和 图 12.17 |
| `:after`（伪元素）<br>示例：`h1:after {content: url("logo.gif"); }`<br>`<h1>Store Name's Web Site</h1>` | 在指定元素的内容之后插入生成的内容 | 在示例中，商店的 logo 显示在所有一级标题之后。 | 第 12 章 第 367 页 |
| `:before`（伪元素）<br>示例：`h1:before {content: url("logo.gif"); }`<br>`<h1>Store Name's Web Site</h1>` | 在指定元素的内容之前插入生成的内容 | 在示例中，商店的 logo 显示在所有一级标题之前。 | 第 12 章 第 368 页 和 图 12.16 |
| `:first-child`（伪类）<br>示例：`div > p:first-child { font-style: italic; }`<br>`<div>`<br>`<p>第一个子元素适用</p>`<br>`<p>不适用</p>`<br>`</div>` | 适用于关联元素中指定元素的第一次出现 | `>` 符号用于标识指定元素。在示例中，`<div>` 是与 `<p>` 元素关联的指定元素。 | 第 12 章 第 367 页 |
| `:first-line`（伪元素）<br>示例：`p:first-line {font-style: italic; }`<br>`<p>此文本的一部分以斜体显示。</p>` | 对指定元素的第一行格式化文本应用特殊样式 | `:first-line` 伪元素只能附加到块级元素。 | 第 12 章 第 367 页 |
| `:first-letter`（伪元素）<br>示例：`p:first-letter {font-weight: bold; }`<br>`<p>首个字母 "T" 为粗体。</p>` | 用于“首字下沉”和“首字母大写”，即文本字符串中的第一个字形被独立格式化 | 这些属性适用于 `.first-letter`：字体属性、颜色属性、背景属性、`text-decoration`、`vertical-align`（仅当 `float` 为 `none` 时）、`text-transform`、`line-height`、外边距属性、内边距属性、边框属性、`float`、`text-shadow` 和 `clear`。 | 第 12 章 第 367 页 和 图 12.16 |
| `:focus`（伪类）<br>示例：`textarea:focus { color: #FF0000; }`<br>`<textarea></textarea>` | 当元素准备好接受输入时适用 | 在示例中，输入到文本区域中的文本以红色显示。 | 第 12 章 第 367 页 |
| `:hover`（伪类）<br>示例：`a:hover { background: #FFFF00; }`<br>`<a href="demo.html">Demo</a>` | 适用于屏幕指针悬停的元素 | 不支持交互媒体的浏览器不必支持此伪类。 | 第 12 章 第 368 页 图 12.17 |



| 选择器 | 示例 | 描述 | 参考 |
| --- | --- | --- | --- |
| `:lang`（伪类） | 示例：<br>`:lang(it) > q { quotes: '"' '"'; font-style: italic; }`<br><br>`<p lang="it">他用意大利语说了 <q>不</q></p>` | 指定应用于元素的语法语言。`>` 符号用于标识关联元素。在示例中，`:lang(it)` 与 `<q>` 元素关联。因此，任何使用意大利语的元素都会在 `<q>` 容器中斜体文本的周围显示 « 和 » 字形。 | |
| `:link`（伪类） | 示例：<br>`a.special:link {color: #0000FF; }`<br>`<a class="special" href="demo.html">Demo</a>` | 适用于尚未访问过的链接。在示例中，链接以蓝色显示。 | 第 12 章 第 368 页 图 12.17 |
| `:visited`（伪类） | 示例：<br>`a.done:visited {color: #660099; }`<br>`<a class="demo" href="demo.html">Demo</a>` | 适用于已经被激活过的链接。在示例中，一旦链接被使用过，它将以紫色字体显示。 | |

# 第五节

## 常用字符集

下表列出了大多数浏览器都能识别的一组常用字符。屏幕上显示的字形列在“符号”一栏下。数值必须始终以 `&#` 开头，并以分号结尾。三位数字值及相关名称（如果可用）可以在 HTML 文档中代替输入的字符。这些字符代表 Latin-1 字符集，也称为国际标准化组织代码 ISO 8859-1。此外，这是 HTML 4.0 规范中标识的 Unicode 字符（ISO 10646-1）的基础字符集。HTML 的 Latin 1 或 Unicode 字符集中不使用数字值 128–159。

| 数值 | 符号 | 名称 | 描述 |
| --- | --- | --- | --- |
| `&#009;` | | | 水平制表符 |
| `&#010;` | | | 换行符 |
| `&#013;` | | | 回车符 |
| `&#032;` | | | 空格 |
| `&#033;` | ! | | 感叹号 |
| `&#034;` | `"` | `&quot;` | 双引号 |
| `&#035;` | # | | 井号 |
| `&#036;` | $ | | 美元符号 |
| `&#037;` | % | | 百分号 |
| `&#038;` | & | `&amp;` | 和号 |
| `&#039;` | `'` | | 撇号 |
| `&#040;` | ( | | 左括号 |
| `&#041;` | ) | | 右括号 |
| `&#042;` | * | | 星号 |
| `&#043;` | + | | 加号 |
| `&#044;` | , | | 逗号 |
| `&#045;` | - | | 连字符 |
| `&#046;` | . | | 句号 |
| `&#047;` | / | | 斜杠 |
| `&#048;` | 0 | | 零 |
| `&#049;` | 1 | | 一 |
| `&#050;` | 2 | | 二 |
| `&#051;` | 3 | | 三 |
| `&#052;` | 4 | | 四 |
| `&#053;` | 5 | | 五 |
| `&#054;` | 6 | | 六 |
| `&#055;` | 7 | | 七 |
| `&#056;` | 8 | | 八 |
| `&#057;` | 9 | | 九 |
| `&#058;` | : | | 冒号 |
| `&#059;` | ; | | 分号 |
| `&#060;` | < | `&lt;` | 小于号 |
| `&#061;` | = | | 等于号 |
| `&#062;` | > | `&gt;` | 大于号 |
| `&#063;` | ? | | 问号 |
| `&#064;` | @ | | at 符号 |
| `&#065;` | A | | 大写 A |
| `&#066;` | B | | 大写 B |
| `&#067;` | C | | 大写 C |
| `&#068;` | D | | 大写 D |
| `&#069;` | E | | 大写 E |
| `&#070;` | F | | 大写 F |
| `&#071;` | G | | 大写 G |
| `&#072;` | H | | 大写 H |
| `&#073;` | I | | 大写 I |
| `&#074;` | J | | 大写 J |
| `&#075;` | K | | 大写 K |
| `&#076;` | L | | 大写 L |
| `&#077;` | M | | 大写 M |
| `&#078;` | N | | 大写 N |
| `&#079;` | O | | 大写 O |
| `&#080;` | P | | 大写 P |
| `&#081;` | Q | | 大写 Q |
| `&#082;` | R | | 大写 R |
| `&#083;` | S | | 大写 S |
| `&#084;` | T | | 大写 T |
| `&#085;` | U | | 大写 U |
| `&#086;` | V | | 大写 V |
| `&#087;` | W | | 大写 W |
| `&#088;` | X | | 大写 X |
| `&#089;` | Y | | 大写 Y |
| `&#090;` | Z | | 大写 Z |
| `&#091;` | [ | | 左方括号 |
| `&#092;` | `\\` | | 反斜杠 |
| `&#093;` | ] | | 右方括号 |
| `&#094;` | ^ | | 脱字符 |
| `&#095;` | _ | | 下划线 |
| `&#096;` | `` ` `` | | 重音符 |
| `&#097;` | a | | 小写 a |
| `&#098;` | b | | 小写 b |
| `&#099;` | c | | 小写 c |
| `&#100;` | d | | 小写 d |
| `&#101;` | e | | 小写 e |
| `&#102;` | f | | 小写 f |
| `&#103;` | g | | 小写 g |
| `&#104;` | h | | 小写 h |
| `&#105;` | i | | 小写 i |
| `&#106;` | j | | 小写 j |
| `&#107;` | k | | 小写 k |
| `&#108;` | l | | 小写 l |
| `&#109;` | m | | 小写 m |
| `&#110;` | n | | 小写 n |
| `&#111;` | o | | 小写 o |
| `&#112;` | p | | 小写 p |
| `&#113;` | q | | 小写 q |
| `&#114;` | r | | 小写 r |
| `&#115;` | s | | 小写 s |
| `&#116;` | t | | 小写 t |
| `&#117;` | u | | 小写 u |
| `&#118;` | v | | 小写 v |
| `&#119;` | w | | 小写 w |
| `&#120;` | x | | 小写 x |
| `&#121;` | y | | 小写 y |
| `&#122;` | z | | 小写 z |
| `&#123;` | { | | 左花括号 |
| `&#124;` | `\|` | | 竖线 |
| `&#125;` | } | | 右花括号 |
| `&#126;` | ~ | | 波浪号 |
| `&#160;` | | `&nbsp;` | 不间断空格 |
| `&#161;` | ¡ | `&iexcl;` | 倒感叹号 |
| `&#162;` | ¢ | `&cent;` | 分币符号 |
| `&#163;` | £ | `&pound;` | 英镑符号 |
| `&#164;` | ¤ | `&curren;` | 通用货币符号 |
| `&#165;` | ¥ | `&yen;` | 日元符号 |
| `&#166;` | ¦ | `&brvbar;` | 断开竖线 |
| `&#167;` | § | `&sect;` | 节号 |
| `&#168;` | ¨ | `&uml;` | 分音符 |
| `&#169;` | © | `&copy;` | 版权符号 |
| `&#170;` | ª | `&ordf;` | 阴性序数指示符 |
| `&#171;` | « | `&laquo;` | 左双角引号 |

## 第 5 节 常用字符集

| 数值 | 符号 | 名称 | 描述 |
| --- | --- | --- | --- |
| `&#172;` | ¬ | `&not;` | 非符号 |
| `&#173;` | - | `&shy;` | 软连字符 |
| `&#174;` | ® | `&reg;` | 注册商标符号 |
| `&#175;` | - | `&macr;` | 长音符号 |
| `&#176;` | ° | `&deg;` | 度符号 |
| `&#177;` | ± | `&plusmn;` | 正负号 |
| `&#178;` | ² | `&sup2;` | 上标二 |
| `&#179;` | ³ | `&sup3;` | 上标三 |
| `&#180;` | ´ | `&acute;` | 锐音符号 |
| `&#181;` | µ | `&micro;` | 希腊字母 mu |
| `&#182;` | ¶ | `&para;` | 段落符号 |
| `&#183;` | · | `&middot;` | 中点 |
| `&#184;` | , | `&cedil;` | 软音符 |
| `&#185;` | ¹ | `&sup1;` | 上标一 |
| `&#186;` | º | `&ordm;` | 阳性序数符号 |
| `&#187;` | » | `&raquo;` | 右尖引号 |
| `&#188;` | ¼ | `&frac14;` | 四分之一分数 |
| `&#189;` | ½ | `&frac12;` | 二分之一分数 |
| `&#190;` | ¾ | `&frac34;` | 四分之三分数 |
| `&#191;` | ¿ | `&iquest;` | 倒问号 |
| `&#192;` | À | `&Agrave;` | 大写 A，重音符号 |
| `&#193;` | Á | `&Aacute;` | 大写 A，锐音符号 |
| `&#194;` | Â | `&Acirc;` | 大写 A，扬抑符 |
| `&#195;` | Ã | `&Atilde;` | 大写 A，波浪符 |
| `&#196;` | Ä | `&Auml;` | 大写 A，变音符号 |
| `&#197;` | Å | `&Aring;` | 大写 A，上圆环 |
| `&#198;` | Æ | `&AElig;` | 大写 AE 连字 |
| `&#199;` | Ç | `&Ccedil;` | 大写 C，软音符 |
| `&#200;` | È | `&Egrave;` | 大写 E，重音符号 |
| `&#201;` | É | `&Eacute;` | 大写 E，锐音符号 |
| `&#202;` | Ê | `&Ecirc;` | 大写 E，扬抑符 |
| `&#203;` | Ë | `&Euml;` | 大写 E，变音符号 |
| `&#204;` | Ì | `&Igrave;` | 大写 I，重音符号 |
| `&#205;` | Í | `&Iacute;` | 大写 I，锐音符号 |
| `&#206;` | Î | `&Icirc;` | 大写 I，扬抑符 |
| `&#207;` | Ï | `&Iuml;` | 大写 I，变音符号 |
| `&#208;` | Ð | `&ETH;` | 大写 Eth，冰岛语 |
| `&#209;` | Ñ | `&Ntilde;` | 大写 N，波浪符 |
| `&#210;` | Ò | `&Ograve;` | 大写 O，重音符号 |
| `&#211;` | Ó | `&Oacute;` | 大写 O，锐音符号 |
| `&#212;` | Ô | `&Ocirc;` | 大写 O，扬抑符 |
| `&#213;` | Õ | `&Otilde;` | 大写 O，波浪符 |
| `&#214;` | Ö | `&Ouml;` | 大写 O，变音符号 |
| `&#215;` | × | `&times;` | 乘号 |
| `&#216;` | Ø | `&Oslash;` | 大写 O，斜杠 |
| `&#217;` | Ù | `&Ugrave;` | 大写 U，重音符号 |
| `&#218;` | Ú | `&Uacute;` | 大写 U，锐音符号 |
| `&#219;` | Û | `&Ucirc;` | 大写 U，扬抑符 |
| `&#220;` | Ü | `&Uuml;` | 大写 U，变音符号 |
| `&#221;` | Ý | `&Yacute;` | 大写 Y，锐音符号 |
| `&#222;` | Þ | `&THORN;` | 大写 THORN，冰岛语 |
| `&#223;` | ß | `&szlig;` | 小写 sz 连字，德语 |
| `&#224;` | à | `&agrave;` | 小写 a，重音符号 |
| `&#225;` | á | `&aacute;` | 小写 a，锐音符号 |
| `&#226;` | â | `&acirc;` | 小写 a，扬抑符 |
| `&#227;` | ã | `&atilde;` | 小写 a，波浪符 |
| `&#228;` | ä | `&auml;` | 小写 a，变音符号 |
| `&#229;` | å | `&aring;` | 小写 a，上圆环 |
| `&#230;` | æ | `&aelig;` | 小写 ae 连字 |
| `&#231;` | ç | `&ccedil;` | 小写 c，软音符 |
| `&#232;` | è | `&egrave;` | 小写 e，重音符号 |
| `&#233;` | é | `&eacute;` | 小写 e，锐音符号 |
| `&#234;` | ê | `&ecirc;` | 小写 e，扬抑符 |
| `&#235;` | ë | `&euml;` | 小写 e，变音符号 |
| `&#236;` | ì | `&igrave;` | 小写 i，重音符号 |
| `&#237;` | í | `&iacute;` | 小写 i，锐音符号 |
| `&#238;` | î | `&icirc;` | 小写 i，扬抑符 |
| `&#239;` | ï | `&iuml;` | 小写 i，变音符号 |
| `&#240;` | ð | `&eth;` | 小写 eth，冰岛语 |
| `&#241;` | ñ | `&ntilde;` | 小写 n，波浪符 |
| `&#242;` | ò | `&ograve;` | 小写 o，重音符号 |
| `&#243;` | ó | `&oacute;` | 小写 o，锐音符号 |
| `&#244;` | ô | `&ocirc;` | 小写 o，扬抑符 |
| `&#245;` | õ | `&otilde;` | 小写 o，波浪符 |
| `&#246;` | ö | `&ouml;` | 小写 o，变音符号 |
| `&#247;` | ÷ | `&divide;` | 除号 |
| `&#248;` | ø | `&oslash;` | 小写 o，斜杠 |
| `&#249;` | ù | `&ugrave;` | 小写 u，重音符号 |
| `&#250;` | ú | `&uacute;` | 小写 u，锐音符号 |
| `&#251;` | û | `&ucirc;` | 小写 u，扬抑符 |
| `&#252;` | ü | `&uuml;` | 小写 u，变音符号 |
| `&#253;` | ý | `&yacute;` | 小写 y，锐音符号 |
| `&#254;` | þ | `&thorn;` | 小写 thorn，冰岛语 |
| `&#255;` | ÿ | `&yuml;` | 小写 y，变音符号 |

如前所述，数值 128–159 在 HTML 的 Latin 1 或 Unicode 字符集中并未使用。但是，某些浏览器（如 Internet Explorer）可以识别这些数值，它们被称为代码页 1252（CP1252）或 C1 超集。下表列出了分配给该字符集的 C1 和 Unicode 数值。Unicode 使用的数值与 Latin 1 一样，必须始终以 `&#` 开头并以分号结尾。

### HTML 可识别的 Unicode 示例（ISO 10646-1）

| Unicode | 符号 | C1 超集 | 描述 |
| --- | --- | --- | --- |
| `&#8218;` | , | `&#130;` | 低位单引号 |
| `&#402;` | ƒ | `&#131;` | 弗罗林符号 |
| `&#8222;` | „ | `&#132;` | 低位双引号 |
| `&#8230;` | … | `&#133;` | 省略号 |
| `&#8224;` | † | `&#134;` | 匕首符号 |
| `&#8225;` | ‡ | `&#135;` | 双匕首符号 |
| `&#710;` | ^ | `&#136;` | 扬抑符 |
| `&#8240;` | ‰ | `&#137;` | 千分号 |
| `&#352;` | Š | `&#138;` | 大写 S，倒扬抑符 |
| `&#8249;` | ‹ | `&#139;` | 单左尖引号 |
| `&#338;` | Œ | `&#140;` | 大写 OE 连字 |
| `&#8216;` | ‘ | `&#145;` | 左单引号 |
| `&#8217;` | ’ | `&#146;` | 右单引号 |
| `&#8220;` | `"` | `&#147;` | 左双引号 |
| `&#8221;` | `"` | `&#148;` | 右双引号 |
| `&#8226;` | • | `&#149;` | 项目符号 |
| `&#8211;` | – | `&#150;` | 短破折号 |
| `&#8212;` | — | `&#151;` | 长破折号 |
| `&#732;` | ~ | `&#152;` | 小波浪符 |
| `&#8482;` | ™ | `&#153;` | 商标符号 |
| `&#353;` | š | `&#154;` | 小写 s，倒扬抑符 |
| `&#8250;` | › | `&#155;` | 单右尖引号 |
| `&#339;` | œ | `&#156;` | 小写 oe 连字 |
| `&#376;` | Ÿ | `&#159;` | 大写 Y，变音符号 |

## 第 6 节 XHTML 模块

| XHTML 模块 | HTML 元素 | 参考 |
| --- | --- | --- |



| 结构模块（必需） | `body`, `head`, `html`, `title` | 第 2 章 第 34 页，第 32 页，第 29 页，第 32 页 |
|---|---|---|
| 超文本模块（必需） | `a` | 第 3 章 第 59 页 |
| 列表模块（必需） | `dd`, `dl`, `dt`, `li`, `ol`, `ul` | 第 4 章 第 102 页，第 101 页，第 102 页，第 88 页，第 83 页，第 92 页 |
| 文本模块（必需） | `abbr`, `acronym`, `address`, `blockquote`, `br`, `cite`, `code`, `dfn`, `div`, `em`, `h1`, `h2`, `h3`, `h4`, `h5`, `h6`, `kbd`, `p`, `pre`, `q`, `samp`, `span`, `strong`, `var` | 第 124 页，第 124 页，第 123 页，第 125 页，第 43 页，第 125 页，第 121 页，第 124 页，第 215 页，第 124 页，第 39 页，第 121 页，第 40 页，第 130 页，第 126 页，第 124 页，第 218 页，第 123 页，第 124 页 |
| 基础模块 | `base` | 第 12 章 第 285 页 |
| 双向文本模块 | `bdo` |  |
| 客户端图像映射模块 | `area`, `map` | 第 14 章 第 414 页，第 414 页，第 413 页 |
| 编辑模块 | `del`, `ins` | 第 5 章 第 126 页，第 126 页，第 126 页 |
| 表单模块 | `button`, `fieldset`, `form`, `input`, `label`, `legend`, `select`, `optgroup`, `option`, `textarea` | 第 11 章 第 324 页，第 324 页，第 334 页，第 301 页，第 307 页，第 336 页，第 334 页，第 328 页，第 333 页，第 332 页，第 325 页 |
| 图像模块 | `img` | 第 6 章 第 144 页 |
| 内置事件模块 | `onblur`, `onchange`, `onclick`, `ondblclick`, `onfocus`, `onkeydown`, `onkeypress`, `onkeyup`, `onload`, `onmousedown`, `onmousemove`, `onmouseout`, `onmouseover`, `onmouseup`, `onreset`, `onselect`, `onsubmit`, ` onunload` | 第 13 章 第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页，第 388 页 |
| 链接模块 | `link` | 第 8 章 第 210 页 |
| 元信息模块 | `meta` | 第 12 章 第 356 页 |

## XHTML 模块

| XHTML 模块 | HTML 元素 | 参考 |
|---|---|---|
| 对象模块 |  | 第 9 章 第 245 页 |
|  | `object` | 第 249 页 |
|  | `param` | 第 249 页 |
| 演示模块 | `b` | 第 121 页 |
|  | `big` | 第 121 页 |
|  | `hr` | 第 43 页 |
|  | `i` | 第 121 页 |
|  | `small` | 第 121 页 |
|  | `sub` | 第 121 页 |
|  | `sup` | 第 121 页 |
|  | `tt` | 第 121 页 |
| 脚本模块 |  | 第 13 章 第 377 页 |
|  | `noscript` | 第 377 页 |
|  | `script` | 第 377 页 |
| 服务器端图像映射模块 | 使用 `ismap` 属性的 `img` | 第 14 章 第 411 页 |
| 样式表模块 | `style` | 第 5 章 第 111 页 |
| 表格模块 |  | 第 7 章 第 193 页 |
|  | `caption` | 第 193 页 |
|  | `col` | 第 197 页 |
|  | `colgroup` | 第 195 页 |
|  | `table` | 第 171 页 |
|  | `tbody` | 第 201 页 |
|  | `td` | 第 186 页 |
|  | `tfoot` | 第 200 页 |
|  | `th` | 第 186 页 |
|  | `thead` | 第 199 页 |
|  | `tr` | 第 184 页 |

# 第七节

## JavaScript 对象

### 用于更出色的 HTML

JavaScript 对象及相关属性、方法和事件的完整列表，请参阅 W3C 网站。

| 对象 | 属性 | 方法 | 事件 | 参考 |
|---|---|---|---|---|
| `Date` |  | `getDate`, `getDay`, `getFullYear`, `getHours`, `getMilliseconds`, `getMinutes`, `getMonth`, `getSeconds`, `getTime`, `getYear` |  | 第 13 章 第 386 页及图 13.8 |
| `Document` | `alinkColor`, `anchors()`, `applets`, `bgColor`, `cookie`, `domain`, `form()`, `fgColor`, `images()`, `lastModified`, `linkColor`, `links()`, `referrer`, `title`, `URL`, `vlinkColor` | `close`, `open`, `write`, `writeln` | `onBlur`, `OnError`, `onFocus`, `onLoad`, `onUnloaded` | 第 13 章 第 389 页 |

## 第 7 节 JAVASCRIPT 对象

| 对象 | 属性 | 方法 | 事件 | 参考 |
|---|---|---|---|---|
| `Navigator` | `appCodeName`, `appName`, `appVersion`, `language`, `platform`, `userAgent` | `javaEnabled()` |  | 第 13 章 第 398 页 |
| `Window` | `closed`, `defaultStatus`, `document`, `frames()`, `history`, `location`, `name`, `opener`, `parent`, `self`, `status`, `statusbar`, `top`, `window` | `alert()`, `blur()`, `clearTimeout()`, `close()`, `confirm()`, `focus()`, `open()`, `prompt()`, `setTimeout()` | `onBlur`, `OnError`, `onFocus`, `onLoad`, `onResize`, `onUnloaded` | 第 13 章 第 398 页 |

本文档由 Anna's Archive 于 2023-2024 年间生成，属于 DuXiu 馆藏的一部分（https://annas-blog.org/duxiu-exclusive.html）。

图片已无损嵌入。原始文件信息可在 PDF 附件中找到。部分统计信息（更多内容见 PDF 附件）：

```json
{
  "filename": "NDAzODg0NzluemlW",
  "filename_decoded": "40388472.zip",
  "filesize": 28830394,
  "md5": "ddad4d0422385708fee347e537dff51f",
  "header_md5": "139791910a4c1955e1286b4052dece7a",
  "sha1": "0c42f93fb4a17635874cda91c63ef598625e6d91",
  "sha256": "5d79abcc18d7fbb025b11598b84e87b9ae2e082def6de7592ffd730425943455",
  "crc32": 1104447352,
  "zip_password": "",
  "uncompressed_size": 30911944,
  "pdg_dir_name": "EVEN MORE EXCELLENT HTML REFERENCE GUIDE_40388472",
  "pdg_main_pages_found": 56,
  "pdg_main_pages_max": 56,
  "total_pages": 61,
  "total_pixels": 456192001,
  "pdf_generation_missing_pages": false
}
```

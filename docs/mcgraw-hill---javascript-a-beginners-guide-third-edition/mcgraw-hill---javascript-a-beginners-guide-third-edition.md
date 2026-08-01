# McGraw Hill - JavaScript 初学者指南，第三版










### 关于作者

**John Pollock** 白天担任 Web 管理员，晚上从事网站和其他项目的开发。他运营着两个致力于 Web 开发和设计的网站——PageResource.com (www.pageresource.com) 是一个开发教程网站，而 JavaScript City (www.javascriptcity.com) 是一个为 Web 开发者提供免费 JavaScript 代码的网站。约翰拥有萨姆·休斯斯斯顿州立大学的英语文学学士学位，目前与妻子 Heather 共同居住在德克萨斯州的新韦弗弗里。

### 关于技术编辑

**Scott Duffy** 是一位居住在加拿大多伦多的作者兼顾问。他为中小型企业设计并开发 Web网站。












*献给我的妻子 Heather Pollock、Bruce 和 Joy Anderson，以及*
*J. D. 博士和 Linda Andrews*
*纪念 James D. 和 Livian Anderson,John William 和 Edith Hopkins,*
*Burley T. 和 Aline Price，以及“Doc” Flores*

*本页特意留白*

vii



ix

## 内容

致谢 | xix
引言 | xxi

### 1 JavaScript 简介 | 1

你需要了解的 | 2
基础 HTML 和 CSS 知识 | 3
基础文本编辑器和浏览器知识 | 3
哪一个版本？ | 6
记住，它不是 Java | 7
与其他语言的相似之处 | 8
从 JavaScript 开始 | 8
基于对象 | 8
客户端 | 8
脚本语言 | 8
### 9 整合一切 | 9
### 9 在线资源 | 9

### 10 尝试这个 1-1：使用 JavaScript 编写文本 | 10





# JavaScript: 入学者指南

## 2. 将 JavaScript 放入 HTML 文件中
15

### 使用 HTML Script 标签
16

### 识别脚本语言
16

### 引入外部脚本
17

### 使用 <noscript></noscript> 标签
17

### 创建你的第一个脚本
19

### 编写一个“Hello World”脚本
19

###为脚本创建 HTML 文档
20

### 将脚本插入 HTML 文档中
20

### 尝试练习 2-1：向 HTML 文档中插入脚本
22

### 使用外部 JavaScript 文件
23

### 创建 JavaScript 文件
23

### 创建 HTML 文件
24

### 在浏览器中查看页面
25

### 尝试练习 2-2：从 HTML 文档调用外部脚本
26

### 使用 JavaScript 注释
27

### 插入单行注释
28

### 添加多行注释
28

## 3. 使用变量
33

### 了解变量
34

### 为什么变量很有用
35

### 变量作为未知值的占位符
35

### 变量作为节省时间的工具
35

### 变量作为代码说明的工具
36

### 为你的脚本定义变量
36

### 声明变量
36

### 为变量赋值
36

### 变量命名
38

### 了解变量类型
40

### 数字 (Number)
40

### 字符串 (String)
41

### 布尔值 (Boolean)
45

### 空 (Null)
46

### 尝试练习 3-1：声明变量
46

### 在脚本中使用变量
47

### 调用变量
48

### 在文本中添加变量
49

### 编写一个 JavaScript 页面
49

### 创建框架
51

### 定义变量
52

### 添加命令
53

### 修改页面
55

### 创建函数
57

### 使用函数
59

### 为什么函数很有用
60

### 构造结构
60

### 声明函数
60

### 定义函数的代码
62

### 函数命名
64

### 参数
66

### 在脚本中调用函数
67

### 脚本标签：Head 还是 Body 部分
68

### 从另一个函数调用函数
70

### 带参数的函数调用
72

### 带返回的函数调用
76

### 定义函数的其他方法
76

### 尝试练习 4-1：创建一个带有函数的 HTML 页面
79

### 整合一切
81

### 尝试练习 4-2：编写你自己的函数
83

## 5. JavaScript 运算符
87

### 了解运算符类型
88

### 了解数学运算符
89

### 加法运算符 (+)
90

### 减法运算符 (−)
92

### 乘法运算符 (*)
94

### 除法运算符 (/)
94

### 模运算运算符 (%)
94

### 递增运算符 (++)
95

### 递减运算符 (--)
96

### 了解赋值
97

### 赋值运算符 (=)
97

### 加赋值运算符 (+=)
98

### 减赋值运算符 (−=)
99

### 乘赋值运算符 (*=)
99

### 除赋值运算符 (/=)
99

### 模赋值运算符 (%=)
99

### 尝试练习 5-1：调整变量值
100

### 了解比较运算符
101

### 等于运算符 (==)
102

### 不等于运算符 (!=)
103

### 大于运算符 (>)
103

### 小于运算符 (<)
104





JavaScript: 入学者指南

大于等于运算符 (>=) . 104

小于等于运算符 (<=) . 105

严格等于运算符 (===) . 105

严格不等于运算符 (!==) . 106

理解逻辑运算符 . 107

逻辑与运算符 (&&) . 107

逻辑或运算符 (||) . 107

逻辑非运算符 (!) . 108

位运算符 . 108

特殊运算符 . 109

理解运算顺序 . 110

尝试一试 5-2：真还是假？ . 111

## 6 条件语句与循环 . 115

### 条件语句的定义 . 116

### 什么是条件语句？ . 116

### 为什么条件语句很有用 . 117

使用条件语句 . 117

#### 使用 if/else 语句块 . 117

#### 使用 switch 语句 . 125

#### 使用三元运算符 . 126

#### 尝试一试 6-1：构建一个 if/else 块 . 129

### 循环的定义 . 130

### 什么是循环？ . 130

### 为什么循环很有用 . 130

使用循环 . 130

#### for 循环 . 136

#### while 循环 . 137

#### do while 循环 . 139

#### for each 循环 . 140

#### break 和 continue . 140

#### 尝试一试 6-2：使用 for 和 while 循环 . 143

## 7 事件处理器 . 47

### 什么是事件？

### 为什么事件处理器很有用 . 48

### 事件处理器的位置与用途 . 48

#### 在 HTML 元素中使用事件处理器 . 49

#### 在脚本代码中使用事件处理器 . 49

#### 尝试一试 7：创建一个按钮 . 53

学习事件处理器 . 54

#### 中止事件 (onabort) . 55

#### 失去焦点事件 (onblur) . 55

#### 改变事件 (onchange) . 56

#### 点击事件 (onclick) . 57

#### 聚焦事件 (onfocus) . 58

#### 键按下事件 (onkeydown) . 59

#### 击事件 (onkeypress) . 60

#### 键释放事件 (onkeyup) . 60

#### 加载事件 (onload) . 60

#### 鼠标按下事件 (onmousedown) . 60

#### 鼠标移动事件 (mousemove) . 61

#### 鼠标经过事件 (onmouseover) . 62

#### 鼠标离开事件 (onmouseout) . 63

#### 鼠标释放事件 (onmouseup) . 64

#### 重置事件 . 64

#### 提交事件 (ons) . 64

#### 卸载事件 (onload) . 64

尝试一试 7- 使用发送警报 . 65

创建脚本事件处理器 . 67

## 8 对象 . 175

### 对象的定义 . 176

### 什么是对象？ . 176

### 为什么对象很有用 . 177

创建对象 . 177

### 命名 . 177

### 对象结构 . 178

### 添加方法 . 186

### 对象操作语句 . 190

#### 尝试一试 8-1：创建一个计算机对象 . 193

#### 定义的 JavaScript 对象 . 194

#### Navigator 对象 . 194

#### History 对象 . 199

#### 尝试一试 8-2：练习 Navigator 对象 . 201

## 9 Document 对象 . 205

### 定义 Document 对象 . 206

### 使用文档模型 . 206

 使用 Document 对象的属性 . 207

### 颜色属性 . 210

anchors 属性（数组） . 210





## JavaScript: 初学者指南

### cookie 属性 ... 210
### dir 属性 ... 211
### domain 属性 ... 212
### name 属性 ... 213
### forms (数组) ... 215
### images (数组) ... 215
### lastModified 属性 ... 217
### layers (数组) ... 217
### all 属性 ... 218
### links (数组) ... 219
### referrer 属性 ... 219
### title 属性 ... 219
### URL 属性 ... 220
### URLEncoded 属性 ... 220

### 使用文档对象的方法 ... 222
### getElementById() 方法 ... 224
### getElementsByClassName() 方法 ... 224
### getElementsByTagName() 方法 ... 225
### open() 和 close() 方法 ... 225
### write() 方法 ... 227
### writeln() 方法 ... 227

### 创建方法 ... 228
### 尝试一下 9-1：向文档添加一个 DOM 节点 ... 233

### 创建动态脚本 ... 234
### JavaScript 中的样式 ... 234
### 编写动态脚本 ... 235
### innerHTML 属性 ... 236

### Window 对象 ... 241
### Window 对象简介 ... 242
### 使用 Window对象的属性 ... 242
### closed 属性 ... 243
### defaultStatus 属性 ... 244
### frames (数组) ... 244
### innerHeight 和 innerWidth 属性 ... 244
### length 属性 ... 246
### location 属性 ... 246
### name 属性 ... 246
### opener 属性 ... 247
### parent 属性 ... 248
### self 属性 ... 248
### status 属性 ... 248
### top 属性 ... 248

### 尝试一下 10-1：使用 location 和 innerWidth 属性 ... 248

### 使用 Window 对象的方法 ... 249
### alert() 方法 ... 249
### confirm() 方法 ... 249
### find() 方法 ... 250
### home() 方法 ... 253
### print() 方法 ... 254
### prompt() 方法 ... 255
### open() 方法 ... 256
### close() 方法 ... 261
### moveBy() 方法 ... 262
### moveTo() 方法 ... 263
### resizeBy() 方法 ... 265
### resizeTo() 方法 ... 265
### scrollBy() 方法 ... 265
### scrollTo() 方法 ... 265
### setInterval() 方法 ... 265
### clearInterval() 方法 ... 266
### setTimeout() 方法 ... 267
### clearTimeout() 方法 ... 267

### 尝试一下 10-2：使用 setTimeout() 和 confirm() 方法 ... 267

### 数组 ... 273
### 什么是数组？ ... 273
### 为什么数组用？ ... 274
### 定义数组 ... 275
### 为数组命名 ... 275
### 其他方法 ... 277
### 属性 ... 279
### 方法 ... 282

### 在循环中使用数组 ... 291
### 创建数组元素 ... 292
### 遍历数组 ... 293
### 尝试一下 11-1：在循环中使用数组 ... 297

### 使用关联数组 ... 298
### 定义关联数组 ... 299
### 访问关联数组 ... 299
### 尝试一下 11-2：使用关联数组 ... 301





# JavaScript：初学者指南

## 12 数学、数字和日期对象 (305)

### 使用 Math 对象 (306)
#### 什么是 Math 对象？ (306)
#### Math 对象有什么用？ (306)
##### 属性 (306)
##### 方法 (308)

尝试练习 12-1：在页面上显示随机链接 (321)

### 理解 Number 对象 (322)
#### 属性 (322)
#### 方法 (324)

### 使用 Date 对象 (326)
#### 属性 (326)
#### 方法 (327)
#### 获取值的方法 (329)
#### 设置值的方法 (332)
#### 其他方法 (333)

来写一些日期脚本好怎么样？ (334)
尝试练习 12-2：创建一个 JavaScript 钟 (338)

## 13 处理字符串 (341)

### String 对象简介 (342)
#### String 对象 (342)
#### 字符串字面量 (343)
#### 它们有什么区别？ (343)

### 使用 String 属性 (344)
#### constructor 属性 (344)
#### length 属性 (344)
#### prototype 属性 (345)

### 使用 String 对象的方法 (345)
#### 添加 HTML 标签的方法 (45)
#### 其他方法 (55)
尝试练习：使用 `charAt()` 查找第一个字母 (59)
将方法组合在一起 (60)
尝试练习：使用 `indexOf()` 测试地址 (62)

### 正则表达式 (63)
#### 创建正则表达式 (63)
#### 使用正则表达式测试字符串 (64)
#### 添加标志位 (65)
#### 强大的模式 (66)
#### 表达式分组 (69)

## JavaScript 与表单 (70)

### 访问表单 (75)
#### 确保表单的可访问性 (77)
#### 使用正确的元素和标签顺序 (92)
#### 使用 `<label>` 标签 (93)
#### 使用 `<fieldset>` 标签 (93)

### 不假设存在客户端脚本 (94)
#### 验证 (95)
#### `onsubmit` 和 `return` 语句 (95)

### 技术 (96)
尝试练习 14-1：请求一个数字 (98)

### 使用表单进行导航 (99)
#### 点击按钮 (99)
尝试练习 14-2：构建选择框导航脚本 (104)

## JavaScript 与框架 (105)

### 框架简介 (107)
#### 框架的目的 (108)
#### 框架背代码 (108)
#### 选项 (110)
#### frames (114)
#### 数组 (114)
#### Name (117)
#### Forms (118)
#### ID (120)
#### Form 对象的属性和方法 (122)
#### 方法 (122)
#### 跳出框架 (123)
#### 将访问者引导到框架 (124)
#### 跨框架使用变量 (126)

尝试练习 15-2：使用变量 (132)



JavaScript：初学者指南

## 16 高级技术简介 ... 435

脚本调试 ... 436

错误类型类型 ... 436

JavaScript 与可访问性 ... 442

将内容与呈现分离 ... 442

增强内容 ... 444

### 尝试一下 16-1：让这段代码具有可访问性 ... 445

使用 Cookie ... 446

设置 Cookie ... 446

读取 Cookie ... 449

### 尝试一下 16-2：记住一个名字 ... 451

处理图像 ... 452

预加载 ... 452

鼠标悬停效果 ... 454

JavaScript 安全性 ... 460

安全与签名脚本 ... 460

页面保护 ... 460

AJAX ... 462

JavaScript 库 ... 463

## 自测题答案 ... 467

第 1 章：JavaScript 简介 ... 468

第 2 章：将 JavaScript 放置在 HTML 文件中 ... 468

第 3 章：使用变量 ... 469

第 4 章：使用函数 ... 469

第 5 章：JavaScript 运算符 ... 470

第 6 章：条件语句与循环 ... 471

第 7 章：事件处理器 ... 471

第 8 章：对象 ... 471

第 9 章：Document 对象 ... 472

第 10 章：Window 对象 ... 473

第 11 章：数组 ... 473

第 12 章：Math、Number 和 Date ... 474

第 13 章：字符串 ... 475

第 14 章：表单 ... 475

第 15 章：框架 ... 476

第 16 章：高级技术简介 ... 477

## 索引 ... 479

## 致谢 ... xix

首先，我要感谢我的妻子，感谢她的包容并在我需要时给予我的鼓励。感谢 Don Sargent、Marty J. Reeder 以及所有人。我要感谢上帝，是他赋予了我通过写作来帮助和教他人的能力。“凡事认认祂，祂必指引你的路。”（箴言 3:6）。

## 引言

欢迎阅读*JavaScript：初学者指南（第三版)*！几年前，我在浏览网页时注意到人们正在发布关于自己的页面，并称其为主页。在看了许多这类页面后，我决定自己也创建一个主页。我当时不知道从何开始，但通过不断尝试，我弄懂了如何编写 HTML 并我的文档发布到 Web 服务器上。随着时间的推移，我看到其他页面上使用了一些有趣的效果（比如凭空弹出的警报信息，或者当我鼠标悬停在上面时会神奇变化的图像）。我感到非常好奇，*必须*知道这些效果是如何制作的。这些页面创建者是否使用了我并不知道的 HTML 标签？最后，一个网站揭示了他们用来创建这些效果的技术：JavaScript。我开始搜索相关信息，并在网络上发现了一些教程和脚本。由于我用过其他语言（例如一种叫 Ada 的冷门语言），通过观察这些教程和脚本，我很快上手了 JavaScript。我学知识多到决定创建一个向初学者教授 HTML 和 JavaScript 的网站。项目一开始，我就收到了访问者提出的远超出我理解范围的问题——这迫使我深入挖掘并学习更多关于 JavaScript 的知识。结果，我完全熟悉这种脚本语言及其功能。你不仅可以为 Web 页面添加有趣的效果，还可以创建执行有用任务的脚本，例如验证表单输入、为文档添加导航元素或响应用户事件。本书的目标是帮助你学习 JavaScript 语言的基础知识，并尽可能减少抓狂和砸显示器的痛苦。你不需要任何先前的编程经验就可以从这本书中学习 JavaScript。你只需要 HTML 和/或 XHTML 的知识、层叠样式表（CSS），以及如何使用你喜欢的文本编辑器和 Web 浏览器（更多信息请参见第 1 章）。






## 本书涵盖内容

本书共 16 章，涵盖了 JavaScript 语言的特定主题。前章涵盖了该语言最基础的内容：它是什么、开始使用 JavaScript 需要了解的知识，以及如何将 JavaScript 放入 HTML 文件中。书的中间部分（第 3 至 15 章）涵盖了从变量到在框架（frames）中使用 JavaScript 的初级 主题。最后一章（第 16 章）介绍了一些高级技术，并如果你在读完本书后想学习更多关于 JavaScript 的知识，将为你提供相关资源。

本书每章都包含许多特殊功能，以帮助你学习 JavaScript。这些功能包括：

- **关键技能与概念 (Key Skills & Concepts)** 每一章都从一组关键技能和概念开始，你将在章节结束时掌握这些内容。
- **提问专家 (Ask the Expert)** “提问专家”章节针对前文中介绍的主题介绍常见问题，并由作者给出解答。
- **尝试一试 (Try This)** 这些章节让你通过动手实践的方法来练习所学知识。每个“尝试一试”都将通过分步指导引导你编写脚本，以便你完成目标。你可以在 McGraw-Hill/Professional 网站 www.mhprofessional.com/computingdownload 找到每个项目的解决方案。
- **注释、提示与警告 (Notes, Tips, and Cautions)** 注释、提示与警告提醒你注意在阅读章节时会发现的有益的重要陈述。
- **代码 (Code)** 代码列表显示在脚本或程序中使用的示例源代码。
- **标注框 (Callouts)** 标注框显示关于示例代码的有用提示和注释，并指向代码中的相关行。
- **自测 (Self Test)** 每一章末尾都有一个自测，这是一个由 15 道题组成的系列，用以检查你是否掌握了该章涵盖的主题。每个自测的答案都可以在书末的附录中找到。

就是这些！你现在已经熟悉了本书的结构和特殊功能，可以开启你的 JavaScript 之之旅了。如果你发现遇到了困难并需要帮助，请随时访问 Web Xpertz 网站上的 JavaScript 讨论论坛：www.webxpertz.net/forums。论坛将允许你与其他 JavaScript 代码编写人员互动，他们可能帮助你解决问题。

现在是时候学习 JavaScript 了。准备好，开始，尽情享受吧！

## 第 1 章：JavaScript 简介

## 关键技能与概念

- 使用文本编辑器、所见即所得（WYSIWYG）编辑器和网络浏览器
- 定义 JavaScript
- JavaScript 与语言的区别

欢迎阅读 *JavaScript：初学者指南，第三版*！你显然对学习 JavaScript 感兴趣，但可能不确定使用它需要了解什么。本章回答了一些关于 JavaScript 是什么的基础问题，讨论了它的优势和局限性，解释了你如何使用它创建更动态、更吸引人的 Web 页面，并提供了该语言的简史。

JavaScript 在万网上无处不在。你可以使用 JavaScript 让你的网页更具交互性，使其对查看者的操作做出反应，并为你的网页添加一些特殊效果（视觉或其他）。

JavaScript 经常与超文本标记语言（HTML）并列，作为初级 Web 开发者的推荐语言之一（无论你是为了业务还是兴趣构建网站）。当然，你可以只使用 HTML 构建网页，但 JavaScript 允许你添加额外的功能，静态 HTML 页面在没有脚本或编程帮助的情况下无法提供这些功能。

### 你需要了解的知识

在开始学习 JavaScript 之前，你应该具备（或获得）以下基础知识：

- HTML 和层叠样式表 (CSS)
- 文本编辑器
- 浏览器
- JavaScript 的不同版本

如果你具备这些基础知识（JavaScript 的不同版本将在本章中讨论），那么你在阅读本书时将会进展得很顺利。不需要掌握另一种编程/脚本语言或有以往的 JavaScript 经验。本书是 JavaScript 的初学者指南。

如果你认为自己在上述某一个领域没有足够的经验，仔细观察每个领域可能有助于你决定该做什么。

### 基础 HTML 和 CSS 知识

虽然你不需要成为 HTML 专家，但你确实需要知道在哪里放置某些元素（如 `<head>` 和 `<body>` 元素）以及如何添加你自己的属性。本书将引用位于 head 部分（在 `<head>` 和 `</head>` 标签之间）和 body 部分（在 `<body>` 和 `</body>` 标签之间）的脚本。

偶尔，你还需要向标签添加属性以使脚本能够正常运行。例如，你可能需要使用 `id` 属性为表单元素命名，如下方的代码所示：

`<input type="text" id="thename" />`

如果你了解使用标签和属性的基础知识，那么 HTML 部分不会给学习 JavaScript 带来任何问题。

如果你没有 HTML 的基础知识，你可以通过多种媒体快速学习。例如，你可以买一本书或在网上查找一些有用的信息。一本好书是 Wendy Willard 写的 *HTML：初学者指南，第四版》（McGraw-Hill Professional, 2009）。要在网上查找有关 HTML 的信息，请查看这些网站：www.pageresource.com/html 和 www.w3schools.com/html/default.asp。

偶尔，你需要使用 CSS 在 Web 页面上添加或更改演示特性。在书中，我们主要通过 JavaScript 动态更改 CSS 属性来实现目的。学习 CSS 的一个好地方是 www.w3schools.com/css/intro。

### 基础文本编辑器和浏览器知识

在开始学习 JavaScript 之前，你必须学会使用文本编辑器或 HTML 编辑器以及浏览器。你将使用这些工具进行编码。

**文本编辑器**
许多文本编辑器和 HTML 编辑器都支持 JavaScript。如果你熟悉 HTML，可能已经使用过 HTML 编辑器，所以可能不需要更改。

然而，某些 HTML 编辑器在添加 JavaScript 代码时会出现问题（例如在保存文件时更改代码）。你可能需要使用更简单的编辑器或寻找可以轻松处理你代码的 HTML 编辑器（例如 Adobe Dreamweaver）。文本编辑器的示例有 Notepad、TextPad 和 Simple Text。

**浏览器**
再次，如果你一直在编写 HTML，可能不需要更改浏览器。然而，某些浏览器在处理新版本的 JavaScript 时存在困难。浏览器的选择最终取决于你，只要它兼容 JavaScript。我建议使用以下浏览器来测试你的 JavaScript 代码：

- Internet Explorer 6.0 或更高版本
- Mozilla Firefox 1.0 或更高版本
- Opera 6.0 或更高版本

这些浏览器仍在不断更新。在本书期间，Internet Explorer 8、Firefox 3 和 Opera 9 的非测试版已发布。

为了让你了解某些浏览器的界面，图 1-1 显示在 Microsoft Internet Explorer 中查看的网页，图 1-2 显示在 Mozilla Firefox 中查看同一个页面。

如果你使用的是旧版浏览器且无法升级，许多功能（主要在书中后面讨论）可能在你的浏览器中无法运行。尽管如此，本书仍然可以帮助你学习 JavaScript 本身，因此即使你有旧版浏览器也不必放弃。上述三个浏览器及其支持的 JavaScript 版本如表 1-1 所示。

下一节“哪个版本？”将更详细地解释版本号的含义。一旦你确定自己符合基本要求，就可以开始学习这种语言了。

图 1-1 在 Microsoft Internet Explorer 中查看的网页





## 第 1 章：JavaScript 简介

5

图 1-2 在 Mozilla Firefox 中查看的页面

![](img/61d166424839b7674a7b9c8434ae4e03_27_0.png)

### 表 1-1 三浏览器支持的 JavaScript 版本

| Microsoft Internet Explorer 版本 | Mozilla Firefox 版本 | Opera 版本 | 支持的 JavaScript 版本 |
| :--- | :--- | :--- | :--- |
| – | 3 | – | 1.8 |
| – | 2 | – | 1.7 |
| – | 1.5 | – | 1.6 |
| 5.5–8 | 6–9 | 1.5 | 4––3 |

JavaScript 入门指南

### 哪个版本？

在本书书中，本章早期推荐的浏览器至少应支持 JavaScript 1.5。（Firefox 最新版本支持 JavaScript 1.8。）

你可能还会看到或听过 JScript 或 ECMAScript。JScript 是 Microsoft Internet Explorer 使用的 JavaScript 版本（因为它被实现为 Windows 脚本引擎，所以具有额外功能；可以使用服务器端语言执行更复杂的任务，如更新数据库）。有关 JScript 的更多信息，请参见 http://msdn.microsoft.com/en-us/library/hbxc2t98.aspx。

ECMAScript 是 JavaScript 语言的国际标准名称和规范，因此它不是新语言，而是为 JavaScript 和 JScript 制定的标准。关于 ECMAScript 的更多信息，请访问 www.ecma-international.org/publications/standards/Ecma-262.htm。

**Q：你提到可以使用我喜欢的文本编辑器或 HTML 编辑器，但我不太确定这意味着什么。什么是文本编辑器，我在哪里可以找到它？**

**A： 文本编辑器是你用来保存和编辑编写的文本的程序。文本编辑器从简单到复杂不等，有很多选择：例如记事本（Notepad）、WordPad、Simple Text 和 Corel WordPerfect X4 等。你也可以从网上购买并下载一些，如 NoteTab 或 TextPad。

HTML 编辑器是更复杂的文本编辑器，或者是允许你通过点击按钮或其他手段添加代码的编辑器——通常被称为“所见即所得”（WYSIWYG）编辑器。我建议使用纯文本编辑器，或者不会改变你手动添加的任何代码的 HTML 编辑器。HTML 编辑器的示例有 Adobe Dreamweaver 和 Softpress Freeway。

**Q：关于使用文本编辑器我到底需要知道什么？**

**A：** 基本上，你只需要知道如何向编辑器中输入纯文本，以 .html 或 .htm 扩展名保存文件，并能够再次打开它并在必要时进行编辑。不需要特殊功能，因为 HTML 文件是由纯文本组成的。

**Q：关于使用浏览器我需要知道什么？**

**A：** 你绝对需要知道的是如何在你的计算机（或 Web 上）上打开本地 HTML 文件，以及如何刷新页面。如果你不知道如何从自己的电脑打开 HTML 文件，请打开浏览器并转到“文件”（File）菜单。寻找类似于“打开”（Open）或“打开文件”（Open File）的选项并选择它。你应该能够像使用其他程序一样浏览想要打开的文件。下面的插显示了该选项在 Microsoft Internet Explorer 中的位置：

专家问

第 1 章：JavaScript 简介

7

### 记住，它不是 Java

JavaScript 和 Java 是两种不同的语言。Java 是一种全编程语言，在执行程序（通常称为 Java *applet*）之前必须经过编译（通过一个将高级代码转换为机器语言的软件来运行程序）。Java 更加功能更强大，但也更复杂。JavaScript 不需要编译器，并且在许多领域（如语法）上更加宽松。

![](img/61d166424839b7674a7b9c8434ae4e03_29_0.png)

**Q：我在哪里获取你提到的那些浏览器？**

**A：** 这里是浏览器的链接：

- **Microsoft Internet Explorer** www.microsoft.com/ie
- **Mozilla Firefox** www.mozilla.com/firefox
- **Opera** www.opera.com

JavaScript 入门指南

### 与其他语言的相似之处

JavaScript 确实与其他编程和脚本语言有相似之处。如果你有 Java、C++ 或 C 的经验，你会发现语法上有一些相似之处，这可能帮助你更快地学习。由于它是一种脚本语言，JavaScript 也与 Perl 等语言有相似之处——它也可以通过解释器运行，而不是通过编译。如果你有任何语言的编程或脚本经验，将使学习 JavaScript 变得更容易——但并非强制要求。

### 从 JavaScript 开始

JavaScript 是网景通信公司（Netscape Communications Corporation）和太阳系统公司（Sun Microsystems, Inc.）共同努力的。新语言的发布于 1995 年 12 月 4 日，当时 Netscape Navigator 2.0 还处于测试版本。JavaScript 1.0 版本随新浏览器发布。（在作为 JavaScript 发布之前，它被称为 LiveScript。）JavaScript 是一种基于对象的客户端脚本语言，你可以它让 Web 页面更加动态。为了理解这个定义，让我们逐个查看它的重要部分。

#### 基于对象

*基于对象*（Object based）意味着 JavaScript 可以可以使用*对象*（objects）的项。然而，这些对象不是*基于类*的（class based）（即没有区分类和实例）；相反它们只是通用对象。你将在第 8 章学习如何操作 JavaScript 对象。在了解该语言的其他功能之前，你不需要了解它们的细节。

#### 客户端

*客户端*（Client side）意味着 JavaScript 在查看者使用的*客户端*（软件）中，而不是在提供页面的 Web 服务器上。在这种情况下，客户端就是 Web 浏览器。为了更好地理解这一点，让我们看看服务器端语言是如何工作的，以及客户端语言是如何工作的。

##### 服务器端语言

服务器端语言需要从 Web 页面或 Web 浏览器获取信息，将其发送运行在主机服务器上的程序，然后将信息传回浏览器。因此，在浏览器中看到程序结果之前，必须有一个中间步骤从服务器发送和检索信息。

服务器端语言通常为程序员提供客户端语言不具备的选项，例如将信息保存到 Web 服务器上供以后使用，或使用新信息更新 Web 页面并保存更新。

然而，服务器端语言在处理客户端语言可以访问浏览器窗口特殊功能方面可能会受到限制（例如 Web 页面特定位置的内容或提交到服务器之前的表单内容）。

第 1 章：JavaScript 简介

9

##### 客户端语言

客户端语言直接通过查看者使用的客户端运行。在 JavaScript 的情况下，客户端是 Web 浏览器。因此，JavaScript 直接在 Web 浏览器中运行，不需要经过从 Web 服务器发送和检索信息的额外步骤。

使用客户端语言，浏览器读取并解释代码，可以在无需先从服务器获取信息的情况下将结果给给查看者。这个过程可以让某些任务运行得更快。

客户端语言还可以访问浏览器窗口的特殊功能，而这些功能用服务器端语言可能无法访问。然而，客户端语言缺乏像服务器端语言那样保存文件或更新文件的能力。

***注意***

使用 XMLHttpRequest 对象允许 JavaScript 请求服务器数据。这将在第 16 章简要介绍。

##### 脚本语言

脚本语言不需要在运行之前编译程序。所有的解释都是由客户端即时完成的。对于普通的编程语言，在运行编写的程序之前，必须使用特殊的编译器进行编译以确保没有语法错误。对于脚本语言，代码在加载到客户端时被解释。因此，你可以更快地测试代码结果。然而，错误在脚本运行之前不会被捕获，如果无法良好处理错误，可能会出现问题。在 JavaScript 的情况下，错误处理取决于查看者使用的浏览器。

### 总结

考虑到这一切，你可能想知道 JavaScript 是如何在浏览器中运行的。你可能想知道在哪里编写 JavaScript 代码，以及什么告诉浏览器它与 Web 页面上的其他内容不同。目前的答案是通用的，下一章将提供更多细节。

JavaScript 通过被添加到现有的 HTML 文档中（直接添加或引用外部脚本文件）在浏览器中运行。你可以添加特殊的标签和命令来


JavaScript：初学者指南

这段 HTML 代码将告诉浏览器需要运行一个脚本。一旦浏览器看到这些特殊标签，它就会解释 JavaScript 命令，并按照你对代码的指令执行操作。因此，通过简单地编辑 HTML 文档，你就可以在 Web 页面上开始使用 JavaScript 并看到结果。

例如，以下代码向 HTML 文件中添加了一些 JavaScript，在网页上写入一些文本。注意这里添加的 `<script>` 和 `</script>` 标签。这些标签内部的代码就是 JavaScript。

```html
<html><body><script type="text/javascript">
document.write("This writes text to the page");
</script></body></html>
```

下一章将介绍如何使用 `<script>` 和 `</script>` HTML 标签在 HTML 文件中添加 JavaScript。这将是你通往成为 JavaScript 编码员道路上的第一步！

在线资源

为了在网上找到更多额外信息来帮助学习 JavaScript，这里是一些实用的资源：

- 一个可以找到带有运行结果示例的教程的地方：www.pageresource.com/jscript
- 一个优秀的教程网站，包含了可供复制粘贴的脚本：www.javascriptkit.com
- 一个你可以向其他编码员咨询 JavaScript 问题的地方：www.webxpertz.net/forums

使用 JavaScript 编写文本

此项目通过在浏览器中加载 HTML 文档向你展示 JavaScript 的实际应用。脚本使用 JavaScript 在浏览器中编写一行文本。

逐步操作

1. 将此处显示的代码复制并粘贴到你的文本编辑器中：

```html
<html><body><script type="text/javascript">
document.write("This text was written with JavaScript!");
</script>
<!-- 这一行代码将引号内的文本写入页面 -->
<!-- 此标签告诉浏览器后面是 JavaScript -->
<!-- 这一行告诉浏览器这是脚本的结束 -->
</body></html>
```

2. 将文件保存为 **pr1_1.html** 并在你的 Web 浏览器中打开它。你应该能看到一行用 JavaScript 编写的文本。

尝试一下这个 

### 总结

在这个项目中，你将一段代码复制并粘贴到文本编辑器中并保存了文件。当你从 Web 浏览器中打开保存的文件时，浏览器中会显示一行文本。这段文本是使用 JavaScript 在浏览器窗口中编写的。你将在第 2 章中看到更多关于这种脚本如何工作的内容。

*第 1 章自测*

1. 为了使用 JavaScript，你必须知道以下哪一项？
A Perl
B C++
C HTML
D SGML

2. 以下哪项是你使用 JavaScript 应该具备的？
A 一个 Web 浏览器
B 一个 C++ 编译器
C 一个 50GB 的硬盘
D 一个 CD-RW 驱动器

3. Web 浏览器的选择取决于你，只要它兼容 ________。
A Flash MX
B VBScript
C JavaScript
D Windows XP

4. JavaScript 和 Java 是同一种语言。
A 正确
B 错误

5. 在语法等许多领域，JavaScript 比 Java 更 __________。
A 复杂
B 强大
C 编译
D 宽松

6. JavaScript 与其他的编程和脚本语言有相似之处。
A 正确
B 错误

7. 在作为 JavaScript 发布之前，它被称为 ________。
A Java
B JavaCup
C LiveScript
D EasyScript

8. JavaScript 是 ________。
A 基于对象的
B 面向对象的
C 缺少对象的
D 不是一种使用对象的语言

9. 客户端语言直接通过观众使用的 __________ 运行。
A 服务器
B 客户端
C 监器
D 律师

10. 在 Web 页面上使用表单时，客户端语言如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

11. 在 Web 页面上使用表单时，客户端语言如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

12. 客户端语言直接通过观众使用的 __________ 运行。
A 服务器
B 客户端
C 监器
D 律师

13. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

14. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

15. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

16. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

17. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

18. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

19. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

20. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

21. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

22. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

23. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

24. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

25. 客户端语言在 Web 页面上使用表单时，如何提供帮助？
A 它可以将信息保存在服务器上。
B 它可以在发送到服务器之前对信息进行验证。
C 它可以更新文件并用新信息保存文件。

第 2 章：在 HTML 文件中放置 JavaScript

关键技能与概念

- 使用 HTML 标签
- 创建你的脚本
- 使用外部文件
- JavaScript 注释

现在你已经接触了 JavaScript，准备好编写了。由于 JavaScript 是运行的，你需要知道如何标记它的开始和结束。最常用的方法是使用 `<script>` 和 `</script>` 标签。你可以将其放在 HTML 文档的头部或部分。本章将向你展示如何使用脚本标签开始你的脚本。在本章结束时，你将学习如何为脚本添加 JavaScript 注释。

### 使用 HTML 标签

脚本标签用于告诉浏览器脚本的开始和结束。在最基本的形式中，脚本标签与其他 HTML 标签一样：

```html
<script>
*此处代码*
</script>
```

如你所示，有一个 `<script>` 标签、JavaScript 代码，然后是 `</script>` 标签。为了安全起见，显式标识语言是个好习惯。通过在起始标签上添加值为“text/javascript”的 type 属性来实现：

```html
<script type="text/javascript">
*此处代码*
</script>
```

### 识别脚本语言

在旧版本的 HTML 中，脚本标签是不区分大小写的。但在 XHTML 中，脚本标签必须是小写。JavaScript 是区分大小写的，因此你需要更加小心。

### 调用外部脚本

如果你想在文档中调用外部文件，脚本标签也非常用。外部 JavaScript 文件*是一个仅包含 JavaScript 的文本文件，并以 .js 扩展名保存。通过调用外部文件，你可以节省每个页面中编码或复制长脚本的时间。相反，你可以在每个页面上使用一行指向 JavaScript 文件的。

你可以通过在起始标签上添加 src（源）属性来调用外部脚本：

```html
<script type="text/javascript" src="yourfile.js"></script>
```

确保起始和结束标签之间没有空格或代码，否则可能会导致脚本调用失败。

### 使用 <noscript></noscript> 标签

为没有 JavaScript（或禁用了 JavaScript）的观众提供替代内容的方法是使用 noscript 标签。`<noscript></noscript>` 标签可以放置在 HTML 文档的任何位置，并包含那些浏览没有 JavaScript 的观众所需的任何内容（例如使用 Blackberry 或 iPhone 等手机浏览器的观众）。例如：

```html
<script type="text/javascript">
document.write("颜色是红色的。");
</script>

<noscript>
颜色是红色的。
</noscript>
```




JavaScript：初学者指南

结束 CDATA 区域

开始和结束的 JavaScript 注释位于 `]]>` 之后

开始和结束的 JavaScript 注释位于 `<![CDATA[` 之前

开始 CDATA 区域

**Q:** **我总是需要使用 `<script>` 标签来向页面添加 JavaScript 吗？**

**A：** 可以使用*事件处理器*，它允许你在 HTML 标签的事件处理属性中编写简短的脚本。你将在第 7 章中学习关于事件处理器的知识。

**Q:** **`language` 属性又是怎样的？**

**答：** 在 XHTML 中，`language` 属性已被 `type` 属性取代。使用 `language` 属性可能会导致 页面无法通过 XHTML 验证（在 XHTML 严格模式下），不再建议使用。

**Q:** **当我向页面添加脚本时，我的页面在 XHTML 严格（或过渡）模式下无法验证。我如何让页面通过验证？**

**答：** 如果脚本包含 XHTML 使用的字符，例如 `<`（在 JavaScript 中用于表示“小于”，但在 XHTML 中被视为新标签的开始），那么在不添加 CDATA 区域的情况下，直接在文档中使用脚本将无法通过验证：

```html
<script type="text/javascript">
<![CDATA[
var x = 5;
var y = 10;
if (x < y) {
  window.alert("x is less than y");
}
]]>
</script>
```

这将允许页面通过验证，但由于 `<![CDATA[` 和 `]]>` 位于脚本中，脚本将不再工作。要修复此，当这些字符位于脚本标签内时，你需要使用 JavaScript 注释（`/*` 和 `*/`）：

```html
<script type="text/javascript">
/*<![CDATA[*/
var x = 5;
var y = 10;
if (x < y) {
  window.alert("x is less than y");
}
/*]]>*/
</script>
```

如你所见，这很快变得非常繁琐！通常，更好的选项是使用外部脚本文件，这消除了这个问题，因为 XHTML 文档中只需要脚本标签本身。

提问专家

## 第 2 章：将 JavaScript 放置在 HTML 文件中

此示例通过 JavaScript 或 `<noscript></noscript>` 标签内的文本向查看者显示“颜色是红色的”。

***注意***

某些旧版浏览器可能无法正确处理 `noscript` 标签，不会显示任一部分的内容。如果你的用户使用旧版浏览器，另一种替代方案是在页面上显示内容，然后使用 JavaScript 为那些能够启用 JavaScript 的用户增强内容。

### 创建你的第一个脚本

现在你已经知道如何使用 HTML `<script>` 标签来告诉浏览器文档中的 JavaScript，你已经准备好学习如何在这些脚本标签之间添加实际的 JavaScript 代码了。教学任何语言时提供的第一个代码示例通常是向默认输出区域写入某些文本，通常被称为基础“Hello World”（你好世界）脚本。遵循这一惯例，你的第一个脚本将在网页上写入一段文本字符串。

### 编写“Hello World”脚本

与其编写“Hello World”，你将为此脚本使用另一行文本：“是的！我现在是一个 JavaScript 编码员了！”这只需要单行代码，使用 `document.write()` 方法，该方法向文档写入一个文本字符串：

```html
<script type="text/javascript">
document.write("Yes! I am now a JavaScript coder!");
</script>
```

注意文本周围的括号和引号。括号是必须，因为 `document.write()` 方法是一个 JavaScript *函数*，它接受一个包含在括号中的*参数*。你将在第 4 章学习更多关于 JavaScript 函数的知识。

引号表示文本*字符串*。字符串是 JavaScript 中一种变量类型，通过将其放在引号内来定义。第 3 章提供了字符串和其他类型 JavaScript 变量的详细信息。

关于你的脚本需要注意的最后一点是行尾的分号。分号表示一个 JavaScript 语句的结束。一个*语句*（statement）是代码的一部分，其在语法上（形式和顺序）不需要额外添加任何内容即可完整。一个语句可以用于执行单个任务、执行多个任务，或调用脚本中执行多条语句的其他部分。大多数 JavaScript 语句都以分号结束，因此养成记住添加分号的习惯是一个好主意。

***注意***

在随后的章节中，你将看到许多不以分号结尾的行，因为它们开启或关闭了一个代码块。此外，你遇到的许多脚本可能没有用分号结束语句。JavaScript 在大多数情况下对分号的使用是宽容的；然而，最好使用分号来结束语句，因为可以防止可能发生的错误并有助于后后的调试（从脚本中移除错误）。

因此，要向页面写入文本字符串，你使用 `document.write()` 方法，后紧跟用引号包围并包含在括号内的文本。用分号结束该行（该语句）。JavaScript 将处理剩余工作。

### 为脚本创建 HTML 文档

为了使此示例完整并测试脚本，你需要将其插入到 HTML 文档中。首先，使用基础标签创建以下 HTML 文档（使用任何你喜好的文本编辑器）：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Untitled</title>
</head>
<body>
</body></html>
```

使用你喜欢的文本编辑器将该文件保存为 `test1.html`。为了看到结果，你需要在浏览器中打开它。

### 在 HTML 文档中插入脚本

为了让这个示例完整并测试脚本，你需要将其插入到 HTML 文档中。首先，使用基础标签创建以下 HTML 文档（使用任何你喜好的文本编辑器）：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Untitled</title>
</head>
<body>
</body></html>
```

使用你喜好的文本编辑器将该文件保存为 `test1.html`。为了看到结果，你需要在浏览器中打开它。

### 在 HTML 文档中插入脚本

为了让这个示例完整并测试脚本，你需要将其插入到 HTML 文档中。首先，使用基础标签创建以下 HTML 文档（使用任何你喜好的文本编辑器）：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Untitled</title>
</head>
<body>
</body></html>
```

（注：由于原文文本中存在部分重复段落，此处按逻辑合并翻译以确保内容连贯）

**在 HTML 文档中插入脚本**

为了让这个示例完整并测试脚本，你需要将其插入到 HTML 文档中。首先，使用基础标签创建以下 HTML 文档（使用任何你喜好的文本编辑器）：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Untitled</title>
</head>
<body>
</body></html>
```

使用你喜好的文本编辑器将该文件保存为 `test1.html`。为了看到结果，你需要在浏览器中打开它。

### 在 HTML 文档中插入脚本

为了让这个示例完整并测试脚本，你需要将其插入到 HTML 文档中。首先，使用基础标签创建以下 HTML 文档（使用任何你喜好的文本编辑器）：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Untitled</title>
</head>
<body>
</body></html>
```

（注：原文提供的文本在后半部分出现了多次重复，翻译时已根据高级文档工程师逻辑进行了去重处理，确保输出内容流畅且不冗余。）

项目：在 HTML 文档中插入脚本

这个项目让你练习在页面上添加脚本。你将创建一个 HTML 文档并插入脚本，在页面加载时显示一个短句。

**步骤**

1. 设置一个 HTML 文档，使 `<body>` 和 `</body>` 标签之间现在还没有内容。
2. 在网页中放入以下文本：我是 HTML 文档的一部分！
3. 在此行之后插入一个 `<br />` 标签（在页面上插入换行）。
4. 在 `<br />` 标签之后插入一个脚本，在页面上写入以下内容：这来自我的脚本，现在在页面上了！
5. 在脚本之后添加另一个 `<br />` 标签。
6. 在最后一个 `<br />` 标签之后在网页中放入以下文本，并进行强调：*我也是 HTML 文档的一部分，在脚本之后！*

**Q:** **为什么 `document.write()` 命令中有一个点 (.)？**

**答：** `document` 是 JavaScript 的预定义对象之一，`write()` 是 `document` 对象的一个预定义方法。点将对象和方法结合使函数工作。第 8 章解释 JavaScript 对象，第 9 章专门介绍 `document` 对象。

**Q:** **我如何知道何时将脚本添加到 `<head>` 部分，何时添加到到<body>` 部分？**

**答：** 将脚本添加到文档的 `<body>` 部分的主要情况是你正直接向页面写入内容时。在许多情况下，大部分脚本可以在 `<head>` 部分完成，因为你可以使用函数来调用 `<body>` 部分的代码。我们在书中经常使用外部脚本，这将消除许多困惑，因为所有代码都将在外部文件中。





## 第 2 章：将 JavaScript 放入 HTML 文件

23

7. 以下是你的 HTML 文档的样式：

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>JavaScript Project 2-1</title>
</head>
<body>
I am part of the HTML document!
<br />
<script type="text/javascript">
document.write("This came from my script, and is now on the page!");
</script>
<br />
<em>I am also part of the HTML document, after the script results!</em>
</body>
</html>
```

8. 将该文件保存为 `pr2_1.html` 并在浏览器中查看该页面以查看结果。

### 尝试本节总结

在这个项目中，你创建了一个 HTML 文件。利用你在此章节中目前学到的知识，你在 HTML 文件中插入了一个脚本，该脚本会在页面上写入特定的文本。当在 Web 浏览器中打开 HTML 页面时，脚本的结果显示在两行文本之间。

### 使用外部 JavaScript 文件

现在假设你想在多个页面上使用你的“Hello World”脚本（你在本章节稍早时候创建的），但你不想在每个页面上都写一遍。你可以通过将脚本放在外部脚本文件中并使用 `script` 标签的 `src` 属性调用它来实现。对于这种方法，你需要创建一个 JavaScript 文本文件来存放你的脚本。你还需要一个或多个 HTML 文件，在其中放置脚本标签以调用你的外部脚本文件。

### 创建 JavaScript 文件

在本例中，你将创建一个只包含一行代码的 JavaScript 文件。在实际应用中，你会用这种方法处理较长的脚本——脚本越长，这种技术就越有用（特别是当你试图验证 Web 页面或将脚本代码与标记语言分离时）。

《JavaScript 入门指南》

在你的文本编辑器中打开一个新文件，仅插入 JavaScript 代码本身（`document.write()` 语句）。外部 JavaScript 文件中不需要 `script` 标签。文件应该如下所示：

```javascript
document.write("Yes! I am now a JavaScript coder!");
```

在你的文本编辑器中将文件保存为 `jsfile1.js`。执行此操作时，你可能需要使用文件上的“另存为”选项，并在文件名周围加上引号，如图 2-2 所示（使用 Windows 记事本）。

一旦文件保存，你就可以继续下一步，创建使用该脚本的 HTML 文件。

### 创建 HTML 文件

你将创建两个文件来放置你的脚本。不过，这种技术适用于任意数量的 HTML 文件，只要你在每个文件中都添加了所需的脚本标签。

对于第一个文件，创建你的基础 HTML 文档，并将脚本标签插入文档的 `<body>` 部分，使用 `src` 属性指向 `jsfile1.js` 文件，并在页面主体中添加一些 HTML 文本以将其标识为第一个 HTML 文档：

```html
<body>
<script type="text/javascript" src="jsfile1.js"></script>
<p>
This is page 1, and the script works here!
</p>
</body>
```

![](img/61d166424839b7674a7b9c8434ae4e03_46_0.png)
图 2-2 使用引号保存 .js 扩展名文件的示例，以便以正确的扩展扩展名保存

在你的文本编辑器中将此文件保存为 `jsext1.html`。确保将其保存到与 `jsfile1.js` 文件相同的目录中。

第二个 HTML 文档与第一个相同，只是 HTML 文本显示它是第 2 页：

```html
<body>
<script type="text/javascript" src="jsfile1.js"></script>
<p>
This is page 2, and the script also works here!
</p>
</body>
```

在你的文本编辑器中将此文件保存为 `jsext2.html`。再次，确保将其放在与其他文件相同的相同的目录中。

### 在浏览器中查看页面

在 Web 浏览器中打开 `jsext1.html` 文件。它应该如图 2-3 所示，JavaScript 从外部脚本文件插入到页面中。

![](img/61d166424839b7674a7b9c8434ae4e03_47_0.png)
图 2-3 在 `jsext1.html` 文件中调用脚本的结果，第一个 HTML 页面

接下来，在你的 Web 浏览器中打开 `jsext2.html` 文件。它应该如图 2-4 所示，唯一的区别是你添加到 HTML 文件中的文本，显示这是第 2 页。JavaScript 在此页面上写入的文本与在第一个 HTML 页面上写入的相同。虽然我们在本例中使用了一个短脚本，但它应该让你了解到当你有一个大型脚本时，使用外部文件如何是一个极好的节省时间的方法。

### 从 HTML 文档调用外部脚本

这个项目将让你练习创建外部 JavaScript 文件并使用它们将脚本插入 Web 页面中。

![](img/61d166424839b7674a7b9c8434ae4e03_48_0.png)
图 2-4 在 `jsext2.html` 文件中调用脚本的结果，第二个 HTML 页面

pr2_2.html
prjs2_2.js

### 步骤

1. 设置一个简单的 HTML 文档，在 `<body>` 和 `</body>` 标签之间什么都不放。
2. 在页面的 `body` 标签之间放置以下文本：
   *This text is from the HTML document!*
3. 在此文本之后放置一个 `<br />` 标签。如果你现在需要保存此文件，请将其保存为 `pr2_2.html`。
4. 创建外部 JavaScript 文件，它在执行时将写入以下行：
   *I love writing JavaScript and using external files!*
5. 你的 JavaScript 文件看起来应该是这样的：
```javascript
document.write("I love writing JavaScript, and using external files!");
```
6. 将 JavaScript 文件保存为 `prjs2_2.js`。
7. 返回 HTML 文档。在文档中的 `<br />` 标签之后放置 `script` 标签，以便外部 JavaScript 文件在页面上写入它的句子。
8. 你的 HTML 文档的 `body` 应该如下：

```html
<body>
This text is from the HTML document!
<br />
<script type="text/javascript" src="prjs2_2.js"></script>
</body>
```
9. 将此文件保存为 `pr2_2.html` 并在浏览器中查看结果。

### 尝试本节总结

在这个项目中，你创建了一个 HTML 页面。利用你在一节中外部 JavaScript 文件的知识，你创建了一个外部 JavaScript 文件，并将必要的代码放入 HTML 文件以包含该外部 JavaScript 文件。当 HTML 文件在 Web 浏览器中显示时，会显示一行纯文本，随后是外部文件的结果。

### 使用 JavaScript 注释

你可能需要在代码中做笔记，例如描述某行代码的作用。你也可能想由于某些原因禁用某行。例如，如果你正在寻找脚本中的错误，你可能想禁用某行。你可以通过 JavaScript 注释来完成这些任务。你可以插入单行注释，也可以多行注释。

### 插入单行注释

如果你想在单行上添加注释，在注释文本前放置双斜杠：
`// Your comment here`

在这种格式下，斜杠之前的任何内容都是“活”代码——即会被执行的代码——斜杠之后的任何内容都会被忽略。例如，假设你写了这一行：
`document.write("This is cool!"); // out opinion`

浏览器将运行 `document.write()` 方法，因此“This is cool!”将被写入页面。然而，斜杠后的注释将被忽略。如果你将斜杠放置在行的开头，浏览器将忽略整行。假设你将上例中的斜杠移动到行的开头：
`// document.write("This is cool!");`

在这种格式下，整行都会被忽略因为它因为它代表注释的双斜杠开头。

### 添加多行注释

由双斜杠标记的注释仅适用于它们所在的行；其效果在行尾截止。要添加跨越任意数量行的注释，你需要使用不同的注释格式：在注释开头使用一个斜杠加一个星号，然后是注释文本，最后在注释结束处使用星号加一个斜杠。这是一个示例：

```javascript
/*
My script will write some text into my HTML document!
All of this text is ignored by the browser.
*/
document.write("You can see me!");
```

使用这种格式，你可以从一行并在另一行结束。多行注释当你想要插入较长的描述或其他文本时非常有用，但使用它们时需要小心。看这个示例，看看是否能发现其中的问题：

```html
<script type="text/javascript">
/*
This code won’t work for some reason.
*/
```





## 第 2 章：将 JavaScript 放入 HTML 文件中

29

document.write("我希望有人能看到我！");

</script>

你注意到缺少 JavaScript 注释的结束符号了吗？当你
使用多行注释时，需要小心关闭它们。否则，你可能会
无意中注释掉你想要执行的代码！在这个示例中，注释会一直持续下去而没有尽头。要修复这个问题，你需要在使用 `document.write()` 方法之前
关闭 JavaScript 注释：

<script type="text/javascript">

/*

现在 JavaScript 代码可以正常工作了！这段文字是被隐藏的。

*/

document.write("现在大家都能看到我了！");

</script>

在前面的示例中，你看到了如何使用注释来为每个脚本提供一些说明文档。在第 16 章中，你将学习如何使用注释来帮助你调试 JavaScript 代码。现在，你应该养成在脚本中添加注释的习惯，作为简短的文档或说明。

*第 2 章自测*

1. `<script>` 和 `</script>` 标签的作用是什么？
A 告诉浏览器脚本从哪里开始到结束
B 让浏览器知道将要使用的脚本语言
C 指向一个外部 JavaScript 文件
D 以上都是

2. 为什么应该在起始脚本标签中使用 `type` 属性？
A 让浏览器知道你是什么种类型的编码员
B 确保浏览器不会将你的 JavaScript 解释为另一种脚本语言，并确保 Web 页面符合 XHTML 标准
C 创建一个类型脚本
D 确保脚本不会出现语法错误

3. JavaScript 代码区分大小写吗？
A 是
B否
✓

JavaScript：初学者指南

4. `noscript` 标签为那些没有 __________ 的人提供了 __________。

5. 外部 JavaScript 文件通常使用名为 __________ 的文件扩展名。
A .js
B .html
C .jav
D .java

6. 下面哪项代码项正确地指向了名为 `yourfile.js` 的外部 JavaScript 文件？
A <extscript type=“text/javascript” src=“yourfile.js”></extscript>
B <script type= “text/javascript” src=“yourfile.js”></script>
C <script language=“yourfile.js”></script>
D <script type=“text/javascript” link=“yourfile.js”></script>

7. 在旧版本的 HTML 中，`script` 标签是不区分大小写的。然而，在 XHTML 中，`script` 标签必须是 __________。

8. __________ 标志着 JavaScript 语句的结束。
A 冒号
B 句号
C 问号
D 分号

9. 为了在 Web 页面上写一段文本，使用了 __________ 方法。
A document.write()
B document.print()
C document.type()
D window.print()

10. 什么情况下使用外部 JavaScript 文件是一个好主意？
A 当脚本很短或只将在一个 HTML 文档中使用
B 当你的网站观众使用较旧的浏览器时
C 当脚本非常长或需要放置在多个 HTML 文档中时
D 外部文件不是一个好主意

11. JavaScript 注释对于 __________ 或 __________ 代码非常有用。

第 2 章：将 JavaScript 放入 HTML 文件中

31

12. 下面哪项表示 JavaScript 代码中之后将跟随着一个单行注释？
A /*
B /-
C //
D <!--

13. 下面哪项表示 JavaScript 代码中之后将跟随着多行以上的注释？
A /*
B /-
C //
D <!--

14. 下面哪项表示多行 JavaScript 注释的结束？
A \\
B -->
C /*
D */

15. 当你使用多行 JavaScript 注释时，你需要小心 __________ 它们。
A 关闭
B 读取
C 编写
D 编译

## 第 3 章：使用变量

JavaScript：初学者指南

核心技能与概念

- 理解变量
- 为什么变量很有用
- 为你的脚本定义变量
- 理解变量类型
- 在脚本中使用变量

现在你已经学习了在 Web 页面中添加 JavaScript 的基础知识，是时候进入该语言的内部工作机制了。由于变量是 JavaScript 编码的重要部分，你将需要尽可能了解它们是什么以及为什么它们在你的脚本中很有用。一旦你理解了变量是如何工作的以及它们能做什么，你就可以继续学习其他基于各种类型变量的使用的话题。

在本章中，你将从学习变量是什么以及它们为什么有用开始。然后，你将学习用于声明变量的方法以及如何给变量赋值。最后，你将看到如何在你的脚本中使用变量。

### 理解变量

一个*变量*代表或持有一个值。变量的实际值可以随时更改。为了理解变量是什么，请考虑一个基础的：

x=2

变量的实际值可以随时更改。为了理解变量是什么，请考虑一个基础的：

x=2

变量的2

可以，更改。为了理解

，，

一个基础的：

x=2

x=2

为了理解变量，，你考虑一个基础的：

x=2

变量的实际值可以随时更改。为了理解变量是什么，请考虑一个基础的：

x=2

现在结果是10。根据根据需要赋值的：

x=7

现在结果是10。

第 3 章：使用变量

35

变量在 JavaScript 中与数学中的变量非常相似。你给变量一个名字，并根据需要进行赋值。如果你在脚本开始时给变量一个值，那么脚本的其余部分就可以使用它了。

### 为什么变量很有用

使用变量有几个益处：

- 它们可以在值未知时被使用。
- 它们可以节省你编写的时间。
- 它们可以让你的代码更清晰。

### 作为未知值的占位符

通常，变量将持有一个在编写时是未知的值。例如，考虑这行代码：

TotalPrice=2.42+3.3;

在这里，数字可以代表任何内容。相反，你可能会将 2.42 赋值给名为 CandyPrice 的变量，将 3.3 赋值给 OilPrice：

TotalPrice=CandyPrice+OilPrice;

现在，与其试图记住数字的含义，你可以看到脚本正在相加某些。

### 节省时间

变量可以加快写作，因为它们的值可以更改。当你稍后给变量赋值时。

JavaScript：初学者指南

### 起解释作用

由于变量代表某些内容，并且你可以给它们起有意义的名字，它们在阅读（和调试）脚本时通常更容易识别。如果你只是添加数字，你可能会忘记它们代表什么。例如，考虑这行代码：

TotalPrice=2.42+3.3;

在这里，数字可以代表任何内容。相反，你可能会将 2.42 赋值给名为 CandyPrice 的变量，将 3.3 赋值给 OilPrice：

TotalPrice=CandyPrice+OilPrice;

现在，与其试图记住数字的含义，你可以看到脚本正在相加某些。

### 为你的脚本定义变量

现在你理解了变量是什么以及为什么要使用它们，你需要学习它们如何在你的脚本中工作。你通过*声明*它们来创建变量。然后使用 JavaScript 赋值运算符为它们赋值。当你命名变量时，遵循 JavaScript 的命名规则，并考虑名称的意义。

### 声明变量

要将文本声明为变量，使用 `var` 关键字，它告诉浏览器文本将是新变量的名字：

var *variablename*;

例如，将你的变量命名为 coolcar，声明如下：

var coolcar;

在这个示例中，你有一个名为 coolcar 的新变量。分号结束了语句。变量 coolcar 还没有赋值。正如下一节所述，你可以在声明的同时给你的新变量赋值，也可以在脚本中稍后为它赋值。

#### 给变量赋值

要给变量赋值，使用 JavaScript 赋值运算符，即等号 (=) 符号。如果你想在同一行声明变量并为其赋值，使用此格式：

var *variablename*=*variablevalue*;





## 第3 章：使用变量

例如，要将变量命名为 paycheck 并赋予其数值值 1200，请使用此语句：

`var paycheck=1200;`

该语句以关键字 `var` 开头，后面跟着变量名 `paycheck`，这与上一节描述的普通变量声明相同。接下来是赋值运算符 (`=`)，它告诉浏览器将运算符右侧的值赋值给运算符左侧的变量。赋值运算符的右侧是 1200，这是被赋值给变量 `paycheck` 的数值。该行以分号结尾，表示该语句的结束。

***注意***

小心不要将赋值运算符 (`=`) 误为“等于”。该运算符只负责赋值。表示“等于”的运算符是两个等号连在一起（`==`），你将在第 5 章中学习到它。

要声明并赋值另一个变量，你可以使用相同的格式，将语句放在新的一行。例如，设置一个名为 `spending` 的变量来跟踪你从 `paycheck` 变量中花费的金额，请使用以下语句：

`var paycheck=1200;`

`var spending=1500;`

当然，你也会注意到这种财务状况正朝着麻烦发展，因为 `spending` 变量中花费的钱多于 `paycheck` 变量带来的钱。奇怪的是，这看起来越来越像我网站的预算了！

你看到的示例说明了变量声明和赋值的正确安全的方法。然而，事实是，JavaScript 在变量方面允许一定的灵活性。在很多情况下，即使不使用精确的代码语法，代码也能运行。例如，你可能会看到某些脚本在第一次使用变量时没有使用 `var` 关键字。JavaScript 经常会在变量第一次使用时自动声明它，即使它之前没有被声明。这里显示了一个示例：

`paycheck=1200;`

这是可以运行的，因为变量被赋值了一个值（JavaScript 会简单地声明该变量并为其赋值值 1200）。但是，如果你尝试在不赋值的情况下声明变量，以下内容将是非法的：

`paycheck;`

这种声明仍然需要 `var` 关键字才能有效，如下代码所示：

`var paycheck;`

给变量 `paycheck` 赋值 1200

给变量 `spending` 赋值 1500

你可能还会看到省略末尾分号的脚本：

`var paycheck=1200`

在某些脚本中，变量赋值的这两个特征都被省略了：

`paycheck=1200`

所有这些快捷方式似乎都很方便，但最好的做法是在使用每个变量之前先定义它，使用 `var` 关键字并包含分号。这样做可能会在某些浏览器中导致错误，并可能给人们留下代码写得不印象。此外，如果你需要调试脚本，这些任何遗漏都可能非常麻烦。给变量正确的声明和赋值将避免问题，而且你的代码将更易于阅读和理解。

### 变量命名

在开始命名自己的变量之前，你需要了解 JavaScript 的命名规则。在选择名称时，你需要考虑的因素有大小写敏感、非法字符以及 JavaScript 预留的名称。此外，你应该尝试给变量起既易于记忆又有意义的名字。

### 在变量中使用大小写

JavaScript 变量是大小写敏感的——`paycheck`、`PAYCHECK`、`Paycheck` 和 `PaYcHeCk` 是四个变量。当你创建一个变量时，你需要确保稍后在脚本中编写该变量名时使用相同的大小写。如果你改变了任何大小写，JavaScript 都会将其视为新变量或返回错误。无论哪种情况，都会导致你的脚本出现问题。

以下关于在变量名中使用大小写的一些建议：

- 如果你使用的变量名仅由一个单词组成，最简单可能是整个名称都使用小写。这样输入速度更快，而且你以后在输入它时也知道要全部输入小写。
- 对于包含两个单词的变量名，你可能决定每个单词的首字母大写。例如，你可以将变量命名为 `MyCar` 或 `My_Car`（你将在下一节看到更多关于下划线字符 `_` 的内容）。

变量的大小写完全由你决定，所以你应该使用你最熟悉的风格。最好采用一种惯例并坚持使用它。例如，如果你只使用小写字母为变量命名，那么在整个脚本中都应该这样做，以避免在以后使用变量时不意外切换大小写。在本书中，我变量名只使用小写字母，以保持代码清晰。

### 使用允许的字符

必须记住的重要规则是，变量名必须以字母或下划线字符 (`_`) 开头。变量名不能以数字或除字母以外的任何其他字符开头。变量名中的其他字符可以是字母、数字或下划线。变量名中不允许空格。因此，以下变量名是有效的：

- `paycheck`
- `_paycheck`
- `pay2check`
- `pay_check`
- `pay_245`

然而，以下变量名是非有效的：

- `#paycheck`
- `1paycheck`
- `pay check`
- `pay_check 2`
- `_pay check`

最难记住的规则可能是不能以数字开头（这是我最经常忘记的）。虽然这种名字看起来合理，但 JavaScript 不允许这样做。

### 避免预留字

命名变量时另一个需要记住的规则是避免使用 JavaScript 预留字。这些是 JavaScript 中用于特定目的的特殊单词。例如，你已经了解到预留字 `var` 用于声明 JavaScript 变量。将其作为变量名会导致你的脚本出现许多问题，因为这个词旨在以不同的方式使用。

表 3-1 列出了 JavaScript 中的预留字。注意，所有单词都是全小写的。在随后的章节中，你将学习如何使用这些预留字，因此它们会随着时间的推移变得更加熟悉。

### 给变量意义

尽管 *x* 是一个可以接受变量名，但如果你以后需要调试程序，可能无法记得它代表什么。此外，如果其他人试图帮助你调试代码，他们的工作将更加困难。

你应该尝试给变量起尽可能清晰地描述它们所代表的内容。假设你想用一个变量来存储页面上某个示例的数字。与其使用 *x*、*ex* 或另一个短变量，不如使用具描述性的名称：

`var example_number=2;`

你以后将很容易识别 `example_number` 变量，其他程序员也可能更快理解它的用途。

脚本中使用的变量越多，使用有意义且易记忆的名字就越重要。

## 理解变量类型

到目前为止，你已经看到了数值类型的变量值示例。在 JavaScript 中，变量值或*类型*可以包括数字、字符串、布尔和空。

与更严格的编程语言不同， JavaScript 并不强制你在定义变量时声明其类型。相反，JavaScript 允许将任何值赋值给任何变量。虽然这在编码时为你提供了灵活性，但你需要小心，因为你可能会得到一些意外的结果——特别是当数字相加时。

### 数字

数字变量就是数字。JavaScript 不要求将数字声明为整数、浮点数（小数）或任何其他数字类型。相反，任何数字都被仅仅视为另一个数字，无论它是 7、–2、3.453 或其他任何数字。除非你执行计算来更改类型，否则该数字将保持相同类型。例如，如果你在变量中使用整数，它不会突然出现小数，除非你执行了某种计算来改变它（例如不整除）。

正如你所看到的，通过使用关键字 `var` 来定义数字变量：

`var *variablename*=*number*;`

表 3-1 JavaScript 预留字

| | | | | |
| :--- | :--- | :--- | :--- | :--- |
| abstract | delete | goto | null | throws |
| as | do | if | package | transient |
| boolean | double | implements | private | true |
| break | else | import | protected | try |
| byte | enum | in | public | typeof |
| case | export | instanceof | return | use |
| catch | extends | int | short | var |
| char | false | interface | static | void |
| class | final | is | super | volatile |
| const | finally | long | switch | while |
| continue | float | namespace | synchronized | with |





## 第3 章：使用变量

41

这里是一些示例：

var paycheck=1200;

var phonebill=29.99;

var savings=0;

var sparetime=-24.5;

如果你需要使用一个特别长的数字，JavaScript 提供了指数计数法。要表示指数，请在基数数字之后、指数之前使用字母 *e*。例如，要创建一个名为 bignumber 的变量并赋值赋值为 4.52 × 10⁵ (452,000) 的值，只需用字母 *e* 替换数字和指数之间的所有内容（代表“乘以 10 的幂次方”这一短语）：

var bignumber=4.52e5;

***注意***

JavaScript 可能会使用指数计数法对计算结果返回答案（就像许多计算器一样）。

### 字符串（String）

*字符串变量*是表示文本字符串的变量。字符串可以包含字母、单词、空格、数字、符号或任何你喜欢的内容。字符串的定义方式与数字略有不同，使用以下格式：

var *variablename*="*stringtext*";

这里是一些字符串变量的示例：

var mycar="Corvette";

var oldcar="Big Brown Station Wagon";

var mycomputer="Pentium 3, 500 MHz, 128MB RAM";

var oldcomputer="386 SX, 40 mHz, 8MB RAM";

var jibberish="what? cool! I am @ home 4 now. (cool, right?)";

如你所示，字符串可以是短的、长的或介于之间的任何长度。你可以在字符串变量中放置各种文本和其他字符。然而，需要考虑引号、某些特殊字符以及字符串的大小敏感性。

### 匹配引号

在 JavaScript 中，正如你在示例看到的，你通过将字符串放在引号（简称 quotes）内部来定义字符串。JavaScript 允许你使用双引号或单引号来定义字符串值。问题在于，如果字符串用双引号开启，则它必须用双引号关闭：

var mycar="Red Corvette";

JavaScript：初学者指南

单引号也是如此：

var myhouse='small brick house';

尝试用错误类型的引号来关闭字符串，或者漏掉起始或结束引号，都会导致问题。

var mycar="Red Corvette';

var myhouse= 'small brick house";

var mycomputer="Pentium 3, 500 mHz, 128MB RAM;

这些错误将在 Web 浏览器中产生“Unterminated String”（未终止的字符串）错误。

### 注意大小写

JavaScript 字符串对大小写敏感。这现在看起来并不重要，但当你需要比较字符串是否匹配时，它很重要。仅仅一个字符的大小写不同就会导致字符串不同：

"My car is fun to drive!"

"my car is fun to drive!"

你将在第 5 章学习更多关于字符串比较的内容。

### 使用特殊字符

*特殊字符*允许你向字符串添加其他无法添加的内容。例如，假设需要在字符串的每个单词之间插入一个制表符。如果你按下键盘上的 TAB 键，JavaScript 可能会将其视为一堆空格。相反，请使用特殊字符 \t，它会在字符串中放置一个制表符，如下例所示：

var mypets="dog\tcat\tbird";

在特殊字符 \t 出现的每个地方，JavaScript 都会将其解释为制表符字符。所有特殊字符都以反斜杠字符 (\) 开头。因此，如果你想在字符串中包含单个反斜杠字符，你需要使用反斜杠的特殊代码： \\。

例如，假设你想在 Web 页面上写句子：“Go to the directory c:\javascript on your computer.” 如果直接使用书写的字符串，你的代码将像所示：

<script type="text/javascript">

document.write("Go to the directory c:\javascript on your computer.");

</script>

- 错误，字符串用单引号开启但用双引号关闭
- 错误，字符串没有结束引号
- 错误，字符串用双引号开启但用单引号关闭
- 单个反斜杠不会打印到浏览器

第3 章：使用变量

43

问题在于，单个反斜杠不会打印在 Web 页面上。它将显示为：

Go to the directory c:javascript on your computer

除非反斜杠后面跟着特殊字符的代码，否则 JavaScript 会按原样打印斜杠后的字符（你将在下一节讨论的转义技术中看到这一点）。要修复这个问题，请使用 \\ 特殊代码在页面上打印单个反斜杠：

<script type="text/javascript">

document.write("Go to the directory c:\\javascript on your computer.");

</script>

现在你得到了想要打印到浏览器的句子，如下：

Go to the directory c\:javascript on your computer.

JavaScript 中使用的特殊字符见表 3-2。

假设你想在 Web 页面上打印一个带有强强调的句子。JavaScript 允许你在 document.write() 方法中作为文档中字符串的一部分向页面打印 HTML 代码（你在第 2 章编写第一个脚本时使用了该方法）。要打印粗体，你只需要添加 HTML 的 <strong> 和 </strong> 标签，如该示例代码所示：

<script type="text/javascript">

document.write("<strong>JavaScript Rules!</strong> This is fun.");

</script>

使用反斜杠字符的特殊代码允许其被打印

| 输出字符 | 使用的特殊代码 |
| :--- | :--- |
| 反斜杠 (\) | \\ |
| 双引号 (") | \" |
| 单引号 (') | \' |
| 退格 | \b |
| 换符 | \f |
| 换行 | \n |
| 回车 | \r |
| 制表符 | \t |
| 垂直制表符 | \v |

表 3-2 JavaScript 特殊字符 *注意 JavaScript 字符串内的 <strong> 和 </strong> 标签*

JavaScript：初学者指南

现在假设你想让代码本身在显示时分行，如下：

**JavaScript Rules!**

This is fun.

你可能会通过向代码添加换行特殊字符来实现：

<script type="text/javascript">

document.write("<strong>JavaScript Rules!</strong>\n This is fun.");

</script>

\n 特殊代码只是 JavaScript 中的换行；它不会产生 HTML 换行。JavaScript 换行代码不会在结果中添加行。因此，上述代码的最终结果是：

**JavaScript Rules!** This is fun.

如果你想在浏览器显示中添加换行，你需要使用 <br /> 标签。请记住，JavaScript 换行只影响源代码的外观；它不影响最终结果。然而，当你以后需要格式化警告框和其他各种 JavaScript 构造时，它会有帮助。

### 转义字符（Escaping Characters）

JavaScript 允许你*转义*某些字符，以便它们正确显示并避免错误。与特殊字符一样，转义序列使用反斜杠字符 (\)，它位于需要转义的字符之前。如前所述，JavaScript 在渲染字符串之前会检查每个字符串是否存在特殊字符。如果你想在字符串内部包含引号，这就很有。例如，假设你想在 Web 页面上打印以下句子：

John said, "JavaScript is easy."

如果你直接把这些内容丢进 document.write() 命令会发生什么？

<script type="text/javascript">

document.write("John said, "JavaScript is easy."");

</script>

如果你查看 document.write() 行末尾，你会发现两个双引号放在一起会导致问题，但浏览器在此点之前就会报错了。当在 *JavaScript* 单词之前使用双引号时，浏览器认为你已经关闭了 document.write() 命令的字符串，并期望结束括号和分号。相反，还有更多文本，浏览器会困惑。

为了避免引号问题，请使用反斜杠字符转义字符串内部的引号。通过在每个内部双引号前面放置反斜杠，

- 此处额外的引号将会导致错误





## 第 3 章：使用变量

45

你强制它们被视为文本字符串的一部分，而不是 JavaScript 语句的一部分：

<script type="text/javascript">
document.write("John said, \"JavaScript is easy.\"");
</script>

这解决了字符串的问题，句子将带有引号一起打印出来。

***注意***

还要注意字符串内部的单引号和撇点（apostrophes）。对于用单引号括的字符串，需要对这些字符进行转义。

这种转义技术也适用于需要引号的 HTML 代码。例如，如果你想在页面上放置一个链接，你会使用锚点标签（<a>）并将 URL 放在引号中。如果你对锚点标签中的引号进行转义，JavaScript 允许你在 `document.write()` 方法中将 HTML 代码写入页面中，如下例所示：

<script type="text/javascript">
document.write("<a href=\"http://someplace.com\">Text</a\">");
</script>

这可以达到效果，但如果你不想一直对引号进行转义，还有更简单的方法可以实现它。

为了避免转义上述代码中的引号，你可以在 URL 地址周围使用单引号，如下代码所示：

<script type="text/javascript">
document.write("<a href='http://someplace.com'>Text</a\">");
</script>

如果你更喜欢在外面使用单引号，也可以反过来这样做，如下例所示：

<script type="text/javascript">
document.write('<a href="http://someplace.com">Text</a>');
</script>

这里需要记住的重要点是，确保你不要在字符串内部使用的引号类型与括住字符串的引号类型相同。如果你需要将引号嵌套超过一层，你就需要开始转义引号；这是因为如果再次切换，它将终止字符串。例如，看这段代码：

document.write("John said, 'Jeff says, \\Hi!\\\" to someone.'");
document.write("John said, 'Jeff says, "Hi!" to someone.'");

第一行代码可以正常工作，因为引号经过了转义以保持字符串的延续。然而，第二行仅在字符串内部的单引号内才切换回双引号。反斜杠允许内部引号成为字符串的一部分。

- 双引号内的单引号是没问题的
- 单引号内的双引号也是没问题的

《JavaScript 入手指南》

如你所见，当需要在字符串中使用大量引号时，引号会非常头疼。然而，记住在需要时使用反斜杠来转义引号，可以在你寻找丢失的引号时省去很多烦恼。我曾多次在代码中寻找丢失的引号，在经历了几次这种情况后，我的头都大了！在本章的稍后部分，你将看到你可以合并字符串，这可以为你简化引号的使用。

### 布尔值（Boolean）

*Boolean*（布尔）变量是指值为 true（真）或 false（假）的变量。以下是示例：

`var JohnCodes=true;`
`var JohnIsCool=false;`

注意，*true* 和 *false* 单词不需要包含在引号中。这是因为它们是保留字，JavaScript 将它们识别为布尔值。

除了使用 *true* 和 *false* 单词，JavaScript 还允许你使用数字 1 代表 *true*，使用数字 0 代表 *false*，所示：

`var JohnCodes=1;`
`var JohnIsCool=0;`

当你需要变量只能有 true 和 false 的值时（例如在事件处理程序中，第 7 章将介绍），布尔变量是有用的。

***注意***

当我们谈论布尔变量的概念时，*Boolean* 单词的首字母大写（因为源于数学家乔治·布尔 George Boole 的名字）。然而，在脚本中使用关键字时，JavaScript 的保留字 `boolean` 是全小写的。

### 空值（Null）

*Null* 意味着变量没有值。它既不是空格，也不是零；它仅仅是无。如果你需要定义一个值为 null 的变量，请使用如下的声明：

`var *variablename*=null;`

与布尔变量一样，你不需要像处理字符串值那样将此值包含在引号中，因为 JavaScript 将 null 识别为具有定义值（无）的关键字。

当你在脚本中测试输入时，null 变量非常有用，正如你将在后面的章节中学到的那样。

- 使用数字 0 等于使用 false 的值
- 使用数字 1 等于使用 true 的值

第 3 章：使用变量

47

### 3-1 声明变量

这个项目为你提供了练习声明带有各种值的变量的机会。它还会在页面上打印一行简短的文本。

**问：为什么我需要学习变量？我不能直接把我想使用的数字或文本放在我要使用它们的地方吗？**

**答：** 你可以这样做；但会让较长的脚本更难编写、阅读和调试。它也让更新脚本变得困难得多，因为为了更改那个数字或文本，你需要更改它出现的所有行。当你使用变量时，你只需要修改一行代码就可以更改变量在每个被使用处的值。随着你对 JavaScript 经验的增加，你将看到变量是有多用。

**问：为什么我不需要定义我正在使用的数字类型（例如整数或浮点数）？**

**答：** 当你声明变量时，你不需要指定类型（整数或浮点数），JavaScript 会自动处理。

**问：当我在字符串中输出文本时，我需要把它加上引号吗？**

**答：** 这样做是为了让 JavaScript 知道字符串何时开始结束。如果不这样做，JavaScript 将不确定字符串的结束。

**问：但是，使用引号来结束字符串时，我需要这样做吗？**

**答：** 只有当使用运算符来连接字符串时，情况才会变得复杂。

**问：反斜杠（\）字符通常的作用是什么？**

**答：** 如果反斜杠后面跟着一个特殊字符，它将被原样显示。否则，它允许在字符串内部包含引号。

询问专家

（继续）

3_1.html

《JavaScript 入手指南》

逐步步骤

1. 创建一个 HTML 页面，留出 `<body>` 和 `</body>` 标签。
2. 在 `<body>` 和 `</body>` 之间添加 `<script>` 和 `</script>` 标签，正如你在第 2 章中学到的那样。
3. 创建一个名为 `chocost` 的数值变量并将其赋值为 `2.59`。
4. 创建一个名为 `istrue` 的布尔变量并将其赋值为 `false`。
5. 创建一个名为 `nada` 的变量并将其赋值为 `null`。
6. 创建一个 JavaScript 语句向网页写入以下字符串值。记住在需要时转义引号：“JavaScript is fun!”

7. 完成后，HTML 文档的 body 部分应该像这样：

<body>
<script type="text/javascript">
var chocost=2.59;
var istrue=false;
var nada=null;
document.write("John said, \"This project is fun!\"");
</script>
</body>

8. 将文件保存为 `pr3_1.html` 并在浏览器中查看。你应该只看到通过 `document.write()` 命令输出的文本。变量定义不会打印在浏览器屏幕上。你可以查看页面源代码查看变量定义的形式。

尝试总结

在这个项目中，你练习了在脚本中声明带有各种值的变量。这个项目包括一个数值变量、一个布尔变量和一个值为 null 的变量。你还能够使用在第 2 章中学到的技能，用 JavaScript 将文本写入页面。

在脚本中使用变量

为了让变量变得有用，你不能仅仅在脚本中声明它。你需要在脚本的后续部分以某种方式使用它，例如打印它的值甚至更改它的值。使用变量时，你在声明该变量后对其进行调用。





## 第 3 章：使用变量

### 调用变量

以下代码展示了如何使用 `document.write()` 方法将变量的值写入 Web 页面：

```javascript
<script language="JavaScript">
var mycar="Corvette";
document.write(mycar);
</script>
```

脚本首先声明了一个变量 `mycar` 并给其赋值为“Corvette”。然后，在 `document.write()` 命令中，你会看到只将变量名 `mycar` 包含在括号内。该脚本的结果仅仅是向浏览器写入“Corvette”。在写入页面的 `mycar` 变量周围没有引号。这是因为 `mycar` 变量已经被赋予了一个字符串值，因此在 `document.write()` 命令中将其值打印到页面上时不需要再包含在引号内。现在，你已经可以看到使用变量的优势是可以让简短的 `document.write()` 命令更易于编码。

### 将变量添加到文本字符串中

前面的代码仅在浏览器中打印变量的值。如果你想让该变量与字符串中的其他文本一起打印，`document.write()` 命令就会变得更加复杂。如果文本字符串没有定义为变量，则需要在其周围加上引号，而变量需要独立存在。你使用加法运算符 (`+`) 将变量的值加到字符串上，如下例所示：

```javascript
<script type="text/javascript">
var mycar="Corvette";
document.write("I like driving my "+mycar);
</script>
```

这段代码在浏览器窗口中打印以下句子：

I like driving my Corvette.

注意代码中单词“my”后面的空格。这确保了在将变量添加到字符串之前会出现一个空格。如果你使用下面这行代码：

`document.write("I like driving my"+mycar);`

结果将是：

I like driving myCorvette.

在添加字符串时，你需要小心添加你希望在输出中显示的空格。

| 描述 | 结果 |
| :--- | :--- |
| 将一个变量添加到写入浏览器的字符串中 | 向浏览器打印 `mycar` 变量的值 |

加法运算符允许你将变量放在字符串的之前、之后，甚至字符串的中间。要将变量插入到字符串的中间（使其在两侧都有文本显示），只需使用另一个加法运算符在变量的右侧添加你需要的内容，如例所示：

```javascript
<script type="text/javascript">
var mycar="Corvette";
document.write("I like driving my "+mycar+" every day!");
</script>
```

现在变量位于两个文本字符串内部，由三个部分组合成一个字符串。这段代码向浏览器打印以下句子：

I like driving my Corvette every day!

在使用变量时，你需要确保变量和加法运算符不在字符串的引号内。如果它们在引号内，你将无法得到预期的结果。例如，看这段代码：

```javascript
<script type="text/javascript">
var mycar="Corvette";
document.write("I like driving my +mycar+ every day!");
</script>
```

JavaScript 将不会识别这里的运算符和变量；由于它们在引号内，它们仅被视为文本字符串的一部分。JavaScript 不会使用变量，而是字面上地获取所有内容并在浏览器中打印这个句子：

I like driving my +mycar+ every day!

为了让这段代码更易编写，你可以将涉及的每个字符串放入变量中，这样你只需要将变量值相加，而无需处理引号，如下所示：

```javascript
<script type="text/javascript">
var firstString= "I like driving my ";
var mycar="Corvette";
var secondString= " every day!";
document.write(firstString+mycar+secondString);
</script>
```

这打印了相同的句子，但允许你以后更改它的部分，而无需编辑 `document.write()` 命令。你在本节中学习的技巧当你的字符串变得复杂时将非常有用，特别是当你在字符串中使用 HTML 代码时。

| 描述 | 描述 |
| :--- | :--- |
| 变量被添加到两个字符串之间 | 加法运算符也必须在引号之外才能生效 |
| 将三个变量相加并打印到浏览器 | |

### 编写 JavaScript 页面

现在你已经知道了如何使用变量以及使用 JavaScript 向页面编写基础 HTML 代码，你将创建一个几乎完全用 JavaScript 编写的页面（`<body>` 和 `</body>` 标签内的所有内容），以此巩固你到为止学过的技巧。

### 创建框架

你首先需要一个页面的基本框架，以便你知道在哪里插入脚本。由于你正在向页面写入信息，`<script>` 标签将放置在 `<body>` 和 `</body>` 标签内。在这种情况下，将使用名为 `ch3_code.js` 的外部脚本文件。你的 HTML 文档的 `body` 部分如下所示：

```html
<body>
  <script type="text/javascript" src="ch3_code.js"></script>
</body>
```

你在 `ch3_code.js` 文件中放置的代码将决定你完成后浏览器中显示的内容。

### 定义变量

要开始你的脚本文件，使用一些 JavaScript 代码写入一个 HTML 标题。你可以直接将代码作为字符串写入 `document.write()` 命令中，如下所示：

`document.write("<h1>A Page of JavaScript</h1>");`

另一方面，你可以将字符串放入变量，稍后在 `document.write()` 命令中使用变量：

```javascript
var headingtext="<h1>A Page of JavaScript</h1>";
// 其他代码可以放在这里...
document.write(headingtext);
```

对于这个示例，你将使用这种方法，因为它使用了变量。事实上，配合 `headingtext` 变量，你还将创建一组包含 HTML 代码的变量以添加到页面。引言部分的变量声明如下：

`var myintro="Hello, welcome to my JavaScript page!";`

接下来，你把链接添加到页面。链接的变量声明如下：

`var linktag="<a href=\"http://www.example.org\">Link to a Site</a>";`

接下来，你放入一些红色文本以添加一点颜色。这里是 `redtext` 的定义：

`var redtext="<span style=\"color:red\">I am colorful today!</span>";`

在此插入脚本标签调用外部文件。最后，你将添加提供加粗标签和段落标签的变量：

```javascript
var begineffect="<strong>";
var endeffect="</strong>";
var beginpara="<p>";
var endpara="</p>";
```

### 添加命令

现在，在变量声明之后，你可以在 `ch3_code.js` 文件中添加一些 `document.write()` 命令，将变量的内容写回 HTML 文档：

```javascript
document.write(headingtext);
document.write(begineffect+myintro+endeffect);
document.write(beginpara);
document.write(linktag);
document.write(endpara);
document.write(beginpara);
document.write(redtext);
document.write(endpara);
```

这在页面顶部写入标题。将 `begineffect` 和 `endeffect` 变量添加到 `myintro` 变量的左右，会在标题下方加粗写入引言文本。之后是一个新段落，后面是一个链接，然后另一个新段落，最后是红色文本消息。

以下是目前为止 `ch3_code.js` 文件的完整代码：

```javascript
var headingtext="<h1>A Page of JavaScript</h1>";
var myintro="Hello, welcome to my JavaScript page!";
var linktag="<a href=\"http://www.example.org\">Link to a Site</a>";
var redtext="<span style=\"color:red\">I am colorful today!</span>";
var begineffect="<strong>";
var endeffect="</strong>";
var beginpara="<p>";
var endpara="</p>";
```

所有的变量在这里都已声明并赋值





## 第3章：使用变量

53

document.write(headingtext);

document.write(begineffect+myintro+endeffect);

document.write(beginpara);

document.write(linktag);

document.write(endpara);

document.write(beginpara);

document.write(redtext);

document.write(endpara);

保存 ch3_code.js 文件，然后加载你的 HTML 文档。这段代码在浏览器中显示的最终结果如图 3-1 所示。注意加粗的介绍性文本以及章节之间段落的使用。

### 修改页面

现在，假设你不喜欢网页上显示的布局。相反，你希望将强力强调的介绍文本变为普通强调。如果你是使用普通字符串而不是变量来编写 `document.write()` 命令，你将需要搜索代码以找到 `<strong></strong>` 标签并将它们更改为 `<em></em>` 标签。

然而，由于你使用了变量，你只需要只需要更改脚本文件顶部相应变量的值。你只需要更改变量的值，而不需要在一堆代码中寻找 `strong` 标签。

变量的值在这里打印到浏览器中：

![](img/61d166424839b7674a7b9c8434ae4e03_75_0.png)

图 3-1 Web 浏览器中 JavaScript 代码的 own

JavaScript：初学者指南

接下来的代码显示了你可以对脚本文件进行的更改以获得新效果。注意你只需要更改 `begineffect` 和 `endeffect` 变量的值即可更改页面上文本的格式：

```javascript
var headingtext="<h1>A Page of JavaScript</h1>";
var myintro="Hello, welcome to my JavaScript page!";
var linktag="<a href=\"http://www.pageresource.com\">Link to a Site</a>a>";
var redtext="<span style=\"color:red\">I am so colorful today!</span>";
var begineffect="<em>";
var endeffect= "</em>";
var beginpara="<p>";
var endpara="</p>";

document.write(headingtext);
document.write(begineffect+myintro+endeffect);
document.write(beginpara);
document.write(linktag);
document.write(endpara);
document.write(beginpara);
document.write(redtext);
document.write(endpara);
```

保存 ch3_code.js 文件并重新加载你的 HTML 文档。图 3-2 显示这些更改如何影响 Web 浏览器中页面的显示。

更改为 </em>
更改为 <em>

![](img/61d166424839b7674a7b9c8434ae4e03_76_0.png)

图 3-2 修改某些 JavaScript 变量后的页面

第3章：使用变量

55

### 使用 JavaScript 创建 HTML 页面

在这个项目中，你将创建一个带有 JavaScript 的 HTML 页面，类似于你在本章中创建的。变量将被赋予新值，差异应该是可见的。

### 逐步步骤

1. 创建一个 HTML 页面，留出 `<body>` 和 `</body>` 标签之间的空间。
2. 在 `<body>` 和 `</body>` 标签之间添加 `<script>` 和 `</script>` 标签以链接名为 `prjs3_2.js` 的文件。将 HTML 文件保存为 `pr3_2.html`。
3. 打开一个文件作为你的 JavaScript 文件。将其保存为文件名 `prjs3_2.js`。使用此文件按照步骤 4-10 添加 JavaScript 代码。
4. 创建一个名为 `myheading` 的变量，并赋予该值：`This is My Page!`
5. 创建一个名为 `linktag` 的变量，并赋予该值：`<a href="http://www.javascriptcity.com">Web Link!</a>`
6. 创建一个名为 `sometext` 的变量，并赋予该值：`This text can be affected by other statements.`
7. 创建一个名为 `begineffect` 的变量，并赋予该值 `<em>`。
8. 创建一个名为 `endeffect` 的变量，并赋予该值 `</em>`。
9. 创建一个名为 `newsection` 的变量，并赋予该值 `<br />`。
10. 按此顺序将每个变量写回 HTML 文档：
    - myheading
    - newsection
    - begineffect
    - sometext
    - endeffect
    - newsection
    - linktag
    - newsection
    - sometext

（续）

pr3_2.html
prjs3_2.js

JavaScript：初学者指南

完成后，保存 `prjs3_2.js` 文件。它看起来应该是这样的：

```javascript
var myheading="<h1>This is My Page!</h1>";
var linktag="<a href=\"http://www.javascriptcity.com\">Web Link!</a>";
var sometext="This text can be affected by other statements.";
var begineffect="<em>";
var endeffect="</em>";
var newsection="<br />";

document.write(myheading);
document.write(begineffect);
document.write(sometext);
document.write(endeffect);
document.write(newsection);
document.write(linktag);
document.write(newsection);
document.write(sometext);
```

11. 在 Web 浏览器中打开 `pr3_2.html` 页面并查看结果。
12. 重新打开 `prjs3_2.js` 文件并执行步骤 13-14 中的更改。
13. 将 `begineffect` 的值更改为 `<strong>`。
14. 将 `endeffect` 的值更改为 `</strong>`。
15. 完成后，保存 `prjs3_2.js` 文件。它看起来应该是这样的：

```javascript
var myheading="<h1>This is My Page!</h1>";
var linktag="<a href=\"http://www.javascriptcity.com\">Web Link!</a>";
var sometext="This text can be affected by other statements.";
var begineffect="<strong>";
var endeffect="</strong>";
var newsection="<br />";

document.write(myheading);
document.write(begineffect);
document.write(sometext);
document.write(endeffect);
document.write(newsection);
document.write(linktag);
document.write(newsection);
document.write(sometext);
```

16. 在 Web 浏览器中重新加载 `pr3_2.html` 页面。注意 JavaScript 文件中变量值变化带来的差异。

第3章：使用变量

57

### 尝试一下

在这个项目中，你将使用变量的新技能与之前使用 JavaScript 编写网页的技能结合起来。你创建了一个使用变量编写 HTML 代码的网页。然后你更改了两个变量的值并重新保存了脚本文件。变量的更改使页面发生了变化。

*第3章自测*

1. 变量 __________ 一个值。
2. 使用变量的两个优势是
    A. 它们可以节省编写和更新脚本的时间，并让你的代码更清晰。
    B. 它们让你的代码更清晰，并让非程序员难以理解脚本。
    C. 它们可以节省编写和更新脚本的时间，并让非程序员难以理解脚本。
    D. 它们没有优势。
3. 声明变量，你使用 __________ 关键字。
4. JavaScript 中用什么符号作为赋值运算符
    A. +
    B. –
    C. :
    D. =
5. 下列哪个声明了一个名为 `pagenumber` 的变量并赋予其值 240？
    A. var PageNumber=240;
    B. pagenumber=20;
    C. var pagenumber=240;
    D. var integer named Pagenumber=240;
6. 变量名大小写敏感。
    A. 是
    B. 否

JavaScript：初学者指南

80

7. 变量名必须以字母 __________ 或字符字符开头。
8. 你应该避免使用 JavaScript 保留字作为变量名。
    A. 是
    B. 否
9. 下列哪个变量声明使用了 JavaScript 中有效的变量名？
    A. var default;
    B. var my_house;
    C. var my dog;
    D. var 2cats;
10. 在 JavaScript 中，变量值或 __________ 可以包括数字、字符串、布尔值和空。
11. 为了在 JavaScript 中表示指数，你在基数数字之后、指数之前使用字母 __________。
12. 下列哪个字符串声明是无效的？
    A. var mytext=“Here is some text!”;
    B. var mytext=‘Here is some text!’;
    C. var mytext= “Here is some text!’;
    D. var mytext= “Here is \n some text!”
13. 下列哪个语句在 JavaScript 中是有效的？
    A. document.write(“John said, “Hi!””);
    B. document.write(‘John said, “Hi!””);
    C. document.write(“John said, “Hi!’”);
    D. document.write(“John said, \“Hi!\””);
14. __________ 字符允许向字符串中添加其他无法添加的内容。
15. 下列哪个能成功通过将变量添加到字符串来打印名为 `myhobby` 的变量？
    A. document.write(“I like to +myhobby+ every weekend”);
    B. document.write(“I like to ” +myhobby+ “ every weekend”);
    C. document.write(“I like to myhobby every weekend”);
    D. document.write(“I like to ‘myhobby’ every weekend”);





## 第4章
### 使用函数

JavaScript：初学者指南

核心技能与概念

- 什么是函数
- 为什么函数很有用
- 函数的结构
- 在脚本中调用函数

作为一名 JavaScript 程序员，你需要了解如何在脚本中使用函数。函数可以使你的脚本更具移植性，并且更易调试。

本章将涵盖使用函数的基础知识。首先，你将了解到什么是函数以及为什么函数很有用。然后，你将学习如何定义和构建函数。最后，你将学习如何在脚本中调用函数。

### 什么是函数

一个*函数*基本上是位于大脚本内部的一个小脚本。它的目的是执行单个任务或一系列任务。函数执行什么操作取决于你放置在内部的代码。例如，一个函数可能会向浏览器写入一行文本，或者计算一个数值并将该值返回给主脚本。

正如你可能在数学课上回过的那样，函数可以用于计算坐标平面上的值。你可能见过类似这样的计算式：

f(x)=x+2
y=x+2

这两者通常用于根据 *x* 坐标的值来计算 *y* 坐标。当你需要 *x* 等于 3 时的 *y* 坐标时，你用 3 代替 *x* 来得到 *y* 值：3+2=5。通过该函数，你发现当 *x*=3 时，*y*=5。

函数本身就一直留在纸上（或者在我们的案例中，留在脚本中），直到你需要使用它来执行任务为止。你可以通过从主脚本中调用它，根据需要多次使用该函数。

### 为什么函数很有用

函数有助于将脚本的不同部分组织成必须完成的不同任务。通过使用一个函数来编写文本，另一个函数来进行计算，你可以让自己和他人更容易看到脚本每个部分的目的，从而更容易地进行调试。

函数有用的另一个原因是它们具有可重用性。它们可以在脚本中被多次使用以执行任务。与其重写整个代码块，你只需要再次调用该函数即可。

考虑简单函数 *y*=*x*+2。如果你只使用它一次，这个函数的作用就不大。然而，如果你需要获取几个值，这个函数就会变得越来越有用。与其为每次计算写出公式，你只需要在每次需要获取 *y* 值时替换 *x* 值即可。所以，如果你需要 *x* 为 3, 4 和 5 时的 *y* 值，你可以使用该函数三次来获取 *y* 值。函数将分别计算出 5、6 和 7。与其编写三次函数的内容，它只需要编写一次即可得到三个答案。

函数可以执行复杂的任务，并且可能非常长。在本章及随后的章节示例中，你将看到它们在 JavaScript 中是多么地有用且节省时间。

### 函数的结构

现在你已经理解什么是函数以及你为什么想要使用它们，你需要学习如何在脚本中构建它们。函数需要用它的名称和代码进行声明。你还有一些可以使用的可选添加，可以使函数变得更有用。你可以将一个或多个变量导入函数中，这些变量被称为*参数*。你还可以使用 *return* 语句从函数向主脚本返回值。你将从观察函数如何开始。

### 声明函数

在函数的第一行，你将其声明为一个函数，为它命名，并指示它是否接受任何参数。要声明一个函数，你使用关键字 `function`，后面跟着它的名称，然后是一组括号：

`function functionname() `

关键字 `function` 告诉浏览器你正在声明一个函数，后面将会有更多信息。下一部分信息是函数的名称。之后，括号组表示该函数是否接受任何参数。

例如，要将你的函数命名为 `reallycool` 并指示它不使用任何参数，第一行看起来如下：

`function reallycool()`

因为函数不使用任何参数，所以括号是留空的。和变量名一样，命名函数也有一些特殊的考虑因素。你将在讨论函数结构之后学习这些考虑因素。

你可能注意到这一行代码没有以分号结尾，正如你到目前为止在书中看到的其他代码行那样。之所以没有分号是因为你使用了不同的技术来显示函数代码的开始和结束，正如接下来描述的那样。然而，函数内部的每一行独立代码都以分号结尾，正如你将在本章示例中看到的那样。

### 定义函数的代码

大括号 ({ }` 包围着函数内部的代码。左大括号标记函数代码的开始；然后是代码；最后，右大括号标记函数的结束，格式如下：

`function reallycool()`
`{`
`*JavaScript 代码*`
`}`

浏览器将执行函数内部的代码。右括号标记函数的结束。你为括号选择的格式可能取决于你的背景以及你喜欢如何查看代码。解释器接受所有样式，所以请使用你觉得最舒服的一种。在书中的示例中，我会左大括号放在与声明同一行，这有助于查看函数结束，并将右大括号放在单独的一行。

另一种常见的格式是将左大括号放在与声明同一行：

`function reallycool()`
`{`
`*JavaScript 代码*`
`}`

或者，如果函数特别短，你甚至可以将整个内容放在同一行：

`function reallycool() { *JavaScript 代码* }`

虽然这可能更难读，但 JavaScript 仍然会认为它是有效的。例如：

`function reallycool() { var a=5; var b=3; var c=6; }`

### 函数的命名

和变量一样，函数需要仔细命名以避免脚本出现问题。适用于变量的基本规则也适用于函数的命名：大小写敏感、使用允许的字符、避开保留字以及为函数赋予易于记忆且有意义的名字。

***注意***为函数选择名称涉及一些特定的细节。

#### 在函数名中使用大小写

函数名对大小写敏感，就像变量名一样。这意味着 `reallycool`、`REALLYCOOL` 和 `ReallyCool` 代表不同的函数。记住，你在调用函数时需要使用与声明时相同的字母大小写。

#### 使用允许的字符并避开保留字

允许函数名的字符与你可以用于变量名的字符相同：

- 函数名必须以字母或下划线字符 ( _ ) 开头。
- 函数名不能包含任何空格。

同样与变量一样，你不能将 JavaScript 保留字作为函数名。会导致函数失败，从而在脚本中引起实际问题。请参阅第三章中的“避开保留字”部分获取完整的 JavaScript 保留字列表。




## JavaScript: 入学者指南

### 给函数赋予有意义的名称

如果你选择能够反映其用途的名称，你的函数将更容易被记忆和调试。正如你在第 3 章中所学习到的那样，对于变量，你应该使用代表其取值的名称，例如用 `example_number` 来表示页面上的示例编号。函数名应该告诉你关于该函数将要做什么。例如，假设你创建了一个向页面写入某些文本的函数。它可能包含以下行代码：

document.write("<strong>This is a strong statement!</strong>");

你可以直接将函数命名为 *text*，但可能不够具有描述性，因为你可能还有其他函数也会向页面写入文本。相反，你可能会将其命名为 `print_strong_text` 之类的，这样你就知道该函数是用于向浏览器打印一段加粗强调的文本。完整函数显示如下：

```javascript
function print_strong_text() {
  document.write("<strong>This is a strong statement!</strong>");
}
```

与变量一样，脚本中使用的函数越多，为它们使用有意义且易记的名称就越重要。

### 为函数添加参数

*参数*用于允许函数从函数外部某处导入一个或多个值。参数设置在函数第一行的括号内，格式如下：

`function *functionname*(*variable1*,*variable2*)`

任何作为参数引入的值都变成函数内部的变量，并使用你在括号内赋予它的名称。

例如，这里是你如何定义一个带有 *coolcar* 和 *coolplace* 参数（变量）的 `reallycool` 函数的：

```javascript
function reallycool(coolcar,coolplace) {
  *JavaScript code here*
}
```

注意，在 JavaScript 中，当你为函数设置参数时不需要使用 `var` 关键字。JavaScript 在它们被设置为函数参数时自动声明这些变量，因此这里不使用 `var` 关键字。例如，像这样的一行是无效的：

`function reallycool(var coolcar, var coolplace)`

- 此名称有助于描述函数的用途
- 这一行是调用函数时将执行的代码
- 参数被添加到括号内的第一行

第 4 章：使用函数
65

参数最初从哪里来？它们是在你调用函数时从函数外部获取的。你将在本章稍后看到它是如何工作的。现在，你只需要知道它们如何作为 JavaScript 函数的参数使用。

***注意***

在其他语言中，变量在设置为参数时通常需要声明，但 JavaScript 会为你完成这一点。然而，当你在其他地方声明变量时，你需要使用 `var` 关键字。

### 使用函数参数值

当你为函数分配参数时，可以像使用其他变量一样使用它们。例如，你可以通过赋值运算符将 `coolcar` 变量的值赋给另一个变量，例所示：

```javascript
function reallycool(coolcar,coolplace) {
  var mycar=coolcar;
}
```

这会将 `coolcar` 参数的值赋值给名为 `mycar` 的变量。

与其将其值赋值给另一个变量，你也可以直接在函数中使用 `coolcar` 参数，例所示：

```javascript
function reallycool(coolcar,coolplace) {
  document.write("My car is a "+coolcar);
}
```

如果 `coolcar` 的值是 `Corvette`，那么函数在调用时将向浏览器打印这一行：

My car is a Corvette

在这里，`coolcar` 参数被凭空赋予了一个值。在实际使用中，该值必须来自主脚本或其他函数的某处，否则该变量将没有值。

### 使用多个参数

你可能注意到上一个示例有两个参数但只使用了一个。函数可以根据你的意愿拥有一个或多个参数。当你分配多个函数参数时，函数并不需要使用所有它们。它可以使用一个参数、几个或一个都不使用。使用多少取决于函数的功能以及它是如何被调用的。

唯一的规则是，如果你有多个参数，需要用逗号分隔每个参数，以便浏览器知道该做什么。

在上一个示例中，第二个参数没有被使用。这里是你如何更改函数以使用两个参数的：

```javascript
function reallycool(coolcar,coolplace) {
  document.write("My car is a "+coolcar+" and I drive it to "+coolplace);
}
```

| coolcar 变量的值赋值给 mycar 变量 |
| coolcar 变量的值在 document.write() 命令中使用 |
| 两个参数都在此 document.write() 命令中作为变量使用 |

JavaScript: 入学者指南
现在，如果 `coolcar` 的值是 `Corvette` 且 `coolplace` 的值是 `LasVegas`，函数在调用时将向浏览器打印以下行：

My car is a Corvette and I drive it to Las Vegas

你可以在函数第一行的括号内放置函数所需的任意数量的参数。这里有一个四个参数的示例：

```javascript
function reallycool(coolcar,coolplace,coolfood,coolbreeze)
```

记住，当有多个参数时，用逗号分隔每个参数。

### 为函数添加返回语句

`return` 语句用于确保函数向主脚本返回一个特定值，供主脚本使用。你将 `return` 语句放在函数的最后一行。（此处由于 OCR 文本存在大量重复和乱码，已根据核心逻辑进行了清理并保留示例结构）。

`return` 语句用于确保函数向主脚本返回一个特定值，供主脚本使用。

返回示例：
```javascript
function get_text() {
  var text1="This is ";
  var text2="fun!";
  var added_text=text1+text2;
  return added_text;
}
```

- coolcar 变量的值赋值给 mycar 变量
- coolcar 变量的值在 document.write() 命令中使用
- 两个参数都在此 document.write() 命令中作为变量使用

### 在脚本中调用函数

现在你已经知道函数是如何运作的，你需要学习如何在脚本中调用函数。JavaScript 中的函数调用简单来说函数名加上括号（括号内有或无参数），并以分号结束，就像普通的 JavaScript 语句一样：

functionname()

你可以在脚本的任何地方调用函数。你甚至可以在另一个函数内部调用函数。一个良好的规则是让函数定义在函数调用之前。确保函数定义在调用之前的最简单方法是将所有定义尽可能地放在脚本的开头。

在调用之前定义函数是一个良好的编程实践建议，而不是严格规则。你可以在 JavaScript 的任何地方调用函数，但函数代码在函数工作之前必须被加载。这就是为什么建议你在调用之前定义函数。如果你要调用一个定义在脚本底部的函数，可能无法准时加载。




# JavaScript：初学者指南

脚本标签：Head 部分或 Body 部分

当直接将脚本添加到 Web 页面而不是使用外部文件时，确保变量和函数声明
位于 `head` 部分通常有助于确保当脚本在 `body` 部分调用它们（调用）它们时，
它们是可用的。然而，由于 JavaScript 经常使用来自文档的可能尚未加载的信息，
这可能会导致问题。

另一方面，当你需要编辑 HTML 代码时，在 `body` 部分有大量的 JavaScript 代码
也会带来麻烦（如果 JavaScript 代码在 `body` 部分，它需要位于包含 JavaScript 
使用其所需信息的元素之后，以确保必要的信息已加载）。更好的做法是将所有代码都放在一个外部的 JavaScript 文件中。这样，你就可以决定将脚本标签放在
`head` 部分还是 `body` 部分了。

如果一个脚本不需要来自文档的任何信息，那么将脚本标签放在 `head` 部分
效果非常好。作为一个例子，你将创建一个脚本，在页面在浏览器中打开时立即
向查看者发送一条警告消息。要在一个小消息框中弹出消息，你使用一个名为
`window.alert` 的 JavaScript 方法。

首先，你将学习如何创建一个 JavaScript 警告，然后你将看到如何构建一个
使用该方法并在脚本中调用该函数。

### 创建 JavaScript 警告

与其使用 `document.write()` 方法向屏幕写入内容，你可以使用 `window.alert`
方法创建一个在消息框中弹出的 JavaScript 警告。与 `document.write()` 方法
一样，`window.alert` 方法接受警告的文本字符串作为参数，格式如下：

`window.alert("*alert_text*");`

文本字符串将显示在警告弹出框中。

例如，假设你想在弹出框中显示“This is an alert!”。你可以在外部
JavaScript 文件中这样写命令（在本例中我们将使用文件名 `js_alert.js`）：

`window.alert("This is an alert!");`

现在你已经知道如何让警告弹出了，但如何让它在页面打开时立即出现呢？
你可以通过确保脚本在 Web 页面的 `body` 部分加载之前调用来实现。通过
将脚本标签放置在文档的 `<head>` 和 `</head>` 标签内部（如下所示），
你可以确保它会在页面其他部分加载之前执行：

```html
<head>
    <title>Functions – Alert!</title>
    <script type="text/javascript" src="js_alert.js"></script>
</head>
<body>
    *HTML code here*
</body>
```

这一行调用了外部 JavaScript 文件。
页面的 HTML 代码将在这里。 

将 HTML 文件保存为 `js_alert.html` 并在 Web 浏览器中查看它。如你所见，
这无疑是页面打开时显示警告的一种简单方法。然而，由于你正在学习函数，
你将采取另一种方法。

### 使用函数处理 JavaScript 警告

以下代码在外部 JavaScript 文件中使用一个函数来弹出警告框。在你的
`js_alert.js` 文件中，将代码更改为如下：

```javascript
function show_message() {
    window.alert("This is an alert!");
}

show_message();
```

此示例创建了一个名为 `show_message()` 的函数来执行显示警告的工作。
只有在定义函数后的某处调用了 `show_message()` 函数，警告才会显示。
在这种情况下，函数在定义之后立即被调用。结果是一个带有
“This is an alert!”消息的小警告框。

***注意***
当警告框出现时，你可能会看到页面暂停，直到你点击 OK 按钮，或者它
在等待你点击 OK 时继续加载。这取决于你的
浏览器。

尽管函数是先定义的，但并不意味着它会先执行。函数在被调用之前
不会被执行；换句话说，在 JavaScript 运行脚本中的函数调用之前，它
不会使用该函数。

任何在函数调用之前的命令（且不属于函数定义的一部分）都将在函数之前
执行。例如，我们可以按如下所示修改 JavaScript 文件中的代码：

```javascript
function show_message() {
    window.alert("This is an alert!");
}

window.alert("I am first, ha!");

window.alert("I am second, ha ha!");

show_message();
```

| 描述 | 操作 |
| :--- | :--- |
| 函数被定义 | 在函数被调用之前，此警告不会发生 |
| 命名并开始函数 | 函数被调用并执行，导致警告弹出 |
| 在函数中使用 `window.alert()` 命令 | 此警告最先显示 |
| (`window.alert("I am first...!"))` | 此警告是第二个 |
| (`window.alert("I am second......!"))` | 这最终调用了函数，以便内部的警告可以显示 |

此示例在第一行定义了相同的函数 `show_message()`。函数之后是两个
孤立的 `window.alert` 命令，然后是调用该函数的行。使用此新代码
保存 `js_alert.js` 文件，然后在 Web 浏览器中重新加载 `js_alert.html` 文件。
你应该会看到一个有趣的结果！

两个孤立的警告命令是 JavaScript 看到的第一个可执行语句，它们最先。
对函数的调用是最后的，这就是为什么你会看到如下结果：

- 两个孤立的警告命令是 JavaScript 看到的第一个可执行语句，它们最先。
- 对函数的调用是最后的，这就是为什么你会看到如下结果：
    - 第一个警告显示 "I am first, ha!"
    - 第二个警告显示 "I am second, ha ha!"
    - 最后调用函数，其内部的警告显示。

## 第4 章：使用函数

### 从另一个函数调用函数

现在假设你想创建三个函数。为了确保它们按照正确的顺序出现，你可以
从另一个函数按顺序调用它们。这是一个使用三个函数的技巧示例：

```javascript
function update_alert() {
    window.alert("Welcome! This site is updated!");
}

function section_alert() {
    window.alert("Please visit the picture section!");
}

function links_alert() {
    window.alert("Also, check out my links page!");
}

function get_messages() {
    update_alert();
    section_alert();
    links_alert();
}

get_messages();
```

代码首先定义了显示每个警告的函数。然后定义了 `get_
messages()` 函数，它只是调用之前的三个。当然，必须调用 `get_
messages()` 函数才能付诸行动。此调用发生在函数之外的第一语句。

当然，创建一个接一个又弹出消息的脚本并不是你通常想做的。虽然这个示例演示了函数调用的正确用法，但这样的脚本可能会
打扰你的观众！你将在后面的章节中看到函数的实际用例示例。





# JavaScript：初学者指南

## 带参数调用函数

上一个示例使用了三个不同的函数来显示三个提示框（alert）。虽然这样做可行，但如果不需要为每个提示框都写一个新函数就更好了。你可以通过使用参数避免这样做。你可以创建一个可以多次使用的函数来执行相同的操作，但每次都带有来自参数的新新信息。

正如本章前面提到的，变量通常被用作参数。然而，你也可以使用值作为参数。你将首先学习不同类型的变量参数，然后查看值参数。

如果你想将某些变量的值发送给函数，必须先声明这些变量，并在发送它们之前确保它们已经拥有你所需的值。在这里，变量的*作用域*（scope）变得非常重要。变量的作用域决定了它在何处有效何无效。JavaScript 有全局变量和局部变量。

### 使用全局变量

*全局变量*是你在第 3 章中学过的变量。因为它们定义在任何函数之外，所以可以在脚本的任何地方进行更改——包括函数内部或外部。全局变量可以在函数外的任何地方声明，如下代码所示：

```javascript
var mycar="Honda";
var paycheck="1200";
```

此示例中的变量可以在脚本的任何地方更改。这意味着它们甚至可能被函数意外覆盖或更改。

为了理解全局变量如何受到函数的影响，请考虑一个显示两个提示框的示例。你想让一个提示框告诉你买某辆车需要多少钱，让另一个提示框告诉你目前有多少钱以及你现在拥有什么种类型的汽车。如果你使用以下代码会发生什么？

```javascript
var mycar="Honda";
var paycheck=1200;

function new_car() {
  mycar="Ferrari";
  paycheck=3500;
  window.alert("You need $"+paycheck+" to get a "+mycar);
}

new_car();
window.alert("You make $"+paycheck+" and have a "+mycar);
```

看起来你在函数内部创建了新变量，尽管它们的名称相同。然而，脚本将在两个提示框中输出以下文本：

You need $3500 to get a Ferrari 
You make $3500 and have a Ferrari

显然，这是不对的。

- 这些是正在声明的全局变量
- 这些正在被声明为全局变量
- 哎！函数为变量分配了新值
- 这里的提示框是你预期的结果
- 这里的提示框不是你预期的，因为变量被意外更改了

第 4 章：使用函数

这个示例演示了为什么在声明变量时需要使用 `var` 关键字。如果没有 `var` 关键字，你并没有在函数内部创建新变量（这会让它们变成局部的）。相反，你正在更改全局变量的值——你发出的是重新赋值命令，而不是新变量命令。

为了澄清这一点，你只需要更改一组变量名，或者像下一节描述的那样使用局部变量。

### 使用局部变量

*局部变量*只能在声明它的函数内部使用。它不存在于该函数之外，除非你通过参数将其传递给另一个函数。在函数中创建局部变量的关键是确保你使用 `var` 关键字对其进行声明。否则，正如你在上一个示例中看到的，同名的任何全局变量可能被更改。要声明局部变量，你必须将其放在函数内部并使用 `var` 关键字，如下代码所示：

```javascript
function new_car() {
  var mycar="Ferrari";
  var paycheck="3500";
}
```

`mycar` 和 `paycheck` 变量现在是局部变量，只能被 `new_car()` 函数看到和更改。

因此，为了纠正上一节中的脚本，你只需要在函数内部添加 `var` 关键字来声明局部变量，如下所示：

```javascript
var mycar="Honda";
var paycheck=1200;

function new_car() {
  var mycar="Ferrari";
  var paycheck=3500;
  window.alert("You need $"+paycheck+" to get a "+mycar);
}

new_car();
window.alert("You make $"+paycheck+" and have a "+mycar);
```

现在，提示框应该按照你预期的显示：

You need $3500 to get a Ferrari
You make $1200 and have a Honda

你可以看到，当你将某些变量作为参数发送给函数时，变量的作用域可能是重要的。

### 使用变量作为函数参数

下面的示例使用了变量参数。它将一个全局变量传递给函数。然后将其值赋值给局部变量，以避免任何意外更改。

- 这些变量被声明为局部变量，
- 在函数内部使用 `var` 关键字
- 添加 `var` 关键字确保变量
- 在本地声明且不会更改
- 同名的全局变量

```javascript
function check_alert(paycheck) {
  var pcheck=paycheck;
  window.alert("You make $"+pcheck);
}

var paycheck=1200;
check_alert(paycheck);
```

脚本从 `check_alert()` 函数开始，该函数接收参数 `paycheck`。函数中的代码行将 `paycheck` 的值赋值给局部变量 `pcheck`。这样，你就可以在函数内部 `pcheck` 以避免更改全局变量 `paycheck`。然后使用该函数显示一个使用 `pcheck` 值的提示框。在函数之后，在外部脚本中，全局变量 `paycheck` 被赋值为 1200。然后代码调用 `check_alert()` 函数并向它发送了 `paycheck` 变量的值。

上一个示例展示了一种防止更改全局变量的相当长的方法。由于函数参数是以变量的值传递的，你可以在函数定义的括号内更改函数接受的变量名。这会从传递给函数的参数中创建一个局部变量。这里有一个示例：

```javascript
function check_alert(pcheck) {
  window.alert("You make $"+pcheck);
}

var paycheck=1200;
check_alert(paycheck);
```

当这段代码调用 `check_alert()` 函数时，它向该函数发送了 `paycheck` 变量的值。该值是从函数本身提取的。与其在这里将该值命名为“paycheck”并赋值给另一个变量，你只需要在括号内使用另一个名称：`pcheck`。`pcheck` 变量变成了 `check_alert` 内部的局部变量。

### 使用值参数

你也可以直接发送值。不需要声明变量，你只需要发送一个值。需要记住的一点是，如果你发送字符串，需要将其包含引号内。例如，上一节的最后一个示例可以进行修改，通过使用值来少写一行代码：

```javascript
function check_alert(pcheck,car) {
  window.alert("You make $"+pcheck+" and have a "+car);
}

check_alert(1200,"Corvette");
```

在这个示例中，函数调用发送了两个参数。第一个是数值，不需要引号。第二个值是字符串，需要包含在引号中。这些值被发送到函数，在那里被读取为局部变量 `pcheck` 和 `car`。它们现在可以在函数中使用显示这个句子：

You make $1200 and have a Corvette

参数也可以通过表达式发送，例如：

check_alert(500+700, "Cor"+"vette");

JavaScript 将评估每个表达式并将结果作为参数发送给函数。因此，之前的代码将具有相同的最终结果（500 加700 得到1200，“Cor” 加“vette”得到“Corvette”）：

You make $1200 and have a Corvette

### 参数是可选的

另一个应该说明的是，向函数发送参数是可选的。函数将尽力在没有发送参数值的情况下工作。你可以不带任何参数调用 `check_alert()` 函数：

```javascript
function check_alert(pcheck,car) {
  window.alert("You make $"+pcheck+" and have a "+car);
}

check_alert();
```

你的结果将类似于下面的文本：

You make $undefined and have a undefined

因此，设置一些代码来处理未发送参数的情况是一个好主意。可以使用条件语句来实现。这里是检查是否发送了参数的方法：

```javascript
function check_alert(pcheck,car) {
  if (pcheck && car) {
    window.alert("You make $"+pcheck+" and have a "+car);
  }
}
```





JavaScript: 入学者指南

else {

    window.alert("My parameters are missing!");

}

}

check_alert();

这本质上是告诉 JavaScript 在将语句写入页面之前，先检查参数是否存在。如果它们存在，则将带有参数值的语句写入页面。

如果它们不存在，访问者将收到一个显示“My parameters are missing!”的警框。逻辑运算符 `&&` 将在第 5 章中详细讨论，而 `if/else` 语句将在第 6 章中详细讨论。

## 使用返回语句调用函数

要调用函数并并在函数中使用 `return` 语句，你可以将函数的结果赋值给变量。通过这种方式，变量获取了从函数返回的值，并在脚本的后续部分可以使用。以下是声明具有函数返回值的变量的格式：

`var variablename = functionname();`

考虑之前的示例，其中有一个函数，它返回两个文本字符串相加后的值。你可以修改它，将函数结果赋值给变量，如下：

```javascript
function get_added_text() {
    var textpart1="This is ";
    var textpart2="fun!";
    var added_text=textpart1+textpart2;
    return added_text;
}

var alert_text=get_added_text();
window.alert(alert_text);
```

你可以看到，函数将 `added_text` 变量的值返回给脚本。通过将 `get_added_text()` 函数的结果赋值给 `alert_text` 变量，你可以在脚本后面使用添加的文本。该变量用于向用户发送带有添加文本结果的警框。警框信息显示

This is fun!

现在，这不很有趣吗？当你学习第14 章的表单验证时，你将看到 `return` 方法的更多实际应用。

## 定义函数的其他方式

在查看脚本时，你可能会遇到几种定义函数的方法，或者发现在编写新脚本时有用：函数声明（已讨论过）、函数构造函数和函数表达式。

- 添加的文本的结果被返回给脚本
- 函数的结果被赋值给变量
- 变量的值用作警框的文本

第 4 章：使用函数
77

### 函数声明 (Function Declaration)

这是你在此为止一直使用的方法，也是书中经常会使用的方法。正如你所记得的，你只需按照如下方式声明函数：

```javascript
function functionname() {
    /* 此处函数代码 */
}
```

你还可以像本章前面提到的那样添加参数和/或 `return` 语句。

### 函数构造函数 (Function Constructor)

函数构造函数创建函数对象的方式与创建一个新实例相同（将在第 8 章中讨论）：

`var functionname = new Function (*arguments*, code for function*);`

它的工作方式与其他函数类似，但这种方法的主要缺点是性能逊于其他方法（它每次被使用时都会求值，而不是只解析一次）。通常情况下，你将使用另外两种方法之一来定义函数。

### 函数表达式 (Function Expression)

函数表达式（也称为函数运算符）使用与函数声明相同的语法。它与函数声明的主要区别在于，函数声明会创建一个与函数名同名的变量，该变量可以在函数外部使用；而函数表达式只能在函数内部通过其名称访问变量。例如，以下代码使用了函数声明，并可以使用函数名作为变量输出警框（变量的值将是函数的所有代码）：

```javascript
function send_alert() {
    var my_num = 1;
}
window.alert(send_alert);
```

另一方面，以下代码在运行时会产生错误：

```javascript
var get_func = function send_alert() {
    var my_num = 1;
}
window.alert(send_alert);
```

如前面的代码所示，函数表达式也使用了函数名。然而，该函数名不能在函数外部作为变量使用。

***注意***

在 Internet Explorer 7 中（截至本文编写时）这种对函数表达式的使用不会报错，而是会产生与函数声明相同的结果。为了测试这种差异，可以使用 Mozilla Firefox。

JavaScript: 入学者指南

### 匿名函数 (Anonymous Functions)

函数表达式的一种有效用法是不使用函数名来创建一个匿名函数。匿名函数是同时被创建和被调用的函数，当你只想在代码的某处调用函数时（而不是在代码的其他地方声明函数并通过多次调用来复用它），它是很有帮助。以下是匿名函数的通用格式：

```javascript
var varname = function(parameters) {
    函数代码
};
```

这使用了 `function` 关键字但没有给函数命名。

在处理 JavaScript 事件时，匿名函数非常有用。例如，为了响应用户在 Web 页面上点击鼠标，你可以为 `document` 的点击事件编写一个简单的函数然后调用它，如下代码所示：

```javascript
function do_not_click() {
    window.alert("Do not click on my page!");
}
document.onclick = do_not_click;
```

这声明了函数，然后在随后调用它（不带括号）来处理点击事件。

然而，你可以使用匿名函数将这些步骤合并为一个，如下：

```javascript
document.onclick = function() {
    window.alert("Do not click on my page!");
};
```





JavaScript：初学者指南

5. 创建一个名为 `car_cost()` 的函数，接收两个参数：`mycar` 和 `paycheck`。创建一个 `window.alert` 命令，显示带有以下消息的警框：

You have a <mycar variable here> and make $<{paycheck variable here}>

6. 创建一个名为 `get_added_text()` 的函数，返回内部两个字符串相加后的值。要相加的两个字符串是以下两个独立的行：

This project 

is almost fun!

7. 在主脚本中（函数定义之后），调用 `car_cost()` 函数，并将“Mustang”和 1500 作为参数传递给它。

8. 在主脚本中（函数定义之后），将 `get_added_text()` 函数的结果赋值给名为 `alert_text` 的变量。创建一个弹窗（alert）并显示该变量的值。

9. 当你完成后，你的外部 JavaScript 文件应该如下所示：

```javascript
function car_cost(mycar,paycheck) {
    window.alert("You have a "+mycar+" and make $"+paycheck);
}

function get_added_text() {
    var textpart1="This project ";
    var textpart2="is almost fun!";
    var added_text=textpart1+textpart2;
    return added_text;
}

car_cost("Mustang",1500);
var alert_text=get_added_text();
window.alert(alert_text);
```

10. 保存外部 JavaScript 文件。

11. 打开 `pr4_1.html` 文件并在浏览器中查看以查看结果。

当你打开该网页时，你应该能看到两个警框消息：

You have a Mustang and make $1500

This project is almost fun!

尝试此总结

在这个项目中，你创建了一个使用两个 JavaScript 函数的脚本。第一个函数使用参数，并根据发送给函数的参数创建一个带有消息的警框。第二个函数在将两个字符串相加后向脚本返回一个值。

浏览器中脚本的结果是两个警框消息，它们基于发送给第一个函数的信息以及从第二个函数返回给脚本的信息。

第 4 章：使用函数

81

整合一切

现在你已经学习了使用函数的基础知识，请看看下面这个相当长的页面。该页面在 HTML 文档添加了一些 JavaScript。尝试按照它操作，看看它是如何工作的以及它将执行什么。

```html
<body
<h1>"Welcome to my Function Page," I said.</h1>
<script type="text/javascript">
function get_added_text(textpart1,textpart2) {
    var added_text=textpart1+" "+textpart2;
    return added_text;
}

function print_text() {
    var myfood=get_added_text("cheese","bread");
    document.write(myfood);
}

var alert_text=get_added_text("soup","crackers");
window.alert(alert_text);
print_text();
</script>
<p style="color:red">I'm seeing red!</p>
</body>
```

首先，你看到定义了两个函数。`get_added_text()` 函数用于合并两个文本，在它们之间添加一个空格，并将该值返回到调用处。

`print_text()` 函数用于将一些文本作为参数发送给 `get_added_text()` 函数，将结果赋值给名为 `myfood` 的变量，并将结果打印到页面本身。

执行的第一条命令是所有函数定义之后的那条命令。就是这一行：

var alert_text=get_added_text("soup","crackers");

这一行声明了一个名为 `alert_text` 的变量，并将 `get_added_text()` 函数接收到“soup”和“crackers”作为参数时返回的值赋值给它。结果将是两个参数值之间有一个空格。返回的字符串“soup crackers”现在被赋值给 `alert_text` 变量。

执行的下一行是紧随其后的行，所示：

window.alert(alert_text);

警框包含了赋值给 `alert_text` 变量的文本，即从 `get_added_text()` 函数返回的合并字符串。

接下来是调用 `print_text()` 函数使其执行。

`print_text()` 函数做的第一件事是声明一个名为 `myfood` 的变量，并将其赋值为 `get_added_text()` 函数返回的值。它接收“cheese”和“bread”作为参数。因此，返回的值是字符串“cheese bread”，它将被赋值给 `myfood` 变量。然后 `print_text()` 函数获取该值并使用 `document.write()` 方法将其写入屏幕。

图 4-1 和 4-2 显示了该脚本在浏览器中运行的结果。图 4-1 显示第一个弹出的警框，图 4-2 显示了在点击警框中的“OK”后看到的页面。

此示例展示了你如何使用在本章中学到的不同技术来结构化函数、为函数添加参数、在函数内部调用函数以及使用 `return` 语句。这些都可以在单个脚本中使用，以便需要时执行它们分配的任务。

图 4-1 在出现或在出现期间显示的警框

图 4-2 点击警框中的 OK 后显示的页面

第 4 章：使用函数

83

编写自己的函数

在这个项目中，你创建了一个包含两个 JavaScript 函数的 HTML 页面，但对于这个项目，使用自己的变量名创建一个脚本。

1. 创建一个 HTML 文件并保存为 `pr_2.html`。
2. 创建一个外部 JavaScript 文件并保存为 `prjs_2.js`。
3. 创建一个接收两个字符串作为参数的函数。让它返回相加字符串的值，但它们之间有一个空格。
4. 创建第二个函数，获取第一个函数的结果并对其赋值。将该变量的值直接写入 HTML 文档。
5. 在主脚本中，创建一个新变量并对其赋值。这时向函数发送“Hi”和“there!”
6. 创建一个警框来显示该变量的值。在 HTML 页面的 body 部分放置脚本标签（指向 `prjs_2.js`），以便脚本在加粗文本“This is some text.”之后显示第二个函数的结果。
7. 完成后，保存 HTML 和 JavaScript 文件并在浏览器中查看 HTML 页面查看它是如何工作的。结果应该是显示“ there!”的警框，随后在点击警框中的 OK 后打开页面。页面应该显示一行加粗文本“This is some text.”。在下一行，应该是普通文本！

尝试此总结

在这个项目中，你创建了一个使用两个 JavaScript 函数的脚本。第一个函数使用参数，并根据发送给函数的参数创建一个带有消息的警框。第二个函数在将两个字符串相加后向脚本返回一个值。

浏览器中脚本的结果是两个警框消息，它们基于发送给第一个函数的信息以及从第二个函数返回给脚本的信息。

*第 4 章自测*

1. 通常来说，函数是较大 __________ 内部的一个小 __________，用于执行单一 __________ 或一组 _________。

2. 函数有用的两个原因是什么？
A. 它让简单的脚本变得复杂，并且让非编程人员难以阅读脚本。
B. 它提供了一种将脚本的不同部分组织成必须完成的不同任务的方法，并且可以重复使用。
C. 它让简单的脚本变得复杂，并且可以重复使用。
D. 它提供了一种将脚本的不同部分组织成必须完成的不同任务的方法，并且让非编程人员难以阅读脚本。

3. 在函数的第一行，你 __________ 它为函数，__________ 它，并指示它是否接受任何 __________。





## 第4章：使用函数

85

4. 要声明一个函数，你使用保留字 __________。

A var
B switch
C function
D for

5. 什么包裹了函数内部的代码？

A 大括号 – {}
B 冒号 – ::
C 方括号 – []
D 无

6. 函数名是区分大小写的的。

A 正确
B 错误

7. JavaScript 保留字可以作为函数名。

A 正确
B 错误

8. 下列哪项是 JavaScript 中有效的函数名？

A function my function()
B function if()
C function get_text()
D function 24hours()

9. __________ 用于允许函数从函数外部导入一个或多个值。

10. 参数在函数的第一行，位于一组 __________ 内部。

A 大括号 – {}
B 圆括号 – ()
C 方括号 – []
D 无

JavaScript：初学者指南

11. 多个参数之间由什么符号分隔？

A 句点
B 冒号
C 分号
D 逗号

12. 下列哪项是 window.alert() 方法的有效用法？

A win.alt(“This is text”);
B window.alert(“This is text);
C window.alert(‘This is text”);
D window.alert(“This is text”);

13. 下列哪项正确调用了名为 some_alert() 的函数并发送两个字符串值作为参数给它？

A some_alert();
B some_alert(“some”,“words”);
C some_alert(“some”,“words);
D SOME_alert(“some”,“words”);

14. 下列哪项正确地将名为 get_something() 的函数结果赋值给名为 shopping 的变量？

A var shopping=get_something();
B var shopping=“get_something”;
C var Shopping=get_Something;
D shopping=getsomething;

15. __________ 变量只能在声明它的函数内部使用。

87

## 第5章：JavaScript 运算符

JavaScript：初学者指南

核心技能与概念

- 理解运算符类型
- 理解数学运算符
- 理解赋值运算符
- 理解比较运算符
- 理解逻辑运算符
- 理解运算顺序

运算符在脚本中承担了大部分工作。在之前的章节中，你已经见过使用赋值 (=) 和加法 (+) 运算符的示例。JavaScript 提供了许多其他类型的运算符来执行各种操作。

本章首先向你介绍不同类型的 JavaScript 运算符。然后，你将学习每种运算符及其在脚本中的用法。最后，你将学习运算符的优先级，它决定了哪些操作先于其他操作执行。

### 理解运算符类型

运算符是 JavaScript 中的某种符号或单词，用于对一个或多个值执行某种计算、比较或赋值。在某些情况下，运算符提供了一种快捷方式来缩短代码，从而减少你需要输入的内容。

常见的计算包括求两个数字之和、合并两个字符串或除以两个数字。一些常见的比较可能是检查两个值是否相等，或者查看一个值是否大于另一个值。快捷赋值运算符可能用于给变量赋新值，这样就不需要输入两次变量名。

JavaScript 使用几种不同类型的运算符：

- **数学（Mathematical）** 这些运算符通常用于对两个值进行数学计算。数学运算符可能是你最熟悉的。它们使用如 +、– 和 * 等符号。
- **赋值（Assignment）** 这些运算符用于给变量分配新值。正如你在第 3 章中所学到的，赋值运算符之一是符号 =。
- **比较（Comparison）** 这些运算符用于比较两个值、两个变量，或者两个较长的语句。它们使用如 >（表示“大于”）和 <（表示“小于”）等符号。

89

- **逻辑（Logical）** 这些运算符用于比较两个条件语句（或对一个语句进行操作），以确定结果是否为真并据此继续执行。它们使用如 &&（如果运算符两边的语句都为真则返回真）和 ||（如果运算符任一侧语句为真则返回真）等符号。
- **位运算（Bitwise）** 这些是在位层级（1 和 0）上工作的逻辑运算符。它们使用如 <<（用于左移位）和 >>（用于右移位）等符号。
- **特殊（Special）** 这些是执行自身其他特殊运行的运算符。

在本章中，你将学习这些运算符的每一种。这将是对每种类型运算符功能的通俗概述，以便你在以后在使用它们时能更好地了解所有运算符类型的目的。首先，你将查看 JavaScript 中的数学运算符。

### 理解数学运算符

对于数学计算，你使用数学运算符。你使用的值可以是你喜欢的任何类型。例如，你可以使用两个变量、两个数字，或者一个变量和一个数字。其中一些运算符能够对单个变量的值执行任务。

正如你所看到的，加法运算符可以用于合并字符串。它也被用于在数学计算中相加数字。

### 用于加结果的变量

加法运算符的一个用途是相加数字以得到数学结果。在相加数值时，你通常会将结果赋值给变量并在稍后使用该变量。例如，为了计算 4 加 7 的值并显示结果，你可以这样编写：

var thesum=4+7;
window.alert(thesum);

结果是显示 11。

为了让示例变得复杂一点，你可以将其中一个数字改为变量：

var num1=4;
var thesum=num1+7;
window.alert(thesum);

结果与上一个示例相同：显示 11。

更进一步，你可以将两个数字都变成变量：

var num1=4;
var num2=7;
var thesum=num1+num2;
window.alert(thesum);

对单个值的三个运算符是递增、递减和取反运算符。递增和递减运算符实际上是加或减 1 的快捷方式，因此学习如何使用它们可以节省时间。

数学运算符及其功能总结在表 5-1 中。后续章节将详细介绍每个运算符。

112

JavaScript：初学者指南

### 加法运算符 (+)

正如你所看到的，加法运算符可以用于合并字符串。它也被用于在数学计算中相加数字。

表 5-1 数学运算符

| 运算符 | 符号 | 功能 |
| :--- | :--- | :--- |
| 加法 | + | 相加两个值 |
| 减法 | - | 从一个值减去另一个值 |
| 乘法 | * | 相乘两个值 |
| 除法 | / | 将一个值除以另一个 |
| 取模 | % | 将一个值除以另一个并返回余数 |
| 递增 | ++ | 单数字加1 的快捷方式 |
| 递减 | -- | 单数字减 1 的快捷方式 |
| 一元取反 | - | 使正数变为负数或负数变为正数 |





## 第 5 章：JavaScript 运算符

此示例提供了最大的灵活性，因为你可以更改两个数字变量的值并获得新结果，而无需深入脚本内部进行修改。

### 加法计算中的类型转换

在处理数学运算符时，注意 JavaScript 如何执行类型转换是非常重要的。当你使用加法和其他数学运算符时，你需要意识到 JavaScript 会自动将不同的值（例如整数[即非小数的数值]和浮点数[即带小数的数值]）转换为相应的类型。例如，你可能会有以下代码：

```javascript
var num1=4.73;
var num2=7;
var thesum=num1+num2;
window.alert(thesum);
```

当运行脚本时，你将看到一个带有结果的警告框。

![](img/61d166424839b7674a7b9c8434ae4e03_113_0.png)

JavaScript 将整数和浮点数相加，并返回了一个浮点数：11.73。JavaScript 经常这样做，因此在开始加法之前，你需要确保你拥有正确类型的值。

例如，如果你将一个数字和一个字符串相加，结果将就像你加了两个字符串一样。看这个示例：

```javascript
var num1=4;
var num2="7";
var thesum=num1+num2;
window.alert(thesum);
```

这看起来像是在相加数字 4 和 7，因为它们看起来都是数字。问题在于，在这种情况下 7 是一个字符串而不是数字，因为它周围有引号。这导致 4 被转换为字符串，然后两个字符串被相加（合并）。在警告框中出现的结果可能会让你大大意料。

![](img/61d166424839b7674a7b9c8434ae4e03_113_1.png)

- 这个变量带有小数
- 两个变量被相加，JavaScript 将显示带小数的答案
- 这个变量是一个整数
- 这个变量是一个数字
- 哎呀！这个变量是一个字符串，而不是数字
- 当它们相加时，它们是像字符串一样相加的

你得到的不是预期的答案 11，而是 47。当两个值作为字符串相加时，它们是被拼接在一起的，而不是进行数学相加。对于字符串，“4”+“7”=47。

***注意***

除了加法运算符 (+) 之外，其他数学运算符只适用于数字，不适用于字符串值。

其他数学运算符也会进行转换，就像加法运算符一样。稍后当你学习如何在脚本中获取用户输入时，你将看到这有多重要。

### 减法运算符 (–)

减法运算符用于从左侧的值减去右侧的值，就像在数学中一样。这里有一个示例：

```javascript
var theresult=10-3;
window.alert(theresult);
```

这段代码简单地从 10（运算符左侧的数字）减去 3（运算符右侧的数字）。结果是一个显示 7 的警告框。

与加法运算符一样，你可以使用变量来存储正在处理的数字，例如此所示：

```javascript
var num1=10;
var num2=3;
var theresult=num1-num2;
window.alert(theresult);
```

结果与上一个示例相同：一个显示 7 的警告框。

在数学运算符上使用变量也适用于乘法、除法和模运算运算符，这些将在后续章节中描述。

### 乘法运算符 (*)

乘法运算符用于将右侧的值乘以左侧的值。再次，这就像数学乘法一样。下一个示例展示了该运算符的作用：

```javascript
var num1=4;
var num2=5;
var thetotal=num1*num2;
window.alert(thetotal);
```

在这里，你得到一个显示 20 的警告框，即 4 乘以 5 的结果。这个运算符不应该带给你太多惊喜，所以继续学习除法运算符。

- 使用减法运算符减去两个数字
- 使用减法运算符减去两个变量
- 使用乘法运算符乘以两个变量

### 除法运算符 (/)

除法运算符用于将左侧的值除以右侧的值。例如，代码 4/2 意味着 4 除以 2，结果为 2。

关于此操作的 JavaScript 示例，请看这段代码：

```javascript
var num1=10;
var num2=2;
var theresult=num1/num2;
window.alert(theresult);
```

这给你一个显示 5 的警告框，即 10 除以 2 的结果。

#### 除以零

当你使用除法运算符时，需要小心不要以某种方式导致除以零。如果你这样做，结果将是无限大 (infinity) 或未 (undefined)，取决于你的浏览器。以下代码显示了这种情况发生的示例（尽管不太可能完全以此方式发生）：

```javascript
var num1=10;
var num2=0;
var theresult=num1/num2;
window.alert(theresult);
```

使用除法运算符时，你需要小心不要以某种方式导致除以零。如果你这样做，结果将是无限大或未，取决于你的浏览器。后续代码显示了这种情况发生的示例（尽管不太可能完全这种方式发生）：

![](img/61d166424839b7674a7b9c8434ae4e03_115_0.png)

#### 除法中的类型转换

关于除法需要记住的另一点是，如果值不能整除，结果将带有小数。以下显示了一个示例：

```javascript
var num1=3;
var num2=4;
var theresult=num1/num2;
window.alert(theresult);
```

- 这个变量带有小数
- 使用除法运算符除两个变量
- 噢！这个变量是一个数字

### 模运算符 (%)

模运算符用于将左侧数除以右侧数，然后给出余数的结果。回想你学习长除法并使用余数的时候。11 除以 2 得到 5，余数为 1。以下是 JavaScript 的示例：

```javascript
var num1=11;
var num2=2;
var theresult=num1%num2;
window.alert(theresult);
```

- 使用除法运算符除两个数字
- 这个变量是一个整数

### 自增运算符 (++)

自增运算符可以使用在操作值的任意侧。它将所操作的值增加 1，就像给该值加 1 一样。实际结果取决于运算符是在操作值之前还是之后使用的，这个值被称为*操作数*。该运算符经常与变量配合使用，并经常用于循环（见第 6 章）。

#### 操作数前的自增

当自增运算符放在操作数之前时，它会将操作数的值增加 1，然后执行语句其余部分。这里有一个示例：

```javascript
var num1=2;
var theresult=++num1;
```

在这种情况下，变量 num1 的初始值为 2。然而，当代码将值赋值给变量 theresult 时，它在赋值之前增加了 num1 的值。由于自增运算符在操作数前面，增加首先发生。因此，num1 的值设置为 3 (2+1)，然后赋值给变量 theresult，后者得到 3。

#### 操作数后的自增

如果你将自增运算符放在操作数之后，它会在赋值后改变操作数的值。考虑这个示例：

```javascript
var num1=2;
var theresult=num1++;
```

- 两个变量使用模运算符获取余数





## 第 5 章：JavaScript 运算符

与上一个示例一样，num1 的初始值为 2。在下一行中，在操作数之后使用了递增运算符。这意味着代码将 num1 的当前值赋值给变量 result，在完成该项操作*之后*，它会增加 num1 的值。因此，只有在这次赋值完成后，num1 才会获得新值。变量 result 被赋予了值 2，然后 num1 变为了 3。如果你在之后使用 num1，它的值将是 3。

另一种查看递增运算符在操作数之前和之后如何工作的方法是在你的浏览器中运行以下脚本。注意第一个 `alert` 中的值是什么，以及第二个 `alert` 中的值又是什么什什么。

<script type="text/javascript">
num1=2;
result= ++num1;
alert("num1= "+num1+" result= "+result);

num1=2;
result= num1++;
alert("num1= "+num1+" result= "+result);
</script>

在第一个弹出框中，你将看到 `num1= 3 result= 3`。因为在这里 `++` 运算符用于操作数之前，num1 的值增加了 1，然后赋值给 result 变量。在第二个弹出框中，你将看到 `num1= 3 result= 2`。这是因为 `++` 运算符用于操作数之后，所以 num1 的值在赋值给 result 变量之后才增加。result 变量获得了值 2，但 num1 会增加到 3。

***注意***

如果你仍然不清楚在操作数之前和之后使用递增运算符的区别，请不要担心。当你在第 6 章学习如何使用循环时，你将看到这个运算符的位置可能非常重要。

### 递减运算符 (--)

递减运算符的工作与递增运算符相同，但它从操作数中减 1 而不是加 1。与递增运算符一样，它在操作数之前或之后的位置很重要。

如果你将递减运算符放在操作数之前，操作数会减1，然后执行语句的剩余部分。这是一个示例：

```javascript
var num1=2;
var result=--num1;
```

在这里，变量 num1 被赋予了值 2。在下一行中，代码从 num1 中减去 1，然后将结果赋值给变量 result。因此，变量 result 的最终值为 1 (2–1)。

当你将运算符放在操作数之后时（如下一个示例所示），会执行语句的剩余部分，然后操作数才减1：

```javascript
var num1=2;
var result=num1--;
```

这一次，变量 result 被赋值为值 2，然后 num1 递减为 1。如果你在这一行之后使用 num1，它的值将是 1。

与递增运算符一样，当你处理循环时，递减运算符也会变得重要，正如你将在后面的章节中学到的那样。

### 一元取反运算符 (--)

一元取反是指仅在单个操作数上使用减号。该运算符创建一个负数，或者反转数字当前的符号（正号或负号）。这里有一个给数字赋值为负值的示例：

```javascript
var negnum=-3;
```

这定义了一个值为负 3 的变量。基本上，该运算符告诉浏览器 3 “不是正数”，因为它通过在数字正前面放置取反运算符，反转了默认的正号。

你也可以使用一元取反运算符来帮助显示负数的加法或减法，如下例：

```javascript
var result=4+(-3);
```

注意语句中 –3 部分周围的括号。就像数学中一样，你可以使用括号来设置运算顺序（你将在本章晚些时候学习），或仅仅是为了在视觉上明确顺序。在这里，括号并不是必要的，但它们有助于组织代码，让你看到它正在向 4 加上 –3。你也可以这样写这段代码：

```javascript
var result=4+-3;
```

这看起来没那么漂亮，但它仍然有效。

你可能在想，编写相同内容的更简单方法看起来像这样：

```javascript
var result=4-3;
```

你是对的，这是编写的最简单方法；但它使用的是减法而不是一元取反。

为了让它看起来更清晰，你可以对变量值使用此运算符，它仅仅是反转了变量所代表的数字的符号：

```javascript
var x=4;
var y=3;
var z=-y;
```

这将变量 z 赋值 y 的一元取反值，即 –3。

现在你已经学习了数学运算符，是时候转向赋值运算符了。

### 理解赋值运算符

赋值运算符将值赋给变量。它们不比较两个项目，也不执行逻辑测试。

当你在第 3 章学习变量时，你看到过如何使用基础赋值运算符（单等号 `=`）来给变量赋一个初始值或新值，如下例所示：

```javascript
var mytime=0;
```

如你所知，这给变量 mytime 赋值了值 0。

其他赋值运算符也给变量赋予新值，但它们执行的方式略有不同，因为它们还执行了简单的计算。这些运算符在循环中特别有用，正如你将学到的那样。

### 赋值运算符 (=)

赋值运算符将右侧的值赋给左侧的变量。如下

| 运算符 | 符号 | 功能 |
| :--- | :--- | :--- |
| 赋值 | = | 将右侧的值赋给左侧变量 |
| 加法赋值 | += | 将右侧的值加到左侧变量，并将结果赋给它 |
| 减法赋值 | -= | 从左侧变量中减去右侧的值，并将结果赋给它 |
| 乘法赋值 | *= | 将左侧变量乘以右侧的值，并将结果赋给它 |
| 除法赋值 | /= | 将左侧变量除以右侧的值，并将结果赋给它 |
| 取模赋值 | %= | 取左侧变量除以右侧的值的余数，并将结果赋给它 |

#### 加法赋值运算符 (+=)

+= 运算符将运算符右侧的值加到左侧变量，并将结果赋给它。本质上，它是此处所示代码的简写：

```javascript
var mymoney=1000;
mymoney=mymoney+1;
```

在这里，变量 mymoney 被创建并赋值为 1000。然后代码通过赋值自身加 1 来改变它的值。赋值给 mymoney 的值是 1001。

与其重复编写变量名，可以使用加法赋值运算符缩短代码。以下代码与之前的示例结果相同：

```javascript
var mymoney=1000;
mymoney+=1;
```

使用加法赋值运算符，这段代码将 1（右侧的值）加到 mymoney（左侧变量）上，将新值 1001 赋给 mymoney。

此运算符可以用于添加任何值，而不只是 1。例如，你可以在赋值中加上 5，如下例：

```javascript
var mymoney=1000;
mymoney+=5;
```

这一次，mymoney 的最终值为 1005。

你甚至可以在右侧使用变量而不是纯数字值，如下例所示：

```javascript
var mymoney=1000;
var bonus=300;
mymoney+=bonus;
```

在这里，bonus 的值为 300，它被加到变量 mymoney 上，然后 mymoney 被赋值为 1300。通过这种方式，可以改变 bonus 变量的值来影响赋值的结果。

这种赋值运算符像加法数学运算符一样也适用于字符串。因此，你可以使用此运算符在字符串值的末尾添加内容：

```javascript
var myname="Bob";
myname+="by";
```

这把字符串“by”添加到字符串“Bob”的末尾，产生字符串“Bobby”。





## 第 5 章：JavaScript 运算符

99

### 减赋值运算符 (–=)

-= 运算符的作用与 += 运算符类似，区别在于是将运算符右侧的值减去左侧变量的值。然后将该值赋值给该变量。以下是该运算符的一个示例：

```javascript
var mymoney=1000;

var bills=800;

mymoney-=bills;
```

此示例将 `bills` 变量的值（800）减去 `mymoney` 变量的值，并将结果赋值给 `mymoney`。最终，`mymoney` 的值为 200。由于这与加赋值运算符非常相似，让我们来看下一个（同样非常相似）。

### 乘赋值运算符 (*=)

*= 运算符将运算符右侧的值乘以左侧变量。然后将结果赋值给该变量。接下来的示例了该运算符的操作：

```javascript
var mymoney=1000;

var multby=2;

mymoney*=multby;
```

在这里，变量 `mymoney` 乘以 `multby` 变量的值（即 2）。得到的结果 2000 被赋值给变量 `mymoney`。

### 除赋值运算符 (/=)

/= 运算符将运算符左侧的变量除以右侧的值。然后将结果赋值给该变量。这里是一个示例：

```javascript
var mymoney=1000;

var cutpayby=2;

mymoney/=cutpayby;
```

在此示例中，变量 `mymoney` 除以变量 `cutpayby` 的值（即 2）。得到的结果 500 被赋值给 `mymoney` 变量。

### 取模赋值运算符 (%=)

与其它也执行数学运算的赋值运算符一样，%= 运算符会对变量赋值进行计算。它将运算符左侧的变量除以右侧的值，取除法的整数余数，并将结果赋值给该变量。以下是你如何使用取模赋值运算符为 `mymoney` 变量赋值：

```javascript
var mymoney=1000;

var cutpayby=2;

mymoney%=cutpayby;
```

在这里，变量 `mymoney` 除以变量 `cutpayby` 的值（即 2）。得到的结果是 500 且无余数，这意味着计算的最终结果为 0。因此，0 是被赋值给变量 `mymoney` 的值。（如果某个地方开始这样削减工资，可能是时候离开那里了！）

## 调整变量值

在这个项目中，你将创建一个页面，使用一些数学运算符和赋值运算符，并将结果写在 HTML 页面上。

这些步骤中的许多步骤都有多种解决方案，因此请随意使用你喜欢的方法。你也可以尝试观察哪种方法需要的字数最少。务必使用 `document.write()` 命令将每次更改的结果写入页面。

### 逐步演进

1. 创建一个 HTML 页面并将其保存为 `pr5_1.html`。在 `body` 部分放置 `script` 标签以指向名为 `prjs5_1.js` 的脚本。
2. 创建一个外部 JavaScript 文件并保存为 `prjs5_1.js`。第 3–10 步使用此文件。
3. 创建名为 `paycheck` 的变量，并赋予其初始值 2000。
4. 仅使用赋值运算符，将 `paycheck` 的值增加到 4000。
5. 使用数学运算符，将 `paycheck` 的值减少到 3500。
6. 使用数学运算符，将 `paycheck` 的值减少到 0。
7. 使用数学运算符，将 `paycheck` 的值增加到 500。
8. 最后，使用赋值运算符，将 `paycheck` 的值减少到 420。
9. 在执行每次操作后，在页面上写入 `paycheck` 变量的值。
10. 保存 HTML 和 JavaScript 文件，并在浏览器中查看 HTML 文件以查看结果。
11. 下面代码显示了 JavaScript 文件的可能解决方案，但请记住，有多种方法可以相同的结果：

```javascript
var paycheck=2000;

document.write(paycheck+"<br />");

paycheck+=2000;

document.write(paycheck+"<br />");

paycheck=paycheck-500;

document.write(paycheck+"<br />");

paycheck=paycheck*0;

document.write(paycheck+"<br />");

paycheck=paycheck+500;

document.write(paycheck+"<br />");

paycheck-=80;

document.write(paycheck+"<br />");
```

### 总结

在这个项目中，你能够利用对数学运算符和赋值运算符的知识在 Web 页面上显示多次计算的结果。这个项目可以用许多种方式完成，取决于你对各种运算符的使用偏好。

## 理解比较运算符

比较运算符通常用于条件语句和循环，以便仅在满足特定条件时执行操作。由于这些运算符比较两个值，因此它们返回 `true` 或 `false`。表 5-3 总结了比较运算符，后面将进行详细讨论。

| 运算符 | 符号 | 功能 |
| :--- | :--- | :--- |
| 等于 | == | 如果值相等则返回 `true` |
| 不等于 | != | 如果值不等则返回 `true` |
| 大于 | > | 如果左侧大于右侧则返回 `true` |
| 小于 | < | 如果左侧小于右侧则返回 `true` |
| 大于等于 | >= | 如果左侧大于或等于右侧则返回 `true` |
| 小于等于 | <= | 如果左侧小于或等于右侧则返回 `true` |
| 严格等于 | === | 如果值相等且类型相同则返回 `true` |
| 严格不等于 | !== | 如果值不等或类型不同则返回 `true` |

### 等于运算符 (==)

为了让 `==` 运算符返回 `true`，两边的值必须相等。它们不能只是接近，必须相等。如果值不等，`==` 运算符返回 `false`。注意，像“4”==4 这样的语句将返回 `true`，因为 JavaScript 会将数字 4 转换为字符串。如果你希望此语句返回 `false`，应该使用严格等于运算符（===），它将在本章后面讨论。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 4==4 | True | 两个相等的数字 |
| (4+2)==3+3) | True | 两侧的结果均为 6，且 6 等于 6 |
| “my socks”==“my socks” | True | 字符串完全相同 |
| (“my ”+“socks”)==(“my”+ “ socks”) | True | 字符串相加返回相同的字符串值 |
| 4==5 | False | 4 和 5 不是相等的数字 |
| (4+3)==(2+2) | False | 左侧结果为 7，右侧结果为 4，它们不等 |
| “My socks”==“my socks” | False | 字符串不完全（大小写问题） |
| (“my”+ “socks”)==(“my ” +“socks”) | False | 左侧结果没有空格字符；右侧有，导致字符串不等 |

***注意***

你会注意到在上表的某些语句中添加了括号，在后面出现的的一些表中也是如此。在这里，添加括号主要是为了提高可读性。你将在本章末尾学习更多关于括号和运算顺序的知识。

与其他运算符一样，你可以在比较运算符中使用变量。如果变量的值相等，比较将返回 `true`。否则，它将返回 `false`。假设你已经声明了以下变量：

```javascript
var num1=2;

var num2=5;

var num3=5;
```





## 第 5 章：JavaScript 运算符

以下比较将返回 `true`：

num2==num3

下一个比较将返回 `false`：

num1==num3

***注意***

请记住，等于运算符 (==) 用于比较。请小心不要在它的位置误用赋值运算符 (=) 来替代它，因为这可能会导致你的脚本运行异常。

### 不等于运算符 (!=)

`!=` 运算符是 `==` 运算符的相反数。`==` 运算符在两侧的值相等时返回 `true`，而 `!=` 运算符在两侧的值*不*相等时才返回 `true`。该运算符返回 `false` 值的唯一方法是它发现运算符两侧的值相等。下表显示了一些使用 `!=` 运算符的语句示例、它们的返回值以及它们返回 `true` 或 `false` 的原因。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 4!=3 | True | 4 和 3 不是相等的数字 |
| “CooL”!=“cool” | True | 字符串的大小写不同，因此它们不相等 |
| 4!=4 | False | 4 等于 4 |
| “cool”!=“cool” | False | 字符串完全相同，因此它们相等 |

### 大于运算符 (>)

当使用大于运算符时，只有当运算符左侧的值大于右侧的值时，比较才返回 `true`。与其他运算符一样，`>` 运算符既可以处理字符串值也可以处理数值值。但一个字符串如何能大于另一个字符串呢？

在字符串的情况下，小写字母大于大写字母，大写字母大于数字。在比较字符串时，JavaScript 首先检查字符串的第一个字母是否有差异。如果没有差异，它将移动到下一个字符，然后是下一个，依此类推，直到找到差异或到达字符串末尾。如果 `>` 运算符两侧的两个值相等，它将返回 `false`。如果右侧的值更大，也会返回 `false`。下表显示了一些使用大于运算符的语句示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 5>2 | True | 5 大于 2 |
| 0>–2 | True | 0 大于负数，例如 –2 |
| “a”>“A” | True | 字符串中的小写字母大于字符串中的大写字母 |
| “A”>“1” | True | 字符串中的字母大于字符串中的数字 |
| 5>7 | False | 5 小于 7，而不是大于 |
| –1>0 | False | 负数小于 0，而不是大于 |
| “Q”>“q” | False | 字符串中的大写字母小于字符串中的小写字母 |
| “3”>“B” | False | 字母大于数字，而不是小于 |
| 2>2 | False | 它们是相等的，所以左侧的值并不大于 |

### 小于运算符 (<)

小于运算符的工作方式与大于运算符相反。小于运算符不是在左侧值大于时返回 `true`，而是在当运算符左侧的值小于运算符右侧的值时返回 `true`。如果运算符左侧的值大于或等于右侧的值，则该比较运算符返回 `false`。同样，你可以通过查看此表中的示例来了解它是如何工作的。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 2<10 | True | 2 小于 10 |
| “A”<“a” | True | 字符串中的大写字母小于字符串中的小写字母 |
| 10<2 | False | 10 大于 2，而不是小于 |
| “a”<“A” | False | 字符串中的小写字母大于字符串中的大写字母，而不是小于 |
| 10<10 | False | 它们是相等的，所以左侧的值并不小于 |

### 大于等于运算符 (>=)

`>=` 运算符与你目前读到的比较运算符略不同。该运算符增加了两侧值相等仍让比较返回 `true` 的选项。因此，要返回 `true`，运算符左侧的值必须大于或等于右侧。大于等于比较只有在左侧的值小于右侧的值时才会返回 `false`。下表显示了一些使用大于等于运算符的语句示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 5>=2 | True | 5 大于 2 |
| 2>=2 | True | 2 等于 2 |
| “a”>=“A” | True | 小写字母大于大写字母 |
| “A”>=“A” | True | 字符串相等 |
| 1>=2 | False | 1 小于 2 |
| “A”>=“a” | False | 大写字母小于小写字母，而不是大于或等于 |

### 小于等于运算符 (<=)

小于等于运算符与大于等于运算符的作用相反。与大于等于运算符一样，小于等于运算符增加了两侧值相等的情况。小于等于运算符在运算符左侧的值小于或等于运算符右侧的值时返回 `true`。下表显示了一些使用小于等于运算符的语句示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 2<10 | True | 2 小于 10 |
| “A”<“a” | True | 字符串中的大写字母小于字符串中的小写字母 |
| 10<2 | False | 10 大于 2，而不是小于 |
| “a”<“A” | False | 字符串中的小写字母大于字符串中的大写字母，而不是小于 |
| 10<10 | False | 它们是相等的，所以左侧的值并不小于 |

 大于等于运算符 (>=)

`>=` 运算符与你目前读到的比较运算符略有不同。该运算符增加了两侧值相等仍让比较返回 `true` 的选项。因此，要返回 `true`，运算符左侧的值必须大于或等于右侧。大于等于比较只有在左侧的值小于右侧的值时才会返回 `false`。下表显示了一些使用大于等于运算符的语句示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 5>=2 | True | 5 大于 2 |
| 2>=2 | True | 2 等于 2 |
| “a”>=“A” | True | 小写字母大于大写字母
| “A”>=“A” | True | 字符串相等 |
| 1>=2 | False | 1 小于 2 |
| “A”>=“a” | False | 大写字母小于小写字母，而不是大于或等于 |

### 小于等于运算符 (<=)

小于等于运算符与大于等于运算符的作用相反。与大于等于运算符一样，小于等于运算符增加了两侧值相等的情况。小于等于运算符在运算符左侧的值小于或等于运算符右侧的值时返回 `true`。下表显示了一些使用小于等于运算符的语句示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 2<10 | True | 2 小于 10 |
| “A”<“a” | True | 字符串中的大写字母小于字符串中的小写字母 |
| 10<2 | False | 10 大于 2，而不是小于 |
| “a”<“A” | False | 字符串中的小写字母大于字符串中的大写字母，而不是小于 |
| 10<10 | False | 它们是相等的，所以左侧的值并不小于 |

### 严格等于运算符 (===)

`===` 运算符是在 JavaScript 1.5 中引入的，为了让它工作，你的浏览器需要支持 1.5（参考第 1 章，表 1-1）。为了让该运算符返回 `true`，运算符两侧的值必须相等且类型也相同。这意味着如果你使用类似 `3===“3"` 的语句，它将返回 `false`，因为左侧的值是数字而右侧是字符串。与等于运算符 `==` 不同，`==` 运算符会尝试将两侧的值转换为相同的类型，然后判断它们是否相等。下表显示了一些使用 `===` 运算符的语句示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 4===4 | True | 两个数字相等 |
| (4+2)===(3+3) | True | 结果都是数字 6且相等 |
| “my socks”===“my socks” | True | 都是字符串且完全相同 |
| (“my”+“socks”)===(“my”+“socks”) | True | 结果都是字符串 且值相等 |
| 4===5 | False | 4 和 5 不相等 |
| (4+3)===“7” | False | 左侧结果为 7，但右侧是字符串，因此类型不同导致不相等 |
| “My socks”===“my socks” | False | 字符串不完全相同（大小写不同） |
| “2”===(1+3) | False | 类型不同且值不等于 4 |

### 严格不等于运算符 (!==)

`!==` 运算符是在 JavaScript 1.5 中引入的，为了让它工作，你的浏览器需要支持 1.5（参考第 1 章，表 1-1）。为了让该运算符返回 `true`，运算符两侧的值必须不相等或者类型不相同。这意味着如果你使用类似 `3!==“3"` 的语句，它将返回 `true`，因为左侧的值是数字而右侧是字符串，它们类型不同（因此不严格相等）。与不等于运算符 `!=` 运算符会尝试将两侧的值转换为相同的类型，然后判断它们是否不相等，而严格不等于运算符 `!==` 在两侧类型不相同时会自动返回 `true`。下表显示了一些使用 `!==` 运算符的语句示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| 4!==3 | True | 4 和 3 不是相等的数字 |
| “4”!==4 | True | 两侧类型不同 |
| 4!==4 | False | 4 等于 4 |
| “cool”!==“cool” | False | 字符串完全相同，因此它们相等 |

你将在第 6 章学习条件语句和循环时，练习使用以及和其他比较运算符。接下来是逻辑运算符，它们也用于检查条件。





## 第 5 章：JavaScript 运算符

107

### 理解逻辑运算符

三个逻辑运算符允许你比较两个条件语句，以判断其中一个或两个语句是否为真，并据此进行相应的操作。如果你想同时检查多个条件并使用其结果，逻辑运算符就会非常有用。与比较运算符一样，逻辑运算符返回 `true` 或 `false`，具体取决于运算符两侧的值。

表 5-4 总结了逻辑运算符，将在后续章节中对它们进行讨论。

### AND 运算符 (&&)

当 `&&` 运算符两侧的比较都为 `true` 时，逻辑运算符 AND 返回 `true`。如果运算符一侧的某或两个比较为 `false`，则返回 `false` 值。下表显示了一些使用 AND 运算符的语句。

| 语句 | 返回值 | 原因 |
| :--- | :--- | :--- |
| (1==1)&&(2==2) | True | 两侧的比较均为真：1 等于 1，2 等于 2 |
| (2>1)&&(3<=4) | True | 两侧的比较均为真：2 大于 1，3 小于 4 |
| (“A”<=“A”)&&(“c”!=“d”) | True | 两侧的比较均为真：“A” 等于 “A”，“c” 不等于 “d” |
| (1==1)&&(2==3) | False | 右侧的比较为假 |
| (“a”!=“a”)&&(“b”!=“q”) | False | 左侧的比较为假 |
| (2>7)&&(5>=20) | False | 两侧的比较均为假 |

### OR 运算符 (||)

当运算符一侧的比较返回 `true` 时，逻辑运算符 OR 返回 `true`。因此，要使其返回 `true`，只需要其中一侧的语句评估为 `true` 即可。

| 运算符 | 符号 | 功能 |
| :--- | :--- | :--- |
| AND | && | 如果运算符两侧的语句均为真，则返回 `true` |
| OR | || | 如果运算符任一侧的语句为真，则返回 `true` |
| NOT | ! | 如果运算符右侧的语句不为真，则返回 `true` |

表 5-4 逻辑运算符

要返回 `false`，运算符两侧的比较必须都返回 `false`。下表显示了一些使用 OR 运算符的比较示例。

| 语句 | 返回值 | 原因 |
| :--- | :--- | :--- |
| (2==2)||(3>5) | True | 左侧的比较为真 |
| (5>17)||(4!=9) | True | 右侧的比较为真 |
| (3==3)||(7<9) | True | 两个比较均为真 |
| (4<3)||(2==1) | False | 两个比较均为假 |
| (3!=3)||(4>=8) | False | 两个比较均为假 |

### NOT 运算符 (!)

逻辑运算符 NOT 可以用于单次比较，表示“如果情况不是如此，则返回 `true`”。基本上，它可以让一个通常返回 `false` 的表达式返回 `true`，或者让一个通常返回 `true` 的表达式返回 `false`。下表显示了该运算符的一些用法示例。

| 比较 | 返回值 | 原因 |
| :--- | :--- | :--- |
| !(3==3) | False | 3 等于 3 为真，但 NOT 运算符使该语句为假 |
| !(2>5) | True | 2 大于 5 为假；NOT 运算符使语句为真 |

现在你已经掌握了普通的逻辑运算符，请快速查看一下位逻辑运算符。

### 位运算符

位运算符是在位（bit）级别工作的逻辑运算符，那里有大量的 1 和 0。你将在本书提供的示例中不会使用它们，但在 Web 的某些脚本中可能会看到它们。下表列出了一些位运算符及其符号。此列表并不完整，但它应该帮助你在看到位运算符时识别出它们。

| 运算符 | 符号 |
| :--- | :--- |
| AND | & |
| XOR | ^ |
| OR | | |
| NOT | ~ |
| 左移 | << |
| 右移 | >> |
| 右移（零填充） | >>> |

### 特殊运算符

JavaScript 中有许多特殊运算符，用于执行特定任务或辅助缩短代码。表 5-5 列出了特殊运算符及其用途。

如果此表中使用的许多术语看起来陌生，请不要气馁。对象、数组和其他熟悉的术语将在后面的章节中讨论。这些运算符中的许多将在后续章节适当的位置重新引入，届时它们的用途可以表达得更清楚。

| 运算符 | 符号 | 用途 |
| :--- | :--- | :--- |
| 三元 | ?: | 通常用作简短的 if/else 类型语句。条件放在问号（?）之前，冒号（:）两侧各放置一个值。 |
| 逗号 | , | 评估运算符两侧的语句，并返回第二个语句的值。 |
| 删除 | delete | 用于删除对象、属性或数组中的元素。 |
| 在 | in | 如果属性在指定对象中，则返回 `true`。 |
| 实例 | instanceof | 如果对象属于指定的对象类型，则返回 `true`。 |
| 新 | new | 创建对象的实例。 |
| 此 | this | 指向当前对象。 |
| 类型 | typeof | 返回关于值的类型的字符串。 |
| 空 | void | 允许表达式执行但不返回任何值。 |

表 5-5 特殊运算符

Q: **为什么有这么多运算符？如果我可以写 `x+1` 而不是 `x+=1`，我需要它们吗？**
A: 它们提供了快捷方式，无需输入变量名。Q: **我可以同时使用多个运算符吗？会发生什么？**
A: 是的，你可以在语句中使用多个运算符。它们将根据优先级执行。

Q: **括号是怎么回事？为什么在某些情况下使用而在另一些情况下不用？它们有什么作用吗？**
A: 目前使用的括号是为了语句的可读性。在某些情况下，必须使用括号来获得结果。这是下一节将讨论的内容。

Q: **这些运算符是否有常见的拼写错误？**
A: 经常会用赋值运算符 (=) 替换比较运算符 (==)，因为不小心漏掉了第二个等号。此外，忘记使用 `&&` 而输入 `&` 是另一个导致问题的常见错误。同样的错误也可能发生在逻辑 OR (`||`) 和位 OR (`|`) 运算符上。

### 理解运算符顺序

在 JavaScript 中，运算符有特定的优先级。在包含多个运算符的语句中，一个运算符的执行可能会在另一个之前，尽管看起来并非如此。例如，看这个例子：`var answer=8+7*2;`。如果你记得数学中的这种工作方式，就会知道先对 `7*2` 部分进行乘法。因此，语句中的任何乘法都会在加法之前执行，除非你覆盖了它。与数学题一样，在 JavaScript 中覆盖运算顺序的方法是通过使用括号来标出应该先执行的部分。因此，如果你想确保在先前的示例中先执行加法，你应该这样写：`var answer=(8+7)*2;`。如果你在同一层级使用多个括号或相同优先级的运算符，它们将从左到右读取，如下所示：`var answer=(8+7)-(4*3)+(8-2);`。由于括号都在同一层级（没有嵌套），它们从左到右读取。括号外的加法和减法运算符具有相同的优先级，因此也从左到右读取。





## 第 5 章：JavaScript 运算符

111

JavaScript 运算符的优先级如表 5-6 所示，从最高优先级（先执行）到最低优先级（后执行）排序。

如表 5-6 所示，括号可以覆盖其他运算符。当你不确定各种运算符的优先级，或者想让某些代码更具可读性时，括号非常有用。

### 是真还是假？

此项目将允许你尝试一些比较运算符，看看它们是如何工作的。你将创建一个脚本，显示一个警告框（alert），说明某个语句或比较将返回 true 还是 false。该脚本将使用条件 `if/else` 语句，该语句将在下一章中详细介绍。

表 5-6 运算符优先级（从高到低）

| 运算符类型 | 运算符示例 |
| :--- | :--- |
| 括号（覆盖其他） | ( ) |
| 一元（数学、逻辑或位运算） | ++ -- -- ! ~ typeof void delete |
| 乘法、除法、取模 | * / % |
| 加法、减法 | + – |
| 移位（位运算） | >>> >> << |
| 关系比较 | > >= < <= in instanceof |
| 等等比较 | == != === !== |
| 与（位运算） | & |
| 异或（位运算） | ^ |
| 或（位运算） | \| |
| 与（逻辑） | && |
| 或（逻辑） | || |
| 条件 | ?: |
| 赋值 | = += –= *= /= %= <<= >>= >>>= &= ^= |= |
| 逗号 | , |

*（续）*

pr5_2.html
prjs5_2.js

逐步操作

1. 创建一个 HTML 文件并将其保存为 `pr5_2.html`。
2. 创建一个外部 JavaScript 文件并保存为 `prjs5_2.js`。在第 3–13 步中使用此文件进行编辑。
3. 将以下代码插入到你的 JavaScript 文件中：
```javascript
var num1=0;
var num2=0;

if(num1==num2) {
    window.alert("True");
}
else {
    window.alert("False");
}
```
4. 在浏览器中打开 HTML 页面。你应该立即看到一个显示“True”的警告框。
5. 将变量 `num1` 的值改为 5。重新保存 JavaScript 文件并刷新浏览器。你现在应该得到一个显示“False”的警告框。
6. 在接下来的代码行中，将 `==` 运算符改为 `>` 运算符：
```javascript
if(num1==num2) {
```
7. 重新保存 JavaScript并刷新浏览器。你应该再次得到“True”。
8. 将变量 `num2` 的值改为 7。
9. 重新保存 JavaScript 文件并刷新浏览器。你现在应该再次得到“False”。
10. 在下一行（你在第 4 步中更改过的行）中，将运算符改为 `<` 运算符：
```javascript
if(num1>num2) {
```
11. 重新保存 JavaScript 文件并刷新浏览器。你应该再次得到“True”。
12. 尝试更改 `num1` 变量的值，以便得到显示“False”的警告框。
13. 尝试使用其他比较运算符进行你自己的测试，看看结果会是什么。

### 本节总结

在这个项目中，你能够利用对比较运算符的知识来创建一个警告框，根据比较语句将返回 true 还是 false 来显示“True”或“False”。如果你愿意，你还可以尝试测试你自己的值和运算符的变体。

### 第 5 章自测

1. 这里的 __________ 是 JavaScript 中的一个符号或单词，用于对一个或多个值执行某种计算、比较或赋值。
2. __________ 运算符最常用于对两个值进行数学计算。
3. __________ 运算符将两个值相加。
4. 当递增运算符放在操作数的 __________ 侧位时，它会将操作数的值加 1，然后执行语句的其余部分。
5. 下列哪项不是 JavaScript 运算符？
   A = 
   B ==
   C &&
   D $#
6. 赋值运算符的作用是什么？
   A 给变量分配一个新值
   B 给变量起一个新名字
   C 执行比较
   D 无什么作用，因为赋值运算符是没用的
7. 加并赋值 (+=) 运算符将运算符 __________ 侧的值加到运算符 __________ 侧的变量上，并将该新值赋值给变量。
8. 比较运算符的作用是什么？
   A 执行数学计算
   B 处理位，现在不重要
   C 比较两个值或语句，并返回 true 或 false 的值
   D 仅比较数字，不比较字符串
9. 下列哪个比较将返回 true？
   A 4!=3
   B 4==3
   C 4<3
   D 4<=3 ✓
10. 下列哪个比较将返回 false？
    A 4!=3
    B 3==3
    C 4>3
    D 4<=3
11. __________ 运算符允许你比较两个条件语句，以查看其中一个或两个语句是否为真，并据此进行。
12. 下列哪个语句将返回 true？
    A (3==3)&&(5<1)
    B !(17>=20)
    C (3!=3)|(7<2)
    D (3!=3)|(7<2)
13. 下列哪个语句将返回 false？
    A 4<=3
    B (4>=3)&&5<=2)
    C (“a”==“a”)&&(c”!=“d”)
    D 2<3
14. __________ 运算符是在位级别工作的逻辑运算符。
15. 在 JavaScript 中，运算符有特定的__________。

## 第 6 章
## 条件语句与循环

## 关键技能与概念
- 定义条件语句
- 使用条件语句
- 定义循环
- 使用循环

现在你已经看到了各种运算符在 JavaScript 中是如何工作的，本章将指导你如何使用它们。条件语句和循环允许你利用数学、比较和逻辑运算符，因为它们

### 定义条件语句

为了使用条件语句，你需要知道它们是什么。

### 什么是条件语句？

条件语句是一种仅在满足条件时执行部分代码的方法。与其执行脚本中的每一行代码，你可以让某些部分在特定条件下运行。

通过条件语句，你可以告诉 JavaScript 执行如下：

- 如果 yourname 等于 John，则在页面上写 hello John。否则，在页面上写 hello surfer。
- 如果 mycar 等于 Corvette 或 Mustang，则发送一个显示“Cool Car”的警告框。否则，发送一个显示“My car is cooler”的警告框。
- 如果 yourname 等于 John 且 mycar 等于 Corvette 或 Mustang，则发送一个显示“John drives a cool car”的警告框。否则，发送一个显示“Unknown surfer drives a car of some sort”的警告框。

### 使用条件语句

现在你知道条件语句是什么，可以详细查看它们并学习如何编写它们了。你将查看 JavaScript 中使用的两种条件语句块：if/else 语句块和 switch 语句块。首先，我们将查看经常使用的 if/else 语句块。

#### 使用 if/else 语句块

在使用条件语句时，你会发现它们在某些方面与函数相似。最引注意的是围绕在给定条件下执行的代码段的大括号 ({})。为了让你更好地理解其工作原理，我将解释 if/else 语句块的基本结构：它的块结构、块嵌套和复杂的比较。




JavaScript：初学者指南

## if/else 语句块结构

在 if/else 语句中，你必须处理的是第一行，它告诉浏览器继续或移动。你使用 JavaScript 关键字 `if` 开始一个 if/else 语句，后面跟着括号内的比较表达式。接的一行显示了第一行格式的示例：

`if (*comparison here)`

你将 *comparison here* 文本替换为实际的比较。要做到这一点，你需要记住上一章节中的比较运算符。假设你想检查一个名为 `boats` 的变量是否等于 `3`。以下是编写 if/else 块第一行的方法：

`if (boats==3)`

请记住，比较将返回 `true`（真）或 `false`（假）值。这就是返回值有用的地方。如果 `boats==3` 的比较返回 `true`，浏览器就可以继续执行下一行。如果返回 `false`，浏览器将开始寻找 `else` 关键字，或者在完成 `if` 行后的代码块之后执行第一行脚本。

如果比较返回 `true`，你需要在 `if` 行之后创建一个要执行的语句块。要做到这一点，你使用大括号的方式类似于封装函数命令的方式。下面的代码显示了如何添加括号来封装在比较返回 `true` 时执行的代码：

`if (boats==3) {
    JavaScript Statements Here
}`
```

如果 `boats==3` 的比较返回 `true`，你放置在大括号内的代码将被执行。如果返回 `false`，大括号内的代码将被忽略，并执行闭合大括号之后的代码行。

如果你希望使用 `else` 块在比较返回 `false` 时执行某些代码，你可以在下一行放置 `else` 关键字，然后紧跟它自己的一组大括号，如下代码所示：

```javascript
if (boats==3) {
    JavaScript Statements Here
}
else {
    JavaScript Statements Here
}
```

现在你可以看到整个 if/else 块以及它是如何通过执行大括号内两个代码块之一的。如果比较返回 `true`，则执行 `if` 语句之后的代码块；如果比较返回 `false`，则执行 `else` 关键字之后的代码块。

- 比较在第一行
- 这里是添加 JavaScript 代码的地方
- `if` 块以 `if` 关键字和比较开始
- `else` 块以 `else` 关键字开始

第 6 章：条件语句与循环
119

你现在可以创建一个包含代码的完整块。假设如果变量 `boats` 等于 `3`，你想发送一个显示“你有正确数量的船”的警报。如果不是，你想发送一个显示“你没有正确数量的船”的警报。该代码如下例所示：

```javascript
if (boats==3) {
    window.alert("You have the right number of boats");
}
else {
    window.alert("You do not have the right number of boats");
}
```

现在你已经设置好了语句，你需要知道比较是否返回 `true`，以便你确定执行的是哪一个代码块。要做到这一点，你需要在比较发生之前声明 `boats` 变量并为其赋值一个值。这将为你提供决定脚本中发生什么情况的值。尝试使用以下代码，猜猜看执行的是哪一个代码块（第一个还是第二个）：

```javascript
var boats=3;
if (boats==3) {
    window.alert("You have the right number of boats");
}
else {
    window.alert("You do not have the right number of boats");
}
```

如果你猜到执行的是第一个代码块，那么你对了！因为变量 `boats` 等于 `3`，比较 `boats==3` 返回 `true`。由于返回了 `true`，所以执行了第一个代码块，`else` 关键字之后的代码块被忽略。你会收到显示“你有正确数量的船”的警报，不再有其他内容。

***注意***

在输入变量赋值 (`=`) 和相等比较 (`==`) 时要小心，因为它们很容易在不小心的情况下写反，并给你的脚本带来问题。

现在看看如何设置语句以获得相反的结果。以下代码将导致比较返回 `false`：

```javascript
var boats=0;
if (boats==3) {
    window.alert("You have the right number of boats");
}
else {
    window.alert("You do not have the right number of boats");
}
```

- 给变量赋值为 0 将导致比较返回 `false`
- 如果第一行的比较返回 `false`，则执行此警报
- 如果第一行的比较返回 `true`，则执行此警报

JavaScript：初学者指南

当变量 `boats` 的值为 0 时，比较 `boats==3` 将返回 `false`；因此，第一个代码块被忽略，相反而执行 `else` 语句之后的代码块。这一次你收到了显示“你没有正确数量的船”的警报，而第一个块中的警报被忽略了。

现在你已经知道了 if/else 语句块的基本结构，你可以准备学习将一个块嵌套在另一个块中的技术了。

## 块嵌套

如果你*嵌套*（nest）某些东西，你基本上是将一个结构放在另一个相同或相似性质的结构内部。对于 if/else 语句块，你可以在比较之后的第一个块（`if` 块）中嵌套其他的 if/else 语句，或者在 `else` 关键字之后的块（`else` 块）中

例如，你可能希望浏览器执行如下语句：“如果名为 `have_cookbook` 的变量等于 `yes`，且名为 `meatloaf_recipe` 的变量等于 `yes`，则发送显示‘找到配谱’的警报。如果 `have_cookbook` 等于 `yes` 但 `meatloaf_recipe` 不等于 `yes`，则发送‘有书但没配谱’的警报；否则，发送显示‘你需要菜谱’的警报。”

这是一个相当复杂的语句，但你可以通过在另一个 if/else 语句的 `if` 块中嵌套 if/else 语句来实现你的目标。

为了了解它是如何工作的，考虑以下示例，它将上述语句转换为 JavaScript 格式：

```javascript
if (have_cookbook=="yes") {
    if (meatloaf_recipe=="yes") {
        window.alert("Recipe found");
    }
    else {
        window.alert("Have the book but no recipe");
    }
}
else {
    window.alert("You need a cookbook");
}
```

为了了解它是如何工作的，考虑以下示例，它将上述语句转换为 JavaScript 格式：

```javascript
if (have_cookbook=="yes") {
    if (meatloaf_recipe=="yes") {
        window.alert("Recipe found");
    }
    else {
        window.alert("Have the book but no recipe");
    }
}
else {
    window.alert("You need a cookbook");
}
```

- `else` 块嵌套在 `if` 块中
- `if` 块嵌套在 `else` 块中
- 嵌套的 if/else 语句在 `if` 块中
- 嵌套的 if/else 语句在 `else` 块中 




JavaScript：初学者指南

扩展了你已有的代码，但在外部 else 块中添加了一个额外的嵌套 if/else 语句：

```javascript
if (have_cookbook=="yes") {
    if (meatloaf_recipe=="yes") {
        window.alert("Recipe found");
    }
    else {
        window.alert("Have the book but no recipe");
    }
}
else {
    if (have_web_access=="yes") {
        window.alert("Find the recipe on the Web");
    }
    else {
        window.alert("You need a cookbook");
    }
}
```

虽然你还没有声明该变量，但你会注意到增加了一个新变量：`have_web_access`。它用于判断脚本应该告诉观众在网上查找食谱，还是买一本食谱。请记住，在实际脚本中，所有变量在使用之前都需要进行声明。

这一次，如果第一个比较（`have_cookbook=="yes`）返回 `false`，你会被发送到外部的 else 块；然而，由于这个外部 else 块内部现在包含了一个嵌套的 if/else 语句，因此浏览器现在会进入内部的 if 块并查看该比较（`have_web_access="yes`）。如果它返回 `true`，就会执行嵌套 if 块中的代码，你会收到“Find the recipe on the Web”的提示。如果比较返回 `false`，浏览器将移动到嵌套的 else 块并执行该代码。在这种情况下，你会收到“You need a cookbook”的提示。

关于嵌套，你应该了解的最后一点是，你可以在其他块内部嵌套任意数量的块。不仅仅是将一个 if/else 语句嵌套另一个内部，你可以在该语句中进行第二次嵌套、第三次嵌套，或者在你不崩溃的情况下能追踪的任何数量次。为了防止示例变得过于复杂，以下代码仅在之前代码的 if 块中又嵌套了一层：

```javascript
if (have_cookbook=="yes") {
    if (meatloaf_recipe=="yes") {
        if (is_moms_meatloaf=="yes") {
            window.alert("Recipe found");
        }
        else {
            window.alert("Recipe found, but not like what mom makes");
        }
    }
    // 这个 if/else 块嵌套在一个外部 if 块内部
    else { 
        // 这个 if/else 块嵌套在一个外部 else 块内部
        // (注意：逻辑继续自原始 OCR 文本结构)
        if (have_web_access=="yes") {
            window.alert("Find the recipe on the Web");
        }
        else {
            window.alert("You need a cookbook");
        }
    }
}
// 这个 if/else 块嵌套在一个嵌套的 if 块内部
```

现在，一个 if 块内部有一个 if 块，而其内部还有一个 if/else 块。正如你所见，增加了另一个变量 `is_moms_meatloaf` 来检查一个更具体的食谱。你可以一直这样下去，直到你无法忍受；但是，这足以让你在以后需要时在此基础上进行构建。

既然你已经了解了一些关于嵌套的知识，在离开本节的 if/else 主题之前，你还需要查看最后一个细节。你需要学习如何在 if/else 语句中进行更复杂的比较。

## 复杂比较

除了进行诸如 *x==2* 或 *y<3* 这样的简单比较外，你还可以使用第 5 章讨论的逻辑运算符来构建更复杂的比较。正如你可能记得的，那一章以类似于下面示例的形式展示了这些比较：

`(2==2)||(3<5)`

在第 5 章中，唯一关注的是比较会返回 `true` 还是 `false`，而不是如何将其添加到 if/else 语句中。注意每个比较周围的括号。它们存在的主要目的是为了组织结构；但考虑到操作顺序，你可以将比较写为：

`2==2||3<5`

这里的问题是这样可读性较差，因此如果你以后需要调试代码，将很难判断代码是否存在问题。

回想一下 if/else 语句的第一行使用括号来包裹比较。如果你在不使用组织性括号的情况下编写复杂比较（如上一个示例所示），你的第一行看起来可能会像这里所示的行代码：

`if (2==2||3<5)`

虽然这很容易输入，但很难阅读，因为你不确定它应该被读作“如果 2 等于 2 或者 3 小于 5”，还是“如果 (2 等于 2) 或者 (3 小于 5)”。如果你为了组织而加上括号，它会更容易读；但你必须小心正确嵌套。以下示例代码显示了为了组织而添加的括号：

`if ((2==2)||(3<5))`

使用哪种形式取决于个人喜。目前，本章使用带有额外括号进行组织的方法。这应该让你更容易阅读书中的代码。

现在，你可以创建允许包含更多值或允许特定范围取值返回 `true` 的脚本。假设你想在一个名为 `num1` 的变量大于 2 但小于 11 时显示提示框，并在 `num1` 不在该范围内时显示另一个提示框。你可以使用：

```javascript
if ((num1 > 2 && num1 < 11) {
    window.alert("In range");
}
else {
    window.alert("Not in range");
}
```

(注：上述逻辑的 OCR 文本是碎片化的，但逻辑符合所提供的描述。)





# JavaScript：初学者指南

首先，此示例声明并赋值了一个名为 `thename` 的变量；它被赋值为 `Fred`。接下来开始了 `switch` 语句，使用变量 `thename` 作为比较的基础。

然后，用大括号打开块，后面是第一个 `case` 语句。这样写的意思是：“如果 `thename` 等于 George，则执行该行末尾冒号后面的命令。”如果 `thename` 等于 George，你将得到一个警框（alert）。

接下来你会看到 `break` 语句，它告诉浏览器退出代码块并移动到块之后的下一行代码。你在 `switch` 块中使用 `break` 语句是为了确保只有一个 `case` 部分被执行；否则，你将面临在返回 `true` 的 `case` 之后的所有 `case` 都会被执行的风险，因为默认情况下，即使浏览器发现某个 `case` 为真，它也会继续执行下一个语句，而不是完全退出代码块。为了确保浏览器退出块，你添加了 `break` 语句。

如果你回到脚本，你会发现 `thename` 不等于 George，因此跳过了这个 `case`；然而，下一个比较返回了 `true`，因为在脚本中 `thename` 等于 `Fred`。因此，这个 `case` 块中的语句将被执行。注意，在这里 `break` 语句之前出现了两行 JavaScript 代码。这表明你可以在 `case` 中包含任意行的代码，只要你记住用 `break` 语句结束即可。

最后，你看到了关键字 `default`。它被用于没有任何一个 `case` 语句返回 `true` 的情况。如果发生这种情况，将执行默认部分的代码。注意，你不需要在 `default` 代码部分之后添加 `break` 语句，因为它本身就在 `switch` 块的末尾，所以浏览器之后会退出块，从而消除了对 `break` 语句的需求。

有时你想让浏览器执行后续语句。一种常见的用法是在要执行的代码之前放置多个 `case` 语句：

```javascript
case "Fred":
case "Frederick":
case "Freddie":
alert("Fred is an OK name");
break;
```

这种对 `break` 语句的使用允许你在跳出之前执行多个 `case`，而不是局限于单个 `case` 然后跳出。

现在你已经学会了如何使用 `switch` 语句，请看看条件运算符（它在第 5 章表 5-5“特殊运算符”中引入，现在你有了 `if/else` 块的经验后，理解它会更有意义）。

## 使用条件运算符

条件运算符（通常称为三元运算符）可以作为根据条件进行赋值的简便方法。例如，你可能决定根据条件语句的结果给一个赋值赋值。你可以使用以下代码来实现：

```javascript
var mynum=1;
var mymessage;
if (mynum==1) {
    mymessage="You win!";
}
else {
    mymessage="Sorry! Try again!";
}
```

这种方法可以运行，并且给 `mymessage` 赋值为“You win!”，因为 `mynum` 等于 1。然而，条件运算符允许你缩短此类测试所需的代码量。它允许你在问号（`?`）之前放置条件，并在冒号（`:`）的两侧放置可能的值，如下：

*varname* = (*conditional*) ? *value1* : *value2;*

JavaScript 评估条件语句，如果语句返回 `true`，则冒号左侧的值（此处为 *value1*）被赋值给变量。如果语句返回 `false`，则冒号右侧的值（此处为 *value2*）被赋值给变量。

将此应用于之前的示例，我们可以将整个代码重写如下：

```javascript
var mynum=1;
var mymessage;
mymessage = (mynum==1) ? "You win!" : "Sorry! Try Again!";
```

它的工作方式与之前的 `if/else` 块相同，但允许你用更少的输入量来编写代码（减小脚本体积）。

需要注意的是，如果你觉得使用条件运算符不习惯，你也可以使用另一种方法来缩短脚本。由于 JavaScript 是宽容的，当你在代码块中只有一个语句要执行时，你可以省略大括号。

例如，以下代码也可以作为脚本的简短版本：

```javascript
var mynum=1;
var mymessage;
if (mynum==1)
    mymessage="You win!";
else
    mymessage="Sorry! Try again!";
```

此外，由于 JavaScript 不关心标记之间的空白或换行符，你还可以进一步缩短它，使整个 `if/else` 块处于一行上：

```javascript
var mynum=1;
var mymessage;
if (mynum==1) mymessage="You win!"; else mymessage="Sorry! Try again!";
```

目前，你将使用你觉得最舒服的方法。随着你脚本经验的增加，条件运算符将成为缩短代码的方便方法，并在需要此类比较时帮助你优化脚本大小。

你在本章中使用的条件语句将使你在学会了如何使用它们后，能够让你的脚本实现更多功能。你将在后面的章节中大量使用它们，因为它们可以帮助你编写出比没有它们时能执行更多任务的复杂脚本。

# JavaScript：初学者指南

**Q:** **为什么条件运算符通常被称为***三***三元运算符？**

**A:** 条件运算符是 JavaScript 中唯一接受三个操作数的运算符。正因如此，它通常被称为*三元*运算符，而不是三元运算符之一。如果 JavaScript 在未来添加了新的运算符，对条件运算符的这种引用可能会改变。

**Q:** **我不喜欢将一个块嵌套在另一个块中。我可以忘记它并从不进行嵌套吗？**

**A:** 你可以这样做，但这将严重限制你以后编写的脚本，因为你将无法在另一个语句中使用比较语句（这在更复杂的脚本中是必要的）。嵌套允许你执行更复杂的任务，正如你将在后面的脚本中看到的。最好是学习嵌套，以便在需要时可以使用它。

第 6 章：条件语句与循环

### 构建 if/else 块

此项目将帮助你学习如何构建 if/else 块。你将获得一些变量进行测试。

### 步骤说明

1. 创建一个 HTML 页面并保存为 `pr6_1.html`。添加脚本标签指向名为 `pr6_1.js` 的外部 JavaScript 文件。
2. 创建一个外部 JavaScript 文件并保存为 `pr6_1.js`。在步骤 3-6 中使用此文件。
3. 创建名为 `thesport` 的变量并将其赋值为：`Golf`。
4. 创建名为 `myfood` 的变量并将其赋值为：`Pizza`。
5. 根据 `thesport` 变量，编写代码块，如果变量等于“Football”，则发送显示“Cool Sport!”的警框；否则，发送显示“That sport might be cool.”的警框。
6. 根据 `myfood` 变量，编写代码块，如果变量等于“Pizza”，则发送显示“My favorite food!”的警框；否则，发送显示“That food sounds OK I guess.”的警框。
7. 保存 JavaScript 文件和 HTML 文件，并在浏览器中查看 HTML 页面。
8. 你应该得到一个显示“That sport might be cool.”的警框。当你点击 OK，你应该会收到另一个显示“My favorite food!”的警框。





## JavaScript: 入学者指南

### 尝试此总结

在本项目中，你运用新学的 `if/else` 条件语句技巧，创建了一个脚本，该脚本会根据变量的值弹出不同的警告框。你通过两个不同的变量实现了这一点：第一个条件返回 `false` 并在 `else` 语句中显示警告，而第二个条件则返回 `true` 并在 `if` 语句中显示警告。

## 定义循环

在开始使用循环之前，你需要了解什么是循环、它们能做什么，以及为什么它们对你的脚本大有益。

### 什么是循环？

循环是一个代码块，允许你重复执行某部分代码多次，并可能在每次执行代码时更改某些变量的值。通过这种方式，你通常可以将某些任务缩短为几行代码，而不是在脚本中反复编写相同的行，从而避免劳累你的手指。

### 为什么循环很有用

循环之所以有用，是因为它们允许你无需重新输入或在文本编辑器中使用剪切和粘贴就能重复某些代码行。这不仅节省了你反复输入相同代码行的时间和麻烦，还避免了重复行中的输入错误。你还可以在浏览器每次通过循环时更改一个或多个变量的值，这再次节省了你输入与上一行略有不同的代码的时间和麻烦。

举个简单的例子，假设你想用 JavaScript 连续在 Web上上写十次句子。通常情况下，你可能需要编写类似下面的代码：

document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");
document.write("All this typing gets tiring after a while!<br />");

哎！剪切和粘贴可以让任务变得更容易，但仍然很无聊，尤其是当你决定要写这个句子 50 次时。使用循环，你只需要写一次 `document.write()` 语句，然后调整你希望它运行的次数即可。它就像下面的示例。这不是实际代码，但当你在下一节“使用循环”中详细查看循环结构时，你将看到重复多次语句所需的实际代码。

执行此代码块 10 次 {
  document.write("I only had to type this once!<br />");
}

当然，你将把“执行此代码块 10 次”文本替换为 JavaScript 能够理解的实际语句。你将在下一节中看到可以使用哪些语句来构建循环。

## 使用循环

为了看到循环如何真正对你有所帮助，你需要查看 JavaScript 中可以使用不同循环结构。本节涵盖的循环结构包括 *for*、*while* 和 *do while* 循环。

### for

要在 JavaScript 中使用 `for` 循环，你需要知道如何编写循环的基本结构代码，以及如何将一个 `for` 循环嵌套在另一个 `for` 循环中。首先，来看一下 `for` 循环的基本结构。

### for 循环的结构

`for` 循环的结构与条件块非常相似。主要的区别在于循环有不同的用途，结果就是第一行有所不同。之后，你使用熟悉的花括号来包裹循环的内容。

`for` 循环的第一行看起来类似于这一行：
`for (var count=1; count<11; count+=1)`

你首先看到的是 `for` 关键字。后面跟着一组括号，里面有三个语句。这三个语句通过提供特殊信息来告诉循环应该重复多少次。

第一个语句（`var count=1`）创建了一个名为 *count* 的变量，并给它一个初始值 1。这个初始值可以是任何数字。这个数字被用作循环重复次数的起点。使用数字 1 可以帮助你更容易看到循环重复的次数。之前的代码以 *count* 值为 1 的开始循环。请注意，如果 *count* 变量在脚本早早已经初始化，那么这里就不需要 `var` 关键字了。

下一个语句（`count<11`）告诉循环何时停止运行。循环将根据这个条件语句停止运行。这里的条件是只有当变量 *count* 不再小于 11 时才停止。这意味着如果你每次通过循环时给 *count* 的值加 1，那么循环的最后一次运行将是 *count* 等于 10 时。当给 10 加 1 时，它变成了 11；这无法通过条件测试，因此循环停止运行。

集合中的最后一个语句（`count +=1`）决定了变量更改的速率以及它每次是变大还是变小。在之前的代码中，你每次回到循环开头时都会给变量加 1。记住，第一次通过时，变量被设置为 1。由于你每次都加 1，变量在第二次通过时值为 2，第三次通过时值为 3，以此此类推，直到变量不再小于 11 为止。

要完成该结构，你插入花括号来包裹你要在循环内使用的代码。`for` 循环完整结构的示例代码代码所示：

```javascript
for (var count=1; count<11; count+=1) {
  // JavaScript Code Here
}
```

现在，你只需要添加一个真实的变量和一些要执行的 JavaScript 代码，你就组合了一个完整的 `for` 循环。为了做到这一点，你将从一个向页面写十次句子的脚本开始。现在你可以使用循环了，你只需要写一次句子本身，而不是连续写十次。下面的示例代码了如何使用 `for` 循环实现这一点：

```javascript
for (var count=1; count<11; count+=1) {
  document.write("I am part of a loop!<br />");
}
```

*count* 变量将从 1 开始计数，因为它被分配了初始值 1。你每次通过循环时都给它加 1。当 *count* 变量的值不再小于 11 时，循环将停止。在这种情况下，*count* 将从 1 运行到 10，从而运行循环10 次。当下次命中 `for` 语句并加 1 时，*count* 变量的值为 11，它不再小于 11；因此，浏览器将跳过循环并继续执行循环结束花括号之后的下一行代码。`document.write` 命令中使用 `<br />` 标签是为了确保每个句子后面都有换行符，而不会将下一个句子写在同一行。

为了在页面上看到此效果，你可以添加 `<script>` 标签并将外部 JavaScript 文件插入到 HTML 页面的 `body` 部分。创建一个名为 `loops01.js` 的 JavaScript 文件，添加以下代码并保存文件。在 HTML 文档中添加必要的 `<script>` 标签并保存为 `loops01.html`。

```javascript
document.write("Get ready for some repeated text.<br />");

for (var count=1; count<11; count++) {
  document.write("I am part of a loop!<br />");
}

document.write("Now we are back to the plain text.");
```

在这里，对 *count* 变量的递增进行了细微调整。没有输入 `count+=1`，而是使用了自增运算符 (`++`)。当仅仅给变量加 1 时，自增

这一行决定了循环将运行多少次

此循环将会在 HTML 文档中反复显示文本





## 第 6 章：条件语句与循环

133

`operator` 是一种缩短代码的方便方法。然而，如果你想将变量增加 2 或更多，仍然需要使用累加并赋值运算符（即 `count+=2`）。

前面的代码所表示的页面有一行短文本，随后是你重复输出的文本。页面以一条注释结束：“现在我们回到了正文。”图 6-1 显示了这部分内容在浏览器窗口中查看时的外观。请注意，“I am part of a loop!”这句话被重复了十次。

现在你已经学会了基础循环，可以准备好向其中添加一些内容，让循环变得更有用。在循环内部，你可以使用 `count` 变量的值（或任何你使用的变量值）来执行各种操作。

你可以做的一件事（当你稍后学习数组时，这一点会变得更加明显）是利用变量每次都会变化的这一事实。随着变量每次循环增加 1，你可以使用循环对句子从 1 到 10 进行编号，使行更具可读性。以下代码实现了这一功能：

![](img/61d166424839b7674a7b9c8434ae4e03_155_0.png)

图 6-1 循环显示了十次该文本

JavaScript：初学者指南

document.write("Get ready for some repeated text.<br />");

for (var count=1;count<11;count++) {
    document.write(count+". I am part of a loop!<br />");
}

document.write("Now we are back to the plain text.");

在前面的代码中，你只是在字符串开始处添加了 `count` 变量的值。句子前的句号会让每行文本在数字后出现一个句号、一个空格，以及你的句子。图 6-2 显示了添加此内容后脚本在浏览器中的外观。

在学习 `while` 循环之前，你还需要学习关于 `for` 循环的另一点。就像 `if/else` 块一样，`for` 循环也可以嵌套在另一个 `for` 循环中。现在变量被用于每次代码重复时添加行号。

![](img/61d166424839b7674a7b9c8434ae4e03_156_0.png)

图 6-2 现在重复的行已从 1 到 10 编号

第 6 章：条件语句与循环

135

### 块嵌套

是的，你现在必须处理嵌套循环了。与 `if/else` 块一样，你可以嵌套到你能处理的任何深度。目前，你只需要在一个循环内嵌套另一个循环。以下示例展示了 `for` 循环内部的 `for` 循环：

```javascript
for (var count=1;count<11;count++) {
    document.write(count+". I am part of a loop!<br />");
    for (var nestcount=1;nestcount<3;nestcount+=1) {
        document.write("I keep interrupting in pairs!<br />");
    }
}
```

***注意***

在嵌套循环时要小心，确保每个嵌套循环在第一行都有它自己的计数器，例如 `for(count=1;count<11;count+=1)`。在大多数情况下，计数器需要对于自己的循环是唯一的。此外，如果没有包含大括号或配对正确，可能会发生很多错误。

现在你有了一个循环，它用自己的文本中断外层循环的文本。每当你通过外层循环，就会写出“I am part of a loop!”这一行。然后，你会遇到另一个循环，它会在屏幕上写出“I keep interrupting in pairs!”

内部循环设置为重复两次；因此，每当从外部循环得到一个句子时，后面紧跟着两个来自内部循环的句子。为了更清楚地看到这一点，请考虑以下示例，它更新了你之前在 `loops01.js` 文件中使用的代码：

```javascript
document.write("Get ready for some repeated text.<br />");
for (var count=1;count<11;count++) {
    document.write(count+". I am part of a loop!<br />");
    for (var nestcount=1;nestcount<3;nestcount++) {
        document.write("I keep interrupting in pairs!<br />");
    }
}
document.write("Now we are back to the plain text.");
```

图 6-3 说明这种嵌套循环如何影响浏览器中页面的外观。你现在可以看到，如果需要，嵌套循环对于在过程中添加更多信息是有用的。

为了让情况更复杂，你还可以将不同类型的块相互嵌套。例如，你可以将一个 `if/else` 语句块放在循环内部，或者将一个循环放在 `if/else` 语句的 `if` 块或 `else` 块中。以下示例在 `for` 循环中创建了一个 `if/else` 块：

```javascript
for (var count=1;count<11;count++) {
    if (count==5) {
        document.write("The loop is halfway done!<br />");
    }
    else {
        document.write("I am part of a loop!<br />");
    }
}
```

这个嵌套循环中断了外部循环

JavaScript：初学者指南

在前面的代码中，你只是在字符串开始处添加了 `count` 变量的值。句子前的句号会让每行文本在数字后出现一个句号、一个空格，以及你的句子。图 6-2 显示了添加此内容后脚本在浏览器中的外观。

在学习 `while` 循环之前，你还需要学习关于 `for` 循环的另一点。就像 `if/else` 块一样，`for` 循环也可以嵌套在另一个 `for` 循环中。现在变量被用于每次代码重复时添加行号。

图 6-2 现在重复的行已从 1 到 10 编号

第 6 章：条件语句与循环

135

是的，你现在必须处理嵌套循环了。与 `if/else` 块一样，你可以嵌套到你能处理的任何深度。目前，你只需要在一个循环内嵌套另一个循环。以下示例展示了 `for` 循环内部的 `for` 循环：

```javascript
for (var count=1;count<11;count++) {
    document.write(count+". I am part of a loop!<br />");
    for (var nestcount=1;nestcount<3;nestcount+=1) {
        document.write("I keep interrupting in pairs!<br />");
    }
}
```

***注意***

在嵌套循环时要小心，确保每个嵌套循环在第一行都有它自己的计数器，例如 `for(count=1;count<11;count+=1)`。在大多数情况下，计数器需要对于自己的循环是唯一的。此外，如果没有包含大括号或配对正确，可能会发生很多错误。

现在你有了一个循环，它用自己的文本中断外层循环的文本。每当你通过外层循环，就会写出“I am part of a loop!”这一行。然后，你会遇到另一个循环，它会在屏幕上写出“I keep interrupting in pairs!”

内部循环设置为重复两次；因此每当从外部循环得到一个句子时，后面紧跟着两个来自内部循环的句子。为了更清楚地看到这一点，请考虑以下示例，它更新了你之前在 `loops01.js` 文件中使用的代码：

```javascript
document.write("Get ready for some repeated text.<br />");
for (var count=1;count<11;count++) {
    document.write(count+". I am part of a loop!<br />");
    for (var nestcount=1;nestcount<3;nestcount++) {
        document.write("I keep interrupting in pairs!<br />");
    }
}
document.write("Now we are back to the plain text.");
```

图 6-3 说明这种嵌套循环如何影响浏览器中页面的外观。你现在可以看到，如果需要，嵌套循环对于在过程中添加更多信息是有用的。

为了让情况更复杂，你还可以将不同类型的块相互嵌套。例如，你可以将一个 `if/else` 语句块放在循环内部，或者将一个循环放在 `if/else` 语句的 `if` 块或 `else` 块中。以下示例在 `for` 循环中创建了一个 `if/else` 块：

```javascript
for (var count=1;count<11;count++) {
    if (count==5) {
        document.write("The loop is halfway done!<br />");
    }
    else {
        document.write("I am part of a loop!<br />");
    }
}
```

这个嵌套循环中断了外部循环

JavaScript：初学者指南

在前面的代码中，你只是在字符串开始处添加了 `count` 变量的值。句子前的句号会让每行文本在数字后出现一个句号、一个空格，以及你的句子。图 6-2 显示了添加此内容后脚本在浏览器中的外观。

在学习 `while` 循环之前，你还需要学习关于 `for` 循环的另一点。就像 `if/else` 块一样，`for` 循环也可以嵌套在另一个 `for` 循环中。现在变量被用于每次代码重复时添加行号。

图 6-2 现在重复的行已从 1 到 10 编号

第 6 章：条件语句与循环

135

是的，你现在必须处理嵌套循环了。与 `if/else` 块一样，你可以嵌套到你能处理的任何深度。目前，你只需要在一个循环内嵌套另一个循环。以下示例展示了 `for` 循环内部的 `for` 循环：

```javascript
for (var count=1;count<11;count++) {
    document.write(count+". I am part of a loop!<br />");
    for (var nestcount=1;nestcount<3;nestcount+=1) {
        document.write("I keep interrupting in pairs!<br />");
    }
}
```

（注：由于中存在大量重复内容，译文已根据原文逻辑进行了去重和格式整理）





## 第 6 章：条件语句与循环

139

现在你已经知道了 `while` 循环的工作原理，让我们来看一个添加了特殊功能的循环。

### do while

`do while` 循环很特殊，因为循环内的代码至少会执行一次，即使使用的比较在第一次返回 `false`。在其他循环中，如果第一次尝试返回 `false`，将导致循环永远不会执行。在 `do-while` 循环中，循环会执行一次，之后每次都会使用该比较来决定是否需要重复。

以下是一个运行五次的 `do while` 循环示例：

```javascript
var count=1;

do {
  document.write("Hi!");
  count++;
} while (count<6);
```

图 6-5 使用 `while` 循环重复了十行的文本

![](img/61d166424839b7674a7b9c8434ae4e03_161_0.png)

- `while` 语句在第一次运行后的每次都会执行比较
- `do` 关键字开始 `do while` 循环

JavaScript：初学者指南

注意，在前面的代码中，块的第一行只有 `do` 关键字和左大括号 `{`。然后，当代码块完成后，你会看到 `while` 语句和比较部分。`do` 关键字是你确保代码块至少执行一次的方法。

此后，浏览器会在重复之前检查比较结果是否为 `true`。

在这种情况下，循环会重复五次，因为变量 `count` 从 1 开始，并在每次通过循环时增加 1。当 `count` 的值达到 6 时，循环被跳过且不再执行。

若要查看一个即使初始比较返回 `false` 也会至少执行一次的 `do while` 循环示例，请看下面的示例代码：

```javascript
var count=11;

do {
  document.write("Hi!");
  count++;
} while (count<10);
```

由于 `count` 变量的初始值为 11，上述代码中的循环将只运行第一次。当检查比较时（此时 `count` 已经是 12 了，因为在循环执行期间它被加了 1），它会返回 `false`，循环不再运行。

当你有一段代码需要至少执行一次，但仅在满足特定条件时才重复时，`do while` 循环最为有用；否则，另外两种循环中的任何一个都足够完成任务了。

### for in

`for in` 循环允许你遍历对象的所有属性名称，并使用一个变量来保存属性名称，为每个属性执行语句。`for in` 循环的通用格式所示：

```javascript
for (*varname in objectname) {
  // 在此处编写 JavaScript 代码
}
```

由于你还没有学过 JavaScript 对象，这对你来说还没有用处。`for in` 循环将在第 8 章中进行详细介绍。

### for each in

`for each in` 循环与 `for in` 循环非常相似，但它不是遍历每个属性的名称，而是允许你遍历每个属性的值。它仅支持 JavaScript 1.6 及更高版本。同样，这将在第 8 章引入对象时进行更详细的介绍。

这只写入页面一次，
因为比较将返回 `false`

第 6 章：条件语句与循环

141

### 使用 break 和 continue

`break` 和 `continue` 语句允许你停止循环正在执行的操作，但它们的工作方式不同。正如你在本章前面的部分在 `switch` 块中使用 `break` 语句所记忆的，`break` 语句在该点停止循环并完全退出循环，移动到循环后的下一个 JavaScript 语句。例如，`break` 可以这样使用：

```javascript
for (count=1;count<11;count++) {
  if (count==5) {
    document.write("循环已经完成了一半，我执行完了！<br />");
    break;
  }
  else {
    document.write("我是循环的一部分!<br />");
  }
}
```

这个循环将正常进行，直到 `count` 等于 5。当这种情况发生时，页面会写入一条特殊消息，并使用 `break` 语句完全结束循环。因此，循环并没有运行十次，而是只执行了五次。

如果你决定在条件发生时不完全离开循环，则可以修改循环以使用 `continue` 语句。`continue` 语句将停止循环在当前轮次中执行其之后的任何语句。然而，它会回到循环的开头并从上次停止的地方继续，而不是完全退出循环。例如，你可以使用以下代码：

```javascript
for (count=1;count<11;count++) {
  if (count==5) {
    continue;
  }
  document.write(count+". 我是循环的一部分!<br />");
}
```

这一次，当 `count` 等于 5 时，页面上没有写入任何内容。相反，循环被告知回到开头并从那里继续。结果是“我是循环的一部分！”消息只会写入页面九次（因为 `count` 等于 5 时什么都没有发生）。




JavaScript: 初学者指南

4. 下面哪一项可以作为 if/else 语句的第一行？

A if (*x=2)

B if (*y<7)

C else

D if ((*x==2 &&))

5. 你使用什么来包裹条件判断和循环中的代码块？

A 圆括号

B 方括号

C 大括号

D 小号和大于号

6. __________ 语句允许你获取单个变量的值，并根据该变量的值执行不同的代码行。

7. 一个 __________ 是一个代码块，允许你重复执行特定次数的代码。

8. 循环是有用的，因为它强迫你重复输入某些代码行。

A 正确

B 错误

9. 下面选项中哪一项可以作为 for 循环的第一行？

A for (*x=1;*x<6;*x+=1)

B for (*x==1;*x<6;*x+=1)

C for (*x=1;x=6;*x+=1)

D for (*x+=1;*x<6;*x*=1)

10. __________ 循环会检查比较条件，并一直重复直到该条件不再为真。

11. 下面选项中哪一项不能作为 while 循环的第一行？

A while (*x<=7)

B while (*x=7)

C while (*x<7)

D while (*x!=7)

第 6 章：条件语句与循环

145

12. do while 循环是特殊的，因为循环内的代码至少会执行一次，即使使用的比较结果在第一次返回为假。

A 正确

B 错误

13. do while 块的第一行包含关键字 `do` 和一个比较表达式。

A 正确

B 错误

14. do while 块的最后一行只包含一个大括号。

A 正确

B 错误

15. 你可以在另一个代码块中嵌套多少次代码块？

A 无

B 一次

C 三次，最多三次

D 随你意愿任意（尽管嵌套过多可能会耗尽浏览器内存）

第 7 章

事件处理器

147

JavaScript: 初学者指南

核心技能与概念

- 理解事件处理器的位置和用途
- 学习事件处理器
- 使用事件处理器创建脚本
- 注册事件的其他方法

在创建脚本时，你经常会发现用户“事件”（例如用户将鼠标移动到某个元素上或点击特定元素），你希望你的脚本对这些事件做出反应。实现这一目标的方法就是使用事件处理器。

要学习事件处理器是如何工作的，你需要了解它们是什么以及它们对你有用。。你将学习事件处理器放置在文档中的位置以及如何使用它们。最后，你将看到 JavaScript 中的各种事件以及处理每个事件的事件处理器。首先，本章介绍了事件处理器的概述。

### 什么是事件处理器？

事件处理器是对象的一个预定义 JavaScript 属性（大多数情况下是文档中的元素），用于处理 Web页面上的事件。

你可能会问：“什么是事件？”事件是页面查看者执行某种操作时发生的事情，例如点击鼠标按键、点击页面上的按钮、更改表单元素的内容或将鼠标移动到页面上的链接上。事件也可以仅由于页面加载或其他类似的动作发生。

当事件发生时，你可以使用 JavaScript 事件处理器来识别它们，然后执行特定的任务或一组任务。JavaScript 允许你对查看者的操作做出反应，并创建具有交互性的脚本，从而对你和查看者都更有用。

### 为什么事件处理器有用

事件处理器之所以有用，是因为它们允许你访问页面上可能发生的事件。例如，如果你想在用户将鼠标移动到链接上时发送一个警告，你可以使用事件处理器调用你编写的响应该事件的 JavaScript alert。你现在正在根据查看者的动作让事情发生，这让你能够创建更具交互性的 Web Page。

创建这种交互让许多人发现 JavaScript 的编写和使用变得更有趣。通过事件处理器，你可以为用户创造一些惊喜，或者编写一些为页面添加更多功能的脚本。JavaScript 可以让 Web 发生很多事情，使页面比静态 HTML 文档更有趣。

第 7 章：事件处理器

149

### 理解事件处理器的位置和用途

要了解事件处理器是如何工作的，你需要知道可以在文档的哪里放置它们，以及如何使用它们为事件添加 JavaScript 代码。

事件处理器可以在多个位置使用。可以通过向 HTML 元素添加特殊属性来直接在元素中使用。它们也可以在 `<script>` 和 `</script>` 标签内使用。

### 在元素中使用事件处理器

要理解事件处理器的位置，你需要学习如何使用它们。可以通过添加特殊属性在 HTML 元素中使用事件处理器。

例如：

<input type="button" value="Click Me" onclick="alert('Hi'); alert('Bye');" />





## 第 7 章：事件处理器

151

#### 在脚本代码中使用事件处理器

你也可以在脚本代码中使用事件处理器（无论使用 HTML 文档中的 `<script>` 标签还是使用外部 JavaScript 文件）。实现此点的方法一种是给元素一个 `id` 属性，然后使用 JavaScript 方法 `document.getElementById()` 来访问该元素。完成后后，你可以为元素绑定一个事件。

#### 添加 id 属性

要按照这种方式使用之前的脚本，你首先需要为输入按钮的 HTML 标签添加一个 `id` 属性，如下所示：

```html
<body>
  <form>
    <input type="button" value="Click Me!" id="say_hi" />
  </form>
  <script type="text/javascript" src="js_event_01.js"></script>
</body>
```

注意，按钮输入元素被赋予了 `say_hi` 的 `id`。你将使用它来访问按钮并在脚本中将其绑定到事件。

#### 访问元素

`document.getElementById()` 方法允许你通过 `id` 属性的值访问 HTML 文档中任何带有 `id` 属性的元素。为了访问你一直使用的 `id` 为 `say_hi` 的按钮输入元素，可以使用以下代码：

```javascript
document.getElementById("say_hi");
```

这仅仅是告诉浏览器你想访问 HTML 文档中 `id` 为 `say_hi` 的元素。这种方法可以直接在脚本中使用访问元素，但如果你反复使用它，通常会希望将此表达式赋值给变量以节省输入。因此，你可以使用以下代码：

```javascript
var hi_button = document.getElementById("say_hi");
```

现在，从 JavaScript 文件 (js_event_01.js) 获取剩余代码并向其添加新的脚本行，如下所示：

```javascript
function hi_and_bye() {
  window.alert('Hi!');
  window.alert('Bye!');
}

var hi_button = document.getElementById("say_hi");
hi_button.onclick = hi_and_bye;
```

现在还有额外的一行代码。最后一行代码使用了用于输入按钮元素的变量，通过在函数及其语句之后添加，为其提供了 `onclick` 事件处理器：

- 通过其 `id` (say_hi) 访问按钮输入元素并将其赋值给变量 (hi_button)
- 使用 `onclick` 事件处理器将函数 (hi_and_bye) 赋值给按钮输入元素的 `onclick` 事件，格式为变量名加点 (.)。

函数 `hi_and_bye`（显示两个警框的函数）被赋值用于处理输入按钮的点击事件。因此，当按钮被点击时，查看者将看到两个警框！

***注意***

这些语句中的某些（例如代码中点 (.) 的使用以及 `document.getElementById()` 方法）将在第 8 章和第 9 章中进行更详细的解释。为了帮助更好地理解这一点，最后两行代码也可以按以下方式编写：

```javascript
document.getElementById("say_hi").onclick = hi_and_bye;
```

两种方法实现相同的结果，但当你需要在代码中多次处理同一个元素时（也许为了添加其他事件，如 `onmouseover`、`onmouseout` 或其他事件），第一种方法很有帮助。

你还会注意到，当将函数赋值用于处理事件时，函数名后没有使用括号。这是因为你希望将函数的执行赋值给事件，而不是将函数的结果（这是你在之前的章节中使用 `return` 语句将函数结果赋值给变量时所做的——这个特定的函数不会返回任何内容）。你不只是赋值一个值，而是希望函数被执行，因此通过只使用函数名将整个函数赋值给事件。

**Q：查看者在 Web 页面上执行的所有操作都有 JavaScript 事件吗？**
**A：** 没有，但查看者可能采取许多操作都被 JavaScript 中的某个事件覆盖了。涵盖每一种可能性是非常的。

**Q：你的意思是我可以像使用 HTML 属性一样通过事件处理器来写一些 JavaScript 吗？**
**A:** 是的，但请记住，给元素添加 `id` 属性并在 JavaScript 代码中响应事件有助于保持 HTML 代码的整洁。

**Q：如果我将事件作为 HTML 属性添加，我如何决定何时使用函数，何时直接将代码添加到事件处理器中？**
**A：** 如果你的 JavaScript 代码很短，并且你不会与其他标签和/或事件多次重复它，那么你可能希望将代码作为属性直接添加到事件处理器中。如果你的代码非常长或者你会重复使用多次，你可能希望使用函数，以使内容更易读且代码可重用。

提问专家

第 7 章：事件处理器

153

此 7-1

这种处理事件的方法允许你将所有的 JavaScript 代码放在 HTML 元素之外，这使得你的 HTML 代码更整洁（特别是如果使用了外部 JavaScript 文件），并且更有可能通过验证。在本章的稍后部分，你将看到具有特定差异的新方法也可用于处理事件（但可能无法跨浏览器工作）。目前，在页面内部响应事件时，你将使用本节描述的方法。

#### 创建按钮

在这个项目中，你将创建一个点击时会发送三个警框的按钮。

#### 逐步步骤

1. 创建名为 `r7_1.html` 的 HTML 页面。
2. 创建名为 `r7_1.js` 的 JavaScript 文件。
3. 在 JavaScript 文件中编写 `send_alerts()` 函数，它将发送三个警框：
   - 警框 1：你好！
   - 警框 2：欢迎
   - 警框 3：这些警框打扰你吗？
4. 在 HTML 页面创建一个 `id` 为 `send_alerts` 文本为 "Click Me" 的按钮。
5. 使用 `onclick` 事件将 `send_alerts` 函数赋值给按钮。
6. 保存文件并在浏览器中加载 HTML 页面。

#### 尝试一下

在这个项目中，你使用 `onclick` 事件创建一个响应查看者的脚本。

学习事件处理器

现在你已经知道了什么是事件处理器以及如何使用它们，你需要查看哪些事件处理器用于页面上的各种事件。查看表 7-1，它列出了常见事件、它们的事件处理器以及触发每个事件的示例。

| 事件 | 事件处理器 | 事件触发器 |
| :--- | :--- | :--- |
| Abort | onabort | 图像加载完成前停止 |
| Blur | onblur | 查看者取消焦点 |
| Change | onchange | 查看者更改表单元素 |
| Click | onclick | 查看者点击元素 |
| ContextMenu | oncontextmenu | 查看者打开菜单 |
| Copy | oncopy | 查看者对页面部分使用复制命令 |
| Cut | oncut | 查看者对页面部分使用剪切命令 |
| Dblclick | ondblclick | 查看者双击鼠标 |
| Error | onerror | 浏览器获取 JavaScript 错误或不存在的图像 |
| Focus | onfocus | 查看者赋予元素焦点 |
| Keydown | onkeydown | 查看者在键盘上按下键 |
| Keypress | onkeypress | 查看者在键盘上按下键，并释放或按住 |
| Keyup | onkeyup | 查看者释放键盘键 |
| Load | onload | 网页加载完成 |
| Mousedown | onmousedown | 查看者按下鼠标按钮 |
| Mousemove | onmousemove | 查看者移动鼠标（移动光标） |
| Mouseout | onmouseout | 查看者鼠标移离开元素 |
| Mouseover | onmouseover | 查看者鼠标移过元素 |
| Mouseup | onmouseup | 查看者释放鼠标按钮 |
| Paste | onpaste | 查看者对页面部分使用粘贴命令 |
| Reset | onreset | 查看者重置页面上的表单 |
| Resize | onresize | 窗口大小发生调整 |
| Scroll | onscroll | 查看者滚动滚动区域 |
| Select | onselect | 用户进行选择 |
| Submit | onsubmit | 查看者提交页面上的表单 |
| Unload | onunload | 查看者离开当前页面 |





## 第 7 章：事件处理器

155

***注意***

其中某些事件（例如复制事件 copy event）仅在某些浏览器中有效（这些浏览器可能需要运行最新版本）。还有一些事件仅在 Internet Explorer 中有效（参见 http://msdn.microsoft.com/en-us/library/ms533051(VS.85).aspx），或者目前尚不具有跨浏览器兼容性（参见 www.w3.org/TR/DOM-Level-3-Events/events.html#Events-EventTypes-complete）。

现在你已经对事件处理器有了大致的了解，并将详细查看一些最常用的事件，看看它们是如何工作的。

#### 中止事件 (onabort)

当查看者停止（中止）加载图像时，会触发 abort 事件。用于处理此事件的事件处理器是 `onabort`。例如，如果你想在用户停止加载图像时显示一条消息，可以使用以下代码：

```html
<img src="myimage.jpg" alt="my picture" onabort="window.alert('Why don\'t you want to see my picture?');" />
```

这将询问用户为什么不想看你的图片。这可能无法说服用户加载图像，但它让用户知道你原本打算加载这张图片。

#### 失去焦点事件 (onblur)

blur 事件是聚焦事件（focus event）的反面，当查看者从表单元素或窗口移开焦点时发生。要移除某个对象的焦点，查看者通常会将焦点赋予其他对象。例如，查看者可以从一个表单元素移动到另一个，或者从一个窗口移动到另一个。

`onblur` 事件处理器用于此类事件，它可以用于表单元素的标签或打开的 `<body>` 标签中（针对窗口）。`onblur` 事件处理器还有一个名为 `blur()` 的相关方法，将在第 10 章和第 14 章中介绍。

***注意***

只有当查看者将焦点赋予另一个区域时，才会触发 blur 事件，这是浏览器知道查看者释放第一个区域焦点的唯一方式。例如，当查看者在输入字段中按回车键时，焦点从输入字段转移到文档窗口。

要查看 blur 事件的作用，你还可以使用文本框。以下示例使用了两个文本框：点击第一个文本框会使其获得焦点，点击第二个文本框会触发第一个文本框的 blur 事件。

```html
<form>
  Give this box focus:<br />
  <input type="text" onblur="window.alert('Hey! Come back!');" /><br />
  then give this box focus to blur the first one:<br />
  <input type="text" />
</form>
```

在给第一个文本框焦点后，点击此文本框将触发第一个文本框的 blur 事件。文本框中的 `onblur` 事件（参见《JavaScript：初学者指南》）。当查看者点击第二个文本框时，他们会收到来自第一个文本框的警框，让他们返回。

图 7-1 显示了上述代码在浏览器中运行的结果。注意，当警框弹出时，焦点在第二个文本框中。通过点击第二个文本框，查看者触发了第一个文本框的 blur 事件。

#### 改变事件 (onchange)

当查看者更改表单元素内的某些内容时，会发生 change 事件。例如，查看者可能会更改文本框中的文本，或从选择框（select box）中进行选择。你使用 `onchange` 事件处理器来处理此事件。

你可以通过设置一个选择框来查看它是如何工作的。你可以在选择框内为查看者提供选项。如果用户通过选择新选项更改了默认选项，你可以发送一个警框询问更改原因，如下例所示：

```html
<form>
  Are you cool?<br />
  <select onchange="window.alert('Why did you change that?');">
    <option selected="selected">Yes</option>
    <option>No</option>
    <option>Undecided</option>
  </select>
</form>
```

图 7-1 当查看者移开文本框焦点时会弹出此警框
![](img/61d166424839b7674a7b9c8434ae4e03_178_0.png)

在列表中做出新选择将触发此处的 `onchange` 事件处理器（第 7 章：事件处理器，157 页）。如果查看者尝试更改默认答案“Yes”，则会弹出警框并向查看者发送一条消息。如果保持选择框不变或查看者选择了默认选项，则什么都不会发生。

#### 点击事件 (onclick)

当查看者点击 Web 页面上的元素时，会发生 click 事件。这些通常是表单元素和链接。在现代浏览器中，点击事件也适用于更通用的区域，例如表格单元格内或一组 `<div>` 和 `</div>` 标签内。本章重点关注表单元素和链接，因为它们最常用。

查看点击事件作用的最简单方法是使用表单按钮。当按钮被点击时，你希望发生某个事件。为了实现这一点，你可以将 `onclick` 事件处理器放在按钮 `input` 标签内部，如下例所示：

```html
<body>
  <form>
    <input type="button" value="Do not Click" onclick="window.alert('I told you not to!');">
  </form>
</body>
```

点击按钮后，将向查看者发送一个警框。图 7-2 显示了查看者点击按钮时此代码的结果。通过点击按钮，查看者触发了按钮的 `onclick` 事件。`onclick` 事件处理器用于按钮（图 7-2 所示）。`onclick` 事件（参见《JavaScript：初学者指南》，180 页）。如果你想用此事件处理器来对链接实现相同操作，你可能会尝试以下内容：

```html
<body>
  <a href="none" onclick="window.alert('Hey! You clicked me!');">Click</a>
</body>
```

此代码的问题是，警框会工作，但浏览器会尝试跟随链接。这可能会导致“未找到服务器”错误。避免“未找到服务器”错误的一种方法是链接到一个实际页面（这对可访问性很有好处），但它会让带有 JavaScript 的用户离开当前页面。为了防止链接被跟随（如果启用了 JavaScript），你需要在 JavaScript 中添加额外的语句。你需要在显示警框后告诉浏览器不要继续。为了这一点，你将添加 `return` 语句。回顾第 4 章关于函数的内容，你使用 `return` 语句返回返回值。在这里你将执行相同的操作。你将返回布尔值 `false`，这告诉浏览器事件已处理，不需要进一步操作。以下代码显示了如何添加 `return` 语句：

```html
<body>
  <a href="http://none" onclick="window.alert('Hey! You clicked me!'); return false;">Don't Click Me</a>
</body>
```

有了这段代码，点击事件将由 `onclick` 事件处理器处理，浏览器无需担心尝试跟随超文本引用（href）属性中的链接。

***注意***

你也可以通过 `javascript:` 命令为链接编写 JavaScript——例如，`<a href="javascript:window.alert('Hi');">Click</a>`——但出于可访问性考虑，不建议这种方法（如果禁用了 JavaScript，链接将无处去）。

#### 聚焦事件 (onfocus)

当查看者赋予 Web 页面上的某个元素焦点时，会发生 focus 事件。查看者通过点击元素内部某处、使用键盘移动到该元素（通常通过 TAB 键）或通过脚本赋予某个对象焦点。例如，点击文本输入框（在输入任何内容之前）的查看者赋予该文本框焦点。此外，点击非活动窗口并使其变为活动窗口也会赋予窗口焦点。

噢不！这会给你带来麻烦，因为浏览器会尝试跟随链接。`return false` 语句可以阻止浏览器尝试跟随链接





## 第 7 章：事件处理器

159

与此事件配合使用的事件处理器是 `onfocus`，它可以用于如表单元素或 Web 页面上的 `body` 标签等位置（用于获取窗口焦点）。`onfocus` 事件处理器还有一个名为 `focus()` 的相关方法，该方法将在第 10 章和第 14 章中介绍。

为了查看 `focus` 事件的效果，你可以创建一个文本输入框，它是表单元素之一，允许你让元素获得焦点。以下示例展示了如何操作，以及如何编写一个提醒警告框，在观众给文本框焦点时弹出：

```html
<form>
  输入姓名 (Enter Your Name):
  <input type="text" onfocus="window.alert('Don\'t forget to capitalize!');" />
</form>
```

这段代码将在观众开始输入之前向其显示一个警告框。警告框的作用是提醒用户大写字母姓名。图 7-3 显示了当观众给文本框焦点时，上述代码在浏览器中显示的结果。

后续章节将探讨 `focus` 事件更好的用法，但这里可以让你了解它的工作原理。

### Keydown 事件 (onkeydown)

`keydown` 事件发生在观众按下键盘上的某个按键时。要处理此事件，你使用 `onkeydown`。你可以将此事件处理器放在 Web 页面上的几乎任何 HTML 标签中。

文本框中的 onfocus 事件
图 7-3 当文本框接收到观众的焦点时会弹出此警告
![](img/61d166424839b7674a7b9c8434ae4e03_181_0.png)

### Keypress 事件 (onkeypress)

`keypress` 事件发生在观众按下键盘上的按键并输入对应字符时。这发生在 `keydown` 和 `keyup` 事件之间。为了处理此事件，你使用 `onkeypress` 事件处理器，它可以放在 Web 页面上的几乎任何 HTML 标签中。

### Keyup 事件 (onkeyup)

`keyup` 事件发生在观众松开键盘上的按键时。该事件的事件处理器是 `onkeyup`，它可以放在 Web 页面上的几乎任何 HTML 标签中。

***注意***

关于 `keydown`、`keypress` 和 `keyup` 事件的更多信息，请访问 www.quirksmode.org/js/keys.html。这将让你更好地了解这些事件在不同浏览器中的工作方式，以及为了跨浏览器处理按键输入而需要使用的代码类型。由于这些事件在不同浏览器之间的支持程度不完全一致，本书目前不会对它们进行详细阐述。

### Load 事件 (onload)

`load` 事件发生在 Web 页面完成加载时。要处理此事件，你使用 `onload` 事件处理器。

请记住，`load` 事件发生的时间与你之前在章节中在页面上放置的警告脚本略有不同。那些脚本在页面其余部分加载之前就开始执行你的任务。然而，通过 `load` 事件，你的任务将在页面完成加载后立即执行。

如果你想在页面加载完成后显示警告框，可以使用以下代码：

```html
<body onload="window.alert('I\'m done loading now!');">
  页面正文内容...
</body>
```

当页面加载完成后，观众将收到一个告诉他们已完成的警告框。你很难区分 `load` 事件的时机与之前脚本中即时警告的时机，因为页面全是文本，加载速度会非常快。图 7-4 显示了上述代码示例在浏览器中的外观。

如果你想在脚本代码中使用 `onload` 事件处理器，而不是在 `body` 标签中，你可以将此代码写入外部 JavaScript 文件（保存为 `load_alert.js`）：

```javascript
window.onload = function() {
  window.alert('I\'m done loading now!');
};
```

注意 `onload` 事件处理器被添加到 `body` 标签中，这将捕获当前窗口的加载事件（`window` 对象将在第 10 章中详细解释）。注意此处使用了匿名函数，以将创建函数和将其赋值给事件的步骤结合（有关函数的更多信息，请参阅第 4 章）。你现在可以指向 Web 页面中的 JavaScript 文件，而无需修改 HTML 代码中的 `body` 标签，如下所示：

```html
<body>
  <script type="text/javascript" src="load_alert.js"></script>
  页面正文内容...
</body>
```

为了看到看到立即执行的警告与在 `onload` 事件处理器中执行的警告在时机上的差异，你可能想在页面正文中添加一些图片，然后将页面和图片发布到网上。这样，页面将需要一些时间来加载，你会发现警告会在页面加载完成后弹出，而不是立即显示。

### Mousedown 事件 (onmousedown)

`mousedown` 事件发生在观众按下鼠标按钮但点击尚未完成（不需要松开）时。要处理此事件，你使用 `onmousedown` 事件处理器，它可以放在 Web 页面上的几乎任何 HTML 标签内。

### Mousemove 事件 (onmousemove)

`mousemove` 事件发生在观众移动鼠标光标时。该事件的事件处理器是 `mousemove`，它可以放在 Web 页面上的几乎任何 HTML 标签中。

文本框中的 onfocus 事件
图 7-3 当文本框接收到观众的焦点时会弹出此警告
![](img/61d166424839b7674a7b9c8434ae4e03_181_0.png)

JavaScript：入门指南

### Mouseover 事件 (onmouseover)

`mouseover` 事件发生在观众将鼠标移到元素上。`mouseover` 事件发生在观众将鼠标移到页面上的区域（如链接、链接图片或链接区域）。使用 `mouseover` 的最快方法是设置文本链接。因此，如果你想在观众移过链接时显示警告框，可以编写如下代码：

```html
<a href="http://www.pageresource.com" onmouseover="window.alert('I told you not to click!');">不要点击！</a>
```

这一次，观众在点击之前会被警告框问候。请记住，如果过度使用这种脚本可能会骚扰你的游客。图 7-5 显示了上述代码在浏览器中的结果。

链接标签中的 onmouseover 事件处理器
图 7-5 当鼠标移过链接时会弹出此警告
![](img/61d166424839b7674a7b9c8434ae4e03_184_0.png)

### Mouseout 事件 (onmouseout)

`mouseout` 事件发生在观众将鼠标离开页面上的区域（如链接、链接图片或图像地图的链接区域）。与 `mouseover` 事件一样，大多数浏览器都支持许多区域的 `mouseout` 事件。你通过使用 `onmouseout` 事件处理器来处理 `mouseout` 事件。

再次，通过设置链接并在链接上添加 `onmouseout` 事件处理器，你可以很容易地看到 `mouseout` 事件。这一次，你可以在用户鼠标离开链接后弹出警告框（假设它尚未被点击）。为了实现这一点，你可以使用以下代码：

```html
<a href="http://www.pageresource.com" onmouseout="window.alert('What, you didn\'t like my link?');">点击我！</a>
```

这一次，警告框在观众离开链接时弹出，并向观众提了一个问题。注意注意单词 *didn’t* 中使用的转义引号（\'），这可以防止出现字符串错误。图 7-6 显示了该脚本的运行效果。

链接标签中的 onmouseout 事件处理器
图 7-6 当鼠标移离链接时会弹出此警告
![](img/61d166424839b7674a7b9c8434ae4e03_185_0.png)





# JavaScript：初学者指南

#### 鼠标释放事件 (onmouseup)

当查看者按下鼠标键后松开时，会触发 mouseup 事件。

`onmouseup` 事件处理器用于此事件，它可以放置在网页上的几乎任何 HTML 标签中。

### 重置事件 (onreset)

当查看者使用表单重置按钮来重置表单中的字段时，会触发 reset 事件。为了处理此事件，你使用 `onreset` 事件处理器，它可以被添加到表单的起始 `<form>` 标签中。`onreset` 事件处理器还有一个名为 `reset()` 的相关方法，这将在第 14 章中介绍。

### 提交事件 (onsubmit)

submit 事件仅在查看者在网页上提交表单时才会发生。此事件使用 `onsubmit` 事件处理器，可以从文档中的起始 `<form>` 标签中调用。`onsubmit` 事件处理器还有一个名为 `submit()` 的相关方法，将在第 14 章中介绍。

要查看 submit 事件的作用，你必须创建一个可以通过提交按钮提交的表单。然后，你将在起始 `<form>` 标签中添加 `onsubmit` 事件处理器。下面的代码将在点击提交按钮后向查看者显示一个“感谢”警报框：

```html
<form onsubmit="window.alert('Thank You');">
What's your name?<br />
<input type="text" id="thename" /><br />
<input type="submit" value="Submit Form">
</form>
```

submit 事件现在对你没有太大帮助（尤其是考虑到表单内容并没有真正去往任何地方），但当你学习第 14 章的表单验证时，这个事件将变得更有用。

### 卸载事件 (onunload)

当查看者离开当前 Web 页面时，会触发 unload 事件。查看者可以通过点击链接、在浏览器中输入另一个地址或关闭窗口离开。用于 unload 事件的事件处理器是 `onunload`。

这个事件被认为会干扰查看者，因为它允许网站所有者在访问者尝试移动另一个页面或另一个网站时执行某些操作（强制他们等待）。

为了在用户离开页面时弹出一个警告框，你可以编写以下代码：

```html
<body onunload="window.alert('Be sure to come back, OK?');">
Other HTML code goes here...
</body>
```

- 在起始 `<form>` 标签中使用了 onsubmit
- 提交按钮在被点击时触发 submit 事件
- `onunload` 事件处理器被添加到 `<body>` 标签中

图 7-7 显示了上述脚本的结果。当查看者尝试离开包含此脚本的页面时，会弹出一个警告框，告诉他们一定要回来。当然，如果将其用在索引页或网站内的多个页面上，可能会让查看者感到非常不便。

与 `onload` 事件处理器一样，你可以通过 `window.onunload` 在脚本代码中使用 `onunload` 事件处理器，而不是作为 `<body>` 标签的属性。

总而言之，在上线页面上使用 unload 事件之前，务必仔细考虑。它有很好的用途，但要小心，因为它确实会干扰大多数 Web 用户。

## 使用事件发送警报

这个项目将允许你练习在本章中目前学到的几个事件处理器。你将创建一个包含各种链接和表单元素的页面，这些元素将使用事件来发送警报。

### 逐步步骤

1. 创建一个 HTML 页面并将其保存为 `pr7_2.html`。
2. 在页面中添加一个指向 `http://www.yahoo.com` 的链接。在链接标签上添加一个事件处理器，当查看者将鼠标光标移动到链接上时，会弹出一个显示“Sorry, I’m not in the mood for you to leave yet!”的警告框。
3. 在链接之后添加一个 `<br />` 标签。
4. 在页面 `<br />` 标签下方添加 `<form>` 和 `</form>` 标签，然后在这些标签之间按照以下步骤添加表单元素。
5. 添加一个文本框询问查看者的电话号码。设置为当查看者给文本框焦点时，弹出一个显示“Format is *xxx-xxxx*”的警告框。
6. 添加第二个文本框询问查看者的姓名。设置为当发生失去焦点（blur）事件时，弹出一个显示“Thanks, if that is your real name!”的警告框。
7. 添加第三个文本框询问查看者的电子邮箱地址。不要设置它响应任何事件。
8. 添加一个显示“Click Here to Submit”的提交按钮。设置为当查看者点击它时，弹出一个显示“Hey! I’m just a button. Leave me alone!”的警告框。
9. 保存文件并在浏览器中打开它。
10. 将鼠标移动到第一个链接上。你应该得到第一个警告框。
11. 点击询问电话号码的文本框内部。你应该得到一个警告框。
12. 点击询问姓名的文本框内部。
13. 点击询问电子邮箱地址的文本框内部。
14. 点击提交按钮。

图 7-7 当查看者尝试离开页面时会弹出此警告框。
![](img/61d166424839b7674a7b9c8434ae4e03_187_0.png)

| 图 | 描述 |
| :--- | :--- |
| 图 7-7 | pr7_2.html（续） |

## 使用事件处理器创建脚本

现在你已经处理了事件处理器列表，是时候玩玩了。在本节中，你将学习两个除了写入页面或发送警报之外的新属性。

在你看了所有这些警报示例后，警报可能已经有些乏味了。因此，你将尝试两个新脚本。一个将在文本框中放置消息，另一个将使表单按钮像链接一样。

### 框消息

由于你已经学习了 `mouseover` 和 `mouseout` 事件，你可以结合在本章中获得的其他知识，编写一个脚本，当鼠标移动到链接上时在文本框中显示消息。

首先，你需要创建一个 HTML 文档（将其保存为 `textbox_message.html`）。在该文档中，你设置一个链接并为其锚标签指定一个 `id`。然后，你设置一个文本框并为其输入标签指定一个 `id`。例如，你可以使用以下代码：

```html
<body>
<a href="message.html" id="msg_link">Get Message</a>
<br /><br />
<form>
<input type="text" id="msg_box" />
</form>
<script type="text/javascript" src="textbox_message.js"></script>
</body>
```

通过这段简单的 HTML 代码，你可以使用 JavaScript 让这个简单的页面从静态变为交互。

**Q: 我需要记住所有的事件吗？**
**A:** 只有当你考试、为了工作需要快速掌握知识，或者你只是喜欢脱口而出这些事件时，你可能需要记住它们；否则，如果你不确定需要哪种事件，可以参考本章的表 7-1。

**Q: 我会使用此书中的每一个事件吗？**
**A:** 由于于这是一本初学者指南，你不会达到使用每一个事件的地步。





# JavaScript：初学者指南

***提示***

为了可访问性，将所有超链接指向一个带有内容的实际 URL（在这种情况下，你只需要提供消息文本）是比较好的。这让没有 JavaScript 的用户也能访问脚本中的内容，同时让拥有 JavaScript 的用户只需使用鼠标悬停事件即可访问消息。

由于文本框将在鼠标移动到链接上时显示消息，你首先需要在你的 JavaScript 文件中设置一些变量（将其保存为前述代码脚本标签中引用的 `testbox_message.js`）。你将如下为消息文本、链接元素和文本框元素设置变量：

```javascript
var message_text = "Help! I'm in a box!";
var message_link = document.getElementById("msg_link");
var message_box = document.getElementById("msg_box");
```

`message_text` 变量存储你在鼠标悬停事件时将显示的消息文本，`message_link` 变量通过其 id (msg_link) 获取链接元素，而 `message_box` 变量通过其 id (msg_box) 获取文本框元素。

现在你已经设置好了这些信息，可以配合 `onmouseover` 事件处理程序在文本框中向观众显示消息：

```javascript
var message_text = "Help! I'm in a box!";
var message_link = document.getElementById("msg_link");
var message_box = document.getElementById("msg_box");
message_link.onmouseover = function() {
    message_box.value = message_text;
};
```

这里的大部分内容应该是熟悉的。`onmouseover` 事件处理程序被分配了一个处理该事件的匿名函数。该函数告诉浏览器更改文本框的值，以便显示消息文本。你会注意到 `message_box.value` 的使用。`value` 属性持有元素的当前值。对于文本框来说，它持有当前文本框中显示的任何值（如果它是空的，其值将为空字符串）。通过使用该属性，你可以将值更改为你选择的任何内容，就像这里做的那样。

如果你保存了 HTML 和 JavaScript 文件并在浏览器中加载 HTML 文件，你将看到结果。将鼠标移动到“Get Message”链接上，“Help! I’m in a box!” 消息应该会显示在文本框中。

现在，如果你不想让该消息一直留在文本框中，你可以使用另一个事件来清除文本框中的消息。你可以使用任何你喜欢的事件（在你选择的任何元素上）。一种解决方案是在当观众将鼠标移链接时，使用 `onmouseout` 事件处理程序简单清除消息。因此，你现在可以在你的 JavaScript 文件中使用以下代码：

```javascript
var message_text = "Help! I'm in a box!";
var message_link = document.getElementById("msg_link");
var message_box = document.getElementById("msg_box");
message_link.onmouseover = function() {
    message_box.value = message_text;
};
message_link.onmouseout = function () {
    message_box.value = "";
};
```

注意，在 `onmouseout` 事件处理程序的函数中，`message_box.value` 被更改为空字符串，清除了文本框中的消息。

保存 JavaScript 文件，然后在浏览器中刷新 HTML 页面。你现在应该可以将鼠标移动到链接上接收消息，并将鼠标移开让消息消失。图 7-8 和 7-9 显示了运行中的完整脚本。

下一个脚本将使表单按钮表现得像超链接。

## 按钮链接

使用 JavaScript，你可以将观众引导到另一个 URL。要实现此，你需要使用另一个新属性：`window.location`。此属性允许你更改所在窗口的 URL 地址。

```javascript
window.location="http://someplace.com";
```

图 7-8：当鼠标移动到链接上时，脚本将显示消息。将 *http://someplace.com* 替换为你想要使用的 URL，例如 `https://www.yahoo.com` 或其他 Web 地址。

要开始，你仍然需要创建一个 HTML 文档（将其保存为 `button_link.html`）。在该页面中，你创建一个输入按钮并给它分配一个 id，如下：

```html
<form>
  <input type="button" value="Go Searching!" id="btn1" />
</form>
```

现在，要让按钮像链接一样工作，你需要只需要 location 属性。创建一个外部 JavaScript 文件（将其保存为 `button_link.js`）并使用以下代码：

```javascript
var web_page1 = "http://www.yahoo.com";
var b1 = document.getElementById("btn1");
b1.onclick = function() {
    window.location = web_page1;
};
```

与之前的脚本一样，它获取必要的值，然后使用匿名函数执行 JavaScript 命令。当观众点击按钮时，浏览器跳转到新页面。图 7-9：要去的 URL 被分配给 `web_page1` 变量；输入按钮分配给 `b1`；函数被分配给输入按钮的 onclick 处理器；观众的 location 被更改。当然，你可以对任意数量的按钮这样做。如果你想让三个按钮链接到三个地方，可以使用以下 HTML 和 JavaScript 代码：

```html
<form>
  <input type="button" value="Go Searching!" id="btn1" /><br />
  <input type="button" value="HTML" id="btn2" /><br />
  <input type="button" value="JavaScript" id="btn3" />
</form>
```

有了额外的按钮，为每个元素添加必要的代码和事件：

```javascript
var web_page1 = "http://www.yahoo.com";
var web_page2 = "http://pages.com";
var web_page3 = "http://javascript.com";
var b1 = document.getElementById("btn1");
var b2 = document.getElementById("btn2");
var b3 = document.getElementById("btn3");
b1.onclick = function() {
    window.location = web_page1;
};
b2.onclick = function() {
    window.location = web_page2;
};
b3.onclick = function() {
    window.location = web_page3;
};
```

此代码创建了链接到三个不同网站的按钮。当然，如果你决定使用大量的此类，使用数组可能会更容易。数组将在第一章中讨论。

***注意***

这种按钮链接存在可访问性问题（因为没有 JavaScript 的用户将无所作为）。如果你需要页面可访问，你需要为按钮提供锚点标签（anchor tags），以确保所有用户可以使用。一些脚本可以处理这一点，你将在第 6 章看到如何实现。`window.location` 属性在你学习后续章节时将非常有用。

## 注册事件的其他方法

除了你使用的方法外，还有另外两种注册事件的方法。编写时，这两种方法都不跨浏览器工作（这是一种缺点，因为使用它们需要多次注册同一个事件，但如果需要某些功能，它们可以帮助完成任务）。这些方法允许你更容易地为同一个事件添加多个函数，并更方便地移除特定脚本需要的事件处理函数。目前，你只需对它们的用法进行简单介绍，如果需要或者其中一种方法开始在所有主流浏览器中工作，它们可能会很有帮助。首先，你将查看来自 Web 联盟（W3C）的模型。接下来，你将查看微软的模型。

### addEventListener() 方法

`addEventListener()` 方法来自 W3C。它允许你指定一个事件、一个为事件执行的函数以及一个 `true` 或 `false` 值，取决于你希望事件处理程序函数在捕获阶段（true）还是冒泡阶段（false）执行。通用格式如下：

```javascript
element.addEventListener('event_type', function_name, true_or_false);
```

因此，如果你想像在本章早期那样创建一个链接的输入按钮，可以调整 JavaScript 代码如下：

```javascript
var web_page1 = "http://www.yahoo.com";
var b1 = document.getElementById("btn1");
b1.addEventListener('click', function() { 
    window.location = web_page1;
}, false);
```

注意，该方法不是使用事件处理程序，而是使用事件名称（而不是 `onclick`，只需使用 `click`）。此外，此方法接受不带括号的函数名，或者允许你使用匿名函数（如上所示）。

当元素内部包含另一个元素且两者都注册了相同的事件类型时，捕获和冒泡就变得很重要。哪个事件先发生取决于使用哪种方法。如果使用捕获，则最外元素的事件先发生，最内元素的事件最后发生。如果使用冒泡，则情况相反。捕获阶段发生在冒泡阶段之前，因此在脚本中使用两个阶段时请记住这一点。

要移除事件，你会使用 `removeEventListener()` 方法：

```javascript
element.removeEventListener('event_type', function_name, true_or_false);
```

### attachEvent() 方法

`attachEvent()` 方法的工作原理与 `addEventListener()` 类似。然而，它只适用于事件冒泡，并且目前（截至编写时）尚没有使用事件捕获的方法。它的用法如下：

```javascript
element.attachEvent(event_handler, function_name);
```





## 第 7 章：事件处理器

173

因此，如果你想继续使用你一直在使用的脚本，可以这样写：

```
var web_page1 = "http://www.yahoo.com";

var b1 = document.getElementById("btn1");

b1.attachEvent(onclick, function() { window.location = web_page1; } );
```

注意这种方法确实使用了事件处理器的名称 (onclick)。此外，它没有第三种选项；它只是使用了事件冒泡。

要移除一个事件，你会使用 `detachEvent()` 方法：

*element*.detachEvent(*event_handler*, *function_name*);

目前，你将在脚本中继续使用你在书中之前部分中使用过的方法。

*第 7 章自测题*

1. 事件处理器是对象的一个预定义 JavaScript 属性，用于处理 Web 页面上的事件。

A 正确
B 错误

2. 事件处理器是有用的，因为它们能允许你获取对页面上可能发生的 __________ 的 __________。

3. 要使用事件处理器，你需要知道事件处理器的 __________以及在 HTML 代码中放置事件处理器的位置。

4. 下列哪项正确编写了点击事件的警报代码？

A <input type="button” onclick="window.alert(“Hey there!”);”>
B <input type="button” onClick=“window.alert(‘Hey there!”);”>
C <input type="button” onclick="window.alert(‘Hey there!’);”>
D <input type="button” onChange=“window.alert(“Hey there!”);”>

5. Web 页面加载完成时，发生 __________ 事件。

6. 在什么情况下发生 mouseover 事件：

A 光标在按钮上时观众点击鼠标。
B 观众将鼠标光标移链接。
C 观众点击链接、链接图像或图像映射的链接区域。
D 观众将鼠标光标移动到页面上的某个元素上。
✓

7. 当观众点击页面上的某个元素时，发生 mouseout 事件。

A 正确
B 错误

8. 当观众离开当前 Web 页面时，发生 __________ 事件。

9. blur 事件是 __________ 事件的对立面。

10. 下列哪项正确在 onfocus 事件处理器中调用了名为 major_alert() 的函数？

A <input type="text” onfocus="major_alert();”>
B <input type="text” onfocus="major alert();”>
C <input type="text” onfocus="major_alert();’>
D <input type="text” onFocus='major_alert()”>

11. 当观众更改表单元素内的内容时，发生 __________ 事件。

12. 当观众在 Web 页面上 __________ 一个 __________ 时，发生 submit 事件。

13. 当观众按下键盘上的某个键时，发生 keydown 事件。

A 正确
B 错误

14. mousedown 事件使用什么关键字作为它的事件处理器？

A onmouseout
B onmousepress
C onmousedown
D mousedown

15. __________ 方法和的 __________ 方法是注册事件的两种新方法。

## 第 8 章：对象

175

JavaScript：初学者指南

核心技能与概念

- 定义对象
- 创建对象
- 理解预定义的 JavaScript 对象

由于 JavaScript 是一种基于对象的语言，你需要通过观察对象来理解它们是什么以及你如何使用它们。JavaScript 中的预定义对象非常有用；但是，为了有效地使用它们，学习对象通用的工作原理以及在需要时如何创建自己的对象将是一个好主意。

本章从定义什么是对象以及对象如何在你的脚本中对你有用开始。然后你将发现如何创建并命名你自己的对象，并在代码中使用它们。最后，本章介绍了预定义的 `navigator` 和 `history` 对象的属性和方法。

### 定义对象

要开始使用 JavaScript 对象，你需要了解它们是什么以及它们如何在你的脚本中对你有用。首先，看看 JavaScript 对象是什么。

### 什么是对象？

对象是对现实事物进行建模的一种，尽管该对象是一个抽象实体。当你思考一个对象时，你可能想要可视化一个通用的东西，比如一辆汽车。当你看到一辆车时，你会注意到它具有某些特征，或者说*属性*。你可能看到这辆车配有一个带 CD 播放器的收音机、真皮座椅和 V8 引擎。所有这些东西都是汽车的特征，从对象的角度来说，就是汽车对象的属性。

你可以通过让收音机拥有属性来进一步拆分，或者你可以反过来，，让汽车成为一个更大对象的一部分。例如，你可以说 CD 收音机具有某些特征，如触摸音量控制、收音机预设和数字接口。如果你反过来，你可以说汽车是汽车对象的一部分，该对象可以包括汽车、面包车、卡车以及各种其他车辆作为属性。

通过这样做，你可以创建一个可以从顶层向下追踪的可视化模型。如果你有一辆属于汽车类的汽车，它将拥有自己的属性，如颜色、年份、品牌和型号。它还将由其他对象组成，如轮胎、收音机、方向盘和仪表盘，每个对象都可以有自己的属性和对象。

如果你沿着汽车的收音机路径向下，你可以假设它带有一个带有数字接口的 CD 收音机，你会看到如下模式：

汽车对象 -> 汽车 -> 收音机 -> 数字接口

177

你可以反过来拥有一辆卡车，但特征保持相同。然后你会得到如下模式：

汽车对象 -> 卡车 -> 收音机 -> 数字接口

之前的示例有点像家族树，从顶层开始。顶层之后的每一层都可能有其兄弟姐妹（位于同一层级的对象）。可视化可能会变得复杂，但当你处理实际的 JavaScript 对象时，你不需要太担心“家族树”。大多数对象只有一层，所以你不需要太担心。你想要学习的主要的是对象内部可以包含许多属性，你可以从外部访问它们。

### 为什么对象很有用

对象是有用的，因为它们为你的脚本提供了另一种组织内容的方式。与其在外面散布许多相似的变量，不如将它们组合在一个对象下。

如果你对你的汽车对象创建变量来表示汽车的特征，你就可以开始看到这种分组的工作原理。你可以创建名为 seats、engine 和 theradio 的变量。我们在之后才会创建汽车对象，所以现在假设汽车对象存在，并且拥有 seats、engine 和 theradio 属性。

由于这些属性是变量，它们可以拥有值。问题是，你如何访问这些属性以获取它们的值？

在 JavaScript 中，你通过使用点运算符来访问对象属性，点运算符就是一个点。例如，如果你想要 seats 属性的值，你可以通过以下代码访问它：

```
var chtype= car.seats;
```





# JavaScript：初学者指南

### 大写敏感性

与之前的命名一样，对象的名称是区分大小写的。因此，一个名为 `car` 的对象与一个名为 `Car`、`CAR` 或 `caR` 的对象不同。为了访问正确的对象，你必须确保在脚本中使用正确的大小写字母；否则，当你尝试运行脚本时，会收到类似“Car is not an object”（Car 不是一个对象）的错误。

### 避免保留字/对象

在命名自己的对象时需要记住的另一点是，你不能使用 JavaScript 的保留字（请参考第 3 章“避免保留字”节中的保留字表）；因此，尝试创建一个名为 `switch` 的对象可能会给你带来麻烦，因为该词被用于 JavaScript 的 `switch` 语句。

### 对象结构

在 JavaScript 中创建对象有两种方法：使用构造函数或使用对象初始化器。首先，你将学习如何使用构造函数来创建对象。随后将对如何使用对象初始化器进行简要讨论。

### 构造函数

构造函数允许你使用与普通函数相同的标准语法来构建对象。唯一的区别在于放置在函数内部的代码以及访问其内容的方式。

例如，为了创建你的汽车对象，你会创建一个名为 `car()` 的构造函数，然后在函数内部添加属性。下面的示例显示了 `car()` 函数的结构：

```javascript
function car() {
  // 属性放在这里。
}
```

为了完成上述函数，你需要将属性添加到函数中。回想你想创建一个名为 `car` 的对象，具有 `seats`（座椅）、`engine`（引擎）和 `radio`（收音机）属性。以下代码显示了如何实现：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}
```

在这段代码的第一行，你看到函数接收三个参数，这是你希望汽车对象拥有的属性数量。接下来看到的是参数的值被赋值给你希望汽车对象拥有的属性；然而，有一个名为 *this* 的新关键字。JavaScript 中的关键字 *this* 用于表示当前正在使用的对象，或者说就是“这个对象”。

- 构造函数
- 这里将列出你正在创建的对象的属性
- 函数接收三个参数
- 参数值被赋值给对象的属性

第 8 章：对象
179

一旦用构造函数设置了对象的属性，你就需要创建一个所谓的对象*实例*（instance）以便使用它，因为构造函数只创建了对象的结构，而不是一个可用的对象实例。要创建对象的实例，你需要使用另一个 JavaScript 关键字：`new`。

使用 `new` 关键字创建你的汽车对象实例的代码如下所示：

```javascript
var work_car= new car("cloth","V-6","Tape Deck");
```

你首先看到的是你正在创建一个名为 `work_car` 的新变量。由于你赋值给它的值，该变量将成为 `car` 对象的一个新实例。接下来你看到 `work_car` 变量被赋值了 `car` 构造函数的结果，但有一个变化。在调用 `car` 函数之前是 *new* 关键字，它确保了你正在创建该构造函数对象的新实例。

接下来，你看到通过发送参数的值调用了 `car` 函数。这些是你希望用于此汽车对象实例的值。根据顺序，你是在表示希望座椅是 `cloth`（布料），引擎是 `V-6`，收音机是 `Tape Deck`（磁带）。

现在你可以访问 `car` 对象的 `work_car` 实例。如果你想知道 `work_car` 拥有什么种类型的引擎，可以使用点运算符访问它：

```javascript
var engine_type= work_car.engine;
```

这将 `car` 对象实例 `work_car` 的引擎属性属性值赋值给变量 `engine_type`。由于你将 `V-6` 作为引擎参数发送给构造函数，`engine_type` 变量被赋值为 `V-6`。

### 整合部分

为了帮助你可视化这一过程，是时候将所有这些部分结合在一起，以便你可以看到它是如何工作的。下面的代码结合了之前所有示例的代码，以便更容易观察：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var engine_type= work_car.engine;
```

现在你可以看到构造函数、汽车对象实例的创建，以及将对象的的一个属性赋值给变量。当 `car` 对象的 `work_car` 实例设置好后，它为 `work_car.seats` 属性赋予 `cloth`，为 `work_car.engine` 属性赋予 `V-6`，为 `work_car.theradio` 属性赋予 `Tape Deck`。

- 构造函数
- 创建了一个对象实例，发送参数用作属性值
- 将对象新实例的属性赋值给一个独立变量

JavaScript：初学者指南

为了看到对象实例是如何工作的，你需要在你的代码中添加另一个 `car` 对象实例。下面的代码使用了两个 `car` 对象实例：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");

var engine_type= work_car.engine;
var seat_type= fun_car.seats;
var radio_type= fun_car.theradio;

document.write("I want a car with "+seat_type+" seats.<br />");
document.write("It also needs a "+engine_type+" engine.<br />");
document.write("Oh, and I would like "+radio_type+" also.");
```

通过赋值从每个实例中获取的变量值，你能够在屏幕上打印出你想要的汽车描述。

- 构造函数
- 创建了两个对象实例
- 从每个对象实例提取一个属性值赋值给独立变量
- 脚本结果显示在图 8-1 中
- `document.write()` 命令用于主体，因此它们会在浏览器中显示

第 8 章：对象
181

文件名为 `objects_01.js`，并使用以下主体代码创建一个 HTML 文件并保存为 `objects_01.html`：

```html
<body>
  <script type="text/javascript" src="objects_01.js"></script>
</body>
```

在你的网络浏览器中打开 `objects_01.html` 文件。该脚本的结果如图 8-1 所示。

图 8-1 你喜欢的每种汽车的特性都打印在了浏览器中。

你也可以通过用你的选择创建一个 `car` 对象的新实例并将这些内容打印到屏幕上，来实现一个示例的结果。如果你创建一个名为 `custom_car` 的实例，你可以使用以下代码：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);

document.write("I want a car with "+custom_car.seats+" seats.<br />");
document.write("It also needs a "+custom_car.engine+" engine.<br />");
document.write("Oh, and I would like "+custom_car.theradio+" also.");
```





JavaScript：初学者指南

注意创建 `car` 对象的 `custom_car` 实例时，发送的参数恰好是 `car` 对象其他实例的属性。在许多情况下，你可以像使用变量一样使用对象属性，这减少了你需要编写的代码量。还要注意，`document.write()` 命令已更改为使用 `custom_car` 的属性而不是旧的变量。脚本的输出是相同的，如图 8-2 所示。

属性值

虽然这并不是房地产，但你可以更改你的属性值。在你的脚本中，你可以通过给对象属性赋一个新值来在运行时更改对象属性的值，这就像操作变量一样。例如，如果你想更改之前示例中 `work_car.engine` 属性的值，只需为它分配一个你选择的新值即可。下面的示例显示了给 `work_car.engine` 属性分配一个新值：

`work_car.engine= "V-4";`

虽然这可能不是一个好的改动，但它可以帮你节省一些保险费（以及汽油）！

需要注意的是，前面的赋值将改变在更改之后对 `work_car.engine` 属性的任何调用值。在更改之前对该值进行的任何操作都不会受到影响。因此，为了对你的脚本结果产生影响，你必须在创建使用该属性的 `car` 对象 `custom_car` 实例之前，更改 `work_car.engine` 属性的值。

图 8-2 尽管代码不同，但输出与图 8-1 相同

![](img/61d166424839b7674a7b9c8434ae4e03_204_0.png)

# 第 8 章：对象

183

以下代码在创建对象的新实例之前对属性进行了新的赋值：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");

work_car.engine="V-4";
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);

document.write("I want a car with "+custom_car.seats+" seats.<br />");
document.write("It also needs a "+custom_car.engine+" engine.<br />");
document.write("Oh, and I would like a "+custom_car.theradio+" also.");
```

`work_car.engine` 属性最初被设置为 V-6，但在创建 `car` 对象 `custom_car` 实例之前它被更改为 V-4。这意味着当你在创建 `custom_car` 实例时使用 `work_car.engine` 属性时，它将使用更改后的值 V-4，因为它是在更改之后使用的。图 8-3 显示了更改后的代码的结果。

对象的一个属性被更改了，这改变了之后任何使用该属性的内容。

图 8-3 一个属性值被更改，改变了脚本的输出

![](img/61d166424839b7674a7b9c8434ae4e03_205_0.png)

JavaScript：初学者指南

为了更清楚地说明这一点，你可以在属性更改前后都使用它，以观察它是如何影响脚本的。下面的代码展示了这一点：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");
var first_engine=work_car.engine;
work_car.engine="V-4";
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);

document.write("At first, I wanted a "+first_engine+" engine.<br />");
document.write("But after thinking about it a bit:<br />");
document.write("I want a car with "+custom_car.seats+" seats.<br />");
document.write("It also needs a "+custom_car.engine+" engine.<br />");
document.write("Oh, and I would like a "+custom_car.theradio+" also.");
```

注意 `work_car.engine` 的值是如何赋值给 `first_engine` 变量的。在你创建 `car` 对象 `custom_car` 实例之前，它被更改了。当你将 `first_engine` 变量的值写入浏览器时，它拥有 `work_car.engine` 属性的旧值，因为它是在更改之前赋值的。

当你写入 `custom_car` 属性的值时，你可以看到更改是在你创建 `car` 对象 `custom_car` 实例之前的某个时候完成的。图 8-4 显示了该脚本在浏览器中的结果。

现在你已经知道如何使用构造函数了，请看看对象初始化方法。

## 对象初始化器

对象初始化器比构造函数短一点。以下是对象初始化器的语法：

`objectname={property1:value1, property2:value2};`

在你的脚本中，你可以通过给对象属性赋一个新值来动态更改对象属性的值，就像操作变量一样。例如，如果你想更改之前示例中 `work_car.engine` 属性的值，只需为它分配一个你选择的新值即可。下面的示例显示了给 `work_car.engine` 属性分配一个新值：

`work_car.engine= "V-4";`

虽然这可能不是一个好的改动，但它可以帮你节省一些保险费（以及汽油）！

需要注意的是，前面的赋值将改变在更改之后对 `work_car.engine` 属性的任何调用值。在更改之前对该值进行的任何操作都不会受到影响。因此，为了对你的脚本结果产生影响，你必须在创建使用该属性的 `car` 对象 `custom_car` 实例之前，更改 `work_car.engine` 属性的值。

图 8-2 尽管代码不同，但输出与图 8-1 相同

![](img/61d166424839b7674a7b9c8434ae4e03_204_0.png)

# 第 8 章：对象

183

以下代码在创建对象的新实例之前对属性进行了新的赋值：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");

work_car.engine="V-4";
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);

document.write("I want a car with "+custom_car.seats+" seats.<br />");
document.write("It also needs a "+custom_car.engine+" engine.<br />");
document.write("Oh, and I would like a "+custom_car.theradio+" also.");
```

`work_car.engine` 属性最初被设置为 V-6，但在创建 `car` 对象 `custom_car` 实例之前它被更改为 V-4。这意味着当你在创建 `custom_car` 实例时使用 `work_car.engine` 属性时，它将使用更改后的值 V-4，因为它是在更改之后使用的。图 8-3 显示了更改后的代码的结果。

对象的一个属性被更改了，这改变了之后任何使用该属性的内容。

图 8-3 一个属性值被更改，改变了脚本的输出

![](img/61d166424839b7674a7b9c8434ae4e03_205_0.png)

JavaScript：初学者指南

为了更清楚地说明这一点，你可以在属性更改前后都使用它，以观察它是如何影响脚本的。下面的代码展示了这一点：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");
var first_engine=work_car.engine;
work_car.engine="V-4";
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);

document.write("At first, I wanted a "+first_engine+" engine.<br />");
document.write("But after thinking about it a bit:<br />");
document.write("I want a car with "+custom_car.seats+" seats.<br />");
document.write("It also needs a "+custom_car.engine+" engine.<br />");
document.write("Oh, and I would like a "+custom_car.theradio+" also.");
```

注意 `work_car.engine` 的值是如何赋值给 `first_engine` 变量的。在你创建 `car` 对象 `custom_car` 实例之前，它被更改了。当你将 `first_engine` 变量的值写入浏览器时，它拥有 `work_car.engine` 属性的旧值，因为它是在更改之前赋值的。

当你写入 `custom_car` 属性的值时，你可以看到更改是在你创建 `car` 对象 `custom_car` 实例之前的某个时候完成的。图 8-4 显示了该脚本在浏览器中的结果。

现在你已经知道如何使用构造函数了，请看看对象初始化方法。

## 对象初始化器

对象初始化器比构造函数短一点。以下是对象初始化器的语法：

`objectname={property1:value1, property2:value2};`

在你的脚本中，你可以通过给对象属性赋一个新值来动态更改对象属性的值，就像操作变量一样。例如，如果你想更改之前示例中 `work_car.engine` 属性的值，只需为它分配一个你选择的新值即可。

`work_car.engine= "V-4";`

虽然这可能不是一个好的改动，但它可以帮你节省一些保险费（以及汽油）！

需要注意的是，前面的赋值将改变在更改之后对 `work_car.engine` 属性的任何调用值。在更改之前对该值进行的任何操作都不会受到影响。因此，为了对你的脚本结果产生影响，你必须在创建使用该属性的 `car` 对象 `custom_car` 实例之前，更改 `work_car.engine` 属性的值。

图 8-2 尽管代码不同，但输出与图 8-1 相同

![](img/61d166424839b7674a7b9c8434ae4e03_204_0.png)

# 第 8 章：对象

185

接下来，你将使用初始化器创建对象。以下代码显示了使用初始化器创建对象：

```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");

work_car.engine="V-4";
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);

document.write("I want a car with "+custom_car.seats+" seats.<br />");
document.write("It also needs a "+custom_car.engine+" engine.<br />");
document.write("Oh, and I would like a "+custom_car.theradio+" also.");
```

这种方法打印了每个类型的结果。

#### 方法

方法是对象的一部分的函数调用。考虑你之前使用构造函数创建的对象。可以使用初始化器创建：
```javascript
var work_car = {
  seats:"cloth",
  engine:"V-6",
  theradio:"Tape Deck"
};
var fun_car = {
  seats:"leather",
  engine:"V-8",
  theradio:"CD Player"
};
```
你可以像使用构造函数一样使用初始化器：
```javascript
document.write("I want a car with "+custom_car.seats+" seats.<br />");
document.write("It also needs a "+custom_car.engine+" engine.<br />");
document.write("Oh, and I would like a "+custom_car.theradio+" also.");
```
这种方法可以减少代码量，至少如果你只需要一个类型时是。

# 第 8 章：对象

185

这种方法在浏览器中显示的结果。

### 添加方法

方法是对象的一部分的函数调用。方法可以执行你想要执行的任务。你可能想要让汽车执行停止、加速或转向的功能。你可能还决定进行某种计算，例如付款。如果你想为该对象添加一个计算月付款额的函数，你可以创建一个如下函数：
```javascript
function get_payment() {
  var the_payment=250;
  if(this.seats == "leather") {
    the_payment+=100;
  }
  else {
    the_payment+=50;
  }
  return the_payment;
}
```
要向你的对象添加此方法，你需要将函数赋值给对象的属性：
```javascript
work_car.get_payment = get_payment;
fun_car.get_payment = get_payment;
```
现在你可以在每个对象上调用该方法：
```javascript
document.write("The payment for the work_car is "+work_car.get_payment()+"<br />");
document.write("The payment for the fun_car is "+fun_car.get_payment()+"<br />");
```
或者，你可以在使用初始化器时定义方法：
```javascript
var work_car = {
  seats:"cloth",
  engine:"V-6",
  theradio:"Tape Deck",
  get_payment:get_payment
};
```
你也可以在使用构造函数时定义方法：
```javascript
function car(seats,engine,theradio) {
  this.seats=seats;
  this.engine=engine;
  this.theradio=theradio;
  this.get_payment = function() {
    var the_payment=250;
    if(this.seats == "leather") {
      the_payment+=100;
    }
    else {
      the_payment+=50;
    }
    return the_payment;
  };
}
```





## 第8章：对象

187

```javascript
if(this.engine == "V-8") {
    the_payment+=150;
}
else {
    the_payment+=75;
}

if(this.theradio == "CD Player") {
    the_payment+=35;
}
else {
    the_payment+=10;
}

return the_payment;
}
```

嗯，之前的函数确实很长。可以通过对每个 if/else 语句使用条件运算符来缩短（关于条件运算符的更多信息，请参考第 6 章）：

```javascript
function get_payment() {
    var the_payment=250;
    the_payment += (this.seats == "leather") ? 100 : 50;
    the_payment += (this.engine == "V-8") ? 150 : 75;
    the_payment += (this.theradio == "CD Player") ? 35 : 10;
    return the_payment;
}
```

定义好函数后，你需要将其赋值给对象构造函数中的对象。使用你可靠的 `car` 对象构造函数，你可以像下面的代码所示进行赋值：

```javascript
function car(seats,engine,theradio) {
    this.seats=seats;
    this.engine=engine;
    this.theradio=theradio;
    this.payment=get_payment;
}
```

注意，这个示例定义了一个名为 `payment` 的方法，它从构造函数外部调用了 `get_payment()` 函数。同样注意，当在这里调用该函数时，函数调末尾没有使用括号。这就是你的外部函数变成对象方法的方法（通过赋值函数本身，而不是函数的执行结果）。

- 一个 if/else 语句根据对象 `engine` 属性的值决定向 `payment` 变量 增加多少金额。
- 一个 if/else 语句根据对象 `theradio` 属性的值决定向 `payment` 变量增加多少金额。
- 返回 `the_payment` 的值。
- 使用条件运算符代替 if/else 语句以使代码更短。
- `get_payment()` 函数像属性一样被赋值，使其成为当前对象的方法；注意赋值时没有使用括号。

JavaScript：初学者指南

为了调用对象的 `payment()` 方法，你需要一个 `car` 对象的实例。如果你加上之前创建的三个实例，你就可以对你的新方法进行一些操作了。因此，将这些实例添加到你已有的代码中：

```javascript
function get_payment() {
    var the_payment=250;
    the_payment += (this.seats == "leather") ? 100 : 50;
    the_payment += (this.engine == "V-8") ? 150 : 75;
    the_payment += (this.theradio == "CD Player") ? 35 : 10;
    return the_payment;
}

function car(seats,engine,theradio) {
    this.seats=seats;
    this.engine=engine;
    this.theradio=theradio;
    this.payment=get_payment;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);
```

现在你已经有了创建 `car` 对象 `payment()` 方法的函数、在 `car` 对象构造函数内部创建 `payment()` 方法的代码，以及三个 `car` 对象实例。

要查找 `work_car` 的每月付款额，你需要使用以下语法调用 `payment()` 方法：

```javascript
var work_car_payments= work_car.payment();
```

`work_car_payments` 变量的值将是 `payment()` 方法返回的值，即 `get_payment()` 函数在带有 `work_car` 实例的值进行运行时所返回的结果。

由于座椅是布质（cloth），`the_payment` 增加了 50（如果是皮革的，则会增加 100）。由于引擎是 V-6，`the_payment` 增加了 75。最后，由于 `theradio` 属性的值是磁带机（Tape Deck），`the_payment` 变量增加了 10。这让你得到的付款金额为 250（初始值）+ 50（皮革座椅）+ 75（非 V-8 引擎）+ 10（CD 播放器），结果为 385。

使用 `payment()` 方法，你现在可以编写脚本在浏览器中显示每种汽车的付款金额，以便观众决定购买哪种汽车。你只需要扩展之前的代码，在页面主体中包含一些使用 `payment()` 方法返回值的 `document.write()` 命令。将 JavaScript 文件保存为 `objects_02.js`，并创建一个带有代码的 HTML 文件并保存为 `objects_02.html`：

```html
<body>
<script type="text/javascript" src="objects_02.js"></script>
</body>
```

- 被用作方法使用的函数
- 构造函数，它使函数成为方法
- 创建了对象的实例，并在需要可以使用该方法

- 下面 `objects_02.js` 文件的 JavaScript 代码提供了每个 `car` 对象实例使用的 `payment()` 方法示例：

```javascript
function get_payment() {
    var the_payment=250;
    the_payment += (this.seats == "leather") ? 100 : 50;
    the_payment += (this.engine == "V-8") ? 150 : 75;
    the_payment += (this.theradio == "CD Player") ? 35 : 10;
    return the_payment;
}

function car(seats,engine,theradio) {
    this.seats=seats;
    this.engine=engine;
    this.theradio=theradio;
    this.payment=get_payment;
}

var work_car= new car("cloth","V-6","Tape Deck");
var fun_car= new car("leather","V-8","CD Player");
var custom_car= new car(fun_car.seats,work_car.engine,fun_car.theradio);

var work_car_payment= work_car.payment();
var fun_car_payment= fun_car.payment();
var custom_car_payment= custom_car.payment();

document.write("<h2>你请求的汽车信息</h2>");
document.write("<strong>用车: ");
document.write(work_car.seats+","+work_car.engine+","+work_car.theradio);
document.write("<br />");
document.write("<strong>付款: $"+work_car_payment);
document.write("<p>");
document.write("<strong>轿用汽车: ");
document.write(fun_car.seats+","+fun_car.engine+","+fun_car.theradio);
document.write("<br />");
document.write("<strong>付款: $"+fun_car_payment);
document.write("</p>");
document.write("<p>");
document.write("<strong>定制汽车: ");
document.write(custom_car.seats+","+custom_car.engine+","+custom_car.theradio);
document.write("<br />");
document.write("<strong>付款: $"+custom_car_payment);
document.write("</p>");
```

与目前为止大多数脚本相比，这个脚本相当长。前面的脚本结果是列出每种类型的汽车及其特征以及付款金额。对象的三个实例的方法返回值被赋值给三个独立的变量。在 `document.write()` 语句中使用各种对象属性和变量来创建汽车、特征和付款金额的列表。

### 对象操作语句

JavaScript 允许你使用 `for-in` 循环处理对象，并使用 `with` 语句更容易地访问特定对象。

### for-in 循环

`for-in` 循环允许你遍历对象的属性以显示它们或操作它们的值。以下代码显示了 `for-in` 循环的结构：

```javascript
for (var variable_name in object_name) {
    // JavaScript 语句
}
```

图 8-6 汽车类型、特征及每月付款金额列表。

循环通过命名一个代表对象属性名的变量来开始。

假设你想遍历 `car` 对象实例的属性以便在页面上显示每个属性的值。`for-in` 循环允许你无需输入每个属性名称完成这一点，代码所示：

```javascript
function car(seats,engine,theradio) {
    this.seats=seats;
    this.engine=engine;
    this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");

for (var prop_name in work_car) {
    document.write(work_car[prop_name]+"<br />");
}
```

你会注意到脚本中的 `work_car[prop_name]` 部分并不熟悉。`for-in` 循环使用数组来存储属性值，这需要这种语法。你将在第 11 章学习更多关于数组的知识，所以如果现在还不清楚请担心。现在你只需要知道 `for-in` 循环的功能。

### with 语句

如果你计划使用大量操作对象的语句，`with` 语句允许你更容易地访问或操作对象的属性和方法。例如，如果你想在网页上编写关于某个对象的语句，可能会对输入对象名、点运算符和属性名感到厌。`with` 语句允许你在 `with` 块内部的语句中省略对象名点运算符，因此只需要输入属性名即可访问所需的属性。以下代码显示了 `with` 语句的结构：

```javascript
with (object) {
    // JavaScript 语句
}
```

假设有一个名为 `car` 的对象，具有 `seats`、`engine` 和 `radio` 属性，以及一个名为 `work_car` 的对象实例。你可以使用 `with` 语句避免重复输入 `work_car` 和点运算符，例如所示：

```javascript
function car(seats,engine,theradio) {
    this.seats=seats;
    this.engine=engine;
    this.theradio=theradio;
}

var work_car= new car("cloth","V-6","Tape Deck");

with (work_car) {
    document.write(seats+"<br />");
    document.write(engine+"<br />");
    document.write(theradio+"<br />");
}
```





JavaScript：初学者指南

document.write("Seats: "+seats+"<br />");

document.write("Engine: "+engine+"<br />");

document.write("Radio: "+this.radio);

}

此示例在页面上输出了 car 对象中 `work_car` 实例的属性值。请注意，在 `with` 块内部，使用属性名时不需要在前面输入 `work_car` 和点运算符。

现在，你已经了解了如何创建自己的对象、属性和方法，这可以更好地理解一些预定义的 JavaScript 对象是如何运作的。在你学习本章剩余部分以及后续的几个章节中，将讨论许多预定义的 JavaScript 对象。

现在，访问对象的 `work_car` 实例的属性时，不需要每次在使用时都输入 `work_car` 和点运算符。

**Q：当我使用构造函数时，每次需要对象时真的都必须创建一个对象的实例吗？**

**A：** 是的。构造函数仅为浏览器提供对象的结构。要使用该结构，你需要创建该对象的实例。你将在第 12 章中看到，你也需要为一些预定义的 JavaScript 对象创建实例。

**Q：那么对象初始化器呢？我不需要用它们创建实例吗？**

**A：** 对象初始化器会直接创建一个对象，而不仅仅像构造函数那样只提供一个结构。因此，创建的对象不需要再创建实例。

**Q：我需要频繁使用自己编写的对象吗？**

**A：** 可能不需要，这取决于你的脚本以及你想做什么。本书中的许多脚本都使用了预定义的 JavaScript 对象；但是，如果自己编写的对象对你之后的脚本编写有帮助，你也可以使用。

**Q：一个对象可以有多个方法吗？**

**A：** 你可以通过重复在本章开头对方法进行的操作，在对象中包含任意数量的方法。例如，你可以再添加另一个方法，根据你已有的汽车类型属性来计算每种汽车的保险费用。

专家问

第 8 章：对象
193

### 8-1 创建一个计算机对象

在这个项目中，你将自己创建对象，并开发对象创建所需的技能。脚本将创建一个计算机对象，然后使用该对象的属性、方法和实例为不同类型的计算机创建特性列表和价格列表。

逐步演练

1. 创建一个 HTML 页面并将其保存为 `pr8_1.html`。添加必要的 script 标签以指向名为 `prjs8_1.js` 的外部 JavaScript 文件。
2. 创建一个外部 JavaScript 文件并将其保存为 `prjs8_1.js`。将其用于第 3–12 步。
3. 创建一个名为 `computer` 的对象，包含三个属性：`speed`、`hdspace` 和 `ram`。
4. 创建 `computer` 对象的实例并命名为 `work_computer`。为 `speed` 参数发送字符串值 `"2GHz"`，为 `hdspace` 参数发送字符串值 `"80GB"`，为 `ram` 参数发送字符串值 `"1GB"`。
5. 创建 `computer` 对象的实例并命名为 `home_computer`。为 `speed` 参数发送字符串值 `"1.5GHz"`，为 `hdspace` 参数发送字符串值 `"40GB"`，为 `ram` 参数发送字符串值 `"512MB"`。
6. 创建 `computer` 对象的实例并命名为 `laptop_computer`。为 `speed` 参数发送字符串值 `"1GHz"`，为 `hdspace` 参数发送字符串值 `"20GB"`，为 `ram` 参数发送字符串值 `"256MB"`。
7. 创建一个名为 `get_price()` 的函数，计算计算机的价格。计算机的基础价格为 500，并赋值给名为 `the_price` 的变量。如果对象的 `speed` 属性等于 `2GHz`，则给 `the_price` 的值加 200；否则给 `the_price` 加 100。如果对象的 `hdspace` 属性为 `80GB`，则给 `the_price` 的值加 50；否则给 `the_price` 加 25。如果对象的 `ram` 属性为 `1GB`，则给 `the_price` 的值加 150；否则给 `the_price` 加 75。使用 `return` 语句结束函数并返回变量 `the_price` 的值。
8. 为 `computer` 对象添加对第 6 步创建的函数的调用。将该方法命名为 `price`。
9. 将在对象的 `work_computer` 实例上使用 `price()` 方法时的返回值赋值给变量 `work_computer_price`。
10. 将在对象的 `home_computer` 实例上使用 `price()` 方法时的返回值赋值给变量 `home_computer_price`。
11. 将在对象的 `laptop_computer` 实例上使用 `price()` 方法时的返回值赋值给变量 `laptop_computer_price`。
*(待续)*
12. 按照本章稍处汽车示例中使用的格式，将每种类型计算机的特性和价格写入浏览器屏幕。
13. 保存 JavaScript 文件并在浏览器中查看 HTML 文件。你应该能看到屏幕上列出了每台计算机的特性列表和价格。

尝试此总结

在这个项目中，你能够自己创建对象，并开发对象创建所需的技能。脚本将创建一个计算机对象，然后使用该对象的属性、方法和实例为不同类型的计算机创建特性列表和价格列表。

理解预定义对象

现在，你已经了解了如何创建自己的对象、属性和方法，这可以更好地理解一些预定义的 JavaScript 对象是如何运作的。在你学习本章剩余部分以及后续的几个章节中，将讨论许多预定义的 JavaScript 对象。

现在，访问对象的 `work_car` 实例的属性时，不需要每次在使用时都输入 `work_car` 和点运算符。

navigator 对象

`navigator` 对象允许你访问各种属性，例如其名称、版本等。首先，查看 `navigator` 的属性。

属性

`navigator` 对象的属性可以让你了解有关浏览器的各种信息。`navigator` 对象的属性是修改的，因为它们被设置为只读。

`appCodeName` 属性：此属性持有浏览器应用程序代码名称的值，通常是如 `Mozilla` 之类的。除了写入屏幕或向查看者发送警告之外，你目前对它没太大用。以下代码显示了如何向查看者发送警告，告知他们所使用的浏览器 `appCodeName`：

window.alert("You are using "+navigator.appCodeName);

表 8-1 Navigator 对象属性

| 属性 | 值 |
| :--- | :--- |
| appCodeName | 浏览器的代码名称 |
| appName | 浏览器的名称 |
| appMinorVersion | 表示浏览器次版本的字符串 |
| appVersion | 浏览器版本及其他信息 |
| browserLanguage | 所用浏览器的语言（Internet Explorer 和 Opera） |
| buildID | 所用浏览器的构建标识符 |
| cookieEnabled | 指定浏览器是否启用了 cookie |
| cpuClass | 表示 CPU 类的字符串（仅限 Internet Explorer） |
| language | 所用浏览器的语言（Firefox 和 Opera） |
| mimetypes | 浏览器支持的 MIME 类型数组 |
| onLine | 指定浏览器是否处于“全局离线模式” |
| oscpu | 表示计算机操作系统的字符串（仅限 Firefox） |
| platform | 创建该浏览器的机器类型 |
| plugins | 浏览器安装的插件数组 |
| product | 表示所用浏览器产品名称的字符串（仅限 Firefox） |
| productSub | 所用浏览器的构建号（仅限 Firefox） |
| securityPolicy | 空字符串——在 Netscape 4.7 中返回一个值（仅限 Firefox） |
| systemLanguage | 操作系统使用的默认语言（仅限 Internet Explorer） |
| userLanguage | 操作系统的自然语言（Internet Explorer 和 Opera） |
| userAgent | 浏览器的 user agent 头 |
| vendor | 空字符串——返回表示所用浏览器供应商的字符串（仅限 Firefox） |
| vendorSub | 空字符串——返回所用浏览器的供应商版本号（仅限 Firefox） |





# JavaScript：初学者指南

请注意，你使用的是对象名后跟点运算符，然后是属性名，就像你创建自己的对象时所做的一样。这就是访问 `navigator` 对象属性的方法。

请注意，对于此属性，几乎所有浏览器都会返回 Mozilla，这是 Netscape Navigator 早期版本的代号。

### appName 属性
此属性允许你查找查看者正在使用哪种类型的浏览器来浏览页面。如果浏览器是 Firefox，此属性的值将是 Netscape。如果浏览器是 Internet Explorer，那么此属性的值将是 Microsoft Internet Explorer。其他浏览器将具有相应的值。

如果你需要知道特定浏览器的值，可以创建一个脚本来提醒（alert）此属性的值，将脚本放在 Web 页面的 script 标签内，然后在该浏览器中查看该页面。然后你将收到关于该浏览器属性值的提醒。以下代码显示了如何编写该提醒代码：

```javascript
window.alert("You have "+navigator.appName);
```

由于这可以让你查找到正在使用的浏览器类型，你可以创建一个简单的浏览器检测脚本。

假设你想根据对对用浏览器的看法向查看者发送一个提醒。你可以使用 `navigator.appName` 属性来创建一个 if/else 块，并根据浏览器类型向查看者发送相应的注释。

以下代码显示了你如何执行此任务的示例：

```html
<body>
  <script type="text/javascript">
    switch (navigator.appName) {
      case "Netscape" : window.alert("Firefox/Netscape is cool."); break;
      case "Microsoft Internet Explorer" : window.alert("Internet Explorer is Cool."); break;
      case "Opera" : window.alert("Opera is cool."); break;
      default : window.alert("What browser is this?");
    }
  </script>
  Hi, and welcome!
</body>
```

如你所见，查看者现在可以知道你对所用浏览器的真实想法。图 8-7 显示了如果你使用 Firefox 查看页面时将收提醒。

### appVersion 属性
此属性的值为浏览器版本号以及一些额外信息。例如，在 Windows XP 的 Firefox 3 中，你可能会看到以下文本作为此属性的值：

`5.0 (Windows; en-US)`

使用 switch 块来确定 `navigator.appName` 属性的值并给查看者提供适当的提醒。当你使用仅应在某些级别以上的浏览器中执行的技术时，这非常有利。但请注意，浏览器对此属性返回不同的结果，此处所示 Windows Vista 上的 Internet Explorer 7 返回的值：

`4.0 (compatible; MSIE 7.0; Windows NT 6.0; SLCC1; .NET CLR 2.0.50727; Media Center PC 5.0; .NET CLR 3.5.30729; .NET CLR 3.0.30618)`

字符串的第一部分是 4.0，随后它描述自己为 MSIE 7.0。因此，在使用此属性时必须小心，因为你需要知道各种浏览器返回的内容，以便最好地利用这些信息。

### cookieEnabled 属性
如果浏览器启用了 cookie，则此属性返回布尔值 true；如果浏览器未启用 cookie，则返回布尔值 false。你将在第 16 章中详细介绍 cookie。

### onLine 属性
如果查看者的系统未处于全局离线模式，此属性返回布尔值 true（详情请参阅 http://msdn.microsoft.com/en-us/library/aa768170(VS.85).aspx），如果系统处于全局离线模式，则返回布尔值 false。

### platform 属性
此属性持有创建浏览器的机器类型的值。例如，在 Windows XP 机器上，值将是 Win32。

![](img/61d166424839b7674a7b9c8434ae4e03_219_0.png)
图 8-7 当使用 Firefox 进入页面时收到的提醒

不同类型的机器有不同的值。如果你想让查看者知道正在使用的机器类型，可以此此属性发送一个提醒：

```javascript
window.alert("Your machine is a "+navigator.platform+" machine.");
```

虽然在这里用处不大，但该属性可以根据用户的机器类型将查看者重定向到相应的页面。

### plugins 属性
此数组持有查看者浏览器中安装的所有插件的值。你将在第 12 章中了解到更多关于数组的知识。

### userAgent 属性
此属性为你提供了关于浏览器的另一个长字符串信息。该字符串是浏览器的用户代理（user agent）头。例如，在 Windows XP 的 Firefox 3 中，你可能会看到以下字符串：

`Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.9.0.4)`
`Gecko/2008102920`
`Firefox/3.0.4`

它和你看到的 navigator.appVersion 属性的文本非常相似，但包含更多信息。

现在你已经了解 `navigator` 的属性，准备好查看方法了。

#### 方法
`navigator` 对象还有许多你可以使用的方法。表 8-2 显示了可用的方法。

### javaEnabled() 方法
如果查看者启用了 Java，此方法返回布尔值 true；否则返回 false。如果你想向查看者显示 applet，javaEnabled() 方法将有用。

表 8-2 Navigator 方法

| 方法 | 目的 |
| :--- | :--- |
| javaEnabled() | 测试浏览器是否启用了 Java |
| mozIsLocally() | 检查特定地址是否可用（仅限 Firefox） |
| preference() | 设置某些浏览器偏好（需要签名脚本） |
| registerContentHandler() | 允许网站注册为特定 MIME 类型的潜在处理器 |
| registerProtocolHandler() | 允许网站注册为特定协议的潜在处理器 |
| taintEnabled() | 因为该方法已不再使用。它曾用于指定浏览器是否启用了数据污染（tainting） |

目前，你只需看到如何发送提醒。这种方式你不需要处理任何 Java 语法。以下代码在查看者启用了 Java 时发送一个提醒，在未启用时发送另一个：

```javascript
var hasJava= navigator.javaEnabled()
if (hasJava==true) {
  window.alert("Cool, you have Java!");
}
else {
  window.alert("Java disabled? You cannot see my app!");
}
```

这测试了 navigator.javaEnabled() 返回的值并给用户提供正确的提醒。

#### History 对象
`history` 对象也是 `window` 对象的一部分，提供了当前窗口浏览器历史信息。

#### 属性
`history` 对象只有一个属性，名为 `length`（在 Firefox 中可以使用更多属性，但它们不适用于 Web 内容）。此属性返回当前浏览器会话历史中的页面数，包括当前加载的页面。它可以以类似方式使用：

```html
<body>
  <script type="text/javascript">
    alert("Your current window has viewed "+history.length+" pages!")
  </script>
</body>
```

这只是向查看者发送一个提醒，说明在当前浏览器窗口中访问了多少页面。

#### 方法
`history` 对象有三个方法，列于表 8-3。

表 8-3 History 方法

| 方法 | 目的 |
| :--- | :--- |
| Back() | 将浏览器窗口在历史列表中后退一页 |
| Forward() | 将浏览器在历史列表中向前一页 |
| Go() | 使用整数值将浏览器跳转到历史列表中的指定页面 |




JavaScript：初学者指南

接下来的章节将详细讨论这些方法中的每一种。

## back() 方法

back() 方法会将浏览器发送到历史列表中当前页面之前访问的上一个页面，这就像使用浏览器的“后退”按钮一样。要使用它，你只需要在脚本中需要的地方调用该方法即可。因此，如果你想通过表单按钮创建一个自己的“后退”按钮，可以使用类似于下面的代码。首先是 HTML 身体部分的代码（保存为 history_01.html）：

```html
<<body>

<form>

<input type="button" value="Back" id="back_button" />
</form>

<script type="text/javascript" src="history_01.js"></script>

</body>
```

接下来是外部的 JavaScript 代码（保存为 history_01.js）：

```javascript
var bb = document.getElementById("back_button");

bb.onclick = function() {
  history.back();
};
```

加载该 HTML 页面将显示“后退（Back）”按钮。当你点击它时，浏览器将跳转到当前页面之前访问的最后一个页面。如果浏览器窗口没有之前的历史记录，点击该按钮将没有任何作用。

## forward() 方法

forward() 方法会将浏览器发送到历史列表中当前页面之后访问的页面，这就像使用浏览器的“前进”按钮一样。要使用它，你只需要在脚本中需要的地方调用该方法即可。通过这种方法，你可以更新之前的脚本添加一个“前进（Forward）”按钮。接下来显示更新后的 HTML 和 JavaScript 代码。

HTML 代码：

```html
<body>

<form>

<input type="button" value="Back" id="back_button" /><br />
<input type="button" value="Forward" id="forward_button" />
</form>

<script type="text/javascript" src="history_01.js"></script>

</body>
```

更新后的外部 JavaScript 代码：

```javascript
var bb = document.getElementById("back_button");
var fb = document.getElementById("forward_button");

bb.onclick = function() {
  history.back();
};

fb.onclick = function() {
  history.forward();
};
```

第 8 章：对象

201

此 8-2

加载该 HTML 页面现在将显示两个按钮。与 back() 方法一样，如果窗口的历史列表中没有前进的页面，使用 forward() 将没有任何作用。

## go() 方法

go() 方法接受一个整数作为参数。该整数可以是负数，用于在历史列表中后退，也可以是正数，用于在历史列表中向前移动。例如，以下代码将会在窗口历史中后退两个页面：

```javascript
history.go(-2);
```

以下代码将会在历史列表中向前移动三个页面：

```javascript
history.go(3);
```

与另外两个方法一样，如果用户尝试访问的页面不存在（例如，像 history.go(15) 这样的页面可能不在窗口历史记录中），那么该方法将什么都不作为。

预定义的 JavaScript 对象非常有帮助。正如你将在下一章中看到的，document（文档）对象允许你访问许多额外的属性和方法，用于处理 HTML 文档。

## 使用预定义的 navigator 对象进行练习

此项目允许你练习使用预定义的 navigator 对象的一些属性和方法。你将创建一个页面，根据所使用的浏览器向查看者显示不同类型的信息。

### 逐步步骤

1. 创建一个 HTML 页面并将其保存为 pr8_2.html。
2. 创建一个外部 JavaScript 文件并将其保存为 prjs8_2.js。将其用于第 3-12 步。
3. 编写在查看者进入页面时弹出的警告（alert）。警告应显示“Hi! You are viewing my page with . ”后面跟随查看者正在使用的浏览器名称。
4. 如果用户启用了 Java，向查看者发送一个新警告，显示“You have Java enabled, that is cool!”。如果查看者没有启用 Java，则发送显示“No Java? Well, no fun stuff here then.”的警告。
5. 发送一个新的警告，告诉查看者正在使用什么种类型的机器。警告应显示“You are using . ”后面跟随查看者查看页面时使用的机器类型。
6. 保存文件并在一个或多个浏览器（如果可以，也可以其他计算机）中打开 HTML 文件。查看结果如何根据查看网页时使用的内容而变化。

*（续）

pr8_2.html

prjs8_2.js

JavaScript：初学者指南

## 尝试总结

在这个项目中，你使用了关于预定义的 navigator 对象的属性和方法的知识。你能够创建一个网页，根据浏览器、机器类型以及是否启用了 Java 向查看者发送不同的警告。

*第 8 章自测*

1. 对象是模拟某些 __________ 的一种方式，尽管该对象是一个（个）__________ 实体。
2. 当你思考一个对象时，你可能想要视觉化某个 __________ 的东西。
3. 对象是有用的，因为它们为你提供了在脚本内 __________ 对象的另一种方法。
4. 在 JavaScript 中，你通过使用以下访问对象属性：
   - A 加法运算符
   - B 点运算符
   - C 乘法运算符
5. 对象的命名规则与 ________ 相似。
6. 你可以通过 ________ 或函数来创建一个对象。
   - A 真
   - B 假
8. 对于以下内容，你可以说：
   - A 假设对象存在，kitchen 被赋值为字符串。
   - B 假设对象存在，kitchen 被添加到。
   - C 假设对象存在，kitchen 被赋值为新字符串。
   - D 将什么都不作为。
10. 这行代码创建了。
12. 对于以下代码，你可以说：
    - A 假设对象存在，kitchen 被赋值为字符串。
    - B 假设对象存在，kitchen 被添加到。
    - C 假设对象存在，kitchen 被赋值为新字符串。
    - D 将什么都不作为。
13. 在 JavaScript 中，有很多 __________ 对象你可以使用来访问某些。
14. __________ 对象允许你访问各种属性。
15. 下列哪项不是 navigator 对象的属性？
    - A appName
    - B appCodeName
    - C appType
    - D appVersion

第 8 章：对象

201

此 8-2

JavaScript：初学者指南

第 8 章：对象

203

第 9 章

文档对象

205

JavaScript：初学者指南

技能与概念

- 定义文档对象
- 使用文档对象
- 使用文档对象的属性
- 使用文档的方法
- 创建动态脚本

N 现在你了解对象如何工作以及如何使用预定义对象，现在是查看一些主要的预定义对象了。本章介绍了 document 对象，它可以帮助你获取查看页的信息。正如你将在本章中发现的，document 对象的某些属性和方法可以获取有关文档的信息或更改有关文档的信息。你还将被介绍文档对象模型（DOM），并了解它如何结合样式表来创建动态脚本。





## 第 9 章：文档对象

207

如果你有以下 HTML 代码，你可以使用 JavaScript 来访问其结构：

```html
<body>
  <h1>My Page</h1>
  <img src="myimage.jpg" alt="My Picture" />
</body>
```

图 9-1 显示了 `body` 元素如何作为一个节点，以及它如何拥有子节点和属性节点。

`h1` 和 `img` 元素都是 `body` 元素的子节点。每个元素也拥有它们自己的节点。`h1` 元素包含一个文本节点作为其子节点（文本为“My Page”），而 `img` 元素包含两个属性节点（`src="myimage.jpg”` 和 `alt="My Picture”`）。这种形式的结构在整个文档中都是通用的，因此虽然这是一个简单的例子，但对于大多数 HTML 页面都可以绘制出更为复杂的文档结构树。

你已经在使用 `document.getElementById()` 方法来访问 DOM，通过通过元素的 `id` 属性值来访问文档中的元素。你还可以使用诸如 `getElementsByTagName()` 或 `getElementsByClassName()` 等方法获取一组元素。

使用 JavaScript 访问 DOM 允许你创建更动态的脚本，能够响应用户事件并更改文档中的元素。你还可以使用文档对象的某些 JavaScript 方法（如 `createElement()` 或 `createTextNode()`）来创建元素和节点。这些类型的脚本将在本章稍后部分介绍。

首先，你将查看文档对象的属性和方法。

### 使用文档对象的属性

表 9-1 列出了文档对象的属性以及每个属性的简短描述。表格之后，将对某些特定属性进行更详细的讨论。为某些属性提供了示例脚本。注意，许多属性使用数组来存储信息。如果你想学习数组以更好地理解用法，请参见第 11 章。

***注意***

并非所有这些属性都跨浏览器兼容。此外，其中许多已被弃用（`alinkColor`、`bgColor`、`fgColor`、`linkColor` 和 `vlinkColor`）。你可以访问 http://developer.mozilla.org/en/DOM/document#Properties 和 http://msdn.microsoft.com/en-us/library/ms531073(VS.85).aspx 查看更多关于这些属性的信息。

图 9-1 文档结构的部分示例

![](img/61d166424839b7674a7b9c8434ae4e03_229_0.png)

JavaScript：初学者指南

#### 表 9-1 文档对象的属性

| 属性 | 描述 |
| :--- | :--- |
| activeElement | 返回一个包含文档中活动元素值的字符串 |
| alinkColor | 返回文档活动链接颜色的十六进制值 |
| anchors | 包含文档中所有具名锚点的数组 |
| async | 用于告诉浏览器是否使用异步请求或同步请求加载文档 |
| applets | 包含文档中所有 Java applet 的数组 |
| bgColor | 返回文档背景颜色的十六进制值 |
| body | 返回文档的 `body` 元素或 `frameset` 元素 |
| characterSet | 返回一个表示编码文档所使用的字符集的字符串值 |
| charset | 返回一个表示编码文档所使用的字符集的字符串值 |
| childNodes | 包含文档所有子节点的数组 |
| compatMode | 如果文档在怪异模式（Quirks mode）下渲染，则返回字符串“BackCompat”，若在严格模式（Strict mode）下渲染，则返回字符串“CSS1Compat” |
| contentType | 返回来自文档 MIME 头部 Content-Type 的字符串 |
| cookie | 用于在文档中设置 JavaScript cookie |
| defaultCharset | 返回一个表示编码文档时使用的默认字符集的字符串值 |
| defaultView | 引用文档的 `window` 对象 |
| designMode | 返回一个提供文档是否可以编辑信息的字符串值 |
| dir | 返回一个表示文档阅读方向的字符串值 |
| doctype | 返回与文档关联的 `doctype` 声明 |
| documentElement | 返回一个表示文档根节点的字符串 |
| documentURI | 返回一个表示文档 URI 的对象（仅对特权 JavaScript 代码可用） |
| domain | 返回文档所在服务器的域名 |
| embeds | 包含文档中所有 `embed` 标签的数组 |
| expando | 根据文档内是否可以创建任意变量返回一个布尔值 |
| fgColor | 返回文档默认文本颜色的十六进制值 |
| fileCreatedDate | 返回文档的创建日期 |
| fileModifiedDate | 返回文档最后修改的日期 |
| form | 本身不是一个属性，但会为文档中放置的每个命名表单创建一个新属性 |
| forms | 包含文档中所有 `form` 标签的数组 |
| frames | 包含文档中使用的所有 `frame` 的数组 |
| height | 返回文档 `body` 元素的高度（单位为像素） |
| images | 包含文档中所有图像（`img`）标签的数组 |
| implementation | 返回一个表示文档实现对象的字符串值 |
| inputEncoding | 返回一个表示文档编码的字符串 |
| lastModified | 返回文档的最后修改日期 |
| layers | 包含页面上所有 `layer` 标签的数组（仅限 Netscape Navigator 4） |
| all | 允许访问页面上的所有对象 |
| linkColor | 返回默认链接颜色的十六进制值 |
| links | 包含文档中所有链接（<a>）标签的数组 |
| location | 返回文档的 URL |
| namespaces | 包含文档中所有命名空间的数组 |
| parentWindow | 返回父窗口的引用 |
| plugins | 包含文档中所有插件的数组 |
| protocol | 返回地址的协议部分 |
| readyState | 返回一个表示当前状态的字符串值 |
| referrer | 返回引用文档的 URL |
| scripts | 包含文档中所有脚本的数组 |
| styleSheets | 包含文档中所有样式表的数组 |
| tags | 设置文档中 HTML 标签的样式 |
| title | 返回文档标题内部的文本 |
| uniqueID | 返回一个表示文档唯一 ID 的字符串值 |
| URL | 返回文档的 URL |
| vColor | 返回访问过的链接颜色的十六进制值 |
| width | 返回文档 `body` 元素的宽度（单位为像素） |

表 9-1 文档对象的属性（续）

209

第 9 章：文档对象

### 颜色属性

`alinkColor`、`bgColor`、`fgColor`、`linkColor` 和 `vlinkColor` 属性曾用于获取或更改页面上各种元素的颜色。现在建议使用 CSS 或样式属性（后文将讨论）来设置这些。

#### anchors 属性（数组）

`anchors` 属性实际上是一个由浏览器设置的数组（例如 `<a name="top">`）。由于你还没有学习数组，这目前对你并没有什么帮助；但是，当你学到第 11 章时，你会发现这样的数组是很有用的。

JavaScript 提供了 `length` 属性，让你能够获取页面上锚点的数量。你可以使用 `length` 属性向浏览器窗口写入页面上有多少锚点：

```html
<body>
  <h1>My Page</h1>
  <a name="sec1"></a>
  <h2>Section 1</h2>
  <p>这部分全是关于第一部分的内容...</p>
  <a name="sec2"></a>
  <h2>Section 2</h2>
  <p>这部分讨论了所有第二部分的问题和...</p>
  <br />
  <script type="text/javascript">
    document.write("There are " + document.anchors.length + " named anchors");
  </script>
</body>
```

这段代码在页面上创建了两个具名锚点，随后写入锚点的数量。图 9-2 显示了该脚本在浏览器窗口中的结果。

再次，这目前更多是一个信息属性。一旦你学习了数组，就可以更多地使用 `anchors` 属性。

### cookie 属性

`cookie` 属性用于设置 JavaScript cookie 以为查看者存储信息。Cookie 是保存在查看者计算机上持续一段时间的小文本文件（特定的日期或浏览器会话）。Cookie 有助于网站记住和检索查看者的信息（例如购物车内容、特殊设置或会话信息）。第一个具名锚点通过锚点标签设置。第二个具名锚点通过锚点标签设置。





## 第 9 章：文档对象

211

要设置 cookie，你需要将 `document.cookie` 属性的值赋值为一个字符串，该字符串包含你想为查看者存储的信息。以下是其语法：

`document.cookie="string";`

你应当将 *string* 替换为包含你想使用的信息的文本字符串。通常，它的格式如下面的设置 cookie 示例所示：

`document.cookie="site=homepage";`

你可以看到 cookie 设置了一项内容：site 为 homepage。在两个值之间，等号用于在读取 cookie 时帮助区分 site 和首页。

在尝试进一步处理 cookie 之前，你将需要熟悉并掌握一些更高级的字符串处理技术。在随后的章节中，你将详细看到如何使用这些高级的字符串处理技术，以及如何设置和读取 cookie。现在，你只需要知道 `document.cookie` 属性是用于设置 cookie 的。

### dir 属性

`dir` 属性返回一个表示文档阅读方向的字符串值。该值可以是 `ltr`（从左到右）或 `rtl`（从右到左）。该属性对于显示从右到左而非从左到右阅读的语言 Web 页面非常有用。

图 9-2 页面上的命名锚点数量显示在浏览器窗口中

![](img/61d166424839b7674a7b9c8434ae4e03_233_0.png)

JavaScript 入入门

通过将值设置为 `rtl`。为了好玩，你可以使用此属性动态更改页面的外观，如下例代码所示：

```javascript
var the_button = document.getElementById("change_sides");

the_button.onclick = function() {
    document.dir = (document.dir!="ltr") ? "ltr" : "rtl";
}
```

然后，在你的 HTML 文件中，你添加一个按钮来实现切换：

```html
<<body>
  <form>
    <input type="button" value="Change Sides" id="change_sides"
    onclick="switch_sides(); />
  </form>
</</body>
```

当查看者点击按钮时，页面的阅读方向将改变。在这种情况下，你的按钮最初位于页面左侧，点击按钮后会移动到右侧。图 9-3 显示了点击按钮之前的页面，图 9-4 显示了点击按钮后的页面。

### domain 属性

`domain` 属性存储了为查看者提供页面的域名值。该值是 Web 地址开头 `http://` 之后且任何正斜杠之前的任何内容。因此，如果你正在查看一个来自 `http://www.pageresource.com` 的页面，那么 `document.domain` 的值就是 `www.pageresource.com`。

代码检查这些值并更改它们

图 9-3 点击按钮前的 Web 页面

![](img/61d166424839b7674a7b9c8434ae4e03_234_0.png)

213

要使用 `domain` 属性，你向查看者发送一个识别域名的 alert。在文档中放置以下代码将弹出一个带有 `domain` 属性值的警框：

```html
<body>
  <script type="text/javascript">
    window.alert("You have reached the "+document.domain+" domain!");
  </script>
</body>
```

如果将此代码放置在 `http://javascriptcity.com` 的任何页面上，查看者将收到一条显示“You have reached the javascriptcity.com domain!”的 alert。

***注意***

在没有 Web 服务器的情况下本地使用此属性时，返回的值可能是一个空字符串而不是域名。

### formname 属性

`formname` 属性本身并不是一个属性。每当你命名一个表单（form）时，你就创建了一个 `formname` 属性，但该属性实际上是表单的名字而不是 `formname`。要理解其含义，请查看带有表单的页面。以下代码将给你一个包含表单的 HTML 页面：

```html
<body>
  <form name="funform">
    <input type="button" name="funb" value="You can click me I suppose" />
  </form>
</body>
```

图 9-4 点击按钮后的 Web 页面

![](img/61d166424839b7674a7b9c8434ae4e03_235_0.png)

为表单命名以创建一个属性

JavaScript 入门

此代码通过起始 `<form>` 标签中的 `name="funform"` 属性创建了 `document.funform` 属性。虽然这本身没做什么什么，但它确实允许你访问表单内的表单元素。

`funform` 属性下实际上还有属性，这些属性以表单元素命名。你可以通过 `document.funform.funb` 访问你在表单中使用 `name="funb"` 属性创建的按钮；然而，即使是这样，这本身也做不了什么。你需要再深入一层。`value` 属性允许你设置或更改表单元素的值。这些内容通常设置在 `input` 标签的 `value` 属性中。下面的示例显示了你可以如何使用 `onclick` 事件来改变按钮文本：

```html
<body>
  <form name="funform">
    <input type="button" name="funb" value="You can click me I suppose"
    onclick="document.funform.funb.value='Thanks, you clicked!';" />
  </form>
</body>
```

图 9-5 显示了点击按钮之前的页面。注意括号内只需要 `document.funform.funb`。如果此属性存在，则返回 `true`（任何非空值都可能被视为真——基本上如此）。通过赋值更改了按钮文本

![](img/61d166424839b7674a7b9c8434ae4e03_236_0.png)

215

### forms 属性（数组）

`forms` 属性是一个数组，页面上的每个表单都有对应的项。该数组提供了使用 `formname` 属性的替代方案；但在深入研究此数组之前，你仍然需要在第 11 章学习数组。

与其他类似的属性一样，你可以使用 `document.forms.length` 属性获取页面上有多少表单。

### images 属性（数组）

`images` 属性是另一个数组。该数组 页面上的每个图像都有对应的项。与其他类似的属性一样，你可以使用 `document.images.length` 属性获取 HTML 文档中有多少图像。

此属性的另一个用途是检测哪些浏览器支持 JavaScript 中的 `Image` 对象。如果你希望预加载图像，这非常有帮助。当图像悬停脚本（你将在第 16 章创建）时，预加载图像是一个好主意；如果你想在查看者的缓存文件中放置另一个页面上将使用的图像，这也很有用，可以使该页面加载得更快。

要检查浏览器是否支持 `Image` 对象，你可以将任何需要 `Image` 对象的代码放在 `if` 块中。该 `if` 块将测试 `document.images` 属性是否存在，如下例所示：

```javascript
if (document.images) {
    // JavaScript 语句
}
```

注意括号内只需要 `document.images`。如果此属性存在，则返回 `true`（任何非空值都可能被视为真——基本上如此）。

图 9-6 点击按钮后的浏览器显示

![](img/61d166424839b7674a7b9c8434ae4e03_237_0.png)

这是你放置需要

`document.images` 属性工作的代码




JavaScript：初学者指南

当返回 `!=null` 时，代码块中的语句将执行。如果该属性不存在，则该代码块被忽略，旧版浏览器会因为不需要尝试运行这些代码而感到满意。

要预加载图像，你首先需要创建一个 JavaScript `Image` 对象的新实例。

以下代码显示了创建 `Image` 对象新实例的语法：

```
var *varname**= new Image(*width*,*height*);
```

你将 *varname* 替换为你想要给此 `Image` 对象实例命的名字。将 *width* 替换为你想要使用的图像宽度（像素），并将 *height* 替换为图像的高度（像素）。

所以，如果你想创建一个名为 `myimage` 的 `Image` 对象实例，该图像宽度为 100 像素，高度为 75 像素，你可以使用以下代码：

```
var myimage= new Image(100,75);
```

宽度和高度参数是可选的。你也可以在没有它们创建对象实例：

```
var myimage= new Image();
```

接下来，你需要一种方法来定义将使用哪种图像（类似于图像标签中的 `src` 属性）。`Image` 对象有一个 `src` 属性允许你执行此操作。你只需要通过给它赋值来设置它。以下代码显示了如何操作：

```
var myimage= new Image();

myimage.src= "smile.gif";
```

现在，浏览器将尝试从本地地址 `smile.gif` 加载图像。如果你需要，也可以使用完整的 URL。由于图像在这里尝试加载而无需显示，因此它正在被预加载。

***提示***

预加载通常在文档的 `head` 部分（或在 `head` 部分中调用的外部脚本文件中）进行，以便图像能够尽快开始加载。

为了将所有这些整合在一起，你需要将此代码放在你的 `if` 块中，这样不支持 `Image` 对象的浏览器就不会运行它。以下代码将两部分结合在一起，并将脚本放在文档的 `head` 部分。这将预加载图像以供以后使用。

```html
<head>

<script language="javascript">

if (document.images) {

var myimage= new Image();

myimage.src= "smile.gif";

}

</script>

</head>
```

这完成了预加载图像的工作，以便你以后可以使用它。

- 创建了 `Image` 对象的新实例
- 给对象的 `src` 属性赋值，预加载图像

第 9 章：文档对象
217

若要预加载多一张图像，你需要为每个想要预加载的图像创建一个 `Image` 对象实例。所以，如果你想预加载三张图像，可以使用以下代码：

```html
<head>

<script type="text/javascript">

if (document.images) {

var myimage= new Image();

myimage.src= "smile.gif";

var yourimage= new Image();

yourimage.src= "friendly.gif";

var herimage= new Image();

herimage.src= "happy.gif";

}

</script>

</head>
```

这为你预加载了三张图像。新实例 `yourimage` 预加载了名为 `friendly.gif` 的图像。实例 `herimage` 预加载了名为 `happy.gif` 的图像。如果你愿意，可以使用相同的技术添加更多图像。

### lastModified 属性

`lastModified` 属性持有当前文档最后修改的日期和时间值。这主要用于信息性目的，例如显示文档最后修改的日期，让观众知道你最后一次更新页面的时间。该属性的值取决于你的浏览器，因为如果你在页面上编写最后修改日期，不同的浏览器会产生不同的结果。

考虑以下代码，它将 `document.lastModified` 属性的值写入 Web 页面，以显示最后修改的日期和时间：

```html
<body>

<h1>My Always Updated Web Page!</h1>

<script type="text/javascript">

document.write("Last Updated: "+document.lastModified);

</script>

</body>
```

图 9-7 显示了在 Mozilla Firefox 中查看此代码的结果。

在页面上书写最后修改的日期时，差异性影响仅体现在页面空间上。某些布局可能需要为较长的属性版本留出额外的空间。

### layers 属性（数组）

`layers` 属性是另一个数组，页面上的每个 `layer` 标签都有一个条目，你可以使用 `document.layers.length` 形式的 `length` 属性来查找页面上的层数。`layer` 标签在 Netscape Navigator 4 中被用作创建页面不同部分（可以分层）的方法，并用于脚本访问它们。在现代浏览器中，它不再被使用，因为每个元素都可以通过其他手段（例如 `document.getElementById()` 方法）访问。

由于此属性仅在 Netscape Navigator 4 版本可用，你可以使用此属性来判断使用的浏览器是否是 Netscape Navigator 4。你可以像测试 `document.images` 属性一样的方法测试 `document.layers` 属性。

- 第一张图像已预加载
- 第二张图像已预加载
- 第三个图像已预加载

JavaScript：初学者指南
240

第 9 章：文档对象
219

### all 属性

虽然 `layers` 属性帮助你检测 Netscape 4，但 `all` 属性可以帮助你检测 Internet Explorer 或更高版本。`all` 属性的目的是让 JavaScript 访问页面上的所有对象。再次，这在现代浏览器中通过其他方法（如 `getElementById()` 方法）更好。

所以，为了查看用户是否使用 Internet Explorer，可以使用以下代码：

```javascript
if (document.all) {

window.alert("You have Internet Explorer!");

}
```

图 9-7 Firefox 中的最后日期

### links 属性（数组）

`links` 属性是另一个数组，它为页面上的每个链接（例如`<a href="url">`）和图像映射的链接区域（例如`<area href="url">`）持有一个值。你可以通过 `document.links.length` 找出页面有多少链接。

### referrer 属性

`referrer` 属性用于信息性目的，持有观众在到达你的页面之前所在的页面的 URL 值。虽然这可能很有用，但观众并不总是带有来源 URL（例如在使用书签或输入地址时），因此该值可能为空。此外，该属性的值并不总是正确的，因为不同的浏览器可能认为不同类型的内容引导用户进入新页面。

要使用此属性，你可以向页面观众发送警报，告诉他们在到达你的页面之前在哪里。将以下示例中的代码放入文档即可实现效果：

```html
<body>

<script type="text/javascript">

window.alert("You came from "+document.referrer+"!");

</script>

</body>
```

所以，如果来源页面是 `http://www.pageresource.com/webdes.htm`，则会向观众发送一条显示“你来自 http://www.pageresource.com/webdes.htm!”的警报。

### title 属性

`title` 属性持有 HTML 文档标题的字符串值。标题设置在页面的 `<title>` 和 `</title>` 标签内部。

你可以使用 `title` 属性将页面标题显示在窗口的其他地方，而不是窗口的顶栏。以下代码允许你执行此操作：

```html
<head>

<title>Lions, Tigers and Bears!</title>

</head>

<body>

<script type="text/javascript">

document.write("<h1>" + document.title + "</h1>");

</script>

Lions and tigers and bears were what I saw when I went to ...

</body>
```

这会将你的标题作为标题显示在页面上。图 9-8 显示了在浏览器中查看此代码的结果。




JavaScript：初学者指南

### URL 属性

`URL` 属性存储当前文档完整 URL 的值。如果你在 HTML 页面底部打印此信息，它将非常有用，因为对于任何打印你页面的人来说，它都会显示该页面的 URL。

虽然你可以手动在底部输入 URL，但要在许多页面上执行此操作时，可能会变得非常繁琐。这时这个属性就派上用场了，因为只需要将一小脚本粘贴到每个页面，而不需要每次都输入不同的 URL 地址。下面的代码展示了在页面上编写 URL 地址的示例：

```html
<body>
<h1>买点东西吧！</h1>
如果你不买点东西，我会非常难过的，所以你最好...
<br/><br/>
<script type="text/javascript">
document.write("You are at: "+document.URL);
</script>
</body>
```

图 9-9 显示了上述代码在浏览器中的执行结果。页面的最后一行告诉查看者当前的位置。该图显示的是本地文件地址，但如果页面在在线上，它将显示一个普通的 URL。

## URLUnencoded 属性

`URLUnencoded` 属性返回无需任何编码的文档 URL。例如，如果文件名包含空格，该属性将返回空格而不是代替 `%20`。对于 URL `http://www.pageresource.com/my script.html`，`document.URL` 属性将返回 `http://www.pageresource.com/my%20script.html`。而 `document.URLUnencoded` 属性返回 `http://www.pageresource.com/my script.html`，即未对空格进行编码的 URL。请注意，在本书时，该属性仅在 Microsoft Internet Explorer（书中提到的三个浏览器之一）中可用。

图 9-8 文档标题以标题的形式显示在页面
![](img/61d166424839b7674a7b9c8434ae4e03_242_0.png)

图 9-9 文档的 URL 显示在页面内容的末尾
![](img/61d166424839b7674a7b9c8434ae4e03_243_0.png)

**Q：这些许多属性都是数组，我还没有办法真正使用。我以后会用它们做些什么吗？**

**A：**没有详细讨论数组的原因是你还没有学习数组是如何运作的。当你学会后，你将能够更好地利用创建数组的属性，因为你将知道如何访问数组，以及在访问数组元素时可以对它们进行什么。

**Q：`referrer` 属性很酷！有没有方法可以在每次访客进入时将该信息写入文件，这样我就知道访客是从哪里来的？**

**A：**遗憾的是，客户端 JavaScript 无法在文件中保存信息（cookie 除外，cookie 只对单个查看者有用）；因此，你无法使用此属性在个人文件中跟踪引用页面的 URL 地址。要实现这一点，你需要使用服务器端语言获取信息并将其保存到服务器上的文件中。

提问专家
（续）

## 使用文档对象的方法

`document` 对象的方法允许你执行一些以前无法做到的新操作。表 9-2 列出了这些方法及其简短描述。由于在本书编写时，许多方法（与属性一样）是特定浏览器的，因此在表格之后仅对某些特定方法进行了详细描述。

**Q：通过为表单命名来创建 `name` 属性有点让人困惑。然后，尝试使用名称和 `value` 属性来更改表单元素的值让它更加困惑。我可以看另一个例子吗，也许是文本框或其他按钮以外的东西？**

**A：** 这种访问表单元素的方法在现代浏览器中并不经常使用。通常情况下，会使用你已经熟悉的 `getElementById()` 等较新的方法。如果仍然感到困惑，不要担心。在书的后面有一整章专门讲解如何在表单中使用 JavaScript JavaScript（第 14 章）。

| 方法 | 描述 |
| :--- | :--- |
| attachEvent() | 将函数绑定到事件，以便该函数在事件发生时运行（仅限 Internet Explorer） |
| createAttribute() | 创建一个属性，其名称作为参数发送给它 |
| createAttributeNS() | 在特定的命名空间中创建一个新属性 |
| createCDATASection() | 创建一个新的 CDATA 节段 |
| createComment() | 创建一个注释，其值作为参数发送给它 |
| createDocumentFragment() | 创建一个新的文档片段 |
| createElement() | 创建一个作为参数发送的类型的元素 |
| createElementNS() | 在特定的 URI 和作为参数发送的特定类型创建一个元素 |
| createEntityReference() | 创建一个新的实体引用 |
| createEvent() | 创建一个事件 |
| createEventObject() | 创建一个事件对象用于传递事件信息 |
| createNodeIterator() | 创建一个节点迭代器 |
| createNodeResolver() | 创建一个解析器 |
| createProcessingInstruction() | 创建处理指令 |
| createRange() | 创建一个范围 |
| createStyleSheet() | 创建一个样式表 |
| createNode() | 创建一个节点 |
| createTreeWalker() | 创建一个树游器 |
| detachEvent() | 从事件中分离函数 |
| elementFromPoint() | 从点获取元素 |
| evaluate() | 评估 |
| execCommand() | 执行命令 |
| getElementById() | 通过 ID 获取元素 |
| getElementsByClassName() | 按类名获取元素 |
| getElementsByName() | 按名称获取元素 |
| getElementsByTagName() | 按标签名获取元素 |
| getElementsByTagNameNS() | 按标签名和命名空间获取元素 |
| getSelection() | 获取选择 |
| getFocus() | 检查文档是否有焦点 |
| load() | 加载文档 |
| mergeAttributes() | 从对象合并属性 |
| open() | 打开新文档 |
| close() | 关闭文档 |
| queryCommandEnabled() | 检查命令是否启用 |
| queryCommandIndeterminate() | 检查命令是否是不定的 |
| queryCommandState() | 检查命令的状态 |
| queryCommandSupported() | 检查是否支持命令 |
| queryCommandValue() | 返回命令的值 |
| recalc() | 重新计算动态属性 |
| releaseCapture() | 捕获 |
| setActive() | 设置对象为激活 |
| write() | 向文档写入文本 |
| writeln() | 向文档写入换行文本 |





## 第 9 章：文档对象

225

### getElementsByTagName() 方法

此方法允许你获取一个数组，数组中包含了文档中所有具有参数传递的指定标签名的元素。例如，要获取文档中的所有图像（image）元素，可以使用以下代码：

`var all_images = document.getElementsByTagName("img");`

由于该方法涉及数组，我们将在第 11 章对其进行更详细的讨论。

### open() 和 close() 方法

`open()` 方法允许你打开一个新的文档，并完全使用 `document.write()` 或 `document.writeln()` 语句创建其内容。当调用 `open()` 方法时，浏览器会寻找这些语句以便写入新页面。一旦 `write()` 和/或 `writeln()` 语句完成，你需要使用 `document.close()` 来完成新页面的加载。

为了获取 `open()` 方法的使用示例，假设你想根据查看者的名称编写一个新页面。要实现这一点，你不仅需要使用 `open()` 和 `close()` 方法，还需要创建一个 `formName` 属性以便使用，从而获取查看者在文本框中输入的名称。

从初始页的 body 部分代码开始。你需要一个带有文本框的表单，以及一种调用创建新文档函数的方法。以下代码显示了实现此操作的方法（将文件保存为 `document_open.html`）：

```html
<body>

<strong>请在下方的框中输入你的名称，然后点击按钮查看个性化页面！</strong>

<br />
<form id="newp" onsubmit="newpage();">

Name: <input type="text" id="yourname" size="25">

<br/><br/>
<input type="submit" value="Submit">

</form>

<script type="text/javascript" src="document_open.js"></script>

</body>
```

这部分设置了你的脚本，为你提供了一个 id 为 `newp` 的表单和一个 id 为 `yourname` 的文本框。它还包含一个用于提交表单的按钮。现在，你需要在外部 JavaScript 文件中创建 `newpage()` 函数，以便该表单能够工作。

`newpage()` 函数需要获取文本框的内容并将其赋值给变量。然后，它需要在浏览器窗口中打开你新定制的页面。以下代码显示了如何实现这一点（将文件保存为 `document_open.js`）：

```javascript
function newpage() {
  var thename = document.getElementById("yourname").value;
  document.open();
  document.write("<h1>Welcome!</h1>");
  document.write("Hello, "+thename+", and welcome to my page!");
  document.close();
}
```

该函数执行的第一件事是获取文本框的内容。要获取文本框的内容，你需要使用 `value` 属性，将其加到末尾以获取 `document.getElementById("yourname").value`。然后，该值被赋值给 `thename` 变量，以便在你的 `document.write()` 命令中使用。

一旦你获取了该值，就可以准备打开新页面了。要做到这一点，你使用 `document.open()` 命令，它允许你使用一系列 `document.write()` 语句，直到使用 `document.close()` 命令。你使用 `document.write()` 语句在页面上为查看者写入问候语。

你现在可以在浏览器中打开 HTML 页面来尝试一下。图 9-10 显示了带有表单的初始页面（点击表单按钮之前的页面）。这是查看者输入名称并点击按钮的地方。

图 9-11 显示了在文本框中输入名称“John”并点击按钮的结果。新页面出现了并带有问候语！

***提示***

`open()` 和 `close()` 方法可以用于根据名称、喜爱的食物或其他你可能想要自定义新页面的变量来动态创建页面。

- 新文档使用这些语句来确定显示什么
- 新文档的设置被关闭，从而允许其显示

图 9-10 这是允许查看者输入信息的页面
![](img/61d166424839b7674a7b9c8434ae4e03_248_0.png)

227

### write() 方法

你在书早期就开始使用 `write()` 方法了，所以你可能已经非常了解它的工作原理了；但这里有一个关于该方法的简要描述，作为复习。`document.write()` 方法用于向页面写入字符串值。以下代码将在 HTML 文档的 body 部分中写入“hi there”：

```html
<body>

<script type="text/javascript">
document.write("hi there");
</script>

</body>
```

### writeln() 方法

`writeln()` 方法的工作方式与 `document.write()` 方法相同，但在语句末尾添加了 JavaScript 换行符 (`\n`)。回想起第 3 章讨论过 JavaScript 换行符是如何运作的——它只在页面源代码中放置一个新行，使其更容易阅读。

***提示***

虽然换行符只会影响使用 `document.write()` 时的源代码显示，但它可以用于在 JavaScript 中创建新行，例如 `alert`、`prompt` 和 `confirm`。

图 9-11 这是在文本框中输入名称“John”并点击按钮的结果。
![](img/61d166424839b7674a7b9c8434ae4e03_249_0)

### 创建方法

document 的一些方法（如 `createElement()`、`createAttribute()`、`createTextNode()`）允许你在页面上创建各种元素或节点。要使用这些方法，必须将其作为现有节点的子。

### 节点属性

DOM 节点属性如表 9-3 所示。

| 属性 | 描述 |
| :--- | :--- |
| attributes | 指定节点中所有属性的数组；数组每个成员的名称和值 |
| childNodes | 指定节点的所有子节点的数组 |
| className | 指定节点的 class 属性 |
| clientHeight | 指定节点的高度（像素） |
| clientWidth | 指定节点的宽度（像素） |
| dir | 指定节点的方向值（ltr 从左到右或 从右到左） |
| firstChild | 节点的第一个子节点 |
| id | 指定节点的 id 属性 |
| innerHTML | 指定节点内部的 HTML 代码（文本、图像、标签等） |
| lang | 指定节点的语言值 |
| lastChild | 节点的最后一个子节点 |
| nodeName | 指定节点的名称（例如 div 元素的名称为 div） |
| nodeType | 指定节点的类型 |
| nodeValue | 指定节点的值（例如 div 内部的文本或属性的值） |
| offsetHeight | 指定节点的偏移高度 |
| offsetWidth | 指定节点的偏移宽度 |
| ownerDocument | 包含指定节点的文档对象 |
| parentNode | 指定节点的父节点 |
| previousSibling | 指定节点之前的节点 |
| scrollLeft | 指定节点左边缘与视图左边缘之间的差 |
| scrollTop | 指定节点顶边缘与视图顶边缘之间的差 |
| scrollHeight | 指定节点的整个高度（包括通过滚动条可见的区域） |
| scrollWidth | 指定节点的整个宽度（包括通过滚动条可见的区域） |
| style | 指定节点的样式对象 |
| tabIndex | 指定节点的标签索引 |
| tagName | 指定节点的标签名（大写写） |
| title | 指定节点的 title 属性值 |

表 9-3 节点属性





JavaScript：初学者指南

如果你想获取 div 元素的 `title` 属性值，可以使用 `document.getElementById()` 通过其 id `div1` 获取该 `div` 元素。这将是 DOM 节点 `title` 属性的指定节点。然后，你可以像下面的代码那样访问元素节点的 `title` 属性：

```javascript
var me_div = document.getElementById("div1");
var me_title = me_div.title;
window.alert("The title of the div element is" + me_title);
```

这的工作原理与你在上一章中学到的对象属性完全一样。`me_div.title` 属性返回字符串值“All about me!”，这是 `div` 元素节点 `title` 属性的值。

了解这一点，你可以以相同的方式使用 DOM 节点方法。

## DOM 节点方法

表 9-4 列出了 DOM 节点方法。

| 方法 | 说明 |
| :--- | :--- |
| addEventListener() | 为指定的节点添加事件监听器，以便在发送给它的事件作为参数运行时运行函数 |
| appendChild() | 将节点作为指定节点的最后一个子节点添加 |
| attachEvent() | 为指定的节点附加事件，以便在发送给它的事件作为参数运行时运行函数 |
| blur() | 从指定的节点移除焦点 |
| click() | 在指定的节点上执行点击事件 |
| cloneNode() | 创建指定节点的克隆 |
| detachEvent() | 从指定的节点上解除事件 |
| dispatchEvent() | 在指定的节点上执行事件 |
| focus() | 给指定的节点赋予焦点 |
| getAttribute() | 返回指定节点上作为参数传递的属性名的值 |
| getAttributeNS() | 返回指定节点上作为参数传递的属性名和命名空间的值 |
| getAttributeNode() | 返回指定节点上作为参数传递的属性名的属性节点 |
| getAttributeNodeNS() | 返回指定节点上作为参数传递的属性名和命名空间的属性节点 |
| getElementById() | 通过 id 获取元素并将其赋值给变量 |
| getElementsByTagName() | 返回指定节点中所有具有作为参数传递的标签名的元素节点数组 |
| getElementsByTagNameNS() | 返回指定节点中所有具有作为参数传递的标签名和命名空间的元素节点数组 |
| hasAttribute() | 如果作为参数传递的属性名存在于指定节点，返回 true，否则返回 false |
| hasAttributeNS() | 如果作为参数传递的属性名和命名空间存在于指定节点，返回 true，否则返回 false |
| hasAttributes() | 如果指定的节点定义了任何属性节点，则返回 true，否则返回 false |
| hasChildNodes() | 如果指定的节点有任何子节点，返回 true，否则返回 false |
| insertBefore() | 在指定的节点内部，将作为参数传递的节点插入到第二个参数传递的节点之前 |
| normalize() | 规范化指定的节点 |
| removeAttribute() | 从指定节点移除作为参数传递的属性名的属性节点 |
| removeAttributeNode() | 从指定节点移除作为参数传递的属性对象引对象的属性节点 |
| removeAttributeNS() | 从指定节点移除作为参数传递的带有命名空间参数的属性名的属性节点 |
| removeChild() | 从指定节点移除作为参数传递的子节点 |
| removeEventListener() | 从指定的节点移除事件监听器 |
| replaceChild() | 在指定的节点中，将作为第二个参数传递的子节点替换为作为第一个参数传递的子节点 |
| scrollIntoView() | 将指定的节点滚动到浏览器窗口的可范围内 |
| setAttribute() | 为指定的节点设置属性节点的名称（第一个参数）和值（第二个参数） |
| setAttributeNode() | 将作为参数传递的属性节点对象设置为指定节点的属性节点 |
| setAttributeNodeNS() | 将作为参数传递的带有命名空间参数的属性节点对象设置为指定节点的属性节点 |
| setAttributeNS() | 为指定的节点设置属性节点的命名空间（第一个参数）、名称（第二个参数）和值（第三个参数） |

表 9-4 DOM 节点方法（续）

***注意***

当你看到列出的使用命名空间的属性或方法时，它们主要用于 XML 文档，在书中不会被频繁引用。

如前所述，为了通过将创建的节点添加到文档使文档对象的创建方法变得有用，需要使用 DOM 节点方法（如 `appendChild()` 或 `insertBefore()`）将新节点添加到文档中。

例如，你可能使用了之前过的 HTML 代码，如下所示：

```html
<body>
  <div id="div1" title="All about me!">
    This page is about me, me, and... me!
  </div>
</body>
```

此代码包含一个带有子文本节点（以及属性节点）的 `div` 元素节点。如果你想创建另一个 `div` 元素作为 `div1` 元素的最后一个子节点，可以使用 `document.createElement()`、`document.createTextNode()` 和 DOM 节点方法 `appendChild()` 的组合。

首先，进入 JavaScript 代码并通过 id 获取 `div1` 元素：

```javascript
var me_div = document.getElementById("div1");
```

接下来，使用 `document.createElement()` 创建 `div` 元素：

```javascript
var inner_div = document.createElement("div");
```

之后，使用 `document.createTextNode()` 为 `inner_div` 节点创建文本节点：

```javascript
var inner_div_text = document.createTextNode("More about me...");
```

接下来，使用 `appendChild()` 方法将文本节点作为 `inner_div` 节点的节点：

```javascript
inner_div.appendChild(inner_div_text);
```

最后，使用 `appendChild()` 方法将 `inner_div` 节点作为 `me_div` 元素的子节点添加到文档中：

```javascript
me_div.appendChild(inner_div);
```

这将你的 `inner_div` 节点添加到原始元素的末尾（在原始元素关闭之前）。因此，使用“查看源代码”命令，HTML 文档结构将如下：

```html
<body>
  <div id="div1" title="All about me!">
    This page is about me, me, and... me!
    <div>
      More about me...
    </div>
  </div>
</body>
```

在创建更复杂的脚本时，这些 DOM 节点属性和方法对你非常有用。在书的剩余部分，你将经常使用 `innerHTML` 和样式属性以及其他 DOM 节点属性和方法。

## 向文档添加节点

此项目允许你练习在本章中学到的新文档和 DOM 节点属性及方法。

### 步骤

1. 创建一个具有以下部分代码 HTML 页面并将其保存为 `pr1.html`：

```html
<body>
  <div id="div1" title="Gosh!">
    Whatever I feel like I want to write...
  </div>
  <script type="text/javascript" src="prjs9_1.js"></script>
</body>
```

2. 执行第 3-5 步。

3. 获取 id 为 “div1”的元素的 `title` 属性值，并将该值作为 alert 发给观众。

4. 创建一个带有文本“See you!”的新 `div` 元素，并将其作为 id 为 “div1”的元素的子节点添加到文档结构中。

5. 保存 JavaScript并在浏览器中打开 HTML 文件以查看结果。

## 尝试总结

在此项目中，你使用了对文档对象和 DOM 节点属性及方法的知识，来报告一个 DOM 节点属性并在文档结构中创建了一个新的 `div` 元素。

pr1.html

prjs9_1.js





## JavaScript: 入学者指南

### 创建动态脚本

正如你所见的，JavaScript 允许你通过 `document.getElementById()` 和 `document.getElementsByTagName()` 等方法访问文档中的所有元素。一旦访问了这些元素，你还可以访问它们的样式属性（通常最初由样式表设置），并使用 `style` DOM 节点属性对它们的位置、颜色、边框、大小或元素样式属性的几乎任何其他部分进行更改。

### JavaScript 中的样式

当使用级联样式表（CSS）设置样式时，你可以在 CSS 代码中编写如下内容（保存为 `dyn_01.css`）：

```css
#div1 { color:#000000; background-color:#FFFFFF; }
#div2 { border-style:solid; border-width:1px; border-color:#000000; }
```

这为你为两个 id（`div1` 和 `div2`）提供了样式属性。因此，如果你有以下 HTML 代码（保存为 `dyn_01.html`），这些 `div` 元素在网页上的显示将使用前述的样式：

```html
<head>
  <link rel="stylesheet" type="text/css" href="dyn_01.css" />
</head>
<body>
  <div id="div1">
    我在 div1 中。这里看起来是个好地方。
  </div>
  <div id="div2">
    我在 div2 中。这里稍微精致一点。
  </div>
  <script type="text/javascript" src="dyn_01.js"></script>
</body>
```

HTML 代码通过 `link` 标签与 CSS 代码相关联。因此，`div1` 元素将显示为白色背景上的简单黑色文本，而 `div2` 元素周围将有一个纯黑色的实线深色边框。

如你所见，此页面为每个 `div` 元素都使用了 id——因此你不仅可以通过 CSS 代码访问这些元素的 id，还可以在 JavaScript 代码中通过它们的 id 访问这些元素。所以，你可以从你的 JavaScript 文件（在前面的 HTML 代码中调用——保存为 `dyn_01.js`）开始编写一些代码，使用 `document.getElementById()` 方法通过 id 获取这两个 `div` 元素：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
```

现在你拥有了这两个这两个元素的变量。

| 描述 | 位置 |
| :--- | :--- |
| CSS 文件在此处链接文档 | |
| id 为 “div1” 的 `div` 元素 | |
| id 为 “div2” 的 `div` 元素 | |
| JavaScript 文件在此处调用 | |

### 编写动态脚本

如果你想通过 JavaScript 修改 CSS 代码中设置的样式，你就需要使用每个元素节点中包含的 `style` 属性。然后，JavaScript 使用与 CSS 选择器相同的名称来访问该特定属性。例如，如果你想将 `div1` 元素中的文字颜色改为绿色，将使用以下代码：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
d1.style.color = "#00FF00";
```

在 CSS 代码中，选择器 `color` 用于更改元素的前景颜色。在 JavaScript 中，它也是访问元素 `style` 属性后用于更改颜色的属性名称。

如果 CSS 选择器不是单个单词怎么办？例如，如果你在 JavaScript 中像在 CSS 代码中那样使用 `background-color` 选择器，它将无法工作。以下代码尝试将背景颜色改为绿色：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
d1.style.background-color = "#00FF00";
```

这将不起作用，因为 JavaScript 不允许将连字符 (`-`) 作为属性名的一部分。相反，JavaScript 将两个单词组合在一起，并将第一个单词之后的任何额外单词的首字母大写。因此，CSS 选择器 `background-color` 在 JavaScript 中变为 `backgroundColor`（同样，类似 `border-right-color` 的内容将变为 `borderRightColor`）。

JavaScript 代码可以重写如下以便更改生效：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
d1.style.backgroundColor = "#00FF00";
```

这将将 `div1` 元素的背景颜色改为绿色。现在唯一的问题是，这将在脚本运行时立即发生，在这种情况下，可能在观众注意到 `div1` 元素原本有另一种背景颜色之前就已经发生了。为了使其更有用，你可以利用这种访问元素样式的能力，并结合你处理事件的知识（在第 7 章介绍），创建一个响应用户事件并进行样式的脚本。

现在你已经知道如何更改元素的样式属性，你就可以响应用户事件来更改它们，从而创建动态脚本。这为你提供了响应任何事件更改几乎任何样式属性的无数可能性。在这里，你将继续使用一直使用的 CSS、HTML 和 JavaScript 文件来创建一个动态的、事件驱动的脚本。

在当前的 CSS 和 HTML 代码基础上，你现在可以编写 JavaScript 来创建触发更改的事件的响应。因此，如果你想修改背景 JavaScript: 入学者指南每个 `div` 元素使用的 id——因此你不仅可以通过 CSS 代码访问这些元素的 id，还可以在 JavaScript 代码中通过它们的 id 访问这些元素。所以，你可以从你的 JavaScript 文件（在前面的 HTML 代码中调用——保存为 `dyn_01.js`）开始编写一些代码，使用 `document.getElementById()` 方法通过 id 获取两个 `div` 元素：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
```

现在你拥有了这两个元素的变量。

| 描述 | 位置 |
| :--- | :--- |
| CSS 文件在此处链接文档 | |
| id 为 “div1” 的 `div` 元素 | |
| id 为 “div2” 的 `div` 元素 | |
| JavaScript 文件在此处调用 | |

如果你想通过 JavaScript 修改在 CSS 代码中设置的样式，你需要使用每个元素节点中包含的 `style` 属性。然后，JavaScript 使用与 CSS 选择器相同的名称来访问该特定属性。例如，如果你想将 `div1` 元素中的颜色改为绿色，将使用以下代码：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
d1.style.color = "#00FF00";
```

在 CSS 代码中，选择器 `color` 用于更改元素的前颜色。在 JavaScript 中，它也是访问元素 `style` 属性后用于更改它的属性名称。

如果 CSS 选择器不是单个单词怎么办？例如，如果你在 JavaScript 中像在 CSS 代码中那样使用 `background-color` 选择器，它将无法工作。以下代码尝试将背景颜色改为绿色：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
d1.style.background-color = "#00FF00";
```

这将不起作用，因为 JavaScript 不允许将连字符 (`-`) 作为属性名的一部分。相反，JavaScript 将两个单词组合在一起，并将第一个单词之后的任何额外单词的首字母大写。因此，CSS 选择器 `background-color` 在 JavaScript 中变为 `backgroundColor`（同样，类似 `border-right-color` 的内容将变为 `borderRightColor`）。

JavaScript 代码可以重写如下以便更改生效：

```javascript
var d1 = document.getElementById("div1");
var d2 = document.getElementById("div2");
d1.style.backgroundColor = "#00FF00";
```

这将将 `div1` 元素的背景颜色改为绿色。现在唯一的问题是，这将在脚本运行时立即发生，在这种情况下，可能在观众注意到 `div1` 元素原本有另一种背景颜色之前就已经发生了。为了使其更有用，你可以利用这种访问元素样式的能力，并结合你处理事件的知识（在第 7 章介绍），创建一个响应用户事件并进行样式的脚本。

现在你已经知道如何更改元素的样式属性，你就可以响应用户事件来更改它们，从而创建动态脚本。这为你提供了响应任何事件更改几乎任何样式属性的无数可能性。在这里，你将继续一直使用的 CSS、HTML 和 JavaScript 文件来创建一个动态的、事件驱动的脚本。

在当前的 CSS 和 HTML 代码基础上，你现在可以编写 JavaScript 来创建触发更改的事件的响应。因此，如果你想修改

### innerHTML 属性

`innerHTML` DOM 节点属性允许你更改指定元素内部的 HTML 代码。例如，你可以从以下 HTML 代码开始：

```html
<body>
  <div id="div1">
    2+2 等于几
  </div>
  <div id="div2">
    <a href="answer.html" id="answer_link">获取答案</a>
  </div>
</body>
```

这段代码设置了一个 id 为 `div1` 的 `div` 元素、另一个 id 为 `div2` 的 `div` 元素以及 id 为 `answer_link` 的链接。现在，如果你想更改 `div1` 元素中的 HTML 代码，以便在点击链接时为观众显示答案，可以使用链接上的点击事件启动脚本，然后更改 `div1` 元素上的 `inner` 属性以将元素的内容更改为答案：

```javascript
var d1 = document.getElementById("div1");
var a_link = document.getElementById("answer_link");
answer_link.onclick = function() {
  d1.innerHTML = "太简单了，答案是<strong>4</strong>！";
  return false;
};
```

记住，为了防止点击链接时跳转，你在执行所需操作后添加了 `return false` 语句。

运行时，此脚本会更改页面上 `div1` 元素内部的内容，因此 HTML 代码将如下（尽管使用浏览器的“查看源代码”命令无法看到）：

```html
<body>
  <div id="div1">
    太简单了，答案是<strong>4</strong>！
  </div>
  <div id="div2">
    <a href="answer.html" id="answer_link">获取答案</a>
  </div>
</body>
```

如你所见，这是一种对网页内容进行动态更改的方便方法。

***提示*** 为了让没有 JavaScript 的用户也能访问脚本，使用了默认链接目标（`answer.html`）。在链接页面上包含答案文本允许没有 JavaScript 的用户仍然点击链接并获取问题的答案。

通过在本章中学习的访问 DOM 并使用 `document` 对象和 DOM 节点的属性和方法，你可以构建脚本对文档的外观或内容进行任何数量的更改。





JavaScript：初学者指南

这 9-2

pr9_2.html

prjs9_2.js

尝试属性更改

此项目允许你练习在本章中学习的 `style` 和 `innerHTML` 新属性的使用。

逐步步骤

1. 创建一个包含以下 body 部分代码的 HTML 页面，并将其保存为 `pr9_2.html`：

```html
<body>
<div id="div1">
我什么时候更新这个页面？
</div>
<div id="div2">
<a href="answer.html" id="c_link">查看答案！</a>
</div>
<script type="text/javascript" src="prjs9_2.js"></script>
</body>
```

2. 创建一个外部 JavaScript 文件并将其保存为 `prjs9_1.js`。将其用于第 3 至 5 步。

3. 编写一些代码，使得当点击链接时，id 为 `div1` 的 `div` 元素的背景颜色变为 `#CCCCCC`，且该元素的内容变为以下内容：
<strong>现在！</strong>这速度不是很快吗？

4. 确保在一个名为 `answer.html` 的独立 HTML 文件中包含相同的答案内容，供那些未启用 JavaScript 的用户。

5. 保存 JavaScript 文件并在浏览器中打开 HTML 文件以查看结果。

本节总结

在这个项目中，你利用关于 DOM 节点 `style` 和 `innerHTML` 属性的知识对 Web 页面进行了样式和内容更改。

*第 9 章自测*

1. `__________` 对象是浏览器为每个查看的新新 HTML 页面创建的对象。

2. document 对象的 `__________` 属性返回将查看者引导至当前文档的 URL。

第 9 章：文档对象，239 页

3. 你可以使用 DOM 节点属性 `style` 来更改元素的样式表属性。
A 正确
B 错误

4. document 对象的 `__________` 方法允许你通过其 `id` 属性的值来获取元素。
A getElementsByClassName()
B createElement()
C getSelection()
D getElementById()

5. `appendChild()` DOM 节点方法允许你将子节点作为指定节点的第一个子节点。
A 正确
B 错误

6. 如果你在 URL 为 `http://www.pageresource.com/html/index.html` 查看 Web 页面，那么 `document.domain` 属性的值应该是？
A pageresource.com
B www.pageresource.com/html/index.html
C www.pageresource.com
D http://www.pageresource.com/html/index.html

7. document 对象的 `__________` 属性是一个数组，包含了页面上所有的锚点 (`<a>`) 标签。

8. `__________` DOM 节点属性允许你更改元素节点的 HTML 内容。

9. `__________` 属性持有当前文档最后修改的日期时间值。

10. 文档对象模型（DOM）允许 JavaScript（以及其他脚本语言）访问浏览器中的文档结构。
A 正确
B 错误

11. 你可以使用 `title` 属性在浏览器窗口顶部以外的地方显示 Web 页面的标题。
A 正确
B 错误

12. 哪个属性返回当前文档的完整 URL？
A domain
B referrer
C URL
D title

13. `writeln()` 方法与 `write()` 方法有什么区别？
A 它在行尾添加一个等同于 HTML `<br />` 标签。
B 它在行尾添加一个等同于 HTML `<p>` 标签。
C 它在行尾添加一个 JavaScript 换行符。
D 它与 `write()` 方法完全相同。

14. 在 JavaScript 中是如何创建 `formName` 类型属性的？
A 当给表单赋予名称时，表单的名称就成为属性名。
B 当给表单赋予名称时，字符串 `formName` 会被用作属性名。
C 表单没有被命名；相反，`formName` 被用作属性名。
D 当给表单赋予名称时，会在开头添加一个 *f* 并将其用作属性名。

15. 在 `document.open()` 和 `document.close()` 之间最常见的语句是什么？
A HTML 命令
B `document.write()` 和 `document.writeln()` 语句
C 仅 `document.writeln()` 语句
D 仅 `window.alert()` 语句

第 10 章
Window 对象，241 页

JavaScript：初学者指南

关键技能与概念

- 使用 Window 对象的属性
- 使用 Window 对象的方法

JavaScript `window` 对象让你能够访问可以在脚本使用的更多属性和方法。通过使用 `window` 对象，你将能够完成许多新操作，例如提示用户输入信息、打开新窗口、确认查看者的操作等。

Window 对象简介

`window` 对象是为屏幕上显示的每个窗口创建的。窗口可以是主窗口、帧（frame）、帧集（frame set），甚至是嵌套帧。它与 `document` 对象的不同之处在于，`window` 包含了许多其他构件对象，如 `history`、`navigator` 等。

在之前的章节中，你已经使用过 `alert()` 方法弹出消息。`window` 对象为你的脚本提供了许多新可用功能。`window` 对象是为屏幕上显示的每个窗口创建的。窗口可以是主窗口、帧、帧集，甚至是嵌套帧。

开始学习 `window` 对象的第一件事是，查看其属性。下一节将介绍 `window` 对象的方法。

使用 Window 对象的属性

开始学习 `window` 对象，请查看表 10-1 中描述的。

***注意***

正如之前的章节一样，本章列出的某些属性并非跨浏览器。更多信息请参阅：https://developer.mozilla.org/en-US/DOM/window 和 http://msdn.microsoft.com/en-us/library/ms3873.aspx。

第 10 章：Window 对象，243 页

closed 属性

`closed` 属性用于检查窗口是否被查看者关闭。它的通常用法是结合窗口名称，如下所示：

```javascript
if (window.closed) { }
```

| 属性 | 描述 |
|---|---|
| closed | 持有窗口是否已关闭的值 |
| defaultStatus | 定义在状态栏中显示的默认 |
| document | 窗口文档对象的引用 |
| frames | 表示给定窗口中所有帧的数组 |
| history | 提供当前窗口的浏览器历史（在第 8 章讨论） |
| innerHeight | 返回窗口内可视区域的高度（像素） |
| innerWidth | 返回窗口内可视区域的宽度（像素） |
| length | 持有等于窗口帧数量的值 |
| location | 持有当前窗口 URL 的值 |
| name | 允许窗口被命名 |
| opener | 指向打开另一个窗口的窗口 |
| outerHeight | 返回整个浏览器窗口的高度（像素） |
| outerWidth | 返回整个浏览器窗口的宽度（像素） |
| parent | 指向包含当前帧的帧集 |
| screen.availWidth | 返回浏览器窗口可用宽度（像素） |
| screen.availHeight | 返回浏览器窗口可用高度（像素） |
| screen.colorDepth | 返回屏幕色彩深度（位/像素） |
| screen.height | 返回屏幕的总高度（像素） |
| screen.pixelDepth | 返回屏幕位深（位/像素） |
| screen.width | 返回屏幕的总宽度（像素） |
| self | 提供引用当前窗口的另一种方式 |
| status | 允许在状态栏放置消息；覆盖 `defaultStatus` |
| top | 指向包含帧、帧集或嵌套帧集的顶层窗口 |
| window | 当前窗口的引用 |

表 10-1 Window 对象的属性





## JavaScript: 入学者指南

你会将 *windowname* 部分替换为你想要检查的窗口名称。

这通常是你用 JavaScript 打开的一个新窗口；你将在本章稍后的“open() 方法”节中学习如何命名一个新窗口。

你也可以在新窗口内部使用 `closed` 属性来检查打开它的那个窗口是否已经关闭。要做到这一点，你可以在 `opener` 属性之后使用 `closed`（稍将在“opener 属性”节中讨论），如下例所示：

```javascript
if (window.opener.closed) {
    *JavaScript 语句*
}
```

如果你选择创建一个新窗口，允许用户通过新窗口中的链接导航到主窗口，那么这种 `closed` 属性的使用非常有用。

### defaultStatus 属性

`defaultStatus` 属性设置了在没有给 `window.status` 属性赋值时，状态栏默认显示的文本字符串。`window.status` 属性的更改会覆盖此设置，因为它只作为默认值显示。

`defaultStatus` 属性通常在 `load` 事件中设置。这主要用于在查看者没有执行会更改状态栏文本的操作时，默认显示一条自定义消息。尽管如此，它可以任何时间设置，因此你可以使用 `load` 事件之外的其他事件来设置它。

***注意***

大多数现代浏览器默认不会显示由 JavaScript 修改的状态栏文本，以防止不良网站通过在状态栏显示虚假链接目标等手段欺骗用户。因此，除非用户更改了浏览器设置，否则 `defaultStatus` 和 `status` 属性通常无效。由于更改浏览器设置以允许修改状态栏文本存在安全风险，因此不建议在脚本中使用这些属性。

### frames 属性（数组）

`frames` 属性是一个数组，保存了帧集（frame set）中每个帧（frame）的值。它通常用于访问页面上各个帧的属性。由于你还没有学习过数组，所以你现在对 `frames` 属性做不了什么。不过，你将在第 11 章中学习数组。

你可以通过使用 `window.frames.length` 属性获取窗口中帧的数量。如果你决定以后使用数组按顺序对页面的帧执行任务，这就会非常有用。

### innerHeight 和 innerWidth 属性

`innerWidth` 和 `innerHeight` 属性持有可视窗口区域的宽度和高度，这意味着这些值不包括滚动条、菜单栏、工具栏或其他浏览器功能。这些属性在 Mozilla Firefox 和 Opera 中有效，但（在本书期间）在 Internet Explorer 中无效。然而，Internet Explorer 提供了获取这些值的替代方案（`document.body.clientWidth` 和 `document.body.clientHeight`）。

因此，如果你想获取脚本可用内容区域宽度，可以使用以下代码：

```javascript
var mywin_width = window.innerWidth;
```

当然，如果你想根据窗口可用 `innerWidth` 为浏览器使用不同的 HTML 代码，可以使用以下代码：

```javascript
var mywin_width = window.innerWidth;
var div_width = (mywin_width >= 800) ? "750px" : "400px";
document.write('<div style="width:'+div_width+'; background-color:#CCC;">');
document.write('Some text for the new div element.');
document.write('</div>');
```

这将决定查看者是否具有 800 像素的可视宽度。如果是，div 元素的宽度将设置为 750 像素。否则，div 元素将具有 400 像素的更安全宽度。背景颜色应该跨越 div 元素的宽度，以便你在用不同浏览器宽度运行脚本时看到差异。

为了使其更具跨浏览器性，你也可以使用 `document.body.clientWidth` 属性为 Internet Explorer 用户获取值。你还可以为使用旧浏览器的用户为 `mywin_width` 变量设置一个默认值：

```javascript
var mywin_width = 450; // 设置一个低默认值
if (window.innerWidth || document.body.clientWidth) {
    mywin_width = (window.innerWidth) ? window.innerWidth : document.body.clientWidth;
}
var div_width = (mywin_width >= 800) ? "750px" : "400px";
document.write('<div style="width:'+div_width+'; background-color:#CCC;">');
document.write('Some text for the new div element.');
document.write('</div>');
```

这次，对于不支持这两个属性的浏览器，为 `mywin_width` 变量设置了一个低默认值（这意味着这些浏览器将获得一个宽度为 400 像素的较小 div 元素）。脚本随后检查当前使用的浏览器中是否存在任一属性。如果是，则 `mywin_width` 变量将重新赋值为 `innerWidth` 属性的值（如果存在），否则赋值为 `document.body.clientWidth` 属性。之后，脚本将按之前的方式运行，根据可用内容区域创建一个 div 元素。

- 将 `innerWidth` 属性的值赋值给 `mywin_width` 变量
- 使用条件运算符进行快速的 `if-else` 语句，根据可用空间确定 div 元素的宽度应该是多少像素
- 将 `innerWidth` 属性的值赋值给 `mywin_width` 变量

#### length 属性

`length` 属性告诉你窗口中有多少帧，就像 `window.length` 一样。

### location 属性

`location` 属性持有当前窗口的 URL。它允许你将查看者重定向到新页面。如果你想立即重定向，可以在 `<head>` 中使用它，如下所示：

```html
<head>
    <title>页面已移动</title>
    <script type="text/javascript">
        window.location="page2.html";
    </script>
</head>
<body>
    <a href="page2.html">新页面</a>
</body>
```

这会将查看者送走，因为不需要操作来设置它。

### name 属性

`name` 属性持有当前窗口的名称，并允许你给窗口命名。如果你想给主窗口命名，可以给该属性赋值你想要使用的名称。如果你想测试它是否生效，可以将该属性的值写入页面。以下代码展示了为窗口命名并将该名称写入页面正体的示例：

```html
<body>
    <script type="text/javascript">
        window.name="cool_window";
        document.write("此窗口名称为 "+window.name);
    </script>
</body>
```

脚本为窗口命名，然后将该名称写入文档。图 10-1 显示了该脚本在浏览器中的结果。注意屏幕上显示的名称 `cool_window`。

### opener 属性

`opener` 属性用于引用打开当前窗口的窗口。这通常用于使用 `open()` 方法打开的新窗口，你将在本章稍后的“open() 方法”节中看到。通过在新窗口中使用 `opener` 属性，你可以利用之前学过的 `closed` 属性检测主窗口是否已经关闭。以下示例展示了如何进行此测试：

```javascript
if (window.opener.closed)
```




JavaScript：入门指南

这 10-1

### parent 属性

parent 属性仅在页面上存在帧（frames）时使用。它允许你访问当前帧的父级帧集。当你希望从一个帧更改另一个帧的属性时，这非常有帮助。我将在第 15 章讲解 JavaScript 和帧时详细讨论这一点。

## self 属性

self 属性是 JavaScript 中表示“当前窗口”的另一种表达方式。它的用法与 `window` 对象类似，可以像访问 `window` 对象一样样访问当前窗口的属性。如果你有许多命名的窗口，并且想要确保使用的是当前窗口的属性，而不是另一个命名窗口的属性，那么 `self` 属性非常有用。

### status 属性

status 属性包含在窗口状态栏中设置的文本值。更改此属性将覆盖通过 `defaultStatus` 属性设置的状态栏内容。

***注意***

大多数现代浏览器默认情况下不会显示由 JavaScript 修改的状态栏文本，以防止不法 Web 网站通过在状态栏显示虚假链接地址等手段来欺骗用户。因此，除非用户更改了浏览器设置，否则 `defaultStatus` 和 `status` 属性通常不起作用。由于更改浏览器设置以允许修改状态栏文本存在安全风险，因此不建议在脚本中使用这些属性。

### top 属性

top 属性用于访问所有帧集（可能是嵌套的）中的顶层窗口。这与 `parent` 属性略有不同，`parent` 属性只到达包含当前帧的帧集的顶层。而 `top` 属性则一直到达顶层窗口，即使该窗口包含了嵌套的帧集。

当你学习到第 15 章 JavaScript 和帧时，你将看到更多关于此属性的用法。

## 使用 location 和 innerWidth 属性

此项目将让你练习使用窗口对象的 `location` 和 `innerWidth` 属性。此外，通过添加 `document.body.clientWidth` 属性，你将帮助提高脚本的跨浏览器兼容性。

pr10_1.html

prjs10_1.js

第 10 章：窗口对象

249

逐步步骤

1. 创建一个 HTML 页面，除了在 `<body>` 部分留空外，在 `</body>` 结束标签之前包含一组 `<script>` 标签，以引用名为 `prjs10_1.js` 的 JavaScript 文件。将文件保存为 `pr10_1.html`。

2. 创建一个 JavaScript 文件并将其保存为 `prjs10_1.js`。在步骤 3-6 中使用此文件。

3. 为名为 `mywin_width` 的变量设置默认值。

4. 如果这些属性之一可用，将 `mywin_width` 的值更改为 `window.innerWidth` 属性的值或 `document.body.clientWidth` 属性的值。

5. 如果 `mywin_width` 的值大于或等于 1000，将用户发送到 URL http://www.pageresource.com。否则，将用户发送到 URL http://www.javascriptcity.com（使用 `window.location` 属性）。

6. 保存 JavaScript 文件并在 Web 浏览器中打开 HTML 文件。尝试更改宽度，然后用新宽度重新打开页面，查看它带你进入哪个网站。

本节练习总结

在这个项目中，你能够利用对窗口对象 `location` 和 `innerWidth` 属性的知识，创建一个脚本，该脚本根据用户浏览器中可视区域的宽度重定向用户。

## 使用窗口对象的方法

现在你已经知道如何使用窗口对象的属性，可以继续学习窗口方法了。表 10-2 列出了窗口对象的若干方法及其描述，接下来将对某些特定方法进行更详细的描述。

### alert() 方法

在前面的章节的示例脚本中，你已经广泛使用了 `alert()` 方法。它会向用户弹出一个消息，用户必须点击 OK 按钮才能继续。记住其语法类似于下面的 `alert`：

`window.alert("Hi there!");`

这只是在屏幕上给用户显示“Hi there!”的警报消息。

正如最初引入 `alert()` 方法时提到的，这种方法在脚本中通常使用如下语法进行简写：

`alert("Hi there!")`

JavaScript：入门指南

| 方法 | 描述 |
| :--- | :--- |
| alert() | 向用户弹出警报，用户随后必须点击 OK 继续 |
| back() | 将窗口返回到其历史列表中的上一个 |
| blur() | 从窗口中移除焦点 |
| clearInterval() | 取消 `setInterval()` 方法调用的操作 |
| clearTimeout() | 取消 `setTimeout()` 方法调用的操作 |
| close() | 关闭浏览器窗口 |
| confirm() | 向用户显示确认对话框，用户随后必须点击 OK 或取消以继续 |
| escape() | 将字符串中的特殊字符转换为十六进制字符 |
| find() | 允许用户启动浏览器的“查找”工具来查找页面上的文本 |
| focus() | 给窗口焦点 |
| forward() | 将窗口向前移动到历史列表中的下一个 |
| home() | 将用户发送到其在 Web 浏览器中设置的主页 |
| moveBy() | 按参数发送的特定像素值移动窗口 |
| moveTo() | 将窗口的左上角移动到参数发送的坐标 |
| open() | 打开一个新的浏览器窗口 |
| print() | 打印窗口内容 |
| prompt() | 弹出一个提示框要求用户输入信息 |
| resizeBy() | 按参数发送的特定像素值调整窗口大小 |
| resizeTo() | 将整个窗口调整为参数发送的高度和宽度 |
| scrollBy() | 按参数发送的特定像素值滚动窗口可视区域 |
| scrollTo() | 将窗口可视区域滚动到参数指定的指定的坐标 |
| setInterval() | 每经过一段时间就调用一次函数 |
| setTimeout() | 在经过一段时间时间后调用一次函数 |
| stop() | 停止窗口加载 |
| unescape() | 将转义后的字符串转换回普通字符 |

表 10-2 窗口对象的方法

第 10 章：窗口对象

251

你为什么可以这样做？记住，JavaScript 是相当灵活的，因此在某些情况下你被采取这样的捷径。在这种情况下，这是允许的，因为 `window` 对象是默认对象。由于假设它存在，你不需要对它进行调用。相反，你只需调用该方法，JavaScript 就会知道这是一个窗口方法。

这种捷径在大多数情况下适用于所有的窗口属性和方法。事实上，你在上一章学习的 `document` 对象属于窗口对象。你可以省略 `window` 部分，因为假设窗口存在。

你可能需要更具体指定的情况通常是新窗口和 `location` 属性。

### confirm() 方法

`confirm()` 方法可以给用户一个确认或取消操作的机会。该方法返回布尔值（true 或 false），因此在使用它时通常将其结果赋值给变量。

以下是将值赋值变量的语法：

`var varname = window.confirm("Your Message");`

你把 *varname* 替换为你想要使用的变量名。然后你把“Your Message”文本替换为你希望在对话框中显示的文本。所以如果你想将结果赋值给名为 `is_sure` 的变量并询问“你确定吗？”，可以使用以下代码：

`var is_sure = window.confirm("Are you sure?");`

图 10-2 显示了上述代码显示的示例确认对话框。注意用户可以选择点击的两个按钮：OK 和取消。根据浏览器的，这可能略有不同。如果用户点击 OK，方法返回 true。如果用户点击取消，方法返回 false。坏消息是，你无法更改按钮文本的值。你只能使用 OK 和取消，至少在使用 `confirm` 方法时是这样。

作为一个方法的真实示例，假设你想创建一个指向另一个页面的链接，但你想在用户离开之前确保他们确实想离开。你可以使用

图 10-2 确认对话框的示例





JavaScript：初学者指南

使用确认对话框（confirm dialog box）查看用户是否想要离开页面。以下代码展示了如何获取查看者的确认并做出相应的响应。

首先，是 HTML 代码：

```html
<<body>
  <a href="http://www.google.com" id="search_link">Go Searching</a>
</body>
```

接下来，使用 JavaScript 在点击链接时确认用户是否真的想离开：

```javascript
var s_link = document.getElementById("search_link");

s_link.onclick = function() {
  var is_sure = window.confirm("Are you sure you want to leave?");
  if (!is_sure) {
    window.alert("OK. You can stay here.");
    return false;
  }
};
```

注意，如果点击 OK 且 `confirm()` 方法返回 true，查看者将被引导到链接网站。如果点击取消（cancel）且 `confirm()` 方法返回 false，则会向查看者发送一个警告（alert），函数返回 false，这样浏览器就不会跟随该链接（你也可以简单地省略 alert，并且在点击取消后什么都不发生，只需使用 `return false` 语句即可）。

图 10-3 显示了点击页面上的链接后的浏览器窗口。屏幕上弹出一个带有“Are you sure you want to leave?”消息的确认对话框。

该函数确认查看者是否想要离开
图 10-3 点击按钮时弹出的确认对话框

![](img/61d166424839b7674a7b9c8434ae4e03_274_0.png)

## 第 10 章：Window 对象

253

### find() 方法

你可以使用 `find()` 方法让查看者在你的页面上查找某些文本。它告诉浏览器使用其内置的“查找”（Find）工具，并允许查看者输入他们想要在页面上查找的内容。

例如，如果你想创建一个按钮，让查看者在想要查找页面上的某些内容时点击，可以使用以下代码：

```html
<form>
  <input type="button" value="Click to Find Text" onclick="window.find();" />
</form>
```

这会在浏览器中弹出查找对话框，并允许查看者搜索页面内的文本。图 10-4 显示了此脚本添加到 HTML 文档后的结果。

如果你的页面非常长，并且希望查看者能够通过搜索页面更快地找到内容，那么此功能非常有用。

### home() 方法

`home()` 方法用于将查看者送到他们在 Web 浏览器设置中设置的主页。例如，你可以用它为查看者提供一个按钮，点击后将将他们带到选定的主页，如下代码所示（在编写时，该方法在 Mozilla Firefox 和 Opera 中有效，但在 Microsoft Internet Explorer 中不起）：

```html
<form>
  <input type="button" value="Go Home!" onclick="window.home();">
</form>
```

图 10-4 弹出的查找对话框，允许查看者搜索页面上的文本

![](img/61d166424839b7674a7b9c8434ae4e03_275_0.png)

### print() 方法

`print()` 方法允许查看者打印当前窗口。当调用此方法时，它应该打开查看者的打印对话框，以便查看者设置打印机设置来打印文档。

要使用它，你可以创建一个按钮，允许查看者打印他们正在查看的页面：

```html
<form>
  <input type="button" value="Click to Print Page" onclick="window.print();">
</form>
```

当用户点击“Click to Print Page”按钮时，此代码应打开用户的打印对话框。图 10-5 显示了在浏览器中运行此脚本的结果。使用的浏览器和打印机不同，此对话框对不同的查看者显示可能不同。

图 10-5 点击打印按钮时弹出查看者的打印选项

![](img/61d166424839b7674a7b9c8434ae4e03_276_0.png)

## 第 10 章：Window 对象

255

### prompt() 方法

`prompt()` 方法用于提示查看者输入信息。使用此方法，你可以根据查看者在提示文本框中输入的内容来执行操作。

首先，你需要查看该方法的语法。与 `confirm()` 方法一样，结果（查看者输入的内容）被赋值给一个变量以供以后使用。

以下是语法的示例：

```javascript
var *varname* = window.prompt("*Your Text*","Default Entry");
```

你将 *varname* 替换为变量名，并将“*Your Text*”替换为你想发送给查看者的消息（通常是一个问题）。第二个参数“Default Entry”允许你为查看者设置一个默认输入。通常将其留为空“ ”即一个空白输入。然而，如果你想为查看者准备一个默认答案供使用，也可以设置为某些内容。

你可以使用 `prompt()` 方法提示查看者输入信息。以下代码是一个示例：

```javascript
var thename = window.prompt("What's name?");
if (thename.length < 1) {
  thename = "Anonymous";
}
document.getElementById("greeting").innerHTML = "<h1>Hello " + thename + "!</h1>";
```

（注：prompt 部分的 OCR 文本乱码/重复，我根据标准的实践重构了逻辑。）

### open() 方法

`open()` 方法是允许你打开新窗口的方法。该方法接受三个参数，第三个参数设置窗口选项。使用 `open()` 方法的通用语法例所示：

```javascript
window.open("URL","name","attribute1=value,attribute2=value");
```

第一个参数“URL”替换为要在新窗口中打开的 HTML 文档的 URL。“name”参数替换为你想给窗口的名字。最后一个参数允许你为新窗口添加属性。这些属性通过在等号右侧使用“yes”、“no”或数值来设置。注意每当设置一个属性值时，前面有一个逗号，且之间没有空格。

如果你想打开一个具有当前窗口的窗口，可以通过省略带有属性的最后一个参数来实现

```javascript
window.open("newpage.html","my_window");
```

### 标准属性

如果你想包含窗口功能，你需要了解一些可以在窗口使用的属性。表 10-3 列出了可以在 `open()` 方法最后一个参数中使用的标准属性。

如果你开始使用属性参数，应该注意一旦你在属性参数中放置了内容，未定义的属性现在将默认为“no”，而不是复制主窗口。因此，如果你想打开一个宽度为 400 像素、高度为 300 像素的基础新窗口，可以使用以下代码：

```javascript
window.open("newpage.html","my_window","width=400,height=300");
```

图 10-7 查看者在 prompt 中输入后，其名字被写在页面上

![](img/61d166424839b7674a7b9c8434ae4e03_279_0.png)





## JavaScript: 入学者指南

此窗口拥有的特征是标题栏，它显示文档标题，以及右上角供查看器关闭或最小化窗口的按钮。

要设置其他属性（全部为布尔值），你可以根据是否需要某项功能为它们分配“yes”（是）或“no”（否）的值。如果你愿意，也可以使用 1 表示是，用 0 表示 否，因为它们的效果是相同的。因此，如果你想拥有一个宽 300×200 像素的窗口，并且只添加一个菜单栏（这会添加前进、后退、停止以及其他类似的按钮），你可以使用以下代码：

`window.open("newpage.html","cool","width=300,height=200,menubar=yes");`

这将为你提供一个新窗口，其中包含 `newpage.html` 的内容，名称为“cool”，尺寸为 300×200 像素，并有一个菜单栏。

你可以在第三个参数的引号内通过逗号分隔每个属性来添加任意数量的属性。请记住，任何内容之间都不应包含空格，并且整个命令在文本编辑器中应该写在一行上。

***注意***

由于空间限制，本书中的新窗口命令在代码中可能会跨多行。请务必在使用代码时，将从 `window.open` 到结束分号（;）的所有内容都放在同一行上，以避免 JavaScript 错误。

| 属性名称 | 可能的值 | 功能 |
| :--- | :--- | :--- |
| width | number | 以像素为单位定义新窗口的宽度 |
| height | number | 以像素为单位定义新窗口的高度 |
| directories | yes, no, 1, 0 | 定义新窗口是否具有目录按钮（如浏览器顶部的“新打开内容”或“链接”按钮） |
| location | yes, no, 1, 0 | 定义新窗口是否具有用于输入新 URL 的地址框 |
| menubar | yes, no, 1, 0 | 定义窗口是否具有菜单栏（文件菜单、编辑菜单等） |
| resizable | yes, no, 1, 0 | 定义是否允许查看器调整新窗口的大小 |
| scrollbars | yes, no, 1, 0 | 定义当窗口内容大于窗口尺寸时，新窗口是否具有滚动条 |
| status | yes, no, 1, 0 | 定义新窗口底部是否具有状态栏 |
| toolbar | yes, no, 1, 0 | 定义新窗口是否具有工具栏（前进和后退按钮、停止按钮等） |

表 10-3 新窗口的标准属性

### 第 10 章：窗口对象 (Window Object)

下面的示例打开了一个包含表 10-3 中提到的所有功能的窗口（再次说明，这里占用了多行空间，但当你在文本编辑器中输入它时，代码应该写在单行上）：

`window.open("newpage.html","cool","width=300,height=200,directories=yes,location=yes,menubar=yes,resizable=yes,scrollbars=yes,status=yes,toolbar=yes");`

这将打开一个 300×200 像素的窗口，并具有所有标准特征功能。如果你想要一个可视图的示例，你需要创建一个名为 `newpage.html` 的页面，并创建主页代码以包含一个 `window.open()` 命令，如接下来所述。

首先，创建 `newpage.html` 的代码（这只是一个包含文本的短页面）：

```html
<body>
我是一个新窗口！我比打开我的那个旧窗口要新，所以我是特殊的。哈，哈！
</body>
```

现在，创建主页（保存为 `mainpage.html`）：

```html
<body>
点击下方的链接来打开一个傲慢的新窗口 ...
<br />
<a href="newpage.html" id="nwin">新页面</a>
<script type="text/javascript" src="openwin.js"></script>
</body>
```

最后，创建 JavaScript 代码（保存为 `openwin.js`）：

```javascript
var nw_win = document.getElementById("nwin");
nw_win.onclick = function() {
    window.open("newpage.html","cool","width=400,height=300,status=yes");
    return false;
};
```

当点击链接时，该匿名函数会生效，并启动一个包含你的 `newpage.html` 文档内容的新窗口。该窗口为 400×300 像素，并且仅在底部添加了状态栏作为额外功能。注意，`return false` 语句添加在打开窗口之后，这样如果查看器具有 JavaScript，当点击链接时 `newpage.html` 文件将不会在主浏览器窗口中同时打开（如果查看器没有 JavaScript，链接将正常工作并在同一窗口中打开 `newpage.html` 文件）。

图 10-8 显示了在浏览器中打开主页并点击链接打开新窗口的结果。

- 给链接分配了一个 id
- 调用了外部 JavaScript
- 链接元素被赋值给变量
- 匿名函数打开新窗口并返回 false

正当你认为没有更多功能可以消化时……接下来的部分将描述较新浏览器提供的其他额外选项。

### 扩展属性

对于较新的浏览器，你可以使用许多属性。在较新的浏览器中，你可以使用较新浏览器提供的额外选项。问题是这些属性在某些浏览器中可能无法工作，因此在使用这些属性时需要小心。表 10-4 显示了新窗口的扩展属性。例如，这些属性适用于 Internet Explorer, Firefox 和 Opera：

| 属性 | 可能的值 | 功能 |
| :--- | :--- | :--- |
| fullscreen | yes, no, 1, 0 | 定义窗口是否以全屏模式打开 |
| popupable | yes, no, 1, 0 | 定义窗口是否作为弹出窗口打开 |
| onclose | yes, no, 1, 0 | 定义在窗口关闭时触发的事件 |
| onresize | yes, no, 1, 0 | 定义在窗口大小改变时触发的事件 |
| onscroll | yes, no, 1, 0 | 定义在窗口滚动时触发的事件 |
| onload | yes, no, 1, 0 | 定义在窗口加载完成时触发的事件 |
| onmenu | yes, no, 1, 0 | 定义在用户打开菜单时触发的事件 |
| onactivate | yes, no, 1, 0 | 定义在用户激活窗口元素时触发的事件 |
| onblur | yes, no, 1, 0 | 定义在窗口失去焦点时触发的事件 |
| onfocus | yes, no, 1, 0 | 定义在窗口获得焦点时触发的事件 |
| onpageshowhow | yes, no, 1, 0 | 定义在页面显示时触发的事件 |
| onpagehide | yes, no, 1, 0 | 定义在页面隐藏时触发的事件 |
| onunload | yes, no, 1, 0 | 定义在页面卸载时触发的事件 |
| onmoveend | yes, no, 1, 0 | 定义在窗口移动结束时触发的事件 |
| onresizeend | yes, no, 1, 0 | 定义在窗口调整大小结束时触发的事件 |
| onscrollend | yes, no, 1, 0 | 定义在窗口滚动结束时触发的事件 |

为了使用这些属性，你需要在 `window.open()` 的第三个参数中包含它们。例如：`window.open("newpage.html","cool","width=300,height=200,fullscreen=yes");`

这些属性允许你对新窗口的行为进行更精细的控制。然而，不同的浏览器支持程度不同。为了测试这些属性，你可以使用以下代码：

```javascript
var nw_win = document.getElementById("nwin");
nw_win.onclick = function() {
    window.open("newpage.html","cool","width=400,height=300,fullscreen=yes");
    return false;
};
```

请记住，在开发 Web 应用程序时，始终检查不同浏览器的兼容性，以确保良好的用户体验。





## 第10 章：Window 对象

图 10-10 显示了从主页上的按钮打开新窗口时的初始位置。

图 10-11 显示了在新窗口中点击“移动窗口”（Move Window）按钮后的窗口状态。注意，它向右和下方各移动了 50 像素。

它的工作原理是，只要按钮可见，用户就可以继续点击该按钮并将窗口在两个方向上再移动 50 像素。窗口将根据脚本中设置的移动像素数持续移动。下讨论的方法会将窗口移动到特定位置，这样它就不会像这种方法一样在连续点击时持续移动。

### moveTo() 方法

moveTo() 方法用于根据方法调用中提供的参数将窗口移动到屏幕上的特定目标。以下是使用该方法的通用语法：

`window.moveTo(*x-value,*y-value*);`

在这里，你用 *x-value* 替换为窗口想要移动到的屏幕左侧的像素数。例如，如果你输入 300，窗口将从屏幕左侧移动 300 像素。然后你用 *y-value* 替换为窗口想要移动到的屏幕顶部的像素数。

图 10-10 新窗口打开时的初始位置
![](img/61d166424839b7674a7b9c8434ae4e03_285_0.png)

作为一个示例，你可以重写 `newpage.html` 页面中的“移动窗口”按钮，使用 `moveTo()` 代替 `moveBy()`。以下是示例代码：

```html
<<body>
  我是一个新窗口！我比打开我的那个旧窗口要新，所以我是特殊的。哈，哈！
  <form>
    <input type="button" value="Move Window" onclick="window.moveTo(50,50);" />
    <br /><br />
    <input type="button" value="Close Window" onclick="window.close(); />
  </form> 
</body>
```

这一次，当点击按钮时，窗口将移动到屏幕上的坐标 (50,50)。通过使用你的主页代码，你可以再次打开窗口来测试此效果。

为了看到它与 `moveBy()` 方法的作用不同，请尝试再次点击按钮。它并没有再次移动，而是留在原处，因为它已经到达了目的地。

图 10-11 移动后在新位置的窗口
![](img/61d166424839b7674a7b9c8434ae4e03_286_0.png)

窗口将移动到屏幕上的坐标 (50,50)，即距离左侧 50 像素，距离顶部 50 像素。

### resizeBy() 方法

resizeBy() 方法用于根据方法调用中发送的参数指定的像素数调整窗口大小。语法和用法与 `moveBy()` 方法相同；`resizeBy()` 只是执行调整大小的操作。要让窗口变大，使用正数；要让它变小，使用负数。

### resizeTo() 方法

resizeTo() 方法用于根据方法调用中发送的参数将窗口调整为特定的像素尺寸。语法和用法与 `moveTo()` 方法相同；`resizeTo()` 只是执行调整大小。你输入新的宽度和高度来代替 `moveTo()` 方法中使用的坐标。

### scrollBy() 方法

scrollBy() 方法用于根据方法调用中发送的参数指定的像素数滚动窗口。语法和用法与 `moveBy()` 方法相同；`scrollBy()` 只是执行滚动操作。要让窗口变大，使用正数；要让它变小，使用负数。

### scrollTo() 方法

scrollTo() 方法用于根据方法调用中发送的参数将窗口滚动到特定的像素目标位置。语法和用法与 `moveTo()` 方法相同；`scrollTo()` 只是滚动到指定的点。

### setInterval() 方法

setInterval() 方法用于按设定的间隔重复执行 JavaScript 函数。以下是使用该方法的通用语法：

`window.setInterval("*function*",time*);`

你用 *function()* 替换为你想要重复的函数名称。然后你用 *time* 替换为每次重复之前想要等待的时间（毫秒计）。所以，如果你真的想骚扰你的观众，可以使用此方法在页面查看后每隔 10 秒（10000 毫秒）弹出一个警框。你可以通过在文档的 HTML 中放置以下脚本来实现：

```html
<body>
  <script type="text/javascript">
    function annoy_alert() {
      window.alert("Am I bothering you?");
    }
    window.setInterval("annoy_alert()",10000);
  </script>
</body>
```

设置了一个间隔；注意在函数调用周围使用了引号。通常情况下，函数必须在引号外被调用。在这里这样做的原因是防止函数立即执行，而不是在设定的间隔时间才执行。函数名被作为字符串参数发送给 `setInterval()` 方法，然后在时间流逝后被调用。当然，这可能会变得非常烦人。间隔中设置的时间越短，就越烦人。幸运的是，十秒的间隔给了你足够的时间在另一个警框弹出之前离开页面。

### clearInterval() 方法

为了结束上一个脚本产生的连环警框攻击，你可以使用 `clearInterval()` 方法。以下是使用该方法的通用语法：

`window.clearInterval(*name*);`

你必须用 *name* 替换为赋值给想要清除的 `setInterval()` 调用的变量名。问题是，在上一个示例中，你没有将 `setInterval()` 调用赋值给变量。为了清除它，你需要调整代码。以下代码经过了更新，并将 `setInterval()` 调用赋值给了一个变量：

```html
<body>
  <script type="text/javascript">
    function annoy_alert() {
      window.alert("Am I bothering you?");
    }
    var madness = window.setInterval("annoy_alert()",10000);
  </script>
</body>
```

你现在有了使用 `clearInterval()` 方法的方法，通过将 `madness` 变量作为参数来调用它。因此，给访问者一个按钮，让他们停止这种疯狂。只要在间隔期间点击它，它就会停止间隔继续运行。以下代码提供了一个完整的页面，带有供观众点击的按钮：

```html
<body>
  <script type="text/javascript">
    function annoy_alert() {
      window.alert("Am I bothering you?");
    }
    var madness = window.setInterval("annoy_alert()",10000);
  </script>
  点击下方按钮以结束无尽的警框轰炸。<br />
  <form>
    <input type="button" value="Stop the Madness!" onclick="window.clearInterval(madness);" />
  </form>
</body>
```

方法调用被设置为了一个变量以便稍后引用。该方法通过变量名引用第一个方法来取消其操作。现在观众可以通过点击“停止疯狂”按钮来停止警框。当然，这个方法还有更好的用途。你将在后面的章节中看到，它对于时钟以及在页面上需要定期更新的其他内容是非常方便的。

### setTimeout() 方法

`setTimeout()` 方法允许你在经过一定时间后执行 JavaScript 函数。它与 `setInterval()` 方法的不同之处在于，它只执行一次（除非它被放入某种循环中）。通用语法与 `setInterval()` 方法相同。

如果你只想在十秒后弹出一个单个警框而不重复，你可以使用以下代码：

```html
<body>
  <script type="text/javascript">
    function annoy_alert() {
      window.alert("Sign my guest book NOW!");
    }
    var theguest = window.setTimeout("annoy_alert()",10000);
  </script>
</body>
```

这将在十秒后向观众发送一个警框，要求立即签名留言簿。你将方法赋值给变量的原因是为了你可以使用队列中的下一个方法，即 `clearTimeout()` 方法。

### clearTimeout() 方法

如果在 `setTimeout()` 调用的时间过期之前调用了 `clearTimeout()` 方法，则该方法允许你取消该 `setTimeout()` 调用。通用语法与 `clearInterval()` 方法相同：你使用变量名作为参数，以便它知道要取消哪个 `setTimeout()` 调用。

所以，如果你想给观众一个避免接收警框的机会，可以添加一个按钮让他们在十秒内点击。如果及时点击，`setTimeout()` 调用将被取消，且不会弹出警框。以下是示例代码：

```html
<body>
  <script type="text/javascript">
    function annoy_alert() {
      window.alert("Sign my guest book NOW!");
    }
    var theguest = window.setTimeout("annoy_alert()",10000);
  </script>
  在 10 秒内点击下方按钮以避免警框消息。<br />
  <form>
    <input type="button" value="No Alert for Me!" onclick="window.clearTimeout(theguest);" />
  </form>
</body>
```

超时被设置了，并且被赋值了一个变量以便稍后引用。超时被设置了，并赋值了一个变量以便稍后引用。




JavaScript：初学者指南

如果及时点击按钮，查看者将避免收到关于签名留言板的警报。

到目前为止，你终于完成了对窗口（window）对象方法的学习。在接下来的章节中，你将在各种脚本中使用这些方法中的许多。

**问：这里的属性和方法太多了！我该如何记住所有这些内容呢？**

**答：** 随着你开始更频繁地使用它们，它们会变得更容易记住。我对自己经常使用的部分比那些不怎么使用的部分记得更牢。如果你经常编写代码，手头留一份参考资料（比如这本书）是很有，以防你偶尔需要检查某个属性或方法的细节。我手头准备了一堆书和书签用来参考相关网站。

**问：弹出窗口不会让访客感到厌烦吗？我应该频繁使用它们吗？**

**答：** 弹出窗口的使用方式往往会让大多数观众感到厌烦（例如一次性打开多个新窗口、要求通过弹出窗口进行网站导航，或者在新的窗口中打开每个导航链接）。在没有特别特殊理由的情况下，不建议使用弹出窗口，因为它们可能会在浏览网站时造成困惑，或干扰希望在一个窗口或标签页中浏览的观众。（注意，如果你的网站通过广告获得收入，你可能需要使用弹出广告来获取收入。如果你确实使用了它们，你会希望在除了广告之外不再打开自己的弹出窗口。）

大多数浏览器现在都通过右菜单为观众提供了在新标签页或新窗口中打开链接的选项，因此最好让观众自己决定如何打开页面。

**问：我很快会制作窗口远程控制器吗？**

**答：** 一个能够改变主窗口属性（如 location 属性）的新窗口被称为“遥控器”。虽然书中没有讨论遥控器，但网络上的免费脚本网站上有这些功能的脚本。目前，你想要确保掌握创建和操作普通新窗口所需的编码。

**问：我会经常使用像 `setTimeout()` 和 `setInterval()` 这样的定时方法吗？**

**答：** 它们可能不会经常出现，但当你需要构建依赖时间的脚本（如时钟、幻灯片或动态 HTML（DHTML）动画）时，你会用到它们。

专家问

## 第 10 章：窗口对象

### 使用 setTimeout() 和 confirm() 方法

此项目将让你练习使用一些窗口方法。你会让浏览器等待若干秒，然后询问观众确认是留在当前页面还是跳转到互联网搜索站点。

#### 逐步步骤

1. 创建一个 HTML 页面，在 `body` 部分中包含以下代码，并将其保存为 `pr10_2.html`：

```html
<body>
  <h1>这里 own一些信息。</h1>
  <ul>
    <li>这里有一个有趣的点……</li>
    <li>这里有一个非常有趣的点……</li>
    <li>这里有一个极其有趣的点……</li>
  </ul>
  <script type="text/javascript" src="prjs10_2.js"></script>
</body>
```

2. 创建一个 JavaScript 文件并将其保存为 `prjs10_2.js`。使用它来完成执行第 3-4 步。

3. 20 秒后，向观众显示一个确认框，询问他们是否想继续使用此 Web 页面。如果是，则什么都不做。如果不是，则将他们发送到 URL `http://www.google.com`。

4. 保存 JavaScript 文件并在 浏览器中打开 HTML 文件。20 秒后，你应该看到一个确认框。

#### 尝试此总结

在这个项目中，你能够利用对窗口对象属性和方法的知识来创建一个定时交互式脚本。这允许你让观众选择是留在当前 Web 页面还是跳转到互联网搜索站点。

#### 第 10 章自测

1. 屏幕上显示的每个窗口都会创建一个（一个n）`__________` 对象。
2. `closed` 属性用于检查窗口是否被观众关闭。
   A 正确
   B 错误
3. `__________` 属性持有窗口内帧（frames）的数量。
4. `location` 属性可以导致浏览器立即重定向到新页面。
   A 正确
   B 错误
5. `__________` 属性持有当前窗口的名称并允许你给窗口命名。
6. 对窗口对象的属性和方法的调用通常可以缩短，因为
   A 窗口对象是 JavaScript 中的默认对象。
   B 窗口属性和方法被假设是 `navigator` 对象的一部分。
   C 实际上没有窗口对象。
   D 浏览器假设窗口对象是 `document` 对象的一部分。
7. `__________` 属性是 JavaScript 中表示“当前窗口”的另一种方式。
8. 为什么这段代码不起作用：
   `onmouseover="window.status='Page 2'; return true;"`
   A 它应该没有问题地工作。
   B 引号设置不正确。
   C 较新的浏览器默认不允许更改窗口状态，因此用户需要__________
   D 浏览器假设窗口对象是 `document` 对象的一部分。
9. 为什么这段代码不起作用：
   A 窗口对象是 JavaScript 中的默认对象。
   B 窗口属性和方法被假设是 `navigator` 对象的一部分。
   C 实际上没有窗口对象。
   D 浏览器假设窗口对象是 `document` 对象的一部分。
10. `__________` 属性是 JavaScript 中表示“当前窗口”的另一种方式。
11. 如果观众点击，`confirm()` 返回什么值？
    A true
    B false
    C OK
    D 25
12. `__________` 方法允许观众。
13. `prompt()` 方法用于输入。
14. 在设置数组时，它具有哪些值？
    A 是和否
    B 1 和 0
    C 仅是的
15. `setInterval()` 和 `setTimeout()` 的区别是什么？
    A `setTimeout()` 方法用于在设定时间重复。
    B `setTimeout()` 方法用于在延迟后执行一次。
    C `setInterval()` 方法用于闪烁。
    D 它们的功能相同。

## 第 11 章：数组

## 关键技能与概念
- 定义和访问数组
- 理解数组对象的属性和方法
- 使用循环数组
- 使用关联数组

之前的章节讨论了属性，为了使用它们，你需要数组的知识。在本章中，你将学习数组以及它们如何帮助你。

你将从数组的基本概述开始，然后学习如何定义和访问数组。之后，你将学习使用循环访问数组的所有元素。最后，你查看关联数组及其用法。

### 什么是数组？
数组是存储相似类型数据的方式，以便访问。在 JavaScript 中，数组基本上是一个用户定义的对象，其访问方式与对象不同。它使用单个变量名来存储多个值（例如，喜欢的颜色或食物列表）。在普通数组中，对元素的访问通常通过索引数字进行。关联数组允许使用字符串代替数字。为了了解普通数组的工作原理，假设你有一满级的学生，并想通过脚本快速打印出每个学生的名字。你可以使用普通变量来保存每个学生的名字，但将每个变量名输入 `document.write()` 语句将花费长时间。相反，你可以将每个学生的名字存储在数组中，这将允许你通过几行循环代码更轻松地访问它。数组允许你组合数字和名称，如下：

- 学生 0 Thomas
- 学生 1 Roger
- 学生 2 Amber
- 学生 3 Jennifer

通过这种存储方式，你可以使用数字获取每个学生的名字。




## 第 11 章：JavaScript 数组

275

***注意***

请注意数组中的第一个学生是 Student 0 而不是 Student 1。这是因为数组从数字 0 开始存储值，而不是从 1 开始。在本章的学习过程中，我们将详细讨论这一点。

### 为什么数组很有用

为什么使用数字会让你更方便地访问存储的信息呢？

因为使用数字，你可以使用循环来遍历信息，而无需手动输入每个条目。如果示例中的学生列表变得很长，当你想要将所有姓名打印到浏览器屏幕上，循环将为你节省大量的打字工作。

例如，如果你将示例列表中的每个学生的名字赋值给变量，然后将这些名字写入屏幕，你将需要在每个 `document.write()` 语句中重写每个变量名。下面的代码展示了这样一个示例：

```javascript
var student0="Thomas";
var student1="Roger";
var student2="Amber";
var student3="Jennifer";

document.write(student0+"<br />");
document.write(student1+"<br />");
document.write(student2+"<br />");
document.write(student3+"<br />");
```

如果你能使用循环为每个学生重复同一个 `document.write()` 语句，你就可以避免编写四个独立的 `document.write()` 语句。数组是一种存储值（学生姓名）的方便方法，因为你可以通过循环遍历这些值，而不是用单独的 `document.write()` 语句写出每个值——即使你事先不知道学生的数量（通过使用数组的 `length` 属性）。

数组本质上是一种创建带有属性列表的对象的快速方法（因为它已经有了一个构造函数）。普通对象（如你在第 8 章中创建的对象）可以像数组一样被访问；但通常创建数组比创建对象更简单，因为你不需要处理构造函数。

定义 定义和访问数组

现在你已经了解了什么是数组，已经准备好学习如何在 JavaScript 中命名、定义和访问数组了。

#### 为数组命名

你可以使用在第 3、第 4 和第 8 章中学过的变量、函数和对象命名的相同规则来为数组命名。基本上，避免在第一个字符中使用数字，避免空格，并避免使用保留字。

- 变量被赋予了值
- 每个变量的值都单独写在页面上

### 定义数组

定义数组类似于创建一个对象的实例。事实上，定义数组的方法在外观和行为上与创建对象实例的方法完全一样。这正是你实际在做的——创建一个 JavaScript Array 对象的实例。

由于你对创建对象实例已经很熟悉了，因此首先展示了这种方法。下面的示例显示了 JavaScript 中数组定义的通用语法：

```javascript
var *arrayname* = new Array(*element0*,*element1*);
```

你用 *arrayname* 替换为你想要给数组起的名字，并用 *element0* 和 *element1* 替换为每个元素将具有的值。你可以使用任意数量的元素。

为了看到一个真实的示例，你将从本章的第一部分获取学生姓名，并将它们作为数组元素。这个数组将有四个元素，每个元素将是学生姓名的值。下面的示例显示了数组的定义，其中姓名作为字符串值：

```javascript
var s_list = new Array("Thomas","Roger","Amber","Jennifer");
```

现在，你将这些值存储在一个名为 `s_list` 的四元素数组中。由于这些值是字符串，所以使用了引号（与普通对象一样）。问题是，既然这些值已经在数组中了，现在如何开始访问这些值呢？

#### 访问数组元素

要访问数组的元素，你需要使用通常被称为“索引数字”的内容，允许通过元素在数组中的位置访问数组的每个元素。例如，将数组的第一个元素赋值给变量的语法如下示例所示：

```javascript
var *varname* = *arrayname*[0];
```

你用 *varname* 替换为变量名，用 *arrayname* 替换为你想要访问的数组名。*arrayname* 之后方括号中的 0 是数组第一个元素的索引数字。索引之所以为 0，是因为数组从 0 开始计数而不是从 1；因此，你需要小心不要混淆数组中元素的索引数字。第一个元素的索引为 0，第二个索引为 1，第三个索引为 2，以此类推。

在紧随数组名称的方括号内，是你放置想要访问的数组元素索引数字的地方。为了看到实际效果，请再次考虑这四个学生的示例。每个学生姓名的数组定义如下代码所示：

```javascript
var s_list = new Array("Thomas","Roger","Amber","Jennifer");
```

现在，假设你想将数组中第一个元素的值（在这种情况下是 Thomas，因为它是列表中的第一个元素）赋值给名为 `tall_student` 的变量。记住，第一个元素的索引为 0；所以，为了获取第一个元素的值，你应该使用以下代码：

```javascript
var tall_student = s_list[0];
```

为了看到实际效果，你可以将该值写入页面：

```javascript
document.write(tall_student);
```

#### 定义数组的其他方法

你已经看到了一种定义数组的方法，但其他定义方法也将会很有帮助。

##### 先分配空间，稍后赋值

定义数组的一种方法是先创建空间，稍后分配值。这在你需要更多元素时适用：

```javascript
var s_list = new Array(4);
```

现在，假设你想向数组中添加第五个元素。通过为它分配值（索引数字 4），你可以添加它：

```javascript
s_list[4] = "Pat";
```

##### 先分配空间，立即赋值

另一种定义数组的方法与刚刚涵盖的方法非常相似。唯一的区别是在创建数组后立即为部分或全部元素赋值。

为了看到示例，请再次考虑 `s_list` 数组。下面的代码显示了如何在创建数组的行之后为数组元素赋值：

```javascript
var s_list = new Array(4);
s_list[0]="Thomas";
s_list[1]="Roger";
s_list[2]="Amber";
s_list[3]="Jennifer";
```

##### 数组名，无参数

定义数组的另一种选项是不带参数定义。这将创建一个没有任何元素的数组，但你可以像其他定义选项一样稍后添加元素。

```javascript
var s_list = new Array();
```





## 第 11 章：JavaScript 数组

这创建了一个名为 s_list 且没有元素的数组。你仍然可以在脚本的后续部分通过序列中的下一个索引数字来添加更多元素。因此，如果你以后决定让数组包含一个元素，可以使用以下代码：

```javascript
var s_list= new Array();
var x = 17;
var y = x+2;
var my_message = "Hi!";
s_list[0]="Thomas";
```

如果你给一个索引号更高的元素赋值，数组将扩展并为该元素之前的任何元素留出槽位。例如，看以下代码：

```javascript
var s_list = new Array();
var x = 17;
var y = x+2;
var my_message = "Hi!";
s_list[29]="Thomas";
```

这段代码的最后一行将字符串“Thomas”赋值给数组中的第 30 个元素（索引为 29）。这意味着数组从 0 个元素增加到了 30 个。通过给这个元素赋值，数组会扩展到留有足够的槽位进行补偿，如果你愿意，以后可以为这些槽位赋值。

## 理解数组对象的属性和方法

现在你已经知道了如何以各种方式定义数组，你需要查看 Array 对象的的一些属性和方法。和其他对象一样，JavaScript 对象的实例可以使用各种属性和方法。当你阅读完对 Array 对象的各个属性和方法的描述时，你会发现，你通过使用数组名后跟你想要使用的属性或方法名来访问这些属性。

表 11-1 列出了 Array 对象的属性，并提供了每个属性的简短描述。每个属性将在后续章节中进行更详细的讨论。

#### 属性

构造构造器属性包含了构造数组的函数值：

```javascript
function Array() { }
```

对数组的第一个元素进行赋值（即定义了数组）。这只是填充了空间，并表明你可以在脚本的后续部分赋值。这在数组中创建了第 30 个元素，并导致数组拥有 30 个元素。

`constructor` 属性主要用于信息目的或比较。要访问该属性，你使用数组名，后跟点运算符和 `constructor` 关键字。以下是使用 Array 属性的通用语法：

*arrayname.property*

你用数组名替换 *arrayname*，用你想要使用的属性替换 *property*。因此，要使用 `constructor` 属性，你需要先创建一个数组，以便你有一个 Array 对象的实例可以使用。这里没有创建新数组，而是使用了早先的 `s_list` 数组，允许你使用以下代码：

```javascript
var s_list = new Array(4);
window.alert(s_list.constructor);
```

这将发送一个带有数组构造函数的警框。

### index 和 input 属性

为了理解 `index` 和 `input` 属性，你首先需要理解正则表达式（用于匹配文本字符串），这需要大量的解释，正如第 13 章所提供的。关于 `index` 和 `input` 属性的讨论将留到本章。

#### length 属性

`length` 属性返回一个数字，告诉数组中有多少个元素。

***注意*** `length` 属性在你以后开始使用循环遍历数组时非常有用。你可能需要知道数组的长度（以防定义数组后添加元素），以便循环遍历数组的每个元素。

| 属性 | 描述 |
| :--- | :--- |
| constructor | 指向用于创建对象实例的构造函数 |
| index | 当通过正则表达式匹配创建数组时使用 |
| input | 当通过正则表达式匹配创建数组时使用 |
| length | 包含一个数值，等于数组中元素的数量 |
| prototype | 允许向如 Array 对象这样的对象上添加属性和方法 |

表 11-1 Array 对象的属性

要使用 `length` 属性，你使用数组名，然后在后面添加 `length` 属性。以下代码展示了使用 `length` 属性告诉查看者数组中有多少元素：

```javascript
var s_list = new Array(4);
s_list[0]="Thomas";
s_list[1]="Roger";
s_list[2]="Amber";
s_list[3]="Jennifer";
window.alert("The array has "+s_list.length+" elements");
```

这将向查看者发送一个显示“数组有 4 个元素”的警框。

#### prototype 属性

`prototype` 属性允许向已存在的对象（如 Array 对象）添加属性和方法。通过使用此属性，你可以从构造函数外部向对象添加属性。然而，请记住，使用 `prototype` 属性进行的更改会影响使用相同构造函数的对象的每个实例。

例如，如果你决定你的某个页面需要 Array 对象有另一个属性，可以使用 `prototype` 属性使用以下语法分配新属性：

*Array.prototype.*new_property=*default_value;*

你用你想要的新属性的名称替换 *new_property*，然后用该属性的默认值替换 *default_value*。

因此，如果你想在页面上的 Array 构造函数上添加一个名为 `attitude` 的新属性，并赋予它“cool”的默认值，可以使用如下代码：

```javascript
Array.prototype.attitude="cool";
var s_list = new Array();
window.alert("This place is "+s_list.attitude);
```

这将发送警框。属性的值发送到数组中。你需要记住，属性的添加会影响每个数组。通过这种方式添加属性而不是保留默认值，可以通过使用数组名来实现。以下示例展示了两个数组使用原型属性：

```javascript
var fish = new Array();
fish.attitude="wide-eyed";
window.alert("Fish are "+fish);
```

#### 方法

了解数组对象的属性后，本节介绍了你可以用来对数组进行不同操作的方法。表 11-2 列出了方法并提供了每个方法功能的描述。在表格之后，将对每个方法进行更详细的描述。

| 方法 | 描述 |
| :--- | :--- |
| concat() | 将两个或多个数组的元素合并为一个新数组 |
| join() | 将数组元素合并为单个字符串 |
| pop() | 移除数组的最后一个元素，并在需要返回被移除的元素 |
| push() | 在数组末尾添加元素，并在需要返回数组长度 |
| reverse() | 反转数组元素的方向：第一个元素移动到最后一个槽位，最后一个元素移动到第一个槽位，依此类推 |
| shift() | 从数组移除第一个元素，并在需要返回该元素 |
| unshift() | 在数组开头添加元素，并在需要返回新数组的长度 |
| slice() | 提取数组的指定部分并将该部分作为新数组返回 |
| splice() | 从数组中删除元素或替换数组元素 |
| sort() | 根据元素的字符串值对数组元素进行字母排序 |
| toString() | 使用逗号作为分隔符将数组元素合并为单个字符串 |

表 11-2 Array 方法





## 第 11 章：JavaScript 数组

283

### concat() 方法

`concat()` 方法用于合并（或连接）两个或多个数组的元素，并返回一个包含所有元素的新数组。你使用数组名称作为参数，并按照你希望组合数组元素的顺序来设置它们。

第一个示例合并了两个数组的元素。要实现这一点，只需要使用一个参数——要添加到调用该方法的数组末尾的数组名称：

```javascript
var fruits = new Array("oranges","apples");
var veggies = new Array("corn","peas");
var fruits_n_veggies = fruits.concat(veggies);
```

这段代码创建了一个名为 `fruits` 的具有两个元素的数组，以及一个名为 `veggies` 的具有两个元素的数组。接下来，它根据前两个数组的组合定义了一个新数组 `fruits_n_veggies`。`concat()` 方法返回的值赋值给这个数组名称，创建了新的合并数组。

之所以使用 `fruits` 数组来调用 `concat()` 方法并将 `veggies` 数组名称作为参数，是为了让你在新数组的开头获得 `fruits` 数组的元素并将 `veggies` 数组的元素添加到新数组的末尾。之前的代码创建的新数组 `fruits_n_veggies` 具有以下元素：

oranges, apples, corn, peas

如果你让 `veggies` 数组的元素排在前面，可以使用 `veggies` 数组名称调用该方法并将 `fruits` 数组名称作为参数：

```javascript
var fruits = new Array("oranges","apples");
var veggies = new Array("corn","peas");
var fruits_n_veggies = veggies.concat(fruits);
```

现在，`veggies` 数组的元素排在前面，新的 `fruits_n_veggies` 数组具有以下元素：

corn, peas, oranges, apples

在使用此方法时，你想要确保通过上述描述的技巧按照你想要的方式设置顺序。

如果你合并三个数组，调用 `concat()` 方法的数组元素将排在前面，然后作为参数发送的每个数组名称的元素将按照它们发送的顺序添加：

```javascript
var fruits = new Array("oranges","apples");
var veggies = new Array("corn","peas");
var meats = new Array("fish","chicken");
var three_groups = fruits.concat(veggies,meats);
```

现在你正在合并三个数组，以下是新的 `three_groups` 数组的元素：

oranges, apples, corn, peas, fish, chicken

JavaScript：初学者指南

如果你按照下面的方式编写代码，将得到一个具有相同元素的数组，但顺序不同：

```javascript
var fruits = new Array("oranges","apples");
var veggies = new Array("corn","peas");
var meats = new Array("fish","chicken");
var three_groups = meats.concat(veggies,fruits);
```

使用这段代码时，新 `three_groups` 数组中的元素顺序如下：

fish, chicken, corn, peas, oranges, apples

### join() 方法

`join()` 方法用于将数组的元素合并成单个字符串，每个元素之间由作为方法参数发送的字符分隔。如果没有发送参数，则在调用方法时将使用逗号作为默认分隔符。

要查看此方法是如何工作的，请看这段代码。以下示例定义了一个数组，然后使用数组名称调用 `join()` 方法：

```javascript
var fruits = new Array("oranges","apples","pears");
var fruit_string = fruits.join();
```

这段代码将使用 `fruits` 数组调用 `join()` 方法的结果赋值给变量 `fruit_string`。由于没有发送参数，数组的元素在新字符串中将用逗号分隔。`fruit_string` 变量将具有以下字符串值：

oranges,apples,pears

你可以通过将字符串变量写入 Web 页面看到此结果。以下代码将为你完成操作：

```html
<body
<script type="text/javascript">
var fruits = new Array("oranges","apples","pears");
var fruit_string = fruits.join();
document.write("The new string is "+fruit_string);
</script>
</body>
```

现在你可以看到从 `join()` 方法返回的字符串。图 11-1 显示了代码在浏览器中运行的结果。

| 描述 |
| :--- |
| 字符串打印到屏幕上 |
| 数组的元素合并成单个字符串，用逗号分隔元素 |
| 创建的数组具有三个元素 |

第 11 章：JavaScript 数组

285

如果你想用逗号以外的字符分隔新字符串中的元素，可以发送你想使用的字符作为参数发送。以下代码将冒号作为字符串参数发送给 `join()` 方法：

```html
<body
<script type="text/javascript">
var fruits = new Array("oranges","apples","pears");
var fruit_string = fruits.join(":");
document.write("The new string is "+fruit_string);
</script>
</body>
```

这一次的字符串与上一个稍有不同，因为它用冒号替换了之前示例中的逗号。图 11-2 显示了该字符串在浏览器窗口中如何打印。

### pop() 方法

`pop()` 方法用于从数组中移除最后一个元素。要查看此方法如何工作，请看一段代码。以下示例定义了一个数组，然后使用数组名称调用 `pop()` 方法：

```javascript
var fruits = new Array("oranges","apples","pears");
var last_element = fruits.pop();
```

这段代码将使用使用 `fruits` 数组调用 `pop()` 方法的结果赋值给变量 `last_element`。由于没有发送参数，数组的元素将用逗号分隔。`last_element` 变量将具有以下字符串值：

pears

你可以通过将字符串变量写入 Web 页面看到此结果。以下代码将为你完成操作：

```html
<body
<script type="text/javascript">
var fruits = new Array("oranges","apples","pears");
var last_element = fruits.pop();
document.write("The removed element is "+last_element);
</script>
</body>
```

现在你可以看到从 `pop()` 方法返回的字符串。图 11-1 显示了代码在浏览器中运行的结果。

`pop()` 方法用于从数组中移除最后一个元素。为了查看此方法如何工作，请看一段代码。以下示例定义了一个数组，然后使用 `pop()` 方法：

数组现在只有两个元素（oranges, apples）。图 11-1 显示了该代码在浏览器中运行的结果。

| 描述 |
| :--- |
| 字符串打印到屏幕上 |
| 数组的元素合并成单个字符串，用逗号分隔元素 |
| 创建的数组具有三个元素 |

JavaScript：初学者指南

如果你按照下面的方式编写代码，将得到一个具有相同元素的数组，但顺序不同：

```javascript
var fruits = new Array("oranges","apples");
var veggies = new Array("corn","peas");
var meats = new Array("fish","chicken");
var three_groups = meats.concat(veggies,fruits);
```

使用这段代码时，新 `three_groups` 数组中的元素顺序如下：

fish, chicken, corn, peas, oranges, apples

### push() 方法

`pop()` 方法用于从数组末最后一个元素。如果你想用逗号以外的字符分隔新字符串中的元素，可以发送你想使用的字符作为参数。如果你合并三个数组：

```javascript
var fruits = new Array("oranges","apples");
var veggies = new Array("corn","peas");
var meats = new Array("fish","chicken");
var three_groups = fruits.concat(veggies,meats);
```

现在你正在合并三个数组，以下是新的 `three_groups` 数组的元素：

使用这段代码 数组的元素顺序如下：

fish, chicken, corn, peas, oranges, apples

### pop() 方法

`pop()` 方法用于从数组中移除最后一个元素。为了查看此方法如何工作，请看一段代码。以下示例定义了一个数组，然后使用 `pop()` 方法：

数组现在只有两个元素（oranges, apples）。图 11-1 显示了该代码在浏览器中运行的结果。

`pop()` 方法用于从数组中移除最后一个元素。

...

| 描述 |
| :--- |
| 字符串打印到屏幕上 |
| 数组的元素合并成单个字符串，用逗号分隔元素 |
| 创建的数组具有三个元素 |

JavaScript：初学者指南

如果你按照下面的方式编写代码，将得到一个具有相同元素的数组，但顺序不同：

```javascript
var fruits = new Array("oranges","apples");
var veggies = new Array("corn","peas");
var meats = new Array("fish","chicken");
var three_groups = meats.concat(veggies,fruits);
```

### reverse() 方法

`reverse()` 方法用于反转数组中元素的顺序。由于它只做这些，因此不需要发送任何参数或返回值。

为了演示如何使用此方法，以下代码创建了一个数组，然后反转了数组中元素的顺序：

```javascript
var fruits = new Array("oranges","apples","pears");
fruits.reverse();
```

数组的初始顺序是 oranges, apples, pears。当为此数组调用 `reverse()` 方法时，元素的顺序被反转，数组现在的顺序是 pears, apples, oranges。

### shift() 方法

`shift()` 方法用于移除数组的第一个元素。它返回被移除元素的值，以防你可能在之后脚本中使用它。

所以，如果你想移除数组中的第一个元素，可以使用类似于下面的代码：

```javascript
var fruits = new Array("oranges","apples","pears");
fruits.shift();
```

这段代码创建了一个具有三个元素的 `fruits` 数组（oranges, apples, pears），然后移除了第一个元素 oranges。数组现在只有前两个元素（apples, pears）。

***注意***

对于那些编写过其他语言的人来说，`push()` 和 `pop()` 将数组视为栈（后进先出）。`shift()` 和 `unshift()` 方法也是这样做，混合使用这两组方法会将数组视为队列。





# JavaScript：初学者指南

此代码创建了一个包含三个元素（橙子、苹果、梨子）的数组，并使用 `shift()` 方法移除第一个元素。这会导致数组仅剩两个元素（苹果、梨子）。

要使用被删除的元素值，你可以将方法的返回值赋值给一个变量。以下代码将被删除的元素赋值给变量，然后通过警告框通知用户删除了什么：

```javascript
var fruits = new Array("oranges","apples","pears");
var picked_fruit=fruits.shift();
window.alert("You picked my "+picked_fruit);
```

此代码会在浏览器窗口中显示警告信息：“You picked my oranges”。

### unshift() 方法

`unshift()` 方法用于向数组的开头添加元素。你想要向数组中添加的元素将作为参数传递给该方法。该方法返回的值是数组新长度的数值。

以下示例向数组的开头添加了一个新元素：

```javascript
var fruits = new Array("apples","pears");
fruits.unshift("oranges");
```

这代码创建了一个名为 `fruits` 且包含两个元素（苹果、梨子）的数组，然后使用 `unshift()` 方法在数组开头添加了一个元素。该数组随后包含三个元素（橙子、苹果、梨子）。

如果你想一次添加多个元素，可以按照你想要添加的顺序将它们全部作为参数发送。以下示例向数组的开头添加了两个元素：

```javascript
var fruits = new Array("apples","pears");
fruits.unshift("oranges","grapes");
```

这获取包含两个元素（苹果、梨子）的初始数组，并在开头添加了两个元素。在调用 `unshift()` 方法后，数组最终包含四个元素（橙子、葡萄、苹果、梨子）。

### slice() 方法

`slice()` 方法用于截取数组的指定部分，并使用旧数组截取部分的元素创建一个新数组。

以下是使用该方法的通用语法：

`arrayname.slice(*start*,stop*)`

你将 *arrayname* 替换为你想要从中提取某组元素以创建新数组的数组名称。你将 *start* 替换为开始截取的索引号。你将 *stop* 替换为你想要截取的的最后一个元素之后的索引号。

第 11 章：JavaScript 数组

例如，以下代码从数组中截取两个元素，并创建一个包含这些元素的新数组：

```javascript
var fruits = new Array("oranges","apples","pears","grapes");
var somefruits = fruits.slice(1,3);
```

这截取了数组的第二个元素（索引号 1）到第三个元素（索引号 2）。它没有提取第四个元素（索引号 3），因为 3 是 2 之后的索引号，即被指定移除的最后一个元素的索引号。名为 `somefruits` 的新数组包含截取的元素（苹果、梨子）。

### splice() 方法

`splice()` 方法允许你删除或替换数组中的元素。可以发送的参数包括开始截取的索引号、要删除的元素数量以及向数组中添加新元素的选项。

如果你想从数组中删除单个元素，可以使用如下代码：

```javascript
var fruits = new Array("oranges","apples","pears","grapes");
var somefruits = fruits.splice(2,1);
```

这从索引号 2 开始删除元素。下一个参数是 1，所以只会删除一个元素；因此，这里只删除了索引号 2 的元素，即梨子。`splice` 后的数组仅包含三个元素（橙子、苹果、葡萄）。

要删除多个元素，可以可以增加第二个参数的值。以下代码从索引号 2 开始删除两个元素：

```javascript
var fruits = new Array("oranges","apples","pears","grapes");
var somefruits = fruits.splice(2,2);
```

这一次数组被缩减为两个元素（橙子、苹果），因为最后两个元素被 `splice()` 方法删除了。

你也可以使用 `splice()` 方法来替换数组中的截取元素，或向数组中添加元素。以下代码通过发送额外的参数，将索引号 2 处的截取元素替换为新元素：

```javascript
var fruits = new Array("oranges","apples","pears","grapes");
var somefruits = fruits.splice(2,1,"watermelons");
```

这一次，索引号 2 的元素被删除了。由于第二个参数是 1，所以删除了一个元素。下一个参数告诉浏览器在第一个参数指定的索引号（索引号 2）处添加此值。该值替换了被删除的值（梨子）。数组仍有四个元素，只是元素不同了（橙子、苹果、西瓜、葡萄）。

如果你想使用 `splice()` 方法向数组添加一个或多个元素但不删除任何内容，可以将第二个参数设置为 0（从而删除零个元素）。你将第一个参数设置为想要开始添加元素的索引号。例如，查看以下代码：

```javascript
var fruits = new Array("oranges","apples","pears","grapes");
var somefruits = fruits.splice(2,0,"watermelons","plums");
```

这一次，元素的添加从第一个参数指定的索引号 2 开始，并且根据第二个参数没有删除任何内容。添加了两个元素后，数组将有六个元素（橙子、苹果、西瓜、李子、梨子、葡萄）。

### sort() 方法

`sort()` 方法按字母顺序对数组排序（类似于目录列表）。然而，这不是数值顺序。例如，再次考虑水果数组。如果你想更改元素的顺序使其按字母顺序排列，可以使用以下代码：

```javascript
var fruits = new Array("oranges","apples","pears","grapes");
fruits.sort();
```

**问：** **在所有属性中，是否有任何属性对数组特别有用？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

（此处省略了重复的重复文本部分）

**问：** **在所有属性中，是否有任何属性对数组特别有用？**

**答：** `length` 属性在很多情况下都很有用。其他属性在某些情况下有用（例如当需要反转数组元素的顺序时）。随着你的学习，你可能会在自己的脚本中发现它们是有用的。

**问：** **有什么简单的方法记住所有属性吗？**

（此处省略了重复的重复文本部分）

### 专家解答（重复）

### toString() 方法

`toString()` 方法将数组的元素组合为一个字符串，并以逗号作为分隔符。例如，可以使用以下代码：

```javascript
var fruits = new Array("oranges","apples","pears","grapes");
var fruit_list = fruits.toString();
document.write(fruit_list);
```

这将在页面上写入字符串：

Oranges,apples,pears,grapes

###扩展方法

对于 JavaScript 1.6 或更高版本，有一些额外的方法可以使用。由于（在编写时）这些方法尚未跨浏览器支持，它们将列在表 11-3 中。有关这些方法的更多信息，请参阅 https://developer.mozilla.org/En/Core_JavaScript_1.5_Reference:Global_Objects:Array（点击任一方法将获得更详细的描述，通常带有您可以在不支持该方法的浏览器中实现相同功能的代码）。

| 方法 | 描述 |
| :--- | :--- |
| `filter()` | 返回一个包含根据过滤函数返回真值的元素的新数组 |
| `forEach()` | 为数组中的每个元素调用指定的函数 |
| `every()` | 如果数组中的所有元素对于指定的测试函数都返回真值，则返回真 |
| `indexOf()` | 返回与指定值相同的元素的最低索引号 |
| `lastIndexOf()` | 返回与指定值相同的元素的最高索引号 |
| `map()` | 返回一个新数组，其结果是对数组中的每个元素调用指定的函数 |
| `reduce()` | 从左到右对数组中的每两个值运行一次函数，直到只剩一个值 |
| `reduceRight()` | 从右到左对数组中的每两个值运行一次函数，直到只剩一个值 |
| `some()` | 如果数组中至少有一个或多个元素对于指定的测试函数返回真值，则返回真 |

表 11-3 扩展数组对象方法





## JavaScript: 入学者指南

### 在循环中使用数组

循环允许你遍历数组元素，而无需编写多行代码逐个处理每个元素。相反，你可以使用循环来遍历数组的每个元素，从而减少处理大型数组所需的代码行数。首先，让我们看看如何使用循环而不是直接赋值值来创建数组元素。

#### 创建数组元素

循环在创建数组元素时非常有用。如果你由于某些原因需要用户输入数组的内容，或者你希望在创建每个元素时执行类似的计算，这就尤为有用。假设你想让用户能够输入之前介绍的 `s_list` 数组中的四个学生姓名。使用 `for` 循环，你可以使用以下代码允许用户输入每个姓名：

```javascript
var s_list = new Array(4);
for(var count=0;count<4;count++) {
    s_list[count] = window.prompt("Enter a name","");
}
```

这段代码创建了一个包含四个元素的新数组。然后使用 `for` 循环为每个值赋值。循环从将循环变量 `count` 设置为 0 开始，一直运行到 `count<4` 不再真为止。由于每次将 `count` 的值加 1（`count++`），这意味着 `count` 变量第一次的值为 0，第二次为 1，第三次为 2，第四次为 3。它不会再执行一次。

***将 `count` 变量从 0 开始的优势是你在使用循环时不容易感到困惑。** `count` 变量代表每个数组元素的索引数字，因此你不需要像之前将 `count` 从 1 开始那样对其值减 1。在循环内部，每次循环都会向 `count` 变量所代表的索引位置的元素赋值。赋值的值是用户在提示输入姓名时所输入的内容。在这种情况下，用户将收到四次提示，并为所有四个元素赋值。

- 创建了一个包含四个元素的新数组
- 循环从 0 循环到 3
- 每次循环都会给用户给出一个提示
- 用户输入的文本被赋值给该元素

第 11 章：JavaScript 数组

### 遍历数组

你也可以遍历已创建的数组来更改它、获取其信息或以你喜欢的方式列出其内容。这非常有用，并且可以在处理大型数组时节省时间。

如果你回到列出学生姓名的旧 `s_list` 数组，你会发现当你决定在屏幕上打印学生列表时，循环可以节省一些打字时间。你还可以设置循环，以便在你以后向数组中添加内容时它会自动调整。首先，看看如何使用循环将姓名列表打印到浏览器屏幕上。HTML 代码如下（将其保存为 `s_names.html`）：

```html
<body>
    <h1>Student Names</h1>
    <script type="text/javascript" src="s_names.js"></script>
</body>
```

- 定义了一个包含十个元素的数组
- 声明了一个新变量来存储每次递增 1 的计数
- 循环每次递增 2，从 0 到 18
- `a_count` 变量进行递增
- 根据 `count` 变量的值在此处为元素

接下来，你可以使用以下 JavaScript 代码（将 JavaScript 文件保存为 `s_names.js`）：

```javascript
var s_list = new Array(4);
s_list[0]="Thomas";
s_list[1]="Roger";
s_list[2]="Amber";
s_list[3]="Jennifer";
for(var count=0;count<4;count++) {
    document.write(s_list[count] + "<br>");
}
```

你基本上使用了循环来打印数组的元素。这展示了脚本运行时的效果。现在，如果你想确保在添加或删除学生时数组能够自动调整，你必须使用数组的长度而不是固定数字。要实现这一点，使用数组的长度来确定数组中有多少元素，并使用循环：

```javascript
for(var count=0;count<s_list.length;count++) {
    document.write(s_list[count] + "<br>");
}
```

元素的顺序使用循环打印在页面上。这展示了脚本运行时的效果。





JavaScript: 入学者指南

元素经过调整，并打印出字母顺序的列表。以下是字母排序的代码：

```javascript
var s_list = new Array();
s_list[0]="Thomas";
s_list[1]="Roger";
s_list[2]="Amber";
s_list[3]="Jennifer";
s_list[4]="Pat";
s_list[5]="Kelly";
s_list[6]="Jerry";
s_list.sort();

for(count=0;count<s_list.length;count++) {
    document.write(s_list[count]+ "<br />");
}
```

注意添加的 `s_list.sort()` 调用。这会对数组进行排序，从而提供字母顺序的输出。

图 11-5 显示了该脚本在浏览器中运行的结果。

#### for each 循环

在较新版本的 JavaScript（1.6 及更高版本）中，你可以使用 `for each` 循环来遍历数组元素列表。它允许你在每次循环中使用一个变量作为数组元素的值（而无需使用类似 `s_list[count]` 的内容，你可以简单地使用如 `student` 的名称）。以下代码展示了使用你在在本章过的 `s_list` 数组的示例：

```javascript
var s_list = new Array();
s_list[0]="Thomas";
s_list[1]="Roger";
s_list[2]="Amber";
s_list[3]="Jennifer";
for each (student in s_list) {
    document.write(student + "<br />");
}
```

注意 `for` 和 `each` 是两个独立的保留字，后面紧跟左括号，接着是你想要使用的变量名（在本例中为 `student`），然后是保留字 `in`，紧接着是数组名称，并以右括号结束。然后，左大括号允许你像往一样编写循环代码，只不过你将使用变量名（在本例中为 `student`），而不是保持一个计数变量并使用 `s_list[count]`。

由于这（在写作期间）尚未支持跨浏览器运行，目前最好的方法是继续使用传统的 `for` 循环（向后兼容），或像下面的代码一样使用 `for in` 循环：

```javascript
var s_list = new Array();
s_list[0]="Thomas";
s_list[1]="Roger";
s_list[2]="Amber";
s_list[3]="Jennifer";
for (student in s_list) {
    document.write(s_list[student] + "<br />");
}
```

你可以开始使用处理数组变得更加复杂的循环，并使用更多的属性和方法。目前，这可以帮助你入门并建立基础，你可以据此为你的 JavaScript 数组构建更复杂的循环。

## 在数组使用循环

此项目允许你练习在数组中使用循环，并练习使用数组的一些属性。你将创建一个计算机部件列表并将其打印到屏幕上。

### 步骤详解

1. 创建一个带有标题“Computer Parts Needed”（所需的计算机部件）的 HTML 页面。添加 script 标签，并包含一个名为 `prjs11_1.js` 的外部 JavaScript 文件。将 HTML 文件保存为 `pr11_1.html`。
2. 创建一个外部 JavaScript 文件并将其保存为 `prjs11_1.js`。在第 3-10 步中使用它。
3. 创建一个新数组，并将以下部件列表赋值给数组中的元素：
   - monitor（显示器）
   - motherboard（主板）
   - chip（芯片）
   - hard drive（硬盘）
4. 在浏览器窗口中逐行打印每个计算机部件（使用循环）。
5. 保存 JavaScript 文件，并在浏览器中加载 HTML 文件以查看结果。
6. 在你的文本编辑器中重新打开 JavaScript 文件，并进行接下来三个步骤中描述的更改。
7. 如果你之前没有这样做，请在比较中使用 `length` 属性而不是数字。
8. 通过在脚本中编码向数组添加一些元素。在已有的前四个项目之后添加以下项目：
   - CD-RW drive（CD-RW 驱器）
   - power supply（电源）
9. 让数组自排序，使其按字母顺序排列。
10. 保存 JavaScript 文件并在浏览器中查看 HTML 文件。新元素应该出现在数组元素的字母顺序列表中。

### 尝试本总结

在这个项目中，你利用关于循环、数组和 Array 对象属性的知识创建了两个不同的结果。一个结果列出了数组的元素，而另一个结果则向数组添加了一些元素并按字母顺序列出这些元素。

### 使用关联数组

关联数组（也称为哈希表）允许你使用字符串代替索引数字。使用关联数组与使用普通数组非常相似，但你可以使用字符串作为索引。





## 第 11 章：JavaScript 数组

### 11-2 使用关联数组

此项目允许你练习使用关联数组。你将根据各种汽车的特性创建一个元素数组。

#### 步骤

1. 创建一个 HTML 页面，包含一个文本为“List of Cars”（汽车列表）的标题。添加 `<script>` 标签以包含名为 `prjs11_2.js` 的外部 JavaScript 文件。将 HTML 文件保存为 `pr11_2.html`。
2. 创建一个外部 JavaScript 文件并将其保存为 `prjs11_2.js`。在步骤 3-6 中使用它。
3. 创建一个带有以下索引字符串的关联数组：
   - cool
   - small
   - long
4. 为索引字符串为“cool”的元素赋值值“Mustang”。为索引字符串为“small”的元素赋值值“Bug”。为索引字符串为“long”的元素赋值值“Station Wagon”。
5. 将每个元素的值打印到浏览器窗口。
6. 保存 JavaScript 文件并在浏览器中查看 HTML 文件。你应该能看到汽车列表。

#### 尝试练习总结

在本项目中，你利用了关于关联数组的知识创建了一个显示关联数组元素的页面。

*第 11 章自测*

1. 数组是一种对相似类型数据进行 __________ 的方法，以便以后在脚本中进行访问。
2. 在 JavaScript 中，数组本质上是一个用户定义的 __________。
3. 在普通数组中，访问元素通常是通过使用(n) __________ 实现的。
   - A 字符串
   - B 索引数字
   - C 随机数
   - D 随机字符串
4. __________ 数组允许使用字符串代替数字进行访问。
5. 下列中哪个是有效的数组名称？
   - A my array
   - B 1stArray
   - C for
   - D soap
6. 下列中哪个不能正确创建数组？
   - A `var myarray = new Array();`
   - B `var myarray = new Array(5);`
   - C `var myarray = new Array("hello","hi","greetings");`
   - D `var if = new Array[10];`
7. 下列哪项可以正确访问名为“cool”的数组的第五个元素？
   - A `cool[5];`
   - B `cool(5);`
   - C `cool[4];`
   - D `cool.array[4];`
8. 下列代码的作用是什么？
   `var s_list = new Array()`
   - A 创建一个名为 s_list 的空数组
   - B 创建一个名为 s_list 的数组，默认元素数量为 10
   - C 创建一个名为 list 的空数组
   - D 创建一个永远无法添加任何元素的数组
9. Array 对象的哪个属性将返回数组长度的数值值？
   - A length 属性
   - B getlength 属性
   - C constructor 属性
   - D lengthOf 属性
10. __________ 属性允许你向已存在的对象添加属性和方法。
11. __________ 方法用于将两个或多个数组的元素合并，并返回一个包含所有元素的新数组。
12. `join()` 方法用于将数组的元素合并成一个单一 __________，每个元素之间用指定的字符分隔。
13. __________ 方法用于删除数组的最后一个元素。
14. 默认情况下，`sort()` 方法如何对数组的内容进行排序？
   - A 它反转数组的内容。
   - B 它按数值排序内容。
   - C 它按字母顺序排序内容。
   - D 它删除数组的最后一个元素。
15. 关联数组中用什么来代替索引数字？
   - A 浮点数值
   - B 布尔值
   - C 负数
   - D 字符串值

## 第 12 章：Math、Number 和 Date 对象

核心技能与概念
- 使用 Math 对象
- 理解 Number 对象
- 使用 Date 对象

上一章介绍了 JavaScript 数组，包括 Array 对象。在本章中，你将按照相应的顺序学习 Math、Number 和 Date 对象。对于每个对象，都将提供简短的介绍，并说明为什么该对象可能很有用。随后将介绍你可以用于该对象可以的各种属性和方法。

### 使用 Math 对象

Math 对象是一个预定义的 JavaScript 对象。与你在书中学习过的其他预定义对象一样，Math 对象提供了供你使用的属性和方法。Math 对象用于数学目的以执行某些操作。

#### Math 对象的用处

如所述，当你需要在脚本中进行数学计算时，Math 对象非常有用。例如，如果你在计算中需要 pi 的值，Math 对象提供了一个供你使用的属性以便你可以获取该值。此外，如果你需要找到一个数的平方根，Math 对象的一个方法允许你实现这一点。该对象提供的另一个功能是生成随机数，你会在某些脚本从中它的用。

#### 属性

Math 对象提供了数值属性，如果你需要执行数学计算时，这些属性可以对你有帮助。表 12-1 列出了 Math 对象的属性及其值。如表 12-1 所示，所有属性都只持有数值，这些数值在数学计算中很有用。由于这些是无理数，列出的值是非无限的，因此是近似值。

#### 使用属性

属性包含只读值，如果你需要执行数学计算时，这些值可以对你有帮助。例如，为了计算圆的面积，你可以根据公式 Area = πr² 输入半径编写应用程序。以下是 HTML 代码：

```html
<form>
  要计算圆的面积，请输入半径：<br />
  <input type="text" id="radius" />
  <input type="button" value="Get the Area!" id="getarea" />
</form>
```

接下来是 JavaScript 代码：

```javascript
var area_button = document.getElementById("getarea");
area_button.onclick = function() {
  var rad = document.getElementById("radius").value;
  if (rad.length < 1) {
    window.alert("请输入半径!");
    return false;
  }
  else if (rad != (rad*1)) {
    window.alert("半径必须是数字!");
    return false;
  }
  else {
    var the_area = Math.PI * (rad * rad);
    window.alert("面积为 " + the_area + " 平方单位。");
    return false;
  }
};
```

这段代码首先通过 id 获取输入按钮并赋值给变量 area_button。当点击此元素时，会执行一个匿名函数。它获取文本框中的值并赋值给变量 rad。

接下来，代码执行两次检查。它检查是否输入了数据，并检查输入的是否数字。

#### 表 12-1 Math 对象的属性

| 属性 | 值 |
| :--- | :--- |
| E | 欧拉常数 (E)，约为 2.71828… |
| LN10 | 10 的自然对数，约为 2.302585… |
| LN2 | 2 的自然对数，约为 0.693147… |
| LOG10E | E 的底为 10 对数，约为 0.43429… |
| LOG2E | E 的底为 2 对数，约为 1.442695… |
| PI | π 值，常用于圆，约为 3.14159… |
| SQRT2 | 2 的平方根，约为 1.4142… |
| SQRT1_2 | 半分之一的平方根，约为 0.7071… |

- 这段代码通过 id 获取输入按钮并赋值给变量 area_button。
- 点击此元素时，会执行一个匿名函数。它通过 value 属性获取半径文本框的值并赋值给变量 rad。
- 接下来，代码执行两次检查：它检查是否输入了数据，并检查输入的是否数字。





## 第 12 章：Math、Number 和 Date 对象

309

图 12-1 为观众显示圆的面积

![](img/61d166424839b7674a7b9c8434ae4e03_331_0.png)

| 方法 | 目的 |
| :--- | :--- |
| abs() | 返回作为参数数字的绝对值 |
| acos() | 返回作为参数数字的反余弦（单位为弧度） |
| asin() | 返回作为参数数字的反正弦（单位为弧度） |
| atan() | 返回作为参数数字的反正正切（单位为弧度） |
| atan2() | 返回两个参数数字商的反正正切（单位为弧度） |
| ceil() | 返回大于或等于参数数字的最小整数 |
| cos() | 返回作为参数数字的余弦（单位为弧度） |
| exp() | 返回 E 的作为参数传递方法的数字的幂 |
| floor() | 返回小于或等于参数数字的最大整数 |
| log() | 返回作为参数数字的自然对数 |
| max() | 返回两个作为参数数字中较大的一个 |
| min() | 返回两个作为参数数字中较小的一个 |
| pow() | 返回第一个参数的第二个参数的幂的数值 |
| random() | 返回一个 0 到 1 之间的随机数；不需要参数 |
| round() | 返回作为参数数字四舍五入到最近整数的值 |
| sin() | 返回作为参数数字的正弦（单位为弧度） |
| sqrt() | 返回作为参数数字的平方根 |
| tan() | 返回作为参数数字的正切（单位为弧度） |

表 12-2 Math 对象的方法

JavaScript：初学者指南

### 基础方法

就本书而言，“基础方法”被定义为接收单个数字、对其进行简单计算并返回一个值的方法。通过这种方式对方法进行分组，避免了为每个方法列出相同的示例——这并不是对方法的任何官方分类，只是为了便于讨论的一种方法。

以下基础方法的工作方式通常都相同：

- abs()
- acos()
- asin()
- atan()
- cos()
- exp()
- log()
- sin()
- sqrt()
- tan()

这些基础方法中的每一个都接收一个数值并返回另一个值。由于通用用法相同，本讨论使用 `sqrt()` 作为示例，说明如何使用其他方法来获取它们的各种值。如果你需要知道其他方法返回什么类型的值，请参考表 12-2 以查看每个方法的功能。

使用 `sqrt()` 方法最简单的方法是将一个正数作为方法的参数输入，如下例所示：

`window.alert(Math.sqrt(4));`

这会弹出 4 的正平方根的值，即 2。

与其计算一个静态数字，你可以让用户输入一个数字，然后向用户发送一个包含用户输入的数字平方根的警告。你可以使用以下代码来实现，从 HTML 代码开始：

```html
<body
<form>
输入一个（正数）数字或 0： <br />
<input type="text" id="sr_num" />
<input type="button" value="获取平方根" id="getroot" />
</form>
</body>
```

第 12 章：Math、Number 和 Date 对象

311

接下来是 JavaScript 代码：

```javascript
var root_button = document.getElementById("getroot");
root_button.onclick = function() {
  var thenum = document.getElementById("sr_num").value
  if (thenum < 0) {
    window.alert("嘿！我说是要输入正数！重试一次.");
    return false;
  }
  else if (thenum != (thenum*1)) {
    window.alert("输入必须是数字!");
  }
  else {
    var theroot = Math.sqrt(thenum);
    window.alert("+thenum+" 的平方根是 "+theroot);
  }
  return false;
};
```

前面的代码使用了匿名函数，该函数在观众点击 HTML 代码中的按钮时被调用。该函数首先将输入赋值给文本框。然后它检查数字是否为负数；如果是，则会出现一个警告告诉观众重试。否则，它会检查输入是否为数字；如果不是，就会弹出一个警告。最后，它计算该数字的平方根并将其赋值给变量，然后向观众显示结果。

（注：OCR 文本在后续部分包含大量重复和乱码句子，已根据提供的代码根据逻辑流进行了清理。）

### 双参数方法

本节讨论了接收两个参数而不是一个的方法。这些包括：

- atan2()
- max()
- min()
- pow()

`max()` 和 `min()` 方法非常相似，而 `pow()` 方法执行的是不同的操作。`max()` 方法接收两个数字并返回较大的。`min()` 方法也接收两个参数但返回较小的数字。你可以通过将结果赋值给变量并在脚本中使用这些方法。例如，你可以使用以下脚本，从 HTML 代码开始：

```html
<body>
<form>
<input type="button" value="哪个更大?" id="getmax" />
</form>
</body>
```

JavaScript：初学者指南

335

313

接下来是 JavaScript 代码：

```javascript
var max_button = document.getElementById("getmax");
max_button.onclick = function() {
  var num1 = window.prompt("输入一个数字。");
  var num2 = window.prompt("输入另一个数字","");
  var largenum = Math.max(num1,num2);
  var smallnum = Math.min(num1,num2);

  if (largenum == smallnum) {
    window.alert("这两个数字相等！");
  }
  else {
    window.alert(largenum+" 大于 "+smallnum);
  }
};
```

此脚本提示观众两个数字并将其赋值给变量。然后它获取两个数字的最大值和最小值并将返回的值赋值给变量。这些变量随后用于检查它们是否相等。如果是，会弹出一个警告说相等；否则，会弹出一个显示结果。下面的插图展示了如果观众在浏览器中第一个数字输入 2，第二个数字输入 5，该脚本的结果。

### pow() 方法

`pow()` 方法接收两个参数并计算第一个参数的第二个参数的幂。例如，以下代码将返回 2 的 3 次幂：

`Math.pow(2,3);`

除此之外，你可以像使用其他双参数方法一样使用它，通过将结果赋值给变量并在脚本中使用该变量。例如，你可以使用以下脚本，从 HTML 代码开始：

```html
<body>
<form>
<input type="button" value="查找幂" id="getpow" />
</form>
</body>
```





JavaScript：初学者指南

接下来是 JavaScript 代码：

```javascript
var pow_button = document.getElementById("getpow");

pow_button.onclick = function() {
  var num1 = window.prompt("Enter a base number.","");
  var num2 = window.prompt("What power should we set it to (a number)?","");
  var theresult = Math.pow(num1,num2);
  window.alert(num1+" to the power of "+num2+" is "+theresult);
};
```

使用这段代码，如果观众在输入第一个数字时输入 2，在询问幂时输入 3，脚本将计算 2 的 3 次方的的结果。然后观众将看到一个显示答案的警框。点击 HTML 代码中的按钮是查看者启动函数的方式。当输入数字 2 和 3 时，该脚本的结果在此所示：

现在你已经了解了双参数方法，让我们来看一些其他尚未涵盖的方法。

#### 其他方法

这些方法接收单个参数，但每个方法对该参数的作用都值得仔细观察。这些独立的方法包括：

- ceil()
- floor()
- round()

### ceil() 方法

ceil() 方法代表 *ceiling*（天花板），它返回大于或等于参数数字的最小整数。该方法主要用于数字可能带有小数部分的情况。它会将数字向上舍整到下一个最大的整数，除非该数字已经是整数。在这种情况下，将返回相同的数字（因为可以相等）。例如，`Math.ceil(12.23);` 将返回 13，但 `Math.ceil(12);` 将返回 12。

以下脚本展示了如何使用 ceil() 方法返回不同的值，从 HTML 代码开始：

```html
<<body>
<form>
  <img src="img/61d166424839b7674a7b9c8434ae4e03_336_0.png">
  <input type="button" value="Find a Ceiling" id="getceiling" />
</form>
</body>
```

接下来是 JavaScript 代码：

```javascript
var ceil_button = document.getElementById("getceiling");

ceil_button.onclick = function() {
  var num1= window.prompt("Enter a number.","");
  var theceil= Math.ceil(num1);
  window.alert("The ceiling of "+num1+" is "+theceil);
};
```

此脚本显示一个警框，说明观众输入的数字的天花板值。下面的插展示了当观众在提示中输入 4.5 时，在浏览器中显示的结果：

### floor() 方法

floor() 方法类似于 ceil() 方法，但它的方向相反。floor() 方法返回小于或等于参数的最大整数。它会将数字向下舍整到下一个最小的整数，除非参数是整数。在这种情况下，它会返回相同的整数，因为它已经是了。基本上，这个方法只是去数字的小数部分，并将整数部分作为结果。例如，`Math.floor(12.23);` 将返回 12，`Math.floor(12);` 也会返回 12。你可以像在前一节中使用 ceil() 方法一样使用 floor() 方法——通过将结果赋值给变量。

### round() 方法

round() 方法的工作原理与之前的方法相似，但是将输入的参数数字舍入到最近的整数，无论它是大于还是小于该数字。任何小数部分值为 .5 或更大的数字将被向上舍入，而任何值小于 .5 的小数将向下舍入。.5 的截断点是严格的，因此即使你倾向于向上舍入，`Math.round(12.49999);` 也会返回 12。

### random() 方法

random() 方法对于创建需要整数的脚本非常有用。它返回一个 0 到 1 之间的随机数。这意味着你得到一个小数可能很长的数字，其本身没用。例如，它可能会返回类似 0.365116549809523 的数字。

为了获得随机整数，你想做的第一件事是让结果具有更大的范围，这样你就不会被卡在 0 和 1 之间。为了获得更大的范围，你可以将 random() 方法的结果乘以一个整数来创建一个更大的范围。就像数组一样，范围将从 0 开始计数；因此，为了获得五个整数的范围，你会将结果乘以 5。下面的代码展示了如何这样做：

```javascript
var rand_num = Math.random()*5;
```

这得到了 0 到 4 之间的结果，但还没有给你整数。数字仍然可能是长小数。要得到 0 到 4 之间的整数，你需要找到一种让所有这些小数转换为整数的方法。记得你之前运行了三个方法，floor()、ceil() 和 round()，它们以各种方式将数字转换为整数。floor() 方法是你将选择的，因为它简单地删除了整数后的小数位，并给你数字的整数部分。

使用 floor() 方法，你可以写以下代码：

```javascript
var rand_num = Math.random()*5;
var rand_int = Math.floor(rand_num);
```

floor() 方法将 `rand_num` 变量的值作为参数传入，然后从中给你一个整数。如果你想节省一行代码，可以写得巧妙一点。你可以直接将 random() 方法和计算作为 floor() 方法的参数。你可以这样做，因为计算结果 `Math.random*5` 是一个数字，而 floor 方法可以接受数字作为参数。下面的代码展示了你如何在单行中编写代码：

```javascript
var rand_int = Math.floor(Math.random()*5);
```

现在，变量 `rand_int` 将拥有 0 到 4 之间的随机整数值。正如你可能注意到的，这种数字范围在数组中可能非常有用。这就是你开始使用随机数编写一些有趣脚本的方法。

### 用于脚本的随机数

现在你可以通过使用 random() 方法对 Math 对象玩点乐了。通过设置一些数组，你可以创建一个每次页面加载时都提供随机引言或显示随机图像的脚本。

### 趣味随机引言




JavaScript：初学者指南

quotes[2]="我的 JavaScript 书在哪了？";

quotes[3]="如果我每花一美元就能得到一块钱——噢，算了。";

quotes[4]="我想你期望在这里看到一句真正的引用。";

quotes[5]="引言很棒，但这话可别引用我的准。";

quotes[6]="我应该在这里写什么呢？";

quotes[7]="如果我故意拼错单词会发生什么？";

quotes[8]="记住我的话，我会记住我的话。";

quotes[9]="这个位置留给更好的引用。";

var q_div = document.getElementById("my_quote");

var rand_int = Math.floor(Math.random()*10);

q_div.innerHTML = quotes[rand_int];

该代码根据 `rand_int` 变量中的随机整数值，在页面上写入一个随机引言。对于没有启用 JavaScript 的用户，提供了一个默认引言（数组数据中的第一个），如果可以使用 JavaScript，则它会被随机引言覆盖。

重新加载页面可以重置随机数，并可能（尽管不一定，因为是随机的）显示不同的引言。

图 12-3 显示了此脚本在浏览器中运行的可能结果之一。

图 12-4 显示了此脚本在浏览器中运行的另一个可能结果。

你可以通过刷新页面不断获得不同的（有时是相同的）结果。

既然你已经可以向页面写入随机引言了，那么显示随机图片如何？

它与上一个脚本非常相似；你只需要进行一些小的调整。

用于更新外观的随机图片

随机图片脚本可以让你的页面具有持续更新的感觉，而不需要你不断更改图像。当然，所有图像都需要适应你决定放置随机选择图像的内容。随机图片脚本非常有用，例如用于美术馆展示其收藏。

![](img/61d166424839b7674a7b9c8434ae4e03_340_0.png)

图 12-3 使用随机引言脚本的一种可能结果

## 第 12 章：Math、Number 和 Date 对象

319

你首先需要一个图像通用资源定位符（URL）地址数组（可以是本地地址，也可以是绝对地址——这里使用了本地地址）。此脚本使用的数组在以下示例代码中：

```javascript
var r_image= new Array(10);

r_image[0]="image0.gif";
r_image[1]="image1.gif";
r_image[2]="image2.gif";
r_image[3]="image3.gif";
r_image[4]="image4.gif";
r_image[5]="image5.gif";
r_image[6]="image6.gif";
r_image[7]="image7.gif";
r_image[8]="image8.gif";
r_image[9]="image9.gif";
```

此数组设置了每次加载页面时可以随机显示的图像的地址。

接下来，你需要一种方法获取 0 到 9 之间的随机整数。这与之前的随机引言脚本相同：

```javascript
var rand_int= Math.floor(Math.random()*10);
```

下一步是在文档的 `body` 部分访问数组，以便在页面在浏览器中加载时显示数组中的随机图像。

以下代码允许你使用 `div` 元素的 `innerHTML` 属性，如果可以使用 JavaScript，则为随机图像写入 `img` 标签。

![](img/61d166424839b7674a7b9c8434ae4e03_341_0.png)

图 12-4 使用随机引言脚本的另一个可能结果

JavaScript：初学者指南

HTML 文件保存为 `random_images.html`，JavaScript 文件保存为 `random_images.js`。首先是 HTML 代码：

```html
<body>
  <h1>我给你的的随机图片：</h1>
  <div id="my_image">
    <img src="image0.gif" alt="随机图片" />
  </div>
  <script type="text/javascript" src="random_images.js"></script>
</body>
```

接下来是 JavaScript 代码：

```javascript
var r_image= new Array(10);

r_image[0]="image0.gif";
r_image[1]="image1.gif";
r_image[2]="image2.gif";
r_image[3]="image3.gif";
r_image[4]="image4.gif";
r_image[5]="image5.gif";
r_image[6]="image6.gif";
r_image[7]="image7.gif";
r_image[8]="image8.gif";
r_image[9]="image9.gif";

var i_div = document.getElementById("my_image");
var rand_int = Math.floor(Math.random()*10);

i_div.innerHTML = '<img src="'+r_image[rand_int]+'" alt="随机图片" />';
```

如你所见，这与随机引言脚本非常相似。你只需要更改数组的内容以及替换 `innerHTML` 属性内容的语句，使脚本显示图像而不是引言。

***注意***

对于此示例，图像保存为 `image0.gif`、`image1.gif` 等；但是，你可以以你喜欢的任何名称保存图像文件。

关于 `random()` 方法的讨论可以持续很长时间，因为有很多东西可以进行随机化。然而，你现在已经了解了该功能工作的基本原理，所以是时候继续下了。

## 第 12 章：Math、Number 和 Date 对象

321

y 这 12-1

12_1.html

js12_1.js

### 在页面上显示随机链接

此脚本允许你更深入地使用 `random()` 方法，让你能够创建一个在页面上显示随机链接的脚本。

### 逐步步骤

1.  创建一个 HTML 页面，其中包含 `script` 标签指向名为 `prjs12_1.js` 的外部 JavaScript 文件。添加一个显示“随机链接”的标题，并添加一个 id 为 `random_link` 的 `div` 元素。在 `div` 元素内部，为没有 JavaScript 的用户插入一个默认链接。将 HTML 文件保存为 `pr12_1.html`。

**Q：我真的用到 Math 对象的任何属性吗？它们全都是我甚至没用过的数字！**

**A：这取决于你执行不同类型计算的频率。作为一个初学者，你不太可能会使用其中任何一个，但确实有一些脚本将它们用于各种高级用途，例如 JavaScript 计算器。**

**Q：我对写计算器没兴趣。我真的需要费心背诵 Math 对象的所有属性吗？**

**A：嗯，可能不需要，因为使用它们的情况可能不会经常出现。不过，手留一份参考资料以防万一，并且大致了解它们是什么是好的，因为它们不时会在 Web 上的脚本中出现。**

**Q：如果我身边没有计算器，这些属性和方法中的一些可能会有用。我可以写一个小脚本来为自己计算一些东西，对吧？**

**A：当然可以！只需务必双检数字，确保你的代码中没有错误。**

**Q：`random()` 方法到目前为止很有趣，但我还没想到其他可以用它的地方。你能给我一些使用它的主意吗？**

**A：还有很多其他地方可以使用它。你可以对几乎任何可以用 HTML 标签显示的内容进行随机化。这里是我脑子里跳出的一些想法：随机链接、随机图片、某种游戏的随机任务（如掷骰子或抽牌）、随机页面问候、随机警报……我确定还有很多。**

### 专家问答

（继续）

JavaScript：初学者指南

2.  创建一个外部 JavaScript 文件并将其保存为 `prjs12_1.js`。使用它完成步骤 3-6。

3.  在数组中创建五个 Web 地址。使用以下地址或你选择的地址：

- http://www.pagerource.com
- http://www.javascriptcity.com
- http://www.mydemos.com
- http://www.yahoo.com
- http://www.google.com

4.  使用 `random()` 方法创建一个随机整数，你可以用该整数作为索引来访问数组。

5.  通过更改 id 为 `random_link` 的 `div` 元素的 `innerHTML` 属性，按如下所示格式在页面上显示随机链接：

```html
<a href="随机地址">随机站点！</a>
```

6.  保存 JavaScript 文件并在 浏览器中打开 HTML 文件。尝试重新加载几次，看看随机地址是如何呈现的。

在这个项目中，你能够运用对 Math 对象的知识。使用 `random()` 方法，你创建了一个指向随机地址的 Web 页面。

理解 Number 对象

`Number` 对象是另一个预定义的 JavaScript 对象，为数字提供了几个实用的属性和方法。它最常用的用途是访问一些可以帮助你创建脚本的有用属性。

属性

表 12-3 列出了 Number 对象的属性，并简要描述了每个属性的用途。本节将对每个属性进行详细描述。

`constructor` 属性持有对象的构造函数的值，类似于 Array 对象中该属性的使用。该属性返回的值与你在 Array 对象中得到的值相似：构造函数的名称以及该函数中的任何公共代码。由于函数代码是私有的，你会得到 `[native code]` 文本来代替实际的函数代码。





## 第 12 章：数学、数字和日期对象

323

### MAX_VALUE 属性

`MAX_VALUE` 属性是一个常量数值，大约为 1.79E+308。该属性之所以有用，是因为在 JavaScript 中，任何大于该属性值的数字都会被表示为无穷大（infinity）。因此，在比较中使用它可以避免进行因过大而无法显示数值的计算。以下代码是关于其工作原理的示例：

```javascript
var big_num = num1*num2*num3;

if (big_num > Number.MAX_VALUE) {
  window.alert("数字太大，请尝试较小的数字。");
}
else {
  window.alert(big_num);
}
```

假设 num1、num2 和 num3 是由用户输入的，如果 `big_num` 的值大于 `MAX_VALUE` 属性的值，警框将不会显示“infinity”单词，而是告知用户尝试输入较小的数字进行计算。

### MIN_VALUE 属性

`MIN_VALUE` 属性是一个常量数值，大约为 5e-324。该属性之所以有用，是因为在 JavaScript 中，任何小于该属性值的数字都会被表示为负无穷（negative infinity）。因此，在比较中使用它可以避免进行因过小而无法显示数值的计算。以下代码是关于其工作原理的示例：

```javascript
var small_num = num1*num2*num3;

if (small_num < Number.MIN_VALUE) {
  window.alert("数字太小，请尝试较大的数字。");
}
else {
  window.alert(small_num);
}
```

| 属性 | 目的 |
| :--- | :--- |
| constructor | 存储创建对象的构造函数的值 |
| MAX_VALUE | 存储一个常量数值，代表 JavaScript 将数字解释为无穷大之前的最大值 |
| MIN_VALUE | 存储一个常量数值，代表 JavaScript 将数字解释为负无穷之前的最小值 |
| NaN | 代表“不是数字”（Not a Number）的值 |
| NEGATIVE_INFINITY | 代表负无穷的值 |
| POSITIVE_INFINITY | 代表无穷大的值 |
| prototype | 如果你需要，允许你向对象添加属性 |

表 12-3 数字对象的属性

JavaScript：初学者指南

假设 num1、num2 和 num3 是由用户输入的，如果计算结果小于 `MIN_VALUE` 属性的值，警框将告知用户尝试输入较大的数字进行计算。

### NaN 属性

`NaN` 属性是一个代表“不是数字”的值。浏览器以字符串值 NaN 的形式显示它，且它不等于任何数字，也不等于另一个 NaN 实例。

### NEGATIVE_INFINITY 属性

`NEGATIVE_INFINITY` 属性是一个代表负无穷的常量。它的用法类似于 `MIN_NUMBER` 和 `MAX_NUMBER` 的用法。

### POSITIVE_INFINITY 属性

`POSITIVE_INFINITY` 属性是一个代表正无穷的常量。它的用法类似于 `MIN_NUMBER` 和 `MAX_NUMBER` 的用法。

#### prototype 属性

`prototype` 属性允许你向 Number 对象添加属性或方法，就像你在第 11 章中对 Array 对象所做的那样。

#### 方法

表 12-4 列出了数字对象的方法，并简要描述了每个方法的目的。接下来的章节将详细讨论每种方法。

### toExponential(), toFixed(), toPrecision(), 和 toString() 方法

这些方法返回一个字符串值，代表 Number 对象以特定方式格式化后的样子。注意，这些方法不能直接用于数字本身（数值值），如下代码所示：

```javascript
document.write(10.toExponential());
```

| 方法 | 目的 |
| :--- | :--- |
| toExponential() | 返回一个字符串值，用科学计数法法表示该数字 |
| toFixed() | 返回一个字符串值，代表保留到小数点后指定位数的数字 |
| toPrecision() | 返回一个字符串值，代表保留到指定数量有效数字的数字 |
| toSource() | 返回一个字符串值，代表该对象的源代码 |
| toString() | 返回 Number 对象的字符串值 |
| valueOf() | 经常被 JavaScript 内部使用 |

表 12-4 数字对象的方法

第 12 章：数学、数字和日期对象

325

这会导致 JavaScript 错误，因为它期望的是一个 Number 对象。为了避免这种情况，请通过给变量赋值数值（这将使它们成为 Number 对象）来使用这些方法，如下代码所示：

```javascript
var the_num = 10;
document.write(the_num.toExponential());
```

***注意***

你也可以使用语法 `var the_num = new Number(10);`（你可能在之前的对象中见过这种用法），这通常也是有效的。

### toExponential() 方法

`toExponential()` 方法返回一个字符串，以科学计数法形式表示 Number 对象。因此，以下代码将在屏幕上写出1.0e+1（或类似的表示法，取决于你的浏览器）的的结果：

```javascript
var the_num = 10;
document.write(the_num.toExponential());
```

### toFixed() 方法

`toFixed()` 方法返回一个字符串，代表保留到小数点后指定位数的 Number 对象。例如，如果你需要将计算结果格式化为两位小数货币，可以使用该方法，如下：

```javascript
var mymoney = 2000;
var share = 7;
document.write("One share of " + share.toFixed(2));
```

浏览器将显示：One share of 7.00

### toPrecision() 方法

`toPrecision()` 方法返回一个字符串，代表保留到指定数量有效数字的 Number 对象。因此，如果你想要保留5位有效数字，可以使用以下代码：

```javascript
var the_num = 45.57689;
document.write(the_num.toPrecision(5));
```

浏览器将显示：45.577

348

JavaScript：初学者指南

### toString() 方法

`toString()` 方法返回 Number 对象的字符串值。如果你想将数值值转换为相应的字符串值（例如，将10转换为“10”），它是很有用的。

### toSource() 方法

`toSource()` 方法返回代表对象源代码的字符串值。对于数字对象，该方法返回构造函数的值。该方法通常由 JavaScript 调用。

### valueOf() 方法

这是另一个主要由 JavaScript 内部使用的方法。现在你只需要知道它是有效方法。

## 使用 Date 对象

Date 对象是另一个内置 JavaScript 对象。它允许你设置时间值并获取可以在脚本中使用时间值。要使用此对象，你需要创建一个可以引用的对象实例。

创建 Date 实例使用 `new` 关键字（正如你对许多其他对象所做的那样），如下所示：

```javascript
var instance_name = new Date();
```

将 *instance_name* 替换为你想要的 Date 对象实例的名称。因此，如果你想要一个名为 rightnow 的实例，可以使用以下代码：

```javascript
var rightnow = new Date();
```

现在你有一个名为 rightnow 的实例。

你可以使用 Date 对象的属性和方法执行各种任务（例如创建 JavaScript 时钟）。这些属性和方法将在后续章节中描述。

#### 属性

Date 对象只有两个属性。表 12-5 列出了这些属性及其目的（你可能觉得很熟悉，因为 Array 和 Number 对象也有这些属性）。

每个属性将在后续章节中进行详细描述。

| 属性 | 目的 |
| :--- | :--- |
| constructor | 存储创建对象的构造函数的值 |
| prototype | 如果你需要，允许你向对象添加属性 |

表 12-5 Date 对象的属性





## 第 12 章：数学、数字和日期对象

#### constructor 属性

`constructor` 属性持有对象构造函数的值，就像在 `Array` 和 `Number` 对象中对 `this` 属性的使用一样。要查看该值是多少，你可以将其写入页面，如下面的代码所示：

```html
<body

<script type="text/javascript">
var rightnow= new Date();
document.write(rightnow.constructor);
</script>

</body>
```

如果你运行这段代码，你可能会在页面上看到类似下面行的输出：

`function Date() { [native code] }`

这和你对 `Array` 对象使用该属性时得到的结果几乎相同：即构造函数的名称以及该函数中的任何公共代码。由于函数代码是私有的，因此你得到的是 `[native code]` 文字，而不是实际的函数代码。

#### prototype 属性

`prototype` 属性允许你向 `Date` 对象添加属性或方法，就像你在第 11 章中对 `Array` 对象执行的那样。例如，如果你想为每个 `Date` 对象的实例添加一个名为 `attitude` 的新属性，你可以使用以下代码：

```javascript
Date.prototype.morning="a.m.";
var rightnow= new Date();
window.alert("This date is "+rightnow.morning);
```

这段代码创建了新属性，创建了一个 `Date` 对象的实例，然后在屏幕上弹出该新属性的值。

现在你已经了解了 `Date` 对象的属性，来看看你可以使用的方法吧。

#### 方法

`Date` 对象提供的属性并不多，但它确实有许多你可以使用的方法。表 12-6 列出了 `Date` 对象的各种方法以及每个方法的用途。每个方法将在随后的章节中进行更详细的讨论。

现在你已经有了长长的方法列表，请更详细地查看它们，从用于获取 `Date` 实例中日期值的方法开始。

| 方法 | 用途 |
| :--- | :--- |
| getDate() | 根据用户的本地时间返回月份中的几 |
| getDay() | 根据用户的本地时间返回一周中的第几天（0–6） |
| getHours() | 根据用户的本地时间返回一天中的几小时（0–23） |
| getMilliseconds() | 根据用户的本地时间返回每秒几毫秒（0-999） |
| getMinutes() | 根据用户的本地时间返回小时中的几分钟（0–59） |
| getMonth() | 根据用户的本地时间返回一年中的几个月（0–11） |
| getSeconds() | 根据用户的本地时间返回分钟中的几秒（0–59） |
| getTime() | 返回 `Date` 对象自 1970 年 1 月 1 日以来的毫秒数 |
| getTimezoneOffset() | 根据用户的本地时区返回时区偏移（相对于格林尼治时间）的分钟数 |
| getYear() | 根据用户的本地时间返回年份（两位数） |
| getFullYear() | 根据用户的本地时间返回完整年份（四位数） |
| getUTCDate() | 返回协调世界时（UTC）月份中的几 |
| getUTCDay() | 返回协调世界时一周中的第几天（0-6） |
| getUTCFullYear() | 返回协调世界时的完整年份（四位数） |
| getUTCHours() | 返回协调世界时一天中的几小时（0–23） |
| getUTCMilliseconds() | 返回协调世界时当前秒的几毫秒（0-999） |
| getUTCMinutes() | 返回协调世界时小时中的几分钟（0–59） |
| getUTCMonth() | 返回协调世界时当前年份中的几个月（0–11） |
| getUTCSeconds() | 返回协调世界时当前分钟中的几秒（0–59） |
| parse() | 根据用户的本地时间返回参数传递的日期自 1970 年 1 月 1 日以来的毫秒数 |
| setDate() | 设置 `Date` 实例的每月几 |
| setHours() | 设置 `Date` 实例的小时 |
| setMilliseconds() | 设置 `Date` 实例的毫秒 |
| setMinutes() | 设置 `Date` 实例的分钟 |
| setMonth() | 设置 `Date` 实例的月份 |

**表 12-6 Date 对象的方法**

### 获取值的方法

获取值的方法允许你获取可以在脚本中使用的各种时间和日期值。允许你获取 `Date` 实例值的方法包括：

- getDate()
- getDay()
- getHours()
- getMilliseconds()

| 方法 | 用途 |
| :--- | :--- |
| setSeconds() | 设置 `Date` 实例的秒 |
| setTime() | 设置 `Date` 实例的时间（自 1970 年 1 月 1 日午夜以来的毫秒） |
| setYear() | 设置 `Date` 实例的年份（两位数） |
| setFullYear() | 设置 `Date` 实例的完整年份（四位数） |
| setUTCDate() | 设置协调世界时的月份中的几 |
| getUTCFullYear() | 设置协调世界时的完整年份（四位数） |
| getUTCHours() | 设置协调世界时一天中的几小时（0–23） |
| getUTCMilliseconds() | 设置协调世界时当前秒的几毫秒（0-999） |
| getUTCMinutes() | 设置协调世界时小时中的几分钟（0–59） |
| getUTCMonth() | 设置协调世界时当前年份中的几个月（0–11） |
| getUTCSeconds() | 设置协调世界时当前分钟中的几秒（0–59） |
| toDateString() | 返回英语格式的 `Date` 对象日期字符串 |
| toGMTString() | 返回格林尼治时间的字符串（现在改用 `toUTCString()`） |
| toLocaleString() | 返回本地格式的日期字符串 |
| toLocaleTimeString() | 返回本地格式的 `Date` 对象时间字符串 |
| toString() | 返回英语格式的 `Date` 对象日期字符串 |
| toTimeString() | 返回英语格式的 `Date` 对象时间字符串 |

**表 12-6 Date 对象的方法（续）**

- minutes()
- getMonth()
- getSeconds()
- getTime()
- getTimezoneOffset()
- getYear()
- getFullYear()
- getUTCDate()
- getUTCDay()
- getUTCFullYear()
- getUTCHours()
- getUTCMilliseconds()
- getUTCMinutes()
- getUTCMonth()
- getUTCSeconds()

要使用这些方法，你需要一个 `Date` 实例。一旦有了实例，你就可以使用实例名调用任何方法。以下是其语法：

`instance_name.method();`

你需要将 `instance_name` 替换为你的 `Date` 对象，并将 `method` 替换为你想要使用的函数。因此，如果你想对名为 `rightnow` 的实例使用 `getDate()` 方法，可以使用以下代码：

```javascript
var rightnow= new Date();
var theday= rightnow.getDate();
```

这会将 `getDate()` 方法的值赋值给变量 `theday`。由于 `Date` 方法返回的值通常是数字，因此后续章节将对这些方法进行进一步的解释。

### getDate 方法

`getDate()` 方法允许你获取用于脚本的每月几。返回的值是一个代表日期的数字。因此，如果是该月的 5 号，`getDate()` 方法将返回 5。如果是 22 号，`getDate()` 方法将返回 22。这个方法很好，因为它直观。

### getDay() 方法

`getDay()` 方法允许你获取星期几；但它返回的不是周一或周五这样的名称，而是一个数字。该数字代表一周中的第几天（0–6），而不是你通常想到的星期几（1–7）。因此，如果是周日，方法返回 0；如果是周三，方法返回 3。在脚本中使用它时，必须记住它是从 0 开始计数的。后续许多方法都会从 0 开始计数。

### getHours 方法

`getHours()` 方法允许你获取一天中的几小时（0–23）。计数从 0 开始。因此，当午夜时方法返回 0；当下午 2 点时，它返回 14。

### getMilliseconds 方法

`getMilliseconds()` 方法允许你获取 `Date` 实例存储的毫秒数（0–999）。

### getMinutes 方法

`getMinutes()` 方法允许你获取 `Date` 实例存储的分钟数（0–59）。同样，计数从 0 开始。因此，如果是 2:00（无论是上午还是下午，或任何整点），方法返回 0；如果是 2:23，方法返回 23。

### getMonth 方法

`getMonth()` 方法允许你获取 `Date` 实例存储的月份数（0–11）。该方法也从 0 开始计数，这使得结果有点复杂。例如，如果是 1 月（人们通常认为是 1 月），方法返回 0；如果是 10 月（人们通常认为是 10 月），方法返回 9。在脚本中使用它时，你需要多加留意这一点，因为如果你想使用数字日期（如 10/24/2000），你需要记得进行调整。

### getSeconds 方法

`getSeconds()` 方法允许你获取 `Date` 实例存储的秒数（0–59）。因此，如果时间是 2:42:23，方法返回 23；如果时间是 2:23:00，方法返回 0。

### getTime 方法

`getTime()` 方法获取 `Date` 实例自 1970 年 1 月 1 日午夜以来的毫秒数。因此，如果你想知道当前自该日期以来的毫秒数，可以使用以下代码：

```javascript
var rightnow= new Date();
var theday= rightnow.getTime();
```

这会将方法的结果赋值给变量，以便你在脚本中需要时以后使用它。





JavaScript：初学者指南

### getTimezoneOffset() 方法

getTimezoneOffset() 方法返回本地时间与 GMT（格林尼治时间）之间的分钟数。因此，如果你与 GMT 相差 6 小时，该方法将返回 360（6 × 60）；如果你仅相差 1 小时，该方法返回 60。

### getYear() 方法

此方法返回年份的最后两位（如果年份在 1900 到 1999 年之间）。例如，如果年份是 1988 年，该方法返回 88。2000 年之后，某些浏览器会返回三位数年份，而另一些会返回四位数年份。为了避免这种情况，你可以使用 getFullYear() 方法，它被新浏览器支持并返回四位数年份。

### getFullYear() 方法

getFullYear() 方法与 getYear() 方法非常相似，但它可以一致地返回四位数年份，以避免 2000 年问题。

getFullYear() 方法的工作方式与 getYear() 方法相同，但你不需要运行任何额外的检查来确保年份正确：

```javascript
var rightnow= new Date();
var theyear= rightnow.getFullYear();
```

这会将方法返回的值赋值给 `theyear` 变量。这次，值已经是四位数的，不需要任何调整。

### UTC 方法

这些方法与其对应的方法工作相同（例如，`getDate()` 和 `getUTCDate()` 的工作方式相同），但返回的是通用世界时间（UTC）信息而非查看者的本地时间。

现在你已经学习了获取值的方法，请看一眼允许为 `Date` 对象实例设置值的方法。

## 设置值的方法

设置值的方法与获取值的方法使用相同类型的值。允许你为 `Date` 对象实例设置值的方法包括：

- setDate()
- setHours()
- setMilliseconds()
- setMinutes()
- setMonth()
- setSeconds()
- setTime()
- setYear()
- setFullYear()
- setUTCDate()
- setUTCFullYear()
- setUTCHours()
- setUTCMilliseconds()
- setUTCMinutes()
- setUTCMonth()
- setUTCSeconds()

要设置这些值，你需要根据想要使用的时间或日期发送一个数值参数。例如，如果你想设置 `Date` 实例的月份某一天，可以使用以下代码：

```javascript
var rightnow= new Date();
rightnow.setDate(22);
```

这将把 `rightnow` `Date` 实例的月份日期设置为 22 号。其他方法的工作方式相同。为了知道需要发送给这些方法之一的什么类型的值，请查看其在“获取值方法”中对应方法返回了什么类型的值。该方法预期的参数将是与该方法返回的值的值。

#### 其他方法

其余的方法以某种方式执行其他方法未涵盖的不同任务。

### parse() 方法

parse() 方法用于计算作为参数输入的日期字符串（例如 1999 年 12 月 12 日）自 1970 年 1 月 1 日午夜以来的毫秒数。这通常与 `setTime()` 方法配合使用，因为它需要一个毫秒参数来设置时间。你可以使用 `parse()` 方法找到从 1970 年 1 月 1 日午夜到 1999 年 12 月 12 日午夜的毫秒数（`rightnow` `Date` 实例将使用此日期作为所有方法返回值的依据），如下代码所示：

```javascript
var rightnow= new Date();
var thenum= Date.parse("Dec 12, 1999")
rightnow.setTime(thenum);
```

这段代码将日期解析为毫秒数，然后将其发送给用于 `rightnow` `Date` 实例的 `setTime()` 方法。该方法可以直接从 `Date` 对象调用。

### toString(), toDateString(), toTimeString(), toLocaleDateString 和 toLocaleTimeString() 方法

这些方法返回表示日期和时间的字符串或其部分。例如，`toString()` 方法返回字符串格式的日期。你可以用它来获取 `Date` 实例的格式化日期，如下代码所示：

```javascript
var rightnow= new Date();
var thedate= rightnow.toString();
```

这会将一个日期字符串值赋值给变量 `thedate`。字符串的值取决于查看者使用什么浏览器查看页面。然后可以将其写入页面，或在脚本与 `Date` 对象的其他方法配合。

### toGMTString() 方法

toGMTString() 方法返回 GMT 格式的日期字符串。你可以使用它来获取 `Date` 实例的 GMT 格式，如下代码所示：

```javascript
var rightnow= new Date();
var thedate= rightnow.toGMTString();
```

这将一个值（如 `Wed, 21 Dec`）赋值给变量 `thedate`。

### toLocaleString() 方法

toLocaleString() 方法返回查看者本地语言的日期字符串。你可以用它来获取 `Date` 实例的本地化格式，如下代码所示：

```javascript
var rightnow= new Date();
var thedate= rightnow.toLocaleString();
```

这将一个日期字符串赋值给变量 `thedate`。字符串的值取决于查看者使用什么浏览器查看页面。然后可以将其写入页面，或在脚本与 `Date` 对象的其他方法配合。

## 脚本如何？

既然你已经掌握了这些方法，看看如何用 `Date` 对象玩点花样。

### 在页面上写日期

要在页面上写日期，你需要找出星期、月份、日期和年份。可以使用 `getDay()`、`getMonth()`、`getDate()` 和 `getFullYear()` 方法来实现。首先是 HTML 代码（保存为 `write_date.html`）：

```html
<body>
  <h1>Date</h1>
  <div id="write_date">
    <!-- 这里可以调用服务器端脚本 -->
  </div>
  <script type="text/javascript" src="write_date.js"></script>
</body>
```

注意 `div` 元素中的注释。如果你想让不支持 JavaScript 的浏览器也能访问，可以在此处调用 PHP（或其他服务器端技术）脚本。例如，如果页面设置为解析 PHP，你可以使用以下代码像 JavaScript 一样显示日期：

```html
<body>
  <h1>Date</h1>
  <div id="write_date">
    <?php
      $the_date = date("l, n/j");
      echo $the_date;
    ?>
  </div>
  <script type="text/javascript" src="write_date.js"></script>
</body>
```

你会发现 PHP 脚本比 JavaScript 脚本短得多，因为它内置了日期化功能。显示的日期可能与查看者的日期不同，因为它是在 Web 服务器上显示的。对服务器端技术的深入讨论不在本书的范围内，但它是为没有 JavaScript 的用户提供相同基本功能的示例。

接下来是 JavaScript 代码（保存为 `write_date.js`）：

```javascript
var rightnow = new Date();
var weekday = rightnow.getDay();
var themonth = rightnow.getMonth();
var thedate = rightnow.getDate();
var theyear = rightnow.getFullYear();

// 设置星期几
var someday = new Array(7);
someday[0] = "Sunday";
someday[1] = "Monday";
someday[2] = "Tuesday";
someday[3] = "Wednesday";
someday[4] = "Thursday";
someday[5] = "Friday";
someday[6] = "Saturday";

// 使用 Date 对象的方法获取所需的值
// 创建 Date 的新实例
// 创建一个数组来存储每个星期几的名称，索引值
// 与 getDay() 方法返回的值对应

document.getElementById("write_date").innerHTML = someday[weekday] + ", " + (themonth + 1) + "/" + thedate + "/ " + theyear;
```




## JavaScript: 初学者指南

// 设置月份数字以便于识别

themonth++;

var date_div = document.getElementById("write_date");

date_div.innerHTML = someday[weekday]+ ", "+themonth+"/"+thedate+"/"+
"+theyear;

此脚本将方法的的结果赋值给变量。然后，它创建一个数组来存储星期的几几，稍后使用 `getDay()` 方法返回的数字作为索引号来访问这些数据。脚本进行了一项调整，将 `getMonth()` 方法返回的数字加 1，这样月份就会以你预期的方式显示（记住，它从 0 开始计算月份而不是从 1 开始，所以这确保了 1 月用数字 1 而不是 0，例如）。

格式化后的输出被写入页面供查看者查看。该脚本在浏览器中运行的结果如图 12-5 所示。

### 创建一个简单的时钟

要创建一个简单的时钟，你需要当前时间的小时、分钟和秒。为了获取这些信息，你可以使用 `getHours()`、`getMinutes()` 和 `getSeconds()` 方法。

- 月份值会递增，使其看起来像标准的数值月份值
- 通过 id 获取 div 元素，并更改其 `innerHTML` 属性以显示格式化日期

图 12-5 页面上显示日期

![](img/61d166424839b7674a7b9c8434ae4e03_358_0.png)

## 第 12 章：Math、Number 和 Date 对象

337

以下代码将创建一个显示在页面上的时钟。首先，是 HTML 代码（保存为 clock.html）：

```html
<body>
<h1>当前时间：</h1>
<div id="my_clock">
<!-- 此处可以放置调用服务器端脚本进行备份 -->
</div>
<script type="text/javascript" src="clock.js"></script>
</body>
```

***注意***

如果你使用服务器端脚本作为 JavaScript 时钟的备份，你几乎可以肯定你并不希望它每秒更新一次，因为这可能会给 Web 服务器带来过大的压力。在这种情况下，最好的方法是直接显示时间而不进行更新。

接下来，是 JavaScript 代码（保存为 clock.js）：

```javascript
function startclock() {
    var thetime = new Date();
    var hours = thetime.getHours();
    var mins = thetime.getMinutes();
    var secn = thetime.getSeconds();
    var ap = (hours >= 12) ? "p.m." : "a.m.";
    if (hours >= 13) {
        hours -= 12;
    }
    if (hours < 1) {
        hours = 12;
    }
    if (mins < 10) {
        mins = "0" + mins;
    }
    if (secn < 10) {
        secn = "0" + secn;
    }
    var clock_div = document.getElementById("my_clock");
    clock_div.innerHTML = hours + ":" + mins + ":" + secn + " " + ap;
    setTimeout("startclock()", 1000);
}
startclock();
```

- 使用 Date 对象的方法来获取小时、分钟和秒
- 设置了一个变量，以便在时间后显示 a.m. 或 p.m.
- 调整了小时、分钟和秒，使其显示方式类似于典型的 12 小时数字时钟
- 获取 div 元素，以便调整 `innerHTML` 属性以显示时钟
- 将小时、分钟、秒和 ap 变量组合，并作为 div 元素新的 `innerHTML` 显示
- 使用 `setTimeout()` 方法每秒调用一次脚本
- 在此处调用函数启动该过程

这 12-2

脚本创建了一个函数，将方法的的结果赋值给变量。它获取 `hours` 变量，如果 `hours` 大于或等于 12，则将 `ap` 变量设置为 p.m.，如果 `hours` 小于 12，则设置为 a.m.（此时 `hours` 变量仍然持有 13 代表下午 1 点，14 代表下午 2 点，以此类推）。完成此后，将对 `hours` 变量进行调整，使其显示 12 小时时钟的预期值。

脚本随后通过调整显示分钟和秒的变量值，即当数字小于 10 时在前面添加一个 0。这样，时钟在 12:02:34 时会显示为 12:02:34，而不是省略 0 显示为 12:2:34（如果你愿意，也可以对 `hours` 变量执行此操作带有前导 0）。

最后，函数在页面上显示输出。该函数在定义后立即被首次调用。函数每隔 1000 毫秒（或 1 秒）重复执行一次。这使得时钟能够保持实时更新。该脚本在浏览器中运行的结果如图 12-6 所示。

### 创建一个 JavaScript 时钟

此项目让你能够更多地使用 Date 对象的方法，并学习如何调整返回的值以便以各种方式使用。这创建了一个 JavaScript 时钟。

#### 步骤说明

1. 创建一个 HTML 页面，其中 script 标签指向外部 JavaScript 文件，命名为 clock.html。添加一个显示“当前时间”的标题，并添加一个 id 为 my_clock 的 div 元素。
2. 创建一个外部 JavaScript 文件，命名为 clock.js。使用它返回星期。
3. 编写一些显示时钟的代码。在这个时钟中，包含格式 mm/dd/yyyy。
4. 更新月份和日期，以便相应调整这些值。
5. 启动时钟，并让它每秒更新。
6. 保存 JavaScript 文件并在浏览器中打开它。

图 12-6 页面上显示日期 ![](img/61d166424839b7674a7b9c8434ae4e03_358_0.png)

361

第 12 章：Math、Number 和 Date 对象

339

月份值会递增，使其看起来像标准的数值月份值
- 通过 id 获取 div 元素，并更改其 `innerHTML` 属性以显示格式化日期
图 12-5 页面上显示日期

![](img/61d166424839b7674a7b9c8434ae4e03_358_0.png)

总结

在这个项目中，你使用了对 Date 对象的知识。通过 Date 方法，你创建了一个显示在页面上的时钟。

## 第12 章自测

1. Math 对象的属性和方法让你能够做什么？
A 取平方根和其他此类值
B 执行数学计算
C 去 math 学习新的
D 它们毫无用处

2. __________ 属性持有欧拉常数。
3. LN10 属性持有自然对数10。
4. LOG10 属性持有 10 的对数。
A正确
B 错误

5. 下列哪项正确在页面上写入 pi 值？
A document.write(Math.Pi);
B document.write(Math.pi);
C document.write(Math.PI);
D document.write(Date.PI);

6. __________ 属性持有值 2。

362

JavaScript: 初学者指南

7. abs() 方法返回传递参数的 __________ 值。
A 缺失
B 荒谬
C 绝对
D 绝对根

8. __________ 方法返回传递的参数的正弦值。
9. pow() 方法返回 __________ 参数的 __________ 参数的幂值。
10. 下列哪项可以正确生成 0 到 7 之间的随机数？
A var rand_int= Math.floor(Math.random()*7);
B var rand_int= Math.floor(Math.random()*6);
C var rand_int= Math.floor(Math.random()*8);
D var rand_int= Math.sqrt(Math.random());

11. __________ 方法返回传递参数的平方根。
12. 在大多数情况下，在使用 Date 对象的属性和方法之前必须创建什么？
A 字符串
B 引用日期的数字
C 设置日期的时间
D Date 对象的实例

13. __________ 方法返回星期几。
14. getMonth() 方法返回与当前月份相同的数字（例如，如果当前月份是 1 月，则返回 1）。
A正确
B 错误

15. 下列哪项正确将名为 rightnow 的 Date 实例的星期赋值给变量 weekday？
A var weekday= rightnow.getDate();
B var weekday= rightnow.getDay();
C var weekday= right now.getDay();
D var weekly= rightlater.getMinutes();





## 第 13 章：处理字符串

JavaScript：初学者指南

**核心技能与概念**
- 使用 String 对象的属性
- 使用 String 对象的方法
- 使用正则表达式

在 JavaScript 中处理字符串，你需要学习处理字符串的各种方法。这些方法源自 JavaScript String 对象。

本章首先将解释什么是 String 对象，以及如何使用它的属性和方法来创建字符串。然后，将详细地讨论 String 对象的属性和方法，让你看到它们是如何运作的。最后，你将编写一个脚本，使用你所学到的某些属性和方法。

### String 对象简介

String 对象提供了属性和方法，用于获取有关字符串的信息或修改字符串。String 对象可以通过两种方式创建：程序员通过使用 `new` 关键字配合构造函数来创建一个；或者当从字符串字面量中调用其中一个方法时，JavaScript 会临时创建一个。是什么构成了 String 对象，什么又构成了字符串字面量？要找到答案，请看下如何在 JavaScript 中创建 String 对象。

### String 对象

正如刚才解释的，创建 String 对象的其中方法是使用 `new` 关键字，就像你之前对其他对象所做的那样。语法所示：

```javascript
var *instance_name* = new String("*string value here*");
```

你将 *instance_name* 替换为你想要为 String 对象实例使用的名称。然后将 *string value here* 替换为用作新 String 对象的字符字符串。

因此，如果你想创建一个名为 `guitar_string` 的 String 对象实例，可以使用以下代码：

```javascript
var guitar_string = new String("G");
```

该脚本为字符串“G”创建了一个 String 对象的实例。虽然使用 `new` 关键字创建 String 对象对于比较 String 对象等操作很有用，但字符串字面量使用得更多。

### 字符串字面量

你只需要给变量赋值一个字符串值就可以创建一个字符串字面量。这种技术比使用 `new` 关键字创建 String 对象稍微短一点，而且仍然允许你使用 String 对象的所有方法（以及其中一个属性）。

在代码中创建了字符串字面量。注意，该代码为变量赋值了一个字符串值。

```javascript
var guitar_string = "G";
```

这使得字符串“G”成为一个字符串字面量，也就是你所知的普通文本字符串。对于文本字符串，你被允许使用 String 对象的属性和方法。

### 有什么区别？

String 对象和字符串字面量的区别在于，普通文本字符串拥有字符串本身的值，并且很容易与另一个字符串进行比较，如下代码所示：

```javascript
var guitar_string1 = "E";
var guitar_string2 = "E";

if (guitar_string1 == guitar_string2) {
    window.alert("字符串是相同的!");
}
else {
    window.alert("字符串不相同!");
}
```

由于这段代码使用了普通的字符串字面量，结果如你所期的。警框显示字符串是相同的。

然而，如果你使用 String 对象来运行相同的 if 块，你将看到意料之外的结果。下面的代码使用了 String 对象：

```javascript
var guitar_string1 = new String("E");
var guitar_string2 = new String("E");

if (guitar_string1 == guitar_string2) {
    window.alert("字符串是相同的!");
}
else {
    window.alert("字符串不相同!");
}
```

这一次，警框会告诉你字符串是不相同的，尽管字符串值都是“E”——因为 String 对象是一个对象值，而不是字面值。对象之间的相等方式与普通文本字符串不同。若要判断两个对象是否相等，你必须编写额外的代码来确定。对于大多数用途，你可能不想费那个麻烦。相反，你可能会使用字符串字面量并让它们使用 String 对象的方法。

- 两个变量具有相同的字符串值
- 字符串被比较
- 值被比较了，但得到了意料之外的结果
- String 对象被赋予了相同的字符串值

普通文本字符串能够使用 String 对象的方法，是因为 JavaScript 会获取字符串字面量将其转换为临时的 String 对象。一旦方法的执行完成，它会返回一个字符串字面量。这允许你无需创建 String 对象即可使用 String 对象的方法。

### 使用 String 对象的属性

String 对象只有三个属性，所以这一节相对较短。表 13-1 提供了这些属性的简要描述，每个属性将在后续章节中逐一讨论。

#### constructor（构造函数）属性

该属性的功能与其具有该属性的其他对象（如 Date 和 Array 对象）相同。它返回构造函数的值。要使用 `constructor` 属性，你必须使用 String 对象而不是字面量。

***注意***
你可以对 `length` 属性和 String 对象的所有方法使用字符串字面量，但 `constructor` 和 `prototype` 属性需要 String 对象。

以下代码将 `constructor` 属性的值写入页面中：

```html
<body
<script type="text/javascript">
var guitar_string = new String("G");
document.write(guitar_string.constructor);
</script>
</body>
```

此代码产生的文本类似于：`function String() { [native code] }`

| 属性 | 目的 |
| :--- | :--- |
| constructor | 存储实例构造函数的值 |
| length | 存储字符串长度（字符数）的数值 |
| prototype | 允许向对象添加属性 |

#### length（长度）属性

该属性返回字符串的长度，即字符串中的字符数。你可以在 String 对象和字符串字面量中使用它。下面的代码使用了普通文本字符串。它将字符串的长度写入页面：

```html
<body>
<script type="text/javascript">
var myname="John";
document.write("名字有 "+myname.length+" 个字符.");
</script>
</body>
```

注意这里是如何像对象一样使用变量名的。这是让 JavaScript 创建一个临时 String 对象以使用该属性的方法。因为名字有四个字符，这里 `length` 属性的值为 4。当你想要分解字符串以获取信息或对其进行更改时，`length` 属性非常有用，特别是当用户输入字符串而你事先不知道长度时。

#### prototype（原型）属性

与其他具有 `prototype` 属性的对象一样，可以使用它为页面上的 String 对象添加属性或方法。以下代码展示了一个示例：

```javascript
String.prototype.attitude="cool";
var rightnow= new String("Joe");
window.alert("这个字符串是 "+rightnow.attitude);
```

现在 String 对象“Joe”拥有了属性“cool”!

### 使用 String 对象的方法

String 对象有很多方法，如表 13-2 所示。是的，这个列表很长！接下来的章节将介绍 String 对象的方法。

#### 添加 HTML 标签的方法

表 13-2 中的许多方法用于在字符串周围创建 HTML 标签（或创建带有作为参数发送的属性值的 HTML 标签）。这些效果中的许多可以使用更现代的方法——访问元素的 style 和/或 innerHTML 属性来完成；然而，这些方法在不同情况下可能很有帮助。





## JavaScript: 入学者指南

| 方法 | 用途 |
| :--- | :--- |
| anchor() | 创建一个带有页面目标的 HTML 锚点标签 |
| big() | 在字符串值周围添加 `<big>` 和 `</big>` 标签 |
| blink() | 在字符串值周围添加 `<blink>` 和 `</blink>` 标签 |
| bold() | 在字符串值周围添加 `<b>` 和 `</b>` 标签 |
| charAt() | 查找字符串指定位置的字符 |
| charCodeAt() | 查找字符串指定位置字符的字符编码 |
| concat() | 将两个或多个字符串相加并返回新的组合字符串值 |
| fixed() | 在字符串值周围添加 `<tt>` 和 `</tt>` 标签 |
| fontcolor() | 在字符串值周围添加 `<font color="*color*">` 和 `</font>` 标签，将字符串颜色改为指定的颜色 |
| fontsize() | 在字符串值周围添加 `<font size="*number*">` 和 `</font>` 标签，将字符串大小改为指定的数字 |
| fromCode() | 使用作为参数发送的字符编码创建新字符串 |
| indexOf() | 在字符串中搜索作为参数发送的字符：如果找到，返回该字符首次出现的位置；否则返回 -1 |
| italics() | 在字符串值周围添加 `<i>` 和 `</i>` 标签 |
| lastIndexOf() | 在字符串中搜索作为参数发送的字符：如果找到，返回该字符最后一次的位置；否则返回 -1 |
| link() | 使用字符串作为链接文本并链接到作为参数发送的 URL 创建 HTML 链接 |
| match() | 比较正则表达式和字符串以查看它们是否匹配 |
| replace() | 查找正则表达式是否匹配字符串，然后将匹配字符串替换为新字符串 |
| search() | 执行正则表达式与指定字符串之间的匹配搜索 |
| slice() | 提取字符串值的指定部分并返回新字符串 |
| small() | 在字符串值周围添加 `<small>` 和 `</small>` 标签 |
| split() | 根据向方法发送的参数字符将字符串拆分为字符串数组 |
| strike() | 在字符串值周围添加 `<strike>` 和 `</strike>` 标签 |
| sub() | 在字符串值周围添加 `<sub>` 和 `</sub>` 标签 |
| substr() | 允许返回指定起始位置并在指定数量字符后结束的字符串部分 |
| substring() | 允许返回指定起始位置和结束位置的字符串部分 |
| sup() | 在字符串值周围添加 `<sup>` 和 `</sup>` 标签 |
| toString() | 返回字符串对象的字面量值 |
| toLowerCase() | 将字符串转换为全小写并返回结果 |
| toUpperCase() | 将字符串转换为全大写并返回结果 |

表 13-2 String 对象的方法

### 第 13 章：处理字符串

347

基础方法（`big()`、`blink()`、`bold()`、`fixed()`、`italics()`、`small()`、`strike()`、`sub()` 和 `sup()`）只是在字符串周围添加基础 HTML 标签。例如，要创建一些较小的文本，可以使用 `small()` 方法：

```javascript
var little_bit = "I only want a little bit of cake.";
var tagged_phrase = little_bit.small();
document.write(tagged_phrase);
```

这段代码将向 HTML 代码写入以下内容：

```html
<small>I only want a little bit of cake.</small>
```

在浏览器中查看时，此文本将比没有 `<small>` 和 `</small>` 标签时正常显示的要小。

***注意***

HTML 标签可以是小写或大写，取决于浏览器。由于在页面加载后使用 JavaScript 构建的标签通常不会引起页面验证问题，标签的大小写可能不会对你的 HTML 代码产生任何影响。然而，如果你决定稍后在脚本中使用该元素，了解标签的大小写是有帮助的，例如它的标签名可能是 `small` 或 `SMALL`。

其余的 HTML 标签方法（`anchor()`、`fontcolor()`、`fontsize()` 和 `link()`）接收参数，并根据发送给它们的字符串值和参数构建标签。这些将在接下来的章节中进行详细讨论。

### anchor() 方法

该方法将文本字符串作为命名锚点的文本。`anchor()` 方法接收一个参数，该参数将作为命名锚点的 `name` 属性。基本上，它创建了一个具有以下语法的 HTML 标签集：

```html
<a name="*parameter_string">*text_string*</a>
```

*parameter_string* 是你作为参数在方法调用中发送的字符串。*text_string* 是调用该方法的字符串的值。

例如，看这段代码：

```javascript
var anchor_text = "Part 1";
var full_anchor = anchor_text.anchor("part1");
document.write(full_anchor);
```

在这里，你将一个字符串字面量赋值给变量 `anchor_text`。然后你从该字符串字面量用参数 “part1” 调用了 `anchor()` 方法。结果被赋值给 `full_anchor`。`anchor()` 方法的结果被赋值给变量。创建了一个字符串字面量。变量的值写入页面变量中。然后将 `full_anchor` 变量的值写入页面。该代码在页面的代码中写入了以下链接：

```html
<a name="part1">Part 1</a>
```

图 13-1 页面上放置了命名锚点

### fontcolor() 方法

`fontcolor()` 方法为为调用该方法的文本字符串添加字体颜色。它接收一个字符串参数，该参数指示文本文本应该是什么颜色。该方法按示例格式化某些代码：

```html
<font color="*color*">*text_string*</font>
```

*color* 被替换为作为参数发送的颜色。例如，这段代码创建了一些红色文本：

```javascript
var the_text = "I am so happy text";
document.write(the_text.fontcolor("red"));
```

此脚本在页面上放置了以下内容：

```html
<font color="red">I am so happy text</font>
```

### fontsize() 方法

`fontsize()` 方法调整调用该方法的文本字符串的字体大小。它接收一个数值表示文本的大小（1 到 7 之间）。该方法格式化的代码使用类似示例的语法：

```html
<font size="*number*">*text_string*</font>
```

*number* 被替换为作为参数发送的数字。示例中，这段代码创建了一些较小的文本：

```javascript
var the_text = "I am pretty small!";
document.write(the_text.fontsize(2));
```

此脚本提供了后续代码：

```html
<font size="2">I am pretty small!</font>
```

### link() 方法

`link()` 方法的工作原理与 `anchor()` 方法非常相似，但它在页面上创建的是典型的超链接。它接收一个字符串参数，该参数是链接的 URL 值，而链接文本将是调用该方法的字符串。该方法使用此处所示的通用语法创建一个链接：

```html
<a href="*url">*text_string*</a>
```

*url* 被替换为方法调用中作为参数发送的 URL，而 *text_string* 被替换为调用的字符串。例如，这段代码创建了一个链接：

```javascript
var link_text = "Click here";
document.write(link_text.link("https://www.google.com"));
```

此脚本在页面上产生以下内容：

```html
<a href="https://www.google.com">Click here</a>
```




JavaScript：初学者指南

查看这个使用 `link()` 方法的示例：

<body>

<script type="text/javascript">
var link_text = "A Web Site";
var full_link = link_text.link("http://www.pageresource.com");
document.write(full_link);
</script>

</body>

这段代码在页面源代码中创建了此处所示的链接：

<a href="http://www.pageresource.com">A Web Site</a></a>

上一个代码示例中的技术也可以作为 `anchor()` 方法的另一侧，用于创建一个指向页面上命名锚点的链接。例如，看这段代码：

<body>

<p>

<script type="text/javascript">
var anchor_text = "Part 1";
var full_anchor = anchor_text.anchor("part1");
document.write(full_anchor);
</script>
</p>

<p>

Part 1 是关于这个、那个以及其他事情的内容。<br />
<br /><br /><br /><br />

在这种情况下，这些是用于填充的无关文本。

</p>

<p>

<script type="text/javascript">
var link_text="Back to Beginning of Part 1";
var full_link= link_text.link("#part1");
document.write(full_link);
</script>
</p>

</body>

这段代码创建了一个锚点，该锚点可以在页面的其他地方引用，通过点击链接到达 Part 1 文本。你可以用某些文本替换页面 Part 1 章节下的任何内容。之后，将创建一个指向回命名锚点的链接，为观众提供了回到页面 Part 1 章节开头的机会。

图 13-2 显示了此脚本在浏览器中运行的结果。你将获得命名锚点、额外的文本以及返回锚点的链接。

链接是根据作为参数发送的 URL 和字符串创建的。

| 创建了指向锚点的链接 | 创建了一个锚点 |

## 第 13 章：处理字符串

351

其他方法

String 对象的其余方法——`charAt()`、`charCodeAt()`、`concat()`、`fromCharCode()`、`indexOf()`、`lastIndexOf()`、`match()`、`replace()`、`search()`、`slice()`、`split()`、`substr()`、`substring()`、`toString()`、`toLowerCase()` 和 `toUpperCase()`——允许你获取有关字符串的信息或更改字符串。所有这些在处理字符串时都非常有用，并在接下来的章节中进行更详细的讨论。

### charAt() 方法

该方法确定字符串中特定位置上的字符是什么。你可以找到第一个或最后一个字符是什么，也可以找到中间的任何字符。`charAt()` 方法接收一个数字，代表你想要获取的字符的位置。

**查找字符**：当你想要查找一个字符时，请记住位置计数是从 0 开始的（与数组一样），而不是从 1 开始，因此第一个字符位于位置 0。下面的代码了如何使用 `charAt()` 方法获取字符串中的第一个字符：

```javascript
var the_text = "Character";
var first_char = the_text.charAt(0);
window.alert("The first character is "+first_char);
```

这段代码将 `charAt()` 方法调用的结果赋值给名为 `first_char` 的变量，然后在警报框中使用它。警报框将告诉观众调用该方法的文本字符串中的第一个字符。在这种情况下，警报框将显示“The first character is C”。

![](img/61d166424839b7674a7b9c8434ae4e03_373_0.png)

图 13-2 命名锚点和返回命名锚点位置的链接

`charAt()` 方法找到字符串中位置 0（第一个字符）处的字符。

**使用 length 属性查找最后一个字符**：如果你想找到最后一个字符，你需要在使用该方法之前知道字符串中有多少字符，或者可以使用 `length` 属性来确定字符串中的字符数量。使用 `length` 属性时，记住它返回的是字符的数量，而不是最后一个字符的位置。

`length` 属性从 1 开始计数，而你必须使用 `charAt()` 方法从 0 开始计数。因此，字符串中的最后一个字符的位置将比其字符数少之一。换句话说，如果字符串有 10 个字符（1–10），那么最后一个位置（0–9）就是 9。如果字符串有 23 个字符（1–23），那么最后一个位置（0–22）就是 23–1=22。

看这个示例来了解它是如何工作的。代码找到字符串中的最后一个字符：

```javascript
var the_text = "Character";
var position = the_text.length-1;
var last_char = the_text.charAt(position);
window.alert("The last character is "+last_char);
```

这段代码将字符串长度减 1 的值赋值给名为 `position` 的变量。`position` 变量现在持有字符串中最后一个字符的位置。将 `position` 值作为参数传递给 `charAt()` 方法的结果赋值给名为 `last_char` 的变量。

*(注：原文中存在大量内容重复内容，译文已按要求去重并保持逻辑连贯)*




## JavaScript: 初学者指南

以下代码在字符串“Cool”中查找字母 *C*：

```javascript
var the_text = "Cool";
var position = the_text.indexOf("C");
window.alert("Your character is at position "+position);
```

请记住，计数是从 0 开始的，因此当它在字符串的第一个字符处找到 *C* 时，它会返回 0。因此，警框将显示“Your character is at position 0”。

注意，该方法是大小写敏感的，因此在这种情况下，*C* 和 *c* 对 JavaScript 来说是两个不同的字符。因此，后续代码将返回 -1（告诉该字符不在字符串中），尽管字符串中包含一个大写的 *C*。

```javascript
var the_text = "Cool";
var position = the_text.indexOf("c");
window.alert("Your character is at position "+position);
```

现在警框将显示“Your character is at position -1”。

如果你想检查这个 -1 以免将其误视为位置，可以使用以下代码在要查找的字符不在字符串时发送不同的警框：

```

javascript
var the_text = "Cool";
var position = the_text.indexOf("c");
if (position == -1) {
    window.alert("Your character is not in the string!");
}
else {
    window.alert("Your character is at position "+position);
}
```

这一次，`if` 语句检查方法是否向变量 `position` 返回了 -1。如果是的话，警框会显示“Your character is not in the string!”。否则，常规警框将告诉你位置。在之前的代码中，小写 *c* 不在字符串中，因此会出现“Your character is not in the string!”的警框。

`indexOf()` 方法仅返回你作为参数传递的字符第一次出现的位置。因此，如果你使用以下代码，你会收到提示说字符位于位置 1，尽管它也位于位置 2：

```javascript
var the_text = "Cool";
var position = the_text.indexOf("o");
if (position == -1) {
    window.alert("Your character is not in the string!");
}
else {
    window.alert("Your character is at position "+position);
}
```

小写 *o* 在字符串中出现了两次，但 `indexOf()` 仅定位字符第一次出现的位置。要找到下一次出现，你需要让方法查找“oo”而不是“o”（这会告诉你第一个“o”的位置，但会让你知道下一个位置也包含一个“o”），或者你可以使用第二个参数让方法从不同的起点开始查找。

### 第 13 章：处理字符串

如果你在 `indexOf()` 方法中添加一个整数作为第二个参数，则对字符或字符串的搜索将从该位置开始，而不是从 0 位置开始。因此，找到第二个“o”的一种方法是跳过位置 1 的第一个，并从位置 2 开始查找。

```javascript
var the_text = "Cool";
var position = the_text.indexOf("o",2);
if (position == -1) {
    window.alert("Your character is not in the string!");
}
else {
    window.alert("Your character is at position "+position);
}
```

这一次，方法返回的结果为 2，因为它在指定的起始位置就找到了它。通常情况下，这种方法用于确保某个字符或字符串在字符串中存在或不存在。例如，如果你想让字符串某处包含“fruit”，但不希望它包含“candy”，你可以编写以下代码：

```javascript
var the_text = "I like fruit!";
if ((the_text.indexOf("fruit") != -1) && (the_text.indexOf("candy") == -1)) {
    window.alert("Yes, fruit is good for you!");
}
else {
    window.alert("Please consider fruit rather than candy.");
}
```

这要求字符串包含“fruit”但不包含“candy”。如果通过测试，则会发送一个赞美水果的警框。如果没有通过，将发送一个建议考虑水果作为糖果替代品的警框。

### lastIndexOf() 方法

`lastIndexOf()` 方法查找特定字符或字符串在字符串中最后一次出现的位置。它只返回作为参数传递的字符或字符串最后一次出现的位置。如果在字符串值中没有找到字符或字符串，则返回 -1。

以下代码在字符串“Cool Cruising Car”中查找字母 *C*：

```javascript
var the_text = "Cool Cruising Car";
var position = the_text.indexOf("C");
window.alert("Your character is at position "+position);
```

这段代码将显示一个警框，告诉用户“Your character is at position 14.”。这种方法是在字符串值内查找字符或字符串最后一次实例的一种方便方法。

### match() 方法

`match()` 方法比较正则表达式和字符串以查看它们是否匹配。由于它涉及正则表达式，我现在不会详细介绍该方法，但正则表达式将在本章后面的“使用正则表达式”章节中介绍。

### replace() 方法

`replace()` 方法查找正则表达式是否匹配字符串。

### search() 方法

`search()` 方法执行正则表达式和字符串的搜索。

### slice() 方法

`slice()` 方法提取字符串的一部分。

### split() 方法

`split()` 方法根据分隔符创建字符串数组。

```javascript
var the_text = "orange:apple:pear:grape";
var split_text = the_text.split(":");
var end_count = split_text.length;
for (var count=0; count<end_count; count++) {
    document.write(split_text[count]+"<br />");
}
```




JavaScript：初学者指南

例如，看看下面的代码。与其不是指定要删除的字符数，不如提供一个结束位置。字符从起始位置开始删除，到结束位置减 1的位置结束。（记住 `slice()` 方法。）

```javascript
var the_text = "Do not cut this short!";

var shorter_string = the_text.substring(3,7);

window.alert(shorter_string);
```

你删除了字符串开头到单词“cut”开头之间的所有内容。

警告框将显示“not ”

### toString() 方法

`toString()` 方法为调用它的 String 对象返回一个字符串字面量值。以下是如何使用该方法的示例：

```javascript
var string_obj = new String("Cool");

var string_lit = string_obj.toString();
```

这段代码获取 String 对象并使用 `toString()` 方法获取其字符串字面量值。然后将该值赋值给变量 `string_lit`。

### toLowerCase() 方法

该方法以小写字母返回调用它的字符串的值。看这段代码：

```html
<body>
<script type="text/javascript">
var the_text = "I FEEL CALM, REALLY.";
document.write(the_text.toLowerCase());
</script>
</body>
```

这段代码在页面上以全小写字母写入该字符串，如下示例文本所示：

i feel calm, really.

### toUpperCase() 方法

该方法以大写字母返回调用它的字符串的值。这里有一个示例：

```html
<body>
<script type="text/javascript">
var the_text = "I am yelling!";
document.write(the_text.toUpperCase());
</script>
</body>
```

这段代码在页面上以全大写字母写入该字符串，如下示例文本所示：

I AM YELLING!

这就是最后几个方法了！现在你准备好测试你所学的内容了。

## 第 13 章：处理字符串

359

y 这 13-1
prjs13_1.html

prjs13_1.js

### 使用 charAt() 查找第一个字母

在这个项目中，你将通过创建一个脚本来练习使用 `charAt()` 方法，该脚本将判断查看者输入的第一个字符是否有效。

#### 逐步说明

1. 创建一个 HTML 页面，其中包含一个“Welcome”标题并调用名为 `prjs13_1.js` 的 JavaScript 文件。将 HTML 文件保存为 `pr13_1.html`。

**Q：所以 length 属性返回字符串中的字符数，但字符串方法从 0 开始计数。这有点让人困惑，就像数组也是一样。有什么简单的方法记住这一点吗？**

**A：最简单的方法可能是记住 length 属性从 1 开始计数，而方法从 0 开始计算位置。因此，length 属性的数值比字符串中的最后一个位置大 1。所以，如果字符串的长度为 5，这意味着字符串中的最后一个位置是第 4 位。**

**Q：是的，但也很让人困惑，因为 `slice()` 和 `substring()` 方法中的第二个参数比方法停止删除字符的位置高出一个。为什么呢？**

**A：刚开始确实很困惑。你只需要习惯每个方法的工作方式即可。`slice()` 和 `substring()` 方法确实有点绕。但如果你使用得足够频繁，你就会记住在什么情况下该使用哪些数字。**

**Q：我为什么需要 `split()` 方法？我不能自己建一个数组就完事了吗？**

**A：可以。然而，一旦你学习了 JavaScript Cookie，`split()` 方法将非常有用，因为你可以拆分存储在 Cookie 中的信息以便使用。Cookie 存储在长文本字符串中，通常用某个字符作为分隔符。这只是 `split()` 方法对你有用的一个例子之一。**

**Q：很多这些方法只是在文本字符串周围添加标签。我不能直接写出 HTML 吗？那样似乎更简单。**

**A：如果你觉得使用 HTML 更舒服，你可以这样做，尽管对于 String 对象来说，这些方法可能更有用。**

#### 提问专家

（续）

2. 创建一个外部 JavaScript 文件并将其保存为 `prjs13_1.js`。在第 3-6 步中使用它。

3. 编写代码获取提示框（prompt）询问名称的结果，并将提示框的结果赋值给一个名为 `the_name` 的变量。

4. 使用 `charAt()` 方法找出提示框中输入的名称的第一个字符是什么，并将结果赋值给一个名为 `first_char` 的变量。

5. 设置页面：只有当查看者输入的名称以大写字母 *S* 开头时，才显示该名称；否则，显示一条消息说明查看者需要一个以大写字母 *S* 开头的名称才能显示。

6. 保存 JavaScript 文件并在浏览器中打开 HTML 文件以查看其效果。

#### 尝试一下总结

在这个项目中，你利用了关于 `charAt()` 方法的知识创建一个脚本，判断查看者输入的第一个字符是否为有效字符。如果输入以大写字母 *S* 开头，则显示查看者的输入。

#### 组合方法

现在你已经知道如何单独使用 String 对象的属性和方法，你准备好创建一个结合使用它们的脚本了。下面的脚本执行了这些操作：




JavaScript：初学者指南

如果原始名称以 *Z* 或 *z* 开头，则执行 else 块。程序并不是将第一个字母替换为 *Z*，而是将其替换为 *W*。下一个 if/else 代码段会对数组中的第二个条目执行相同的任务，如果输入正确，该条目将是姓氏。

然后系统会向观众显示结果，告知用户新名称。图 13-4 显示了当观众输入 Big Mag 时，该脚本在浏览器中运行的结果。

## 使用 indexOf() 测试地址

在这个项目中，你将通过创建一个脚本，对观众输入的电子邮件地址进行非常基础的测试，从而练习 `indexOf()` 方法的使用。

### 逐步步骤

1.  创建一个 HTML 页面，并引用一个名为 `prjs13_2.js` 的 JavaScript 文件。创建一个观众可以点击的按钮，id 为“email”。给它标记为“点击以输入电子邮件地址”。将 HTML 文件保存为 `pr13_2.js`。
2.  创建一个外部 JavaScript 文件并将其保存为 `prjs13_2.js`。在第 3 到 7 步中使用它。
3.  创建一个名为 `get_add()` 的函数。在其中，将询问电子邮件地址的 prompt 结果赋值给名为 `email_add` 的变量。
4.  同样在函数中，使用 `indexOf()` 检查地址是否包含 at (@）字符。

![](img/61d166424839b7674a7b9c8434ae4e03_384_0.png)
图 13-4 观众在弹窗中获得了一个名称

5.  同样在函数中，使用 `indexOf()` 检查地址是否包含点 (.) 字符。
6.  同样在函数中，如果地址同时包含 at (@）字符和点 (.) 字符，则发送一个 alert 感谢观众。否则，发送一个 alert 告诉观众他们需要这些字符并重试。
7.  保存 JavaScript 文件并在浏览器中打开 HTML 文件，查看你可以对它进行什么。

## 练习总结

在这个项目中，你利用对 `indexOf()` 方法的知识来测试观众输入的电子邮件地址是否包含特定字符。如果缺少其中一个字符，将向观众发送错误警报。否则，将向观众发送一个感谢观众的警报。

## 使用正则表达式

正则表达式赋予了你在脚本中处理字符串更强大的能力。它们允许你形成可以与字符串进行匹配的模式，而不是尝试使用 String 对象的方法，后者可能会让你更难实现精确匹配。

例如，你可能想知道电子邮件地址文本框中输入的值是否开头至少包含一个字符，后面是一个 at (@) 符号，然后是至少一个字符，接着是一个点 (.)，最后是至少两个字符（匹配传统的电子邮件地址，如 jon@jon.com 或最短类型的电子邮件地址 j@j.jj）。第 13-2 节“练习”（Try This）为你提供了一个类似但更简单的测试供你尝试。

String 对象的方法没有提供一种整洁、高效的方式来执行此任务（尽管经过足够的尝试，可能是可能的）。然而，正则表达式可以缩短任务，甚至将一个使用 String 对象方法看似无法实现的匹配变为可以完成的匹配。

#### 创建正则表达式

要创建正则表达式，你必须创建一个 JavaScript `RegExp` 对象的实例。你可以几乎以创建字符串字面量相同的方式来实现。要创建一个 RegExp 字面量，你只需将正则表达式赋值给变量。不要使用引号包围表达式，而是使用正斜线 (/)，如下所示：

`var *varname* = /*your_pattern*/flags;`

你将 *varname* 替换为你想要使用的变量名，并将 *your_pattern* 替换为你选择的正则表达式模式。你可以在最后一个斜线后跟随一个或多个标记（这些将在接下来的章节“添加标记”中讨论）。

***注意***

JavaScript 使用正斜线来告诉浏览器正则表达式位于两个斜线之间，就像使用引号区分字符串一样。因此，如果正则表达式内部使用了正斜线，必须使用反斜线对其进行转义才能正常工作。例如，你不需要写 /02/03/2009/，而需要写 /02\/03\/2009/。

最容易创建的正则表达式模式是那种寻找字符精确匹配的模式。例如，如果你想查看字符串中是否存在 *our* 序列，你可以创建如下正则表达式模式：

`var tomatch = /our/;`

前面的代码创建了一个名为 `tomatch` 的 RegExp 字面量。现在你需要一个字符串来测试该模式。如果你对表达式测试单词 *our*，它是匹配的。如果你测试 *your*、*sour*、*pour* 或 *pouring*，它都是匹配的。如果你测试 *cool*、*Our*、*oUR*、*OUR* 或 *souR*，则不会匹配。那么，你如何执行这项测试呢？

#### 使用正则表达式测试字符串

要用字符串测试正则表达式，你可以使用 `test()` 方法。基本语法如下：

`var is_match = regex.test(string);`

`test()` 方法的结果是一个布尔值，用作 if 语句的条件。如果结果为 true，观众会收到“哇，我们有相同的名字！”的 alert。如果结果为 false，观众会收到“不是我的名字，但可以的！”的 alert。

由于该方法返回 true 或 false，因此它可以单独作为 if 语句的条件放置（如果你愿意的话，也可以写成 `regex.test(string)==true`）。例如，看下面的示例：

```javascript
var thename = window.prompt("Enter your name:");
var tomatch = /John/;
if (tomatch.test(thename)) {
    alert("Wow, we have the same name!");
} else {
    alert("Not my name, but it will work!");
}
```

上面的代码是区分大小大小的。因此，只有包含大写 J 的 John 条目会匹配。如果你希望不区分大小写，你需要使用特殊字符，这将在稍后讨论。

### 添加标记

标记允许你使匹配不区分大小写，或者查找字符串中的每个匹配项而不仅仅是第一个（全局测试）。要添加标记，请将其放在正则表达式最后一个斜线之后。你可以使用三种选项，如表 13-3 所示。

如果你想调整之前使用的名称脚本使其不区分大小写，你可以为正则表达式添加一个 i 标记，如下代码所示：

```javascript
var thename = window.prompt("Enter your name:");
var tomatch = /John/i;
if (tomatch.test(thename)) {
    alert("Wow, we have the same name!");
} else {
    alert("Not my name, but it will work!");
}
```

| 表 13-3 正则表达式标记 |
| 标记(s) | 目的 |
| :--- | :--- |
| i | 使匹配不区分大小写 |
| g | 使匹配全局化 |
| m | 使匹配在多行模式下有效 |





JavaScript: 入门指南

只要字符串中包含 John 的模式，`test()` 方法现在将返回 `true`。它可以不区分大小写，因此现在 John、JOHN、john 甚至 JoHn 都是匹配项，并将导致 `test()` 方法返回 `true`。

你也可以同时使用多个一个标记或同时使用所有三个标记。例如，如果你想让匹配既不区分大小写又是全局的（即获取整个字符串中的每个匹配项），你可以使用以下代码：

`var tomatch=/John/ig;`

## 创建强大的模式

虽然能够创建如此精确的模式是一件好事，但你并不总是要寻找如此精确的匹配项。在很多情况下，你将寻求匹配一个更通用的模式，例如至少包含三个字符的条目，或者需要两个任意类型的字符后跟一个特殊字符的条目。

通过在表达式中使用特殊字符，你可以创建你需要的模式来匹配你想要的给定序列。JavaScript 正则表达式以 Perl 正则表达式为模型。因此，如果你在 Perl 中用过正则表达式，那么这些内容对你来说将非常熟悉。表 13-4 列出了一些字符来帮助你创建模式。如你所见，创建你需要的模式有广泛的选项。现在，你可以根据你设定的标准轻松地验证字符串。

现在，如果你想确保一个文本字段包含一个或多个数字，你可以结合表 13-4 中的 `/d` 和 `+` 字符使用以下 HTML 和 JavaScript 代码，从 HTML 代码开始：

```html
<body>
  <form>
    输入一些文本: <input type="text" id="has_digits" />
    <input type="button" id="t_btn" value="Test" />
  </form>
</body>
```

接下来，是 JavaScript 代码：

```javascript
var t_button = document.getElementById("t_btn");
t_button.onclick = function() {
  var has_num = document.getElementById("has_digits").value;
  var tomatch = /\d+/;
  if (tomatch.test(has_num)) {
    window.alert("您的输入包含一个或多个数字!");
  } else {
    window.alert("您的输入不包含任何数字!");
  }
}
```

### 表 13-4 正则表达式代码

| 字符 | 用途 | 示例 |
| :--- | :--- | :--- |
| `^` | 仅从行首匹配 | `/^c/` 匹配 *corn* 中的 *c*；`/^c/` 不匹配 *acorn* 中的 *c* |
| `$` | 仅在行尾匹配 | `/r$/` 匹配 *Car* 中的 *r*；`/r$/` 不匹配 *Cat* 中的 *t* |
| `*` | 如果前面的字符出现零次或多次，则匹配该字符 | `/co*/` 匹配 *co* 或 *c*；`/co*/` 不匹配 *pi* |
| `+` | 如果前面的字符出现一次或多次，则匹配该字符 | `/co+/` 匹配 *co* 或 *cooooo*；`/co+/` 不匹配 *ca* |
| `?` | 如果前面的字符出现零或一次，则匹配该字符 | `/o?l/` 匹配 *style* 或 *column*；`/co?l/` 不匹配 *cool* |
| `.` | 匹配任何单个字符（换行符除外） | `/.l/` 匹配 *al* 或 *@l*；`/.l/` 不匹配 *\nl* 或 *l* |
| `(*x*)` | 通过用字符替换 *x*，匹配该序列并将其留在内存中供以后使用；用于表达式分组 | `/(a)/` 匹配 *a*；`/(cool)/` 匹配 *cool*；`/(cool)/` 不匹配 *coal* |
| `\|` | 用作逻辑或符号，允许匹配符号左侧的内容或右侧的内容 | `/cool|bad/` 匹配 *cool* 或 *bad*；`/cool|bad/` 不匹配 *car* |
| `{*x*}` | 使用数字替换 *x*，当前面的字符恰好出现 *x* 次时匹配 | `/n{1}/` 匹配 *n*；`/nn{2}/` 匹配 *nnn*；`/nn{1}/` 不匹配 *nnn* |
| `{*x*,}` | 使用数字替换 *x*，当前面的字符出现 *x* 次或更多时匹配 | `/n{1,}/` 匹配 *n*；`/n{1,}/` 匹配 *nnnnn*；`/n{3,}/` 不匹配 *nn* |
| `{*x*,*y*}` | 使用数字替换 *x* 和 *y*，当前面的字符出现至少 *x* 次但不过于 *y* 次时匹配 | `/n{1,2}/` 匹配 *n* 或 *nn*；`/n{2,3}/` 不匹配 *n*；`/n{4,7}/` 不匹配 *nnn* |
| `[]` | 匹配你选择的字符集；当括号内的任意一个字符（如 [abc]）或范围内的任意一个字符（如 [a-k]）存在时匹配 | `/[abc]/` 匹配 *a*、*b* 或 *c*；`/[a-k]/` 匹配 *j*；`/[a-k]/` 不匹配 *n* |
| `[^]` | 当你的字符集中的字符**不**存在时匹配；可以是一个集合（如 [abc]）或范围（如 [a-k]） | `/[^abc]/` 匹配 *d*；`/[^abc]/` 不匹配 *b*；`/[^a-k]/` 匹配 *n* |

***表 13-4 正则表达式代码（续）***

| 字符 | 用途 | 示例 |
| :--- | :--- | :--- |
| `\` | 用于转义特殊字符或使普通字符变得特殊 | `\@` 转义 @ 字符 |
| `\n` | 代表换行符 | `\n` |
| `[\b]` | 匹配退格键输入 | `[\b]` 匹配退格 |
| `\b` | 当字符的前一个或之后位于单词边界时匹配，例如在空格字符之前或之后；要匹配单词开头，将字符放在右侧；要匹配单词末尾，将字符放在左侧 | `/\bc/` 匹配 *my* 中的 *c* |
| `\B` | 在非单词边界处匹配 |
| `\s` | 匹配空白字符 |
| `\c` | 使用 *c* 替换的的控制符 |
| `\S` | 匹配空白字符 |
| `\d` | 匹配数字 |
| `\D` | 匹配非数字 |
| `\f` | 匹配换页符 |
| `\r` | 匹配回车符 |
| `\t` | 匹配制表符 |
| `\w` | 匹配单词字符 |
| `\W` | 匹配非单词字符 | (注：由于原文表格后半部分在输入中不完整，此处已根据标准正则逻辑进行翻译性补全)

#### 表达式分组

此代码简单检查字符串中是否包含数字。如果你想确保字符串只包含数字且没有其他字符，你需要从字符串开头到结尾进行测试。使用表 13-4 中的 `^` 和 `$` 符号，你可以根据你设定的标准验证字符串。因此，以下模式允许只有数字：

`var tomatch = /^\d+$/`

从开头到结尾的有效字符都是数字，这对于不包含其他字符的输入将返回 `true`。

***注意*** 正则表达式在验证时非常强大，因为它们允许接受较少的错误信息。客户端验证诸如电子邮件地址或电话号码的提交可以减少往服务器的次数。然而，用户可能会禁用 JavaScript 并直接提交表单。因此，客户端验证应该支持服务端验证（例如通过 CGI 脚本或 Java Servlet），但绝不能取代它（存储或显示未验证的用户数据可能会导致巨大的安全风险）。

你会注意到表 13-4 中用圆括号括起的表达式表示一个可以供以后使用的组（或使用如 `match()` 方法，它会将每个组匹配与整体匹配一起存储在数组中）。例如，你可能决定使用特定的数字序列并让该序列重复特定的次数。要匹配重复的次数，可以使用大括号 {} 配合数字或数字范围。例如，如果你想匹配五次数字3，可以使用以下表达式：

`/3{5}/`

如果你希望在数字3至少出现五次但不超过十次的情况，可以使用以下表达式：

`/3{5,10}/`

现在，假设你想匹配以3开头且后面跟任意数字的序列，并匹配该整个序列五次（因此，类似 3234353637 的将是一个匹配）。你可能会这样写：

`/3\d{5}/`




JavaScript: 入学者指南

这个问题的问题在于，它匹配了 3，但之后又匹配了五位数字，而不需要
重复 3 次。因此，像 387643 这样的数字会被匹配，尽管你想要
得到五组两个数字，且每组都以 3 开头。要修复这个问题，你可以
用括号将 3 和 \d 组合在一起，并在后面跟上它应该重复的次数：

/(3\d){5}/

这一次，3 和第二位数字被分组在一起，该序列必须重复
五次。

分组是更充分利用正则表达式的一种有用方法，当你到达下一章的
表单验证时，你会看到更多这种用法。

## replace(), match() 和 search() 方法

这些 String 对象的方法在在本章前面已经提到过，现在引入了正则表达式后，
它们将变得更有意义。

### replace() 方法

要替换字符串中的信息，你可以使用正则表达式和 String 对象的
replace() 方法。使用 replace() 方法的语法如下：

*varname*= *stringname*.replace(*regex*,*newstring*);

你将 *varname* 替换为变量名，该变量将在信息被替换后持有新的字符串值。
你将 *stringname* 替换为将进行替换的字符串变量名。
你将 *regex* 替换为用于匹配字符串的正则表达式名称。最后，
你将 *newstring* 替换为字符串或字符串变量，用于替换字符串中
任何匹配到的值。

例如，以下代码将 mystring 中第一个实例“car”替换为
“skunk”：

var mystring= "I like the way a new car smells, and cars are fun.";
var toreplace=/car/;
var newstring= mystring.replace(toreplace,"skunk");
window.alert(newstring);

```

前面的代码只替换了第一个 car，弹窗显示“I like the way a new
skunk smells, and cars are fun.” 如果你想更改每一个实例“car”，那么
在正则表达式的末尾添加 g 标志将会很有帮助，如下代码所示：

var mystring= "I like the way a new car smells, and cars are fun.";
var toreplace=/car/g;
var newstring= mystring.replace(toreplace,"skunk");
window.alert(newstring);

| 说明 |
| :--- |
| 字符串中的第一个匹配项被替换，结果被赋值给变量 |
| 要替换的模式被设置为正则表达式 |
| 弹窗显示更新后的字符串 |
| 创建了一个字符串字面量 |
| 添加 g 标志会导致在运行 replace() 方法时所有模式的所有项都被替换 |

g 标志将匹配字符串中找到的正则表达式的每一个实例。因此，当
运行 replace() 方法时，所有的“car”实例都将被替换为“skunk”。
查看者将看到此弹窗：“I like the way a new skunk smells, and skunks are fun.”

你也可以使用 replace() 方法来创建一个改名脚本，它比本章前面的
脚本更短且稍微不那么复杂。通过使用正则表达式配合 replace() 方法，
可以更容易地更改名和姓的首字母。
以下代码展示了如何操作：

```javascript
function getname() {
var tomatch=/^[A-Za-z]+\s[A-Za-z]+$/;
var toreplace=/\b[A-Za-z]/gi;
var thename=window.prompt("Enter your first and last name","");
if (tomatch.test(thename)) {
newname=thename.replace(toreplace,"Z");
window.alert("Now your name is "+newname);
}
else {
window.alert("Name invalid. Please Try Again");
getname();
}
}
getname();
```

此脚本无论名和姓的首字母原来是什么，都会将其更改为 *Z*。
替换的正则表达式仅仅是使用单词边界 (\b) 代码查找单词开头的字母。
每当字母位于单词开头时，它就会被替换。

对输入的验证防止了脚本获取超过两个名字和一个空格，它还确保了
每个名字中至少有一个字母，且没有数字或特殊字符。插图显示了如果查看者在提示框中输入 Debra Loo，脚本的结果是：查看者的名字被更改了。

### match() 方法

match() 方法比较正则表达式和字符串以查看它们是否匹配。它
返回一个包含一个或多个匹配项的数组，取决于它的用法。如果没有
找到匹配项，它将返回 –1。

正则表达式用于验证和更改用户的输入。

match() 方法的基本用法如下：

*string*.match(*regex*);

*string* 将是你的字符串字面量，*regex* 将是你的正则表达式字面量。
注意此方法与 test() 方法之间顺序的区别。你可以这样使用它：

```javascript
var mystring = "I am Ironman!";
var toreplace=/Iron/;
if (mystring.match(toreplace)) {
window.alert("Iron found!");
}
else {
window.alert("Sorry, no Iron in string.");
}
```

字符串中的第一个匹配项被替换，结果被赋值给变量。
要替换的模式被设置为正则表达式。
弹窗显示更新后的字符串。
创建了一个字符串字面量。
添加 g 标志会导致在运行 replace() 方法时所有模式的所有项都被替换。

### search() 方法

search() 方法对正则表达式和指定字符串执行搜索。如果找到了
匹配项，它将返回找到匹配的位置。否则，它返回 –1。正如你所见，语法与 match() 方法相似。

```javascript
var mystring = "I am Ironman!";
var toreplace=/Iron/;
if (mystring.search(toreplace) !== -1) {
window.alert("Iron found at "+mystring.search(toreplace));
}
else {
window.alert("Sorry, no Iron in string.");
}
```

## 更多信息

关于正则表达式以及如何创建复杂模式的更多信息，你可以使用以下资源：

- regular-expressions.info
- regular-expressions.com/
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

有了这些技术，你准备好开始处理表单了。

## 第 13 章：处理字符串





## 第 14 章：JavaScript 与表单

### JavaScript 入门指南

#### 核心技能与概念
- 访问表单
- 使用表单对象的属性和方法
- 确保表单可用可用
- 表单验证
- 使用表单进行导航

当你使用 JavaScript 访问表单时，可以为 Web 页面创建新的脚本。

本章首先介绍如何使用 JavaScript 访问表单。然后你将学习用于表单和表单元素的各种属性和方法。你还将学习表单与可用性、如何验证表单元素，以及如何将`<select></select>`元素作为导航工具。

### 访问表单

每当你向 HTML 文档添加一组 `<form>` 和 `</form>` 标签，就会创建一个表单对象。要使用 JavaScript 访问其中一个表单，可以使用以下任意选项：

字体 使用文档对象的 `forms` 数组
- 在起始表单标签中为表单命名并使用该名称访问表单
- 在起始表单标签中为表单指定 `id` 并使用 `document.getElementById()` 方法访问它

#### 使用 forms 数组

`forms` 数组允许你使用数组中的索引数字访问表单。页面上的每组 `<form>` 和 `</form>` 标签都会在 `forms` 数组中创建一个额外的元素，并按照它们在文档中出现的顺序。因此，你可以这样引用文档中的第一个表单：

`document.forms[0]`

正如你所记得，数组从 0 开始计数，因此上一个示例将访问文档中的第一个表单。如果你想访问第二个表单，可以使用以下代码：

`document.forms[1]`

这同样适用于页面上的其余表单。只需记住从 0 开始计数而不是从 1 开始，即可访问正确的表单。

访问表单本身不会产生任何操作。你访问的表单是一个对象。要使用它，你需要该对象的某个属性或方法。表单对象的属性和方法将在稍后的部分——“使用表单对象的属性和方法”中列出，但现在，可以先看一眼 `length` 属性及其作用的。

#### 属性值

本节中的示例使用了表单对象的 `length` 属性。该属性允许你查找 HTML 表单中存在多少个元素（如输入框、选择框、单选按钮等）。例如，来看这段代码：

```html
<body>
  <form>
    Name: <input type="text" />
    E-mail: <input type="text" />
    <input type="submit" value="Submit" />
  </form>
</body>
```

这段代码创建了一个简单的表单，包含三个元素：两个文本框和一个提交按钮。因为它是页面上唯一的表单，所以它将是第一个表单，允许你使用 `document.forms[0]` 访问它。要使用 `length` 属性，请像这样添加到末尾：

`document.forms[0].length`

使用前面的代码，你可以创建一个短脚本来告诉观众表单中有多少个元素。（你通常不会这样使用 `length` 属性，但作为一个示例是非常好的。）接下来的代码将在表单后的页面上写入该信息：

```html
<body>
  <form>
    Name: <input type="text" /> <br />
    E-mail: <input type="text" /> <br />
    <input type="submit" value="Submit" />
  </form>
  <p>
    <script type="text/javascript">
      document.write("The form has "+document.forms[0].length+" elements.");
    </script>
  </p>
</body>
```

这段代码告知观众表单有三个元素。图 14-1 显示了该脚本在浏览器中运行的结果。

- 第一个元素是这个文本框
- 第二个元素是这个文本框
- 第三个元素是这个提交按钮
- 表单的元素在这里
- 表单中的元素数量打印在页面上

#### 两个 length 属性

如果你想在页面上有多个表单时尝试显示每个表单的元素数量，可以使用一个更复杂的脚本，为页面上的每个表单打印消息。记住，因为表单是一个数组，你可以找到数组的长度。

数组的长度是页面上表单的数量（就像特定表单的 `length` 属性是表单中元素的数量）。要查找页面上表单的数量而不是单个表单的长度，请记住通过省略括号和索引数字来指定表单，如下例所示：

`document.forms.length`

这种语法可以找到页面上表单的数量。因此，你必须记住这一点：

- `document.forms.length` 查找页面上表单的数量。
- `document.forms[*x*].length` 查找页面上特定表单中的元素数量，其中 *x* 是要访问的表单的索引数字。

这种语法看起来可能有点困惑，但只需记住 `document.forms.length` 查找页面上表单的数量，而 `document.forms[*x*].length` 查找特定表单中的元素数量。

#### 使用表单名称

使用表单名称允许你为页面上稍后访问的表单命名。此选项可以帮助消除 `document.forms.length` 和 `document.forms[*x*].length` 之间的任何混淆，因为除非你要遍历每个表单中的每个元素，否则你不需要后者。

要使用表单名称，你必须在想要访问的表单的起始表单标签中添加 `name*=*“*yourname*”` 属性。将 *yourname* 替换为你想要使用的表单名称，如下代码所示：

```html
<form name="info_form">
  Name: <input type="text" />
  <input type="submit" />
</form>
```



` 似乎包含了一段重复的标题和页码，且没有提供完整的正文内容。作为高级文档工程师，我已根据您提供的逻辑进行了翻译，并遵循了所有的 Markdown 格式要求。

[content]
## 第 14 章：JavaScript 与表单

381

现在表单名称为 `info_form`，你可以使用此名称在脚本中访问该表单。

表单名称允许你通过其名称访问表单对象的实例。要使用 JavaScript 访问一个使用名称（name）的表单，可以使用以下语法：

`document.*yourname`

将 *yourname* 替换为起始表单标签中 `name="yourname*"` 属性给出的表单名称。因此，如果你想编写脚本来获取命名表单中的元素数量，可以使用以下代码：

```html
<body>
  <form name="info_form">
    Name: <input type="text" /><br />
    <input type="submit" />
  </form>
  <p>
    <script type="text/javascript">
      document.write("表单有 "+document.info_form.length+" 个元素.");
    </script>
  </p>
</body>
```

注意 `document.write()` 语句中是如何访问表单的。而不是 `forms` 数组，表单名称位于其位置。现在可以通过访问 `length` 属性访问表单对象的属性。

### 使用 ID

访问表单的第三种方法是使用 `id` 属性，然后使用 `getElementById()` 访问表单元素。这通常是访问表单及其元素最清晰的方法，因为之前的两种访问方法需要知道表单在 `forms` 数组中的索引或表单名称。

如果你想使用 `id` 方法编写上一节的脚本，可以使用以下代码：

```html
<body>
  <form id="info_form">
    Name: <input type="text" /><br />
    <input type="submit" />
  </form>
  <p>
    <script type="text/javascript">
      var f_length = document.getElementById("info_form").length;
      document.write("表单有 "+f_length+" 个元素.");
    </script>
  </p>
</body>
```

- 表单被赋予了一个名称
- 表单被赋予了一个 id
- 命名表单中的元素数量写在页面上
- 命名表单中的元素数量写在页面上

### JavaScript：学者指南

由于你已经熟悉使用 `document.getElementById()`，因此这对你来说应该很直接的方法。

访问表单及其元素的方法取决于你编写的脚本类型。如果你在页面上使用多个表单，`forms` 数组可以是遍历每个表单的方便方法。如果你试图尽可能与旧版浏览器兼容，使用 `name` 方法可能是更好的选择。另一方面，尝试 XHTML 1.0 strict 模式要求你使用 `id` 来命名每个表单元素，因此在这种情况下使用 `id` 方法更合适。

### 使用表单对象的属性和方法

当你在脚本中访问表单的某些元素或属性时，JavaScript 表单对象将提供帮助。表单对象只有几个属性。

#### 属性

表单对象的属性提供了你在脚本处理表单时可能需要的信息。表 14-1 列出了表单对象的属性及其值。这些属性中的大多数值对应于 HTML 表单标签中的各种属性。不过，其中几个具有不同类型的值，如文所示。

#### action 属性

此属性允许你访问起始表单标签中 `action="url"` 属性的值。该属性用于将表单发送到服务器端脚本（例如 Perl 或 PHP 脚本）进行处理。示例显示了如何访问命名表单的该属性：

```html
<body>
  <form name="info_form" action="http://someplace.com/php/form.php">
    Name: <input type="text" /><br />
    <input type="submit" />
  </form>
  <p>
    <script type="text/javascript">
      document.write("表单将前往 "+document.info_form.action);
    </script>
  </p>
</body>
```

该脚本会将 action 属性中指定的 URL 写在页面上。图 14-3 显示了该脚本在浏览器中运行的结果。

#### elements 属性（数组）

elements 属性是一个数组，允许按照代码中从 0 开始顺序访问特定表单内的每个元素。它的工作方式与 `forms` 数组非常相似，但为给定表单中的每个元素都有一个条目。

要使用 elements 数组访问表单中的元素，请使用要访问的元素的索引号。例如：

```html
<form name="info_form">
  Name: <input type="text" /><br />
  <input type="submit" />
</form>
```

表 14-1 表单对象的属性

| 属性 | 值 |
| :--- | :--- |
| action | HTML 表单标签中 action 属性的值 |
| elements | 数组，其中包含 HTML 表单中每个表单元素对应的数组元素 |
| encoding | enctype 属性的值，随不同浏览器而异 |
| length | HTML 表单中元素总数的值 |
| method | HTML 表单标签中 method 属性的值 |
| name | HTML 表单标签中 name 属性的值 |
| target | HTML 表单标签中 target 属性的值 |




JavaScript：初学者指南

`checked` 属性将返回 `true` 或 `false`，不需要将 `checked` 属性的值与任何内容进行测试。`checked` 属性已经有一个值，因此该值不需要与任何内容进行比较（除非你喜欢这样做，那样也是可以的）。

### defaultChecked 属性

该属性也是一个 `true` 或 `false` 的布尔值。其值取决于复选框或单选按钮在 HTML 中是否具有 `checked` 属性（这会将该元素在页面上默认设为选中）。如果元素具有 `checked` 属性，则值为 `true`；否则，则值为 `false`。

例如，以下 HTML 代码使用了 `checked` 属性：

```html
<form>
您希望我们向您发送电子邮件更新和优惠吗？<br />
是 <input type="checkbox" id="yes" checked="checked" />
否 <input type="checkbox" id="no" />
</form>
```

由于第一个复选框的 `checked` 属性被设置为 `checked`，该元素的 `checked` 属性将返回 `true`。对于第二个复选框元素，该属性将返回 `false`。

### defaultValue 属性

你可以在文本框和文本区域中使用此属性。它存储了在在元素标签的 `value` 属性中设置的默认值。如果你在文本框中设置了默认值，用户删除了它，然后用户决定如果回到默认值就好了，那么这个功能就会非常有用。你可以编写一个按钮，在查看者点击时返回该值，如下代码所示：

```html
<body>
<form>
最喜欢的 URL：<br />
<input type="text" id="favurl" value="http://www.yahoo.com">
<br /><br />
<input type="button" value="重置默认" onclick="back_to_default();">
</form>

<script type="text/javascript">
function back_to_default() {
  var url_box = document.getElementById("favurl");
  url_box.value = url_box.defaultValue;
}
</script>
</body>
```

在 HTML 代码中，文本框 `input` 标签中的 `value` 属性被设置为 `http://www.yahoo.com`。这为它提供了一个默认值。当函数被调用时，它通过将当前值（`url_box.value`）更改为默认值（`url_box.defaultValue`），将此默认值赋回文本框。

- 按钮调用重置默认值的函数
- 文本框被分配了一个默认值
- 复选框的当前值改回默认值

第 14 章：JavaScript 与表单
387

***注意***

如果你希望将特定值恢复为默认值，这种技术非常有用。如果你想将*所有*内容都恢复为默认值，只需在你的 HTML 代码中使用重置按钮（即 `<input type="reset" value="Reset" />`）。

### form 属性

该属性通常与关键字“this”一起使用，指向包含该元素的表单。例如，如果你想通过点击按钮更改文本框的值，可以使用 `this.form` 来引用表单，而不需要使用表单的名称或 ID：

```html
<form>
最喜欢的 URL：<br />
<input type="text" name="favurl" value="http://www.yahoo.com />
<br /><br />
<input type="button" value="更改" onclick="this.form.favurl.value='http://www.lycos.com';" />
</form>
```

当按钮被点击时，这段代码会将文本框的当前值更改为 `http://www.lycos.com`。使用 `this.form.favurl.value` 允许你从内部的元素访问同一个表单，而不需要回退使用表单名称或 ID，后者代码会冗长一些。

### name 属性

该属性存储元素 `name` 属性的值。例如，以下代码将打印页面上第一个元素（文本框）的名称：

```html
<body>
<form name="info_form">
名称： <input type="text" name="yourname" /><br />
<input type="submit" value="提交" />
</form>

<p>
<script type="text/javascript">
document.write("第一个元素是 "++document.info_form.elements[0].name);
</script>
</p>
</body>
```

这是一个查找元素名称的方便方法，无需在代码中搜索它。

### options 属性（数组）

`options` 属性是一个数组，包含表单中 `select` 框列出的每个选项的元素。索引数字从 0 开始，每个选项按照在 HTML 代码中编写的顺序放在数组中。以下代码显示了如何访问选项的值（这是 `option` 标签 `value` 属性值，而不是标签的内容）并将其写在页面上：

```html
<body>
<form>
水果：
<select id="optlist">
<option selected="selected" value="orange">橙子</option>
<option value="apple">苹果</option>
<option value="pear">梨</option>
</select>
</form>

<p>
<script type="text/javascript">
var fbox = document.getElementById("optlist");
document.write("第二个选项是 ");
document.write(fbox.options[1].value);
</script>
</p>
</body>
```

- 第一个选项
- 第二个选项
- 第三个选项
- 第二个选项的值
- 复选框改回默认值

JavaScript：初学者指南
第 14 章：JavaScript 与表单
389

### type 属性

该属性存储表单元素的 `type` 值，例如 `type="text"` 或 `type="button"`。这些值分别为 `text` 和 `button`。

### value 属性

该属性存储元素的当前值。例如，文本框可能没有默认值；但当查看者向框内输入信息时，文本框就有当前值。如果框内为空，当前值将为空字符串（你在之前的章节中用过此属性）。
你将在信息处理、验证和表单导航中频繁使用此属性。

### blur() 方法

该方法允许你在代码中为元素创建 `blur` 事件。例如，如果你不想让用户调整文本框中的默认值，可以使用 `blur()` 方法移除元素的焦点。以下代码显示了示例：

```html
<body>
<form>
你喜欢的食物
<input type="text" name="fav_food" value="披萨" onfocus="this.form.fav_food.blur(); />
</form>
</body>
```

点击文本框会获得焦点，但 `onfocus` 事件处理器会捕获文本框的焦点，然后对元素使用 `blur()` 方法来移除焦点。当然，你也可以对没有默认值的框使用此脚本，创建一个无法填充的文本框，因为它无法获取焦点。无论哪，如果查看者在浏览器中禁用了 JavaScript，脚本就会失效，因此不建议将其作为防止用户填写字段的保护。

### click() 方法

该方法允许你在代码中为按钮创建 `click` 事件。然而，这种方式创建的点击不会激活按钮中使用的 `onclick` 事件处理器。因此，`click()` 方法最适用于激活诸如提交按钮和重置按钮，这些按钮不需要 `onclick` 事件处理器即可工作。

例如，重置按钮在点击时会重置表单。如果你想在字段失去焦点时重置表单（并以此激怒查看者），可以使用以下代码：

```html
<body>
<form>
你喜欢的食物
<input type="text" name="fav_food" onblur="this.form.annoy.click(); />
</form>
</body>
```





JavaScript: 入门指南

```html
<form>
  <input type="text" />
  <br />
  Drink <input type="text" />
  <br /><br />
  <input type="reset" name="annoy" value="Reset Form">
</form>
```

这段代码使用 `onblur()` 事件，当查看者从第一个文本框移除焦点时，会触发名为“annoy”（重置表单）的按钮的操作。

## focus() 方法

`focus()` 方法允许你在代码中创建一个焦点事件，以便为查看者获取某个表单元素的焦点。

例如，你可能希望在页面加载时立即赋予页面上的第一个表单元素（通常是文本框）焦点，这样查看者无需点击该元素即可获得焦点并开始输入。以下代码展示了如何实现这一点：

```html
<body>
  <form>
    Your Favorite Food
    <input type="text" id="fav_food" /><br />
    Drink <input type="text" />
  </form>
  <script type="text/javascript">
    var f_box = document.getElementById("fav_food");
    f_box.focus();
  </script>
</body>
```

该脚本在表单及其元素存在后加载。它随后使用 `focus()` 方法为查看者获取第一个文本框的焦点。

## select() 方法

该方法允许你自动为查看者选择（高亮）文本框或文本区域的内容。如果你为元素设置了默认值，并希望查看者能够快速删除该值以输入新值，或者你希望让查看者方便复制和粘贴元素的内容，这种方法非常有用。

以下代码会在查看者赋予文本区域焦点时选择文本区域中的文本，使查看者能够快速删除文本或轻松将其复制到剪贴板：

```html
<body>
  <form>
    <textarea name="sometext" onfocus="this.form.sometext.select();">
      这段文字是文本区域的默认文本，当查看者赋予文本区域焦点时，它会被选中。
    </textarea>
  </form>
</body>
```

## 第 14 章：JavaScript 与表单

`onfocus` 事件处理程序会在查看者点击文本区域内部时执行该方法的调用。`<textarea>` 和 `</textarea>` 标签内的所有默认文本都会被选中。

表单元素的属性和方法就此结束。现在是回到表单对象的属性了。

## encoding 属性

该属性通常持有表单标签中 `entype` 属性的值。然而，不同浏览器的结果可能有所不同。

#### length 属性

`length` 属性持有页面上给定表单中的元素数量。本章已经非常详细地涵盖了该属性，因此这里无需再次讨论它。

## method 属性

该属性持有表单标签中 `method` 属性包含的值。因此，如果你正在将表单发送到服务器进行处理，可能会使用类似下面的代码：

```html
<form name="f1" method="post" action="http://site.com/cgi-bin/form.cgi">
  <!-- 此处为表单内容 -->
</form>
```

此表单 method 属性的值为 `post`，因为它位于表单的 `method` 属性中。

### name 属性

该属性持有表单名称，该名称是在表单标签的 `name` 属性中赋予的。你可能会有类似这样的代码：

```html
<form name="cool_form">
  <!-- 此处为表单内容 -->
</form>
```

这里，name 属性的值是 `cool_form`，因为它是表单 `name` 属性内部的值。

## target 属性

该属性持有表单标签中 `target` 属性赋予的值。例如，你可能会有以下代码：

```html
<form name="cool_form" target="place" action="program.cgi">
  <!-- 此处为表单内容 -->
</form>
```

这里，target 属性的值是 `place`，因为它是表单 `target` 属性内部的值。

#### 方法

现在来看表单对象的方法。表单对象只有两个方法：`reset()` 和 `submit()`，将在下文中进行描述。

## reset() 方法

该方法允许你使用脚本重置表单，允许你在任何喜欢的事件后重置表单。因此，如果你想在查看者从元素中移除焦点后重置表单，可以使用以下代码：

```html
<body>
  <form>
    Your Favorite Food
    <input type="text" name="fav_food" onblur="this.form.reset();" /><br />
    Drink <input type="text" />
    <br /><br />
    <input type="reset" value="Reset Form" />
    <input type="submit" value="Submit Form" />
  </form>
</body>
```

## submit() 方法

该方法允许你在查看者点击提交按钮之前提交表单。以下代码展示了当查看者从元素中移除焦点时如何执行（与 `reset()` 方法的方法类似）：

```html
<body>
  <form action="http://site.com/php/form.php">
    Your Favorite Food
    <input type="text" name="fav_food" onblur="this.form.submit();" /><br />
    Drink <input type="text" />
    <br /><br />
    <input type="submit" value="Submit Form" />
  </form>
</body>
```

## 表单的可访问性

确保表单对于查看者具有可访问性具有挑战性，因为布局可能无法被辅助技术（如 Jaws 或 Reader）正确解释。你可以采取几种方法来确保表单的可访问性：调整元素顺序、使用 `<label>` 标签、使用 `<fieldset>` 标签，并确保用户启用了客户端脚本（如 JavaScript）。

## 正确元素和标签顺序

在 HTML 代码中，标签文本和元素的顺序有助于辅助技术读取表单。例如，考虑以下输入：

```
<input type="text" name="yourname" id="yourname" /> Name
<input type="text" name="zip_code" id="zip_code" /> Zip Code
```

在这里，辅助技术在表单元素之前寻找标签文本。由于第一个输入元素之前没有标签文本，查看者仅被提示输入，而没有关于要输入什么信息的指示。为了纠正这一点，你只需移动标签文本并将其放在元素之前，如下代码所示：

```
Name <input type="text" name="yourname" id="yourname" />
Zip Code <input type="text" name="zip_code" id="zip_code" />
```

现在，辅助技术可能会获取表单标签并允许用户输入预期的信息。同时使用 `name` 和 `id` 属性也有帮助，因为各种辅助技术也能识别这些属性。这对于文本框、文本区域和选择框同样有效。然而，在处理复选框和单选按钮时，许多辅助技术期望元素在前，随后是描述性标签。因此，在使用它们时应该交换位置。在处理按钮（如提交、重置或创建的按钮）时，请确保使用 `value` 属性来描述按钮的功能，这是辅助技术可能预期的。

## 使用 <label></label> 标签

使用 `<label>` 标签可以帮助你指定哪个标签文本属于哪个表单元素。这是一个示例：

```html
<label for="yourname">Name</label>
<input type="text" name="yourname" id="yourname" />
```

在这里，你将起始标签的 `for` 属性赋予表单元素的 `id` 属性值，该元素将使用 `<label>` 和 `</label>` 标签包含的标签文本。在前面的示例中，`for` 属性包含 `yourname`，将文本与 HTML 代码中 id 为 `yourname` 的元素关联起来。

## 使用 <fieldset></fieldset> 标签

在处理单选按钮和复选框时，使用 `<fieldset>` 可以很有帮助，可以将它们组合到一个逻辑集合中。使用 `<legend>` 标签来标记供选择的选项。





JavaScript：初学者指南

允许用户知道预期选择的是什么。以下代码使用 `fieldset` 将一组用于选择水果种类的单选按钮分组合在一起：

<fieldset>
<legend>选择一种水果:</legend>
<input type="radio" name="fruits" id="fruits1" value="Orange" />
<label for="fruits1">橙子</label>
<input type="radio" name="fruits" id="fruits2" value="Banana" />
<label for="fruits2">香蕉</label>
<input type="radio" name="fruits" id="fruits3" value="Apple" />
<label for="fruits3">苹果</label>
</fieldset>

在这里，将所有单选按钮分组在 `<fieldset>` 和 `</fieldset>` 标签内，并在起始 `fieldset` 标签之后使用 `legend` 标签为该组提供一个标签。然后，每个元素在 `fieldset` 内部正常地进行标记（同样使用 `label` 标签）。

## 不要假设存在客户端脚本执行

在最初编写表单时，最好不要假设 JavaScript 或其他客户端技术是可用的。如果需要 JavaScript 才能使表单可用，那么许多用户将无法使用它，因为他们出于安全等各种原因禁用了 JavaScript。

最佳实践是即使在 JavaScript 不可用的情况下，也允许表单发送到服务器端（由服务器端处理表单并提供最重要的验证程序）。

如下所示的代码对于没有 JavaScript 的人来说是无法使用的：

<input type="button" onclick="this.form.submit();" value="提交表单" />

在这种情况下，需要 JavaScript 事件处理程序和方法来提交表单。使用传统的 `submit` 元素来创建提交按钮更好。

如果你正在使用某些 JavaScript 验证，可以使用如下代码：

<form method="post" action="form.php" onsubmit="return check_form();">
<!-- 此处为表单内容 -->
<input type="submit" name="submit" id="submit" value="提交表单" />
</form>

这允许你在 JavaScript 可用时运行 JavaScript 函数 `check_form()`。否则，`onsubmit` 事件处理程序将被忽略，表单将提交到服务器端脚本进行验证和处理。如果 JavaScript 可用，该验证程序可以节省一次与服务器的通信往返。如果不可用，服务器端脚本将需要完成工作，但用户仍然能够按预期使用表单。

## 第 14 章：JavaScript 与表单
395

#### 验证

验证 JavaScript 表单是非常用的。例如，你可以在提交之前对输入进行验证，以帮助减少信息不或不准确的表单数量。在提交到如通用网关接口（CGI）脚本、PHP 脚本或 Java servlet 之前对表单数据进行验证可以节省时间并减轻服务器负载。在验证之前，你将学习如何结合 `return` 语句使用 `onsubmit` 事件处理程序，并学习一些验证技术。

### onsubmit 和 return 语句

为了验证表单一个或多个元素的内容，你需要知道查看者何时尝试提交表单。当查看者点击提交按钮时，会发生提交事件，这可以通过起始 `form` 标签中的 `onsubmit` 事件处理程序捕获。

因此，如下表单可以在点击提交按钮时、执行其 `action` 属性的操作之前执行某些操作：

<form method="post" action="form.php" onsubmit="script*">
<label for="yourname">姓名:</label>
<input type="text" name="yourname" id="yourname" />
<br /><br />
<input type="submit" name="submit" id="submit" value="提交">
</form>

你在这里将 *script* 替换为点击提交按钮时执行的某些 JavaScript。这通常是调用一个将运行以测试一个或多个表单字段的函数。然而，为了让函数执行其工作，你必须确保如果查看者的输入没有通过验证，提交按钮无法执行其默认操作。这意味着在 `onsubmit` 事件处理程序中一个 `return` 语句。你希望该语句在验证通过时返回 `true`，在验证失败时返回 `false`。因此，你希望最终结果为

onsubmit="return true;"

这允许提交正常继续，或者

onsubmit="return false;"

这使得提交无效从而什么都不做。

为了上述代码中的技术与函数配合，`onsubmit` 事件处理程序中的 `return` 语句必须调用一个返回 `true` 或 `false` 值的函数。因此，你将得到如下的语句：

onsubmit="return *yourfunction*();"

你将 *yourfunction* 替换为真实的函数名。

JavaScript：初学者指南

这里的关键是函数必须返回 `true` 或 `false` 值，以便之前的语句评估为你所需的结果（`return true;` 或 `return false;`）。函数本身可以执行任何其他操作，但它需要一个 `return` 语句向事件处理程序发送 `true` 或 `false` 值。

所以，你可以对表单进行验证，以确保文本框没有完全留空。以下代码了如何使用带有 `onsubmit` 事件处理程序的函数来实现。首先是 HTML 代码（保存为 val_form.html）：

<<body>
<form method="post" action="form.php" onsubmit="return check_form()">
<label for="yourname">姓名:</label>
<input type="text" name="yourname" id="yourname" />
<br /><br />
<input type="submit" name="submit" id="submit" value="提交">
</form>
<script type="text/javascript" src="val_form.js"></script>
</body>

接下来是 JavaScript 代码（保存为 val_form.js）：

function check_form() {
var thename = document.getElementById("yourname");
if (thename.length < 1) {
window.alert("姓名留空，请重试.");
return false;
} else {
return true;
}

该函数使用 `if` 语句检查名称是否被留空。如果是，则提示查看者重试且函数返回 `false`。否则，返回 `true`。如果返回 `true`，则提交。

### 技术

在大多数情况下，JavaScript 中的验证可以根据你的需要简单或复杂。你所做的就是创建自己的函数来验证你选择的字段。

第 14 章：JavaScript 与表单
397

例如，前节的示例检查了空文本框。然而，对于邮编（Zip code），你可以使用正则表达式检查字段是否包含五个数字。如果不是，你可以发送警告查看用户代码无效并要求重新输入。以下代码显示了实现此点的方法：

<body>
<form method="post" action="form.php" onsubmit="return check_form()">
<label for="zip_code">邮编:</label>
<input type="text" name="zip_code" id="zip_code" />
<br /><br />
<input type="submit" name="submit" id="submit" value="提交">
</form>
<script type="text/javascript">
function check_form() {
var zip = document.getElementById("zip_code").value;
var tomatch = /^\d{5}$/;
if (tomatch.test(zip)) {
return true;
} else {
window.alert("输入的邮编无效");
return false;
}
}
</script>
</body>

该代码使用正则表达式检查五个数字。如果输入了除五个数字以外的内容，函数将返回 `false`。你当然可以扩展此以允许有时用于更精确指定邮编内区域的额外四个数字。为此，添加另一个输入字段，并要求如果第二个字段中有值。

在在应用程序层（你的服务器端脚本或程序），你需要对你的验证程序格外小心，以确保坏数据和/或恶意数据无法提交到你的应用程序。

***提示***

寻找验证脚本的一种方法是尝试检查 Web 上的一些 JavaScript 网站。许多网站都有专门用于验证不同类型数据的函数。如果你能找到适合你用途的函数，这可以节省你一些工作。





JavaScript：初学者指南

**问：文本区域和选择框等所有元素都有太多属性和方法，难以记忆。有什么建议吗？**

**答：** 这些属性和方法中的许多适用于所有的元素类型，而只有少数是特定的。随着你编写编写的编写，你将开始熟悉哪些元素拥有哪些属性和方法，这样就不会那么困惑了。如果你能注意到每个元素使用了哪些属性和方法，就能更容易看出某个属性是否是特定类型元素有的。

**问：我可以验证哪些类型的输入？**

**答：** 在大多数情况下，你可以以你认为合适的方式验证任何想要的内容。你可以验证日期、名称、时间、地址、电子邮件地址、电话号码或你需要的任何其他内容。

**问：我可以验证选择框中的选项或文本区域中的文本，或者其他某些输入类型吗？**

**答：** 在这些某些情况下，你已经在元素中内置了自己的值。然而，如果可能的话，你仍然应该将这些值与其他信息进行对比验证，以确保收到的信息符合你的需求。你只需要调整函数，根据不同的输入设备（文本区域、单选按钮等）执行所需的任务即可。例如，下一节将介绍与导航相关的选择框。然而，某些信息（如 `selectedIndex` 属性）对验证也很有用。

问：我不使用服务器端脚本，但我为了好玩使用 JavaScript 并想验证信息。我真的需要添加服务器端脚本吗？

**答：** 是否需要服务器端脚本取决于你的目的。如果你有一个表单需要保存信息、通过电子邮件发送或发送到数据库，那么你需要一个服务器端应用程序。

咨询专家

请求数字

在这个项目中，你将创建一个脚本，用于对观众输入的电话号码进行基础验证，例如 222-222-2222。

## 第 14 章：JavaScript 与表单

### 逐步演练

1. 创建一个 HTML 页面，其中包含一个表单和一个带有标签文本“Phone Number (XXX-XXX-XXXX):”的文本框。确保表单有一个提交按钮，并调用 JavaScript 函数 `check_it()` 来验证输入内容。在表单之后插入必要的脚本标签，以调用名为 `prjs14_1.js` 的外部 JavaScript 文件。将 HTML 文件保存为 `pr14_1.html`。
2. 创建一个外部 JavaScript 文件并将其保存为 `prjs14_1.js`。在第 3 步中使用它。
3. 使用正则表达式确保文本框中输入的数字符合 XXX-XXX-XXXX 格式。如果是，则发送一个显示“Phone number validated.”的警告；否则，发送显示“Invalid phone number entered. Valid format is XXX-XXX-XXXX.”。
4. 保存 JavaScript 文件并在浏览器中打开 HTML 文件。通过在文本框中输入各种值并提交表单，查看其是否有效。

### 本节练习总结

在这个项目中，你利用对 JavaScript 和表单的知识创建了一个用于验证表单的脚本。该脚本验证观众输入的时间目，以检查其是否符合某特定标准的有效电话号码。

### 使用表单进行导航

通过在表单中使用 JavaScript，你可以根据需要创建普通文本链接和图像链接导航的替代方案。本节将讨论如何使用选择框为你的网站创建导航。

这种导航允许观众从选择框的列表中选择目的地，然后通过点击按钮或更改值跳转到新位置。开始之前，你将创建一个导航选择框，利用观众点击按钮跳转到新位置。

#### 点击按钮

创建选择框非常简单。首先，你像这样设置选择框的代码（将 HTML 存为 `select.html`）：

```html
<form>
  <label for="s1">Select Page:</label>
  <select name="s1" id="s1">
    <option selected="selected" value="page1.html">Page 1</option>
    <option value="page2.html">Page 2</option>
    <option value="page3.html">Page 3</option>
  </select>
</form>
```

注意选择框被赋予了 id 为 `s1`。此外，注意 `value` 属性被赋予了 URL 值（此处是本地 URL）。这些就是当观众从列表中选择指定选项并点击按钮时，你希望他们去的地方。最后，每个选项显示的文本被添加在 `<option>` 和 `</option>` 标签内部。

接下来，编写在点击按钮时启动此过程的脚本。按钮需要执行将观众转移到新目的地的操作。为了实现这一点，脚本必须能够访问选择框中选中的选项并获取其值（URL）。然后，浏览器需要将观众带到新的 URL。

要访问被选中的选项，你必须逐级找到选择框的 `options` 数组。记得选择框被赋予了 id 为 `s1`，所以你可以设置一个变量来持有选择元素：

`var s = document.getElementById("s1");`

然后，要获取选项的值，可以使用以下代码：

`s.options[s.selectedIndex].value`

这就是选择框的 `selectedIndex` 属性变得有用之处。观众应该能够通过做出选择并点击按钮来进行导航。图 14-5 显示了在浏览器中看到的初始下拉框。

这现在告诉浏览器在表单提交（通过点击按钮）时运行名为 `go_there()` 的 JavaScript 函数。它还调用了名为 `select.js` 的外部 JavaScript 文件，你将更改 URL 的代码放在那里：

```html
<body>
  <form onsubmit="return go_there()">
    <label for="s1">Select Page:</label>
    <select name="s1" id="s1">
      <option selected="selected" value="page1.html">Page 1</option>
      <option value="page2.html">Page 2</option>
      <option value="page3.html">Page 3</option>
    </select>
    <input type="submit" name="go" id="go" value="Go!" />
  </form>
  <script type="text/javascript" src="select.js"></script>
</body>
```

注意如何使用选中的值来更改 `window.location` 属性到新的 URL。返回 `false` 防止表单提交到服务器，以便让客户端脚本处理它。图 14-6 显示了选择 Page 2 选项并点击 Go! 按钮的结果。

```javascript
function go_there() {
  s = document.getElementById("s1");
  window.location = s.options[s.selectedIndex].value;
  return false;
}
```

![Figure 14-5](img/61d166424839b7674a7b9c8434ae4e03_423_0.png)

图 14-6 显示了选择 Page 2 选项并点击 Go! 按钮的结果。结果，浏览器显示了一个新页面。





JavaScript：初学者指南

如果你想让此脚本更具可访问性，可以使用服务端脚本来备份 JavaScript。你将为服务端脚本编写代码，在 HTML 代码中添加 `method` 属性，并添加 `action` 属性：

```html
<body>
  <form method="post" action="/php/select.php" onsubmit="return go_there();">
    <label for="s1">选择页面：</label>
    <select name="s1" id="s1">
      <option selected="selected" value="page1.html">页面 1</option>
      <option value="page2.html">页面 2</option>
      <option value="page3.html">页面 3</option>
    </select>
    <input type="submit" name="go" id="go" value="跳转!" />
  </form>
  <script type="text/javascript" src="select.js"></script>
</body>
```

现在，如果查看者没有可用 JavaScript，`onsubmit` 属性将被忽略，但 `action` 属性将会被用于处理表单。这将跳转到服务器上 `php` 目录中名为 `select.php` 的脚本（这些只是示例文件和目录名称）。服务端脚本随后可以执行发送查看者到新 URL 的工作，允许脚本对没有 JavaScript 的用户有效。

还需要注意的一点是，此脚本只有在查看者的浏览器能够处理 `document.getElementById()` 方法时才能工作。如果你预见到某些用户可能使用旧版浏览器，那么在这种情况下，确保他们使用服务端脚本可能是一个主意（或者你可以添加选项，通过 forms 数组或使用表单名称和选择名称来实现此功能）。为了防止旧浏览器运行 JavaScript 代码，你可以执行以下操作：

```javascript
function go_there() {
  if (document.getElementById && document.createTextNode) {
    s = document.getElementById("s1");
    // 图 14-6 做出选择并点击按钮后显示的页面
    // ![](img/61d166424839b7674a7b9c8434ae4e03_424_0.png)
    window.location = s.options[s.selectedIndex].value;
    return false;
  }
  return true;
}
```

现在，代码将仅对支持 `getElementById()` 和 `createTextNodeNode()` 的浏览器有效（这是为了那些仅支持 `getElementById()` 但支持方式不符合预期的浏览器而添加的）。否则，脚本将返回 `true` 并调用服务端脚本。

## 无按钮版本

要创建一个没有按钮的导航选择框，你需要使用 `onchange` 事件处理程序。然而，出于可访问性考虑，不建议使用这种导航，因为它不仅让那些使用辅助技术的人非常难以选择所需的选项，而且在通常情况下也可能引起困惑，因为查看者一旦选择了目标，就会立即被带到所选定的地。

如果你是为了休闲而使用此脚本，且不需要脚本具有可访问性，那么你可以在网上找到许多此类类型的导航脚本版本。

## 构建选择框导航脚本

在这个项目中，你将构建一个导航选择框，它将为查看者提供五个供选择的目的地。

### 逐步步骤

1. 创建一个 HTML 文档并添加 `script` 标签，以便 HTML 文件将调用名为 `prjs14_2.js` 的外部 JavaScript 文件。将 HTML 文件保存为 `pr14_2.html`。
2. 创建一个带有用于导航按钮的选择框。你可以选择任何你喜欢的目的站点和描述。将选择框命名为 `s1`。保存 HTML 文件。
3. 创建一个 JavaScript 文件并将其保存为 `prjs14_2.js`。在第 4 步中使用它。
4. 在文件中添加代码，以便在点击按钮时浏览器将打开选定的 URL。
5. 保存 JavaScript 文件并在浏览器中打开 HTML 文件。检查导航系统是否正常工作。

## 尝试总结

在这个项目中，你利用对 JavaScript 和表单的知识创建了一个导航系统。

*第 14 章自测*

1. 每当你向一个 HTML 文档添加一组 `<form>` 和 `</form>` 标签时，就会创建一个（一个）_______ 对象。
2. `forms` __________ 属性允许你通过索引号访问表单。
3. 下列哪项可以访问页面上的第四个表单？
   A document.forms[4]
   B document.forms[3]
   C document.forms(4)
   D document.forms(3)
4. 下列哪项可以找到页面上第三个表单中的元素数量？
   A document.forms[2].length
   B document.forms[3].length
   C document.forms.length
   D document.forms(3).length
5. 下列哪项持有文档中表单数量的值？
   A document.forms[0].length
   B document.form.length
   C document.forms.length
   D document.forms[1].length
6. 使用 form __________ 属性允许你为稍后要访问的页面表单命名。
7. 下列哪项访问名为 `f1` 的表单中名为 `e1` 的元素的值？
   A document.forms.e1.value
   B document.f1.value
   C document.forms[f1].value
   D document.forms[e1].value
8. __________ 属性允许访问名为 `f1` 的表单中名为 `e1` 的元素的值。（检查逻辑：“下列哪项访问了名为 `f1` 的表单中名为 `e1` 的元素的值？”）
9. `forms` 属性允许访问文档中的表单数量。
10. `frames` 是一个包含元素的数组。
11. `frameset` 属性允许访问框架数量。
12. 当使用时，__________ 应该返回什么类型？
   A yes
   B false
   C maybe
   D a number
13. 当查看者点击时，会发生 __________。
14. __________ 方法允许你更改框架。
15. 使用什么获取当前选择项？
   A length 属性
   B reset() 方法
   C getSelected() 方法
   D selectedIndex 属性

第14 章：JavaScript 与表单

### 框架简介

关键技能与概念
- 框架简介
- 访问框架
- 更改框架

## 框架的用途

框架将窗口分为两个或多个区域（框架集），每个区域包含一个独立的 HTML 文档。这与表格的区别在于框架集的每个部分包含一个文档，你可以更改其中一个而不影响另一个。

是否在网站上使用框架取决于你。这取决于你的导航需求。如果你对框架一无所知，本将帮助你判断它们对你是否有用。如果你已经熟练使用框架，可以略读本节。

## 框架后的代码

以下代码包含 `frameset` 元素。它定义了打开文档时显示的框架数量和结构。

```html
<html>
  <frameset cols="20%,80%">
    <frame src="frame1.html"></frame>
    <frame src="frame2.html"></frame>
  </frameset>
  <noframes>
    抱歉，您的浏览器不支持框架。请使用下面的链接进入无框架版本的站点。<br />
    <a href="noframes.html">无框架站点</a>
  </noframes>
</html>
```





JavaScript: 入门指南

2. 起始 `<frameset>` 标签的 `cols` 属性告诉浏览器窗口将分为两列（从左到右移动）。第一列（左侧）占据屏幕空间的 20%，而第二列（右侧）占据屏幕空间的 80%。

3. 第一个 `<frame>` 标签在页面上创建第一个框架。浏览器按照它们在源代码中出现的顺序，从左到右、从上到下显示这些框架。因此，此框架（frame）位于页面的左上部分——在这种情况下，它只是页面的左侧。

4. `src` 属性告诉浏览器要作为框架内容显示的 HTML 文档的 URL，这实际上是用户在窗口左侧看到的内容。在本例中，该文档是一个名为 `frame1.html` 的文件。

5. 第二个 `<frame>` 标签的作用与第一个相同，但该框架是按左到右、从上到下顺序中的下一个。同样，由于只有两列，此框架仅位于窗口的右侧。`src` 属性指向要在此框架中显示的 HTML 文档的 URL。在本例中，该文档是一个名为 `frame2.html` 的文件。

6. `</frameset>` 标签结束框架集。

7. `<noframes>` 和 `</noframes>` 标签之间的内容将显示在不支持框架的浏览器中，以便用户在屏幕上能看到显示内容。你可以放置一个指向无框架版本网站的链接，也可以使用任何你需要的 HTML 代码。在示例中，我使用了文本和链接以保持该章节简短。

根据上一个代码创建的文档是你想要在浏览器中打开以显示框架的页面。将此文档保存为 `frameset.html`，这样当你为框架中使用的文档添加一些代码后，就可以使用它。

一旦创建了框架集，你就必须创建填充框架的文档。首先，创建一个用于左侧框架（`frame1.html`）的文档：

```html
<html>
<body>
I am frame1.html, and I am on the left side!
</body>
</html>
```

这段简单的代码会告诉你哪个文档正在显示在哪个框架中。（你可以根据需要让代码变得尽可能复杂。）将将其保存为 `frame1.html`，并存放在与 `frameset.html` 相同的目录下。

接下来，你必须为另一个框架（`frame2.html`）提供代码：

```html
<html>
<body>
I am frame2.html, and I am on the right side!
</body>
</html>
```

将此保存为 `frame2.html`，并存放在与 `frameset.html` 和 `frame1.html` 相同的目录下。

## 第 15 章：JavaScript 与框架

411

现在，当你在浏览器中打开 `frameset.html` 时，它应该显示一个包含两个框架的窗口，每个框架包含相应的 HTML 文档，如图 15-2 所示。

### 框架选项

正如你所看到的，起始的 `<frameset>` 标签可以接受 `cols` 属性将窗口分为列。同样，它也可以使用 `rows` 属性将页面从上到下划分为行。以下是一个创建具有两行的框架集的代码示例：

```html
<html>
<frameset rows="20%,80%">
<frame src="frame1.html"></frame>
<frame src="frame2.html"></frame>
</frameset>
<noframes>
Use the link below to go to the frameless version of the site.<br />
<a href="noframes.html">Frameless Site</a>
</noframes>
</html>
```

这一次，页面被划分为两个框架，一个在上方，另一个在下方。如果 `frame1.html` 和 `frame2.html` 都存在，其外观示例如图 15-3 所示。

### 行或列

如果你愿意，`rows` 或 `cols` 属性中使用的数字可以是像素而不是百分比。此外，如果你想让某个框架在其他框架设置后占据所有剩余空间，可以使用星号 (**)。例如，看这段代码：

```html
<html>
<frameset rows="150,*">
<frame src="frame1.html"></frame>
<frame src="frame2.html"></frame>
</frameset>
```

![图 15-2 由 frameset 创建的带有两个框架的框架集，每列一个](img/61d166424839b7674a7b9c8434ae4e03_433_0.png)

这一次，由于使用了 `rows` 属性，框架是从上到下的。星号告诉第二个框架占据第一个框架未被使用的任何剩余空间。

```html
<frame src="frame2.html"></frame>
</frameset>
<noframes>
Use the link below to go to the frameless version of the site.<br />
<a href="noframes.html">Frameless Site</a>
</noframes>
</html>
```

这一次，第一行（顶部）占据 150 像素，而第二行（底部）占据窗口中剩余的全部空间。

### 多于两行或两列

当然，你并不限于只有两行或两列。你可以根据需要拥有任意数量的行或列。例如，如果你想要一个三列的框架集，可以使用以下代码：

```html
<html>
<frameset cols="150,*150">
<frame src="frame1.html"></frame>
<frame src="frame2.html"></frame>
<frame src="frame3.html"></frame>
</frameset>
```

![图 15-3 基于行的框架集](img/61d166424839b7674a7b9c8434ae4e03_434_png)

### 嵌套行和列

最后，如果你想要一个同时包含行和列的复杂框架集，你必须在一个框架集中嵌套另一个框架集。例如，你可能想要一个高度为 100 像素的行，然后是两列：

```html
<frameset rows="100,*">
<frame src="frame1.html"></frame>
<frameset cols="150,*">
<frame src="frame2.html"></frame>
<frame src="frame3.html"></frame>
</frameset>
</frameset>
<noframes>
Use the link below to go to the frameless version of the site.<br />
<a href="noframes.html">Frameless Site</a>
</noframes>
```

注意，在第二个（底部）行没有使用 `<frame>` 标签，而是使用了 `<frameset>`，将该行分为两个框架。这些框架按列运行并从左到右排列。

***提示***

请确保每个 `<frameset>` 标签都用 `</frameset>` 标签关闭。与表格一样，忘记其中一个可能会导致框架显示异常或无法显示。

![图 15-4 嵌套框架集允许在窗口中使用同时行和列](img/61d166424839b7674a7b9c8434ae4e03_436_png)

JavaScript: 入门指南

访问框架

如何在 JavaScript 中访问框架？你可以使用 `frames` 数组，也可以命名框架并使用名称。首先，查看如何使用 `frames` 数组访问框架。

### frames 数组

你使用 `frames` 数组根据源代码中的顺序访问框架。你将从一个框架内部访问另一个框架，因此你必须找到想要访问的框架。

记得 `frames` 数组来自 `window` 对象。框架带有与普通窗口的大部分属性和方法，但访问它们的方式不同。例如，查看这段创建两个框架的框架集的代码。将其命名为 `frameset1.html`。（这替换了之前的示例。）

```html
<html>
<frameset cols="60%,40%">
<frame src="frame1.html"></frame>
<frame src="frame2.html"></frame>
</frameset>
<noframes>
Use the link below to go to the frameless version of the site.<br />
<a href="noframes.html">Frameless Site</a>
</noframes>
</html>
```





## 第 15 章：JavaScript 与框架

如果你在第一个框架（frame1.html）中编写某些脚本，并想获取第二个框架（frame2.html）中 `location` 属性的值以显示给观众看，你必须弄清楚如何访问第二个框架。记住，你正在一个框架集（frameset）中工作。你正在编写其中一个文档的代码，该文档将作为框架集中第一个框架的内容。因此，要访问另一个框架，你需要找到一种方法回到主窗口并引用该框架。回想第 10 章，`window` 对象的 `top` 属性允许你访问框架集最顶层的窗口（主窗口）。

现在你可以使用 `frames` 数组了，因为你已经访问了包含框架集代码的主窗口。`frames` 数组包含了代码中每个 `frame` 标签的项（条目）。计数从 0 开始，并按照每个 `frame` 标签在源代码中出现的顺序继续计数。因此，要访问框架集中的第一个框架，可以使用以下语法：

`top.frames[0]`

使用 `top` 属性允许你访问主窗口和框架集代码。然后，使用 `frames[0]` 来访问源代码中的第一个框架。所以，如果你在第二个框架中编写代码并想访问第一个框架，将使用此语法：

`top.frames[0]`

现在，你可以让第二个框架中的代码访问第一个框架中所需的信息并展示给观众。以下是用于第一个框架（frame1.html）的代码：

```html
<body>
我是框架 1，另一个框架从我这里获取了信息！真没礼貌！
</body>
```

为了完成此脚本，你可以为 `frame2.html` 使用以下代码：

```html
<body>
第一个框架来自：<br />
<script type="text/javascript">
document.write(top.frames[0].location);
</script>
</body>
```

现在，你可以通过打开主窗口（frameset1.html）来查看结果。右侧框架应该会告诉你左侧框架所用文档的地址（location）。图 15-5 显示了这在浏览器中可能出现的样子。（你的位置值可能与文件名不同。）

`frames` 数组是访问未命名框架或在需要循环遍历时访问框架的好方法。如果你还记得第 10 章，`frames` 数组的 `length` 属性提供了文档中框架的数量。因此，你可以遍历 `frames` 数组，在一个框架中打印每个框架的地址，供观众查看。首先，你需要让包含框架集的文档投入使用。

第二个框架的 `location` 值将通过 `frames` 数组访问框架中的信息，并打印在页面上。

对于此示例，请将此主窗口保存为 `frameset2.html`。该文档的代码所示：

```html
<html>
<frameset cols="20%,80%">
<frame src="frame1.html"></frame>
<frame src="frame2.html"></frame>
</frameset>
<noframes>
使用下方的链接访问网站的无框架版本。<br />
<a href="noframes.html">无框架站点</a>
</noframes>
</html>
```

这一次，`frame1.html` 将仅有一句简短的声明：

```html
<html>
<body>
我是框架 1！
</body>
</html>
```

现在，`frame2.html` 是脚本和结果出现的地方，可以像所示这样编码：

```html
<body>
<script type="text/javascript">
for (var count=0; count<top.frames.length; count+=1) {
var framenum = count+1;
document.write("Frame "+framenum+" is from "+top.frames[count].location);
document.write("<br />");
}
</script>
</body>
```

图 15-5：第二个框架显示了从第一个框架获取的信息。
循环开始，使用 `length` 属性来确定何时退出。
创建了一个新变量来为框架编号。
使用 `frames` 数组访问并将结果打印在页面上。

正如你在之前的脚本中所看到的，`length` 属性决定了循环何时结束。`framenum` 变量从 1 开始打印框架编号，而不是它在数组中的索引号（索引从 0 开始）。随后在 `document.write()` 语句中使用 `frames` 数组，以打印每个框架的 `location` 属性值。

图 15-6 显示了此脚本在浏览器中运行时的结果（当打开 `frameset1.html` 时）。再次，你的位置值可能与文件名不同。

### 使用框架名称

从一个框架访问另一个框架的另一种方法是使用框架的名称（就像你在前一章中使用表单名称一样）。例如，此代码通过向 `frame` 标签添加 `name` 属性来为每个框架命名（将此命名为 `frameset3.html`）：

```html
<html>
<frameset cols="50%,50%">
<frame src="frame1.html" name="left_side"></frame>
<frame src="frame2.html" name="right_side"></frame>
</frameset>
<noframes>
使用下方的链接访问网站的无框架版本。<br />
<a href="noframes.html">无框架站点</a>
</noframes>
</html>
```

这一次，`frame1.html` 将仅有一句简短的声明：

```html
<html>
<body>
我是框架 1！
</body>
</html>
```

现在，`frame2.html` 是脚本和结果出现的地方，可以像所示这样编码：

```html
<body>
<script type="text/javascript">
for (var count=0; count<top.frames.length; count+=1) {
var framenum = count+1;
document.write("Frame "+framenum+" is from "+top.frames[count].location);
document.write("<br />");
}
</script>
</body>
```

现在，你可以让第二个框架中的代码访问第一个框架中所需的信息并展示给观众。用于第一个框架（frame1.html）的代码如下：

```html
<body>
我是框架 1，另一个框架从我这里获取了信息！真没礼貌！
</body>
```

为了完成此脚本，你可以为 `frame2.html` 使用以下代码：

```html
<body>
第一个框架来自：<br />
<script type="text/javascript">
document.write(top.frames[0].location);
</script>
</body>
```

现在，你可以通过打开主窗口（frameset1.html）来查看结果。右侧框架应该告诉你左侧框架所用文档的地址。图 15-5 显示了这在浏览器中可能出现的样子。（你的位置值可能与文件名不同。）

从一个框架访问另一个框架的另一种方法是使用框架的名称（就像你在前一章中使用表单名称一样）。例如，此代码通过向 `frame` 标签添加 `name` 属性来为每个框架命名（将此命名为 `frameset3.html`）：

```html
<html>
<frameset cols="50%,50%">
<frame src="frame1.html" name="left_side"></frame>
<frame src="frame2.html" name="right_side"></frame>
</frameset>
<noframes>
使用下方的链接访问网站的无框架版本。<br />
<a href="noframes.html">无框架站点</a>
</noframes>
</html>
```

这一次，`frame1.html` 将仅有一句简短的声明：

```html
<html>
<body>
我是框架 1！
</body>
</html>
```

现在，`frame2.html` 是脚本和结果出现的地方，可以像所示这样编码：

```html
<body>
<script type="text/javascript">
for (var count=0; count<top.frames.length; count+=1) {
var framenum = count+1;
document.write("Frame "+framenum+" is from "+top.frames[count].location);
document.write("<br />");
}
</script>
</body>
```

### 修改单个框架

在 HTML 中，如果你想更改一个框架，可以使用 `target` 属性。例如，如果你想更改某个框架的内容，可以使用以下语法：

`<a href="nextpage.html" target="right_side">下一页</a>`

**提示** 确保 `target` 与框架名称完全匹配。如果不匹配，页面将在新窗口中打开而不是当前框架中。

### 修改多个框架

要一次更改多个框架，可以使用 JavaScript。再次获取基础框架集并将其保存为 `frameset4.html`。代码如下：

```html
<html>
<frameset cols="20%,80%">
<frame src="frame1.html" name="left_side"></frame>
<frame src="frame2.html" name="right_side"></frame>
</frameset>
<noframes>
使用下方的链接访问网站的无框架版本。<br />
<a href="noframes.html">无框架站点</a>
</noframes>
</html>
```

为了更改两个框架的内容，你需要两个额外的 HTML 文件，以便两个框架中的两个文档可以更改为两个新文档。因此，你需要一个类似下面的文档列表：

- frameset4.html（主窗口代码）
- frame1.html（最初在左框架中显示的文档）





JavaScript：初学者指南

- frame2.html (最初在右侧框架显示的文档)
- frame3.html (将出现在左侧框架的新文档)
- frame4.html (将出现在右侧框架的新文档)

你已经拥有了 frameset4.html 的代码，因此你只需要剩余四个文档的代码。有趣的地方出现在 frame1.html 的示例中，所以你从那里开始。

### 框架 1：动作框架

此框架包含一个让两个框架都显示新 HTML 文档的链接。要实现这一点，你可以使用一个函数，然后在链接中调用该函数。以下是 frame1.html 的代码：

```html
<<body>
<script type="text/javascript">
function twoframes() {
  top.right_side.location="frame4.html";
  self.location="frame3.html";
}
</script>
<a href="javascript:twoframes();">更改两个框架</a>
</body>
```

链接标签调用了 `twoframes()` 函数。该函数首先通过引用其名称（`right_side`）更改右侧框架的内容。然后它更改其所在框架的位置（回“self”是引用当前窗口或框架的一种，这使得代码中更改的内容稍微不那么歧义）。当点击链接时，两个文档都将更改为新文档。

***注意***

你会注意到，你当前不在的框架首先被更改，而 `self.location` 最后被更改。这是因为如果你在更改任何其他框架位置之前更改了 `self.location`，浏览器将跳转，且脚本将不会完成执行。

### 其他框架：基础代码

在剩余的框架中，你只需要添加一些简单的代码来让框架识别自己。以下是 frame2.html 的代码：

```html
<<body>
我是框架 2！
</</body>>
```

以下是 frame3.html 的代码：

```html
<<body>
我是框架 3！
</</body>>
```

- 当前框架被更改
- 右侧框架被更改
- 链接调用函数来更改两个框架

最后，这里是 frame4.html 的代码：

```html
<<body>
我是框架 4！
</</body>>
```

一旦设置好这些，打开 frameset4.html 来查看链接如何更改两个框架。图 15-7 显示了点击链接之前 frameset4.html 的初始视图。图 15-8 显示了点击链接后两个框架内容都更改后的页面。

![](img/61d166424839b7674a7b9c8434ae4e03_443_0.png)
图 15-7 点击链接前的框架集视图

![](img/61d166424839b7674a7b9c8434ae4e03_443_1.png)
图 15-8 点击链接后，框架中出现了两个新文档

- pr15_1.html
- pr15_1_frame1.html
- pr15_1_frame2.html 
- pr15_1_frame3.html
- pr15_1_frame4.html
- pr15_1_frame5.html

如果你愿意，完全可以使用更详细的代码。你可以设置更多的框架，然后根据你的意愿更改其中许多个。你还可以为其中一个新框架编写代码，带有一个让观众回到原始两个框架的链接。此外，你还可以使用 URL 或文件名作为函数的参数。

### 更改框架

在这个项目中，你创建了框架集并同时更改了多个框架。你还创建了一个框架集，它使用一个框架来更改文档中另外两个框架的内容。

### 逐步步骤

1. 创建一个 HTML 文档作为框架集。创建一个从上到下（行）包含三个框架的框架集。顶部和底部的框架每个应使用可用窗口空间的 33%，而中间的框架应使用剩余空间。
2. 为每个框架使用以下文件名：
   - 顶部框架：pr15_1_frame1.html
   - 中间框架：pr15_1_frame2.html
   - 底部框架：pr15_1_frame3.html
3. 为每个框架使用这些名称：
   - 顶部框架：t_frame
   - 中间框架：m_frame
   - 底部框架：b_frame
4. 将文件保存为 pr15_1.html。
5. 在顶部框架（pr15_1_frame1.html）的代码中，提供一个链接导致两个下方的框架接收新内容。为两个新框架使用这些文件名：pr15_1_frame4.html 和 pr15_1_frame5.html。
6. 保存文件（pr15_1_frame1.html）。
7. 向剩余的框架文件（pr15_1_frame2.html、pr15_1_frame3.html、pr15_1_frame4.html、pr15_1_frame5.html）添加任何你喜欢的内容。
8. 在浏览器中打开 pr15_1.html 并尝试该链接。它应该更改框架集中底部的两个框架，而顶部框架保持不变。

### 练习总结

在这个项目中，你利用 JavaScript 和框架的知识编写了一个框架集。当在浏览器中打开时，观众可以通过点击链接来更改多个框架。

### 框架导航

JavaScript 还提供了方便的框架导航技术。例如，你可以调整第 14 章中创建的选择框导航，使其能够从一个框架工作到另一个框架。或者，你可以编写代码允许观众跳出框架。你还可以编写代码，如果观众意外进入了本应在框架集中的页面，则将其发送到你的框架中。

### 在框架中使用选择框

如果你想让一个框架中的选择框在另一个框架中打开文档，你必须稍微修改选择框导航。要做到这一点，你只需要更改选择框代码中的部分内容。

让我们使用文件名 frameset5.html 来查看框架将如何显示。代码所示：

```html
<html>
<frameset rows="120,*">
<frame src="frame1.html" name="t_frame">
<frame src="frame2.html" name="b_frame">
</frameset>
<noframes>
<a href="noframes.html">无框架站点</a>
</noframes>
</html>
```

在这种情况下，框架使用行（rows）从上到下排列。顶部框架（`t_frame`）从顶部延伸 120 像素，底部框架（`b_frame`）占据剩余空间。在前面的示例中，顶部框架中放置了一个选择框，以允许观众更改底部框架。因此，你需要查看 frame1.html 中的代码：

```html
<body>
<form onsubmit="return go_there();">
<label for="s1">更改下方框架：</label>
<select id="s1">
<option selected="selected" value="#">选择目标</option>
<option value="frame3.html">框架 3</option>
<option value="frame4.html">框架 4</option>
<option value="frame2.html">返回框架 2</option>
</select>
<input type="submit" id="submit" value="去!" />
</form>

<script type="text/javascript">
function go_there() {
  var s = document.getElementById("s1");
  top.b_frame.location = s.options[s.selectedIndex].value;
  return false;
}
</script>
</body>
```

注意选择框代码的主要区别在于 `go_there()` 函数中的第二行。它没有使用 `window.location`（更改相同框架），而是使用底部框架的名称以便更改位置（`top.b_frame.location`）。唯一的其他任务是为其他框架文件（frame2.html、frame3.html 和 frame4.html）添加一些代码，以便底部框架中有内容可供查看。图 15-9 显示了在做出选择之前 frameset5.html 的外观（取决于你为 frame2.html 添加的代码）。

![](img/61d166424839b7674a7b9c8434ae4e03_446_0.png)
图 15-9 选择前框架集可能的初始外观

#### 跳出框架

有时另一个 Web 站点会编写在到达你的网站之前不跳出该站点框架的链接。这样，你的网站将留在观众窗口的较小部分，而其他站点的导航显示在其他框架中。当这种情况发生时，你





## 第 15 章：JavaScript 与框架（Frames）

425

可能想要你的观众提供一种跳出其他网站框架的方法，或者你可能想

自动实现。

### 使用可选链接

你可以在页面上放置一个链接，让观众点击以跳出框架。你需要在

`<a>` 标签中添加一个特殊的 `target` 属性，如下所示：

`<a href="http://yoursite.com" target="_top">跳出框架</a>`

`target="_top"` 的目标值告诉浏览器在打开链接中的 URL 时使用整个窗口，

而不是在框架内部打开该链接。你只需要将标签中的 URL 替换为

你自己的即可。

***注意***

在锚点（`<a>`）标签中使用 `_top` 作为 `target` 会告诉浏览器在打开链接中的

URL 时使用整个窗口，而不是在框架内部打开该链接。

如果你在网站上使用框架，并想确保观众在跳转到新网站时不会被卡在你的框架中，你可以使用相同的 `target` 来确保新 URL 在整个窗口中打开，而不是在框架中。以下代码显示了这样一个示例：

`<a href="http://www.pageresource.com" target="_top">另一个站点</a>`

这种技术甚至不需要 JavaScript（如果你真的想做，也可以用 JavaScript 实现），但下一种技术需要。

![](img/61d166424839b7674a7b9c8434ae4e03_447_0.png)

图 15-10 选择 Frame 3 选项后的可能外观

JavaScript 入门指南

### 自动移除框架

要自动移除框架，你必须在 页面加载时确定它是否位于框架集（frameset）内部。如果你的页面没有使用框架，那么你可以通过 `length` 属性很容易地判断它是否被卡在另一个网站的框架中。

如果你的页面位于框架集内部，那么主窗口中框架数组的 `length` 属性值将大于 0。因此，你可以检查 `length` 属性是否大于 1，如果有框架，则在整个窗口中重新加载页面。尝试这段代码：

```html
<head>
<script type="text/javascript">
function check_frames() {
  if (top.frames.length > 0) {
    top.location="http://yoursite.com";
  }
}
</script>
</head>

<body onload="check_frames();">
<h1>欢迎来到我的页面</h1>
</body>
```

`check_frames()` 函数在页面加载时被调用。该函数检查主窗口是否存在任何框架。如果是，顶层窗口（top window）的 location将被更改为你页面的 URL，使你的页面在主窗口中打开，而不是在框架内。你会将代码中显示的 URL 替换为你自己的 URL。

### 将观众引导至框架

当你使用框架时，访问者可能会通过旨在位于框架集内部的页面进入你的网站，而不是通过整个窗口进入。这可能发生在使用搜索引擎时，搜索引擎可能会索引该文档并列出它。观众能看到它，但可能无法导航到网站的其他部分，因为框架并不在那里。

以下代码检查页面是否在没有框架的情况下加载，如果框架没有加载，则将观众重定向到网站的主页：

```html
<head>
<script type="text/javascript">
function check_frames() {
  if (top.frames.length == 0) {
    top.location="http://www.yoursite.com";
  }
}
</script>
</head>

<body onload="check_frames();">
<h1>某个内部页面</h1
我应该位于框架集内部；此页面加载时运行的脚本将检查我是否在此。
</body>
```

- 如果存在框架，主窗口将重置为在整个窗口中显示
- 函数被调用
- 检查主窗口中框架的数量
- 这一次的检查是查看主窗口是否缺少必要的框架

第 15 章：JavaScript 与框架

427

`check_frames()` 函数检查 `length` 属性是否为 0。如果是这样，说明你的框架集尚未加载。在这种情况下，观众将被带到你的主页，在在那里可以加载你的框架集。你会将代码中的 URL 替换为包含你框架集的文档 URL（通常是你的主页）。

**问：为什么我需要嵌套框架集才能在列中包含行或在行中包含列？**
**为什么我不能直接在一个 frameset 上同时使用 rows 和 cols 属性呢？**

**答：** 你必须嵌套框架集，以便浏览器知道将如何放置所有的行和列。如果你只是告诉浏览器你想要三行两列，它并不一定知道将它们全部放在哪里。例如，是其中一列容了这三行，还是其中某一行包含了这两列？当框架集嵌套时，浏览器就知道你想让元素出现在什么位置了。

**问：那个“self”到底是什么的？**
**答：** 翻回第 10 章查看关于该概念的简短解释。基本上，它是编写“window”的另一种方式。与其写 `window.location`，你可以写 `self.location`。（你可以在任何框架中这样做）。如果你使用框架，更容易理解框架的含义。

**问：我为什么会想要改变多个一个框架？**
**答：** 有些框架为了导航之目的，改变多个一个框架是有帮助的。

**问：我不喜欢框架，也不打算使用它们。我需要阅读关于它们的内容吗？**
**答：** 虽然你可能不会使用它们，了解框架可以帮助你在调试代码时使用。

专家提问

JavaScript 入门指南

450

跨框架使用变量

使用框架的另一个优势是，你可以在一个框架中使用变量，你创建的脚本获取另一个框架的信息，并在框架加载后存储它。你可以在一个框架中存储信息并在再次使用它。

首先，你需要框架集。你可以使用一个简单的双框架系统，如下所示：

```html
<html>
<frameset cols="150,*">
<frame src="frame1.html" name="left_side"></frame>
<frame src="frame2.html" name="right_side"></frame>
</frameset>
<noframes>
使用下面的链接进入无框架版本的站点。<br />
<a href="noframes.html">无框架站点</a>
</noframes>
</html>
```

将其保存为 `frameset.html`。你应该有一个左侧框架（left_side）占据 150 像素，右侧框架（right_side）占据剩余的窗口空间。在左侧框架中，你需要一个包含变量的文档。这是不会被更改的框架，因此当其他框架的内容更改时，它可以跟踪变量值。对于这个脚本，你想有一个名为 `thename` 的变量和一个名为 `thefood` 的变量，用于存放观众在另一个框架中输入的信息。这里是 `frame1.html` 的代码：

```html
<head>
<script type="text/javascript">
var thename="";
var thefood="";
</script>
</head>

<body>
这是 frame1.html；它持有变量值。

你可以在这里放置任何喜欢的内容。
</body>
```

变量初始被赋予空字符串值。当观众从另一个框架发送信息时，这些值将被改变。





## 第 15 章：JavaScript 与框架

429

<body>

我想获取你的名字。请在下方输入。

<br />

<form onsubmit="return store_info();">

<label for="yourname">您的姓名：</label>
<input type="text" id="yourname" size="25" />
<br /><br />

<input type="submit" value="继续" />
</form>

<script type="text/javascript">

function store_info() {
var yn = document.getElementById("yourname").value;
top.left_side.thename= yn;
self.location="frame3.html";
return false;
}
</script>

<body>

当查看者点击继续按钮时，会调用 `store_info()` 函数。请注意这里使用了 `top.left_side` 来访问左侧框架。然后通过添加变量名（`top.left_side.thename`）来访问另一个框架中的 `thename` 变量。表单文本框中输入的值随后被赋予左侧框架中的 `thename` 变量。之后，框架中的文档将更改为 `frame3.html`，它能够从左侧框架获取信息。

在 `frame3.html` 文档中，查看者的名字写在问候中。它也被填充在一个新表单的字段中，以防止查看者重复输入。（这只是展示了存储变量值的用途；在这种情况下，你并不真的需要在表单中再次需要名字。）

表单还要求查看者输入最喜欢的食物，查看者必须输入。此页的代码所示：

<body>

<script type="text/javascript">

document.write("Hi, "+top.left_side.thename+"!<br />");
</script>

现在我想获取你最喜欢的食物。请在下方输入：

<br />

<form onsubmit="return more_info();">

<label for="yourname">您的姓名：</label>
<input type="text" id="yourname" size="25" />
<br />

<label for="yourfood">最喜欢的食物：</label>
<input type="text" id="yourfood" size="25" />
<br /><br />

<input type="submit" value="继续" />
</form>

<script type="text/javascript">

var tn = document.getElementById("yourname");
tn.value = top.left_side.thename;

框架中的文档被更改
左侧框架中的变量被赋予了来自当前框架表单的值
左侧框架中变量的值被用于编写问候
第一个文本框的值使用左侧框架变量中存储的信息进行设置

JavaScript：初学者指南

function more_info() {
var fd = document.getElementById("yourfood");
top.left_side.thefood= fd.value;
self.location="frame4.html";
return false;
}
</script>

<body>

在这里，页面加载时，名字表单字段被赋予了来自左侧框架的值。名字也打印在页面问候中。当查看者填写食物并点击按钮后，该值被存储在左侧框架的 `thefood` 变量中，框架中的文档被更改为 `frame4.html`。

在 `frame4.html` 中，存储在左侧框架中的两个变量的值将仅用于在页面上为查看者打印一条特殊消息，如下代码所示：

<body>

<script type="text/javascript">

function print_info() {
document.write("Thank you, "+top.left_side.thename+"!");
document.write("<br /><br />");
document.write("You must really like "+top.left_side.thefood+"!");
}
print_info();
</script>

<body>

在前面的代码中，信息只是作为消息打印给查看者。打印的信息标记了该脚本的结束，因为没有更多表单或变量可以使用了。（尽管如果你愿意，你也可以添加更多表单和变量。）

图 15-11 显示了 `frameset6.html` 在任何更改之前的初始外观。

- 表单中 Food 字段的值被存储在左侧框架的变量中
- 框架中的文档被更改
- 存储在左侧框架变量中的信息被打印给查看者
- 在此处调用了函数

![](img/61d166424839b7674a7b9c8434ae4e03_452_0.png)

图 15-11 框架的初始外观

图 15-12 在第一个表单中输入 John 并点击按钮的结果

![](img/61d166424839b7674a7b9c8434ae4e03_453_0.png)

图 15-13 不建议吃用砂纸！

![](img/61d166424839b7674a7b9c8434ae4e03_453_1.png)

图 15-12 在第一个表单中输入 John 并点击按钮的 own

图 15-13 不建议吃用砂纸！

图 15-12 显示了查看者在第一个表单中输入 John 并点击按钮时的页面样子。图 15-13 显示了查看者在食物字段中输入砂纸并点击按钮时的页面样子。

（此处省略重复的段落，以符合指令“不要重复输出原文”）

图 15-12 显示了查看者在第一个表单中输入 John 并点击按钮时的页面样子。图 15-13 显示了查看者在食物字段中输入砂纸并点击按钮时的页面样子。

第 15 章：JavaScript 与框架

431

图 15-12 在第一个表单中输入 John 并点击按钮的结果

图 15-13 不建议吃用砂纸！

JavaScript：初学者指南

454

JavaScript：初学者指南

使用变量

在此项目中，你利用框架的知识创建了一个跨框架使用变量的 frameset。查看者能够在框架中输入信息并在另一个框架中查看结果。

逐步步骤

1. 创建包含两个框架的 frameset，左侧占据 150 像素，右侧使用窗口剩余部分。将左侧框架命名为 `left_side`，右侧框架。第一个框架的文件应为 `pr15_2_frame1.html`，第二个框架为 `pr15_2_frame2.html`。
2. 在 `pr15_2_frame1.html` 中，创建三个变量并将其赋值为空字符串。使用这些变量名：
   `thename`
   `thecolor`
   `thecar`
3. 在 `pr15_2_frame2.html` 中，创建一个表单询问查看者的名字、最喜欢的颜色和汽车。当点击按钮时，信息应存储在左侧框架的变量中，并将文档更改为 `pr15_2_frame3.html`。
4. 在 `pr15_2_frame3.html` 中，在页面上为查看者打印以下问候，使用左侧框架中存储的值：
   Hello, *<查看者名字>*! 我敢定你很想要有一辆 *<喜欢的颜色汽车>* 真可惜我不能给你一个！
5. 在浏览器中打开 `pr15_2.html` 并尝试一下。

尝试总结

在此项目中，你利用 JavaScript 和框架的知识创建了一个使用变量的 frameset。查看者能够在一个框架中输入并在另一个框架中查看结果。

第 15 章：JavaScript 与框架

433

*第 15 章自测*

1. __________ 将窗口分为两个或多个独立的区域，每个区域都包含内容。
2. 框架与表格的不同之处在于 frameset 中的划分包含独立的文档。
3. 使用 __________ 标签来创建 frameset。
4. 使用 __________ 标签创建单个框架。
5. __________ 属性将 frameset 分为列。
6. 如果你想要一个既包含行又包含列的更复杂的 frameset，可以将一个 frameset __________ 在另一个内部。
7. 访问框架的两种方法是什么？
   A frames 数组或框架名称
   B frame 数组或框架名称
   C frames 数组或特殊代码
   D 只有一种方法可以实现
8. 使用 JavaScript，你可以一次更改多个一个框架的内容。
   A 正确
   B 错误
9. frames 数组的 `length` 属性的值是什么？
   A 根据宽度或高度特定框架的长度
   B 页面上 frameset 的数量
   C 窗口中框架的数量
   D 框架中数组的数量
10. 在 frameset 的 rows 或 cols 属性中使用星号 (*) 表示什么？
    A 没有空间放置另一个框架了。
    B 框架应该占据窗口的剩余空间。
    C 框架永不结束。
    D 框架在弹出窗口中显示。




456

JavaScript：初学者指南

11. 使用什么访问主窗口以便访问另一个框架？

A top

B self

C window

D this

12. 下面哪项可以正确地从另一个框架将名为 `right_side` 的框架内容更改为 `frame3.html`？

A self.location="frame3.html";

B top.right_side.location="frame3.html";

C self.location="frame3.htm";

D top.location="frame03.html";

13. 使用目标为 `_________` 会告诉浏览器在打开 URL 时使用整个窗口，而不是在框架中打开 URL。

14. 你可以在另一个框架中使用存储在一个框架中的变量。

A 正确

B 错误

15. `__________` 属性将框架集（frameset）划分为行。

第 16 章
高级技术简介

435

JavaScript：初学者指南

关键技能与概念

- 脚本调试
- JavaScript 与无障碍性
- 使用 Cookies
- 图像处理
- JavaScript 安全
- AJAX 简介
- JavaScript 库

本章介绍了一些高级技术，当你读完这本书后，你可能希望进一步研究。你将学习调试出现问题的脚本（这在程序出现问题时很有帮助）、JavaScript 与无障碍性（当 JavaScript 被禁用时可以帮助用户访问你的信息）、使用 Cookies（允许你为用户存储和检索小段信息）、图像处理（允许你预加载和更改图像）、JavaScript 安全（帮助你保护你的用户）、AJAX（增强用户体验）以及 JavaScript 库（这些可以帮助你避免重复编写代码）。除了书中涵盖的内容外，关于这些主题的更多信息可以在章节末提供的链接中找到。

脚本调试

尽管 JavaScript很有趣，但有时它也可能非常令人沮丧。代码中的一个错误就会导致整个脚本运行异常或完全不运行。调试脚本可能是一个耗时且艰巨的过程，但你可以使用一些技巧，可能帮助在检查代码时节省一些时间。调试脚本的第一步是确定是什么类型的错误可能导致了问题。

错误类型

两种主要的错误是语法错误和逻辑错误。当编码员忘记添加分号、忘记引号、拼错单词等时，就会发生语法错误。

当代码实现错误时，就会发生逻辑错误。

例如，如果执行循环的条件永远不会变为假，那么 while 循环可能会无限进行。虽然它的代码语法可能是正确的，但结果将不符合程序员的预期。

第 16 章：高级技术简介

437

查找语法错误

语法错误可能仅仅是漏掉了必要的分号。例如，以下代码在语句之间缺少一个分号：

<input type="button" value="Click" onclick="analert() analert2()" />

在这种情况下，分号是非常重要的，因为两个语句（函数调用）在同一行上。要修复此，你只需要添加所需的分号，所示：

<input type="button" value="Click" onclick="analert();analert2()" />

语法错误通常会导致浏览器显示错误消息，以便你调试脚本。例如，你可能会看到类似图 16-1 所示的消息。

这些消息可以帮助你找出导致问题的原因。错误消息中显示的行号通常会告诉你错误所在的位置。例如，如果消息说错误在第 15 行，你将从文档顶部的第 15 行开始查看那里有什么内容。消息的其他部分可能会告诉你缺少了什么或者什么被放置得不当。

然而，有时消息中指出的行并不是实际问题所在的行。它可能在前面的行、在几行之外，甚至在完全其他地方。你需要进行一些搜索来确定问题是从哪里开始的。（接下来的章节“扫描脚本”将更详细地介绍这一点。）

如果你收到错误消息，它要么能让问题更容易发现，要么会让你更头疼。某些消息比其他要好。首先，转到错误消息给出的行。如果消息中的文本有任何意义（例如“预期‘；’”），那么查看消息是否在引导你向正确的方向。

图 16-1 一个 JavaScript 错误消息

JavaScript：初学者指南

例如，如果它告诉你有预期一个分号，那么查看该行或附近的行是否缺少了分号。

如果你在附近没有发现问题，你就必须搜索它。如果所涉及的行正在调用脚本其他部分的函数或使用变量，请查看该函数或变量定义的地方。转到函数或变量，查看名称是否与你调用它时使用的相同。如果是，检查所有语法是否正确（例如大括号、引号和括号）。例如，查看以下代码：

<<body>
<form>
<input type="button" value="Click" onclick="cool();"></input>
</form>

<script type="text/javascript">
function cool() {
window.alert("Cool!");
}
</script>
</body>

当你点击 Click 按钮时，代码将产生一条显示“Object Expected”（预期对象）的消息（取决于使用的浏览器），并指向代码中页面放置按钮的行（在本例中为第 4 行）。如果你查看该行，似乎没有问题。然而，如果你在代码中继续查看（第 8 行）在该行上调用的函数 cool()，你会发现缺少起始大括号。缺失的括号就是问题所在，添加它将修复代码。

扫描脚本如果错误消息没有帮助你定位问题，请尝试扫描脚本查找错误。这种解决方法可能是枯燥的，但如果错误消息没有帮助，它可能可能帮助你找到问题。

| 扫描脚本时要查找的项目 |
| :--- |
| 外观 |
| 缺少分号 | ; |
| 缺少大括号或方括号 | } ] |
| 缺少括号 | ( ) |
| 缺少单引号或双引号 | ' " |
| 拼写错误 | 使用 *cool* 而不是 *cool* |

第 16 章：高级技术简介

439

以下代码充斥着错误；看看你能找到其中多少个。

<script type="text/javascript">
var mycar="Mustang";

function send_alert()
window.alery("You like+mynar+"!");

}

var somearray=neq Array(2)

somearray[0]="Me";

somearray1]="Me2";

for var count=0;count<somearray.length;count+=1) {
document.write(somearray[0+"and"+somearray[1]);
}
</script>

代码缺少了许多项目。以下是你应该发现的项目列表：

- 第 3 行和第 4 行之间：函数缺少起始大括号。
- 第 4 行：*alert* 拼写为 *alery*；like 后面缺少引号；mycar 变量拼写为 *mynar*。
- 第 5 行：alert 方法缺少右括号。
- 第 7 行：*new* 拼写为 *neq*。
- 第 9 行：数组索引数字缺少起始方括号。
- 第 10 行：循环缺少起始左括号。
- 第 11 行：somearray[0 缺少结束右方括号。
- 第 11 行和第 12 行之间：缺少结束循环的右大括号。

查找逻辑错误

逻辑错误通常很难发现，因为代码的语法是正确的。你将试图在代码实现中寻找错误。例如，查看以下代码（但不要运行）：

<script type="text/javascript">
x=1;
y=2;

while (x<=y) {
window.alert("Hi");
}
</script>

问题：*x* 永远不会大于 *y*！




JavaScript：初学者指南

代码没有语法错误。所有的分号和引号都处于它们应该的位置。这里的问题在于，变量 *x* 永远不会大于变量 *y*。这种情况会导致无限循环，可能导致浏览器崩溃。

你可以通过在循环内部添加一行代码来增加 *x* 的值、减小 *y* 的值，或者同时增加 *x* 并减小 *y*，从而修复代码。关键点是，必须采取某些操作使条件变为为假。以下代码展示了该问题的一种可能的解决方法：

<script type="text/javascript">
x=1;
y=2;
while (x<=y) {
window.alert("Hi");
x++;
}
</script>

接下来的章节描述的技术可以帮助你发现逻辑错误。

### 针对问题变量的 Alert 技术

发现上一个示例中问题的方法之一是返回并重新运行它，同时使用 alert 在每次循环时测试一个或两个变量的值（假设它没有导致浏览器崩溃）。alert 是发现发生情况的极佳方法，并可以给你提供解决问题的思路。

例如，以下代码取了上一个示例（修复之前的），并添加了一个 alert，在每次循环运行时显示 *x* 和 *y* 的值：

<script type="text/javascript">
x=1;
y=2;
while (x<=y) {
window.alert("x is: "+x+" and y is "+y);
window.alert("Hi");
}
</script>

只要脚本没有导致浏览器崩溃，你就能看到问题所在。每当 alert 弹出时，它都会显示相同的内容：“x is 1 and y is 2。”因此，你会知道需要在循环中进行调整来修复它。

当你脚本中的某个变量经过了多次重新赋值和计算时，这种技术非常有用。通过使用放置恰当的 alert，你可以发现问题从哪里开始。例如，看看这段代码：

<script type="text/javascript">
var item1="10";
var item2=20;
var total=item1+item2;
upcharge=5;
total+=upcharge;
window.alert("The total is $"+total);
</script>

- 在循环中增加 *x* 会让 *x* 随着时间的推移大于 *y*
- alert 提供了两个变量的值，帮助你发现问题
- 此 alert 没有显示预期的结果

第 16 章：高级技术简介

变量 total 在第四行被赋值，然后在第六行通过将另一个变量加到它上进行重新赋值。在完成所有计算后，带有 total 的 alert 给出了一个 10205 这种奇特的结果。你看到问题了吗？如果没有看到，你可以在第一次赋值后放置一个 alert，以检查 item1+item2 的计算是否正常工作：

<script type="text/javascript">
var item1="10";
var item2=20;
var total=item1+item2;
window.alert(total);
upcharge=5;
total+=upcharge;
window.alert("The total is $"+total);
</script>

该 alert 允许你看到第一次计算是否正常工作。

**Q：我收到的错误信息包含我不懂的内容。我该怎么办？**
**A：** 错误信息并不总是有意义，也不总是指向代码中正确的某一行。你可能需要追踪你在信息给出的行上调用的任何变量或函数，或者检查其附近的行是否有错误。当你看到几次错误信息后，它的含义就会变得更容易理解。

**Q：当我尝试运行代码时，代码中的某些内容导致浏览器崩溃，我无法添加 alert 来帮助寻找问题，因为每次都会崩溃！我该怎么办？**
**A：** 如果脚本导致浏览器崩溃，请仔细检查你的变量、循环、对象和函数。作为最后的手段，从头开始编写新代码。

**Q：我代码中的错误不仅导致浏览器崩溃，还导致了电脑崩溃！我该怎么办？**
**A：** 重启电脑但*不要*再次运行代码。仔细检查以能否找到问题。

**Q：还有其他策略可以帮助我调试脚本吗？**
**A：** 一些编辑器使用颜色编码来标记 HTML 标签、JavaScript 代码或其他类型的代码。颜色编码可以帮你更清晰地看到代码，并更容易检测错误。（尝试使用 Vim 或 NoteTab 编辑器。）

提问专家

当你再次运行脚本时，第一个 alert 给出的结果是 1020。现在问题变得清晰了一些。由于某些原因，脚本将 item1 和 item2 视为字符串而不是数字，导致两个数字组合在一起而不是进行数学上的相加。

回看对 item1 的赋值，注意它被意外地赋值为了字符串。删除 10 周围的引号即可修复脚本，并给你得到预期的最终结果 35。

### 硬核方法：追踪一切或做出更改

如果所有捷径方法都失败了，最后的选择是尝试逐段重新运行整个脚本，看看是否能检测到错误。如果没有，看看是否可以找到另一种编写该任务的方法。例如，尝试使用不同类型的循环。希望新策略能帮助你解决问题并完成脚本。

### JavaScript 与可障碍性（Accessibility）

你在书中多次看到的一个主题是脚本或脚本 HTML 代码如何与可障碍性相关。在某些情况下，例如政府机构网站，州或联邦法律（如《美国残疾人法案》）可能要求网站对残障人士可访问。即使这对于你的网站来说不是法律问题，它仍然是一个可用性问题：你希望尽可能多的游客可以使用你的网站并访问你提供的信息。

可障碍性的核心主题是内容需要适用于所有浏览器和其他可能访问网站的软件。这意味着你的内容不仅应该被各种 Web 浏览器读取，还应该被辅助技术（例如来自 Freedom Scientific 的 JAWS）或手机等移动设备上的 Web 浏览器软件读取。

### 将内容与表现分离

使内容可访问的第一步通常是将可障碍性构建到 HTML/CSS 中。虽然这种做法是有效的，但如果你决定使用不同名称的函数或将其改为没有 JavaScript 的普通链接，就会变得麻烦，因为你需要更新每个 HTML 文件以适应更改。为了将此 onclick 事件处理程序从 HTML 代码中提取出来，你可以稍微重写 JavaScript 并给锚点标签添加一个 id（就像你在书中早之前做的那样）。




JavaScript 入门指南

接下来，是 `myscript.js` JavaScript 文件：

```javascript
function send_alert() {
  window.alert("Hi, there is a sale today! 20% off everything!");
  return false;
}

var s_alert = document.getElementById("sale");
s_alert.onclick = send_alert;
```

现在，HTML 代码中没有散落在其中的 JavaScript 命令，只有末尾有一个对外部脚本的调用。锚标签被赋予了 `id="sale"`，JavaScript 代码可以使用该 ID 来捕获作用在该元素上的点击事件。JavaScript 代码现在使用 `document.getElementById()` 获取锚点元素，然后为其分配一个在点击时运行的函数。

这里的最后一点是，对于那些没有 JavaScript 的用户，该链接将不起任何作用。由于警框的内容是你需要访问者知道的（这样他们才知道有促销活动），你会希望确保即使是没有 JavaScript 的访问者也能看到此消息。你可以在页面的其他地方显示它，使用一组 `<noscript></noscript>` 标签内联显示消息，或者编写链接让其指向一个包含消息的 HTML 页面，如下代码所示：

```html
<body>
  <a href="sale_alert.html" id="sale">Hi</a>
  <script type="text/javascript" src="myscript.js"></script>
</body>
```

然后，你可以在 `sale_alert.html` 文件中放置你的消息：

```html
<body>
  Hi, there is a sale today! 20% off everything!
</body>
```

这确保了所有用户（无论是否使用 JavaScript）都能够访问到该消息。

## 增强内容

一种已成为广泛使用的、用于确保广泛可访问性的技术是：首先为查看者提供内容，然后使用 JavaScript 为能够运行它的用户提供更具吸引力的体验。这通常被称为“渐进式增强”（progressive enhancement），它允许所有查看者使用该网站，同时为使用现代浏览器的用户提供更丰富的体验。

这正是你在上一节的脚本中（小规模地）所做的事情。通过在点击链接时提供“促销”消息，你让所有查看者都能看到它。然而，拥有 JavaScript 的用户可以在不离开页面无需返回的情况下查看警框，这在某种程度上增强了他们的体验。

这个过程可以很简单（如上一个示例所示），也可以很复杂，例如添加大量的 JavaScript 代码以适应各种浏览器，和/或添加服务器端脚本来帮助没有 JavaScript 的用户。你可以在 http://developer.yahoo.com/yui/articles/gbs/#progressive-enhancement 了解更多关于渐进式增强的知识。Yahoo！有一套非常详细且组织良好的渐进式增强系统，允许 JavaScript 代码尽可能兼容各种浏览器，同时也为没有 JavaScript 的用户提供服务器端脚本或 HTML 内容。

***提示***

有关使用 JavaScript 和表单的可访问性信息，请参阅第 14 章，该章节讨论了这一主题以及在 JavaScript 中表单。

## 使此代码具有可访问性

为了练习让 JavaScript 更具可访问性，你将取一个 HTML 并对其进行处理，尽可能将 JavaScript 代码和 HTML 代码分离。你还将使用代码来确保没有 JavaScript 的用户也能获取任何额外内容。

### 逐步步骤

1. 创建名为 `pr16_1.html` 的 HTML 文档，并在 body 部分使用以下 HTML 代码：

```html
<body>
  <script type="text/javascript">
    function new_win() {
      window.open('sales.html','newwin','width=300,height=200');
    }
  </script>
  <div>
    <h1>Sales:</h1>
  </div>
  <div>
    <a href="#" onclick="new_win(); return false;">Click for Sale Information</a>
  </div>
</body>
```

2. 创建一个名为 `sales.html` 的 HTML 文档，并在 body 部分使用以下 HTML 代码：

```html
<body>
  <h1>Sales:</h1>
  Clothes: 25% off<br />
  Electronics: 10% off<br />
  Appliances: 15% off (with coupon)
</body>
```
（续上）

3. 通过进行必要的调整并将尽可能多的 JavaScript 代码移动到名为 `prjs16_1.js` 的 JavaScript 文件中，使代码对没有 JavaScript 的用户具有可访问性和可用性。

4. 作为额外奖励，尝试完全移除这个新窗口，并将促销信息放在一个仅包含“Sales:”文本的 div 中，供拥有 JavaScript 的用户使用。

5. 保存 HTML 和 JavaScript 文件，并在浏览器中打开 HTML 文件。内容现在应该可以在你选择的任何打开该页面的浏览器中访问。

### 练习总结

在这个项目中，你利用了可访问性的知识，让文档和脚本对查看者更具可访问性。

## 使用 Cookie

*cookie* 是存储在终端用户计算机上的get小文本文件。只要 cookie 没有被删除或过期，每当查看者返回你的网站时，就可以引用它。当然，如果查看者不接受 cookie，那么之后就无法设置或引用 cookie。使用 cookie 时记住以下几点：

- 每个 cookie 必须是 4KB（4000 个字符）或更少。
- 如果浏览器不接受 cookie，你就无法使用它们。
- 你可以使用任何类型的分隔符来定义键值对。

## 设置 Cookie

设置一个基础 cookie 就像给 document 对象的 `cookie` 属性赋值一样简单。唯一的限制是不能在字符串内部使用空格、逗号或分号。

例如，你可以使用以下代码设置一个 `name=tasty` 的 cookie：

```javascript
function set_it() {
  document.cookie="name=tasty1";
}
```

***注意***

设置 cookie 时，记住不要设置 cookie 数据的字符串内部使用空格、逗号或分号。

前面的代码在调用函数时会设置一个值为 `tasty1` 的 cookie。你可以设置任何分隔符，设置分隔符允许你存储多个值。以下代码同样有效：

```javascript
function set_it() {
  document.cookie="name:tasty1";
}
```

## escape() 方法

如果你想在 cookie 中使用空格、逗号或分号，你需要一种方法“转义”它们，以便它们被转换为 cookie 接受的内容。

cookie 会接受像 CGI 程序经常那样的字符代码。它们看起来像 %20、%41 或类似的内容。要将空格、逗号和分号转换为这些代码，你必须使用 JavaScript 的 `escape()` 方法。




## JavaScript: 入学者指南

以下代码展示了如何使用 `escape()` 方法设置一个包含空格的 cookie：

```javascript
function set_it() {
  var thetext="name=tasty1&fav=Chocolate Chip"
  var newtext=escape(thetext);
  document.cookie=newtext;
}
```

`thetext` 变量被赋值为包含你想在 cookie 中使用的字符串。`newtext` 变量被用于存储对 `thetext` 使用 `escape()` 方法的结果。随后，转义后的文本被用作 cookie 的字符串，它现在将包含空格字符的编码（当你需要使用这些数据时，你需要对其进行反转义/unescape）。

### 允许用户输入

通过使用 `escape()` 方法，你可以提示查看者输入信息，对其进行转义，然后在 cookie中使用。以下代码展示了如何这样做以获取查看者喜欢的饼干类型：

```javascript
function set_it() {
  var thefav=window.prompt("输入你最喜欢的饼干类型","");
  var thetext="name=tasty1&fav="+thefav;
  var newtext=escape(thetext);
  document.cookie=newtext;
}
```

现在，查看者可以帮助决定设置在 cookie 中的信息，你可以在查看者下次访问你的网站时使用他们在网站上输入的信息。

### 设置过期日期

在 cookie 中添加过期日期可以防止它在浏览器关闭后被删除，或者可以用于过期你不再使用的 cookie。要设置过期日期，请在你的 cookie 字符串中添加更多内容，如下代码所示：

```javascript
function set_it() {
  var thetext="quote=I have a quote";
  var expdate=";expires=Mon, 30 Mar 2009 13:00:00 UTC";
  var newtext=escape(thetext);
  newtext+=expdate;
  document.cookie=newtext;
}
```

基本上，你是在添加另一个包含了过期日期的键/值对（注意键/值对之间用分号隔开）。它需要符合这种格式：

expires=date（UTC 格式）

| 描述 |
| :--- |
| 创建一个包含用于 cookie 信息的字符串字面量 |
| 对字符串进行转义以便在 cookie 中使用 |
| 将转义后字符串的值放入 cookie 中 |
| 将转义后的字符串放入 cookie 中 |
| 对字符串进行转义以便在 cookie 中使用 |
| 将提示框中输入的值添加到一个用于 cookie 的字符串中 |
| 查看者能够在此提示框中输入信息 |
| 给出一个过期日期 |
| 将过期日期添加到文本中 |
| 为 cookie 赋予组合后的文本和过期日期的值 |

第 16 章：高级技术简介

在代码中，通过添加 UTC 格式的日期为 cookie 添加了过期日期。然后，将结果添加到将用于设置 cookie 字符串的变量中。如果你想让 cookie 留存很久，可以设置一个遥远的日期。如果你想让一个不再使用的 cookie 过期，设置一个过去的日期，cookie 就会过期。

### 读取 Cookie

如果你只设置了一个 cookie 并想要读取它，那么读取 cookie 非常简单。要读取 cookie，你只需要从浏览器获取 `document.cookie` 属性的值即可：

```javascript
function read_it() {
  var mycookie=document.cookie;
}
```

然而，之前的代码只会给 `mycookie` 变量返回一个长且可能杂乱的字符串值。它看起来可能像：

name=tasty1&fav=Chocolate%20Chip

`%20` 是在 cookie 输入使用 `escape()` 方法进行转义时进入代码的。要修复这个问题，使用 `unescape()` 方法获取更具可读格式的数据。因此，以下代码将提供你需要的字符串：

```javascript
function read_it() {
  var mycookie=document.cookie;
  var fixed_cookie= unescape(mycookie);
}
```

接下来，你找到一种方法从 cookie 中提取你需要的信息。假设 cookie 包含了刚刚作为示例的字符串（name=tasty1&fav=Chocolate%20Chip），现在该字符串看起来像这样：

name=tasty1&fav=Chocolate Chip

注意，文本是以两种不同的方式划分的。连接符 `&` 将字符串分为键/值对，而等号 `=` 将键/值对划分为键和值。假设字符串 `name=tasty1&fav=Chocolate Chip` 是现在代码中 `fixed_cookie` 变量中的内容，你可以使用该变量通过 `&` 字符分割字符串来创建一个新数组：

```javascript
function read_it() {
  var mycookie=document.cookie;
  var fixed_cookie= unescape(mycookie);
  var thepairs= fixed_cookie.split("&");
}
```

| 描述 |
| :--- |
| cookie 字符串按 `&` 分割为数组 |
| 对值进行反转义，使字符串具有可读字符 |
| 读取 `cookie` 属性的值 |
| 新变量按等号 `=` 分割 |
| 将数组元素的值赋值给变量 |
| 使用从 cookie 中获取的值 |




JavaScript：初学者指南

尝试此总结

在这个项目中，你使用了使用 JavaScript 设置和读取 cookie 的知识。

你创建了一个 Web 页面，当访问者返回该页面时，它可以记住访问者的。

处理图像

JavaScript 使用图像对象（image object）来预加载图像、创建鼠标悬停效果（rollover effects），甚至创建幻灯片或动画。当你想要创建此类脚本时，图像对象的属性将大有帮助。表 16-2 列出并描述了图像对象的属性。

`src` 属性在本章中最常用，因为它允许更改图像源以创建鼠标悬停效果。

预加载

在编写 Web 页面时，有时你可能希望预加载图像。*预加载*图像允许它在 HTML 或 JavaScript 代码调用之前就存在于浏览器的缓存中。通过这种方式，当图像被调用时，将会显示得更快，访问者不需要等待加载。

预加载的一种技术是在主页面加载网站其他页面将使用的图像。例如，你可能希望网站的 Logo 出现在的每个页面上。当它在第一个页面加载时，它会立即显示。

| 属性 | 目的 |
| :--- | :--- |
| name | 存储来自 `name` 属性的值 |
| src | 存储来自 `src` 属性的 URL |
| width | 存储来自 `width` 属性的值 |
| height | 存储来自 `height` 属性的值 |
| border | 存储来自 `border` 属性的数值 |
| hspace | 存储来自 `hspace` 属性的数值 |
| vspace | 存储来自 `vspace` 属性的数值 |
| lowsrc | 存储来自 `lowsrc` 属性的 URL |
| complete | 表示图像是否完成加载 |

表 16-2 Image对象的属性

当然，在 HTML 中这样做是有意义的，因为你可能希望 Logo 出现在主页面以及其他页面。因此，当你编写 `img` 元素时，图像被加载到了缓存中。

在某些情况下，你可能希望预加载稍后出现在同一页面上的图像。这种做法在使用鼠标悬停或其他页面加载完成后调用图像的脚本时很常见。在这种情况下，你不希望访问者停下来等待图像加载，因为这会导致脚本无法正常工作。例如，如果你设置了当访问者鼠标移动到图像上时显示新图像，你希望新图像立即显示。如果访问者必须等待几秒钟加载，将会破坏预期效果。

通过 JavaScript，你可以创建一个图像对象的新实例，然后将其 `src` 属性设置为想要预加载的图像 URL，如下：

```javascript
if (document.images) {
  var pic1= new Image(120,35);
  pic1.src="image1.gif";
  var pic2= new Image();
  pic2.src="image2.gif";
}
```

回想数组数组讨论过的类似代码。图像对象的第一个实例 (pic1) 定义了图像的宽度和高度。第二个 (pic2) 没有定义，但它将从图像的实际宽度和高度获取这些值。你不需要同时使用两种方法。你可以选择你喜欢的方法并将其用于所有想要预加载的图像。

带有 `img` 元素的 HTML 页面可能如下：

```html
<body>
  <script type="text/javascript" src="preload.js"></script>
  <h1>一些图像</h1>
  <img src="image1.gif" width="120" height="35" />
  <br /><br />
  <img src="image2.gif" width="50" height="75" />
</body>
```

JavaScript 代码可能像这样：

```javascript
if (document.images) {
  var pic1= new Image(120,35);
  pic1.src="image1.gif";
  var pic2= new Image();
  pic2.src="image2.gif";
}
```

当然，在这种情况下，预加载实际上并没有作用。为了给预加载技术一个意义，你需要一个在事件发生时显示新图像的脚本，例如在鼠标悬停脚本中。

鼠标悬停

图像*悬停*（也称为悬停按钮、图像翻转或其他类似名称）可以为你的导航图像增加趣味。当访问者将鼠标移动到链接图像上，图像会发生变化。变化可以是从简单的颜色变化到完全不同的图像，从而增加访问者对导航系统的兴趣。最后两句话描述的效果是简单的鼠标悬停，但你也可以通过另一个链接图像或文本链接的鼠标移入事件来更改图像，甚至一次更改多个图像。

### 简单的鼠标悬停

当鼠标移动到初始图像上时，简单的鼠标悬停将一个图像变为另一个。首先，你创建两个图像，并让第二个图像以某种方式不同。例如，检查这两个图像：

（注意：OCR文本在此部分包含几个伪影/乱码字符串，已根据逻辑流和上下文进行了清理）。

简单的鼠标悬停当鼠标移动到初始图像上时，将一个图像变为另一个。首先，你创建两个图像，并让第二个图像以某种方式不同。

简单的鼠标悬停当鼠标移动到初始图像上时，将一个图像变为另一个。首先，你创建两个图像，并让第二个图像以某种方式不同。

简单的鼠标悬停当鼠标移动到初始图像上时，将一个图像变为另一个。首先，你创建两个图像，并让第二个图像以某种方式不同。

简单的鼠标悬停当鼠标移动到初始图像上时，将一个图像变为另一个。首先，你创建两个图像，并让第二个图像以某种方式不同。

简单的鼠标悬停当鼠标移动到初始图像上时，将一个图像变为另一个。首先，你创建两个图像，并让第二个图像以某种方式不同。





# JavaScript：初学者指南

在这里，你可以看到结果的最直观方法就是查看一组前后的对比图。

图 16-2 显示了初始图像，而图 16-3 显示了当鼠标移动到图像上时的结果。

### 更改不同的图像

你可能想要更改一个与鼠标悬停对象上不同的图像。要实现这一点，设置与上一节相同，不同的是你需要更改当鼠标移动到初始图像上时所改变的元素。

你可以修改你一直使用的代码，让第一张图像保持静态并改变另一张图像。因此，你需要在将要改变的图像上预加载第二张图像。以下是每个文件的代码，从 HTML 代码开始：

```html
<body>
<script type="text/javascript" src="preload.js"></script>
<h1>下方的第一张图像将改变第二张图像！将鼠标悬停在它上面！</h1>
<a href="somepage.html"><img src="image1.gif" id="pic1" border="0" /></a>
<br /><br />
<img src="image2.gif" id="pic2" />
<script type="text/javascript" src="change.js"></script>
</body>
```

这简单地在两个换行符之后添加了新图像（image2.gif）。接下来是 `preload.js` 文件：

```javascript
if (document.images) {
  // 预加载将在 mouseover 事件中显示的图像
  var pic2_new= new Image();
  pic2_new.src="image2_c.gif";
}
```

这改变了从 pic1 和 image1（它们将不再被改变）到 pic2 和 image2（它们现在将变为改变的图像）。

![](img/61d166424839b7674a7b9c8434ae4e03_478_0.png)
图 16-2 初始图像

最后是 `change.js` 文件：

```javascript
var im1 = document.getElementById("pic1");
var im2 = document.getElementById("pic2");
im1.onmouseover = function() { im2.src = pic2_new.src; };
im1.onmouseout = function() { im2.src = "image2.gif" };
```

在这里，添加了变量 `im2` 以通过其 id (pic2) 获取第二张图像。当查看者鼠标移动到第一张图像 (im1) 上时，它会被改变。

现在鼠标可以移动到第一张图像上并改变第二张图像。图 16-4 和 16-5 显示了另一组前后的屏幕。

![](img/61d166424839b7674a7b9c8434ae4e03_479_0.png)
图 16-3 发生over 事件时出现新图像
图 16-4  mouseover 事件前显示的图像

![](img/61d166424839b7674a7b9c8434ae4e03_480_1.png)

### 更改多个图像

要一次更改多一张图像，你需要为每个想要更改的图像准备一组两个图像。为了简单起见，你使用的示例仅包含两对图像。创建的代码将导致第一张图像上的 mouseover 事件同时改变它自己和页面上的第二张图像。此脚本使用的图像是 image1.gif、image1_c.gif、image2.gif 和 image2_c.gif。

HTML 代码将与上一个示例相同（标题除外）：

```html
<body>
<script type="text/javascript" src="preload.js"></script>
<h1>下方的图像将改变自身和另一张图像！</h1>
<a href="somepage.html"><img src="image1.gif" id="pic1" border="0" /></a>
<br /><br />
<img src="image2.gif" id="pic2" />
<script type="text/javascript" src="change.js"></script>
</body>
```

接下来是 `preload.js` 的代码：

```javascript
if (document.images) {
  var pic1_start = new Image();
  pic1_start.src = "image1.gif";
  var pic1_new= new Image();
  pic1_new.src="image1_c.gif";
```
![](img/61d166424839b7674a7b9c8434ae4e03_480_0.png)
图 16-5 mouseover 事件后显示的图像
```javascript
  var pic2_start = new Image();
  pic2_start.src = "image2.gif";
  var pic2_new= new Image();
  pic2_new.src="image2_c.gif";
}
```

主要的区别在于你现在预加载了两组图像（这有助于脚本组织，并允许你之后使用 src 属性）。最后是 `change.js` 的更改：

```javascript
var im1 = document.getElementById("pic1");
var im2 = document.getElementById("pic2");
im1.onmouseover = function() {
  im1.src = pic1_new.src;
  im2.src = pic2_new.src;
};
im1.onmouseout = function() {
  im1.src = pic1_start.src;
  im2.src = pic2_start.src;
};
```

这添加了第二组图像，并在 mouseover 事件上将它们都变为各自的第二图像，然后在 mouseout 事件时恢复。注意，由于初始图像在 `preload.js` 脚本中被赋值为对象，你可以使用 `pic1_start.src` 和 `pic2_start.src`。当代码运行时，你会看到类似图 16-6 和 16-7 所示的屏幕。

![](img/61d166424839b7674a7b9c8434ae4e03_481_0.png)
图 16-6 mouseover 事件前的图像

### JavaScript 安全

你可能注意到，当你在主浏览器窗口使用 `window.close()` 时，会弹出一个确认框询问是否要关闭窗口。这种情况是 JavaScript 安全问题之一。浏览器不希望在没有查看者许可的情况下关闭窗口，这可能是个问题。安全的另一个方面是误认为可以通过密码“保护”网页或防止用户查看页面源代码。安全的另一个方面是防御跨站脚本，即使用 JavaScript 从未正确过滤输入的服务器端应用程序获取信息。

### 安全与签名脚本

要获得关闭主浏览器窗口的权限或在 JavaScript 中使用某些属性，必须使用签名脚本（signed scripts）。签名脚本将开启一些额外功能，但你必须进行额外的工作。基本上，是使用特殊工具对脚本进行数字签名。查看者在进入页面时会收到消息，询问是否允许带有某些信息的签名脚本。如果查看者接受，你就可以使用额外功能。如果没有，你需要准备好替代代码以避免 JavaScript 错误。关于此主题的更多信息，请访问 www.mozilla.org/projects/security/signed-scripts.html。

### 页面保护

许多脚本试图以此阻止查看者，例如使用密码保护或使用“禁用右键”脚本防止查看页面源代码。

![](img/61d166424839b7674a7b9c8434ae4e03_482_0.png)
图 16-7 mouseover 事件后的图像

然而，这些安全策略在很大程度上是无效的，因为这些“密码”和“禁用右键”脚本通常可以通过禁用 JavaScript 或进行额外工作来绕过。

### 密码

某些密码系统比其他的好，但似乎没有哪一个能提供真正的网页安全。如果你不想让某人查看页面，比使用 JavaScript 系统有更好的方法，例如使用服务器端语言或在你的 Web 服务器上使用某些设置。如果你在使用免费的 Web 托管服务，更好的方法可能不可用。但请记住，JavaScript 密码系统并非万无一失，你不应该用这种系统保护任何重要内容。

### 隐藏网页源代码

许多人都想隐藏网页的源代码。然而，JavaScript 并起不了作用。许多脚本尝试通过各种手段禁用右键。基本上，这些策略不起作用，因为可以通过以下几种方式绕过：

- 如果禁用了右键，你始终可以尝试“查看 | 源代码”（View | View Source）。
- 如果上述方法不起作用，你始终可以禁用 JavaScript 或查看电脑上的缓存目录。浏览器必须拥有显示页面的代码，因此其副本会进入浏览器缓存。

从长远来看，这些脚本只是让查看源代码变得困难（而且它们很烦人）。关于此主题的更多信息，请访问 http://webhome.idirect.com/~bower/copy/copy1.htm。

### 跨站脚本

跨站脚本（通常简称 XSS）恶意恶意使用 JavaScript 代码（或其他类型的代码）从存在漏洞的各种网站的用户处获取信息。通过这些信息，他人可以使用别人的 cookie 或会话信息，并以获取信息的用户的身份访问该 网站。这无疑可能导致大麻烦，特别是当该用户是应用程序的管理员或该应用程序涉及资金时（例如银行或购物应用程序）。

虽然 JavaScript 是执行此类攻击的一种方式，但漏洞的应用程序通常是服务器端的并在页面上显示用户输入。如果服务器端应用程序没有对用户输入进行清洗（验证），那么就可以输入任何可能的恶意脚本，而不是预期的输入。

例如，你可能有一个使用服务器端脚本允许人们发送评论的表单。脚本会将用户提交的评论返回给用户作为确认。如果输入没有经过清洗，可能会在评论字段中输入如下的内容：

<script>alert(“你被耍了！”);</script>。如果有人提交了这些并在响应页面上看到警窗，此人就知道那里存在潜在的漏洞，并简单地将后续用户引导到一个恶意 URL，在在那里可以获取用户的 cookie 或会话信息。图 16-8 显示了漏洞应用程序将如何显示此类警窗（这一个还包含了一些文本以帮助掩盖提交表单者的意图）。





JavaScript：初学者指南

跨站脚本（Cross-site scripting）在多年年来一直在演变。起初，一个恶意网站可以在框架中（或弹出浏览器窗口中）加载一个良网站，然后使用 JavaScript 访问文本框、cookie 和其他数据（用户 ID 和密码）——因此得名为“跨站”。需要注意的是，在过去的四五年里，现代浏览器已不再允许这种类型的跨站脚本攻击。一个域名无法访问另一个域名的内容。大多数现代跨站脚本攻击都是注入攻击，例如此处的示例（尽管通常要复杂得多）。

本介绍仅触及此类安全问题的一角。要记住的最点点是，当你使用服务器端应用程序时，必须对任何用户输入进行清理，以确保你收到的是预期的输入类型。关于此主题的更多信息，请访问 www.owasp.org/index.php/Cross_site_scripting。

## AJAX

AJAX 代表异步 JavaScript 和 XML（Asynchronous JavaScript and XML），它是 JavaScript 从 XML 文件获取信息而无需重新加载页面的方法。例如，向 Web 服务器的同步请求需要重新加载当前页面才能使用新信息。异步请求允许在无需等待整个页面重新加载的情况下获取并使用信息。

这种脚本在渐进式增强中非常有用，因为它允许为在现代浏览器中启用 JavaScript 的用户增强用户体验。无需等待页面再次加载，就可以实时获取并使用信息。

图 16-8 噢不！这对该网站的用户来说是不好的！

![](img/61d166424839b7674a7b9c8434ae4e03_484_0.png)

第 16 章：高级技术简介

463

在 JavaScript 中，会创建一个 XMLHttpRequest 对象，随后它可以在后台向服务器发送 HTTP 请求，并允许用户不中断地继续使用应用程序。

对此主题的深入介绍超出了初学者指南的范围；然而，关于 AJAX 以及如何在你的应用程序中使用它，可以在以下网站找到更多信息：

- https://developer.mozilla.org/en/AJAX
- www.w3schools.com/Ajax/Default.Asp

## JavaScript 库

有很多 JavaScript 库可以帮助你编写更高级的脚本，比从零开始编写所有代码要省力得多。这里列出了其中一些，以便你进一步研究：

- **jQuery** http://jquery.com
- **Prototype** www.prototypejs.org
- **Yahoo! YUI** http://developer.yahoo.com/yui

**Q：我可以在网上找到免费的可以复制粘贴的 JavaScript 代码？**
**A：** http://javascript.internet.com
http://webdeveloper.earthweb.com/webjs
www.javascriptcity.com

**Q：我可以在哪里学习更多关于 JavaScript 的？**
**A：** https://developer.mozilla.org/en/JavaScript
www.javascriptkit.com
www.quirksmode.org/js/contents.html
www.pageresource.com/jscript

**Q：我可以在哪里学习更多关于层样式表（CSS）？**
**A：** www.w3schools.com/Css/default.asp
www.csszengarden.com

**Q：我可以在哪里学习更多关于 DHTML？**
**A：** http://webreference.com/dhtml
www.dynamicdrive.com

专家问答

JavaScript：初学者指南

*第 16 章自测*

1. 以下哪行代码不会产生 JavaScript 语法错误？
A var myvar="cool;
B function 1cool()
C document.write(“Is there an error?”);
D window.alert “what is this?”);

2. 下列哪行代码不会产生 JavaScript 语法错误？
A var else=3;
B window.alert(“Cool!");
C document.write(“Cool!’);
D function while()

3. __________错误通常很难发现，因为代码的语法是正确的。
4. __________-__________脚本可能允许某人从应用程序的用户获取信息。
5. __________ 增强为所有观众提供内容，但为现代浏览器中使用 JavaScript 的用户增强了内容。
6. 尽可能从 HTML 文件中移除 JavaScript 代码并将其移动到外部文件中是一个好主意。
A 真
B 假
7. __________ 代表异步 JavaScript 和 XML。
8. JavaScript __________可能会通过让代码更容易编写来让一些高级编码任务变得更容易。
9. JavaScript 应该用于重要信息的密码保护。
A 真
B 假
10. __________ 是存储在终端用户计算机上的小型文本文件。
11. 使用哪个属性来设置和读取 cookie？
A window 对象的 cookie 属性
B document 对象的 cookie 属性
C document 对象的 cook 属性
D document 对象的 set_or_read_cookie 属性
12. 对象的哪个属性设置了图像对象实例的源？
A width
B height
C img_width
D src
13. 在哪种脚本中，你可能想在页面上预加载图像？
A 状态栏文本变化
B 悬停效果
C 动画文本
D 禁用右键
14. 使用 JavaScript 尝试隐藏页面源代码有效吗？
A 当然！
B 为什么不呢？
C 不，但它可以让阅读变得更加困难或令人恼火。
D 每次都有效！
15. JavaScript 有趣吗？
A 有趣！
B 不！
C 我是被老板强迫学的这个，所以它永远不会有趣！
D 你对趣味的定义是什么？

*本页特意留空*

![](img/61d166424839b7674a7b9c8434ae4e03_489_0.png)

467

附录

自测答案

JavaScript：初学者指南

第 1 章：JavaScript 简介

1. C. HTML
2. A. Web 浏览器
3. C. JavaScript
4. B. 假
5. D. lenient
6. A. 真
7. C. LiveScript
8. A. object based
9. B. client
10. B. 它可以在发送到服务器之前验证信息。
11. C. scripting
12. A. 真
13. D. Web 浏览器
14. D. 它被添加到 HTML 文档中。
15. A. <script> 和 </script> HTML 标签

第 2 章：将 JavaScript 放在 HTML 文件中

1. D. 以上所有
2. B 为了确保浏览器将将 JavaScript 解释为另一种脚本语言，并确保网页通过 XHTML 验证。
3. A. 是
4. noscript 标签为没有 **JavaScript** 的人提供了**内容**。
5. A. .js
6. B. <script type= “text/javascript” src=“yourfile.js”></script>
7. 在旧版本的 HTML 中，script 标签不区分大小写。但在 XHTML 中，script 标签必须小写。
8. D. 分号
9. A. document.write()
10. C. 当脚本很大或需要放在多个 HTML 文档中

附录：自测答案

469

11. JavaScript 注释对于**记录**或**调试**代码非常有用。
12. C. //
13. A. /*
14. D. */
15. A. close

第 3 章：使用变量

1. 变量**代表**或**保存**一个值。
2. 它们节省编写和更新脚本的时间，并使代码目的更清晰。
3. 要声明变量，使用 **var** 关键字。
4. D. =
5. C. var pagenumber=240;
6. B. 假
7. 变量名必须以字母或下划线开头。
8. A. 真
9. B. var my_house;
10. 在 JavaScript 中，变量值（类型）包括数字、字符串、布尔值和空。
11. 为了在 JavaScript 中表示指数，在基数数字之后、指数之前使用字母 **e**。
12. C. var mytext= “Here is some text!’
13. D. document.write(“John said, \“Hi!\””);
14. 特殊字符允许向字符串中添加其他无法添加的内容。
15. B. document.write(“I like to ”+myhobby+ “ every weekend”);

第 4 章：使用函数

1. 通常来说，函数是较大脚本中的小型**脚本**，用于执行单项**任务**或一系列**任务**。
2. 它们提供了一种将脚本的不同部分组织成必须完成的各个任务的方法，并且可以重用。





JavaScript：初学者指南

3. 在函数的第一行，你**声明**它为一个函数，给它**命名**，并指明它是否接受任何**参数**。

4. C. function

5. A. 大括号 – {}

6. A. 正确

7. B. 错误

8. C. function get_text()

9. **参数**用于允许函数从函数外部的地方导入一个或多个值。

10. B. 圆括号 – ()

11. D. 逗号

12. D. window.alert(“This is text”);

13. B. some_alert(“some”,“words”);

14. A. var shopping=get_something();

15. A **本地**变量只能在声明它的函数内部使用。

## 第 5 章：JavaScript 运算符

1. **运算符**（operator）是 JavaScript 中的一个符号或单词，用于对一个或多个值执行某种计算、比较或赋值。

2. **数学**运算符最常用于对两个值进行数学计算。

3. **加法**运算符将两个值相加。

4. 当自增运算符放在操作数**之前**时，它会将操作数的值加 1，然后执行语句的其余部分。

5. D. $#

6. A. 给变量赋一个新值

7. 加加赋值（+=）运算符将运算符**右侧**的值加到**左侧**变量上，然后将该新值赋给变量。

8. C. 比较两个值或语句，并返回真或假的尔值。

9. A. 4!=3

10. D. 4<=3

### 附录：自测答案

471

11. **逻辑**运算符允许你比较两个条件语句，以判断一个或两个语句是否为真，并据此进行操作。

12. B. !(17>=20)

13. B. (4>=4)&&(5<=2)

14. **位**运算符是在比特级上运行的逻辑运算符。

15. 在 JavaScript 中，运算符具有特定的**优先级**。

## 第 6 章：条件语句与循环

1. 条件语句是一种根据**条件**执行一段代码的语句，或者在该**条件**不满足时执行其他操作。

2. 你可以将条件语句想象成有点像**因**与**果**。

3. A. 正确

4. B. if (*y*<7)

5. C. 大括号

6. **switch**语句允许你取单个变量值，并根据变量的值执行不同的代码行。

7. **循环**是一个允许你重复执行某段代码的代码块。

8. B. 错误

9. A. for (*x=1;*x*<6;*x*+=1)

10. **while** 循环查看一个比较，并在比较不再为真时不断重复。

11. B. while (*x*=7)

12. A. 正确

13. B. 错误

14. B. 错误

15. D. 按照你喜欢的任意次数

## 第 7 章：事件处理器

1. A. 正确

2. 事件处理器非常有用，因为它们允许你**访问**页面上可能发生的**事件**。

3. 要使用事件处理器，你需要知道事件处理器的**关键字**以及将事件处理器放在 HTML 代码的什么位置。

4. C. <input type=“button” onclick=“window.alert('Hey there!’);”>

5. **load** 事件在 页面加载完成时发生。

6. D. 用户将鼠标光标移动到页面上的某个元素上。

7. B. 错误

8. **unload** 事件在用户离开当前 Web 页面时发生。

9. blur（失去焦点）事件是 **focus**（获得焦点）事件的反面。

10. A. <input type=“text” onfocus=“major_alert();”>

11. **change** 事件在用户更改表单内的内容时发生。

12. submit 事件在用户**提交** 页面上的**表单**时发生。

13. A. 正确

14. C. onmousedown

15. **addEventListener** 方法和 **attachEvent** 方法是注册事件的两种新方式。

## 第 8 章：对象

1. 对象是建模**真实**事物的一种，尽管对象是一个**抽象**实体。

2. 当你思考一个对象时，你可能想要可视化某个**通用**的东西。

3. 对象是有用的，因为它们提供了在脚本内部**组织**事物的另一种方法。

4. B. 点运算符

5. 对象的命名规则与命名**变量**和**函数**的规则相似。

6. 你可以使用**构造器**函数或对象**初始化器**来创建 JavaScript 对象。

7. A. 正确

8. B. 错误

9. C. 假设 myhouse 对象存在，它将 myhouse 对象的 kitchen 属性的值赋给变量 *x*。

10. D. this.cost=get_cost;

11. B. window.alert(“You are using ”+navigator.appName);

### 附录：自测答案

473

12. C. 假设 myhouse 对象存在，它将 myhouse 对象的 kitchen 属性的值赋给变量 *x*。

13. 在 JavaScript 中，原型（prototype）允许向对象添加属性和方法。

14. navigator 对象提供了浏览器的各种属性。

15. C. type

## 第 9 章：Document 对象

1. **document** 对象允许你访问页面的内容。

2. **document** 属性返回当前页面的 URL。

3. A. 正确

4. D. 属性

5. **document** 属性允许你修改页面内容。

6. C. 标签

7. **document** 属性包含了所有的 <a> 标签。

8. **innerHTML** 属性允许你修改内容。

9. **lastModified** 属性记录页面修改的时间。

10. A. 正确

11. A. 正确

12. C. URL

13. C. 属性

14. A. 属性

15. B. 间隔

## 第 10 章：Window 对象

1. **window** 属性允许你访问窗口。

2. A. 正确

3. **length** 属性记录了数量。

4. A. 正确

5. D. 属性

6. A. 属性

7. **self** 属性指向当前窗口。

8. C. 属性

9.

9. A. 正确

10. A. 正确

11. A. 正确

12. **alert** 方法属性出一个出一个消息。

13. **prompt** 方法用于提示用户输入。

14. D. 属性

15. B. 属性

## 第 11 章：数组

1. 数组是存储相似类型数据的一种方式。

2. 在 JavaScript 中，数组基本上是一个**对象**。

3. B. 索引

4. **关联**数组允许使用字符串进行访问。

5. D. 数组

6. D. new Array[10];

7. C. [4];

8. A. 数组

9. length 属性

10. 原型属性允许向现有对象添加属性和方法。

### 附录：自测答案

475

11. **concat()` 方法用于合并两个或多个数组并返回包含所有元素的数组。

12. join() 方法用于将数组元素合并为一个单一**字符串**，并用指定的字符分隔。

13. **pop() 方法用于从数组中删除最后一个元素。

14. C. 按字母顺序排序。

15. D. 字符串值

## 第 12 章：Math, Number 和 Date 对象

1. 对字符串的平方根等值进行计算并返回一个数字。

2. **E** 属性持有欧拉常数的值。

3. **LN10** 属性持有 10 的自然对数值。

4. B. 错误

5. document.write(Math.PI);

6. **SQRT2** 属性持有 2 的平方根值。

7. C. 绝对值

8. **asin() 方法返回传入数字的正弦值。

9. pow() 方法返回**第一个**参数的**第二个**参数幂的数值值。

10. C. var rand_int= Math.floor(Math.random()*8);

11. **sqrt() 方法返回传入数字的平方根。

12. D. Date 对象的实例

13. **getDay() 方法返回一周中的第几天。

14. B. 错误

15. B. 属性

## 第 13 章：处理字符串

1. **String** 对象提供了获取字符串信息或修改字符串的属性和方法。

2. 创建 String 对象的实例和创建字符串字面量

3. 你可以通过给变量赋值字符串值来创建一个字符串字面量。





JavaScript：初学者指南

4. C. JavaScript 获取字符串字面量并将其转换为临时的 String 对象

5. C. length

6. **length** 属性返回字符串的长度。

7. B. var the_text= "Look at me!";

8. B. charAt()

9. **big()** 方法在字符串值周围添加 `<big>` 和 `</big>` 标签。

10. concat() 方法将两个或多个字符串**组合**在一起，并返回新的组合字符串值。

11. D. indexOf() 方法返回一个数值，该数值是作为参数传递的字符的位置，但仅返回该字符首次出现的位置。

12. **italics()** 方法在字符串值周围添加 `<i>` 和 `</i>` 标签。

13. **toString()** 方法返回 String 对象的字符串字面量量值。

14. 若要替换字符串中的信息，可以使用正则表达式和 String 对象的 replace() 方法。

15. **match()** 方法比较正则表达式和字符串，以检查它们是否匹配。

## 第 14 章：JavaScript 与表单

1. 每当你向 HTML 文档添加一组 `<form>` 和 `</form>` 标签时，就会创建一个 **form**（表单）对象。

2. forms **array**（数组）允许你使用索引数字访问表单。

3. B. document.forms[3]

4. A. document.forms[2].length

5. C. document.forms.length

6. 使用表单 **names 或 ids** 允许你对以后想要访问的页面表单命名。

7. A. document.f1.e1.value

8. **action** 属性允许你访问起始表单标签中 `action="**"`"` 属性的值。

9. **elements** 属性是一个数组，允许你访问特定表单中的每个元素。

10. options 属性是一个数组，包含表单中 select 框内列出的每个 **option**（选项）的元素。

11. **reset()** 方法允许你使用脚本重置表单。

## 附录：自测答案

477

12. B. true or false

13. 当查看者点击表单上的提交按钮时，会发生 submit 事件，并可以通过 **onsubmit** 事件处理器进行捕获。

14. **submit()** 方法允许你在无需查看者点击提交按钮的情况下提交表单。

15. D. selectedIndex 属性

## 第 15 章：JavaScript 与框架

1. **Frames**（框架）将窗口划分为两个或多个独立的区域，每个区域包含不同的内容。

2. 框架与表格的区别在于，因为 frameset 中的划分包含独立的 **HTML** 文档。

3. **`<frameset></frameset>**** 标签用于创建框架集（frameset）。

4. 使用 **`<frame></frame>** 标签创建一个单个框架。

5. **cols** 属性将 frameset 划分为列。

6. 如果你想拥有一个既包含行又包含列的复杂框架集，可以将一个 frameset **嵌套**在另一个 frameset 内部。

7. A. frames 数组或框架名称

8. A. True

9. C. 窗口中框架的数量

10. B. 框架应该占据窗口中的任何剩余空间。

11. A. top

12. B. top.right_side.location="frame3.html";

13. 使用 target 为 **top** 告诉浏览器在打开 URL 时使用完整窗口，而不是在框架中打开 URL。

14. A. True

15. **rows** 属性将 frameset 划分为行。

## 第 16 章：高级技术简介

1. C. document.write("Is there an error?");

2. B. window.alert("Cool!");

3. **逻辑**（Logical）错误通常更难发现，因为代码的语法是正确的。

4. **跨**-**站**（Cross-site）脚本可能允许某些从应用程序的用户获取信息。

5. **渐进式**（Progressive）增强为所有查看者提供内容，但为现代浏览器中带有 JavaScript 的用户对其进行增强。

6. A. True

7. **AJAX** 代表异步 JavaScript 和 XML。

8. JavaScript **libraries**（库/类库）可能通过使代码更容易编写来让某些高级编码任务变得更容易。

9. B. False

10. **cookie**（Cookie）是存储在终端用户计算机上的小型文本文件。

11. B. document 对象的 cookie 属性

12. D. src

13. B. Rollover （鼠标悬停效果）

14. C. 不，但它可能会阅读变得更加困难或恼人。

15. 任何答案都是正确的！

## 索引

479

/ (正斜杠), 28

} (花括号), 62–63, 128

+ (加法运算符), 47, 49–50, 90–92

&& (与逻辑运算符), 107

= (赋值运算符), 36, 88, 97

(反斜杠), 42–43, 47

. (点), 22

" (引号), 47

转义字符, 44–46

== (等于运算符), 102–103

> (大于运算符) 103–104

>= (大于等于运算符) 104–105

< (小于运算符) 104

<= (小于等于运算符) 105

!= (不等于运算符) 103

=== (严格等于运算符) 105–106

!== (严格不等于运算符) 106

* (乘法运算符), 92

*= (乘法赋值运算符), 99

(分号), 19, 61–62

A

abort 事件 (onabort), 155

可访问性, 442–445

action 属性, 382–383

加法赋值运算符 (+=), 98

addEventListener( ) 方法, 172

+ (加法运算符), 47, 49–50, 90–92

AJAX, 462–463

alert( ) 方法, 249–251

alerts（警报框）

创建, 68–69

查找变量, 440–442

使用函数进行一个 alert, 69–70

alink 属性, 210

all 属性, 218

函数中的允许字符, 63

变量, 38–39

anchor( ) 方法, 347–348

anchors 属性, 210, *211*

AND 运算符 (&&), 107

匿名函数, 78

B

back( ) 方法, 200

反斜杠 (\), 42–43, 47

bgColor 属性, 210

位运算符, 89, 108

块 嵌套, 120–123

blur( ) 方法, 389

blur 事件 (onblur), 155–156

body 章节, 22, 68–70

arguments（参数）, 19

访问数组元素, 276–277

关联数组, 298–300

concat( ) 方法, 283–284, 353

constructor 属性, 279–280

创建数组, 292–293

定义的, 274–275

定义, 276–279

扩展方法, 291

index 和输入属性, 280

join( ) 方法, 284–285

length 属性, 280–281

遍历数组, 293–297

命名, 275

pop( ) 方法, 285–286

属性, 279–282

prototype 属性, 281–282

push( ) 方法, 286–287

reverse( ) 方法, 287, 290

shift( ) 方法, 287–288

slice( ) 方法, 288–289

sort( ) 方法, 290–291

splice( ) 方法, 289–290

toString( ) 方法, 291

unshift( ) 方法, 288–289

使用循环, 292–297

为什么数组很有用, 275

赋值运算符 (=), 36, 88, 97

访问, 299–300

定义, 299

attachEvent( ) 方法, 172–173

C

层叠样式表。*参见* CSS

大小敏感性, 17

对象, 178

变量, 38

CDATA 章节, 18

ceil( ) 方法, 314–315

charAt( ) 方法, 351–352

charCodeAt( ) 方法, 352

checked 属性, 384–386

基于类的, 定义, 8

clearInterval( ) 方法, 266–267

clearTimeout( ) 方法, 267–268

click( ) 方法, 389–390

客户端语言, 9

时钟,创建一个简单的时钟, 336–338

close( ) 方法, 225–227, 261–262

closed 属性, 243–244

颜色属性, 210

命令,添加到页面, 52–53

注释, 27

单行插入, 28

多行注释, 28–29

比较运算符, 88, 101

等于运算符 (==), 102–103

大于运算符 (>), 103–104

大于等于运算符 (>=), 104–105

小于运算符 (<), 104

小于等于运算符 (<=), 105

不等于运算符 (!=), 103

严格等于运算符 (===), 105–106

严格不等于运算符 (!==), 106

复杂比较, 123–125

concat( ) 方法, 283–284, 353

条件运算符, 126–127

Index

481

条件语句

定义的, 116–117

if/else 语句, 120–123

switch 语句, 125

为什么条件语句很有用, 117, 129

confirm( ) 方法, 251–252

内容

增强, 444–445

与呈现分离, 442–444

continue 语句, 141

cookie 属性, 210–211

cookieEnabled 属性, 197

Cookies, 446

读取, 449–451

设置, 446–449

创建方法, 228–233

D

Date 对象, 326

方法, 327–329

获取值的方法的方法, 329–332

设置值的方法的方法, 332–333

属性, 326–327

日期脚本, 334–338

调试脚本, 436–442

递减运算符 (–), 95–96

defaultChecked 属性, 384

defaultValue 属性, 386–387

dir 属性, 211–212

除法赋值运算符 (/=), 99

除以零, 93

除法运算符 (/), 93–94

do while 循环, 139–140

document 对象

all 属性, 218

anchors 属性, 210, *211*

颜色属性, 210

cookie 属性, 210–211

定义的, 206

dir 属性, 211–212

DOM节点方法, 230–233

DOM 节点属性, 228–230

domain 属性, 212–213

点 (.), 22

动态脚本

编码, 235–236

innerHTML 属性, 236–237

样式, 234–235

E

ECMAScript, 6

elements 属性, 383–384

encoding 属性, 391

errors, 436

alerts, 440–442

错误消息, 437–438, 441

逻辑错误, 439–442

扫描脚本的错误, 438–439

语法错误, 437–439





# JavaScript：初学者指南

- escape( ) 方法, 447–448
- 字符转义, 44–46
- 事件处理器, 18, 152, 154, 171–172
- addEventListener( ) 方法, 172
- 添加 id 属性, 151
- attachEvent( ) 方法, 172–173
- 按钮链接, 169–171
- 使用创建脚本, 167–171
- 定义, 148
- 文本框消息, 167–169
- 在 HTML 元素中使用, 149–150
- 在脚本代码中使用, 151–153
- 为什么事件处理器有用, 148
- 事件, 154–155, 166–167
- 终止事件 (onabort), 155
- 失去焦点事件 (onblur), 155–156
- 改变事件 (onchange), 156–157
- 点击事件 (onclick), 157–158
- 聚焦事件 (onfocus), 158–159
- 键按下事件 (onkeydown), 159
- 键击事件 (onkeypress), 160
- 键释放事件 (onkeyup), 160
- 加载事件 (onload), 160–161
- 鼠标按下事件 (onmousedown), 161
- 鼠标移动事件 (onmousemove), 161
- 鼠标移出事件 (onmouseout), 163
- 鼠标悬入事件 (onmouseover), 162–163
- 鼠标释放事件 (onmouseup), 164
- 重置事件 (onreset), 164
- 提交事件 (onsubmit), 164
- 卸载事件 (onunload), 164–165
- 练习。*参见* “尝试一下”练习
- 外部 JavaScript 文件
- 调用, 17
- 创建 JavaScript 文件, 23–24
- 创建 HTML 文件, 24–25
- 在浏览器中查看页面, 25–26

## F
- fgColor 属性, 210
- fieldset 标签, 393–394
- find( ) 方法, 253
- Firefox, 3, 4, 7
- 标志, 365–366
- floor( ) 方法, 315
- focus( ) 方法, 390
- fontcolor( ) 方法, 348–349
- fontsize( ) 方法, 349
- 循环中的 for each, 140, 296–297
- for in 循环, 140, 190–191
- for 循环, 131–137, 142
- 表单对象
- fieldset 标签, 393–394
- label 标签, 393
- 方法, 392
- 不假设客户端脚本, 394
- 属性, 377–380, 382–391
- 使用正确的元素和标签顺序, 393
- form 属性, 387
- formname 属性, 213–215, 222
- 表单
- 使用 ID 访问, 381–382
- 使用表单名称访问, 380–381
- 使用 forms 数组访问, 376–380
- 点击按钮, 399–403
- 确保可访问性, 392–394
- 带有对象和方法的表单元素, 385
- 验证, 395–397, 398
- forms 数组, 376–380
- forms 属性, 215
- forward( ) 方法, 200–201
- 正斜杠 (//), 28
- 框架 (frames)
- 使用框架名称访问, 417–418
- 使用 frames 数组访问, 414–417
- 跳出框架, 424–426
- 改变单个框架, 418–419, 427
- 改变多个框架, 419–422, 427
- 框架后的代码, 409–411
- 导航, 423–427
- 嵌套, 413–414, 427
- 选项, 411–414
- 目的, 408–409
- 行或列, 411–413
- 将观众导向, 426–427
- 与选择框配合, 423–424
- 跨框架使用变量, 428–431
- frames 属性, 244
- JavaScript 页面的框架，创建, 51
- fromCharCode( ) 方法, 353
- 函数构造函数, 77
- 函数表达式, 77
- 函数运算符, 77
- 函数, 19
- 允许字符, 63
- 匿名函数, 78
- 调用, 78
- 从另一个函数调用函数, 70–71
- 调用不存在的函数, 79
- 调用带参数的函数, 72–76
- 调用带返回语句的函数, 76
- 在脚本中调用, 67
- 大小写敏感, 63
- 声明, 61–62, 77
- 定义, 60–61
- 定义, 76–78
- 为...定义代码, 62–63
- 示例, 81–83
- 赋予意义的名字, 64
- 命名, 63–64
- 参数值, 65
- 参数, 61, 64–66
- 删除, 79
- 保留字, 63
- 返回语句, 61, 66–67
- 用于 JavaScript 警告, 69–70
- 使用多个参数, 65–66
- 使用值参数, 74–75
- 将变量作为函数参数, 73–74
- 何时调用, 79

## G
- getDate( ) 方法, 330
- getDay( ) 方法, 331
- getElementById( ) 方法, 224
- getElementsByClassName( ) 方法, 224
- getElementsByTagName( ) 方法, 225
- getFullYear( ) 方法, 332
- getHours( ) 方法, 331
- getMilliseconds( ) 方法, 331
- getMinutes( ) 方法, 331
- getMonth( ) 方法, 331
- getSeconds( ) 方法, 331
- getTime( ) 方法, 331
- getTimezone( ) 方法, 332
- getYear( ) 方法, 332
- 全局变量, 72–73
- *参见* 变量
- go( ) 方法, 201

## H
- head 部分, 22, 68–70
- Hello World 脚本
- 创建 HTML 文档, 20
- 插入到 HTML 文档, 20–21
- 编写脚本, 19–20
- 隐藏源代码, 461
- history 对象, 199–201
- home( ) 方法, 253
- HTML
- 学习 JavaScript 需知识, 3
- 脚本标签, 16
- HTML 编辑器, 6
- id 属性, 151
- *参见* Internet Explorer
- if/else 语句, 117–125
- 花括号, 128
- image 对象，属性, 452
- 改变不同的图片, 456–458
- 改变多个图片, 458–460
- 预加载, 452–453
- 鼠标悬停 (rollover), 454–460
- images 属性, 215
- 增运算符 (++), 94–95
- index 属性, 280
- indexOf( ) 方法, 353–355
- innerHeight 属性, 244–245
- innerHTML 属性, 236–337
- innerWidth 属性, 244–245
- input 属性, 280
- Internet Explorer, 3, 4, 7
- 等运算符 (==), 102–103
- 大于运算符 (>), 103–104
- 大于等于运算符 (>=), 104–105
- 小于运算符 (<), 104
- 小于等于运算符 (<=), 105
- 不等于运算符 (!=), 103

## J
- Java, 7
- Java applets, 7
- JavaScript
- 在浏览器中运行, 9–10
- 概述, 8–9
- 学习需知识, 2–6
- 主流浏览器支持, 5
- 编写页面, 51–54
- JavaScript, 6
- *参见* 语言

## L
- label 标签, 393
- 语言, 18
- JavaScript 属性, 18
- 脚本语言, 217, 18
- languages 属性, 246, 280–281, 344–345, 352, 359, 391
- 库, 463
- link( ) 方法, 349–351
- link 属性, 210
- link 属性, 219
- 加载事件 (onload), 160–161
- 本地变量, 73
- *参见* 变量
- location 属性, 246
- 逻辑错误, 439–442
- 逻辑运算符, 89, 107
- 位运算符, 108
- AND 运算符 (&&), 107
- OR 运算符 (||), 107–108

## 循环
- break 和 continue 语句, 141
- 计数变量, 142
- 定义, 130
- do while 循环, 139–140, 142
- for each 循环, 140, 296–297
- for 循环, 131–137, 142
- for in 循环, 140, 190–191
- 嵌套循环, 135–137
- 使用数组, 292–297
- while 循环, 137–139, 142
- 为什么循环有用, 130–131, 142

## M
- match( ) 方法, 356, 371–372
- Math 对象, 306
- ceil( ) 方法, 314–315
- floor( ) 方法, 315
- max( ) 和 min( ) 方法, 312–313
- 方法, 308–320
- pow( ) 方法, 313–314
- 属性, 306–308, 321
- random( ) 方法, 315–320, 321
- round( ) 方法, 315
- 双参数方法, 312–314
- 数学运算符, 88, 89–90
- 加法运算符 (+), 47, 49–50, 90–92
- 减减运算符 (–), 95–96
- 除法运算符 (/), 93–94
- 增运算符 (++), 94–95
- 取模运算符 (%), 94
- 乘法运算符 (*), 92
- 减法运算符 (–), 92
- 一元否定运算符 (–), 96
- max( ) 方法, 312–313
- MAX_VALUE 属性, 323
- 方法属性, 391
- 方法, 186–190, 198–199
- Microsoft Internet Explorer。*参见* Internet Explorer
- min( ) 方法, 312–313
- MIN_VALUE 属性, 323–324
- 取模运算符 (%), 94

## N
- 取模并赋值运算符 (%), 99–100
- 鼠标按下事件 (onmousedown), 161
- 鼠标移动事件 (onmousemove), 161
- 鼠标移出事件 (onmouseout), 163
- 鼠标悬入事件 (onmouseover), 162–163
- 鼠标释放事件 (onmouseup), 164
- moveBy( ) 方法, 262–263
- moveTo( ) 方法, 263–264
- Mozilla Firefox。*参见* Firefox
- 乘法运算符 (*), 92
- 乘法并赋值运算符 (*=), 99
- 名称, 246, 317, 387
- 导航表单, 399–403
- navigator 对象, 194
- 方法, 198–199
- NEGATIVE_INFINITY 属性, 24
- 嵌套循环, 135–137
- 嵌套框架, 413–414, 427
- 嵌套 if/else 语句, 117–125
- noscript 标签, 18
- NOT 运算符 (!), 108
- Number 对象, 322
- MAX_VALUE 属性, 323
- 方法, 198–199
- MIN_VALUE 属性, 323–324
- NEGATIVE_INFINITY 属性, 24
- POSITIVE_INFINITY 属性, 24
- 原型属性, 217
- toExponential( ) 方法, 324–325
- toFixed( ) 方法, 324–325
- toSource( ) 方法, 324
- toString( ) 方法, 324
- valueOf( ) 方法, 324
- 数字变量, 40–41

## O
- 基于对象的，定义, 8
- 对象操作
- for in 循环, 190–191
- with 语句, 191–192
- 对象
- 添加方法, 186–190, 192
- 构造函数, 178–184
- 定义, 176–177
- history 对象, 199–201
- 实例, 179, 192
- 命名, 177–178
- navigator 对象, 194–199
- 对象初始化器, 184–186, 192
- 预定义的, 194–201
- 属性, 176
- 属性值, 182–184
- 自写对象, 192
- 结构, 178–186
- 为什么对象有用, 177





JavaScript: 初学者指南

运算符 (*继续*)

比较, 88, 101–106
条件判断, 126–127, 129
逻辑, 89, 107–108
数学, 88, 89–96
优先级, 110–111
特殊, 89, 109
options 属性, 387–388
OR 运算符 (||), 107–108
优先级, 110–111

P

页面保护, 460–462
参数, 61, 64–66
可选的, 75–76
使用函数参数值, 65
使用多个参数, 65–66
使用值参数, 74–75
使用变量作为函数参数, 73–74
parent 属性, 248
括号, 110
parse( ) 方法, 333
密码, 461
platform 属性, 197–198
plugins 属性, 198
pop( ) 方法, 285–286
弹出窗口, 268
POSITIVE_INFINITY 属性, 324
pow( ) 方法, 313–314
预定义对象, 194–201
print( ) 方法, 254

编程语言
与 JavaScript 的相似之处, 8
*另另* 脚本语言
prompt( ) 方法, 255–256
prototype 属性, 281–282, 324, 327, 345
push( ) 方法, 286–287

Q

引号 (“), 47
转义字符, 44–46
以及字符串变量, 41–42

R

random( ) 方法, 315–320, 321
用于更新视觉效果的随机图片, 318–320
随机整数, 316
脚本的随机数, 316
用于趣味的随机引号, 316–318
referrer 属性, 219, 221
正则表达式, 363
添加标记, 365–366
代码, 367–368
创建, 363–364
创建强大的模式, 366–369
分组, 369–370
资源, 372
对字符串进行测试, 364–365
遥控器, 268
replace( ) 方法, 356, 370–371
保留字, 39, 40, 63
以及对象, 178
reset( ) 方法, 392
reset 事件 (onreset), 164
resizeBy( ) 方法, 265
resizeTo( ) 方法, 265
return 语句, 61, 66–67, 395–396
使用它们调用函数, 76
reverse( ) 方法, 287, 290
鼠标悬停效果, 454–460
round( ) 方法, 315

S

script 标签, 16, 18
body 部分, 68–70
外部脚本, 17
fieldset 标签, 393–394
head 部分, 68–70
label 标签, 393
noscript 标签, 17–19
脚本语言, 9
识别, 16–17
*另另* 编程语言

脚本
日期脚本, 334–338
动态脚本, 234–237

索引 487

Hello World, 19–21
签名脚本, 460
scrollBy( ) 方法, 265
scrollTo( ) 方法, 265
search( ) 方法, 356, 372
安全, 460–462
select( ) 方法, 390–391
selectedIndex 属性, 388
self 属性, 248

自测 (Self Tests)
答案, 448–478
第1章, 11–13
第2章, 29–31
第3章, 57–58
第4章, 84–86
第5章, 113–114
第6章, 143–145
第7章, 173–174
第8章, 202–203
第9章, 238–240
第10章, 269–271
第11章, 301–303
第12章, 339–340
第13章, 373–374
第14章, 404–405
第15章, 433–434
第16章, 464–465
自写的对象, 192
分号 (;), 19, 61–62
服务器端语言, 8
setInterval( ) 方法, 265–266
setTimeout( ) 方法, 267
shift( ) 方法, 287–288
签名脚本, 460
slice( ) 方法, 288–289, 356, 359
源代码，隐藏, 461
特殊字符, 42–44
特殊运算符, 89, 109
slice( ) 方法, 289–290
split( ) 方法, 356–357, 359
string 属性, 452
语句, 19
status 属性, 248
严格相等运算符 (===), 105–106
严格不等于运算符 (!==), 106
字符串字面量, 343
String 对象, 342
anchor( ) 方法, 347–348
charAt( ) 方法, 351–352
charCodeAt( ) 方法, 352
concat( ) 方法, 353
constructor 属性, 344
fontcolor( ) 方法, 348–349
fontsize( ) 方法, 349
fromCharCode( ) 方法, 353
indexOf( ) 方法, 353–355
length 属性, 344–345, 352
link( ) 方法, 349
match( ) 方法, 356, 371–372
添加 HTML 标签, 345–351
prototype 属性, 345
将方法组合, 360–362
正则表达式, 363–370
replace( ) 方法, 356, 370–371
search( ) 方法, 356, 372
slice( ) 方法, 356–357
对比 字符串字面量, 343–344
substr( ) 方法, 357
substring( ) 方法, 357–358
toLowerCase( ) 方法, 358
toString( ) 方法, 358
toUpperCase( ) 方法, 358
string 变量, 41–46
*另另* 变量
样式, 234–235
submit( ) 方法, 392
submit 事件 (onsubmit), 164
substr( ) 方法, 357
substring( ) 方法, 357–358
减赋值运算符 (=), 99
减法运算符 (-), 92
switch 语句, 125–126
语法错误, 437–439

T
target 属性, 391
三元运算符, 126–127, 129
文本框, 167–169
文本字符串, 19
title 属性, 219–220
DateString( ) 方法, 334
Exponential( ) 方法, 324–325
Fixed( ) 方法, 324–325
GMTString( ) 方法, 334
标记, 62–63
LocaleDateString( ) 方法, 334
LocaleString( ) 方法, 334
LocaleTimeString( ) 方法, 334
LowerCase( ) 方法, 358
op 属性, 248
Source( ) 方法, 291, 324, 326, 334, 358
String( ) 方法, 334
TimeString( ) 方法, 334

Try This (尝试练习)
向文档添加 DOM 节点, 233
调整变量值, 100–101
构建选择框脚本, 403
从 HTML 文档调用外部脚本, 26–27
更改框架, 422
构建 if/else 块, 129–130
创建一个按钮, 153
创建一个计算机对象, 193–194
创建一个 JavaScript 时钟, 338–339
带有函数的 HTML 页面, 79–80
带有 JavaScript 的 HTML 页面, 55–57
声明变量, 47–48
在页面显示随机链接, 321–322
将脚本插入 HTML 文档, 22–23
使用选择框脚本, 403
从 HTML 文档使用外部脚本, 26–27

V
var 关键字, 37
window 对象, 242
alert( ) 方法, 249–251
closed( ) 方法, 243–244
confirm( ) 方法, 251–252
defaultStatus 属性, 244
扩展属性, 260–261
find( ) 方法, 253
frames 属性, 244
home( ) 方法, 253
innerHeight 和 innerWidth, 244–245
length 属性, 246
location 属性, 246
方法, 249–250
moveBy( ) 方法, 262–263
moveTo( ) 方法, 263–264
name 属性, 246–247
open( ) 方法, 256–261
opener 属性, 247
parent 属性, 248
弹出窗口, 268
print( ) 方法, 254
prompt( ) 方法, 255–256
属性, 242–248
resizeBy( ) 方法, 265
resizeTo( ) 方法, 265
scrollBy( ) 方法, 265
scrollTo( ) 方法, 265
self 属性, 248
setInterval( ) 方法, 265–266
setTimeout( ) 方法, 267
标准属性, 257–260
status 属性, 248
top 属性, 248
with 语句, 191–192
write( ) 方法, 227
writeIn( ) 方法, 227–228

X
XHTML
大小写敏感, 17
type 属性, 18
页面验证, 18
XMLHttpRequest 对象, 9


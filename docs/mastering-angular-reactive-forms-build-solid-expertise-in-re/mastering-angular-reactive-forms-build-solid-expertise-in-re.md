# Angular 响应式表单精通：通过真实案例使用 Angular 12 表单控件、表单组、表单数组、验证器及测试等构建坚实的响应式表单专业知识






通过 Angular 12 的真实案例，使用 Form Control、Form Group、Form Array、Validators、测试等构建实实的响应式表单专业知识













**献给**

*献给我那耐心的妻子 Tania，她将我的不完美变为完美，以及我的女儿 Nelly！*
*感谢一切。*

## 关于作者

**Fanis Prodromou** 是一位对 Angular 前端开发充满热情的高级软件工程师。他住在希腊雅典，曾曾在许多大型公司工作。在 14 年的编程生涯中，他在代码质量、应用架构和应用性能方面积累了丰富的经验。

由于意识到计算机科学和技术领域演变之快，他努力通过参加会议和聚会、学习以及尝试新技术来保持与同步。他喜欢分享自己的知识并帮助其他开发者。

“分享即关怀”

他通过 Code.Hub Institute 在企业公司教授 Angular，撰写文章，制作 YouTube 视频并在 Angular 聚会上发表演讲。他喜欢与他的两只猫度过时光，并在空闲时间徒步和潜水。

## 关于评审员

**Pankaj Parkar** 在 Angular、React 和 EmberJS 等不同前端技术方面拥有七年的工作经验，目前在 Deskera 担任高级软件工程师。他在 Angular 和 Web 应用开发等方面的技能使他成为了 Microsoft MVP 和 Google 开发者专家（GDE）。

Pankaj 喜欢与社区分享知识；因此，你会发现他在各种技术活动和会议上进行演讲。Pankaj 也是印度 Stack Overflow 的顶级贡献者，并在 Angular 和 AngularJS 领域位列全球前 20 名。他还是 BPB Publications 的技术评审员。他现在专注于将自己的知识投入开源项目，并通过导师指导、创建 POC（概念验证）、举办工作坊和编写博客与社区分享，以帮助世界变得更美好、更发达。

## 致谢

我在 15 年前遇到了我的妻子，从那以后，我们就生活在一起。毫无疑问，她是我的另一半。她支持我的抱负，让我成为一个更好的人。没有我的妻子，我无法写出这本书。

感谢我在 Angular Athens Meetup 和 Angular Nation 的朋友和共同组织者，我在那里结识了优秀的人并交流了许多想法。

感谢书籍评审员 Pankaj Parkar。他的参与和宝贵建议让这本书变得完善。特别感谢 BPB Publications，尤其是 Nrip Jain，感谢他们在创建和出版这本书过程中提供的支持、建议和帮助。

## 前言

Angular 框架有两种构建 HTML 表单的方法：基于模板驱动的表单（template-driven forms）和响应式表单（reactive forms）。后者由于基于模型，因此也被称为模型驱动表单（model-driven forms）。

比较这两者，我们可以说责任已经从 HTML 模板转移到了源代码。例如，在模板驱动的表单中，单元测试和验证是在 HTML 中应用的；而在响应式表单中，它们是应用在源代码（typescript）中的。在响应式表单中，源代码起着重要作用，并提供了极大的活性。

Angular 表单是用户与系统之间的通信通道。我们通过表单收集数据，并在大多数情况下通过 API 向服务器提供这些数据。数据是一项宝贵的资产，应当是准确的。因此，使用 Angular 响应式表单是有优势的，因为我们拥有所有必要的工具来确保数据的完整性。

本书遵循 Angular 12 的最新更改，并基于 Typescript 的 Strict（严格）标志。

*本书由七章组成，读者将在其中学习以下内容：*


## 下载代码

**代码包和彩色图片：**

请通过链接下载本书的***代码包***和***彩色图片***：

**https://rebrand.ly/eccf8c**

**勘误**

我们对 BPB Publications 的工作非常自豪，并遵循最佳实践以确保内容的准确性，为订阅者提供浸式的阅读体验。读者是我们的镜子，我们利用他们的输入来反思并改进出版过程中可能出现的人为错误。为了让我们维护质量并帮助任何因意外错误而遇到困难的读者，请写邮件告诉我们：**errata@bpbonline.com**

BPB Publications 家庭非常感谢您的支持、建议和反馈。

您知道吗？BPB 为出版的书提供电子版本，提供 PDF 和 ePub 文件。作为纸质书客户，您可以在 **www.bpbonline.com** 升级到电子版，您有权获得电子版的折扣。

有关更多信息，请通过 **business@bpbonline.com** 与我们联系。

在 **www.bpbonline.com**，您还可以阅读免费的技术文章集、订阅一系列免费的时事通讯，并



获取 BPB 书籍和电子书的专属折扣和优惠。

**BPB 寻找像你这样的作者**

如果你对成为 BPB 的作者感兴趣，请访问 **www.bpbonline.com** 并立即提交申请。我们曾与成千上万像你这样的开发者和技术专业人员合作，帮助他们将自己的见解分享给全球技术社区。

你可以提交通用申请、申请我们正在招募作者的特定热门话题，或者提交自己的想法。

书籍的代码包也托管在 GitHub 上，地址为 **https://github.com/bpbpublications/Mastering-Angular-Reactive-Forms**。如果代码有更新，它将在现有的 GitHub 仓库中进行更新。

我们丰富的书籍和视频目录中还有其他代码包，地址为 **https://github.com/bpbpublications**。快去查看吧！

**反盗版声明**

如果您在互联网上发现任何形式的我们作品非法盗版，如果您能向我们提供地址或网站名称，我们将不胜感激。请通过 **business@bpbonline.com** 联系我们并附上材料的链接。

**如果你对成为作者感兴趣**

如果你有一个你擅长的领域，并且你对编写或贡献书籍感兴趣，请访问 **www.bpbonline.com**。

**评论**

请留下您的评论。在您阅读并使用此书后，为什么不在您购买的网站上发表评论呢？潜在的读者可以查看并参考您中立的意见来做出购买决策，我们 BPB 可以了解您对我们产品的看法，我们的作者也可以看到您对他们书籍的反馈。谢谢！

欲了解更多关于 BPB 的信息，请访问 **www.bpbonline.com**。







- 问题
- 问题

索引

# 第一章：响应式表单入门

### 简介
Angular 表单是用户与系统之间的通信通道。我们通过表单收集数据，并在大多数情况下，通过 API 向服务器提供这些数据。数据是宝贵的资产，应该是准确的，因此使用响应式表单非常有优势，因为我们拥有所有工具来确保数据的完整性。

在本章中，我们将学习什么是响应式表单以及为什么我们应该掌握它们。我们还将学习所有的响应式表单构建块：**FormControl**、**FormGroup** 和 **FormArray**。为了完全跟随此书，您应该熟悉以下内容：
- 具备创建 Angular 组件和 Angular 模块所需的技能
- HTML5 基础知识
对 CSS3 的基本理解

**注意：** 本书的代码示例可在以下 GitHub 仓库中找到，分为不同的分支：https://github.com/profanis/bpb-mastering-angular-reactive-forms

### 结构
- 什么是响应式表单？
- 为什么要使用响应式表单？
- 理解构建块
- 使用 FormControl
- 使用 FormGroup
- formControlName 指令
- 嵌套 FormGroup
- formGroupName 指令
- 在 FormGroup 中使用 FormArray
- 在 FormArray 中动态添加控件
- *从 FormArray 中动态移除控件*
- FormGroup 操作
- *创建页面*
- *更新页面*
- 表单模型 (Form Model)
- 表单构建器 (Form Builder)
- *带有 FormControls 的 FormGroup*
- 带有 FormControl 的 FormArray

### 目标
阅读本章后，您将掌握响应式表单的基础知识，并学习如何构建 Angular 表单。您还将学会区分各种响应式表单指令，并根据情况使用它们来提高整体性能。





## 模板

表单模型

单元测试

验证

我们所说的“**模板**(templating)”是指终端用户在浏览器中看到的实际表单。

我们所说的“**表单模型**(form model)”是指我们创建的与 HTML 模板进行绑的模型。由于这是一个有趣的话题，我们在本章末尾添加了一个单独章节。

“**单元测试**(unit tests)”应该是开发者的好朋友。我们熟悉使用 Karma/Jasmine、Jest 或任何其他库对 Angular 服务中的业务代码进行单元测试。使用响应式表单（Reactive Forms），我们可以不引用 HTML 而测试表单，只需测试源代码（**component.ts**）。

“**验证**(validations)”可能会变得复杂。例如：

“*一个输入元素应该最少三个字母，最多十个字母；它应该包含至少一个特殊字符，并且当另一个字段具有特定值时，此验证也有效。*”噢，天哪！如果我们有正确的工具，这只是一个可以完成的简单挑战。没错，通过响应式表单，验证可以变得很有趣。

## 理解构建块

响应式表单有三个构建块，每个构建块都负责处理值和有效性。重要的是理解，我们要么从 `component.ts` 代码中设置值，要么在终端用户在 HTML 表单字段中输入时设置值。不完全理解没关系，我们很快就会学习值和有效性的含义。

- **FormControl** 是一个我们与单个 HTML 输入元素映射的类。
- **FormGroup** 是一组 **FormControl** 实例的组。
- **FormArray** 是 **FormControl**、**FormGroup** 或 **FormArray** 实例的数组。

下面的图展示了上述内容的示例：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_22_0.png)

***图 1.1:*** *响应式表单构建块*

## 使用 FormControl

**FormControl** 是响应式表单三个基本构建块之一。另外两个是 **FormGroup** 和 **FormArray**，我们将在接下来的页面中介绍。在 HTML 表单中，**FormControl** 是 HTML 元素，例如输入元素、复选框、单选按钮和选择菜单。

让我们用下面的图片描述这一点：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_22_1.png)

***图 1.2:*** *带有两个 FormControl 项的表单*

在图中，“**First Name**”和“**Last Name**”输入被视为 FormControl，但我们必须先将它们转换为实际 **FormControl** 实例。

首先，由于 Angular 是模块化的，我们必须在我们的**单页应用**(**SPA**)² 中导入相应的模块。

**注意：** 如果像 Angular 这样的框架不是模块化的并且默认加载所有内容，这将意味着额外的编译和树摇优化（Tree Shaking）时间。

相应的模块是 **ReactiveFormsModule**，我们必须在每个打算使用响应式表单的功能模块³中导入它。通过导入此模块，Angular 会注入开发表单所需的功能。这些功能由几个指令和各种类组成。

让我们看看如何在模块中导入 **ReactiveFormsModule** 的示例：

**module.ts 代码**

1: import {NgModule} from '@angular/core';
2: import {ReactiveFormsModule} from '@angular/forms';
3: import {BrowserModule} from '@angular/platform-browser';
4: import {AppComponent} from './app.component';
5:
6: @NgModule({
7: declarations: [
8: AppComponent
9: ],
10: imports: [
11: BrowserModule,
12: **ReactiveFormsModule**
13: ],
14: bootstrap: [AppComponent]
15:})
16: export class AppModule {}

在第 2 行，我们使用 ES6 声明从 **@angular/forms** 导入 **ReactiveFormsModule**。在第 12 行，我们将该模块导入 Angular 的 imports 数组中。遵循前面的*图 1.2*，我们将在组件中创建两个 **FormControl** 实例，如下代码所示：

**component.ts 代码**

1: import {Component, OnInit} from '@angular/core';
2: import {FormControl} from '@angular/forms';
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss']
8:})
9: export class AppComponent implements OnInit {
10: firstNameControl!: FormControl
11: lastNameControl!: FormControl
12:
13: ngOnInit(): void {
14: **this.firstNameControl = new FormControl()**
15: **this.lastNameControl = new FormControl()**
16: }
17:}

在第 2 行，我们使用 ES6 声明从 **@angular/forms** 导入 **FormControl**，在第 14 行和第 15 行中，我们实例化了 FormControl。

现在让我们如何在 HTML 中使用这些控件：

**component.html 代码**

1: <input type="text"
2: placeholder="First Name"
3: [formControl]="firstNameControl">
4:
5: <input type="text"
6: placeholder="Last Name"
7: [formControl]="lastNameControl">

在第 3 行和第 7 行中，我们使用 [formControl]，它是源代码（**component.ts**）和模板（**component.html**）之间的胶水。我们什么是绑定？简单来说，终端用户在输入字段中输入的任何内容，对应的 **FormControl** 的值都会自动更新。让我们尝试一下！





在第 14 行，我们使用构造函数为 **FormControl** 定义了一个默认值，在第 16 行，我们使用了 **.setValue**。

之前的代码具有以下结果：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_28_0.png)

***图 1.4:*** *带有结果的 FormControl 示例*

## 使用 FormGroup

在上一节中，我们学习了 HTML 元素是如何映射到 FormControl 的。那么，如果我们有可以组合在一起的 HTML 元素呢？我们使用 **FormGroup** 将 **FormControl**、嵌套的 **FormGroup** 或 **FormArray** 实例分组，并处理所有这些控件的值和有效性。

让我们创建一个 **FormGroup** 实例：

**component.ts 代码**

1: import {Component, OnInit} from '@angular/core'
2: import {FormGroup} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8:})
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup
11:
12: ngOnInit(): void {
13: **this.myForm = new FormGroup({})**
14: }
15:}

在第 2 行，我们从 **@angular/forms** 使用 ES6 声明导入 **FormGroup**，在第 13 行，我们实例化了本地变量 **myForm**。如果我们仔细观察，**FormGroup** 类的构造函数有一个空对象符号 {}，我们将从这里开始分组。

在接后的代码中，我们将看到如何向 **FormGroup** 中添加 **FormControl** 实例。在此之前，重要的是理解 **FormGroup** 是一个带有属性和值的 JavaScript 对象。如果以对象 {"foo": "bar"} 为例，"foo" 是属性，而 "bar" 是值。

同样，在 **FormGroup** 中，控件名称是属性，而控件类型是值。

让我们看一个包含两个 FormControl 的 **FormGroup** 示例：

**component.ts 代码**

1: import {Component, OnInit} from '@angular/core'
2: import {FormControl, FormGroup} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8:})
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup
11: firstNameControl!: FormControl
12: lastNameControl!: FormControl
13:
14: ngOnInit(): void {
15: **this.firstNameControl = new FormControl()**
16: **this.lastNameControl = new FormControl()**
17:
18: this.myForm = new FormGroup({
19: firstName: this.firstNameControl,
20: lastName: this.lastNameControl,
21: )
22: }
23:}

在第 18-21 行，我们看到了一个名为 **myForm** 的 **FormGroup**，它有两个控件：

1. **firstName FormControl：**
   为了更好地理解这一点，让我们看看 JavaScript 对象的部分：
   - **property（属性）**: 是 **firstName**
   - **value（值）**: 是 **this.firstNameControl**

2. **lastName FormControl：**
   为了更好地理解这一点，让我们看看 JavaScript 对象的部分：
   - **property（属性）**: 是 **lastName**
   - **value（值）**: 是 **this.lastNameControl**

我们不应该避免提到，虽然这段代码是有效的，但使用变量 **FormControl(s)** 的 **FormGroup** 并不常见。原因是该组件可以扩展很多。想象一个有 20 个表单元素的表单。如果我们必须定义 FormControl 变量（如前面代码中的第 11, 12 行所示）并实例化它们（如第 15 和 16 行所示），将导致代码杂乱。

较好的是使用单行代码，如下所示所示：

**component.ts 代码**

1: import {Component, OnInit} from '@angular/core'
2: import {FormControl, FormGroup} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8:})
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup
11:
12: ngOnInit(): void {
13: this.myForm = new FormGroup({
14: **firstName: new FormControl(),**
15: **lastName: new FormControl(),**
16: )
17: }
18:}

之前的代码更具可读性，并且符合当前的最佳实践！

让我们继续学习 **FormGroup** 并学习如何将这些控件（**firstName** 和 **lastName**）绑定到 HTML 元素。

**component.html 代码**

1: <form [formGroup]="myForm">
2:
3: <input type="text"
4: placeholder="First Name"
5: formControlName="firstName" />
6:
7: <input type="text"
8: placeholder="Last Name"
9: formControlName="lastName" />
10:
11: </form>

在第 1 行，我们使用 [formGroup] 指令将文档对象模型（DOM）与 **FormGroup** 实例绑定，这对应了我们在 **component.ts** 中创建的表单模型。

请注意，在第 5 行和第 9 行，我们使用 formControlName 指令来应用输入字段，而不是像我们在之前的示例中那样。

在下一节中，我们将看到该指令是如何工作的。**[formGroup]** 指令有一个作用域，它位于开始和结束标签之间，如下图所示：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_32.png)

***图 1.5:*** *FormGroup 范围*

## formControlName 直接

我们使用此指令通过名称引用属于 FormGroup 的 FormControl。这背后的机制是 formControlName 指令会检查 DOM 祖先以寻找最近的 **formGroup**。为了更好地理解这一点，让我们看一个纯 JavaScript 示例：

1: const obj = {
2: foo: 'bar',
3: foo1: 'bar1',
4: }
5: console.log(obj['foo'])
6: console.log(obj.foo)

两个访问器都会返回相同的结果。

## 嵌套 FormGroup

企业级应用通常具有带有复杂验证表单。在这种情况下，必须通知用户表单的有效性状态（详见*第 3 章：内置验证*）。如果我们将表单拆分成较小的部分，更容易管理数据和有效性状态。

在接后的图中，我们看到了一个由两部分组成的表单示例。第一部分指的是用户基本信息的表单字段：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_34.png)

***图 1.6:*** *用户基本信息*

第二部分指的是用户地址的表单字段：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_35.png)

***图 1.7:*** *用户地址*





**component.ts 代码**

1: import {Component, OnInit} from '@angular/core'
2: import {FormControl, FormGroup} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8:})
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup
11:
12: ngOnInit(): void {
13: this.myForm = new FormGroup({
14: basicInfo: new FormGroup({
15: firstName: new FormControl(),
16: lastName: new FormControl(),
17: email: new FormControl(),
18: age: new FormControl(),
19: }),
20: address: new FormGroup({)

第一个 FormGroup 位于第 14 行，第二个位于第 20 行，且它们都是名为 **myForm** 的 FormGroup 的子项。我们实现了一个树形结构，如下：

/myForm
  /basicInfo
    firstName
    lastName
    email
    age
  /address
    street
    number
    postal

现在让我们看看如何将这些控件与 HTML 输入元素绑定：

**component.html 代码**

1: <form [formGroup]="myForm">
2:
3: <div formGroupName="basicInfo">
4:
5: <input type="text"
6: placeholder="First Name"
7: formControlName="firstName" />
8:
9: <input type="text"
10: placeholder="Last Name"
11: formControlName="lastName" />
12:
13: <input type="email"
14: placeholder="e-mail"
15: formControlName="email" />
16:
17: <input type="number"
18: placeholder="Age"
19: formControlName="age" />
20:
21: </div>
22:
23: <div formGroupName="address">
24:
25: <input type="text"
26: placeholder="Street"
27: formControlName="street" />
28:
29: <input type="number"
30: placeholder="Number"
31: formControlName="number" />
32:
33: <input type="number"
34: placeholder="Postal Code"
35: formControlName="postal" />
36:
37: </div>
38:
39: </form>

在第 3 行和第 23 行中，我们使用了 **formGroupName** 指令，它的作用与 **formControlName** 相似。我们使用它通过名称定位嵌套的 FormGroup，并在相应的 div 元素中应用绑定。

### formGroupName 指令

我们使用 **formGroupName** 指令将嵌套的 FormGroup 绑定到 DOM 元素中。

为了理解该指令的工作原理，让我们来看一个普通 JavaScript 对象的示例以及属性访问器的工作方式：

1: const obj = {
2: foo: {
3: key1: 'value1',
4: },
5: foo1: {
6: key2: 'value2',
7: },
8: }
9:
10: console.log(obj['foo']['key1'])
11: console.log(obj.foo.key1)

上面的示例是一个包含两个嵌套对象的对象：foo 和 foo1。有两种方式可以访问嵌套对象及其属性：

- 在第 10 行中，我们使用了**括号表示法（bracket notation）**属性访问器
- 在第 11 行中，我们使用了**点表示法（dot notation）**属性访问器

这两个访问器将返回相同的结果，“**value1**”。

同样，**formGroupName** 指的是一个嵌套的 JavaScript 对象，或者准确地说，一个嵌套的 **FormGroup**。

让我们来看包含以下 **FormGroup** 的示例：

1: this.myForm = new FormGroup({
2: basicInfo: new FormGroup({
3: firstName: new FormControl(),
4: }),
5:})

以及 HTML：

1: <form [formGroup]="myForm">
2:
3: <div formGroupName="basicInfo">
4:
5: <input type="text"
6: placeholder="First Name"
7: formControlName="firstName" />
8: </div>
9:
10: </form>

为了在输入元素（第 5-7 行）中应用绑定，我们必须定位 **FormControl** 实例路径，就像我们之前处理 **obj.foo.key1** 时做的那样。路径是 **myForm.basicInfo.firstName**。

### 在 FormGroup 中使用 FormArray

**FormArray** 类是响应式表单（Reactive Forms）三个基础构建模块之一，我们将它与 **FormGroup** 配合使用。

**FormGroup** 除了嵌套 **FormGroup** 或 **FormControl** 实例外，还可以拥有 **FormArray** 实例。

当我们有相同类型的项时（例如字符串值颜色的列表，或者相同类型对象的列表），使用 **FormArray** 会更好。

在下面的图片中，我们看到了两个 HTML 输入元素，根据我们目前掌握的知识，我们知道如何对它们应用绑定。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_39_0.png)

***图 1.8:*** *颜色 FormArray 示例*

但等一下，这张图片的右下角有一个加号图标，表示用户可以动态添加更多 **FormControl** 项。

由于我们需要更多相同类型的 **FormControl**（特别是颜色），我们可以想象我们需要一个数组。

让我们逐步查看它。我们将创建一个包含嵌套的 FormGroup 实例的 FormArray 的 FormGroup，结构如下树形结构：

| AbstractControl 实例 | AbstractControl 类型 |
| :--- | :--- |
| **myForm** | **FormGroup** |
| | **colors** (**FormArray**) |
| | | **0** (**FormGroup**) |
| | | **name** (**FormControl**) |
| | | **1** (**FormGroup**) |
| | | **name** (**FormControl**) |
| | | **2** (**FormGroup**) |
| | | **name** (**FormControl**) |

***表 1.1***

请注意，我们有三个嵌套的 FormGroup 实例，它们被标记为索引 0、1、2。

**component.ts 代码**

1: import {Component, OnInit} from '@angular/core'
2: import {FormControl, FormGroup} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8:})
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup
11:
12: ngOnInit(): void {
13: this.myForm = new FormGroup({
14: basicInfo: new FormGroup({
15: firstName: new FormControl(),
16: lastName: new FormControl(),
17: email: new FormControl(),
18: age: new FormControl(),
19: }),
20: address: new FormGroup({
21: street: new FormControl(),
22: number: new FormControl(),
23: postal: new FormControl(),
24: }),
25: })
26: }
27: }

在第 12-14 行中，我们有一个返回颜色 FormArray 的 getter 方法。因为返回的类型是 **AbstractControl**，我们必须显式提供类型。

**component.html 代码**

1: <form [formGroup]="myForm">
2:
3: <div-container formArrayName="colors">
4:
5: <div *ngFor="let _ of colors.controls; let idx = index">
6: <ng-container [formGroupName]="idx">
7: <input type="text" formControlName="name" />
8: </ng-container>
9: </div>
10: </ng-container>
11: </form>

（等等，HTML 的 OCR 文本乱序了，根据提供的片段逻辑进行了重构）

与 **formGroupName** 指令一样，我们使用 **formArrayName** 指令在宿元素（第 3 行）中应用绑定。然后我们遍历数组项（第 5 行）。在第 7 行中，我们对嵌套的 FormGroup 应用绑定，这可能是索引。

**component.ts 代码**

1: addColor(value?: string) {
2: this.colors.push(
3: new FormGroup({
4: name: new FormControl(value),
5: })
6: )
7: }

假设我们调用了方法 **addColor('cyan')**。在这种情况下，colors 数组将拥有四个 **FormControl**，由于绑机制，第四个不需要额外的编程操作就会出现在 HTML 中。

| 索引 | 值 |
| :--- | :--- |
| 1 | red |
| 2 | green |
| 3 | blue |
| 4 | cyan |

***表 1.2***

**从 FormArray 中动态删除控件**

既然我们已经学习了如何动态添加控件，让我们也看看如何使用以下方法动态删除 AbstractControl：

removeAt(index: number): void;





**注意：** `removeAt()` 方法是从零开始索引的。

在接下来的示例中，我们将使用 **.removeAt()** 方法从数组中移除控件：

**component.ts 代码**

1: removeColor(index: number) {
2: this.colors.removeAt(index)
3: }

假设我们调用了 **removeColor(0)** 方法。在这种情况下，颜色数组将减少一个，更改将无需任何额外的编程操作就会显示在 HTML 中。

在这里，我们将看到一个实用的示例，展示如何将 **removeColor()** 方法应用于 HTML 模板：

**component.html 代码**

1: <div *ngFor="let _ of colors.controls; let idx = index">
2:
3: <ng-container [formGroupName]="idx">
4: <input type="text" formControlName="name" />
5: **<span (click)="removeColor(idx)">X</span></span>**
6: </ng-container>
7: 
8: </div>

在第 5 行中，我们将 **removeColor** 设置为 span 元素的点击事件处理程序。

## FormGroup 操作

**FormGroup** 是继承自 **AbstractControl** 类的类，具有许多方法，如果我们学会如何有效地使用它们，将对我们大有帮助。方法列表非常大，但我们将回顾它们非常基础的内容。

| 方法名称 | 描述 |
| :--- | :--- |
| **setValue()** | 它接受一个与 FormGroup 结构相似的对象 |
| **patchValue()** | 它与 setValue() 相同，不同在于如果我们没有传递相同的对象结构，它不会报错 |

***表格 1.3***

使用 **setValue()** 和 **patchValue()** 方法的一个实际用例是当我们需要从 API 获取数据填充 **FormGroup** 时。例如，让我们获取包含“基本信息 (BasicInfo)”和“地址 (Address)”部分的用户资料页。根据虚拟的业务需求，我们必须创建一个用户可以在其中创建配置的页面，以及另一个更新已创建配置的页面。我们将这些页面分别命名为“*创建* (Create)”和“*更新*”。为了用数据填充表单字段，我们将使用 **setValue()** 或 **patchValue()**。

### 创建页面

当用户点击表单的提交按钮时，我们收集数据以进行处理。在接下来的代码中，我们将看到如何在表单中设置提交事件：

**component.html 代码**

1: <form [formGroup]="myForm" (ngSubmit)="submitForm()">
2:
3: <div formGroupName="basicInfo">
4: <!-- 输入元素 -->
5: </div>
6: 
7: <div formGroupName="address">
8: <!-- 输入元素 -->
9: </div>
10:
11: **<button type="submit">提交</button>**
12: </form>

在下一个代码中，我们将看到提交事件处理程序的实现：

**component.ts 代码**

1: submitForm() {
2: //在此调用服务方法，该方法会将请求委托给 API 请求
3: console.log(this.myForm.value)
4: }

在第 3 行中，我们使用 **FormGroup** 的属性值，它返回一个与我们在 FormGroup 中构建的类似的 JSON 对象。以下 JSON 对象是我们在“更新页面”部分将创建的表单模型的结果：

```json
{
  "basicInfo":{
    "firstName":"John",
    "lastName":"Doe",
    "email":"john@doe.com",
    "age":"76"
  },
  "address":{
    "street":"street name",
    "number":"12",
    "postal":"49000"
  }
}
```

### 更新页面

为了更新已创建的用户配置，我们从源（例如 API 等）获取值，并用这些数据填充表单字段。在接下来的代码中，我们创建了一个 **FormGroup**，并使用 **setValue()** 方法为其提供数据：

**component.ts 代码**

1: ngOnInit(): void {
2: this.myForm = new FormGroup({
3: basicInfo: new FormGroup({
4: firstName: new FormControl(),
5: lastName: new FormControl(),
6: email: new FormControl(),
7: age: new FormControl(),
8: }),
9: address: new FormGroup({
10: street: new FormControl(),
11: number: new FormControl(),
12: postal: new FormControl(),
13: }),
14: })
15:
16: **this.myForm.setValue(this.mockData())**
17: }
18:
19: private mockData() {
20: return {
21: basicInfo: {
22: firstName: 'John',
23: lastName: 'Doe',
24: email: 'john@doe.com',
25: age: '76',
26: },
27: address: {
28: street: 'street name',
29: number: '12',
30: postal: '49000',
31: },
32: }
33: }

在前面的示例中，**mockData()** 方法代表 API 响应。

**注意：** mockData() 方法的对象结构与 FormGroup 结构相同。它包含了所有属性，这允许我们使用 setValue()。如果我们不确定对象是否具有所有属性，建议使用 patchValue()。我们预期访问页面并看到带有数据的输入元素。“基本信息”表单字段如下：

![](/cd4d52de62d88033f6a0089db_47_0)

***图 1.9*** *带有数据的基本信息*

地址表单字段如下：

![](/cd4d52de62d88033f6a0089db_47_1)

***图 1.10*** *带有数据的地址*

**setValue()** 方法要求对象具有 FormGroup 的所有属性。如果属性相同，Angular 将抛出错误。例如，如果我们删除第 22 行的属性，我们将得到错误：“必须提供 firstName 值”。

## 响应式表单

在 Angular 中有两种表单：模板驱动表单 (Template-Driven forms) 和响应式表单 (Reactive-Forms)。响应式”这个名字有一个完美的理由，它与用户交互有关。

**注意：** 映射层可以是负责 API 请求和转换的方法集。

![](/cd4d52de62d88033f6a0089db_49_0)

***图 1.11*** 应用程序架构

如果我们有一个包含许多 FormGroup(s)、FormControl(s) 和 FormArray(s) 的复杂表单，语法可能会有点难以理解。我们可以使用 **FormBuilder** 让代码看起来更直观，它提供了语法糖。这是创建 **FormControl**、**FormGroup** 和 **FormArray** 的另一种方法。下表描述了类与 FormBuilder 语法之间的等效性。

| 类语法 | FormBuilder 语法 |
| :--- | :--- |
| new FormControl() | [] or this.fb.control('') |
| new FormGroup() | this.fb.group() |
| new FormArray() | this.fb.array() |

为了使用语法糖，我们需要在组件中注入 **FormBuilder**，如接下来的代码第 11 行所示：

```typescript
import {Component} from '@angular/core';
import {FormBuilder} from '@angular/forms';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {

  constructor(private fb: FormBuilder) {}

}
```

**带有 FormControls 的 FormGroup**

在这里，我们看到表单模型使用类时是什么样的，以及它与 **FormBuilder** 的等效性将如何。

**使用类**

```typescript
this.myForm = new FormGroup({
  firstName: new FormControl(),
  lastName: new FormControl(),
})
```





**使用 FormBuilder**

```javascript
1: this.myForm = this.fb.group({
2: firstName: [],
3: lastName: [],
4:})
```

### 带 FormControl 的 FormArray

在这里，我们看到了使用 **FormGroup**、**FormControl**(s) 和 **FormArray** 类的表单模型，以及它使用 **FormBuilder** 语法时的后的样子。

**使用类**

```javascript
1: this.myForm = new FormGroup({
2: firstName: new FormControl(),
3: lastName: new FormControl(),
4: colors: new FormArray([
5: new FormControl('Red'),
6: new FormControl('Green'),
7: new FormControl('Blue'),
8: ]),
9:})
```

**使用 FormBuilder**

```javascript
1: this.myForm = this.fb.group({
2: firstName: [],
3: lastName: [],
4: colors: this.fb.array([
5: ['Red'],
6: ['Green'],
7: ['Blue'],
8: ]),
9:})
```

**注意：** 我们在数组括号中设置的值（例如 `['Red']`）是 `FormControl` 的默认值。

### 带 FormGroup 的 FormArray

在这里，我们看到了使用 **FormGroup**、**FormControl**(s) 和包含 **FormGroup**(s) 的 **FormArray** 的表单模型，以及它使用 **FormBuilder** 语法时的样子。

**使用类**

```javascript
1: this.myForm = new FormGroup({
2: firstName: new FormControl(),
3: lastName: new FormControl(),
4: colors: new FormArray([
5: new FormGroup({name: new FormControl('Red')}),
6: new FormGroup({name: new FormControl('Green')}),
7: new FormGroup({name: new FormControl('Blue')}),
8: ]),
9:})
```

**使用 FormBuilder**

```javascript
1: this.myForm = this.fb.group({
2: firstName: [],
3: lastName: [],
4: colors: this.fb.array([
5: this.fb.group({name: ['Red']}),
6: this.fb.group({name: ['Green']}),
7: this.fb.group({name: ['Blue']}),
8: ]),
9:})
```

## 结论

在本章中，我们涵盖了所有的响应式表单（Reactive Forms）基础。我们学习了如何构建表单，无论是使用单个表单元素，还是多个表单元素（通过将它们分组或添加到数组中）。所有这些变体都是我们构建表单所需的基础工具。这是一个极好的基础，我们将在此基础上继续精通响应式表单。

## 关键术语

- **FormControl**: 处理每个表单元素的值和有效性的类。
- **formControlName**: 该指令用于从 **FormGroup** 中选择 **FormControl** 并应用与表单元素的绑定。
- **[formControl]**: 将 **FormControl** 实例与表单元素进行绑定的指令。
- **FormArray**: 处理 **AbstractControl** 项数组的值和有效性的类。
- **FormGroup**: 处理一组 **FormControl**、**FormArray** 或嵌套 **FormGroup** 实例的值和有效性的类。
- **FormGroupName**: 该指令通过名称从父级 **FormGroup** 中选择嵌套的 **FormGroup**，并应用与 DOM 元素的绑定。
- **FormArrayName**: 该指令通过名称从父级 **FormGroup** 中选择嵌套的 **FormArray**，并应用与 DOM 元素的绑定。
- **[formGroup]**: 将 **FormGroup** 与 DOM 元素绑定的指令。
- **Form model**: 由 **AbstractControl** 类创建的、代表 HTML 表单结构的模型。
- **FormBuilder**: 为 **FormControl**、**FormArray** 和 **FormGroup** 类提供了语法糖。
- **AbstractControl**: **FormControl**、**FormArray** 和 **FormGroup** 类的基类。

## 问题

**Q: 使用 FormBuilder 可以吗？**

**A: 是的，我们可以通过 [formControl] 指令从 FormGroup 中选择 FormControl 并应用与表单元素的绑定。**（此处上上）

**Q: 这里的 FormBuilder 语法糖可以吗？**

**A: 是的，它为 FormControl、FormArray 和 FormGroup 类提供了语法糖。**

**Q: 在 HTML 元素中进行 FormControl 实例化可以吗？**

**A: 是的，我们可以从源将数据注入到模板中，这是一种单向绑定。**

**Q: 我应该通过 FormGroup 绑定 吗？**

**A: 是的，这是一种单向绑定。**

*(注：由于原文 Q&A 部分存在较多断句和重复，译文已根据上下文逻辑进行了对齐处理，以确保通顺。)*



```typescript
export class AppComponent {
  **isDisabled: boolean** = true;
}
```

在模板中，我们按照如下方式在按钮的 DOM 属性中注入属性 **isDisabled**：

**component.html 代码**
```html
<button type="button" [disabled]="isDisabled">Submit</button>
```

上述绑定将导致浏览器中的按钮呈现为禁用状态。

**注意：** 在在这两个示例中，模板都不会影响源的值。这是一种单向绑定。

**双向**意味着源会将数据注入到模板中，而模板会用数据更新源。这就是双向绑定。在 Angular 中，用数据更新源的功能是事件绑定。

## 事件绑定 (Event binding)

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_58_0.png)
***图 2.3：*** *事件绑定*

事件绑定对于模板与源之间的通信至关重要。通过事件处理器，模板向源发送带有相关信息（事件参数）的事件。

在接下来的示例中，我们将结合事件绑定和插值表达式：

**component.ts 代码**
```typescript
import {Component} from '@angular/core'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  **buttonLabel = 'Submit'**

  submit() {
    this.buttonLabel = 'Submitting...'
  }
}
```

**component.html 代码**
```html
<button type="button" (click)="submit()">
  {{buttonLabel}}
</button>
```

在浏览器首次渲染时，按钮的值将为 "*Submit*”。当用户点击按钮时，值将变为 "*Submitting*…”。这个示例结合了插值表达式和事件绑定，它们都是单向数据绑定——尽管如此，两者的结合实现了双向数据绑定。在 Angular 表单中，双向数据绑定的工作原理与之前的示例类似。

接下来，我们将探索如何在表单中应用数据绑定。首先，我们将解释如何使用原生 JavaScript 实现这一功能。

## 使用原生 JavaScript 进行绑定 (Binding Using Vanilla JavaScript)

在接下来的示例中，我们将使用内置事件处理表单绑定。该示例的用例是在 HTML span 元素上重复 HTML input 元素的值。这种值的重复复现将在每次按键时发生。

**源代码 (javascript)**
```javascript
function inputEventHandler() {
  const value = document.getElementById('inputId').value
  document.getElementById('inputValue').innerHTML = value
}
```

在第 2 行，我们获取输入元素的值，并在第 3 行通过 **innerHTML** 提供它。

**模板代码**
```html
<input type="text" id="inputId" oninput="inputEventHandler()">
<span id="inputValue"></span>
```

在第 1 行，我们在 **oninput** 事件上注册了事件处理器 **inputEventHandler**。该事件会在每次按键时触发，这意味着我们每次在输入框中输入时都会触发。在第 2 行，HTML 元素将重复我们在输入元素中输入的值。

我们使用原生 JavaScript 实现了双向数据绑定。我们可以想象在一个包含多个 HTML input 元素的表单中编写此类代码有多困难。幸运的是，我们不需要自定义实现。让我们看看如何使用 Angular 绑定实现相同的功能。

## 使用 Angular 语义进行绑定 (Binding using Angular Semantics)

在接下来的示例中，我们将使用 Angular 实现与之前原生 JavaScript 示例相同的功能：

**component.ts 代码**
```typescript
import {Component} from '@angular/core'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  inputValue = ''

  inputEventHandler(value) {
    this.inputValue = value
  }
}
```

在第 12 行，我们获取输入元素的值，并将其赋值给 **inputValue** 类属性。

**component.html 代码**
```html
<input type="text" (input)="inputEventHandler($event.target.value)" [value]="inputValue">
<span>{{inputValue}}</span>
```

在第 2 行，我们在 input 事件上注册了事件处理器 **inputEventHandler**，该事件会在每次按键时触发。这是从模板到源的单向绑定。在第 4 行，HTML 元素将重复我们在输入元素中输入的值。请注意，我们使用了插值表达式，这是另一种从源到模板的单向绑定。因此，我们使用 Angular 实现了双向数据绑定。

## 使用响应式表单绑定 (Binding using Reactive Forms)

幸运的是，在响应式表单（Reactive Forms）中，我们不需要手动处理从源到模板及反向通信。**formControl** 和 **formControlName** 指令解决了绑定问题。

在上一章节，我们学习了如何绑定输入元素。在接下来的示例中，我们将看到如何使用响应式表单实现这一功能。

**component.ts 代码**
```typescript
import {Component} from '@angular/core'
import {FormControl} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  name = new FormControl('John')
}
```

**component.html 代码**
```html
<input type="text" [formControl]="name">
<span>{{name.value}}</span>
```

这个示例的精彩之处在于，我们没有使用任何事件绑定来建立模板与源之间的通信！

## 单选框绑定 (Data bind radio buttons)

绑定与 input 类型不同，因为单选框通常成组使用，这意味着用户可以选择一个值。在接下来的章节中，我们将看到绑定单选框的示例，可以使用 **formControl** 或 **formControlName** 指令。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_63_0.png)
***图 2.4：*** *单选框示例*

#### 使用 [formControl] 指令

在下面的代码中，我们创建一个 FormControl 实例并使用 **formControl** 指令将其应用于单选框。我们通过在两个元素中设置相同的 name 来对单选框进行分组。它们都具有 **name="frontDev"**，但值不同。

如果用户点击第一个单选框，我们将更新为 "1"。如果用户点击第二个单选框，我们需要将 **frontDev FormControl** 的值更新为 "2"。

请注意，在两种情况下，我们更新的同一个 FormControl 的值！

**component.html 代码**
```html
<label>I am a front-end developer</label>
<div>
  <label for="yesFrontEnd">Yes</label>
  <input id="yesFrontEnd"
    type="radio"
    [formControl]="frontDev"
    name="frontDev"
    value="1">
</div>
<div>
  <label for="noFrontEnd">No</label>
  <input id="noFrontEnd"
    type="radio"
    [formControl]="frontDev"
    name="frontDev"
    value="2">
</div>
```

### 使用 [formControlName] 指令

我们可以通过将 FormControl 嵌套在 FormGroup 中来应用与之前相同的功能。在下面的代码中，我们使用 FormBuilder 语法糖来实现：

**component.ts 代码**
```typescript
import {Component, OnInit} from '@angular/core'
import {FormBuilder, FormGroup} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
```



```typescript
templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent implements OnInit {
  myForm!: FormGroup

  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.myForm = this.fb.group({
      frontEndDev: this.fb.control(null),
    })
  }
}
```

**提示：** 在 `FormBuilder` 中，`FormControl` 等同于 `[]` 和 `this.fb.control(null)`。让我们看看后续代码中如何使用 **formControlName** 指令：

**component.html 代码**
```html
<label>我是一名前端开发人员</label>
<div [formGroup]="myForm">
  <div>
    <label for="yesFrontEnd">是</label>
    <input id="yesFrontEnd"
           type="radio"
           formControlName="frontEndDev"
           name="frontEndDev"
           value="1">
  </div>

  <div>
    <label for="noFrontEnd">否</label>
    <input idnonoFrontEnd"
           type="radio"
           formControlName="frontEndDev"
           name="frontEndDev"
           value="2">
  </div>
</div>
```

在第 7 行和第 16 行中，我们使用 **formControlName** 指令从 **FormGroup** 中通过名称 **frontEndDev** 请求 **FormControl**。

### 设置默认值

单选按钮上的默认值表示在初次渲染时预先选择哪个选项，如图所示：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_66_0.png)

***图 2.5：*** *带有默认值的单选按钮示例*

为了实现这一点，默认值应该与我们在 HTML 的 `value` 属性中声明的值相似。

例如，如果单选按钮中的值为 1 和 2（正如我们在之前的代码第 9 行和第 18 行中所做的那样），我们应该提供其中一个作为默认值。

在初始化 **FormControl** 时设置数据，我们必须在第一个参数中填充一个值，如下例所示：

1. **frontEndDev: this.fb.control('1')** — 在 FormControl 中提供值 "1" 将勾选标签为“是”的第一个单选按钮。
2. **frontEndDev: this.fb.control('2')** — 在 FormControl 中提供值 "2" 将选中标签为“否”的第二个单选按钮。

## 复选框（Checkbox）数据绑定

复选框元素接受布尔值类型。它可以是 "true"，使复选框处于选中状态；也可以是 "false"，使复选框未被选中。

与通常成组使用且仅允许选择一个的单选按钮相比，复选框可以有多个元素处于选中状态。

在接下来的章节中，我们将看到如何通过 **formControl** 指令或 **formControlName** 指令对复选框进行数据绑定——这些示例的结果将是：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_67_0.png)

***图 2.6：*** *复选框示例*

#### 使用 [formControl] 指令

在以下代码中，我们创建了一个 **FormControl** 实例，并使用 **formControl** 指令与复选框进行绑定。

**component.ts 代码**
```typescript
import {Component} from '@angular/core'
import {FormControl} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  termsAndConditions = new FormControl()
}
```

由于 **FormControl** 实例没有提供值，HTML 中的复选框将是未选中状态。

在下面的 HTML 中，我们在复选框元素中绑定了 **FormControl**：

**component.html 代码**
```html
<input type="checkbox"
       id="termsAndConditions"
       [formControl]="termsAndConditions">

  <label for="termsAndConditions">我接受条款和条件</label>
```

在第 3 行中，我们使用 **formControl** 指令应用复选框的绑定，**termsAndConditions** **formControl** 的值将是：
- 如果用户勾选复选框，则为 **true**
- 如果用户取消勾选复选框，则为 **false**

#### 使用 formControlName 指令

我们可以实现与使用 **formControl** 指令相同的功能，但这次我们将把 **FormControl** 嵌套在 **FormGroup** 中，如下代码所示，并使用了 **FormBuilder** 语法糖：

**component.ts 代码**
```typescript
import {Component, OnInit} from '@angular/core'
import {FormBuilder, FormGroup} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent implements OnInit {
  myForm!: FormGroup

  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.myForm = this.fb.group({
      termsAndConditions: this.fb.control(null),
    })
  }
}
```

在第 16 行中，**FormControl** 提供的值是 null。在接下来的代码中，我们通过 **formControlName** 指令在 **FormGroup** 中使用复选框元素来绑定 **FormControl**：

**component.html 代码**
```html
<div [formGroup]="myForm">
  <input type="checkbox"
         id="termsAndConditions"
         formControlName="termsAndConditions">

  <label for="termsAndConditions">我接受条款和条件</label>
</div>
```

在第 4 行中，我们使用 **formControlName** 指令应用复选框的绑定，**termsAndConditions** 的值将是：
- 如果用户勾选复选框，则为 **true**
- 如果用户取消勾选复选框，则为 **false**

### 设置默认值

复选框的默认值表示在初次渲染时预先选中哪个选项，如图所示：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_69_0.png)

***图 2.7：*** *带有默认值的复选框示例*

为了实现这一点，默认值应该与我们在 HTML 的 `value` 属性中声明的值相似。

例如，如果单选按钮中的值为 1 和 2（正如我们在之前的代码第 9 行和第 18 行中所做的那样），我们应该提供其中一个作为默认值。

在初始化 **FormControl** 时设置数据，我们必须在第一个参数中填充一个值，如下例所示：

1. **frontEndDev: this.fb.control('1')** — 在 FormControl 中提供值 "1" 将勾选标签为“是”的第一个单选按钮。
2. **frontEndDev: this.fb.control('2')** — 在 FormControl 中提供值 "2" 将选中标签为“否”的第二个单选按钮。

虽然复选框接受布尔值，但本质上 Angular 使用隐式类型转换将值转换为布尔值。每个真值都会勾选复选框，每个假值都会让复选框未被选中。

我们在 **FormControl** 初始化或 `setValue`/`patchValue` 方法中使用真值和假值：

1. **termsAndConditions = new FormControl(true)** — 在 FormControl 中提供值 true 将选中复选框。
2. **termsAndConditions: this.fb.control(null)** — 在 FormControl 中提供值 null 将使复选框未被选中。

在下面的表格中，我们看到真值和假值的示例：

| 各种值的 FormControl | 是否选中 |
| :--- | :--- |
| termsAndConditions = new FormControl() | 否 |
| termsAndConditions = new FormControl(true) | 是 |
| termsAndConditions = new FormControl("true") | 是 |
| termsAndConditions = new FormControl("false") | 是 |
| termsAndConditions = new FormControl(false) | 否 |
| termsAndConditions = new FormControl([]) | 是 |
| termsAndConditions = new FormControl({}) | 是 |
| termsAndConditions = new FormControl(null) | 否 |
| termsAndConditions = new FormControl(undefined) | 否 |

***表 2.1***

请注意，将 **FormControl** 替换为 **FormBuilder** 语法糖具有相同的结果。

## 下拉列表（select element）数据绑定

虽然构建下拉菜单看起来很简单，但由于其数据源可能是字符串数组或对象数组，它比较特殊。当我们选择一个单选按钮时，会在相应的 **formControl** 中设置单选按钮的值。同样，当我们勾选或取消勾选复选框时，会在相应的 **formControl** 中设置布尔值。

在后续章节中，我们将看到如何使用单个 **FormControl** 为下拉菜单绑定三个选项，如图 2.8 所示。请注意 **formControlName** 指令的用法与之前的 HTML 元素类似。

#### 带有预定义选项的用例

通过“预定义”，是指直接在 HTML 中硬编码 **Select** 选项。




在下面的示例中，我们创建了一个 **FormControl** 实例，并在模板中使用它来与 **Select** 元素进行绑定：

**component.ts 代码**

1: import {Component} from '@angular/core'
2: import {FormControl} from '@angular/forms'
3:

4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8:})
9: export class AppComponent {
10: myColor = new FormControl()
11: }

让我们来看看如何在 HTML 中设置带有 value 属性的预定义 **Select** 选项示例：

**component.html 代码**

1: <label>选择你的颜色</label>
2: <select [formControl]="myColor" >
3: <option value="1">红色</option>
4: <option value="2">绿色</option>
5: <option value="3">蓝色</option>
6: </select>

我们设置了三个预定义选项，每个选项都有一个 value 属性。在第 2 行，我们使用了 **formControl** 指令，它将 **Select** 菜单与 **myColor formControl** 实例绑定。

当用户选择一个 **Select** 选项时，所选选项的值将赋值给 **myColor formControl**。例如，如果用户选择了绿色，**myColor** 将获得值 2。

### 设置默认值

**Select** 菜单的默认值表示在浏览器中显示的选项，如下图所示：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_73_0.png)

***图 2.9：*** *带有默认值的 Select 菜单示例*

要设置默认值，我们应该在初始化 **formControl** 实例时，传入我们想要选中的选项相应的 **value**。

例如，如果我们想选中“绿色”选项，我们必须提供值 2，如下所示：

**component.ts 代码**

1. myColor = new FormControl(2)

### 不带值的预定义选项用例

以下代码与上一个示例类似，但 **Select** 选项中没有 value 属性。

**component.html 代码**

1: <label>选择你的颜色</label>
2: <select [formControl]="myColor" >
3: <option>红色</option>
4: <option>绿色</option>
5: <option>蓝色</option>
6: </select>

当用户选择一个 **Select** 选项时，所选选项的 label 将赋值给 **myColor formControl**。例如，如果用户选择了“绿色”，**formControl** 将获得值 "Green"。

### 设置默认值

要设置默认值，我们应该在初始化 **formControl** 实例时，传入我们想要选中的选项相应的 label。例如，如果我们想选中“*Green*”选项，我们必须提供值“*Green*”，如下所示：

**component.ts 代码**

1. myColor = new FormControl('Green')

### 字符串数组选项用例

HTML 中并不总是有预定义值。我们可能需要从一个数组中获取数据，并使用 ***ngFor*** 创建选项。在下面的示例中，我们将构建一个包含三种颜色的 Select 菜单，但这次我们将从数组中获取数据。

**component.ts** 中的代码与之前的示例类似，唯一的区别是我们必须设置一个字符串数组，如下所示：

**component.ts 代码**

1. colors = ['Red', 'Green', 'Blue']

在接下来的 HTML 代码中，我们将遍历该数组以构建选项：

**component.html 代码**

1: <label>选择你的颜色</label>
2: <select [formControl]="myColor">
3: <option [ngValue]="null">选择</option>
4: <option *ngFor="let color of colors" [ngValue]="color">
5: {{color}}
6: </option>
7: </select>

在第 3 行中，我们使用了带有 null 值的 **ngValue** 指令，它在选中时会清除任何之前赋值过的值。

在第 4 行中，我们使用 ***ngFor*** 遍历数组，生成三个选项。我们仍然在 **ngValue** 指令中设置了变量 `color`，这似乎与 **{{color}}** 插值值是多余的，但我们需要它来帮助我们分配一个默认值。

### 设置默认值

无论是遍历数组还是使用预定义选项，选择选项的机制都是相同的。例如，如果我们想选中 label 为“*Green*”的选项，我们提供值“*Green*”，如下：

**component.ts 代码**

myColor = new FormControl('Green')

### 对象数组选项用例

现在让我们看看如何遍历对象数组。代码与之前的示例类似，唯一的区别在于我们需要设置一个字符串数组，如下所示：

**component.ts 代码**

1. colors = ['Red', 'Green', 'Blue']

在接下来的 HTML 代码中，我们将遍历数组来构建选项：

**component.html 代码**

1: <label>选择你的颜色</label>
2: <select [formControl]="myColor">
3: <option [ngValue]="null">选择</option>
4: <option *ngFor="let color of colors" [ngValue]="color">
5: {{color}}
6: </option>
7: </select>

在第 3 行中，我们使用了带有 null 值的 **ngValue** 指令，它在选中时会清除任何之前赋值过的值。例如，如果用户选择了绿色，**formControl** 将获得值 "Green"。

### 设置默认值

要设置默认值，我们应该在初始化 **formControl** 实例时，传入我们想要选中的选项相应的 label。例如，如果我们想选中“*Green*”选项，我们必须提供值“*Green*”，如下所示：

**component.ts 代码**

1. myColor = new FormControl('Green')




**A.** 在 HTML 表单中，我们经常会在表单无效、处于 pristine（初始）³状态或任何符合应用需求的其他状态组合时禁用按钮。我们使用 [disable] 属性绑定来禁用它。

¹1 有关 Angular 绑定的更多信息，请访问 https://angular.io/guide/binding-syntax。
2 类型强制转换（Type coercion）是将一种数据类型转换为另一种数据类型的过程 https://developer.mozilla.org/en-US/docs/Glossary/Type_coercion
3 pristine 表示表单尚未被用户修改 - https://angular.io/api/forms/AbstractControl#pristine。

# 第 3 章
## 内置验证器

### 简介
在之前的章节中，我们学习了构建 Angular 响应式表单（Reactive Form）的基础。为了补充已学知识，我们需要在 UI 和终端用户之间建立通信通道。让用户知道表单字段中填写的数据是否正确至关重要。在本章中，我们将学习如何在 `FormControl(s)` 上注册内置验证器，并告知用户任何错误的数据输入。

### 结构
- 为什么要使用验证器？
- 控件中的有效性
- 内置验证器
- FormControl 验证器
- FormGroup 验证器
- 访问 FormGroup 的控件
- FormArray 验证器
- 访问 FormArray 的控件
- 在控件中使用 AbstractControl 属性
- updateOn 选项
- AbstractControl 属性与 CSS

### 目标
读完本章后，你将学习如何通过在 **FormControl** 实例中应用内置验证器，与终端用户建立通信并并在服务器端维护数据完整性。

## 为什么要使用验证器？
如果我们必须在纸质表单上填写数据，我们可能会疑惑是否需要填写所有字段。如果可能，我们会寻求帮助；如果不可，我们将把纸质表单提交给相应的实体办公室，并等待确认。他们可能会要求我们填写某些特意留空的字段，或者可能要求我们在某些字段中编写的字符数量不要超过特定限制。

当然，在数字时代这种情况不应该发生，因为我们可以立即对终端用户做出响应。

通过验证，我们可以：
- 与终端用户建立通信
- 确保服务器端的数据完整性

这两者是互相关联的。我们与用户通信以告知他们表单的“*规则*”。由于用户遵守规则，我们在服务器上将拥有正确的数据，从而保证数据完整性。

## 控件中的有效性
在*第 1 章：响应式表单入门*中，我们提到 **AbstractControl** 会计算值和有效性。具体来说：
- **FormControl** 处理单个元素的值和有效性。
- **FormGroup** 处理一组 **AbstractControl** 实例的值和有效性。
- **FormArray** 处理一个 **AbstractControl** 实例数组的值和有效性。

有效性（validity）描述 **AbstractControl** 是否有效，该值可以通过 `.valid` 属性获取。在图 3.1 中，我们看到了一些字段。“Name”字段是必填的，绑定的 **FormControl** 的有效性为 `false` (`valid=false`)。如果我们在字段上输入任何字符，有效性将从 `valid=false` 切换到 `valid=true`。默认情况下，有效性会在每次击键时重新计算。

图 3.1：带有验证错误消息的表单

**AbstractControl** 实例拥有在验证过程中非常有用的属性。下表描述了这些属性：

| 属性 | 类型 |  |
| :--- | :--- | :--- |
| VALIDITY | valid | 布尔。如果控件满足所有验证规则，则为有效。 |
| | invalid | 布尔。如果控件不满足所有验证规则，则为无效。 |
| VISITED | touched | 布尔。当用户触发失去事件时，控件被标记为已触碰（touched）。这是一个不可逆的值。一旦被触碰，就无法恢复。 |
| | untouched | 布尔。未触碰（untouched）是控件的默认状态。这是一个不可逆的值。一旦被设置为 false，就无法恢复。 |
| VALUE | pristine | 布尔。如果用户尚未更改值，则控件为初始状态（pristine）。这是一个不可逆的值。一旦被设置为 false，就无法恢复。 |
| | dirty | 布尔 | 如果用户更改了值，则控件为已脏（dirty）。这是一个不可逆的值。一旦被标记为脏，就无法恢复。 |

表 3.1

## 内置验证器
根据业务规则，HTML 表单可能对每个表单字段有限制。某些字段可能是必填的，而另一些字段可能有不同的规则。例如，用户可能会误输电子邮件地址或留空某个必填字段。在 HTML 开发中，这些限制被称为验证。在下表中，我们看到了内置验证器的列表及其含义：

| 验证器 | 满足条件时有效 |
| :--- | :--- |
| min(min: number) | 值 >= 提供的数字 |
| max(max: number) | 值 <= 提供的数字 |
| required() | 值不空 |
| requiredTrue() | 值为 True |
| email() | 值是有效的电子邮件格式 |
| minLength(minLength: number) | 值的长度 >= 提供的长度 |
| maxLength(maxLength: number) | 值的长度 <= 提供的最小长度 |
| pattern(pattern: string) | 值匹配正则表达式模式 |

表 3.2

## FormControl 验证器
**FormControl** 类接受两个参数，正如我们已经学过的，第一个参数是控件的默认状态。第二个参数接受单个验证或验证器数组。请注意，第二个参数在 **FormControl** 类或 **FormBuilder** 语法糖中均适用。

在下面的代码中，我们看到了如何在 **FormControl** 实例上设置验证器：

component.ts 代码 (使用 FormControl 类)
```typescript
import {Component} from '@angular/core'
import {FormControl, Validators} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  firstName = new FormControl('', Validators.required)
  lastName = new FormControl('', [
    Validators.required,
    Validators.minLength(3),
  ])
}
```

在第 2 行中，我们导入了 Validators，在第 10 和 11 行中，我们为 "firstName" 和 "lastName" 表单字段注册了验证器。请注意，“lastName”字段的第二个参数是一个包含多个验证器的数组。正如我们所说，设置单个验证器或验证器数组都是有效的。

在下面的代码中，我们看到了之前相同的示例，但使用了 **FormBuilder** 语法糖：

component.ts 代码 (使用 FormBuilder)
```typescript
import {Component} from '@angular/core'
import {FormBuilder, Validators} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent {
  firstName = this.fb.control('', Validators.required)
  lastName = this.fb.control('', [
    Validators.required,
    Validators.minLength(3),
  ])

  constructor(private fb: FormBuilder) {}
}
```





![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_85_0.png)

***图 3.2:*** *AbstractControl 属性*

在下面的代码中，我们看到如何访问有效性属性 
并为特定控件显示错误消息：

**component.html 代码**

1: <input type="text"
2: placeholder="First Name"
3: [formControl]="firstName" />
4:
5: <small *ngIf="firstName.invalid">Field is required</small>
6:
7: <input type="text"
8: placeholder="Last Name"
9: [formControl]="lastName" />

在第 5 行中，我们设置了一个条件，如果“**First Name**”无效，则向用户显示错误消息。由于我们只为 **firstName** 控件注册了必填（必填）验证器，因此使用 `invalid` 属性来显示关于该字段为必填的消息是安全的。

该属性的值将仅由必填验证器发生改变。

然而，如果我们有多个验证器（如“**Last Name**”字段所示），我们无法确定 **.valid** 或 **.invalid** 属性是由 **required** 还是 **minLength** 验证器改变的，因为这两者都会影响控件的有效性。在这种情况下，我们必须使用 **.errors** 属性，这是一个由未满足的验证器生成的对象。

由于 **lastName** 控件拥有 **required** 和 **minLength** 验证器，**.errors** 属性将生成以下对象：

| 验证器 | 生成的错误对象 |
| :--- | :--- |
| required | `{"required": true}` |
| minLength | `{"minlength": {"requiredLength": 3, "actualLength": 1}}` |

***表 3.3***（上表内容）

**.errors** 属性非常有用，因为我们可以根据不同情况设置不同的验证消息。

下面的代码在 **required** 或 **minLength** 验证器未被满足时会显示不同的消息：

**component.html 代码**

1: <input type="text"
2: placeholder="First Name"
3: [formControl]="firstName" />
4:
5: <small *ngIf="firstName.invalid">Field is required</small>
6:
7: <input type="text"
8: placeholder="Last Name"
9: [formControl]="lastName" />
10:
11: <small *ngIf="lastName.errors?.minlength">The length of this field is {{lastName.errors?.minlength.requiredLength}}</small>
12: <small *ngIf="lastName.errors?.required">Field is required</small>

在第 12–14 行中，如果 **minLength** 验证器未被满足，我们将显示消息“*此字段的长度为 3*”。

在第 15–17 行中，如果 **required** 验证器未被满足，我们将显示一条消息。

**注意：** 在组件模板中string **errors** 属性时，建议使用安全导航操作符（也称为 Elvis 运算符 (?)）。如果我们忽略了它，将得到类似于“*Cannot read property 'required' of null.*”的错误。

**FormGroup**

**FormGroup** 与 **FormControl** 类似，它扩展了 **AbstractControl** 类并包含了我们在*表 3.1*中看到的所有属性。然而，用户无法直接触发 **FormGroup**。嵌套的 **FormControl** 实例的任何更改都会冒泡并改变 **FormGroup**，如如下图所示：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_88_0.png)

***图 3.3:*** *FormControl 状态冒泡*

让我们看看它是如何工作的。下面的表显示了一个树形结构，包含根节点 (**myForm**) 和子节点 (**firstName** 和 **lastName**)。

| AbstractControl 实例 | 类型 |
| :--- | :--- |
| myForm | FormGroup |
| firstName | FormControl |
| lastName | FormControl |

***表 3.4***（上表内容）

我们假设所有定义的 **FormControl** 实例都是必填的。对于这个示例，我们将关注 **.valid** 属性。首先，所有控件处于默认状态，如下如下：

| AbstractControl 实例 | .valid 属性 |
| :--- | :--- |
| myForm | False |
| firstName | False |
| lastName | False |

***表 3.5***（上表内容）

然后，用户满足了 **firstName** 的验证器，导致：

1. **firstName FormControl** 的 .valid 属性变为 true。
2. **lastName FormControl** 的 .valid 属性保持为 false。
3. **myForm FormGroup** 的 .valid 属性也保持为 false。

当所有嵌套的 **FormControl** 都为 true 时，FormGroup 的有效性才会变为 true。

| AbstractControl 实例 | .valid 属性 |
| :--- | :--- |
| myForm | False |
| firstName | True |
| lastName | False |

***表 3.6***（上表内容）

最后，用户满足了 **lastName** 验证器，因为所有嵌套的 **FormControl** 都为 true，FormGroup 的有效性变为 true。

| AbstractControl 实例 | .valid 属性 |
| :--- | :--- |
| myForm | True |
| firstName | True |
| lastName | True |

***表 3.7***（上表内容）

在下面的代码中，我们看到 FormControl 的状态如何冒泡并更新 **FormGroup**：

**component.ts 代码**

1: import {Component, OnInit} from '@angular/core'
2: import {FormBuilder, FormGroup, Validators} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8: })
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup
11:
12: constructor(private fb: FormBuilder) {}
13:
14: ngOnInit(): void {
15: this.myForm = this.fb.group({
16: firstName: ['', Validators.required],
17: lastName: ['', [Validators.required, Validators.minLength(3)]],
18: })
19: }
20: }

在前面的代码中，我们看到 **firstName** 和 **lastName** 都是必填控件，同样，**lastName** 拥有一个 **minLength** 验证器。

**component.html 代码**

1: <form [formGroup]="myForm">
2:
3: <input type="text"
4: placeholder="First Name"
5: formControlName="firstName" />
6:
7: <input type="text"
8: placeholder="Last Name"
9: formControlName="lastName" />
10:
11: <small *ngIf="myForm.invalid">The form is invalid</small>
12:
13: </form>

在第 11 行中，我们有一个条件，当表单无效时向用户显示消息。请注意 **FormGroup** 本身没有验证规则。**.invalid** 属性是从子 **FormControl** 的状态计算出的。

**访问 FormGroup 的控件**

我们学习了当单个 **FormControl** 无效时如何显示消息。在本节中，我们将学习从 **FormGroup** 查询 **FormControl**。为了实现这一点，我们可以通过以下两种方式：

1. **formGroup.controls.formControl.property**: 第一种方案是使用点符号。正如*图 3.3*所示，我们需要将 **FormGroup**、**formControl** 和属性替换为相应的值 (**myForm.controls.firstName.invalid**）。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_92_0.png)

***图 3.4:*** *通过 FormGroup 和 FormControl 选择属性*

2. **formGroup.get('formControl')?.property**: 第二种方案是使用 get 方法。正如*图 3.4*所示，我们需要将 **FormGroup**、**formControl** 和属性替换为相应的值 (**myForm.get('firstName')?.invalid**)。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_92_1.png)

***图 3.5:*** *通过 FormGroup 和 FormControl 使用 get 方法*

请注意 **formControl** 应该是一个字符串。

在下面的代码中，我们看到当嵌套的 **FormControl** 实例无效时如何显示消息：

**component.html 代码**

1: <form [formGroup]="myForm">
2:
3: <input type="text"
4: placeholder="First Name"
5: formControlName="firstName" />
6:
7: <small *ngIf="myForm.controls.firstName.invalid">Required field</small>
8:
9: <input type="text"
10: placeholder="Last Name"
11: formControlName="lastName" />
12:
13: <small *ngIf="myForm.controls.lastName.invalid">Required field</small>
14:
15: </form>





![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_94_0.png)

***图 3.6:*** *FormArray 的状态会被改变并向上冒泡*

让我们来看看它是如何工作的。下表显示了一个树形结构格式，其中包含 **FormGroup** 根节点以及子节点 **FormControl** 和 **FormArray** 实例：

| AbstractControl 实例 | AbstractControl 类型 |
| :--- | :--- |
| myForm | FormGroup |
| colors | FormArray |
| {array item} | FormGroup |
| Name | FormControl |

***表 3.8***

我们假设所有定义的 **FormControl** 实例都是必填的。在这个示例中，我们将关注 **.valid** 属性。

首先，所有控件都有默认状态，因此 **.valid** 属性为 false，如下所示：

| AbstractControl 实例 | .valid 属性 |
| :--- | :--- |
| myForm | False |
| colors | False |
| {array item} | False |
| Name | False |

***表 3.9***

然后，用户满足了 **Name formControl** 的验证器，这导致了以下结果：

- **Name FormControl** 的 **valid** 属性将变为 true
- **父级 FormGroup** (array item) 的 ..**valid** 属性将变为 true
- **colors FormArray** 的 ..**valid** 属性将变为 true
- **myForm FormGroup** 的 **.valid** 属性将变为 true

| AbstractControl 实例 | .valid 属性 |
| :--- | :--- |
| myForm | True |
| colors | True |
| {array item} | True |
| Name | True |

***表 3.10***

在第一章中，我们学习了 **FormArray** 可以由 **FormControl** 或 **FormGroup** 实例组成。在当前示例中，**FormArray** 由 **FormGroup** 实例组成，这就是为什么 {array item} 继承其 **FormControl** 子节点的状态。

在下面的中，我们看到了前一个示例的 Form 模型：

**component.ts 代码**

```typescript
1: import {Component, OnInit} from '@angular/core'
2: import {FormArray, FormBuilder, FormGroup, Validators} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: templateUrl: './app.component.html',
7: styleUrls: ['./app.component.scss'],
8:})
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup
11:
12: get colors() {
13: return this.myForm.get('colors') as FormArray
14: }
15:
16: constructor(private fb: FormBuilder) {}
17:
18: ngOnInit(): void {
19: this.myForm = this.fb.group({
20: colors: this.fb.array([
21: this.getFormArrayItem('Red'),
22: this.getFormArrayItem(),
23: ]),
24: })
25: }
26:
27: private getFormArrayItem(value?: string) {
28: return this.fb.group({
29: name: [value, Validators.required],
30: })
31: }
32:}
```

现在让我们来看看如何检查根节点 **FormGroup** 的有效性。

**component.html 代码**

```html
1: <form [formGroup]="myForm">
2:
3: <ng-container formArrayName="colors">
4: <div *ngFor="let color of colors.controls; let idx = index">
5: <ng-container [formGroupName]="idx">
6: <input type="text" formControlName="name" />
7: </ng-container>
8: </div>
9: </ng-container>
10:
11: <small *ngIf="myForm.invalid">
12: The form is invalid
13: </small>
14: </form>
```

在第 11-13 行中，我们检查根 **FormGroup** 的有效性并显示错误消息。

**访问 FormArray 的控件**

我们已经学习了如何为嵌套在 **FormGroup** 中的 FormControl(s) 显示错误消息。在本节中，我们将学习如何为嵌套在 **FormArray** 中的 **FormGroup** 里的深层 FormControl(s) 显示错误消息。

让我们看看如何检查 **FormArray** 部分每个 **FormControl** 实例的有效性状态：

**component.html 代码**

```html
1: <form [formGroup]="myForm">
2:
3: <ng-container formArrayName="colors">
4: <div *ngFor="let color of colors.controls; let idx = index">
5: <ng-container [formGroupName]="idx">
6: <input type="text" formControlName="name" />
7: <small *ngIf="color.get('name')?.invalid">
8: Required field
9: </small>
10: </ng-container>
11: </div>
12: </ng-container>
13:
14: </form>
```

在第 4 行中，我们遍历 colors 数组的数组项（它们是 **FormGroup** 实例），并将每个 **FormGroup** 赋值给变量 color。

在第 7 行中，我们从当前的 **FormGroup** 中获取 **FormControl**。我们设置了一个条件，如果 **FormControl** 无效，则向用户显示消息。

**注意：** 类似于 .invalid 属性；我们可以使用任何其他 AbstractControl 属性，例如 .touched、.untouched 等。

由于有效性状态会向上冒泡，我们可以设置不同的条件来检查 **FormControl**、**FormArray** 或根 **FormGroup** 的状态。

在下面的代码中，我们看到了如何检查 **FormArray** 的有效性状态：

**component.html 代码**

```html
1: <form [formGroup]="myForm">
2:
3: <ng-container formArrayName="colors">
4: <div *ngFor="let color of colors.controls; let idx = index">
5: <ng-container [formGroupName]="idx">
6: <input type="text" formControlName="name" />
7: </ng-container>
8: </div>
9: </ng-container>
10:
11: <small *ngIf="colors.invalid">
12: All fields are required
13: </small>
14: </form>
```


每个 **AbstractControl** 属性都有一个对应的 CSS 类，该类会自动附加到 HTML 元素上。例如，如果一个控件是 **valid**（有效的），则 **ng-valid** CSS 类将自动附加到相应的 HTML 元素中。

在下表中，我们看到了与 **AbstractControl** 属性对应的 CSS 类。

| 属性 | CSS 类 |
| :--- | :--- |
| valid | ng-valid |
| invalid | ng-invalid |
| touched | ng-touched |
| untouched | ng-untouched |
| pristine | ng-pristine |
| dirty | ng-dirty |
| pending | ng-pending |

***表 3.11***

这些 CSS 类非常有用，因为我们可以编写全局 CSS 规则来装饰（例如）无效的输入字段。在接下来的代码中，我们将看到如何为无效（invalid）且被修改（dirty）的 HTML 输入字段添加边框。

**component.css 代码**
```css
1: input.ng-invalid.ng-dirty {
2: border: 1px solid red;
3:}
```

为了理解 CSS 类的工作原理，让我们来看并检查我们在“*FormArray Validators*”章节中看到的示例表单的 HTML 代码。

**component.html 代码**
```html
1: <form [formGroup]="myForm">
2:
3: <div formArrayName="colors">
4: <ng-container *ngFor="let _ of colors.controls; let idx = index">
5: <div [formGroupName]="idx">
6: <input type="text" formControlName="name" />
7: </div>
8: </ng-container>
9: </div>
10:
11: </form>
```

在第 1 行中，我们用 [**formGroup**] 指令绑定表单元素，Angular 会自动在生成的代码中附加 CSS 类。

第 3 行和第 5 行的 div 元素以及第 6 行的输入字段也是如此。每当我们使用指令对 HTML 表单字段应用绑定时，Angular 都会向生成的代码中附加 CSS 类。

**注意：** 在前面的代码中，我们使用了 `<div>` 标签而不是 `<ng-container>` 标签。由于 `<ng-container>` 不附加任何 DOM 元素，我们将无法获得附加的 CSS 类。

让我们看看生成的代码：

**生成的 HTML 代码**
```html
1: <form class="ng-untouched ng-pristine ng-invalid">
2: <div formarrayname="colors" class="ng-untouched ng-pristine ng-invalid">
3: <div class="ng-untouched ng-pristine ng-invalid">
4: <input type="text"
5: formcontrolname="name"
6: class="ng-untouched ng-pristine ng-invalid" />
7: </div>
8:
9: <div class="ng-untouched ng-pristine ng-invalid">
10: <input type="text"
11: formcontrolname="name"
12: class="ng-untouched ng-pristine ng-invalid" />
13: </div>
14: </div>
15: </form>
```

当我们用任何 Angular 响应式表单指令（**[formGroup]**、**formArrayName**、**[formGroupName]**、**formControlName**）绑定 HTML 元素时，Angular 会自动附加 CSS 类。

## 结论

我们学习了如何使用 **AbstractControl** 属性以及它们有多么有用。我们可以设置各种条件来捕捉不同的业务和用例。我们还学习了可以通过验证在服务器端实现数据完整性，并且正在与最终用户建立通信。在下一章中，我们将继续探索验证器；学习如何构建自定义验证器以应对更高级的用例。

## 关键术语

- **Valid**: 一个布尔属性，表示控件是否有效。
- **Invalid**: 一个布尔属性，表示控件是否无效。
- **Touched**: 表示控件是否已被触碰（点击并失去焦点）。
- **Untouched**: 表示控件是否未被触碰。
- **Pristine**: 表示控件是否处于“纯净”状态（未被修改）。
- **Dirty**: 表示控件是否已被修改过。
- **Pending**: 表示验证正在进行中。




让我们拆解键值对并分别分析每个部分。

## ValidationErrors - key（键）

在 HTML 模板中，我们可以通过检查错误类型向用户条件地显示错误消息。我们通过利用 **AbstractControl** 实例的 **error** 属性来实现。然而，如果我们想为特定的验证器显示特定的消息，例如 **minLength**，我们可以像下面的代码中那样写一个条件：

```html
<small *ngIf="yourControlName.errors?.minlength">
  给用户的消息
</small>
```

同样，如果我们想为自定义验证器显示错误消息，我们使用“*key*”（键）名称。在上面的骨架代码第 9 行中，我们返回了键名 **validatorName**。因此，如果我们想在验证器未满足条件时显示错误消息，可以如下操作：

```html
<small *ngIf="yourControlName.errors?.validatorName">
  给用户的消息
</small>
```

## ValidationErrors - value（值）

“*value*”值包含了我们可能想要显示给用户的有用信息。例如，**Validators.minLength(3)** 返回一个具有以下对象属性的对象：

- **RequiredLength**：这是一个数字，代表该验证器需要满足的长度。
- **ActualLength**：这是一个数字，代表 FormControl 当前的长度。

我们可以使用这些信息向用户显示更有意义的错误消息。如果我们想显示消息“**当前长度为 '1'，但至少需要为 '3'*”，我们可以使用类似下面的代码：

```html
<small *ngIf="firstName.errors?.minlength">
  当前长度为'{{firstName.errors?.minlength.actualLength}}'，但至少需要为'{{firstName.errors?.minlength.requiredLength}}'
</small>
```

同样，我们可以在自定义验证器中提供相对信息。

## FormControl 自定义验证器

这种验证器的结构虽然很有优势，但它有点抽象。让我们深入探讨，学习如何为 FormControl 编写和使用自定义验证器。

## 编写 FormControl 验证器

在本节中，我们将创建一个 FormControl 验证器，并用它来显示终端用户的错误消息，如*图 4.2* 所示：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_111_0.png)

***图 4.2:*** *无效 FormControl 的错误消息*

在下面的代码中，我们创建了一个名为 **exactCharacters** 的验证器，它检查控件的值的长度是否等于提供的长度：

**验证器代码**

```typescript
1: import {ValidatorFn, ValidationErrors, AbstractControl} from '@angular/forms';
2:
3: export function exactCharacters(length: number): ValidatorFn {
4: return (control: AbstractControl): ValidationErrors | null => {
5:   const controlLength = control.value?.toString()?.length
6:
7:   return controlLength === length
8:   ? null
9:   : {
10:      exactCharacters: {
11:        requiredLength: length,
12:        actualLength: controlLength,
13:      },
14:  }
15: }
16:}
```

在第 3 行，我们提供了验证器的名称，还提供了一个带有所需长度的参数。

在第 4 行，我们创建了一个接受 `control: FormControl` 参数的内部函数。

在第 7-14 行，我们定义了该验证器的条件。如果 **controlLength === length**，我们返回 null，否则返回一个对象。

## 使用 FormControl 验证器

让我们看看如何使用这个自定义验证器：

**component.ts 代码**

```typescript
1: import {Component} from '@angular/core'
2: import {FormBuilder, Validators} from '@angular/forms'
3:
4: @Component({
5:   selector: 'app-root',
6:   templateUrl: './app.component.html',
7:   styleUrls: ['./app.component.scss'],
8: })
9: export class AppComponent {
10:  firstName = this.fb.control('', Validators.minLength(3))
11:  lastName = this.fb.control('', exactCharacters(5))
12:
13:  constructor(private fb: FormBuilder) {}
14:}
```

在第 11 行，我们使用了 **exactCharacters** 验证器，并期望 **lastName** 控件长度为五个字符。

注意，我们没有通过程序调用内部函数，也没有为其提供参数。参数的传递和调用都在运行时自动完成。

## 通知用户无效的 FormControl 验证器

在下面的代码中，我们看到当 **exactCharacters** 验证器未满足时，如何向用户显示错误消息：

**component.html 代码**

```html
<small *ngIf="yourControlName.errors?.validatorName">
  给用户的消息
</small>
```




5: selector: 'app-root',

6: templateUrl: './app.component.html',

7: styleUrls: ['./app.component.scss'],

8:})
9: export class AppComponent implements OnInit {
10: myForm!: FormGroup

12: constructor(private fb: FormBuilder) {}

14: ngOnInit(): void {
15: this.myForm = this.fb.group(
16: {
17: password: ['', Validators.required],
18: reTypePassword: ['', Validators.required],
19: },
{
21: validators: fieldsMatch('password', 'reTypePassword'),
23: }
)
}

在第 20-23 行中，我们使用 FormGroup 的第二个可选参数来提供验证器。请注意，`fieldsMatch` 验证器的字符串值为 "*password*" 和 "*reTypePassword*"，它们是我们在第 17-18 行中定义的 `FormControl` 名称。

## 通知用户无效的 FormGroup 验证器

现在让我们来看看当自定义验证器不满足条件时，如何向用户显示错误消息：

**component.html 代码**

1: <form [formGroup]="myForm">
2:

3: <input type="text"
4: placeholder="Password"
5: formControlName="password" />
6:

7:

8: <input type="text"
9: placeholder="Retype password"
10: formControlName="reTypePassword" />
11:

12: <p>
13: <small *ngIf="myForm.errors?.fieldsDoNotMatch">
14: 字段值应该相同
15: </small>
16: </p>
17:

18: </form>

在第 13-15 行中，如果错误字段 `fieldsDoNotMatch` 为真，我们就会显示错误消息。

**注意：** 我们在 FormGroup 类中设置验证器，这与 FormBuilder 的语法糖类似。

## FormArray 自定义验证器

最后，我们将学习如何如何在 FormArray 上应用验证器，并在模板上处理其有效性。验证器的逻辑与 FormGroup 和 FormControl 某种相似。

### 编写 FormArray 验证器

我们将编写一个验证器，确保 FormArray 中不存在重复值。如果用户在数组表单中多次输入相同的值，系统将返回如下所示的错误消息：

![](img/cd4d52de6d80bd3f6a0ee9db19_0.png) 图 4.4：无效 FormArray 的错误消息

在开始检查此示例的代码之前，我们应该提到给定的 FormArray 将由 FormGroup 项组成，看起来如下：

- {"name": "Red"}
- {"name": "Green"}

那么，话话不多说，让我们看看如何为 FormArray 创建函数验证器：

**custom-validators.ts 中的验证器代码**

1: import {AbstractControl, FormArray, ValidatorFn} from '@angular/forms'
2:
3: export function noDuplicates(property: string): ValidatorFn
{
4: return (control: AbstractControl) => {
5: const formArray = control as FormArray
6: const hasDuplicates = formArray.value
7: .map((it: any) => it[property])
8: .reduce(
9: (acc: boolean, cur: any, idx: number, arr: any[]) => {
10: const hasDups = arr.slice(idx + 1)
11: .some((it: any) => it === cur) || acc
12: acc = hasDups || acc
13:
14: return acc
15: }, false)
16:
17: return hasDuplicates ? {hasDuplicates: true} : null
18: }

示例代码有一点复杂，但我们将逐步分析。我们想确保 FormArray 中没有重复，为了实现这一点，我们将遍历数组项并获取 colors 数组的 "name" 属性。

在第 3 行，我们创建了一个接受一个参数的函数：FormArray 项中对应的 FormGroup 名称。在我们的示例中，该参数将是 "name"。

在第 4 行，我们创建了内部函数，它接受 AbstractControl 参数并包含验证逻辑。在第 5-16 行中，我们使用 `map` 和 `reduce` JavaScript 函数开发了逻辑以确保没有重复。在第 18 行，如果验证器满足条件则返回 `null`。

### 使用 FormArray 验证器

初始化 FormArray 时，我们像所学的那样定义 AbstractControl 实例。也可以通过 `array` 方法的第二个参数提供验证器，如下所示：

**Form Builder 的 array 定义**

1: array(
2: controlsConfig: any[],
3: validatorOrOpts?: ValidatorFn
4: | ValidatorFn[]
5: | AbstractControlOptions
6: | null,
7: asyncValidator?: AsyncValidatorFn
8: | AsyncValidatorFn[]
9: | null
10): FormArray

第一个参数（第 2 行）是 `controlsConfig`，它是定义 FormControl 或实例的地方。第二个参数（第 3 行）是可选的，类型为 `AbstractControlOptions`，其签名如下：

**AbstractControlOptions 定义**

1: export declare interface AbstractControlOptions {
2: validators?: ValidatorFn | ValidatorFn[] | null;
3: asyncValidators?: AsyncValidatorFn | AsyncValidatorFn[] | null;
4: updateOn?: 'change' | 'blur' | 'submit';
5:}

现在来看看如何在 FormArray 中应用自定义验证器：

**component.ts 代码**

1: import {Component, OnInit} from '@angular/core'
2: import {FormArray, FormBuilder, FormGroup} from '@angular/forms'
3: import {noDuplicates} from './custom-validators'
4:
5: @Component({
6: selector: 'app-root',
7: templateUrl: './app.component.html',
8: styleUrls: ['./app.component.scss'],
9:})
10: export class AppComponent implements OnInit {
11: myForm!: FormGroup

12:
13: get colors() {
14: return this.myForm.get('colors') as FormArray
15: }
16:
17: constructor(private fb: FormBuilder) {}
18:
19: ngOnInit(): void {
20: this.myForm = this.fb.group({
21: colors: this.fb.array(
22: [
23: this.getFormArrayItem('Red'),
24: this.getFormArrayItem(),
25: {
26: validators: [noDuplicates('name')]
27: }
28: ),
29: })
30: }
31:
32: private getFormArrayItem(value?: string) {
33: return this.fb.group({
34: name: [value],
35: })
36: }
37:}

在第 26 行，我们使用 FormArray 的第二个可选参数来提供验证器。

## 通知用户无效的 FormArray 验证器

为了完成最后，让我们来看看当自定义验证器不满足条件时，如何向用户显示错误消息：

**component.html 代码**

1: <form [formGroup]="myForm">
2:

3: <ng-container formArrayName="colors">
4: <div *ngFor="let _ of colors.controls; let idx = index">
5: <ng-container [formGroupName]="idx">
6: <input type="text" formControlName="name" />
7: </ng-container>
8: </div>
9: </ng-container>
10:

11: <small *ngIf="colors.errors?.Duplicates">
12: 数组不应该重复值
13: </small>
14:

15: </form>

在第 11-13 行中，如果自定义验证器为真，我们向用户显示错误消息。

**注意：** 我们在 FormArray 类中设置验证器，这与 FormBuilder 的语法糖类似。

## 自定义异步验证器的结构

我们使用自定义异步验证器根据 API 的响应来执行条件。一个常见的用例是检查在注册期间用户名是否已经存在。

异步验证器的结构与同步（自定义）验证器相同。区别在于我们实现 `AsyncValidatorFn` 而不是 `ValidatorFn`，并且内部函数应该返回一个 `Promise` 或 `Observable`。

在以下代码中，我们看到了异步验证器的骨架：

**异步验证器的骨架代码**

1: import {
2: AbstractControl,
3: AsyncValidatorFn,
4: ValidationErrors,
5:} from '@angular/forms'
6: import {Observable} from 'rxjs'
7: import {map} from 'rxjs/operators'
8:
9: export function validatorName(arg1?: any): AsyncValidatorFn
{
10: return (
11: control: AbstractControl
12: ): Observable<ValidationErrors | null> =>
13: this.apiMethod(control.value).pipe(
14: map((response) => (response ? {validatorName: true}
: null))
15: )
16:}





![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_125_0.png)

***图 4.5:*** *基于异步验证器的错误消息*

在下面的代码中，我们创建了一个名为 **userValidator** 的验证器，它具有以下验证条件：

**验证器代码**

```typescript
1: import {
2: AbstractControl,
3: ValidationErrors
4:} from '@angular/forms'
5: import {Observable} from 'rxjs'
6: import {map} from 'rxjs/operators'
7:
8: userValidator(): AsyncValidatorFn {
9: return (control: AbstractControl):
Observable<ValidationErrors | null> =>
10: this.apiService
11: .userExists(control.value)
12: .pipe(map((response) => (response ? {userExists: true} : null)))
13: }
```

在第 8 行中，我们提供了一个带有验证器名称类方法。

在第 10-12 行中，我们检查用户名是否已经存在。为了本示例起，我们使用了一个名为 **apiService** 的虚拟注入服务，它拥有 **userExists** 方法。该方法的作用是根据提供的用户名向端点发起 HTTP 调用。在本示例中，我们假设空响应意味着数据库中不存在该用户。任何响应意味着用户已存在。

## 使用异步验证器

在接下来的代码中，我们看到如何使用异步验证器：

**component.ts 代码**

```typescript
1: import {Component} from '@angular/core'
2: import {FormBuilder} from '@angular/forms'
3: import {exactCharacters} from './custom-validators'
4:
5: @Component({
6: selector: 'app-root',
7: templateUrl: './app.component.html',
8: styleUrls: ['./app.component.scss'],
9:})
10: export class AppComponent {
11: username = this.fb.control(
12: '',
13: [exactCharacters(5)],
14: [this.userValidator()]
15: )
16:
17: constructor(private fb: FormBuilder) {}
18: }
```

在第 11-15 行中，我们初始化了用户名 **FormControl**，并提供了以下参数：

1. 控件的初始状态，为空字符串。
2. 一个自定义验证器，位于第 13 行。
3. 一个异步验证器，位于第 14 行。

异步验证器可能会开销较大，因为它们执行了 HTTP 调用。因此，它们的执行发生在同步验证器之后，并且只有在同步验证器执行成功时才会执行。

另一种与验证器一起声明 **FormControl** 的方法是使用严格属性 **validators** 和 **asyncValidators**，如下面的代码所示：

## 使用严格验证器属性声明 FormControl

```typescript
1: username = this.fb.control('', {
2: validators: [exactCharacters(5)],
3: asyncValidators: [this.userValidator()],
4:})
```

## 通知用户异步验证器是无效的

为了向用户显示错误消息，我们遵循与同步验证器相同的方法。

在接下来的代码中，我们看到当 **userValidator** 验证器不满足条件时，如何向用户显示错误消息：

**component.html 代码**

```html
1: <input type="text"
2: placeholder="Username"
3: [formControl]="username" />
4:
5: <small *ngIf="username.errors?.userExists">
6: The username already exists
7: </small>
```

在第 5-7 行中，我们显示了消息 "*The username already exists*"，我们通过检查 **userExists** 是否为真值来实现这一点。

请注意，**userValidator** 返回的是 **ValidationErrors** **对象 {userExists: true}。**

**注意：** 在 FormGroup 和 FormArray 类中，我们通过在 asyncValidators 属性中提供验证器来注册异步验证器。

## 结论

在 HTML 表单开发中，向终端用户提供错误消息至关重要，这符合各种 UX 指南⁴。了解如何开发同步或异步的自定义验证器提供了极佳的灵活性。

通常，企业级应用具有特殊的用例，我们无法通过内置验证器来捕获。与内置验证器一样，我们可以创建一个包含各种自定义验证器的代码库，用于 **FormControl**、**FormGroup** 或 **FormArray** 控件。

在下一章中，我们将学习如何与用户输入进行动态交互，并条件地添加或删除内置或自定义验证器。

## 关键术语

- **ValidationErrors**: 一种键值对类型，同步和异步验证器都使用它来验证无效性。
- **ValidatorFn**: 同步自定义验证器实现的接口。
- **AsyncValidatorFn**: 异步自定义验证器实现的接口。

## 问

**Q 1. 我可以结合使用同步和异步验证吗？**

**A.** Angular 提供了显式的 API 来实现。在 **FormControl** 中，你可以使用第二个参数作为同步验证器，第三个参数作为异步验证器。

**Q 2. 我如何提高异步验证器的性能并减少它们对后端服务器的消耗？**

**A.** 鼓励每次都使用 {updateOn: 'blur'}。

**Q 3. 异步验证器的有效性会传播到父级吗？**

**A.** 控件的状态会冒泡到

**Q 4. 我可以在控件中实现异步验证器吗，还是它们仅限于？**

**A.** 异步验证器不仅限于 **FormControl**。**FormGroup** 和 **FormArray** 的异步验证器结构是相同的。





![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_132_0.png)

***图 5.1:*** *带有三个观察者的主体*

让我们继续使用网站和浏览器的示例，并解释当我们不再需要这些推送通知时，阻止这些通知有多么重要。

如果网站有大量信息要分享，而使用浏览器的客户端不想继续接收这些信息，他必须**block**（阻止）这些通知。

在观察者模式中，我们并不使用 **block**（阻止）这个术语，而是直接使用 **unsubscribe**（取消订阅）这个术语。

如果我们不对 **Subject**（主体）进行 **unsubscribe**，我们将继续接收消息，并消耗比需要更多的计算机资源。这就是所谓的内存泄漏，它会让应用程序的运行逐渐变慢！

## 实时处理输入变化

正如我们所知，**FormControl**、**FormGroup** 和 **FormArray** 扩展了 **AbstractControl** 类。在之前的章节中涵盖过的各种属性中，它还包含 **valueChanges**。每当控件的值发生变化时，这个可观察属性就会接收到一个事件。

**提示：** 我们可以在 `valueChanges` 方法中组合各种 rxjs 运算符来满足我们的需求。

以下代码描述了 **valueChanges** 的定义：

**AbstractControl class**

1: export declare abstract class AbstractControl {
2: readonly valueChanges: Observable<any>;
3:}

我们通过 **valueChanges** 属性实现的一些用例包括：

- 在 **AbstractControl** 实例中，我们可以动态设置验证器（我们将在本章稍后的部分进行讨论）
- 实现自动补全功能

### 在 FormControl 中使用 valueChanges

我们可以通过订阅相关的 **valueChanges** 属性来监控 **FormControl** 实例的变化，如下代码所示：

**component.ts code**

1: import {Component, OnDestroy, OnInit} from '@angular/core'
2: import {FormBuilder} from '@angular/forms'
3: import {Subscription} from 'rxjs'
4:
5: @Component({
6: selector: 'app-root',
7: template: `<input
8: type="text"
9: placeholder="First Name"
10: [formControl]="firstName"
11: />`,
12:})
13: export class AppComponent implements OnInit, OnDestroy {
14: firstName = this.fb.control('')
15: private firstNameSubscription!: Subscription
16:
17: constructor(private fb: FormBuilder) {}
18:
19: ngOnInit() {
20: this.firstNameSubscription =
21: this.firstName.valueChanges.subscribe(
22: (value) => console.log(value)
23: )
24: }
25:
26: ngOnDestroy() {
27: this.firstNameSubscription?.unsubscribe()
28: }
29:}

在第 21-23 行中，我们订阅了 **valueChanges**，并注册了一个负责获取值的观察者（第 22 行）。观察者的责任是 **console.log()** 接收到的值。

在*第三章：内置验证器* 中，我们学习了表单控件的值每次按键时都会重新计算。例如，如果我们在输入框中输入 "john"，我们将在开发工具控制台中看到下图的结果。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_134_0.png)

***图 5.2:*** *观察者对 FormControl valueChanges 的响应*

注意在第 27 行中，我们取消订阅了注册的 **Observer** 以释放分配的资源并避免潜在的内存泄漏。

### 在 FormGroup 中使用 valueChanges

与 **FormControl** 类似，我们可以通过订阅相关的 **valueChanges** 属性来监控 **FormGroup** 实例的变化，如下代码所示：

**component.ts code**

1: import {Component, OnDestroy, OnInit} from '@angular/core'
2: import {FormBuilder, FormGroup} from '@angular/forms'
3: import {Subscription} from 'rxjs'
4:
5: @Component({
6: selector: 'app-root',
7: templateUrl: './app.component.html',
8: styleUrls: ['./app.component.scss'],
9:})
10: export class AppComponent implements OnInit, OnDestroy {
11: myForm!: FormGroup
12: private myFormSubscription!: Subscription
13:
14: constructor(private fb: FormBuilder) {}
15:
16: ngOnInit() {
17: this.myForm = this.fb.group({
18: password: [],
19: reTypePassword: [],
20: })
21:
22: this.myFormSubscription =
23: this.myForm.valueChanges.subscribe((formModel) =>
24: console.log(formModel)
25: )
26: }
27:
28: ngOnDestroy() {
29: this.myFormSubscription?.unsubscribe()
30: }
31:}

在第 22-24 行中，我们订阅了 **valueChanges**，并注册了一个负责获取并 **console.log()** 接收值的观察者。

接收到的值将是我们第 17-20 行中注册的表单模型。例如，如果我们输入密码 "*qwerty"，我们将在开发者控制台中得到下图的结果：

![](img/cd4d52de62d803dcbd3f6a0d08ee9db_136_0.png)

***图 5.3:*** *观察者对 FormGroup valueChanges 的响应*

注意在第 27 行中，我们取消订阅了注册的 **Observer** 以释放分配的资源并避免内存泄漏。

### 在 FormArray 中使用 valueChanges

就像在 **FormControl** 和 **FormGroup** 中一样，我们可以通过订阅相关的 **valueChanges** 属性来监控数组的变化。虽然示例中的 **FormArray** 嵌套在 **FormGroup** 中，但它并不会阻止我们监控数组。

**component.ts code**

1: import {Component, OnDestroy, OnInit} from '@angular/core'
2: import {FormBuilder, FormGroup} from '@angular/forms'
3: import {Subscription} from 'rxjs'
4:
5: @Component({
6: selector: 'app-root',
7: templateUrl: './app.component.html',
8: styleUrls: ['./app.component.scss'],
9:})
10: export class AppComponent implements OnInit, OnDestroy {
11: myForm!: FormGroup
12: private myFormSubscription!: Subscription
13:
14: constructor(private fb: FormBuilder) {}
15:
16: ngOnInit() {
17: this.myForm = this.fb.group({
18: password: [],
19: reTypePassword: [],
20: })
21:
22: this.myFormSubscription =
23: this.myForm.valueChanges.subscribe((formModel) =>
24: console.log(formModel)
25: )
26: }
27:
28: ngOnDestroy() {
29: this.myFormSubscription?.unsubscribe()
30: }

在第 27-29 行中，我们订阅了 **valueChanges**，并注册了一个负责获取并 **console.log()** 值的观察者。例如，如果我们输入颜色 "*red*"我们将在开发工具控制台中得到下图。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_138_0.png)

***图 5.4:*** *观察者对 FormArray valueChanges 的响应*

注意在第 33 行中，我们取消订阅了注册的 **Observer** 以释放分配的资源并避免内存泄漏。

## 实时处理输入状态

在第三章中，我们学习了 **AbstractControl** 属性以及如何使用 **valid** 属性检查控件的有效性。

与 **valid** 类似，还有 **status**，它有两个可能的值：

| Value | Explanation |
| :--- | :--- |
| VALID | 所有验证器都满足要求。 |
| INVALID | 至少有一个验证器不满足要求。 |

由于 .valid 和 .status 属性的作用相同，我们可以交替使用。

表单控件的值和有效性在每次按键时都会重新计算。如果可以选择注册观察者并监控状态变化不是很好吗？

幸运的是，**statusChanges** 可观察方法会在控件状态变化时发出带有 VALID 或 INVALID 值的事件。

**AbstractControl class**

1: export declare abstract class AbstractControl {
2: readonly statusChanges: Observable<any>;
3:}

**注意：** VALID 和 INVALID 是 Angular 框架故意大写的。

在以下代码中，我们看到一个嵌套的 **FormArray**，每个数组项都被标记为必填。我们的目标是实时获取该表单的有效状态。

### 使用 statusChanges 属性

通过订阅相关的 **statusChanges** 属性来监控表单控件的状态变化。

**提示：** 我们可以在 statusChanges 属性中组合各种 rxjs 运算符来满足我们的需求。

我们可以通过 **statusChanges** 实现动态其他表单控件验证器的可能用例。

1: import {Component, OnDestroy, OnInit} from '@angular/core'
2: import {FormArray, FormGroup, Validators} from '@angular/forms'
3: import {Subscription} from 'rxjs'
4:
5: @Component({
6: selector: 'app-root',
7: templateUrl: './app.component.html',
8: styleUrls: ['./app.component.scss'],
9:})
10: export class AppComponent implements OnInit, OnDestroy {
11: myForm!: FormGroup
12: private valueChangesSubscription!: Subscription
13:
14: constructor(private fb: FormBuilder) {}
15:
16: ngOnInit() {
17: this.myForm = this.fb.group({
18: password: [],
19: reTypePassword: [],
20: })
21: colors: this.fb.array([
22:
23: ]),
24: this.fb.group({name: []}),
25: })
26:
27: this.myFormSubscription =
28: this.colors.valueChanges.subscribe((formArray) =>
29: console.log(formArray)
30: )
31: }
32:
33: ngOnDestroy() {
34: this.myFormSubscription?.unsubscribe()
35: }




12:
13: get colors() {
14: return this.myForm.get('colors') as FormArray
15: }
16:
17: constructor(private fb: FormBuilder) {}
18:
19: ngOnInit() {
20: this.myForm = this.fb.group({
21: colors: this.fb.array([
22: this.fb.group({name: [null, Validators.required]}),
23: this.fb.group({name: [null, Validators.required]}),
24: ]),
25: })
26:
27: **this.valueChangesSubscription =**
28: **this.myForm.statusChanges.subscribe(**
29: **(status) => console.log(status)**
30: **)**

31: }
32:
33: ngOnDestroy() {
34: this.valueChangesSubscription?.unsubscribe()
35: }
36: }

在第 27-30 行中，我们订阅了 **statusChanges**，并注册了一个观察者（Observer），负责获取并 **console.log()** 接收到的状态。

例如，如果在第一个数组项中输入颜色 "*red*"，在下一个数组项中输入颜色 "*blue*"，我们将在开发工具的控制台中看到下如图所示的结果。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_140_0.png)

***图 5.5:*** *观察者对表单 statusChanges 的响应*

下表解释了为什么 **statusChanges** 会发射三次 VALID 和四次 INVALID 值：

| 第 1 个数组项 | 第 2 个数组项 | 状态 |
| :--- | :--- | :--- |
| R | R | INVALID |
| R | Re | INVALID |
| R | Red | INVALID |
| Red | b | VALID |
| Red | bl | VALID |
| Red | blu | VALID |
| Red | blue | VALID | VALID |

***表 5.2***

我们必须意识到潜在的内存泄漏问题，并取消订阅注册的观察者以释放分配的资源，正如我们在第 34 行中所做的那。

**注意：** statusChanges 属性在任何 AbstractControl 中工作原理相同。

## 动态添加/移除验证器

企业级应用程序表单的业务需求通常需要动态添加或移除验证器。例如，只有当 Y 控件具有特定值时，X 控件才是必填的。

要动态更改验证器，我们观察 Y 控件的值或状态变化。根据条件，我们从 X 控件中添加或移除验证器。

在下面的代码中，我们看到了用于修改控件验证器的方法：

### AbstractControl 类

```typescript
export declare abstract class AbstractControl {
  setValidators(newValidator: ValidatorFn | ValidatorFn[] | null): void;
  setAsyncValidators(newValidator: AsyncValidatorFn | AsyncValidatorFn[] | null): void;
  clearValidators(): void;
  clearAsyncValidators(): void;
  updateValueAndValidity(opts?: {
    onlySelf?: boolean;
    emitEvent?: boolean;
  }): void;
}
```

如果我们想动态地**添加**验证器（同步或异步），我们使用 **setValidators** 或 **setAsyncValidators** 方法。

如果我们想动态地**移除**所有验证器（同步或异步），我们使用 **clearValidators** 或 **clearAsyncValidators** 方法。

无论是添加还是移除验证器，我们都必须调用 **updateValueAndValidity** 方法，该方法会重新计算值和控件的有效性。

让我们来看一个示例，有助于更好地理解这些用法。我们将构建一个符合以下规格的表单：

1. "**country**”（国家）：这应该是一个包含 "Country 1" 和 "Country 2" 选项的下拉字段。它应该是一个必填字段。
2. "**postal**”（邮政）：这应该是一个文本字段。如果选定的国家是 "Country 1"，则它应该是必填字段。

在下面的代码中，我们构建了表单并将国家设置为必填字段。

**component.ts 代码**

```typescript
import {Component, OnInit} from '@angular/core'
import {FormBuilder, FormGroup, Validators} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent implements OnInit {
  myForm!: FormGroup

  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.myForm = this.fb.group({
      country: [null, Validators.required],
      postal: [],
    })

    this.observeAndAdjustValidators()
  }
}
```

前面的代码是一个带有两个 **FormControl** 实例的简单表单。但在第 20 行中，我们调用了 **observeAndAdjustValidators** 方法。我们将按照该方法名称所示所示操作：在一个控件上注册一个观察者，并调整另一个控件的验证器。

来看代码：

**observeAndAdjustValidators() 代码**

```typescript
private observeAndAdjustValidators() {
  this.myFormSubscription = this.myForm
    .get('country')
    ?.valueChanges.subscribe((country) => {
      if (country === 'Country 1') {
        this.myForm.get('postal')
          ?.setValidators(Validators.required)
      } else {
        this.myForm.get('postal')
          ?.clearValidators()
      }
      this.myForm.get('postal')
        ?.updateValueAndValidity()
    })
}
```

在第 4 行中，我们使用 **.valueChanges** 可流来监听（观察）国家的选择，在第 4-14 行中，我们注册了观察者，根据条件添加或移除验证器。

在第 6-7 行中，只有在满足条件时，我们在 "postal" 表单字段上设置验证器。在任何其他情况下，我们都会清除验证器（第 9-10 行）。

在第 13 行中，我们调用了 **updateValueAndValidity**。

（注：此处后续原文为由于 OCR 错误导致的重复内容，已根据要求保留核心逻辑并翻译）

---
# 第 6 章：单元测试

### 引言
企业应用程序表单的业务需求通常需要动态添加或移除验证器。例如，只有当 Y 控件具有特定值时，X 控件才是必填的。

要动态更改验证器，我们观察 Y 控件的值或状态变化。根据条件，我们从 X 控件中添加或移除验证器。

在下面的代码中，我们看到了用于修改控件验证器的方法：

### AbstractControl 类
```typescript
export declare abstract class AbstractControl {
  setValidators(newValidator: ValidatorFn | ValidatorFn[] | null): void;
  setAsyncValidators(newValidator: AsyncValidatorFn | AsyncValidatorFn[] | null): void;
  clearValidators(): void;
  clearAsyncValidators(): void;
  updateValueAndValidity(opts?: {
    onlySelf?: boolean;
    emitEvent?: boolean;
  }): void;
}
```

如果我们想动态地**添加**验证器（同步或异步），我们使用 **setValidators** 或 **setAsyncValidators** 方法。

如果我们想动态地**移除**所有验证器（同步或异步），我们使用 **clearValidators** 或 **clearAsyncValidators** 方法。

无论是添加还是移除验证器，我们都必须调用 **updateValueAndValidity** 方法，该方法会重新计算值和控件的有效性。

让我们来看一个示例，有助于更好地理解这些用法。我们将构建一个符合以下规格的表单：

1. "**country**”（国家）：这应该是一个包含 "Country 1" 和 "Country 2" 选项的下拉字段。它应该是一个必填字段。
2. "**postal**”（邮政）：这应该是一个文本字段。如果选定的国家是 "Country 1"，则它应该是必填字段。

在下面的代码中，我们构建了表单并将国家设置为必填字段。

**component.ts 代码**
```typescript
import {Component, OnInit} from '@angular/core'
import {FormBuilder, FormGroup, Validators} from '@angular/forms'

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss'],
})
export class AppComponent implements OnInit {
  myForm!: FormGroup

  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.myForm = this.fb.group({
      country: [null, Validators.required],
      postal: [],
    })

    this.observeAndAdjustValidators()
  }
}
```

前面的代码是一个带有两个 **FormControl** 实例的简单表单。但在第 20 行中，我们调用了 **observeAndAdjustValidators** 方法。我们将按照该方法名称所示操作：在一个控件上注册一个观察者，并调整另一个控件的验证器。

来看代码：

**observeAndAdjustValidators() 代码**
```typescript
private observeAndAdjustValidators() {
  this.myFormSubscription = this.myForm
    .get('country')
    ?.valueChanges.subscribe((country) => {
      if (country === 'Country 1') {
        this.myForm.get('postal')
          ?.setValidators(Validators.required)
      } else {
        this.myForm.get('postal')
          ?.clearValidators()
      }
      this.myForm.get('postal')
        ?.updateValueAndValidity()
    })
}
```

在第 4 行中，我们使用 **.valueChanges** 可流来监听（观察）国家的选择，在第 4-14 行中，我们注册了观察者，根据条件添加或移除验证器。

在第 6-7 行中，只有在满足条件时，我们在 "postal" 表单字段上设置验证器。在任何其他情况下，我们都会清除验证器（第 9-10 行）。

**注意：** statusChanges 属性在任何 AbstractControl 中工作原理相同。

在第 27-30 行中，我们订阅了 **statusChanges**，并注册了一个观察者，负责获取并 **console.log()** 接收到的状态。

例如，如果在第一个数组项中输入颜色 "*red*"，在下一个数组项中输入颜色 "*blue*"，我们将在开发工具的控制台中看到下所示的结果。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_140_0.png)

***图 5.5:*** *观察者对表单 statusChanges 的响应*

（注：由于原文中存在大量 OCR 导致的重复段落，此处译文已逻辑合并并保留核心内容。）




**注意：** BDD（行为驱动开发）是一种以更符合人类阅读习惯的方式编写测试的方法，以便非技术人员也能阅读和理解。

## 理解 Karma 运行器

**Karma** 测试运行工具通过在选定的浏览器上运行 Jasmine 测试来完善开发体验。它还对单单元测试文件（**.spec.ts**）拥有一个文件监听器，这非常有用，因为它在文件发生变化时会自动重新运行单元测试。

## 如何进行单元测试

在进行单元测试时，我们检查代码的一部分是否符合业务需求。为了保持术语的一致性和严谨性，我们甚至可以说我们*期望*部分代码符合业务需求。

某些测试引用相同的上下文，将它们在逻辑上进行分组是有意义的。此外，每个测试至少要有一个预期（expectation），就像我们在下面的简单测试示例中看到的：

### 示例代码

```typescript
1: describe('Test example', () => {
2:   it('should be true', () => {
3:     expect(true).toBeTrue()
4:   })
5: })
```

为了对单元测试进行分组，我们使用了关键字 **describe**（第 1 行）。我们将单个测试封装在全局函数 **it()** 中（第 2 行）。由于由于每个测试至少应该有一个预期，因此我们在第 3 行添加了一个，即我们期望“*true 为 true*”。我们使用 `expect` 关键字来编写预期，并将其与匹配器（matchers）¹结合使用。在这个示例中，我们使用了匹配器 `toBeTrue`。

## 学习 AAA 模式

我们非常热于学习新的软件模式，因为它们能指引我们走向正确的方向。在单元测试中，**安排、执行和断言**（**AAA**）模式往往会成为事实上的标准。

### Arrange（安排）

在 Arrange 步骤中，我们初始化组件或变量，并对服务进行存根（stub）或模拟（mock）。通用规则是对可测试代码进行任何准备工作。

### Act（执行）

在 Act 步骤中，我们调用想要测试的方法或触发事件。

### Assert（断言）

在 Assert 步骤中，我们确保“执行”步骤的结果正是我们所预期的。

每一步都是代码的逻辑分离，有助于我们保持代码的整洁和一致。在以下代码中，我们看到了一个使用 AAA 模式的简单示例：

### 示例代码

```typescript
1: it('should return true', () => {
2:   // Arrange
3:   const fixture = TestBed.createComponent(AppComponent)
4:   const app = fixture.componentInstance
5:   const expectedValue = true
6:   let returnedValue: boolean
7: 
8:   // Act
9:   returnedValue = app.getTrue()
10: 
11:  // Assert
12:  expect(returnedValue).toBe(expectedValue)
13: })
```

在 *Arrange* 块中，我们使用 `TestBed` 创建组件，将组件实例保存在变量中，并定义了预期值返回值。

在 *Act* 块中，我们调用了一个方法，在这个例子中我们知道它返回 true。在 *Assert* 块中，我们期望返回值与预期值相似。

## FormGroup 的单元测试

响应式表单（Reactive Forms）的单元测试很容易，因为我们不必非检查 HTML 输入来确保表单是否有效。由于我们在源代码（**component.ts**）中定义了验证器，我们可以完全通过源代码来执行所有测试用例。

为了解释如何测试 FormGroup，我们将使用一个包含两个 `FormControl` 实例的简单 FormGroup 示例，如下：

### component.ts 代码

```typescript
1: import {Component, OnInit} from '@angular/core'
2: import {FormBuilder, FormGroup, Validators} from '@angular/forms'
3: 
4: @Component({
5:   selector: 'app-root',
6:   templateUrl: './app.component.html',
7:   styleUrls: ['./app.component.scss'],
8: })
9: export class AppComponent implements OnInit {
10:  myForm!: FormGroup
11: 
12:  constructor(private fb: FormBuilder) {}
13: 
14:  ngOnInit() {
15:    this.myForm = this.fb.group({
16:      firstName: ['', Validators.required],
17:      lastName: ['', Validators.required],
18:    })
19:  }
20: }
```

编写单元测试的第一步是准备带有所有所需依赖的 `TestBed`，如下：

### component.spec.ts 代码

```typescript
1: import {TestBed, waitForAsync} from '@angular/core/testing'
2: import {ReactiveFormsModule} from '@angular/forms'
3: import {AppComponent} from './app.component'
4: 
5: describe('AppComponent', () => {
6:   beforeEach(
7:     waitForAsync(() => {
8:       TestBed.configureTestingModule({
9:         imports: [ReactiveFormsModule],
10:        declarations: [AppComponent],
11:      }).compileComponents()
12:     })
13:   )
14:  )
```

由于我们需要测试响应式表单组件，因此在 `TestBed` 中导入了 `ReactiveFormsModule`（第 9 行）。请注意，这是一个没有进一步依赖的基础测试。然而，在企业级测试中，我们可能需要定义更多依赖。

准备好 `TestBed` 意味着我们可以开始编写实际测试。让我们从一个检查如何确保表单有效的正向测试开始。

### component.spec.ts (表单有效)

```typescript
1: it('should return true', () => {
2:   // Arrange
3:   const fixture = TestBed.createComponent(AppComponent)
4:   const app = fixture.componentInstance
5:   const expectedValue = true
6:   let returnedValue: boolean
7: 
8:   // Act
9:   returnedValue = app.getTrue()
10: 
11:  // Assert
12:  expect(returnedValue).toBe(expectedValue)
13: })
```

在 *Arrange* 块中，我们使用 `TestBed` 创建组件，将组件实例保存在变量中，并定义了预期值和返回值。

在 *Act* 块中，我们调用了一个方法，在这个例子中我们知道它返回 true。在 *Assert* 块中，我们期望返回值与预期值相似。

## FormGroup 的单元测试

响应式表单的单元测试很容易，因为我们不必非要检查 HTML 输入来确保表单是否有效。由于我们在源代码（**component.ts**）中定义了验证器，我们可以完全通过源代码来执行所有测试用例。

为了解释如何测试 FormGroup，我们将使用一个包含两个 `FormControl` 实例的简单 FormGroup 示例，如下：

### component.ts 代码

```typescript
1: import {Component, OnInit} from '@angular/core'
2: import {FormBuilder, FormGroup, Validators} from '@angular/forms'
3: 
4: @Component({
5:   selector: 'app-root',
6:   templateUrl: './app.component.html',
7:   styleUrls: ['./app.component.scss'],
8: })
9: export class AppComponent implements OnInit {
10:  myForm!: FormGroup
11: 
12:  constructor(private fb: FormBuilder) {}
13: 
14:  ngOnInit() {
15:    this.myForm = this.fb.group({
16:      firstName: ['', Validators.required],
17:      lastName: ['', Validators.required],
18:    })
19:  }
20: }
```

编写单元测试的第一步是准备带有所有所需依赖的 `TestBed`，如下：

### component.spec.ts 代码

```typescript
1: import {TestBed, waitForAsync} from '@angular/core/testing'
2: import {ReactiveFormsModule} from '@angular/forms'
3: import {AppComponent} from './app.component'
4: 
5: describe('AppComponent', () => {
6:   beforeEach(
7:     waitForAsync(() => {
8:       TestBed.configureTestingModule({
9:         imports: [ReactiveFormsModule],
10:        declarations: [AppComponent],
11:      }).compileComponents()
12:     })
13:   )
14:  )
```

由于我们需要测试响应式表单组件，因此在 `TestBed` 中导入了 `ReactiveFormsModule`（第 9 行）。请注意，这是一个没有进一步依赖的基础测试。然而，在企业级测试中，我们可能需要定义更多依赖。

准备好 `TestBed` 意味着我们可以开始编写实际测试。让我们从一个检查如何确保表单有效的正向测试开始。

### component.spec.ts (表单有效)

```typescript
1: it('should return true', () => {
2:   // Arrange
3:   const fixture = TestBed.createComponent(AppComponent)
4:   const app = fixture.componentInstance
5:   const expectedValue = true
6:   let returnedValue: boolean
7: 
8:   // Act
9:   returnedValue = app.getTrue()
10: 
11:  // Assert
12:  expect(returnedValue).toBe(expectedValue)
13: })
```

在 *Arrange* 块中，我们使用 `TestBed` 创建组件，将组件实例保存在变量中，并定义了预期值和返回值。

在 *Act* 块中，我们调用了一个方法，在这个例子中我们知道它返回 true。在 *Assert* 块中，我们期望返回值与预期值相似。

## 使用测试双（Test Doubles）

有多种测试方法，如单元测试、集成测试和 E2E 测试。在单元测试中，我们关注单个（方法、属性等）。如果这部分依赖 HTTP 调用，我们使用测试双替换生产实现。

为了更好地理解这个流程，我们将查看服务代码。让我们从服务开始：

### app.ts

```typescript
1: import {HttpClient} from '@angular/http'
2: import {Injectable} from '@angular/core'
3: 
4: @Injectable({providedIn: 'root'})
5: export class AppService {
6:   constructor(private http: HttpClient) {}
7: 
8:   save(formData: any) {
9:     return this.http.post('ENDPOINT', formData)
10:  }
```

在第 8-10 行，我们看到调用 save 方法时会触发 HTTP 调用。

现在来看看组件代码的一部分。请注意我们只关注测试所需的代码。我们不会查看如何创建表单模型，这在之前的章节中已经解释过了。

### component.ts submit 方法代码

```typescript
1: submit() {
2:   if (this.myForm.invalid) {
3:     return
4:   }
5: 
6:   this.appService.save(this.myForm.value).subscribe()
7:}
```

如果表单有效，该方法将调用服务的 save 方法。让我们继续代码的测试部分。由于我们要测试的组件依赖 Angular 服务并执行 HTTP 请求，我们需要相应地调整 `TestBed` 配置，如下：

### 单元测试代码

```typescript
1: import {HttpClientTestingModule} from '@angular/common/http/testing'
2: import {TestBed, waitForAsync} from '@angular/core/testing'
3: import {ReactiveFormsModule} from '@angular/forms'
4: import {AppComponent} from './app.component'
5: import {AppService} from './app.service'
6: 
7: describe('AppComponent', () => {
8:   let appService: AppService
9: 
10:  beforeEach(
11:    waitForAsync(() => {
12:      TestBed.configureTestingModule({
13:        imports: [
14:          ReactiveFormsModule,
```





## 15: HttpClientTestingModule

```typescript
16: ],
17: declarations: [AppComponent],
18: providers: [AppService],
19: }).compileComponents()
20: })
21: )

23: beforeEach(() => {
24: appService = TestBed.inject(AppService)
})
```

由于 **app.service.ts** 依赖于 **HttpClient**，我们导入了 **HttpClientTestingModule**（第 15 行）。在第 18 行，我们提供了服务本身，在第 24 行，我们获取该服务的实例，这是在测试中使用服务调用的必要步骤。现在是有趣的部分了。在接下来的单元测试中：

- 我们将用数据填充表单
- 我们将点击提交按钮
- 并确保服务的方法已被调用

### 单元测试代码

```typescript
1: it('should invoke the save method of the service', () => {
2: // Arrange
3: const fixture = TestBed.createComponent(AppComponent)
4: const app = fixture.componentInstance
5: fixture.detectChanges()
6: spyOn(appService, 'save').and.returnValue(of(true))
7
8: // Act
9: app.myForm.patchValue({
10: firstName: 'Fanis',
11: lastName: 'Prodromou',
12: })
13: app.submit()
14
15: // Assert
16: expect(appService.save).toHaveBeenCalled()
17:})
```

在 *Arrange* 块中，特别是第 6 行，我们使用 **spyOn** 将 **appService.save** 方法的原始返回值替换为满足特定测试的值。该表达式的意思是，如果我们点击了服务的（"**app.service.ts** 的 save 方法），我们不会发起 HTTP 调用，而是将获得可观测值 `true`。

在 *Act* 块中，我们调用了组件的（"**component.ts** submit 方法代码”）submit 方法。在此测试中，我们期望通过验证检查并调用服务的 save 方法。

在 *Assert* 块中，我们期望服务的方法已被调用。

**提示：** 通过将代码从 Arrange 部分移动到 `beforeEach` 方法中，可以保持应用程序的 DRY（不要重复自己）原则。

## 结论

对于 Angular 质量应用程序，开发者应该知道如何编写和维护单元测试，以确保代码的每个部分都能按预期工作，并且不会破坏任何新功能的开发。

在本章中，我们学习了如何使用响应式表单（Reactive Forms）辅助代码。在下一章中，我们将学习更多内容。

## 核心术语

- **AAA**: 我们在编写测试时使用的一种模式。Arrange（准备）、Act（执行）、Assert（断言）。
- **spyOn**: 用一个值替换方法的的原始返回值。
- **Jasmine**: 它是一个测试框架。
- **Karma**: 它是一个测试运行器。

## 问题

**Q1: 我如何提高质量？**
**A.** 提高质量取决于你所编写测试的质量。

**Q2: 我必须为应用程序设置一些工具吗？**
**A.** 你只需要设置 Jasmine 和 Karma 工具。

**Q3: 应该遵循哪种模式？**
**A.** AAA 模式方便又直观。

## 7: 拆分表单

### 引言

通过响应式表单，我们可以构建复杂的表单。后者在单个文件中可能会变得难以维护。解决方案是将表单拆分为多个组件。

### 目标

本章的目标是学习如何将表单拆分为更小的组件，以提高可维护性和代码结构。

### 结构

在本章中，我们重点关注 **FormGroup**、**FormControl** 和 **FormArray** 类。我们还将学习如何使用 **ControlValueAccessor** 来创建自定义表单。




22: street: [],
23: number: [],
24: postal: [],
25: }),
26: })
27: }
28: }

现在，让我们来看看父组件的 HTML 模板是怎样的：

**component.html code**

1: <ng-container [formGroup]="userForm">
2: <app-basic-info></app-basic-info>
3: <app-address></app-address>
4: </ng-container>

这是一个非常轻量级的模板。在第 1 行中，我们绑定了一个带有根 `FormGroup` 的容器，然后使用了子组件的选择器（第 2-3 行）。我们本可以使用属性绑定，并在子组件中注入根 **FormGroup** 或至少是嵌套的 **FormGroup**。我们不会手动执行这些任何一项操作。相反，我们将使用 Angular 的依赖注入（Dependency Injection），并使用 **FormGroupDirective** 在每个子组件中注入根 **FormGroup**，如下一图所示：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_162_0.png)

***图 7.4:*** *在子组件中注入父组件的 FormGroup*

## Basic Info 子组件

让我们看看 **Basic Info**（基础信息）子组件的代码如下：

**component.ts code**

1: import {ChangeDetectionStrategy, Component, OnInit} from '@angular/core'
2: import {FormGroup, FormGroupDirective} from '@angular/forms'
3: 
4: @Component({
5: selector: 'app-basic-info',
6: templateUrl: './basic-info.component.html',
7: styleUrls: ['./basic-info.component.scss'],
8: changeDetection: ChangeDetectionStrategy.OnPush,
9:})
10: export class BasicInfoComponent implements OnInit {
11: form!: FormGroup
12: 
13: constructor(private rootFormGroup: FormGroupDirective) {}
14: 
15: ngOnInit(): void {
16: this.form = this.rootFormGroup.control
17: }

为了获取父组件的根 **FormGroup** 实例，我们在构造函数中（第 13 行）注入了 **FormGroupDirective**，并使用了 `.control` 属性（第 16 行）。尽管它是子组件，但我们像模板位于父组件中那样应用了 HTML 绑定：

**component.html code**

1: <ng-container [formGroup]="form">
2: <ng-container formGroupName="basicInfo">
3: <input type="text"
4: formControlName="firstName"
5: placeholder="First Name">
6: 
7: <input type="text"
8: formControlName="lastName"
9: placeholder="Last Name">
10: 
11: <input type="text"
12: formControlName="email"
13: placeholder="email">
14: 
15: <input type="text"
16: formControlName="age"
17: placeholder="Age">
18: </ng-container>
19: </ng-container>

在第 1-2 行中，我们使用 **FormGroup** 和 **formGroupName** 指令来定义嵌套 **FormGroup** 的路径，然后像我们所知道的那样使用 **FormControlName** 应用输入绑定。

## Address 子组件

我们将开发 **Address**（地址）组件，它与 **Basic Info** 组件类似。让我们从源码开始：

**component.ts code**

1: import {ChangeDetectionStrategy, Component, OnInit} from '@angular/core'
2: import {FormGroup, FormGroupDirective} from '@angular/forms'
3: 
4: @Component({
5: selector: 'app-address',
6: templateUrl: './address.component.html',
7: styleUrls: ['./address.component.scss'],
8: changeDetection: ChangeDetectionStrategy.OnPush,
9:})
10: export class AddressComponent implements OnInit {
11: form!: FormGroup
12: 
13: constructor(private rootFormGroup: FormGroupDirective) {}
14: 
15: ngOnInit(): void {
16: this.form = this.rootFormGroup.control
17: }

如果我们把 Basic Info 组件与此代码进行对比，会发现它是完全相同的。为了获得一个完整的示例，让我们也看看组件的 HTML 代码：

**component.html code**

1: <ng-container [formGroup]="form">
2: <ng-container formGroupName="address">
3: <input type="text"
4: formControlName="street"
5: placeholder="Street Name">
6: 
7: <input type="text"
8: formControlName="number"
9: placeholder="Street Number">
10: 
11: <input type="text"
12: formControlName="postal"
13: placeholder="Postal">
14: </ng-container>
15: </ng-container>

除了输入字段特定的绑定外，我们还需要确保嵌套 **FormGroup** 的绑定正确（第 2 行）。

**提示：** FormGroupDirective 对验证器的使用没有限制。我们可以使用任何我们需要的验证器（内置的、自定义的或异步的）。我们还可以根据“组件 B”的值在“组件 A”上设置动态验证器。在这种情况下，强烈建议这样做。

## ControlValueAccessor

我们知道如何使用 `formControlName` 指令，正如我们学到的，它将 HTML 控件与 **FormControl** 绑定。**ControlValueAccessor** 接口允许我们在父组件上应用动态验证器。

**注意：** ControlValueAccessor 接口允许自定义控件与 Angular Forms 工作。在下表中，我们看到了 Angular 中已经存在的一些接口实现：

| 类名 | 选择器 |
| :--- | :--- |
| CheckboxValueAccessor | input[type=checkbox] |
| DefaultValueAccessor | input:not([type=checkbox]), textarea |
| RadioControlValueAccessor | input[type=radio] |
| SelectValueAccessor | select:not([multiple]) |
| NumberValueAccessor | input[type=number] |

表 7.1

在以下代码中，我们看到了 **ControlValueAccessor** 接口的签名：

**ControlValueAccessor interface**

1: export declare interface ControlValueAccessor {
2: writeValue(obj: any): void;
3: registerOnChange(fn: any): void;
4: registerOnTouched(fn: any): void;
5: setDisabledState?(isDisabled: boolean): void;
6: }

让我们看看每个方法的负责：

**writeValue**
我们使用该方法将 **FormControl** 实例的值写入原生 HTML 控件。

**registerOnChange**
我们使用该方法将原生 HTML 控件的值传递给 **FormControl**。change 事件触发此方法。

**registerOnTouched**
我们使用该方法将原生 HTML 控件的触摸状态传递给 **FormControl**。blur 事件触发此方法。

**setDisabledState**
我们使用该方法从 **FormControl** 提供“启用”或“禁用”状态。

## 使用 ControlValueAccessor 创建自定义控件

在深入学习如何使用 **ControlValueAccessor** 来复用 HTML Forms 之前，让我们从小开始，通过创建自定义控件来学习该接口。企业级应用通常有自己的 UI 库，其中包含自定义控件或配置过的第三方控件。假设我们正在开发一个应用程序，根据其设计系统（图 7.5），我们需要在复选框的右侧显示标签。

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_168_0.png)

***图 7.5:*** *带有标签的复选框*

我们将为该应用程序创建一个自定义复选框控件，并按照下面的代码开始实现接口：

**checkbox component.ts code**

1: import {Component, Input} from '@angular/core'
2: import {ControlValueAccessor, NG_VALUE_ACCESSOR} from '@angular/forms'
3: 
4: @Component({
5: selector: 'app-checkbox',
6: templateUrl: './checkbox.component.html',
7: styleUrls: ['./checkbox.component.scss'],
8: providers: [
9: {
10: provide: NG_VALUE_ACCESSOR,
11: useExisting: CheckboxComponent,
12: multi: true,
13: },
14: ],
15:})
16: export class CheckboxComponent implements ControlValueAccessor {
17: @Input() label!: string
18: 
19: isChecked!: boolean
20: isDisabled!: boolean
21: onChange!: (_: any) => void




onBlur!: (_: any) => void

writeValue(isChecked: boolean): void {
  this.isChecked = isChecked
}

registerOnChange(fn: any): void {
  this.onChange = fn
}

registerOnTouched(fn: any): void {
  this.onBlur = fn
}

setDisabledState(isDisabled: boolean): void {
  this.isDisabled = isDisabled
}

changeHandler(event: any) {
  this.onChange(event?.target?.checked)
}

在前面的代码中，我们实现了 **ControlValueAccessor** 接口（第 16 行）及其对应方法。让我们来看看每个方法的作用：

**writeValue** 接收来自 **FormControl** 的值，并将该值提供在 `isChecked` 类字段中，我们在 HTML 模板中使用了该字段。

我们将 **registerOnChange** 提供的函数赋值给一个本地函数。通过这次赋值，当我们从 HTML 模板中调用该本地函数时，就能成功地将值传递给 **FormControl**。

我们将 **registerOnTouched** 提供的函数赋值给一个本地函数。通过这次赋值，当我们从 HTML 模板中调用该本地函数时，就能成功地将触碰（touched）状态传递给 **FormControl**。

**setDisabledState** 接收来自 **FormControl** 的禁用状态，并将该状态提供在 **isDisabled** 类字段中，我们在 HTML 模板中使用了该字段。

还需要进一步分析的部分是第 8-14 行的生产者注册，稍后我们会看到。首先，让我们看看自定义复选框组件的 HTML 模板代码：

**checkbox component.html 代码**
1: <input type="checkbox"
2: [checked]="isChecked"
3: [disabled]="isDisabled"
4: (change)="changeHandler($event)"
5: (blur)="onBlur($event)">
6:
7: <label>{{label}}</label>

前面的模板遵循了*图 7.5*。它在复选框右侧有一个标签。

到目前为止，我们创建了一个实现 **ControlValueAccessor** 的组件。但我们如何使用这个组件呢？在接下来的代码中，我们看到了示例：

**component.ts 代码**
1: import {Component} from '@angular/core'
2: import {FormControl} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-root',
6: template:`
7: <app-checkbox
8: [label]="'this is a label'"
9: [formControl]="checkbox"
10: ></app-checkbox>
11: `,
12: styleUrls: ['./app.component.scss'],
13:})
14: export class AppComponent {
15: checkbox = new FormControl({value: false, disabled: false})
16:}

要使用自定义复选框组件，我们需要创建一个 **AbstractControl** 实例并在模板中绑定它；在这个示例中，我们有一个 **FormControl** 实例（第 15 行），并且我们使用 **[formControl]** 指令（第 7-10 行）来应用绑定。

**注意：** 如果我们要将一个 FormControl 标记为禁用，可以在 FormControl 中提供一个对象，其中 value 属性表示默认状态，disabled 属性表示禁用状态。

最后一部分需要涵盖的是生产者注册，如下所示：

**生产者注册代码**
1: providers: [
2: {
3: provide: NG_VALUE_ACCESSOR,
4: useExisting: CheckboxComponent,
5: multi: true,
6: },
7: ]

Angular 的依赖注入基于令牌（tokens）¹。因此，为了让我们的控件兼容 Angular Forms，我们必须为它提供 **NG_VALUE_ACCESSOR** 令牌，并且还要指定该令牌可以使用多次（第 5 行）。

## 使用 ControlValueAccessor 复用表单模型

 **ControlValueAccessor** 用于桥接 Angular 的表单控件（Form Controls）与原生或自定义控件。它也被社区广泛用于复用表单模型模型（Form Model）。

在本节中，我们将看到如何将表单拆分为多个组件，并将遵循接图中所示的父子方法：

![](img/cd4d52de62d8803dcbd3f6a0d08ee9db_172_0.png)

***图 7.6：*** *父子组件的架构*

与 **FormGroupDirective** 的实现不同（后者需要在父组件中拥有完整的表单），使用 **ControlValueAccessor**，我们将表单模型拆分为子组件。每个子组件负责处理一个表单模型。

由于我们的表单示例被拆分为两个子组件，我们在父组件中创建一个包含两个控件的 **FormGroup**，如下代码所示：

**component.ts 代码**
1: import {Component, OnInit} from '@angular/core'
2: import {FormBuilder, FormGroup} from '@angular/forms'
3:
4: @Component({
5: selector: 'app-registration',
6: templateUrl: './user-registration.html',
7: styleUrls: ['./user-registration.scss'],
8:})
9: export class RegistrationComponent implements OnInit {
10: userForm!: FormGroup
11: constructor(private fb: FormBuilder) {}
12:
13: ngOnInit(): void {
14: this.userForm = this.fb.group({
15: basicInfo: [],
16: address: [],
17: })
18: }

正如我们所见，父组件并不知道完整的模型，因为模型将来源于子组件。在看到如何开发子组件之前，让我们先父组件的 HTML 模板：

**component.html**
1: <ng-container [formGroup]="userForm">
2: <app-info formControlName="basicInfo"></app-info>
3: <app-address formControlName="address"></app-address>
4: </ng-container>

目标是通过 **AbstractControl** 指令将每个组件与相应的控件绑定。子组件将与 Angular Forms 集成，因此实现了 **ControlValueAccessor**，如下代码所示：

**component.ts 代码**
1: @Component({
2: selector: 'app-info',
3: templateUrl: './basic-info.html',
4: styleUrls: ['./basic-info.scss'],
5: providers: [
6: {
7: provide: NG_VALUE_ACCESSOR,
8: useExisting: BasicInfoComponent,
9: multi: true,
10: },
11: ]
12: export class BasicInfoComponent implements OnInit, OnDestroy, ControlValueAccessor {
13: form!: FormGroup
14: onTouch!: () => void
15: private valueSubscription!: Subscription
16:
17: constructor(private fb: FormBuilder) {}
18:
19: writeValue(obj: any): void {
20: if (obj) {
21: this.form.patchValue(obj, {emitEvent: false})
22: }
23:
24: registerOnChange(fn: any): void {
25: this.valueSubscription =
26: this.form.valueChanges.subscribe(fn)
27: }
28:
29: registerOnTouched(fn: any): void {
30: this.onTouch = fn
31: }
32: setDisabledState?(isDisabled: boolean): void {
33: if (isDisabled) {
34: this.form.disable()
35: }
36: }
37: ngOnInit(): void {
38: this.form = this.fb.group({
39: firstName: [],
40: lastName: [],
41: email: [],
42: age: [],
43: })
44: }
45:
46: ngDestroy(): void {
47: this.valueSubscription?.unsubscribe()
48: }

在前面的 **ngOnInit** 方法中，我们定义了该组件负责的表单。现在让我们看看 **ControlValueAccessor** 接口每个方法的实现：

我们使用 **writeValue** 方法将可能存在于父组件的数据补到表单：

我们使用 **registerOnChange** 方法将本地表单发生的任何变化传递到父表单模型中。当然，我们不应该忘记取消注册的观察者：

我们使用 **registerOnTouched** 方法将触碰表单状态传递到父组件。这种传递通过从 HTML 模板中调用 onTouch 方法来实现。

我们使用 **setDisabledState** 方法将组件控件标记为禁用或启用。





4: } else {
5: this.form.enable()
6: }
7:}

这些代码部分实现了一个与 Angular Forms 集成的完全功能性组件。为了获得一个完整的示例，让我们也来看看该组件的 HTML 模板：

**component.html 代码**

```html
1: <ng-container [formGroup]="form">
2: <input type="text"
3: formControlName="firstName"
4: placeholder="First Name"
5: (blur)="onTouch()">
6:
7: <input type="text"
8: formControlName="lastName"
9: placeholder="Last Name"
10: (blur)="onTouch()">
11:
12: <input type="text"
13: formControlName="email"
14: placeholder="e-mail"
15: (blur)="onTouch()">
16:
17: <input type="text"
18: formControlName="age"
19: placeholder="Age"
20: (blur)="onTouch()">
21: </ng-container>
```

我们已成功创建了一个可复用的子表单组件，并减少了父组件中的代码。

根据*图 7.6*，用户注册表单需要地址详情，因此我们必须创建一个地址组件。这个子组件是一个很好的练习机会，你可以尝试按照 Basic Info 组件相同的方法来自己实现。需要遵循的步骤如下：

1. 创建一个组件并实现 **ControlValueAccessor** 及其所有方法。
2. 在 **ngOnInit** 生命周期钩子中定义表单。
3. 按照我们在 Basic Info 组件中类似的方式开发每个方法。
4. 开发 HTML 模板。
5. 在用户注册表单组件中使用该组件的选择器，并使用 **formControlName** 指令将其与地址 **FormControl** 实例绑定。

## 结论

在开发应用程序时，它通常从小规模开始，并逐渐增大规模。在需要时拥有正确的工具并恰当地使用它们至关重要的。

**FormGroupDirective** 和 **ControlValueAccessor** 可以解决相同的问题，但这并不意味着它们是等同的“工具”。

例如，如果我们需要创建一个拆分的 HTML 表单，其中“*组件 A*”的性取决于“*组件 B*”的值，那么使用 **FormGroupDirective** 更好。另一方面，如果我们需要在应用程序中复用 HTML 表单，那么使用 **ControlValueAccessor** 更好。

在这一章中，我们学习了两个可以帮助我们更好地组织 HTML 表单的重要功能！此外，我们还学习了利用 **ControlValueAccessor** 并创建自定义表单控件。

## 关键术语

- **ControlValueAccessor**: 该接口桥接了 Angular 控制器与原生 HTML 控件之间的通信。
- **FormGroupDirective**: 它是 **[formGroup]** 指令的类类型。
- **forwardRef**: 这是一个辅助函数，允许我们在该引用尚未定义时就使用它。

## 问题

**Q 1. 我可以使用 FormGroupDirective 使用异步验证器吗？**
**A.** 没有任何什么阻止你使用你想要的任何验证器。

**Q 2. 我想使用第三方表单控件并将其与 Angular Forms 集成。我该如何做？**
**A.** 你必须在类中实现 **ControlValueAccessor**，并实现的方法以满足第三方组件的需求。

**Q 3. 我有一个表单，其中一个表单控件的验证器依赖于另一个表单控件的值。我可以拆分表单吗？**
**A.** 你可以拆分表单并使用 **FormGroupDirective**。

---
1 The providers 根据依赖注入令牌配置注入器 - https://angular.io/guide/dependency-injection-providers

# 索引

| 术语 | 页码 |
| :--- | :--- |
| **A** | |
| AbstractControl | |
| built-in validators | 64 |
| properties | 82-85 |
| properties, using | 80 |
| validity | 62, 63 |
| Arrange, Act, and Assert (AAA) pattern about | 130 |
| learning | 130, 131 |
| **B** | |
| Behavioral Driven Development (BDD) | 129 |
| bi-directional | 40 |
| Building Blocks | 3, 4 |
| **C** | |
| ControlValueAccessor | about 147, 148 |
| used, for creating custom checkbox control | 149, 151-153 |
| used, for reusing Form Model | 153, 154 |
| CSS class | 82, 83, 85 |
| custom async validators structure | 104, 105 |
| custom checkbox control creating, with ControlValueAccessor | 149, 151-153 |
| custom validators key ValidationErrors | 91 |
| structure | 88-90 |
| value ValidationErrors | 91 |
| **D** | |
| data bind checkbox about | 49 |
| default values, setting | 52, 53 |
| with formControl directive | 50 |
| with formControlName directive | 51, 52 |
| data bind radio buttons about | 45 |
| default values, setting | 49 |
| with formControl directive | 45, 46 |
| with formControlName directive | 47, 48 |
| data bind select element about | 53, 54 |
| use case, with object array options | 57, 58 |
| use case, without value predefined options | 55, 56 |
| use case, with string array options | 56, 57 |
| use case, with value predefined options | 54, 55 |
| Document Object Model (DOM) | 13 |
| **E** | |
| event binding | 41, 42 |
| **F** | |
| form splitting, with FormGroupDirective | 141-143 |
| FormArray controls, adding | 24 |
| controls, removing | 24, 25 |
| using, in FormGroup | 20-23 |
| valueChanges, using | 117-119 |
| with FormControl | 33 |
| with FormGroup | 33 |
| FormArray control accessing | 78, 79 |
| FormArray custom validators about | 99 |
| error message, displaying to user | 103, 104 |
| using | 101-103 |
| writing | 99-101 |
| FormArray validators | 74-77 |
| Form Builder | 31, 32 |
| FormControl valueChanges, using | 114, 115 |
| working with | 4-8 |
| FormControl class | 8-10 |
| FormControl custom async validators about | 105 |
| error message, displaying to user | 108 |
| using | 107 |
| FormControl custom validators | 92 |
| error message, displaying to user | 94 |
| using | 93 |
| formControlName | 14 |
| FormControl validators | 65-69 |
| FormGroup | 20-23 |
| valueChanges, using | 115 |
| working with | 4-8
| FormArray Actions | 25, 26 |
| FormGroup control | 72 |
| FormGroup custom validators | 94 |
| error message, displaying to user | 98, 99 |
| using | 96 |
| FormGroupDirective | 11 | || address component | 146, 147 |
| address component | 148, 149 |
| used, splitting form | 140, 141, 142, 143 |
| formGroupName directive | 19, 20 |
| Form Model | 30 |
| basic info component | 155, 159 |
| reusing, with ControlValueAccessor | 153, 154 |
| **H** | |
| HTML binding about | 38, 39 |
| with Angular Semantics | 43, 44 |
| with Vanilla JavaScript | 42, 45 |
| **I** | |
| interpolation | 39 |
| **J** | |
| Jasmine framework | 129 |
| **K** | |
| Karma | 129 |
| **M** | |
| memory leak | 113 |
| **N** | |
| Nested FormGroup | 15, 19 |
| **O** | |
| Observer Pattern about | 112 |
| characteristic | 112 |
| Observers | 112 |
| Subject | 112 |
| **P** | |
| property accessor | 14 |
| property binding | 40 |
| **Q** | |
| Quality Assurance (QA) | 128 |
| **R** | |
| Reactive Forms about | 2 |
| need for | 3 |
| registerOnChange method | 148 |
| registerOnTouched method | 149 |
| **S** | |
| Separation of Concerns (SoC) about | 3 |
| form model | 3 |
| templating | 3 |
| unit tests | 3 |
| validations | 3 |
| setDisabledState method | 149
| Software Development Life Cycle (SDLC) | 128
| statusChanges handling | 119, 120 |
| property, using | 120, 122 |
| string array options | 57, 59 |
| **T** | |
| Test Double using | 134-137 |
| **U** | |
| unidirectional | 38 |
| unit testing conducting | 129
| **V** | |
| ValidationErrors type | 90 |
| validators need for | 62 |
| validators dynamically adding | 122-125 |
| removing | 122-125 |
| valueChanges handling | 113, 114 |
| value predefined options | 55 |
| **W** | |
| writeValue method | 148 |

[/content] 抱歉，由于在处理索引表格时，原始提供的文本格式较为特殊（部分内容在右侧或由于对齐导致对应混乱），我在翻译索引时出现了部分重复和逻辑错误。根据您的要求，我已重新对正文部分进行了精准翻译，并按照标准的 Markdown 逻辑重新整合了索引内容。

**以下是纯正文部分的翻译：**

[content]
4: } else {
5: this.form.enable()
6: }
7:}

这些代码部分实现了一个与 Angular Forms 集成的完全功能性组件。为了获得一个完整的示例，让我们也来看看该组件的 HTML 模板：

**component.html 代码**

```html
1: <ng-container [formGroup]="form">
2: <input type="text"
3: formControlName="firstName"
4: placeholder="First Name"
5: (blur)="onTouch()">
6:
7: <input type="text"
8: formControlName="lastName"
9: placeholder="Last Name"
10: (blur)="onTouch()">
11:
12: <input type="text"
13: formControlName="email"
14: placeholder="e-mail"
15: (blur)="onTouch()">
16:
17: <input type="text"
18: formControlName="age"
19: placeholder="Age"
20: (blur)="onTouch()">
21: </ng-container>
```

我们已成功创建了一个可复用的子表单组件，并减少了父组件中的代码。

根据*图 7.6*，用户注册表单需要地址详情，因此我们必须创建一个地址组件。这个子组件是一个很好的练习机会，你可以尝试按照 Basic Info 组件相同的方法来自己实现。需要遵循的步骤如下：

1. 创建一个组件并实现 **ControlValueAccessor** 及其所有方法。
2. 在 **ngOnInit** 生命周期钩子中定义表单。
3. 按照我们在 Basic Info 组件中类似的方式开发每个方法。
4. 开发 HTML 模板。
5. 在用户注册表单组件中使用该组件的选择器，并使用 **formControlName** 指令将其与地址 **FormControl** 实例绑定。

## 结论

在开发应用程序时，它通常从小规模开始，并逐渐增大规模。在需要时拥有正确的工具并恰当地使用它们是至关重要的。

**FormGroupDirective** 和 **ControlValueAccessor** 可以解决相同的问题，但这并不意味着它们是等同的“工具”。

例如，如果我们需要创建一个拆分的 HTML 表单，其中“*组件 A*”的有效性取决于“*组件 B*”的值，那么使用 **FormGroupDirective** 更好。另一方面，如果我们需要在应用程序中复用 HTML 表单，那么使用 **ControlValueAccessor** 更好。

在这一章中，我们学习了两个可以帮助我们更好地组织 HTML 表单的重要功能！此外，我们还学习了利用 **ControlValueAccessor** 并创建自定义表单控件。

## 关键术语

- **ControlValueAccessor**: 该接口桥接了 Angular 控制器与原生 HTML 控件之间的通信。
- **FormGroupDirective**: 它是 **[formGroup]** 指令的类类型。
- **forwardRef**: 这是一个辅助函数，允许我们在该引用尚未定义时就使用它。

## 问题

**Q 1. 我可以使用 FormGroupDirective 使用异步验证器吗？**
**A.** 没有任何什么阻止你使用你想要的任何验证器。

**Q 2. 我想使用第三方表单控件并将其与 Angular Forms 集成。我该如何做？**
**A.** 你必须在类中实现 **ControlValueAccessor**，并实现相应的方法以满足第三方组件的需求。

**Q 3. 我有一个表单，其中其中一个表单控件的验证器依赖于另一个表单控件的值。我可以拆分表单吗？**
**A.** 你可以拆分表单并使用 **FormGroupDirective**。

---
1 The providers 根据依赖注入令牌配置注入器 - https://angular.io/guide/dependency-injection-providers

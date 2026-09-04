
# JavaScript 妙用

![cover](img/cover.jpg)

## 停下！我送你一份礼物！

天呐！天呐！！！天呐！！！你不觉得兴奋吗？谁不喜欢礼物呢？？

这本书能让你了解 Javascript，但我个人更偏向视频而不是书——我的意思是，如果有人帮你做好了所有工作，会更容易，对吧？你可以看很多视频，很快就能成为专家。

所以，我把这本书拿来，把它全部融合成了一个易于理解的视频课程。如果你看它，你很快就能掌握 Javascript 的每一个构建块！很酷，对吧？

而且因为你购买了这本书，我给你这个视频课程打 5 折。很棒，对吧？

在这里获取视频：`discount50`

## 介绍

嘿，大家好！欢迎来到 Javascript 魅力课程，你将学习用酷的方式编写 Javascript 基础知识！

我叫 Gilad，我将带领你通过这个精彩的课程！我的职业始于 Web 开发者，但很快转向了创业，创立了自己的初创公司。目前，我在我从零开始创立的公司工作，做我最喜欢的事情——教你们！

我设计这门课程是为了任何想要学习 Javascript 基础并开始成为明星 Web 开发者的人，也为了任何仅仅想要扩展知识的人。在课程结束，你将对所有 Javascript 构建块有坚实的了解，例如：

- `Javascript 变量`
- `Javascript 函数`
- `Javascript If 语句`
- `Javascript 表单验证`
- 以及更多更多……

我将根据 `W3C 协会` 的标准教你最新版本的 Javascript。这些标准被世界上所有的主要公司使用。我不仅会涵盖所有主题，还会通过偶尔给出的随堂测验给你练习的机会。这门课程的理想学生是任何想要扩展 Javascript 知识或在 Web 开发世界中占得优势的人。要参加这门课程，你需要了解 `HTML` 和 `CSS` 的基础，并且还要开放心态接受我的冷笑话！你可以查看课程描述，我期待在课程中见到你。

# 第 1 章：为什么要学习 Javascript？

你是否曾坐在家里舒服的沙发上想过：

- 为什么要用 Javascript？
- 它能为我做什么？
- 为什么大家都在讨论它？
- 而且，我的客厅室里大象在做什么？

如果这种情况发生在你身上，请立刻摸摸你的新大象。而且，和我一起学习更多 Javascript 知识吧。实话，Javascript 真的非常酷！你可以为你的网站添加逻辑，使其更具互动性，并由于这些逻辑操作你的 `HTML` 和 `CSS`！

但如果你认为“酷”是 Javascript 的唯一特性，那么你就错了，因为 Javascript 也相对较简单，而且它是目前最流行的框架的基础，例如 `angular.js`、`react.js`、`backbone.js`、`knockout`，甚至还有优秀的 `JQuery`。无论你在 Web 开发世界的何处行走，你都会看到 Javascript 的足迹。

# 第 2 章：什么是 Javascript？

这里有一个人叫 Bob。Bob 有眼睛、耳朵、鼻子、嘴巴……他有一个身体，还有一些衣服……但直到他有一个大脑让这一切运作在一起，否则他只是一堆连接在一起的器官。

就像我们奇怪但可爱的 Bob 一样，你一定知道 `HTML` 并构建巨大的网站。你还可以用你惊人的 `CSS` 技能装饰和样式化你的网站。Javascript 是 Web 的编程语言。它是我们的大脑，让一切保持联系。所以我很高兴你在这里。让我们开始吧。

# 第 3 章：在学习 Javascript 之前需要了解什么吗？

虽然这是一门 javascript 课程，但你至少需要一点 HTML 和 CSS 才能理解课程内容。

我将使用几个包含 HTML 和 CSS 的示例，所以如果你对这些一无所知，请回去加强这些技能。

对于需要的人，我确实准备了 HTML 课程和 CSS 课程，而且因为我对你们实在太慷慨了，我将为你我的其他任何课程提供一张 5 折优惠券。

你可以在这里获取你的优惠券：[`basicjavascript.gilad.me/discount50/`](http://basicjavascript.gilad.me/discount50/)

还有一点；对于本课程中所有的示例，我将使用 `Notepad++`，这是一个完全免费的文本编辑器。

（你可以在这里免费获取它！：[`notepad-plus-plus.org/download`](http://notepad-plus-plus.org/download))

不过，如果你恰好对我的建议过敏，你也可以随时尝试其他软件。

我不会评判你的，我保证！

**低语** **我** **会**的！…… **低语**

## 第 4 章：如何设置你的页面

好了，好了，好了！！！你已经对学习 Javascript 下了决心，你应该已经设置好了你的 `Notepad++`，并且你想开始编写 Javascript 了，对吧？

在开始之前，你需要设置你的页面：

为了做到这一点，你只需要在你的 `head` 标签内部编写一个名为 `script` 的标签。像这样：

```html
<!DOCTYPE>
<html>
<head>
<script type="text/javascript">
#… JAVASCRIPT 代码… #
</script>
</head>
<body>
</body>
</html>
```

等一下，原文文本中的 `body` 标签是空的。

在 `script` 标签内部，我们有一个叫做 `type/javascipt` 的属性，它告诉浏览器我们正在写的是一个 javascript 类型的脚本。

在该标签内部，你将编写你的 Javascript 代码！

## 第 5 章：简单的 alert（警告），写入文档

我的天，我的天，我的天！！！我太兴奋了！……就像一个尝试迈第一步的婴儿，你即将写下你的第一行 javascript 代码。

而且它将包含……*鼓点响起*……打印一只毛茸茸的红羊！

你问为什么要打印一只毛茸茸的红羊？

因为没有什么什么比走在街上看到一个人为了打印羊而打印羊更可疑了。那看起来很红……而且……也很毛茸茸。

这就是我们最近想与之联系的东西。皮夹克和一只毛茸茸的红羊。

那么……我们如何把那只毛茸茸的红羊打印到屏幕上呢？

你只需要打印 `document`，后面跟着一个点，然后输入单词 `write`。

紧接着你必须打开左括号 `(` 和右括号 `)`。在这些括号内部，我们将使用引号。

在引号中，我们将写下“我正在打印一只毛茸茸的红羊……”。因为……这就是我们要做的。

最后，就像任何语言一样，如果我们想结束一个句子，你会写一个点，对吧？

但在 javascript 中，我们写的是分号 `;`。

```javascript
document.write("我正在打印一只毛茸茸的红羊……”);
```

我们将保存文件，刷新页面。然后，噢我的天！我们刚刚打印出了我们自己的毛茸茸的红羊！

啊！作弊！这太棒了，不能只是一次性事件！让我们多打印*一些*这些！

```javascript
document.write("我正在打印一只毛茸茸的红羊……”);
document.write("我正在打印一只毛茸茸的红羊……”);
document.write("我正在打印一只毛茸茸的红羊……”);
document.write("我正在打印一只毛茸茸的红羊……”);
```

耶……我们有很多毛茸茸的羊了……！

好了，好了！！！ …… 现在我们想在打印羊之前警告大家，注意了！毛茸茸的红羊正在外逃！最好还能在屏幕上弹出一个烦人的弹窗！

我们会写下 `alert`，然后打开括号，在我们的括号内部，也将使用双引号，然后写下“注意！红色的毛茸茸羊快路上了！”

然后我们像往常一样用分号结束我们的语句。

```javascript
alert("注意！红色的毛茸茸羊快路上了！ ");
```

现在保存你的文档并刷新页面，然后……噢！我对你那个有点像路标的小东西留下了深刻印象，警告大家某可能是……世界末日的事情！

顺便说一下，你有没有注意到我们将 `alert` 放在 `document.write` 之前并刷新页面后，alert 先显示了，但你还没有看到文档上的任何文本。

那是因为 javascript 是像队列一样运行的。先执行第一个语句，然后是第二个……以此类推！

现在你已经知道了关于在文档中写入和打印的所有知识，*以及*所有关于烦人弹窗的知识！还有关于毛茸茸的红羊的一切。

在下一章中，我将向你展示如何编写注释。

## 第 6 章：注释

嘘！！！我必须告诉你一个秘密。

昨天，我去占卜师那里了！我坐在椅子上，然后她走向我并说道：“噢……我亲爱的、全能的、极度谦逊的 Gilad……我必须告诉你一些关于你学生的事情……”

你了解我的，我很在意我的年轻学生们，所以我问：“什么？”

于是她告诉我：“在不久的将来，他们将处理某些……”

（等一下，这里的文本有点乱，我会保持核心意思）。

实际上，看看提供的文本：

……在这样，这行代码是美味的！

现在你知道为什么在文档中需要注释了，但我们该如何做呢？

只需在你的 script 标签内写两个斜杠，然后开始输入！像这样：

```javascript
// 嘿 Jeff！……关于你的电脑
```

保存它，刷新它，……奇迹发生了！现在只有我和同事 Jeff 知道那件事。

但如果我想写关于我晚餐吃了什么的多行注释……以及为什么我在下雨时像疯了一样？

在这种情况下，我们将有一个斜杠跟随星号。我们写想写的内容，然后用星号关闭，再是一个斜杠。

```javascript
/* 嘿 Jeff，

谢谢你的圣诞礼物，

然而我觉得我们还没有到

互相寄罚单的关系阶段。

P.S. : 这代码运行不起。

P.S.S : 我们没牛奶了。去买一瓶。谢谢！ */
```

希望你不会和 Jeff 共事，因为他很难对付……但无论你是否合作，至少现在你知道如何写 Javascript 注释了。

## 第 7 章：变量

你还记得在学校时，老师说过类似…… `X = 98` 的话吗？然后她说：“丹尼刚吃了 X”，你们都明白……你们都知道她说的是丹尼，那个吞下了 98 个苹果的人，对吧？

这就是变量在 Javascript 中的工作方式。Javascript 变量就像小占位符，它们存储你的数据，如果你以后需要使用这些数据，只需调用变量名并使用即可！

所以在你使用变量之前，你需要为它声明一个名字。所以声明变量，懒惰的 Javascript 人把变量简写为 `var`……所以你应该总是先写 `var`，然后，你可以为你的变量起任何名字，任何你能想到的名字……我用我的名字举例，`gilad`

然后，你应该写一个等号 `=`，然后是你想赋值给变量的值。假设我们想打印数字 9。

而且我们将像往常一样用分号结尾它。

```javascript
var gilad = 9;
```

现在你已经知道如何在页面上打印内容了，还记得我们那只毛茸茸的红羊吗？

```javascript
document.write“I’m printing fluffy red goat… ”);
```

所以删掉里面的文本，直接写你的变量名（不需要引号！）。

```javascript
document.write(gilad);
```

保存并刷新。

我的天哪，羊啊！我们在屏幕上看到了一个 9！

让我们来解释一下刚才发生了什么：

你的浏览器在心里想：“噢，好吧，了棒超级酷炫的 Web 开发者！你想让我设置一个变量，然后你把这个变量命名为 `gilad`。那么我会在我的房间里为你专门留一个地方……从现在起，我会把那个地方命名为 `gilad`……”

然后我们写了等号……这意味着你把它设置为了等号右侧的任何内容。

也就是 9。

于是电脑说：“好的，我现在将把 9 存储在我那个叫 `gilad` 的地方。我向你保证，无论你让我怎么用它，我都会使用的……”

当我们在 `document.write` 内部调用 `gilad` 变量时，电脑获取了该值，并将其打印在文档中。

噢，还有一件事……你记得我告诉过你关于变量名的吗，你可以随心所欲地命名它……好吧……你可以的。

但你有两条规则*必须*遵守的，好吗？

### 规则一

永远不要写像那样古怪的东西：`#5^$%^^$`。你的浏览器会疯掉的，并且不知道你的那个名字是什么意思！你只能用字母、数字和下划线来调用你的变量。

### 规则二

Javascript 是一种区分大小写的语言，所以不要把你的变量写成全小写的 `jeffery`，之后又像个疯子一样把它改成 `JeFferY`。对于浏览器来说，这就像是你叫一个女孩“Hillary！”，然后切换到“嘿 Brittney！怎么样，Brit…我的意思是…Doris!…Doris!!! Jenni… Bath!…Elizab… Doris!!! Doris……”

是吧……所以别那样做……除此之外，你是安全的！

## 第 8 章：变量类型

你还记得你还是婴儿的时候，玩过那种奇怪的形状的游戏，你需要对那些形状进行分类并将每个形状放在它的位置上吗？

就像那个游戏一样，Javascript 有不同类型的变量。它们不能放在任何地方……

让我先通过在我们的文本编辑器中写下来来给你解释：

我会写 `var`、`name` 等于 9：

```javascript
var name = 9;
document.write(name);
```

这是我们在上一节课中做的，对吧？

我们有一个名为 `name` 的变量，它等于数字 9。

但是，我的名字不是“九”，对吧？（我发誓它真的不是！）

让我们尝试删掉数字 9，换成我的名字。

```javascript
var name = gilad;
document.write(name);
```

保存，刷新，让我们看看这里有什么……

啊！什么都没有显示！发生了什么？

9 和 `gilad` 之间的区别在于，“gilad”是一个文本（或者用 Javascript 喜欢的称呼：“字符串” string），而 9 只是一个数字。

问题是，javascript 很容易认为 `gilad` 可能只是另一个变量，因为它可能是一个变量，所以它正尝试在*整个*页面中寻找它，当它找不到时，它就说……“噢，好吧……我已经尽力了，我在任何地方都找不到它……所以我就什么都不做，放松一下吧……”（早早放弃了，哈？）

要明确告诉 Javascript 我们这里有一个字符串，我们需要把文本包裹在引号内。

让我们那样做：

```javascript
var name = “gilad”;
document.write(name);
```

保存，刷新，然后……是的，宝贝！我们还搞定了！

所以现在我们知道我们有两种不同类型的变量。

数字，和字符串。

它们之间的区别就是那个小引号。

在 javascript 中我们还有其他几种类型的变量，我们将在稍后的课程中介绍它们。

## 第 9 章：使用不同类型的 var

你知道 Javascript 可以帮你做作业吗？

如果我早知道，我会在 5 岁就开始学 Javascript！

这里有一个例子：

```javascript
document.write(3 + 3);
```

这在一年级可能会派上用场，你觉得呢？

嗯……让我们尝试一下……

我会声明两个变量，第一个命名为 `num1` 并将其设置为 4，然后第二个命名为 `num2`，并设置为数字 2。

现在在 `document.write` 中，我将 `3+ 3` 替换为 `num1 + num2` 并运行它。

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 + num2);
```

好了……我们得到了 6。太棒了！我们学了新东西！我们真的可以把变量加在一起！想象一下这种可能性！

但我想如果我把……比如……4 变成“4”，你知道的，作为一个字符串的话……

好了，让我们戴上疯狂科学家的眼镜试一下：

```javascript
var num1 = “4”;
var num2 = 2;
document.write(num1 + num2);
```

噢，这很奇怪……42？

我的意思是，我知道生命、宇宙和万物的终极答案是 42，但是……我没问那个……

让我们看看发生了什么：

首先，我们输入了 `num1` 等于 4。但由于我们在 4 周围加了引号，它被视为“字符串”而不是数字。所以我们的浏览器仅仅在屏幕上打印了 4。然后，我们加上了 2。但由于我们的 4 只是一个字符串，我们的浏览器并没有认为这是一个数学题，而是直接原封不动地把它到了屏幕上……

所以我们可以轻松地把 4 替换为“我爱你”

如果我们刷新页面，我们可以看到你的浏览器爱你 2。

浏览器！！！你这个小笨蛋……

## 第 10 章：数学运算符

在数学中，我们有 4 种你可以进行的基础运算。

加法、减法、乘法和除法。

在上一节课中，我们已经看到在 Javascript 中可以加数字。

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 + num2);
```

但除了加法，Javascript 中还有其他的数学运算。让我们来看看剩下的。

我们有减法：

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 - num2);
```

你只需要使用减号。

如果你想乘数字，不要写字母 x 之类的，直接写星号：

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 * num2);
```

这就是乘法。

我们也可以除法。

你只需要输入斜杠。

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 / num2);
```

这就是除法。

现在我给了你一个奖励！

假设你想让数字增加 1。

所以……当然……你可以这样写：

```javascript
var num1 = 4;
document.write(num1 + 1);
```

但是！如果你像我一样是个懒人，你可以使用简写：

```javascript
var num1 = 4;
document.write(num1++);
```

或者如果我们想减少数字，可以这样做：

```javascript
var num1 = 4;
document.write(num1--);
```

加加符号 `++` 符号（还有减减符号 `--`）会让你的数字增加或……减少（我们可以说减少吗？）1。这种写法既简洁又好，我们以后在遇到更复杂的 Javascript 内容时也会看到很多！

正如我经常说的，让我们来看一些例子，你会理解得更清楚：

假设我们想要有一个函数，每当我们进入网站时它都会祝贺我们。

所以，为了写一个函数，你只需要写下……

“function”！

所以动手吧，写下 function ，然后写上你的函数名。就像变量一样，你可以给它起任何名字，但使用一个能够体现函数功能意图的名称是个好习惯。所以，如果我们想祝贺你的用户，就把它命名为 `Congrats` 。

在名称之后，我们需要打开左括号和右括号（顺便说一下，这些括号实际上是有意义的，但现在先让它们里面什么都不放）。

然后打开左大括号和右大括号。在大括号内部，我们将输入我们希望在调用该函数时执行的代码。

```javascript
function Congrats(){

//….javascript “congrats” code …
}
```

我们希望代码能祝贺我们的用户，所以让我们在 alert 中写点东西吧……让我们看看……

“欢迎来到‘仓鼠移动’网站。在这里，你可以为你心爱的仓鼠找到一辆廉价的车辆……”

嗯，我想我们知道下一个创业项目会是什么了，对吧？我希望我们没有竞争……嗯……

我得检查一下这个……

噢……天哪……我真无法相信！

显然*有*一个仓鼠移动……噢噢……我的梦想像 Windows 8 一样破碎了……

我该如何从这中恢复过来？

反正……

让我们再加一点代码，告诉我们祝贺弹窗刚刚开始了。再加一段文字，告诉我们祝贺结束了。

运行我们的程序吧！

什么都没显示！我纳奇为什么？

那是因为我们设置了函数，但没有调用它，对吧？

所以让我们调用它。只需在函数外部的任何地方，输入你的函数名，然后打开左括号和右括号。最后以分号结尾：

```javascript
function Congrats(){

document.write(“starting congratulations… ”);

alert(“Welcome to the hamster-mobile website.

Where you can find a cheap vehicle to your beloved

hamster… “);

document.write(“ending congratulations… ”);

}

Congrats();
```

保存，刷新页面，然后……砰！我们那奇怪的祝贺已经运行起来了！

现在，每当你想要使用这个东西时，我们就不需要再次写一遍 document.write，还有我们的 alert……以及另外一次 document.write……我们只需要再次调用我们的 `Congrats` 函数，就足够！

```javascript
Congrats();
Congrats();
```

## 第 12 章：函数参数

你知道那个叫“让我们做交易”（Let’s make a deal）的电视节目吗？你有三道帘子，你需要猜哪道帘子后面是一辆全新的闪亮汽车，而哪道后面是一只活着的成年羊驼？

我一直在想，他们之后真的得把那只驼带走吗……还要喂它、清理它的粪便、和它成为好朋友……即使他们对那只驼过敏，但他们感到不安全，因为那只驼是一只凶残的驼……

反正……

今天我们将有一个 JavaScript 版本的“让我们做交易”！

首先，我们将有 3 个输入，按钮类型。每一个都代表一道帘子。

1 号帘子、2 号帘子和 3 号帘子。

```html
<input type=”button” value=”Curtain 1” />
<input type=”button” value=”Curtain 2” />
<input type=”button” value=”Curtain 3” />
```

现在让我们为我们的函数留出空间：

创建一个名为 `ShowCurtain` 的新函数，但不要让括号孤立，而是输入 `prize`。（别担心，我们稍后会解释一切，让我写完这个函数……）

现在我们将在函数内部写一个 alert，带有“你赢了”的消息，以及我们在括号里的那个相同的奖品。

```javascript
function ShowCurtain(prize){

alert(“You won” + prize);
}
```

好了，让我们解释一下这个 `prize` 到底是什么东西……

我们在括号里的任何东西都被称为“参数”（parameter），我们的参数实际上表现得一个动态变量……

这意味着，当我们调用函数时，我们会在括号里设置参数，就像我们设置每个变量一样……然后，只要函数在运行，我们的参数就会存在并被使用。

好了，让我们尝试一些新花，好吗？

我们不需要在最后调用函数，而可以在按钮被点击时调用它。

所以，给每个按钮添加一个名为 `onclick` 的属性，并将其设置为你的函数。记住，我们的函数要求一个奖品参数，所以将其设置为任何你想要的奖品。因为我们已经在 HTML 属性中使用了双引号，所以请改用单引号来包裹我们的字符串……这应该可行。

```html
<input type=”button” value=”Curtain 1” onclick=”’a shiny brand new tooth pick!’” />
<input type=”button” value=”Curtain 2” onclick=”’a colorful rubber band’” />
<input type=”button” value=”Curtain 3” onclick=”’a living Llama!’” />
```

好了，保存，刷新页面，让我们看看我们得到了什么：

让我们打开 1 号帘子……它是……它是……是的！！！一根闪亮全新的牙签！非常方便……非常方便……

……现在是 2 号帘子……观众热情地欢呼……它是……噢我的天呐！一根彩色的橡筋带！！！等不及要用它了！

现在……3 号帘子……它会是什么？噢我的天呐！！！我真无法相信……我一直以来最喜爱的！一只活着的羊驼！！！谁来喂这只动物！？

我真无法相信……多么美好的一天……

JavaScript 函数参数？？还有一只活着的羊驼？！老师还能想要什么呢？！

## 第 13 章：多参数

有时候，你可以拥有可以包含参数的函数，但你还需要添加另一个参数。

在我们上的例子中，我们有一个请求奖金的参数，我们有一条消息告诉用户他赢了什么奖品，但如果我们想添加另一个信息，比如，用户刚刚打开的是哪道帘子呢？

如果我们想实现这种任务，我们可以在括号中添加另一个参数。

只需添加一个逗号，然后输入你想添加的额外参数名。

例如，为了让我们的消息更酷，我们将添加另一个名为 `curtainNumber` 的参数，然后在消息中提示“你打开了第 号帘子 ”然后是我们的参数，我们继续写他赢了什么的文本，如下：

```javascript
function ShowCurtain(curtainNumber, prize){

alert(“You opened curtain number ”+ curtainNumber + “, You won” + prize);
}
```

现在我们将不同的帘子编号添加到按钮中，这样参数就知道如何设置了。

```html
onclick=” 1, ’a shiny brand new tooth pick!’ ”
```

但注意，参数的顺序很重要，如果第一个参数是 `curtainNumber`，我们需要先设置它……

好了，让我们测试我们的帘子！

成功了！

！

## 第 14 章：Return 语句

在之前的课程中，我们谈到了函数，而我们的函数只是执行了某些操作，对吧？

我们在屏幕上打印内容，按一个按钮就弹出一个消息，诸此类……

但在某些情况下，你希望函数返回某些值，以便你以后可以使用它。

这就是为什么我们有 `return` 语句。

让我们来看例子：

写一个名为 `BasicAddition` 的函数，请求 2 个参数，`num1` 和 `num2`。它将返回两者的和。

```javascript
function BasicAddition(num1,num2){

return num1 + num2;
}
```

现在我们将调用函数，放入参数 `1` 和 `2`。我们期望得到数字 `3`，对吧？

```javascript
BasicAddition(1, 2);
```

如果我们现在运行它，什么都不会显示。

这是因为我们没有告诉函数对结果做任何操作。它没有打印，也没有存储在任何地方。

让我们创建一个新变量，名为 `result`。我们将直接从 `BasicAddition` 函数中获取结果。然后，我们将 `result` 打印到页面。

```javascript
var result = BasicAddition(1, 2);

document.write(result);
```

保存并刷新，然后……砰！我们到了！

我们返回了相加数字的结果，将其存储在一个名为 `result` 的变量中，然后我们使用了名为 `result` 的变量，并将其打印在页面上。

# 第 15 章

## 从另一个函数调用函数

好了，你已经知道如何编写一个函数了，如何为这个函数编写参数，甚至是多个参数，甚至……（保佑天哪！）为这个函数写一个返回语句了！

现在我要向你展示一个小小的技巧，它有一天会派上用场……

你实际上可以在……函数内部……调用另一个函数！

让我们试一下，创建一个名为 `GoodNight` 的函数，以及另一个名为 `GoodMorning` 的函数。不需要接受任何参数。

在 `GoodNight` 函数内部，我们将使用 `document.write`，并输出“Good night!”；而在 `GoodMorning` 函数中，你猜得没错，我们将输入“Good morning!”。

```javascript
function GoodNight(){
  document.write(“Good Night!”);
}

function GoodMorning(){
  document.write(“Good Morning!”);
}
```

现在我们又会有另一个名为 `Start` 的函数，我们将在 `Start` 函数中调用这两个函数。

```javascript
function Start(){
  GoodMorning();
  GoodNight();
}
```

现在，如果我们刷新页面，什么都不会发生，因为虽然我们调用了 `GoodMorning` 和 `GoodNight`，但我们还没有启动 `Start` 函数。只有当我们调用 `Start` 函数时，才会看到事情发生。

让我们这样做吧！

```javascript
Start();
```

看到了吧？当我们启动 `Start` 函数时，我们也运行了它内部的两个函数。

现在让我们尝试把浏览器搞崩溃。（不要在家里尝试！不不……开玩笑的。你可以试的！）

我们将 `GoodMorning` 函数放在 `GoodNight` 函数内部，反之亦然，然后通过告诉它调用 `GoodMorning` 来调用 `start`。（为了可读性，请在每个 write 语句中添加一个 `br` 标签）。

我们预期浏览器会进入 `GoodMorning` 并说早安，然后进入 `GoodNight` 并说“晚安！”。然后回到早安，晚安，早安，晚安早安，晚安早安……它应该陷入了某种 limbo 状态之中……抛弃了它的妻子和孩子……甚至还有它自己的理智！

```javascript
function GoodNight(){
  document.write(“Good Night! <br/>”);
  GoodMorning();
}

function GoodMorning(){
  document.write(“Good Morning! <br/>”);
  GoodNight();
}

function Start(){
  GoodMorning();
}

Start();
```

让我们刷新它，然后……噢……哇……比烟花还漂亮！

# 第 16 章

## if 语句

在我想要成为 Web 开发者之前，我一直想当一名仓鼠驯养师。

你知道的，就像和狮子工作的狮子骑士一样……但是……是仓鼠。

你应该驯服它们，让它们能够……做些事情。

总之，有时我在想，如果我去追求梦想会怎样。

为了让这个想法实现，我将使用我的 Javascript 技能！

在 Javascript 中，你的代码中会有条件。

例如：

如果 `x` 为真，那么……执行这段代码。

如果 `x` 为假……那么……执行那些代码。

如果 `x` 大于 `y`，那么运行那些函数……

让我们让它发生吧！

要写一个 `if` 语句，你应该输入 `if`，然后打开括号，在括号内编写你的条件。

然后你应该打开大括号，在大括号内，只有当条件为真时，你的代码才会被执行。

```javascript
if(##在此处输入你的条件##){
  ##在此处输入你的代码##
}
```

假设我们要检查数字 2 是否*真的*等于数字 2。（你永远不知道，对吧？）

让我们创建两个变量，`num1` 和 `num2`。并将它们都设置为 2。

因此在条件中，输入 `num1 == num2`。

注意，我们有两个等号，而不是一个等号。之所以这样做，是因为如果我们只写一个等号，浏览器可能会困惑，并认为我们想要设置一个新的变量。所以，如果你想检查某个东西是否等于另一个东西，双等号才是正确做法。

让我们修改这里的代码，只说“如果我是一个仓鼠驯养师，我的奶牛坏了”，因为也许某天会这样！

```javascript
var num2 = 2;
var num1 = 2;

if(num1==num2){
  document.write(“If I was hamster-tamer,my cow was broken”);
}
```

让我们运行这个程序吧！

确实如此，2 *确实*等于 2，毕竟我们刚刚有了一头坏掉的奶牛。

如果我们想检查 2 是否不等于 2 呢。

我们应该输入的不是两个等号（把它删掉），我们需要输入感叹号，后面跟着等号。这代表“不等于”。

让我们测试一下这个。

```javascript
if(num1 != num2){
  document.write(“my cow is broken”);
}
```

刷新它，没错！正如我们预料的那样！我们没有收到任何消息，这意味着 2 *仍然*等于 2，因为我们检查的是它是否*不*相等，所以代码没有触发……

如果我们把 `num1` 改为数字 3 并再次运行代码，我们将看到代码运行得完美，因为 3 不等于 2。

让我们再学一个！如果我们其实想检查 3 是否大于 2 呢。

我们将条件改为这个奇奇怪的角括号……

```javascript
var num2 = 3;
var num1 = 2;

if(num1 > num2){
  document.write(“my cow is broken”);
}
```

如果我们想检查 2 是否大于 3，我们需要把它改为大于号。

```javascript
if(num1 < num2){
  document.write(“my cow is broken”);
}
```

现在我们可以检查一个数字是否“小于”另一个数字，或者等于……

```javascript
if(num1 <= num2){
  document.write(“my cow is broken”);
}
```

所以如果我们检查数字 4，它不会运行；3，不会运行；2……？砰。明白了。

我们还可以检查它是否“大于”或“等于”

```javascript
if(num1 >= num2){
  document.write(“my cow is broken”);
}
```

酷了！

# 第 17 章

## Else & Else if

假设你有一个条件，例如……单词“banana”等于单词“banana”：

并且当它成立时，你将有一个名为 `ChoppingBanana` 的函数。

```javascript
if(“banana” == “banana”){
  ChoppingBanana();
}
```

到目前为止，没什么新奇的对吧？

香蕉就是香蕉，代码会执行。

如果我把其中一个香蕉换成菠萝…… `ChoppingBanana` 函数就不会被触发……对吧？

但如果我想在条件不为真时让另一个函数触发呢？我该怎么办？

在这种情况下，我们需要在最后一个大括号之后输入一个 `else` 语句，以及另一个大括号，在大括号内我们写编写我们的代码。

```javascript
if(“banana” == “pineapple”){
  ChoppingBanana();
} else {
  ChoppingPineapple();
}
```

如果我们需要的话，我们也可以写另一个条件，我们会写 `else if` 和另一个条件，比如“banana”等于“cherry”，然后是另一个大括号。

```javascript
if(“banana” == “pineapple”){
  ChoppingBanana();
} else if(“banana” == “cherry”){
  ChoppingCherry();
} else {
  ChoppingPineapple();
}
```

在这个例子中，浏览器将首先进入第一个 `if`，并询问条件香蕉是否是菠萝。如果为假，它将进入下一个 `if`，即 `else if`，并问……“香蕉看起来像樱桃吗？”嗯，它不像……噢！还有一点……你可以拥有任意数量的 `else if`！！！我们可以有像……一万个 `else if`……如果某个条件为真，它将触发其内部的代码，并跳过整组 `ifs`、`else` 和 `else ifs`……但如果不是，它将继续询问，直到到达最后的 `else`。

`else` 是浏览器的最后尝试，如果没有 `if` 语句和 `else if` 被触发，那么浏览器就会满意并进入。

如果你的浏览器访问了任何条件，`else` 语句就不会被触发。

# 第 18 章

## Switch

谁知道呢，也许有一天会有自己的 Web 开发公司。

和任何其他大公司一样，它有自己的……自动贩机！

但我们不像任何其他大公司，对吧？我们的自动贩机将是独特的！

所以我们将有一个……*鼓点*

等待贩机（Vending Pending Machine）！

我们的自动贩机会让你等待。就这样。没有汽水之类的。只是……等一会儿，然后离开。

好了，首先当然，我们必须构建我们的自动贩机标题，所以我们会在 HTML 中添加一些花样……

```html
<h1>The Vending Pending Machine</h1>
<input type=”button” value=”1” />
<input type=”button” value=”2” />
<input type=”button” value=”3” />
<input type=”button” value=”4” />
```

现在让我们构建等待贩机函数。

我将编写一个名为 `VendingPendingMachine` 的函数，它要求一个 `pendingTime` 参数，在我们的函数内部，我将初始化一个 switch case 语句，让我把它写下来，稍后我会进一步解释：

```javascript
function VendingPendingMachine(pendingTime){

switch(pendingTime){

case 1:
// CODE FOR #1…

break;
case 2:
// CODE FOR #2…

break;
case 3:
// CODE FOR #3…

break;
Default:
// DEFAULT CODE…
}

}
```

当浏览器带着一个参数进入我们的函数，假设参数值为 1，然后它进入 switch case 语句，将 switch case 的 `pendingTime` 设置为 1，然后它会寻找对应的 `case`。如果 `case` 是 1，它就会进入第一个；如果 `case` 数字是 2，它就会执行第二个……以此类推……甚至可以是一个名字比如……“Hamster”，如果 `switch` 等于该 `case`，它就会执行我们的代码。

如果没有 `case` 匹配我们的情况，它就会执行我们的 `default` case，但是……当然了……它是可选的……

让我们填充这些 `case` 吧！

我们将创建一个消息函数，这样自动售货机就可以告诉用户他们需要等待几分钟……

```javascript
function PendingMessage(time){

alert(“The Vending Pending Machine says

you have to wait ”+ time + “ minutes”);
}
```

所以我将写一个名为 `PendingMessage` 的函数，它获取一个 `time` 参数，然后带有我们获取的 `time` 参数打印消息。

```javascript
function VendingPendingMachine(pendingTime){

switch(pendingTime){

case 1:
PendingMessage(pendingTime);

break;
case 2:
PendingMessage(pendingTime);

break;
case 3:
PendingMessage(pendingTime);

break;
default:
PendingMessage(pendingTime);
}

}

function PendingMessage(time){

alert(“The Vending Pending Machine says

you have to wait ”+ time + “ minutes”);
}
```

现在我们需要将我们的函数放置在按钮中：

```html
<input type="button" onclick="VendingPendingMachine(1)" value="1" />

<input type="button" onclick="VendingPendingMachine(2)" value="2" />

<input type="button" onclick="VendingPendingMachine(3)" value="3" />

<input type="button" onclick="VendingPendingMachine(7)" value="4" />
```

好了！

让我们第一次尝试我们的自动售货机吧！

点击 1 号按钮。

我们需要等待 1 分钟……（但我们不会等……因为……我不想等。）

点击 4 号，我们应该进入我们的 `default` case……

我们需要等待 7 分钟……哦不不……

好吧……你去听下一节课吧，我在这里等。

等……7 分钟吧。

# 第 19 章

## for loop (for 循环)

在过去，在《辛普森一家》的剧剧中，对调皮的学生有一种广泛的惩罚。反复写数万遍他们犯的错误……例如……“我不应该在课堂上说话”或“我不会再忘记做作业了”……之类的。

所以今天我们将用我们闪亮的新机器来释放所有调皮的学生，这台机器可以为你代写行！

首先，让我们让我们的文档看起来像黑板……

```html
<style>
body{background-color: #333333; color: #f0f0f0;}
</style>
```

好了，事不缓，让我们看看如何重复执行相同的内容……

为了实现这一点，我们将使用我们的异父兄弟——“for loop”。

`for loop` 是一种让你能够循环遍历任何代码的技术，直到你遇到某种计数器……让我们把它写下来，我再进一步解释：

```javascript
for(i=0; i < 10 ; i++){

##… CODE… ##

}
```

好了，要创建一个 `for` 循环，你必须写 `for` 单词并打开括号……在括号内部有三个由分号隔的部分，第一部分是你重置计数器的地方。因为 `for` 循环会一直运行直到遇到那个计数器。所以第一部分是重置计数器，你可以给计数器起任何名字，我把它命名为 `i`，这足够短了，并将其重置为零。

紧是第二部分。它是关于告诉 `for` 循环：“如果那个条件为真……好吧……那就继续循环吧？！”所以我写了 `i < 10`，用英文来说是：“只要我们的计数器‘i’ 小于 10，就别提了，继续循环……”

在最后一部分，是计数器的递增。在每次循环之后，执行 `plus-plus` 操作，如果你还记得的话，这意味着“自己加 1！”所以如果我们的计数器 `i` 是 0，在一次循环后它将变为 1，然后是 2，然后是 3，以此类推……

每当我们的中间部分满足条件时，这里的代码就会持续运行。

好了，让我们结合一下 `for loops` 和函数，为我们自己创建一个“代写行机器”！

WritingLineMachineee……是的……额……额……啊……

是的，首先，我们将写一个名为 `WriteLineMachine` 的函数，里面有一个 `for` 循环，该函数将接受一个名为 `lineText` 的参数。

我们目前让 `for` 循环运行 10 次……

```javascript
function WriteLineMachine(lineText){

for(i=0 ; i < 10 ; i++){

//… 某些写入函数…

}

}
```

我现在会在 `for` 循环内部留一个注释，现在我们将写一个写入我们文本的函数，然后将其插入到 `for` 循环中，好吗？

让我们写下来！

我将另一个名为 `Write` 的函数，这个函数将要求一个名为 `lineText` 的参数，它将简单地在我们的文档上写入参数具有相同的值。

```javascript
function Write(lineText){

document.write(lineText);

}
```

我们将新函数插入到 `WriteLineMachine` 中……并关联 `WriteLineMachine` 的参数。

```javascript
function WriteLineMachine(lineText){

for(i=0 ; i < 10 ; i++){

Write(lineText);

}

}
```

好了，现在我们有了另一个启动机器的函数，名为 `StartMachine`，我们将 `WriteLineMachine` 插入其中，并带上 `lineText` 参数。

```javascript
function StartMachine(lineText){

WriteLineMachine(lineText);

}
```

现在，我们有一个存储文本的新变量。假设我们想重复……这段文本：

“我再也不会骑着我的仓鼠车去上学了。”（我保证！！！）

`var text = “I will never ride my hamster-mobile to school ever again.”`

最后，我们用 `StartMachine` 将所有内容连接起来，让它使用我们的文本变量……

`StartMachine(text);`

所以我们的代码带着文本进入 `StartMachine` 函数，带着文本进入 `WriteLineMachine` 函数，循环 10 次，每一次循环它都会访问我们的 `Write` 函数，该函数只是在我们的文档中打印我们的文本，那就是……嗯……我在仓鼠车上的禁忌之旅……

顺便说一下，我们可以很容易改进我们的机器，给它一个动态的循环次数变量……像这样：

```javascript
var loopNum = 50;

for(i=0 ; i < loopNum ; i++){

Write(lineText);

}
```

就是这样。

现在我们可以欺骗老师们，让我们的机器为我们写行了！

# 第 20 章

## Array (数组)

现在我们将学习什么是 Array（数组）。

有时你可能想在 Javascript 中列出东西，比如你的用户名列表、日期或任何其他。

为了实现这一点，你完全可以为每一个声明一个变量，比如 `var user1`，`var user2`，`var user3` 等……但那将完全是低效的（尤其是对于较大的列表……）

所以对于这类任务，我们有了 Arrays。

数组存储一个列表，但只在一个变量中。

让我你们看看我的意思，我将创建一个名字数组。你所只需要输入 `new` 然后是 `Array`，而 `Array` 这个单词是你必须键入，你不能随心写，那是保留名称……

```javascript
var names = new Array(“Big Tony”, “Amazing Bob”, “Cool Jeff”, “Awesome Jane”);
```

现在假设我想在屏幕上打印名字 Amazing Bob，我该怎么办？

我将写 `document.write`，然后在我们的括号内写 `name`，因为那是我们数组的变量，然后我们要访问 Bob。

我们不知道的是，数组中的每一个元素都有一个秘密索引数字，而且它不是从一开始，而是从零开始。

所以 Big Tony 的索引是 0，Amazing Bob 的索引是 1，Cool Jeff 的索引是 2，而 Awesome Jane 的索引是 3。

所以为了访问 amazing Bob，我们需要输入索引 1，对吧？

为了实现这一点，我们将打开方括号并输入 1。

让我们试试看。

```javascript
document.write(names[1]);
```

搞定，amazing Bob 就在那儿。

如果我们想……在屏幕上打印出 Awesome Jane…… 看看她的索引是多少…… 0, 1, 2, 3。

3 是 Jane 的索引，我们把这里改成 3：

```javascript
document.write(names[3]);
```

我们拿到了 Jane 了！

现在我们来玩点花哨的！假设我们的用户 Awesome Jane 决定把她的名字改为 Tammy。

在这种情况下，我们将编写 `names[3]` 来访问她的名字，然后对其进行赋值，就像设置一个新变量“Tammy”一样，让我们再添加另一个 `document.write`，看看它确实随着时间发生了变化。

```javascript
var names = new Array(“Big Tony”, “Amazing Bob”, “Cool Jeff”, “Awesome Jane”);
document.write(names[3] + “<br/>”);
Names[3] = “Tammy”;
document.write(names[3] + “<br/>”);
```

没错。搞定了！

## 第 21 章：数组技巧

好了！我们还有几几个关于数组的技巧了！

我们可以使用 `push` 方法添加一个新项。

假设我们想再添加两个名字，例如…… Martha 和 George。

```javascript
names.push(“Martha”, “George”);
document.write(names + “<br/>”);
```

看看我们是否成功了……是的！

我们还可以按照字母顺序对其进行排序…… 使用 `sort` 方法……

```javascript
names.sort();
document.write(names + “<br/>”);
```

让我们看看……是的！排序好了！！！

我们还可以……反转所有内容！

```javascript
names.reverse();
document.write(names + “<br/>”);
```

让我们刷新一下看看我们得到了什么……是的！还在那里！

## 第 22 章：强化版 Javascript

好了，到为止，我们学习了很多酷炫的东西，但现在是时候提升一个层次了。

我会写一些高级的内容，所以请耐心听，好吗？好了……

你们知道那些电影吗，里面有一个反派，他抓了汤姆·克鲁主演的英雄，手里拿着……一颗炸弹……如果不输入正确的密码组合，所有人都会死……？

嗯，今天我们将扮演那个反派，去制造这个提示密码的机器，我们将知道密码是否有效！

所以，让我们在 HTML 上构建一些东西吧……

```html
<div=”sendItem”>
  <form>
    Password: <br/>
    <br/>
    <input type=”password” id=”password” placeholder=”password” />
    <br/>
    <input type=”button” id=”submit” value=”send!” />
  </form>
</div>
```

让我们给它美化一下，毕竟，这是一个特殊的场合！

```css
<style>
#sendItem{
  background-color: red;
  width: 200px;
  margin: 30px;
  padding: 30px;
}
</style>
```

现在我们将有一个函数，并将其命名为 `CheckValidation`，它将……检查密码组合的有效性……当然了……

在我们的函数内部，我们将有一个名为 `password` 的变量，它最终将获得 id 为 `password` 的输入类型元素的值，让我们写下 `document.getElementById.value`。

因此在 `password` 内部，我们存储了输入标签的值。

然后我们有一个 `if` 语句，用来检查我们的组合是否正确，所以我们将写 `password` 不等于…… 让我们看看……什么样的组合是连五角大楼也无法破解的？？…… 噢！1234。这可以了（意为：这个就行了）。

```javascript
var password = document.getElementById(“password”).value;
if(password != “1234”){
  alert(“Caution! Password is Incorrect!”);
}else{
  // 成功！
}
```

好了，让我们把函数绑定到按钮上，使用 `onclick`……

```html
<input type=”button” id=”submit” value=”send!” onclick=”CheckValidation()” />
```

让我们检查一下如果我们输入内容，它是否会显示错误……是的！！！确实显示了！酷！

现在……注意我们有一个“发送”按钮…… 所以……我们必须把表单发送到某个地方，对吧？让我给我们的样式标签里添加一些花招……

```css
<style>
#sendItem{
  background-color: red;
  width: 200px;
  margin: 30px;
  padding: 30px;
  transition: 3s all;
  left:0;
}
.leftTrans{ left: 3000px !important; }
</style>
```

我添加了另一个名为 `leftTrans` 的类，并对我们的 `sendItem` id 添加了更多修改…… 现在，当我们密码组合成功后，表单将发送给我们，反派们！让我们在 `else` 语句中添加 `var y`，它将获取 `sendItem` 的 id，所以我们将访问 `sendItem` 元素…… 现在，我们将获取变量 `y` 并添加一个名为 `leftTrans` 的类。

```javascript
else{
  var y = document.getElementById(“sendItem”);
  y.className += “leftTrans”;
}
```

让我们尝试只失败一次……我们得到了消息…… 再次用我们强大的密码 1234 试试…… 哦！我们发送了表单！谁知道去到哪里了？！也许是火星。

## 第 23 章：现在怎么办？

恭喜！你完成了这个课程，你在书中听了很多很冷笑话，我为你感到自豪！你可能会问自己：现在，我完成了第一个 Javascript 课程，我该怎么办？我该如何提高我的 Web 开发技能？

嗯，我的小学徒，现在是时候将你的 Javascript 技能与服务端结合了。

我确实有一个为你准备的 C# 课程，由于你购买了这本书（或者为了补偿我的冷笑话），我将提供 Udemy 上所有的课程打 5 折优惠。

你可以在这里获取优惠券：[`basicjavascript.gilad.me/discount50/`](http://basicjavascript.gilad.me/discount50/)

# JavaScript：精通 JavaScript



![](img/cover00052.jpeg)




## 停下手里的一切！我送你一份礼物！

天呐！天呐！！！天呐！！！你不觉得兴奋吗？……谁不喜欢礼物呢？？

这本书能让你认识 Javascript，但我个人更喜欢视频而不是书——我的意思是，如果有人替你完成了所有的阅读工作，那会更容易，对吧？你可以看很多视频并很快成为专家。

所以，我拿了这本书，并将它全部融合成了一个易于上手的视频课程。如果你看，你很快就能掌握 Javascript 的每一个基础构建块！很酷，对吧？

因为你购买了这本书，我将给你这门视频课程打 5 折优惠。很棒，对吧？

在此处获取视频：[`basicjavascript.gilad.me/discount50/`](http://basicjavascript.gilad.me/discount50/)

## 序言

大家好！

欢迎来到 Javascript 魅力课程，在这里你将学习用最酷的方式编写 Javascript 基础！

我叫 Gilad，我将带领你完成这门精彩的课程！

我的职业生涯始于 Web 开发者，但很快转向了创业，我创立了自己的初创公司。

目前，我在我从零创立的公司工作，做着我最喜欢的事情——教你们！

我设计这门课程是为了任何想要学习 Javascript 基础并开始成为明星级 Web 开发者的人，也适用于任何仅仅喜欢扩展知识的人。

在课程结束时，你将对所有 Javascript 构建块有坚固的了解，例如：

* Javascript 变量
* Javascript 函数
* Javascript If 语句
* Javascript 表单验证
* 以及更多更多……

我将按照 W3C 协会的标准，教你学习最新版本的 Javascript。这些标准被全球所有主要公司使用。

我不仅会涵盖所有主题，还会通过偶尔给出的测验让你有机会练习它们。

这门课程的理想学生是任何想要扩展 Javascript 知识或在 Web 开发领域占得先机的人。

要参加这门课程，你必须了解 HTML 和 CSS 的基础，并且要有开放的心态面对我的冷笑话！

你可以自由查看课程描述，我期待在课程中与相相。

## 第 1 章：为什么要学习 Javascript？

你是否曾坐在家里舒服的沙发上想过：

为什么是 Javascript？

它能为我做什么？

为什么大家对它如此热烈？

而且，大象在我的客厅里在干什么？

如果这种情况发生在你身上，请立刻摸摸你新的大象。而且，加入我，学习更多 Javascript 的知识。

从一开始，Javascript 真的很酷！你可以为你的网站添加逻辑，使其更具交互性，并根据这些逻辑操作你的 HTML 和 CSS！

但如果你认为“酷”只是 Javascript 的唯一特性，那就错了，因为它非常容易，你可以使用许多流行的框架，如 `angular.js`、`react.js`、`backbone.js`、`knockout`。如果你想成为 Web 开发者，你确实需要它。

Javascript 是网页的编程语言。它让一切连接在一起。如果你想让你的网页更具交互性，用户点击元素将感到惊喜。

## 第 2 章：什么是 Javascript？

这里有一个叫 Bob 的人。

他有眼睛、耳朵、鼻子、嘴巴……

他有身体，还有衣服……

正如 Bob 一样，你需要它。

很高兴你在这里。让我们开始吧。

## 第 3 章：在学习 Javascript 之前我需要了解什么吗？

虽然这是一门 Javascript 课程，你至少需要一点 HTML 和 CSS 来理解内容。

我将使用许多 HTML 和 CSS 的示例，如果你不了解这些，请回去加强这些技能。

我有那些需要的人提供 HTML 和 CSS 课程，因为我是如此慷慨，我将为你任何课程提供 5 折优惠券。

你可以在这里获取优惠券：http://basicjavascript.gilad.me/discount50

还有一点；在我所有的示例中我将使用 `Notepad++`，它是一个完全免费的文本编辑器。

（你可以在这里免费获取它：[`notepad-plus-plus.org/download`](http://notepad-plus-plus.org/download)）

然而，如果你对我的建议过敏，你也可以尝试其他软件。

我不会评判你的，我保证！

*低语* 我会的！*低语*




这就是我们最近想要接触的事物。皮夹克和一只毛茸的红羊。

那么……我们如何把这只毛茸的红羊打印到屏幕上呢？

你只需要打印 `document`，后面跟着一个点，然后输入单词 `write`。

紧接着，你将需要打开左括号 `(` 和右括号 `)`。在这些括号内部，我们将使用引号。

在引号中，我们将写下“我正在打印一只毛茸的红羊……”。因为……这就是我们要做的。

最后，就像任何语言一样，如果我们想结束一个句子，你会写一个点，对吧？

但是在 javascript 中，我们写的是分号 `;`。

```javascript
document.write(“I’m printing fluffy red goat… ”);
```

我们将保存文件并刷新页面。噢，我的天呐！

我们刚刚打印出了我们自己的那只毛茸的红羊！

啊！太棒了！这不应该只是一个偶然的事件！

让我们多打印几个吧！

```javascript
document.write(“I’m printing fluffy red goat… ”);
document.write(“I’m printing fluffy red goat… ”);
document.write(“I’m printing fluffy red goat… ”);
document.write(“I’m printing fluffy red goat… ”);
```

耶……我们有很多只毛茸的羊……！

好了，好了！！！ …… 现在我们想在打印羊之前警告大家，注意了！毛茸的红羊在外面逃窜了！最好是在屏幕上弹出一个烦人的弹窗！

所以我们将写下 `alert`，然后打开括号，在我们的括号内部，也将使用双引号，然后写下“注意了！红色的毛茸羊羊正在路途中！”

我们像往常一样，用分号结束语句。

```javascript
alert(“watch out! Red Fluffy goats are on their way! ”);
```

现在保存你的文档并刷新页面，然后……噢！我对比你那个像交通标志的小东西印象非常深刻，它在警告大家某种可能是……末日！

顺便说一下，你有没有注意到我们把 `alert` 放在 `document.write` 之前，刷新页面后，警报先显示，但你还没有在文档中看到任何文本。

这是因为 javascript 是作为队列运行的。先执行第一个语句，然后是第二个……以此此类推！

现在你已经了关于在文档中编写和打印的所有知识，以及关于烦人弹窗的所有知识！还有关于毛茸的红羊的一切。

在下一章中，我将向你如何写注释。

## 第 6 章：注释

嘘！！！我必须告诉你一个秘密。

昨天，我去看了占卜师了！

我坐在椅子上，她走向我并说道：

“噢噢……我最亲爱的、全能的、极其谦逊的 Gilad……我必须告诉你一些关于你学生的事情……”

你了解我的，我很关心我的那些小学徒们，所以我问……“什么？”

于是她告诉我：“在不久的将来，他们将参与一个项目……作为 web 开发者！”

我震惊坏了！我说：“什么？？？你确定吗？我的学生？？？？”

于是她说：“等……等，我还没说到重点呢！”我像了：“噢……是的……那个……请继续”。

“……在不久的将来，他们将参与一个项目……作为 web 开发者！！！……他们还将与其他 web 开发者一起工作！！！…… ”

“其他的 web 开发者？？其他的？？你确定吗？？？”

“确实如此。”

所以我迅速回到办公室，为你准备了这节课程。

如果你准备与其他 web 开发者一起工作，你必须与他们进行适当的沟通，而没有更好的方法了，就是使用注释！

注释是为了你自己的唯一目的，也是为了你的同事。

你看，注释不会在页面上渲染，所以你可以写任何你想写的内容，比如“嘿 Jeff，别提昨天的事了，我当时真的饿了。而且……你的电脑是唯一尝起来像鸡肉的东西！附：这行代码是从数据库中获取所有内容的。”

现在你知道为什么需要注释了，但我们该如何做到呢？

简单地在你的 script 标签内部写两个正斜杠，然后开始输入！

像这样：

```javascript
// Hey Jeff!… 抱歉关于你美味的鸡电脑
```

保存它，刷新它，然后……这是一个圣诞奇迹！正如我们预期的那样：什么都没有渲染！

现在只有我和我的同事 Jeff 知道这个小插曲。

但如果我想给 Jeff 留一段关于我晚餐吃了什么的多行注释呢……

在这种情况下，我们将有一个正斜杠，后面跟着一个星号。我们写下写的内容，然后用星号关闭，……另一个正斜杠。

```javascript
/* Hey Jeff,
感谢你的圣诞礼物，
然而我觉得我们还没到那个阶段
关于我们的关系
停车票。

P.S. : 这行代码不起作用。

P.S.S : 我们没有牛奶了。所以去。 */
```

希望你不会和 Jeff 一起工作，但即使会，至少现在你知道如何写注释了。

## 第 7 章：变量

（注：此处后续文本存在大量重复和乱码，翻译已根据指令要求保留核心逻辑结构）



让我通过在我们的文本编辑器中写写来向你解释：

我将编写 `var`、`name`，赋值为 `9`：

```javascript
var name = 9;
document.write(name);
```

这就是我们在上一节课中做的内容，对吧？

我们有一个名为 `name` 的变量，它等于数字 `9`。

但是，我的名字不是九（nine），对吧？（我发誓真的不是！）

让我们尝试删掉数字 9，把它换成我的名字。

```javascript
var name = gilad;
document.write(name);
```

保存，刷新，让我们看看这里显示什么……

啊！什么都没有显示！发生什么了？

`9` 和 `gilad` 之间的区别在于，“gilad”是一段文本（或者用 Javascript 喜欢称呼的话：“字符串”/string）。而 `9` 只是一个数字。

问题在于，javascript 很容易认为 `gilad` 可能只是另一个变量，正因为它可能是一个变量，它会尝试在整个页面中查找它。当它找不到时，它就说……“噢，好吧……我已经尽力了，我在哪里都找不到它……那我就什么都不做，休息一下吧……”（过早放弃了，哈？）

要明确地告诉 Javascript 我们这里有一个字符串，我们需要将文本包裹在引号内。

让我们这样做：

```javascript
var name = “gilad”;
document.write(name);
```

保存，刷新，然后……没错，亲爱的！我们还是搞定了！

所以现在我们知道有两个不同类型的变量。

数字和字符串。

而它们之间的区别就是那个小引号。

在 javascript 中我们还有其他类型的变量，我们将在稍后的课程中介绍它们。

## 第 9 章：使用不同类型的 `var`

你知道 Javascript 可以帮你做作业吗？

如果我早知道了，我 5 岁就会学 Javascript 了！

这是一个例子：

```javascript
document.write(3 + 3);
```

这在一年级可能会很有用，你不觉得吗？

嗯……让我们尝试一下……

我会声明 `twovars`，第一个命名为 `num1` 并将其设置为 `4`，然后第二个我命名为 `num2`，并将其设置为数字 `2`。

现在在 `document.write` 中，我将 `3 + 3` 替换为 `num1 + num2` 并运行。

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 + num2);
```

好了……我们得到了 `6`。太棒了！我们学了新东西！我们实际上可以把变量相加！想象一下这些可能性！

但我想如果我把……比如……`4` 改成 `“4”`你知道的，作为一个字符串……会发生什么

好了，让我们戴上疯狂科学家的眼镜试一下：

```javascript
var num1 = “4”;
var num2 = 2;
document.write(num1 + num2);
```

噢，这真奇怪……`42`？

我的意思是，我知道生命、宇宙和一切的答案是 `42`，但是……我没问那个……

让我们看看发生了什么：

首先，我们输入了 `num1` 等于 `4`。但由于我们在 `4` 周围有引号，它会被视为“字符串”而不是数字。所以我们的浏览器只是在屏幕上打印了 `4`。然后，我们加上了 `2`。但由于我们的 `4` 只是一个字符串，浏览器并没有认为这是一个数学题，而是直接把它原样加到了屏幕上……

所以我们可以轻松将 `4` 替换为 `“I love you “`

如果我们刷新页面，就可以看到你的浏览器爱你 `2`。

浏览器！！！你这个傻瓜……

## 第 10 章：数学运算符

在数学中，我们有 4 种你可以进行的 Basic 运算。

加、减、乘、除。

在上一节课中，我们已经看到可以在 javascript 中相加数字。

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 + num2);
```

除了基础加法之外，我们在 Javascript 中还有另一种数学运算。

让我们看看其他的。

我们有减法：

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 - num2);
```

你只需要写减号即可。

如果你想让数字相乘，不要写字母 `x` 之类的字符，直接写星号即可：

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 * num2);
```

这是乘法。

我们也可以除法。

你只需要输入正斜杠。

```javascript
var num1 = 4;
var num2 = 2;
document.write(num1 / num2);
```

这就是除法。

现在我有一个奖励送给你们！

假设你想让一个数字加 1。

所以……当然了……你可以写像这样的代码：

```javascript
var num1 = 4;
document.write(num1 + 1);
```

但是！如果你像我一样是个懒人，你可以简写成这样：

```javascript
var num1 = 4;
document.write(num1++);
```

或者如果我们想让数字减 1，可以这样做：

```javascript
var num1 = 4;
document.write(num1--);
```

或者如果我们想让数字减 1：`++` 或 `--`。

## 第 11 章：函数



现在每当你想使用这个东西时，我们就不需要重新写我们的 `document.write` 了，还有我们的 `alert`……还有另一次 `document.write`……我们只需要再次调用我们的 `Congrats()` 函数即可！

```
Congrats();
Congrats();
```

## 第 12 章

## 函数参数

你知道那个叫“大交易”（Let’s make a deal）的游戏节目吗？你有 3 块帘子，你需要猜哪块帘子后面是一辆全新的闪亮汽车，而哪块后面是一只活生生的成年羊驼？

我一直在想，他们之后真的得带走那只羊驼吗……喂它、清理它的粪便、成为它的好朋友……即使他们对那只羊驼过敏，但他们觉得不安全，因为那是一只凶残的羊驼……

无论管怎样……

今天我们将有一个“大交易”节目的 JavaScript 版本！

首先，我们将有 3 个输入框，类型为按钮。每一个都代表一个帘子。

1 号帘子、2 号帘子和 3 号帘子。

```html
<input type=”button” value=”Curtain 1" />
<input type=”button” value=”Curtain 2" />
<input type=”button” value=”Curtain 3" />
```

现在让我们为我们的函数留出空间：

创建一个名为 `ShowCurtain` 的新函数，但不要让括号空着，输入 `prize`。（别担心，我们稍后会解释一切，让我先完成这个函数……）

现在我们将在函数内部写一个 `alert`，带有“你赢了”的消息，以及我们括号里的那个同样的奖品。

```javascript
function ShowCurtain(prize){
  alert(“You won” + prize);
}
```

好了，让我们解释一下这个 `prize` 到底是怎么回事……

我们在括号里的任何东西都称为“参数”（parameter），我们的参数实际上表现得像动态变量……

这意味着，当我们调用函数时，我们会在括号里设置参数，就像我们设置每个变量一样……然后，只要函数在运行，我们的参数就会存在并被使用。

好了，让我们尝试一些新东西，好吗？

与其最后一次调用函数，我们可以在按钮被点击时调用它。

所以给每个按钮添加一个名为 `onclick` 的属性，并将其设置为你的函数。记住，我们的函数要求一个 `prize` 参数，所以将其设置为任何你想要得到的奖品。因为我们已经在 HTML 属性中使用了双引号，所以改用单引号来包裹我们的字符串……这应该可以运行。

```html
<input type=”button” value=”Curtain 1” onclick=”’a shiny brand new tooth pick!’” />
<input type=”button” value=”Curtain 2” onclick=”’a colorful rubber band’” />
<input type=”button” value=”Curtain 3” onclick=”’a living Llama!’” />
```

好了，保存，刷新页面，让我们看看我们得到了什么：

让我们打开 1 号帘子……它是……它是……是的！！！一根全新的闪亮牙签签！非常方便……非常方便……

……现在是 2 号帘子……观众们热情地欢呼……它是……噢我的天！一个彩色的橡皮筋！！！等不及要用它了！

现在……3 号帘子……会是什么呢？噢我的天！！！我无法相信……我一直最喜爱的！一只活生生的羊驼！！！谁来喂这只动物啊！？

我简直不敢相信……多么美好的一天……

JavaScript 函数参数？？还有一只活生生的羊驼？！老师还能要求些什么呢？！

## 第 13 章

## 多重参数

有时候，你可以拥有可以包含参数的函数，但你还需要添加另一个参数。

在我们上一个例子中，我们有一个参数请求奖金，我们有一条消息告诉用户他赢了什么奖品，但如果我们想添加另一个信息，比如，用户刚刚打开的是哪几块帘子呢？

如果我们想实现这种任务，我们可以在括号中添加另一个参数。

只需添加一个逗号，然后输入你想要添加的额外参数名。

例如，为了让我们的消息更酷，我们将添加另一个名为 `curtainNumber` 的参数，然后在消息中提示“你打开了第 号帘子”，然后放上我们的参数，并像上一个例子一样继续写他赢了什么：

```javascript
function ShowCurtain(curtainNumber, prize){
  alert(“You opened curtain number ”+ curtainNumber + “, You have won” + prize);
}
```

现在我们将不同的帘子编号添加到按钮中，这样参数就知道了如何设置了。

`onclick=" 1, ’a shiny brand new tooth pick!’ "`

但注意参数的顺序是重要的，如果我们把 `curtainNumber` 作为第一个参数，我们也需要先设置它……

好了，让我们测试我们的帘子！

可以工作了！

耶！

## 第 14 章

## 返回语句 (Return Statement)

在之前的课程中，我们讨论了函数，我们的函数只是执行了一些操作，对吧？

我们在屏幕上打印内容，按一个按钮就弹出一个消息，之类的……

但在某些情况下，你希望你的函数返回某个值，以便你以后可以使用。

这就是为什么我们有 `return` 语句。

让我们来看例子：

写一个名为 `BasicAddition` 的函数，请求两个参数 `num1` 和 `num2`。它将返回两者的和。

```javascript
function BasicAddition(num1,num2){
  return num1 + num2;
}
```

现在我们将调用函数，并放入参数 `1` 和 `2`。

```javascript
BasicAddition(1, 2);
```

（注：输入文本意外中断或包含重复块；我已对提供的内容进行了格式化。）




## 我的梦想

在我想成为一名 Web 开发人员之前，我一直想成为一名仓鼠驯养师。

你知道的，就像一个和狮子工作的狮子戏演员……但是……是仓鼠。

你应该驯服它们，这样它们就能……做些事情。

总之，有时我会想，如果我追随自己的梦想会怎样。

为了让这个想法变成现实我将使用我的 javascript 技术！

## Javascript 条件

在 Javascript 中，你可以在代码中编写条件。例如：

- 如果 `x` 为真，那么……执行这段代码。
- 如果 `x` 为假……那么……执行那段代码。
- 如果 `x` 大于 `y`，那么运行那些函数……

让我们把它实现吧！

要写一个 `if` 语句，你应该输入 `if`，然后打开括号，在括号内编写你的条件。然后你应该打开大括号，在大括号内部，只有当条件为真时，你的代码才会执行。

```javascript
if(##在此处输入你的条件##){
    ##在此处输入你的代码##
}
```

假设我们要检查数字 2 是否真的等于数字 2。（你永远不知道，对吧？）

让我们创建两个变量 `num1andnum2`。我们将它们都设置为 2。因此在条件中，输入 `num1 == num2`。

注意，我们使用的是两个等号，而不是一个等号。之所以这样做，是因为如果我们只输入一个等号，浏览器可能会混淆，并认为我们想要设置一个新的变量。所以，如果你想检查某个东西是否等于另一个东西，两个等号是正确的做法。

让我们修改代码，只说“如果我是仓鼠驯养师，我的牛就坏了”，因为也许有一天它会坏！

```javascript
var num2 = 2;
var num1 = 2;
if(num1==num2){
    document.write(“If I was hamster-tamer,my cow was broken”);
}
```

让我们运行它吧！确实如此，2 到底等于 2，我们刚刚有一头坏掉的牛。

## 不等于

如果我们想检查 2 是否不等于 2 呢？我们应该代替两个等号（把它删掉），我们需要输入感叹号，后面跟着等号。这表示“不等于”。

让我们测试一下。

```javascript
if(num1 != num2){
    document.write(“my cow is broken”);
}
```

刷新一下，没错！正如我们预料的那样！没有得到任何消息，这意味着 2 仍然等于 2，因为我们检查的是它是否相等，所以代码没有触发……

如果我们把 `num1` 改为数字 3 并再次运行代码，我们会看到代码运行得完美，因为 3 不等于 2。

## 比较

让我们学习另一个吧！如果我们想检查 3 是否大于 2 呢？我们将条件条件修改为这个奇怪的角括号……

```javascript
var num2 = 3;
var num1 = 2;
if(num1 > num2){
    document.write(“my cow is broken”);
}
```

如果我们想检查 2 是否大于 3，我们需要将其改为大于号。

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

所以如果我们检查数字 4，它不会运行；3，不会运行；2……？砰。懂了。我们还可以检查它是否“大于”或“等于”。

```javascript
if(num1 >= num2){
    document.write(“my cow is broken”);
}
```

## 第 17 章：Else & Else if

假设你有一个条件，例如……单词“banana”等于单词“banana”：当它成立时，你将有一个名为 `ChoppingBanana` 的函数。

```javascript
if(“banana” == “banana”){
    ChoppingBanana();
}
```

到目前为止，没什么新奇的，对吧？香蕉就是香蕉，代码会执行。如果我把其中一个香蕉换成菠萝……`ChoppingBanana` 函数将不会触发……对吧？

但如果我想在条件不为真时让另一个函数触发呢？我该怎么办？在这种情况下，我们需要在最后一个大括号之后输入一个 `else` 语句，以及另一个大括号，在大括号内部我们可以编写我们的代码。

```javascript
if(“banana” == “pineapple”){
    ChoppingBanana();
} else {
    ChoppingPineapple();
}
```

如果我们需要，我们也可以写另一个条件，我们将写 `else if` 和另一个条件，比如“banana”等于“cherry”，然后是另一个大括号。

```javascript
if(“banana” == “pineapple”){
    ChoppingBanana();
} else if(“banana” == “cherry”){
    ChoppingCherry();
} else {
    ChoppingPineapple();
}
```

## 第 18 章：Switch

谁知道呢，也许有一天你将拥有自己的 Web 开发公司。就像任何其他大公司一样，它有自己的……自动售卖机！但我们不像其他大公司，对吧？我们的自动售卖机是特殊的！

所以我们将拥有……*鼓点* 自动等待机！我们的自动售卖机会让你等待。而且……就这样了。没有饮料之类的。只是……等一会儿，然后离开。

好了，首先，我们当然要构建自动售卖机标题。

```html
<h1>The Vending Machine</h1>
```

现在我们需要构建自动售卖机函数。

```javascript
function VendingMachine(pendingTime){
    switch(pendingTime){
        case 1:
            // 为 #1 代码……
            break;
        case 2:
            // 为 #2 代码……
            break;
        case 3:
            // 为 #3 代码……
            break;
        default:
            // 默认代码……
    }
}
```

让我们填充我们的分支 (case)

```javascript
function PendingMessage(time){
    alert(“The Vending Machine says you have to wait ”+ time + “ minutes”);
}
```

现在我们需要函数放入按钮中：

```html
<input type="button" onclick="VendingMachine(1)" value="1" />
<input type="button" onclick="VendingMachine(2)" value="2" />
<input type="button" onclick="VendingMachine(3)" value="3" />
<input type="button" onclick="VendingMachine(7)" value="4" />
```

好了！让我们第一次尝试我们的等待售卖机！点击 1 号按钮。我们需要等 1 分钟……（但我们不用等……因为……我不想等。）




让我们按下数字 4，我们应该进入默认分支……

我们得等 7 分钟……哦不……

好吧……你去听下一节课吧，我在这里等。

大概要等……7 分钟吧。

## 第 19 章
## for 循环

在过去，以及现在《辛普森一家》的剧集里，对调皮的学生有一种普遍的惩罚。写成千万遍他们所犯的错误……例如……“我不应该在课堂上说话”或“我再也不会忘记做作业了”……诸此类。

所以今天我们将用我们闪亮的崭新的机器，让所有调皮的学生获得自由，这台机器可以为你写行！

首先，让我们让我们的文档看起来像黑板一样……

```html
<style>
body{background-color: #333333; color: #f0f0f0;}
</style>
```

好了，先说第一，让我们看看如何一遍又一遍地重复同样的事情……

为了实现这一点，我们将使用我们的异父异母的兄弟——`for loop`。

`for loop` 是一种技术，允许你循环遍历任何代码，直到你遇到某种计数器……让我们把它写下来，我再进一步解释：

```javascript
for(i=0; i < 10 ; i++){

##… 代码… ##

}
```

好了，要创建一个 `for loop`，你必须写 `for` 单词并打开括号……在括号内部有三个由分号隔开的部分，第一部分是你应该重置计数器。因为 `for loop` 会一直运行直到你遇到那个计数器。所以第一部分是重置计数器，你可以给计数器起任何喜欢的名字，我命名为 `iti`，足够短了，并将其重置为零。

紧接着是第二部分。它是关于告诉 `for loop`：“如果那个条件为真……好吧……就继续循环好吗？！”所以我写了 `i < 10`，用英语表达的意思是：“只要我们的计数器‘i’ 小于 10，就别提它，继续循环……”

在最后一部分，是计数器的增加。在每次循环之后，执行加加操作，如果你记得的话，它的意思是“自己加 1!”，所以如果我们的计数器 `i` 是 0，在一次循环后它将变成 1，然后是 2，然后是 3，以此此类推……

每当我们的中间部分满足时，我们这里的代码就会继续运行。

好了，让我们结合一下 for 循环和函数，为自己创建一个“写行机器”！

�� ♫……写行机啊……耶耶……ea…ea…a……♫ ��

是的，首先，我们将写一个名为 `WriteLineMachine` 的函数，并在里面包含一个 `for loop`，该函数将接受一个名为 `lineText` 的参数。

我们现在让 `for loop` 运行 10 次……

```javascript
function WriteLineMachine(lineText){

for(i=0 ; i < 10 ; i++){

//… 某些写入函数…

}

}
```

我会在 `for loop` 内部留一个注释，现在我们将写一个写入我们文本的函数，然后将其插入到 `for loop` 中，好吗？

让我们写下来吧！

我将创建另一个名为 `Write` 的函数，这个函数将要求一个名为 `lineText` 的参数，它将简单地在我们的文档上写入参数所拥有的相同值。

```javascript
function Write(lineText){

document.write(lineText);

}
```

我们将新函数插入到 `WriteLineMachine` 内部……并关联 `WriteLineMachine` 的参数

```javascript
function WriteLineMachine(lineText){

for(i=0 ; i < 10 ; i++){

Write(lineText);

}

}
```

好了，现在我们会有另一个启动我们机器的函数，名为 `StartMachine`，我们将 `WriteLineMachine` 插入到其中。并带有一个 `lineText` 参数。

```javascript
function StartMachine(lineText){

WriteLineMachine(lineText);

}
```

现在，我们将有一个新变量，它存储一段文本。假设我们想要重复……这段文本：“我再也不会骑着我的仓鼠移动车上学了。”（我保证！！！）

`var text = “I will never ride my hamster-mobile to school ever again.”;`

最后，我们用 `StartMachine` 将这一切连接起来，让它使用我们的文本变量……

`StartMachine(text);`

所以我们的代码进入 `StartMachine` 函数，带着我们的文本，旅行到 `WriteLineMachine` 函数带着我们的文本，循环 10 次，每一次循环中它都会访问我们的 `Write` 函数，该函数只是在我们的文档中打印我们的文本，也就是……好吧……我骑仓鼠移动车的禁忌之旅……

顺便说一下，我们可以很容易地改进我们的机器，给它一个循环次数的动态变量……像这样：

```javascript
var loopNum = 50;

for(i=0 ; i < loopNum ; i++){

Write(lineText);

}
```

就是这样。

现在我们可以欺骗我们的老师，让我们的机器为我们写行了！

## 第 20 章
## Array

现在我们将学习什么是 Array（数组）。

有时你想列出一些东西。

你可能想在屏幕上列出一些列表，比如名字、日期或者任何其他。为了这个任务，你可能声明一个变量，比如 `var user1`、`var user2`、`var user3` 等。

但现在我们可以使用数组。数组可以存储一个列表。

现在，让我们看看数组如何定义。

你定义一个数组，打开括号，在那些括号里你写下名字。

`var names = new Array(“Big Tony”, “Amazing Bob”, “Cool Jeff”, “Awesome Jane”);`

现在假设我想在屏幕上打印 Amazing Bob，我该怎么办？

我会写 `document.write`，然后在我们的括号里写下名字。

我们不知道的是，数组的每一个项都有一个秘密索引，而且不是从一而是从零开始。所以 Big Tony 是索引 0，Amazing Bob 是索引 1，Cool Jeff 是索引 2，Awesome Jane 是索引 3。

`document.write(names[0]);`
`document.write(names[1]);`
`document.write(names[2]);`
`document.write(names[3]);`

现在让我们做点什么！假设我们的 Awesome Jane 决定改名为 Tammy。

`names[3] = “Tammy”;`
`document.write(names[3] + “br/>”`

## 第 21 章
## Array 技巧

好了！我们对数组还有有更多技巧！

我们可以使用 `push` 方法添加新项

所以假设我们想添加两个名字，例如……Martha 和 George。

```javascript
names.push(“Martha”, “George”);
document.write(names + “br/>”);
```

让我们看看是否搞定了……是的！

我们还可以按字母顺序进行排序……使用 `sort` 方法……

```javascript
names.sort();
document.write(names + “br/>”);
```

看看……是的！排序好了！！！

我们还可以……反转一切！

```javascript
names.reverse();
document.write(names + “br/>”);
```

## 第 22 章
## 强化版 Javascript

好了，到为止我们学了很多很酷的东西，但现在，是时候提升一下了。

我会写一些高级的内容，所以请耐心一点，好吗？

好了……

你们知道所有那些电影吗，反派抓了由汤姆·克鲁斯主演的英雄，他有一个……一个炸弹……如果他不放置正确的密码组合，所有人都会死……？

那么，今天我们将成为那个反派，去构建这个提示密码的机器，我们就能知道密码是否有效！

所以让我们在 HTML 中构建一些东西……

```html
<div id=”sendItem”>
```




<form>
密码: <br/>
<br/>
<input type="password" id="password" placeholder="password" />
<br/>
<input type="button" id="submit" value="send!" />
</form>
</div>

让我们给它修饰一下吧，毕竟这可是特殊的场合！

<style>
#sendItem{
background-color: red;
width: 200px;
margin: 30px;
padding: 30px;
}
</style>

现在我们将有一个函数，并将其命名为 `CheckValidation()`，它将…… 检查密码组合的验证……当然了……

在我们的函数内部，我们将有一个名为 `password` 的变量，它最终将获取 id 为 `password` 的输入类型元素的值。让我们输入 `document`、`getElementById`、`value`。所以我们在 `password` 中存储了输入标签的值。

然后，我们将有一个 `if` 语句，用来检查我们的组合是否正确，所以我们会写 `password` 不等于……让我们看看……什么样的组合是连五角大楼都无法破解的？？……哦！1234。这个就行了。

并且我们有一个 `alert` 提示，显示“警告！密码错误！”

```javascript
var password = document.getElementById(“password”).value;
if(password != “1234”){
alert(“Caution! Password is Incorrect!”);
}else{
// success!
}
```

好了，让我们把函数绑定到按钮上，使用 `onclick`……

```html
<input type="button" id="submit" value="send!" onclick="CheckValidation()" />
```

让我们检查一下如果我们输入某些内容，它是否会显示错误……是的！！！确实会！太酷了！

现在……注意，我们有一个“发送”按钮……所以……我们必须把表单发送到某个地方，对吧？让我给我们的样式标签里添加一些小花样……

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

我添加了另一个名为 `leftTrans` 的类，并对我们的 `sendItem` id 添加了更多修改……

现在，在我们成功输入密码组合后，表单将被发送给我们——这些反派！让我们在 `else` 语句中添加 `var y`，它将获取 `sendItem` 的 id，这样我们访问 `sendItem` 元素……现在，我们将获取变量 `y` 并添加一个名为 `leftTrans` 的类。

```javascript
else{
var y = document.getElementById(“sendItem”);
y.className += “leftTrans”;
}
```

让我们尝试失败一次……我们收到了消息……让我们用我们的强密码 1234 再试一次……哦！我们发送了表单！谁知道发送到哪里了？！也许是到火星。

## 第 23 章

## 现在怎么办？

恭喜你！你完成了这门课程，你在书里听了很多非常冷笑话，我为你感到非常自豪！

你可能会问自己：现在我已经完成了第一门 JavaScript 课程，我该做什么呢？我该如何提高我的 Web 开发技能？

嗯，年轻的学徒（padawan），现在是时候将你的 JavaScript 技能与服务器端结合起来了。我有一门专门为你准备的 C# 课程，因为你购买了这本书（或者为了补偿我那些冷笑话），我将为你提供 Udemy 上所有课程的 5 折扣优惠。

你可以在这里领取优惠券：`http://basicjavascript.gilad.me/discount50/`


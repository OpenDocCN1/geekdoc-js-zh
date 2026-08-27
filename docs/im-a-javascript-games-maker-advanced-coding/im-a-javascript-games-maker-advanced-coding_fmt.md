
# JavaScript 游戏制作进阶指南

## 简介

本书将向你展示如何使用JavaScript编写激动人心的新游戏。JavaScript用于使网页更具交互性。它也可以用来创建在线游戏，这些游戏可以在桌面和移动设备上运行。在本书结束时，你将学到很多很棒的技巧，使你成为终极JavaScript专家。

你可以使用普通的文本编辑器来创建你的代码。

```
mygame.html
<script>
alert('Press any key to start')
</script>
```

这可以正常工作，但可能相当繁琐，因为软件不会给你任何帮助。

本书活动中最适合使用的是离线HTML文本编辑器。它将在你输入代码时提供支持，同时也让你有机会学习真正的JavaScript代码。

你将使用两个独立的窗口。安排它们，以便你可以同时看到它们。

有许多不同的网络浏览器可供使用。我们建议在本书活动中使用Google Chrome。在开始之前，请确保你的计算机上安装了最新版本。

在本书中，你将学习一些HTML以及JavaScript。HTML是用于构建网页的语言。JavaScript是让这些页面栩栩如生的语言！

如果你想了解更多关于HTML工作原理的知识，或者你需要JavaScript的入门指南，那么请尝试阅读*Generation Code*系列中的其他一些书籍。但是，如果你以前从未使用过HTML或JavaScript，你仍然可以创建本书中的所有游戏。

那么你还等什么？开始编程吧！

## 入门准备

你需要一个文本编辑器来开始JavaScript编程。你的计算机上可能已经有一个简单的文本编辑器，名为记事本（如果你使用Windows），或TextEdit（在Mac上）。这足以让你入门，但如果你下载一个更强大的文本编辑器，创建JavaScript会容易得多。在本书中，我们将使用一个名为Sublime Text的文本编辑器。你可以下载许多其他编辑器，例如Brackets或Notepad++——所有这些都可以免费试用。

### 第1步 – 查找Sublime Text网站

- 打开你的网络浏览器并访问`www.sublimetext.com`

### 第2步 – 开始下载

- 点击网页顶部的下载按钮。
- 选择你需要的Sublime Text版本。如果不确定，请让成年人帮助你找到正确的版本：如果你使用Mac，请点击苹果菜单，然后点击关于。在PC上，单击开始菜单，选择系统，然后单击关于。
- 等待下载完成。

### 第3步 – 安装软件

- 一些网络浏览器随后会要求你运行安装程序。选择运行。
- 如果这没有发生，不要惊慌。安装程序文件应该已经下载到你的计算机上。在你的下载文件夹中查找它。双击它开始安装你的新文本编辑器。你应该会得到一个大的白色或灰色框，告诉你下一步该怎么做。按照这些说明完成安装。

### 第4步 – 运行Sublime Text

- 在PC上：
  - 点击 **开始** > **程序** > **Sublime Text**。或者，如果它出现在 **最近添加** 部分，直接点击 **Sublime Text**。
- 在Mac上：
  - 点击 **Finder**。
  - 点击 **应用程序**。
  - 通过将 **Sublime Text** 从 **Finder** 拖到桌面底部的程序坞来创建一个快捷方式。
  - 点击 **Sublime Text** 图标。

### 第5步 – 开始编程！

在文本编辑器的第1、2、3行仔细输入此代码。

```
1 <script>
2     alert("Start Coding!")
3 </script>
```

- 标记JavaScript部分的开始。
- 显示一个消息框，内容为“开始编程！”。
- 标记JavaScript部分的结束。

### 第6步 – 保存你的代码

- 点击 **文件** > **保存**。
- 保存到你的 **文档** 文件夹。
- 输入 **start.html** 作为文件名。

### JavaScript需要HTML

虽然我们使用JavaScript编程，但我们需要将文件放在一些HTML代码中才能使其工作。HTML代表超文本标记语言，是用于构建网页的语言。

HTML用于描述网页上显示的对象或元素。如果你正在创建一个简单的游戏，你需要使用HTML来添加图像和一些文本以显示分数。JavaScript被添加来告诉图像在按下不同键或单击鼠标时移动。它也可以用来显示分数并使其变化。

我们需要同时使用HTML和JavaScript来制作更有趣的游戏。JavaScript旨在添加到HTML页面中，使其更具交互性。

你将在本书中使用一系列HTML元素。每个元素使用标签来显示其元素类型（见第31页）。标签用`< >`尖括号括起来。

### 第7步 – 查看你的页面

- 打开你的 **文档** 文件夹。
- 找到 **start.html** 文件并双击它。
- 你的网页现在应该在正常的网络浏览器中加载。
- 你应该会看到一条消息 **开始编程！**

## UFO能量补充

在这个游戏中，玩家必须尽快移动一个外星飞船（UFO）以获取更多能量。玩家通过按键盘上的方向键来移动UFO。原子符号（下面绿色的）用于代表能量源。玩家完成任务五次后，游戏停止并显示所用时间。你可以和朋友比赛，看谁能用最短的时间完成它！游戏的完整代码列在第11页。

### 第1步 – 规划

分数显示在HTML段落元素中。

计时器将计算收集五个原子所需的时间。

每次UFO移动时，我们需要检查它是否已经到达原子位置。这是通过比较它们的坐标来完成的。

变量用于计数分数、游戏运行时间以及原子和UFO的坐标。

当收集到五个原子时，游戏结束并显示所用时间。

我们只需要一张原子图像。每次UFO收集到它，我们都会将其移动到一个新的随机位置，并将分数增加1。

按方向键会改变`ufoX`和`ufoY`坐标，使UFO在屏幕上移动。

点击 **确定** 再玩一次。

### 第2步 – 寻找一些图片

- 找一张原子图片使用，或者找另一个符号来代表游戏中的能量。它需要保存到与HTML文件相同的文件夹中。
- 搜索原子剪贴画使用。
- 右键单击一张图片。
- 点击图片另存为...
- 导航到你的文档文件夹，然后点击保存。
- 现在重复此步骤，但搜索UFO剪贴画使用。

### 流畅动画

我们将为图像添加一个过渡属性，使其平滑移动。这意味着图像的样式属性（即其与屏幕左侧或顶部的距离）将在特定时间内逐渐改变。

所有样式属性都将受到影响。

```
-webkit-transition: all 0.5s;
```

这些改变将在0.5秒（半秒）内逐步完成。

### 第三步 – 开始新文件

首先输入游戏的HTML代码，设置好主体、图像和显示得分的段落。

Sublime Text

```html
1 <html>
2 <body style="background-color:black">
3   <img id="atom" style="width: 50px; position:absolute" src="atom.png">
4   <img id="ufo" style="width: 50px; position:absolute; top:0; left:0; -webkit-transition: all 0.2s;" src="ufo.png">
5   <p id="scoreTB" style="position:absolute; color:white;">Score: 0</p>
6   <p id="timeTB" style="position:absolute; right:50px; color:white;">Time: 0</p>
7 </body>
```

设置背景颜色。

添加原子图像。确保`src`属性与下载文件的名称匹配。

添加UFO图像。

添加得分段落。

添加时间段落。

点击 **文件 > 另存为**，并输入文件名为`ufo.html`。

确保将其保存在您的 **文档** 文件夹中。每隔几分钟记得保存一次。

### 第四步 – 开始编写脚本

既然我们已经定义了页面上的元素，现在需要开始编写JavaScript。

在游戏开始时，我们需要：

- 创建变量
- 定义一个生成随机数的函数
- 告诉程序页面加载并准备就绪时运行哪个函数。
- 告诉程序当按键被按下时运行哪个函数
- 定义一些设置坐标的函数

```javascript
8  <script>
9  var score=0, gameTime=0, gameTimer, ufoX=0, ufoY=0, atomX=0, atomY=0;
10 onkeydown=handleKeys;
11 onready=startUp();
12 function setLeft(id,x){document.getElementById(id).style.left=x+"px";}
13 function setTop(id,y){document.getElementById(id).style.top=y+"px";}
14 function randomNumber(low,high){return(Math.floor(low+Math.random()*(1+high-low)));}
```

开始脚本部分。

创建变量以存储分数、游戏时间和坐标。

告诉程序按键被按下时运行哪个函数。

告诉程序页面准备就绪时运行哪个函数。

定义设置任何元素坐标的函数。

定义一个返回两个数值之间随机数的函数。

### 第五步 - 开始运行

页面在浏览器中加载后，`startUp`函数将被调用。（“调用”一个函数意味着运行它并执行其内部的所有代码。）`startUp`函数将运行代码将原子图标移动到随机位置，并启动游戏计时器。

```javascript
15 function startUp(){
16     moveAtom();
17     gameTimer=window.setInterval(displayTime, 1000);
18 }
```

定义函数。

调用`moveAtom`函数。

启动`gameTimer`。这个计时器将每1000毫秒（每秒）调用一次名为`displayTime`的函数。

结束函数。

### 第六步 - 运行多久？

添加`displayTime`变量。这将存储游戏运行了多少秒。

```javascript
19 function displayTime(){
20     gameTime++;
21     document.getElementById("timeTB").innerText="Time:"+gameTime;
22 }
```

定义函数。

将`gameTime`变量中存储的值加1。

在名为`timeTB`的段落中显示剩余时间。

结束函数。

### 元素定位

计算机图像由像素（图片元素）组成。在JavaScript和HTML中，像素可以用作坐标的单位。

可以通过设置坐标将元素定位在特定位置。这是通过设置它们的`left`和`top`样式属性来实现的。在值的末尾加上`px`表示以像素为单位。

(0,0)始终是浏览器左上角的坐标。`left`和`top`的最大值将取决于浏览器窗口的大小。此屏幕上红点的坐标是(100,50)。

### 第七步 – 移动原子

我们需要定义一个函数，将原子移动到屏幕上的随机位置。

```javascript
23 function moveAtom(){
24 atomX=randomNumber(2,16);
25 atomY=randomNumber(2,16);
26 setLeft("atom",50*atomX);
27 setTop("atom",50*atomY);
28 }
```

定义函数。

将`atomX`设置为2到16之间的随机数。

将`atomY`设置为2到16之间的随机数。

通过将`atomX`乘以50，`atomY`乘以50（`*`表示乘法，在JavaScript中用来替代数学符号×）来设置原子符号的新位置。

### 第八步 – 移动UFO

当按下方向键时，我们需要将UFO向上、下、左或右移动——方向取决于按下了哪个键。我们需要在函数中添加一种特殊类型的变量，称为参数，它将存储有关所按键的信息。在函数名后输入`(e)`来添加参数。

键盘上的每个键都有一个特定的代码与之关联。左箭头键的代码是37，右箭头键的代码是39，上箭头键是38，下箭头键是40。按下的键的代码将存储在`e.keyCode`中。输入以下函数以触发按键被按下时发生的情况：

```javascript
29 function handleKeys(e){
30 if(e.keyCode==37){ufoX--;}
31 if(e.keyCode==39){ufoX++;}
32 if(e.keyCode==38){ufoY--;}
33 if(e.keyCode==40){ufoY++;}
34 setLeft("ufo",50*ufoX);
35 setTop("ufo",50*ufoY);
36 checkIfHitAtom();
37 }
```

定义一个名为`handleKeys`的函数。有关按下了哪个键的信息将被放入名为`e`的变量中。

如果发送了左箭头键的代码，使`ufoX`减少1。（`ufoX--`表示从`ufoX`的值中减去1。）

如果发送了右箭头键的代码，使`ufoX`增加1。（`ufoX++`表示在`ufoX`上加1。）

如果按下了上箭头键，从`ufoY`中减去1。

如果按下了下箭头键，在`ufoY`上加1。

通过将`ufoX`乘以50，`ufoY`乘以50来设置UFO的新位置。

UFO移动后，我们需要运行`checkIfHitAtom()`函数来检查它是否击中了原子符号。

> 请记住，事件是特殊的代码片段，它们“监听”鼠标或键盘，并在运行其他代码之前等待某些事情发生。

### 第九步 – 命中还是未中？

每次UFO移动时，它都会调用下面的函数。此函数将检查UFO是否击中了原子符号。我们通过比较原子和UFO的x坐标（距离左侧的距离）和y坐标（距离顶部的距离）来编写此代码。如果它们相等，那么它们一定在同一个位置。因此，UFO击中了原子符号并补充了它的能量水平！

```javascript
38 function checkIfHitAtom(){
39   if((ufoX===atomX) && (ufoY===atomY)){
40     score++;
41     document.getElementById("scoreTB").innerText="Score: "+score;
42     moveAtom();
43     if(score===5){gameOver();}
44   }
45 }
```

如果坐标匹配，运行下面的代码（`&&`表示与）。将分数加1。在名为`scoreTB`的段落中显示分数。将原子符号移动到新的随机位置。如果分数达到5，那么玩家获胜，因此调用`gameOver`函数。

### 第十步 – 游戏结束

当玩家收集了五个原子图标后，游戏结束，并运行以下代码：

```javascript
46 function gameOver(){
47   clearInterval(gameTimer);
48   alert("Well done! Your time was: "+ gameTime);
49   location.reload();
50 }
```

定义函数。停止计时器运行，这样时间就不会继续增加。显示一条消息，说明玩家完成游戏所花的时间。此命令将重新加载页面并使游戏重新开始。（如果不想这样，省略这一行即可。）

### 第十一步 – 最后几行

最后，添加这两行以显示脚本部分和HTML的结束。

```html
51 </script>
52 </html>
```

保存您的文件，重新加载浏览器，然后开始玩吧！

### 自定义

- 修改游戏，使玩家必须收集10个原子图标。
- 使用不同的图像设计您自己的收集游戏。

### 完整代码

```
<html>
<body style="background-color:black">
  <img id="atom" style="width: 50px; position:absolute" src="atom.png">
  <img id="ufo" style="width: 50px; position:absolute; top:0; left:0; -webkit-transition: all 0.2s;" src="ufo.png">
  <p id="scoreTB" style="position:absolute; color:white;">Score: 0</p>
  <p id="timeTB" style="position:absolute; right:50px; color:white;">Time: 0</p>
</body>
<script>
  var score=0, gameTime=0, gameTimer, ufoX=0, ufoY=0, atomX=0, atomY=0;
 onkeydown=handleKeys;
 onready=startUp();
 function setLeft(id,x){document.getElementById(id).style.left=x+"px";}
 function setTop(id,y){document.getElementById(id).style.top=y+"px";}
 function randomNumber(low,hi){return (Math.floor(low+Math.random()*(1+hi-low)));}
 function startUp(){
     moveAtom();
     gameTimer=window.setInterval(displayTime, 1000);
 }
 function displayTime(){
     gameTime++;
     document.getElementById("timeTB").innerText="Time: "+gameTime;
 }
 function moveAtom(){
     atomX=randomNumber(2,16);
     atomY=randomNumber(2,16);
     setLeft("atom",50*atomX);
     setTop("atom",50*atomY);
 }
 function handleKeys(e){
     if(e.keyCode==37){ufoX--;}
     if(e.keyCode==39){ufoX++;}
     if(e.keyCode==38){ufoY--;}
     if(e.keyCode==40){ufoY++;}
     setLeft("ufo",50*ufoX);
     setTop("ufo",50*ufoY);
     checkIfHitAtom();
 }
 function checkIfHitAtom(){
     if((ufoX==atomX) && (ufoY==atomY)){
         score++;
         document.getElementById("scoreTB").innerText="Score:"+score;
         moveAtom();
         if(score==5){gameOver();}
     }
 }
 function gameOver(){
     clearInterval(gameTimer);
     alert("Well done! Your time was:"+gameTime);
     location.reload();
 }
</script>
</html>
```

## 幽灵迷宫

在这个项目中，你将制作一个简单的迷宫游戏。当按下方向键时，玩家会四处移动。为了防止玩家穿过墙壁，我们将使用一种特殊的数据结构来存储迷宫形状。这被称为二维数组，它是一个列表的列表，用于存储迷宫中哪些方格是墙壁，哪些方格不是。最后，我们将检查玩家的位置，并在玩家到达迷宫出口时显示一条消息。游戏的完整代码列在第17页。

### 第1步 – 规划

游戏开始时使用一个数据网格来绘制迷宫。墙壁将用黄色绘制，路径用蓝色绘制。

在玩家被允许移动之前，我们需要检查它是否会撞到墙壁。这是通过检查`mazeData`来完成的。

按下方向键将改变玩家图标的坐标，使其在屏幕上移动。

迷宫信息以1和0存储。1代表墙壁，0代表路径。

变量存储玩家的坐标。

每次玩家移动时，我们需要检查它是否到达了出口。这是通过检查坐标来完成的。

### 第2步 – 找一张图片

- 首先，你需要找一张要使用的图片。它需要放在与HTML文件相同的文件夹中。
- 上网搜索一些可用的剪贴画。
- 右键单击一张图片。
- 点击 **将图像另存为...**
- 导航到你的 **文档** 文件夹，然后点击 **保存**。

### 第3步 – 开始一个新文件

首先输入游戏的HTML代码。添加用于主体、迷宫容器和玩家（幽灵，玩游戏时会四处移动）的代码。迷宫稍后构建，但我们需要准备一个特殊的容器来容纳方块——`mazeHolder`。我们还将添加一个特殊的样式部分，其中包含每个迷宫方块的尺寸和颜色。

```
<html>
<body style="background-color:black">
    <div id="mazeHolder" style="position:absolute; top:0; left:0;"></div>
    <img id="player" style="position:absolute; width:50px; top:50px; left:0; -webkit-transition: all 0.2s;" src="ghost.png" >
    <style>
        div{position:absolute; background-color:yellow; width:50px; height:50px;}
    </style>
</body>
```

1. 设置背景颜色。
2. 创建一个方框来容纳迷宫的所有方块。
3. 将`src`属性与下载文件的名称匹配。
4. 开始样式部分。
5. 这部分样式用于构成迷宫方块的`div`元素。
6. 结束样式部分。

### 第4步 – 保存你的代码

- 点击 文件 > 另存为，并将文件名输入为`maze.html`。
- 确保将其保存在你的 **文档** 文件夹中。每隔几分钟就保存一次。

### 迷宫数据

当开发者设计带有迷宫、墙壁或平台的游戏时，他们需要找到一种方法来确保游戏中的物体在碰到坚硬物体时停止。有很多方法可以做到这一点，但都涉及某种数据结构来存储坚硬物体的位置信息。在这个游戏中，我们将创建一个名为二维数组的特殊数据网格，它使用1和0来表示墙壁和路径。

```
var mazeData=[
    [1,1,1,1,1,1,1,1],
    [0,0,1,1,0,0,0,1],
    [1,0,0,0,0,1,1,1],
    [1,0,1,1,0,1,0,1],
    [1,0,1,1,0,0,0,1],
    [1,0,0,0,0,1,0,0],
    [1,1,1,1,1,1,1,1]
];
```

- 我们需要将1变成黄色的墙壁。在网页上查看时，它们可能看起来有点橙色。
- 所有的0都需要变成蓝色的路径。

我们选择绘制迷宫的颜色并不重要。重要的是所有的1和0。我们将用它们来阻止玩家穿过墙壁。

### 第5步 – 输入迷宫数据

开始脚本部分并输入迷宫数据。

创建一个名为`mazeData`的数组，将其作为二维数组存储在其中。

```
<script>
var mazeData=[
 [1,1,1,1,1,1,1,1],
 [0,0,1,1,0,0,0,1],
 [1,0,0,0,0,1,1,1],
 [1,0,1,1,0,1,0,1],
 [1,0,1,1,0,0,0,1],
 [1,0,0,0,0,1,0,0],
 [1,1,1,1,1,1,1,1]
];
```

开始脚本部分。

创建`mazeData`数组。

非常小心地输入数据。迷宫的每一行都成为数组中的一个列表。迷宫中的每个方格是0或1，用逗号分隔。每个列表必须以方括号`[ ]`开始和结束。一旦代码运行起来，你可以尝试更改此数据以改变迷宫的布局。

结束`mazeData`数组。

### 第6步 – 变量和简单函数

输入代码，告诉程序在按下按键和程序启动时该做什么。

创建所需的变量并定义设置坐标的函数。

```
onkeydown=handleKeys;
onready=drawMaze();
var px=0, py=1;
function setLeft(id,x){document.getElementById(id).style.left=x+"px";}
function setTop(id,y){document.getElementById(id).style.top=y+"px";}
```

当按下任何键时，调用名为`handleKeys`的函数。

当页面加载完毕后，调用名为`drawMaze`的函数。

创建坐标变量。

定义设置任何元素坐标的函数。

### 第7步 – 绘制迷宫

需要使用`mazeData`数组中的信息在页面上绘制迷宫。下面的函数将遍历数组，并为迷宫中的每个方格创建一个`div`元素。然后它将查看迷宫数据中的相关项是0还是1。如果是1，它将保留`div`为黄色；如果是0，则将其着色为蓝色。

```
function drawMaze(){
    for(var y=0; y<7; y++){
        for(var x=0; x<8; x++){
            var newOb=document.createElement('div');
            document.getElementById("mazeHolder").appendChild(newOb);
            var divId=Math.random();
            newOb.setAttribute('id',divId);
            setLeft(divId,50*x);
            setTop(divId,50*y);
            if(mazeData[y][x]==0){
                document.getElementById(divId).style.backgroundColor="blue";
            }
        }
    }
}
```

- 循环遍历迷宫的每一行。
- 循环遍历迷宫的每一列。
- 创建一个名为`newOb`的新`div`。
- 将其添加到`mazeHolder`中。
- `div`需要一个名称。编一个随机名称！
- 将新名称赋予该`div`。
- 根据其坐标将其定位在`mazeHolder`中的正确位置。x和y值乘以(*)50，因为每个方块是50 x 50像素。
- 如果`mazeData`中的相关项是0，那么：
  - 将`div`着色为蓝色，使其成为一条路径。
  - 结束IF命令块。
- 结束x循环。
- 结束y循环。
- 结束函数。

### 第8步 – 移动玩家

当按下方向键时，我们需要将玩家向上、向下、向左或向右移动。然而，我们还需要检查移动玩家是否会使其撞到墙壁。为此，我们需要查看玩家要移动进入的`mazeData`项的值。如果是0，则允许玩家移动。如果是1，则玩家会撞墙，因此玩家无法移动。

```
function handleKeys(e){
    if((e.keyCode==37)&&mazeData[py][px-1]==0){px--;}
    if((e.keyCode==39)&&mazeData[py][px+1]==0){px++;}
    if((e.keyCode==38)&&mazeData[py-1][px]==0){py--;}
    if((e.keyCode==40)&&mazeData[py+1][px]==0){py++;}
    setLeft("player",px*50);
    setTop("player",py*50);
    if(px==7 && py==5){alert("Well done!");}
}
```

- 定义一个名为`handleKeys`的函数。
- 如果按下左箭头键且玩家左侧没有墙壁，则从`px`中减去1。
- 如果按下右箭头键且玩家右侧没有墙壁，则在`px`上加1。
- 如果按下上或下箭头键，并且如果玩家移动不会撞墙，则以同样的方式更改`py`。
- 通过将`px`乘以50和`py`乘以50来设置玩家的新位置。
- 如果`px`和`py`与出口的坐标匹配，则显示消息“干得好！”。

### 第9步 – 完成游戏

最后，添加以下两行来结束脚本部分和HTML。

```html
</script>
</html>
```

> 保存文件，重新加载浏览器，然后测试你的迷宫！

### 核心概念

#### 以数据存储的图形

游戏世界的信息不是使用背景图片，而是存储在一个二维数组中——一个列表的列表。

#### 动态元素

到目前为止，我们通过输入HTML来向页面添加元素，但有时元素太多无法用这种方式添加。我们可能想设置细节，例如元素的颜色或何时运行程序。JavaScript运行时创建的元素称为动态元素。

### 自定义

- 通过更改`mazeData`中的一些1和0来尝试不同的迷宫布局。
- 制作一个更大的迷宫并尝试使用不同的颜色。

1. 首先在方格纸上规划你的迷宫。确保它是可以解决的！
2. 将你的迷宫转换成1和0。当你想要墙壁时使用1。用你的新数据替换原始代码的第10到18行。

```javascript
var mazeData=[
  [1,1,1,1,1,1,1,1,1,1,1,1],
  [0,0,0,1,0,0,0,0,0,0,0,1],
  [1,0,1,1,1,1,0,1,1,1,0,1],
  [1,0,0,0,1,0,0,0,0,1,0,1],
  [1,1,1,0,0,0,1,1,0,0,0,1],
  [1,0,1,1,0,1,1,1,1,1,1,1],
  [1,0,0,0,0,1,0,0,0,0,0,1],
  [1,0,1,1,0,1,0,1,1,0,1,0],
  [1,0,1,0,0,1,0,0,1,0,1,1],
  [1,0,1,0,1,1,1,0,1,0,0,1],
  [1,0,1,0,0,0,1,0,1,0,0,0],
  [1,1,1,1,1,1,1,1,1,1,1,1]
];
```

3. 在`drawMaze`函数中，你需要更改循环运行的次数。在示例中，两者都需要更改为12，因为迷宫有12列宽和12行深（坐标从0开始）。

```javascript
// 将7改为新迷宫的行数。
for(var y=0; y<7; y++) {
  // 将8改为新迷宫的列数。
  for(var x=0; x<8; x++){
```

4. 为新出口位置设置坐标。（在示例中，这将是`px==11`和`py==10`）。

```javascript
if(px==7 && py==5){alert("Well done!");}
```

### 完整代码

```html
<html>
<body style="background-color:black">
    <div id="mazeHolder" style="position:absolute; top:0; left:0;"></div>
    <img id="player" style="position:absolute; width:50px; top:50px; left:0; -webkit-transition:all 0.2s;" src="ghost.png" >
    <style>
        div{position:absolute; background-color:yellow; width:50px; height:50px;}
    </style>
</body>
<script>
   var mazeData=[
       [1,1,1,1,1,1,1,1],
       [0,0,1,1,0,0,0,1],
       [1,0,0,0,0,1,1,1],
       [1,0,1,1,0,1,0,1],
       [1,0,1,1,0,0,0,1],
       [1,0,0,0,0,1,0,0],
       [1,1,1,1,1,1,1,1]
   ];
   onkeydown=handleKeys;
   onready=drawMaze();
   var px=0, py=1;
   function setLeft(id,x){document.getElementById(id).style.left=x+"px";}
   function setTop(id,y){document.getElementById(id).style.top=y+"px";}
   function drawMaze(){
       for(var y=0; y<7; y++){
           for(var x=0; x<8; x++){
               var newOb=document.createElement('div');
               document.getElementById("mazeHolder").appendChild(newOb);
               var divId=Math.random();
               newOb.setAttribute('id',divId);
               setLeft(divId,50*x);
               setTop(divId,50*y);
               if(mazeData[y][x]==0){
                   document.getElementById(divId).style.backgroundColor="blue";
               }
           }
       }
   }
   function handleKeys(e){
       if((e.keyCode==37)&&mazeData[py][px-1]==0){px--;}
       if((e.keyCode==39)&&mazeData[py][px+1]==0){px++;}
       if((e.keyCode==38)&&mazeData[py-1][px]==0){py--;}
       if((e.keyCode==40)&&mazeData[py+1][px]==0){py++;}
       setLeft("player",px*50);
       setTop("player",py*50);
       if(px==7 && py==5){alert("Well done!");}
   }
</script>
</html>
```

## 岩石风暴

这个游戏是一个简单的横向卷轴游戏：岩石会从屏幕右侧移动，朝向由玩家控制的飞船。按下 **上** 和 **下** 箭头可以让飞船躲避岩石。每次岩石移动时，一个函数会检查它们是否撞到了飞船。分数将存储在一个变量中，并且每次飞船躲避岩石时都会增加。当你玩游戏时，最大化屏幕，这样游戏更大，更容易躲避岩石。游戏的完整代码列在第23页。

### 第1步 – 规划

分数显示在一个HTML段落元素`<p>`中。

按下 **上** 和 **下** 箭头键将使飞船在屏幕上上下移动。

一个计时器将每20毫秒移动一次岩石。

然后它通过测试它们是否重叠来检查任何岩石是否撞到了飞船。我们将创建一个特殊函数来处理这个测试。

点击 **确定** 重新玩或取消。

### 第2步 – 找到一些图片

1. 找一张飞船的图片来使用。它需要保存到与HTML文件相同的文件夹中。
2. 在互联网上搜索飞船剪贴画来使用。
3. 右键单击一张图片。
4. 点击 **将图像另存为...**。
5. 导航到你的 **文档** 文件夹，然后点击 **保存**。
6. 现在重复此步骤，但搜索 **太空岩石剪贴画** 来使用。

### 第3步 - 开始一个新文件

首先输入游戏的HTML。添加主体的代码、四张图片和一个用于显示分数的段落。

#### Sublime Text

```html
<html>
<body style="background-color:#8060AA">
  <img id="ship" style="position:absolute; width:100px; left:50px;" src="spcshp.png">
  <img id="rock1" style="position:absolute; width:100px; left:-200px;" src="rock.png">
  <img id="rock2" style="position:absolute; width:100px; left:-200px;" src="rock.png">
  <img id="rock3" style="position:absolute; width:100px; left:-200px;" src="rock.png">
  <p id="scoreTB" style="position:absolute; color:yellow; font-size:20px; font-family:Arial">Score: 0</p>
</body>
```

设置背景颜色。

确保`src`属性与下载的飞船文件名匹配。

为三块岩石添加代码。每块的代码非常相似，但每块的ID不同 - `rock1`、`rock2`和`rock3`。确保`src`属性正确。

添加分数段落。

### 第4步 - 保存你的代码

点击文件 > 另存为，并输入 **rocks.html** 作为文件名。

确保你将其保存在 **文档** 文件夹中。每次添加任何代码后都要保存它。

> 设置坐标意味着将元素移动到屏幕上的新位置。获取坐标意味着找出元素在哪里。

### 第5步 - 开始脚本

在脚本开始时，我们需要：

- 创建我们需要的变量
- 告诉程序按键时运行哪个函数
- 告诉程序页面加载并准备好时运行哪个函数
- 定义一个函数来生成随机数
- 定义一些函数来获取和设置坐标。

```javascript
<script>
  var score=0, yChange=3, speed=5, gameTimer;
  document.onkeydown=handleKeys;
  onready=startUp();
  function setLeft(id,x){document.getElementById(id).style.left=x+"px";}
  function setTop(id,y){document.getElementById(id).style.top=y+"px";}
  function getLeft(id){return document.getElementById(id).offsetLeft;}
  function getTop(id){return document.getElementById(id).offsetTop;}
  function randomNumber(low,high){return(Math.floor(low+Math.random()*(1+high-low)));}
```

开始脚本部分。

创建所需的变量。

按键时运行此函数。

页面准备好时运行此函数。

定义设置任何元素坐标的函数。

定义获取任何元素坐标的函数。

定义一个返回两个值之间随机数的函数。

### 碰撞还是重叠？

在前两个游戏中，我们每次移动对象50或100像素。通过测试x坐标（距左边的距离）和y坐标（距顶部的距离），可以很容易地判断对象是否发生了碰撞。在一个对象移动距离较小的游戏中，它们可能会发生碰撞，但坐标不会完全相同。为了检测这种情况，我们需要查看两个对象是否重叠。

这两个对象的宽度和高度都是100像素。

我们知道这两个对象是重叠的，因为它们的左边界坐标差值小于宽度：120-50=70

并且它们的顶部坐标差值小于高度：140-85=55

这意味着它们重叠并发生了碰撞。

### 第6步 – 重叠测试代码

我们需要一个函数来测试三个岩石中的任何一个是否与飞船重叠。我们不必为每个岩石编写单独的代码，而是编写一个可以测试任意两个对象是否重叠的函数。我们将这两个假想的对象称为`ob1`和`ob2`。调用函数时，我们会告诉它我们要用哪两个对象进行重叠测试。

```
function isOverlapping(ob1, ob2) {
  return ((getLeft(ob1) + 100 > getLeft(ob2)) && (getLeft(ob1) < getLeft(ob2) + 100) &&
    (getTop(ob1) + 100 > getTop(ob2)) && (getTop(ob1) < getTop(ob2) + 100));
}
```

添加代码，在测试两个对象的坐标后返回（送回）一个值。如果对象重叠，返回`true`；如果不重叠，返回`false`。该函数假设对象的高度和宽度都是100像素。

### 第7步 – 启动

页面在浏览器中加载完毕后，将调用`startUp`函数。`startUp`函数将设置一个定时器来移动岩石。

```
function startUp() {
  gameTimer = window.setInterval(moveThings, 20);
}
```

启动`gameTimer`。这个定时器将每20毫秒（每秒50次）调用一次名为`moveThings`的函数。

### 第8步 – 移动对象

当定时器调用`moveThings`函数时，所有三个岩石都需要移动。我们可以通过编写一段代码来移动`rock1`，另一段来移动`rock2`，最后一段来移动`rock3`来实现。但这需要大量代码，并且意味着如果我们想加快或减慢岩石的速度，就需要更改每个部分。相反，我们将使用一个循环来依次移动每个岩石并检查它是否撞到了飞船。我们的循环将从1数到3。第一次移动`rock1`，然后`rock2`，接着`rock3`。为此，我们需要编写一段通用代码来移动一个假想的岩石，称为`rock n`。我们可以给`n`赋一个1到3之间的值。这将写成`"rock"+n`。

最后，我们需要让飞船上下移动。为了增加游戏难度，飞船不会保持静止。

```
function moveThings() {
  for (var n = 1; n <= 3; n++) {
    var x = getLeft("rock" + n);
    if (x < -100) {
      x = window.innerWidth;
      y = randomNumber(0, window.innerHeight - 100);
      setTop("rock" + n, y);
      score = score + 10;
      document.getElementById("scoreTB").innerText = "Score: " + score;
    }
    setLeft("rock" + n, x - speed - n);
    if (isOverlapping("rock" + n, "ship")) {
      gameOver();
    }
  }
  var y = getTop("ship");
  if ((y <= 0) || (y > window.innerHeight - 100)) {
    yChange = -yChange;
  }
  setTop("ship", y + yChange);
}
```

### 第9步 – 改变方向

为了增加游戏难度，飞船会持续向上或向下移动。按下一个键将设定它的方向，但它是在`moveThings`函数中被移动的。输入此函数来决定按下按键时会发生什么。

```
function handleKeys(e) {
  if (e.keyCode == 38) {
    yChange = -3;
  }
  if (e.keyCode == 40) {
    yChange = 3;
  }
}
```

定义一个名为`handleKeys`的函数。关于按下了哪个键的信息将存储在变量`e`中。

如果传递给函数的是向上箭头键的代码，将`yChange`设置为-3。

如果发送的是向下箭头键的代码，将`yChange`设置为3。

结束函数。

### 第10步 – 碰撞

如果其中一个岩石撞到了飞船，那么将调用以下函数：

```
function gameOver() {
  clearInterval(gameTimer);
  if (confirm("Game Over – Click OK to play again.") == true) {
    location.reload();
  }
}
```

定义函数。

停止定时器运行，这样时间就不会继续增加。

显示一条消息，询问玩家是否想再玩一次。如果他们点击确定，则运行下一行。

重新加载页面，让游戏重新开始。

结束IF语句。

结束函数。

### 第11步 – 结束

最后，添加这两行以显示脚本部分和HTML的结束。

```
</script>
</html>
```

### 关键概念

**循环遍历元素**

使用循环来移动多个名称相似的对象，例如`rock1`、`rock2`和`rock3`。

**碰撞检测**

使用一个函数来检查任意两个特定对象是否重叠，从而检测碰撞。

保存你的文件，重新加载 **浏览器**，然后开始玩吧！

### 完整代码

```
<html>
<body style="background-color:#8060AA">
  <img id="ship" style="position:absolute; width:100px; left:50px;" src="spcshp.png">
  <img id="rock1" style="position:absolute; width:100px; left:-200px;" src="rock.png">
  <img id="rock2" style="position:absolute; width:100px; left:-200px;" src="rock.png">
  <img id="rock3" style="position:absolute; width:100px; left:-200px;" src="rock.png">
  <p id="scoreTB" style="position:absolute; color:yellow; font-size:20px; font-family:Arial">Score: 0</p>
</body>
<script>
  var score = 0, yChange = 3, speed = 5, gameTimer;
  document.onkeydown = handleKeys;
  onready = startUp();

  function setLeft(id, x) {
    document.getElementById(id).style.left = x + "px";
  }
  function setTop(id, y) {
    document.getElementById(id).style.top = y + "px";
  }
  function getLeft(id) {
    return document.getElementById(id).offsetLeft;
  }
  function getTop(id) {
    return document.getElementById(id).offsetTop;
  }
  function randomNumber(low, high) {
    return (Math.floor(low + Math.random() * (1 + high - low)));
  }
  function isOverlapping(ob1, ob2) {
    return ((getLeft(ob1) + 100 > getLeft(ob2)) && (getLeft(ob1) < getLeft(ob2) + 100) &&
      (getTop(ob1) + 100 > getTop(ob2)) && (getTop(ob1) < getTop(ob2) + 100));
  }
  function startUp() {
    gameTimer = window.setInterval(moveThings, 20);
  }
  function moveThings() {
    for (var n = 1; n <= 3; n++) {
      var x = getLeft("rock" + n);
      if (x < -100) {
        x = window.innerWidth;
        y = randomNumber(0, window.innerHeight - 100);
        setTop("rock" + n, y);
        score = score + 10;
        document.getElementById("scoreTB").innerText = "Score: " + score;
      }
      setLeft("rock" + n, x - speed - n);
      if (isOverlapping("rock" + n, "ship")) {
        gameOver();
      }
    }
    var y = getTop("ship");
    if ((y <= 0) || (y > window.innerHeight - 100)) {
      yChange = -yChange;
    }
    setTop("ship", y + yChange);
  }
  function handleKeys(e) {
    if (e.keyCode == 38) {
      yChange = -3;
    }
    if (e.keyCode == 40) {
      yChange = 3;
    }
  }
  function gameOver() {
    clearInterval(gameTimer);
    if (confirm("Game Over - Click OK to play again.") == true) {
      location.reload();
    }
  }
</script>
</html>
```

### 自定义

- 尝试通过改变岩石和飞船的速度来使游戏更难。
- 添加第四个名为`rock4`的岩石。修改循环使其移动。
- 构建你自己的游戏，让玩家必须躲避移动的对象。它可以在水下进行……

## 潜艇探险家

本游戏涉及玩家在屏幕上引导一艘潜艇，试图抓住从沉船上掉落的宝藏。它使用了一种不同的移动系统，该系统常用于驾驶游戏和侧向飞行游戏中，以便以一定角度操控和移动。游戏使用了一些复杂的数学计算来处理角度问题。游戏还包含基本音效。游戏的完整代码列在第29页。

### 步骤 1 - 规划

分数显示在HTML段落元素`<p>`中。

计时器将移动金币和潜艇。

每次潜艇移动时，我们需要检查它是否抓住了金币。这是通过使用一个测试重叠的函数来完成的。

如果金币被抓住，将播放音效。

变量用于计算分数、潜艇的速度、其行进角度及其坐标。

如果金币掉落到屏幕底部，游戏结束。

按下上、下箭头键将改变潜艇的角度，在屏幕上进行操控。

单击确定再次游玩或取消。

### 步骤 2 - 寻找一些图片

- 找到一张潜艇的图片使用。它需要保存到与HTML文件相同的文件夹中。
- 在互联网上搜索潜艇剪贴画。
- 右键单击一张图片。
- 单击 **将图像另存为...**
- 导航到你的 **文档** 文件夹，然后单击 **保存**。
- 现在重复此步骤，但搜索 **金币剪贴画** 使用。

### 步骤 3 - 声音文件

我们需要一个音效在潜艇抓住金币时播放。你的计算机上可能已有一些。如果没有，在网上搜索要下载使用的声音文件。

搜索结果中显示的每个网站都会不同。尝试找到一个允许你下载mp3文件的网站。

### 步骤 4 - 开始一个新文件

首先输入游戏的HTML代码。为`body`、两张图片和一个分数段落添加代码。

```
<html>
<body style="background-color:#2980b9">
    <img id="sub" style="position:absolute; top:500px; width:100px;"
         src="sub.png">
    <img id="coin" style="position:absolute; left:300px; width: 50px;"
         src="coin.png">
    <p id="scoreTB" style="position:absolute; color:white; font-size:
         20px; font-family:Arial">Score: 0</p>
</body>
```

设置背景颜色。

确保`src`属性与下载的潜艇文件名匹配。

确保`src`属性与下载的金币文件名匹配。

添加分数段落。

### 步骤 5 - 保存你的代码

单击 **文件 > 保存** 并输入 **sub.html** 作为文件名。

确保你将其保存在 **文档** 文件夹中。每次添加新代码时都要保存它。

### 步骤 6 - 开始脚本

在脚本的开头，我们需要：

- 创建所需的变量
- 告诉程序当按键按下时运行哪个函数
- 启动`gameTimer`并告诉它每20毫秒调用`moveThings`函数
- 定义一些函数来获取和设置坐标，以及生成随机数。

```
<script>
var score=0, angle=0, speed=4, subX=0, subY=500, gameTimer;
onkeydown=handleKeys;
gameTimer=window.setInterval(moveThings,20);
function setLeft(id,x){document.getElementById(id).style.left=x+"px";}
function setTop(id,y){document.getElementById(id).style.top=y+"px";}
function getLeft(id){return document.getElementById(id).offsetLeft;}
function getTop(id){return document.getElementById(id).offsetTop;}
function randomNumber(low,high){return(Math.floor(low+Math.random()*(1+high-low)));}
```

### 步骤 7 - 重叠测试代码

我们将使用第20页用过的函数来测试名为`ob1`和`ob2`的对象是否重叠。

```
function isOverlapping(ob1, ob2){
return ((getLeft(ob1)+50>getLeft(ob2)) && (getLeft(ob1)<getLeft(ob2)+50) &&
(getTop(ob1)+50>getTop(ob2)) && (getTop(ob1)<getTop(ob2)+50));}
```

我们需要对Rock Storm游戏进行一些调整。这一次，其中一个对象要小得多，所以我们需要将100改为50。

### 以一定角度移动

当我们用JavaScript编码时，让对象左右或上下移动相当简单。我们只需确保其`position`属性设置为`absolute`，然后更改`left`（x坐标）和`top`（y坐标）样式值。要使其以一定角度移动，我们需要使用一些更复杂的数学知识。如果你不完全理解，不要担心，但试着找出以下代码行中哪些部分使其移动，这样你就可以将其应用到你制作的其他游戏中。

如果潜艇以30度角向下移动，那么它的运动可以分解为向下移动多少和向右移动多少。

通过使用数学函数 **正弦** 和 **余弦**，我们可以将角度移动转换为水平和垂直移动的组合。在JavaScript中，我们将其输入为`Math.sin`和`Math.cos`：

通过 **速度** 乘以潜艇角度的余弦值来改变`subX`。

```
subX=subX+speed*Math.cos(Math.PI*angle/180);
subY=subY+speed*Math.sin(Math.PI*angle/180);
```

通过 **速度** 乘以潜艇角度的正弦值来改变`subY`。

### 步骤 8 – 移动物体

每次计时器调用函数时，我们需要移动潜艇和金币。该函数还调用另一个函数`checkHit`，用于测试潜艇是否抓住了金币。最后，我们检查金币是否已经一路掉到海底。

```
function moveThings(){
  subX=subX+speed*Math.cos(Math.PI*angle/180);
  subY=subY+speed*Math.sin(Math.PI*angle/180);
  if(subX<-100){subX=innerWidth;}
  if(subX>innerWidth){subX=-100;}
  if(subY<-100){subY=innerHeight;}
  if(subY>innerHeight){subY=-100;}
  setLeft("sub",subX);
  setTop("sub",subY);
  y=getTop("coin");
  setTop("coin", y+1+score*0.1);
  checkHit();
  if(y>window.innerHeight){gameOver();}
}
```

根据潜艇的角度更改变量`subX`和`subY`。

如果潜艇已经过了屏幕左边缘，将其移到右边。

如果它已经太靠右，将其全部移到左侧。

如果它已经太高，将其移到底部。

如果它已经太低，将其移到顶部。

现在我们已经计算出新的坐标，需要移动潜艇。

找出金币的位置并将其存储在变量`y`中。

将金币向下移动，随着分数增加移动速度加快。

调用将检查它们是否碰撞的函数。

如果金币已经过了屏幕底部边缘，则添加结束游戏的代码。

### 步骤 9 – 正中目标？

此函数通过测试它们是否重叠来检查潜艇是否抓住了金币。如果重叠，分数增加，金币移回顶部，并播放音效。

```
function checkHit(){
  if(isOverlapping("sub", "coin")){
    score++;
    document.getElementById("scoreTB").innerHTML="Score: "+score;
    setTop("coin",0);
    setLeft("coin",randomNumber(0,innerWidth-100));
    new Audio("beep.mp3").play();
  }
}
```

测试潜艇是否与金币重叠。如果是，运行以下代码：

将分数增加1。

将金币移回屏幕顶部。

为金币设置一个新的随机左侧位置。

播放音效。确保你在引号之间输入的文件名与你在步骤3中下载的mp3文件匹配。

结束IF语句。

### 自定义

- 通过思考Rock Storm游戏在第18到23页的工作原理，使用多于一个金币。
- 制作一个新游戏，使用类似的代码驾驶汽车。

### 步骤 10 – 操控潜艇

输入下面的函数来处理按键事件。它更改角度变量并旋转图像。

```
function handleKeys(e){
  if(e.keyCode==38){angle=angle-10;}
  if(e.keyCode==40){angle=angle+10;}
  document.getElementById("sub").style.webkitTransform = 'rotate('+angle+'deg)';
}
```

如果收到了 **上** 箭头键的代码，则将角度变量减少10度。

如果收到了 **下** 箭头键的代码，则将角度变量增加10度。

更改图像的显示角度以匹配角度变量。

### 步骤 11 – 游戏结束

如果其中一个金币到达海底，将需要运行以下函数：

```
function gameOver(){
  clearInterval(gameTimer);
  if(confirm("Game Over - Click OK to play again.")==true){
    location.reload();
  }
}
</script>
</html>
```

停止计时器运行以停止物体移动。

显示一条消息询问玩家是否想再玩一次？如果他们单击确定，则运行下一行。

重新加载页面并让游戏重新开始。

结束IF语句。

结束函数。

结束脚本。

结束HTML。

保存你的文件，重新加载浏览器，然后开始玩！

### 完整代码

```html
<html>
<body style="background-color:#2980b9">
    <img id="sub" style="position:absolute; top:500px; width:100px;" src="sub.png">
    <img id="coin" style="position:absolute; left:300px; width: 50px;" src="coin.png">
    <p id="scoreTB" style="position:absolute; color:white; font-size:20px; font-family:Arial;">分数: 0</p>
</body>
<script>
    var score=0, angle=0, speed=4, gameTimer, subX=0, subY=500;
    onkeydown=handleKeys;
    gameTimer=window.setInterval(moveThings, 20);
    function setLeft(id,x){document.getElementById(id).style.left=x+"px";}
    function setTop(id,y){document.getElementById(id).style.top=y+"px";}
    function getLeft(id){return document.getElementById(id).offsetLeft;}
    function getTop(id){return document.getElementById(id).offsetTop;}
    function randomNumber(low,hi){return(Math.floor(low+Math.random()*(1+hi-low)));}
    function isOverlapping(ob1, ob2){
        return ((getLeft(ob1)+50>getLeft(ob2)) && (getLeft(ob1)<getLeft(ob2)+50) && 
        (getTop(ob1)+50>getTop(ob2)) && (getTop(ob1)<getTop(ob2)+50));}
    function moveThings(){
        subX=subX+speed*Math.cos(Math.PI*angle/180);
        subY=subY+speed*Math.sin(Math.PI*angle/180);
        if(subX<-100){subX=innerWidth;}
        if(subX>innerWidth){subX=-100;}
        if(subY<-100){subY=innerHeight;}
        if(subY>innerHeight){subY=-100;}
        setLeft("sub",subX);
        setTop("sub",subY);
        y=getTop("coin");
        setTop("coin", y+1+score*0.1);
        checkHit();
        if(y>window.innerHeight){gameOver();}
    }
    function checkHit(){
        if(isOverlapping("sub","coin")){
            score++;
            document.getElementById("scoreTB").innerHTML="分数: "+score;
            setTop("coin",0);
            setLeft("coin",randomNumber(0,innerWidth-100));
            new Audio("beep.mp3").play();
        }
    }
    function handleKeys(e){
        if(e.keyCode==38){angle=angle-10;}
        if(e.keyCode==40){angle=angle+10;}
        document.getElementById("sub").style.webkitTransform = 'rotate('+angle+'deg)';
    }
    function gameOver(){
        clearInterval(gameTimer);
        if(confirm("游戏结束 - 点击确定重新开始。")==true){
            location.reload();
        }
    }
</script>
</html>
```

## 术语表

动画 - 使程序中的对象移动。

重叠 - 当对象发生碰撞但并非完全处于同一位置时。

变量 - 程序中用于存储可变化信息的值。

浏览器 - 用于查看网页的程序，例如 Chrome 或 Internet Explorer。

像素 - 屏幕上的一个小点，可用作计量单位。

### 缺陷与调试

缺陷 - 程序中导致其无法正常工作的错误。

属性 - 关于元素样式的信息，例如其颜色或大小。

#### 查找缺陷的技巧：

- 当你发现代码未能按预期工作时，停下来检查你输入的每一行代码。以下是一些检查事项：
- 检查你是否正确拼写了命令。
- 检查你是否使用了正确的大小写。
- 检查你是否遗漏了任何引号。
- 检查你是否正确关闭了标签。
- 如果图像没有显示，请检查文件名是否输入准确。
- 如果图像没有移动，请检查你是否设置了`position:absolute`。
- 确保你使用了正确类型的括号和其他符号。

调试 - 从程序中移除缺陷（或错误）。

随机数 - 由计算机选择的、无法预测的数字。

元素 - 构成网页的对象之一，例如段落或图像。

标签 - HTML文档中的特殊词，被尖括号`<>`包围，用于定义一个元素。

事件 - 程序运行时发生的事情，例如鼠标点击或按键。

文本编辑器 - 用于创建和修改代码的程序。

函数 - 结合多个命令的可重用代码段。

计时器 - 在指定延迟后或按固定间隔运行函数的对象。

HTML（超文本标记语言） - 用于构建网页的语言。

二维数组 - 用于表示数据网格或表格的列表的列表。

JavaScript - 一种用于使网页交互或构建简单游戏的编程语言。

## 命令列表

### JavaScript 命令

- `alert("Hello");` – 在弹出框中显示 "Hello" 消息。
- `var score=0;` – 定义一个名为`score`的变量。
- `var gameTimer=window.setInterval(myFunction, 1000);` – 每秒运行一个名为`myFunction`的函数。
- `clearInterval(gameTimer);` – 停止名为`gameTimer`的计时器。
- `function gameOver();` – 定义一个名为`gameOver()`的函数。
- `document.getElementById("dog")` – 选择页面上的一个元素。
- `Math.random()` – 创建一个0到1之间的随机数。
- `Math.round()` – 将小数四舍五入到最接近的整数。
- `location.reload();` – 重新加载页面以重新启动JavaScript（和游戏）。

### HTML 元素

- `<html>...</html>` – 开始和结束HTML文件。
- `<script>...</script>` – 开始和结束脚本部分。
- `<img>` – 标记一张图像，例如照片或剪贴画。
- `<p>...</p>` – 标记一个段落或一行文本。
- `<body>...</body>` – 开始和结束页面的主体，实际上就是你程序的背景。

### 事件

- `onclick` – 鼠标被点击。
- `onmousedown` – 鼠标被按下（发生在click和mouseup之前）。
- `onmouseup` – 鼠标按钮被释放。
- `onkeydown` – 键盘上的一个键被按下。

### 减少缺陷的技巧

- 🐞 如果你要制作自己的网页，请在开始之前花时间规划。
- 🐞 练习调试！制作一个非常简单的网页，让一个朋友在你看不到时修改一行代码。你能修复它吗？
- 🐞 当一切正常运行时，花时间查看你的代码，以便理解每一行。要善于调试，你需要理解你代码的每一行是做什么的以及你的代码是如何工作的。

### 样式属性

- `position:absolute` – 允许通过更改`left`和`top`属性来移动元素。
- `left` – 设置元素（如图像）在屏幕上水平方向的位置。
- `top` – 设置元素距离屏幕顶部的垂直位置。
- `height` – 设置元素的高度，例如图像（例如20px表示20像素高）。
- `width` – 设置元素的宽度，例如图像。
- `-webkit-transition` – 设置元素属性变化的速度。

## 索引

- **角度** 24, 27, 28
- **动画** 7, 30
- **方向键** 6, 9, 12, 15, 18, 22, 24, 28
- **括号** 5, 14, 30
- **缺陷** 30, 31
- **颜色** 7, 13, 16, 19, 25
- **逗号** 14
- **命令** 10, 15, 30, 31
- **坐标** 6, 7, 8, 9, 10, 12, 14, 15, 16, 19, 20, 21, 24, 26, 27
- **余弦** 27
- **调试** 30, 31
- **元素** 5, 7, 8, 13, 14, 16, 18, 19, 22, 24, 26, 30, 31
- `div` 13, 15
- 动态 16
- **函数** 7, 8, 9, 10, 14, 15, 16, 18, 20, 21, 22, 24, 26, 27, 28, 30, 31
- **游戏** 3, 5, 6–11, 12–17, 18–23, 24–29
- **碰撞检测** 20, 22, 27, 28
- **HTML** 3, 5, 6, 7, 8, 10, 12, 13, 16, 18, 19, 22, 24, 25, 30, 31
- **IF语句** 15, 21, 22, 28
- **图像** 5, 6, 7, 8, 10, 12, 16, 18, 19, 24, 25, 28, 30, 31
- **键盘事件** 5, 6, 7, 9, 12, 14, 18, 19, 22, 24, 26, 28, 30, 31
- **循环** 15, 16, 21, 22, 23
- **迷宫** 12-17
- **鼠标事件** 5, 9, 30, 31
- **段落** 6, 7, 8, 10, 18, 19, 24, 25, 31
- **参数** 9
- **像素** 8, 15, 20, 30
- **引号** 28, 30
- **随机数** 7, 9, 19, 21, 26, 28, 30, 31
- **得分** 5, 6, 7, 10, 18, 19, 21, 24, 25, 27, 28, 31
- **正弦** 27
- **音效** 24, 25, 28
- **src属性** 7, 13, 19, 25
- **startUp函数** 8, 20
- **样式属性** 7, 8, 13, 27
- **标签** 5, 30, 31
- **文本编辑器** 3, 4, 5, 30
- Sublime Text 4, 5
- **计时器** 6, 7, 8, 10, 18, 20, 21, 22, 24, 26, 27, 28, 30, 31
- **过渡属性** 7
- **二维数组** 12, 13, 14, 15, 16, 30
- **变量** 6, 7, 8, 9, 12, 14, 18, 19, 21, 22, 24, 26, 27, 28, 30, 31
- **网页浏览器** 3, 4, 5, 8, 10, 16, 20, 28, 30
- **网页** 2, 3, 4, 5, 31

### 可调节式救生衣

`www.torreslifejacket.co.uk`

020 8520 0012

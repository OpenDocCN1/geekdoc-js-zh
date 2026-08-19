# Topalian JavaScript 数学生成器











**Christopher Andrew Topalian**




**献给**
**父神**
**上帝**


# 数学练习生成器

生成

25
43
7

不正确

# 数学练习生成器

生成

25
43
68

正确 :-)

# 数学练习生成器

生成

89
37
126

正确 :-)

# 数学练习生成器

生成

74
78
152

正确 :-)


<!-- 献给父神上帝 -->
<!-- 版权所有 Christopher Topalian -->
<!-- 版权 2000-2024 -->
<!-- https://github.com/ChristopherTopalian -->
<!-- <!--
https://github.com/ChristopherAndrewTopalian n -->
<!-- Topalian_JavaScript_Math_Generator.html -->
<!-- 版本 001 - (2024-01-16) -->
<html>


<head>
<title> Topalian JavaScript 数学生成器 </title>
<link rel='stylesheet' href='css/style001.css'>
<script>
function ge(whichId) {
let result=document.getElementById(whichId);
return result;
}
function ce(whichType)

{
let result=document.createElement(whichType);
return result;
}
function ba(whichElement) {
let result=document.body.append(whichElement);
return result;
}
function createMathGenerator() {
// mainDiv
let mainDiv=ce('div');
mainDiv.id='mainDiv';
mainDiv.className='mainDiv';
mainDiv.style.position='relative';
mainDiv.style.width=300 + 'px';
ba(mainDiv);
//-//
// theTitle
let theTitle=ce('div');
theTitle.innerHTML='数学练习生成器';
theTitle.className='theTitle';
mainDiv.append(theTitle);
//-//
// generate button
let generateButton=ce('button');
generateButton.textContent='生成';
generateButton.id='generateButton';
generateButton.className='buttonStyle001';
generateButton.onclick=function() {
ge('textBox1').value=Math.floor(Math.random() * 100);
ge('textBox2').value=Math.floor(Math.random() * 100);
ge('textBox3').value='';
ge('textBox4').value='';
ge('mainDiv').style.borderColor='rgb(255, 255, 255)';
};
mainDiv.append(generateButton);
//-//
// textBox1
let textBox1=ce('input');
textBox1.type='text';
textBox1.value=Math.floor(Math.random() * 100);
textBox1.id='textBox1';
mainDiv.append(textBox1);
//-//
// textBox2
let textBox2=ce('input');
textBox2.type='text';
textBox2.value=Math.floor(Math.random() * 100);
textBox2.id='textBox2';
mainDiv.append(textBox2);
//-//
// textBox3
let textBox3=ce('input');
textBox3.type='text';
textBox3.id='textBox3';
textBox3.change=function() {
let textBox1=parseFloat(ge('textBox1').value);
let textBox2=parseFloat(ge('textBox2').value);
let textBox3=parseFloat(ge('textBox3').value);
let evaluated=textBox1 + textBox2;
if (textBox3 == evaluated) {
console.log('Correct');
textBox4.value='Correct :-)';
mainDiv.style.borderColor='rgb(255, 255, 255)';
} else {
console.log('Not that');
textBox4.value='不正确';
mainDiv.style.borderColor='rgb(255, 0, 0)';
}
mainDiv.append(textBox3);
//-//
// textBox4
let textBox4=ce('input');
textBox4.type='text';
textBox4.id='textBox4';
mainDiv.append(textBox4);
}
</script>
</head>
<body onload='createMathGenerator()'>
</body>
</html>

<!-- 献给父神上帝 -->
<!-- 版权所有 Christopher Topalian -->
<!-- 版权 2000-2024 -->
<!-- https://github.com/ChristopherTopalian -->
<!-- <!--
https://github.com/ChristopherAndrewTopalian n -->
<!-- Topalian_JavaScript_Math_Generator.html -->
<!-- 版本 001 - (2024-01-16) -->
<html>


<head>
<title> Topalian JavaScript 数学生成器 </title>
<link rel='stylesheet' href='css/style001.css'>
<script>
function ge(whichId) {
let result=document.getElementById(whichId);
return result;
}
function ce(whichType)

{
let result=document.createElement(whichType);
return result;
}
function ba(whichElement) {
let result=document.body.append(whichElement);
return result;
}
function createMathGenerator() {
// mainDiv
let mainDiv=ce('div');
mainDiv.id='mainDiv';
mainDiv.className='mainDiv';
mainDiv.style.position='relative';
mainDiv.style.width=300 + 'px';
ba(mainDiv);
//-//
// theTitle
let theTitle=ce('div');
theTitle.innerHTML='数学练习生成器';
theTitle.className='theTitle';
mainDiv.append(theTitle);
//-//
// generate button
let generateButton=ce('button');
generateButton.textContent='生成';
generateButton.id='generateButton';
generateButton.className='buttonStyle001';
generateButton.onclick=function() {
ge('textBox1').value=Math.floor(Math.random() * 100);
ge('textBox2').value=Math.floor(Math.random() * 100);
ge('textBox3').value='';
ge('textBox4').value='';
ge('mainDiv').style.borderColor='rgb(255, 255, 255)';
};
mainDiv.append(generateButton);
//-//
// textBox1
let textBox1=ce('input');
textBox1.type='text';
textBox1.value=Math.floor(Math.random() * 100);
textBox1.id='textBox1';
mainDiv.append(textBox1);
//-//
// textBox2
let textBox2=ce('input');
textBox2.type='text';
textBox2.value=Math.floor(Math.random() * 100);
textBox2.id='textBox2';
mainDiv.append(textBox2);
//-//
// textBox3
let textBox3=ce('input');
textBox3.type='text';
textBox3.id='textBox3';
textBox3.change=function() {
let textBox1=parseFloat(ge('textBox1').value);
let textBox2=parseFloat(ge('textBox2').value);
let textBox3=parseFloat(ge('textBox3').value);
let evaluated=textBox1 + textBox2;
if (textBox3 == evaluated) {
console.log('Correct');
textBox4.value='Correct :-)';
mainDiv.style.borderColor='rgb(255, 255, 255)';
} else {
console.log('Not that');
textBox4.value='不正确';
mainDiv.style.borderColor='rgb(255, 0, 0)';
}
mainDiv.append(textBox3);
//-//
// textBox4
let textBox4=ce('input');
textBox4.type='text';
textBox4.id='textBox4';
mainDiv.append(textBox4);
}
</script>
</head>
<body onload='createMathGenerator()'>
</body>
</html>






```css
.buttonStyle001 {
  padding-top: 3px;
  padding-bottom: 3px;
  padding-left: 10px;
  padding-right: 10px;
  border-radius: 8px;
  background-color: rgb(0, 0, 0);
  font-family: arial;
  font-size: 20px;
  color: rgb(255, 255, 255);
}

.buttonStyle001:hover {
  border-color: rgb(0, 255, 255);
}

.buttonStyle001:active {
  color: rgb(0, 255, 255);
}
```


真正的人工智能系统
同言

| 术语 | 二进制 |
| :--- | :--- |
| 矛盾反对 | 1111 |
| 异或 (XOR) | 0000 |
| 价异或 (XNOR) | 0110 |
| 与 (AND) | 1001 |
| 非与 (NAND) | 0001 |
| 或 (OR) | 1110 |
| 非或 (NOR) | 0111 |
| MI | 1000 |
| MNI | 1101 |
| LP | 0010 |
| LC | 0011 |
| RP | 1100 |
| RC | 0101 |
| CI | 1010 |
| CNI | 1011 |
| 16边形 | |

![](img/865544a8e1192fb8e223d4b06c92518d_23_0.png)

更多教程：
- CollegeOfScripting.weebly.com
- CollegeOfScripting.wordpress.com
- Youtube.com/ScriptingCollege
- Twitter.com/CollegeOfScript
- GitHub.com/ChristopherTopalian
- GitHub.com/ChristopherAndrewTopalian
- Sites.google.com/view/CollegeOfScripting

![](img/865544a8e1192fb8e223d4b06c92518d_24_0.png)

献给父神

本书由脚本音乐与科学学院 (College of Scripting Music & Science) 创作。

始终记住，每当你用笔和纸写脚本时，它就会深深地印在记忆中，从而让你极好地掌握材料和方法。

当你输入脚本时，也是如此。你通过键盘或纸笔输入和写出的脚本越多，你学到的编程就越多！

写下并输入你看到的每一个示例。
保持你所有的脚本整洁。
你创建的每一个脚本都会提升你的编程能力。

**看到代码**是一回事，但**编写代码**是另一回事。

写下它、输入它、说出它、看到它、梦见它。

CollegeOfScripting.weebly.com


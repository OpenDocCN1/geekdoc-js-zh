# Topalian JavaScript 密码生成器 002













**献给**
**天**
**父神**


双击 **Launch.html**

# 密码生成器
# Launch.html


**Topalian_JavaScript_Password_Generator.html**



<!-- 献给天父神 -->
<!-- 版权所有 Christopher Andrew Topalian Copyright 2000-2023 -->
<!-- https://github.com/ChristopherTopalian -->
<!-- https://github.com/ChristopherAndrewTopalian -->
<!-- Launch.html -->
<html>
<head>
<title>Topalian JavaScript 密码生成器启动器</title>


<style>
body {
  background-color: rgb(40,40,40);
  background-image: url('Topalian_JavaScript_Password_Generator/texture/code.webp');
  font-size: 20px;
  font-weight: bold;
  color: rgb(255,255,255);
}
.buttonLauncher {
  position: fixed;
  left: 20px;
  top: 20px;
  width: 200px;
  height: 100px;
  border-style: solid;
  border-width: 5px;
  border-radius: 5px;
  border-color: rgb(0,0,0);
  background-color: rgb(5,5,84);
  font-size: 30px;
  font-weight: bold;
  color: white;
  line-height: 30px;
}
.buttonLauncher:hover {
  border-color: rgb(0,255,255);
  color: rgb(0,255,255);
  cursor: pointer;
}
.buttonLauncher:active {
  border-color: rgb(255,255,255);
  color: rgb(255,255,255);
}
</style>
<script>
function createWindow() {
  let newWindow = window.open("Topalian_JavaScript_Password_Generator/Topalian_JavaScript_Password_Generator.html", "", "left = 10 top = 10 width = 450, height = 255", true);
  // 等待指定时长后移除启动器
  setTimeout(function() {
    window.close();
  }, 500)
}
</script>
</head>


<body>
<button onclick="createWindow();" class='buttonLauncher'> 密码生成器</button>
</body>
</html>

<!-- 献给天父神 -->
<!-- https://github.com/ChristopherTopalian -->
<!-- https://github.com/ChristopherAndrewTopalian -->
<!-- Topalian_JavaScript_Generator.html -->
<!-- 版本 002 -->

<html>
<head>
<title> Topalian 密码生成器</title>
<link rel="stylesheet" href="css/style01.css">
<script>
// 当前密码长度为 12
let passwordLength = 12;
// 可以注释掉任何我们不想包含在生成中的符号
let symbolsArray = ["0","1","2","3","4","5","6","7","8","9","a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z","A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z","!","@","#","$%","^","&","?"];

function createGenerator() {
  let mainDiv = document.createElement("div");
  mainDiv.className = "mainDiv";
  document.body.append(mainDiv);
  let passwordTextBox = document.createElement("textarea");
  passwordTextBox.className = "passwordTextBox";
  passwordTextBox.id = "passwordTextBox";
  mainDiv.append(passwordTextBox);
  let lineBelowTextBox = document.createElement("hr");
  mainDiv.append(lineBelowTextBox);
  let buttonSection = document.createElement('div');
  mainDiv.append(buttonSection);
  let generateButton = document.createElement("button");
  generateButton.className = "button001";
  generateButton.innerHTML = "生成";
  generateButton.onclick = function() {
    generateRandomPassword(symbolsArray);
  };
  buttonSection.append(generateButton);
  let copyButton = document.createElement("button");
  copyButton.className = "button002";
  copyButton.innerHTML = "复制";
  copyButton.onclick = function() {
    copyText();
  };
  buttonSection.append(copyButton);
  let lineBelowCopyButton = document.createElement("hr");
  mainDiv.append(lineBelowCopyButton);
  let passwordLengthTitle = document.createElement("div");
  passwordLengthTitle.className = "passwordLengthTitle";
  passwordLengthTitle.innerHTML = "密码长度";
  mainDiv.append(passwordLengthTitle);
}
</script>
</head>
</html>





////-

let passwordLengthTextBox = document.createElement("input");
passwordLengthTextBox.className = "passwordLengthTextBox";
passwordLengthTextBox.id = "passwordLengthTextBox";
passwordLengthTextBox.value = passwordLength;
passwordLengthTextBox.onkeyup = function() {
  passwordLength = passwordLengthTextBox.value;

  document.getElementById("passwordLengthSlider").value = passwordLength;
};
mainDiv.append(passwordLengthTextBox);

////-

let passwordLengthSlider = document.createElement("input");
passwordLengthSlider.className = "passwordLengthSlider";
passwordLengthSlider.id = "passwordLengthSlider";
passwordLengthSlider.type = "range";
passwordLengthSlider.min = 1;
passwordLengthSlider.max = 200;

passwordLengthSlider.value = passwordLength;
passwordLengthSlider.oninput = function() {
  document.getElementById("passwordLengthTextBox").value = passwordLengthSlider.value;
  passwordLength = document.getElementById("passwordLengthTextBox").value = passwordLengthSlider.value;
};
mainDiv.append(passwordLengthSlider);
}

function copyText() {
  let copyText = document.getElementById("passwordTextBox");
  copyText.select();
  copyText.setSelectionRange(0, 1000);
  document.execCommand("copy");
  console.log(document.getElementById("passwordTextBox").value);
}

function generateRandomPassword(whichArray) {
  // 创建一个名为 randomSymbolsArray 的空数组
  let randomSymbolsArray = [];
  for (let i = 0; i < passwordLength; i++) {
    // 遍历 whichArray
    for (let x = 0; x < whichArray.length; x++) {
      // 将随机符号添加到 randomSymbolsArray
      randomSymbolsArray.push(whichArray[Math.floor(Math.random() * whichArray.length)]);
    }
  }

} // 从 randomSymbolsArray 中移除逗号
randomSymbolsArray = randomSymbolsArray.join("");
// passwordLength 当前被设置为 12
// 下面，我们使用 slice 函数从 randomSymbolsArray 中提取 12 个项目
// 以创建随机密码
// slice 函数有 start 和 end 参数
// 我们从 0 开始提取，提取到（但不包含）结束位置：12
// 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11 意味着我们从 randomSymbolsArray 中提取了 12 个项目

randomSymbolsArray = randomSymbolsArray.slice(0, passwordLength);
// 显示生成的随机密码 randomSymbolsArray
document.getElementById("passwordTextBox").innerHTML = randomSymbolsArray;
}
function whenLoaded() {
  createPasswordGenerator();
  generateRandomPassword(symbolsArray);
}

</script>
</head>
<body onload="whenLoaded()">
</body>
</html>

/* 献给父神 */
/* 版权所有 Christopher Andrew Topalian Copyright 2000-2023 */
/* https://github.com/ChristopherTopalian */
/*
https://github.com/ChristopherAndrewTopalian */
/* style001.css */
body {
  background-color: rgb(40, 40, 40);
}

hr {
  width: 400px;
  padding-top: 1px;
  padding-bottom: 1px;
  height: 1px;
  margin-top: 1px;
  margin-bottom: 1px;
}
mainDiv {
  position: relative;
  top: 0px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.button01 {
  margin: 4px;
  padding-left: 10px;
  padding-right: 10px;
  border: solid;
  border: 1px;
  border-radius: 8px;
  background-color: rgb(0, 0, 0);
  font-family: arial;
  font-size: 20px;
  font-weight: bold;
  color: rgb(255, 255, 255);
  text-align: center;
}
.button01:hover {
  border-color: rgb(0, 255, 255);
}
.button01:active {
  position: relative;
  top: 1px;
  color: rgb(0, 255, 255);
}

.button02 {
  margin: 4px;
  padding-left: 10px;
  padding-right: 10px;
  border: solid;
  border: 1px;
  border-radius: 8px;
  background-color: rgb(50, 50, 50);
  font-family: arial;
  font-size: 20px;
  font-weight: bold;
  color: rgb(255, 255, 255);
  text-align: center;
}
.button02:hover {
  border-color: rgb(0, 255, 255);
}
.button02:active {
  position: relative;
  top: 1px;
  color: rgb(0, 255, 255);
}
![](img/b0db8f5f73016fec5c6999ccbaffec34_35_0.png)
.passwordTextBox {
  height: 100px;
  padding-left: 10px;
  padding-right: 10px;
  padding-top: 5px;
  padding-bottom: 5px;
  margin-bottom: 0px;
  background-color: rgb(40, 40, 40);
  border: solid;
  border: 3px;
  border-color: rgb(120, 120, 120);
  border-radius: 8px;
  font-family: arial;
  font-size: 30px;
  color: rgb(255, 255, 255);
  text-align: center;
  overflow-y: scroll;
}
.passwordLengthTitle {
  padding-top: 1px;
  margin-top: 0px;
  margin-bottom: 0px;
  font-family: arial;
  font-size: 20px;
  font-weight: bold;
  color: rgb(200, 200, 200);
}
.passwordLengthTextBox {
  width: 100px;
}






```css
{
  margin-top: 1px;
  margin-bottom: 4px;
  border-radius: 8px;
  background-color: rgb(0, 0, 0);
  font-size: 20px;
  font-weight: bold;
  color: rgb(255, 255, 255);
  text-align: center;
  resize: none;
}

.passwordLengthSlider {
  margin-top: 2px;
  width: 400px;
  border-style: solid;
  border-width: 1px;
  border-color: rgb(70, 70, 70);
```


```css
  border-radius: 8px;
  background-color: rgb(0, 0, 0);
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
}
```


真正的人工智能系统

| 术语 | 二进制 |
| :--- | :--- |
| 恒真式 | 1111 |
| 矛盾式 | 0000 | |
| 异门 (XOR) | 0110 |
| 异否门 (XNOR) | 1001 |
| 与门 (AND) | 0001 |
| 非与门 (NAND) | 1110 |
| 或门 (OR) | 0111 |
| 非或门 (NOR) | 1000 |
| MI | 1101 |
| MNI | 0010 |
| LP | 0011 |
| LC | 1100 |
| RP | 0101 |
| RC | 1010 |
| CI | 1011 |
| CNI | 0100 |
| 16边形 | |

![](img/b0db8f5f73016fec5c6999ccbaffec34_41_0.png)

更多教程：

- CollegeOfScripting.wordpress.com
- Youtube.com/ScriptingCollege
- Twitter.com/CollegeOfScript
- GitHub.com/ChristopherTopalian
- GitHub.com/ChristopherAndrewTopalian
- Sites.google.com/view/CollegeOfScripting

![](img/b0db8f5f73016fec5c6999ccbaffec34_42_0.png)

献给父父神

本书由脚本音乐与科学学院（College of Scripting Music & Science）创建。

请始终记住，每当你用纸和笔编写脚本时，它都会深刻地印在记忆中，从而让你非常好地掌握这些材料和方法。

当你输入脚本时，情况也是如此。你通过键盘或纸笔输入并写出脚本得越多，你学到的编程就越多！

写下并输入你看到的每一个例子。保持你所有的脚本整洁。你创建的每一个脚本都能提高编程能力。

**看代码**是一回事，但**写代码**是另一回事。

写下它，输入它，说出它，看到它，梦见它。

CollegeOfScripting.weebly.com


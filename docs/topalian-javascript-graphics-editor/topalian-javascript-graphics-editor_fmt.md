
# Topalian JavaScript 图形编辑器

**献给我们的父神**

脚本音乐与科学学院

CollegeOfScripting.weebly.com

![](img/53420ea31f2d946491030784cbf3b0ae_7_0.png)

**>**

**n -->**

**>**

```html
<head>
<title>Topalian JavaScript 图形编辑器</title>
<link rel='stylesheet' href='css/style001.css'>
<script>
function ge(whichId) {
  let result = document.getElementById(whichId);
  return result;
}

function ce(whichType) {
  let result = document.createElement(whichType);
  return result;
}

function ba(whichElement) {
  let result = document.body.append(whichElement);
  return result;
}

function menuBrushOptions() {
  if (ge('mainLineWidthDiv')) {
    ge('mainLineWidthDiv').remove();
  }
  let mainDiv = ce('div');
  mainDiv.id = 'mainLineWidthDiv';
  mainDiv.style.position = 'fixed';
  mainDiv.style.right = '3px';
  mainDiv.style.top = '30px';
  ba(mainDiv);
  //-//
  let brushOptions = ce('div');
  mainDiv.append(brushOptions);
  //-//
```

```javascript
let lineWidthText = ce('span');
lineWidthText.innerHTML = '线宽';
lineWidthText.style.fontSize = '15px';
brushOptions.append(lineWidthText);
//-//
let linebreakLineWidthText = ce('br');
brushOptions.append(linebreakLineWidthText);
//-//
let lineWidthTextbox = ce('input');
lineWidthTextbox.type = 'text';
lineWidthTextbox.id = 'lineWidthTextbox';
```

```javascript
lineWidthTextbox.className = 'inputStyle001';
lineWidthTextbox.onkeyup = function() {
  lineWidth = lineWidthTextbox.value;
};
brushOptions.append(lineWidthTextbox);
//-//
let brushForceLabel = ce('div');
brushForceLabel.innerHTML = '力度 N/A';
brushForceLabel.id = 'brushForceLabel';
brushForceLabel.style.fontSize = '15px';
brushOptions.append(brushForceLabel);
//-//
```

```javascript
let brushForceTextbox = ce('input');
brushForceTextbox.type = 'text';
brushForceTextbox.id = 'brushForceTextbox';
brushForceTextbox.className = 'inputStyle001';
brushForceTextbox.title = 'brushForceTextbox';
brushForceTextbox.placeholder = 'N/A';
brushForceTextbox.onkeyup = function() {
  brushForce = brushForceTextbox.value;
};
brushOptions.append(brushForceTextbox);
//-//
brushOptions.append(ce('br'));
}
```

```javascript
function updateLineCap() {
  if (ge('roundCap')) {
    ctx.lineCap = 'round';
  } else if (ge('squareCap')) {
    ctx.lineCap = 'square';
  } else if (ge('buttCap')) {
    ctx.lineCap = 'butt';
  }
}
```

```javascript
function clearCanvas() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
}

function toolboxCreate() {
  let mainDivToolBox = ce('div');
  mainDivToolBox.id = 'toolbox';
  mainDivToolBox.className = 'mainDivToolBox';
  ba(mainDivToolBox);
  //-//
  // saveButton
  let saveButton = ce('button');
```

```javascript
saveButton.textContent = '保存';
  saveButton.id = 'saveButton';
  saveButton.className = 'toolboxButton';
  saveButton.onclick = function() {
    saveDrawing();
  };
  mainDivToolBox.append(saveButton);
  //-//
  let linebreakSaveButton = ce('br');
  mainDivToolBox.append(linebreakSaveButton);
  //-//
```

```javascript
// drawButton
let drawButton = ce('button');
drawButton.textContent = '绘制';
drawButton.id = 'drawButton';
drawButton.className = 'toolboxButton';
drawButton.onclick = function() {
  selectTool('draw');
};
mainDivToolBox.append(drawButton);
//-//
let linebreakDrawButton = ce('br');
mainDivToolBox.append(linebreakDrawButton);
```

```javascript
//-//
// eraseButton
let eraseButton = ce('button');
eraseButton.textContent = '擦除';
eraseButton.id = 'eraseButton';
eraseButton.className = 'toolboxButton';
eraseButton.onclick = function() {
  selectTool('erase');
};
mainDivToolBox.append(eraseButton);
//-//
let linebreakEraseButton = ce('br');
```

```javascript
mainDivToolBox.append(linebreakEraseButton);
//-//
let colorChooser = ce('input');
colorChooser.id = 'colorChooser';
colorChooser.type = 'color';
colorChooser.oninput = function() {
  lineColor = colorChooser.value;
};
mainDivToolBox.append(colorChooser);
//-//
mainDivToolBox.append(ce('hr'));
```

```javascript
//-//
let lineCapContainer = createElement('div');
mainDivToolBox.append(lineCapContainer);
//-//
let capText = createElement('label');
capText.textContent = '线端样式';
capText.style.fontSize = '13px';
capText.style.fontWeight = 'bold';
lineCapContainer.append(capText);
//-//
lineCapContainer.append(createElement('br'));
//-//
let roundCapCheckbox = createElement('input');
roundCapCheckbox.type = 'radio';
roundCapCheckbox.id = 'roundCap';
roundCapCheckbox.name = 'lineCapChoice';
roundCapCheckbox.onchange = function() {
    updateLineCap();
};
lineCapContainer.append(roundCapCheckbox);
//-//
let labelRound = createElement('label');
labelRound.id = 'labelRound';
labelRound.textContent = '圆角';
labelRound.className = 'labels';
lineCapContainer.append(labelRound);
//-//
lineCapContainer.append(createElement('br'));
//-//
let squareCapCheckbox = createElement('input');
squareCapCheckbox.type = 'radio';
squareCapCheckbox.textContent = '方方形';
squareCapCheckbox.id = 'squareCap';
squareCapCheckbox.className = 'labels';
squareCapCheckbox.onchange = function() {
    updateLineCap();
};
lineCapContainer.append(squareCapCheckbox);
//-//
let labelSquare = createElement('label');
labelSquare.id = 'labelSquare';
labelSquare.textContent = '方方形';
labelSquare.className = 'labels';
lineCapContainer.append(labelSquare);
//-//
lineCapContainer.append(createElement('br'));
//-//
let buttCapCheckbox = createElement('input');
buttCapCheckbox.type = 'radio';
buttCapCheckbox.textContent = '平圆头';
buttCapCheckbox.id = 'buttCap';
buttCapCheckbox.name = 'lineCapChoice';
buttCapCheckbox.className = 'labels';
buttCapCheckbox.onchange = function() {
    updateLineCap();
};
lineCapContainer.append(buttCapCheckbox);
//-//
let labelButt = createElement("label");
labelButt.textContent = '平圆头';
labelButt.id = 'labelButt';
labelButt.className = 'labels';
lineCapContainer.append(labelButt);
//-//
lineCapContainer.append(createElement('hr'));
//-//
// 清除按钮
let clearButton = createElement('button');
clearButton.textContent = '清空';
clearButton.className = 'toolbox';
clearButton.onclick = function() {
    let choice = confirm('全部擦除');
    if (choice) {
        clearCanvas();
    } else {
        return;
    }
};
mainDivToolBox.append(clearButton);
//-//
mainDivToolBox.append(createElement('hr'));
//-//
let githubLink = createElement('a');
githubLink.textContent = '代码';
githubLink.href = 'https://github.com/Christopher/JavaScript-Editor';
githubLink.target = '_blank';
githubLink.style.fontSize = '13px';
mainDivToolBox.append(githubLink);
//-//
let info = createElement('div');
info.textContent = 'JavaScript 编辑器';
info.style.fontSize = '12px';
mainDivToolBox.append(info);
function whenLoaded() {
    toolbox();
    brushOptions();
}
</script>
</head>
<body onload='whenLoaded()'>
<input type='file' id='imageInput' accept='image/*'>
<canvas id='drawingCanvas'></canvas>
<script>
let canvas = getElement('drawingCanvas');
canvas.width = 775;
canvas.height = 450;
let ctx = canvas.getContext('2d');
let lineWidth = 5;
let brushForce = 1.0;
let lineColor = `rgba(0, 0, 0, ${brushForce})`;
let colorPicker = getElement('colorPicker');
let paths = [];
let selectedTool = 'draw';
let drawing = false;
let erasing = false;
let lastPos;
canvas.addEventListener('mousedown', handleMouseDown);
canvas.addEventListener('mouseup', handleMouseUp);
canvas.addEventListener('mousemove', handleMouseMove);
function handleImageUpload(event) {
    let file = event.target.files[0];
    if (file) {
        let reader = new FileReader();
        reader.onload = function(e) {
            let img = new Image();
            img.onload = function() {
                canvas.width = img.naturalWidth;
                canvas.height = img.naturalHeight;
                ctx.clearRect(0, 0, canvas.width, canvas.height);
                ctx.drawImage(img, 0, 0, canvas.width, canvas.height);
            };
            img.src = e.target.result;
```



```javascript
reader.readAsDataURL(file);
```

```javascript
let imageInput = ge('imageInput');

if (imageInput) {
  imageInput.addEventListener('change', handleImageUpload);
} else {
  console.error("Element with id 'imageInput' not found.");
}
```

```javascript
function handleMouseDown(e) {
  if (selectedTool === 'draw') {
    drawing = true;
    startDrawing(e);
  } else if (selectedTool === 'erase') {
    erasing = true;
    startErasing(e);
  }
}
```

```javascript
function handleMouseUp() {
  if (drawing) {
    stopDrawing();
  } else if (erasing) {
    erasing = false;
    stopErasing();
  }
}
```

```javascript
function handleMouseMove(e) {
  if (drawing) {
    draw(e);
  } else if (erasing) {
    erasePath(e);
  }
}
```

```javascript
function startDrawing(e) {
  lastPos = getMousePos(e);
  ctx.beginPath();
  ctx.moveTo(lastPos.x, lastPos.y);
}
```

```javascript
function stopDrawing() {
  drawing = false;
  paths.push(ctx.getImageData(0, 0, canvas.width, canvas.height));
}
```

```javascript
function draw(e) {
  if (!drawing) {
    return;
  }
  let currentPos = getMousePos(e);
  ctx.lineTo(currentPos.x, currentPos.y);
  ctx.strokeStyle = lineColor;
  ctx.lineWidth = lineWidth;
  ctx.stroke();
}
```

```javascript
function startErasing(e) {
  if (!erasing) {
    return;
  }
  lastPos = getMousePos(e);
  ctx.beginPath();
  ctx.moveTo(lastPos.x, lastPos.y);
}
```

```javascript
function stopErasing() {
  if (!erasing) {
    return;
  }
  ctx.closePath();
}
```

```javascript
function erasePath(e) {
  if (!erasing) {
    return;
  }
  let currentPos = getMousePos(e);
  ctx.clearRect(currentPos.x - lineWidth / 2, currentPos.y - lineWidth / 2, lineWidth, lineWidth);
}
```

```javascript
function getMousePos(e) {
  let rect = canvas.getBoundingClientRect();
  return {
    y: e.clientY - rect.top
  };
}
```

```javascript
function selectTool(whichTool) {
  selectedTool = whichTool;
  drawing = false;
}
```

```javascript
function saveDrawing() {
  let dataUrl = canvas.toDataURL('image/png');
  let link = ce('a');
  link.href = dataUrl;
  link.download = 'drawing.png';
  link.click();
}
```

```css
body {
  background-color: rgb(80, 80, 80);
  color: rgb(255, 255, 255);
  text-shadow: 2px 2px 4px rgb(0, 0, 0);
}

canvas {
  border-style: solid;
  border-width: 1px;
  border-color: rgb(0, 0, 0);
}

a {
  text-decoration: none;
  color: rgb(0, 255, 255);
}

#drawingCanvas {
  position: absolute;
  left: 110px;
  top: 5px;
}

#toolbox {
  position: fixed;
  left: 0px;
  top: 0px;
  width: 70px;
  height: 400px;
  padding: 10px;
  border-style: solid;
  border-width: 1px;
  border-color: rgb(255, 255, 255);
  border-radius: 8px;
  overflow-y: scroll;
  scrollbar-width: thin;
}

.toolboxButton {
  padding: 5px;
  padding-right: 5px;
  padding-top: 3px;
  padding-bottom: 3px;
  margin-bottom: 2px;
  border-style: solid;
  border-width: 1px;
  border-radius: 8px;
  background-color: rgb(20, 20, 20);
  color: rgb(255, 255, 255);
  font-size: 15px;
  line-height: 17px;
}

.toolboxButton:hover {
  border-color: aqua;
}

.toolboxButton:active {
  color: aqua;
}

.labels {
  font-size: 13px;
}

.inputStyle01 {
  width: 70px;
  padding-left: 10px;
  padding-right: 10px;
  border-radius: 8px;
  border-color: rgb(255, 255, 255);
  background-color: rgb(0, 0, 0);
  font-size: 15px;
  color: rgb(255, 255, 255);
}

.imageInput {
  position: fixed;
  right: 0px;
  top: 0px;
  width: 100px;
  padding-left: 1px;
  padding-right: 1px;
  padding-top: 1px;
  padding-bottom: 1px;
  margin-bottom: 1px;
  border-style: solid;
  border-width: 1px;
  border-radius: 8px;
  border-color: rgb(255, 255, 255);
  background-color: rgb(20, 20, 20);
  font-size: 15px;
  color: rgb(255, 255, 255);
  line-height: 15px;
  z-index: 100;
}
```

| 运算 | 二进制 |
| :--- | :--- |
| 矛盾 | 1111 |
| 异或 | 0000 |
| 同异或 | 0110 |
| 与 | 1001 |
| 非与 | 0001 |
| 或 | 1110 |
| 非或 | 0111 |
| MI | 1000 |
| MNI | 1101 |
| LP | 0010 |
| LC | 0011 |
| RP | 1100 |
| RC | 0101 |
| CI | 1010 |
| CNI | 1011 |
| 16边形 | 0100 |

- CollegeOfScripting.weebly.com
- Youtube.com/ScriptingCollege
- Twitter.com/CollegeOfScript
- GitHub.com/ChristopherAndrewTopalian
- Sites.google.com/view/CollegeOfScripting

![](img/53420ea31f2d946491030784cbf3b0ae_52_0.png)

**献给父神**

本书由脚本音乐与科学学院（College of Scripting Music & Science）创作。

永远记住，每当你用笔和纸写脚本时，它会被深深地烙印在记忆中，从而极好地学习材料和方法。

当你输入脚本时也是如此。你通过键盘或纸笔输入和写出的脚本越多，你学到的编程知识就越多！

写下并输入你看到的每一个例子。

保持你所有脚本的整洁。

你创建的每一个脚本都会提升你的编程能力。

**看代码**是一回事，但**写代码**是另一回事。

写下它、输入它、说出它、看到它、梦见它。

CollegeOfScripting.weebly.com

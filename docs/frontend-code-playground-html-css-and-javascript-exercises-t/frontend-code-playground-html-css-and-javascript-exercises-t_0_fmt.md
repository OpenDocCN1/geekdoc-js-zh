
# 前端代码练习场：HTML、CSS 和 JavaScript 技能提升练习

献给：

亚历克西斯和塞巴斯蒂安·斯维基斯

感谢你们的支持。

## 更改背景颜色

### 描述

在本练习中，学生将创建一个简单的网页，其中包含一个按钮，点击该按钮可更改页面的背景颜色。本练习介绍基本的 DOM 操作和事件处理。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Change Background Color</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<button id="changeColorButton">Change Background Color</button>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
background-color: #f0f0f0;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
```

### JavaScript

```javascript
document.getElementById('changeColorButton').addEventListener('click', function() {
document.body.style.backgroundColor = getRandomColor();
});
function getRandomColor() {
const letters = '0123456789ABCDEF';
let color = '#';
for (let i = 0; i < 6; i++) {
color += letters[Math.floor(Math.random() * 16)];
}
return color;
}
```

## 显示/隐藏文本

### 描述

在本练习中，学生将创建一个网页，其中包含一个按钮，用于切换段落的可见性。本练习介绍使用 JavaScript 显示和隐藏元素的概念。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（显示/隐藏元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Show/Hide Text</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<button id="toggleTextButton">Show/Hide Text</button>
<p id="text" style="display: none;">This is a sample text that can be shown or hidden.</p>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
flex-direction: column;
align-items: center;
height: 100vh;
justify-content: center;
margin: 0;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
margin-bottom: 20px;
}
p {
font-size: 18px;
}
```

### JavaScript

```javascript
document.getElementById('toggleTextButton').addEventListener('click', function() {
const text = document.getElementById('text');
if (text.style.display === 'none') {
text.style.display = 'block';
} else {
text.style.display = 'none';
}
});
```

## 向列表添加项目

### 描述

在本练习中，学生将创建一个包含输入字段和按钮的网页，用于向列表添加项目。本练习介绍如何创建新元素并将其附加到 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（创建和附加元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Add Items to List</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<input type="text" id="itemInput" placeholder="Enter item">
<button id="addItemButton">Add Item</button>
<ul id="itemList"></ul>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
flex-direction: column;
align-items: center;
height: 100vh;
justify-content: center;
margin: 0;
}
input {
padding: 10px;
font-size: 16px;
margin-bottom: 10px;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
margin-bottom: 20px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
font-size: 18px;
margin: 5px 0;
}
```

### JavaScript

```javascript
document.getElementById('addItemButton').addEventListener('click', function() {
const itemInput = document.getElementById('itemInput');
const newItemText = itemInput.value;
if (newItemText !== '') {
const newItem = document.createElement('li');
newItem.textContent = newItemText;
document.getElementById('itemList').appendChild(newItem);
itemInput.value = '';
}
});
```

### 多项选择题

#### 1. 在 JavaScript 中，用于检测按钮点击的事件监听器是什么？

a) `click`

b) `mouseover`

c) `keydown`

d) `load`

**答案：**a) `click`

**解释：**`click`事件监听器用于检测按钮被点击的时刻。

#### 2. 如何使用 JavaScript 更改网页的背景颜色？

a) `document.body.color`

b) `document.body.backgroundColor`

c) `document.body.style.backgroundColor`

d) `document.body.style.color`

**答案：**c) `document.body.style.backgroundColor`

**解释：**要更改背景颜色，需要使用`document.body.style.backgroundColor`。

#### 3. 哪个 CSS 属性用于隐藏 DOM 中的元素？

a) `visibility`

b) `opacity`

c) `display`

d) `hidden`

**答案：**c) `display`

**解释：**`display`属性可以设置为`none`来隐藏元素。

#### 4. 如何使用 JavaScript 创建新的 HTML 元素？

a) `document.createElement()`

b) `document.newElement()`

c) `document.create()`

d) `document.new()`

**答案：**a) `document.createElement()`

**解释：**`document.createElement()`方法用于创建新的 HTML 元素。

#### 5. 在“向列表添加项目”练习中，哪个函数将新项目附加到列表？

a) `append()`

b) `addChild()`

c) `appendChild()`

d) `add()`

**答案：**c) `appendChild()`

**解释：**`appendChild()`方法用于向父节点添加新的子元素。

#### 6. 在“更改背景颜色”练习中，`getRandomColor`函数的目的是什么？

A) 更改文本颜色

B) 生成随机背景颜色

C) 更改字体大小

D) 生成随机字体样式

**答案：**B

**解释：**`getRandomColor`函数生成一个随机颜色代码，用于更改页面的背景颜色。

#### 7. 在“更改背景颜色”练习中，哪个事件监听器用于触发颜色变化？

A) `mouseover`

B) `keydown`

C) `click`

D) `scroll`

**答案：**C

**解释：**`click`事件监听器用于在按钮被点击时触发背景颜色变化。

#### 8. 在“更改背景颜色”练习中，哪个 HTML 元素具有 ID `changeColorButton`？

A) `<body>`

B) `<button>`

C) `<div>`

D) `<span>`

**答案：**B

**解释：**`<button>`元素具有 ID `changeColorButton`。

#### 9. 在`getRandomColor`函数中，表达式`Math.floor(Math.random() * 16)`的作用是什么？

A) 生成 0 到 16 之间的随机数。

B) 生成 0 到 15 之间的随机数。

C) 生成 1 到 16 之间的随机数。

D) 生成 1 到 15 之间的随机数。

**答案：**B

**解释：**`Math.random()`生成 0 到 1 之间的随机数。乘以 16 并使用`Math.floor`将其向下取整为 0 到 15 之间的整数。

#### 10. 在“显示/隐藏文本”练习中，段落的初始 CSS `display`属性值是什么？

A) `block`

B) `inline`

C) `flex`

D) `none`

**答案：**D

**解释：**段落的初始 CSS `display`属性值设置为`none`，使其隐藏。

#### 11. 在“显示/隐藏文本”练习中，切换文本可见性时检查的条件是什么？

A) 如果文本内容为空

B) 如果文本的`display`为`none`

C) 如果按钮被点击

D) 如果文本的`display`为`block`

**答案：**B

**解释：**条件检查文本的`display`属性是否为`none`，以切换其可见性。

#### 12. 在“显示/隐藏文本”练习中，当`toggleTextButton`被点击且文本已经可见时会发生什么？

A) 文本变为斜体

B) 文本被隐藏

C) 文本颜色改变

D) 文本字体大小增加

**答案：**B

**解释：**如果文本已经可见，点击按钮会通过将`display`属性设置为`none`来隐藏文本。

#### 13. 在“向列表添加项目”练习中，当`addItemButton`被点击时会发生什么？

A) 添加一个新段落

B) 添加一个新列表项

C) 输入字段被清空

D) B 和 C 都正确

**答案：**D

**解释：**当按钮被点击时，会添加一个新列表项，并且输入字段被清空。

#### 14. 在“向列表添加项目”练习中，哪个 HTML 元素用于捕获用户的输入？

A) `<input>`

B) `<textarea>`

C) `<div>`

D) `<span>`

**答案：**A

**解释：**`<input>`元素捕获用户的输入。

#### 15. 在“向列表添加项目”练习中，使用什么方法创建新的列表项元素？

A) `document.createElement('li')`

B) `document.createElement('div')`

C) `document.createElement('p')`

D) `document.createElement('span')`

**答案：**A

**解释：**`document.createElement('li')`方法用于创建新的列表项元素。

## 显示当前日期和时间

### 描述

在本练习中，学生将创建一个包含按钮的网页，点击按钮时显示当前日期和时间。本练习介绍如何使用 JavaScript 日期对象以及在网页上显示文本。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 使用 JavaScript Date 对象
- DOM 操作

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Display Date and Time</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<button id="showDateTimeButton">Show Date and Time</button>
<p id="dateTimeDisplay"></p>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
flex-direction: column;
align-items: center;
height: 100vh;
justify-content: center;
margin: 0;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
margin-bottom: 20px;
}
p {
font-size: 18px;
}
```

### JavaScript

```javascript
document.getElementById('showDateTimeButton').addEventListener('click', function() {
const now = new Date();
const dateTimeString = now.toLocaleString();
document.getElementById('dateTimeDisplay').textContent = dateTimeString;
});
```

## 更改文本内容

### 描述

在本练习中，学生将创建一个包含输入字段和按钮的网页。当按钮被点击时，段落中的文本内容会更新为输入字段中输入的文本。本练习介绍如何使用 JavaScript 动态更新文本内容。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Change Text Content</title>
<link rel="stylesheet" href="styles.css">
```

```html
<link rel="stylesheet" href="styles.css">

</head>

<body>

<input type="text" id="textInput" placeholder="Enter new text">

<button id="changeTextButton">Change Text</button>

<p id="textDisplay">This is the original text.</p>

<script src="script.js"></script>

</body>

</html>
```

### CSS



```css
body {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
    justify-content: center;
    margin: 0;
}

input {
    padding: 10px;
    font-size: 16px;
    margin-bottom: 10px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    margin-bottom: 20px;
}

p {
    font-size: 18px;
}
```

JavaScript:

```javascript
document.getElementById('changeTextButton').addEventListener('click', function() {
    const newText = document.getElementById('textInput').value;
    document.getElementById('textDisplay').textContent = newText;
});
```

## 高亮列表项

### 描述

在本练习中，学生将创建一个包含项目列表的网页。当点击某个项目时，其背景颜色会改变以突出显示。本练习介绍了事件委托和动态更新样式。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 事件委托
- DOM 操作（更新样式）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Highlight List Items</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <ul id="itemList">
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
    </ul>
    <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
    justify-content: center;
    margin: 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    font-size: 18px;
    margin: 5px 0;
    padding: 10px;
    cursor: pointer;
}

li.highlight {
    background-color: yellow;
}
```

### JavaScript

```javascript
document.getElementById('itemList').addEventListener('click', function(event) {
    if (event.target.tagName === 'LI') {
        const items = document.querySelectorAll('li');
        items.forEach(item => item.classList.remove('highlight'));
        event.target.classList.add('highlight');
    }
});
```

## 动态图片画廊

### 描述

在本练习中，学生将创建一个简单的图片画廊。当点击缩略图时，将显示该图片的较大版本。本练习介绍了处理点击事件和动态更新图片源。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更改图片源）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Image Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="gallery">
        <img src="thumbnail1.jpg" alt="Thumbnail 1" class="thumbnail">
        <img src="thumbnail2.jpg" alt="Thumbnail 2" class="thumbnail">
        <img src="thumbnail3.jpg" alt="Thumbnail 3" class="thumbnail">
    </div>
    <div id="display">
        <img id="largeImage" src="placeholder.jpg" alt="Large Image">
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
    justify-content: center;
    margin: 0;
}

#gallery {
    display: flex;
    gap: 10px;
}

.thumbnail {
    width: 100px;
    cursor: pointer;
}

#display {
    margin-top: 20px;
}

#largeImage {
    width: 300px;
}
```

### JavaScript

```javascript
document.querySelectorAll('.thumbnail').forEach(thumbnail => {
    thumbnail.addEventListener('click', function() {
        const largeImage = document.getElementById('largeImage');
        largeImage.src = this.src.replace('thumbnail', 'large');
    });
});
```

## 交互式计数器

### 描述

在本练习中，学生将创建一个带有增加和减少计数按钮的交互式计数器。本练习介绍了根据用户输入更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Counter</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="counter">
        <button id="decrementButton">-</button>
        <span id="count">0</span>
        <button id="incrementButton">+</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
    justify-content: center;
    margin: 0;
}

#counter {
    display: flex;
    align-items: center;
    gap: 10px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
}

span {
    font-size: 24px;
    width: 50px;
    text-align: center;
}
```

### JavaScript

```javascript
let count = 0;

document.getElementById('incrementButton').addEventListener('click', function() {
    count++;
    document.getElementById('count').textContent = count;
});

document.getElementById('decrementButton').addEventListener('click', function() {
    count--;
    document.getElementById('count').textContent = count;
});
```

## 表单验证

### 描述

在本练习中，学生将创建一个带有验证功能的简单表单。当点击提交按钮时，脚本将检查所有字段是否已填写，如果任何字段为空，则显示一条警告消息。本练习介绍了基本的表单验证。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 表单验证
- DOM 操作（警告消息）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Validation</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <form id="myForm">
        <input type="text" id="name" placeholder="Name">
        <input type="email" id="email" placeholder="Email">
        <button type="submit">Submit</button>
    </form>
    <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
    justify-content: center;
    margin: 0;
}

form {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

input {
    padding: 10px;
    font-size: 16px;
    width: 200px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
}
```

### JavaScript

```javascript
document.getElementById('myForm').addEventListener('submit', function(event) {
    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    if (name === '' || email === '') {
        event.preventDefault();
        alert('Please fill out all fields.');
    }
});
```

### 多项选择题

#### 动态图片画廊

在动态图片画廊练习中，使用什么方法为每个缩略图添加点击事件监听器？

a) `addEventListener`

b) `attachEvent`

c) `onClick`

d) `addListener`

答案：a) `addEventListener`

解释：`addEventListener`方法用于将事件处理程序附加到指定元素。

如何在 JavaScript 中更改图片元素的源？

a) `element.src`

b) `element.href`

c) `element.link`

d) `element.url`

答案：a) `element.src`

解释：图片元素的`src`属性用于获取或设置要显示的图片的 URL。

#### 交互式计数器

在交互式计数器练习中，使用什么方法更新`span`元素的文本内容？

a) `innerHTML`

b) `textContent`

c) `innerText`

d) `value`

答案：b) `textContent`

解释：`textContent`属性用于设置或返回元素的文本内容。

在 JavaScript 中，哪个事件用于检测表单何时被提交？

a) `click`

b) `submit`

c) `change`

d) `input`

答案：b) `submit`

解释：当表单提交时，会触发`submit`事件。

在表单验证练习中，如果验证失败，如何阻止表单提交？

a) `return false`

b) `event.stop`

c) `event.preventDefault`

d) `event.prevent`

答案：c) `event.preventDefault`

解释：`event.preventDefault`方法用于阻止事件的默认行为被触发。

## 动态图片库

在动态图片库练习中，`forEach`方法的主要用途是什么？

A) 选择具有特定类名的第一个元素

B) 为每个缩略图应用事件监听器

C) 更改所有缩略图的图片源

D) 移除所有缩略图图片

答案：B

解释：`forEach`方法用于为每个缩略图图片应用事件监听器。

在动态图片库练习中，哪个事件触发大图的显示？

A) 鼠标悬停

B) 双击

C) 单击

D) 按键

答案：C

解释：当缩略图被单击时，`click`事件触发大图的显示。

在动态图片库练习中，大图的来源是如何更新的？

A) 通过更改`alt`属性

B) 通过更改`src`属性

C) 通过添加新的图片元素

D) 通过移除旧的图片元素

答案：B

解释：大图元素的`src`属性被更新为所单击缩略图的来源，文件名被修改为指向大图版本。

在动态图片库练习中，缩略图图片具有哪个类名？

A) `gallery`

B) `display`

C) `largeImage`

D) `thumbnail`

答案：D

解释：缩略图图片具有类名`thumbnail`。

## 交互式计数器

在交互式计数器练习中，当点击增加按钮时会发生什么？

A) 计数值减 1

B) 计数值加 1

C) 计数值重置为 0

D) 计数值显示为负数

答案：B

解释：点击增加按钮会使计数值增加 1。

在交互式计数器练习中，当前计数值显示在哪里？

A) 在`<div>`元素中

B) 在`<span>`元素中

C) 在`<p>`元素中

D) 在`<h1>`元素中

答案：B

解释：当前计数值显示在 ID 为`count`的`<span>`元素中。

在交互式计数器练习中，使用哪个 JavaScript 方法来更新计数显示的文本内容？

A) `innerHTML`

B) `value`

C) `textContent`

D) `appendChild`

答案：C

解释：`textContent`属性用于更新计数显示的文本内容。

## 表单验证

在表单验证练习中，使用哪个事件来验证表单？

A) 提交按钮的点击事件

B) 输入字段的按键弹起事件



C) 表单的提交事件

D) 表单的更改事件

答案：C

解释：当点击提交按钮时，表单的`submit`事件用于验证表单。

在表单验证练习中，如果验证失败，哪个方法阻止表单提交？

A) `stopPropagation()`

B) `preventDefault()`

C) `stopImmediatePropagation()`

D) `return false`

答案：B

解释：如果验证失败，`preventDefault()`方法阻止表单提交。

在表单验证练习中，如果任何表单字段为空，会显示什么消息？

A) "表单提交成功"

B) "请填写所有字段。"

C) "无效输入"

D) "提交失败"

答案：B

解释：如果任何表单字段为空，会显示一条警告消息："请填写所有字段。"

哪个 JavaScript 对象用于处理日期和时间？

a) `Time`

b) `Date`

c) `Calendar`

d) `Clock`

答案：b) `Date`

解释：`Date`对象用于在 JavaScript 中处理日期和时间。

如何使用 JavaScript 更新 HTML 元素的文本内容？

a) `element.innerText`

b) `element.textContent`

c) `element.innerHTML`

d) `element.updateText`

答案：b) `element.textContent`

解释：`textContent`属性用于设置或返回元素的文本内容。

什么是事件委托？

a) 一种为多个元素附加单个事件监听器的技术

b) 一种阻止事件传播的方法

c) 一种移除事件监听器的方式

d) 一种更改事件类型的属性

答案：a) 一种为多个元素附加单个事件监听器的技术

解释：事件委托是一种允许你为父元素附加单个事件监听器，以处理多个子元素事件的技术。

在 JavaScript 中，哪个方法用于向元素添加新的 CSS 类？

a) `element.classList.add()`

b) `element.style.add()`

c) `element.addClass()`

d) `element.className.add()`

答案：a) `element.classList.add()`

解释：`classList.add()`方法用于向元素添加新类。

在“高亮列表项”练习中，哪个事件属性用于识别被点击的元素？

a) `event.target`

b) `event.currentTarget`

c) `event.srcElement`

d) `event.element`

答案：a) `event.target`

解释：事件对象的`target`属性指向触发事件的元素。

在“显示当前日期和时间”练习中，`new Date()`构造函数的目的是什么？

A) 格式化字符串

B) 创建一个表示当前日期和时间的新`Date`对象

C) 添加延迟

D) 显示警告

答案：B

解释：`new Date()`构造函数创建一个表示当前日期和时间的新`Date`对象。

在“显示当前日期和时间”练习中，哪个方法用于将`Date`对象转换为可读字符串？

A) `toString()`

B) `toDateString()`

C) `toLocaleString()`

D) `toUTCString()`

答案：C

解释：`toLocaleString()`方法将`Date`对象转换为表示日期和时间的可读格式字符串。

在“显示当前日期和时间”练习中，哪个 HTML 元素用于显示日期和时间？

A) `<div>`

B) `<p>`

C) `<span>`

D) `<h1>`

答案：B

解释：ID 为`dateTimeDisplay`的`<p>`元素用于显示日期和时间。

在“显示当前日期和时间”练习中，什么操作触发当前日期和时间的显示？

A) 鼠标悬停在按钮上

B) 点击按钮

C) 双击按钮

D) 页面加载

答案：B

解释：点击 ID 为`showDateTimeButton`的按钮会触发当前日期和时间的显示。

在“更改文本内容”练习中，当点击`changeTextButton`时会发生什么？

A) 段落中的文本更改为输入值

B) 按钮文本被更改

C) 输入字段被清空

D) 段落被隐藏

答案：A

解释：点击`changeTextButton`会将 ID 为`textDisplay`的段落的文本内容更新为输入字段中输入的值。

在“更改文本内容”练习中，哪个 HTML 元素捕获用户的输入？

A) `<textarea>`

B) `<input>`

C) `<button>`

D) `<div>`

答案：B

解释：ID 为`textInput`的`<input>`元素捕获用户的输入。

在“更改文本内容”练习中，使用哪个方法来更新元素的文本内容？

A) `innerHTML`

B) `innerText`

C) `textContent`

D) `value`

答案：C

解释：`textContent`属性用于更新段落元素的文本内容。

在“高亮列表项”练习中，事件委托的目的是什么？

A) 为每个列表项处理多个事件监听器

B) 处理整个列表上的点击事件

C) 为列表项设置样式

D) 创建新的列表项

答案：B

解释：事件委托用于处理整个列表（`<ul>`元素）上的`click`事件，而不是为每个单独的列表项附加事件监听器。

在“高亮列表项”练习中，当点击列表项时，会添加哪个 CSS 类？

A) `selected`

B) `active`

C) `highlight`

D) `clicked`

答案：C

解释：`highlight`类被添加到被点击的列表项，以更改其背景颜色。

在“高亮列表项”练习中，JavaScript 代码如何确保一次只高亮一个列表项？

A) 它在被点击的项上切换`highlight`类

B) 它将`highlight`类添加到被点击的项

C) 它在将`highlight`类添加到被点击的项之前，先从所有项中移除该类

D) 它改变被点击项的文本颜色

答案：C

解释：代码首先从所有列表项中移除`highlight`类，然后将其添加到被点击的项，以确保一次只高亮一个项。

### 切换深色模式

**描述：**

在本练习中，学生将创建一个带有按钮的网页，该按钮可在浅色和深色模式之间切换。本练习介绍了如何根据用户交互动态更改 CSS 样式。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更改样式）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Toggle Dark Mode</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<button id="toggleButton">Toggle Dark Mode</button>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
background-color: white;
color: black;
transition: background-color 0.3s, color 0.3s;
}

button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}

body.dark-mode {
background-color: black;
color: white;
}
```

**JavaScript：**

```javascript
document.getElementById('toggleButton').addEventListener('click', function() {
document.body.classList.toggle('dark-mode');
});
```

### 过滤列表项

**描述：**

在本练习中，学生将创建一个带有输入字段的网页，用于过滤列表项。当用户在输入字段中键入时，列表将被过滤，仅显示与输入匹配的项。本练习介绍了 DOM 中的过滤和搜索。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（过滤元素）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Filter List Items</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<input type="text" id="filterInput" placeholder="Filter items...">
<ul id="itemList">
<li>Apple</li>
<li>Banana</li>
<li>Cherry</li>
<li>Date</li>
<li>Fig</li>
<li>Grape</li>
</ul>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
flex-direction: column;
align-items: center;
height: 100vh;
justify-content: center;
margin: 0;
}

input {
padding: 10px;
font-size: 16px;
margin-bottom: 10px;
}

ul {
list-style-type: none;
padding: 0;
}

li {
font-size: 18px;
margin: 5px 0;
}
```

**JavaScript：**

```javascript
document.getElementById('filterInput').addEventListener('input', function() {
const filter = this.value.toLowerCase();
const items = document.querySelectorAll('#itemList li');
items.forEach(item => {
if (item.textContent.toLowerCase().includes(filter)) {
item.style.display = '';
} else {
item.style.display = 'none';
}
});
});
```

### 手风琴菜单

**描述：**

在本练习中，学生将创建一个手风琴菜单，点击某个部分的标题可展开或折叠其内容。本练习介绍了使用 JavaScript 创建交互式菜单。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（显示/隐藏元素）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Accordion Menu</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="accordion">
<div class="accordion-item">
<div class="accordion-header">Section 1</div>
<div class="accordion-content">Content for section 1.</div>
</div>
<div class="accordion-item">
<div class="accordion-header">Section 2</div>
<div class="accordion-content">Content for section 2.</div>
</div>
<div class="accordion-item">
<div class="accordion-header">Section 3</div>
<div class="accordion-content">Content for section 3.</div>
</div>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}

.accordion {
width: 300px;
}

.accordion-item {
border: 1px solid #ccc;
border-radius: 5px;
margin-bottom: 10px;
}

.accordion-header {
background-color: #f0f0f0;
padding: 10px;
cursor: pointer;
font-weight: bold;
}

.accordion-content {
display: none;
padding: 10px;
}
```

**JavaScript：**

```javascript
document.querySelectorAll('.accordion-header').forEach(header => {
header.addEventListener('click', function() {
const content = this.nextElementSibling;
if (content.style.display === 'block') {
content.style.display = 'none';
} else {
content.style.display = 'block';
}
});
});
```

## 创建模态弹窗

**描述：**

在本练习中，学生将创建一个模态弹窗，当点击按钮时显示，点击弹窗内的关闭按钮时消失。本练习介绍了创建覆盖层和处理多个事件。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（显示/隐藏元素）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Modal Popup</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<button id="openModalButton">Open Modal</button>
<div id="modal" class="modal">
<div class="modal-content">
<span id="closeModalButton" class="close">&times;</span>
<p>This is a modal popup!</p>
</div>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**



```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

.modal {
  display: none;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 5px;
  width: 300px;
  text-align: center;
}

.close {
  position: absolute;
  top: 10px;
  right: 10px;
  cursor: pointer;
  font-size: 24px;
}
```

## JavaScript

```javascript
document.getElementById('openModalButton').addEventListener('click', function() {
  document.getElementById('modal').style.display = 'flex';
});

document.getElementById('closeModalButton').addEventListener('click', function() {
  document.getElementById('modal').style.display = 'none';
});
```

## 图片轮播

### 描述

在本练习中，学生将创建一个简单的图片轮播，带有“上一张”和“下一张”按钮，用于浏览图片。本练习介绍了如何操作 DOM 以根据用户交互更改显示的内容。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更改图片源）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Carousel</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="carousel">
    <button id="prevButton">&lt;</button>
    <img id="carouselImage" src="image1.jpg" alt="Image Carousel">
    <button id="nextButton">&gt;</button>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.carousel {
  display: flex;
  align-items: center;
  gap: 10px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
```

### JavaScript

```javascript
const images = ['image1.jpg', 'image2.jpg', 'image3.jpg'];
let currentIndex = 0;

document.getElementById('prevButton').addEventListener('click', function() {
  currentIndex = (currentIndex === 0) ? images.length - 1 : currentIndex - 1;
  document.getElementById('carouselImage').src = images[currentIndex];
});

document.getElementById('nextButton').addEventListener('click', function() {
  currentIndex = (currentIndex === images.length - 1) ? 0 : currentIndex + 1;
  document.getElementById('carouselImage').src = images[currentIndex];
});
```

## 倒计时器

### 描述

在本练习中，学生将创建一个倒计时器，从指定的秒数开始倒计时，并在时间到时显示一个警告。本练习介绍了如何在 JavaScript 中使用定时器。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 使用 JavaScript 定时器（`setInterval` 和 `clearInterval`）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Countdown Timer</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <input type="number" id="timeInput" placeholder="Enter seconds">
  <button id="startButton">Start Countdown</button>
  <p id="timerDisplay">0</p>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100vh;
  justify-content: center;
  margin: 0;
}

input {
  padding: 10px;
  font-size: 16px;
  margin-bottom: 10px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  margin-bottom: 20px;
}

p {
  font-size: 24px;
}
```

### JavaScript

```javascript
let timer;
let countdown;

document.getElementById('startButton').addEventListener('click', function() {
  clearInterval(timer);

  const timeInput = document.getElementById('timeInput').value;
  countdown = parseInt(timeInput, 10);

  document.getElementById('timerDisplay').textContent = countdown;

  timer = setInterval(function() {
    countdown--;
    document.getElementById('timerDisplay').textContent = countdown;

    if (countdown <= 0) {
      clearInterval(timer);
      alert('Time is up!');
    }
  }, 1000);
});
```

## 多项选择题

### 基础问题

#### 1. 在 JavaScript 中，用于切换元素上 CSS 类的方法是哪个？

- a) `addClass`
- b) `removeClass`
- c) `toggleClass`
- d) `classList.toggle`

**答案：** d) `classList.toggle`

**解释：** `classList.toggle` 方法用于根据类是否已存在来添加或移除元素上的类。

#### 2. 在“过滤列表项”练习中，哪个事件用于检测输入字段的变化？

- a) `change`
- b) `input`
- c) `keyup`
- d) `keydown`

**答案：** b) `input`

**解释：** 当 `<input>`、`<textarea>` 或 `<select>` 元素的值发生变化时，会触发 `input` 事件。

#### 3. 如何使用 JavaScript 选择 DOM 中的下一个兄弟元素？

- a) `previousElementSibling`
- b) `nextElement`
- c) `nextSibling`
- d) `nextElementSibling`

**答案：** d) `nextElementSibling`

**解释：** `nextElementSibling` 属性返回紧跟在指定元素之后的兄弟元素，如果指定元素没有下一个兄弟元素，则返回 `null`。

#### 4. 在“手风琴菜单”练习中，手风琴内容的初始显示样式是什么？

- a) `block`
- b) `inline`
- c) `none`
- d) `hidden`

**答案：** c) `none`

**解释：** 手风琴内容的初始显示样式设置为 `none`，表示内容默认隐藏。

#### 5. 哪个 CSS 属性常用于在动态更改样式时创建平滑过渡？

- a) `animation`
- b) `transform`
- c) `transition`
- d) `duration`

**答案：** c) `transition`

**解释：** `transition` 属性用于在 CSS 属性值动态变化时创建平滑过渡。

## 切换深色模式

#### 1. 在“切换深色模式”练习中，用于触发深色模式切换的事件监听器是哪个？

- A) `mouseover`
- B) `click`
- C) `dblclick`
- D) `keydown`

**答案：** B

**解释：** 当按钮被点击时，使用 `click` 事件监听器来触发深色模式切换。

#### 2. 在“切换深色模式”练习中，哪个 CSS 类被添加到 body 元素以启用深色模式？

- A) `dark`
- B) `night-mode`
- C) `dark-mode`
- D) `dark-theme`

**答案：** C

**解释：** CSS 类 `dark-mode` 被添加到 body 元素以启用深色模式。

#### 3. 在“切换深色模式”练习中，哪个 CSS 属性被更改以在浅色和深色模式之间切换？

- A) `color`
- B) `background-color`
- C) `font-size`
- D) `margin`

**答案：** B

**解释：** `background-color` 属性被更改以在浅色和深色模式之间切换。

#### 4. 在“切换深色模式”练习中，CSS 中的过渡效果有什么作用？

- A) 它立即改变文本颜色
- B) 它平滑地改变背景和文本颜色
- C) 它增加字体大小
- D) 它在改变颜色之前添加延迟

**答案：** B

**解释：** 过渡效果平滑地改变背景和文本颜色，使浅色和深色模式之间的切换更具视觉吸引力。

## 过滤列表项

#### 1. 在“过滤列表项”练习中，哪个 JavaScript 事件用于触发列表项的过滤？

- A) `click`
- B) `input`
- C) `change`
- D) `mouseover`

**答案：** B

**解释：** 当用户在输入字段中键入时，使用 `input` 事件来触发列表项的过滤。

#### 2. 在“过滤列表项”练习中，哪个方法用于将文本转换为小写以进行比较？

- A) `toUpperCase()`
- B) `toLowerCase()`
- C) `trim()`
- D) `substring()`

**答案：** B

**解释：** `toLowerCase()` 方法用于将文本转换为小写，以实现不区分大小写的比较。

#### 3. 在“过滤列表项”练习中，与过滤输入不匹配的列表项会发生什么？

- A) 它们被删除
- B) 它们的文本颜色改变
- C) 它们被隐藏
- D) 它们被移动到列表底部

**答案：** C

**解释：** 与过滤输入不匹配的列表项通过将其 `display` 属性设置为 `none` 来隐藏。

## 手风琴菜单

#### 1. 在“手风琴菜单”练习中，哪个 CSS 属性用于初始隐藏手风琴内容？

- A) `visibility`
- B) `opacity`
- C) `display`
- D) `overflow`

**答案：** C

**解释：** `display` 属性设置为 `none` 以初始隐藏手风琴内容。

#### 2. 在“手风琴菜单”练习中，哪个事件监听器用于展开或折叠手风琴部分？

- A) `mouseover`
- B) `click`
- C) `dblclick`
- D) `focus`

**答案：** B

**解释：** 当点击标题时，使用 `click` 事件监听器来展开或折叠手风琴部分。

#### 3. 在“手风琴菜单”练习中，JavaScript 代码如何确定要显示或隐藏哪个手风琴内容？

- A) 它使用特定的 ID
- B) 它使用 `nextElementSibling` 属性
- C) 它使用类名
- D) 它使用属性选择器

**答案：** B

**解释：** 使用 `nextElementSibling` 属性来选择点击标题后面的内容元素，以显示或隐藏它。

## 模态弹窗、图片轮播与倒计时器

#### 1. 在“模态弹窗”练习中，哪个方法用于显示模态框？

- a) `display = 'block'`
- b) `display = 'flex'`
- c) `show()`
- d) `visible = true`

**答案：** b) `display = 'flex'`

**解释：** 模态框通过设置 `display = 'flex'` 来显示，以便使用 Flexbox 居中。

#### 2. 在“图片轮播”练习中，哪个方法用于导航到下一张图片？

- a) `nextImage()`
- b) `next()`
- c) `src = nextImage`
- d) `addEventListener`

**答案：** d) `addEventListener`

**解释：** `addEventListener` 方法用于处理导航到下一张图片的点击事件。

#### 3. 在“倒计时器”练习中，哪个函数用于按设定间隔重复执行代码？

- a) `setTimeout`
- b) `setInterval`
- c) `clearInterval`
- d) `setTimer`

**答案：** b) `setInterval`

**解释：** `setInterval` 函数用于按指定间隔重复执行代码。

#### 4. 在倒计时器练习中，如何停止倒计时？

- a) `stop()`
- b) `clearInterval()`
- c) `endTimer()`
- d) `reset()`

**答案：** b) `clearInterval()`

**解释：** `clearInterval` 函数用于停止计时器的继续执行。

#### 5. 在图片轮播练习中，当当前图片的索引超过图片数组的长度时会发生什么？

- a) 轮播停止。
- b) 索引重置为 0。
- c) 索引保持不变。
- d) 抛出错误。

**答案：** b) 索引重置为 0。

**解释：** 当索引超过图片数组的长度时，它会重置为 0，以循环回到第一张图片。

#### 6. 在创建模态弹窗练习中，模态框的初始 CSS display 属性值是什么？

- A) `block`
- B) `none`
- C) `flex`
- D) `inline`

**答案：** B

**解释：** 模态框的初始 CSS display 属性值为 `none`，表示默认隐藏。

#### 7. 在创建模态弹窗练习中，什么事件触发模态框出现？

- A) 鼠标悬停
- B) 点击打开模态框按钮
- C) 双击
- D) 鼠标移出

**答案：** B

**解释：** 点击打开模态框按钮会触发模态框出现。

#### 8. 哪个 CSS 属性使模态框显示在其他元素之上？

- A) `position: absolute`
- B) `z-index: 1`
- C) `visibility: visible`
- D) `position: fixed`

**答案：** D

**解释：** `position: fixed` 属性确保模态框显示在其他元素之上，并相对于视口保持固定位置。

#### 9. 在创建模态弹窗练习中，如何关闭模态框？

- A) 点击模态框外部
- B) 点击模态框内部的关闭按钮
- C) 按下 Escape 键
- D) 双击模态框

**答案：** B

**解释：** 通过点击模态框内部的关闭按钮来关闭模态框。

#### 10. 在图片轮播练习中，使用哪个 JavaScript 数组来存储图片？

- A) `pictures`
- B) `photos`
- C) `slides`
- D) `images`

**答案：** D

**解释：** 数组 `images` 用于存储轮播图片的文件名。

#### 11. 在图片轮播练习中，点击“下一张”按钮时会发生什么？

- A) 显示下一张图片
- B) 显示上一张图片
- C) 轮播停止
- D) 显示第一张图片

**答案：** A

**解释：** 点击“下一张”按钮会显示轮播中的下一张图片。

#### 12. 在图片轮播练习中，点击“上一张”按钮时，当前图片索引如何更新？

- A) 增加 1
- B) 减少 1
- C) 重置为 0



D) 设置为最后一个索引

答案：B

解释：点击“上一张”按钮会将当前图片索引减 1，如果索引为 0，则循环到最后一张图片。

在图片轮播练习中，哪个元素显示当前图片？

A) `<div>`

B) `<span>`

C) `<img>`

D) `<p>`

答案：C

解释：ID 为 `carouselImage` 的 `<img>` 元素显示当前图片。

在倒计时器练习中，使用哪个 JavaScript 函数来重复执行倒计时？

A) `setTimeout`

B) `setInterval`

C) `clearInterval`

D) `requestAnimationFrame`

答案：B

解释：`setInterval` 函数用于每秒重复执行倒计时。

在倒计时器练习中，当倒计时归零时会发生什么？

A) 计时器重置

B) 计时器停止并显示提示

C) 计时器继续倒计时到负数

D) 计时器从初始值重新开始

答案：B

解释：当倒计时归零时，计时器停止并显示提示，表示时间已到。

## 灯箱图片查看器

### 描述

在本练习中，学生将创建一个灯箱图片查看器，点击缩略图时在覆盖层中显示图片。点击图片外部或关闭按钮将关闭灯箱。本练习介绍如何处理多个事件和动态类操作。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（显示/隐藏元素、更改类）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lightbox Image Viewer</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="gallery">
<img src="thumb1.jpg" alt="Thumbnail 1" class="thumbnail">
<img src="thumb2.jpg" alt="Thumbnail 2" class="thumbnail">
<img src="thumb3.jpg" alt="Thumbnail 3" class="thumbnail">
</div>
<div id="lightbox" class="lightbox">
<span id="closeButton" class="close">&times;</span>
<img id="lightboxImage" src="" alt="Large View">
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
height: 100vh;
margin: 0;
}
.gallery {
display: flex;
gap: 10px;
}
.thumbnail {
width: 100px;
cursor: pointer;
}
.lightbox {
display: none;
position: fixed;
top: 0;
left: 0;
width: 100%;
height: 100%;
background-color: rgba(0, 0, 0, 0.8);
justify-content: center;
align-items: center;
z-index: 1000;
}
.lightbox.active {
display: flex;
}
.lightbox img {
max-width: 80%;
max-height: 80%;
}
.close {
position: absolute;
top: 20px;
right: 20px;
font-size: 24px;
cursor: pointer;
color: white;
}
```

### JavaScript

```javascript
document.querySelectorAll('.thumbnail').forEach(thumbnail => {
thumbnail.addEventListener('click', function() {
const lightbox = document.getElementById('lightbox');
const lightboxImage = document.getElementById('lightboxImage');
lightboxImage.src = this.src.replace('thumb', 'large');
lightbox.classList.add('active');
});
});
document.getElementById('closeButton').addEventListener('click', function() {
document.getElementById('lightbox').classList.remove('active');
});
document.getElementById('lightbox').addEventListener('click', function(event) {
if (event.target === this) {
this.classList.remove('active');
}
});
```

## 工具提示悬停效果

### 描述

在本练习中，学生将创建在悬停特定文本元素时出现的工具提示。本练习介绍鼠标事件和创建动态元素。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（创建和定位元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tooltip Hover Effect</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<p>Hover over the <span class="tooltip" data-tooltip="This is a tooltip!">highlighted text</span> to see the tooltip.</p>
<p>Hover over this <span class="tooltip" data-tooltip="Another tooltip!">other text</span> to see another tooltip.</p>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
margin: 50px;
}
.tooltip {
position: relative;
cursor: pointer;
color: blue;
text-decoration: underline;
}
.tooltip .tooltiptext {
visibility: hidden;
width: 120px;
background-color: black;
color: white;
text-align: center;
border-radius: 5px;
padding: 5px;
position: absolute;
z-index: 1;
bottom: 125%; /* Position the tooltip above the text */
left: 50%;
margin-left: -60px;
opacity: 0;
transition: opacity 0.3s;
}
.tooltip:hover .tooltiptext {
visibility: visible;
opacity: 1;
}
```

### JavaScript

```javascript
document.querySelectorAll('.tooltip').forEach(item => {
item.addEventListener('mouseenter', function() {
const tooltipText = document.createElement('div');
tooltipText.className = 'tooltiptext';
tooltipText.innerHTML = this.getAttribute('data-tooltip');
this.appendChild(tooltipText);
});
item.addEventListener('mouseleave', function() {
const tooltipText = this.querySelector('.tooltiptext');
```

```javascript
if (tooltipText) {
  tooltipText.remove();
}
```

## 可折叠区域

### 描述

在本练习中，学生将创建可折叠区域，点击标题时展开或折叠。本练习介绍如何切换可见性和动态更改样式。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（切换可见性）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Collapsible Sections</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="collapsible">
    <div class="collapsible-header">Section 1</div>
    <div class="collapsible-content">Content for section 1.</div>
  </div>
  <div class="collapsible">
    <div class="collapsible-header">Section 2</div>
    <div class="collapsible-content">Content for section 2.</div>
  </div>
  <div class="collapsible">
    <div class="collapsible-header">Section 3</div>
    <div class="collapsible-content">Content for section 3.</div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  margin: 20px;
}
.collapsible {
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
.collapsible-header {
  background-color: #f0f0f0;
  padding: 10px;
  cursor: pointer;
  font-weight: bold;
}
.collapsible-content {
  display: none;
  padding: 10px;
}
```

### JavaScript

```javascript
document.querySelectorAll('.collapsible-header').forEach(header => {
  header.addEventListener('click', function() {
    const content = this.nextElementSibling;
    if (content.style.display === 'block') {
      content.style.display = 'none';
    } else {
      content.style.display = 'block';
    }
  });
});
```

## 拖拽排序列表

### 描述

在本练习中，学生将创建一个拖拽排序列表，通过拖放来重新排列项目。本练习介绍拖放事件和动态更新 DOM。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 拖放事件
- DOM 操作（重新排列元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Drag and Drop List</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <ul id="draggableList">
    <li draggable="true">Item 1</li>
    <li draggable="true">Item 2</li>
    <li draggable="true">Item 3</li>
    <li draggable="true">Item 4</li>
    <li draggable="true">Item 5</li>
  </ul>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
ul {
  list-style-type: none;
  padding: 0;
  width: 200px;
}
li {
  padding: 10px;
  margin: 5px 0;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  cursor: move;
}
```

### JavaScript

```javascript
const list = document.getElementById('draggableList');
let draggedItem = null;

list.addEventListener('dragstart', function(event) {
  draggedItem = event.target;
  event.target.style.opacity = 0.5;
});

list.addEventListener('dragend', function(event) {
  event.target.style.opacity = '';
});

list.addEventListener('dragover', function(event) {
  event.preventDefault();
});

list.addEventListener('dragenter', function(event) {
  if (event.target.tagName === 'LI') {
    event.target.style.borderTop = '2px solid #000';
  }
});

list.addEventListener('dragleave', function(event) {
  if (event.target.tagName === 'LI') {
    event.target.style.borderTop = '';
  }
});

list.addEventListener('drop', function(event) {
  event.preventDefault();
  if (event.target.tagName === 'LI') {
    event.target.style.borderTop = '';
    list.insertBefore(draggedItem, event.target);
  }
});
```

## 简易计算器

### 描述

在本练习中，学生将创建一个简易计算器，能够执行基本的算术运算（加、减、乘、除）。本练习介绍如何处理表单输入并使用 JavaScript 进行计算。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算

### HTML



```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" disabled>
    <div class="buttons">
      <button class="number">7</button>
      <button class="number">8</button>
      <button class="number">9</button>
      <button class="operator">/</button>
      <button class="number">4</button>
      <button class="number">5</button>
      <button class="number">6</button>
      <button class="operator">*</button>
      <button class="number">1</button>
      <button class="number">2</button>
      <button class="number">3</button>
      <button class="operator">-</button>
      <button class="number">0</button>
      <button id="clear">C</button>
      <button id="equals">=</button>
      <button class="operator">+</button>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.calculator {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid #ccc;
  border-radius: 10px;
  padding: 20px;
  background-color: #f9f9f9;
}

#display {
  width: 200px;
  padding: 10px;
  margin-bottom: 10px;
  font-size: 18px;
  text-align: right;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 50px);
  gap: 10px;
}

button {
  width: 50px;
  height: 50px;
  font-size: 18px;
  cursor: pointer;
}
```

## JavaScript

```javascript
let display = document.getElementById('display');
let buttons = Array.from(document.getElementsByClassName('number'));
let operators = Array.from(document.getElementsByClassName('operator'));
let clear = document.getElementById('clear');
let equals = document.getElementById('equals');
let currentOperator = null;
let firstOperand = null;
let secondOperand = null;

buttons.forEach(button => {
  button.addEventListener('click', function() {
    display.value += this.textContent;
  });
});

operators.forEach(operator => {
  operator.addEventListener('click', function() {
    if (display.value) {
      firstOperand = parseFloat(display.value);
      currentOperator = this.textContent;
      display.value = '';
    }
  });
});

clear.addEventListener('click', function() {
  display.value = '';
  firstOperand = null;
  secondOperand = null;
  currentOperator = null;
});

equals.addEventListener('click', function() {
  if (display.value) {
    secondOperand = parseFloat(display.value);
    switch (currentOperator) {
      case '+':
        display.value = firstOperand + secondOperand;
        break;
      case '-':
        display.value = firstOperand - secondOperand;
        break;
      case '*':
        display.value = firstOperand * secondOperand;
        break;
      case '/':
        display.value = firstOperand / secondOperand;
        break;
    }
    firstOperand = null;
    secondOperand = null;
    currentOperator = null;
  }
});
```

## 标签页导航

### 描述

在本练习中，学生将创建一个标签页导航界面，点击标签时显示对应内容并隐藏其他内容。本练习介绍如何使用 JavaScript 在内容区域之间切换。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（显示/隐藏元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tabs Navigation</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="tabs">
    <button class="tab-button active" data-tab="tab1">Tab 1</button>
    <button class="tab-button" data-tab="tab2">Tab 2</button>
    <button class="tab-button" data-tab="tab3">Tab 3</button>
  </div>

  <div class="tab-content" id="tab1">Content for Tab 1</div>
  <div class="tab-content" id="tab2">Content for Tab 2</div>
  <div class="tab-content" id="tab3">Content for Tab 3</div>

  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  margin: 20px;
}

.tabs {
  display: flex;
  gap: 10px;
}

.tab-button {
  padding: 10px 20px;
  cursor: pointer;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.tab-button.active {
  background-color: #ccc;
}

.tab-content {
  display: none;
  margin-top: 20px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #f9f9f9;
}

.tab-content.active {
  display: block;
}
```

### JavaScript

```javascript
document.querySelectorAll('.tab-button').forEach(button => {
  button.addEventListener('click', function() {
    document.querySelectorAll('.tab-button').forEach(btn => btn.classList.remove('active'));
    document.querySelectorAll('.tab-content').forEach(content => content.classList.remove('active'));
    this.classList.add('active');
    document.getElementById(this.getAttribute('data-tab')).classList.add('active');
  });
});
```

## 随机名言生成器

### 描述

在本练习中，学生将创建一个随机名言生成器，每次点击按钮时显示一条新名言。本练习介绍如何使用数组和随机选择元素。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 数组
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Random Quote Generator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="quote-box">
    <p id="quoteDisplay">Click the button to see a random quote.</p>
    <button id="newQuoteButton">New Quote</button>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.quote-box {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
```

### JavaScript

```javascript
const quotes = [
  "The best way to predict the future is to invent it.",
  "Life is 10% what happens to us and 90% how we react to it.",
  "The only limit to our realization of tomorrow is our doubts of today.",
  "Do not watch the clock. Do what it does. Keep going.",
  "Keep your face always toward the sunshine—and shadows will fall behind you."
];

document.getElementById('newQuoteButton').addEventListener('click', function() {
  const randomIndex = Math.floor(Math.random() * quotes.length);
  document.getElementById('quoteDisplay').textContent = quotes[randomIndex];
});
```

## 实时字符计数器

### 描述

在本练习中，学生将创建一个实时字符计数器，当用户在文本区域输入时自动更新。本练习介绍如何使用输入事件和动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Real-time Character Counter</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="counter-box">
    <textarea id="textInput" placeholder="Type something..."></textarea>
    <p id="charCount">Characters: 0</p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.counter-box {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

textarea {
  width: 100%;
  height: 100px;
  padding: 10px;
  font-size: 16px;
  margin-bottom: 10px;
}

p {
  font-size: 18px;
  margin: 0;
}
```

### JavaScript

```javascript
document.getElementById('textInput').addEventListener('input', function() {
  const charCount = this.value.length;
  document.getElementById('charCount').textContent = `Characters: ${charCount}`;
});
```



### 多项选择题

在灯箱图片查看器练习中，哪种方法用于在点击图片外部时关闭灯箱？

a) `event.stopPropagation`

b) `event.preventDefault`

c) `event.target`

d) `event.currentTarget`

答案：c) `event.target`

解释：`event.target` 属性用于判断点击是否发生在图片外部，从而关闭灯箱。

在工具提示悬停效果练习中，使用哪个 CSS 属性来创建平滑的过渡效果？

a) `transform`

b) `animation`

c) `transition`

d) `visibility`

答案：c) `transition`

解释：`transition` 属性用于创建工具提示可见性和不透明度的平滑过渡效果。

在工具提示悬停效果练习中，如何将工具提示文本动态添加到元素中？

a) 使用 `innerHTML`

b) 使用 `textContent`

c) 使用 `createElement` 和 `appendChild`

d) 使用 `insertAdjacentHTML`

答案：c) 使用 `createElement` 和 `appendChild`

解释：工具提示文本通过 `createElement` 和 `appendChild` 方法动态创建并添加。

如何在 JavaScript 中切换元素的可见性？

a) `style.visibility`

b) `style.display`

c) `classList.toggle`

d) 以上全部

答案：d) 以上全部

解释：根据所需效果，可以使用 `style.visibility`、`style.display` 或 `classList.toggle` 来切换可见性。

在可折叠区域练习中，切换哪个 CSS 属性来显示或隐藏内容？

a) `visibility`

b) `opacity`

c) `display`

d) `height`

答案：c) `display`

解释：`display` 属性在 `block` 和 `none` 之间切换，以显示或隐藏可折叠内容。

在拖放列表练习中，哪个 HTML 属性使元素可拖动？

a) `draggable`

b) `movable`

c) `sortable`

d) `dropzone`

答案：a) `draggable`

解释：`draggable` 属性用于指定元素可拖动。

在拖放列表练习中，当可拖动元素被放下时触发哪个事件？

a) `dragend`

b) `dragstart`

c) `drop`

d) `dragenter`

答案：c) `drop`

解释：当可拖动元素被放下时触发 `drop` 事件。

在简单计算器练习中，使用什么方法将按钮的值添加到显示屏？

a) `innerHTML`

b) `textContent`

c) `value`

d) `appendChild`

答案：c) `value`

解释：使用 `value` 属性将按钮的值添加到显示屏。

在简单计算器练习中，如何清除显示屏？

a) `display.clear()`

b) `display.value = ''`

c) `display.reset()`

d) `display.textContent = ''`

答案：b) `display.value = ''`

解释：通过将 `value` 属性设置为空字符串来清除显示屏。

在标签页导航练习中，如何显示当前激活的标签页内容？

a) `style.display = 'block'`

b) `classList.add('active')`

c) `innerHTML`

d) `textContent`

答案：b) `classList.add('active')`

解释：通过使用 `classList.add('active')` 添加 `active` 类来显示当前激活的标签页内容。

在随机名言生成器练习中，使用什么方法从数组中随机选择一条名言？

a) `Math.random()`

b) `Math.floor()`

c) `Array.prototype.random()`

d) `Math.ceil()`

答案：a) `Math.random()`

解释：使用 `Math.random()` 方法生成随机数，并使用 `Math.floor()` 将其转换为数组索引范围内的整数。

在实时字符计数器练习中，使用什么事件来更新字符计数？

a) `change`

b) `input`

c) `keydown`

d) `keyup`

答案：b) `input`

解释：`input` 事件在每次 `input` 或 `textarea` 的值发生变化时触发，非常适合实时更新。

在实时字符计数器练习中，字符计数是如何显示给用户的？

a) `innerHTML`

b) `textContent`

c) `value`

d) `appendChild`

答案：b) `textContent`

解释：`textContent` 属性用于更新段落元素中显示的字符计数。

在灯箱图片查看器练习中，灯箱的初始显示属性是什么？

A) `block`

B) `none`

C) `flex`

D) `inline`

答案：B

解释：灯箱的初始显示属性是 `none`，表示默认隐藏。

在灯箱图片查看器练习中，点击缩略图时会发生什么？

A) 灯箱显示变为 `block`

B) 灯箱显示变为 `none`

C) 灯箱变为隐藏

D) 灯箱显示变为 `flex` 并且图片源被更新

答案：D

解释：点击缩略图时，灯箱显示变为 `flex`，并且图片源被更新为显示大图版本。

在灯箱图片查看器练习中，点击图片外部时如何关闭灯箱？

A) 仅通过点击关闭按钮

B) 点击灯箱内部任意位置

C) 点击图片

D) 点击图片外部但仍在灯箱内部

答案：D

解释：点击图片外部但仍在灯箱内部会移除 `active` 类，从而隐藏灯箱。

在灯箱图片查看器练习中，哪个类被添加到灯箱以使其可见？

A) `show`

B) `visible`

C) `active`

D) `open`

答案：C

解释：`active` 类被添加到灯箱以使其可见。

在工具提示悬停效果练习中，什么事件触发工具提示出现？

A) `click`

B) `hover`

C) `mouseenter`

D) `mouseleave`

答案：C

解释：当用户将鼠标悬停在文本上时，`mouseenter` 事件触发工具提示出现。

在工具提示悬停效果练习中，使用什么方法创建工具提示元素？

A) `innerHTML`

B) `createElement`

C) `appendChild`

D) `textContent`

答案：B

解释：使用 `createElement` 方法创建工具提示元素。

在工具提示悬停效果练习中，当鼠标离开文本时如何移除工具提示？

A) 将 `innerHTML` 设置为空字符串

B) 使用 `removeChild`

C) 使用 `remove`

D) 将 `display` 设置为 `none`

答案：C

解释：通过对工具提示元素使用 `remove` 方法来移除工具提示。

在可折叠区域练习中，使用什么事件来切换可折叠区域的可见性？

A) `click`

B) `mouseover`

C) `dblclick`

D) `keydown`

答案：A

解释：使用 `click` 事件来切换可折叠区域的可见性。

在可折叠区域练习中，如何切换可折叠内容的可见性？

A) 通过添加/移除 `active` 类

B) 通过将 `display` 属性在 `block` 和 `none` 之间切换

C) 将 `visibility` 设置为 `hidden`

D) 改变 `opacity`

答案：B

解释：通过将 `display` 属性在 `block` 和 `none` 之间切换来切换可见性。

在拖放列表练习中，哪个事件用于开始拖拽项目？

A) `drag`

B) `dragstart`

C) `dragenter`

D) `dragend`

答案：B

解释：`dragstart` 事件用于开始拖拽项目。

在拖放列表练习中，如何标识正在被拖拽的项目？

A) 通过设置 `dataTransfer`

B) 通过改变类

C) 通过存储对被拖拽项目的引用

D) 通过改变 `id`

答案：C

解释：通过将正在被拖拽的项目引用存储在一个变量中来标识它。

在拖放列表练习中，`dragover` 事件的目的是什么？

A) 高亮放置目标

B) 更新被拖拽项目的位置

C) 阻止事件的默认处理并允许放置

D) 更新光标样式

答案：C

解释：`dragover` 事件阻止事件的默认处理并允许项目被放置。

在简单计算器练习中，哪个事件用于处理按钮点击？

A) `submit`

B) `input`

C) `click`

D) `dblclick`

答案：C

解释：使用 `click` 事件来处理按钮点击。

在简单计算器练习中，点击等号按钮时如何执行计算？

A) 使用 `eval` 函数

B) 使用一系列 `if` 语句

C) 使用 `switch` 语句

D) 使用正则表达式

答案：C

解释：使用 `switch` 语句来处理不同的运算符，从而执行计算。

在标签导航练习中，哪个事件用于切换标签？

A) `mouseover`

B) `dblclick`

C) `click`

D) `mouseenter`

答案：C

解释：使用 `click` 事件来切换标签。

在标签导航练习中，如何识别并显示当前活动标签的内容？

A) 通过改变标签内容的 `display` 属性

B) 通过添加/移除 `active` 类

C) 使用 `visibility` 属性

D) 改变 `opacity`

答案：B

解释：通过添加/移除 `active` 类来识别并显示当前活动标签的内容。

在随机名言生成器练习中，名言是如何存储的？

A) 在字符串中

B) 在对象中

C) 在数组中

D) 在 JSON 文件中

答案：C

解释：名言存储在一个数组中。

在随机名言生成器练习中，使用什么方法选择随机名言？

A) `Math.random()`

B) `Math.floor()`

C) A 和 B 都使用

D) `Array.prototype.random`

答案：C

解释：同时使用 `Math.random()` 和 `Math.floor()` 从数组中选取随机名言。

在实时字符计数器练习中，哪个事件用于更新字符计数？

A) `keypress`

B) `keydown`

C) `keyup`

D) `input`

答案：D

解释：使用 `input` 事件在用户输入时更新字符计数。

在实时字符计数器练习中，字符计数是如何显示的？

A) 通过更新段落元素的 `innerHTML`

B) 通过更新段落元素的 `textContent`

C) 通过更新输入元素的 `value`

D) 通过更新文本区域的 `placeholder`

答案：B

解释：通过更新段落元素的 `textContent` 来显示字符计数。

## 简单待办事项列表

### 描述

在本练习中，学生将创建一个简单的待办事项列表，可以添加新任务并将其标记为已完成。本练习介绍了表单处理、动态向 DOM 添加元素以及更新样式。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（添加和更新元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simple To-Do List</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="todo-container">
<h1>To-Do List</h1>
<form id="todoForm">
<input type="text" id="taskInput" placeholder="Enter a new task">
<button type="submit">Add Task</button>
</form>
<ul id="taskList"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.todo-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 10px;
margin: 5px 0;
background-color: #fff;
border: 1px solid #ccc;
border-radius: 5px;
cursor: pointer;
}
li.completed {
text-decoration: line-through;
color: grey;
}
```

### JavaScript

```javascript
document.getElementById('todoForm').addEventListener('submit', function(event) {
event.preventDefault();
const taskInput = document.getElementById('taskInput');
```

```javascript
const taskText = taskInput.value;

if (taskText === '') return;

const li = document.createElement('li');

li.textContent = taskText;

li.addEventListener('click', function() {

li.classList.toggle('completed');

});

document.getElementById('taskList').appendChild(li);

taskInput.value = '';

});
```

## 图片轮播

### 描述

在本练习中，学生将创建一个每隔几秒自动切换图片的图片轮播。本练习介绍如何使用定时器以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更改图片源）
- 定时器的使用

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Image Slider</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="slider">
<img id="sliderImage" src="image1.jpg" alt="Image Slider">
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.slider {
width: 80%;
max-width: 600px;
overflow: hidden;
position: relative;
}
.slider img {
width: 100%;
display: block;
}
```

### JavaScript

```javascript
const images = ['image1.jpg', 'image2.jpg', 'image3.jpg'];
let currentIndex = 0;
function showNextImage() {
currentIndex = (currentIndex + 1) % images.length;
document.getElementById('sliderImage').src = images[currentIndex];
}
setInterval(showNextImage, 3000); // 每 3 秒切换图片
```

## 交互式常见问题解答

### 描述

在本练习中，学生将创建一个交互式常见问题解答（FAQ）区域，点击问题即可显示答案。本练习介绍如何切换可见性以及动态更新样式。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（切换可见性）

### HTML



```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive FAQ</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="faq-container">
<div class="faq-item">
<div class="faq-question">What is your return policy?</div>
<div class="faq-answer">Our return policy is 30 days with a receipt.</div>
</div>
<div class="faq-item">
<div class="faq-question">Do you offer international shipping?</div>
<div class="faq-answer">Yes, we offer shipping to over 50 countries.</div>
</div>
<div class="faq-item">
<div class="faq-question">How can I track my order?</div>
<div class="faq-answer">You can track your order using the tracking number provided in the confirmation email.</div>
</div>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.faq-container {
width: 80%;
max-width: 600px;
}
.faq-item {
border: 1px solid #ccc;
border-radius: 5px;
margin-bottom: 10px;
}
.faq-question {
padding: 10px;
background-color: #f0f0f0;
cursor: pointer;
}
.faq-answer {
display: none;
padding: 10px;
background-color: #fff;
}
```

### JavaScript

```javascript
document.querySelectorAll('.faq-question').forEach(question => {
question.addEventListener('click', function() {
const answer = this.nextElementSibling;
if (answer.style.display === 'block') {
answer.style.display = 'none';
} else {
answer.style.display = 'block';
}
});
});
```

## 货币转换器

### 描述

在本练习中，学生将创建一个货币转换器，根据预定义的汇率将金额从一种货币转换为另一种货币。本练习介绍如何使用表单、处理用户输入以及执行计算。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Currency Converter</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="converter">
<h1>Currency Converter</h1>
<form id="converterForm">
<input type="number" id="amountInput" placeholder="Enter amount" required>
<select id="currencySelect">
<option value="EUR">USD to EUR</option>
<option value="GBP">USD to GBP</option>
<option value="JPY">USD to JPY</option>
</select>
<button type="submit">Convert</button>
</form>
<p id="resultDisplay"></p>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.converter {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
display: flex;
flex-direction: column;
gap: 10px;
}
input, select, button {
padding: 10px;
font-size: 16px;
}
```

### JavaScript

```javascript
const exchangeRates = {
EUR: 0.85,
GBP: 0.75,
JPY: 110.00
};
document.getElementById('converterForm').addEventListener('submit', function(event) {
event.preventDefault();
const amount = parseFloat(document.getElementById('amountInput').value);
const currency = document.getElementById('currencySelect').value;
const rate = exchangeRates[currency];
const convertedAmount = (amount * rate).toFixed(2);
document.getElementById('resultDisplay').textContent = `Converted Amount: ${convertedAmount} ${currency}`;
});
```

## 石头剪刀布游戏

### 描述

在本练习中，学生将创建一个简单的石头剪刀布游戏，用户可以与电脑对战。本练习介绍如何处理用户输入、生成随机选择以及实现游戏逻辑。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理用户输入
- 实现游戏逻辑

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rock, Paper, Scissors Game</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="game-container">
<h1>Rock, Paper, Scissors</h1>
<div class="choices">
<button class="choice" data-choice="rock">Rock</button>
<button class="choice" data-choice="paper">Paper</button>
<button class="choice" data-choice="scissors">Scissors</button>
</div>
<p id="resultDisplay"></p>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.game-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
.choices {
display: flex;
justify-content: center;
gap: 10px;
margin-bottom: 20px;
}
button.choice {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
```

### JavaScript

```javascript
const choices = ['rock', 'paper', 'scissors'];
document.querySelectorAll('.choice').forEach(button => {
button.addEventListener('click', function() {
const userChoice = this.getAttribute('data-choice');
const computerChoice = choices[Math.floor(Math.random() * choices.length)];
let result = '';
if (userChoice === computerChoice) {
result = 'It\'s a tie!';
} else if (
(userChoice === 'rock' && computerChoice === 'scissors') ||
(userChoice === 'paper' && computerChoice === 'rock') ||
(userChoice === 'scissors' && computerChoice === 'paper')
) {
result = 'You win!';
} else {
result = 'You lose!';
}
document.getElementById('resultDisplay').textContent = `You chose ${userChoice}. Computer chose ${computerChoice}. ${result}`;
});
});
```

## 带暂停和重置功能的倒计时器

### 描述

在本练习中，学生将创建一个可以暂停和重置的倒计时器。本练习介绍了如何使用定时器、控制其执行以及动态更新 DOM。

### 涵盖的主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 使用定时器
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Countdown Timer</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="timer-container">
<h1>Countdown Timer</h1>
<input type="number" id="timeInput" placeholder="Enter seconds" required>
<div class="buttons">
<button id="startButton">Start</button>
<button id="pauseButton">Pause</button>
<button id="resetButton">Reset</button>
</div>
<p id="timerDisplay">0</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.timer-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
input {
padding: 10px;
font-size: 16px;
margin-bottom: 10px;
}
.buttons {
display: flex;
justify-content: center;
gap: 10px;
margin-bottom: 20px;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
p {
font-size: 24px;
margin: 0;
}
```

### JavaScript

```javascript
let timer;
let countdown;
let isPaused = false;

document.getElementById('startButton').addEventListener('click', function() {
if (!isPaused) {
clearInterval(timer);
const timeInput = parseInt(document.getElementById('timeInput').value, 10);
countdown = timeInput;
}
isPaused = false;
document.getElementById('timerDisplay').textContent = countdown;
timer = setInterval(function() {
if (!isPaused) {
countdown--;
document.getElementById('timerDisplay').textContent = countdown;
if (countdown <= 0) {
clearInterval(timer);
alert('Time is up!');
}
}
}, 1000);
});

document.getElementById('pauseButton').addEventListener('click', function() {
isPaused = true;
});

document.getElementById('resetButton').addEventListener('click', function() {
clearInterval(timer);
countdown = 0;
document.getElementById('timerDisplay').textContent = countdown;
isPaused = false;
});
```

### 多项选择题

#### 1. 在简单待办事项列表练习中，哪个事件用于处理表单提交？

a) `click`

b) `submit`

c) `change`

d) `input`

**答案：** b) `submit`

**解释：** `submit` 事件用于在向待办事项列表添加新任务时处理表单提交。

#### 2. 在简单待办事项列表练习中，使用什么方法来切换任务的 `completed` 类？

a) `classList.add`

b) `classList.remove`

c) `classList.toggle`

d) `classList.change`

**答案：** c) `classList.toggle`

**解释：** `classList.toggle` 方法用于在点击任务时添加或移除 `completed` 类。

#### 3. 在图片轮播练习中，图片多久更换一次？

a) 每秒

b) 每 2 秒

c) 每 3 秒

d) 每 5 秒



答案：c) 每 3 秒

解释：`setInterval` 函数用于每 3 秒更换一次图片。

## 交互式常见问题解答

### 1. 如何显示或隐藏答案？

a) 通过更改 `innerHTML`

b) 通过更改 `textContent`

c) 通过切换 `display` 属性

d) 通过使用 `visibility` 属性

答案：c) 通过切换 `display` 属性

解释：`display` 属性在 `block` 和 `none` 之间切换，以显示或隐藏常见问题解答的答案。

### 2. 常见问题解答答案的初始 `display` 属性是什么？

a) `block`

b) `inline`

c) `none`

d) `hidden`

答案：c) `none`

解释：常见问题解答答案的初始 `display` 属性设置为 `none`，表示默认隐藏。

### 3. 哪个事件用于切换答案的可见性？

A) `mouseover`

B) `click`

C) `dblclick`

D) `mouseenter`

答案：B

解释：`click` 事件用于在点击问题时切换答案的可见性。

### 4. 更改哪个 CSS 属性以显示或隐藏答案？

A) `visibility`

B) `opacity`

C) `display`

D) `height`

答案：C

解释：`display` 属性在 `none` 和 `block` 之间切换，以显示或隐藏答案。

### 5. 每个常见问题项中的答案包含在哪个 HTML 元素中？

A) `<p>`

B) `<div>`

C) `<span>`

D) `<section>`

答案：B

解释：答案包含在问题 `<div>` 之后的 `<div>` 元素中。

### 6. 用户如何显示问题的答案？

A) 通过悬停在问题上

B) 通过点击问题

C) 通过双击问题

D) 通过右键点击问题

答案：B

解释：用户通过点击问题来显示答案。

## 货币转换器

### 1. 如何显示转换后的金额？

a) 使用 `innerHTML`

b) 使用 `textContent`

c) 使用 `value`

d) 使用 `appendChild`

答案：b) 使用 `textContent`

解释：`textContent` 属性用于在结果显示元素中显示转换后的金额。

### 2. 使用哪个事件监听器来处理表单提交？

A) `input`

B) `change`

C) `submit`

D) `click`

答案：C

解释：使用 `submit` 事件监听器来处理表单提交。

### 3. 如何计算转换后的金额？

A) 使用预定义的汇率

B) 使用用户输入的汇率

C) 通过从 API 获取实时汇率

D) 硬编码结果

答案：A

解释：转换后的金额使用存储在对象中的预定义汇率进行计算。

## 石头剪刀布游戏

### 1. 使用什么方法为计算机生成随机选择？

a) `Math.random()`

b) `Math.floor()`

c) `Array.prototype.random()`

d) `Math.ceil()`

答案：a) `Math.random()`

解释：`Math.random()` 方法用于生成一个随机数，然后用于为计算机选择随机选项。

### 2. 什么决定用户是否获胜？

a) 用户的选择与计算机的选择相同

b) 用户的选择击败了计算机的选择

c) 计算机的选择与用户的选择相同

d) 计算机的选择击败了用户的选择

答案：b) 用户的选择击败了计算机的选择

解释：根据石头剪刀布的规则，如果用户的选择击败了计算机的选择，则用户获胜。

### 3. 如何确定电脑的选择？

A) 通过用户输入

B) 通过预定义的顺序

C) 从数组中随机选择

D) 总是选择石头

答案：C

解释：电脑的选择是通过从选项数组中随机选择来确定的。

### 4. 什么事件触发游戏逻辑？

A) `hover`

B) `click`

C) `keydown`

D) `submit`

答案：B

解释：当用户点击他们的选择时，`click` 事件触发游戏逻辑。

## 倒计时器

### 1. 哪个函数用于重复执行倒计时逻辑？

a) `setTimeout`

b) `setInterval`

c) `clearInterval`

d) `setTimer`

答案：b) `setInterval`

解释：`setInterval` 函数用于每隔一秒重复执行倒计时逻辑。

### 2. 如何暂停计时器？

a) 通过清除间隔

b) 通过设置暂停标志

c) 通过重置计时器

d) 通过使用 `pause()` 方法

答案：b) 通过设置暂停标志

解释：通过将 `isPaused` 标志设置为 `true` 来暂停计时器，这会停止倒计时而不清除间隔。

### 3. 哪个函数用于重复更新倒计时？

A) `setTimeout`

B) `setInterval`

C) `clearTimeout`

D) `requestAnimationFrame`

答案：B

解释：使用 `setInterval` 函数重复更新倒计时。

### 4. 如何暂停计时器？

A) 通过清除间隔

B) 通过设置标志变量

C) 通过重置倒计时值

D) 通过禁用开始按钮

答案：B

解释：通过将标志变量（`isPaused`）设置为 `true` 来暂停计时器。

### 5. 点击重置按钮会发生什么？

A) 倒计时继续

B) 倒计时归零

C) 倒计时暂停

D) 倒计时从初始输入值重新开始

答案：B

解释：点击重置按钮会将倒计时归零并停止计时器。

## 简单待办事项列表

### 1. 哪个事件阻止了默认的表单提交？

A) `click`

B) `submit`

C) `load`

D) `input`

答案：B

解释：`submit` 事件用于在添加新任务时阻止默认的表单提交。

### 2. 点击任务时会发生什么？

A) 任务被删除

B) 任务被编辑

C) 通过切换类，任务被标记为已完成

D) 任务被移动到列表顶部

答案：C

解释：点击任务会切换 `completed` 类，将其标记为已完成或未完成。

### 3. 哪个 HTML 元素用于显示任务列表？

A) `<div>`

B) `<ol>`

C) `<ul>`

D) `<section>`

答案：C

解释：`<ul>` 元素用于显示任务列表。

### 4. 哪个 HTML 元素用于提交新任务？

A) `<button>`

B) `<input>`

C) `<form>`

D) `<div>`

答案：C

解释：使用 `<form>` 元素提交新任务。

### 5. 使用什么属性确保任务输入字段不为空？

A) `required`

B) `placeholder`

C) `maxlength`

D) `pattern`

答案：A

解释：使用 `required` 属性确保在提交前任务输入字段不为空。

## 图片轮播

### 1. 哪个函数用于每隔几秒更换图片？

A) `setTimeout`

B) `clearInterval`

C) `setInterval`

D) `requestAnimationFrame`

答案：C

解释：`setInterval` 函数用于每 3 秒更换一次图片。

### 2. 如何显示数组中的下一张图片？

A) 通过递增当前索引

B) 通过递减当前索引

C) 通过随机选择

D) 通过反向遍历数组

答案：A

解释：递增当前索引以显示数组中的下一张图片。

### 3. 哪个事件监听器用于启动图片轮播？

A) `click`

B) `load`

C) `mouseover`

D) `resize`

答案：B

解释：`load` 事件监听器被隐式使用，因为 `setInterval` 函数在页面加载后自动运行。

### 4. 图片多久变化一次？

A) 每秒

B) 每 2 秒

C) 每 3 秒

D) 每 5 秒

答案：C

解释：图片每 3 秒变化一次，由 `setInterval` 中的间隔定义。

## 温度转换器

### 描述

在本练习中，学生将创建一个温度转换器，用于在摄氏度和华氏度之间转换温度。本练习介绍如何处理用户输入和执行计算。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Temperature Converter</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="converter">
<h1>Temperature Converter</h1>
<form id="converterForm">
<input type="number" id="temperatureInput" placeholder="Enter temperature" required>
<select id="unitSelect">
<option value="CtoF">Celsius to Fahrenheit</option>
<option value="FtoC">Fahrenheit to Celsius</option>
</select>
<button type="submit">Convert</button>
</form>
<p id="resultDisplay"></p>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.converter {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
display: flex;
flex-direction: column;
gap: 10px;
}
input, select, button {
padding: 10px;
font-size: 16px;
}
```

### JavaScript

```javascript
document.getElementById('converterForm').addEventListener('submit', function(event) {
event.preventDefault();
const temperature = parseFloat(document.getElementById('temperatureInput').value);
const unit = document.getElementById('unitSelect').value;
let convertedTemperature;
if (unit === 'CtoF') {
convertedTemperature = (temperature * 9/5) + 32;
} else {
convertedTemperature = (temperature - 32) * 5/9;
}
document.getElementById('resultDisplay').textContent = `Converted Temperature: ${convertedTemperature.toFixed(2)}°`;
});
```

## 购物清单

### 描述

在本练习中，学生将创建一个购物清单，可以添加和删除项目。本练习介绍如何处理表单输入、动态添加和删除 DOM 元素。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（添加和删除元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shopping List</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="shopping-container">
<h1>Shopping List</h1>
<form id="shoppingForm">
<input type="text" id="itemInput" placeholder="Enter item" required>
<button type="submit">Add Item</button>
</form>
<ul id="shoppingList"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.shopping-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 10px;
margin: 5px 0;
background-color: #fff;
border: 1px solid #ccc;
border-radius: 5px;
display: flex;
justify-content: space-between;
}
button.remove {
background: none;
border: none;
color: red;
cursor: pointer;
font-size: 16px;
}
```

### JavaScript

```javascript
document.getElementById('shoppingForm').addEventListener('submit', function(event) {
event.preventDefault();
const itemInput = document.getElementById('itemInput');
const itemText = itemInput.value;
if (itemText === '') return;
const li = document.createElement('li');
li.textContent = itemText;
const removeButton = document.createElement('button');
removeButton.textContent = 'Remove';
removeButton.classList.add('remove');
removeButton.addEventListener('click', function() {
li.remove();
});
li.appendChild(removeButton);
document.getElementById('shoppingList').appendChild(li);
itemInput.value = '';
});
```

## 亮色/暗色模式切换

### 描述

在本练习中，学生将创建一个亮色/暗色模式切换按钮，用于在亮色和暗色模式之间切换网页主题。本练习介绍如何切换 CSS 类并动态更新样式。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（切换类）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Light/Dark Mode Toggle</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="container">
<button id="toggleButton">Toggle Light/Dark Mode</button>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS



```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
transition: background-color 0.3s, color 0.3s;
}

body.light-mode {
background-color: white;
color: black;
}

body.dark-mode {
background-color: black;
color: white;
}

.container {
text-align: center;
}

button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
```

JavaScript:

```javascript
document.getElementById('toggleButton').addEventListener('click', function() {
document.body.classList.toggle('dark-mode');
document.body.classList.toggle('light-mode');
});
```

## 秒表

### 描述

在本练习中，学生将创建一个可以开始、停止和重置的秒表。本练习介绍如何使用定时器、控制其执行以及动态更新 DOM。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 定时器的使用
- DOM 操作（更新文本内容）

HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stopwatch</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="stopwatch-container">
<h1>Stopwatch</h1>
<p id="stopwatchDisplay">00:00:00</p>
<div class="buttons">
<button id="startButton">Start</button>
<button id="stopButton">Stop</button>
<button id="resetButton">Reset</button>
</div>
</div>
<script src="script.js"></script>
</body>
</html>
```

CSS:

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}

.stopwatch-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#stopwatchDisplay {
font-size: 36px;
margin-bottom: 20px;
}

.buttons {
display: flex;
justify-content: center;
gap: 10px;
}

button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
```

JavaScript:

```javascript
let timer;
let startTime;
let elapsedTime = 0;
let isRunning = false;

function updateDisplay() {
const display = document.getElementById('stopwatchDisplay');
const time = new Date(elapsedTime);
const minutes = time.getUTCMinutes().toString().padStart(2, '0');
const seconds = time.getUTCSeconds().toString().padStart(2, '0');
const milliseconds = Math.floor(time.getUTCMilliseconds() / 10).toString().padStart(2, '0');
display.textContent = `${minutes}:${seconds}:${milliseconds}`;
}

document.getElementById('startButton').addEventListener('click', function() {
if (!isRunning) {
startTime = Date.now() - elapsedTime;
timer = setInterval(function() {
elapsedTime = Date.now() - startTime;
updateDisplay();
}, 10);
isRunning = true;
}
});

document.getElementById('stopButton').addEventListener('click', function() {
if (isRunning) {
clearInterval(timer);
isRunning = false;
}
});

document.getElementById('resetButton').addEventListener('click', function() {
clearInterval(timer);
elapsedTime = 0;
updateDisplay();
isRunning = false;
});
```

## 密码强度检查器

### 描述

在本练习中，学生将创建一个密码强度检查器，根据输入的密码提供强度反馈。本练习介绍如何处理表单输入并根据输入值提供实时反馈。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新文本内容和样式）
- 实时输入验证

HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Password Strength Checker</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="password-container">
<h1>Password Strength Checker</h1>
<input type="password" id="passwordInput" placeholder="Enter password">
<p id="strengthDisplay">Password Strength: </p>
</div>
<script src="script.js"></script>
</body>
</html>
```

CSS:

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}

.password-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

input {
padding: 10px;
font-size: 16px;
margin-bottom: 10px;
}

p {
font-size: 18px;
margin: 0;
}
```

JavaScript:

```javascript
function checkStrength(password) {
let strength = 'Weak';
const regexes = [
/[a-z]/,
/[A-Z]/,
/[0-9]/,
/[^a-zA-Z0-9]/
];
const passedTests = regexes.filter(regex => regex.test(password)).length;
if (password.length >= 8 && passedTests >= 3) {
strength = 'Strong';
} else if (password.length >= 6 && passedTests >= 2) {
strength = 'Medium';
}
return strength;
}

document.getElementById('passwordInput').addEventListener('input', function() {
const password = this.value;
const strength = checkStrength(password);
document.getElementById('strengthDisplay').textContent = `Password Strength: ${strength}`;
});
```

## 小费计算器

### 描述

在本练习中，学生将创建一个小费计算器，根据用户输入计算小费金额和总账单。本练习介绍如何处理用户输入并执行计算。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算

HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tip Calculator</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="calculator-container">
<h1>Tip Calculator</h1>
<form id="calculatorForm">
<input type="number" id="billAmount" placeholder="Enter bill amount" required>
<input type="number" id="tipPercentage" placeholder="Enter tip percentage" required>
<button type="submit">Calculate</button>
</form>
<p id="tipAmountDisplay">Tip Amount: $0.00</p>
<p id="totalAmountDisplay">Total Amount: $0.00</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

CSS:

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}

.calculator-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form {
display: flex;
flex-direction: column;
gap: 10px;
}

input, button {
padding: 10px;
font-size: 16px;
}

p {
font-size: 18px;
margin: 0;
}
```

JavaScript:

```javascript
document.getElementById('calculatorForm').addEventListener('submit', function(event) {
event.preventDefault();
const billAmount = parseFloat(document.getElementById('billAmount').value);
const tipPercentage = parseFloat(document.getElementById('tipPercentage').value);
const tipAmount = (billAmount * (tipPercentage / 100)).toFixed(2);
const totalAmount = (billAmount + parseFloat(tipAmount)).toFixed(2);
document.getElementById('tipAmountDisplay').textContent = `Tip Amount: $${tipAmount}`;
document.getElementById('totalAmountDisplay').textContent = `Total Amount: $${totalAmount}`;
});
```

## 颜色选择器

### 描述

在本练习中，学生将创建一个颜色选择器，根据从输入中选择的颜色更改 div 的背景颜色。本练习介绍如何使用输入元素并动态更新样式。

### 涉及主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新样式）

HTML：

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Color Picker</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="color-picker-container">
<h1>Color Picker</h1>
<input type="color" id="colorInput">
<div id="colorBox"></div>
</div>
<script src="script.js"></script>
</body>
</html>
```

CSS：

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.color-picker-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
#colorBox {
width: 100px;
height: 100px;
margin-top: 20px;
border: 1px solid #ccc;
}
```

JavaScript：

```javascript
document.getElementById('colorInput').addEventListener('input', function() {
const color = this.value;
document.getElementById('colorBox').style.backgroundColor = color;
});
```

## 单词计数器

### 描述

在此练习中，学生将创建一个单词计数器，用于统计文本区域输入中的单词数量，并实时显示计数。本练习介绍如何处理输入事件以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新文本内容）

HTML：



```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Word Counter</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="counter-container">
<h1>Word Counter</h1>
<textarea id="textInput" placeholder="Type something..."></textarea>
<p id="wordCount">Words: 0</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

CSS：

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.counter-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
textarea {
width: 100%;
height: 100px;
padding: 10px;
font-size: 16px;
margin-bottom: 10px;
}
p {
font-size: 18px;
margin: 0;
}
```

JavaScript：

```javascript
document.getElementById('textInput').addEventListener('input', function() {
const text = this.value.trim();
const wordCount = text === '' ? 0 : text.split(/\s+/).length;
document.getElementById('wordCount').textContent = `Words: ${wordCount}`;
});
```

## 多项选择题

### 温度转换器

在温度转换器练习中，转换后的温度如何显示？

a) 使用 `innerHTML`

b) 使用 `textContent`

c) 使用 `value`

d) 使用 `appendChild`

答案：b) 使用 `textContent`

解释：`textContent` 属性用于在结果显示元素中显示转换后的温度。

在温度转换器练习中，使用什么事件监听器来处理表单提交？

A) `input`

B) `change`

C) `submit`

D) `click`

答案：C

解释：`submit` 事件监听器用于处理表单提交，从而执行温度转换。

在温度转换器练习中，哪个函数将摄氏度转换为华氏度？

A) `(temperature * 5/9) + 32`

B) `(temperature * 9/5) + 32`

C) `(temperature - 32) * 9/5`

D) `(temperature - 32) * 5/9`

答案：B

解释：公式 `(temperature * 9/5) + 32` 将摄氏度转换为华氏度。

在温度转换器练习中，温度输入字段使用什么类型？

A) `text`

B) `number`

C) `range`

D) `date`

答案：B

说明：温度输入使用数字输入字段，以确保输入为数值。

### 购物清单

在购物清单练习中，使用什么方法向购物清单添加新项目？

a) `appendChild`

b) `insertAdjacentHTML`

c) `innerHTML`

d) `textContent`

答案：a) `appendChild`

解释：`appendChild` 方法用于向购物清单添加新的列表项元素。

在购物清单练习中，如何从购物清单中移除一个项目？

a) 设置 `display: none`

b) 设置 `visibility: hidden`

c) 使用 `remove` 方法

d) 设置 `innerHTML = ''`

答案：c) 使用 `remove` 方法

解释：`remove` 方法用于从购物清单中移除列表项元素。

在“购物清单”练习中，用于向购物列表添加新项的事件监听器是哪个？

A) `input`

B) `click`

C) `submit`

D) `keydown`

答案：C

说明：当表单提交时，使用 `submit` 事件监听器向购物列表添加新项。

在“购物清单”练习中，如何从购物列表中移除一项？

A) 双击该项

B) 单击该项

C) 按删除键

D) 单击该项旁边的移除按钮

答案：D

说明：单击该项旁边的移除按钮会触发将其从购物列表中移除。

### 亮/暗模式切换

在亮/暗模式切换练习中，使用什么方法切换主题？

a) `toggle`

b) `classList.toggle`

c) `classList.add`

d) `classList.remove`

答案：b) `classList.toggle`

解释：`classList.toggle` 方法用于通过切换相应的 CSS 类来在亮模式和暗模式之间切换。

在“明暗模式切换”练习中，用于切换明暗模式的事件监听器是哪个？

A) `mouseover`

B) `click`

C) `dblclick`

D) `focus`

答案：B

说明：使用 `click` 事件监听器来切换明暗模式。

在“明暗模式切换”练习中，切换明暗模式时切换的是哪些 CSS 类？

A) `day-mode` 和 `night-mode`

B) `light-theme` 和 `dark-theme`

C) `light-mode` 和 `dark-mode`

D) `white-mode` 和 `black-mode`

答案：C

说明：切换 `light-mode` 和 `dark-mode` 这两个 CSS 类来实现明暗模式切换。

### 秒表

在秒表练习中，使用什么方法每 10 毫秒更新一次显示？

a) `setTimeout`

b) `setInterval`

c) `requestAnimationFrame`

d) `clearInterval`

答案：b) `setInterval`

解释：`setInterval` 函数用于每 10 毫秒重复执行更新显示的函数。

在秒表练习中，如何启动计时器？

a) 将 `isRunning` 设置为 true

b) 调用 `startTime` 函数

c) 初始化计时器变量

d) 设置 `startTime` 并使用 `setInterval`

答案：d) 设置 `startTime` 并使用 `setInterval`

解释：通过设置 `startTime` 并使用 `setInterval` 更新经过的时间和显示来启动计时器。

在“秒表”练习中，用于重复更新秒表显示的函数是哪个？

A) `setTimeout`

B) `clearInterval`

C) `setInterval`

D) `requestAnimationFrame`

答案：C

说明：使用 `setInterval` 函数重复更新秒表显示。

在“秒表”练习中，点击重置按钮会发生什么？

A) 秒表暂停

B) 秒表继续

C) 经过时间重置为零

D) 秒表从上一次时间重新开始

答案：C

说明：点击重置按钮会将经过时间重置为零并停止计时器。

### 密码强度检查器

在密码强度检查器练习中，使用什么函数来确定密码的强度？

a) `checkPassword`

b) `validatePassword`

c) `checkStrength`

d) `passwordStrength`

答案：c) `checkStrength`

解释：`checkStrength` 函数用于根据特定标准确定输入密码的强度。

在密码强度检查器练习中，使用哪些标准来确定密码的强度？

a) 长度、数字和特殊字符的存在

b) 长度、大写和小写字母、数字和特殊字符的存在

c) 长度、空格和标点符号的存在

d) 长度、字母的存在和大小写敏感性

答案：b) 长度、大写和小写字母、数字和特殊字符的存在

解释：密码的强度根据其长度以及大写和小写字母、数字和特殊字符的存在来确定。

在“密码强度检查器”练习中，密码使用什么类型的输入字段？

A) `text`

B) `number`

C) `password`

D) `email`

答案：C

说明：使用密码输入字段以确保输入时密码被隐藏。

在“密码强度检查器”练习中，如何确定密码强度？

A) 检查密码长度

B) 检查是否存在不同类型的字符

C) 将密码与预定义列表进行比较

D) 用正则表达式检查密码

答案：B

说明：通过检查是否存在不同类型的字符（例如小写字母、大写字母、数字、特殊字符）以及密码长度来确定密码强度。

### 小费计算器

在小费计算器练习中，如何计算小费金额？

a) `(billAmount * tipPercentage / 100)`

b) `(billAmount + tipPercentage / 100)`

c) `(billAmount * (tipPercentage / 100) + billAmount)`

d) `(billAmount / tipPercentage * 100)`

答案：a) `(billAmount * tipPercentage / 100)`

解释：小费金额通过将账单金额乘以小费百分比再除以 100 来计算。

在“小费计算器”练习中，用于处理表单提交的事件监听器是哪个？

A) `input`

B) `change`

C) `submit`

D) `click`

答案：C

说明：使用 `submit` 事件监听器处理表单提交，触发小费金额和总账单的计算。

在“小费计算器”练习中，小费金额如何计算？

A) `billAmount / tipPercentage`

B) `billAmount * (tipPercentage / 100)`

C) `billAmount + tipPercentage`

D) `billAmount - (tipPercentage / 100)`

答案：B

说明：小费金额计算公式为 `billAmount * (tipPercentage / 100)`。

### 颜色选择器

在颜色选择器练习中，使用哪种输入类型来选择颜色？

a) `text`

b) `color`

c) `range`

d) `checkbox`

答案：b) `color`

解释：`color` 输入类型用于提供颜色选择器界面。

在颜色选择器练习中，如何更新颜色框的背景颜色？

a) 更改 `innerHTML`

b) 更改 `textContent`

c) 更改 `value`

d) 更改 `style.backgroundColor`

答案：d) 更改 `style.backgroundColor`

解释：`style.backgroundColor` 属性用于根据所选颜色更新颜色框的背景颜色。

在“颜色选择器”练习中，用于选择颜色的输入字段类型是什么？

A) `text`

B) `number`

C) `color`

D) `range`

答案：C

说明：使用颜色输入字段，允许用户从颜色选择器中选择颜色。

在“颜色选择器”练习中，用于改变 div 背景颜色的事件监听器是哪个？

A) `input`

B) `click`

C) `submit`

D) `change`

答案：A

说明：当用户选择颜色时，使用 `input` 事件监听器改变 div 的背景颜色。

### 单词计数器

在单词计数器练习中，使用什么事件来更新单词计数？

a) `change`

b) `input`

c) `keyup`

d) `keydown`

答案：b) `input`

解释：每当输入或文本区域的值发生变化时，会触发 `input` 事件，非常适合实时更新。

在单词计数器练习中，如何计算单词数量？

a) 通过统计字符数

b) 通过按逗号分割文本

c) 通过按空格分割文本

d) 通过按换行符分割文本

答案：c) 通过按空格分割文本

解释：单词数量通过按空格分割文本并统计结果数组元素来计算。

在“单词计数器”练习中，用于更新单词计数的事件是哪个？

A) `keypress`

B) `keydown`

C) `keyup`

D) `input`

答案：D

说明：当用户在文本区域中键入时，使用 `input` 事件更新单词计数。

在“单词计数器”练习中，如何计算单词数？

A) 统计行数

B) 统计字符数

C) 按空格分割文本并统计结果数组的长度

D) 统计句子数

答案：C

说明：通过按空格分割文本并统计结果数组的长度来计算单词数。

### DOM 操作

在 DOM 中创建新 HTML 元素使用什么方法？

A) `getElementById`

B) `createElement`

C) `appendChild`

D) `querySelector`

答案：B

说明：`createElement` 方法用于在 DOM 中创建新的 HTML 元素。

在 DOM 中向现有元素追加新的子元素使用什么方法？

A) `createElement`

B) `appendChild`

C) `removeChild`

D) `getElementById`

答案：B

说明：`appendChild` 方法用于向现有元素追加新的子元素。

如何在 JavaScript 中阻止表单提交？

A) `return false`

B) `event.stopPropagation()`

C) `event.preventDefault()`

D) `event.stopImmediatePropagation()`

答案：C

说明：`event.preventDefault()` 方法用于阻止表单提交，从而允许自定义处理表单数据。

## 带本地存储的待办事项列表

### 描述

在本练习中，学生将创建一个待办事项列表，该列表将任务保存到本地存储中，以便在页面刷新后仍然保留。本练习介绍了如何使用本地存储、处理表单输入以及动态更新 DOM。

### 涵盖的主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 本地存储
- DOM 操作（添加、更新和删除元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>To-Do List with Local Storage</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="todo-container">
<h1>To-Do List</h1>
<form id="todoForm">
<input type="text" id="taskInput" placeholder="Enter a new task" required>
<button type="submit">Add Task</button>
</form>
<ul id="taskList"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.todo-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 10px;
margin: 5px 0;
background-color: #fff;
border: 1px solid #ccc;
border-radius: 5px;
display: flex;
justify-content: space-between;
}
button.remove {
background: none;
border: none;
color: red;
cursor: pointer;
font-size: 16px;
}
```

### JavaScript



```javascript
document.addEventListener('DOMContentLoaded', function() {
  const taskList = document.getElementById('taskList');
  const tasks = JSON.parse(localStorage.getItem('tasks')) || [];

  tasks.forEach(task => {
    addTaskToDOM(task);
  });

  document.getElementById('todoForm').addEventListener('submit', function(event) {
    event.preventDefault();

    const taskInput = document.getElementById('taskInput');
    const taskText = taskInput.value;

    if (taskText === '') return;

    addTaskToDOM(taskText);
    tasks.push(taskText);
    localStorage.setItem('tasks', JSON.stringify(tasks));
    taskInput.value = '';
  });

  function addTaskToDOM(taskText) {
    const li = document.createElement('li');
    li.textContent = taskText;

    const removeButton = document.createElement('button');
    removeButton.textContent = 'Remove';
    removeButton.classList.add('remove');

    removeButton.addEventListener('click', function() {
      li.remove();

      const index = tasks.indexOf(taskText);
      tasks.splice(index, 1);
      localStorage.setItem('tasks', JSON.stringify(tasks));
    });

    li.appendChild(removeButton);
    taskList.appendChild(li);
  }
});
```

# BMI 计算器

## 描述

在此练习中，学生将创建一个 BMI（身体质量指数）计算器，根据用户输入的体重和身高计算 BMI。本练习介绍如何处理表单输入和执行计算。

## 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BMI Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="calculator-container">
    <h1>BMI Calculator</h1>
    <form id="bmiForm">
      <input type="number" id="weightInput" placeholder="Enter weight in kg" required>
      <input type="number" id="heightInput" placeholder="Enter height in cm" required>
      <button type="submit">Calculate</button>
    </form>
    <p id="bmiDisplay">Your BMI: </p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.calculator-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input, button {
  padding: 10px;
  font-size: 16px;
}

p {
  font-size: 18px;
  margin: 0;
}
```

## JavaScript

```javascript
document.getElementById('bmiForm').addEventListener('submit', function(event) {
  event.preventDefault();

  const weight = parseFloat(document.getElementById('weightInput').value);
  const height = parseFloat(document.getElementById('heightInput').value) / 100;
  const bmi = (weight / (height * height)).toFixed(2);

  document.getElementById('bmiDisplay').textContent = `Your BMI: ${bmi}`;
});
```

# 数字时钟

## 描述

在此练习中，学生将创建一个数字时钟，显示当前时间并每秒更新。本练习介绍如何处理日期和时间，以及动态更新 DOM。

## 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理日期和时间
- DOM 操作（更新文本内容）

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Digital Clock</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="clock-container">
    <h1>Digital Clock</h1>
    <p id="clockDisplay">00:00:00</p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.clock-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#clockDisplay {
  font-size: 36px;
  margin-top: 20px;
}
```

## JavaScript

```javascript
function updateClock() {
  const now = new Date();
  const hours = now.getHours().toString().padStart(2, '0');
  const minutes = now.getMinutes().toString().padStart(2, '0');
  const seconds = now.getSeconds().toString().padStart(2, '0');

  document.getElementById('clockDisplay').textContent = `${hours}:${minutes}:${seconds}`;
}

setInterval(updateClock, 1000);
updateClock(); // Initial call to display clock immediately
```

# 响应式导航菜单

## 描述

在此练习中，学生将创建一个响应式导航菜单，在较小屏幕上折叠为汉堡菜单。本练习介绍使用 CSS 进行响应式设计以及处理 JavaScript 中的点击事件。

## 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 响应式设计
- DOM 操作（切换类）

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Navigation Menu</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <nav class="navbar">
    <div class="brand-title">Brand</div>
    <a href="#" class="toggle-button">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </a>
    <div class="navbar-links">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
  </nav>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  padding: 10px 20px;
  color: white;
}

.brand-title {
  font-size: 1.5rem;
}

.navbar-links ul {
  list-style: none;
  padding: 0;
}

.navbar-links li {
  display: inline;
  padding: 0 20px;
}

.navbar-links a {
  color: white;
  text-decoration: none;
}

.toggle-button {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.toggle-button .bar {
  width: 25px;
  height: 3px;
  background-color: white;
  margin: 4px 0;
}

@media (max-width: 768px) {
  .toggle-button {
    display: flex;
  }

  .navbar-links {
    display: none;
    width: 100%;
  }

  .navbar-links ul {
    width: 100%;
    display: flex;
    flex-direction: column;
  }

  .navbar-links li {
    text-align: center;
    padding: 10px 0;
  }

  .navbar-links.active {
    display: flex;
  }
}
```

## JavaScript

```javascript
document.querySelector('.toggle-button').addEventListener('click', function() {
  document.querySelector('.navbar-links').classList.toggle('active');
});
```

# 测验应用

## 描述

在此练习中，学生将创建一个简单的测验应用，显示问题并评估答案。本练习介绍如何处理用户输入、动态更新 DOM 以及提供反馈。

## 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新元素）
- 处理用户输入

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quiz Application</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="quiz-container">
    <h1>Quiz Application</h1>
    <div id="quiz"></div>
    <button id="submit">Submit</button>
    <div id="results"></div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.quiz-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 20px;
}
```

## JavaScript

```javascript
const quizContainer = document.getElementById('quiz');
const resultsContainer = document.getElementById('results');
const submitButton = document.getElementById('submit');

const myQuestions = [
  {
    question: "What is the capital of France?",
    answers: {
      a: "Berlin",
      b: "Madrid",
      c: "Paris"
    },
    correctAnswer: "c"
  },
  {
    question: "Who is the CEO of Tesla?",
    answers: {
      a: "Jeff Bezos",
      b: "Elon Musk",
      c: "Bill Gates"
    },
    correctAnswer: "b"
  },
  {
    question: "What is the smallest planet in our solar system?",
    answers: {
      a: "Mars",
      b: "Venus",
      c: "Mercury"
    },
    correctAnswer: "c"
  }
];

function buildQuiz() {
  const output = [];

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answers = [];

    for (letter in currentQuestion.answers) {
      answers.push(
        `<label>
          <input type="radio" name="question${questionNumber}" value="${letter}">
          ${letter} :
          ${currentQuestion.answers[letter]}
        </label>`
      );
    }

    output.push(
      `<div class="question"> ${currentQuestion.question} </div>
      <div class="answers"> ${answers.join('')} </div>`
    );
  });
}
```



```javascript
quizContainer.innerHTML = output.join('');
}

function showResults() {
const answerContainers = quizContainer.querySelectorAll('.answers');
let numCorrect = 0;

myQuestions.forEach((currentQuestion, questionNumber) => {
const answerContainer = answerContainers[questionNumber];
const selector = `input[name=question${questionNumber}]:checked`;
const userAnswer = (answerContainer.querySelector(selector) || {}).value;

if (userAnswer === currentQuestion.correctAnswer) {
numCorrect++;
answerContainers[questionNumber].style.color = 'green';
} else {
answerContainers[questionNumber].style.color = 'red';
}
});

resultsContainer.innerHTML = `${numCorrect} out of ${myQuestions.length}`;
}

buildQuiz();

submitButton.addEventListener('click', showResults);
```

### 番茄钟计时器

#### 描述

在本练习中，学生将创建一个包含工作时段和休息时段的番茄钟计时器。本练习介绍如何使用定时器、处理用户输入以及动态更新 DOM。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 使用定时器
- DOM 操作（更新文本内容）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pomodoro Timer</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="pomodoro-container">
<h1>Pomodoro Timer</h1>
<p id="timerDisplay">25:00</p>
<div class="buttons">
<button id="startButton">Start</button>
<button id="resetButton">Reset</button>
</div>
</div>
<script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.pomodoro-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
#timerDisplay {
font-size: 48px;
margin: 20px 0;
}
.buttons {
display: flex;
justify-content: center;
gap: 10px;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
```

#### JavaScript

```javascript
let timer;
let timeLeft = 1500; // 25 minutes
let isRunning = false;

function updateDisplay() {
const minutes = Math.floor(timeLeft / 60).toString().padStart(2, '0');
const seconds = (timeLeft % 60).toString().padStart(2, '0');
document.getElementById('timerDisplay').textContent = `${minutes}:${seconds}`;
}

function startTimer() {
if (!isRunning) {
timer = setInterval(function() {
if (timeLeft > 0) {
timeLeft--;
updateDisplay();
} else {
clearInterval(timer);
alert('Time is up!');
}
}, 1000);
isRunning = true;
}
}

function resetTimer() {
clearInterval(timer);
timeLeft = 1500; // Reset to 25 minutes
updateDisplay();
isRunning = false;
}

document.getElementById('startButton').addEventListener('click', startTimer);
document.getElementById('resetButton').addEventListener('click', resetTimer);
updateDisplay();
```

### 带历史记录的计算器

#### 描述

在本练习中，学生将创建一个能保存计算历史记录的简易计算器。本练习介绍如何处理用户输入、执行计算以及更新 DOM。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理用户输入
- 执行计算
- DOM 操作（添加和更新元素）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calculator with History</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="calculator-container">
<h1>Calculator</h1>
<input type="text" id="display" disabled>
<div class="buttons">
<button class="number">7</button>
<button class="number">8</button>
<button class="number">9</button>
<button class="operator">/</button>
<button class="number">4</button>
<button class="number">5</button>
<button class="number">6</button>
<button class="operator">*</button>
<button class="number">1</button>
<button class="number">2</button>
<button class="number">3</button>
<button class="operator">-</button>
<button class="number">0</button>
<button id="clear">C</button>
<button id="equals">=</button>
<button class="operator">+</button>
</div>
<h2>History</h2>
<ul id="history"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.calculator-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
input {
width: 200px;
padding: 10px;
margin-bottom: 10px;
font-size: 18px;
text-align: right;
border: 1px solid #ccc;
border-radius: 5px;
}
.buttons {
display: grid;
grid-template-columns: repeat(4, 50px);
gap: 10px;
}
button {
width: 50px;
height: 50px;
font-size: 18px;
cursor: pointer;
}
h2 {
margin-top: 20px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
margin: 5px 0;
background-color: #fff;
padding: 5px;
border: 1px solid #ccc;
border-radius: 5px;
}
```

#### JavaScript

```javascript
let display = document.getElementById('display');
let buttons = Array.from(document.getElementsByClassName('number'));
let operators = Array.from(document.getElementsByClassName('operator'));
let clear = document.getElementById('clear');
let equals = document.getElementById('equals');
let currentOperator = null;
let firstOperand = null;
let secondOperand = null;
let history = document.getElementById('history');

buttons.forEach(button => {
button.addEventListener('click', function() {
display.value += this.textContent;
});
});

operators.forEach(operator => {
operator.addEventListener('click', function() {
if (display.value) {
firstOperand = parseFloat(display.value);
currentOperator = this.textContent;
display.value = '';
}
});
});

clear.addEventListener('click', function() {
display.value = '';
firstOperand = null;
secondOperand = null;
currentOperator = null;
});

equals.addEventListener('click', function() {
if (display.value) {
secondOperand = parseFloat(display.value);
let result;
switch (currentOperator) {
case '+':
result = firstOperand + secondOperand;
break;
case '-':
result = firstOperand - secondOperand;
break;
case '*':
result = firstOperand * secondOperand;
break;
case '/':
result = firstOperand / secondOperand;
break;
}
display.value = result;
let historyItem = document.createElement('li');
historyItem.textContent = `${firstOperand} ${currentOperator} ${secondOperand} = ${result}`;
history.appendChild(historyItem);
firstOperand = null;
secondOperand = null;
currentOperator = null;
}
});
```

### 自定义倒计时器

#### 描述

在本练习中，学生将创建一个倒计时器，用户可以输入自定义的倒计时时间。本练习介绍如何处理表单输入、使用定时器以及动态更新 DOM。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 使用定时器
- DOM 操作（更新文本内容）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Custom Countdown Timer</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="timer-container">
<h1>Countdown Timer</h1>
<input type="number" id="timeInput" placeholder="Enter seconds" required>
<div class="buttons">
<button id="startButton">Start</button>
<button id="resetButton">Reset</button>
</div>
<p id="timerDisplay">0:00</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.timer-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

input {
  padding: 10px;
  font-size: 16px;
  margin-bottom: 10px;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-bottom: 20px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

p {
  font-size: 24px;
  margin: 0;
}
```

#### JavaScript



```javascript
let timer;
let timeLeft;
let isRunning = false;

function updateDisplay() {
  const minutes = Math.floor(timeLeft / 60).toString().padStart(1, '0');
  const seconds = (timeLeft % 60).toString().padStart(2, '0');
  document.getElementById('timerDisplay').textContent = `${minutes}:${seconds}`;
}

function startTimer() {
  if (!isRunning) {
    const timeInput = parseInt(document.getElementById('timeInput').value, 10);
    timeLeft = timeInput;
    timer = setInterval(function() {
      if (timeLeft > 0) {
        timeLeft--;
        updateDisplay();
      } else {
        clearInterval(timer);
        alert('Time is up!');
      }
    }, 1000);
    isRunning = true;
  }
}

function resetTimer() {
  clearInterval(timer);
  timeLeft = 0;
  updateDisplay();
  isRunning = false;
}

document.getElementById('startButton').addEventListener('click', startTimer);
document.getElementById('resetButton').addEventListener('click', resetTimer);
```

### 自定义分账小费计算器

#### 描述

在本练习中，学生将创建一个小费计算器，根据用户输入的账单金额、小费百分比和人数，计算每人应付的小费金额和总账单。本练习介绍如何处理多个表单输入并执行计算。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tip Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="calculator-container">
    <h1>Tip Calculator</h1>
    <form id="calculatorForm">
      <input type="number" id="billAmount" placeholder="Enter bill amount" required>
      <input type="number" id="tipPercentage" placeholder="Enter tip percentage" required>
      <input type="number" id="numberOfPeople" placeholder="Enter number of people" required>
      <button type="submit">Calculate</button>
    </form>
    <p id="tipAmountDisplay">Tip Amount: $0.00</p>
    <p id="totalAmountDisplay">Total Amount: $0.00</p>
    <p id="perPersonDisplay">Amount per Person: $0.00</p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.calculator-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input, button {
  padding: 10px;
  font-size: 16px;
}

p {
  font-size: 18px;
  margin: 5px 0;
}
```

#### JavaScript

```javascript
document.getElementById('calculatorForm').addEventListener('submit', function(event) {
  event.preventDefault();
  const billAmount = parseFloat(document.getElementById('billAmount').value);
  const tipPercentage = parseFloat(document.getElementById('tipPercentage').value);
  const numberOfPeople = parseInt(document.getElementById('numberOfPeople').value);
  const tipAmount = (billAmount * (tipPercentage / 100)).toFixed(2);
  const totalAmount = (billAmount + parseFloat(tipAmount)).toFixed(2);
  const perPersonAmount = (totalAmount / numberOfPeople).toFixed(2);
  document.getElementById('tipAmountDisplay').textContent = `Tip Amount: $${tipAmount}`;
  document.getElementById('totalAmountDisplay').textContent = `Total Amount: $${totalAmount}`;
  document.getElementById('perPersonDisplay').textContent = `Amount per Person: $${perPersonAmount}`;
});
```

### 多项选择题

#### 带本地存储的待办事项列表

在“带本地存储的待办事项列表”练习中，用于将任务存储到本地存储的方法是？

- a) `localStorage.setItem`
- b) `localStorage.save`
- c) `localStorage.store`
- d) `localStorage.addItem`

**答案：**a) `localStorage.setItem`

**解释：**`localStorage.setItem` 方法用于将任务以字符串形式存储到本地存储中。

在“带本地存储的待办事项列表”练习中，如何从待办列表中移除任务？

- a) 调用 `removeChild` 方法
- b) 设置 `display: none`
- c) 使用 `remove` 方法
- d) 设置 `innerHTML = ''`

**答案：**c) 使用 `remove` 方法

**解释：**`remove` 方法用于从 DOM 中移除列表项元素，并更新本地存储。

页面加载时，使用什么事件从本地存储加载任务？

- A) `load`
- B) `DOMContentLoaded`
- C) `click`
- D) `submit`

**答案：**B

**解释：**使用 `DOMContentLoaded` 事件确保在 DOM 完全加载后从本地存储加载任务。

使用什么方法从本地存储中检索项目？

- A) `localStorage.get`
- B) `localStorage.retrieve`
- C) `localStorage.getItem`
- D) `localStorage.fetch`

**答案：**C

**解释：**使用 `localStorage.getItem` 方法从本地存储中检索项目。

任务如何存储在本地存储中？

- A) 纯文本
- B) JSON 字符串
- C) XML
- D) HTML

**答案：**B

**解释：**任务以 JSON 字符串的形式存储在本地存储中，这允许存储数组等复杂数据结构。

在删除任务后，使用什么方法更新本地存储中的任务列表？

- A) `localStorage.updateItem`
- B) `localStorage.removeItem`
- C) `localStorage.setItem`
- D) `localStorage.saveItem`

**答案：**C

**解释：**在修改任务列表后，使用 `localStorage.setItem` 方法更新本地存储中的任务列表。

#### BMI 计算器

在“BMI 计算器”练习中，用于计算 BMI 的公式是？

- a) `weight / height`
- b) `weight / (height * height)`
- c) `weight * height`
- d) `(weight + height) / 2`

**答案：**b) `weight / (height * height)`

**解释：**BMI 的计算方式是用体重（千克）除以身高（米）的平方。

在 BMI 计算器练习中，计算 BMI 的公式是什么？

- A) `(weight / height)`
- B) `(weight / (height * height))`
- C) `(height / weight)`
- D) `(weight * height)`

**答案：**B

**解释：**BMI 使用公式 `(weight / (height * height))` 计算，其中体重以千克为单位，身高以米为单位。

在“BMI 计算器”练习中，身高输入使用的单位是？

- a) 米
- b) 英寸
- c) 英尺
- d) 厘米

**答案：**d) 厘米

**解释：**身高输入以厘米为单位，然后转换为米用于 BMI 计算。

在 BMI 计算器练习中，身高输入的单位是什么？

- A) 英寸
- B) 米
- C) 厘米
- D) 英尺

**答案：**C

**解释：**身高输入以厘米为单位，在 BMI 计算中会转换为米。

#### 数字时钟

在“数字时钟”练习中，用于每秒更新时间的方法是？

- a) `setTimeout`
- b) `setInterval`
- c) `requestAnimationFrame`
- d) `clearInterval`

**答案：**b) `setInterval`

**解释：**`setInterval` 函数用于每 1000 毫秒（1 秒）重复执行 `updateClock` 函数。

在数字时钟练习中，用于每秒重复更新时钟显示的方法是什么？

- A) `setTimeout`
- B) `setInterval`
- C) `requestAnimationFrame`
- D) `clearInterval`

**答案：**B

**解释：**使用 `setInterval` 方法每秒重复更新时钟显示。

在数字时钟练习中，使用什么 JavaScript 对象获取当前时间？

- A) `Date`
- B) `Time`
- C) `Clock`
- D) `Moment`

**答案：**A

**解释：**使用 `Date` 对象获取当前时间。

#### 响应式导航菜单

在“响应式导航菜单”练习中，用于切换导航菜单的事件是？

- a) `mouseover`
- b) `click`
- c) `dblclick`
- d) `mouseout`

**答案：**b) `click`

**解释：**当点击汉堡图标时，使用 `click` 事件来切换导航菜单。

在“响应式导航菜单”练习中，`@media (max-width: 768px)` 的作用是？

- a) 为宽度大于 768px 的屏幕应用样式
- b) 为宽度小于 768px 的屏幕应用样式
- c) 禁用宽度大于 768px 的屏幕的样式
- d) 禁用宽度小于 768px 的屏幕的样式

**答案：**b) 为宽度小于 768px 的屏幕应用样式

**解释：**`@media (max-width: 768px)` CSS 媒体查询为宽度为 768px 或更小的屏幕应用样式。

在响应式导航菜单练习中，用于根据屏幕宽度应用样式的 CSS 规则是什么？

- A) `@import`
- B) `@keyframes`
- C) `@media`
- D) `@viewport`

**答案：**C

**解释：**使用 `@media` 规则根据屏幕宽度应用样式。

在响应式导航菜单练习中，用于切换导航菜单的事件监听器是什么？

- A) `mouseover`
- B) `click`
- C) `dblclick`
- D) `keydown`

**答案：**B

**解释：**当点击汉堡按钮时，使用 `click` 事件监听器切换导航菜单。

#### 问答应用

在“问答应用”练习中，如何获取用户选择的答案？

- a) 使用 `querySelector`
- b) 使用 `getElementById`
- c) 使用 `innerHTML`
- d) 使用 `textContent`

**答案：**a) 使用 `querySelector`

**解释：**`querySelector` 方法用于从单选按钮中选择用户选择的答案。

在“问答应用”练习中，`numCorrect` 变量代表什么？

- a) 错误答案的数量
- b) 问题的总数
- c) 正确答案的数量
- d) 得分百分比

**答案：**c) 正确答案的数量

**解释：**`numCorrect` 变量记录用户选择的正确答案数量。

#### 测验应用

在测验应用练习中，用于显示测验问题和答案的 HTML 元素是什么？

- A) `<form>`
- B) `<div>`
- C) `<ul>`
- D) `<table>`

**答案：**B

**解释：**使用 `<div>` 元素显示测验问题和答案。

在测验应用练习中，用于构建测验界面的函数是什么？

- A) `displayQuiz`
- B) `showQuiz`
- C) `buildQuiz`
- D) `renderQuiz`

**答案：**C

**解释：**调用 `buildQuiz` 函数来构建测验界面。

在测验应用练习中，如何评估用户的答案？

- A) 通过将输入值与预定义答案进行比较
- B) 通过检查表单提交中的值
- C) 通过遍历单选按钮并检查选中的值
- D) 通过使用服务器端脚本

**答案：**C

**解释：**通过遍历单选按钮并检查选中的值来评估用户的答案。

#### 番茄钟计时器

在“番茄钟计时器”练习中，计时器的初始时间设置为？

- a) 20 分钟
- b) 25 分钟
- c) 30 分钟
- d) 15 分钟

**答案：**b) 25 分钟

**解释：**番茄钟计时器的初始时间设置为 25 分钟（1500 秒）。

在番茄钟练习中，`isRunning` 变量代表什么？

- a) 剩余时间
- b) 初始时间
- c) 计时器状态
- d) 当前间隔

**答案：**c) 计时器状态

**解释：**`isRunning` 变量表示计时器当前是否正在运行。

在番茄钟练习中，用于更新计时器显示的函数是什么？

- A) `showTimer`
- B) `displayTimer`

#### 带历史记录的计算器

在“带历史记录的计算器”练习中，如何显示计算历史？

- a) 使用 `innerHTML`
- b) 使用 `textContent`
- c) 使用 `appendChild`
- d) 使用 `insertAdjacentHTML`

**答案：**c) 使用 `appendChild`

**解释：**通过创建列表项并使用 `appendChild` 将其追加到历史元素中来显示计算历史。

在带历史记录的计算器练习中，用于清除显示的方法是什么？

- a) `innerHTML = ''`
- b) `textContent = ''`
- c) `value = ''`
- d) `removeChild`

**答案：**c) `value = ''`

**解释：**将显示输入的 `value` 属性设置为空字符串以清除显示。

#### 自定义时间倒计时器

在“自定义时间倒计时器”练习中，用于启动计时器的事件是？

- a) `click`
- b) `input`
- c) `change`
- d) `submit`

**答案：**a) `click`

**解释：**当点击开始按钮时，使用 `click` 事件来启动计时器。

#### 自定义分摊小费计算器

在带自定义分摊的小费计算器练习中，人均金额如何计算？

- a) `(totalAmount / tipPercentage)`
- b) `(billAmount / numberOfPeople)`
- c) `(totalAmount / numberOfPeople)`
- d) `(billAmount + tipAmount) / numberOfPeople`

**答案：**c) `(totalAmount / numberOfPeople)`

**解释：**人均金额通过总金额除以人数计算得出。

在带自定义分摊的小费计算器练习中，计算小费需要哪些输入字段？

- a) 账单金额和人数
- b) 账单金额和小费百分比
- c) 小费百分比和人数
- d) 账单金额、小费百分比和人数

**答案：**d) 账单金额、小费百分比和人数

**解释：**需要账单金额、小费百分比和人数来计算小费金额、总金额和人均金额。



`C) updateDisplay`

`D) refreshDisplay`

答案：`C`  
解释：使用`updateDisplay`函数更新计时器显示。

## 计时器与计算器练习

### 在番茄钟练习中，如何启动计时器？

A) 通过设置超时

B) 通过使用循环

C) 通过设置间隔

D) 通过使用递归

答案：`C`  
解释：使用`setInterval`启动计时器，每秒更新计时器显示。

### 在带历史记录的计算器练习中，计算历史如何存储？

A) 在数据库中

B) 在本地存储中

C) 在数组中

D) 在会话存储中

答案：`C`  
解释：计算历史存储在数组中，并显示在`DOM`中。

### 在带历史记录的计算器练习中，用于清除显示的事件监听器是什么？

A) `click`

B) `dblclick`

C) `mouseover`

D) `keydown`

答案：`A`  
解释：当点击清除按钮时，使用`click`事件监听器清除显示。

### 在带自定义时间的倒计时器练习中，用于启动倒计时器的函数是什么？

A) `beginTimer`

B) `initiateTimer`

C) `startTimer`

D) `runTimer`

答案：`C`  
解释：使用`startTimer`函数启动倒计时器。

### 在带自定义时间的倒计时器练习中，用于清除间隔的方法是什么？

A) `stopInterval`

B) `clearTimer`

C) `clearInterval`

D) `resetInterval`

答案：`C`  
解释：使用`clearInterval`方法清除间隔并停止计时器。

### 在带自定义分摊的小费计算器练习中，用于处理表单提交的事件监听器是什么？

A) `click`

B) `change`

C) `submit`

D) `input`

答案：`C`  
解释：使用`submit`事件监听器处理表单提交，触发小费和总金额的计算。

## 动态表格筛选

### 描述

在本练习中，学生将创建一个动态表格筛选器，允许用户根据输入筛选行。本练习介绍如何处理输入事件以及动态更新`DOM`以显示或隐藏表格行。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- `DOM`操作（根据输入筛选元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dynamic Table Filter</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="filter-container">
<h1>Dynamic Table Filter</h1>
<input type="text" id="filterInput" placeholder="Filter table rows...">
<table id="dataTable">
<thead>
<tr>
<th>Name</th>
<th>Age</th>
<th>City</th>
</tr>
</thead>
<tbody>
<tr>
<td>John Doe</td>
<td>25</td>
<td>New York</td>
</tr>
<tr>
<td>Jane Smith</td>
<td>30</td>
<td>Los Angeles</td>
</tr>
<tr>
<td>Mike Johnson</td>
<td>45</td>
<td>Chicago</td>
</tr>
<tr>
<td>艾米丽·戴维斯</td>
<td>22</td>
<td>休斯顿</td>
</tr>
</tbody>
</table>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.filter-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

input {
  padding: 10px;
  font-size: 16px;
  margin-bottom: 20px;
  width: 100%;
  box-sizing: border-box;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

th, td {
  padding: 10px;
  border: 1px solid #ccc;
}

thead {
  background-color: #ddd;
}
```

### JavaScript

```javascript
document.getElementById('filterInput').addEventListener('input', function() {
  const filter = this.value.toLowerCase();
  const rows = document.querySelectorAll('#dataTable tbody tr');
  rows.forEach(row => {
    const cells = row.querySelectorAll('td');
    let match = false;
    cells.forEach(cell => {
      if (cell.textContent.toLowerCase().includes(filter)) {
        match = true;
      }
    });
    row.style.display = match ? '' : 'none';
  });
});
```

## 模态弹窗

### 描述

在本练习中，学生将创建一个可以通过按钮打开和关闭的模态弹窗。本练习介绍如何处理点击事件、切换类以及动态更新`DOM`。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- `DOM`操作（显示和隐藏元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Modal Popup</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="modal-container">
    <button id="openModalButton">Open Modal</button>
    <div id="modal" class="modal">
      <div class="modal-content">
        <span id="closeModalButton" class="close-button">&times;</span>
        <h2>Modal Title</h2>
        <p>This is a simple modal popup.</p>
      </div>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.modal-container {
  text-align: center;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

.modal {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  position: relative;
}

.close-button {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 24px;
  cursor: pointer;
}

.modal.active {
  display: flex;
}
```

### JavaScript

```javascript
document.getElementById('openModalButton').addEventListener('click', function() {
  document.getElementById('modal').classList.add('active');
});

document.getElementById('closeModalButton').addEventListener('click', function() {
  document.getElementById('modal').classList.remove('active');
});

window.addEventListener('click', function(event) {
  const modal = document.getElementById('modal');
  if (event.target === modal) {
    modal.classList.remove('active');
  }
});
```

## 带计次的秒表

### 描述

在本练习中，学生将创建一个带计次功能的秒表。本练习介绍如何使用定时器、处理用户输入以及动态更新`DOM`。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 定时器操作
- `DOM`操作（添加和更新元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Stopwatch with Lap Times</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="stopwatch-container">
    <h1>Stopwatch</h1>
    <p id="stopwatchDisplay">00:00:00</p>
    <div class="buttons">
      <button id="startButton">Start</button>
      <button id="lapButton">Lap</button>
      <button id="resetButton">Reset</button>
    </div>
    <h2>Lap Times</h2>
    <ul id="laps"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.stopwatch-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#stopwatchDisplay {
  font-size: 36px;
  margin-bottom: 20px;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-bottom: 20px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 5px;
  border-bottom: 1px solid #ccc;
}
```

### JavaScript

```javascript
let timer;
let startTime;
let elapsedTime = 0;
let isRunning = false;

function updateDisplay() {
  const display = document.getElementById('stopwatchDisplay');
  const time = new Date(elapsedTime);
  const minutes = time.getUTCMinutes().toString().padStart(2, '0');
  const seconds = time.getUTCSeconds().toString().padStart(2, '0');
  const milliseconds = Math.floor(time.getUTCMilliseconds() / 10).toString().padStart(2, '0');
  display.textContent = `${minutes}:${seconds}:${milliseconds}`;
}

function startStopwatch() {
  if (!isRunning) {
    startTime = Date.now() - elapsedTime;
    timer = setInterval(function() {
      elapsedTime = Date.now() - startTime;
      updateDisplay();
    }, 10);
    isRunning = true;
  }
}

function resetStopwatch() {
  clearInterval(timer);
  elapsedTime = 0;
  updateDisplay();
  isRunning = false;
  document.getElementById('laps').innerHTML = '';
}

function lapStopwatch() {
  if (isRunning) {
    const lapTime = document.getElementById('stopwatchDisplay').textContent;
    const li = document.createElement('li');
    li.textContent = lapTime;
    document.getElementById('laps').appendChild(li);
  }
}

document.getElementById('startButton').addEventListener('click', startStopwatch);
document.getElementById('resetButton').addEventListener('click', resetStopwatch);
document.getElementById('lapButton').addEventListener('click', lapStopwatch);

updateDisplay();
```

## 带优先级的待办事项列表

### 描述

在本练习中，学生将创建一个为每个任务设置优先级的待办事项列表。本练习介绍如何处理表单输入、动态更新`DOM`以及使用 CSS 根据优先级设置元素样式。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- `DOM`操作（添加、更新和删除元素）



- 处理表单输入

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List with Priority</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="todo-container">
    <h1>To-Do List</h1>
    <form id="todoForm">
      <input type="text" id="taskInput" placeholder="Enter a new task" required>
      <select id="prioritySelect" required>
        <option value="high">High</option>
        <option value="medium">Medium</option>
        <option value="low">Low</option>
      </select>
      <button type="submit">Add Task</button>
    </form>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input, select, button {
  padding: 10px;
  font-size: 16px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 10px;
  margin: 5px 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
}

li.high {
  border-left: 5px solid red;
}

li.medium {
  border-left: 5px solid orange;
}

li.low {
  border-left: 5px solid green;
}

button.remove {
  background: none;
  border: none;
  color: red;
  cursor: pointer;
  font-size: 16px;
}
```

## JavaScript

```javascript
document.getElementById('todoForm').addEventListener('submit', function(event) {
  event.preventDefault();

  const taskInput = document.getElementById('taskInput');
  const prioritySelect = document.getElementById('prioritySelect');
  const taskText = taskInput.value;
  const priority = prioritySelect.value;

  if (taskText === '') return;

  const li = document.createElement('li');
  li.textContent = taskText;
  li.classList.add(priority);

  const removeButton = document.createElement('button');
  removeButton.textContent = 'Remove';
  removeButton.classList.add('remove');

  removeButton.addEventListener('click', function() {
    li.remove();
  });

  li.appendChild(removeButton);
  document.getElementById('taskList').appendChild(li);

  taskInput.value = '';
  prioritySelect.value = 'medium';
});
```

# 多项选择题测验应用

## 描述

在此练习中，学生将创建一个显示多项选择题并根据用户答案提供反馈的测验应用。本练习介绍如何处理用户输入、动态更新 DOM 以及提供反馈。

## 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新元素）
- 处理用户输入

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quiz App</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="quiz-container">
    <h1>Quiz App</h1>
    <div id="quiz"></div>
    <button id="submit">Submit</button>
    <div id="results"></div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.quiz-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 20px;
}
```

## JavaScript

```javascript
const quizContainer = document.getElementById('quiz');
const resultsContainer = document.getElementById('results');
const submitButton = document.getElementById('submit');

const myQuestions = [
  {
    question: "What is the capital of France?",
    answers: {
      a: "Berlin",
      b: "Madrid",
      c: "Paris"
    },
    correctAnswer: "c"
  },
  {
    question: "Who is the CEO of Tesla?",
    answers: {
      a: "Jeff Bezos",
      b: "Elon Musk",
      c: "Bill Gates"
    },
    correctAnswer: "b"
  },
  {
    question: "What is the smallest planet in our solar system?",
    answers: {
      a: "Mars",
      b: "Venus",
      c: "Mercury"
    },
    correctAnswer: "c"
  }
];

function buildQuiz() {
  const output = [];

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answers = [];

    for (letter in currentQuestion.answers) {
      answers.push(
        `<label>
          <input type="radio" name="question${questionNumber}" value="${letter}">
          ${letter} :
          ${currentQuestion.answers[letter]}
        </label>`
      );
    }

    output.push(
      `<div class="question"> ${currentQuestion.question} </div>
      <div class="answers"> ${answers.join('')} </div>`
    );
  });

  quizContainer.innerHTML = output.join('');
}

function showResults() {
  const answerContainers = quizContainer.querySelectorAll('.answers');
  let numCorrect = 0;

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answerContainer = answerContainers[questionNumber];
    const selector = `input[name=question${questionNumber}]:checked`;
    const userAnswer = (answerContainer.querySelector(selector) || {}).value;

    if (userAnswer === currentQuestion.correctAnswer) {
      numCorrect++;
      answerContainers[questionNumber].style.color = 'green';
    } else {
      answerContainers[questionNumber].style.color = 'red';
    }
  });

  resultsContainer.innerHTML = `${numCorrect} out of ${myQuestions.length}`;
}

buildQuiz();
submitButton.addEventListener('click', showResults);
```

# 简单绘图应用

## 描述

在此练习中，学生将创建一个简单的绘图应用，用户可以使用鼠标在画布上绘图。本练习介绍如何使用 HTML5 `<canvas>` 元素、处理鼠标事件以及绘制形状。

## 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- Canvas API
- 处理鼠标事件

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Drawing App</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="drawing-container">
    <h1>Simple Drawing App</h1>
    <canvas id="drawingCanvas" width="600" height="400"></canvas>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.drawing-container {
  text-align: center;
}

canvas {
  border: 1px solid #000;
  cursor: crosshair;
}
```

## JavaScript

```javascript
const canvas = document.getElementById('drawingCanvas');
const ctx = canvas.getContext('2d');
let drawing = false;

canvas.addEventListener('mousedown', () => drawing = true);
canvas.addEventListener('mouseup', () => drawing = false);
canvas.addEventListener('mouseout', () => drawing = false);
canvas.addEventListener('mousemove', draw);

function draw(event) {
  if (!drawing) return;

  ctx.lineWidth = 2;
  ctx.lineCap = 'round';
  ctx.strokeStyle = '#000';
  ctx.lineTo(
    event.clientX - canvas.offsetLeft,
    event.clientY - canvas.offsetTop
  );
  ctx.stroke();
  ctx.beginPath();
  ctx.moveTo(
    event.clientX - canvas.offsetLeft,
    event.clientY - canvas.offsetTop
  );
}
```

# 带计圈功能的秒表

## 描述

在此练习中，学生将创建一个带计圈功能的秒表，允许用户记录圈数时间。本练习介绍如何使用定时器、处理按钮点击以及动态更新 DOM。

## 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 使用定时器
- DOM 操作（添加和更新元素）

## HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Stopwatch with Laps</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="stopwatch-container">
    <h1>Stopwatch with Laps</h1>
    <p id="stopwatchDisplay">00:00:00</p>
    <div class="buttons">
      <button id="startButton">Start</button>
      <button id="lapButton">Lap</button>
      <button id="resetButton">Reset</button>
    </div>
    <h2>Lap Times</h2>
    <ul id="laps"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## CSS



```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.stopwatch-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
#stopwatchDisplay {
font-size: 36px;
margin-bottom: 20px;
}
.buttons {
display: flex;
justify-content: center;
gap: 10px;
margin-bottom: 20px;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 5px;
border-bottom: 1px solid #ccc;
}
```

## JavaScript

```javascript
let timer;
let startTime;
let elapsedTime = 0;
let isRunning = false;
function updateDisplay() {
const display = document.getElementById('stopwatchDisplay');
const time = new Date(elapsedTime);
const minutes = time.getUTCMinutes().toString().padStart(2, '0');
const seconds = time.getUTCSeconds().toString().padStart(2, '0');
const milliseconds = Math.floor(time.getUTCMilliseconds() / 10).toString().padStart(2, '0');
display.textContent = `${minutes}:${seconds}:${milliseconds}`;
}
function startStopwatch() {
if (!isRunning) {
startTime = Date.now() - elapsedTime;
timer = setInterval(function() {
elapsedTime = Date.now() - startTime;
updateDisplay();
}, 10);
isRunning = true;
}
}
function resetStopwatch() {
clearInterval(timer);
elapsedTime = 0;
updateDisplay();
isRunning = false;
document.getElementById('laps').innerHTML = '';
}
function lapStopwatch() {
if (isRunning) {
const lapTime = document.getElementById('stopwatchDisplay').textContent;
const li = document.createElement('li');
li.textContent = lapTime;
document.getElementById('laps').appendChild(li);
}
}
document.getElementById('startButton').addEventListener('click', startStopwatch);
document.getElementById('resetButton').addEventListener('click', resetStopwatch);
document.getElementById('lapButton').addEventListener('click', lapStopwatch);
updateDisplay();
```

## 费用追踪器

### 描述

在本练习中，学生将创建一个费用追踪器，允许用户添加带有描述和金额的费用。本练习介绍如何处理表单输入、动态更新 DOM 以及计算总计。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（添加和更新元素）
- 处理表单输入

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Expense Tracker</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="tracker-container">
<h1>Expense Tracker</h1>
<form id="expenseForm">
<input type="text" id="descriptionInput" placeholder="Enter description" required>
<input type="number" id="amountInput" placeholder="Enter amount" required>
<button type="submit">Add Expense</button>
</form>
<ul id="expenseList"></ul>
<p id="totalAmount">Total: $0.00</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.tracker-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
form {
display: flex;
flex-direction: column;
gap: 10px;
}
input, button {
padding: 10px;
font-size: 16px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 10px;
margin: 5px 0;
background-color: #fff;
border: 1px solid #ccc;
border-radius: 5px;
display: flex;
justify-content: space-between;
}
button.remove {
background: none;
border: none;
color: red;
cursor: pointer;
font-size: 16px;
}
p {
font-size: 18px;
margin-top: 20px;
}
```

### JavaScript

```javascript
document.getElementById('expenseForm').addEventListener('submit', function(event) {
event.preventDefault();
const descriptionInput = document.getElementById('descriptionInput');
const amountInput = document.getElementById('amountInput');
const description = descriptionInput.value;
const amount = parseFloat(amountInput.value);
if (description === '' || isNaN(amount)) return;
const li = document.createElement('li');
li.textContent = `${description}: $${amount.toFixed(2)}`;
const removeButton = document.createElement('button');
removeButton.textContent = 'Remove';
removeButton.classList.add('remove');
removeButton.addEventListener('click', function() {
li.remove();
updateTotal();
});
li.appendChild(removeButton);
document.getElementById('expenseList').appendChild(li);
updateTotal();
descriptionInput.value = '';
amountInput.value = '';
});
function updateTotal() {
const amounts = document.querySelectorAll('#expenseList li');
let total = 0;
amounts.forEach(li => {
const amount = parseFloat(li.textContent.split('$')[1]);
total += amount;
});
document.getElementById('totalAmount').textContent = `Total: $${total.toFixed(2)}`;
}
```

## 带分段计时的秒表

### 描述

在本练习中，学生将创建一个带分段计时功能的秒表，允许用户记录分段时间。本练习介绍如何使用定时器、处理按钮点击以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 使用定时器
- DOM 操作（添加和更新元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stopwatch with Split Times</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="stopwatch-container">
<h1>Stopwatch with Split Times</h1>
<p id="stopwatchDisplay">00:00:00</p>
<div class="buttons">
<button id="startButton">Start</button>
<button id="splitButton">Split</button>
<button id="resetButton">Reset</button>
</div>
<h2>Split Times</h2>
<ul id="splits"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.stopwatch-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
#stopwatchDisplay {
font-size: 36px;
margin-bottom: 20px;
}
.buttons {
display: flex;
justify-content: center;
gap: 10px;
margin-bottom: 20px;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 5px;
border-bottom: 1px solid #ccc;
}
```

### JavaScript

```javascript
let timer;
let startTime;
let elapsedTime = 0;
let isRunning = false;
function updateDisplay() {
const display = document.getElementById('stopwatchDisplay');
const time = new Date(elapsedTime);
const minutes = time.getUTCMinutes().toString().padStart(2, '0');
const seconds = time.getUTCSeconds().toString().padStart(2, '0');
const milliseconds = Math.floor(time.getUTCMilliseconds() / 10).toString().padStart(2, '0');
display.textContent = `${minutes}:${seconds}:${milliseconds}`;
}
function startStopwatch() {
if (!isRunning) {
startTime = Date.now() - elapsedTime;
timer = setInterval(function() {
elapsedTime = Date.now() - startTime;
updateDisplay();
}, 10);
isRunning = true;
}
}
function resetStopwatch() {
clearInterval(timer);
elapsedTime = 0;
updateDisplay();
isRunning = false;
document.getElementById('splits').innerHTML = '';
}
function splitStopwatch() {
if (isRunning) {
const splitTime = document.getElementById('stopwatchDisplay').textContent;
const li = document.createElement('li');
li.textContent = splitTime;
document.getElementById('splits').appendChild(li);
}
}
document.getElementById('startButton').addEventListener('click', startStopwatch);
document.getElementById('resetButton').addEventListener('click', resetStopwatch);
document.getElementById('splitButton').addEventListener('click', splitStopwatch);
updateDisplay();
```

## 多项选择题

### 1. 在动态表格筛选练习中，用于筛选表格行的事件是哪个？

a) `change`

b) `input`

c) `click`

d) `keydown`

**答案：**b) `input`

**解释：**当用户在筛选输入框中输入时，使用`input`事件实时筛选表格行。

### 2. 在模态弹窗练习中，用于显示模态弹窗的方法是哪个？

a) `display = 'block'`

b) `classList.add('active')`

c) `style.visibility = 'visible'`

d) `style.opacity = 1`

**答案：**b) `classList.add('active')`

**解释：**通过向模态元素添加`active`类，使用`classList.add('active')`方法显示模态弹窗。

### 3. 在“带计圈功能的秒表”练习中，哪个函数用于定期更新显示？

a) `setTimeout`

b) `setInterval`



c) `requestAnimationFrame`

d) `setImmediate`

答案：b) `setInterval`

解释：`setInterval` 函数用于每 10 毫秒定期更新显示。

在“带计圈功能的秒表”练习中，如何计算经过的时间？

a) `Date.now() - startTime`

b) `startTime - Date.now()`

c) `new Date().getTime() - startTime`

d) `startTime - new Date().getTime()`

答案：a) `Date.now() - startTime`

解释：经过的时间是通过当前时间（`Date.now()`）减去`startTime`计算得出的。

在“模态弹窗”练习中，当用户点击模态内容外部时会发生什么？

a) 什么也不会发生

b) 模态内容被隐藏

c) 模态弹窗被关闭

d) 模态内容被最小化

答案：c) 模态弹窗被关闭

解释：当用户点击模态内容外部时，通过从模态元素中移除`active`类来关闭模态弹窗。

在“带优先级的待办事项列表”练习中，优先级级别如何应用于任务？

a) 通过更改文本颜色

b) 通过添加边框

c) 通过添加 CSS 类

d) 通过更改字体大小

答案：c) 通过添加 CSS 类

解释：优先级级别通过根据所选优先级级别添加 CSS 类来应用于任务。

在“多项选择题测验应用”练习中，如何检索用户选择的答案？

a) 使用`getElementById`

b) 使用`querySelector`

c) 使用`innerHTML`

d) 使用`textContent`

答案：b) 使用`querySelector`

解释：`querySelector`方法用于从单选按钮中检索用户选择的答案。

在“带优先级的待办事项列表”练习中，哪个事件用于处理表单提交？

a) `click`

b) `submit`

c) `change`

d) `input`

答案：b) `submit`

解释：`submit`事件用于在添加带有优先级的新任务时处理表单提交。

在“简易绘图应用”练习中，哪个事件用于开始在画布上绘图？

a) `click`

b) `mousedown`

c) `mouseup`

d) `mousemove`

答案：b) `mousedown`

解释：当鼠标按钮按下时，`mousedown`事件用于开始在画布上绘图。

在“带计圈功能的秒表”练习中，调用哪个函数来记录计圈时间？

a) `startStopwatch`

b) `resetStopwatch`

c) `lapStopwatch`

d) `updateDisplay`

答案：c) `lapStopwatch`

解释：调用`lapStopwatch`函数来记录计圈时间并将其添加到计圈时间列表中。

在“简易绘图应用”练习中，`ctx.lineTo`方法的作用是什么？

a) 设置线条的起点

b) 绘制一条到指定坐标的线条

c) 清除画布

d) 用颜色填充画布

答案：b) 绘制一条到指定坐标的线条

解释：`ctx.lineTo`方法在画布上绘制一条到指定坐标的线条。

在“带计圈功能的秒表”练习中，`elapsedTime`变量的作用是什么？

a) 存储秒表的总经过时间

b) 存储秒表的开始时间

c) 存储秒表的计圈时间

d) 存储计时器的间隔 ID

答案：a) 存储秒表的总经过时间

解释：`elapsedTime`变量用于存储秒表的总经过时间，该时间会定期更新并显示。

在“费用追踪器”练习中，如何计算总金额？

a) 通过求和费用列表中的金额

b) 通过相乘费用列表中的金额

c) 通过相除费用列表中的金额

d) 通过相减费用列表中的金额

答案：a) 通过求和费用列表中的金额

解释：总金额是通过对费用列表中所有费用的金额求和计算得出的。

在“带分段计时功能的秒表”练习中，使用什么函数来记录分段时间？

a) `startStopwatch`

b) `resetStopwatch`

c) `splitStopwatch`

d) `updateDisplay`

答案：c) `splitStopwatch`

解释：`splitStopwatch`函数用于记录并显示秒表中的分段时间。

在“费用追踪器”练习中，如何将任务添加到费用列表？

a) 通过设置`innerHTML`

b) 通过设置`textContent`

c) 通过使用`appendChild`

d) 通过使用`innerText`

答案：c) 通过使用`appendChild`

解释：通过创建列表项元素并使用`appendChild`将其追加到费用列表中来添加任务。

在“带本地存储的待办事项列表”练习中，使用什么事件来确保在 DOM 完全加载后从本地存储加载任务？

A) `load`

B) `DOMContentLoaded`

C) `window.onload`

D) `ready`

答案：B) `DOMContentLoaded`

解释：`DOMContentLoaded`事件用于确保在 DOM 完全加载后加载任务，从而实现准确的任务显示。

在“带本地存储的待办事项列表”练习中，任务如何存储在本地存储中？

A) 作为纯文本

B) 作为 JSON 字符串

C) 作为数组

D) 作为对象

答案：B) 作为 JSON 字符串

解释：任务以 JSON 字符串形式存储，以便轻松保存和检索复杂的数据结构。

在“带本地存储的待办事项列表”练习中，使用什么方法来更新本地存储中的任务列表？

A) `localStorage.saveItem`

B) `localStorage.updateItem`

C) `localStorage.setItem`

D) `localStorage.putItem`

答案：C) `localStorage.setItem`

解释：`localStorage.setItem`方法用于更新本地存储中的任务列表。

在“BMI 计算器”练习中，身高输入使用什么单位？

A) 英寸

B) 米

C) 厘米

D) 英尺

答案：C) 厘米

解释：身高输入以厘米为单位，然后转换为米以进行 BMI 计算。

在“数字时钟”练习中，使用什么方法每秒更新时钟显示？

A) `setTimeout`

B) `setInterval`

C) `requestAnimationFrame`

D) `clearInterval`

答案：B) `setInterval`

解释：`setInterval`方法用于每秒更新时钟显示。

在“响应式导航菜单”练习中，哪个 CSS 规则用于根据屏幕宽度应用样式？

A) `@import`

B) `@media`

C) `@keyframes`

D) `@font-face`

答案：B) `@media`

解释：CSS 中的`@media`规则用于根据屏幕宽度应用样式，从而实现响应式设计。

在“测验应用”练习中，如何显示测验问题和答案？

A) 使用`<div>`元素

B) 使用`<table>`元素

C) 使用`<form>`元素

D) 使用`<span>`元素

答案：A) 使用`<div>`元素

解释：使用`<div>`元素显示测验问题和答案，有效构建界面。

在“番茄钟计时器”练习中，使用什么方法来停止计时器？

A) `clearTimeout`

B) `clearInterval`

C) `stopTimer`

D) `pauseTimer`

答案：B) `clearInterval`

解释：`clearInterval`方法通过清除间隔来停止计时器。

在“自定义时间倒计时器”练习中，如何从表单中读取用户的输入时间？

A) 使用`parseFloat`

B) 使用`parseInt`

C) 使用`Number`

D) 使用`getValue`

答案：B) 使用`parseInt`

解释：使用`parseInt`读取用户的输入时间，以确保输入被视为整数。

在“动态表格筛选”练习中，哪个事件用于触发表格行的筛选？

A) `click`

B) `input`

C) `change`

D) `keyup`

答案：B) 使用`input`

解释：`input`事件用于根据用户在筛选字段中的输入触发表格行的筛选。

## 带用户输入的倒计时器

### 描述

在此练习中，学生将创建一个倒计时器，允许用户输入秒数并启动计时器。本练习介绍如何处理表单输入、使用计时器以及动态更新 DOM。

### 涵盖的主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 使用计时器
- 处理表单输入
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
```

### 完整 HTML

```html
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Countdown Timer with User Input</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="timer-container">
<h1>Countdown Timer</h1>
<form id="timerForm">
<input type="number" id="secondsInput" placeholder="Enter seconds" required>
<button type="submit">Start Timer</button>
</form>
<p id="timerDisplay">0:00</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.timer-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
display: flex;
flex-direction: column;
gap: 10px;
margin-bottom: 20px;
}
input, button {
padding: 10px;
font-size: 16px;
}
p {
font-size: 36px;
margin-top: 20px;
}
```

### JavaScript

```javascript
let timer;
let timeLeft;
document.getElementById('timerForm').addEventListener('submit', function(event) {
event.preventDefault();
clearInterval(timer);
timeLeft = parseInt(document.getElementById('secondsInput').value);
startTimer();
});
function startTimer() {
timer = setInterval(function() {
if (timeLeft > 0) {
timeLeft--;
updateDisplay();
} else {
clearInterval(timer);
alert('Time is up!');
}
}, 1000);
}
function updateDisplay() {
const minutes = Math.floor(timeLeft / 60).toString().padStart(1, '0');
const seconds = (timeLeft % 60).toString().padStart(2, '0');
document.getElementById('timerDisplay').textContent = `${minutes}:${seconds}`;
}
updateDisplay();
```

## 交互式测验应用

### 描述

在本练习中，学生将创建一个交互式测验应用，显示多项选择题并提供即时反馈。本练习介绍如何处理表单输入、动态更新 DOM 以及提供反馈。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- DOM 操作（更新元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Quiz App</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="quiz-container">
<h1>Quiz App</h1>
<div id="quiz"></div>
<button id="submit">Submit</button>
<div id="results"></div>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.quiz-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
margin-top: 20px;
}
```

### JavaScript




```javascript
const quizContainer = document.getElementById('quiz');
const resultsContainer = document.getElementById('results');
const submitButton = document.getElementById('submit');
const myQuestions = [
  {
    question: "What is the capital of France?",
    answers: {
      a: "Berlin",
      b: "Madrid",
      c: "Paris"
    },
    correctAnswer: "c"
  },
  {
    question: "Who is the CEO of Tesla?",
    answers: {
      a: "Jeff Bezos",
      b: "Elon Musk",
      c: "Bill Gates"
    },
    correctAnswer: "b"
  },
  {
    question: "What is the smallest planet in our solar system?",
    answers: {
      a: "Mars",
      b: "Venus",
      c: "Mercury"
    },
    correctAnswer: "c"
  }
];

function buildQuiz() {
  const output = [];

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answers = [];

    for (letter in currentQuestion.answers) {
      answers.push(
        `<label>
          <input type="radio" name="question${questionNumber}" value="${letter}">
          ${letter} :
          ${currentQuestion.answers[letter]}
        </label>`
      );
    }

    output.push(
      `<div class="question"> ${currentQuestion.question} </div>
      <div class="answers"> ${answers.join('')} </div>`
    );
  });

  quizContainer.innerHTML = output.join('');
}

function showResults() {
  const answerContainers = quizContainer.querySelectorAll('.answers');
  let numCorrect = 0;

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answerContainer = answerContainers[questionNumber];
    const selector = `input[name=question${questionNumber}]:checked`;
    const userAnswer = (answerContainer.querySelector(selector) || {}).value;

    if (userAnswer === currentQuestion.correctAnswer) {
      numCorrect++;
      answerContainers[questionNumber].style.color = 'green';
    } else {
      answerContainers[questionNumber].style.color = 'red';
    }
  });

  resultsContainer.innerHTML = `${numCorrect} out of ${myQuestions.length}`;
}

buildQuiz();
submitButton.addEventListener('click', showResults);
```

## 带本地存储的购物清单

**描述：** 在本练习中，学生将创建一个购物清单，将商品保存到本地存储中，以便在页面刷新后仍然保留。本练习介绍如何处理表单输入、动态更新 DOM 以及使用本地存储。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 本地存储
- DOM 操作（添加、更新和删除元素）
- 处理表单输入

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Shopping List with Local Storage</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="list-container">
    <h1>Shopping List</h1>
    <form id="shoppingForm">
      <input type="text" id="itemInput" placeholder="Enter a new item" required>
      <button type="submit">Add Item</button>
    </form>
    <ul id="itemList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.list-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input,
button {
  padding: 10px;
  font-size: 16px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 10px;
  margin: 5px 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
}

button.remove {
  background: none;
  border: none;
  color: red;
  cursor: pointer;
  font-size: 16px;
}
```

### JavaScript

```javascript
document.addEventListener('DOMContentLoaded', function() {
  const itemList = document.getElementById('itemList');
  const items = JSON.parse(localStorage.getItem('items')) || [];

  items.forEach(item => {
    addItemToDOM(item);
  });

  document.getElementById('shoppingForm').addEventListener('submit', function(event) {
    event.preventDefault();

    const itemInput = document.getElementById('itemInput');
    const itemText = itemInput.value;

    if (itemText === '') return;

    addItemToDOM(itemText);
    items.push(itemText);
    localStorage.setItem('items', JSON.stringify(items));
    itemInput.value = '';
  });

  function addItemToDOM(itemText) {
    const li = document.createElement('li');
    li.textContent = itemText;

    const removeButton = document.createElement('button');
    removeButton.textContent = 'Remove';
    removeButton.classList.add('remove');

    removeButton.addEventListener('click', function() {
      li.remove();

      const index = items.indexOf(itemText);

      if (index !== -1) {
        items.splice(index, 1);
        localStorage.setItem('items', JSON.stringify(items));
      }
    });

    li.appendChild(removeButton);
    itemList.appendChild(li);
  }
});
```

## 响应式导航栏

**描述：**（原文未提供进一步内容。）

在本练习中，学生将创建一个响应式导航栏，该导航栏在小屏幕上会折叠成汉堡菜单。本练习介绍了如何处理 CSS 媒体查询、JavaScript 事件监听器和 DOM 操作。

**涵盖主题：**

- HTML 结构
- CSS 样式
- CSS 媒体查询
- JavaScript 事件监听器
- DOM 操作（切换类）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Navbar</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <nav class="navbar">
    <div class="brand-title">Brand</div>
    <a href="#" class="toggle-button">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </a>
    <div class="navbar-links">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
  </nav>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  padding: 10px;
}

.brand-title {
  font-size: 1.5em;
  color: white;
}

.navbar-links {
  height: 100%;
}

.navbar-links ul {
  display: flex;
  margin: 0;
  padding: 0;
  list-style: none;
}

.navbar-links li {
  margin-left: 10px;
}

.navbar-links a {
  color: white;
  text-decoration: none;
  padding: 5px 10px;
}

.toggle-button {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.toggle-button .bar {
  width: 25px;
  height: 3px;
  background-color: white;
  margin: 2px 0;
}

@media (max-width: 768px) {
  .toggle-button {
    display: flex;
  }

  .navbar-links {
    display: none;
    width: 100%;
  }

  .navbar-links ul {
    flex-direction: column;
  }

  .navbar-links ul li {
    text-align: center;
  }

  .navbar-links.active {
    display: flex;
  }
}
```

### JavaScript

```javascript
const toggleButton = document.querySelector('.toggle-button');
const navbarLinks = document.querySelector('.navbar-links');

toggleButton.addEventListener('click', () => {
  navbarLinks.classList.toggle('active');
});
```

## 猜数字游戏

### 描述

在本练习中，学生将创建一个猜数字游戏，用户需要猜测某个范围内随机生成的数字。本练习介绍了如何处理表单输入、生成随机数以及提供反馈。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 生成随机数
- 处理表单输入
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Random Number Guessing Game</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="game-container">
    <h1>Random Number Guessing Game</h1>
    <form id="guessForm">
      <input type="number" id="guessInput" placeholder="Enter your guess" required>
      <button type="submit">Submit Guess</button>
    </form>
    <p id="resultDisplay">Guess a number between 1 and 100.</p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.game-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}

input,
button {
  padding: 10px;
  font-size: 16px;
}

p {
  font-size: 18px;
  margin-top: 20px;
}
```

### JavaScript




```javascript
const randomNumber = Math.floor(Math.random() * 100) + 1;
const guessForm = document.getElementById('guessForm');
const guessInput = document.getElementById('guessInput');
const resultDisplay = document.getElementById('resultDisplay');

guessForm.addEventListener('submit', function(event) {
  event.preventDefault();
  const userGuess = parseInt(guessInput.value);
  if (userGuess === randomNumber) {
    resultDisplay.textContent = 'Congratulations! You guessed the correct number.';
  } else if (userGuess < randomNumber) {
    resultDisplay.textContent = 'Too low! Try again.';
  } else if (userGuess > randomNumber) {
    resultDisplay.textContent = 'Too high! Try again.';
  }
  guessInput.value = '';
});
```

### 井字棋游戏

#### 描述

在本练习中，学生将创建一个简单的井字棋游戏，两名玩家可以相互对战。本练习介绍了如何处理点击事件、动态更新 DOM 以及检查获胜条件。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理点击事件
- DOM 操作（更新元素）
- 检查获胜条件

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tic-Tac-Toe Game</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="game-container">
    <h1>Tic-Tac-Toe</h1>
    <div id="gameBoard">
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
      <div class="cell" data-cell></div>
    </div>
    <p id="gameStatus">Player X's turn</p>
    <button id="restartButton">Restart Game</button>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.game-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#gameBoard {
  display: grid;
  grid-template-columns: repeat(3, 100px);
  grid-template-rows: repeat(3, 100px);
  gap: 5px;
}

.cell {
  width: 100px;
  height: 100px;
  background-color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 36px;
  cursor: pointer;
  border: 1px solid #ccc;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 20px;
}

p {
  font-size: 18px;
  margin-top: 20px;
}
```

#### JavaScript

```javascript
const cells = document.querySelectorAll('[data-cell]');
const gameStatus = document.getElementById('gameStatus');
const restartButton = document.getElementById('restartButton');
let isXTurn = true;

const winningCombinations = [
  [0, 1, 2],
  [3, 4, 5],
  [6, 7, 8],
  [0, 3, 6],
  [1, 4, 7],
  [2, 5, 8],
  [0, 4, 8],
  [2, 4, 6]
];

startGame();

restartButton.addEventListener('click', startGame);

function startGame() {
  isXTurn = true;
  gameStatus.textContent = "Player X's turn";
  cells.forEach(cell => {
    cell.classList.remove('x');
    cell.classList.remove('o');
    cell.removeEventListener('click', handleClick);
    cell.addEventListener('click', handleClick, { once: true });
  });
}

function handleClick(e) {
  const cell = e.target;
  const currentClass = isXTurn ? 'x' : 'o';
  placeMark(cell, currentClass);
  if (checkWin(currentClass)) {
    endGame(false);
  } else if (isDraw()) {
    endGame(true);
  } else {
    swapTurns();
    updateStatus();
  }
}

function placeMark(cell, currentClass) {
  cell.classList.add(currentClass);
}

function swapTurns() {
  isXTurn = !isXTurn;
}

function updateStatus() {
  gameStatus.textContent = isXTurn ? "Player X's turn" : "Player O's turn";
}

function checkWin(currentClass) {
  return winningCombinations.some(combination => {
    return combination.every(index => {
      return cells[index].classList.contains(currentClass);
    });
  });
}

function isDraw() {
  return [...cells].every(cell => {
    // 注意：原文此处未完整，但保留原样
  });
}
```

```javascript
return cell.classList.contains('x') || cell.classList.contains('o');

});

}

function endGame(draw) {

if (draw) {

gameStatus.textContent = "It's a draw!";

} else {

gameStatus.textContent = isXTurn ? "Player X wins!" : "Player O wins!";

}

}
```

### 计算器

#### 描述

在此练习中，学生将创建一个简单的计算器，执行基本的算术运算（加法、减法、乘法、除法）。本练习介绍如何处理按钮点击、执行计算以及动态更新 DOM。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理按钮点击
- 执行计算
- DOM 操作（更新文本内容）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="calculator-container">
    <h1>Calculator</h1>
    <div id="calculator">
      <div id="display">0</div>
      <button class="btn" data-value="7">7</button>
      <button class="btn" data-value="8">8</button>
      <button class="btn" data-value="9">9</button>
      <button class="btn" data-value="/">/</button>
      <button class="btn" data-value="4">4</button>
      <button class="btn" data-value="5">5</button>
      <button class="btn" data-value="6">6</button>
      <button class="btn" data-value="*">*</button>
      <button class="btn" data-value="1">1</button>
      <button class="btn" data-value="2">2</button>
      <button class="btn" data-value="3">3</button>
      <button class="btn" data-value="-">-</button>
      <button class="btn" data-value="0">0</button>
      <button class="btn" data-value=".">.</button>
      <button class="btn" id="clear">C</button>
      <button class="btn" data-value="+">+</button>
      <button class="btn" id="equals">=</button>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.calculator-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#calculator {
  display: grid;
  grid-template-columns: repeat(4, 50px);
  gap: 10px;
}

#display {
  grid-column: span 4;
  padding: 20px;
  background-color: #fff;
  border: 1px solid #ccc;
  text-align: right;
  font-size: 24px;
  border-radius: 5px;
}

.btn {
  padding: 20px;
  font-size: 18px;
  cursor: pointer;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.btn:hover {
  background-color: #e0e0e0;
}
```

#### JavaScript

```javascript
const display = document.getElementById('display');
const buttons = Array.from(document.getElementsByClassName('btn'));

buttons.forEach(button => {
  button.addEventListener('click', function() {
    const value = this.getAttribute('data-value');
    if (value === null) return;
    switch(value) {
      case 'C':
        display.textContent = '0';
        break;
      case '=':
        try {
          display.textContent = eval(display.textContent);
        } catch {
          display.textContent = 'Error';
        }
        break;
      default:
        if (display.textContent === '0' || display.textContent === 'Error') {
          display.textContent = value;
        } else {
          display.textContent += value;
        }
    }
  });
});

document.getElementById('clear').addEventListener('click', () => {
  display.textContent = '0';
});

document.getElementById('equals').addEventListener('click', () => {
  try {
    display.textContent = eval(display.textContent);
  } catch {
    display.textContent = 'Error';
  }
});
```

### 待办事项列表

#### 描述

在此练习中，学生将创建一个简单的待办事项列表，允许用户添加和删除任务。本练习介绍如何处理表单输入、动态更新 DOM 以及管理项目列表。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- DOM 操作（添加和删除元素）
- 管理项目列表

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="todo-container">
    <h1>To-Do List</h1>
    <form id="todoForm">
      <input type="text" id="taskInput" placeholder="Enter a new task" required>
      <button type="submit">Add Task</button>
    </form>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

#### CSS



```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input,
button {
  padding: 10px;
  font-size: 16px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 10px;
  margin: 5px 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
}

button.remove {
  background: none;
  border: none;
  color: red;
  cursor: pointer;
  font-size: 16px;
}
```

## JavaScript

```javascript
document.getElementById('todoForm').addEventListener('submit', function (event) {
  event.preventDefault();

  const taskInput = document.getElementById('taskInput');
  const taskText = taskInput.value;

  if (taskText === '') return;

  const li = document.createElement('li');
  li.textContent = taskText;

  const removeButton = document.createElement('button');
  removeButton.textContent = 'Remove';
  removeButton.classList.add('remove');

  removeButton.addEventListener('click', function () {
    li.remove();
  });

  li.appendChild(removeButton);
  document.getElementById('taskList').appendChild(li);
  taskInput.value = '';
});
```

## 多项选择题

在“随机数字猜谜游戏”练习中，当用户猜对数字时会发生什么？

a) 输入被清空

b) 显示祝贺消息

c) 页面重新加载

d) 生成一个新的随机数字

答案：b) 显示祝贺消息

解释：当用户猜对数字时，会显示一条祝贺消息。

在“井字棋游戏”练习中，使用哪个方法来检查获胜条件？

a) `checkWin`

b) `isDraw`

c) `placeMark`

d) `swapTurns`

答案：a) `checkWin`

解释：`checkWin` 方法通过将当前棋盘状态与获胜组合进行比较，来检查是否有玩家获胜。

在“随机数字猜谜游戏”练习中，使用哪个事件来处理表单提交？

a) `click`

b) `submit`

c) `change`

d) `input`

答案：b) `submit`

解释：`submit` 事件用于处理表单提交并处理用户的猜测。

在“井字棋游戏”练习中，当游戏以平局结束时会发生什么？

a) 游戏自动重新开始

b) 游戏显示平局消息

c) 游戏高亮显示获胜组合

d) 游戏停止响应

答案：b) 游戏显示平局消息

解释：当游戏以平局结束时，会显示一条表示平局的消息。

在“计算器”练习中，使用哪个事件来处理按钮点击？

a) `click`

b) `submit`

c) `change`

d) `input`

答案：a) `click`

解释：`click` 事件用于处理按钮点击并执行相应操作。

在“待办事项列表”练习中，当点击任务的“删除”按钮时会发生什么？

a) 任务被划掉

b) 任务从列表中移除

c) 任务被编辑

d) 任务被标记为已完成

答案：b) 任务从列表中移除

解释：点击“删除”按钮会将任务从列表中移除。

在“待办事项列表”练习中，`taskInput` 元素的用途是什么？

a) 输入任务描述

b) 输入任务截止日期

c) 显示任务总数

d) 移除一个任务

答案：a) 输入任务描述

解释：`taskInput` 元素用于输入要添加到列表中的新任务的描述。

在倒计时器练习中，哪个 HTML 标签用于创建表单？

a) `<div>`

b) `<form>`

c) `<input>`

d) `<button>`

答案：b) `<form>`

解释：`<form>` 标签用于创建供用户输入的 HTML 表单。

在倒计时器练习中，使用哪个事件监听器来阻止表单的默认行为？

a) `click`

b) `change`

c) `submit`

d) `input`

答案：c) `submit`

解释：使用 `submit` 事件监听器来阻止表单的默认行为，并通过 JavaScript 处理表单提交。

在倒计时器练习中，使用什么方法将用户输入转换为整数？

a) `parseFloat()`

b) `toString()`

c) `parseInt()`

d) `Number()`

答案：c) `parseInt()`

解释：`parseInt()` 方法用于将用户输入转换为整数。

在倒计时器练习中，哪个函数被重复调用来更新计时器显示？

a) `setTimeout()`

b) `clearInterval()`

c) `setInterval()`

d) `updateDisplay()`

答案：c) `setInterval()`

解释：`setInterval()` 函数被重复调用，每秒更新一次计时器显示。

在交互式测验应用练习中，使用什么标签来包含问题和答案？

a) `<form>`

b) `<div>`

c) `<span>`

d) `<section>`

答案：b) `<div>`

解释：`<div>` 标签用于包含问题和答案。

在交互式测验应用练习中，如何指示正确答案？

a) 通过更改背景颜色

b) 通过添加勾选图标

c) 通过将文本颜色更改为绿色

d) 通过在答案下方显示一条消息

答案：c) 通过将文本颜色更改为绿色

解释：正确答案通过将文本颜色更改为绿色来指示。

使用什么方法将购物清单项目存储在本地存储中？

a) `localStorage.getItem()`

b) `localStorage.setItem()`

c) `localStorage.save()`

d) `localStorage.store()`

答案：b) `localStorage.setItem()`

解释：`localStorage.setItem()` 方法用于将购物清单项目存储在本地存储中。

页面加载时，使用哪个事件监听器从本地存储加载项目？

a) `load`

b) `DOMContentLoaded`

c) `ready`

d) `initialize`

答案：b) `DOMContentLoaded`

解释：`DOMContentLoaded` 事件监听器用于在页面加载时从本地存储加载项目。

在响应式导航栏练习中，哪个 CSS 属性用于在较小屏幕上隐藏导航链接？

a) `visibility`

b) `display`

c) `opacity`

d) `position`

答案：b) `display`

解释：通过将 `display` 属性设置为 `none`，可以在较小屏幕上隐藏导航链接。

在响应式导航栏练习中，切换哪个类来显示或隐藏导航栏链接？

a) `show`

b) `toggle`

c) `active`

d) `visible`

答案：c) `active`

解释：当点击汉堡菜单时，切换 `active` 类来显示或隐藏导航栏链接。

## 闪卡应用

### 描述

在此练习中，学生将创建一个闪卡应用，显示问题并在点击时揭示答案。本练习介绍如何处理点击事件、管理状态以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理点击事件
- DOM 操作（更新文本内容）
- 状态管理

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flashcard App</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="flashcard-container">
    <h1>Flashcard App</h1>
    <div id="flashcard" class="flashcard">
      <p id="flashcardContent">Click to reveal the answer</p>
    </div>
    <button id="nextButton">Next</button>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.flashcard-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.flashcard {
  width: 300px;
  height: 200px;
  background-color: white;
  border: 1px solid #ccc;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 24px;
  cursor: pointer;
  margin-bottom: 20px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
```

### JavaScript

```javascript
const flashcards = [
  { question: 'What is the capital of France?', answer: 'Paris' },
  { question: 'What is 2 + 2?', answer: '4' },
  { question: 'What is the capital of Spain?', answer: 'Madrid' }
];

let currentFlashcardIndex = 0;

const flashcardContent = document.getElementById('flashcardContent');
const flashcard = document.getElementById('flashcard');

function showFlashcard(index) {
  flashcardContent.textContent = flashcards[index].question;
  flashcard.dataset.flipped = 'false';
}

flashcard.addEventListener('click', () => {
  if (flashcard.dataset.flipped === 'false') {
    flashcardContent.textContent = flashcards[currentFlashcardIndex].answer;
    flashcard.dataset.flipped = 'true';
  } else {
    flashcardContent.textContent = flashcards[currentFlashcardIndex].question;
    flashcard.dataset.flipped = 'false';
  }
});

document.getElementById('nextButton').addEventListener('click', () => {
  currentFlashcardIndex = (currentFlashcardIndex + 1) % flashcards.length;
  showFlashcard(currentFlashcardIndex);
});

showFlashcard(currentFlashcardIndex);
```

## 带反馈的测验应用

### 描述

在此练习中，学生将创建一个带反馈的测验应用，显示多项选择题并根据用户的答案提供反馈。本练习介绍如何处理用户输入、动态更新 DOM 以及提供反馈。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新元素）
- 处理用户输入

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quiz App with Feedback</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="quiz-container">
    <h1>Quiz App</h1>
    <div id="quiz"></div>
    <button id="submit">Submit</button>
    <div id="results"></div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.quiz-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 20px;
}
```

### JavaScript



```javascript
const quizContainer = document.getElementById('quiz');
const resultsContainer = document.getElementById('results');
const submitButton = document.getElementById('submit');
const myQuestions = [
  {
    question: "What is the capital of France?",
    answers: {
      a: "Berlin",
      b: "Madrid",
      c: "Paris"
    },
    correctAnswer: "c"
  },
  {
    question: "Who is the CEO of Tesla?",
    answers: {
      a: "Jeff Bezos",
      b: "Elon Musk",
      c: "Bill Gates"
    },
    correctAnswer: "b"
  },
  {
    question: "What is the smallest planet in our solar system?",
    answers: {
      a: "Mars",
      b: "Venus",
      c: "Mercury"
    },
    correctAnswer: "c"
  }
];

function buildQuiz() {
  const output = [];

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answers = [];

    for (letter in currentQuestion.answers) {
      answers.push(
        `<label>
          <input type="radio" name="question${questionNumber}" value="${letter}">
          ${letter} :
          ${currentQuestion.answers[letter]}
        </label>`
      );
    }

    output.push(
      `<div class="question"> ${currentQuestion.question} </div>`
    );
  });
}
```

### 带优先级的待办事项列表

**描述：**

在此练习中，学生将创建一个待办事项列表，并为每个任务设置优先级级别。本练习介绍如何处理表单输入、动态更新 DOM，以及使用 CSS 根据优先级设置元素样式。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（添加、更新和删除元素）
- 处理表单输入

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List with Priorities</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="todo-container">
    <h1>To-Do List</h1>
    <form id="todoForm">
      <input type="text" id="taskInput" placeholder="Enter a new task" required>
      <select id="prioritySelect" required>
        <option value="high">High</option>
        <option value="medium">Medium</option>
        <option value="low">Low</option>
      </select>
      <button type="submit">Add Task</button>
    </form>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input,
select,
button {
  padding: 10px;
  font-size: 16px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 10px;
  margin: 5px 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
}

li.high {
  border-left: 5px solid red;
}

li.medium {
  border-left: 5px solid orange;
}

li.low {
  border-left: 5px solid green;
}

button.remove {
  background: none;
  border: none;
  color: red;
  cursor: pointer;
  font-size: 16px;
}
```

#### JavaScript

```javascript
document.getElementById('todoForm').addEventListener('submit', function(event) {
  event.preventDefault();

  const taskInput = document.getElementById('taskInput');
  const prioritySelect = document.getElementById('prioritySelect');
  const taskText = taskInput.value;
  const priority = prioritySelect.value;

  if (taskText === '') return;

  const li = document.createElement('li');
  li.textContent = taskText;
  li.classList.add(priority);

  const removeButton = document.createElement('button');
  removeButton.textContent = 'Remove';
  removeButton.classList.add('remove');

  removeButton.addEventListener('click', function() {
    li.remove();
  });

  li.appendChild(removeButton);
  document.getElementById('taskList').appendChild(li);

  taskInput.value = '';
  prioritySelect.value = 'medium';
});
```

### 带暂停/恢复功能的倒计时器

**描述：**

在此练习中，学生将创建一个可以暂停和恢复的倒计时器。本练习介绍如何处理表单输入、使用定时器以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 使用定时器
- DOM 操作（更新文本内容）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Countdown Timer with Pause/Resume</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="timer-container">
    <h1>Countdown Timer</h1>
    <form id="timerForm">
      <input type="number" id="secondsInput" placeholder="Enter seconds" required>
      <button type="submit">Start Timer</button>
    </form>
    <p id="timerDisplay">0:00</p>
    <button id="pauseButton" disabled>Pause</button>
    <button id="resumeButton" disabled>Resume</button>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.timer-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}

input,
button {
  padding: 10px;
  font-size: 16px;
}

p {
  font-size: 36px;
  margin-top: 20px;
}
```

#### JavaScript

```javascript
let timer;
let timeLeft;
let isPaused = false;

document.getElementById('timerForm').addEventListener('submit', function(event) {
  event.preventDefault();

  clearInterval(timer);
  timeLeft = parseInt(document.getElementById('secondsInput').value);
  isPaused = false;
  startTimer();

  document.getElementById('pauseButton').disabled = false;
  document.getElementById('resumeButton').disabled = true;
});

document.getElementById('pauseButton').addEventListener('click', function() {
  clearInterval(timer);
  isPaused = true;

  document.getElementById('pauseButton').disabled = true;
  document.getElementById('resumeButton').disabled = false;
});

document.getElementById('resumeButton').addEventListener('click', function() {
  if (isPaused) {
    startTimer();

    document.getElementById('pauseButton').disabled = false;
    document.getElementById('resumeButton').disabled = true;
  }
});

function startTimer() {
  timer = setInterval(function() {
    if (timeLeft > 0) {
      timeLeft--;
      updateDisplay();
    } else {
      clearInterval(timer);
      alert('Time is up!');
    }
  }, 1000);
}

function updateDisplay() {
  const minutes = Math.floor(timeLeft / 60).toString().padStart(1, '0');
  const seconds = (timeLeft % 60).toString().padStart(2, '0');

  document.getElementById('timerDisplay').textContent = `${minutes}:${seconds}`;
}

updateDisplay();
```

### 测验应用

**描述：**

在此练习中，学生将创建一个测验应用，显示多项选择题并根据用户的答案提供反馈。本练习介绍如何处理用户输入、动态更新 DOM 以及提供反馈。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- DOM 操作（更新元素）
- 处理用户输入

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quiz App</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="quiz-container">
    <h1>Quiz App</h1>
    <div id="quiz"></div>
    <button id="submit">Submit</button>
    <div id="results"></div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.quiz-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 20px;
}
```

#### JavaScript



```javascript
const quizContainer = document.getElementById('quiz');
const resultsContainer = document.getElementById('results');
<div class="answers"> ${answers.join('')} </div>`

);
});
quizContainer.innerHTML = output.join('');
}
function showResults() {
const answerContainers = quizContainer.querySelectorAll('.answers');
let numCorrect = 0;
myQuestions.forEach((currentQuestion, questionNumber) => {
const answerContainer = answerContainers[questionNumber];
const selector = `input[name=question${questionNumber}]:checked`;
const userAnswer = (answerContainer.querySelector(selector) || {}).value;
if (userAnswer === currentQuestion.correctAnswer) {
numCorrect++;
answerContainers[questionNumber].style.color = 'green';
} else {
answerContainers[questionNumber].style.color = 'red';
}
});
resultsContainer.innerHTML = `${numCorrect} out of ${myQuestions.length}`;
}
buildQuiz();
submitButton.addEventListener('click', showResults);
```

```javascript
const submitButton = document.getElementById('submit');

const myQuestions = [
  {
    question: "What is the capital of France?",
    answers: {
      a: "Berlin",
      b: "Madrid",
      c: "Paris"
    },
    correctAnswer: "c"
  },
  {
    question: "Who is the CEO of Tesla?",
    answers: {
      a: "Jeff Bezos",
      b: "Elon Musk",
      c: "Bill Gates"
    },
    correctAnswer: "b"
  },
  {
    question: "What is the smallest planet in our solar system?",
    answers: {
      a: "Mars",
      b: "Venus",
      c: "Mercury"
    },
    correctAnswer: "c"
  }
];

function buildQuiz() {
  const output = [];

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answers = [];

    for (letter in currentQuestion.answers) {
      answers.push(
        `<label>
<input type="radio" name="question${questionNumber}" value="${letter}">
${letter} :
${currentQuestion.answers[letter]}
</label>`
      );
    }

    output.push(
      `<div class="question"> ${currentQuestion.question} </div>
<div class="answers"> ${answers.join('')} </div>`
    );
  });

  quizContainer.innerHTML = output.join('');
}

function showResults() {
  const answerContainers = quizContainer.querySelectorAll('.answers');
  let numCorrect = 0;

  myQuestions.forEach((currentQuestion, questionNumber) => {
    const answerContainer = answerContainers[questionNumber];
    const selector = `input[name=question${questionNumber}]:checked`;
    const userAnswer = (answerContainer.querySelector(selector) || {}).value;

    if (userAnswer === currentQuestion.correctAnswer) {
      numCorrect++;
      answerContainers[questionNumber].style.color = 'green';
    } else {
      answerContainers[questionNumber].style.color = 'red';
    }
  });

  resultsContainer.innerHTML = `${numCorrect} out of ${myQuestions.length}`;
}

buildQuiz();

submitButton.addEventListener('click', showResults);
```

## 带截止日期的待办事项列表

### 描述

在此练习中，学生将创建一个包含每项任务截止日期的待办事项列表。本练习介绍如何处理表单输入、动态更新 DOM 以及管理项目列表。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- DOM 操作（添加和删除元素）
- 管理项目列表

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List with Due Dates</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="todo-container">
    <h1>To-Do List</h1>
    <form id="todoForm">
      <input type="text" id="taskInput" placeholder="Enter a new task" required>
      <input type="date" id="dueDateInput" required>
      <button type="submit">Add Task</button>
    </form>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input,
button {
  padding: 10px;
  font-size: 16px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 10px;
  margin: 5px 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
}

button.remove {
  background: none;
  border: none;
  color: red;
  cursor: pointer;
  font-size: 16px;
}
```

### JavaScript

```javascript
document.getElementById('todoForm').addEventListener('submit', function(event) {
  event.preventDefault();

  const taskInput = document.getElementById('taskInput');
  const dueDateInput = document.getElementById('dueDateInput');
  const taskText = taskInput.value;
  const dueDate = dueDateInput.value;

  if (taskText === '' || dueDate === '') return;

  const li = document.createElement('li');
  li.textContent = `${taskText} - Due: ${dueDate}`;

  const removeButton = document.createElement('button');
  removeButton.textContent = 'Remove';
  removeButton.classList.add('remove');

  removeButton.addEventListener('click', function() {
    li.remove();
  });

  li.appendChild(removeButton);
  document.getElementById('taskList').appendChild(li);

  taskInput.value = '';
  dueDateInput.value = '';
});
```

## 带分类的 BMI 计算器

### 描述

在此练习中，学生将创建一个 BMI（身体质量指数）计算器，根据用户输入的体重和身高计算 BMI 并显示 BMI 分类。本练习介绍如何处理表单输入、执行计算以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BMI Calculator with Category</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="calculator-container">
    <h1>BMI Calculator</h1>
    <form id="bmiForm">
      <input type="number" id="weightInput" placeholder="Enter weight in kg" required>
      <input type="number" id="heightInput" placeholder="Enter height in cm" required>
      <button type="submit">Calculate</button>
    </form>
    <p id="bmiDisplay">Your BMI: </p>
    <p id="categoryDisplay">Category: </p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.calculator-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}

input,
button {
  padding: 10px;
  font-size: 16px;
}

p {
  font-size: 18px;
  margin-top: 10px;
}
```

### JavaScript

```javascript
document.getElementById('bmiForm').addEventListener('submit', function(event) {
  event.preventDefault();

  const weight = parseFloat(document.getElementById('weightInput').value);
  const height = parseFloat(document.getElementById('heightInput').value) / 100;
  const bmi = (weight / (height * height)).toFixed(2);

  document.getElementById('bmiDisplay').textContent = `Your BMI: ${bmi}`;

  let category = '';

  if (bmi < 18.5) {
    category = 'Underweight';
  } else if (bmi < 24.9) {
    category = 'Normal weight';
  } else if (bmi < 29.9) {
    category = 'Overweight';
  } else {
    category = 'Obesity';
  }

  document.getElementById('categoryDisplay').textContent = `Category: ${category}`;
});
```

## 带本地存储的待办事项列表

### 描述

在此练习中，学生将创建一个待办事项列表，将项目保存到本地存储中，以便在页面刷新后仍然保留。本练习介绍如何处理表单输入、动态更新 DOM 以及使用本地存储。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 本地存储
- DOM 操作（添加、更新和删除元素）
- 处理表单输入

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Todo List with Local Storage</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="todo-container">
    <h1>Todo List</h1>
    <form id="todoForm">
      <input type="text" id="taskInput" placeholder="Enter a new task" required>
      <button type="submit">Add Task</button>
    </form>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
```



```css
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}

form {
display: flex;
flex-direction: column;
gap: 10px;
}

input, button {
padding: 10px;
font-size: 16px;
}

ul {
list-style-type: none;
padding: 0;
}

li {
padding: 10px;
margin: 5px 0;
background-color: #fff;
border: 1px solid #ccc;
border-radius: 5px;
display: flex;
justify-content: space-between;
}

button.remove {
background: none;
border: none;
color: red;
cursor: pointer;
font-size: 16px;
}
```

```javascript
document.addEventListener('DOMContentLoaded', function() {
const itemList = document.getElementById('taskList');
const items = JSON.parse(localStorage.getItem('items')) || [];
items.forEach(item => {
addItemToDOM(item);
});

document.getElementById('todoForm').addEventListener('submit', function(event) {
event.preventDefault();
const taskInput = document.getElementById('taskInput');
const taskText = taskInput.value;
if (taskText === '') return;
addItemToDOM(taskText);
items.push(taskText);
localStorage.setItem('items', JSON.stringify(items));
taskInput.value = '';
});

function addItemToDOM(taskText) {
const li = document.createElement('li');
li.textContent = taskText;
const removeButton = document.createElement('button');
removeButton.textContent = 'Remove';
removeButton.classList.add('remove');
removeButton.addEventListener('click', function() {
li.remove();
const index = items.indexOf(taskText);
if (index !== -1) {
items.splice(index, 1);
localStorage.setItem('items', JSON.stringify(items));
}
});
li.appendChild(removeButton);
itemList.appendChild(li);
}
});
```

### 字符计数器

**描述：**在本练习中，学生将创建一个字符计数器，用于显示文本区域中输入的字符数。本练习介绍了如何处理输入事件以及动态更新 DOM。

**涵盖的主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理输入事件
- DOM 操作（更新文本内容）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Character Counter</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="counter-container">
<h1>Character Counter</h1>
<textarea id="textInput" placeholder="Start typing..."></textarea>
<p id="charCountDisplay">Characters: 0</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}

.counter-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

textarea {
width: 100%;
height: 100px;
padding: 10px;
font-size: 16px;
}

p {
font-size: 18px;
margin-top: 10px;
}
```

**JavaScript：**

```javascript
document.getElementById('textInput').addEventListener('input', function() {
const charCount = this.value.length;
document.getElementById('charCountDisplay').textContent = `Characters: ${charCount}`;
});
```

### 多项选择题

在带有本地存储的购物清单练习中，项目保存在哪里以在页面刷新后保持持久化？

a) Session storage

b) Cookies

c) Local storage

d) IndexedDB

答案：c) Local storage

解释：项目保存在本地存储中，以便即使在页面刷新后也能保持持久化。

在带有本地存储的购物清单练习中，当点击某个项目的“Remove”按钮时会发生什么？

a) 该项目被划掉

b) 该项目从列表和本地存储中移除

c) 该项目被编辑

d) 该项目被标记为已完成

答案：b) 该项目从列表和本地存储中移除

解释：点击“Remove”按钮会将项目从列表和本地存储中移除。

在响应式导航栏练习中，使用哪种方法来显示或隐藏导航栏链接？

a) `add`

b) `remove`

c) `toggle`

d) `replace`

答案：c) `toggle`

解释：通过切换`active`类，`toggle`方法用于显示或隐藏导航栏链接。

在响应式导航栏练习中，`@media (max-width: 768px)`查询的作用是什么？

a) 为小于 768px 的屏幕应用样式

b) 为大于 768px 的屏幕应用样式

c) 隐藏导航栏

d) 更改导航栏的颜色

答案：a) 为小于 768px 的屏幕应用样式

解释：`@media (max-width: 768px)`查询为小于 768px 的屏幕应用样式，使导航栏具有响应性。

在闪卡应用练习中，点击闪卡时会发生什么？

a) 闪卡内容被隐藏

b) 显示下一张闪卡

c) 答案被揭示

d) 闪卡被移除

答案：c) 答案被揭示

解释：点击闪卡时，问题的答案会被揭示。

在闪卡应用练习中，`nextButton`的作用是什么？

a) 揭示答案

b) 打乱闪卡顺序

c) 显示下一张闪卡

d) 重置闪卡

答案：c) 显示下一张闪卡

解释：`nextButton`用于显示列表中的下一张闪卡。

在带反馈的测验应用练习中，如何获取用户选择的答案？

a) 使用`getElementById`

b) 使用`querySelector`

c) 使用`innerHTML`

d) 使用`textContent`

答案：b) 使用`querySelector`

解释：`querySelector`方法用于从单选按钮中获取用户选择的答案。

在带优先级的待办事项列表练习中，`prioritySelect`元素的作用是什么？

a) 允许用户输入新任务

b) 从列表中移除任务

c) 设置新任务的优先级

d) 显示任务列表

答案：c) 设置新任务的优先级

解释：`prioritySelect`元素允许用户设置添加到列表中的新任务的优先级。

在测验应用练习中，使用什么事件来处理测验提交？

a) `click`

b) `submit`

c) `change`

d) `input`

答案：a) `click`

解释：`click`事件用于处理测验提交并计算结果。

在测验应用练习中，如何获取用户选择的答案？

a) 使用`getElementById`

b) 使用`querySelector`

c) 使用`innerHTML`

d) 使用`textContent`

答案：b) 使用`querySelector`

解释：`querySelector`方法用于从单选按钮中获取用户选择的答案。

在字符计数器练习中，使用什么事件来更新字符计数？

a) `click`

b) `submit`

c) `change`

d) `input`

答案：d) `input`

解释：`input`事件用于在用户输入文本时更新字符计数。

在闪卡应用练习中，哪个 HTML 元素用于显示闪卡内容？

a) `<div>`

b) `<p>`

c) `<span>`

d) `<section>`

答案：b) `<p>`

解释：ID 为`flashcardContent`的`<p>`元素用于显示闪卡的内容。

在闪卡应用练习中，使用什么 JavaScript 方法来处理闪卡上的点击事件以揭示答案？

a) `addEventListener`

b) `removeEventListener`

c) `attachEvent`

d) `setTimeout`

答案：a) `addEventListener`

解释：`addEventListener`方法用于处理闪卡上的点击事件。

在闪卡应用练习中，如何切换闪卡内容在问题和答案之间？

a) 通过更改 CSS 类

b) 通过切换`innerHTML`属性

c) 通过切换`textContent`属性

d) 通过切换`dataset`属性

答案：d) 通过切换`dataset`属性

解释：切换`dataset.flipped`属性以在问题和答案之间切换。

在带反馈的测验应用练习中，哪个 HTML 元素用于包含测验问题和答案？

a) `<div>`

b) `<form>`

c) `<section>`

d) `<article>`

答案：a) `<div>`

解释：ID 为`quiz`的`<div>`元素用于包含测验问题和答案。

在带反馈的测验应用练习中，使用什么方法来检查用户的答案？

a) `querySelectorAll`

b) `querySelector`

c) `getElementById`

d) `getElementsByClassName`

答案：a) `querySelectorAll`

解释：`querySelectorAll`方法用于选择所有答案容器以检查用户的答案。

在带优先级的待办事项列表练习中，使用哪个 HTML 元素来输入任务优先级？

a) `<input>`

b) `<select>`

c) `<textarea>`

d) `<button>`

答案：b) `<select>`

解释：`<select>`元素用于输入任务优先级。

在带优先级的待办事项列表练习中，如何根据优先级对任务进行样式设置？

a) 通过添加内联样式

b) 通过添加 CSS 类

c) 通过添加数据属性

d) 通过修改样式属性

答案：b) 通过添加 CSS 类

解释：添加 CSS 类（`high`、`medium`、`low`）来根据优先级对任务进行样式设置。

在带暂停/恢复功能的倒计时器练习中，使用哪个 JavaScript 函数以设定的时间间隔重复调用一个函数？

a) `setTimeout`

b) `setInterval`

c) `clearTimeout`

d) `clearInterval`

答案：b) `setInterval`

解释：`setInterval`函数用于以设定的时间间隔重复调用一个函数。

在带暂停/恢复功能的倒计时器练习中，点击“暂停”按钮会发生什么？

a) 计时器重新开始

b) 计时器值重置为零

c) 计时器停止并可恢复

d) 显示一个警告

答案：c) 计时器停止并可恢复

解释：点击“暂停”按钮会停止计时器，之后可以恢复。

在测验应用练习中，如何指示正确答案？

a) 通过改变背景颜色

b) 通过添加勾选图标

c) 通过将文本颜色改为绿色

d) 通过在答案下方显示消息

答案：c) 通过将文本颜色改为绿色

解释：正确答案通过将文本颜色改为绿色来指示。

### Simple Quiz App

**描述：**

在此练习中，学生将创建一个简单的测验应用，该应用呈现多项选择题并提供用户答案的反馈。本练习介绍如何处理表单提交、使用数组以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单提交
- 使用数组
- DOM 操作（更新文本内容）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simple Quiz App</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="quiz-container">
<h1>Quiz App</h1>
<form id="quizForm">
<div class="question">
<p>What is the capital of France?</p>
<label><input type="radio" name="q1" value="a"> Paris</label><br>
<label><input type="radio" name="q1" value="b"> Berlin</label><br>
<label><input type="radio" name="q1" value="c"> Madrid</label>
</div>
<div class="question">
<p>What is 2 + 2?</p>
<label><input type="radio" name="q2" value="a"> 3</label><br>
<label><input type="radio" name="q2" value="b"> 4</label><br>
<label><input type="radio" name="q2" value="c"> 5</label>
</div>
<button type="submit">Submit</button>
</form>
<p id="resultDisplay"></p>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}

.quiz-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}

.question {
margin-bottom: 20px;
}

button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
}

#resultDisplay {
margin-top: 20px;
font-size: 18px;
}
```

**JavaScript：**



```javascript
document.getElementById('quizForm').addEventListener('submit', function(event) {
event.preventDefault();
let score = 0;
const q1 = document.querySelector('input[name="q1"]:checked');
if (q1 && q1.value === 'a') {
score++;
}
const q2 = document.querySelector('input[name="q2"]:checked');
if (q2 && q2.value === 'b') {
score++;
}
const resultDisplay = document.getElementById('resultDisplay');
resultDisplay.textContent = `You scored ${score} out of 2.`;
});
```

### Random Number Generator

**描述：**

在此练习中，学生将创建一个随机数生成器，该生成器在指定范围内生成一个随机数并显示它。本练习介绍如何处理表单输入以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 生成随机数
- DOM 操作（更新文本内容）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Random Number Generator</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="rng-container">
<h1>Random Number Generator</h1>
<form id="rngForm">
<input type="number" id="minValue" placeholder="Min value" required>
<input type="number" id="maxValue" placeholder="Max value" required>
<button type="submit">Generate</button>
</form>
<p id="randomNumberDisplay"></p>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.rng-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
display: flex;
flex-direction: column;
gap: 10px;
margin-bottom: 20px;
}
input, button {
padding: 10px;
font-size: 16px;
}
p {
font-size: 24px;
margin-top: 20px;
}
```

**JavaScript：**

```javascript
document.getElementById('rngForm').addEventListener('submit', function(event) {
event.preventDefault();
const minValue = parseInt(document.getElementById('minValue').value);
const maxValue = parseInt(document.getElementById('maxValue').value);
const randomNumber = Math.floor(Math.random() * (maxValue - minValue + 1)) + minValue;
document.getElementById('randomNumberDisplay').textContent = `Random Number: ${randomNumber}`;
});
```

### Text Reverser

**描述：**

在此练习中，学生将创建一个文本反转器，该反转器反转输入文本并显示反转后的文本。本练习介绍如何处理表单输入以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 字符串操作
- DOM 操作（更新文本内容）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Text Reverser</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="reverser-container">
<h1>Text Reverser</h1>
<form id="reverserForm">
<textarea id="textInput" placeholder="Enter text" required></textarea>
<button type="submit">Reverse Text</button>
</form>
<p id="reversedTextDisplay"></p>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.reverser-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
display: flex;
flex-direction: column;
gap: 10px;
margin-bottom: 20px;
}
textarea, button {
padding: 10px;
font-size: 16px;
}
p {
font-size: 24px;
margin-top: 20px;
}
```

**JavaScript：**

```javascript
document.getElementById('reverserForm').addEventListener('submit', function(event) {
event.preventDefault();
const textInput = document.getElementById('textInput').value;
const reversedText = textInput.split('').reverse().join('');
document.getElementById('reversedTextDisplay').textContent = `Reversed Text: ${reversedText}`;
});
```

### 互动故事

**描述：**

在此练习中，学生将创建一个互动故事，用户通过选择影响故事结局。本练习介绍如何处理按钮点击、使用数组以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理按钮点击
- 使用数组
- DOM 操作（更新文本内容）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>互动故事</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="story-container">
<h1>互动故事</h1>
<p id="storyText">你身处一片森林。你看到两条路。你选择哪一条？</p>
<button id="option1">走左边的小路</button>
<button id="option2">走右边的小路</button>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.story-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 400px;
}
button {
padding: 10px 20px;
font-size: 16px;
cursor: pointer;
margin-top: 10px;
}
```

**JavaScript：**

```javascript
const storyText = document.getElementById('storyText');
const option1 = document.getElementById('option1');
const option2 = document.getElementById('option2');

option1.addEventListener('click', () => {
storyText.textContent = '你走了左边的小路，发现了一个宝箱。你是打开它还是离开？';
option1.textContent = '打开宝箱';
option2.textContent = '离开';
option1.removeEventListener('click', arguments.callee);
option2.removeEventListener('click', arguments.callee);
option1.addEventListener('click', () => {
storyText.textContent = '你打开了宝箱，发现了金币！你赢了！';
option1.style.display = 'none';
option2.style.display = 'none';
});
option2.addEventListener('click', () => {
storyText.textContent = '你离开了宝箱，继续你的旅程。你赢了！';
option1.style.display = 'none';
option2.style.display = 'none';
});
});

option2.addEventListener('click', () => {
storyText.textContent = '你走了右边的小路，遇到了一只熊。你是与它搏斗还是逃跑？';
option1.textContent = '与熊搏斗';
option2.textContent = '逃跑';
option1.removeEventListener('click', arguments.callee);
option2.removeEventListener('click', arguments.callee);
option1.addEventListener('click', () => {
storyText.textContent = '你与熊搏斗并获胜了！你赢了！';
option1.style.display = 'none';
option2.style.display = 'none';
});
option2.addEventListener('click', () => {
storyText.textContent = '你逃跑了，安全脱险。你赢了！';
option1.style.display = 'none';
option2.style.display = 'none';
});
});
```

### 带本地存储的任务列表

**描述：**

在此练习中，学生将创建一个任务列表，该列表将任务保存到本地存储中，以便在页面刷新后仍然保留。本练习介绍如何处理表单输入、动态更新 DOM 以及使用本地存储。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 本地存储
- DOM 操作（添加、更新和删除元素）
- 处理表单输入

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>带本地存储的任务列表</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="task-list-container">
<h1>任务列表</h1>
<form id="taskForm">
<input type="text" id="taskInput" placeholder="输入新任务" required>
<button type="submit">添加任务</button>
</form>
<ul id="taskList"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.task-list-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
form {
display: flex;
flex-direction: column;
gap: 10px;
}
input, button {
padding: 10px;
font-size: 16px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 10px;
margin: 5px 0;
background-color: #fff;
border: 1px solid #ccc;
border-radius: 5px;
display: flex;
justify-content: space-between;
}
button.remove {
background: none;
border: none;
color: red;
cursor: pointer;
font-size: 16px;
}
```

**JavaScript：**



```javascript
document.addEventListener('DOMContentLoaded', function() {
const taskList = document.getElementById('taskList');
const tasks = JSON.parse(localStorage.getItem('tasks')) || [];
tasks.forEach(task => {
addTaskToDOM(task);
});

document.getElementById('taskForm').addEventListener('submit', function(event) {
event.preventDefault();
const taskInput = document.getElementById('taskInput');
const taskText = taskInput.value;
if (taskText === '') return;
addTaskToDOM(taskText);
tasks.push(taskText);
localStorage.setItem('tasks', JSON.stringify(tasks));
taskInput.value = '';
});

function addTaskToDOM(taskText) {
const li = document.createElement('li');
li.textContent = taskText;
const removeButton = document.createElement('button');
removeButton.textContent = '删除';
removeButton.classList.add('remove');
removeButton.addEventListener('click', function() {
li.remove();
const index = tasks.indexOf(taskText);
if (index !== -1) {
tasks.splice(index, 1);
localStorage.setItem('tasks', JSON.stringify(tasks));
}
});
li.appendChild(removeButton);
taskList.appendChild(li);
}
});
```

### 带优先级的待办事项列表

**描述：**

在此练习中，学生将创建一个待办事项列表，允许用户添加不同优先级的任务。本练习介绍如何处理表单输入、动态更新 DOM 以及根据优先级对元素进行排序。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- DOM 操作（添加和排序元素）
- 使用数组

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>带优先级的待办事项列表</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="todo-container">
<h1>待办事项列表</h1>
<form id="todoForm">
<input type="text" id="taskInput" placeholder="输入新任务" required>
<select id="priorityInput">
<option value="High">高</option>
<option value="Medium">中</option>
<option value="Low">低</option>
</select>
<button type="submit">添加任务</button>
</form>
<ul id="taskList"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.todo-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
form {
display: flex;
flex-direction: column;
gap: 10px;
}
input, select, button {
padding: 10px;
font-size: 16px;
}
ul {
list-style-type: none;
padding: 0;
}
li {
padding: 10px;
margin: 5px 0;
background-color: #fff;
border: 1px solid #ccc;
border-radius: 5px;
display: flex;
justify-content: space-between;
}
button.remove {
background: none;
border: none;
color: red;
cursor: pointer;
font-size: 16px;
}
```

**JavaScript：**

```javascript
document.getElementById('todoForm').addEventListener('submit', function(event) {
    event.preventDefault();
    const taskInput = document.getElementById('taskInput');
    const priorityInput = document.getElementById('priorityInput');
    const taskText = taskInput.value;
    const priority = priorityInput.value;
    if (taskText === '') return;
    addTaskToDOM(taskText, priority);
    sortTasks();
    taskInput.value = '';
});

function addTaskToDOM(taskText, priority) {
    const li = document.createElement('li');
    li.textContent = `${taskText} (${priority})`;
    li.setAttribute('data-priority', priority);
    const removeButton = document.createElement('button');
    removeButton.textContent = 'Remove';
    removeButton.classList.add('remove');
    removeButton.addEventListener('click', function() {
        li.remove();
    });
    li.appendChild(removeButton);
    document.getElementById('taskList').appendChild(li);
}

function sortTasks() {
    const taskList = document.getElementById('taskList');
    const tasks = Array.from(taskList.children);
    tasks.sort((a, b) => {
        const priorities = { 'High': 3, 'Medium': 2, 'Low': 1 };
        return priorities[b.getAttribute('data-priority')] - priorities[a.getAttribute('data-priority')];
    });
    tasks.forEach(task => taskList.appendChild(task));
}
```

### 随机颜色生成器

**描述：**

在本练习中，学生将创建一个随机颜色生成器，每次点击按钮时页面背景颜色都会改变。本练习介绍如何处理按钮点击、生成随机颜色以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理按钮点击
- 生成随机颜色
- DOM 操作（更新样式）

**HTML：**

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Random Color Generator</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="color-generator-container">
<h1>Random Color Generator</h1>
<button id="colorButton">Generate Color</button>
</div>
<script src="script.js"></script>
</body>
</html>
```

**CSS：**

```css
body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.color-generator-container {
    text-align: center;
    background-color: #f0f0f0;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
}
```

**JavaScript：**

```javascript
document.getElementById('colorButton').addEventListener('click', function() {
    const randomColor = `#${Math.floor(Math.random() * 16777215).toString(16)}`;
    document.body.style.backgroundColor = randomColor;
});
```

### 多项选择题

#### 带截止日期的待办事项列表

在“带截止日期的待办事项列表”练习中，当点击任务的“移除”按钮时会发生什么？

- a) 任务被划掉
- b) 任务从列表中移除
- c) 任务被编辑
- d) 任务被标记为已完成

答案：b) 任务从列表中移除

解释：点击“移除”按钮会将任务从列表中移除。

在“带截止日期的待办事项列表”练习中，`dueDateInput` 元素的用途是什么？

- a) 输入任务描述
- b) 输入任务截止日期
- c) 显示任务总数
- d) 移除任务

答案：b) 输入任务截止日期

解释：`dueDateInput` 元素用于输入要添加到列表的新任务的截止日期。

#### 带分类的 BMI 计算器

在“带分类的 BMI 计算器”练习中，什么 BMI 值被认为是“正常体重”？

- a) BMI < 18.5
- b) 18.5 ≤ BMI < 24.9
- c) 24.9 ≤ BMI < 29.9
- d) BMI ≥ 29.9

答案：b) 18.5 ≤ BMI < 24.9

解释：BMI 值在 18.5 到 24.9 之间被认为是“正常体重”。

在“带分类的 BMI 计算器”练习中，使用什么事件来处理表单提交？

- a) `click`
- b) `submit`
- c) `change`
- d) `input`

答案：b) `submit`

解释：使用 `submit` 事件来处理表单提交并执行 BMI 计算。

#### 带本地存储的待办事项列表

在“带本地存储的待办事项列表”练习中，当任务被移除时会发生什么？

- a) 任务被隐藏
- b) 任务从 DOM 和本地存储中移除
- c) 任务被标记为已完成
- d) 任务被编辑

答案：b) 任务从 DOM 和本地存储中移除

解释：当任务被移除时，它会从 DOM 和本地存储中删除。

在“带本地存储的待办事项列表”练习中，任务存储在哪里以便页面刷新后仍然保留？

- a) Cookies
- b) 会话存储
- c) 本地存储
- d) IndexedDB

答案：c) 本地存储

解释：任务存储在本地存储中，以便即使在页面刷新后也能保留。

#### 简单测验应用

在“简单测验应用”练习中，使用什么事件来处理表单提交？

- a) `click`
- b) `submit`
- c) `input`
- d) `change`

答案：b) `submit`

解释：使用 `submit` 事件来处理表单提交并计算测验分数。

在“简单测验应用”练习中，如何计算用户的分数？

- a) 通过检查所选答案是否与正确答案匹配
- b) 通过统计问题数量
- c) 通过计算完成测验所花费的时间
- d) 通过将用户的答案与最高分进行比较

答案：a) 通过检查所选答案是否与正确答案匹配

解释：用户的分数是通过检查每个问题的所选答案是否与正确答案匹配来计算的。

#### 随机数生成器

在“随机数生成器”练习中，使用什么函数来生成随机数？

- a) `Math.random()`
- b) `Math.floor()`
- c) `Math.random()` 和 `Math.floor()`
- d) `Math.ceil()`

答案：c) `Math.random()` 和 `Math.floor()`

解释：`Math.random()` 函数生成一个 0 到 1 之间的随机数，`Math.floor()` 用于获取指定范围内的整数。

在“随机数生成器”练习中，用户需要输入什么值？

- a) 一个数字
- b) 最小值和最大值
- c) 一个数字范围
- d) 一个布尔值

答案：b) 最小值和最大值

解释：用户需要输入最小值和最大值来定义随机数生成的范围。

#### 文本反转器

在“文本反转器”练习中，使用什么方法来反转输入文本？

- a) `reverse()`
- b) `split()`
- c) `split().reverse().join()`
- d) `join()`

答案：c) `split().reverse().join()`

解释：使用 `split().reverse().join()` 方法将输入文本拆分为数组，反转数组，然后重新连接成字符串。

#### 互动故事

在“互动故事”练习中，使用什么事件来处理用户的选择？

- a) `click`
- b) `submit`
- c) `input`
- d) `change`

答案：a) `click`

解释：使用 `click` 事件来处理用户的选择并更新故事。

在“互动故事”练习中，当用户点击“走左边的小路”时会发生什么？

- a) 故事结束
- b) 用户被要求打开或离开一个宝箱
- c) 用户遇到一只熊
- d) 用户回家

答案：b) 用户被要求打开或离开一个宝箱

解释：点击“走左边的小路”会引导用户到一个宝箱，并提供打开或离开的选项。

#### 图片轮播

在“图片轮播”练习中，使用什么事件来浏览图片？

- a) `mouseover`
- b) `click`
- c) `submit`
- d) `input`

答案：b) `click`

解释：使用 `click` 事件来处理图片轮播的导航按钮。

#### 带本地存储的任务列表

在“带本地存储的任务列表”练习中，任务存储在哪里以便页面刷新后仍然保留？

- a) Cookies
- b) 会话存储
- c) 本地存储
- d) IndexedDB

答案：c) 本地存储

解释：任务存储在本地存储中，以便即使在页面刷新后也能保留。

在“带本地存储的任务列表”练习中，当点击任务的“移除”按钮时会发生什么？

- a) 任务被标记为已完成
- b) 任务被编辑
- c) 任务从 DOM 和本地存储中移除
- d) 任务被移动到列表末尾

答案：c) 任务从 DOM 和本地存储中移除

解释：当任务的“移除”按钮被点击时，它从 DOM 和本地存储中删除。

#### 带优先级的待办事项列表

在“带优先级的待办事项列表”练习中，用于存储每个任务优先级的属性是什么？

- a) `data-task`
- b) `data-priority`
- c) `task-priority`
- d) `priority-level`

答案：b) `data-priority`

解释：`data-priority` 属性用于存储每个任务的优先级。

#### 随机颜色生成器

在“随机颜色生成器”练习中，用于生成随机颜色的方法是什么？

- a) `Math.random()`
- b) `Math.floor()`
- c) `Math.random()` 和 `Math.floor()`
- d) `Math.ceil()`



答案：c) `Math.random()` 和 `Math.floor()`

解释：`Math.random()` 方法生成一个随机数，`Math.floor()` 用于将其转换为整数并创建有效的十六进制颜色代码。

## 练习题

### 带优先级的待办事项列表

任务在列表中如何排序？

a) 按字母顺序

b) 按创建日期

c) 按优先级

d) 按任务描述长度

答案：c) 按优先级

解释：任务按优先级在列表中排序，高优先级任务出现在中优先级和低优先级任务之前。

### 随机颜色生成器

什么事件触发背景颜色变化？

a) 页面加载

b) 表单提交

c) 按钮点击

d) 鼠标悬停

答案：c) 按钮点击

解释：背景颜色变化由按钮点击事件触发。

### 简单测验应用

用于处理表单提交的事件类型是什么？

a) `change`

b) `click`

c) `submit`

d) `input`

答案：c) `submit`

解释：表单提交通过监听表单元素上的 `submit` 事件来处理。

如何评估用户的答案？

a) 通过比较标签的文本内容

b) 通过检查选中的单选输入的值

c) 通过计算选中的单选输入的数量

d) 通过验证表单输入值

答案：b) 通过检查选中的单选输入的值

解释：通过检查选中的单选输入的值并与正确答案进行比较来评估用户的答案。

### 随机数生成器

用于生成随机数的 JavaScript 方法是什么？

a) `Math.random()`

b) `Math.floor()`

c) `Math.ceil()`

d) `Math.round()`

答案：a) `Math.random()`

解释：`Math.random()` 方法用于生成一个介于 0（包含）和 1（不包含）之间的随机数。

用于显示生成的随机数的 HTML 元素是什么？

a) `<div>`

b) `<p>`

c) `<span>`

d) `<h1>`

答案：b) `<p>`

解释：带有 ID `randomNumberDisplay` 的 `<p>` 元素用于显示生成的随机数。

### 文本反转器

用于反转文本的字符串方法是什么？

a) `split()`

b) `reverse()`

c) `join()`

d) 以上全部

答案：d) 以上全部

解释：通过使用 `split()` 将文本拆分为字符数组，使用 `reverse()` 反转数组，再使用 `join()` 将数组重新组合成字符串来反转文本。

用于输入文本的 HTML 元素是什么？

a) `<input>`

b) `<textarea>`

c) `<div>`

d) `<p>`

答案：b) `<textarea>`

解释：带有 ID `textInput` 的 `<textarea>` 元素用于输入要反转的文本。

### 互动故事

故事选项如何呈现给用户？

a) 使用单选按钮

b) 使用下拉菜单

c) 使用按钮

d) 使用超链接

答案：c) 使用按钮

解释：故事选项通过按钮呈现给用户，允许他们做出影响故事结局的选择。

用于处理用户选择的事件监听器是什么？

a) `submit`

b) `input`

c) `click`

d) `change`

答案：c) `click`

解释：当用户点击按钮时，使用 `click` 事件监听器来处理用户的选择。

### 使用本地存储的任务列表

任务如何保存以在页面重新加载后持久存在？

a) 使用 cookies

b) 使用本地存储

c) 使用会话存储

d) 使用数据库

答案：b) 使用本地存储

解释：任务保存到本地存储中，以便在页面刷新后仍然存在。

用于从 DOM 和本地存储中移除任务的 JavaScript 方法是什么？

a) `removeChild()`

b) `remove()`

c) `splice()`

d) `delete()`

答案：b) `remove()`

解释：使用 `remove()` 方法从 DOM 中移除任务元素，同时使用 `splice()` 从本地存储数组中移除该任务。

## 单位转换器

### 描述

在此练习中，学生将创建一个单位转换器，用于在不同测量单位（例如长度、重量）之间进行转换。本练习介绍了处理表单输入、执行计算以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 执行计算
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Unit Converter</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="converter-container">
<h1>Unit Converter</h1>
<form id="converterForm">
<input type="number" id="inputValue" placeholder="Enter value" required>
<select id="unitFrom">
<option value="meters">Meters</option>
<option value="kilometers">Kilometers</option>
<option value="grams">Grams</option>
<option value="kilograms">Kilograms</option>
</select>
<select id="unitTo">
<option value="meters">Meters</option>
<option value="kilometers">Kilometers</option>
<option value="grams">Grams</option>
<option value="kilograms">Kilograms</option>
</select>
<button type="submit">Convert</button>
</form>
<p id="resultDisplay">Converted Value: </p>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
font-family: Arial, sans-serif;
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
margin: 0;
}
.converter-container {
text-align: center;
background-color: #f0f0f0;
padding: 20px;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
display: flex;
flex-direction: column;
gap: 10px;
margin-bottom: 20px;
}
input, select, button {
padding: 10px;
font-size: 16px;
}
p {
font-size: 18px;
margin-top: 20px;
}
```

### JavaScript

```javascript
document.getElementById('converterForm').addEventListener('submit', function(event) {
event.preventDefault();
const inputValue = parseFloat(document.getElementById('inputValue').value);
const unitFrom = document.getElementById('unitFrom').value;
const unitTo = document.getElementById('unitTo').value;
let convertedValue;
if (unitFrom === unitTo) {
convertedValue = inputValue;
} else {
const conversionRates = {
meters: { kilometers: 0.001, grams: null, kilograms: null },
kilometers: { meters: 1000, grams: null, kilograms: null },
grams: { kilograms: 0.001, meters: null, kilometers: null },
kilograms: { grams: 1000, meters: null, kilometers: null }
};
convertedValue = inputValue * (conversionRates[unitFrom][unitTo] || 1);
}
document.getElementById('resultDisplay').textContent = `Converted Value: ${convertedValue}`;
});
```

## 单词反转器

### 描述

在此练习中，学生将创建一个单词反转器，用于反转给定句子中每个单词的字母顺序。本练习介绍了处理表单输入、字符串操作以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 字符串操作
- DOM 操作（更新文本内容）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
```

### 单词反转器

#### HTML

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>单词反转器</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="reverser-container">
<h1>单词反转器</h1>
<form id="reverserForm">
<textarea id="textInput" placeholder="输入一个句子" required></textarea>
<button type="submit">反转单词</button>
</form>
<p id="resultDisplay">反转后的句子：</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.reverser-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}
textarea, button {
  padding: 10px;
  font-size: 16px;
}
p {
  font-size: 18px;
  margin-top: 20px;
}
```

#### JavaScript

```javascript
document.getElementById('reverserForm').addEventListener('submit', function(event) {
  event.preventDefault();
  const textInput = document.getElementById('textInput').value;
  const words = textInput.split(' ');
  const reversedWords = words.map(word => word.split('').reverse().join(''));
  const reversedSentence = reversedWords.join(' ');
  document.getElementById('resultDisplay').textContent = `反转后的句子：${reversedSentence}`;
});
```

## 交互式待办事项列表

### 描述

在本练习中，学生将创建一个交互式待办事项列表，允许用户添加、标记完成和删除任务。本练习介绍如何处理表单输入、管理状态以及动态更新 DOM。

### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 管理状态
- DOM 操作（添加、更新和删除元素）

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>交互式待办事项列表</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="todo-container">
<h1>交互式待办事项列表</h1>
<form id="todoForm">
<input type="text" id="taskInput" placeholder="输入新任务" required>
<button type="submit">添加任务</button>
</form>
<ul id="taskList"></ul>
</div>
<script src="script.js"></script>
</body>
</html>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.todo-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}
form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
input, button {
  padding: 10px;
  font-size: 16px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  padding: 10px;
  margin: 5px 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
}
button.remove {
  background: none;
  border: none;
  color: red;
  cursor: pointer;
  font-size: 16px;
}
li.completed {
  text-decoration: line-through;
}
```

### JavaScript



```javascript
document.getElementById('todoForm').addEventListener('submit', function(event) {
  event.preventDefault();
  const taskInput = document.getElementById('taskInput');
  const taskText = taskInput.value;
  if (taskText === '') return;
  addTaskToDOM(taskText);
  taskInput.value = '';
});

function addTaskToDOM(taskText) {
  const li = document.createElement('li');
  li.textContent = taskText;
  const completeButton = document.createElement('button');
  completeButton.textContent = '完成';
  completeButton.addEventListener('click', function() {
    li.classList.toggle('completed');
  });
  const removeButton = document.createElement('button');
  removeButton.textContent = '删除';
  removeButton.classList.add('remove');
  removeButton.addEventListener('click', function() {
    li.remove();
  });
  li.appendChild(completeButton);
  li.appendChild(removeButton);
  document.getElementById('taskList').appendChild(li);
}
```

### 带开始/停止/重置功能的倒计时器

**描述：** 在本练习中，学生将创建一个倒计时器，允许用户开始、停止和重置倒计时。本练习介绍如何处理按钮点击、使用计时器以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理按钮点击
- 使用计时器
- DOM 操作（更新文本内容）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>倒计时器</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="timer-container">
<h1>倒计时器</h1>
<form id="timerForm">
<input type="number" id="secondsInput" placeholder="输入秒数" required>
<button type="submit">开始计时</button>
</form>
<p id="timerDisplay">0:00</p>
<button id="stopButton" disabled>停止</button>
<button id="resetButton" disabled>重置</button>
</div>
<script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.timer-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}
input, button {
  padding: 10px;
  font-size: 16px;
}
p {
  font-size: 36px;
  margin-top: 20px;
}
```

#### JavaScript

```javascript
let timer;
let timeLeft;
let isRunning = false;

document.getElementById('timerForm').addEventListener('submit', function(event) {
  event.preventDefault();
  clearInterval(timer);
  timeLeft = parseInt(document.getElementById('secondsInput').value);
  updateDisplay();
  startTimer();
  document.getElementById('stopButton').disabled = false;
  document.getElementById('resetButton').disabled = false;
});

document.getElementById('stopButton').addEventListener('click', function() {
  clearInterval(timer);
  isRunning = false;
  document.getElementById('stopButton').disabled = true;
});

document.getElementById('resetButton').addEventListener('click', function() {
  clearInterval(timer);
  timeLeft = 0;
  updateDisplay();
  document.getElementById('stopButton').disabled = true;
  document.getElementById('resetButton').disabled = true;
});

function startTimer() {
  if (!isRunning) {
    timer = setInterval(function() {
      if (timeLeft > 0) {
        timeLeft--;
        updateDisplay();
      } else {
        clearInterval(timer);
        alert('时间到！');
        document.getElementById('stopButton').disabled = true;
        document.getElementById('resetButton').disabled = true;
      }
    }, 1000);
    isRunning = true;
  }
}

function updateDisplay() {
  const minutes = Math.floor(timeLeft / 60).toString().padStart(1, '0');
  const seconds = (timeLeft % 60).toString().padStart(2, '0');
  document.getElementById('timerDisplay').textContent = `${minutes}:${seconds}`;
}

updateDisplay();
```

### 交互式测验

**描述：** 在本练习中，学生将创建一个交互式测验，呈现多项选择题并在最后显示得分。本练习介绍如何处理表单输入、管理状态以及动态更新 DOM。

**涵盖主题：**

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 管理状态
- DOM 操作（更新文本内容）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>交互式测验</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="quiz-container">
<h1>交互式测验</h1>
```

（注：原文在此处截断，后续内容缺失，故仅输出已有部分。）

HTML:

```html
<div id="quiz"></div>

<button id="nextButton">Next</button>

<p id="scoreDisplay"></p>

</div>

<script src="script.js"></script>

</body>

</html>
```

CSS:

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.quiz-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 300px;
}
#quiz {
  margin-bottom: 20px;
}
button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
p {
  font-size: 18px;
}
```

JavaScript:

```javascript
const quizData = [
  {
    question: 'What is the capital of France?',
    choices: ['Berlin', 'Madrid', 'Paris', 'Rome'],
    correct: 'Paris'
  },
  {
    question: 'What is 2 + 2?',
    choices: ['3', '4', '5', '6'],
    correct: '4'
  },
  {
    question: 'Who wrote "To Kill a Mockingbird"?',
    choices: ['Harper Lee', 'Mark Twain', 'J.K. Rowling', 'Jane Austen'],
    correct: 'Harper Lee'
  }
];
let currentQuestionIndex = 0;
let score = 0;
const quizElement = document.getElementById('quiz');
const nextButton = document.getElementById('nextButton');
const scoreDisplay = document.getElementById('scoreDisplay');
function loadQuestion() {
  const currentQuestion = quizData[currentQuestionIndex];
  quizElement.innerHTML = `
    <p>${currentQuestion.question}</p>
    ${currentQuestion.choices.map((choice, index) => `
      <label>
        <input type="radio" name="choice" value="${choice}">
        ${choice}
      </label>
      <br>
    `).join('')}
  `;
}
function showScore() {
  quizElement.style.display = 'none';
  nextButton.style.display = 'none';
  scoreDisplay.textContent = `Your score: ${score} / ${quizData.length}`;
}
nextButton.addEventListener('click', () => {
  const selectedChoice = document.querySelector('input[name="choice"]:checked');
  if (selectedChoice) {
    const answer = selectedChoice.value;
    if (answer === quizData[currentQuestionIndex].correct) {
      score++;
    }
    currentQuestionIndex++;
    if (currentQuestionIndex < quizData.length) {
      loadQuestion();
    } else {
      showScore();
    }
  } else {
    alert('Please select an answer');
  }
});
loadQuestion();
```

### 随机背景颜色

#### 描述

在本练习中，学生将创建一个按钮，每次点击时，页面背景颜色会变为随机颜色。本练习介绍了处理按钮点击、生成随机颜色以及动态更新 DOM。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理按钮点击
- 生成随机颜色
- DOM 操作（更新样式）

#### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Random Background Color</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="color-container">
<h1>Random Background Color</h1>
<button id="colorButton">Change Color</button>
</div>
<script src="script.js"></script>
</body>
</html>
```

#### CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.color-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
```

#### JavaScript

```javascript
document.getElementById('colorButton').addEventListener('click', function() {
  const randomColor = `#${Math.floor(Math.random() * 16777215).toString(16)}`;
  document.body.style.backgroundColor = randomColor;
});
```

### 数字猜谜游戏

#### 描述

在本练习中，学生将创建一个数字猜谜游戏，用户需要猜一个介于 1 到 100 之间的随机数字。本练习介绍了处理表单输入、生成随机数字以及动态更新 DOM。

#### 涵盖主题

- HTML 结构
- CSS 样式
- JavaScript 事件监听器
- 处理表单输入
- 生成随机数字
- DOM 操作（更新文本内容）

#### HTML



```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Number Guessing Game</title>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="game-container">
<h1>Number Guessing Game</h1>
<form id="guessForm">
<input type="number" id="guessInput" placeholder="Enter your guess" required>
<button type="submit">Submit Guess</button>
</form>
<p id="resultDisplay">Guess a number between 1 and 100!</p>
</div>
<script src="script.js"></script>
</body>
</html>
```

## CSS

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.game-container {
  text-align: center;
  background-color: #f0f0f0;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
}
input, button {
  padding: 10px;
  font-size: 16px;
}
p {
  font-size: 18px;
  margin-top: 20px;
}
```

## JavaScript

```javascript
const randomNumber = Math.floor(Math.random() * 100) + 1;
let attempts = 0;
document.getElementById('guessForm').addEventListener('submit', function(event) {
  event.preventDefault();
  const guess = parseInt(document.getElementById('guessInput').value);
  attempts++;
  let result = '';
  if (guess === randomNumber) {
    result = `Correct! The number was ${randomNumber}. It took you ${attempts} attempts.`;
  } else if (guess > randomNumber) {
    result = 'Too high! Try again.';
  } else {
    result = 'Too low! Try again.';
  }
  document.getElementById('resultDisplay').textContent = result;
});
```

## 多项选择题

### 1. 单位转换器练习中的表单提交事件

在单位转换器练习中，用于处理表单提交的事件是什么？

- a) `click`
- b) `submit`
- c) `input`
- d) `change`

**答案：** b) `submit`

**解释：** `submit` 事件用于处理表单提交并执行单位转换。

### 2. 单词反转器练习中的字母反转方法

在单词反转器练习中，用于反转每个单词字母的方法是什么？

- a) `reverse()`
- b) `split()`
- c) `split().reverse().join()`
- d) `join()`

**答案：** c) `split().reverse().join()`

**解释：** `split().reverse().join()` 方法用于将单词拆分为字符，反转它们，然后重新组合成单词。

### 3. 单位转换器练习中的转换率定义

在单位转换器练习中，转换率是如何定义的？

- a) 作为变量
- b) 作为对象
- c) 作为数组
- d) 作为字符串

**答案：** b) 作为对象

**解释：** 转换率被定义为一个对象，其中包含每个度量单位的嵌套对象。

### 4. 单词反转器练习中的句子输入元素

在单词反转器练习中，用于捕获句子的输入元素是什么？

- a) `input`
- b) `textarea`
- c) `select`
- d) `button`

**答案：** b) `textarea`

**解释：** `textarea` 元素用于捕获用户输入的句子。

### 5. 交互式待办事项列表中的完成类

在交互式待办事项列表练习中，当任务标记为完成时，添加了什么类？

- a) `done`
- b) `finished`
- c) `completed`
- d) `checked`

**答案：** c) `completed`

**解释：** 当任务标记为完成时，会添加 `completed` 类，用于对任务应用删除线样式。

### 6. 数字猜谜游戏中的随机数字生成方法

在数字猜谜游戏练习中，用于生成随机数字的方法是什么？

- a) `Math.random()`
- b) `Math.floor()`
- c) `Math.ceil()`
- d) `Math.round()`

**答案：** a) `Math.random()`

**解释：** `Math.random()` 方法用于生成 0 到 1 之间的随机数字，然后缩放并向下取整，得到 1 到 100 之间的数字。

### 7. 单位转换器练习中的表单提交事件类型

在单位转换器练习中，用于处理表单提交的事件类型是什么？

- a) `change`
- b) `click`
- c) `submit`
- d) `input`

**答案：** c) `submit`

**解释：** 表单提交通过监听表单元素上的 `submit` 事件来处理，以防止默认表单提交并执行转换。

### 8. 单位转换器练习中的结果显示元素

在单位转换器练习中，哪个 HTML 元素用于显示转换后的值？

- a) `<div>`
- b) `<span>`
- c) `<p>`
- d) `<h1>`

**答案：** c) `<p>`

**解释：** 带有 ID `resultDisplay` 的 `<p>` 元素用于显示转换后的值。

### 9. 单词反转练习中的单词反转方法

在单词反转练习中，用于反转每个单词的方法是哪个？

- a) `split()`
- b) `reverse()`
- c) `join()`
- d) 以上全部

**答案：** d) 以上全部

**解释：** 要反转每个单词，首先使用 `split()` 将文本拆分为单词数组，然后使用 `reverse()` 反转每个单词，最后使用 `join()` 将单词重新组合成字符串。

### 10. 单词反转练习中的文本输入元素

在单词反转练习中，用于输入文本的 HTML 元素是哪个？

- a) `<input>`
- b) `<textarea>`
- c) `<div>`
- d) `<p>`

**答案：** b) `<textarea>`

**解释：** 带有 ID `textInput` 的 `<textarea>` 元素用于输入将要反转的句子。

### 11. 交互式待办事项列表中的完成标记方式

在交互式待办事项列表练习中，如何将任务标记为已完成？

- a) 通过更改文本内容
- b) 通过向任务元素添加一个类
- c) 通过移除任务元素
- d) 通过更改任务元素的颜色

**答案：** b) 通过向任务元素添加一个类

**解释：** 通过切换任务元素上的 `completed` 类来将任务标记为已完成，该类会应用删除线样式。

### 12. 交互式待办事项列表中的表单提交事件监听器

在交互式待办事项列表练习中，用于处理表单提交的事件监听器是哪个？

- a) `change`
- b) `click`
- c) `submit`
- d) `input`

**答案：** c) `submit`

**解释：** 使用 `submit` 事件监听器来处理表单提交，以向列表中添加新任务。

### 13. 倒计时器中的停止计时器方法

在倒计时器练习中，用于停止计时器的方法是哪个？

- a) `clearTimeout()`
- b) `clearInterval()`
- c) `stopInterval()`
- d) `stopTimeout()`

**答案：** b) `clearInterval()`

**解释：** `clearInterval()` 方法用于通过清除 `setInterval()` 设置的间隔来停止计时器。

### 14. 倒计时器中的剩余时间显示元素

在倒计时器练习中，用于显示剩余时间的 HTML 元素是哪个？

- a) `<div>`
- b) `<span>`
- c) `<p>`
- d) `<h1>`

**答案：** c) `<p>`

**解释：** 带有 ID `timerDisplay` 的 `<p>` 元素用于显示剩余时间。

### 15. 交互式测验中的答案评估方式

在交互式测验练习中，如何评估用户的答案？

- a) 通过比较标签的文本内容
- b) 通过检查选中的单选输入的值
- c) 通过计算选中的单选输入的数量
- d) 通过验证表单输入值

**答案：** b) 通过检查选中的单选输入的值

**解释：** 通过检查选中的单选输入的值并将其与正确答案进行比较来评估用户的答案。

### 16. 交互式测验中的问题显示元素

在交互式测验练习中，用于显示测验问题的 HTML 元素是哪个？

- a) `<div>`
- b) `<ul>`
- c) `<p>`
- d) `<form>`

**答案：** a) `<div>`

**解释：** 带有 ID `quiz` 的 `<div>` 元素用于显示测验问题。

## 致谢

《前端代码游乐场：HTML、CSS 和 JavaScript 练习提升技能》一书的创作是一段充满热情、奉献和集体努力的旅程。这项事业得益于许多个人和社区的贡献，每个人都带来了独特的见解和支持。

我向 Web 开发社区致以最深切的感谢。你们在开源项目中的创新以及在讨论中分享的智慧，一直是灵感和知识的源泉。这本书是对我们领域标志性的集体智慧和协作精神的致敬。

特别感谢我的学生们，你们的问题和反馈在塑造这本书稿中起到了关键作用。你们对学习的热情不仅指导了本书内容的制定，也确保了它的相关性和适应性，以满足学习者不断变化的需求。

亲爱的读者，我衷心感谢你们与我一同踏上这段教育之旅。这本书献给你们在 Web 开发世界中不断成长和取得成就。正是你们磨练技能的决心推动着这项事业。

当我们共同推动 Web 开发的边界时，我不断意识到你们在这段旅程中扮演的关键角色。感谢你们成为这个持续过程中不可或缺的一部分。因对技术和创新的共同热情而团结在一起，我们共同前进。

致以深深的感谢，

Laurence Lars Svekis

## 关于作者

Laurence Svekis 是一位杰出的 Web 开发者、教育家和创新者，在 Web 应用和在线学习领域拥有超过二十年的经验。凭借在 JavaScript 和 Google Workspace 方面的专业知识，Laurence 通过设计适合所有水平学习者的综合课程，在在线教育领域取得了显著进展。他的专业能力体现在他已成功教授全球超过一百万名学生，这充分展示了他教育策略的有效性和广泛吸引力。

作为畅销书作者，Laurence 的出版物以清晰易懂的教学风格，为 Web 开发和编程提供了宝贵的实用见解。除了教育和写作角色外，他还是一位富有远见的企业家，致力于推动解决实际问题的 Web 技术。他的广泛贡献使他成为 Web 开发和数字学习领域的关键人物，激励着广大受众探索数字世界。

更多信息，请访问 <https://basescripts.com/>

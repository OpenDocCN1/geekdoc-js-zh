![](image_rsrc330.jpg)

JAVA SCRIPT

100 PROGRAM

By – Devbrat Rudra

[www.englishmybook.com](http://www.englishmybook.com)

VISIT OUR WEBSITE FOR MORE PDF BOOKS

INDEX

1\. Simple Hello World Program

2\. Simple Web Page with Heading

3\. Simple Web Page with Paragraph

4\. Simple Web Page with Image

5\. Simple Web Page with Link

6\. Simple List in HTML

7\. Simple Table in HTML

8\. Simple Form in HTML

9\. Simple CSS Styling

10\. Simple JavaScript Alert

11\. Simple JavaScript Prompt

12\. Simple JavaScript Confirm

13\. Simple Addition Calculator

14\. Simple Subtraction Calculator

15\. Simple Multiplication Calculator

16\. Simple Division Calculator

17\. Simple Increment Counter

18\. Simple Decrement Counter

19\. Simple Toggle Button

20\. Simple Toggle Text

21\. Simple Hide Element

22\. Simple Show Element

23\. Simple Toggle Element

24\. Simple Element Animation

25\. Simple Mouseover Event

26\. Simple Mouseout Event

27\. Simple Click Event

28\. Simple Double Click Event

29\. Simple Form Submission

30\. Simple Image Change on Click

31\. Simple Background Color Change

32\. Simple Text Color Change

33\. Simple Element Border Change

34\. Simple Element Size Change

35\. Simple Text Style Change

36\. Simple Text Font Change

37\. Simple Text Alignment Change

38\. Simple Text Bold

39\. Simple Text Italic

40\. Simple Text Underline

41\. Simple Bullet List

42\. Simple Numbered List

43\. Simple Nested List

44\. Simple Table with Border

45\. Simple Table with Colspan

46\. Simple Table with Rowspan

47\. Simple Form with Input Fields

48\. Simple Form with Text Field

49\. Simple Form with Text Area

50\. Simple Form with Checkbox

51\. Simple Form with Radio Button

52\. Simple Form with Dropdown

53\. Simple Form with Submit Button

54\. Simple External CSS Styling

55\. Simple Internal CSS Styling

56\. Simple Inline CSS Styling

57\. Simple JavaScript Console Log

58\. Simple JavaScript Variable

59\. Simple JavaScript Array

60\. Simple JavaScript Object

61\. Simple JavaScript Function

62\. Simple JavaScript If-Else Statement

63\. Simple JavaScript Switch Statement

64\. Simple JavaScript For Loop

65\. Simple JavaScript While Loop

66\. Simple JavaScript Do-While Loop

67\. Simple JavaScript Break Statement

68\. Simple JavaScript Continue Statement

69\. Simple JavaScript Math Functions

70\. Simple JavaScript Date Functions

71\. Simple JavaScript String Functions

72\. Simple JavaScript Array Functions

73\. Simple JavaScript Event Handling

74\. Simple JavaScript DOM Manipulation

75\. Simple JavaScript Element Creation

76\. Simple JavaScript Element Removal

77\. Simple JavaScript Element Attribute Change

78\. Simple JavaScript Element Style Change

79\. Simple JavaScript Element Content Change

80\. Simple JavaScript Element Traversal

81\. Simple JavaScript AJAX Request

82\. Simple JSON Data Parsing

83\. Simple Local Storage Usage

84\. Simple Session Storage Usage

85\. Simple Web Storage Clearing

86\. Simple Canvas Drawing

87\. Simple Canvas Animation

88\. Simple Geometric Shapes on Canvas

89\. Simple Gradient Filling on Canvas

90\. Simple Image Drawing on Canvas

91\. Simple QR Code Generation

92\. Simple Page Scroll Animation

93\. Simple Video Background

94\. Simple Image Zoom on Hover

95\. Simple Random Quote Generator

96\. Simple Image Slider with Dots

97\. Simple Modal Box

98\. Simple Pagination

99\. Simple Tabbed Content

100\. Simple To-Do List

101\. Simple Typing Effect

102\. Simple Form Validation

103\. Simple Search Filter

104\. Simple Image Gallery

105\. Simple Weather Information using API

106\. Simple Drag and Drop Feature

107\. Simple Audio Player

108\. Simple Video Player

109\. Simple Animated Loading Spinner

110\. Simple Mouseover Image Change

111\. Simple Scroll to Top Button

112\. Simple Form Auto-Complete

113\. Simple Page Refresh Button

114\. Simple Countdown Timer

115\. Simple Image Carousel

116\. Simple Digital Clock

117\. Simple Drawing Canvas

118\. Simple RSS Feed Display

119\. Simple Geolocation Information

120\. Simple Toggle Switch

121\. Simple Cookie Handling

122\. Simple Slider

123\. Simple Social Media Sharing Links

1\. **Hello World Output:**

<!DOCTYPE html>

<html>

<body>

<h1>My First JavaScript</h1>

<script>

document.write("Hello World!");

</script>

</body>

</html>

2\. **Button Click Alert:**

<!DOCTYPE html>

<html>

<body>

<button onclick="alert('Hello')">Click me</button>

</body>

</html>

3\. **Simple Calculator:**

<!DOCTYPE html>

<html>

<body>

<input id="num1" type="text"> +

<input id="num2" type="text">

<button onclick="addNumbers()">Add</button>

<p>Result: <span id="result"></span></p>

<script>

function addNumbers() {

var num1 = parseInt(document.getElementById("num1").value);

var num2 = parseInt(document.getElementById("num2").value);

var result = num1 + num2;

document.getElementById("result").innerText = result;

}

</script>

</body>

</html>

4\. **Simple Form Validation:**

<!DOCTYPE html>

<html>

<body>

<form onsubmit="return validateForm()">

Name: <input type="text" id="name">

<input type="submit" value="Submit">

</form>

<script>

function validateForm() {

var name = document.getElementById("name").value;

if (name == "") {

alert("Name must be filled out");

return false;

}

return true;

}

</script>

</body>

</html>

5\. **Display Current Date:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

document.getElementById("demo").innerHTML = Date();

</script>

</body>

</html>

6\. **Changing HTML Content:**

<!DOCTYPE html>

<html>

<body>

<p id="demo">JavaScript can change HTML content.</p>

<button type="button" onclick='document.getElementById("demo").innerHTML = "Hello JavaScript!"'>Click Me!</button>

</body>

</html>

7\. **Array Manipulation:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

var fruits = ["Apple", "Banana", "Orange"];

document.getElementById("demo").innerHTML = fruits;

fruits.push("Lemon");

document.getElementById("demo").innerHTML = fruits;

fruits.pop();

document.getElementById("demo").innerHTML = fruits;

</script>

</body>

</html>

8\. **Simple Image Slideshow:**

<!DOCTYPE html>

<html>

<body>

<img id="slide" width="300" height="200">

<script>

var images = ["image1.jpg", "image2.jpg", "image3.jpg"];

var currentIndex = 0;

function nextImage() {

if (currentIndex === images.length) {

currentIndex = 0;

}

document.getElementById("slide").src = images[currentIndex];

currentIndex++;

}

setInterval(nextImage, 2000);

</script>

</body>

</html>

9\. **Changing CSS Styles:**

<!DOCTYPE html>

<html>

<body>

<p id="demo">JavaScript can change the style of an HTML element.</p>

<button type="button" onclick='document.getElementById("demo").style.fontSize="25px"'>Click Me!</button>

</body>

</html>

10\. **Handling Mouse Events:**

<!DOCTYPE html>

<html>

<body>

<button onmouseover="mouseOver()" onmouseout="mouseOut()">Hover over me</button>

<script>

function mouseOver() {

document.body.style.backgroundColor = "lightgray";

}

function mouseOut() {

document.body.style.backgroundColor = "white";

}

</script>

</body>

</html>

SET-2

1\. **Simple To-Do List:**

<!DOCTYPE html>

<html>

<body>

<h2>My To Do List</h2>

<input type="text" id="taskInput">

<button onclick="addTask()">Add</button>

<ul id="taskList"></ul>

<script>

function addTask() {

var task = document.getElementById("taskInput").value;

var list = document.getElementById("taskList");

var item = document.createElement("li");

item.appendChild(document.createTextNode(task));

list.appendChild(item);

}

</script>

</body>

</html>

2\. **Basic Clock:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

function displayTime() {

var date = new Date();

var time = date.toLocaleTimeString();

document.getElementById("demo").innerHTML = time;

}

setInterval(displayTime, 1000);

</script>

</body>

</html>

3\. **Simple Animation:**

<!DOCTYPE html>

<html>

<body>

<div id="box" style="width:100px; height:100px; background-color:red; position:relative;"></div>

<script>

var pos = 0;

var box = document.getElementById("box");

function moveBox() {

if (pos >= 150) {

clearInterval(id);

} else {

pos += 1;

box.style.left = pos + "px";

}

}

var id = setInterval(moveBox, 10);

</script>

</body>

</html>

4\. **Basic Drag and Drop:**

<!DOCTYPE html>

<html>

<body>

<p>Drag the image into the rectangle:</p>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69">

<script>

function allowDrop(ev) {

ev.preventDefault();

}

function drag(ev) {

ev.dataTransfer.setData("text", ev.target.id);

}

function drop(ev) {

ev.preventDefault();

var data = ev.dataTransfer.getData("text");

ev.target.appendChild(document.getElementById(data));

}

</script>

</body>

</html>

5\. **Simple Popup Window:**

<!DOCTYPE html>

<html>

<body>

<button onclick="openPopup()">Open Popup</button>

<script>

function openPopup() {

window.open("", "Popup", "width=400,height=400");

}

</script>

</body>

</html>

6\. **Displaying User Input:**

<!DOCTYPE html>

<html>

<body>

<input type="text" id="inputField" oninput="displayInput()">

<p id="display"></p>

<script>

function displayInput() {

var input = document.getElementById("inputField").value;

document.getElementById("display").innerHTML = input;

}

</script>

</body>

</html>

7\. **Interactive Dropdown Menu:**

<!DOCTYPE html>

<html>

<body>

<select id="mySelect" onchange="showSelected()">

<option value="1">Apple</option>

<option value="2">Banana</option>

<option value="3">Cherry</option>

<option value="4">Date</option>

</select>

<p id="demo"></p>

<script>

function showSelected() {

var select = document.getElementById("mySelect");

var selectedValue = select.options[select.selectedIndex].text;

document.getElementById("demo").innerHTML = "You selected: " + selectedValue;

}

</script>

</body>

</html>

8\. **Playing Sound on Click:**

<!DOCTYPE html>

<html>

<body>

<button onclick="playSound()">Play Sound</button>

<audio id="myAudio">

<source src="sound.mp3" type="audio/mpeg">

Your browser does not support the audio element.

</audio>

<script>

var sound = document.getElementById("myAudio");

function playSound() {

sound.play();

}

</script>

</body>

</html>

9\. **Simple Drag and Resize:**

<!DOCTYPE html>

<html>

<head>

<style>

#mydiv {

width: 100px;

height: 100px;

border: 1px solid black;

resize: both;

overflow: auto;

}

</style>

</head>

<body>

<div id="mydiv" draggable="true"></div>

</body>

</html>

10\. **Displaying Geolocation:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

function getLocation() {

if (navigator.geolocation) {

navigator.geolocation.getCurrentPosition(showPosition);

} else {

document.getElementById("demo").innerHTML = "Geolocation is not supported by this browser.";

}

}

function showPosition(position) {

document.getElementById("demo").innerHTML = "Latitude: " + position.coords.latitude +

"<br>Longitude: " + position.coords.longitude;

}

</script>

<button onclick="getLocation()">Get Location</button>

</body>

</html>

SET-3

1\. **Simple Countdown Timer:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

var seconds = 60;

function countdown() {

seconds--;

document.getElementById("demo").innerHTML = seconds + " seconds remaining.";

if (seconds <= 0) {

clearInterval(countdownInterval);

document.getElementById("demo").innerHTML = "Time's up!";

}

}

var countdownInterval = setInterval(countdown, 1000);

</script>

</body>

</html>

2\. **Simple Responsive Web Design:**

<!DOCTYPE html>

<html>

<head>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>

.responsive {

max-width: 100%;

height: auto;

}

</style>

</head>

<body>

<img src="img.jpg" alt="Nature" class="responsive" width="600" height="400">

</body>

</html>

3\. **Simple Form Submission:**

<!DOCTYPE html>

<html>

<body>

<form onsubmit="submitForm()">

<input type="text" id="fname" name="fname" placeholder="First name">

<input type="text" id="lname" name="lname" placeholder="Last name">

<input type="submit" value="Submit">

</form>

<p id="result"></p>

<script>

function submitForm() {

var firstName = document.getElementById("fname").value;

var lastName = document.getElementById("lname").value;

document.getElementById("result").innerHTML = "Submitted: " + firstName + " " + lastName;

}

</script>

</body>

</html>

4\. **Simple Drag and Drop File Upload:**

<!DOCTYPE html>

<html>

<body>

<div id="drop_zone" ondrop="dropHandler(event);" ondragover="dragOverHandler(event);">

Drop files here

</div>

<script>

function dropHandler(ev) {

ev.preventDefault();

if (ev.dataTransfer.items) {

for (var i = 0; i < ev.dataTransfer.items.length; i++) {

if (ev.dataTransfer.items[i].kind === 'file') {

var file = ev.dataTransfer.items[i].getAsFile();

console.log('File: ' + file.name);

}

}

} else {

for (var i = 0; i < ev.dataTransfer.files.length; i++) {

console.log('File: ' + ev.dataTransfer.files[i].name);

}

}

}

function dragOverHandler(ev) {

ev.preventDefault();

}

</script>

</body>

</html>

5\. **Dynamic Content Update:**

<!DOCTYPE html>

<html>

<body>

<p id="demo">Click the button to change the text.</p>

<button onclick="changeText()">Click me</button>

<script>

function changeText() {

document.getElementById("demo").innerHTML = "Hello JavaScript!";

}

</script>

</body>

</html>

6\. **Simple Image Gallery:**

<!DOCTYPE html>

<html>

<body>

<img src="img1.jpg" alt="Image 1" width="300" height="200">

<img src="img2.jpg" alt="Image 2" width="300" height="200">

<img src="img3.jpg" alt="Image 3" width="300" height="200">

</body>

</html>

7\. **Drawing Canvas:**

<!DOCTYPE html>

<html>

<body>

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>

<script>

var canvas = document.getElementById("myCanvas");

var ctx = canvas.getContext("2d");

ctx.font = "30px Arial";

ctx.fillText("Hello World", 10, 50);

</script>

</body>

</html>

8\. **Simple Table Creation:**

<!DOCTYPE html>

<html>

<body>

<table border="1">

<tr>

<th>Name</th>

<th>Age</th>

</tr>

<tr>

<td>John</td>

<td>30</td>

</tr>

<tr>

<td>Doe</td>

<td>25</td>

</tr>

</table>

</body>

</html>

9\. **Simple Marquee Text:**

<!DOCTYPE html>

<html>

<body>

<marquee behavior="scroll" direction="left">This is a simple marquee text!</marquee>

</body>

</html>

10\. **Handling Keyboard Events:**

<!DOCTYPE html>

<html>

<body>

<input type="text" id="myInput" onkeydown="myFunction()">

<p id="demo"></p>

<script>

function myFunction() {

var x = document.getElementById("myInput");

document.getElementById("demo").innerHTML = "You pressed the " + x.value + " key.";

}

</script>

</body>

</html>

SET-4

1\. **Simple CSS Animation:**

<!DOCTYPE html>

<html>

<head>

<style>

#animate {

width: 100px;

height: 100px;

background-color: red;

position: relative;

animation: mymove 5s infinite;

}

@keyframes mymove {

from {left: 0px;}

to {left: 200px;}

}

</style>

</head>

<body>

<div id="animate"></div>

</body>

</html>

2\. **Simple Dropdown Menu:**

<!DOCTYPE html>

<html>

<body>

<select id="mySelect" onchange="showSelected()">

<option value="1">Option 1</option>

<option value="2">Option 2</option>

<option value="3">Option 3</option>

<option value="4">Option 4</option>

</select>

<p id="demo"></p>

<script>

function showSelected() {

var select = document.getElementById("mySelect");

var selectedOption = select.options[select.selectedIndex].text;

document.getElementById("demo").innerHTML = "You selected: " + selectedOption;

}

</script>

</body>

</html>

3\. **Simple SVG Drawing:**

<!DOCTYPE html>

<html>

<body>

<svg width="100" height="100">

<circle cx="50" cy="50" r="40" stroke="black" stroke-width="3" fill="red" />

</svg>

</body>

</html>

4\. **Handling Checkbox Events:**

<!DOCTYPE html>

<html>

<body>

<p>Click the checkbox to display its status.</p>

<input type="checkbox" id="myCheck" onclick="checkBox()">

<p id="text"></p>

<script>

function checkBox() {

var checkBox = document.getElementById("myCheck");

var text = document.getElementById("text");

if (checkBox.checked == true) {

text.innerHTML = "Checkbox is checked!";

} else {

text.innerHTML = "Checkbox is not checked!";

}

}

</script>

</body>

</html>

5\. **Simple Responsive Navigation Bar:**

<!DOCTYPE html>

<html>

<head>

<style>

ul {

list-style-type: none;

margin: 0;

padding: 0;

overflow: hidden;

background-color: #333;

}

li {

float: left;

}

li a {

display: block;

color: white;

text-align: center;

padding: 14px 16px;

text-decoration: none;

}

li a:hover {

background-color: #111;

}

</style>

</head>

<body>

<ul>

<li><a href="#home">Home</a></li>

<li><a href="#news">News</a></li>

<li><a href="#contact">Contact</a></li>

<li><a href="#about">About</a></li>

</ul>

</body>

</html>

6\. **Simple Local Storage Example:**

<!DOCTYPE html>

<html>

<body>

<input type="text" id="myInput">

<button onclick="saveText()">Save</button>

<p id="savedText"></p>

<script>

function saveText() {

var inputText = document.getElementById("myInput").value;

localStorage.setItem("text", inputText);

document.getElementById("savedText").innerHTML = "Saved: " + localStorage.getItem("text");

}

</script>

</body>

</html>

7\. **Simple Audio Player:**

<!DOCTYPE html>

<html>

<body>

<audio controls>

<source src="song.mp3" type="audio/mpeg">

Your browser does not support the audio tag.

</audio>

</body>

</html>

8\. **Simple Video Player:**

<!DOCTYPE html>

<html>

<body>

<video width="320" height="240" controls>

<source src="movie.mp4" type="video/mp4">

Your browser does not support the video tag.

</video>

</body>

</html>

9\. **Simple WebSocket Connection:**

<!DOCTYPE html>

<html>

<body>

<button onclick="startWebSocket()">Open WebSocket</button>

<script>

var ws = new WebSocket("wss://echo.websocket.org");

function startWebSocket() {

ws.onopen = function(event) {

ws.send("Hello, Server!");

};

ws.onmessage = function(event) {

alert("Message from server: " + event.data);

};

}

</script>

</body>

</html>

10\. **Displaying Random Number on Button Click:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<button onclick="generateRandomNumber()">Generate Random Number</button>

<script>

function generateRandomNumber() {

var randomNumber = Math.floor(Math.random() * 100) + 1;

document.getElementById("demo").innerHTML = "Random Number: " + randomNumber;

}

</script>

</body>

</html>

SET-5

Of course, here are ten more HTML and JavaScript program examples:

1\. **Simple Tooltip on Hover:**

<!DOCTYPE html>

<html>

<head>

<style>

.tooltip {

position: relative;

display: inline-block;

}

.tooltip .tooltiptext {

visibility: hidden;

width: 120px;

background-color: black;

color: #fff;

text-align: center;

border-radius: 6px;

padding: 5px;

position: absolute;

z-index: 1;

bottom: 125%;

left: 50%;

margin-left: -60px;

}

.tooltip:hover .tooltiptext {

visibility: visible;

}

</style>

</head>

<body>

<div class="tooltip">Hover over me

<span class="tooltiptext">Tooltip text</span>

</div>

</body>

</html>

2\. **Simple Responsive Image Grid:**

<!DOCTYPE html>

<html>

<head>

<style>

.responsive {

width: 24%;

margin: 1%;

float: left;

}

@media (max-width: 600px) {

.responsive {

width: 49%;

margin: 2%;

}

}

@media (max-width: 400px) {

.responsive {

width: 100%;

}

}

</style>

</head>

<body>

<div class="responsive">

<img src="img1.jpg" alt="Image 1" style="width:100%">

</div>

<div class="responsive">

<img src="img2.jpg" alt="Image 2" style="width:100%">

</div>

<div class="responsive">

<img src="img3.jpg" alt="Image 3" style="width:100%">

</div>

<div class="responsive">

<img src="img4.jpg" alt="Image 4" style="width:100%">

</div>

</body>

</html>

3\. **Geolocation Map Display:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

function getLocation() {

if (navigator.geolocation) {

navigator.geolocation.getCurrentPosition(showPosition);

} else {

document.getElementById("demo").innerHTML = "Geolocation is not supported by this browser.";

}

}

function showPosition(position) {

var latitude = position.coords.latitude;

var longitude = position.coords.longitude;

document.getElementById("demo").innerHTML = "Latitude: " + latitude + "<br>Longitude: " + longitude;

var mapLink = "https://www.google.com/maps?q=" + latitude + "," + longitude;

document.getElementById("demo").innerHTML += "<br><a href='" + mapLink + "' target='_blank'>View on Map</a>";

}

</script>

<button onclick="getLocation()">Get Location</button>

</body>

</html>

4\. **Simple Form Auto-Complete:**

<!DOCTYPE html>

<html>

<body>

<form autocomplete="on">

<label for="fname">First name:</label><br>

<input type="text" id="fname" name="fname"><br>

<label for="lname">Last name:</label><br>

<input type="text" id="lname" name="lname"><br><br>

<input type="submit" value="Submit">

</form>

</body>

</html>

5\. **Basic Canvas Animation:**

<!DOCTYPE html>

<html>

<body>

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>

<script>

var canvas = document.getElementById("myCanvas");

var ctx = canvas.getContext("2d");

var posX = 0;

function draw() {

ctx.clearRect(0, 0, canvas.width, canvas.height);

ctx.fillStyle = "#FF0000";

ctx.fillRect(posX, 0, 50, 50);

posX++;

if (posX > canvas.width) {

posX = 0;

}

}

setInterval(draw, 10);

</script>

</body>

</html>

6\. **Responsive Table:**

<!DOCTYPE html>

<html>

<head>

<style>

table {

font-family: arial, sans-serif;

border-collapse: collapse;

width: 100%;

}

td, th {

border: 1px solid #dddddd;

text-align: left;

padding: 8px;

}

tr:nth-child(even) {

background-color: #dddddd;

}

</style>

</head>

<body>

<table>

<tr>

<th>Firstname</th>

<th>Lastname</th>

<th>Age</th>

</tr>

<tr>

<td>John</td>

<td>Doe</td>

<td>30</td>

</tr>

<tr>

<td>Jane</td>

<td>Smith</td>

<td>25</td>

</tr>

<tr>

<td>Frank</td>

<td>Johnson</td>

<td>35</td>

</tr>

</table>

</body>

</html>

7\. **Simple Math Operation:**

<!DOCTYPE html>

<html>

<body>

<p>Click the button to perform the operation.</p>

<button onclick="mathOperation()">Perform Operation</button>

<p id="result"></p>

<script>

function mathOperation() {

var x = 10;

var y = 5;

var addition = x + y;

var subtraction = x - y;

var multiplication = x * y;

var division = x / y;

document.getElementById("result").innerHTML = "Addition: " + addition + "<br>" + "Subtraction: " + subtraction + "<br>" + "Multiplication: " + multiplication + "<br>" + "Division: " + division;

}

</script>

</body>

</html>

8\. **Simple Image Map:**

<!DOCTYPE html>

<html>

<body>

<img src="worldmap.gif" alt="World Map" usemap="#worldmap">

<map name="worldmap">

<area shape="rect" coords="34,44,270,350" alt="North America" href="northamerica.html">

<area shape="rect" coords="290,172,333,250" alt="Europe" href="europe.html">

<area shape="circle" coords="337,300,44" alt="Asia" href="asia.html">

</map>

</body>

</html>

9\. **Dynamic URL Redirect:**

<!DOCTYPE html>

<html>

<body>

<p>Click the button to redirect to a different page.</p>

<button onclick="redirect()">Redirect</button>

<script>

function redirect() {

window.location.href = "https://www.example.com";

}

</script>

</body>

</html>

10\. **Displaying Current Time and Date:**

<!DOCTYPE html>

<html>

<body>

<p

id="demo"></p>

<script>

var today = new Date();

var date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();

var time = today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();

var dateTime = date+' '+time;

document.getElementById("demo").innerHTML = "Current Date and Time: " + dateTime;

</script>

</body>

</html>

SET-6

1\. **Simple Email Validation:**

<!DOCTYPE html>

<html>

<body>

<input type="email" id="emailInput">

<button onclick="validateEmail()">Validate</button>

<p id="result"></p>

<script>

function validateEmail() {

var email = document.getElementById("emailInput").value;

var pattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/;

if (pattern.test(email)) {

document.getElementById("result").innerHTML = "Valid email address.";

} else {

document.getElementById("result").innerHTML = "Invalid email address.";

}

}

</script>

</body>

</html>

2\. **Simple Currency Converter:**

<!DOCTYPE html>

<html>

<body>

<input type="number" id="amountInput" placeholder="Enter amount">

<select id="currencySelect">

<option value="usd">USD</option>

<option value="eur">EUR</option>

<option value="gbp">GBP</option>

</select>

<button onclick="convertCurrency()">Convert</button>

<p id="result"></p>

<script>

function convertCurrency() {

var amount = document.getElementById("amountInput").value;

var currency = document.getElementById("currencySelect").value;

var rate;

if (currency === "usd") {

rate = 0.85;

} else if (currency === "eur") {

rate = 1.12;

} else if (currency === "gbp") {

rate = 1.25;

}

var convertedAmount = amount * rate;

document.getElementById("result").innerHTML = amount + " units of your currency is equal to " + convertedAmount + " units of the selected currency.";

}

</script>

</body>

</html>

3\. **Simple Digital Clock:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

function displayTime() {

var date = new Date();

var time = date.toLocaleTimeString();

document.getElementById("demo").innerHTML = time;

}

setInterval(displayTime, 1000);

</script>

</body>

</html>

4\. **Simple CSS Grid Layout:**

<!DOCTYPE html>

<html>

<head>

<style>

.grid-container {

display: grid;

grid-template-columns: auto auto auto;

background-color: #2196F3;

padding: 10px;

}

.grid-item {

background-color: rgba(255, 255, 255, 0.8);

border: 1px solid rgba(0, 0, 0, 0.8);

padding: 20px;

font-size: 30px;

text-align: center;

}

</style>

</head>

<body>

<div class="grid-container">

<div class="grid-item">1</div>

<div class="grid-item">2</div>

<div class="grid-item">3</div>

<div class="grid-item">4</div>

<div class="grid-item">5</div>

<div class="grid-item">6</div>

</div>

</body>

</html>

5\. **Simple Image Slider:**

<!DOCTYPE html>

<html>

<body>

<img id="slider" width="300" height="200">

<script>

var images = ["image1.jpg", "image2.jpg", "image3.jpg"];

var currentIndex = 0;

function changeImage() {

document.getElementById("slider").src = images[currentIndex];

currentIndex++;

if (currentIndex >= images.length) {

currentIndex = 0;

}

}

setInterval(changeImage, 2000);

</script>

</body>

</html>

6\. **Simple Drag and Drop Image Upload:**

<!DOCTYPE html>

<html>

<body>

<div id="drop_zone" ondrop="dropHandler(event);" ondragover="dragOverHandler(event);">

Drop image here

</div>

<script>

function dropHandler(ev) {

ev.preventDefault();

var image = ev.dataTransfer.files[0];

var reader = new FileReader();

reader.onload = function(event) {

var img = document.createElement('img');

img.src = event.target.result;

document.body.appendChild(img);

};

reader.readAsDataURL(image);

}

function dragOverHandler(ev) {

ev.preventDefault();

}

</script>

</body>

</html>

7\. **Simple Toggle Button:**

<!DOCTYPE html>

<html>

<body>

<p>Click the button to toggle between hiding and showing the content.</p>

<button onclick="toggleContent()">Toggle Content</button>

<p id="content" style="display:none">This is the hidden content.</p>

<script>

function toggleContent() {

var content = document.getElementById("content");

if (content.style.display === "none") {

content.style.display = "block";

} else {

content.style.display = "none";

}

}

</script>

</body>

</html>

8\. **Simple Drawing App:**

<!DOCTYPE html>

<html>

<body>

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>

<script>

var canvas = document.getElementById("myCanvas");

var ctx = canvas.getContext("2d");

var painting = false;

canvas.addEventListener('mousedown', startPosition);

canvas.addEventListener('mouseup', finishedPosition);

canvas.addEventListener('mousemove', draw);

function startPosition(e) {

painting = true;

draw(e);

}

function finishedPosition() {

painting = false;

ctx.beginPath();

}

function draw(e) {

if (!painting) return;

ctx.lineWidth = 5;

ctx.lineCap = 'round';

ctx.strokeStyle = 'black';

ctx.lineTo(e.clientX - canvas.offsetLeft, e.clientY - canvas.offsetTop);

ctx.stroke();

ctx.beginPath();

ctx.moveTo(e.clientX - canvas.offsetLeft, e.clientY - canvas.offsetTop);

}

</script>

</body>

</html>

9\. **Simple Page Reload:**

<!DOCTYPE html>

<html>

<body>

<p>Click the button to reload the page.</p>

<button onclick="reloadPage()">Reload Page</button>

<script>

function reloadPage() {

location.reload();

}

</script>

</body>

</html>

10\. **Displaying Browser Window Size:**

<!DOCTYPE html>

<html>

<body>

<p>Width: <span id="width"></span></p>

<p>Height: <span id="height"></span></p>

<script>

document.getElementById("width").innerText = window.innerWidth;

document.getElementById("height").innerText = window.innerHeight;

window.onresize = function() {

document.getElementById("width").innerText = window.innerWidth;

document.getElementById("height").innerText = window.innerHeight;

};

</script>

</body>

</html>

SET-7

1\. **Simple Text Animation:**

<!DOCTYPE html>

<html>

<head>

<style>

#textAnimation {

width: 100%;

white-space: nowrap;

overflow: hidden;

border: 1px solid black;

}

</style>

</head>

<body>

<div id="textAnimation"></div>

<script>

var text = "This is a simple text animation.";

var i = 0;

function typeWriter() {

if (i < text.length) {

document.getElementById("textAnimation").innerHTML += text.charAt(i);

i++;

setTimeout(typeWriter, 100);

}

}

typeWriter();

</script>

</body>

</html>

2\. **Simple Interactive Map:**

<!DOCTYPE html>

<html>

<body>

<img src="worldmap.jpg" usemap="#worldmap">

<map name="worldmap">

<area shape="rect" coords="0,0,100,100" alt="North America" href="northamerica.html">

<area shape="rect" coords="100,100,200,200" alt="Europe" href="europe.html">

<area shape="rect" coords="200,200,300,300" alt="Asia" href="asia.html">

</map>

</body>

</html>

3\. **Simple JSON Data Display:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

var data = '{"name":"John", "age":30, "city":"New York"}';

var obj = JSON.parse(data);

document.getElementById("demo").innerHTML = "Name: " + obj.name + "<br>Age: " + obj.age + "<br>City: " + obj.city;

</script>

</body>

</html>

4\. **Simple Currency Conversion using API:**

<!DOCTYPE html>

<html>

<body>

<input type="number" id="amountInput" placeholder="Enter amount">

<select id="currencySelect">

<option value="USD">USD</option>

<option value="EUR">EUR</option>

<option value="GBP">GBP</option>

</select>

<button onclick="convertCurrency()">Convert</button>

<p id="result"></p>

<script>

function convertCurrency() {

var amount = document.getElementById("amountInput").value;

var currency = document.getElementById("currencySelect").value;

fetch("https://api.exchangerate-api.com/v4/latest/USD")

.then(response => response.json())

.then(data => {

var rate = data.rates[currency];

var convertedAmount = amount * rate;

document.getElementById("result").innerHTML = amount + " units of your currency is equal to " + convertedAmount + " units of " + currency;

});

}

</script>

</body>

</html>

5\. **Simple Login Form with Local Storage:**

<!DOCTYPE html>

<html>

<body>

<form>

<label for="username">Username:</label><br>

<input type="text" id="username" name="username"><br>

<label for="password">Password:</label><br>

<input type="password" id="password" name="password"><br><br>

<input type="button" value="Submit" onclick="login()">

</form>

<p id="result"></p>

<script>

function login() {

var username = document.getElementById("username").value;

var password = document.getElementById("password").value;

if (username === localStorage.getItem("username") && password === localStorage.getItem("password")) {

document.getElementById("result").innerHTML = "Login successful!";

} else {

document.getElementById("result").innerHTML = "Invalid username or password!";

}

}

localStorage.setItem("username", "user");

localStorage.setItem("password", "pass");

</script>

</body>

</html>

6\. **Simple Sticky Navbar:**

<!DOCTYPE html>

<html>

<head>

<style>

.navbar {

overflow: hidden;

background-color: #333;

position: sticky;

position: -webkit-sticky;

top: 0;

}

.navbar a {

float: left;

display: block;

color: #f2f2f2;

text-align: center;

padding: 14px 20px;

text-decoration: none;

}

.navbar a:hover {

background-color: #ddd;

color: black;

}

</style>

</head>

<body>

<div class="navbar">

<a href="#home">Home</a>

<a href="#news">News</a>

<a href="#contact">Contact</a>

</div>

<p style="margin-top:100px">Some text to represent the main content of the page.</p>

</body>

</html>

7\. **Simple Date Picker:**

<!DOCTYPE html>

<html>

<body>

<label for="date">Select a date:</label>

<input type="date" id="date" name="date">

</body>

</html>

8\. **Simple QR Code Generator:**

<!DOCTYPE html>

<html>

<body>

<p>Enter text to

generate QR code:</p>

<input type="text" id="inputText">

<button onclick="generateQRCode()">Generate</button>

<div id="qrcode"></div>

<script src="https://cdn.jsdelivr.net/npm/qrcode@1.4.4/qrcode.min.js"></script>

<script>

function generateQRCode() {

var text = document.getElementById("inputText").value;

new QRCode(document.getElementById("qrcode"), text);

}

</script>

</body>

</html>

9\. **Simple Page Scroll Animation:**

<!DOCTYPE html>

<html>

<head>

<style>

#container {

width: 100%;

height: 1000px;

background-color: lightblue;

}

</style>

</head>

<body>

<div id="container">

<p>Scroll down to see the animation</p>

</div>

<script>

var container = document.getElementById("container");

function scrollAnimation() {

container.scrollIntoView({ behavior: 'smooth' });

}

setTimeout(scrollAnimation, 2000);

</script>

</body>

</html>

10\. **Simple Video Background:**

<!DOCTYPE html>

<html>

<body>

<video autoplay muted loop id="myVideo">

<source src="background_video.mp4" type="video/mp4">

Your browser does not support HTML5 video.

</video>

</body>

</html>

SET-8

1\. **Simple Text Animation:**

<!DOCTYPE html>

<html>

<head>

<style>

#textAnimation {

width: 100%;

white-space: nowrap;

overflow: hidden;

border: 1px solid black;

}

</style>

</head>

<body>

<div id="textAnimation"></div>

<script>

var text = "This is a simple text animation.";

var i = 0;

function typeWriter() {

if (i < text.length) {

document.getElementById("textAnimation").innerHTML += text.charAt(i);

i++;

setTimeout(typeWriter, 100);

}

}

typeWriter();

</script>

</body>

</html>

2\. **Simple Interactive Map:**

<!DOCTYPE html>

<html>

<body>

<img src="worldmap.jpg" usemap="#worldmap">

<map name="worldmap">

<area shape="rect" coords="0,0,100,100" alt="North America" href="northamerica.html">

<area shape="rect" coords="100,100,200,200" alt="Europe" href="europe.html">

<area shape="rect" coords="200,200,300,300" alt="Asia" href="asia.html">

</map>

</body>

</html>

3\. **Simple JSON Data Display:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

var data = '{"name":"John", "age":30, "city":"New York"}';

var obj = JSON.parse(data);

document.getElementById("demo").innerHTML = "Name: " + obj.name + "<br>Age: " + obj.age + "<br>City: " + obj.city;

</script>

</body>

</html>

4\. **Simple Currency Conversion using API:**

<!DOCTYPE html>

<html>

<body>

<input type="number" id="amountInput" placeholder="Enter amount">

<select id="currencySelect">

<option value="USD">USD</option>

<option value="EUR">EUR</option>

<option value="GBP">GBP</option>

</select>

<button onclick="convertCurrency()">Convert</button>

<p id="result"></p>

<script>

function convertCurrency() {

var amount = document.getElementById("amountInput").value;

var currency = document.getElementById("currencySelect").value;

fetch("https://api.exchangerate-api.com/v4/latest/USD")

.then(response => response.json())

.then(data => {

var rate = data.rates[currency];

var convertedAmount = amount * rate;

document.getElementById("result").innerHTML = amount + " units of your currency is equal to " + convertedAmount + " units of " + currency;

});

}

</script>

</body>

</html>

5\. **Simple Login Form with Local Storage:**

<!DOCTYPE html>

<html>

<body>

<form>

<label for="username">Username:</label><br>

<input type="text" id="username" name="username"><br>

<label for="password">Password:</label><br>

<input type="password" id="password" name="password"><br><br>

<input type="button" value="Submit" onclick="login()">

</form>

<p id="result"></p>

<script>

function login() {

var username = document.getElementById("username").value;

var password = document.getElementById("password").value;

if (username === localStorage.getItem("username") && password === localStorage.getItem("password")) {

document.getElementById("result").innerHTML = "Login successful!";

} else {

document.getElementById("result").innerHTML = "Invalid username or password!";

}

}

localStorage.setItem("username", "user");

localStorage.setItem("password", "pass");

</script>

</body>

</html>

6\. **Simple Sticky Navbar:**

<!DOCTYPE html>

<html>

<head>

<style>

.navbar {

overflow: hidden;

background-color: #333;

position: sticky;

position: -webkit-sticky;

top: 0;

}

.navbar a {

float: left;

display: block;

color: #f2f2f2;

text-align: center;

padding: 14px 20px;

text-decoration: none;

}

.navbar a:hover {

background-color: #ddd;

color: black;

}

</style>

</head>

<body>

<div class="navbar">

<a href="#home">Home</a>

<a href="#news">News</a>

<a href="#contact">Contact</a>

</div>

<p style="margin-top:100px">Some text to represent the main content of the page.</p>

</body>

</html>

7\. **Simple Date Picker:**

<!DOCTYPE html>

<html>

<body>

<label for="date">Select a date:</label>

<input type="date" id="date" name="date">

</body>

</html>

8\. **Simple QR Code Generator:**

<!DOCTYPE html>

<html>

<body>

<p>Enter text to

generate QR code:</p>

<input type="text" id="inputText">

<button onclick="generateQRCode()">Generate</button>

<div id="qrcode"></div>

<script src="https://cdn.jsdelivr.net/npm/qrcode@1.4.4/qrcode.min.js"></script>

<script>

function generateQRCode() {

var text = document.getElementById("inputText").value;

new QRCode(document.getElementById("qrcode"), text);

}

</script>

</body>

</html>

9\. **Simple Page Scroll Animation:**

<!DOCTYPE html>

<html>

<head>

<style>

#container {

width: 100%;

height: 1000px;

background-color: lightblue;

}

</style>

</head>

<body>

<div id="container">

<p>Scroll down to see the animation</p>

</div>

<script>

var container = document.getElementById("container");

function scrollAnimation() {

container.scrollIntoView({ behavior: 'smooth' });

}

setTimeout(scrollAnimation, 2000);

</script>

</body>

</html>

10\. **Simple Video Background:**

<!DOCTYPE html>

<html>

<body>

<video autoplay muted loop id="myVideo">

<source src="background_video.mp4" type="video/mp4">

Your browser does not support HTML5 video.

</video>

</body>

</html>

SET-9

1\. **Simple Image Zoom on Hover:**

<!DOCTYPE html>

<html>

<head>

<style>

.image-container {

position: relative;

width: 200px;

}

.image-container img {

width: 100%;

height: auto;

}

.image-container .zoom {

display: none;

position: absolute;

top: 0;

left: 0;

width: 100%;

height: auto;

}

.image-container:hover .zoom {

display: block;

}

</style>

</head>

<body>

<div class="image-container">

<img src="image.jpg" alt="Image">

<img class="zoom" src="image.jpg" alt="Zoomed Image">

</div>

</body>

</html>

2\. **Simple Random Quote Generator:**

<!DOCTYPE html>

<html>

<body>

<p id="quote"></p>

<button onclick="generateQuote()">Generate Quote</button>

<script>

var quotes = [

"The only way to do great work is to love what you do. - Steve Jobs",

"Life is what happens when you're busy making other plans. - John Lennon",

"The future belongs to those who believe in the beauty of their dreams. - Eleanor Roosevelt",

"It does not matter how slowly you go as long as you do not stop. - Confucius",

"Believe you can and you're halfway there. - Theodore Roosevelt"

];

function generateQuote() {

var randomIndex = Math.floor(Math.random() * quotes.length);

document.getElementById("quote").innerHTML = quotes[randomIndex];

}

</script>

</body>

</html>

3\. **Simple Image Slider with Dots:**

<!DOCTYPE html>

<html>

<head>

<style>

.slideshow-container {

max-width: 1000px;

position: relative;

margin: auto;

}

.mySlides {

display: none;

}

.dot {

height: 15px;

width: 15px;

background-color: #bbb;

border-radius: 50%;

display: inline-block;

}

.active {

background-color: #717171;

}

</style>

</head>

<body>

<div class="slideshow-container">

<div class="mySlides">

<img src="slide1.jpg" style="width:100%">

</div>

<div class="mySlides">

<img src="slide2.jpg" style="width:100%">

</div>

<div class="mySlides">

<img src="slide3.jpg" style="width:100%">

</div>

</div>

<div style="text-align:center">

<span class="dot"></span>

<span class="dot"></span>

<span class="dot"></span>

</div>

<script>

var slideIndex = 0;

showSlides();

function showSlides() {

var i;

var slides = document.getElementsByClassName("mySlides");

var dots = document.getElementsByClassName("dot");

for (i = 0; i < slides.length; i++) {

slides[i].style.display = "none";

}

slideIndex++;

if (slideIndex > slides.length) {slideIndex = 1}

for (i = 0; i < dots.length; i++) {

dots[i].className = dots[i].className.replace(" active", "");

}

slides[slideIndex-1].style.display = "block";

dots[slideIndex-1].className += " active";

setTimeout(showSlides, 2000);

}

</script>

</body>

</html>

4\. **Simple Modal Box:**

<!DOCTYPE html>

<html>

<head>

<style>

.modal {

display: none;

position: fixed;

z-index: 1;

left: 0;

top: 0;

width: 100%;

height: 100%;

overflow: auto;

background-color: rgba(0,0,0,0.4);

}

.modal-content {

background-color: #fefefe;

margin: 15% auto;

padding: 20px;

border: 1px solid #888;

width: 80%;

}

.close {

color: #aaa;

float: right;

font-size: 28px;

font-weight: bold;

}

.close:hover, .close:focus {

color: black;

text-decoration: none;

cursor: pointer;

}

</style>

</head>

<body>

<button onclick="openModal()">Open Modal</button>

<div id="myModal" class="modal">

<div class="modal-content">

<span class="close" onclick="closeModal()">&times;</span>

<p>This is a simple modal box!</p>

</div>

</div>

<script>

var modal = document.getElementById("myModal");

function openModal() {

modal.style.display = "block";

}

function closeModal() {

modal.style.display = "none";

}

</script>

</body>

</html>

5\. **Simple Pagination:**

<!DOCTYPE html>

<html>

<body>

<div id="pagination"></div>

<script>

var currentPage = 1;

var itemsPerPage = 5;

var items = ["Item 1", "Item 2", "Item 3", "Item 4", "Item 5", "Item 6", "Item 7", "Item 8", "Item 9", "Item 10", "Item 11", "Item 12", "Item 13", "Item 14", "Item 15"];

function displayItems(page) {

var start = (page - 1) * itemsPerPage;

var end = start + itemsPerPage;

var paginatedItems = items.slice(start, end);

document.getElementById("pagination").innerHTML = paginatedItems.join("<br>");

}

displayItems(currentPage);

</script>

</body>

</html>

6\. **Simple Tabbed Content:**

<!DOCTYPE html>

<html>

<head>

<style>

.tab {

overflow: hidden;

border: 1px solid #ccc;

background-color: #f1f1f1;

}

.tab button {

background-color: inherit;

float: left;

border: none;

outline: none;

cursor: pointer;

padding: 14px 16px;

transition: 0.3s;

}

.tab button:hover {

background-color: #ddd;

}

.tab button.active {

background-color: #ccc;

}

.tabcontent {

display: none;

padding: 6px 12px;

border: 1px solid #ccc;

border-top: none;

}

</style>

</head>

<body>

<div class="tab">

<button class="tablinks" onclick="openTab(event, 'Tab1')">Tab 1</button>

<button class="tablinks" onclick="openTab(event, 'Tab2')">Tab 2</button>

<

button class="tablinks" onclick="openTab(event, 'Tab3')">Tab 3</button>

</div>

<div id="Tab1" class="tabcontent">

<h3>Content of Tab 1</h3>

<p>This is the content of tab 1.</p>

</div>

<div id="Tab2" class="tabcontent">

<h3>Content of Tab 2</h3>

<p>This is the content of tab 2.</p>

</div>

<div id="Tab3" class="tabcontent">

<h3>Content of Tab 3</h3>

<p>This is the content of tab 3.</p>

</div>

<script>

function openTab(evt, tabName) {

var i, tabcontent, tablinks;

tabcontent = document.getElementsByClassName("tabcontent");

for (i = 0; i < tabcontent.length; i++) {

tabcontent[i].style.display = "none";

}

tablinks = document.getElementsByClassName("tablinks");

for (i = 0; i < tablinks.length; i++) {

tablinks[i].className = tablinks[i].className.replace(" active", "");

}

document.getElementById(tabName).style.display = "block";

evt.currentTarget.className += " active";

}

</script>

</body>

</html>

7\. **Simple To-Do List:**

<!DOCTYPE html>

<html>

<body>

<h2>My To-Do List</h2>

<ul id="myUL">

<li>Hit the gym</li>

<li class="checked">Pay bills</li>

<li>Meet George</li>

<li>Buy eggs</li>

<li>Read a book</li>

<li>Organize office</li>

</ul>

<script>

var list = document.querySelector('ul');

list.addEventListener('click', function(ev) {

if (ev.target.tagName === 'LI') {

ev.target.classList.toggle('checked');

}

}, false);

</script>

</body>

</html>

8\. **Simple Typing Effect:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

var text = 'This is a simple typing effect.';

var i = 0;

function typeWriter() {

if (i < text.length) {

document.getElementById("demo").innerHTML += text.charAt(i);

i++;

setTimeout(typeWriter, 100);

}

}

typeWriter();

</script>

</body>

</html>

9\. **Simple Form Validation:**

<!DOCTYPE html>

<html>

<body>

<form onsubmit="validateForm(event)">

<label for="email">Email:</label><br>

<input type="email" id="email" name="email" required><br><br>

<input type="submit" value="Submit">

</form>

<p id="error"></p>

<script>

function validateForm(event) {

var email = document.getElementById("email").value;

var pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

if (!pattern.test(email)) {

document.getElementById("error").innerHTML = "Invalid email address!";

event.preventDefault();

}

}

</script>

</body>

</html>

10\. **Simple Search Filter:**

<!DOCTYPE html>

<html>

<body>

<input type="text" id="myInput" onkeyup="filterFunction()" placeholder="Search for names..">

<ul id="myUL">

<li><a href="#">Adele</a></li>

<li><a href="#">Agnes</a></li>

<li><a href="#">Billy</a></li>

<li><a href="#">Bob</a></li>

<li><a href="#">Calvin</a></li>

<li><a href="#">David</a></li>

<li><a href="#">Freddie</a></li>

<li><a href="#">Glen</a></li>

<li><a href="#">Harry</a></li>

<li><a href="#">Irene</a></li>

<li><a href="#">Jimmy</a></li>

</ul>

<script>

function filterFunction() {

var input, filter, ul, li, a, i, txtValue;

input = document.getElementById('myInput');

filter = input.value.toUpperCase();

ul = document.getElementById('myUL');

li = ul.getElementsByTagName('li');

for (i = 0; i < li.length; i++) {

a = li[i].getElementsByTagName('a')[0];

txtValue = a.textContent || a.innerText;

if (txtValue.toUpperCase().indexOf(filter) > -1) {

li[i].style.display = '';

} else {

li[i].style.display = 'none';

}

}

}

</script>

</body>

</html>

SET-10

1\. **Simple Image Zoom on Hover:**

<!DOCTYPE html>

<html>

<head>

<style>

.image-container {

position: relative;

width: 200px;

}

.image-container img {

width: 100%;

height: auto;

}

.image-container .zoom {

display: none;

position: absolute;

top: 0;

left: 0;

width: 100%;

height: auto;

}

.image-container:hover .zoom {

display: block;

}

</style>

</head>

<body>

<div class="image-container">

<img src="image.jpg" alt="Image">

<img class="zoom" src="image.jpg" alt="Zoomed Image">

</div>

</body>

</html>

2\. **Simple Random Quote Generator:**

<!DOCTYPE html>

<html>

<body>

<p id="quote"></p>

<button onclick="generateQuote()">Generate Quote</button>

<script>

var quotes = [

"The only way to do great work is to love what you do. - Steve Jobs",

"Life is what happens when you're busy making other plans. - John Lennon",

"The future belongs to those who believe in the beauty of their dreams. - Eleanor Roosevelt",

"It does not matter how slowly you go as long as you do not stop. - Confucius",

"Believe you can and you're halfway there. - Theodore Roosevelt"

];

function generateQuote() {

var randomIndex = Math.floor(Math.random() * quotes.length);

document.getElementById("quote").innerHTML = quotes[randomIndex];

}

</script>

</body>

</html>

3\. **Simple Image Slider with Dots:**

<!DOCTYPE html>

<html>

<head>

<style>

.slideshow-container {

max-width: 1000px;

position: relative;

margin: auto;

}

.mySlides {

display: none;

}

.dot {

height: 15px;

width: 15px;

background-color: #bbb;

border-radius: 50%;

display: inline-block;

}

.active {

background-color: #717171;

}

</style>

</head>

<body>

<div class="slideshow-container">

<div class="mySlides">

<img src="slide1.jpg" style="width:100%">

</div>

<div class="mySlides">

<img src="slide2.jpg" style="width:100%">

</div>

<div class="mySlides">

<img src="slide3.jpg" style="width:100%">

</div>

</div>

<div style="text-align:center">

<span class="dot"></span>

<span class="dot"></span>

<span class="dot"></span>

</div>

<script>

var slideIndex = 0;

showSlides();

function showSlides() {

var i;

var slides = document.getElementsByClassName("mySlides");

var dots = document.getElementsByClassName("dot");

for (i = 0; i < slides.length; i++) {

slides[i].style.display = "none";

}

slideIndex++;

if (slideIndex > slides.length) {slideIndex = 1}

for (i = 0; i < dots.length; i++) {

dots[i].className = dots[i].className.replace(" active", "");

}

slides[slideIndex-1].style.display = "block";

dots[slideIndex-1].className += " active";

setTimeout(showSlides, 2000);

}

</script>

</body>

</html>

4\. **Simple Modal Box:**

<!DOCTYPE html>

<html>

<head>

<style>

.modal {

display: none;

position: fixed;

z-index: 1;

left: 0;

top: 0;

width: 100%;

height: 100%;

overflow: auto;

background-color: rgba(0,0,0,0.4);

}

.modal-content {

background-color: #fefefe;

margin: 15% auto;

padding: 20px;

border: 1px solid #888;

width: 80%;

}

.close {

color: #aaa;

float: right;

font-size: 28px;

font-weight: bold;

}

.close:hover, .close:focus {

color: black;

text-decoration: none;

cursor: pointer;

}

</style>

</head>

<body>

<button onclick="openModal()">Open Modal</button>

<div id="myModal" class="modal">

<div class="modal-content">

<span class="close" onclick="closeModal()">&times;</span>

<p>This is a simple modal box!</p>

</div>

</div>

<script>

var modal = document.getElementById("myModal");

function openModal() {

modal.style.display = "block";

}

function closeModal() {

modal.style.display = "none";

}

</script>

</body>

</html>

5\. **Simple Pagination:**

<!DOCTYPE html>

<html>

<body>

<div id="pagination"></div>

<script>

var currentPage = 1;

var itemsPerPage = 5;

var items = ["Item 1", "Item 2", "Item 3", "Item 4", "Item 5", "Item 6", "Item 7", "Item 8", "Item 9", "Item 10", "Item 11", "Item 12", "Item 13", "Item 14", "Item 15"];

function displayItems(page) {

var start = (page - 1) * itemsPerPage;

var end = start + itemsPerPage;

var paginatedItems = items.slice(start, end);

document.getElementById("pagination").innerHTML = paginatedItems.join("<br>");

}

displayItems(currentPage);

</script>

</body>

</html>

6\. **Simple Tabbed Content:**

<!DOCTYPE html>

<html>

<head>

<style>

.tab {

overflow: hidden;

border: 1px solid #ccc;

background-color: #f1f1f1;

}

.tab button {

background-color: inherit;

float: left;

border: none;

outline: none;

cursor: pointer;

padding: 14px 16px;

transition: 0.3s;

}

.tab button:hover {

background-color: #ddd;

}

.tab button.active {

background-color: #ccc;

}

.tabcontent {

display: none;

padding: 6px 12px;

border: 1px solid #ccc;

border-top: none;

}

</style>

</head>

<body>

<div class="tab">

<button class="tablinks" onclick="openTab(event, 'Tab1')">Tab 1</button>

<button class="tablinks" onclick="openTab(event, 'Tab2')">Tab 2</button>

<

button class="tablinks" onclick="openTab(event, 'Tab3')">Tab 3</button>

</div>

<div id="Tab1" class="tabcontent">

<h3>Content of Tab 1</h3>

<p>This is the content of tab 1.</p>

</div>

<div id="Tab2" class="tabcontent">

<h3>Content of Tab 2</h3>

<p>This is the content of tab 2.</p>

</div>

<div id="Tab3" class="tabcontent">

<h3>Content of Tab 3</h3>

<p>This is the content of tab 3.</p>

</div>

<script>

function openTab(evt, tabName) {

var i, tabcontent, tablinks;

tabcontent = document.getElementsByClassName("tabcontent");

for (i = 0; i < tabcontent.length; i++) {

tabcontent[i].style.display = "none";

}

tablinks = document.getElementsByClassName("tablinks");

for (i = 0; i < tablinks.length; i++) {

tablinks[i].className = tablinks[i].className.replace(" active", "");

}

document.getElementById(tabName).style.display = "block";

evt.currentTarget.className += " active";

}

</script>

</body>

</html>

7\. **Simple To-Do List:**

<!DOCTYPE html>

<html>

<body>

<h2>My To-Do List</h2>

<ul id="myUL">

<li>Hit the gym</li>

<li class="checked">Pay bills</li>

<li>Meet George</li>

<li>Buy eggs</li>

<li>Read a book</li>

<li>Organize office</li>

</ul>

<script>

var list = document.querySelector('ul');

list.addEventListener('click', function(ev) {

if (ev.target.tagName === 'LI') {

ev.target.classList.toggle('checked');

}

}, false);

</script>

</body>

</html>

8\. **Simple Typing Effect:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

var text = 'This is a simple typing effect.';

var i = 0;

function typeWriter() {

if (i < text.length) {

document.getElementById("demo").innerHTML += text.charAt(i);

i++;

setTimeout(typeWriter, 100);

}

}

typeWriter();

</script>

</body>

</html>

9\. **Simple Form Validation:**

<!DOCTYPE html>

<html>

<body>

<form onsubmit="validateForm(event)">

<label for="email">Email:</label><br>

<input type="email" id="email" name="email" required><br><br>

<input type="submit" value="Submit">

</form>

<p id="error"></p>

<script>

function validateForm(event) {

var email = document.getElementById("email").value;

var pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

if (!pattern.test(email)) {

document.getElementById("error").innerHTML = "Invalid email address!";

event.preventDefault();

}

}

</script>

</body>

</html>

10\. **Simple Search Filter:**

<!DOCTYPE html>

<html>

<body>

<input type="text" id="myInput" onkeyup="filterFunction()" placeholder="Search for names..">

<ul id="myUL">

<li><a href="#">Adele</a></li>

<li><a href="#">Agnes</a></li>

<li><a href="#">Billy</a></li>

<li><a href="#">Bob</a></li>

<li><a href="#">Calvin</a></li>

<li><a href="#">David</a></li>

<li><a href="#">Freddie</a></li>

<li><a href="#">Glen</a></li>

<li><a href="#">Harry</a></li>

<li><a href="#">Irene</a></li>

<li><a href="#">Jimmy</a></li>

</ul>

<script>

function filterFunction() {

var input, filter, ul, li, a, i, txtValue;

input = document.getElementById('myInput');

filter = input.value.toUpperCase();

ul = document.getElementById('myUL');

li = ul.getElementsByTagName('li');

for (i = 0; i < li.length; i++) {

a = li[i].getElementsByTagName('a')[0];

txtValue = a.textContent || a.innerText;

if (txtValue.toUpperCase().indexOf(filter) > -1) {

li[i].style.display = '';

} else {

li[i].style.display = 'none';

}

}

}

</script>

</body>

</html>

SET-11

1\. **Simple Image Gallery:**

<!DOCTYPE html>

<html>

<head>

<style>

.gallery {

display: flex;

flex-wrap: wrap;

}

.gallery img {

width: 200px;

height: 150px;

object-fit: cover;

margin: 5px;

}

</style>

</head>

<body>

<div class="gallery">

<img src="image1.jpg" alt="Image 1">

<img src="image2.jpg" alt="Image 2">

<img src="image3.jpg" alt="Image 3">

<img src="image4.jpg" alt="Image 4">

<img src="image5.jpg" alt="Image 5">

<img src="image6.jpg" alt="Image 6">

</div>

</body>

</html>

2\. **Simple Weather Information using API:**

<!DOCTYPE html>

<html>

<body>

<input type="text" id="cityInput" placeholder="Enter city">

<button onclick="getWeather()">Get Weather</button>

<p id="weather"></p>

<script>

function getWeather() {

var city = document.getElementById("cityInput").value;

fetch("https://api.openweathermap.org/data/2.5/weather?q=" + city + "&appid=YOUR_API_KEY")

.then(response => response.json())

.then(data => {

var weather = data.weather[0].main;

var description = data.weather[0].description;

document.getElementById("weather").innerHTML = "Weather in " + city + ": " + weather + " (" + description + ")";

});

}

</script>

</body>

</html>

3\. **Simple Drag and Drop Feature:**

<!DOCTYPE html>

<html>

<head>

<style>

#div1, #div2 {

float: left;

width: 100px;

height: 35px;

margin: 10px;

padding: 10px;

border: 1px solid black;

}

</style>

<script>

function allowDrop(ev) {

ev.preventDefault();

}

function drag(ev) {

ev.dataTransfer.setData("text", ev.target.id);

}

function drop(ev) {

ev.preventDefault();

var data = ev.dataTransfer.getData("text");

ev.target.appendChild(document.getElementById(data));

}

</script>

</head>

<body>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<br>

<div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

<br>

<img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="88" height="31">

</body>

</html>

4\. **Simple Audio Player:**

<!DOCTYPE html>

<html>

<body>

<audio controls>

<source src="song.mp3" type="audio/mpeg">

Your browser does not support the audio element.

</audio>

</body>

</html>

5\. **Simple Video Player:**

<!DOCTYPE html>

<html>

<body>

<video width="320" height="240" controls>

<source src="movie.mp4" type="video/mp4">

Your browser does not support the video tag.

</video>

</body>

</html>

6\. **Simple Animated Loading Spinner:**

<!DOCTYPE html>

<html>

<head>

<style>

.loader {

border: 16px solid #f3f3f3;

border-top: 16px solid #3498db;

border-radius: 50%;

width: 120px;

height: 120px;

animation: spin 2s linear infinite;

}

@keyframes spin {

0% { transform: rotate(0deg); }

100% { transform: rotate(360deg); }

}

</style>

</head>

<body>

<div class="loader"></div>

</body>

</html>

7\. **Simple Mouseover Image Change:**

<!DOCTYPE html>

<html>

<body>

<img id="image" src="image1.jpg" onmouseover="changeImage()" onmouseout="restoreImage()">

<script>

var originalImage = "image1.jpg";

var newImage = "image2.jpg";

function changeImage() {

document.getElementById("image").src = newImage;

}

function restoreImage() {

document.getElementById("image").src = originalImage;

}

</script>

</body>

</html>

8\. **Simple Scroll to Top Button:**

<!DOCTYPE html>

<html>

<head>

<style>

#myBtn {

display: none;

position: fixed;

bottom: 20px;

right: 30px;

z-index: 99;

border: none;

outline: none;

background-color: red;

color: white;

cursor: pointer;

padding: 15px;

border-radius: 10px;

}

#myBtn:hover {

background-color: #555;

}

</style>

</head>

<body>

<button onclick="topFunction()" id="myBtn" title="Go to top">Top</button>

<script>

window.onscroll = function() {scrollFunction()};

function scrollFunction() {

if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {

document.getElementById("myBtn").style.display = "block";

} else {

document.getElementById("myBtn").style.display = "none";

}

}

function topFunction() {

document.body.scrollTop = 0;

document.documentElement.scrollTop = 0;

}

</script>

</body>

</html>

9\. **Simple Form Auto-Complete:**

<!DOCTYPE html>

<html>

<body>

<form autocomplete="on">

<label for="fname">First name:</label><br>

<input type="text" id="fname" name="fname"><br>

<label for="lname">Last name:</label><br>

<input type="text" id="lname" name="lname"><br><br>

<input type="submit">

</form>

</body>

</html>

10\. **Simple Page Refresh Button:**

<!DOCTYPE html>

<html>

<body>

<button onclick="refreshPage()">Refresh Page</button>

<script>

function refreshPage() {

location.reload();

}

</script>

</body>

</html>

SET-12

1\. **Simple Countdown Timer:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

var countDownDate = new Date("Oct 31, 2023 00:00:00").getTime();

var x = setInterval(function() {

var now = new Date().getTime();

var distance = countDownDate - now;

var days = Math.floor(distance / (1000 * 60 * 60 * 24));

var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));

var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));

var seconds = Math.floor((distance % (1000 * 60)) / 1000);

document.getElementById("demo").innerHTML = days + "d " + hours + "h "

+ minutes + "m " + seconds + "s ";

if (distance < 0) {

clearInterval(x);

document.getElementById("demo").innerHTML = "EXPIRED";

}

}, 1000);

</script>

</body>

</html>

2\. **Simple Image Carousel:**

<!DOCTYPE html>

<html>

<head>

<style>

.slideshow-container {

max-width: 500px;

position: relative;

margin: auto;

}

.mySlides {

display: none;

}

.prev, .next {

cursor: pointer;

position: absolute;

top: 50%;

width: auto;

padding: 16px;

margin-top: -22px;

color: white;

font-weight: bold;

font-size: 18px;

transition: 0.6s ease;

border-radius: 0 3px 3px 0;

user-select: none;

}

.next {

right: 0;

border-radius: 3px 0 0 3px;

}

.prev:hover, .next:hover {

background-color: rgba(0,0,0,0.8);

}

.text {

color: #f2f2f2;

font-size: 15px;

padding: 8px 12px;

position: absolute;

bottom: 8px;

width: 100%;

text-align: center;

}

.dot {

cursor: pointer;

height: 15px;

width: 15px;

margin: 0 2px;

background-color: #bbb;

border-radius: 50%;

display: inline-block;

transition: background-color 0.6s ease;

}

.active, .dot:hover {

background-color: #717171;

}

</style>

</head>

<body>

<div class="slideshow-container">

<div class="mySlides">

<img src="slide1.jpg" style="width:100%">

<div class="text">Caption Text 1</div>

</div>

<div class="mySlides">

<img src="slide2.jpg" style="width:100%">

<div class="text">Caption Text 2</div>

</div>

<div class="mySlides">

<img src="slide3.jpg" style="width:100%">

<div class="text">Caption Text 3</div>

</div>

<a class="prev" onclick="plusSlides(-1)">&#10094;</a>

<a class="next" onclick="plusSlides(1)">&#10095;</a>

</div>

<br>

<div style="text-align:center">

<span class="dot" onclick="currentSlide(1)"></span>

<span class="dot" onclick="currentSlide(2)"></span>

<span class="dot" onclick="currentSlide(3)"></span>

</div>

<script>

var slideIndex = 1;

showSlides(slideIndex);

function plusSlides(n) {

showSlides(slideIndex += n);

}

function currentSlide(n) {

showSlides(slideIndex = n);

}

function showSlides(n) {

var i;

var slides = document.getElementsByClassName("mySlides");

var dots = document.getElementsByClassName("dot");

if (n > slides.length) {slideIndex = 1}

if (n < 1) {slideIndex = slides.length}

for (i = 0; i < slides.length; i++) {

slides[i].style.display = "none";

}

for (i = 0; i < dots.length; i++) {

dots[i].className = dots[i].className.replace(" active", "");

}

slides[slideIndex-1].style.display = "block";

dots[slideIndex-1].className += " active";

}

</script>

</body>

</html>

3\. **Simple Digital Clock:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

function displayTime() {

var date = new Date();

var time = date.toLocaleTimeString();

document.getElementById("demo").innerHTML = time;

}

setInterval(displayTime, 1000);

</script>

</body>

</html>

4\. **Simple Drawing Canvas:**

<!DOCTYPE html>

<html>

<body>

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>

<script>

var canvas = document.getElementById("myCanvas");

var ctx = canvas.getContext("2d");

ctx.beginPath();

ctx.arc(95, 50, 40, 0, 2 * Math.PI);

ctx.stroke();

</script>

</body>

</html>

5\. **Simple RSS Feed Display:**

<!DOCTYPE html>

<html>

<body>

<div id="rssOutput"></div>

<script>

var rssOutput = document.getElementById("rssOutput");

fetch('https://rss.example.com/feed')

.then(response => response.text())

.then(str => new window.DOMParser().parseFromString(str, "text/xml"))

.then(data => {

var items = data.querySelectorAll("item");

items.forEach(item => {

var title = item.querySelector("title").textContent;

var link = item.querySelector("link").textContent;

rssOutput.innerHTML += `<a href="${link}">${title}</a><br>`;

});

});

</script>

</body>

</html>

6\. **Simple Geolocation Information:**

<!DOCTYPE html>

<html>

<body>

<p id="demo"></p>

<script>

if (navigator.geolocation) {

navigator.geolocation.getCurrentPosition(showPosition);

} else {

document.getElementById("demo").innerHTML = "Geolocation is not supported by this browser.";

}

function showPosition(position) {

document.getElementById("demo").innerHTML = "Latitude: " + position.coords.latitude +

"<br>Longitude: " + position.coords.longitude;

}

</script>

</body>

</html>

7\. **Simple Toggle Switch:**

<!DOCTYPE html>

<html>

<body>

<label class="switch">

<input type="checkbox

" onclick="toggleSwitch()">

<span class="slider round"></span>

</label>

<script>

function toggleSwitch() {

var checkBox = document.querySelector("input[type='checkbox']");

if (checkBox.checked == true){

// Perform action when switch is on

} else {

// Perform action when switch is off

}

}

</script>

</body>

</html>

8\. **Simple Cookie Handling:**

<!DOCTYPE html>

<html>

<body>

<button onclick="setCookie()">Set Cookie</button>

<button onclick="getCookie()">Get Cookie</button>

<script>

function setCookie() {

document.cookie = "username=John Doe; expires=Thu, 18 Dec 2023 12:00:00 UTC; path=/";

}

function getCookie() {

var cookieValue = document.cookie;

alert(cookieValue);

}

</script>

</body>

</html>

9\. **Simple Slider:**

<!DOCTYPE html>

<html>

<head>

<style>

.slidecontainer {

width: 100%;

}

.slider {

-webkit-appearance: none;

width: 100%;

height: 15px;

border-radius: 5px;

background: #d3d3d3;

outline: none;

opacity: 0.7;

-webkit-transition: .2s;

transition: opacity .2s;

}

.slider:hover {

opacity: 1;

}

.slider::-webkit-slider-thumb {

-webkit-appearance: none;

appearance: none;

width: 25px;

height: 25px;

border-radius: 50%;

background: #4CAF50;

cursor: pointer;

}

.slider::-moz-range-thumb {

width: 25px;

height: 25px;

border-radius: 50%;

background: #4CAF50;

cursor: pointer;

}

</style>

</head>

<body>

<div class="slidecontainer">

<input type="range" min="1" max="100" value="50" class="slider" id="myRange">

</div>

<script>

var slider = document.getElementById("myRange");

var output = document.getElementById("demo");

output.innerHTML = slider.value;

slider.oninput = function() {

output.innerHTML = this.value;

}

</script>

</body>

</html>

10\. **Simple Social Media Sharing Links:**

<!DOCTYPE html>

<html>

<body>

<a href="https://www.facebook.com/sharer/sharer.php?u=example.com" target="_blank">Share on Facebook</a>

<a href="https://twitter.com/share?url=example.com&text=Check%20out%20this%20link" target="_blank">Share on Twitter</a>

<a href="https://www.linkedin.com/shareArticle?url=example.com&title=Title&summary=Summary" target="_blank">Share on LinkedIn</a>

</body>

</html>
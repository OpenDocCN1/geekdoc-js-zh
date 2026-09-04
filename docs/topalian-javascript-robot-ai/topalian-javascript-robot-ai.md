
# Topalian JavaScript 机器人 AI 实战

**作者**

**Christopher Andrew Topalian**

**献给**

**圣父上帝（天父）**

你好

你好，伙计

你怎么样？

玩得开心吗，你呢？

极棒

你好

你好，伙计

你怎么样？

玩得开心吗，你呢？

极棒

很不错

你好

你好，伙计

你怎么样？

玩得开心吗，你呢？

极棒

很不错

你好

你好，伙计

你怎么样？

玩得开心吗，你呢？

极棒

很不错

天气怎么样？

今天天气很好朗。

地球是个好地方

你还有关于它的更多信息吗？

嗯，它有陆地也有水

地球是个好地方

你还有关于它的更多信息吗？

嗯，它有陆地也有水

有趣，请继续。

地球是个好地方

你还有关于它的更多信息吗？

嗯，它有陆地也有水

有趣，请继续。

地球是个值得游玩的地方

地球是个好地方

你还有关于它的更多信息吗？

嗯，它有陆地也有水

有趣，请继续。

地球是个值得游玩的地方

那很有趣。

Christopher Topalian

200+200

发送

200+200

400

发送

脚本音乐与科学学院

CollegeOfScripting.weebly.com

Christopher Topalian

```
(16*4) + (400/16) * 750
```

发送

(16*4) + (400/16) * 750

18814

发送

脚本音乐与科学学院

CollegeOfScripting.weebly.com

**-->**

**https://github.com/ChristopherAndrewTopalia**

**<!-- Topalian_JavaScript_Robot_AI.html-->**

**<html>**

**<head>**

**<title> Topalian JavaScript 机器人 AI </title>**

**<link rel='stylesheet' href='css/style001.css'>**

**<script src='js/utility.js'></script>**

**<script src='data/responses.js'></script>**

**<script src='data/randomResponses.js'></script>**

**<script>**

**function calculate(input)**

**{**

**try**

**{**

![](img/3e986e3c8d5087a94f9df94cc12e8768_14_0.png)

**return eval(input);**

**}**

**catch(error)**

**{**

**return null;**

**}**

**}**

**function createRobot()**

**{**

**let context=null;**

**let mainDiv=ce('div');**

**mainDiv.id= 'mainDiv';**

**mainDiv.className= 'mainDiv';**

**document.body.append(mainDiv);**

**//-//**

**let chatBox=ce('div');**

**chatBox.id= 'chatBox';**

**chatBox.innerHTML= '';**

**chatBox.className= 'chatBox';**

**mainDiv.append(chatBox);**

**//-//**

**let lineBreakOutput=ce('hr');**

**mainDiv.append(lineBreakOutput);**

**//-//**

**let userInput=ce('input');**

**userInput.id= 'userInput';**

**userInput.className= 'userInput';**

**userInput.style.type= 'text';**

**userInput.placeholder='Type Words';**

**mainDiv.append(userInput);**

**//-//**

**let sendButton=ce('button');**

**sendButton.innerHTML= 'Send';**

**sendButton.id= 'sendButton';**

**sendButton.className= 'sendButton';**

**mainDiv.append(sendButton);**

**//-//**

**// Enter activates a click on send button**

**userInput.onkeydown=function(event)**

**{**

**if (event.key === 'Enter')**

**{**

**// prevent Enter key**

**event.preventDefault();**

**// trigger a click on send button**

**sendButton.click();**

**}**

**};**

**sendButton.onclick=function()**

**{**

**// display what person typed in chatBox**

**chatBox.innerHTML+=`<span style='color: aqua;'>${userInput.value}</span><br>`;**

**let userQuestion=userInput.value.trim();**

**if (userQuestion)**

**{**

**let responseObj=responses.find(function(obj)**

**{**

**return obj.keywords.some(function(keyword)**

**{**

**// lowercase and remove punctuation**

**let cleanInput=userQuestion.toLowerCase().replace(/[^\w\s\]/g,'');**

**let cleanKeyword=keyword.toLowerCase();**

**// check for exact match of cleaned input and cleaned keyword**

**return cleanInput === cleanKeyword;**

**});**

**});;**

**if (responseObj)**

**{**

**let randomIndex=Math.floor(Math.random() * responseObj.responses.length);**

**chatBox.innerHTML+=`<span style='color: aqua;'>${responseObj.responses[randomIndex]}</span><br>`;**

**if (responseObj.keywords.indexOf('bye') !== -1)**

**{**

**context=null;**

**chatBox.scrollTop=chatBox.scrollHeight;**

**}**

**else**

**{**

**context=responseObj.keywords;**

**chatBox.scrollTop=chatBox.scrollHeight;**

**}**

**}**

**else**

**{**

**let result=calculate(userQuestion);**

**if (result !== null)**

**{**

**chatBox.innerHTML+=`<span style='color: aqua;'>${result}</span><br>`;**

**}**

**}**

**ge('chatBox').scrollTop = ge('chatBox').scrollHeight;**

**} else {**

**let randomIndex = Math.floor(Math.random() * randomResponses.length);**

**ge('chatBox').innerHTML += `<span style='color: aqua;'>${randomResponses[randomIndex]}</span><br>`;**

**ge('chatBox').scrollTop = ge('chatBox').scrollHeight;**

**}**

**}**

**userInput.value = '';**

**}**

**};**

**</script>**

**</head>**

**<body onload='createRobot()'>**

**</body>**

**</html>**

```
// 
https://github.com/ChristopherAndrewTopalian

// utility.js
function ge(whichId) {
    return document.getElementById(whichId);
}

function ce(whichType) {
    return document.createElement(whichType);
}
```

```css
/* 献给父神 */
/* 
https://github.com/ChristopherAndrewTopalian */

/* style001.css */
body {
    background-color: rgb(40, 40, 40);
    color: rgb(255, 255, 255);
}

.mainDiv {
    position: fixed;
    top: 0px;
    left: 0px;
    width: 400px;
    padding: 5px;
    margin: 20px;
    border-radius: 8px;
    z-index: 10000;
    background-color: rgb(0, 0, 0);
    color: rgb(255, 255, 255);
}

.userInput {
    width: 340px;
    padding-left: 10px;
    padding-right: 10px;
    padding-top: 4px;
    padding-bottom: 4px;
    border-radius: 8px;
    background-color: rgb(0, 0, 0);
    color: rgb(255, 255, 255);
}

.robotTextStyle {
    color: rgb(255, 135, 255);
}

.sendButton {
    margin-left: 5px;
    border-radius: 8px;
    background-color: rgb(0, 0, 0);
    color: rgb(255, 255, 255);
}

.sendButton:hover {
    border-color: aqua;
}

.sendButton:active {
    color: rgb(0, 255, 255);
}

.chatBox {
    height: 200px;
    padding-left: 10px;
    padding-right: 10px;
    padding-top: 5px;
    padding-bottom: 5px;
    background-color: black;
    overflow-y: scroll;
}
```

```javascript
// 
https://github.com/ChristopherAndrewTopalian

// responses.js
// 如果找到关键词，使用这些回复
let responses = [
    {
        keywords: ["hi", "howdy", "hey", "holla", "good evening", "good morning", "greetings", "yo"],
        responses: ["Howdy Buddy", "Hi Friend", "Hi there", "Greetings Friend", "Good day", "Bonjour"]
    },
    {
        keywords: ["what is the weather like", "what is the forecast", "is it going to be sunny"],
        responses: ["It's a beautiful day.", "The weather is very nice.", "It's sunny and warm."]
    },
    {
        keywords: ["how are you", "what's up", "what are you up to?"],
        responses: ["I'm doing good, you?", "Having fun and you?", "I'm good, how about you?"]
    },
    {
        keywords: ["excellent", "very good", "doing good"],
        responses: ["Nice", "That's nice", "Very good", "Very Excellent"]
    },
    {
        keywords: ["bye", "goodbye", "take care"],
        responses: ["Bye. Talk to you soon.", "Goodbye", "Have fun"]
    },
    {
        keywords: ["what are your interests", "what do you want to do as a career", "what is your current job goal"],
        responses: ["Computer Science is fun.", "Programming is lots of fun.", "I like programming a lot."]
    }
];
```

```javascript
// 
https://github.com/ChristopherAndrewTopalian

// responses.js
// 如果没有找到关键词，使用这些回复
let responses = [
    "That's interesting.",
    "Would you tell me?",
    "Hmm, tell me more about that.",
    "Would you elaborate?",
    "Interesting, please go on.",
    "What else can you tell me about it?",
    "Do you have anymore information on it?",
    "Say again?",
    "Fascinating! Tell me more."
];
```

**更多教程：**

- **CollegeOfScripting.weebly.com**

- **CollegeOfScripting.wordpress.com**

- **Youtube.com/ScriptingCollege**

- **Twitter.com/CollegeOfScript**

- **GitHub.com/ChristopherTopalian**

- **GitHub.com/ChristopherAndrewTopalian**

- **Sites.google.com/view/CollegeOfScripting**

**献给父神上帝**

**本书由脚本编写音乐与科学学院（College of Scripting Music & Science）创作。**

**永远记住，每当你用铅笔和纸书写脚本时，它就会深深地印在记忆中，从而极好地掌握这些材料和方法。**

**当你输入脚本时，情况也是如此。你通过键盘或铅笔纸输入和书写脚本越写，你学到的编程就越多！**

**写下并输入你看到的每一个示例。**

**保持你所有脚本整齐有序。**

**你创建的每一个脚本都能提升你的编程能力。**

**看到代码是一回事，编写代码是另一回事。**

**写下它、输入它、说出它、看到它、梦见它。**

**CollegeOfScripting.weebly.com**

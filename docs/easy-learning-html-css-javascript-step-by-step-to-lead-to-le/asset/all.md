![](Image00000.jpg)

Easy LearningHTML CSS Javascript![](Image00002.jpg)YANG HUSimple is the beginning of wisdom. From the essence of practice, this book to briefly explain the concept about HTML CSS and Javascript programming.[http://en.verejava.com](http://en.verejava.com)Copyright © 2020 Yang HuAll rights reserved.ISBN :     979868513370 0CONTENTS1 [First Web Page](#text00002.html_a73F)2. [Box](#text00002.html_a73F)2.1 [<div> CSS Box](#text00003.html_a751)2.2 [Radius of The Div's Corners](#text00004.html_a76R)2.3 [Shadows of The Div's Box](#text00005.html_a76F)2.4 [Background Color of The Div Box](#text00007.html_a73S)2.5 [Absolute Position of The Div's Box](#text00008.html_a73T)2.6 [Relative Position of The Div's Box](#text00009.html_a76W)2.7 [Space Outside of The Div's Box](#text00010.html_a76G)2.8 [Space Inside of The Div's Box](#text00012.html_a76M)2.9 [Space Between Two Inline Elements](#text00014.html_a76P)2.10 [Insert Image to The Div's Box](#text00016.html_a75X)2.11 [Insert Text Below Image](#text00017.html_a74D)2.12 [Text Wraps Around The Image](#text00019.html_a74X)2.13 [Unordered List](#text00021.html_a74N)2.14 [Link Status Style](#text00023.html_a767)2.15 [Drop-Down Menu](#text00025.html_a74F)2.16 [Navigate Menu](#text00026.html_a74M)2.17 [Click Drop Down Menu](#text00027.html_a766)2.18 [Login Div Dialog](#text00028.html_a73M)3. [Javascript Basic Concept](#text00029.html_a73R)3.1 [Javascript HelloWorld](#text00029.html_a73R)3.2 [Variable](#text00030.html_a76C)3.3 [Variable and Type](#text00032.html_a76H)4. [Operational Operator](#text00033.html_a74C)4.1 [Arithmetic Operator](#text00033.html_a74C)4.2 [Function](#text00034.html_a74W)4.3 [Class](#text00037.html_a765)4.4 [Type Conversion](#text00039.html_a75T)4.5 [DOM](#text00040.html_a73G)4.6 [Event](#text00043.html_a74Y)4.7 [Create a Web Caculator](#text00044.html_a773)4.8 [Assignment Operator](#text00046.html_a75Z)4.9 [Relational Operator](#text00048.html_a74H)4.10 [If Conditional Statement](#text00049.html_a75C)4.11 [Logic Operator](#text00051.html_a762)5. [Control Statement](#text00055.html_a73W)5.1 [Switch Statement](#text00055.html_a73W)5.2 [While Loop Statement](#text00057.html_a76T)5.3 [For Loop Statement](#text00059.html_a774)6. [Array](#text00061.html_a75U)6.1 [One-Dimensional Array](#text00061.html_a75U)6.2 [Select All Check Box](#text00064.html_a772)6.3 [Two-Dimensional Array](#text00065.html_a75Y)6.4 [Find Dog Game](#text00067.html_a73C)6.5 [Secondary Linkage Drop-down](#text00070.html_a74G)7. [More Event](#text00076.html_a75S)7.1 [Login Web Page](#text00076.html_a75S)7.2 [MouseOver Thumbnail to Larger](#text00078.html_a753) ​8. [DOM and Element Hierarchy](#text00079.html_a73J)8.1 [Element Hierarchy](#text00079.html_a73J)8.2 [Create Text Node](#text00085.html_a74A)8.3 [Delete Node](#text00089.html_a73H)8.4 [Replace Node](#text00091.html_a76Y)8.5 [Add Contact Example](#text00093.html_a748)8.6 [CSS Style Font](#text00095.html_a76N)8.7 [CSS Change Class Selector](#text00096.html_a75P)8.8 [CSS Overflow Expand and Close](#text00098.html_a775)8.9 [CSS Floating Highlighting](#text00099.html_a770)8.10 [Table Create  Rows Columns](#text00100.html_a768)8.11 [Delete Table Row Column](#text00101.html_a74R)9. [Timer](#text00102.html_a73X)10. [Canvas Progress Bar Animation](#text00103.html_a74J)10.1 [Draw a line on Canvas](#text00104.html_a752)10.2 [Draw  a Rectangle on Canvas](#text00105.html_a73V)10.2 [Draw Progress Bar](#text00105.html_a73V)11. [Canvas Ball Bounce](#text00107.html_a745)11.1 [Draw a circle on the canvas](#text00107.html_a745)11.2 [Create a function drawBall](#text00108.html_a742)11.3 [Create a class Ball to draw](#text00109.html_a74U)11.4 [Create a Ball and then move down](#text00110.html_a75D)11.5 [Ball Bounce Upwards and Downwards](#text00111.html_a73U)12. [Javascript ES6 Object-Oriented Programming](#text00113.html_a73Z)12.1 [Create Class](#text00113.html_a73Z)12.2 [Inheritance](#text00115.html_a740)12.3 [Override](#text00116.html_a74T)13. [Airplane Game](#text00118.html_a761)13.1 [Create Airplane class](#text00120.html_a76U)13.2 [Keypress Event](#text00122.html_a763)13.3 [Move Airplane on canvas](#text00124.html_a75H)13.4 [Airplane Fire a Bullet](#text00126.html_a73D)13.5 [Enemyplane Move Down](#text00129.html_a75W)13.6 [Bullet Collided With EnemyPlane](#text00132.html_a74E)First Web PageHTML is a series of tags on a web page that format the display.1\. Create a FirstWebPage.html file with Notepad or anther Editor and open it in your browser to see the webpage![](Image00003.jpg)<html>: tag tells the browser that this is an HTML document.<title>: tag it defines the title of the document.<body>: tag defines the document's body.

| <! DOCTYPE HTML><html><head><title> First Web Page </title></head><body>A good start is half successful</body></html> |

<div> CSS Box1\. Create a Box.html file and open it in your browser to see the webpage![](Image00004.jpg)<div>: html tag defines a division or a section in an HTML document.<style>: setting the style of an HTML element..class selector: css selects elements with a specific class attribute.border: CSS properties allow you to specify the style, width, and color of an element's border.Color: (red:#ff0000 ,  green:#00ff00 , blue:#0000ff ,  grey:#cccccc )text-align: CSS properties specifies the horizontal alignment of text (left, center, right)

| <! DOCTYPE HTML><html><head><title> Border </title><style>.box{border:1px solid #cccccc;width:300px;height:150px;text-align:center;}</style></head><body><div class ="box" >Better Life</div></body></html> |

2\. defines the radius of the div's corners.![](Image00005.jpg)border-radius: CSS3 property defines the radius of the element's corners.

| <style>.box{border:1px solid #cccccc;width:300px;height:150px;text-align:center;border-radius:25px;}</style><div class ="box" >Better Life</div> |

3\. defines the shadows of the div's box.![](Image00006.jpg)box-shadow: CSS3 property attaches one or more shadows to an element.

| <style>.box{border:1px solid #cccccc;width:200px;height:200px;text-align:center;border-radius:25px;box-shadow: 0px 0px 5px #888888;}</style><div class ="box" >Better Life</div> |

4\. defines the shadows of the div's box.![](Image00007.jpg)box-shadow: CSS3 property attaches one or more shadows to an element.h-offset: The horizontal offset of the shadow.v-offset: The vertical offset of the shadow.

| <style>.box{border:1px solid #cccccc;width:200px;height:200px;text-align:center;border-radius:25px;box-shadow: 10px 10px 5px #888888;}</style><div class ="box" >Better Life</div> |

5\. defines the background color of the div's box.![](Image00008.jpg)background-color: CSS property define the color of background.font-size:24px; CSS property define the size of font.color:#ffffff; CSS property define the color of font.

| <style>.box{border:1px solid #cccccc;width:200px;height:200px;text-align:center;border-radius:8px;background-color:#ff0000;font-size:24px;color:#ffffff;}</style><div class ="box" >Better Life</div> |

6\. defines the absolute position of the div's box.![](Image00009.jpg)position:absolute; the element is positioned absolutely to its first positioned parent.top: offset; CSS property defines the top position of an element.left: offset; CSS property defines the left position of an element.

| <style>.redBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#ff0000;position:absolute;top:0px;left:0px;}.greenBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#00ff00;position:absolute;top:10px;left:10px;}.blueBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#0000ff;position:absolute;top:20px;left:20px;}</style><div class ="redBox" ></div><div class ="greenBox" ></div><div class ="blueBox" ></div> |

7\. defines the relative position of the div's box.![](Image00010.jpg)position:relative; the element is positioned relative to its normal position.

| <style>.redBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#ff0000;position:relative;}.greenBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#00ff00;position:relative;}.blueBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#0000ff;position:relative;}</style><div class ="redBox" ></div><div class ="greenBox" ></div><div class ="blueBox" ></div> |

8\. defines space around an element's content, outside of the div's box.![](Image00011.jpg)margin: CSS properties are used to create space around elements, outside of any defined borders. (top, right, bottom, and left)1\. margin-top2\. margin -right3\. margin -bottom4\. margin -left

| <style>.redBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#ff0000;position:relative;}.greenBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#00ff00;position:relative;}.blueBox{border:1px solid #cccccc;width:100px;height:100px;border-radius:8px;background-color:#0000ff;position:relative;}</style><div class ="redBox" ></div><div class ="greenBox" ></div><div class ="blueBox" ></div> |

9\. defines space around an element's content, inside of the div's box.![](Image00012.jpg)padding: CSS properties are used to generate space around an element's content, inside of any defined borders. (top, right, bottom, and left)1\. padding-top2\. padding-right3\. padding-bottom4.padding-left

| <style>.box{border:1px solid #cccccc;width:300px;border-radius:8px;padding:15px 15px 15px 15px;}</style><div class ="box" >Love is patient, love is kind. It does not envy, it does not boast, it is not proud. It is not rude, it is not self-seeking, it is not easily angered, it keeps no record of wrongs. Love does not delight in evil but rejoices with the truth. It always protects, always trusts, always hopes, always perseveres.</div> |

10\. defines the space between two inline elements, inside of the div's box.![](Image00013.jpg)line-height: CSS property defines the space between two inline elements.<br>: html tag break a new line.

| <style>.box{border:1px solid #cccccc;width:300px;border-radius:8px;padding:15px 15px 15px 15px;line-height:40px;}</style><div class ="box" >Love never fails.<br>Love is patient<br>love is kind<br>It always hopes</div> |

11. insert image to the div's box.![](Image00014.jpg)<img>: tag defines an image in an HTML page. src ="shirt.jpg" image path.

| <style>.box{border:1px solid #cccccc;width:250px;border-radius:8px;padding:15px 15px 15px 15px;}</style><div class ="box" ><img src ="shirt.jpg" /></div> |

12\. insert text below image to the div's box.![](Image00015.jpg)![](Image00016.jpg)#id: CSS to select an element with a specific id

| <style>.box{border:1px solid #cccccc;width:250px;border-radius:8px;padding:15px 15px 15px 15px;}#imgBox{width:100%;}#textBox{text-align:center;width:100%;line-height:30px;}</style><div class ="box" ><div id ="imgBox" ><img src ="shirt.jpg" /></div><div id ="textBox" >Life can be love t-shirt.</div></div> |

13\. Text wraps around the image.![](Image00017.jpg)float: CSS property specifies how an element should float. (left, right, clear).box img: Descendant selector the CSS style will be used in child element.font-family: "Times New Roman", Times, serif;

| <style>.box{border:1px solid #cccccc;width:250px;border-radius:8px;padding:15px 15px 15px 15px;font-size:16px;font-family: "Times New Roman", Times, serif;}.box img{width:80px;float:left;}</style><div class ="box" ><img src ="shirt.jpg" />Love is patient, love is kind. It does not envy, it does not boast, it is not proud. It is not rude, it is not self-seeking, it is not easily angered, it keeps no record of wrongs. Love does not delight in evil but rejoices with the truth. It always protects, always trusts, always hopes, always perseveres.</div> |

14. unordered list: starts with the <ul> tag. Each list item starts with the <li> tag.![](Image00018.jpg)

| <style>#box{border:1px solid #cccccc;width:250px;border-radius:8px;padding:15px 15px 15px 15px;font-size:16px;font-family: "Times New Roman", Times, serif;}</style><div id ="box" ><ul><li> Easy Learning HTML CSS </li><li> Easy Learning Javascript </li><li> Easy Learning Python 3 </li></ul></div> |

15\. unordered list: insert icon image replace the black dot.![](Image00019.jpg)list-style-image:url('icon.jpg'); CSS property is used to specify an image that is to be used as a marker

| <style>#box{border:1px solid #cccccc;width:250px;border-radius:8px;padding:15px 15px 15px 15px;font-size:16px;font-family: "Times New Roman", Times, serif;}#box ul li{list-style-image:url('icon.jpg');}</style><div id ="box" ><ul><li> Easy Learning HTML CSS </li><li> Easy Learning Javascript </li><li> Easy Learning Python 3 </li></ul></div> |

16. Link status style![](Image00020.jpg)text-decoration: none; Remove text-decoration from textli a:link: is used to select elements when not visitedli a:hover: is used to select elements when you mouse over them.li a.active: CSS pseudo-class. It specifies <li> <a> on a state the active

| <style>#box{border:1px solid #cccccc;width:250px;border-radius:8px;padding:15px 15px 15px 15px;font-size:16px;font-family: "Times New Roman", Times, serif;}#box ul li a:link{color:#000000;text-decoration: none;}#box ul li a:hover{color:#0000ff;}#box ul li a:active{color:#ff0000;}</style><div id ="box" ><ul><li><a href ="#" > Easy Learning HTML CSS </a></li><li><a href ="#" > Easy Learning Javascript </a></li><li><a href ="#" > Easy Learning Python 3 </a></li></ul></div> |

17. Drop-down menu![](Image00021.jpg)list-style-type: none: CSS property Remove marker is shown in the <li>display: block;  Displays an element as a block (like <div>). It starts on a new line.li a:hover:not(.active): is used to select elements when you mouse over them but not active

| <style>ul {list-style-type: none;margin: 0;padding: 0;width: 300px;background-color: #eeeeee;}li a {display: block;color: #000000;padding: 8px 16px;text-decoration: none;}li a.active {background-color: #075272;color: white;}li a:hover:not(.active) {background-color: #59c9f9;color: white;}</style><ul><li><a class ="active" href ="#" > Books </a></li><li><a href ="#" > Easy Learning Javascript </a></li><li><a href ="#" > Easy Learning Java </a></li><li><a href ="#" > Easy Learning Python 3 </a></li></ul> |

18. Navigate menu![](Image00022.jpg)

| <style>ul {list-style-type: none;margin: 0;padding: 0;overflow: hidden;background-color: #333;position: fixed;top: 10;width: 100%;}li {float: left;}li a {display: block;color: white;text-align: center;padding: 15px;text-decoration: none;}li a:hover:not(.active) {background-color: #fde352;}.active {background-color: #fde352;}</style><ul><li><a class ="active" href ="#" > HTML </a></li><li><a href ="#" > CSS </a></li><li><a href ="#" > Javascript </a></li><li><a href ="#" > Python </a></li></ul> |

19. click drop down menu![](Image00023.jpg)

| <style>.menubtn {background-color: #000000;color: white;padding: 16px;font-size: 16px;border: none;cursor: pointer;}.menudown {position: relative;display: inline-block;float:left;}.menudown-content {display: none;position: absolute;right: 0;background-color: #f9f9f9;min-width: 300px;}.menudown-content a {color: black;padding: 12px 16px;text-decoration: none;display: block;}.menudown-content a:hover {background-color: #f1f1f1}.menudown:hover .menudown-content {display: block;}.menudown:hover .menubtn {background-color: #000000;}</style><div class ="menudown" ><button class ="menubtn" > Books </button><div class ="menudown-content" style ="left:0;" ><a href ="#" > Easy Learning HTML CSS </a><a href ="#" > Easy Learning Javascript </a><a href ="#" > Easy Learning Java </a></div></div> |

20. login div dialog .![](Image00024.jpg)

| <style>#login{border:1px solid #cccccc;width:250px;border-radius:8px;padding:15px 15px 15px 15px;font-size:16px;font-family: "Times New Roman", Times, serif;}#login div{line-height:30px;width:100%;}.textbox{width:160px;}#buttonDiv{text-align:center;}#buttonDiv input{border:1px solid #cccccc;background-color:#ffffff;}</style><div id ="login" ><div> Username: <input class ="textbox" type ="text" id ="username" /></div><div> Password: <input class ="textbox" type ="password" id ="username" /></div><div id ="buttonDiv" ><input type ="button" value ="Login" /><input type ="button" value ="Close" /></div></div> |

Javascript HelloWorldJavascript is a web page dynamic interactive language that used in web development.1\. Create a helloworld.html file with Notepad and open it in your browser to see the webpage<html>: tag tells the browser that this is an HTML document.<head>: tag is a container for metadata about content and charset.<title>: tag defines the title of the document.<body>: tag defines the document's body.<script>: tag is used to define a client-side script (JavaScript).document.write(): writes HTML content to document in browser

| <html><head><meta http-equiv ="Content-Type" content ="text/html; charset=UTF-8" ><title> First Web Page </title></head><body><script type ="text/javascript" >document.write( "HelloWorld" );</script></body></html> |

Result:![](Image00025.jpg)Variable![](Image00026.jpg)1.Create a file : Variable.html and open it in your browser//  : single comments are not executed by javascript"": string type

| <script type ="text/javascript" >var basket = "Apple" ;document.write( basket);</script> |

Result:![](Image00027.jpg)2.Change file : Variable.html Put " orange " to replace " apple " .![](Image00028.jpg)<br>: html tag wrap a new line

| <script type ="text/javascript" >var basket = "Apple" ;document.write( basket);document.write( "<br>" );basket = "Orange" ;document.write( basket);</script> |

Run Result:![](Image00029.jpg)Variable and TypeJavascript is dynamic type language1\. Create a var.html file with Notepad and open it in your browser to see the webpagetypeof(): find the type of a JavaScript variable

| <script type ="text/javascript" >var x;           //undefinedvar a= 9 ;         //numbervar b= 1.5 ;       //numbervar c= true ;      //Booleanvar d= "abc" ;     //stringvar e= 'abc' ;     //stringdocument.write( typeof ( x) + "<br>" );document.write( typeof ( a) + "<br>" );document.write( typeof ( b) + "<br>" );document.write( typeof ( c) + "<br>" );document.write( typeof ( d) + "<br>" );document.write( typeof ( e) + "<br>" );</script> |

Result:undefinednumbernumberbooleanstringstringArithmetic Operator1\. Create a ArithmeticOperator.html file with Notepad and open it in your browserArithmetic Operator:Add +, minus -, multiply *, divisible /, take modulo %![](Image00030.jpg)

| <script type ="text/javascript" >var a = 1 ;var b = 2 ;var c = 3 ;var d = 4 ;document.write( a + b); // = 3document.write( "<br>" );document.write( a - b); // = -1document.write( "<br>" );document.write( a * b); // = 2document.write( "<br>" );document.write( b / a); // = 2document.write( "<br>" );document.write( c % b); // = 1 //number remaining after dividedocument.write( "<br>" );</script> |

Function![](Image00031.jpg)![](Image00032.jpg)![](Image00033.jpg)1.Create a file : Function.html

| <script type ="text/javascript" >function add( a, b){return a + b;}var result = add( 4 , 2 );document.write( result); // 6document.write( "<br>" );var result = add( 5 , 3 );document.write( result)   // 8</script> |

Run Result:682\. Add 3 more functions about - , *, / to Function.html

| <script type ="text/javascript" >function add( a, b){return a + b;}function sub( a, b){return a - b;}function multiply( a, b){return a * b;}function divide( a, b){return a / b;}var result = add( 4 , 2 );document.write( result); // 6document.write( "<br>" );var result = sub( 4 , 2 );document.write( result)   // 2document.write( "<br>" );var result = multiply( 4 , 2 );document.write( result)   // 8document.write( "<br>" );var result = divide( 4 , 2 );document.write( result)   // 2</script> |

Class![](Image00034.jpg)1.Create a file : Caculator.html

| <script type ="text/javascript" >function Caculator(){this.add= function ( a, b){return a + b;}this.sub= function ( a, b){return a - b;}this.multiply= function ( a, b){return a * b;}this.divide= function ( a, b){return a / b;}}var cal = new Caculator();var result = cal.add( 4 , 2 );document.write( result); // 6var result = cal.sub( 4 , 2 );document.write( result)   // 2var result = cal.multiply( 4 , 2 );document.write( result)   // 8var result = cal.divide( 4 , 2 );document.write( result)   // 2</script> |

Type Conversion1\. Create a TypeConversion.htmlparseInt(): this is javascript default function can convert string to integer.

| <script type ="text/javascript" >var a= "1" ;        var b= "2" ;    var result = a + b; // + concatenate two stringsdocument.write( result); // = 12document.write( "<br>" );result = parseInt( a) + parseInt( b);document.write( result); // = 3</script> |

Result:123DOMDOM: In Javascript every HTML element is a class object.Document Object Model structure diagram:![](Image00035.jpg)1.Create a file : getElementById.htm ldocument.getElementById(): is a DOM method to get the element by ID attribute.alert(): is a function to open a information window.Obj.innerHTML: sets or returns the inner HTML content of an element.<div>: tag defines a division or a section in an HTML document.

| <div id ="word" > Faith and Hope </div><script type ="text/javascript" >var divObj = document.getElementById( "word" );var htmlContent = divObj.innerHTML;alert( htmlContent);</script> |

![](Image00036.jpg)2.Change a file : getElementById.htm l<input type= " text " />: html tag specifies an input field where the user can enter data.

| <input type ="text" id ="username" value ="Joseph" /><script type ="text/javascript" >var divObj = document.getElementById( "username" );var value = divObj.value;alert( value);</script> |

![](Image00037.jpg)Event1.Create a file : onClick.htmlonClick: when the mouse clicks the button will call a function.<input type= " button " />: html tag defines a clickable button.

| <input type ="text" id ="username" value ="Joseph" /><input type ="button" value ="Click Me" onClick ="doClick()" /><script type ="text/javascript" >function doClick(){var divObj = document.getElementById( "username" );var value = divObj.value;alert( value);}</script> |

![](Image00038.jpg)Create a Web Caculator1.Create a file : WebCaculator.html![](Image00039.jpg)

| a: <input type ="text" id ="a" value ="" />b: <input type ="text" id ="b" value ="" />=<span id ="result" ></span><br><input type ="button" value ="+" onClick ="doAdd()" /><script type ="text/javascript" >function doAdd(){var aObj = document.getElementById( "a" );var bObj = document.getElementById( "b" );var resultObj = document.getElementById( "result" );var a = parseInt( aObj.value); // Convert string to integervar b = parseInt( bObj.value);resultObj.innerHTML = a + b;}</script> |

2.Add 3 mores function - , * , / to WebCaculator.html

| a: <input type ="text" id ="a" value ="" />b: <input type ="text" id ="b" value ="" />=<span id ="result" ></span><br><input type ="button" value ="+" onClick ="doAdd()" /><input type ="button" value ="-" onClick ="doSub()" /><input type ="button" value ="*" onClick ="doMultiply()" /><input type ="button" value ="/" onClick ="doDivide()" /><script type ="text/javascript" >function doAdd(){var aObj = document.getElementById( "a" );var bObj = document.getElementById( "b" );var resultObj = document.getElementById( "result" );var a = parseInt( aObj.value); // Convert string to integervar b = parseInt( bObj.value);resultObj.innerHTML = a + b;}function doSub(){var aObj = document.getElementById( "a" );var bObj = document.getElementById( "b" );var resultObj = document.getElementById( "result" );var a = parseInt( aObj.value); // Convert string to integervar b = parseInt( bObj.value);resultObj.innerHTML = a - b;}function doMultiply(){var aObj = document.getElementById( "a" );var bObj = document.getElementById( "b" );var resultObj = document.getElementById( "result" );var a = parseInt( aObj.value); // Convert string to integervar b = parseInt( bObj.value);resultObj.innerHTML = a * b;}function doDivide(){var aObj = document.getElementById( "a" );var bObj = document.getElementById( "b" );var resultObj = document.getElementById( "result" );var a = parseInt( aObj.value); // Convert string to integervar b = parseInt( bObj.value);resultObj.innerHTML = a / b;}</script> |

Click + button Result:![](Image00040.jpg)Click - button Result:![](Image00041.jpg)Click * button Result:![](Image00042.jpg)Click / button Result:![](Image00043.jpg)Assignment Operator1\. Create a AssignmentOperator.html file with Notepad and open it in your browser

| <script type ="text/javascript" >var d = 4 ;document.write( d++); // = 4 print d and then increment 1document.write( "<br>" );d = 4 ;document.write(++ d); // = 5 increment 1 and then print ddocument.write( "<br>" );d = 4 ;document.write( d--); // = 4 print d and then decrement 1document.write( "<br>" );d = 4 ;document.write(-- d); // = 3 decrement 1 and then print dvar result = 10 ;result = result + 1 ;document.write( result); // = 11document.write( "<br>" );result = 10 ;result++;document.write( result); // = 11document.write( "<br>" );result = 10 ;result += 1 ;document.write( result);   // = 11document.write( "<br>" );</script> |

2\. Create a quantity adder and subtracter   quantity.htmlClick + button to increase the quantity by 1, and click - button to decrease the quantity by 1.![](Image00044.jpg)

| Quantity:<br><input type ="text" style ="width:30px" id ="quantity" value ="1" /><input type ="button" value ="+" onClick ="doAdd()" /><input type ="button" value ="-" onClick ="doSub()" /><script type ="text/javascript" >function doAdd(){var quantityObj = document.getElementById( "quantity" );var value = parseInt( quantityObj.value);value++quantityObj.value = value;}function doSub(){var quantityObj = document.getElementById( "quantity" );var value = parseInt( quantityObj.value);value--quantityObj.value = value;}</script> |

Relational Operator1\. Create a RelationalOperator.html file with Notepad and open it in your browserRelational operators only two value: true, false

| <script type ="text/javascript" >document.write( 1 > 2 ); // falsedocument.write( "<br>" );document.write( 1 >= 1 ); // truedocument.write( "<br>" );document.write( 1 < 2 ); // truedocument.write( "<br>" );document.write( 1 <= 2 ); // truedocument.write( "<br>" );document.write( 1 == 1 ); // truedocument.write( "<br>" );document.write( 1 != 2 ); // true</script> |

If Conditional StatementIf statement1\. if (expression){statement}2\. if (expression) { statement } else { statement }3\. if (expression) {statement } else if { statement }1\. Create a If.html file with Notepad and open it in your browserScore example:if score == 5 :  Excellentelse if score == 4 :   Goodelse : Need to catch up![](Image00045.jpg)![](Image00046.jpg)![](Image00047.jpg)

| Please input your score:<br><input type ="text"   id ="score" value ="" /><input type ="button" value ="Submit" onClick ="doSubmit()" /><br><span id ="message" ></span><script type ="text/javascript" >function doSubmit(){var scoreObj = document.getElementById( "score" );var messageObj = document.getElementById( "message" );var score = parseInt( scoreObj.value);if ( score == 5 ) {messageObj.innerHTML = "Excellent" ;} else if ( score == 4 ) {messageObj.innerHTML = "Good" ;} else {messageObj.innerHTML = "Need to catch up" ;}}</script> |

Logic Operator1\. Create a LogicOperator.html file with Notepad and open it in your browserLogical Operator: and &&, or ||, not !1\. && returns true if both sides of the operation are true, otherwise false2\. || The result is false when both sides of the operation are false, otherwise true;3\. ! if returns true, the result is false, otherwise is true

| <script type ="text/javascript" >document.write( true && false ); // falsedocument.write( "<br>" );document.write( false && true ); // falsedocument.write( "<br>" );document.write( false && false ); // falsedocument.write( "<br>" );document.write( true && true ); // truedocument.write( "<br>" );document.write( true &#124;&#124; false ); // truedocument.write( "<br>" );document.write( false &#124;&#124; true ); // truedocument.write( "<br>" );document.write( true &#124;&#124; true ); // truedocument.write( "<br>" );document.write( false &#124;&#124; false ); // falsedocument.write( "<br>" );document.write(! true ); // falsedocument.write( "<br>" );document.write(! false ); // truedocument.write( "<br>" );</script> |

2\. Create a LogicOperator2.html

| <script type ="text/javascript" >document.write( 1 > 2 && 3 > 4 ) // = falsedocument.write( 2 > 1 && 3 > 4 ) // = falsedocument.write( "--------------" )document.write( 2 > 1 &#124;&#124; 3 > 4 ) // = truedocument.write( 2 > 1 &#124;&#124; 3 > 4 ) // = truedocument.write( 1 > 2 &#124;&#124; 3 > 4 ) // = false</script> |

3\. Payroll tax example:Tax amount = salary * tax ratelevel:500 -- 2000 $ : tax rate 10%2000--5000 $ :   tax rate 15%5000-- 20000 $ : tax rate 20%More than 20000$ :   tax rate 30%

| <script type ="text/javascript" >var salary = 10000 ;var tax = 0 ;if ( salary >= 500 && salary < 2000 ) {tax = salary * 0.1 ;} else if ( salary >= 2000 && salary < 5000 ) {tax = salary * 0.15 ;} else if ( salary >= 5000 && salary < 20000 ) {tax = salary * 0.2 ;} else {tax = salary * 0.3 ;}document.write( "tax amount=" + tax);</script> |

Result:tax amount=20002\. Create a WebTax.htm lInput salary and then click Calculate Tax button![](Image00048.jpg)

| Salary: <input type ="text" id ="salary" value ="" />=<span id ="tax" ></span><input type ="button" value ="Calculate Tax" onClick ="doTax()" /><script type ="text/javascript" >function doTax(){var salaryObj = document.getElementById( "salary" );var salary = parseInt( salaryObj.value);var tax = 0 ;if ( salary >= 500 && salary < 2000 ) {tax = salary * 0.1 ;} else if ( salary >= 2000 && salary < 5000 ) {tax = salary * 0.15 ;} else if ( salary >= 5000 && salary < 20000 ) {tax = salary * 0.2 ;} else {tax = salary * 0.3 ;}document.getElementById( "tax" ). innerHTML = tax;}</script> |

Switch Statement1\. Create a switch.html file with Notepad and open it in your browserInput a number 1 , 2, 31 : Pay by Visa Card2 : Pay by Master Card3: Pay by PaypalOtherwise Pay by face to face

| <script type ="text/javascript" >var num = 1 ;switch ( num) {case 1 :document.write( "Pay by Visa Card" );break ; // terminate the code to continue executioncase 2 :document.write( "Pay by Master Card" );break ;case 3 :document.write( "Pay by Paypal" );break ;default :document.write( "Pay by face to face" );}</script> |

Result:Pay by Visa Card2\. Create a WebPay.htmlthis: current element object![](Image00049.jpg)

| <input type ="radio" name ="card" value ="1" onclick ="doPay(this)" /> Visa Card<input type ="radio" name ="card" value ="2" onclick ="doPay(this)" /> Master Card<input type ="radio" name ="card" value ="3" onclick ="doPay(this)" /> Paypal<br><span id ="result" ></span><script type ="text/javascript" >function doPay( obj){var num = parseInt( obj.value);var resultObj = document.getElementById( "result" );switch ( num) {case 1 :resultObj.innerHTML = "Pay by Visa Card" ;break ;case 2 :resultObj.innerHTML = "Pay by Master Card" ;break ;case 3 :resultObj.innerHTML = "Pay by Paypal" ;break ;default :resultObj.innerHTML = "Pay by face to face" ;}}</script> |

While Loop Statementwhile (expression){statement;}continues execution if the expression is true , otherwise exits loop![](Image00050.jpg)1\. Create a WhileLoop.html file with Notepad and open it in your browser

| <script type ="text/javascript" >var i = 0 ;while ( i < 10 ){document.write( i+ "," );i++;}</script> |

Result:0,1,2,3,4,5,6,7,8,9,For Loop Statement![](Image00051.jpg)1\. Create a ForLoop.html file with Notepad and open it in your browser

| <script type ="text/javascript" >for ( var i = 0 ; i < 10 ; i++) {document.write( i + "," );}</script> |

Result:0,1,2,3,4,5,6,7,8,9,One-Dimensional Array![](Image00052.jpg)1\. Create a OneArray.html file with Notepad and open it in your browser

| <script type ="text/javascript" >// One-dimensional array definition and initializationvar scores = [ 90 , 70 , 50 , 80 , 60 , 85 ];document.write( scores[ 0 ] + "<br>" );document.write( scores[ 2 ] + "<br>" );document.write( scores[ 4 ] + "<br>" );</script> |

Result:9050602\. Change OneArray.html   print all scores of the arra yScores.length: the total count of array

| <script type ="text/javascript" >var scores = [ 90 , 70 , 50 , 80 , 60 , 85 ];//print all the scores of the arrayfor ( var i = 0 ; i < scores.length; i++) {document.write( scores[ i] + "," );}</script> |

Result:90,70,50,80,60,85,3\. Change OneArray.html   print all scores of the array

| <script type ="text/javascript" >// Dynamically define a one-dimensional arrayvar scores = new Array();scores[ 0 ] = 90 ;scores[ 1 ] = 70 ;scores[ 2 ] = 50 ;scores[ 3 ] = 80 ;scores[ 4 ] = 60 ;scores[ 5 ] = 85 ;//print all the scores of the arrayfor ( var i = 0 ; i < scores.length; i++) {document.write( scores[ i] + "," );}</script> |

Result:90,70,50,80,60,85,Select All Check Box![](Image00053.jpg)1\. Create a SelectCheckBox.html file with Notepad and open it in your browserdocument.getElementsByName(): get an array of elements with the same namechecked: if the checkbox is checked

| <table width ="400" border ="1" ><tr><td><input type ="checkbox" onclick ="checkAll(this)" /> Select All </td><td> Book Name </td></tr><tr><td><input type ="checkbox" name ="book" /></td><td> Easy Learning Java </td></tr><tr><td><input type ="checkbox" name ="book" /></td><td> Easy Learning Python 3 </td></tr></table><script language= "JavaScript" >function checkAll( obj){var bookArray= document.getElementsByName( "book" );for ( var i= 0 ; i< bookArray.length; i++){bookArray[ i]. checked= obj.checked;}}</script> |

Two-Dimensional Array![](Image00054.jpg)1\. Create a TwoArray.html file with Notepad and open it in your browser

| <script type ="text/javascript" >// Two-dimensional array definition and initializationvar arrs =[[ 10 , 20 , 30 ],[ 40 , 50 , 60 ],[ 70 , 80 , 90 ]];document.write( arrs[ 0 ][ 0 ] + "<br>" );document.write( arrs[ 0 ][ 2 ] + "<br>" );document.write( arrs[ 1 ][ 2 ] + "<br>" );</script> |

Result:1030602\. Create a TwoArray2.html file with Notepad and open it in your browser![](Image00055.jpg)

| <script type ="text/javascript" >var arrs =[[ 10 , 20 , 30 ],[ 40 , 50 , 60 ],[ 70 , 80 , 90 ]];// i: row index, j: column indexfor ( var i = 0 ; i < arrs.length; i++) {for ( var j = 0 ; j < arrs[ i]. length; j++) {document.write( arrs[ i][ j]);document.write( " " );}document.write( "<br>" );}</script> |

Find Dog Game1\. Draw buttons according to two-dimensional array maps![](Image00056.jpg)

| <style>input{width:40px;height:40px;}</style><span id ="result" ></span><script type ="text/javascript" >var maps =[[ 1 , 1 , 1 , 1 ],[ 1 , 1 , 1 , 1 ],[ 1 , 2 , 1 , 1 ],[ 1 , 1 , 1 , 1 ]];var mapHTML = "" ;for ( var i = 0 ; i < maps.length; i++) {for ( var j = 0 ; j < maps[ i]. length; j++) {mapHTML += "<input type='button' value=' ' />" ;}mapHTML += "<br>" ;}document.getElementById( "result" ). innerHTML = mapHTML;</script> |

2\. Fill in the value of the array into the button, and add a button click event, if button value is 1 becomes * , if button value is 2 becomes Dog![](Image00057.jpg)1:      *2:     Dog

| <style>input{width:40px;height:40px;}</style><span id ="result" ></span><script type ="text/javascript" >var maps =[[ 1 , 1 , 1 , 1 ],[ 1 , 1 , 1 , 1 ],[ 1 , 2 , 1 , 1 ],[ 1 , 1 , 1 , 1 ]];var mapHTML = "" ;for ( var i = 0 ; i < maps.length; i++) {for ( var j = 0 ; j < maps[ i]. length; j++) {mapHTML += "<input type='button' value=' ' onClick='doButtonClick(this," + maps[ i][ j]+ ")' />" ;}mapHTML += "<br>" ;}document.getElementById( "result" ). innerHTML = mapHTML;function doButtonClick( obj, value){if ( value == 1 ){obj.value = "*" ;} else if ( value == 2 ){obj.value = "Dog" ;}}</script> |

3\. Print random numbers 0-9Math.random(): returns a random number between 0  and 1.Math.floor(): rounds a number downwards to the nearest integer

| <script type ="text/javascript" >for ( var i= 0 ; i< 10 ; i++){var num = Math.floor( Math.random() * 10 )document.write( num + ", " );}</script> |

Result:9, 3, 9, 0, 4, 1, 0, 3, 4, 5,4\. Randomly generate 1- 2 initialize two-dimensional array, Fill in the value of the array into the button, and add a button click event, if button value is 1 becomes * , if button value is 2 becomes Dog![](Image00058.jpg)1:      *2:     DogSecondary Linkage Drop-down1\. Create a Drop-down.html file with Notepad and open it in your browserwindow.onload: execute a function after a page has been loadeddocument.createElement(): create a html element![](Image00059.jpg)

| <select id ="country" ><option value ="" > --Please Select Country-- </option></select><script type ="text/javascript" >window.onload= function (){var countryObj= document.getElementById( "country" );option= document.createElement( "option" );option.text= "United States" ;option.value= "United States" ;countryObj.options[ countryObj.options.length]= option;}</script> |

2\. Add more options by countryArray![](Image00060.jpg)

| <select id ="country" ><option value ="" > --Please Select Country-- </option></select><script type ="text/javascript" >var countryArray=[ "China" , "United States" ];window.onload= function (){var countryObj= document.getElementById( "country" );for ( var i= 0 ; i< countryArray.length; i++){var option= document.createElement( "option" );option.text= countryArray[ i];option.value= countryArray[ i];countryObj.options[ countryObj.options.length]= option;}}</script> |

3\. Add province option sselectedIndex: sets or returns the index of the selected option in a drop-down list.![](Image00061.jpg)

| <select id ="country" onchange ="doCountryChange(this)" ><option value ="" > --Please Select Country-- </option></select><select id ="province" ></select><script type ="text/javascript" >var countryArray=[ "China" , "United States" ];var provinceArray = new Array();provinceArray[ 0 ] =[];provinceArray[ 1 ] =[ "Beijing" , "Shanghai" ];provinceArray[ 2 ] =[ "San Francisco" , "New York" ];window.onload= function (){var country= document.getElementById( "country" );for ( var i= 0 ; i< countryArray.length; i++){var option= document.createElement( "option" );option.text= countryArray[ i];option.value= countryArray[ i];country.options[ country.options.length]= option;}}function doCountryChange( obj){var provinceObj= document.getElementById( "province" );provinceObj.options.length= 0 ; // clear allvar index= obj.selectedIndex;for ( var i= 0 ; i< provinceArray[ index]. length; i++){var option= document.createElement( "option" );option.text= provinceArray[ index][ i];option.value= provinceArray[ index][ i];provinceObj.options[ provinceObj.options.length]= option;}}</script> |

EventEvent List:

| Onblur | element loses focus |
| Onchange | changes the contents |
| Onclick | mouse click on an object |
| Ondblclick | mouse double click on an object |
| Onerror | An error occurred while loading a document or image |
| Onfocus | element gets focus |
| Onkeydown | The key of a keyboard is pressed |
| Onkeypress | The key of a keyboard is pressed |
| Onkeyup | The key of a keyboard is released |
| Onload | a page or image is loaded |
| Onmousedown | a mouse button is pressed |
| Onmousemove | mouse is moved |
| Onmouseout | mouse is moved out from an element |
| Onmouseover | mouse is moved over an element |
| Onmouseup | mouse button is released |
| Onreset | reset button is clicked |
| Onresize | window or frame is resized |
| Onselect | text is selected |
| Onsubmit | submit button is clicked |
| Onunload | exit page |

Login Web Page![](Image00062.jpg)1\. Create a Login.html file with Notepad and open it in your browser

| Username: <input type ="text" id ="username"   value =""   /> <br>Password: <input type ="password"   id ="pwd"   value =""   /> <br><input type ="button" value ="Login" onclick ="checkLogin()"   /><script   type ="text/javascript" >function checkLogin(){var usernameObj= document.getElementById( "username" );var pwdObj= document.getElementById( "pwd" );if ( usernameObj.value== "" ){alert( "Please input username !" );return ;}if ( pwdObj.value== "" ){alert( "Please input password !" );return ;}alert( "login successfull !" );}</script> |

2\. Create a Login.html file with Notepad and open it in your browserdocument.onkeypress: the event occurs when the user presses a key.

| Username: <input type ="text" id ="username"   value =""   /><br>Password: <input type ="password"   id ="pwd"   value =""   /><br><input type ="button" value ="Login" onclick ="checkLogin()"   /><script   type ="text/javascript" >document.onkeypress= function ( event){var ext= window.event? window.event: event;var key= ext.keyCode? ext.keyCode: ext.which;if ( key== 13 ) // press enter key will be invoked{checkLogin();}}function checkLogin(){var usernameObj= document.getElementById( "username" );var pwdObj= document.getElementById( "pwd" );if ( usernameObj.value== "" ){alert( "Please input username !" );return ;}if ( pwdObj.value== "" ){alert( "Please input password !" );return ;}alert( "login successfull !" );}</script> |

MouseOver Thumbnail to Larger![1554891382(1)](Image00063.jpg)1\. Create a ThumbnailLarger.html file with Notepad and open it in your browser<img>: tag defines an image in an HTML page.

| <img src ="images/java.jpg" width ="60"   onmouseover ="zoomImage(this)" /><img src ="images/python.jpg" width ="60"   onmouseover ="zoomImage(this)" /><img src ="images/csharp.jpg" width ="60"   onmouseover ="zoomImage(this)" /><hr><img id ="image" src="" /><script type ="text/javascript" >function zoomImage( obj){document.getElementById( "image" ). src = obj.src;}</script> |

Element Hierarchy![](Image00064.jpg)1\. Change ElementHierarchy.html to get all child nodes .obj.childNodes: ​ get all child nodes of current nodeobj . nodeName: ​ get the node’s nameobj . nodeType: ​ get the node’s typeobj . innerHTML: ​ get the node’s html content![](Image00065.jpg)<b>: tag specifies bold text.<a>: tag defines a hyperlink, which is used to link from one page to another.

| <body><div id ="div" ><b> United State </b><span> Book </span><a href ="#" > VereJava </a></div><hr><input type ="button" value ="Get Parent Node" onclick ="doGetParentNode()" /></body><script type ="text/javascript" >function doGetParentNode(){var divObj= document.getElementById( "div" );alert( divObj.parentNode.nodeName);}</script> |

2\. Change ElementHierarchy.html get all child node sobj.childNodes: ​ get all child nodes of current nodeobj.nodeName: ​ get the parent node’s nameobj.nodeType: ​ get the parent node’s typeobj.innerHTML: ​ get the parent node’s html content![](Image00066.jpg)

| <body><div id= "div" ><b> United State </b><span> Book </span><a href ="#" > VereJava </a></div><hr><input type ="button" value ="Get Child Nodes" onclick ="doGetChildNodes()" /></body><script type ="text/javascript" >function doGetChildNodes(){var div= document.getElementById( "div" );var childNodes= div.childNodes;for ( var i= 0 ; i< childNodes.length; i++){if ( childNodes[ i]. nodeType== 1 ){document.write( childNodes[ i]. nodeName+ " , " );document.write( childNodes[ i]. nodeType+ " , " );document.write( childNodes[ i]. innerHTML+ "<br>" );}}}</script> |

3\. Change ElementHierarchy.html get book node’s previous and next nod eobj . previousSibling: ​ get previous node of current nodeobj . nextSibling: ​ get next node of current node![](Image00067.jpg)

| <body><div id ="div" ><b> United State </b><span id ="book" > Book </span><a href ="#" > VereJava </a></div><hr><input type ="button" value ="Get Sliding Nodes" onclick ="doGetSliding()" /></body><script type ="text/javascript" >function doGetSliding(){var bookObj= document.getElementById( "book" );document.write( bookObj.previousSibling.innerHTML+ "<br>" );document.write( bookObj.nextSibling.innerHTML);}</script> |

Create Text Node![](Image00068.jpg)1\. Create a CreateTextNode.html file with Notepad and open it in your browse robj . createTextNode: ​ creates a Text Node with the specified textobj . appendChild: ​ appends a node as the last child of a node

| <style>div{width:200px;height:100px;border:1px solid #ff0000;}</style><div id ="div" ></div><input type ="button" value ="Create Text Node" onclick ="doCreateTextNode()" /><script type ="text/javascript" >function doCreateTextNode(){var divObj = document.getElementById( "div" );var newNode= document.createTextNode( "Good Dreams" );divObj.appendChild( newNode);}</script> |

2\. Create a CreateElement.html file with Notepad and open it in your browse robj . createElement: ​ creates an Element Node with the specified nameobj . appendChild: ​ appends a node as the last child of a node![](Image00069.jpg)

| <style>div{width:200px;height:100px;border:1px solid #ff0000;}</style><div id ="div" ></div><input type ="button" value ="Create Element" onclick ="doCreateElement()" /><script type ="text/javascript" >function doCreateElement(){var divObj = document.getElementById( "div" );var buttonElement= document.createElement( "input" );buttonElement.type= "button" ;buttonElement.value= "button" ;divObj.appendChild( buttonElement);}</script> |

Delete Node![](Image00070.jpg)1\. Create a DeleteNode.html file with Notepad and open it in your browse robj . removeChild: ​ removes a specified child node

| <style>div{width:200px;height:250px;border:1px solid #ff0000;}</style><div id ="div1" ><img id ="image" src ="python.jpg" /></div><br><input type ="button" value ="Remove Child" onclick ="doRemoveChild()" /><script type ="text/javascript" >function doRemoveChild(){var div= document.getElementById( "div1" );var img= document.getElementById( "image" );div.removeChild( img);}</script> |

Replace Node![](Image00071.jpg)1\. Create a ReplaceNode.html file with Notepad and open it in your browse robj . replaceChild: ​ replaces a child node with a new node

| <style>#div1{width:200px;height:200px;border:1px solid #ff0000;}</style><div id ="div1" > Everyone has inside them a piece of good news. </div><input type ="button" value ="Replace Child Node" onclick ="doReplaceChild()" /><script type ="text/javascript" >function doReplaceChild(){var imgNode= document.createElement( "img" );imgNode.src= "python.jpg" ;var div1= document.getElementById( "div1" );div1.replaceChild( imgNode, div1.childNodes[ 0 ]);}</script> |

Add Contact Example![](Image00072.jpg)1\. Create a AddContactExample.html file with Notepad and open it in your browser

| <style>#div{border:1px solid #ff0000;width:550px;}</style><a href ="javascript:void(0)" onclick ="addContact()" > Add Contact </a><div id ="div" ><div id ="contact" >Name: <input type ="text" name ="user" />Telephone: <input type ="text" name ="telephone" /><a href ="javascript:void(0)" onclick ="deleteNode(this)" > Delete </a></div></div><script type ="text/javascript" >function addContact(){var contact= document.getElementById( "contact" );var newNone= contact.cloneNode( true );var div= document.getElementById( "div" );div.appendChild( newNone);}function deleteNode( obj){if ( obj.parentNode.parentNode.childNodes.length> 1 )obj.parentNode.removeNode( true );}</script> |

CSS Style Font![](Image00073.jpg)1\. Create a CSSStyleFont.html file with Notepad and open it in your browser

| <div id ="div" > Choose to stay positive </div><input type ="button" value ="Change Font Style" onclick ="doChangeFont()" /><script type ="text/javascript" >function doChangeFont(){var div= document.getElementById( "div" );div.style.fontSize= 48 + "px" ;div.style.fontWeight= "bold" ;div.style.color= "#ff0000" ;}</script> |

CSS Change Class Selector![](Image00074.jpg)1\. Create a CSSClassSelector.html file with Notepad and open it in your browser

| <style type ="text/css" >.smallFont{font-size:12px;color:#ff0000;}.bigFont{font-size:48px;font-weight:bold;color:#00ff00;}</style><div id ="div" > Just keep doing every day. </div><input type ="button" value ="Change Font Class" onclick ="changeFont()" /><script type ="text/javascript" >function changeFont(){var div= document.getElementById( "div" );if ( div.className== "smallFont" ){div.className= "bigFont" ;}else{div.className= "smallFont" ;}}</script> |

CSS Overflow Expand and Close![1554913527(1)](Image00075.jpg)1\. Create a CSSExpandClose.html file with Notepad and open it in your browser

| <style type ="text/css" >.open{display :"" ;}.close{display :none ;}#div{width:300px;height:30px;border:1px solid #ff0000;text-align:right;}#div2{width:300px;border:1px solid #00ff00;}</style><div id ="div" onclick ="change()" > Chick Here </div><div id ="div2" ><ul><li> Don’t be afraid, for I am with you. </li><li> Your smile lights up the room. </li><li> You are doing an amazing job at life. </li></ul></div><script type ="text/javascript" >function change(){var div2= document.getElementById( "div2" );if ( div2.className== "open" ){div2.className= "close" ;}else{div2.className= "open" ;}}</script> |

CSS Floating Highlighting![](Image00076.jpg)1\. Create a CSSHighlighting.html file with Notepad and open it in your browser

| <style type ="text/css" >.over{background-color: #ff0000;}.down{background-color: #0000ff;}table{border:1px solid #eeeeee;width:400px;border-collapse: collapse;}table th{border:1px solid #eeeeee;background-color: #cccccc;}table td{border:1px solid #eeeeee;}</style><table><tr><th> Username </th><th> Password </th></tr><tr onmousedown ="doDown(this)" onmouseover ="doOver(this)" onmouseout ="doOut(this)" ><td> admin </td><td> 111111 </td></tr><tr onmousedown ="doDown(this)"   onmouseover ="doOver(this)" onmouseout ="doOut(this)" ><td> isacc </td><td> 222222 </td></tr><tr onmousedown ="doDown(this)"   onmouseover ="doOver(this)" onmouseout ="doOut(this)" ><td> sala </td><td> 333333 </td></tr></table><script type ="text/javascript" >function doOver( obj){if ( obj.className!= "down" ){obj.className= "over" ;}}function doOut( obj){if ( obj.className!= "down" ){obj.className= "" ;}}function doDown( obj){if ( obj.className!= "down" ){obj.className= "down" ;} else {obj.className= "over" ;}}</script> |

Table Create  Rows Columns![](Image00077.jpg)1\. Create a TableCreate RowsColumns.html file with Notepad and open it in your browsertable.insertRow: ​ inserts a new row (<tr>) in a given <table>, returns a reference to the new row.table . insertCell: ​ inserts a new col (<td>) in a given <tr>, returns a reference to the new col.Delete Table Row Column![](Image00078.jpg)1\. Create a DeleteTableRowColumn.html file with Notepad and open it in your browsertable . deleteCell: ​ delete a cell in the current table row.Timer![](Image00079.jpg)1\. Create a Timer.html file with Notepad and open it in your browsergetFullYear(): ​ Get the year as a four digit number (yyyy)getMonth(): ​         Get the month as a number (0-11)getDate(): ​         Get the day as a number (1-31)getHours(): ​         Get the hour (0-23)getMinutes(): ​ Get the minute (0-59)getSeconds(): ​ Get the second (0-59)getTime(): ​         Get the time (milliseconds since January 1, 1970)setInterval(): ​ continue calling the function until clearInterval() is called.

| <div id ="dateDiv" ></div><script type ="text/javascript" >function doSetInterval(){var dateDiv= document.getElementById( "dateDiv" );var d= new Date();var dateString = d.getHours()+ ":" + d.getMinutes()+ ":" + d.getSeconds()dateDiv.innerHTML= dateString;}setInterval( "doSetInterval()" , 1000 );</script> |

Canvas Progress BarCanvas: HTML <canvas> element is used to draw graphics on a web page.![](Image00080.jpg)1\. Create a Canvas.html file with Notepad and open it in your browser<style>: describes how HTML elements are to be displayed on screen.#id: The #id selector styles the element with the specified id.

| <style>#myCanvas{border:1px solid #c3c3c3;}</style><canvas id ="myCanvas" width ="400" height ="200" ></canvas> |

2. Draw  a line on Canvas![](Image00081.jpg)canvas.getContext("2d"): returns an object that provides methods for drawing on the canvas.

| <style>#myCanvas{border:1px solid #c3c3c3;}</style><canvas id ="myCanvas" width ="400" height ="200" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );//Begin a path create a line  move from (20,100) to (200,100):var context = canvas.getContext( "2d" );context.beginPath();context.moveTo( 20 , 100 );context.lineTo( 200 , 100 );context.stroke();</script> |

3. Draw  a Rectangle on Canvas![](Image00082.jpg)context.fillRect(x, y, width, height): draw a rectangle on the canvas.context.fillStyle: the color to fill rectangle(red : #ff0000, green: #00ff00, blue: #0000ff).

| <style>#myCanvas{border:1px solid #c3c3c3;}</style><canvas id ="myCanvas" width ="400" height ="200" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );//Begin a path create a rectanglevar context = canvas.getContext( "2d" );context.fillStyle = "#ff0000" ;context.fillRect( 100 , 50 , 100 , 50 );</script> |

4\. Draw Progress Bar Animation4.1. Draw an empty rectangle first4.2. Draw a solid rectangle, the width increasing by 10 every 200 milliseconds until width=100![](Image00083.jpg)context . strokeRect(x, y, width, height): draw a stroke rectangle on the canvas.

| <style>#myCanvas{border:1px solid #c3c3c3;}</style><canvas id ="myCanvas" width ="400" height ="200" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );context.strokeRect( 100, 50, 100, 20);var time = setInterval( "drawProgressBar()" , 200 );var width = 0 ;function drawProgressBar(){context.fillStyle = "#ff0000" ;context.fillRect( 100, 50, width, 20);width = width + 10 ;if ( width> 100 ){clearInterval( time);}}</script> |

Canvas Ball Bounce1\. Draw a circle on the canvas center= (100, 100) , r= 50 from 0 to 2*PI .![](Image00084.jpg)1\. Create a ball.html file with Notepad and open it in your browsercontext.arc(x,y,r,sAngle,eAngle): Rotate 360 degrees counterclockwise with x, y as the center and r as the radius.

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="200" height ="200" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );context.fillStyle = "#0000ff" ;context.beginPath();context.arc( 100 , 100 , 50 , 0 , 2 * Math.PI);context.fill();</script> |

2. Create a function drawBall(x, y, r, color) to draw 3 circle on the canvas .![](Image00085.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="400" height ="200" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );function drawBall( x, y, r, color){context.fillStyle = color;context.beginPath();context.arc( x, y, r, 0 , 2 * Math.PI);context.fill();}drawBall( 50 , 50 , 30 , "#ff0000" );drawBall( 120 , 50 , 30 , "#00ff00" );drawBall( 190 , 50 , 30 , "#0000ff" );</script> |

3\. Create a class Ball and then create a method draw() to draw 3 circle on the canvas .![](Image00085.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="400" height ="200" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );class Ball{constructor( x, y, r, color){this.x = x;this.y = y;this.r = r;this.color = color;}draw(){context.fillStyle = this.color;context.beginPath();context.arc( this.x, this.y, this.r, 0 , 2 * Math.PI);context.fill();}}//new Ball the constructor method will be called automaticallyvar redBall = new Ball( 50 , 50 , 30 , "#ff0000" );redBall.draw();var greenBall = new Ball( 120 , 50 , 30 , "#00ff00" );greenBall.draw();var blueBall = new Ball( 190 , 50 , 30 , "#0000ff" );blueBall.draw();</script> |

4. Create a Ball and then move down .![](Image00086.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="200" height ="250" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );class Ball{constructor( x, y, r, color){this.x = x;this.y = y;this.r = r;this.color = color;}draw(){context.fillStyle = this.color;context.beginPath();context.arc( this.x, this.y, this.r, 0 , 2 * Math.PI);context.fill();}move( distance){this.y = this.y + distance;}}var ball = new Ball( 100 , 50 , 30 , "#0000ff" );ball.draw();function continueRun(){context.clearRect( 0 , 0 , 200 , 250 ); //clear canvasball.move( 10 );ball.draw();}//Run every 200 millisecondsvar time = setInterval( "continueRun()" , 200 );</script> |

5. Ball Bounce Upwards and Downwards![](Image00087.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="200" height ="250" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );var canvasWidth= 200 ;var canvasHeight= 250 ;class Ball{constructor( x, y, r, color){this.x = x;this.y = y;this.r = r;this.color = color;}draw(){context.fillStyle = this.color;context.beginPath();context.arc( this.x, this.y, this.r, 0 , 2 * Math.PI);context.fill();}move( distance){this.y = this.y + distance;}getY(){return this.y;}getR(){return this.r;}}var ball = new Ball( 100 , 50 , 30 , "#0000ff" );ball.draw();var direction = "down" ;function continueRun(){context.clearRect( 0 , 0 , canvasWidth, canvasHeight);if ( ball.getY()+ ball.getR() < canvasHeight && direction == "down" ){ball.move( 10 );ball.draw();} else {direction = "up"}if ( ball.getY()- ball.getR() > 0 && direction == "up" ){ball.move(- 10 );ball.draw();} else {direction = "down"}}//Run every 200 millisecondsvar time = setInterval( "continueRun()" , 200 );</script> |

Create ClassAlmost everything is an object, with its properties and methods. Class is like an object constructor  for creating objects.In the game, planes, bullets, bombs, and enemy planes are  called class Sprite![](Image00088.jpg)1\. Create a class.html file with Notepad and open it in your browserConstruction method name must be constructorconstructor : when create object will be called automatically

| <script type ="text/javascript" >// defining a Sprite classclass Sprite{//constructor methodconstructor( name, color){this.name = name;this.color = color;}// defining method, this: is current objectdraw(){var text = this.color + " " + this.name+ "  is drawn on canvas" ;document.write( text+ "<br>" );}}//create the object constructor will be called automaticallyblueSprite = new Sprite( "Airplane" , "Blue" );//Use sprite access properties and methodsblueSprite.draw();redSprite = new Sprite( "Bullet" , "Blue" );redSprite.draw();</script> |

Result:Blue Airplane  is drawn on canvasBlue Bullet  is drawn on canvasInheritanceAll Class EnemyPlane, BluePane, RedPlane, Bullet inherit from Sprite1\. Sprite is called Parent Class2\. EnemyPlane, BluePane, RedPlane, Bullet are called Child Class3\. Child Class can call the properties and method from Parent Class![](Image00089.jpg)1\. Create a Inheritance.html file with Notepad and open it in your browser

| <script type ="text/javascript" >class Sprite{constructor( name, color){this.name = name;this.color = color;}draw(){var text = this.color + " " + this.name+ "  is drawn on canvas" ;document.write( text+ "<br>" );}}//BluePlane is Child, extends is inherit, Sprite is Parentclass BluePlane extends Sprite{}class RedPlane extends Sprite{}class Bullet extends Sprite{}blueSprite = new Sprite( "Airplane" , "Blue" );blueSprite.draw();redSprite = new Sprite( "Bullet" , "Blue" );redSprite.draw();redBullet= new Bullet( "Bullet" , "Red" )     redBullet.draw()</script> |

Result:Blue Airplane  is drawn on canvasRed Airplane  is drawn on canvasRed Bullet  is drawn on canvasOverrideOverride:the child class overrides the method of the parent class,the instance of the child class will call the overrided methodSprite can fire bullet, but BluePlane can fire blue bullet and RedPlane can fire red bullet.![](Image00090.jpg)

| <script type ="text/javascript" >class Sprite{shoot(){document.write( "fire bullet <br>" );}}// BluePlane Inherit Spriteclass BluePlane extends Sprite{shoot(){document.write( "BluePlane fire blue bullet <br>" );}}// RedPlane Inherit Spriteclass RedPlane extends Sprite{shoot(){document.write( "RedPlane fire red bullet <br>" );}}bluePlane = new BluePlane()bluePlane.shoot();redPlane = new RedPlane()redPlane.shoot();</script> |

Result:BluePlane fire blue bulletRedPlane fire red bulletAirplane Game1 . Draw a image on canvas.1.1 put the 2 plane image to directory        images/blue_plane.png.        images/red_plane.png        ![](Image00091.jpg) ![](Image00092.jpg)    1.2 draw images/blue_plane.png, images/red_plane.png on canvas.![](Image00093.jpg)All images in KidsLearningJavascriptImages.zip please find download from this link:[http://en.verejava.com/download.jsp?id=1](http://en.verejava.com/download.jsp?id=1)1\. Create a DrawImage.html file with Notepad and open it in your browserImage.onload: event occurs when an image has been loaded.drawImage(): draws an image onto the canvas.

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="300" height ="300" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );var bluePlaneImage = new Image();bluePlaneImage.src = "./images/blue_plane.png" ;bluePlaneImage.onload = function (){     context.drawImage( bluePlaneImage, 60 , 220 );         };var redPlaneImage = new Image();redPlaneImage.src = "./images/red_Plane.png" ;redPlaneImage.onload = function (){context.drawImage( redPlaneImage, 160 , 220 );               };</script> |

3 . Create Airplane class and then create draw method to create image on canvas.![](Image00094.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="300" height ="300" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );class Airplane{constructor( img, x, y){this.x = x;this.y = y;this.img = img;}draw( context){context.drawImage( this.img, this.x, this.y);}}//////////// test /////////////////var bluePlaneImage = new Image();bluePlaneImage.src = "./images/blue_plane.png" ;var bluePlane = new Airplane( bluePlaneImage, 60 , 220 );bluePlaneImage.onload = function (){     bluePlane.draw( context);         };var redPlaneImage = new Image();redPlaneImage.src = "./images/red_Plane.png" ;var redPlane = new Airplane( redPlaneImage, 160 , 220 );redPlaneImage.onload = function (){redPlane.draw( context);                };</script> |

4 . Keypress Event.    4.1 If click up, down, left, right key the function doKeyDown will be invoked.![](Image00095.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="300" height ="300" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );class Airplane{constructor( img, x, y){this.x = x;this.y = y;this.img = img;}draw( context){context.drawImage( this.img, this.x, this.y);}}//////////// test /////////////////var bluePlaneImage = new Image();bluePlaneImage.src = "./images/blue_plane.png" ;var bluePlane = new Airplane( bluePlaneImage, 60 , 220 );bluePlaneImage.onload = function (){     bluePlane.draw( context);         };var redPlaneImage = new Image();redPlaneImage.src = "./images/red_Plane.png" ;var redPlane = new Airplane( redPlaneImage, 160 , 220 );redPlaneImage.onload = function (){redPlane.draw( context);                };canvas.addEventListener( 'keydown' , doKeyDown, true );canvas.focus();window.addEventListener( 'keydown' , doKeyDown, true );function doKeyDown( e) {var keyID = e.keyCode ? e.keyCode : e.which;if ( keyID === 37 )   { //left arrowalert( "left" );e.preventDefault();}if ( keyID === 38 )   { //up arrowalert( "up" );e.preventDefault();}if ( keyID === 39 )   { //right arrowalert( "right" );e.preventDefault();}if ( keyID === 40 )   { //down arrowalert( "down" );e.preventDefault();}}</script> |

4 . Click Up , Down , Left , Right Key to move airplane on canvas.![](Image00096.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><canvas id ="myCanvas" width ="300" height ="300" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );var canvasWidth = 300 ;var canvasHeight = 300 ;class Airplane{constructor( img, x, y){this.x = x;this.y = y;this.img = img;}draw( context){context.drawImage( this.img, this.x, this.y);}move( context, distanceX, distanceY){this.x = this.x + distanceX;this.y = this.y + distanceY;context.drawImage( this.img, this.x, this.y);}}//////////// test /////////////////var bluePlaneImage = new Image();bluePlaneImage.src = "./images/blue_plane.png" ;var bluePlane = new Airplane( bluePlaneImage, 100 , 220 );bluePlaneImage.onload = function (){     bluePlane.draw( context);         };canvas.addEventListener( 'keydown' , doKeyDown, true );canvas.focus();window.addEventListener( 'keydown' , doKeyDown, true );function doKeyDown( e) {context.clearRect( 0 , 0 , canvasWidth, canvasHeight);var keyID = e.keyCode ? e.keyCode : e.which;if ( keyID === 37 )   { //left arrowbluePlane.move( context,- 5 , 0 )e.preventDefault();}if ( keyID === 38 )   { //up arrowbluePlane.move( context, 0 , - 5 )e.preventDefault();}if ( keyID === 39 )   { //right arrowbluePlane.move( context, 5 , 0 )e.preventDefault();}if ( keyID === 40 )   { //down arrowbluePlane.move( context, 0 , 5 )e.preventDefault();}}</script> |

5 . The Airplane fire a blue bullet.    5.1 The bullets fired from the top center of the plane![](Image00097.jpg)    5.2 Start a setInterval("reDraw()",200) to keep the bullet moving up,  when the bullet move out of the canvas, the bullet need be destroyed set visible = false, the bullet can be reissued.![](Image00098.jpg)5.3 Airplane and bullet inherit from Sprite from reuse.![](Image00099.jpg)6 . The enemyplane keep moving down.    6.1 The enemy plane randomly starts from top of canvas and moves down![](Image00100.jpg)    6.2 Keep the enemyplane moving down,  when the enemyplane move out of the canvas, the enemyplane need be destroyed set visible = False, the enemyplane can be reissued.![](Image00101.jpg)    6.3 Airplane, bullet and enemyplane inherit from Sprite from reuse.![](Image00102.jpg)7 . The bullet collided with the enemy plane and exploded.![](Image00103.jpg)    7.1 bullet collided with the enemy planeThe absolute value of the difference between the center coordinates of the two pictures is less than the sum of half of their width and height, we think they have an intersection and they are collided![](Image00104.jpg)

| <style>#myCanvas{border:1px solid #c3c3c3;position: absolute;}</style><span id ="dd" ></span><br><canvas id ="myCanvas" width ="300" height ="300" ></canvas><script type ="text/javascript" >var canvas = document.getElementById( "myCanvas" );var context = canvas.getContext( "2d" );var canvasWidth = 300 ;var canvasHeight = 300 ;class Sprite{constructor( img, x, y){this.x = x;this.y = y;this.img = img;}draw( context){context.drawImage( this.img, this.x, this.y);}move( context, distanceX, distanceY){this.x = this.x + distanceX;this.y = this.y + distanceY;}collideWith( sprite){var centerX = this.x + this.getWidth()/ 2 ;var centerY = this.y + this.getHeight()/ 2 ;var spriteCenterX = sprite.getX() + sprite.getWidth()/ 2 ;var spriteCenterY = sprite.getY() + sprite.getHeight()/ 2 ;if ( Math.abs( centerX - spriteCenterX) < ( this.width/ 2 + sprite.getWidth()/ 2 )&&Math.abs( centerY - spriteCenterY) <   ( this.height/ 2 + sprite.getHeight()/ 2 ))return trueelsereturn false}isVisible(){return this.visible;}setVisible( visible){this.visible = visible;}getX(){return this.x;}setX( x){this.x= x;}getY(){return this.y;}setY( y){this.y= y;}getHeight(){return this.height;}setHeight( height){this.height = height;}getWidth(){return this.width;}setWidth( width){this.width= width;}}class Airplane extends Sprite{}class Bullet extends Sprite{move( context, distanceX, distanceY){this.x = this.x + distanceX;this.y = this.y + distanceY;if ( this.y + this.height <= 0 ){this.setVisible( false )}}}class EnenmyPlane extends Sprite{move( context, distanceX, distanceY){this.x = this.x + distanceX;this.y = this.y + distanceY;if ( this.y >= canvasHeight){this.setVisible( false );}}}//////////// test /////////////////var bluePlaneImage = new Image();bluePlaneImage.src = "./images/blue_plane.png" ;var bluePlane = new Airplane( bluePlaneImage, 100 , 220 );bluePlaneImage.onload = function (){     bluePlane.setWidth( bluePlaneImage.width);bluePlane.setHeight( bluePlaneImage.height);bluePlane.draw( context);};var bulletImage = new Image();bulletImage.src = "./images/blue_bullet.png" ;var bullet = new Bullet( bulletImage,- 100 ,- 100 );bulletImage.onload = function (){     bullet.setWidth( bulletImage.width);bullet.setHeight( bulletImage.height);bullet.setVisible( false );bullet.draw( context);         };var enemyImage = new Image();enemyImage.src = "./images/enemy.png" ;var enemyPlane = new EnenmyPlane( enemyImage,- 100 ,- 100 );enemyImage.onload = function (){     enemyPlane.setWidth( enemyImage.width);enemyPlane.setHeight( enemyImage.height);enemyPlane.setVisible( false );enemyPlane.draw( context);         };canvas.addEventListener( 'keydown' , doKeyDown, true );canvas.focus();window.addEventListener( 'keydown' , doKeyDown, true );function doKeyDown( e) {var keyID = e.keyCode ? e.keyCode : e.which;if ( keyID === 37 )   { //left arrowbluePlane.move( context,- 5 , 0 )e.preventDefault();}if ( keyID === 38 )   { //up arrowbluePlane.move( context, 0 , - 5 )e.preventDefault();}if ( keyID === 39 )   { //right arrowbluePlane.move( context, 5 , 0 )e.preventDefault();}if ( keyID === 40 )   { //down arrowbluePlane.move( context, 0 , 5 )e.preventDefault();}if ( keyID === 13 )   { //enter arrowif (! bullet.isVisible()){var x = bluePlane.getX()+ bluePlane.getWidth()/ 2 - bullet.getWidth()/ 2 ;var y = bluePlane.getY() - bullet.getHeight();bullet.setX( x);bullet.setY( y);bullet.setVisible( true );}e.preventDefault();}bluePlane.draw( context);}function bulletMove(){if ( bullet.isVisible()){bullet.move( context, 0 ,- 5 );}bullet.draw( context);}function enemyPlaneMove(){if (! enemyPlane.isVisible()){var x = Math.floor( Math.random()* canvasWidth)+ 1 ;var y = - enemyPlane.getHeight();enemyPlane.setX( x);enemyPlane.setY( y);enemyPlane.setVisible( true );enemyPlane.draw( context);}if ( enemyPlane.isVisible()){enemyPlane.move( context, 0 , 3 );}enemyPlane.draw( context);}function collide(){if ( bullet.isVisible() && enemyPlane.isVisible()){if ( bullet.collideWith( enemyPlane)){bullet.setX(- 100 );bullet.setY(- 100 );bullet.setVisible( false );enemyPlane.setVisible( false );}}}function reDraw(){context.clearRect( 0 , 0 , canvasWidth, canvasHeight);bulletMove();enemyPlaneMove();bluePlane.draw( context);collide();}window.onload= function (){//Run reDraw() every 200 millisecondsvar time = setInterval( "reDraw()" , 200 );}</script> |

Thanks for learning, if you want to learn web coding, please study book[https://www.amazon.com/dp/B086T5H983](https://www.amazon.com/dp/B086T5H983)![](Image00105.jpg)[https://www.amazon.com/dp/B08D863KFY](https://www.amazon.com/dp/B08D863KFY)![](Image00106.jpg)If you enjoyed this book and found some benefit in reading this, I’d like to hear from you and hope that you could take some time to post a review on Amazon. Your feedback and support will help us to greatly improve in future and make this book even better.You can follow this link now.[http://www.amazon.com/review/create-review?&asin=B08HTF1J52](http://www.amazon.com/review/create-review?&asin=B08HTF1J52)Different country reviews only need to modify the amazon domain name in the link:www.amazon.co.ukwww.amazon.dewww.amazon.frwww.amazon.eswww.amazon.itwww.amazon.cawww.amazon.nlwww.amazon.inwww.amazon.co.jpwww.amazon.com.brwww.amazon.com.mxwww.amazon.com.auI wish you all the best in your future success!
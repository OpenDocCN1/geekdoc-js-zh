# 使用JavaScript框架和NoSQL的Web应用实用指南：程序员到程序员的集体智慧

## 前言

### 为什么写这本书？

在过去的几年里，我们接触了不同的客户端项目，这些项目传统上基于 J2ee 或其他开源技术（如 PHP、Ruby 等）构建。另一方面，2013 年见证了 Angular.js、Backbone.js 等 JavaScript 框架的日益流行，这些框架在客户端开发中获得了动力。这些强烈的变革之风带来了结构化的框架、编码以及开发与生产环境中的性能提升，变得绝对必要。此外，新兴的小型项目和初创公司对采用这些新技术表现出越来越大的兴趣。2013 年，存储非结构化数据的新兴趋势被统称为 NoSQL。很明显，这些新趋势伴随着围绕 JavaScript 和 NoSQL 相关存储库的新软件工具集而来。如今，JavaScript 不仅用于客户端验证。它还通过 Node.js 平台为 Web 应用提供服务器端开发。在本书中，我们尝试展示使用其中一些工具进行初创实验的实践。

### 目标是什么？




本书旨在展示上述部分工具在实际应用中的使用方法，以及如何利用这些工具开始开发应用程序。书中借助这些工具介绍了一些概念验证应用。此外，还简要描述了这些工具的一些重要方面。作为一名从职业生涯初期就开始从事开发的程序员，我一直试图寻找可以组合起来在工作中产生新概念的代码。本书正是我基于这种敏锐洞察力所付出的努力和实验性观点的集体成果。因此，新鲜知识将不断更新。我个人认为，使用像 Javascript 和 NoSql 相关产品这样的新技术很有趣，并且我完全享受这个阶段。另外，需要说明的是，我并非作者，而是一名职业程序员；所以我的本意并非用理论和解释来写作，而是更倾向于包含实际的工作示例。

### 本书适合谁？

具有 Web 编程背景并了解 Javascript 的人会发现本书很有用，因为本书汇集了基于 Javascript 的工具及其不同应用领域的使用知识。本书各章节通过工具的重要方面进行讲解，并涵盖了各种代码解释，而不仅仅是原始理论。值得一提的是，我尽量在需要时融入概念的解释。本书不适合初级程序员，而是适合具有中级知识的程序员，以及已经掌握了传统的 J2ee、PHP、Dot net 或其他开源 Web 技术（像我一样）的高级程序员。

## 使用 Javascript 启动 Web 服务器

我们发现像 `node.js` 平台这样的服务器端 Javascript 框架在开发中非常有用。我们在本书的章节中没有过多解释 `node.js`，但下面是对 `node.js` 的一点介绍，本书中的大多数概念验证都使用了它。

如今，开发人员都知道 `Node.js` 是一个服务器端 Javascript 执行平台。

根据 `nodejs.org` 的说法：

> “Node.js 是一个基于 Chrome V8 引擎构建的平台，用于轻松构建快速、可扩展的网络应用程序。Node.js 使用事件驱动、非阻塞 I/O 模型，使其轻量且高效，非常适合跨分布式设备运行的数据密集型实时应用程序。”

现在，`node.js` 开辟了一种执行或服务 Web 请求或任何其他类型服务器请求的新方式——称为非阻塞 I/O 操作。

我们遇到了以下链接 - http://code.danyork.com/2011/01/25/node-js-doctors-offices-and-fast-food-restaurants-understanding-event-driven-programming/，它以一种极好的方式展示了 `node.js` 的非阻塞概念，并与现实生活中的工作场景相关联。

由于我过去 5-6 年一直作为 J2ee 程序员，我了解并理解了 J2ee 环境中的 Servlet 编程模型，这是一种多线程编程模型，即当 Web 请求到达基于 Java 的 Web 服务器时，请求会命中 Servlet，Servlet 会打开一个新线程来处理请求并将数据响应回客户端。所有数据库相关方法或任何服务器资源密集型调用（本质上是共享的）都需要从 Servlet 中小心处理，以避免死锁或其他与共享对象相关的不必要情况。

尽管通过这种方式，进程被分割成线程，并在线程内服务 Web 请求，与服务器进程相比，线程的开销相对较小。但是，如果某个数据库调用在请求和响应的执行过程中（在线程调用内）花费了相当长的时间，那么它将因为同步活动而阻塞客户端，这就是阻塞 I/O 操作。

现在是时候理解非阻塞 I/O 了，`node.js` 平台正是基于此定义的。

首先，`node.js` 应用程序环境将在单线程编程模型上运行。

`node.js` 中的所有 Web 请求和服务器请求调用都是非阻塞 I/O。一个 Web 请求到达 `node.js` Web 服务器，Web 服务器接受该请求并将其交给一个监听器对象来处理响应。同时，该 Web 服务器将保持就绪状态以接受任何新的 Web 请求。而之前的响应处理将留在队列中，以执行其余操作。现在，`node.js` 环境负责准备 Web 响应，这又可能涉及从实际应用程序中调用数据库。此外，这个数据库查询也可以包含回调函数，当数据库响应准备就绪时进行处理。这些操作在队列中执行，也称为事件驱动编程，并且所有这些操作本质上是异步的。

所以这里要讨论的重点是，`node.js` 上下文中的所有函数调用都是非阻塞输入输出操作。在 `node.js` 环境中，执行操作由一个对象完成，而操作的结果由回调函数处理。

为了理解 `node.js`，我们推荐一本优秀的书籍 (http://www.nodebeginner.org/)。

在本书接下来的大部分应用程序中，我们都使用了基于 `node.js` 的 Web 服务器。

## Javascript 的面向对象方式——一些有趣的研究

随着我们走向前端 Web 应用程序开发中客户端 MVC 的世界，新的 Javascript 框架变得极其重要。我们在这里发布了 Javascript 中的面向对象编程和其他有趣的事实，并附有功能示例。以下是带注释的代码——

### 关于 Javascript 的一些有趣事实

#### Javascript 对象定义

```
1 var newObject = new Object();
2 var newObj = {};
```

#### 为对象定义属性

```
1 newObject.blogname = "PhloxBlog";
2 var blogname = newObject.blogname;
3 
4 console.log(blogname);
5 
6 newObj["blogtitle"] = "Technical Blogs";
7 var blogtitle = newObj["blogtitle"];
8 
9 console.log(blogtitle);
```

#### Javascript 中有趣的嵌套对象访问

以下类型的 Javascript 类使用字面量表示法定义。在一个类中，变量被定义为属性，函数被定义为该类的方法。

```
1 var nestedaddress = {
2 	State: "West Bengal",
3 	address: {
4 		streetname: "4C, Chidam Mudi Lane",
5 		city : "Kolkata",
6 		pincode: "700006"
7 	}
8 }
9 console.log(nestedaddress.address.city);
```

### 关于 Javascript 函数的有趣事实

#### 函数声明——

```
1 function averageout(x, y) {
2 	var avg = (x + y)/2;
3 	return avg;
4 }
5 
6 console.log(averageout()); 
7 console.log(averageout(2,3)); 
8 console.log(averageout(2,3,4)); 
```

在上面的例子中，第一次调用函数将返回 `NaN`。第二次调用时，函数将对两个参数起作用；最后一次调用时，多余的第三个参数将被忽略。

#### 现在……函数内部可以访问一个额外的变量——称为 arguments

```
1 function averageoutonarguments() {
2 	var sum = 0;
3 	for (var i = 0, j = arguments.length; i < j; i++) { 			
4                     sum += arguments[i]; 		
5             }
6 	return sum/arguments.length; 	
7    }
8 
9 console.log(averageoutonarguments(1, 2, 3, 4)); 
```

在 Javascript 中，所有参数都被称为 arguments。我们可以用任意数量的参数或不带参数调用函数，如上例所示。

#### Javascript 中的匿名函数

```
1 var simpleFunction = function() 	{ 	  
2  var aStringvalue = 'My Value in Moon'; 	  
3  function oneMoreString(val) { 			
4      return 'Altered Value is ' + ' ' +val; 		
5  } 		
6  console.log(oneMoreString(aStringvalue)); 	
7 }
8 
9 simpleFunction(); 
```



在上面的示例中，`simpleFunction` 使用匿名函数定义，并从该函数内部返回字符串。

### JavaScript 是一种基于原型的语言，不包含 class 语句

```
 1 function makeAddressWith(streetno, streetaddress, city, state, country, pincode) { 		
 2 	return { 			
 3 	       streetno: streetno ,
 4 	       streetaddress: streetaddress,
 5 	       city: city, 			
 6 	       state: state, 			
 7 	       country: country, 			
 8 	       pincode: pincode 		
 9 	} 	
10 } 	 	
11     
12 function fullAddress(address) { 		
13       return 'Full Address is -->>' + '\n' + address.streetno + ' ' + 
14               address.streetaddress + '\n' + address.city + ' ' + 
15               address.pincode + '\n' + address.state + ' ' + address.country;
16 }
17     
18 function addressWithCityAndPincode(address) {
19 	return 'City and Pincode is -->>' + '\n' + 
20 		address.city + ' ' + address.pincode ;
21 }
22     
23 address = makeAddressWith("4C", "Chidam Mudi Lane", "Kolkata", 
24 			  "West Bengal", "India", "700006");
25     
26 console.log(fullAddress(address));
27 console.log(addressWithCityAndPincode(address));
```

### 现在更简洁的类定义

```
 1 function makeAnotherAddressWith(streetno, streetaddress, city, 
 2 		state, country, pincode) {
 3 	return {
 4 		streetno: streetno ,
 5 		streetaddress: streetaddress, 
 6 		city: city,
 7 		state: state,
 8 		country: country,
 9 		pincode: pincode,
10 		fullAddress: function() {
11 		          return 'Full Address is (another function) -->>' + '\n' + 
12 				address.streetno + ' ' + address.streetaddress + '\n' + 
13                                 address.city + ' ' + address.pincode + 
14                                 '\n' + address.state + ' ' + address.country;
15 		},
16 		addressWithCityAndPincode: function() {
17 			return 'City and Pincode is (another function) -->>' + '\n' 
18 			+ address.city + ' ' +  address.pincode ;
19 		}
20 	}
21 }
22     
23 anotheraddress = makeAnotherAddressWith("4C", "Chidam Mudi Lane", "Kolkata", 
24                                                 "West Bengal", "India", "700006");
25 
26 console.log(anotheraddress.fullAddress());
27 console.log(anotheraddress.addressWithCityAndPincode());
```

### 接下来是原型的使用。SomeObject.prototype 将被 SomeObject 的所有实例使用。

在下面查找 `this` 和 `new` 的用法——

```
 1 function AddressWithPrototype(streetno, streetaddress, city, state, 
 2 		country, pincode) {
 3 		this.streetno = streetno;
 4 		this.streetaddress = streetaddress;
 5 		this.city = city;
 6 		this.state = state;
 7 		this.country = country;
 8 		this.pincode =  pincode;
 9 	}
10 
11 AddressWithPrototype.prototype.fullAddress = function() {
12 	return 'Full Address is (prototype) -->>' + '\n' + this.streetno + 
13 		' ' + this.streetaddress + '\n' 
14                     + this.city + ' ' + this.pincode + 
15                       '\n' + this.state + ' ' + this.country;
16 }
17 
18 AddressWithPrototype.prototype.addressWithCityAndPincode = function() {
19 	return 'City and Pincode is (prototype) -->>' + '\n' + this.city + 
20 		' ' + this.pincode ;
21 }
22 
23 address1 = new AddressWithPrototype("4C", "Chidam Mudi Lane", "Kolkata", 
24 					"West Bengal", "India", "700006");
25 console.log(address1.fullAddress());
26 address2 = new AddressWithPrototype("5C", "Chidam Mudi Lane", "Kolkata", 
27 					"West Bengal", "India", "700034");
28 console.log(address2.addressWithCityAndPincode());
```

### 在原型上添加额外的方法

```
1 AddressWithPrototype.prototype.addressWithStateAndCountry = function() {
2 	return 'State and Country is (prototype) -->>' 
3 		+ '\n' + this.state + ' ' + this.country ;
4 }
5 
6 address3 = new AddressWithPrototype("5C", "Chidam Mudi Lane", "Kolkata", 
7 					"East Bengal", "India", "700034");
8 console.log(address3.addressWithStateAndCountry());
```

### 内部函数

```
1 function anOuterFunction() {
2 	var a = 1;
3 	function innerFunction() {
4 		return a + 1;
5 	}
6 	return innerFunction();
7 }
8 console.log(anOuterFunction());
```

### JavaScript 闭包（巧妙且令人困惑……）

```
 1 function closureFunction(a) {
 2 	return function(b) {
 3 		return a + b;
 4 	}
 5 }
 6 x = closureFunction(5);
 7 y = closureFunction(20);
 8 
 9 console.log(x(6));
10 console.log(y(7));
```

输出将是 - `javascript 11 27`

### JavaScript 中的类

```
 1 function Blog() { }
 2 
 3 // The Object (Class Instances) in javascript
 4 
 5 function BlogAuthor() { }
 6 
 7 var firstPerson = new BlogAuthor();
 8 var secondPerson = new BlogAuthor();
 9 
10 // The Constructor in jaascript
11 
12 function BlogContent() {
13   console.log('BlogContent instantiated');
14 }
15 
16 var content1 = new BlogContent();
17 var content2 = new BlogContent();
18 
19 // The property (object attribute) in javascript
20 
21 function BlogModerator(name) {
22   this.name = name;
23   console.log('BlogModerator instantiated');
24 }
25 
26 var bm = new BlogModerator('My Name');
27 
28 // display the blog moderator name
29 console.log('Blog moderator is  ' + bm.name); 
30 
31 // The methods
32 
33 function BlogComment(username) {
34   this.username = username;
35   console.log('Blog Comment instantiated');
36 }
37 
38 BlogComment.prototype.comment = function()
39 {
40   console.log('This is a nice one by '+ this.username);
41 };
42 
43 var comment1 = new BlogComment('Bob');
44 var comment2 = new BlogComment('Michael');
45 
46 // call the BlogComment comment method.
47 
48 comment1.comment(); 
49 comment2.comment(); 
```

### JavaScript 中的继承

```
 1 // define the Post Class
 2 
 3 function Post() {}
 4 
 5 Post.prototype.createpost = function(){
 6   console.log('A post is created in draft mode');
7 };
 8 Post.prototype.save = function(){
 9   console.log('Post is saved');
10 };
11 
12 // define the Technical Post class
13 function TechnicalPost() {
14   // Call the parent constructor
15   Post.call(this);
16 }
17 
18 // inherit Post
19 TechnicalPost.prototype = new Post();
20 
21 // correct the constructor pointer because previously it points to Post
22 TechnicalPost.prototype.constructor = TechnicalPost;
23 
24 // replace the save method
25 TechnicalPost.prototype.save = function(){
26   console.log('Post is now TechnicalPost');
27 }
28 
29 // add publish method
30 TechnicalPost.prototype.publish = function(){
31   console.log('TechnicalPost is published');
32 }
33 
34 var post = new TechnicalPost();
35 post.createpost();
36 post.save();
37 post.publish();
38 
39 // check inheritance
40 console.log(post instanceof Post); // true
41 console.log(post instanceof TechnicalPost); // true
42 
43 // Using Object.create the inheritance line would instead be
44 
45 TechnicalPost.prototype = Object.create(Post.prototype);
```

### 封装

在上面的例子中，`TechnicalPost` 不需要知道 `Post` 类的 `createpost()` 方法的具体实现，但可以使用该方法；除非我们需要重写或使用它，否则 `TechnicalPost` 类不需要定义该方法。这就是封装，通过它每个类都继承其父类的方法，并且只需要定义它想要更改的内容。此外，子类还可以定义其他方法。

**参考资料：**

[面向对象 JavaScript 简介](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)

[JavaScript 再介绍（JS 教程）](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)

## 一个具有最小效果的简单 jQuery 图片滑块插件

我们尝试制作一个简单的 jQuery 图片滑块插件，以便更详细地理解 jQuery 动画和插件功能。该图片滑块插件具有从上下左右滑动整个内容的功能，这些功能可在 HTML 页面中进行配置。

这里我们详细介绍了该插件的代码。



我们已经参考了文章 [如何创建你自己的 jQuery 滑块插件](http://www.script-tutorials.com/how-to-create-your-own-jquery-slider-plugin/) 来制作这个插件。

因此，感谢 (script-tutorials.com) 提供了这个。下面是代码部分。

我们在 HTML 或 jQuery 代码的注释部分解释了代码。

### HTML 部分

```html
 1 <!DOCTYPE html>
 2 <html>
 3 <head>
 4     <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
 5     <link rel="stylesheet" href="main.css" type="text/css" />
 6     <script type="text/javascript" src="jquery.slider.js"></script> 
 7 	<!-- the plugin file -->
 8     <script>
 9         $(document).ready( function() {
10            $('#slider').plainSlider('down',3000); // Plugin method calling
11         });
12     </script>
13 </head>
14 <body>
15    <div class="example">
16       <div>
17           <ul id="slider">
18               <li><img src="Chrysanthemum.jpg" alt="" width="480" height="310"/>
19 		<p>这是第一张</p>
20 	      </li>
21               <li><img src="Desert.jpg" width="480" height="310" alt="" />
22                 <p>这是第二张</p>
23               </li>
24           </ul>
25      </div>
26    </div>
27 </body>
28 </html>
```

### jQuery 插件代码

```javascript
 1 (function($){
 2 $.fn.plainSlider = function(direction,timediff) { 
 3 	// Plugin Method and taking parameters
 4      var slides;
 5      var allcount;
 6      var i;
 7 
 8      function run() {
 9         if(direction==='up') //use of slideUp Method from parameter checking
10           {
11              $(slides[i]).slideUp(3000);
12              i++;
13              if (i >= allcount) i = 0;
14              $(slides[i]).show(3000);
15           }
16         else if(direction==='down') 
17           {
18              //use of slideDown Method from parameter checking
19              $(slides[i]).hide(3000);
20              i++;
21              if (i >= allcount) i = 0;
22              $(slides[i]).slideDown(3000);
23           }
24         else if(direction==='left')  
25           {
26 	     //use of left to right animate from parameter checking
27              $(slides[i]).show();
28              var position = $(slides[i]).position();
29              if(position.left===500)
30                {
31                  $(slides[i]).css({ left: 0});
32                };
33              $(slides[i]).animate({"left": "+=500px"}, 3000);
34              i++;
35              if (i >= allcount) i = 0;
36            }
37         else  //use of right to left animate from parameter checking
38           {
39              $(slides[i]).show();
40              var position = $(slides[i]).position();
41              if(position.left<0)
42                 {
43                   $(slides[i]).css({ left: 0});
44                 };
45              $(slides[i]).animate({"left": "-=500px"}, 3000);
46              i++;
47              if (i >= allcount) i = 0;
48            }
49            setTimeout(run, timediff); 
50 		//use of time parameter to run the method in Plugin
51          }
52 
53         slides = $(this).children();
54         allcount = slides.length;
55         i=0;
56 	//use of time parameter to run the method in Plugin
57         setTimeout(run, timediff); 
58      };
59 })(jQuery);
```

读者可以在此处查看代码 [这里](http://www.phloxblog.in/wp-content/uploads/2013/06/imagesliderplugin.zip)。

## 使用 d3.js 和 Prototype.js 的简单柱状图——基于 Javascript 类的方法

![AngularD3BarGraph](img/00003.jpeg)

我们正在努力将客户端的 JavaScript 代码转换为面向对象的方法。

因此，我们在前一章中学习了 JavaScript OOP 的过程。在这里，我们尝试将 `d3.js` 代码分离出来放入 JavaScript 框架中，为此我们采用了 `prototype.js` 来为 `d3.js` 代码分离创建 JavaScript 类。

那么，我们在 HTML 中到底做了什么？

### 1> 在 HTML 页面中添加了 `prototype.js`、`d3.js` 以及 d3 相关 JavaScript 类的引用

```html
1 <script type="text/javascript" src="js/prototype.js"></script>
2 <script src="js/barGraphProto.js"></script>
3 <script src="http://d3js.org/d3.v3.min.js"></script>
```

### 2> 放置了 `d3.js` 相关的类初始化代码——

```javascript
1 var   ourGraph = new BarGraph('sample.json','Year',905,'Frequency',6,'.0%'); 
2 //d3 related Variable initialisation
3 ourGraph.workOnElement('#d3bar'); // Work on particular element
4 ourGraph.generateGraph(); // generate the actual bar graph
```

### 3> d3 相关的柱状图代码——





```
 1 // properties are directly passed to `create` method
 2 var BarGraph = Class.create({ // prototype class creation
 3 initialize: function(datajson,xaxisName,xaxisPos,yaxisName,yaxisPos,d3Format) {
 4                 this.datajson = datajson;
 5                 this.xaxisName = xaxisName;
 6                 this.xaxisPos = xaxisPos;
 7                 this.yaxisName = yaxisName;
 8                 this.yaxisPos = yaxisPos;
 9                 this.d3Format = d3Format;
10                 // Taking all the variables and set in Class 
11 		//Instance Variables (d3 property specific)
12             },
13 workOnElement: function(element) {
14                 this.element = element;
15                 // Taking the DOM Element on which the graph will be drawn
16             },
17 generateGraph: function() {
18 
19                //d3 specific coding
20                var margin = {top: 20, right: 20, bottom: 30, left: 40},
21                    width = 960 - margin.left - margin.right,
22                    height = 500 - margin.top - margin.bottom;
23 
24               var formatPercent = d3.format(this.d3Format);
25 	      //setting the instance variable to d3 property
26 
27               var x = d3.scale.ordinal()
28                    .rangeRoundBands([0, width], .1);
29 
30               var y = d3.scale.linear()
31                       .range([height, 0]);
32 
33               var xAxis = d3.svg.axis()
34                       .scale(x)
35                       .orient("bottom");
36 
37               var yAxis = d3.svg.axis()
38                       .scale(y)
39                       .orient("left")
40                       .tickFormat(formatPercent);
41 
42               var svg = d3.select(this.element).append("svg")
43                       .attr("width", width + margin.left + margin.right)
44                       .attr("height", height + margin.top + margin.bottom)
45                       .append("g")
46                       .attr("transform", 
47                             "translate(" + margin.left + "," + margin.top + ")");
48 
49              d3.json(this.datajson, function(error, data) { 
50                       // getting the data
51                       if (error) return console.warn(error);
52 
53                       x.domain(data.map(function(d) { return d.letter; }));
54                       y.domain([0, d3.max(data, function(d) 
55                                          { return d.frequency; })]);
56 
57              svg.append("g")
58                      .attr("class", "x axis")
59                      .attr("transform", "translate(0," + height + ")")
60                      .call(xAxis)
61                      .append("text")
62                      .attr("x", this.xaxisPos)
63                      .attr("dx", ".71em")
64                      .style("text-anchor", "end")
65                      .text(this.xaxisName);
66 
67              svg.append("g")
68                      .attr("class", "y axis")
69                      .call(yAxis)
70                      .append("text")
71                      .attr("transform", "rotate(-90)")
72                      .attr("y", this.yaxisPos)
73                      .attr("dy", ".71em")
74                      .style("text-anchor", "end")
75                      .text(this.yaxisName);
76 
77              svg.selectAll(".bar")
78                      .data(data)
79                      .enter().append("rect")
80                      .attr("class", "bar")
81                      .attr("x", function(d) { return x(d.letter); })
82                      .attr("width", x.rangeBand())
83                      .attr("y", function(d) { return y(d.frequency); })
84                      .attr("height", function(d) { return height - y(d.frequency); });
85         }.bind(this)); // the bind syntax is important. 
86                        // Otherwise class instance variables will not be
87                        // accessible in inner function
88      }
89 });
```

[此处](http://www.phloxblog.in/wp-content/uploads/2013/07/simpleProto.zip)是供读者感兴趣的代码。我们将在 Angular.js 指令部分重用与 d3 相关的 JavaScript 类代码。

## Angular.js 应用程序开发中的概念

在本章中，我们将逐一讨论 Angular.js 应用程序开发中一些众所周知的概念。

### 1. ng-app

它是一个 Angular 指令，用于定义 HTML body 或 HTML body 的一部分作为 Angular.js 应用程序。

### 2. Angular 表达式

像`{{ some_angular_variable }}`这样的代码会计算变量值。这就是 Angular 表达式。

### 3. Angular 视图模板

Angular.js 视图模板是一个部分，它将被来自 Angular 模型的数据替换。

### 4. Angular 控制器

Angular 控制器是一种 JavaScript 函数形式，在其中，DOM 元素属性的变量值被绑定，并且与 DOM 元素属性绑定的变量的呈现逻辑在 JavaScript 函数（控制器）的控制下被控制和更改。因此，变量值的呈现逻辑应在 Angular 控制器中控制，这些变量通过`ng-model`指令或 Angular 表达式与 DOM 元素绑定，Angular 框架提供变量与 DOM 元素的自动绑定，即在指定位置，每当控制器中的变量值发生变化时，该变化将自动影响 DOM 元素。

### 5. Angular 作用域变量

在 Angular.js 应用程序中，JavaScript 变量值将在 Angular 作用域生命周期内存在。因此，所有变量都可以被观察其值的变化并对此采取行动——在 Angular.js 应用程序的各自作用域内。

### 6. Angular MVC

#### A. Angular 模型

模型是数据，可以通过 Angular 作用域的属性访问。

#### B. Angular 控制器

Angular 控制器是一种 JavaScript 函数形式，在其中，DOM 元素属性的变量值被绑定，并且与 DOM 元素属性绑定的变量的呈现逻辑在 JavaScript 函数（控制器）的控制下被控制和更改。

#### C. Angular 视图

在 Angular 框架中，视图由 HTML 元素和 Angular 表达式组成，这些元素和表达式在 Angular 控制器和 Angular 模型中处理后，在浏览器中渲染。

下面是一个 Angular 示例：

#### 一个 Angular 模型示例

```
 1 [
 2 	{
 3 	   "Product": "REL",
 4 	   "BBP": "10",
 5 	   "BSP": "10.2",
 6 	   "LTP": "10.1"
 7 	},
 8 	{
 9 	   "Product": "BEL",
10 	   "BBP": "20",
11 	   "BSP": "20.4",
12 	   "LTP": "20"
13 	},
14 	{
15 	   "Product": "MTL",
16 	   "BBP": "50",
17 	   "BSP": "50.5",
18 	   "LTP": "50.1"
19 	},
20 	{
21 	   "Product": "BSL",
22 	   "BBP": "100",
23 	   "BSP": "101",
24 	   "LTP": "100.2"
25 	}
26 ]
```

#### HTML 中的 Angular 代码片段

```
 1 ...
 2 <html lang="en" ng-app="stocksample"> 
 3 <!--Angular Directive for Angular Application Definition -->
 4 ...
 5 <body ng-controller="StockListCtrl">  
 6 <!--Angular Controller to control Angular Model Data for View in HTML Body-->
 7 ....
 8 <table>
 9 <tbody>
10      <tr ng-repeat="stock in stocks"> <!-- The Angular Scope Variable for the Model -->
11          <td>{{stock.Product}}</td>   <!-- Angular Expressions -->
12          <td>{{stock.BBP}}</td>
13          <td>{{stock.BSP}}</td>
14          <td>{{stock.LTP}}</td>
15      </tr>
16 </tbody>
17 </table>
18 </body>
```

#### Angular 控制器

```
1 function StockListCtrl($scope, $http) {// Dependency Injection for Angular Service
2 	$http.get('stocks.json').success(function(data) { // Angular $http Service
3 	 $scope.stocks = data;
4 	});
5 }
```

在接下来的章节中，我们将讨论 Angular 服务以及 Angular 应用程序中的依赖注入。

**参考文献：**





[Angular.js 文档](http://docs.angularjs.org/tutorial)

## Angular.js 服务与依赖注入

在本章中，我们将尝试通过一些代码示例来解释 Angular.js 的服务定义。

首先是在 Angular Factory 中声明服务并在 Angular Controller 中访问它的示例——

### 以下是 Controller

```
1 app.controller('StockListCtrl', function($scope,stockService) { 
2     // 将 Angular 放入服务中
3     stockService.getStocks(function(data){                      
4         // 访问控制器方法
5         console.log(data);
6         $scope.stocks = data;
7     });
8 });
```

### 以下是上述在 Angular Factory 中的 stockService

```
 1 app.factory('stockService', function($http) {
 2     // 服务声明并引入内置的 $http 服务
 3     return {
 4         getStocks: function(callback) {      
 5             // 将方法作为服务的公共方法返回
 6             $http.get('stocks.json').success(function(data) { 
 7                  // 访问外部资源
 8                  callback(data);             
 9                  // 使用数据调用回调函数，
10                  // 以便在方法访问级别进行操作
11             });
12         }
13     }
14 });
```

第二个是 Service Provider 的示例——

```
 1 app.config(function($provide) {                    
 2 	// Angular 应用配置部分
 3   $provide.provider('stockService', function() {   
 4 	// 使用内置的 provide 服务创建服务提供者
 5     this.$get = function($http) {                  
 6         // 获取服务的约定——$get
 7         // ——服务将通过此调用被实例化
 8       return {
 9 	  getStocks: function(callback) {          
10                 // 将方法作为服务的公共方法返回                    \
11    
12 		$http.get('stocks.json').success(function(data) { 
13                         // 访问外部资源
14 			callback(data);      
15                         // 使用数据调用回调函数，
16                         // 以便在方法访问级别进行操作     
17 		});   
18 	     }
19 	 }
20       };
21   });
22 });
```

对于上述服务，我们可以重用之前指定的同一个控制器。

### 现在介绍一些从 Angular 依赖注入服务中获取服务的方法——

Angular 注入器（`$injector`）负责创建自定义 Angular 服务的实例。当 Angular 应用被创建时，注入器会在 Angular 环境中被实例化。

### 在 Angular.js 中使用依赖注入的第一种方式

```
 1 app.controller('StockListCtrl', function($scope,$injector ) {
 2 	var stkService = $injector.get('stockService'); 
 3         // 从 Angular 的 $injector 对象中获取服务，该对象
 4         // 负责将服务从 Angular 应用配置推送到
 5         // 其他函数或控制器中
 6 	stkService.getStocks(function(data){
 7 	   console.log(data);
 8            $scope.stocks = data;
 9         });
10    });
```

### 在 Angular.js 中使用依赖注入的另一种方式——推荐方式，如 Angular 文档所述

```
1 app.controller('StockListCtrl',
2     ['$scope', 'stockService', function($scope,stockService ) {  
3         // 引入依赖
4 	stockService.getStocks(function(data){                   
5         // stockService 在此处被注入到控制器中
6 	  console.log(data);
7           $scope.stocks = data;
8         });
9   }]);
```

读者可以通过以下参考资料深入了解 Angular.js 服务——

[`github.com/angular/angular.js/wiki/Understanding-Dependency-Injection`](https://github.com/angular/angular.js/wiki/Understanding-Dependency-Injection)

[`stackoverflow.com/questions/13937318/convert-angular-http-get-function-to-a-service`](http://stackoverflow.com/questions/13937318/convert-angular-http-get-function-to-a-service)

## Angular.js $watch 与 $observe——简要介绍

### Angular.js $watch——

Angular.js 的 `$watch` 事件在检测到 DOM 属性变量值发生变化时触发。对于 `$watch` 表达式，每当检测到上下文中的当前值与之前的值不同时，监听器就会触发。为了理解 `$watch` 表达式，我们提供了一个简单的可运行示例。我们创建了一个输入文本框，它通过 `ng-model` 绑定到 `watchtext`。我们可以更改文本框的值，并在 HTML 页面中看到之前的值和当前的值。

#### HTML 代码如下——

```
 1 <form name="myForm" ng-controller="Ctrl">
 2  A word: <input type="text" name="input" ng-model="watchtext" />
 3  <br/>
 4  Word changed {{counter}} times.
 5  <br/>
 6  Last value of counter was {{lastvalue}}
 7  <br/>
 8  Current value of counter is {{currentvalue}}
 9  <br/>
10 
11   <button ng-click="initCounter()" >
12        Counter = 0
13   </button>
14 </form>
```

这里我们有一个 Angular.js 控制器——`"ctrl"`。其他代码在 JavaScript 代码中已有注释。

#### Angular.js 代码如下——

```
 1 function Ctrl($scope) {
 2 	var scope = $scope;
 3 	scope.watchtext = 'First Value'; // 在此处初始化 watchtext
 4 	scope.counter = 0;
 5 	scope.lastvalue = '';
 6 	scope.currentvalue = '';
 7 
 8 	$scope.initCounter = function() {
 9 		scope.counter = 0; // 在此处初始化 counter 变量
10 	}
11 
12 	scope.$watch('watchtext', function(newValue, oldValue) { 
13 		scope.counter = scope.counter + 1; 
14 		scope.lastvalue = oldValue;
15 		scope.currentvalue = newValue;
16 	});
17 	// lastvalue 和 currentvalue 通过 Angular 表达式在 HTML 页面中更新。
18 	// 这些值在 watch 函数中被更新。
19 }
```

### Angular $observe——

在 Angular 指令的链接阶段，`$observe` 函数是获取所有属性值以进一步执行指令代码的位置。HTML 代码如下——

```
1 <div id="bar" sample-directive time-interval=1000 datajson="sample.json"> 
2 <!-- 设置属性值 -->
3  scope.firstvalue is {{firstvalue}}<br/>
4  scope.secondvalue is {{secondvalue}}<br/>
5 </div>
```

下面是一个属性指令——`"AngularExample"`，仅用于示例说明。代码中已有注释。Angular.js 代码如下——

```
 1 angular.module('AngularExample', [])
 2 .directive('sampleDirective', function ($timeout) {// Angular 指令
 3   return {
 4         restrict: 'A', // 仅属性指令
 5     scope: {
 6             timeInterval: '@', // 使用 @ 获取变量值，
 7                                // 这些值在链接函数中不能立即使用
 8 	datajson: '@'      // 同上
 9         },
10         link: function (scope, elem, attrs) {
11 	console.log(scope.timeInterval);
12 	attrs.$observe('timeInterval', function(value) { 
13 		// 仅在 observe 函数中从 HTML DOM 获取属性值
14 		console.log('timeInterval has changed value to ' + value);
15 		scope.firstvalue = value;
16 	  });
17 	attrs.$observe('datajson', function(value) {
18 		console.log('datajson has changed value to ' + value);
19 		scope.secondvalue = value;
20 	  });
21 	console.log(scope.firstvalue);
22 
23 	var t = $timeout( function() { 
24                 // 使用 timeout 函数——展示一段时间后属性变量的变化。
25                 // 这是通过跟踪 Angular 变量来改变 HTML DOM 展示的位置。
26 
27 	    scope.firstvalue = 'new--' + ' and old--1' ;
28 	    scope.secondvalue = 'new--' + ' and old--2' ;
29 
30 	}, 2000);
31         }
32     }
33 });
```

读者可以在此处查看完整的 plunker——

[`plnkr.co/VTVep9yW5hr8HKK2KtDX`](http://plnkr.co/VTVep9yW5hr8HKK2KtDX)





## Angular.js Promise 与 Deferred API - 实现详解

### Angular.js Promise -

Angular.js 中的 Promise 充当一个占位符，JavaScript 对象通过它异步返回某些结果数据，且不保证固定的响应时间。Angular.js 中 Deferred 和 Promise API 的组合，确保了在客户端代码中通过异步系统处理成功和拒绝回调。

### Angular.js Deferred API -

Deferred 对象通过 `$q.defer()` 构建。该 API 用于通知异步工作的成功或失败完成，这些工作位于 Deferred API 的上下文中。`deferred 对象` 通过 `.resolve(arg)` 和 `.reject(arg)` 方法处理成功和拒绝情况。

### Angular.js Promise API -

`deferred.promise` 在 Angular.js 中返回一个 Promise 实例。在 Deferred 对象中完成任务后，我们可以访问 Promise 对象中的结果。`promise.then(success, error)` – 这一部分始终向 UI 返回一个确定的结果（成功或错误），位于成功或错误回调中。其中一个方法（resolve 或 reject）会携带结果或拒绝原因被调用。

### Angular.js Promise 链 -

由于 `promise.then` 中派生的对象本身也是一个 Promise 对象，因此我们可以在此建立 Promise 链。为了实现 Promise 功能，Angular.js 中提供了 `$q service` 功能。这里的 `$q` 与 Angular 作用域模型集成，并被 Angular 模板引擎识别。下面是展示 `Promise` 功能的带注释代码库：

```
 1     'use strict';
 2     
 3     var app = angular.module('angularjs-promise', []); // 创建应用
 4     
 5     app.controller('PhoneListCtrl', function($scope, phoneService) { 
 6 		// Angular 控制器定义，注入服务
 7             phoneService.getPhones().then(function(data) {// Angular promise
 8                 $scope.phones = data;
 9             });
10        });
11     
12     app.factory('phoneService', function($http, $q) {
13 		// Angular 服务声明
14         return {
15             getPhones: function() {                                 
16                 var deferred = $q.defer(); // Deferred 对象声明
17                 $http.get('phones.json').success(function(data) {   
18 				// 异步服务调用
19                      deferred.resolve(data);
20                 }).error(function(){
21                      deferred.reject();
22                 });
23             return deferred.promise;
24          }
25        }
26     });
```

为了理解完整功能，我们制作了一个 plunker，链接如下：

[`plnkr.co/hBbq6qiCXZXttkFEnZWj`](http://plnkr.co/hBbq6qiCXZXttkFEnZWj)

参考资料：

[Angular.js 文档](http://docs.angularjs.org/api/ng.$q)

## JavaScript 测试框架 - Jasmine - 快速学习

如今，各种基于 JavaScript 的应用越来越流行。因此，在开发工作的各个方面，自动化测试 JavaScript 代码的需求日益明显。以下是对

### JavaScript 测试框架 - Jasmine

的简要学习

#### 安装与运行部分 -

从[此处](https://github.com/pivotal/jasmine/downloads)安装 Jasmine 独立版框架。解压文件夹。将测试规范代码放入 Jasmine 独立版文件夹中 spec 文件夹内的 `<<你的功能规范>>.js` 文件中。将 JavaScript 代码放入 Jasmine 独立版文件夹中 src 文件夹内的 `<<你的功能>>.js` 文件中。

现在，在 `Jasmine 安装文件夹` 中的 `SpecRunner.html` 文件的 `在此处包含源文件` 部分，添加源 JavaScript 文件的 script 标签。在 `Jasmine 安装文件夹` 中的 `SpecRunner.html` 文件的 `在此处包含规范文件` 部分，添加规范 JavaScript 文件的 script 标签。现在，如果我们运行 `SpecRunner.html`，示例规范应该通过，并且消息会显示在 `SpecRunner.html` 文件中。安装部分到此结束。

#### Jasmine 中需要理解的一些要点 -

1. Jasmine 是一个适合行为驱动开发的 JavaScript 测试框架。
2. `describe` 是 Jasmine 测试套件中的一个关键字。
3. Jasmine 测试框架中的测试由 `describe` 块内的 `it` 定义。
4. 这些是 Jasmine 框架下的独立测试单元。
5. 在 `describe` 和 `it` 块中，可以运行任何可执行的 JavaScript 函数。
6. 在 `describe` 函数中声明的任何变量，在该 `describe` 函数块内的所有 `it` 函数中均可使用。
7. 期望（Expectations）是期望实际值与函数返回的值进行比较的函数。
8. 匹配器（Matchers）对实际值和期望值进行布尔比较。它向 Jasmine 报告期望为真或假。

### 以下是一些用于测试的代码，并在注释中进行了说明 -

我们的 JavaScript 源文件代码 -

（基于原型的 JavaScript 类的最小代码） -

如果读者不熟悉 JavaScript 类，可以阅读《面向对象方式下的 JavaScript – 第一章中的一些有趣研究》。

```
 1     // 简单的 JavaScript 函数
 2  
 3     function helloWorld() {
 4         return "Hello world!";
 5     }
 6     
 7     function checkArraylength() {
 8     	var arr = new Array();
 9     	arr[0] = 12;
10     	return arr.length;
11     }
12     
13     // 基于原型的 JavaScript 类
14 
15     function AddressWithPrototype(streetno, streetaddress, 
16                                   city, state, country, pincode) {
17     			this.streetno = streetno;
18     			this.streetaddress = streetaddress;
19     			this.city = city;
20     			this.state = state;
21     			this.country = country;
22     			this.pincode =  pincode;
23     		}
24     
25     AddressWithPrototype.prototype.fullAddress = function() {
26     	return '完整地址是（原型）-->>' + '\n' + this.streetno + 
27 			' ' + this.streetaddress + '\n'
28                          + this.city + ' ' + this.pincode + '\n' + 
29 			 this.state + ' ' + this.country;
30     }
31     
32     AddressWithPrototype.prototype.changeAddressForCity = function() {
33         this.city = 'Delhi';
34     	return '完整地址是（原型）-->>' + '\n' + this.streetno 
35 			 + ' ' + this.streetaddress + '\n'
36                          + this.city + ' ' + this.pincode + '\n' 
37 		         + this.state + ' ' + this.country;
38     }
```

### 我们的测试规范代码如下 -





```
 1     describe("Hello world", function() {  // Jasmine 测试套件
 2         it("says hello", function() {     
 3 		// 单个测试组件 - 引用我们的源 JavaScript 文件代码
 4             expect(helloWorld()).toEqual("Hello world!");  
 5 		// 与函数输出进行相等性检查
 6         }); 
 7     
 8         it("says world1", function() {
 9             expect(helloWorld()).toContain("world");      
10 		// 检查函数输出中是否包含特定值
11         });
12     
13         // 添加自定义匹配器
14         beforeEach(function() {
15             this.addMatchers({
16                 toContainElementMoreThanZero: function() {  
17 			// 创建自定义匹配器
18                     return (this.actual > 0);
19                 }
20             });
21         });
22      
23         it('contains more than one array element', function() {
24             expect(checkArraylength()).toContainElementMoreThanZero(); 
25 		// 应用自定义匹配器
26         });
27         
28         var newAddress;
29         
30         beforeEach(function() {
31     		newAddress = new AddressWithPrototype("4C", "Chidam Mudi Lane", 
32                     "Kolkata", "West Bengal", "India", "700006");  
33 			// 引用源 JavaScript 类
34         });
35         
36         it("calls the fullAddress() function", function() {
37             spyOn(newAddress, "fullAddress");  
38 		// 将检查类的 fullAddress 方法是否被调用
39             newAddress.fullAddress();
40             expect(newAddress.fullAddress).toHaveBeenCalled(); 
41 		// 确保方法被调用
42         });
43         
44         it("calls with 'Delhi' as argument", function() {
45             spyOn(newAddress, "changeAddressForCity");
46             newAddress.changeAddressForCity("Delhi");
47     	    expect(newAddress.changeAddressForCity).toHaveBeenCalledWith("Delhi"); 
48 		// 以 'Delhi' 作为参数调用
49         });
50         
51         it("not called with 'Kolkata' as argument", function() {
52             spyOn(newAddress, "changeAddressForCity");
53             newAddress.changeAddressForCity("Delhi");
54     	expect(newAddress.changeAddressForCity).not.toHaveBeenCalledWith("Kolkata"); 
55         })
56         
57         it("return delhi as city", function() {
58             newAddress.changeAddressForCity();
59             expect(newAddress.fullAddress()).toContain("Delhi");
60         });
61     });
```

### 异步功能测试

```
 1     describe("async tests", function(){
 2      var flag, value;
 3      it("should simulate an asynchronous call", function () { 
 4       runs(function() { 
 5         flag  = false; 
 6         value = 0; 
 7     
 8         setTimeout(function() { // 该函数将在 500 毫秒后被调用
 9 			        
10           value++; 
11           flag = true; 
12         }, 500); 
13       });  
14     
15       waitsFor(function() {     
16 		// 等待直到函数调用返回值
17         return flag; 
18       }, "The Value should be incremented", 5000);  
19 	// 如果等待 5 秒后仍未得到结果，则退出框架方法
20          
21       runs(function() {  
22         expect(flag).toEqual(true);   
23         expect(value).toEqual(1); 
24       }); 
25      }); 
26     });
```

与 Jasmine 相关的其他要点如下——

我们可以在 Jasmine 测试中使用的一些关键特性

#### 场景 1 -

```
1 var a; 
2 a = true; 
3 expect(a).toBe(true); <-- 这里 .toBe 是测试的关键字
4 expect(false).not.toBe(true); <-- 使用 not 关键字的另一种测试变体
```

#### 场景 2 - 正则表达式的匹配器

```
1 var message = 'It is an address'; 
2 expect(message).toMatch('address'); <-- 这里 .toMatch 是测试的关键字
3 expect(message).toMatch(/address/); 
```

#### 场景 3 - 与 'undefined' 比较的匹配器

```
1 var person = 'Piyas De'; 
2 expect(person).toBeDefined(); <-- 这里 .toBeDefined 是测试的关键字 
3 expect(aotherperson).not.toBeDefined(); 
4 
5 或者 
6 
7 expect(aotherperson).toBeUndefined(); <-- 这里 .toBeUndefined 是测试的关键字
```

#### 场景 4 - 小于检查

```
1 var amount = 10; 
2 var anotheramount = 12; 
3 expect(anotheramount).not.toBeLessThan(amount); <-- 这里 .toBeLessThan 是测试的关键字 
4 						    
```

#### 场景 5 - 抛出检查

```
 1 function checkThrow() 
 2 { 
 3 	return aVariable; 
 4 } 
 5 
 6 expect(checkThrow()).toThrow(); <-- 这里 .toThrow 是测试的关键字
 7 
 8 function checkNotThrow() 
 9 { 
10 	return 1; 
11 } 
12 
13 expect(checkNotThrow()).not.toThrow(); 
```

有关 Jasmine 中测试函数的所有详细信息，请参阅——

#### 参考资料——

[Jasmine 文档](http://pivotal.github.io/jasmine/)

## 使用 Jasmine 进行 Angular.js 测试

在本章中，我们将尝试讨论使用 Jasmine 测试框架进行 Angular.js 客户端测试。我们已经介绍了使用 Jasmine 框架对客户端控制器和 Angular Mock 服务的测试。代码中已添加注释以帮助理解测试。

我们的两个示例控制器是——

### controllers.js

```
 1     // 该控制器在 $scope 变量中返回三个 JSON 元素
 2     function PhoneListCtrl($scope) {
 3       $scope.phones = [
 4         {"name": "Nexus S",
 5          "snippet": "Fast just got faster with Nexus S."},
 6         {"name": "Motorola XOOM™ with Wi-Fi",
 7          "snippet": "The Next, Next Generation tablet."},
 8         {"name": "MOTOROLA XOOM™",
 9          "snippet": "The Next, Next Generation tablet."}
10       ];
11     }
```

以及

### RTcontroller.js

在该控制器中，我们创建了一个服务，通过 `$http` 和 `$q` 对象将数据返回到 Angular `$scope` 的 "stocks" 变量中。

```
 1     var app = angular.module('angularjstest', []); 
 2     
 3     app.controller('StockListCtrl', function($scope, stockService) { 
 4 		// Angular 控制器定义
 5                 // 带有服务注入
 6             stockService.getStocks().then(function(data) {           
 7 		// Angular promise
 8                 $scope.stocks = data;
 9             });
10        });
11     
12     app.factory('stockService', function($http, $q) {               
13 		// Angular 服务声明
14         return {
15             getStocks: function() {                                 
16                 var deferred = $q.defer();                          
17 			// 延迟对象声明
18                 $http.get('stocks.json').success(function(data) {   
19 			// 异步服务调用
20                      deferred.resolve(data);
21                 }).error(function(){
22                      deferred.reject();
23                 });
24             return deferred.promise;
25          }
26        }
27     });
```

以下代码是用于测试的规范文件，可以通过 `testrunner.html` 运行，该文件是 Jasmine 框架中的默认测试文件。我们仅针对示例工作修改了此文件。源文件需要包含在 `testrunner.html` 的 `<!-- include source files here...-->` 部分中

`<script type="text/javascript" src="src/controllers.js"></script>`

`<script type="text/javascript" src="src/RTcontroller.js"></script>`

同时，规范文件需要包含在 `testrunner.html` 的 `<!-- include spec files here...-->` 部分中 `<script type="text/javascript" src="spec/ControllerSpec.js"></script>`

现在来看规范文件——

### Angular.js 测试规范编码——

```
 1     // 该控制器在 $scope 变量中返回三个 JSON 元素
 2     function PhoneListCtrl($scope) {
 3       $scope.phones = [
 4         {"name": "Nexus S",
 5          "snippet": "Fast just got faster with Nexus S."},
 6         {"name": "Motorola XOOM™ with Wi-Fi",
 7          "snippet": "The Next, Next Generation tablet."},
 8         {"name": "MOTOROLA XOOM™",
 9          "snippet": "The Next, Next Generation tablet."}
10       ];
11     }
```





```javascript
 1     describe('Controller function', function() {  // Jasmine 测试套件
 2     
 3       describe('PhoneListCtrl', function() {      
 4 		// Angular 控制器的内部测试套件
 5         var scope;
 6     
 7         beforeEach(inject(function($rootScope, $controller) {  
 8 			// 无头浏览器情况下的数据初始化
 9                         // $rootScope 是 Angular 内置对象，用于创建 Angular 作用域
10 	                // angular 作用域将由此创建
11 	  scope = $rootScope.$new();
12           var ctrl = $controller(PhoneListCtrl, {$scope: scope}); 
13 			// 将在测试环境中为 PhoneListCtrl 控制器创建控制器对象
14                         // 在测试环境中为 PhoneListCtrl 控制器创建控制器对象
15         }));
16     
17         it('should create "phones" model with 3 phones', function() { 
18           expect(scope.phones.length).toBe(3); 
19 		// 单个测试组件 - 参考上述 Angular 控制器的源代码
20 		// 参考上述 Angular 控制器的源代码
21         });                                    
22       });
23     
24       describe('StockListCtrl', function() {
25          var scope;
26          var $httpBackend, $rootScope, createController, _stockService;
27     
28     	 beforeEach(function () {
29                 module("angularjstest");   // Angular 模块初始化
30             }); 
31     
32         beforeEach(inject(function($rootScope, $controller, 
33 					$injector ,stockService) {
34     
35     	  $httpBackend = $injector.get('$httpBackend'); 
36 		// 用于测试环境的模拟对象，配合 $http 服务
37     	  $httpBackend.when('GET', 'stocks.json')
38 			.respond([{"Product": "REL", "BBP": "10", 
39                                    "BSP": "10.2", "LTP": "10.1"}]); 
40                         // 通过创建 $httpbackend 服务发送模拟数据
41     	  $rootScope = $injector.get('$rootScope');
42     	  scope = $rootScope.$new();
43     	  var $controller = $injector.get('$controller'); 
44 		// 为测试环境创建 Angular 控制器
45     	  _stockService = stockService;
46     	  spyOn(stockService, 'getStocks').andCallThrough(); 
47 			// 通过 spyOn 确保调用了 'getStocks' 方法
48     	  createController = function() { // 创建控制器的方法
49                   return $controller('StockListCtrl', 
50 			{'$scope' : scope }, {stockService : _stockService});
51               }; 
52     
53         }));
54     
55         it('should call getStocks', function() {
56     	  var controller = createController();
57     	  expect(_stockService.getStocks).toHaveBeenCalled(); 
58 				// 服务方法是否被调用
59     	  $httpBackend.flush();
60         });
61         it('should have more than 0 stock', function() {
62     	  var controller = createController();
63     	  $httpBackend.flush();
64               expect(scope.stocks.length).not.toBe(0); 
65 		// 期望从此处返回一些股票数据 -
66                 // 我们已在上方创建了模拟服务
67     
68         });
69       });
70     });
```

因此，在本章中，我们介绍了在有无 Angular 服务的情况下测试 Angular 控制器的方法。

## Angular.js 指令下的 jQuery 插件——一种更简洁的 HTML 方法

![angular-jquery-image-slider](img/00004.jpeg)

angular-jquery-image-slider

在上一章中，我们介绍了如何从头构建一个 jQuery 插件。这里我们将介绍一种简洁的方法，通过 Angular.js 指令生成干净的 HTML，该指令将封装上述 jQuery 插件的功能。该插件已可配置图片移动方向——左、右、上、下。

### 那么什么是 Angular.js 指令？

### 直接来自 angularjs.org——

> 指令是一种教 HTML 新技巧的方式。在 DOM 编译期间，指令会与 HTML 进行匹配并执行。这使得指令能够注册行为或转换 DOM。

简单来说，我们理解到：在 Angular.js 框架下，我们可以在网页中引入绑定我们规则的新 HTML 标签。同时，我们始终可以分离并最小化 HTML 页面中 JavaScript 代码的使用。从本次练习中我们学到的另一件事是，我们可以在 Angular.js 框架封装内，以最小的调整使用现有的复杂 jQuery 插件。现在让我们来看代码。与之前的文章一样，我们将在 HTML 和 JavaScript 代码中添加注释。

### 主要 HTML 代码片段

```html
 1     <div class="example" >
 2         <div image-slider slider-id ="'slider'" time-interval="3000" 
 3 							my-direction="'down'" >
 4         <!-- imageSlider 是我们的 Angular 指令名称 -->
 5         <!-- sliderId, timeInterval, myDirection 是三个变量 -->
 6         <!-- 用于插件运行的 UL 元素的 id -->
 7         <!-- timeInterval 是插件运行的时间间隔，myDirection 是图片滑动的方向 -->
 8             <ul id="slider">
 9                 <li><img src="Chrysanthemum.jpg" alt="" width="480" height="310"/>
10 							<p>这是第一张幻灯片</p></li>
11                 <li><img src="Desert.jpg" width="480" height="310" 
12 						alt="" /><p>这是第二张幻灯片</p></li>
13             </ul>
14         </div>
15     </div>
```

### Angular 方式的代码

```javascript
 1 angular.module('AngularSlider', [])
 2 .directive('imageSlider', function () { // Angular 指令声明
 3      return {
 4          restrict: 'A',                 // 该指令为属性类型
 5          scope: {
 6              timeInterval: '=',         // 三个初始化变量
 7              myDirection: '=',
 8              sliderId: '='
 9          },
10          link: function (scope, elem, attrs) {
11              $('#'+scope.sliderId).plainSlider(scope.myDirection,
12 							scope.timeInterval);
13              // 在 link 函数中调用 jQuery 插件方法
14 	     // 针对特定的 DOM 元素
15          }
16      }
17 });
```

此处使用的特定 jQuery 插件相关信息可在《"Simple jQuery Image Slider Plugin with minimal effects"》章节中找到。我们的代码可在 [Github](https://github.com/piyasde/angulardicective) 中找到。

### 参考资料：

1> [`docs.angularjs.org/guide/directive`](http://docs.angularjs.org/guide/directive)

2> [`www.befundoo.com/university/tutorials/angularjs-directives-tutorial/`](http://www.befundoo.com/university/tutorials/angularjs-directives-tutorial/).

## Angular.js 指令中的 D3.js——摆脱 HTML 页面中的 D3 svg 代码

我们在项目中曾使用 **D3.js** 代码生成图表。就我个人而言，这段代码对于初学者来说有些复杂。最近我正在学习 **Angular.js** 和 **Angular 指令**。因此我想到引入一个 Angular 指令来封装 D3.js 的复杂功能。于是就有了本章的结果——**借助 D3.js 通过 Angular 指令创建柱状图**。

我从 [`bl.ocks.org/mbostock/3885304`](http://bl.ocks.org/mbostock/3885304) 学习了 D3.js 代码。上一章也是我们关于创建 Angular 指令的文档。

### 首先——柱状图图片——

![AngularD3BarGraph](img/00003.jpeg)

AngularD3BarGraph

### 现在是在 HTML 中的带注释代码片段——

```html
 1 <body>
 2 	<div id="d3bar" angulard3-bar-graph datajson="'sample.json'" 
 3 	       xaxis-name = "'Year'" 
 4 	       xaxis-pos = "905"  
 5 	       yaxis-name = "'Frequency'" 
 6 	       yaxis-pos = "6" 
 7 	       d3-format= "'.0%'" >
 8 	<!-- angular 指令是 angulard3-bar-graph -->
 9 	<!-- 指令变量为 xaxis-name, yaxis-name, xaxis-pos, yaxis-pos -->
10 	<!-- y 轴数据格式 (d3-format) -->
11 	<!-- 以及 datajson 变量，它保存外部数据源 -->
12 	</div>
13 </body>
```

下面是

### 封装了柱状图 D3.js 代码的 Angular 指令





```
 1     angular.module('AngularD3BarGraph', []) // Angular Module Name
 2         .directive('angulard3BarGraph', function () { 
 3 		// Angular Directive
 4             return {
 5                 restrict: 'A', // Directive Scope is Attribute
 6                 scope: {
 7                     datajson: '=',
 8                     xaxisName: '=',
 9                     xaxisPos: '=',
10                     yaxisName: '=',
11                     yaxisPos: '=',
12                     d3Format: '='
13                     // All the Angular Directive Vaiables used as d3.js parameters
14                 },
15                 link: function (scope, elem, attrs) {
16                     // The d3.js code for generation of bar graph. 
17 		    // further reading should be done from 
18 		    //	http://d3js.org/
19                     var margin = {top: 20, right: 20, bottom: 30, left: 40},
20                         width = 960 - margin.left - margin.right,
21                         height = 500 - margin.top - margin.bottom;
22     
23                     var formatPercent = d3.format(scope.d3Format); 
24 				// formatting via angular variable
25     
26                     var x = d3.scale.ordinal()
27                            .rangeRoundBands([0, width], .1);
28     
29                    var y = d3.scale.linear()
30                            .range([height, 0]);
31     
32                    var xAxis = d3.svg.axis()
33                            .scale(x)
34                            .orient("bottom");
35     
36                    var yAxis = d3.svg.axis()
37                            .scale(y)
38                            .orient("left")
39                            .tickFormat(formatPercent);
40     
41                    var svg = d3.select("#"+elem[0].id).append("svg") 
42 			// selecting the DOM element by d3.js
43                         // - getting from Angular context  
44                        .attr("width", width + margin.left + margin.right)
45                        .attr("height", height + margin.top + margin.bottom)
46                        .append("g")
47                            .attr("transform", 
48 				"translate(" + margin.left + "," + margin.top + ")");
49     
50                   d3.json(scope.datajson, function(error, data) { 
51 			// external data filename- angular directive variable
52                       if (error) return console.warn(error);
53     
54                       x.domain(data.map(function(d) { return d.letter; }));
55                       y.domain([0, d3.max(data, function(d) 
56 					{ return d.frequency; })]);
57     
58                       svg.append("g")
59                           .attr("class", "x axis")
60                           .attr("transform", "translate(0," + height + ")")
61                           .call(xAxis)
62                           .append("text")
63                               .attr("x", scope.xaxisPos)
64                               .attr("dx", ".71em")
65                               .style("text-anchor", "end")
66                               .text(scope.xaxisName);
67                       // x axis legend setting from angular variables
68                       svg.append("g")
69                           .attr("class", "y axis")
70                           .call(yAxis)
71                           .append("text")
72                               .attr("transform", "rotate(-90)")
73                               .attr("y", scope.yaxisPos)
74                               .attr("dy", ".71em")
75                               .style("text-anchor", "end")
76                               .text(scope.yaxisName);
77                       // y axis legend setting from angular variables
78                       svg.selectAll(".bar")
79                           .data(data)
80                           .enter().append("rect")
81                           .attr("class", "bar")
82                           .attr("x", function(d) { return x(d.letter); })
83                           .attr("width", x.rangeBand())
84                           .attr("y", function(d) { return y(d.frequency); })
85                           .attr("height", function(d) 
86 				{ return height - y(d.frequency); });
87                       });
88                   }
89                }
90            });
```

代码可以从 [GitHub](https://github.com/piyasde/d3) 下载。

## 在 Angular 指令中使用 d3.js 和 Prototype.js 的简单柱状图——基于 JavaScript 类的方法

![AngularD3 柱状图](img/00003.jpeg)

我们最近正在努力将客户端 JavaScript 代码转换为面向对象的方式。因此，我们经历了 JavaScript OOP 的学习过程，并撰写了上一章——JavaScript 的 OOP 方式——一些有趣的研究。在学习 `d3.js` 图形创建的过程中，我们在 `Angular.js` 指令中编写了 `D3.js`——这让我们从 HTML 页面中的 D3 SVG 代码中解脱出来。

现在我们正尝试将 `d3.js` 代码分离出来，放入 JavaScript 框架中，为此我们采用了 `prototype.js` 来为 `d3.js` 代码分离创建 JavaScript 类。我们创建了 Angular 指令，并通过在 `prototype.js` 中创建类来分离与 `d3.js` 相关的代码，然后在 Angular 指令的链接函数中访问该类实例的相关代码。那么，我们在 HTML 中到底做了什么呢？

### 1> 在 HTML 页面中添加 `angular.js`、`prototype.js`、`d3.js` 以及 d3 相关 JavaScript 类的引用

```
1 <script type="text/javascript" src="js/prototype.js"></script>
2 <script src="js/barGraphProto.js"></script>
3 <script src="http://d3js.org/d3.v3.min.js"></script>
4 <script type="text/javascript" 
5 	src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.6/angular.min.js">
6 </script>
```

### 2> 在 HTML 中放置与 `d3.js` 相关的 Angular 指令——

```
 1 <div id="d3bar" angulard3-bar-graph datajson="'sample.json'" 
 2                xaxis-name = "'Year'" 
 3                xaxis-pos = "905"  
 4                yaxis-name = "'Frequency'" 
 5                yaxis-pos = "6" 
 6                d3-format= "'.0%'" >
 7 	<!-- angular directive is angulard3-bar-graph -->
 8 	<!-- directive variables are xaxis-name,yaxis-name,xaxis-pos,
 9 	    yaxis-pos,y axis data format(d3-format)
10 	    and finally the datajson variable which is holding the external data source -->
11 </div>
```

### 3> Angular 指令中的代码——

```
 1     angular.module('AngularD3BarGraph', []) // Angular Module Name
 2         .directive('angulard3BarGraph', function () { // Angular Directive
 3             return {
 4                 restrict: 'A', // Directive Scope is Attribute
 5             scope: {
 6                 datajson: '=',
 7                 xaxisName: '=',
 8                 xaxisPos: '=',
 9                 yaxisName: '=',
10                 yaxisPos: '=',
11                 d3Format: '='
12                 // All the Angular Directive Vaiables used as d3.js parameters
13            },
14            link: function (scope, elem, attrs) {
15                  var ourGraph = new BarGraph(scope.datajson,scope.xaxisName,
16 					     scope.xaxisPos,scope.yaxisName,
17                                              scope.yaxisPos,scope.d3Format);
18                  //d3 related Variable initialisation
19                  ourGraph.workOnElement('#'+elem[0].id); // Work on particular element
20                  ourGraph.generateGraph();  // generate the actual bar graph
21            }
22         }
23     });
```

### 4> 与 `d3` 相关的柱状图代码——





```
 1     // properties are directly passed to `create` method
 2     var BarGraph = Class.create({ // prototype class creation
 3         initialize: function(datajson,xaxisName,xaxisPos,yaxisName,yaxisPos,d3Format) {
 4                         this.datajson = datajson;
 5                         this.xaxisName = xaxisName;
 6                         this.xaxisPos = xaxisPos;
 7                         this.yaxisName = yaxisName;
 8                         this.yaxisPos = yaxisPos;
 9                         this.d3Format = d3Format;
10                         // Taking all the variables and set in Class 
11 			// Instance Variables (d3 property specific)
12                     },
13         workOnElement: function(element) {
14                         this.element = element;
15                         // Taking the DOM Element on which the graph will be drawn 
16                     },
17         generateGraph: function() {
18     
19                        //d3 specific coding
20                        var margin = {top: 20, right: 20, bottom: 30, left: 40},
21                            width = 960 - margin.left - margin.right,
22                            height = 500 - margin.top - margin.bottom;
23     
24                       var formatPercent = d3.format(this.d3Format);
25                          //setting the instance variable to d3 property
26     
27                       var x = d3.scale.ordinal()
28                            .rangeRoundBands([0, width], .1);
29     
30                       var y = d3.scale.linear()
31                               .range([height, 0]);
32     
33                       var xAxis = d3.svg.axis()
34                               .scale(x)
35                               .orient("bottom");
36     
37                       var yAxis = d3.svg.axis()
38                               .scale(y)
39                               .orient("left")
40                               .tickFormat(formatPercent);
41     
42                       var svg = d3.select(this.element).append("svg")
43                               .attr("width", width + margin.left + margin.right)
44                               .attr("height", height + margin.top + margin.bottom)
45                               .append("g")
46                               .attr("transform", 
47 				   "translate(" + margin.left + "," + margin.top + ")");
48     
49                      d3.json(this.datajson, function(error, data) { // getting the data
50                               if (error) return console.warn(error);
51     
52                               x.domain(data.map(function(d) { return d.letter; }));
53                               y.domain([0, d3.max(data, function(d) 
54                                                          { return d.frequency; })]);
55     
56                      svg.append("g")
57                              .attr("class", "x axis")
58                              .attr("transform", "translate(0," + height + ")")
59                              .call(xAxis)
60                              .append("text")
61                              .attr("x", this.xaxisPos)
62                              .attr("dx", ".71em")
63                              .style("text-anchor", "end")
64                              .text(this.xaxisName);
65     
66                      svg.append("g")
67                              .attr("class", "y axis")
68                              .call(yAxis)
69                              .append("text")
70                              .attr("transform", "rotate(-90)")
71                              .attr("y", this.yaxisPos)
72                              .attr("dy", ".71em")
73                              .style("text-anchor", "end")
74                              .text(this.yaxisName);
75     
76                      svg.selectAll(".bar")
77                              .data(data)
78                              .enter().append("rect")
79                              .attr("class", "bar")
80                              .attr("x", function(d) { return x(d.letter); })
81                              .attr("width", x.rangeBand())
82                              .attr("y", function(d) { return y(d.frequency); })
83                              .attr("height", function(d) 
84 				  { return height - y(d.frequency); });
85                 }.bind(this)); // the bind syntax is important. 
86 			       // Otherwise class instance variables will 
87                                // not be accessible in inner function
88              }
89         });
```

[这里](http://www.phloxblog.in/wp-content/uploads/2013/07/angularProto.zip)是供读者感兴趣的代码。我们将在下一章中在 Angular.js 指令中重用与 d3 相关的 JavaScript 类代码。

## 使用 d3.js 和 Prototype.js 在 Angular 指令中的简单柱状图 – 基于元素的指令定义

![AngularD3 柱状图](img/00003.jpeg)

AngularD3 柱状图

我们最近正在努力将客户端 JavaScript 代码转换为面向对象的方法。因此，我们经历了 JavaScript OOP 的学习过程，并撰写了上一章——`Javascript in OOP Way -- some interesting study`，在学习 d3.js 图形创建的同时，我们编写了`D3.js in Angular.js Directive -- a relief from D3 svg code in HTML Page`。

我们已经将 d3.js 代码分离出来放入 JavaScript 类中，为此我们使用了 prototype.js 来创建用于 d3.js 代码分离的 JavaScript 类。因此，`Simple Bar Graph with d3.js and Prototype.js - a Javascript Class based Approach`是我们之前的章节之一。当前章节是 Angular 指令的一个变体——它是一个基于元素的指令。

**示例 -**

在 HTML 中，我们想要引入新的标签元素，比如`<bargraph />`。我们创建了 Angular 指令，并通过在 prototype.js 中创建类来分离 d3.js 相关代码，然后在 Angular 指令的`Complie`函数中访问类实例相关代码。那么我们在 HTML 中到底做了什么？

### 1> 在 HTML 页面中添加了`angular.js`、`prototype.js`、`d3.js`以及 d3 相关 JavaScript 类的引用

```
1      <script type="text/javascript" src="js/prototype.js"></script>
2      <script src="js/barGraphProto.js"></script>
3      <script src="http://d3js.org/d3.v3.min.js"></script>
4      <script type="text/javascript" 
5 	src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.6/angular.min.js">
6      </script>
```

### 2> 将 d3.js 相关的 Angular 指令放入 HTML 中 -

```
 1     <bargraph id="d3bar" 
 2               datajson="sample.json" 
 3               xaxis-name = "'Year'" 
 4               xaxis-pos = "905" 
 5               yaxis-name = "'Frequency'" 
 6               yaxis-pos = "6" 
 7               d3-format= "'.0%'" />
 8        <!-- angular directive is bargraph -->
 9        <!-- here "d3bar" is the id of bargraph tag directive variables are 
10 	    xaxis-name,yaxis-name,xaxis-pos,yaxis-pos,
11             yaxis data format(d3-format) and finally the datajson variable 
12 	    which is holding the external data source -->
```

### 3> Angular 指令中的代码 -





```
 1 angular.module('AngularD3BarGraph', []) // Angular Module Name
 2 .directive('bargraph', function () { // Angular Directive
 3     return {
 4         restrict: 'E', // Directive Scope is Element
 5         replace: true, // replace original markup with template
 6         transclude: false, // not to copy original HTML DOM
 7         compile: function (elem, attrs) { // the compilation of DOM is done here.
 8 	// It is responsible for produce HTML DOM or it returns a 
 9 	// combined link function. Further Docuumentation on this - 
10 	// http://docs.angularjs.org/guide/directive
11 
12 
13             var html = "<div id='" + attrs.id + "' ></div>"; 
14 			// the HTML to be produced
15             var newElem = $(html);
16             elem.replaceWith(newElem); // Replacement of the element.
17             var ourGraph = new BarGraph(attrs.datajson,attrs.xaxisName,
18 					attrs.xaxisPos,attrs.yaxisName,
19 			                attrs.yaxisPos,attrs.d3Format);
20 
21 		                //d3 related Variable initialisation             
22 
23             ourGraph.workOnElement('#'+attrs.id);
24             // Work on particular element
25             ourGraph.generateGraph();  // generate the actual bar graph
26    }
27 }
28 });
```

### 与 d3 相关的柱状图代码

```
 1     // properties are directly passed to `create` method
 2     var BarGraph = Class.create({ // prototype class creation
 3         initialize: function(datajson,xaxisName,xaxisPos,yaxisName,yaxisPos,d3Format) {
 4                         this.datajson = datajson;
 5                         this.xaxisName = xaxisName;
 6                         this.xaxisPos = xaxisPos;
 7                         this.yaxisName = yaxisName;
 8                         this.yaxisPos = yaxisPos;
 9                         this.d3Format = d3Format;
10                         // Taking all the variables and set in Class 
11 			// Instance Variables (d3 property specific)
12                     },
13         workOnElement: function(element) {
14                         this.element = element;
15                         // Taking the DOM Element on which the graph will be drawn
16                     },
17         generateGraph: function() {
18     
19                        //d3 specific coding
20 
21                        var margin = {top: 20, right: 20, bottom: 30, left: 40},
22                            width = 960 - margin.left - margin.right,
23                            height = 500 - margin.top - margin.bottom;
24     
25                       var formatPercent = d3.format(this.d3Format);
26 			//setting the instance variable to d3 property
27     
28                       var x = d3.scale.ordinal()
29                            .rangeRoundBands([0, width], .1);
30     
31                       var y = d3.scale.linear()
32                               .range([height, 0]);
33     
34                       var xAxis = d3.svg.axis()
35                               .scale(x)
36                               .orient("bottom");
37     
38                       var yAxis = d3.svg.axis()
39                               .scale(y)
40                               .orient("left")
41                               .tickFormat(formatPercent);
42     
43                       var svg = d3.select(this.element).append("svg")
44                               .attr("width", width + margin.left + margin.right)
45                               .attr("height", height + margin.top + margin.bottom)
46                               .append("g")
47                               .attr("transform", "translate(" + margin.left + "," + margin\
48 .top + ")");
49     
50                      d3.json(this.datajson, function(error, data) { // getting the data
51                               if (error) return console.warn(error);
52     
53                               x.domain(data.map(function(d) { return d.letter; }));
54                               y.domain([0, d3.max(data, function(d) { return d.frequency; \
55 })]);
56     
57                      svg.append("g")
58                              .attr("class", "x axis")
59                              .attr("transform", "translate(0," + height + ")")
60                              .call(xAxis)
61                              .append("text")
62                              .attr("x", this.xaxisPos)
63                              .attr("dx", ".71em")
64                              .style("text-anchor", "end")
65                              .text(this.xaxisName);
66     
67                      svg.append("g")
68                              .attr("class", "y axis")
69                              .call(yAxis)
70                              .append("text")
71                              .attr("transform", "rotate(-90)")
72                              .attr("y", this.yaxisPos)
73                              .attr("dy", ".71em")
74                              .style("text-anchor", "end")
75                              .text(this.yaxisName);
76     
77                      svg.selectAll(".bar")
78                              .data(data)
79                              .enter().append("rect")
80                              .attr("class", "bar")
81                              .attr("x", function(d) { return x(d.letter); })
82                              .attr("width", x.rangeBand())
83                              .attr("y", function(d) { return y(d.frequency); })
84                              .attr("height", function(d) { return height - y(d.frequency);\
85  });
86                 }.bind(this)); // the bind syntax is important. 
87 			       // Otherwise class instance variables will not be
88                                // accessible in inner function
89              }
90         });
```

[此处](http://www.phloxblog.in/wp-content/uploads/2013/07/angularElementProto.zip)是供读者参考的代码。

## 创建 Google Chrome 扩展以添加自定义 RSS 订阅阅读器

我们制作了一个 RSS 订阅阅读器，它能够通过标签导航在同一页面中读取多个 RSS 订阅。我们使用了 `Bootstrap.js` 和 CSS，从开发者的角度为应用程序提供了标准 UI。接下来，我们尝试将这个 RSS 订阅阅读器作为 Google Chrome 扩展提供。其背后的想法是——当我们连接互联网并打开 Google Chrome 浏览器，点击一个图标时，所有与我们相关的当前新闻都能随时可用。下面是该订阅阅读器的图示。

![RSS 订阅阅读器](img/00005.jpeg)

RSS 订阅阅读器

我们使用了一些技术和技巧来实现这一点。下面列出如下：

**1> 我们制作了一个自定义的 PHP RSS 订阅阅读器**

**2> 我们集成了 `bootstrap.js` 和 CSS，以创建带有标签导航的标准 UI**

**3> 我们使阅读器支持跨域 Ajax 请求**

**4> 我们制作了一个 Google Chrome 扩展**

**5> 我们使用了 Google 字体来装饰内容**

**6> 我们授予了 Google Chrome 扩展从外部 URL 读取订阅的权限**

关于第 1、2 和 3 点，读者应阅读[使用 Bootstrap.js 和 CSS 创建 RSS 订阅阅读器并进行装饰](http://www.phloxblog.in/creating-rss-feed-reader-decorating-bootstrap-js/)。

现在，要制作 Chrome 扩展，读者应阅读[入门：构建 Chrome 扩展](https://developer.chrome.com/extensions/getstarted.html)。

### 对 UI 进行一点装饰——使用 Google 字体，我们使用了——

```
1     <link href='http://fonts.googleapis.com/css?family=Josefin+Slab' rel='stylesheet' type\
2 ='text/css'>
3     <style>
4     body {
5     .....
6     
7     font-family: 'Josefin Slab', serif;
8     }
9     </style>
```

### 另一个给读者的提示——阅读[入门：构建 Chrome 扩展](https://developer.chrome.com/extensions/getstarted.html)后，我们将了解配置文件——`manifest.jon`。





现在，要使 Chrome 扩展程序能够访问互联网上的任何外部内容，我们需要在 `manifest.json` 中授予相应的权限。

### 以下是权限代码片段：

```
1     ....
2       "permissions": [
3         "http://phloxblog.in/"
4       ],
5     ....
```

因为我们通过自己托管的服务器获取外部订阅源内容。

**编码：**

服务端的 PHP 代码可以在此处下载：[这里](http://www.phloxblog.in/wp-content/uploads/2013/06/rss.zip)。Google Chrome 扩展程序的完整代码也可在此处获取：[这里](http://www.phloxblog.in/wp-content/uploads/2013/06/ExperimentGC.zip)。

因此，我们在此提供了未打包版本的扩展程序，读者可以自行试验，并根据自己的想法使其更加实用。

## 在 Google Chrome 扩展程序中使用 Angular.js、HTML5 LocalStorage 和 Bootstrap 装饰的任务列表

我们曾设想创建一个每日任务列表作为 Google Chrome 扩展程序，并附带与每日感兴趣新闻相关的新闻订阅源阅读器。以下是使用以下集成工具制作的 Chrome 扩展程序：

### 1. Angular.js

用于实现任务列表和任务添加功能。

### 2. HTML5 LocalStorage

用于将任务数据保存在临时存储中，并从中提供数据。

### 3. 集成我们自己的个人订阅源阅读器

以便获取有用的新闻。

### 4. 制作一个极简的 Google Chrome 扩展程序

使其可在 Google Chrome 浏览器中使用。

以下是我们之前的相关文章：

**HTML5 和 LocalStorage：**

A. [HTML5 LocalStorage 和 Json 对象 – 一些操作](http://www.phloxblog.in/html5-localstorage-json-object-operations/)

**RSS 订阅源阅读器：**

B. [创建 RSS 订阅源阅读器并使用 Bootstrap.js 和 CSS 进行装饰](http://www.phloxblog.in/creating-google-chrome-extension-add-custom-rss-feed-reader/)

**在 Google Chrome 扩展程序中集成订阅源阅读器：**

C. [创建 Google Chrome 扩展程序以添加自定义 RSS 订阅源阅读器](http://www.phloxblog.in/creating-google-chrome-extension-add-custom-rss-feed-reader/)

[这里](http://www.phloxblog.in/wp-content/uploads/2013/06/Experiment1.zip) 是我们使用 Angular.js、HTML5 LocalStorage 和 RSS 订阅源阅读器的工作代码库。

读者也可以在 [github](https://github.com/piyasde/Experiment) 上找到代码。另外，[这里](http://www.phloxblog.in/wp-content/uploads/2013/06/Experiment19032013.zip) 是我们的 Google Chrome 扩展程序。

读者可以在 [Google Chrome 网上应用店](https://chrome.google.com/webstore/detail/task-list-and-feed-reader/igiphijnjbhhpkbdgmjdlfdoacojddig) 中体验它。

我们在本文前面提到的文章中已经讨论了制作 RSS 订阅源阅读器、Bootstrap 集成以及制作 Google Chrome 扩展程序的部分。以下是扩展程序的图片：

![任务列表和订阅源阅读器](img/00006.jpeg)

任务列表和订阅源阅读器

这里我们主要展示和讨论 **Angular.js 和 HTML5 LocalStorage 的集成**。

我们将在代码中内联注释以帮助理解。

### Angular.js 中的 HTML 模板

用于显示任务列表的代码（`listtodo.html`）如下：

```
 1 <form ng-submit="clear()">  
 2 <!-- 提交此表单时，将触发控制器中的 clear 方法 -->
 3 <div style="float:right;"><center><button type="submit" >
 4 			Clear Tasks</button></center></div>
 5   <ul style="list-style-type:none">
 6      <li ng-repeat="todo in todos" > 
 7 	<!-- 我们最喜欢的 angular.js 重复器功能 -->
 8         <p>{{todo.task}}</p> 
 9 	<!-- todo 对象中的任务元素将在此处显示。它是一个 Json 元素 -->
10      </li>
11   </ul>
12 </form>
```

#### 用于显示添加任务的代码（`addtodo.html`）如下：

```
 1 <form ng-submit="save()"> <!-- 控制器中将数据保存到 localstorage 的方法 -->
 2 <fieldset>
 3   <legend>New Task</legend>
 4   <div class="control-group">
 5      <center><input type="text" placeholder="Task..." ng-model="task" 
 6 						size=50 required/></center> 
 7 	<!--Angular.js 模型-->
 8   </div>
 9 </fieldset>
10 <p>
11    <div><center><button type="submit" >Remember it...</button></center></div>
12 </p>
13 </form>
```

#### `index.html` 中的主要代码片段如下：

```
 1 <html lang="en" ng-app="taskslist" ng-csp=""> 
 2 <!-- 在 Chrome 扩展程序中启用 angular.js (ng-csp)-->
 3 .....
 4 <div ng-controller="TaskListCtrl" > 
 5 <!-- Angular 控制器，负责在视图中渲染数据 -->
 6 .....
 7 <div id="addtodo" class="tab-pane fade" ng-include="'views/addtodo.html'"></div> 
 8 <div id="listtodo" class="tab-pane fade active in" ng-include="'views/listtodo.html'"></div>
 9 <!-- 使用 ng-include 添加 angular 模板 -->
```

#### 现在，控制器中的主要代码片段：

```
 1       /* 控制器 */
 2       function TaskListCtrl($scope,$location) {
 3     
 4         $scope.save = function() {
 5               var tmpVar = {}; 
 6     	  tmpVar.task = this.task; 
 7 		// 新的 json 对象，用于从 angular.js 模型获取数据
 8     	  this.task = '';
 9     	  $scope.todos.push(tmpVar); 
10 		// 将 json 对象推入 angular $scope 变量中的数组
11     	  localStorage.setItem("todoList", JSON.stringify($scope.todos)); 
12 			// 将数组保存到 html5 本地存储
13     	  console.log($scope.todos.length);
14     	  $scope.list();
15         };
16     
17         //数据加载
18         $scope.list = function(){ 	 
19     	  if(typeof $scope.todos ==='undefined')
20     	  {
21     		  if(localStorage.getItem("todoList") ===null)
22     		  {
23     		  	$scope.todos = [];
24     		  }
25     		  else
26     		  {
27     		  	$scope.todos = JSON.parse(localStorage.getItem("todoList")); 
28 			// 从 localstorage 获取值
29     		  }
30     	  } 
31     	  else
32     	  {
33     		  console.log('length'+$scope.todos.length);
34     	  }
35     	};
36     
37         $scope.clear = function(){ 	
38     		  $scope.todos = [];
39     		  localStorage.setItem("todoList", JSON.stringify($scope.todos)); 
40                       // 清除 HTML5 localstorage 中特定存储变量的所有值
41     	};
42     
43        $scope.list(); 
44 	// 每当我们通过这个 angular 控制器时，都会触发 list 方法
45        if(!$scope.$$phase) {
46     	$scope.$apply(); // 应用 angular $scope 中的所有更改
47        }
48     }
```

## 图数据库的初步概念

我们将逐步尝试在文章中结合 neo4j（一种图数据库）来阐明图数据库的概念。

以下是我们的第一篇文章，描述了图数据库的快速入门概念。

**图：**

图由相互连接的节点中的信息组成。一个图也可以只包含一个节点。一个特定的节点可以拥有多个属性，以键值对的形式存在。此外，节点可以通过多种方式连接，我们称之为关系。

**示例：**

学校信息是一个单独的节点。学生和教师是不同的节点，通过关系连接。

学生（节点）在（关系）学校（节点）学习。

教师（节点）在（关系）学校（节点）教学。

学校有名称、地址、建校年份、认证等，这些可以描述为属性。

学生有姓名、地址、入学年份、班级等，这些可以描述为属性。

教师有姓名、地址、入职年份、最高学历等，这些可以描述为属性。

**节点：**

节点是图中每一组实体信息的集合。

**示例：**

如果我们将学校信息系统视为一个图，

学校本身是学校图中的一个节点。

每个学生是学校图中的一个节点。

同样，每个教师也是学校图中的一个节点。

**关系：**

节点通过某些信息连接起来——这些信息就是图中的关系。

**示例：**

学生在学校学习。

教师在学校教学。





这里 `study` 和 `teach` 是学校图中节点之间的关系信息。

## 标签

当节点在图中形成一组，并通过某些信息进行标识时，这些信息就被称为标签。

### 示例

在学校图中，我们可以为学校图中的所有学生标记 `(All Students)` 标签。

同样，可以为相应的学生赋予 `(5th Class Students)`、`(6th Class Students)` 标签。

这里的 `(All Students)`、`(5th Class Students)`、`(6th Class Students)` 可以称为子图。

## 节点遍历

当我们在所有节点的图中查找某些特定信息时，我们会按照某种预先确定的最优方式处理信息，这称为图遍历。

### 示例

在学校图中，要获取诸如“教授五年级学生的老师姓名”这样的信息，我们可以通过以下方式遍历：

在 `(Particular School)` –>> `study by` –>> `(5th Class Students)` –>> `Teached by` –>> `(Teachers)`

注意：以上是遍历信息，可用于理解图中的遍历。

## 索引

当我们想要获取节点或关系的特定信息集时，我们将所有这些信息放入特定的映射中，这些映射称为索引。

### 示例

在学校图中，我们可以为 `(Science Subject Teachers)`、`(Art Subject Teachers)` 等设置特定的节点集，并将其放入索引中。

在我们后续关于图数据库的文章中，我们将描述一个可以使用图数据库的案例研究。

然后，我们将描述在 `neo4j` 上下文中通过 `Cypher Query` 从图数据库获得的模式和信息。

## 基于 Neo4j Cypher 查询的图数据库案例研究

我们在此展示一个与图数据库模型相关的典型案例研究。

### 图数据库案例研究

#### 节点

- 实体 – `User`（表示为节点）
- 实体 – `Organisation`（表示为节点）
- 实体 – `Project`（表示为节点）
- 实体 – `Skill`（表示为节点）

#### 关系

- 用户在组织中工作 –（关系 – `worked`）
- 用户关注组织 –（关系 – `following`）
- 用户完成过项目 –（关系 – `has done`）
- 用户拥有技能 –（关系 – `has`）
- 用户是用户的朋友 –（关系 – `is Friend`）

### 图数据库表示的图解模型

![图数据库图解](img/00007.gif)

图数据库图解

## 示例图数据库的 Neo4j Cypher 查询快速浏览

我们尝试展示不同的 Neo4j Cypher 查询，以展示图数据库的不同功能。

要开始了解图数据库的基本概念，请阅读前面章节中的《图数据库基本概念》和《基于 Neo4j Cypher 查询的图数据库案例研究》。

### 安装

从 (http://www.neo4j.org/download) 安装 Neo4J。

在 Windows 中启动 Neo4j 服务器：

`neo4j.bat start`

然后打开浏览器访问地址 – `http://localhost:7474`

以下是我们之前在数据控制台上测试过的 Cypher 查询，这些查询与前一章节中提到的模型相关。

### 创建节点

```
CREATE (user {entitytype:'user', name : 'bill'}) return user;
```

```
CREATE (company {entitytype:'company', name : 'CTS'}) return company;
```

```
CREATE (project {entitytype:'project', name : 'ABC Insurance'}) return project;
```

```
CREATE (skill {entitytype:'skill', name : 'HTML, CSS'}) return skill;
```

这里展示了一些节点创建的示例。

### 创建关系

```
START user=node(1), company=node(9) CREATE relation = user-[:WORKS_AT]->company return relation;
```

```
START user=node(7), company=node(9) CREATE relation = user-[:FOLLOWS]->company return relation;
```

```
START user=node(5), skill=node(12) CREATE relation = user-[:HAS_SKILL]->skill return relation;
```

```
START user=node(6), seconduser=node(7) CREATE relation = user-[:FRIEND]->seconduser return relation;
```

```
START user=node(6), work=node(11) CREATE relation = user-[:CURRENT_ENGADGEMENT]->work return relation;
```

```
START user=node(6), work=node(11) CREATE relation = user-[:CURRENT_ENGADGEMENT]->work return relation;
```

```
START company=node(9), project=node(11) CREATE relation = company-[:EXECUTING_UNDER]->project return relation;
```

这里展示了一些关系创建的示例。

### 删除节点

```
START nullnode=node(0), DELETE nullnode;
```

// 删除一个节点

### 获取节点和关系

```
start n = node(*) return n;
```

// 查看所有节点

```
start r = relationship(*) return r;
```

// 查看所有关系

```
start n = node:node_auto_index(name = 'john') return n;
```

// 选择特定用户 –> 通过索引选择数据

```
START n=node(*) WHERE has(n.name) RETURN n;
```

// 选择具有 name 属性的节点

```
START n=node(*) WHERE has(n.name) and (n.entitytype = 'skill') RETURN n;
```

// 选择 entitytype = 'Skill' 的节点

#### 索引

// 获取节点和关系中的索引

```
START n=node(*) WHERE has(n.name) and n.name =~ 'j.*' return n;
```

// 从索引中选择节点名称以 "j" 开头的节点

```
START n=node(*) WHERE has(n.name) and n.name =~ '.*j.*' return n;
```

// 从索引中选择节点名称包含 "j" 的节点

```
start n = node(6) match(n)–(x) return x;
```

// 返回与节点 6 相关的所有节点

```
start n = node:node_auto_index(name='andrew') match(n)–(x) return x;
```

// 返回与节点名称 'andrew' 相关的所有节点

```
start n = node:node_auto_index(name='andrew') match(n)<–(x) return x;
```

// 返回所有与 'andrew' 有入向关系的节点

```
start n = node:node_auto_index(name='andrew') match(n)–>(x) return x;
```

// 返回所有与 'andrew' 有出向关系的节点

// 注意：这里将返回 andrew 具有出向关系的所有实体类型（skill, project, user, company）

```
START n=node:node_auto_index(name='andrew') MATCH (n)-[:WORKS_AT]->(x) RETURN x;
```

// 按关系类型和出向节点匹配

```
START n=node:node_auto_index(name='linda') MATCH (n)-[:FRIEND]->(x) RETURN x;
```

// 这里的结果将是 'andrew'，他是 'linda' 的出向关系

```
START n=node:node_auto_index(name='linda') MATCH (n)<-[:FRIEND]-(x) RETURN x;
```

// 这里的结果将是 'john'，对于他来说 'linda' 是出向关系

```
START n=node:node_auto_index(name='andrew') MATCH (n)-[r:WORKS_AT]->() return r;
```

// 按关系类型匹配并使用标识符

```
START a=node:node_auto_index(name='andrew') MATCH (a)-[:WORKS_AT]->(b)<-[:WORKS_AT]-(c) return a,b,c
```

// 返回多个关系

// 这里将返回所有在 'IBM' 工作的人，因为 'andrew' 在 'IBM' 工作

```
START n=node(*) WHERE has(n.name) and (n.name =~ 'john.*') RETURN n;
```

// 查询中的 WHERE 条件、'节点中存在属性' 子句以及 LIKE 子句

```
START n=node(*) WHERE n.entitytype? = "skill" RETURN n;
```

// 如果节点缺少属性，则默认为 true，并返回所有其他匹配的节点

```
START n=node(*) WHERE n.entitytype! = "skill" RETURN n;
```

// 仅返回匹配的节点。注意："!=" 和 "! =" 不同

```
START persons=node(*), company=node:node_auto_index(name='IBM') WHERE has(persons.name) and (persons.entitytype='user') and not(persons–>company) RETURN persons;
```

// 将返回与 'IBM' 没有关系的人员

```
START persons=node(*), company=node:node_auto_index(name='IBM') WHERE has(persons.name) and (persons.entitytype='user') and (persons–>company) RETURN persons;
```

// 将返回与 'IBM' 有关系的人员（注意这里的 'WORKS_AT' 和 'FOLLOWS' 关系）

```
START persons=node(*), company=node:node_auto_index(name='IBM') WHERE has(persons.name) and (persons.entitytype='user') and (persons-[:WORKS_AT]->company) RETURN persons;
```

// 将返回与 'IBM' 有关系的人员（仅 'WORKS_AT' 关系）





```cypher
START me=node:node_auto_index(name='andrew') MATCH me-->friend where (friend.entitytype='user') RETURN count(friend),friend;
// Return only those users who are outbound to 'andrew'
```

```cypher
START me=node:node_auto_index(name='andrew') MATCH me<--friend<--friend_of_friend where (friend_of_friend.entitytype='user') RETURN count(friend_of_friend),friend_of_friend;
// This is a 'friend of friend' relationship. Here 'John' is friend of 'linda' and 'linda' is friend of 'andrew'
```

```cypher
START me=node:node_auto_index(name='andrew'),company=node:node_auto_index(name='CTS') MATCH me<--friend<--friend_of_friend where (friend_of_friend.entitytype='user') and (friend_of_friend-[:WORKS_AT]->company) RETURN count(friend_of_friend),friend_of_friend,company;
// This is a 'friend of friend' relationship. Here 'John' is friend of 'linda' and 'linda' is friend of 'andrew' and he is returned as he is working in 'CTS'
```

```cypher
START me=node:node_auto_index(name='andrew'),company=node(8,9) MATCH me<--friend<--friend_of_friend where (friend_of_friend.entitytype='user') and (friend_of_friend-[:WORKS_AT]->company) RETURN count(friend_of_friend),friend_of_friend,company;
// Same Query of above for selection of all the companies
```

```cypher
start n = node:node_auto_index(name='UI Restructuring') match n<--x<-[:WORKS_AT]-x1 return x1;
// Here the project is done in 'IBM' and nodes – 'x1' are working in the company;
```

```cypher
start n = node:node_auto_index(name='UI Restructuring') match n<--x<-[:FOLLOWS]-x1 return x1;
// Here the project is done in 'IBM' and nodes – 'x1' are following the company;
```

```cypher
START n=node:node_auto_index(name='jude') MATCH (n)-[:WORKS_AT]->x<-[:FOLLOWS]-x1 return x1;
// return all the nodes which follows the company on which 'jude' is working;
```

```cypher
START n=node:node_auto_index(name='CTS') MATCH (n)<-[r:WORKS_AT]-() RETURN type(r), count(*);
// How much nodes are in the graph who are with 'WORKS_AT' in 'CTS'
```

```cypher
START n=node(*) RETURN distinct(n.entitytype?); // Select distinct entity types
```

```cypher
START person=node:node_auto_index('name: *') MATCH person-[?:WORKS_AT]->company where person.entitytype ='user' RETURN person.name
// return all the nodes with 'WORKS_AT' relationship
```

```cypher
START begin = node(4), end = node(7) MATCH p = begin -[*]-> end foreach(n in nodes(p) : SET n.network = true);
// Updating connecting nodes and example of loop in cypher query
```

```cypher
START begin = node(4), end = node(7) MATCH p = begin -[*]-> end return *; // showing the result of updation in connecting nodes
```

```cypher
START n=node(1) MATCH p=n-[*..]->b WHERE ANY(x in nodes(p) WHERE x.network? = true) RETURN p;
// Example of Predicates
```

### 参考资料

1. `http://docs.neo4j.org/refcard/1.9/`
2. `http://java.dzone.com/articles/10-caveats-neo4j-users-should`
3. `http://docs.neo4j.org/chunked/milestone/cypher-query-lang.html`

我们展示了一些可以在图数据库实际应用中使用的查询。由于这是一种新型的 NoSQL 数据库，以上内容是我们提供的一些 neo4j Cypher 查询示例的介绍。

## 使用 Node.js、Express.js REST 服务和 Neo4j（neo4j-js 模块）开发 Web 应用程序

本文是一个概念验证，旨在使用基于 JavaScript 的 Web 服务器（Node.js）和 Neo4j 构建 Web 应用程序。

为了实现这一目标，我们选择了：

1. Node.js 用于服务器端开发
2. 基于 REST 的 Web 服务创建，使用 `express.js`
3. 图数据库 – Neo4j
4. Node.js Neo4j 模块扩展（`neo4j-js`）

我们创建了一个基于 JavaScript 的 Web 服务器的概念验证，重点在于使用基于 JavaScript 的框架 Node.js 处理 Neo4j（图数据库）。

我们借助了 Neo4j-js 模块，该模块在 Neo4j 官网以及 [Bret Copeland 的 Github 项目贡献](https://github.com/bretcope/neo4j-js) 中有所讨论。

我们根据之前关于 Neo4j 章节的知识，为本应用程序采用了 Neo4j 图数据库的参考数据模型。

首先是架构图——

![架构](img/00008.jpeg)

架构

以下是具体步骤——

### 安装

1. 从[此处](http://nodejs.org/download/)下载并安装 Node.js。
2. 要开发应用程序，我们需要为 Node.js 安装 `neo4j-js` 模块

   命令 – `npm install neo4j-js`（需连接互联网）

3. 我们需要为 Node.js 安装 `express.js`

   命令 – `npm install express`（需连接互联网）

4. 我们需要安装 `http-status`

   命令 – `npm install http-status`（需连接互联网）

### 配置代码

现在，我们将描述代码部分——

```javascript
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path"),
4     HTTPStatus = require('http-status'); // To return http status for error codes
5 
6 var config = require('./config');
```

这里我们根据 Node.js 的概念，在 JavaScript 变量中初始化了 `express.js`。

我们引入了另一个 js 文件——`config.js`，用于存放所有与 Neo4j 配置相关的信息。

```javascript
1 var app = express();
```

这里我们在 `app` 变量中初始化了 express Web 服务器。

```javascript
1 var neo4j = require('neo4j-js');
```

这里我们使 Node.js 的 `neo4j-js` 模块可用。

```javascript
1 var neo4jurl = process.env.NEO4J_URL ;
2 neo4jurl = neo4jurl +'/db/data/';
```

这里从配置文件中设置了 Neo4j 数据库服务器的 URL。

```javascript
1 var query = [ 'START me=node:node_auto_index(name={inputusername}) MATCH me<--friend<--fri\
2 end_of_friend where 
3 	    (friend_of_friend.entitytype={inputentitytype}) RETURN friend_of_friend;'];
4 
5 var insertquery = [ 'CREATE (user {entitytype:{inputentitytype}, name : {inputname}}) retu\
6 rn user;' ];
7 
8 var queryforallrelation = [ 'start n = node:node_auto_index(name={inputusername}) match(n)\
9 --(x)  return x;'];
```

这里所有查询变量都设置为 Neo4j Cypher 查询。

```javascript
1 // Express Config
2 
3 app.configure(function () {
4   app.use(express.bodyParser());
5   app.use(express.methodOverride());
6   app.use(app.router);
7   app.use(express.static(path.join(application_root, "public")));
8   app.use(express.errorHandler({ dumpExceptions: true, showStack: true }));
9 });
```

这里我们进行了与 `express.js` 相关的配置。

### REST 服务代码

```javascript
1 app.get('/api', function (req, res) {
2   res.send('Our Sample API is up...');
3 });
```

这里我们创建了第一个基于 REST 的 Web 服务，并测试了 `express.js` 是否正常运行。

我们的示例 API 将是：`http://127.0.0.1:1212/api`（GET 方法）

```javascript
 1 app.get('/friendoffriend/:username', function (req, res){
 2 	res.set({'Content-Type': 'text/json'}); // setting content type
 3 	username = req.params.username;
 4 	type = 'user';
 5 	neo4j.connect(neo4jurl, function (err, graph) { //Connecting neo4J
 6 	graph.query(query.join('\n'), {inputusername : username, inputentitytype :type} ,
 7              function (err, results) {	// Query to Neo4j Database through Neo4j-js Module
 8 		if (err) {
 9 			res.send(HTTPStatus.INTERNAL_SERVER_ERROR,'Internal Server Error'); 
10                         // Return Http Status for Error
11 		}
12 		else {
13 			res.send(HTTPStatus.OK,JSON.stringify(results)); 
14                         // Return the json in response
15 		}
16 	     });	
17      });
18 });
```

这里我们创建了 REST API，用于从 Neo4j 节点集合中获取用户信息，并通过 Neo4j-js 扩展库实现。我们使用 Cypher 查询语言编写了一个“朋友的朋友”查询。

有关 Neo4j Cypher 查询的更多信息，请参阅前一章——示例图数据库的 Neo4j Cypher 查询。

我们的示例 API 将是：`http://127.0.0.1:1212/friendoffriend/andrew`（GET 方法）





```javascript
 1 app.get('/insertuser/:username', function (req, res){
 2 	res.set({'Content-Type': 'text/json'});
 3 	username = req.params.username;
 4 	type = 'user';
 5 	neo4j.connect(neo4jurl, function (err, graph) { // Connection to neo4J
 6 	graph.query(insertquery.join('\n'), {inputname : username, inputentitytype :type} 
 7              ,function (err, results) {	// Query to Neo4j through neo4j-js module
 8 		if (err) {
 9 			res.send(HTTPStatus.INTERNAL_SERVER_ERROR,'Internal Server Error');
10                         // Return Http Status for Error
11 		}
12 		else {
13 			res.send(HTTPStatus.OK,JSON.stringify(results));
14                         // Return the json in response 
15 		}
16 	    });	
17        });
18 });
```

这里我们通过 REST Web 服务调用，使用 Cypher 查询在数据库中插入了一个节点。

我们的示例 API 将是 - `http://127.0.0.1:1212/insertuser/anotheruser`（GET 方法）

```javascript
 1 //Cypher Query with Javascript Callback Example
 2 
 3 function neo4jQuery(neo4jurl, query, parameters, giveresults) { 
 4         //Function with query, parameter and callback as arguments
 5 	neo4j.connect(neo4jurl, function (err, graph) {  // Connection to neo4J
 6 		graph.query(query.join('\n'), {inputusername : 'andrew'} ,
 7                         function (err, results) { // Query to Neo4j through neo4j-js module
 8 
 9 			if (err) {
10 				giveresults(HTTPStatus.INTERNAL_SERVER_ERROR);  
11 				// Return Http Status in callback
12 			}
13 			else {
14 				giveresults(JSON.stringify(results));  
15 				// Return the json in callback
16 			}
17 		});	
18 	});
19 }
20 
21 
22 //Below is a separation of REST related code and neo4j related code via a javascript callb\
23 ack function
24 
25 app.get('/allrelations/:username', function (req, res){
26 	res.set({'Content-Type': 'text/json'});
27 	username = req.params.username;
28 	parameters = {inputusername : username};
29 	neo4jQuery(neo4jurl, queryforallrelation, parameters, function(results){ // the previous \
30 function is called
31 		res.send(results);
32 	});
33 });
```

我们的示例 API 将是 - `http://127.0.0.1:1212/allrelations/andrew`（GET 方法）

上面我们展示了另一个来自 Node.js 的查询示例，包含查询、参数和回调函数。

```javascript
1 // Launch server
2 app.listen(1212);
```

我们让服务器监听 1212 端口。

要运行应用程序，我们应该在命令行中使用 - `node neo4jtest.js`。

## MongoDB 快速入门

我们在项目工作中使用了一些 MongoDB 中的有用命令。以下是 MongoDB 命令的快速参考，这些命令可以在 MongoDB shell 中执行。我们已经在 MongoDB shell 中使用测试数据示例测试了所有命令。

我们可以从[这里](http://www.mongodb.org/downloads)下载 MongoDB。

启动 MongoDB

我们应该使用 -

`mongod –dbpath <<我们的 MongoDB 数据目录>>`

现在从 shell 启动数据库 -

`mongo` // 启动数据库

`db` // 测试当前数据库

`show dbs` // 显示所有数据库

`use userdb` // 切换到数据库或创建新数据库

// 现在向集合中插入数据

`user = { username : “firstuser”,password:”firstuser”,email:”firstuser@gmail.com” }` // 准备数据

`db.users.insert(user);` // 将数据插入 things 集合

`show collections;` // 查看 MongoDB 中的所有集合，这里我们应该看到之前创建的 “users” 集合

`db.users.find();` // 查看集合中的所有文档

`db.users.find(0);` // 按索引查找集合

`db.users.find({username:”firstuser”});` // 按 JSON 元素查找集合中的文档

// 使用 JSON 中的游标 -

```javascript
1 var c = db.users.find();
2 while ( c.hasNext() ) printjson( c.next() )
```

// CRUD 操作 -

// 数据插入

`user = { username : “firstuser”,password:”firstuser”,email:”firstuser@gmail.com” }` // 准备数据

// 以下命令可用于带 “_id” 或不带 “_id” 的插入

`db.users.insert(user);` // 将数据插入 things 集合。

// 不带 “_id” 字段插入数据

`db.users.save({username:”thirduser”,password:”thirduser”,email:”thirduser@gmail.com”});`

`db.users.find();` // 确认操作

// 如果未找到 “_id”，则带 “_id” 字段插入数据到集合

`db.users.save({_id:10,username:”fourthuser”,password:”fourthuser”, email:”fourthuser1@gmail.com”});`

// 如果找到 “_id”，则更新集合中的数据

`db.users.save({_id:10,username:”fourthuser1″,password:”fourthuser1″, email:”fourthuser1@gmail.com”});`

// 使用 upsert 标志进行相同操作，即如果找到 “_id” 则更新，否则插入 // 遵循操作 – 如果找到用户名为 “fifthuser” 则更新，否则插入

```
db.users.update({username:"fifthuser"},
{_id:11,username:"fifthuser",password:"fifthuser",
email:"fifthhuser@gmail.com"},{upsert:true});
```

`db.users.find();` // 数据应已插入

```
db.users.update({username:"fifthuser"},
{_id:11,username:"fifthuser1",password:"fifthuser1",
email:"fifthhuser1@gmail.com"},{upsert:true});
```

`db.users.find();` // 数据应已更新

// 从 MongoDB 中选择数据

`db.users.find({username: { $in: [ 10, 11 ] }});` `db.users.find({username: { $in: [ “firstuser”, “seconduser” ] }});`

// 使用 find 操作的查询游标 -

```javascript
1 var myCursor = db.users.find( { username: /.*user.*/ } );
2 myCursor.forEach(printjson);
```

// 更新文档中的字段 // 设置新字段

`db.users.update({ _id: 10 },{$set: { ‘username’: ‘sixthuser’ },});` `db.users.update({ _id: 10 },{$set: { ‘useraddress’: ‘sixthuser address’ },});` `db.users.find();`

// 取消设置文档中的字段

`db.users.update({ _id: 10 },{ $unset: { useraddress: ‘sixthuser address’ } });` `db.users.find();`

// 从集合中删除文档

`db.users.remove( { ‘username’ : ‘fifttuser1′ } );`

参考链接 -

(http://docs.mongodb.org/manual/core/update/)

(http://docs.mongodb.org/manual/core/delete/)

(http://docs.mongodb.org/manual/core/read/)

(http://docs.mongodb.org/manual/core/create/)

## 使用 Angular.js、Node.js 和 MongoDB（MongoJS 模块）的单页应用

本文旨在概念验证，使用基于 JavaScript 的 Web 服务器构建 Web 应用程序。这种技术栈通常被称为 [MEAN Stack](http://blog.mongodb.org/post/49262866911/the-mean-stack-mongodb-expressjs-angularjs-and)。

为了实现这一点，我们选择了 -

1. Angular.js 用于客户端开发 – 单页应用
2. Angular.js 和 Node.js 之间的跨域通信
3. Node.js 用于服务器端开发
4. 使用 express.js 创建基于 REST 的 Web 服务
5. 数据库 – MongoDB
6. Node.js MongoDB 模块扩展（mongojs）

我们创建了一个基于 JavaScript 的 Web 服务器的概念验证，重点在于使用基于 JavaScript 的框架 Node.js 和客户端 Angular.js 处理 NoSQL（MongoDB）。

我们的初始代码可以从[这里](https://github.com/piyasde/NodeMongoDBAngular)下载。

### 架构概览 -

![架构图](img/00009.gif)

架构图

以下是步骤 -

### 安装 -

- A> 从[这里](http://nodejs.org)下载并安装 Node.js。

```
1     命令 – npm install mongojs（需要连接互联网）
```

- B> 要开发应用程序，我们需要为 Node.js 安装 mongojs 模块

```
1     命令 – npm install mongojs（需要连接互联网）
```

- C> 我们需要为 Node.js 安装 express.js

```
1     命令 – npm install express（需要连接互联网）
```

### 配置代码 -

现在，我们将尝试描述代码部分 -

```javascript
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

这里我们根据 Node.js 的概念，在 JavaScript 变量中初始化了 express.js。

```javascript
1 var app = express();
```




这里我们在 `app` 变量中初始化了 Express Web 服务器。

```
1 var databaseUrl = "sampledb"; 
2 var collections = ["things"]
3 var db = require("mongojs").connect(databaseUrl, collections);
```

这里我们使用 Node.js 的 `mongojs` 模块扩展库建立了与 MongoDB 数据库的连接。

```
1 // Config
2 
3 app.configure(function () {
4   app.use(express.bodyParser());
5   app.use(express.methodOverride());
6   app.use(app.router);
7   app.use(express.static(path.join(application_root, "public")));
8   app.use(express.errorHandler({ dumpExceptions: true, showStack: true }));
9 });
```

这里我们完成了与 `express.js` 相关的配置。

### REST 服务代码

```
1 app.get('/api', function (req, res) {
2   res.send('Our Sample API is up...');
3 });
```

这里我们创建了第一个基于 REST 的 Web 服务，并测试了 `express.js` 是否正常运行。

我们的示例 API 将是：`http://127.0.0.1:1212/api`（GET 方法）

```
 1 app.get('/getangularusers', function (req, res) {
 2 	res.header("Access-Control-Allow-Origin", "http://localhost");
 3 	res.header("Access-Control-Allow-Methods", "GET, POST");
 4         // 以上两行是跨域通信所必需的
 5         // （允许作为跨域请求发送的方法）
 6 	db.things.find('', function(err, users) { 
 7 				// 通过 Mongo JS 模块在 MongoDB 中查询
 8 	if( err || !users) console.log("No users found");
 9 	  else 
10 	{
11 		res.writeHead(200, {'Content-Type': 'application/json'}); 
12 						// 通过 json 发送数据
13 		str='[';
14 		users.forEach( function(user) {
15 			str = str + '{ "name" : "' + user.username + '"},' +'\n';
16 		});
17 		str = str.trim();
18 		str = str.substring(0,str.length-1);
19 		str = str + ']';
20 		res.end( str);
21                 // 在此处准备 JSON 数组
22 	}
24   });
25 });
```

这里我们创建了另一个 REST API，用于从用户集合中获取所有用户名，并执行了 `mongojs` 查询。

我们的示例 API 将是：`http://127.0.0.1:1212/getangularusers`（GET 方法）

```
 1 app.post('/insertangularmongouser', function (req, res){
 2   console.log("POST: ");
 3   res.header("Access-Control-Allow-Origin", "http://localhost");
 4   res.header("Access-Control-Allow-Methods", "GET, POST");
 5   // 以上两行是跨域通信所必需的
 6   // （允许作为跨域请求发送的方法）
 7   console.log(req.body);
 8   console.log(req.body.mydata);
 9   var jsonData = JSON.parse(req.body.mydata);
10 
11   db.things.save({email: jsonData.email, password: jsonData.password, 
12 					username: jsonData.username},
13        function(err, saved) { // 通过 Mongo JS 模块在 MongoDB 中查询
14            if( err || !saved ) res.end( "User not saved"); 
15            else res.end( "User saved");
16        });
17 });
```

这里我们创建了一个 POST 请求，通过 REST 调用来创建用户。

我们的示例 API 将是：`http://127.0.0.1:1212/insertangularmongouser`（POST 方法）

```
1 // Launch server
2 app.listen(1212);
```

我们让服务器监听 1212 端口。

现在在命令行中运行 `node appmongodbangular.js`。

### Angular.js 部分

以下是 Angular 控制器中的代码：

```
 1 'use strict';
 2 
 3 var myApp = angular.module('myApp', []); 
 4 // 将 Angular 应用赋值给 JavaScript 变量
 5 
 6 // 以下代码用于允许通过 angular.js 从 Web 服务器发起跨域请求
 7 myApp.config(['$httpProvider', function($httpProvider) {
 8         $httpProvider.defaults.useXDomain = true;
 9         delete $httpProvider.defaults.headers.common['X-Requested-With'];
10     }
11 ]);
12 
13 /* 控制器 */
14 
15 function UserListCtrl($scope, $http, $templateCache) {
16 
17   var method = 'POST';
18   var inserturl = 'http://localhost:1212/insertangularmongouser';
19 		// Node.js 服务器运行的 URL
20   $scope.codeStatus = "";
21   $scope.save = function() {
22     // 从 Angular 模型准备要发送到服务器的 JSON 数据
23     var formData = {
24       'username' : this.username,
25       'password' : this.password,
26 	  'email' : this.email
27     };
28 
29 	this.username = '';
30 	this.password = '';
31 	this.email = '';
32 
33 	var jdata = 'mydata='+JSON.stringify(formData); // 数据必须是字符串
34 
35 	$http({ 
36 		// 使用 Angular $http 服务通过 REST 通信将数据发送到 Node 服务器
37             method: method,
38             url: inserturl,
39             data:  jdata ,
40             headers: {'Content-Type': 'application/x-www-form-urlencoded'},
41             cache: $templateCache
42         }).
43         success(function(response) {
44 		console.log("success"); // 在回调中获取成功响应
45                 $scope.codeStatus = response.data;
46 		console.log($scope.codeStatus);
47 
48         }).
49         error(function(response) {
50 		console.log("error"); // 在回调中获取错误响应
51                 $scope.codeStatus = response || "Request failed";
52 		console.log($scope.codeStatus);
53         });
54 	$scope.list();// 调用 Angular 控制器中的 list 函数
55 		      // 在 HTML 中显示所有当前数据
56         return false;
57   };	
58 
59   $scope.list = function() {
60 	  var url = 'http://localhost:1212/getangularusers';
61 			// Node.js 服务器运行的 URL	
62 	  $http.get(url).success(function(data) {
63 		$scope.users = data;
64 	  });
65           // 使用 Angular $http 服务通过 REST 通信从 Node 服务器获取数据
66   };
67 
68   $scope.list();
69 }
```

### Angular 模板和 HTML

```
1  <html lang="en" ng-app="myApp">
2 .....
```

我们在上述代码中引用了 Angular 应用

```
1 <body ng-controller="UserListCtrl">
2 .....
```

我们在上述代码中引用了 Angular 控制器

```
1 Search: <input ng-model="user">
2 <div class="span10">
3     <!--Body content-->
4     <ul class="users">
5         <li ng-repeat="user in users | filter:user ">
6             {{user.name}}
7         </li>
8     </ul>
9 </div>
```

我们使用了 ng-repeat 标签从 REST 通信中获取用户数据模型，并在 HTML 中显示

```
 1 <form name="myform" id="myform1" ng-submit="save()">
 2     <fieldset>
 3         <legend>New User</legend>
 4             <div class="control-group">
 5                 <center><input type="text" placeholder="User…" 
 6 				ng-model="username" size=50 required/></center>
 7                 <center><input type="text" placeholder="Password…" 
 8 				ng-model="password" size=50 required/></center>
 9                 <center><input type="text" placeholder="Email…" 
10 				ng-model="email" size=50 required/></center>
11             </div>
12     </fieldset>
13     <p>
14          <div><center><button type="submit" >Save now...</button></center></div>
15     </p>
16 </form>
```

我们使用了 ng-submit 标签通过 REST 通信发送 `user` 数据模型，并将其发送到 Node 服务器以保存到 MongoDB。

读者可以在 [GitHub](https://github.com/piyasde/NodeMongoDBAngular) 下载完整的源代码。

## 使用 Highchart.js、Node.js、Express.js 和 MongoDB（Mongo-JS 模块）的 Web 应用

![HighChart](img/00010.jpeg)

HighChart

该应用是另一个概念验证，旨在使用基于 JavaScript 的 Web 服务器构建用于生成图表的 Web 应用。

在本应用中，我们使用了以下工具和技术：

### 1. Node.js 用于服务器端开发

### 2. 使用 express.js 创建基于 REST 的 Web 服务

### 3. 数据库 – MongoDB

### 4. Node.js MongoDB 模块扩展（mongojs）

### 5. Highchart.js 通过异步调用（Ajax）生成图表

### 6. 使用跨域策略从 Node.js 访问 REST 服务到 Ajax 调用

处理基于 JavaScript 框架 Node.js 的 NoSQL（MongoDB）。



我们的初始代码可以从[这里](https://github.com/piyasde/NodeMongoDBHighchart1)下载。

### 架构概览

![架构](img/00011.gif)

架构

以下是步骤——

### 安装

#### A. 从[这里](http://nodejs.org/download/)下载并安装 Node.js。

#### B. 开发应用需要安装 Node.js 的 `mongojs` 模块

```
1     Command – npm install mongojs (should be connected to internet)
```

#### C. 需要安装 Node.js 的 `express.js`

```
1     Command – npm install express (should be connected to internet)
```

## 服务器端应用

### 配置代码

现在，我们来描述代码部分——

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

这里我们根据 Node.js 的概念，在 JavaScript 变量中初始化了 `express.js`。

```
1 var app = express();
```

这里我们在 `app` 变量中初始化了 express 网络服务器。

```
1 var databaseUrl = "faodb"; 
2 var collections = ["seeds"]
3 var db = require("mongojs").connect(databaseUrl, collections);
```

这里我们使用 Node.js 的 `mongojs` 模块扩展库建立了与 MongoDB 数据库的连接。

```
1 // Config
2 
3 app.configure(function () {
4   app.use(express.bodyParser());
5   app.use(express.methodOverride());
6   app.use(app.router);
7   app.use(express.static(path.join(application_root, "public")));
8   app.use(express.errorHandler({ dumpExceptions: true, showStack: true }));
9 });
```

这里我们完成了与 `express.js` 相关的配置。

### REST 服务代码

```
1 app.get('/api', function (req, res) {
2   res.header("Access-Control-Allow-Origin", "*"); // Configuration for Cross-Domain-Policy
3   res.send('Our Sample API is up...');
4 });
```

这里我们创建了第一个基于 REST 的网络服务，并测试了 `express.js` 是否正常运行。

我们的示例 API 将是——`http://127.0.0.1:1212/api`（GET 方法）

```
 1 app.get('/getseeddata/:seedname', function (req, res) {
 2     res.header("Access-Control-Allow-Origin", "*");
 3     seed = req.params.seedname;
 4 	db.seeds.find({seedname:seed}, function(err, seeds) {
 5 	if( err || !seeds) console.log("No seeds found");
 6 	  else 
 7 	{
 8 		res.writeHead(200, {'Content-Type': 'text/json'});
 9 		seedscollection = seeds[0].seedprice;
10 		str = '[';
11 		//console.log(seedscollection);
12 
13 		seedscollection.forEach( function(seed) {
14 		   str = str + '{"month":"'+ seed.mmonth + '","price":"'+ seed.price +'"},';
15 		});
16 		str = str.substring(0,str.length-1)
17 		str = str + ']';
18 		res.end(JSON.stringify(str));
19 	}
20   });
21 });
```

这里我们创建了另一个 REST API，用于从种子集合中获取特定种子的价格信息，并执行了 `mongojs` 查询。

我们的示例 API 将是——`http://127.0.0.1:1212/getseeddata/Arachide`（GET 方法）

现在我们需要在命令 shell 中运行 `node appmongodbhighchart.js` 来启动 Node 服务器。

## 客户端应用

### Highchart 代码说明

```
 1 <script type="text/javascript">
 2     var myAjaxChart;
 3     var mydata = []; // Javascript Array Declaration
 4 $(document).ready(function () { 
 5 
 6 $("#seedselect").change(function() { // On change event of HTML Select Control
 7     mydata = [];
 8     requestData($(this).val()); // Parameterised Function calling for Ajax and Highchart I\
 9 nitiation
10 });
11 
12 function requestData(data) {
13 $.ajax({
14     url: 'http://localhost:1212/getseeddata/'+data, // Node.js Server REST Call
15     type: "GET",
16     dataType: "json",
17     success: function(seed) {
18         var jsonobj = seed;
19         var obj = jQuery.parseJSON(jsonobj);
20         for(i=0;i<obj.length;i++)
21         {
22             mydata.push(parseInt(obj[i].price)); // Filling of Array after Ajax Call
23         }
24         // Initialising the Highchart Object within the success callback
25         //Chart
26         var options ={
27             chart: {
28             renderTo: 'container', // Initialising the DIV with Highchart Object
29             type: 'line',
30             marginRight: 130,
31             marginBottom: 25,
32          },
33          // Other Highchart Properties
34          title: {
35            text: 'Price Data',
36            x: -20 //center
37          },
38          xAxis: {
39          },
40          yAxis: {
41               title: {
42               text: 'Price (Rs)'
43          },
44          plotLines: [{
45               value: 0,
46               width: 1,
47               color: '#808080'
48         }]
49      },
50      tooltip: {
51              valueSuffix: 'Rs'
52      },
53      legend: {
54            layout: 'vertical',
55            align: 'right',
56            verticalAlign: 'top',
57            x: -10,
58            y: 100,
59            borderWidth: 0
60       }
61       ,
62       series: [{
63            name: 'Price',
64            data: mydata  // Here the previously populated javascript array will be initial\
65 ised in data parameter
66       }],
67      };
68      var chardata = new Highcharts.Chart(options);
69    },
70    cache: false
71   });
72  }
73 });
```

## 使用 Angular.js、Node.js 和 Socket.io 实现实时数据更新

本文是一个概念验证，旨在使用基于 JavaScript 的网络服务器配合 `Socket.IO`、Angular.js 和 Node.js 构建实时网络应用。我们模拟了一个场景，包含 4 种产品及其最佳买入价、最佳卖出价和最后成交价。

![示意图](img/00012.jpeg)

为了实现这一目标，我们选择了——

### 1> Angular.js 用于客户端开发——应用前端

### 2> Node.js 用于服务器端开发

### 3> Socket.IO 用于服务器与客户端通信

### 4> Node.js 的 Socket.IO 模块扩展

我们创建了一个基于 JavaScript 的网络服务器 Node.js 的概念验证，重点在于使用 `Socket.IO` 处理实时应用，并在客户端使用 Angular.js。

### 架构概览

![Angular.js NodeJS SocketIO](img/00013.jpeg)

Angular.js NodeJS SocketIO

以下是步骤——

### 安装

A. 从[这里](http://nodejs.org/download/)下载并安装 `Node.js`。

B. 开发应用需要安装 Node.js 的 `socket.io` 模块 命令——`npm install socket.io`（需连接互联网）

### 配置代码

现在，我们来描述代码部分——

```
1     var http = require('http');
2     var url = require('url');
3     var fs = require('fs');
4     
5     // use socket.io
6     var io = require('socket.io').listen(server);
```

这里我们根据 Node.js 的概念，在 JavaScript 变量中初始化了 `http`、`url` 和 `filesystem` 对象。同时，我们在 Node.js 环境中初始化了 `socket.io` 变量。

```
 1     server = http.createServer(function(req, res){ // Server creation
 2     ....
 3     case '/angulartableRT.html':
 4                 fs.readFile(__dirname + path, function(err, data){
 5                     if (err){ 
 6                         return send404(res);
 7                     }
 8                     res.writeHead(200, {'Content-Type': path == 'json.js' ? 
 9 					'text/javascript' : 'text/html'});
10                     res.write(data, 'utf8');
11                     res.end();
12                 });	
13     ....
14     server.listen(8001);
15     ....
```




在上述代码中，我们展示了 Node 应用的一些重要部分。第一部分，我们通过 `http.createServer` 编写了服务器的创建。接着，我们允许客户端浏览器从 Node.js 服务器访问资源——`angulartableRT.html`。现在服务器正在监听 8001 端口。读者可以在本章末尾链接的 GITHUB 中获取完整代码。现在最重要的是——`socket.io 与 Node.js 的通信`。我们在下方注释了 Node.js 的 socket.io 特定代码。

```
 1     // define interactions with client
 2     io.sockets.on('connection', function(socket){ 
 3         //send data to client
 4         setInterval(function(){
 5     
 6     		for(i=0;i<serverjson.length;i++) 
 7 		// A simulation of data from server instead of database calling
 8     		{
 9     			serverjson[i].BBP = Math.round((parseInt(serverjson[i].BBP) 
10 						+ Math.random())*100)/100;
11     			serverjson[i].BSP = Math.round((parseInt(serverjson[i].BSP) 
12 						+ Math.random())*100)/100;
13     			serverjson[i].LTP = Math.round((parseInt(serverjson[i].LTP) 
14 						+ Math.random())*100)/100;
15     		}
16     
17     		var serverjsonstr = JSON.stringify(serverjson);
18     
19     		socket.emit('msg', {'msg': serverjsonstr}); // Emitting Messages from Server
20     		socket.emit('msgWrite', msgWrite);
21         }, 1000);
22     
23     });
```

现在在命令行中运行 `node server.js`。这是我们的 Node.js 特定代码文件。我们的示例应用将运行在——

[`localhost:8001/`](http://127.0.0.1:1212/getallusers)

### Angular.js 部分

以下是 Angular 控制器中的代码，并讨论了与 Socket 相关的代码。

```
 1     /* Controllers */
 2     app.controller('StockListCtrl', function($scope, socket) { 
 3       $scope.stocks = [];
 4       socket.on('msg', function(data) { **// Listening in Socket in Angular Controller**
 5     		$scope.stocks = JSON.parse(data.msg);
 6     
 7     	});
 8     
 9     });
10     
11     //Getting value from server data change event
12     app.factory('socket', function($rootScope) {
13     	var socket = io.connect(); // Connection to the server socket
14     	return {
15     		on: function(eventName, callback) { 
16 			// Return callback to the actual function to manipulate it.
17     			socket.on(eventName, function() { 
18     				var args = arguments;   
19     				$rootScope.$apply(function() {
20     					callback.apply(socket, args);
21     				});
22     			});
23     		}
24     	};
25     });
```

### Angular HTML 绑定

```
1      <script src="http://localhost:8001/socket.io/socket.io.js"></script> 
2      // Important to know
3      // **Access socket.io.js from Angular.js** 
4     .....
```

以下是 Angular HTML 与控制器的动态绑定——

```
 1     <body ng-controller="StockListCtrl">
 2          <div>
 3               <table class="table">
 4                     ...
 5                   <tbody>
 6                        <tr ng-repeat="stock in stocks"> 
 7 			   <!-- Dynamic Binding of Angular Template with Data -->
 8                            <td>{{stock.Product}}</td>
 9                            <td>{{stock.BBP}}</td>
10                            <td>{{stock.BSP}}</td>
11                            <td>{{stock.LTP}}</td>
12                        </tr>
13                   </tbody>
14               </table>
15          </div>
16     </body>
```

读者可以在 [GitHub](https://github.com/piyasde/NodeSocketIO) 下载完整源代码。

## 使用 Angular.js、Node.js 和 CouchDB（Cradle 模块）构建单页应用

本文旨在概念验证，使用基于 JavaScript 的 Web 服务器配合 CouchDB、Angular.js 和 Node.js 构建 Web 应用。

这次我们尝试了 CouchDB，根据 [Apache CouchDB](http://couchdb.apache.org/) 网站的定义——

> Apache CouchDB™ 是一种数据库，它使用 JSON 作为文档格式，JavaScript 用于 MapReduce 查询，并通过常规 HTTP 提供 API。

为了实现这一目标，我们选择了——

1. Angular.js 用于客户端开发——单页应用
2. Angular.js 与 Node.js 之间的跨域通信
3. Node.js 用于服务器端开发
4. 使用 express.js 创建基于 REST 的 Web 服务
5. 数据库——CouchDB
6. Node.js Cradle 模块扩展（用于与 CouchDB 通信）
7. 使用 Map-Reduce 创建 CouchDB 视图以获取数据

我们创建了一个基于 JavaScript 的 Web 服务器的概念验证，重点在于使用基于 JavaScript 的框架 Node.js 和客户端 Angular.js 处理 NoSQL（CouchDB）。

我们的初始代码可以 [在此处](https://github.com/piyasde/NodeCouchDBAngular) 下载。

### 架构概览

![架构图](img/00014.gif)

架构图

以下是步骤——

### 安装

A. 从 [此处](http://nodejs.org/download/) 下载并安装 Node.js。

B. 开发应用需要安装 Node.js 的 mongojs 模块

命令 – `npm install cradle`（需要连接互联网）

C. 需要安装 Node.js 的 express.js

命令 – `npm install express`（需要连接互联网）

### 配置代码

现在，我们将尝试描述代码部分——

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

这里我们根据 Node.js 的概念，在 JavaScript 变量中初始化了 express.js。

```
1 var app = express();
```

这里我们在 app 变量中初始化了 express Web 服务器。

```
1 var databaseUrl = "sampledb";
2 var cradle = require('cradle');
3 var connection = new(cradle.Connection)('http://couchadmin:couchadmin@localhost', 5984, {
4 auth: { username: 'couchadmin', password: 'couchadmin' }
5 });
6 var db = connection.database(databaseUrl);
```

这里我们使用 Node.js 的 mongojs 模块扩展库建立了与 mongodb 数据库的连接。

```
1 // Config
2 
3 app.configure(function () {
4   app.use(express.bodyParser());
5   app.use(express.methodOverride());
6   app.use(app.router);
7   app.use(express.static(path.join(application_root, "public")));
8   app.use(express.errorHandler({ dumpExceptions: true, showStack: true }));
9 });
```

这里我们进行了与 express.js 相关的配置。

### REST 服务代码

```
1 app.get('/api', function (req, res) {
2   res.header("Access-Control-Allow-Origin", "http://localhost");
3   res.send('Our Sample API is up...');
4 });
```

这里我们创建了第一个基于 REST 的 Web 服务，并测试 express.js 是否正常运行。

我们的示例 API 将是——http://127.0.0.1:1212/api（GET 方法）

```
 1 app.get('/getangularusers', function (req, res) {
 2 	res.header("Access-Control-Allow-Origin", "http://localhost");
 3 	res.header("Access-Control-Allow-Methods", "GET, POST");
 4         // The above 2 lines are required for Cross Domain Communication(Allowing the meth\
 5 ods            
 6         // that come as Cross Domain Request
 7         res.writeHead(200, {'Content-Type': 'application/json'});
 8         str='[';
 9         db.view('characters/all', function (err, response) { //Query in CouchDB View
10              response.forEach(function (row) {
11              str = str + '{ "name" : "' + row.username + '"},' +'\n';
12         });
13         str = str.trim();
14         str = str.substring(0,str.length-1);
15         str = str + ']';
16         res.end( str);
17       });
18 });
```

这里我们创建了另一个 REST API，用于从用户集合中获取所有用户名，并执行了查询。

### CouchDB 视图创建

在运行 Angular 客户端应用以从 CouchDB 获取特定数据集之前，需要执行此视图创建。

另外请注意，要运行此视图创建，我们应该设置——

`[httpd]` `authentication_handlers = {couch_httpd_auth, null_authentication_handler}`





在`<<CouchDB Installation folder>>/etc/couchdb`文件夹的`local.ini`文件中，无需管理员身份即可执行此映射函数。

此特定功能我们花了一些时间才发现。

```
 1 app.get('/createview', function (req, res) { // Before running the Angular Application, th\
 2 e view must be created
 3 	db.save('_design/characters', { // Main View Family Name
 4       all: { // A particular set of data selection by javascript map-reduce
 5           map: function (doc) {
 6               if (doc.username) emit(doc.username, doc); // specific code to execute map f\
 7 unction on each document
 8           }
 9       }
10    });
11 });
```

我们的示例 API 为：`http://127.0.0.1:1212/getangularusers`（GET 方法）

```
 1 app.post('/insertangularcouchuser', function (req, res){
 2   console.log("POST: ");
 3   res.header("Access-Control-Allow-Origin", "http://localhost");
 4   res.header("Access-Control-Allow-Methods", "GET, POST");
 5   // The above 2 lines are required for Cross Domain Communication(Allowing the methods th\
 6 at come as Cross 
 7   // Domain Request
 8   console.log(req.body);
 9   console.log(req.body.mydata);
10   var jsonData = JSON.parse(req.body.mydata);
11   var doc = {email: jsonData.email, password: jsonData.password, username: jsonData.userna\
12 me};
13   db.save('\''+Math.random()+'\'', doc, function (err, res) {
14       if (err) {
15           // Handle error
16           res += ' SAVE ERROR: Could not save record!!\n';
17       } else {
18           // Handle success
19           res += ' SUCESSFUL SAVE\n';
20       }
21    });
22 });
```

这里我们通过 REST 调用发送了一个 POST 请求来创建用户。

我们的示例 API 为：`http://127.0.0.1:1212/insertangularcouchuser`（POST 方法）

```
1 // Launch server
2 app.listen(1212);
```

我们让服务器监听 1212 端口。

现在在命令行中运行`node appcouchdbangular.js`。这是我们的 Node.js 特定代码文件。

参考资料：

1. http://wiki.apache.org/couchdb/Setting_up_an_Admin_account
2. http://guide.couchdb.org/draft/security.html
3. https://github.com/cloudhead/cradle

### Angular.js 部分 -

以下是 Angular 控制器中的代码：

```
 1 'use strict';
 2 
 3 var myApp = angular.module('myApp', []); // Taking Angular Application in Javascript Varia\
 4 ble
 5 
 6 // Below is the code to allow cross domain request from web server through angular.js
 7 myApp.config(['$httpProvider', function($httpProvider) {
 8         $httpProvider.defaults.useXDomain = true;
 9         delete $httpProvider.defaults.headers.common['X-Requested-With'];
10     }
11 ]);
12 
13 /* Controllers */
14 
15 function UserListCtrl($scope, $http, $templateCache) {
16 
17   var method = 'POST';
18   var inserturl = 'http://localhost:1212/insertangularcouchuser';// URL where the Node.js \
19 server is running
20   $scope.codeStatus = "";
21   $scope.save = function() {
22     // Preparing the Json Data from the Angular Model to send in the Server. 
23     var formData = {
24       'username' : this.username,
25       'password' : this.password,
26 	  'email' : this.email
27     };
28 
29 	this.username = '';
30 	this.password = '';
31 	this.email = '';
32 
33 	var jdata = 'mydata='+JSON.stringify(formData); // The data is to be string.
34 
35 	$http({ // Accessing the Angular $http Service to send data via REST Communication to Nod\
36 e Server.
37             method: method,
38             url: inserturl,
39             data:  jdata ,
40             headers: {'Content-Type': 'application/x-www-form-urlencoded'},
41             cache: $templateCache
42         }).
43         success(function(response) {
44 		console.log("success"); // Getting Success Response in Callback
45                 $scope.codeStatus = response.data;
46 		console.log($scope.codeStatus);
47 
48         }).
49         error(function(response) {
50 		console.log("error"); // Getting Error Response in Callback
51                 $scope.codeStatus = response || "Request failed";
52 		console.log($scope.codeStatus);
53         });
54 	$scope.list();// Calling the list function in Angular Controller to show all current data\
55  in HTML
56         return false;
57   };	
58 
59   $scope.list = function() {
60 	  var url = 'http://localhost:1212/getangularusers';// URL where the Node.js server is ru\
61 nning	
62 	  $http.get(url).success(function(data) {
63 		$scope.users = data;
64 	  });
65           // Accessing the Angular $http Service to get data via REST Communication from N\
66 ode Server 
67   };
68 
69   $scope.list();
70 }
```

### Angular 模板和 HTML

```
1 <html lang="en" ng-app="myApp">
2 .....
```

我们在上面的代码中引用了 Angular 应用。

```
1 <body ng-controller="UserListCtrl">
2 .....
```

我们在上面的代码中引用了 Angular 控制器。

```
1 Search: <input ng-model="user">
2 <div class="span10">
3     <!--Body content-->
4     <ul class="users">
5         <li ng-repeat="user in users | filter:user ">
6             {{user.name}}
7         </li>
8     </ul>
9 </div>
```

我们使用了`ng-repeat`标签从 REST 通信中获取用户数据模型并显示在 HTML 中。

```
 1 <form name="myform" id="myform1" ng-submit="save()">
 2     <fieldset>
 3         <legend>New User</legend>
 4             <div class="control-group">
 5                 <center><input type="text" placeholder="User…" ng-model="username" size=50\
 6  required/></center>
 7                 <center><input type="text" placeholder="Password…" ng-model="password" siz\
 8 e=50 required/></center>
 9                 <center><input type="text" placeholder="Email…" ng-model="email" size=50 r\
10 equired/></center>
11             </div>
12     </fieldset>
13     <p>
14          <div><center><button type="submit" >Save now...</button></center></div>
15     </p>
16 </form>
```

我们使用了`ng-submit`标签通过 REST 通信发送用户数据模型，并发送到 Node 服务器以保存到 CouchDB。

读者可以在 [GitHub](https://github.com/piyasde/NodeCouchDBAngular) 下载完整的源代码。

## 使用 Google DART、Node.js 和 MongoDB 处理 POST 请求

本章介绍如何使用 DART 和 MongoDB 处理 GET 和 POST 请求。我们尝试使用基于 JavaScript 的 Web 服务器 Node.js 创建一个概念验证，重点在于使用基于 JavaScript 的框架 Node.js 和客户端 Google DART 处理 NoSQL（MongoDB）。

为了实现这一点，我们选择了：

1. DART 用于客户端开发
2. DART 与 Node.js 之间的跨域通信
3. Node.js 用于服务器端开发
4. 使用 express.js 创建基于 REST 的 Web 服务
5. 数据库 – MongoDB
6. Node.js MongoDB 模块扩展（mongojs）

代码可以在 [Github](https://github.com/piyasde/NodeMongoDBDART) 找到。

![Architecture at a glance](img/00015.gif)

架构概览

以下是步骤：

### 安装 -

从 [这里](http://nodejs.org/download) 下载并安装 Node.js。

B> 要开发此应用，我们需要为 Node.js 安装 mongojs 模块。

命令 – `npm install mongojs`（需要连接互联网）

我们需要为 Node.js 安装 express.js。

命令 – `npm install express`（需要连接互联网）

### 配置代码 -

现在，我们将描述代码部分：

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

这里我们根据 Node.js 的概念在 JavaScript 变量中初始化了 express.js。

```
1 var app = express();
```

这里我们在`app`变量中初始化了 express Web 服务器。

```
1 var databaseUrl = "sampledb"; 
2 var collections = ["things"]
3 var db = require("mongojs").connect(databaseUrl, collections);
```

这里我们使用 Node.js 的 mongojs 模块扩展库建立了与 MongoDB 数据库的连接。





```
1 // Config
2 
3 app.configure(function () {
4   app.use(express.bodyParser());
5   app.use(express.methodOverride());
6   app.use(app.router);
7   app.use(express.static(path.join(application_root, "public")));
8   app.use(express.errorHandler({ dumpExceptions: true, showStack: true }));
9 });
```

这里我们进行了与 express.js 相关的配置。

### REST 服务代码 -

```
1 app.get('/api', function (req, res) {
2   res.send('Our Sample API is up...');
3 });
```

这里我们创建了第一个基于 REST 的 Web 服务，并测试了 express.js 是否正常运行。

我们的示例 API 将是 - [`127.0.0.1:1212/api`](http://127.0.0.1:1212/getallusers) (GET 方法)

```
 1 app.get('/getdartusers', function (req, res) {
 2 	res.header("Access-Control-Allow-Origin", "http://127.0.0.1:3030");
 3 	res.header("Access-Control-Allow-Methods", "GET, POST");
 4         // The above 2 lines are required for Cross Domain Communication
 5         // (Allowing the methods that come as Cross Domain Request
 6 	db.things.find('', function(err, users) { // Query in MongoDB via Mongo JS Module
 7 	if( err || !users) console.log("No users found");
 8 	  else 
 9 	{
10 		res.writeHead(200, {'Content-Type': 'application/json'}); // Sending data via json
11 		str='[';
12 		users.forEach( function(user) {
13 			str = str + '{ "name" : "' + user.username + '"},' +'\n';
14 		});
15 		str = str.trim();
16 		str = str.substring(0,str.length-1);
17 		str = str + ']';
18 		res.end( str);
19                 **// Prepared the jSon Array here**
20 	}
21   });
22 });
```

这里我们创建了另一个 REST API，用于从用户集合中获取所有用户名，并执行了 mongojs 查询。

我们的示例 API 将是 - [`127.0.0.1:1212/getangularusers`](http://127.0.0.1:1212/getallusers) (GET 方法)

### 处理 POST 请求

我们看到请求以两部分形式到达服务器——一部分是 **HTTP OPTIONS** 方法，另一部分是 **HTTP POST** 方法。

这些的代码如下所示 -

```
 1 app.all('/insertdartmongouser', function(req, res, next) {
 2 
 3   if (req.method === 'OPTIONS') {
 4       console.log('!OPTIONS');
 5 
 6       var headers = {}; // Header values inclusion - OPTIONS handling
 7       // IE8 does not allow domains to be specified, just the *
 8       headers["Access-Control-Allow-Origin"] = "*";
 9       headers["Access-Control-Allow-Methods"] = "POST, GET, PUT, DELETE, OPTIONS";
10       headers["Access-Control-Allow-Credentials"] = false;
11       headers["Access-Control-Max-Age"] = '86400'; // 24 hours
12       headers["Access-Control-Allow-Headers"] = "X-Requested-With, X-HTTP-Method-Override,\
13  Content-Type, Accept";
14       res.writeHead(200, headers);
15       res.end();
16   } else {
17 	next(); // If the http request method is not 'OPTIONS' then go to next handling - which i\
18 s 'POST' here.
19   }
20 });
```

以及 node.js 中的 POST 方法代码 -

```
 1 app.post('/insertdartmongouser', function (req, res){
 2     console.log("POST: ");
 3     res.header("Access-Control-Allow-Origin", "*");
 4     res.header("Access-Control-Allow-Methods", "GET,POST,OPTIONS");
 5     console.log("got method"+req.method);
 6     var alldata = '';
 7     req.on('data', function(chunk) { **// Getting the body information in node.js 
 8 				       // request 'on data arrive' condition**
 9 	console.log("Received body data:"); **// this is an asynchronous event in node.js post**
10 	console.log(chunk.toString());
11 	alldata = chunk.toString();
12 	var jsonData = JSON.parse(alldata);
13 	console.log(jsonData.username);
14 	console.log(jsonData.password);
15 	console.log(jsonData.email);
16 	db.things.save({email: jsonData.email, password: jsonData.password, username: jsonData.us\
17 ername}, 
18 	function(err, saved) {  // Calling the function
19 	    if( err || !saved ) res.end( "User not saved"); 
20 	    else res.end( "User saved");
21 	});
22    });
23 });
```

这里我们通过 REST 调用创建了一个 POST 请求来创建用户。

我们的示例 API 将是 – http://127.0.0.1:1212/insertdartmongouser (POST 方法)

```
1 // Launch server
2 app.listen(1212);
```

我们让服务器监听 1212 端口。

现在在命令行中运行 `node appmongodbdart.js`。

### DART 部分 -

以下是 DART 源代码中的代码 -

```
 1 // Importing Core DART libraries
 2 
 3 import 'dart:html';
 4 import 'dart:json' as json;
 5 import 'package:web_ui/web_ui.dart';
 6 
 7 var wordList; // Variables in DART
 8 
 9 var saveUser;
10 var httpPostRequest;
11 @observable String serverResponse = '';
12 
13 void main() { // Main Entrypoint of the Program
14     wordList = query('#userList');  // Assigning variable to 'wordlist' DOM Element
15     query('#getUsers').onClick.listen(makeRequest); 
16 	// Register 'makeRequest' to an event listener
17     query('#saveUser').onClick.listen(makePostRequest);
18 }
19 
20 **// A get Request**
21 
22 void makeRequest(Event e) {
23     var path = 'http://127.0.0.1:1212/getdartusers'; 
24 	// Asynchronous request path (Cross Domain Request)
25     var httpRequest = new HttpRequest();
26     httpRequest
27         ..open('GET', path)
28         ..onLoadEnd.listen((e) => requestComplete(httpRequest))
29         ..send(''); // Preparing the http request and send to server
30 }
31 
32 **//A post request**
33 
34 void makePostRequest(Event e) {
35   //var path = 'sample.json';
36   e.preventDefault();
37   print ('post request');
38   var path1 = 'http://127.0.0.1:1212/insertdartmongouser';// URL for the REST Calling
39   httpPostRequest = new HttpRequest();
40   httpPostRequest.onReadyStateChange.listen(onData(e)); 
41 
42   httpPostRequest.open('POST', path1);
43   httpPostRequest.send(userJsonData());
44 }
45 
46 String userJsonData() {
47   // Put date in the map.
48   print ('userJsonData');
49 
50   var usernm = query('#usernameid');
51   var passwd = query('#passwordid');
52   var eml = query('#emailid');
53 
54   theData['username'] = usernm.value;
55   theData['password'] = passwd.value;
56   theData['email'] = eml.value;
57   usernm.value='';
58   passwd.value='';
59   eml.value='';
60   print("mydata="+json.stringify(theData));
61   return json.stringify(theData);
62 }
63 
64 void onData(Event e) {
65   print ('onData');
66 
67   if (httpPostRequest.readyState == HttpRequest.DONE && httpPostRequest.status == 200) {
68       // Data saved OK.
69       serverResponse = httpPostRequest.responseText;
70       print (serverResponse);
71   } else if (httpPostRequest.readyState == HttpRequest.DONE &&
72       httpPostRequest.status == 0) {
73       // Status is 0...most likely the server isn't running.
74       serverResponse = 'No server';
75       print (serverResponse);
76   }
77 }
78 
79 requestComplete(HttpRequest request) {
80     print(request.status);
81     print(request.statusText);
82 
83     if (request.status == 200) {
84         List samples = json.parse(request.responseText); // Parsing JSON and put in DART L\
85 ist
86         wordList.children.clear();
87         for (int i = 0; i < samples.length; i++) {
88             var myObject = samples[i];
89             wordList.children.add(new LIElement()..text = myObject['name']); // Adding dat\
90 a to DOM Element
91            }
92      } else {
93            wordList.children.add(new LIElement()..text =
94                'Request failed, status={$request.status}');
95      }
96 }
```

编写此解决方案非常有用的参考资料 -

https://gist.github.com/nilcolor/816580

http://stackoverflow.com/questions/17689986/jquery-ajax-sending-both-options-and-post-how-to-handle-with-express-js-node-j

http://blog.frankgrimm.net/2010/11/howto-access-http-message-body-post-data-in-node-js/

### DART 代码参考和 HTML





```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>用户</title>
        <link rel="stylesheet" href="<<css file reference>>">
    </head>
    <body>
         <h1>所有用户</h1>
         <button id="getUsers">获取用户</button>
         <div>
              <ul id="userList">
              </ul>
         </div>
         <div>
             <h1>输入用户：</h1>
             <form name="dartform" id="dartform" method="POST" 
					action="http://127.0.0.1:1212/insertdartmongouser">
                  名称：<input type="text" name ="username" id="usernameid" value="" />
                  密码：<input type="text" name ="password" id="passwordid" value="" \
/>
                  邮箱：<input type="text" name ="email" id="emailid" value="" />
                  <button id="saveUser" >保存</button>
             </form>
         </div>
         <script type="application/dart" src="users.dart"></script> <!--Dart 文件引用 \
-->
         <!-- 要使下一行生效，pubspec.yaml 文件中必须依赖 'browser' -->
         <script src="packages/browser/dart.js"></script>
    </body>
</html>
```

我们使用了 Dart 异步代码，通过 REST 通信发送用户数据模型，并发送到 Node 服务器以从 MongoDB 获取数据。

读者可以在 [GitHub](https://github.com/piyasde/NodeMongoDBDART) 下载完整的源代码。

## 使用 Should.js 进行 Node.js 单元测试

should.js 是 Node.js 单元测试的 JavaScript 库之一。在机器上安装 Node.js 后，我们需要通过 npm（Node 包管理器）安装 should.js。

要安装 should.js，需要在终端中运行：

`npm install should`

要在任何给定的 JavaScript 文件中启用 should.js，我们需要包含：

`require('should');`

以下是一些单行测试：

布尔变量功能测试：

```javascript
true.should.be.ok;

false.should.not.be.ok;

true.should.be.true;

'1'.should.not.be.true;

false.should.be.false;

''.should.not.be.false;
```

检查数组功能：

```javascript
[].should.be.empty; // 数组为空

[1,2,3].should.eql([1,2,3]); // 数组包含与预期相同的值

[1, 2, 3].should.have.length(3); // 数组长度检查

[1,2,3].should.containEql(1); // 数组包含预期值

[].should.be.an.instanceOf(Array); // 数组实例
```

检查一些字符串功能：

```javascript
''.should.be.empty; // 空字符串

'foobar'.should.endWith('bar'); // 字符串以预期字符串结尾

'foobar'.should.not.endWith('foo'); // 字符串不应以预期字符串结尾

'test'.should.equal('test'); // 字符串相等性检查
```

检查一些数字功能：

```javascript
(4).should.equal(4);

(10).should.be.above(5);

(15).should.be.within(10, 15);

(10).should.not.be.below(5);
```

Undefined 和 Infinity 检查：

```javascript
(undefined + 0).should.be.NaN;

(1/0).should.be.Infinity;
```

JSON 功能检查：

```javascript
({ foo: 'bar' }).should.eql({ foo: 'bar' }); // JSON 相等性检查

({}).should.be.an.Object; // 一个对象

var jsonVar = {a:1, b:2}; 

jsonVar.should.have.property('a'); // JSON 属性检查

var obj = { foo: 'bar', baz: 'raz' }; 

(obj).should.containEql({ foo: 'bar', baz: 'raz' }); // JSON 包含预期值

obj.should.have.keys('foo', 'baz'); // JSON 包含这些键

obj.should.have.keys(['foo', 'baz']);
```

函数应抛出错误：

```javascript
(function(){
  throw new Error('fail');
}).should.throw();

var user = {
    name: 'tj'
};

user.should.have.property('name', 'tj');
```

要使用 'Describe' 独立测试功能，我们需要安装自动测试运行器。这里 `mocha` 是一个自动测试运行器，它将运行测试并在控制台中显示结果。

现在我们需要安装 mocha：

`npm install -g mocha`

现在用于测试的函数：

```javascript
function sumTwoNumbers(firstNum,secondNum)
{
	return (parseInt(firstNum) + parseInt(secondNum));
}
```

要测试这个函数，我们需要运行：

`mocha ourfilename.js`

这里 `ourfilename.js` 应该是测试用例文件的名称。

## 使用 Backbone.js 开发 Java REST Web 应用程序

最近在我们的基于 J2ee 的 Web 应用程序开发中，我们探索了 JavaScript MVC 框架来开发结构化的用户界面开发。在 JavaScript 框架中，我们找到了足够的 Backbone.js 文档，用于开发基于 J2ee 应用程序后端的示例概念验证。

我们撰写这篇文章是因为我们在网络上没有找到使用 backbone.js 作为 UI 开发工具的完整 Java Web 应用程序。在开发 POC 的过程中，我们修改了 backbone.js 部分的代码。

我们从 *Backbone.js Wine Cellar 教程 — 第 2 部分：CRUD*（作者 **Christophe Coenraets**）中学习了相关知识，并使用他的示例 POC 开发了一个以 Backbone.js 作为 Web 层开发框架的 J2ee Web 应用程序。主要应用程序的功劳归功于他。

我们已将示例应用程序上传到 GitHub（这里是链接）。

以下是整个项目的基本理解：

J2ee 项目基于 Java Jersey REST 框架。数据库模式附在项目源代码中，文件名为 `cellar.sql`。

**开发环境：**

1.  数据库 – MySql
2.  基于 REST 的 Web 服务开发 – Java Jersey。
3.  UI 开发 – Backbone.js

**部署环境：**

1.  Apache Tomcat 7（我们已在其上测试过。）

下面我们将尝试给出服务器端开发和客户端开发的概念和代码片段。

### 服务器端 -

A. `ConnectionHelper.java` – 用于与 MySql 数据库建立连接。

B. `Wine.java` – 用作数据库中表的简单 POJO 类。

C. `WineDAO.java` – 用于编写与 MySql 表中插入/更新/删除/选择相关的 JDBC 代码。所有数据库操作方法都写在这里。

D. `WineResource.java` – 与基于 REST API 的 Web 服务相关的重要类。方法签名如下：

```java
@GET @Path("wines")
@Produces(MediaType.APPLICATION_JSON) 
public List findAll() {

    // 从数据库获取所有数据

}


@GET @Path("search/{query}")
@Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
public List<Wine> findByName(@PathParam("query") String query) {
   // 根据产品名称从数据库获取特定数据


}
@GET 
@GET @Path("{id}")
@Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
public Wine findById(@PathParam("id") String id) {
	// 根据 ID 从数据库获取特定数据
}


@POST
@Consumes({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML})
@Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
public Wine create(Wine wine) {
       // 使用简单 POJO Wine 将数据插入数据库
}


@PUT @Path("{id}")
@Consumes({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML})
@Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
public Wine update(Wine wine) {
	// 使用特定 ID 更新数据	
}


@DELETE @Path("{id}")
@Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
public void remove(@PathParam("id") int id) {
	// 删除具有选定 ID 的特定记录
}
```

所有基于 REST 的 API 都可以使用类 `Test.java` 进行测试：

此处测试的特定行：

```java
System.out.println(service.path("rest").path("wines").accept(MediaType.APPLICATION_JSON).get(String.class));
```

现在简单解释一下如何对基于 Jersey 的 REST Web 服务进行测试：




我们可以进一步深入查看 `web.xml` 中的以下行：

`<init-param> <param-name>com.sun.jersey.config.property.packages</param-name> <param-value>org.webphlox.brandserver.sample</param-value> </init-param>`

*   用于让 Java Jersey 服务器扫描基于 REST 的 Web 服务资源所在的包。

```
1 <servlet-mapping>
2    <servlet-name>Jersey REST Service</servlet-name>
3    <url-pattern>/rest/*</url-pattern>
4 </servlet-mapping>
```

*   用于标识基于 REST 的 Web 服务的路径，此处为 `/rest/`。

因此，在上述测试方法中，

`service.path("rest")`

对应的是 url-pattern，

而 `.path("wines")` 用于获取特定的方法。同时，它将以 json 格式输出结果。

### 客户端部分 -

HTML 部分 -

在客户端，`index.html` 用于 backbone.js 模板 -

```
1 <script type="text/template" id="tpl-header">
2    <button class="new">New Wine</button>
3 </script>
```

*   这里的按钮用于添加新数据。

```
1 <script type="text/template" id="tpl-wine-list-item">
2    <a href='#wines/<%= id %>'><%= name %></a>
3 <!-- <%= id %> 和 <%= name %> 用作模板变量。
4 </script>
```

*   用于以表格形式显示数据列表。

```
 1 <script type="text/template" id="tpl-wine-details">
 2 <div class="form-left-col">
 3 <label>Id:</label>
 4 <input type="text" id="wineId" name="id" value="<%= id %>" disabled />
 5 <label>Name:</label>
 6 <input type="text" id="name" name="name" value="<%= name %>" required/>
 7 <label>Grapes:</label>
 8 <input type="text" id="grapes" name="grapes" value="<%= grapes %>"/>
 9 <label>Country:</label>
10 <input type="text" id="country" name="country" value="<%= country %>"/>
11 <label>Region:</label>
12 <input type="text" id="region" name="region" value="<%= region %>"/>
13 <label>Year:</label>
14 <input type="text" id="year" name="year" value="<%= year %>"/>
15 <button class="save">Save</button>
16 <button class="delete">Delete</button>
17 </div>
18 
19 <div class="form-right-col">
20 <img height="300" src="pics/<%= picture %>"/>
21 <label>Notes:</label>
22 <textarea id="description" name="description"><%= description %></textarea>
23 </div>
24 
25 </script>
```

*   用于显示特定数据项的详细信息。

### Javascript 部分 (Backbone.js)

所有与 javascript 相关的代码都可以在 `main.js` 中找到。

首先，我们需要定义由 backbone javascript 处理的数据模型（Model）。

```
 1 // Models 
 2 
 3 window.Wine = Backbone.Model.extend({
 4 urlRoot:"http://localhost:8080/brandserver/rest/wines",
 5 defaults:{
 6 "id":null,
 7 "name":"",
 8 "grapes":"",
 9 "country":"USA",
10 "region":"California",
11 "year":"",
12 "description":"",
13 "picture":""
14 }
15 });
16 
17 window.WineCollection = Backbone.Collection.extend({
18 model:Wine,
19 url:"http://localhost:8080/brandserver/rest/wines"
20 });
```

`urlRoot` 是基于 REST 的 Web 服务调用点（端点）。这里我们指定了数据选择/插入/更新/删除所需的 URL。模型（Model）是 `Wine`，它将用于存储来自 Web 服务端点的数据并进行操作，它是集合（Collection）`WineCollection` 的一部分。

`default` 参数用于在添加数据时初始化一个新模型。

应用程序中有三个视图（View）：

A. `WineListView` – 包含一个项目视图（Item View）集合 - `WineListItemView`

B. `WineListItemView` – 负责渲染模型模板 – `WineView`

C. `WineView` – 包含添加、删除和更新的核心方法 -

有趣的方法是 – 1> `saveWine` 和 2> `deleteWine`

D. `HeaderView` – 负责初始化用于添加新模板的视图。

有趣的方法是 – `newWine`

路由器（Router） - `AppRouter` 负责应用程序的初始路由。

### 客户端 JavaScript MVC 中的 Backbone.js

本文是 [基于 Backbone.js 的 Java Web 项目应用](http://www.phloxblog.in/developing-java-web-applications-backbone-js) 的扩展。

项目代码可以 [在此处](https://github.com/piyasde/GitHub_Projects) 下载。

在 Backbone.js JavaScript MVC 框架中，模型（Model）指的是客户端用于数据操作、客户端验证、从服务器端获取数据以及最终提交到服务器端的中间数据持有对象。

在我们的例子中，模型代码如下：

```
 1 window.Wine = Backbone.Model.extend({
 2 urlRoot:"http://localhost:8080/brandserver/rest/wines",
 3      defaults:{
 4      "id":null,
 5      "name":"",
 6      "grapes":"",
 7      "country":"USA",
 8      "region":"California",
 9      "year":"",
10      "description":"",
11      "picture":""
12     }
13 });
```

这里，`defaults` 属性用于新模型数据实例化时的数据。

我们还可以在 `AppRouter` 的 `newwine` 函数中看到模型数据的实例化：

```
1 app.wineView = new WineView({model:new Wine( 
2 		{id:null,name:"",
3 		 grapes:"",
4                  country:"",
5                  region:"",
6                  year:"",
7                  description:"", 
8                  picture:"generic.jpg" }
9  )}); // 模型实例化
```

这里我们向 `Wine` 模型的属性传递了一些值。

在模型中，`urlRoot` 指定了基于 REST 的 Web 服务的主 URL 路径。

在我们的例子中，它是：

`urlRoot:"http://localhost:8080/brandserver/rest/wines"`

现在在 -

```
1 window.WineCollection = Backbone.Collection.extend({
2     model:Wine,
3     url:"http://localhost:8080/brandserver/rest/wines"
4 });
```

名为 `WineCollection` 的集合使用模型 `Wine` 进行初始化，期望通过调用基于 REST 的 Web 服务从服务器获取相同的 json 数据。

有趣的是，当执行以下代码时，`AppRouter` 会调用 `list` 函数，该函数实际上在内部发起了一个基于 REST 的 Web 服务调用：

```
1 this.wineList = new WineCollection();
2 this.wineListView = new WineListView({model:this.wineList});
3 this.wineList.fetch(); // 调用服务器获取所有数据（REST Web 服务）
```

现在有趣的是模型保存函数 – `saveWine` -

```
 1     var win = new Wine(this.model);
 2 
 3     win.set({
 4         name:$('#name').val(),
 5         grapes:$('#grapes').val(),
 6         country:$('#country').val(),
 7         region:$('#region').val(),
 8         year:$('#year').val(),
 9         description:$('#description').val()
10    });
11 
12    // 部分代码片段
13    app.wineList.create(win, {  // 内部调用 REST Web 服务
14        success:function () {
15             	alert('Wine saved successfully');
16                	app.navigate('', true);// 初始化状态
17                 window.history.back(); 
18              }
19       });
20    // 上述代码片段用于将新模型保存到服务器。create 函数很重要。此
21    // 回调函数在实例化新模型并为其属性设置值后被调用。
22 
23    win.save(); // 内部调用 REST Web 服务
24    alert('Wine updated successfully');
25    app.navigate('', true); // 初始化状态
26    window.history.back();
27    // 上述代码片段用于将模型更新到服务器。save 函数很重要。此
28    // 回调函数在设置现有模型属性的值后被调用。
```

现在来看 `deleteWine` 函数 -





```
 1     var win = new Wine(this.model); // Instantiate variable with current model.
 2     win.destroy({ // REST Web Service Calling
 3          success:function () {  
 4                 alert('Wine deleted successfully');
 5                 app.navigate('', true);
 6                 //window.history.back();
 7             }
 8         });
 9 
10    // The above Code snippet is used for deleting a model to the server. The destory funct\
11 ion is important. This     
12    // callback function is called to delete corresponding row in database of the current m\
13 odel. 
```

### 客户端 JavaScript MVC 中的 Backbone.js 路由

在 Backbone.js JavaScript MVC 框架中，路由用于通过哈希标签（#）导航网站 URL。

Backbone.js 中的所有路由都包含路由及其映射函数。在我们的案例中，路由指的是——

```
 1 // Router
 2 var AppRouter = Backbone.Router.extend({
 3 
 4 	initialize:function () {
 5         // Function is called at the time of initialization of Router.
 6     },
 7 
 8     routes:{
 9         "wines/new":"newWine", // a router mapping to a particular function newWine
10         // Other code snippets // Other route paths...
11     },
12 
13     list:function () {
14         // Code to fetch the value from database using the REST based web service.
15         $('#sidebar').html(this.wineListView.render().el); // Rendering a html fragment - \
16 template by Backbone View.
17     },
18 
19     // Other code snippets....
20     newWine:function () {
21         // mapped function from route. 
22         // New Model initialisation and html template rendering code to be here.
23     }
24 });
```

```
1 var app = new AppRouter(); // Backbone router initialisation
2 Backbone.history.start(); //  Start Backbone history to capture navigation pattern in brow\
3 ser for later use.
```

### 客户端 JavaScript MVC 中的 Backbone.js 视图

Backbone.js 视图用于渲染客户端应用程序数据模型。它们用于监听事件并据此执行操作。我们将结合 JavaScript 模板库，在应用程序中针对其中一个视图解释视图功能。

```
 1 window.HeaderView = Backbone.View.extend({
 2 
 3     template:_.template($('#tpl-header').html()), // Here template controls the DOM Elemen\
 4 t in the HTML.
 5 
 6     initialize:function () {
 7        // This function will be called at the initialisation of a View...
 8         this.render(); // render function loads the template in the el property of backbon\
 9 e.js
10     },
11 
12     render:function (eventName) {
13         $(this.el).html(this.template());
14         // Above el is a property of backbone view. This is created as empty div element i\
15 n browser and the control on        
16         // the Div element is done completely by the Backbone.js. As this binds the contai\
17 ner element, all the events 
18         // will trigger for this element. 
19         return this;
20     },
21 
22     events:{
23         "click .new":"newWine" 
24         // here the listening for click event is happening. And it will call the mapped ne\
25 wWine function 
26     },
27 
28     newWine:function (event) {
29         // when Button is clicked, this function is called for the Click event trigger.
30         app.navigate("wines/new", true);
31         return false;
32   }
33 });
```

项目代码可在此处下载：[这里](https://github.com/piyasde/GitHub_Projects)。

**更多资源：**

[什么是视图？](http://backbonetutorials.com/what-is-a-view)

[Backbone.js 教程：列表视图](http://dailyjs.com/2012/12/27/backbone-tutorial-5)

[什么是路由？](http://backbonetutorials.com/what-is-a-router)

1.  [Backbone.js 经验教训与改进示例应用](http://coenraets.org/blog/2012/01/backbone-js-lessons-learned-and-improved-sample-app)

2.  [完全掌握 Backbone.js](http://javascriptissexy.com/learn-backbone-js-completely)


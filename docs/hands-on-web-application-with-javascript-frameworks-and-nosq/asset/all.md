![](images/00016.jpeg)

## Hands-On Web Application with Javascript Frameworks and NoSQL

### Collective knowledge from Programmer to Programmer

#### Piyas De

This book is for sale at [http://leanpub.com/javascriptnosql](http://leanpub.com/javascriptnosql)

This version was published on 2014-02-28

![publisher's logo](images/00001.jpeg)

*   *   *   *   *

This is a [Leanpub](http://leanpub.com) book. Leanpub empowers authors and publishers with the Lean Publishing process. [Lean Publishing](http://leanpub.com/manifesto) is the act of publishing an in-progress ebook using lightweight tools and many iterations to get reader feedback, pivot until you have the right book and build traction once you do.

*   *   *   *   *

[![Creative Commons by](images/00002.jpeg)](http://creativecommons.org/licenses/by/3.0/deed.en_US)

This work is licensed under a [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/deed.en_US)

To Titas, Ketaki and Parma

# Table of Contents

*   [Preface](#part0003.html_leanpub-auto-preface)
    *   [Why this book?](#part0003.html_leanpub-auto-why-this-book)
    *   [What is the aim?](#part0003.html_leanpub-auto-what-is-the-aim)
    *   [Who is the book for?](#part0003.html_leanpub-auto-who-is-the-book-for)
*   [Starting the Web Server with Javascript](#part0004.html_leanpub-auto-starting-the-web-server-with-javascript)
*   [Javascript in OOP Way - some interesting study](#part0005.html_leanpub-auto-javascript-in-oop-way---some-interesting-study)
*   [A Simple jQuery Image Slider Plugin with minimal effects](#part0006.html_leanpub-auto-a-simple-jquery-image-slider-plugin-with-minimal-effects)
*   [Simple Bar Graph with d3.js and Prototype.js - a Javascript Class based Approach](#part0007.html_leanpub-auto-simple-bar-graph-with-d3js-and-prototypejs---a-javascript-class-based-approach)
*   [Concepts in Angular.js Application Development](#part0008.html_leanpub-auto-concepts-in-angularjs-application-development)
*   [Angular.js Service and Dependency Injection](#part0009.html_leanpub-auto-angularjs-service-and-dependency-injection)
*   [Angular.js $watch and $observe - a brief look](#part0010.html_leanpub-auto-angularjs-watch-and-observe---a-brief-look)
*   [Angular.js Promise and Deferred Api - Implementation Explained](#part0011.html_leanpub-auto-angularjs-promise-and-deferred-api---implementation-explained)
*   [JavaScript Testing Framework - Jasmine - a quick study](#part0012.html_leanpub-auto-javascript-testing-framework---jasmine---a-quick-study)
*   [Angular.js Tests with Jasmine](#part0013.html_leanpub-auto-angularjs-tests-with-jasmine)
*   [jQuery Plugin under Angular.js Directive - a more clean html approach](#part0014.html_leanpub-auto-jquery-plugin-under-angularjs-directive---a-more-clean-html-approach)
*   [D3.js in Angular.js Directive - a relief from D3 svg code in HTML Page](#part0015.html_leanpub-auto-d3js-in-angularjs-directive---a-relief-from-d3-svg-code-in-html-page)
*   [Simple Bar Graph in Angular Directive with d3.js and Prototype.js – a Javascript Class based Approach](#part0016.html_leanpub-auto-simple-bar-graph-in-angular-directive-with-d3js-and-prototypejs----a-javascript-class-based-approach)
*   [Simple Bar Graph in Angular Directive with d3.js and Prototype.js – Element based Directive Definition](#part0017.html_leanpub-auto-simple-bar-graph-in-angular-directive-with-d3js-and-prototypejs----element-based-directive-definition)
*   [Creating Google Chrome Extension to add a Custom RSS Feed Reader](#part0018.html_leanpub-auto-creating-google-chrome-extension-to-add-a-custom-rss-feed-reader)
*   [Task List with Angular.js, HTML5 Local Storage and Decorate with Bootstrap in Google Chrome Extension](#part0019.html_leanpub-auto-task-list-with-angularjs-html5-local-storage-and-decorate-with-bootstrap-in-google-chrome-extension)
*   [Preliminary Concepts of Graph Database](#part0020.html_leanpub-auto-preliminary-concepts-of-graph-database)
    *   [A Case Study in Graph Database in Context of Neo4j Cypher Query](#part0020.html_leanpub-auto-a-case-study-in-graph-database-in-context-of-neo4j-cypher-query)
*   [Quick Glance at Neo4j Cypher Queries for Sample Graph Database](#part0021.html_leanpub-auto-quick-glance-at-neo4j-cypher-queries-for-sample-graph-database)
*   [Develop Web Application with Node.js, Express.js REST Service and Neo4j (neo4j-js module)](#part0022.html_leanpub-auto-develop-web-application-with-nodejs-expressjs-rest-service-and-neo4j-neo4j-js-module)
*   [A Quick Primer on MongoDB](#part0023.html_leanpub-auto-a-quick-primer-on-mongodb)
*   [Single Page Application with Angular.js, Node.js and MongoDB (MongoJS Module)](#part0024.html_leanpub-auto-single-page-application-with-angularjs-nodejs-and-mongodb-mongojs-module)
*   [Web Application with Highchart.js, Node.js, Express.js and MongoDB(Mongo-JS Module)](#part0025.html_leanpub-auto-web-application-with-highchartjs-nodejs-expressjs-and-mongodbmongo-js-module)
*   [Real-time Data update with Angular.js, Node.js and Socket.io](#part0026.html_leanpub-auto-real-time-data-update-with-angularjs-nodejs-and-socketio)
*   [Single Page Application with Angular.js, Node.js and CouchDB (Cradle Module)](#part0027.html_leanpub-auto-single-page-application-with-angularjs-nodejs-and-couchdb-cradle-module)
*   [POST requests with Google DART, Node.js and MongoDB](#part0028.html_leanpub-auto-post-requests-with-google-dart-nodejs-and-mongodb)
*   [Node.js Unit Testing with Should.js](#part0029.html_leanpub-auto-nodejs-unit-testing-with-shouldjs)
*   [Developing Java REST web applications with Backbone.js](#part0030.html_leanpub-auto-developing-java-rest-web-applications-with-backbonejs)
    *   [Server Side -](#part0030.html_leanpub-auto-server-side--)
    *   [Backbone.js in Client Side Javascript MVC](#part0030.html_leanpub-auto-backbonejs-in-client-side-javascript-mvc)
    *   [Backbone.js Router in Client Side Javascript MVC](#part0030.html_leanpub-auto-backbonejs-router-in-client-side-javascript-mvc)
    *   [Backbone.js View in Client Side Javascript MVC](#part0030.html_leanpub-auto-backbonejs-view-in-client-side-javascript-mvc)

## Preface

### Why this book?

In the last few years, we came across different client side projects which were traditionally built on J2ee or other Open Source Technologies such as PHP, Ruby etc. On the other hand, the year 2013 saw increasing popularity of several javascript frameworks like Angular.js, Backbone.js which in turn gained momentum in client side development. These strong winds of change were brought about structural framework, coding and performance enhancement in development and production environment became absolutely imperative. On top of that emerging small sized projects and start-up companies have shown growing interest in adapting those new technologies.Evolving trends for storing non-structure data within repository is collectively called nosql in 2013\. It is obvious that these fresh trends are clearly coming with new set of tools in software which revolve around javascript and nosql related repositories.Today javascript is not merely used for client side validation. It offers server side development for web applications along with node.js platform. In this book, we have tried to show start-up experimentation with some of these tools.

### What is the aim?

The aim of this book is to show the use of some of the above mentioned tools in application and how we can start development of application with those tools. The book deals with some of the Proof-of-Concept Applications with the help of those tools. Apart from that,brief descriptions of some important aspects of these tools have also been incorporated . Being a developer from the very begining of my career, I always tried to find the codes which I can put together to generate new concepts in work. This book is a collective outcome of my efforts and experimental view with that acumen in mind. So there will be continuous updation of fresh knowledge from time to time.One personal opinion of mine is, working with new technologies like Javascript and NoSql related products is fun and I am thoroughly enjoying this phase. Also just to accompany, I am not an author but a programmer by profession; so writing things with all the theories and explanations was not my intention, rather I prefer to include practical working examples.

### Who is the book for?

People with web programming backgound with javascript knowledge will find this book useful because this book is a collective knowledge source of usages of Javascript based tools and different application areas with those. The chapters of the book are explained with important aspects of the tools and covered with various coding explanations rather than just original theories. It is worth mentioning that I tried to incorporate explanations of the concepts as and when required. This book is not for beginner programmer but for the programmers with intermediate knowledge and for advanced programmers who have already mastered the traditional web programming with age-old J2ee, PHP, Dot net or other open source web technologies (like me..).

## Starting the Web Server with Javascript

We have found server side javascript framework like node.js platform is quite useful in development. We have not explained much about node.js in chapters of this book, but below is a litte introduction about node.js, which is used for most of the proof-of-concepts in this book.

Now-a-days developers know about Node.js as a server -side javascript execution platform.

According to nodejs.org -

> “Node.js is a platform built on Chrome’s JavaScript runtime for easily building fast, scalable network applications. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.”

Now node.js opens a new way of performing or serving to the web requests or any other type of server requests – which is called Non-blocking IO Operation.

We have came across the following link - http://code.danyork.com/2011/01/25/node-js-doctors-offices-and-fast-food-restaurants-understanding-event-driven-programming/, which is an excellent way of showing the non-blocking concepts of node.js with relate to real-life working scenarios.

As my background for last 5-6 years as J2ee Programmer, I knew and understood the Servlet Programming Model in J2ee Environment, which is a multi-threaded programming model i.e. when a web request come to java based web server, the request hit to the servlet with the request and the servlet opens a new thread to handle the request and response the data back to the client. All the database related methods or any server resource intensive call, which are shared in nature, are to be handled carefully from the servlet to avoid any deadlock or other unwanted situations which will be related to shared objects.

Though through this way a process parts in threads and serves the web request within thread which are having relatively small overhead as compared to server processes. But still if some database call amounts to a significant time within the execution of request and response which is within a thread call, it will hold the client for this with their synchronous activity which is blocking IO operation.

Now it is time to understand the non-blocking I/O, on which node.js platform is defined.

First of all, node.js application environment will run on a single threaded programming model.

All the web requests and server requests call in node.js are of non-blocking I/Os. An web request comes in node.js web server and the web server accepts this request and handle this request to a listener object to process the response. Also this web server will remain ready to accept any new web request. And the previous response handling will remain in a queue for performing the rest of operations. Now the node.js environment takes care of preparing the web response which again can be a database call from the actual application. Also this database query can also consists of callback functions with the response from database as being ready. Those operations are executed in a queue and also called as event driven programming and all of these operations are asynchronous in nature.

So the whole point to discuss here is, all the function calls within node.js context are non-blocking input-output operations. In node.js environment, the performing operation is executed by one object and the results of the operation are handled by the callback functions.

For understanding node.js we recommend an excellent book at (http://www.nodebeginner.org/).

We have used the node.js based web server for most of the next applications in this book.

## Javascript in OOP Way - some interesting study

As we are moving towards a world of client side MVC in Front End Web Application Development, new frameworks of javascript are becoming extremely important. We have posted here the Object Oriented Programming and other interesting facts in Javascript with feature examples. So below are the codes with Comments -

##### Some interesting facts about Javascript

###### Javascript Object Definitions

```
1 var newObject = new Object();
2 var newObj = {};
```

###### Defining properties for an object

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

###### Interesting nested object access in javascript

The following type of Javascript Class is defined with Literal Notation. Within one class, variables are defined as properties and functions are defined as methods of that particular class.

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

##### Interesting facts about function in javascript

###### A function declaration -

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

In the above example, the first call of the function will return NaN. For the second one, the function will work for the two arguments and for the last one, the extra third parameter will be ignored.

###### Now… functions have access to an additional variable inside - called arguments

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

In javascript, all the parameters are called as arguments. And we can call functions with any no of arguments or no argument as in the example above.

###### Anonymous function in Javascript

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

In the above example, **simpleFunction** is defined with an anonymous function and it is returning string from within that function.

###### JavaScript is a prototype-based language which contains no class statement

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

###### Now more concise definition of the class

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

###### Next is use of prototype. SomeObject.prototype will be used by all instances of SomeObject.

Look for usages of ‘this’ and ‘new’ at below -

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

###### Adding extra methods at prototype

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

###### Inner functions

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

###### Javascript Closures (Cleverly confusing….)

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

The output will be - `javascript 11 27`

###### Class in Javascript

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

###### Inheritance in JavaScript

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

###### Encapsulation

In above, TechnicalPost does not need to know the body of Post class’s createpost() method,but can use that method; the TechnicalPost class doesn’t need to define the method unless we need to override or use it. This is encapsulation, by which every class inherits the methods of its parent and only needs to define things it wishes to change. Also the child class can define other methods.

**References :**

[Introduction to Object-Oriented JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)

[A re-introduction to JavaScript (JS Tutorial)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript)

## A Simple jQuery Image Slider Plugin with minimal effects

We have tried to make a simple jQuery Image Slider Plugin to understand the jQuery Animation and Plugin functionality in more Details. This Image Slider Plugin is having feature to slide whole content from UP, Down, Left and Right, which are configurable from HTML Page.

Here we have gone through this plugin code.

We have gone through the Article - [How to Create your own jQuery Slider Plugin](http://www.script-tutorials.com/how-to-create-your-own-jquery-slider-plugin/) to make this plugin.

So thanks to (script-tutorials.com) for this. Now below is the code part.

We have explained the code in comment section of HTML or jQuery Coding.

###### HTML Part -

```
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
19 		<p>this is 1</p>
20 	      </li>
21               <li><img src="Desert.jpg" width="480" height="310" alt="" />
22                 <p>this is 2</p>
23               </li>
24           </ul>
25      </div>
26    </div>
27 </body>
28 </html>
```

###### jQuery Plugin Code -

```
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

Reader can look through the code [here](http://www.phloxblog.in/wp-content/uploads/2013/06/imagesliderplugin.zip).

## Simple Bar Graph with d3.js and Prototype.js - a Javascript Class based Approach

[![AngularD3BarGraph](images/00003.jpeg)]

We were working to convert our client side javascript code to convert in Object Oriented approach.

So we have gone through learning process of javascript OOP in previous chapter. Here we are trying to separate the d3.js code to put in Javascript Framework and for that we have taken the prototype.js to make the javascript classes for the d3.js code separation.

So what have we really done in HTML ?

###### 1> Added the prototype.js, d3.js in the HTML Page and the reference of the d3 related javascript class

```
1 <script type="text/javascript" src="js/prototype.js"></script>
2 <script src="js/barGraphProto.js"></script>
3 <script src="http://d3js.org/d3.v3.min.js"></script>
```

###### 2> Put the the d3.js related class initialisation -

```
1 var   ourGraph = new BarGraph('sample.json','Year',905,'Frequency',6,'.0%'); 
2 //d3 related Variable initialisation
3 ourGraph.workOnElement('#d3bar'); // Work on particular element
4 ourGraph.generateGraph(); // generate the actual bar graph
```

###### 3> The d3 related bar graph code -

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

[Here](http://www.phloxblog.in/wp-content/uploads/2013/07/simpleProto.zip) is the code for this for reader’s interest. We will reuse the d3 related javascript class code in Angular.js Directive section.

## Concepts in Angular.js Application Development

In this chapter we will discuss some of the well-known concepts in Angular.js Application Development one-be-one.

###### 1> ng-app -

It is an angular directive, which defines a html body or a portion of html body to be defined as Angular.js Application.

###### 2> Angular Expression -

Some code like `{{ some_angular_variable }}` will evaluate the variable value. It is Angular Expression.

###### 3> Angular View Template -

An Angular.js View Template is a portion, which will be replaced by the data from Angular Model.

###### 4> Angular Controller -

Angular Controller is a form of JavaScript function, within which variable values for attributes of DOM elements are bound and the presentation logic of variables bound with DOM element attributes are controlled and changed within the control of the JavaScript function(Controller). So the presentation logic for the values of the variables should be controlled in Angular Controller and those variables are bound with ng-model directive or angular expression with the DOM elements and Angular framework offers automatic binding of the variables with DOM Elements, where specified i.e. whenever the variable values will be changed within the Controller, that change will have automatic effect on the DOM elements.

###### 5> Angular Scope Variables -

In an Angular.js Application, JavaScript variable values will have existence within angular scope life-cycle. So all the variables can be observed for change of value and take action for that - within the respective scope of Angular.js Application.

###### 6> Angular MVC -

###### A> Angular Model -

Model is the data, which can be accessed by property of Angular Scope.

###### B> Angular Controller -

Angular Controller is a form of JavaScript function, within which variable values for attributes of DOM elements are bound and the presentation logic of variables bound with DOM element attributes are controlled and changed within the control of the JavaScript function(Controller).

###### C> Angular View -

In Angular framework, the views consist of HTML Elements and Angular expressions, which are rendered in Browser, after manipulated in Angular Controller and Angular Model.

###### So an angular example is here below-

###### An example Angular Model

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

###### Angular Code Snippet in HTML

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

###### Angular Controller

```
1 function StockListCtrl($scope, $http) {// Dependency Injection for Angular Service
2 	$http.get('stocks.json').success(function(data) { // Angular $http Service
3 	 $scope.stocks = data;
4 	});
5 }
```

In next chapters, we will discuss about Angular Services and Dependency Injection in Angular Application.

**References :**

[Angular.js Documentation](http://docs.angularjs.org/tutorial)

## Angular.js Service and Dependency Injection

In the current chapter, we will try to explain the Angular.js Service Definitions with some of the ways with our coding.

First is the example of declaring service within Angular Factory and access it in Angular Controller -

###### Below is the Controller

```
1 app.controller('StockListCtrl', function($scope,stockService) { 
2     // Putting Angular in the Service
3     stockService.getStocks(function(data){                      
4         // Accessing controller methods 
5         console.log(data);
6         $scope.stocks = data;
7     });
8 });
```

###### Below is the above mentioned stockService within Angular Factory

```
 1 app.factory('stockService', function($http) {
 2     // Service Declaration and inclusion of built-in $http service
 3     return {
 4         getStocks: function(callback) {      
 5             // returning the method as public one from the Service
 6             $http.get('stocks.json').success(function(data) { 
 7                  //get access to external resource
 8                  callback(data);             
 9                  // initiating callback with data, 
10                  // to manipulate at method access level
11             });
12         }
13     }
14 });
```

Second one is the example of **Service Provider** -

```
 1 app.config(function($provide) {                    
 2 	// Angular App Configuration Section
 3   $provide.provider('stockService', function() {   
 4 	// making the service provider with built-in provide service
 5     this.$get = function($http) {                  
 6         // the convention to get the service - $get 
 7         // - service will be instantiated with this call 
 8       return {
 9 	  getStocks: function(callback) {          
10                 // returning the method as public one from the Service                    \
11    
12 		$http.get('stocks.json').success(function(data) { 
13                         //get access to external resource
14 			callback(data);      
15                         // initiating callback with data, 
16                         // to manipulate at method access level     
17 		});   
18 	     }
19 	 }
20       };
21   });
22 });
```

For the above service, we can reuse the same controller as we had specified above.

###### Now some bits about getting service from Angular Dependency Injection service -

Angular Injector($injector) is responsible for creating instances of custom angular service. An injector is instantiated within angular environment as the Angular Application is created.

###### 1st Way of using Dependency Injection in Angular.js

```
 1 app.controller('StockListCtrl', function($scope,$injector ) {
 2 	var stkService = $injector.get('stockService'); 
 3         // getting the service from Angular $injector object, which
 4         // is responsible for pushing the service from angular 
 5         // App configuration to other functions or controller 
 6 	stkService.getStocks(function(data){
 7 	   console.log(data);
 8            $scope.stocks = data;
 9         });
10    });
```

###### Another Way of using Dependency Injection in Angular.js – recommended as Angular Doucmentation

```
1 app.controller('StockListCtrl',
2     ['$scope', 'stockService', function($scope,stockService ) {  
3         // Taking the Dependency
4 	stockService.getStocks(function(data){                   
5         // stockservice is injected here within controller
6 	  console.log(data);
7           $scope.stocks = data;
8         });
9   }]);
```

Reader should go in more deep explanation for Angular.js services in following references -

[https://github.com/angular/angular.js/wiki/Understanding-Dependency-Injection](https://github.com/angular/angular.js/wiki/Understanding-Dependency-Injection)

[http://stackoverflow.com/questions/13937318/convert-angular-http-get-function-to-a-service](http://stackoverflow.com/questions/13937318/convert-angular-http-get-function-to-a-service)

## Angular.js $watch and $observe - a brief look

##### Angular.js $watch -

Angular.js $watch event is fired every time, when it detects change on a DOM attribute variable value. For a $watch expression, the listener fire every time when it detect that the current value in context is not same as the previous value. To undetstand the $watch expression we put below a simple working example. We have created a input text which is bound by a ng-model - **watchtext**. We will be able to change the value of the textbox and able see the previous value and current value in the html page.

###### HTML Code is here -

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

Here we have angular.js controller - **“ctrl”**. Also other codes are commented in the javascript code.

###### Angular.js Code is here -

```
 1 function Ctrl($scope) {
 2 	var scope = $scope;
 3 	scope.watchtext = 'First Value'; // watchtext is initialised here.
 4 	scope.counter = 0;
 5 	scope.lastvalue = '';
 6 	scope.currentvalue = '';
 7 
 8 	$scope.initCounter = function() {
 9 		scope.counter = 0; // the counter variable is initialized here.
10 	}
11 
12 	scope.$watch('watchtext', function(newValue, oldValue) { 
13 		scope.counter = scope.counter + 1; 
14 		scope.lastvalue = oldValue;
15 		scope.currentvalue = newValue;
16 	});
17 	// The lastvalue and currentvalue are updated in html page 
18 	// through angular expression. Those are updated in watch function.
19 }
```

###### Angular $observe -

In Angular Directive Linking Phase, the observe function is the position, where all attribute values can be taken for further execution of the directive code-base. HTML Code is here -

```
1 <div id="bar" sample-directive time-interval=1000 datajson="sample.json"> 
2 <!-- Attribute value setting -->
3  scope.firstvalue is {{firstvalue}}<br/>
4  scope.secondvalue is {{secondvalue}}<br/>
5 </div>
```

Below is a Attribute Directive - **“AngularExample”** which is only illustrated for example. Codes are commented below. Angular.js Code is here -

```
 1 angular.module('AngularExample', [])
 2 .directive('sampleDirective', function ($timeout) {// Angular Directive
 3   return {
 4         restrict: 'A', // Attribute only directive
 5     scope: {
 6             timeInterval: '@', // Getting variable values with @, 
 7                                // which are not immediately available in
 8 	datajson: '@'      // link function
 9         },
10         link: function (scope, elem, attrs) {
11 	console.log(scope.timeInterval);
12 	attrs.$observe('timeInterval', function(value) { 
13 		// getting attribute value only in observe
14                 // function from HTML DOM
15 		console.log('timeInterval has changed value to ' + value);
16 		scope.firstvalue = value;
17 	  });
18 	attrs.$observe('datajson', function(value) {
19 		console.log('datajson has changed value to ' + value);
20 		scope.secondvalue = value;
21 	  });
22 	console.log(scope.firstvalue);
23 
24 	var t = $timeout( function() { 
25                 // Use of a timeout function - to show the change of attribute 
26                 // variables after some time. It is a position on which HTML DOM
27                 // presentation can be changed by tracking the angular variables. 
28 
29 	    scope.firstvalue = 'new--' + ' and old--1' ;
30 	    scope.secondvalue = 'new--' + ' and old--2' ;
31 
32 	}, 2000);
33         }
34     }
35 });
```

Reader can view a complete plunker for this in -

[http://plnkr.co/VTVep9yW5hr8HKK2KtDX](http://plnkr.co/VTVep9yW5hr8HKK2KtDX)

## Angular.js Promise and Deferred Api - Implementation Explained

###### Angular.js Promise -

A promise in Angular.js act as an placeholder from where a javascript object returns some result as data which is done in an asynchronous way and it does not guarantee any fixed response time. A combination of deffered and promise API in Angular.js ensure the success and reject callback handling in client side code with asynchronous system handling.

###### Angular.js Deferred Api -

This deferred object is constructed with $q.defer(). This Api is used to notify the success or unsuccesful completion of the asynchronous work, which is within the context of Deferred Api. The **deferred object** handle success and reject situation with **.resolve(arg)** and **.reject(arg)** method.

###### Angular.js Promise Api -

**deferred.promise** returns a promise instance in Angular.js. After completing the task in deferred object, we can have access to the result in promise object. **`promise.then(success, error)`** – This section always gives a definite result to the UI, whether it is success or error, within success or error callback. One of the method - resolve or reject is called with either result or rejection reason.

###### Angular.js Promises Chain -

As the derived object in promise.then is also a promise object, we can establish promises chain here. To accomplish the promise functionality, we have **$q service** functionality in Angular.js. Here **$q** is integrated with Angular scope model and it is recognised by Angular template engine. Now below is the commented code-base to show the functionality of **Promise** -

```
 1     'use strict';
 2     
 3     var app = angular.module('angularjs-promise', []); // Creation of Application
 4     
 5     app.controller('PhoneListCtrl', function($scope, phoneService) { 
 6 		// Angular Controller Definition with service injection
 7             phoneService.getPhones().then(function(data) {// Angular promise
 8                 $scope.phones = data;
 9             });
10        });
11     
12     app.factory('phoneService', function($http, $q) {
13 		// Angular Service Declaration
14         return {
15             getPhones: function() {                                 
16                 var deferred = $q.defer(); // Deferred Object Declaration
17                 $http.get('phones.json').success(function(data) {   
18 				// Asynchronous Service calling
19                      deferred.resolve(data);
20                 }).error(function(){
21                      deferred.reject();
22                 });
23             return deferred.promise;
24          }
25        }
26     });
```

To understand the full functionality, we have made a plunker, the link is -

[http://plnkr.co/hBbq6qiCXZXttkFEnZWj](http://plnkr.co/hBbq6qiCXZXttkFEnZWj)

**References :**

[Angular.js Documentation](http://docs.angularjs.org/api/ng.$q)

## JavaScript Testing Framework - Jasmine - a quick study

Now-a-days various JavaScript based applications are being increasingly popular. So there are requirements to test JavaScript code in automated way are being evident in all aspects of development work. Below is a short study on

##### JavaScript Testing Framework - Jasmine

###### Installation and Running Section -

Install the Jasmine Standalone framework from **[here](https://github.com/pivotal/jasmine/downloads)**. Unzip the folder. Put the TestSpce code in <<your functional_spec>>.js file in spec folder within jasmine standalone folder. Put the JavaScript code in <<your functionality>>.js file in src folder within jasmine standalone folder.

Now attach the script tag of source JavaScript file in **include source files here** section in the **SpecRunner.html** file in **jasmine installation folder**. Attach the script tag of spec JavaScript file in **include spec files here** section in the **SpecRunner.html** file in **jasmine installation folder**. Now if we run the **SpecRunner.html**, sample specs should be passed and the messages should be shown in **SpecRunner.html** File. That is it for installation.

###### Some points to understand within Jasmine -

###### 1. Jasmine is a javascript testing framework which is suited for behaviour driven development.

###### 2. ‘describe’ is a keyword in test suite for jasmine tests

###### 3. tests in jasmine testing framework is defined by ‘it’ within the ‘describe’ block.

###### 4. These are individual test units under jasmine framework.

###### 5. In ‘describe’ and ‘it’ block, any javascript executable function can run.

###### 6. Any variable declared within ‘describe’ function, will be available in all ‘it’ functions within the particular ‘describe’ function block.

###### 7. Expectations are the function which expect actual value to be compared with values returned from function.

###### 8. Matchers do boolean comparison with actual value and expected value. It reports jasmine to have expectation as true or false.

##### Below are some coding for testing and explained within comments -

Our JavaScript Source file code -

(Some minimum coding with Prototype based JavaScript Class) -

If reader is not familiar with JavaScript Classes, he/she can go through Javascript in OOP Way – some interesting study in first chapter.

```
 1     // simple javascript functions
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
13     // Javascript prototype based class
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
26     	return 'Full Address is (prototype) -->>' + '\n' + this.streetno + 
27 			' ' + this.streetaddress + '\n'
28                          + this.city + ' ' + this.pincode + '\n' + 
29 			 this.state + ' ' + this.country;
30     }
31     
32     AddressWithPrototype.prototype.changeAddressForCity = function() {
33         this.city = 'Delhi';
34     	return 'Full Address is (prototype) -->>' + '\n' + this.streetno 
35 			 + ' ' + this.streetaddress + '\n'
36                          + this.city + ' ' + this.pincode + '\n' 
37 		         + this.state + ' ' + this.country;
38     }
```

##### Our Test Spec Codes are as follows -

```
 1     describe("Hello world", function() {  // Jasmine Test Suite
 2         it("says hello", function() {     
 3 		// Individual Test Component - refer to our source javaScript file code
 4             expect(helloWorld()).toEqual("Hello world!");  
 5 		// Equality checking with function output
 6         }); 
 7     
 8         it("says world1", function() {
 9             expect(helloWorld()).toContain("world");      
10 		// Checking of particular value in function output
11         });
12     
13         // Adding own Matchers
14         beforeEach(function() {
15             this.addMatchers({
16                 toContainElementMoreThanZero: function() {  
17 			// Creating custom Matcher
18                     return (this.actual > 0);
19                 }
20             });
21         });
22      
23         it('contains more than one array element', function() {
24             expect(checkArraylength()).toContainElementMoreThanZero(); 
25 		// Applying Custom Matcher
26         });
27         
28         var newAddress;
29         
30         beforeEach(function() {
31     		newAddress = new AddressWithPrototype("4C", "Chidam Mudi Lane", 
32                     "Kolkata", "West Bengal", "India", "700006");  
33 			// Refer to source JavaScript Class
34         });
35         
36         it("calls the fullAddress() function", function() {
37             spyOn(newAddress, "fullAddress");  
38 		// invocation of fullAddress method of Class will be checked
39             newAddress.fullAddress();
40             expect(newAddress.fullAddress).toHaveBeenCalled(); 
41 		// Calling of method will be ensured
42         });
43         
44         it("calls with 'Delhi' as argument", function() {
45             spyOn(newAddress, "changeAddressForCity");
46             newAddress.changeAddressForCity("Delhi");
47     	    expect(newAddress.changeAddressForCity).toHaveBeenCalledWith("Delhi"); 
48 		// Called with 'Delhi' as argument
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

##### Asynchronous Functionality Testing

```
 1     describe("async tests", function(){
 2      var flag, value;
 3      it("should simulate an asynchronous call", function () { 
 4       runs(function() { 
 5         flag  = false; 
 6         value = 0; 
 7     
 8         setTimeout(function() { // This function will be called 
 9 			        // after 500 miliseconds
10           value++; 
11           flag = true; 
12         }, 500); 
13       });  
14     
15       waitsFor(function() {     
16 		// Waiting till value return from the function call
17         return flag; 
18       }, "The Value should be incremented", 5000);  
19 	// If no result found after waiting for 5 seconds, then exit from
20         // framework method 
21       runs(function() {  
22         expect(flag).toEqual(true);   
23         expect(value).toEqual(1); 
24       }); 
25      }); 
26     });
```

Other key points related to jasmine to be noted are as follows -

Some of the Key features which we can use in jasmine tests

**Scenario 1 -**

```
1 var a; 
2 a = true; 
3 expect(a).toBe(true); <-- here .toBe is a keyword for testing
4 expect(false).not.toBe(true); <-- another variation of test with not keyword
```

**Scenario 2 - matcher for regular expressions**

```
1 var message = 'It is an address'; 
2 expect(message).toMatch('address'); <-- here .toMatch is a keyword for testing
3 expect(message).toMatch(/address/); 
```

**Scenario 3 - matcher to compare against ‘undefined’**

```
1 var person = 'Piyas De'; 
2 expect(person).toBeDefined(); <-- here .toBeDefined is a keyword for testing 
3 expect(aotherperson).not.toBeDefined(); 
4 
5 or 
6 
7 expect(aotherperson).toBeUndefined(); <-- here .toBeUndefined is a keyword for testing
```

**Scenario 4 - Less Than Checking**

```
1 var amount = 10; 
2 var anotheramount = 12; 
3 expect(anotheramount).not.toBeLessThan(amount); <-- here .toBeLessThan is a keyword 
4 						    for testing
```

**Scenario 5 - Throw Checking**

```
 1 function checkThrow() 
 2 { 
 3 	return aVariable; 
 4 } 
 5 
 6 expect(checkThrow()).toThrow(); <-- here .toThrow is a keyword for testing
 7 
 8 function checkNotThrow() 
 9 { 
10 	return 1; 
11 } 
12 
13 expect(checkNotThrow()).not.toThrow(); 
```

For all the details of testing functions in Jasmine -

**References -**

[Jasmine Documentation](http://pivotal.github.io/jasmine/)

## Angular.js Tests with Jasmine

In current chapter we are trying to discuss the Angular.js client side testing with Jasmine Testing Framework. We have covered the testing of Client side Controller and Angular Mock Service with Jasmine Framework. Codes are commented to help understanding of the testing.

Our 2 Example Controllers are -

###### controllers.js

```
 1     // This controller returns three json elements in $scope variable
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

and

###### RTcontroller.js

In this controller we have created a service, from which data will be returned in “stocks” variable of angular $scope via $http and $q object.

```
 1     var app = angular.module('angularjstest', []); 
 2     
 3     app.controller('StockListCtrl', function($scope, stockService) { 
 4 		// Angular Controller Definition
 5                 // with service injection
 6             stockService.getStocks().then(function(data) {           
 7 		// Angular promise
 8                 $scope.stocks = data;
 9             });
10        });
11     
12     app.factory('stockService', function($http, $q) {               
13 		// Angular Service Declaration
14         return {
15             getStocks: function() {                                 
16                 var deferred = $q.defer();                          
17 			// Deferred Object Declaration
18                 $http.get('stocks.json').success(function(data) {   
19 			// Asynchronous Service calling
20                      deferred.resolve(data);
21                 }).error(function(){
22                      deferred.reject();
23                 });
24             return deferred.promise;
25          }
26        }
27     });
```

Following code is the specification file for testing which can be run with **testrunner.html**, which is default file for testing in Jasmine Framework. We have modified this file only for our example work. The source files are to be included in `<!-- include source files here...-->` section of **testrunner.html**

###### <script type="text/javascript" src="src/controllers.js"></script>

######<script type="text/javascript" src="src/RTcontroller.js"></script>

Also the spec file is to be included in `<!-- include spec files here...-->` section of **testrunner.html** ######<script type="text/javascript" src="spec/ControllerSpec.js"></script>

Now the spec file -

###### The Angular.js test spec coding -

```
 1     describe('Controller function', function() {  // Jasmine Test Suite
 2     
 3       describe('PhoneListCtrl', function() {      
 4 		// Inner Test suite for Angular Controller
 5         var scope;
 6     
 7         beforeEach(inject(function($rootScope, $controller) {  
 8 			// Data initialisation in case of Headless Browser
 9                         // $rootScope is the Angular Built-in object from which
10 	                // angular scope will be created.
11 	  scope = $rootScope.$new();
12           var ctrl = $controller(PhoneListCtrl, {$scope: scope}); 
13 			// Controller object will be created for the
14                         // PhoneListCtrl controller in testing environment.
15         }));
16     
17         it('should create "phones" model with 3 phones', function() { 
18           expect(scope.phones.length).toBe(3); 
19 		// Individual Test Component - refer to source javaScript code
20 		// of the above Angular Controller
21         });                                    
22       });
23     
24       describe('StockListCtrl', function() {
25          var scope;
26          var $httpBackend, $rootScope, createController, _stockService;
27     
28     	 beforeEach(function () {
29                 module("angularjstest");   // Angular Module Initialisation
30             }); 
31     
32         beforeEach(inject(function($rootScope, $controller, 
33 					$injector ,stockService) {
34     
35     	  $httpBackend = $injector.get('$httpBackend'); 
36 		// Mock object for Testing Environment with $http service
37     	  $httpBackend.when('GET', 'stocks.json')
38 			.respond([{"Product": "REL", "BBP": "10", 
39                                    "BSP": "10.2", "LTP": "10.1"}]); 
40                         // Send the mock data by creating $httpbackend service
41     	  $rootScope = $injector.get('$rootScope');
42     	  scope = $rootScope.$new();
43     	  var $controller = $injector.get('$controller'); 
44 		// Creating the Angular Controller for Test Environment
45     	  _stockService = stockService;
46     	  spyOn(stockService, 'getStocks').andCallThrough(); 
47 			// Calling of the 'getStocks' method is ensured by spyOn
48     	  createController = function() { // Method to create controller
49                   return $controller('StockListCtrl', 
50 			{'$scope' : scope }, {stockService : _stockService});
51               }; 
52     
53         }));
54     
55         it('should call getStocks', function() {
56     	  var controller = createController();
57     	  expect(_stockService.getStocks).toHaveBeenCalled(); 
58 				// Service method is called or not
59     	  $httpBackend.flush();
60         });
61         it('should have more than 0 stock', function() {
62     	  var controller = createController();
63     	  $httpBackend.flush();
64               expect(scope.stocks.length).not.toBe(0); 
65 		// some stock data is expected to be returned from here -
66                 // We have created mock service for this above.
67     
68         });
69       });
70     });
```

So in the current chapter, we have covered testing of Angular Controller with and without Angular Services.

## jQuery Plugin under Angular.js Directive - a more clean html approach

![angular-jquery-image-slider](images/00004.jpeg)

angular-jquery-image-slider

In previous chapter, we have described about building a jQuery Plugin from scratch. Here we will describe a clean approach to make clean html with Angular.js Directive which will wrap the functionality of the above JQuery plugin. This plugin is already configurable for the image moving direction - left, right, up and down.

###### Now what is Angular.js Directive ?

###### Directly from angularjs.org -

> Directives are a way to teach HTML new tricks. During DOM compilation directives are matched against the HTML and executed. This allows directives to register behavior, or transform the DOM.

In a more simple way what we have understood that, we can introduce new html tags binding with our rules, in web page, under Angular.js wrapper. Also we can always separate and minimise the use of javascript code in a html page. Another thing that we have learned from this exercise is, we can use existing jQuery complex plugins with minimal tweaks within Angular.js framework wrapper. Now we should go to the code. As our previous articles, we will comment within the codes of HTML and Javascript.

###### Main HTML Code Snippet

```
 1     <div class="example" >
 2         <div image-slider slider-id ="'slider'" time-interval="3000" 
 3 							my-direction="'down'" >
 4         <!-- imageSlider is our angular directive name -->
 5         <!-- sliderId, timeInterval, myDirection are three variables 
 6 				for the UL id on which the plugin will run, -->
 7         <!-- timeInterval after which the plugin will run and the direction 
 8 						on which the images will slide -->
 9             <ul id="slider">
10                 <li><img src="Chrysanthemum.jpg" alt="" width="480" height="310"/>
11 							<p>This is first slide</p></li>
12                 <li><img src="Desert.jpg" width="480" height="310" 
13 						alt="" /><p>This is second slide</p></li>
14             </ul>
15         </div>
16     </div>
```

###### Code in Angular way

```
 1 angular.module('AngularSlider', [])
 2 .directive('imageSlider', function () { // Angular Directive Declaration
 3      return {
 4          restrict: 'A',                 // The Directive is with Attribute
 5          scope: {
 6              timeInterval: '=',         // three initializer variables
 7              myDirection: '=',
 8              sliderId: '='
 9          },
10          link: function (scope, elem, attrs) {
11              $('#'+scope.sliderId).plainSlider(scope.myDirection,
12 							scope.timeInterval);
13              // calling the jQuery plugin method in link function 
14 	     // for the particular DOM Element
15          }
16      }
17 });
```

The particular jquery plugin related information, which is used here, can be found in `"Simple jQuery Image Slider Plugin with minimal effects"` chapter. Our code can be found in [Github](https://github.com/piyasde/angulardicective).

###### References :

1> [http://docs.angularjs.org/guide/directive](http://docs.angularjs.org/guide/directive)

2> [http://www.befundoo.com/university/tutorials/angularjs-directives-tutorial/](http://www.befundoo.com/university/tutorials/angularjs-directives-tutorial/).

## D3.js in Angular.js Directive - a relief from D3 svg code in HTML Page

We have came through **D3.js** coding for Graph generation in our projects. To me personally, this coding is somewhat complex for startup programmers. Recently I am going through learning **Angular.js** and **Angular Directive**. So I had a thought to introduce an angular directive which will wrap the complex functionality of D3.js. So here is the result - this chapter - **creating a bar chart through Angular Directive with the help of D3.js**.

I have learned the D3.js code from - [http://bl.ocks.org/mbostock/3885304](http://bl.ocks.org/mbostock/3885304) Also previous chapter is our documentation on making the Angular Directive.

###### First - the Bar Chart Picture -

![AngularD3BarGraph](images/00003.jpeg)

AngularD3BarGraph

###### Now the Commented code snippet in HTML -

```
 1 <body>
 2 	<div id="d3bar" angulard3-bar-graph datajson="'sample.json'" 
 3 	       xaxis-name = "'Year'" 
 4 	       xaxis-pos = "905"  
 5 	       yaxis-name = "'Frequency'" 
 6 	       yaxis-pos = "6" 
 7 	       d3-format= "'.0%'" >
 8 	<!-- angular directive is angulard3-bar-graph -->
 9 	<!-- directive variables are xaxis-name,yaxis-name,xaxis-pos,yaxis-pos
10 	,y axis data format(d3-format)
11 	and finally the datajson variable which is holding the external data source -->
12 	</div>
13 </body>
```

And below is

###### Angular directive which wrapped d3.js code for Bar Graph

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

The Code can be downloaded from [Github](https://github.com/piyasde/d3).

## Simple Bar Graph in Angular Directive with d3.js and Prototype.js – a Javascript Class based Approach

![AngularD3BarGraph](images/00003.jpeg)]

We are recently working to convert our client side javascript code to convert in Object Oriented approach. So we have gone through learning process of javascript OOP and written our previous chapter - Javascript in OOP Way – some interesting study and while learning the d3.js graph creation, we have written D3.js in Angular.js Directive – a relief from D3 svg code in HTML Page.

Now we are trying to separate the d3.js code to put in Javascript Framework and for that we have taken the prototype.js to make the javascript classes for the d3.js code separation. We have made the Angular Directive and seperated the d3.js related code through class creation in prototype.js and accessed the the class instance related code in Angular Directive Link Functon. So what we have done really in HTML ?

###### 1> Added the angular.js,prototype.js, d3.js in the HTML Page and the reference of the d3 related javascript class

```
1 <script type="text/javascript" src="js/prototype.js"></script>
2 <script src="js/barGraphProto.js"></script>
3 <script src="http://d3js.org/d3.v3.min.js"></script>
4 <script type="text/javascript" 
5 	src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.6/angular.min.js">
6 </script>
```

###### 2> Put the the d3.js related Angular Directive in HTML -

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

###### 3> The Code in Angular Directive -

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

###### 4> The d3 related bar graph code -

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

[Here](http://www.phloxblog.in/wp-content/uploads/2013/07/angularProto.zip) is the code for this for reader’s interest. We will reuse the d3 related javascript class code in Angular.js Directive in next chapter.

## Simple Bar Graph in Angular Directive with d3.js and Prototype.js – Element based Directive Definition

![AngularD3BarGraph](images/00003.jpeg)

AngularD3BarGraph

We are recently working to convert our client side javascript code to convert in Object Oriented approach. So we have gone through learning process of javascript OOP and written our previous chapter - `Javascript in OOP Way -- some interesting study` and while learning the d3.js graph creation, we have written `D3.js in Angular.js Directive -- a relief from D3 svg code in HTML Page`.

We have separated the d3.js code to put in Javascript Class and for that we have taken the prototype.js to make the javascript classes for the d3.js code separation. So - `Simple Bar Graph with d3.js and Prototype.js - a Javascript Class based Approach` is one of our previous chapter. The current chapter is a variation of Angular Directive - it is a Element based Directive.

**Example -**

In HTML we want to introdroduce new Tag Element like **<bargraph />.** We have made the Angular Directive and seperated the d3.js related code through class creation in prototype.js and accessed the the class instance related code in Angular Directive **Complie** Functon. So what we have done really in HTML ?

###### 1> Added the angular.js,prototype.js, d3.js in the HTML Page and the reference of the d3 related javascript class

```
1      <script type="text/javascript" src="js/prototype.js"></script>
2      <script src="js/barGraphProto.js"></script>
3      <script src="http://d3js.org/d3.v3.min.js"></script>
4      <script type="text/javascript" 
5 	src="https://ajax.googleapis.com/ajax/libs/angularjs/1.0.6/angular.min.js">
6      </script>
```

###### 2> Put the the d3.js related Angular Directive in HTML -

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

###### 3> The Code in Angular Directive -

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

#####4> The d3 related bar graph code -

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

[Here](http://www.phloxblog.in/wp-content/uploads/2013/07/angularElementProto.zip) is the code for this for reader’s interest.

## Creating Google Chrome Extension to add a Custom RSS Feed Reader

We had made a RSS Feed reader which is capable to read multiple RSS Feed in same page using a tab navigation. We had used Bootstrap.js and CSS to end the Application with a standard UI from developer perspective. Next we have tried to make this RSS Feed Reader available as Google Chrome Extension. The idea behind this was - to make all current related news to us to be readily available when we connect internet and open the Google Chrome Browser and click on an icon. Below is a pictorial representation of the Feed Reader.

![RSS Feed Reader](images/00005.jpeg)

RSS Feed Reader

We have used some of the technologies and tricks to make this. Below is a listing -

**1> We had made a custom RSS Feed Reader in PHP**

**2> We have integrated bootstrap.js and css to make a standard UI with Tab Navigation**

**3> We have made our reader Cross Domain Ajax Request enabled**

**4> We have made a Google Chrome Extension**

**5> We have used Google Font to decorate Content**

**6> We have given permission to the Google Chrome Extension to reed the feed from external url**

To refer point no 1, 2 and 3 our reader should read [Creating RSS Feed Reader and Decorating with Bootstrap.js and CSS](http://www.phloxblog.in/creating-rss-feed-reader-decorating-bootstrap-js/).

Now to make a Chrome Extension, reader should read [Getting Started: Building a Chrome Extension](https://developer.chrome.com/extensions/getstarted.html).

###### A little decoration to UI - using the Google Font, we have used -

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

###### Another note to reader - after reading the [Getting Started: Building a Chrome Extension](https://developer.chrome.com/extensions/getstarted.html), we will know about the configuration file - manifest.jon.

Now to make any external content from internet to be available in Chrome Extension, we have to give permission for this in manifest.json.

###### Here the permission code snippet is -

```
1     ....
2       "permissions": [
3         "http://phloxblog.in/"
4       ],
5     ....
```

as we have got the external feed content via our hosted server.

**Coding :**

Php code for server-side can be downloaded [here](http://www.phloxblog.in/wp-content/uploads/2013/06/rss.zip). Also the complete code for Google Chrome Extension is available [here](http://www.phloxblog.in/wp-content/uploads/2013/06/ExperimentGC.zip).

So here we have made the extension available in unpacked version, with which the reader should experiment and make the extension more useful with his/her own thoughts.

## Task List with Angular.js, HTML5 Local Storage and Decorate with Bootstrap in Google Chrome Extension

We had an idea to add a Daily Task List as Google Chrome Extension with News Feed Reader related to daily interested news to us. So here is a Chrome Extension made with following integrated tools -

##### 1>Angular.js

to make the Task List and Task Adding Functionalities.

###### 2> HTML5 Localstorage

to keep the task data in temporary storage and serve those from there.

###### 3> Integrated our Personal Feed Reader

to make the useful news available to us.

###### 4> Made a Bare minimum Google Chrome Extension

to be available in Google Chrome Browser.

Here are our previous posts related to -

**HTML5 and LocalStorage -**

A. [HTML5 LocalStorage and Json Object – Some Operations](http://www.phloxblog.in/html5-localstorage-json-object-operations/)

**RSS Feed Reader -**

B. [Creating RSS Feed Reader and Decorating with Bootstrap.js and CSS](http://www.phloxblog.in/creating-google-chrome-extension-add-custom-rss-feed-reader/)

**Integration of Feed reader in Google Chrome Extension -**

C. [Creating Google Chrome Extension to add a Custom RSS Feed Reader](http://www.phloxblog.in/creating-google-chrome-extension-add-custom-rss-feed-reader/)

[Here](http://www.phloxblog.in/wp-content/uploads/2013/06/Experiment1.zip) is our code base for the Work with Angular.js, HTML5 locastorage and RSS Feed Reader.

Also reader can find the code in [github](https://github.com/piyasde/Experiment). Also [here](http://www.phloxblog.in/wp-content/uploads/2013/06/Experiment19032013.zip) is our Google Chrome Extension.

Reader can have it live in [Google Chrome Webstore](https://chrome.google.com/webstore/detail/task-list-and-feed-reader/igiphijnjbhhpkbdgmjdlfdoacojddig).

We have discussed the part of making rss feed reader, Bootstrap integration and making google chrome extension in earlier mentioned articles in this post. Below is the picture for the Extension -

![Task List and Feed Reader](images/00006.jpeg)

Task List and Feed Reader

Here we mainly show and discuss about **Angular.js and HTML5 localstorage integration**.

We will comment inline within the code to understand the work.

**HTML templates in Angular.js** ========================

To show the list of Tasks, the codes are (listtodo.html) -

```
 1 <form ng-submit="clear()">  
 2 <!-- On submit of this form clear method in controller will fire -->
 3 <div style="float:right;"><center><button type="submit" >
 4 			Clear Tasks</button></center></div>
 5   <ul style="list-style-type:none">
 6      <li ng-repeat="todo in todos" > 
 7 	<!-- Our favourite repeater functionality from angular.js -->
 8         <p>{{todo.task}}</p> 
 9 	<!-- Task element in todo object will be shown here. It is a Json Element -->
10      </li>
11   </ul>
12 </form>
```

###### To show the Addition of Tasks, the codes are (addtodo.html) -

```
 1 <form ng-submit="save()"> <!-- The method in controller which will save data in localstora\
 2 ge-->
 3 <fieldset>
 4   <legend>New Task</legend>
 5   <div class="control-group">
 6      <center><input type="text" placeholder="Task..." ng-model="task" 
 7 						size=50 required/></center> 
 8 	<!--Angular.js Model-->
 9   </div>
10 </fieldset>
11 <p>
12    <div><center><button type="submit" >Remember it...</button></center></div>
13 </p>
14 </form>
```

###### Main Code snippets in index.html are -

```
 1 <html lang="en" ng-app="taskslist" ng-csp=""> 
 2 <!-- enable angular.js in chrome extension (ng-csp)-->
 3 .....
 4 <div ng-controller="TaskListCtrl" > 
 5 <!-- Angular Controller which is responsible to render the data in View -->
 6 .....
 7 <div id="addtodo" class="tab-pane fade" ng-include="'views/addtodo.html'"></div> 
 8 <div id="listtodo" class="tab-pane fade active in" ng-include="'views/listtodo.html'"></di\
 9 v>
10 <!-- adding the angular templates with ng-include -->
```

###### Now the main code snippet in controller -

```
 1       /* Controllers */
 2       function TaskListCtrl($scope,$location) {
 3     
 4         $scope.save = function() {
 5               var tmpVar = {}; 
 6     	  tmpVar.task = this.task; 
 7 		// new json object to get the data from angular.js model
 8     	  this.task = '';
 9     	  $scope.todos.push(tmpVar); 
10 		// pushing the json object in array in angular $scope variable
11     	  localStorage.setItem("todoList", JSON.stringify($scope.todos)); 
12 			// saving array in html5 local storage
13     	  console.log($scope.todos.length);
14     	  $scope.list();
15         };
16     
17         //Data Load
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
28 			// get value from localstorage
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
40                       // clear all value in particular storage variable in HTML5 localstor\
41 age
42     	};
43     
44        $scope.list(); 
45 	// whenever we are through this angular controller, we will fire the list method
46        if(!$scope.$$phase) {
47     	$scope.$apply(); // apply all changes in angular $scope
48        }
49     }
```

## Preliminary Concepts of Graph Database

We will try to clarify the Concepts of Graph Database in context of neo4j – a graph database in our posts one-by-one.

So below is our first post which describes the quick start up concepts of Graph Database.

**Graph -**

A graph consists of information in Nodes which are interconnected. A Graph can consists of a single node also. A particular node can have multiple properties in it as key-value pair. Also the nodes are connected in multiple ways, which we can describe as relationship.

**Examples -**

A School information is a single node. Students and Teachers are different nodes which are connected through relationship.

Students(Nodes) study(Relationship) in School(Node).

Teachers(Nodes) teach(Relationship) in School(Node).

School has name, address, year of stablishment, accreditation etc. which can be described as Properties.

Student has name, address, year of join, class etc. which can be described as Properties.

Teacher has name, address, year of join, highest qualification etc. which can be described as Properties.

**Node -**

Nodes are every single set of entity information in a Graph.

**Examples -**

If we consider a school information system as a Graph,

School itself is a node in the School Graph.

Each Student is node in the School Graph.

Also, each Teacher is node in the School Graph.

**Relationship -**

Nodes are joined by some information – which are relationship in graph.

**Examples -**

Students study in School.

Teachers teach in School.

Here study and teach are the relationship information between nodes in a School Graph.

Labels – When nodes form a group in a graph and are identified by some information, then that information will be called label.

**Examples -**

In a school graph,

we can classify

(All Students) label for all the students in the school graph.

Again,

(5th Class Students), (6th Class Students) label can be given for respective students.

Here (All Students), (5th Class Students), (6th Class Students) can be called as sub graphs.

**Node Traversal -**

When we look for some specific information in a graph of all the Nodes, we process the information udentsin some specific pre-determined optimum way and this is called Graph Traversal.

**Examples -**

In a school graph, to have a information like “Name of the teachers who teaches the 5th Class students”,

We can traverse by

In (Paricular SChool) –>> study by –>> (5th Class Students) –>> Teached by –>> (Teachers)

Note : Above is a traversal information, which ma y be used for understanding traversal in a Graph.

**Indexes -**

When we want for a specific set of information of nodes or relationship, we put all those information in specific maps, which will be called as index.

**Examples -**

In a school graph-

We can have specific set of nodes for

(Science Subject Teachers), (Art Subject Teachers) etc. which we can put in indexes.

In next part of our posts related to Graph Database,

we will describe a Case Study where we can use a Graph Database.

Then,

We will describe the schema and information we can obtain from Graph Database through **Cypher Query** in context of **neo4j**.

### A Case Study in Graph Database in Context of Neo4j Cypher Query

We have presented here a typical case study related to graph database model.

##### Case Study for Graph Database -

**Nodes -**

Entity – **User** (Represented as Node)

Entity - **Organisation** (Represented as Node)

Entity – **Project** (Represented as Node)

Entity – **Skill** (Represented as Node)

**Relationships -**

User worked in Organisation. – (Relationship – **worked**)

User is following Oganisation – (Relationship – **following**)

User has done Projects – (Relationship – **has done**)

User has Skills - (Relationship – **has**)

User is Friend of User – (Relation - **is Friend**)

##### Diagrammatic Model for Graph Database Representation -

![Graph Database Diagram](images/00007.gif)

Graph Database Diagram

## Quick Glance at Neo4j Cypher Queries for Sample Graph Database

We have tried to show different Neo4j Cypher Queries to show different capabilities of graph database.

To start with graph database preliminary concepts, read Preliminary Concepts of Graph Database and Case Study in Graph Database in Context of Neo4j Cypher Query in previous chapters.

###### Installation -

Install Neo4J from (http://www.neo4j.org/download).

Starting Neo4j Server in Windows -

**neo4j.bat start**

Then go to browser at the address – **http://localhost:7474**

Now the cypher queries, which we have tested on the Data Console which is in relation to the mentioned model in previous chapter.

###### Creating Nodes -

**CREATE (user {entitytype:’user’, name : ‘bill’}) return user;**

**CREATE (company {entitytype:’company’, name : ‘CTS’}) return company;**

**CREATE (project {entitytype:’project’, name : ‘ABC Insurance’}) return project;**

**CREATE (skill {entitytype:’skill’, name : ‘HTML, CSS’}) return skill;**

Some of the Nodes creation examples are shown here.

###### Creating Relationships -

**START user=node(1), company=node(9) CREATE relation = user-[:WORKS_AT]->company return relation;**

**START user=node(7), company=node(9) CREATE relation = user-[:FOLLOWS]->company return relation;**

**START user=node(5), skill=node(12) CREATE relation = user-[:HAS_SKILL]->skill return relation;**

**START user=node(6), seconduser=node(7) CREATE relation = user-[:FRIEND]->seconduser return relation;**

**START user=node(6), work=node(11) CREATE relation = user-[:CURRENT_ENGADGEMENT]->work return relation;**

**START user=node(6), work=node(11) CREATE relation = user-[:CURRENT_ENGADGEMENT]->work return relation;**

**START company=node(9), project=node(11) CREATE relation = company-[:EXECUTING_UNDER]->project return relation;**

Some of the relation creation examples are shown here.

###### Removing node -

**START nullnode=node(0), DELETE nullnode;** // Delete a Node

###### Fetching Nodes and Relationships -

**start n = node(*) return n;**// See all the nodes

**start r = relationship(*) return r;** //see all the relationships

**start n = node:node_auto_index(name = ‘john’) return n;**// Selecting particular user –>Selecting Data by Indexes

**START n=node(*) WHERE has(n.name) RETURN n;** // Selecting those nodes where we have name properties

**START n=node(*) WHERE has(n.name) and (n.entitytype = ‘skill’) RETURN n;**

// Selecting nodes where entitytype = ‘Skill’

###### index –indexes

// To Get the Indexes in nodes and relationships

**START n=node(*) WHERE has(n.name) and n.name =~ ‘j.*’ return n;** //Selecting nodes from indexes where node name starts with “j”

**START n=node(*) WHERE has(n.name) and n.name =~ ‘.*j.*’ return n;** //Selecting nodes from indexes where node name contains “j”

**start n = node(6) match(n)–(x) return x;** //return all the related nodes with node 6

**start n = node:node_auto_index(name=’andrew’) match(n)–(x) return x;** //return all the related nodes with node name = ‘andrew’

**start n = node:node_auto_index(name=’andrew’) match(n)<–(x) return x;** // return all nodes which are having inbound relationship with ‘andrew’

**start n = node:node_auto_index(name=’andrew’) match(n)–>(x) return x;** // return all nodes which are having outbound relationship with ‘andrew’

// Note : Here all entitytype (skill, project, user, company) to which andrew is having outbound relationship will return

**START n=node:node_auto_index(name=’andrew’) MATCH (n)-[:WORKS_AT]->(x) RETURN x;**

//Match by relationship type and outbound nodes

**START n=node:node_auto_index(name=’linda’) MATCH (n)-[:FRIEND]->(x) RETURN x;**

// Here result will be ‘andrew’ who is outbound relationship to ‘linda’

**START n=node:node_auto_index(name=’linda’) MATCH (n)<-[:FRIEND]-(x) RETURN x;**

// Here result will be ‘john’ for whom ‘linda’ is outbound relationship

**START n=node:node_auto_index(name=’andrew’) MATCH (n)-[r:WORKS_AT]->() return r;**

// Match by relationship type and use an identifier

**START a=node:node_auto_index(name=’andrew’) MATCH (a)-[:WORKS_AT]->(b)<-[:WORKS_AT]-(c) return a,b,c**

//return Multiple relationships

// Here all the people, who are working in ‘IBM’ will be returned, as ‘andrew’ is working in ‘IBM’

**START n=node(*) WHERE has(n.name) and (n.name =~ ‘john.*’) RETURN n;**

// Where condition in the Query and ‘property exists in node’ clause and Like clause

**START n=node(*) WHERE n.entitytype? = “skill” RETURN n;**

// Default true for nodes if property is missing and all other matching nodes

**START n=node(*) WHERE n.entitytype! = “skill” RETURN n;**

// Only for nodes with matching nodes. Note : “!=” and “! =” are not same

**START persons=node(*), company=node:node_auto_index(name=’IBM’) WHERE has(persons.name) and (persons.entitytype=’user’) and not(persons–>company) RETURN persons;**

// Those persons will be returned who are not related to ‘IBM’riend

**START persons=node(*), company=node:node_auto_index(name=’IBM’) WHERE has(persons.name) and (persons.entitytype=’user’) and (persons–>company) RETURN persons;**

// Those persons will be returned who are has relation to ‘IBM’ (here note the ‘WORKS_AT’ and ‘FOLLOWS’ relationship)

**START persons=node(*), company=node:node_auto_index(name=’IBM’) WHERE has(persons.name) and (persons.entitytype=’user’) and (persons-[:WORKS_AT]->company) RETURN persons;**

// Those persons will be returned who are has relation to ‘IBM’ (Only ‘WORKS_AT’ relationship)

**START me=node:node_auto_index(name=’andrew’) MATCH me–>friend where (friend.entitytype=’user’) RETURN count(friend),friend;**

// Return only those users who are outbound to ‘andrew’

**START me=node:node_auto_index(name=’andrew’) MATCH me<–friend<–friend_of_friend where (friend_of_friend.entitytype=’user’) RETURN count(friend_of_friend),friend_of_friend;**

// This is a ‘friend of friend’ relationship. Here ‘John’ is friend of ‘linda’ and ‘linda’ is friend of ‘andrew’

**START me=node:node_auto_index(name=’andrew’),company=node:node_auto_index(name=’CTS’) MATCH me<–friend<–friend_of_friend where (friend_of_friend.entitytype=’user’) and (friend_of_friend-[:WORKS_AT]->company) RETURN count(friend_of_friend),friend_of_friend,company;**

// This is a ‘friend of friend’ relationship. Here ‘John’ is friend of ‘linda’ and ‘linda’ is friend of ‘andrew’ and he is returned as he is working in ‘CTS’

**START me=node:node_auto_index(name=’andrew’),company=node(8,9) MATCH me<–friend<–friend_of_friend where (friend_of_friend.entitytype=’user’) and (friend_of_friend-[:WORKS_AT]->company) RETURN count(friend_of_friend),friend_of_friend,company;**

// Same Query of above for selection of all the companies

**start n = node:node_auto_index(name=’UI Restructuring’) match n<–x<-[:WORKS_AT]-x1 return x1;**

// Here the project is done in ‘IBM’ and nodes – ‘x1′ are working in the company;

**start n = node:node_auto_index(name=’UI Restructuring’) match n<–x<-[:FOLLOWS]-x1 return x1;**

// Here the project is done in ‘IBM’ and nodes – ‘x1′ are following the company;

**START n=node:node_auto_index(name=’jude’) MATCH (n)-[:WORKS_AT]->x<-[:FOLLOWS]-x1 return x1;**

// return all the nodes which follows the company on which ‘jude’ is working;

**START n=node:node_auto_index(name=’CTS’) MATCH (n)<-[r:WORKS_AT]-() RETURN type(r), count(*);**

// How much nodes are in the graph who are with ‘WORKS_AT’ in ‘CTS’

**START n=node(*) RETURN distinct(n.entitytype?);** // Select distinct entity types

**START person=node:node_auto_index(‘name: *’) MATCH person-[?:WORKS_AT]->company where person.entitytype =’user’ RETURN person.name**

// return all the nodes with ‘WORKS_AT’ relationship

**START begin = node(4), end = node(7) MATCH p = begin -[*]-> end foreach(n in nodes(p) : SET n.network = true);**

// Updating connecting nodes and example of loop in cypher query

**START begin = node(4), end = node(7) MATCH p = begin -[*]-> end return *;** // showing the result of updation in connecting nodes

**START n=node(1) MATCH p=n-[*..]->b WHERE ANY(x in nodes(p) WHERE x.network? = true) RETURN p;**

// Example of Predicates

References :

1> (http://docs.neo4j.org/refcard/1.9/)

2> (http://java.dzone.com/articles/10-caveats-neo4j-users-should)

3> (http://docs.neo4j.org/chunked/milestone/cypher-query-lang.html)

We have shown some of the queries, which we can use in practical applications in Graph Database. And as this is a new type of NoSql Database, the above post is an introduction for some of the neo4j cypher query examples from our end.

## Develop Web Application with Node.js, Express.js REST Service and Neo4j (neo4j-js module)

This article is a proof of concept towards make a web application with Javascript based Web Server with Node.js and Neo4j.

To make this possible, we have selected -

**1> Node.js for server side development**

**2> Rest based web service creation with express.js**

**3> Graph Database – Neo4j**

**4> Node.js Neo4j Module Extention (neo4j-js)**

We have created a Proof of Concept with Javascript based web server, where we have focused on dealing with Neo4j(Graph Database) with javascript based framework Node.js.

We have taken help of the Neo4j-js module, which are discussed in Neo4j Site and the [Github project contribution from Bret Copeland](https://github.com/bretcope/neo4j-js).

We have taken reference Data Model of Neo4j Graph Database for this application from our knowledge from previous chapter on Neo4j.

First is the architechture diagram -

![Architechture](images/00008.jpeg)

Architechture

So here are the steps -

###### Installation -

1.  Download and install Node.js from [here](http://nodejs.org/download/).
2.  To Develop the application we need to install Neo4j-js module for Node.js

    Command – **npm install neo4j-js** (should be connected to internet)

3.  We need to install express.js for node.js

    Command – **npm install express** (should be connected to internet)

4.  We need to install http-status

    Command – **npm install http-status** (should be connected to internet)

###### Configuration Code -

Now, we will try to describe the code portion -

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path"),
4     HTTPStatus = require('http-status'); // To return http status for error codes
5 
6 var config = require('./config');
```

Here we have initialised the express.js within javascript variables in respect of Node.js concept.

We have introduced another js file – config.js to put all the neo4j configuration related information.

```
1 var app = express();
```

Here we have initialised the express web server in app variable.

```
1 var neo4j = require('neo4j-js');
```

Here we have made the Node.js Neo4j-js module available .

```
1 var neo4jurl = process.env.NEO4J_URL ;
2 neo4jurl = neo4jurl +'/db/data/';
```

Here the Neo4j Database server url is set from configuration file.

```
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

Here all the query variables are set with Neo4j Cypher Queries.

```
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

Here we have made the configuration related to express.js

**Rest Services Code -**

```
1 app.get('/api', function (req, res) {
2   res.send('Our Sample API is up...');
3 });
```

Here we have made our first REST based web service and tested whether the express.js is up.

Our sample api will be - **http://127.0.0.1:1212/api** (Get Method)

```
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

Here we have created REST api to get user information from Neo4j Nodes Collection and so have done through Neo4j-js Extention Library. We have made a query for **‘Friend of Friend’** in Cypher Query Language.

More information about Neo4j Cypher query can be found in Previous Chapter - Neo4j Cypher Queries for Sample Graph Database.

Our sample api will be - **http://127.0.0.1:1212/friendoffriend/andrew** (Get Method)

```
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

Here we have inserted a node in database through cypher query via REST web service calling.

Our sample api will be - **http://127.0.0.1:1212/insertuser/anotheruser** (Get Method)

```
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

Our sample api will be -**http://127.0.0.1:1212/allrelations/andrew** (Get Method)

Above we have taken another Query Example from Node.js with Query, Parameter and Callback function.

```
1 // Launch server
2 app.listen(1212);
```

We have made the server to listen at 1212 port.

To run the application, we should use - **node neo4jtest.js** from command shell.

## A Quick Primer on MongoDB

We have used some of useful commands in MongoDB in our project work. Below is the quick reference of MongoDB commands which can be executed from MongoDB shell. We have tested all the commands from mongodb shell with test data examples.

We can download mongodb from [here](http://www.mongodb.org/downloads).

To start mongodb

we should use -

**mongod –dbpath <<Our MongoDB Data Directory>>**

Now to start the Database from shell -

**mongo** // to satrt the db

**db** // to test current database

**show dbs** // to show all the databases

**use userdb** // to change to database or to create a new database

// Now to insert data in Collection

**user = { username : “firstuser”,password:”firstuser”,email:”firstuser@gmail.com” }** // prepare the data

**db.users.insert(user);** // insert the data in things collection

**show collections;** // to see all the collections in mongodb, here we should view the collection “users” which we have previously created

**db.users.find();** // to see all the documents in the collection

**db.users.find(0);** // find collection by index

**db.users.find({username:”firstuser”});** // find doucment in collection by json elements

//Working with cursors in json -

```
1 var c = db.users.find();
2 while ( c.hasNext() ) printjson( c.next() )
```

// CRUD Operation -

// Insertion of Data

**user = { username : “firstuser”,password:”firstuser”,email:”firstuser@gmail.com” }** // prepare the data

//Below command can be used to insert with “_id” or without “_id”

**db.users.insert(user);** // insert the data in things collection.

//To insert data without “_id” field

**db.users.save({username:”thirduser”,password:”thirduser”,email:”thirduser@gmail.com”});**

**db.users.find();** // Confirming the operation

// To insert data in collection with “_id” field if the “_id” not found

**db.users.save({_id:10,username:”fourthuser”,password:”fourthuser”, email:”fourthuser1@gmail.com”});**

// To update data in collection with “_id” field if the “_id” found

**db.users.save({_id:10,username:”fourthuser1″,password:”fourthuser1″, email:”fourthuser1@gmail.com”});**

// Same operation update with upsert flag i.e. if data found with “_id” // then update operation else insert operation // follow the opetation – if username with “fifthuser” is found // then update operation else insert operation

###### db.users.update({username:”fifthuser”},

###### {_id:11,username:”fifthuser”,password:”fifthuser”,

###### email:”fifthhuser@gmail.com”},{upsert:true});

**db.users.find();** // data insertion should be there

###### db.users.update({username:”fifthuser”},

###### {_id:11,username:”fifthuser1″,password:”fifthuser1″,

###### email:”fifthhuser1@gmail.com”},{upsert:true});

**db.users.find();** // data updation should be there

// Select data from mongodb

**db.users.find({username: { $in: [ 10, 11 ] }});** **db.users.find({username: { $in: [ “firstuser”, “seconduser” ] }});**

// A query cursor with find operation -

```
1 var myCursor = db.users.find( { username: /.*user.*/ } );
2 myCursor.forEach(printjson);
```

// Update field in document // Set a new field

**db.users.update({ _id: 10 },{$set: { ‘username’: ‘sixthuser’ },});** **db.users.update({ _id: 10 },{$set: { ‘useraddress’: ‘sixthuser address’ },});** **db.users.find();**

// Unset a field in the document

**db.users.update({ _id: 10 },{ $unset: { useraddress: ‘sixthuser address’ } });** **db.users.find();**

// Remove document from collection

**db.users.remove( { ‘username’ : ‘fifttuser1′ } );**

Reference links -

(http://docs.mongodb.org/manual/core/update/)

(http://docs.mongodb.org/manual/core/delete/)

(http://docs.mongodb.org/manual/core/read/)

(http://docs.mongodb.org/manual/core/create/)

## Single Page Application with Angular.js, Node.js and MongoDB (MongoJS Module)

Current post is a proof of concept towards make a web application with Javascript based Web Server. This technological stack is popularly known as [MEAN Stack](http://blog.mongodb.org/post/49262866911/the-mean-stack-mongodb-expressjs-angularjs-and).

To make this possible, we have selected -

###### 1> Angular.js for client side development – Single Page Application

###### 2> Cross Domain Communication in between Angular.js and Node.js

###### 3> Node.js for server side development

###### 4> Rest based web service creation with express.js

###### 5> Database – MongoDb

###### 6> Node.js MongoDb Module Extention (mongojs)

We have created a Proof of Concept with Javascript based web server, where we have focused on dealing with NoSql (MongoDB) with javascript based framework Node.js and angular.js on client side.

Our initial code can be downloaded [here](https://github.com/piyasde/NodeMongoDBAngular).

##### Architecture at a glance -

![Architechture](images/00009.gif)

Architechture

So here are the steps -

##### Installation -

###### A> Download and install Node.js from here.

###### B> To Develop the application we need to install mongojs module for Node.js

```
1     Command – npm install mongojs (should be connected to internet)
```

###### C> We need to install express.js for node.js

```
1     Command – npm install express  (should be connected to internet)
```

##### Configuration Code -

Now, we will try to describe the code portion -

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

Here we have initialised the express.js within javascript variables in respect of Node.js concept.

```
1 var app = express();
```

Here we have initialised the express web server in app variable.

```
1 var databaseUrl = "sampledb"; 
2 var collections = ["things"]
3 var db = require("mongojs").connect(databaseUrl, collections);
```

Here we have made the connection to the mongodb database using the Node.js mongojs module extension library.

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

Here we have made the configuration related to express.js

##### Rest Services Code -

```
1 app.get('/api', function (req, res) {
2   res.send('Our Sample API is up...');
3 });
```

Here we have made our first REST based web service and tested whether the express.js is up.

Our sample api will be - **http://127.0.0.1:1212/api** (Get Method)

```
 1 app.get('/getangularusers', function (req, res) {
 2 	res.header("Access-Control-Allow-Origin", "http://localhost");
 3 	res.header("Access-Control-Allow-Methods", "GET, POST");
 4         // The above 2 lines are required for Cross Domain Communication
 5         // (Allowing the methods 
 6         // that come as Cross Domain Request
 7 	db.things.find('', function(err, users) { 
 8 				// Query in MongoDB via Mongo JS Module
 9 	if( err || !users) console.log("No users found");
10 	  else 
11 	{
12 		res.writeHead(200, {'Content-Type': 'application/json'}); 
13 						// Sending data via json
14 		str='[';
15 		users.forEach( function(user) {
16 			str = str + '{ "name" : "' + user.username + '"},' +'\n';
17 		});
18 		str = str.trim();
19 		str = str.substring(0,str.length-1);
20 		str = str + ']';
21 		res.end( str);
22                 // Prepared the jSon Array here
23 	}
24   });
25 });
```

Here we have created another REST api to get all username from user collection and so have done the mongojs query.

Our sample api will be - **http://127.0.0.1:1212/getangularusers** (Get Method)

```
 1 app.post('/insertangularmongouser', function (req, res){
 2   console.log("POST: ");
 3   res.header("Access-Control-Allow-Origin", "http://localhost");
 4   res.header("Access-Control-Allow-Methods", "GET, POST");
 5   // The above 2 lines are required for Cross Domain Communication
 6   // (Allowing the methods that come as Cross 
 7   // Domain Request
 8   console.log(req.body);
 9   console.log(req.body.mydata);
10   var jsonData = JSON.parse(req.body.mydata);
11 
12   db.things.save({email: jsonData.email, password: jsonData.password, 
13 					username: jsonData.username},
14        function(err, saved) { // Query in MongoDB via Mongo JS Module
15            if( err || !saved ) res.end( "User not saved"); 
16            else res.end( "User saved");
17        });
18 });
```

Here we have made a POST request to create an user via REST calling.

Our sample api will be - **http://127.0.0.1:1212/insertangularmongouser** (Post Method)

```
1 // Launch server
2 app.listen(1212);
```

We have made the server to listen at 1212 port.

Now run **node appmongodbangular.js** from command shell.

##### Angular.js part -

Below is the code in Angular Controller -

```
 1 'use strict';
 2 
 3 var myApp = angular.module('myApp', []); 
 4 // Taking Angular Application in Javascript Variable
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
18   var inserturl = 'http://localhost:1212/insertangularmongouser';
19 		// URL where the Node.js server is running
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
35 	$http({ 
36 		// Accessing the Angular $http Service to send data 
37 		// via REST Communication to Node Server.
38             method: method,
39             url: inserturl,
40             data:  jdata ,
41             headers: {'Content-Type': 'application/x-www-form-urlencoded'},
42             cache: $templateCache
43         }).
44         success(function(response) {
45 		console.log("success"); // Getting Success Response in Callback
46                 $scope.codeStatus = response.data;
47 		console.log($scope.codeStatus);
48 
49         }).
50         error(function(response) {
51 		console.log("error"); // Getting Error Response in Callback
52                 $scope.codeStatus = response || "Request failed";
53 		console.log($scope.codeStatus);
54         });
55 	$scope.list();// Calling the list function in Angular Controller 
56 		      // to show all current data in HTML
57         return false;
58   };	
59 
60   $scope.list = function() {
61 	  var url = 'http://localhost:1212/getangularusers';
62 			// URL where the Node.js server is running	
63 	  $http.get(url).success(function(data) {
64 		$scope.users = data;
65 	  });
66           // Accessing the Angular $http Service to get data via 
67 	  // REST Communication from Node Server 
68   };
69 
70   $scope.list();
71 }
```

##### Angular Template and HTML

```
1  <html lang="en" ng-app="myApp">
2 .....
```

We have referred the Angular Application in above code

```
1 <body ng-controller="UserListCtrl">
2 .....
```

We have referred the Angular Controller in above code

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

We have used the ng-repeat tag to take the users data model from REST communication and shown in HTML

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

We have used the ng-submit tag to send the **user** data model from REST communication and sent to node server to save in MongoDB.

Reader can download the complete source-code in [GitHub](https://github.com/piyasde/NodeMongoDBAngular).

## Web Application with Highchart.js, Node.js, Express.js and MongoDB(Mongo-JS Module)

![HighChart](images/00010.jpeg)

HighChart

This application is another proof of concept towards make a web application for graph generation with Javascript based Web Server.

In this application we have used following tools and technologies -

###### 1. Node.js for server side development

###### 2. Rest based web service creation with express.js

###### 3\. Database – MongoDb

###### 4. Node.js MongoDb Module Extention (mongojs)

###### 5. Highchart.js for Graph generation through Asynchronous call (Ajax)

###### 6. Using Cross-Domain policy to access REST service from Node.js to Ajax Call

on dealing with NoSql (MongoDB) with javascript based framework Node.js.

Our initial code can be downloaded [here](https://github.com/piyasde/NodeMongoDBHighchart1).

##### Architecture at a glance -

![Architechture](images/00011.gif)

Architechture

So here are the steps -

##### Installation -

###### A. Download and install Node.js from [here](http://nodejs.org/download/).

###### B. To Develop the application we need to install mongojs module for Node.js

```
1     Command – **npm install mongojs** (should be connected to internet)
```

###### C. We need to install express.js for node.js

```
1     Command – **npm install express** (should be connected to internet)
```

#### Server Application

##### Configuration Code -

Now, we will try to describe the code portion -

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

Here we have initialised the express.js within javascript variables in respect of Node.js concept.

```
1 var app = express();
```

Here we have initialised the express web server in app variable.

```
1 var databaseUrl = "faodb"; 
2 var collections = ["seeds"]
3 var db = require("mongojs").connect(databaseUrl, collections);
```

Here we have made the connection to the mongodb database using the Node.js mongojs module extension library.

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

Here we have made the configuration related to express.js

##### Rest Services Code -

```
1 app.get('/api', function (req, res) {
2   res.header("Access-Control-Allow-Origin", "*"); // Configuration for Cross-Domain-Policy
3   res.send('Our Sample API is up...');
4 });
```

Here we have made our first REST based web service and tested whether the express.js is up.

Our sample api will be - **http://127.0.0.1:1212/api** (Get Method)

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

Here we have created another REST api to get price information for particular seed from seeds collection and so have done the mongojs query.

Our sample api will be - **http://127.0.0.1:1212/getseeddata/Arachide** (Get Method)

Now we have to run node appmongodbhighchart.js from command shell to start the node server.

#### Client Application

##### Code Explanation for Highchart -

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

## Real-time Data update with Angular.js, Node.js and Socket.io

Current post is a proof of concept towards make a real time web application with Javascript based Web Server with **Socket.IO** with Angular.js and Node.js. We have simulated a situation with 4 Product with their Best Buy Price, Best Sell Price and Last Trade Price.

![Illustration](images/00012.jpeg)]

To make this possible, we have selected -

##### 1> Angular.js for client side development - Application Front End

##### 2> Node.js for server side development

##### 3> Socket.IO for Server and Client Communication.

##### 4> Node.js Socket.IO module extention.

We have created a Proof of Concept with Javascript based web server Node.js, where we have focused on dealing with Socket.IO for real time application and angular.js on client side.

##### Architecture at a glance -

![Angular.js NodeJS SocketIO](images/00013.jpeg)

Angular.js NodeJS SocketIO

So here are the steps -

##### Installation -

A. Download and install **Node.js** from [here](http://nodejs.org/download/).

B. To Develop the application we need to install socket.io module for Node.js Command - **npm install socket.io **(should be connected to internet)

##### Configuration Code -

Now, we will try to describe the code portion -

```
1     var http = require('http');
2     var url = require('url');
3     var fs = require('fs');
4     
5     // use socket.io
6     var io = require('socket.io').listen(server);
```

Here we have initialised the http, url and filesystem object within javascript variables in respect of Node.js concept. Also we have initialised **socket.io **variable in the Node.js Environment.

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

In the above code, we have shown some of the important part of node application. In first section, we have written the creation of server via - `http.createServer.` Next, we are giving access to the resources from the node.js server - “**angulartableRT.html**” for the client browser. Now the server is listening on port 8001 Reader will get the whole code in GITHUB, which is linked at the end of chapter. Now the most important one is - **socket.io communication from Node.js**. We have commented below the node.js socket.io specific code.

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

Now run **node server.js** from command shell. This is our node.js specific code file. Our sample application will be -

[http://localhost:8001/](http://127.0.0.1:1212/getallusers)

##### Angular.js part -

Below is the code in Angular Controller and the Socket related code is discussed.

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

##### Angular HTML Binding

```
1      <script src="http://localhost:8001/socket.io/socket.io.js"></script> 
2      // Important to know
3      // **Access socket.io.js from Angular.js** 
4     .....
```

Below is the dynamic binding of Angular HTML with the Controller -

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

Reader can download the complete source-code in [GitHub](https://github.com/piyasde/NodeSocketIO).

## Single Page Application with Angular.js, Node.js and CouchDB (Cradle Module)

Current post is a proof of concept towards make a web application with Javascript based Web Server with CouchDB with Angular.js and Node.js.

This time we have tried with CouchDB, by definition which is from [Apache CouchDB](http://couchdb.apache.org/) site -

> Apache CouchDB™ is a database that uses JSON for documents, JavaScript for MapReduce queries, and regular HTTP for an API

To make this possible, we have selected -

###### 1> Angular.js for client side development – Single Page Application

###### 2> Cross Domain Communication in between Angular.js and Node.js

###### 3> Node.js for server side development

###### 4> Rest based web service creation with express.js

###### 5> Database – CouchDb

###### 6> Node.js Cradle Module Extention (to make communication with CouchDB)

###### 7> Making CouchDB views with Map-Reduce to fetch the data

We have created a Proof of Concept with Javascript based web server, where we have focused on dealing with NoSql (CouchDB) with javascript based framework Node.js and angular.js on client side.

Our initial code can be downloaded [here](https://github.com/piyasde/NodeCouchDBAngular).

##### Architecture at a glance -

![Architechture](images/00014.gif)

Architechture

So here are the steps -

##### Installation -

A. Download and install Node.js from [here](http://nodejs.org/download/).

B. To Develop the application we need to install mongojs module for Node.js

Command – **npm install cradle** (should be connected to internet)

C. We need to install express.js for node.js

Command – **npm install express** (should be connected to internet)

##### Configuration Code -

Now, we will try to describe the code portion -

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

Here we have initialised the express.js within javascript variables in respect of Node.js concept.

```
1 var app = express();
```

Here we have initialised the express web server in app variable.

```
1 var databaseUrl = "sampledb";
2 var cradle = require('cradle');
3 var connection = new(cradle.Connection)('http://couchadmin:couchadmin@localhost', 5984, {
4 auth: { username: 'couchadmin', password: 'couchadmin' }
5 });
6 var db = connection.database(databaseUrl);
```

Here we have made the connection to the mongodb database using the Node.js mongojs module extension library.

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

Here we have made the configuration related to express.js

##### Rest Services Code -

```
1 app.get('/api', function (req, res) {
2   res.header("Access-Control-Allow-Origin", "http://localhost");
3   res.send('Our Sample API is up...');
4 });
```

Here we have made our first REST based web service and tested whether the express.js is up.

Our sample api will be - **http://127.0.0.1:1212/api** (Get Method)

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

Here we have created another REST api to get all username from user collection and so have done the query.

##### CouchDB View Creation

This view creation is to be executed, before running the Angular Client Application to get specific set of data from couchdb.

Also a note, to run this view creation, we should put -

**[httpd]** **authentication_handlers = {couch_httpd_auth, null_authentication_handler}**

in the local.ini file of <<CouchDB Installation folder>>/etc/couchdb folder to execute this map function without being the admin user.

This particular feature has taken some time to be discovered by us.

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

Our sample api will be - **http://127.0.0.1:1212/getangularusers** (Get Method)

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

Here we have made a POST request to create an user via REST calling.

Our sample api will be - **http://127.0.0.1:1212/insertangularcouchuser**(Post Method)

```
1 // Launch server
2 app.listen(1212);
```

We have made the server to listen at 1212 port.

Now run `node appcouchdbangular.js` from command shell. This is our node.js specific code file.

References :

1.  (http://wiki.apache.org/couchdb/Setting_up_an_Admin_account)
2.  (http://guide.couchdb.org/draft/security.html)
3.  (https://github.com/cloudhead/cradle)

##### Angular.js part -

Below is the code in Angular Controller -

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

##### Angular Template and HTML

```
1 <html lang="en" ng-app="myApp">
2 .....
```

We have referred the Angular Application in above code

```
1 <body ng-controller="UserListCtrl">
2 .....
```

We have referred the Angular Controller in above code

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

We have used the ng-repeat tag to take the users data model from REST communication and shown in HTML

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

We have used the ng-submit tag to send the user data model from REST communication and sent to node server to save in CouchDB.

Reader can download the complete source-code in [GitHub](https://github.com/piyasde/NodeCouchDBAngular).

## POST requests with Google DART, Node.js and MongoDB

Current chapter is for GET and POST request handling with DART and MongoDB. We have tried to create a Proof of Concept with Javascript based web server – Node.js, where we have focused on dealing with NoSql (MongoDB) with javascript based framework Node.js and Google DART on client side.

To make this possible, we have selected -

##### 1> DART for client side development

##### 2> Cross Domain Communication in between DART and Node.js

##### 3> Node.js for server side development

##### 4> Rest based web service creation with express.js

##### 5> Database – MongoDb

##### 6> Node.js MongoDb Module Extention (mongojs)

The code can be found in [Github](https://github.com/piyasde/NodeMongoDBDART).

![Architecture at a glance](images/00015.gif)

Architecture at a glance

So here are the steps -

##### Installation -

Download and install **Node.js** from [here](http://nodejs.org/download).

B> To Develop the application we need to install mongojs module for Node.js

Command – **npm install mongojs** (should be connected to internet)

We need to install express.js for node.js

Command – **npm install express** (should be connected to internet)

##### Configuration Code -

Now, we will try to describe the code portion -

```
1 var application_root = __dirname,
2     express = require("express"),
3     path = require("path");
```

Here we have initialised the express.js within javascript variables in respect of Node.js concept.

```
1 var app = express();
```

Here we have initialised the express web server in app variable.

```
1 var databaseUrl = "sampledb"; 
2 var collections = ["things"]
3 var db = require("mongojs").connect(databaseUrl, collections);
```

Here we have made the connection to the mongodb database using the Node.js mongojs module extension library.

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

Here we have made the configuration related to express.js

##### Rest Services Code -

```
1 app.get('/api', function (req, res) {
2   res.send('Our Sample API is up...');
3 });
```

Here we have made our first REST based web service and tested whether the express.js is up.

Our sample api will be - [http://127.0.0.1:1212/api](http://127.0.0.1:1212/getallusers) (Get Method)

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

Here we have created another REST api to get all username from user collection and so have done the mongojs query.

Our sample api will be - [http://127.0.0.1:1212/getangularusers](http://127.0.0.1:1212/getallusers) (Get Method)

Now the critical part – **handling POST Request** -

We have seen the request is coming in server with two parts – one is **HTTP OPTIONS** method and another is **HTTP POST** Method.

The code for these are given below -

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

and the POST method code in node.js -

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

Here we have made a POST request to create an user via REST calling.

Our sample api will be – http://127.0.0.1:1212/insertdartmongouser(Post Method)

```
1 // Launch server
2 app.listen(1212);
```

We have made the server to listen at 1212 port.

Now run **node appmongodbdart.js** from command shell.

##### DART part -

Below is the code in DART source code -

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

References which are really helpful to write this solution -

https://gist.github.com/nilcolor/816580

http://stackoverflow.com/questions/17689986/jquery-ajax-sending-both-options-and-post-how-to-handle-with-express-js-node-j

http://blog.frankgrimm.net/2010/11/howto-access-http-message-body-post-data-in-node-js/

##### DART Code Reference and HTML

```
 1 <!DOCTYPE html>
 2 <html>
 3     <head>
 4         <meta charset="utf-8">
 5         <title>Users</title>
 6         <link rel="stylesheet" href="<<css file reference>>">
 7     </head>
 8     <body>
 9          <h1>All Users</h1>
10          <button id="getUsers">Get Users</button>
11          <div>
12               <ul id="userList">
13               </ul>
14          </div>
15          <div>
16              <h1>Enter User :</h1>
17              <form name="dartform" id="dartform" method="POST" 
18 					action="http://127.0.0.1:1212/insertdartmongouser">
19                   Name : <input type="text" name ="username" id="usernameid" value="" />
20                   Password : <input type="text" name ="password" id="passwordid" value="" \
21 />
22                   Email : <input type="text" name ="email" id="emailid" value="" />
23                   <button id="saveUser" >Save</button>
24              </form>
25          </div>
26          <script type="application/dart" src="users.dart"></script> <!--Dart file referenc\
27 e -->
28          <!-- for this next line to work, pubspec.yaml file must have a dependency on 'bro\
29 wser' -->
30          <script src="packages/browser/dart.js"></script>
31     </body>
32 </html>
```

We have used the dart asynchronous code to send the user data model from REST communication and sent to node server to get data in MongoDB.

Reader can download the complete source-code in [GitHub](https://github.com/piyasde/NodeMongoDBDART).

## Node.js Unit Testing with Should.js

One of node.js unit testing javascript library is should.js. After having node.js in machine, we have to install should.js through npm(node package manager).

To install should.js we need to run in terminal -

**npm install should**

To enable should.js in any given javascript file, we have to include -

**require(‘should’);**

Some of the testing which are one-liner -

Boolean variable functionality testing -

```
 1 true.should.be.ok;
 2 
 3 false.should.not.be.ok;
 4 
 5 true.should.be.true;
 6 
 7 '1'.should.not.be.true;
 8 
 9 false.should.be.false;
10 
11 ''.should.not.be.false;
```

Checking array functionalities -

```
1 [].should.be.empty; // Array is empty
2 
3 [1,2,3].should.eql([1,2,3]); // Array contains same values as expected
4 
5 [1, 2, 3].should.have.length(3); // Array length checking
6 
7 [1,2,3].should.containEql(1); // The Array contains value as expected
8 
9 [].should.be.an.instanceOf(Array); // Instance of an array
```

Checking of some string functionalities -

```
1 ''.should.be.empty; // Empty String
2 
3 'foobar'.should.endWith('bar'); // String end with some expected string
4 
5 'foobar'.should.not.endWith('foo'); // String should not end with some expected string
6 
7 'test'.should.equal('test'); // String equality checking
```

Checking of some number functionalities -

```
1 (4).should.equal(4);
2 
3 (10).should.be.above(5);
4 
5 (15).should.be.within(10, 15);
6 
7 (10).should.not.be.below(5);
```

Undefined and Infinity checking -

```
1 (undefined + 0).should.be.NaN;
2 
3 (1/0).should.be.Infinity;
```

JSON functionalities checking -

```
 1 ({ foo: 'bar' }).should.eql({ foo: 'bar' }); // JSON Equality checking
 2 
 3 ({}).should.be.an.Object; // An Object
 4 
 5 var jsonVar = {a:1, b:2}; 
 6 
 7 jsonVar.should.have.property('a'); // JSON Property Checking
 8 
 9 var obj = { foo: 'bar', baz: 'raz' }; 
10 
11 (obj).should.containEql({ foo: 'bar', baz: 'raz' }); // JSON contains the expected value
12 
13 obj.should.have.keys('foo', 'baz'); // JSON has the keys
14 
15 obj.should.have.keys(['foo', 'baz']);
```

Function should throw the error -

```
1 (function(){
2   throw new Error('fail');
3 }).should.throw();
4 
5 var user = {
6     name: 'tj'
7 };
8 
9 user.should.have.property('name', 'tj');
```

To test functionalities independently with ‘Describe’, we have to intstall automatic test runner. Here **mocha** is a automatic test runner and it will run the tests and show the results in console.

Now we need to install mocha -

##### npm install -g mocha

Now the function for Testing -

```
1 function sumTwoNumbers(firstNum,secondNum)
2 {
3 	return (parseInt(firstNum) + parseInt(secondNum));
4 }
```

To test this function, we need to run -

**mocha ourfilename.js**

Here ourfilename.js is supposed to be the name for the test case file.

## Developing Java REST web applications with Backbone.js

Recently in our J2ee based web application development, we had explored Javascript MVC frameworks to develop structured User Interface Development. Within javascript frameworks, we have found sufficient documentation for Backbone.js to develop sample Proof of Concept with J2ee based Application Back End.

We are writing post as we have not found a full-fledged Java based web application with backbone.js as UI development tool in Web. While working on the POC, we have changed codes in backbone.js section.

We have learned the where-about from ***Backbone.js Wine Cellar Tutorial — Part 2: CRUD*** by **Christophe Coenraets** and used his sample POC to develop a J2ee web application with Backbone.js as web tier development framework. The main Application credit goes to him.

We have uploaded the Sample Application in GitHub (here is the Link).

Now below is the basic understanding for the overall project -

The J2ee Project is based on java jersey REST based framework. The database schema is attached in the project source code, which is named - *cellar.sql*

**Development environment -**

1.  Database – MySql
2.  Rest based Web Services Development – Java Jersey.
3.  UI Development – Backbone.js

**Deployment Environment -**

1.  Apache Tomcat 7 (We have tested on it.)

We are trying to give the concepts and code snippet for both Server side development and Client Side Development below.

### Server Side -

A. *ConnectionHelper.java* – it is used for making connection with MySql Database.

B. *Wine.java* - it is used as simple POJO class for the table in database.

C. *WineDAO.java* – it is used to write JDBC related codes for insert/update/delete/select in the MySql Table. All the DB manipulation methods are written here.

D. *WineResource.java* – Important Class related to REST API Based Web Services. Method Signatures are given below -

```
 1 @GET @Path("wines")
 2 @Produces(MediaType.APPLICATION_JSON) 
 3 public List findAll() {
 4 
 5     // to fetch all data from DB
 6 
 7 }
 8 
 9 
10 @GET @Path("search/{query}")
11 @Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
12 public List<Wine> findByName(@PathParam("query") String query) {
13    // to fetch particular data from DB on basis of product name.
14 
15 
16 }
17 @GET 
18 @GET @Path("{id}")
19 @Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
20 public Wine findById(@PathParam("id") String id) {
21 	//to fetch particular data from DB on basis of ID.
22 }
23 
24 
25 @POST
26 @Consumes({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML})
27 @Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
28 public Wine create(Wine wine) {
29        // To insert the data in db with the simple POJO Wine
30 }
31 
32 
33 @PUT @Path("{id}")
34 @Consumes({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML})
35 @Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
36 public Wine update(Wine wine) {
37 	// For updating the Data with particular ID	
38 }
39 
40 
41 @DELETE @Path("{id}")
42 @Produces({ MediaType.APPLICATION_JSON, MediaType.APPLICATION_XML })
43 public void remove(@PathParam("id") int id) {
44 	// to Delete the particular record with the selected ID
45 }
```

All the REST based API can be tested with the class

6>*Test.java* -

particular line to test here -

```
1 System.out.println(service.path("rest").path("wines").accept(MediaType.APPLICATION_JSON).g\
2 et(String.class));
```

Now a simple explanation on how the testing is happening for Jersey based REST Web Service -

We can dig into the *web.xml* further to see the lines -

<init-param> <param-name>com.sun.jersey.config.property.packages</param-name> <param-value>org.webphlox.brandserver.sample</param-value> </init-param>

*   for scanning the packages for REST based web service resources by Java Jersey Server.

```
1 <servlet-mapping>
2    <servlet-name>Jersey REST Service</servlet-name>
3    <url-pattern>/rest/*</url-pattern>
4 </servlet-mapping>
```

*   for identifying the path for REST based web services which is here – **/rest/**

So in the above testing method,

**service.path(“rest”)**

is for url-pattern

**and .path(“wines”)** is for getting the particular method. And also it will send the output in json format.

**Client Side -**

HTML Part -

In client side, the index.html is for the backbone.js templates -

```
1 <script type="text/template" id="tpl-header">
2    <button class="new">New Wine</button>
3 </script>
```

*   Here the Button is for New Data Add.

```
1 <script type="text/template" id="tpl-wine-list-item">
2    <a href='#wines/<%= id %>'><%= name %></a>
3 <!-- <%= id %> and <%= name %> are used as template variables.
4 </script>
```

*   to show the Data list in a tabular format.

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

*   to show the particular data item details.

**Javascript part (Backbone.js)**

All the javascript related codes can be found in main.js.

First, we have to define the Model of Data to be handled by backbone javascript.

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

**urlRoot** is the REST based web service calling point (endpoint). Here we have specified the url which is needed to data select/insert/update/delete. Also the Model is **Wine** – which will be used to store data from web service endpoint and manipulate the data and it is part of collection - **WineCollection**.

The **default** parameter is used to initialize a new Model while adding the data.

There are three views in the Application

A. *WineListView* – contains a collection of Item View - WineListItemView

B. *WineListItemView* – responsible for rendering the model template – WineView

C. *WineView* – contains core methods for adding,deleting and updating -

The interesting methods are – 1> *saveWine* and 2> *deleteWine*

D. *HeaderView* -responsible for initialize the view for adding a new template.

The interesting method is – *newWine*

Router - *AppRouter* is responsible for initial routing of the Application.

### Backbone.js in Client Side Javascript MVC

This article is extension of [Backbone.js based Application with Java based web project](http://www.phloxblog.in/developing-java-web-applications-backbone-js).

The project code can be downloaded [here](https://github.com/piyasde/GitHub_Projects).

In Backbone.js Javascript MVC Frameworks, The Model is referred to the intermediate data holding objects in client side which is required for data manipulation, validation on client side, fetching data from server side and finally required for submission to server side.

In our case, the Model Code is -

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

Here, the defaults attributes are for the data at the time of new Model data instansiation.

Also we can see the model data instantiation in newwine function of AppRouter -

```
1 app.wineView = new WineView({model:new Wine( 
2 		{id:null,name:"",
3 		 grapes:"",
4                  country:"",
5                  region:"",
6                  year:"",
7                  description:"", 
8                  picture:"generic.jpg" }
9  )}); // instantiation of model
```

Here we have passed some values to the Attributes of the Wine Model.

In a Model, the urlRoot specifies the main url path for the REST based web service.

In our case, it is -

**urlRoot:”http://localhost:8080/brandserver/rest/wines”**

Now in -

```
1 window.WineCollection = Backbone.Collection.extend({
2     model:Wine,
3     url:"http://localhost:8080/brandserver/rest/wines"
4 });
```

The collection, named as WineCollection is initialised with Model Wine by expecting same json data from server by calling the REST based web service.

Interesting to see, the AppRouter calls the list function, which actually takes A REST based web service call internally, when the following code is executed -

```
1 this.wineList = new WineCollection();
2 this.wineListView = new WineListView({model:this.wineList});
3 this.wineList.fetch(); // Call to Server for all data selecting (REST Web Service)
```

Now interesting is Model Saving function – saveWine -

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
12    // Some code snippet
13    app.wineList.create(win, {  //REST Web Service calling internally
14        success:function () {
15             	alert('Wine saved successfully');
16                	app.navigate('', true);// to initialize the state
17                 window.history.back(); 
18              }
19       });
20    // The above Code snippet is used for saving a new model to the server. The create func\
21 tion is important. This     
22    // callback function is called after instantiating a new model and set values to it's a\
23 ttributes. 
24 
25    win.save(); //REST Web Service calling internally
26    alert('Wine updated successfully');
27    app.navigate('', true); // to initialize the state
28    window.history.back();
29    // The above Code snippet is used for updating a model to the server. The save function\
30  is important. This     
31    // callback function is called after setting values to an existing model attributes. 
```

Now the deleteWine Function -

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

### Backbone.js Router in Client Side Javascript MVC

In Backbone.js Javascript MVC Frameworks, router are used to navigate web site URL’s by using hash tags(#).

All routers in Backbone.js contain route and function to map to that route. In our case, the route refers to -

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

### Backbone.js View in Client Side Javascript MVC

Backbone.js views are used to render client side application data model. They are used to listen events and work as per that. We will explain view functionality with JavaScript template library within our application for one of our view.

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

The project code can be downloaded [here](https://github.com/piyasde/GitHub_Projects).

**More Resources :**

[What is a view?](http://backbonetutorials.com/what-is-a-view)

[Backbone.js Tutorial: List Views](http://dailyjs.com/2012/12/27/backbone-tutorial-5)

[What is a router?](http://backbonetutorials.com/what-is-a-router)

1.  [Backbone.js Lessons Learned and Improved Sample App](http://coenraets.org/blog/2012/01/backbone-js-lessons-learned-and-improved-sample-app)
2.  [Learn Backbone.js Completely](http://javascriptissexy.com/learn-backbone-js-completely)
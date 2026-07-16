![](images/00004.jpeg)

JavaScript:

Elite JavaScript Coding from The Ground Up

© Copyright 2017 by Keith Dvorjak - All rights reserved.

The transmission, duplication, or reproduction of any of the following work including specific information will be considered an illegal act irrespective of if it is done electronically or in print. This extends to creating a secondary or tertiary copy of the work or a recorded copy and is only allowed with an express written consent of the Publisher. All additional rights reserved.

The information in the following pages is broadly considered to be a truthful and accurate account of facts, and as such any inattention, use or misuse of the information in question by the reader will render any resulting actions solely under their purview. There are no scenarios in which the publisher or the original author of this work can be in any fashion deemed liable for any hardship or damages that may befall them after undertaking information described herein.

Additionally, the information in the following pages is intended only for informational purposes and should thus be thought of as universal. As befitting its nature, it is presented without assurance regarding its prolonged validity or interim quality.

Table of Contents

Chapter 1: OOP(Object Oriented Programming) in JavaScript

Chapter 2: The ‘this’ keyword in JavaScript

Chapter 3: JSON

Chapter 4: Synchronous and Asynchronous Javascript

Chapter 5: Promises in JavaScript

Chapter 6: AJAX

Chapter 7: Closures and Callbacks in JavaScript

Chapter 8: Apply, call and bind methods

Chapter 9: Collections in JavaScript

Chapter 10: Working with Canvas in JavaScript

Chapter 11: Animations in JavaScript

Chapter 12: Memory leaks in JavaScript

Chapter 13: Recursion

Introduction

Thank you for downloading JavaScript: Elite JavaScript Coding from The Ground Up! This book is the fourth entry of the DIY JavaScript series. It is preceded by the books:

- JavaScript: Beginner JavaScript Coding from The Ground Up

- JavaScript: Intermediate JavaScript Coding from The Ground Up

- JavaScript: Advanced JavaScript Coding from The Ground Up

…and assumes that the user is familiar with the contents of those books, including JavaScript code, syntax, and beginner to advanced concepts. The books should be taken in chronological order for optimal results. This book will cover high level JavaScript manipulation techniques, with code examples to match the topics explained.

Thank you again for downloading this book! You have many choices available to you for furthering your JavaScript coding knowledge. Thank you for selecting the DIY JavaScript series as your tool of choice!

Chapter 1: Object-oriented programming in JavaScript

Among a chest-full of programming languages, choosing one of them needs to be done wisely. There are a lot of factors that affect the choice of language, ranging from efficiency to reliability. A significant part of the whole discussion also depends on the paradigm the language follows.

A programming paradigm is a model to classify programming languages based on the features it provides. It is a fundamental style of building the structure and elements of the language. The styles and capabilities of the programming languages are defined by their paradigms. A language can even implement multiple paradigms. For example, Haskell uses only a single paradigm to define itself i.e., functional programming. JavaScript supports functional, object-oriented and imperative programming styles. Different programming paradigms are:

•    Imperative

•    Object-oriented

•    Logic

•    Symbolic

•    Declarative

•    Functional

Why do we have so many paradigms? The answer to this basic question is because we have a lot of problems to solve and different paradigms work more efficiently when tackling particular sets of problems. The object-oriented paradigm is a good way to handle complexities, while concurrency can be avoided by using the functional paradigm. It is quite easy to understand that multiple paradigm languages will in most cases over-rule single paradigm languages.

Paradigm Used in JavaScript

We already know that JavaScript implements multiple paradigms, such as functional, object-oriented and imperative. We are going to look into the object-oriented nature of JavaScript. Before completely diving into its implementation in the language, let’s understand what it is and what its advantages are.

Object-Oriented Programming

Object-oriented programming is a programming language model which is focused on objects, rather than on performing actions, and data rather than on logic involved. In such a style of programming, the programmer only cares about implementing objects. Here, objects can be anything from human beings to dinosaurs, bricks to buildings, and anything else you can think of. Each object has a set of data associated with it, and different methods which can be used to manipulate it. As an example, let’s take a car as an object. A car has its color, size, the number of seats, and much more as its data, while moving, stopping and starting can be considered as the methods associated with a car.

The big problem arises when implementing it in a program. We start off by identifying all the objects that we are going to use, as well as the relations they share among each other; this is known as data modeling. The second step involves generalizing the object as a class of objects, which defines the data associated with it and the different methods/abilities of the object.

The concepts of object-oriented programming provide us with these benefits:

•    For every class, we can define subclasses which can inherit properties and functionalities from its main class. This is called inheritance. The real world follows an inheritance tree where the child element inherits some, or all, of the parent’s properties added with some of its own unique properties which might not be available with its sibling elements. This helps in reducing development time, as well as increasing the efficiency of the programmer.

•    While defining classes, we are only concerned with the class’s data. Hence, when an instance of the class i.e., an object is run, it won’t be able to modify any data which is not a part of it. This process is known as data-hiding, which provides system security, and also helps in avoiding unintended data-corruption.

•    A class can be used again and again. It is reusable not only by its own program, but also by other programs.

•    Found an error in your program? No problem! You need only to check your code for the class which throws the error. This helps to make testing easier, debugging and maintaining of the whole program.

OOPS in JavaScript

In the earlier section, we briefly learned about different concepts of object-oriented languages. While we focus directly on its implementation in our language of interest i.e., JavaScript, which is dynamic in nature, we are only concerned with Inheritance and Encapsulation. Why don’t we care about Polymorphism then? JavaScript, being a dynamically typed programming language, makes observing the effects of polymorphism much more difficult because it is more evident in statically-typed languages like C or C++.There’s no point of discussing method or function overloading in JavaScript, because we do not have any data-type being specified while we code. Therefore, the machine can’t differentiate between two definitions of the same function. In JavaScript, a lot of concepts are implemented with the help of functions. Object-oriented coding is no exception to it. An instance is an implementation of the function.

Function child(name){

    // code here

}  // child is a constructor because we will use the keyword “new” to invoke it.

Now, this may seem to be similar to languages like Java, where we use the new keyword to create instances.

Var aditya = new child(“aditya”); // Aditya is an instance of child

alert(typeof(aditya)); //displays "object"

In the preceding example, Aditya is an instance that was created from the child constructor function. Here, child is both a function and an object, because functions ARE objects in JavaScript. This instance can have its own data/properties and functionalities from the child object, which we will discuss in the coming section.

There exist several ways of creating objects in JavaScript. The most fundamental and easy to understand method is using ubiquitous object literal pattern. For example:

var student = {

    name: “ritesh”,

    age: “19”,

    branch: “cse”

};

Here, we have created an object “student” with name, age and branch as its properties.

The second method is using the constructor pattern. For example:

function student (name, age, branch) {

this.name = name;

this.age = age;

this.branch = branch;

} // student () is the constructor function because we use the new keyword below to invoke it.

var rahul = new student(“rahul”, 19 , “cse”) // Rahul is a new object that we have created from the student () constructor function.

console.log(rahul.name); // Rahul

console.log(student.branch); // cse

In the methods detailed above, we observe a major difference between the two. In the literal pattern, we have already created an object while declaring it. In the constructor pattern, we need to explicitly call the constructor along with the “new” keyword in order to create an instance of a student.

The third and the last method is using the prototype pattern, where we directly add each property and method to the object’s prototype as the method’s name suggest. For example:

function student ()

{

student.prototype.firstName = "Ritesh";

student.prototype.lastName = "Kumar";

student.prototype.age =19;

student.prototype.branch = “cse”;

student.prototype.fullName = function () {

console.log (this.firstName + " " + this.lastName);

};

var ritest = new student () // creating instance of student using new keyword

console.log(ritesh.fullName()); // This logs into the console of the browser with the value “Ritesh Kumar”

You might be confused with the “prototype” keyword being used in the above example. This is the most important part of this method. We define prototype as an internal object which is used by other objects to inherit properties. This allows multiple instances of the same object to share common properties. Therefore, the properties which are defined using the prototype object are inherited by all of its instances.

Now, among the three methods that are available to you for creating objects, “which one is the most suitable?” and “in which situation?” needs to be discussed. We will try to find the answer to this question in our next section, focused on Encapsulation.

Why Do We Need Encapsulation?

The literal method is handy when you want to have only a single copy of a particular object, and it is only going to store data. This method is ineffective however, when you want to have several instances of the same object with different data available to all of them.

When we want to create many objects with the same properties? We can encapsulate the common properties shared by all of them into a function, then use the constructor to create multiple objects. This is where we utilize encapsulation.

The practical implementation in JavaScript uses the constructor and prototype method combined. For example:

function student (name, age, branch) {

    this.name = name;

    this.age = age;

    this.branch= branch;

    this.marks = [];

}

With the help of the code above, we created the constructor function for the student object using the constructor method. This only contains the data that is associated with a student. In the following code snippet, we are going to add the functionalities that are associated with the student using the prototype method.

student.prototype = {

    showName:function ()  {

        return this.name;

    },

    addMarks:function (mark)  {

        this.marks.push(mark);

    }

}

Here we end up writing code for defining an object. The next task involves creating instances of the object we just created.

// First instance of the object

rishabh = new student("rishabh", 20, “cse”);

rishabh.addMarks(98); // adds 98 to the marks array

rishabh.showName();  //returns “rishabh”

// Another instance

mitul = new student("Mitul", 19, “mechanical”);

mitul.addMarks(100); // adds 100 to the marks array

mitul.showName (); // returns “mitul”

With the example above, the importance and benefits of having encapsulation in your hands might be very clear. We encapsulated all the data and functionalities of a student into one function, and later created instances of it (rishabh and mitul) which share the same properties that a student does. This reduces the whole task of defining each property for similar object instances repeatedly.

That’s it for encapsulation! The next section will be focused on broadening the implementation of objects by using inheritance, so that different objects can share or inherit properties from a parent element.

Inheritance in JavaScript

This feature brings us much closer to the real world. Let us take a look at humans, for this example. Human beings inherit some properties from the Hominid class, which itself inherits some properties from its parent class that further goes on to the Mammal class. Objects inherit properties from its parent’s class. Inheritance comes to be very handy when coding to address similar problems. We create an object for the Mammal class, which is later inherited by the Hominid class, and human beings inherit from the Hominid’s class. While doing so, human beings get the properties of both the Hominid’s and Mammal’s classes. Since humans reproduce like other mammals, this approach seems to be completely fine. Moreover, the human beings’ class can have other properties added to it which might not be available to other mammals.

So far, we have only discussed the real-life implementation of inheritance. Let’s dive into coding and flesh it out.

Let’s make a car object.

var car = {

    Color: “black”,

    Seats: “4”

};

// inheriting from the car object

var myCar = Object.create (cars); // now myCar inherits the properties from car

console.log(myCar.color); // black

We can also add more properties to the instance we created.

Now comes the meat of the inheritance section. We use the inheritPrototype function for inheriting from the parent class.

function inheritPrototype(child, parent) {

    var parentCopy = Object.create(parent.prototype);

    parentCopy.constructor = child;

   child.prototype = parentCopy;

}

Let’s understand how this code works. Initially, we started off by creating an instance of the parent child (parentCopy). We store the child instance into the constructor of the parentCopy. This is done because in the next step, we will be storing the parentCopy into the child’s prototype. When we do this, we override the previous contents of the child’s prototype, and hence lose the actual values. To keep this from happening, we created a copy of the child’s constructor. While we store the parentCopy into child’s constructor, it doesn’t lose its old values.

Creating a new object, which will later inherit from our parent object i.e., car.

var audi = {

    name = “audi”

};

inheritPrototype(audi, car);

Audi will have the same properties as a car, but it needs to define its own unique property, which is “name”.

Chapter 2: The ‘this’ keyword in JavaScript

In JavaScript, the keyword ‘this’ behaves differently than when compared to other programming languages. The value of 'this' is determined by how an object is instantiated, or “where the keyword is actually being used”. The 'this' keyword in simple words returns the current local scope object.

If you are using this on global scope, it will refer to the window object. The window object is the only globally available object in JS.

Therefore, the result of console.log(this) on global scope will be returning the window object.

To get a better understanding of ‘this’, let’s define an object as follows:

<code>

var obj = {

someProperty1: “Hi”,

someProperty2: function(name) {

// here ‘this’ will scope to the obj object as it is the current local scope object out

// it's scope there exists the window object

return this.someProperty1 + name;

}

}

var myObj = obj.someProperty2(“ John”);

console.log(myObj); // === “Hi John”

</code>

In the code above, in someProperty2 property of obj , we used ‘this’ keyword to access another property of current object that is someProperty1, and hence the function returned “Hi John” as a result.

The results would not have been affected if we used arrow functions of JavaScript. The results would have bene the same.

With the help of the ‘this’ operator, we can make constructors of objects in JS as follows:

<code>

function obj(name) {

this.name = name;

this.someMethod = function() {

console.log(this.name);

}

}

var myObj = new obj(“John”);

myObj.someMethod(); // === John

</code>

You can also use ‘this’ on object prototypal chain like:

<code>

var obj = function() {

return this.a + this.b;

};

var myObj = Object(obj);

myObj.a = 5;

myObj.b = 6;

myObj(); // === 11

</code>

Similarly as before, we used the this keyword to access the current object, and to instantiate its data members and functions.

I would like to conclude saying that the ‘this’ keyword in JavaScript is something you’ll find need of frequently. It will make your work easier and give you much flexibility in your coding style.

Chapter 3: JSON

JSON or JavaScript  Object Notation, originally specified by Douglas Crockford, is one of the most commonly used data-interchange format. JSON is nothing but a simple medium of storing and exchanging the data. This exchange happens between the browser and the server.

The format of data can only be text and any JavaScript Object can be converted into JSON format for sending data to the server. Likewise, any JSON text can be converted into JavaScript Object when receiving data from the server.

JSON is a lightweight format which is easy to understand for humans, as well as easy to parse for machines. It is language independent, meaning that it is not only restricted for use with JavaScript, although, JSON uses JavaScript syntax, Since the format is text only, it can be read and used by any programming language. Its filename extension is .json. JSON is widely preferred over other data-transferring notations such as XML due to its easy-to-parse characteristics.

JSON Syntax

JSON syntax somewhat resembles JavaScript syntax, with the minor difference that keys must be strings written in double quotes “ ” which include the following notations:

1.  The data to be exchanged should be in the pairs of Name & Value. Each Name has a Value corresponding to it, which can be accessed with a JavaScript object through its Name.

Ex: “name”: “Mark”

1.  The objects are placed inside the Curly braces ‘{ }’. Each name field is followed by a colon ‘:’, then its value. Each name-value pair is followed by a comma ‘,’ in case the user wants to enter another name-value pair.

Ex: {

“name”: “Mark”,

“age”: “20”

}

1.  The arrays of these objects are contained in square brackets ‘[ ]’ and each object is itself separated by a comma in an array.

Ex: [

{

“name”: “Mark”,

“age”: “20”

},

{

“name”: “Anthony”,

“age”: “40”

}]

Data Types

JSON can be written with the values having following data types:

1.  Number - In JSON, numbers used must be integers or floating-point numbers

Ex: { “age”: 20 }

1.  String

Ex: { “firstName”: “Mark” }

1.  Boolean

Ex: { “vegetarian”: true }

1.  Array

Ex: { “children”: [“Henry”, “Emma”, “Joe”] }

1.  Another JSON object

Ex: {

“details”: {

“lastName”: “Lucas”,

“bankAccount”: “savings”

}

}

1.  Null

Ex: { “middleName”: null }

Note: Do not confuse JSON data types with JavaScript data types. Do not use any of the following data types:

1.  Functions
2.  Dates
3.  undefined

Objects in JSON

JSON Object values can be accessed using dot(.) notation as follows:

Ex: If we want to access only the firstName of the variable fullName, it can be done as such:

var fullName = {

“firstName”: “Mark”,

“lastName”: “Anthony”

};

var firstname = fullName.firstName;

Another way is to use square bracket [ ] notation:

var firstname = fullName[“firstName”];

Similarly, we can access the nested JSON objects by moving down the hierarchy name by name.

Ex: var fullName = {

“name”: {

“firstName”: “Mark”,

“lastName”: “Anthony”

},

“age”: 25,

“profession”: “Business”

}

var firstname = fullName.name.firstName;

Values can also be set using dot or square bracket notation by simply equating the desired key with the required value:

Ex: fullName.name.firstName = “Ross”;

Or fullName.name[“firstName”] = “Ross”;

Arrays in JSON

JSON array values can be accessed using the index number of the key/value of that specific array.

Ex: var fullName = {

“name”: [

“firstName”: “Mark”,

“middleName”: null,

“lastName”: “Anthony”

],

“age”: 25,

“profession”: “Business”

}

var firstname = fullName.name[0];

Similarly, we can access the nested JSON arrays by moving down the hierarchy name by name.

Ex: var fullName = {

“details”: [

{

“name”: [

“firstName”: “Mark”,

“lastName”: “Anthony”

],

},

{ “age”: 25 },

{ “profession”: “Business”}

]

}

var firstname = fullName.details[0].name[0];

In arrays, values can only be set using square bracket notation by equating the desired key with the required value:

Ex: fullName.details[0].name[0] = “Ross”;

JSON Methods

The JSON data received from the server-side to the client-side will always a string. Since we require the data to be a JavaScript object to access the values from the keys, the JSON data is parsed using the JSON.parse() method.

Ex: JSON.parse(‘{ “children”: { “Henry”, “Emma”, “Joe” } }’); will give us the JSON object { “children”: { “Henry”, “Emma”, “Joe” } }

Note: Text must be written in JSON format to avoid a syntax error.

Similarly, the JSON data to be sent from the client-side to the server-side is must always be a string. Since our data is a JavaScript object, we need to convert it to a string before sending it to the server. The JSON object is converted to a string using the JSON.stringify() method.

Ex: JSON.stringify({ “children”: { “Henry”, “Emma”, “Joe” } }); will give us the string ‘{ “children”: { “Henry”, “Emma”, “Joe” } }’

Arrays can also be stringified in the same way using “JSON.stringify(arr)”, where arr is an array of JSON objects.

Chapter 4: Synchronous and Asynchronous JavaScript

Understanding the concept of asynchronous and synchronous in terms of programming is a rather difficult task. There can be a steep learning curve, but after getting a good grasp of this concept, you will be able to understand other advanced concepts easily. Most of the advanced concepts in JavaScript are based on asynchronous behaviors within JavaScript.

What do synchronous and asynchronous mean?

“Synchronous” refers to actions occurring simultaneously, happening at the same time as one another. Asynchronous is simply opposite of synchronous.

In terms of programming, synchronous behavior means that the code is executed in the same order that it is written in, and asynchronous means that code is not necessarily executed in the same order that it is written in.

Let us understand this with the help of a real-life scenario.

Imagine you are ordering a pizza by making a phone call, but there is only one in the pizza shop who can take the call. If someone else is also placing a phone order while you call, you will get a busy tone. You will have to wait for the current phone call to finish until you can place your order and cannot do other things while waiting for your turn! This scenario shows a synchronous behavior, where you cannot move onto your next task until the current one is finished.

Now let us alter some circumstances in the same scenario. Say that the person taking pizza orders gets an answering machine, which records the call when the phone is busy and reports it to the person taking the order after they finishes the current call. Now if the phone is busy when you call, you simply leave the order on the answering machine and continue with your activities. When the person taking the orders receives your order, the call will be returned, and the order will be filled. This scenario details asynchronous behavior, as you do not have to wait for the other call to be finished. You can fulfill your side of the transaction, and complete it with any details necessary (expected time of receipt, payment method, address, etc) when the other party is ready to participate.

There are simpler examples to detail this behavior. Your body can perform multiple tasks at once, like playing the guitar while singing. This is an example of asynchronous behavior. Conversely, all other actions stop while sneezing. This is an example of synchronous behavior, as you must wait for the sneeze action to be completed for other actions to resume or begin.

Similarly, in programming, if you do not have to wait for an action to finish and can move onto another task, then the action is said to be asynchronous. The action started earlier running in parallel may report its progress, like the person taking order may return back to you with more details after he gets your order.

Let us see examples code of both synchronous and asynchronous JavaScript.

Synchronous:

console.log('how');

console.log('are');

console.log('you');

The output of the above code will be:

how

are

you

This is simple! The output is as you would expect it to be.

Asynchronous:

console.log('how');

setImmediate(function() {

console.log('are');

});

console.log('you');

The output of the above code will be:

how

you

are

Notice that there is a difference in output here. This is because of the asynchronous nature of the setImmediate() method.

Why Asynchronous?

Whenever you do some heavy or time-consuming operation in synchronous mode, the rest of the code won’t execute until that code finishes executing. This leads to a condition known as I/O blocking. When this happens, the UI, also known as the “frontend” of your website or web application, will become non-responsive for the time being. This is because the UI and the JavaScript code run in the same thread! In cases like these, we use asynchronous methods. That way, the heavy task keeps running and it doesn't cause the user interface of the application to be unresponsive.

Here’s an example usage scenario.

Let’s imagine that you have a very long loop. Say the loop is:

for( var i = 0; i < 99999999; i++) {

// doing some task here

}

While this loop is running, nothing else will run and the web application’s frontend will become unresponsive. In order to solve this problem, we will use setImmediate(). Here is the converted version of the loop:

function longLoop(i) {

// doing some task here

if( i < 99999999) setImmediate(longLoop, i + 1); // increasing value of i and calling function again to create a loop

}

setImmediate(longLoop, 0); // starting the loop

Running the above code won’t cause the UI to go unresponsive. The call to each iteration of the loop is asynchronous, thereby allowing other functions to be executed as well.

The concept of synchronous and asynchronous is the core of JavaScript and the base of almost all advanced concepts in JavaScript. Be it timers, AJAX, or any number of other concepts, it becomes important to understand this concept to establish a base for your continued knowledge.

Chapter 5: Promises in JavaScript

Promises in JavaScript provide an alternative for managing asynchronous requests. Another alternative is to use callbacks.

You can interpret promises in JavaScript like the promises that you make in your real life. For example, if your friend promises to do your homework on your behalf by the end of the day? He would have either done your homework for you or not. There are only a set number of outcomes to his promise, right? Similarly, promises in JavaScript can have three states:

● Pending: This means that the Promise is still waiting to be fulfilled. It can have any output, such as “it's not the end of day yet, and you don’t know whether your friend will complete your homework or not.”

● Rejected: This means that you have gotten the result of the promise and it was negative, like “your friend didn’t do your homework after all.”

● Resolved: This means that you have gotten the result of the promise and it was positive, yielding the desired output. “Your friend did your homework!”

Once the promise is either Resolved or Rejected, it is said to have been settled.

Promise is a class in JavaScript. You create a new object of this class by using the keyword ‘new’ to create a new Promise object.

ECMAScript 5 or ES5 standards for JavaScript, which is currently used in all major browsers at the time of this publication, does not natively have standards for Promises. However, some browsers still support Promises. ES6 natively supports Promises. Promises will soon be supported by all major browsers.

Creating Promise

As stated earlier we will use the keyword ‘new’ to create a new object of the class Promise, generating a new Promise object. The constructor of this object takes in a closure function, which itself takes two parameters. Here is the syntax for creation and consumption of a new promise object.

ES5 Syntax:

new Promise( function(resolve, reject) { /* task here */ } ).then( function() { } ).catch( function() { } );

ES6 Syntax:

new Promise( (resolve, reject) => { /* task here */ } ).then( () => {} ).catch( () => {} );

The two parameters ‘resolve’ and ‘reject’ passed as the argument to the closure functions are used to settle the promise. Both of these parameters are functions themselves. Calling the resolve() method sets the promise state to resolved, and the function passed as the argument of the then() method is called. Calling the reject() method sets the promise state to rejected, and the function passed as the argument of the .catch() method is called.

Now let's create a promise representing the friend and homework example we used earlier:

var friendPromise = new Promise( function(resolve, reject) {

/* usually an asynchronous task goes here */

if( isHomeworkCompleted() ) resolve();

else reject();

});

Some points to be noted here are:

● Promise starts doing the task as soon as it is created. In the example above, as soon as we create the Promise, it calls the function isHomeworkCompleted() to check if homework is completed or not.

● Once a promise is settled (once the resolve() or reject() method is used inside the promise), using them again will have no effect at all.

Getting the Promise result

We can get the promise result after it is settled using the then() and catch() methods of the Promise object. Its syntax has already been defined in the previous section.

Now let's consider the example code we wrote in the previous section and see how we can use it:

friendPromise.then( function() {

console.log( 'Promise fullfilled!' );

}).catch( function() {

console.log( 'Promise rejected :( ' );

});

Promises are Asynchronous

The process of getting the result of a promise is asynchronous. To understand this, consider the following example:

console.log('Before');

friendPromise.then( function() {

console.log( 'Promise settled' );

}).catch( function() {

console.log( 'Promise settled' );

});

console.log('After');

The output of the above code will be:

Before

After

Promise settled

As you can see, ‘After’ was printed before ‘Promise settled’ on the console screen. Without knowing any better, it may seem that it would have been be printed after it.

Getting Promise to execute when we want it to

As explained earlier, promise starts executing the task as soon as it is created. However, we often want the promise code to be predefined and to execute when we want it to. This is performed by wrapping the promise inside a function and returning the promise object from that function.

The above example would convert to this:

var friendPromise = function() {

return new Promise( function(resolve, reject) {

/* usually an asynchronous task goes here */

if( isHomeworkCompleted() ) resolve();

else reject();

});

}

And now we can consume it like this:

friendPromise().then( function() {

console.log( 'Promise settled' );

}).catch( function() {

console.log( 'Promise settled' );

});

Passing information from the task to then() or catch() method

We can achieve this by passing the information as the parameter(s) of resolve() or reject() functions. The parameters passed in the resolve() or reject() method gets passed as parameters to the function passed as argument of the then() and catch() methods, respectively.

Let’s explore this concept with an example:

var promiseSum = function() {

return new Promise( function(resolve, reject) {

var x = 5 + 5;

if( someCondition() ) resolve( x + 5 );

else reject( x * 5 );

});

}

promiseSum().then( function(y) {

console.log( y ); // prints ‘15’ on the console screen if promise is fulfilled

}).catch(function(y) {

console.log( y ); // prints ‘50’ on the console screen if promise is rejected

});

Chaining multiple promises

We can chain the then() methods of multiple promises one after another to execute asynchronous tasks one after another. This is because then() returns a promise itself.

If we return a value from the function in the then() method, that value gets passed onto the next then() method’s argument function in the chain, if any.

var examplePromise = function() {

return new Promise( function(resolve, reject) {

resolve();

});

}

examplePromise().then( function() {

return 5 + 7;

}).then(function( y ) { // chaining

console.log( y ); // prints ‘12’ on the console screen

return y + 15;

}).then(function( y ) { // chaining

console.log( y ); // prints ‘27’ on the console screen

});

If we return a promise from the function in the then() method, the next then() method in the chain acts as the then() method of the promise object returned earlier.

var examplePromise = function() {

return new Promise( function(resolve, reject) {

resolve(7);

});

}

var someOtherPromise = function(x) {

return new Promise( function(resolve, reject) {

resolve( x * 10 );

});

}

examplePromise().then( function(x) {

console.log( x ); // prints ‘7’ on the console screen

return someOtherPromise(x); // returning a NEW promise

}).then(function( y ) { // chaining

console.log( y ); // prints ‘70’ on the console screen

return y + 15;

}).then(function( y ) { // chaining

console.log( y ); // prints ‘85’ on the console screen

});

The Promise.all() method

General Syntax:

Promise.all( [ [ Promise1 [, Promise2 [, Promise3 [, Promise4 … ] ] ] ] ] );

This method returns a single promise when all of the promises passed as its argument have been settled, or one of them is rejected. The resulting promise’s then() method function argument’s parameter is an array containing all values passed by all the promise’s resolve method, and in the order that they were resolved.

Let’s see an example:

var promise1 = new Promise( function(resolve, reject) { resolve(9); });

var promise2 = new Promise( function(resolve, reject) { resolve(8); });

var promise3 = new Promise( function(resolve, reject) { resolve(7); });

var promise4 = new Promise( function(resolve, reject) { resolve(6); });

var result = Promise.all( [ promise1, promise2, promise3, promise4] );

result.then( function(x) {

console.log( x );

});

The output of the above code will be:

[9, 8, 7, 6]

If a promise in the stack is rejected, the catch() method of the promise is used. The function passed as the .catch() argument contains a single value, which is the value from the rejected promise in the stack.

Now let’s see what happens when we change the above example to make a rejected promise:

var promise1 = new Promise( function(resolve, reject) { resolve(9); });

var promise2 = new Promise( function(resolve, reject) { resolve(8); });

var promise3 = new Promise( function(resolve, reject) {

reject(7); // REJECTING

});

var promise4 = new Promise( function(resolve, reject) { resolve(6); });

var result = Promise.all( [ promise1, promise2, promise3, promise4] );

result.then( function(x) {

console.log( x ); // prints nothing on the console screen

}).catch( function(x) {

console.log( x ); // prints ‘7’ on the console screen

});

The Promise.race() method

General Syntax:

Promise.race( [ [ Promise1 [, Promise2 [, Promise3 [, Promise4 … ] ] ] ] ] );

This method takes in an array of promises and returns a single promise. The returned promise is the one which is first to settle, either to be resolved or rejected, from the stack of the promises passed.

Promises are a very useful feature of JavaScript and are widely used since it provides a clean and manageable method to handle asynchronous tasks in JavaScript.

Chapter 6: AJAX

You might have developed a lot of web pages containing images, videos, etc. All of them probably lacked a common functionality. They were all perhaps static web pages, which had to be refreshed to display new content. There is always an alternative, a better way to do any task when you code. Why not have a dynamic web page? This is where AJAX comes into the picture. AJAX stands for Asynchronous JavaScript And XML.

AJAX is an important frontend web technology which plays a crucial role in the development of several sites you visit all day. This technology helps you update a particular part of the web page without the need to refresh the complete page. This creates a better and faster web experience for your site’s visitors, and also decreases the amount of data exchanged between the host computer and the server.

AJAX helps JavaScript communicate with a web server. Now your site isn’t static anymore, but completely dynamic. Gmail, Facebook, Twitter, and Youtube are only a few websites to name who utilize AJAX heavily in their frontend code.

Understanding the AJAX Call Process

This involves a number of steps to get the task done. We will list those steps in this section, and explore the concepts in the next section.

•    Triggering the event: This happens when you click on a button, submit a form, or any type action that initiates a response.

•    AJAX call fires up and a request is sent to the web server using XML

•    The server side script (PHP, ASP, etc.) takes the input and processes it accordingly. It also accesses the database if required.

•    The script then sends back the output of the processing performed using XML to the client side page which made the particular request to the server.

•    A JavaScript callback function receives the data, processes it accordingly, and then updates the relevant section of the web page.

Let’s Code!

Step 1- Making an HTTP request

To make an HTTP request, we need an object that handles the necessary functionalities for the request. As we already know that JavaScript supports OOPS, making an object isn’t a challenging task for us. The only thing we need to handle is the various object types that different browsers support. Microsoft’s Internet Explorer supports ActiveX object. Other browsers like Chrome, Mozilla, etc. support XMLHttpRequest object. Meanwhile, Microsoft also implemented the XMLHttpRequest object in its later browsers, but for increased compatibility, we are going to consider ActiveX object, too.

//browsers supporting XMLHttpRequest object

if (window.XMLHttpRequest) {

    requestObject = new XMLHttpRequest();

//browsers supporting ActiveX object

} else if (window.ActiveXObject) {

    requestObject = new ActiveXObject("Microsoft.XMLHTTP");

}

As covered in our previous section, the server returns a response after processing the input. We need to define the function which is going to handle the response.

The object we have created has a property named “onreadystatechange” which handles the response sent back by the server.

requestObject.onreadystatechange = functionName;

You might observe that we haven’t put parenthesis after functionName. This is because we are only assigning a reference to the function.

You can also define a function like this:

 requestObject.onreadystatechange = function(){

    //Body of the function which will handle the response

};

Now we are all set to make the request. This can be done by calling the open() and send() methods of the object we just created.

requestObject.open(‘GET’, ‘http://www/websiteExample.com/file-name’, true);

requestObject.send();

Let’s discuss the parameters for the open method.

•    This is known as the HTTP request method. There are several other methods that can be passed like POST, HEAD, DELETE, and many others. These vary from server to server, as all servers do not support every method defined. As per standards, the method should always be in capitals. Otherwise, some browsers might not support your request.

•    The second parameter is the URL you’re sending the request to.

•    The third parameter is for determining whether the request is asynchronous or not, and is optional. The default value is “true”, which means the script continues and the user is allowed to use the web page while the request is being processed. Alternatively, “false” stops the script and waits for the server to send a response.

Step 2- Handling the server’s response

In the first step, we defined a function which would handle the responses sent by the server. In this step, we are going to learn about its functionality in detail.

The first thing the function needs to do is to check the response’s state. There are five response states defined. These are:

Value State Description

0 UNSENT Request client created but open method isn’t called yet

1 OPENED Open method is called

2 HEADERS_RECEIVED    Send method is called

3 LOADING Loading the data

4 DONE Request is complete

From the table, we can figure out that value 4 is the successful state. We need to check whether the response returned was successful or not. In other words, we need to check if it state’s value is 4\.

This can be done by comparing the state’s value to XMLHttpRequest.DONE, which has a value of 4.

if (requestObject.readyState === XMLHttpRequest.DONE) {

    //The request has been successfully completed and can be processed further

} else {

    // Not yet ready

}

Once we are done with the above step, our next step is to check the response code. Similar to the response’s state, there are several response codes which can be sent by the server. Response code 200 evaluates that it was a successful AJAX call. We need to check for code 200 to proceed further.

if (requestObject.status === 200) {

    // Successful

} else {

    // The request was unsuccessful

    // 404 (Not Found)

    // 500 (Internal Server Error)

    // 204 (No content)

    // and so on.

}

After checking for a successful AJAX request, you can do anything with the returned data as required.

Let’s look into some of its usages.

• Login forms: You might have observed that some websites pop-up a small login window, and upon login notify you that you have been logged in, while the page remains unchanged during the process.

• Auto-complete forms: The most common example of this usage is Google. When you type in the search box, it suggests you for a probable term or set of terms you might be looking for. This is done using AJAX.

• Form submission and validation: Almost all websites nowadays validate forms on the go using AJAX.

• Chat rooms and instant messaging: The best example for this is Facebook. While chatting, the new messages come up without reloading the whole page. This is AJAX’s magic.

• External Widgets: Google AdSense is a popular example for this. It shows you content based on the website you are on and changes accordingly without refreshing the whole page.

Chapter 7: Closures and Callbacks in JavaScript

The chapter will deal with two very basic concepts of JavaScript, closures and callbacks. They allow us to make our code concise, crisp and creative. You will encounter these concepts in your development repeatedly. Let us have a look.

Closures in JavaScript

Closures, in their most basic form, are inner functions that have access to variables from outside its scope. The concept of closures requires a legit understanding of nested functions.

Nested functions are “functions containing functions”. Let’s look at an example to expand upon the point:

//function 1 is an outer function

function outer(){ //definition of function 1

//body of outer()

//function 2 is an inner function

function inner(){//definition of function 2

//body of inner()

}

}

In above example, function 2(  inner() ) resides inside the body of function 1(outer()) and hence is called a nested function. Similarly, we can have more than one nested function inside an outer function.

//function 1 is an outer function

function outer(){ //definition of function 1

//body of outer()

//function inner1 is an inner function

function inner1(){//definition of inner function 1

//body of inner()

}

//function inner2 is an inner function

function inner2(){//definition of inner function 2

//body of inner()

}

.

.

//function innerN is an inner function

function innerN(){//definition of Nth inner function

//body of inner()

}

}

The ability of the inner function to evaluate or perform calculations on the variables or parameters defined in outer function is closure.

Let us take a very basic example of JavaScript code.

//Example 1

//define a variable a = 5

var a = 5;

//define function add which adds 5 to a and returns value

var add = function(val){

a = a + val;//adding val to a

return a;//return a

}

var result = add(5); //will make result = 10

In above code, the function  add() will take the value of variable a from its outer scope, and will add 5 to it and return the result. So, our output will show 10\. This is the most basic use of closures. Surprised? You might have used it multiple times while developing code by now.

Closures are popular, as the inner functions are able to retrieve variables from outside their scope, modify their values, and return the result. The closures have access to only the following variables:

● variables inside its scope, i.e. variables defined inside the function body

● variables of outer function, i.e. variables of containing function

● global variables

Let us move to a more complicated scenario:

//Example 2

//define function addTo() which takes a parameter

var addTo = function(param_outer){

//define a variable sample of value 10

var sample = 10;

//define function add which takes another parameter

var add = function(){

return sample + param_outer;

}

//return the inner function

return add;

}

Here, we have a nested function  add() which can take in parameters from the outer function  addTo().  When user makes a call to  addto()  with some parameter, he will get the inner function as a return for it, which in turn will execute the addition and return the value.

var test = addTo(10);

Internally,  param_outer will be equal to 10, and add will take value of addition of  param_outer and sample and will evaluate to 20.

var add = 20 ;

When the  addTo() call returns add, the value of test will equal to that of add, which is 20.

Let us take an even more complicated example:

//Example 3

//define function addTo() which takes a parameter

var addTo = function(param_outer){

//define function add which takes another parameter

var add = function(param_inner){

return param_inner + param_outer;

}

//return the inner function

return add;

}

var test = addTo(10); //value will not be 20

Here, test will take the value of inner function and will become a function itself, which will have a preserved variable,  param_outer equal to 10, set by us.

So, test will internally look like this:

//this is only a representation of how it will internally look

var test = function(param_inner){

return param_inner + 10;

}

If we want to add 10 to any number, we can simply write:

var x =10;

var y = test(x);

This will make the value of y equal to 20, or 10 + 10.

A good use case is when we want to add a constant to some numbers. We can use this approach for closures.

Example:

var addThree = addTo(3);

var a = addThree(10);//a will have 3 + 10 = 13   

var a = addThree(20);//a will have 3 + 20 = 13   

var a = addThree(30);//a will have 3 + 30 = 33

Features of Closures

●The inner functions have access to outer function variables even after they have been executed, as we saw in our third example. We called the outer function before calling the inner function and even after returning the value, we could use the outer function parameters inside the inner function as it was preserved.

●Closures store references and not actual values to outer functions variables and can be edited, if needed (refer example 4).

●Closures provide a secure way of dealing with certain data, as we can save references to variables and prevent accidental changes.

//Example 4

//define a variable a = 5

var a = 5;

//define function add which adds 5 to a and returns value

var add = function(val){

a = a + val;//adding val to a

return a;//return a

}

a = 10; //update value of a

var result = add(5); //will make result equal to 15 and not 10 as //value of a is updated before the closure is called so saved //reference is updated with new reference

Closures are powerful but due care needs to be taken, as updated references can make your code full of bugs. Always make sure to use the capability carefully.

Note: Closures are functions or inner function which have preserved data referenced inside them from global or outer scopes.

Callbacks in JavaScript

JavaScript functions are first-class objects. “First-class objects” mean that they can be used like other objects in the body. Like variables, we can save their references, pass them as arguments, declare nested functions (refer to previous sections), and can be return values of functions as we saw earlier.

The capability of a function to be passed as argument to another function makes JavaScript functions special. A passed function can be executed at a later stage, or be returned as a function to be executed later by some other function. This is what constitutes the JavaScript Callbacks.

Callbacks are functions which are passed as parameters to another function and is executed from the body of the containing function. Since the scenarios where such capabilities are of use is limited, they can be referred to as callback patterns.

//define a callback function sum()

var sum = function ( num1 , num2 ){

return num1 + num2;

}

//define a function that will use sum() as parameter

var calling_func = function ( a , b , callback ){

return callback ( a , b );//calling the callback function with //parameters

}

var sample = calling_func( 5 , 5 , sum);//new will be assigned 10

Let us walk through the code above. First, we declare a simple function that adds two values and return the result. Next, we define a function which takes in two parameters and a third parameter which is “callback”. Callback is basically a variable which will store the name of function we will pass and execute it accordingly. It can be called any name. For ease of understanding, I have named it callback.

The important thing to note is that when we pass a function as variable, we only send the definition of callback function as in the name (say  sum), not the function call with parenthesis. The function is executed only when it is called inside the body of the containing function.

As we have seen, callback functions are not called immediately, but are preserved as references and are only called when specified by the calling function, thus making them closures as detailed in the previous section.

Callback functions not only can take existing functions as parameters, but can also define a completely new function in the parameter. It will be called as a callback by the containing function. Let’s go through an example:

//no callback function is defined

//define a function that will use sum() as parameter

var sum = function(a,b){

return a+b;

}

var some_func= function( a , b , callback ){

return callback(a,b);

}

console.log(some_func(5,5,function(a,b){

return a-b;

}));

//output

0

Here, the function is specified directly with a return value. This works fine, and is used when we have situations where we know a certain function will only be used once or twice during our development.

Another important point to learn is that we can pass parameters to callback functions from inside the containing function.

var sum = function(a,b){

return a+b;

}

var b = 10; //define a global variable

var some_func= function( a , callback ){

return callback(a,b);//pass global var as a parameter

}

console.log(some_func(5,sum));

//output

//15

Here, we can pass in some reserved or pre-defined parameters to the callback function which can consume it. This results in better code quality and more security.

There is a necessary condition that whatever the callback function is should legitimately be a function. To prevent accidentally passing callback variables as something other than a function, we can put an “if” condition to check  typeof callback, and only execute further if it is of type “function”.

If(typeof callback === “function”){

//body of our function

}

Callbacks can be more than one function and can be passed as a parameter, as for a single callback.

var sum = function(a,b){

console.log("Callback")

}

var sum1 = function(a,b){

console.log("Callback2")

}

var b = 10;

var some_func= function( smthn , callback ){

console.log("containign func")

callback();

  smthn();

}

some_func(sum,sum1);

//output

containing func

Callback

Callback2

Here, we are passing in two callbacks and executing them one after another, as per our needs. This is the basic concept of callbacks.

Closures and callbacks are developed to facilitate ease of development for us and should be used as needed. Due attention needs to be paid while using them. Remember, closures are nothing but functions with preserved data. Similarly, callbacks can be generalized to “functions containing functions as parameters”.

Chapter 8: Apply, call, and bind methods in JavaScript

The apply(), call(), and bind() methods in JavaScript allow us to change the value of the "this" keyword with the help of some arguments. These methods are useful for calling a specified or targeted function. All three of these methods are closely related.

In this section, we will review these three methods of JavaScript in brief.

The ‘this’ keyword

Before diving into the details of apply(), call(), and bind() methods, we need to know about the keyword “this” in JavaScript.

In terms of global context

The keyword “this” refers to the global object outside of any method. In the following example, we will see the scope of this keyword in the global context. We will just console.log the “this” keyword in the browser.

console.log(this);

The result in the console is “window”, which is nothing but the global object. This result implies that:

console.log(this === window); // is true

In the example above, we entered console.log(this) which gave us window object.

In this example, we will use strict mode and check the value of the “this” keyword.

function abc(){

'use strict'; // the strict mode

return this;

}

console.log(abc()); // undefined

This time, the value of the ‘this” keyword is undefined because it was not defined inside the function abc().

In terms of function context

Addressing the “this” keyword in terms of function context, we have the three methods call(), apply(), and bind().

Let’s talk about these methods in detail.

The apply method

The apply() method invokes a function with the value of “this” keyword, and parameters provided as an array (or an array-like object).

Syntax:

The method apply() has the following syntax:

functionName.apply(thisArgument, argsArray[])

Parameters

Let's have a look at the arguments provided to the apply() method.

● thisArgument: The value of keyword "this" provided for the invoke the functionName.

Note: The value of the keyword "this" may not be the original value seen by the function when working in non-strict mode. The primitive values and the global object will be replaced by “undefined” and “null”.

● argsArray[]:  An argument of an array-like object that specifies the arguments with which functionName should be called, or undefined or null if no arguments should be provided to the method.

Example:

In the following example, we will take a look at the basic functionality of the apply() method.

var student1 = {firstName: 'Abhishek', lastName: 'Kumar'};

var student2 = {firstName: 'Ashok', lastName: 'Mehta'};

function text(hello) {

    console.log(hello + ' ' + this.firstName + ' ' + this.lastName + ' ?'  );

}

text.apply(student1, ['How are you']); // How are you Abhishek Kumar ?

text.apply(student2, ['How are you']); // How are you Ashok Mehta ?

The call method

The call() method invokes a particular function with the help of the "this" keyword and an individual argument.

Syntax:

The method call() has the following syntax:

functionName.call (thisArgument, argument1, argument2, ....)

Parameters

Let's have a look at the arguments provided to the apply() method.

● thisArgument:  The value of keyword "this" provided for the invoke the functionName.

Note: As with the apply() method, the value of keyword "this" may not be the original value seen by the function when working in non-strict mode. The primitive values and the global object will again be replaced by undefined and null.

● Argument1, 2 … :Arguments for the different functions

Example:

var student1 = {firstName: 'Abhishek', lastName: 'Kumar'};

var student2 = {firstName: 'Ashok', lastName: 'Mehta'};

function text(hello) {

    console.log(hello + ' ' + this.firstName + ' ' + this.lastName + ' ?' );

}

text.call(student1, ['How are you']); // How are you Abhishek Kumar ?

text.call(student2, ['How are you']); // How are you Ashok Mehta ?

The bind method

The method bind() calls a newly created function (created by the method itself), which has the value of the keyword "this" set to the specified value, with a given pattern of parameters.

Syntax:

The method call() has the following syntax:

function.bind (thisArgument[, argument1[, argument2[, ...]]])

Parameters

Let's have a look at the arguments provided to the apply() method.

● thisArgument: The value to be passed as the keyword this argument to the specified function when the bound function is invoked.

If the bound function is created using the new operator, the value will be ignored.

● argument1,[, argument2[, ...]]]: Arguments attached to arguments provided to the bound function when calls the specified function.

Example:

var student1 = {firstName: 'Abhishek', lastName: 'Kumar'};

var student2 = {firstName: 'Ashok', lastName: 'Mehta'};

function text() {

    console.log('hello' + ' ' + this.firstName + ' ' + this.lastName + ' ?');

}

var textHelloAbhishek = text.bind(student1);

var textHelloAshok = text.bind(student2);

textHelloAbhishek(); // How are you Abhishek Kumar ?

textHelloAshok(); // How are you Ashok Mehta ?

Difference between apply, call and bind

The apply() method calls the function and allows you to pass in parameters as an array or an array-like object.

The call() method calls the function and allows you to pass in parameters one by one.

The bind() method returns a newly created function and allows you to pass in any number of arguments.

Now that we know what the call(), apply(), and bind() methods in JavaScript are, the question still remains “when do I use which methods”?

In this section, we will clear this confusion by comparing all of them based on a few parameters.

The method call(), and apply() are somewhat interchangeable, depending on how you as the programmer decide to utilize them. You have a choice to determine whether it is easier to send a list of arguments separated by commas, or an array of arguments.

The bind() method is a bit different from the other two.

Where the apply() and call() methods execute the current function on the spot, the bind() method returns a newly created function.

A bind() method can be used for events such as onClick, where the firing of such events is uncertain.

We as programmers can't predict when those events will be fired, but we can serve the context to them.

Chapter 9: Collections in JavaScript

In JavaScript, a collection refers to the grouping of data. More specifically, it refers to incorporating the data in such a structure that we can access every value by its index, or by the key if it is in a key/value pair. Collections in JavaScript can be in many forms, like objects, arrays, functions, maps, and sets.

In this chapter, we will be focusing on data structures like objects and arrays to explore the concept. We will be learning about how to create an object/array, how to populate those arrays, and methods for iterating over arrays. We will also cover various other array methods like push, pop, sort, concat, indexOf, etc. Moreover, we will be discussing multi-dimensional arrays along with the single-dimensional arrays.

An array is a data-structure containing ordered set of values which can be referred to with its name or index. In JavaScript, we do not need to define specific data-type for each array during its declaration like in C, C++ or Java. Instead, we can use a predefined Array object and its various methods. An array can be created in any of the following ways:

For Ex: var fruitsArray = new Array(apple, mango, banana, orange);
OR var fruitsArray = Array(apple, mango, banana, orange);
OR var fruitsArray = [apple, mango, banana, orange];

In general, the third way of implementing Array is most commonly used (the one in square-bracket notation), and is known as ‘Array Literal’ or ‘Array Initializer’.

When we are not sure about the items to be populated in the array and want to push them into the array afterwards (but want to declare a non-zero length array right now), we can perform that action with:

var arr = [];

Remember that passing a single number value while declaring the array in the square-bracket notation [ ] denotes the value of that array, whereas passing a single number value to the Array function “()” notation denotes the length of that array and allocates the number of empty locations for that array accordingly.

For Ex: var arr = [10]; will create an array named arr with value 10

Whereas, var arr = Array(10); will create an array named arr with no elements but its length set to 10.

Populating an Array

Populating an array simply means assigning values to the array at different indices. A single value by default is populated at the 0th index of the array as:

arr[0] = ‘0th value’;

We can also populate the array at the time we create it as:

var fruitsArray = [apple, mango, banana, orange];

And then access each element from their index as:

console.log(fruitsArray[0]); will give us ‘Apple’ as a result.

But generally, we do not iterate over each index manually. Rather, we can use loops for that which automatically iterates over each index and each value of the array can be accessed accordingly.

For Ex: var fruitsArray = [apple, mango, banana, orange];

for(i = 0; i < fruitsArray.length; i++)

{

console.log(fruitsArray[i]);

}

The above code will give the output as:

apple

mango

banana

orange

Here, .length is a predefined array method used to determine the length of the array. It is beneficial for iterating over the arrays. The above output can also be obtained by using forEach loop instead of For loop as follows:

For Ex: fruitsArray.forEach(function(fruit){

console.log(fruit);

  });

Useful methods

We have already discussed one of the predefined Array methods, the .length method. There are many other methods too. These methods are defined over the Array object as follows:

push( ): This method is used for adding elements in an array. All the elements get added at the end of the array.

For Ex: var fruitsArray = [apple, mango, banana, orange];

fruitsArray.push(‘litchi’);

Now, the resulting fruitsArray would be

[apple, mango, banana, orange, litchi]

pop( ): This method is used for removing the last element from an array and also returns the removed element.

For Ex: var fruitsArray = [apple, mango, banana, orange];

var removedFruit = fruitsArray.pop();

Now, the resulting fruitsArray would be

[apple, mango, banana] and removedFruit = orange.

concat( ): This method is used for combining one array with another into a new array.

For Ex: var fruitsArray = [apple, mango, banana, orange];

var carsArray = [honda, suzuki, toyota];

var fruitsAndCars = fruitsArray.concat(carsArray);

Now, the resulting fruitsAndCars would be

[apple, mango, banana, orange, honda, suzuki, toyota];

sort( ): This method is used for sorting the array in an increasing order.

For Ex: var fruitsArray = [apple, mango, banana, orange];

fruitsArray.sort();

Now, the resulting fruitsArray would be

[apple, banana, mango, orange]

reverse( ): This method is used for reversing the order of elements of the array i.e first element becomes the last element and the last element becomes the first.

For Ex: var fruitsArray = [apple, mango, banana, orange];

fruitsArray.reverse();

Now, the resulting fruitsArray would be

[orange, banana, mango, apple]

indexOf(reqdElement, [fromIndex]): This method is used to search for the index of a particular element in an array.

For Ex: var fruitsArray = [apple, mango, banana, orange];

fruitsArray.indexOf(‘mango’); will give 1 as result.

If there is more than one element with the same name in an array, we can also specify which index we want to start looking for the required element, as an optional parameter.

For Ex: var fruitsArray = [apple, mango, banana, orange, mango];

fruitsArray.indexOf(‘mango’, 2); will give 4 as result.

Multi-Dimensional Arrays

A multi-dimensional array can be created by the nesting of one array into another array, and populating each element for one dimension to each element of another dimension. A multi-dimensional array can be created and populated as follows:

For Ex: var arr = new Array(5);
for (i = 0; i < 5; i++) {
 arr[i] = new Array(5);
 for (j = 0; j < 5; j++) {
   a[i][j] = i + j;
 }
}

The above code, when logged at console, will give the following output:

00 01 02 03 04

10 11 12 13 14

20 21 22 23 24

30 31 32 33 34

40 41 42 43 44

This completes the explanation of the concept of collections in JavaScript. Use the knowledge wisely! Always think your code out before you write it. There are many ways to reach the end of a particular path. Structure is everything.

Chapter 10: Working with Canvas in JavaScript

The canvas element in HTML is responsible for displaying many graphics elements, such as drawing, animations, interactivities etc.

A simple canvas element looks like this:

<canvas id="idCanvas" width="300" height="300"></canvas>

At first, it looks like an <img> element, with the absence of src and alt attributes.

The default height and width of the canvas element is 300px and 150px, respectively. The height and width attributes of the canvas are optional and can be changed using DOM manipulations. The styling and appearance of the canvas can also be manipulated using CSS.

The id="idCanvas" plays a crucial role in selecting the canvas. The name of "id" can be anything you choose it to be. The canvas element is selected in this way:

var canvas = document.getElementById("idCanvas");

Once the canvas element has been selected, it can be easily modified using JavaScript's object-oriented methodology.

For example:

canvas.height= 100;

canvas.width=  100;

The fallback content

Canvas doesn't work in some old browsers, such as older versions of Internet Explorer or certain textual browsers.

To avoid any uncertainty, we generally include fallback content inside the canvas element. To do so, we need only to insert alternative text inside the canvas block.

For example:

<canvas id="idCanvas" width="300" height="300">

   The alternative text goes here.

</canvas>

If the browser doesn't recognize the canvas, it will render the alternative text and vice versa.

The required closing tag:

Like every other tag in HTML, the canvas tag also requires the closing tag. When using canvas elements, if the closing canvas tag is not provided, the rest of the document would be considered fallback content. It would then only display if a browser doesn't recognize the canvas.

Role of JavaScript in canvas

We have already seen a basic use of JavaScript with canvas in the glimpse we just took into the HTML canvas section, which was the selection of canvas using DOM properties.

var canvas = document.getElementById("idCanvas");

Now we will discuss the actual use of JavaScript on the canvas.

Initially, the canvas is completely blank. To draw something onto the canvas, JavaScript is needed to access the rendering context, with the help of a method called getContext();

This method has one parameter which defines the type of context.

For example:

getContext("2d");

To include this method in JavaScript, we first need to select the canvas and store it into a variable, just like we did earlier with the DOM properties.

Secondly, we have to use the same variable to connect the getContext method.

Finally, we must store this into another variable (usually named as 'ctx'), which we will be using for the rest of the project to manipulate canvas elements.

var canvas = document.getElementById("idCanvas");

var ctx    = canvas.getContext("2d");

Notice that the getContext method is connected by the same variable ('canvas') which we have created to store the selected canvas.

As the context has been created now, we can easily set different values for our canvas with the help of the variable 'ctx'.

For example:

1\. ctx.fillStyle="blue";

2\. ctx.fillRect(8,  8,  40,  40);

The above code will draw a rectangle with the given coordinates in line 2 and will provide a blue color as stated in line 1.

Drawing shapes in canvas

So far, we have discussed how to set up the canvas environment with basics of JavaScript. We will now advance our knowledge and learn how to draw shapes in canvas using JavaScript.

The canvas grid

The canvas grid or coordinate space helps us to draw shapes and figures precisely.

"1 unit or 1 block of canvas grid system is equivalent to 1 pixel."

Drawing rectangles

There are three methods that draw rectangles:

fillRect(A, B, width, height)

It draws a filled rectangle.

strokeRect(A, B, width, height)

It draws a rectangular outline.

clearRect(A, B, width, height)

Clears the specified rectangular area, draws a fully transparent rectangle.

The above three methods take some parameters in the format of:

A, B – specifies the relative position of the rectangle in the canvas grid.

width – specifies the width of the rectangle.

height – specifies the height of the rectangle.

Example:

<!DOCTYPE HTML>

<HTML>

<head>

<title>drawing rectangle</title>

</head>

<body>

<canvas id="idCanvas" width="200" height="100"

this browser does not support the canvas element.

</canvas>

<script>

var canvas = document.getElementById("idCanvas");

var ctx = canvas.getContext("2d");

ctx.fillStyle = "blue";

ctx.fillRect(0,0,150,75);

</script>

</body>

</HTML>

Drawing the paths

A path is basically a list of points or dots connected by a segment of lines. The shapes can be different or the same, different heights, widths, colors, etc.

It can even be closed or open.

Note about rectangles and paths:

The rectangle and path are the only primitive shapes in the canvas.

To draw any other shape of your choice and mind, you must draw it by connecting several paths.

How to draw any shape using paths:

The following methods are required to create, connect, and manipulate paths to form shapes.

1.  beginPath() method:

used to create a new path.

2\. path functions:

● CanvasRenderingContext2D.moveTo()

Moves the starting index of a newly created path to the (A, B) coordinates.

● .CanvasRenderingContext2D.bezierCurveTo()

Adds a curve to the path (also known as cubic Bézier curve).

● CanvasRenderingContext2D.lineTo()

connects the subpath to the A, B coordinates and the last point with a straight line.

● . CanvasRenderingContext2D.arc()

Adds an arc to the path centered at (A, B) position with radius r. starts at startAngle and ends at endAngle going in the given direction by anticlockwise.

● .  CanvasRenderingContext2D.ellipse()

An ellipse is added to the path centered at (A, B) position

having radiusX and radiusY as radii, start at startAngle and ends at endAngle going in the given direction by anticlockwise.

● . CanvasRenderingContext2D.fill()

subpaths get filled with the current fill style.

● .  CanvasRenderingContext2D.rect()

A path for a rectangle at position (A, B) is created with a size determined by respective width and height.

● .  CanvasRenderingContext2D.quadraticCurveTo()

A quadratic Bézier curve is added to the current path.

● .  CanvasRenderingContext2D.arcTo()

An arc to the path is added, including the given radius and the control points connected by a straight line to the previous point.

3\. closePath()

Closes the path. Let the next drawing commands to direct again.

4.fill()

By fill() method we can draw a solid shape filled with the content area.

5.stroke()

By stroke() method we can draw a border around the shape.

Following these steps will help you to draw any shape you can imagine using paths:

1\. Create a new path

2\. Draw into the path with the Drawing commands listed above.

3\. Close the path, once it has drawn. Your path has now been created.

4\. Once the creation of path is complete, you can easily manipulate it by either stroking or filling it.

5\. The path is now ready to render.

Drawing a triangle with paths

This section shows how to draw a triangle with paths. Take a look at the code examples below.

HTML code:

<!DOCTYPE HTML>

<HTML>

<body onload="drawTriangle();">

   <canvas id="idCanvas" width="100" height="100"></canvas>

</body>

<script type="text/JavaScript" src="new.js"></script>

</HTML>

JavaScript code:

function drawTriangle() {

  var canvas = document.getElementById('idCanvas');

  if (canvas.getContext) {

    var ctx = canvas.getContext('2d');

    ctx.beginPath();

    ctx.moveTo(50, 75);

    ctx.lineTo(95, 72);

    ctx.lineTo(101, 26);

    ctx.fill();

  }

}

Applying styles and colors to context

Next, we will take a look at how to add colors and style the shapes or contexts, according to our wishes.

The two important attributes

In order to add colors and style our shapes in the canvas, we must consider two important attributes.

1.  fillStyle = "color";
2.  strokeStyle = "color";

The fillStyle attribute sets the style while filling shapes and contexts

The strokeStyle attribute sets the style of the shape's border.

Notice the “color” written after the equals sign inside the quotes. It represents the color of your choice. This space must be filled by a string.

The color simply represents the CSS color: attribute. Color can accept values of the following type:

● Predefined colors name such as- "red", "blue", "green" etc.

● Can accept Hex codes of colors, for example- "#232323", "#ffffff" etc

● Can accept the rgb color codes for example -"rgb(255, 60, 16)";

Example of valid values of fillStyle and strokeStyle attributes

ctx.fillStyle="green";

ctx.fillStyle="#232323";

ctx.fillStyle="rgb(233, 30, 25)";

Example of fillStyle attribute

HTML code:

<!DOCTYPE HTML>

<HTML>

<body onload="usingFillStyle();">

   <canvas id="idCanvas" width="100" height="100"></canvas>

</body>

<script type="text/JavaScript" src="new.js"></script>

</HTML>

JavaScript code:

function usingFillStyle() {

  var ctx = document.getElementById('idCanvas').getContext('2d');

  for (var i = 1; i <= 6; i++) {

    for (var j = 1; j <= 6; j++) {

      ctx.fillStyle = 'rgb(' + Math.floor(245 - 42.5 * i) + ', ' +

                       Math.floor(245 - 42.5 * j) + ', 0)';

      ctx.fillRect(j * 35, i * 25, 25, 25);

    }

  }

}

Example of strokeStyle attribute

HTML code:

<!DOCTYPE HTML>

<HTML>

<body onload="usingStrokeStyle();">

   <canvas id="idCanvas" width="100" height="100"></canvas>

</body>

<script type="text/JavaScript" src="new.js"></script>

</HTML>

JavaScript code:

function usingStrokeStyle() {

    var ctx = document.getElementById('idCanvas').getContext('2d');

    for (var i = 1; i <=6; i++) {

      for (var j = 1; j <=6; j++) {

        ctx.strokeStyle = 'rgb(0, ' + Math.floor(245 - 42.5 * i) + ', ' +

                         Math.floor(245 - 42.5 * j) + ')';

        ctx.beginPath();

        ctx.arc(12.4 + j * 25, 12.4 + i * 25, 10, 0, Math.PI * 2, true);

        ctx.stroke();

      }

    }

  }

This concludes our examination of the concept of canvas in JavaScript. I hope you found it useful!

Chapter 11: Animations in JavaScript

When animating objects with JavaScript, the first two options available to us are:

1.  Using pure JavaScript with DOM properties.
2.  Using Canvas.

Animations with DOM properties

Animations with DOM properties are our easiest tool. We don't have to worry about the frames and grid management, which we would need to track if we were using canvas.

Animation with DOM properties is done by manipulating the objects under certain interval or timer.

Simple animation using JavaScript

In the following example, we will move a ball from one position to another with the help of DOM properties

HTML code:

<!DOCTYPE html>

<html>

<body>

<p>

<button onclick="movingBall()">Click to move ball</button>

</p>

<div id ="content">

<div id ="object"></div>

</div>

</body>

</html>

CSS code:

body{

  background-color: #fff;

}

#content {

  width: 400px;

  height: 400px;

  position: relative;

  background: #232323;

}

#object {

  width: 50px;

  height: 50px;

  border-radius: 50%;

  position: absolute;

  background-color: yellow;

}

JavaScript code:

function movingBall() {

  var elementA = document.getElementById("object");  

  var positionA = 0;

  var id = setInterval(frame, 5);

  function frame() {

    if (positionA == 350) {

      clearInterval(id);

    } else {

      positionA++;

      elementA.style.top = positionA + 'px';

      elementA.style.left = positionA + 'px';

    }

  }

}

Screenshot of the result:      

![](images/00001.jpeg) ![](images/00002.jpeg)

We can do many advanced animations in this fashion.

Working with Events

Animations in JavaScript can be triggered according to user’s actions.

Here is the list of some commonly fired events and their respective uses.

Example:

1\. The button should animate as soon as a user clicks on it.

2\. The Dropdown menu should animate when a user clicks on a particular button.

3\. The background transition should change on user's scrolling.

Ultimately, any basic animation should happen, whenever a user performs a particular action.

Some commonly used events for mouse

● onclick: Performs a given task when a user clicks the mouse.

● oncontextmenu: Performs a specific task when a user right-clicks the mouse.

● ondblclick:  Performs a specific task when a user double-clicks through the mouse.

● onmouseover: Performs a specific task when the pointer of the mouse is moved over an element.

● onmousemove:  Performs a specific task when the pointer of the mouse is moving.

● onmouseup: Performs a specific task when the mouse button is being released by a user from an element.

Some commonly used events for keyboard

● onkeydown: Performs a specific task when a user pressing any specified key.

● onkeypress: Performs a specific task when a user presses a key.

● onkeyup: Performs a specific task when a user releases a key.

Animations with canvas in JavaScript

The basic rule to animate or move any previously drawn shape on canvas is to redraw it, either logically or hard coded.

Simple animation steps

In this section, we will see how we can create a frame and animate the objects using predefined methods.

Steps to create a frame

1\. Use clearReact() method-

You need to clear the previously drawn shapes when the canvas gets filled by them. The method clearReact() helps in clearing the canvas.

2\. Save every time before you manipulate.

When you create a new setting and you want your previously drawn shape to be saved on the canvas, you must save your original state every time a new frame is created.

3\. Add animations

In this step, the actual rendering of the frame is completed.

4\. The restoration process.

Last but not the least, with whatever you have done so far, allow the canvas to restore before you create a new frame.

Animations according to you

In this section, we will examine some methods to control the animations.

1\. setInterval(method, delay)

Starts repeatedly executing the method specified by method every delay milliseconds.

2\. setTimeout(method, delay)

Executes the method specified by “method”, with the delay interpreted in milliseconds.

3\. requestAnimationFrame(function callback)

Asks the browser to call a specified method to update an animation before the next restoration, on your demand of performing the animation.

* 4\. windowRequestAnimation()

Animations can be done in a more smooth and effective manner by calling the frame of animation when the canvas is ready to paint the frame. The number of function callbacks is generally 60 times/second, which might get reduced to a lower rate while running in the background.

Example:

In the following example, we will use the canvas element with JavaScript for animation.

HTML code:

<!DOCTYPE html>

<html>

<body>

<canvas id="idCanvas"></canvas>

</body>

</html>

CSS code:

html{

Height: 100%;

Width: 100%;

Margin: 0;

Padding: 0;

}

body{

Height: 100%;

Width: 100%;

Margin: 0;

Padding: 0;

}

canvas{

Position: absolute;

JavaScript code:

const canvas = document.getElementById('idCanvas');

const context = canvas.getContext('2d');

let height, width, s = 1;

window.onresize = function resize() {

height = canvas.height = document.body.offsetHeight;

width = canvas.width = document.body.offsetWidth;

};

window.onresize();

context.fillStyle = 'white';

context.fillRect(0, 0, width, height);

(function loop() {

context.save();

  context.translate(width/2, height/2);

context.fillStyle = 'rgba(0,0,0,0.09)';

  context.fillRect(-width/2, -height/2, width, height);

let j = 0, k = 0;

  s += 0.001;

  for( let i = 0; i < 512; i++ ) {

const r = i * ((j / k) / 5);

    context.beginPath();

    context.fillStyle = `hsl(${i%360}, 100%, 50%)`;

    context.globalAlpha = r/(512 * ((2 / 3) / 5) / 2) + 0.1;

    context.translate(Math.sin(i * s) * (i * j++), Math.cos(i * s) * (i * k++));

    context.fillRect(0, 0, r, r);

    context.closePath();

    if( j > 2 ) j = 0;

    if( k > 3 ) k = 0;

}

  context.restore();

  requestAnimationFrame(loop);

}());

Screenshot of the result:

![](images/00003.jpeg)

Animations not only look interesting, but also leave a good impression on your project. In this chapter, we have seen two ways to implement animations in your web project. The first way was using pure JavaScript and DOM properties, while the second was using canvas.

Chapter 12: Memory leaks in JavaScript

Problems in computing are almost inevitable, and programming is no exception. There are several problems that a developer faces every day one of which is Memory Leaks. Even though the language you are working on is a memory-managed language, there may be instances where memory leaks go undetected by the many algorithms that are implemented to detect EXACTLY those memory blocks which can be freed up.

The automatic garbage collection process in high-level languages creates an impression on the developer to not worry about memory management in their applications, which unfortunately is a widespread misconception. Memory leaks become much more severe by giving rise to problems like application crashing, high latency, and slowdowns which act as obstacles to a hassle-free user experience.

Diving into memory leaks

What are memory leaks? To accomplish a task, applications occupy a certain amount of memory from the free memory pool. Generally, this memory should be returned after the accomplishment of the task, since a system has fixed amount of memory. For reasons still unknown, these garbage memory blocks may still be occupied by the application. These instances are termed “memory leaks”. The memory management process depends on the language you are working on. The language can employ several methods for memory management.

Many programming languages don’t use a memory management algorithm, but rather leave the entire process to the developers. The programming language C has memory management primitives like calloc(), malloc(), realloc() and free(). The whole task of memory management falls on the developer to call these functions as per his/her understanding of the program, to free up memory blocks that should be unused.

Finding unused memory blocks is a very troublesome problem. Those memory blocks which can’t be reached by the program can be detected using the garbage collection algorithms stated earlier. Despite the language or programmer’s attempts to mitigate the problem, there are often cases where some unused memory blocks remain captured by the program. The whole logic for memory management depends on the application and its developer. The capability of an individual block of memory to be freed or not can be readily determined by going through the code and its logic. This cannot be done by an algorithm, and has to be done manually by the developer himself/herself. For now, we will only concentrate on JavaScript, its memory management process, and certain algorithms which are used to reduce memory leaks.

Memory life-cycle

Regardless of the language you are working on, memory life-cycle pretty much remains the same. The life-cycle of memory consists of three phases:

•   Memory allocation.

•   Use the allocated memory either by writing or reading.

•   Free up the memory when not in use.

Efficient usage of memory has always been troublesome for developers, and will always be. However, the first and third steps differ in low-level and high-level languages. High-level languages implement it implicitly (done by the language automatically), whereas low-level languages implement it explicitly (has to be done by the programmer himself/herself).

Memory allocation

Memory can be allocated mainly in two ways:

•    Value Initialization: JavaScript allocates memory while declaring values.

var number = 1234;//This allocates memory for a variable ‘number’ of type number

var name = ‘John’; //This allocates memory for a variable ‘name’ of type string

var obj = {

    x: ‘name’,

    y: 8

}//This allocates memory for an object ‘obj’ and the values contained in it.

var arr = [2, 3, 4, 5];//This allocates memory for an array of numbers

function add5(num1){

return num1+5;

}//allocated memory

•     Function Calls: Some function calls also result in the allocation of memory for an object.

var date = new Date(); //This allocates memory for date object

Garbage collection

As mentioned before, certain algorithms are implemented to find the memory blocks which are unused by the application and available to be freed up. Here, we are going to look into the two most important garbage collection algorithms and their limitations:

•    Reference Counting Garbage Collection

•    Mark-and-Sweep Algorithm

Reference counting garbage collection

Many popular languages, such as PHP and Python, implement this algorithm. It’s based on the idea that if there are no references to an object, it can be freed up. It considers an object with zero references to be an object which is no longer in use by the application.

var obj = {obj1: {x:3}, c:3, d: 4};

obj -----> obj1 //As one object references another, neither of them can be freed up

obj = 0; //Now, no object references to 'obj1' and hence this can be freed up

LIMITATION:

This algorithm tends to fail when objects create a reference cycle, as explained in the example below:

var obj1 = {}

var obj2 = {}

obj1.x = obj2;

obj2.x = obj1;

This creates a reference cycle between objects 'obj1' and 'obj2'. Let this code snippet be a part of a function, or any local scope. When the program goes out of this scope, both these objects become useless and hence should be freed up as they are no longer in use. The reference counting algorithm fails to free the memory taken by these objects as they both have at least one reference to them.

Mark-and-sweep algorithm

When an individual object is unreachable by the application, the mark-and-sweep algorithm returns the memory occupied by that object to the free memory pool.

Though the reference cycle problem no longer prevails in this algorithm, there can be instances when some zombie memory blocks aren’t released as the algorithm considers them to be reachable.

Common mistakes in JavaScript leading to memory leaks

•    Accidental Global Variables

•    Closures

•    DOM References to Removed Elements

•    Forgotten Callbacks

While some languages do provide garbage collection mechanisms, they do not prove to be universally effective. It ultimately depends on the programmer to keep track of the memory usage and try to free up memory explicitly wherever possible. Doing so adds to the potential of the garbage collection mechanism employed by the language to reduce any such error of memory leaks.

Chapter 13: Recursion in JavaScript

Recursion is a programming technique, which can be used in almost all programming languages. It is not a function or a data type. It is a type of architecture, a design pattern, or a type of coding style to solve a particular problem.

What is Recursion?

Recursion is the act of calling a function from within the function itself. It may sound simple, but can be a complex concept to grasp in practice. Many programmers struggle to understand on how to use this technique properly. This process of calling the function from within itself goes on until the desired goal is achieved.

Recursion is a loop. You repeat the same set of code again and again, as the function calls itself from within itself. You can generally achieve the same goal using recursion or using a loop. Most recursive algorithms can be recreated by using loops.

Recursion Examples

Let us take a look at some examples of loops, and the equivalent recursion for accomplishing the same goal.

We will start by printing numbers from 0 to 10\. When using a loop, the code will look something like this:

for(var i = 0; i <= 10; i++) {

console.log( i );

}

Now let us take a look at the recursive technique to print all the numbers from 0 to 10:

function printNumbers(x) {

console.log( x );

X++; // incrementing x’s value

if(x < 10)printNumbers(x);

}

printNumbers(0); // calling function once to initialize process

Both pieces of code do the same thing. With the recursion technique, you can see that we have an ‘if’ statement that checks whether x’s value is less than 10\. If it is less than 10, the function is called again. We need to have these types of checks if using the recursion technique, or else the recursion process will go on forever.

Let us move onto more difficult problems. We will try getting the factorial of a number, which is the product of all the natural numbers up to that number.

First, let us do it with help of a loop:

var number = 6; // number to get the factorial of

function getFactorial(x) {

var r = 1;

for(var i = 1; i <= number; i++) {

r = i * r;

}

return r;

}

var result = getFactorial( number );

console.log( 'Factorial of number ' + number + ' is ' + result );

Now, let us see how to do it via recursion:

var number = 6; // number to get the factorial of

function getFactorial(x) {

if(x == 1) return x;

return x * getFactorial( --x ); // recursion!

}

var result = getFactorial( number );

console.log( 'Factorial of number ' + number + ' is ' + result );

What happens here is that we decrease x’s value by 1 every instance before we make the recursive call. We check to see “if x’s value is 1, then return x” which is 1\. Until the value of x reaches 1 there is a stack of calls that multiply each number up to 1. As soon as 1 is returned, recursion stops and the factorial is returned.

Call getFactorial(6)

● Return 6 x getFactorial(5)step i

● Return 5 x getFactorial(4)step ii

● Return 4 x getFactorial(3)step iii

● Return 3 x getFactorial(2)step iv

● Return 2 x getFactorial(1)step v

● getFactorial(1) one returns 1 because of the check, so now values go up the queue that is mentioned above.

● Control moves to step v which now becomes: return 2 x 1 or return 2

● Control moves to step iv which now becomes: return 3 x 2 or return 6

● Control moves to step iii which now becomes: return 4 x 6 or return 24

● Control moves to step ii which now becomes: return 5 x 24 or return 120

● Control moves to step i which now becomes: return 6 x 120 or return 720

● Finally, the factorial of 6, i.e., 720, is returned.

Recursion disadvantages

While recursion can make a complex problem’s code shorter, it still has some major disadvantages that should be kept in mind when utilizing it in practice:

● It makes the code more difficult to understand.

● Each call to function gets stacked up in memory. A very long recursive chain can lead to filling all of the memory that the JavaScript engine is allocated, thus leading to unforeseen errors. Different machines may have different memory capacity.

● Recursion is slower than loops, as there must be a new call to function in each iteration. Every function call consumes some time.

Where to use Recursion?

Recursion should be used where there is a branching of loops, or too much nesting of loops. Operations such as searching through dynamic structures, traversing graphs, etc. can be made easy by using recursion. You should never use recursion for simple problems that can easily be solved by loops, as they are much faster and don’t use as much memory.

Many complex algorithms use recursions. It is a very powerful technique. JavaScript compilers stack each function call in recursion. This can be very dangerous, but in ES6( ECMAScript 6 ), this will no longer be the case. Instead of stacking, recursion will lead to immediate execution of code, which will make using recursion much safer.

Conclusion

Thank you very much for downloading JavaScript: Elite JavaScript Coding from The Ground Up! I hope you have gotten as much out of reading it as I have out of writing it. If you have enjoyed this book, please leave a positive review on Amazon to show your support. Your feedback is greatly appreciated!
![](images/calibre_cover.jpg)

Javascript: Objects, Functions, and Event Loops

by J Adrian Zimmer

Author's email: jazimmer@BonsaiReads.com.

Published by [Bonsai Reads](http://BonsaiReads.com) and distributed by Amazon.

Cover Design: J Adrian Zimmer

Copyright 2017 by J Adrian Zimmer

All rights reserved. Permission to copy is granted to the purchaser for personal use provided purchaser takes reasonable steps to prohibit further copying by others.

Edition: 1.0

There are two tables of contents. One is an annotated list of sections. The other has a listing for every major code segment.

Annotated List of Keywords

Javascript

For Javascript programmers who are ready to learn something more about how things work.

Objects

Javascript is object oriented, but not class oriented.

Functions

Javascript functions are callable objects.

Event

Events from outside the Javascript system cause handler functions to be queued for later execution.

Event Loop

Event loop processing chooses queued functions one by one for execution. Functions are usually, but not exclusively, queued as a response to an outside event.

Macrotask queue

Think of the macrotask queue as the event-handler queue.

Microtask queue

Think of the microtask queue as the me-first queue.

Promises

Promises handle asynchronous requests, sequencing follow up actions on the me-first queue.

Pseudo Classes

Javascript's clever use of `new` makes an object-based language look class-based.

Annotated List of Sections

[I. Object Inheritance](#index_split_005.html_filepos8396)

A quick look at the role of prototypes in object inheritance chains.

[II. Functions](#index_split_008.html_filepos15555)

Functions are callable objects which inherit their function characteristics.

[III. Centering Two Lines of Text](#index_split_014.html_filepos24867)

A webpage template for our example scripts.

[IV. Event Loops](#index_split_018.html_filepos30319)

Making use of an event handler.

[V. Multitasking with an Event Loop](#index_split_022.html_filepos37930)

Setting up two independent repeating processes.

[VI. Multitasking with Event Queuing](#index_split_027.html_filepos44854)

Eliminating `setTimeout` from repetitive processes.

[VII. Functions as Objects](#index_split_032.html_filepos59787)

Adding a state to `writeMessage` and `setColor`.

[VIII. Promises](#index_split_036.html_filepos66178)

How promises decouple the steps of a process while making use of a me-first queue.

[IX. Multitasking Example with Promises](#index_split_046.html_filepos85813)

Independent repeating processes with promises.

[X. Making Promises](#index_split_049.html_filepos91680)

Two examples in which promises manage responses to outside events.

[XI. Implementing `hesitating`](#index_split_056.html_filepos106371)

Implementing the `hesitating` factory method.

[XII. More on Object Orientation in Javascript](#index_split_059.html_filepos111516)

How the `new` operator fakes classes.

Preface

“Javascript: Objects, Functions, and Event Loops” is not an introductory book nor does it go into lots of detail. Rather it goes into depth about a few concepts whose Javascript variations confuse many programmers, namely objects, functions, promises, event loop programming, and the way Javascript fakes classes. The intent is to provide a solid base on which to continue building your understanding of Javascript. To that end, each section contains a single exercise which you should attempt before paging ahead to the answer. Even if you do not finish the exercise, the attempt will make the answer more meaningful and later sections more intelligible.

It is assumed that you already know some Javascript and are familiar with class-based object orientation as found in languages such as Java and Python.

This ebook has a [Github repository](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/) where you can find downloadable copies of the answers to exercises. It also contains two useful factory methods.

Be aware that the formatting of scripts and interactive sessions in this ebook is not meant to be exemplary. Rather it is meant to produce short lines so that the scripts can be read more easily on small screens.

You can recognize interactive sessions because they have lines beginning with `>`. They are transcribed from the [Node.js](https://nodejs.org/) interpreter but the transcriptions have many appearances of `undefined` removed. For example

> `> var x = 'hi'`
> `undefined `
> `> console.log(x)`
> `hi`
> `undefined`

is transcribed merely as

> `> var x = 'hi'`
> `> console.log(x)`
> `hi`

Both `var` and `console.log` actually return `undefined` but to see that in the transcript is confusing because we do not think of them as returning anything.

I. Object Inheritance

A counting object in Javascript might be defined this way

> `var counter = { `
> `  val: 0,`
> `  incr: function() { `
> `          this.val += 1; `
> `          return this.val `
> `        }`
> `}`

Do not confuse this with a class. It is an object. As you will see, it can inherit from other objects in much the same way that classes can inherit from other classes. But it is nevertheless an object.

Both `val` and `incr` are properties of the object. You can see that one represents an integer and the other a function. The property `incr` would normally be called a “method”. Methods can be assigned this way because functions can be assigned to variables and properties. They can be passed as arguments and can serve as return values. In other words they are first class. (Yep, the “class” in “first class” is different than the object-oriented “class”.)

Javascript has a built-in object named `Object` whose methods help programmers manipulate objects. Two example methods are `getOwnPropertyNames` and `getPrototypeOf`. When applied to `counter` these functions produce

> `> Object.getOwnPropertyNames(counter)`
> `[ 'val', 'incr' ]`

and

> `> var getP = Object.getPrototypeOf;`
> `> getP(counter)  === Object.prototype`
> `true`

To get “own” property names means to get the properties that are in the object itself and not those inherited from other objects.

The `getPrototypeOf` method returns the immediate predecessor of its argument in an inheritance chain. You can think of this as the “super” object. Often it is referred to as the [[Prototype]] of an object.

Many objects have a property named `prototype`. As you will see `prototype`s become [[Prototype]]s of other objects. They are not the [[Prototype]]s of the objects to which they belong. In some cases they may not be [[Prototype]]s of any object.

For example `Object.prototype` becomes the last object in the inheritance chains of most other objects. So most objects have access to a `toString` method because `toString` is present in `Object.prototype`.

There are other useful functions in `Object`. One I will make use of is `Object.create` which can create an empty object that has a designated [[Prototype]]. In particular this expression

> `Object.create{obj}`

creates a new empty object whose [[Prototype]] is `obj`.

Question

Implement `counter` as above and then

1.  create `counter2` which inherits from `counter` and adds a `decr` method which decrements `val` by 1.
2.  check to see what each of

    `Object.getOwnPropertyNames(counter2)`
    `Object.getOwnPropertyNames(counter)`

    returns. The answer isn't completely apparent from what has been said, so experiment a bit.

Answer

Create `counter2` this way

> `var counter2 = Object.create(counter);`
> `counter2.decr = function() { this.var -= 1 }`

The own properties of `counter` are of course

> `> Object.getOwnPropertyNames(counter)`
> `[ 'val', 'incr' ]`

However the order in which you see them will be depend on how the Javascript engine is implemented.

If you didn't get two different answers for the own properties of `counter2`, you missed something. Things change when you execute `incr` or `decr`.

Upon creation

> `> Object.getOwnPropertyNames(counter2)`
> `[ 'decr' ]`

but after either of `counter2.incr` or `counter2.decr` has executed, you will get

> `> Object.getOwnPropertyNames(counter2)`
> `[ 'decr', 'val' ]`

The reason is that `counter2` can fetch data values from `counter` through inheritance but it cannot alter them. When alteration is necessary a new property in `counter2` is made. After that, fetching from `counter2` will be of `counter2`'s property not its original in `counter`.

This means that `counter` can be used to give an initial value to any object for which it is a [[Prototype]].

II. Functions

Functions are callable objects which means:

*   they are objects containing the function body (probably in compiled form).
*   their inheritance chains have access to methods which can execute this function body.

The reason function objects can have access to methods which execute their code is that their inheritance chains have

> `Function.prototype`

inserted in them. There are two methods in `Function.prototype` which can execute a function, namely `apply` and `call`.

The following short interactive session shows the inheritance chain of a function.

Clarifing `Function.prototype`

> `> var getP = Object.getPrototypeOf;`
> `> function f() {}`
> `> getP(f)===Function.prototype`
> `true`
> `> getP(Function.prototype)===Object.prototype`
> `true`

Both `apply` and `call` require an argument which specifies which object `this` will refer to when the function is executing. In addition both these functions accept a list of normal arguments. They differ only in the way the arguments list is specified. You can see the difference in the following example.

Difference between `call` and `apply`

Assume this definition

> `function f(x,y) { return x+y }`

Then this

> `f.call({},2,3)`

and this

> `f.apply({},[2,3])`

will both return 5.

In both cases `this` refers to an empty object.

A more informative example involves this function

> `function f(x) { return x+this.y }`

which expects to be executed in the context of a `this` object that contains `y`. Execute it this way

> `f(2)`

and `this` will refer to the global object. Execution will fail unless `y` has been assigned a value globally.

Another way to execute `f` is

> `> var obj = {f:f, y;3}`
> `> obj.f(2)`
> `5`

This works because `obj` contains both `y` and `f`. If `f` is missing from the object then it won't work.

> `> var obj = {y:3}`
> `> obj.f(2)         // nope`

What `call` and `apply` do is allow `this` to refer to a different object than `f` is executed from. For example we can execute `f` from the global object with `this.y` taken from a different object this way

> `> Object.apply({y:3},f)`
> `5`

To summarize: functions are callable objects, methods are functions, and `this` is determined by the context in which a function is executed. You can mess with that context by using `call` or `apply`.

You can read more about `this` in the next section.

Question

When a function `f` executes, the object pointed to by `this` is determined by the context in which it executes. What if that is not wanted? Suppose I want the `this` in a function definition to point to the same thing regardless of context. That can be accomplished with either `call` or `apply` but these functions are unpleasant to use.

This is a problem you can fix. Create a factory method `fixThis` such that

> `f.fixThis(obj);`

will return a function just like `f` except that its `this` pointer will always reference `obj`. For example

> `> function f(z) { return z + this.x }`
> `> var x = '?'`
> `> f('hi')`
> `'hi?'`
> `> var obj = { x: '!' }`
> `> var g = f.fixThis(obj)`
> `> g('hi')`
> `'hi!'`

You may know that `Function.prototype` already contains a function `bind` which behaves like `fixThis`. Using that function would be to miss the point of this exercise.

Answer

You probably figured out that the definition needs to start this way

> `Function.prototype.fixThis = function(obj) {`
> `   …`
> `}`

and that you need to define a function for `fixThis` to return. That function must execute `f` with `apply` or `call`. At that point you may have gotten stuck because you were not sure how to refer to `f`. To get that right you needed to remember two things: that `f` is the object that `this` will refer to in `f.fixThis` but that `f` is not the object `this` will refer to in the function that `f.fixThis` returns. If need be, try again with this insight in mind.

The answer appears on the next page.

Implementation of `fixThis`

> `Function.prototype.fixThis = function(obj) {`
> `   var that = this;`
> `   return function() { `
> `              return that.apply(obj,arguments);`
> `          }`
> `}`

As you probably know, `arguments` is a pseudo array containing whatever arguments have been passed to the function it is contained in.

III. Centering Two Lines of Text

Javascript normally runs in a browser and is initiated from an HTML page. I have chosen to use basically the same web page for my examples and exercises. This web page displays two lines of text centered vertically and horizontally. Taking a break from the subject of this ebook, I show how this centering can be done.

To begin with, I create a separate `div` for each line this way

> `<div id='upper' class="upper_center"></div>`
> `<div id='lower' class="lower_center"></div>`

Assuming each `div` will get one line of text I can center them horizontally with CSS's `textalign` and vertically by absolutely positioning `upper` so that its bottom margin is 50% of the page and `lower` so that its top margin is 50% of the page.

The next page shows a template for the web pages you will be asked to create in the exercises.

Template for centering two lines

> `<!DOCTYPE html>`
> `<html>`
> 
> `<header>`
> `<title> `
> `Display? from "Javascript Objects, Functions, and Event Loops"`
> `</title>`
> `<style>`
> `.lower_center {`
> `   position:absolute;`
> `   width:100%;`
> `   text-align:center;`
> `   top:50%;`
> `}`
> `.upper_center {`
> `   position:absolute;`
> `   width:100%;`
> `   text-align:center;`
> `   bottom:50%;`
> `}`
> `</style>`
> `LOAD SCRIPTS HERE`
> `</header>`
> 
> `<body>`
> `<div id='upper' class="upper_center">upper</div>`
> `<div id='lower' class="lower_center">lower</div>`
> 
> `<script type="text/javascript">`
> `INCLUDE SCRIPT HERE`
> `</script>`
> `</body>`
> 
> `</html>`

If your browser is rather recent you can place text in the `div`s with the `innerText` property as in

> `document`
> `  .getElementById('upper')`
> `  .innerText               = "Hi there!";`

But I don't care how you do it. Use jQuery if you like.

Question

Fill in

> LOAD SCRIPTS HERE

and

> INCLUDE SCRIPT HERE

such that these two lines

> `Line one.`
> `Line two.`

are written with

> `writeMessage("Line One","Line Two")`

Answer

LOAD SCRIPTS HERE

remove

INCLUDE SCRIPT HERE

> `function writeMessage(line1,line2) {`
> `   document.getElementById('upper').innerText = line1;`
> `   document.getElementById('lower').innerText = line2;`
> `}`
> 
> `writeMessage("Line One","Line Two")`

This complete HTML is available at [Display1.html](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/Display1.html).

IV. Event Loops

You have probably had some experience with event listeners. What this section can do is fill in some details about how things work. It will also establish language for use in subsequent sections.

The first linguistic issue is the difference between “listener” and “event handler”. It is minuscule. Either can be a function defined by programmers to handle some kind of outside event. “Listener” emphasizes the source of the event and “event handler” emphasizes what will be done when the event has happened. I will use the terms almost interchangeably.

Assuming this function

> `function f(x,y) { return x+y }`

I will describe another function such as this

> `function t() { f(2,2) }`

as a task. Tasks take no arguments and return no values. They can be stored for later execution. In fact they often exist just to set up delayed execution of another function. A sequence of tasks can be queued and then executed one after the other without necessarily influencing each other.

In the example just given, the function `f` is said to be wrapped in the task `t`.

An event loop is a run-time system that takes tasks from a queue and executes them. Each task executes to completion before the next is executed.

Of course the rest of the world does not stand still while a task is executing. Incoming data arrives. Mouse clicks happen. Such things are the result of outside forces. They are events. Event loop systems have a mechanism for handling events without having any effect on the currently executing task. When the event-loop system becomes aware of an event, it wraps an event handler with an argument describing the event into a task and enqueues that task. To do this, the system interrupts the currently executing task. A task can be interrupted and restarted without being aware that the interruption has occurred. Actual processing of an event is left for a subsequent task.

Note:

> Of course an interruption may not be necessary on a multi-processor system but most software systems do not seem to have caught up with hardware in this respect.

I will use `addEventListener` to add listeners to a running Javascript session. The next page shows an example. Listeners are normally defined anonymously but in the following example I use the name `aHandler` so I can talk about the listener being added.

Example of adding a listener.

> `document`
> ` .addEventListener(`
> `   "click",`
> `   function aHandler (event) {`
> `      console.log(`
> `          event.pageX,`
> `          event.pageY`
> `      )`
> `   }`
> ` )`

After this, whenever a click event happens the run-time system creates an event object `E` and wraps `aHandler` with it this way

> `function() { aHandler(E) }`

The task is then enqueued.

For a mouse click, `E`'s content will include the screen coordinates `pageX` and `pageY` of the place where the mouse was when the click happened.

The queue where such tasks wait for execution is usually called an event queue. But event queues may contain tasks that do not handle actual events. In an acknowledgement of this, Javascript documentation writes “macrotask queue” instead of “event queue”.

Note:

> For those who would look this up know that, for silly trademark reasons, official Javascript documentation describes “ECMAScript” not “Javascript”.

Question

From [Section III](#index_split_014.html_filepos24867), fill in

> LOAD SCRIPTS HERE

and

> INCLUDE SCRIPT HERE

such that, when there is a mouse click over the screen, the display lines will be:

> `X coordinate: ``the X coordinate where the mouse clicked`
> `Y coordinate: ``the Y coordinate where the mouse clicked`

Use `writeMessage` from [Section III](#index_split_014.html_filepos24867) to create the splash page (i.e. the initial screen) with

> `writeMessage('Click','someplace');`

Answer

LOAD SCRIPTS HERE

remove

INCLUDE SCRIPT HERE

> `function writeMessage(line1,line2) {`
> `   document.getElementById('upper').innerText = line1;`
> `   document.getElementById('lower').innerText = line2;`
> `}`
> 
> `document`
> ` .addEventListener(`
> `   "click",`
> `   function aHandler (event) {`
> `     writeMessage(`
> `         'X coord: ' + event.pageX,`
> `         'Y coord: ' + event.pageY`
> `     )`
> `   }`
> ` )`
> 
> `writeMessage('Click','someplace');`

The complete HTML is available at [Display2.html](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/Display2.html)

V. Multitasking with an Event Loop

In Javascript when you want to put your own task on the event queue, you use the `setTimeout` function. Essentially what you are doing is enqueuing a handler for a timing event. For example, to cause a function `f` to be applied to arguments `"one"` and `"two"` after 5 seconds have elapsed you would write

> `setTimeout(`
> `    function () { f("one ","two ") },`
> `    5000`
> `)`

This creates an anonymous task that goes on the event queue after 5000 milliseconds have elapsed.

Note:

> Replace 5000 with 0 if you want the task to go on the queue immediately but remember that being placed immediately on the event queue is not the same thing as immediately executing.

The following page shows what you could write to repeat a task `t` every half second.

Using the event queue for repetition.

> `function t() {`
> `   …`
> `   setTimeout( `
> `      function() { t() },`
> `      500`
> `   )`
> `}`

This looks recursive but it is not. Recursive functions call themselves as they would any other function and they remain ready to continue executing when the called function returns. The kind of repetition `t` shows is different. Instead of calling itself, `t` finishes executing after having arranged for the Javascript engine to do the calling. Each execution of `t()` returns to the same place in the event loop where another task will be chosen for execution.

Before asking this section's question I want to provide you with some data. The next page shows three messages attributed to Mark Twain and an array of color declarations. You will use them in your answer.

Messages and Colors

> `var messages = [`
> `     "Politicians and diapers " +`
> `        "should be changed frequently",`
> `     "and for the same reason.",`
> `     "Actions speak louder than words",`
> `     "but not nearly as often.",`
> `     "Don't let schooling interfere",`
> `      "with your education" `
> `    ],`
> `    colors = ["BBFFFF", "FFBBFF", "FFFFBB"];`

Question

Fill in

> LOAD SCRIPTS HERE

and

> INCLUDE SCRIPT HERE

such that the display rotates through the three two-line messages in `messages` and the background color through the three choices in `colors`. These rotations should be independent of each other with the message changing approximately each 1500 milliseconds and the background color changing approximately each 850 milliseconds.

Answer

LOAD SCRIPTS HERE

remove

INCLUDE SCRIPT HERE

> `var messages = [`
> `   "Politicians and diapers should be changed frequently",`
> `   "and for the same reason.",`
> `   "Actions speak louder than words",`
> `   "but not nearly as often.",`
> `   "Don't let schooling interfere",`
> `    "with your education"`
> `];`
> `var colors = [ "BBFFFF", "FFBBFF", "FFFFBB" ];`
> 
> `function writeMessage(which) {`
> `   document.getElementById('upper').innerText = messages[2*which];`
> `   document.getElementById('lower').innerText = messages[2*which+1];`
> `   setTimeout(`
> `       function () { `
> `          writeMessage( (which+1)%3 )`
> `       },`
> `       1500`
> `   )`
> `}`
> 
> `function setColor(which) {`
> `   document.bgColor = colors[which];`
> `   setTimeout(`
> `       function () {`
> `          setColor( (which+1)%3 )`
> `       },`
> `       850`
> `   )`
> `}`
> 
> `writeMessage(0);`
> `setColor(0);`

The complete HTML is available at [Display3.html](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/Display3.html)

VI. Multitasking with Event Queuing

Event queuing is a name I give to a technique that simplifies writing the kind of script you wrote in the previous section's exercise. Event queuing replaces `setTimeout` with single-purpose function that can wrap and queue other functions. Suppose this

> `function f(x,y) { return x+y }`

were the function to be wrapped. Instead of doing it this way

> `setTimeout(`
> `   function() { f(2,2) },`
> `   0`
> `);`

event queuing does it this way

> `f.que(2,2)`

The syntax is pleasingly similar to

> `f(2,2)`

but the effect is the same as with `setTimeout`.

It is possible to implement `que` using techniques you have already seen: `setTimeout` will arrange for the actual enqueuing and `apply` will do the actual executing. So that `que` will be available to any `f`, it will reside in `Function.prototype`.

The next page shows my first (inadequate) attempt at implementing `que`.

Inadequate `que` function.

> `function.prototype.que = function() {`
> `   var that = this;`
> `   setTimeout( `
> `     function() {`
> `        that.apply({},arguments)`
> `     },`
> `     0`
> `   );`
> `}`

This definition of `que` works but I was dissatisfied with it for three reasons:

1.  the name `que` might not always be appropriate.
2.  `Function.prototype` ought not be altered without providing some notification of what has been done.
3.  there needs to be a way to choose a delay other than 0 milliseconds.

All three changes are possible if instead of defining `que` I define a factory function that makes `que`. I can pass the desired name and number of microseconds delay to the factory function. These choices will then be built into `que` whose name can be anything. Here is an example

> `> installQer('queue',3000)`
> `'queue' has been added to Function.prototype.`

This installs a method `queue` in `Function.prototype` and sends a message about the installation to the console. Given any `f`, the installation allows this statement

> `f.queue(2,2)`

to cause this task

> `function() { f(2,2) }`

to be enqueued after 3 seconds have passed.

Before I implement `installQer` there is a question I need to consider. It concerns the visibility of the method being installed. What, for example, should this loop

> `for(o in Function.prototype) console.log(o)`

display? The designers of Javascript chose not to let it display built-in functions such as `apply` and `call`. Feel free to disagree but I think a meethod installed by `installQer` is similar and so should be similarly invisible.

This kind of visibility is determined by something called a property descriptor. Javascript didn't always have descriptors and not all properties have them but many do. Descriptors are like objects in that they have their own properties but these descriptor properties are only used to provide information about the property they describe. One piece of information of course is the value assigned to the described property. The value is placed in the `value` descriptor property. Another descriptor property is `enumerable` which determines the visibility of the property being described.

The `Object.defineProperty` function is used to create a property with a descriptor. If `installQer`'s installations are to have the same limited visibility as the built-in functions, I must use it. Here is the general pattern

> `Object.defineProperty(`
> `object``,`
> `property name``,`
> `complete or partial descriptor object`
> `);`

When a partial descriptor object is used Javascript fills in default values.

The next page shows my implementation of `installQer`.

`installQer`

> `function installQer(desired_name,delay) {`
> `   delay = delay || 0;`
> `   Object.defineProperty( `
> `      Function.prototype, `
> `      desired_name, `
> `      { enumerable: false,`
> `        value: function() {`
> `           var that = this;`
> `           setTimeout( `
> `              ()=>that.apply({},arguments), `
> `              delay `
> `           ) `
> `       }`
> `     } `
> `   );`
> `   console.log( `
> `      desired_name + `
> `      ' has been added to Function.prototype'`
> `   )`
> `}`

This script contains another feature of Javascript which you may not be aware of, namely the use of `=>`. Know that

> `()=>that.apply({},args)`

stands for

> `function() {return that.apply({},args)}`

A more typical use might be

> `(x) => x+1`

Because event queuing sometimes comes in handy I have placed `installQer` in a script named [JavascriptEventLoopTools.js](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/JavascriptEventLoopTools.js).

If you place `JavascriptEventLoopTools.js` in a folder with your HTML pages, you can make its functions available by adding

> `<script type="text/javascript"`
> ` src="JavascriptEventLoopTools.js"> `
> `</script> `

to your HTML header.

Note:

> If this were a lecture there would be somebody at the back of the room who would tell me: "You didn't really remove `setTimeout`." These kinds of objections, which revolve around the semantics of words like “really”, always seem to come from the back of the room.

> I did remove `setTimeout` from the scripts we have to write. In so doing I made those scripts more intelligible and pleasing to look at. Of course `setTimeout` is hiding in `installQer` so, in a sense, it is not really removed.

Question

Fill in

> LOAD SCRIPTS HERE

and

> INCLUDE SCRIPT HERE

such that the display is the same as the previous section's exercise but the rotating of messages and background colors can be stopped by pressing the ESC key.

The implementation should expand this event handler

> `document`
> ` .addEventListener(`
> `    'keydown',`
> `    function (e) {`
> `      if(e.code=='Escape') {`
> `        …`
> `      }`
> `    }`
> `  )`

and make use of `installQer` instead of `setTimeout`.

Answer

LOAD SCRIPTS HERE

> `<script type="text/javascript"`
> ` src="JavascriptEventLoopTools.js">`
> `</script>`

INCLUDE SCRIPT HERE

> `var messages = [`
> `   "Politicians and diapers should be changed frequently",`
> `   "and for the same reason.",`
> `   "Actions speak louder than words",`
> `   "but not nearly as often.",`
> `   "Don't let schooling interfere",`
> `    "with your education"`
> `];`
> 
> `var colors = [ "BBFFFF", "FFBBFF", "FFFFBB" ];`
> 
> `var running = true;`
> 
> `installQer('q1500',1500);`
> `installQer('q850',850);`
> 
> `function writeMessage(which) {`
> `   if( !running ) return;`
> `   document.getElementById('upper').innerText = messages[2*which];`
> `   document.getElementById('lower').innerText = messages[2*which+1];`
> `   writeMessage.q1500( (which+1)%3 ) `
> `}`
> 
> `function setColor(which) {`
> `   if( !running ) return;`
> `   document.bgColor = colors[which];`
> `   setColor.q850( (which+1)%3 ) `
> `}`
> 
> `document`
> ` .addEventListener(`
> `     'keydown',`
> `     function (e) {`
> `        if(e.code=='Escape') running = false;`
> `     }`
> ` )`
> 
> `writeMessage(0);`
> `setColor(0);`

The complete HTML is available at [Display4.html](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/Display4.html).

VII. Functions as Objects

Since functions are objects, we can give them states that remember what they have done from one execution to the next. The following shows how I might add a state to `writeMessage`.

A Statefull `writeMessage`

> `function writeMessage() {`
> `   if( !running ) return;`
> `   var ms = writeMessage.messages,`
> `       i = 2*writeMessage.which;`
> `   writeMessage.which = (writeMessage.which+1)%3;`
> `   document.getElementById('upper').innerText = ms[i];`
> `   document.getElementById('lower').innerText = ms[i+1];`
> `   writeMessage.q1500()`
> `}`
> 
> `writeMessage.messages = [`
> `   "Politicians and diapers should be changed frequently",`
> `   "and for the same reason.",`
> `   "Actions speak louder than words",`
> `   "but not nearly as often.",`
> `   "Don't let schooling interfere",`
> `   "with your education"`
> `];`
> `writeMessage.which = 0;`

You can see that this state not only keeps track of which message to write next but it also adheres to the general rule: “Don't clutter your global namespace with names that are not needed there.”

Question

Fill in

> LOAD SCRIPTS HERE

and

> INCLUDE SCRIPT HERE

such that `writeMessage` and `setColor` are statefull.

Answer

LOAD SCRIPTS HERE

> `<script type="text/javascript"`
> `        src="JavascriptEventLoopTools.js">`
> `</script>`

INCLUDE SCRIPT HERE

> `var running = true;`
> 
> `installQer('q1500',1500);`
> `installQer('q850',850);`
> 
> `// Stateful writeMessage`
> 
> `function writeMessage() {`
> `   if( !running ) return;`
> `   var ms = writeMessage.messages,`
> `       i = 2*writeMessage.which;`
> `   writeMessage.which = (writeMessage.which+1)%3;`
> `   document.getElementById('upper').innerText = ms[i];`
> `   document.getElementById('lower').innerText = ms[i+1];`
> `   writeMessage.q1500()   // repeating`
> `}`
> `writeMessage.messages = [`
> `   "Politicians and diapers should be changed frequently",`
> `   "and for the same reason.",`
> `   "Actions speak louder than words",`
> `   "but not nearly as often.",`
> `   "Don't let schooling interfere",`
> `   "with your education"`
> `];`
> `writeMessage.which = 0;`
> 
> `// Stateful setColor`
> 
> `function setColor() {`
> `   if( !running ) return;`
> `   var cs = setColor.colors,`
> `       i = setColor.which;`
> `   setColor.which = (setColor.which+1)%3;`
> `   document.bgColor = cs[i];`
> `   setColor.q850()   // repeating`
> `}`
> `setColor.colors = [ "BBFFFF", "FFBBFF", "FFFFBB" ];`
> `setColor.which=0;`
> 
> `// Keystroke Event Handler`
> 
> `document`
> ` .addEventListener(`
> `   'keydown',`
> `   function (e) {`
> `     if( e.code=='Escape' ) running = false;`
> `   } `
> ` );`
> 
> `// Start`
> 
> `writeMessage();`
> `setColor();`

The complete HTML is available at [Display5.html](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/Display5.html)

VIII. Promises

Suppose you have three functions `f1`, `f2`, and `f3`. Suppose further you want `f2` to execute after `f1` has finished, but not necessarily immediately after. Instead you want already queued tasks to have their turn. Suppose further that you want `f3` to execute after `f2` in the same way. With the event queuing technique you would do something like the following.

Using `f1.que`, `f2.que`, and `f3.que` sequentially

> `function f1(``<f1 arg>``) {`
> `   …    `
> `   f2.que(…)   `
> `}`
> `function f2(``<f2 arg>``) {`
> `   …  `
> `   f3.que(…)   `
> `}`
> `function f3(``<f3 arg>``) {`
> `   …  `
> `}`
> 
> `f1.que( ``<f1 arg>`` )`

The `que` method wraps each `f`[`i`] in a task with an argument of your choice and places the task on the event queue.

Notice that the functions `f1`, `f2`, and `f3` are not independent of each other: `f2` is mentioned in `f1` and `f3` in `f2`. This can make it hard to reuse these functions for other purposes. For example, it will be hard to use `f1` in any setting where it is not followed by `f2`.

Promises allow `f1`, `f2`, and `f3` to be decoupled from each other. The next page shows how the decoupling works.

`f1`, `f2`, and `f3` with a promise

> `function f1(``f1 arg``) {`
> `   … `
> `   return ``<f1 return val>``;`
> `}`
> 
> `function f2(``<f2 arg>``) {`
> `   … `
> `   return ``<f2 return val>``;`
> `}`
> 
> `function f3(``<f3 arg>``) {`
> `   …   `
> `   return ``<f3 return val>``;`
> 
> `p.then(f1) `
> ` .then(f2) `
> ` .then(f3) `
> `}`

Here `p` is a promise that starts things up. All promises have a `then` method which creates another promise. There is much more to say about `p` and how <f1 arg> comes into the picture, but for now I'll focus on the sequencing of the `f`[`i`]'s. How promises are created will come up later in [Section X](#index_split_049.html_filepos91680) and [Section XI](#index_split_056.html_filepos106371).

Although specified differently, sequencing is similar to event queuing, the underlying mechanism will cause each `f`[`i`] to be wrapped and queued after `f`[`i-1`] has finished.

However unlike event queuing, each `f`[`i`] passes a value to the next by simply returning that value.

Another difference is that the queuing is not done on the event queue. An additional queue exists for use by promises. Because tasks on this additional queue have priority over tasks on the event queue, I call it the me-first queue. The real name however is the microtask queue.

Here is an example of resequencing the `f`[`i`]'s

> `p.then(f1) `
> ` .then(f3) `

and here is another

> `p.then(f1) `
> ` .then(f2) `
> ` .then(f2a) `
> ` .then(f3) `

Of course not all functions can be resequenced in these ways. Those which can include functions that act independently of each other and functions that act as filters for each other.

A final significant difference with event queuing is that promises give better control over error handling. Error handling is supported with a `catch` method; `catch` is similar to `then` but responds to error situations. The next page shows how `catch` methods might be interleaved with `then` methods.

A `then/catch` chain

> `p `
> ` .then(f1)    // p1`
> ` .catch(f2)   // p2`
> ` .then(f3)    // p3`
> ` .catch(f4)   // p4`

The p[i]'s refer to the promises created by the various `then`'s and `catch`'s. You can see that the first `catch` method belongs to p1 and produces p2, the second `then` belongs to p2 and produces p3, and so on.

The promises generated this way are all in a state known as `pending`. In general promises have three states: pending (waiting for something to happen), fulfilled (no error), and rejected (error). Fulfilled and rejected promises are said to be settled and they have promise values.

How `p` becomes settled is discussed in [Section X](#index_split_049.html_filepos91680). When `p` does become settled, a task capable of settling p1 will be enqueued, when p1 becomes settled a task capable of settling p2 will be enqueued, and so on.

Unlike event queuing, promises have a mechanism for transferring data from one step to the next. This mechanism passes the promise value of a settled promise to the next `f`[`i`].

The way any p[i] will be settled depends on whether it was generated with `then` or `catch` and on whether the previous promise has been fulfilled or rejected.

Previous promise fulfilled, p[i] from `then`:

In this case `f`[`i`] will be wrapped for execution; its argument will be previous promise value; p[i] will be fulfilled or rejected depending on the outcome from executing `f`[`i`]. Its promise value arises from the value `f`[`i`] returns.

Previous promise fulfilled, p[i] from `catch`:

In this case `f`[`i`] will not be executed; p[i] will be fulfilled and its promise value will be the same as the previous promise value.

Previous promise rejected, p[i] from `then`:

In this case `f`[`i`] will not be executed; p[i] will be rejected and its promise value will be the same as the previous promise value.

Previous promise rejected, p[i] from `catch`:

In this case `f`[`i`] will be wrapped for execution; its argument will be the previous promise value; p[i] will be fulfilled or rejected depending on the outcome from `f`[`i`]. Its promise value arises from the value `f`[`i`] returns.

Note:

> When `f`[`i`] is executed, the outcome can be a thrown error, a non-promise return value or a returned promise. If a thrown error, p[i] is rejected with the error object as its value. If a non-promise return value `rv`, p[i] is fulfilled with promise value `rv`. If the return value `rp` is a promise, p[i] is given the same state as `rp`.

The slightly more complex `then/catch` chain on the next page illustrates how error handling can work. Take the time to think about the ensuing explanation.

A `then/catch` chain

> `p             // assume fulfilled `
> ` .then(f1)    // p1`
> ` .then(f2)    // p2`
> ` .catch(f3)   // p3`
> ` .then(f4)    // p4`
> ` .catch(f5)   // p5`

If `f1` throws an error, `f2` will be skipped and `f3` will have a chance to repair the problem. If `f3` executes and simply returns a value, then that value will be assumed to be fulfilled and processing will continue with `f4`.

If neither p1 or p2 is rejected `f3` will be skipped and `f4` will receive the value that `f2` returned.

The final `catch` will execute `f5` if, and only if, a rejected promise has propagated to it.

Note:

1.  You might wonder what advantages event queuing can have over promises. The most obvious is that event queuing is easier to understand.
2.  Less obvious but important is that event queuing plays nice with event handlers. Because the settling of promises is done with tasks placed on the me-first queue, a promise programmer must be careful not to create an `then/catch` chain that will starve tasks on the event queue. That would make the script unresponsive to user input.
3.  I believe the sequencing flexibility of promise responders will encourage the development of utility functions in much the same way the flexibility of Unix pipes did.

Question

Assume there are two settled promises `p` and `q`, that `p` is fulfilled with promise value `'good'`, and that `q` is rejected with promise value `'bad'`. Assume also that we have a function

> `function s(x) { `
> `   console.log(x); return x+x;`
> `}`

This question has two parts, a and b.

Question: Part a

What be written on the console and what will happen to p1, p2, and p3 if the following executes?

> `p                   // p1`
> `  .catch(s)         // p2`
> `  .then(s);         // p3`
> `console.log("That's All Folks!")`

Answer: Part a

Nothing appears on the console while p1, p2, and p3 are being created. The first to appear will be “That's All Folks!!”

Later promise p2 will become fulfilled with promise value `'good'`. The `s` in `.catch(s)` will not execute.

Yet later the `s` in `.then(s)` will execute causing “good” to be written. Promise p3 will become fulfilled with promise value

> `'goodgood'`

So what you will see on the screen is

> `That's All Folks!`
> `good`

Question: Part b

What be written on the console and what will happen to p1, p2, and p3 if the following executes?

> `q                  // p1`
> ` .catch(s)         // p2`
> ` .catch(s)         // p3`
> ` .then( () => q )  // p4`
> ` .catch(s)         // p5`
> `console.log("That's All Folks!")`

Answer: Part b

Again “That's All Folks!” will be the first to appear on the console.

The `s` in the first `.catch(s)` will execute causing “bad” to be written on the console. The promise p2 will become fulfilled with promise value “badbad”.

The `s` in the second `.catch(s)` will not execute. The promise p3 will become fulfilled with promise value “badbad”.

The `()=>q` will execute. Promise p4 will become rejected with promise value “bad” (the same as `q`'s promise value).

The `s` in the third `.catch(s)` will execute causing `bad` to be written on the screen. Promise p5 will become fulfilled with the promise value `badbad`.

So what you will see on the screen is

> `That's All Folks!`
> `bad`
> `bad`

IX. Multitasking Example with Promises

This section is mostly an exercise asking you to rewrite the multitasking exercise in [Section VII](#index_split_032.html_filepos59787) with promises. However before you can do that, you need a way to generate an initial promise. The `hesitating` factory method can do that. It is found in [JavascriptEventLoopTools.js](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/JavascriptEventLoopTools.js). You first made use of this file in [Section VI](#index_split_027.html_filepos44854).

This statement

> `var p = hesitating(``<microseconds>``)`

will create a promise that will wait the specified number of microseconds before becoming fulfilled with an `undefined` promise value. While it is waiting, tasks on the event queue can execute. Using `hesitating` is the easiest way forward with the next exercise.

Question

Redo the multitasking exercise in [Section VII](#index_split_032.html_filepos59787). Fill in

> LOAD SCRIPTS HERE

and

> INCLUDE SCRIPT HERE

such that the event queuing methodology is replaced with promises.

Answer

No need to install anything in `Function.prototype` here. Instead `hesitating` is used in both `writeMessage` and `setColor`.

LOAD SCRIPTS HERE

> `<script type="text/javascript"`
> `        src="JavascriptEventLoopTools.js">`
> `</script>`

INCLUDE SCRIPT HERE

> `var running = true;`
> 
> `// Stateful writeMessage`
> 
> `function writeMessage() {`
> `   if( !running ) return;`
> `   var ms = writeMessage.messages,`
> `       i = 2*writeMessage.which;`
> `   writeMessage.which = (writeMessage.which+1)%3;`
> `   document.getElementById('upper').innerText = ms[i];`
> `   document.getElementById('lower').innerText = ms[i+1];`
> `   hesitating(1500).then(writeMessage)   // repeating`
> `}`
> 
> `writeMessage.messages = [`
> `   "Politicians and diapers should be changed frequently",`
> `   "and for the same reason.",`
> `   "Actions speak louder than words",`
> `   "but not nearly as often.",`
> `   "Don't let schooling interfere",`
> `   "with your education"`
> `];`
> `writeMessage.which = 0;`
> 
> `// Stateful setColor`
> 
> `function setColor() {`
> `   if( !running ) return;`
> `   var cs = setColor.colors,`
> `       i = setColor.which;`
> `   setColor.which = (setColor.which+1)%3;`
> `   document.bgColor = cs[i];`
> `   hesitating(850).then(setColor)   // repeating`
> `}`
> 
> `setColor.colors = [ "BBFFFF", "FFBBFF", "FFFFBB" ];`
> `setColor.which=0;`
> 
> `// Keystroke Event Handler`
> 
> `document`
> ` .addEventListener(`
> `   'keydown',`
> `   function (e) {`
> `     if( e.code=='Escape' ) {`
> `        running = false;`
> `     } `
> `   }`
> ` );`
> 
> `// Start`
> 
> `writeMessage();`
> `setColor();`

The complete HTML is available as [Display6.html](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/Display6.html)

X. Making Promises

You saw in [Section VIII](#index_split_036.html_filepos66178) how to use existing promises to decouple a chain of actions from each other. Another important use of promises is to make a request of an outside force. Making the request and channeling the response to a `then/catch` chain is the job of the script which creates the promise.

Here is how promises are created

> `var p = new Promise(e)`

where `e` is a function called an executor. I distinguish executors from functions passed to `then` and `catch` by calling those functions responders.

I'll first show how this works without the outside force: an executor takes two arguments, both functions, as in

> `function e(resolve,reject) { … }`

This executor

> `new Promise(`
> `  function f(resolve,reject) { `
> `     resolve('hi');`
> `})`

creates a promise which quickly settles with a fulfilled promise value of `'hi'`. Similarly this executor

> `new Promise(`
> `  function f(resolve,reject) { `
> `     reject('bad juju');`
> `})`

creates a promise which quickly settles with a rejected promise value of “bad juju”.

To demonstrate how to create a promise whose settling will depend on a response from an outside force I will continue with two examples of outside forces

1.  Node.js's run-time system which (in conjunction with your computer's operating system) can provide a file's contents.
2.  JQuery's `$.ajax` function which (in conjunction with your browser, your computer's operating system, a server, and a network) can provide the response to a request made to a server.

Both these examples will involve displaying a file `Sample.txt`. [Node.js](https://nodejs.org/), which the first example requires, is a Javascript interpreter that lacks access to a browser's DOM and but has file read/write capability.

JQuery, which the second example requires, can be loaded into your browser with an HTML `script` tag this way

> `<script`
> `src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js">`
> `</script> `

The second example also requires you to have an operational web server capable of serving `Sample.txt`. In theory you could just fetch `Sample.txt` from Github but cross origin security restrictions prohibit that. The easiest way to do the `$.ajax` exercise is to have `Sample.txt` and your HTML page in the same folder on your computer and set up your own web server. You can easily arrange for this through Node.js's `http-server` module. Install `http-server` with Node.js's `npm` and then run it from a folder containing `Sample.txt`. Be sure nothing you want to keep private is accessible through that folder.

Note:

> If you don't want to install these things, you can always answer this section's question with a paper and pencil effort. This is the only section in which you need these installations.

Reading a File

In Node.js you can read a file asynchronously this way

> `var fs = require('fs');`
> `    fs.readFile('Sample.txt','utf8',callback)`

where `callback` has been defined to handle both failed and successful reads like this

> `function callback(err,data) {`
> `   if(err)     ``handle error with`` err`
> `   then        ``handle success with`` data`
> `} `

Your operating system is an outside force that a script using `readFile` must wait on. The script could block until the read operation is finished (which would be the case with `readFileSync`) or it could make use of a callback as shown above with `readFile`. Using `readFile` is exactly the kind of situation that fits into a promise's executor. The next page shows how that might be done.

Reading with a promise.

> `var p = new Promise(`
> `         function (resolve,reject) {`
> `           function callback(err,txt) {`
> `             if(err)     reject(err)`
> `             then        resolve(txt)`
> `           } `
> `           fs.readFile(`
> `              'Sample.txt',`
> `              'utf8',`
> `              callback`
> `           )`
> `        }`
> `      )`

Notice I have not tried to process the text or the error message in the callback. I am letting the promise decouple that processing from this request. Given these functions for displaying errors and file contents

> `function showError(e) {`
> `   console.log(`
> `       "ERROR:\n" + e`
> `   )`
> `}`
> 
> `function showText(t) {`
> `   console.log(t)`
> `}`

here is one way the processing might be done

> `p.then(showText).catch(showError);`

and here is another

> `p.catch(showError).then(showText);`

The difference is that with the second way any error that happened to be thrown writing the text to the console wouldn't be handled.

Note:

> You would think that `showText` would not be needed as it could be replaced with `console.log`. It is one of Node.js's quirks that this does not always work.

Ajax

Simple requests for information over the world wide web can be made with JQuery's `ajax` method as shown in the following.

An `ajax` request

> `$.ajax({`
> `   url: "Sample.txt", `
> `   success: ``function to process text`
> `   error: ``function to process error object`
> `});`

I am going to put this in a web page that requests the file `Sample.txt` when the user clicks on a button. Two tweaks are needed to the template shown in [Section III](#index_split_014.html_filepos24867):

1.  A button is needed. Insert this

    `<button id='aButton'>Explain Things</button>`

    into the `upper` `div`.

2.  The fetched text may require more room than can fit in half the page. Shift things upward by changing the bottom margin of `upper` to %80 and the top margin of `lower` to 22%.

The 2% gap gives the button some room before the text starts.

Question

Fill in

> LOAD SCRIPTS HERE

and

> INCLUDE SCRIPT HERE

such that the web page will fetch (through `$.ajax`) and display `Sample.txt` when the user clicks on the button.

Know that it is the `'click'` event you want your `aButton` listener to respond to. Your response should create an appropriate promise with `then/catch` chain. If an error is reported, you can extract an error message from the `statusText` property of the error event.

You can write whatever you like on the page before the user clicks on the button.

This is a exercise, not an attempt to define production code. I am ignoring important things like how to let the user specify the file name and what to do if the network request times out and I am keeping `Sample.txt` hard-coded into the script. Rename the file in its folder if you want to test the error response.

Answer

Assuming the HTML display template in [Section III](#index_split_014.html_filepos24867) has been tweaked as described above the answer is:

LOAD SCRIPTS HERE

> `<script type="text/javascript"`
> `        src="JavascriptEventLoopTools.js">`
> `</script>`

INCLUDE SCRIPT HERE

> `function writeMessage(txt) {`
> `   document`
> `     .getElementById('lower')`
> `     .innerText = txt;`
> `}`
> 
> `document`
> ` .getElementById('aButton')`
> ` .addEventListener(`
> `   'click',`
> `   function() {  `
> `     var p = new Promise(`
> `               function(resolve,reject) {`
> `                  $.ajax({`
> `                    url: "Sample.txt", `
> `                    success: resolve ,`
> `                    error: reject `
> `               } ) }`
> `             );`
> `     p.then ( `
> `        writeMessage`
> `     ).catch(`
> `        err => writeMessage(err.statusText)`
> `     )`
> `   }`
> ` )`

The complete answer is available as [Display7.html](https://github.com/J-Adrian-Zimmer/JavascriptObjectsFunctionsAndEventLoops/blob/master/Display7.html)

XI. Implementing `hesitating`

The `hesitating` factory method, described in this section, was used in the exercise of [Section IX](#index_split_046.html_filepos85813) to make promises for our multitasking display. Only one argument was used there but `hesitating` can take two: the first is the number of microseconds to wait before the created promise becomes fulfilled and the second, optional argument, is the promise value to give to the fulfilled promise. In particular, this argument is the <arg 1> I neglected to work with in [Section VIII](#index_split_036.html_filepos66178).

If you have read through to here you should be able to implement the `hesitating` factory method yourself.

Question

Here is how the `hesitating` script begins

> `function hesitating(`
> `   micros,       // number of microseconds for the`
> `                 // returned promise to hesitate`
> `                 // before becoming settled`
> `                 // 0 if omitted`
> `   promise_val   // promise value of returned promise`
> `                 // undefined if omitted`
> `) {`
> `  // returns a promise that hesitates for the given `
> `  // number of microseconds before resolving with`
> `  // the given promise value  -- allows tasks`
> `  // on the event queue to execute before the`
> `  // effects of settling happen`
> `  micros = micros || 0;`
> `    … `
> `  );`
> `}`

Finish the implementation.

You can test your answer by replacing

> `<script type="text/javascript"`
> ` src="JavascriptEventLoopTools.js">`
> `</script>`

in Display6.html with

> `<script type="text/javascript">`
> `your definition of` `hesitating`
> `</script>`

Answer

This answer also appears in the `JavascriptEventLoopTools.js` file.

> `function hesitating(`
> `   micros,       // number of microseconds for the`
> `                 // returned promise to hesitate`
> `                 // before becoming settled`
> `                 // 0 if omitted`
> `   promise_val   // promise value of returned promise`
> `                 // undefined if omitted`
> `) {`
> `  // returns a promise that hesitates for the given `
> `  // number of microseconds before resolving with`
> `  // the given promise value `
> `  micros = micros || 0;`
> 
> `return new Promise(`
> `    function(resolve) {`
> `       setTimeout( `
> `          ()=>resolve(promise_val), `
> `          micros `
> `       )`
> `    }`
> `  );`
> `}`

XII. More on Object Orientation in Javascript

Object orientation involves defining kinds of objects and then creating working objects that match those definitions. The working objects are usually called instances. Object orientation also involves some kind of inheritance in which there can be refinements of existing kinds of objects.

Traditional languages like Java and Python have a concept of a class that is used for defining kinds of objects. An instance is constructed from a class and linked to that class. Javascript is different: kinds of objects are defined by example. That is to say you define a prototype object and instances are just new objects that inherit from the prototype.

With the class-based approach it is classes that do the inheriting. With the object-based approach it is objects that do the inheriting. Whether object based or class based the rules that inheritance follows are pretty much the same.

In [Section I](#index_split_005.html_filepos8396) and [Section II](#index_split_008.html_filepos15555) you saw two built-in `prototype` objects, `Object.prototype` and `Function.prototype`. Those prototypes provide services to all objects and/or functions. I use the word archetype for prototypes which define a kind of object that programmers define for their own use. The next page shows an example of an archetype with two instance variables and two methods.

An archetype

> `var archetype = { `
> `   x : 1,`
> `   y : 1,`
> `   add: function() {`
> `      return this.x+this.y;`
> `   },`
> `   double: function() { `
> `              this.x = 2*this.x;`
> `              this.y = 2*this.y`
> `   }`
> `};`

OK, it is a silly example but clear your mind of that and realize this is an object not a class. Archetypes are not meant to be used directly. Instances that inherit from them are constructed instead. Inheritance lets the archetype be an unchanging template for all instances of the same kind, that is to say all objects that directly inherit from the archetype. The unchanging aspect is what makes the archetype a reliable description of a kind of object.

In Java and Python, when a class is meant to have just one instance, it is said to be a singleton. This is a little weird as it is like defining a whole subspecies to describe your dog “Rover”. Rover would be the single instance of that subspecies or class. In Javascript you merely describe Rover and dispense with the subspecies. Said another way: in Javascript you describe a single object and dispense with the idea of an archetype. There is no need for the concept of singleton in Javascript. Such things are merely objects.

When archetypes are used to describe kinds of objects, it is the `create` method discussed in [Section I](#index_split_005.html_filepos8396) that creates instances. For example new instances `obj1` and `obj2` of `archetype` can be created this way

> `var obj1 = Object.create(archetype),`
> `    obj2 = Object.create(archetype);`

Because of the way inheritance works `obj1` and `obj2` are independent of each other. Changes to one do not impact the other. The first time `obj1.double()` or `obj2.double()` executes the inheritance search for values of `x` and `y` will take 1 from `archetype.x` and `archetype.y`. However the doubled values will not be assigned to the same `x` and `y` because there is no inheritance search when assigning a value. Instead new properties of `x` and `y` will be created in `obj1` or `obj2` and given the doubled values. From then on each instance is on its own.

In this example `obj1` and `obj2` are initialized with the same starting values. If they are to be initialized with different starting values, a constructor would be useful. A constructor is a function that

1.  creates a new object.
2.  initializes the instance variables of the newly created object.

Of course `Object.create` can perform the first step, but to get both steps we need to write our own constructor function. The next page shows one way to do this.

Archetypal construction

> `function Calc(x,y) {`
> `   var obj = Object.create(archetype);`
> `   obj.x = x;`
> `   obj.y = y`
> `   return obj;`
> `}`

This is a complete constructor. An instance can be created this way

> `> var obj = Calc(2,-3)`

This function may seem more like a factory method to you than a constructor because it makes no use of a `this` or `self` keyword. I think of it as a constructor because it is meant to create an instance rather that a specialized instance. If writing constructors without `this` or `self` disturbs you, you can make use of Javascript's `new` operator whose purpose is to fake class-based object orientation. With `new` you can define your constructor this way

> `function Calc(x,y) {`
> `   this.x = x;`
> `   this.y = y;`
> `}`

and your methods as shown on the next page

Pseudo-class construction

> `function Calc(x,y) {`
> `   this.x = x;`
> `   this.y = y;`
> `}`
> `Calc.prototype = {`
> `   add: function() { `
> `            return this.x + this.y`
> `   },`
> `   double: function() { `
> `              this.x = 2*this.x;`
> `              this.y = 2*this.y`
> `   }`
> `}`

When I first saw this way of defining methods, I thought it pretty weird. But it really isn't. The fact is that `Calc.prototype` is an archetype in disguise. That is to say each instance created with

> `new Calc(``args``)`

will have the same `Calc.prototype` as its [[Prototype]]. This is possible because the `function` statement that defined `Calc` created an empty `Calc.prototype` object which I later redefined. (Confused? Then recall that functions are callable objects. That is to say we can think of them both as functions and as objects.)

This is the way `new` works: all instances it creates inherit from a pre-existing `prototype` object. Once an instance is created, `new` runs your constructor. It does so in such a way that `this` refers to the newly created instance. You saw a way for `new` to do that in [Section II](#index_split_008.html_filepos15555).

So what is going on with `new` is really object orientation in the Javascript object-based system.

In the above definition I reassigned `Calc.prototype` to an archetypal object that contains the desired methods. I need to confess that this is not the normal way of defining methods. What you are more likely to see is shown on the next page.

Pseudo-class construction, common variation

> `function Calc(x,y) {`
> `   this.x = x;`
> `   this.y = y;`
> `}`
> `Calc.prototype.add = function() {`
> `                           return this.x+this.y;`
> `                        };`
> `Calc.prototype.double = function () {`
> `                           this.x = 2*this.x;`
> `                           this.y = 2*this.y`
> `                        }`

This style of defining a kind of object individually adds properties to `Calc.prototype`. Each addition preserves what is already there. Although this style is much more common I see no advantage to it because I prefer to write a complete definition in one place.

There is a third style for defining a kind of object which is useful in some situations and which emphasizes the similarities between using `new` or not. This style involves writing a setter for each instance variable. The setters are written in such a way that they can be chained together when instances are created. The obvious name for this technique is the chaining setter technique.

I'll show the chaining setter technique to you in both the archetypal and pseudo-class styles. The next page shows `Calc` defined in a chaining setter, archetypal style.

Archetypal, chaining setter style

> `> function Calc() {`
> `   return Object.create(`
> `            Calc.prototype`
> `          )`
> `}`
> `> Calc.prototype = {`
> `   x : 1,`
> `   y : 1,`
> `   setX:  function(x) { `
> `      this.x = x;`
> `      return this;`
> `   },`
> `   setY:  function(y) { `
> `      this.y = y;`
> `      return this;`
> `   },`
> `   add: function() {`
> `      return this.x+this.y;`
> `   },`
> `   double: function() { `
> `              this.x = 2*this.x;`
> `              this.y = 2*this.y`
> `   }`
> `};`
> `> var add1 = Calc().setX(2).setY(-3);`
> `> add1.add()`
> `-1`
> `> var add2 = Calc().setX(2);`
> `> add2.add()`
> `2`

Extrapolating from two instance variables, you can see that the chaining setter style is advantageous when there are a lot of instance variables and those instance variables have default values that seldom need overriding. In that case creating a new instance becomes easy.

Note:

> Does it bother you to use `Calc.prototype` within the definition of `Calc`? It works because, when `Calc` is executed, these things have happened;

> 1) the callable object `Calc` has been created.

> 2) an archetypal object has been assigned to `Calc.prototype`.

As shown on the next page, essentially the same definition works for the pseudo-classes.

Pseudo-class, chaining setter style

> `function Calc() { }`
> `Calc.prototype = {`
> `   x : 1,`
> `   y : 1,`
> `   setX:  function(x) { `
> `      this.x = x;`
> `      return this;`
> `   },`
> `   setY:  function(y) { `
> `      this.y = y;`
> `      return this;`
> `   },`
> `   add: function() {`
> `      return this.x+this.y;`
> `   },`
> `   double: function() { `
> `              this.x = 2*this.x;`
> `              this.y = 2*this.y`
> `   }`
> `};`
> `> var add1 = (new Calc()).setX(2).setY(-3)`
> `> add1.add()`
> `-1`
> `> var add2 = (new Calc()).setX(2)`
> `> add2.add()`
> `2`

Both variations of the chaining setter style create an object with this inheritance chain

1.  The instance
2.  The archetype (`Calc.prototype`)
3.  Object.prototype

Question

Implement a function `Construct` that can be used like this

> `var obj = Construct(Calc,2,-3);`

as a replacement for

> `var obj = new Calc(2,-3);`

One thing you will need to know to answer this question is how to remove the first argument from the pseudo-array `arguments`. Do it this way

> `var args = Array.from(arguments),`
> `    F = args.shift();`

Now `F` is the first argument and `args` is an array of the remaining arguments.

Answer

> `function Construct() {`
> `   var args = Array.from(arguments),`
> `       F = args.shift(),`
> `       obj = Object.create(F.prototype); `
> `   F.apply(obj,args);`
> `   return obj;`
> `}`

About the Author

J Adrian Zimmer

![](images/00001.jpg)

Zimmer is a Ph.D. mathematician who retired knowing more about computer science than about mathematics. He has taught at all levels from high school though graduate school. His expertise lies more in explaining things than in any one specialty.

His hobbies include biking, reading, American Sign Language, and watching the kind of movies that make one think about the various ways to be human.

(See also [jazimmer.net](http://jazimmer.net).)

[Title Page](#index_split_000.html_filepos319)

[Copyright Page](#index_split_001.html_filepos782)

[Annotated List of Keywords](#index_split_002.html_filepos1262)

[Annotated List of Sections](#index_split_003.html_filepos3042)

[Preface](#index_split_004.html_filepos5713)

[I. Object Inheritance](#index_split_005.html_filepos8396)

[Ia Question](#index_split_006.html_filepos12404)

[Ib Answer](#index_split_007.html_filepos13224)

[II. Functions](#index_split_008.html_filepos15555)

[IIa Clarifing Function.prototype](#index_split_009.html_filepos16634)

[IIb Difference between call and apply](#index_split_010.html_filepos17631)

[IIc Question](#index_split_011.html_filepos20908)

[IId Answer](#index_split_012.html_filepos22788)

[IIe Implementation of fixThis](#index_split_013.html_filepos24075)

[III. Centering Two Lines of Text](#index_split_014.html_filepos24867)

[IIIa Template for centering two lines](#index_split_015.html_filepos26224)

[IIIb Question](#index_split_016.html_filepos28785)

[IIIc Answer](#index_split_017.html_filepos29454)

[IV. Event Loops](#index_split_018.html_filepos30319)

[IVa Example of adding a listener.](#index_split_019.html_filepos33438)

[IVb Question](#index_split_020.html_filepos35378)

[IVc Answer](#index_split_021.html_filepos36444)

[V. Multitasking with an Event Loop](#index_split_022.html_filepos37930)

[Va Using the event queue for repetition.](#index_split_023.html_filepos39329)

[Vb Messages and Colors](#index_split_024.html_filepos40677)

[Vc Question](#index_split_025.html_filepos41588)

[Vd Answer](#index_split_026.html_filepos42292)

[VI. Multitasking with Event Queuing](#index_split_027.html_filepos44854)

[VIa Inadequate que function.](#index_split_028.html_filepos46803)

[VIb installQer](#index_split_029.html_filepos51836)

[VIc Question](#index_split_030.html_filepos55542)

[VId Answer](#index_split_031.html_filepos56809)

[VII. Functions as Objects](#index_split_032.html_filepos59787)

[VIIa A Statefull writeMessage](#index_split_033.html_filepos60133)

[VIIb Question](#index_split_034.html_filepos61914)

[VIIc Answer](#index_split_035.html_filepos62343)

[VIII. Promises](#index_split_036.html_filepos66178)

[VIIIa Using f1.que, f2.que, and f3.que sequentially](#index_split_037.html_filepos66873)

[VIIIb f1, f2, and f3 with a promise](#index_split_038.html_filepos69202)

[VIIIc A then/catch chain](#index_split_039.html_filepos73572)

[VIIId A then/catch chain](#index_split_040.html_filepos79067)

[VIIIe Question](#index_split_041.html_filepos81352)

[VIIIf Question: Part a](#index_split_042.html_filepos82111)

[VIIIg Answer: Part a](#index_split_043.html_filepos82668)

[VIIIh Question: Part b](#index_split_044.html_filepos83671)

[VIIIj Answer: Part b](#index_split_045.html_filepos84381)

[IX. Multitasking Example with Promises](#index_split_046.html_filepos85813)

[IXa Question](#index_split_047.html_filepos87104)

[IXb Answer](#index_split_048.html_filepos87560)

[X. Making Promises](#index_split_049.html_filepos91680)

[Xa Reading a File](#index_split_050.html_filepos96367)

[Xb Reading with a promise.](#index_split_051.html_filepos97898)

[Xc Ajax](#index_split_052.html_filepos100609)

[Xd An ajax request](#index_split_053.html_filepos100855)

[Xe Question](#index_split_054.html_filepos102394)

[Xf Answer](#index_split_055.html_filepos103793)

[XI. Implementing hesitating](#index_split_056.html_filepos106371)

[XIa Question](#index_split_057.html_filepos107317)

[XIb Answer](#index_split_058.html_filepos109656)

[XII. More on Object Orientation in Javascript](#index_split_059.html_filepos111516)

[XIIa An archetype](#index_split_060.html_filepos113199)

[XIIb Archetypal construction](#index_split_061.html_filepos117425)

[XIIc Pseudo-class construction](#index_split_062.html_filepos119149)

[XIId Pseudo-class construction, common variation](#index_split_063.html_filepos121964)

[XIIe Archetypal, chaining setter style](#index_split_064.html_filepos124030)

[XIIf Pseudo-class, chaining setter style](#index_split_065.html_filepos127054)

[XIIg Question](#index_split_066.html_filepos129206)

[XIIh Answer](#index_split_067.html_filepos130259)

[About the Author](#index_split_068.html_filepos130845)
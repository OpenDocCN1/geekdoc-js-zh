![](images/00084.jpeg)

**JavaScript Objects**

**Functions and Arrays**

***Explained***

Tony de Araujo  Technical Writer/Instructor

New Jersey, USA

Last update: June 2014

Minor update: January 2015

copyright © Tony de Araujo

All Rights Reserved

Last update: *June 2014*

Download Amazon’s free Reading App
for your computer: **[Kindle Reading Apps](http://www.amazon.com/gp/feature.html?ie=UTF8&docId=1000493771)**. 

Author’s profile at  [Amazon](http://www.amazon.com/Tony-de-Araujo/e/B00D7V08WY/)

"***Excellence is not a skill. It is an attitude.***"

-- Soren Kierkegaard

To all the teachers, authors and fellow students I’ve learned from, my gratitude.

To my family and friends around the world,

a *Big* thanks!

# Table of Contents

[Table of Contents](#part0000_split_003.html__Toc409877802)

[Preface](#part0000_split_004.html__Toc409877803)

[A note from the author](#part0000_split_005.html__Toc409877804)

[About the Second Edition](#part0000_split_006.html__Toc409877805)

[Color Representation in This Book](#part0000_split_007.html__Toc409877806)

[PART I : AT THE GATES OF ENLIGHTENMENT](#part0000_split_008.html__Toc409877807)

[1.1 Prototypical versus Class-based](#part0000_split_009.html__Toc409877808)

[1.2 The Memory Concept](#part0000_split_010.html__Toc409877809)

[1.3 Variables vs. Reference Types](#part0000_split_012.html__Toc409877810)

[1.4 Everything comes from objects](#part0000_split_015.html__Toc409877811)

[1.4.1 Lab 1](#part0000_split_015.html__Toc409877812)

[1.4.2 Lab 2](#part0000_split_016.html__Toc409877813)

[1.5 More Variables, add Functions.](#part0000_split_018.html__Toc409877814)

[What happens when we assign a function to a variable?](#part0000_split_018.html__Toc409877815)

[1.5.1 Lab Work 3](#part0000_split_019.html__Toc409877816)

[1.6 Named Functions vs. Anonymous Functions](#part0000_split_020.html__Toc409877817)

[1.7 First Review](#part0000_split_021.html__Toc409877818)

[1.8 The Untouchable Object](#part0000_split_022.html__Toc409877819)

[Do you remember where an object resides?](#part0000_split_022.html__Toc409877820)

[How do we access the object?](#part0000_split_022.html__Toc409877821)

[What happens to the object when we remove the variable?](#part0000_split_022.html__Toc409877822)

[Can we directly touch and modify the object itself?](#part0000_split_022.html__Toc409877823)

[1.8.2 Native objects](#part0000_split_023.html__Toc409877824)

[1.8.3 Hosted Objects](#part0000_split_024.html__Toc409877825)

[1.8.4 What is a property?](#part0000_split_025.html__Toc409877826)

[1.8.5 What is a variable?](#part0000_split_026.html__Toc409877827)

[1.8.6 What is an execution context?](#part0000_split_027.html__Toc409877828)

[1.9 Second Review](#part0000_split_028.html__Toc409877829)

[1.10 The Window Object – Intro](#part0000_split_029.html__Toc409877830)

[1.10.2 An example of scope](#part0000_split_031.html__Toc409877831)

[1.11 More Primitive and Reference Values](#part0000_split_032.html__Toc409877832)

[1.11.2 How to pass in data from the stack to the heap](#part0000_split_033.html__Toc409877833)

[PART II – KNOW THY TOOLS](#part0000_split_035.html__Toc409877834)

[2.1 Strings as Objects in JavaScript](#part0000_split_036.html__Toc409877835)

[2.1.2 charAt( pos ) and charCodeAt( pos )](#part0000_split_039.html__Toc409877836)

[2.1.3 fromCharCode( )](#part0000_split_040.html__Toc409877837)

[2.1.4 concat( )](#part0000_split_041.html__Toc409877838)

[2.1.5 indexOf() and lastIndexOf( )](#part0000_split_042.html__Toc409877839)

[2.1.6 match( )](#part0000_split_043.html__Toc409877840)

[2.1.7 replace( )](#part0000_split_044.html__Toc409877841)

[2.1.8 search( )](#part0000_split_045.html__Toc409877842)

[2.1.9 slice( )](#part0000_split_046.html__Toc409877843)

[2.1.10 split( )](#part0000_split_047.html__Toc409877844)

[2.1.11 substr( )](#part0000_split_048.html__Toc409877845)

[2.1.12 substr( ) vs substring( )](#part0000_split_049.html__Toc409877846)

[2.1.13 toLowerCase() and toUpperCase()](#part0000_split_050.html__Toc409877847)

[2.1.14 trim( )](#part0000_split_051.html__Toc409877848)

[2.1.15 valueOf( )](#part0000_split_052.html__Toc409877849)

[Summary: String Object methods](#part0000_split_053.html__Toc409877850)

[2.2 The Array Object in JavaScript](#part0000_split_054.html__Toc409877851)

[2.2.1 concat()](#part0000_split_057.html__Toc409877852)

[2.2.2 join( )](#part0000_split_058.html__Toc409877853)

[2.2.3 reverse( )](#part0000_split_059.html__Toc409877854)

[2.2.4 sort( )](#part0000_split_060.html__Toc409877855)

[2.2.5 pop( ) and push( )](#part0000_split_061.html__Toc409877856)

[2.2.6 shift() and unshift()](#part0000_split_062.html__Toc409877857)

[2.2.7 slice( )](#part0000_split_063.html__Toc409877858)

[2.2.8 splice( )](#part0000_split_064.html__Toc409877859)

[2.3 New JavaScript Array Iteration Methods](#part0000_split_065.html__Toc409877860)

[2.3.1 forEach()](#part0000_split_065.html__Toc409877861)

[2.3.2 map( )](#part0000_split_067.html__Toc409877862)

[2.3.3 every( )](#part0000_split_068.html__Toc409877863)

[2.3.4 some( )](#part0000_split_069.html__Toc409877864)

[2.3.5 filter( )](#part0000_split_070.html__Toc409877865)

[2.4 New JavaScript Array Reduction and Location Methods](#part0000_split_071.html__Toc409877866)

[2.4.1 What is Reduction](#part0000_split_071.html__Toc409877867)

[2.4.2 reduce( )](#part0000_split_072.html__Toc409877868)

[2.4.3 reduceRight( )](#part0000_split_073.html__Toc409877869)

[2.4.4 Location Methods](#part0000_split_074.html__Toc409877870)

[2.4.5 indexOf( ) versus lastIndexOf( )](#part0000_split_075.html__Toc409877871)

[PART III – ENTERING THE SECOND REALM](#part0000_split_078.html__Toc409877872)

[3.1 JavaScript Functions and Arguments as Objects](#part0000_split_079.html__Toc409877873)

[3.1.1 arguments](#part0000_split_080.html__Toc409877874)

[3.1.2 Nested Functions](#part0000_split_081.html__Toc409877875)

[3.1.3 A Gentle Introduction to Closures](#part0000_split_082.html__Toc409877876)

[3.1.4 The closure principal](#part0000_split_083.html__Toc409877877)

[3.1.5 Lexical Scope](#part0000_split_084.html__Toc409877878)

[3.1.6 The arguments object versus inner functions](#part0000_split_085.html__Toc409877879)

[3.1.7 The “this” variable](#part0000_split_086.html__Toc409877880)

[3.1.8 Functions as Object Constructors](#part0000_split_087.html__Toc409877881)

[3.2 Function Properties and Methods](#part0000_split_088.html__Toc409877882)

[3.2.1 apply( ) and call( )](#part0000_split_088.html__Toc409877883)

[3.2.2 Adding more arguments to call( ) and apply(  )](#part0000_split_089.html__Toc409877884)

[3.2.3 More practice with call( ), apply( ) methods.](#part0000_split_090.html__Toc409877885)

[PART IV – STRENGTHENING THE WARRIOR’S ARSENAL](#part0000_split_092.html__Toc409877886)

[4.1 The Math Object](#part0000_split_093.html__Toc409877887)

[4.1.1 Math.random( ), floor( ), ceil( ), round( )](#part0000_split_094.html__Toc409877888)

[4.1.2 Math.max( ) and Math.min( )](#part0000_split_095.html__Toc409877889)

[4.1.3 Math constants, PI](#part0000_split_097.html__Toc409877890)

[4.1.4 Useful Math Object references](#part0000_split_098.html__Toc409877891)

[4.2 The Date Object](#part0000_split_099.html__Toc409877892)

[4.2.1 Creating a working Date object instance](#part0000_split_100.html__Toc409877893)

[4.2.2 Converting Date to a string](#part0000_split_101.html__Toc409877894)

[4.2.3 Useful JavaScript date libraries](#part0000_split_102.html__Toc409877895)

[PART V – DEFEATING THE DRAGON](#part0000_split_103.html__Toc409877896)

[5.1 Unordered Lists as Objects](#part0000_split_104.html__Toc409877897)

[5.1.2 Accessor methods](#part0000_split_106.html__Toc409877898)

[5.1.3 Mutation methods](#part0000_split_107.html__Toc409877899)

[5.1.4 Practice and review: Create a Loan Application Object](#part0000_split_108.html__Toc409877900)

[5.1.5 How to automatically evaluate and call a method](#part0000_split_109.html__Toc409877901)

[5.1.6 Prototyping new methods](#part0000_split_110.html__Toc409877902)

[5.1.7 Objects that inherit from other objects](#part0000_split_111.html__Toc409877903)

[5.1.8 How to include prototype methods inside a constructor](#part0000_split_112.html__Toc409877904)

[Conclusion](#part0000_split_113.html__Toc409877905)

[APPENDIX](#part0000_split_115.html__Toc409877906)

[Other eBooks from the author](#part0000_split_116.html__Toc409877907)

[Resources](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)

[Errata and Contact](#part0000_split_117.html__Toc409877909)

[Copyright](#part0000_split_118.html__Toc409877910)

[Gentle Rain](#part0000_split_119.html__Toc409877911)

# 
Preface

Even when literature about JavaScript Objects is abundant and already accessible to the reader, this book still fills a need. **JavaScript Objects Functions and Arrays Explained** challenges the void between books for teaching syntax and those covering specific implementations of the language. This comprehensive approach revisits the foundation of JavaScript Objects without asking anyone to memorize constructs that are seldom used in the real world of JavaScript implementation. It dissects objects from the simplest form to a more complex paradigm. It uses simple illustrations allowing the reader to stay focused on the subject matter. Although most book sales happen in the US, this book has also been written in international English and any idiomatic expression has a link to a suitable explanation.

**JavaScript Objects Functions and Arrays Explained** is about concepts; it is not about implementation of exotic scripts that may lose students before they have a chance to grasp the idea behind the topic.  Because JavaScript is such a complex language, the author has chosen to simplify, but not to diminish, certain areas that may be new to a great number of readers. One example is **closures**. The author approaches closures in a minimalistic yet effective way, with illustrations and simplified scripts in order to keep the concept from being lost by the power of the code itself.

The author’s intent is to approach JavaScript in a manner he hoped to find when first initiated his studies of the language. This book is not for the very beginner because it does not cover basic rules of syntax. However, *if you have been exposed to the basics* somewhere else before, you will not have any problem grasping the written material. On the other hand if you come from a different language or need a refresher, **there is always an explanation of the scripts presented,** line by line.

For the early beginner or if you need a review, please refer to the following eBook before attempting to read this one:
[JavaScript in Plain Language – A Self-Study Method, JSON and AngularJS Prep](http://www.amazon.com/JavaScript-Plain-Language-Self-Study-AngularJS-ebook/dp/B00NQERIEI).

Each topic has been kept short on purpose; yet, packed with information normally missed in introductory books or even in many of the more advanced writings. The author assumes that anyone adventuring into JavaScript has the capacity to learn, if given a change to do so.

The book has not just been written for *newer* developers. It is also intended for those already involved with JavaScript but lacking time to search for detailed explanations of why JavaScript works the way it does. This book is the result of many hundreds of hours of research and lab testing by the author, and intends to give every reader *something* worth taking.

**JavaScript Objects Functions and Arrays Explained** will give you the foundation needed to move into more complex books: It will open many doors of understanding without insulting anyone’s intelligence.

**Welcome to the second edition of JavaScript Objects Functions and Arrays Explained.**

## A note from the author

Dear reader,

Thank you for choosing to read *JavaScript Objects Functions and Arrays Explained*. With so many great books out there, it is a real honor and a humble experience to feel welcome into your inner world and I will work hard in this writing to make it worth your while.

This book is a *hands-on* approach. Theory and lab will come together, to bring concepts to a full understanding. You may decide to do a quick reading of the material or just use it as a reference. However, the book can also be ***executed***. I suggest taking the last approach first and later return to read at random.

Aside from one-line scripts, all other sample code will have a link to a *raw file*, giving you a choice of copy and paste into the console, or of coding it from scratch.

The book explains the *newly available* JavaScript native objects, as well as how to create your own. I have spent many days meditating on each topic, paragraph by paragraph, to find the best way to approach each one of them in an effort to convey that information more effectively. As much as I enjoy writing, my love for teaching is deeper.

Native objects are the most used objects in JavaScript because they are faster and well recognized by modern browsers. Yet, several authors choose to teach object *construction* right from the beginning, confusing readers with terminology and concepts the student may never see again in real life. I guess this approach mimics the way other languages are taught. But JavaScript is not any other language. JavaScript is a combination of ECMAScript, plus the ***host environment***. Its mutant characteristic makes it behaves differently each time, depending where and how it is going to be used.

In this book, concepts will come in *layers* and nothing will need to be memorized. When I first started my research for the book, I was caught in awe by the complexity of JavaScript Objects. Complexity in the sense that JavaScript is not like any other language; it resides apart in its own world. The legend goes that [Brendan Eich](http://en.wikipedia.org/wiki/Brendan_Eich), the inventor of JavaScript, wanted to do a Scheme-like (Lisp dialect) language for Netscape, but a reality check intervened, forcing him to compromise with a C/Java syntax, which was familiar to a plethora of programmers already on the field.  In the ECMAScript 5 official publication, one can read the following: “*Some of the facilities of ECMAScript are similar to those used in other programming languages; in particular Java™, Self, and Scheme*”

Today, many developers hate the language for what it is not; but once they get to know it, they love the language for what it is. I certainly love the language as it positively surprises me almost every day!

Thank you for this opportunity,

*Tony de Araujo*

Technical writer – New Jersey, 2013

## About the Second Edition

The Second Edition of this eBook was published in early ***June, 2014***. In reality this eBook has been updated on a regular basis, almost monthly. The reason to publish it as a Second Edition is because the Index has been subdivided into five parts instead of only the prior two. The titles and subtitles of each topic remain basically the same but this subdivision makes it easier to determine which topics to review the second time around.

Some illustrations have been improved and a few misspells have been corrected.

Hyperlinks have been checked for validity. Also exercise URLs have been written explicitly for a possible printout of the eBook.

Other than that, the author has asserted the material as current and relevant to his goals for the book.

## Color Representation in This Book

· **ORANGE**  - New term or element: *make a mental note of it*.

· **BROWN**  -  Previously introduced element

· **GREEN**   - New *action* to take: *Focus on the action*.

· **BLUE**  - Blue represents an external link for further reading.

· **BLUE  -** Some *side notes* are also written in blue to call attention.

Images of code scripts will have links to an actual script. They will be listed as raw files.

In this book the author uses the JavaScript Console from Google Chrome, as well as *Opera* and *Epic*.  

At the browser we can access the console by clicking on

*   **CTRL+SHIFT+j**  for Windows
*   or **CMD+OPT+j** for Mac.  

When you open it for the first time, **undock the console** by clicking on the square button on the lower left. Here’s a [link](https://developers.google.com/chrome-developer-tools/docs/shortcuts) to a list of shortcuts for the Chrome Developer Toolset. Google Chrome can be downloaded from [source](https://www.google.com/intl/en/chrome/browser/). As an alternative both [Opera](http://www.opera.com/) and [Epic](https://www.epicbrowser.com/) work the same. Please feel free to use your favorite browser as long as you know how to access its JavaScript console.

If you need an editor online to use as a scratchpad you can use [EditPad](http://www.editpad.org/), or many other alternatives. **Update:** [jsbeautifier.org](http://jsbeautifier.org/) can also be used as an editor with the advantage of beautifying your code before you copy it. I’ve been using it daily to correct the layout of scripts submitted by my students.

There is no need to memorize anything in the book.

Please follow instructions for the exercises discussed on each chapter. Repetition of the examples is the key to master the subject at hand.

Each topic is *short* and right to the point. Many subjects will be repeated as needed with further explanation the second time around. ***The onion is peeled in layers***.

For your convenience there will also be external link references. The links to Standard ECMA-262 point directly to the topic being discussed. Sometimes the link takes us to the main page instead of the correct topic. This is due to some erratic behavior at the ECMA site. Usually if you click a second time it then goes directly into the correct location.

“*Empty your cup, start at the beginning*”
like every black belt martial artist does each day.

# PART I : AT THE GATES OF ENLIGHTENMENT

Awareness empowers

## 1.1 Prototypical versus Class-based

Because JavaScript is all about *creating* and *destroying* objects, understanding the nature of a JavaScript object is the most important step for mastering JavaScript.

Let’s revisit JavaScript by entering through the back door, albeit the least most common path.

JavaScript is a **prototype-based** object oriented language. It is not a class-based object language.

Both prototype-based and class-based languages have one purpose in common: to share code and avoid redundancy.

In a class-based language, the programmer creates a blue-print (the class) and then objects are built based on such *schematic*.

In a prototype-based language, the programmer creates an object and allows it to become a prototype for the creation of other objects. Like in a class paradigm, this technique avoids repeating code and it saves memory. From here on, all the theory about classes starts fading away. In addition, since objects are allowed to be linked together in a hierarchically manner, the code can be reused forming a **prototypical chain**. When an object needs a tool (a method), it goes up the chain until it grabs one from one of its ancestors (parent or grandparent).

This classless model of language, also known as *instance-based* or **prototype-oriented programming** works with a process called *delegation*, or one object relying upon another to provide a specified set of functionality. It works because JavaScript relies on its real-time environment to make its magic. Like water in a river, it is never the same the second time around.

Just because JavaScript can simulate many of the popular class features by using prototypes, it doesn’t mean it is a class based language. Someone once said that *familiarity takes off the edge of admiration*. Let’s admire JavaScript for what it is and not by what it looks like.

Is there any advantage in prototypical code versus a class-based languages?

Throughout the book, you will find useful reference links for further reading. Here is our first link from [Wikipedia](http://en.wikipedia.org/wiki/Prototype-based_programming). In the middle of the page, you will find a topic titled “Criticism” that may lead you in the right direction to get an answer to this question.

## 1.2 The Memory Concept

Memory management or the act of *managing computer memory* is defined as a way to dynamically allocate portions of memory to a *program* **at** its request. It is also the act of freeing memory for reuse when data is no longer needed (a task **done by browsers**).

A *thread* of execution **is** the smallest sequence of programmed instructions that can be managed independently. Multiple threads can coexist within the same process and share the same memory area.

In general terms, we can **subdivide memory** into two distinct areas, the **stack** and the **heap**.

A **stack** is a **restricted** data structure. Only a small number of operations can be performed in it. Usually this data points to bigger data on the *heap*. Like for example, variables pointing to objects.

When these operations are done, the data is **automatically cleared** to give space for the next batch. In a way the stack acts as ***scratchpad*** for memory operations, and for the most part, only *quick data* such as **pointers** (variable names) reside in the **stack**.

The ***heap*** is a completely different mater. To start with, in the heap, data is not as well organized as in the stack, and chunks of data can be stored [ad-hoc](http://en.wikipedia.org/wiki/Ad_hoc) because in the heap, if a piece of data gets larger, memory can be allocated as needed. This makes the heap slower than the stack. Stack memory is faster because in the stack, each data set has a specific size under strict management.

![](images/00001.jpeg)

Figure 1 A picture is worth a gazillion words

In **JavaScript**, **primitive type values** are stored in the **stack** and **reference type values** are stored in the **heap**. Remember “**reference type**”, we will be talking a lot about it.

In general terms, a reference is something being referred by something else and without the referrer, there is no reference. In the picture above, when you cancel the link from **y** at the *stack* to the object in the *heap*, the object vanishes as we will see later in more detail.

Do not try to *memorize* all this information. Just read it and **understand it**, as we will be mentioning it repeatedly with incremental detail in the process of pealing the JavaScript *onion*.

In JavaScript **primitive type values** are defined as **Number**, **Boolean**, **String**, **Null** and **Undefined**. Since these are *simple values*, in JavaScript they are stored directly in the location taken by the **variable** itself (the stack): they are one and the same. For other types of data, **variables are nothing but *labels*** or *symbols* that point to the bigger stuff at the *heap*.

**Reference type values** are that “*bigger stuff values at the heap*” mentioned in the prior paragraph. They have their *variable name* stored in the *stack* (acting as a **pointer** to the real data at the heap).

Speaking of *Primitives*, the **Undefined** type is assigned to any *declared* variable that does not yet have a specific value. An undefined variable has no **length property** because it has exactly *one* value (called *undefined*) so a length property would have been useless and one more thing hanging on the memory vine.

The **Null** on the other hand is usually a *placeholder* for an *object* and the reason why it is considered a primitive in JavaScript is due to an error made earlier by the ECMAScript Standard. It remains a primitive due to historical reasons. It also has exactly *one* value, *null*. On the previous image one could say that the variable ***y*** has a value of null. Variables with value of *null* are eventually erased from memory (more about this later).

The **Boolean** type represents a logical entity having *two* values, called *true* and *false*.

The **String** Primitive type is a strange one! Normally in other languages Strings are considered a **Reference type** but in JavaScript the string is a **Primitive** type.

As we know Strings can vary in size so in JavaScript, when you add words to a string, the current string is replaced by another string containing the newly added data. Since the variable and its data is one in the same when it comes to primitive values, the whole variable is replaced when we modify the string. This replacement happens because of the memory size necessary to accommodate the new data. The replacement happens in the background and we never notice the difference.

A string value can store 0 or more characters and each character is represented by a 16-bit positive integer. The first position is numbered zero. Therefore, in a string “Tony”, the *position* of the *last character* **is** the length of “Tony” **minus 1** since it starts at zero. When a string contains actual textual data, each element is considered a single UTF-16 [code unit](http://en.wikipedia.org/wiki/Code_point).

*In short*, (this will be demonstrated later) JavaScript strings are actually stored in the stack because they are primitives. If the string expands, **a new string replaces the old string** and the old *data* is discarded.

## 1.3 Variables vs. Reference Types

I’m aware we didn’t introduce the **Number** primitive type yet. Numbers will be covered in more detail as we go along. Basically, primitive types are types provided by the system. The Number type, along with text (String type) and Booleans are *the primitives* in JavaScript.

**Numbers, Strings, Booleans  =>** JavaScript primitives.

As for reference types, here we are talking about *object definitions*. Other languages use classes. Classes are not used in the [ECMAScript](https://en.wikipedia.org/wiki/ECMAScript) Standard (reads é*kma* script). ECMAScript is the name of the scripting language standardized in ECMA-262\. JavaScript is the combination of this standard plus the *environment* where it is used (such as the **browser**).

In **JavaScrip**t there is an object we could call the **Global Object**. This is the prototype (the **template**) for which every other object created will *inherit* **standard properties**.

The Global Object is [mutant](http://en.wikipedia.org/wiki/Mutant): it actually takes a different life depending where we use ECMAScript . When ECMAScript mixes in with a computer browser, the *Global Object* becomes the *Window Object* and that’s how we address it (discussed later).

So if we declare *tony* as an **O**bject (capital O):

**var tony = new  Object();**

We are giving the variable *tony* **predefined tools to use**. I mean, *tony* **inherits a standard number of properties and methods** from the **JavaScript internal library**, tools which are included with the *built in* Object "prototype".

So what exactly is this new object (tony) inheriting from the Object standard template?

**1. Object Properties:**

Once *declared as* an object, our new object *tony* “*inherits by pointing to*” **properties** such as:

(No need to memorize. We will cover this subject naturally along the way. Just understand it.)

A) **Constructor** – A “formula” for creating similar **future** objects via the **new** operator. A constructor is a reference to a function. If you need to create instances of an object, a constructor can be used as a script which serves as an interface with rules of **what can** and cannot **be allowed** on the new object to be. This simplifies conception and it saves memory because all objects can feed from its source (the present source), and we only have to code this source once, independently of how many object instances there are. An **inherited** constructor is a **pointer to source**, and it is not necessary for the functionality of the object already constructed. It serves only to give to a *future* object, the right to be born and exist via the constructor *umbilical* cord. A constructor takes advantage of the *hidden* parameter called **this**, a generic ***placeholder*** that will represent the object being processed. In the English language we use the pronoun “whose”. As in whose, in JavaScript and other languages we use **this** to create a similar result. “This” meaning “this instance of the last object in scope”, or the object we mean to represent here and now. More about “this” later.

B) **Prototype** – Another inherited property is Prototype which is a built-in interface. Prototype acts as an **umbilical cord** or pipeline for an object to inherit properties and methods from a parent object. ‘Protos” or parent, is the source from which the current object inherits properties/methods from another object somewhere above in the chain. The usefulness of this link goes beyond the current object itself as other objects of a lower hierarchy may also inherit traits from their grandparent. Like the constructor, the prototype link is used only in retrieval. It has no effect on updating prototypes. This means that any change in the current object does not change its prototype or parent source. We can also think of prototype as a list of all methods the object is authorized to use. Every new instance of the object inherits this list. We will do some lab work on prototypes later.

**![](images/00002.jpeg)**

Figure 2

Don’t think of JavaScript in terms of *inheriting* properties and methods. Think of it in terms of **interfaces**. Some objects have methods. These methods can be interfaced with other objects down the pipeline and the other objects can used them to create their own functionality which may or may not be similar to the parent object.

**2- Object Methods:**

As for **inherited methods***,* (our example object *tony*) inherits “*by pointing to*” ***methods*** from its parent object, the “Object” object*,* such as:

(No need to memorize. We will cover this subject naturally along the way. Just understand it.)

**a) hasOwnProperty**– (look at hasOwnProperty as a question where JavaScript provides a result as an answer). This method does *not* check *up* or *down* the chain of inheritance. It only verifies if the object in question has created **its own** properties (for example property ‘writer’: does **object_name.hasOwnProperty(‘writer’);** ? returns true **if** it exists **and if** it has been created, not inherited from up the chain.

Does **tony.hasOwnProperty("toString");**? Returns *false* because it belongs to its parent object. **Note:** We will try this on the console soon.

**b) isPrototypeOf**-  The *isPrototypeOf* method allows us to check if an object feeds its *magic* directly from another object. We need to include the term “prototype” in order to use this method. In other words, “**ObjectOne.isPrototypeOf(ObjectTwo)**” will not work because JavaScript does not know what exactly we mean by that command. We need to be more specific and write it this way: **ObjectOne**.**prototype.****isPrototypeOf(ObjectTwo);** ? It returns true if objectOne is **the prototype** of objectTwo. This is the same as saying that *objectTwo* was modeled from *objectOne*. “Modeling from” saves memory because whatever properties objectOne already have, will not be recreated when instantiating objectTwo since they already exist (Note: we will see later that it all depends how we code our scripts).

**c) propertyIsEnumerable** - This method is used to determine whether the specified property in an object, is *visible enough* (listed) to be enumerated in a script such as for...in loop. **It actually lists the object own properties** because own properties can be enumerated, but all inherited properties are not in the *enumerable* list and will not appear on a for...in loop.

**d) toString()** - Every object has a toString() method. It is automatically called when the object is to be represented as a text value like when we alert(object) or console.log it. String conversion happens when a string representation of an object is required.

e) **valueOf()** - JavaScript **returns the primitive value of** the specified object. **myobject.valueOf();** may return an Array, Boolean, Date, Function, Number, Object, String. JavaScript uses this method internally and as needed, but we can also call it on purpose. Objects *Math* and *Error* do not have a built-in valueOf method.

Going back to properties:

Picture this: **A property** of an object can be explained as a **variable**  **attached to** the object. Of course, all these properties and values can be overwritten when we create a new object.

**So, in this example:** var tony = new Object(); **is *tony* the object itself?**

The answer is **No;** *tony* is a **label**, a *symbol*. Technically the symbol *tony* is classified as a **variable** (a pointer) which temporarily resides in the **stack** and **points** to an **object** instantiated (cloned but using existing functionality) from a **template**. This object resides in the **heap** and once we reassign or delete the label *tony*, this objet goes into **garbage collection mode** from where it will be erased (different browsers implement different ways of sweeping unused data. This technique gets improved with each new browser version).

In **JavaScrip**t, ***almost* everything is an object**. All primitive types except **null** and **undefined**, are actually treated as objects by JavaScript, because they get internally *wrapped into* objects, whenever the interpreter needs to implement a method to process the primitive in question.

Because they can be wrapped as objects, properties and methods can be assigned to primitives, showing all the characteristics of an object. This is because **JavaScript** has a prototype **reference** for **Boolean**, **Number** and **String** in its library, which is automatically called in when temporarily needed  to wrap a primitive value:

![](images/00003.jpeg)

Figure 3

## 1.4 Everything comes from objects

## 1.4.1 Lab 1

Time to fire up your favorite *JavaScript Console* and do some lab work. In this project I will use the console from **Google Chrome**. At the browser, you can click on the shortcut **CRTL+SHIFT+j** for Windows, **CMD+OPT+j** for Mac, or follow the steps below:

a) Open Chrome. On the top right, locate the 3-horizontal-lines button, and click.

b) In the *Tools* section, click on *JavaScript Console*.

Now let’s play a bit with**typeof**. Observe each result and try deducting the reasons why it is so.

**typeof** is a JavaScript operator. Its purpose is to  return a string indicating the type of the operand.

Enter the code in green, followed by the **Enter** key. Pay closer **attention to steps 9..15**:

1-    **typeof 1;**

// result is “**number**”. Of course one is a number! Notice how the console automatically finished the *typeof* keyword. Never wrap a number in quotes unless you want to convert it to type string.

2-    **typeof x;**

// result is “**undefined**”. x does not exist as defined.

3-    typeof **tony;** 

// result is “**undefined**”. JavaScript doesn’t mess around!

4-    typeof **"tony"**;

// result is “**string**”. Ah now we are speaking JS lingo! The quotation marks make it a string.

5-    typeof **true;**

// result is “boolean”. *true* is a reserved word. JavaScript is case sensitive.

6-    typeof **"true"**;

// result is “**string**” *Do you see why*? Although *true* is reserved, **“**true**”** does not exist as string.

7-    **var** y = 123;

// (enter) then code: 

8-    **typeof y;** 

// result is “**number**”.

9-    var z = new  Object;

// O is capitalized. Click (enter), then code:

10-  **typeof z;**

// result is “**object**”.

11-  var b **=** z;

// (enter), then code:

12-  typeof b;

// result is “object”. Now both **z** and **b** point to the **same object**. Let’s now reassign **z**:

13-  **z = 123;**

// (enter) Then code:

14-  typeof **z**;

// result is now “**number**”. Z no longer points to the object. It symbolizes the number 123 in the stack.

15-        typeof **b**;

// result is still “object”. Object still exists due to symbol **b** which keeps it alive.

In exercise **9** we declared **z** as a new Object (more about this later). Notice how the o Object is capitalized. All JavaScript native objects start with a capital letter. String and string are not the same symbol. JavaScript is case sensitive. Back to our **z**, z is a variable in the stack that points to an object in the heap, right?

In exercise **11** we declared a variable **b** and assigned it to the same value as **z**. So **b** is now a *label* for a pointer pointing to the same object as **z** (remember our figure 1?).

In **13** we changed our mind and pointed **z** to the number 123\. So now **z** is of type “number’. It’s no longer pointing to the object.

In exercise **15** we realize that **b** remains a true friend of the object and didn’t follow **z**. It still points to the object. This reminds us that when we assign one variable that points to something on the heap to another variable, it is a one shot deal. It says, “*Hey you, I want you to point at the same location I’m pointing at, but stay out of my way!*” If any of the variables gets reassigned to another object, the other variable doesn’t follow it. However if any of the variables **modifies the** current object it points to, the modification is reflected on both variables.

**Note:** The description above only happens when we assign **reference data to variables**. If variable **a** is a string or a is a number, and we assign it to b, like **b = a**, string **a** is **copied** to string **b**. With ***primitives***, each variable and its data is independent of any other variable and its data.

**Question:**

Let’s suppose we reassign variable **b** (now the only link to the object) to something else, like for example *b=345*; Now the *type* of **b** is a ***number*** and the object which **b** was previously pointing to, has no label to address it because no other variable points to it. **What happens to the object located in the heap**?

**Answer:** The object gets flagged for “**garbage collection**” and eventually it will be *erased* from the browser the next time the interpreter sweeps the code.

## 1.4.2 Lab 2

Let’s fire up our favorite JavaScript Console (I’m using Chrome) and code the following:

`1-` `var x = "hat";`  `// Declare one more variable:`

2-    var color = "green";

3-    typeof x;  // result is “**string**”. (Nothing new so far!).

4-    typeof color;  // result is “**string**”. (Same as above).

You know how in JavaScript *almost* everything is an object, right?

Let’s test it!

Try another variable. This time however let’s add a few more properties to it. Notice the semicolon after the curly brace on the next step 1\. We are declaring a variable named shirt. *Variable declarations **always terminate with a semicolon** even if after curly braces*. A semicolon informs JavaScript that the statement is over, nothing more to declare:

1-            var shirt={color: "white", size: "M", material: "cotton"};

2-            typeof shirt;  //results in “object”

**What happened there?** JavaScript is smart and as soon as it saw the **curly braces** it decided that this variable was going to be a bit more complicated than a simple primitive, and placed it in the **heap**, keeping *shirt* in the **stack** as a *pointer* to it.

NOTICE: *because each label (like for example **“color”:**)  is  technically a string, it is also good practice to  write them within  double quotes at the time of declaration. Single quotes will work the same but stick to doubles because once you get into JSon this type of writing will be stricter, so might as well get used to it from the beginning. In the future, I will write them within quotes.*

**Alright, now we’ve got a *real* object, yes?**

Let’s access its data:

3-            shirt.color;  //results in “white”.

4-            shirt.size;  //results in “M”.

5-            shirt.material;  //results in “cotton”.

This variable has **properties** and **methods** *inherited* from the **Object template**. By using **Dot syntax** we can access its values. After all, an object is nothing but a bunch of mapped **key-value** items harnessed together by a *variable* name, pointing to the data.

We could also use **bracket syntax** instead of **dot syntax**. Like this:

6-            shirt["color"];  //results in “white”.

7-            Shirt["material"];  //results in “cotton”.

It all depends on what you are trying to accomplish and also on your preferences of syntax. Bracket syntax is more versatile in the sense that we could apply a numeric *key* if we had one to use, whereas Dot syntax will not accepts numbers. We will see this later in more advanced lab works.

***A*re objects difficult to understand?**

Think of variables as symbols pointing to data; think of *stack* pointing to the *heap*; and of *key-value pairs* in the heap, bound by a pointer in the stack. If no pointer exists, no key-value pairs exist. Just like a coin, one side does not exist without the other. An unassigned variable has a value of **undefined** but still exists. If you really want to get rid of a variable, assign it to **null** after you are done with it. This will clear it from working memory. To check if a variable is assigned or if is not assigned, use **typeof**. We will use **typeof**  later on in the book to verify if methods have been activated in object instantiation in order to avoid method duplication. Don’t memorize anything, just keep practicing and read back if your mind flies away for a bit. Review often.

Think of JavaScript as a collection of objects inheriting functionality from their “parent object” to which they *interface* with.

New objects can also override the original properties and methods and create their own.

These newly created properties can be passed on down the pipeline via the object’s **prototype** property every time we instantiate (reproduce) the object (more about this as we move along).

We can also use the prototype property to assign (adding) new functionality to the existing object, even to the global object **for this particular instance** (since anything added to a the global object is temporary).

Let’s keep going…

8-            var shelf = {"books": 20, "CDs": 57, "Magazines": 19};

9-            shelf.CDs;  // results in 57.

10-          shelf.books;  // results in 20  Now try the following:

11-          shelf.books **=** 21; // added one more.
You could also do it this way: shelf["books"] = 21;

12-          shelf.books;  // results in  21.

We have just added 1 more book to the *shelf* by changing the value of books in the shelf variable.

Let’s test it:

13-           shelf; //results in Object {books: 21, CDs: 57, Magazines: 19}.

We can also *add* (assign) new items to the object:

14-          shelf.audioBooks = 11; *or* shelf["audioBooks"] = 11;

Call the object:

15-                              shelf; // results in:  Object {books: 21, CDs: 57, Magazines: 19, audioBooks**: 11**}

As you see, a *variable* can point to a collection of data in key-value pairs, making the collection an object. However, even regular strings, although primitive values, inherit properties and methods from Object since almost everything is an object.

Look at the following examples:

16-          var x = “tony”;  Then code the following:

17-          typeof x;  //results in “string”.

18-          x.length;  //result 4.  (Where did length come from?)

19-          x.substring(0,3);  //result “ton”.

The **0** parameter represents the **first included** character for the substring and the **3** parameter represents the **first** **excluded** character. We’ll cover more about length and substrings in a later chapter.

**What happened in exercises 18 ... 19?** 

Remember Figure 3? It seems that although JavaScript didn’t move “tony” to the heap converting it into an “official” object, the string still has properties and methods available to work with, due to **object wrapping**. In JavaScript it is then best to just think of objects and nothing but objects. Code makes more sense from this perspective.

## 1.5 More Variables, add Functions.

### What happens when we assign a function to a variable?

## 1.5.1 Lab Work 3

1- Write this function on a simple editor (I’m using *Notepad*) and copy it to the JavaScript Console (you can also copy my file by clicking of the **raw file** link):

![](images/00004.jpeg)

Figure 4 [raw file](http://icontemp.com/joagi/scripts/4.txt). [ icontemp.com/joagi/scripts/4.txt ]

**Notice the semicolon**. This is a **function definition** statement, which means that we are defining the variable addMe100 which points to some unnamed function object on the heap, which in turn adds 100 to any *argument* passed in by the *parameter*. (We haven’t passed in any argument yet). As you know, when we declare a variable we add a semicolon to its end of declaration, hence the semicolon at the end of this function.

Functions are like **black boxes** where groups of code scripts exist to perform a specific task.

Functions are very useful to save code and/or data for later usage. They diminishing *redundancy* by reusing the same code each time it is needed. We delegate the code every time the function is called upon. Sounds familiar? Functions are objects and objects can also be collections of functions. A collection of functions designed to perform a specific assignment for an object is called a method. Sometimes a method has only one function, other times, a method comprises of several function in the same method. When we aggregate functionality that works together to accomplish a specific outcome (behavior), we are creating an object. Yes, objects within objects within objects make up a package known as a program.

The above script is represented in the same manner as when we declare a variable. What I mean by this is that there is no value to the variable itself. **Its purpose is** to point to a function. It works just like any other variable declaration such as **var x;** Browsers will keep it as a reference, but the interpreter will only act when we call the function, such as when we write **addMe100(3);**  (3) being the argument to be passed into the function via the interface *parameter1*. The browser then keeps track of that unique execution of the function.

2- Let’s code this: **addMe100(3);** // results in **103**

3- Code: **typeof addMe100;** // results in “**function**”.

4- **addMe100.length;** // results in **1**.
The property .length in a function returns the number of *official* parameters available in this particular function. These parameters are the interfaces to insert data into the function as arguments.

We pass **data in** (this data is called **arguments** going in, and up to 255 different arguments can be passed) into the function by using the placeholder inside the parenthesis (called **parameter**, and it is actually an object array-lookalike holding a maximum of **up** to 255 parameters.). We pass **data out** from the function using the **return** statement. The return also acts as a **break** and no further code will be processed within the function once the interpreter processes the return. **Return** is the last thing that happens in a function process. The function instance is then destroyed, unless there is another pointer keeping it alive (more about this later).

Functions can be called *externally* (like we just did), or *internally* within their own body (called **recursion**).

In JavaScript **functions are objects** (you know that!). They can be passed around just like any other object does. We could assign several variables to it, or include the function inside of other scripts, etc.

5- In long programs, after we are done with function **addMe100** and we no longer need it, we should **dereference** the variable (pointer) in order to remove it from the browser’s memory, because it is a global variable and it will remain in memory until the end of the program if not dereferenced. Dereferencing means to **remove the reference** by making the variable "**null**“. This will eventually clear both the variable and the function. Here’s how it is done:

Code: **addMe100 = null;**.

(**Note:** After dereferencing *addMe100* to *null*, if you check its *typeof*, you will get an empty *object*. Null is a special object (Remember the historical reason stated on chapter 1?). JavaScript will delete *addMe100* based on how the browser implements *garbage Collection*). Also the function ceases to exist. Try calling the function. You will get an error. addMe100(3); will result in TypeError: object is not a function.

Practical functions implementations will be covered in more detail on later chapters. Let’s move along a keep peeling this current onion.

## 1.6 Named Functions *vs.* Anonymous Functions

Our function **addMe100** from step 1, Lab Work 3, is an **anonymous** function. This means that the function is assigned to a **variable declaration** and it is an **expression** (part of a program) of the *declared* variable.

Let me explain…

In JavaScript we can have **variable declarations** such as this:

**var x;**

We can also have **function declarations**:

**function y( ){ };**

Declarations can have **expressions** such as:

![](images/00005.jpeg)

Figure 5

Also **variables** can have **functions as expressions**:

![](images/00006.jpeg)

Figure 6

When we declare a variable or a function, they are normally **hoisted** (pulled up) to the top of the **scope** by the interpreter, which lists all *variable declarations* on the top. Sort of like an index of what’s available. **Only the declaration is hoisted**, not the expression. This may not make a difference or matter to the program in itself, except when *debugging* code. When we debug, it is nice to visually distinguish between variables and functions from the list. It simplifies our understanding of what’s on the menu, right?

**Here’s the problem:**

In our example**s** above, the following would be figuratively seen on the top of scope:

**x**, **y( )**, **z**

Notice how **y** is shown as a function but **z** looks like a variable of some sort. That’s because **only the declaration name is hoisted** and not the expression. It only means a bit more work when it comes to debugging.

There is another difference between y and z: We could actually call ***y*** before we declare the function script because JavaScript already recognizes ***y*** as a function and it will look for it. However, in ***z***, if we call the function in ***z*** before the function assignment is written, we may have an error.

It is considered a best practice to declare all our functions before we try calling them.

Other than that, **using [anonymous](http://en.wikipedia.org/wiki/Function_literal) functions is perfectly ok and a very powerful technique** if implemented wisely (jQuery makes extensive use of anonymous functions).

## 1.7 First Review

*   JavaScript is a **prototype-based** language.
*   Just like classes, prototyping avoids repeating code which saves memory and simplifies the script.
*   **Memory** is subdivided between ***Stack*** and ***Heap***. Stack acts as a scratch pad for short length data such as primitives and other temporary data. Longer more detailed data such as objects of any kind, are written in the Heap.
*   To access objects we create **pointers** known as variables. Once we dereference a pointer, the object goes into delete schedule via a **Garbage Collection** method. Garbage Collection methods are determined by the browser itself and may vary from browser version to browser version.
*   **Primitive types** reside in the *Stack* and **Reference types** reside in the *Heap*.
*   To **dereference** an object we declare the pointer (variable) as *null*.
*   We can create an object by instantiating it from the object Object (**the Global object**).
*   Once we declare an object, it inherits **properties** and **methods** from the prototype we “cloned” it from, as well as from any parent of this prototype further up the chain.
*   When we declare a variable containing strings as *key-value pairs* the data is saved as an object in the Heap, and the variable name is saved in the stack as a symbol. We can then recall each value by using **Dot syntax** or even **Bracket syntax**. Know both methods.
*   Since everything is an object, functions and arrays are also objects in their own right and they all inherit from the object Object.
*   When we declare variables or functions their names are **hoisted** to the top of the **Scope** so JavaScript knows they exist. Their expressions are not hoisted, they will be evaluated at runtime as the script gets to it, but the *pointer* gets acknowledged at the very top.
*   An **Anonymous** **function** is a function *assigned* to a variable. It acts as an expression of the variable. We terminate the variable assignment with a semicolon.
*   A **Named function** is a *declared* function. It is listed at the top of the scope as a function and not as a simple named variable.
*   When a function calls itself within its own body is called a ***[recursion](http://en.wikipedia.org/wiki/Recursion)***.

## 1.8 The Untouchable Object

### Do you remember where an object resides?

Objects reside in the *heap*. They are reference types.

### How do we access the object?

We access the object by assigning a label to it. This label is known as a variable. The variable points to the object.

### What happens to the object when we remove the variable?

The object is placed automatically in garbage collection to be deleted by the browser.

### Can we directly touch and modify the object itself?

*Big **No**!* We need to use a *pointer* (variable) to handle the object. Through the pointer and other manipulative techniques therefrom, we are able to manipulate or modify the object via interface mechanisms, which depend on properties and methods available to the object.

At this point we already know how a new object inherits certain methods and properties from the big mother object, the JavaScript object template, but we certainly can add new ones or override existing ones. We will have opportunity to practice different techniques in our lab sessions.

In review, **objects** are created by JavaScript when we assign a variable to the object. The variable resides in the stack and points to the location of the object in the heap. Without this *umbilical cord* leading the program to the object, there is no object. If we cut the umbilical cord by *dereferencing* the variable (declaring it null or reassigning it to something else), the object ceases to exist.

But wait! Without a variable pointing to the object there is no object if the object has been created from scratch, or instantiated from another object. What about permanent objects such as **native** objects, **built in** objects or **the Global object** itself?

These objects always exist. They are in standby waiting to be called upon by another variable whenever needed. **The permanent library never goes away**.

**This is an important concept:** JavaScript is **not just** **ECMAScript**. JavaScript is a combination of ECMAScript and the environment where it is being used such as the browser (I’m referring to DOM & BOM). ECMAScript is implemented by a JavaScript Engine. There are several engines being used. A short discussion on engines can be found at [Wikipedia](http://en.wikipedia.org/wiki/JavaScript_engine).

## 1.8.2 Native objects

Native objects are originally implemented by the ECMAScript standard and they are always present no matter where JavaScript is being used at. They help to specify and define other objects. Native objects are also called **Standard Global Objects**.

Some of the standard built in objects are the following:

Array, Boolean, Date, Function, Math, Number, Object, RegEx, String.

A list of Standard Global objects can be seen At the [Mozzila Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects).

Do not confuse the term ***Global* Objects** with ***The* Global** Object (the mother of all objects, the object Object). This particular object is the prototype we have mentioned earlier in 1.3 Variables vs. Reference Types. Actually we **can’t** even refer to it directly since its name varies with each environment where ECMAScript is used at. For example, in the browser it assumes the name **Window**. Window is the very first object, (root of the script) and any global declaration (like for example: **var x;**), are scoped at the *Window level* or at the level of the *Global Object*. We will experiment with this concept on the next lab work.

Some native objects, such as String and Math, allow access to their properties and methods without instantiating a new object. Other native objects, such as *Date*, require you to create a new instance in order to use their properties and methods.

## 1.8.3 Hosted Objects

Other objects are supplied by the **host environment** which interfaces with ECMAScript to complete the whole JavaScript functionality. In the browser, the other objects come from the [DOM](http://en.wikipedia.org/wiki/Document_Object_Model) (the document environment) and the BOM (the browser environment).

**BOM** - Browser Object Model: this is a collection of objects that define the browser window and its contents. By using the BOM, developers can perform actions that do not directly relate to the document content such as *move the window* and *change text in the status bar*. Unfortunately BOM was not standardized until HTML5 and each browser uses its own implementation. With the advent of HTML5 the browser industry is now starting to implement standards and it should get better for every new browser version published.

**DOM** - Document Object Model: this is an **object** which defines the document being displayed in the browser window. Dom has been standardized and it is an object within the Window scope. Window is an internal part of the BOM.

In addition to being used on web browsers and servers, JavaScript interpreters are also embedded in a plethora of software tools. Each of these applications provides its own unique **object model**, which allows the core language to interface with the host environment. JavaScript core (ECMAScript), remaining basically the same in each application. The Global Object takes a different life in each one of these cases, and it serves as the *liaison* between the core language and its host. One example of such implementation is Adobe's Acrobat and Adobe Reader which support JavaScript in PDF files. Other tools using JavaScript are Photoshop, Illustrator and Dreamweaver. Also Flash which implements ECMAScript under the name of ActionScript.

The following image is a very broad view of a browser instance. Each internal object is included on the outer object. BOM being the wrapper of it all. Unfortunately BOM is not a standard but all the other objects have been standardized. Notice how HEAD and BODY are siblings, and children of HTML. In the BODY section, notice how each object shown is a sibling of the others within the BODY. Notice also how ***text*** is actually an object in itself.

![](images/00007.jpeg)

Figure 7 - When we open a new Window, the window belongs to the browser. We are using BOM syntax when we open a new window. The object is the window itself. In window.open("url"); .open is a method from the BOM.

## 1.8.4 What is a property?

Let’s peel the onion a bit more…

A property is an *association* between a name and one of the values of the object in question, which is to say that properties are the building blocks of objects.

## 1.8.5 What is a variable?

A variable is a “property” acting within an **execution context**.

## 1.8.6 What is an execution context?

An execution context is the scope *in which* something is executed. A variable declared inside of a function has a scope of its function or inner functions inside it. However, in execution context terms, each time we call a function the scope of this variable is different than other prior or future function call. That’s an execution context.

When the interpreter first starts, there is only one execution context, the global context. In the Global context we can visualize scope a lot better than afterwards. Then, as each function executes, the context changes, and since JavaScript only does one thing at a time, each time the execution context is unique.

When JavaScript is running in the browser the global context is **window**.  

Everything runs under window (the object Object). Then we can subdivide into functions which are objects that include groups of code environments. A function context runs each time we call the function and it clears out when the program exits the function.

When we declare **var x = "tony";** in the browser environment x becomes a property of the Global Object known in the browser as **window**.

If in the console we type **x;** the result is “tony”

If instead, we type **window.x;** the result is still ‘tony”. “tony” is a value of window and x points to ”tony”.

If however we have a function like for example

![](images/00008.jpeg)

Figure 8

**z** is a property of function **y**, not of **window**. However just for the record, **function y** is a function of the *global object* (window).

We will cover more about scope and context a bit later on. Like a slow-moving tortoise, *slow and steady wins the race*!

## 1.9 Second Review

*   Reference values reside in the Heap.
*   In order to call or modify an object we need to have a variable pointing to it.
*   JavaScript is composed of its core (ECMAScript) *plus* the objects from the environment where it is being implemented.
*   In a browser, the main object is Window. ECMAScript interfaces with the Document Object and the Browser Object Models.
*   The Document Object (DOM) has been standardized. The Browser Object Model continues to be browser brand specific but it is rapidly changing.
*   ECMAScript comes with Native objects, which are always available, such as the Global Object, Array, Boolean, Date, Function, Math, Number, RegEx and String.
*   The running environment (such as a browser) adds its own objects called **Hosted Objects**. In a browser, the Global Object *morphs* *in* to become **Window**. Then we have the Document Object (**DOM**) and all sorts of proprietary objects known as the **BOM** collection.
*   A variable is a given name *declared* under a given scope.
*   A property is a variable **+** the data to which the variable points to.
*   Contrary to some other popular languages, there is no scope protection inside of a JavaScript code block, except if this code block is a function. This will change in EcmaScript 6 with the introduction of “**let**”. In JavaScript, functions protect their variables, but only if predefined with the prefix **var** when they are declared.
*   Although in the global scope the keyword “var” could be omitted because the variable is available down the scope chain, it is good practice to always write it down when we declare a variable in order to prevent confusion and misinterpretation by the JavaScript interpreter. **var binds the variable to its immediate scope**. In the latest ECMAScript 5, the omission of “var” will actually throw an error.

## 1.10 The Window Object – Intro

As mentioned before, the Global Object becomes the Window object, when using JavaScript in a browser environment.

Let’s do a little test to illustrate this concept:

Fire up your JS Console and code the following:

1. **var myText = "hello World!";**

2.  **myText;** // returns “hello World!”
3.  **window.myText;** // returns “hello World!”
4.  **console.log(myText);** // returns hello World!
5.  **window.console.log(myText);** // returns hello World!
6.  **this.myText;** // returns “hello World!” (**this** substitutes (points to) the object under which the variable is *scoped at*. In this case it substitutes **window**). More about it later.
7.  **this.console.log(myText);** // returns hello World!

**What about a function?**

8.  Code the following in your text editor then paste in the console (raw file available):

![](images/00009.jpeg)

Figure 9 [raw file](http://icontemp.com/joagi/scripts/9.txt). [ icontemp.com/joagi/scripts/9.txt ]

9.  **x;** // returns **function(){var text2 = "hello JavaScript";};**
    Remember, x points to an expression which happens to be a function. We are not calling the function here because we didn’t use parentheses as a postfix.
10.  **window.x;** 
    // returns function(){var text2 = "hello JavaScript";};
11.  **text2;** // returns tex2 is **not defined**. (text2 doesn’t exist on the global scope.)
12.  **window.text2;** // returns **undefined**. Same as above. Window recognizes function x, but does not recognize the function’s local variables.

1- Consider the following loop where **i** is used as a temporary counter ([raw file](http://icontemp.com/joagi/scripts/f1.txt)). [ icontemp.com/joagi/scripts/f1.txt ]

**for (var i = 0; i<5; i++){ console.log(i); }**

// returns 0,1,2,3,4

After we run it, we no longer need the variable **i**, right?

2- Call i:

**i;** returns 5 ( that’s no good, it’s keeping up memory unnecessarily).

3- Now try coding the same loop but inside of a function:

See [raw file](http://icontemp.com/joagi/scripts/f2.txt). We used **y** instead of **i** just so that we don’t get confused. [ icontemp.com/joagi/scripts/f2.txt ]

4- Now if we try to call in y, the same as the earlier **i**, we get an error:

y; // returns y is not defined.

The function has effectively isolated and destroyed the temporary variable. We still have **x** to worry about because it points to the function, but **x** is more obvious to us and we could assign it to *null*. In either case, the idea here is to illustrate how functions can isolate variables from the global object (and also to start thinking about possible [memory leaks](http://en.wikipedia.org/wiki/Memory_leak)).

The object window is both: the ECMAScript’s **Global Object**, and also the browser’s **BOM** central object.

Each window represents an **instance of the browser** itself. The object window is the *interface* between the core JavaScript language and the browser. It represents the global scope for every variable and function on the webpage.

We can add properties to the object window at will (although not on a permanent basis).

**Try this:**

13- **window.color = "green";**

Note: This is actually declaring a variable named “color”. It is the same as declaring the variable by itself excluding “window” because window is assumed. However since we are grasping concepts please write window to cement the idea behind it.

14- **window.mood = "happy";**

15- **window.gender = "female";**

16-   **color;**  
// returns “*green”*.

17-   **mood;**  
// returns “*happy”*.

18-   **gender;** 
// returns “*female”*.

19-  **this.color;** // returns green. (etc….)

## 1.10.2 An example of scope

Let’s just make sure we understand about **window scope** (global) and **function scope** (local).

1- Declare a variable, and then a function as follows:

**![](images/00010.jpeg)**

Figure 10 [raw file](http://icontemp.com/joagi/scripts/16.txt). [ icontemp.com/joagi/scripts/16.txt ]

1- Call the function x:
 **x();**

It should return the following: **my car is a Subaru** **"the other car is a Ford"**

**Why did we get both variables outputted?**

Both variables have the same name but they are in different scopes. The first variable car (Ford) is at the **global** scope, or **window** scope. Since we declared another variable with the same name inside of the function, JavaScript will not be able to use the global variable because their names are alike and it always picks the one from the closest environment.

On line 6, we address the conflicted problem by including the complete path to the global variable *car* in order to tell JavaScript which *car* we really mean. Had they been different names we would not have to include the extra object *window* prefix. Using the same name for both variables was done for illustration purposes, but it can actually happen in real life. Either way, we are just trying to understand the concept of scope:

In order to use both variables with similar names, we needed to call the global variable with its **full complete path** meaning the name of its scoped object, which in this case is  **window**, followed by a **dot** and the name of the variable. This syntax assigns the correct target to the variable.

**Here’s a bonus question?** Could we have used the placeholder ***this*** instead of **window**, in other words **this.car**?

2- **Try using "this"** to see what happens. Substitute ***window*** for ***this*** on line 6\. Then call the function (line 9):

 ![](images/00011.jpeg)

Figure 11 [raw file](http://icontemp.com/joagi/scripts/17.txt). [ icontemp.com/joagi/scripts/17.txt ]

**The answer is:** **In JavaScript this always refers to the owner of the function being executed. Who is the owner of this *method* "x"?** The Global Object ***window***.

However, keep in mind that as we instantiate other objects, they will become owners of methods themselves even if they are under the window scope as we will see later. This means that ***this*** will belong to them in that execution environment, and a global variable would not be able to *be called* in this manner. Bottom line: avoid using the same name twice.

**A note about security and the global object:**  (This is a side note about the window object and it has nothing to do with our topic). In a tabbed browser, each tab contains its own window object. The same happens if we have multiple open windows. For security purposes, the window object instance is not shared among multiple windows. This prevents a script from one window peeking into another window when a user has multiple sites open at the same time.

For a brief reference of all of the methods, properties, and events available through the **DOM** window object please refer to this page [docs](https://developer.mozilla.org/en-US/docs/Web/API/Window)  at the **Mozilla Developer Network**. We will be covering most of those methods later in the book.

## 1.11 More Primitive and Reference Values

Now, let’s see if we can directly assign a *property* to a regular *string variable*. Remember how *primitive* *values*, for example strings, are saved in the *stack*, and *reference values* such as objects are saved in the *heap*?

1- Declare a variable: **var x = "ninja";**

2- Add the property color: **x.color = "green";** Console returns “green” (so it must have accepted it, right?) Let’s test it and see:

3- Enter **x.color;** returns “undefined”. **What happened?** It didn’t save it. **In order to save a *property* we should send it to the heap as a reference value**. Let’s do that….

4- Declare another variable but this time assign it to an object by creating the expression at the heap (the braces will do that for you):

**var y = { };**

5- Now try adding a property just like before: **y.color = "green";**

6- Call the property: **y.color;** // console returns “green”. Alright, *we’re in business!!*

7- Call it again with window just for fun:

**window.y.color;** // returns “green”.

**What do you think it happened?**

By pointing a variable to a *reference value*, we can add properties to it. When and if we delete, **dereference** or reassign the variable, the object will automatically be placed on *garbage collection* according to the browser’s implementation, and the memory will be cleared once the object gets deleted.

In summary, we have created an object under the window object. This object inherited all the properties and methods available from window, also known as the Global Object. We will *peel* more of this onion a bit later.

Now let’s consider another important concept:

Our first variable **x** contains a value of “**ninja**”. Let’s assign “ninja” to a second variable:

8- Declare a new variable **z** and assign it to **x:** **var z = x;**

9- Test **z**: **z;** // returns “ninja”

10- Now change **x** to  **samurai**: **x = "samurai";**

11- Test **x**: **x;** // returns “samurai”.

12- Test **z**; **z;** // returns “**ninja**”.

**What do you think it happened?**

If **x** was pointing at an *object* when we assigne **z = x**, we would have told **z** to *point at* the same object. However, **x** is a **string** variable located in the *stack* because it is a **primitive value**. When we assign other variables to existing primitive values we are actually copying the data into the new assignment. We copied **x** into **z**. Then we changed the value of **x** which it didn’t affect the value of **z**, right?

This is called **passing data by value** and it is what happens with primitive values.

Every time we assign a value to another variable it gets copied into the variable itself because in the stack, a variable and its stack data is all **one unit**. As a helper to remember “passing by value”, think of “adding value” when we duplicate (copy) stuff (I know it’s cheesy but it may help).

When it comes to reference values (the ones in the heap), things work a bit differently. That’s why they are called *“reference”* and we will see the difference in a second. This is obviously called **passing data by reference** (by pointing instead of copying).

Let’s do some more testing:

You should still have your **object** **y** in the console (if not, create a new one again by following steps 4 & 5 above).

13- Test y just to be sure: **y;** it should return *Object {color: "green"}*

14- Assign a new variable **b** to ***y***: **var b = y;**

15- Test **b**: **b;** // it should return *Object {color: "green"}*.
Now **y** and **b point to the same object *source***.

16-  Add a new color to **y**:

**y.color2 = "red";**

17- Test **y**:

**y;** //  returns *Object {color: "green", color2: "red"}*

18- Test **b**: **b;**//  returns *Object {color: "green", color2: "red"}*

As seen, reference values don’t get copied when we assign a second variable to them.

Here the variable acts as a *pointer*, and a reference value can have many pointers. If one of the pointers edits the data from the object, the other pointers will reflect the same data from the same object. This saves memory but we also need to be careful because if we want to **dereference** the object in order to clear memory space, we need to make sure that we dereference all the variables pointing to the object.

**What would happen to b, if we reassigned y to a different object?**

Let’s try it:

19- Reassign y: **y = {"color": "violet"}**

20- Test it: **y;** // returns *Object {color: "violet"}*

21- Test b: **b;**  //b remains the same:  *Object {color: "green", color2: "red"}*.

22- Let’s practice **dereferencing** objects  by first, assigning another variable to **b**:

**var c = b;**

23- Test **c;**  // returns *Object {color: "green", color2: "red"}*

24- Dereference **b**: **b = null;**

25- Test **c**: **c;**  // returns *Object {color: "green", color2: "red"}*

26- Dereference **c**: **c = null;**

27- Test **c**: **c;**  // returns null

The object has finally been sent to **Garbage Collection** and it will be disposed of because there is no reference pointing to it from the stack. It will be deleted on the next memory sweep.

## 1.11.2 How to pass in data from the stack to the heap

One way to pass data from the stack to the heap is as an *argument* in a function *call*.

![](images/00012.jpeg)

Figure 12

In JavaScript, *primitive* data from a variable can be passed *into* a function as a copy, via a function ***argument*** which is given to a function ***parameter***.

The parameter acts as the *interface* between stack and heap. In other words, the data in the variable and the data being passed into the function become independent of each other. (**x above is pointing to function, but x(33) is copying into the function**). So even though a function resides in the heap, we are **not** pointing or **passing by reference**, we are actually cloning the data to be processed by the function, which is the same as *passing by value* (remember? *like copying data into another variable, or “adding”value*). If the data as in x(33) changes after the first copy, it will not affect the function data already passed in, it will create a new function call (a new instance of the function with new data).

**Please note:** we are talking about *passing in* data from the ***stack*** to the ***heap***. This data is copied because there is no physical connection.

When it comes to internal data being passed into a function from inside the heap itself, like from another function, object or array, it is done *by reference*, not by copying. When we pass an object or an array as an argument into a function, we are **passing by reference**. They are both in the heap,  function and (objects or arrays). Passing by reference means that any change processed inside of the function will be reflected on the original object/array being passed in. This is because we have actually given permission to the function to point at the object or array and modify it as per the function code.

Looking it from a different perspective, a function parameter accepts a copy of data coming from a primitive on the stack, but it does not accept a copy of data if the data is coming from the heap. Instead, it points to the existing data, the one coming from another function, object or array.

This difference is important because the behavior of data coming from the stack and data coming from within the heap have different outcomes. To *cross the void* from stack to heap, one needs to copy. To travel from within the heap one only needs to point and in this case, *any change by the pointer will change the original data*.

Congratulations on reading and understanding this material.

Let’s move on to part two and peel the onion a bit more.

This mental picture of JavaScript will serve you well.

There is no shame on reviewing if you must, it is actually a good sign.

Black belt is on the horizon…

*Thanks for coming along!*

*Tony de Araujo*

# PART II – KNOW THY TOOLS

===

“For the things we have to learn before we can do them, we learn by doing them"

--- Aristotle, The Nicomachean Ethics

A good word about what you have learned so far is an incentive for the author to keep writing and it  is greatly appreciated.

[Please take the time to do it](http://www.amazon.com/Tony-de-Araujo/e/B00D7V08WY).
Thanks! [ amazon.com/Tony-de-Araujo/e/B00D7V08WY ]

**About Part 2:**

This section covers some new concepts as we go through the JavaScript library methods and object properties. The best way to take advantage of this section is by reading it, understanding it and try out each exercise. If possible, repeat this section several times and create examples of your own.

There is no need to memorize these methods, just make sure you understand them. Later you will return to grab one method or another as you need them in your own projects, or you can just do a web search to find the correct syntax for the method you need to use. However, if you don’t go through this section and do your own tests, you will not know what to look for in the future. Awareness if three quarters of the path to know about something.

Then on **Part 3** we will cover functions in more detail as well as other objects such as ordered and unordered lists (arrays and hashes).

Once you master these two sections you will be well on your way to become a great JavaScript programmer.

# 2.1 Strings as Objects in JavaScript

Up to this point we have been covering strings as primitive values in JavaScript. Strings are **immutable** (fixed values) and they reside in the Stack. If we edit a string, the variable gets replaced by another string variable of a shorter or longer length and with the same name. The previous string gets automatically discarded since no editing is possible.

However there is such thing as a **String object**. The prototype is there, in all its glory, with bells and whistles to be called upon when needed. Actually JavaScript calls the String object at will and wraps strings into objects when it needs to do so.  You want to find out the length of a string variable? JavaScript replies: “No problem sir, madam, I’ve got you covered!”.

All methods and properties of the String object are automatically available to primitive values. There is no need to instantiate an object.

First let’s define two terms in our vocabulary.

The term “**literal**” refers to a character, word, or phrase within quotes like for example “*apples and bananas*”. A string literal is composed of *zero* or more characters enclosed in single or double quotes. Although there is no difference between single or double quotes in JavaScript, double quotes are mandatory in JSon (JavaScript Object Notation) and many developers are picking up double quotes as a standard format.

Also, just to be sure you understand the term **method**, method is what programmers call a piece of functionality that acts on behalf of an object. A method is normally a function, or a collection of functions to accomplish one specific task.

In JavaScript the string literal is normally a primitive type. When a *method* is called on a string literal, the string is temporarily and automatically *wrapped* into an object in order to process the call.

Here’s an example of a string primitive to be used in our subsequent demonstration of properties and methods. Please do the exercises in green as we did during our  previous lab work:

**(fire up your favorite JavaScript Console,** I’m using Chrome**)**.

**var x = "bananas";**

When a string primitive is wrapped around a String object, it automatically inherits several (a) properties, and several (b) methods.

Let’s take a look at some of these properties and methods:

a) **String properties** such as length, prototype, constructor:

1- **length** 

Returns a number based on the length of the string:

**x.length;** // returns *7*

2- **prototype**

The prototype property is used to ***add* properties and methods** to an *existing* object. Let’s add a property to the String object to see if “x” inherits from the object (I’m assuming you still have **x** in your console from the previous exercise) S for string is capitalized:

**String.prototype.feelings = "love bananas";** (notice the capitalized **S** for string).

Since a picture is worth a million words I would remember it like this: “Mr. String, please *prototype* (verb meaning create as prototype) the property “*feelings*” with a value of  “*love bananas*”. (In this case I would also *see*  a property in my mind as a key-value pair as in *x.feelings*).

Think of the *prototype command* as adding something new to a *menu* of tools. We can think of the name of this menu as *prototype*, the verb allowing the addition of new properties and methods  is also the verb  *prototype*.

**Now test it:**  **x.feelings;** // it should return "love bananas".
Remember, you can also write it as x["feelings"];
because *feelings* is the location where the property *value* resides.

The property *feelings* became part of the string **x** and it can be called using **Dot** *or* **Bracket notation**. **x** is still a string *primitive* and you can confirm it by calling **typeof** on it, which returns a lower cased string type, and not an *object*.

When we look at the syntax, we see a property named “**feelings**’ which was prototyped (created) on the ***String object prototype*** (menu). It is now part of a list of properties available to all string primitives during *this* particular *execution context*.

Did I just say that **feelings** is “available to all” other string variables?

The property *feelings* is universal. This means that *x* is inheriting it from the String object, but any other string variable inherits the same property because feelings was added to the global String object, as you can see by looking at the prototype declaration done earlier.

**If we declare another string variable, will this property be also available to it?**

Let’s try it:

Declare the following variable: **var y = "oranges";**

Print out its feelings property: **y.feelings;** // returns “love bananas”

So the answer is **yes**, any other string variable will inherit the newly created property because this property belongs to the mother object, which is the String object. If you go back and look at the prototype declaration you will not see any reference to ***x***, the property was added to the String object prototype.

**What about any other variable from a different type?**

Try this: **var z = 123;**

Then this: **z.feelings;** // it returns ***undefined***.

Of course we already knew that. This property belongs to the **String** object and not to the **Number** object. This new property however is *temporary* and it only applies to **this instance**. When it comes to the Native Objects (built in objects), we can add functionality (properties and methods) to our instance of the program but **we cannot permanently modify the native String object** to use on other programs.

**What about adding a new method to String, via prototype?**

Try this one:

![](images/00013.jpeg)

Figure 13 [raw file](http://icontemp.com/joagi/scripts/18.txt). [ icontemp.com/joagi/scripts/18.txt ]

Now let’s call on it by writing **x.repeat( );** // It returns "**bananasbananas**", ***this*** is a *placeholder* for the object calling it.

Also try **y.repeat();** // returns "**orangesoranges**".

So, adding methods to the String object prototype *menu* and applying them to string primitives is also possible.

We can retrieve the list of our own properties and methods by using a *quick-and-dirty* technique on the variable in question:

**x.__proto__;** (2 underscores each)

returns " String {*feelings*: "love bananas", *repeat*: function} ".

That’s proto and 2 underscores on the left after the dot and 2 underscores on the right.

__proto__ is not a JavaScript standard, hence the term *quick-and-dirty*.

In the new ECMAScript 5, __proto__  will be replaced by the following method, but not all browsers support it at the time of this writing and you may get this error *TypeError: Object.getPrototypeOf called on non-object*:

**Object.getPrototypeOf(x);**

For practice purposes **add a few more properties and methods** to the String object via the prototype property, and call **x** for each one of them. Creative practice is the way to cement concepts.

Don’t forget that **x** is a property of the object **window**. x is a string which inherits String methods but it is also a property of window. We could have coded all our scripts with **dot window** as a prefix, like: **window.x.feelings;** *or* even **window["x"]["feelings"];** which means the following address: location *x* on object *window*, property on location *feelings*.

3- **Constructor**

Every time we create a new string variable, it inherits the "menu" *prototype* where we can find readily available properties and methods  to use, and we can add our own, via the "property" also known as *prototype*.

The third property available to a string primitive via its benefactor String object, is the "constructor" which contains a reference to the ***function* that *constructs*** (creates) **instances** of the String object.

If on one hand the *property prototype* points to a "menu" where prototyped tools exist, on the other hand, the *property constructor* points to a function or method that can potentially build another replica of  the object that is inheriting this property.

The string **constructor** creates **objects** which may also include **properties** and **methods**. This means that we can bypass the act of prototyping such functionality by doing it directly as we create the object.

So, while the **prototype** only creates **properties** and **methods**, the constructor creates objects **with optional properties and methods**. However, for memory efficiency it is best to leave the method creation to the prototype mechanism, because a constructor will *duplicate* everything, instead of referring to already existing method prototypes. We will cover this concept in our lab work later.

These newly constructed objects also inherit properties and methods from their ***native objects type*** + the *Window **Global Object*** itself. Those methods will be covered next.

b) **String native methods** such as: charAt, charCodeAt, concat, fromCharCode, indexOf, lastIndexOf, match, replace, search, slice, split, substr, substring, toLowerCase, toUpperCase, trim, valueOf

## 2.1.2 charAt( pos ) and charCodeAt( pos )

Both of the above methods have to do with accessing a character from a string and **based on the character’s position**. The first returns the character and the later returns the character Unicode itself.

Let’s look at an example of each:

1- Declare a variable x: **var x = "bananas** **";**

2- Call its wrapper String method charAt: **x.charAt(2);** // returns “n” ( it starts from 0, the most left character and it picks the character at position 2, like from 0, 1, 2).

3- The above method does the same as when we call the *character number* with **bracket notation**. Try it out:

**x[2];** // returns “n”.
Bracket notation is newer, from the ECMAscript 5 standard. It may not be recognized on very old browsers.

4- Try the other String method: **x.charCodeAt(2);**  // returns  its Unicode which is 110\.

Unicode code points range from 0 to 1,114,111and the first 128 Unicode code points are a direct match of the ASCII character encoding. For information on Unicode please read it here: [Mozzila](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Values,_variables,_and_literals#Unicode) or  [Wikipedia](http://en.wikipedia.org/wiki/Unicode).

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.4 String.prototype.charAt](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.4).

· [15.5.4.5 String.prototype.charCodeAt](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.5)

## 2.1.3 fromCharCode( )

The method **fromCharCode( )** is the inverse of charCodeAt(). This method is pretty simple. It returns a character based on the Unicode given, as an argument:

**String.fromCharCode(110);**

 // returns a string character ***n***. You can assign the result of these methods to variables.

We can also call in several Unicode numbers:

**String.fromCharCode(110,111,112);** // returns ***nop***.

For more information, please refer to the following ECMASCRIPT 5 page:

· [15.5.3.2 String.fromCharCode](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.3.2).

## 2.1.4 concat( )

The concat() method is sometimes used in place of the “**+**” operator to concatenate (join) different  strings to one another. Here’s an example:

1- Our previously declared variable x: **var x = "bananas";**

2- Declare another variable combining two strings (notice the space on the left): **var w = x.concat(" are good for you!** **");**

3- Call **w**: **w;** // it returns "bananas are good for you! ".

Concatenation does not change the value of the original variable “**x**” unless concatenation is called upon itself like in this case (no need to do it):

 x=x.concat(" are good for you!"); which is the same as using **+=** on itself instead of concat().

4- The method ***concat*** comes handy at times like in this example where several variables are added to compose a new string:

**var h = "Read this: ";
var y = " are good for you!";
h = h.concat(x,y);**  // returns “**Read this: bananas are good for you!**”.

For performance reasons the preferable way to concatenate in JavaScript is using **+** or **+=**  However the **+** is slower than the **+=** as the engine creates a *new temporary string* for every two strings separated by a + and that takes time.

Which method to use? It just depends on what you are trying to accomplish based on the existing surrounding code. To have options is a good thing.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.6 String.prototype.concat](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.6).

## 2.1.5 indexOf() and lastIndexOf( )

This is a very important method .

The String methods **indexOf**  and **lastIndexOf**, return the position of a specified value in a string.

The first method searches *from* the beginning of the string, and the second method starts searching from the last character instead of from the first.

If the character is unique, both methods will return the same value. If we ask for the index of “**n**” in “**bananas**” where multiple “n”s exist, **indexOf** will return position 2 because it finds the first “n” there. However, **lastIndexOf** will return position 4 because it finds its first “n” there (but it also displays its counts from left to right, not from last to first). A position number 5, for example, is the same position for both methods.

Example scripts:

1- If our old **x** is not defined, define it again as **var x = "bananas";** then try the following scripts:

**x.indexOf("n");** // returns 2 as a position number. Notice how the console tries to complete the word for you. This is a very convenient feature.

**x.lastIndexOf("n");** 
// returns 4 as a position number.

2- Let’s try another one:

**var aba = "The quick brown fox jumps over the lazy dog.";**

**aba.indexOf("brown");** // returns 10 which is the position where brown starts, counting from 0.

**When a word or character is not found, both methods return a** **-1**.

This can be very useful. Suppose your decision depends whether a certain word exists or not on the paragraph. We could use a conditional statement such as this:

**if(aba.indexOf("brown") !== -1)**, which means, if the word *brown* exists (or in its current negative logic: not nonexistent), do this, *else* do that. See the following raw file for an example of both conditions: [raw file](http://icontemp.com/joagi/scripts/indexof.txt). [ icontemp.com/joagi/scripts/indexof.txt ]

***Note:*** If your intention for searching is to actually replace a specific word, use replace() discussed further down the page.

Please note how these methods use *[camel case](http://en.wikipedia.org/wiki/CamelCase)* syntax.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [ 15.5.4.7 String.prototype.indexOf](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.7).

· [15.5.4.8 String.prototype.lastIndexOf](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.8).

## 2.1.6 match( )

This method searches a string for a match against a **regular expression** returning all the matches as an Array.

Sample scripts:

**var xyz = "Apples and bananas are delicious";**

**xyz.match(/n/g);** 
// returns ["n  ", "n  ", "n  "]

The symbols / / delimit the expression we are searching for. **g** indicates that this is a *global* search, meaning that we want JavaScript to return all findings, not just the first finding.

More examples:

**xyz.match(/banana/g);** // returns ["banana"]

We could assign a variable to the array being returned . For example, in "Apples and bananas".

**var fruits = xyz.match(/Apples and bananas/g);** // returns ["banana"]

We could also convert the output to ***string*** instead of getting an array:

var fruits = xyz.match(/Apples and bananas/g).toString();

Call fruits:

**fruits;** // returns "Apples and bananas":

Regular Expressions are a subject beyond the scope of the current edition of this writing.

Useful references:

[Mozzila](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) | [RegExr](http://gskinner.com/RegExr/) : an intuitive tool for learning RegEx.

**For more information, please refer to the following ECMASCRIPT 5 page:**

*   [String.prototype.match (regexp)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.10).

## 2.1.7 replace( )

Another search method is the replace() which searches a string for a specific value and returns a *new string* where the value found is replaced by the value indicated on the second parameter. We could also search using regular expressions.

The sample script below uses our previous variable **xyz** to replace delicious for tasty:

**xyz = xyz.replace("delicious","tasty");** 

// returns “Apples and bananas are **tasty**”.

**For more information, please refer to the following ECMASCRIPT 5 page:**

*   [String.prototype.replace (searchValue, replaceValue)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.11).

## 2.1.8 search( )

The **search( )** method returns a negative one **(-1)** if no match is found, or it returns a ***position number*** if a match is found.

1- Create a string variable:

**var xyz = "Apples and bananas are delicious";**

2- Then use search() to look for a word in the string:

**xyz.search("bananas");** // returns 11 (it starts counting from 0, *b* is at position 11 including spaces).

3- Let’s try finding the characters ‘na’:

**xyz.search("na");**  // returns 13 ( from 0, n is at position 13).

4- search() is by default a ***case sensitive*** method:

**xyz.search("A");**  // returns position 0 for **A**pple.

**xyz.search("a");**  // returns position  7 (Apples **a**nd…)

**xyz.search(/a/i);**

 // returns position 0\. Here we used a **regular expression** with flag "i" which stands for **insensitive** (case insensitive). This will give me the first character "a" found, regardless of its *letter case*.

To learn more about regular expressions please navigate to Mozilla’s [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.12 String.prototype.search](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.12).

## 2.1.9 slice( )

The method **slice( )** extracts the text *from* one string and **returns** a *new* string with the extracted text. Changes to the text in the old string do not get affect unless the method is applied to itself. This is the same as taking a slice of cake but the cake stays intact. We must give this copy of sliced cake to another variable in order to reuse it.

This method uses up to  two parameters. The first parameter indicates the zero based **first character to be sliced** *(copied from)*. The second parameter indicates the first character to be excluded from the action of slicing. 

Sample scripts:

1- Declare a variable: **var xpt = "red,blue,white,black";**

2- Extracting the word “**blue**” into another variable:

**var xpt2 = xpt.slice(4,8);**

3- Call **xpt2;** // returns “blue” The first character to be included is on position 4, and the first to be excluded is on position 8, which is the comma.

- **Using negative numbers:**

As an alternative, if we apply an negative number to the second parameter, it changes its meaning: now it means to start *excluding* from the right based on the number of characters indicated. Commas and spaces count as characters.

4- For example: excluding the last color, (black and the *comma* to the left) from our slicing:

**var xpt3 = xpt.slice(0,-6);**

5- Call the variable: **xpt3;** // returns “red, blue, white”.
In other words, it includes all characters from position zero on, except the last 6 from the end. This also means that we could exclude some characters from the extreme left if instead of zero we entered some other number as the left parameter.

- **Using just one parameter:**

When using just one positive parameter, it represents the first character position to be included on the slice which extends all the way to the end.

6- For example:

**var x = xpt.slice(3);** // returns ",blue,white,black", which means that "red" was cutoff.

If the single parameter is negative, it has an opposite effect: it tells JavaScript how many characters to include from the right and exclude all else.

7- Example:

**var x = xpt.slice(-3);** // it returns "ack" from "black". It counted from the right to the left 3 characters and cutoff all the others to the left.

8- One more example. Extract the "e"  from ecmascript:

**"ecmascript".slice(1);** // returns "cmascript".

This is actually useful to remove the first character and replace it with another similar capitalized character, as we will see later in the book when we cover toUpperCase().

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.13 String.prototype.slice](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.13).

## 2.1.10 split( )

The method **split()** is a very useful one so let’s make sure we understand the mechanism behind it. split() converts a string into an array. The opposite of split() is join(). Arrays will be covered on the next topic.

1- As an example we are going to declare a new variable with words separated by a space ( no commas)

**var abc = "green yellow red black";**

Vocabulary: In computer science, a **delimiter** is a symbol (or sequence of characters) marking the beginning or the end, of a *unit of data*. In the following example, 1|2|3, the delimiter is the pipe symbol |. Here, “1, 2, 3, 4” the delimiter is the comma, etc.

The first thing we need to determine when splitting a string is what are we going to use as a *delimiter* in order to separate the *units of data*.

In our case we will use a **blank space** between words as a delimiter. What this means is that the method split( ) will grab everything in between two delimiters , creating an array with the split data.

2- Let’s **split** variable abc into separate words using the white space as a delimiter, and put it on a new variable named abc2:

**var abc2 = abc.split(" ");**

3- Call the variable: **abc2;** // returns ["green", "yellow", "red", "black"].

The white space was eliminated and each word became individualized in a new array.

Remember that the delimiter is not included in the new array. If we want to split **abcdefg** using *"d"* as our delimiter, *"d"* will not be included, and the new array will look like this: [**abc, efg]**. If you want to try it, make sure to include "d" in quotes because it is a string. Example:   *var y = x.split("d");*

The method **split()** can use a **second parameter**. The first is the **delimiter** (what separates on unit from another), the second parameter is a **limiter** of how many units are to be included, or in other words, the *length* of the array.

Let’s try it:

4- Declare a variable: **var abc3 = abc.split(" ",3);**

5- Call **abc3**:

 **abc3;** // returns **["green", "yellow", "red"]**, it left out “**black**”.

6- What is the length of abc3? **abc3.length;** // returns 3

**Note:** When using **split()** we must pass at least one argument which is the delimiter. If we don’t pass the delimiter into the split function, the result will still be an array but the number of items on the array will be one. So in a way, the split() could be used as another way to **convert a string into an array** with the *length* of one, but probably not a very used method for that matter.

Regular Expressions turn split into a very powerful method. Investing some time to learn RegEx is a very rewarding time spent. Here’s another link about the subject: [Wikipedia](http://en.wikipedia.org/wiki/Regular_expression).

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.14 String.prototype.split](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.14).

## 2.1.11 substr( )

The substring method **substr()** is an alternative to the slice() method. While the slice() method takes in a **start** index position and an **end** index position, the substr() method takes in a **start** index position and a number representing the length of items to be extracted.

Do not confuse substr() with substring(). The later has actually replaced by slice(). We will talk about it in a moment.

**When to use slice versus when to use substr?**

Use slice() when you know the position numbers of the first character to be **included** *and* the position of the first character to be **excluded**. Use substr() when you know the **length** in characters of what needs to be extracted. With either method, you need to know the position of the first character to be included.

In substr(), a (4,9) means that the extraction starts at 4 (from zero and counting white space, which means the 5^(th) character) and stops at 12 (inclusive), meaning the 13^(th) character, which corresponds to 4 + 9.

**Sample code (same as the one used for slice):**

1- Declare a variable:

**var xpt = "red, blue, white, black";**

2- Use the same script as the one used earlier for slice so that we can see the difference:

**var xpt2 = xpt.substr(4,9);**  
// starts at 4 from zero, making the space the first character, then it counts 9 to the right, inclusively.

**xpt2;** 
// returns " blue, wh". 

If you remember, the same numbers (4,9) used earlier for slice gave us “blue”. With slice 4/9 meant starts at 4 (0 based) and excludes 9, giving us “blue”. Now, by using substr, (4, 9) means starts at 4 (0 based) and it expands 9 characters to the right, giving us “blue, wh”.

**Note:** In **substr**, the second digit, 9, is the number of characters to extract.  In **slice**, the second digit, 9, represents a *position* number, the first to be excluded.

![](images/00014.jpeg)

Figure 14

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [String.prototype.substr (start, length)](http://www.ecma-international.org/ecma-262/5.1/#sec-B.2.3)

Substr was not published with ecma-262. However it is now on Annex B (link above)

## 2.1.12 substr( ) vs substring( )

This is where things get a bit confusing since the names **substr** and substring look so much alike. In reality they work differently in the sense that **substring has been replaced by slice**.

At one time JavaScript developers wanted to implement negative numbers as the means to count from the end of the string to a certain position. The trouble was to be backwards compatible so they decided to come up with a different method name which was slice() and kept the former name intact, *substring*.

Aside from not accepting negative numbers, substring doesn’t care about the order of parameters, which means that it always assumes the smaller number is first. So when we code (5,4) it means (4,5).The method **slice()** is more strict, the order matters as it will not reverse the order by itself.

**What to do?** Use **slice()**. Be aware of **substring()** when analyzing code previously written.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.15 String.prototype.substring](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.15).

## 2.1.13 toLowerCase() and toUpperCase()

The String method **toLowerCase()** outputs a new string with only lower case characters. “AFRICA” returns as “africa”.

The String method **toUppercase()** outputs a new string with only upper case characters. “apple” returns as “APPLE”.

**Sample code:**

1- Declare and call a  string variable:
 **var txt = "ECMASCRIPT";**

2- Convert to lower case: **txt.toLowerCase();** // returns "ecmascript".

3- Convert to upper case again: **txt.toUpperCase();** // returns "ECMASCRIPT".

4- Here’s one way for capitalizing just the first character using what we have covered so far:

**txt.charAt(0).toUpperCase() + txt.slice(1).toLowerCase();**

// returns "*Ecmascript*".
First character is converted to uppercase. Then we concatenate the string by slicing out the first character at position zero, and down casing the rest of the string. When using just one positive parameter in slice(), the number represents the first character position to be included on the slice which extends all the way to the end.

5- Or instead of using **charAt** we could call the first character using the array bracket notation:

**txt[0].toUpperCase() + txt.slice(1).toLowerCase();** // returns "Ecmascript".

Don’t forget that we can also use CSS to capitalize the first letter of a paragraph:

**p:first-letter {  text-transform:capitalize; }**

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.16 String.prototype.toLowerCase](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.17).

· [15.5.4.18 String.prototype.toUpperCase](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.18).

## 2.1.14 trim( )

The **trim()** method was introduced by ECMAScript 5\. It creates a copy of a string cutting off all leading/trailing spaces. Since the original remains the same, if we are cleaning up the original, we need to assign it to itself.

**Sample code:**

1- Declare a string with multiple leading and trailing spaces:

![](images/00015.jpeg)

Figure 15 [raw file](http://icontemp.com/joagi/scripts/8.txt). [ icontemp.com/joagi/scripts/8.txt ]

2- Call the variable to see how the string looks like: **str1;**  
// it returns test with multiple spaces like the picture above, right?

3- Declare a second variable and assign it to the trimmed version of *str1*:

![](images/00016.jpeg)

Figure 16

4- Call str2 to see how it looks: **str2;** // it returns “test” all trimmed up, right?

5- Call str1 to see how it looks? **str1;** // returns the original string with all the white space.

In order to clean up the original string we need to assign the variable to itself.

6- Like in the following picture:

![](images/00017.jpeg)

Figure 17

7- Now if you call str1 again, it will be all trimmed up with no white space around it.

The method *trim()* may not be recognized by older browsers like *IE8* and below. If this is a problem try using the jQuery version instead.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.5.4.20 String.prototype.trim](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.20).

## 2.1.15 valueOf( )

The String method **valueOf()** converts an object to a primitive. This is usually done automatically so we seldom call it ourselves. We will be using it sometimes throughout the book.

All objects including String, descend from object Object, and all objects inherit properties and methods from the Object.prototype unless they are overridden by the new object. The valueOf() method is inherited from Object but every *built-in object* such as String, overrides it so it can return an appropriate value for its type.

When we call valueOf it returns a value as follows:

In an Array, the array instance; In a Boolean, the Boolean value; In Date, the stored time value in milliseconds since midnight, January 1, 1970 UTC; In a Function, the function itself; In Number, the numeric value; In String, the string value; In Math and Error objects, nothing is returned since there are no valueOf methods; And last but not least, in objects with no primitive values, the object itself as object Object.

The code script is **objectName.valueOf( )**. When we call **valueOf** on a string variable JavaScript wraps it on the String object and gives us its value.

Sample code:

1- Declare a variable: **var ppp = "amazon";**

2- Call valueOf: **ppp.valueOf();** // returns “amazon”.

Recapping this concept, **the valueOf() returns the primitive of an object**. **If there is no primitive, it returns the object reference itself**. Each built-in object type modifies the output to coincide with its type. In case of a String, it returns the string value. This method is usually called automatically by JavaScript behind the scenes when it needs the primitive value of an object. It is not a commonly written code script but there are exceptions.

**valueOf()** is the default method used to extract a single value from an object. Another method would have been **toString()** which is not needed on a String object but it comes handy on other types of objects, a way to display the value itself. As written earlier, In a Boolean Object, the value will be converted to the string **true** or its counterpart, **false**. In some other Object types, the valueOf() result will not have much use and may not be applied as much. We will revisit valueOf in later chapters.

**Need further explanation?**

3- Declare the following variable: **var x = 123;**

4- Call the valueOf x: **x.valueOf();** // returns 123\. It shows the value inside of x.

5- Declare an array: **var y = ["Tony","de","Araujo"];**

6- Get  the  valoueOf y: **y.valueOf();** // returns ["Tony", "de", "Araujo"]

7- The example on step 6 could be replaced by the method *toString()* to have a different visual effect: **y.toString();** // returns "Tony,de,Araujo"

JavaScript does this conversions internally depending on what it needs to use at the moment and what king of object it is working with. Programmers also take advantage of *valueOf()* as you will be able to see in later topics.

**For more information, please refer to the following ECMASCRIPT 5 page:**.

· [15.5.4.3 String.prototype.valueOf](http://www.ecma-international.org/ecma-262/5.1/#sec-15.5.4.3).

## Summary: String Object methods

In ECMAScript, the Object constructor is able to automatically **box all primitive types** as object types when need.

It is like saying that when an Object sees a primitive being used as object, it *boxes* it like this:

**new Object([primitive])**.

Then later, it unboxes it like this:

**[boxedobject].valueOf()** (Remember the discussion about **valueOf( )**? It returns a primitive value when invoked).

We will be using String methods in subsequent topics because these methods are used everywhere. Make sure to return to this chapter if you find yourself a bit lost. I will remind you as we go along.

Learning is nonlinear, the conveyor-belt model of learning is from the 19^(th) century and it has no place in our modern world. We learn by doing, through direct experiences and by dealing with issues as they arise. We learn by making connections between what we already knew and what we are currently learning. Each one of us constructs our own knowledge set. I hope I am being somewhat successful on providing you the tools to build your own experience.

# 2.2 The Array Object in JavaScript

Arrays are *ordered list* objects. The order is what makes this object an array since objects by themselves are typically unordered.

(For unordered lists please see 5.1 Unordered Lists as Objects.)

In JavaScript an [array](http://en.wikipedia.org/wiki/Array) uses an index number pointing to a *pocket* where data may be stored. Contrary to other languages, in JavaScript there is no such thing as an Associative Array where the index is substituted by a string label. If you attempt to assign a label to a data pocket, it makes the data a property of the object, and it is not listed as an array item. If you really want *key-value pairs*, it is best to use the Object construct (*curly braces* which makes it an *unordered list*) instead of the array construct (square brackets). Object constructs will be covered in more detail in a later chapter. A link to that chapter can be found above this paragraph.

Because of the Array rigid order, there are *specific methods* to append data to the beginning, to the end, and also to append in between items.

The array constructor is as follows:

var bcd = new Array("green","red","yellow");

This declares a variable (a pointer) named *bcd* which points to an array object containing three string names. Notice the **new** keyword. Although we could skip “new” when we declare an array object like this, it is recommended to **always** include it if you use this type of construct (I mean the Array() function call). Notice how the first letter of **A**rray is capitalized, just like **O**bject and **S**tring object. In JavaScript, native and built in object names have their first character capitalized. Since JavaScript is case sensitive, all native and built in objects must be called upon exactly as they were created, in other words, with the first letter capitalized.

JavaScript has a shortcut to create arrays, which is the **square bracket notation**.

Instead of this: **var ijk = new Array( );** // creates an empty array.

1- It is more common to do it this way: **var ijk = [ ];** 
// creates an empty array.

Contrary to some other languages, there is no need to declare the *number of items* the array can contain. JavaScript arrays adjust accordingly. When we add new items, just like it does with strings, JavaScript copies de existing data plus the new data into a new array instance and discards the old one, and at the same time, JavaScript tells the variable to point to the latest array instance.

2- After declaring the above array **ijk**, we can add items like this:

**ijk[0] = "red";** 
// first location is always location **0**.

**ijk[1] = "white";**

**ijk[2] = "blue";**

3- Call it like this: **ijk;** // returns ["red", "white", "blue"];.

4- We can also call individual items like this: **ijk[0];** // returns "red".

And just like the String object, the Array object inherits properties and methods from **object Object**.

We will cover some of these properties and methods next.

a) **Array properties** such as **length**, **prototype** and **constructor**.

The **constructor** property has already been explained when we covered String objects. We will explore *constructors* during our lab work when we get to create our own objects at a later chapter.

The **length** property of an array works just like the length of a String object. After all, a string is just a list of ordered characters like an array, right? However, there are reasons to use strings and reasons to use arrays. We can display or print a string, but to print an array we need to iterate over each item. We can also change elements of an array, but to change a character on a string is a bit more complicated. That is why sometimes we need to convert an array into a string, and other times we convert a string into an array. Do you remember when we used **split()** to convert a string into an array? The opposite is accomplished with **join()** which will be covered in this chapter when we come to Array methods.

1- In the string **xyz = "bananas";** **xyz.length;** // returns 7.

2- In our previous array, **ijk.length;** // returns 3 as we have three items on the array, ["red", "white", "blue"].

**Length** comes handy when we need to iterate over an array, like going item by item to accomplish something. The reason for using length is that most of the times we don’t know how many items an array contains. By calling its length directly or indirectly to represent the number of items, we don’t really have to worry about the size of the array. Be aware that when  you need a specific *location* number for an item, you may have to call its **length -1**, since an array starts at a zero location. It all depends on what you are trying to accomplish. An array with 6 items has a length of six but its item locations go from zero to five. There will be examples of these techniques later.

The **prototype** property is a constructor that allows the addition of new properties and methods to the Array **object**. Remember, just like the String prototype, The Array prototype adds new methods and properties to the object Array() itself, not to a single array instance. Up to this point and until we cover the object *Object*, we have been working with **built in objects** and we will continue to do so because built in objects are the most important to know about in JavaScript. Later we will discuss creation of *user* objects as prototypes. When we add a new property or method to the Array object, this addition is not permanent, it only applies to this instance of the Array object and to all the arrays under this executable environment. When the program is over, every customization gets wiped out.

Time for some action.

Since we can’t natively display array items like we display a string, let’s prototype a method that *console logs* array items in a string format when we call it.

1- Let’s use the same array as before. If you don’t have it on your console yet, declare a new one like shown below:

**var ijk = ["red", "white", "blue"];**

Let’s prototype a function that uses the property *length* to iterate over the array and *console log* each individual item to the screen. The function will be called *listArray*:

![](images/00018.jpeg)

Figure 18 [raw file](http://icontemp.com/joagi/scripts/5.txt). [ icontemp.com/joagi/scripts/5.txt ]

The figure above uses the dot syntax which *binds* a newly created variable name *listArray* to the Array prototype menu, which in turns binds to the **A**rray object. *listArray* points to an anonymous function. This method uses the temporary variable "*i*" to loop over each item of an array represented by *"this"*, until it reaches the end of its *length*. For each iteration, "**this**", which is a *placeholder* for the array calling the function, will print the item on position "*i*".

2- Copy the above prototype script into your editor (see raw file), and then paste it into the console. This will add **listArray()** to the current native Array object instance.

3- Now call **listArray()** on the existing array: **ijk.listArray();** // it returns *red white blue*.

Did you write listArray as listArray( )? It is a function or method so the parentheses are necessary.

Just to prove this method actually belongs to the Array object itself, let’s create a new array and see if we can display its items:

**4-** Declare a new array: **var bcd = ["apples","bananas","grapes"];**

5- Call its listArray() method: **bcd.listArray();** // returns *apples bananas grapes*.

So far we know that a prototype property is used to **add properties and methods** to an *existing* object. We also know how to design the basic script to create such methods. We have seen it with String and we have seen it with Array. No need to memorize anything, **we learn by layers**. When eating an elephant take one bite at a time, right?

Next we are going to discuss the *native* Array methods automatically available when we instantiate a new array object.

a) **Array methods** such as concat( ), join, reverse(), sort(), pop(),push(), shift(), unshift(), slice(), splice()

Some of these Array methods were covered when we discussed the String object and they will sound familiar the second time around. They say that repetition is the mother of learning, especially when we add a new *flavor* to it.

## 2.2.1 concat()

The method **concat()** will concatenate (add) the elements of a second array, into the end of the first array, creating a possible third array if assigned to it, or we could just display it.

If you still have the previous arrays in the console skip the following two steps which are to declare two different arrays (or you can start all over again):

1- Declare an array: **var ijk = ["red", "white", "blue"];**

2- Declare a second array: **var bcd = ["apples","bananas","grapes"];**

3- Now let’s declare a third array and assign it a concatenation of the first two arrays: **var abc = ijk.concat(bcd);**

4- Call in abc: **abc;** // returns ["red", "white", "blue", **"apples", "bananas", "grapes"**]
*ijk* was written first and the other array inside of the parentheses was written second.

5- If you call the other arrays you will see that they haven’t changed.

Also, the elements of the concatenated arrays were **actually copied**. The third array is *not* a reference pointing to the other arrays. If you change or delete any of the first two arrays, the third array will remain unchanged.

We now have three different arrays. If however our intention was to merge those arrays we could have scripted it this way: (**don’t do it so we can use the same arrays on the next topic**)

**ijk.concat(bcd);**

ijk; // returns ["red", "white", "blue", "apples", "bananas", "grapes"]

We could now declare bcd as *null*: **bcd = null;**

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.4 Array.prototype.concat](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.4)

## 2.2.2 join( )

To convert an array into a string we use the Array method **join( )**. This is the opposite of the String method split() which converts a string into an array.

1- If you don’t have the array ***abc*** from the previous topic, declare it as such: **var abc = ["red", "white", "blue", "apples", "bananas", "grapes"];**

**2-** Let’s assign a new string variable to include the elements of the array **abc**: **var abc2 = abc.join();**

3- Call in abc2: **abc2;** // returns **"**red,white,blue,apples,bananas,grapes**"**

Notice how each element of the string is separated by a **comma**. This is the **default setup**. We can specify what separates each element by including the symbol inside the parentheses:

**abc2 = abc.join(" ");**  // returns "red white blue apples bananas grapes".

**abc2 = abc.join("/");** // returns "red/white/blue/apples/bananas/grapes". Etc.

The array **abc** remains unchanged.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.5 Array.prototype.join](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.5)

## 2.2.3 reverse( )

The Array method **reverse( )** reverses the order of elements.

**Reversing is *permanent***:

Reverse **abc**:

**abc.reverse( );** // returns ["grapes", "bananas", "apples", "blue", "white", "red"].

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.8 Array.prototype.reverse ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.8)

## 2.2.4 sort( )

In the method sort(), the sorting order is done alphabetically by default, or from *a* to *z*. However,  alphabetical sorting doesn’t work with numbers since, for example, 20 comes before 3\. This is because the number is converted to string before being sorted and therefore the first digit to the left is the one being sorted accordingly. **To get a true numerical sort we should be more specific** and let JavaScript know about it. This alphabetical sorting happens even if all items are numeric due to String [casting](http://en.wikipedia.org/wiki/Programming_language#Type_system).

1- Let’s test it using the following array,  var x = ["red", "white", "blue", 35, 24];

**x.sort( );** // returns [24, 35, "blue", "red", "white"].

Because JavaScript knows that sorting can become problematic, JavaScript allows passing in a comparison function as a parameter in the sort() parentheses. This function is an example of a ***callback function***. It is named callback because JS is calling back a function that you have provided earlier. (See the function in the image below).

The method *sort( )* processes your *callback function* which is comparing every two items of the array and making a decision. Then it compares the item placed *last* with the *next* item on the array, and so on.

This is the selection criteria:

When the result of the function comparison (*subtraction*) is a **negative number**, the first item goes **before** the second item being compared (no switch is made). When a result is **zero**,  both items are **equal** and no changes in sorting will happen. When a result is a **positive** number, the **first** item switches with the second item making this last one first.

2- Let’s declare a numeric array to see how this works:

**var numA = [5,8,1,3,20];** // normally, 20 would display before 3.

3- Copy the following function to your editor then paste it on your console;

![](images/00019.jpeg)

Figure 19 [raw file](http://icontemp.com/joagi/scripts/6.txt).[ icontemp.com/joagi/scripts/6.txt ]

We will *pass* the function **compareMe** into the **sort()** method. This will *trigger* JavaScript to **take notice of** the result of each array element as it passes through the function. Then a decision is made to place the item accordingly. When **num1 is lower** than num2, the result is **negative**. If they are **equal**, the result is **zero**. When num1 is **higher** than num2, the result is **positive**. JavaScript will sort according to its **internal table**. The function has nothing to do with this decision; the function just helps the decision making by providing a result of its calculation. The sort() mechanism does the rest. This function acts like a filter that gives a rank to each item before the numbers are sorted.

4- Now we can sort numbers correctly:

**numA.sort(compareMe);** // returns [1, 3, 5, 8, 20].

5- What if we want the sort reversed?

**numA.sort(compareMe).reverse();** // returns [20, 8, 5, 3, 1].

Since sort( ) allows us to use a callback function, we could also use it with string arrays to sort by, for example, *word length*. For that, instead of num1 – num2, we would use paran1.length – paran2.length. (the name “paran” is my invention. You can call it anything).

Here’s a sample script for future reference. Note how this script efficiently uses a built in anonymous function as a callback:

![](images/00020.jpeg)

Figure 20 [raw file](http://icontemp.com/joagi/scripts/19.txt).[ icontemp.com/joagi/scripts/19.txt ]

**For more information, please refer to the following ECMASCRIPT 5 page:** [15.4.4.11 Array.prototype.sort](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.11)

## 2.2.5 pop( ) and push( )

The array method **pop( )** *pops out* the **last element** of an array AND it **decrements** the array length by one since one goes along with the other.

1- Create our fruity array *abc* again (or copy it from this  [raw file](http://icontemp.com/joagi/scripts/225.txt)): [ icontemp.com/joagi/scripts/225.txt ]

var abc =["apples","bananas","blue","grapes","red","white"];e

2- Call the array to the console: **abc;** // results ["apples", "bananas", "blue", "grapes", "red", "white"].

3- Remove the last item: **abc.pop();** // removes "white".

4- Call the array: **abc;** // results ["apples", "bananas", "blue", "grapes", "red"].

The “white” element is **gone forever** unless we bring it back with **push( )**:

The array method push( ) inserts an element into the last location.

5- Reinsert the last item: **abc.push("white");** // returns 6\. Six is the number of elements.

6- Call abc again: **abc;** // results in ["apples", "bananas", "blue", "grapes", "red", "white"].

The last element *white* is back again and on the last location since push adds elements to the end of the array.

In a sense the array is acting like a stack restricting the insertion and removable of items in a last-in-first-out fashion. pop() and push() are useful to insert and remove items without having to refer to their specific position. We always know that the action happens at the end of the array.

7- We could push( ) **multiple items** ( manually or in a loop):

**abc.push("peaches","cherries", "apricots");**

8- Now **abc** has 9 items:

**abc;** // returns ["apples", "bananas", "blue", "grapes", "red", "white", "peaches", "cherries", "apricots"].

Let’s remove them again with pop( )  **ah, but wait!!!** Although push() can add several items at once, pop() can only remove one at a time. We would have to *manually* pop() out three times, right? Of course we could also [create a loop](http://icontemp.com/joagi/scripts/225a.txt) and pop all items from the array, but be careful not to go below the array’s total length because you will get an error if the loop goes below zero.

9- Just for practice let’s do it manually three times. This will bring our **abc** array to its original status. On the first time I will unsuccessfully attempt to pop() all of them at once:

**abc.pop("peaches","cherries", "apricots");** // it removed only “apricots”. It ignored the other two elements so we will have to remove the others one by one: **abc.pop( );** // removed “cherries”. **abc.pop( );** // removed “peaches”. We should now be back to the original array’s length: **abc;** // returns ["apples", "bananas", "blue", "grapes", "red", "white"]

**NOTE:** Although we should know about pop() because it is used in many scripts, we could have used **splice()** such as abc.splice(-3,3); splice has several customized options which could come very handy. (splice() will be covered further down in this chapter).

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.6 Array.prototype.pop ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.6)

· [15.4.4.7 Array.prototype.push](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.7)

## 2.2.6 shift() and unshift()

The methods **shift( )** and **unshift( )** are similar to **pop( )** and **push( )**, but instead of acting on the last element, they perform on the **first element of the array**.

Think of an array as a [Pez](http://en.wikipedia.org/wiki/Pez_Candy) dispenser for candy. When we insert a candy into the top of the dispenser we need to push it in. When we remove a piece of candy we pop it. On the other hand, when we insert a piece to the bottom of it we need to unshift the others up one slot, their positions are moved from their original location by one, so they lose location “rank”. If we remove a piece of candy from the bottom the others get shifted by falling downward, their rank location gets promoted.

Here’s our array example: **var abc = ["apples", "bananas", "blue", "grapes", "red", "white"];**

1- Remove the first item: (link to original [raw file](http://icontemp.com/joagi/scripts/225.txt)) [ icontemp.com/joagi/scripts/225.txt ]

**abc.shift();** // removes “apples”.

2- Call the array: **abc;** // returns ["bananas", "blue", "grapes", "red", "white"]

3- Reinsert the first item: **abc.unshift("apples");** // returns 6\. Six is the number of elements.

4- Call the array: **abc;** // returns ["Apples", "bananas", "blue", "grapes", "red", "white"].

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.9 Array.prototype.shift ( )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.9)

· [15.4.4.13 Array.prototype.unshift](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.13)

## 2.2.7 slice( )

Just like it does in a String object, the method **slice( )** extracts items from one array and **returns** a new array with the extracted data. Changes to items in the old array do not get affect unless the method is applied to the same array.

This method takes two parameters. The first number indicates the *zero* based **first item to be sliced**. The second number indicates the first item **not** to be sliced. ([raw file](http://icontemp.com/joagi/scripts/225.txt)). [ icontemp.com/joagi/scripts/225.txt ]

1- Create the same **abc** array as before (see raw file above):
**["apples", "bananas", "blue", "grapes", "red", "white"]**

2- Let’s apply *slice( )* by creating a new array based on our *abc*, but excluding **“red”** and **“white”**: **var abc2 = abc.slice(0,4);**   
// starts at zero and exclude position 4 and over.

3- Call the new array: **abc2;** // returns ["apples", "bananas", "blue", "grapes"] which are locations 0,1,2,3.

**Negative numbers in slice():**

There is more to **slice( )** than what we just experienced. By using **negative numbers** we can select items from the end of the array length (right most position) to the beginning. Let’s see a few examples to illustrate this confusing topic:

4- Our array **abc** is
**["apples", "bananas", "blue", "grapes", "red", "white"]**.

5- Declare another array and assign it the result of negatively slicing abc by -2: **var abc3 = abc.slice(-2);** // it will **copy** the last two items from *abc*. A negative number selects from the right to the left a number equivalent to is number designation. In this case, it picked two items from the right. Here we are not speaking of location position but on number of items.

**abc3;** // returns ["red", "white"].

6- Assign another array to **abc** sliced with two negative numbers: **var** **abc4 = abc.slice(-4,-2);** // this will copy the 4^(th) item **from the last** and the 3^(rd) from the last, since it cuts off on the second from the last item. So we could say “start from the 4^(th) from last and exclude the last two”. **abc4;** // returns ["blue", "grapes"].

The best way to learn slice() is to practice by using different scenarios based on an array of your choice. Also, return to this page when you need to refresh your mind.

For another example on slice, see section 3.1.1.

**For more information, please refer to the following ECMASCRIPT 5 page:** [15.4.4.10 Array.prototype.slice](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.10)

## 2.2.8 splice( )

The Array method splice( ) is a very interesting one. Do you still remember push and unshift? they add items to the end or beginning of an array, right? splice() adds items to the middle ( or anywhere in the array).

Let’s see how it works.

Depending on how many arguments you use in the parenthesis, you can the following:

a) **Delete** **items** mode:
When you use only **two arguments** you are giving the **index positions** of
*First argument*:  where the action is to start (inclusively), 
*Second argument*: How many items will be removed.

**Two arguments** means deleting because there is nothing to add.

b) **Add** **items** mode,
If you insert **more than two arguments**, the ***third*** and consecutive arguments are **data to be inserted**, and in that case JavaScript assumes you want to insert items into the array.

In juts add mode, the second argument is *zero*, which means that no items will be deleted in exchange for the items we are adding with the third and consecutive parameters.

c) **Replace items** mode. If the second parameter in ***add mode*** is anything other than zero, this number will indicate how many items will be deleted in exchange for the items being added.

For example **splice(0,3)** means to delete 3 items: the first, second and third. Number 3 represents the quantity of items to be removed. The number 3 coincides with the third item on the array but it is not necessarily so. If we had splice(2,3) it would remove the third, fourth and fifth items, which correspond to positions 2,3,4 and counting from zero.

The 3^(rd) and consecutive arguments represent the items to be inserted.
For example, **splice(2,0,** **"yellow")** means to insert *yellow* in position two (third item) and un*shift* the others because the zero means that no items are to be deleted.

In **splice(2,1,** **"yellow")**  it means to add *yellow* to position 2 ( third item) and remove whatever is there (this is a replacement due to the second argument).

The picture below will illustrate the concept:

![](images/00021.jpeg)

Figure 21

Let’s try a few samples to illustrate the concept.

**Deleting** items with splice( ):

**1-** Declare an array [raw file](http://icontemp.com/joagi/scripts/228b.txt): [ icontemp.com/joagi/scripts/228b.txt ]  **var x = ["blue","red","green", "violet", "brown"];**

2- Delete 3 items starting at positions 0: **x.splice(0,3);**

3- Call in the array: **x;** // returns ["violet", "brown"]. Items in positions 0,1,2 were deleted.

**Adding** items with splice( ):

4- Let’s add our items back into the array, starting at position zero: **x.splice(0,0, "blue","red", "yellow");**

4- Call the array: **x;** // returns ["blue", "red", "yellow", "violet", "brown"].
We started at position zero and added all the listed items and deleted zero items.

What would happen now if the second digit was 3 instead of zero? splice() would first deleted three items, and it would replace the same three items back.  **No change**.

Remember the footnote on the topic pop( )?

**abc.splice(-3,3);** note: if you want to try it change *abc* for *x*.

The -3 counts 3 items from the right as an inclusive starting position. The second number means to delete 3 items with no replacements.

**Extracting items into another array:**

Up to now we have been editing the same array *x* but we could also extract the items we are currently deleting into another array, like if we were splitting the array in two, sort of like using *slicing()* with the addition of deleting the items from the original array:

5- Take for example the original array ***x***: **var x =["blue","red","green","violet","brown"];**

6- Split the array by copying the first three items into ***newArray*** before deleting them: **var newArray = x.slice(0,3);**

7- Call array ***x***: **x;** // returns ["violet", "brown"]

8- Call array ***newArray***: **newArray;** // returns ["blue", "red", "green"].

**For more information, please refer to the following ECMASCRIPT 5 page:** [15.4.4.12 Array.prototype.splice](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.12)

# 2.3 New JavaScript Array Iteration Methods

## 2.3.1 forEach()

Do not confuse forEach() with **for each… in** which has been *[deprecated](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for_each...in)* in JavaScript.

*forEach* is a function which takes another function as an input argument.

The array method **forEach( )** was introduced with ECMAScript 5 *when* nine new methods were added to help developers create ways of searching and manipulating array contents. These methods perform operations that previously would have required complex iterative loops. The nine additions are: **indexOf**, **lastIndexOf**, **every**, **some**, **forEach**, **map**, **filter**, **reduce**, **reduceRight**. **All these methods are variations of the forEach() method which I’m about to discuss**.

forEach( ) performs a specified action for each element on the array. The specification of what to do is written by the programmer as a function in the form of an argument to the forEach() mechanism.

Remember, the purpose of a function is to store some code that will run when the function is called. We create the function, and forEach() will process it.

So, forEach( ) takes a **function as its argument**. The parameters of the function itself will *interface* with each **valid** element of the array in an iterative manner, just like a loop would do. By valid element I mean an element with data ( not an empty element location). Empty or undefined array indexes are ignored.

1- Let’s experiment with this method in increments. Start by introducing on the console a new array (I’m using the Chrome console):

**var g = ["red", "blue", "white"];**

2- *Call* forEach( ) on the array **g** by using a function with just one parameter, “**y**” . In this function we stored a simple console.log output (see the figure below):

![](images/00022.jpeg)

Figure 22 [raw file](http://icontemp.com/joagi/scripts/20.txt).[ icontemp.com/joagi/scripts/20.txt ]

The function being used here may contain up to 3 arguments. The first argument (as the example above), points to the array data. Do you remember when on the chapter **More Primitive and Reference Values** we mentioned how we could point to a *reference type* value such as an array, via a function parameter? Review that lesson chapter if you need refreshment.

This forEach “*macro*” saves us a lot of coding, such as what we used to script this way:

for (var i = 0; i < array.length; i ++)

In the forEach( ) example given above, parameter ***y*** will point to the value of each index on the array, and the method **forEach** will process each value according to the **instructions written in the body**. In this case the next instruction is to *console.log* each value at each “y” iteration and the result is: *red blue white* (in separate lines).

You may ask “*How does JavaScript does all these?*” and the answer may be “*Don’t ask! let it go for now. Learn how to use the tool not how the tool was conceived*”. knowing how the tool was conceived is a curiosity that interferes with your mastering of the trade. Leave that question for later when you have time to spare.

**Two arguments instead of just one:**

3- Let’s try the same script with two arguments instead of just one:

![](images/00023.jpeg)

Figure 23 [raw file](http://icontemp.com/joagi/scripts/21.txt).[ icontemp.com/joagi/scripts/21.txt ]

As seen before, the first argument points to the element **data**. The second argument points to the **index** location of the data. In the example above we were able to print the index and the value for each element of the array **g**. Note that arguments y, index are arbitrary names. You can name them anything.

**Notes:** forEach calls the *callback* function once per item in the array like a loop would do. The calling is done in ascending order.

Sometimes a **third parameter** is used to specify the Array being traversed.

The forEach function is intentionally generic; it does not require its third parameter to be an Array object. Therefore it can be transferred as a method to other kinds of objects. However the functionality of forEach with other types of Objects is implementation-dependent.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.18 Array.prototype.forEach](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.18).

## 2.3.2 map( )

The method map( ) iterates an array just like forEach( ) does, with the exception that it actually **returns a value**, and because it returns a value, it can be used to create a second modified array based on the first. Also, contrary to  *forEach()* that calls the function for every item that iterates, *map* calls the function once for the whole process.

Here’s an example:

1- Declare a new array (see raw file bellow image):

**var firstArray = ["amazon", "nile", "kwanza"];**

2- Declare a second array and assign it value by mapping and returning the contents of firstArray. To be sure they are visually different, convert them to *upper case*. After scripting  a map, call the second array:

![](images/00024.jpeg)

Figure 24 [raw file](http://icontemp.com/joagi/scripts/22.txt).[ icontemp.com/joagi/scripts/22.txt ]

Just like in *forEach( )*, we used a function to store some code that takes the item from the array it points to,  and returns it in upper case. This return is then assigned to another array (our *secondArray*).

By using **map()** instead of forEach(), each element was copied into another array we arbitrarily named *secondArray* and via the *return* mechanism. If you try to assign a forEach() to another array it will not work like it does with map(). Like for each(), map() is just a *macro* and its magic is internal. All we do is to input parameters to be worked on (such as “item” in our case).

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.19 Array.prototype.map](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.19)

## 2.3.3 every( )

The method **every( )** is another iterative mechanism. It is called “*every*” because whatever is going to be checked, must be **true** for every item in the array (all items), or it will return **false**. This is a read only method. It doesn’t change anything in the original array. It can be used for testing and searching, like using **every( )** to inspect an array and make decisions based on the outcome.

Here’s a sample script where we check if the elements are all *odd* or all *even*. If even, return true, else, return false:

1- Declare a new array with a mix of odd and even numbers:

**var abc = [1,2,3,4,5];**

2- Call the array **abc** with the method **every( )**, using a function that checks for *even* numbers. If all items do not match, *every ( )* will result in “**false**”:

![](images/00025.jpeg)

Figure 25 [raw file](http://icontemp.com/joagi/scripts/23.txt).[ icontemp.com/joagi/scripts/23.txt ]

**Remember from the previous two methods:** “item” is just a generic name representing each element of the array. It serves as an *interface* by pointing to each element (I put emphases on each because all these methods are different versions of **forEach( )**). As *item* points to the elements of the array and the function does its magic, **every( )** gathers the results and applies them to my own program, which is inside the body area.

If on the other hand (in this case) the array is “all even” (based on the sample script), every( ) will return *true*.

Remember, the purpose of this function is to store code that can be used when every() calls the function. This internal function does not have to be named, it is known as an anonymous function or a callback function because it gets called back when needed and there is no reason for a pointer to it because it is internal to the every() script.

3- Here’s a sample of an array that will return true:

**var xyz = [2,30,40,60];**

4- After declaring the array from the previous step, change the script on the above figure to apply **every( )** on **xyz** instead of on **abc**. The result should be *true*.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.16 Array.prototype.every](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.16).

## 2.3.4 some( )

When it comes to *all or nothing*, the method **some( )** is the *opposite* of **every( ).** It will return **true if *any*** of the elements checks positive to the query criteria. As *every( )*, it doesn’t change the original data, it only **reads the data** and reports back. It is up to us to manipulate the data in question.

The method *some()* can be used to test a script of the existence of a certain element or condition.

Here’s a sample script based on the same data from the last exercise:

1- Declare an array ( if not yet declared):

** var abc = [1,2,3,4,5];**

2- Call the **some( )** method to check if any of the elements in the array are even. As long as *one* element is even, the result will be true:

![](images/00026.jpeg)

Figure 26 [raw file](http://icontemp.com/joagi/scripts/24.txt).[ icontemp.com/joagi/scripts/24.txt ]

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.17 Array.prototype.some](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.17)

## 2.3.5 filter( )

The array method **filter( )** works the same way as **some( )**  but instead of returning true or false, it **returns an array** containing the elements that qualify as true.

Let’s use the same *abc* array as an example.

1- Declare the array **abc**  if it hasn’t been declared before:

**var abc = [1,2,3,4,5];**.

What we want here to do, is to extract all the *even* numbers into a new array.

2- Declare a new array abc2 and use **filter( )** to iterate through each item and fetch all **even** numbers into it:

![](images/00027.jpeg)

Figure 27 [raw file](http://icontemp.com/joagi/scripts/25.txt).[ icontemp.com/joagi/scripts/25.txt ]

3- Call array **abc2** as per line 9 and observe the result which should be even numbers such as [2, 4].

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.20 Array.prototype.filter](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.20)

# 2.4 New JavaScript Array Reduction and Location Methods

## 2.4.1 What is Reduction

In computer Science a *reduction* is an algorithm for transforming one problem into another problem, or the conversion of an expression or equation into its simplest form.

ECMASCript 5 has introduced two methods of reduction, **reduce( )** and **reduceRight( )**. The difference between one and the other is the *direction* in which they operate. One starts at the beginning of the array, the other starts at the end of the array.

Both reduction methods take an anonymous function where we can save some *code customization* of our own, and an optional base value:

![](images/00028.jpeg)

Figure 28

**The *initValue* is an arbitrary name for a parameter in the reduce/reduceRight methods that change the outcome:**

If the **initValue** is present, the function iteration will start at the *initValue* value.

In the JavaScript reduction methods, when an *initValue* is present, the first parameter of the anonymous function which I will call ***previousValue*** starts at the **initValue**‘s value. The second parameter of the function, which I call **currentValue**, starts at the value of the first item.

![](images/00029.jpeg)

Figure 29

Normally the **initValue** is not present and in this case, the first parameter, **previousValue**, starts at the first item value, and the second parameter, **currentValue**, starts at the second item value.

See the next two examples for further explanation.

## 2.4.2 reduce( )

The method **reduce( )** allows a callback function with up to four arguments:

a) *previousValue* - The value from the previous call to the callback function.

b) *currentValue* - The value of the element at current iteration (position).

c) Optional *current index*, or location of the object being traverse. You can exclude the index as a parameter, or included it if you need to influence the calculation process.

Let’s look at an example. We are going to declare an array with **even** numbers. Then we will declare a variable to store the result of multiplying all numbers of the array, using reduce( ).

1- Declare array **qaz**:

**var qaz = [2,4,6,8];**

2- Declare a variable **addQAZ** and assign **qaz** to the variable where both left and right values are multiplied by one another with the help of the method *reduce( )*:

![](images/00030.jpeg)

Figure 30 [raw file](http://icontemp.com/joagi/scripts/26.txt).[ icontemp.com/joagi/scripts/26.txt ]

3- Call **addQAZ;** 
// returns 384.

On the first iteration, previousValue is 2 (first element), and the currentValue is 4 (second element), and so on.

However, if we had included the **initValue**, which would go here: **}, init);** the *previousValue* would have started at the *initValue* given, and because of that, the *currentValue* would have started at the first element’s value instead of at the second’s, resulting in a totally different output since the *initValue* value would have influenced the operation at hand. See the next example:

4- For example, let’s declare another variable using the same script as before but giving *reduce( )*  an **initValue** of **10**:

![](images/00031.jpeg)

Figure 31 [raw file](http://icontemp.com/joagi/scripts/27.txt).[ icontemp.com/joagi/scripts/27.txt ]

5- Call **addQAZ2;** // returns 3840\. A big difference from before.

**For more information, please refer to the following ECMASCRIPT 5 page:** 

· [15.4.4.21 Array.prototype.reduce](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.21)

## 2.4.3 reduceRight( )

The array method **reduceRight( )** works the same way as the previously described method reduce( ). The difference is **where it starts**: *reduceRight()* starts processing from the last two elements of the array, whereas *reduce()* starts processing from the first two elements of the array. One works from right to left, the other works from left to right. Everything else that has been described for *reduce( )*, also applies for *reduceRight( )*.

If we use the previous script (multiplication) to *reduceRight( )*, the result is the same, 384 and 3840\. For testing purposes just **change “reduce” to “reduceRight”** on line 2 in the examples given above.

For illustration’s sake let’s try a different script. This time we subtract one value from the other to see how these methods differ:

1- Use the previously declared array **qza**. If you are restarting you JavaScript console, declare the array as shown below:

**var qaz = [2,4,6,8];**

2- Follow the next two steps on the figures shown below to test *reduce* **and** *reduceRight*, when values are subtracted:

![](images/00032.jpeg)

Figure 32 [raw file](http://icontemp.com/joagi/scripts/28.txt).[ icontemp.com/joagi/scripts/28.txt ]

3- Call **subQAZ;** //  returns -16.

4- Change the method to *reduceRight*:

![](images/00033.jpeg)

Figure 33 [raw file](http://icontemp.com/joagi/scripts/28b.txt).[ icontemp.com/joagi/scripts/28b.txt ]

5- Call **subQAZ;** 
// returns -4.

In the above example, **subQAZ** returns **-4** when using reduceRight, as opposed to **-16** in the prior exercise.

As you can see the result of subtracting all the array items is quite different between *reduce* and *reduceRight*. Keep these differences in mind when looking for code solutions.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.22 Array.prototype.reduceRight](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.22)

## 2.4.4 Location Methods

Beyond the *iteration* and *reduction* methods, JavaScript has two new methods that can be used to locate items in the array:  **indexOf( )** and **lastIndexOf( )**.

IndexOf starts from the left to the right, and lastIndexOf starts from the right towards the left.

They both work the same way and give the same location reference position.

However, since they only report the first item that matches, if there are two similar items in the array, the *lastIndexOf* will find the very last first, and that is the one it will report.

## 2.4.5 indexOf( ) versus lastIndexOf( )

If all we need is the index of one specific and unique item, ***indexOf*** and ***lastIndexOf*** will give us the same performance. However in long arrays, one may be faster than the other depending where the item is located, if at the first half or if at the last half.

Should there be more than one item of the same, choosing one method over the other will output different results.

**1-** Let’s declare a new array on the console ([raw file](http://icontemp.com/joagi/scripts/245.txt)): [ icontemp.com/joagi/scripts/245.txt ]  **var x1 = ["peanuts", "almonds", "walnuts", "heartnuts"];**

2- Call the index of  “walnuts” using **indexOf( )** : **x1.indexOf("walnuts");** // returns 2 because it counts 0,1,2.

3- Call the index of  “walnuts” again, but this time using the **lastIndexOf( )**: **x1.lastIndexOf("walnuts");** // returns 2.
Although it searches from the right, it reports the position counting from the left (it decrements instead of incrementing).

4- Let’s try it with “peanuts”: **x1.indexOf("peanuts");** // returns 0. **x1.lastIndexOf("peanuts");** // returns 0.

From the examples above, there is no difference in what is returned in both methods as applied to this simple script.

However if there are two elements alike, the results will be different. Consider the next exercise:

5- Add a second element “walnuts” to the end of the array by using **push( )**: **x1.push("walnuts");** // returns ["peanuts", "almonds", "walnuts", "heartnuts", "walnuts"].

6- Call the index of  “walnuts” using **indexOf( )** : **x1.indexOf("walnuts");** // returns 2.

7- Call the index of  “walnuts” using the **lastIndexOf( )**: **x1.lastIndexOf("walnuts");** // returns **4**.
It finds the last “walnuts” first.

**If the item being searched is not in the array, both of these methods will return a** **-1**.

How are these elements being compared?  The index methods compare, the elements used for search, to the elements in the Array, using **strict equality**, which is the same method used by the === (the triple-equals operator). If the elements differ in syntax or type, the algorithm will return a -1 as of "*not found*".

**Optional second argument: Where to begin.**

There is a **second optional argument** that could be used with  *indexOf( )* and *lastIndexOf( )*.

This second optional argument is commonly *known* as fromIndex ( any name will do).

The optional *fromIndex* argument specifies the array index at which to begin the search (inclusively). I mean, it is possible to bypass a portion of the data and start searching further down the pipe.

 *fromIndex* is base zero, which means the first element counts as 0 and the 1,2,3, etc.

Based on the sample we currently have on the console:

**["peanuts", "almonds", "walnuts", "heartnuts"", "walnuts"];**

8- Let’s experiment with the *fromIndex* parameter, using an argument of **2**: **x1.indexOf("walnuts",2);** // returns 2
(found the first “walnuts” which by coincidence it is the first item to be searched.

**x1.indexOf("walnuts",3);** // returns 4
(passed the first "walnuts", finds the second "walnuts".

Now let’s see how the *lastIndexOf* behaves: **x1.lastIndexOf("walnuts",2);** // returns 2
It couldn’t find the last “walnuts” because it only searched from item 2 and down to zero ( like **2**,1,0) and “walnuts” was on location 2 from zero. Remember, it searches towards the left and it began at the third element, position 2, so nothing at the right of position 2 was scanned.

9- One more test: **x1.lastIndexOf("walnuts",4);** // returns **4**.
Found the first “walnuts” from the right to the left.

**Search criteria summary.**

The following is a summary for both *indexOf* and *lastIndexOf*. It is written for future reference. Do not confuse yourself trying to memorize these rules. Just refer to them when you need to implement the method at a later date.

· **Search criteria for the indexOf( ) method:**

a) In the indexOf( ) method, the optional second argument **fromIndex**, defaults to 0\. If the fromIndex argument is missing, JavaScript assumes fromIndex as zero. If on the other hand, the fromIndex is greater than or equal to the length of the array, search will not be performed and a **-1** will be returned.

b) An indexOf with a **positive number**, indicates where to start searching from (inclusively), and thereafter, search is done to the right. Example: a fromIndex of 1 starts searching on the second element (inclusively) because it is zero based.

c) An indexOf with a **negative number**, is used to offset the first element to be searched, based on the array’s length **plus** the negative number. Counting is zero based: (-1 in a length of 5, makes it start at position 4, which is 0, 1, 2, 3, 4 or the fifth element), and thereafter, search is done to the right.

Example:

1- Remember, our **x1** is **["peanuts", "almonds", "walnuts", "heartnuts", "walnuts"]** **x1.indexOf("walnuts", -2);** // returns 4 because ( 5 -2 = 3. Three is actually element 4 (heartnuts) which already passed the first “walnuts”. The index for the *next* “walnuts”, the fourth element, is returned instead).

· **Search criteria for the lastIndexOf( ) method:**

a) The *fromIndex* defaults to the ***array's length -1*** when used with the lastIndexOf( ). Which makes sense since it starts from the right.

In an array with 5 elements, it defaults to 4 which means that all elements will be searched: 0,1,2,3,4\. In the previous method it defaulted to zero since it moved from left to right. Also a *fromIndex* larger than the array length will not make a difference how the array will be searched. In an array with 5 elements, a *fromIndex* of 5 or 6, etc. will act the same as a *fromIndex* of 4.

b) A *lastIndexOf( )* with a **negative** **fromIndex**  will start the search at an **offset** position based on the length **plus** the negative number. An array with 5 elements and a -1 as *fromIndex*, will start searching at default which is the very last element, position 4 or element 5\.

2- In our example, it is the last “walnuts”: **x1.lastIndexOf("walnuts",-1);  //** returns 4.

Similarly, the same array with 5 elements and a **-2** as ***fromIndex*** will start searching from position 3 or element 4\.

3- In our example, it starts at “heartnuts". **x1.lastIndexOf("walnuts",-2);** // returns 2.
It initiated search after the first “walnuts” from the end.

c- When using the ***lastIndexOf( )*** method, a ***fromIndex*** with **positive** **number** determines what position to start searching from (right to left). Example: a fromIndex of 0 will only search the very first item, which in our example it is “peanuts”. A fromIndex of 1 will only search the second and the first elements, in that order. Etc.

**For more information, please refer to the following ECMASCRIPT 5 page:**

· [15.4.4.14 Array.prototype.indexOf](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.14)

· [15.4.4.15 Array.prototype.lastIndexOf](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.15)

# PART III – ENTERING THE SECOND REALM

“Knock on the sky and listen to the sound.” * A Zen Saying*

# 3.1 JavaScript Functions and Arguments as Objects

From a previous chapter on Part 1, you were told how every function in JavaScript is actually an object. Let’s explore this concept a bit further.

## 3.1.1 arguments

In ECMAScript 5, **arguments** are no longer properties of the function as they used to be. They have been upgraded to *objects* that look like arrays but with only one array property available from the array library: **length**.

Length is and important property since it facilitates iteration by looping over each existing arguments’ element.

An *arguments object* acts like a local variable of the function. It only really works with functions. It is called into action by the function itself, or by any subfunction within the function (after proper binding is applied as seen later). You cannot explicitly create an arguments object since it only becomes available when a function **begins** its execution. This *arguments* object has an array with a holding capacity of up to 255 items.

The number of argument **parameters** is declared individually within the function parentheses. However, we don’t really need to *formalize* this parameter’s **declaration** in order to pass data into the function. It all depends on what the inside code asks for this input data. Consider the following example:

1- Declare a function **x** with no parameters and return the  object argument**s**:

![](images/00034.jpeg)

Figure 34 [raw script](http://icontemp.com/joagi/scripts/33.txt). Purpose: Returning all arguments.
[ icontemp.com/joagi/scripts/33.txt]

1- Call the function and include a few values: **x("cow","dog");** // returns all arguments passed in: ["cow", "dog"]

2- Call the function with *even* **more** values: **x(1,2,3,4,5,6,7,8,9);** // returns [1, 2, 3, 4, 5, 6, 7, 8, 9]

Although *arguments* looks like an array we know it is not a *real* one. However, if we wanted to, we could actually convert it into an array by using the array’s **slice( )** method (review this method on the previous chapter if needed: **2.2.7 slice( )**, and once converted, we could use its data for further processing.

As an example, let’s use some of our previously acquired knowledge for multiplying all the arguments, by utilizing the array **reduce( )** method. Let’s try it:

3- Write (or copy) the following function (lines 1 – 9) on your editor and *paste* it to the JS console. **Then** call it, like it shows on line 11 below:

![](images/00035.jpeg)

Figure 35 [raw script](http://icontemp.com/joagi/scripts/29.txt). Purpose: working with the arguments object. The use of call().
[ icontemp.com/joagi/scripts/29.txt ]

· If you get a bit lost on this next explanation don’t worry about it, just come back to it next time around and you will understand a bit more. Especially after you finish this book and do a review. Understanding comes in layers, at least that’s how it happened to me and it is still happening every day.

· On line 1 the function **x** was declared with **no formalized parameters**.

· On line 3 we declared a variable *randomly* named **gts**, and assigned it an extraction of the object **arguments** of the function x as an array, by utilizing **slice( )**. We needed to call its full path here in order for gts to be recognized as an array. As a shortcut, we could also have used the following script:

**var gts = [ ].slice.call(arguments);**

· Line 3 introduces something new to us, **.call( )**, which is a method from the function object we will discuss a bit later. **call()** makes sure we apply "*this*" to the intended target by binding it to whatever we name in the inside parentheses, which means in this case:  “*from this particular function which name is x, call **its** arguments*”.

· Line 5 mathematically “**reduces**” the new array, and returns its calculation. If you need to review please go to the section **2.4 New JavaScript Array Reduction and Location Methods**.

· Line 11 tests our script by calling the function with a few arguments as an example. These arguments are **copied** by the function and processed to give us a result of 120.

4- If you need further understanding of the **.cal( )** method, try the following example as an exercise. We will cover more about it on section 3.2 Function Properties and Methods:

![](images/00036.jpeg)

Figure 36 [raw script](http://icontemp.com/joagi/scripts/44.txt). Purpose: Peeling the onion:  understanding call().
[ icontemp.com/joagi/scripts/44.txt ]

· On line 1 we declared a string variable z.

· On line 3 – 6 we created function **b** (somewhat similar to the previous function **x**) in which we declared a variable getZ and assigned it a string array from the string in “**z**’. We point the array to “**z**” by including it as the first parameter in the **call( )** method. Remember, call() redirects “this”. Normally ‘this’ is pointing at the object that owns the script at the time of action.

· On line 4 just like before, we request the prototype of the **Array’s slice** and apply it to whatever is being pointed to by the **call()** method.

· On line 8 we address function **b()** which returns an array of the string,  line 9.

**Going back to the *arguments* object in a function…** **why would we formally include parameters in a function, when in fact we can *pass in* any arguments without *formally* using parameters**? One obvious answer is that when we include parameters, we **establish a *sequence*** of items to be introduced into the function, which allows for specific processing of each argument.

Let’s do a test by creating a function **with** *parameters*:

5- Declare a function which takes two arguments into the parameters **x** and **y**, and returns them back:

![](images/00037.jpeg)

Figure 37 [raw script](http://icontemp.com/joagi/scripts/30.txt). Purpose: The role of parameters in a function.
[ icontemp.com/joagi/scripts/30.txt ]

6- Try the following test calls: **aba(7,11);** // returns "x= 7, y= 11".
Data in, same result out. **aba(7);** // returns  "x= 7, y= undefined".
 x was outputted, y was missing. **aba(7,11,9);** // returns "x= 7, y= 11".
The *last* parameter was *dismissed* because the return *script* had no way to grab it.

7- Let’s change the function so it processes more parameters than what we originally intended it for:

![](images/00038.jpeg)

Figure 38 [raw script](http://icontemp.com/joagi/scripts/31.txt). Purpose: How arguments process output, as opposed to formal args.
[ icontemp.com/joagi/scripts/31.txt ]

By changing line 2 to **return arguments** instead of naming them individually, we can output any number of arguments (up to 255).

8- Test it: **aba(7,11,9,45,57,89);** // returns [7, 11, 9, 45, 57, 89].

9- Here’s another example accessing unlimited arguments with a **for loop** targeted at the arguments’ **length**:

![](images/00039.jpeg)

Figure 39 [raw script](http://icontemp.com/joagi/scripts/32.txt). Purpose: accessing unlimited arguments with a for loop.
[ icontemp.com/joagi/scripts/32.txt ]

10- Call the function with fruits: f("banana","apple","grape","peach"); // returns banana is a fruit, apple is a fruit, grape is a fruit, peach is a fruit.

In summary, the new arguments object along with formal parameters of a function open a tremendous amount of possibilities.

Use formal parameters whenever you want a specific sequence of inputs, and the arguments object for more creative scripting.

The last two exercises might have been a bit advanced for some readers but please don’t stop here. Everything will be much clearer in the next few topics. Just give it a chance.

## 3.1.2 Nested Functions

Nested functions are functions inside of functions. These inner functions have access to all the data of the outer functions which gives them immense power. The purpose of this next topic is to develop a basic understanding of some important characteristics of inner and outer functions.

## 3.1.3 A Gentle Introduction to Closures

1- Suppose we have an array assigned to the variable **ara**:

**var ara = [1,2,3,4,5];**

2- And we assign ara to **ujo** and then,  ujo to **tony**:

**var ujo = ara;**

**var tony = ujo;**

*What did we just do?*

We’ve created three variables that point to the same array on the heap, right?

Let’s test it to be sure:

3- **ujo;** // returns [1,2,3,4,5].

4- **tony;** // returns [1,2,3,4,5].

5- **ara;** 
// returns [1,2,3,4,5].

6- If  we now declare the original variable **ara** as *null*:

 **ara = null;**

7- The array still exists under the symbols **ujo** and **tony**, right?

**tony;** returns [1,2,3,4,5]

As long as the array still has some variable pointing to it, the array will not be flagged for *garbage collection*.

## 3.1.4 The closure principal

“Knowledge is *closed* under entailment”. Entailment means “logical consequence”. If A knows B, and B entails C, then A knows C.

In the array described above, when variable **ara** was declared *null*, normally the array would be placed for **garbage collection**. However, it is said that variables **ujo** and **tony** had closure on the *array* and therefore, the array survived the dismissal of its original pointer ara.

In JavaScript, closure “talk” is usually referred to functions since when a function returns, it ends and it is sent to garbage collection. However, if there is an **inner function** still holding the thread to the inner variables of the outer function, those variables will not be destroyed. They will remain in the **execution context** until the inner function finishes its job.

Before we get to function examples, let’s analyze the picture below, just to be sure we understand the principle behind closures since there isn’t much literature about it out there.

![](images/00040.jpeg)

Figure 40

1- Let’s create an easy function to experiment with closures:

![](images/00041.jpeg)

Figure 41 [raw script](http://icontemp.com/joagi/scripts/59.txt).[ icontemp.com/joagi/scripts/59.txt ]

2- Call the function on boy: **kiteFlying("boy");** // returns "has kite".

“**boy**” returns the variable **boy** which is “*has kite*”.

3- Call the function on girl: **kiteFlying("girl");** // returns "has kite".

“**girl**” triggers *else*, which triggers the function girl( ), which in turn, return the contents of **boy**, which are “*has kite*”. When girl( ) activates**,** kiteFlying( ) has already returned, but variable boy is still available because girl() has closure rights.

The above function has an inner function and based on the argument given it returns either the **boy** from the outer function or **girl** which is the inner function.

However, as you know, when a function returns, it gets *wiped out*. In this case, if the function returns “else”, which is another function, it still gets wiped out, but the inner function is able to fetch the variable from the outer function in the process of returning while the outer function is already gone. Then the inner function also gets wiped out.

**The question is:** How does the inner function access the outer function’s variable, when the outer function no longer exists? Remember the picture with the balloons above the script?

**This is what happens:**

1- JavaScript looks at the outer function at the time of calling and makes an inventory:

**Outer function**, **variable boy**, “**has kite**”

2- JavaScript also looks at the inner function and makes an inventory:

**Inner function**, ***mapped* variable boy** (a *free* gift from outer function), “**has kite**”.

Then, it does not matter what happens to the outer function. As long as the inner function is still processing, JavaScript keeps a pointer to the surrounding applicable variables such as **boy = “has kite”**. And that’s because of the **inventory list** JavaScript first made.

JavaScript functions aren't really just pieces of code you can execute; they are **closures**, like [dreamcatchers](http://en.wikipedia.org/wiki/Dreamcatcher), they are symbols of unit.  A closure records not only what code a function must run, but also what environment it was created in. An inner function has access to the outer function and the outer of outer function, all the way up to the Global object.

![](images/00042.jpeg)

Figure 42

Sometimes we read on the web how closures have “*free* variables”. By free variables it is meant all those variables a function can use but are not in the function. In this illustration, func2 has the following free variables: A, B, and C. ( D, it is not free, it belongs to func2).

Below we have another way of seeing it based on the balloon concept. This demonstrates which balloons are being held by whom at the time **function1** is instantiated (called):

![](images/00043.jpeg)

Figure 43

Taking the concept of the above illustration as an example, we could use func2 to make the outer function variables *more* private if we wanted to. We would do this by outputting the outer function variables through the inner function, creating a shield between the outside world and *function 1*. Consider the following example:

![](images/00044.jpeg)

Figure 44 [raw script](http://icontemp.com/joagi/scripts/61.txt).[ icontemp.com/joagi/scripts/61.txt ]

In the above example, we further isolated the outer function data (clientBalance) from the public scope. We did this by creating an **inner** function which acts as an **interface** between the outer function and the outside world. The outer function’s data remains private as there is no output directly from it. The process works due to the closure principle, which keeps tabs on the **lexical environment** (covered next), even when the outer function returns before the inner function does, which is the case. The outer function outputs the inner function which in turn returns its result. Its result (inner) is based on the data in the outer function.  The data in the outer function does not get wiped out *during the microseconds when the outer function returns and closes*, because the inner function is still pointing at its (outer) data. It only gets wipeout (outer) after the inner function returns and places itself and its entire lexical environment, at the mercy of the garbage collection mechanism.

So what is the purpose of all these?

The purpose is to prevent any script from the outside to view or edit the private variable *clientBalance*. This variable is only being accessed by the inner function, which is being called from the outside via the outer function. Sort of like a bank clerk accessing the vault to remove money for someone cashing a check. 

## 3.1.5 Lexical Scope

Lexical means “words that refer to things” or a “menu of things”. In languages *without* closures, the lifetime of a local variable ends with the execution of the scope where that variable is declared. However, in languages with closures, such as JavaScript, variables *continue to exist* well after the code is done, **as long as** there are **closures** surrounding them.

Since scope in JavaScript is determined by functions, functions are also the ones that create closure environments, which connect variables and arguments to running processes. As you remember, a closure happens when a mechanism in an inner scope points to data in an outer scope, and JavaScript needs to keep a log of *potentially necessary* data, preventing any active scope from being wiped out. This persistence method is normally done by the garbage collection mechanism. *Garbage collection* is managed by the browser, and it varies depending on which browser and its version JavaScript is being run on.

The image below illustrates a set of nested functions and their scope environment, also known as **lexical (or static) scoping** “Every inner level can access its outer levels”:

![](images/00045.jpeg)

Figure 45

In the figure above, if you attempt to directly return (the most inner function) function 3, from function 1, it will give you a “**ReferenceError: Function3 is not defined**”. To access function **3** from function **1**, one must first have a return from 3 to 2, and then from 2 to 1, in order for function 3 to be available to function 1. This is because an inner function is only available to the immediate function above it. However, as seen, Function 3 has access to its *entire environment* which spans all the way up to Window or the Global Scope. **It’s a one way street, functions point (see) from inside out**.

**Here’s a key concept:** **Every time we call a function to evaluate an argument, we are creating a new function with a whole new list of available variables and other resources**. When the function ***returns,*** these list gets wiped out.

**Variable search:** For each different scope, a list called an **activation object** is created. An activation object is a list of all available variables. The activation object is saved in the **heap** allowing it to last longer than if it was in the temporary stack. This is the **chain** the *interpreter* will traverse when looking for a variable. It starts at the local scope, the inner most scope where the script is acting from; if not there, it goes one step further; if not there, it goes up higher until it reach the end of the scope environment for the script in question. The **first** variable to be found with a *given name* is the one to be used. Even if there are other variables with the same name elsewhere up the chain, the interpreter will never get there once it finds its first target.

Every function can actually be considered a *closure* since a function has access to global variables, as well as to the variables from outer functions if any (parent functions, not sibling functions). What is a closure if not the combination of a function and all the variables available in the entirety of its scope? Be sure to **return** your closure functions when no longer needed, in order for the garbage collection to do its job and save memory in the long run. Avoid [memory leaks](http://en.wikipedia.org/wiki/Memory_leak).

**Reminder:** I had mentioned earlier that when variables are assigned to a function parameter, the data is copied and it remains independent from the variable. This has nothing to do with closures since the closure “link” doesn’t happen via a function parameter. Closure functions (any function) actually keep a reference of the outer variables (all variables) because they are automatically bound to them, which means that closure functions can actually **update** the outer variables during their data process if there is an internal assignment inside the function pointing to the variable on the outer scope. So there is a difference between data passed via an argument from stack to heap, and data presented to a function by directly calling an outer variable. The first is a copy of the data; the second is only a pointer. And pointers have the power to modify data at the location they point to.

1- Here’s an example of what I mean. Try the exercises in the following picture and read the comments if you need to understand what is going on:

![](images/00046.jpeg)

Figure 46  [raw file](http://icontemp.com/joagi/scripts/38.txt).[ icontemp.com/joagi/scripts/38.txt ]

**Note:** Had the variable x inside of the function been written like this: **var x = x * num**, the **var** would had created a new scope for x which would make it a separate x from the outer x. In this case, the *outer* x would not have been affected by the calculation.

## 3.1.6 The arguments object versus inner functions

An *inner* function has access to the *outer* function ***variables*** and ***parameters***, as well as to global variables.

However, the inner function doesn’t have ***direc***t access to the outer function *arguments  **object***; **only if arguments are *specified in as* formal parameters**.

This is important to keep in mind because it can confuse you if you are not aware of it.

Now, why is the *arguments object* from a parent function invisible to an inner function?

Because the inner function also have its own *arguments object* even when it is empty.

So when we call the object *arguments*, which *arguments* are we talking about: the inner *arguments* or the outer *arguments*? When we tell an inner function to return the arguments object it returns its own which could be an empty set.

If you need to review **arguments object** versus **arguments via formalized parameters** please refer to the beginning of this chapter.

Let’s create some code in order to prove that this is so and to see how we can go around it.

1- Create a function named ***mx*** by itself and test it (get the **raw file** from the next image below).

2- Then create an **inner** function and attempt to use the outer function’s **arguments object** to see what happens. Just follow the instructions on the image itself.

**Note:** In these examples we are not calling parameter “num” directly (that would have worked); we are calling the whole *arguments object*. Let’s take a look:

![](images/00047.jpeg)

Figure 47 [raw file](http://icontemp.com/joagi/scripts/36.txt).[ icontemp.com/joagi/scripts/36.txt ]

The thing to remember in the example above is that we are trying to use the inner function to access the outer function’s arguments **object**, not the outer function formal argument such as “num” in the parentheses. The last example (lines 22 – 27) works fine because we accessed the outer arguments object from within the inner function **by binding the inner function** to the arguments object in outer function (line 24).

Remember, inner functions have access to outer function’s variables. The **formal parameter** of a function acts as **temporary variable**. However, when we attempt to access the **object arguments** itself (which is not considered a parameter), then we need to specify which object we are talking about, because the inner function also has its own arguments object and that one takes priority.

## 3.1.7 The “this” variable

Let’s peel another layer of the keyword **this**. In an earlier chapter we had mentioned that **this** is used as we would use the pronoun “*whose*”. You can think of “**this**” as a variable that points to the value of the *last object previously mentioned*, or under whose scope the script is functioning. Let’s fire up our JS console to play with “*this*” idea:

1- Create a variable **x** and a simple function that will print **x** **+ m**:

![](images/00048.jpeg)

Figure 48 [raw file](http://icontemp.com/joagi/scripts/39.txt).[ icontemp.com/joagi/scripts/39.txt ]

2- Call the function by adding 10: **y(10);** // returns 355 and all works fine since 345 + 10 = 355.

Let’s see how we could apply **this** in this context. I know it’s overkilling but please stick with me, there is a point to it. We know the variable **x** is a global variable and all global variables are properties of the object Object which in the browser is called *window*.

3- Let’s redo the function by applying the full path to the variable **x**:

![](images/00049.jpeg)

Figure 49

4- Call the function by adding 11: **y(11);** // returns 356 and it works just fine, right?

Since we can call the global variable by its name or by *binding* to the **window** object, it should also work when we bind it to “**this**” since it represents the object that owns the function, the *window object*, right?

5- Let’s modify the function again:

![](images/00050.jpeg)

Figure 50

6- Call the function by adding 20: **y(20);** // returns 365 and it works just fine. Same process!

7- Let’s perform a “*litmus test*” on this baby. **Add a variable inside the function with the same name as the outer variable**. You know from a previous reading that normally the function would ignore the outer variable and use just the internal variable if they are named the same because it is the first one it finds, right? Not in this case because we are binding the external variable making sure the script understands what we mean.
Let’s see:

![](images/00051.jpeg)

Figure 51

8- Call the function by adding 20 (same as before): **y(20);** // returns 10365 and it works just fine. It added **outer x** + m + **inner x**.

So “**this**” is just a *shortcut* referring to its *parent* object. For the most part, as long as we keep this concept in mind we will not go wrong. The reason to use “this” is ***portability***. It allows creating generic scripts that can be applied to different subjects depending on which subject is being called in at any given time. Whenever a property (a variable) is referred to without a doted prefix of the object’s name (or “**this**” in its place), it is understood that such object is firstly a local object, or secondly, a global object under which the script falls into scope.

As for “this” in our example, even if we use an inner function, (see fig below), the **this.x** still refers to the global (window) property **x**:

![](images/00052.jpeg)

Figure 52 [raw file](http://icontemp.com/joagi/scripts/43.txt).[ icontemp.com/joagi/scripts/43.txt ]

**NOTE:** This concept is simple but we should keep in mind that the variable “this” only gets assigned to the object’s name in question at the time that the object **invokes the script**. This is known as “***late binding***”. When we call the function, **this** will represent the object under which we are calling the function from. In our case it works correctly because **our function y is bound to window**. The explicit path to call the expression is actually de following: **window.y(20);** // **y(20) is just a shortcut**.

**If**, in a different object oriented context under which the script is written, we mean to call the function for an instance of another object, “**this**’ will represent the instance of the object in question, and not its prototype. However, we need to make sure we are not calling the wrong object by accident. Sometimes it is best to use methods like Call(), Bind () or  Apply () in place of ”**this**”, especially when it comes to **callback** functions because the context may change and the object need may not be pointing at the script when the function is called back. These methods will be covered soon and the concept of “**this**” will be expanded. Let’s keep peeling that onion!

## 3.1.8 Functions as Object Constructors

We can use functions to build *objects of our own*, sort of like prototypes from which we can then instantiate other replicas, using the same functionality. If functions are collections of scripts that can be called in to work together, objects are referred to as containers of functions and variables coming together to represent a common functionality (of data and behavior).

To build an **object constructor** we create a function just like any other, but since this is the prototype mold of future objects, we follow the JavaScript convention, which is to **capitalize** the first character of the constructor’s name, to visually distinguish this “*3d printer*” function from other regular functions, because its purpose is to instantiated other objects. This allows us to recognize the “*queen bee*” of all the little bees we are about to reproduce. In an illustrative way, we create a **Form pad** and then we *rip out* each page every time we create (fill in) a **new** Form.

![](images/00053.jpeg)

Figure 53

1- The basic structure of the function object constructor is this: **function JobApplication() {
  // properties go here;
}**

Since I didn’t use the variable declaration we have been using all along in this book, I don’t need the *semicolon* at the end. Please note that we are creating a brand new object constructor and not an instance of the object Object. Of course we could have used a variable declaration, but this is a more common design. Also keep in mind that it gets hoisted as a function to the top of the scope (*see* **1.6 Named Functions vs. *Anonymous*** Functions).

**JobApplication** is the name of the **function** we have created above. It is also the name of our **object prototype**.

By declaring the above function, we are creating a **template** for the job Application. Now we need to design a few text boxes inside the function in order for the form to make sense, since right now, we only have a *blank* form or an empty container.

2- Let’s ***redo*** our Job Application with one of the properties we want to get from the applicant (a job position) (see link to *raw file* below the image if you want to copy it):

![](images/00054.jpeg)

Figure 54 [raw file](http://icontemp.com/joagi/scripts/45.txt).[ icontemp.com/joagi/scripts/45.txt ]

Here we created a form that allows the applicant to insert a job position into the function when he/she fills out the form. Our first applicant arrives and we rip a form from the application pad so that he can fill it up. By ripping out a page, I mean to **create a new instance** of the application.

3- We create a new instance of the application in the following manner: **var** **tonyDeAraujo** **=** **new** **JobApplication("writer");**

A variable **tonyDeAraujo** was created and a *new* **JobApplication** was assigned to the variable, and a job position of  “writer” was passed in via the function parameter.

4- Test it in the console like this: **tonyDeAraujo;** // returns *JobApplication {position: "writer"}*.

The keyword **new**, **binds** the JobApplication **template** to the **variable** *tonyDeAraujo* with a set of *preconfigured* properties. In this case the only property available is “**position**” which reflects the position *tonyDeAraujo* has filled out in his application. How does JavaScript know whose position this is? It knows it by the generic variable **this** attached to position. “this” holds the place of the object that calls the function.

**Is tonyDeAraujo an object?**

5- Let’s test if tonyDeAraujo is an object: **typeof tonyDeAraujo;** // returns  "object".

6- Now we **start from the beginning again** and create a second version of the JobApplication form with a lot more options (practice makes perfect, right?) See the raw file:

![](images/00055.jpeg)

Figure 55 [raw file](http://icontemp.com/joagi/scripts/46.txt).[ icontemp.com/joagi/scripts/46.txt ]

Notice how “**this**” binds each property into each parameter, which means that, whatever information we introduce when we fill out another instance of the JobApplication, it will be bound to the name of the instance we create via the function parameters. Notice also the arrows showing the sequence of assignment: The data comin in via the age parameter is assigned to this.age. If for example the new object’s name is tonyDeAraujo and its age is 39, this.age becomes tonyDeAraujo.age = 39.

7- Make sure you paste the above script on the console and then let’s *recreate* the tonyDeAraujo’s application again: **var tonyDeAraujo =** **new** **JobApplication("writer", "Tony", "deAraujo", 99);**

8- Call the applicant: **tonyDeAraujo;** // returns
*JobApplication {position: "writer", firstName: "Tony", lastName: "deAraujo", age: 99}*.

9- Let’s introduce another applicant: **var lespaul =** **new** **JobApplication("guitarist", "Les", "Paul", 99);**

10- Call the applicant: **lespaul;** // returns
*JobApplication {position: "guitarist", firstName: "Les", lastName: "Paul", age: 99}*.

11- Don’t forget to introduce yourself as an applicant just for practicing.

And now it is time to create **methods** common to all applicants. We know from previous experiments with prototype, that if we mix the methods together with the property names under the **new** function constructor, we will be **duplicating** methods, which is not what we want to do. We want to create a method and then use the same method for each applicant (by reference).

In order to make these methods unique in the sense that they will only be created once and then used by all instances of JobApplication, we must create them by listing them on the **prototype property** menu. We need to create them **outside of the function** because they are only created **once**, and there is no need to recreate them each time we fill out a new application. They will always be there, ready to be acted upon by each new applicant. It is almost like saying, “*thanks for registering as a new applicant. You may now take advantage of our benefits. Here’s a list of all the benefits you now qualify for*”.

12- Let’s create a method to see how this works. Create a method called “**introduction**” that will automatically displays a message every time we *call* “introduction” on a new or existing applicant.

Here are two examples of our “introduction”:

 My name is Tony deAraujo. I'm 99 years old and I'm applying for the position of writer.

My name is Les Paul. I'm 99 years old and I'm applying for the position of guitarist.

13- **How do we do this?** We do it by creating the following **prototype** (paste the raw file or retype it manually):

![](images/00056.jpeg)

Figure 56 [raw file](http://icontemp.com/joagi/scripts/47.txt).[ icontemp.com/joagi/scripts/47.txt ]

**JobApplication.prototype.introduction** means to add to the **prototype list** menu of JobApplication, a method called **introduction**. Then, to the right, we define the method which obviously is a function. Think of prototyping as adding methods to an already existing object template so that all the instantiated objects can instantly share this functionality.

14- Now, in our example, every time we need to *introduce* an applicant, we call the function’s **introduction** method by ***binding*** the object and the method with *dot syntax*. Like this:

**tonyDeAraujo.introduction();**   
// returns
*My name is Tony deAraujo. I'm 99 years old and I'm applying for the position of writer.*

**lespaul.introduction();** // returns
*My name is Les Paul. I'm 99 years old and I'm applying for the position of guitarist*.

15- Let’s add one more method: A way to *list* a complete job application of a specific applicant.

![](images/00057.jpeg)

Figure 57 [raw file](http://icontemp.com/joagi/scripts/48.txt).[ icontemp.com/joagi/scripts/48.txt ]

16- Call the method on one of the applicants: **tonyDeAraujo.listApplicant();** // returns **Name:** Tony deAraujo, Age 99
**Job Position:** writer
*My name is Tony deAraujo. I'm 99 years old and I'm applying for the position of writer*.

We now know how powerful and convenient “**this**” can be when used in functions. We created a job application and use it for an infinite number of applicants. Hopefully you had a chance to test it with your own name and added a few more possibilities. If not, please do so to practice a bit more. Practice is the name of the game. Let’s review some key points:

· **Do you know how to declare a new method to an object prototype?** objectName.prototype.methodName =

· A method is composed of one or more functions. We attach “this” to variables instead of the object name in order to make it generic so it can be applied to any *instance*.

· Although we could create method prototypes inside of the function constructor, we choose to keep them outside in order to avoid duplication of the same method every time we instantiate a new object from the original template. *Let’s keep peeling this onion…*

# 3.2 Function Properties and Methods

## 3.2.1 apply( ) and call( )

Sometimes we want to call in an object that is not the object owning our function in the current execution environment, and since “**this**” refers to the object under which the calling script belongs to at the time of calling, it will prevent us from addressing our intended target since it is not the object currently pointing at the script. That’s when the methods **call( )** or **apply( )** become useful. These two mechanisms from the JavaScript library allow us to borough methods from other objects, without having to rewrite them again. It is like **importing** from an external source to the current execution environment and à la carte (which is the opposite of [table d'hôte](http://en.wikipedia.org/wiki/Table_d%27h%C3%B4te)).

The way I visualize call() is by keeping in mind one of the meanings of the term *call* which is “refer to”, or “consider to be”, “apply to”. The same goes for *apply()*.

**Preamble:**

The first parameter included in **call( )** *or* **apply( )** works in the same way for both methods, and it is the one we mostly frequently use, which means that for the most part, either method will work.

If however we are going to include several parameters, then *call( )* will accept individual arguments to fine tune the script, whereas apply( ) will require the second parameter to be an array of arguments. This is the difference between the two methods, individual arguments versus an array. We will see how this works in the next exercises.

Let’s look at a simple example to illustrate the concept.

In this example we have two objects as well as one *external* method with no reference to the two objects whatsoever.

The two objects we are going to create are named **MailCustomer** and **WalkInCustomer**.

Our sample method will be called **thankYouCard** and we will use it to send a *thank you note* to ***all*** our customers, regardless of their classification.

1- Create the **MailCustomer** object:

![](images/00058.jpeg)

Figure 58 [raw file for steps 1 - 4](http://icontemp.com/joagi/scripts/49.txt).[ icontemp.com/joagi/scripts/49.txt ]

2- Create the **WalkInCustomer** object:

![](images/00059.jpeg)

Figure 59

3- **Add** a person to each of these customer types:

![](images/00060.jpeg)

Figure 60

4- Create an independent **thankYouCard** method:

![](images/00061.jpeg)

Figure 61

We can**not** directly use the **thankYouCard** method with either of our customers, because the “**this**’ will be *undefined*:

![](images/00062.jpeg)

Figure 62

We could however, *use* the methods **call( )** or **apply( )** to bypass the ‘this’ from the customer’s object in order to address the targeted method.

**Using call( )**

1- Call the *thankYouCard* for each customer **by using** **call( )**:

![](images/00063.jpeg)

Figure 63

Notice that the keyword *mary* is the name of the object being targeted. So we use call as call(this_object_name), or apply this method to *this_object_name*.

Do the same for *john*:

**thankYouCard.call(john);** // returns “Hello, John! Thank you so much for your last purchase.”

**Using apply( ):**

2- Call the *thankYouCard* for each customer by using **apply( )**:

**thankYouCard.apply(john);** // Hello, John! Thank you so much for your last purchase.

3- The same thing goes for **mary**.

**As seen, when we use just one argument, both call( ) and apply( ) work identically**. The examples above are simple in an effort to peel *our first onion* on the subject.

These two methods can take more than one argument:

**call( )** takes **individual** arguments.

**apply()** takes an **array** after the very first argument.

We will use them later on other scripts. Did you notice how the console actually helps us with the syntax? Testing on the console is always a great idea before we hardwire code somewhere else.

## 3.2.2 Adding more arguments to call( ) and apply(  )

Let’s add more functionality to our thankYouCard by introducing **gender** to the greetings (such as **Dear Miss**, or **Dear Mr**.) depending on the addressee:

We are going to modify the thankYouCard to accommodate for a second argument, by adding a parameter, “***gender***”, into the function. Please spend a few moments analyzing the script, then paste into the console:

![](images/00064.jpeg)

Figure 64 [raw file](http://icontemp.com/joagi/scripts/54.txt).[ icontemp.com/joagi/scripts/54.txt ]

4- Now we can call the method thankYouCard for each one of our customers in a more formal way. As we write the script bellow, notice the difference between the current call() function, and the previous call()  function. The first parameter points to the object the method will be applied to, it represents the ‘this’, and the second parameter applies the “gender” argument parameter which acts as a placeholder :

**thankYouCard.call(mary, "Dear Miss");** // returns
 “***Dear Miss Mary!*** *Thank you so much for your last purchase*.”

**thankYouCard.call(john, "Dear Mr.");** // returns
*“**Dear Mr. John!** Thank you so much for your last purchase.”*

5- We cannot test the method **apply( )** in the same way, because it will give us an error if the second argument is not an array. **However**, we could *fake an array* and it would output just fine:

**thankYouCard.apply(john,["Dear Mr."]);** // returns
*”**Dear Mr. John!** Thank you so much for your last purchase.”*

**About the second argument:** The first argument addresses the object being targeted for processing. The second and consecutive arguments target properties of the object. By attaching the desired method to **call( )** or to **apply( )** with *dot syntax*, we are binding the method to the target object, allowing “**this**” to be addressed accordingly.

What if we want to simplify the **thankYouCard** method calling in order to be used by a non-technical person?

As an example we could simplify the calling, by creating a “**thanks**” *function* that calls the **thankYoucard** as applied to the targeted customer:

![](images/00065.jpeg)

Figure 65 [raw file](http://icontemp.com/joagi/scripts/66.txt).[ icontemp.com/joagi/scripts/66.txt ]

Now we can just instruct our helper to call the “thanks” function every time he or she needs to thank a customer by using the following syntax:

**thanks(mary,"Dear Miss");**

**thanks(john,"Dear Mr.");**

This is just a shortcut to **thankYouCard.call(mary, "Dear Miss ");** and it avoids spelling errors.

**Note:** Although john and mary look like regular names, they are object names and the script inside the method caters to the property name that belongs to the object’s this.name. Because of this, a regular “string” name will not work in its place. If you call “tony” on the thankYouCard method, it will output the name as *undefined*. However, we could call any name (string) if the internal method script is less specific, as we shall see next.

## 3.2.3 More practice with call( ), apply( ) methods.

Let’s look at a few more examples to *cement* our understanding of these important function methods.

1- The following function prints a license number based on the parameter entered, and that’s all it does. As you will see next, when we call it, we are able to *call* this function on anyone, an object or a string, by using the **call( )** method:

![](images/00066.jpeg)

Figure 66 [raw file](http://icontemp.com/joagi/scripts/63.txt).[ icontemp.com/joagi/scripts/63.txt ]

2- Call the function on a person (string value) named Tony with license 34568: **showLicense.call("Tony","34568");** // returns *“Tony has license number 34568”*.

As seen above, “**this**” is applied to the first argument of the call( ) method, and “**license**” is applied to the second argument of the call( ) method.

3- Let’s try another similar script with a third argument:

![](images/00067.jpeg)

Figure 67 [raw file](http://icontemp.com/joagi/scripts/64.txt).[ icontemp.com/joagi/scripts/64.txt ]

4- Call the function again but this time add an expiration date: **showLicense2.call("Tony","34568","January 5, 2016");** // returns *“Tony has license number 34568 expiring on January 5, 2016”*.

The *call* method will apply the first parameter to the placeholder *this* (the object named), wherever it may be on the output script, and subsequent parameters where a placeholder matches the parameter’s name.

Arguments for all the parameters can comprise of objects, strings or even **functions**. See this [external script](http://icontemp.com/joagi/scripts/63z.txt) [icontemp.com/joagi/scripts/63z.txt] for a sample where a function return result is being applied as the ‘this’ on a *call* method.

Before we move on, let’s visualize **call functions** from a different window in the hopes of bringing a better understanding to the subject matter.

Consider the following test script:

![](images/00068.jpeg)

Figure 68

· Lines 1 through 3 represent function x with one parameter, num.

· Line 5 calls the function on an argument 3 and the output result is num + 1 = 4.

· On line 7 we attempted to *bind* x to *call* and pass *num* as 3, but JavaScript assumed 3 as the first parameter, the “this”), and  a value of “nothing” as the second parameter. The second was supposed to be a number. So we’ve got a NaN error.

· On line 9 we applied window (the object under which the function **x** exists) as the first parameter, and then 3 is finally processed as the second parameter of **call( )** which becomes **num**.

This shows that **x(3)** is actually a **shortcut** for **x.call(window, 3)**. Better yet, remembering some of our first lectures, and to be more specific, x(3) is the same as:
**window.x.call(window, 3);**

In the past few exercises we’ve experimented with functions to test the method **call( )** where the object was actually a string (“Tony”), and also where the object was *window* (the default value). **In summary**, our tests show that functions don’t have a persistent awareness of “**this**”, because “this” is determined **at call time** based on who is invoking the function. This flexibility is a great asset. We could have called x like this: **x.call(“y”, 3);**. Just to make sure 3 was applied to the second parameter since the first parameter (in this case) is just for window-dressing (no pun intended).

**Which method is best, call( ) or apply( )?**

When we know upfront the arguments to be used, **call( )** is more suitable.

For an undetermined number of arguments, **apply( )** is best, since it uses an array as its second argument.

Either way, call( ) or apply( ) allows for the usage of methods that have no relationship with the object where they are being  implemented on. This opens a plethora of possibilities.

I hope this introduction to Call and Apply has inspired you to learn more about them.

**For more information please refer to the following ECMASCRIPT 5 page:**

*   [15.3.4.4 Function.prototype.call (thisArg [ , arg1 [ , arg2, … ] ] )](http://www.ecma-international.org/ecma-262/5.1/#sec-15.3.4.4)
*   [15.3.4.3 Function.prototype.apply (thisArg, argArray)](http://www.ecma-international.org/ecma-262/5.1/#sec-15.3.4.3)

Below, please find an image summarizing the concept if **this** as applied to **call( )** in different scenarios:

 ![](images/00069.jpeg)

Figure 69 SUMMARY

# PART IV – STRENGTHENING THE WARRIOR’S ARSENAL

“Any fool can know. The point is to understand.”
 *Albert Einstein*

4.1 The Math Object

The Math object is a very useful predefined and static group of mathematical methods and constants. Static means that they don’t have to be constructed, they are always present.

The Math library is not only convenient, it is a lot faster than programming manual alternatives since it is hardwired in a lower level language.

They say the JavaScript Math library is more powerful than a pocket calculator. However we need to take in consideration its precision which is limited to 16 digits. Of course this is more than enough for anything I would need.

Let’s do some lab work to get familiar with the most common methods of this library. I will leave a link to a list of all methods and properties later for your reference.

Please fire up your JavaScript console and try the following shortcuts as I explain them.

## 4.1.1 Math.random( ), floor( ), ceil( ), round( )

**Math.random( );** // returns a random number from 0 (inclusively) and 1 (exclusively). It takes its seed from the computer clock. It returns 0… 0.9999.

1- After you write  **Math.random( );** on the console and press enter,  ***arrow up*** to bring it back and try again and again until you have a clear notion on how it works.

Because **Math.random( )**  is less than 1, if we need random numbers higher than 1 we need to add a constant to the method. For example if we add 5 we get numbers from 5 (inclusively) to 6 (exclusively):

**Math.random( ) + 5;** 
// try it a few times. We get numbers such as 5.2907, etc.

Let’s suppose we want random numbers between **1 and 10**. We multiply the method result by 10 and add 1 in order to start from 1:

**Math.random( ) * 10 + 1;** // example return: 7.784083819948137

This brings me to a *related topic*. On one of my tests I got and answer of 10.575064114760607\. That’s because the 10 multiplier + 1 makes random outputs from1 to 10.999… We could remove the decimals to get a cleaner output by using another method:

**Math.floor( )** or **Math ceil( )**. The first rounds the number *down*, the second rounds them *up*.

How do we combine *Math.floor( )* with *Math.random( )*?

**We wrap the second into the first**: **Math.floor(Math.random()*10+1);** // results: rounds down to 1,7, 8, 4,10 etc

**Math.ceil(Math.random()*10+1);** // results: rounds up to 2, 8, 9, 5, 11etc.

**Human versus machine**

The following script is a simple guessing game between  a machine and a man. It could be the seed for a more sophisticated match if you want to make it better. Its purpose is to illustrate Math.random and Math.floor. When we call the function with a number (ranging from 1 to 5), it compares it to a randomized number and whichever is higher wins the round, human or computer:

![](images/00070.jpeg)

Figure 70 [raw file](http://icontemp.com/joagi/scripts/68.txt).[ icontemp.com/joagi/scripts/68.txt ]

Call the game a couple of times with a number argument from 1 to 5 like for example: **game(3);** // returns “human wins!” Or “machines wins”.

You could improve the game by giving points to lower numbers and taking points when a human uses the highest number, or preventing the usage of the highest number more than once, and many more possibilities. That of course would takes us out of this topic.

**Moving along…**

**Math.round( )**.

Since **Math.floor** always rounds down and **Math.ceil** always rounds up, we need another method to round up **or** down *based on the value given*.

For that JavaScript has **Math.round( )**. Not to confuse with *math.random()*.

**Math.round( )** rounds it up if the value >= **.**5 or down if the value is less than half.

4.1.2 Math.max( ) and Math.min( )

The **Math.max( )** returns the largest number from a list of given parameters:

**Math.max(6,9,23,57,3);** // returns 57

**Math.max(5,10);** // returns 10

**Math.max(-5,-10);** // returns -5

We could **fetch max from an array** by using **apply( )**
(remember, *apply()* takes an array as the second argument):

Code the following array **x**: **var x = [3,6,9,1];**

**Math.max.apply(null,x);** // returns 9\.

**Null** took the place of the **window** object, since *x* is an array under the *window* object and ‘this’ points to *window*. We could have written (**null**, x), (**window**, x), (**x**,x), or even (“tony”,x). The result would have been the same. The important thing to realize here is that we had to include a first parameter so that our second parameter was recognized as a second parameter and not as a “this” parameter. In case you’re wondering why “tony” is in quotes, it is because there is no variable named tony in our execution context and without quotes JS would have thrown an error. In this script we are not taking advantage of the first parameter, so anything would do. Our target is the second parameter.

The opposite of max is **min**:

**Math.min(6,9,23,57,3);** // returns 3.

**Math.min.apply(null,x);** // returns 1 ( from our previous x array)

These methods are very handy. They can replace quite a bit of code.

Take for example the **loop script** on the next figure that iterates over an array in order to choose the largest value:

![](images/00071.jpeg)

Figure 71 [raw file](http://icontemp.com/joagi/scripts/69.txt).[ icontemp.com/joagi/scripts/69.txt ]

We can simplify it by using Math.max in conjunction with apply( ). The following script replaces the above loop mechanism (lines 4 through 8), applying the **max** (or largest) to the variable **largest**:

**largest = Math.max.apply(null,*array*);** // returns 75.

We could even eliminate line 2 if we declare the variable largest at the same time we assign Math.max to it. That’s six less lines of code and a drastic reduction of possible syntax errors. Another advantage is that JavaScript library methods are written internally  in a language closer to machine which makes them much more productive in terms of execution speed.

  4.1.3 Math.pow( ), Math.sqrt( ), Math.abs( )

**Math.pow(** *base***,** *exponent* **)** returns a number based on its exponent:

**Math.pow(2,2);** // returns 4.
As of (2 x 2 = 4).

**Math.pow(2,3);** // returns 8.
As of (2 x 2 x 2 = 8).

**Math.sqrt(**num**)** returns the square root of a number:

**Math.sqrt(9);** // returns 3.

**Math.abs(**num**)** returns the absolute value of a number:

**Math.abs(-2);** // returns 2.

**Math.abs(null);** // returns 0.

## 4.1.3 Math constants, PI

**Math.pi( )** returns the constant of **3.14159**, which is the ratio of the circumference of a circle to its diameter.

An example of where **PI** could be used is when calculating the area of a circle: **var area = Math.PI * radius * radius;**

In the example above all we need to know is the radius. PI is given automatically by JavaScript.
if  **var radius = 10;** the area will be calculated to 314.159...

## 4.1.4 Useful Math Object references

· [Mozzila Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).- A full list of Math’s constants and methods.

· [Sylvester](http://sylvester.jcoglan.com/) - a math JavaScript library for vectors, matrix and geometry.

· [Accounting.js](http://jster.net/library/accounting-js) - library for number, money and currency formatting.

· [Numeral.js](http://jster.net/library/numeral-js) - currency, percentages, time, and more.

· [JSter](http://jster.net/category/math-libraries) - a catalog of front end JavaScript libraries.

This is a draft of what is coming in the near future if you are looking ahead:

[ECMAScript Language Specification 6th Edition (ECMA-262)](http://people.mozilla.org/~jorendorff/es6-draft.html#sec-math-object).

# 4.2 The Date Object

**Date();** // by itself will return today’s complete date, like for example:

"Wed May 28 2014 17:37:21 GMT-0400 (Eastern Daylight Time)"

We can also use Date**.now()**; // returns in milliseconds the date it was executed.
1401313102975.

Using the above **Date( )** returns a complete **object**, and it can be used at any time. However, contrary to the Math object which is *static* and readily available, in order to use the functionality from the Date object’s library, one needs to create an instance of the object, and then call the different methods from there.

Let’s create an instance of the object Date.

## 4.2.1 Creating a working Date object instance

We create an instance of Date with the **new** keyword.

Example:

var **sampleDate = new Date**; 
// try it on your console.

Once we have an instance of the object  **Date** we can use it as an *interface* in order to access Date methods from JavaScript library:

sampleDate**.getDate()**; // returns today’s monthly day. Example: 28, if today is the 28^(th) day of the month.

 sampleDate**.getDay()**; // returns the day of the week. *0* being Sunday and *6* being Saturday.

sampleDate**.getMonth()**; // returns the month from *0* - *11*, *0* being January.

sampleDate**.getFullYear()**; // returns the current year, like 2014.

sampleDate**.getHours()**; // returns the hour ( *0* – *23*), like 17.

sampleDate**.getMinutes()**; // returns the exact minute of the Date object. *0* – *59*.

sampleDate**.getSeconds()**; // returns the exact second of the Date object *0* – *59*.

Below you will find a *sample* script on how to use Date based on the methods we have covered so far:

![](images/00072.jpeg)

Figure 72 [raw file](http://icontemp.com/joagi/scripts/70.txt).[ icontemp.com/joagi/scripts/70.txt ]

Lines 1 - 10 represent an arbitrary function ***writeDate*** which calls each method of the Date object represented as ***myDate*** (line 4). Then it concatenates the returned data into the variable ***DisplayDate***. Notice how we added ***1*** to ***getMonth*** because JavaScriptS returns ***0* as January**. In the end we call console.log to display today’s date in all its glory. To apply it we call the function on line 12.

## 4.2.2 Converting Date to a string

There are several methods to convert a date format to string format. Let’s look at a few of the most used ones to get an idea on how to use them:

We are going to use the same **sampleDate** object we created earlier. If you are restarting the console again, please create **sampleData** as described earlier **and** below:
var **sampleDate = new Date**; 

Depending where you are located your result may be different. Here is mine: **sampleDate;** // returns " Wed May 28 2014 17:49:04 GMT-0400 (Eastern Daylight Time)".

Now we can test some of the **string conversion methods** available from the date object:

sampleDate**.toDateString()**; // returns (in my case) "Wed May 28 2014"

It grabbed the left portion of the full date displayed on the previous exercise, leaving out the time portion at the far right.

sampleDate**.toLocaleDateString()**; //returns  "5/28/2014"

It returned the same date as previously, but in a format more appropriate to my **location**.

sampleDate**.toLocaleTimeString()**; // returns "5:49:04 PM"

*toLocaleTimeString* returns the localized ***time*** portion of the date.

sampleDate**.toLocaleString()**; 
// returns "5/28/2014 5:49:04 PM"

*toLocaleString* is a combination of *toLocaleDateString* and *toLocaleTimeString*.

sampleDate**.toUTCString()**; // returns "Wed, 28 May 2014 21:49:04 GMT"

*toUTCSString* returns a string, according to **universal time**.

sampleDate**.toJSON()**; // returns " "2014-05-28T21:49:04.498Z"

*toJSON* returns a string in the **JSON format**. W

## 4.2.3 Useful JavaScript date libraries

JavaScript date libraries allow us to add date and time picker functionality to our applications by manipulating, parsing and formatting dates.

*   [Later.js](http://bunkat.github.io/later/) - Easily define complex schedules then quickly calculate future or previous schedule occurrences. Works in Node and in the browser.
*   [Countdown.js](http://countdownjs.org/) - A simple JavaScript API for producing an accurate, intuitive description of the timespan between two Date instances.
*   [Moment.js](http://momentjs.com/) - This library can easily convert any given date to many different formats, add/subtract dates, hours, and has methods for displaying user-friendly date/times like “in 5 days”, in a multi-language environment.
*   [Cubism.js](http://square.github.io/cubism/) - Is a JavaScript visualization library for HTML and SVG, to display time series in real-time.
*   [XDate](http://arshaw.com/xdate/) – Is a thin wrapper around JavaScript's native Date object that provides enhanced functionality for parsing, formatting, and manipulating dates. It implements the same methods as the native Date, so it should seem very familiar.

# PART V – DEFEATING THE DRAGON

“Great things are not done by impulse,
but by a series of small things brought together.” *Van Gogh*

# 5.1 Unordered Lists as Objects

We’ve seen earlier on 2.2 The Array Object in JavaScript how **array** objects are numerically *ordered* lists. In JavaScript when we see the *square* brackets we know it is an array of some sort:

**var x = [77, 34, 23, "book"];**

We also know how, in arrays, every item is ordered starting from location 0 and up. In our example, the first location (at zero) contains item 77\. The fourth location, which is in position 3, contains a string named “book”.

We can also recall seeing something like the following script:

**var y = {"Fruits": "apple", "Vegetables": "spinach", "Grains": "beans"};**

The above script represents an **unordered list**. In JavaScript, **unordered lists** are not part of the *array family*, they stand on their own as objects of their own right. They are represented by **key-value pairs**.

Because we can fetch the items by their **key label**, they don’t need to be *ordered* in any particular sequence, and this gives them a different flexibility than arrays.

So, in summary, we use square brackets **[ ]** to declare numeric ordered arrays,
and curly braces **{ }** to declare objects with key-value pairs.

In arrays we call in an item this way: **x[2];**  // returns 23
which is the 3^(rd) element from our example above.

In object notation we call an item in this way: **y.Fruits;** // returns “apple”.

We could also call an object key label with *bracket notation* just like we do with arrays:

**y["Fruits"];** //  returns "apple ". Make sure you include the key **in quotes** for bracket notation.

**Bracket notation** is good to keep in mind *because* if you ever use a number as a *key* in a **key-value pair**, you can’t call it or add it with **dot.syntax**, like this **y.12="foo"**;. We need to add or call it like this:

**y[12] = "foo";**

Printing y: **y;** // returns Object {**12: "foo"**, Fruits: "apple", Vegetables: "spinach", Grains: "beans"}

Also calling y 12: y[12]; // returns 12: "foo". (Contrary to *keys as strings* which require quotes when referring to them in bracket notation, numbers as keys work either way, quotes or not).

**Lab Work:**

1- **Let’s create the object again**.

This time we add each different item in a separate line. This is a common method of creating more complex objects because it is visually more appealing and less prone to error than the above example, albeit the same. (copy from  the raw file if you so desire):

![](images/00073.jpeg)

Figure 73 [raw file](http://icontemp.com/joagi/scripts/71.txt).[ icontemp.com/joagi/scripts/71.txt ]

Creating an object in this manner such as the one above, works well if we don’t have intentions of *instantiating* other objects based on the same *template*. If we have intentions of using this object as a prototype for other objects, then it is best to create the object through a function with parameters just like we created the *JobApplication Form* on the subchapter 3.1.8 Functions as Object Constructors. We will go over it again soon.

There are many ways to create objects. Mentioning all of these ways is a source of unnecessary confusion and it can actually slow the learning process as well as the gaining of practical experience. Do not overload yourself. Here, less is actually more!

2- If you haven’t done so, please **paste the above object** ***y*** on your *Javascript Console* in order to test a few important concepts before we build anything more detailed.

3- Print the object: **y;** // returns Object {Fruits: "apple", Vegetables: "spinach", Grains: "beans"}

3- Print Fruits: **y.Fruits;** // returns "apple"

**Here’s a silly story:**  “apple” is my favorite fruit. However anyone can come to my computer and change my favorite fruit to “lemon” while I’m not looking.

4- (try it): **y.Fruits = "lemon";**

Then one day another friend comes to visit me and I’m showing him how my JavaScript object can remember my favorite fruit,

5- and when I type fruits... **y.Fruits;** // I get “lemon”!!!

Since I didn’t appreciate the joke ( *I have no sense of humor!*), I decided to play a joke of my own by “**locking**” *my favorites* in place so no one could accidentally change them.

**How would I lock my properties?**

Well, do you remember how scope is based on functions?
See the chapter **3.1.5 Lexical** Scope if you want to brush up on that.

We could create the object via a function, like we did for the *JobApplication*, and include our properties as variables with the prefix **var** which makes them private, right?

6- Redo the following object **y** by using a **function constructor**. Copy the **raw file** if you don’t want to retype it:

![](images/00074.jpeg)

Figure 74 [raw file](http://icontemp.com/joagi/scripts/72.txt).[ icontemp.com/joagi/scripts/72.txt ]

Now if we print object **y** we get a copy of the above image. Our favorite fruits, vegetables and grains are there, but we can’t read them nor edit them directly because we have no access to the function variables.

Try **y.Fruits;** // returns *undefined*

We have made our object properties private; too private for our own sake! We want **[encapsulation](http://en.wikipedia.org/wiki/Encapsulation_%28object-oriented_programming%29)** but we don’t want to feel claustrophobic.

Since our object is now **encapsulated** (remember this term), we need to create a method to read our properties from the outside.

**How do we expose the data of a private variable from inside of a function?**

We expose a *var scoped property* by creating an **inner function** that returns the data. We have done it before, remember? Do you remember *closures*, and the balloon with two strings? Inner functions have access to the outer function data and can use it or display it to the outside world acting as agents like [tellers](http://en.wikipedia.org/wiki/Bank_teller) in a bank.

## 5.1.2 Accessor methods

Study the **inner function** on line 6 below, and read the comments afterwards:

![](images/00075.jpeg)

Figure 75 (for raw file see next)

The above script makes sense. We create a method arbitrarily called **getFruit**, which returns our property **Fruits**. However there are a couple of problems with it:

a) Because **y** is a constructor, we cannot call its methods in its current form because an object constructor is just the **blueprint** of the object. It reminds me of the **Date Object**. We need to *instantiate* an object in order to use its methods. Also, although it is not mandatory, by convention I should have capitalized **y** but I don’t want this to take us away from our real topics: ***a***) and ***b***).

b) Once we *instantiate* a ***new*** *object* we need to make sure that the method *getFruit* is applied to it (**this** new object), and not to any other object. So we need to add a ***this*** prefix as a *placeholder* to the method inside the constructor. Like **this.getfruit =** .

8- Add a ***this*** to **getFruit**:

![](images/00076.jpeg)

Figure 76 [raw file](http://icontemp.com/joagi/scripts/74.txt).[ icontemp.com/joagi/scripts/74.txt ]

In the script above we have addressed problem (***b***). To address problem (***a***) we need to instantiate a *new object*.

9- Let’s instantiate an object from ***y*** called ***myOb*** (or whatever name you wish): **var myOb = new y();**

10- Now we can finally call *getFruit* from *myOb*: **myOb.getFruit();** // returns "apple".

**Summary:**

When we create an object, its properties are public, which makes it easier to *read* and *write* properties. However, we can protect our object properties by initiating them with the prefix **var**. Once we protect the object’s properties, the only way to *fetch* data from them is through an **inner function** also known as an **Accessor method** (because it is allowed to access the property). It is conventional, although not mandatory, to name these Accessor methods **get**Something (“something” being the name of the property) because they are popularly called “**getters**” methods. *Just a good habit to form*!

## 5.1.3 Mutation methods

What if we want to mutate (modify) one of the properties inside of our *protected* object?

Before we made the decision to protect our object properties, we also were able to **assign** a **new value** to any of the object properties (the variables), like
object**.property = "otherValue";**

Now that our properties are tagged with ***var*** as well as being inside of a **function** (*an object property is always inside of a function*), we can’t modify them directly from the outside because they are invisible to an external bracket syntax approach. The only way to edit a private property is via an internal method that does it for us. A kind of [surrogacy](http://en.wikipedia.org/wiki/Surrogacy) arrangement:

11- **Create a second method** that *sets* the property **Fruits** to a different fruit, if you ever want to modify it:

![](images/00077.jpeg)

Figure 77 [raw file](http://icontemp.com/joagi/scripts/75.txt).[ icontemp.com/joagi/scripts/75.txt ]

The **setFruit** method takes an argument as input via the parameter **myFruit** (arbitrary name), and assigns the property **Fruits** to a *new value*.

12- Now that we have modified the object, make sure you **reset** the **previously instantiated** object **myOb** since it is still pointing at the old **y** object (in our case you may have to declare it again):
**myOb = new y();**

13- Next, let’s modify the **Fruits** value from “**apple**” to “**banana**”: **myOb.setFruit("banana");**

14- Print the **Fruits** property of **myOb**: **myOb.getFruit();** // returns "banana".

Just to be sure we understand, when we call ***myOb*** to the console, the only *items* we see from the object are the *public* methods. Because of var, all data is hidden: **myOb;** // returns y {getFruit: function, setFruit: function}

**Finish the object:** *(your turn!)*

*Try* adding getters and setters for the two other properties: **Vegetables** and **Grains**. Don’t forget to reset ***myOb*** or any other previously created object so that you can test your code. In the console you may have to re-declare *myOb* again.

When you are finished or if you need to peek, you can check my own result [here](http://icontemp.com/joagi/scripts/75a.txt). [ icontemp.com/joagi/scripts/75a.txt ]

## 5.1.4 Practice and review: Create a Loan Application Object

![](images/00078.jpeg)

Figure 78

In this code *drill* we are going to design a *fictitious* loan application in order to review some of the key elements we have covered so far in this chapter.

· Object name: ***LoanApp***.

· Application input properties: ***personName***, ***income***, ***loanAmount***.

· Private properties: ***bankBranch***, ***approvalStatus***.

· Public methods: ***submit***.

a) A person will fill up the loan application by declaring his/her name, income and loan amount desired. This is a simple app: income is merely a number to allow us a basic calculation. No details needed.

b) There will be a method (**submit**) that calculates the ratio between the person’s (**income**) and loan requested (**loanAmount**), a simple division. If the person’s income is at least twice the amount of the loan applied for, the loan will be approved *instantly* and a message will be sent as follows: "*Congratulations! Your application for a loan of*  " + **lanAmount** + " *has been approved.*" Also, at the same time, variable (**approvalStatus**) will change from "*invalid*" to "*Approved*".

**Else**, if the person’s income is less than the automatic qualification, the person will receive a message as follows: "*Thanks for submitting a loan application. We will contact you shortly.*" Also, at the same time, variable (**approvalStatus**) will change from "*invalid*" to "*On review*".

That is it for now. We will improve the script after we get a working object.

You can follow my directions or if you wish, do it at your own pace and just check the results later. I will make some comments as I go along. It might be best to follow through and then redo it again on your own.

I am going to start by first creating part (**b**) by itself so that I can **test it**. Part (b) is the method that submits and approves the loan application.

Then I will create the *object* and copy (as well as adapt) my ***submit method*** to the *object*. (A link to the raw file is available on step **3**).

If you need an online editor as a scratch pad there is an interesting one here: [editpad.org](http://www.editpad.org/).

1- First I declare a variable **approvalStatus** and set it to **"invalid"**:

**var approvalStatus = "invalid";** // invalid is just a string of my choice, not a keyword.

2- Then, create a ***testing* function** named **submit** with these two parameters: **income** and **loanAmount**.

These parameters will not be in the final project because they will be included on the object constructor itself, but for now, I need them here in order to test the method *submit*:

**var submit = function(income, loanAmount){ };**

3- In the body of the function I need a *conditional statement* to qualify the applicant and also to send him/her a message accordingly.

If income is at least twice of the amount of the loan requested, the loan will be immediately approved, the outer variable **approvalStatus** will be set to "**Approved**", and a status message will be sent, *else*, **approvalStatus** will be set to "**On review**" and a different message will be sent:

**if(income/loanAmount >= 2){**  //this will calculate the ratio of income to loan.  **approvalStatus = "Approved";
console.log(“**see script for the message**”);
} else {
approvalStatus = "On review";
console.log(“**see script for the message**”);
}**

**Please find the** **raw file** **[here](http://icontemp.com/joagi/scripts/pre1.txt)**. [ icontemp.com/joagi/scripts/pre1.txt ]

4- Paste the script to the ***console*** and test the function **submit** by using different ratios between *income* and *loanAmount*: **submit(5000, 1000);** // returns "*Congratulations! Your application for a loan of 1000 has been approved*".

**approvalStatus;** // returns "*Approved*".

5- So far so good! Now I will test it with a lower income: **submit(1500, 1000);** // returns "*Thanks for submitting a loan application. We will contact you shortly.*"

**approvalStatus;** // returns "*On review*".

Great, our method is working!

Now it is time to create our object construct, **LoanApp**.

**This is a summary of what we will be doing next:**

In the *LoanApp* object constructor,  **personName**, **income**, and **loanAmount** will be programmed as **input parameters**. These parameters will take arguments from any *new object* LoanApp application when being instantiated.

Inside of the body, we are going to take advantage of the ***this*** placeholder, in order to make the object portable (*instantiable*).

Also, two private variables will be declared: **bankBranch** and **approvalStatus**.

Then, the function **submit** will be copied into the object but we need to remove the parameters from our current submit function because they are not need anymore. (the raw file link is on step 5).

**Let’s do it:**

1- Declare the object constructor:

**function LoanApp(personName, income, loanAmount){**

2- In separate lines, include the properties listed on the function parameters. Don’t forget to apply the **this** to each one of them:

**this.personName = personName;**

**this.income = income;**

**this.loanAmount = loanAmount;**

3- Declare a private property named **bankBranch** and assign it a location:

**var bankBranch = "New York";** // we will look into this later

4- Declare a private property named **approvalStatus** and assign it the string value "invalid":

**var approvalStatus = "invalid";**

5- Finally copy the method **submit**, but make sure you prefix it with ***this***, so it can be applied to each different object instantiation:

**this.submit = function(){** etc...
// find the whole script up to step 5 on this  **[raw file](http://icontemp.com/joagi/scripts/pre2.txt)**.
[ icontemp.com/joagi/scripts/pre2.txt ]

6- Testing: Paste the object script on the console to see if it passes validation. Correct any errors. Take a look at the raw file from the previous step if needed.

7- Instantiate an object. My object will be *tony* with an income of 5000 and a loan request of 1000:

**var tony = new LoanApp("Tony",5000,1000);** // it passed!!

8- Call the object tony: **tony;** // returns *LoanApp {personName: "Tony", income: 5000, loanAmount: 1000, submit: function}*

9- **Submit** tony’s application: **tony.submit();** // returns "*Congratulations! Your application for a loan of 1000 has been approved.*"

10- Call tony’s **approvalStatus**: **tony.approvalStatus;** // returns undefined ("*Houston, we have a problem!*")

As you see, we can’t fetch **approvalStatus** because we have made it a private property. The only way to read the data from a private property is by creating an intermediary reading method, a **getter**, do you remember?

11- Let’s modify our object construct to include a **getApprovalStatus** method. Try to do it on your own then look at the **[new raw file](http://icontemp.com/joagi/scripts/pre3.txt)** if needed.
[ icontemp.com/joagi/scripts/pre3.txt ]

12-  Paste the new object construct on the console and **reset** the object tony by re-instantiating it:

**var tony = new LoanApp("Tony",5000,1000);**

13-  Get tony’s approve status:

**tony.getApprovalStatus();** // still returns “invalid” (***why?***)

The result was “invalid” because it hasn’t been changed from its original status. We have not yet **submitted** the application.

14- Let’s submit the application:

**tony.submit();** // returns "*Congratulations! Your application for a loan of 1000 has been approved.*"

15- Verify if tony’s approval status has actually changed:

**tony.getApprovalStatus();** // returns "**Approved**".

***One more thing….***

We have not yet tested the “**else**” on the submit method. We need to test it to make sure that it actually works.

16- Create another application for Mary as *mary*. Her income is also 5000 but she wants a bigger loan for 3000 which will delay her approval:

**var mary = new LoanApp("Mary",5000,3000);**

17-  Submit her application:

**mary.submit();** // returns "*Thanks for submitting a loan application. We will contact you shortly.* "

18- Some time has passed and Mary wants to check her approval status:

**mary.getApprovalStatus();** // returns "*On review*".

Great!!!!

Let’s peel this onion a bit more. ***What if*** we wanted to submit the application and get an immediate *status change* at the time we instantiate a new object?

## 5.1.5 How to automatically evaluate and call a method

**This is a function:**

**function ( ) { } ;**

**This is a function that calls itself:**

**function () {}();**

The last pair of parentheses to the right trigger the function to call itself.

The function *as* written above will work just fine. It will call itself when the program starts. However, it is visually more explicit to tell another programmer that such function will call itself, if we also *enclose* the whole function (before calling) in parentheses.

Like this:

** (function( ){ })();** 

// returns function ( ) { }

**Going back** to our **LoanApp** object, we could implement this technic on the **submit** method. This will make the method to run as soon as we instantiate a new LoanApp, which will print the status *message* and update the **approvalStatus** private variable.

The following image shows where the extra parentheses will go, and a raw file for the whole script is also available:

![](images/00079.jpeg)

Figure 79 [raw file](http://icontemp.com/joagi/scripts/pre4.txt) (complete). [ icontemp.com/joagi/scripts/pre4.txt ]

1- Paste the new object constructor on the console and **reset** the object tony from the last exercise, by re-instantiating it:

**var tony = new LoanApp("Tony",5000,1000);**

You should be able to see the approval message immediately after you instantiate the new applicant tony. There is no need to manually submit the application as an extra step since the submit function is called in automatically as soon as you instantiate an object.

2- Test the approvalStatus variable by calling in its *get* method, to see if that was also changed automatically:

**tony.getApprovalStatus();** // returns "**Approved**".

Congratulations! If you feel a bit confused it is because we have covered a huge territory. As long as you understand what is happening, you can proceed to the next step. If you still need to mend a few concepts here and there, it may be a good idea to review this chapter now since you have a broader view of what is being covered. *Repetition* is the secret to learn JavaScript.

## 5.1.6 Prototyping new methods

What if we want to add a new method to our *LoanApp* object?

We could go *into* the object and *hardwire* the method like we did when we first created *LoanApp*. However, many times this is not a convenient way to do it. Also, it is not a memory efficient implementation because, if you recall from previous chapters, every time we instantiate a *new* object, the constructor copies all the data which, when it comes to methods, it is totally unnecessarily.

We could instead, just *point* the new instance object to the original method, and use it when needed.

It is best practice then, to add methods as separate prototype links. However, if you prefer to encapsulate them inside the object as opposed to have them separate, there are ways to do it and we will cover one of such implementations soon, once we finish covering the proper way of doing it.

**Question:** Based on what was written above about memory efficiency, why did we include the methods **submit** and **getApprovalStatus** inside the object **LoanApp**, and not outside? Isn’t this a bad practice? Yes, it seems to be. The reason why we did it this way was because we are using these methods as **getters** to access private data. We can’t get private information by using outside methods. We always attempt to code the most efficient way possible. Right now this is what we can do with our LoanApp.

For the most part however, newly added methods will be created separately.

**Let’s add a new method to our** **LoanApp** **just for practicing purposes**.

Our boss comes in one day and asks us if there is a way to get a **summary** of each individual applicant from the **LoanApp**. We reply that there isn’t one yet, but we could implement such method in less than 5 minutes. She approves it, and we go back to the drawing board.

Do you still remember the syntax from an earlier chapter? Let me remind you: we add a new method name to the object prototype *menu*, in other words, we *prototype it*.

1- Create a prototype method named **summary** that returns an applicant’s name and the loan he/she is applying for, see raw file on step 4 (**[raw file](http://icontemp.com/joagi/scripts/pre5.txt)**). [ icontemp.com/joagi/scripts/pre5.txt ]  **LoanApp.prototype.summary = function(){**

2- In the body of the function write the following: **console.log(this.personName + " is applying for a loan of " + this.loanAmount);**

3- Don’t forget to close the function: **}**

Let’s test it before we show it to our boss:

4- Paste the **LoanApp** to the console: see (**[raw file](http://icontemp.com/joagi/scripts/pre4.txt)**). [ icontemp.com/joagi/scripts/pre4.txt ]

5- Paste the **summary** method afterwards. ([raw file](http://icontemp.com/joagi/scripts/pre5.txt)). [ icontemp.com/joagi/scripts/pre5.txt ]

6- Instantiate a new applicant:

**var tony = new LoanApp("Tony", 5000, 1000);**

7- Test the new method:

**tony.summary();** // returns "Tony is applying for a loan of 1000".

Go ahead and show it to your boss!

We had previously covered method prototyping earlier when we created a job application. It may be a good time to review that section because it might make more sense now.

Here’s the link: *3.1.8 Functions as Object Constructors*.

## 5.1.7 Objects that inherit from other objects

Sometimes we want to create an object with a certain functionality that already exists in another object. JavaScript allows us to inherit functionality from other objects avoiding repetition.

There are several ways to implement such inheritance, each one of them with its quirks. I will cover the ones I believe to be best practices. Let’s do discuss them as by creating a new application:

The branch manager from Los Angeles calls the programmer in New York and praises him for the work he did with the LoanApp. They want to be able to access an application from Los Angeles under their own branch name, and they wanted to be sure the app is independent from the New York application in case they decide to add more functionality to it. The Los Angeles branch also wanted an additional method to print the branch location since they noticed the existing application does not provide such information to the public.

We decided to reuse the object *LoanApp* to save time and resources by just making a few changes to the new object constructor as follows:

*   New application name is **LoanApp2**.
*   *bankBranch* is **Los Angeles**.
*   The additional method is **getBankBranch**.

We are going to use a technique called object **masquerading**.

![](images/00080.jpeg)

Figure 80 (raw file on next picture).

Let’s do it!

1- New object declaration:

**function LoanApp2(personName, income, loanAmount){**

2- Assign **inheritance** from **LoanApp** to **LoanApp2**, via a temporary variable **x** ( I have chosen **x** to make this clear: the name does not matter but in real life this variable should have a more illustrative name):

**this.x = LoanApp;** // here x inherits all of LoanApp.

3- Next choose which properties will need to inherit methods from LoanApp, using **x** as a conduit:

**this.x(personName, income, loanAmount);**

The inheritance has been established, JavaScript has taken note, and we don’t need the *temp* variable **x** anymore because we want to have a “disconnect” from one object to the other. Do you remember the kite held by boy and girl? and closures? Now that JavaScript knows *loanApp2* has a connection with the properties and methods of  *loanApp*, we can safely “return” or delete *loanApp* and still keep the goodies to be used on loanApp2\.

Here we introduce a new keyword: **delete**. The delete operator removes a property from an object. The syntax is *delete object.property*, delete does not affect regular variables or functions, just objects.

4- Delete x:

**delete this.x;**

Now we can add newer functionality. The reason to do it *after* we deleted **x** is to prevent any overwriting from loanApp1 to loanApp2 when we first introduced inheritance:

5- Add the new branch name:

**var bankBranch = "Los Ageles";**

6- Add a new method to return the branch name by a client:

**this.getBankBranch = function() {
 return bankBranch;
};**

7- Close the object LoanApp2:

**}** // (see image and link to raw file below).

![](images/00081.jpeg)

Figure 81 [raw file](http://icontemp.com/joagi/scripts/pre6.txt). [ icontemp.com/joagi/scripts/pre6.txt ]

 **Let’s test our object inheritance:**

8- Paste the original **LoanApp** in the console (**[raw file](http://icontemp.com/joagi/scripts/pre4.txt)**). [ icontemp.com/joagi/scripts/pre4.txt ]

9- Paste the **summary** prototype method (for later usage). (**[raw file](http://icontemp.com/joagi/scripts/pre5.txt)**). [ icontemp.com/joagi/scripts/pre5.txt ]

10- Paste the new object **LoanApp2** in the console (**[raw file](http://icontemp.com/joagi/scripts/pre6.txt)**). [ icontemp.com/joagi/scripts/pre6.txt ]

11- Create a user for the Los Angeles **LoanApp2** (old Tony is just fine):

**var tony = new LoanApp2("Tony", 5000, 1000);**

12-  Test the new method getBankBranch:

**tony.getBankBranch();** // returns *Los Angeles*.

13- Test the methods *inherited* from the New York object:

**tony.getApprovalStatus();** // returns “*Approved*”.

Now let’s use another new operator: **instanceof**. This operator comes handy to verify where an object comes from:

**tony instanceof LoanApp2;** //? returns *true*.

**tony instanceof LoanApp;** // returns *false*. (tony if from Los Angeles)

**LoanApp2 instanceof LoanApp;** // returns *false*. (LoanApp2 is not an instance of LoanApp even though it inherits its functionality and then is adds some more of its own. LoanApp is a constructor.)

14- If you pasted the *external method* on **step 9**, you also have the added prototype method **summary**. Let’s test it:

**tony.summary();** // returns "TypeError: Object #<LoanApp2> has no method 'summary'"

Ooops! That’s the “*drawback*” of using **masquerading** to inherit from other objects because the new constructor is pointing at its own prototype list, not at the list from its ancestor’s constructor. This is no problem if you don’t have external prototyped methods. However, if you do have them or plan to have them, then you need to add another line of scripting in order to access prototyped based methods from the older constructor. A proper interface need to be implemented. We need to link the LoanApp’s prototype list to LoanApp2\. Then your object inheritance **will work perfectly**:

Just like when we create an external prototype method, create an external *prototype chain* that links all the prototype methods from **LoanApp** to **LoanApp2** . Follow step 15:

15- Paste the following script into the console. It will be immediately available to new applicants. However we need to reset all existing applicants:

**LoanApp2.prototype = new LoanApp();**

16-  Now we can instantiate an applicant:

**var tony = new LoanApp2("Tony",5000,1000);**

17- Test if **summary** works:

**tony.summary();**

// returns "*Tony is applying for a loan of 1000*".

“***We have lift off!!***”.

**Question:** What would happen if we now declared LoanApp as null? Remember the kite being held by a boy and a girl? If we declare the old constructor as null, the new constructor still holds the inherited functionality. However, because LoanApp is no longer available, variable x will not function and therefore, we can’t instantiate new applicants!

In other words, in order for loanApp2 to function with its 100% capabilities, both loanApp and loanApp2 need to coexist. It’s like saying that we need an internet service in order to visit Amazon and download a [new eBook](http://www.amazon.com/Tony-de-Araujo/e/B00D7V08WY/) from Tony de Araujo (*sorry, couldn’t help myself!*).

**Summary:** *Masquerading* an existing object as a new object, is a great way to delegate functionality avoiding code repetition. One needs to make sure that the prototype chain is linked to the new object constructor if methods created under the prototype mechanism exist in the object to be inherited from. The Los Angeles branch manager is now a very happy person and so are we!

We have looked at object creation, unordered lists to be exact. We’ve seen how **encapsulation** makes code more functional, and we have pondered on how inheritance can save memory and development time by chaining objects together. These are two important concepts in the JavaScript *object paradigm* and they are all used frequently.

Before we leave this subject there is another topic of great importance about encapsulation:

**How can we include object methods inside of the constructor without creating duplication which may overload the memory? So far we have included prototype methods as external scripts, which is a recommended practice. However it is possible to include them inside of the constructor and at the same time avoid duplication. Let’s look into a way of achieving such endeavor in the next topic**.

5.1.8 How to include prototype methods inside a constructor

Sometimes we just want to have *properties* and *methods* together for whatever reason, even if it is to look like *some other language*! Not that there is anything wrong with the way we have done it so far, and it is the recommended way; but I’m including the other option here, in case you are interested on knowing about it. And even if you are going to use it, this explanation will open new doors of understanding on how JavaScript ‘thinks’.

Let’s create a simple object to illustrate how to include methods inside of the constructor in ways that do not overload the memory (the other alternative is to prototype them externally like we have done before).

This object will be called **Player** and it contains two properties: name and instrument. Then we create a method to display a **summary** about the player. Simple enough, right?

1- **Create Player and paste it into the console**:

![](images/00082.jpeg)

Figure 82 [raw file](http://icontemp.com/joagi/scripts/79.txt). [ icontemp.com/joagi/scripts/79.txt ]

2- Instantiate a player:

**var jc = new Player("Coltrane", "saxophone");**

3- Call jc:

**jc;** // returns Player {name: "Coltrane", instrument: "saxophone", summary: function}.

4- All elements seem to be there. Let’s test the method **summary**:

**jc.summary();** // returns "*Coltrane  plays the saxophone*".

The object is working fine. So why would we want to change it?

If this object was going to stand alone I would leave it like it is. However, this is not just an object; this is a **constructor**, which means that we are going to instantiate many objects from it.

Since we are going to instantiate other objects, I’m concerned with *memory management*.

In order not to duplicate the object methods each time we create a new instance of the object, we need to place the methods outside of the object, ***or*** inside but wrapped around a script that checks if the methods have already been *instantiated* by another *instance*. If the methods have already been instantiated, then there is no need to duplicate them, because they are instantly available to future instances within the same code implementation being executed. The first implementation is all we need.

**Preamble.**

The **typeof** operator in JavaScript allows you to probe the data type of its operand, or even to see if the data is **undefined**. It is this last one that we need to get.

Conventionally, an underscore before a variable name, means that such variable or keyword is for internal use. This of course is only to elucidate another developer that may come by and peek at our script (like ourselves 6 months later since months later we will not remember what we did earlier, not even tomorrow!).

We are going to make a *magic pass* at our object. We ask the program to proceed forward only if a certain variable does not exist. We do this **by implicitly asking the object if “x variable” is undefined**. But of course it is undefined because it is the first time we mention such variable. Then we code our methods, and finally we set the variable to **true**, making it **defined**. By being *defined*, the *next* time we instantiate an object within the same executable environment will have a different outcome since the variable in question will be **true** and therefore, the *undefined* will be **false**, and so JavaScript will jump over the method creation, not duplicating the methods.

It’s a mouthful! Let’s see how this works in practice:

5- Add the following if statement to the object just before the method(s). We are asking if a variable named _xyz exists:

**if (typeof Player._xyz === "undefined"){**

Now we include our methods and then we set **_xyz** to **true** and close the **if** statement ( I will explain it again with an illustration).

**However**, we can’t just write this.summary = function,  etc. This will not work. We need to send the method to the *prototype chain* in order to be part of the menu available for all objects to be instantiated, not just the original. We’ve done it before outside of the constructor, and we can also do it inside of the construct.

See the next image for details and also the *raw file*:

![](images/00083.jpeg)

Figure 83 [raw file](http://icontemp.com/joagi/scripts/80b.txt). [ icontemp.com/joagi/scripts/80b.txt ]

On line 5 we included a **_xyz** (arbitrarily uniquely named variable) which was *undefined* to begin with, and which allowed the method to be implemented. Then on line 10 we made _xyz **true** which will prevent the next object instance from recopying the method(s). Of course the properties themselves will always be different so we don’t have to worry about those.

1- Test the object instance again to be sure it is working:

**var jc = new Player("Coltrane", "saxophone");**

**jc;** // returns Player {name: "Coltrane", instrument: "saxophone", summary: function}.

We can’t really see any difference between this implementation and the original, but if you are going to encapsulate your methods along with the constructor, this is a better way of doing it because it prevents methods from overloading the memory. In the end, as you know, the best technique is to code your prototyped methods *outside of* the constructor.

Note: At this time, knowing what we now know and if you need some more practice, you  could go back to 5.1.4 Practice and review: Create a Loan Application Object and redo it so that each method gets declared only once per execution context.

# Conclusion

We could go on and on because JavaScript is as large as the Atlantic Ocean and we are just at the Jersey Shore (my hometown), but I believe we have traveled far and our journey is well on the way to enlightenment... Well, if you’re like me you know that such nirvana keeps moving forward and it is by its own nature untouchable. The more we become aware, the more we realize how much we still don’t know.

This is probably the right time to review some of the concepts covered in the book. Do not get distracted searching the internet because you will get lost and you will get confused. Most of what is written on the internet is a copy of a copy of a copy and as you know garbage in, garbage out.

Don’t take me wrong, there is a lot of goodness online and I have learned my share from it which I’m thankful. But there is great danger and I have wasted so much time trying to understand the understandable because copying is not teaching. Teaching is explaining and giving room for the reader to think and come to his or her own conclusions. Sometimes we have to tell a story and let the reader put the pieces of the puzzle together. Telling a story is a way to convey information without forcing anyone to memorize what they don’t understand. I’m a great fan of metaphors. They expand our horizons exponentially.

You have come a long way and I am proud of you because you have endured my writing and arrived at the end of the book. The end is just the beginning, right?

As a mental review, here is what you have covered:

*   Memory concepts. Stack versus Heap.
*   The value of reference types.
*   Everything in JavaScript comes from objects.
*   You have become good friends with the JavaScript Console.
*   You have played with functions and they also became your friends.
*   The untouchable Object. Pointers, primitives, object wrapping.
*   Execution context, scope, private variables, this, the role of functions in privacy.
*   Native objects, hosted objects, user objects.
*   Anonymous functions, closures, call functions, apply.
*   String objects, Arrays, new methods of interaction.
*   Arguments, nested functions, Lexical scope.
*   Functions as object constructors.
*   Math, Date constructs. Libraries.
*   Unordered lists, inheritance, encapsulation.

We could have continued on, but what good is a 400 page book if it goes unread?

It is best then to stop and think about what has been covered because if you know this much, then you know quite a lot and everything else will be easier to grasp.

With this knowledge you can go into more specialized books without getting lost as easily because you have acquired some powerful concepts.

This book can also be used as a reference when you need to clear up your mind about some method that is giving you problems and you just don’t see why.

I am planning to keep on improving the book, by reading it, editing it, adding to it, and always, thinking of you and what you would like to find in this writing.

It has truly been an honor and a very exciting experience writing this book.

Thank you so much!

Tony de Araujo

*Edited last on May 29^(th), 2014*

  One More Thing…

Thanks for reading and investing your time doing the exercises! If you have enjoyed this eBook or found it useful in any way, I’d be very grateful if you'd post a short review on Amazon. It really makes a difference to myself and to others looking for ideas about this subject.

If you would like to leave a review please go to my [Amazon profile](http://www.amazon.com/Tony-de-Araujo/e/B00D7V08WY/) and click on the book from there.

Thank you again for your support!

Tony de Araujo

New Jersey, November 2013 | May 2014 | January 2015

# APPENDIX

## Other eBooks from the author

( As of January 2015 )

1.  [JavaScript in Plain Language - A Self-Study Method: JSON and AngularJS Prep](http://www.amazon.com/JavaScript-Plain-Language-Self-Study-AngularJS-ebook/dp/B00NQERIEI) -  If you have found the currently book somewhat difficult to grasp this eBook is for you. It introduces JavaScript concepts followed by advanced topics such as JSON and AngularJS which is the modern way to include JavaScript on an HTML page.
2.  [Practicing AngularJS in HTML: Volumes I & II](http://www.amazon.com/Practicing-AngularJS-HTML-Mastering-JavaScript-ebook/dp/B00P6ZARCA/) – This eBook covers the part of AngularJS written on the book describe above and adds another level to it. It assumes the reader knows basic JavaScript and HTML.
3.  [Solid Steps into JavaScript: A hands on Approach](http://www.amazon.com/Solid-Steps-into-JavaScript-Approach-ebook/dp/B00HGLG4CO/) – You may not need this book since it is less advanced than the one you’ve just read. However, it is a solid book about basic syntax and a way to practice more JavaScript. If you have to choose between this book or the one on the very top which came out later, go with the top book because it covers other important topics. However, if you can afford it and want to practice, then by all means get both.
4.  [Small Projects to Learn JavaScript - Drawing Six 'Lucky' Numbers](http://www.amazon.com/Small-Projects-Learn-JavaScript-Drawing-ebook/dp/B00H4P987A/) – This is a short book but readers love it because it is a fun project to do. In it the concepts covered on the basic books are reviewed and some new concepts are added, such as methods from the Math library. It also introduces a way to **embed JavaScript on HTML**.
5.  [JavaScript innerHTML: A Project in Three Acts](http://www.amazon.com/JavaScript-innerHTML-Project-Projects-Mastering-ebook/dp/B00JAOLFZ6/) – This eBook is also a single project designed to introduce innerHTML. Important concepts about JavaScript as used in HTML are covered. It is a fun topic for a Sunday afternoon.
6.  [JavaScript Objects Functions and Arrays Explained](http://www.amazon.com/JavaScript-Objects-Functions-Arrays-Explained-ebook/dp/B00GDEPBZQ/) –  (**This current eBook**) This is a more advanced JavaScript book. Here, variables, functions, arrays and objects are explained in further detail. Memory management concepts are introduced, the concept of execution context, scope and closures are explained. The book also explains the most useful methods from the JavaScript library. It is a great book to keep around.
7.  [HTML For Everyone - First Layer In Web Literacy](http://www.amazon.com/HTML-Everyone-First-Layer-Literacy-ebook/dp/B00DD24US0/) – This is an introduction to HTML. If you need to review basic concepts or if the is your first approach to HTML this book is for you. If you already know HTML you may find this book very basic because it is an introduction.

Most of these books have been translated to Portuguese. You may find the Portuguese version on my [profile](http://www.amazon.com/Tony-de-Araujo/e/B00D7V08WY/). Please visit. *[ amazon.com/Tony-de-Araujo/e/B00D7V08WY  ]*sd

Future projects:

· More AngularJS

·  Typescript / ATscript / ECMAScript 6

· C#

## Errata and Contact

This work is in an EBook format. Any major modification will be available through Amazon. Normally you will be able to upgrade if the book is modified, please check with Amazon since rules and regulations vary worldwide. All other minor code modifications; error corrections as well as new minor additions will be notified on the raw files the book links to. They will be constantly updated as needed.

My email is [tony@icontemp.com](mailto:tony@icontemp.com)

Learning to code is a cumulative process. That’s why I didn’t overload you with code, just enough to get you started. After all it was the purpose of this book. The other purpose is to use it as a reference when you feel lost or need more detailed information on the objects covered so far.

You can find me at [JSplain.com](http://jsplain.com/javascript/).

My Amazon profile is the following: [www.amazon.com/Tony-de-Araujo/e/B00D7V08WY/](http://www.amazon.com/Tony-de-Araujo/e/B00D7V08WY/)

Thank you,

Tony de Araujo

--- New Jersey, USA

## Copyright

Amazon, Google, Mozilla, ECMASCRIPT and all other famous names used in this book are of their respective owners and being named only to illustrate the concepts written by the author.

All rights reserved © Tony de Araujo

"Be sure you put your feet in the right place, then stand firm". - *Abraham Lincoln*

Gentle Rain

Gentle rain, soothing me
Drops of liquid life
Wind and thunder
Wooing man and mice

Trees and bushes
Moving to and fro
Quiver, tremble, and rock
As lightning makes them glow

I thought I had forgotten
But it all came back again,
All my memories appeared
As drops of gentle rain

They were there, alive and well
In all their glory, their amazing grace
And my mother and my father
In a glorious embrace

It was so long ago
So many years before
And I wish I knew what I know
I would have lived it more!

*Tony de Araujo*
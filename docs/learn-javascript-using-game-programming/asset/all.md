![](Images/cover00502.jpeg)

# Learn JavaScript using Game Programming

First Edition

## Learn the basics of programming and game development using vanilla JavaScript with the canvas tag.

## Chris Moeller

# About the Author

Chris Moeller was born in Mesa, Arizona. He's been playing games since "Wolfenstein 3d", and games like "Monuments of Mars". He originally started working on games by making 3d models in 3ds max. He started programming using C++ and Java, worked as an automation QA engineer, web developer, Flash developer, and has created cross platform games and apps for Android, iOS, and PC.

He's currently working on games and apps for the company he started with his wife and cats, Ackmi.com.  He's interested in creating fun games, and fun educational games, accessible to everyone in the future.

# 1. Introduction

## What will you learn?

You will learn the basics of programming, by creating a game from scratch using JavaScript. With this knowledge, you should be able to proceed to code your own games or apps, whether it be from scratch in another language/ library, or game engine.

I won't do a complete deep dive into all programming concepts, instead focusing on essentials needed to get the game created.

We’ll be going through:

● Setting up your development environment, and setting up a HTML + JavaScript main file.

● Grabbing HTML elements from JavaScript and manipulating them

● Using canvas to draw out the 2d game

● Overview of programming concepts, such as variable types, functions, classes and objects

● Game programming concepts such as drawing in 2d, game loops, getting player inputs, 2d animation, and more

In the end, you'll have a game loop created, draw the game using the html canvas tag, and be able to control a player character that animates when moved. This should give you a good idea about how a game is created, and ideas about expanding what we create to make it into your own game.

You can see all the example files for each chapter here:

[https://github.com/doomtoo/Learn-to-code-games-using-JavaScript-Examples/](https://github.com/doomtoo/Learn-to-code-games-using-JavaScript-Examples/)

## Pros and Cons of using JavaScript

JavaScript can be useful, but also has its own faults. Modern JavaScript is close enough to other languages, where by learning JavaScript, you can easily transition into other languages.

JavaScript’s pros are:

● It can be run on any device that supports a browser (and even without a browser using node.js)

● It has become super versatile in recent years, and can be used in all stages of development, from adding interaction on websites, to being used on backend servers and storing information in databases, or connect people together in multiplayer games

● Modern JavaScript now allows you to code in an intuitive, object-oriented way, and has basic error checking, making it much less frustrating than a few years ago

● You can tie it into HTML and CSS, which makes it easy to layout graphics, UI, and animation

JavaScript’s cons are:

● It appears to be object oriented, but behind the scenes, everything is actually a function, which can cause some odd errors compared to true object-oriented languages, but is mostly hidden using modern coding techniques

● JavaScript maintains backwards compatibility to a fault. A lot of the unusual parts of the language have stuck around forever, and there have been many languages that have sought to replace it with something better. But none have been fully adopted, so JavaScript still exists, keeping much of what was included in its 10-day inception. It used to be very painful to create complex applications in, but modern syntax seeks to alleviate many of the pain points

Conclusion:

JavaScript is relatively easy to get started with. It doesn't have as many rules as other languages, which can allow you to get started faster, but have a harder time tracking down errors. It's not perfect, but it's a great language to start with, and these days you can develop anything in it, as well as use that knowledge to learn other languages.

## What you need to follow along

Recommended requirements:

● A computer that you can install visual code on (PC, mac, Linux, raspberry pi): [https://code.visualstudio.com/](https://code.visualstudio.com/)

● Install live server from the extensions inside visual code. This will allow you to right click in your file, and launch it with live server to see it in the browser.

● Everything used is FREE and open source.

NOTE: visual code is different from visual studio. It's much leaner, faster, and doesn't require multiple restarts and gigs to download.

## What we’re going to make / project planning

One good habit to get into is trying to plan out your projects upfront as much as you can, to have an idea of what tasks you’ll need to do to arrive at your final product.

For this book, my goals are:

● To allow you to learn the basics of programming, while also learning the basics of what is required to make a game

● Make the game relatable to games you may have played and enjoyed

● To include game development concepts that could be used to make any game (2d and later applicable to 3d)

● Not completely finish the game (so you can modify to make it into your own game)

● Provide concepts that allow you to create completely different games than the one created in the book

So, the “elevator pitch” of what I would like to do, as a basic version of the game:

A game where you move a character around in a 2d, tile based, side scrolling world.

Project planning is something you attempt to do upfront with the knowledge you have at the time, but it will always change/ grow as you actually work through your projects. As you finish more projects, you’ll learn from each one, and have a better idea of what you need to do for the next project. 

In the next chapter, we’ll look at setting up our development environment, to get coding.

# 2. Setting up your development environment & boilerplate code

## Setting up Visual Code

Go to: [https://code.visualstudio.com/](https://code.visualstudio.com/) and download and install visual code for your operating system (Windows, Mac, Linux, etc)

![](Images/image00462.jpeg)

Next, start up visual code, click on the bottom left set of boxes (extensions, or hit ctrl+shift+X on PC, command+shift+x on mac), search for "live server", and click the blue install button to install live server in visual code.

![](Images/image00463.jpeg)

Live server needs you to open a folder in Visual Code, where you'll have all your project files located, which will allow it to launch a quick web server from the folder.

Side Note: Don't worry, no one online can access the server, unless you open ports on your router to forward requests to your computer, which is a topic out of scope for this project.

Finally, we'll need to go to the top left hand "File"->"Open Folder". Choose a place where you want your project to go on your hard drive. For instance, click on desktop on the left side. On the right-hand side, right click in an empty area-> "New"->"Folder"-> name the folder "my_javascript_game", and click "select folder" on the bottom to use this folder.

![](Images/image00464.jpeg)

This should refresh the window, showing your project folder on the left-hand side, with a blank grey window below it. Right click in the blank area below your folder name ("my_javascript_game"), and select "new file", and type in: index.html. Alternatively, the button next to your folder name also lets you create a new file.

![](Images/image00465.jpeg)

Now we just need to set up some boilerplate code in our index.html, so we can see our file rendered in our browser.

On line 1, type out: "htm" and it should popup a drop down with 3 options in it (if not, hit "ctrl+space" to bring up autocomplete/ IntelliSense).

![](Images/image00466.jpeg)

Select the second option "html:5      Emmet….", and it should fill out a basic HTML page with boilerplate code:

![](Images/image00467.jpeg)

Now to actually add something so we can see our webpage when we launch it with live server.

Add above "</body>":

<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Document</title>

</head>

<body>

    <h1>This is HTML on my webpage!</h1>

    <script>

        alert("hello from JavaScript!");

    </script>

</body>

</html>

So your code will look like:

![](Images/image00468.jpeg)

Right click anywhere in the code and select-> "Open with Live Server", which will start up the live server, open your webpage in your browser window, and should look like:

![](Images/image00469.jpeg)

If you keep this window open in the background, whenever you change anything in the code, the webpage will automatically be updated, using live server. So Try to keep this browser window open, while working in visual code in the background, and just swap windows to see your webpage updated whenever you save.

If you do accidentally close it, don’t worry- just right click in visual code again, and choose to launch with live server again to have it re-open your browser with your webpage!

## Understanding the HTML boilerplate code

If you don’t know anything about HTML, It would be useful to search online for a basic tutorial on what HTML is, such as searching for "basic html", this comes up: [https://www.w3schools.com/html/html_basic.asp](https://www.w3schools.com/html/html_basic.asp)

Basics of html tags

A html tag will usually be in this format: <atag> some info</atag>. The "atag" here is a predefined word, which you can look up by looking for "html tags" in the search engine.
But a html tag is always wrapped in triangle like brackets, one "opening the tag": "<anothertag>", followed by information you want in the tag: "this is in the tag", and finally closing the tag, which is just the same as the opening tag, but with a forward slash in front of the words (indicating you’re closing the tag): "</anothertag>".

How is this useful?

The tags in html let the browser know what is going to be inside them. Whether it be the container of the html page, where the JavaScript will go, or text on the screen, which can be made up of paragraphs, headers, etc. It's basically how you talk to the browser, to let it know what to do with the info you give it.

Basic structure of an html page

The basic structure of an html page is just:

<html>

    <head>

    </head>

    <body>

    </body>

</html>

The "html" tag just lets the browser know where your web page starts and ends.

The head tag

The "head" tag is the first tag inside html, which can have stuff in it that will not be visible on the page.

This can be stuff like CSS (cascading style sheets), which is used for styling your webpage, such as changing colors, positioning things, and making the html content look cool.

Or you can put JavaScript tags in there, which runs before the page is fully loaded. Or as you saw above, a "title" tag, which shows the title of your website in the browser.

There's other stuff you can put in there, including some of the stuff inserted in the boilerplate code such as:

<meta name="viewport" content="width=device-width, initial-scale=1.0">

Which allows web pages to scale properly on mobile devices. There are many other predefined tags, which you can do a web search on if you want to learn more, but we'll just be using the boiler plate code for our purposes.

The body tag

The "body" tag is where the actual content of your page will go. If you want text, images, headers (such as "chapter 1" or "what I did this summer"), it all goes in the body tag. Additionally, if you want your JavaScript to run after the rest of the page has loaded (which is common these days to be able to access html on the page), you'll want to put it right before the end of the body tag.

We used the "h1" tag (also known as "Header 1") for some text on the page. H1 is your biggest header for your most important information about your page (like "Welcome to my awesome webpage"), but headers can go all the way down to h6, which is the smallest header.

For normal text you can use a paragraph tag (such as: <p> I like turtles because turtles eat pizza, are expert ninjas…. </p>). You can search online for "html tags" and find a bunch of them, including image, divs (divisions- for separating your html page into different rectangles, for things like 2 column layouts), canvas (to draw on for games), etc.

I'll include more info on html tags we need as we go along, but in general, just search online if you find you want to add something to a webpage, but you don't know how yet, and you're likely to find the info you need.

Script tag

We used the "script" tag to put some JavaScript into the page:

<script>

    alert("hello from JavaScript!");

</script>

All of our JavaScript goes inside this html script tag. Once we're inside the script tag, you can't use any more html tags inside of it- it becomes a programming only area/block.

"alert" is a function built into all browsers, which allows you to put a notification box that pops out of the browser when it's run.

It's pretty annoying, but that was originally the most widely used JavaScript across the web, and you could actually lock up a browser by spamming it constantly. But you'll find that JavaScript has come a long way in recent years from a humble beginning of being used primarily for annoying pop ups!

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/2_Boilerplate.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/2_Boilerplate.html)

# 3. Programming concept: Variables

## Storing Strings

The first thing to learn to begin programming is about variables. Variables are just names you give to a value you want to remember.

For example- I have 3 friends.

Friend 1 is named Tom Smith. He's 9 years old, has brown hair, his catchphrase is "Tom in da house!", and loves spinach.

Friend 2 is Jill Jones. She's 18 years old, has blonde hair, her catchphrase is "Jillin be illin!", and doesn't love spinach.

Friend 3 is Steve Thomas. He's 22 years old, has red hair, his catchphrase is "Who took my stapler?", and also doesn't love spinach.

My memory is pretty terrible, so I'm going to store my friends' information in variables on the computer.

Some rules for creating variables:

● In JavaScript, you create a new variable using the keyword 'let' (or in the past 'var').

● A variable name can't have any spaces in it, so I use underscores (example: "my_var_name") instead of spaces.

● If you want to store words like a name (which is called a string), you need to put it in between 2 quotes: "_ _ _ _" or "It was a dark and stormy…".

● You also need to end each line with a semicolon, to let JavaScript know you finished what you wanted to say.

So, let's create 3 variables for each of our friends' names. Inside the script tag add:

let friend1_name = "Tom Smith";

let friend2_name = "Jill Jones";

let friend3_name = "Steve Thomas";

That's all we have to do to create 3 variables, one for each friend's name, and store their names in memory!

We used underscores instead of spaces in the variable names (friend1_name), and quotes around text we want to store, which can have spaces in it (example: "Tom Smith").

But how do we know we actually created these variables (aside from not seeing any errors)?

There is a built-in statement that you can use to see what your program is doing called “console.log()”, example:

console.log("put something in here!");

This lets us "log" out any information to the console, so we can see what is happening in our program at any time, behind the scenes (kind of like a cheat area for programmers to see what the program is doing).

So, we can add console.log statements below where we declared our variables, like this:

console.log("My friends are: ");

console.log(friend1_name);

console.log(friend2_name);

console.log(friend3_name);

Which would print out:

My friends are:

Tom Smith

Jill Jones

Steve Thomas

To make it easier, we can actually combine words/ strings into one string using '+', so we don't have to have multiple console.log statements.

For example:

console.log("One of my  friends is: "+friend1_name);

Combining all of them, with a comma and a space inside its own quotes, in between each string:

console.log("My friends are: " + friend1_name + ", " + friend2_name + ", " + friend3_name );

Which prints out:

My friends are: Tom Smith, Jill Jones, Steve Thomas

Your final script tag will look like:

<script>

    let friend1_name = "Tom Smith";

    let friend2_name = "Jill Jones";

    let friend3_name = "Steve Thomas";

    console.log("My friends are: " + friend1_name + ", " + friend2_name + ", " + friend3_name );

</script>

So now we can now print out the names we gave the variables (such as 'friend1_name'), and it will show us the actual friend’s name (the value) stored in that variable.

To see the console

If you run this in live server, you won’t see anything until you open up the console. If you’re using Firefox or Chrome, you can hit the key on your keyboard “F12” to bring up the console, or right click on the web page, go to inspect (ctrl+shift+i), and click on “console”. You should then be able to see your console.log statements on the right side of the screen, under the console.

![](Images/image00470.jpeg)

## Storing numbers

But what if we want to store other information about our friends? Such as their age?

We can do it the same way, but because these are numbers instead of words, we don't put quotes around them.

let friend1_age= 9;

let friend2_age= 18;

let friend3_age= 22;

You can also console.log out these if you want to see the value was stored in the variables.

console.log("My friends ages are: " + friend1_age + ", " + friend2_age + ", " + friend3_age);

## Storing true or false (Booleans)

What about storing whether they love spinach? Liking spinach can either be true or false. In programming, we call things that can be either "true" or "false" as "Booleans". Like a light switch can either be on or off, or you can either be able to lick your own elbow, or not.

let friend1_loves_spinach = true;

let friend2_loves_spinach = false;

let friend3_loves_spinach = false;

You can also console.log out these if you want to see the value was stored in the variables.

## Advanced topic/ nice to know - other types of variables

Later on, we'll use other types of variables. Most programming languages have different types of variables built in, that lets you store different kinds of "basic" information. You don't need to know these in depth now, but if you're curious, there's more information below.

Built in types usually include:

### For storing numbers:

int - For integer- it's for whole numbers, that don't have decimals. Like 1, 4, 200, 9000). Even more advanced, in some languages you can define how big of an integer it might be, so you don't waste memory reserving space for a giant number, but only needing to store a little one.

For instance, if you're just storing someone's age, you know it will be between 0-120, you could use a int8, which will allow you to store any number between -128 up to 127\. Or if you're storing the U.S debt in trillions ($26.70 trillion, or 26,700,000,000,000), you'll need to use int64 to be able to store such a large number. But JavaScript doesn't have these/ only has one type for storing all numbers.

float - For "floating point numbers", or numbers that have decimals in them. Like 0.75, 1.9, 100.6, or even 10.0 (they can store whole numbers too, but take more memory for the same number than integers to store, so not ideal)

number - (only in JavaScript- for storing an integer/ whole number or a floating/ decimal number- makes it simpler, at the cost of using more memory)

### For storing more than one thing:

Say you want to store all your friends inside of one variable. There's a thing that allows you to store a whole list of them, but only have to refer to the list name (like "my_friends"), instead of having to have a variable for every friend.

array - An array is a list of things, like your friends, or foods you like, but allows you to only have to remember the name of the array. In most languages, you need to know how many things you'll store in there ahead of time, and have to create a new array when you have too many things to fit in one. But you can store less things in it, and leave spots blank. This seems like a bother, but is faster for the computer to do, and is important if you need a lot of performance)

list - pretty much the same thing as an array, except you can add new items to it whenever you want, and behind the scenes it creates a new, bigger list, and you don't have to worry about it. This is what JavaScript uses as its "array")

### For storing text:

char - For characters- single letters. It's a basic type that lets you store one letter, but isn't super useful on its own)

string - Allows you to store a bunch of characters instead of just one, so you can store names, sentences, even a book in one. Behind the scenes it's actually an array of characters/words, and it's managed automatically behind the scenes.

### For storing "nothing":

Sometimes you'll actually want to store "nothing". For instance, if your player can know who he is attacking, but hasn't started attacking yet, you'll want to be able to check whether he's attacking someone, or "no one/ nothing".

null - This means "nothing", or "I have the variable name, but nothing is stored in it yet". Most languages have this as an option for any variable, but JavaScript makes its own unique "type", which can be tricky coming from any other programming language. You have to manually assign a variable the value of null in JavaScript ( ex: let my_spouse_name = null), which makes it have its own "type" of null, different than a string/words or a number, even if you intend that variable to be a string/number soon afterwards.

undefined - This is only used by JavaScript. JavaScript has 2 versions of "nothing". Undefined means that you created the variable, but didn't give it a value yet (didn't say it's equal to a number, or some text, just declared it). It's essentially what "null" is in other languages.

### For storing true/ false

bool or boolean - This is unique in that it only stores true/ false. This makes it so it uses the least memory of any other type, since it can only store 2 values (essentially a 0 or a 1 in binary).

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/3_Variables.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/3_Variables.html)

# 4. Bundling up many variables into a single object

We already have 9 different variables for our 3 different friends, and there's more info that we want to store about them (hair color, catchphrase, etc.). Wouldn't it be nice to have just one variable we can refer to for each person, with variables inside it for their specific information?

Luckily someone already thought of it! Since they all have the same type of things we're interested in storing (name, age, loves spinach, etc.), we can create a "class", which is just saying what stuff we want to store for all of our people/ friends.

A class in general is just defining something that will hold information for a bunch of similar objects (like a blueprint, or an idea). It's something that doesn't do anything on its own, so we'll later have to use it after we define it.

## Creating our own type/ class/ template/blueprint

So, we create it like:

class Friend

{

    constructor()

    {

        this.name = "someones name";

        this.age = 0;

        this.loves_spinach = true;

        console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

    }

}

You use curly braces (such as: {}) inside a class or a function (more on this later on) to show where the class will begin and end.

The key word "constructor()", with the parenthesis, is a function that gets run automatically whenever a new "Friend" i created from our friend class. It also uses curly braces to show the start and end of the function. It also needs normal circular parenthesis (ex= () ), which means it will be a function that gets run/called, and not a variable.

Declaring variables inside a class, you don't need to use the "let" keyword anymore, but do have to use "this.variable_name", with "this" which will refer to any object you create from the class.

## Creating an object from our class

So now if we want to create a new friend variable from the class we just defined, which will have the other 3 variables types inside of it, we can do:

let my_friend = new Friend();

That's all that's needed to create 1 new friend object, which is one friend that has everything defined by our Friend class/blueprint above!

This will also automatically run the constructor which the object is created from the class, which creates the name, age, loves_spinach variables inside of a new friend object (based off of the friend class template), and will print out the console.log right before the end of the "constructor" function (which automatically gets called whenever we create a new friend). So, if you type that in now, you'll just see the console.log being outputted.

Your script tag will look like:

<script>

    class Friend

    {

        constructor()

        {

            this.name = "someones name";

            this.age = 0;

            this.loves_spinach = true;

            console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

        }

    }

    let my_friend = new Friend();

</script>

And if run, will print out:

A friend was created, with name: someones name, age: 0, and loves spinach: true

If we want to say change out the name and age, we can do so by adding on the next line after creating a new friend:

my_friend.name="Timmy";

my_friend.age=12;

To verify we changed it, we can console.log it out on the next line:

console.log("My friend name is: " + my_friend.name +", and his age is: "+ my_friend.age);

JavaScript also lets you print out the entire object if you want to see what it looks like:

console.log(my_friend);

So, if we want to make another new friend, do the same thing (which will look at the class, create a new object from that class, and give us the new object back), by adding on the next line:

let my_other_friend = new Friend();

And if you print out this one, you can see it's a different object then "my_friend", but they both are based off the "Friend" class, both have the same type of variables inside them, but different values stored in their own variables (this friend just has the default name, age, etc we assigned it in the constructor)

console.log(my_other_friend);

To change the name and age again, we'd have to do something like:

my_other_friend.name="Betty Sue";

my_other_friend.age=110;

But wouldn't it be nice if we could just assign the name and age the same time we create the friend, instead of having to put it on 3 different lines, since we'll probably almost never use the default name/ age anyways?

Again, there is a way!

Your final code should look similar to:

<script>

    class Friend

    {

        constructor()

        {

            this.name = "someones name";

            this.age = 0;

            this.loves_spinach = true;

            console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

        }

    }

    let my_friend = new Friend();

    my_friend.name="Timmy";

    my_friend.age=12;

    console.log("My friend name is: " + my_friend.name +", and his age is: "+ my_friend.age);

    console.log(my_friend);

    let my_other_friend = new Friend();

    console.log(my_other_friend);

    my_other_friend.name="Betty Sue";

    my_other_friend.age=110;

    console.log(my_other_friend);

</script>

## Passing in values to the constructor function

We can actually pass what we want those variables to hold to the constructor, and assign it there instead of the default values! So, change the class to:

class Friend

{

    constructor(their_name, their_age, their_loves_spinach)

    {

        this.name = their_name;

        this.age = their_age;

        this.loves_spinach = their_loves_spinach;

        console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

    }

}

So, we are going to pass over what we want those variables to hold, and instead of just the default values being assigned to our friends’ variables, it will assign any value we pass in. So, we can now just do:

let my_new_friend = new Friend("Steve", 12, false);

Which will pass "Steve" in, and name it with the variable in the first parameter (their_name), next pass in 12, and assign it to the next variable in the constructor (their_age), and finally the last thing we pass to it is false, which gets passed over and stored in the variable (their_loves_spinach).

Side Note: The names of the variables in the constructor parameters (ex: their_name, their_age, etc) can be called anything we want, because those variable names will only exist inside the constructor. We could call them var1, var2, or param1, param2, or name age, etc. It just depends on what makes the most sense to you. But since they are only defined in the parameters (the parenthesis) of the constructor, they won't exist outside it.

So now we can create new friends super easy, and it only takes one line to do it!

Example:

let my_new_friend = new Friend("Steve Guttenberg", 12, false);

let my_new_friend2 = new Friend("Zhanna Matzaball", 36, true);

let my_new_best_friend = new Friend("Jerriah N", 1, false);

But what if we want them to console.log out their information? Right now we'd have to do:

console.log("Hi, my name is "+my_new_friend.name +", my age is: "+my_new_friend.age+", and do I love spinach? "+my_new_friend.loves_spinach+".");

For every friend! If we have 5 of them, it's a lot of text to type, 20, even more so. Wouldn't it be nice if we could ask each friend to say their own information, and type out something much shorter than "console.log…"?

## Functions / Methods- doing something

Luckily there is! We can put a custom function in our class, somewhat like the constructor, and we can just have it run whenever we want to. So, change our friend class to be:

class Friend

{

    constructor(their_name, their_age, their_loves_spinach)

    {

        this.name = their_name;

        this.age = their_age;

        this.loves_spinach = their_loves_spinach;

        console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

    }

    SayHi()

    {

        console.log("Hi, my name is "+this.name +", my age is: "+this.age+", and do I love spinach? "+this.loves_spinach+".");

    }

}

So, we just created a new function called "SayHi", and we're not passing in any variables, because it will already have all the information stored in any friend object, because it’s inside of it (name, age, etc.).

Now you can just call/run this function for it to print out all the friend information, like:

my_new_friend.SayHi();

my_new_friend2.SayHi();

my_new_best_friend.SayHi();

So now we have a friend class/ template/ blueprint that we're using to create several friend objects. They are based on the class/ all have the same variable types and functions, but can each store different information in their own object variables. They are all friend type objects, but can have a different name or age than the other ones.

We also have them passing in the values for their variables through the constructor when they get created, and added a function to make them tell us about themselves.

Wouldn't it be cool if we could now actually see our friends somehow? Like drawing them out to the screen with other information, like hair and eye color? We can in the next section!

Your final code will look something like:

<script>

    class Friend

    {

        constructor(their_name, their_age, their_loves_spinach)

        {

            this.name = their_name;

            this.age = their_age;

            this.loves_spinach = their_loves_spinach;

            console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

        }

        SayHi()

        {

            console.log("Hi, my name is "+this.name +", my age is: "+this.age+", and do I love spinach? "+this.loves_spinach+".");

        }

    }

    let my_new_friend = new Friend("Steve Guttenberg", 12, false);

    let my_new_friend2 = new Friend("Zhanna Matzaball", 36, true);

    let my_new_best_friend = new Friend("Jerriah N", 1, false);

    my_new_friend.SayHi();

    my_new_friend2.SayHi();

    my_new_best_friend.SayHi();

</script>

## Advanced topic/ nice to know info about functions

A function is usually just some action you want to do. For example: Car.MoveForward(), Car.Stop(), Player.HitEnemy(), TextField.CheckIfEmpty(), Data.SubmitToServer(), Computer.Restart(), Facebook.Open().

You can call them multiple times, not send any additional information to them if they don't need it, or pass information in to them if they need values to do whatever you want them to do. For instance, if the player is supposed to hit an enemy, you might want to pass in which enemy to hit, how much damage the player is doing, what animation you want to play (if it's a magic or physical attack).

The initial structure is based on whatever makes sense to you at the time. If you have all the information in your class you need to run the function (like make the player run), you don't have to pass anything. If you want the player to run at different speeds, you can send what speed you want him to run at, and pass it in as a parameter. It will all make sense/ become easier the more you do it (like everything else, practice makes perfect).

Functions are also called "methods" in some languages - sometimes just when they are inside a class. People use the terms interchangeably, depending on the programming language. I prefer the term "function"- because they usually do something/ provide some kind of function, but it's a matter of preference.

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/4_Objects.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/4_Objects.html)

# 5. Creating visuals by connecting JavaScript to HTML

JavaScript allows you to do stuff, storing information, getting key inputs from a user, interaction, etc. But besides looking at the console, it has no way of outputting to a user, showing a user interface, or really being able to communicate with someone who is trying to use a program/ game/ app you built.

Luckily, something came before JavaScript that is meant to be visual, and JavaScript can talk to it (getting stuff from it, and sending stuff to it), that we can use to start showing stuff on screen!

That is HTML, or known as 'HyperText Markup Language', a fancy way of saying "it allows you to show information". HTML is mainly used to layout information- text, pictures, etc. HTML wraps text in "tags", which represent parts of a webpage, who are all wrapped in triangle brackets like <this_could_be_an_html_tag>. Additionally, most tags have to close after you put any information inside of them, by putting a forward slash: "/" in a second copy of the tag. For example:

<text> this is some text </text>

<image> this is an image</image>

Those aren't the actual format for that information, but it shows how information has to be inside an open and close tag.

All HTML documents/ files have to all follow the same basic structure.

First, we need an open and close html tag:

<html>

</html>

Next, html has a head like you, and a body like you as well. The head you can think of as like your thoughts- you can't see what you put in it on the final page, but it's there for things that run behind the scenes. Things like the JavaScript, the title for your page (which shows up in the top of your browser, not on the page), or even the colors for your page can go there.

<html>

    <head>

    </head>

</html>

Finally, it also has a body- just like you, which will actually be visible on the page, and this is where everything you want to be seen will go.

<html>

    <head>

    </head>

    <body>

    </body>

</html>

That's the basic structure required of all HTML pages- it's just required before we can add anything that we can see. Now we can start adding stuff that we can actually see.

You'll notice in HTML, you'll want to indent/ move forward with around 4 spaces or 1 tab any tags that are inside other ones. That way you can easily see what tags are inside other ones, because that will make things much easier to organize when things become more complicated in the future.

Let's add some text (also known as a paragraph, or the <p> tag, one tag you can put text in), and something that will allow us to draw from JavaScript- the canvas tag. Canvas is what you use to paint on in art- usually some white cloth where you'll start painting all your colors on. Since we're not going to draw anything on it yet, it will just be white, so won't be visible unless we give it a border:

<html>

    <head>

    </head>

    <body>

        <p>This is some text that I created on a webpage</p>

        <canvas style="border:1px solid green"></canvas>

        <script>

        </script>

    </body>

</html>

If you run this now, you'll see our text on the webpage, and a small box with a green border on it, which is our canvas, that will let us draw!

We added "style" to the canvas tag, which is called an "attribute".

Style is also known as "CSS", and this allows us to change how things look, changing colors, background colors, font type, almost anything that modifies things visually. It's known as "cascading style sheets". Cascading is like a waterfall- where water from the top cascades down the waterfall, going lower and lower till it splashes in a pool.

Likewise with CSS, you could say a background color is red, and below it, change it to green, and it will override the top color/ style. Seems kind of pointless right now, but it becomes useful as things become more involved. For instance, if you want to have all text being black, but then you have some boxes that are black, and you want that text inside them to be white, you'd define your whole page to have black text, but later say that text in the black boxes should only be white.

It's another concept that will make more sense when you need to use it more, but for now all you need to know is it allows you to change colors, spacing, and most things visually for HTML.

HTML is just used to state what content is there (an image, text, the canvas tag, a video tag, etc), but CSS lets us change how it's displayed differently than the default/ built in CSS.

The canvas tag is different in the way that we can draw inside of it using JavaScript, without needing to worry about CSS inside of it.

So, let’s now connect our JavaScript to HTML, by grabbing both the paragraph tag, and the canvas tag, and modifying them from JavaScript!

## Modifying HTML from JavaScript

There are some built-in functions, that are part of JavaScript, that allow us to grab an HTML tag from our HTML. If we want to grab our paragraph(<p>) tag, we can do it by putting into JavaScript (inside the script tag):

document.querySelector("p");

This will grab the first <p> tag from our html, but doesn't do anything with it, so we can't see it did anything. So, let's console.log it out instead:

console.log(document.querySelector("p"));

If you look at the console, you'll see it shows:

<p>This is some text that I created on a webpage</p>.

This is a built-in function, but you can think of "document" as the main html tag, and "querySelector" as a function built into "document" that lets you grab html tags on your page, in a lot of different ways.

But what if we want to change the text inside our paragraph from JavaScript? Well, let's first store the paragraph in a variable, so we don't have to type out "document.query…." every time we want to access it. So:

let my_paragraph = document.querySelector("p");

So now we have the paragraph HTML element stored in our variable "my_paragraph", so anytime we want to play with it, we now have a variable we can access it with.

Now let's change the text INSIDE the p tag- also known as the "inner html"

my_paragraph.innerHTML = "I changed this text from JavaScript!";

If you run this, you'll now see that the text is changed on your HTML page! Every time the page loads, the JavaScript runs, and replaces the text quickly. Later on, we could add a button, or some other kind of input to change the text after the page loads, so there would be a delay to see it change. But for now, we'll work on drawing something in the canvas tag.

## Drawing with the canvas tag

So first you'll want to grab your canvas tag again, and assign it to a variable for easy access:

let my_canvas = document.querySelector("canvas");

Additionally, to actually draw on the canvas, you need to ask it for a "drawing context", and tell it you just want to draw normal 2d drawings for now (and not 3d):

let draw_context = my_canvas.getContext("2d");

If we want to, we can actually create another variable name that is shorter, and use that instead, even though it's less clear- it will store the same reference to our canvas tag, but an additional name (or alias) we can refer to it with. This is similar to calling someone Bill, Billy, Bill-dawg, B-shidigy, Will, Willy, etc. Same person, but can call them several different names/ or aliases.

let ctx = draw_context;

Now let's draw something- say a block/rectangle for a head.

First, we'll need to tell it what color we're using, by calling "fillStyle =color"

Then we'll need to tell it we're going to draw a filled in rectangle using: "fillRect(left, top, width, height)":

ctx.fillStyle = "pink";

ctx.fillRect(10, 20, 50, 60);

The 'fillRect' function requires 4 parameters to be passed to it to draw a rectangle- where to put it, and how big to make it.

The first two are how far away to draw it from the top left of the canvas. We supplied "10" to draw it 10 pixels/squares away from the left side, and "20" to draw it 20 pixels down from the top.

The next two parameters are the width and height to make the rectangle. We have it 50 pixels wide, 60 pixels tall (a head is taller than it is wider, usually).

You can play with these, make bigger rectangles, position them differently, etc.

You should have something like the following example:

<script>

    let my_paragraph = document.querySelector("p");

    my_paragraph.innerHTML = "I changed this text from JavaScript!";

    let my_canvas = document.querySelector("canvas");

    let draw_context = my_canvas.getContext("2d");

    let ctx = draw_context;

    ctx.fillStyle = "pink";

    ctx.fillRect(10, 20, 50, 60);

</script>

![](Images/image00471.jpeg)

### Side Note: Colors

For the color, we can supply most normal color names, but if we want to supply a custom color, say a pinkish brown flesh tone, we'd have to send a custom color in a different way.

On the computer- it displays everything using tiny little dots on the screen, which are made up of 3 different dots- red, green, and blue. Kind of like crayons- you have primary colors, and by combining those colors, you can make a ton of different other colors.

With crayons, you can draw blue, and then yellow on top of it, and it will combine to make green. Crayons are made up of pigments- like if you squashed a blueberry on your white shirt- it would stain it blue. They combine in a certain way to make other colors, but colored light combines into different colors than pigments do. So blue and yellow light won't make green like they do with pigments, but mix to make a completely different color with light.

You can learn more here:

[http://learn.leighcotnoir.com/artspeak/elements-color/primary-colors/](http://learn.leighcotnoir.com/artspeak/elements-color/primary-colors/)

In programming, if we want none of a certain color, its value is 0\. If we want the maximum amount of the color, its value is 255- which means 100% (it may seem odd right now, but 0-255 is a way of conserving memory into 1 byte, but also letting us have more than 0-100 different colors).

Instead of 0-255, you may see something called "hexadecimal"- hexa meaning 6\. That's because they use 2 values for red, 2 for green, 2 for blue- 6 total values. And instead of 0-255, they use 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F- or 0-F (F being the highest value).

Some examples:

100% red in RGB (format: red 0-255, green 0-255, blue 0-255):

rgb(255, 0,0)

In hexadecimal (format: rr gg bb)

FF0000

100% blue in RGB:

rgb(0, 0,255)

In hexadecimal (rr gg bb)

0000FF

And a mid gray (equal amounts of all of them- 127 is about half 255)

rgb(127, 127, 127)

In hexadecimal (rr gg bb)

7f7f7f

### Creating a tan color

The easiest way to find the red, green and blue (rgb) values you want to use, is to find one in an app with a color picker (like photoshop) or google even has one:

[https://www.google.com/search?q=color+picker](https://www.google.com/search?q=color+picker)

Using the hue slider on the bottom, change to the general color you want (between red and yellow, closer to red- a bit of an orange). Next move the main slider (saturation) window to the left, close to gray/ white and black, which will de-saturate the color/ making it more gray/ less intense, and bringing the value/brightness down a little, making it slightly darker. This gave me the RGB values: 209, 181, 140, a tan color, which we'll now change our rectangle to be:

ctx.fillStyle = "rgb(209, 181, 140)";

ctx.fillRect(10, 20, 50, 60);

## Adding more to our rectangle

Having a head is pretty cool, but let's add more- say eyes next.

We'll want to make variables to store our colors in, since we'll have to refer to the eye color for each eye, say 100% blue:

let eye_color = "rgb(0, 0, 255)";

Now to draw it on our rectangle. It will be smaller, down a little more, and each eye offset from the other:

//set the fill style:

ctx.fillStyle = eye_color;

//draw the left eye

ctx.fillRect(20, 35, 10, 15);

//draw the right eye

ctx.fillRect(40, 35, 10, 15);

Example:

![](Images/image00472.jpeg)

### Side note: Comments:

You'll notice I put little comments above the fillStyle and fillRects above. By putting 2 forward slashes (//) in front of some code, it will create a comment, which is something the computer will completely ignore, but is placed for humans to leave notes to themselves/ others, or to temporarily make some code not be run if put on the front of a line.

So if you want to stop drawing the right eye to test this, just add // before ctx.fillRect(40, 35, 10, 15);, and it will "comment" it out, making it so it no longer runs, but you as a human can still see it. I'll use these more in the future, since commenting code can help you write down what you are about to do, so you can plan out what your code will be, or will allow you to look back, and immediately see what a line of code does by looking at the comment.

## We gotta do more!

Now let's try to draw a mouth, nose, hair, maybe a body, some clothes, and do the same thing for 20 other friends. Doing it the current way is going to take a looooong time, and we'll just be repeating ourselves a lot. If only there was some way we could do the same thing over and over, but slightly different? Like drawing a bunch of heads, all with different skin colors, and eye colors, that we somehow pass unique values to only have to change the differences.

Wait- we already learned about functions- so this seems like it would be the right tool for the job!

So, let's add some variables to our friend class, to make them be able to draw out their own heads, with their own colors. Change out our code to:

class Friend

{

    constructor(their_name, their_age, their_loves_spinach, their_eye_color, their_skin_color, their_hair_color, their_x_pos, their_y_pos)

    {

        this.name = their_name;

        this.age = their_age;

        this.loves_spinach = their_loves_spinach;

        this.eye_color = their_eye_color;

        this.skin_color = their_skin_color;

        this.hair_color = their_hair_color;

        this.x_pos = their_x_pos;

        this.y_pos = their_y_pos

        console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

        console.log("And some facts about them, eye color: "+this.eye_color+", skin color: "+this.skin_color+", hair color: "+this.hair_color+", x and y: "+this.x_pos+", "+this.y_pos);

        this.DrawFriend();

    }

    SayHi()

    {

        console.log("Hi, my name is "+this.name +", my age is: "+this.age+", and do I love spinach? "+this.loves_spinach+".");

    }

    DrawFriend()

    {

        //this is where we will start drawing our friend

    }

}

So, we just added more things to pass to the constructor- eye, skin, and hair color. We also don't want all our friends to be drawn on top of each other, or we'll only see one, whoever is drawn last/ on top of the others. So, we're also going to provide an x and y position, to position them inside the canvas. We also have it logging out those variables, so we know they got set properly.

At the end, we're going to call/invoke our new function "DrawFriend()". Nothing is in there yet, except a comment about us wanting to draw them. So, we'll fill it in with what we already did, but use the variables we defined for the colors, and the position.

## Creating the DrawFriend Function:

So update DrawFriend() to:

        DrawFriend()

    {

        //this is where we will start drawing our friend

        //---------------- get the canvas stuff we need to be able to draw ----------------

        let my_canvas = document.querySelector("canvas");

        let draw_context = my_canvas.getContext("2d");

        let ctx = draw_context;

        //---------------- draw the head ----------------

        //define width and height of the head

        let width_head = 50;

        let height_head = 60;

        ctx.fillStyle = this.skin_color;

        ctx.fillRect(this.x_pos, this.y_pos, width_head, height_head);

        //---------------- draw the eyes ----------------

        //define width and height of the eyes

        let width_eyes = 10;

        let height_eyes = 15;

        //set the fill style:

        ctx.fillStyle = this.eye_color;

        //define how offset the eyes should be from the left and right side of the head

        let eye_x_offset = 10;

        //define how offset the eyes should be from the top of the head

        let eye_y_offset = 15;

        //--draw the left eye, left corner, top , width and height --

        ctx.fillRect(this.x_pos+eye_x_offset, this.y_pos+eye_y_offset, width_eyes, height_eyes);

        //--draw the right eye--

        //a lot more complicated- have to find right side of head (x_pos+width_head), then minus out the width of eye + x offset of eye to position the left side of the eye away from the right side of the head

        let right_side_of_head=this.x_pos+width_head

        let right_eye_x_pos = right_side_of_head - width_eyes-eye_x_offset;

        ctx.fillRect(right_eye_x_pos, this.y_pos+eye_y_offset , width_eyes, height_eyes);

    }

Ouch, a very long function. We're doing the same thing as before, but we're using "this.x_pos", the y_pos, the eye color and skin color to draw the head instead.

For the left eye- we just take the x position of the left side of the head, and add the offset/ how far we want the left side of the eye to be away from the left side of the head.

For the right side, it's a lot more complicated, and we actually have to do some more math steps. It by default draws the rectangles from the top left, but we want to place it away from the right side of the head. So, we first figure out where the right side of the head is. The x_pos is the left side + the width of the head gives us the right side.

If we drew here, the eye would start off the right side of the head. So we need to minus the width of the eye, which moves the eye to the left that much. and now the eye would be drawn up to the right edge of the head. Finally, we need to minus our eye offset, to move it away from the right side of the head, the same that we moved the left eye.

## Creating and drawing a bunch of friends:

You could at this point play with the head width and height, or the eye width, height, and offsets to change how the face is laid out. But now we can easily draw a few friends with:

//create 3 new friends:

//the parameters we are passing are: (their_name, their_age, their_loves_spinach, their_eye_color, their_skin_color, their_hair_color, their_x_pos, their_y_pos)

let timmy = new Friend("Timmy Smith", 16, true, "rgb(0,0,255)", "rgb(209, 181, 140)", "rgb(125, 60, 34)", 20, 20);

let jackie = new Friend("Jackie O", 42, true, "rgb(0,255,0)", "rgb(245, 215, 171)", "rgb(110, 91, 91)", 100, 50);

let shaun = new Friend("Shaun W", 30, true, "rgb(31, 26, 22)", "rgb(79, 48, 23)", "rgb(5, 2, 0)", 200, 10);

let megan = new Friend("Megan Rocky", 16, true, "rgb(0,0,0)", "rgb(209, 181, 140)", "rgb(0, 60, 0)", 260, 120);

If you run this, you'll see we get a bunch of different faces with eyes, all with different colors and positions!

Example:

![](Images/image00473.jpeg)

Full code listing:

<html>

    <head>

    </head>

    <body>

        <p>This is some text that I created on a webpage</p>

        <canvas style="border:1px solid green"></canvas>

<script>

    class Friend

    {

        constructor(their_name, their_age, their_loves_spinach, their_eye_color, their_skin_color, their_hair_color, their_x_pos, their_y_pos)

        {

            this.name = their_name;

            this.age = their_age;

            this.loves_spinach = their_loves_spinach;

            this.eye_color = their_eye_color;

            this.skin_color = their_skin_color;

            this.hair_color = their_hair_color;

            this.x_pos = their_x_pos;

            this.y_pos = their_y_pos

            console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

            console.log("And some facts about them, eye color: "+this.eye_color+", skin color: "+this.skin_color+", hair color: "+this.hair_color+", x and y: "+this.x_pos+", "+this.y_pos);

            this.DrawFriend();

        }

        SayHi()

        {

            console.log("Hi, my name is "+this.name +", my age is: "+this.age+", and do I love spinach? "+this.loves_spinach+".");

        }

        DrawFriend()

        {

            //this is where we will start drawing our friend

            //---------------- get the canvas stuff we need to be able to draw ----------------

            let my_canvas = document.querySelector("canvas");

            let draw_context = my_canvas.getContext("2d");

            let ctx = draw_context;

            //---------------- draw the head ----------------

            //define width and height of the head

            let width_head = 50;

            let height_head = 60;

            ctx.fillStyle = this.skin_color;

            ctx.fillRect(this.x_pos, this.y_pos, width_head, height_head);

            //---------------- draw the eyes ----------------

            //define width and height of the eyes

            let width_eyes = 10;

            let height_eyes = 15;

            //set the fill style:

            ctx.fillStyle = this.eye_color;

            //define how offset the eyes should be from the left and right side of the head

            let eye_x_offset = 10;

            //define how offset the eyes should be from the top of the head

            let eye_y_offset = 15;

            //--draw the left eye, left corner, top , width and height --

            ctx.fillRect(this.x_pos+eye_x_offset, this.y_pos+eye_y_offset, width_eyes, height_eyes);

            //--draw the right eye--

            //a lot more complicated- have to find right side of head (x_pos+width_head), then minus out the width of eye + x offset of eye to position the left side of the eye away from the right side of the head

            let right_side_of_head=this.x_pos+width_head

            let right_eye_x_pos = right_side_of_head - width_eyes-eye_x_offset;

            ctx.fillRect(right_eye_x_pos, this.y_pos+eye_y_offset , width_eyes, height_eyes);

        }

    }

    //create 3 new friends:

    //the parameters we are passing are: (their_name, their_age, their_loves_spinach, their_eye_color, their_skin_color, their_hair_color, their_x_pos, their_y_pos)

    let timmy = new Friend("Timmy Smith", 16, true, "rgb(0,0,255)", "rgb(209, 181, 140)", "rgb(125, 60, 34)", 20, 20);

    let jackie = new Friend("Jackie O", 42, true, "rgb(0,255,0)", "rgb(245, 215, 171)", "rgb(110, 91, 91)", 100, 50);

    let shaun = new Friend("Shaun W", 30, true, "rgb(31, 26, 22)", "rgb(79, 48, 23)", "rgb(5, 2, 0)", 200, 10);

    let megan = new Friend("Megan Rocky", 16, true, "rgb(0,0,0)", "rgb(209, 181, 140)", "rgb(0, 60, 0)", 260, 120);

</script>

    </body>

</html>

It's a nice start, but it's all so static- unmoving. In the next section, let's try to move something around!

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/5_Creating_visuals.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/5_Creating_visuals.html)

# 6. Moving things around on screen (sprites)

Let's first start by going back down to just one friend, say Timmy, and removing all the others (I’m also going to remove the paragraph tag in the html for now, so it won’t be in screenshots):

let timmy = new Friend("Timmy Smith", 16, true, "rgb(0,0,255)", "rgb(209, 181, 140)", "rgb(125, 60, 34)", 20, 20);

Now let's move Timmy to where Megan was on the bottom right:

timmy.x_pos = 260;

timmy.y_pos = 120;

You'll see that Timmy doesn't actually move to where we placed him. That's because in the constructor, we position him first, then we draw him. So, all we have to do is redraw him, right? Luckily we put all friends drawing actions into one convenient function "DrawFriend()", so let’s call that now for Timmy:

timmy.DrawFriend();

Now if you look, you'll see 2 Timmy's, one where he was originally, and one in the new position, but we only have one Timmy, so what happened?

![](Images/image00474.jpeg)

## How canvas drawing works

You have to think of the canvas like a piece of paper. If you draw a square in one corner, then draw in the other- you'll have 2 squares, even if you draw the same square in both spots. Even though we moved the "object" that is Timmy, we actually drew him 2 times, but we actually want to erase the first drawing, before we draw the second one.

So, we'll create a function to clear the canvas before we draw Timmy the second time.

### Canvas Clear

Before drawing Timmy add:

let my_canvas = document.querySelector("canvas");

let draw_context = my_canvas.getContext("2d");

let ctx = draw_context;

let background_color = "rgba(255,255,255, 1)";

ctx.fillStyle = background_color;

ctx.fillRect(0, 0, my_canvas.width, my_canvas.height);

timmy.DrawFriend();

Now if you try it, you'll see the old Timmy was erased before the new Timmy was drawn. If we want to keep moving Timmy, we'll want to move the clearing code into its own function, so we can call it multiple times easily. So, create a new function below our Friend class:

function ClearCanvas(ctx, background_color)

{

    ctx.fillStyle = background_color;

    ctx.fillRect(0, 0, my_canvas.width, my_canvas.height);

}

Since the function is outside of a class, in JavaScript we have to say "function" before the function name. We're also going to pass the draw context to the function, so we don't have to get the canvas and context inside the function. Additionally, we're going to pass over a background color, so we can change it to whatever background we want.

So now we'll change the previous code to:

let my_canvas = document.querySelector("canvas");

let draw_context = my_canvas.getContext("2d");

let ctx = draw_context;

ClearCanvas(ctx, "rgba(0,0,255,255)");

timmy.DrawFriend();

When we call the "ClearCanvas" function, we're passing over the canvas drawing context, and a string (in quotes) for an rgba value, which stands for "red, green, blue, alpha". Alpha is how transparent or see through something is. 0 is completely see through/ we can't see it, 255 is completely opaque, or solid/ not see through at all, and any value in between is partially see through (128 being half way between, so 50% see through).

So, we passed over 0 red, 0 green, 255 or max blue, and 255/max for alpha/ setting it to not see through at all.

We could have passed over "rgb(0,0,255)", and it would have done the same thing (automatically filling in 255 for alpha), but I wanted to show that we could use partially transparent colors.

If you run this, you’ll see that Timmy did move, but the page loads up so fast, we never see the original Timmy before he moves.

So, we'll want to make it so he moves slowly, over time to the right, instead of all at once. In the next section, we'll learn how to slowly move him, which will make it look like he's animating across the screen.

## How Animation/ moving pictures works

What we want to do is move Timmy a little bit, but moving all the time.

The way computers and TV's make things move is that they show still images- but very, very fast, so they look like they are moving. Typically, the screen or TV will update the image on the screen 30-60 times in one second. These still images are called "frames", and how fast they change is called "frames per second", or fps.

When things look slow, or stuttering, that is when things are being displayed at low frames per second. The smoother they look, the higher the frames per second, but the human eye can only see so many frames per second, before the images look like they are moving smoothly. For movies and TV, they are only displayed at 24fps, but for games you typically want at least 30fps, and 60 or more can look slightly smoother.

So, what we'll do is try to draw over and over again, as fast as our device will let us

## Updating the drawing fast enough to make an animation

JavaScript has a built-in function to call any function you provide, whenever it is able to update the screen, so that you can draw your next frame. This is "window.requestAnimationFrame(my_update_function(current_time_in_ms) );"

All you will do is call this, passing what function you want it to call whenever it can render a frame, which will also automatically pass to your function a time in milliseconds (ms- 1000th of a second, so 1000 of these make up one second).

You will eventually want to use that time to figure out how much time has passed since the previous update, so you can move things on the screen at certain speeds, regardless of if it's running on a system doing 10fps or 60fps.

So, we'll add before creating a friend:

function Update(time_ms)

{

    console.log("Update: "+time_ms);

    window.requestAnimationFrame(Update);// have to request another frame, which will call this function again when it can

}

window.requestAnimationFrame(Update); //request one frame

Our function "Update" will be called whenever the browser can allow it to draw a new frame. It will also pass a time in milliseconds, which once it calls it a 2nd time, we can find how much time it took to ask for the second frame. But we also have to call it again inside our update function, so it can wait for the next frame, and call our function again. This will call out Update function over and over again, as long as the browser can render a frame, which we can use to update our game.

When you run that, you'll see that it outputs the time in milliseconds (ms) to the console, and keeps increasing over time.

We now have a basic update loop, and can tell the time of each frame.

But we need to take it one step further, and see how much time has passed between each frame- which will then allow us to move things on screen relative to the actual time that has passed, which will let objects move at the same speed on low and high frames per second.

If we move an object at 10px each frame, and it's running at 1fps, it will only move 10px in 1 second. But if it's running on a faster computer at 60fps, then it will run 60 frames/ updates in 1 second, each frame moving 10px, so 600px! To make it move consistently across devices, you need to find the time between updates also known as the difference in time, or delta time.

So, update the code to:

function Update(time_ms)

{        

    let frame_delta_ms = time_ms - last_time_ms; // #2 going to find the delta/difference in time between the last frame (initially 0) and the current time

    let delta_s = frame_delta_ms / 1000; //since time is in ms (1 /1000 s), to convert to seconds, divide by 1000, exp: 2000ms/ 1000 = 2s

    let fps= 1 / delta_s; //we can convert from seconds/ frame (delta_s) to frames/ second by flipping it dividing 1 by it- 1/ (seconds/frame) = frame/ second= fps

    frame_delta_ms = frame_delta_ms.toFixed(2); //going to round to just 2 decimal places using toFixed(2)

    //so.... toFixed which rounds a number, returns a string instead of a number.... so have to now turn it back into a number... JavaScript... otherwise it counts as adding strings together- so instead of 5+5 = 10, 5+5=55 -which is to 5s stuck together, instead of added

    frame_delta_ms = parseFloat(frame_delta_ms);

    fps = fps.toFixed(2);

    console.log("Update: delta time: "+frame_delta_ms+", fps: "+fps);

    last_time_ms = time_ms;

    window.requestAnimationFrame(Update);

}

let last_time_ms = 0; // #1 "creating last_time_ms" first, which will exist outside of the function, and record what the last time update was called

window.requestAnimationFrame(Update);

First, we declare a variable (last_time_ms) outside the function (on the bottom), so it will exist outside of the function/ will keep its value after the function runs each time.

Next we call the function "window.requestAnimationFrame", passing it our soon to be created "Update" function.

We create the “Update” function, but say that it will be passed something when "window.requestAnimationFrame" calls it. That will be a time in ms, since the page began loading. We don't really need this, but by storing it at the end of each frame, we can take the difference between the time the last frame was run, and the current one, which will give us a time difference- how long each frame is currently taking to be drawn.

This delta time/difference in time is a bit hard to understand, so we first convert it to seconds by dividing the milliseconds (1ms = 1/1000s) by 1000, converting it into seconds (the time difference in seconds, which will be a small decimal, such as 0.0166).

Now we have "seconds /frame", but we want to flip it upside down to become "frame/second" or fps. 1 divided by any fraction will flip it upside down, so we do 1/delta_s to have fps.

We round it to 2 decimal places, because seeing 25 decimal places isn't very readable. The function “toFixed” is built into JavaScript, belonging to the number type of variable (so we just run it on our number to round it). For some odd reason, rounding a number in JavaScript returns a string. It might look like a number, but if you try to add it/ use it, it will be combined as a string, not as a number, so will cause some strange bugs. For instance if it’s 5, adding 5+5= 10 as a number, but 5+5 as strings are 2 strings stuck together- or 55\. So we have to convert our rounded number back into a number using “ParseFloat” to parse it back into a number- a float being one that allows decimals.

We can then console.log out the “delta_ms”, and converted to fps, so we can check if fps is in a normal range (0-60+fps).

We then store the current frame time, so we can find the difference next time, and then ask for another frame (whenever it can let us run the Update function again)

## Finally animating!

So now we actually have a basic program/ game loop, we can then do things in there over time, which will make it look like objects are smoothly moving.

Above the “Update” function, add a new function:

function UpdateGame(delta_ms)

{

    timmy.x_pos=timmy.x_pos+5; //moves timmy 5 pixels to the right each frame/ time the function is called

    ClearCanvas(ctx, "rgba(0,0,255,255)"); //clears the canvas, so we don't get "ghosting"

    timmy.DrawFriend(); //re-draw Timmy

}

In Update, we'll call our UpdateGame function under the console.log:

...

console.log("Update: delta time: "+frame_delta_ms+", fps: "+fps);

UpdateGame(frame_delta_ms);

…

And lastly, we'll change our code out for drawing Timmy, getting rid of the movement code:

let my_canvas = document.querySelector("canvas");

let draw_context = my_canvas.getContext("2d");

let ctx = draw_context;

let timmy = new Friend("Timmy Smith", 16, true, "rgb(0,0,255)", "rgb(209, 181, 140)", "rgb(125, 60, 34)", 20, 20);

If you refresh the page, you can see Timmy moving quickly across the screen! Refresh multiple times to see it if he leaves the screen too fast.

## Emulating low FPS to show movement without account for frame time

Above we're just animating by moving 5 pixel every frame, but at 60fps, this is 300 pixels(5px/frame * 60 frames/ second= 300px/second) moved every second (Timmy is 50 pixels wide, so almost 6 Timmy widths moved every second). But if we're on a slow device that's only running at 10fps, that means it will only move 50 pixels in a second, so the game will actually move slower, characters will move slower, and people will get super speeds on 120fps devices!

So, we want to change it to move based on how much time has passed, not how many frames have passed. This will make characters "teleport", or move less smoothly on low FPS devices, but will allow people to play the game at the same speed on all sorts of devices.

We'll first try to slow down the fps so we can see how it would move right now on a slower device.

In the "Update" function, change the bottom line to:

setTimeout( function(){window.requestAnimationFrame(Update) }, 100);

// window.requestAnimationFrame(Update);

We commented out the requestAnimationFrame function call, and changed it out with another function above it. "setTimeOut" has a function with no name inside of it, which has our "requestAnimationFrame" function call inside it. Then after the comma, we pass the next parameter, which tells the timeout function how long to wait before it calls the blank function (which will then call our Update function).

We wanted about 10fps, so we used a delay of 100ms, divided by 1000 = 0.1s / frame, for 1/(0.1s/frame) = 10frames/s. It should be about 10fps, but either way you'll see the character moving a lot slower/ taking longer to make the same distance.

So next we'll add time to our movement, so it moves based on the time passed, and not the frame passed, so he moves the same distance on all devices in a given time!

## Animating with deltaTime in ms

Math warning:

You don't have to know how to do this next section- you can get by, by just plugging in values until you are happy with a movement speed. This is only for if you REALLY want to make an object move a certain number of pixels in a given number of seconds. Otherwise skip the math section, and you can just plug in numbers to see what "feels" right (which is usually good enough for what you’re trying to achieve).

Math Section:

Let's say we want to move Timmy 50 pixels(px) every second. We'll assume we're testing on a 60fps (or 1/60 = 0.0166sec/frame *1000= 16.66ms/frame) or 16.66ms delta time (you can assume any fps, it should all workout)

So, each update, we should move him:

50px / (60f / s).

If we want to make it easy, you can change it to multiplication, but have to flip the second fraction

50px * (1s / 60frames) = 0.833 px s /frames

Normally we move by doing:

obj.x_pos = obj.x_pos +speed*delta_time_ms;

So how far something moves in a frame is:

pixels we're adding / distance moved in a frame = speed*delta_time_ms

So, filling in with our 2 values above, we can solve for speed:

0.833 px s /frames = speed * 16.66ms/frame

(0.833 px s /frame ) / 16.66ms = speed

speed = 0.05 px /frame

So to move him 50pixels (1 head width) every second, you have to multiply the time it took to render the frame (whether it be 16ms or 100ms) by 0.05206, and he'll move the same distance in the same time, regardless of frame rate.

Or you could just play with the value until you get one you like!

End of math

So, in "UpdateGame" change it to:

// timmy.x_pos=timmy.x_pos+5;

timmy.x_pos=timmy.x_pos+delta_ms*0.05206;

Now we're moving Timmy's x position based on the time it took for the frame to render (16ms @60fps, 100ms @10fps), multiplied by how fast we want him to move each frame (*0.05206).

Refresh the page and roughly count how long it takes Timmy to exit the page (default canvas size is 300px, he starts at 20px, so 280px left, Timmy should move 50px every second, so (280px)/(50px/s) = ~6seconds.

You can count to see roughly how fast he moves till he is offscreen. To test if he moves at the same speed in low FPS and high FPS, change back and forth in the bottom of the Update function between (roughly 10fps):

setTimeout(function(){window.requestAnimationFrame(Update)}, 100 );

// window.requestAnimationFrame(Update);

And (roughly 60fps+ if your device supports it):

// setTimeout(function(){window.requestAnimationFrame(Update)}, 100 );

window.requestAnimationFrame(Update);

So now we're moving him the same amount, regardless of the frame rate, which is the way all games seem to handle this issue.

Let’s add a little UI just to see the framerate on screen.

## Adding UI for FPS - styling

First we want to add the html to display FPS. Change the canvas tag to:

<div id="game_container">

    <canvas></canvas>

    <p id="fps">120</p>

</div>

This will create a "p" tag (paragraph, for text), with an id of "fps". Giving it an id will allow us to target this specific "p" tag from both CSS and JavaScript easily, since we're likely to have more text UI elements in the future (for things like health, number of items, speech, etc).

We also wrap both the "canvas" and "p" tag in a "div" tag, with its own id of "game_container", since it will contain our main canvas tag and the fps paragraph.

Div is short for "division", which really just means "a container that I can position + put stuff in, which isn't meant to contain only text".

This just adds the html for it to the page, but by default, the canvas and "p" tag will just be placed next to each other, instead of the fps on top of our canvas. So, we also have to add to our CSS area to position and style them correctly:

We're going to use some CSS to fix some issues. Inside your head tag, add the below:

<style>

*

{

    margin:0;

    padding:0;

    font-family: Verdana, Geneva, Tahoma, sans-serif;

}

#game_container

{

    position: relative;

    display: inline-block;

}

#fps

{

    position: absolute;

    top:10px;

    right:10px;

    color:white;

    font-weight: 900;

    font-size: 20px;

    text-shadow:2px 2px 0 black,

        2px -2px 0 black,  

        -2px -2px 0 black,

        -2px 2px 0 black;

    pointer-events: none;

}

</style>   

This is a "style" tag, which uses CSS. You can put it in the head of your page to target/style specific elements on the page.

In this case, we're going to target asterisk ( * ) which means all elements on the page. Margin is the spacing on the outside of html elements/tags, and padding is the spacing inside of the tags. Most browsers will add some margin and padding to different elements of the page, but we don't want any here, or there will be ugly scroll bars over our canvas, as our canvas will be larger than the page.

We changed the font family on everything to be Verdana, which uses a standard way of also falling back to other fonts on systems that don't have it. Geneva if it can't find Verdana, Tahoma if that can't be found, and lastly any "sans-serif", meaning "no serif"/ little extra marks on letters that some fonts have, which should be found on any system.

To target an HTML element by an id, we have to put a number sign (#) before the id, for it to know that we're trying to target it by an id (and not just a tag type, or later on, a class type- there are lots of different ways to target HTML elements).

So, we target the "game_container", and set the position to "relative". This doesn't do anything to this element directly - but says any child element inside of it will be positioned relative to this element, instead of based on the entire page, which is the default. That way we can position the fps on the top right corner of this element, instead of the top right of the entire page.

We set its display to "inline" for now- so that it grows only as big as the content inside of it- so only as big as the canvas tag. If we don't, it will be displayed as a "block" instead- which will take up the entire width of the page, and put our fps outside of our canvas area.

Next, we target the "fps" id. We position it absolute- which means that other elements won't affect it/ move it around like normal. So, we can put it anywhere on the page- even on top of our canvas element! We'll also position it from the top, and the right side of its container (game_container), offset by 10px each, so it pushes it a little bit away from the top and right side.

We also made it white, since our background is blue, and it's hard to see if it is set to normal black. We made it as bold as possible by setting font-weight to 900- you can set it from 100 to 900, increasing by 100 each time. We set it to font size of 20px, and made a text-shadow that is made up of 4 different shadows- to the right by 2px, and up by 2px, then one to the right 2px, but down to -2px, and the other 2 sides- so there are 4 text shadows surrounding the text on all corners.  This makes a black "stroke"/ line around our white text, which will make it readable even on a white background. That way, no matter what background we have, we should be able to read the FPS text.

Lastly, since we don't want the FPS text blocking us from being able to click on the part of the canvas it will cover, we set "pointer-events: none;", so it won't be clickable.

Now let's actually connect this text to our JavaScript, so it can output the actual FPS to the screen.

## Connecting FPS text to JavaScript

We were already seeing the actual FPS in the code, and in the console, but not on the screen before, let's connect the two.

Below all your functions, where we start declaring our variables outside the functions/ classes (also known as "global" variables), add this new top line above the existing “last_time_ms”:

let fps_txt_element = document.getElementById("fps");

let last_time_ms = 0; 

...

Here, we're getting an element on the page with the id of "fps" (our fps text we created in the last section). Next, we assign it to the variable name "fps_txt_element", because we'll want to use it every frame to update the current FPS.

Next, we'll actually want to update/ change the text out. In your "Update" function, add the following line:

fps_txt_element.innerHTML=Math.round(fps);

console.log("Update: delta time: "+frame_delta_ms+", fps: "+fps);

…

Here we're just using the fps_txt_element variable we created above (which is the paragraph tag with the id of "fps" on the html page), and we change out its innerHTML (which we initially had set to "120") with our fps variable we declared right above. We'll also call "Math.round()" to round our fps to a whole number, instead of a decimal, since it's harder to read with the decimal changing constantly.

If you check out the page, you'll see our fps text updating in real-time, when the frame updates!

You can check it changes by switching between the 2 below lines in the “Update” function:

setTimeout(function(){window.requestAnimationFrame(Update)}, 100 );

// window.requestAnimationFrame(Update);

// setTimeout(function(){window.requestAnimationFrame(Update)}, 100 );

window.requestAnimationFrame(Update);

The first line artificially delays the next call of the "Update" function by 100ms (0.1s), which slows it down to around 10fps. The second is our actual update call, which should run a lot faster than that (60fps on my screen).

When you're finished, comment out the first line, and keep the second, and we can move forward!

We now can see the FPS on screen, which is our first piece of UI. It will also help us quickly see if we do something wrong, that severely brings down the FPS on our system. We can also comment out the console.log logging out the FPS and deltatime in “Update”, so we don't clog up our console (and leave it clear to debug statements, warnings or errors).

// console.log("Update: delta time: "+frame_delta_ms+", fps: "+fps);

Let's finally make the game take up the full size, so it's not the default little 300x150 canvas anymore.

## Making the canvas take up the entire screen

Let's modify our canvas to actually take up the full screen.

First remove the style attribute with the border from your canvas tag:

<canvas></canvas>

Next modify your style tag to add canvas, and modify "game_container":

canvas

{

    display: block;

}

#game_container

{

    position: relative;

}

Our canvas element by default is set to "inline"- meaning it allows it to be placed in the middle of a sentence/ inside a line, and allows other things to be placed on both sides. But we instead want it to be displayed like a "block"- have it not allow other stuff to be placed beside it, take up the entire width, which will again make sure we don't get ugly scroll bars on top of our game.

We also get rid of the code setting our "game_container" to be inline-block- because otherwise we'll get scrollbars, and now the canvas is going to be the full width and height of the page, so the FPS will be positioned correctly.

We still have to set the canvas to be 100% of the width of our window and the height. If we use CSS to do it, it just stretches out our canvas in an ugly way- scaling up everything we draw in it, without giving us more room to draw.

That might be fine when we're done with our game- to scale it up or down to any resolution, and have the game draw the same way. But we want to take advantage of the extra room we have, so we're going to change the size of the canvas using the width and height attribute on the tag, not the width and height of the style/CSS.

To do this, we're going to add the following code above where we create our friends in our JavaScript:

//change the width and height of the canvas to be the same size as the window

my_canvas.setAttribute('width', window.innerWidth);

my_canvas.setAttribute('height', window.innerHeight);

let timmy = …

This will just change the width and height attribute of the canvas tag (instead of the style width and height) to the inner height/width of the window (the height and width without scrollbars).

What this does is actually change the resolution (how many pixels) the canvas "image" has, and allows us to draw more pixels in the canvas than we could before.

By default, when you create a canvas tag without a width and height set, it creates what you can draw on with a 300 pixel width, and 150 height resolution. This is a good safe, small size, that you can see on any screen, but would be pretty blurry if you scaled it up on most screens (1080p standard screens are 1920 width x 1080 height).

If we had instead set it with CSS, it would scale up the 300x150 image, making it 10x blurrier on a 1080p screen. We would still only have a 300x150 area to draw in, so it wouldn't help us out with what we're trying to do.

## Fixing issue with resizing screen

If you try resizing your window, to make it smaller, you'll see that you get scroll bars. This is because we set the canvas size to whatever the window is when we first load up- so if the window then gets smaller, the canvas will just remain the original size, and be larger than the page.

So, we just have to detect when the screen size changes, and resize the canvas at the same time.

Above where we declare Timmy, add:

let last_width=window.innerWidth;

let last_height=window.innerHeight;

We'll store what the last/current width and height of the window/ page is, so that we can check if it changed in our update function (that runs every frame, where we can catch if the size has changed).

Next create a new function under the Update function:

function Resize()

{

    if(window.innerWidth != last_width || window.innerHeight != last_height)

    {

        my_canvas.setAttribute('width', window.innerWidth);

        my_canvas.setAttribute('height', window.innerHeight);

        last_width=window.innerWidth;

        last_height=window.innerHeight;

    }

}

First, we created a function like normal. But then we declare an "if" statement. This lets you check if something is true, and to run the code inside if it is.

We want to check to see when the window/page “innerwidth” is not equal to the value of the “innerwidth” we stored earlier.

The characters "!=" mean "not equal". The characters "||" mean "OR". So, in plain English we are doing:

IF window.innerWidth "IS NOT EQUAL TO" last_width "OR IF" window.innerHeight "IS NOT EQUAL TO" last_height)

We check to see if the width we stored is no longer equal to the current window width, meaning they resized the width (or rotated their phone), but also if the height might have changed. If either one is true, then we'll run the code inside it.

If so, we then set the canvas to the new width and height, which unfortunately Also causes the canvas to be erased whenever the width and size are changed (because it's creating a new image of that size to draw to).

Finally, we store what this width and height are now, so we can then check if it ever changes again in the future.

Now we actually need to call this resize function, which checks if the window size has changed, and resizes the canvas. Because the canvas texture gets re-created, and is blank initially, we want to resize right before we draw on the canvas, so that if it did get resized, it will immediately get drawn on afterwards.

In Update, before calling UpdateGame:

…

Resize();

UpdateGame(frame_delta_ms);

…

Now if you resize the window, you'll see the game updates and resizes perfectly!

## Full code listing

The full code is becoming much longer now, but I included it so that you can error check if anything is going wrong. You can also find the code up on the books github page as “6_Moving_sprites.html”.

WARNING: I’m not indenting the html tags fully, because otherwise we’d have too much white space at the front of the code listing. But you should always indent as you go deeper a HTML tag, object, etc, for readability (and some languages like python require indentation, and remove all curly brackets, so it’s good practice)

<html  lang="en">

<head>

 <meta  charset="UTF-8">

 <meta  http-equiv="X-UA-Compatible"  content="IE=edge">

 <meta  name="viewport"  content="width=device-width, initial-scale=1.0">

 <title>My JavaScript Game</title>

 <style>

 *

        {

 margin:0;

 padding:0;

 font-family: Verdana, Geneva, Tahoma, sans-serif;

        }

 canvas

        {

 display: block;

        }

 #game_container

        {

 position: relative;

        }

 #fps

        {

 position: absolute;

 top:10px;

 right:10px;

 color:white;

 font-weight: 900;

 font-size: 20px;

 text-shadow:2px  2px  0  black,

 2px  -2px  0  black, 

 -2px  -2px  0  black,

 -2px  2px  0  black;

 pointer-events: none;

        }

 </style> 

</head>

<body>

 <div  id ="game_container">

 <canvas></canvas>

 <p  id="fps">120</p>

 </div>

 <script>

 class  Friend

        {

 constructor(their_name, their_age, their_loves_spinach, their_eye_color, their_skin_color, their_hair_color, their_x_pos, their_y_pos)

            {

 this.name = their_name;

 this.age = their_age;

 this.loves_spinach = their_loves_spinach;

 this.eye_color = their_eye_color;

 this.skin_color = their_skin_color;

 this.hair_color = their_hair_color;

 this.x_pos = their_x_pos;

 this.y_pos = their_y_pos;

 console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

 console.log("And some facts about them, eye color: "+this.eye_color+", skin color: "+this.skin_color+", hair color: "+this.hair_color+", x and y: "+this.x_pos+", "+this.pos_y);

 this.DrawFriend();

            }

 SayHi()

            {

 console.log("Hi, my name is "+my_new_friend.name +", my age is: "+my_new_friend.age+", and do I love spinach? "+my_new_friend.loves_spinach+".");

            }

 DrawFriend()

            {

 // this is where we will start drawing our friend

 //-------------------get the canvas stuff we need to be able to draw-------------------

 let  my_canvas = document.querySelector("canvas");

 let  draw_context = my_canvas.getContext("2d");

 let  ctx = draw_context;

 //-------------------draw the head-------------------

 // define width and height of the head

 let  width_head = 50;

 let  height_head = 60;

 ctx.fillStyle = this.skin_color;

 ctx.fillRect(this.x_pos, this.y_pos, width_head, height_head);

 //-------------------draw the eyes-------------------

 // define width and height of the eyes

 let  width_eyes = 10;

 let  height_eyes = 15;

 // set the fill style:

 ctx.fillStyle = this.eye_color;

 // define how offset the eyes should be from the left and right side of the head

 let  eye_x_offset = 10;

 // define how offset the eyes should be from from the top of the head

 let  eye_y_offset = 15;

 //-------------------draw the left eye, left corner, top , width and height-------------------

 ctx.fillRect(this.x_pos+eye_x_offset, this.y_pos+eye_y_offset, width_eyes, height_eyes);

 //--draw the right eye--

 //a lot more complicated- have to find right side of head (x_pos+width_head), then minus out the width of eye + x offset of eye to position the left side of the eye away from the right side of the head

 let  right_side_of_head = this.x_pos+width_head;

 let  right_eye_x_pos = right_side_of_head - width_eyes-eye_x_offset;

 ctx.fillRect(right_eye_x_pos, this.y_pos+eye_y_offset , width_eyes, height_eyes);

            }

        }

 function  ClearCanvas(ctx, background_color)

        {

 ctx.fillStyle = background_color;

 ctx.fillRect(0, 0, my_canvas.width, my_canvas.height);

        }

 function  UpdateGame(delta_ms)

        {

 // timmy.x_pos=timmy.x_pos+5; //moves timmy 5 pixels to the right each frame/ time the function is called

 timmy.x_pos=timmy.x_pos+delta_ms*0.05206;

 ClearCanvas(ctx, "rgba(0,0,255,255)"); //clears the canvas, so we don't get "ghosting"

 timmy.DrawFriend(); //re-draw Timmy

        }

 function  Update(time_ms)

        {       

 let  frame_delta_ms = time_ms - last_time_ms; // #2 going to find the delta/difference in time between the last frame (initially 0) and the current time

 let  delta_s = frame_delta_ms / 1000; //since time is in ms (1 /1000 s), to convert to seconds, divide by 1000, exp: 2000ms/ 1000 = 2s

 let  fps= 1 / delta_s; //we can convert from seconds/ frame (delta_s) to frames/ second by flipping it dividing 1 by it- 1/ (seconds/frame) = frame/ second= fps

 frame_delta_ms = frame_delta_ms.toFixed(2); //going to round to just 2 decimal places using toFixed(2)

 //so.... toFixed which rounds a number, returns a string instead of a number.... so have to now turn it back into a number... JavaScript... otherwise it counts as adding strings together- so instead of 5+5 = 10, 5+5=55 -which is to 5s stuck together, instead of added

 frame_delta_ms = parseFloat(frame_delta_ms);

 fps = fps.toFixed(2);

 fps_txt_element.innerHTML=Math.round(fps);

 // console.log("Update: delta time: "+frame_delta_ms+", fps: "+fps);

 Resize();

 UpdateGame(frame_delta_ms);

 // setTimeout( function(){window.requestAnimationFrame(Update) }, 100);

 window.requestAnimationFrame(Update);

        }

 function  Resize()

        {

 if(window.innerWidth != last_width || window.innerHeight != last_height)

            {

 //change the width and height of the canvas to be the same size as the window

 my_canvas.setAttribute('width', window.innerWidth);

 my_canvas.setAttribute('height', window.innerHeight);

 last_width=window.innerWidth;

 last_height=window.innerHeight;

            }

        }

 let  fps_txt_element = document.getElementById("fps");

 let  last_time_ms = 0; // #1 "creating last_time_ms" first, which will exist outside of the function, and record what the last time update was called

 window.requestAnimationFrame(Update);

 let  my_canvas = document.querySelector("canvas");

 let  draw_context = my_canvas.getContext("2d");

 let  ctx = draw_context;

 let  last_width=window.innerWidth;

 let  last_height=window.innerHeight;

 let  timmy = new  Friend("Timmy Smith", 16, true, "rgb(0,0,255)", "rgb(209, 181, 140)", "rgb(125, 60, 34)", 20, 20);

 </script>

</body>

</html>

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/6_Moving_sprites.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/6_Moving_sprites.html)

# 7. Adding player controls

It's kinda boring with our character just moving to the right and offscreen. So, let’s make it so we can control them!

Since these days it's safe to assume someone either has a touch screen, or a mouse, but might not have access to arrow keys/ using WASD to move, we'll make our character move based on where they tap on the screen.

## Get touch/click position

First, we need to tell if they clicked/ touched on the canvas, and where they did it. We'll want to handle clicks and touches in the same way, so add the following:

At the bottom of our functions, below "function Resize()"

function SetupInput()

{

    my_canvas.addEventListener("mouseup", MouseUp);

    my_canvas.addEventListener("touchend", TouchUp);

}

This created the function "SetupInput", which when called, will add an "event listener" onto the “my_canvas” element.

SIDE NOTE: For a full list of potential events to listen for, you can look at: [https://www.w3schools.com/jsref/dom_obj_event.asp](https://www.w3schools.com/jsref/dom_obj_event.asp) (or google "JavaScript events").

The two events we are interested in are "mouseup", which is when someone had the mouse button down, but let go of it (a click). We also want the same thing for touches, so use "touchend", which is when someone was touching the screen, but stopped.

They will each call their own function "MouseUp" and "TouchUp", which will convert the touch and mouse "events" they send to those functions, to points we can use to move our character to.

Next, above that, add the functions:

function MouseUp(event)

{

    let x_dest = event.clientX;

    let y_dest = event.clientY;

    console.log("Mouse up at: x: "+x_dest+", y: "+y_dest);

    MoveMyPlayer(x_dest, y_dest)

}

function TouchUp(event)

{

    let x_dest = event.changedTouches[0].clientX;

    let y_dest = event.changedTouches[0].clientY;

    console.log("Touch up at: x: "+x_dest+", y: "+y_dest);

    MoveMyPlayer(x_dest, y_dest)

}

“MouseUp” and “TouchUp” will be called from the event listeners/ they'll each get the x and y position of the click/ touch, and assign it to the variables "x_dest" and "y_dest", as in destination (the destination of where we’ll want the player to move to).

The clientX and Y is just the touch/ click position, relative to the top left of the screen.

The touch function is a little more complicated. We have to look at the "changedTouches" instead of the "touches", because since it is when the person stops touching the screen, if we had checked "touches", it would have shown nothing. We add "[0]" to the end, which checks only the first touch point- since most screens support up to 10 fingers being able to touch the screen at the same time.

SIDE NOTE: The variable "changedTouches" lets you look at all the fingers touching the screen, so it is a list of fingers, or in programming terms, an "array" of finger positions. We'll touch more on arrays/ being able to store multiple things in one variable name later.

Finally, we'll add a new function above these ones:

function MoveMyPlayer(x_dest, y_dest)

{

    //move my_player/ timmy to the destination clicked

    console.log("Moving my player to destination: x: "+x_dest+", y: "+y_dest)

 if(timmy.SetDestination) //just checking to see if the "SetDestination" function exists yet- which doesn't at this point

 timmy.SetDestination(x_dest, y_dest);

}

This just gets the x and y destination from either "TouchUp" or "MouseUp", and logs it out for now.

Lastly, you need to call the function. Below where you create timmy, add the function call for "SetupInput":

let  timmy = new  Friend("Timmy Smith", 16, true, "rgb(0,0,255)", "rgb(209, 181, 140)", "rgb(125, 60, 34)", 20, 20);

SetupInput();

If you try it, you should see the mouse click position being logged out from the functions, both when using a touch screen or a mouse. If you click on the very top left of the game, it should output a x and y position of close to "0,0", and if you click on the bottom right, it should give a much bigger number/ the size of your game (like 480x800 if you're in portrait mode, on that resolution screen).

We’ll also set our player destination here, but still need to create the function in our friend class.

## Move character to click position

Now that we know where we want to move to, let's move our character there, when the screen has been clicked/ touched!

This will be a bit long, since we'll be moving him until he gets to his destination, and checking + moving in both x and y direction.

So, in our "Friend" class "constructor", add the new variables on the bottom, above the console.log statements:

//for moving

this.x_dest=0;

this.y_dest=0;

this.moving_x=false;

this.moving_y=false;

this.move_speed= 0.2;

This defines an x and y destination for our character to move to, whether he's moving in the x or y direction, and how fast we want him to move (I set it to 0.2 after testing, and deciding what I thought was a good move speed, but a good default is just "1", and raising/ lowering it from there).

Next, we need to define the function to set the destination for the friend, when the screen is clicked/ touched. So, add under the function "SayHi":

SetDestination(x_dest, y_dest)

{

    this.x_dest=x_dest;

    this.y_dest=y_dest;

    this.moving_x=true;

    this.moving_y=true;

}

This will just get the mouse/ touch point, set it to the friends x and y destination, and set that it is now going to be moving.

Next, we'll actually make the functions to move him each frame if he has a destination set. This is a long one, because we need to check if he's reached his destination, in both directions:

SIDE NOTE: Adding to a variable using "operators"+,-, +=, +-, ++, --:

In the upcoming code, I use some shorthand code that you may not have seen before.

If you want to add something to a variable, there are two ways of doing it.

The longer way:

let some_variable = 5;

some_variable = some_variable +12; // so 5+12

console.log(some_variable); //some variable is now 5+12= 17

Or a shorter way:

let some_variable = 5;

some_variable += 12; // same thing- some variable +=, meaning "add to itself"

console.log(some_variable); //some variable is now 5+12= 17

So "+=" just means "add to the variable the amount on the right side"

ADDITIONAL INFO:

Likewise, you could also do minus:

some_variable = some_variable -3; // so 5-3

console.log(some_variable); //some variable is now 5-3=2

some_variable -= 3; // so 5-3

console.log(some_variable); //some variable is now 5-3=2

And there are additional operators for just adding or subtracting just 1 at a time (since you can go through items 1 at a time a lot in programming):

Longer way:

some_variable = some_variable +1; // so 5+1

console.log(some_variable); //some variable is now 5+1= 6

Shorter way:

some_variable++; // so 5+1

console.log(some_variable); //some variable is now 5+1= 6

Longer way:

some_variable = some_variable -1; // so 5-1

console.log(some_variable); //some variable is now 5-1= 4

Shorter way:

some_variable--; // so 5-1

console.log(some_variable); //some variable is now 5-1= 4

You're free to use either method, but once you become more used to the shorter way, and can easily recognize it, it's faster and can be more readable (and is the method I’ll be using).

END OF SIDE NOTE

So, in your friend class, add the following below the “DrawFriend” function:

Update(delta_ms)

{

    this.MoveToDest();

}

MoveToDest(delta_ms)

{

    if(this.moving_x)

    {

        if(this.x_dest>this.x_pos)

        {

            this.x_pos+=this.move_speed*delta_ms;

            if(this.x_pos>=this.x_dest)

            {

                this.x_pos=this.x_dest;

                this.moving_x=false;

            }

        }

        else //x_dest < x_pos -so need to move to the left/ -x

        {

            this.x_pos-=this.move_speed*delta_ms;

            if(this.x_pos<=this.x_dest)

            {

                this.x_pos=this.x_dest;

                this.moving_x=false;

            }

        }

    }

    if(this.moving_y)

    {

        if(this.y_dest>this.y_pos) // if dest is greater, move him down, where y increases

        {

            this.y_pos+=this.move_speed*delta_ms;

            if(this.y_pos>=this.y_dest)

            {

                this.y_pos=this.y_dest;

                this.moving_y=false;

            }

        }

        else //y_dest < y_pos -so need to move upward/ -y

        {

            this.y_pos-=this.move_speed*delta_ms;

            if(this.y_pos<=this.y_dest)

            {

                this.y_pos=this.y_dest;

               this.moving_y=false;

            }

        }

    }

}

Here, we first create our own "Update" function inside of "Friend", so it can be updated from the main game on its own, and can do more complicated things in the future.

Next, we'll create the "MoveToDest" function, to check if we have an x or y destination set, and to move it depending on where the destination is. We basically just copy the same movement code for moving in the x direction as we do for moving in the y direction.

First we check if it is moving in the x_dir : " if(this.moving_x)". If it is, we'll look into how to move it, afterwards, we'll check if it has a destination set in the y direction.

But say it is moving in the x_direction, we'll check if the x_dest is greater than the current position "if(this.x_dest>this.x_pos)", which means our x_destination is to the right, so we need to add some value to our current position to move it to the right "this.x_pos+=this.move_speed*delta_ms;".

If instead the x_dest is to the left, it will be less than the current x_pos (else //x_dest < x_pos -so need to move to the left/ -x), so we'll do the same thing, but subtract based on the speed "this.x_pos -= this.move_speed*delta_ms;".

So that will allow us to move him right or left, but we'll also check if he needs to move up or down, and move him the exact same way, changing out x for y, but otherwise doing the exact same thing.

Finally, we need to change the “UpdateGame” code to not move our friend automatically, but to also update him in case he did get a destination to move to.

function UpdateGame(delta_ms)

{

    ClearCanvas(ctx, "rgba(0,0,255,255)"); //clears the canvas, so we don't get "ghosting"

    timmy.Update(delta_ms);

    timmy.DrawFriend(); //re-draw Timmy

}

So now that we have our character moving around, lets create a world for them to move around in.

## Full code listing

You can also find the code up on the books github page as “7_Player_controls.html”.

<html>

<head>

 <style>

 *

    {

 margin:0;

 padding:0;

 font-family: Verdana, Geneva, Tahoma, sans-serif;

    }

 canvas

    {

 display: block;

    }

 #game_container

    {

 position: relative;

 display: inline-block;

    }

 #fps

    {

 position: absolute;

 top:10px;

 right:10px;

 color:white;

 font-weight: 900;

 font-size: 20px;

 text-shadow:2px  2px  0  black,

 2px  -2px  0  black,  

 -2px  -2px  0  black,

 -2px  2px  0  black;

 pointer-events: none;

    }

 </style> 

</head>

<body>

<div  id="game_container">

<canvas></canvas>

 <p  id="fps">120</p>

</div>

<script>

 class  Friend

    {

 constructor(their_name, their_age, their_loves_spinach, their_eye_color, their_skin_color, their_hair_color, their_x_pos, their_y_pos)

        {

 this.name = their_name;

 this.age = their_age;

 this.loves_spinach = their_loves_spinach;

 this.eye_color = their_eye_color;

 this.skin_color = their_skin_color;

 this.hair_color = their_hair_color;

 this.x_pos = their_x_pos;

 this.y_pos = their_y_pos

 //for moving

 this.x_dest=0;

 this.y_dest=0;

 this.moving_x=false;

 this.moving_y=false;

 this.move_speed= 0.2;

 console.log("A friend was created, with name: "+this.name+", age: "+this.age+", and loves spinach: "+this.loves_spinach);

 console.log("And some facts about them, eye color: "+this.eye_color+", skin color: "+this.skin_color+", hair color: "+this.hair_color+", x and y: "+this.x_pos+", "+this.y_pos);

 this.DrawFriend();

        }

 SayHi()

        {

 console.log("Hi, my name is "+this.name +", my age is: "+this.age+", and do I love spinach? "+this.loves_spinach+".");

        }

 SetDestination(x_dest, y_dest)

        {

 this.x_dest=x_dest;

 this.y_dest=y_dest;

 this.moving_x=true;

 this.moving_y=true;

        }

 DrawFriend()

        {

 //this is where we will start drawing our friend

 //---------------- get the canvas stuff we need to be able to draw ----------------

 let  my_canvas = document.querySelector("canvas");

 let  draw_context = my_canvas.getContext("2d");

 let  ctx = draw_context;

 //---------------- draw the head ----------------

 //define width and height of the head

 let  width_head = 50;

 let  height_head = 60;

 ctx.fillStyle = this.skin_color;

 ctx.fillRect(this.x_pos, this.y_pos, width_head, height_head);

 //---------------- draw the eyes ----------------

 //define width and height of the eyes

 let  width_eyes = 10;

 let  height_eyes = 15;

 //set the fill style:

 ctx.fillStyle = this.eye_color;

 //define how offset the eyes should be from the left and right side of the head

 let  eye_x_offset = 10;

 //define how offset the eyes should be from the top of the head

 let  eye_y_offset = 15;

 //--draw the left eye, left corner, top , width and height --

 ctx.fillRect(this.x_pos+eye_x_offset, this.y_pos+eye_y_offset, width_eyes, height_eyes);

 //--draw the right eye--

 //a lot more complicated- have to find right side of head (x_pos+width_head), then minus out the width of eye + x offset of eye to position the left side of the eye away from the right side of the head

 let  right_side_of_head=this.x_pos+width_head

 let  right_eye_x_pos = right_side_of_head - width_eyes-eye_x_offset;

 ctx.fillRect(right_eye_x_pos, this.y_pos+eye_y_offset , width_eyes, height_eyes);

        }

 Update(delta_ms)

        {

 this.MoveToDest(delta_ms);

        }

 MoveToDest(delta_ms)

        {

 if(this.moving_x)

            {

 if(this.x_dest>this.x_pos)

                {

 this.x_pos+=this.move_speed*delta_ms;

 if(this.x_pos>=this.x_dest)

                    {

 this.x_pos=this.x_dest;

 this.moving_x=false;

                    }

                }

 else  //x_dest < x_pos -so need to move to the left/ -x

                {

 this.x_pos-=this.move_speed*delta_ms;

 if(this.x_pos<=this.x_dest)

                    {

 this.x_pos=this.x_dest;

 this.moving_x=false;

                    }

                }

            }

 if(this.moving_y)

            {

 if(this.y_dest>this.y_pos) // if dest is greater, move him down, where y increases

                {

 this.y_pos+=this.move_speed*delta_ms;

 if(this.y_pos>=this.y_dest)

                    {

 this.y_pos=this.y_dest;

 this.moving_y=false;

                    }

                }

 else  //y_dest < y_pos -so need to move upward/ -y

                {

 this.y_pos-=this.move_speed*delta_ms;

 if(this.y_pos<=this.y_dest)

                    {

 this.y_pos=this.y_dest;

 this.moving_y=false;

                    }

                }

            }

        }

    }//end of Friend class

 function  ClearCanvas(ctx, background_color)

    {

 ctx.fillStyle = background_color;

 ctx.fillRect(0, 0, my_canvas.width, my_canvas.height);

    }

 function  UpdateGame(delta_ms)

    {

 // timmy.x_pos=timmy.x_pos+5;

 // timmy.x_pos=timmy.x_pos+delta_ms*0.05206;

 ClearCanvas(ctx, "rgba(0,0,255,255)"); //clears the canvas, so we don't get "ghosting"

 timmy.Update(delta_ms);

 timmy.DrawFriend(); //re-draw Timmy

    }

 function  Update(time_ms)

    {        

 let  frame_delta_ms = time_ms - last_time_ms; // #2 going to find the delta/difference in time between the last frame (initially 0) and the current time

 let  delta_s = frame_delta_ms / 1000; //since time is in ms (1 /1000 s), to convert to seconds, divide by 1000, exp: 2000ms/ 1000 = 2s

 let  fps= 1 / delta_s; //we can convert from seconds/ frame (delta_s) to frames/ second by flipping it dividing 1 by it- 1/ (seconds/frame) = frame/ second= fps

 frame_delta_ms = frame_delta_ms.toFixed(2); //going to round to just 2 decimal places using toFixed(2)

 //so.... toFixed which rounds a number, returns a string instead of a number.... so have to now turn it back into a number... JavaScript...

 frame_delta_ms = parseFloat(frame_delta_ms);

 fps = fps.toFixed(2);

 fps_txt_element.innerHTML=Math.round(fps);

 // console.log("Update: delta time: "+frame_delta_ms+", fps: "+fps);

 Resize();

 UpdateGame(frame_delta_ms);

 last_time_ms = time_ms;

 // setTimeout(function(){window.requestAnimationFrame(Update)}, 100 );

 window.requestAnimationFrame(Update);

    }

 function  Resize()

    {

 if(window.innerWidth != last_width || window.innerHeight != last_height)

        {

 my_canvas.setAttribute('width', window.innerWidth);

 my_canvas.setAttribute('height', window.innerHeight);

 last_width=window.innerWidth;

 last_height=window.innerHeight;

        }

    }

 function  MoveMyPlayer(x_dest, y_dest)

    {

 //move my_player/ timmy to the destination clicked

 console.log("Moving my player to destination: x: "+x_dest+", y: "+y_dest)

 timmy.SetDestination(x_dest, y_dest);

    }

 function  MouseUp(event)

    {

 let  x_dest = event.clientX;

 let  y_dest = event.clientY;

 console.log("Mouse up at: x: "+x_dest+", y: "+y_dest);

 MoveMyPlayer(x_dest, y_dest)

    }

 function  TouchUp(event)

    {

 let  x_dest = event.changedTouches[0].clientX;

 let  y_dest = event.changedTouches[0].clientY;

 console.log("Touch up at: x: "+x_dest+", y: "+y_dest);

 MoveMyPlayer(x_dest, y_dest)

    }

 function  SetupInput()

    {

 my_canvas.addEventListener("mouseup", MouseUp);

 my_canvas.addEventListener("touchend", TouchUp);

    }

 let  fps_txt_element = document.getElementById("fps");

 let  last_time_ms = 0;

 window.requestAnimationFrame(Update);

 let  my_canvas = document.querySelector("canvas");

 let  draw_context = my_canvas.getContext("2d");

 let  ctx = draw_context;

 //change the width and height of the canvas to be the same size as the window

 my_canvas.setAttribute('width', window.innerWidth);

 my_canvas.setAttribute('height', window.innerHeight);

 let  last_width=window.innerWidth;

 let  last_height=window.innerHeight;

 let  timmy = new  Friend("Timmy Smith", 16, true, "rgb(0,0,255)", "rgb(209, 181, 140)", "rgb(125, 60, 34)", 20, 20);

 SetupInput();

// timmy.DrawFriend();

</script>

</body>

</html>

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/7_Player_controls.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/7_Player_controls.html)

# 8. Creating the world - background tiles

## Choosing a game tile size

How big should we make the tile? With backgrounds, to save room, as well as be able to generate different maps on the fly, we usually use smaller images, and tile, or repeat the tile across the screen many times to generate a repeating background. If you make them too small, you'll see the repeating pattern relatively easily. But if you make them too big, it takes more memory to store 1 big image, when you could store many smaller tiles instead. Additionally, when players modify a tile, the smaller the tile, the more the number of things they can interact or change on screen at once.

Looking into what the most common resolutions are:

[https://gs.statcounter.com/screen-resolution-stats](https://gs.statcounter.com/screen-resolution-stats)

The second most common resolution as of right now is: 1366x768 (1366 wide, 768 tall on widescreen), which is slightly smaller than the 1st most common resolution, and bigger than the 3rd most common. So, we'll design based on that size.

Graphics cards can display textures/ images that are in multiples of 2's much easier than random size, so it's usually a good idea to try to have things as a multiple of 2 when you can, for performance (but not absolutely required these days). Multiples of 2's are: 2x2= 4, 2x2x2= 8, 2x2x2x2 = 16, 32, 64, 128, 256, 512, 1024, 2048, 4096, etc.

If we want to use 64x64 pixel tiles, that would let us have 1366/64 = 21 tiles wide, and 768/64 = 12 tiles tall.

That sounds reasonable for what a player would be able to see on the screen at a time, so we'll use that. We could use any value, but it's good to setup restrictions early on, so you have an area to design into, but can always change it before you do too much work if you realize it could be better, for some reason.

## Using a canvas to create textures

The canvas tag can be used for drawing directly to the screen, like we saw. But we can also create textures to it temporarily, and save them, to use again later.

We're going to create a “TileCreator” class, which will create its own canvas, which is the tile width and height, and create tiles on it, saving them to use in the main game.

Create the “TileImageCreator” class after the "Friend" class:

class TileImageCreator

{

    constructor()

    {

        //width, height, and image to store tiles

        this.width_tile= 64;

        this.height_tile= 64;

        this.dirt_tile= new Image();

        //canvas to create the tile images on

        let tile_canvas = document.createElement('canvas');

        tile_canvas.width = this.width_tile;

        tile_canvas.height = this.height_tile;

        let tile_ctx = tile_canvas.getContext('2d');

        this.CreateDirtTileImage(tile_canvas, tile_ctx);

    }

    CreateDirtTileImage(tile_canvas, tile_ctx)

    {

        //define colors we're going to be drawing with

        let medium_brown = "rgb(99, 65, 5)"

        let dark_brown = "rgb(61, 40, 2)"

        let light_brown = "rgb(125, 75, 9)"

        //draw the medium brown color over the entire image

        tile_ctx.fillStyle = medium_brown;

        tile_ctx.fillRect(0, 0, this.width_tile, this.height_tile);

        //draw dark brown spots

        tile_ctx.fillStyle = dark_brown;

        tile_ctx.fillRect(0, 10, this.width_tile*.33, this.height_tile*.25);

        tile_ctx.fillRect(40, 40, this.width_tile*.33, this.height_tile*.25);

        tile_ctx.fillRect(25, 0, this.width_tile*.33, this.height_tile*.25);

        //draw the light brown spots

        tile_ctx.fillStyle = light_brown;

        tile_ctx.fillRect(30, 50, this.width_tile*.1, this.height_tile*.1);          

        tile_ctx.fillRect(60, 10, this.width_tile*.1, this.height_tile*.1);

        tile_ctx.fillRect(0, 30, this.width_tile*.1, this.height_tile*.1);

        //copy the drawing from the tile canvas to the dirt tile image

        this.dirt_tile.src = tile_canvas.toDataURL("image/png");

    }

} //end of TileImageCreator class

In the constructor, we'll first define variables we want for the entire "TileImageCreator" class, the width and height of all tiles, then we'll create an image called "dirt_tile" to permanently store the drawing we do on the tile canvas.

We'll also create a canvas just for creating the tiles, with the width and height of the tile images. We'll then create the dirt tile image using "CreateDirtTileImage".

In this function, we're just drawing like we did for our character. We define all the colors, set the canvas context to the color we want to draw with, and then draw rectangles using the context. I just played around with the x, y, width and height of the rectangles to get something that looked roughly like a dirt tile.

Finally, we save it in the "dirt_tile" Image as the src/ source of the image.

Now to actually see the image, we need to draw it to the screen.

First, we’ll initialize the “TileImageCreator”, by adding before we create our friend “Timmy”:

let tile_creator = new TileImageCreator();

In the function "UpdateGame", under "ClearCanvas(ctx, "rgba(0,0,255,255)");", add the line:

ctx.drawImage(tile_creator.dirt_tile, 150, 0);

Which will draw our "tile_creator.dirt_tile" we just created at position x=150, y=0 on the screen before drawing our character, after the canvas was cleared.

Now we have one tile drawn to the screen, but we'll want a bunch of them, tiled in both the x and y direction, so we have the full screen filled with tiles (or more, and add scrolling). So, let's create something that can contain a bunch of tiles!

## Creating a map of tiles

Right now, to be able to draw multiple tiles to the screen, we have to draw each tile individually, such as to draw 3 tiles on the top row (under "ClearCanvas(ctx, "rgba(0,0,255,255)");", again):

ctx.drawImage(tile_creator.dirt_tile, 0, 0);

ctx.drawImage(tile_creator.dirt_tile, 64, 0);

ctx.drawImage(tile_creator.dirt_tile, 128, 0);

If we want to create a map/ world that is the size of the most common screen size, 1366x768, we’ll need to draw out 1366/64 = 21 tiles across, and 768/64 = 12 tiles down, and to fill the full screen that is 21x12= 252 times we would have to copy the “drawImage” function! And I want to make the first map 2x the screen width and height, so 42x24=1,008 tiles/ draw calls!

Doing that by copying and pasting would be insanity, not to mention one of the biggest things to remember in programming is “DRY” – “Do Not Repeat Yourself”. Programmers do what they do to save people time, automate things, and find efficient ways to do things. So if you find yourself repeating things more than once or twice, there’s likely a much more efficient way of doing things.

## Arrays or Lists

We have a built-in object type in programming known as an “Array”, or “List”. It’s just a type of object that can hold a bunch of the same type of objects. Think of if you have 8 friends, you could put them in a variable called “my_friends”.

Say you need to get grocery items at the store, “2 lemons”, “cereal”, “meat”, “blueberries”, “pizza”, “fried chicken”, “salad”, “5 avocados”. You could store them in individual variables like “grocery_item1”, “grocery_item2”, etc.

But the way to store them in one object, known as an array is:

let grocery_list= new Array("2 lemons", "cereal", "meat", "blueberries", "pizza", "fried chicken", "salad", "5 avocados");

You can put this in on the bottom of your program for testing, which we’ll delete before we move forward on the game.

If you console.log out the “grocery_list” variable:

console.log(grocery_list);

It should show you something like:

Array(8) [ "2 lemons", "cereal", "meat", "blueberries", "pizza", "fried chicken", "salad", "5 avocados" ]
0: "2 lemons"
1: "cereal"
2: "meat"
3: "blueberries"
4: "pizza"
5: "fried chicken"
6: "salad"
7: "5 avocados"
length: 8

One major thing to realize about arrays is they start at “0”. This can be a bit confusing at first, but item 0 is the first item. The last item is the number of total items minus 1 (since it started at 0 instead of 1). So, we have 8 items in our array, the first is at position 0, so the 8th is one less, or item 7 (since the first item is 0, instead of 1- which is 1 less than you normally do).

It’s a bit counter-intuitive at first, but makes some math dealing with arrays a lot smoother later on.

So, we can log out the entire array, but how do we log out individual items in the array? You access it using the variable name, and square blocks of which item number.

For example, if you want to console.log out the first item in the array:

console.log(grocery_list[0]);

“2 lemons”

or the 3rd item in the list (so 3-1 = 2, so we log out item 2 to see the 3rd item)

console.log(grocery_list[2]);

“meat”

What about the last item? You could know that the length of items is 8, so you could log out item: 8-1=7. But an easier way is to use a built-in property of all arrays: “length”.

To log out the length of the array use: 

console.log(grocery_list.length);

“8”

This logs out “8”, since that is the number of items in the array. So to be able to see the last item, we can use this length – 1 (which would be 7 in this case) to see the last item:

console.log(grocery_list[grocery_list.length-1]);

"5 avocados"

This is the same thing as saying:

console.log(grocery_list[7]);

But it allows us to be able to add or remove stuff from the grocery list, and always print out the last item, no matter how many items are in the list.

Speaking of which, we saw above how to create an array from scratch, and have items added to it when it is created, but how do you add or remove items from the array/list?

## Adding and removing items from an array

Change the code on the bottom of your program to:

let grocery_list= new Array("2 lemons", "cereal", "meat", "blueberries", "pizza", "fried chicken", "salad", "5 avocados");

//put new code below here

console.log(grocery_list);

console.log(grocery_list.length);

console.log(grocery_list[grocery_list.length-1]);

This will print out the size of the array (8) and the last item in the list. But let’s add a new item on the end of the list. Add the following below where new code should be placed:

grocery_list.push("chocolate bars");

Now you should see the size of the array is now 9, and the last item is the new item we added. “Push” is a function built into the array to add something onto the end.

If you want to remove an item from the array, add under the push:

grocery_list.splice(2,1);

This will remove item number 2 (0,1,2 – so the third item, meat). The number 2 is the position in the array, and the number 1 is for how many items to remove (this time just one).

What if we want to put a new item somewhere in the array, but not pushed onto the end? Well, here it gets a little confusing:

grocery_list.splice(1,0, "milk");

Now we’re “splicing” at item 1(2nd item, cereal), but we’re going to remove “0 items”, and the last thing is we’re going to add the new item “milk”. So now “milk” will be the new item 1 (2nd item), and will push cereal to be the 3rd item instead.

Don’t worry if it’s not super understandable right now, this is one of those things that becomes easier with practice, and on top of that, we won’t be modifying our arrays after we create them for the background tiles (but will modify other arrays later on).

You should delete all this “grocery_list” code, since it was only to show how arrays work, and won’t be used in our game.

## Creating an array of tiles

If we want to create an array of tiles, so we can draw a bunch of them easily, the first thing we’ll want to do is create a tile class, so it can keep track of where it is being drawn on screen, and later what type of tile it is.

Create a new tile class below where you created your “TileImageCreator” class:

class Tile

{

    constructor(x, y)

    {

        //x and y position of the tile, to be able to draw it onscreen

        this.x= x;

        this.y= y;

    }

} //end of Tile class

We just created a class that just has an “x” and “y”, so we will know where to draw it on screen. We’re also passing over the x and y values when we create it in the constructor, so we can pass over the position quickly when we create each tile.

Now we want to create an array of tiles on the bottom of our program, below where we created the “tile_creator” variable:

let tiles = new Array(new Tile(0,0), new Tile(64, 64), new Tile(64*2, 64*2), new Tile(64*3, 64*3), new Tile(64*4, 64*4));

We create 5 new tiles in the array, going up by 64 (the width and height of our tiles) in both the x and y direction, which will create 5 tiles going down in a diagonal direction (going over 1 tile space, then down 1 tile space each time). I could have typed out the actual numbers for each one (64*2 = 128, 64*3 = 192, etc), but I just had the program do the math for each tile instead, since it’s easier.

Now let’s draw out tiles onscreen. In the “UpdateGame” function, under “ClearCanvas” replace the tile drawing code with:

ctx.drawImage(tile_creator.dirt_tile, tiles[0].x, tiles[0].y);

ctx.drawImage(tile_creator.dirt_tile, tiles[1].x, tiles[1].y);

ctx.drawImage(tile_creator.dirt_tile, tiles[2].x, tiles[2].y);

ctx.drawImage(tile_creator.dirt_tile, tiles[3].x, tiles[3].y);

ctx.drawImage(tile_creator.dirt_tile, tiles[4].x, tiles[4].y);

This just draws out our 5 tiles, but using the “tiles” array object we created, accessing the x and y position we gave each tile. If you run this now, you’ll see our 5 tiles being drawn out in a diagonal pattern.

But so far this doesn’t really save us time using the array, since we’re still only printing out 5 tiles. So, let’s start optimizing based on the DRY principle.

## Loops to go through arrays, and limit repetitiveness

When you have to do something repetitive like this, you can usually replace it while using a “loop”, to loop through each item, one by one, first to last.

The basis loop is called a “while” loop- it keeps going through the same bit of code, over and over again until a “if” condition is met. So at the bottom of your program, in a temp area we’ll print out counting 1 to 5 how we currently know how to do it:

console.log("counting number: "+0);

console.log("counting number: "+1);

console.log("counting number: "+2);

console.log("counting number: "+3);

console.log("counting number: "+4);

Repetitive, huh?

Well, lets replace it with a while loop:

let count=0;

while(count < 5)

{

    console.log("counting number: "+count);

    count++;

}

While loops check to see if something is true (just like an if statement), and will keep running the same loop, over and over again, until what it is checking becomes false.

In this case, we created the variable “count” outside the while loop, set it to 0, and then check to see if it is less than 5, which it is (but if it was 5, it would have never entered the loop).

Next, inside the loop, we log out the number like before, but we also increment, or “add 1” to count.

So, the first time it goes into the loop, count is 0, prints it out, and adds 1 to it, making count now “1”. It then starts back at the top, checks if 1 is less than 5 (which it is), and enters the loop again. It keeps doing this, changing count to 2, 3, 4, 5, every time through the loop. When it hits 5, the while statement realizes that it is no longer less than 5, and exits the loop/ goes on with the program (doing anything below the loop).

Pretty nice! But this becomes a lot more useful when you have LOTS of things to do. For instance, if we wanted to count to 100, all we would have to do is change when the loop exits (exits if count had become 101, so it only runs in the loop up to 100):

let count=0;

while(count < 101)

{

    console.log("counting number: "+count);

    count++;

}

Now it will count all the way up to 100, but with only a few lines of code!

We can do something similar with our tiles in a minute. But first I wanted to show you another type of loop that is used a lot more often (but does the same thing as above, with less lines). The “for loop”!

So, replacing the above with a for loop:

for (let count=0; count < 101; count++)

{

    console.log("counting number: "+count);

}

It does the same thing as above, but puts it on fewer lines.

In a for loop, the first section is declaring a variable (usually your count, also known as the “index”). Here we just declare a variable “count”, and set it to 0.

Next, we have a semi colon to do the next part, which is actually what was in the “while” statement above- it just checks to see if something is true, and if it is, goes into the loop again.

Next another semicolon, and we do whatever happens at the end of the loop- usually iterating/ adding 1 to the count/index.

So, all you really have to know at this point is a for loop starts somewhere, checks if it’s still in a valid range, and adds to the count/index to keep going through the loop until the middle area becomes false, and it exits the loop.

For consistency, most people use “index” for the name of the variable in a for loop like:

for (let index=0; index < 101; index++)

{

    console.log("counting number: "+index);

}

And to save time, you can cut down “index” to “i”:

for (let i=0; i < 101; i++)

{

    console.log("counting number: "+i);

}

You can name the variable inside the loop anything you want, but “i” is usually quickest to do, and most programmers will use it. It might be confusing when starting, but the more times you see it, the more you’ll recognize it.

You should delete this test code, because we’re going to apply the same concept to our tiles in the next section.

## Using for loops for our tiles

Let’s draw out tiles using the for loop on screen. In the “UpdateGame” function, under “ClearCanvas” replace the tile drawing code with:

for (let i=0; i < tiles.length; i++)

{

    ctx.drawImage(tile_creator.dirt_tile, tiles[i].x, tiles[i].y);

}

This does the same things as before, but with using a for loop. We start at the first item (0), make sure it’s less than the length of tiles, draw the image, then add 1 to the index, and repeat until the index is no longer less than the number of tiles.

Now we’re also going to use a “for loop” for creating the tiles, instead of just drawing them.

Down at the bottom of the program, replace the code where you create the tiles array (below where we created the “tile_creator” variable) with:

let tiles = new Array();

let screen_width_default=1366;

/*number of tiles we're going to have in the x direction. 

This is the screen width *2 (so 2 screen widths) 

divided by the width of each tile, to find the number of tiles in the x direction

*/

let num_tiles_x = Math.round(screen_width_default*2 / tile_creator.width_tile);

for(let x= 0;x<num_tiles_x; x++)

{

    tiles.push(new Tile(x*tile_creator.width_tile, 0));

}

We first create a blank array of tiles, since we’re going to use the for loop to figure out their positions.

We’ll code in what the default width of the screen is, so we can use that to create 2 screens worth of tiles (so we can later on have a scrolling world).

Next, we need to figure out how many tiles make up 2 screen widths. We’re going to round the number (since you can’t have a decimal for the number of tiles- (you can’t have ½, or 1/10th of a tile). So the screen width *2 (in number of pixels) divided by the width (in pixels) of each of our tiles, is the number of tiles we need to have 2 screen widths of them.

Now we have a for loop to create all of them. So instead of using “index” or “i” for counting, we’re going to use “x”, since we’re going to be moving a little over in the x direction every time through the loop. We’ll start at 0 (the left edge of the screen), and increase the x position by 1 tile width each time through the loop (putting a bunch of tiles moved over by 1 tile width, so all being moved over 1 tile space each time through the loop).

Inside the loop, we’re just pushing each new tile into our tile array, just increasing the x position by whatever tile number we’re on, times the width of the tile (to get them side by side). For the y position, we’re just using 0, so they’ll all be at the top of the screen for now.

If you run the code now, you’ll see one row on top, going all the way across the screen!

![](Images/image00475.jpeg)

But what if we want to also loop over in the y direction, so we have tiles going both across and down the screen?

It’s a little more complicated, but we just also have to create a loop to iterate/ count in the y direction too! So, change your creation code to:

let  tiles = new  Array();

let screen_width_default=1366;

let screen_height_default=768;

let num_tiles_x = Math.round(screen_width_default*2 / tile_creator.width_tile);

let num_tiles_y = Math.round(screen_height_default*2 / tile_creator.height_tile);

for(let x= 0;x<num_tiles_x; x++)

{

    for(let y= 0;y<num_tiles_y; y++)

    {

        tiles.push(new Tile(x*tile_creator.width_tile, y*tile_creator.height_tile));

    }

}

So we also store what our default screen height is, because we’ll use that to figure out how many tiles we need again.

We calculate the number of tiles we’ll need in the y direction as well.

Next we create a for loop for the y direction too this time, and we’ll also get to create tiles based on their y position, since we’re looping through in the y direction as well.

So, to see how we would step through this:

Loop x=0, y=0:

Initially both x and y are 0, so tile position is 0,0.

Loop: x=0, y=1 (we need to go through all the y positions while x is 0, before we can move on to x =1):

x is still 0, y is now 1, so tile position is: 0, 64

Loop: x=0, y=2:

x is still 0, y is now 2, so tile position is: 0, 128

So on and so on, until the y gets greater than the number of tiles in the y direction. Finally, when we’re all done going through the number of y tiles for x=0\. We exit the y loop, and go back to the top, and now x is 1!

So, we then run through it again, but now x is 1, but we’ll go through all the y’s for x=1.

Loop x=1, y=0:

x is now 1, y is 0 so tile position is 64,0.

Loop x=1, y=1:

x is now 1, y is 1 so tile position is 64,64.

Loop x=1, y=2:

x is now 1, y is 2 so tile position is 64,128

So on, and so on, until we went through all the y positions, for all the x positions. So if you could pause at the end of every y loop, you would see a long strip of tiles being added, going in the first x position, all the way down the screen. The next time through the x loop, it would then draw another long strip of tiles, all the way down the screen, continuing strip by strip, until every x position is drawn.

Since the y loop is inside the x loop, you go through every y position, the full y loop, for every x position. The x loop only gets run once (since it’s the outside loop), but the y loop gets run many, many times, for every x.

We could have put the x loop inside the y loop instead, drawing strips across the screen, then down one, every single time, and we would have gotten the same results. But for me, it makes more sense to have the x loop on the outside, and it is easier to visualize drawing strips down the screen in the y loop, then moving 1 tile to the right every time we go through the x loop.

So now if you run this, you’ll see we have a full tiles world behind our character, and he can still move through it!

![](Images/image00476.jpeg)

It looks nice, but a bit monotonous. So, let’s add a couple more tile types.

## Adding in more tile types

Let’s add in a couple more tile types, maybe a basic stone, grass, bush and water type. We’ll do this the same way we did the dirt tile, with the biggest change just being what we draw.

Change our Tile class to allow us to have more tile types:

class Tile

{

    static DIRT = 0;

    static STONE = 1;

    static WATER = 2;

    static GRASS = 3;

    static BUSH = 4;    

    static LAST_TYPE = 4; //to keep track of whatever the last tile type is, for picking a random tile

    constructor(x, y, type, image)

    {

        //x and y position of the tile, to be able to draw it on screen

        this.x = x;

        this.y = y;

        this.type = type;

        this.image = image;

    }

    Draw(ctx)

    {

        ctx.drawImage(this.image, this.x, this.y);

    }

} //end of Tile class

Static is a keyword that creates a variable on a class, not an object/ instance of the class. This will allow us to have some values we can access by calling: “Tile.DIRT” or “TILE.STONE”, rather than having these tile types on one specific tile. That way we can even access these without creating an actual tile object- since the variables are part of the class, so all tile objects will share these variables.

This makes it easier, since all tiles will be of some “tile type”, and we can access these tile types before we create any tiles.

We also set them to be unique numbers, counting up from 0\. Any new tile types we’ll have to increase the number, so each tile type will be easily identifiable based on its number/ type.

We also changed the constructor, so we can pass in the tile type, and the tile image. That way the tile knows what type it is, and can draw its own image.

We also added a function called “Draw”, that passes in the canvas context, and allows tiles to draw themselves, which could allow us to later change the draw function to do other things, such as draw animated tiles.

Next, in the “TileImageCreator” class, we’re going to add some new functions to create the new tile types. Change the constructor to:

constructor()

{

    //width, height, and image to store the dirt tile

    this.width_tile= 64;

    this.height_tile= 64;

    this.dirt_tile= new Image();

    this.stone_tile= new Image();

    this.water_tile= new Image();

    this.grass_tile= new Image();

    this.bush_tile= new Image();

    //canvas to create the tile images on

    let tile_canvas = document.createElement('canvas');

    tile_canvas.width = this.width_tile;

    tile_canvas.height = this.height_tile;

    let tile_ctx = tile_canvas.getContext('2d');

    this.CreateDirtTileImage(tile_canvas, tile_ctx);

    this.CreateStoneTileImage(tile_canvas, tile_ctx);

    this.CreateWaterTileImage(tile_canvas, tile_ctx);

    this.CreateGrassTileImage(tile_canvas, tile_ctx);

    this.CreateBushTileImage(tile_canvas, tile_ctx);

}

We’re just creating a new image for each type in the top, and in the bottom, we’re calling functions for drawing out each image type, which we’ll add below.

Below the “CreateDirtTileImage()” function, add the following new functions:

CreateStoneTileImage(tile_canvas, tile_ctx)

{

    let medium_grey = "rgb(99, 99, 99)"

    tile_ctx.fillStyle = medium_grey;

    tile_ctx.fillRect(0, 0, this.width_tile, this.height_tile);

    this.stone_tile.src = tile_canvas.toDataURL("image/png");

    // console.log("created stone tile");

}

CreateWaterTileImage(tile_canvas, tile_ctx)

{

    let medium_blue = "rgb(100, 100, 200)"

    tile_ctx.fillStyle = medium_blue;

    tile_ctx.fillRect(0, 0, this.width_tile, this.height_tile);

    this.water_tile.src = tile_canvas.toDataURL("image/png");

}

CreateGrassTileImage(tile_canvas, tile_ctx)

{

    let medium_green = "rgb(100, 200, 100)"

    tile_ctx.fillStyle = medium_green;

    tile_ctx.fillRect(0, 0, this.width_tile, this.height_tile);

    this.grass_tile.src = tile_canvas.toDataURL("image/png");

}

CreateBushTileImage(tile_canvas, tile_ctx)

{

    let dark_green = "rgb(0, 200, 0)"

    tile_ctx.fillStyle = dark_green;

    tile_ctx.fillRect(0, 0, this.width_tile, this.height_tile);

    this.bush_tile.src = tile_canvas.toDataURL("image/png");

}

GetTileImage(type)

{

    if(type==Tile.DIRT)

        return this.dirt_tile;

    else if(type==Tile.STONE)

        return this.stone_tile;

    else if(type==Tile.WATER)

        return this.water_tile;

    else if(type==Tile.GRASS)

        return this.grass_tile;

    else if(type==Tile.BUSH)

        return this.bush_tile;

}

These functions just draw out one flat color for each tile type, and set the corresponding image to that drawing from the canvas, like we did with the dirt tile.

The last function will return the right image type, when the tile type is sent, so that we can easily get the right image when we create the tiles.

We now have tile graphics being created, the different tile types as numbers/unique ids, and being able to get the image for the tile type. So now let’s actually generate them in our world.

In the bottom of the program, where you create the tiles, change it to:

for(let x= 0;x<num_tiles_x; x++)

{

    for(let y= 0;y<num_tiles_y; y++)

    {

        let type = Math.floor(Math.random()*(Tile.LAST_TYPE+1));//need +1 or doesn't include the highest number/ 

        tiles.push(new Tile(x*tile_creator.width_tile, y*tile_creator.height_tile, type, tile_creator.GetTileImage(type)));

    }

}

First, we’re going to be getting a random tile type, based on the number of ones we have. You kind of have to read this line from the inside out.

Math.random is a function that will find a random decimal number between 0 and 1, but doesn’t actually include 1\. If we multiply this by the last tile number +1, it will be any number between 0 and our last tile (0,1, 2,3 or 4). Since it is a decimal, but our ids are whole numbers, we have to “math.floor” it, or round down the decimal place to make it a whole number.

Next, we create our tile, but also pass it the tile type, and we get the image for the tile based on the type.

Finally, we’ll have to change out how we draw the tiles to actually see the different images. In the “UpdateGame” function, change out the tile drawing code:

for (let  i=0; i < tiles.length; i++)

{

 tiles[i].Draw(ctx);

}

If you save, and refresh the page, you’ll see all the different tile types being populated on screen! But it looks pretty messy right now. You can refresh the page multiple times, and the map will change every time. But it looks too random, so we should work on making it look a bit nicer.

![](Images/image00477.jpeg)

First, let’s change around the drawing code for the tiles, so that we can more easily distinguish the grass, stone, and bushes.

Change out your stone image generation code with:

CreateStoneTileImage(tile_canvas, tile_ctx)

{

    let medium_grey = "rgb(99, 99, 99)";

    let dark_grey = "rgb(70, 70, 70)";

    let light_grey = "rgb(170, 170, 170)";

    tile_ctx.fillStyle = medium_grey;

    tile_ctx.beginPath();

    //format for arc(angles in "radians"/ Math.PI):  arc(x, y, radius, startAngle, endAngle)

    tile_ctx.arc(this.width_tile*.5, this.height_tile*.5, this.width_tile*.5, 0, 2 * Math.PI);

    tile_ctx.fill();

    tile_ctx.fillStyle = dark_grey;

    tile_ctx.beginPath();

    tile_ctx.arc(this.width_tile*.3, this.height_tile*.45, this.width_tile*.2, 0, 2 * Math.PI);

    tile_ctx.arc(this.width_tile*.5, this.height_tile*.4, this.width_tile*.3, 0, 2 * Math.PI);

    tile_ctx.fill();

    tile_ctx.fillStyle = light_grey;

    tile_ctx.beginPath();

    tile_ctx.arc(this.width_tile*.3, this.height_tile*.3, this.width_tile*.1, 0, 2 * Math.PI);

    tile_ctx.fill();

    this.stone_tile.src = tile_canvas.toDataURL("image/png");

}

The major difference is we’re using canvas’s “arc” function to be able to draw circles. The format for it is the x position, y position, radius (half the circle width), starting angle, and ending angle (both in “radians”, not degrees).

We draw it at half the width and height for x and y, which puts it right in the center of our tile. We also make the radius half the width and height, which makes it have the full width of our tile size (radius is half the total width/ diameter of a circle). We start at angle 0 (which points to the right side of our tile), all the way to Math.PI (which goes around the entire circle, and comes back to 0, drawing a full circle).

We then create some extra circles, with different colors of grey below, to add some details.

If you run this now, you’ll see the rock being drawn on the dirt tile, but it looks a little bit like an eyeball with the perfect circle. ![](Images/image00478.jpeg)

So, we’re going to change it to use custom curves, to get a more “rock like” shape to it. Bezier curves are curves that let you create more custom shapes, and are one of the main ways of drawing using vector programs like Adobe Illustrator or Inkscape.

You can even “save as” your vector art from Inkscape, and save it as “HTML5 canvas”, so that you can actually work with an art program, instead of having to guess and test manually using each command. Just create your vector art in Inkscape, save it as an html canvas, open the html file up with a text editor/ visual code, and copy the drawing code into your program.

I created this using Inkscape, setting the document properties (file->document properties) to 64x64 width and height, scale to 1.0.

Then I created a roughly rock shape:

CreateStoneTileImage(tile_canvas, tile_ctx)

{

    //format for arc(angles in "radians"/ Math.PI):  arc(x, y, radius, startAngle, endAngle)

    let ctx = tile_ctx;

    ctx.beginPath();

    ctx.fillStyle = 'rgb(125, 125, 125)';

    ctx.strokeStyle = 'rgb(0, 0, 0)';

    ctx.lineWidth = 2.000000;

    ctx.lineCap = 'butt';

    ctx.lineJoin = 'miter';

    ctx.moveTo(0.430373, 53.826145);

    ctx.bezierCurveTo(2.211780, 43.734546, 10.769525, 1.063608, 31.308098, 0.400035);

    ctx.bezierCurveTo(46.271642, -0.083416, 62.638869, 44.648782, 63.729706, 51.926548);

    ctx.bezierCurveTo(65.826382, 65.915002, 43.669500, 63.520649, 30.595534, 63.324116);

    ctx.bezierCurveTo(17.638494, 63.129345, 0.192852, 64.392639, 0.430373, 53.826145);

    ctx.fill();

    ctx.stroke();

    this.stone_tile.src = tile_canvas.toDataURL("image/png");

}

I ended up creating a variable alias “ctx” in the function from the tile_ctx, because Inkscape generates the canvas context variable with that name by default, and it’s quicker than needing to rename it every time I save it out.

A Bezier curve is a point that has 2 handles on each side of a point, that lets us smooth/ modify that point by changing those handles. It’s the main tool pretty much all vector graphics use to create vector art.

You can learn more about it here:

[https://en.wikipedia.org/wiki/B%C3%A9zier_curve](https://en.wikipedia.org/wiki/B%C3%A9zier_curve)

Mozilla has a good article on how to use the curves to draw:

[https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes#bezier_and_quadratic_curves](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes#bezier_and_quadratic_curves)

This is what the rock looks like in the game:

![](Images/image00479.jpeg)

In general, it’s a lot easier to just use a vector drawing program to generate the drawing code for you. For example, I spent more time in Inkscape refining the rock a bit more and copying the generated drawing code over the old drawing code, and came up with this:

CreateStoneTileImage(tile_canvas, tile_ctx)

{

 //format for arc(angles in "radians"/ Math.PI):  arc(x, y, radius, startAngle, endAngle)

 let  ctx = tile_ctx;

// #path8902

 ctx.beginPath();

 ctx.fillStyle = 'rgb(145, 145, 145)';

 ctx.strokeStyle = 'rgb(0, 0, 0)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(26.259351, 2.436401);

 ctx.bezierCurveTo(20.537698, 2.244682, 7.201005, 6.603291, 1.088764, 23.347364);

 ctx.bezierCurveTo(0.164719, 30.545345, 2.971184, 49.833056, 7.725955, 63.104766);

 ctx.bezierCurveTo(23.233916, 63.318872, 52.417972, 64.297286, 55.041516, 63.104766);

 ctx.bezierCurveTo(60.338343, 51.711711, 61.512815, 52.899955, 61.632822, 42.363643);

 ctx.bezierCurveTo(56.002553, 27.503631, 49.261347, 8.617523, 26.259351, 2.436401);

 ctx.fill();

 ctx.stroke();

// #path12107

 ctx.beginPath();

 ctx.fillStyle = 'rgb(194, 194, 194)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(26.140407, 2.529717);

 ctx.bezierCurveTo(8.938332, 4.047547, 3.480977, 19.675919, 1.349182, 23.442043);

 ctx.bezierCurveTo(1.220109, 23.670070, 1.544982, 24.081600, 1.802323, 24.075763);

 ctx.bezierCurveTo(45.201030, 23.091445, 52.902576, 22.870841, 47.221381, 15.852893);

 ctx.bezierCurveTo(41.487356, 8.769685, 28.260407, 2.975209, 26.140407, 2.529717);

 ctx.fill();

// #path13488

 ctx.beginPath();

 ctx.fillStyle = 'rgb(118, 118, 118)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(2.867012, 43.173834);

 ctx.lineTo(33.054967, 39.126287);

 ctx.lineTo(49.076507, 47.895972);

 ctx.lineTo(55.041516, 63.104766);

 ctx.lineTo(7.725955, 63.104766);

 ctx.fill();

// #path14810

 ctx.beginPath();

 ctx.fillStyle = 'rgb(82, 82, 82)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(59.701317, 38.451696);

 ctx.lineTo(49.076507, 47.895972);

 ctx.lineTo(55.041516, 63.104766);

 ctx.lineTo(60.544556, 51.268928);

 ctx.lineTo(61.632822, 42.363643);

 ctx.fill();

// #path15538

 ctx.beginPath();

 ctx.fillStyle = 'rgb(162, 162, 162)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(48.233268, 17.370722);

 ctx.lineTo(33.729558, 23.273395);

 ctx.bezierCurveTo(33.076527, 29.233484, 33.448479, 34.123069, 33.054967, 39.126287);

 ctx.lineTo(49.076507, 47.895972);

 ctx.lineTo(59.701317, 38.451696);

 ctx.fill();

// #path17944

 ctx.beginPath();

 ctx.fillStyle = 'rgb(89, 89, 89)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(6.914559, 12.648585);

 ctx.lineTo(18.213962, 23.947986);

 ctx.lineTo(11.636698, 42.161947);

 ctx.lineTo(4.216195, 48.233268);

 ctx.lineTo(1.686478, 33.223615);

 ctx.lineTo(1.088764, 23.347364);

 ctx.fill();

// #path19438

 ctx.beginPath();

 ctx.fillStyle = 'rgb(248, 248, 248)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(6.973555, 13.095532);

 ctx.lineTo(18.213962, 23.947986);

 ctx.lineTo(33.549445, 23.633622);

 ctx.lineTo(32.336180, 39.607631);

 ctx.lineTo(48.536167, 48.436312);

 ctx.lineTo(54.240798, 63.129934);

 ctx.lineTo(55.041516, 63.104764);

 ctx.lineTo(55.041516, 63.104764);

 ctx.lineTo(49.602045, 47.820716);

 ctx.lineTo(33.054967, 39.126287);

 ctx.lineTo(34.436878, 22.895241);

 ctx.lineTo(18.235225, 22.883774);

 ctx.lineTo(7.454899, 12.288358);

 ctx.fill();

// #path23147

 ctx.beginPath();

 ctx.fillStyle = 'rgb(248, 248, 248)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(48.696415, 16.967058);

 ctx.lineTo(33.838257, 23.006180);

 ctx.lineTo(34.509270, 23.964771);

 ctx.lineTo(48.792274, 17.542213);

 ctx.fill();

// #path23147-0

 ctx.beginPath();

 ctx.fillStyle = 'rgb(248, 248, 248)';

 ctx.lineWidth = 1.000000;

 ctx.lineCap = 'butt';

 ctx.lineJoin = 'miter';

 ctx.moveTo(59.816068, 38.151915);

 ctx.lineTo(48.312979, 48.121260);

 ctx.lineTo(49.942582, 48.888133);

 ctx.lineTo(60.391223, 38.151916);

 ctx.fill();

 this.stone_tile.src = tile_canvas.toDataURL("image/png");

}

![](Images/image00480.jpeg)

It’s a lot more code (9 total paths generated), but looks a lot nicer. You could play with any of the graphics more in Inkscape to generate more complicated graphics, but we’ll try to keep it to a minimum, to focus on finishing the game.

We’re getting to the point that it might be worth creating the graphics for the tiles in a rasterization paint program (using pixels, not vector), such as Photoshop.

## Creating and loading graphics using a paint program

I’ll provide a link to the finished graphics on github, so you can load them into your game remotely, or you could just keep the vector based graphics in the game. But I’m going to remake all the tiles in a rasterization paint program, like ArtClash (the free paint program I created) or Photoshop.

You’ll want to create a new image, 64x64, then begin painting in it. I’ll start with the dirt tile, making the whole background a medium brown. Then I put in darker brown areas to be mud clumps, add shadows on the bottom half, highlights on the top. I did a similar technique for all the tiles. The grass I used a grass brush in Photoshop, which makes grass like blades everywhere, alternating between a lighter and darker green.

I saved the images in a sub folder, “assets/imgs”, and all the images inside of it.

Create a new folder in your project called “assets”, and inside of that a new folder called “imgs”.

Go to the github repo, and download the images and save them in your project into the folder you created: “assets/imgs”.

## Loading images from file

To load our rasterized graphics, we’re going to have to add some new code to load the images, before displaying them in the game. I’ve got to warn you, this is a long one.

We’re going to create a new class under our previous classes named “AssetLoader”:

class AssetLoader

{

    constructor()

    {

        this.callback=null;

        this.image_containers = new Array();

    }

    //put images in an array ready to be loaded

    AddImageToQueue(name, src)

    {

        let img_container = new Object();

        img_container.src=src;

        img_container.name=name;

        img_container.loaded=false;

        img_container.image= new Image();

        this.image_containers.push(img_container);

    }

}//end of class AssetLoader

In the constructor, we’ll have a “callback” variable- which will be a function we will call when all of our images load. That way we can fire a function whenever all the images have finished loading. We’ll also create an array that we will store all of our “images” in.

Next, we’ll create a function called “AddImageToQueue”, which will take a name for the image to be identified with (like “dirt”, or “stone”), and an actual source path/ the path from the current folder to get to that image.

We’ll actually just make the “img_container” a generic object initially. You can do it this way in JavaScript, but in other languages, you would need to declare an actual class first.

Next, we’ll set the object to have a variable named “src”, with source location of the image passed in to the function. This is what we’ll actually use to load the image later.

Next, we’ll set the other variables on our custom “img_container” object. The name we passed in, whether the image has finished loading yet (false right now), and create an “image” variable which will hold the actual built in “image” type, that we’ll be able to draw in the canvas. Finally, we’ll add this to our array of images, so that we can load them after we add all the images we plan to load.

Now we can add below the last function (inside the AssetLoader class):

//load all the images in the queue, and pass a function that will run when all the images have loaded

LoadImages(callback)

{

 this.callback=callback;

 for (let  i = 0; i < this.image_containers.length; i++)

    {

 let  img_container = this.image_containers[i];

 img_container.image.src= img_container.src;//set the actual image type source, which will begin loading the image

 let  asset_loader= this;//hack to allow us to access "this" inside the below functions- otherwise "this" becomes the image that was loaded

 img_container.image.onload = function(event) {asset_loader.ImageLoaded(img_container);};

 img_container.image.onerror = function(error) {asset_loader.ImageError(img_container, error);};

    }

 console.log("loading images!");

}

This is our function to be able to load all the images we queued up to load. First we’ll pass in the callback- which function we will call when we’re all done loading the images.

Then we go through all the images using a for loop. We set the actual “image” object src on our custom “img_container” object to the src we passed in earlier. This actually initializes loading the image from disk.

Next we create a temp variable for the class we’re in (asset_loader), because when the image gets loaded below, JavaScript will place us inside the image that was loaded (which will be now “this”), and we won’t have access to our asset_loader. So we have to create a temporary variable that stores what “this” currently is (our asset_loader), so we can use it after the image is loaded.

Next, on the actual image, we set the “onload” function that is built into “Image” to a quick one-line function. It gets passed the event when the image is loaded, but all we care about is the img object we created is now loaded. This function will load for every image we are trying to load, and will call our “asset_loader.ImageLoaded” function, so we can handle when each image is loaded.

Finally, we also handle “onerror”, which will only fire if it has trouble loading our image (if the source file path doesn’t exist, or other issues).

Now we can add below the last function (inside the AssetLoader class):

ImageLoaded(img_container)

{

 console.log("image loaded! ", img_container.src);

 img_container.loaded=true;

 if(this.CheckIfAllImagesLoaded())

    {

 console.log("all images loaded!");

 this.callback();

    }

}

ImageError(img_container, error)

{

 console.log("Couldn't load an image, check above for an error, probably the wrong path", img_container.src, error);

}

The function “ImageLoaded” gets fired for each image when it gets loaded. We pass over our custom “img_container” object, so that we can set its “loaded” property to true. Then we run a function (we’ll define next) to check if all the images are loaded, and if so, we’ll print out that all are loaded, and fire the callback to let the rest of the program know the images are loaded, and we can start the game (which we’ll show soon).

Now we can add below the last function (inside the AssetLoader class):

CheckIfAllImagesLoaded()

{

 let  num_imgs_loaded=0;

 for (let  i = 0; i < this.image_containers.length; i++)

    {

 let  img_container = this.image_containers[i];

 if(img_container.loaded)

 num_imgs_loaded++;

    }

 if(num_imgs_loaded == this.image_containers.length)

 return  true;

 else

 return  false;

}

GetImage(name)

{

 for (let  i = 0; i < this.image_containers.length; i++)

    {

 let  img_container = this.image_containers[i];

 if(img_container.name==name)

 return  img_container;

    }

 return  null;

}

The function “CheckIfAllImagesLoaded” will be run for every image that gets loaded. Since they probably will get loaded out of order (the larger files will take longer, and load last), we have to check for every image if it’s the last of the images to be loaded.

So here we just start with “0 images loaded before checking”, go through all the images, and count how many have been loaded. Afterwards, if the number of images loaded is the same as the total images we tried to load, it means we’re finished loading all of them, and can return that it is true/ finished loading! If not, we’ll return false, and keep waiting until all the images have had “onload” called.

We create a “GetImage” function, which will get passed in a name for one of the tiles, and will look through all of our custom “img_container” objects, look if the name matches what we’re looking for, and return it if it was found (or return null if nothing was found).

We’re done with our “AssetLoader class”, but below that class (outside of it), add a new class:

class Level

{

    constructor(tile_images)

    {

        this.tile_images = tile_images;

    }

}//end of class Level

This will be used to house our level- but right now it will just be used to store the tile images, in order (so 0 for dirt, 1 for stone, etc- the stuff defined in the “Tile” class).

We also should add our tile width and height on our tile class as a static property, instead of having it on our “TileCreator” object, since we won’t be using it anymore:

class Tile

{

    static width=64;

    static height=64;

Now, at the bottom of our program, we’re going to change how we generate tiles. Delete all the tile generation code (everything related to tiles, starting at “new TileImageCreator() at the bottom of the program ), and replace it with:

let  last_width=window.innerWidth;

let  last_height=window.innerHeight;//existing code

let  asset_loader = new  AssetLoader();

asset_loader.AddImageToQueue("dirt", "assets/imgs/dirt.jpg");

asset_loader.AddImageToQueue("stone", "assets/imgs/stone.jpg");

asset_loader.AddImageToQueue("water", "assets/imgs/water.jpg");

asset_loader.AddImageToQueue("grass", "assets/imgs/grass.jpg");

asset_loader.AddImageToQueue("bush", "assets/imgs/bush.jpg");

asset_loader.LoadImages(AllAssetsLoaded);

function  AllAssetsLoaded()

{

 CreateTileMap();

}

We create a new AssetLoader, and we queue up all of our images we want to load. Next, we actually run the function to load the images, passing in our “callback” as “AllAssetsLoaded”, which will get called after all the images have finished loading. Finally, it will call a new function to generate the tiles “CreateTileMap”:

let  tiles = new  Array();

function  CreateTileMap()

{

 // let tile_creator = new TileImageCreator();

 let  tile_images = new  Array(asset_loader.GetImage("dirt"),

 asset_loader.GetImage("stone"),

 asset_loader.GetImage("water"),

 asset_loader.GetImage("grass"),

 asset_loader.GetImage("bush"),

                        );

 let  level = new  Level(tile_images);

 let  screen_width_default=1366;

 let  screen_height_default=768;

 let  num_tiles_x = Math.round(screen_width_default*2 / Tile.width);

 let  num_tiles_y = Math.round(screen_height_default*2 / Tile.height);

 for(let  x= 0;x<num_tiles_x; x++)

    {

 for(let  y= 0;y<num_tiles_y; y++)

        {

 let  type = Math.floor(Math.random()*(Tile.LAST_TYPE+1));//need +1 or doesn't include the highest number/

 // tiles.push(new Tile(x*tile_creator.width_tile, y*tile_creator.height_tile, type, tile_creator.GetTileImage(type)));

 tiles.push(new  Tile(x*Tile.width, y*Tile.height, type, level.tile_images[type].image));

        }

    }

}

We commented out the “tile_creator”, since we are going to be loading the tile graphics from the file, instead of creating them on the fly. We create an array of the images from the “asset_loader”, in the same way they are defined in the Tile class (0 = dirt, 1 = stone, etc). That way we can just refer to their position in this array easily. Next, we pass that to “Level”, which will just hold onto this array of tile images for now.

Then we just create the tiles the same way as before, but use “level.tile_images[type].image” to get the image for each tile.

If you run the program now, it will preload all the images, then fire the function/ callback after they are all finished loading, and generate the world using the tiles loaded from the file!

![](Images/image00481.jpeg)

It’s looking pretty good now, aside from being totally random, and our player is starting to look rather plain compared to the background.

So, let’s load a better character model, so he fits in the world better!

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/8_Creating_world.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/8_Creating_world.html)

# 9. Creating animated/flipbook graphics

## Sprite sheets

There’s a decent amount of work involved with drawing an animated character. You have to look into walk cycles, understand how a walk cycle works, and create graphics for the character walking down, to one side (and mirror it for the other side), and up. So even if you have the character just bobbing up and down with 2 frames of animation, you have to at least have 2 for 3 different directions/ 6 drawings for a quick bobbing walk (and walk cycles usually have more frames than that).

You can learn more here:

[https://en.wikipedia.org/wiki/Walk_cycle](https://en.wikipedia.org/wiki/Walk_cycle)

I found a decent looking animated character for free on craftpix.net:

[https://craftpix.net/freebies/free-3-character-sprite-sheets-pixel-art/](https://craftpix.net/freebies/free-3-character-sprite-sheets-pixel-art/)

![](Images/image00482.gif)

The only negative is there isn’t a “down” or “up” animation, so that can be a future feature that can be added. For now, they’ll just have a left or right walk cycle when moving down/ up.

An issue with that site is they require you to have an account for the “free download”… and quite a wait for it to download. So, you can find basic logins that other people shared on:

[http://bugmenot.com/view/craftpix.net](http://bugmenot.com/view/craftpix.net)

I downloaded the sprite sheet, and added it to the folder with the rest of the image assets. We can now load the image through our asset loader, but it’s a sprite sheet with all the animations for the character, not just a single image. So, we’ll have to break apart the image areas, and create “animations” for a set of images on the sprite sheet.

I also found another sprite sheet that looked useful, if nothing else because it has many rows and columns for the different animations, and some animation sequences on the next row, so it gives us more things to test for creating a sprite sheet loader.

[https://rvros.itch.io/animated-pixel-hero](https://rvros.itch.io/animated-pixel-hero)

![](Images/image00483.jpeg)

## Sprite Sheets and texture atlases

As you can see by looking at those images, a sprite sheet has several “sprites” on it (a sprite being an image that will be displayed in our program). A sprite sheet will generally contain all the animations for a certain character/ item in a game, and might contain multiple characters animations, if there is extra space on the sprite sheet.

It makes things harder- loading a texture, and splitting it up into multiple parts afterwards, not to mention needing to use a special tool to put all the images onto a giant image.

Why would you put them on one texture instead of multiple textures? The biggest reason is that it takes time to switch between images to draw them- so if you can put more images on less textures/ overall image that holds many, it takes a lot less time to draw them, and you get better game speeds (fps).

Another is because it also takes time to open each file- so it ends up taking less time to load a couple big images than a ton of small ones.

You can actually get programs like “texturepacker pro”, which rotates your images, and uses a complex algorithm to try to pack them together as close as possible, to save as much space/ maximize the number of sprites you can store on a texture.

Sprite sheets and texture atlases are the same sort of idea. A texture atlas generally will contain more advanced packing algorithms, and will include a text (usually JSON notation) file that describes where each section is, so that you can pull images off it easily.

A sprite sheet on the other hand, is usually just a grid of even sized boxes containing the sprites. All you have to know is how big each tile of sprites in the sprite sheet are, and can figure out where each sprite is.

Our plan is to first create a class to display all of our sprites- from the tiles, player, enemies, NPC’s. They’ll all have in common an x and y position to draw on screen, and width and height to draw them, and either an image, or animations to draw.

## A debug box class

We can create a small debug box class to be able to check where a sprite/ animation is onscreen, compared to where it’s drawn. There is blank space in some frames of the animations, which makes it difficult to see where it’s actually being drawn. So, this makes it easier to see how to align/ position animations relative to the sprite they are in. Add this to the bottom of your classes:

//for drawing debug boxes around sprites, animations, etc

class  DebugBox

{

 constructor()

    {

    }

 DrawDebugBox(ctx, x, y, width, height, thickness, color)

    {

 ctx.fillStyle = color;

 ctx.fillRect(x, y, width, thickness);//top

 ctx.fillRect(x, y+height-thickness, width, thickness);//bottom

 ctx.fillRect(x, y, thickness, height);//left

 ctx.fillRect(x+width-thickness, y, thickness, height);//right

    }

}//end of class DebugBox

## Creating a sprite class

We’ll create a sprite class, which will mainly be in charge of keeping track of the x and y positions, width, height, and be able to draw out images or animations to that position + size.

class  Sprite

{

 constructor(x,y, width, height, image)

    {

 this.x=x;

 this.y=y;

 if(width==undefined)

 width=Tile.width;

 if(height==undefined)

 height=Tile.height;

 this.width=width;

 this.height=height;

 this.image=image;

 this.animations = new  Array();

 this.curr_anim=0;

 this.flip_x=false;

    }

 Draw(ctx, delta_ms)

    {

 if(this.image!=undefined)

 ctx.drawImage(this.image, this.x, this.y);

 if(this.animations.length>0)

        {

 this.animations[this.curr_anim].Draw(ctx, delta_ms, this.x, this.y, this.flip_x);

        }

    }

}//end of class Sprite

A sprite has a position (x,y, or horizontal and vertical) that it is drawn at on the screen, the width and height of the image/ animation, and possibly an image passed over.

We’ll check to see if width and height are undefined (meaning they didn’t get passed in for this sprite), and if so, we’re going to use the default tile size for both.

We’ll also assign the image (if one wasn’t passed over, it will also be undefined). We create an array for any possible animations to go into, and set the current animation as the first one (0). We also set the “flip_x” to false, which will be used to flip the animation when the sprite is moving left instead of right (which all the sprites are drawn facing).

Next, the “Draw” function will get the context to draw on, and the delta time in milliseconds, so we can pass it to any animations, so they can move to the next frame in the animation if enough time has passed (at 60fps, 1/60 = 0.016s per frame, or 16ms). Then we draw whatever the current animation is, if we have any in the array. We pass over anything that will be needed to draw the animation.

## Creating an entity and player class

We’ll also want to create an “entity” class, which will be a more advanced version of a sprite. We’ll use this for our main player, NPC’s, enemies- anything that will move around/ animate.

class  Entity  extends  Sprite

{

 static  DIRECTION = {UP:0, DOWN:1, LEFT:2, RIGHT:3};

 static  STATE = {IDLE:0, WALKING:1, RUNNING:2, ATTACKING:3};

 constructor(x,y, width, height, image)

    {

 super(x,y, width, height, image);

 this.state=Entity.STATE.IDLE;

 this.dir=Entity.DIRECTION.DOWN;

 this.x_dest=0;

 this.y_dest=0;

 this.moving_x=false;

 this.moving_y=false;

 this.move_speed= 0.2;

 //a way to store a state + animation, so we can add animations for states- in the format of an object with {state, animation}

 this.state_to_anim = new  Array();

    }

}//end of class Entity

The first new thing we’re using here is “extends”- an entity will be a sprite, get all of its variables and functions, but also be able to add its own new variables and functions, or even override/ replace functions we created in the sprite class! We could have copied all the sprite code into here instead, but it’s cleaner to be able to just have access to all the sprites functionality, without having to duplicate all the code.

An entity will have “static” variables on it, so we can access them for all entities, even without creating any instance of an entity. In most languages we can create “enums”, which are words that automatically get assigned a number, starting at 0 and going up. In JavaScript we don’t have it, so we made something similar, creating 2 objects called “DIRECTION” and “STATE”, which have their own variables, which we assign numbers to, starting at 0, to uniquely identify each word.

This will allow us to check if an entity is moving “DIRECTION.UP”, or if its state is “STATE.ATTACKING”, and it will really just be checking to see if the number matches up, but allows us to use text to check what it is doing. I do static variables in all caps, to visually show myself it’s not a variable that each unique object can change, but a variable set on the entire class.

In the constructor, we pass over everything the sprite class needed, and we can even call the constructor for the sprite class using “super(…)“, since the class we extended is referred to as the “super class”. This just calls the sprites constructor also, and initializes everything the sprite needs to.

Next, we set all the default variables that entity’s specifically need. The state they start in (idle), the default direction (down), their destination, and the variable related to moving, and finally an array that will associate a certain state with a certain animation, so that we can look up which animation to use if we’re in a given state (like walking, or attacking, etc).

We need to add several functions to this class to complete its functionality:

Draw(ctx, delta_ms)

{

 super.Draw(ctx, delta_ms);

 this.MoveToDest(delta_ms);

}

The “Draw” function just takes in what we need to be able to draw (context and time that has passed since the last frame), calls the “super.Draw” function, which calls the base “Sprite” class “Draw” function. Next we call the “MoveToDest” function, which we’ll get from our original “Friend” class, that will allow our Entity to check if it needs to move somewhere, and to move there.

Next add another function:

ChangeState(new_state)

{

 if(this.state!=new_state||this.dir!=this.curr_anim.dir)

    {

 console.log("changing state to: "+new_state);

 this.state=new_state;

 let  new_anim = this.GetAnimIndex(this.state);

 if(new_anim!=-1)

        {

 this.curr_anim=new_anim;

 this.animations[this.curr_anim].frame=0;

        }

    }

}

The “ChangeState” function will get passed in a new state. If it isn’t the state we currently are in, we’ll then set the state to the new state. We’ll then try to grab the animation for this state- if it’s -1, it means it couldn’t be found (since the animations are in an array, which always starts at 0). If it isn’t -1, we’re going to be playing a different animation, so we’ll set the number we found as the new current animation, and set that animation back to frame 0/ resetting the animation.

Next add another function:

ChangeDirection(direction)

{

 if(this.dir!=direction)

    {

 this.dir=direction;

 //should also flip animation to go left if they weren't

 if(this.dir==Entity.DIRECTION.LEFT)

 this.flip_x=true;

 else  if(this.dir==Entity.DIRECTION.RIGHT)

 this.flip_x=false;    

 //also force it to update the animation being played if the direction changed:

 this.ChangeState(this.state);       

    }

}

The “ChangeDirection” function will be passed in a direction, and if the direction is different than the current one, it will set it, and set “flip_x” to true if that direction is left. This will allow us to tell the flipbook animation to flip and reposition when rendering.

Next add another function from our “friend” class:

SetDestination(x_dest, y_dest)

{

 this.x_dest=x_dest;

 this.y_dest=y_dest;

 this.moving_x=true;

 this.moving_y=true;

 this.ChangeState(Entity.STATE.WALKING);

}

The “SetDestination” function will take in the x and y destination, set it, and set the moving state for both to be true, and change the entity state to walking, since now it has a destination set.

Next add another function from our “friend” class:

MoveToDest(delta_ms)

{

 let  was_moving = false;

 if(this.moving_x)

    {

 was_moving=true;

 if(this.x_dest>this.x)

        {

 this.ChangeDirection(Entity.DIRECTION.RIGHT);

 this.x+=this.move_speed*delta_ms;

 if(this.x>=this.x_dest)

            {

 this.x=this.x_dest;

 this.moving_x=false;

            }

        }

 else  //x_dest < x -so need to move to the left/ -x

        {

 this.ChangeDirection(Entity.DIRECTION.LEFT);

 this.x-=this.move_speed*delta_ms;

 if(this.x<=this.x_dest)

            {

 this.x=this.x_dest;

 this.moving_x=false;

            }

        }

    }

 if(this.moving_y)

    {

 was_moving=true;

 if(this.y_dest>this.y) // if dest is greater, move him down, where y increases

        {

 this.ChangeDirection(Entity.DIRECTION.DOWN);

 this.y+=this.move_speed*delta_ms;

 if(this.y>=this.y_dest)

            {

 this.y=this.y_dest;

 this.moving_y=false;

            }

        }

 else  //y_dest < y -so need to move upward/ -y

        {

 this.ChangeDirection(Entity.DIRECTION.UP);

 this.y-=this.move_speed*delta_ms;

 if(this.y<=this.y_dest)

            {

 this.y=this.y_dest;

 this.moving_y=false;

            }

        }

    }

 if(was_moving)

 if(!this.moving_y && !this.moving_x)

 this.ChangeState(Entity.STATE.IDLE);

}

The “MoveToDest” function is pretty much as it was in our friend class. But we’re also going to track “was_moving”, to see if the entity had a destination, but reached it- so we can then change the state to idle if they’ve reached it. We also change the direction to left or right if the entity is moving left or right, which will change the animation direction

Next add another function:

AddAnimation(anim, anim_state, direction)

{

 this.animations.push(anim);

 this.state_to_anim.push({state:anim_state, anim_index:this.animations.length-1, dir:direction});

}

This function will just be passed in an animation, and which state this animation will play when in. It will add the animation to our array of animations.Then it will push a new object, which will store which state, and the index of where the animation was added to the array (whatever the length of the array is, -1, since the index is 1 less than the length). We also add a direction, so in the future we can play different animations for the different directions a player/entity is facing.

The last function to add:

GetAnimIndex(anim_state)

{

 let  anim_index=-1;

 for (let  i = 0; i < this.state_to_anim.length; i++)

    {

 if(this.state_to_anim[i].state == anim_state)

        {

 if(this.state_to_anim[i].dir==this.dir|| this.state_to_anim[i].dir==undefined)

            {

 anim_index= this.state_to_anim[i].anim_index;           

 break;

            }

        }

    }

 return  anim_index;

}

The “GetAnimIndex” will be passed in a state, then will look through the array of states related to animations, find the state we’re looking for, and will return the index of that animation, so that we can play the animation for that state. We initially have the animation index set to “-1”, since an array starts at 0, it can never be -1, so we know we didn’t find an animation for this state if it stays -1.

We’ll also look to see if the direction of the animation is the same as the direction of our entity, or if no direction is defined for this animation, then we’ll just use it anyways. That way if we later on have different animations for different directions, it will grab the right animation (such as an animation for walking right instead of down). But for now it can also be undefined, so if we don’t have animations for multiple directions, it can still use it.

We’ll finally create a new class after this one:

class Player extends Entity

{

    Draw(ctx, delta_ms)

    {

        super.Draw(ctx, delta_ms);

    }

}

This “player” class extends the Entity class, but only has a “Draw” function in it, which just calls the super/ Entity class’s draw function. Right now it doesn’t really do much, but we’ll add more later to differentiate a player from a different type of entity.

## Creating an animation class

So, let’s create a class to load sprite sheets, figure out where each frame is for animation, and be able to display it as an animation on screen.

We’ll want to pass in the image, how wide and tall a frame will be, which column (x direction) and row (y direction) the animation starts in, and how many frames the animation is. Using this, we can find where in the sprite atlas our animation is, and be able to split out where each frame for the animation is.

Next, we’ll also want to pass over information so that it can be drawn, such as the width we want it drawn on, in case the sprite sheet sprites are a different size than what we want drawn in our game. Additionally, we also want to pass how long to wait to change to the next frame, which will control the speed the animation plays at.

Create a new class at the bottom of your classes:

class FlipBookAnimation

{

    //image, size of each frame, where the animation starts, how many frames, scale to draw onscreen, how long to wait in before changing to the next frame

    constructor(image, width_frame, height_frame,

                    start_column_x, start_row_y, 

                    num_frames,

                    scale,

                    delay_ms)

    {

        this.image=image;

        this.width_frame=width_frame;

        this.height_frame=height_frame;

        this.num_frames=num_frames;

        this.scale=scale;

        this.delay_ms=delay_ms;

        this.width_drawn=width_frame*scale;

        this.height_drawn=height_frame*scale;

        this.timer=0; //timer for switching to next frame

        this.frame=0; // current frame, going from 0 to num_frames-1

        //offsets to draw with an offset/ centered around the parent object

        this.offset_x=0;

        this.offset_y=0;

 //if we don't always want the frame centered- since frames can be wide for other animations (like a wide attack vs narrow idle), we can offset them from center more

 this.offset_x_extra=0;

 this.offset_y_extra=0;

        //frames will be x and y positions in the texture atlas, assuming moving from left to right, and possibly wrapping onto new rows

        this.frames = new Array();

        //start columns from the user will start at 1- but in here we need to start at 0

        start_column_x--;

        start_row_y--;

        let x=start_column_x*width_frame;

        let y=start_row_y*height_frame;

        //figure out the x and y position of each frame

        while(this.frames.length<this.num_frames)

        {

            this.frames.push({x:x, y:y});

            x+=width_frame;

            if(x>image.width)//if the x is now outside the image/ passed the right side of our texture atlas, have it wrap down to the start of the next row

            {

                x=0;

                y+=height_frame;

            }

        }

    }

} //end of class FlipBookAnimation

First, we pass in everything that we’ll need to figure out where our frames will be, and what we need to be able to draw a frame out.

We pass in the sprite sheet image, the width and height of each frame, the start column and row of the animation we’re looking for, and how many frames long the animation goes for. We also pass in what we’ll scale the original frame size to when we draw the frames out on screen; in case the sprite sheet uses smaller/ larger sprites than we want to use in our game. Lastly, we pass in the delay we want between changing frames, so we can slow down animations by increasing the delay, or speed them up by decreasing the delay.

We assign all the variables passed in to the object’s variables (“this” to assign it to the current object). We figure out the width and height of what we’ll draw to screen (scale * frame width and height).

We set the timer to 0, which will be used to count how long the total time has been between each frame change. We set the current frame to be 0/ the first one.

We’re going to have x and y offsets to position the animation differently, depending on the dimensions of the parent. For instance, if the parent/player is less wide than the animation (which is the case for the animations), we’ll want to center the animations so it looks more correct.

We also assume the user will give us the column and row the animation is in starting at “the first column/ row” / 1, instead of “the 0 column or row”, so we have to minus 1 to change it to start with 0, since that is the way they’ll be taken out of the main image (the left top is 0,0, the next frame would be 0+width, next 0+width*2, etc.).

Next, we’re going to start grabbing the frame positions out of the overall image. We set the start row and column to be whichever one they gave us (but starting at 0), and multiply it by the width and height of each frame to go to the correct starting position for the frame in the image.

Now, we check “while” we haven’t gotten all the frames yet (the length of our frames array is less than the number of frames we’re looking for), we’ll keep grabbing more frames. We’ll push in the current frame position (the start position initially), and then move one frame to the right (by adding in the width of the frame). If the current position + the width of the frame is greater than the full image width, we’ve gone too far over to the right side/ off the image, so we need to reset x back to 0, so it will be on the left side of the image, and increase y by one frame height, to go onto the next row.

We then repeat this until we have all of our frames!

We also need to add a function into this class to be able to draw out our animation. So, add this function to the “FlipBookAnimation” class:

Draw(ctx, delta_ms, x, y, flip_x)

{

 //if flipped, have to save, then flip the entire canvas, draw, then restore the original canvas drawing

 if(!flip_x)

    {

 debug_boxes.DrawDebugBox(ctx, x+this.offset_x, y+this.offset_y, this.width_drawn, this.height_drawn, 2, "#0000ff");

 ctx.drawImage(this.image,

 this.frames[this.frame].x, this.frames[this.frame].y,

 this.width_frame, this.height_frame,

 x+this.offset_x+this.offset_x_extra, y+this.offset_y+this.offset_y_extra,

 this.width_drawn, this.height_drawn);

    }

 else

    {

 ctx.save();

 ctx.scale(-1, 1);

 debug_boxes.DrawDebugBox(ctx, -x-(this.width_drawn+this.offset_x), y, this.width_drawn, this.height_drawn, 2, "#0000ff");

 ctx.drawImage(this.image,

 this.frames[this.frame].x, this.frames[this.frame].y,

 this.width_frame, this.height_frame,

                    -(x+this.offset_x-this.offset_x_extra+this.width_drawn), y+this.offset_y+this.offset_y_extra,

 this.width_drawn, this.height_drawn);

 ctx.restore();

    }

 this.timer+=delta_ms;

 if(this.timer>this.delay_ms)

    {

 this.timer=0;

 this.frame++;

 if(this.frame==this.num_frames)//the maximum frame should be 1 less than the number of frames, since frames start at 0

 this.frame=0;

    }        

}

The “Draw” function takes in the canvas context, the delta_ms/ how much time has passed since the last frame in ms, and the x and y position to draw the animation at, as well as if we want to try “flipping” the animation. By default, they drew out all the animations facing right, but we can flip them to face left instead. We’ll check to draw the “not flipped”/ “!flipped” version first, since that’s more straightforward.

We’ll add a new class later on to draw debug boxes (boxes that let us see where our player, or the animation are being rendered). But we’ll call the drawing function now, passing in the context, the x position we’re drawing to + whatever offset we are drawing the animation off (to center it inside our player object), the same thing with the y position, the width and height of the animation being drawn, how big we want the borders of our box, and the color we want the box to be drawn.

Next, we actually call the drawing function, passing in the overall image, the x and y position of the current frame, the width and height of the frame, the x and y position on screen to draw it at, and finally, the width and height to draw the frame on screen.

To flip the image, it’s more difficult than a lot of other interfaces/ game engines. Normally we just draw it with a negative width, which flips it, then have to move it to the right by its width, to make up for drawing it in a negative direction.

But for drawing with the canvas, we need to save the current state, scale the canvas in the negative direction (-1 or 100% negative in the x direction), then we can draw with everything backwards. The only thing that changes what we draw when flipped is we have to draw the x position negative, and minus out the width to have it drawn in the same spot as when facing right. Lastly, we restore the canvas, to unflip it/ scale it back to 1 in the x direction.

We then increase our timer based on the “delta_ms”/ time that has passed since the last frame was drawn.

We check to see if this timer is now greater than the delay we were waiting for to go to the next frame. If it is greater, we first reset the timer to 0 so it can start counting again in the next update. We increase which frame we’re on, but if we’ve made it to the total number of frames, we’ve gone past the number of frames we have, so need to reset back at the first frame again (0), to loop the animation, and have it play again.

Lastly, we need one more function to center an animation inside of its parent (since the animation is wider than our tile size).

CenterSize(parent_width, parent_height)

{

 this.offset_x= parent_width*.5-this.width_drawn*.5;

 this.offset_y= parent_height*.5-this.height_drawn*.5;

}

This just takes the parent width and height, sets the offset to half the parents width/height (which would have it start drawing from the center), then subtracts its own width and height, which centers it inside the parent.

Now we actually have a class that can extract frames from a sprite sheet, and draw them. Time to use them in the game!

## Using the animation class to play animations

On the bottom where we load the tile images, add the following:

asset_loader.AddImageToQueue("woodcutter_idle", "assets/imgs/Woodcutter_idle.png");

asset_loader.AddImageToQueue("woodcutter_run", "assets/imgs/Woodcutter_run.png");

asset_loader.AddImageToQueue("woodcutter_attack1", "assets/imgs/Woodcutter_attack1.png");

asset_loader.AddImageToQueue("adventurer", "assets/imgs/adventurer-v1.5-Sheet.png");

This will load the images, so change the “AllAssetsLoaded” area to (also comment out the existing: “SetupInput()” at the bottom, since we’re moving it to this inside the “AllAssetsLoaded” function):

let  sprites = new  Array();

let  my_player;

let  an_entity;

let  debug_boxes = new  DebugBox();

function  AllAssetsLoaded()

{

 CreateTileMap();

 my_player = new  Player(0,0,Tile.width, Tile.height);

 let  scale_woodcutter = my_player.height / 48;

 let  woodcutter_idle = new  FlipBookAnimation(asset_loader.GetImage("woodcutter_idle").image, 48, 48, 1,1, 4, scale_woodcutter, 100);

 let  woodcutter_run = new  FlipBookAnimation(asset_loader.GetImage("woodcutter_run").image, 48, 48, 1,1, 6, scale_woodcutter, 100);

 let  woodcutter_attack1 = new  FlipBookAnimation(asset_loader.GetImage("woodcutter_attack1").image, 48, 48, 1,1, 6, scale_woodcutter, 100);

 woodcutter_idle.CenterSize(my_player.width, my_player.height);

 woodcutter_run.CenterSize(my_player.width, my_player.height);

 woodcutter_attack1.CenterSize(my_player.width, my_player.height);

 woodcutter_idle.offset_x_extra=12;

 woodcutter_run.offset_x_extra=10;

 my_player.AddAnimation(woodcutter_idle, Entity.STATE.IDLE);

 my_player.AddAnimation(woodcutter_run, Entity.STATE.WALKING);

 my_player.AddAnimation(woodcutter_attack1, Entity.STATE.ATTACKING);

 my_player.ChangeState(Entity.STATE.ATTACKING);

 an_entity = new  Entity(Tile.width*3,Tile.width*2,Tile.width, Tile.height);

 let  scale_adventurer = my_player.height / 37;

 let  adventurer_idle = new  FlipBookAnimation(asset_loader.GetImage("adventurer").image, 50, 37, 1,1, 4, scale_adventurer, 100);

 let  adventurer_run = new  FlipBookAnimation(asset_loader.GetImage("adventurer").image, 50, 37, 2,2, 5, scale_adventurer, 100);

 let  adventurer_attack1 = new  FlipBookAnimation(asset_loader.GetImage("adventurer").image, 50, 37, 6,7, 6, scale_adventurer, 100);

 adventurer_idle.CenterSize(my_player.width, my_player.height);

 adventurer_run.CenterSize(my_player.width, my_player.height);

 adventurer_attack1.CenterSize(my_player.width, my_player.height);

 an_entity.AddAnimation(adventurer_idle, Entity.STATE.IDLE);

 an_entity.AddAnimation(adventurer_run, Entity.STATE.WALKING);

 an_entity.ChangeState(Entity.STATE.WALKING);

 sprites.push(my_player);

 sprites.push(an_entity);

 SetupInput();

}

We create the array “sprites” for all of our sprites to be put into, so that we can go through this array in the game, and draw out any sprites we add easily. We also create a variable for “my_player”, and “debug_boxes”, so we can use these.

After all the assets are loaded, we initialize our player, being the size of a tile.

Then we create the animations for the woodcutter sprites. We set the scale to scale the woodcutter sprites to be the height of our player divided by the height of the woodcutter frames (each frame is 48), so that we can scale down the wood cutter to fit our player height (the width of the animation can be wider than our player box, since attacking animation will go outside of the player box).

Next, we create variables for the different types of animation, passing in the width and height of each frame, which column (x) and row (y) to start the animation on, the number of frames to use for the animation, the scale that we want to draw it on screen, and the delay between each frame being changed out.

We also use “CenterSize” to center the animation around the player's width and height (so it will be centered/ drawn from the middle, vs from the left side like normal), so animations will be all centered on where our player is. Additionally, some animations we don’t want centered. For instance, the idle animation is at the left edge of the frame, because the attack frame makes the frame size much wider, but we want it to be drawn centered. So, we can add extra offset to not have it drawn centered, based on its frame size, and give it a little bit of an offset to make it look better. 

Lastly, we just set the player state to attacking, to show that we can set the state, which will change the animation.

Next, we create an entity, at 3 tile widths over to the right, and 2 tile widths down (Tile.width*3,Tile.width*2), we add the animations to their animations array, and we change the entity state to walking, just to show how to change the state, which then also changes the current animation playing again.

Finally, we add both sprites (both Entities and Players are extended from sprites) to our sprites array.

Now we’ve done everything, aside from actually rendering out the animated sprites. In “UpdateGame”, add at the bottom:

if(sprites!=undefined)

{

 for (let  i = 0; i < sprites.length; i++)

    {

 const  sprite = sprites[i];

 //draw a debug box in red for each sprite at its x and y, and width and height

 debug_boxes.DrawDebugBox(ctx, sprite.x, sprite.y, sprite.width, sprite.height, 2, "#FF0000");

 sprite.Draw(ctx, delta_ms);

    }

}

This just checks to make sure sprites isn’t undefined (which it is before we add our sprites), then goes through however many sprites there are, first drawing a debugbox out for where the sprite is, then calling the draw function for each.

If you run this now, you should see 2 different sprites on screen, playing out their animations:

![](Images/image00484.jpeg)

But we can still see our friend being rendered behind them. So, let’s change them out with an animated character, and have the animated character move around when we click on the screen.

## Moving controls from Friend to Player Class

We’re going to heavily modify our “Player” class based on the existing “Friend” class, which represents the object the player controls. The player right now is almost identical to the entity class, so let’s add functions from the friend class into the player.

First, we’ll remove all our references to our friend class. Search for and remove the line: “let timmy = new Friend(” at the bottom of the script. Next remove these 2 lines in “UpdateGame”:

timmy.Update(delta_ms);

timmy.DrawFriend(); //re-draw Timmy

Next find the function: “MoveMyPlayer”, and change it to (by changing “timmy” to “my_player” :

function  MoveMyPlayer(x_dest, y_dest)

{

 //move my_player to the destination clicked

 console.log("Moving my player to destination: x: "+x_dest+", y: "+y_dest)

 my_player.SetDestination(x_dest, y_dest);

}

The “SetDestination” function is the one our “Entity” class has, which allows us to move an entity towards a certain point.

Go check the game out, and when you click, the player will be able to move to where the click happened, just like the “Friend” class was able to do before!

![](Images/image00485.jpeg)

Now we have a character that can move around in the world, be controlled by the user, changes state, direction, and animation while moving. But we can see the part of the world as wide as the screen being visible right now, even though we made the world wider than the screen. So, in the next section, we’ll add a “Camera” to follow the player, which will allow them to explore the larger map!

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/9_Animated_graphics.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/9_Animated_graphics.html)

# 10. Making a "camera" to follow the player

## Creating a Camera

We’ll want to create a camera to be able to move around to see the larger world around our character, as well as to follow our character as he approaches offscreen.

So, we’ll create a “Camera” class, knowing we’ll want to position it with x and y:

class  Camera

{

 //camera will be moved using its x and y position, to show where it is in the world

 constructor(x,y)

    {

 this.x=x;

 this.y=y;

    }

}//end of class Camera

Next, we’ll actually want the camera to be the thing that draws out the world and the character (so it can move the world around our character when our character moves). Take all the drawing code from update game and move it to our “Camera” class under a new function “Draw

class  Camera

{

 //camera will be moved using its x and y position, to show where it is in the world

 constructor(x,y)

    {

 if(x==undefined)

        {

 x=0;

 y=0;

        }

 this.x=x;

 this.y=y;

    }

 //camera will draw out everything based on its own positon

 Draw(ctx, delta_ms)

    {

 for (let  i=0; i < tiles.length; i++)

        {

 tiles[i].Draw(ctx);

        }

 if(sprites!=undefined)

        {

 for (let  i = 0; i < sprites.length; i++)

            {

 const  sprite = sprites[i];

 //draw a debug box in red for each sprite at its x and y, and width and height  

 debug_boxes.DrawDebugBox(ctx, sprite.x, sprite.y, sprite.width, sprite.height, 2, "#FF0000");

 sprite.Draw(ctx, delta_ms);

            }

        }

    }

}//end of class Camera

Now we’ll actually want to call this drawing code from our “UpdateGame” function, so we’ll be essentially doing the same thing as before:

function  UpdateGame(delta_ms)

{

 ClearCanvas(ctx, "rgba(0,0,255,255)"); //clears the canvas, so we don't get "ghosting"

 camera.Draw(ctx, delta_ms);

}

Finally, lets create our camera towards the bottom of our script file, after “SetupInput, and before “let fps_txt_element = document.getElementById("fps");”

let  camera = new  Camera(0, 0);

If you run it now, everything should look the same, which means we just put the drawing functionality into our camera class. So now we’ll want to be able to move the position of our camera, which will cause the screen to move in the opposite direction. Lets move our camera over by “-window.innerWidth / 2” (1/2 a screen width to the left):

let  camera = new  Camera(-window.innerWidth/2, 0);

Nothing should change yet, since we haven’t actually used the camera x and y values yet. So, we’ll move everything over based on the camera's position, in tiles and in entities drawing functions.

So, in your “class Tile”, update your draw function to draw based on the camera's position:

Draw(ctx)

{

 ctx.drawImage(this.image, this.x-camera.x, this.y-camera.y);

}

If you run this now, you’ll see your tiles are offset by half the screen width, how it should be. But now we have to also offset our sprites. In your sprite class, change your draw function to add in the camera position as well:

Draw(ctx, delta_ms)

{

 if(this.image!=undefined)

 ctx.drawImage(this.image, this.x-camera.x, this.y-camera.y);

 if(this.animations.length>0)

    {

 this.animations[this.curr_anim].Draw(ctx, delta_ms, this.x-camera.x, this.y-camera.y, this.flip_x);

    }

}

When you run this, you’ll see everything except the debug boxes are now moved over. These are being drawn from our “Camera” class, so in that function, change the line for drawing the debug boxes to:

debug_boxes.DrawDebugBox(ctx, sprite.x-camera.x, sprite.y-camera.y, sprite.width, sprite.height, 2, "#FF0000");

Now you should be able to see all our stuff moved over with the camera positioned! Just to make sure the y value is also working, change the camera initialization to be offset by half the height in the y direction:

let  camera = new  Camera(-window.innerWidth/2, -window.innerHeight/2);

When you run this, you should see the top corner of the world, and all the sprites offset by half the width in the x direction, and half the height in the y direction!

We could at this point change the x and y camera position to move our camera around manually with the arrow keys to see it move around, but we instead want the camera to center on our Player sprite, and follow him around as he moves.

![](Images/image00486.jpeg)

So, let’s add a function on the camera to follow our player, but make it able to follow any sprite.

## Making the camera follow the player

We want the player to be centered on the screen. The center of the screen is the width of our screen, divided in half (which is the midpoint), as well as the height divided in half. But since the sprites are drawn from their top left corner, they would be drawn with their left side on the centerline. To get them centered in the middle, we have to subtract out half the width and height of the sprite as well, so it gets moved over to the left half a width, and up half a height, so his center is dead center with the center of the screen.

Update the camera class in the following way:

//camera will be moved using its x and y position, to show where it is in the world

constructor(x,y)

{

 this.x=x;

 this.y=y;

 //used to center target in the middle of the screen

 this.target=undefined;

 this.half_width_minus_target_half_width=0;

 this.half_height_minus_target_half_height=0;

 console.log("camera x: "+this.x);

}

Follow(target)

{

 this.target=target;

 this.half_width_minus_target_half_width = window.innerWidth*.5 - target.width*.5;

 this.half_height_minus_target_half_height = window.innerHeight*.5 - target.height*.5;

}

We create a “Follow” function that will be passed a sprite. We’ll set the things we need to follow that sprite- storing a reference to that sprite in the first line of “Follow”. Next we store the value in a very long variable name for half the width and height of the screen, minus half the width and height of the sprite to get him perfectly centered.

We’ll additionally want to add an “Update” function, so that when the target moves, our camera will also update its position. Add below the Draw function:

Update(delta_ms)

{

 if(this.target!=undefined)

    {

 this.x=this.target.x-this.half_width_minus_target_half_width;

 this.y=this.target.y-this.half_height_minus_target_half_height;

    }

}

This will just take in the delta time/ frame rate, but not do anything with it yet. We’ll check to make sure we have a target, and if so, we’ll update our x and y to be the same as the targets, which would put our top left corner of the screen at the top left corner of the sprite. But we subtract out the half screen width/ height, and sprite half width/height, which will get the sprite to always be centered on the screen.

Next you actually have to call the “Update” function, so we’ll just call it from our “Draw” function, since it’s already being called every frame update:

Draw(ctx, delta_ms)

{

 this.Update(delta_ms);

    ...

Now the camera is ready to be able to update its position when it has a target. Let’s give it one!

At the bottom of your script, in the “AllAssetsLoaded()” function, at the bottom add the call to the camera.follow function:

   ...

 SetupInput();

 camera.Follow(my_player);

}

Now if you refresh, you’ll see the player centered on the screen, and if you click around, you’ll see him move around the world, while also staying in the center of the screen!

![](Images/image00486.jpeg)

You’ve probably noticed one major issue now- when you click somewhere, the player no longer goes to the correct position in the world where you clicked. This is because the camera is offsetting the world, but the click position is not aware that we’re moving the camera/ world around. So we just need to add our camera offset when we get the click position.

## Fixing input position based on camera position

To fix this, change the function “MoveMyPlayer” to include the camera position as follows:

function  MoveMyPlayer(x_dest, y_dest)

{

 //add in the offset of the camera to accurately move our player around the world.

 x_dest=x_dest+camera.x;

 y_dest=y_dest+camera.y;

 //move my_player to the destination clicked

 console.log("Moving my player to destination: x: "+x_dest+", y: "+y_dest)

 my_player.SetDestination(x_dest, y_dest);

}

Now if you click around the world, the player actually goes to where you clicked, regardless of where the camera is scrolled! 

But one other issue, if you click the center of a tile, you would expect your player to also go and sit in the center of the tile. Right now he is being placed based on the top left, so we’ll also want to subtract out half his width and height from the click position, to get him centered. So update it to:

function  MoveMyPlayer(x_dest, y_dest)

{

 //add in the offset of the camera to accurately move our player around the world.

 x_dest=x_dest+camera.x;

 y_dest=y_dest+camera.y;

 //center player on where mouse click happened, instead of positioning the top left there:

 x_dest=x_dest-my_player.width*.5;

 y_dest=y_dest-my_player.height*.5;

 //move my_player to the destination clicked

 console.log("Moving my player to destination: x: "+x_dest+", y: "+y_dest)

 my_player.SetDestination(x_dest, y_dest);

}

Now when you click around, you’ll see that the player goes to that position, but centers themselves on it!

But now we also want to make sure the player can’t wander off the world, and that we don’t see the ugly blue clear color when he’s wandering around, so we’re going to add some limits to how far the camera can move.

## Adding in camera boundaries

To add in camera boundaries, we’re going to make sure the top left of it never goes past the top left of the world, the bottom right doesn’t go past the bottom right of our world, and so on. We’ll set it up so that the camera will always follow the player, except in these cases.

What we want to say is “don’t go past our world boundaries and show the blue background”. Since we know our world starts at x=0, y=0, we can first tell it to not go below this.

So, change our cameras “Update” function to stop it from going below 0 in the x and y:

Update(delta_ms)

{

 if(this.target!=undefined)

    {

 this.x=this.target.x-this.half_width_minus_target_half_width;

 this.y=this.target.y-this.half_height_minus_target_half_height;

 if(this.x<0)

 this.x=0;

 if(this.y<0)

 this.y=0;

    }

}

Now if you move around the world, you’ll see that it doesn’t show the blue background in the top left corner, but follows the player, except in that situation. So now let’s also make it so it doesn’t go past the other 3 corners.

To do this, we need to know the width and height of the world, and make sure the right side of the camera (camera.x + window.innerWidth) doesn’t go past the right side of the map.

We could calculate how wide the tiles are * the number of tiles in the x direction, but let’s instead add this functionality to the level class. We’ll move all the Tile generation code after “new Level()” at the bottom into a new function in the “Level” class, and add variables to the constructor for things we want to keep track of:

class  Level

{

 constructor(tile_images)

    {

 this.tile_images = tile_images;

 this.num_tiles_x=1;

 this.num_tiles_y=1;

 this.width=this.num_tiles_x*Tile.width;

 this.height=this.num_tiles_y*Tile.height;

    }

 CreateLevel(screen_widths, screen_heights)

    {

 let  screen_width_default=1366;

 let  screen_height_default=768;

 this.num_tiles_x = Math.round(screen_width_default*screen_widths / Tile.width);

 this.num_tiles_y = Math.round(screen_height_default*screen_heights / Tile.height);

 this.width=this.num_tiles_x*Tile.width;

 this.height=this.num_tiles_y*Tile.height;

 for(let  x= 0;x<this.num_tiles_x; x++)

        {

 for(let  y= 0;y<this.num_tiles_y; y++)

            {

 let  type = Math.floor(Math.random()*(Tile.LAST_TYPE+1));//need +1 or doesn't include the highest number/

 tiles.push(new  Tile(x*Tile.width, y*Tile.height, type, this.tile_images[type].image));

            }

        }

    }

}//end of class Level

We left the constructor parameters the same, but we added variables to keep track of the number of tiles in the x and y direction + the overall height and width of the level, which is just the number of tiles in each direction, times how wide or tall each tile is (to get the total width/ height).

Next, we create a “CreateLevel” function that will get passed in how many screen widths and heights we want our level to be. We moved our level generation code into here from the bottom of the script, and instead of multiplying it by 2 screen widths/ heights, we’re going to be able to pass it in, and generate different sized levels very easily.

So on the bottom of the script, in “CreateTileMap()”, remove the level generation code, so it now looks like this:

let  tiles = new  Array();

let  level =undefined;

function  CreateTileMap()

{

 let  tile_images = new  Array(asset_loader.GetImage("dirt"),

 asset_loader.GetImage("stone"),

 asset_loader.GetImage("water"),

 asset_loader.GetImage("grass"),

 asset_loader.GetImage("bush"),

                        );

 level = new  Level(tile_images);

 level.CreateLevel(1.25, 1.25);

}

We create the “level” variable outside of this function, so that other places can reference it, otherwise it would only exist in the function we created (but now will exist everywhere, since not being created in a particular function/ class).

We still create/initialize the level after the tiles have loaded, but call the function to actually create the tiles, and pass in 1.25, or 1 screen width/ height plus a quarter more, so the world will be slightly larger than our screen.

If you run this now, you’ll see everything as before, but the level is smaller, so we can more easily test when moving our player will show the background screen.

So, let’s finally constrict the camera, since now we have the width and height of the world stored in the level.

In our “Camera” update function, change it to:

Update(delta_ms)

{

 if(this.target!=undefined)

    {

 this.x=this.target.x-this.half_width_minus_target_half_width;

 this.y=this.target.y-this.half_height_minus_target_half_height;

 let  right_side_of_screen = this.x+window.innerWidth;

 let  bottom_side_of_screen = this.y+window.innerHeight;

 if(this.x<0)

 this.x=0;

 else  if(right_side_of_screen > level.width)

 this.x=level.width-window.innerWidth;

 if(this.y<0)

 this.y=0;

 else  if(bottom_side_of_screen > level.height)

 this.y=level.height-window.innerHeight;

    }

}

We’re first storing the right and bottom of the screen (since left and top are just the x and y). To find them, we just add the width of the screen to the current x position, or the height of the screen to the current y position.

Then, we’re checking the left side to make sure it’s not below 0/ the left side of the level again, but if it is not, then we’re going to check to see if the right side is greater than the right side of the level. If it is, we’ll set the x of the camera back to the right edge of the screen, but also subtract out the width of our camera/window, so that our right side of the camera will be aligned with the right edge of the level.

We then do the same thing for the bottom of the screen, making sure the bottom of our camera/ window will never go below the bottom of our level.

And that’s it! If you play the game now, you’ll see that no matter where you move, you can’t see the background/ outside of our level.

![](Images/image00487.jpeg)

Now we have a player that can be controlled, move around our world, and can’t move outside of our world. We can easily modify the size of the level by passing in how many screen widths and heights we want to use, and can make a super large level if we want. But right now, it’s kind of boring- everything is generated completely randomly, but we want to be able to have a place for a house, an NPC, an enemy, and an area to farm. So, let’s modify how we create the world, so that we’ll actually be able to create a static level, but still allow some randomness for each new game.

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/10_Camera.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/10_Camera.html)

# 11. Creating more involved graphics

We’re up to the point where we’ll need to be able to start breaking down rocks, cutting grass, chopping down trees, and attacking enemies in the future. So, we’re going to create graphics that will allow us to display:

● We’ll create our own unique character, which will allow us to add more animation types

○ One copy with short hair, one with long hair

○ Same size as our tiles (64px x 64px)

● Attacking/ harvesting animations

○ Attacking will use the same animations as harvesting

○ Tools that will need to be added include:

■ Hammer to break rock

■ Axe to break wood

■ Scythe to chop grass

■ Hoe to till dirt

■ Sword to attack enemies

○ A watering animation for watering plants

○ An eating animation for the player to regain health from plants

● Enemy graphic based off our player

● NPC graphic based off our player

Creating artwork, even pixel art work is a lot of work and time. I created a sprite sheet of a character for use with this book. I wanted him to look like characters from other 2d RPG like games that are popular- Pokémon and Harvest Moon.

The way I made the character was to create an ArtClash or Photoshop (or other art program) new project that was the size of our tiles (64x64), drew out roughly the head shape, body shape, etc. I pulled up sprite sheets by searching on google images for “pokemon sprite sheet” and “harvest moon sprite sheet”, and found a few good references to go off of.

## Idle animation

I made the first drawing of the character that is at idle/ default position, modified that one to make one more idle frame (by moving his head and shoulders up one pixel- it’s hard to see in here, but easier when animated in the game).

![](Images/image00488.jpeg)![](Images/image00489.jpeg)

## Walking animation

I then created 2 walking frames, by using the sprite sheets as reference, as well as looking up more references for “walk cycle” on google images. I mainly changed his arm positions around so they look like they swing back and forth between the 2 frames, and moved his legs up and down, to make it look like they are going forward and backwards.

![](Images/image00490.jpeg)![](Images/image00491.jpeg)

Usually if you want your animations to look better, you’ll want to spend time looking up what the basic “key poses” are for each type of animation cycle, starting with those, then deciding if you want to draw more frames in between the most important key poses, to have an even more fluid animation.

I wanted him to also be able to swing a tool/ weapon, so I created a new layer, and created a basic looking scythe that he holds in his hands when idle. I knew that I wanted to layer the tool animation on top of the player animation, so I erased anywhere on the tool graphic where the player should show through (like showing his hands “over” the tool, by removing the pixels for the tool there, to look like the player's hands are on top).

I then copied it, and moved it up slightly for the second idle animation (the gaps below are where the player's hands show through the tool to give it the illusion that the player's hands are over the tool, even though the tool will be drawn over the player).

![](Images/image00492.jpeg)![](Images/image00493.jpeg)

## Harvesting/ attacking animation

I also want the player to be able to harvest things, so I again copied the idle frame, and started changing it around to make it look like the player was harvesting.

The most important frames are when the player draws the tool back, and when he has “chopped” forward (think of chopping with an axe, or swiping with a pole).

So, I first put a new layer on top of that image, and drew the position I wanted the tool to be changed to when the character draws it back. I then went back to the characters layer, and started to move the hands + arms to be able to hold the tool, erasing parts of the tool that made sense to show the character holding onto it.

I also tried to change his legs up on one side, down on the other, as if he was taking a step back when he was pulling the tool back. I also moved his eyes, and updated his face to look like he was turning his head slightly, along with the rest of his body.

I then repeated it for the frame of when he brings the tool forward. I copied the idle character, I created a new layer over it for where the tool would be, drew in the tool, then updated the idle frame to now have the character leaning forward with the tool, to look like he finished swiping.

![](Images/image00494.jpeg)![](Images/image00495.jpeg)![](Images/image00496.jpeg)![](Images/image00497.jpeg)

At this point I realized I would also need to make images/ frames for the walking animation, similar to the attack animation, so I repeated the above. I created a new layer above the first walking frame, drew in the tool, made sure it looked like it fit his hands, then repeated for the second walking animation.

## Making the other angles

I then copied the idle frame, and started drawing in the face, and changing around the pants, to make it look like it was from a back view. I copied the other frames (both idles, walking, and harvesting), flipped them horizontally (since he’s now walking/ harvesting away from the camera), and started drawing in his body + face to look like it was the back of the character for all frames.

I then had to do the same, but make a side view (supposed to be a side/ top view, but I need to practice perspective more to get it looking better in the future). I moved one eye over to one side, filled in the rest of the face, rotated the hair, and drew in places to look like it was more front facing. I had to draw in the body differently, and move the feet around to look like they were side by side, and kept every body part on a different layer, to allow me to rotate them for each animation, and fill in the parts that looked wrong manually.

Finally I had a front, back, and side view finished. We can flip the side view to work for the left or right side, just like we did for previous sprites.

## Saving out the images

I then went through each image, and saved them each out with transparency, so I had a total of 18 images/frames animations (2 frames x 3 directions x 3 animations =18).

We could just load the images up in our game now how they are, 1 by 1, but since we already know about sprite sheets, and we know they are faster to render (though we’re talking 100s of images on screen at a time to notice a difference, depending on the device), we’ll change our frames into a sprite sheet.

## Creating a sprite sheet

There are a lot of different tools out there to turn your images into a sprite sheet, but one I decided to use is “texture packer pro”. It’s free for the basic version, which is all we need. Download, install, and run it, and just use the free version. Drag your images into the program, and it will generate a sprite sheet preview for you, but we have to change some options.

Under settings-> layout on the right hand side, change “size constraints” to POT (power of 2), which will force our sprite sheet to be a power of 2, which is faster for a video card to render to the screen. Next, towards the bottom, uncheck “allow rotation”.

Lastly, there is a button at the bottom middle to disable pro features, which you want to do, or it will put a ugly red color over the transparent parts of your images (and will warn you when you save out). Go to “file->publish sprite sheet” (or ctrl+p), and it will ask you where you want to save your sprite sheet. Save it into your project under “assets->images->”my_player.png”.

I then decided to modify the colors to make 2 other entity types- an enemy and an NPC. I used a function in photoshop: “Image->Adjustments->replace color”, and fooled around with replacing the hair, skin, shirt and overalls color, to have 3 distinct color palettes.

![](Images/image00498.jpeg) ![](Images/image00499.jpeg) ![](Images/image00500.jpeg)

## Using your sprite sheet in the game

Now we actually need to load our sprite sheet into our game, and use it for different animations.

We can just update what we already have, and load our sprite sheet in instead of the previous one we were using.

So, change the “AllAssetsLoaded” function to:

function  AllAssetsLoaded()

{

 CreateTileMap();

 my_player = new  Player(0,0,Tile.width, Tile.height);

 let  my_player_img= asset_loader.GetImage("my_player").image;

 let  scale_my_player = my_player.height / 64;

 let  my_player_idle_D = new  FlipBookAnimation(my_player_img, 64, 64, 3,1, 2, scale_my_player, 400);

 let  my_player_walk_D = new  FlipBookAnimation(my_player_img, 64, 64, 1,2, 2, scale_my_player, 150);

 let  my_player_harvest_D = new  FlipBookAnimation(my_player_img, 64, 64, 1,1, 2, scale_my_player, 400);

 let  my_player_idle_U = new  FlipBookAnimation(my_player_img, 64, 64, 3,4, 2, scale_my_player, 400);

 let  my_player_walk_U = new  FlipBookAnimation(my_player_img, 64, 64, 1,5, 2, scale_my_player, 150);

 let  my_player_harvest_U = new  FlipBookAnimation(my_player_img, 64, 64, 1,4, 2, scale_my_player, 400);

 let  my_player_idle_R = new  FlipBookAnimation(my_player_img, 64, 64, 1,3, 2, scale_my_player, 400);

 let  my_player_walk_R = new  FlipBookAnimation(my_player_img, 64, 64, 3,3, 2, scale_my_player, 150);

 let  my_player_harvest_R = new  FlipBookAnimation(my_player_img, 64, 64, 3,2, 2, scale_my_player, 400);

 my_player.AddAnimation(my_player_idle_D, Entity.STATE.IDLE, Entity.DIRECTION.DOWN);

 my_player.AddAnimation(my_player_walk_D, Entity.STATE.WALKING, Entity.DIRECTION.DOWN);

 my_player.AddAnimation(my_player_harvest_D, Entity.STATE.ATTACKING, Entity.DIRECTION.DOWN);

 my_player.AddAnimation(my_player_idle_U, Entity.STATE.IDLE, Entity.DIRECTION.UP);

 my_player.AddAnimation(my_player_walk_U, Entity.STATE.WALKING, Entity.DIRECTION.UP);

 my_player.AddAnimation(my_player_harvest_U, Entity.STATE.ATTACKING, Entity.DIRECTION.UP);

 my_player.AddAnimation(my_player_idle_R, Entity.STATE.IDLE, Entity.DIRECTION.RIGHT);

 my_player.AddAnimation(my_player_walk_R, Entity.STATE.WALKING, Entity.DIRECTION.RIGHT);

 my_player.AddAnimation(my_player_harvest_R, Entity.STATE.ATTACKING, Entity.DIRECTION.RIGHT);

 my_player.AddAnimation(my_player_idle_R, Entity.STATE.IDLE, Entity.DIRECTION.LEFT);

 my_player.AddAnimation(my_player_walk_R, Entity.STATE.WALKING, Entity.DIRECTION.LEFT);

 my_player.AddAnimation(my_player_harvest_R, Entity.STATE.ATTACKING, Entity.DIRECTION.LEFT);

 sprites.push(my_player);

 SetupInput();

 camera.Follow(my_player);

}

The main things to note are that the 2nd set of 2 numbers are the column (x) and row (y) that the animation we’re looking for starts in (starting with x=1, y=1 being the top left). So, I looked through the sprite sheet, and set the right starting frame for each animation to be added.

The easier way to do this, as you get more and more frames/ sprite sheets, is to use a “sprite atlas”. It’s basically the same thing as a sprite sheet, but also includes a text file (in json or XML format), that tells you which animation is at what spot in the image, so you don’t have to do it manually (especially since the frame positions change in the sprite sheet every time you add another frame!).

If you load it up now, you’ll see our character in the game, complete with idle and walking animation!

![](Images/image00501.jpeg)

We can’t see the harvest animation yet, so let’s make it so when we press “spacebar”, we can see it for now (later when we click on something we can harvest, we’ll then play the harvest animation).

## Seeing the harvest animation using spacebar

We want to use the spacebar to play the harvest animation, so the first thing we need to do is tell when the spacebar has been pressed. We already have a function for setting up input: “SetupInput”, so change it as follows:

function  SetupInput()

{

 my_canvas.addEventListener("mouseup", MouseUp);

 my_canvas.addEventListener("touchend", TouchUp);

 document.addEventListener("keyup", KeyUp);

}

We’re just going to add another event listener, but this time a “keyup” event (when any key on the keyboard has been pressed, and released), and going to run a function we’ll create “KeyUp” when a keyup is fired.

So add the function above “SetupInput()”:

function  KeyUp(event)

{

 console.log(event.code);

}

If you run this now, and press your spacebar, you’ll see in the console “Space”, when you press it. What is happening is that we get passed in the event for any listener, in this case the event is a “KeyboardEvent”, and one of the properties/ variables on the event object is “code”, which gives us the name of the key that was involved in the event, in a human readable fashion. If you press any other keys, you’ll also see their names printed out in the same way.

But now we’ll actually want to change the state of “my_player” when the spacebar has been pressed.

function  KeyUp(event)

{

 console.log(event.code);

 if(event.code=="Space")

 my_player.ChangeState(Entity.STATE.ATTACKING);

}

Now if you run this, you’ll see the player switch to the attacking/ harvesting state when space has been pressed, and switch back to moving, or idle when you move him.

So now we can move around the world, and use the harvesting tool.

### Chapter example on github:

[https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/11_Making_Graphics.html](https://doomtoo.github.io/Learn-to-code-games-using-JavaScript-Examples/11_Making_Graphics.html)

# 12. Conclusion

So now we have a game world we can move around, attack, and later modify more. At this point you could add modified versions of the player to use as NPC's or enemies. You could also create a predefined world, so it isn't built randomly, or use a tool like "Tiled" ([http://mapeditor.org](http://mapeditor.org)) to visually create tile maps to use in the game.

If you'd like to see more message me on twitter: [http://twitter.com/doomtoo](http://twitter.com/doomtoo).

I had planned to walk through creating a full "Harvest Moon" like game, but wanted to put the book out to find if there is any interest in the area, before investing more time (and potentially never having anyone read the book).

If there is considerable interest, I'll fully finish the game + update the github repository with all updates, and update on twitter.

I also plan to make more tutorials using WebGL instead of canvas for better performance, as well as pixi.js and phaser.js to create games quicker/ with less low level code. I would also like to show how to use socket.io as well as websockets to make your own basic real time multiplayer game. If you're interested in any of these, let me know, and I'll create mini tutorials on my blog ([http:/chrismweb.com](http://www.chrismweb.com)), before compiling them together into another book. I also plan to adapt these into videos on YouTube + SkillShare, if there is any interest.

Thank you so much for taking the time to follow along, and I hope you learned about programming, a little about web development, and the fundamentals of game development!
![](images/cover.png)

Copyright 2020 by John Rhea. This book is licensed under the Creative Commons [Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/) (CC BY-NC 4.0)

Distributed by the [Undead Institute](https://undead.institute/) a division of [StoryLab LLC](https://storylab.us/)

This book made possible by a generous grant from [Grant for the Web](https://www.grantfortheweb.org).

## You Know What Else Kills Zombies?

Honest feedback. Enjoyed the book? Found an error or an omission? Still confused about something? Want to complement the author’s sense of humor (or lack thereof)? Email John directly at [feedback@undead.institute](mailto:feedback@undead.institute)

## Find More Zombified Web Development at

[https://undead.institute](https://undead.institute)

## Four Word

Stop those zombie cowboys!

## Content Warning
(for Silliness)

This book contains a large amount of information, zombies, silliness, and a sense of humor that some would call “terrible”. If you’re looking for straight technical information or a cure to your insomnia, this is not the book for you.

If you’re looking for a book that’s accessible to those without technical training or inclination and/or don’t mind laughing a bit while you’re learning, this book is for you. We at the Undead Institute believe that getting braaains should be fun. Join us and let’s stop those smelly zombies once and for all! (No, seriously. Their breath is terrible.)

## Get a Free Apocalyptic JavaScript-ic Cheat Sheet

[![](images/jsintro.png)](https://undd.link/intro2js)

When you sign up for Webpocalypse Weekly, our email newsletter. This printable cheat sheet covers JavaScript loops, variable, conditionals and functions. Write JavaScript easily with your very own Apocalyptic Javascript-ic Cheat Sheet

[https://undd.link/intro2js](https://undd.link/intro2js)

# An Introduction to Programming in JavaScript:
Stomping Zombies with Variables, Loops, Functions and More

by John Rhea

Published by [*The Undead Institute*](https://undead.institute)

## Hello Human Resistance Cell

JavaScript differs from other front-end web languages, such as HTML and CSS. It’s much more programmatic and uses logic and variables and functions and loops and all kinds of things—but don’t fear for your mind as though a zombie were hot on your trail. We’ll walk you through everything and get you up to speed, even if this is your first taste of JavaScript and/or of a more traditional programming language.

This book assumes a small amount of HTML/web page knowledge. If you have none, you can get what you'd need from our free book *[Punching Zombies: An HTML & CSS Quick Start Guide for Writers, Designers, and Beginners](https://undead.institute/death-to-boring-programming-books/)*

## Buckets and Buckets of Zombie Guts

One of the first things to understand is a concept called variables. Variables are like buckets you store things in. You can put water in a bucket or your lunch or a mannequin head or the rookie cards of the 2037 Los Angeles Zombie-Dodgers Human Resistance Cell. You can put just about anything in a bucket.

There are also lots of different JavaScripty types of things you can put in a bucket, such as:

**Numbers:** These are what you think they are.

**Strings of Letters (Strings):** These are actually more than just letters—they are any text or character that you want to treat as a single thing. Enclose strings in quotation marks (both single and double quotes work in JavaScript) and can include any valid character. Examples of strings are:

“Hello Post-Apocalyptic World”

Or,

“Don’t look at me, Norm. The zombie pulled your lunch out of the fridge and ate it.”

Or,

“I know you labeled it. The zombie didn’t care or couldn’t read.”

Or,

“Only one way to find out. He’s over there eating 7 other lunches.”

Or,

“7?”

Or,

“7”

So you can have number characters in a string too, but they’ll behave as strings and not as numbers—so you can’t add or multiply them without converting them back to numbers. If something is in quotes, it’s a string.

**Boolean:** The value is true or false and can’t be anything else. This makes it great for using it like a switch to turn something on or off.

There are a few more types of variables in JavaScript, but this is enough to get us started.

## Buckets of Type Z

Some buckets can only hold one type of thing. For instance, a bucket with a hole in the bottom wouldn’t hold water or the soda from the last working soda fountain in North America, but it could be great for holding books or large rocks or the personal effects of your zombified roommate. Similarly, variables often only hold one type of thing.

In some programming languages, putting the wrong type of content in the wrong bucket can cause errors, but JavaScript is forgiving. The positive side of that is that JavaScript just handles a lot of stuff without complaining. The negative is that if it messes up or handles something different from what you expect, you can get weird results or programming bugs that are hard to track down.

![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

One common place these types of bugs happen is when you try to add a number (2) and a string that looks like a number (“2”). In JavaScript, 2 + “2” is “22”. Since one of these is a string, it casts/treats the other as a string too and puts them together or concatenates them. (This can be very useful when you need to construct a message for the user.) Thus, be careful that you are adding numbers with numbers and not strings.

## Variable Bucket Contents

These buckets we’ve been talking about are called variables. They’re called variables because they are…ahem…variable. You can put something in them, and, during your program, you can take that out and look at it or take it out and do something with it or take it out and put something else in. You can do that any number of times.

Before we can use these buckets/variables to beat back the zombie hordes, we have to name them. We can name a variable just about anything we want. However, we can only use letters, numbers, and underscores. We can’t use any other characters, and the first character can’t be a number—i.e., 7zombies is invalid, but sevenzombies or _7zombies or zombies_numbering_7 would all work just fine.

Also, variables are case sensitive, so a variable of zombie is different from a variable of Zombie, which is also different from a variable named ZOMBIE, which is different from zOmBiE—so watch which case you use, and use that case throughout your code.

![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

We can use this to our advantage with camel case. Camel case makes multi-word variable names much easier to read and understand. In camel case, you write the first word in all lower case, and then capitalize the first letter of each additional word. Here are some examples:

sevenZombies sevenFormerHumans thatGuyFromAccountingWhoTurnedZombie dawnOfTheDeadFromSales rickTheUndeadHarbingerOfDoom

The last rule for variable names is that you can’t use any of JavaScript’s reserved words—meaning the words that have special meaning to JavaScript and are how the language functions. If HTML had variables, it’d be like naming your bucket <p>. It would be hard for the browser to understand when you meant the p tag and when you meant the variable/bucket, as you’d given both the same name.

Now how do you declare a variable in JavaScript? There are three ways: var, let, and const. (These would be examples of reserved words that cannot be variable/bucket names.)

Before we name variables, you need to learn a few important syntax rules. Similar to CSS, JavaScript lines should end with a semicolon. Also, two forward slashes (//) in JavaScript indicate a comment or, to be more specific, tell the browser to ignore the two slashes and everything after them until the end of the line. CSS style comments also work in JavaScript—that is, the browser will ignore everything from your opening /* to your ending */, no matter how many lines it is.

**Var:** var is the original way to set a variable and the method that is most backward-compatible. If you’re building something for older browsers, use var. Examples:

var zombie; //Just creating the variable/bucket var zombie = 45; /* creating the variable and assigning it the number 45 or creating the bucket and putting the number 45 into it… and then having a multi-line comment */ var apocalypse = “The end of the world”; //putting a string in the bucket var zombieDoomed = true; // putting a Boolean in the bucket

**Let:** The next option is to use let instead of var. Let is a newer choice and exists because var could have unexpected behavior. JavaScript’s loosey-goosey (zombly-wombly?) attitude toward variables—that is, how forgiving it is—can, in certain cases, get you into trouble. Let solves that issue and should be your default way of creating variables for any recent browser work.

let zombie; let zombie = 45; let apocalypse = “The end of the world”; let zombieDoomed = true;

**Const:** The last option is almost a contradiction in terms because the next way to instantiate a variable is to create a constant...Yeah, that seems zomborrific to me too, but hear me out. Sometimes you’ll have a value that should stay constant during a program, like the number of zombies cured by one cc of anti-zombie serum or the ratio of human resistance cells to the number of zombie nests in an area. But that number may change outside the bounds of the program. For example, you might increase the effectiveness of the anti-zombie serum (for instance, by infusing it with HTML, CSS, and/or JavaScript), or you might eradicate a zombie nest, making the ratio inaccurate. Rather than putting that value in sixty times and then looking for every instance of that value and replacing it, you can use the name of a constant throughout the program, and then, if the value of the constant changes, you only have to update it in one place in the code. You cannot change a constant while the program is running. You can only change it by editing the code.

The keyword for a constant is const.

const zCuredPerSerumCC = 7; const cell2NestRatio = 0.8271;![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

You can define more than one variable at a time by using a comma between variable names. I’m using *let* below, but it works with var and const too.let zombie, undead;

You can also set their values while chaining them:

let horde = 700, humanityInTrouble = true;

## Undead Output

There are several ways to output something in JavaScript. Outputting for user view is almost always the end goal, even if the results of a program do something else first. Outputting for user view is also helpful in figuring out what’s wrong in a program and how to fix it.

### Output to an Alert

One of the easiest (but often most annoying) ways to output a variable is to use an alert statement. An alert statement is a JavaScript function that creates a dialog box with a message and an okay button. For instance:

alert(“The zombies are here!”);

would show

![alert box with the text The zombies are here!](images/Image0.png)

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/bGemwXJ](https://codepen.io/undeadinstitute/pen/bGemwXJ)

File Demo: [https://undead.institute/files/zombie-programming/001-zombie-alert.html](https://undead.institute/files/zombie-programming/001-zombie-alert.html)

Outputs to an alert are useful, particularly when you are starting out, as you learn what a variable holds at a particular point in your program. The downside is that you have to click “okay” on each dialogue box opened. If you create an alert in a loop, you may end up with quite a lot of clicking. And if you forget to remove a debugging alert from your code before you publish the site, your users will see them, be annoyed, and decide that maybe being a zombie ain't so bad if humans are this monstrous.

### Output to the Page

You can output content or information to the page using document.write.

document.write(“The zombies are here!”);

This prints out content to the page, which is usually where you want to see it. The downsides are that it’s a little complicated to get the content where you want it (although it’s easy to add at, for example, the bottom of the page), and if you leave any debugging code in the production files, the zombies will win, and your users will see your confusing debugging output.

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/ZEOqBbW](https://codepen.io/undeadinstitute/pen/ZEOqBbW)

File Demo: [https://undead.institute/files/zombie-programming/002-zombie-write.html](https://undead.institute/files/zombie-programming/002-zombie-write.html)

Another option is similar to document.write. You can also select an HTML element on the page and add or change the text, or you can create an element in JavaScript and append it to the page with the information. This is the major way that you’ll show content/the results of your program to your users, but when you use it for debugging, it has the downside of being visible to users. This is a powerful and useful way to show content (debugging or otherwise). We’ll look at it in the next book, *JavaScript Basics: Flinging Event, Element, and Object Bombs at Zombie Heads*.

### Output to the Console

The way that’s often best to output debug content is to the console. (I say often the best because each method has its purpose. I use the console most often but will sometimes throw up an alert or write it to the page for a quick and dirty solution.) The console is part of each browser’s web developer tools and allows you to output content to a hidden command line. All you have to do is use:

console.log(“The zombies are here!”);

The output will then appear in the console, and you can figure out where your program went wrong. While I would still recommend removing console.log statements from production code, if you forget, no one but us developer types are likely to see the output.

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/LYZgber](https://codepen.io/undeadinstitute/pen/LYZgber)

File Demo: [https://undead.institute/files/zombie-programming/003-console-zombies.html](https://undead.institute/files/zombie-programming/003-console-zombies.html)

## Math after the Apocalypse

Next we’ll tackle something familiar, though it may be unpleasant for some: math. A lot of math can happen in programming and all the usual culprits are there: addition, subtraction, multiplication, and division, as well as one you may not be familiar with, modulus division.

**Addition:** undead = zombies + infected

**Subtraction:** undead = zombies - cured

**Multiplication:** undead = humans * infectionRate

**Division:** undead = zombies / antidote

**Modulus Division:** is just like division except the remainder is the answer—for example, 13 modulus 5 is 3 because 3 is the remainder/what’s left over after 5 is divided into 13.) Modulus uses the % sign.

nextHorde = zombies % hordeSize;

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/eYzPyLm?editors=0010](https://codepen.io/undeadinstitute/pen/eYzPyLm?editors=0010)

File Demo: [https://undead.institute/files/zombie-programming/004-mathematical-zombies.html](https://undead.institute/files/zombie-programming/004-mathematical-zombies.html)

There are some shortcuts for things we do often. For instance, if we wanted to add a number to a variable and save the new answer to that variable we’d do:

undead = undead + 12;

A shortcut for this is to use the += operator that performs the same as above.

undead += 12;

This isn’t just for addition. It works for all the arithmetic operators.

undead = undead - 7
is equivalent to
undead -= 7

undead = undead * 7
is equivalent to
undead *= 7

undead = undead / 7
is equivalent to
undead /= 7

undead = undead % 7
is equivalent to
undead %= 7

There’s one arithmetic operation so common that it has a shortcut even shorter than using +=. To increment a value by 1, add ++ to the variable (you can decrement by 1 using --).

undead += 1 is equivalent to undead++

undead -= 1 is equivalent to undead--

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/QWEZPXP](https://codepen.io/undeadinstitute/pen/QWEZPXP)

File Demo: [https://undead.institute/files/zombie-programming/005-zombie-math-shortcuts.html](https://undead.institute/files/zombie-programming/005-zombie-math-shortcuts.html)

There’s one little quirk with ++ and -- that can occasionally come in handy. You can put the ++ or -- in front of the variable too.

++undead;

--undead;

It still increments or decrements the variable. However, if the ++ or -- comes after the variable, the variable increments or decrements *before* the contents of the variable/bucket is looked at. If the ++ or -- comes before the variable name, the variable/bucket will increment or decrement before it’s looked at (see the examples below). If the statement is on its own line, it doesn’t matter much whether it’s incremented or decremented before or after. The statements are equivalent. But if it’s used within another JavaScript statement, the result may change.

For instance:

let undead = 10; let zombie = 17 + undead++;

would set zombie equal to 28 and undead equal to 11; whereas

let undead = 10; let zombie = 17 + ++undead;

would set zombie equal to 27 and undead equal to 11.

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/WNxYQbw](https://codepen.io/undeadinstitute/pen/WNxYQbw)

File Demo: [https://undead.institute/files/zombie-programming/006-incremetal-apocalypse.html](https://undead.institute/files/zombie-programming/006-incremetal-apocalypse.html)

## Logically Challenged Zombies

Since variables can hold almost any value, it can be difficult to keep track of what a variable/bucket is supposed to hold. The problem is exacerbated by growing complexity. But you can figure out what’s in a variable by using if-then statements. These allow you to test a condition (if) and do something based on the results (then).

Here’s how an if-then statement looks when the if tests whether undead and zombie are equivalent (we’ll talk about the different tests you can do in a second):

if( undead == zombie ) { //stop horde }

If undead and zombie are equivalent, then whatever code you put in the curly brackets will run. (It's like CSS in that whenever an element matches your selector, the browser will apply the rules in the curly brackets.) If undead and zombie aren’t equivalent, then the browser will skip any code in the curly brackets.

Here are the logical operators we have to work with:

### Equal:

undead == zombie and undead === zombie test for equality.

Three equals signs is stricter than two, and it’s usually what you’ll want to use.

![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

How can things be more or less equal (outside of *Animal Farm*)? This is because of one way that a computer saves memory. Our bucket metaphor will break down a bit here, but let’s say we had a bucket full of something complex, such as a loaf of bread. There’s a lot of information there. It’s complex, and it takes up space.

The human resistance commander needs to see what rations are available, but he’s in the field with the resistance fighters. We could create a copy or 3-D model of the bread (super easy in this computer-i-fied example), but that would take up as much space as the original, and we might run out of buckets. We’d also have to transport the bread or model out to him, which can get complicated when you have quite a few buckets to transport.

So we take a picture of the bread instead. In very general terms, the loaf and the picture are equivalent because one is the loaf and one points to or is a picture of that same loaf. (In computer science, the picture from our analogy is called a pointer because it “points” to the original.) That’s the double equals == level of equality. The triple equals === is when you’re trying to see if two loaves of bread are the same or, rather, if one of them isn’t a pointer to/picture of the other.

In code, a simplified version of that might look like

7 == “7” //true 7 === “7” //false

### Less than:

undead < zombie

Let’s say undead is equal to 10\. Is the value of undead less than the value of zombie? For this to return true, zombie would have to be more than 10 (e.g., 11, 12, 10.1, 312 etc.). It will return false if zombie is 10 or less (e.g., 9, 10, 7, -437, etc.).

### Greater than:

undead > zombie

Is the value of undead greater than the value of zombie? If undead = 10, then true values include 9, 8, -10, 0, and so on. False values include 10, 11, 412, and so on.

### Less than or equal to:

undead <= zombie

Is the value of undead less than or equal to the value of zombie? If undead = 10, true values include 10, 11, 1017, and so on. False values include 9.9, -78, 6, and so on. (You can also do <== to enforce the stricter form of equality.)

### Greater than or equal to:

undead >= zombie

Is the value of undead greater than or equal to the value of zombie? If undead = 10, true values include 10, 9, -7, and so on. False values include 11, 10.1, 371, and so on. (You can also do >== to enforce the stricter form of equality.)

### Not equal:

undead != zombie

The values of undead and zombie are two different things. If undead = 10, true values include 9, 17, 38, -239, and so on, while the false value is 10\. Nothing else is a false value. (You can also use !== to enforce the stricter form of inequality.)

There’s one additional thing you can do based on the if, but it’s not required. It’s called an else statement, and it allows you to do one thing if the conditional is true (then) and another thing if it’s false (else). It looks like this:

if( undead === zombie ) {

//stop horde

} else {

//stop contagion

}

Thus, if undead and zombie are equal, then the browser will “stop horde.” If they aren’t (else), it will “stop contagion.”

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/MWezKez](https://codepen.io/undeadinstitute/pen/MWezKez)

File Demo: [https://undead.institute/files/zombie-programming/007-logically-its-the-apocalypse.html](https://undead.institute/files/zombie-programming/007-logically-its-the-apocalypse.html)

If you need to test multiple conditions, you can do an else if, allowing you to further segment how the program reacts. For instance, if two values are equal, you may want to “stop horde.” But if they aren’t equal, you may want to “stop a greater horde” if one is greater and “stop a lesser horde” if one is lesser.

if( undead === zombie ) {

//stop horde

} else if (undead > zombie) {

//stop a greater horde

} else {

//stop a lesser horde

}

You can do as many of these if-else-if chains as you want. You can also refine the something you want to do by whatever variables make sense for your program.

You can combine conditionals using AND (&&) and OR (||).

**AND** means both statements have to be true to execute the then portion. AND is represented by two ampersands:

if( undead === zombie && zombie > human ) {

//stop horde

} else {

//stop contagion

}

Undead and zombie must be equal AND zombie must be greater than human for the browser to “stop horde.” If neither of them is true, or if only one or the other is true, a “stop contagion” will be done.

**OR** means that if either statement is true or if both are true, then “stop horde” will be done.

if( undead === zombie || zombie > human ) {

//stop horde

} else {

//stop contagion

}

If undead and zombie are equal or if zombie is greater than human or both, “stop horde” will be done. The only way “stop contagion” will happen is if undead and zombie are not equal *and* human is greater than zombie.

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/OJXaMmO](https://codepen.io/undeadinstitute/pen/OJXaMmO)

File Demo: [https://undead.institute/files/zombie-programming/008-if-hes-not-human-and-not-a-zombie.html](https://undead.institute/files/zombie-programming/008-if-hes-not-human-and-not-a-zombie.html)

![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

Because we often test for true and false, changing everything to a literal true or false or writing a specific test would be additional work every time we’re testing something. So, as a shortcut, most programming languages (including JavaScript) count several values as false that aren’t technically false. For instance, if an expression or variable evaluates to 0, it’s counted as false. If it’s any other numeric value, it will evaluate as true. In this way, you might see a single value (this is a rather contrived example, but hopefully it will make sense).

let undead = 0; if ( undead ) {

//stop horde

} else {

//stop contagion

}

In that example, undead being equal to 0 would evaluate as false and “stop contagion” would be done.

Other values that evaluate to false include null (meaning an empty variable/one without a value), undefined (a variable that has never been set), an empty string represented by two double or single quotation marks next to each other “” or ‘’, and NaN which stands for not a number. You see it when you try to do numbery things with non-numbers, such as “12” / 2 (remember that anything in quotation marks is treated as a string, not a number) or on the protest signs of a populace being barcoded by an authoritarian human settlement.

**Note:** this test works best on primitive types: numbers, strings, and so on. It may not work on more complicated types like arrays (we’ll discuss these later).

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/ZEOmvjN](https://codepen.io/undeadinstitute/pen/ZEOmvjN)

File Demo: [https://undead.institute/files/zombie-programming/009-zombie-brain-is-null.html](https://undead.institute/files/zombie-programming/009-zombie-brain-is-null.html)

## Getting Loopy with Zombies

The next important thing in JavaScript—and in other programming languages—is the loop. Loops are just what they sound like, they do some code again and again and again until they hit a stopping condition. There are two main types of loops (with a couple variations): the for loop and the while loop.

For loops run whatever code you place between the curly brackets for a set number of iterations.

![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

The letters i, j, and k are traditionally used as loop counters (a variable that counts the number of iterations used. You don’t have to use these as your counter values, but if you don’t, name your counters clearly. For clearer code, it’s best not to use i, j, or k for any other kind of variable.

A traditional for loop in JavaScript looks like this:

for( let i = 0; i < 10; i++ ) {

//stop zombies 10 times

}

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/bGeQaZx](https://codepen.io/undeadinstitute/pen/bGeQaZx)

File Demo: [https://undead.institute/files/zombie-programming/010-zombie-loop-de-loop.html](https://undead.institute/files/zombie-programming/010-zombie-loop-de-loop.html)

![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

You’ll notice that the i counter started at zero instead of one. This is not a requirement, but it can make things easier in the long run. The reason is that computers start counting at 0 rather than at 1\. (Like some zombies, computers don’t have fingers to count on.) So later, when we work on arrays, their indexes start at 0 rather than at 1, and if you start your for loop at 1, you’ll skip the first array element, and the zombies will win. (If that made little sense, no worries. We’ll get there.)

The for loop itself (inside the parentheses) is three statements in one. First (let i = 0;), you instantiate the counter or just set it to an initial value. Next (i < 10), you set the conditional for how long to continue the loop (i.e., while i is less than 10, keep running all the code between the curly brackets). Finally (i++), you’re setting how fast you go from the initial value (i = 0) to the end condition (when i is greater than or equal to 10). In most cases, that’s by an increment of 1 (i++), but it could be a decrement (i--) or you could do it by more than 1 depending on your needs (i += 2, etc.).

Be careful that you don’t set up a condition that will never come about, or the loop will go on forever, and the zombies will win. For instance, if your condition is i < 10, and you decrement instead of increment, then i will always be less than 10, and your loop will never exit. (I’ve done this myself more times than there are zombies in a horde, so if you find your browser hanging or repeating something well beyond the number of times you anticipate, it’s best to just close the browser window, fix your code, and then reopen the page. Hopefully you’ll be free of the infinite loops that’ll eat your brain like a zombie with an empty stomach).

let horde = 0; let humans = 100; for( let i = 0; i < 10; i++) {

horde += 10;

humans -= 10;

} //perform the same task using a decrementing loop let horde = 0; let humans = 100; for( let j = 10; j < 1; j--) {

horde += 10;

humans -= 10;

}

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/JjKepGE](https://codepen.io/undeadinstitute/pen/JjKepGE)

File Demo: [https://undead.institute/files/zombie-programming/011-loopy-little-zombies.html](https://undead.institute/files/zombie-programming/011-loopy-little-zombies.html)

The for loop examples above, assume you have something numeric to compare. What if there isn’t a set number of times to run something or a numeric comparison just isn’t appropriate? That’s where the second kind of loop comes in, the while loop.

The while loop tells the browser to keep looping *while* a condition is true.

let george = “zombie”, stillAZombie = true; while( stillAZombie ) { if( george == “zombie” ) { tryToCure( george ); } else { stillAZombie = false; } }

The example above checks whether the stillAZombie variable is true. If it is, it checks whether the george variable holds a string of “zombie.” If it does, the program tries a cure on george. If the tryToCure function succeeds, then the george variable will no longer hold “zombie,” the if test will fail, and the else section will be executed, setting stillAZombie to false and ending the loop the next time the while loop checks whether stillAZombie is true.

The while loop has a half-brother called the do-while loop. Do-while loops are used when you want to put the conditional at the end of the loop (i.e., you want to run the statements in the loop at least once).

let george = “zombie”, stillAzombie = true; do {

if( george == “zombie” ) {

tryToCure( george );

} else {

stillAZombie = false;

}

} while( stillAZombie );

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/zYBMRoB](https://codepen.io/undeadinstitute/pen/zYBMRoB)

File Demo: [https://undead.institute/files/zombie-programming/012-while-zombie-freak-out.html](https://undead.institute/files/zombie-programming/012-while-zombie-freak-out.html)

The do-while loop above does the same thing as the while loop did, but the if test is ensured to run at least once.

Be careful with this kind of loop though, because if stillAzombie never becomes false, then your loop will continue forever, and the zombies will winter in Florida while taking out loans in your name and ruining that credit score you worked so hard to get. You know…they’ll win.

## Zombie Sniper and Variable Scopes

Before we go further, let’s talk about variable scope—that is, where you can use a variable. When we define a bucket using var or let or const, it’s like we’re writing its name on the side. If you have a horde of buckets with names on their sides, it can take a while to find the one you want, right? So JavaScript allows you to create groups of buckets and localize the bucket names to make things easier to find and make sure there aren’t any conflicts. You can think of a group of buckets as all the buckets (variables) defined between two curly brackets. Any bucket you’ve named within that group won’t be used outside that group, but any variable declared outside that group can also be used within the group. For instance:

let zombie = 0; for( let i = 0; i < 10; i++ ) {

let undead = i;

zombie = i;

}
//print contents of both variables. document.write(zombie); //Output is 10 document.write(undead); //Output is undefined

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/abZQPye](https://codepen.io/undeadinstitute/pen/abZQPye)

File Demo: [https://undead.institute/files/zombie-programming/013-using-scope-on-zombie-breath.html](https://undead.institute/files/zombie-programming/013-using-scope-on-zombie-breath.html)

Since the variable zombie was defined outside the for loop/curly brackets, it can be accessed from within the loop and changed. However, since undead was defined within the loop, it does not exist outside of that and thus will be undefined when printed outside the loop.

## An Array of Apocalyptic Outcomes

There’s one more data type to discuss, though this might be better called a data structure: the array. You can think of an array as an orderly line of buckets, or a line of people with empty bowls waiting for whatever-we-got stew at your nearest human resistance cell. This line is a useful way to group everyone, and you could either go down the line and hand out stew, or you could call out names for them to come get stew, or you could send out a line of stew cooks the same size as the line of hungry people to give them stew. Whatever way you access the people in the line, you can because they’re all in one place and in an order you understand. Arrays are a line of buckets or variables. You can access all the variables in sequence using their indices (places in line), pull out a specific variable in the array (you can have string names as your indices too), or you can use a map function (we’ll get to these in the next book) to do work on all the variables at once.

Arrays use bracket notation to designate which bucket you are on. By default, indices are numbered starting at zero. (Empty brackets designate creating an empty array.)

let horde = []; horde[0] = “Bob”; horde[1] = “Fred”; horde[2] = “Leroy”; //the horde array then looks like [“Bob”, “Fred”, “Leroy”]

You can also create that array this way:

let horde = [“Bob”, “Fred”, “Leroy”];

But you aren’t limited to a line of buckets. You can also create a line of lines and a line of lines of lines and a line of lines of lines of...you get it. Youcan create arrays of multiple dimensions. A two-dimensional array is like a square. If you’ve ever seen a majority military human resistance cell walk into battle or the last vestiges of our air force planes fly in a tight, square formation, you’ll understand what I mean. Or look at this array of buckets:

![](images/Image1.png)

A two-dimensional array is accessed in a similar way as a one-dimensional array but with two indices (one horizontal, and one vertical).

let zombie = horde[6][2];

The code above would save the contents of seven down and three across into the variable zombie. (Don’t forget. A two-dimensional array’s first cell is at [0][0].)

There are also a few array-specific properties we can use to get information about the array. One of the most common is length, which gives us the number of items in the array, allowing us to write a for loop to search the entire array. You call length by adding a period after the array name and the word length.

let horde = [ 1, 0, 0, 1, 1 ]; let results = []; for( let i = 0; i < horde.length; i++) {

results[i] = tryToCure( horde[i] );

}

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/ExyGryj?editors=0010](https://codepen.io/undeadinstitute/pen/ExyGryj?editors=0010)

File Demo: [https://undead.institute/files/zombie-programming/014-a-wide-array-of-zombies.html](https://undead.institute/files/zombie-programming/014-a-wide-array-of-zombies.html)

Using the code above, you go through every bucket in the array. Bucket zero is the first one in the horde array or horde[0]. When you increment i by one, you can look at the second bucket or horde[1], and so on, till you get through the entire array.

## Functional Apocalypse

Sometimes you create a section of code that you want to use again and again—for instance, code that cures the zombie contagion or that finds the highest strength zombie in a horde.

Now in your human resistance cell, you could do every task yourself and overload your schedule. Or you could delegate a task to Fred or Nancy, and then they could do that task every time and be excellent at it (rather than you having to relearn/remember that task every time you had to do it).

It’s similar with code. Rather than writing that same set of code again and again and again, you can put it in a function. A function is a set of tasks/code that you can reuse. Like asking Fred or Nancy to do the task, you ask the function to do the task.

![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

While there is some disagreement on the best way to use functions, whether you do almost everything in small functions or use more monolithic functions, both have their advantages. More functions can make it harder to follow the code and can make things confusing because the code won’t be as linear and will jump around from location to location wherever the function is defined. On the other hand, if something’s wrong, it’s confined to a rather small section of code. Using more monolithic functions can make it easier to find the function the problem is in, but that is often an extensive section of code.

I’d recommend a middle approach. When you start out, have your functions do one thing at a time and anything you do multiple times. They’re easier to debug (figure out where the code went wrong/why it’s not doing what you intend), and, once you have some practice, you’ll get a handle on when you need a function or not, and what makes sense to you.

Before we do some function code, we need to discuss how we hand information to Fred or Nancy and how we get information back from them.

You don’t always need to give a function (or Fred or Nancy) any information to perform their task other than “Go!” But you might have a horde you want them to target or a weapon you want them to reload or a specific zombie you want them to cure, such as a formerly human spouse or child. When you pass information to a function or hand data to Fred or Nancy to process, that information or data is called a parameter, and you can have none, one, two, or however many parameters or inputs into a function.

After the task is complete, you might want Fred or Nancy to hand something back to you or return with some information. That might be a now reloaded weapon or whether the antidote worked on your un-bucket-kicking spouse or child. (Don’t worry, the antidote was infused with JavaScript code, and your spouse/child is now resting, fully restored.) If they hand you a bunch of things, it’ll be hard to know what each thing is unless it’s organized (e.g. like into an array or something). Functions can only return one value, but that value could be an array, allowing you to circumvent the one-value return policy.

A function definition (where you define the function’s name and what it does) begins with the word *function*, and then you enter the case-sensitive name you want to give that function. Next, in parentheses, add any parameters in a comma-separated list. If you don’t have any parameters, just leave the space between the parentheses blank/empty.

function tryToCure( person ) {

let result = Math.random() * 100;

if(result <= 10) {

return person + " is cured!";

} else {

return person + " is still a zombie";

}

}

When you call the function, you could write:

tryToCure( spouse );

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/wvWNvXa](https://codepen.io/undeadinstitute/pen/wvWNvXa)

File Demo: [https://undead.institute/files/zombie-programming/015-functionally-undead.html](https://undead.institute/files/zombie-programming/015-functionally-undead.html)

It will be just as though you handed Nancy your spouse’s whereabouts and asked her to use a tranquilizer dart to bring your spouse in and administer the antidote.

To capture the returned value, you need to save it in a variable. Returning a value is optional.

let human = tryToCure( spouse );

If you had no parameters to send the function, you could write this:

function cureAllZombies() {

//cure all zombies

if( allCured == true ) {

return true;

} else {

return false;

}

}

If it didn’t return a value because Fred cured all the zombies, there would be no return statement in the function and no need to capture a result. It would be called like this:

cureAllZombies();

With two or more parameters, you separate the parameters with commas.

function cureTwoZombies( zombie1, zombie2) {

//cure two zombies

}

Assuming it didn’t need to return anything, it would be called like this:

cureTwoZombies( spouse, child );

Let’s look at an example program. For arbitrary reasons that make this example easier, we magically have an array filled with zombie results from the latest testing done at a hospital. It is held in a one-dimensional array, and the results are set up so that a 1 is a human and a 0 is a zombie ("because zombies are zeroes and humans are heroes," said the totally cool and hip author...). The hospital wants a JavaScript program to sort the array into humans and zombies and get a count of each.

let patientList = [1, 1, 0, 1, 1, 1, 0, 0, 1, 0, 1, 0 ], i = 0; let humans = 0, zombies = 0; while (patientList[i] != null) {

if( patientList[i] === 1 ) {

humans++;

} else {

zombies++;

}

i++

} //Output: humans 7, zombies 5

#### Try it Out:

Codepen Demo: [https://codepen.io/undeadinstitute/pen/KKMJwEB](https://codepen.io/undeadinstitute/pen/KKMJwEB)

File Demo: [https://undead.institute/files/zombie-programming/016-sorting-an-array-of-zombies.html](https://undead.institute/files/zombie-programming/016-sorting-an-array-of-zombies.html)

Now that we have some idea of how the logic and programming works, how do we add this stuff to the HTML page? There are several ways, but the most important is the HTML script tag.

<script type=“text/javascript”>

cureAllZombies();

</script>

You can also use the script tag to load a file full of JavaScript.

<script src=“thecure.js” type=“text/javascript”></script>![](images/livingtip-jsloops.png)

#### Night of the Living Tip:

You want to load your JavaScript code as late as possible in the downloading of the site—that is just before the closing body tag. If you load it earlier, such as in the head tag, it can block the download of other assets. The total time spent downloading will be the same wherever the JavaScript is placed, but if it blocks download or rendering because the browser is waiting on your js file to download or your js code to execute, it can prevent the rest of the page from displaying, giving the user a blank screen for longer. Even if the page isn’t functional until the js loads, the user likes to see that things are working, and the browser rendering what it can will help. A blank page, like a zombie's blank stare, usually means something is broken and users will assume as such. There will be some JavaScript that needs to be executed before the page loads or to determine how the page loads, so there may very well be JavaScript in the head, but if it's pushed to the bottom and the page still works as intended, that would be ideal.

This book covered most of the basic tools you need to get up and running with programming with an eye towards doing so in JavaScript. While the syntax/how you write it will vary, most programming languages have all the concepts discussed here. The next book, *JavaScript Basics: Flinging Event, Element, and Object Bombs at Zombie Heads* will get into specifics of and focus on JavaScript and some unique offerings of that language.

But before we go there, let’s test out those skills.

## Punch Those Zombies in the Array

You will take a two-dimensional array composed of names and a super-secret numbery biologicy thingy (NBT) and process that array using several functions. The starter HTML file/codepen will hold the array and have stubs for the functions.

#### Starter File

Codepen: [https://codepen.io/undeadinstitute/pen/jOrdwrE](https://codepen.io/undeadinstitute/pen/jOrdwrE)

File: [https://undead.institute/files/zombie-programming/017-our-cells-numbery-biologicy-thingy-results.html](https://undead.institute/files/zombie-programming/017-our-cells-numbery-biologicy-thingy-results.html)

Your first function, processPerson, should take the subject’s name and the conveniently provided NBT. (Running it in a loop would probably help you process all the entries.) The NBT, due to arbitrary convenience for this exercise, can tell you both whether a subject will become a zombie and whether a cure will work on them once they become a zombie.

From processPerson, hand the NBT to a function called willBecomeZombie. willBecomeZombie should return true or false. If the NBT modulus 7 is 2 or more, the person, if infected, will become a zombie, so return true. If it’s 0 or 1, return false.

Also from processPerson, you call a function named infectionRateCalculation to calculate the likelihood of infection using that magical NBT. Divide the NBT by 19307 and multiply the result by 0.1257\. That will give you the infection rate of others should the person be infected. Return the infection rate so that you can print it with the other info.

From processPerson, call a function called curable that takes the NBT. The antidote will work on the person if (NBT * 3 + 2) modulus 17 is 0 or 7\. Therefore, those values should return true. Any other value should return false.

Once you have all the information calculated, call a function that outputs it to the screen using document.write. Your output should list the person’s name and label the results of each function. Please also ensure that each person’s info prints on its own line.

#### Example Answer:

Codepen: [https://codepen.io/undeadinstitute/pen/xxOMWbd](https://codepen.io/undeadinstitute/pen/xxOMWbd)

File Demo: [https://undead.institute/files/zombie-programming/017answers-our-cells-numbery-biologicy-thingy-results.html](https://undead.institute/files/zombie-programming/017answers-our-cells-numbery-biologicy-thingy-results.html)

### Got Questions?

Join the [Undead Institute Facebook group](https://www.facebook.com/groups/490540551375786/) and get answers. https://www.facebook.com/groups/undeadinstitutehelpforum

### You Know What Else Kills Zombies?

Honest feedback. Enjoyed the book? Found an error or an omission? Still confused about something? Want to complement the author’s sense of humor (or lack thereof)? Email John directly at [feedback@undead.institute](mailto:feedback@undead.institute)

### Find More Zombified Web Development at

[https://undead.institute](https://undead.institute/)

## About the Author

John is a storyteller with design and development skills. By day he designs and builds websites and mobile apps, by night he spins sci-fi stories at StoryLab ([https://storylab.us](https://storylab.us/)) and counts his words carefully at [https://8wordstories.com](https://8wordstories.com/). He's a pineapple in disguise [https://pineapplecomics.com](https://pineapplecomics.com/) and (as you know) tries to make learning web development fun by helping you kill zombies [https://undead.institute](https://undead.institute/). He's been lucky enough to collect a wife and five kids along with six cats, four dogs, and a small army of fish. If he remembers to wear pants, it’s been a good day.

Ask him questions, compliment his tastes in thirteenth century Greenlandic literature, and argue with him over minutia (like whether Greenland had any independent literature in the thirteenth century) on twitter [@storykaboom](http://twitter.com/storykaboom)

We Hope Getting Braaains was Fun!
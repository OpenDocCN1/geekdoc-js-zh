![](Images/cover05089.jpeg)

What  is  JavaScript?

Last year, millions of learners from our community started with JavaScript. Why?  JavaScript is primarily known as the language of most modern web browsers, and its  early quirks gave it a bit of a bad reputation. However, the language has continued  to evolve and improve. JavaScript is a powerful, flexible, and fast programming  language  now  being  used  for increasingly  complex web  development and  beyond!

Since JavaScript remains at the core of web development, it’s often the first language  learned by self-taught coders eager to learn and build. We’re excited for what you’ll  be able to create with the JavaScript foundation you gain here. JavaScript powers the  dynamic  behavior  on most websites, including this one.

In this lesson, you will learn introductory coding concepts including data types and  built-in objects—essential knowledge for all aspiring developers. Make sure to take  notes and pace yourself. This foundation will set you up for understanding the more  complex  concepts you’ll encounter later.

![](Images/image04554.jpeg)

Console

The console is a panel that displays important messages, like errors, for  developers.  Much  of the  work  the  computer  does  with our  code is  invisible

to us by default. If we want to see things appear on our screen, we can  print,  or log,  to our console directly.

In JavaScript, the  console  keyword refers to an object, a collection of data  and actions, that we can use in our code. Keywords are words that are built  into the JavaScript language, so the computer will recognize them and  treats  them specially.

One  action, or  method, that  is built  into the  console  object  is

the  .log()  method. When we write  console.log()  what we put inside the  parentheses  will get printed, or logged, to the  console.

It’s going to be very useful for us to print values to the console, so we can  see  the work that  we’re doing.

console.log(5);  This example logs  5  to the console. The semicolon denotes the end of the  line, or statement. Although in JavaScript your code will usually run as  intended without a semicolon, we recommend learning the habit of ending  each statement with a semicolon so you never leave one out in the few  instances  when  they are required.

You’ll  see  later on  that we can use  console.log()  to print different  kinds of  data.

Instructions  1.

Use  the  console.log  code in  the editor  to log  your  age to the console.

Run  your  code when  you are ready  to see the  result.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

On  the next line, write another  console.log  to print out a different number  representing  the number  of weeks you’ve been programming.

![](Images/image04555.jpeg)

Comments

Programming is often highly collaborative. In addition, our own code can  quickly become difficult to understand when we return to it— sometimes  only an hour later! For these reasons, it’s often useful to leave notes in our  code  for  other  developers or ourselves.

As we write JavaScript, we can write comments in our code that the  computer will ignore as our program runs. These comments exist just for  human  readers.

Comments can explain what the code is doing, leave instructions for  developers  using the  code,  or  add any other  useful annotations.

There  are  two types  of code  comments  in JavaScript:

1. A single line comment will comment out a single line and is denoted  with two forward  slashes  //  preceding it.

![](Images/image04556.jpeg)

You can also use a single line comment to comment after a line of  code:

console.log(5);  //  Prints  5

2. A multi-line comment will comment out multiple lines and is denoted  with  /*  to begin  the comment, and  */  to end the comment.

![](Images/image04557.jpeg)

You can also use this syntax to comment something out in the middle  of  a line of code:

console.log(/*IGNORED!*/ 5);  // Still just prints 5  Instructions 1.

Let’s  practice  adding  some code  comments.

To the right, we’ve provided you with the beginning of the  book Catch-22  by Joseph Heller.

On  line 1, write a  single line comment  that says  Opening  line.

![](Images/image04558.jpeg)

2.

Single line comments are great for adding context to your code. Multi-line  comments are often best suited to prevent a block of code from running.  However,  both  types of comments  can be used for  either  purpose.

Use  a  multi-line  comment  so that the  bottom 6  console.log()  statements are  all  commented out

![](Images/image04559.jpeg)

![](Images/image04560.jpeg)

Data  Types

Data types are the classifications we give to the different kinds of data that  we use in programming. In JavaScript, there are seven fundamental data  types:

*   Number: Any number, including numbers with  decimals:  4,  8,  1516,  23.42.
*   String: Any grouping of characters on your keyboard (letters,  numbers, spaces, symbols, etc.) surrounded by single quotes:  ' ...  '  or double quotes  " ... ". Though we prefer single quotes. Some  people  like to think of  string as a fancy word  for text.
*   Boolean:  This data  type only  has two possible  values—

either true  or  false  (without  quotes).  It’s helpful to think  of booleans  as  on  and  off  switches  or  as  the  answers  to  a  “yes”  or  “no” question.

*   Null: This data type represents the intentional absence of a value, and  is  represented by the  keyword  null  (without quotes).
*   Undefined:  This data  type is denoted  by the

keyword  undefined  (without quotes).  It also  represents  the  absence of a  value  though it has a different use than  null.

*   Symbol: A newer feature to the language, symbols are unique  identifiers, useful in more complex coding. No need to worry about  these for  now.
*   Object:  Collections  of  related  data.

The first 6 of those types are considered primitive data types. They are the  most basic data types in the language. Objects are more complex, and you’ll  learn much more about them as you progress through JavaScript. At first,  seven types may not seem like that many, but soon you’ll observe the world  opens with possibilities once you start leveraging each one. As you learn  more  about objects,  you’ll be able  to create  complex collections of  data.

But  before  we do  that,  let’s get  comfortable  with  strings  and  numbers!

![](Images/image04561.jpeg)

In  the  example above,  we  first  printed  a  string.  Our  string  isn’t  just  a  single

word; it includes both capital and lowercase letters, spaces, and  punctuation.

Next,  we printed  the number 40,  notice we did not use  quotes.

![](Images/image04562.jpeg)

![](Images/image04563.jpeg)1.

![](Images/image04564.jpeg)On  line 1,  log the string

Checkpoint 2  Passed

Stuck?  Get a hint

2.

![](Images/image04564.jpeg)On  line 2, log the  number

Checkpoint 3  Passed

Stuck?  Get a hint

![](Images/image04565.jpeg)3.

![](Images/image04564.jpeg)On  line 3, print

Checkpoint 4  Passed

Stuck?  Get a hint

4.

to  the console.

![](Images/image04566.jpeg)to  the console.

to  the console.

On  line 4,  print the number  20.49  to the  console.

![](Images/image04567.jpeg)

Arithmetic  Operators

Basic  arithmetic  often comes  in handy  when  programming.

An operator is a character that performs a task in our code. JavaScript has  several built-in in arithmetic operators, that allow us to perform  mathematical calculations on numbers. These include the following  operators  and  their corresponding symbols:

1. Add:  +

2. Subtract:  -

3. Multiply:  *

4. ![](Images/image04568.jpeg)![](Images/image04568.jpeg)Divide:  /

5. Remainder:  %

The  first four  work  how you might  guess:

![](Images/image04569.jpeg)console.log(3  +  4);  //  Prints 7

console.log(5  -  1);  //  Prints 4

console.log(4  *  2);  //  Prints 8

console.log(9  /  3);  //  Prints 3

Note that when we  console.log()  the computer will evaluate the expression  inside the parentheses and print that result to the console. If we wanted to  print the characters  3 + 4, we would wrap them in quotes and print them as  a string.

![](Images/image04570.jpeg)

The remainder operator, sometimes called modulo, returns the number that  remains after the right-hand number divides into the left-hand number as  many times as it evenly can:  11 % 3  equals 2 because 3 fits into 11 three  times,  leaving 2 as the remainder.

Instructions  1.

Inside  of a  console.log(), add  3.5  to your age.

This  is the  age you’ll be  when we start sending people  to  live on  Mars.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

On a new line write another  console.log(). Inside the parentheses, take the  current  year and  subtract  1969.

The  answer is  how many years  it’s been since  the 1969  moon landing.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Create  another  console.log(). Inside  the  parentheses divide  65  by  240.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Create one last  console.log().  Inside the  parentheses, multiply  0.2708  by  100.

That’s the percent of the sun that is made up of helium. Assuming we could  stand  on  the sun, we’d  all sound  like chipmunks!

![](Images/image04571.jpeg)

String  Concatenation

![](Images/image04568.jpeg)Operators  aren’t  just for numbers! When a  +  operator  is used on two  strings,  it appends the right  string to the  left  string:

![](Images/image04572.jpeg)

This  process of  appending one string  to another  is  called concatenation.

Notice in the third example we had to make sure to include a space at the  end of the first string. The computer will join the strings exactly, so we  needed to make sure to include the space we wanted between the two  strings.

![](Images/image04573.jpeg)

Just like with regular math, we can combine, or chain, our operations to get  a  final result:

![](Images/image04574.jpeg)

1.

![](Images/image04575.jpeg)Inside a  strings

statement, concatenate the two  and  'World'.

Note: You should concatenate the two strings exactly (without introducing  any  additional characters).

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

We  left  off the space last  time.  Create a  second  console.log()  statement  in  which you concatenate the strings  'Hello'  and  'World', but this time make  sure  to  also include a  space ('  ')  between the two words.

![](Images/image04576.jpeg)

Properties

When you introduce a new piece of data into a JavaScript program, the  browser saves it as an instance of the data type. Every string instance has a  property called  length  that  stores the number of characters in that  string.

You can retrieve property information by appending the string with a  period  and the property name:

console.log('Hello'.length);  //  Prints  5

The  .  is another operator! We call it the dot operator.

In the example above, the value saved to the  length  property is retrieved  from  the instance of the string,  'Hello'. The  program prints  5  to  the  console,  because  Hello  has five characters in it.

Instructions  1.

Use  the  .length  property to log the  number of characters in  the following  string to  the console:

'Teaching  the  world  how  to code'

console.log('Teaching  the  world  how  to  code'.length);

Methods

Remember that methods are actions we can perform. JavaScript provides a  number  of string methods.

We  call,  or use,  these methods by  appending an instance  with:

*   a  period  (the dot  operator)
*   the  name of the method
*   opening  and  closing parentheses

E.g.  'example  string'.methodName().

Does that syntax look a little familiar? When we use  console.log()  we’re  calling the  .log()  method on  the  console  object.  Let’s  see  console.log()  and  some  real string methods in action!

![](Images/image04577.jpeg)

Let’s  look at  each  of the lines above:

*   On the first line, the  .toUpperCase()  method is called on the string  instance  'hello'. The result is logged to the console. This method  returns  a string in all capital letters:  'HELLO'.
*   On the second line, the  .startsWith()  method is called on the string  instance  'Hey'.  This method also accepts the character  'H'  as an input,  or argument, between the parentheses. Since the string  'Hey'  does  start  with the letter  'H',  the  method returns the boolean  true.

You can find a list of built-in string methods in the [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype)  [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype). Developers use documentation as a reference tool. It  describes  JavaScript’s keywords, methods,  and syntax.

Instructions  1.

Use  the  .toUpperCase()  method  to  log the  string  'Codecademy'  to  the  console  in  all  capital letters.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

In the second  console.log()  statement in app.js, we have a string  ' Remove  whitespace '  which has spaces  before  and after  the  words  'Remove whitespace'.

If we browse the [JavaScript string documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype), we find several built-in  string methods that each accomplish a different goal. The one method that  seems  ideal for  us is  .trim().

Use the method to remove the whitespace at the beginning and end of the  string in the second  console.log()  statement.

![](Images/image04578.jpeg)

Variables

In programming, a variable is a container for a value. You can think of variables as  little containers for information that live in a computer’s memory. Information stored  in variables, such as a username, account number, or even personalized greeting can  then  be found in memory.

Variables also provide a way of labeling data with a descriptive name, so our  programs  can be  understood more clearly  by the reader  and ourselves.

In short, variables label and store data in memory. There are only a few things you  can  do with variables:

1. Create  a variable  with a  descriptive name.

2. Store  or  update information  stored  in  a  variable.

3. Reference  or “get”  information stored  in  a variable.

It is important to distinguish that variables are not values; they contain values and  represent them with a name. Observe the diagram with the colored boxes. Each box  represents variables; the values are represented by the content, and the name is  represented  with  the label.

In  this lesson,  we will cover how to use the  var,  let, and  const  keywords to create  variables.

![](Images/image04579.jpeg)

Create  a  Variable:  var

There were a lot of changes introduced in the ES6 version of JavaScript in  2015.  One  of the  biggest  changes was two new keywords,  let  and  const, to

create, or declare, variables. Prior to the ES6, programmers could only use  the  var  keyword to declare variables.

![](Images/image04580.jpeg)

Let’s  consider  the example above:

1. var, short for variable, is a JavaScript keyword that creates, or declares,  a new  variable.

2. myName  is the variable’s name. Capitalizing in this way is a standard  convention in JavaScript called camel casing. In camel casing you  group words into one, the first word is lowercase, then every word  that follows will have its first letter uppercased. (e.g.  camelCaseEverything).

3.  =  is the assignment operator. It assigns the value ('Arya') to the  variable  (myName).

4. 'Arya'  is the value  assigned (=)  to the variable  myName. You can also say  that the  myName  variable is initialized  with a value of  'Arya'.

5. After  the variable is declared, the string value  'Arya'  is printed to  the  console  by referencing  the variable  name:  console.log(myName).

There  are a  few general  rules for  naming variables:

*   Variable  names  cannot  start with  numbers.
*   Variable names are case sensitive, so  myName  and  myname  would be  different variables. It is bad practice to create two variables that have  the  same name using different cases.
*   Variable names cannot be the same as keywords. For a  comprehensive list of keywords check out  [MDN’s keyword](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords)  [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords).

Note: In the next exercises, we will learn why ES6’s  let  and  const  are the  preferred variable keywords by many programmers. Because there is still a  ton  of  code written prior  to ES6, it’s helpful to be  familiar with  the

pre-ES6  var  keyword.

If  you  want  to  learn  more about  var  and the quirks associated with it, check  out  the [MDN var documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var).

![](Images/image04581.jpeg)

1.

Declare a  variable named  favoriteFood  using the  var  keyword and  assign to it  the  string  'pizza'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Declare a  variable named  numOfSlices  using the  var  keyword and assign to it  the  number  8.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Under the  numOfSlices  variable, use  console.log()  to print the  value saved  to  favoriteFood.

On  the  following  line, use  console.log()  to  print the  value saved  to  numOfSlices.

![](Images/image04582.jpeg)

Create  a  Variable:  let

As mentioned in the previous exercise, the  let  keyword was introduced in  ES6.  The let  keyword signals that the variable can be  reassigned a  different  value.  Take a look at the example:

![](Images/image04583.jpeg)

Another concept that  we  should  be aware  of when  using  let  (and even  var)  is that we can declare a variable without assigning the variable a value. In  such  a case,  the  variable  will be  automatically initialized with  a value

of  undefined:

![](Images/image04584.jpeg)

Notice  in the  example above:

*   If we don’t assign a value to a variable declared using  the  let  keyword,  it automatically has a value of  undefined.
*   We  can  reassign the  value  of  the variable.

Instructions  1.

Create  a  let  variable called  changeMe  and  set it  equal to the boolean  true.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

On  the line after  changeMe  is declared,  set the value of  changeMe  to be the  boolean  false.

To  check  if changeMe  was reassigned,  log the  value  saved to  changeMe  to  the  console.

![](Images/image04585.jpeg)

Create  a  Variable:  const

The  const  keyword was also introduced in ES6,  and is short for  the word  constant. Just like  with  var  and  let  you can store  any value in

a  const  variable. The way you declare a  const  variable  and  assign a  value to it  follows the same structure as  let  and  var. Take a look at the following  example:

![](Images/image04586.jpeg)

However, a  const  variable cannot be reassigned  because it  is constant. If you

try to reassign a  const  variable, you’ll  get a  TypeError.

Constant variables must be assigned a value when declared. If you try to  declare a  const  variable without a  value, you’ll get a  SyntaxError.

If  you’re trying to decide between which keyword  to use,  let  or  const,  think  about whether you’ll need to reassign the variable later on. If you do need  to  reassign the variable use  let, otherwise, use  const.

Instructions  1.

Create  a  constant variable  named  entree  and  set it  to equal  to the  string  'Enchiladas'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Just  to  check that  you’ve saved the  value of  'Enchiladas'  to  entree,  log  the  value of  entree  to the  console.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Great, let’s see what happens if you try to reassign a constant variable.  Paste  the following  code to the bottom of  your  program.

entree  =  'Tacos'

This  code throws the following  error  when you  run your  code:

TypeError:  Assignment  to  constant  variable.

After you clear this checkpoint, if you want to see about another quirk  of  const  in action open the hint!

![](Images/image04587.jpeg)

Mathematical  Assignment  Operators

Let’s consider how we can use variables and math operators to calculate  new  values  and  assign  them  to  a  variable.  Check  out  the  example  below:

| let w = 4;  w  =  w  +  1;console.log(w);  //  Output:  5 |
| In  the  example  above,  we  created  the  variable  w | with  the  number  4 | assigned |
|  |  |  |

to  it. The following line,  w =  w +  1, increases the  value of  w  from  4  to  5.

Another way we could have reassigned  w  after performing some  mathematical operation on it is to use built-in mathematical assignment  operators.  We could re-write the code above to be:

![](Images/image04588.jpeg)

In the second example, we used the  +=  assignment operator to reassign  w.  We’re  performing  the  mathematical  operation of the  first  operator  +  using  the  number to the right, then  reassigning  w  to the  computed value.

We also have access to other mathematical assignment operators:  -=,  *=,  and /=  which  work in a  similar fashion.

![](Images/image04589.jpeg)

Let’s  practice  using these  mathematical assignment  operators!

Instructions  1.

Use  the  +=  mathematical assignment operator to increase the  value stored  in  levelUp  by  5.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

![](Images/image04590.jpeg)Use the  in

mathematical assignment operator to decrease the value stored  by  100.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Use  the  *=  mathematical assignment operator  to multiply  the value stored  in  multiplyMe  by  11.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Use  the  /=  mathematical assignment operator  to divide the value  stored  in  quarterMe  by  4.

![](Images/image04591.jpeg)

The  Increment  and  Decrement  Operator

Other mathematical assignment operators include the increment  operator  (++)  and decrement operator  (--).

![](Images/image04592.jpeg)The increment operator will increase the value of the variable by 1\. The  decrement operator will decrease the value of the variable by 1\. For  example:

variable’s value is updated and assigned as the new value of that variable.  Instructions 1.

Using  the  increment  operator, increase  the  value of  gainedDollar.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Using  the  decrement  operator,  decrease the  value  of  lostDollar.

![](Images/image04593.jpeg)

String  Concatenation  with  Variables

In previous exercises, we assigned strings to variables. Now, let’s go over  how  to connect,  or concatenate,  strings in variables.

The  +  operator can be  used  to combine two string  values  even if those  values  are  being stored in variables:

![](Images/image04594.jpeg)

In  the  example above,  we  assigned  the value  'armadillo'  to

the  myPet  variable. On the second line,  the  +  operator  is used to combine

three strings:  'I own a pet', the value saved to  myPet, and  '.'. We log the  result  of this concatenation to  the console as:

![](Images/image04595.jpeg)

1.

Create  a  variable named  favoriteAnimal  and  set  it equal  to your  favorite  animal.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Use  console.log()  to  print  'My favorite animal:  ANIMAL'  to the  console.  Use  string concatenation so that  ANIMAL  is replaced  with the value in

your favoriteAnimal  variable.

![](Images/image04596.jpeg)

String  Interpolation

In the ES6 version of JavaScript, we can insert, or interpolate, variables into  strings using template literals. Check out the following example where a  template  literal is used to log strings together:

![](Images/image04597.jpeg)

Notice  that:

*   ![](Images/image04598.jpeg)a template literal is wrapped  by backticks  `  (this  key is usually  located  on  the  top of your  keyboard, left of the  1  key).
*   Inside the template literal, you’ll see a placeholder,  ${myPet}. The value  of  myPet  is inserted into the template literal.
*   When we interpolate  `I own a pet ${myPet}.`, the output we print is the  string:  'I own a pet armadillo.'

One of the biggest benefits to using template literals is the readability of  the code. Using template literals, you can more easily tell what the new  string will be. You also don’t have to worry about escaping double quotes  or  single quotes.

![](Images/image04599.jpeg)

1.

![](Images/image04564.jpeg)Create  a  variable  called

Checkpoint 2  Passed

Stuck?  Get a hint

2.

![](Images/image04564.jpeg)Create  a  variable  called

Checkpoint 3  Passed

3.

and  assign it your  name.

![](Images/image04600.jpeg)![](Images/image04601.jpeg)and  assign  it your  favorite  city’s name.

Use a single template literal to interpolate your variables into the sentence  below. Use  console.log()  to print your sentence to the console in the  following  format:

My  name  is  NAME. My  favorite  city  is CITY.   Replace NAME  and  CITY  in the string above by interpolating the values saved  to  myName  and  myCity.

![](Images/image04602.jpeg)

typeof  operator

While writing code, it can be useful to keep track of the data types of the  variables in your program. If you need to check the data type of a variable’s  value, you can use the  typeof  operator.

The  typeof  operator checks the value to  its right and  returns,  or passes  back,  a  string  of the data type.

![](Images/image04603.jpeg)

![](Images/image04604.jpeg)Let’s break down the first example. Since the value  string, typeof unknown1  will return  'string'.

is  'foo',  a

Instructions

1.

Use  console.log()  to  print  the  typeof  newVariable.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Great, now let’s check what happens if we reassign the variable. Below  the  console.log()  statement,  reassign  newVariable  to  1.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Since you assigned this new value to  newVariable, it has a new type! On the  line  below your reassignment, use  console.log()  to print  typeof

newVariable  again.

![](Images/image04605.jpeg)

Review  Variables

Nice work! This lesson introduced you to variables, a powerful concept you will use in  all  your  future programming endeavors.

Let’s  review  what  we  learned:

*   Variables  hold reusable  data in  a program  and  associate it  with a  name.
*   Variables  are  stored in  memory.
*   The  var  keyword is used in pre-ES6 versions  of JS.
*   let  is the preferred way to declare a variable when it can be reassigned,  and  const  is the  preferred way to declare a variable with a constant value.

*   Variables  that  have not  been  initialized store  the  primitive data  type  undefined.
*   Mathematical assignment operators make it easy to calculate a new value and  assign  it  to the same variable.
*   The  +  operator is  used  to  concatenate  strings including  string values  held  in  variables
*   In  ES6,  template  literals use backticks  `  and  ${}  to interpolate  values into  a  string.
*   The  typeof  keyword returns  the data  type  (as a  string) of  a  value.

What  are  Conditional Statements?

In life, we make decisions based on circumstances. Think of an everyday  decision as mundane as falling asleep — if we are tired, we go to bed,  otherwise,  we wake up and  start our  day.

These if-else decisions can be modeled in code by creating conditional  statements. A conditional statement checks a specific condition(s) and  performs  a  task based on the condition(s).

In this lesson, we will explore how programs make decisions by evaluating  conditions  and  introduce logic into  our code!

We’ll  be covering  the following  concepts:

*   if,  else if,  and  else  statements
*   comparison  operators
*   logical  operators
*   truthy  vs falsy values
*   ternary  operators
*   switch  statement

So if you’re ready to learn these concepts go to the next lesson— else, read  over the concepts, observe the diagram, and prepare yourself for this  lesson!

Instructions

Check out the diagram to see how conditionals allow us to create decision-  making  technology.

![](Images/image04606.jpeg)

If  Statement

We often perform a task based on a condition. For example, if the weather  is nice today, then we will go outside. If the alarm clock rings, then we’ll  shut  it off. If we’re tired, then we’ll go to sleep.

In programming, we can also perform a task based on a condition using  an  if  statement:

![](Images/image04607.jpeg)

Notice  in  the example above, we have an  if  statement. The  if  statement is  composed of:

*   The  if  keyword  followed  by a set  of parentheses  ()  which is followed  by  a  code  block,  or block statement, indicated  by a set of curly

braces  {}.

*   Inside the parentheses  (), a condition is provided that evaluates  to  true  or  false.
*   If the condition evaluates to  true, the code inside the curly  braces  {}  runs, or executes.
*   If the condition evaluates to  false, the block won’t execute.  Let’s  make  an  if  statement.

Instructions

1.

Using  the  let  keyword, declare a  variable named  sale. Assign  the  value  true  to it.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Now  create an  if  statement.  Provide  the  if  statement a condition  of  sale.

Inside  the  code block of the  if  statement,  console.log()  the string  'Time to  buy!'.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Notice  that the code  inside  the  if  statement ran,  since  'Time to buy!'  was  logged  to the console.

Below the  sale  variable declaration, but  before  the  if  statement,

reassign  sale  to  false. Run  your  code and observe what happens,  we’ll be  changing  this behavior in the next exercise.

![](Images/image04608.jpeg)

If...Else  Statements

In  the  previous  exercise,  we  used an  if  statement  that checked a  condition  to decide whether or not to run a block of code. In many cases, we’ll have  code  we want  to run  if our condition evaluates  to  false.

If  we  wanted  to  add  some default behavior to the  if  statement, we can add  an  else  statement  to run a  block of code when the condition evaluates

to  false. Take  a look at the inclusion of  an  else  statement:

![](Images/image04609.jpeg)

An  else  statement  must be paired with an  if  statement, and together they  are  referred to as an  if...else  statement.

In  the  example  above,  the  else  statement:

*   Uses  the  else  keyword following  the code block of an  if  statement.
*   Has  a  code  block that  is wrapped  by a  set of  curly braces  {}.
*   The  code  inside  the  else  statement  code block will execute when  the  if  statement’s condition evaluates to  false.

if...else  statements  allow  us  to  automate  solutions  to yes-or-no  questions,  also  known as binary decisions.

Instructions  1.

Add  an  else  statement to the  existing  if  statement. Inside  the code  block of  the  else  statement,  console.log()  the  string  'Time to wait  for  a  sale.'

![](Images/image04610.jpeg)

Comparison  Operators

When writing conditional statements, sometimes we need to use different  types  of operators to  compare values. These operators  are

called  comparison operators.

Here  is a list  of some handy  comparison  operators and  their  syntax:

*   Less  than:  <
*   Greater  than:  >
*   Less  than  or equal  to:  <=
*   Greater  than or  equal to:  >=

*   Is  equal  to:  ===
*   Is  not equal  to:  !==

Comparison operators compare the value on the left with the value on the  right.  For instance:

10  < 12  //  Evaluates to  true  It can be helpful to think of comparison statements as questions. When the  answer  is  “yes”, the  statement evaluates  to  true, and when  the  answer  is  “no”, the statement evaluates to  false. The code above would be asking: is  10  less than 12? Yes! So  10 < 12  evaluates to  true.

We  can  also  use comparison  operators on  different data  types like  strings:

'apples'  ===  'oranges'  // false  In the example above, we’re using the identity operator (===) to check if the  string 'apples'  is the same as the string  'oranges'. Since the two strings are  not  the same,  the comparison statement evaluates to  false.

All  comparison  statements  evaluate to  either  true  or  false  and are  made up  of:

*   Two  values  that will  be  compared.
*   An operator that separates the values and compares them  accordingly  (>,  <,  <=,>=,===,!==).

Let’s  practice  using  these comparison  operators!

Instructions  1.

Using  let, create a  variable named  hungerLevel  and set it equal  to  7.

 Checkpoint 2 Passed

2.

Write an  if...else  statement using a comparison operator. The condition  should  check  if  hungerLevel  is greater  than  7.  If so,  the  conditional  statement  should  log,  'Time  to  eat!'. Otherwise, it  should log  'We  can eat  later!'.

After you press run, play around with the condition by tweaking the  comparison of  hungerLevel  by  using different  operators  such as  <=,>=,>,  and  <.

let  hungerLevel  =  7;

![](Images/image04611.jpeg)

Logical  Operators

Working  with conditionals means  that we will  be using

booleans,  true  or  false  values.  In JavaScript, there are operators  that work  with boolean values known as logical operators. We can use logical  operators to add more sophisticated logic to our conditionals. There are  three  logical operators:

*   the  and  operator  (&&)
*   the  or  operator  (||)
*   ![](Images/image04612.jpeg)the not operator, otherwise known as the bang operator (!)  When  we  use the  &&  operator, we are checking that  two  things are  true:

When  using  the &&  operator,  both conditions must  evaluate  to  true  for the  entire condition to evaluate to  true  and execute. Otherwise, if either  condition is  false, the  &&  condition will evaluate to  false  and  the  else  block  will execute.

If we only care about either condition being  true, we can use  the  ||  operator:

![](Images/image04613.jpeg)

When  using  the  ||  operator,  only  one  of  the  conditions  must  evaluate  to  true  for  the overall statement  to evaluate to  true.  In  the code example

above, if  either  day === 'Saturday'  or  day  === 'Sunday'  evaluates to  true  the  if‘s  condition will evaluate to  true  and  its code block will execute. If the first

condition  in  an  ||  statement  evaluates  to  true, the  second condition won’t  even be checked. Only if  day === 'Saturday'  evaluates to  false  will  day ===  'Sunday'  be evaluated. The code in the  else  statement above will execute  only  if both  comparisons evaluate to  false.

The  !  not operator  reverses, or  negates, the  value of a boolean:

![](Images/image04614.jpeg)

Essentially, the  !  operator  will either  take  a  true  value and  pass back  false, or  it  will take a  false  value and  pass back  true.

Logical operators are often used in conditional statements to add another  layer  of logic to our  code.

Instructions  1.

In  main.js there  are two variables  mood  and  tirednessLevel.

Let’s create an  if...else  statement  that checks

if  mood  is  'sleepy'  and  tirednessLevel  is  greater than  8.

If  both  conditions evaluate  to  true,  then  console.log()  the  string  'time  to  sleep'.  Otherwise, we should  console.log()  'not bed time  yet'.

After you press “Run”, play  around  with the  ||  operator and the  !  operator!  What happens if you negate the value of the entire statement with  !  and  switch  to  ||  instead  of  &&?

![](Images/image04615.jpeg)

Truthy  and Falsy

Let’s consider how non-boolean data types, like strings or numbers, are  evaluated  when checked inside  a condition.

Sometimes, you’ll want to check if a variable exists and you won’t  necessarily want it to equal a specific value — you’ll only check to see if the  variable  has been assigned a value.

Here’s  an  example:

![](Images/image04616.jpeg)The  code block in the

statement  will  run  because

has

![](Images/image04617.jpeg)a truthy value; even though the value of  myVariable  is not explicitly the  value  true, when used in a boolean or conditional context, it evaluates  to  true  because  it  has been assigned a non-falsy value.

So  which  values  are  falsy— or  evaluate to  false  when checked  as a  condition?  The list of falsy values includes:

*   0
*   Empty strings like  ""  or  ''
*   null  which represent when  there is no value  at all
*   undefined  which represent when  a declared variable lacks  a value
*   NaN, or Not a Number  Here’s  an  example  with  numbers:

![](Images/image04618.jpeg)

The  condition evaluates  to  false  because the value of  the  numberOfApples  is  0.  Since  0  is a falsy value, the  code block  in the  else  statement  will run.

Instructions  1.

Change the  value  of  wordCount  so that  it is  truthy. This  value should  still be  a  number.

After you make this change and run your code,  'Great! You've started your  work!'  should log to  the console.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Change the value of  favoritePhrase  so that it  is still a string but  falsy.

After you make this change and run your code,  'This string is definitely  empty.'  should log to the console.

![](Images/image04619.jpeg)

Truthy  and Falsy  Assignment

Truthy  and  falsy  evaluations open  a  world of  short-hand  possibilities!

Say you have a website and want to take a user’s username to make a  personalized  greeting.  Sometimes,  the  user  does  not  have  an  account,

making  the  username  variable falsy. The code below  checks if  username  is  defined  and assigns a default string if it is not:

![](Images/image04620.jpeg)

If you combine your knowledge of logical operators you can use a short-  hand for the code above. In a boolean condition, JavaScript assigns the  truthy value to a  variable if you  use the  ||  operator  in your assignment:

let  defaultName  =  username  ||  'Stranger';

Because  ||  or statements check the  left-hand condition first, the

variable defaultName  will be assigned the actual value of  username  if is truthy,  and it will be assigned the value of  'Stranger'  if  username  is falsy.  This concept  is  also referred to as short-circuit evaluation.

Instructions  1.

Let’s use short-circuit evaluation to assign a value to  writingUtensil. Do not  edit  tool  yet,  we’ll return to  tool  in the next step.

Assign  to  writingUtensil  the value of  tool  and  if  tool  is falsy, assign a default  value of  'pen'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Notice  that text  'The pen is  mightier than the sword'  logged to the console.  Which  means the value of  writingUtensil  is  'pen'.

What  if we reassign the value of  tool  to  'marker'. Let’s see  what happens to  the  value  of  writingUtensil.

![](Images/image04621.jpeg)

![](Images/image04622.jpeg)

Ternary  Operator

In the spirit of using short-hand syntax, we can use a ternary operator to  simplify an  if...else  statement.

Take  a look at the  if...else  statement  example:

![](Images/image04623.jpeg)

We  can  use a  ternary  operator  to perform the  same functionality:

![](Images/image04624.jpeg)

In  the  example  above:

*   The  condition,  isNightTime,  is  provided  before  the  ?.
*   Two  expressions  follow the  ?  and  are separated by  a colon  :.
*   If  the condition  evaluates to  true,  the  first expression executes.
*   If  the  condition evaluates  to  false,  the second  expression executes.

Like  if...else  statements,  ternary operators  can  be  used  for conditions  which evaluate to  true  or  false.

Instructions  1.

Refactor, or edit, the first  if...else  block to use a  ternary operator.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Refactor the second  if...else  block to use  a  ternary operator.

 Checkpoint 3 Passed

3.

Refactor the third  if...else  block to use a ternary operator.

![](Images/image04625.jpeg)

Else  If Statements

We  can add more conditions to our  if...else  with  an  else if  statement.

The  else if  statement allows for  more than two possible outcomes. You can  add as many  else if  statements as you’d like, to make more complex  conditionals!

The  else if  statement always comes after the  if  statement and before

the  else  statement.  The  else if  statement  also takes a condition. Let’s take a  look  at the syntax:

![](Images/image04626.jpeg)

The  else if  statements allow you to  have multiple  possible

outcomes.  if/else if/else  statements are read from top to bottom, so the

first  condition  that evaluates to  true  from the top to bottom is the block  that  gets executed.

In  the  example above,  since  stopLight  === 'red'  evaluates

to  false  and  stopLight  ===  'yellow'  evaluates  to  true,  the code inside the  first else if  statement is executed. The rest of the conditions are not  evaluated. If none of the conditions evaluated to  true, then the code in  the  else  statement  would have executed.

Instructions  1.

Let’s create a program that keeps track of the way the environment  changes with the seasons. Write a conditional statement to make this  happen!

In  main.js there is already an  if...else  statement  in  place.  Let’s add an  else  if  statement that checks if  season  is  equal to  'winter'.

Inside  the  code block  of the  else if  statement, add a  console.log()  that prints  the  string  'It\'s winter!  Everything  is  covered in  snow.'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Add  another else if  statement  that checks  if  season  is  equal to  'fall'.

Inside  the  code  block of the  else if  statement  you just created,  add  a  console.log()  that  prints  the string  'It\'s fall!  Leaves are falling!'.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Add  a final  else if  statement that checks if  season  is equal to  'summer'.

Inside the code block of the  else if  statement you just created, add  a  console.log()  that prints the  string  'It\'s  sunny and  warm  because  it\'s  summer!'.

let  season  =  'summer';

![](Images/image04627.jpeg)

The  switch keyword

else  if  statements  are a  great tool  if  we  need  to check  multiple  conditions.  In programming, we often find ourselves needing to check multiple values  and  handling each of them differently.  For  example:

![](Images/image04628.jpeg)

In the code above, we have a series of conditions checking for a value that  matches a  groceryItem  variable. Our code works fine, but imagine if we  needed  to check 100 different  values! Having  to write that many  else

if  statements  sounds  like  a  pain!

A  switch  statement provides an alternative syntax that is easier  to read and  write. A  switch  statement looks like this:

![](Images/image04629.jpeg)

![](Images/image04630.jpeg)

*   The  switch  keyword initiates the  statement and is followed  by  (  ...  ),

which  contains  the value that each  case  will compare. In the  example,  the  value or expression of the  switch  statement is  groceryItem.

*   Inside the block,  { ... }, there are multiple  cases. The  case  keyword  checks if the expression matches the specified value that comes after  it.  The value following the first  case  is  'tomato'.  If  the value

of  groceryItem  equalled  'tomato',  that  case‘s  console.log()  would  run.

*   The  value  of  groceryItem  is  'papaya',  so the third  case  runs—  Papayas are

$1.29  is logged  to the console.

*   The  break  keyword tells the computer to exit the block and not  execute any more code or check any other cases inside the code  block.  Note: Without  break  keywords,  the first  matching case will  run,  but so will every subsequent case regardless of whether or not it  matches—including  the default. This behavior  is different

from  if/else  conditional statements  that execute  only  one  block of  code.

*   At the end of each  switch  statement, there is a  default  statement. If  none  of the  cases  are true, then the  code in the  default  statement will  run.

Instructions  1.

Let’s  write a  switch  statement  to decide what medal  to award an athlete.

athleteFinalPosition  is already defined at the  top of main.js.  So start by  writing  a  switch  statement  with  athleteFinalPosition  as  its expression.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside the  switch  statement,  add three  cases:

*   The  first  case  checks  for  the value  'first place'
    *   If  the expression’s  value matches  the value of

the case  then  console.log()  the  string  'You  get  the gold  medal!'

*   The  second  case  checks for the value  'second place'
    *   If  the expression’s  value matches  the value of

the case  then  console.log()  the  string  'You  get  the silver  medal!'

*   The  third  case  checks for the value  'third place'
    *   If  the expression’s  value matches  the value of

the case  then  console.log()  the  string  'You  get  the bronze  medal!'

Remember to  add  a  break  after each  console.log().

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Now, add  a  default  statement  at  the  end  of  the  switch  that  uses  console.log()  to  print  'No medal  awarded.'.

If  athleteFinalPosition  does  not equal any  value of our  cases, then  the  string  'No medal awarded.'  is logged to the console.

Remember to add  the  break  keyword at  the  end of  the  default  case.

![](Images/image04631.jpeg)

}

Review

Way  to  go! Here  are some  of  the major concepts for  conditionals:

*   An  if  statement  checks  a  condition and will execute a  task if that  condition  evaluates to  true.
*   if...else  statements  make binary decisions and execute  different  code blocks  based on  a provided  condition.
*   We  can add more conditions using  else if  statements.
*   Comparison operators,  including  <,  >,  <=,  >=,  ===, and  !==  can  compare  two  values.
*   The logical and operator,  &&, or “and”, checks if both provided  expressions  are truthy.
*   The logical operator  ||, or “or”, checks if either provided expression is  truthy.
*   The  bang operator,  !, switches the  truthiness and  falsiness of  a  value.
*   The ternary operator is shorthand to simplify  concise  if...else  statements.
*   A  switch  statement  can be used to simplify  the process of writing  multiple  else if  statements. The  break  keyword stops the  remaining  cases from being checked and executed in

a  switch  statement.

Instructions

In  main.js, practice the  skills you learned  in this lesson.

What  are Functions?

When first learning how to calculate the area of a rectangle, there’s a sequence of  steps  to calculate  the correct answer:

1. Measure  the width  of the rectangle.

2. Measure  the height  of  the rectangle.

3. Multiply  the  width and  height of  the rectangle.

With practice, you can calculate the area of the rectangle without being instructed  with  these  three steps every  time.

We  can  calculate the  area of  one rectangle  with the  following  code:

![](Images/image04632.jpeg)

Imagine  being asked to  calculate the area  of  three different rectangles:

![](Images/image04633.jpeg)

In programming, we often use code to perform a specific task multiple times. Instead  of rewriting the same code, we can group a block of code together and associate it  with one task, then we can reuse that block of code whenever we need to perform  the task again. We achieve this by creating a function. A function is a reusable block  of  code  that groups together  a sequence of  statements to perform a  specific  task.

In this lesson, you will learn how to create and use functions, and how they can be  used  to create clearer and  more concise code.

Function  Declarations

In JavaScript, there are many ways to create a function. One way to create a  function  is by using a function  declaration.  Just like  how a  variable

declaration binds a value to a variable name, a function declaration binds a  function to a name, or an identifier. Take a look at the anatomy of a  function  declaration below:

A  function declaration  consists of:

*   The  function  keyword.
*   The  name of  the function,  or its identifier,  followed by  parentheses.
*   A function body, or the block of statements required to perform a  specific  task, enclosed in the function’s curly  brackets,  { }.

A function declaration is a function that is bound to an identifier, or name.  In the next exercise we’ll go over how to run the code inside the function  body.

We should also be aware of the hoisting feature in JavaScript which allows  access  to function  declarations before they’re defined.

Take  a  look at example of  hoisting:

![](Images/image04634.jpeg)

Notice how  hoisting  allowed  greetWorld()  to be called before

the  greetWorld()  function  was  defined! Since  hoisting isn’t  considered  good  practice,  we  simply want  you to be  aware of this feature.

If you want to read more about hoisting, check out [MDN documentation](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)  [on hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting).

Instructions  1.

Let’s create a function that prints a reminder to the console. Using a  function  declaration,  create  a function called  getReminder().

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

In the function body of  getReminder(), log the following reminder to the  console:  'Water  the plants.'

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Let’s create another function that prints a useful Spanish travel phrase to  the  console.

Using  a  function  declaration,  create  a  function called  greetInSpanish().

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Add  code  to the  function  body of  greetInSpanish():

*   In  the  function  body  console.log()  the  following Spanish  phrase  to  the  console:  'Buenas Tardes.'

![](Images/image04635.jpeg)

Calling  a Function

As we saw in previous exercises, a function declaration binds a function to  an  identifier.

However, a function declaration does not ask the code inside the function  body to run, it just declares the existence of the function. The code inside a  function  body runs, or  executes, only when  the function is called.

To call a function in your code, you type the function name followed by  parentheses.

This function call executes the function body, or all of the statements  between  the curly braces in the function  declaration.

We can call the same function as many times as needed.  Let’s  practice calling functions in our  code.

![](Images/image04636.jpeg)

1.

Imagine that you manage an online store. When a customer places an  order, you send them a thank you note. Let’s create a function to complete  this task:

*   ![](Images/image04637.jpeg)Define  a  function calledas a  function declaration.
*   In the function body of  sayThanks(), add code such that the  function writes the following thank you message to the  console when called:  'Thank you for your purchase! We appreciate  your  business.'

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Call  sayThanks()  to  view  the  thank  you message  in  the console.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Functions  can be  called as  many times  as you  need  them.

Imagine that three customers placed an order and you wanted to send  each  of them a thank you message.  Update  your code to

call  sayThanks()  three times.

![](Images/image04638.jpeg)

Parameters  and  Arguments

So far, the functions we’ve created execute a task without an input.  However, some functions can take inputs and use the inputs to perform a  task. When declaring a function, we can specify its parameters. Parameters  allow functions to accept input(s) and perform a task using the input(s). We  use parameters as placeholders for information that will be passed to the  function  when it is called.

Let’s  observe  how  to specify parameters  in our  function  declaration:

In the diagram above,  calculateArea(), computes the area of a rectangle,  based  on  two inputs,  width  and  height. The  parameters are specified between  the parenthesis as  width  and  height, and inside the function body, they act  just  like regular  variables.  width  and  height  act as placeholders for values that  will  be multiplied  together.

When calling a function that has parameters, we specify the values in the  parentheses that follow the function name. The values that are passed to  the function when it is called are called arguments. Arguments can be  passed  to the  function as values or variables.

In the function call above, the number  10  is passed as the  width  and  6  is  passed as  height. Notice that the order in which arguments are passed and  assigned  follows the order that the  parameters are declared.

The  variables  rectWidth  and  rectHeight  are initialized with the values  for  the  height  and width of  a rectangle  before  being used in the  function  call.

By using parameters, calculateArea()  can be reused to compute the area of  any rectangle! Functions are a powerful tool in computer programming so  let’s  practice creating  and calling functions with  parameters.

Instructions

1.

The  sayThanks()  function works  well,  but  let’s add  the customer’s  name in the  message.

Add  a  parameter called  name  to  the function  declaration  for  sayThanks().

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

With  name  as  a  parameter, it  can  be used  as a variable in  the  function  body  of  sayThanks().

Using  name  and  string concatenation,  change  the thank you  message into  the  following:

![](Images/image04639.jpeg)

Copy  and  paste  the above message  into  your  code.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

A customer named Cole just purchased something from your online store.  Call  sayThanks()  and pass  'Cole'  as  an argument  to send  Cole  a  personalized  thank  you message.

![](Images/image04640.jpeg)

Default  Parameters

One of the features added in ES6 is the ability to use default parameters.  Default parameters allow parameters to have a predetermined value in case  there  is no argument passed into  the function or  if  the  argument

is  undefined  when  called.

Take  a  look  at the  code snippet  below that  uses a  default parameter:

![](Images/image04641.jpeg)

*   In  the example above,  we used the  =  operator to assign the

![](Images/image04568.jpeg)parameter  name  a  default  value of  'stranger'. This is useful  to have in  case  we  ever want to  include a  non-personalized default  greeting!

*   When the  code  calls  greeting('Nick')  the  value of the argument is  passed  in and,  'Nick', will  override the default parameter

of  'stranger'  to log  'Hello,  Nick!'  to the console.

*   When there isn’t an argument passed into  greeting(), the default value  of  'stranger'  is used, and  'Hello, stranger!'  is logged to the console.

By using a default parameter, we account for situations when an argument  isn’t  passed into a function  that is expecting  an argument.

Let’s  practice  creating functions  that use  default parameters.

Instructions  1.

The  function  makeShoppingList()  creates  a shopping list  based on the items  that  are passed to  the function as arguments.

Imagine that you always purchase milk, bread, and eggs every time you go  shopping for groceries. To make creating a grocery list easier, let’s assign  default  values to the parameters in  makeShoppingList().

Change the parameters of  makeShoppingList()  into  default parameters  :

*   Assign  ‘milk’ as the default value  of  item1.
*   Assign  ‘bread’ as  the default  value of  item2.
*   Assign  ‘eggs’ as the  default value of  item3.

![](Images/image04642.jpeg)

![](Images/image04643.jpeg)

Return

When a function is called, the computer will run through the function’s  code and evaluate the result of calling the function. By default that  resulting  value is  undefined.

![](Images/image04644.jpeg)

In  the  code  example,  we defined our function to calculate the  area  of  a  width  and  height  parameter. Then  rectangleArea()  is  invoked with  the

arguments 5  and  7. But when we went to print the results we got  undefined.  Did we write our function wrong? No! In fact, the function worked fine, and  the computer did calculate the area as  35, but we didn’t capture it. So how  can  we do that? With  the keyword  return!

To pass back information from the function call, we use a return statement.  To create a return statement, we use the  return  keyword followed by the  value  that we wish to  return. Like we  saw  above,  if the value is

omitted,  undefined  is  returned  instead.

When a  return  statement is used in a function body, the execution of the  function is stopped and the code that follows it will not be executed. Look  at  the example below:

![](Images/image04645.jpeg)

![](Images/image04646.jpeg)![](Images/image04647.jpeg)If  an argument fororis  less than  0, then  rectangleArea()  will

return  'You need positive integers to calculate area!'. The second return  statement  width  * height  will not run.

The  return  keyword is  powerful because  it  allows functions  to produce  an  output.  We can then save  the output to a  variable for later use.

Instructions  1.

Imagine if we needed to order monitors for everyone in an office and this  office is conveniently arranged in a grid shape. We could use a function to  help  us calculate  the number of  monitors needed!

Declare a  function  monitorCount()  that  has two  parameters. The  first  parameter is  rows  and the second parameter is  columns.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Let’s  compute  the  number  of monitors by  multiplying  rows  and  columns  and  then  returning  the value.

In  the  function body  of  the  function you  just wrote, use  the  return  keyword  to  return  rows  * columns.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Now that the function is defined, we can compute the number of monitors  needed.  Let’s say that  the office has 5 rows and 4 columns.

Declare a  variable named  numOfMonitors  using the  const  keyword  and  assign numOfMonitors  the value of invoking  monitorCount()  with the  arguments  5  and  4.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

To  check that the  function worked properly, log  numOfMonitors  to the  console.

![](Images/image04648.jpeg)

Helper  Functions

We can also use the return value of a function inside another function.  These functions being called within another function are often referred to  as helper functions. Since each function is carrying out a specific task, it  makes  our code easier  to read and debug if  necessary.

If we wanted to define a function that converts the temperature from  Celsius  to Fahrenheit, we  could write  two  functions like:

![](Images/image04649.jpeg)

In  the  example  above:

*   getFahrenheit()  is  called and  15  is passed  as  an argument.
*   The  code  block  inside of  getFahrenheit()  calls  multiplyByNineFifths()  and  passes  15  as an argument.
*   multiplyByNineFifths()  takes  the  argument  of  15  for  the  number  parameter.
*   The  code  block  inside  of  multiplyByNineFifths()  function  multiplies  15  by  (9/5), which evaluates to  27.
*   27  is  returned back  to the  function  call in  getFahrenheit().
*   getFahrenheit()  continues  to  execute. It  adds  32  to  27,  which  evaluates  to  59.
*   Finally,  59  is returned back to the  function call  getFahrenheit(15).

We can use functions to section off small bits of logic or tasks, then use  them when we need to. Writing helper functions can help take large and  difficult  tasks and  break them into  smaller  and more  manageable tasks.

![](Images/image04650.jpeg)

1.

In the previous exercise, we created a function to find the number of  monitors to order for an office. Now let’s write another function that uses  the  monitorCount  function to figure out  the price.

Below  monitorCount  Create a  function declaration  named  costOfMonitors  that  has  two parameters,  the first parameter is  rows  and  the second  parameter  is  columns. Leave the function body empty  for now.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Time  to  add some code to the function body of  costOfMonitors  to calculate  the  total cost.

Add  a return  statement  that returns the  value  of calling  monitorCount(rows,  columns)  multiplied by  200.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

We  should  save the  cost  to a  variable.

Declare a  variable named  totalCost  using the  const  keyword.  Assign  to  totalCost  the  value of  calling  costOfMonitors()  with  the

arguments  5  and  4  respectively.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

To  check that the  function worked properly, log  totalCost  to the console.

![](Images/image04651.jpeg)

![](Images/image04652.jpeg)

Function  Expressions

Another way to define a function is to use a function expression. To define a  function  inside  an  expression, we  can  use  the  function  keyword.  In a  function  expression,  the  function  name  is  usually  omitted.  A  function  with  no  name  is called an anonymous function. A function expression is often stored in a  variable  in  order  to refer  to it.

Consider  the  following  function  expression:

To  declare  a function  expression:

1. Declare a variable to make the variable’s name be the name, or  identifier, of your function. Since the release of ES6, it is common  practice to use  const  as the  keyword  to declare  the variable.

2. Assign as that variable’s value an anonymous function created by  using the  function  keyword followed by a set of parentheses with  possible parameters. Then a set of curly braces that contain the  function  body.

To invoke a function expression, write the name of the variable in which the  function is stored followed by parentheses enclosing any arguments being  passed into the  function.

variableName(argument1,  argument2)  Unlike function declarations, function expressions are not hoisted so they  cannot  be called before they are defined.

Let’s  define a  new  function  using  a function  expression.

Instructions  1.

Let’s say we have a plant that we need to water once a week on  Wednesdays. We could define a function expression to help us check the  day  of the week and the plant needs to  be watered:

*   Create  a  variable  named  plantNeedsWater  using the  const  variable  keyword.
*   Assign an anonymous function that takes in a parameter  of  day  to  plantNeedsWater.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Now  we need to  add some  code  to the  function  body  of  plantNeedsWater():

*   In  the  function  body  add  an  if  conditional that  checks  day  ===  'Wednesday'.
*   If  the  conditional  is truthy, inside the  if  code  block, use  the  return  keyword  to return  true.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

On  days  that  aren’t  'Wednesday',  plantNeedsWater()  should return  false:

*   Add  an  else  statement after  the  if  statement.
*   Inside  the  else  statement use the  return  keyword to  return  false.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Call  the  plantNeedsWater()  and  pass  in  'Tuesday'  as  an  argument.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Let’s  check that  plantNeedsWater()  returned the  expected value.

Log  plantNeedsWater('Tuesday')  to  the  console.  If  it  worked  correctly,  you  should see  false  logged to  the console.

![](Images/image04653.jpeg)

![](Images/image04654.jpeg)

row  Functions

ES6 introduced arrow function syntax, a shorter way to write functions by  using the special “fat  arrow”  ()  =>  notation.

Arrow functions remove the need to type out the keyword  function  every  time you need to create a function. Instead, you first include the parameters  inside the  ( )  and then add an arrow  =>  that points to the function body  surrounded in  { }  like this:

![](Images/image04655.jpeg)

It’s important to be familiar with the multiple ways of writing functions  because you will come across each of these when reading other JavaScript  code.

Instructions  1.

Change plantNeedsWater()  to use arrow function syntax.

![](Images/image04656.jpeg)

};

Concise  Body  Arrow Functions

JavaScript also provides several ways to refactor arrow function syntax. The  most condensed form of the function is known as concise body. We’ll  explore  a few of these  techniques below:

1. Functions that take only a single parameter do not need that  parameter to be enclosed in parentheses. However, if a function takes  zero  or  multiple parameters,  parentheses  are required.

2. A function body composed of a single-line block does not need curly  braces. Without the curly braces, whatever that line evaluates will be  automatically returned. The contents of the block should immediately  follow the arrow  =>  and the  return  keyword can be removed. This is  referred  to as implicit return.

So  if we have a function:

![](Images/image04657.jpeg)

We  can  refactor  the function  to:

const  squareNum  =  num  =>  num  *  num;

Notice  the  following changes:

*   The  parentheses  around  num  have been removed, since  it has a single  parameter.
*   The  curly  braces  {  }  have been removed since the function  consists of  a single-line block.
*   The  return  keyword  has been removed since the function consists of a  single-line  block.

Instructions  1.

![](Images/image04658.jpeg)Let’s  refactorto be  a concise body.  Notice that  we’ve

already  converted  the  if/else  statement  to  a  ternary operator to  make  the  code  fit on  one line.

const  plantNeedsWater  =  day =>  day  ===  'Wednesday'  ?  true :  false;

Review  Functions

Give yourself a pat on the back, you just navigated through functions!  In  this  lesson,  we  covered some  important concepts  about functions:

*   A function is a reusable block of code that groups together a sequence of  statements  to perform a specific task.
*   A  function  declaration  :

*   A parameter is a named variable inside a function’s block which will be  assigned  the value  of  the argument  passed  in  when the  function  is invoked:

*   To  call  a function  in your code:

*   ES6 introduces new ways of handling arbitrary parameters through default  parameters which allow us to assign a default value to a parameter in case no  argument  is passed into the function.
*   To  return a value  from a  function, we  use a return  statement.
*   To  define  a function  using function  expressions:

*   To  define  a function  using arrow  function notation:

*   Function  definition  can be  made concise  using concise  arrow  notation:

It’s good to be aware of the differences between function expressions, arrow  functions, and function declarations. As you program more in JavaScript, you’ll see a  wide  variety of how  these function types are used.

Scope

An important idea in programming is scope. Scope defines where variables can be  accessed or referenced. While some variables can be accessed from anywhere within  a  program,  other variables may  only  be available in a  specific  context.

You can think of scope like the view of the night sky from your window. Everyone  who lives on the planet Earth is in the global scope of the stars. The stars are  accessible globally. Meanwhile, if you live in a city, you may see the city skyline or the  river. The skyline and river are only accessible locally in your city, but you can still see  the  stars that are available globally.

Over the next few exercises, we’ll explore how scope relates to variables and learn  best  practices for variable declaration.

Blocks  and Scope

Before  we talk  more about  scope, we  first  need to  talk about  blocks.

We’ve seen blocks used before in functions and  if  statements. A block is  the code found inside a set of curly braces  {}. Blocks help us group one or  more statements together and serve as an important structural marker for  our  code.

A  block of code could  be a function, like  this:

![](Images/image04659.jpeg)

Notice that the function body is actually a block of code.  Observe the block in an  if  statement:

![](Images/image04660.jpeg)In the next few exercises, we’ll see how blocks define the scope of variables.  Instructions               1.

At  the top  of  main.js, declare a  const  variable, named  city  set equal to  'New  York  City'. This variable  will exist outside  of the block.

 Checkpoint 2 Passed

2.

Below  the city  variable,  write a function named  logCitySkyline.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Inside of the function body of  logCitySkyline(), write another variable  using  let  named  skyscraper  and set it equal to  'Empire State  Building'.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Inside  the function,  include a return  statement like  this:

![](Images/image04661.jpeg)

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Beneath the  logCitySkyline()  function,  use  console.log()  to log  the value  of  logCitySkyline()  to  the console.

You’ll notice that the  logCitySkyline()  function is able to access both  variables without any problems. In the next exercise we’ll consider why  would it be preferable to have one variable outside of a block and the other  inside  of a block.

![](Images/image04662.jpeg)

Global  Scope

Scope is the context in which our variables are declared. We think about  scope in relation to blocks because variables can exist either outside of or  within  these blocks.

In global scope, variables are declared outside of blocks. These variables are  called global variables. Because global variables are not bound inside a block,  they  can be  accessed by  any code in  the program,  including code  in blocks.

Let’s  take  a look at an  example  of global scope:

![](Images/image04663.jpeg)

*   Even  though  the  color  variable is defined outside of  the block,  it can  be  accessed in the function  block, giving it  global scope.
*   In  turn,  color  can  be accessed within the  returnSkyColor  function  block.

Let’s work with global variables to see how data can be accessible from any  place  within a program.

Instructions  1.

At  the  top of main.js, write three  global variables:

*   Name  the first variable  satellite  and set it equal to  'The  Moon'.
*   Name  the  second variable  galaxy  and set it  equal to  'The Milky  Way'.
*   Name  the third variable  stars  and  set it equal to  'North  Star'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Below  the  variables  created  in  the  previous  step,  write  a  function  named  callMyNightSky. Inside the function, include a return statement like  this:

![](Images/image04664.jpeg)

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Beneath  the

![](Images/image04665.jpeg)function, use  console.log()  to  log the  value

of  callMyNightSky()  to  the  console.

You’ll notice that the function block for  callMyNightSky()  is able to  access the  global variables freely since the variables are available to all lines of code in  the file.

![](Images/image04666.jpeg)

Block  Scope

The next context we’ll cover is block scope. When a variable is defined inside  a block, it is only accessible to the code within the curly braces  {}. We say  that variable has block scope because it is only accessible to the lines of  code  within that block.

Variables that are declared with block scope are known as local  variables because they are only available to the code that is part of the  same block.

Block  scope works like  this:

![](Images/image04667.jpeg)

You’ll  notice:

*   We  define  a  function  logSkyColor().
*   Within  the  function, the  color  variable is only available  within the curly  braces  of the function.
*   If we try to log the same variable outside the function, throws  a  ReferenceError.

Instructions  1.

In  main.js,  define  a  function  logVisibleLightWaves().

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Within the logVisibleLightWaves()  function, using  const, create a  variable lightWaves  and set it equal to  'Moonlight'.

 Checkpoint 3 Passed

3.

Within the logVisibleLightWaves()  function, beneath the  lightWaves  variable,  add a  console.log()  statement that  will  log  the value  of  the  lightWaves  variable  when  the function runs.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Call  the  logVisibleLightWaves()  function from outside the function.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Beneath  the  function call, log  the value of  lightWaves  to  the console from  outside  the function.

You’ll  notice that it  logs a  ReferenceError  since the  variable is tied to  the  block  scope of the function!

![](Images/image04668.jpeg)

Scope  Pollution

It may seem like a great idea to always make your variables accessible, but  having  too many  global variables can  cause problems in  a program.

When you declare global variables, they go to the global namespace. The  global namespace allows the variables to be accessible from anywhere in  the program. These variables remain there until the program finishes which  means  our global namespace can fill up really  quickly.

Scope pollution is when we have too many global variables that exist in the  global  namespace,  or  when we reuse  variables across different  scopes.

Scope pollution makes it difficult to keep track of our different variables  and sets us up for potential accidents. For example, globally scoped  variables can collide with other variables that are more locally scoped,  causing  unexpected behavior  in our code.

Let’s look at an example of scope pollution in practice so we know how to  avoid it:

![](Images/image04669.jpeg)

You’ll  notice:

*   We  have  a variable  num.
*   Inside the function body of  logNum(), we want to declare a new  variable but forgot to use the  let  keyword.
*   When we call  logNum(),  num  gets reassigned  to  100.
*   The  reassignment inside  logNum()  affects  the  global variable  num.
*   Even though the reassignment is allowed and we won’t get an error,  if we decided to use  num  later, we’ll unknowingly use the new value  of  num.

While it’s important to know what global scope is, it’s best practice to not  define  variables in  the global scope.

Instructions

1.

Let’s see what happens if we create a variable that overwrites a global  variable.

Inside  the  callMyNightSky()  function,  on the  very  first line  of the  function  body, assign the variable  stars  to  'Sirius'  as such:

![](Images/image04670.jpeg)

 Checkpoint 2 Passed

2.

Outside  the  function, under the current  console.log()  statement,  add  another  console.log()  statement to  log  stars  to the  console.

You’ll notice that the global variable  stars  was reassigned to  'Sirius'. In  other words, we  changed  the value of  the global  stars  variable but it’s  not  easy to read what exactly happened. This is bad practice in code  maintainability  and  could  impact our  program  in ways we  do not intend.

![](Images/image04671.jpeg)

Practice  Good Scoping

Given the challenges with global variables and scope pollution, we should  follow best practices for scoping our variables as tightly as possible using  block scope.

Tightly scoping your variables will greatly improve your code in several  ways:

*   It will make your code more legible since the blocks will organize  your  code into discrete  sections.
*   It makes your code more understandable since it clarifies which  variables are associated with different parts of the program rather  than  having to keep track of them line after line!
*   It’s  easier to  maintain your code,  since your  code will be  modular.
*   It will save memory in your code because it will cease to exist after  the block  finishes running.

Here’s another example of how to use block scope, as defined within  an  if  block:

![](Images/image04672.jpeg)

Here,  you’ll notice:

*   We  create a  variable  dusk  inside the  logSkyColor()  function.
*   After  the  if  statement, we  define a new code block  with the  {}  braces.  Here we assign a new value to the variable  color  if the  if  statement is  truthy.
*   Within the  if  block, the  color  variable holds the value  'pink', though  outside  the  if  block, in the function body, the  color  variable holds the  value  'blue'.
*   While we use block scope, we still pollute our namespace by reusing  the same variable name twice. A better practice would be to rename  the  variable inside  the block.

Block scope is a powerful tool in JavaScript, since it allows us to define  variables with precision, and not pollute the global namespace. If a variable  does  not need to exist outside a block— it shouldn’t!

Instructions

1.

Inside  the  function body  of  logVisibleLightWaves(), beneath the  region  variable  and before the  provided  console.log()  statement, create an  if  statement that  checks if the  region  is the  'The  Arctic'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside  the  if  block,  define a new  let  variable  lightWaves  and set it equal  to  'Northern Lights'.

 Checkpoint 3 Passed

3.

Beneath  the  variable in the  if  block, use  console.log()  to log the value of the  block variable inside the  if  block.

Run  your  code and  notice the  output. Inside

the  if  block  console.log(lightWaves)  logs the value  Northern  Lights  to the  console. Outside the  if  block, but still within the function, the same  statement logs  Moonlight  to the  console.

![](Images/image04673.jpeg)

Review:  Scope

In this lesson, you learned about scope and how it impacts the accessibility of  different  variables.

Let’s  review  the following  terms:

*   Scope is the idea in programming that some variables are  accessible/inaccessible  from  other parts  of  the program.

*   Blocks  are  statements that  exist within  curly  braces  {}.
*   Global scope refers to the context within which variables are accessible to  every  part  of the program.
*   Global  variables  are  variables that  exist within global  scope.
*   Block scope refers to the context within which variables that are accessible  only  within the block they are defined.
*   Local  variables  are  variables that  exist within block  scope.
*   Global namespace is the space in our code that contains globally scoped  information.
*   Scope pollution is when too many variables exist in a namespace or variable  names  are reused.

Arrays

Organizing  and  storing data  is a  foundational concept  of  programming.

One way we organize data in real life is by making lists. Let’s make one  here:

New  Year's  Resolutions:

1. Keep  a journal

2. Take  a  falconry  class

3. Learn  to juggle

Let’s  now  write  this  list in JavaScript, as  an array:

![](Images/image04674.jpeg)

Arrays are JavaScript’s way of making lists. Arrays can store any data types  (including strings, numbers, and booleans). Like lists, arrays are ordered,  meaning  each  item has a  numbered position.

Here’s  an  array  of the concepts  we’ll cover:

![](Images/image04675.jpeg)

By the end of this lesson you’ll have another tool under your belt that helps  you  manage chunks of data!

![](Images/image04676.jpeg)

Run  the code  to see  what is logged  to the  console.

![](Images/image04677.jpeg)

Create  an  Array

One way we can create an array is to use an array literal. An array literal  creates an array by wrapping items in square brackets  []. Remember from  the  previous exercise, arrays  can store any  data type —  we can have  an

array that holds all the same data types or an array that holds different data  types.

Let’s  take  a closer  look at  the syntax  in the  array example:

*   The  array  is  represented by the square  brackets  []  and the content  inside.
*   Each  content  item inside  an  array is  called  an element.
*   There  are  three  different  elements inside  the  array.
*   Each  element inside  the array  is a  different data type.

We can also save an array to a variable. You may have noticed we did this in  the  previous exercise:

![](Images/image04678.jpeg)

Let’s  practice by  making an array  of our  own.

Instructions  1.

Declare a  variable using  const  named  hobbies  and  set  it  equal  to an  array  with  three strings inside of it.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Use  console.log()  to  print  hobbies  to  the  console.

![](Images/image04679.jpeg)

Accessing  Elements

Each element in an array has a numbered position known as its index. We  can access individual items using their index, which is similar to referencing  an  item in a list based on the item’s position.

![](Images/image04568.jpeg)Arrays in JavaScript are zero-indexed, meaning the positions start counting  from  0  rather than  1.  Therefore, the first  item in an array  will be at position  0.  Let’s  see how  we could access an  element in an array:

In  the  code snippet  above:

*   cities  is an array that has three elements.
*   We’re  using bracket notation,  []  with the index  after the name  of the  array  to  access the element.
*   cities[0]  will access the  element at index  0  in the array  cities.  You  can  think of  cities[0]  as accessing the space in memory that holds the  string  'New York'.

You can also access individual characters in a string using bracket notation  and  the index. For instance, you can write:

![](Images/image04680.jpeg)

The console will display  W  since it is the character  that is at index  6.

Instructions  1.

Individual  elements in  arrays  can also be stored  to variables.

Create  a  variable named  listItem  and set it equal to  the first item in  the  famousSayings  array  using square bracket  notation ([]).

Then  use  console.log()  to  print  the  listItem  variable  to  the  console.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Now, console.log()  the  third  element  in  the  famousSayings  array  using  bracket  notation  to access the element.

Do  not save the element  to  a new  variable before you  log it.

![](Images/image04681.jpeg)

![](Images/image04682.jpeg)

Update  Elements

In the previous exercise, you learned how to access elements inside an array  or a string by using an index. Once you have access to an element in an  array,  you can update its value.

![](Images/image04683.jpeg)In the example above, the  seasons.

array  contained the  names of  the  four

However, we  decided that we preferred  to  say  'Autumn'  instead of  'Fall'.

The  line,  seasons[3] =  'Autumn';  tells  our  program to  change  the item  at  index  3  of  the seasons  array  to  be  'Autumn'  instead of  what  is already there.

Instructions  1.

Change the second element  of the array  groceryList  to  'avocados'.

![](Images/image04684.jpeg)

Arrays  with let  and const

You  may  recall that  you can  declare variables  with both

the  let  and  const  keywords. Variables declared  with  let  can be reassigned.

Variables declared with the  const  keyword cannot be reassigned. However,  elements in an array declared with  const  remain mutable. Meaning that we  can  change the  contents of a  const  array, but  cannot reassign a new array or  a  different value.

The instructions below will illustrate this concept more clearly. Pay close  attention to the similarities and  differences between the  condiments  array and  the  utensils  array as you complete the steps.

Instructions  1.

Below the two existing arrays, re-assign the element in  index  0  of  condiments  to  'Mayo'.

Log  the updated  array,  condiments,  to  the console.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Below  your code from Step 1, reassign  condiments  to be a  new  array that  contains  a single string  ['Mayo']

Log  the result to the  console.

Notice that you can re-assign elements in an array and re-assign an entire  new array to a variable declared using the  let  keyword.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Below  your code  from Step 2,  re-assign  the last item from the  utensils  array  to  'Spoon'.

Log  the updated  array to  the console.

![](Images/image04685.jpeg)

![](Images/image04686.jpeg)The  .length  property

One of an array’s built-in properties is  items in the array. We access the  strings.  Check the example below:

and it returns the number of  property  just like we do  with

![](Images/image04687.jpeg)In the example above, we log  the  following  steps:

to  the console using

*   ![](Images/image04688.jpeg)![](Images/image04689.jpeg)We  use dot  notation,  chaining  a  period with  the property  name to  the

array,  to  access  the

*   Then  we log  the

property  of  the  n

of

![](Images/image04568.jpeg)to  the  console.

array.

*   Since  console.

has two  elements, so  2  would be logged  to the

When we want to know how many elements are in an array, we can access  the  .length  property.

Instructions  1.

Find  the  length  of  the  objectives  array and  log it  to the  console.

![](Images/image04690.jpeg)

The  .push()  Method

Let’s learn about some built-in JavaScript methods that make working with  arrays easier. These methods are specifically called on arrays to make  common  tasks,  like  adding  and  removing  elements,  more  straightforward.

One  method, .push()  allows us to add items to the end of an array. Here is  an  example of how this is used:

![](Images/image04691.jpeg)

So, how  does  .push()  work?

*   We  access  the  push  method by  using dot  notation,  connecting  push  to  itemTracker  with a  period.
*   Then  we  call it  like a function. That’s  because  .push()  is a  function and  one  that JavaScript  allows us to use right on  an array.
*   .push()  can  take  a  single  argument or  multiple arguments  separated  by  commas. In this case, we’re adding  two elements:  'item

3'  and  'item 4'  to  itemTracker.

*   Notice that  .push()  changes, or mutates,  itemTracker. You might also  see  .push()  referred to as a  destructive  array method  since it  changes  the  initial array.

If you’re looking for a method that will mutate an array by adding elements  to  it, then  .push()  is the method for you!

Instructions

1.

Add  two elements to  the

![](Images/image04692.jpeg)array  using  .push().

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Use  console.log  to  print your  chores  array  to make  sure your items  were  added.

![](Images/image04693.jpeg)

The  .pop()  Method

Another  array  method,  .pop(),  removes the  last  item of  an array.

![](Images/image04694.jpeg)

*   In  the  example  above,  calling  .pop()  on  the  newItemTracker  array  removed  item  2  from the end.
*   .pop()  does not  take any arguments, it simply removes the last  element  of  newItemTracker.
*   .pop()  returns  the  value  of the last element.  In the example,  we store  the  returned value in  a variable  removed  to  be  used  for later.
*   .pop()  is a method  that mutates the initial  array.

When you need to mutate an array by removing the last element,  use  .pop().

Instructions  1.

![](Images/image04695.jpeg)Use  themethod  to remove the  last element from  chores.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

In  a  line  after  you  called chores.pop(),  log  chores  to  the console to  make sure  it worked.

![](Images/image04696.jpeg)

More  Array  Methods

There  are many more array methods than  just  .push()  and  .pop(). You can  read about all of the array methods that exist on the [Mozilla Developer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)  [Network  (MDN) array  documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).

.pop()  and  .push()  mutate  the  array on  which they’re  called.  However, there  are times that we don’t want to mutate the original array and we can use  non-mutating array methods. Be sure to check MDN to understand the  behavior  of the method  you  are  using.

Some  arrays  methods  that are  available  to  JavaScript developers

include:  .join(),  .slice(),  .splice(),  .shift(),  .unshift(), and  .concat()  amongst  many others. Using these built-in methods make it easier to do some  common  tasks when working with arrays.

Below, we will explore some methods that we have not learned yet. We will  use these methods to edit a grocery list. As you complete the steps, you  can  consult  the MDN  documentation to learn what  each  method does!

Instructions  1.

Use  the  .shift()  method  to remove  the first  item from  the array  groceryList.  Log the new  groceryList  to the  console.

Read  about  .shift()  at  [MDN’s  shift documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift).

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Under the  code  added in step 1, use the  .unshift()  method  to  add 'popcorn'  to  the beginning  of  your grocery  list.

After calling  .unshift()  on  groceryList, log  groceryList  to  the  console.

You  may wish to  delete the  console.log()  statement  from the previous  step.  Read  about  .unshift()  at [MDN’s unshift documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift).

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

You’re in a hurry so you decide to ask a friend to help you with your  grocery shopping. You want him to pick up the  'bananas',  'coffee beans',  and  'brown rice'.

Under the code you added for step 2, use  .slice()  to provide your friend  with  a  list of these  three things.

Log this part of the list to the console. Unlike the two previous checkpoints,  you should  do  both of these steps in one line.

Read about  .slice()  at [MDN’s slice documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice).

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

After calling .slice()  on  groceryList,  log the grocery  list to the  console one  more time.

Notice  that the  groceryList  array  still contains the same items it  had  in Step

2.  That  means  .slice()  is  non-mutating!  You can  confirm  this in  the  link in  the  previous step.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Let’s  find the index of a particular  element in  groceryList  using  .indexOf().

Call  .indexOf()  on  groceryList  to  find the  index  of the  element  'pasta'  and  save the returned  value to a  const  variable named  pastaIndex.

Then  log pastaIndex  to the  console. (You may remove the  other console.log()  statements to declutter the  terminal.)

Read  about  .indexOf()  at  [MDN’s  indexOf documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf).

![](Images/image04697.jpeg)

Arrays  and Functions

Throughout the lesson we went over arrays being mutable, or changeable.  Well what happens if we try to change an array inside a function? Does the  array keep the change after the function call or is it scoped to inside the  function?

Take a look at the following example where we call  .push()  on an array  inside  a function.  Recall,  the  .push()  method  mutates, or changes, an array:

![](Images/image04698.jpeg)

Let’s  go over  what happened in  the example:

• The  flowers  array  that  has 3  elements.

• The  function  addFlower()  has a  parameter of  arr  uses  .push()  to add  a  'lily'  element into  arr.

• We  call  addFlower()  with  an argument  of  flowers  which  will  execute  the  code  inside  addFlower.

• We  check  the  value  of  flowers  and  it  now includes the  'lily'  element!  The  array  was mutated!

So when you pass an array into a function, if the array is mutated inside the  function, that change will be maintained outside the function as well. You  might also see this concept explained as pass-by-reference since what we’re  actually passing the function is a reference to where the variable memory is  stored  and changing  the memory.

Instructions  1.

In  main.js, there is an  array  concept. There is also a function  changeArr  that  will  assign the element in index  3  of an array to  'MUTATED'.  The

function changeArr  was called  with an argument  of  concept.

Underneath  the function  call, log  concept  to  the console to check  if this  reassignment  mutated  the array.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Let’s double check what happens if we mutate an array using a built-in  method  inside a function.

![](Images/image04699.jpeg)Under the  named

statement,  define  another  function

that  takes a  parameter of  newArr.  Inside  the function

body call  .pop()  on  newArr.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Call  removeElement()  with  an  argument  of  concept.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

After calling removeElement(concept),  check the  value of  concept  by logging  it to  console.

Notice that in both cases, the change to the array was maintained outside  of the  function!

![](Images/image04700.jpeg)

Nested  Arrays

Earlier we mentioned that arrays can store other arrays. When an array  contains another array it is known as a nested array. Examine the example  below:

const  nestedArr  =  [[1],  [2,  3]];  To access the nested arrays we can use bracket notation with the index  value,  just like we did  to access any other  element:

![](Images/image04701.jpeg)Notice  thatwill grab  the element in  index 1 which  is the

array  [2, 3]. Then, if we wanted to access the elements within the nested  array  we can  chain,  or  add  on,  more bracket  notation with index  values.

![](Images/image04702.jpeg)

In the second console.log()  statement, we have two bracket notations  chained to nestedArr. We know that  nestedArr[1]  is the array  [2, 3]. Then to  grab  the  first element  from that array,  we  use  nestedArr[1][0]  and we  get the  value of  2.

Instructions  1.

Let’s make a nested array! Create a variable  numberClusters. Assign as its  value  an  array with three array elements.

• The  first  array  element should hold  the elements  1  and  2  in  that  order.

• The  second  array  element should hold  the  elements  3  and  4  in  that  order.

• The  third  array  element should  hold  the  elements  5  and  6  in  that  order.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

![](Images/image04703.jpeg)![](Images/image04704.jpeg)Awesome,  you made  a nested array! Now  declare a  variable

![](Images/image04568.jpeg)named

using  the

keyword  and assign  to access  the

element  6  inside  numberClusters.

![](Images/image04705.jpeg)

Review  Arrays

Nice  work!  In  this lesson,  we  learned these  concepts  regarding arrays:

• Arrays  are lists  that  store  data  in JavaScript.

• Arrays  are  created  with brackets  [].

• Each  item inside  of an  array is  at a  numbered position,  or  index,  starting at  0.

• We  can access one  item in an  array  using its  index,  with syntax  like:  myArray[0].

• We can also change an item in an array using its index, with syntax  like  myArray[0]  = 'new string';

• Arrays have  a  length  property,  which allows you to see  how  many items are in  an  array.

• Arrays  have their own  methods,  including  .push()  and  .pop(), which  add and  remove  items from an array,  respectively.

• Arrays  have  many  methods that perform  different  tasks,  such

as  .slice()  and  .shift(), you  can  find  documentation at  the [Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)  [Developer  Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) website.

• Some built-in methods are mutating, meaning the method will change the  array, while others are not mutating. You can always check the  documentation.

• Variables that contain arrays can  be  declared with  let  or  const. Even  when  declared with  const, arrays are still mutable. However, a variable declared  with  const  cannot be  reassigned.

• Arrays mutated inside of a function will keep that change even outside the  function.

• Arrays  can  be nested  inside  other arrays.

• To  access  elements in  nested  arrays chain  indices using  bracket  notation.

Learning how to work with and manipulate arrays will help you work with chunks of  data!

Loops

A loop is a programming tool that repeats a set of instructions until a specified  condition, called a stopping condition is reached. As a programmer, you’ll find that  you rely on loops all the time! You’ll hear the generic term iterate when referring to  loops;  iterate simply means “to repeat”.

When we need to reuse a task in our code, we often bundle that action in a function.  Similarly, when we see that a process has to repeat multiple times in a row, we write  a loop. Loops allow us to create efficient code that automates processes to make  scalable,  manageable programs.

As illustrated in the diagram, loops iterate or repeat an action until a specific  condition is met. When the condition is met, the loop stops and the computer moves  on  to  the next part of the  program.

![](Images/image04706.jpeg)

Repeating  Tasks  Manually

Before we write our own loops let’s take a moment to develop an  appreciation for loops. The best way to do that is by showing you how  cumbersome it would be if a repeated task required you to type out the  same code  every  single time.

Instructions

1.

Create the variable  vacationSpots, and assign its value to an array of three  strings  naming places you’d like to visit.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Next, console.log()  each item  in  vacationSpots.  Since  we don’t  know loops  yet,  we  have to  console.log()  each element in the array  separately.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Nice work! Now imagine that the vacation list had 100 places on it—  logging each array element to the console by hand would be a tedious  task! In the next exercise, we will learn how to make things more efficient  with  for  loops.

![](Images/image04707.jpeg)

The  For  Loop

Instead of writing out the same code over and over, loops allow us to tell  computers to repeat a given block of code on its own. One way to give  computers these instructions is with  a  for  loop.

The  typical  for  loop includes an iterator variable  that  usually appears in all  three expressions. The iterator variable is initialized, checked against the  stopping  condition,  and  assigned a new  value on each  loop iteration.

Iterator variables can have any name, but it’s best practice to use a  descriptive  variable name.

A  for  loop contains three expressions  separated by  ;  inside the parentheses:

1. an initialization starts the loop and can also be used to declare the  iterator  variable.

2. a stopping condition is the condition that the iterator variable is  evaluated  against— if the condition evaluates to  true  the  code block  will  run, and if it evaluates to  false  the code will  stop.

3. an iteration statement is used to update the iterator variable on each  loop.

The  for  loop syntax  looks  like this:

![](Images/image04708.jpeg)

In  this example, the  output would  be the  following:

![](Images/image04709.jpeg)

Let’s  break down  the example:

• The  initialization is  let  counter  =  0, so the  loop  will  start counting  at  0.

• The stopping condition is  counter < 4, meaning the loop will run as  long  as the  iterator  variable,  counter, is less than 4.

• The iteration statement is  counter++. This means after each loop, the  value of  counter  will increase by 1\. For the first iteration  counter  will  equal  0,  for the  second iteration  counter  will equal  1,  and so on.

• The code block is inside of the curly braces,  console.log(counter), will  execute until the condition evaluates to  false. The condition will be  false  when  counter  is greater than  or equal to  4 — the point that the  condition  becomes false is sometimes  called  the stop condition.

This for  loop makes it possible to write  0,  1,  2, and  3  programmatically.  Instructions 1.

Now, make your own! Create a program that loops from 5 to 10 and logs  each  number to the  console.

![](Images/image04710.jpeg)

![](Images/image04711.jpeg)

Looping  in  Reverse

What if we want the  for  loop to log  3,  2,  1, and then  0? With simple  modifications  to  the  expressions,  we  can  make  our  loop  run  backward!

To  run a  backward  for  loop, we must:

• Set the iterator variable to the highest desired value in the  initialization  expression.

• Set the stopping condition for when the iterator variable is less than  the  desired  amount.

• The  iterator  should decrease  in  intervals  after  each iteration.

Instructions  1.

Make a for  loop that loops backwards printing  3  to  0  to the console. Use  the  >=  comparison  operator in  your  stopping  condition and  the  --  operator  in  your  iteration statement.

![](Images/image04712.jpeg)

Looping  through  Arrays

for  loops are very handy for iterating over data structures. For example, we  can use a  for  loop to perform the same operation on each element on an  array. Arrays hold lists of data, like customer names or product information.  Imagine  we owned a store  and wanted to  increase  the price of every

product in our catalog. That could be a lot of repeating code, but by using  a  for  loop to iterate through the  array we could  accomplish  this task easily.

To  loop  through each  element in  an array, a  for  loop  should use  the  array’s  .length  property in its condition.

Check out the example below to see how  for  loops  iterate on arrays:

![](Images/image04713.jpeg)

This  example would give you  the  following output:

![](Images/image04714.jpeg)

In the loop above, we’ve named our iterator variable  i. This is a variable  naming convention you’ll see in a lot of loops. When we use  i  to iterate  through arrays we can think of it as being short-hand for the word index.  Notice how our stopping condition checks that  i  is less than  animals.length.  Remember that arrays are zero-indexed, the index of the last element of an  array is equivalent to the length of that array minus 1\. If we tried to access  an  element at  the index of  animals.length  we will have gone too  far!

With  for  loops,  it’s  easier  for  us  to  work  with  elements  in  arrays.  Instructions 1.

Write  a for  loop that iterates through  our  vacationSpots  array using  i  as the  iterator  variable.

Inside the block of the  for  loop, use  console.log()  to log each element in  the  vacationSpots  array  after the string  'I  would  love to  visit '. For example,  the first round of the loop should print  'I would love to visit Bali'  to the  console.

![](Images/image04715.jpeg)

![](Images/image04716.jpeg)

Nested  Loops

When we have a loop running inside another loop, we call that a nested loop.  One use for a nested  for  loop is to compare the elements in two arrays. For  each round of the outer  for  loop, the inner  for  loop will run completely.

Let’s look at  an  example of a nested  for  loop:

![](Images/image04717.jpeg)

Let’s  think about what’s  happening in the nested  loop in our  example. For

each element in the outer loop array,  myArray, the inner loop will run in its  entirety comparing the current element from the outer array,  myArray[i], to  each element in the inner array,  yourArray[j]. When it finds a match, it prints  a string  to the  console.

Now  it’s your  turn to write  a  nested loop!

Instructions  1.

Imagine  you’re  a  big-wig  programmer  for  a  social  media  platform!  You  have been tasked with building a prototype for a mutual followers program.  You’ll need two arrays of “friends” from two mock users so that you can  extract  the names of  the followers who  exist in both  lists. Make  a  variable

called  bobsFollowers  and  set  it  equal  to  an  array  with  four strings  representing  the names of Bob’s friends.

 Checkpoint 2 Passed

2.

Make a variable called  tinasFollowers  and set it equal to an array with three  strings representing the names of Tina’s friends. Make exactly two of these  the  same as two  of the friends in the  bobsFollowers  array.

 Checkpoint 3 Passed

3.

Create a third  variable named  mutualFollowers  and set it to an empty  array.

 Checkpoint 4 Passed

4.

Create  a  nested  loop that iterates  through  bobsFollowers  as the array  for the  outer loop and  tinasFollowers  as the array for the inner loop. If the current  element from the outer loop is the same as the current element from the  inner  loop, push that element into  the  mutualFollowers  array.

![](Images/image04718.jpeg)

The  While Loop

You’re doing great! We’re going to teach you about a different type of  loop: the  while  loop. To start, let’s convert a  for  loop into  a  while  loop:

![](Images/image04719.jpeg)

![](Images/image04720.jpeg)Let’s  break down  what’s  happening with ourloop syntax:

![](Images/image04721.jpeg)• The  inside  our

variable is declared before the loop. We can access it  loop  since it’s in the global scope.

• We start our loop with the keyword  while  followed by our stopping  condition, or test condition. This will be evaluated before each round  of the loop. While the condition evaluates to  true, the block will  continue to run. Once it  evaluates to  false  the  loop will stop.

• Next,  we  have our loop’s code block  which prints  counterTwo  to the  console  and increments  counterTwo.

What  would  happen  if we didn’t increment  counterTwo  inside our  block? If we  didn’t include this,  counterTwo  would always have its initial value,  1. That  would mean the testing condition  counterTwo < 4  would always  evaluate

to true  and our loop would never stop running! This is called an infinite  loop and it’s something we always want to avoid. Infinite loops can take up  all of your computer’s processing power potentially freezing your  computer.

So  you may be  wondering  when to  use a  while  loop! The syntax of

a  for  loop  is  ideal  when we  know how many times the loop  should run, but  we don’t always know this in advance. Think of eating like a  while  loop:  when you start taking bites, you don’t know the exact number you’ll need  to become full. Rather you’ll eat  while  you’re hungry. In situations when we  want a loop to execute an undetermined number of times,  while  loops are  the  best choice.

Instructions  1.

Below  the cards  array, declare  a variable,  currentCard,  with the  let  keyword  but  don’t assign  it  a value.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Create  a  while  loop with  a  condition that checks  if the  currentCard  does not  have  that value  'spade'.

Inside the block of your  while  loop, add the  following  line of  code:

currentCard  =  cards[Math.floor(Math.random()  *  4)];  Math.floor(Math.random() * 4)  will give us a random number from  0  to  3. We’ll  use  this number to index  the  cards  array,  and assign  the value

of  currentCard  to a random  element  from  that array.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Awesome! Your loop is running, but you can’t tell because it doesn’t output  anything. Let’s add a  console.log()  statement to our  while  block. Inside the  block, after you assign  currentCard  a new value, log  currentCard  to the  console.

For fun you can run your code a few times and see how the output  changes!

![](Images/image04722.jpeg)

Do...While  Statements

In some cases, you want a piece of code to run at least once and then loop  based  on a  specific condition after  its initial run. This is where

the  do...while  statement  comes  in.

A  do...while  statement says to do a  task once and then keep doing it until a  specified condition is no longer met. The syntax for a  do...while  statement  looks  like this:

![](Images/image04723.jpeg)

In  this  example,  the code block makes changes to the  countString  variable by  appending the string form of the  i  variable to it. First, the code block after  the do  keyword is executed once. Then the condition is evaluated. If the  condition evaluates to  true, the block will execute again. The looping stops  when  the condition evaluates to  false.

Note  that the  while  and  do...while  loop are different! Unlike

the  while  loop,  do...while  will run  at  least once  whether or not  the condition  evaluates  to  true.

![](Images/image04724.jpeg)

1.

We’d like a program to simulate part of the cake-baking process.  Depending on the recipe, a different number of cups of sugar is required.  Create the variable  cupsOfSugarNeeded, and assign it a number value of your  choosing.  The  cups of  sugar must be added  to the batter  one  at a time.

Declare the variable  cupsAdded  and assign it  the value  0.

 Checkpoint 2 Passed

2.

We have a sweet tooth, so we want to add at least one cup of sugar to the  batter even if the value of  cupsOfSugarNeeded  is  0. Create a  do...while  loop  which  increments  cupsAdded  by one  while  cupsAdded  is less

than  cupsOfSugarNeeded.

![](Images/image04725.jpeg)

The  break  Keyword

Imagine we’re looking to adopt a dog. We plan to go to the shelter every  day for a year and then give up. But what if we meet our dream dog on day  65? We don’t want to keep going to the shelter for the next 300 days just  because our original plan was to go for a whole year. In our code, when we  want to stop a loop from continuing to execute even though the original  stopping condition we wrote for our loop hasn’t been met, we can use the  keyword  break.

The  break  keyword  allows programs  to “break”  out of the loop from  within  the loop’s block.

Let’s check out the syntax  of  a  break  keyword:

![](Images/image04726.jpeg)

![](Images/image04727.jpeg)

This  is the  output for  the above  code:

![](Images/image04728.jpeg)statements can be especially helpful when we’re looping through  large data structures! With breaks, we can add test conditions besides the  stopping  condition,  and exit the loop when  they’re met.

![](Images/image04729.jpeg)

1.

Log  each element from

![](Images/image04730.jpeg)in  a

![](Images/image04731.jpeg)loop  with  the iterator  variable  i.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

![](Images/image04732.jpeg)After the  for  loop, log  the stringto the

console. Note: since there’s a single quote character,  ', in our string, we can  use  double quotes  around the string  to make sure  character prints.

 Checkpoint 3 Passed

3.

Add  a break  inside your  loop’s block that breaks out of the  loop  if the  element at the current index in the  rapperArray  is  'Notorious  B.I.G.'.

![](Images/image04733.jpeg)

![](Images/image04734.jpeg)

Review

Great job! In this lesson, we learned how to write cleaner code with loops. You now  know:

![](Images/image04735.jpeg)• Loops perform repetitive actions so we don’t have to code that process  manually  every time.

• How  to  write

• How  to  use  a

loops with an iterator variable that increments or decrements  loop  to iterate through an array

• A  nested  for  loop is  a loop  inside another  loop

• while  loops allow for different types of stopping  conditions

• Stopping  conditions are  crucial for  avoiding  infinite  loops.

• do...while  loops  run code at least once—  only checking the stopping  condition  after the  first  execution

• The  break  keyword  allows programs to leave a loop during the execution  of its  block

Introduction

We are often unaware of the number of assumptions we make when we  communicate with other people in our native languages. If we told you to “count to  three,” we would expect you to say or think the numbers one, two and three. We  assumed you would know to start with “one” and end with “three”. With  programming, we’re faced with needing to be more explicit with our directions to the  computer.  Here’s how  we might tell the computer to  “count to three”:

![](Images/image04736.jpeg)

When we speak to other humans, we share a vocabulary that gives us quick ways to  communicate complicated concepts. When we say “bake”, it calls to mind a familiar  subroutine—  preheating  an  oven,  putting  something  into  an  oven  for  a  set  amount  of time, and finally removing it. This allows us to abstract away a lot of the details and  communicate key concepts more concisely. Instead of listing all those details, we can  say,  “We baked a cake,” and still impart all  that  meaning  to you.

In programming, we can accomplish “abstraction” by writing functions. In addition to  allowing us to reuse our code, functions help to make clear, readable programs. If  you encountered countToThree()  in a program, you might be able to quickly guess  what  the function  did without having to  stop and read  the function’s body.

We’re also going to learn about another way to add a level of abstraction to our  programming: higher-order functions. Higher-order functions are functions that  accept other functions as arguments and/or return functions as output. This enables  us to build abstractions on other abstractions, just like “We hosted a birthday party”  is  an abstraction that  may  build  on the abstraction “We  made a  cake.”

In summary, using more abstraction in our code allows us to write more modular  code  which is easier  to read and debug.

Functions  as Data

JavaScript functions behave like any other data type in the language; we  can assign functions to variables, and we can reassign them to new  variables.

Below, we have an annoyingly long function name that hurts the readability  of any code in which it’s used. Let’s pretend this function does important  work  and needs to  be called repeatedly!

![](Images/image04737.jpeg)

What  if  we wanted  to rename  this function  without  sacrificing  the source

code? We can re-assign the function to a variable with a suitably short  name:

![](Images/image04738.jpeg)is a variable that holds a reference to our original function. If we could  look  up the  address in memory of  busy  and  the address in memory

of announceThatIAmDoingImportantWork  they would point to the same place. Our  new busy()  function can be invoked with parentheses as if that was the  name we  originally  gave our  function.

Notice how we assign  announceThatIAmDoingImportantWork  without parentheses  as  the  value to  the  busy  variable. We want  to assign the value of the function  itself,  not the value it returns when invoked.

In JavaScript, functions are first class objects. This means that, like other  objects you’ve encountered, JavaScript functions can have properties and  methods.

Since  functions are  a type  of object,  they have  properties such

as  .length  and  .name  and methods such as  .toString().  You can  see more  about  the  methods and  properties of  functions [in  the documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function).

Functions are special because we can invoke them, but we can still treat  them  like any other  type of  data.  Let’s  get some practice doing  that!

Instructions  1.

We’ve  defined a  function with  a very long

name:  checkThatTwoPlusTwoEqualsFourAMillionTimes. This function takes a long  time to execute. It checks whether 2 + 2 = 4, but it does it a million times  (just to be really sure)! Create a shorter-named variable,  is2p2  that will be  easier  to  work  with,  and assign  checkThatTwoPlusTwoEqualsFourAMillionTimes  as  its  value.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Invoke  your

![](Images/image04739.jpeg)function

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

![](Images/image04740.jpeg)Hmmm,  if we  forgot  the  original name  of  our function,  is there  a way  we

could  figure it out? Useto  console.log()  the  name  property  of  the

function we assigned to  is2p2. Check out [the documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function) if you need a  hint.

![](Images/image04741.jpeg)

Functions  as Parameters

Since functions can behave like any other type of data in JavaScript, it  might not surprise you to learn that we can also pass functions (into other  functions) as parameters. A higher-order function is a function that either  accepts functions as parameters, returns a function, or both! We call the  functions  that  get passed in as parameters and invoked  callback

functions because they get called during the execution of the higher-order  function.

When we pass a function in as an argument to another function, we don’t  invoke it. Invoking the function would evaluate to the return value of that  function call. With callbacks, we pass in the function itself by typing the  function name without the parentheses (that would evaluate to the result of  calling  the function):

![](Images/image04742.jpeg)

We  wrote  a higher-order  function,  timeFuncRuntime().  It takes  in a  function as

an argument, saves a starting time, invokes the callback function, records  the time after the function was called, and returns the time the function  took  to  run by subtracting the starting  time from the  ending time.

This higher-order function could be used with any callback function which  makes  it  a potentially powerful piece of  code.

We  then  invoked  timeFuncRuntime()  first  with the  addOneToOne()  function -  note  how we passed in  addOneToOne  and  did not invoke it.

![](Images/image04743.jpeg)

In  this  example,  we invoked  timeFuncRuntime()  with  an  anonymous function  that counts backwards from 10\. Anonymous functions can be arguments  too!

Let’s get some practice using functions and writing higher-order functions.  Instructions 1.

Save a variable,  time2p2. Assign as its value the result of invoking  the  timeFuncRuntime()  function with

the  checkThatTwoPlusTwoEqualsFourAMillionTimes()  function.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Write a higher-order function,  checkConsistentOutput(). This function should  have two parameters: a function and a value. It should call the argument  function with the value two times. If the callback function produces the  same result twice, it should return the result of the function call, otherwise,  it  should return  the string  'This  function  returned  inconsistent  results'

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Invoke  your checkConsistentOutput()  with the  addTwo()  function we wrote and a  number  as arguments.

![](Images/image04744.jpeg)

![](Images/image04745.jpeg)

Review

Great job! By thinking about functions as data and learning about higher-order functions,  you’ve taken important steps in being able to write clean, modular code and take advantage  of  JavaScript’s flexibility.

Let’s  review what  we learned in  this lesson:

• Abstraction allows us to write complicated code in a way that’s easy to reuse, debug,  and understand  for  human readers

• We can work with functions the same way we would any other type of data including  reassigning  them to new variables

• JavaScript functions are first-class objects, so they have properties and methods like  any object

• Functions  can be  passed into  other functions  as parameters

• A higher-order function is a function that either accepts functions as parameters,  returns  a function, or both

Introduction  to  Iterators

Imagine you had a grocery list and you wanted to know what each item on  the  list was.  You’d have to  scan through  each row and  check for the  item.

This common task is similar to what we have to do when we want to iterate  over, or loop through,  an array. One tool at our  disposal is the  for  loop.

However, we also have access to built-in array methods which make  looping easier.

The built-in JavaScript array methods that help us iterate are called iteration  methods, at times referred to as iterators. Iterators are methods called on  arrays  to manipulate elements and  return values.

In this lesson, you will learn the syntax for these methods, their return  values, how to use the documentation to understand them, and how to  choose  the right iterator method for a given task.

Instructions

Inspect the code in main.js. Notice the different methods being called on  the  arrays:

• .forEach()

• .map()

• .filter()

Run  the code to  see the output!

![](Images/image04746.jpeg)

![](Images/image04747.jpeg)

The  .forEach()  Method

The first iteration method that we’re going to learn is  .forEach(). Aptly  named, .forEach()  will execute the same code for  each element of an array.

The code above will log a nicely formatted list of the groceries to the  console.  Let’s explore the syntax  of invoking  .forEach().

• groceries.forEach()  calls  the  forEach  method  on  the  groceries  array.

• .forEach()  takes an argument of callback function. Remember, a  callback function is a function passed as an argument into another  function.

• .forEach()  loops through  the array  and  executes the  callback function  for each element. During each execution, the current element is  passed  as an argument to the callback function.

• The  return value for  .forEach()  will always  be  undefined.

Another way  to pass a  callback for  .forEach()  is  to use arrow  function  syntax.

groceries.forEach(groceryItem => console.log(groceryItem));  We can also define a function beforehand to be used as the callback  function.

![](Images/image04748.jpeg)

![](Images/image04749.jpeg)

The  above example  uses a  function  declaration but you  can also use  a

function  expression  or  arrow  function  as well.

All three code snippets do the same thing. In each array iteration method,  we can use any of the three examples to supply a callback function as an  argument to the iterator. It’s good to be aware of the different ways to pass  in callback functions as arguments in iterators because developers have  different stylistic preferences. Nonetheless, due to the strong adoption of  ES6,  we  will be using  arrow function syntax  in the later  exercises.

Instructions  1.

Iterate  over the  fruits  array to log  I want to eat a  plus the  name  of each fruit  to  the  console.  For example,  I  want  to eat a  mango.

You  may  use  any form  of callback  you prefer.

![](Images/image04750.jpeg)

The  .map() Method

The  second iterator  we’re going to  cover  is  .map().  When  .map()  is called on  an array, it takes an argument of a callback function and returns a new  array!  Take a  look at an example of  calling  .map():

![](Images/image04751.jpeg)

![](Images/image04752.jpeg)works in a similar manner to  .forEach()— the major difference is  that .map()  returns a  new array.

In  the  example  above:

• numbers  is  an  array of numbers.

• bigNumbers  will store the return value of  calling  .map()  on  numbers.

• numbers.map  will iterate  through each  element in  the  numbers  array  and  pass  the element into the  callback function.

• return  number  *  10  is  the  code  we  wish  to  execute  upon  each  element  in  the  array.  This will save each value from  the  numbers  array, multiplied  by  10, to a  new array.

If  we  take  a look  at  numbers  and  bigNumbers:

![](Images/image04753.jpeg)

Notice  that the elements in  numbers  were not altered and  bigNumbers  is  a new  array.

Instructions  1.

Add  your  code  under  the  animals  array and before  the  line  console.log(secretMessage.join(''));

Use  .map()  to create a new array that  contains the  first  character of each  string  in the  animals  array.  Save the new  array to a  const  variable

named  secretMessage.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Use  .map()  to divide all the  numbers in  bigNumbers  by  100. Save the returned  values to a variable declared with  const  called  smallNumbers.

![](Images/image04754.jpeg)

The  .filter()  Method

Another useful iterator method is  .filter(). Like  .map(),  .filter()  returns a  new array.  However,  .filter()  returns  an  array  of  elements  after filtering  out  certain  elements from the original  array.  The callback function for

the  .filter()  method  should  return  true  or  false  depending  on the  element  that  is  passed  to  it.  The  elements  that  cause  the  callback  function  to  return true  are added to the new array. Take a look at the following  example:

![](Images/image04755.jpeg)

• ![](Images/image04756.jpeg)words  is an array that contains string elements.

• const  shortWords  =  declares a  new variable  that  will store  the returned  array  from invoking  .filter().

• The  callback function is an  arrow  function has a  single

parameter,  word.  Each element in the  words  array will be passed  to this  function  as an argument.

• ![](Images/image04757.jpeg)is  the  condition  in  the callback function.  Any  word  from  the  words  array that has  fewer than  6  characters will  be  added to

the shortWords  array.

Let’s also check the values of  words  and  shortWords:

![](Images/image04758.jpeg)

Observe how  words  was not  mutated, i.e.  changed,  and  shortWords  is a new  array.

Instructions  1.

Call the .filter()  method on  randomNumbers  to return values that are less  than  250.  Save  them  to  a  new array  called  smallNumbers,  declared  with  const.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Now  let’s work with  an array of  strings. Invoke  .filter()  on

the  favoriteWords  array to  return elements that  have more than 7  characters.  Save  the  returned array  to a  const  variable named  longFavoriteWords.

![](Images/image04759.jpeg)

![](Images/image04760.jpeg)

The  .findIndex()  Method

We sometimes want to find the location of an element in an array. That’s  where  the  .findIndex()  method  comes  in!  Calling  .findIndex()  on  an  array  will  return the index of the first element that evaluates to  true  in the callback  function.

![](Images/image04761.jpeg)

• jumbledNums  is an  array that  contains elements  that are numbers.

• const  lessThanTen =  declares a new  variable that  stores the  returned  index  number  from invoking  .findIndex().

• The  callback function is  an arrow  function  has a single parameter,  num.

Each element in the  jumbledNums  array  will be  passed  to this function  as  an  argument.

• num <  10;  is the condition  that elements are checked

against. .findIndex()  will return the index of  the first element which  evaluates to  true  for that  condition.

Let’s  take a look  at what  lessThanTen  evaluates to:

console.log(lessThanTen);  //  Output:  3

If  we check  what  element has  index of 3:

console.log(jumbledNums[3]);  //  Output:  5

Great,  the  element in index  3  is the number  5.  This makes sense  since  5  is  the  first element that is less than 10.

If there isn’t a single element in the array that satisfies the condition in the  callback, then  .findIndex()  will return  -1.

![](Images/image04762.jpeg)

![](Images/image04763.jpeg)

1.

Invoke

![](Images/image04764.jpeg)on the  animals  array  to find the index of the element that

has  the  value  'elephant'  and  save the  returned  value  to a  const  variable  named  foundAnimal.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Let’s see if we can find the index of the first animal that starts with the  letter  's'.

Call  .findIndex()  on the  animals  array  return  the index  of the  first  element  that starts with  's'. Assign the returned value to a  const  variable

named  startsWithS.

![](Images/image04765.jpeg)

The  .reduce()  Method

Another widely  used  iteration  method  is  .reduce().  The  .reduce()  method  returns a single value after iterating through the elements of an array,  thereby  reducing  the  array. Take a  look at the  example below:

![](Images/image04766.jpeg)

![](Images/image04767.jpeg)![](Images/image04768.jpeg)Here are the values of  the  numbers  array:

Iteration  accumulator  currentValue

and

return  value

as  we  iterate  through

| First | 1 | 2 | 3 |
| Second | 3 | 4 | 7 |
| Third | 7 | 10 | 17 |

Now  let’s go over the  use of  .reduce()  from the  example above:

• numbers  is an array that contains numbers.

• summedNums  is  a variable  that stores  the returned value  of  invoking  .reduce()  on  numbers.

• numbers.reduce()  calls  the  .reduce()  method  on  the  numbers  array  and  takes  in a callback function as argument.

• The  callback  function has  two

parameters,  accumulator  and  currentValue.  The  value

of  accumulator  starts off as the  value of  the first element  in the array  and the currentValue  starts as the second element. To see the value  of  accumulator  and  currentValue  change, review  the chart  above.

• As  .reduce()  iterates through the array, the return value of the  callback function becomes the  accumulator  value for the next  iteration,  currentValue  takes on the value of the  current element in  the looping  process.

The  .reduce()  method can  also take an  optional second parameter to  set an  initial value for  accumulator  (remember, the first argument is the callback  function!).  For  instance:

![](Images/image04769.jpeg)

![](Images/image04770.jpeg)

Here’s  an  updated  chart that accounts  for the second  argument of  100:

Iteration  #

accumulator  currentValuereturn

value

| First | 100 | 1 | 101 |
| Second | 101 | 2 | 103 |
| Third | 103 | 4 | 107 |
| Fourth | 107 | 10 | 117 |

Instructions

1.

Let’s  practice  calling  .reduce()  and using  console.log()  to  check the  values  as  .reduce()  iterates through the  array.

In  main.js, there  is an  array  of numbers,  newNumbers.

To start, declare a new variable named  newSum  using the  const  keyword.  Assign  to  newSum  the value  of calling  .reduce()  on  newNumbers.  You don’t  need  to  provide any arguments to  .reduce()  yet.

You’ll also see a  TypeError: undefined is  not a  function  but  we’ll fix that  after  we add our callback function in the  next step!

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Provide .reduce  with an argument of a callback function. The callback  function has two parameters. The first parameter is  accumulator  and the  second parameter is  currentValue. Use either a function expression or an  arrow  function.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

To check the value being used as we iterate through the array, add three  statements  to the  function body of the callback:

• console.log('The  value  of  accumulator:  ',  accumulator);

• console.log('The  value  of  currentValue:  ',  currentValue);

• a return statement that  adds  accumulator  to  currentValue.

 Checkpoint 4 Passed

Stuck?  Get a hint

![](Images/image04771.jpeg)4.

Log  the value of

to  the console to see the  return value  of

callingon  newNumbers.

 Checkpoint 5 Passed

5.

While we have this code set up, let’s also check what happens if you add a  second argument to  .reduce(). The second argument acts as an initial value  for  the  accumulator.

Add  a  second  argument  of  10  to  .reduce().

![](Images/image04772.jpeg)

Iterator  Documentation

There are many additional built-in array methods, a complete list of which  is  on the  [MDN’s Array  iteration methods page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Iteration_methods).

The  documentation  for  each  method  contains  several  sections:

1. A  short definition.

2. A  block with the  correct  syntax for  using  the  method.

3. A  list  of  parameters the  method  accepts or  requires.

4. The  return value  of the function.

5. An  extended  description.

6. Examples  of the method’s  use.

7. Other  additional information.

In the instructions below, there are some errors in the code. Use the  documentation for a given method to determine the error or fill in a blank  to  make the  code run  correctly.

![](Images/image04773.jpeg)

1.

In the code editor, there is an array called  words. We want to create a new  array of interesting words. The first thing we want to do is check if there are  words that are fewer than  6  characters long. There is something missing in  the words.some()  method call. Fix this method so that  true  is printed to the  console.

For  more  information browse  [MDN’s documentation  on  .some()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some).

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

The .some()  method returned  true, which means there are some words in  the  array that are shorter than six characters. Use the  .filter()  method to  save  any words longer  than  5  characters to a new variable

called  interestingWords,  declared  with  const.

We’ve  used  .filter()  in a previous exercise, but, for  more information  browse  [MDN’s documentation on  .filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter).

 Checkpoint 3 Passed

3.

In  the last line  of main.js, there is  this code:

![](Images/image04774.jpeg)

Complete the code between the parentheses to check if every element has  more  than 5 characters.

Make  sure to  uncomment (delete the  //  before)  the last line of the program  before  you run  the code.

For  more  information browse  [MDN’s documentation  on  .every()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every).

![](Images/image04775.jpeg)

![](Images/image04776.jpeg)

Choose  the Right Iterator

There are many iteration methods you can choose. In addition to learning  the correct syntax for the use of iteration methods, it is also important to  learn how to choose the correct method for different scenarios. The  exercises  below will give you  the opportunity  to do  just that!

You’ll see errors pop up in the terminal as you work through this exercise,  but  by the end the errors will be gone!

![](Images/image04777.jpeg)

1.

Replace  the word  method  in the first method call  with a method that  will do  something  to each  of the  values in the  array  and return  undefined.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

In  the  second method call, replace  the word  method  with a  method that will  return  a  new array with only those elements longer than  7  characters.

 Checkpoint 3 Passed

3.

In  the  third method call, replace  the  word  method  with a method that take an  array  that contains multiple values and returns  a single value.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

In  the  fourth  method call,  replace  the word  method  with a  method  that  will  return  a new array  of numbers returned from  the function.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

In  the  fifth method call, replace the word  method  with a method that will  return  a boolean value.

![](Images/image04778.jpeg)

Review

Awesome job on clearing the iterators lesson! You have learned a number of useful  methods in this lesson as well as how to use the JavaScript documentation from the  Mozilla Developer Network to discover and understand additional methods. Let’s  review!

• .forEach()  is  used to execute the same code on  every element in an  array but  does  not change the array and returns  undefined.

• .map()  executes  the  same code  on every element in  an array and returns  a new  array  with the updated elements.

• .filter()  checks every  element in an  array  to see  if it meets certain criteria  and  returns  a new  array with the  elements that return  truthy for  the  criteria.

• .findIndex()  returns the index  of the first  element of an  array  which satisfies  a  condition in the callback function. It returns  -1  if none of the elements in the  array  satisfies the condition.

• .reduce()  iterates  through an  array and takes  the values  of the elements  and  returns  a single value.

• All iterator methods takes a callback function that can be pre-defined, or a  function  expression,  or an arrow  function.

• You can visit the  [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) to learn more about iterator  methods  (and  all other parts of JavaScript!).

Introduction  to  Objects

It’s time to learn more about the basic structure that permeates nearly every aspect  of  JavaScript programming: objects.

You’re probably already more comfortable with objects than you think, because  JavaScript loves objects! Many components of the language are actually objects  under the hood, and even the parts that aren’t— like strings or numbers— can still  act  like objects in some instances.

There are only seven fundamental data types in JavaScript, and six of those are the  primitive data types: string, number, boolean, null, undefined, and symbol. With the  seventh type, objects, we open our code to more complex possibilities. We can use  JavaScript objects to model real-world things, like a basketball, or we can use objects  to  build the  data structures that  make  the web possible.

At their core, JavaScript objects are containers storing related data and functionality,  but that deceptively simple task is extremely powerful in practice. You’ve been using  the power of objects all along, but now it’s time to understand the mechanics of  objects  and  start making your  own!

Creating  Object  Literals

Objects can be assigned to variables just like any JavaScript type. We use  curly  braces,  {}, to designate an object literal:

let  spaceship  = {};  //  spaceship  is an  empty object  We fill an object with unordered data. This data is organized into key-value  pairs. A key is like a variable name that points to a location in memory that  holds a value.

A key’s value can be of any data type in the language including functions or  other  objects.

We make a key-value pair by writing the key’s name, or identifier, followed  by a colon and then the value. We separate each key-value pair in an object  literal with a comma (,). Keys are strings, but when we have a key that does  not have any special characters in it, JavaScript allows us to omit the  quotation  marks:

![](Images/image04779.jpeg)and  color.  'Fuel  Type'  has  quotation  marks because it contains a  space  character.

Let’s  make some objects!

Instructions  1.

The  spaceship  we have so  far looks good  but,  unfortunately,  is not very fast  at hyperspace travel due to having an inferior fuel source. Make a new  spaceship object named  fasterShip  with the same  color  as  spaceship  but  with a  Fuel  Type  equal to  'Turbo Fuel'.

![](Images/image04780.jpeg)

Accessing  Properties

There are two ways we can access an object’s property. Let’s explore the  first  way— dot notation,  ..

You’ve used dot notation to access the properties and methods of built-in  objects and  data instances:

'hello'.length;  //  Returns  5  With property dot notation, we write the object’s name, followed by the dot  operator  and then the property name (key):

![](Images/image04781.jpeg)

![](Images/image04782.jpeg)

If we try to access a property that does not exist on that  object, undefined  will be  returned.

spaceship.favoriteIcecream;  //  Returns  undefined

Let’s  get  some more practice  using dot  notation on  an object!

Instructions  1.

Let’s  use the dot operator  to access the value of  numCrew  from

the  spaceship  object in  the code  editor. Create a  variable  crewCount  and  assign  the  spaceship‘s  numCrew  property to  it.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Again  using  the dot operator,  create a  variable  planetArray  and assign  the  spaceship‘s  flightPath  property to it.

![](Images/image04783.jpeg)

Bracket  Notation

The second way to access a key’s value is by using bracket notation,  [ ].  You’ve  used  bracket notation when indexing an array:

['A',  'B',  'C'][0];  //  Returns  'A'

To use bracket notation to access an object’s property, we pass in the  property  name (key) as a string.

We must use bracket notation when accessing keys that have numbers,  spaces, or special characters in them. Without bracket notation in these  situations,  our  code would throw  an error.

![](Images/image04784.jpeg)

With bracket notation you can also use a variable inside the brackets to  select the keys of an object. This can be especially helpful when working  with  functions:

![](Images/image04785.jpeg)

If  we  tried  to write our  returnAnyProp()  function with  dot  notation

(objectName.propName)  the  computer  would  look  for  a key  of  'propName'  on  our object and not the value of  the  propName  parameter.

Let’s get some practice using bracket notation to access properties!  Instructions 1.

![](Images/image04786.jpeg)![](Images/image04787.jpeg)Let’s  use bracket notation  to access the  value offrom

the

object  in  the code  editor. Create  a  variable

and

assign  the  spaceship‘s  'Active  Mission'  property to  it.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Using  bracket  notation and  the  propName  variable

provided,  console.log()  the value of the  'Active Mission'  property.

![](Images/image04788.jpeg)

Property  Assignment

Once we’ve defined an object, we’re not stuck with all the properties we  wrote. Objects are mutable meaning we can update them after we create  them!

We can use either dot notation,  ., or bracket notation,  [], and the  assignment operator,  =  to  add new  key-value  pairs to an object  or  change  an  existing property.

One  of  two  things can  happen with  property assignment:

• If the property already exists on the object, whatever value it held  before  will be replaced with the  newly assigned  value.

• If there was no property with that name, a new property will be  added  to the object.

It’s important to know that although we can’t reassign an object declared  with  const, we can still mutate it, meaning we can add new properties and  change  the properties that are there.

![](Images/image04789.jpeg)

You  can delete a  property from an object  with the  delete  operator.

![](Images/image04790.jpeg)

1.

Reassign the  color  property of  the  spaceship  object to have  a value  of  'glorious gold'

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Without  changing  lines  1 - 6,  add a  numEngines  property with  a  numeric  value between 1 and 10 to the  spaceship  object.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

![](Images/image04791.jpeg)Use  theoperator to remove  the  'Secret  Mission'  property  from

the  spaceship  object.

![](Images/image04792.jpeg)

Methods

When the data stored on an object is a function we call that a method. A  property  is what an  object has,  while a  method is what  an object does.

Do object methods seem familiar? That’s because you’ve been using them  all along! For example  console  is a global javascript object and  .log()  is a  method  on  that  object.  Math  is also  a global javascript object and  .floor()  is  a  method on it.

We can include methods in our object literals by creating ordinary, comma-  separated key-value pairs. The key serves as our method’s name, while the  value  is an anonymous function expression.

![](Images/image04793.jpeg)

![](Images/image04794.jpeg)

With  the new  method syntax introduced  in ES6  we can omit  the colon  and

the  function  keyword.

![](Images/image04795.jpeg)

Object methods are invoked by appending the object’s name with the dot  operator  followed by the method  name and parentheses:

![](Images/image04796.jpeg)

1.

Below  the retreatMessage  variable  in the code  editor, create

an  alienShip  object. It  should contain a  method  .retreat()  which  will  console.log()  the  retreatMessage.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Add another method to your object literal. This method,  .takeOff(),  should  console.log()  the  string  'Spim...  Borp...  Glix...  Blastoff!'.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Invoke your  two methods: first  .retreat()  then  .takeOff().

![](Images/image04797.jpeg)

![](Images/image04798.jpeg)

Nested  Objects

In application code, objects are often nested— an object might have  another object as a property which in turn could have a property that’s an  array  of  even more objects!

In our spaceship  object, we want a  crew  object. This will contain all the crew  members  who do important work on  the craft. Each of those  crew  members  are objects themselves. They have properties like  name, and  degree, and they  each have unique methods based on their roles. We can also nest other  objects in the  spaceship  such as a  telescope  or nest details about the  spaceship’s computers inside  a parent  nanoelectronics  object.

![](Images/image04799.jpeg)

![](Images/image04800.jpeg)

We  can  chain operators  to access nested  properties. We’ll have  to  pay

attention to which operator makes sense to use in each layer. It can be  helpful to pretend you are the computer and evaluate each expression from  left  to right  so that  each operation  starts to  feel a  little more manageable.

![](Images/image04801.jpeg)

In  the preceding  code:

• First the computer evaluates  spaceship.nanoelectronics, which results  in  an object  containing the  back-up  and  computer  objects.

• We  accessed the  back-up  object  by  appending  ['back-up'].

• The  back-up  object has  a  battery  property, accessed

with .battery  which  returned  the value stored there:  'Lithium'

Instructions  1.

Create  a  variable capFave  and assign the  captain‘s  favorite food  (the  element  in the 0th index of her  'favorite foods'  array) to it. Make sure to use  bracket and  dot notation  to  get the value  of the  food through nested  access  (don’t  just copy the value into  the variable!)

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Right  now the  passengers  property has a  value of  null. Instead, assign as its  value  an  array  of objects. These  objects should  represent the  spaceship‘s

passengers as individual objects. Make at least one passenger object in the  array  that has at least one key-value pair  on it.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Create a variable  firstPassenger  and assign the first passenger as its value  (the element in the 0th index of the  spaceship.passengers  array you just  made). Make sure to use bracket and dot notation to get the passenger  object  through  nested  access  (don’t  just  copy  the  object  into  the  variable!)

![](Images/image04802.jpeg)

![](Images/image04803.jpeg)

Pass  By  Reference

Objects are passed by reference. This means when we pass a variable  assigned to an object into a function as an argument, the computer  interprets the parameter name as pointing to the space in memory holding  that object. As a result, functions which change object properties actually  mutate  the object permanently  (even when the object  is assigned to

a  const  variable).

![](Images/image04804.jpeg)

Our function  paintIt()  permanently changed  the  color of

our spaceship  object. However,  reassignment of  the  spaceship  variable  wouldn’t  work in the same  way:

![](Images/image04805.jpeg)

![](Images/image04806.jpeg)

Let’s  look at  what  happened in the code  example:

• ![](Images/image04807.jpeg)We  declared thisobject  with  let.  This allowed  us to  reassign

it  to  a  new  object  with  identified  and  'transport  type'  properties  with  no problems.

• When we tried the same thing using a function designed to reassign  the object passed into it, the reassignment didn’t stick (even though  calling  console.log()  on the object produced the expected result).

• When we  passed  spaceship  into that function,  obj  became a  reference  to  the memory  location of the  spaceship  object, but not  to

the  spaceship  variable.  This is  because  the  obj  parameter of

the tryReassignment()  function is a variable in its own right. The body  of  tryReassignment()  has  no  knowledge  of  the  spaceship  variable  at  all!

• When we did the reassignment in the body of  tryReassignment(),  the  obj  variable came to refer to the memory location of the  object  {'identified' : false, 'transport type' : 'flying'}, while  the  spaceship  variable was completely unchanged from its earlier  value.

Instructions  1.

Write  a function  greenEnergy()  that has an  object as a parameter and sets  that object’s  'Fuel  Type'  property  to  'avocado oil'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Write  a  function  remotelyDisable()  that has  an  object  as  a parameter  and  sets  (or reassigns) that object’s  disabled  property to  true.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Call  your  two  functions  with  the  spaceship  object  in  the  code  editor,  then  console.log()  the  spaceship  object to  confirm  those  properties  were  changed/added.

![](Images/image04808.jpeg)

Looping  Through  Objects

Loops are programming tools that repeat a block of code until a condition  is met. We learned how to iterate through arrays using their numerical  indexing, but the key-value pairs in objects aren’t ordered! [JavaScript has](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)  [given  us alternative solution for iterating through objects  with](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)

[the for...in  syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in).

for...in  will execute a given block of code for  each property  in an object.

![](Images/image04809.jpeg)let spaceship = {  crew:  {

captain:  {  name:  'Lily',

degree:  'Computer  Engineering',

cheerTeam()  {  console.log('You  got  this!')  }

},

'chief officer': {  name:  'Dan',

degree:  'Aerospace  Engineering',

agree()  {  console.log('I  agree,  captain!')  }

},

medic:  {

name: 'Clementine',  degree:  'Physics',

announce() { console.log(`Jets on!`) } },  translator:  {

name:  'Shauna',

degree:  'Conservation  Science',

powerFuel()  {  console.log('The  tank  is  full!')  }

}

}

};

//  for...in

for (let crewMember in spaceship.crew) {  console.log(`${crewMember}:

${spaceship.crew[crewMember].name}`);

}

Our for...in  will iterate through each element  of the  spaceship.crew  object.  In each iteration, the variable  crewMember  is set to one of  spaceship.crew‘s  keys,  enabling us to log  a list of  crew members’  role and  name.

Instructions  1.

Using  for...in,  iterate  through  the  spaceship.crew  object in the code  editor  and console.log()  a  list of crew  roles and  names  in the  following

format:  '[crew member's role]: [crew member's name]', e.g.,'chief officer:  Dan'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Using  for...in,  iterate  through  the  spaceship.crew  object in the code  editor  and  console.log()  a  list  of  crew  names  and  degrees  in  the  following  format:  '[crew member's name]: [crew member's degree]', i.e.,'Lily: Computer  Engineering'.

![](Images/image04810.jpeg)

![](Images/image04811.jpeg)

Review

Way to go! You’re well on your way to understanding the mechanics of objects in  JavaScript. By building your own objects, you will have a better understanding of how  JavaScript built-in objects work as well. You can also start imagining organizing your  code  into  objects and modeling real world things in code.

Let’s  review  what we  learned in  this lesson:

• Objects  store  collections  of  key-value  pairs.

• Each key-value pair is a property—when a property is a function it is known as  a method.

• An object literal is composed of comma-separated key-value pairs surrounded  by  curly braces.

• You can access, add or edit a property within an object by using dot notation  or  bracket notation.

• We can add methods to our object literals using key-value syntax with  anonymous function expressions as values or by using the new ES6 method  syntax.

• We  can navigate  complex,  nested  objects by  chaining  operators.

• Objects are mutable—we can change their properties even when they’re  declared  with  const.

• Objects are passed by reference— when we make changes to an object  passed  into a function, those changes are permanent.

• We  can  iterate  through objects  using the  For...in  syntax.

Advanced  Objects  Introduction

Remember, objects in JavaScript are containers that store data and functionality. In  this lesson, we will build upon the fundamentals of creating objects and explore  some  advanced  concepts.

So if there are no objections, let’s learn more about objects!  In  this lesson we will cover these topics:

• how to use the  this  keyword.

• conveying  privacy  in  JavaScript methods.

• defining  getters  and  setters  in objects.

• creating  factory  functions.

• using  destructuring  techniques.

![](Images/image04812.jpeg)

![](Images/image04813.jpeg)

The  this Keyword

![](Images/image04814.jpeg)Objects are collections of related data and functionality. We store that  functionality  in  methods on our objects:

the

![](Images/image04815.jpeg)method  on  goat.

method.  We can invoke

goat.makeSound();  //  Prints  baaa   Nice, we have a  goat  object that can print  baaa  to the console. Everything  seems  to be working  fine.  What if we  wanted  to add  a  new method to

our goat  object  called  .diet()  that prints  the  goat‘s  dietType?

![](Images/image04816.jpeg)

![](Images/image04817.jpeg)That’s  strange,  why isnot  defined even  though  it’s a  property

of  goat?  That’s  because  inside the scope  of  the  .diet()  method, we  don’t  automatically have access to  other  properties of the  goat  object.

Here’s  where  the this  keyword comes to the rescue. If  we change  the  .diet()  method to use the  this,  the  .diet()  works! :

![](Images/image04818.jpeg)

The  this  keyword  references  the  calling object which  provides access  to  the  calling  object’s properties. In the  example above, the  calling  object

is  goat  and  by  using  this  we’re accessing the  goat  object itself, and then  the  dietType  property of  goat  by using  property dot notation.

Let’s get  comfortable using the  this  keyword  in a  method.

Instructions  1.

Let’s  create a  new object  to  practice  using  this.

In  main.js there is  an object  robot,  add  a  property of  model  and  assign to  it  a  value  of '1E78V2'. Add  another  property,  energyLevel  and assign to it a value  of  100.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

![](Images/image04819.jpeg)Inside  theobject,  add  a  method  named  provideInfo.  Inside the  body

of  provideInfo(),  return  the  following  string  by  using  interpolation:

I  am  MODEL  and  my  current energy  level  is  ENERGYLEVEL.

Replace  ‘MODEL’  and ‘ENERGYLEVEL’  with the  calling

object’s  model  and  energyLevel  property. Remember, to get  the access to  the  calling  object’s properties inside a  method, you have to use

the  this  keyword!

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Now  to  check  .provideInfo()  has  access to  the internal  properties  of  robot.  Log the result of calling  .provideInfo()  method on  robot  to the console.

![](Images/image04820.jpeg)

Arrow  Functions and  this

We saw in the previous exercise that for a method, the calling object is the  object  the  method  belongs  to. If we  use the  this  keyword  in a method  then  the value of  this  is the calling object. However, it becomes a bit more  complicated when we start using arrow functions for methods. Take a look  at  the example below:

![](Images/image04821.jpeg)

![](Images/image04822.jpeg)In  the comment,  you can see  thatwould log  undefined. So  what

happened? Notice that  in the  .diet()  is defined  using an arrow function.

Arrow functions inherently bind, or tie, an already defined  this  value to the  function itself that is NOT the calling object. In the code snippet above, the  value  of this  is  the  global  object,  or an object  that exists in the global scope,  which  doesn’t have a  dietType  property  and therefore returns  undefined.

To read more about either arrow functions or the global object check out  the  MDN documentation of  [the global object](https://developer.mozilla.org/en-US/docs/Glossary/Global_object) and [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions).

The key takeaway from the example above is to avoid using arrow functions  when using  this  in a  method!

Instructions  1.

Currently  the  .checkEnergy()  method  is  not  producing  the correct output  because  it is using arrow function  syntax.

Refactor, or change, the method to use a function expression. You can write  the  function using  either longhand or shorthand format.

After refactoring  the  method, notice  that  .checkEnergy()  has  access  to  the  other internal properties of the  robot  object.

![](Images/image04823.jpeg)

![](Images/image04824.jpeg)

Privacy

Accessing and updating properties is fundamental in working with objects.  However, there are cases in which we don’t want other code simply  accessing and updating an object’s properties. When discussing privacy in  objects, we define it as the idea that only certain properties should be  mutable  or  able to change in value.

![](Images/image04825.jpeg)![](Images/image04825.jpeg)Certain languages have privacy built-in for objects, but JavaScript does not  have this feature. Rather, JavaScript developers follow naming conventions  that signal to other developers how to interact with a property. One  common convention is to place an underscore  _  before the name of a  property to mean that the property should not be altered. Here’s an  example of using  _  to  prepend a  property.

![](Images/image04826.jpeg)const  bankAccount  =  {

_amount:  1000

}

In  the  example  above, the  _amount  is  not intended  to be directly  manipulated.

Even  so, it is  still possible to  reassign  _amount:

bankAccount._amount  =  1000000;

In later exercises, we’ll cover the use of methods called getters and setters.  Both methods are used to respect the intention of properties prepended, or  began, with  _. Getters can return the value of internal properties and setters  can safely reassign property values. For now, let’s see what happens if we  can  change properties that  don’t have setters or getters.

Instructions  1.

Below  the robot  object, reassign the  _energyLevel  property to  'high'.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Now  take  a look at the new  recharge  method in  robot.  .recharge()  will  add 30  to  _energyLevel.

What  will  happen  now that  _energyLevel  isn’t  a  number?  Call  .recharge()  on  robot  to  find  out.

Notice that a funky string is printed to the console! This is known as a side-  effect of type-coercion. No need to worry about what this means for now,  but it’s important to understand that you can cause unwanted side-effects  when  mutating objects and  their properties.

![](Images/image04827.jpeg)

Getters

Getters are methods that get and return the internal properties of an object.  But they can do more than just retrieve the value of a property! Let’s take a  look  at a  getter  method:

![](Images/image04828.jpeg)

![](Images/image04829.jpeg)

Notice  that in  the getter  method above:

![](Images/image04830.jpeg)• We  use  the

• We use an  both

keyword followed by a function.  conditional  to check if

and  _lastName  exist (by making  sure  they  both return

truthy values) and then return a different value depending on the  result.

• We  can access  the calling object’s  internal properties using  this.

In  fullName, we’re  accessing  both  this._firstName  and  this._lastName.

• In  the  last  line we  call  fullName  on  person. In  general, getter methods  do not need to be called with a set of parentheses. Syntactically, it  looks  like we’re accessing a property.

Now that we’ve gone over syntax, let’s discuss some notable advantages of  using  getter  methods:

• Getters  can  perform an  action on  the data  when getting  a  property.

• Getters  can  return different  values  using conditionals.

• In a getter, we can access the properties of the calling object  using  this.

• The functionality of our code is easier for other developers to  understand.

Another thing to keep in mind when using getter (and setter) methods is  that properties cannot share the same name as the getter/setter function. If  we  do so,  then calling  the  method will result in  an infinite call stack  error.

One workaround is to add an underscore before the property name like we  did  in the  example above.

Great,  let’s  go getter!

Instructions  1.

In  robot,  create  a getter  method  named  energyLevel  using the  get  keyword.  Leave  function body  blank for now.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside the getter method, add an  if  statement to check

if  this._energyLevel  is  a  number using  the  typeof  operator. If  that  condition  is  truthy,  return  'My  current energy  level  is ENERGYLEVEL'.

Replace  ENERGYLEVEL  with  the  value of  this._energyLevel.

Make  sure  you  return the  string  and not  logging it  to the  console.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

If  this._energyLevel  isn’t  a  number  it  could  be  that

the  _energyLevel  property  was  altered. Let’s  add a default  return  statement  for  when such a scenario arises.

Add  an  else  statement  that returns  'System  malfunction: cannot  retrieve  energy  level'.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Log the  result  of calling  the getter method  energyLevel  on  robot  to  the  console.

Notice that the method will return a formatted response rather than just  accessing  a property!

![](Images/image04831.jpeg)

![](Images/image04832.jpeg)

Setters

Along with getter methods, we can also create setter methods which  reassign values of existing properties within an object. Let’s see an example  of a setter  method:

![](Images/image04833.jpeg)

Notice  that in  the example above:

• We can perform a check for what value is being assigned  to  this._age.

• When we use the setter method, only values that are numbers will  reassign  this._age

• There are different outputs depending on what values are used to  reassign  this._age.

Then  to  use the setter method:

![](Images/image04834.jpeg)

Setter methods like  age  do not need to be called  with a set of parentheses.  Syntactically,  it  looks like  we’re reassigning the value  of a property.

Like getter methods, there are similar advantages to using setter methods  that include checking input, performing actions on properties, and  displaying  a clear  intention for  how the  object is supposed to be  used.

Nonetheless, even with a setter method, it is still possible to directly  reassign properties. For example, in the example above, we can still  set  ._age  directly:

![](Images/image04835.jpeg)

1.

Currently, in  robot  there is a  getter  method  for  numOfSensors  but no  setter  method! What if we need to add or remove some sensors? Let’s fix that  problem.

Add  a setter method named  numOfSensors  using  the  set  keyword. Provide a  parameter  of  num. Leave the function body  empty for now.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

There  are a  couple  of things we should  do in the setter  method:

• Add  a  check  to see  if  num  is a number using  the  typeof  operator.

• num  should also be greater  than or  equal to  0.

• If  both conditions are  met,  reassign  this._numOfSensors  to  num.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Now  add  an  else  that logs  'Pass  in a  number  that is greater  than or  equal  to  0'  to  the  console.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Use  the  numOfSensors  setter  method  on  robot  to assign  _numOfSensors  to  100.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

To  check  that the  setter  method worked,  console.log()  robot.numOfSensors.

![](Images/image04836.jpeg)

Factory  Functions

So far we’ve been creating objects individually, but there are times where  we want to create many instances of an object quickly. Here’s where factory  functions come in. A real world factory manufactures multiple copies of an  item quickly and on a massive scale. A factory function is a function that  returns  an object and can be  reused to make multiple  object instances.

Factory functions can also have parameters allowing us to customize the  object  that gets returned.

Let’s say we wanted to create an object to represent monsters in JavaScript.  There are many different types of monsters and we could go about making  each monster individually but we can also use a factory function to make  our  lives  easier.  To  achieve  this  diabolical  plan of  creating  multiple  monsters  objects, we can use  a factory function  that has  parameters:

![](Images/image04837.jpeg)

![](Images/image04838.jpeg)In thefunction  above, it  has four  parameters and  returns an

object that has the properties:  name,  age,  energySource, and  scare(). To make  an  object  that represents a  specific monster like  a ghost,  we can

call  monsterFactory  with  the  necessary  arguments  and  assign the  return  value to  a variable:

![](Images/image04839.jpeg)

Now we have a  ghost  object as a result of calling  monsterFactory()  with the  needed arguments. With  monsterFactory  in place,  we don’t have to create an  object  literal every time we  need a new  monster.  Instead, we can invoke

the  monsterFactory  function with the  necessary  arguments  to take  over the  world  make a monster for  us!

Instructions  1.

Instead of making individual robots like we’ve been doing, let’s make a  factory  function to make robots as we  please!

Create a factory function named  robotFactory  that  has two

parameters  model  and  mobile.  Make the function return  an object. In the  object, add a key of  model  with the value of the  model  parameter. Add  another property that has a key of  mobile  with a  value of

the  mobile  parameter.

Then  add  a method named  beep  without a parameter that will log  'Beep  Boop'  to the console.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Use  your factory  function by  declaring a

![](Images/image04840.jpeg)variable  named  tinCan.

Assign  to  tinCan  the value  of calling  robotFactory  with  the first argument  of  'P-500'  and the second  argument of  true.

 Checkpoint 3 Passed

3.

Let’s now  check what  tinCan  can  do! Call  .beep()  on  tinCan.

You  should  see  'Beep Boop'  printed to the  console which means the factory  function produced a robot object! Play around with  tinCan  to check the  other  properties!

![](Images/image04841.jpeg)

Property  Value  Shorthand

ES6 introduced some new shortcuts for assigning properties to variables  known  as destructuring.

In the previous exercise, we created a factory function that helped us create  objects. We had to assign each property a key and value even though the  key name was the same as the parameter name we assigned to it. To  remind  ourselves, here’s a truncated  version of the  factory function:

![](Images/image04842.jpeg)

Imagine  if  we had  to include  more properties,  that  process would  quickly

become tedious! But we can use a destructuring technique, called property  value shorthand, to save ourselves some keystrokes. The example below  works  exactly like the example above:

![](Images/image04843.jpeg)

Notice  that  we don’t  have  to repeat  ourselves  for  property  assignments!

Instructions  1.

Use the property value shorthand and refactor the factory function  in main.js

Property  Value  Shorthand

ES6 introduced some new shortcuts for assigning properties to variables  known  as destructuring.

In the previous exercise, we created a factory function that helped us create  objects. We had to assign each property a key and value even though the  key name was the same as the parameter name we assigned to it. To  remind  ourselves, here’s a truncated  version of the  factory function:

![](Images/image04844.jpeg)

![](Images/image04845.jpeg)

Imagine  if  we had  to include  more properties,  that  process would  quickly

become tedious! But we can use a destructuring technique, called property  value shorthand, to save ourselves some keystrokes. The example below  works  exactly like the example above:

![](Images/image04846.jpeg)

Notice  that  we don’t  have  to repeat  ourselves  for  property  assignments!

Instructions  1.

Use the property value shorthand and refactor the factory function  in main.js

Property  Value  Shorthand

ES6 introduced some new shortcuts for assigning properties to variables  known  as destructuring.

In the previous exercise, we created a factory function that helped us create  objects. We had to assign each property a key and value even though the  key name was the same as the parameter name we assigned to it. To  remind  ourselves, here’s a truncated  version of the  factory function:

![](Images/image04847.jpeg)

Imagine if we had to include more properties, that process would quickly  become tedious! But we can use a destructuring technique, called property  value shorthand, to save ourselves some keystrokes. The example below  works  exactly like the example above:

![](Images/image04848.jpeg)

Notice  that  we don’t  have  to repeat  ourselves  for  property  assignments!

Instructions  1.

Use the property value shorthand and refactor the factory function  in main.js

![](Images/image04849.jpeg)

Destructured  Assignment

We often want to extract key-value pairs from objects and save them as  variables.  Take for example the  following object:

![](Images/image04850.jpeg)

![](Images/image04851.jpeg)If we wanted to extract the  the  following  code:

property  as  a  variable,  we could  using

![](Images/image04852.jpeg)

However,  we  can also  take advantage  of a  destructuring technique

called destructured assignment to save ourselves some keystrokes. In  destructured assignment we create a variable with the name of an object’s  key that is wrapped in curly braces  { }  and assign to it the object. Take a  look  at the example below:

![](Images/image04853.jpeg)

Look  back  at  the  vampire  object’s properties  in the first code example. Then,  in the example above, we declare a new variable  residence  that extracts the  value  of  the  residence  property of  vampire.  When we log  the value

of  residence  to  the console,  'Transylvania'  is  printed.

We can even use destructured assignment to grab nested properties of an  object:

![](Images/image04854.jpeg)

1.

Use  destructured  assignment  to  create  a  const  variable

named  functionality  that extracts  the  functionality  property  of  robot.

If you need a reminder on how to use destructured assignment, review the  example  in the narrative  or check the hint.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Since functionality  is referencing  robot.functionality  we can call the  methods available to  robot.functionality  simply  through  functionality.

Take  advantage of  this shortcut  and call the  .beep()  method  on  functionality.

![](Images/image04855.jpeg)

Built-in  Object  Methods

In the previous exercises we’ve been creating instances of objects that have  their own methods. But, we can also take advantage of built-in methods for  Objects!

For  example,  we have  access  to object  instance methods

like:  .hasOwnProperty(),  .valueOf(), and many more! Practice your  documentation reading skills and check out: [MDN’s object instance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object#Methods)  [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object#Methods).

There  are  also useful  Object class  methods  such

as  Object.assign(),  Object.entries(),  and  Object.keys()  just  to name  a  few.  For  a comprehensive  list, browse:  [MDN’s object instance  documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object#Methods_of_the_Object_constructor).

Let’s  get  acquainted  with  some of these  methods and their  documentation.

Note: You will see errors as you work through this exercise, but by the end  the  errors will be fixed!

Instructions  1.

In main.js there is an object,  robot. We’d like to grab the property names,  otherwise known as keys, and save the keys in an array which is assigned  to  robotKeys. However,  there’s something  missing  in  the  method call.

Find out what we have to include by  reading  [MDN’s  Object.keys()  documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys).

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Object.entries()  will  also  return  an array,  but  the array will  contain  more  arrays  that  have both  the key and  value of the  properties in an  object.

Declare  a  const  variable  named  robotEntries  and assign  to it  the entries  of  robot  by  calling  Object.entries().

To  find  how to  use  Object.entries(), read  [the  documentation at  MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries).

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Now  what if we  want another  object that has the properties of  robot  but  with a few additional properties.  Object.assign()  sounds like a great  method  to use,  but like the previous examples we  should

check  [Object.assign()  documentation  at MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign).

Declare  a const  variable named  newRobot.  newRobot  will  be a  new object  that  has  all the properties of  robot  and the properties in the following

object:  {laserBlaster: true, voiceRecognition: true}. Make sure that you  are  not changing the  robot  object!

![](Images/image04856.jpeg)

Review

Congratulations on finishing Advanced Objects!  Let’s  review  the concepts  covered  in this  lesson:

• The  object that  a method belongs to is called  the calling object.

• The  this  keyword refers the calling object  and  can  be used to access  properties  of the calling object.

• Methods do not automatically have access to other internal properties of the  calling object.

• The value of  this  depends  on where the  this  is  being accessed from.

• We cannot use arrow functions as methods if we want to access other internal  properties.

• JavaScript objects do not have built-in privacy, rather there are conventions to  follow  to notify other developers about  the intent of the code.

• The usage of an underscore before a property name means that the original  developer  did not intend  for that property to be  directly changed.

• Setters and getter methods allow for more detailed ways of accessing and  assigning  properties.

• Factory  functions  allow us  to  create  object  instances quickly  and repeatedly.

• There are different ways to use object destructuring: one way is the property  value  shorthand and  another  is destructured  assignment.

• As with any concept, it is a good skill to learn how to use the documentation  with  objects!

Introduction  to Classes

JavaScript is an object-oriented programming (OOP) language we can use to  model  real-world items.  In this  lesson, you  will  learn how  to make  classes.

Classes  are a  tool that developers  use to quickly  produce similar  objects.

Take, for example, an object representing a dog named  halley. This  dog’s  name  (a  key) is  "Halley"  (a  value) and has an  age  (another  key)  of  3  (another value). We  create the  halley  object below:

![](Images/image04857.jpeg)

Now, imagine you own a dog daycare and want to create a catalog of all  the dogs who belong to the daycare. Instead of using the syntax above for  every dog that joins the daycare, we can create a  Dog  class that serves as a  template  for creating new  Dog  objects. For  each new dog,  you can  provide  a  value  for  their name.

As you can see, classes are a great way to reduce duplicate code and  debugging  time.

After we lay the foundation for classes in the first few exercises, we will  introduce inheritance and static methods — two features that will make  your  code more efficient and meaningful.

Instructions  1.

In the next exercise, you will learn about classes in greater detail. Before  you  do,  take a moment to study  the class in  main.js.

Spend  some  time identifying  the similarities  and  differences  between

the  Dog  class in  main.js  and the code  we used to  create our  halley  object in  the  instructions above.

 Checkpoint 2 Passed

2.

Copy  the  class  instantiation,  method  call,  and  console.log()  statements  below into  main.js.

![](Images/image04858.jpeg)

What  do you expect  to  see when you  run this  code?

![](Images/image04859.jpeg)

![](Images/image04860.jpeg)

Constructor

In the last exercise, you created a class called  Dog, and used it to produce  a  Dog  object.

Although you may see similarities between class and object syntax, there is  one  important method that sets them apart.  It’s called

the  constructor method.  JavaScript  calls  the  constructor()  method every  time  it creates a  new instance  of  a class.

![](Images/image04861.jpeg)

• Dog  is  the  name  of our  class. By convention,  we capitalize and  CamelCase  class names.

• JavaScript  will  invoke the  constructor()  method every  time we create  a  new instance of our  Dog  class.

• This  constructor()  method  accepts  one  argument,  name.

• Inside  of  the  constructor()  method, we  use  the  this  keyword.  In  the  context of a class,  this  refers to an  instance of that class.  In

the  Dog  class,  we  use  this  to set the  value of the Dog  instance’s  name  property  to the  name  argument.

• Under  this.name, we create a property called  behavior, which will keep  track  of the number  of times a  dog misbehaves.

The  behavior  property  is always  initialized  to zero.

In  the next exercise, you will learn how  to create  Dog  instances.

![](Images/image04862.jpeg)

1.

Create  an empty  class named  Surgeon.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside  the  Surgeon  class,  create a  constructor()  method  that accepts  two  parameters:  name  and  department.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Inside  the  Surgeon  constructor(),  create  name  and  department  properties  and  set  them equal to  your input parameters.

![](Images/image04863.jpeg)

Instance

Now, we’re ready to create class instances. An instance is an object that  contains the property names and methods of a class, but with unique  property values. Let’s look at our  Dog  class example.

![](Images/image04864.jpeg)

![](Images/image04865.jpeg)Below  our

class,  we  use  the

keyword  to  create an  instance  of

![](Images/image04866.jpeg)our Dog  class. Let’s consider the line  of  code step-by-step.

• We  create a  new variable named  halley  that will  store an instance of  our  Dog  class.

• We  use  the  new  keyword to  generate  a new instance  of the  Dog  class.  The  new  keyword calls the  constructor(), runs the code inside of it,  and  then returns the new  instance.

• We  pass  the  'Halley'  string to the  Dog  constructor,  which sets  the  name  property  to  'Halley'.

• Finally,  we  log  the value saved  to the  name  key in our  halley  object,  which logs  'Halley'  to the  console.

Now you know how to create instances. In the next exercise, you will learn  how  to add getters, setters,  and methods.

Instructions  1.

Create  an  instance  of the  Surgeon  class — set  the  name  to  'Francisco  Romero'  and  department  to  'Cardiovascular'.

Save  the instance  to a  constant  variable  called  surgeonRomero.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Create  an  instance  of the  Surgeon  class — set  the  name  to  'Ruth  Jackson'  and  department  to  'Orthopedics'.

Save  the instance  to a  constant  variable  called  surgeonJackson.

![](Images/image04867.jpeg)

![](Images/image04868.jpeg)

Methods

At  this point, we  have a  Dog  class  that spins up objects

with name  and  behavior  properties. Below,  we will  add  getters and a method  to  bring our class to life.

Class method and getter syntax is the same as it is for objects except you  can  not include commas between methods.

![](Images/image04869.jpeg)

In  the  example  above, we add getter  methods for  name  and  behavior.  Notice,  we  also prepended our property names with  underscores

(_name  and  _behavior), which indicate these  properties should  not be  accessed  directly. Under  the getters,  we add  a method

named .incrementBehavior(). When you call  .incrementBehavior()  on a Dog  instance,  it  adds  1  to the  _behavior  property. Between each of our  methods,  we  did  not  include commas.

![](Images/image04870.jpeg)

1.

In  the Surgeon  constructor, prepend the  name  and  department  properties with  an  underscore (_).

 Checkpoint 2 Passed

2.

Inside  of  the  constructor(), add  a  property

named  _remainingVacationDays  and set it equal to  20.

 Checkpoint 3 Passed

3.

Under  the  constructor(),  create  a  getter  called  name  that  returns  the  value  saved to  _name.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Under the  name  getter, create a  getter called  department  that returns the  value  saved to  _department.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Under the  department  getter, create a getter

called  remainingVacationDays  that  returns  the  value  saved  to  _remainingVacationDays.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Under the  remainingVacationDays  getter, create a  method

called  takeVacationDays  that  accepts  one  argument  named  daysOff.

Inside of the method,  subtract  daysOff  from  the  number saved

to  _remainingVacationDays.  Set  _remainingVacationDays  to  the  result.

![](Images/image04871.jpeg)

![](Images/image04872.jpeg)

Method  Calls

Finally, let’s use our new methods to access and manipulate data  from  Dog  instances.

![](Images/image04873.jpeg)

![](Images/image04874.jpeg)In the example above, we create the  save  it to a  variable named  halley.

class,  then  create  an  instance,  and

The syntax for calling methods and getters on an instance is the same as  calling them on an object — append the instance with a period, then the  property or method name. For methods, you must also include opening  and  closing parentheses.

Let’s  take a  moment to create two  Dog  instances and  call  our  .incrementBehavior()  method on  one  of  them.

![](Images/image04875.jpeg)

In  the  example  above, we create  two  new  Dog  instances,  nikko  and  bradford.  Because  we increment the behavior of our  nikko  instance, but not  bradford,  accessing  nikko.behavior  returns  1  and

accessing  bradford.behavior  returns  0.

Instructions  1.

At  the  bottom  of  main.js, use  console.log()  to print the value saved  to  thename  property  of the  surgeonRomero  object.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Call

![](Images/image04876.jpeg)on  surgeonRomero,  with an  input of  3.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

After the call to  .takeVacationDays(), use  console.log()  to print the value  saved  to  the  remainingVacationDays  property of the  surgeonRomero  instance.

![](Images/image04877.jpeg)

console.log(surgeonRomero.remainingVacationDays);

Inheritance  I

![](Images/image04878.jpeg)Imagine our doggy daycare is so successful that we decide to expand the business  and  open  a kitty daycare. Before the daycare opens, we need to create a  Cat  class so  we can quickly generate  Cat  instances. We know that the properties in our  Cat  class  (name, behavior) are similar to the properties in our  Dog  class, though, there will be  some  differences, because of course, cats are not dogs.

Let’s say that our  Cat  class looks like this:

![](Images/image04879.jpeg)

In  the  example  above, we create a  Cat  class.  It shares a  couple of properties

(_name  and _behavior) and a method (.incrementBehavior()) with the  Dog  class from  earlier exercises.  The  Cat  class  also  contains  one  additional  property  (_usesLitter), that  holds  a boolean  value to indicate  whether  a cat  can use their litter  box.

When  multiple classes  share  properties or  methods, they  become candidates

for inheritance — a tool developers use to decrease the amount of code they need to  write.

With inheritance, you can create a parent class (also known as a superclass) with  properties and methods that multiple child classes (also known as subclasses) share.  The  child classes inherit the  properties and  methods from  their parent class.

Let’s  abstract the  shared  properties and methods  from our  Cat  and  Dog  classes into  a  parent  class called  Animal.

![](Images/image04880.jpeg)

In  the  example  above, the  Animal  class contains the properties and methods  that  the  Cat  and Dog  classes share (name,  behavior,  .incrementBehavior()).

The diagram to the right shows the relationships we want to create between the  Animal,  Cat, and Dog classes.

![](Images/image04881.jpeg)

Inheritance  II

In  the last exercise,  we created a  parent  class named  Animal  for two  child  classes named  Cat  and  Dog.

The  Animal  class  below contains  the shared  properties and methods  of  Cat  and  Dog.

![](Images/image04882.jpeg)

![](Images/image04883.jpeg)The code below shows the  the  Animal  class.

class  that  will  inherit  information  from

![](Images/image04884.jpeg)

To  the  right, in main.js,  you  will put what  you learned to practice  by

creating  a  parent  class  named  HospitalEmployee.

Instructions  1.

In  the  next few exercises, you  will create two subclasses  (Doctor  and  Nurse)  from a parent class named  HospitalEmployee. Below, we have listed the  properties and methods you will find  in the  Doctor  and  Nurse  classes.

Doctor

• Properties:  _name,  _remainingVacationDays  (set  to  20  inside  the  constructor()),  _insurance

• Methods:  .takeVacationDays()

Nurse

• Properties:  _name,  _remainingVacationDays  (set  to  20  inside  constructor()),  _certifications

• Methods:  .takeVacationDays(),  .addCertification()

In main.js, create a parent class named  HospitalEmployee. Add a constructor  with name  as an argument.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside  of  the  constructor(), set  the

instance’s  _name  to  name  and  _remainingVacationDays  to  20.

 Checkpoint 3 Passed

3.

Under  the constructor,  create getters  for

your _name  and  _remainingVacationDays  properties.

Inside  the  getter,  return the  property’s  value.

 Checkpoint 4 Passed

4.

Under the getters, add a method called  takeVacationDays.  This  method  should  accept  one  argument,  called  daysOff.

Inside  the method, subtract  daysOff  from  _remainingVacationDays.  Save  the  result  to  _remainingVacationDays.

![](Images/image04885.jpeg)

![](Images/image04886.jpeg)

Inheritance  III

We’ve  abstracted  the  shared  properties and  methods of

our Cat  and  Dog  classes into  a parent class called  Animal  (See below).

![](Images/image04887.jpeg)

Now that we have these shared properties and methods in the  parent  Animal  class, we can extend them to the subclass,  Cat.

![](Images/image04888.jpeg)

![](Images/image04889.jpeg)In the example above, we create a new class named  the  Animal  class.  Let’s pay special  attention to  our  new  keywords:  extends  and  super.

that  extends

• The  extends  keyword makes  the methods of  the  animal class  available  inside  the cat  class.

• The  constructor,  called when  you create  a new  Cat  object,  accepts two  arguments,  name  and  usesLitter.

• The  super  keyword calls the constructor of the parent class. In this  case,  super(name)  passes the name  argument of the  Cat  class to the  constructor of  the  Animal  class.  When  the  Animal  constructor  runs,  it  sets  this._name  = name;  for  new  Cat  instances.

• _usesLitter  is  a  new property that is unique to the  Cat  class, so we set  it  in the  Cat  constructor.

Notice, we call  super  on the first  line of  our  constructor(), then set

the usesLitter  property on the second line. In a  constructor(), you must  always  call the  super  method before you can use the  this  keyword — if you  do not, JavaScript will throw a reference error. To avoid reference errors, it  is  best practice to call  super  on the first line of  subclass  constructors.

Below,  we  create  a  new Cat  instance  and call its name  with the  same syntax  as  we did  with the  Dog  class:

![](Images/image04890.jpeg)

In  the  example  above,  we  create  a new  instance  the  Cat  class,  named  bryceCat. We pass  it  'Bryce'  and  false  for

our name  and  usesLitter  arguments.  When  we

call  console.log(bryceCat._name)  our  program  prints,  Bryce.

In  the  example above,  we  abandoned  best practices  by  calling

our _name  property directly.  In  the next exercise,  we’ll address this  by calling  an  inherited getter  method for  our  name  property.

Instructions  1.

![](Images/image04891.jpeg)In  this exercise, you  will  begin to create theclass  as a  child of

the  HospitalEmployee  class.  Remember  the  Nurse  class  has  the following  properties  and methods:

Nurse

• Properties:  _name,  _remainingVacationDays  (set  to  20  inside  constructor()),  _certifications

• Methods:  .takeVacationDays(),  .addCertification()

Under  HospitalEmployee,  create  an  empty class  named  Nurse  that  extends  HospitalEmployee.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside  the  Nurse  class, create a  constructor()  that accepts two arguments.  Use  the list  of properties above to name these  arguments.

Check  the Hint  if  you need help.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

In  the  Nurse  constructor,  call the  parent’s constructor  method and  pass  the  appropriate  value(s).

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Inside  of  the  Nurse  constructor,  and under  super, set  _certifications.

 Checkpoint 5 Passed

5.

Under the Nurse  class, create a new instance of  Nurse  and save it to a  constant variable named  nurseOlynyk. Pass in the following values for each  property:

• name:  'Olynyk'

• certifications:  ['Trauma',  'Pediatrics']

![](Images/image04892.jpeg)

Inheritance  IV

Now that we know how to create an object that inherits properties from a  parent  class let’s turn our  attention to  methods.

When  we  call  extends  in a class declaration, all of the parent methods  are  available to  the child class.

Below, we extend our  Animal  class to a  Cat  subclass.

![](Images/image04893.jpeg)In  the example  above, ourclass extends  Animal. As a result, the  Cat  class

has  access to the  Animal  getters and the  .incrementBehavior()  method.

Also in  the code above, we  create a  Cat  instance named  bryceCat.  Because bryceCat  has access to the  name  getter, the code below  logs  'Bryce'  to the console.

console.log(bryceCat.name);  Since the  extends  keyword brings all of the parent’s getters and methods  into the child class,  bryceCat.name  accesses the  name  getter and returns the  value saved to the  name  property.

Now consider a more involved example and try to answer the following  question:  What will the code below  log to the  console?

![](Images/image04894.jpeg)

The  correct  answer is  1.  But why?

• The  Cat  class  inherits the  _behavior  property,  behavior  getter, and  the  .incrementBehavior()  method from  the  Animal  class.

• When we  created  the  bryceCat  instance,  the  Animal  constructor set  the  _behavior  property  to zero.

• The  first  line of code calls  the inherited  .incrementBehavior()  method,  which  increases the  bryceCat  _behavior  value  from zero  to one.

• The  second  line  of  code calls  the  behavior  getter  and logs  the value  saved to  _behavior  (1).

Instructions  1.

Call  .takeVacationDays()  with  an  input  of  5  on  your  nurseOlynyk  instance.

 Checkpoint 2 Passed

2.

Under  the  method  call,  log  the  value  saved  to  the  remainingVacationDays  property  in  nurseOlynyk.

![](Images/image04895.jpeg)

![](Images/image04896.jpeg)

Inheritance  V

In addition to the inherited features, child classes can contain their own  properties,  getters,  setters, and  methods.

Below,  we  will  add a  usesLitter  getter.  The syntax for  creating  getters,  setters,  and methods is the  same as it is in  any other class.

![](Images/image04897.jpeg)

In  the  example  above, we  create a  usesLitter  getter in the  Cat  class that  returns  the value saved  to  _usesLitter.

Compare the  Cat  class above to the one  we  created  without  inheritance:

![](Images/image04898.jpeg)class  Cat  {

constructor(name, usesLitter) {  this._name = name;  this._usesLitter = usesLitter;  this._behavior  = 0;

}

get  name()  {

return  this._name;

}

get  usesLitter()  {

return  this._usesLitter;

}

get  behavior()  {

return  this._behavior;

}

incrementBehavior() {  this._behavior++;

}

}

We  decreased the number of lines required  to create  the  Cat  class by  about  half. Yes, it did require an extra class (Animal), making the reduction in the  size of our Cat  class seem moot. However, the benefits (time saved,  readability, efficiency) of inheritance grow as the number and size of your  subclasses  increase.

One benefit is that when you need to change a method or property that  multiple classes share, you can change the parent class, instead of each  subclass.

Before we move past inheritance, take a moment to see how we would  create  an additional subclass, called  Dog.

![](Images/image04899.jpeg)

This Dog  class has access to the same properties, getters, setters, and  methods  as  the  Dog  class  we made without inheritance,  and is a quarter  the  size.

Now that we’ve abstracted animal daycare features, it’s easy to see how you  can  extend  Animal  to  support other  classes,  like  Rabbit,  Bird  or even  Snake.

Instructions  1.

Use the properties and methods below to help you complete the tasks that  follow.

Nurse

• Properties:  _name,  _remainingVacationDays  (set  to  20  inside  the  constructor()),  _certifications

• Methods:  .takeVacationDays(),  .addCertification()

Under the Nurse  constructor(), add a getter that returns the value saved to  the  Nurse  instance’s  _certifications.

 Checkpoint 2 Passed

2.

Add  a method called  addCertification  under the  certifications  getter.

The method should accept one input (newCertification). Inside the method,  use  the [push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push?v=example) method to add the  newCertification  value to the

nurse’s  certifications  array.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

At  the bottom  of  main.js call  the  .addCertification()  method  on  nurseOlynyk  with a  parameter of  'Genetics'.

 Checkpoint 4 Passed

4.

Log the  value saved  to the  certifications  property of  nurseOlynyk.

![](Images/image04900.jpeg)class HospitalEmployee {  constructor(name)  {

this._name = name;  this._remainingVacationDays  =  20;

}

get  name()  {

return  this._name;

}

get  remainingVacationDays()  {

return  this._remainingVacationDays;

}

takeVacationDays(daysOff) {  this._remainingVacationDays  -=  daysOff;

}

}

class Nurse extends HospitalEmployee {  constructor(name,  certifications)  {

super(name);

this._certifications  =  certifications;

}

get  certifications()  {

return  this._certifications;

}

addCertification(newCertification) {  this._certifications.push(newCertification);

}

}

const nurseOlynyk = new Nurse('Olynyk', ['Trauma','Pediatrics']);  nurseOlynyk.takeVacationDays(5);  console.log(nurseOlynyk.remainingVacationDays);  nurseOlynyk.addCertification('Genetics');

console.log(nurseOlynyk.certifications);

Static  Methods

Sometimes you will want a class to have methods that aren’t available in  individual  instances, but that you  can call directly from the  class.

Take  the  Date  class, for  example — you can  both create  Date  instances to  represent  whatever date you want, and  call  static  methods,

like  Date.now()  which  returns  the current  date,  directly  from the  class.

The  .now()  method is static,  so you can call it  directly from the class, but  not  from  an instance of the class.

Let’s  see  how to  use the  static  keyword to create  a static method  called  generateName  method in our  Animal  class:

![](Images/image04901.jpeg)

In  the example above, we  create  a  static  method

![](Images/image04902.jpeg)called  .generateName()  that  returns  a  random  name  when  it’s  called.  Because  of the static keyword, we can only access  .generateName()  by appending it  to the  Animal  class.

We  call the  .generateName()  method  with the following  syntax:

console.log(Animal.generateName());  //  returns  a  name

You  cannot access  the  .generateName()  method  from  instances of  the  Animal  class or  instances of its subclasses (See below).

![](Images/image04903.jpeg)

The  example  above will  result in  an error,  because you  cannot call  static

methods  (.generateName())  on  an  instance  (tyson).

Instructions  1.

Inside of your  HospitalEmployee  class,  create  a  static method

called  generatePassword. When it’s called, this method should return a  random  integer between zero  and 10,000.

![](Images/image04904.jpeg)

![](Images/image04905.jpeg)

Review:  Classes

Way  to  go! Let’s review  what you learned.

• Classes  are templates for  objects.

• Javascript  calls a constructor  method when we  create  a  new instance of  a class.

• Inheritance is when we create a parent class with properties and methods that  we  can extend  to child classes.

• We  use  the  extends  keyword to  create a  subclass.

• The  super  keyword calls the  constructor()  of  a  parent class.

• Static  methods are  called on  the class,  but  not on  instances of  the class.

BROWSER  COMPATIBILITY AND TRANSPILATION

Introduction

You’re probably prompted to update your web browser every few months.  Do you know why? A few reasons include addressing security  vulnerabilities, adding features, and supporting new HTML, CSS, and  JavaScript  syntax.

The reasons above imply there is a period before a software update is  released when there are security vulnerabilities and unsupported language  syntax.

This lesson focuses on the latter. Specifically, how developers address the  gap between the new JavaScript syntax that they use and the JavaScript  syntax  that web  browsers recognize.

This has become a widespread concern for web developers since Ecma  International, the organization responsible for standardizing JavaScript,  released a new version of it in 2015, called ECMAScript2015, commonly  referred to as ES6\. Note, the 6 refers to the version of JavaScript and is not  related  to the year it was released (the  previous version was ES5).

Upon release, web developers quickly adopted the new ES6 syntax, as it  improved readability and efficiency. However, ES6 was not supported by  most  web  browsers,  so  developers  ran  into  browser  compatibility  issues.

In this lesson, you will learn about two important tools for addressing  browser  compatibility issues.

• caniuse.com — A website that provides data on web browser  compatibility for HTML, CSS, and JavaScript features. You will learn  how  to use it to look up ES6 feature support.

• Babel — A Javascript library that you can use to convert new,  unsupported JavaScript (ES6), into an older version (ES5) that is  recognized  by most  modern browsers.

Let’s get started by running ES6 JavaScript on a fake old web browser  version.

Instructions

1.

Copy the following code into main.js. The code includes three features of  ES6  syntax:  const,  let, and ES6 string interpolation.

![](Images/image04906.jpeg)

Output

![](Images/image04907.jpeg)

caniuse.com  I

Since Ecma’s release of ECMAScript2015 (ES6), software companies have slowly  added support for ES6 features and syntax. While most new browser versions  support the majority of the ES6 library, there are still a couple sources of  compatibility issues:

• Some users have not updated to the latest, ES6 supported web browser  version.

• A few ES6 features, like modules, are still not supported by most web  browsers.

Because companies add support for ES6 features gradually, it’s important for you to  know  how to look up browser support  on a  feature-by-feature basis.  The

website [caniuse.com](http://caniuse.com/) is the best resource for finding browser compatibility  information.

In caniuse, you can enter an ES6 feature, like  let, and see the percentage of browsers  that recognize it. You can also see when each major web browser (Chrome, Safari,  Edge,  etc.)  added support for the keyword.

caniuse.com  II

Now, it’s your turn to get some practice with [caniuse.com](http://caniuse.com/). In a new tab,  open  caniuse.com and complete the tasks below.

Instructions  1.

Look up the percentage of browsers that support JavaScript ES5\. Save the  value,  as a  number, to  the  variable  esFivePercentageSupport.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Look up the percentage of browsers that support “Template Literals”, a  feature  that  was introduced in ES6.

Save  the  value,  as a  number,  to the  variable  esSixTemplateLiterals.

![](Images/image04908.jpeg)

Why  ES6?

Before we learn how to set up a JavaScript project that converts ES6 to an  older version, it’s worth understanding a few of the reasons Ecma made  such  substantial updates.

The version of JavaScript that preceded ES6 is called JavaScript ES5\. Three  reasons  for  the ES5 to ES6 updates are listed below:

• Readability and economy of code — The new syntax is often easier to  understand (more readable) and requires fewer characters to create  the  same functionality  (economy of code).

• Addresses sources of ES5 bugs — Some ES5 syntax led to common  bugs. With ES6, Ecma introduced syntax that mitigates some of the  most  common pitfalls.

• A similarity to other programming languages — JavaScript ES6 is  syntactically more similar to other object-oriented programming  languages. This leads to less friction when experienced, non-  JavaScript  developers want to learn JavaScript.

Because ES6 addressed the above issues, Ecma knew that adoption by web  developers  would  occur  quickly,  while web  browser  support lagged  behind.

To limit the impact of ES6 browser compatibility issues, Ecma made the new  syntax backwards compatible, which means you can map JavaScript ES6  code  to ES5.

Instructions  1.

In  these  tasks, you  will manually  change the  code  in main.js  to ES5  syntax.

The  let  and const  keywords  were introduced in ES6.  Before  that, we  declared all variables with  the  var  keyword.

Change  the

and

keywords  in  main.js  to  var.

![](Images/image04909.jpeg)![](Images/image04910.jpeg)     Checkpoint 2 Passed

Stuck?  Get a hint

2.

The  following  line  of  code is  written  with  ES6 string  interpolation:

![](Images/image04911.jpeg)

In  ES5, we used  plus signs (+)  to  interpolate variables into  strings.

In  main.js,  use  ES5  string  interpolation to  set  carbonara  to the same string  as above.

![](Images/image04912.jpeg)

Transpilation  With  Babel

In the last exercise, you manually converted ES6 code to ES5\. Although  manual conversion only took you a few minutes, it is unsustainable as the  size  of the JavaScript file  increases.

Because ES6 is predictably backwards compatible, a collection of JavaScript  programmers developed a JavaScript library called Babel that transpiles ES6  JavaScript  to ES5.

Transpilation is the process of converting one programming language to  another.

In the remaining exercises of this lesson, you will learn how to use Babel to  transpile the new, easy-to-write version of JavaScript (ES6) to the old,  browser-compatible  version of JavaScript (ES5).

In the instructions below, you will pass JavaScript ES6 code to Babel, which  will  transpile it to  ES5 and write  it to a file in the  lib  directory.

![](Images/image04913.jpeg)

1.

In  the terminal  window  type:

![](Images/image04914.jpeg)

This  installs one  of the  two required  Babel packages.

![](Images/image04915.jpeg)Checkpoint 2  Passed

2.

In  the terminal  window  type:

![](Images/image04916.jpeg)

This  installs the  second  of  two required Babel  packages.

![](Images/image04915.jpeg)Checkpoint 3  Passed

3.

In  the  terminal,  type  npm run  build  and press enter.  You  can view the  ES5  code in ./lib/main.js.

You  may  need to  refresh to  see the  newly created  lib  directory.

![](Images/image04917.jpeg)

npm  init

In the last exercise, you wrote one command in your terminal to transpile  ES6 code to ES5\. In the next five exercises you will learn how to setup a  JavaScript project that transpiles code when you run  npm run build  from the  root  directory of a JavaScript project.

The first step is to place your ES6 JavaScript file in a directory called src.  From  your  root directory,  the path  to the ES6 file is ./src/main.js

The  initial  JavaScript project  file structure  is:

![](Images/image04918.jpeg)

Before we install Babel, we need to setup our project to use the [node](https://docs.npmjs.com/getting-started/what-is-npm)  [package manager (npm)](https://docs.npmjs.com/getting-started/what-is-npm). Developers use npm to access and manage Node  packages. Node packages are directories that contain JavaScript code  written by other developers. You can use these packages to reduce  duplication  of  work and avoid bugs.

Before we can add Babel to our project directory, we need to run  npm init.  The  npm  init  command  creates a package.json  file in  the root directory.

A package.json file contains information about the current JavaScript  project.  Some of this information includes:

• Metadata — This includes a project title, description, authors, and  more.

• A list of node packages required for the project — If another  developer  wants to  run your  project,  npm looks

inside  package.json  and  downloads the  packages in  this list.

• Key-value pairs for command line scripts — You can use npm to run  these shorthand scripts to perform some process. In a later exercise,  we  will add a  script that runs  Babel and transpiles ES6  to ES5.

If you have Node installed on your computer, you can create  a  package.json  file by  typing  npm init  into  the  terminal.

The terminal prompts you to fill in fields for the project’s metadata (name,  description,  etc.)

You are not required to answer the prompts, though we recommend at  minimum, you add your own title and description. If you don’t want to fill in  a field, you can press enter. npm will leave fill these fields with default  values  or leave  them empty when it creates the  package.json  file.

After you run  npm  init  your  directory structure will  contain the following  files  and folders:

![](Images/image04919.jpeg)

npm  adds the  package.json  file  to the same level as  the src  directory.

Instructions  1.

Run  ls  in the terminal to see the  file structure of  your current directory.

 Checkpoint 2 Passed

2.

Use npm to create a new package.json file. We recommend you set  the  name  and  description  properties to the following  values:

• name  —  learning-babel

• description  —  Use  Babel to  transpile JavaScript  ES6  to ES5

Enter ls  into  the  terminal to  see the file  structure of  your current directory.  Notice  the  addition of package.json.

npm  init

In the last exercise, you wrote one command in your terminal to transpile  ES6 code to ES5\. In the next five exercises you will learn how to setup a  JavaScript project that transpiles code when you run  npm run build  from the  root  directory of a JavaScript project.

The first step is to place your ES6 JavaScript file in a directory called src.  From  your  root directory,  the path  to the ES6 file is ./src/main.js

The  initial  JavaScript project  file structure  is:

![](Images/image04920.jpeg)

Before  we install  Babel,  we  need  to  setup our  project to  use the  [node](https://docs.npmjs.com/getting-started/what-is-npm)

[package manager (npm)](https://docs.npmjs.com/getting-started/what-is-npm). Developers use npm to access and manage Node  packages. Node packages are directories that contain JavaScript code  written by other developers. You can use these packages to reduce  duplication  of  work and avoid bugs.

Before we can add Babel to our project directory, we need to run  npm init.  The  npm  init  command  creates a package.json  file in  the root directory.

A package.json file contains information about the current JavaScript  project.  Some of this information includes:

• Metadata — This includes a project title, description, authors, and  more.

• A list of node packages required for the project — If another  developer  wants to  run your  project,  npm looks

inside  package.json  and  downloads the  packages in  this list.

• Key-value pairs for command line scripts — You can use npm to run  these shorthand scripts to perform some process. In a later exercise,  we  will add a  script that runs  Babel and transpiles ES6  to ES5.

If you have Node installed on your computer, you can create  a  package.json  file by  typing  npm init  into  the  terminal.

The terminal prompts you to fill in fields for the project’s metadata (name,  description,  etc.)

You are not required to answer the prompts, though we recommend at  minimum, you add your own title and description. If you don’t want to fill in  a field, you can press enter. npm will leave fill these fields with default  values  or leave  them empty when it creates the  package.json  file.

After you run  npm  init  your  directory structure will  contain the following  files  and folders:

![](Images/image04921.jpeg)

![](Images/image04922.jpeg)

npm  adds the  package.json  file  to the same level as  the src  directory.

![](Images/image04923.jpeg)

1.

![](Images/image04564.jpeg)Run

Checkpoint 2  Passed

![](Images/image04924.jpeg)2.

in  the terminal  to see  the  file  structure of  your current  directory.

Use npm to create a new package.json file. We recommend you set  the  name  and  description  properties to the following  values:

• name  —  learning-babel

• description  —  Use  Babel to  transpile JavaScript  ES6  to ES5

Enter ls  into  the  terminal to  see the file  structure of  your current directory.  Notice  the  addition of package.json.

npm  init

In the last exercise, you wrote one command in your terminal to transpile  ES6 code to ES5\. In the next five exercises you will learn how to setup a  JavaScript project that transpiles code when you run  npm run build  from the  root  directory of a JavaScript project.

The first step is to place your ES6 JavaScript file in a directory called src.  From  your  root directory,  the path  to the ES6 file is ./src/main.js

The  initial  JavaScript project  file structure  is:

![](Images/image04925.jpeg)

Before we install Babel, we need to setup our project to use the [node](https://docs.npmjs.com/getting-started/what-is-npm)  [package manager (npm)](https://docs.npmjs.com/getting-started/what-is-npm). Developers use npm to access and manage Node  packages. Node packages are directories that contain JavaScript code  written by other developers. You can use these packages to reduce  duplication  of  work and avoid bugs.

Before we can add Babel to our project directory, we need to run  npm init.  The  npm  init  command  creates a package.json  file in  the root directory.

A package.json file contains information about the current JavaScript  project.  Some of this information includes:

• Metadata — This includes a project title, description, authors, and  more.

• A list of node packages required for the project — If another  developer  wants to  run your  project,  npm looks

inside  package.json  and  downloads the  packages in  this list.

• Key-value pairs for command line scripts — You can use npm to run  these shorthand scripts to perform some process. In a later exercise,  we  will add a  script that runs  Babel and transpiles ES6  to ES5.

If you have Node installed on your computer, you can create  a  package.json  file by  typing  npm init  into  the  terminal.

The terminal prompts you to fill in fields for the project’s metadata (name,  description,  etc.)

You are not required to answer the prompts, though we recommend at  minimum, you add your own title and description. If you don’t want to fill in  a field, you can press enter. npm will leave fill these fields with default  values  or leave  them empty when it creates the  package.json  file.

After you run  npm  init  your  directory structure will  contain the following  files  and folders:

![](Images/image04926.jpeg)

npm  adds the  package.json  file  to the same level as  the src  directory.

Instructions  1.

Run  ls  in the terminal to see the  file structure of  your current directory.

 Checkpoint 2 Passed

2.

Use npm to create a new package.json file. We recommend you set  the  name  and  description  properties to the following  values:

• name  —  learning-babel

• description  —  Use  Babel to  transpile JavaScript  ES6  to ES5

Enter ls  into  the  terminal to  see the file  structure of  your current directory.  Notice  the  addition of package.json.

npm  init

In the last exercise, you wrote one command in your terminal to transpile  ES6 code to ES5\. In the next five exercises you will learn how to setup a  JavaScript project that transpiles code when you run  npm run build  from the  root  directory of a JavaScript project.

The first step is to place your ES6 JavaScript file in a directory called src.  From  your  root directory,  the path  to the ES6 file is ./src/main.js

The  initial  JavaScript project  file structure  is:

![](Images/image04927.jpeg)

Before  we install  Babel,  we  need  to  setup our  project to  use the  [node](https://docs.npmjs.com/getting-started/what-is-npm)

[package manager (npm)](https://docs.npmjs.com/getting-started/what-is-npm). Developers use npm to access and manage Node  packages. Node packages are directories that contain JavaScript code  written by other developers. You can use these packages to reduce  duplication  of  work and avoid bugs.

Before we can add Babel to our project directory, we need to run  npm init.  The  npm  init  command  creates a package.json  file in  the root directory.

A package.json file contains information about the current JavaScript  project.  Some of this information includes:

• Metadata — This includes a project title, description, authors, and  more.

• A list of node packages required for the project — If another  developer  wants to  run your  project,  npm looks

inside  package.json  and  downloads the  packages in  this list.

• Key-value pairs for command line scripts — You can use npm to run  these shorthand scripts to perform some process. In a later exercise,  we  will add a  script that runs  Babel and transpiles ES6  to ES5.

If you have Node installed on your computer, you can create  a  package.json  file by  typing  npm init  into  the  terminal.

The terminal prompts you to fill in fields for the project’s metadata (name,  description,  etc.)

You are not required to answer the prompts, though we recommend at  minimum, you add your own title and description. If you don’t want to fill in  a field, you can press enter. npm will leave fill these fields with default  values  or leave  them empty when it creates the  package.json  file.

After you run  npm  init  your  directory structure will  contain the following  files  and folders:

![](Images/image04928.jpeg)

npm  adds the  package.json  file  to the same level as  the src  directory.

Instructions  1.

Run  ls  in the terminal to see the  file structure of  your current directory.

 Checkpoint 2 Passed

2.

Use npm to create a new package.json file. We recommend you set  the  name  and  description  properties to the following  values:

• name  —  learning-babel

• description  —  Use  Babel to  transpile JavaScript  ES6  to ES5

Enter ls  into  the  terminal to  see the file  structure of  your current directory.  Notice  the  addition of package.json.

npm  init

In the last exercise, you wrote one command in your terminal to transpile  ES6  code to  ES5.  In  the next five exercises you  will learn how  to setup  a

JavaScript project that transpiles code when you run  npm run build  from the  root  directory of a JavaScript project.

The first step is to place your ES6 JavaScript file in a directory called src.  From  your  root directory,  the path  to the ES6 file is ./src/main.js

The  initial  JavaScript project  file structure  is:

![](Images/image04929.jpeg)

Before we install Babel, we need to setup our project to use the [node](https://docs.npmjs.com/getting-started/what-is-npm)  [package manager (npm)](https://docs.npmjs.com/getting-started/what-is-npm). Developers use npm to access and manage Node  packages. Node packages are directories that contain JavaScript code  written by other developers. You can use these packages to reduce  duplication  of  work and avoid bugs.

Before we can add Babel to our project directory, we need to run  npm init.  The  npm  init  command  creates a package.json  file in  the root directory.

A package.json file contains information about the current JavaScript  project.  Some of this information includes:

• Metadata — This includes a project title, description, authors, and  more.

• A list of node packages required for the project — If another  developer  wants to  run your  project,  npm looks

inside  package.json  and  downloads the  packages in  this list.

• Key-value pairs for command line scripts — You can use npm to run  these shorthand scripts to perform some process. In a later exercise,  we  will add a  script that runs  Babel and transpiles ES6  to ES5.

If you have Node installed on your computer, you can create  a  package.json  file by  typing  npm init  into  the  terminal.

The terminal prompts you to fill in fields for the project’s metadata (name,  description,  etc.)

You are not required to answer the prompts, though we recommend at  minimum,  you  add  your  own  title  and  description.  If  you  don’t  want  to  fill  in

a field, you can press enter. npm will leave fill these fields with default  values  or leave  them empty when  it creates the  package.json  file.

After you run  npm  init  your  directory structure will  contain the following  files  and folders:

![](Images/image04930.jpeg)

npm  adds the  package.json  file  to the same level as  the src  directory.

Instructions  1.

Run  ls  in the terminal to see the  file structure of  your current directory.

 Checkpoint 2 Passed

2.

Use npm to create a new package.json file. We recommend you set  the  name  and  description  properties to the following  values:

• name  —  learning-babel

• description  —  Use  Babel to  transpile JavaScript  ES6  to ES5

Enter ls  into  the  terminal to  see the file  structure of  your current directory.  Notice  the  addition of package.json.

Install  Node Packages

We  use  the  npm  install  command  to  install new Node packages locally.  The  install  command  creates  a  folder  called node_modules and copies  the package files to it. The  install  command also installs all of the  dependencies  for  the given package.

To  install Babel, we  need to  npm install  two packages,  babel-cli  and  babel-  preset-env. However, npm installs over one hundred other packages that  are  dependencies for  Babel to run properly.

We  install Babel  with the  following two  commands:

![](Images/image04931.jpeg)![](Images/image04932.jpeg)package includes command line Babel tools, and the  package  has  the  code  that  maps  any  JavaScript  feature,  ES6  and

above  (ES6+),  to ES5.

![](Images/image04933.jpeg)The  called

flag  instructs npm to  add each  package to  a property

in  package.json. Once  the project’s dependencies

are listed in  devDependencies, other developers can run your project without  installing  each package separately. Instead,  they can simply  run  npm

install  —  it  instructs npm to look inside  package.json  and download all of  the  packages listed  in  devDependencies.

Once  you  npm install  packages, you can find the Babel  packages and all  their dependencies in the node_modules folder. The new directory  structure  contains the  following:

![](Images/image04934.jpeg)

The  ...  in  the  file  structure above is a  placeholder  for  100+  packages that  npm installed.

Instructions  1.

Enter ls  into the terminal to view the current directory’s file  structure.

 Checkpoint 2 Passed

2.

Use  npm  with the  -D  flag to install the Babel command  line package  and  add it to the  devDependencies  property  in  package.json.

 Checkpoint 3 Passed

3.

Use  npm with the  -D  flag to install the  Babel preset environment  package  and add it to the  devDependencies  property in package.json.

Enter ls  into  the  terminal to  see the file  structure of  your current directory.  Notice the  addition of node_modules.

You can also see the new folder by clicking on the file navigation button  above  the text editor.

.babelrc

Now that you’ve downloaded the Babel packages, you need to specify the  version  of the  source JavaScript code.

You can specify the initial JavaScript version inside of a file named .babelrc.  In  your root directory, you can  run  touch .babelrc  to  create this file.

Your  project  directory  contains the following  folders and  files:

![](Images/image04935.jpeg)

Inside .babelrc you need to define the preset for your source JavaScript file.  The  preset  specifies the version  of  your initial JavaScript file.

Usually, you want to transpile JavaScript code from versions ES6 and later  (ES6+) to ES5\. From this point on, we will refer to our source code as ES6+,  because  Ecma  introduces new  syntax  with each  new version  of  JavaScript.

To specify that we are transpiling code from an ES6+ source, we have to  add  the following JavaScript object into .babelrc:

![](Images/image04936.jpeg)

When you run Babel, it looks in .babelrc to determine the version of the  initial JavaScript file. In this case,  ["env"]  instructs Babel to transpile any  code  from versions ES6 and later.

Instructions  1.

In  the  root directory, use  touch  to create a new  .babelrc  file.

 Checkpoint 2 Passed

2.

Open the .babelrc file and add an object that specifies the preset to  "env".  Run  the code once you’ve  added the  object.

Babel  Source Lib

There’s one last step before we can transpile our code. We need to specify  a  script  in  package.json  that initiates the  ES6+ to  ES5 transpilation.

Inside  of  the  package.json  file, there  is  a property  named  "scripts"  that  holds  an object  for specifying command  line shortcuts. It  looks like this:

![](Images/image04937.jpeg)

In the code above, the  "scripts"  property contains an object with one  property called  "test". Below the  "test"  property, we  will add  a script  that  runs  Babel like this:

![](Images/image04938.jpeg)

In the "scripts"  object above, we add a property called  "build". The  property’s value,  "babel src -d lib", is a command line method that  transpiles ES6+ code to ES5\. Let’s consider each argument in the method  call:

![](Images/image04939.jpeg)• —  The Babel  command call  responsible for  transpiling  code.

![](Images/image04940.jpeg)• — Instructs Babel to transpile all JavaScript code inside  the  src  directory.

• —  Instructs  Babel  to write  the  transpiled code  to  a directory.

• —  Babel writes  the transpiled  code to a  directory called  lib.

In  the  next exercise, we’ll  run the  babel  src  -d  lib  method to transpile our  ES6+ code.

Instructions  1.

In  package.json, add  a script  called  "build".

When  run,  the  "build"  script should use Babel to transpile  JavaScript code  inside  of the src  folder  and write it to a  folder called  lib.

Don’t  forget to add  a comma after  the  “test” script.

![](Images/image04941.jpeg)

Build

We’re ready to transpile our code! In the last exercise, we wrote the  following  script in package.json:

"build":  "babel  src  -d  lib"   Now, we need to call  "build"  from the command line to transpile and write  ES5  code to  a directory called  lib.

From  the command line,  we type:

npm  run  build

The  command  above  runs the  build  script in  package.json.

Babel writes the ES5 code to a file named main.js (it’s always the same  name as the original file), inside of a folder called  lib. The resulting  directory  structure is:

![](Images/image04942.jpeg)

Notice, the directory contains a new folder named lib, with one file,  called main.js.

The npm run build  command will transpile all JavaScript files inside of  the src folder. This is helpful as you build larger JavaScript projects —  regardless of the number of JavaScript files, you only need to run one  command  (npm run  build) to transpile  all of your code.

Instructions  1.

Transpile the  ES6+ code to  lib  using the  build  command.

Once  you’ve done this,  navigate to the new  lib  folder and  open  main.js.

Review

In this lesson, you learned about browser compatibility and transpilation. Let’s review  the key  concepts:

• ES5 — The old JavaScript version that is supported by all modern web  browsers.

• ES6 — The new(er) JavaScript version that is not supported by all modern web  browsers. The syntax is more readable, similar to other programming  languages,  and addresses the  source of common bugs in ES5.

• caniuse.com — a website you can use to look up HTML, CSS, and JavaScript  browser  compatibility information.

• Babel  — A  JavaScript package  that transpiles  JavaScript  ES6+  code to  ES5.

• npm  init  — A terminal command that creates a package.json  file.

• package.json  —  A  file that  contains  information about  a  JavaScript project.

• npm  install  —  A command  that installs  Node packages.

• babel-cli  — A Node package  that contains command line  tools for  Babel.

• babel-preset-env  —  A Node package that contains ES6+ to ES5 syntax  mapping  information.

• .babelrc  — A  file that  specifies  the version of  the JavaScript  source  code.

• "build"  script — A package.json  script that you use to tranpsile ES6+ code  to  ES5.

• npm  run  build  — A command  that runs the  build  script and  transpiles  ES6+  code  to ES5.

Introduction

In web development, asynchronous programming is notorious for being a  challenging  topic.

An asynchronous operation is one that allows the computer to “move on” to other  tasks while waiting for the asynchronous operation to complete. Asynchronous  programming means that time-consuming operations don’t have to bring everything  else  in  our programs to a halt.

There are countless examples of asynchronicity in our everyday lives. Cleaning our  house, for example, involves asynchronous operations such as a dishwasher washing  our dishes or a washing machine washing our clothes. While we wait on the  completion  of those operations, we’re free to do other  chores.

Similarly, web development makes use of asynchronous operations. Operations like  making a network request or querying a database can be time-consuming, but  JavaScript  allows us to  execute other tasks while  awaiting their completion.

This lesson will teach you how modern JavaScript handles asynchronicity using  the  Promise  object, introduced with ES6\. Let’s get  started!

What  is a Promise?

Promises are objects that represent the eventual outcome of an asynchronous  operation. A  Promise  object can be in one  of three states:

• Pending:  The initial state— the  operation has  not completed yet.

• Fulfilled: The operation has completed successfully and the promise now has  a resolved value. For example, a request’s promise might resolve with a JSON  object  as its value.

• Rejected: The operation has failed and the promise has a reason for the  failure. This reason is usually an  Error  of some  kind.

We refer to a promise as settled if it is no longer pending— it is either fulfilled or  rejected.  Let’s think of a  dishwasher as  having  the states of a promise:

• Pending:  The  dishwasher  is  running but  has not  completed  the washing  cycle.

• Fulfilled: The dishwasher has completed the washing cycle and is full of clean  dishes.

• Rejected: The dishwasher encountered a problem (it didn’t receive soap!) and  returns  unclean dishes.

If our dishwashing promise is fulfilled, we’ll be able to perform related tasks, such as  unloading the clean dishes from the dishwasher. If it’s rejected, we can take alternate  steps,  such as running  it  again with soap  or  washing  the dishes by hand.

All promises eventually settle, enabling us to write logic for what to do if the promise  fulfills  or  if it rejects.

Constructing  a  Promise Object

Let’s  construct  a  promise!  To  create a  new  Promise  object, we use  the  new  keyword and the  Promise  constructor  method:

![](Images/image04943.jpeg)

The  Promise  constructor  method  takes a  function parameter  called

the executor function which runs automatically when the constructor is  called. The executor function generally starts an asynchronous operation  and  dictates how the promise  should  be settled.

The executor function has two function parameters, usually referred to as  the  resolve()  and  reject()  functions. The  resolve()  and  reject()  functions  aren’t defined by the programmer. When the  Promise  constructor runs,  JavaScript will pass its own  resolve()  and  reject()  functions into the  executor  function.

• resolve  is  a  function with one argument.  Under  the hood, if  invoked,  resolve()  will change the promise’s status

from  pending  to  fulfilled,  and the  promise’s resolved value  will be set  to  the  argument passed into  resolve().

• reject  is a function that takes a reason or error as an argument.  Under the hood,  if  invoked,  reject()  will change  the promise’s status  from  pending  to  rejected, and the promise’s rejection reason will be  set  to the  argument passed into  reject().

Let’s look at  an example  executor  function in a  Promise  constructor:

![](Images/image04944.jpeg)

![](Images/image04945.jpeg)

Let’s  break down  what’s happening above:

![](Images/image04946.jpeg)• ![](Images/image04947.jpeg)We  declare a  variable

•

the

is constructed using  constructor  method.

which  is

•

as  parameters:

is passed to the constructor and has two functions  and  reject.

• If  someCondition  evaluates  to  true, we  invoke  resolve()  with  the  string  'I resolved!'

• If  not, we invoke  reject()  with  the string  'I  rejected!'

In our example,  myFirstPromise  resolves or rejects based on a simple  condition, but, in practice, promises settle based on the results of  asynchronous operations. For example, a database request may fulfill with  the data from a query or reject with an error thrown. In this exercise, we’ll  construct promises which resolve synchronously to more easily understand  how  they work.

Instructions  1.

You’ll be writing your code in the code-editor, but we won’t be running it  until the final step. To check your code for a step, you can press the “Check  Work”  button.

We’re going to create a promise representing ordering sunglasses from an  online store. First, create the function,  myExecutor(). Later on, you’ll pass this  function into  the  Promise  constructor.

myExecutor()  should:

• Have  two parameters:  resolve  and  reject

• Check if the  sunglasses  property on  the  inventory  object  has a  value  greater  than zero

• If  it  does,  myExecutor()  should invoke  resolve()  with  the  string  'Sunglasses  order processed.'

• ![](Images/image04948.jpeg)If  it does  not,should  invoke  reject()  with the

string  'That  item  is  sold out.'

When  you’re  ready, press  the “Check  Work” button.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Create a function,  orderSunglasses(). This function should have no  parameters. It should return a new promise constructed by passing  your myExecutor()  function  into the  Promise  constructor.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Create  a variable  orderPromise  assigned to the  returned value of  your orderSunglasses()  function.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

At  the bottom of your app.js  file, log  orderPromise  to  the  console.

 Checkpoint 5 Passed

5.

![](Images/image04949.jpeg)In this exercise and throughout the lesson, we’ll provide you with a bash  terminal  to execute  your  code.  To  run  the  app.js  program, you’ll type  node

![](Images/image04950.jpeg)app.js  in the terminal and hit  of  the  program  in  the  terminal.

(or  return).  You’ll  be able  to  see  the  output

![](Images/image04951.jpeg)Let’s try  it! Type  node  app.js  in the  terminal  and hit  enter.

If you’d like, you can see an alternate output by changing  the sunglasses  property in the  inventory  object to  0  and  executing app.js  from the terminal again.

When  you’re ready  to move  on, press  the “Check  Work” button.

![](Images/image04952.jpeg)

![](Images/image04953.jpeg)

The  Node  setTimeout() Function

Knowing how to construct a promise is useful, but most of the time,  knowing how to consume, or use, promises will be key. Rather than  constructing promises, you’ll be handling  Promise  objects returned to  you as  the result of an asynchronous operation. These promises will start off  pending  but settle eventually.

Moving forward, we’ll be simulating this by providing you with functions  that return promises which settle after some time. To accomplish this, we’ll  be using setTimeout().  setTimeout()  is a Node API (a comparable API is  provided by web browsers) that uses callback functions to schedule tasks to  be performed after a delay.  setTimeout()  has two parameters: a callback  function  and a delay  in  milliseconds.

![](Images/image04954.jpeg)

Here, we invoke  setTimeout()  with the callback

function delayedHello()  and  2000.  In at least two seconds  delayedHello()  will

be invoked. But why is it “at least” two seconds and not exactly two  seconds?

This delay  is  performed asynchronously—the  rest of  our  program  won’t  stop executing during the delay. Asynchronous JavaScript uses something  called  the event-loop. After two  seconds,  delayedHello()  is added  to a  line of  code waiting to be run. Before it can run, any synchronous code from the  program will run. Next, any code in front of it in the line will run. This means  it might be more than two seconds before  delayedHello()  is actually  executed.

Let’s  look at how we’ll be using  setTimeout()  to  construct asynchronous  promises:

![](Images/image04955.jpeg)

In  the  example  code, we  invoked  returnPromiseFunction()  which returned a  promise. We assigned that promise to the variable  prom. Similar to the  asynchronous  promises you  may encounter in  production,  prom  will  initially  have  a  status of pending.

Let’s  explore  setTimeout()  a  bit more.

Instructions  1.

Create a function,  usingSTO(). Your  usingSTO()  function should have no  parameters. Inside the function body, it should print a string to the console.  This can be any string you want (as long as it’s not either “This is the first  line  of synchronous code.” or  “This is the last  line of synchronous code.”).

Check  your  work to move  on to the  next  step.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

![](Images/image04956.jpeg)

![](Images/image04957.jpeg)Checkpoint 3  Passed

Stuck?  Get a hint

3.

Take  a  moment to  predict the  output of  this program.

![](Images/image04958.jpeg)Whenever  you’re  ready, type  node  app.js  in  the  terminal  and  hit  enter.

See if the program’s output in the terminal lines up with what you  expected.

![](Images/image04959.jpeg)

Consuming  Promises

The initial state of an asynchronous promise is  pending, but we have a guarantee that  it will settle. How do we tell the computer what should happen then? Promise objects  come with an aptly named  .then()  method. It allows us to say, “I have a promise,  when  it  settles,  then  here’s what I want to  happen…”

In  the case  of  our dishwasher  promise,  the dishwasher  will  run then:

• If our promise rejects, this means we have dirty dishes, and we’ll add soap and  run  the dishwasher again.

• If our promise fulfills, this means we have clean dishes, and we’ll put the  dishes away.

.then()  is a higher-order  function— it takes two callback functions as arguments. We  refer to these callbacks as handlers. When the promise settles, the appropriate  handler  will be invoked with that settled value.

• The first handler, sometimes called  onFulfilled, is a success handler, and it  should  contain the logic for the promise resolving.

• The second handler, sometimes called  onRejected, is a failure handler, and it  should  contain the logic for the promise rejecting.

We can invoke  .then()  with one, both, or neither handler! This allows for flexibility,  but it can also make for tricky debugging. If the appropriate handler is not provided,  instead of throwing an error,  .then()  will just return a promise with the same settled  value as the promise it was called on. One important feature of  .then()  is that it  always returns a promise. We’ll return to this in more detail in a later exercise and  explore  why it’s so important.

Success  and Failure  Callback Functions

To handle a “successful” promise, or a promise that resolved, we  invoke  .then()  on the promise, passing in a success handler callback  function:

![](Images/image04960.jpeg)

Let’s  break down  what’s happening  in the  example code:

• prom  is a promise which will resolve  to  'Yay!'.

• We define a function,  handleSuccess(), which prints the argument  passed to it.

• We  invoke  prom‘s  .then()  function  passing in  our  handleSuccess()  function.

• Since  prom  resolves,  handleSuccess()  is invoked with  prom‘s resolved  value,  'Yay',  so  'Yay'  is  logged  to  the  console.

With typical promise consumption, we won’t know whether a promise will  resolve or reject, so we’ll need to provide the logic for either case. We can  pass  both a success callback and a  failure callback to  .then().

![](Images/image04961.jpeg)

Let’s  break down  what’s happening  in the  example code:

• prom  is a promise which will randomly either  resolve with  'Yay!'  or  reject  with  'Ohhh noooo!'.

• ![](Images/image04962.jpeg)We pass two handler functions to  .then(). The first will be invoked  with 'Yay!'  if  the  promise resolves,  and  the second  will be  invoked  with 'Ohhh noooo!'  if the promise rejects.

Note: The success callback is sometimes called the “success handler function”  or the onFulfilled  function. The failure callback is sometimes called the  “failure handler function” or the  onRejected  function.

Let’s  write  some  success  and  failure  callbacks!

![](Images/image04963.jpeg)

1.

Take  a look  at  the  provided code  in app.js. We  use  require()  to include the  function checkInventory()  from library.js. It builds on the  logic of

the  orderSunglasses()  function  you  wrote  in  a  previous  exercise.

• checkInventory()  takes  in  an  array  representing an  order  and  returns  a promise.

• If every item in the order is in stock, that promise resolves with  the  value  "Thank you.  Your  order was  successful."

• Otherwise, the promise rejects with the value  "We're sorry.  Your order could not be completed because some items are sold  out".

We  used  setTimeout()  to  ensure  that the  checkInventory()  promise  settles  asynchronously.

If you’d like, look at the library.js file to see how it works. Press “Check  Work”  when you’re ready to move on.

 Checkpoint 2 Passed

![](Images/image04964.jpeg)2.

Write a function,  handleSuccess(). You’ll use this function later on as your  success  handler.  handleSuccess()  should  have  one  parameter,  representing  a  resolved value. Inside the body of  handleSuccess(), log the parameter to the  console.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Write a function,  handleFailure(). You’ll use this function later on as your  failure  handler.  handleFailure()  should  have  one  parameter,  representing  a  rejection reason. Inside the body of  handleFailure(), log the parameter to  the  console.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Invoke  checkInventory()  with  order.  This  will  return  a promise. Attach

a  .then()  function  to this. Pass into  .then()  the two handlers  you wrote as  callback  functions.

 Checkpoint 5 Passed

Stuck?  Get a hint

![](Images/image04965.jpeg)5.

Type  node  app.js  in the  terminal  and  hit  enter.

![](Images/image04966.jpeg)

Using  catch()  with  Promises

One way to write cleaner code is to follow a principle called separation of  concerns. Separation of concerns means organizing code into distinct  sections each handling a specific task. It enables us to quickly navigate our  code  and know where to  look if  something isn’t working.

Remember,  .then()  will return a  promise  with the same settled value  as the  promise it was called on if no appropriate handler was provided. This  implementation allows us to separate our resolved logic from our rejected  logic. Instead of passing both handlers into one  .then(), we can chain a  second .then()  with a failure handler to a first  .then()  with a success  handler  and both cases will be handled.

![](Images/image04967.jpeg)

Since JavaScript doesn’t mind whitespace, we follow a common convention  of putting each part of this chain on a new line to make it easier to read. To  create  even more readable code, we  can use a different promise

function:  .catch().

The  .catch()  function takes only  one argument,  onRejected.  In the case  of a  rejected promise, this failure handler will be invoked with the reason for  rejection. Using  .catch()  accomplishes  the same thing as  using

![](Images/image04968.jpeg)a .then()  with only a failure handler.  Let’s  look  at  an  example  using  .catch():

Let’s  break down  what’s happening  in the  example code:

• prom  is a promise which randomly either  resolves with  'Yay!'  or  rejects  with  'Ohhh  noooo!'.

• We  pass  a  success  handler to  .then()  and  a failure handler  to  .catch().

• If the promise resolves,  .then()‘s success handler will be invoked  with  'Yay!'.

• If the promise rejects,  .then()  will return a promise with the same  rejection reason as the original promise and  .catch()‘s failure handler  will  be invoked with that rejection reason.

Let’s practice writing  .catch()  functions.

Instructions  1.

We’re going to refactor the functionality of the previous exercise but this  time we’ll use  .catch()! First invoke the  checkInventory()  function with  the  order.  Remember,  this function will return a  promise.

 Checkpoint 2 Passed

2.

![](Images/image04969.jpeg)Add ato  the  returned promise.  Pass in the  success

handler  handleSuccess().

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Add  a  .catch()  to  the  returned  promise.  Pass  in  the  failure  handler  handleFailure().

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

![](Images/image04970.jpeg)We set our inventory of sunglasses to  0, so the order shouldn’t go through.  Let’s make sure our code has the expected results. Type  node app.js  in the  terminal and hit  enter.

![](Images/image04971.jpeg)

Chaining  Multiple Promises

One common pattern we’ll see with asynchronous programming is multiple  operations which depend on each other to execute or that must be  executed in a certain order. We might make one request to a database and  use the data returned to us to make another request and so on! Let’s  illustrate  this with another  cleaning example, washing  clothes:

We take our dirty clothes and put them in the washing machine. If the  clothes are cleaned, then we’ll want to put them in the dryer. After the  dryer runs, if the clothes are dry, then we can fold them and put them  away.

This process of chaining promises together is called composition. Promises  are designed with composition in mind! Here’s a simple promise chain in  code:

![](Images/image04972.jpeg)

Let’s  break down  what’s happening  in the example:

• We  invoke a  function  firstPromiseFunction()  which returns a promise.

• We  invoke  .then()  with  an anonymous function  as the success  handler.

• Inside the success handler we return a new promise— the result of  invoking a second function,  secondPromiseFunction()  with the first  promise’s  resolved value.

• We  invoke  a second  .then()  to  handle the logic for  the second  promise  settling.

• Inside that  .then(), we have a success handler which will log the  second  promise’s resolved value to the console.

In  order for  our chain  to work properly,  we had to  return  the

promise  secondPromiseFunction(firstResolveVal). This ensured that the  return value of the first  .then()  was our second promise rather than the  default  return  of  a  new  promise  with  the  same  settled  value  as  the  initial.

Let’s  write  some  promise  chains!

Instructions  1.

Take  a  look at  the provided code.  We  require in three

functions:  checkInventory(),  processPayment(),  shipOrder(). These functions  each  return  a promise.

checkInventory()  expects  an  order  argument  and  returns  a promise.  If  there  are enough items in stock to fill the order, the promise will resolve to an  array.  The first element in the  resolved value  array will be the

same  order  and the second  element will  be  the total cost of the order  as a  number.

processPayment()  expects an array argument with the  order  as the first  element and the purchase total as the second. This function returns a  promise. If there is a large enough balance on the giftcard associated with  the order, it will resolve to an array. The first element in the resolved value  array will be the same  order  and the second element will be a tracking  number.

shipOrder()  expects an array argument with the  order  as the first element  and a tracking number as the second. It returns a promise which resolves to  a  string  confirming the order has shipped.

If you’d like, look at the library.js file to see how these functions work.  Press  “Check  Work”  when  you’re  ready  to  move  on  to  the  next  checkpoint.

 Checkpoint 2 Passed

2.

We set up a promise chain but it’s missing a couple important lines of code  to  make it function  properly.

We  invoked  checkInventory()  with  order  and chained a  .then()  function to it.  This .then()  has an anonymous function as its success handler, but it’s  missing a  return  statement.

The  success  handler should  return a  processPayment()  promise.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

We  have  a second  .then()  function  on the chain. This  .then()  also has an  anonymous  function  as its success handler and  is missing

a  return  statement.

The  success  handler should  return a  shipOrder()  promise.

 Checkpoint 4 Passed

Stuck?  Get a hint

![](Images/image04973.jpeg)4.

Type  node  app.js  in the  terminal  and  hit  enter.

Chaining  Multiple Promises

One common pattern we’ll see with asynchronous programming is multiple  operations which depend on each other to execute or that must be  executed in a certain order. We might make one request to a database and  use the data returned to us to make another request and so on! Let’s  illustrate  this with another  cleaning example, washing  clothes:

We take our dirty clothes and put them in the washing machine. If the  clothes are cleaned, then we’ll want to put them in the dryer. After the  dryer runs, if the clothes are dry, then we can fold them and put them  away.

This process of chaining promises together is called composition. Promises  are designed with composition in mind! Here’s a simple promise chain in  code:

![](Images/image04974.jpeg)

Let’s  break down  what’s happening  in the example:

• We  invoke a  function  firstPromiseFunction()  which returns a promise.

• We  invoke  .then()  with  an anonymous function  as the success  handler.

• Inside the success handler we return a new promise— the result of  invoking a second function,  secondPromiseFunction()  with the first  promise’s  resolved value.

• We  invoke  a second  .then()  to  handle the logic for  the second  promise  settling.

• Inside that  .then(), we have a success handler which will log the  second  promise’s resolved value to the console.

In  order for  our chain  to work properly,  we had to  return  the

promise  secondPromiseFunction(firstResolveVal). This ensured that the  return value of the first  .then()  was our second promise rather than the  default  return  of  a  new  promise  with  the  same  settled  value  as  the  initial.

Let’s  write  some  promise  chains!

Instructions  1.

Take  a  look at  the provided code.  We  require in three

functions:  checkInventory(),  processPayment(),  shipOrder(). These functions  each  return  a promise.

checkInventory()  expects  an  order  argument  and  returns  a promise.  If  there  are enough items in stock to fill the order, the promise will resolve to an  array.  The first element in the  resolved value  array will be the

same  order  and the second  element will  be  the total cost of the order  as a  number.

processPayment()  expects an array argument with the  order  as the first  element and the purchase total as the second. This function returns a  promise. If there is a large enough balance on the giftcard associated with  the order, it will resolve to an array. The first element in the resolved value  array will be the same  order  and the second element will be a tracking  number.

shipOrder()  expects an array argument with the  order  as the first element  and a tracking number as the second. It returns a promise which resolves to  a  string  confirming the order has shipped.

If you’d like, look at the library.js file to see how these functions work.  Press  “Check  Work”  when  you’re  ready  to  move  on  to  the  next  checkpoint.

 Checkpoint 2 Passed

2.

We set up a promise chain but it’s missing a couple important lines of code  to  make it function  properly.

We  invoked  checkInventory()  with  order  and chained a  .then()  function to it.  This .then()  has an anonymous function as its success handler, but it’s  missing a  return  statement.

![](Images/image04975.jpeg)The  success handler should return  apromise.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

We  have  a second  .then()  function  on the chain. This  .then()  also has an  anonymous  function  as its success handler and  is missing

a  return  statement.

The  success  handler should  return a  shipOrder()  promise.

 Checkpoint 4 Passed

Stuck?  Get a hint

![](Images/image04976.jpeg)4.

Type node  app.js  in  the  terminal and  hit  enter.  Chaining  Multiple Promises

One common pattern we’ll see with asynchronous programming is multiple  operations which depend on each other to execute or that must be  executed in a certain order. We might make one request to a database and  use the data returned to us to make another request and so on! Let’s  illustrate  this with another  cleaning example, washing  clothes:

We take our dirty clothes and put them in the washing machine. If the  clothes are cleaned, then we’ll want to put them in the dryer. After the  dryer runs, if the clothes are dry, then we can fold them and put them  away.

This process of chaining promises together is called composition. Promises  are designed with composition in mind! Here’s a simple promise chain in  code:

![](Images/image04977.jpeg)

Let’s  break down  what’s happening  in the example:

• We  invoke a  function  firstPromiseFunction()  which returns a promise.

• We  invoke  .then()  with  an anonymous function  as the success  handler.

• Inside the success handler we return a new promise— the result of  invoking a second function,  secondPromiseFunction()  with the first  promise’s  resolved value.

• We  invoke  a second  .then()  to  handle the logic for  the second  promise  settling.

• Inside that  .then(), we have a success handler which will log the  second  promise’s resolved value to the console.

In  order for  our chain  to work properly,  we had to  return  the

promise  secondPromiseFunction(firstResolveVal). This ensured that the  return value of the first  .then()  was our second promise rather than the  default  return  of  a  new  promise  with  the  same  settled  value  as  the  initial.

Let’s  write  some  promise  chains!

Instructions  1.

Take  a  look at  the provided code.  We  require in three

functions:  checkInventory(),  processPayment(),  shipOrder(). These functions  each  return  a promise.

checkInventory()  expects  an  order  argument  and  returns  a promise.  If  there  are enough items in stock to fill the order, the promise will resolve to an  array.  The first element in the  resolved value  array will be the

same  order  and the second  element will  be  the total cost of the order  as a  number.

processPayment()  expects an array argument with the  order  as the first  element and the purchase total as the second. This function returns a  promise. If there is a large enough balance on the giftcard associated with  the order, it will resolve to an array. The first element in the resolved value  array will be the same  order  and the second element will be a tracking  number.

shipOrder()  expects an array argument with the  order  as the first element  and a tracking number as the second. It returns a promise which resolves to  a  string  confirming the order has shipped.

If you’d like, look at the library.js file to see how these functions work.  Press  “Check  Work”  when  you’re  ready  to  move  on  to  the  next  checkpoint.

 Checkpoint 2 Passed

2.

We set up a promise chain but it’s missing a couple important lines of code  to  make it function  properly.

We  invoked  checkInventory()  with  order  and chained a  .then()  function to it.  This .then()  has an anonymous function as its success handler, but it’s  missing a  return  statement.

The  success  handler should  return a  processPayment()  promise.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

We  have  a second  .then()  function  on the chain. This  .then()  also has an  anonymous  function  as its success handler and  is missing

a  return  statement.

The  success  handler should  return a  shipOrder()  promise.

 Checkpoint 4 Passed

Stuck?  Get a hint

![](Images/image04978.jpeg)4.

Type  node  app.js  in the  terminal  and  hit  enter.

Chaining  Multiple Promises

One common pattern we’ll see with asynchronous programming is multiple  operations which depend on each other to execute or that must be  executed in a certain order. We might make one request to a database and  use the data returned to us to make another request and so on! Let’s  illustrate  this with another  cleaning example, washing  clothes:

We take our dirty clothes and put them in the washing machine. If the  clothes are cleaned, then we’ll want to put them in the dryer. After the  dryer runs, if the clothes are dry, then we can fold them and put them  away.

This process of chaining promises together is called composition. Promises  are designed with composition in mind! Here’s a simple promise chain in  code:

![](Images/image04979.jpeg)

Let’s  break down  what’s happening  in the example:

• We  invoke a  function  firstPromiseFunction()  which returns a promise.

• We  invoke  .then()  with  an anonymous function  as the success  handler.

• Inside the success handler we return a new promise— the result of  invoking a second function,  secondPromiseFunction()  with the first  promise’s  resolved value.

• We  invoke  a second  .then()  to  handle the logic for  the second  promise  settling.

• Inside that  .then(), we have a success handler which will log the  second  promise’s resolved value to the console.

In  order for  our chain  to work properly,  we had to  return  the

promise  secondPromiseFunction(firstResolveVal). This ensured that the  return value of the first  .then()  was our second promise rather than the  default  return  of  a  new  promise  with  the  same  settled  value  as  the  initial.

Let’s  write  some  promise  chains!

Instructions  1.

Take  a  look at  the provided code.  We  require in three

functions:  checkInventory(),  processPayment(),  shipOrder(). These functions  each  return  a promise.

checkInventory()  expects  an  order  argument  and  returns  a promise.  If  there  are enough items in stock to fill the order, the promise will resolve to an  array.  The first element in the  resolved value  array will be the

same  order  and the second  element will  be  the total cost of the order  as a  number.

processPayment()  expects an array argument with the  order  as the first  element and the purchase total as the second. This function returns a  promise. If there is a large enough balance on the giftcard associated with  the order, it will resolve to an array. The first element in the resolved value  array will be the same  order  and the second element will be a tracking  number.

shipOrder()  expects an array argument with the  order  as the first element  and a tracking number as the second. It returns a promise which resolves to  a  string  confirming the order has shipped.

If you’d like, look at the library.js file to see how these functions work.  Press  “Check  Work”  when  you’re  ready  to  move  on  to  the  next  checkpoint.

 Checkpoint 2 Passed

2.

We set up a promise chain but it’s missing a couple important lines of code  to  make it function  properly.

We  invoked  checkInventory()  with  order  and chained a  .then()  function to it.  This .then()  has an anonymous function as its success handler, but it’s  missing a  return  statement.

The  success  handler should  return a  processPayment()  promise.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

We  have  a second  .then()  function  on the chain. This  .then()  also has an  anonymous  function  as its success handler and  is missing

a  return  statement.

The  success  handler should  return a  shipOrder()  promise.

 Checkpoint 4 Passed

Stuck?  Get a hint

![](Images/image04980.jpeg)4.

Type  node  app.js  in the  terminal  and  hit  enter.

![](Images/image04981.jpeg)

![](Images/image04982.jpeg)

Avoiding  Common  Mistakes

Promise composition allows for much more readable code than the nested  callback syntax that preceded it. However, it can still be easy to make  mistakes. In this exercise, we’ll go over two common mistakes with promise  composition.

Mistake  1:  Nesting  promises instead  of chaining  them.

![](Images/image04983.jpeg)

Let’s  break down  what’s happening in  the above code:

![](Images/image04984.jpeg)• We invoke

• We invoke

which returns a promise.  with  a  success handler.

• Inside  the success handler,  we

invoke  returnsSecondValue()  with  firstResolveVal  which  will  return  a  new  promise.

• We  invoke  a second  .then()  to  handle the logic for  the second  promise  settling  all inside  the  first  then()!

• Inside that second  .then(), we have a success handler which will log  the  second  promise’s resolved value  to the console.

Instead of having a clean chain of promises, we’ve nested the logic for one  inside the logic of the other. Imagine if we were handling five or ten  promises!

Mistake 2:  Forgetting  to  return  a promise.

![](Images/image04985.jpeg)

Let’s  break down  what’s happening  in the example:

• We  invoke  returnsFirstPromise()  which returns  a promise.

• We  invoke  .then()  with  a success handler.

• Inside the success handler, we create our second promise, but we  forget to  return  it!

• We invoke a second  .then(). It’s supposed to handle the logic for the  second promise, but  since we didn’t return,  this  .then()  is invoked  on  a  promise with the  same  settled  value  as the original  promise!

Since forgetting to return our promise won’t throw an error, this can be a  really  tricky thing to  debug!

Instructions  1.

The  code in  app.js  works  correctly, but  it doesn’t  follow  best  practices.

![](Images/image04986.jpeg)Type  node  app.js  in  the  terminal  and hit  enter,  so you  can  see what the  program  outputs.

 Checkpoint 2 Passed

2.

Refactor, or rewrite, the code to avoid the two common mistakes: nesting  and  forgetting to return properly.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

![](Images/image04987.jpeg)Type node  app.js  in the terminal and hit  still  working as expected.

to  make sure  your  program is

![](Images/image04988.jpeg)

Using  Promise.all()

When done correctly, promise composition is a great way to handle  situations where asynchronous operations depend on each other or  execution order matters. What if we’re dealing with multiple promises, but  we  don’t care about  the order? Let’s  think in terms  of cleaning again.

For us to consider our house clean, we need our clothes to dry, our trash  bins emptied, and the dishwasher to run. We need all of these tasks to  complete but not in any particular order. Furthermore, since they’re all  getting done asynchronously, they should really all be happening at the  same time!

To maximize efficiency we should use concurrency, multiple asynchronous  operations happening together. With promises, we can do this with the  function  Promise.all().

Promise.all()  accepts  an array of promises  as its  argument and returns  a  single  promise.  That single promise will  settle in one of two  ways:

• If every promise in the argument array resolves, the single promise  returned  from  Promise.all()  will  resolve with an array  containing the  resolve  value from each promise in the  argument array.

• If any promise from the argument array rejects, the single promise  returned from  Promise.all()  will immediately  reject with the reason  that  promise rejected.  This behavior  is  sometimes referred  to

as  failing fast.

Let’s  look at  a code  example:

![](Images/image04989.jpeg)

Let’s  break down  what’s happening:

• We  declare  myPromises  assigned to invoking  Promise.all().

• We  invoke  Promise.all()  with  an array  of three promises—  the  returned  values from functions.

• We  invoke  .then()  with a  success handler which will  print the array  of  resolved  values if each  promise resolves successfully.

• We  invoke  .catch()  with  a failure handler which will print the first  rejection  message if any promise rejects.

Instructions  1.

Our business is doing so well that we’re running low on inventory. We want  to reach out to some distributors to see if they have the items we need. We  only want to make one restocking order, so we’ll only want to place the  order  if all  of the items are available.

Take a look at the provided code. We require in one  function:  checkAvailability().

checkAvailability()  expects two string arguments: an item and a  distributor. It returns a promise. The function simulates checking that the  given  distributor  has a given item. 80%  of the time it will resolve the

promise with the item, and 20% of the time it will reject the promise with an  error  message stating that the item isn’t  available.

We also provided two functions which will serve as success and failure  handlers.

If you’d like, look at the library.js file to see how these functions work.  Press  “Check  Work”  when  you’re  ready  to  move  on  to  the  next  checkpoint.

 Checkpoint 2 Passed

2.

Create  three  variables each  assigned to  a  separate  promise:

• checkSunglasses  should be assigned the value returned from  invoking  checkAvailability()  with  'sunglasses'  as its first  argument  and  'Favorite Supply Co.'  as its  second argument.

• checkPants  should be assigned the value returned from  invoking  checkAvailability()  with  'pants'  as  its  first  argument  and  'Favorite Supply  Co.'  as its  second argument.

• checkBags  should be assigned the value returned from  invoking  checkAvailability()  with  'bags'  as its first argument  and  'Favorite Supply  Co.'  as its  second argument.

 Checkpoint 3 Passed

3.

![](Images/image04990.jpeg)Invoke

and  checkBags.

with  an  array  containing  checkSunglasses,  checkPants,

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Chain  a .then()  to the  promise returned  from  Promise.all(). You should  pass in  onFulfill  to serve as the success handler.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Add  a  .catch()  to the chain.  You should pass in  onReject  to serve  as  the  failure  handler.

 Checkpoint 6 Passed

6.

![](Images/image04991.jpeg)Type node app.js  in  the terminal and hitto execute  your  program.

![](Images/image04992.jpeg)

Review

Awesome job! Promises are a difficult concept even for experienced developers, so  pat yourself on the back. You’ve learned a ton about asynchronous JavaScript and  promises.  Let’s review:

• Promises are JavaScript objects that represent the eventual result of an  asynchronous  operation.

• Promises  can  be in  one  of three  states:  pending,  resolved,  or rejected.

• A  promise is settled if  it is either resolved  or  rejected.

• We  construct  a  promise  by  using the  new  keyword  and  passing an  executor  function to the  Promise  constructor  method.

• setTimeout()  is a Node function  which delays the  execution of  a callback  function  using the event-loop.

• We  use  .then()  with  a  success  handler  callback  containing the  logic for what  should happen  if  a promise resolves.

• We  use  .catch()  with a failure handler callback containing the  logic for  what  should happen  if  a promise rejects.

• Promise composition enables us to write complex, asynchronous code that’s  still  readable.  We do this by  chaining  multiple  .then()‘s and  .catch()‘s.

• To use promise composition correctly, we have to remember  to  return  promises constructed within a  .then().

• We  should  chain multiple  promises rather  than  nesting  them.

• To  take  advantage of  concurrency, we  can use  Promise.all().

ASYNC  AWAIT

Introduction

Often in web development, we need to handle asynchronous actions—  actions we can wait on while moving on to other tasks. We make requests  to networks, databases, or any number of similar operations. JavaScript is  non-blocking: instead of stopping the execution of code while it waits,  JavaScript uses an [event-loop](https://youtu.be/8aGhZQkoFbQ) which allows it to efficiently execute other  tasks  while it awaits  the completion of  these asynchronous actions.

Originally, JavaScript used callback functions to handle asynchronous  actions. The  problem with  callbacks is that they  encourage complexly  nested code which quickly becomes difficult to read, debug, and scale. With  ES6, JavaScript integrated native [promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) which allow us to write  significantly  more readable code.  JavaScript  is continually improving,

and [ES8](https://en.wikipedia.org/wiki/ECMAScript#8th_Edition_-_ECMAScript_2017) provides a new syntax for handling our asynchronous  action, async...await. The  async...await  syntax allows us to write  asynchronous code that reads similarly to traditional synchronous,  imperative  programs.

The async...await  syntax is [syntactic sugar](https://en.wikipedia.org/wiki/Syntactic_sugar)— it doesn’t introduce new  functionality into the language, but rather introduces a new syntax for  using promises and [generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator). Both of these were already built in to the  language. Despite this,  async...await  powerfully improves the readability  and  scalability of  our code. Let’s learn  how to use it!

Instructions  1.

![](Images/image04993.jpeg)In this lesson, you’ll be given a code-editor to write your code and a bash  terminal  to execute  your  code. To  execute your  program,  you’ll type  node

![](Images/image04994.jpeg)app.js  in  the  terminal  and  hit(or  return).  You’ll  press  the  “Check  Work”

button  to submit your  code  for evaluation.

Check out the code we provided. It shows three ways of accomplishing the  same  task: reading and printing  from two  files in  a specified order:

• The  first  version  uses  callback functions.

• The  second  version uses  native  promise syntax

• The  third  version  uses  async...await.

![](Images/image04995.jpeg)Don’t worry about understanding the  async...await  syntax— that’s what  you’ll learn  in  this lesson!  If you haven’t  already, type  node app.js  into  the  terminal and press  enter. Then, press “Check Work”.

![](Images/image04996.jpeg)

![](Images/image04997.jpeg)

![](Images/image04998.jpeg)

![](Images/image04999.jpeg)}

readFiles();

const  fs  =  require('fs');

const  promisifiedReadfile  =  require('./promisifiedReadfile');

// Here we use fs.readfile() and callback functions:  fs.readFile('./file.txt',  'utf-8',  (err,  data)  =>  {

if  (err)  throw  err;

let  firstSentence  =  data;

fs.readFile('./file2.txt',  'utf-8', (err, data) => {  if  (err) throw  err;

let secondSentence = data;  console.log(firstSentence,  secondSentence);

});

});

// Here we use native promises with our "promisified" version of readfile:  let  firstSentence;

promisifiedReadfile('./file.txt',  'utf-8')

.then((data) => {  firstSentence  =  data;

return  promisifiedReadfile('./file2.txt',  'utf-8');

})

.then((data)  =>  {

let secondSentence = data;  console.log(firstSentence,  secondSentence)

})

.catch((err)  =>  {console.log(err)});

// Here we use promisifiedReadfile() again but instead of using the native pro  mise  .then() syntax,  we  declare  and  invoke  an  async/await  function:

async  function  readFiles()  {

let firstSentence = await promisifiedReadfile('./file.txt', 'utf-8');  let secondSentence = await promisifiedReadfile('./file2.txt', 'utf-8');  console.log(firstSentence,  secondSentence);

}

![](Images/image05000.jpeg)

The  async  Keyword

The async  keyword is used to write functions that handle asynchronous  actions. We wrap our asynchronous logic inside a function prepended with  the  async  keyword.  Then, we invoke that function.

![](Images/image05001.jpeg)

We’ll  be using  async  function declarations throughout this lesson,  but we

can  also create  async  function  expressions:

![](Images/image05002.jpeg)

async  functions  always return  a promise.  This means  we can use  traditional

promise  syntax,  like  .then()  and  .catch  with our  async  functions.  An  async  function  will return  in  one of three  ways:

• If there’s nothing returned from the function, it will return a promise  with  a  resolved value of  undefined.

• If there’s a non-promise value returned from the function, it will  return  a promise resolved to that value.

• If a promise is returned from the function, it will simply return that  promise

![](Images/image05003.jpeg)

![](Images/image04825.jpeg)![](Images/image04825.jpeg)what’s actually returned when we invoke  resolved  value of  5.

Let’s write an  async  function!

inside the function body,  is  a  promise  with  a

![](Images/image05004.jpeg)Instructions

1.

We provided a function  withConstructor()  which takes in a number. If the  number is  0, it returns a promise that resolves to the string  'zero'. If the  number is not  0, it returns a promise that resolves to the string  'not zero'.  Take  a  moment to  understand  this function  and the code  that follows.

![](Images/image05005.jpeg)When  you’re ready to run it, type  node  app.js  in  to the terminal and  press  enter.

 Checkpoint 2 Passed

2.

Write  an  async  function,  withAsync()  which  reproduces the  functionality

of  withConstructor(). Though your function will return a promise, it should  not  construct  the  promise using  the  new  keyword.  Instead, it  should rely on  the  fact that an  async  function automatically returns a promise.

When  you’re ready,  check your  work to move  on to  the next step.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

![](Images/image05006.jpeg)Now  test your  code! Uncomment  the  test  code we  wrote at  the bottom

of  app.js.  In  the  terminal, type  node  app.js  and press  code.

to  execute the

![](Images/image05007.jpeg)

![](Images/image05008.jpeg)

The  await  Operator

In  the  last exercise, we covered the  async  keyword.  By  itself, it  doesn’t  do  much; async  functions are almost always used with the additional  keyword  await  inside the function  body.

The await  keyword can only be used inside an  async  function.  await  is an  operator: it returns the resolved value of a promise. Since promises resolve  in  an indeterminate amount of  time,  await  halts,  or pauses, the  execution of  our async  function until a given promise is resolved.

In most situations, we’re dealing with promises that were returned from  functions. Generally, these functions are through a library, and, in this  lesson, we’ll be providing  them. We can  await  the  resolution of the  promise  it returns inside an  async  function. In the example below,  myPromise()  is a  function that returns a promise which will resolve to the string  "I am  resolved  now!".

![](Images/image05009.jpeg)

Within our  async  function,  asyncFuncExample(), we use  await  to halt our  execution until  myPromise()  is resolved and assign its resolved value to the  variable  resolvedValue.  Then  we  log  resolvedValue  to  the console.  We’re  able  to  handle  the  logic  for  a  promise  in  a  way  that  reads  like  synchronous  code.

Instructions  1.

In  the  provided  code,  we’ve  required  in  the  function  brainstormDinner().  This function expects no arguments and returns a new promise with a  resolved value of a string representing a meal. (You can look at the code for  this  function by  navigating to the library.js  file.)

Look at the nativePromiseDinner()  function in app.js. Take a moment to  understand this function and predict its expected outcome. In the next step,  you’ll be recreating its functionality using  async...await  rather than native  promises.

It’s not necessary to execute the  nativePromiseDinner()  function, but, if  you’d like to, check out the hint for some guidance. Press “Check Work”  when  you’re ready to  move on to the next  step.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Fill  in  the body  of  the  announceDinner()  function so that it has the same  functionality  as  nativePromiseDinner(). It  should  wait for  the promise

returned from brainstormDinner()  to resolve, and then log a string to the  console in the same format as did  nativePromiseDinner(). You’ll need to use  the  await  operator  inside your function.

When  you’re ready,  check your  work to move  on to  the next step.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

At the bottom of app.js, beneath the function declaration, invoke  the  announceDinner()  function.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

![](Images/image05010.jpeg)In  the  terminal  type  node  app.js  and pressto execute  your code.

![](Images/image05011.jpeg)

Writing  async  Functions

We’ve seen that the  await  keyword halts the execution of an  async  function  until  a  promise  is  no  longer pending.  Don’t forget the  await  keyword!  It may  seem  obvious,  but  this  can  be  a  tricky  mistake  to  catch  because  our  function  will still run— it just won’t have the  desired  results.

We’re going to explore this using the following function, which returns a  promise that resolves to  'Yay,  I resolved!'  after  a 1 second delay:

![](Images/image05012.jpeg)

Now  we’ll write two  async  functions which invoke  myPromise():

![](Images/image05013.jpeg)

In  the  first  async  function,  noAwait(),  we left  off  the  await  keyword  before  myPromise().  In the  second,  yesAwait(),  we  included  it.

The  noAwait()  function  logs  Promise  { <pending> }  to the console. Without  the  await  keyword,  the function execution wasn’t paused.

The  console.log()  on  the following  line was  executed before  the promise  had  resolved.

Remember that  the  await  operator  returns the  resolved value of  a promise.  When  used properly in  yesAwait(), the variable  value  was assigned  the

resolved  value of  the  myPromise()  promise,  whereas in  noAwait(),  value  was  assigned  the promise object itself.

Instructions  1.

Take  a  look at  the provided code.  We required in

the  shopForBeans()  function from  library.js which  returns  a  promise  with  a  resolved  value of a string representing a type  of bean,  eg. ‘kidney’.

Next,  we  declared  the  getBeans()  function.  Let’s summarize its  intended  functionality:

• Log  '1.  Heading to the store  to  buy  beans...'  to the  console.

• Capture the resolved value of the promise returned when we  invoke  shopForBeans().

• The  promise  returned from  shopForBeans()  prints a string in the  format  '2.  I  bought  [the  resolved  type  of  beans]  beans  because  they  were  on sale.'

• Finally, the function prints a string in the format  '3. Great! I'm  making [the bean type] beans for dinner tonight!'  to the  console.

Execute  app.js  in the terminal to see if  getBeans()  is working as intended.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Uh oh, getBeans()  is logging  '3. Great! I'm making [object Promise] beans  for dinner tonight!'  to  the  console.  Take a moment to  understand why this  is happening, and then refactor  getBeans()  so it works as intended. Check  your  work when you’re ready to move on to the  next step.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

To test that the code is now functioning properly, execute app.js in the  terminal  again.

![](Images/image05014.jpeg)

![](Images/image05015.jpeg)

Handling  Dependent Promises

The true beauty of  async...await  is when we have a series of asynchronous  actions which depend on one another. For example, we may make a  network request based on a query to a database. In that case, we would  need to wait to make the network request until we had the results from the  database. With native promise syntax, we use a chain of  .then()  functions  making  sure to return  correctly  each one:

![](Images/image05016.jpeg)

Let’s  break down what’s happening  in the  nativePromiseVersion()  function:

• Within our function we use two functions which return  promises:  returnsFirstPromise()  and  returnsSecondPromise().

• We  invoke  returnsFirstPromise()  and  ensure  that  the  first  promise  resolved  by  using  .then().

• In the callback of our first  .then(), we log the resolved value of the  first  promise,  firstValue, and then

return  returnsSecondPromise(firstValue).

• We  use  another  .then()  to  print the second  promise’s resolved  value  to the  console.

Here’s how  we’d write an  async  function to accomplish the same  thing:

![](Images/image05017.jpeg)

Let’s  break down what’s happening  in our  asyncAwaitVersion()  function:

• We  mark  our function  as  async.

• Inside our function, we create a variable  firstValue  assigned  await  returnsFirstPromise().  This  means  firstValue  is  assigned  the  resolved  value  of the awaited promise.

• Next, we log  firstValue  to the console.

• Then, we create a variable  secondValue  assigned to  await  returnsSecondPromise(firstValue).  Therefore,  secondValue  is  assigned  this  promise’s resolved  value.

• Finally, we log  secondValue  to the  console.

Though using the  async...await  syntax can save us some  typing, the  length  reduction  isn’t  the main point. Given  the two versions of the  function,

the  async...await  version  more  closely resembles  synchronous  code, which  helps developers maintain and debug their code. The  async...await  syntax  also makes it easy to store and refer to resolved values from promises  further back in our chain which is a much more difficult task with native  promise syntax. Let’s create some  async  functions with

multiple  await  statements!

Instructions  1.

Take  a  look at  the provided code.  We  require in three

functions:  shopForBeans(),  soakTheBeans(), and  cookTheBeans(). These  functions  each  return a promise.

• shopForBeans()  expects  no  arguments  and  returns  a  promise  which  will resolve to a string of  a  bean type.

• soakTheBeans()  expects a bean  type string as an  argument and  returns a promise which resolves to a boolean indicating  whether  or  not the beans are softened.

• cookTheBeans()  expects  a  boolean  as  an  argument  and,  if  that  value is  true, returns a promise which will resolve to a string  announcing  that dinner is ready.

If you’d like, look at the library.js file to see how these functions work.  Press  “Check Work” to  move on  to the next  step.

 Checkpoint 2 Passed

2.

In the following checkpoints, you’ll create an  async  function that handles  the three dependent promises we just walked through. It will simulate  shopping for, soaking, and then cooking the beans. To get started, declare  an async  function,  makeBeans(). You can leave the function body blank for  now.

Check  your  work to move  on to the  next  step.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Inside your function, declare a variable,  type, assigned to the resolved value  of  shopForBeans(). This must  be accomplished  in  one statement.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Next inside your function, declare a variable,  isSoft, assigned to the  resolved value of  soakTheBeans().  Don’t forget:  the  soakTheBeans()  function  expects  an  argument.  Make sure to pass the expected value

into  soakTheBeans().

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Next inside your function, declare a variable,  dinner, assigned to the  resolved of  cookTheBeans(). Don’t  forget: the  cookTheBeans()  function also  expects  an  argument.  Make sure to pass the expected value

into  cookTheBeans().

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Next  inside your function, log  your  dinner  variable to  the console.

 Checkpoint 7 Passed

7.

Beneath your function  declaration, invoke the  makeBeans()  function.

 Checkpoint 8 Passed

8.

Let’s see your  async  function in action! In the terminal, type  node  app.js  and

![](Images/image05018.jpeg)press  continue)

to  execute the  code. (Press  “Check Work”  when complete  to

![](Images/image05019.jpeg)

Handling  Errors

When  .catch()  is  used with a long promise chain,  there is no indication of  where in the chain the error was thrown. This can make debugging  challenging.

With async...await, we use  try...catch  statements for error handling. By  using this syntax, not only are we able to handle errors in the same way we  do with synchronous code, but we can also catch both synchronous and  asynchronous  errors.  This makes for  easier  debugging!

![](Images/image05020.jpeg)

promise’s

functions return promises we can still use native  with an  async  function

![](Images/image05021.jpeg) 

![](Images/image05022.jpeg)

This  is sometimes  used in the  global scope  to catch final  errors in  complex

code.

Instructions  1.

For convenience, we’ve been working with a lot of promises that never  reject,  but this isn’t very realistic!

This time we’ve required in a function,  cookBeanSouffle()  which returns a  promise that resolves or rejects randomly. When it resolves, the promise  resolves with a value of  'Bean Souffle'  and, when it rejects, it  rejects with a  value of  'Dinner is ruined!'. If you’re interested, you can see how the  function  works by looking in the  library.js  file.

Press  “Check Work” when you’re ready  to move on to the  next  step.

 Checkpoint 2 Passed

2.

Declare  an  async  function, hostDinnerParty().  Inside  your  function,  create  a try...catch  statement. The  catch  statement should specify an  identifier, error. You can leave  both the  try  and  catch  blocks empty.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

![](Images/image05023.jpeg)![](Images/image05024.jpeg)Inside your  try  block, log a  string in the  following  format:

of cookBeanSouffle()  promise] is  served!'  ie.  'Bean  Souffle  is  served!'.  Make sure to  await  the  cookBeanSouffle()  promise. For more guidance,  check out  the hint.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Now  let’s  fill  in the  catch  block! First log the error to the console, and then  log  the string:  'Ordering a pizza!'  to the console.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Awesome!  Beneath  your  function  declaration,  invoke  hostDinnerParty().

 Checkpoint 6 Passed

6.

Let’s  see your  function in action. In the terminal  type  node  app.js  and

![](Images/image05025.jpeg)pressto  run the code. If you keep  executing app.js  you’ll see  the

results  of the  promise resolving or  rejecting.

![](Images/image05026.jpeg)

Handling  Independent  Promises

Remember that  await  halts  the execution of our  async  function. This  allows  us to conveniently write synchronous-style code to handle dependent  promises. But what if our  async  function contains multiple promises which  are  not dependent on the results of  one another  to execute?

![](Images/image05027.jpeg)

In the waiting()  function, we pause our function until the first promise  resolves, then we construct the second promise. Once that resolves, we  print  both resolved values to the console.

In our concurrent()  function, both promises are constructed without  using  await.  We  then await  each of their  resolutions to  print them to the  console.

With  our concurrent()  function  both promises’ asynchronous operations  can  be run simultaneously. If possible, we want to get started on each  asynchronous operation as soon as possible! Within our  async  functions we  should still take advantage of concurrency, the ability to perform  asynchronous  actions at the  same time.

Note: if we have multiple truly independent promises that we would like to  execute fully  in  parallel,  we must use  individual  .then()  functions  and  avoid  halting  our  execution with  await.

Instructions  1.

Take  a  look at  the provided code.  We  require in four

functions:  cookBeans(),  steamBroccoli(),  cookRice(),  and  bakeChicken().  These

functions each return a promise which will resolve to a string representing a  part  of a meal.

![](Images/image04564.jpeg)If you’d like, look at the library.js file to see how these functions work.  Press  “Check Work” when you’re ready  to move on.

Checkpoint 2  Passed

2.

Declare an  async  function,  serveDinner().  Create four  variables:

• vegetablePromise  which should be assigned  the return value  of  steamBroccoli()

• starchPromise  which  should  be  assigned the  return  value  of  cookRice()

• proteinPromise  which  should be  assigned the  return  value  of  bakeChicken()

• and  sidePromise  which should be  assigned the  return  value  of  cookBeans()

These variables should be assigned the promise objects themselves not  their  resolved values.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Next  console.log()  a  string in the  following  format:  Dinner  is  served.  We’re  having  [resolved value of  the  vegetablePromise], [resolved  value of

the  starchPromise], [resolved value of the  proteinPromise], and [resolved  value of the  sidePromise]. ie. ‘Dinner is served. We’re having broccoli, rice,  chicken,  and beans.’

You’ll  need  to  await  each promise,  but  there are a few  different  ways you  can accomplish the desired functionality. Check out the hint if you want  some  guidance.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Awesome! Let’s see your function in action. Beneath your function  declaration,  invoke  serveDinner().

 Checkpoint 5 Passed

5.

![](Images/image05028.jpeg)In  the  terminal  type  node  app.js  and pressto run the code.

![](Images/image05029.jpeg)

Await  Promise.all()

Another way to take advantage of concurrency when we have multiple  promises which can be executed simultaneously is to  await  a  Promise.all().

We can pass an array of promises as the argument to  Promise.all(), and it  will return a single promise. This promise will resolve when all of the  promises in the argument array have resolved. This promise’s resolve value  will be an array containing the resolved values of each promise from the  argument  array.

![](Images/image05030.jpeg)

In  our above example,  we  await  the  resolution of a  Promise.all().

This  Promise.all()  was  invoked  with  an  argument  array  containing  four  promises  (returned  from  required-in  functions).  Next,  we  loop  through

our  resultArray,  and log  each  item to  the console.  The  first element

in  resultArray  is the  resolved value of the  asyncTask1()  promise,  the  second  is  the value of the  asyncTask2()  promise, and  so  on.

Promise.all()  allows us  to take  advantage of  asynchronicity— each  of the  four asynchronous tasks can process concurrently.  Promise.all()  also has  the benefit of failing fast, meaning it won’t wait for the rest of the  asynchronous actions to complete once any one has rejected. As soon as  the  first promise in the  array  rejects, the promise  returned

from  Promise.all()  will  reject with  that  reason. As  it  was when  working with  native promises, Promise.all()  is a good choice if multiple asynchronous  tasks  are all  required,  but none  must wait for  any other before  executing.

Instructions  1.

In this exercise, we require in the same four functions as in the last  exercise:  cookBeans(),  steamBroccoli(),  cookRice(),  and  bakeChicken().

These functions each return a promise which will resolve to a string  representing a part of a meal. You can check them out in the library.js file.  Press  “Check Work” to  move on  to the next  step.

 Checkpoint 2 Passed

2.

![](Images/image05031.jpeg)You’re  going  to  create a very similar  function to the  serveDinner()  function  you  created in the last  exercise. This time,  you’ll use  Promise.all()!

Create  an  async  function  serveDinnerAgain(). Inside your  function, declare a  variable foodArray  and assign it  the resolved value of the promise returned  from  Promise.all().

Remember that Promise.all()  takes in an  array of promises. Pass in an  array  containing  the  steamBroccoli(),  cookRice(),  bakeChicken(),

and  cookBeans()  functions  in  that  order.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Next  console.log()  a  string in the  following  format:  Dinner  is  served.  We’re  having  [first item in  foodArray  ], [second item in  foodArray  ], [third item

in  foodArray],  and [fourth  item in  foodArray  ].  eg. ‘Dinner is served. We’re  having  broccoli, rice,  chicken, and  beans.’

There are a few different ways you can accomplish the desired functionality.  Check  out the hint if you want some  guidance.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Ok great! Now let’s see your function in action. Beneath your function  declaration,  invoke  serveDinnerAgain().

 Checkpoint 5 Passed

5.

![](Images/image05032.jpeg)In  the  terminal  type  node  app.js  and pressto run the code.

![](Images/image05033.jpeg)

Review

Awesome  work  getting the  hang of the  async...await  syntax! Let’s  review what you’ve  learned:

• async...await  is syntactic  sugar  built on native  JavaScript promises  and  generators.

• We  declare  an  async  function with  the  keyword  async.

• Inside an  async  function we use the  await  operator to pause execution of our  function until an asynchronous action completes and the awaited promise is  no longer  pending .

• await  returns the  resolved  value of the awaited  promise.

• We  can  write multiple  await  statements to produce code  that reads like  synchronous  code.

• We  use  try...catch  statements within our  async  functions  for error handling.

• We  should still take advantage of concurrency by writing  async  functions that  allow  asynchronous actions  to happen  in concurrently  whenever  possible.

Introduction  to Requests

Have  you  ever  wondered  what  happens  after you  click  a  “Submit” button  on a web page? For instance, if you are submitting information, where does  the information go? How is the information processed? The answer to the  previous  questions revolves around HTTP requests.

There are many types of HTTP requests. The four most commonly used  types of HTTP requests are GET, POST, PUT, and DELETE. In this lesson, we’ll  cover GET and POST requests. If you want to learn more about the different  HTTP  requests,  we recommend the following  documentation:

• [Mozilla  Developer  Network:  HTTP  methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)

With a GET request, we’re retrieving, or getting, information from some  source (usually a website). For a POST request, we’re posting information to  a  source that will process the information  and  send  it  back.

In this lesson, we will explain how to make GET and POST requests by using  JavaScript’s XHR object. We’ll also incorporate query strings into our  requests.

We’ll use the Datamuse API for GET requests and the Rebrandly URL  Shortener API for POST requests. To complete the exercise on POST, make  sure you create a Rebrandly API Key by following the instructions in the  article  below:

• [Codecademy  Articles:  Rebrandly URL  Shortener  API](https://www.codecademy.com/articles/rebrandly-signup) .

Instructions

Click  the button  on  the web page  to  see what the  code in main.js  does.

You’ll see JSON being displayed on the page. JSON, JavaScript Object  Notation, will be the format in which our data is sent to us. That button you  click  produces a  GET request.  That’s  right,  you’ve just made a  GET  request!

HTTP  Requests

One of JavaScript’s greatest assets is its non-blocking properties, or that it  is  an asynchronous  language.

Websites, like newspaper websites, take advantage of these non-blocking  properties to provide a better user experience. Generally, a site’s code is  written so that users don’t have to wait for a giant image to load before  being allowed to read the actual article—rather, that text is rendered first  and  then the image can load in the background.

JavaScript  uses  an  event  loop  to  handle  asynchronous  function  calls.  When  a program is run, function calls are made and added to a stack. The  functions that make requests that need to wait for servers to respond then  get sent to a separate queue. Once the stack has cleared, then the functions  in  the queue are  executed.

Web developers use the event loop to create a smoother browsing  experience by deciding when to call functions and how to handle  asynchronous events. We’ll be exploring one system of technologies called  Asynchronous  JavaScript and XML,  or AJAX.

To  read  more about  the event  loop, read  the MDN  documentation:

• [MDN  Documentation: Event Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)

Instructions  1.

To get a glimpse of how the event loop works, take a look at the code in  the  code editor.

We’ll be using  setTimeout(), which will pass a function call to the queue. The  first argument is a callback and the second argument is the number of  milliseconds  the program must wait  before the callback can  be run.

The  other  console.log()  calls  are run from the  stack.

 Checkpoint 2 Passed

2.

Interesting  right?

What  if we change the  2500  in  setTimeout()  to be  0?  Essentially the  callback  doesn’t need to wait before it can be called. Do you think that this change  will  affect the order?

![](Images/image05034.jpeg)

XHR  GET Requests I

Asynchronous JavaScript and XML (AJAX), enables requests to be made  after the initial page load. Initially, AJAX was used only for XML formatted  data, now it can be used to make requests that have many different  formats.

[MDN  Documentation:  Extensible  Markup Language  (XML)](https://developer.mozilla.org/en-US/docs/XML_introduction).

Similarly, the XMLHttpRequest (XHR) API, named for XML, can be used to  make  many kinds of requests and  supports other  forms of  data.

Remember, we use GET to retrieve data from a source. Take a look at the  boilerplate  code  in  the  diagram  to  see  how  to  make  an  XHR  GET  request.

We’ll construct this template from scratch in a different exercise and walk  through  what each step does.

Instructions

Move  on to  the next  exercise  when  you’re ready!

![](Images/image05035.jpeg)

XHR  GET Requests II

We are going to reconstruct XHR GET request boilerplate code step-by-  step  until we have written a complete GET request.

Feel free to refer to the XHR GET diagram at any point while completing  this exercise:

• [XHR  GET  diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/XHR%20GET%20diagram.svg)

![](Images/image05036.jpeg)Instructions  1.

First,  we need  to create the

Save  this  object  in  a  const  called  xhr.

object using  the  new  operator.

Note: While the code will work regardless of how you name your variables,  it  is a common  practice to name this object  xhr.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Next,  save  the  following URL to a  const  called  url.  Make sure  the URL is  wrapped  in quotes so that it is a string.

![](Images/image05037.jpeg)

Stuck?  Get a hint

3.

Set  the  responseType  property  of  the  xhr  object to  equal  'json'.

JSON is JavaScript Object Notation, which is how the response is going to  be  formatted.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Set  the  xhr.onreadystatechange  event  handler  equal  to  an  anonymous  arrow  function.  Leave the function empty.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

In the code block of the function you created in the previous step, add this  conditional  statement:

![](Images/image05038.jpeg)

The purpose of this conditional statement checks to see if the request has  finished.

 Checkpoint 6 Passed

6.

In  the  code  block  of  the conditional statement,  return the  response  property  of  xhr.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Below  the  function  you  created  in  the  previous  two  steps,  call  the  .open()  method  on the  xhr  object and pass it  'GET'  and  url  as  arguments.

.open()  creates a new  request  and the arguments passed  in determine the  type  and URL of the request.

 Checkpoint 8 Passed

Stuck?  Get a hint

8.

On  the following  line, call the  .send()  method  on  the  xhr  object. Do  not  pass  it any arguments.

Nice  work! You’ve written  the boilerplate code  for  an AJAX  GET  request  using an  XMLHttpRequest  object.

![](Images/image05039.jpeg)

XHR  GET Requests III

By this point, you have an idea of how to write the boilerplate code for an  AJAX  request using  an XHR object.

In this exercise, you will incorporate that boilerplate code to make a GET  request  to the Datamuse API to search  for words that  rhyme!

• [Datamuse  API Documentation](https://www.datamuse.com/api/)

![](Images/image05040.jpeg)

1.

At  the top  of  main.js, create  a  const  named  url  and save to it the following  URL  (as a  string):

https://api.datamuse.com/words?

You’ll  be using this URL to  direct  your  request.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Underneath  const  url, create  another  const  named  queryParams  and assign it  to  'rel_rhy='

'rel_rhy='  is the start of a parameter for  the  query string. This parameter  will  narrow your search  to words that rhyme.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

In  the  function  getSuggestions(), create  a  const  named  wordQuery  and assign  it  to be  inputField.value.

inputField.value  grabs  what is in  the  inputField  and assigns  it  to  the  variable  wordQuery.

You’ll  be working in  getSuggestions()  for  the  rest of  the exercise.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Now  create another  const  named  endpoint, and assign  equal  to a  string that  concatenates  url,  queryParams, and  wordQuery.

endpoint  will store  the value of the entire URL  and query  string.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

You  can  now start on  the  XMLHttpRequest  object. Declare  a const  named  xhr  and use the  new  operator to create  the  XMLHttpRequest  object.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Set  the responseType  of  xhr  to  'json'.

When  data is  sent back,  it will be  in JSON  format.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Assign  an  anonymous arrow function to the  onreadystatechange  event  handler  of  xhr.

 Checkpoint 8 Passed

Stuck?  Get a hint

8.

Include the following code inside the code block of the anonymous arrow  function  you just  created:

![](Images/image05041.jpeg)

The  renderRawResponse()  helper function  can be  viewed  at  public/helperFunctions.js.

 Checkpoint 9 Passed

9.

Below  the anonymous  arrow function you  just  created  (but  still inside

of  getSuggestions()),  call  the  .open()  method  on  the  XHR  object and  pass

it  'GET'  and  endpoint  as respective  arguments. This method call will  create a  new request using the two arguments:  'GET'  sets the method and  url  sets  the  destination.

Underneath .open(), call the  .send()  method on  xhr  and pass it no  arguments. The  .send()  method will send  the request  to  the  server.

Then  run your  code.

Type in a word in the input field and click the submit button. If all went well,  the  response  field  in  the  browser  will  display  the  raw  response  from  the  API!

 Checkpoint 10  Passed

Stuck?  Get a hint

10.

Now  delete  renderRawResponse(xhr.response)  and  replace  it  with  renderResponse(xhr.response)  and  run  your  code.

Then type in a word in the input field and click the submit button.  Great,  now  it  looks nice and formatted!

![](Images/image05042.jpeg)

![](Images/image05043.jpeg)

XHR  GET Requests IV

In the previous exercise, you made a GET request to the Datamuse API to  find words that rhyme. In this exercise, we will create a request to set a  topic  and  find  adjectives  that  describe  the  input  word  using  query  strings.

A query string contains additional information to be sent with a request.  The Datamuse API allows us to retrieve more specific data with query  strings  attached to the request URL.

• [Wiki:  query  string](https://en.wikipedia.org/wiki/Query_string)

![](Images/image04825.jpeg)A query string is separated from the URL using a  ?  character. After  ?, you  can then create a parameter which is a key value pair joined by a  =. Examine  the  example below:

'https://api.datamuse.com/words?key=value'

If you want to add an additional parameter you will have to use  the  &  character to  separate your parameters.  Like so:

![](Images/image05044.jpeg)

Let’s  incorporate  this  into  our code!

Instructions  1.

Let’s do something else besides finding words that rhyme. Have  const  queryParams  store the value  'rel_jjb='. This will search for words that  describe  another word.

Run the code. Then, type in a word and click the submit button on the web  page.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Since we want to retrieve more specific results, we should create another  parameter.  Create  another  const  additionalParams  underneath  queryParams,  and  assign it  '&topics='.

Reminder: the  &  character at the start of the string  is  used to  separate our  parameters. The  =  character will  join the key  'topics'  to a  value.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Now, if you were wondering why there’s a second input field, that’s exactly  what we’re going to hook up now! The word typed in here will be the value  portion  of our second  parameter.

The second parameter will filter the response using the word typed into the  second input field. In the next step, we’ll incorporate this parameter in with  our  query string.

In the code block of  getSuggestions(), under  wordQuery, declare  a  const  topicQuery, and  assign  it to  the  value  of  topicField.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

In  getSuggestions(), change the value of  endpoint  to a concatenated string  of  url,  queryParams,  wordQuery,  additionalParams, and  topicQuery.

Run  the  code. Then  enter a  word and  a  topic and  click submit.

Our request will have returned a response of adjectives that are related to a  topic! Feel free to play around with variables and parameters to get more  word  suggestions!

![](Images/image05045.jpeg)

![](Images/image05046.jpeg)

XHR  POST Requests I

Reminder: If you haven’t already signed up for an API Key from Rebrandly, please  read  this Rebrandly  sign up  guide.

• [Codecademy  Articles:  Rebrandly URL  Shortener  API](https://www.codecademy.com/articles/rebrandly-signup) .

Great! By this point, you’ve signed up for an API key and you know the essence of  making  a GET request.

The major difference between a GET request and POST request is that a POST  request requires additional information to be sent through the request. This  additional  information is sent in the  body  of the post request.

Review the code from the diagram to construct your own POST request in the next  lesson.

![](Images/image05047.jpeg)

XHR  POST Requests II

We are going to reconstruct the code from the previous exercise step-by-  step  until we have written a complete AJAX  POST request.

Feel free to refer to the XHR POST diagram at any point while completing  this exercise:

• [XHR  POST diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/XHR%20POST%20diagram.svg)

![](Images/image05048.jpeg)Instructions  1.

Create  a new

a  const  called  xhr.

object using  the  new  operator, and  save it  in

The  XMLHttpRequest  object  is  used  in  JavaScript to  interact  with  servers.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Next,  save  the  following URL to a  const  called  url.  Make sure  the URL is  wrapped  in quotes so that it is a string.

https://api-to-call.com/endpoint

The  URL  will direct  the request  to the  correct  server.

 Checkpoint 3 Passed

3.

Create a new  const  called  data,  and save this line of  code to it:

JSON.stringify({id:  '200'});   JSON.stringify()  will convert a value to a JSON string. By converting the  value  to  a string, we can then  send  the data  to a server.

 Checkpoint 4 Passed

4.

Set  the  responseType  property  of  the  xhr  object to  be  'json'.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Set  the  xhr.onreadystatechange  event  handler  equal  to  an  anonymous  arrow  function.  Leave the function empty until the next step.

.onreadystatechange  will  contain  the  event  handler that  will  be called  when  xhr‘s state changes.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

In the code block of the function you created in the previous step, add a  conditional statement  that  checks to  see if  the  readyState  of  xhr  is equal  to  XMLHttpRequest.DONE.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

In  the  code  block  of  the conditional statement,  return the  response  property  of xhr. The response  property will contain the data that we’re getting back  from  the  POST request.

 Checkpoint 8 Passed

Stuck?  Get a hint

8.

Below  the function  you created  in the previous  two steps,  call

the  .open()  method  on the  xhr  object  and pass it  'POST'  and  url  as  arguments.

.open()  creates a new  request and the arguments passed in  determine what  type  of request is being made and  where  it’s being  made  to.

 Checkpoint 9 Passed

Stuck?  Get a hint

9.

On  the following  line, call  the  .send()  method  on  the  xhr  object and  pass  data  as an argument.

.send()  will send  the  request to  the server.

Nice  work!  You’ve  written  the boilerplate  code for an AJAX  POST  request  using an  XMLHttpRequest  object.

![](Images/image05049.jpeg)

XHR  Post Requests III

Reminder: If you haven’t already signed up for an API Key from Rebrandly,  please  read  our [Rebrandly  URL  Shortener  API](https://www.codecademy.com/articles/rebrandly-signup) article. Keep  in  mind,  while  it’s ok to use your API key in these exercises, you should not share your key  with  anyone (not  even if asking a question in the  forums)!

In this exercise, you’ll be making a POST request to the Rebrandly API to  shorten  a URL.

Get ready! You’re now going to incorporate the previous lesson’s  boilerplate  code into making an actual POST request!

If you reset the exercise at any point, you will have to paste in your API key  again  at the top.

![](Images/image05050.jpeg)

1.

Copy  your Rebrandly  API Key, and assign it to the  const  apiKey  at  the top of  your  code.

 Checkpoint 2 Passed

2.

Within the code block of  shortenUrl(), create a  const  called  urlToShorten,  and  save  inputField.value  to  it.  urlToShorten  will  now  save  the  value  of  the  input field

Note: for the remainder of this exercise’s instructions we will be working  inside  the code block of  shortenUrl()!

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Create a  const  called  data, and save the following code to it:

JSON.stringify({destination:  urlToShorten});  We’re including this information because the API expects to see an object  with a  key  destination  that has a value of a  URL.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Create  a new  XMLHttpRequest  object  using  the  new  operator, and  save  it  to  a  const  called  xhr.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Set  the  responseType  property  of  the  xhr  object to  be  'json'.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Save  an  empty anonymous  arrow function to the  onreadystatechange  event  handler of the  xhr  object.  This function will not take in any parameters.

Inside the anonymous function’s code block, include the following code  inside  of its code block:

![](Images/image05051.jpeg)

The  renderRawResponse  function  can  be  viewed  at  public/helperFunctions.js.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Below  the  anonymous  function you  just  created, call  the  .open()  method  on  xhr, and  pass it  'POST'  and  url  as respective arguments.

 Checkpoint 8 Passed

Stuck?  Get a hint

8.

To access the Rebrandly API, we need a header with two key-value pairs. In  the  header, you must include values for  'Content-type'  and an  'apikey'.

To set the header, we have to include the following code below  our .open()  method.

![](Images/image05052.jpeg)

 Checkpoint 9 Passed

Stuck?  Get a hint

9.

On  xhr,  call the  .send()  method, and pass  it  data  as an  argument.

 Checkpoint 10  Passed

Stuck?  Get a hint

10.

Enter this URL into the input field, and click the shorten button in the web  page.

![](Images/image05053.jpeg)<map name="awmap1"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="86, 21, 92, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="75, 21, 86, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="64, 21, 75, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="53, 21, 64, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="42, 21, 53, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="30, 21, 42, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="19, 21, 30, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="8, 21, 19, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="2, 21, 8, 42"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="509, 1, 515, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="498, 1, 509, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="486, 1, 498, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="481, 1, 486, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="469, 1, 481, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="458, 1, 469, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="448, 1, 458, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="442, 1, 448, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="432, 1, 442, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="420, 1, 432, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="413, 1, 420, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="407, 1, 413, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="395, 1, 407, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="384, 1, 395, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="378, 1, 384, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="367, 1, 378, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="357, 1, 367, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="346, 1, 357, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="338, 1, 346, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="326, 1, 338, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="320, 1, 326, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="310, 1, 320, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="293, 1, 310, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="283, 1, 293, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="271, 1, 283, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="260, 1, 271, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="250, 1, 260, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="240, 1, 250, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="228, 1, 240, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="218, 1, 228, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="208, 1, 218, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="190, 1, 208, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="184, 1, 190, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="167, 1, 184, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="156, 1, 167, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="146, 1, 156, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="140, 1, 146, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="123, 1, 140, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="112, 1, 123, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="106, 1, 112, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="95, 1, 106, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="84, 1, 94, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="67, 1, 84, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="61, 1, 67, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="55, 1, 61, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="49, 1, 55, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="40, 1, 49, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="28, 1, 40, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="21, 1, 28, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="14, 1, 21, 21"><area shape="rect" href="https://medium.com/%40codecademy/breaking-the-coding-language-" coords="2, 1, 14, 21"></map>

Notice  the  object that came  back!

Now

replace  renderRawResponse(xhr.response)  with  renderResponse(xhr.response).  Run  the code.

![](Images/image05054.jpeg)

![](Images/image05055.jpeg)

Review  Requests I

You’ve done an amazing job navigating through making XHR GET and POST  requests! Take some time to review the core concepts before moving on to the next  lesson.

1. JavaScript is the language of the web because of its asynchronous capabilities.  AJAX, which stands for Asynchronous JavaScript and XML, is a set of tools that  are  used  together  to  take advantage  of  JavaScript’s  asynchronous  capabilities.

2. There  are many  HTTP request  methods, two  of which  are GET  and POST.

3. GET  requests  only  request information  from  other  sources.

4. POST methods can introduce new information to other sources in addition to  requesting  it.

5. GET requests can be written using an XMLHttpRequest object and vanilla  JavaScript.

6. POST requests can also be written using an XMLHttpRequest object and  vanilla  JavaScript.

7. Writing GET and POST requests with XHR objects and vanilla JavaScript  requires constructing the XHR object using  new, setting the  responseType,  creating a function that will handle the response object, and opening and  sending  the request.

8. To  add a query string to  a URL endpoint  you  can  use  ?  and include  a  parameter.

9. To  provide additional parameters, use  &  and then include a key-value pair,  joined  by  =.

10. Determining how to correctly write the requests and how to properly  implement them requires carefully reading the documentation of the API with  which  you’re working.

![](Images/image05056.jpeg)

![](Images/image05057.jpeg)while(responseField.firstChild){  responseField.removeChild(responseField.firstChild);

};

getSuggestions();

};

submit.addEventListener('click',  displaySuggestions);

// information to reach Rebrandly API  const  apiKey =  '<Your API  Key>';

const  rebrandlyUrl  =  'https://api.rebrandly.com/v1/links';

//  element  selector

const  shortenButton  =  document.querySelector('#shorten');

//  AJAX  functions

const  shortenUrl  =  ()  =>  {

const  urlToShorten  =  inputField.value;

const  data  =  JSON.stringify({destination:  urlToShorten});

const xhr = new XMLHttpRequest();  xhr.responseType  = 'json';

xhr.onreadystatechange  =  ()  =>  {

if (xhr.readyState === XMLHttpRequest.DONE) {  renderByteResponse(xhr.response);

}

};

xhr.open('POST', rebrandlyUrl);  xhr.setRequestHeader('Content-type', 'application/json');  xhr.setRequestHeader('apikey',  apiKey);

xhr.send(data);

}

// Clear page and call AJAX functions  const  displayShortUrl  =  (event)  =>  {

event.preventDefault();  while(responseField.firstChild){

![](Images/image05058.jpeg)

Introduction  to Requests  with ES6

In the previous lesson, we spent a lot of time dealing with asynchronous data  (remember AJAX/ Asynchronous JavaScript And XML?). Many of our web page  interactions rely on asynchronous events, so managing these events is essential to  good  web development.

To make asynchronous event handling easier, promises were introduced in JavaScript  in ES6:

• [Mozilla  Development  Network:  Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

A  promise is  an object  that handles asynchronous  data.  A  promise has  three states:

• pending  :  when a  promise  is created  or  waiting  for  data.

• fulfilled  :  the  asynchronous  operation  was handled  successfully.

• rejected  :  the asynchronous  operation  was unsuccessful.

The great thing about promises is that once a promise is fulfilled or rejected, you can  chain  an additional method to the original promise.

![](Images/image05059.jpeg)In this lesson, we will explain how to use  requests.  Then,  we  will  simplify  requests  using

, which uses promises to handle  and  await.

We’ll use the Datamuse API for GET requests and Rebrandly URL Shortener API for  POST  requests

fetch()  GET Requests I

The  first  type of  requests we’re  going to  tackle are  GET requests  using  fetch()

• [MDN: Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API).  The  fetch()  function:

• Creates  a request  object  that  contains relevant  information that  an API  needs.

• Sends  that request  object  to the  API endpoint  provided.

• Returns a promise that ultimately resolves to a response object, which  contains  the  status of  the promise  with  information the  API sent  back.

In  the next exercise we’ll go over  the boilerplate code  for  using  fetch()  and  walk  through  what each step does!

![](Images/image05060.jpeg)

fetch()  GET Requests II

We are going to reconstruct the boilerplate code necessary to create a GET  request using the  fetch()  function  step-by-step.

Feel  free  to refer to the  fetch()  GET  diagram at  any point while completing  this exercise:

• [fetch()  GET  diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/fetch%20GET%20diagram.svg)

Instructions  1.

First, call the  fetch()  function and pass  it  this URL  as a string:

https://api-to-call.com/endpoint

This  first argument  determines the endpoint  of the  request.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Chain  a .then()  method to the end of the  fetch()  function  and pass it the  success callback arrow function as its first argument. The success callback  function  takes one parameter,  response.

.then()  will fire  only after  the  promise status of  fetch()  has been resolved.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Inside of the  response  callback function, check the  ok  property

of  response  inside of a  conditional statement. In the  code  block of  the  conditional  statement,  return  response.json().

The  reason we’re testing the  ok  property of the response  object is that it will  be  a Boolean value.  If there were no errors  response.ok  will be  true  and  then  your  code will return  response.json().

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Below the curly braces of the conditional statement, create a new error with  this code:

throw  new  Error('Request  failed!');

Your code will  throw  this error when  response.ok  is falsy.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Add a second argument to  .then(), it will be an arrow function that will  handle our failures. Separate the first callback function from the second  with  a  comma.  The second callback function takes a single

parameter,  networkError.

In the code block of the second callback function,  log  networkError.message  to  the  console.

If we could not reach the endpoint at all, e.g., the server is down, then we  would  get this  networkError.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Chain  another  .then()  method to  the end  of the  first  .then()  method.

Pass  the new  .then()  method a  callback function that takes  jsonResponse  as  its  parameter  and return  jsonResponse.

The  second  .then()‘s success  callback  won’t run  until the

previous  .then()  method has finished  running.  It  will also not  run if  there  was  an error  was thrown previously.

![](Images/image05061.jpeg)

fetch()  GET Requests III

In the previous exercise, you wrote the boilerplate code for a GET request  using fetch()  and  .then(). In this exercise, you’re going to use that code  and manipulate it to access the Datamuse API and render information in  the  browser.

• [Datamuse  API](https://www.datamuse.com/api/).

If the request is successful, you’ll get back an array of words that sound like  the  word you typed into the input field.

You may get some errors as you complete each step. This is because  sometimes we’ve split a single step into one or more steps to make it easier  to  follow.  By  the end,  you should be receiving  no errors.

Instructions  1.

At  the top  of  main.js, create a  const  called  url.  Assign  url  to the following  URL  as a string:

![](Images/image05062.jpeg)

Stuck?  Get a hint

2.

Below  url, create another  const  and  call it  queryParams. Assign  it a  value  of  '?sl='

queryParams  will be the start of your query string and  will narrow your  search  to  words that  sounds like your  word.

 Checkpoint 3 Passed

3.

Inside  the  getSuggestions()  function,  create  a  const  called  wordQuery  and  assign  it  inputField.value.

You’ll need  wordQuery  to  store the value  of what  is being typed into the  input field.

You  will be  working inside  getSuggestions()  for  the remainder of this  exercise.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Now it’s time to add a query string to the URL with all the necessary  parameters.

Create  another const  called  endpoint,  assign it value of  a string that  is  url,  queryParams, and  wordQuery  concatenated in  that  order.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Call the fetch()  function and pass in  endpoint  as an argument. For this API  to  work  within  the provided  browser,  add  {cache: 'no-cache'}  as  the second  argument.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Chain  a .then()  method to  the  fetch()  function. Pass it  a  success  arrow  callback  function as an argument.  The callback function should

take  response  as its single parameter.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Inside the success callback function, create a conditional statement that  checks  if the  ok  property of the  response  object evaluates to a truthy value.  If

so,  call  the function  renderJsonResponse()  and pass in  response  as an  argument.  Then,  run your  code.

Then type in a word to and click the submit button to view the JSON that  came  back. The status  of the  promise return  from  fetch()  will be  resolved.

The  code  for  renderJsonResponse()  can  be  viewed  at  public/helperFunctions.js.

 Checkpoint 8 Passed

Stuck?  Get a hint

8.

Delete  renderJsonResponse(response)  and  replace  it  with  return  response.json().

By  returning  response.json(),  the  next  function  that is  .then()  chained to  it  will  receive a  Promise with JSON data.

 Checkpoint 9 Passed

9.

Below the condition’s code block, add this code to raise an exception if the  request  failed:  throw new  Error('Request  failed!');

 Checkpoint 10  Passed

Stuck?  Get a hint

10.

Separate the success callback function and the error callback function with  a comma. The error callback function will also be an arrow function that  takes one parameter,  networkError. In the code block of the arrow function,  log  networkError.message  to the  console.

![](Images/image05063.jpeg)

![](Images/image05064.jpeg)

fetch() GET Requests IV  Great  job  making  it  this  far!

In  the previous  exercise, you  created the  query  URL, called

the fetch()  function and passed it the query URL and a settings object.  Then, you chained a  .then()  method and passed it two functions as  arguments — one to handle the promise if it resolves, and one to handle  network  errors if the promise is rejected.

In this exercise, you’ll now take the information that was returned with the  promise  and manipulate  the webpage!

![](Images/image05065.jpeg)

1.

At  the end of the  .then()  method,  chain another  .then()  method.

Pass  .then()  an  anonymous  arrow  callback  function that  takes  jsonResponse  as  its single  parameter.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside  the  callback  function,  call  the  function  renderRawResponse()  and pass  in  jsonResponse  as an argument.  Run  the code.

In  the input  field, you  can  type in  a word  and click  the submit button.

If all went well, you should see an array of words that the Datamuse API  responded  with!

You  can view the  purpose of  renderRawResponse  at public/helperFunctions.js.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Time  to clean up  that response a  bit.

Delete  renderRawResponse(jsonResponse)  and  replace  it  with  renderResponse(jsonResponse).

Run  your  code.

Try  the  webpage again  with another  word!

![](Images/image05066.jpeg)

![](Images/image05067.jpeg)

fetch()  POST Requests I

In the previous exercise, you successfully wrote a GET request using the fetch API and  handled  Promises  to  get  word  suggestions  from  Datamuse.  Give  yourself  a  pat  on  the  back (or two to treat yourself)!

Now, you’re going  to learn  how  to use  fetch()  to construct POST  requests!

Take a look at the diagram to the right. It has the boilerplate code for a POST request  using  fetch().

Notice that the initial call takes two arguments: an endpoint and an object that  contains information needed for the POST request. The rest of the request is identical  to the  GET request.

fetch()  POST Requests II

We are going to reconstruct the code from the previous exercise step-by-  step  until we have written a complete POST request

using  fetch()  and  .then().

Feel  free  to refer  to the  fetch()  POST diagram at any point while  completing this  exercise:

• [fetch()  POST  diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/fetch%20POST%20diagram.svg)

Instructions  1.

Call  the  fetch()  function, pass  it the  URL  below  as a  string as  its first  argument,  and  pass  it an  empty  object ({})  as  its  second argument.

https://api-to-call.com/endpoint  We’re calling fetch()  and providing an endpoint. In the next step we’ll fill in  the  empty  object with the necessary information.

 Checkpoint 2 Passed

2.

The  settings  object you passed  to the  fetch()  function will  contain two  properties:  method, with a value of  'POST',  and  body,  with a value

of  JSON.stringify({id:  '200'}).

This second argument determines that this request is a POST request and  what  information will be sent to the API.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Chain a  .then()  method to the  fetch()  function and pass it the success  callback  function  as its first parameter. Pass in  response  as an  argument for

the callback function. Leave the code block of the callback function empty  for now.

The  code  inside  .then()  will execute when  the promise returned  from  fetch()  is resolved.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Inside the callback function’s code block, check the  ok  property  of

the  response  object  inside of  a conditional  statement. In  the code block  of  the  conditional statement, return  response.json().

When  returned, this information will be passed on to the  next  .then()  callback function.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Below the curly braces of the conditional statement, create a new error with  this code:

throw  new  Error('Request  failed!');

This  error will  be raised  if we  get back  some status  error.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Create the failure callback function. This function takes a single  parameter,  networkError. Separate the first callback function from the  second  with a  comma.  This function is  still inside of  the  .then()  method.

In  the  code  block  of  the  function you just made, log  networkError.message  to  the  console.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Chain  another  .then()  method to  the end  of the  first  .then()  method.

In  the  new  .then()  method, create an  arrow callback function  that  takes  jsonResponse  as its parameter.

Then  in  the  code block  return  jsonResponse.

The purpose of this step is to view the JSON that was returned from the  previous  .then().

![](Images/image05068.jpeg)

fetch()  Post Requests III

In the previous exercise, you created the boilerplate code for making a  POST  request using  fetch()  and  .then(). In  this exercise, you’re  going  to  update that boilerplate code to allow you to shorten a URL using the  Rebrandly  URL Shortener API.

• [Rebrandly  API](https://developers.rebrandly.com/).

If you haven’t already created a Rebrandly API key, read through the  Rebrandly  sign  up guide:

• [Codecademy  Articles:  Rebrandly  URL  Shortener  API](https://www.codecademy.com/articles/rebrandly-signup).

Keep  in  mind,  while  it’s  ok  to  use  your  API  key  in  these  exercises,  you  should not share your key with anyone (not even if asking a question in the  forums)! Also, if you reset the exercise at any point, you will have to paste in  your  API key again at  the top.

Instructions  1.

Assign apiKey  to  your  Rebrandly  API  key  as a  string.

![](Images/image04564.jpeg)If you do not assign the correct key, you will not see the proper results in  the  steps afterwards.

Checkpoint 2  Passed

Stuck?  Get a hint

2.

Inside  the  code  block  of  shortenUrl(),  create

a  const  named urlToShorten  and  assign it  inputField.value.  urlToShorten  will  keep  the  value of what is being  typed into  the input field.

Please  note, you will be  working  inside  shortenUrl()  for the  remainder of  this exercise.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Underneath  urlToShorten, create another  const  named  data,  and assign it  to  the result of calling the method  JSON.stringify()  with  {destination:  urlToShorten}  as an argument.

The  reason for creating  data  is to prepare the information needed to send  in  the body.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Below  data, call the  fetch()  function.  Pass it  url  as  its first argument  and  an  empty  object as its second argument.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Now it’s time to add some properties to the empty object that you just  created. Create a property  with the key  method  and  the value  'POST'.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

In the same object, create another property. The key for this property  is  headers  and  the value will be another object.

Assign headers  the value  of another  object listed  below:

![](Images/image05069.jpeg)

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

In  that same object  that  has the properties  method  and  headers, add  another  property. The key is named  body  and the value  will be  data.

Setting  up  this  information now  will make  chaining  .then()  in  the  next  exercise  much easier!

![](Images/image05070.jpeg)

![](Images/image05071.jpeg)

fetch()  POST Requests IV

In the previous exercise you’ve positioned yourself to make the POST  request by providing the endpoint and the object containing all the  necessary  information. In this  exercise you’ll handle the  response.

The request returns a Promise which will either be resolved or rejected. If  the  promise resolves, you  can use that information  and the  ok  status.  Let’s  implement  that knowledge into your  code!

If you reset the exercise at any point, you will have to paste in your API key  again  at the top!

Instructions  1.

Chain  a .then()  method to the  end of the  fetch()  function you wrote in the  previous exercise. As its first argument, pass it an arrow function as a  callback that takes  response  as its single parameter.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside the block of the function you made in Step 1, use a conditional  statement to  check the  value of the  ok  property of  response.  If  it evaluates to  a  truthy value,  call  renderJsonResponse()  and pass in  response.

Run  the code.

Now,  if  you post  a URL,  you  should see the  object that was sent  back!

renderJsonResponse()  is  a  helper  function  found  in  public/helperFunctions.js.

 Checkpoint 3 Passed

3.

Great, now that you see the raw object, you will need to pass the JSON to  the  next  .then(). Delete  renderJsonResponse(response)  and replace  it

with  return  response.json()

 Checkpoint 4 Passed

4.

Below  the curly braces of the conditional statement,  throw  a new  Error  in  case  response.ok  is falsy.

The  message  the  error should  raise  is  ‘Request  failed!’.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Outside of the code block from the first callback function you wrote, add  another arrow callback function that takes  networkError  as a single  parameter.

console.log()  the  networkError.message  inside  of  the  callback function  you  just  wrote.

By adding this second callback, you’re safeguarding yourself in the rare  event  that the network returns an  error!

![](Images/image05072.jpeg)

![](Images/image05073.jpeg)

fetch()  POST Requests V

You’re  almost  done  with the POST  request you started  a  few  lessons back!

In  fact,  this time you’ll  add another  .then()  to the chain to  finally  make the  information  available to your  webpage!

If you reset the exercise at any point, you will have to paste in your API key  again  at the top!

Instructions  1.

Chain  a .then()  method to the end of the original  .then()  method.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Pass in an anonymous arrow function as an argument for  .then(). This  callback function will take  jsonResponse  as its single parameter.

Inside  the  callback  function,  call  renderRawResponse()  and  pass  in  jsonResponse.

Run  the code.

Put in any URL in the text field, and then click the shorten button on the  webpage. Make sure you include the entire link, including ‘http://‘ or  ‘https://‘.

You’ll  see the JSON of  the response sent back from  the API.

The  renderRawResponse()  helper function  can be  viewed  at  public/helperFunctions.js.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Delete  renderRawResponse(jsonResponse). In its place,  call  renderResponse()  and passing  in  jsonResponse.

Run  the code.

Put a URL into the text field again and then click the Shorten button on the  web  page. Notice  the difference?

The  renderResponse()  helper function can be viewed  at  public/helperFunctions.js.

![](Images/image05074.jpeg)

![](Images/image05075.jpeg)const  inputField  =  document.querySelector('#input');  const  shortenButton  =  document.querySelector('#shorten');

const  responseField  =  document.querySelector('#responseField');

//  AJAX  functions

const  shortenUrl  =  ()  =>  {

const  urlToShorten  =  inputField.value;

const  data  =  JSON.stringify({destination:  urlToShorten})

fetch(url, {  method: 'POST',  headers:  {

'Content-type': 'application/json',  'apikey':  apiKey

},

body:  data

}).then(response => {  if  (response.ok)  {

return  response.json();

}

throw  new  Error('Request  failed!');

}, networkError => {  console.log(networkError.message)

}).then(jsonResponse => {  renderResponse(jsonResponse);

})

}

// Clear page and call AJAX functions  const  displayShortUrl  =  (event)  =>  {

event.preventDefault();  while(responseField.firstChild){

responseField.removeChild(responseField.firstChild)

}

shortenUrl();

}

shortenButton.addEventListener('click',  displayShortUrl);

async  GET  Requests I

Let’s  take a  minute to  appreciate what  you’ve  accomplished  so far:

• used  fetch()  to make GET and POST requests.

• check  the status  of the  responses coming back

• catch  errors  that  might possibly  arise

• taking successful responses and rendering it on the webpage  That  is fantastic! It’s the  basis of how  the  internet works!

In the following exercises, we’re going to take what you’ve learned about chaining  Promises  and make it simpler  using functionality introduced in  ES8:  async  and  await.  You  read that  right, you  did the  hard part  already, now  it’s time  to make  it easier.

The structure for this request will also be slightly different. Notice the new  keywords  async  and  await, as well  as the  try  and  catch  statements.

![](Images/image05076.jpeg)

async  GET Requests II

We are going to walk through and recreate the boilerplate code necessary  to  create a GET request using the  async  and  await.

Here  are some key points to  keep in mind as we  walk  through the code:

• Using an  async  function that  will  return a  promise.

• await  can only  be used in an  async  function.  await  allows a program to  run  while waiting for  a promise to resolve.

• In a  try...catch  statement, code in the  try  block will be run and in  the  event of an exception/error, the code  in the  catch  statement will  run.

Feel  free to  refer to the  async/await  GET  diagram at  any point while  completing this  exercise:

• [async/await  GET  diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/async%20await%20GET%20diagram.svg)

Instructions  1.

In  main.js,  create  an arrow  function using the  async  keyword and save it to  a  const  getData.

The  async  keyword  will ensure that  the  function returns a promise.  Check  the hint  for syntax help.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

In  the  code block for  getData,  we  should  add a  try  statement  with an empty  code block.

Below the  try  statement’s code block,  add a  catch(error)  statement.

The  code in  the  try  block  will send  a request and  handle the response.  The  catch  statement  will then take care of an  error if it  is thrown.

Check  the  hint  for  syntax help.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

Inside the  catch  code  block, log  error  to the  console.

Since this exercise is an example, we’re using  console.log()  to view the  error. Generally, developers create a more sophisticated way of handling  the error, like redirecting their users to another page, but logging is fine for  us  at the moment.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Now  we have to  consider  what  to do inside of the code  block of

the try  statement. We should start by using the  await  keyword before  calling  fetch(). Pass in the following URL, as a string, to the function as its  first  argument:

https://api-to-call.com/endpoint  We’ll have to save the returned promise in a variable called  response  using  the const  keyword.  response  will save the response of endpoint once that  information  has been sent back.

Check  the  hint  for  syntax help.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Under  response, create  a  conditional statement  that checks  if

the  ok  property  of the  response  object  evaluates  to a truthy  value.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Inside  the code block of the conditional statement,  await  the resolution  of  calling the  .json()  method on  response.

Save  the  returned  object  to a  variable  called  jsonResponse  using  the  keyword  const.

Since .json()  is an asynchronous method we have to  await  until the  promise status is resolved. Then we store the value to know what data the  JSON holds.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Return jsonResponse  directly below  the code  you  wrote  in the  previous  step.

Normally,  we’d  want to use the information  from  jsonResponse  in a different  manner.  In this  exercise, we’re  practicing how to  write the  boilerplate code.

 Checkpoint 8 Passed

8.

Below  the  conditional statement,  throw  a  new  Error. The  message the  error  should  raise is  ‘Request failed!’.

![](Images/image05077.jpeg)

async  GET Requests III

In the previous exercise, we created the boilerplate code for making a GET  request using  async  and  await.

In this exercise, you’re going to build on previously created boilerplate code  to  get  nouns that describe  the inputted  word  from the  Datamuse API:

• [Datamuse  API Documentation](https://www.datamuse.com/api/).

![](Images/image05078.jpeg)

1.

Under the comment “AJAX function”, create a new arrow function  called  getSuggestions()  using the  async  keyword.

You’ll  be coding inside the arrow function  of  const  getSuggestions  for the  remainder  of  this exercise.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

Inside  the code block of  the  async  arrow  function, create  a  const  variable  named  wordQuery  and  assign it  inputField.value.

 Checkpoint 3 Passed

3.

Create  another const  called  endpoint,  assign it value of  a string that  is  url,  queryParams, and  wordQuery  concatenated in  that  order.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

Add  a  try  statement  with an empty  code block. Outside the code block  for  try, add a catch(error)  statement with a code block that logs  error  to the  console.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Inside the  try  code block, using  const, create a  variable named  response  and  assign it to  await  the result of calling  fetch()  with  endpoint  as the first  argument. For this API to work within the provided browser, add  {cache:  'no-cache'}  as the  second argument.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

Below the variable  response  from the previous step, create a conditional  statement  that  the  checks if  the  ok  property of  the  response  evaluates  to a  truthy  value.

Inside  the  code block  of the  conditional

statement, await  response.json()  and save it to a  variable  called  jsonResponse  using the  const  keyword.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Call  the  function renderRawResponse()  and pass  in  jsonResponse.  Then, run  the  code.

In the response field, type in a word and click the submit button on the web  page.

You should now see an array of objects that contain nouns that describe  the  word you typed in!

You  can  view  the  purpose of  the  renderRawResponse  helper function  at  public/helperFunctions.js.

 Checkpoint 8 Passed

Stuck?  Get a hint

8.

Now that you can see the body of  response, you should clean it up to  display  on the  webpage.

Delete  renderRawResponse(jsonResponse)  and  replace  it

with  renderResponse(jsonResponse). Run the code. Then type in another word  and  click the submit button.

Great, now you have an organized list of words and you finished your GET  request!

You  can  view  the purpose  of  renderResponse  function  at  public/helperFunctions.js.

![](Images/image05079.jpeg)//  Information to  reach  API

const url = 'https://api.datamuse.com/words?';  const  queryParams  = 'rel_jja=';

//  Selecting  page  elements

const inputField = document.querySelector('#input');  const  submit  =  document.querySelector('#submit');

const  responseField  =  document.querySelector('#responseField');

//  AJAX  function

//  Code  goes here

const getSuggestions = async () => {  const  wordQuery  =  inputField.value;

const endpoint = `${url}${queryParams}${wordQuery}`;  try  {

const response = await fetch(endpoint, {cache: 'no-cache'});  if(response.ok){

const jsonResponse = await response.json();  renderResponse(jsonResponse);

}

} catch (error) {  console.log(error);

}

}

// Clear previous results and display results to webpage  const  displaySuggestions  = (event)  =>  {

event.preventDefault();  while(responseField.firstChild){

responseField.removeChild(responseField.firstChild);

}

getSuggestions();

}

submit.addEventListener('click',  displaySuggestions);

async  POST Requests I

Now  that  you’ve  made an  async  GET request, let’s start on getting you  familiar  the  async  POST request.

As  with the other GET  and POST requests that you’ve been  making,  an  async  POST  request  requires more information. Take a  look at  the diagram.

We  still have the same structure of using  try  and  catch  as  before. But, in

the  fetch()  call, we now have to include an  additional  argument that contains more  information like  method  and  body.

We’ll  be  explaining the why’s and how’s of the boilerplate  code  for  async  POST  requests  in the  next lesson.

async  POST Requests II

Now  we’re going  to  piece together a POST  request using  async  and  await.

Feel  free to  refer to the  async/await  diagram below at any point  while  completing this  exercise:

• [async/await  POST  diagram](https://content.codecademy.com/courses/intermediate-javascript-requests/diagrams/async%20await%20POST%20diagram.svg)

Instructions  1.

At  the top of main.js  create an  async  arrow  function and  save it  to  a  const  getData().

The  async  keyword will ensure that the  function  returns a promise.

 Checkpoint 2 Passed

Stuck?  Get a hint

2.

In  the  code block for  getData,  we  should  add a  try  statement  with an empty  code block.

In  case things go  wrong,  we need some  code to handle that.  Below

the  try  code block,  add  a  catch  statement and  pass in  error  as an argument.

Then, in  the  catch  statement code block, log  error  to the console.

 Checkpoint 3 Passed

Stuck?  Get a hint

3.

We  now have to consider  what we want  to do inside of  the  try  code block.

Since we are making a POST request, we should start by using  the  await  keyword before calling the  fetch()  function.

We will have to save the returned promise in a variable  called  response  using the  const  keyword.

 Checkpoint 4 Passed

Stuck?  Get a hint

4.

In  the fetch()  call that  we just made, pass in the  following URL  to the  function  as a  string for the first argument:

https://api-to-call.com/endpoint

Then  as our  second argument, let’s  pass in an  empty object for  now.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

Let’s  now  fill in  the request options  in our  second  argument.

First,  add the  method  property and  the value  is  'POST'.  Then  we have to  include a  body  property  and the  value is  JSON.stringify({id: 200}).

Remember  to  separate the  properties with  a comma.

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

After the code block of  response, we should  create an  if  statement  that  checks  the  ok  property of the  response  object.

Inside  the code block of the conditional statement,  await  the resolution  of  calling the  .json()  method on  response. Save the returned object to a  variable called  jsonResponse  using the keyword  const.

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Now  that  we  have what  we want, we should return  jsonResponse  directly  below  the code written in the  previous step.

Like  with  previous  boilerplate exercises,  we’re  practicing  writing code.

Normally, we would want to do more beyond this step of  returning  jsonResponse.

 Checkpoint 8 Passed

8.

Below  the if  conditional,  throw  a  new Error()  with the message  'Request  failed!'

Nice  work, didn’t that feel  very similar  to making  a GET  request?

![](Images/image05080.jpeg)

async  POST Requests III

Since you’ve created the boilerplate code for a POST request, the next step  is  to incorporate that experience  and logic into making  a real request.

In this exercise, you’ll need to retrieve your Rebrandly API key to access the  Rebrandly  API.

• [Rebrandly  API Keys](https://app.rebrandly.com/account/api-keys).

If you reset the exercise at any point, you will have to paste in your API key  again  at the top!

![](Images/image05081.jpeg)

1.

![](Images/image04915.jpeg)![](Images/image05082.jpeg)At  the  top of main.js,  assign

Checkpoint 2  Passed

2.

to  your Rebrandly  API key.

![](Images/image05083.jpeg)Checkpoint 3  Passed

Stuck?  Get a hint

3.

Inside  the  code block  of the arrow function of  shortenUrl  create two  consts:  One  named urlToShorten  and  assign it  inputField.value.

The  other  named  data  and  assign  it the value  of calling  JSON.stringify()  and  passing  in  {destination: urlToShorten}.

Please  note,  we  will be working inside  shortenUrl()  for the remainder  of the  exercise.

 Checkpoint 4 Passed

4.

Add  a  try  statement  and leave the code block empty  for  now. After  the  try  code block,  create a  catch  statement  and pass in  error.

In  the  code block of  catch(error),  log  error  to  the console.

 Checkpoint 5 Passed

Stuck?  Get a hint

5.

![](Images/image05084.jpeg)Inside the  try  code block, using  const, create a  variable named  response  and  assign it to  await  the value of calling calling  fetch().

 Checkpoint 6 Passed

Stuck?  Get a hint

6.

In  the fetch()  call, pass  in  url  as  the first  argument  and an empty  object  as  the second  argument.

In that empty object you just created. It will have the following three  properties:

• method  with a value  of  'POST'

• body  with a  value  of  data

• headers  with a  value of the  object below:

![](Images/image05085.jpeg)

 Checkpoint 7 Passed

Stuck?  Get a hint

7.

Below  the  variable  response  from the previous step,  create  a conditional  statement that the checks if the  ok  property of  response  evaluates to a  truthy  value.

 Checkpoint 8 Passed

Stuck?  Get a hint

8.

Inside  the  code block  of the  conditional

statement, await  response.json()  and save it to a  variable  called  jsonResponse  using the  const  keyword.

 Checkpoint 9 Passed

9.

Call  the  function renderRawResponse()  and pass  in  jsonResponse.  Then, run  the  code.

In  the response  field,  you can  paste in a  URL and  click the shorten  button.

You should now see an object containing all the information the Rebrandly  API sent back!

You  can  view  the  purpose of  the  renderRawResponse()  helper function  at  public/helperFunctions.js.

 Checkpoint 10  Passed

10.

Now  it’s time to clean up  the  response sent back.

Delete  renderRawResponse(jsonResponse)  and  replace  it

with  renderResponse(jsonResponse). Run the code. Then paste in the URL  again  and click the shorten button.

Notice  the  formatted response.

Great  job  using Rebrandly  to  shorten your  URL!

You  can  view  the  purpose of  the  renderRawResponse()  helper function  at  public/helperFunctions.js.

![](Images/image05086.jpeg)

![](Images/image05087.jpeg)

Review  Requests II

Let’s  recap on  the concepts  covered in  the previous exercises:

1. GET  and POST  requests can  be created  a variety  of ways.

2. Use  AJAX  to asynchronously  request  data from

APIs. fetch()  and  async/await  are  new functionalities  developed  in ES6  (promises)  and  ES8 respectively.

3. Promises are a new type of JavaScript object that represent data that will  eventually  be returned from a request.

4. fetch()  is a web API that  can be used to create  requests.  fetch()  will return  promises.

5. We  can chain  .then()  methods to handle promises  returned by  fetch().

6. The  .json()  method  converts a returned  promise to  a  JSON object.

7. ![](Images/image05088.jpeg)is  a  keyword that  is used  to create  functions that  will return  promises.

8. is a keyword that is used to tell a program to continue moving through  the  message queue while  a promise resolves.

9. await  can only be  used within  functions declared with  async.
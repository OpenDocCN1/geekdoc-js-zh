![](cover.jpeg)

## **Contents**

[CHAPTER ONE Introduction](#part0001.html_UGI0-be68632f57af4bd3967d594a82bfa4b5)

[CHAPTER TWO arrays](#part0002.html_1T140-be68632f57af4bd3967d594a82bfa4b5)

[CHAPTER THREE conditionals](#part0003.html_2RHM0-be68632f57af4bd3967d594a82bfa4b5)

[CHAPTER FOUR functions](#part0004.html_3Q280-be68632f57af4bd3967d594a82bfa4b5)

[CHAPTER FIVE numbers](#part0005.html_4OIQ0-be68632f57af4bd3967d594a82bfa4b5)

[CHAPTER SIX objects](#part0006.html_5N3C0-be68632f57af4bd3967d594a82bfa4b5)

[CHAPTER SEVEN strings](#part0007.html_6LJU0-be68632f57af4bd3967d594a82bfa4b5)

[CHAPTER EIGHT miscellaneous](#part0008.html_7K4G0-be68632f57af4bd3967d594a82bfa4b5)

CHAPTER ONE

Introduction

Introduction  

I've been working with code for over 30 years now. I still find new things to learn about coding every day. Here is a small collection of JavaScript tips tricks and techniques that I have picked up over the years.

You can download samples of this code at my website, [WilliamClarkson.net](https://www.williamclarkson.net/code), and if you have any questions about the code or JavaScript in particular you can contact me there and I'll be happy to do my best to help you.

I love talking about code!

If you are interested in using JavaScript for game design you might want to check out some of my other books, or my website on game development [phasergames.com](https://www.phasergames.com).

I hope you enjoy this collection of JavaScript Snippets!

CHAPTER TWO

arrays

Array to list

This is a handy little function I've used in a couple of my programs to be able to convert an array to an HTML list.

function arrayToList(array) {

var oString = "<ol>";

var len = array.length;

for (var i = 0; i < len; i++) {

var word = array[i];

oString += "<li>" + word + "</li>";

}

oString += "</ol>";

return oString;

}

window.onload = function() {

document.getElementById('output').innerHTML = arrayToList(['red', 'blue', 'green']);

}

Cache the array length

Storing an array length in a variable means that the browser will not have to calculate the length of the array every time the loop is executed. I've seen good performance results on my own code over the years.

Some research seems to suggest that the browser makers realizing that the array had to be calculated every time have now done workarounds to cache the array length for you, however, I still like to do it. It is also a good practice because you never know how old the browser that your user is using.

not cached

for (i = 0; i < array.length; i++) {

//do stuff

}

cached

var len = array.length;

for (var i = 0; i < len; i++) {

//do stuff

}

Binary search

This is a trick I used way back in the 80s when computers were a lot slower than they are today. It works only on arrays that are alphabetically sorted but you could also modify this code where you have an array of objects it's alphabetically sorted on a key.

It works like this: imagine that you have a telephone book and you want to find a certain name. You don't start at the letter A and work your way through until you find the name that you are looking for. However, that's how we often do it in programming with just a for Loop going through every name until we find the one that we want. With the phone book, we open it to a random page and then turn forwards or backward depending on where we landed. This code looks at the element in the middle or halfway through the array. It did either discards the last half or the first half of the array depending on if the name that is looking for is greater than or less than the value of that middle element. It keeps discarding half of the array until it finds the one that it wants

function binSearch(array, value) {

var first = 0,

last = array.length - 1,

middle = Math.floor((last + first) / 2);

while (array[middle] != value && first < last) {

if (value < array[middle]) {

last = middle - 1;

} else if (value > array[middle]) {

first = middle + 1;

}

middle = Math.floor((last + first) / 2);

}

return (array[middle] != value) ? -1 : middle;

}

var array = ['Norberto', 'Fay', 'Leonia', 'Silvana', 'Julieann', 'Nubia', 'Verlene', 'Mittie', 'Ophelia', 'Kali', 'Mertie', 'Alaine', 'Caryn', 'Joeann', 'Leonie', 'Carolina', 'Kimber', 'Lacresha', 'Lianne', 'Tatiana'];

//sort the array

array.sort();

console.log(binSearch(array, 'Nubia'));

//returns 5

Clear array

A quick little trick to empty out an array that you want to keep using it simply to set the length of the array to zero.

var array = [11, 22, 33, 44, 55, 66];

//

console.log(array);

//set length to zero

//

array.length=0;

//

console.log(array);

Truncate array

Just as setting an array length 0 will clear the array, you can also truncate the array by setting the length to the number of elements you want to keep.

var array = [11, 22, 33, 44, 55, 66];

//

console.log(array);

//set length to zero

//

array.length=3;

//

console.log(array);

Output

[11,22,33]

Slice vs Delete

Deleting an element on an array will set that element to undefined. Slice will simply remove it.

//array.splice(index,delete_count)

array.splice(position, 1);

delete array[1];

delete output

[ 'a', undefined, 'c' ]

splice output

[ 'a', 'c' ]

Shuffle

The shuffle array function will take two random elements of an array and swap their values. I use this function a lot in card games.

var array = [1, 2, 3, 4, 5, 6, 7];

for (var i = 0; i < 20; i++) {

array = shuffleArray(array);

}

function shuffleArray(arr) {

var index1 = Math.floor(Math.random() * arr.length);

var index2 = Math.floor(Math.random() * arr.length);

//

//

var temp = arr[index1];

arr[index1] = arr[index2];

arr[index2] = temp;

return arr;

}

Get last element

Use the built-in array slice function to be able to get a list of elements from the end of an array.

var array = [1, 2, 3, 4, 5, 6,7,8,9];

get last element

console.log(array.slice(-1)); // [9]

get last two elements

console.log(array.slice(-2)); // [8,9]

Join 2 arrays

If you want to join two arrays together take the array that you want to go at the beginning and then concat the second array to it

var array1 = [1, 2, 3];

var array2 = [4, 5, 6];

var array3=array1.concat(array2);

console.log(array3);

Output

[1,2,3,4,5,6];

Using Array.find

Use the array built-in find function to quickly search through an array of objects.

const animals = [

{ type: 'Dog', name: 'Rover'},

{ type: 'Cat', name: 'Eliza'},

{ type: 'Cat', name: 'Angel'}]

animal = animals.find(animal => animal.type ==='Cat' && animal.name === 'Eliza');

console.log(animal);

Output

{ type: 'Cat', name: 'Eliza' }

Get random element

This function will pick an element at random from the array.

var items=['fishes','cats','dogs','elephants'];

var randItem = items[Math.floor(Math.random() * items.length)];

Get unique values

There are two methods listed here to be able to get unique elements from an array the first one is an older one that I've used over the years the second one is a new way of accomplishing the task with functionality more recently added to JavaScript.

//old method

function getUniques(array) {

var uArray = [];

var len = array.length;

for (var i = 0; i < len; i++) {

uArray[array[i]] = 1;

}

var nArray = [];

for (var key in uArray) {

nArray.push(key);

}

return nArray;

}

console.log(getUniques([1, 2, 3, 'fish', 3, 'cake', 'cake', 'cake', 1, 2, 3, 4, 'fish']));

//ES6 -newer shorter method

var arr = [...new Set([1, 2, 3, 'fish', 3, 'cake', 'cake', 'cake', 1, 2, 3, 4, 'fish'])];

console.log(arr);

Output

[1,2,3,'fish','cake',4]

CHAPTER THREE

conditionals

Conditinal shortcurt

Instead of using an if statement to call a function you can simply take the condition and use the ‘and’ (&&) to call the function if the conditional is true.

old way

if (conected) {

login();

}

new way

conected && login();

Ternary operator

Using a ternary operator can shorten several lines of if-then code into one

old way

var age = 19;

var canDrink;

if (age > 20) {

canDrink = true;

} else {

canDrink = false;

}

new way

var age = 19

canDrink=(age>20)?true:false;

Console.log(canDrink);

The formula for this is:

variable=(condition)?meetsCondition:doesNotMeetCondition

Ternary operator with methods

You can also use ternary operators to call a method.

old way

if (success) {

avatar.start();

} else {

avatar.stop();

}

new way

success ? avatar.start() : avatar.stop();

Switch vs If

Using a switch statement instead of a series of if-then statements will make your code more readable and in some cases speed up the execution.

old way

if (color == "red") {

//do stuff

}

if (color == "blue") {

//do stuff

}

if (color == "green") {

//do stuff

}

if (color == "brown") {

//do stuff

}

if (color == "yellow") {

//do stuff

}

new way

switch (color) {

case "red":

//do stuff

break;

case "blue":

//do stuff

break;

case "green":

//do stuff

break;

case "brown":

//do stuff

break;

case "yellow":

//do stuff

break;

}

CHAPTER FOUR

functions

Assumed Arguments

If you want to be able to send an unfixed amount of arguments to a function, you can just leave the argument section blank and then use the arguments keyword to access any parameters past. It's worth noting that although the arguments act as an array it is not an actual JavaScript array.

function sum1(a, b) {

return a + b;

}

function sum2() {

return arguments[0] + arguments[1];

}

function sum3() {

var sum = 0;

for (var i = 0, len = arguments.length; i < len; ++i) {

sum += arguments[i];

}

}

sum1(1,2);

sum2(1,2);

sum3(1,2,3,4,5,6,7,8,9);

Object vs Parameters

Many times when I am writing classes there are times when I will wind up with 10 to 15 parameters being passed to the constructor. Some of the parameters are optional so when I want to add a required parameter later I have to go back and change a lot of code. I have found in some cases passing a single object as a sole parameter saves a lot of time

function doAttack(weapon, damage, monster, useMagic = false) {

console.log('you use the ' + weapon + ' on the ' + monster);

}

function doAttack2(obj) {

console.log('you use the ' + obj.weapon + ' on the ' + obj.monster);

}

doAttack('sword', 10, orc);

var attackObj = {

'weapon': 'sword',

'damage': 10,

'monster': 'orc'

};

attackObj.extraStuff = 'whatever';

attackObj.speed = 10;

doAttack2(attackObj);

Defaults

Use the double pipe (||) ‘or’ keyword to set defaults to a variable. The defaults will be set if no value is passed for that variable.

function User(name, age) {

this.name = name || "Oliver Stirling";

this.age = age || 63;

}

Short Hand Functions

You can use double arrow notation to create a function.

function calcCircumference(diameter) {

return Math.PI * diameter

}

calcCircumference = diameter => (Math.PI * diameter;)

CHAPTER FIVE

numbers

Even or Odd?

If you divide a number by 2 and there is no remainder it is an even number else it is odd.

function isEven(num)

{

return num/2==Math.floor(num/2);

}

Is divisible by?

Use this function to tell if a number is divisible by another number without remainders.

function isDivisbleBy(num, div) {

return (num / div == Math.floor(num / div));

}

Get Max or Min values

Use the built-in math functions of JavaScript to get the maximum or minimum number in an array

var numbers = [3, 3354, 143, -245, 118, 400, 122222, -80011];

var maxInNumbers = Math.max.apply(Math, numbers);

var minInNumbers = Math.min.apply(Math, numbers);

//

//

console.log("max", maxInNumbers);

console.log("min=" + minInNumbers);

Output

122222

-80011

Random In Range

This function will return a random whole number between the two numbers that are passed to it.

function between(start, end) {

return Math.floor(Math.random() * (end - start + 1)) + start;

}

Round to decimal places

This bit of code is good for rounding off to a certain decimal place

var num =8.675309;

num = Math.floor(num*1000)/1000;

//10 for 2 places

//100 for 3 places

//1000 for 4 places

String to Number

Use the plus sign operator to convert a string to a number.

function toNumber(strNumber) {

return +strNumber;

}

var myNum=toNumber('213');

console.log(myNum);

CHAPTER SIX

objects

Array to object

Use the ...arr keyword to convert an array to an object

var arr = [ 'fish', 'chicken', 100]

var obj = { ...arr }

console.log(obj)

Output

{0: "fish", 1: "chicken", 2: 100}

Clone Object

We can use JSON to turn an object into a string and then use that string to create a new object.

var obj={'name':'Jane','age':20};

var newObj = JSON.parse(JSON.stringify(obj));

newObj.age=22;

console.log(obj);

console.log(newObj);

Output

{name: "Jane", age: 20}

{name: "Jane", age: 22}

Shorthand create

If you pass variables into an object without a key-value pair the name of the variable will become the key with the value set.

var x=10;

var y=10;

var obj = { x:x, y:y };

console.log(obj);

var obj2={x,y};

console.log(obj2);

Output

Both objects will output as: {x: 10, y: 10}

CHAPTER SEVEN

strings

Cap first letter

Put the first letter of a word in caps.

function capFirstLetter(word) {

return word.charAt(0).toUpperCase() + word.slice(1);

}

Get words

Split a sentence into an array of words.

function getWords(sentence) {

var words=sentence.split(" ");

return words;

}

Cap all words

Let's combine a couple of the functions we've already made and capitalize the first letter of every word in a sentence.

function capAllWords(sentence) {

var words = sentence.split(" ");

var numWords = words.length;

for (var i = 0; i < numWords; i++) {

words[i] = words[i].charAt(0).toUpperCase() + words[i].slice(1);

}

return words;

}

Multi-line text

Use backticks for line returns instead of escape characters.

Old way

var lorem = 'Lorem ipsum dolor sit amet, consectetur\n\t'

+ 'adipisicing elit, sed do eiusmod tempor incididunt\n\t'

+ 'ut labore et dolore magna aliqua. Ut enim ad minim\n\t'

+ 'veniam, quis nostrud exercitation ullamco laboris\n\t'

+ 'nisi ut aliquip ex ea commodo consequat. Duis aute\n\t'

+ 'irure dolor in reprehenderit in voluptate velit esse.\n\t';

New way

var lorem = `Lorem ipsum dolor sit amet, consectetur

adipisicing elit, sed do eiusmod tempor incididunt

ut labore et dolore magna aliqua. Ut enim ad minim

veniam, quis nostrud exercitation ullamco laboris

nisi ut aliquip ex ea commodo consequat. Duis aute

irure dolor in reprehenderit in voluptate velit esse.`;

Random String

This function is useful for generating test data and nonces.

makeRandString(len) {

var text = "";

var letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";

for (var i = 0; i < len; i++) {

text += letters.charAt(Math.floor(Math.random() * letters.length));

}

text += " ";

return text;

}

makeRandString(10);

Remove double spaces

Sometimes double spaces creep into strings from user input. This function will remove the double spaces.

function removeDoubleSpaces(text) {

for (var i = 0; i < 100; i++) {

text = text.split(" ").join(" ");

}

return text;

}

var myText = removeDoubleSpaces("test me to see if I remove all double spaces or not !");

console.log(myText);

Replace all

This function splits a string by the needle or search phrase and then rejoins the array into a string using the replace keyword as the delimiter

function replaceAll(haystack,needle,replace)

{

var array=haystack.split(needle);

var str=array.join(replace);

return str;

}

var myString="It was the best of times, it was the worst of times";

myString=replaceAll(myString,'times','occasions');

Returns

It was the best of occasions, it was the worst of occasions

Find string in string

Use this function to tell if one string contains another

function contains(haystack,needle)

{

return string.indexOf(substring)!=1;

}

//

//

console.log(contains("the quick brown fox jumped over the lazy dog","fox"));

Returns

true

CHAPTER EIGHT

miscellaneous

Shortcut for console.log

If you use console.log a lot you can shorten that function and save yourself from some typing by binding the function to the document

var cl = console.log.bind(document);

cl('shorter to type');

Output

shorter to type

cl(1 + 1);

Output

2

console.table

Use table.log to see a visual representation of your objects in the console.

var person={'name':'Hero','hp':100};

console.table(person);

![ ](images/00001.jpeg)

Using classes

Classes are a fairly new addition to JavaScript. this allows us a lot more flexibility than the old function object.

function Person(firstName, lastName) {

this.firstName = firstName;

this.lastName = lastName;

}

class Person2 {

constructor(firstName, lastName) {

this.firstName = firstName;

this.lastName = lastName;

}

sayName()

{

console.log("Hi "+this.firstName);

}

}

var player = new Person('Bob', 'Smith');

var player2=new Person2('Bob','Smith');

player2.sayName();

Extending Classes

By using the Extends keyword we can take all the properties and methods of one class and add on to them in our new class.

class Person2 {

constructor(firstName, lastName) {

this.firstName = firstName;

this.lastName = lastName;

}

sayName() {

console.log("Hi " + this.firstName);

}

}

class Superman extends Person2 {

constructor(firstName, lastName) {

super(firstName, lastName);

}

fly() {

console.log("up up and away");

}

}

var player = new Superman('Clark', 'Kent');

player.sayName();

player.fly();

Linked List

A linked list is a series of objects that have a reference to either the previous item the next item or both. using a linked list can have a great advantage over looping through items. I use it frequently when I'm making virtual worlds and it really speeds up the the program.

class Person {

constructor(name) {

this.name = name;

this.nextPerson = null;

}

sayName() {

console.log(this.name);

if (this.nextPerson) {

this.nextPerson.sayName();

}

}

}

var names = ['Aubrey', 'Marlin', 'Brittanie', 'Summer', 'Araceli', 'Jolie', 'Denyse'];

//

//

var firstPerson = null;

var previousPerson = null;

//

//make the list

var len = names.length;

for (var i = 0; i < len; i++) {

//make a new person

var person = new Person(names[i]);

//set first person to current if not already set

if (firstPerson == null) {

firstPerson = person;

}

//if previousPerson exists then assign current person as next

if (previousPerson) {

previousPerson.nextPerson = person;

}

previousPerson = person;

}

//call the first person sayName function

//to start a chain reaction

firstPerson.sayName();

Delete a linked list element

To remove elements from a linked list we need to have a reference to both the next and previous elements of the list. To remove an element we simply take the previous element and set the next item to the next item of the item we're deleting. It makes more sense in the code!

class Person {

constructor(name) {

this.name = name;

this.nextPerson = null;

this.previousPerson = null;

}

sayName() {

console.log(this.name);

if (this.nextPerson) {

this.nextPerson.sayName();

}

}

removeByName(name) {

if (this.name == name) {

this.previousPerson.nextPerson = this.nextPerson;

}

if (this.nextPerson) {

this.nextPerson.removeByName(name);

}

}

}

var names = ['Aubrey', 'Marlin', 'Brittanie', 'Summer', 'Araceli', 'Jolie', 'Denyse'];

//

//

var firstPerson = null;

var lastPerson = null;

//

//

var len = names.length;

for (var i = 0; i < len; i++) {

//make a new person

var person = new Person(names[i]);

//set first person to current if not already set

if (firstPerson == null) {

firstPerson = person;

}

//if lastPerson exists then assign current person as next

//asign lastPerson to previousPerson of current person

if (lastPerson) {

lastPerson.nextPerson = person;

person.previousPerson = lastPerson;

}

lastPerson = person;

}

firstPerson.removeByName('Summer');

firstPerson.sayName();

Collision detection

This is a function I use in a lot of my games to tell if two objects are touching each other.

function checkCollide(obj1, obj2) {

var distX = Math.abs(obj1.x - obj2.x);

var distY = Math.abs(obj1.y - obj2.y);

if (distX < obj1.width / 2) {

if (distY < obj1.height / 2) {

return true;

}

}

return false;

}

var obj1={x:100,y:100,width:200,height:50};

var obj2={x:150,y:120,width:200,height:50};

checkCollide(obj1,obj2);

Convert to Boolean

Use double exclamation points (!!) to turn a number into a Boolean. Please note this only works with zero for false. negative numbers will still give a true value.

function checkPlayerHealth(hitPoints) {

var isAlive = !!hitPoints;

return isAlive;

}

console.log(checkPlayerHealth(100));

console.log(checkPlayerHealth(0));

Get URL of page

If you need to know the name of the page that you are on use window.location.href

function getUrl()

{

return window.location.href;

}

console.log(getUrl());

Local storage - Strings

Use local storage to store strings into the browser memory cache.

//set the value

localStorage.setItem('monsterName', 'orc');

//get the value

var name=localStorage.getItem('monsterName');

Local storage - Objects

To store an object into local storage first use JSON.stringify to turn it into a string.

var monsterObj = { 'name':'orc','health':100,'defense':20 };

// Put the object into storage

localStorage.setItem('monster', JSON.stringify(monsterObj));

// Retrieve the object from storage

//

var monsterObj = localStorage.getItem('monster');

var monster=JSON.parse(monsterObj);

Swap variables

Use anonymous arrays to be able to quickly swap values.

var a = 'world';

var b = 'hello';

[a, b] = [b, a]

console.log(a) //hello

console.log(b) //world

I hope you enjoyed this collection of JavaScript Snippets and please remember if you have any questions or found any mistakes please contact me at [WilliamClarkson.net](https://www.williamclarkson.net/code)